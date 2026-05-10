# Spacing (UI)

Whitespace, gap, padding, margin rules

- **Total canonical rules**: 65
- **Sub-categories**: 12

---

## Contents
- Component inner spacing — 15 canonical
- Insufficient spacing — 6 canonical
- Miscellaneous — 12 canonical
- Grouping spacing — 4 canonical
- Excessive spacing — 4 canonical
- Content horizontal margin — 4 canonical
- Design process — 5 canonical
- Weight and density balance — 4 canonical
- Spacing system and consistency — 4 canonical
- Section spacing — 3 canonical
- Variable length and flexibility — 2 canonical
- Concept and whitespace — 2 canonical

---

## Component inner spacing (15 canonical)

### [SPACE-INNER-001] Card inner padding is independent of content length
- **Platform**: Mobile
- **Frequency weight**: 4
- **Sub-category**: Component inner spacing

**Principle**: Apply fixed padding values to card interiors regardless of content length.

**Why**: Padding that varies with content length destroys visual consistency.

**Anti-pattern**: Cards with short text have generous padding while long ones feel cramped.

---

### [SPACE-INNER-002] Never let text touch container edges
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: Always give text inside a container horizontal padding. Text touching the boundary feels cramped and unfinished.

**Why**: Inner padding gives content room to breathe.

**Anti-pattern**: Card text runs straight into the border.

---

### [SPACE-INNER-003] Give chips, tags, and badges enough vertical padding
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: Inline components like chips, tags, and badges need sufficient vertical inner padding between text and edge so they read as components.

**Why**: Without padding, users cannot tell whether they are looking at text or a component.

**Anti-pattern**: A chip with zero vertical padding collides with adjacent text.

---

### [SPACE-INNER-004] Use 16px button padding on all sides
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: Set button horizontal and vertical padding to at least 16px to secure both an adequate touch area and visual balance.

**Why**: It is the industry standard; Apple and Material guidelines both recommend similar values.

**Anti-pattern**: An 8px button padding feels cramped and is hard to tap.

---

### [SPACE-INNER-005] Account for the icon's bounding box when calculating button margin
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: When a button contains both text and an icon, calculate the icon-side margin using the icon's frame (including its built-in padding) to achieve visual balance.

**Why**: Icons carry their own guide padding, so applying identical margins on both sides creates imbalance.

**Anti-pattern**: Applying the same 16px margin on both the text side and the icon side.

---

### [SPACE-INNER-006] Give search bars and input fields generous inner padding
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: Provide ample horizontal inner padding inside input fields such as search bars so they feel spacious and comfortable to type into.

**Why**: The act of typing should be made as frictionless as possible.

**Anti-pattern**: A 4px horizontal padding inside a search bar feels suffocating.

---

### [SPACE-INNER-007] Reserve roughly 16px of trailing margin in input fields
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: Always reserve sufficient trailing margin (around 16px) inside input fields to accommodate the longest possible text entry.

**Why**: Without a buffer at the end of the input, typed text gets clipped.

**Anti-pattern**: Zero right margin makes typed text run flush against the edge.

---

### [SPACE-INNER-008] Center icons in circular containers with equal padding on all four sides
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: Pictograms inside circular containers (such as icon badges) need equal padding at the 12, 3, 6, and 9 o'clock positions to feel visually stable.

**Why**: If padding is tight on one side, the icon looks tilted or off-center.

**Anti-pattern**: A plus icon fills the circle with zero padding on all four sides.

---

### [SPACE-INNER-009] Measure icon margins from the bounding box, not the pictogram
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: When defining margin or padding rules for an icon component, base them on the icon's bounding box rather than the pictogram's visible edge.

**Why**: An icon's visual area is not the same as its actual bounding box.

**Anti-pattern**: Measuring a 20px margin from the edge of the pictogram, which then disagrees with the icon's official guide area.

---

### [SPACE-INNER-010] Title component bottom spacing must not depend on body presence
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: A title component should have bottom spacing measured from the title itself, and never have a structure where that spacing changes based on whether body text exists.

**Why**: If overall height shifts depending on whether body text is present, the system becomes unstable.

