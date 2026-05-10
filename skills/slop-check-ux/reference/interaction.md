# Interaction (UX)

Button interaction, modal, feedback, behavior rules

- **Total canonical rules**: 122
- **Sub-categories**: 11

---

## Contents
- Interaction patterns — 35 canonical
- Missing features / Edge cases — 19 canonical
- Affordance / Touch — 13 canonical
- Input — 12 canonical
- State expression — 8 canonical
- Feedback — 9 canonical
- Navigation — 10 canonical
- Add/Remove symmetry — 5 canonical
- Motion — 5 canonical
- Missing or duplicate cases — 4 canonical
- Hover vs. Click — 2 canonical

---

## Interaction patterns (35 canonical)

### [INTER-PATTERN-001] Unify identical patterns
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Interaction patterns

**Principle**: When the same interaction pattern (e.g., a slider) repeats across multiple sections, unify it into a single consistent UX model.

**Why**: Pattern consistency reduces learning cost.

**Anti-pattern**: Different slider controls in every section.

---

### [INTER-PATTERN-002] Confirm on the right, cancel on the left
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Place the confirm (positive) button on the right and the cancel (negative) button on the left to match common user mental models. Reversing this invites mistakes.

**Why**: A spatial metaphor rooted in everyday experience.

**Anti-pattern**: Confirm on the left and cancel on the right (reversed).

---

### [INTER-PATTERN-003] Right means positive, left means negative
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Interaction patterns

**Principle**: Apply the spatial metaphor — right/forward signals positive progress, left/back signals negative retreat — consistently when designing UI direction.

**Why**: A mental model drawn from everyday user experience.

**Anti-pattern**: Next button on the left, back button on the right.

---

### [INTER-PATTERN-004] Choose popup patterns by context
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Choose UI patterns (bottom sheet, modal, etc.) based on content volume and context, not because they are trendy.

**Why**: Patterns are tools; using them without purpose creates noise.

**Anti-pattern**: Adopting a bottom sheet just because other apps use one.

---

### [INTER-PATTERN-005] Use inline popovers for small content
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: For lightweight popups, use an inline popover or small overlay instead of a modal or bottom sheet that blocks the background, so users keep their context.

**Why**: Covering the full screen breaks the user's flow.

**Anti-pattern**: Showing a three-option menu inside a full-screen modal.

---

### [INTER-PATTERN-006] Use a full popup for large content
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When a bottom sheet would cover most of the screen, use a full-screen modal instead. Bottom sheets are best for partial information.

**Why**: Match the pattern to the volume of content.

**Anti-pattern**: A bottom sheet that covers almost the entire screen.

---

### [INTER-PATTERN-007] Use a single arrow for simple toggles
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Express simple toggle interactions like accordions with a single arrow icon. Avoid adding unnecessary UI elements.

**Why**: Simple actions deserve simple cues.

**Anti-pattern**: Using complex UI controls for collapse/expand.

---

### [INTER-PATTERN-008] Allow multi-expand for comparison UI
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When the UI is meant for comparison, use multi-expand instead of an accordion so users can compare items side by side.

**Why**: Accordions make comparison impossible.

**Anti-pattern**: Comparing pricing plans inside an accordion, preventing side-by-side review.

---

### [INTER-PATTERN-009] Show details in a layer popup
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Show detail content in a layer popup rather than pushing the layout downward; this preserves the existing layout and feels cleaner.

**Why**: Pushing content down destabilizes the layout.

**Anti-pattern**: Clicking a team member pushes details inline and shifts the layout.

---

### [INTER-PATTERN-010] Expand all at once or use an accordion
- **Platform**: PC
- **Frequency weight**: 3
- **Sub-category**: Interaction patterns

**Principle**: For expandable content, open and close everything at once or use an accordion that opens only one item at a time. This is more stable than toggling each item individually.

**Why**: Constant opening and closing creates visual chaos.

**Anti-pattern**: Each item expands individually, causing the layout to jump.

---

### [INTER-PATTERN-011] Provide a collapse-all action when multi-expand is allowed
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Interfaces that allow multiple expanded panels must include a 'collapse all' or batch-close action to remain usable.

**Why**: Closing items one by one is a burden.

**Anti-pattern**: Five videos are all expanded but there is no collapse-all option.

---

### [INTER-PATTERN-012] Move one tab at a time when there are many tabs
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When there are many tabs, advancing one position per tap is easier to use than scrolling through them with a swipe.

**Why**: Precise navigation is faster.

**Anti-pattern**: Browsing twenty tabs with sliding only.

---

### [INTER-PATTERN-013] Place carousel indicators at the bottom
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Place slider or carousel indicators at the bottom rather than the top so users recognize them intuitively.

**Why**: The bottom is the standard position for indicators.

