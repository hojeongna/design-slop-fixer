# Information Architecture (UX)

Information grouping, navigation, menu structure rules

- **Total canonical rules**: 150
- **Sub-categories**: 15

---

## Contents
- Information priority — 14 canonical
- Grouping/proximity — 15 canonical
- Missing information — 14 canonical
- Chat/social metadata — 13 canonical
- Planning first — 13 canonical
- Page purpose — 8 canonical
- Menu/navigation structure — 12 canonical
- Miscellaneous — 11 canonical
- User flow — 10 canonical
- Card structure — 8 canonical
- Portfolio-specific — 10 canonical
- Progressive disclosure — 7 canonical
- Information density — 8 canonical
- Data visualization — 5 canonical
- Payment grouping — 2 canonical

---

## Information priority (14 canonical)

### [INFO-PRIO-001] Decide priority before designing
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: Before starting to design, first decide what the most important information on this page is. Compose by information priority, not visual judgment.

**Why**: Designing without structure destabilizes the information hierarchy.

**Anti-pattern**: Starting from pretty layout first.

---

### [INFO-PRIO-003] Place key information in highly readable positions
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Information priority

**Principle**: Place key information that users must notice most (e.g., price) in highly readable positions at a sufficient size.

**Why**: Position equals visual hierarchy.

**Anti-pattern**: Tucking the price into a small spot in the top-left corner.

---

### [INFO-PRIO-004] Separate the price onto its own line
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: Separate the information users value most (price, key figures) onto its own line and enlarge it so it stands out at a glance.

**Why**: A dedicated line enables instant recognition.

**Anti-pattern**: Placing the price on the same line as other text.

---

### [INFO-PRIO-005] Design the user's gaze flow
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Information priority

**Principle**: Treat the information users should see first with the strongest visual emphasis to design the gaze flow. The user's eye should move exactly as designed.

**Why**: Active gaze flow design.

**Anti-pattern**: Information priority that conflicts with visual emphasis.

---

### [INFO-PRIO-006] Inverted pyramid structure
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: UX/UI layouts work best for information hierarchy when they follow an inverted pyramid structure (important information on top, details below).

**Why**: Matches the F-pattern reading flow.

**Anti-pattern**: Important information placed at the bottom of the page.

---

### [INFO-PRIO-007] Reduce weight of repeatedly exposed information
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: On final pages users reach after passing through several depths, reduce the importance of visual elements they have already verified (thumbnails, etc.) and emphasize information focused on that page's core purpose.

**Why**: Information already seen creates redundant cognitive load.

**Anti-pattern**: Emphasizing a large thumbnail even on the order form.

---

### [INFO-PRIO-008] Decide on 1-2 pieces of information to highlight
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Information priority

**Principle**: On each page, choose the 1-2 pieces of information you most want to show users first, and treat them with the strongest visual emphasis.

**Why**: Emphasizing everything on a page emphasizes nothing.

**Anti-pattern**: All information rendered with similar intensity.

---

### [INFO-PRIO-009] Organize information by readability
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: Readability must be the criterion for every decision about organizing and arranging information.

**Why**: Readability is the essence of information delivery.

**Anti-pattern**: Organizing with aesthetics as the priority.

---

### [INFO-PRIO-010] Make information priority criteria explicit
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Information priority

**Principle**: When organizing information, first set criteria for 'what is important,' then distribute visual emphasis according to that standard. A design where the criteria are visible is a good design.

**Why**: Design without criteria becomes scattered.

**Anti-pattern**: Listing multiple pieces of information with no criteria.

---

### [INFO-PRIO-011] Order information by the user's curiosity
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: Arrange information in the order the user is most curious about (what -> when -> conditions).

**Why**: Follows the user's cognitive flow.

**Anti-pattern**: Putting 'same-day payout' before the emoticon (the thing being received).

---

### [INFO-PRIO-012] Benefits come before options
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: On product detail pages, surface benefits (coupons, discount vouchers, etc.) before the option selection UI. Benefits influence purchase decisions more directly.

**Why**: Purchase motivation precedes selection.

**Anti-pattern**: Emphasizing only option selection.

---

### [INFO-PRIO-013] Horizontal arrangement improves visibility
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: Key feature items read in one glance with higher visibility when arranged horizontally rather than vertically. Do not place important information in positions the eye does not reach (such as bottom-left).

**Why**: Leverage positions where the gaze naturally lands.

**Anti-pattern**: Three key features stacked vertically in the bottom-left.

---

### [INFO-PRIO-014] Emphasize the key column in tables
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: In tables, the most important column (e.g., amount) becomes immediately recognizable when set with heavier weight, larger size, and right alignment.

**Why**: Improves table scanning efficiency.

**Anti-pattern**: All table columns rendered with the same weight.

---

### [INFO-PRIO-015] Lead the eye to key table data
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information priority

**Principle**: In tables, give visual emphasis to the most important information (e.g., amount) so the user's eye is naturally led to the key data.

**Why**: Design that guides the gaze.

**Anti-pattern**: Amount and supplementary information rendered with the same weight.

---

## Grouping/proximity (15 canonical)

### [INFO-GROUP-002] Place buttons inside the most related information unit
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Place a button inside the information unit it most directly acts upon. Putting it in the parent container makes it unclear which item the button refers to.

**Why**: A button's position conveys its meaning.