**Anti-pattern**: A title-plus-body component changes its overall height depending on whether the body is filled in.

---

### [SPACE-INNER-011] Keep GNB padding tight and rely on hover to compensate
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: In space-constrained areas like the global nav bar, use tight padding (around 12px) and compensate for the smaller targets with hover affordances.

**Why**: The GNB is a supporting region and should not eat into the content area.

**Anti-pattern**: A 24px GNB inner padding lets the nav bar overpower the page.

---

### [SPACE-INNER-012] Unify padding across selects and inputs
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Component inner spacing

**Principle**: Standardize inner padding for every input and select component within a form using a single consistent rule.

**Why**: Forms are systems; consistency builds user trust.

**Anti-pattern**: Inputs use 12px while selects use 16px, creating an awkward mismatch.

---

### [SPACE-INNER-013] Match button height to content density
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: Set button height to match the density of the content and overall layout. Premium-feeling designs call for thinner, restrained buttons.

**Why**: A 70px button is generally excessive.

**Anti-pattern**: A luxury brand site using chunky 70px-tall buttons.

---

### [SPACE-INNER-014] Match button and input heights
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: Components that may sit side by side (buttons and inputs) should share the same height so no combination ever produces a broken layout.

**Why**: Components of different heights sitting next to each other break the visual line.

**Anti-pattern**: A 40px search input next to a 48px button creates a misaligned baseline.

---

### [SPACE-INNER-015] Use horizontal margin to keep tab bar items cohesive
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Component inner spacing

**Principle**: Apply at least a minimum horizontal margin inside the tab bar so the icons read as a cohesive group.

**Why**: Spreading icons all the way to the screen edges without margin looks awkward.

**Anti-pattern**: Bottom tab bar icons stretched out to the very edges of the screen.

---

## Insufficient spacing (6 canonical)

### [SPACE-LACK-001] Adjacent elements need spacing to avoid collision
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Insufficient spacing

**Principle**: Always secure sufficient spacing between adjacent elements to prevent visual collisions.

**Why**: Without spacing, elements appear to overlap and visual hierarchy collapses.

**Anti-pattern**: Two pieces of text running edge to edge so they cannot be distinguished.

---

### [SPACE-LACK-002] Touching corners make the layout feel cramped
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Insufficient spacing

**Principle**: Without enough gap between adjacent areas, their corners appear to touch and the entire layout feels narrow and packed.

**Why**: A sense of space equals a sense of openness.

**Anti-pattern**: Sections pressed corner to corner blur into a single undifferentiated mass.

---

### [SPACE-LACK-003] Tight spacing reads as cramped, busy, and heavy
- **Platform**: Mobile/PC
- **Frequency weight**: 14
- **Sub-category**: Insufficient spacing

**Principle**: Spacing that is too tight makes a design feel suffocating and pushes information density to a busy, heavy place.

**Why**: Whitespace is visual breath; without it the design feels stifling.

**Anti-pattern**: An information-dense screen with only 8px of spacing throughout.

---

### [SPACE-LACK-004] Insufficient between-group spacing makes groups disappear
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Insufficient spacing

**Principle**: Spacing between different groups must be larger than spacing within a group so that visual grouping reads clearly.

**Why**: When inner and outer group spacing match, the grouping becomes invisible.

**Anti-pattern**: The gap between payment method cards equals the padding inside each card.

---

### [SPACE-LACK-005] Equal top and bottom margins make a button feel adrift
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Insufficient spacing

**Principle**: If a button has identical top and bottom margins, its section ownership becomes unclear and it appears to float. It must be visually bound to its related content.

**Why**: Directional spacing is what creates a sense of belonging.

**Anti-pattern**: A button with 32px margin both above and below leaves its grouping ambiguous.

---

### [SPACE-LACK-006] Title-to-body gap should be smaller than the gap above the title
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Insufficient spacing

**Principle**: A title needs less spacing below (toward its body) than above (toward the previous section) so it visually pairs with the body and the section hierarchy survives.

**Why**: Title and body form one group.

**Anti-pattern**: Identical spacing above and below the title leaves it floating in space.

---

## Miscellaneous (12 canonical)

