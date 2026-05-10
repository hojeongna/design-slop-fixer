# Component (UI)

Button, icon, card, input field, and other UI component design rules

- **Total canonical rules**: 41
- **Sub-categories**: 13

---

## Contents
- Button — 7 canonical
- Icon — 6 canonical
- Design system / consistency — 3 canonical
- Card — 4 canonical
- Input field — 6 canonical
- Tab — 5 canonical
- GNB / navigation — 2 canonical
- Chart / graph — 1 canonical
- Chip / badge / tag — 2 canonical
- Toggle / checkbox — 1 canonical
- Indicator / slider — 2 canonical
- Modal / popup / overlay — 1 canonical
- Effect — 1 canonical

---

## Button (7 canonical)

_Principles for overall button design, including minimum size, visual hierarchy, style consistency, shared componentization, internal text balance, and treatment of secondary buttons._

### [COMP-BTN-001] Minimum touch target for buttons
- **Platform**: Mobile/PC
- **Frequency weight**: 24
- **Sub-category**: Button

**Principle**: On mobile, set the minimum button height to at least 40px, with 44-48px recommended. Buttons in the 26-36px range have touch targets that are too narrow and are not acceptable in real-world practice. On the web, buttons that are too chunky or too thin also clash with the typographic scale.

**Why**: Platform HIGs (iOS 44pt, Material 48dp) define the minimum standard for comfortable touch input. Buttons below this threshold are physically difficult for users to tap.

**Anti-pattern**: Designing sub-standard buttons such as 26px or 36px and only verifying them on the designer's monitor while ignoring actual device usability.

---

### [COMP-BTN-002] Design a clear visual hierarchy for buttons
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Button

**Principle**: Buttons must have a clear hierarchy of Primary (filled), Secondary (outlined), and Tertiary (text). When every button is rendered at the same intensity (e.g., black, filled), users cannot tell which action to prioritize.

**Why**: Without a button hierarchy, every action is emphasized equally, increasing visual noise and making user decisions harder.

**Anti-pattern**: Treating delete, cancel, and secondary buttons all with the same Primary style (strong black, filled background).

---

### [COMP-BTN-003] Keep button styles consistent
- **Platform**: Mobile/PC
- **Frequency weight**: 13
- **Sub-category**: Button

**Principle**: Within a single screen, buttons that play the same role must share the same corner radius, color, and style (filled or outlined). When buttons on the same screen, such as a login button and a social login button, use different corner radii, consistency breaks down.

**Why**: Mixing buttons with inconsistent styles creates unintended hierarchy differences and gives the impression of an unfinished design.

**Anti-pattern**: A login button with a large corner radius placed alongside a social login button with a small radius, causing the styles to clash on the same screen.

---

### [COMP-BTN-004] Define buttons as shared components
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Button

**Principle**: Define buttons that share the same role as a single shared component and reuse it across every page. Place buttons inside a frame (container) so that spacing is managed consistently.

**Why**: Drawing buttons from scratch on every page is inefficient because changes must be made on every page individually, and inconsistencies inevitably emerge.

**Anti-pattern**: Drawing buttons of similar roles separately on each page so their heights end up as 52, 46, 44, and 42px in different places.

---

### [COMP-BTN-005] Balance button text and padding
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Button

**Principle**: As button height increases, the size and weight of the inner text should scale up accordingly. Padding that is too tight feels cramped, and a strong container paired with weak text produces visual imbalance.

**Why**: When the container color is read first and the inner label only after, the button fails to communicate its function (its label).

**Anti-pattern**: A 64px tall button containing only small text, so the background color dominates the perception.

---

### [COMP-BTN-006] Use lower emphasis for secondary and delete buttons
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Button

**Principle**: Secondary action buttons such as delete, more, and expand should carry less emphasis than the Primary style. Expressing them lightly as a text link or outlined button prevents unintended clicks and lets the primary CTA stand out.

**Why**: When delete buttons are emphasized in red, the entire table becomes visually cluttered and the risk of accidental clicks increases.

**Anti-pattern**: Placing a red delete button in Primary style on every row of a table, or unnecessarily emphasizing an expand button inside a card.

---

### [COMP-BTN-007] Other button design principles
- **Platform**: Mobile/PC
- **Frequency weight**: 29
- **Sub-category**: Button

