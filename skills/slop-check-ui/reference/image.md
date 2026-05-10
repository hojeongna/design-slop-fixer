# Image (UI)

Image size, aspect ratio, treatment, usage rules

- **Total canonical rules**: 59
- **Sub-categories**: 13

---

## Contents
- Image aspect ratio — 6 canonical
- Content over images — 9 canonical
- Image selection — 12 canonical
- Expressing depth — 8 canonical
- Image effects — 5 canonical
- Icons — 5 canonical
- Image size — 4 canonical
- Graphic assets — 3 canonical
- Maps and markers — 2 canonical
- Data visualization — 2 canonical
- Image overlap — 1 canonical
- Background images — 1 canonical
- Image context — 1 canonical

---

## Image aspect ratio (6 canonical)

### [IMG-RATIO-CONSIST] Unify image aspect ratio within a section
- **Platform**: Mobile/PC
- **Frequency weight**: 8
- **Sub-category**: Image aspect ratio

**Principle**: Keep a single aspect ratio for all images within the same section, component, or gallery. Size variation is fine; ratio variation is not. A unified ratio alone can still produce a dynamic layout.

**Why**: Ratio consistency is the foundation of visual order, and mixed ratios force operators to register and process each image individually.

**Anti-pattern**: Mixing square, portrait, and landscape ratios in a single section, producing a cluttered layout.

---

### [IMG-RATIO-DISTORT] Never distort image aspect ratio to fit
- **Platform**: PC
- **Frequency weight**: 4
- **Sub-category**: Image aspect ratio

**Principle**: Do not stretch or squash an image to fit its container. Fit it through crop or clip instead.

**Why**: A distorted image looks immediately wrong and undermines trust in the product itself.

**Anti-pattern**: Product cards with flattened shoes or billboards with elongated models.

---

### [IMG-RATIO-MAINT] Treat ratio variety as maintenance debt
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Image aspect ratio

**Principle**: A variety of image ratios will create operations and maintenance problems down the line. Lock the ratio in as a fixed policy value.

**Why**: Operators end up reprocessing every image to match the ratio, which wastes resources.

**Anti-pattern**: Leaving the thumbnail ratio open so each new post requires custom processing.

---

### [IMG-RATIO-CROP] Crop with care; do not make it the default
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Image aspect ratio

**Principle**: Cropping is a useful tool, but it can cut into the subject. Do not treat it as the default approach; keep the source aspect ratio whenever possible.

**Why**: Automatic cropping is mechanical, not intentional, so it can slice off the parts that matter most.

**Anti-pattern**: Force-cropping every image to unify the ratio, which slices off subjects' heads.

---

### [IMG-RATIO-STD] Use the domain's standard aspect ratio
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Image aspect ratio

**Principle**: Follow the domain's standard ratio for content like video thumbnails (for example, 16:9). Non-standard ratios feel off.

**Why**: Users are accustomed to standard ratios, so anything else creates cognitive friction.

**Anti-pattern**: Pairing a YouTube-style video with a 4:3 thumbnail.

---

### [IMG-RATIO-PROC] Always process images that don't match the ratio
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image aspect ratio

**Principle**: Never drop an image straight into a banner if its ratio does not match. Retouch it to fit the ratio first, then use it.

**Why**: Ignoring the source aspect ratio undermines overall polish.

**Anti-pattern**: Dropping a narrow image into a wide banner as-is, leaving an awkward result.

---

## Content over images (9 canonical)

### [IMG-OVERLAY-GRAD] Gradient dim (bottom to middle, around 50%)
- **Platform**: PC
- **Frequency weight**: 3
- **Sub-category**: Content over images

**Principle**: Secure text legibility over an image with a bottom-to-middle gradient (about 50% opacity) rather than a full-frame dim. It feels natural and keeps the image alive.

**Why**: A full-frame dim kills the image; a gradient delivers both image presence and legibility.