**Anti-pattern**: Placing carousel indicators at the top.

---

### [INTER-PATTERN-014] Indicators teach that the slider can be swiped
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: For image sliders, prefer indicator dots over left/right arrows. The dots themselves teach that the content is swipeable, so arrows may be unnecessary.

**Why**: Indicators alone are a sufficient affordance.

**Anti-pattern**: Arrows but no indicators, leaving the user unaware of the total count.

---

### [INTER-PATTERN-015] Mobile sliders rely on swipe
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Avoid left/right arrow navigation in mobile UI. Replace it with swipe gestures and indicators.

**Why**: On mobile, the finger is the natural interface.

**Anti-pattern**: Left/right arrows on a mobile image slider.

---

### [INTER-PATTERN-016] Provide a Top button on long-scrolling screens
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Interaction patterns

**Principle**: On screens with long-scrolling content, provide a Top button so users can jump back to the top quickly.

**Why**: Returning to the top after a long scroll is a very common action.

**Anti-pattern**: A long chat screen with no Top button.

---

### [INTER-PATTERN-017] Swap direction buttons by scroll position
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: On long content screens, swap up/down direction buttons in and out depending on the current scroll position.

**Why**: Showing only the relevant direction reduces cognitive load.

**Anti-pattern**: The Top button is shown even at the very top of the page.

---

### [INTER-PATTERN-018] Auto-slide beats static stacking
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When listing many items such as promotional banners, an auto-sliding carousel beats stacking them statically — both for space efficiency and user experience.

**Why**: It compresses space and uses time well.

**Anti-pattern**: Stacking five banners vertically all at once.

---

### [INTER-PATTERN-019] Do not slide a small number of items
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Interaction patterns

**Principle**: When there are only a few products or items, showing them all on one screen is more intuitive than putting them in a slider.

**Why**: Sliding through three to five items is overkill.

**Anti-pattern**: Putting three recommended products into a slider.

---

### [INTER-PATTERN-020] Use a grid or expanded layout for few options
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When there are only a few items (eight or fewer), revealing them all at once in a grid or expanded layout is better than a slider.

**Why**: Immediate exposure is faster than navigation.

**Anti-pattern**: Showing five categories only through a slider.

---

### [INTER-PATTERN-021] Let sliders peek at the next item
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Interaction patterns

**Principle**: Horizontal sliders should peek the next item at the screen edge so users intuitively recognize that the content is swipeable.

**Why**: Showing a sliver signals that more content exists.

**Anti-pattern**: Cutting slider content cleanly at the grid boundary.

---

### [INTER-PATTERN-022] No expand button on scroll-loading screens
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When content loads through infinite scroll or pagination, a separate 'expand' action is unnecessary; let scrolling handle it instead.

**Why**: Modern UX is scroll-first.

**Anti-pattern**: An 'expand' button at the end of a feed.

---

### [INTER-PATTERN-023] Show quantity controls at the action moment
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: On mobile product detail pages, expose quantity controls at the moment of purchase or add-to-cart, or handle them in the cart itself — that flow feels more natural.

**Why**: Detail pages are for exploring information; quantity follows the decision.

**Anti-pattern**: Quantity +/- buttons always visible on the product detail page.

---

### [INTER-PATTERN-024] Calendar UI: arrows for months, layer for direct selection
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: In calendar UI, navigate months with arrows but offer a layer for picking year/month directly. This dramatically improves UX.

**Why**: Tapping the arrow 120 times to reach a date ten years ago is unreasonable.

**Anti-pattern**: Only month-by-month arrows, no way to jump years.

---

### [INTER-PATTERN-025] Highlight the entire calendar day cell
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: When a date is selected in a calendar, fill the entire cell background to mark selection clearly. This is the most intuitive treatment.

**Why**: A full cell fill is clearer than a small dot or underline.

**Anti-pattern**: Marking the selected date with only a small dot.

---

### [INTER-PATTERN-026] Start large calendars in a collapsed state
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Show large UI elements such as calendars or date pickers in a collapsed state on entry, and consider expanding them via a bottom sheet on tap.

**Why**: If the default state fills the screen, other content disappears.

**Anti-pattern**: Entering with the calendar expanded so the content below is hidden.

---

### [INTER-PATTERN-027] Prevent collisions on tab transitions
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Design spacing and placement up front for interaction scenarios so components don't collide with surrounding elements when they move or change state.

**Why**: A static layout can look fine but collide once it animates.

**Anti-pattern**: Tabs collide with header elements when they slide up.

---

### [INTER-PATTERN-028] Sticky bar — design cases for each scroll position
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Design how a sticky bottom bar handles duplicate information at different scroll positions. For example, hide the amount on the bar when the payment-amount section is visible, or swap its text.

**Why**: Duplicate information adds cognitive load.