**Anti-pattern**: A 'class time' button placed inside the instructor card.

---

### [INFO-GROUP-003] Do not split information cards
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Display related information bound together in a single group. Elements in the same category, such as benefits or shipping information, should be visually grouped together.

**Why**: Splitting creates cognitive load.

**Anti-pattern**: Breaking benefit information into four small cards.

---

### [INFO-GROUP-004] Bundle related metadata together
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Grouping/proximity

**Principle**: Place related information close together (proximity principle). Metadata such as source, vendor name, and date should sit near the content title.

**Why**: Metadata supports the content.

**Anti-pattern**: The source appearing separately at the bottom of the card.

---

### [INFO-GROUP-005] Clearly separate groups of different nature
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Separate items from different categories clearly with whitespace, color, or dividers so users can recognize group boundaries.

**Why**: Without separation, items read as one bundle.

**Anti-pattern**: Card payment and easy payment sharing the same gray background.

---

### [INFO-GROUP-006] Different functions belong in separate groups
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Group UI elements by functional similarity. Separate elements of different nature into distinct groups.

**Why**: A group represents a functional unit.

**Anti-pattern**: Voice and file attachment placed in the same group.

---

### [INFO-GROUP-007] Group information and images separately
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: When grouping information, bind elements of the same nature together. Readability improves when text information and images are not interleaved but kept in separate regions.

**Why**: Mixing scatters the gaze.

**Anti-pattern**: Alternating information-image-information layout.

---

### [INFO-GROUP-008] Separate the calculation from the payment method
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Separate the payment summary (calculation) from the payment method input area into distinct sections.

**Why**: The two areas serve different purposes.

**Anti-pattern**: The calculation included inside the card-payment card.

---

### [INFO-GROUP-009] Place tabs directly above the content they control
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Place the tab component directly above the content it controls. Avoid placements that make tabs look like a child element of an adjacent component.

**Why**: Tab position signals scope of effect.

**Anti-pattern**: Tabs sitting next to the email field, making them look like email-related tabs.

---

### [INFO-GROUP-010] Keep key information near the user's path
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Group core purchase information such as price and specs visually close to the product name or icon to shorten the user's information-seeking path.

**Why**: Long paths break information continuity.

**Anti-pattern**: Price placed far from the product.

---

### [INFO-GROUP-011] CTA belongs inside its group
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Include the CTA button within its information group to honor the proximity principle.

**Why**: When separated, the CTA reads as unrelated.

**Anti-pattern**: Plan information separated from the free trial button.

---

### [INFO-GROUP-012] Concentrate comparison information on one side
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Concentrate comparison information on the left side to reduce gaze travel and improve scanning efficiency.

**Why**: Zig-zag gaze patterns cause fatigue.

**Anti-pattern**: Comparison information spread widely across left and right.

---

### [INFO-GROUP-013] Group shipping information
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Bundle shipping-related information such as shipping fee, delivery date, and shipping savings into one group placed in close proximity.

**Why**: Grouping by topic.

**Anti-pattern**: Shipping savings placed in a separate area.

---

### [INFO-GROUP-014] Organize and group footer elements
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: The footer should clearly group related elements and use whitespace between groups to build visual structure. Listing without grouping increases complexity.

**Why**: The footer is also an information area.

**Anti-pattern**: Information listed sequentially in the footer with no structure.

---

### [INFO-GROUP-015] Bundle, do not split
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Wrap elements that belong to the same information group in a single container. Unnecessary separation increases layout complexity and harms information connectivity.

**Why**: Splitting becomes noise.

**Anti-pattern**: Splitting keywords and brands into three separate areas.

---

### [INFO-GROUP-016] Visually group related elements
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Grouping/proximity

**Principle**: Group related information visually. When individual elements are scattered separately, the information structure blurs.

**Why**: A group is a cognitive unit.

**Anti-pattern**: Elements scattered across the dashboard.

---

## Missing information (14 canonical)

### [INFO-MISSING-001] Show counts on social actions
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: Showing the count below social action icons such as favorite, share, and comment is the standard pattern.

**Why**: Acts as a trust indicator.

**Anti-pattern**: No favorite count displayed.

---

### [INFO-MISSING-002] Standard action set for short-form video
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: In short-form video formats, the comment icon is nearly mandatory; review the favorite, share, comment, and more action set as the default configuration.

**Why**: Domain standard.

**Anti-pattern**: Short-form video without a comment action.

---

### [INFO-MISSING-003] Audit required information up front
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Missing information

**Principle**: Audit up front whether mandatory information required by domain standards (contact, terms, footer information, etc.) is missing.

**Why**: Discoveries after launch require expensive fixes.

**Anti-pattern**: Missing contact field in sign-up.

---

### [INFO-MISSING-004] Cite sources in AI answers
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: When showing information assembled by AI, also provide source links or reference indicators.

**Why**: Builds trust and enables verification.

**Anti-pattern**: AI answers with no source.

---

### [INFO-MISSING-005] Show selection results
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: The user's selected value must always be verifiable, even in the collapsed state. Visibility of the selection result is essential.

**Why**: A foundation of trust.

**Anti-pattern**: Unable to verify the selected region after choosing it.

---

### [INFO-MISSING-006] Place selected options where they can be recognized
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: Display the selected option value clearly in a position the user can recognize immediately. Avoid low-recognition positions (bottom, small size).

**Why**: Selection feedback.

