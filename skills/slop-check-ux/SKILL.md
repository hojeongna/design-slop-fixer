---
name: slop-check-ux
description: Rule-based UX validator that cites specific RULE-IDs from a 388-rule canonical library covering Concept, Information Architecture, Interaction, Copy. Dispatches independent visual and code-lens sub-agents per category in parallel, then aggregates both perspectives. Use when the user explicitly wants traceable rule violations on UX flows or codebase — e.g. "slop check this UX", "cite UX violations", "audit user flow against rules", "find UX consistency issues with rule IDs". Skip for vague "is this confusing" or general usability vibes without explicit rule-citation intent.
---

# Slop Check (UX)

## Purpose

Rule-based UX validator. Returns specific `[RULE-ID]` citations for every issue found, grounded in either visual evidence (mockup/screenshot) or code evidence (file:line, hard counts) — no hand-waving.

Backed by **388 canonical rules** across 4 categories.

## When to use

Trigger ONLY when the user explicitly wants **rule-based citation** of UX issues:
- "Slop check this UX"
- "Audit this flow against UX rules"
- "Find specific UX violations with rule IDs"
- "Cite IA / interaction issues by rule"
- "Validate this navigation against canonical rules"

## When NOT to use

Skip this skill for:
- "Is this confusing?" → vibes-based usability review without rule-citation intent
- "Give me UX feedback" → general critique without explicit rule-validation
- "Make this easier to use" → open-ended UX brainstorming
- General persona/journey discussions without an explicit rule-validation intent

## Architecture: two independent perspectives

This skill runs **two parallel review tracks per category** that do NOT influence each other:

1. **Visual track** — sub-agents read the mockup/flow screenshot and walk every canonical rule visually.
2. **Code track** — sub-agents grep/analyze the codebase against the same canonical rules from a code-evidence angle.

Each track is independent. Aggregation happens AFTER both finish, so cross-reference (where both agree) signals high-confidence issues.

For each category, that means **2 sub-agents** (1 visual + 1 code). Across 4 UX categories, a full check dispatches **8 sub-agents** in parallel.

If only one input is available (mockup only OR codebase only), only that track runs — but both should be present for full coverage.

## Procedure

### Step 1 — Input handshake (MANDATORY)

Before dispatching anything, confirm with the user what's available:

```
What inputs do you have for this UX slop check?
  [a] Mockup screenshot(s) only       → visual track only (4 sub-agents)
  [b] Codebase path only              → code track only (4 sub-agents)
  [c] Both mockup(s) + codebase       → full review (8 sub-agents)  ← recommended
  [d] Live URL (Playwright/MCP)       → live screenshot + DOM/route inspection

How many pages/flows are you submitting?
  - Multiple mockups (one per screen)?
  - Codebase contains multiple routes/flows?
  - Live URL with multiple paths to navigate?
  Multi-page reviews surface systemic UX issues — same issue across many
  screens = system-level slop.

Want to focus on specific categories? (e.g. "Information Architecture only")
Or extend default scope? Default scope already covers:
  - Information hierarchy across pages
  - Navigation/menu/tab structure consistency
  - Missing information (stock count, chat metadata, payment summary, etc.)
  - Concept consistency across screens
  - Interaction feedback (states, errors, loading, toast)
  - Modal/popup correctness
  - Affordance / hover / clickable signals
  - Copy clarity (labels, error messages, button text)
  - + standard rule walk per category
```

Do NOT proceed without input confirmation. **Always enumerate pages explicitly.**

### Step 2 — Identify platform & domain

- Mobile / PC / Web / Dashboard
- Domain: e-commerce, portfolio, dashboard, AI chat, fintech, travel, social, etc.
- Briefly describe the flow in 3-5 sentences (gets passed to every sub-agent as fallback context).

### Step 3 — Dispatch sub-agents in parallel

Use the `Task` / `Agent` tool to launch all relevant sub-agents in a single message.