**Anti-pattern**: Showing the same amount in both the payment section and the bottom bar.

---

### [INTER-PATTERN-029] Mobile checkout CTA stays sticky at the bottom
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: On mobile checkout pages, the primary CTA (such as 'Pay') should be sticky at the bottom and always reachable.

**Why**: Checkout pages are long; the action must be tappable from anywhere.

**Anti-pattern**: The Pay button only sits at the very bottom of the page.

---

### [INTER-PATTERN-030] Reveal card details on hover
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Interaction patterns

**Principle**: Hide detailed text inside a card by default and reveal it on hover. This keeps the initial layout light and invites exploration.

**Why**: The default state is the most frequently seen state.

**Anti-pattern**: Showing every piece of information on the card all the time.

---

### [INTER-PATTERN-031] Hide secondary actions until hover
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Reveal secondary actions like share or bookmark only on hover so the content stays the focus.

**Why**: The default state is the most frequently seen state.

**Anti-pattern**: Share icons always shown on every card.

---

### [INTER-PATTERN-032] Light default tone, emphasized on hover
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Keep the button's default tone soft so it balances with surrounding content, then escalate to a strong color on hover or click for feedback.

**Why**: Emphasizing every default state causes conflicts across the screen.

**Anti-pattern**: Strong solid color from the default state, leaving no contrast on hover.

---

### [INTER-PATTERN-033] Default to stroke, hover to solid
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: To preserve brand color while reducing visual weight, use a stroke button by default and fill it with color on hover.

**Why**: Restrained default plus a clear hover signal.

**Anti-pattern**: Filling the button with color from the default state.

---

### [INTER-PATTERN-034] Hide auxiliary info until hover (dashboards)
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Instead of treating auxiliary info as a strong button by default, reveal it on hover. The interface looks less cluttered.

**Why**: Controlling when something appears is a powerful tool.

**Anti-pattern**: The notification badge in the global nav is always styled as an emphasized button.

---

### [INTER-PATTERN-035] Hide auxiliary functions by default
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Interaction patterns

**Principle**: Hide auxiliary buttons such as download by default and surface them on hover to keep the UI clean.

**Why**: Showing rarely used functions by default is noise.

**Anti-pattern**: A download button always visible on every image.

---

## Missing features / Edge cases (19 canonical)

### [INTER-EDGE-001] Verification code: include timer and resend
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Verification code screens must include a validity countdown and a resend button.

**Why**: It's the standard pattern.

**Anti-pattern**: No resend button on the verification code screen.

---

### [INTER-EDGE-002] Tapping a profile opens an info popup
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Tapping a sender's profile image in a chat room should open a basic info popup (profile card).

**Why**: Standard pattern across social and messaging apps.

**Anti-pattern**: Tapping the profile image does nothing.

---

### [INTER-EDGE-003] Reply feature in group chat
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Provide a reply feature in group chats so conversation context is preserved when responding to a specific message.

**Why**: Context must be preserved when many people are talking.

**Anti-pattern**: No reply feature in group chat.

---

### [INTER-EDGE-004] @mentions in group chat
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Group chat must support @mentions so users can target a specific participant.

**Why**: Standard in Slack, KakaoTalk, and similar apps.

**Anti-pattern**: No @mention feature.

---

### [INTER-EDGE-005] Message deletion as a baseline feature
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Chat services must let users delete their own messages.

**Why**: It allows recovery from typos and other mistakes.

**Anti-pattern**: No way to delete sent messages.

---

### [INTER-EDGE-006] Show heading on the map marker
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: On a map UI, the current-location marker should include a visual indication of the direction the user is facing.

**Why**: Standard in Google Maps and Naver Maps.

**Anti-pattern**: Current-location marker without a heading indicator.

---

### [INTER-EDGE-007] Clear UI for one-time vs. repeating alarms
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Whether an alarm is one-time or repeating is critical information; expose it through a clear selection UI (toggle or checkbox).

**Why**: Critical information must be unambiguous.

**Anti-pattern**: User cannot tell whether an alarm is one-time or repeating.

---

### [INTER-EDGE-008] Make the select/save action explicit
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: The page title (and purpose) must match the interactions on offer, and a button for completing the action — select or save — must be provided.

**Why**: A page's purpose must be completable.

**Anti-pattern**: A sound-selection page with no select button.

---

### [INTER-EDGE-009] Keep selection pattern consistent (immediate vs. confirm)
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Pick one consistent pattern for sound or option selection: either 'tap to apply immediately' or 'save via a confirm button'.

**Why**: Mixing patterns is confusing.

**Anti-pattern**: Sound selection both applies immediately and requires a confirm button.

---

### [INTER-EDGE-010] Apply theme changes immediately
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: When the user picks a theme or color mode, the screen must update immediately so they can see the result in real time.