**Anti-pattern**: Option name shown small at the bottom of the card.

---

### [INFO-MISSING-007] State the number selectable
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: If there is a quantity limit on selectable items, state the maximum allowed and the current count on screen.

**Why**: Relieves user anxiety.

**Anti-pattern**: No information on the maximum selection count.

---

### [INFO-MISSING-008] Current selection counter
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: In multi-select UIs, display the current number selected in real time so users can intuitively grasp progress.

**Why**: Progress awareness.

**Anti-pattern**: Unable to tell how many items have been selected.

---

### [INFO-MISSING-009] Number selection order
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: In multi-select UIs, displaying selection-order numbers on icons or chips lets users grasp the selection state immediately.

**Why**: Order conveys additional information.

**Anti-pattern**: All selected items shown identically.

---

### [INFO-MISSING-010] Design search up front
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: Services where list content (chats, contacts, etc.) can grow must include search from the design stage.

**Why**: Considers scalability.

**Anti-pattern**: Skipping search because the list is currently small.

---

### [INFO-MISSING-011] Design every edge case
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: Design every result state of interactions (after deletion, after error, empty state, etc.) without exception.

**Why**: Ignoring edge cases leads to incidents after launch.

**Anti-pattern**: No empty state designed after profile deletion.

---

### [INFO-MISSING-012] Show total count in collapsed lists
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: On collapsed lists, state the total item count as text so users can grasp the content's scale in advance.

**Why**: Foreshadowing is user-friendly.

**Anti-pattern**: Unable to know the total count before expanding.

---

### [INFO-MISSING-013] Mark one-off vs recurring alarms
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Missing information

**Principle**: In alarm lists, clearly indicate each alarm's recurrence (one-off, daily, specific weekdays, etc.).

**Why**: Core information.

**Anti-pattern**: Unable to tell whether the alarm is one-off or recurring.

---

### [INFO-MISSING-014] Keep 12-hour and 24-hour formats consistent
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing information

**Principle**: When a time picker uses AM/PM, it must display only 1-12; never mix 12-hour and 24-hour formats.

**Why**: Notation consistency.

**Anti-pattern**: Mixing AM/PM with 17-23 hour values.

---

## Chat/social metadata (13 canonical)

### [INFO-CHAT-001] Chat count badge
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: Chat list items must display a badge (alert count) showing the number of unread messages.

**Why**: Standard messenger pattern.

**Anti-pattern**: No unread message count.

---

### [INFO-CHAT-002] Chat message preview
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Chat/social metadata

**Principle**: In chat lists, display the most recent message as a 1-2 line preview.

**Why**: Helps users decide which room to open.

**Anti-pattern**: No recent message preview.

---

### [INFO-CHAT-003] Show chat timestamps
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Chat/social metadata

**Principle**: Chat list items must display the date or time of the most recent message.

**Why**: Recency awareness.

**Anti-pattern**: No chat timestamp displayed.

---

### [INFO-CHAT-004] Show senders in group chat
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: In group chats, display each message with the sender's profile image and nickname (or ID).

**Why**: Multiple participants require identification.

**Anti-pattern**: Group chat with no sender information.

---

### [INFO-CHAT-005] Show group member count
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: Group chat room items should display the current participant count so users can grasp the room's size at a glance.

**Why**: Room-identifying information.

**Anti-pattern**: No member count shown for group chats.

---

### [INFO-CHAT-006] Support custom room names
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: Support user-defined chat room names; in group or purpose-based chats especially, the room title is the key means of identification.

**Why**: Preserves context.

**Anti-pattern**: Group chat name limited to participant nicknames only.

---

### [INFO-CHAT-007] Participant management
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: If group chat exists, provide both participant invite and remove functions.

**Why**: Basic for group operation.

**Anti-pattern**: Invites supported but no remove function.

---

### [INFO-CHAT-008] Show multiple participant profiles
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: In multi-participant chat rooms, surface multiple profile images in overlapping form or display the participant count alongside.

**Why**: Visibility of multi-participation.

**Anti-pattern**: Only one person's profile displayed.

---

### [INFO-CHAT-009] Chat room settings menu
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: Provide a chat room settings menu that includes renaming the room, managing participants, and listing shared media or files.

**Why**: Standard for room management.

**Anti-pattern**: No chat room settings menu.

---

### [INFO-CHAT-010] Group AI chat exchange modules
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: In AI chats, group question, processing, and answer into a single conversation module (card) so the information structure becomes clear.

**Why**: Recognizes the conversation unit.

**Anti-pattern**: Question, answer, and processing scattered apart.

---

### [INFO-CHAT-011] Left/right alignment in AI chat
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: In chat-style AI interfaces, distinguish user messages and AI responses clearly by left/right alignment or background color; do not use center alignment, which causes confusion.

**Why**: Messenger standard.

**Anti-pattern**: All messages center-aligned in AI chat.

---

### [INFO-CHAT-012] Travel card = date + party size
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: Content cards must include the key metadata needed for decision-making, such as date and time.

**Why**: Decision-making information.

**Anti-pattern**: Travel room card with no date.

---

### [INFO-CHAT-013] State group participant count
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Chat/social metadata

**Principle**: In group or room participation services, state the current participant count on the card.

**Why**: Core room information.

**Anti-pattern**: Room card with no participant count.

---

## Planning first (13 canonical)

