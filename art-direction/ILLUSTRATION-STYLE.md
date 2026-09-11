# Illustration style guide

Art direction for any illustrated artwork added to the AvantStay guest
experience journey map, adapted from the pen-and-ink single-accent-color
formula used in the PayPal 3YP reference project
(`3yp-main/art-direction/ILLUSTRATION-STYLE.md`). Nothing here is measured
from an existing AvantStay plate set the way the reference was — there isn't
one yet — so treat these as starting parameters to lock in once the first few
plates exist, not settled facts.

## The one-sentence version

Loose black pen-and-ink line drawing with grey marker wash on a plain white
background, square, no outline or frame, with AvantStay navy used as the only
colour and only on the thing AvantStay actually touches — the booking app on
a phone, a keycard, a welcome folder.

## Target parameters

| Property | Value |
| --- | --- |
| Aspect ratio | 1:1 square, no exceptions |
| Pixel size | 1024 x 1024 |
| Format | JPEG or PNG, quality high enough to keep pen strokes crisp |
| Background | Pure white, no border, no drop shadow, no vignette |
| Colour coverage | Under 8% of pixels saturated — spot colour, not a colour illustration |
| Accent colour | AvantStay navy `#022B54` only |
| Fully monochrome plates | Normal and expected for any scene with no AvantStay-branded surface in frame |

That colour-coverage number is the constraint that matters most. These are
black-and-white drawings with a spot colour, not colour illustrations.

## Rules

**Line.** Sketchy, confident, visibly hand-drawn. Strokes overshoot corners and
double back. Contour lines are not closed or cleaned up. This should look like
a practised illustrator working quickly in ink, not a vector illustration.

**Shading.** Grey marker wash in flat, streaky blocks with visible stroke
edges, plus cross-hatching for deeper shadow. Two or three grey values only.
No smooth gradients, no airbrushing, no soft light.

**Colour.** Exactly one colour: AvantStay navy. Apply it only to the surface
AvantStay owns in that moment — typically the booking app on a phone screen,
a keycard or lockbox, a luggage tag, or a welcome folder. Everything else
stays monochrome, including other devices, clothing, and the environment. A
plate with no AvantStay surface in it should be fully monochrome.

**Composition.** Subject(s) centred, cropped at roughly waist or chest,
floating on white with no ground plane except a suggested surface line or a
soft wash shadow. Background detail fades out toward the edges rather than
filling the square.

**Cast.** Unlike the PayPal reference (one recurring persona, Amy), this
project has six named personas — Maya, Daniel, Bailey, the Whitfield family,
the Ashworths, the Renewals — each a different party size and travel style.
Match the cast to the scene: a solo guest for Maya, a returning couple for
Daniel, a group of friends for Bailey, a multigenerational family for the
Whitfields, a couple at a premium property for the Ashworths. Keep any one
recurring character consistent across plates the way the reference does with
Amy, if a plate set settles on a throughline character; otherwise let the
group composition itself carry each persona's identity, since "who's in the
frame" already reads as the story.

**Never.** Colour beyond the navy accent. Photorealism. 3D or gradient mesh.
Flat corporate vector style. Heavy black fills. Text or lettering of any
kind. Logos. Borders, frames, or rounded corners. Non-square crops.

## Generation prompt

Fill in the bracketed part. Keep the rest close to verbatim; it encodes the
rules above. Written for DALL·E 3, which has no separate negative-prompt
field — exclusions are folded into the sentence instead of split out.

> Black and white pen-and-ink sketch illustration of [subject and action],
> drawn with loose confident linework and visible overlapping strokes. Grey
> marker wash shading in flat streaky blocks with cross-hatching for shadow.
> Plain white background, no frame, no border. Square 1:1 composition,
> subject centred and cropped at the chest, background detail fading toward
> the edges. The only colour in the image is a deep navy blue, hex `#022B54`,
> used exclusively on [the phone screen / the keycard / the welcome folder],
> covering less than 5% of the frame. Everything else is pure black, white,
> and grey — no other colour anywhere. Editorial illustration style,
> hand-drawn, not vector, not photorealistic, not a corporate flat-design
> illustration, no text or lettering, no logo, no border or frame, no
> gradient or airbrush effect, no photorealism or 3D render.

If the subject has no AvantStay surface in it, delete the sentence about navy
and add: "Entirely monochrome, no colour anywhere."

For a tool that does support a separate negative prompt (Midjourney, Stable
Diffusion):

> colour, colored, vibrant, saturated, photorealistic, photograph, 3d render,
> vector art, flat design, corporate illustration, text, words, lettering,
> watermark, logo, border, frame, rounded corners, gradient, airbrush, glossy

## Ready-to-use examples

One per persona, matched to the moment each one is defined by in the journey
map. Maya's is done (`assets/illustrations/maya.jpg`) — the rest are
`placeholder`s on the live page until generated.

**Maya arriving at her weekend rental** (solo/small group, budget-conscious) — done:

> Black and white pen-and-ink sketch illustration of a young woman pulling a
> small wheeled suitcase up to a front door, checking her phone in her other
> hand, drawn with loose confident linework and visible overlapping strokes.
> Grey marker wash shading in flat streaky blocks with cross-hatching for
> shadow. Plain white background, no frame, no border. Square 1:1
> composition, subject centred and cropped at the chest, background detail
> fading toward the edges. The only colour in the image is a deep navy blue,
> hex `#022B54`, used exclusively on the phone screen showing a booking
> confirmation, covering less than 5% of the frame. Everything else is pure
> black, white, and grey — no other colour anywhere. Editorial illustration
> style, hand-drawn, not vector, not photorealistic, no text or lettering, no
> logo, no border or frame, no gradient or airbrush effect.