| # | Category | Visual sub-agent | Code-lens sub-agent | Rule count |
|---|----------|------------------|---------------------|-----------|
| 1 | Concept | mockup → CONCEPT rules | grep design-language patterns, repeated structural decisions | 100 |
| 2 | Information Architecture | mockup → INFO rules | grep page route structure, nav/menu definitions, sitemap | 150 |
| 3 | Interaction | mockup → INTER rules | grep onClick handlers, modal/toast/error/loading components, state mgmt | 122 |
| 4 | Copy | mockup → COPY rules | grep all UI strings, error messages, button labels, placeholder text | 16 |

Reference paths:
- `skills/slop-check-ux/reference/concept.md`
- `skills/slop-check-ux/reference/information_architecture.md`
- `skills/slop-check-ux/reference/interaction.md`
- `skills/slop-check-ux/reference/copy.md`

### Step 4 — Collect, verify, aggregate

After all sub-agents return:
1. **Verify completion** — each sub-agent appends `Rules walked: N/total`. If under-counted or missing, re-dispatch.
2. **No pre-filtering, no cap** — keep every finding. The user wants the full picture.
3. **Dedup within track** — same rule cited twice within visual or code → keep one.
4. **Cross-reference** — when visual and code both flag the same area, mark as **high-confidence**.
5. **Severity sort** — High → Medium → Low, within each track.
6. **Merge per page** — visual and code findings on the same rule for the same page combine into one fix entry.

### Step 5 — Output the documented report (in chat AND save to file)

This is a documentation deliverable. Two outputs required:

**5a. In-chat output** — the full report in the conversation, using the standard format below. Don't truncate.

**5b. Saved file** — write the same report to a file using the Write tool. Filename:
```
slop-check-{ui|ux|full}-report-{YYYYMMDD}-{HHMMSS}.md
```
Save at:
- Project root if a codebase path is in scope
- Otherwise current working directory
- Or wherever the user has a docs/audits folder if one exists

After saving, tell the user the file path so they can open it.

The file should contain ALL the same content as the chat output. No truncation in either.

## Sub-agent prompt template — Visual track

```
You are reviewing a {platform} {domain} UX flow against the **{category}** canonical rules
from the **visual perspective**. You see the rendered output, not the code.

**Mockup**:
- Image path: {image_path}  (use Read tool to view)
- Description (fallback): {description}

**Reference file**: {reference_path}

**MANDATORY first step**: Read the reference file in FULL via the Read tool.
The reference is the ONLY source of truth. Your review is invalid without
reading it.

**Pages to review**: {pages list — e.g., "/login", "/onboarding/step1", "/onboarding/step2", "/home"}

**Your task** (in order, no skipping):

### Phase A — Build the per-page checklist matrix progressively

1. Read the FULL reference file via Read tool.
2. Extract the list of rule IDs.
3. Initialize matrix: all cells `?`. **Output empty matrix first** to lock structure.
4. **Iterate page-by-page.** After EACH page:
   - Read that page's mockup via Read tool
   - Walk EVERY rule and mark the cell with `✓`/`✗`/`⚠`/`—`/`?` (definitions below)
   - **Output the updated matrix immediately** after that page
   - Briefly note 1-2 most striking findings from this page
5. Continue until all columns filled.

Don't batch all output at the end. Progressive updates let patterns surface earlier — by page 3 of 5, you may already see "rule X fails everywhere → systemic".

Cell legend:
- `✓` = rule satisfied
- `✗` = clear violation
- `⚠` = borderline (when in doubt, prefer `⚠` over `✓`)
- `—` = N/A
- `?` = needs code track confirmation

Output matrix format:

```markdown
## Checklist matrix — {category}