### [SPACE-MISC-001] Design spacing for touch comfort, not just visuals
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Miscellaneous

**Principle**: Treat spacing as more than empty area; deliberately design it to secure comfortable touch targets and accommodate future scale.

**Why**: Whitespace serves both visual rhythm and interaction.

**Anti-pattern**: Treating spacing as nothing more than visual breathing room.

---

### [SPACE-MISC-002] Drop dividers once hierarchy is already established
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: If hierarchy is already conveyed through font size or color, omit the divider line. Unnecessary rules are visual noise.

**Why**: Dividers should be a last resort.

**Anti-pattern**: Adding another divider line next to a price that is already visually emphasized.

---

### [SPACE-MISC-003] Space short-form video action icons more generously than feels natural
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Spacing between the right-side action icons on short-form video screens (Shorts, Reels) should be wider than instinct suggests; benchmark density against shipping apps.

**Why**: Designer intuition can diverge from the actual industry standard.

**Anti-pattern**: Short-form action icons spaced tightly based on gut feel.

---

### [SPACE-MISC-004] Match a card's inner and outer spacing (e.g., 32px)
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Standardizing the spacing inside and outside a card component on the same value (such as 32px) yields a more consistent layout.

**Why**: Matching inner and outer spacing produces an orderly impression.

**Anti-pattern**: 16px inside the card and 32px outside it creates visual imbalance.

---

### [SPACE-MISC-005] Keep GNB horizontal margins consistent with the content area
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: The horizontal margins of the GNB must stay consistent with the content area; excessive margin makes the design feel meager.

**Why**: The GNB and content must share the same alignment axis.

**Anti-pattern**: 80px GNB margin against 24px content margin produces a disjointed feel.

---

### [SPACE-MISC-006] Tight spacing between list items hurts readability
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: When information lists lack spacing between items, readability suffers; give them enough gap so each item is perceived individually.

**Why**: Item separation is readability.

**Anti-pattern**: Profile detail rows packed together with no breathing room.

---

### [SPACE-MISC-007] The stronger the image, the more whitespace around it
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Miscellaneous

**Principle**: The more visually intense an image is, the more generous its surrounding whitespace must be in order to maintain balance and a sense of ease.

**Why**: Whitespace is what disperses an image's visual weight.

**Anti-pattern**: Pairing a powerful image with text using only a thin margin between them.

---

### [SPACE-MISC-008] Make dropdown items feel spacious
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Items inside dropdowns and layered menus should be sized generously so the menu feels open and easy to read.

**Why**: Cramped sizing reads as suffocating.

**Anti-pattern**: 24px-tall dropdown items leave a tightly packed impression.

---

### [SPACE-MISC-009] Give buttons generous breathing room
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Secure enough padding inside the button and enough margin around it. Generous spacing makes buttons stand out and easier to operate.

**Why**: Buttons trigger action; both perception and interaction matter.

**Anti-pattern**: Almost no whitespace around the button.

---

### [SPACE-MISC-010] Give chat input fields enough height
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Chat and text input fields need appropriate height and width so users can clearly see what they are typing.

**Why**: A cramped input area degrades usability.

**Anti-pattern**: A chat input field that is only one line tall.

---

### [SPACE-MISC-011] Keep GNB spacing in the 12-16px sweet spot
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Adjust horizontal spacing inside the GNB based on screen size and the number of items; 12 to 16px usually strikes the right balance.

**Why**: The GNB is a small region, so its spacing must not be overdone.

**Anti-pattern**: 24px horizontal spacing inside the GNB is excessive.

---

### [SPACE-MISC-012] Keep margins on the same axis consistent within a screen
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Within a single screen, spacing along the same axis (such as horizontal padding) should be unified to one value; mixing values section by section makes the layout look disorderly.

**Why**: Uneven margins read as disorder.

**Anti-pattern**: A single page mixing horizontal margins of 12, 24, and 16px.

---

## Grouping spacing (4 canonical)

### [SPACE-GROUP-001] In-group spacing must be tighter than between-group spacing (proximity principle)
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Grouping spacing

**Principle**: Keep spacing between related elements (inside a group) tight and spacing between different groups wide. The contrast in spacing is what visualizes the grouping.

