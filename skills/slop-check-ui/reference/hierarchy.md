# Hierarchy (UI)

Information hierarchy, visual emphasis, priority rules

- **Total canonical rules**: 52
- **Sub-categories**: 13

---

## Contents
- Core information top priority emphasis — 6 canonical
- Restrain over-emphasis of secondary elements — 5 canonical
- Emphasis & contrast — 6 canonical
- Visual hierarchy fundamentals — 6 canonical
- Content vs. title priority — 4 canonical
- Element collision & balance — 3 canonical
- Eye flow & visual center of gravity — 4 canonical
- Selection state & hierarchy expression — 7 canonical
- Usage-frequency-based emphasis design — 3 canonical
- Weakening dividers, backgrounds & effects — 3 canonical
- Readability & visual hierarchy — 2 canonical
- Banner hierarchy design — 2 canonical
- Emphasis priority — 1 canonical

---

## Core information top priority emphasis (6 canonical)

### [HIE-INFO-001] Place information by order of importance
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Core information top priority emphasis

**Principle**: Arrange information in order of importance. More important information must occupy more visible positions (top placement, larger size, bolder weight). Visual hierarchy is complete only when emphasis and position align.

**Why**: Users read top to bottom, starting with the most strongly emphasized elements. When importance and visual position misalign, information takes longer to grasp.

**Anti-pattern**: Enrollment and graduation years placed in a more prominent position than the school name, causing less important information to register first.

---

### [HIE-INFO-002] Never invert hierarchy
- **Platform**: Mobile/PC
- **Frequency weight**: 13
- **Sub-category**: Core information top priority emphasis

**Principle**: Visual hierarchy must match the order of importance. If descriptive text appears visually stronger than core information (names, titles, figures), the hierarchy is inverted. Labels and badges must be visually weaker than titles.

**Why**: When hierarchy inverts, users perceive less important information first, causing confusion.

**Anti-pattern**: App description text shown larger than the app name, or tags rendered stronger than titles.

---

### [HIE-INFO-003] Design strong-weak hierarchy inside cards
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Core information top priority emphasis

**Principle**: Apply a clear strong-weak hierarchy to elements inside card UIs. The most important information must be recognizable at a glance, with color, size, and weight varied to create visual order based on importance.

**Why**: Even with a card structure in place, a flat internal information hierarchy makes it impossible to see what matters.

**Anti-pattern**: Brand name, product name, price, and rating inside a card all rendered at the same size and style, leaving no hierarchy at all.

---

### [HIE-INFO-004] Emphasize numbers in data visualization
- **Platform**: PC
- **Frequency weight**: 4
- **Sub-category**: Core information top priority emphasis

**Principle**: In data visualization, emphasize the numbers themselves rather than the labels. Chart titles should play a supporting role, and title size must be restrained so the visualization itself remains the protagonist. Multiple data series within a chart must also distinguish primary from secondary data through color, thickness, and opacity.

**Why**: The numbers are what users need to read first in a graph. When labels or titles are emphasized, recognition of the numbers is delayed.

**Anti-pattern**: A 'customer complaints' label emphasized over the '8%' figure in a chart, delaying recognition of the core data.

---

### [HIE-INFO-005] Emphasize benefits and outcomes over calls to action
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Core information top priority emphasis

**Principle**: Even within CTA areas, emphasize the benefit the user receives more strongly than the action prompt itself to drive click motivation. On result screens, display core information (IDs, completion messages, etc.) at sufficient size and clarity for instant recognition.

**Why**: Users are more sensitive to 'what they gain' than to the action itself.

**Anti-pattern**: 'Get promo code' emphasized more than the 'code reward' benefit content, weakening click motivation.

---

### [HIE-INFO-006] Give each formula element its own hierarchy
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Core information top priority emphasis

**Principle**: When displaying a calculation or formula structure (A -> B = result), assign hierarchy to each element. Operators, result values, and input values must differ in size or color.

**Why**: When every element shares the same hierarchy, it becomes hard to identify where the result is and which values are inputs.