**Anti-pattern**: Laying a full 50% black box over the image so the image disappears.

---

### [IMG-OVERLAY-STRENGTH] Tune overlay strength — legibility vs. image
- **Platform**: Mobile/PC
- **Frequency weight**: 6
- **Sub-category**: Content over images

**Principle**: Set overlay strength only as high as needed to secure stable text legibility. Too weak and legibility wavers; too strong and the image dies.

**Why**: Guarantees consistent legibility no matter which image is loaded.

**Anti-pattern**: A 5% opacity overlay leaves text invisible on bright images.

---

### [IMG-OVERLAY-WHITE-LIGHT] Subtle white overlay (10-20%) as a legibility aid
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Content over images

**Principle**: Even when text on an image already reads, a thin 10-20% white overlay raises legibility further without harming the image.

**Why**: A strong overlay kills the image, while a light one only reinforces baseline legibility.

**Anti-pattern**: Bolding the font only and skipping any extra legibility aid.

---

### [IMG-OVERLAY-COUNT] Use only one gradient overlay
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Content over images

**Principle**: Keep gradient overlays to a minimum and avoid stacking them beyond what is necessary. Each added layer pushes the image too dark.

**Why**: Stacking overlays produces results that diverge from the original intent.

**Anti-pattern**: Stacking three gradient overlays so the image is barely visible.

---

### [IMG-OVERLAY-INSET] Inset blurred elements on white backgrounds
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Content over images

**Principle**: When placing an element with a backdrop blur on a white background, inset it into the background so the background's edges remain clearly visible.

**Why**: Blur on a white background blurs the edges into mush.

**Anti-pattern**: Dropping a blurred white panel directly onto a white background.

---

### [IMG-OVERLAY-VERIFY] Verify legibility against real images
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Content over images

**Principle**: Do not validate against the design-time image only. Drop in a range of real images and verify legibility against each. Text that only reads on a gray placeholder is a trap.

**Why**: If you do not simulate image variability during design, legibility problems will surface after launch.

**Anti-pattern**: Validating the design with a single dummy image.

---

### [IMG-OVERLAY-CONTEXT-SPLASH] Keep splash screens image-forward (light dim)
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Content over images

**Principle**: On a splash screen, image, text, and effects must all read clearly. The dim is a legibility aid, not a layer for covering the image.

**Why**: A splash flashes by in a moment; if the image cannot be seen, it serves no purpose.

**Anti-pattern**: Burying the splash background image under an 80% black dim.

---

### [IMG-OVERLAY-DOM] Don't let overlays bury the image
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Content over images

**Principle**: When overlaying information onto an image, keep the image as visible as possible and treat it cleanly. Avoid approaches that completely cover the image.

**Why**: If you are going to obscure the image, you may as well not use one.

**Anti-pattern**: An information overlay covering 95% of the image underneath.

---

### [IMG-OVERLAY-FADE] Use a gradient fade in place of a flat dim
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Content over images

**Principle**: When darkening a background image, a bottom gradient fading from black to transparent feels more natural than a plain semi-transparent black dim.

**Why**: A gradient has direction, which aligns with the viewer's line of sight.

**Anti-pattern**: A 30% black box covering the entire image.

---

## Image selection (12 canonical)

### [IMG-SELECT-FOCUS] One focal subject plus breathing room
- **Platform**: PC
- **Frequency weight**: 3
- **Sub-category**: Image selection

**Principle**: Prefer images with a clear central subject and ample negative space. Images cluttered with many elements complicate the screen.

**Why**: A single focus delivers meaning instantly; negative space provides breathing room.

**Anti-pattern**: Using a busy image packed with multiple elements.

---

### [IMG-SELECT-IMPACT] Image choice is 70-80% of the polish
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: On image-driven sites, the choice and placement of imagery accounts for 70-80% of overall design polish. A great layout cannot rescue weak images.

**Why**: The image itself is the design; the wrong image cannot be saved by any layout.