### [INFO-PLAN-001] Plan before designing
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Planning first

**Principle**: Before starting UI design, first plan each screen's policies, interaction cases, and required functions.

**Why**: Without planning, omissions cause incidents.

**Anti-pattern**: Starting from visuals in Figma.

---

### [INFO-PLAN-002] IA/flow diagrams
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Include IA or user flow diagrams in portfolio and collaboration files to make screen-to-screen connections explicit.

**Why**: Helps understanding of structure.

**Anti-pattern**: Scattering screens only, with no flow.

---

### [INFO-PLAN-003] Provide organized documents
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: When sharing design files, present the IA (information architecture map) or flow diagram first so the overall flow can be grasped at a glance.

**Why**: Review efficiency.

**Anti-pattern**: Figma pages scattered in all directions.

---

### [INFO-PLAN-004] Full-case design
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Document UX as a full set of cases that includes detailed states (success, failure, in-progress, disabled, etc.) beyond the main screens.

**Why**: Edge cases are part of real usage.

**Anti-pattern**: Designing only the major screens with no detailed cases.

---

### [INFO-PLAN-005] Guide consistency is the system
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Continually align minor UI details across pages; breaking the guide on a single page collapses the whole system.

**Why**: The guide is consistency.

**Anti-pattern**: Each page following a slightly different guide.

---

### [INFO-PLAN-006] Consistency for maintainability
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Strictly enforce guide consistency from the initial design stage with maintenance in mind.

**Why**: Early breakdown becomes a later time bomb.

**Anti-pattern**: Loose at the start, plan to fix later.

---

### [INFO-PLAN-007] Composition and flow over visuals
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Judge design completeness by how thoroughly usable cases are covered rather than visual beauty.

**Why**: Usability first.

**Anti-pattern**: Building only pretty screens with many missing functions.

---

### [INFO-PLAN-008] Always provide alternatives when removing a function
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: When removing a function, first design an alternative solution for the user scenarios that needed it.

**Why**: Removal does not equal a solution.

**Anti-pattern**: Wiping everything because it's complex.

---

### [INFO-PLAN-009] Decide based on user needs
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Decisions to remove functions in UX design must be based on actual user need, not the designer's personal preference.

**Why**: User perspective.

**Anti-pattern**: Removing because I personally would not use it.

---

### [INFO-PLAN-010] Benchmarking is pattern analysis
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: Before designing UI in a new domain, thoroughly analyze and understand the domain's standard patterns and references first.

**Why**: Standards reduce learning cost.

**Anti-pattern**: Center-aligning AI chat without analyzing the pattern.

---

### [INFO-PLAN-011] Follow domain standards
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: For authentication method selection, following industry standard patterns (tabs or radios within a single screen) reduces user learning cost.

**Why**: Unfamiliar patterns are a burden.

**Anti-pattern**: A custom pattern that diverges from the domain standard.

---

### [INFO-PLAN-013] Identification scheme for multiple accounts
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Planning first

**Principle**: In the password recovery flow, review with service policy whether the authentication method is sufficient for account identification. If multiple accounts can exist under the same method, request additional identifying information.

**Why**: Confirms the user's identity.

**Anti-pattern**: Recovering password by phone number alone.

---

### [INFO-PLAN-014] Require ID input (identification)
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Planning first

**Principle**: In services where the ID and email are separate, include an ID input field during password recovery to identify the user.

**Why**: Identification is security.

**Anti-pattern**: No ID field in password recovery.

---

## Page purpose (8 canonical)

### [INFO-PURPOSE-001] Focus on the core purpose
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Page purpose

**Principle**: Identify the page's core purpose and decide the layout and decorative elements to focus on that purpose as much as possible.

**Why**: Once the purpose blurs, everything becomes noise.

**Anti-pattern**: A map page filled with cards and decorations.

---

### [INFO-PURPOSE-002] Every page needs a reason to exist
- **Platform**: Mobile
- **Frequency weight**: 4
- **Sub-category**: Page purpose

**Principle**: Every page or section must have a clear reason to exist. If the designer cannot answer 'why is this page needed,' redesign or remove the element.

**Why**: Pages without a reason are noise.

**Anti-pattern**: A page that just shows a project difficulty indicator.

---

### [INFO-PURPOSE-003] Design payment like a receipt
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Page purpose

**Principle**: Design the payment summary screen as intuitively as a receipt. Total amount, discount details, and final payment amount must read clearly in hierarchy.

**Why**: Familiar receipt pattern.

**Anti-pattern**: Payment information listed flatly with no hierarchy.

---

### [INFO-PURPOSE-004] Payment screens emphasize the amount
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Page purpose

**Principle**: On the final payment step, 'how much I am paying and why' is the top information. Place total amount, discount details, and benefit information up front rather than the product image.

**Why**: For payment, the amount is the core.

**Anti-pattern**: Emphasizing a large thumbnail on the final payment step.

---

### [INFO-PURPOSE-005] Use simple boxes on information pages
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Page purpose

**Principle**: On information-focused pages, a simple box layout is more effective. Remove distinctive design elements if they hinder information readability.

**Why**: Distinctiveness ranks below readability.

**Anti-pattern**: A folder-style design on an information page.

---

### [INFO-PURPOSE-006] Readability over distinctiveness
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Page purpose

**Principle**: Remove distinctive UI patterns boldly if they hinder information delivery. Content readability always takes priority over design originality.

