---
name: slop-check-ui
description: Rule-based UI validator that cites specific RULE-IDs from a 380-rule canonical library covering Component, Layout, Typography, Color, Hierarchy, Spacing, Image. Dispatches independent visual and code-lens sub-agents per category in parallel, then aggregates both perspectives. Use when the user explicitly wants traceable rule violations on UI mockups or codebase — e.g. "slop check this UI", "cite UI violations", "audit against design rules", "find UI consistency issues with rule IDs". Skip for vague "how does this look" or general feedback without explicit rule-citation intent.
---

# Slop Check (UI)

## Purpose

Rule-based UI validator. Returns specific `[RULE-ID]` citations for every issue found, grounded in either visual evidence (from mockup/screenshot) or code evidence (file:line, hard counts) — no hand-waving.

Backed by **380 canonical rules** across 7 categories.

## When to use

Trigger ONLY when the user explicitly wants **rule-based citation** of UI issues:
- "Slop check this UI"
- "Audit this mockup against design rules"
- "Find specific UI violations with rule IDs"
- "Validate this against canonical rules"
- "Cite UI issues by rule"

## When NOT to use

Skip this skill for:
- "Does this look good?" → vibes-based review without rule-citation intent
- "Give me feedback" → general critique without explicit rule-validation
- "Make this prettier" → aesthetic suggestions
- General brainstorming without an explicit rule-validation intent

## Architecture: two independent perspectives

This skill runs **two parallel review tracks per category** that do NOT influence each other:

1. **Visual track** — sub-agents read the mockup/screenshot and walk every canonical rule visually.
2. **Code track** — sub-agents grep/analyze the codebase against the same canonical rules from a code-evidence angle.

Each track is independent. Code findings do not bias visual review and vice versa. Aggregation happens AFTER both finish, so cross-reference (where both agree) signals high-confidence issues.

For each category, that means **2 sub-agents** (1 visual + 1 code). Across 7 UI categories, a full check dispatches **14 sub-agents** in parallel.

If only one input is available (mockup only OR codebase only), only that track runs — but both should be present for full coverage.

## Procedure

### Step 1 — Input handshake (MANDATORY)

Before dispatching anything, confirm with the user what's available:

```
What inputs do you have for this slop check?
  [a] Mockup screenshot(s) only       → visual track only (7 sub-agents)
  [b] Codebase path only              → code track only (7 sub-agents)
  [c] Both mockup(s) + codebase       → full review (14 sub-agents)  ← recommended
  [d] Live URL (Playwright/MCP)       → live screenshot + computed style inspection

How many pages are you submitting?
  - Multiple mockups (one per page)?
  - Codebase contains multiple pages/routes?
  - Live URL with multiple paths to navigate?
  Multi-page reviews surface systemic issues — same rule failing on
  many pages = system-level slop, not page-level.

Want to focus on specific categories? (e.g. "Color and Spacing only")
Or extend default scope? Default scope already covers:
  - Component duplication / shared component candidates
  - Token consistency (color, font, spacing, border-radius)
  - Inline style audit
  - Page hierarchy / button placement / layout consistency
  - Cross-page reference / unification
  - + standard rule walk per category
```

Do NOT proceed without input confirmation. If user just attaches a screenshot without saying anything, ask if they also want code analysis (most users want both). **Always enumerate pages explicitly** — even single-page reviews benefit from explicit page labeling.

### Step 2 — Identify platform & domain

- Mobile / PC / Web / Dashboard
- Domain: e-commerce, portfolio, dashboard, AI chat, fintech, travel, etc.

Briefly describe in 3-5 sentences (gets passed to every sub-agent as fallback context).

### Step 3 — Dispatch sub-agents in parallel

Use the `Task` / `Agent` tool to launch all relevant sub-agents in a single message. Each category gets up to 2 agents based on available inputs.