**Anti-pattern**: Spending 90% of the time on layout and 10% on image selection, ending up with a mediocre result.

---

### [IMG-SELECT-PERSP] Heroes need perspective and composition
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Choose hero images with strong perspective and composition that put the subject in the spotlight. Flat images have low pulling power.

**Why**: Large areas require a sense of depth to land with impact.

**Anti-pattern**: Using a monotonous flat illustration as the hero.

---

### [IMG-SELECT-WEIGHT] Don't anchor visual weight on images alone
- **Platform**: PC
- **Frequency weight**: 2
- **Sub-category**: Image selection

**Principle**: Do not rely on images alone for the design's center of gravity. Distribute visual weight through non-image elements such as black or bold-color backgrounds as well.

**Why**: Leaning entirely on images makes the design feel heavy and cluttered.

**Anti-pattern**: A strong image in every hero and section, making the page feel heavy.

---

### [IMG-SELECT-RHYTHM] Alternate strong and soft tones
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: When laying out multiple images, alternate strong and soft tones to create visual balance and rhythm.

**Why**: Tones skewed in one direction feel oppressive.

**Anti-pattern**: Lining up five uniformly dark images.

---

### [IMG-SELECT-FOCUS-PRODUCT] Product images must lead the eye to the product
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Pick product photos that focus the eye on the hero (the product itself). Avoid images where another subject steals attention.

**Why**: On a product site, the product is the protagonist.

**Anti-pattern**: A perfume product image where the eye is drawn to the model's fingernails.

---

### [IMG-SELECT-CURATE] Curation matters more than retouching
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Initial image curation matters more than retouching. From a pool of 100 sources, pick the well-composed ones first, then retouch.

**Why**: A good original lowers retouching cost and raises the final result.

**Anti-pattern**: Grabbing any image and patching it with generative fill.

---

### [IMG-SELECT-VOLUME] Judge by volume plus color-tone combination
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Select images on two criteria: (1) the subject's visual volume (its weight within the frame) and (2) a color tone that fits the overall page's tone and manner.

**Why**: Evaluating on two axes secures consistency in image selection.

**Anti-pattern**: Judging on volume alone and ignoring color tone, leaving the page tone misaligned.

---

### [IMG-SELECT-WHITESPACE] Image plus negative space equals immersion
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Immersion peaks when an image is paired with enough negative space. Centered with surrounding whitespace, the image and the layout create synergy.

**Why**: Negative space makes the image stand out more.

**Anti-pattern**: Filling the image edge-to-edge so there is no breathing room.

---

### [IMG-SELECT-COMPLEX] Complexity often originates from the image
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Complexity in a web or UI design often originates from the image, not the layout. Image selection sets the overall mood.

**Why**: Designers burn time debugging the layout when the real culprit is the image.

**Anti-pattern**: Tearing up the layout first whenever something feels complex.

---

### [IMG-SELECT-LAYOUT] Consider layout and image together
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: Even a strong layout can fall apart with the wrong image. Consider image and layout in parallel.

**Why**: Layout and imagery are an inseparable pair.

**Anti-pattern**: Locking the layout first and slotting images in afterward.

---

### [IMG-SELECT-BG-MINIMAL] Choose images with simple backgrounds (focus on the subject)
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Image selection

**Principle**: In fashion and editorial design, choose images with simple backgrounds that let the subject hold attention.

**Why**: A busy background reduces the subject's pull.

**Anti-pattern**: Running a portrait spread on an image where multiple background elements compete with the subject.

---

## Expressing depth (8 canonical)

### [IMG-3D-INNER-MULTI] Use 5+ inner-shadow layers
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: When expressing depth with inner shadow, apply at least five separate layers to each face (top, bottom, left, right, and the highlight) for a natural, refined result.

**Why**: One or two layers leave the faces visibly broken; multi-layering reads naturally.

