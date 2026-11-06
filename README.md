# AI pet rap video guide

Notes for making a lip-synced rap clip — a cat, dog or person "spitting" a verse — from **one still photo**, and for posting it on TikTok, Reels and Shorts without the punchline hidden behind UI.

A single-photo lip-sync model has to invent a moving mouth, jaw and head from one frame. How good that looks depends mostly on the photo: whether the mouth area is visible, sharp and lit, and whether the head is close to frontal.

- [Choosing and framing the photo (pets and people)](docs/01-photo-for-lip-sync.md)
- [12-second clips: BPM, bars, captions and safe zones](docs/02-12-second-rap-timing.md)

## The one-minute version

| Check | Good | Bad |
|---|---|---|
| Faces in the photo | exactly one | two pets, pet + owner's face |
| Head angle | frontal or up to ~30° | profile, looking up at the owner |
| Mouth / muzzle | fully visible, closed or slightly open | covered by a toy, paw, hand, food bowl |
| Camera height | at the pet's eye level | from standing height looking down |
| Face size | head ≥ 25–30% of image height | tiny pet in a big room |
| Face pixels | ≥ 300 px across the head | screenshot of a screenshot |
| Light | daylight, soft | backlit window, dark room, flash red-eye |
| Fur colour | true to life (daylight) | orange cast from bulbs |
| Eyes | open, visible | squinting, closed, covered by hair |
| Edits | none | stickers, beauty filters, heavy sharpening |

## Common failures

| What you see | Likely cause | Fix |
|---|---|---|
| Mouth moves like a puppet flap | Muzzle in shadow or small in frame | Closer, brighter photo; muzzle clearly lit |
| Teeth/tongue appear out of nowhere | Photo with mouth wide open (yawn, pant) | Mouth closed or barely open |
| Different-looking cat or dog | Shot from above; warm light shifted fur colour | Eye-level daylight photo |
| Second animal starts "rapping" too | Two faces in the photo | Crop to one face |
| Head warps when it bobs | Profile or strongly tilted head | Frontal photo, tilt < 15° |
| Whiskers / ears flicker | Over-sharpened or upscaled source | Use the original camera file |
| Caption hides the mouth | Text placed in the bottom 20% | Captions in the upper-middle band (see doc 02) |

## Tool

Written while making clips with [Rap Video Generator](https://rapvideogenerator.app), which turns one photo into a 12-second, 720p vertical rap video with an original AI verse and the rap track included. The cat-specific page ("Eminem cat" style battle rap) is [AI cat rap video](https://rapvideogenerator.app/effects/cat-rap-video).

The photo checks apply to any single-image lip-sync or talking-head model.

## License

Text: CC BY 4.0.