**Why**: The principle of proximity says nearby items read as a group. Equal spacing flattens the hierarchy.

**Anti-pattern**: Title-to-body spacing equals body-to-next-section spacing, leaving the title visually adrift.

---

### [SPACE-GROUP-002] Whitespace alone can express grouping
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Grouping spacing

**Principle**: Groups can be communicated clearly with whitespace alone, without dividers or boxes. The fewer lines, the cleaner the result.

**Why**: Lines are visual noise; whitespace is a more elegant grouping tool.

**Anti-pattern**: Reaching for a divider line every time you need to separate a group.

---

### [SPACE-GROUP-003] Uniform spacing flattens the design
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Grouping spacing

**Principle**: Uniform spacing hides information grouping; differentiated spacing is essential.

**Why**: Equal spacing means no hierarchy.

**Anti-pattern**: All spacing standardized at 16px so no grouping is discernible.

---

### [SPACE-GROUP-004] Pair icon and label tightly via proximity
- **Platform**: Mobile
- **Frequency weight**: 5
- **Sub-category**: Grouping spacing

**Principle**: Place an icon and its label close enough together that they read as a single visual unit (the principle of proximity).

**Why**: When the icon and label drift apart, users fail to perceive the association.

**Anti-pattern**: An 11px gap between a tab bar icon and its label makes them look separated.

---

## Excessive spacing (4 canonical)

### [SPACE-EXCESS-001] Spacing that is too wide reads as a line
- **Platform**: PC
- **Frequency weight**: 4
- **Sub-category**: Excessive spacing

**Principle**: Excessively wide whitespace starts to read as a visual line. Keep spacing strong enough to define relationships between elements yet quiet enough that it does not draw attention to itself.

**Why**: Whitespace that overreaches its role becomes noise.

**Anti-pattern**: 30px of spacing carving a visible line across the entire page.

---

### [SPACE-EXCESS-002] Excessive spacing severs groups
- **Platform**: Mobile
- **Frequency weight**: 4
- **Sub-category**: Excessive spacing

**Principle**: Whitespace gives breathing room, but too much makes elements feel disconnected. On information-dense screens, keep spacing tight so the flow of information remains continuous.

**Why**: Excessive whitespace produces a separating effect.

**Anti-pattern**: 20px between card items prevents them from reading as one group.

---

### [SPACE-EXCESS-003] Oversized inner padding makes content float
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Excessive spacing

**Principle**: When inner container padding becomes excessive, the content appears to float inside an empty void.

**Why**: Spacing should support content rather than abandon it.

**Anti-pattern**: 80px of inner padding inside a card leaves a small piece of text floating like a pupil in an iris.

---

### [SPACE-EXCESS-004] Excessive grid gaps fragment the layout
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Excessive spacing

**Principle**: If grid items in a layout look fragmented, reduce the margin between them and tie them together more tightly to recover a sense of unity.

**Why**: For the overall layout to read as one unit, the gaps must be controlled.

**Anti-pattern**: 24px gaps between game grid items leave each one feeling isolated.

---

## Content horizontal margin (4 canonical)

### [SPACE-EDGE-001] Use 16-20px horizontal margin on mobile
- **Platform**: Mobile
- **Frequency weight**: 5
- **Sub-category**: Content horizontal margin

**Principle**: Mobile UI content margins should typically follow a 16-20px standard. Anything below 12px feels suffocating.

**Why**: It is the standard derived from smartphone screen width and the size of a fingertip.

**Anti-pattern**: 12px horizontal margin makes content feel jammed against the screen edges.

---

### [SPACE-EDGE-002] Make PC margins wider than mobile (20px+)
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Content horizontal margin

**Principle**: On PC, secure more generous spacing between icons and elements than on mobile (20px or more). Tight elements on a wide screen look cramped.

**Why**: On PC the field of view is wider, so the same physical distance feels closer.

**Anti-pattern**: Applying the same 12px gap on PC that you would use on mobile.

---

### [SPACE-EDGE-003] 36px or more is overkill
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Content horizontal margin

**Principle**: Mobile horizontal margin as wide as 36px shrinks the content area unnecessarily; around 24px is a reasonable upper bound.

