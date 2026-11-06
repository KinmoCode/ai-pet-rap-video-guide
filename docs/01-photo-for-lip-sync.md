# Choosing and framing the photo for single-image lip-sync

## Why the photo matters more than usual

Image-to-video lip-sync drives the mouth region from audio. It needs to know where the lips (or muzzle edges), jaw line and teeth are. With one input frame, anything hidden, blurred or in shadow there gets invented — and invented mouths are what make a clip look fake.

## 1. One face, frontal

- **Exactly one face.** If a second face (another pet, the owner in the background, a face on a poster) is visible, crop it out. Models sometimes animate both.
- **Frontal to three-quarter (≤ ~30°).** The mouth has to be visible on both sides for convincing rapping. Profile photos give one lip line.
- **Head tilt < ~15°.** Cats tilt a lot; pick the straightest frame from a burst.

## 2. Camera height and distance

- **At the animal's eye level.** Get down to the floor or put the pet on a sofa at your eye level. Photos from standing height (looking down) show forehead and back, shrink the muzzle and make the "looking into the mic" framing impossible.
- **Distance.** Phone main lens at ~0.5–1 m, or the 2× lens from ~1–1.5 m. Very close wide-angle shots (< 30 cm) balloon the nose; that is cute in a still but looks rubbery once animated.
- For people: chest-up, phone at eye level, ≥ 1 m away or 2× lens. Arm's-length selfies work but exaggerate the nose.

## 3. Size and resolution

| Measure | Target |
|---|---|
| Head height in the image | ≥ 25–30% of image height |
| Pixels across the head | ≥ 300 px, more is better |
| Long edge of the file | ≥ 1024 px after cropping |
| File type | original JPG/HEIC/PNG from the camera roll |

Crop rather than upscale. AI upscalers add fur and skin texture that the video model then animates as real detail, which shows up as shimmering whiskers and eyebrows.

Photos forwarded through messaging apps are often re-compressed to ~1600 px long edge with blocky JPEG artefacts around the mouth. Use the original from the phone that took it.

## 4. Light and colour

- **Daylight, soft.** Next to a window (window beside you, not behind the pet) or outside in shade.
- **No backlight.** A bright window behind the pet leaves the face dark and noisy.
- **No flash.** Flash produces eye-shine (green/yellow in cats, red in dogs) and flattens the muzzle so the mouth edges disappear.
- **Watch warm bulbs.** Household bulbs are around 2700–3000 K. A grey cat can look ginger in an evening photo; the model keeps the wrong colour, or "corrects" it into a different-looking animal. Daylight is ~5000–6500 K.
- **Black pets:** expose for the face; a slightly brighter photo with visible fur detail around the mouth beats a dramatic dark one.
- **White pets:** avoid clipped highlights; tap to expose on the face.

## 5. Mouth and expression

- **Mouth closed or barely open.** A yawning or panting photo shows teeth and tongue, and the model then has to close and reopen them on every syllable.
- **Nothing in or near the mouth:** no toys, treats, paws, hands, food bowls, collars pulled up.
- **Eyes open.** Squinting or half-closed eyes stay half-closed in most frames.
- **People:** neutral face or slight smile; no sunglasses; hair off the mouth; no face masks.

## 6. Background and props

Backgrounds are usually replaced or restyled into a stage/studio, but busy backgrounds still make it harder to separate the head. Plain sofa, wall or floor is ideal. Accessories (hats, chains, sunglasses on the head) can survive; things that cross the face can not.

## 7. Before you upload

1. One face, frontal, tilt < 15°.
2. Eye-level shot, head ≥ 25–30% of the frame.
3. Original file, ≥ 300 px across the head, no filter or upscale.
4. Daylight, no flash, no backlight, true fur/skin colour.
5. Mouth visible, closed or barely open, nothing in front of it.