**Why**: A theme is a visual decision; the user needs to see it now.

**Anti-pattern**: A theme change only takes effect after pressing an apply button.

---

### [INTER-EDGE-011] Use the X icon for close/delete only
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Respect the conventional meaning of icons (X = close/delete). Reusing it for other functions like 'hide' confuses users.

**Why**: Breaking conventions causes user mistakes.

**Anti-pattern**: An X icon that actually maps to 'hide'.

---

### [INTER-EDGE-012] Make QR codes large with a white background
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Because QR codes exist to be scanned, place them at a sufficient size against a white background. Do not shrink them as if they were decoration.

**Why**: Scannability comes first.

**Anti-pattern**: A QR code rendered small on a gray background.

---

### [INTER-EDGE-013] Keep the QR scan area clean
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Eliminate visual elements around a QR code that could interfere with recognition.

**Why**: QR scanning is image recognition.

**Anti-pattern**: Crowding the area around a QR code with graphics.

---

### [INTER-EDGE-014] Functional elements prioritize real usability
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Missing features / Edge cases

**Principle**: Place functional UI elements such as QR codes or buttons so they're convenient in real use. Don't treat them as filler.

**Why**: Function is not decoration.

**Anti-pattern**: Inserting a tiny QR code just to fill empty space on the screen.

---

### [INTER-EDGE-015] Mobile sliders require indicators
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: On mobile image sliders you can drop the arrows, but indicators that show current position and total count are mandatory.

**Why**: They signal that swipe is available and convey position.

**Anti-pattern**: A mobile slider without indicators.

---

### [INTER-EDGE-016] Image sliders need indicators
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Provide indicators on image sliders so users know the total number of images and their current position.

**Why**: Without a total count, users can't tell whether they've reached the end.

**Anti-pattern**: A desktop image slider with no indicators.

---

### [INTER-EDGE-017] Define the button's result cases
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: When designing a button, also define what happens when it is pressed — state changes, navigation, and so on.

**Why**: A button without a defined result is unfinished design.

**Anti-pattern**: Designing a 'See more' button without deciding what its click does.

---

### [INTER-EDGE-018] Benchmark by actually using the product
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: Always use a product first-hand when benchmarking. UI that looks good in screenshots can be uncomfortable in practice.

**Why**: A screenshot is not the actual UX.

**Anti-pattern**: Copying a design just from Dribbble screenshots.

---

### [INTER-EDGE-019] Minimalism still needs interaction design
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Missing features / Edge cases

**Principle**: When pursuing minimal design, don't think only about static layout — use interaction (hover, click, expand) to hide unnecessary elements or reveal them progressively.

**Why**: Minimal plus interaction yields both efficiency and cleanliness.

**Anti-pattern**: A minimal concept where every element is always visible.

---

## Affordance / Touch (13 canonical)

### [INTER-AFFORD-001] Size buttons for tappability first
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Affordance / Touch

**Principle**: Prioritize button sizes that are easy to tap. Even if it looks chunky, secure a sufficient touch target. Operability beats aesthetic appeal.

**Why**: Design appeal is less important than usability.

**Anti-pattern**: A pretty 28px button that's hard to tap with a finger.

---

### [INTER-AFFORD-002] Minimum touch target of 44pt
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Affordance / Touch

**Principle**: Mobile touch targets must account for finger thickness; ensure at least 44pt.

**Why**: It's the Apple HIG and Material Design standard, matching the average finger area.

**Anti-pattern**: A 20px X button or a tiny toggle.

---

### [INTER-AFFORD-003] Icon hit area is wider than the visible icon
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: Reserve a sufficient hitbox around an icon. The standard is to set a frame larger than the icon and center the icon within it.

**Why**: Visible area is not the same as the active area; separating them tolerates fine-precision errors.

**Anti-pattern**: Just placing the icon, so it only fires when clicked precisely.

---

### [INTER-AFFORD-004] Split navigation bar touch areas evenly
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: Align every tab icon in the navigation bar within evenly divided touch areas. Designing those hit areas is fundamental to nav-bar design.

**Why**: The tab bar is touched very frequently.

**Anti-pattern**: Navigation bar icons spaced unevenly.

---

### [INTER-AFFORD-005] Hover and click on the full row
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Affordance / Touch

**Principle**: Each row in a table or list should have a hover area spanning the full width. Limiting hover to part of the text feels awkward.

**Why**: Row-level interaction naturally maps to a row-wide click.

**Anti-pattern**: Only the text inside a row is clickable, forcing the user to land precisely on it.

---

### [INTER-AFFORD-006] Distinguish buttons from input fields
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: Visually distinguish buttons from input fields. Buttons should look like buttons and input fields should look like input fields.