**Anti-pattern**: Applying only one inner shadow, producing a fake-looking sense of depth.

---

### [IMG-3D-TEXT-TIGHT] Keep blur tight on text inner shadows
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: Inner shadow on text needs a small, tight blur value (around 1.5) to preserve crisp depth.

**Why**: A large blur kills both text legibility and the sense of depth.

**Anti-pattern**: An inner shadow blur of 10 on text leaves it muddy and unclear.

---

### [IMG-3D-DARK-LIGHT] Pair dark with light (light-shadow contrast)
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: The core rule for depth: every dark area must have a matching light area. The contrast between light and shadow is what creates dimensionality.

**Why**: One side alone reads as flat; only contrast yields depth.

**Anti-pattern**: An inner shadow on the dark side only, leaving the form flat.

---

### [IMG-3D-GRAD-3STEP] Build 3D gradients in three steps
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: Structure 3D-feeling gradients in a three-step soft-medium-strong sequence to render light and shadow on a face naturally.

**Why**: A simple two-step gradient reads flat.

**Anti-pattern**: A two-color light-to-dark gradient that lacks depth.

---

### [IMG-3D-LIGHT-DIAGONAL] Cast light diagonally with a layered blur
- **Platform**: Mobile/PC
- **Frequency weight**: 2
- **Sub-category**: Expressing depth

**Principle**: When applying a gradient to an object, place soft-to-strong values along a diagonal to express natural light reflection. A white-to-transparent gradient plus a layered blur creates the light-source effect.

**Why**: A diagonal feels more natural than a vertical or horizontal gradient.

**Anti-pattern**: A top-to-bottom gradient only.

---

### [IMG-3D-METHOD-INNER-OVER-FACET] Prefer inner shadow over splitting faces
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: Express depth by layering inner shadow and gradient softly rather than physically splitting the faces; the connection between surfaces stays natural that way.

**Why**: Splitting faces creates breaks; layering preserves continuity.

**Anti-pattern**: Drawing each face as a separate shape to fake depth.

---

### [IMG-3D-DETAIL] Depth requires every detail to land
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: Depth on a graphic object needs every detail dialed in: shadow, inner shadow, gradient, and light reflection. Polish comes from setting them all carefully.

**Why**: Depth is the sum of accumulated detail.

**Anti-pattern**: Applying one or two effects and expecting depth.

---

### [IMG-3D-FLOAT-SHADOW] Add a floor shadow to floating objects
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Expressing depth

**Principle**: Always add a floor shadow beneath an object that floats in mid-air to establish spatial presence and a sense of reality.

**Why**: Floating without a shadow looks unreal.

**Anti-pattern**: A speech bubble or card floating with no floor shadow.

---

## Image effects (5 canonical)

### [IMG-FX-BLUR] Use blur only when there is intent
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Image effects

**Principle**: Do not apply blur to an image without a specific intent. It makes the design feel complicated and messy.

**Why**: Blur is a tool; unintentional use becomes noise.

**Anti-pattern**: Laying blur behind a hero slide for no reason.

---

### [IMG-FX-BLUR-DEPTH] Pair blur with layered depth
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image effects

**Principle**: When using blur, express the foreground-background relationship (the depth between layers) alongside it; that is what completes the sense of dimension.

**Why**: Blur on its own halves the effect; tie it to depth.

**Anti-pattern**: Applying blur alone, leaving a flat blur effect.

---

### [IMG-FX-RESTRAINT] Restrain effects; reserve them for the core
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Image effects

**Principle**: On the main billboard, minimize unnecessary effects and prioritize the image's focus. The more graphic shapes and effects you combine, the more complexity rises.

**Why**: More effects do not make the design stronger.

**Anti-pattern**: Stacking gradient, shadow, blur, and light reflection on the hero.

---

### [IMG-FX-SHADOW-LAYER] Build shadows as a separate gradient layer
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image effects