| # | Category | Visual sub-agent | Code-lens sub-agent |
|---|----------|------------------|---------------------|
| 1 | Component | mockup → COMP rules | grep JSX duplication, prop interfaces, shared components |
| 2 | Layout | mockup → LAYOUT rules | grep grid/flex patterns, container max-widths |
| 3 | Typography | mockup → TYPO rules | grep font-size/weight values, count distinct |
| 4 | Color | mockup → COLOR rules | grep color values (hex/rgb/tailwind), count distinct |
| 5 | Hierarchy | mockup → HIER rules | grep h1/h2/h3 per page, z-index sprawl |
| 6 | Spacing | mockup → SPACING rules | grep padding/margin/gap values, count distinct |
| 7 | Image | mockup → IMAGE rules | grep img tags, alt presence, src patterns |

Reference paths:
- `skills/slop-check-ui/reference/component.md`
- `skills/slop-check-ui/reference/layout.md`
- `skills/slop-check-ui/reference/typography.md`
- `skills/slop-check-ui/reference/color.md`
- `skills/slop-check-ui/reference/hierarchy.md`
- `skills/slop-check-ui/reference/spacing.md`
- `skills/slop-check-ui/reference/image.md`

### Step 4 — Collect, verify, aggregate

After all sub-agents return:
1. **Verify completion** — each sub-agent appends `Rules walked: N/total`. If under-counted or missing, re-dispatch.
2. **No pre-filtering, no cap** — keep every finding. The user wants the full picture. Aggregation = dedup + sort + format, not editorial.
3. **Dedup within track** — same rule cited twice within visual or code → keep one.
4. **Cross-reference** — when visual and code both flag the same area, mark as **high-confidence**.
5. **Severity sort** — High → Medium → Low, within each track.
6. **Merge per page** — visual and code findings on the same rule for the same page combine into one fix entry.

### Step 5 — Output the documented report (in chat AND save to file)

This is a documentation deliverable. Two outputs required:

**5a. In-chat output** — the full report rendered in the conversation, using the standard format below. Don't truncate.

**5b. Saved file** — write the same report to a file using the Write tool. Filename:
```
slop-check-{ui|ux|full}-report-{YYYYMMDD}-{HHMMSS}.md
```
Save at:
- Project root if a codebase path is in scope (so the report sits next to the code it audits)
- Otherwise current working directory
- Or wherever the user has a docs/audits folder if one exists

After saving, tell the user the file path so they can open it. If the user asked for a specific location, save there.

The file should contain ALL the same content as the chat output — heatmap, per-page lists, systemic findings, high-confidence section, summary. No truncation in either.

## Sub-agent prompt template — Visual track

```
You are reviewing a {platform} {domain} UI mockup against the **{category}** canonical rules
from the **visual perspective**. You see the rendered output, not the code.

**Mockup**:
- Image path: {image_path}  (use Read tool to view)
- Description (fallback): {description}

**Reference file**: {reference_path}

**MANDATORY first step**: Read the reference file in FULL via the Read tool.
Do NOT proceed with analysis based on category name alone or your prior
knowledge. The reference is the ONLY source of truth — your review is
invalid without reading it. If the reference file fails to load, stop
and report the error rather than guessing rules.

**Pages to review**: {pages list — e.g., "/home", "/login", "/profile"}

**Your task** (in order, no skipping):

### Phase A — Build the per-page checklist matrix progressively

1. Read the FULL reference file via Read tool.
2. Extract the list of rule IDs from the reference (e.g., `COMP-BTN-001`, `COMP-BTN-002`, ...).
3. Initialize the matrix with all cells as `?` (unreviewed). All rule rows × all page columns.
4. **Output the empty matrix first** so the structure is locked in.
5. **Then iterate page-by-page.** After EACH page is reviewed:
   - Mark every cell in that page's column with one of:
     - `✓` = rule satisfied
     - `✗` = clear violation
     - `⚠` = borderline (when in doubt, prefer `⚠` over `✓`)
     - `—` = N/A (rule doesn't apply to this page)
     - `?` = can't tell from mockup, needs code track
   - **Output the updated matrix immediately** after that page (don't wait until all pages are done).
   - Briefly note (1-2 sentences) the most striking finding from this page.
6. Continue page-by-page until every column is filled.

This progressive update matters: by page 3 of 5, patterns are already visible (e.g., "rule X fails on every page so far → likely systemic"), letting the rest of the review be more targeted. Don't batch all output at the end.

Final matrix format:

```markdown
## Checklist matrix — {category}

