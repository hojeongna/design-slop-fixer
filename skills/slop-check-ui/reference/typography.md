# Typography (UI)

Font size, weight, line height, readability rules

- **Total canonical rules**: 30
- **Sub-categories**: 10

---

## Contents
- Minimum body text size — 3 canonical
- Line height — 3 canonical
- Letter spacing — 2 canonical
- Font hierarchy — 3 canonical
- Font weight usage — 3 canonical
- Font family consistency — 3 canonical
- Text alignment — 2 canonical
- Special-region text — 4 canonical
- Typography system and scale — 4 canonical
- Readability first — 3 canonical

---

## Minimum body text size (3 canonical)

_Covers minimum font size standards and readability thresholds for body, secondary, and special text._

### [TYPO-BODY-001] Minimum 14px for body text
- **Platform**: M/o/b/i/l/e
- **Frequency weight**: 16
- **Sub-category**: Minimum body text size

**Principle**: Body text on mobile and web must be at least 13-14px to ensure readability. Anything below this threshold becomes difficult for users to read.

**Why**: In real-world conditions (mobile viewing distance, varying light, aging eyes), body text under 12px imposes significant cognitive load. Major platform guidelines also treat 14px as the practical minimum.

**Anti-pattern**: Using body text under 12px because it looks fine on a designer's monitor, resulting in broken readability on actual devices.

---

### [TYPO-BODY-002] Web body text 14-16px standard
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Minimum body text size

**Principle**: In web UI, standard body text should be 14-16px. Dashboards and admin screens center on 14px; general landing and marketing pages center on 16px. Reserve sizes of 20px or larger for emphasis elements only.

**Why**: If web body text is too large, the hierarchy with titles collapses and layout density breaks down. 14-16px strikes the right balance between readability and information density.

**Anti-pattern**: Using 20px or larger for standard body text, making it impossible to distinguish hierarchy from titles.

---

### [TYPO-BODY-003] Avoid 12px and 10px
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Minimum body text size

**Principle**: Never use 10px fonts in UI, and avoid 12px whenever possible. Allow 12px only in a limited way for auxiliary metadata such as badges and tags.

**Why**: At 10px, readability degrades severely and the size is effectively unusable. Using 12px for body copy or critical information also harms the user experience.

**Anti-pattern**: Shrinking important text to 10-12px to save space, producing a UI that cannot be read.

---

## Line height (3 canonical)

_Covers line-height standards for body and title text, the principle of setting explicit numeric values, and the interplay between line height and letter spacing._

### [TYPO-LH-001] Generous line height for body text
- **Platform**: Mobile/PC
- **Frequency weight**: 14
- **Sub-category**: Line height

**Principle**: Set body text line height with ample breathing room to ensure readability. As a rule, 140-160% of the font size is recommended, while 100% is too tight in nearly every case.

**Why**: Tight line height makes text blocks feel cramped and heavy, hurting readability. Generous line height lets the text breathe, improving both legibility and visual comfort.

**Anti-pattern**: Leaving line height at the default (auto or 100%), creating cramped, suffocating text blocks.

---

### [TYPO-LH-002] Set line height with explicit values
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Line height

**Principle**: Do not rely on 'Auto' line height; set explicit percentage values (e.g., 130%, 140%) by hand. The larger and bolder the font, the tighter the line height should be in order to maintain a stable visual rhythm.

**Why**: Auto line height does not reflect the designer's intent and produces different results across fonts. Specifying explicit values guarantees consistent typography.

**Anti-pattern**: Shipping with line height set to Auto, causing layouts to collapse whenever the font changes.

---

### [TYPO-LH-003] Tune line height and letter spacing together
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Line height

**Principle**: If line height feels tight, letter spacing is likely off as well. The two properties are interconnected, so when tuning one, always review and adjust the other. The more conceptual the design, the more this detail defines the level of polish.

**Why**: Line height and letter spacing together determine the density and rhythm of text. Adjusting only one of them produces unbalanced typography.

**Anti-pattern**: Widening line height while leaving letter spacing untouched, producing a discord that is dense horizontally yet wide vertically.

---

## Letter spacing (2 canonical)

_Covers the principle of setting letter spacing deliberately and the rule against using overly tight letter spacing._

### [TYPO-LS-001] Always set letter spacing intentionally
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Letter spacing

**Principle**: Set letter spacing and line height intentionally for every text element, never relying on defaults. Letter spacing is a fundamental skill that directly affects readability and typographic polish.

