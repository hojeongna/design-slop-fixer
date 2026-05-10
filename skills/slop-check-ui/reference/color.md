# Color (UI)

Color usage, tone, contrast, and color system rules

- **Total canonical rules**: 80
- **Sub-categories**: 15

---

## Contents
- Contrast & accessibility — 8 canonical
- Accent color restraint — 7 canonical
- Misc — 14 canonical
- Text over images — 5 canonical
- Background treatment — 4 canonical
- Color consistency/tokens — 4 canonical
- Shadow/effect restraint — 9 canonical
- Stroke/border — 6 canonical
- Gradient — 6 canonical
- Black restraint — 3 canonical
- Gray usage — 3 canonical
- Text color hierarchy — 3 canonical
- Semantic state colors — 3 canonical
- Tone adjustment — 4 canonical
- Opacity usage — 1 canonical

---

## Contrast & accessibility (8 canonical)

### [COLOR-CONTRAST-001] Meet WCAG contrast standards
- **Platform**: Mobile/PC
- **Frequency weight**: 26
- **Sub-category**: Contrast & accessibility

**Principle**: Both body and secondary text must meet WCAG AA contrast standards against the background (minimum 4.5:1).

**Why**: Accessibility is mandatory.

**Anti-pattern**: Faded, low-contrast text.

---

### [COLOR-CONTRAST-002] Avoid faded grays in the 9XX/AXX range
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Contrast & accessibility

