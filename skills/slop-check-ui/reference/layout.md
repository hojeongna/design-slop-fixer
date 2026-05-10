# Layout (UI)

Grid, alignment, section composition, responsive layout rules

- **Total canonical rules**: 53
- **Sub-categories**: 15

---

## Contents
- Grid & Alignment — 3 canonical
- Cards & Containers — 6 canonical
- Divider line principles — 4 canonical
- GNB (Global Navigation Bar) — 5 canonical
- Tab bar & Mobile baseline — 2 canonical
- Eye flow & Information path — 3 canonical
- Responsive & Breakpoints — 3 canonical
- Section separation & Division — 4 canonical
- Image & Thumbnail placement — 4 canonical
- Information density & Whitespace — 3 canonical
- Element size & Balance — 4 canonical
- Layout rhythm & Pattern consistency — 4 canonical
- Banner & Hero layout — 2 canonical
- Choosing horizontal vs. vertical arrangement — 3 canonical
- Element position & Affiliation — 3 canonical

---

## Grid & Alignment (3 canonical)

_Grid-based layout placement and consistent alignment between elements. The habit of designing with an invisible grid in mind._

### [LAYOUT-GRID-001] Always use a grid system
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Grid & Alignment

**Principle**: Align layouts to a structured grid system (such as a 12-column grid) instead of arbitrary pixel values. Without a grid, alignment and spacing become inconsistent and the design looks unpolished. For complex layouts, always lay down the grid and guidelines first, then design on top of them.

**Why**: The grid can live entirely in the designer's head. Aligning elements to an invisible grid is what makes a design feel orderly. The single most important first principle of clean design is to design while honoring the grid.

**Anti-pattern**: Layouts where elements are placed at arbitrary pixel values, resulting in inconsistent spacing and alignment.

---

### [LAYOUT-GRID-002] Keep alignment consistent
- **Platform**: Mobile/PC
- **Frequency weight**: 11
- **Sub-category**: Grid & Alignment

**Principle**: Elements placed on the same axis (left, right, or center) must share the same alignment value to feel visually stable. Mixing text alignment directions within a single screen makes the layout look unanchored and visually confusing. Text elements inside the same content block should share a common starting line (vertical alignment baseline). Default to left alignment for the same type of content and keep it consistent.

**Why**: Misalignment is the most basic design problem and the most obvious flaw to the eye. Half-hearted alignment is worse than no alignment at all. Billboard text feels more stable when left-aligned, and center alignment should only be used when the element is simple.

**Anti-pattern**: A layout where each section mixes left, right, and center alignment with no consistency.

---

### [LAYOUT-GRID-003] Align elements precisely inside containers
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Grid & Alignment

**Principle**: Elements inside containers (text inside buttons, icons inside frames) must be exactly centered both vertically and horizontally. Odd-pixel icon sizes can throw off alignment, so manage icons in even pixel sizes. Set clear anchor points for cards (e.g., title top-left, icon bottom-right) to keep layouts consistent. Center-aligning titles inside popups and dropdowns gives an open and orderly feel.

**Why**: If elements inside a button or frame are not centered, perceived quality drops immediately. For a GNB title, when the number of icons on each side is asymmetric, the mathematical center and the optical center can differ.

**Anti-pattern**: Button text that is mathematically centered via auto-layout but looks visually off-center.

---

## Cards & Containers (6 canonical)

_Principles for using card layouts. Minimize nested cards, choose between flat placement vs. cards, remove unnecessary containers, and clarify list item boundaries._

### [LAYOUT-CARD-001] Minimize nested cards
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Cards & Containers

**Principle**: Avoid nesting a card inside another card. Once an area is already wrapped in a container, do not wrap it again in another card. Nesting cards inside cards increases visual complexity exponentially and shrinks usable space.

**Why**: Double nesting forces multiple layers of margin, which eats away usable design space. At the same hierarchical level, a single container is enough.

**Anti-pattern**: A triple-nested structure where products are wrapped in a card, placed inside a white card, which sits inside a gray background card.

---

### [LAYOUT-CARD-002] Decide between cards vs. flat placement
- **Platform**: Mobile/PC
- **Frequency weight**: 13
- **Sub-category**: Cards & Containers

**Principle**: Information does not always need to be wrapped in a card. A white background with well-considered whitespace can deliver enough readability and grouping. To build an open, spacious layout without cards, whitespace must be the core strategy. Substituting it with background colors or column dividers produces the opposite effect.