**Anti-pattern**: All formula elements rendered at the same hierarchy, making the result invisible at a glance.

---

## Restrain over-emphasis of secondary elements (5 canonical)

### [HIE-SUB-001] Never let CTA buttons overpower content
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Restrain over-emphasis of secondary elements

**Principle**: CTA buttons must carry less visual weight than the primary content (images, text). When buttons overpower content, user attention shifts to the button before they grasp the message, eliminating motivation to act.

**Why**: Users decide to act after reading the content first. Once they recognize that the entire banner is clickable, a strong button becomes a hindrance rather than a help.

**Anti-pattern**: A heavy black CTA button inside a banner that draws the eye away from the banner message, with the supporting element overshadowing the main one.

---

### [HIE-SUB-002] Visually weaken secondary action buttons
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Restrain over-emphasis of secondary elements

**Principle**: Secondary action buttons such as 'view details', 'view all', 'expand/collapse', and 'change' must be rendered visually weaker than the primary content or primary CTA. A button's visual intensity must be proportional to its importance and frequency of use.

**Why**: Treating secondary actions strongly inverts the hierarchy with the primary content.

**Anti-pattern**: A 'change card' button on a payment page emphasized more than the payment flow itself, scattering user attention.

---

### [HIE-SUB-003] Treat helper text as the lowest tier
- **Platform**: Mobile
- **Frequency weight**: 5
- **Sub-category**: Restrain over-emphasis of secondary elements

**Principle**: Treat helper text and supporting descriptions as the lowest tier on the page. Font size, color, and weight must all be weaker than the main information. High intensity is mistaken for high importance.

**Why**: Strong helper text pulls user attention to supporting information first, disrupting the core flow.

**Anti-pattern**: Helper text on an order form rendered visually stronger than the shipping address or product name, inverting importance.

---

### [HIE-SUB-004] Keep GNB and navigation quieter than content
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Restrain over-emphasis of secondary elements

**Principle**: GNB and headers must be visually quieter than the content. Reduce size, weight, and color so navigation recedes behind the content. Include only the GNB elements that are truly necessary, and review the rationale for each one.

**Why**: Navigation exists to support content. When over-emphasized, the supporting role takes over the leading role.

**Anti-pattern**: GNB text rendered bolder and larger than the main content, or a search UI so prominent that it pushes the content aside.

---

### [HIE-SUB-005] Keep supporting UI elements weaker than content
- **Platform**: Mobile
- **Frequency weight**: 5
- **Sub-category**: Restrain over-emphasis of secondary elements

**Principle**: Supporting UI such as navigation arrows and icons must be rendered visually weaker than the content so users can focus on it. Repeating the same effect across multiple areas erases hierarchy. Use effects only when they create a clear hierarchical difference.

**Why**: Oversized icons capture attention before the text information that actually matters.

**Anti-pattern**: Arrows thicker and darker than the text so they catch the eye before the content, or identical glass effects applied to both top and bottom areas.

---

## Emphasis & contrast (6 canonical)

### [HIE-EMPH-001] Lead emphasis with size contrast first
- **Platform**: Mobile
- **Frequency weight**: 6
- **Sub-category**: Emphasis & contrast

**Principle**: The correct order for text emphasis is (1) establish strong-weak contrast through size, weight, and spacing, then (2) use color as a supporting means. Attempting to emphasize first with color or decoration (backgrounds, gradients) only creates visual noise.

**Why**: Size contrast is the most intuitive and quickly perceived. Decorative elements more often raise visual complexity than they emphasize.

**Anti-pattern**: Trying to emphasize price by simultaneously applying background, gradient, and color, which actually degrades readability.

---

### [HIE-EMPH-002] Scale up core numbers boldly
- **Platform**: Mobile/PC
- **Frequency weight**: 11
- **Sub-category**: Emphasis & contrast