**Principle**: Do not use faded grays above 50% lightness (e.g., #999, #ACACAC, #C4C4C4, #767676) for body or content text.

**Why**: Fails WCAG.

**Anti-pattern**: Using #ACACAC for body copy.

---

### [COLOR-CONTRAST-003] Add a boundary when similar colors meet
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Contrast & accessibility

**Principle**: Do not place elements of the same or similar color on top of a matching background. If unavoidable, separate them with a thin boundary such as a white stroke.

**Why**: Separation is essential.

**Anti-pattern**: A gray card on a gray background.

---

### [COLOR-CONTRAST-004] Reserve 9XX-range colors for disabled states
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Contrast & accessibility

**Principle**: Text colors must have sufficient lightness contrast with the background, and very pale ranges (such as 9XX values) should be limited to disabled states or decorative use only.

**Why**: Meaning drives usage.

**Anti-pattern**: Using 9XX-range grays for body text.

---

### [COLOR-CONTRAST-005] Provide a rich palette of steps
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Contrast & accessibility

**Principle**: A design system's color palette must include enough steps to cover all key states such as emphasis, default, secondary, and disabled.

**Why**: States need expression.

**Anti-pattern**: Only five steps, which is insufficient.

---

### [COLOR-CONTRAST-006] Avoid overlapping tones
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Contrast & accessibility

**Principle**: When different elements share similar surrounding tones, they become indistinguishable, so separate the tones clearly.

**Why**: Adjacent similar tones erase boundaries and make information hard to distinguish.

**Anti-pattern**: A screen where the search bar shares the background tone, making the input area invisible.

---

### [COLOR-CONTRAST-007] Distinguish similar colors with secondary cues
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Contrast & accessibility

**Principle**: When the same color appears twice at the same hierarchy level, the difference is lost, so support it with circles, icons, or text.

**Why**: Color alone cannot convey distinctions in meaning, so secondary visual cues are necessary.

**Anti-pattern**: A table with two cells in identical colors and no way to tell them apart.

---

### [COLOR-CONTRAST-008] Pair darks with lights for depth
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Contrast & accessibility

**Principle**: Whenever a dark element is present, a light one must accompany it to create depth, and pairs of light elements need a dark anchor.

**Why**: Balanced contrast brings both visual depth and emphasis to life.

**Anti-pattern**: Continuous dark or light surfaces that flatten the entire screen visually.

---

## Accent color restraint (7 canonical)

### [COLOR-POINT-001] Reserve accent color for the essentials
- **Platform**: Mobile/PC
- **Frequency weight**: 20
- **Sub-category**: Accent color restraint

**Principle**: Use accent or brand colors (CTA, emphasis) in only one or two places per screen. Repeating them everywhere dilutes the emphasis.

**Why**: The emphasis paradox.

**Anti-pattern**: Brand color on every button.

---

### [COLOR-POINT-002] Frame first, color last
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Accent color restraint

**Principle**: Lock down the frame and structure first, and apply color only at the end where accent is needed.

**Why**: Structure comes first.

**Anti-pattern**: Painting in color from the start.

---

### [COLOR-POINT-003] When it looks busy, cut color first
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Accent color restraint

**Principle**: When a design feels cluttered, the first thing to reduce is color. If the structure still reads clearly without color, you are on the right track.

**Why**: Color is noise.

**Anti-pattern**: Adding more color when it already feels busy.

---

### [COLOR-POINT-004] Account for sticky elements
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Accent color restraint

**Principle**: Set the color intensity of sticky elements (sticky buttons, bottom bars) first, then design the remaining content to be weaker than that baseline.

**Why**: Whole-screen context.

**Anti-pattern**: Designing each screen in isolation.

---

### [COLOR-POINT-006] Tone down and soften
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Accent color restraint

**Principle**: When colors feel too strong or saturated, tone them down and lighten them.

**Why**: Overly strong colors create visual fatigue and overwhelm other elements, breaking the hierarchy.

**Anti-pattern**: A screen where every color is pushed to maximum saturation and brightness.

---

### [COLOR-POINT-007] Balance strong and soft
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Accent color restraint

**Principle**: Strong elements must be paired with softer ones; when everything is strong, the design becomes heavy.

**Why**: Contrast between strong and soft elements lets emphasis stand out and distributes visual weight properly.

**Anti-pattern**: A heavy screen where every element competes for attention with no clear focal point.

---

### [COLOR-POINT-008] Use yellow with restraint
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Accent color restraint

**Principle**: Avoid yellow as a base color; it is so intense that graphics get buried and white text becomes unreadable.

**Why**: A yellow background struggles to produce contrast, so almost no text color reads well on it.

**Anti-pattern**: A banner where white text and graphics are all swallowed by a yellow background.

---

## Misc (14 canonical)

### [COLOR-MISC-001] Avoid meaningless multicolor
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Misc

**Principle**: Use a different color per item only when the meaning is clear.

**Why**: Color is a categorical signal.

**Anti-pattern**: Five different colors for five recommended search terms.

---

### [COLOR-MISC-002] Same hierarchy, same color
- **Platform**: PC
- **Frequency weight**: 3
- **Sub-category**: Misc

**Principle**: Apply the same style and color to buttons that share function and hierarchy.

**Why**: Color carries meaning.

**Anti-pattern**: Three download buttons in three different colors.

---

### [COLOR-MISC-003] Recheck contrast when the background changes
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Misc

**Principle**: When changing a background color, also verify that every element on top of it (buttons, text, etc.) still has sufficient contrast.

**Why**: Domino effect.

**Anti-pattern**: Changing only the background and stopping there.

---

### [COLOR-MISC-004] Glass effect: readability first
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Misc

**Principle**: Use glass effects (translucency plus blur) only when readability is guaranteed.

**Why**: Readability comes first.

**Anti-pattern**: Glass effect that makes the text unreadable.

---

### [COLOR-MISC-007] On dark backgrounds, no color outshines white
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Misc

**Principle**: To emphasize text with color on a dark background, the color must read visually stronger than white, which is hard to achieve.

**Why**: Relative intensity matters.

**Anti-pattern**: Colored text on a dark background to convey emphasis.

---

### [COLOR-MISC-008] Light gray is often enough
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Misc

**Principle**: When a button color feels too strong against the background, swap white for a light gray to blend in more naturally.

**Why**: Intensity tuning.

**Anti-pattern**: Defaulting to harsh, pure white.

---

### [COLOR-MISC-009] Dim map overlays without hiding the map
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Misc

**Principle**: Handle text readability on map UIs by following the patterns used by real map services (Naver, Google), such as white background cards or translucent treatments.

**Why**: Follow domain patterns.

**Anti-pattern**: A solid black overlay covering the map.

---

### [COLOR-MISC-010] Use text color alone to signal selection
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Misc

**Principle**: To distinguish selected from unselected states, changing only the text color can deliver clear feedback without altering the entire button background.

**Why**: Use varied means.

**Anti-pattern**: Always changing the entire background as the only feedback.

---

### [COLOR-MISC-011] Use strong color for emphasis areas
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Misc

**Principle**: For areas that need emphasis, use strong color, gradients, or shadows instead of gray boxes to increase visual impact.

**Why**: Weak emphasis equals no emphasis.

**Anti-pattern**: Trying to emphasize with a gray box.

---

### [COLOR-MISC-012] Reserve accent color for key actions
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Misc

**Principle**: Apply the accent (CTA) color selectively to the single most important call-to-action on the page so that emphasis stays effective.

**Why**: Selectivity.

**Anti-pattern**: Every button colored blue.

---

### [COLOR-MISC-013] Separate button colors by role
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Misc

**Principle**: Separate button colors by role: use neutral colors (such as black) for default and navigation buttons, and reserve the accent color for the primary CTA only.

**Why**: Role determines color.

**Anti-pattern**: Overusing a single accent color across every button.

---

### [COLOR-MISC-015] Design freely, do not mimic reality
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Misc

**Principle**: Graphics do not have to mirror reality exactly.

**Why**: Design allows abstraction and reinterpretation, so faithful imitation is not required.

**Anti-pattern**: Designs constrained to real-world colors and shapes that lose expressive freedom.

---

### [COLOR-MISC-016] Always question every color choice
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Misc

**Principle**: Whenever you use color, deliberate on where and why before applying it.

**Why**: Color used without intent muddles the message and breaks the hierarchy.

**Anti-pattern**: A screen filled with colors added simply because they look pretty, with no real reason.

---

### [COLOR-MISC-017] Match color across equivalent regions
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Misc

**Principle**: Apply the same treatment used in an established area (such as the main billboard top) to other equivalent areas to maintain consistency.

**Why**: Treating regions with the same role differently breaks the system.

**Anti-pattern**: Main and sub regions that should share a tone but instead diverge, breaking consistency.

---

## Text over images (5 canonical)

### [COLOR-OVERLAY-001] Apply a gradient dim (around 50%)
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Text over images

**Principle**: Apply a gradient dim or dark overlay so that text and icons placed on images or video remain legible regardless of background brightness.

**Why**: Images are variable.

**Anti-pattern**: Text placed directly over an image with no gradient.

---

### [COLOR-OVERLAY-002] Opacity alone is not enough
- **Platform**: Mobile/PC
- **Frequency weight**: 9
- **Sub-category**: Text over images

**Principle**: Do not rely on opacity alone for text and tags placed over images. Use clear contrast tools such as background blur, a dark overlay, or a dim layer.

**Why**: Opacity behaves unpredictably.

**Anti-pattern**: White at 50% opacity as the only treatment.

---

### [COLOR-OVERLAY-003] Add a drop shadow to icons over images
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Text over images

**Principle**: Apply a drop shadow to icons placed on images or video so they remain identifiable across varying background brightness.

**Why**: The Instagram pattern.

**Anti-pattern**: A bare white icon over an image with no shadow.

---

### [COLOR-OVERLAY-004] Top overlays need a top gradient
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Text over images

**Principle**: When video or image screens have overlay elements at the top (title, back button, etc.), apply a gradient at the top as well.

**Why**: Protect both ends.

**Anti-pattern**: Applying a gradient only at the bottom.

---

### [COLOR-OVERLAY-005] Keep text readable over color surfaces
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Text over images

**Principle**: When descriptive text is being swallowed by a color surface, remove the color or adjust the text color.

**Why**: Text in a similar tone to its color background loses all readability.

**Anti-pattern**: A card whose text disappears into the colored surface.

---

## Background treatment (4 canonical)

### [COLOR-BG-002] Section backgrounds need a clear purpose
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Background treatment

**Principle**: Use a gray background fill to separate sections only when it carries clear meaning or purpose.

**Why**: Backgrounds need a reason.

**Anti-pattern**: Filling backgrounds for no reason.

---

### [COLOR-BG-003] Avoid strong color for the GNB background
- **Platform**: PC
- **Frequency weight**: 6
- **Sub-category**: Background treatment

**Principle**: Do not fill the GNB background with a color that is too strong, such as solid black.

**Why**: It is supporting UI.

**Anti-pattern**: A solid black GNB sitting on top of an image.

---

### [COLOR-BG-004] Avoid stacking graphics on a colored background
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Background treatment

**Principle**: Do not add a background color in areas that already contain a graphic or image.

**Why**: Accumulation creates noise.

**Anti-pattern**: An illustrated card placed on a colored background.

---

### [COLOR-BG-005] Separate background and graphic colors
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Background treatment

**Principle**: If the background is blue, blue raindrop graphics on top will disappear, so separate background and graphic colors.

**Why**: When background and graphic colors are too close, the graphic visually vanishes.

**Anti-pattern**: A screen where blue graphics vanish into a same-tone blue background.

---

## Color consistency/tokens (4 canonical)

### [COLOR-SYSTEM-001] Share color across PC and mobile
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Color consistency/tokens

**Principle**: In responsive design, PC and mobile should share the same color system as a rule.

**Why**: Device should not change color.

**Anti-pattern**: Different colors on PC versus mobile.

---

### [COLOR-SYSTEM-002] Dark mode is its own system
- **Platform**: Mobile/PC
- **Frequency weight**: 4
- **Sub-category**: Color consistency/tokens

**Principle**: Dark mode is not a simple inversion of light mode. Design it as a separate color system from the outset.

**Why**: It follows a separate curve.

**Anti-pattern**: An auto-inverted dark mode.

---

### [COLOR-SYSTEM-003] Do not use disabled colors for active content
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Color consistency/tokens

**Principle**: Do not use colors reserved for disabled or placeholder states (such as #999) on active content text.

**Why**: Tokens carry meaning.

**Anti-pattern**: Using #999 for active body text.

---

### [COLOR-SYSTEM-004] Do not use the brand color at 100%
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Color consistency/tokens

**Principle**: Do not apply the brand color at full strength everywhere; reserve it for what you want to emphasize and use a medium tone elsewhere.

**Why**: Using the brand color everywhere makes the screen flashy and disperses emphasis.

**Anti-pattern**: A screen with brand color spread evenly throughout, leaving no emphasis behind.

---

## Shadow/effect restraint (9 canonical)

### [COLOR-SHADOW-001] Keep shadows very subtle
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Shadow/effect restraint

**Principle**: Use very subtle shadow values, around 3-8% opacity, as the default.

**Why**: A hint of depth.

**Anti-pattern**: Heavy drop shadows.

---

### [COLOR-SHADOW-002] Use shadows only on key emphasis
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Shadow/effect restraint

**Principle**: Apply shadows sparingly, only to key elements that need emphasis or depth.

**Why**: Overuse breaks the hierarchy.

**Anti-pattern**: Shadows applied everywhere.

---

### [COLOR-SHADOW-004] Use shadow instead of heavy strokes
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Shadow/effect restraint

**Principle**: On dashboards, give depth with shadows rather than heavy strokes.

**Why**: Heavy strokes carry too much visual weight and make information feel cramped.

**Anti-pattern**: A cramped dashboard where every card is wrapped in a heavy black border.

---

### [COLOR-SHADOW-005] Use shadows to create depth
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Shadow/effect restraint

**Principle**: When you want to emphasize, use shadows to create elevation and depth, establishing layered hierarchy and spatial structure.

**Why**: Strong-and-soft shadows establish a z-axis hierarchy that effectively groups information.

**Anti-pattern**: A flat screen where every shadow has identical intensity.

---

### [COLOR-SHADOW-006] A slight shadow is the right amount
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Shadow/effect restraint

**Principle**: Shadows should sit just barely on the surface; if they feel too strong, dial them back to something modest.

**Why**: Strong shadows weigh the design down and produce a fake-looking dimensionality.

**Anti-pattern**: A heavy screen where every button and card carries a deep black shadow.

---

### [COLOR-SHADOW-007] Inner shadow
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Shadow/effect restraint

**Principle**: Apply inner shadows tight and slight, with a subtle hue tuned to the surface color.

**Why**: Inner shadow is meant to add texture, not depth, so it must not be strong.

**Anti-pattern**: An overly intense inner shadow that makes the surface look caved in.

---

### [COLOR-SHADOW-008] Layer inner shadows actively
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Shadow/effect restraint

**Principle**: To keep surface effects from feeling vague, use inner shadows actively. Layer at least three or four to bring out real depth.

**Why**: A single inner shadow looks weak and awkward; only multiple layered shadows produce rich dimensionality.

**Anti-pattern**: A surface with a single weak inner shadow that ends up looking flat and ambiguous.

---

### [COLOR-SHADOW-009] Restrain blur on inner shadows
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Shadow/effect restraint

**Principle**: Do not over-blur inner shadows. When they spread out, the result looks like cheap free 3D.

**Why**: Excess blur erases depth and produces a cheap pseudo-3D feel.

**Anti-pattern**: Surfaces with such heavy inner shadow blur that they look like free 3D assets.

---

### [COLOR-SHADOW-010] Drop shadow as paper-on-paper
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Shadow/effect restraint

**Principle**: Drop shadow is not about the shadow itself; it should suggest a document floating slightly above another. Keep the color from being too dark.

**Why**: The essence of a drop shadow is the subtle paper-on-paper sense of depth.

**Anti-pattern**: A drop shadow set in heavy black, making the shadow itself the most prominent thing on the surface.

---

## Stroke/border (6 canonical)

### [COLOR-STROKE-001] Remove unnecessary strokes
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Stroke/border

**Principle**: Remove unnecessary boxes and strokes; let color alone define the area.

**Why**: Lines add complexity.

**Anti-pattern**: A border on every card.

---

### [COLOR-STROKE-002] Make strokes perceptible
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Stroke/border

**Principle**: Apply strokes with enough thickness and intensity that they are visually perceptible.

**Why**: Half-measures are worst.

**Anti-pattern**: 1px stroke at 0.5 opacity.

---

### [COLOR-STROKE-003] Keep dividers very faint
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Stroke/border

**Principle**: Dividers exist to support content, not to demand attention, so keep them very faint.

**Why**: Supporting elements stay supporting.

**Anti-pattern**: Heavy, attention-grabbing dividers.

---

### [COLOR-STROKE-004] Use dark borders on badges
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Stroke/border

**Principle**: Use a badge border color that contrasts with the underlying background (usually a dark hue) so the badge appears to float.

**Why**: Separation effect.

**Anti-pattern**: A white-stroke badge on a white background.

---

### [COLOR-STROKE-005] Avoid heavy strokes
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Stroke/border

**Principle**: Strokes on input areas such as search bars feel cramped when too heavy, so keep them light.

**Why**: A heavy stroke carries strong visual weight and makes the input area look like a primary emphasis element.

**Anti-pattern**: A search field whose dark, thick border becomes the most emphasized item on the screen.

---

### [COLOR-STROKE-006] Emphasize through stroke weight
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Stroke/border

**Principle**: Create emphasis through differences in stroke weight rather than color.

**Why**: Differences in weight establish hierarchy cleanly without the weight of additional color.

**Anti-pattern**: Pushing colors stronger to create emphasis, leaving the screen scattered and noisy.

---

## Gradient (6 canonical)

### [COLOR-GRADIENT-001] Use gradients to add richness
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Gradient

**Principle**: A pure primary color used as-is feels harsh and flat; a gradient adds richness even with the same hue.

**Why**: Primary colors feel harsh.

**Anti-pattern**: A solid #FF0000 fill.

---

### [COLOR-GRADIENT-002] Add depth with radial gradients
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Gradient

**Principle**: Do not rely solely on linear gradients; make use of radial gradients as well.

**Why**: Variety matters.

**Anti-pattern**: Top-to-bottom linear gradients only.

---

### [COLOR-GRADIENT-003] Restrain the number of gradient stops
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Gradient

**Principle**: Two stops are usually enough for a gradient; three or more is generally too much.

**Why**: More stops muddy the color and erase the intended smoothness.

**Anti-pattern**: A surface with three or more gradient stops blended into a muddy color.

---

### [COLOR-GRADIENT-004] Restrain gradients on portfolio pages
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Gradient

**Principle**: Inserting decorative gradient shapes on content pages such as profiles or portfolios is almost always unnecessary.

**Why**: When pages whose essence is content are loaded with visual ornamentation, the actual content is weakened.

**Anti-pattern**: A portfolio cover page loaded with showy gradient ornamentation.

---

### [COLOR-GRADIENT-005] Plant subtle gradients
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Gradient

**Principle**: Even on white surfaces, planting a slight gradient reduces monotony and adds richness.

**Why**: Pure 100% white feels flat and cold; a subtle gradient gives it depth.

**Anti-pattern**: A screen where every surface is pure 100% white, flat and lifeless.

---

### [COLOR-GRADIENT-006] Apply gradient to the stroke
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Gradient

**Principle**: When you want to emphasize, apply a gradient to the stroke rather than the fill.

**Why**: A solid fill feels heavy and disperses emphasis, while a gradient on the stroke offers light, focused emphasis.

**Anti-pattern**: Buttons or cards filled with a heavy color, leaving the emphasis feeling cramped.

---

## Black restraint (3 canonical)

### [COLOR-BLACK-001] Avoid repeating heavy black
- **Platform**: PC
- **Frequency weight**: 6
- **Sub-category**: Black restraint

**Principle**: Black is visually very strong; using it repeatedly accumulates weight and makes the entire design feel oppressive.

**Why**: Quantity equals weight.

**Anti-pattern**: Black spread everywhere.

---

### [COLOR-BLACK-002] Soften pure black
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Black restraint

**Principle**: In minimal, calm designs, text reads softer with a slight gray mixed in rather than pure #000 black.

**Why**: Digital intensity.

**Anti-pattern**: Body text in pure #000.

---

### [COLOR-BLACK-003] Avoid heavy weights on dark backgrounds
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Black restraint

**Principle**: On dark backgrounds, cap font weight at Semi Bold or below to manage visual weight.

**Why**: Doubled heaviness.

**Anti-pattern**: A dark background combined with Extra Bold type.

---

## Gray usage (3 canonical)

### [COLOR-GRAY-001] Avoid gray on multiple layers at once
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Gray usage

**Principle**: Do not use gray simultaneously across background, text, lines, chips, and other layers.

**Why**: Hierarchy disappears.

**Anti-pattern**: Gray background plus gray text plus gray lines plus gray chips.

---

### [COLOR-GRAY-002] Gray buttons can read as disabled
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Gray usage

**Principle**: When gray-background buttons or inputs are too dark, they read as disabled and users hesitate to click.

**Why**: Prevent misreading.

**Anti-pattern**: An active button rendered in deep gray.

---

### [COLOR-GRAY-003] Same role, same gray
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Gray usage

**Principle**: Use the same color token for grays that play the same role, whether dividers, backgrounds, or supporting elements.

**Why**: System discipline.

**Anti-pattern**: Similar but slightly different grays scattered around.

---

## Text color hierarchy (3 canonical)

### [COLOR-TEXT-001] Define about four text color steps
- **Platform**: Mobile/PC
- **Frequency weight**: 5
- **Sub-category**: Text color hierarchy

**Principle**: Define around four text color steps: strong (titles), medium (body), weak (supporting), and disabled.

**Why**: Systems require restraint.

**Anti-pattern**: Using six different blacks.

---

### [COLOR-TEXT-002] Mix a subtle gray into supporting text
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Text color hierarchy

**Principle**: Use a subtly gray-mixed color for supporting and sub-text instead of pure black (#000).

**Why**: Express hierarchy.

**Anti-pattern**: All text in #000.

---

### [COLOR-TEXT-003] Do not stack bold and color for emphasis
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Text color hierarchy

**Principle**: When emphasizing text, choose either bold or color intensity, not both at once.

**Why**: Double emphasis feels unnatural.

**Anti-pattern**: Bold combined with a faded color.

---

## Semantic state colors (3 canonical)

### [COLOR-SEMANTIC-001] Color carries meaning
- **Platform**: Mobile/PC
- **Frequency weight**: 3
- **Sub-category**: Semantic state colors

**Principle**: Every color choice in a design must have a clear reason behind it.

**Why**: Color without reason becomes noise.

**Anti-pattern**: Using a color simply because it looks pretty.

---

### [COLOR-SEMANTIC-002] Reflect the actual active/inactive state
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Semantic state colors

**Principle**: UIs with state (active/inactive, applied/unapplied) must use colors that accurately reflect the real state.

**Why**: Color equals state.

**Anti-pattern**: A pink badge on a coupon that has not been applied.

---

### [COLOR-SEMANTIC-003] Reserve red for errors
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Semantic state colors

**Principle**: Use red only for errors, warnings, and danger. Red used merely for emphasis or decoration sends the wrong signal to users.

**Why**: Convention.

**Anti-pattern**: Red used as decoration.

---

## Tone adjustment (4 canonical)

### [COLOR-TONE-001] Nudge saturation up slightly
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Tone adjustment

**Principle**: When colors look dull, nudge only the saturation up slightly.

**Why**: Insufficient saturation makes the whole design look hazy and weakens the message.

**Anti-pattern**: A screen washed out by near-neutral, dull colors with no emphasis at all.

---

### [COLOR-TONE-002] Calm the design through tone adjustment
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Tone adjustment

**Principle**: Adjusting the overall color tone and amplifying only the emphasis brings calm to the design.

**Why**: Slightly lowering the overall tone brings the key emphasis to life and reduces visual fatigue.

**Anti-pattern**: A screen meant to feel calm but loaded with strong colors and no tone adjustment.

---

### [COLOR-TONE-003] Avoid an overall dark tone
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Tone adjustment

**Principle**: When the first screen is dark, the impression feels heavy, so keep the overall tone bright.

**Why**: A dark tone adds weight but degrades both readability and mood on information-driven pages.

**Anti-pattern**: An information-focused site whose very first screen is overall dark.

---

### [COLOR-TONE-004] Pink tones over red
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Tone adjustment

**Principle**: Choose a softer pink tone instead of a strong red to deliver the same emphasis more gently.

**Why**: It delivers the same emphasis with a softer, more refined impression.

**Anti-pattern**: Relying solely on strong red, leaving the tone aggressive or overly intense.

---

## Opacity usage (1 canonical)

### [COLOR-OPACITY-002] Keep decorative lines at low opacity
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Opacity usage

**Principle**: Treat decorative lines and dividers at very low opacity so they are barely noticeable.

**Why**: Supporting elements stay quiet.

**Anti-pattern**: Heavy, prominent dividers.

---