**Why**: Before wrapping things in cards, practice designing hierarchy and whitespace on the bare background first; this leads to better card designs later. Self-contained elements feel lighter and cleaner when placed directly on the background.

**Anti-pattern**: Wrapping everything in cards just because there is a lot of information, resulting in a cramped and busy layout.

---

### [LAYOUT-CARD-003] Do not over-divide the inside of a card
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Cards & Containers

**Principle**: Card UIs should keep their inner elements grouped as a single block to preserve a sense of visual unity. Do not unnecessarily subdivide that group; when there are only a few items, listing them directly without inner boxes is cleaner. Merging thumbnails into the card itself is more space-efficient.

**Why**: Nested subdivisions destroy the sense of a unified block and waste space. Splitting many items into cards within a narrow area only increases complexity.

**Anti-pattern**: Already wrapped in a card, then further divided inside with another gray background block.

---

### [LAYOUT-CARD-004] Minimize unnecessary boxes and containers
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Cards & Containers

**Principle**: Unnecessary boxes (container borders or backgrounds) make the layout busy. Use boxes only when separation is truly required; if whitespace and alignment alone create the needed separation, remove the box. A simple line is often cleaner than a full box.

**Why**: Repeating the same card style across every section kills rhythm and feels redundant. Stuffing complex content into a narrow card only makes it more complex.

**Anti-pattern**: A layout where every section is wrapped in the same card style, making the whole page feel repetitive.

---

### [LAYOUT-CARD-005] Reveal the next card in a slider
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Cards & Containers

**Principle**: Slide-style cards should leave the next card slightly visible. Cutting it off entirely removes any cue to scroll further. Use horizontal sliders for secondary content rather than vertical scroll, so main content stays visible. For products, showing fewer items per screen with breathing room and letting users swipe is cleaner than packing many items at once.

**Why**: When a slider lets the next card peek through, users recognize there is more to see and feel motivated to explore.

**Anti-pattern**: A slider that crops cards flush to the edge, hiding the fact that more content exists.

---

### [LAYOUT-CARD-006] Make list item boundaries clear
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Cards & Containers

**Principle**: When listing multiple independent items, mark each item's boundary clearly using cards, dividers, or background color changes. Choose between cards, lines, or whitespace based on context; switching background color blocks is overkill for general lists outside of dashboards. For tables, give the header a background color but keep content cells on a plain white background for better readability.

**Why**: When search results from multiple sources are listed without separators, it is hard to tell which result belongs to which source. Without dividers, the start and end of each item is unclear, hurting readability.

**Anti-pattern**: A list where independent items run together with no separators, making it hard to tell where one item ends and the next begins.

---

## Divider line principles (4 canonical)

_Minimize divider use, keep them light and thin, and never combine multiple separation methods. Always first check whether whitespace alone is enough._

### [LAYOUT-LINE-001] Do not overuse dividers
- **Platform**: Mobile/PC
- **Frequency weight**: 25
- **Sub-category**: Divider line principles

**Principle**: Use divider lines only when truly needed; if grouping or whitespace already separates content well, omitting the line is cleaner. Overusing lines makes the design feel busy and heavy. When dividing a layout into two regions, a single central divider is enough.

**Why**: Dividers exist to support the content, so they must never be visually stronger than the content itself. In many cases whitespace and alignment alone provide enough separation. Every element added to a design should have a clear purpose.

**Anti-pattern**: A layout where dividers are placed between every item and every section, making the lines more prominent than the content.

---

### [LAYOUT-LINE-002] Keep dividers thin and light
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Divider line principles

**Principle**: When a divider is needed, keep it as thin and light as possible (1px, light gray). Omit the divider below the last list item for a cleaner look. Strokes should also be kept as soft as possible to keep the UI feeling light.

**Why**: Dividing sections with thick lines is an outdated style. White or pale gray lines provide more than enough separation, and the overall layout feels lighter.

**Anti-pattern**: Sections divided by overly dark, thick lines that make the whole layout feel heavy.

---

### [LAYOUT-LINE-003] Pick only one section separation method
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Divider line principles

**Principle**: Pick only one method to separate sections — line, background color, or card. Combining a line with a background color dilutes the intent and adds visual weight. The exception: long scrolling lists do require dividers. Because dividers imply grouping, use whitespace rather than lines to separate individual items — it sends a more accurate signal.

**Why**: Dividers are needed when there are many items and scrolling is required. But with only a few items, a background color or whitespace alone is enough.