**Why**: Design is a means of conveying information.

**Anti-pattern**: A distinctive pattern that hides the information.

---

### [INFO-PURPOSE-007] Top priority: price visibility on payment pages
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Page purpose

**Principle**: On payment pages, place the price at the largest and most visible position. Users are sensitive to price, so price visibility is the top priority.

**Why**: Price is decision-critical information.

**Anti-pattern**: Price shown small in the top-left of a folder.

---

### [INFO-PURPOSE-008] Product detail: structure and logic first
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Page purpose

**Principle**: For product detail pages, design the information structure, usage flow, hierarchy, and component roles before the visual design.

**Why**: A page that holds a complex UX flow.

**Anti-pattern**: Worrying only about a pretty screen.

---

## Menu/navigation structure (12 canonical)

### [INFO-NAV-001] Review drawer menu by context
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Provide back and home icons by default on the GNB of product detail pages. A drawer menu is unnecessary in the product detail context.

**Why**: GNB matched to context.

**Anti-pattern**: A hamburger menu on a product detail page.

---

### [INFO-NAV-002] Provide back and home separately
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Provide back and home icons separately. Back navigates to the previous page and home enters the main page; the roles differ, and both are needed.

**Why**: Different functions.

**Anti-pattern**: Using the same icon for back and home.

---

### [INFO-NAV-003] Simplify GNB on sub-pages
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: On sub-screens, use a simplified top bar (including back navigation) appropriate to that screen instead of the main GNB.

**Why**: Sub-screens stay simple.

**Anti-pattern**: Keeping the main GNB intact on sub-screens.

---

### [INFO-NAV-004] Tab bar is not for every page
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: The bottom tab bar should not follow every screen by default; consider removing it on sub-screens.

**Why**: Depends on context.

**Anti-pattern**: Main tab bar appearing on sub-screens too.

---

### [INFO-NAV-005] Consistent rules for GNB and tab bar
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Decide whether to keep the main GNB and bottom tab bar on sub-pages intentionally based on screen nature (modal, flow, sub, etc.), and maintain consistency across pages.

**Why**: Mixed treatment causes confusion.

**Anti-pattern**: GNB handled differently on each sub-screen.

---

### [INFO-NAV-006] Consolidate categories with tabs
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: It is efficient to bundle similar categories or content with a tab UI and consolidate them into a single section.

**Why**: Saves space and improves clarity.

**Anti-pattern**: Keeping similar sections apart.

---

### [INFO-NAV-007] Separate content with tabs
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Separate content with clearly distinct categories into tabs so users can immediately recognize and switch between each area.

**Why**: Tabs deliver clear separation.

**Anti-pattern**: 'In progress' and 'hidden' listed vertically.

---

### [INFO-NAV-008] Separate sections with dividers or chips
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Clearly separate two sections of different nature with stroke dividers or label chips.

**Why**: A visual signal for grouping.

**Anti-pattern**: No separation between search results and recommended products.

---

### [INFO-NAV-009] Use chips for section labels
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Display section labels clearly with chip (tag) components to improve readability and information structure.

**Why**: Chips form a visual unit.

**Anti-pattern**: Section labels rendered as plain text.

---

### [INFO-NAV-010] No missing titles in split layouts
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: When splitting a layout left/right or top/bottom, always provide a title or label that clarifies the meaning of each area.

**Why**: Splitting needs a basis.

**Anti-pattern**: A left/right split with no titles.

---

### [INFO-NAV-011] Separate action button placement
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Action buttons (add, delete, etc.) must be visually distinct from list items. Place them at the end position or differentiate them with a separate style.

**Why**: An action is not an item.

**Anti-pattern**: An add button that looks like a menu name.

---

### [INFO-NAV-012] Review the reason for a title
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Menu/navigation structure

**Principle**: Top-of-UI labels and titles must have a clear reason to exist. If they merely display the page name, consider omitting them.

**Why**: Text without a reason is noise.

**Anti-pattern**: A 'Shorts' label at the top of a Shorts page.

---

## Miscellaneous (11 canonical)

### [INFO-MISC-001] Use numbering only when order matters
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Use numbering only when users need to perceive order. Unnecessary numbering on simple lists or product enumerations complicates the information hierarchy.

**Why**: Numbering with a reason.

**Anti-pattern**: 1, 2, 3 numbers on a product enumeration.

---

### [INFO-MISC-002] Distinguish cart vs favorite
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Cart and favorite have different storage logic and login requirements. Design them separately and distinguish them clearly in the UI.

**Why**: Different functions.

**Anti-pattern**: Treating cart and favorite as the same.

---

### [INFO-MISC-003] Separate non-map actions
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Move function buttons that do not belong to the map UI (favorite, share, etc.) outside the map and place them in the text content area to clarify their roles.

**Why**: Context separation.

**Anti-pattern**: A favorite icon placed on top of the map.

---

### [INFO-MISC-004] Map controls vs content actions
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Place only map control functions as icons on the map; separate content action buttons such as favorite or share into the information text area.

**Why**: Areas by function.

**Anti-pattern**: Map and content actions mixed together.

---

### [INFO-MISC-005] Tables are more efficient
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: List data with repeating attributes is more efficient and more readable as a table than as cards.

**Why**: Repetition belongs in a table.

**Anti-pattern**: Showing class times as cards.

---