**Principle**: For a gradient shadow at the bottom of an image, building a dedicated overlay layer with gradient and blur is more natural and easier to control than a drop-shadow property.

**Why**: drop-shadow is limited; a hand-built layer is more refined.

**Anti-pattern**: Trying to fake a natural shadow with drop-shadow alone.

---

### [IMG-FX-SPARKLE] Limit accent effects to one or two spots
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Image effects

**Principle**: Accent effects like sparkles and highlights only land when used in one or two places. Spread them around and the emphasis disappears.

**Why**: The emphasis paradox — emphasizing everywhere emphasizes nothing.

**Anti-pattern**: Putting sparkles on the heart, the speech bubble, and the logo all at once.

---

## Icons (5 canonical)

### [IMG-ICON-SIZE] Make visual-communication icons large enough
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Icons

**Principle**: Place icons whose job is visual communication (weather, categories, and similar) large enough that content changes are recognizable at a glance.

**Why**: Tiny icons fail to communicate meaning.

**Anti-pattern**: A weather icon dropped in at around 16 px.

---

### [IMG-ICON-TONE] Keep icon tone, manner, and color consistent
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Icons

**Principle**: Unify the icon color range to match the UI's tone and manner. When using free sources, always verify color consistency.

**Why**: Icons live as a system, and unity is the key.

**Anti-pattern**: Mixing Lucide, Material, and custom icons with mismatched colors.

---

### [IMG-ICON-WEIGHT] Unify icon weight
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Icons

**Principle**: Choose icon stroke weight to align with the overall design's tone. Excessively thick icons weigh the design down.

**Why**: Different weights collide inside the same design system.

**Anti-pattern**: Body text is in a thin font, but the icons use a 4 px stroke.

---

### [IMG-ICON-3D] Use 3D icons to add weight
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Icons

**Principle**: When the design lacks visual weight, swapping icons to a 3D style is an effective way to anchor the center of gravity.

**Why**: 3D icons carry impact on their own.

**Anti-pattern**: Using only flat line icons, leaving the screen feeling bland.

---

### [IMG-ICON-OFFICIAL] Use official icons for social login
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Icons

**Principle**: Use the official icon for social login, and present it cleanly with no unnecessary custom detail or cropping.

**Why**: Preserves user recognition and respects the brand guideline.

**Anti-pattern**: Customizing the Google icon arbitrarily so it ends up clipped.

---

## Image size (4 canonical)

### [IMG-SIZE-INTENT] Big enough to read intent; otherwise drop it
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Image size

**Principle**: If you are going to use an image, make it large enough that its intent is legible. If it is too small to read, leaving it out is the cleaner choice.

**Why**: An image is only valuable when its intent matches the visual outcome.

**Anti-pattern**: A 1 cm decorative image on the side that no one can identify.

---

### [IMG-SIZE-BOLD] Go boldly large with images
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image size

**Principle**: Use images at a boldly large size to lift visual impact and polish. Shrunk to icon scale, an image might as well not be there.

**Why**: Large images create immediate visual value.

**Anti-pattern**: The image sits next to text at icon scale.

---

### [IMG-SIZE-NOFRAG] Don't fragment images; show them spaciously
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Image size

**Principle**: Show images as large and as spaciously as possible. Splitting them into multiple pieces on a single screen sharply raises complexity and scatters the eye.

**Why**: Fragmentation raises visual processing cost and lowers focus.

**Anti-pattern**: Chopping a hero image into four cards.

---

### [IMG-SIZE-LOGO] Size logos so they can be recognized
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Image size

**Principle**: Display the logo at a size users can recognize instantly. Legibility and recognizability come before any decorative placement.

**Why**: The logo is the brand identification point; if it cannot be recognized, it serves no purpose.

**Anti-pattern**: A new brand's logo placed small in the top-left corner where no one notices it.

---

## Graphic assets (3 canonical)

### [IMG-ASSET-QUALITY] Asset quality first — drop low-quality assets
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Graphic assets