**Anti-pattern**: A line-driven design that also uses background color on every section, doubling up on separation methods.

---

### [LAYOUT-LINE-004] Use gradient fade at scroll edges
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Divider line principles

**Principle**: At the edge of a horizontal scroll list, or below a floating element that sits above a scrolling area, apply a gradient fade. This hints that more content exists while finishing the area naturally.

**Why**: A gradient fade naturally solves the problem of fixed margins failing to accommodate variable content, which makes content appear abruptly cut off.

**Anti-pattern**: A horizontal scroll list whose edge is sharply cut off, or a floating button that overlaps the background content with no boundary, looking messy.

---

## GNB (Global Navigation Bar) (5 canonical)

_GNB height, logo/menu/icon placement structure, element size balance, and the single-row principle._

### [LAYOUT-GNB-001] Keep the GNB slim
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: GNB (Global Navigation Bar)

**Principle**: Keep the GNB no taller than necessary to maximize the visible content area. Desktop GNBs should be around 70px, and mobile should be even more restrained than PC. An oversized GNB squeezes the content area and feels heavy. Even on a 1920 desktop, the billboard height should be designed against the actual browser viewport (around 960px).

**Why**: The user's attention is on the content. A bulky GNB pushes the content down on every page, accumulating friction.

**Anti-pattern**: Setting the GNB height to 88px or more, or keeping the same GNB height on mobile as on PC.

---

### [LAYOUT-GNB-002] GNB structure: logo left, icons right
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: GNB (Global Navigation Bar)

**Principle**: The standard GNB structure is logo on the left, menu in the center, and icons on the right; the logo is conventionally left-aligned. Side navigation should hug the left edge to create a clean two-pane split between menu and main content. About 240px is enough for sidebar width. For fixed regions like the GNB, lock down the area (a guide box) first, then place elements inside — this keeps alignment consistent.

**Why**: A center-aligned logo, without a specific brand intent, can confuse users.

**Anti-pattern**: Centering the logo, or wrapping the left menu in a card so that it visually blends into the content.

---

### [LAYOUT-GNB-003] Balance the size of GNB elements
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: GNB (Global Navigation Bar)

**Principle**: The size and visual weight of GNB elements (logo, search, icons, profile) must stay in balance. The profile image and logo should not be larger than necessary. Place conditional buttons (e.g., Upgrade) at the far end so they do not affect the other elements. Group related elements on the right side of the header (icons, profile, buttons) and align them together.

**Why**: When elements on the right side of the header drift apart and do not read as a single group, the header looks untidy.

**Anti-pattern**: An oversized logo that leaves the GNB feeling empty, or a profile image so large that the user's face dominates the UI.

---

### [LAYOUT-GNB-004] Keep the GNB to a single row
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: GNB (Global Navigation Bar)

**Principle**: Keep the GNB to a single row whenever possible; space-hungry elements like a search bar can be replaced with an icon-plus-popover pattern. When elements with different roles (tab buttons and a search bar) coexist in the GNB, separate their visual roles clearly so they do not clash.

**Why**: A two-row GNB takes up too much of the top area and squeezes the content. When similar-shaped elements share the same area, visual collisions occur.

**Anti-pattern**: Splitting the GNB into two rows so the top area dominates the screen, or letting tabs and a search bar visually clash within the same GNB.

---

### [LAYOUT-GNB-005] Collapsible sidebar for dashboards
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: GNB (Global Navigation Bar)

**Principle**: Always design a collapse/expand affordance for sidebars in admin pages and dashboards. Place the logo in an independent region (such as the header) so it remains visible even when the sidebar is collapsed.

**Why**: A permanently fixed sidebar drastically shrinks the content area at narrow resolutions. A collapse/expand control is essential for both wide-screen usability and narrow-resolution support.

**Anti-pattern**: Putting the logo inside the sidebar with no collapse function, so collapsing the sidebar makes the logo disappear with it.

---

## Tab bar & Mobile baseline (2 canonical)

_Even distribution of the bottom tab bar on mobile, choosing a baseline device, and the requirement to verify on real devices._

### [LAYOUT-TAB-001] Divide the tab bar evenly
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Tab bar & Mobile baseline

**Principle**: Divide the bottom tab bar evenly across its horizontal space according to the number of tabs, and center each icon precisely within its slot. Balance the number of icons with the slot size so excessive empty space does not appear.

**Why**: The tab bar is the persistent UI users encounter most often. Uneven slots or sloppy icon placement directly translate into a basic quality issue.