**Why**: Confusion leads to user mistakes.

**Anti-pattern**: A chat navigation button that looks like an input field.

---

### [INTER-AFFORD-007] Underline or arrow is enough for text links
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: An underline or arrow icon is enough for a text link. Heavy containers like chips or boxes blur the link's intent.

**Why**: Secondary elements should look secondary.

**Anti-pattern**: Putting a gray chip background behind link text.

---

### [INTER-AFFORD-009] Intuitiveness and clarity beat originality
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: In UX design, a button's intuitiveness and usability matter more than an original shape. For primary CTAs, clear and conventional forms work best.

**Why**: Critical actions like login are safest with standard forms.

**Anti-pattern**: An unusually shaped login button that users fail to recognize.

---

### [INTER-AFFORD-010] Make interaction targets generous
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: Interaction targets — hover or click areas — must be generous. Narrow targets like a thin line make users slip off and hurt UX.

**Why**: Demanding precision burdens the user.

**Anti-pattern**: Hover that only triggers on a thin 1px line.

---

### [INTER-AFFORD-011] Keep interaction controls inside the visible area
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Affordance / Touch

**Principle**: Interaction elements such as slider controls or buttons must sit inside the resolution container. If they fall outside, users cannot click them.

**Why**: Obvious, but a frequently missed mistake.

**Anti-pattern**: Placing arrows outside the 1920px viewport.

---

### [INTER-AFFORD-012] Make slider arrows large enough
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: Slider navigation arrows must be large enough to be easy to click and easy to spot.

**Why**: Small arrows score low on both discoverability and click success.

**Anti-pattern**: A 16px arrow icon.

---

### [INTER-AFFORD-013] Give dropdowns and carousels visual cues
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Affordance / Touch

**Principle**: Dropdowns, expandable menus, sliders, and carousels — anything interactive — must include a visual cue such as an arrow.

**Why**: Without a cue, users won't know the component is interactive.

**Anti-pattern**: A dropdown menu with no arrow icon.

---

### [INTER-AFFORD-014] Show that the brand name is clickable
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Affordance / Touch

**Principle**: Style brand names so users see they are clickable — use an arrow icon, color shift, or similar cue. Don't render them as plain text.

**Why**: An e-commerce pattern — the brand name leads to the brand page.

**Anti-pattern**: A brand name that looks like body text.

---

## Input (12 canonical)

### [INTER-INPUT-001] Show a clear X while the user is typing
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: While the user is typing, expose an X button on the text field that clears the value in one tap.

**Why**: It removes friction for clearing long entries.

**Anti-pattern**: Forcing the user to backspace character-by-character in a search field.

---

### [INTER-INPUT-002] Indicate active input with a stronger border
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: When an input field is being typed in, it must show an active state (emphasized border) and a clear-content X button.

**Why**: Focus indication is a UX standard.

**Anti-pattern**: No visual change when the input is focused.

---

### [INTER-INPUT-003] Eye icon on password fields
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: Password inputs must include an eye icon to toggle showing or hiding the value.

**Why**: It helps users type complex passwords correctly.

**Anti-pattern**: No way to verify the password after typing it.

---

### [INTER-INPUT-004] Don't place feature icons where they don't belong
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: Place UI elements only in contexts where the underlying feature is actually needed. Putting them in unrelated situations confuses users.

**Why**: Function and placement must match for users to recognize the element.

**Anti-pattern**: A password-reveal eye icon on the 'Find ID' screen.

---

### [INTER-INPUT-005] Design the keyboard-up case
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Input

**Principle**: When designing mobile input states, account for the layout with the keyboard raised.

**Why**: Half of mobile input happens with the keyboard active.

**Anti-pattern**: Designing only the keyboard-down screen, so the layout breaks in real use.

---

### [INTER-INPUT-006] Don't let the keyboard cover the input
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: When the keyboard appears, scroll the screen up or float the input above the keyboard so the input area stays visible.

**Why**: Users need to see what they're typing for the input to be usable.

**Anti-pattern**: The bottom input is hidden behind the keyboard.

---

### [INTER-INPUT-007] Show a send button whenever input is possible
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Input

**Principle**: Whenever a text input is available, expose the matching send or confirm button alongside it.

**Why**: Without a next action, the flow breaks.

**Anti-pattern**: Typing a chat message with no send button visible.

---

### [INTER-INPUT-008] Hide search suggestions once typing starts
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: Show search suggestions only in the pre-input state and remove them as soon as the user begins typing.

**Why**: State changes require component swaps.

**Anti-pattern**: Search suggestions remain visible while the user is typing.

---

### [INTER-INPUT-009] Design input flows per state
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: Design state transitions (initial → typing → results) so only the components relevant to each stage are shown; hide everything unnecessary.