### [INFO-MISC-006] Match icons to their meaning
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Icons must convey meaning that fits the context. Carelessly using icons that imply a different meaning can confuse users.

**Why**: Meaning is the signal.

**Anti-pattern**: Using an exclamation mark (a warning) on general information.

---

### [INFO-MISC-007] Use visual differentiators
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Miscellaneous

**Principle**: Use visual differentiators such as color or icons together with state changes or key information points to improve readability.

**Why**: Text alone is weak.

**Anti-pattern**: Conveying transfer information by text alone.

---

### [INFO-MISC-008] Text leads, graphic supports
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: In banners, text must be able to convey the information on its own; graphics are supporting elements that lose meaning without text.

**Why**: Text is the core of information.

**Anti-pattern**: Trying to convey the service through graphics alone.

---

### [INFO-MISC-009] Four-tier banner information hierarchy
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Prioritize banner information hierarchy in the order brand identification -> core benefit -> detailed benefit -> additional conditions.

**Why**: Information flow.

**Anti-pattern**: Banner information arranged without regard to hierarchy.

---

### [INFO-MISC-010] Rebalance visual weight at payment
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Decide the importance of each screen's elements based on the steps the user took to arrive there. Information already verified multiple times can carry less weight on that screen.

**Why**: Importance by context.

**Anti-pattern**: A large thumbnail even on the order form.

---

### [INFO-MISC-013] Screens without planning are meaningless
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Miscellaneous

**Principle**: Design work must proceed after planning (usage flow, required functions, case definitions) is done. A design produced without planning becomes an unusable artifact.

**Why**: Planning is the foundation.

**Anti-pattern**: Drawing only screens with no planning.

---

## User flow (10 canonical)

### [INFO-FLOW-002] Result screen for the authentication flow
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: User flow

**Principle**: The authentication flow must give users feedback on the result (showing the recovered ID, confirming the send, etc.) to feel complete.

**Why**: Without a result, the flow feels unfinished.

**Anti-pattern**: The recovery screen ending with no result.

---

### [INFO-FLOW-003] Design the user's gaze flow first
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: When designing, think about 'in what order the user reads' before 'pretty arrangement.' Begin design from the user's gaze flow rather than a visual approach.

**Why**: Visuals without structure collapse.

**Anti-pattern**: Starting from a pretty card layout.

---

### [INFO-FLOW-004] Build structure first, then design
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: For complex information layouts, design the information structure and user flow first, before the visuals.

**Why**: Structure is the skeleton.

**Anti-pattern**: Drawing screens first in Figma.

---

### [INFO-FLOW-005] Temporary password to reset is standard
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: Auto-navigating to a password reset screen when logging in with a temporary password is the standard security flow and must be included in the design.

**Why**: A security standard.

**Anti-pattern**: Continuing to use the account after logging in with a temporary password.

---

### [INFO-FLOW-006] After password recovery: send temp or reset
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: After completing password recovery, always connect to a notice that a temporary password was sent or to a password reset screen.

**Why**: Prevents a broken flow.

**Anti-pattern**: No next step after password recovery.

---

### [INFO-FLOW-007] Place CTA after context
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: Place the CTA button where users naturally proceed to action after encountering enough context.

**Why**: A CTA without context will not be clicked.

**Anti-pattern**: A More button before the user has seen the content.

---

### [INFO-FLOW-008] No unnecessary elements in the purchase flow
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: In flows where task completion matters, such as purchase and payment, remove unnecessary visual elements and design so that only the truly necessary remains visible.

**Why**: Task completion comes first.

**Anti-pattern**: Ads or promotions on the payment page.

---

### [INFO-FLOW-009] Choose multi-method authentication on one screen
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: In authentication flows that support multiple methods (email, mobile, etc.), offer the method choices within a single screen using radios or tabs.

**Why**: Splitting choices increases learning cost.

**Anti-pattern**: Email recovery and phone recovery on separate screens.

---

### [INFO-FLOW-010] Select first, then branch
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: If a flow requires the user to choose one of several methods, present the choices first or complete the selection before branching.

**Why**: Branching after selection stays clean.

**Anti-pattern**: Only a recovery button with no indication of which method.

---

### [INFO-FLOW-011] Sign-up entry path
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: User flow

**Principle**: The login screen must always provide a path to sign-up.

**Why**: Entry for new users.

**Anti-pattern**: No sign-up link on the login screen.

---

## Card structure (8 canonical)

### [INFO-CARD-001] Card information order matches decision flow
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Card structure

**Principle**: The information order on a card must follow the user's decision-making flow. On travel or lodging cards, the price should catch the eye before the star rating.

**Why**: Decision information first.

**Anti-pattern**: Star rating emphasized over the price.

---

### [INFO-CARD-002] Use list view for high information volume
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Card structure

**Principle**: Cards with high information volume (image + price + rating + tags, etc.) accommodate the information far more easily in a horizontal list view than in a grid view.

**Why**: Grid favors visuals; list favors information.

**Anti-pattern**: Information-dense cards in a grid.

---

### [INFO-CARD-003] Lead with the content subject
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Card structure

**Principle**: On content cards, place what the user must know first (the subject or purpose) at the top.

**Why**: The subject is the first recognition.

**Anti-pattern**: Instructor card where the instructor sits at the bottom.

---

### [INFO-CARD-004] Include a summary on article cards
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Card structure