**Anti-pattern**: A tab bar area that is too large for the number of tabs, or one whose slots are unevenly divided so the icons feel haphazard.

---

### [LAYOUT-TAB-002] Set a mobile baseline device and verify on real hardware
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Tab bar & Mobile baseline

**Principle**: Anchor the mobile design at 360–375px to make small (320px) screens easier to support. Always verify mobile designs on a real phone (mirroring or device preview) while you work.

**Why**: Going from 390px down to 280px is too big a gap for beginners to handle responsively. Elements that look fine in Figma can appear small or awkward on an actual device.

**Anti-pattern**: Finishing a design entirely in Figma without real-device verification and then finding the layout looks off on actual hardware.

---

## Eye flow & Information path (3 canonical)

_Avoid zigzag arrangements, remove elements that disrupt the eye flow, and design layouts with readability as the top priority._

### [LAYOUT-FLOW-001] Avoid zigzag layouts
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Eye flow & Information path

**Principle**: Zigzag content layouts seriously damage readability. Users naturally read horizontally, so a zigzag structure forces the eye to bend back and forth and makes the reading order hard to follow. Arrange information so it reads in a consistent direction (left-to-right, top-to-bottom).

**Why**: For sequential information, a vertical stack is the easiest to read. UX/UI layouts should follow an inverted pyramid (strongest first, then medium, then weakest) for better eye flow and readability.

**Anti-pattern**: A portfolio that zigzags projects across the page so the 1 → 2 → 3 reading order is hard to follow.

---

### [LAYOUT-FLOW-002] Remove elements that disrupt the eye flow
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Eye flow & Information path

**Principle**: Remove or relocate elements that interrupt the eye's flow through the layout. Readability peaks when information flows uninterrupted horizontally and vertically. Place the same kind of UI elements as one continuous visual group and do not let unrelated information cut in. Put the core information in the largest and most prominent central area.

**Why**: When a button cuts across text mid-read, or benefit information breaks between option buttons, users lose track of how the elements relate.

**Anti-pattern**: A card whose button sits next to the main text and breaks the reading flow, or a layout that forces the eye into a V-shape or diagonal jump.

---

### [LAYOUT-FLOW-003] Readability is the layout's yardstick
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Eye flow & Information path

**Principle**: Readability is the criterion for layout composition. Always judge against whether the user can understand the content comfortably and intuitively. When designing, lock down the composition (layout structure) first, then refine the details.

**Why**: When designing a complex information page, establish clear criteria — information priority, grouping logic, eye flow — before designing the overall layout logic.

**Anti-pattern**: Deciding the layout purely on visual instinct and sticking with a composition that is hard for users to read.

---

## Responsive & Breakpoints (3 canonical)

_Setting a max-width, defining breakpoints up front, and the strategy of designing PC first then scaling down to mobile._

### [LAYOUT-RESP-001] Set a max-width for content
- **Platform**: PC
- **Frequency weight**: 4
- **Sub-category**: Responsive & Breakpoints

**Principle**: Set a maximum breakpoint (max-width) for the layout; beyond that resolution, the content should stop growing and stay fixed. Absorb the extra resolution as left/right whitespace. Interactive elements like slider arrows must sit inside the content's max-width area.

**Why**: Without a max breakpoint, the layout expands indefinitely. You also need to verify that UI elements remain visible without clipping at the target minimum resolution.

**Anti-pattern**: A layout where content keeps spreading without limit as the screen grows beyond 1920px.

---

### [LAYOUT-RESP-002] Define responsive breakpoints up front
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Responsive & Breakpoints

**Principle**: Before starting responsive design, define how text, whitespace, and component sizes change at each breakpoint. Build the PC version to a high level of polish first, then carry those decisions (colors, fonts, whitespace) down to mobile by scaling them. Keep the number of properties that change to a minimum.

**Why**: Designing with values shared across PC and mobile dramatically reduces mobile work. Responsive thinking pushes the layout structure toward simplicity.

**Anti-pattern**: Building PC and mobile separately with no shared breakpoint rules, doubling the design effort.

---

### [LAYOUT-RESP-003] Small-screen support and auto-layout
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Responsive & Breakpoints

**Principle**: Responsive support across screen sizes is mandatory. The first goal is to fit naturally without clipping or distortion. When building responsive components in Figma, configure auto-layout's Fill and Hug appropriately for the context. In a video feed, video content is typically filled to full width with no left/right margins.