| Rule ID | /home | /login | /profile | /checkout |
|---------|-------|--------|----------|-----------|
| COMP-BTN-001 | ✓ | ✗ | ⚠ | ✓ |
| COMP-BTN-002 | ✗ | ✗ | ✗ | ✗ |  ← systemic
| COMP-BTN-003 | ✓ | ✓ | ✓ | ✓ |
| ... | ... | ... | ... | ... |
```

### Phase B — Identify patterns from matrix

After matrix complete:
- **Systemic** = rule fails (`✗`) on ≥50% of pages → high priority, system-level issue
- **Borderline systemic** = rule borderline (`⚠`) on ≥50% → likely needs investigation
- **Page-specific** = rule fails on only 1-2 pages → localized fix
- **Walk completeness** = no empty cells. Every rule × every page = explicit mark

### Phase C — Output ALL findings (no truncation)

After the matrix, write detail blocks for **every single** `✗` and `⚠` cell. Do NOT cap, summarize, or omit. The user explicitly wants the full list per page so they can fix everything. Even if there are 30+ findings on one page, list all 30.

```
[RULE-ID] Rule title  (or [HEURISTIC] short label for non-rule findings)
Affected pages: /home, /profile  (or "all pages" if systemic)
Pattern: systemic | page-specific | borderline
Severity: high | medium | low
Observation: what specifically you see — per page if observation differs
Why it's a problem: connect detail to rule principle in one sentence
Suggested fix: concrete action (system-level if systemic, per-page if local)
Confidence: high | medium | low
```

**Catch all ambiguous cases.** When in doubt → mark `⚠` and write a finding block.

**Beyond rules: flag awkward / weird / off things.** After the matrix, sweep each page for anything that looks off in this category without a matching rule (awkward button placement, off-tone icon, broken rhythm). Tag `[HEURISTIC]`. Add to a separate matrix:

```markdown
## Heuristic matrix — {category}

| Heuristic label | /home | /login | /profile | /checkout |
|-----------------|-------|--------|----------|-----------|
| Awkward CTA placement | — | ✗ | — | — |
| ... | ... | ... | ... | ... |
```

If a rule requires code-level evidence you can't see in the mockup (exact px, token consistency across files), mark cell `?` — the code sub-agent will resolve.

### Phase D — Consolidated handoff to main agent

After all page-by-page output, write a **final consolidated section** for the main agent to merge cleanly. This is the structured handoff. **Be specific** — "high severity" alone says nothing. Each finding must answer: where exactly is it, what specifically is wrong, why does it hurt the user, why this severity level.

```markdown
## FINAL HANDOFF — {category} (visual track)

### Per-page totals
- /home: {H high}, {M medium}, {L low}, {N heuristic}
- /login: ...
- ...

### All findings, indexed for merge

For each page, one block per finding:

```
PAGE: /home
ID: COMP-BTN-002
TYPE: rule | heuristic
TITLE: Button hierarchy missing
LOCATION: Header bar, top-right (Save / Cancel / Delete cluster, ~64px from top edge)
OBSERVATION: Save, Cancel, and Delete buttons all rendered identically — filled black background, h-10, same font weight. No visual distinction between primary action (Save) and destructive action (Delete).
USER IMPACT: User cannot tell which action is intended primary. Save and Delete are visually equivalent → high risk of accidental Delete click. Eye-tracking equivalent: nothing draws focus first.
WHY (rule): Buttons must have clear Primary/Secondary/Tertiary tiers. Without hierarchy, every action is emphasized equally → noise + decision paralysis.
SEVERITY: high
SEVERITY REASON: Affects every user on every visit. Risk of destructive action confusion. Foundational hierarchy missing — fix unblocks downstream rules.
CONFIDENCE: high
FIX:
  - Save → variant="primary" (filled, brand color, weight 600)
  - Cancel → variant="secondary" (outlined, neutral)
  - Delete → variant="tertiary" or text-only with red accent, smallest weight
SYSTEMIC: yes | no  (true if this rule fails on ≥50% of pages)
```