**Principle**: Provide at least a minimum summary (headline, lead, etc.) on article cards. Too little information prevents users from deciding whether to enter.

**Why**: Aids the decision.

**Anti-pattern**: Article cards with title only.

---

### [INFO-CARD-005] Keep the top of the card simple
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Card structure

**Principle**: Keep the top of the card simple, focused on core content (title, image), and move auxiliary actions (share, favorite) to the bottom or a supporting area.

**Why**: A complex top area creates cognitive load.

**Anti-pattern**: Top of the card crowded with source, share, and heart.

---

### [INFO-CARD-006] Appropriate hierarchy for metadata
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Card structure

**Principle**: UI elements must be prioritized in the order of importance to the user. Putting supplementary information at the very top reduces the visibility of the actual core content.

**Why**: The source ranks below the content.

**Anti-pattern**: Vendor information emphasized at the very top of the card.

---

### [INFO-CARD-007] Standard order for social actions
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Card structure

**Principle**: Social action buttons conventionally follow the order like/favorite -> share -> more.

**Why**: Order by usage frequency.

**Anti-pattern**: Share before favorite.

---

### [INFO-CARD-008] Visual anchor at conventional position
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Card structure

**Principle**: Place badges and status indicators where the user's eye lands first (such as top-left). Following conventional positions benefits readability.

**Why**: Conventional positions reduce learning cost.

**Anti-pattern**: A live badge in a non-conventional position.

---

## Portfolio-specific (10 canonical)

### [INFO-PORT-001] Portfolio means information and readability
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: On a portfolio profile page, information and readability matter most. Information delivery takes priority over appearance or photo styling.

**Why**: What interviewers care about.

**Anti-pattern**: Emphasizing a large portrait photo.

---

### [INFO-PORT-002] Reduce weight of obvious information
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: On a portfolio, lower the weight of items every role is presumed to have (e.g., design tools for a designer) or remove them. Allocate area to your unique appeal points.

**Why**: Give space to differentiation.

**Anti-pattern**: Heavily emphasizing Figma/PS proficiency.

---

### [INFO-PORT-003] Consistent chronological order in history
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: Sort time-based information such as history, experience, and certifications consistently as either newest-first or oldest-first.

**Why**: Chronological order helps readability.

**Anti-pattern**: Years jumping around like '21 -> '23 -> '20.

---

### [INFO-PORT-004] Story arc with setup, development, turn, and resolution
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: Present design changes in a portfolio in the narrative structure 'existing problem -> direction of solution -> outcome.' Designs without context are unpersuasive.

**Why**: The reason for change is the value.

**Anti-pattern**: Showing only the to-be design in isolation.

---

### [INFO-PORT-005] Portfolio needs quantity and quality
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: A portfolio must show a sufficient amount of designs and information together. Focusing solely on publishing quality with thin content fails to prove design skill.

**Why**: Both quantity and quality.

**Anti-pattern**: Crafting just five pages and stopping there.

---

### [INFO-PORT-006] Build the table of contents by category
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: Compose the portfolio table of contents by top-level category (web design, mobile design, etc.), not by page type (main/sub/my). Excessive subdivision looks like padding.

**Why**: Meaningful categories.

**Anti-pattern**: Categorizing as main page / sub page.

---

### [INFO-PORT-007] Structure thinking over visuals
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: When making a portfolio, invest more time in how to structure it (planning ability) than in visual decoration. Even with flashy form, weak structure is unpersuasive.

**Why**: Structure is planning ability.

**Anti-pattern**: Spending 90% of time on decoration.

---

### [INFO-PORT-008] Layout follows information volume
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: When choosing a layout pattern, consider the information volume in each item. High-volume items should use a simple, linear arrangement.

**Why**: Information volume determines form.

**Anti-pattern**: Information-heavy items arranged in a zig-zag.

---

### [INFO-PORT-009] Make timeline markers clear
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: On timelines or sequential structures, visualize each item's branch point (marker) clearly. Without them, users struggle to understand the structure.

**Why**: Structural recognition.

**Anti-pattern**: A timeline with no markers.

---

### [INFO-PORT-010] Linear arrangement is the natural gaze flow
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Portfolio-specific

**Principle**: Linear arrangements (left-to-right, top-to-bottom) match the user's natural gaze flow, so the order is intuitive without numbering. The more non-linear the arrangement, the more explicit ordering such as numbering is needed.

**Why**: Standard gaze flow.

**Anti-pattern**: Emphasizing numbering on a linear layout.

---

## Progressive disclosure (7 canonical)

### [INFO-DISCLOSE-001] Reveal at the moment of need
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Progressive disclosure

**Principle**: Reveal information at the moment it is needed. Use interactions such as hover, collapse/expand, and pagination to reduce the initial information load and show more when the user wants it.

**Why**: Design the moment of exposure.

**Anti-pattern**: All information exposed at all times.

---

### [INFO-DISCLOSE-002] Default accordions to collapsed
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Progressive disclosure

**Principle**: Set information-rich accordion structures to collapsed by default and leave only key items expanded to reduce information overload.

**Why**: The default state is what users see most often.

**Anti-pattern**: All plans expanded by default.

---

### [INFO-DISCLOSE-003] Expand the recommended plan
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Progressive disclosure

**Principle**: In a pricing comparison UI, expose the recommended plan's details by default and leave the others collapsed to heighten visual focus.

**Why**: Expand only what you want to emphasize.