**Why**: On a mobile grid, mismatched card heights break the balance, so design the layout with the height variations from different text lengths in mind.

**Anti-pattern**: Skipping responsive treatment even though images or text are squashed or clipped on a 320px small screen.

---

## Section separation & Division (4 canonical)

_Clear criteria for section division, completing login on one screen, fitting sections within the mobile viewport, and giving core content a large footprint._

### [LAYOUT-SEC-001] Set clear criteria for section division
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Section separation & Division

**Principle**: Use a clear division rule for the layout, such as a two-pane split. Each element must clearly belong to one region; placing it ambiguously between two regions makes the structure hard to read. When inserting an image, check that it balances with the surrounding group.

**Why**: If the division rule is wrong, even generous whitespace makes the layout look more complicated. When keeping a card-based UI style, separating areas with a white top and a card bottom feels more natural than column dividers.

**Anti-pattern**: A layout where an element sits ambiguously between the upper and lower regions, making the hierarchy hard for users to read.

---

### [LAYOUT-SEC-002] Fit the full login flow on one screen
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Section separation & Division

**Principle**: On the login page, all core flows — sign-in, sign-up, password recovery — must be visible in a single screen without scrolling. On checkout and selection pages, the important information should also be visible on one screen without scrolling.

**Why**: If users do not notice the sign-up option, conversion rates drop. Hiding core flows below the fold increases drop-off.

**Anti-pattern**: A login page where the sign-up prompt is not visible on the first screen at 375px and only appears after scrolling.

---

### [LAYOUT-SEC-003] Complete mobile sections within the viewport
- **Platform**: Mobile
- **Frequency weight**: 5
- **Sub-category**: Section separation & Division

**Principle**: On mobile, size each section (corner) so it fits entirely within a single viewport. If content overflows, use a large image and overlap text and tabs on top of it to keep everything on one screen. Composing the layout differently for the empty (inactive) and entered (active) states can improve both space efficiency and usability.

**Why**: Content that spills past the viewport without intent is hard for users to navigate. Remove anything not strictly needed to keep the screen concise and reduce columns.

**Anti-pattern**: A mobile layout where a single section is taller than the viewport, forcing the user to scroll just to see one section.

---

### [LAYOUT-SEC-004] Make core content large and clear
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Section separation & Division

**Principle**: Dashboard graphs and charts should fill as much of their module as possible — only at that scale can they convey data effectively. Keep the layout structure simple. If a title and body can be combined rather than separated by an image in the middle, combine them.

**Why**: Small graphs make data hard to read and undermine the dashboard's function. Unnecessary separation makes the screen busier.

**Anti-pattern**: A dashboard whose graph area is far too small relative to the module, making the data hard to read.

---

## Image & Thumbnail placement (4 canonical)

_Unifying image ratios, principles for overlapping text on images, ways to emphasize an image, and overlapping label placement._

### [LAYOUT-IMG-001] Unify and clarify image ratios
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Image & Thumbnail placement

**Principle**: Same-type thumbnails on the same screen must share the same aspect ratio. Image areas should be defined at a clear ratio such as 1:1, 4:3, or 16:9, and limit image card ratios within a single section to at most two.

**Why**: Mismatched ratios significantly lower the perceived quality of the layout. On mobile, text wrapping changes card heights and leaves a 'gap-toothed' look, so plan for it ahead of time.

**Anti-pattern**: A layout that mixes square, vertical-rectangle, and horizontal-rectangle images within the same section.

---

### [LAYOUT-IMG-002] Principles for text-on-image overlap
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Image & Thumbnail placement

**Principle**: When placing text on top of an image, position it so it does not cover the image's main subject (its visual focal point). On a billboard, separate text and image clearly into left/right or top/bottom regions, or adjust placement so they do not cover each other. Overlapping text on a functional interactive element hurts readability, so move the text outside that area. When highlighting a product image, overlapping text on top while maximizing the image area is effective.

**Why**: In any layout where graphics and text coexist, the text must never be clipped or block the main subject. Splitting the image and text information into distinct columns or blocks makes both more readable.

**Anti-pattern**: Text covering the image's focal point, or text overlapping a map so both readability and interaction suffer.

---

### [LAYOUT-IMG-003] Emphasize images by showing them large
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Image & Thumbnail placement

**Principle**: To emphasize an image, remove anything that obscures it and compose the layout so the image appears as large and clear as possible. Product detail pages aiming for a premium feel should be image-led with minimal information. An open, spacious feel comes from the balance between image size, font size, and overall density.