**Principle**: Free graphic assets do not come with a quality guarantee. When picking assets like illustrations or icons, evaluate quality first; if it is low, you are better off without them.

**Why**: Low-quality graphics chip away at the design's overall polish.

**Anti-pattern**: Dropping a free Freepik illustration in as-is, leaving an awkward quality level.

---

### [IMG-ASSET-LINE] Simplify to line art when quality is low
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Graphic assets

**Principle**: When graphic quality is low, simplify to line art or a dotted-line treatment rather than a full-color illustration. Simple, clean graphics beat complex, low-quality ones.

**Why**: A line treatment makes it easier to establish consistency in the design itself.

**Anti-pattern**: Leaving a low-quality color illustration as-is, creating clutter.

---

### [IMG-ASSET-FIT] Lay out for the asset you actually have
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Graphic assets

**Principle**: Design the layout realistically around the character of the image assets you actually have (whether they have a background, their composition). The layout only works when the imagery can carry it.

**Why**: Without assets that fit the desired layout, no result will land.

**Anti-pattern**: A layout that needs transparent PNGs, but only background-filled images are available.

---

## Maps and markers (2 canonical)

### [IMG-MAP-VIS] Make map markers stand out (stroke and shadow)
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Maps and markers

**Principle**: Markers on a map need visual emphasis like a white stroke and a drop shadow so they stand apart from the background.

**Why**: On a map, the marker is the point; if it cannot be seen, the feature fails.

**Anti-pattern**: A faint 10 px gray marker.

---

### [IMG-MAP-EDGE] Soften gradient edges with a light blur
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Maps and markers

**Principle**: When the edge of a gradient or overlay is too sharp, apply a light blur (1-2 px) to soften it naturally.

**Why**: A hard edge feels unnatural.

**Anti-pattern**: A directional-indicator gradient with an edge as sharp as a knife cut.

---

## Data visualization (2 canonical)

### [IMG-VIZ-REFERENCE] Show a reference value (anchor point) on charts
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: In data visualization, mark the position of a reference value such as the mean or median clearly. Without an anchor point, viewers cannot perceive relative position.

**Why**: A visualization without a reference cannot communicate the meaning of the data.

**Anti-pattern**: Drawing the bars only and omitting the average line.

---

### [IMG-VIZ-LINE] Keep graph lines thin and color restrained
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Data visualization

**Principle**: Use thin lines and a restrained color palette for graphs; even strong colors stay in harmony with the rest of the screen. Darkening the background tone slightly lets the graph float forward naturally.

**Why**: A thick, loud graph hijacks the eye.

**Anti-pattern**: A 5 px deep-red graph line.

---

## Image overlap (1 canonical)

### [IMG-OVERLAP-CARE] Overlap shapes onto images with care
- **Platform**: Mobile/PC
- **Frequency weight**: 1
- **Sub-category**: Image overlap

**Principle**: Before overlapping shapes or text boxes onto an image, decide explicitly whether the image or the title is the one being emphasized.

**Why**: Overlap can make the image read as fragmented.

**Anti-pattern**: A large shape overlapped onto a thumbnail, fragmenting the image.

---

## Background images (1 canonical)

### [IMG-BG-INFO-NONE] No background images in info-heavy sections
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Background images

**Principle**: Avoid using background images unnecessarily in information-heavy sections. A background image should never command more attention than the content itself.

**Why**: When a background image competes with the content, legibility suffers.

**Anti-pattern**: Laying an image behind the FAQ section as a background.

---

## Image context (1 canonical)

### [IMG-CONTEXT-ONBOARD] Place a visual anchor at the top of onboarding
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Image context

**Principle**: At the top of an onboarding screen, place a relevant image, illustration, or icon to create a visual anchor and reinforce the screen's purpose.

**Why**: Text alone is monotonous and fails to grab attention.

**Anti-pattern**: An onboarding screen that is just a title and text.

---