**Principle**: Core numbers (prices, KPIs, view counts, times, etc.) must be rendered overwhelmingly larger than the surrounding descriptive text. Treat units and labels as small and light, and when establishing hierarchy, boldly increasing size is more effective than relying on weight changes alone.

**Why**: On dashboards and cards, the core numbers are what users must grasp fastest. When sized similarly to surrounding descriptions, the numbers become buried.

**Anti-pattern**: Core numbers and their units (%) sized similarly, leaving the user unsure where to focus.

---

### [HIE-EMPH-003] Emphasize clearly with a single method
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Emphasis & contrast

**Principle**: It is enough to emphasize an element clearly with a single method. When the same effect, color, or style is applied to multiple elements on one screen, hierarchy disappears and nothing ends up emphasized.

**Why**: Emphasis is relative. When everything is emphasized, the baseline for emphasis disappears.

**Anti-pattern**: Buttons, tabs, and badges all sharing the same accent color, collapsing hierarchy across the entire screen.

---

### [HIE-EMPH-004] Verify emphasis intent matches the result
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Emphasis & contrast

**Principle**: An element you intend to emphasize must actually stand out visually. If your intended emphasis is buried by surrounding elements, change the emphasis method or increase its intensity.

**Why**: When intent and outcome diverge, the design fails to achieve its purpose.

**Anti-pattern**: Bold applied but surrounding buttons obscure the emphasis, or a price intended to be emphasized buried by surrounding colors.

---

### [HIE-EMPH-005] Design remaining intensity using the CTA as baseline
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Emphasis & contrast

**Principle**: Take the color intensity of the most important call to action in the UI as the baseline, and design every other element weaker than it. When color changes alone are insufficient for important emphasized information, wrap it in a container or badge for a more distinct emphasis effect.

**Why**: Once a baseline element is fixed, judging the relative intensity of other elements becomes easier.

**Anti-pattern**: Designing each element individually without a baseline, mixing in elements stronger than the baseline CTA and collapsing hierarchy.

---

### [HIE-EMPH-006] Always have at least one emphasis point
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Emphasis & contrast

**Principle**: Every design must contain at least one visual emphasis point. When all elements are equally emphasized, nothing is emphasized, attention scatters, and core information fails to come through.

**Why**: Without an emphasis point, users do not know where to look.

**Anti-pattern**: All numbers and text rendered at the same intensity, leaving no emphasis point at all.

---

## Visual hierarchy fundamentals (6 canonical)

### [HIE-BASIC-001] Triangular font hierarchy principle
- **Platform**: PC
- **Frequency weight**: 7
- **Sub-category**: Visual hierarchy fundamentals

**Principle**: Vary font size and weight in a triangular structure of large (title), medium (subtitle), and small (body and supplementary information). When the overall volume is uniformly large or small, hierarchy disappears and information becomes hard to recognize.

**Why**: Without hierarchy, users do not know where to start reading. The triangular structure naturally guides the eye from the most to the least important.

**Anti-pattern**: Title, subtitle, and body all sharing the same font size and weight, forcing users to read the content just to grasp its structure.

---

### [HIE-BASIC-002] Four fundamentals of dashboard design
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Visual hierarchy fundamentals

**Principle**: Dashboard design quality is determined by four fundamentals: spacing, font size, font hierarchy, and layout. Sort these four out first, and the overall impression transforms.

**Why**: Detail completeness on the fundamentals shapes final quality more than any special styling. Even with a sound layout structure, weak detail on internal elements makes the work look unfinished.

**Anti-pattern**: Starting decoration with color or illustration first, locking in low overall quality due to missing fundamentals.

---

### [HIE-BASIC-003] Master hierarchy fundamentals before decoration
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Visual hierarchy fundamentals

**Principle**: Designers must first develop the ability to organize visual hierarchy before decorating. Practice creating emphasis points through hierarchy fundamentals (size, weight, and spacing contrast) before reaching for visual decoration.

**Why**: Focusing only on visual decoration without a basic hierarchy structure makes it hard to earn recognition for quality.