**Why**: Wrapping an image in a box is not how you emphasize it. For mobile image sliders, filling the area edge-to-edge instead of slicing it into cards lets the product appear larger.

**Anti-pattern**: Claiming to emphasize an image while boxing it in, or chopping thumbnails into cards with vertical margins.

---

### [LAYOUT-IMG-004] Overlap labels and badges slightly
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Image & Thumbnail placement

**Principle**: Labels (badges, tags) feel more refined and dimensional when placed with a slight overlap on the related element. Listing multiple profile images with a slight overlap also makes them read as a single group.

**Why**: Laying labels flat in their own area is visually flat and uninteresting. Overlapping naturally expresses depth and hierarchy.

**Anti-pattern**: Labels listed flat beneath the image with no overlap.

---

## Information density & Whitespace (3 canonical)

_Designing rhythm of strong and soft, securing breathing room, generous whitespace on the web, and removing unnecessary elements._

### [LAYOUT-DENSITY-001] Create strong/soft rhythm and breathing room
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Information density & Whitespace

**Principle**: Always place breathing room (empty space, whitespace) between bold colors and large elements. If the top is visually heavy, lighten the bottom section to balance the strong/soft rhythm. A heavy section should be followed by a lighter one to create visual rhythm and natural content flow.

**Why**: If every region shouts, nothing stands out. The more visually intense the imagery, the more breathing room the layout needs for the whole design to breathe.

**Anti-pattern**: A layout packed exclusively with bold-toned elements and no breathing room at all.

---

### [LAYOUT-DENSITY-002] Use generous whitespace in web design
- **Platform**: PC
- **Frequency weight**: 6
- **Sub-category**: Information density & Whitespace

**Principle**: Just because the web canvas is wide does not mean you should fill every element. Instead, lean into spaciousness and use whitespace boldly and generously. In minimal design, volume comes not from adding elements but from boldly enlarging existing element sizes and whitespace. The layout should preserve a sense of mass while still securing whitespace.

**Why**: A cramped-looking UI is not always due to insufficient whitespace. Heavy lines or unresolved text hierarchy can produce the same symptom. Item lists do not have to fill the full width — leaving intentional whitespace makes them feel more orderly.

**Anti-pattern**: A web layout made busy by trying to fill the wide canvas with anything and everything.

---

### [LAYOUT-DENSITY-003] Remove unnecessary elements
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Information density & Whitespace

**Principle**: Removing unnecessary elements is as important a design act as adding them. Simpler layout structure is better. A quick checklist to lift main page quality: 1) remove unnecessary decoration, 2) remove excessive dark backgrounds, 3) tidy whitespace, 4) tidy corner radii. Even with strong volume, too many unnecessary distractions make a layout look busy.

**Why**: On text-driven information pages, background colors and decorative shapes interrupt the reading flow. Stacking another busy section under an already busy top design causes visual fatigue.

**Anti-pattern**: A portfolio layout with colored shapes scattered across the background, disrupting text readability.

---

## Element size & Balance (4 canonical)

_Proportional element sizing, optical centering corrections, size contrast and count limits for graphic objects, and balance between input components._

### [LAYOUT-SIZE-001] Proportional sizing and balance
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Element size & Balance

**Principle**: Size elements within a layout in proportional relationships to one another. Decide visual size in proportion to information importance. The thumbnail and any UI element placed on top of it (such as a button) must be sized in proportion. Notification/banner components that remain pinned on screen should be kept as compact as possible.

**Why**: When a single element sticks out or is too small, the overall balance collapses. On information-confirmation pages like an order summary, shrink the thumbnail to focus attention on the text information.

**Anti-pattern**: An order screen where the product thumbnail is so large that the image dominates over the information being confirmed.

---

### [LAYOUT-SIZE-002] Optical centering correction
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Element size & Balance

**Principle**: When a center-placed element looks like it sags visually, nudge it slightly above the mathematical center to achieve optical balance. Deliberately tune the top/bottom weight distribution of the layout to create visual stability.

**Why**: The mathematical center differs from the optical center, which can create the illusion that the logo is sagging downward.

**Anti-pattern**: A splash screen logo that is mathematically centered but visually appears to sag downward.

---

### [LAYOUT-SIZE-003] Size contrast and count for graphic objects
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Element size & Balance

**Principle**: When placing multiple graphic elements, always introduce size contrast to create a focal point for the eye. Limit repeated objects to three or fewer and use size contrast (large-medium-small, or one large and two small) to build visual rhythm. Size contrast alone is enough to feel dynamic.