**Principle**: Buttons must have a size and visual structure that makes clickability immediately obvious. Place high-emphasis buttons inside a card so they are tied to the content. Consolidate buttons with similar functions to reduce complexity.

**Why**: When a button floats outside its card, its ownership becomes ambiguous, and splitting buttons with similar functions scatters the UI and adds complexity.

**Anti-pattern**: Using a size or structure that leaves it unclear whether something is a button, or splitting buttons that perform the same function into several separate buttons.

---

## Icon (6 canonical)

_Icon design principles covering set consistency (stroke weight and style), appropriate sizing, simplification, semantic and functional fit, and minimizing circular backgrounds._

### [COMP-ICO-001] Keep the icon set unified
- **Platform**: Mobile/PC
- **Frequency weight**: 21
- **Sub-category**: Icon

**Principle**: All icons used on a single screen must come from one unified set with consistent line/fill style, stroke weight (e.g., 2px), size, and end caps (rounded or square). Mixing icons with inconsistent stroke weights or from sources with different styles destroys the cohesion of the set.

**Why**: Without icon consistency, the icons no longer feel like 'one product's icon set' but like a collection pulled from different places, lowering the perceived quality and trustworthiness.

**Anti-pattern**: Randomly mixing line icons and filled icons, or placing icons with inconsistent stroke weights such as 1px, 1.5px, and 2px on the same screen.

---

### [COMP-ICO-002] Use the right icon size
- **Platform**: Mobile/PC
- **Frequency weight**: 18
- **Sub-category**: Icon

**Principle**: Around 28px is the standard for UI icons: 28px for GNB and tab bars, 24px for inline use, and at least 40-44px for the touch target. On a mobile tab bar, 36px is too large and 20px is too small.

**Why**: Icons that are too small reduce recognizability and touch comfort, while icons that are too large shift the layout's visual weight and make the UI feel heavy.

**Anti-pattern**: Using a 16px icon directly as a tap target, or placing a 36px icon in the tab bar so it consumes excessive space.

---

### [COMP-ICO-003] Keep icons simple
- **Platform**: Mobile/PC
- **Frequency weight**: 14
- **Sub-category**: Icon

**Principle**: Strip UI icons of unnecessary detail and design them simply. Their shapes must remain clearly recognizable at small sizes, so minimize the number of lines and avoid complex depictions. Icons must always be delivered as SVG vector files.

**Why**: Complex icons blur at small sizes and add UI noise. PNG/JPG icons cannot be recolored or scaled cleanly.

**Anti-pattern**: A house icon that even draws the chimney, an icon with so many lines that it looks like an illustration, or icons inserted as PNGs.

---

### [COMP-ICO-004] Match icons to meaning and function
- **Platform**: Mobile/PC
- **Frequency weight**: 14
- **Sub-category**: Icon

**Principle**: Use icons only when text alone is insufficient to convey meaning. Unnecessary icons, or icons whose meaning does not match the accompanying text, only add visual complexity. Buttons of the same hierarchy must also be consistent about whether they include an icon.

**Why**: Icons that do not contribute to conveying information complicate the layout and dilute the user's focus.

**Anti-pattern**: Placing 'location/place' text next to a home icon so the icon and content don't match, or having an arrow icon on the share button while the cancel button has none.

---

### [COMP-ICO-005] Minimize circular backgrounds on icons
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Icon

**Principle**: Before adding a circular or square background (wrapper) around an icon, first verify that the icon is sufficiently recognizable without one. Unnecessary circular backgrounds add weight and complicate the layout, and when repeated excessively they make the screen feel cluttered.

**Why**: When a circular background is repeated on every icon, each icon reads as an independent emphasis element and the overall screen becomes scattered.

**Anti-pattern**: Applying a circular background to every icon by default, or wrapping icons in a circle for no reason and adding visual weight to the screen.

---

### [COMP-ICO-006] Other icon design principles
- **Platform**: Mobile/PC
- **Frequency weight**: 13
- **Sub-category**: Icon

**Principle**: Review icons at their actual usage size (the rendered, reduced state). Reviewing only at zoomed-in sizes cannot guarantee legibility in the real UI. Tab bar icons must convey their function intuitively, and when meaning is ambiguous, pair them with a text label.

**Why**: The quality of an icon's design is determined at its actual rendered size, and an icon whose function the user cannot recognize is no better than no icon at all.

**Anti-pattern**: An icon that looks fine when zoomed in but blurs at the actual 28px size, or using an abstract tab bar icon whose function is unclear without a text label.