**Why**: Each state needs its own visual environment.

**Anti-pattern**: Initial, typing, and result states all share the same layout.

---

### [INTER-INPUT-010] Disable the submit button until required fields are filled
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Input

**Principle**: Keep the submit button disabled until every required field is filled.

**Why**: It prevents empty-form submission failures.

**Anti-pattern**: The login button stays active even when nothing has been entered.

---

### [INTER-INPUT-011] Clear the password field on error
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: On a password error, clear the field and surface the error state — this is the common pattern.

**Why**: It's the standard pattern users are used to.

**Anti-pattern**: After an error, the password text remains in the field, just turned red.

---

### [INTER-INPUT-012] Auto-expand the chat input
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Input

**Principle**: The chat input should grow in height as the text gets longer, then scroll internally past a set maximum height.

**Why**: Users need to see what they're writing in long messages.

**Anti-pattern**: Long messages get truncated with an ellipsis as the user types.

---

## State expression (8 canonical)

### [INTER-STATE-001] Make active/selected states instantly recognizable
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: State expression

**Principle**: Show selected or active states with a clear change of color, weight, or icon — not a translucent overlay or a subtle color shift. 'Barely there' is a recognition failure.

**Why**: If users can't perceive the state, they can't decide what to do next.

**Anti-pattern**: Marking the selected state with only a 30% translucent stroke that disappears.

---

### [INTER-STATE-002] Design every state case
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: State expression

**Principle**: Interactive components — inputs, buttons, selects — must explicitly design every state: default, hover, selected, completed, error.

**Why**: Missing states only get caught after launch and are expensive to fix.

**Anti-pattern**: Designing only the default state and improvising the rest.

---

### [INTER-STATE-003] One visual signal is enough for selection
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: State expression

**Principle**: One clear visual signal is enough to express selection. Changing background, border, and text color all at once is excessive.

**Why**: Changing many attributes at once feels unnatural and confusing.

**Anti-pattern**: Changing background, border, and text color all at once on selection.

---

### [INTER-STATE-004] Keep it simple with a stroke or color accent
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: State expression

**Principle**: Express selection through simple means like an underline or color accent rather than heavy color shifts and shadows.

**Why**: Simple signals are perceived more easily.

**Anti-pattern**: On selection, changing color, adding a shadow, and resizing all at once.

---

### [INTER-STATE-005] Selection over images: dim plus a strong indicator
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: State expression

**Principle**: Selection indicators placed over images should pair a strong border with a dim overlay so they stay distinct from the background image.

**Why**: If selection blends into the image, users won't recognize it.

**Anti-pattern**: Just a checkbox over the image, swallowed by the background.

---

### [INTER-STATE-006] The active tab must look active
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: State expression

**Principle**: The tab bar item for the currently active page (in bottom navigation) must always be rendered in its active state.

**Why**: Failing to perceive the current location means feeling lost.

**Anti-pattern**: On the home screen, the Home tab still looks inactive.

---

### [INTER-STATE-007] Tabs have only two states: selected or not
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: State expression

**Principle**: Tabs should only distinguish two states: selected and not selected. Mixing three or more states confuses users.

**Why**: Simplicity is clarity.

**Anti-pattern**: Tabs mixing selected, unselected, and a third unclear gray state.

---

### [INTER-STATE-008] Mark sidebar selection with weight and color
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: State expression

**Principle**: In navigation menus, emphasize the selected item with a heavier font weight (semibold or bolder) or a color so users know where they are.

**Why**: The sidebar signals location.

**Anti-pattern**: Selected and unselected menus styled identically.

---

## Feedback (9 canonical)

### [INTER-FB-001] Hover and tap feedback is mandatory
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: Every clickable UI element should provide visual hover or active feedback to improve usability.

**Why**: Feedback signals that the interaction was registered.

**Anti-pattern**: Nothing changes when the button is clicked.

---

### [INTER-FB-002] Visual change after a button click
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: After a button click, give clear feedback with a visual state change such as switching to a check icon or filling in color.

**Why**: Users confirm whether an action completed by sight.

**Anti-pattern**: Pressing the follow button shows no indication.

---

### [INTER-FB-003] Visualize that something was selected
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: When users select or add an item, show a 'selected' state on it as visual feedback. Unresponsive interactions are a UX failure.

**Why**: Without feedback, users don't know whether the action registered.

**Anti-pattern**: Adding a pattern leaves no selected indicator on the card.

---

### [INTER-FB-004] Make selection clear with checkmarks or color
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: Mark selection clearly with checkmarks, color changes, or shadows. Users should intuitively perceive 'this is selected'.

**Why**: A checkmark is a universal selection signal.

**Anti-pattern**: Selection is too weakly indicated for users to notice.

---