**Why**: Multiple objects of similar size scatter attention rather than focusing it. A perfectly straight-line arrangement lacks depth and dynamism, and looks monotonous.

**Anti-pattern**: A banner with four similarly sized hearts arranged in a perfectly straight line.

---

### [LAYOUT-SIZE-004] Balance between input components
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Element size & Balance

**Principle**: Input components placed side by side within the same section must be balanced in length and form. If needed, place the button inside the input or restructure the layout. An input and its related button (Confirm, Apply, etc.) should sit side by side horizontally or be closely connected to make the relationship explicit.

**Why**: Different-purpose UI elements like input boxes and select boxes need to be visually distinguished by whitespace and color for the balance to come through. When an input and its related button sit in different places, users struggle to see the connection.

**Anti-pattern**: An input box and a select box of different lengths in the same section, looking visually awkward together.

---

## Layout rhythm & Pattern consistency (4 canonical)

_Repeating common layout modules, designing rhythmic variation, unified design feel, and diversifying benchmarks._

### [LAYOUT-RHYTHM-001] Repeat a common layout module
- **Platform**: Mobile/PC
- **Frequency weight**: 11
- **Sub-category**: Layout rhythm & Pattern consistency

**Principle**: Clean design rests on a repeatable common layout module. Consistently repeating the same layout pattern creates a concise, orderly impression. Two designs only feel like 'different styles' when their layout flow and module composition differ. Minimizing layout types within a page and keeping a repeating pattern raises visual consistency.

**Why**: Using a different structure for every section looks complicated and chaotic. When inner sections share the same layout as the billboard, the design feels more unified.

**Anti-pattern**: A main page where every corner uses a completely different layout shape, with no common module.

---

### [LAYOUT-RHYTHM-002] Vary the layout rhythm
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Layout rhythm & Pattern consistency

**Principle**: Layouts need rhythm and variation. Alternate dense sections with open sections, or vary density, to create visual rhythm. Repeating the same split pattern in card or list layouts kills the sense of rhythm. Decide ahead of time how the last row of an odd-count grid will be handled.

**Why**: Repeating the same dense pattern flattens the rhythm and feels monotonous. In a scrolling layout, place elements that anchor the visual weight at intervals to prevent monotony.

**Anti-pattern**: A layout that repeats the same dense block in every section, or keeps splitting cards only horizontally with no rhythmic variation.

---

### [LAYOUT-RHYTHM-003] Unified, concise design feel
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Layout rhythm & Pattern consistency

**Principle**: A clean layout should be composed normally, without anomalies or excess. Unified design feel emerges naturally when elements share the same alignment baseline and the same style rules are applied repeatedly. In minimal design, 'clean because it's empty' is different from 'clean because it's well organized'. A simple and refined feel is created when information elements are aligned to one baseline and given enough whitespace.

**Why**: Elements that repeat within the same area must be treated consistently — borders, backgrounds, size units, and so on.

**Anti-pattern**: A minimal design that looks clean because of whitespace but is actually missing alignment and volume discipline.

---

### [LAYOUT-RHYTHM-004] Diversify your benchmarks
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Layout rhythm & Pattern consistency

**Principle**: When benchmarking layouts, compare multiple apps rather than a single one and identify the common patterns to apply. If your alignment and structure end up too similar to a reference site, apply a differentiation strategy to secure uniqueness. Do not apply print's document-style layout approach directly to web design.

**Why**: Referencing only one benchmark causes you to blindly follow that single platform's decisions.

**Anti-pattern**: A news app design that copies Instagram's layout straight down to the same whitespace structure.

---

## Banner & Hero layout (2 canonical)

_Banner workflow (text first), full-width placement, and setting a clear visual focal point._

### [LAYOUT-BANNER-001] Place text first when designing banners
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Banner & Hero layout

**Principle**: Always lock in the text placement and hierarchy first when designing a banner, then work on the graphics. Place low-priority logos small in a peripheral area such as the top right to preserve space for the core content.

**Why**: If you draw the graphics first, the text's readability and placement become subordinate to them and the core message weakens.

**Anti-pattern**: A banner workflow that places the graphic image first and squeezes the text into whatever space remains.

---

### [LAYOUT-BANNER-002] Make banners powerful with full width
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Banner & Hero layout

**Principle**: Elements meant to make an impression — like banners — feel stronger and anchor the layout's center of gravity when filled to full width. When image and text coexist in a banner or hero section, set a clear visual focal point and align the elements to it.

