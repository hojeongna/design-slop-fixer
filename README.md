# design-slop-fixer

> **⚡ Ultra Skill — Max 20x subscribers only.**
> This plugin spawns up to **22 parallel sub-agents** per run (visual + code-lens × 11 categories) and walks 768 canonical rules across every page you submit. Token usage is heavy. Recommended only for Claude **Max 20x** subscribers — Max 5x users will likely hit the cap mid-run, Pro is a no-go.

A Claude Code plugin that validates UI/UX mockups against 768 canonical design rules and cites every issue by `[RULE-ID]`. Catches the kind of "design slop" vibe-coded sites often ship with — wrong contrast, off spacing, hierarchy that confuses users, copy that doesn't land.

Two skills:

- **`slop-check-ui`** — 380 rules across Component, Layout, Typography, Color, Hierarchy, Spacing, Image
- **`slop-check-ux`** — 388 rules across Concept, Information Architecture, Interaction, Copy

Use this when you want **traceable rule citations** with concrete locations, severity reasons, user-impact statements, and actionable fixes — not vibes-based feedback.

## Why "ultra"

A single full review:
- Spawns up to 22 parallel sub-agents (7 UI visual + 7 UI code + 4 UX visual + 4 UX code)
- Each sub-agent reads its full reference file (~1,000-2,000 lines)
- Each walks every rule × every page (e.g., 380 rules × 5 pages = 1,900 cells per UI run)
- Each writes a comprehensive `FINAL HANDOFF` section
- Main agent merges all 22 reports into a documented audit, no truncation

This is the deepest design review you can run in a single command — and it costs accordingly. **Don't run this casually.** Save it for real audits before shipping.

## Install

```
/plugin marketplace add hojeongna/design-slop-fixer
/plugin install design-slop-fixer@design-slop-fixer
```

Or skills only (no plugin system):

```bash
git clone https://github.com/hojeongna/design-slop-fixer.git
cp -r design-slop-fixer/skills/slop-check-ui ~/.claude/skills/
cp -r design-slop-fixer/skills/slop-check-ux ~/.claude/skills/
```

## Quick start

Attach a mockup screenshot in Claude Code, then **ask explicitly for rule-based check**:

- *"Slop check this UI"*
- *"Audit this mockup against design rules"*
- *"Find specific UI violations with rule IDs"*
- *"Cite UX issues by rule"*

The matching skill auto-triggers and walks the canonical rules.

This is built for explicit rule-based audits — not casual "how does this look" feedback.

## How it works

Each canonical rule has these fields:

| Field | What it is |
|-------|-----------|
| Title | Short rule name |
| Principle | What to do (or not do) |
| Why | Reasoning |
| Anti-pattern | What failure looks like |
| Platform | Mobile / PC / Both |
| Frequency weight | How strongly the rule was emphasized in source feedback |

Reviews cite every violation by `[RULE-ID]`, so claims are traceable.

## What's inside

| Skill | Categories | Rules | Sub-categories |
|-------|------------|-------|----------------|
| `slop-check-ui` | Component, Layout, Typography, Color, Hierarchy, Spacing, Image | 380 | 81 |
| `slop-check-ux` | Concept, Information Architecture, Interaction, Copy | 388 | 46 |

### UI Track (380 rules)

- **Component** (41) — Button, Icon, Card, Tab, Profile, Input field, Design system consistency
- **Layout** (53) — Grid, Alignment, Section composition, Responsive breakpoints, Layout rhythm
- **Typography** (30) — Font size, Line height, Weight, Readability, Hierarchy
- **Color** (80) — Contrast/accessibility, Accent restraint, Text hierarchy, Background, Gray, Shadow/effect, Gradient, Tone, Black restraint
- **Hierarchy** (52) — Emphasis, Contrast, Information priority
- **Spacing** (65) — Whitespace fundamentals, Padding, Margin, Section spacing, Rhythm
- **Image** (59) — Size, Aspect ratio, Treatment, Quality, Thumbnail

### UX Track (388 rules)

- **Concept** (100) — Restraint, Concept consistency, Usability first, Benchmarking, Minimalism, System & standards, Intentional design, Composition, Domain fit, Practical sense
- **Information Architecture** (150) — Grouping, Navigation, Menu structure, GNB/Tab bar, Information hierarchy, Search, Filter
- **Interaction** (122) — Button behavior, Modal/Popup, Feedback, Error handling, Loading, Toast, Affordance, Scroll, Gesture
- **Copy** (16) — Tone, Button copy, Error message, Microcopy, Clarity

## Output format

```
## Slop Check (UI) Result

### [RULE-ID] Rule title — Severity (high/medium/low)
- Observation: what I see in the mockup
- Principle: cited canonical rule
- Suggestion: concrete fix
- Related: [OTHER-ID] for cross-reference
```

## Disclaimer

These rules are one curated take on general design principles. Domain and product context matter — treat the review as a second opinion, not a strict checklist.

## License

MIT