**Why**: Whitespace is a problem when too narrow and when too wide; balance is everything.

**Anti-pattern**: 36px horizontal mobile margin leaves too little room for content.

---

### [SPACE-EDGE-004] Do not force one universal margin across every screen
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Content horizontal margin

**Principle**: Do not apply the default 16px margin to every screen identically; adjust it flexibly based on screen type and content character.

**Why**: Dense content and airy content cannot share the same margin appropriately.

**Anti-pattern**: Forcing a 16px horizontal margin even on an image-packed gallery.

---

## Design process (5 canonical)

### [SPACE-PROCESS-001] Start spacing wide, then tighten
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Design process

**Principle**: Beginning the design with generous spacing and tightening it later allows more flexible adjustment.

**Why**: It is easy to tighten wide spacing but hard to widen tight spacing.

**Anti-pattern**: Starting tight from the beginning makes later adjustments difficult.

---

### [SPACE-PROCESS-002] Whitespace is a design element, not a void to fill
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Design process

**Principle**: Whitespace is part of the design. Resist the impulse to fill every empty area; whitespace is what focuses attention on the content and clarifies grouping.

**Why**: It is a common mistake among less experienced web designers.

**Anti-pattern**: Reaching to fill any empty space the moment you notice it.

---

### [SPACE-PROCESS-003] Details determine final quality
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Design process

**Principle**: Design quality is decided by the accumulation of small details such as grouping, spacing, and font size; tend to each one carefully.

**Why**: The before-and-after difference comes down to details.

**Anti-pattern**: Caring only about the large structure while ignoring small spacing.

---

### [SPACE-PROCESS-004] Review designs at the standard viewport
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Design process

**Principle**: Evaluate the size of design elements against the standard viewport; an inflated overall canvas distorts your sense of how big each element actually is.

**Why**: On an oversized canvas, elements that look small are in fact more than large enough.

**Anti-pattern**: Sizing every element large on a 1920px canvas, only to find them gigantic when scaled down to mobile.

---

### [SPACE-PROCESS-005] There is no need to fill it all; empty on purpose
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Design process

**Principle**: There is no obligation to fill the content area entirely. Whitespace left empty on purpose lets the design breathe and produces an orderly impression.

**Why**: Emptiness is itself an active design choice.

**Anti-pattern**: The reflexive habit of filling whitespace whenever you see it.

---

## Weight and density balance (4 canonical)

### [SPACE-DENSITY-001] The stronger the tone, the wider the whitespace
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Weight and density balance

**Principle**: Strong-colored elements need ample whitespace between them; the stronger the tone, the more you should widen spacing to reduce visual noise.

**Why**: Strong elements plus narrow whitespace equals visual bombardment.

**Anti-pattern**: Saturated thumbnails separated by only 8px of spacing.

---

### [SPACE-DENSITY-002] Balance design weight against density
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Weight and density balance

**Principle**: A design's weight and density must be kept in balance; a strong, packed combination presses down on the user.

**Why**: When weight is high, density must come down to maintain balance.

**Anti-pattern**: Strong color paired with packed information overwhelms the user.

---

### [SPACE-DENSITY-003] If it feels cute and cramped, widen the whitespace
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Weight and density balance

**Principle**: When a design starts looking cutesy and cramped, the first move is to widen whitespace and bump up font size; an open, airy feel serves information delivery better.

**Why**: It reduces the user's cognitive load.

**Anti-pattern**: Trying to preserve a cramped design as-is.

---

### [SPACE-DENSITY-004] Larger elements need wider whitespace
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Weight and density balance

**Principle**: The bulkier the UI element, the more surrounding whitespace it needs; with enough whitespace, even large, heavy elements feel light.

**Why**: Whitespace offsets visual weight.

**Anti-pattern**: Large cards stuck together without margin produce an oppressively heavy feel.

---

## Spacing system and consistency (4 canonical)

### [SPACE-SYS-001] Manage spacing with a consistent system (8pt grid, etc.)
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Spacing system and consistency

**Principle**: Manage whitespace with a consistent system based on a common unit such as 8pt or 4pt; arbitrary values (like 71 or 105) destroy consistency.