**Anti-pattern**: Attempting emphasis through color and effects without hierarchy, so everything looks emphasized yet nothing actually registers.

---

### [HIE-BASIC-004] Maintain hierarchy consistency throughout
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Visual hierarchy fundamentals

**Principle**: Text elements that play the same role (title, body, etc.) must keep their size, color, and spacing consistent across all screens and sections. Maintain font hierarchy and spacing groupings consistently across the entire page to raise design completeness.

**Why**: Consistent hierarchy lets users grasp structure without having to relearn it each time.

**Anti-pattern**: Title sizes varying from screen to screen, causing users to perceive same-level elements as having different importance.

---

### [HIE-BASIC-005] Inspect font, spacing, and color together
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Visual hierarchy fundamentals

**Principle**: If any one of font size and weight, spacing, or color contrast is lacking, the entire design looks sloppy. Review the three together, and when one changes, adjust the others accordingly.

**Why**: When all three design elements falter at once, the completeness of the entire section drops sharply.

**Anti-pattern**: Font, spacing, and color all underdeveloped at once, so no single fix can resolve it.

---

### [HIE-BASIC-006] Build text hierarchy with combined means
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Visual hierarchy fundamentals

**Principle**: Text hierarchy must combine not only size contrast but also weight, color, and letter spacing for the design to feel detailed and intentional. Size differences alone do not convey deliberate hierarchy design.

**Why**: When only size differs and weight or color stay the same, the hierarchy feels weak. Hierarchy is complete only when combined means are applied.

**Anti-pattern**: Only size variation with no difference in weight or color, giving the impression of a title slapped together without thought.

---

## Content vs. title priority (4 canonical)

### [HIE-TITLE-001] Reduce titles and emphasize the primary content
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Content vs. title priority

**Principle**: The recent UI trend is to lower the visual intensity of titles while bringing the primary content (numbers, content itself) forward. Labels and titles play a guiding role, not the leading one. Section titles are reference information, so lower their emphasis and place visual priority on the content.

**Why**: Users check the actual content (numbers, product names, content itself) far more than they check the titles.

**Anti-pattern**: A dashboard section title standing out more than the KPI figures, or search filter labels rendered bolder than the input values.

---

### [HIE-TITLE-002] Balance the title-to-body ratio
- **Platform**: Mobile
- **Frequency weight**: 4
- **Sub-category**: Content vs. title priority

**Principle**: When changing title size, adjust the ratio with the body text as well to keep hierarchy in balance. A strong title with weak body text reduces information impact, and an excessive gap between the two also breaks balance.

**Why**: Hierarchy is determined by relative ratios, not by absolute size.

**Anti-pattern**: Enlarging the title while leaving the body unchanged, collapsing the title-body hierarchy.

---

### [HIE-TITLE-003] Design section title placement and hierarchy
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Content vs. title priority

**Principle**: Section titles work better for readability and layout balance when placed outside images or dark containers rather than within them. Lower the hierarchy of subsection titles after the intro to preserve the page's overall visual flow. When no title exists but tabs do, treat the tabs themselves as the title.

**Why**: Titles inside dark backgrounds weigh the layout down and hurt readability.

**Anti-pattern**: Every section title repeated at the same size and weight, leaving no sense of which is more important.

---

### [HIE-TITLE-004] Concentrate visual emphasis on core functionality
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Content vs. title priority

**Principle**: Concentrate visual emphasis on the page's core functionality or content, not on its title. Determine UI hierarchy by the order in which users actually need information; titles do not always have to be the most emphasized.

**Why**: Just as the map matters more than the title on a map selection screen, the subject of emphasis must shift with the page's purpose.

**Anti-pattern**: Putting weight on the title on a map selection page, leaving the actual interaction area relatively weak.

---

## Element collision & balance (3 canonical)

### [HIE-BAL-001] Give equivalent elements a hierarchy
- **Platform**: Mobile
- **Frequency weight**: 6
- **Sub-category**: Element collision & balance