**Why**: Leaving letter spacing alone makes text feel clumped or overly loose, lowering the perceived quality of the work. Deliberate letter-spacing control is foundational to a designer's typographic craft.

**Anti-pattern**: Leaving letter spacing at 0 (default), making text feel overly dense and unrefined.

---

### [TYPO-LS-002] Avoid overly tight letter spacing
- **Platform**: P/C
- **Frequency weight**: 2
- **Sub-category**: Letter spacing

**Principle**: Letter spacing around -5% is excessively tight and should not be used. Always set the value explicitly to control intent; -2% to -3% is generally a safe range.

**Why**: Overly tight letter spacing severely hurts readability. Auto letter spacing also reduces polish, so explicit values are essential.

**Anti-pattern**: Cramming text together at -5% letter spacing in pursuit of a sleek look, ending up with degraded readability.

---

## Font hierarchy (3 canonical)

_Covers principles for designing font size and weight hierarchy across titles, subtitles, body, and secondary text._

### [TYPO-HIER-001] Make title-to-body hierarchy explicit
- **Platform**: Mobile/PC
- **Frequency weight**: 26
- **Sub-category**: Font hierarchy

**Principle**: Define font hierarchy (title - subtitle - body - secondary) explicitly. When the same style repeats or the hierarchy is ambiguous, users cannot tell what information is important.

**Why**: The clearer the visual hierarchy, the faster users can scan and grasp key information. Typography without hierarchy collapses the information architecture itself.

**Anti-pattern**: Using the same font size and weight for every piece of text, leaving users with no idea where to start reading.

---

### [TYPO-HIER-002] Express hierarchy through size
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Font hierarchy

**Principle**: Hierarchy reads more clearly through size changes than through weight changes. Make titles clearly larger than body text, but avoid going so large that the layout's center of gravity is thrown off.

**Why**: Size differences communicate hierarchy more intuitively than weight differences. The modern approach is to establish hierarchy through size first, using weight as a secondary tool.

**Anti-pattern**: Keeping title and body at the same size and only changing weight, leaving a faint hierarchy with weak visual impact.

---

### [TYPO-HIER-003] Review the full type combination
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Font hierarchy

**Principle**: Always review the hierarchy and harmony of the entire screen's type combination (header - body - caption, etc.), not individual elements in isolation. Typography is judged as a whole composition.

**Why**: Each text element can look fine on its own, yet the overall composition often loses balance or becomes hierarchically unclear when combined.

**Anti-pattern**: Reviewing only individual text elements and skipping the overall combination, lowering the screen's level of polish.

---

## Font weight usage (3 canonical)

_Covers limiting the number of font weights, pairing larger sizes with thinner weights, and avoiding misuse of bold._

### [TYPO-WT-001] Limit weights to 2-3 styles
- **Platform**: Mobile/PC
- **Frequency weight**: 24
- **Sub-category**: Font weight usage

**Principle**: Limit font weights across the entire design to 2-3 options (e.g., Regular, Medium, Bold) and apply them by a consistent rule. Text at the same hierarchy level should use the same weight on every screen.

**Why**: The more weights in play, the less consistent the design feels, signaling that work was done without a shared guide. Operating systematically with a small set of weights makes maintenance easier.

**Anti-pattern**: Mixing Regular, Medium, SemiBold, Bold, and ExtraBold all together, breaking down consistency.

---

### [TYPO-WT-002] Larger size, lighter weight
- **Platform**: Mobile/PC
- **Frequency weight**: 16
- **Sub-category**: Font weight usage

**Principle**: When scaling text up, lighten the weight (Light to Regular) at the same time to keep the impression refined rather than heavy. For display sizes in particular, Regular or lighter is the balanced choice.

**Why**: Pairing large font sizes with heavy weights makes the whole screen feel heavy and clunky. The 'large and light' combination preserves presence while delivering a refined, minimal impression.

**Anti-pattern**: Setting large titles in ExtraBold, leaving the entire screen feeling heavy and oppressive.

---

### [TYPO-WT-003] Do not overuse bold in body text
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Font weight usage

**Principle**: For body-level text, consider Medium or SemiBold first instead of Bold. Unnecessary Bold blurs the contrast hierarchy and weighs down the entire screen. On dark backgrounds, drop the weight even further.

**Why**: Bold only works when reserved for elements that genuinely need emphasis. When every piece of text is bold, nothing is emphasized.

**Anti-pattern**: Bolding all body text in the name of better readability, collapsing hierarchy and increasing visual fatigue.

---

## Font family consistency (3 canonical)