**Daniel, the direct-booking regular, letting himself in** (confident repeat behavior, no OTA middleman):

> Black and white pen-and-ink sketch illustration of a man in his thirties
> unlocking a front door with a smart-lock keypad, phone in his other hand
> showing a booking confirmation, relaxed and unhurried, drawn with loose
> confident linework and visible overlapping strokes. Grey marker wash
> shading in flat streaky blocks with cross-hatching for shadow. Plain white
> background, no frame, no border. Square 1:1 composition, subject centred
> and cropped at the chest, background detail fading toward the edges. The
> only colour in the image is a deep navy blue, hex `#022B54`, used
> exclusively on the smart-lock keypad, covering less than 5% of the frame.
> Everything else is pure black, white, and grey — no other colour anywhere.
> Editorial illustration style, hand-drawn, not vector, not photorealistic,
> no text or lettering, no logo, no border or frame, no gradient or airbrush
> effect.

**Bailey's Nashville celebration, group arrival** (bachelorette/milestone energy):

> Black and white pen-and-ink sketch illustration of three young women
> laughing together on a front porch, one holding up a phone to take a
> photo, one wearing a "bride" sash, suitcases at their feet, drawn with
> loose confident linework and visible overlapping strokes. Grey marker wash
> shading in flat streaky blocks with cross-hatching for shadow. Plain white
> background, no frame, no border. Square 1:1 composition, group centred and
> cropped at the waist, background detail fading toward the edges. The only
> colour in the image is a deep navy blue, hex `#022B54`, used exclusively
> on the phone screen, covering less than 5% of the frame. Everything else
> is pure black, white, and grey — no other colour anywhere. Editorial
> illustration style, hand-drawn, not vector, not photorealistic, no text or
> lettering, no logo, no border or frame, no gradient or airbrush effect.

**The Whitfield family reunion, coordinated arrival** (large multigenerational group):

> Black and white pen-and-ink sketch illustration of a multigenerational
> family — grandparents, parents, kids — unloading suitcases from a car in
> front of a large house, drawn with loose confident linework and visible
> overlapping strokes. Grey marker wash shading in flat streaky blocks with
> cross-hatching for shadow. Plain white background, no frame, no border.
> Square 1:1 composition, group centred and cropped at the waist, background
> detail fading toward the edges. The only colour in the image is a deep
> navy blue, hex `#022B54`, used exclusively on a keycard one of them is
> holding, covering less than 5% of the frame. Everything else is pure
> black, white, and grey — no other colour anywhere. Editorial illustration
> style, hand-drawn, not vector, not photorealistic, no text or lettering, no
> logo, no border or frame, no gradient or airbrush effect.

**The Ashworths, VIP concierge welcome** (premium property, white-glove service):

> Black and white pen-and-ink sketch illustration of a well-dressed couple
> in their fifties being greeted at an estate's front entrance by a
> concierge holding a tray, their luggage already being carried in by
> someone else, drawn with loose confident linework and visible overlapping
> strokes. Grey marker wash shading in flat streaky blocks with
> cross-hatching for shadow. Plain white background, no frame, no border.
> Square 1:1 composition, group centred and cropped at the waist, background
> detail fading toward the edges. The only colour in the image is a deep
> navy blue, hex `#022B54`, used exclusively on the concierge's tablet,
> covering less than 5% of the frame. Everything else is pure black, white,
> and grey — no other colour anywhere. Editorial illustration style,
> hand-drawn, not vector, not photorealistic, no text or lettering, no logo,
> no border or frame, no gradient or airbrush effect.

**The Renewals, a familiar welcome back** (repeat guest, recognized on arrival):

> Black and white pen-and-ink sketch illustration of a woman in her
> forties smiling as she reads a text message on her phone while standing
> on a familiar-looking porch, keys already in her other hand, relaxed and
> at ease, drawn with loose confident linework and visible overlapping
> strokes. Grey marker wash shading in flat streaky blocks with
> cross-hatching for shadow. Plain white background, no frame, no border.
> Square 1:1 composition, subject centred and cropped at the chest,
> background detail fading toward the edges. The only colour in the image is
> a deep navy blue, hex `#022B54`, used exclusively on the phone screen
> showing a "welcome back" message, covering less than 5% of the frame.
> Everything else is pure black, white, and grey — no other colour anywhere.
> Editorial illustration style, hand-drawn, not vector, not photorealistic,
> no text or lettering, no logo, no border or frame, no gradient or airbrush
> effect.

## Naming and wiring

Save finished plates to `assets/illustrations/`, named after the persona:
`maya.jpg`, `daniel.jpg`, `bailey.jpg`, `whitfield.jpg`, `ashworths.jpg`,
`renewals.jpg`. In `index.html`, each persona card in the "Who we serve"
grid has a `.portrait` div; swap the `.portrait.placeholder` markup for:

```html
<div class="portrait"><img src="assets/illustrations/NAME.jpg" alt="DESCRIBE WHAT'S HAPPENING" loading="lazy" width="88" height="88"></div>
```

Alt text is required — describe the moment, not "an illustration of a
person." Resize/compress before adding (`sips -s format jpeg -s
formatOptions 82 -z 1024 1024 input.png --out assets/illustrations/name.jpg`
on macOS) — the raw ChatGPT export runs ~2MB per image, which is too heavy
to ship six of on one page.

## Acceptance checklist

Before adding a plate to this project:

- [ ] Square, 1024 x 1024
- [ ] Background is pure white to the edges, no frame
- [ ] Navy appears on the AvantStay surface only, and nowhere else
- [ ] Navy covers well under 10% of the frame
- [ ] No text or logos anywhere
- [ ] Strokes read as hand-drawn, with visible overshoot