**Principle**: Two elements of similar nature placed side by side or carrying similar visual mass collide with each other. Distinguish one as primary and one as secondary in visual priority, or make a clear difference in size or style.

**Why**: Elements of equal volume steal attention from each other, leaving none of them visible.

**Anti-pattern**: Two buttons sharing the same size, color, and position, colliding without hierarchy.

---

### [HIE-BAL-002] Balance images and text visually
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Element collision & balance

**Principle**: Adjust image and text sizes to achieve visual balance with each other. Text placed beside a large image needs ample letter and line spacing, with title size scaled up to match the image. When the title overpowers the image, the image dies.

**Why**: When image and text lose balance, one inevitably kills the other.

**Anti-pattern**: A strong billboard image paired with weak internal type, or a title so prominent that the image's presence disappears.

---

### [HIE-BAL-003] Distinguish sections through volume contrast
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Element collision & balance

**Principle**: Distinguish sections within a screen through strong-weak contrast in visual mass. Repeating the same volume removes corner distinction and creates visual monotony. When a design feels bland, raise the volume (size, thickness, contrast) of individual elements rather than restructuring the whole.

**Why**: Volume contrast is the most natural means by which users perceive section boundaries.

**Anti-pattern**: Every section repeated at the same visual mass, leaving sections indistinguishable from one another.

---

## Eye flow & visual center of gravity (4 canonical)

### [HIE-FLOW-001] Design the eye flow intentionally
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Eye flow & visual center of gravity

**Principle**: Design hierarchy and emphasis so that the user's gaze flows naturally in the intended order. The moment users have to actively 'search', hierarchy design has already failed.

**Why**: An information structure that requires active searching adds cognitive load and drives users away.

**Anti-pattern**: A layout where users do not know where to look, or a design with no consideration for eye flow.

---

### [HIE-FLOW-002] Horizontal eye flow and numbering
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Eye flow & visual center of gravity

**Principle**: Lay out comparison data (prices, figures) along a left-to-right horizontal eye flow in a single row so it can be read at a glance. When placing order-sensitive information in grid or card layouts, visualize the numbering clearly.

**Why**: Diagonal compositions or scattered placements force the gaze to move repeatedly, making comprehension harder.

**Anti-pattern**: Price comparison information laid out in a diagonal composition, causing the gaze to jump around and obscuring the prices.

---

### [HIE-FLOW-003] Distinguish visual complexity from visual weight
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Eye flow & visual center of gravity

**Principle**: Visual complexity and visual weight are different. Even simplified elements can carry appropriate weight through size, dimensionality, and color contrast. You can secure a visual center of gravity while reducing unnecessary complexity.

**Why**: Older designs often have visual complexity without any visual weight.

**Anti-pattern**: Plenty of icons and text but no center of gravity, leaving the design feeling thin.

---

### [HIE-FLOW-004] Make core content recognized first on entry
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Eye flow & visual center of gravity

**Principle**: Compose the layout so that the element a user must recognize first—aligned with the page's purpose—is visually foregrounded above all else. Structural devices appearing before content is a hierarchy failure.

**Why**: When users enter a page, they must immediately recognize the intended core information.

**Anti-pattern**: The center line of a timeline catching the eye before the project images, so the structure rather than the content registers first.

---

## Selection state & hierarchy expression (7 canonical)

### [HIE-STATE-001] Clearly distinguish selected and unselected states
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Selection state & hierarchy expression

**Principle**: In menus and categories, separate selected from unselected items with clear contrast in font weight or color to create visual order. True hierarchy is only complete when only the currently selected item is emphasized and the rest visually recede.

**Why**: When all items are equally emphasized, the current state is impossible to identify.

**Anti-pattern**: Every category at the same emphasis level, so the selected item cannot be distinguished.

---

### [HIE-STATE-002] Differentiate parent-child hierarchy in UI
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Selection state & hierarchy expression

**Principle**: Selection elements in a hierarchical relationship (parent-child, upper-lower) must be visually distinguished through size, color, or placement. Using the same design to represent different hierarchies makes the structure hard for users to understand.