---

## Design system / consistency (3 canonical)

_Foundations of the design system, including building a shared component system, reuse principles, maintaining consistency, and handling edge cases such as profile images._

### [COMP-DS-001] Build a shared component system
- **Platform**: Mobile/PC
- **Frequency weight**: 13
- **Sub-category**: Design system / consistency

**Principle**: Production design covers not only the visual output but also component design, design system construction, and long-term maintainability. Unify shared standards (fonts, colors, sizes) across all screens, and define the shared system first - then design through reuse - before the number of cases grows.

**Why**: Adding new styles for every case without rules makes collaboration and maintenance impossible and gives the impression that no design system exists.

**Anti-pattern**: Different font, color, and size standards on every screen, or creating a new spec for every edge case so the number of component variants grows endlessly.

---

### [COMP-DS-002] Maintain component consistency
- **Platform**: Mobile/PC
- **Frequency weight**: 7
- **Sub-category**: Design system / consistency

**Principle**: Components that play the same role must follow the same style standards throughout the design. Use the same module for sections that share the same structure, and fix any unintended inconsistency in shared elements immediately. Unify border-radius values across the entire project as well.

**Why**: Unnecessary design variations break visual consistency and make the work look unfinished.

**Anti-pattern**: Three items of the same role where two share a common style but one is treated differently, or component corner radii that vary across 12, 16, and 8px.

---

### [COMP-DS-003] Other component design principles
- **Platform**: Mobile/PC
- **Frequency weight**: 32
- **Sub-category**: Design system / consistency

**Principle**: For profile images, always design a default (placeholder icon) for the unregistered initial state, and add a border stroke to overlapping profile images. Corner radii are invisible without color contrast or a shadow that separates them from the background, so apply visual separation alongside the radius. A stroke is generally more effective than a shadow for separation, while a shadow works better against complex backgrounds.

**Why**: Missing edge cases such as the unregistered initial state or unhandled overlap separation breaks the UI in real usage.

**Anti-pattern**: An unregistered profile that already shows a real photo, or overlapping profile images of similar colors that cannot be distinguished from each other.

---

## Card (4 canonical)

_Card component design principles, including restrained shadows, appropriate corner radii, stroke and border treatment, when to use cards, and avoiding nested cards._

### [COMP-CARD-001] Use card shadows sparingly
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Card

**Principle**: Keep card shadows extremely subtle - around 2-3% opacity - just enough to separate the card from the background. Using a stroke and a shadow together becomes over-emphasis. Applying shadows to every card dilutes their meaning.

**Why**: Strong shadows make cards appear to float excessively and feel visually heavy. Shadows should be minimized especially on information-dense screens such as dashboards.

**Anti-pattern**: Applying a shadow with 10% or higher opacity to every card, or using a stroke and a shadow at the same time and over-emphasizing the card.

---

### [COMP-CARD-002] Right-size card corner radii
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Card

**Principle**: Set a card's border-radius to match the design concept and content complexity. Keep dashboards tight at around 12px, and use a moderate radius for general apps. For nested rounded boxes, make the inner radius smaller than the outer one.

**Why**: Excessive rounding may look stylish in information-first environments such as dashboards, but it actually increases the perceived complexity of the data.

**Anti-pattern**: Applying deep corner radii to dashboard modules, or setting the inner card's radius equal to or larger than the outer card's radius in a nested layout.

---

### [COMP-CARD-003] Card stroke and border treatment
- **Platform**: PC
- **Frequency weight**: 9
- **Sub-category**: Card

**Principle**: When a card's background matches the page background, define its boundary clearly with a stroke or a shadow. Use strokes for a functional purpose (readability), not decoration; unnecessarily heavy strokes weigh the card down.

**Why**: Without a boundary, the card blends into the background and the layout appears to fall apart. Conversely, excessive strokes make the design look messy.

**Anti-pattern**: Placing a white card on a white background with no stroke, or using a border line so heavy that the structure is read before the content itself.

---

### [COMP-CARD-004] When to use cards
- **Platform**: Mobile/PC
- **Frequency weight**: 15
- **Sub-category**: Card

**Principle**: Use cards only for areas that contain real content. Do not force cards onto regions where simple navigation or a plain text list would suffice. Nested cards (a card inside a card) increase complexity, so handle internal grouping with lighter means such as spacing or dividers.