**Required fields explained**:
- `LOCATION` — be precise. Not just "the button" but "Save button at top-right of header card". For multi-instance: "all buttons in the action toolbar".
- `OBSERVATION` — specific concrete description, not "looks bad". Cite colors, sizes, positions you can see.
- `USER IMPACT` — what experience degrades. The reason this matters for the actual user, not the rule.
- `SEVERITY REASON` — why high vs medium vs low. Frequency of exposure × consequence severity × reversibility.
- `FIX` — actionable. If multiple options exist, list them. Don't say "improve hierarchy" — say "Save → filled-primary; Cancel → outlined".

### Pattern summary
- Systemic patterns observed (rules failing on ≥50% pages): list rule IDs
- Cross-page sprawl noted: list any patterns
- Heuristic recurring themes: list any cross-page heuristic patterns
```

**Return format** (full sub-agent output, in order):
1. The empty checklist matrix (initial state)
2. Updated matrix after each page (one update per page)
3. Final full matrix
4. Heuristic matrix (rows with at least one ✗ or ⚠)
5. **Phase D — FINAL HANDOFF section** (the consolidated, merge-ready output)

At the end, append:
- "Rules walked: {N rules} × {M pages} = {N×M} cells filled"
- "Pages reviewed: {list}"
- "Total findings: {rule findings} rule + {heuristic findings} heuristic = {total}"
```

## Sub-agent prompt template — Code-lens track

```
You are reviewing a {platform} {domain} UI codebase against the **{category}** canonical rules
from the **code perspective**. You see the source files, not the rendered output.

**Codebase**:
- Root path: {codebase_path}
- Stack: {detected stack — e.g., Next.js + Tailwind, Vue + CSS modules}

**Reference file**: {reference_path}

**MANDATORY first step**: Read the reference file in FULL via the Read tool.
The reference is the ONLY source of rule truth.

**Pages to review**: {pages list — e.g., page files src/pages/home.tsx, src/pages/login.tsx, ...}
   Or detect pages from routes if not provided.

**Your task** (in order):

### Phase A — Build the per-page checklist matrix progressively

1. Read the FULL reference file via Read tool.
2. Extract the list of rule IDs.
3. Enumerate the pages (page files / route handlers).
4. Initialize matrix with all cells `?`. **Output empty matrix first** to lock structure.
5. **Iterate page-by-page.** After EACH page:
   - Mark every cell in that page's column with `✓`/`✗`/`⚠`/`—`/`?` (definitions below)
   - **Output the updated matrix immediately** (don't batch until end)
   - Briefly note 1-2 most striking code-level findings from this page
6. Continue until all columns filled.

Cell legend:
- `✓` = rule satisfied in this page's code
- `✗` = clear violation in this page's code
- `⚠` = borderline (could be intentional, could be sprawl)
- `—` = N/A (rule doesn't apply to this page type)
- `?` = needs runtime / visual confirmation

Output matrix format:

```markdown
## Code checklist matrix — {category}