### [INTER-FB-005] Major actions need a result screen or alert
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: For every major user action — sending a verification code, completing a lookup — provide clear result feedback through an alert or completion screen.

**Why**: An action with no result is an incomplete flow.

**Anti-pattern**: No completion screen after a password change.

---

### [INTER-FB-006] Express loading and processing clearly
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: Express loading and processing states clearly with text or animation so users can recognize them at a glance.

**Why**: Users feel anxious when they can't tell processing from a freeze.

**Anti-pattern**: The AI is composing an answer with no indicator visible.

---

### [INTER-FB-007] Keep hover changes subtle
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Feedback

**Principle**: Design hover states as subtle shifts from the default. Overblown color changes can read as a different element entirely.

**Why**: A wide swing in change feels unnatural.

**Anti-pattern**: A line button that flips to a strong solid color on hover.

---

### [INTER-FB-008] A weak hover at design time feels right in use
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: A hover effect that looks weak in the design tool will feel strong enough in actual use. Don't overdial it.

**Why**: Perception differs between static and animated states.

**Anti-pattern**: Boosting the hover because it looks weak in the file, then it's too much in real use.

---

### [INTER-FB-009] Hover shadows should be dark and neutral
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Feedback

**Principle**: Use dark, neutral shadows on hover. Colored shadows are too heavy and make the UI feel busy.

**Why**: Colored shadows become emphasis themselves.

**Anti-pattern**: Colorful shadows appear on hover.

---

## Navigation (10 canonical)

### [INTER-NAV-001] Guarantee a way back
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Every sub-screen must offer a back or close button so users can return to the previous step.

**Why**: A screen with no exit is a trap.

**Anti-pattern**: A modal with no close button.

---

### [INTER-NAV-002] Apps must include their own back UI
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Native and hybrid app screens have no browser back button, so they must include an in-screen back UI.

**Why**: Apps differ from the web — they must own their navigation.

**Anti-pattern**: An app screen with no back button.

---

### [INTER-NAV-003] If a choice can change, the user must be able to return
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: If a user can change a previous choice, they must be able to return to that screen. Blocking it intentionally requires a clear reason.

**Why**: Forcing a one-way path burdens UX.

**Anti-pattern**: After picking a region, the user cannot return to change it.

---

### [INTER-NAV-004] Show back based on entry path
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Conditionally show the back button based on how the user entered. Show it for direct entry, omit it for entries through a tab or dock — that's the standard pattern.

**Why**: Back is meaningless when the user arrived from a main tab.

**Anti-pattern**: Always showing back on the Home tab.

---

### [INTER-NAV-005] Place the close (X) button separately
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Place the close (X) button separately from content controls like 'view all' or 'zoom'. Keep close on its own, typically in the top right.

**Why**: Grouping them together leads to accidental closes.

**Anti-pattern**: Putting X and 'view all' in the same group.

---

### [INTER-NAV-006] Cleanly separate the close button
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Separate the close button's click area clearly enough to avoid unintended actions.

**Why**: Accidental closes cost the user their work.

**Anti-pattern**: The close button's hit area overlaps another button's.

---

### [INTER-NAV-007] Full popups need an X close button
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Modals, full popups, and any layer that covers the main screen must include a clear close action (X or Cancel).

**Why**: It prevents the trapped feeling.

**Anti-pattern**: A full popup with no close button.

---

### [INTER-NAV-008] Review popup and dropdown positions in advance
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Place popups, dropdowns, and tooltips so they don't cover important content when open. Review layer stacking and possible overlaps in advance.

**Why**: Collision risk has to be predicted at design time.

**Anti-pattern**: A dropdown covers another menu.

---

### [INTER-NAV-009] Modals need an explicit X (outside-click is not enough)
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: Modals and popups must include an explicit close (X) button for accessibility. Outside-click-to-dismiss alone does not meet accessibility standards.

**Why**: Keyboard-navigation users also need access.

**Anti-pattern**: A modal that closes only via outside-click.

---

### [INTER-NAV-010] Show carousel buttons on hover only
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Navigation

**Principle**: In minimal UI, hide carousel navigation buttons by default and reveal them on hover. This cuts visual noise while keeping access available.

**Why**: The default state stays clean.

**Anti-pattern**: Strong arrows always visible in a minimal design.

---

## Add/Remove symmetry (5 canonical)

### [INTER-PAIR-001] If add exists, remove must exist too
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Add/Remove symmetry

**Principle**: Anything users can add, they must also be able to delete. Add and remove must exist as a pair.

**Why**: Irreversible actions are a UX risk.

**Anti-pattern**: Patterns can be added but not removed.

---

### [INTER-PAIR-002] If select-all exists, individual select must exist too
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Add/Remove symmetry

**Principle**: Whenever you offer 'select all', also design individual selection. The two features work as a set.