**Why**: When identically styled buttons represent different hierarchies, users perceive the two as belonging to the same level.

**Anti-pattern**: Province/city buttons and district/city buttons sharing the same design, making the upper-lower relationship impossible to discern.

---

### [HIE-STATE-003] Distinguish action hierarchy inside input areas
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Selection state & hierarchy expression

**Principle**: Vary the visual hierarchy (size, color, position) of multiple action icons within a chat input field by their importance and usage frequency. Without hierarchy, users cannot tell which feature matters most.

**Why**: Icons grouped identically feel like they are simply listed without any priority.

**Anti-pattern**: Bundling file attachment, voice, and AI icons at the same hierarchy, making it impossible to tell which is the primary feature.

---

### [HIE-STATE-004] Never emphasize equivalent items arbitrarily
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Selection state & hierarchy expression

**Principle**: Items with equivalent roles must receive identical visual treatment. Emphasizing a specific item requires a clear reason and a consistent pattern. When importance differs between items, separators (a dot, a line) alone are enough to distinguish them.

**Why**: Emphasizing just one item among equivalents distorts hierarchy and breaks consistency.

**Anti-pattern**: Bolding only one of six equivalent items, leaving the reason for emphasis ambiguous.

---

### [HIE-STATE-005] Tune the strong-weak ratio within elements
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Selection state & hierarchy expression

**Principle**: Within a single area, text weight, stroke intensity, icon size, and card element volume must balance with one another. Treat elements that are set once and rarely changed at low visual intensity so they do not disrupt the page's main flow.

**Why**: When strong-weak relationships between elements are off, the entire area feels either too heavy or too thin.

**Anti-pattern**: Strong text combined with heavy strokes and tiny icons, throwing the entire area out of balance.

---

### [HIE-STATE-006] Prioritize information by content type
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Selection state & hierarchy expression

**Principle**: Set the information hierarchy to match the section type (community, news, gallery, etc.). Community sections must prioritize text, while galleries must prioritize images.

**Why**: The information users most want differs from one content type to another.

**Anti-pattern**: Thumbnails laid out larger than posts in a community section, making it hard to read the post content.

---

### [HIE-STATE-007] Order content above controls
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Selection state & hierarchy expression

**Principle**: Place content above and operational controls (toggles, etc.) below or in an appropriately grouped position to make information hierarchy clear.

**Why**: When controls come before content, the control is shown without context for what it operates, causing confusion.

**Anti-pattern**: A toggle placed at the top with descriptive text below, forcing users to read the content before they can understand the control.

---

## Usage-frequency-based emphasis design (3 canonical)

### [HIE-USAGE-001] Match emphasis level to usage frequency
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Usage-frequency-based emphasis design

**Principle**: The visual intensity of buttons and UI elements must be proportional to the feature's usage frequency and importance. Lower the emphasis on infrequently used features (card change, category addition, etc.) and make them accessible only when needed.

**Why**: Always emphasizing elements that rarely change after initial setup disrupts the actually important flow.

**Anti-pattern**: A 'register card' UI emphasized as strongly as the payment button, so an infrequently used feature constantly steals attention.

---

### [HIE-USAGE-002] Hierarchy login paths by actual usage
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Usage-frequency-based emphasis design

**Principle**: On login screens, give a stronger visual hierarchy to the primary actions actually used most often (such as social login), and treat secondary actions visually weaker.

**Why**: When the hierarchy runs counter to actual usage patterns, friction arises for users.

**Anti-pattern**: A standard email login button emphasized over social login, pushing the more frequently used path visually backward.

---

### [HIE-USAGE-003] Clearly distinguish multi-action hierarchy
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Usage-frequency-based emphasis design

**Principle**: When multiple actions coexist on a screen, visually emphasize the core action to clarify hierarchy. Vary size, color, and position of multiple icons within input areas according to feature importance and usage frequency.

**Why**: Without an established hierarchy, users cannot tell what matters.