**Why**: Overusing cards makes every region look like an emphasized element, breaking the hierarchy and weighing the UI down.

**Anti-pattern**: Wrapping simple navigation areas such as a header or breadcrumb in a card, or forcing content into a card format when it does not fit.

---

## Input field (6 canonical)

_Input field design principles, including visual differentiation between states (default, focus, disabled), unified sizing, stroke and background treatment, search field design, and form elements overall._

### [COMP-INP-001] Differentiate input states visually
- **Platform**: Mobile
- **Frequency weight**: 5
- **Sub-category**: Input field

**Principle**: Clearly distinguish the default, focus (active), filled, and disabled states of an input field through color and style. The focus state must be emphasized more strongly than the filled state. In the disabled state, dim the text color and hide unnecessary icons.

**Why**: When input states are not differentiated, users cannot tell which field is currently editable and become confused.

**Anti-pattern**: A default stroke that is black so it is impossible to tell whether the field is being edited or already filled, or eye and clear (X) icons that remain visible even in the disabled state.

---

### [COMP-INP-002] Unify input sizes
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Input field

**Principle**: Limit input field heights across the entire site or app to 2-3 sizes, and use a single size within the same flow (such as the login process). Match the heights of inputs and adjacent buttons to the same size system so that alignment stays clean.

**Why**: When input heights vary by screen across 40, 44, and 48px, it looks like there is no system and collaboration and maintenance become difficult.

**Anti-pattern**: Login, signup, and find-ID screens whose input field heights all differ, or a 48px input next to a 44px button whose heights do not match.

---

### [COMP-INP-003] Input stroke and background treatment
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Input field

**Principle**: An input field can express its editable nature with just a light gray background and no stroke. In list-style layouts, appropriate spacing alone is enough to distinguish inputs. For mouse-over states, a background color change feels more natural than a stroke change.

**Why**: Adding strokes unnecessarily makes the UI complex and visually heavy.

**Anti-pattern**: Adding an unnecessary stroke to an input that is already clearly defined by its background or spacing, or applying a heavy border to every input.

---

### [COMP-INP-004] Other input design principles
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Input field

**Principle**: When a text input becomes active, expose a clear (X) button to reset its content. Input icons must match the field type (use a clear icon on an ID field, not a visibility eye), and placeholder text must match the actual accepted format. Numeric-only fields should trigger the numeric keypad.

**Why**: Incorrect icons or placeholder text prevent users from understanding the correct way to input information.

**Anti-pattern**: Placing a password visibility toggle (eye icon) on an ID field, or using a Korean-text placeholder example on a phone number field.

---

### [COMP-INP-005] Search field design
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Input field

**Principle**: On mobile, give the search field a minimum height of 40px and use a rounded shape with a background fill - this looks more refined than a square outlined box. When a full search field would weigh down the GNB, it is more efficient to show only an icon and expand into a popup or dropdown on click.

**Why**: A thin search field or a square outlined box feels stiff and dated and reduces usability.

**Anti-pattern**: A thin search field 38px or shorter, a square outlined search box, or placing a full search field inside the GNB and weighing the layout down.

---

### [COMP-INP-006] Other form element principles
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Input field

**Principle**: Selection-based input components must include an 'Other / custom input' option for cases not in the list. Handle space-hungry UIs such as date and time pickers lightly via a slide or dropdown. If a separate title above an input can be replaced by a placeholder, omit the title.

**Why**: A UI that cannot handle exceptions blocks users whenever they fall outside the predefined options.

**Anti-pattern**: A select box without an 'Other / custom input' option, or a date picker permanently expanded so it takes up excessive page space.

---

## Tab (5 canonical)

_Tab component design principles, including selected/unselected state differentiation, style choice (underline or button), size and spacing, and purpose-appropriate use._

### [COMP-TAB-001] Differentiate selected and unselected tab states
- **Platform**: Mobile/PC
- **Frequency weight**: 10
- **Sub-category**: Tab

**Principle**: Distinguish the selected tab state with stronger font weight (Bold/SemiBold) and a strong color, and the unselected state with Regular/Medium plus a toned-down color. Apply the brand color to the selected icon in the tab bar. Omitting the active state on a screen where a tab should be active leaves users unable to identify their current location.

**Why**: When selected and unselected states are not differentiated, users cannot recognize their current location and navigation breaks down.