**Why**: With only one of them, meaningful bulk actions become impossible.

**Anti-pattern**: Only 'select all' exists, with no individual checkboxes.

---

### [INTER-PAIR-003] Hide must come with restore
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Add/Remove symmetry

**Principle**: Hide and disable features must always be paired with a way to undo or re-enable them.

**Why**: Irreversible hiding frustrates users.

**Anti-pattern**: An alarm was hidden but cannot be re-enabled.

---

### [INTER-PAIR-004] History implies the ability to restore
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Add/Remove symmetry

**Principle**: If you offer history or a record feature, also provide a way to restore to those states.

**Why**: History exists for the sake of restoration.

**Anti-pattern**: A history of hidden alarms exists, but they cannot be restored.

---

### [INTER-PAIR-005] Provide bulk actions for lists
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Add/Remove symmetry

**Principle**: When a list contains many items, provide bulk operations such as select/deselect all.

**Why**: Operating one by one is inefficient.

**Anti-pattern**: No way to turn off 100 alarms in bulk.

---

## Motion (5 canonical)

### [INTER-MOTION-001] Subtle motion lifts quality
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Motion

**Principle**: Adding restrained micro-motion in a couple of places — subtle icon moves, smooth transitions — raises the overall quality and polish of the design.

**Why**: Static UI feels lifeless; motion brings it alive.

**Anti-pattern**: Every interaction snaps instantly with no motion.

---

### [INTER-MOTION-002] Motion needs a clear purpose
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Motion

**Principle**: When using motion, first define its purpose — focus, transition, information, depth — and align the whole design to that purpose.

**Why**: Motion without reason is noise.

**Anti-pattern**: Flashy, scattering motion that means nothing.

---

### [INTER-MOTION-003] Motion should create space and immersion
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Motion

**Principle**: Motion should serve more than just 'appearing'. To deliver immersion, design motion that creates spatial depth — images expanding, perspective shifting.

**Why**: A plain fade-in isn't motion; it's added cost.

**Anti-pattern**: Every motion is just a fade-in.

---

### [INTER-MOTION-004] Lean into motion in your portfolio
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Motion

**Principle**: When a portfolio is a chance to show coding ability, add meaningful interaction or motion even to static elements to highlight your skills.

**Why**: It's a chance to showcase ability.

**Anti-pattern**: Motion is possible but the portfolio stays static.

---

### [INTER-MOTION-005] Combine motion with data visualization
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Motion

**Principle**: If you can code and animate, combine motion with data visualization — number count-ups, bar-chart growth animations — to deliver the message more powerfully.

**Why**: Motion is a tool for visualizing change in data.

**Anti-pattern**: Graphs displayed only as static images.

---

## Missing or duplicate cases (4 canonical)

### [INTER-CASE-001] Distinguish the selected case clearly
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing or duplicate cases

**Principle**: Mark selected items clearly with a stroke or color accent. Even without animation, the selected state can be perceived just fine.

**Why**: A static design is enough.

**Anti-pattern**: Selection indicated only by an ambiguous color shift.

---

### [INTER-CASE-002] Selection indicator must not clash with other UI
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Missing or duplicate cases

**Principle**: The selected-state indicator must be clearly distinct from other interactive elements on the screen to prevent confusion.

**Why**: If the selection signal looks like a 'more' icon, users get confused.

**Anti-pattern**: The selection indicator resembles the 'more' icon.

---

### [INTER-CASE-003] Show the selected state clearly
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Missing or duplicate cases

**Principle**: When a user selects an item, visually mark the corresponding icon or element as active. Without selection feedback, UX becomes confusing.

**Why**: Feedback is the foundation of trust.

**Anti-pattern**: Selecting a team member produces no change in the icon.

---

### [INTER-CASE-004] Emphasize selection in one place only
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Missing or duplicate cases

**Principle**: Show the current selected state with one clear background or accent color, not several. Emphasizing multiple elements at once makes selection hard to read.

**Why**: One emphasis equals clarity.

**Anti-pattern**: Both the tab and the sidebar are color-emphasized at the same time.

---

## Hover vs. Click (2 canonical)

### [INTER-HOVER-001] Click is safer for informational content
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Hover vs. Click

**Principle**: Use click rather than hover for informational content like articles, news, and sports info. A hover closes the moment the cursor drifts, which hurts usability.

**Why**: Hover demands precision.

**Anti-pattern**: Opening news card details only on hover.

---

### [INTER-HOVER-002] Use click in comparison UI to keep multiples open
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Hover vs. Click

**Principle**: When the UI is for comparison, switch from hover to click so users can keep several panels open at once and compare.

**Why**: Hover only opens one at a time.

**Anti-pattern**: Plan comparison runs on hover, preventing side-by-side review.

---