_Covers using one font per language and role, choosing fonts well-suited to Korean UI, and managing font styles systematically._

### [TYPO-FF-001] One font per language
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Font family consistency

**Principle**: Within a single service, use the same font for the same language (Korean / English). Define a clear rule for font selection (e.g., font A for Korean, font B for English) and apply it consistently across the product.

**Why**: Mixing different fonts within the same language breaks design consistency and lowers perceived polish. In practice, font mixing also makes maintenance harder.

**Anti-pattern**: Mixing Noto Sans for some Korean text and Pretendard for other Korean text on the same screen.

---

### [TYPO-FF-002] Choose fonts optimized for Korean UI
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Font family consistency

**Principle**: For Korean UI, choose fonts with strong Korean readability such as Pretendard or Noto Sans KR rather than Latin-optimized fonts like Roboto. Consider visual weight as part of the selection.

**Why**: Applying Latin-focused fonts to Korean text reduces readability and feels off. Fonts optimized for Korean UI elevate both polish and brand credibility.

**Anti-pattern**: Using Roboto or fonts with strong brand identity for Korean UI, reducing readability and neutrality.

---

### [TYPO-FF-003] Manage font styles as a system
- **Platform**: P/C
- **Frequency weight**: 1
- **Sub-category**: Font family consistency

**Principle**: Group font styles and manage them systematically, keeping a list of styles in use organized in a dedicated panel or at the top of the file.

**Why**: Without organized font styles, maintaining design consistency becomes difficult and collaboration falls into confusion.

---

## Text alignment (2 canonical)

_Covers left-aligning body and list text, keeping alignment consistent within a region, and controlling text line breaks._

### [TYPO-ALIGN-001] Left-align body text
- **Platform**: M/o/b/i/l/e
- **Frequency weight**: 9
- **Sub-category**: Text alignment

**Principle**: Body, list, and descriptive text read more easily when left-aligned rather than centered. For text that runs two or more lines, center alignment disrupts the eye's flow.

**Why**: Left alignment guides the eye naturally from left to right and top to bottom. Center alignment increases reading fatigue with longer text.

**Anti-pattern**: Center-aligning list content or long descriptive body text, hurting readability.

---

### [TYPO-ALIGN-002] Consistent alignment and controlled line breaks
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Text alignment

**Principle**: Keep text alignment consistent within a single card or section. Set titles on one line whenever possible, and avoid unnecessary line breaks when there is enough space.

**Why**: Mixed alignments send the eye drifting diagonally, reducing readability. Unintended line breaks weaken how clearly the message comes across.

**Anti-pattern**: Mixing a left-aligned card title with center-aligned body text, or letting a title wrap to two lines despite having sufficient space.

---

## Special-region text (4 canonical)

_Covers font handling principles for special UI regions such as text over images, GNB/navigation, buttons and chips, and section/card/popup titles._

### [TYPO-SPEC-001] Readable text over images
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Special-region text

**Principle**: When placing text over a bright image or background image, always apply a gradient dimming overlay to secure readability.

**Why**: The readability of text over images depends entirely on background brightness. The presence or absence of a dim overlay makes a clear difference, so it is mandatory rather than optional.

**Anti-pattern**: Placing white text on a bright hero image with no overlay, leaving the text completely buried.

---

### [TYPO-SPEC-002] Keep GNB text light
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Special-region text

**Principle**: Set GNB and navigation text smaller and lighter (Regular to Medium) than content text to preserve overall hierarchy. The GNB supports content rather than competing with it, and around 16px is standard.

**Why**: If GNB text is too large or too bold, attention shifts from content to navigation and the information hierarchy is inverted.

**Anti-pattern**: Setting GNB menu items in large SemiBold, making navigation register more strongly than the actual content.

---

### [TYPO-SPEC-003] Standards for button and chip text
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Special-region text

**Principle**: Scale text inside a button in proportion to the button itself. Give CTA buttons visual force with Bold or SemiBold, and render placeholder text lighter than actual input text to clearly distinguish state.

**Why**: An imbalance between button size and internal text feels awkward. Bold text on a CTA button strengthens click-through pull.

**Anti-pattern**: Placing small text inside a large button, or rendering a CTA button in Regular weight, weakening its click-through pull.

---

### [TYPO-SPEC-004] Section, card, and popup title sizing
- **Platform**: Mobile/PC
- **Frequency weight**: 28
- **Sub-category**: Special-region text

**Principle**: Make section titles larger than body text but kept within a range that does not break the overall layout balance. Set popup and bottom-sheet titles to at least 16pt so the screen's purpose is instantly recognizable. Never invert sizes such that a card's internal body text becomes larger than the outer title.