**Anti-pattern**: Three icons grouped equally with no hierarchy at all, making it impossible to tell which one matters.

---

## Weakening dividers, backgrounds & effects (3 canonical)

### [HIE-LINE-001] Keep dividers weaker than content
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Weakening dividers, backgrounds & effects

**Principle**: When dividers and borders are treated lightly, attention naturally concentrates on the content. Lines must recede like background for the content to come forward. The correct direction is to subdue the lines and elevate the text.

**Why**: Strong dividers create an inversion in which the structure itself registers before the content.

**Anti-pattern**: White dividers on a dashboard so strong that the lines register before the text.

---

### [HIE-LINE-002] Remove unnecessary visuals from settings pages
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Weakening dividers, backgrounds & effects

**Principle**: Express hierarchy on settings pages through font emphasis alone (bold/regular, etc.), and remove unnecessary section dividers or background fills to keep things simple.

**Why**: Settings pages should be simple, yet unnecessary visual elements raise their complexity.

**Anti-pattern**: Overusing meaningless section dividers and background fills on a settings page without applying any font emphasis.

---

### [HIE-LINE-003] Tune font hierarchy and dividers together
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Weakening dividers, backgrounds & effects

**Principle**: If text hierarchy (size, weight, color contrast) is not sorted out, even strong dividers will not save readability. Tune hierarchy and dividers together, and design the visual force of lines and text as inversely proportional.

**Why**: Even with strong lines, an absent text hierarchy makes content hard to grasp.

**Anti-pattern**: Heavy dividers paired with no text emphasis, with the two factors combining to double the visual complexity.

---

## Readability & visual hierarchy (2 canonical)

### [HIE-READ-001] Readability is the top condition of design
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Readability & visual hierarchy

**Principle**: The most basic condition of design is that information be visible. No matter how beautiful the typography and layout, without readability they have no meaning. Design is not about decoration; it is about presenting information effectively.

**Why**: Allowing users to read and understand information is design's purpose. Visual flourish is a concern only after readability.

**Anti-pattern**: Graphics meticulously crafted while text hierarchy is absent, or focusing on decoration without securing readability.

---

### [HIE-READ-002] Structurally guarantee text readability over images
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Readability & visual hierarchy

**Principle**: Apply a gradient dim or text shadow to text and icons placed over video or images so they remain legible even on bright backgrounds. A structure that only works well on certain images is unacceptable.

**Why**: Even when readable over dark images, legibility disappears once a bright image is loaded. Readability must be guaranteed structurally.

**Anti-pattern**: Readability that works because the current image is dark, but completely disappears when a bright image is uploaded.

---

## Banner hierarchy design (2 canonical)

### [HIE-BNR-001] Define banner text importance first
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Banner hierarchy design

**Principle**: Lay out text by first defining the order of importance, then deciding size, weight, and position based on that order—never by feel. In banners, the logo is the lowest priority and the core benefit or service content must be emphasized most.

**Why**: Layouts driven by feel cannot guarantee hierarchy or readability.

**Anti-pattern**: Laying out by feel ends with the logo being the largest while the benefit text is small.

---

### [HIE-BNR-002] Subdivide banner hierarchy and ensure readability
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Banner hierarchy design

**Principle**: A banner's text hierarchy must be subdivided not only at the overall stages (logo-title-sub) but also one or two more times within the title itself to clarify visual hierarchy. Readability is the top priority in banner design—text must be the most visible element, ahead of graphics.

**Why**: With only the major stages and no internal subdivision, importance differences within the title fail to come across.

**Anti-pattern**: A three-tier hierarchy with no further hierarchy inside the title, burying the core message.

---

## Emphasis priority (1 canonical)

### [HIER-EMP-001] Distinguish main vs. sub clearly
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Emphasis priority

**Principle**: Visually distinguish which objects are main and which are sub.

**Why**: When everything appears equal in rank, the core cannot be identified and the message blurs.

**Anti-pattern**: A heart sits in the main slot while the actual main object is elsewhere, throwing the priority off.

---