**Why**: If the banner does not use the full width and looks weak, the impact of the entire layout suffers.

**Anti-pattern**: A layout where the banner sticks out to the right and fails to occupy the full width, leaving it looking weak.

---

## Choosing horizontal vs. vertical arrangement (3 canonical)

_Choosing the arrangement direction by context, planning for variable content expansion, and handling text overflow._

### [LAYOUT-DIR-001] Choose horizontal vs. vertical by context
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Choosing horizontal vs. vertical arrangement

**Principle**: When you have many short items like categories or tags, a horizontal arrangement uses space efficiently and looks open. For list-style information with many items, vertical arrangement is more readable than horizontal. For information-rich cards, a horizontal list layout scans better than a vertical one. The arrangement direction should be decided by information structure and usage context, not by the desire to add visual volume.

**Why**: Forcing a horizontal arrangement in a narrow area squashes the spacing between elements. When listing many items, use a grid (e.g., 3 left and 3 right) or a two-column layout to improve space efficiency and scannability.

**Anti-pattern**: Stacking items vertically just to add visual volume even though a horizontal arrangement would suit them better.

---

### [LAYOUT-DIR-002] Design for variable content expansion
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Choosing horizontal vs. vertical arrangement

**Principle**: Items that may be added repeatedly should be laid out vertically to preserve scalability. For variable-length text (usernames, titles, etc.), always design for the case where it wraps to two or more lines. Placing fluidly varying text on the same row as fixed elements causes overlap bugs. When designing a list item, account for text that may wrap to multiple lines so the layout does not break.

**Why**: When social login buttons expand from three to four, the horizontal arrangement loses its balance. Areas with variable-length text such as price should consider vertical placement instead of a single horizontal row.

**Anti-pattern**: Three social login buttons arranged horizontally, then adding a fourth and breaking the layout.

---

### [LAYOUT-DIR-003] Label-input vertical, single representative SNS icon
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Choosing horizontal vs. vertical arrangement

**Principle**: A label (title) above its input field (input or select) flows more naturally for reading than a horizontal arrangement and uses space more efficiently. For social-link icons, placing a single representative one per section is cleaner; repeating one per image creates visual noise. For interest or category selection UI, the standard patterns are a tag (chip) list or a grid.

**Why**: Horizontal arrangements make elements compete in narrow spaces and feel cramped. Repeated social icons become visual noise and reduce focus.

**Anti-pattern**: A layout where the title sits in front and the input sits to the right, competing for room in a narrow space.

---

## Element position & Affiliation (3 canonical)

_Making the relationship between an element's position and its related content clear, managing button containers, and using space efficiently for indicators._

### [LAYOUT-POS-001] Position elements with a clear affiliation
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Element position & Affiliation

**Principle**: Place UI elements where they naturally connect to their related content. Group related elements together to express their visual relationship; separating them blurs the relationship. Place chart data labels as close as possible to their data points. Combining functionally related elements (search bar plus button, etc.) into a single unit is cleaner and more intuitive.

**Why**: When action buttons like Save or Share sit in isolated positions, both discoverability and usability drop. Titles should be placed visually close to the content they relate to.

**Anti-pattern**: Share and save icons floating in an ambiguous spot, disconnected from the content they belong to.

---

### [LAYOUT-POS-002] Place buttons inside a fixed container
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Element position & Affiliation

**Principle**: CTA buttons must always live inside a container (frame), managed as a fixed area including the top and bottom whitespace. Pin the button to a clearly defined location on the screen (top or bottom) and keep it from overlapping the content area. Place floating elements where they do not obscure the main interactive elements. For a centered form, center-align the title so visual focus converges in the middle.

**Why**: Placing a button without a container makes it hard to define its relationship with the safe area and other elements, and causes problems when reused on other pages.

**Anti-pattern**: A CTA button placed without any frame, floating loosely on the screen.

---

### [LAYOUT-POS-003] Use space efficiently for indicators and overlays
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Element position & Affiliation

**Principle**: Page indicators and progress bars should be overlaid on top of content rather than occupying their own region, so the screen space is used efficiently. Layer (depth) separation should be based on information structure and user flow.

**Why**: An unnecessary top region eats into the screen and shrinks the content area. Layer separation purely for visual effect actually creates confusion.

**Anti-pattern**: A layout that puts the progress bar in a separate top region, creating unnecessary whitespace.

---