| Rule ID | home.tsx | login.tsx | profile.tsx | checkout.tsx |
|---------|----------|-----------|-------------|--------------|
| COMP-BTN-001 | ✓ | ✗ | ⚠ | ✓ |
| COMP-BTN-002 | ✗ | ✗ | ✗ | ✗ |  ← systemic in code
| ... | ... | ... | ... | ... |
```

### Phase B — Run grep / scan
For applicable rules, run targeted Bash/Grep commands to gather evidence
across the WHOLE codebase (cross-page sprawl is a key signal).

5. Examples of code-level evidence per category:

   - **Component**: grep for similar JSX patterns repeated across files
     (button-with-icon, card-with-header, etc.) → duplication candidates
     Find inline-styled vs componentized versions of same UI
   - **Layout**: grep for container patterns, grid/flex usage,
     max-width values, breakpoint patterns
   - **Typography**: grep for font-size/font-weight values
     (CSS, Tailwind classes, inline) → count distinct values
   - **Color**: grep for color values (hex, rgb, hsl, Tailwind classes,
     CSS vars) → count distinct, find near-duplicates
   - **Hierarchy**: grep for <h1>, <h2>, <h3> per page file
     → flag pages without h1, multiple h1s, h3 before h2, etc.
   - **Spacing**: grep for padding, margin, gap values → count distinct,
     find sprawl (e.g., 14 different padding values)
   - **Image**: grep for <img>, <Image>, src patterns → find missing alt,
     non-optimized formats, hardcoded sizes

6. Do NOT skip rules. For rules that genuinely can't be detected from code
   (e.g., "image visually fits brand"), mark cells `?` and say so.

### Phase C — Pattern detection from matrix

After matrix complete:
- **Systemic** = rule fails on ≥50% of pages → token sprawl, missing system
- **Page-specific** = rule fails on 1-2 pages → localized fix
- **Cross-page sprawl** = inventory shows N variants where 2-3 expected

### Phase D — Output findings

Detail block for every `✗` and `⚠` cell + grep findings:

```
[RULE-ID] Rule title
  (or [PATTERN] for structural pattern matching a rule's spirit)
  (or [ANOMALY] for code smells beyond rules)
Affected pages: page1.tsx, page2.tsx  (or "all pages" if systemic)
Pattern: systemic | page-specific | cross-page-sprawl
Severity: high | medium | low
Evidence: hard counts and file:line citations
  e.g., "9 distinct border-radius values across 47 files"
       "src/pages/Home.tsx:42, src/components/Card.tsx:18 (inline styles)"
Why it's a problem: connect code finding to rule principle (or general
  consistency principle for [ANOMALY]) in one sentence