**Why**: When the size ratio between a section title and its content is off, layout balance collapses. All essential information must be large enough to be read at a glance.

**Anti-pattern**: Making a module's internal title larger than or equal to the page title, or shrinking a popup title to 12px so its purpose becomes unclear.

---

## Typography system and scale (4 canonical)

_Covers using a standard font-size scale, establishing a shared typography guide, and handling text truncation and responsive variants._

### [TYPO-SYS-001] Use a standard size scale
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Typography system and scale

**Principle**: Pick font sizes from a standard scale built on 4pt or 8pt multiples (14, 16, 18, 20, 24, etc.). Arbitrary values like 105, 71, or 27, or vague in-between numbers, signal that no typography system exists.

**Why**: A standard scale produces clear hierarchy and a consistent typographic rhythm. Arbitrary values complicate maintenance and collaboration.

**Anti-pattern**: Using arbitrary values like 105px for a title and 71px for a subtitle, blurring hierarchy and creating collaboration confusion.

---

### [TYPO-SYS-002] Shared text style guide
- **Platform**: M/o/b/i/l/e
- **Frequency weight**: 6
- **Sub-category**: Typography system and scale

**Principle**: Define a shared guide for text styles (size, weight, line height, letter spacing, color) before applying them, then apply it systematically to every element. Evaluate typography as an overall composition, not as isolated elements.

**Why**: Handling each case differently without a guide breaks consistency and makes future maintenance painful. A typography system is what makes collaboration and scaling possible.

**Anti-pattern**: Setting different title sizes and weights on every screen, producing an inconsistent UI.

---

### [TYPO-SYS-003] Text truncation policy
- **Platform**: M/o/b/i/l/e
- **Frequency weight**: 1
- **Sub-category**: Typography system and scale

**Principle**: Decide upfront whether text in repeating UI elements (dates, titles, cards, etc.) is allowed to wrap, and define a truncation/clamp policy. Text must either fit entirely inside its container or be explicitly clamped.

**Why**: Without designed text-overflow behavior, long content breaks the UI as soon as it arrives.

**Anti-pattern**: Leaving text clamping undefined so that long titles overflow card boundaries and break the UI.

---

### [TYPO-SYS-004] Separate responsive font sizes
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Typography system and scale

**Principle**: In responsive design, define font sizes, spacing, and element sizes separately for each breakpoint. Never carry PC values straight over to mobile.

**Why**: Because PC and mobile differ in screen size and viewing distance, using the same font size on both will inevitably cause readability problems on one of them.

**Anti-pattern**: Applying PC font settings unchanged to mobile, causing readability issues on one side or the other.

---

## Readability first (3 canonical)

_Covers the principle that readability outweighs aesthetic preference, reviewing on actual devices, and the importance of practicing with larger type._

### [TYPO-READ-001] Readability over aesthetics
- **Platform**: Mobile/PC
- **Frequency weight**: 27
- **Sub-category**: Readability first

**Principle**: When deciding font size and color, prioritize readability over aesthetic preference. Trying to make a design look 'clean' through small type is a flawed approach that sacrifices readability. Just adjusting font size and spacing alone can substantially improve both readability and overall design quality.

**Why**: The primary purpose of design is helping users read and understand information easily. No matter how visually beautiful, a design that cannot be read is a design that has failed.

**Anti-pattern**: Using small type to free up whitespace for a 'clean' look, sacrificing readability in the process.

---

### [TYPO-READ-002] Review on the actual device
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Readability first

**Principle**: Judge mobile font sizes against the actual device, not a zoomed-in Figma canvas. When benchmarking the type sizes of real services, compare by measured values rather than by feel.

**Why**: Type that looks large in Figma can look right-sized or even small on an actual device. The font sizes of reference designs also need to be validated as realistically implementable.

**Anti-pattern**: Reviewing at 200% zoom in Figma, judging the size as appropriate, and ending up with text that is too small on the actual device.

---

### [TYPO-READ-003] Practice using larger type
- **Platform**: M/o/b/i/l/e
- **Frequency weight**: 1
- **Sub-category**: Readability first

**Principle**: Build the habit of using larger type so you can design layouts with real sense of scale, which also strengthens your hierarchy skills. Always defaulting to small type prevents your sense of contrast from developing.

**Why**: If you only ever get comfortable with small type, you never develop the ability to express hierarchy through size. Boldly scaling up is the shortcut to improving typographic skill.

---