| Rule ID | /login | /onboard1 | /onboard2 | /home |
|---------|--------|-----------|-----------|-------|
| INFO-PRIO-001 | ✓ | ✗ | ⚠ | ✓ |
| INFO-NAV-001 | ✗ | ✗ | ✗ | ✗ |  ← systemic
| ... | ... | ... | ... | ... |
```

### Phase B — Identify patterns

- **Systemic** = rule fails ≥50% pages → system-level UX issue
- **Page-specific** = 1-2 pages → localized
- **Borderline systemic** = ⚠ on majority → likely sprawl

### Phase C — Output findings

Detail block per `✗` and `⚠` cell:

```
[RULE-ID] Rule title  (or [HEURISTIC] short label for non-rule findings)
Affected pages: /login, /home  (or "all pages" if systemic)
Pattern: systemic | page-specific | borderline
Severity: high | medium | low
Observation: what specifically you see — per page if observation differs
Why it's a problem: connect to rule principle (or general UX intuition)
Suggested fix: concrete action
Confidence: high | medium | low
```

**Catch all ambiguous cases.** When in doubt → mark `⚠` and write finding.

**Beyond rules: flag awkward / unclear / off UX patterns.** After the
matrix, sweep each page for anything that looks usability-wise weird
without a matching rule (confirmation dialog with no clear primary action,
flow needing too many taps to reach goal, label tonally off). Tag
`[HEURISTIC]` and add to a separate matrix:

```markdown
## Heuristic matrix — {category}

| Heuristic label | /login | /onboard1 | /onboard2 | /home |
|-----------------|--------|-----------|-----------|-------|
| Confusing primary action | — | ✗ | ✗ | — |
| ... | ... | ... | ... | ... |
```

If a rule requires code-level evidence (navigation routes, hierarchy across all pages, data flow), mark `?` — code track will resolve.

### Phase D — Consolidated handoff to main agent

After all page-by-page output, write a **final consolidated section** for the main agent. Each finding must specify exactly where the issue is, what specifically is wrong, what user impact occurs, and why this severity level.

```markdown
## FINAL HANDOFF — {category} (visual track)

### Per-page totals
- /login: {H high}, {M medium}, {L low}, {N heuristic}
- /onboard1: ...

### All findings, indexed for merge (one block per finding)

PAGE: /login
ID: INFO-NAV-001 | HEURISTIC-...
TYPE: rule | heuristic
TITLE: Hamburger menu on login screen
LOCATION: Top-left of header bar, ~16px from screen edge
OBSERVATION: A hamburger menu icon appears on the login page even though there's no global navigation needed pre-authentication. No back button, no relevant routes accessible.
USER IMPACT: User taps hamburger expecting menu, sees nothing useful (or worse, sees authenticated routes that fail). Confusing dead-end interaction.
WHY (rule): Drawer menu must match context (INFO-NAV-001). Login is pre-auth — drawer has nothing meaningful to surface.
SEVERITY: high
SEVERITY REASON: Hits 100% of users (every login). First impression is confusion. Cheap to fix (just remove the icon).
CONFIDENCE: high
FIX: Remove hamburger menu from /login. If a back-navigation is needed, use a left-arrow back icon instead.
SYSTEMIC: no  (login-specific)
```

**Required fields**:
- `LOCATION` — precise visual region or flow position
- `OBSERVATION` — concrete description of what's visible
- `USER IMPACT` — actual user pain
- `SEVERITY REASON` — frequency × consequence × reversibility, concretely
- `FIX` — actionable steps

### Pattern summary
- Systemic patterns: ...
- Heuristic recurring themes: ...
```

**Return format** (full sub-agent output, in order):
1. Empty matrix
2. Updated matrix after each page
3. Final full matrix
4. Heuristic matrix (rows with at least one mark)
5. **Phase D — FINAL HANDOFF section**

At the end, append:
- "Rules walked: {N rules} × {M pages} = {N×M} cells filled"
- "Pages reviewed: {list}"
- "Total findings: {rule} rule + {heuristic} heuristic = {total}"
```

## Sub-agent prompt template — Code-lens track

```
You are reviewing a {platform} {domain} UX codebase against the **{category}** canonical rules
from the **code perspective**.