**Why**: A predictable system inspires trust; arbitrary values are noise.

**Anti-pattern**: Spacing scattered across 28px, 17px, 20px, 71px, and 105px with no rhyme or reason.

---

### [SPACE-SYS-002] Unify spacing on the same axis within a single screen
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Spacing system and consistency

**Principle**: Within a single screen, whitespace of the same nature (horizontal margin, top padding, etc.) must use the same value; inconsistency destroys the sense of alignment.

**Why**: A sense of alignment is the bedrock of design.

**Anti-pattern**: Mixing 32px and 24px horizontal margins within a single screen.

---

### [SPACE-SYS-003] Even a 1-2px difference separates polished from sloppy
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Spacing system and consistency

**Principle**: Horizontal margins must match exactly; even a 1 or 2 pixel difference can decide the fine quality of a design.

**Why**: Details are completeness.

**Anti-pattern**: 8px on the left and 10px on the right - subtle, but visibly off.

---

### [SPACE-SYS-004] Breaking the shared spacing system collapses the whole system
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Spacing system and consistency

**Principle**: Margin and padding values must follow the shared spacing system across the entire site or app; using different values on a single screen breaks the system as a whole.

**Why**: Break it in one place and it falls like dominoes.

**Anti-pattern**: Using a 50px margin only on one specific page.

---

## Section spacing (3 canonical)

### [SPACE-SECTION-001] Differentiate section spacing for rhythm
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Section spacing

**Principle**: Do not give every section the same gap; reserve more whitespace before and after key sections to create rhythm.

**Why**: Whitespace is a tool for emphasis; uniform spacing flattens everything.

**Anti-pattern**: An 80px gap standardized between every single section.

---

### [SPACE-SECTION-002] Empty whitespace boldly
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Section spacing

**Principle**: Do not be afraid of whitespace; leave it boldly. Whitespace is not empty area but a visual element that lets content show more clearly.

**Why**: A fully packed design conveys suffocation.

**Anti-pattern**: Trying to fill whitespace simply because it looks empty.

---

### [SPACE-SECTION-003] Give enough bottom margin where a section ends
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Section spacing

**Principle**: At the end of a section, provide enough bottom margin to clearly define the boundary with the next section.

**Why**: Visual separation at section endings is what creates content hierarchy.

**Anti-pattern**: Zero margin at the end of a section makes it run straight into the next one.

---

## Variable length and flexibility (2 canonical)

### [SPACE-FLEX-001] Reserve enough space for variable-length text
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Variable length and flexibility

**Principle**: Design areas that hold variable-length text (prices, product names, etc.) with enough whitespace and a flexible structure so the layout never breaks no matter how long the text grows.

**Why**: Text length is variable; the design must be robust.

**Anti-pattern**: Allocating exactly the right width for the price - which then breaks when the text grows.

---

### [SPACE-FLEX-002] Set spacing for repeating patterns based on the full arrangement
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Variable length and flexibility

**Principle**: When designing layouts of repeating items, set whitespace based on the entire repeated arrangement rather than a single item; only when one item feels generous will the full pattern feel comfortable.

**Why**: What looks fine for one may not look fine for five.

**Anti-pattern**: Spacing that feels right with a single card looks tight when five are arranged together.

---

## Concept and whitespace (2 canonical)

### [SPACE-CONCEPT-001] The stronger the concept, the stricter the spacing
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Concept and whitespace

**Principle**: The stronger a design's concept, the more strictly you must manage whitespace and alignment; the louder the concept, the more glaring any weakness in the fundamentals.

**Why**: Concept is surface; fundamentals are skeleton.

**Anti-pattern**: Ignoring spacing and alignment in a design with a strong line-driven concept.

---

### [SPACE-CONCEPT-002] Refined designs deserve deliberately bold whitespace
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Concept and whitespace

**Principle**: When the goal is a line-driven concept or a refined feel, widen whitespace deliberately and boldly; ample whitespace is the key element that makes the concept come alive.

**Why**: Whitespace is the tool of refinement.

**Anti-pattern**: Pursuing a sophisticated concept while keeping whitespace tight - the result feels suffocating.

---