**Anti-pattern**: All plans collapsed.

---

### [INFO-DISCLOSE-004] Expand everything for comparison
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Progressive disclosure

**Principle**: On the pricing selection screen, expand the benefits of every plan so users can compare easily.

**Why**: Comparison requires simultaneous exposure.

**Anti-pattern**: Everything collapsed even though the screen is for comparison.

---

### [INFO-DISCLOSE-005] Show titles only
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Progressive disclosure

**Principle**: When the information volume is high, use progressive disclosure: show titles only at first and expand the details on click or tap.

**Why**: Prevents information overload.

**Anti-pattern**: Exposing every detail from the start.

---

### [INFO-DISCLOSE-006] Strip back text
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Progressive disclosure

**Principle**: When whitespace is hard to create, hiding or removing text is also a valid method. Stripping back text is the fastest way to give the design room to breathe.

**Why**: Removal quickly improves readability.

**Anti-pattern**: Insisting on keeping all the text.

---

### [INFO-DISCLOSE-007] Reveal progressively with 'See more'
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Progressive disclosure

**Principle**: When the item count is moderate, showing some first and expanding the rest via 'See more' makes exploration easier.

**Why**: Foreshadowing plus curiosity.

**Anti-pattern**: Showing everything from the start.

---

## Information density (8 canonical)

### [INFO-DENSITY-001] More information does not mean readability
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: The more information you pack into one screen, the lower the readability. True readability rises only when you reduce information and secure whitespace.

**Why**: Information overload.

**Anti-pattern**: Exposing all information on a single screen.

---

### [INFO-DENSITY-002] Too much information is not seen
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: Showing more information is not always better. Strongly exposing one key item and hiding the rest in slides or tabs benefits readability.

**Why**: Selection and focus.

**Anti-pattern**: Spraying out all the information so none of it is seen.

---

### [INFO-DENSITY-003] Reduce sections on the main page
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: Show only a few key sections on the main page and remove unnecessary ones to heighten focus.

**Why**: Selection and focus.

**Anti-pattern**: Twelve sections on the main page.

---

### [INFO-DENSITY-004] Main page: key sections plus repeating patterns
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: Modern main pages trend toward showing only key sections concisely and composing them with repeating layout patterns.

**Why**: Main page trend.

**Anti-pattern**: Every kind of section on the main page.

---

### [INFO-DENSITY-005] Premium design reduces information
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: The more premium the design, the more you should reduce visible information and secure broad whitespace.

**Why**: Premium means restraint.

**Anti-pattern**: Information packed tightly in a luxury section.

---

### [INFO-DENSITY-006] If the first impression is 'too much,' revisit it
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: A design that gives the first impression of 'too much' needs an information-structure review. Adjust information density to lower cognitive load.

**Why**: Intuition is a signal.

**Anti-pattern**: A dashboard packed with information.

---

### [INFO-DENSITY-007] Reduce and organize information
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: For simple, premium design, an editing process that abbreviates and organizes elements down to only what is truly needed is essential.

**Why**: Editing is the core of design.

**Anti-pattern**: A 'just include everything' mindset.

---

### [INFO-DENSITY-008] A single-line body has no meaning
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Information density

**Principle**: When showing body text in a list, at least 2-3 lines are needed for it to be meaningful. If only one line is shown, it is better to drop it boldly.

**Why**: A single line carries low information value.

**Anti-pattern**: A one-line body preview.

---

## Data visualization (5 canonical)

### [INFO-VIZ-001] Convey chart meaning instantly
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: Every chart, through its title, axis labels, and legend, should let readers understand what the data means immediately, without extra explanation.

**Why**: The purpose of a chart.

**Anti-pattern**: A bar chart with no labels.

---

### [INFO-VIZ-002] Show baseline lines on charts
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: Data graphs need horizontal baseline lines matched to the value units so users can intuitively perceive a value's position.

**Why**: Perceives relative position.

**Anti-pattern**: Graphs with no baseline lines.

---

### [INFO-VIZ-003] Show change with a graph
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: For data where comparison matters, such as up/down trends, use graphs or charts so it can be grasped at a glance.

**Why**: Intuitive comparison.

**Anti-pattern**: Indicating change with text only.

---

### [INFO-VIZ-004] Charts must convey the key message at a glance
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: Design data visualization by the standard 'is the key message visible at a glance,' and prioritize a simple structure that reads major patterns immediately over fine details.

**Why**: Simplicity enables fast recognition.

**Anti-pattern**: A chart filled with complex information.

---

### [INFO-VIZ-005] Progress bar value position
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: Place the progress bar value (percentage) directly above the bar's progress point so the current state is intuitively recognizable.

**Why**: Position equals meaning.

**Anti-pattern**: Percentage value placed at the end.

---

## Payment grouping (2 canonical)

### [INFO-PAY-001] Payment and discount in one group
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Payment grouping

**Principle**: Bundle payment amount and discount items into one group, and separate items of different nature like point accrual into their own group.

**Why**: Logical flow defines the group.

**Anti-pattern**: Bundling discount and point accrual together.

---

### [INFO-PAY-002] Payment receipt flow
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Payment grouping

**Principle**: Compose the payment summary section in the logical flow 'product amount - discount = final payment amount, and then point accrual.'

**Why**: The receipt format users are familiar with.

**Anti-pattern**: Payment information in an illogical order.

---