**Codebase**:
- Root path: {codebase_path}
- Stack: {detected stack}

**Reference file**: {reference_path}

**MANDATORY first step**: Read the reference file in FULL via the Read tool.

**Pages to review**: {pages list — e.g., src/pages/login.tsx, src/pages/onboarding/, ...}
   Or detect from routes if not provided.

**Your task** (in order):

### Phase A — Build per-page checklist matrix progressively

1. Read the FULL reference file via Read tool.
2. Extract the list of rule IDs.
3. Enumerate the pages (page files / route handlers).
4. Initialize matrix: all cells `?`. **Output empty matrix first** to lock structure.
5. **Iterate page-by-page.** After EACH page:
   - Walk EVERY applicable rule, mark the cell `✓`/`✗`/`⚠`/`—`/`?`
   - **Output the updated matrix immediately**
   - Briefly note 1-2 striking findings from this page
6. Continue until all columns filled.

Cell legend:
- `✓` = satisfied
- `✗` = clear violation
- `⚠` = borderline
- `—` = N/A
- `?` = needs visual confirmation

Output matrix format:

```markdown
## Code checklist matrix — {category}

| Rule ID | login.tsx | onboard1.tsx | onboard2.tsx | home.tsx |
|---------|-----------|--------------|--------------|----------|
| INFO-PRIO-001 | ✓ | ✗ | ⚠ | ✓ |
| INTER-FEED-001 | ✗ | ✗ | ✗ | ✗ |  ← systemic
| ... | ... | ... | ... | ... |
```

### Phase B — Run grep / scan

5. For applicable rules, run targeted Bash/Grep across the WHOLE codebase
   (cross-page sprawl is a key signal). Examples per category:

   - **Concept**: grep design-language consistency
     (e.g., are some pages flat-styled while others use shadows?)
     grep for repeated structural decisions vs one-offs
   - **Information Architecture**:
     · List all routes/pages → check hierarchy depth
     · Find navigation/menu definition files → check consistency
     · grep for h1/h2 hierarchy across pages
     · Find sitemap entries vs actual routes
     · Detect tab definitions, drawer menus, GNB components
   - **Interaction**:
     · grep for onClick/onSubmit handlers → look for missing feedback
     · Find modal/dialog/toast/error/loading components → check completeness
     · Find form fields without validation states
     · Detect buttons without loading/disabled states
     · Find affordance issues (e.g., divs as buttons)
   - **Copy**:
     · grep all UI strings (labels, button text, placeholders, errors)
     · Check vague labels ("Submit", "OK"), missing actionable hints
     · Find error messages without recovery action
     · Detect inconsistent capitalization, terminology drift

6. Do NOT skip rules. For rules that can't be detected from code, mark `?`.

### Phase C — Pattern detection

- **Systemic** = rule fails ≥50% pages
- **Page-specific** = 1-2 pages
- **Cross-page sprawl** = inventory shows N variants where 2-3 expected

### Phase D — Output findings

Detail block for every `✗` and `⚠` + grep findings:

```
[RULE-ID] Rule title
  (or [PATTERN] / [ANOMALY])
Affected pages: page1.tsx, page2.tsx  (or "all pages" if systemic)
Pattern: systemic | page-specific | cross-page-sprawl
Severity: high | medium | low
Evidence: hard counts and file:line citations
Why it's a problem: connect to rule principle (or general UX consistency)
Suggested fix: concrete action
Confidence: high | medium | low
```

**Catch all ambiguous cases.** When grep shows borderline patterns
("3 different error message tones across the codebase"), mark `⚠` and
write finding.

**Beyond rules: flag awkward / weird patterns.** After matrix, sweep for
UX code smells (toast called from 5 components but no shared ToastProvider,
error handling missing recovery action in 8 places, route hierarchy
/a/b/c/d nesting too deep). Tag `[PATTERN]` or `[ANOMALY]`. Add to
anomaly matrix:

```markdown
## Anomaly matrix — {category}

| Anomaly label | login.tsx | onboard1.tsx | onboard2.tsx | home.tsx |
|---------------|-----------|--------------|--------------|----------|
| Missing error recovery | ✗ | — | ✗ | ✗ |
| ... | ... | ... | ... | ... |
```

### Phase E — Consolidated handoff to main agent

After all page-by-page output, write a **final consolidated section**. Be specific — generic "high severity" without concrete reason and location is useless.

```markdown
## FINAL HANDOFF — {category} (code-lens track)

### Per-page totals
- src/pages/login.tsx: {H high}, {M medium}, {L low}, {N anomaly}
- src/pages/onboard1.tsx: ...

### All findings, indexed for merge (one block per finding)

PAGE: src/pages/login.tsx
ID: INFO-NAV-001 | PATTERN-... | ANOMALY-...
TYPE: rule | pattern | anomaly
TITLE: Hamburger menu component imported on login route
LOCATION: src/pages/login.tsx:14 (import), :47 (render)
OBSERVATION: <HamburgerMenu /> rendered in login layout. The component imports authenticated route definitions from src/routes/authenticated.ts:1-45 — login users have no access to any of these.
EVIDENCE:
  - src/pages/login.tsx:14 — import HamburgerMenu
  - src/pages/login.tsx:47 — <HamburgerMenu /> in JSX
  - src/components/HamburgerMenu.tsx:23 — guards routes with useAuth(), but login user has no auth → menu is empty
USER IMPACT: User taps hamburger, sees an empty (or auth-required) menu. Dead-end interaction.
DEV IMPACT: Adds unused dependency on authenticated routes from a pre-auth screen.
WHY (rule): Drawer must match context (INFO-NAV-001).
SEVERITY: high
SEVERITY REASON: 100% of login flows hit this. Confusing first impression. 1-line fix.
CONFIDENCE: high
FIX:
  - Remove import line 14
  - Remove <HamburgerMenu /> from line 47
  - Or replace with a context-appropriate left-arrow back button
SYSTEMIC: no
SPRAWL: no
```

**Required fields**:
- `LOCATION` — file:line precision
- `OBSERVATION` — concrete code/structure detail
- `EVIDENCE` — multiple file:line refs
- `USER IMPACT` + `DEV IMPACT` — real consequences
- `SEVERITY REASON` — concrete justification, not abstract
- `FIX` — actionable steps with file:line precision

### Pattern summary
- Systemic patterns: ...
- Cross-page sprawl: ...
- Anomaly recurring themes: ...
```

**Return format**:
1. Empty matrix
2. Updated matrix after each page
3. Final full matrix
4. Anomaly matrix (rows with at least one mark)
5. **Phase E — FINAL HANDOFF section**

At the end, append:
- "Rules walked: {N rules} × {M pages} = {N×M} cells filled"
- "Pages reviewed: {list}"
- "Code patterns audited: {grep patterns}"
- "Total findings: {rule} rule + {pattern} pattern + {anomaly} anomaly = {total}"
```

## Aggregation logic

**This is a documentation deliverable, not a quick summary.** The user wants the full picture per page so they can fix every issue. Length is fine — quantity matters.

**No pre-filtering, no truncation.** Don't drop or cap findings. Keep `[HEURISTIC]` and `[ANOMALY]` — they often catch UX issues no rule covers yet. If a flow has 25 findings, list all 25.

**Read every sub-agent's `FINAL HANDOFF` section.** Use the structured merge-ready data, not just severity blocks.

**Primary aggregation goal: per-page fix lists.** For each page reviewed, collect every `✗` and `⚠` finding (visual + code) that landed on that page. Merge visual and code observations into a single fix entry per rule per page. Sort by severity within each page.

**Build the cross-page heatmap** as overview only. Count `✗` and `⚠` cells per page × category.