**Anti-pattern**: On the home screen, the Home tab appears unselected with no active indicator, or selected and unselected tabs share the same color and weight.

---

### [COMP-TAB-002] Choose the right tab style
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Tab

**Principle**: Choose the tab style (underline, filled background, or text-only) to fit the background context. On gray or colored backgrounds, text-with-underline tabs produce less noise than bordered styles. Whichever style you choose, use only one consistently and do not mix them.

**Why**: A tab style that does not fit its background creates visual noise, and mixing tab styles destroys consistency.

**Anti-pattern**: Using filled-background tabs on a gray background and creating unnecessary visual noise, or mixing underline tabs and card-style tabs within a single service.

---

### [COMP-TAB-003] Tab size and inner padding
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Tab

**Principle**: Tab components need sufficient height and inner padding (horizontal spacing) to secure a clickable tap target and improve legibility. Medium is generally more appropriate than Bold for tab text, and tabs that are too large consume the main content's space.

**Why**: Tabs that are too small leave the click target too narrow, while tabs that are too large or too heavy cause an inversion where navigation visually outweighs the content.

**Anti-pattern**: Tab buttons so small that the text becomes hard to read, or a large brand name in the tab making the tab appear larger than the content itself.

---

### [COMP-TAB-004] Use tabs only for their intended purpose
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Tab

**Principle**: Use a tab component only when it actually switches content. Overusing tabs as decoration without function confuses users. Place tabs and their related action buttons inside the same container.

**Why**: Repeating tabs without meaning adds unnecessary complexity and makes it harder to distinguish them from tabs that actually switch content.

**Anti-pattern**: Repeating the visual form of tabs in places where they have no meaning, or using tabs purely for decoration without any content-switching function.

---

### [COMP-TAB-005] Other tab design principles
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Tab

**Principle**: Tab components must clearly signal that they are clickable; avoid simply listing text. Tabs look cleaner when consolidated as a single group rather than split into separate elements. When adding an underline (boundary line), always check whether it collides with adjacent elements as the indicator moves.

**Why**: User experience suffers when users cannot recognize a tab as a clickable area, or when the tab's underline collides with adjacent elements.

**Anti-pattern**: Listing tabs as plain text so they don't look like button areas, or splitting individual tab items into separate, disconnected pieces.

---

## GNB / navigation (2 canonical)

_Navigation bar design principles, including componentization and unification of the top GNB and bottom tab bar, icon sizing, and active-state indication._

### [COMP-GNB-001] Componentize the GNB
- **Platform**: Mobile/PC
- **Frequency weight**: 11
- **Sub-category**: GNB / navigation

**Principle**: Always build the GNB (top global navigation bar) as an independent frame, and ensure no inner element extends beyond the frame or overlaps another. Manage it as a single component that can be applied across every page. Never use a text box as a container.

**Why**: Without wrapping the GNB in a frame, you cannot manage it consistently across multiple pages, and the GNB ends up varying from page to page.

**Anti-pattern**: GNB elements scattered as individual layers, stretching a text box to define the GNB area, or the GNB design changing from page to page.

---

### [COMP-GNB-002] Bottom tab bar design
- **Platform**: Mobile
- **Frequency weight**: 9
- **Sub-category**: GNB / navigation

**Principle**: Bottom tab bar (dock bar) icons should be around 28px. Always show the currently active tab in an emphasized state. Chat and notification tabs must include an unread badge. Do not apply effects that hurt legibility (such as a glass effect) to the tab bar.

**Why**: The tab bar is the core element of navigation and must always be clearly recognizable; missing the active-state indicator prevents users from identifying their current location.

**Anti-pattern**: A tab bar icon as large as 36px, the Home tab shown as inactive on the home screen, or a tab bar where icons are obscured by a glass effect.

---

## Chart / graph (1 canonical)

_Chart component design principles for data visualization, including reference lines, data markers, bar corner radii and gradients, and background treatment._

### [COMP-CHR-001] Chart reference lines and structure
- **Platform**: PC
- **Frequency weight**: 9
- **Sub-category**: Chart / graph

**Principle**: Always display low, middle, and high reference lines on data visualization charts so the relative position of each value is instantly readable. Render reference lines as dashed lines to distinguish them visually from data lines. On line charts, place a marker at each data point.

**Why**: Without reference lines, users cannot judge whether chart values are high or low, and the chart fails to convey information.