Suggested fix: concrete action (e.g., "consolidate to 4 token values:
4/8/12/16px in tailwind.config.js")
Confidence: high | medium | low
```

**Catch all ambiguous cases.** When grep shows borderline patterns
("8 distinct font sizes — could be intentional scale, could be sprawl"),
mark cells `⚠` and write a finding rather than dismissing.

**Beyond rules: flag awkward / weird patterns.** After the matrix, sweep
for code smells in this category even without a matching canonical rule
(3 different ways of declaring the same button, one component file with
5x more lines than its siblings, a single page with deeply nested ternaries
that suggests structural drift). Tag these `[PATTERN]` or `[ANOMALY]` and
add to a separate matrix:

```markdown
## Anomaly matrix — {category}

| Anomaly label | home.tsx | login.tsx | profile.tsx | checkout.tsx |
|---------------|----------|-----------|-------------|--------------|
| Inline style overload | ✗(23) | — | — | ✗(15) |
| Deep ternary nesting | — | — | ✗ | — |
| ... | ... | ... | ... | ... |
```

### Phase E — Consolidated handoff to main agent

After all page-by-page output, write a **final consolidated section** for the main agent. Be specific — generic severity without concrete reason is useless. Each finding must include exact location (file:line), what's specifically wrong, what user/dev impact, and why this severity.

```markdown
## FINAL HANDOFF — {category} (code-lens track)

### Per-page totals
- src/pages/home.tsx: {H high}, {M medium}, {L low}, {N anomaly}
- src/pages/login.tsx: ...

### All findings, indexed for merge (one block per finding)

PAGE: src/pages/home.tsx
ID: COMP-BTN-002 | PATTERN-... | ANOMALY-...
TYPE: rule | pattern | anomaly
TITLE: Button hierarchy missing
LOCATION: src/pages/home.tsx:142-156 (action toolbar component)
OBSERVATION: Three buttons rendered with className="bg-black text-white h-10 px-4". No props or className differences distinguishing role. No <Button variant=...> pattern in use.
EVIDENCE: 
  - src/pages/home.tsx:142 (Save button)
  - src/pages/home.tsx:148 (Cancel button)
  - src/pages/home.tsx:154 (Delete button)
  - grep "bg-black text-white h-10" returns 47 matches across 12 files
USER IMPACT: Users can't visually distinguish Save vs Delete. With Delete adjacent to Save and identically styled, accidental destructive clicks are likely.
DEV IMPACT: No shared Button component → every new button copies these classes → divergence guaranteed at next style update.
WHY (rule): Buttons must have Primary/Secondary/Tertiary tiers (COMP-BTN-002). Without a shared component, hierarchy becomes a per-page accident.
SEVERITY: high
SEVERITY REASON: Affects every page (47 occurrences across 12 files), destructive-action confusion possible, blocks design-system adoption.
CONFIDENCE: high
FIX:
  - Define <Button variant="primary|secondary|tertiary"> in src/components/Button.tsx
  - Replace all "bg-black text-white h-10" usages with the variant prop
  - Estimated touchpoints: 47 lines across 12 files
SYSTEMIC: yes
SPRAWL: yes  (47 inline duplicate styles across the codebase)
```

**Required fields**:
- `LOCATION` — precise file:line range, not just file
- `OBSERVATION` — specific code/structure observed (className, prop, structure)
- `EVIDENCE` — multiple file:line citations + grep counts where relevant
- `USER IMPACT` — what user experience suffers
- `DEV IMPACT` — what maintenance pain this causes
- `SEVERITY REASON` — concrete (frequency × consequence × reversibility), not generic
- `FIX` — actionable steps with concrete touchpoint count

### Pattern summary
- Systemic patterns: ...
- Cross-page sprawl: e.g., "9 distinct border-radius values across 47 files"
- Anomaly recurring themes: ...
```

**Return format** (full sub-agent output, in order):
1. Empty matrix
2. Updated matrix after each page (one update per page)
3. Final full matrix
4. Anomaly matrix (rows with at least one mark)
5. **Phase E — FINAL HANDOFF section** (consolidated, merge-ready)

At the end, append:
- "Rules walked: {N rules} × {M pages} = {N×M} cells filled"
- "Pages reviewed: {list}"
- "Code patterns audited: {grep patterns you ran}"
- "Total findings: {rule} rule + {pattern} pattern + {anomaly} anomaly = {total}"
```

## Aggregation logic

**This is a documentation deliverable, not a quick summary.** The user wants the full picture so they can fix every issue. Length is fine — quantity matters.

**No pre-filtering, no truncation.** Don't drop or cap findings based on your own judgment about importance. Keep `[HEURISTIC]` and `[ANOMALY]` findings — they often catch the issues no rule covers yet. If a page has 30 findings, list all 30. The output may be long; that's the point.

**Read every sub-agent's `FINAL HANDOFF` section.** That's the structured merge-ready data. Do NOT skip ahead to severity blocks alone — the FINAL HANDOFF has the per-page index you need.

**Primary aggregation goal: per-page fix lists.** For each page reviewed, collect every `✗` and `⚠` finding (visual + code) that landed on that page. Merge visual and code observations into a single fix entry per rule per page (don't list visual COMP-BTN-001 and code COMP-BTN-001 separately for the same page — combine them). Sort by severity within each page.

**Build the cross-page heatmap** as overview. Count `✗` and `⚠` cells from each sub-agent's matrix, grouped by page × category.

**Flag systemic findings** = any rule failing on ≥50% of pages across any sub-agent. These appear in a follow-up section, not replacing per-page lists — the user still needs the per-page lists to fix specific pages, AND the systemic note to know they could fix many at once via design system update.

**Output as a documented report** — this is meant to be saved, shared, referenced later. Structure it like a real audit report, not a chat reply. Include section anchors, clear headings, tables where helpful.

When the same issue is flagged within a track:
- Prefer the more specific category. Example: button too small flagged by both Component and Spacing → keep Component (`COMP-BTN-001`).
- If genuinely orthogonal, keep both.

When sub-agents disagree on severity:
- Take the higher one.

When **visual and code both flag the same area** (e.g., visual: "inconsistent button rounding"; code: "9 border-radius values"):
- Mark as **high-confidence** in output. This is the strongest signal — both perspectives agree.

**Verify reference walk completion.** Each sub-agent appends `Rules walked: N/total`. If any count is significantly under or missing, re-dispatch that sub-agent.

## Output format

The primary deliverable is **per-page fix lists**. Each page reviewed gets its own actionable list of issues to fix on that page. Systemic findings are a follow-up section showing where a single system-level fix replaces multiple per-page fixes.

```
## Slop Check (UI) Result

**Platform**: {Mobile | PC} · **Domain**: {detected domain}
**Pages reviewed**: {list of pages with labels}
**Inputs**: Mockup {✓|✗} / Codebase {✓|✗} / Live URL {✓|✗}
**Sub-agents dispatched**: {N visual} visual + {N code} code = {total}
**Findings**: {H} high / {M} medium / {L} low ({S} systemic, {C} high-confidence)

---

### Cross-page heatmap (overview)

| Category | /home | /login | /profile | /checkout |
|----------|-------|--------|----------|-----------|
| Component | 2 ✗ / 1 ⚠ | 5 ✗ / 0 ⚠ | 1 ✗ / 3 ⚠ | 0 ✗ / 2 ⚠ |
| Color | 1 ✗ | 3 ✗ | 0 ✗ | 1 ✗ |
| Typography | 0 ✗ | 4 ✗ | 2 ✗ | 0 ✗ |
| (etc) | ... | ... | ... | ... |
| **Total** | **3 ✗** | **12 ✗** | **3 ✗** | **2 ✗** |

→ Hot spots immediately visible.

---

## Per-page fix lists

### /home — {H} high, {M} medium, {L} low

#### High severity
1. **[RULE-ID] Rule title** — *Category*
   - **Location**: where on page / file:line
   - **What's wrong**: specific concrete observation (visual + code merged for this page)
   - **User impact**: what experience suffers
   - **Why high severity**: frequency × consequence × reversibility (concrete reason)
   - **Why (rule)**: cited canonical principle
   - **Fix**: actionable concrete steps (e.g., "Save → variant=primary; Cancel → variant=secondary; touchpoints: src/pages/home.tsx:142,148")
   - **Confidence**: H/M/L
   - **System-level note**: if systemic across pages, "→ also see Systemic [RULE-ID]"

2. **[RULE-ID] ...**

#### Medium severity
[same numbered list format]

#### Low severity
[same format]

#### Heuristic / anomaly findings on /home
- **[HEURISTIC] label**: ... · Fix: ...

---

### /login — {H} high, {M} medium, {L} low
[same per-page structure]

---

### /profile — ...
[same]

---

### /checkout — ...
[same]

---

## Systemic findings (apply once, fix many pages)

These rules fail on ≥50% of pages — a single system-level fix replaces all the per-page fixes above.

**[RULE-ID] Rule title** — *Category*
- **Affected pages**: /home, /login, /profile, /checkout (4/4)
- **System-level fix**: e.g., "Define `<Button variant>` in design system; replace ad-hoc styles in 4 pages"
- **Per-page fix items this replaces**: links/refs to the per-page entries above

---

## High-confidence findings (visual + code both agree)

These are flagged by both visual and code-lens sub-agents independently — strongest signal.

**[RULE-ID] Rule title** — *Category, affected pages*
- **Visual evidence**: ...
- **Code evidence**: hard counts, file:line
- **Fix**: ...

---

## Summary

{2-3 sentences}:
- Hottest page → top recommendation for that page
- Highest-impact systemic fix → estimated reduction in per-page items
- Top 3 actions in priority order
```

## Sister skill: slop-check-ux

For comprehensive design review (UI + UX), also dispatch `slop-check-ux` in the same turn. Triggers like "full slop check", "complete design audit", "design slop 전부", "UI + UX 검사" mean the user wants both skills running.

When both run together, you orchestrate **up to 22 sub-agents total** (14 UI + 8 UX) in parallel — assuming both visual and code inputs are available for both tracks.

Save a single combined file: `slop-check-full-report-{YYYYMMDD}-{HHMMSS}.md` (not two separate files). One unified document with both tracks.

Output groups findings by track:

```
## Slop Check Result (UI + UX)

### UI track
[high-confidence / visual / code blocks per slop-check-ui]

### UX track
[high-confidence / visual / code blocks per slop-check-ux]
```

## Tone

- Direct, practical, prioritize stripping away over decoration
- Concrete rule violation identification + improvement, not vague praise
- All claims must cite a canonical rule by `[ID]` (or `[PATTERN]` for code-only structural issues)
- Evidence over assertion — "I see X in the mockup" or "grep shows N occurrences" — never "this looks bad"