**Flag systemic findings** = any rule failing on ≥50% of pages across any sub-agent. Follow-up section, not replacing per-page lists.

**Output as a documented report** — this is meant to be saved, shared, referenced later. Real audit report structure, not a chat reply.

When the same issue is flagged within a track:
- Prefer the more specific category. Example: confusing menu flagged by both Information Architecture (`INFO-NAV-001`) and Concept (`CONCEPT-USAB-001`) → keep `INFO-NAV-001`.
- If genuinely orthogonal, keep both.

When sub-agents disagree on severity:
- Take the higher one.

When **visual and code both flag the same area**:
- Mark as **high-confidence** in output.

**Verify reference walk completion.** Each sub-agent appends `Rules walked: N/total`. Re-dispatch if under-counted.

## Output format

The primary deliverable is **per-page fix lists**. Each page reviewed gets its own actionable list of issues to fix on that page. Systemic findings are a follow-up section showing where a single system-level fix replaces multiple per-page fixes.

```
## Slop Check (UX) Result

**Platform**: {Mobile | PC} · **Domain**: {detected domain}
**Pages reviewed**: {list of pages with labels}
**Inputs**: Mockup {✓|✗} / Codebase {✓|✗} / Live URL {✓|✗}
**Sub-agents dispatched**: {N visual} visual + {N code} code = {total}
**Findings**: {H} high / {M} medium / {L} low ({S} systemic, {C} high-confidence)

---

### Cross-page heatmap (overview)

| Category | /login | /onboard1 | /onboard2 | /home |
|----------|--------|-----------|-----------|-------|
| Concept | 1 ✗ / 0 ⚠ | 3 ✗ / 1 ⚠ | 4 ✗ / 0 ⚠ | 0 ✗ / 1 ⚠ |
| Information Architecture | ... | ... | ... | ... |
| Interaction | ... | ... | ... | ... |
| Copy | ... | ... | ... | ... |
| **Total** | **2 ✗** | **6 ✗** | **8 ✗** | **1 ✗** |

→ Hot spots visible immediately.

---

## Per-page fix lists

### /login — {H} high, {M} medium, {L} low

#### High severity
1. **[RULE-ID] Rule title** — *Category*
   - **Location**: where on page / file:line
   - **What's wrong**: specific concrete observation (visual + code merged)
   - **User impact**: what experience suffers
   - **Why high severity**: frequency × consequence × reversibility
   - **Why (rule)**: cited canonical principle
   - **Fix**: actionable concrete steps with file:line touchpoints
   - **Confidence**: H/M/L
   - **System-level note**: if systemic, "→ also see Systemic [RULE-ID]"

2. **[RULE-ID] ...**

#### Medium severity
[same numbered list format]

#### Low severity
[same format]

#### Heuristic / anomaly findings on /login
- **[HEURISTIC] label**: ... · Fix: ...

---

### /onboard1 — {H} high, {M} medium, {L} low
[same per-page structure]

---

### /onboard2 — ...
[same]

---

### /home — ...
[same]

---

## Systemic findings (apply once, fix many pages)

These rules fail on ≥50% of pages — a single system-level fix replaces all the per-page fixes above.

**[RULE-ID] Rule title** — *Category*
- **Affected pages**: /login, /onboard1, /onboard2 (3/4)
- **System-level fix**: e.g., "Add shared ErrorMessage component with recovery action; remove ad-hoc handling on 3 pages"
- **Per-page fix items this replaces**: refs to the per-page entries above

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

## Sister skill: slop-check-ui

For comprehensive design review (UI + UX), also dispatch `slop-check-ui` in the same turn. Triggers like "full slop check", "complete design audit", "design slop 전부", "UI + UX 검사" mean the user wants both skills running.

When both run together, you orchestrate **up to 22 sub-agents total** (14 UI + 8 UX) in parallel.

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
- Evidence over assertion — "I see X in the flow" or "grep shows N occurrences" — never "this is confusing"