**Anti-pattern**: No reference lines, leaving the relative position of the data unreadable, or rendering reference lines and data lines in the same solid style so they get confused.

---

## Chip / badge / tag (2 canonical)

_Design principles for secondary label components such as chips, badges, and tags, including hierarchy, stroke weight, and methods of conveying information._

### [COMP-CHIP-001] Chip and badge hierarchy and style
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Chip / badge / tag

**Principle**: Design secondary labels such as chips, badges, and tags one step smaller than the main text. Keep their border lines as thin and light as possible. For supplementary information or annotation-style text, use lightly weighted plain text instead of a tag format.

**Why**: When secondary elements appear larger or stronger than the main text, the hierarchy inverts and the user's attention scatters.

**Anti-pattern**: Chips placed at a size larger than or similar to the body text, or chips with thick strokes that add excessive visual weight.

---

### [COMP-CHIP-002] Designing information in badges
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Chip / badge / tag

**Principle**: Wrap important numeric information such as notification counts in a badge so it stands out visually. Design badges so that the layout does not break even when two or more digits appear. A cart icon must always be designed together with a quantity badge.

**Why**: A notification count rendered as plain text with no background is easy to miss, and ignoring edge cases leads to broken layouts when real data appears.

**Anti-pattern**: A cart icon with no quantity badge, or a badge designed only for single digits that breaks when a two-digit number appears.

---

## Toggle / checkbox (1 canonical)

_Design principles for selection input components such as toggle switches and checkboxes, including appropriate sizing, platform-specific size standards, and state expression._

### [COMP-TOG-001] Toggle and checkbox sizing
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Toggle / checkbox

**Principle**: Set mobile toggle height to a minimum of 28px and aim for a 44px touch target. Web toggles work well at around 20px. For checkboxes, the standard is around 22px on mobile and 20px on the web; 26px or larger is excessive.

**Why**: Toggles and checkboxes that are too small are hard to tap, while ones that are too large break the layout's balance.

**Anti-pattern**: A 16px mobile toggle that is hard to tap, or applying the mobile size (32px) as-is on the web so the control becomes unnecessarily large.

---

## Indicator / slider (2 canonical)

_Slider component design principles, including indicator visibility, handling many items, and placement of carousel arrow controls._

### [COMP-IND-001] Indicator visibility and handling many items
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Indicator / slider

**Principle**: Slide and carousel indicators must have a visible presence (at least 2px thick). When the number of items exceeds 10, replace the dot pattern with a number format (e.g., 8/20) or a line bar.

**Why**: Twenty dot indicators make it impossible to identify the current position and severely degrade usability.

**Anti-pattern**: Lining up 20 dot indicators, or using indicators so thin they have no visual presence.

---

### [COMP-IND-002] Slider control placement
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Indicator / slider

**Principle**: Place carousel and slider arrow buttons where they will not overlap the content, and consider in advance whether overlap could occur with different content variations. Size, shadow, and proportions must work in harmony.

**Why**: Placement that only considers the current screen leads to arrows overlapping with content under real data, degrading usability.

**Anti-pattern**: Arrows placed where they overlap the image, or arrows that are too small with strong shadows and a cramped height.

---

## Modal / popup / overlay (1 canonical)

_Design principles for overlay components such as modals, popups, bottom sheets, and dropdowns, including background separation, corner radii, and when to use them._

### [COMP-MOD-001] Modal, popup, and bottom sheet design
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Modal / popup / overlay

**Principle**: UI elements that float above the layer - popups, cards, dropdowns - must always include a stroke or a shadow so they are clearly separated from the background. A bottom sheet is an excessive pattern when there are few items; lighter patterns such as an inline popup are more appropriate. Set the corner radius proportionally to the overall design tone and the component's size.

**Why**: Without background separation, the boundary between the popup and the background becomes ambiguous and legibility drops.

**Anti-pattern**: A popup with neither a stroke nor a shadow that is indistinguishable from the background, using a bottom sheet for only three items, or a popup with an excessively large corner radius.

---

## Effect (1 canonical)

### [COMP-EFFECT-001] Limit decorative sparkles to the focal point
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Effect

**Principle**: Apply decorative effects such as sparkles to about one main object only, and hold back on secondary elements.

**Why**: Multiple decorative effects scatter the emphasis away from the main object.

**Anti-pattern**: A screen with sparkles on both the main and secondary elements, leaving it unclear which is the main subject.

---
