# 12-second rap clips: BPM, bars, captions and safe zones

## 1. How much rap fits in 12 seconds

```
seconds per beat   = 60 / BPM
beats in 12 s      = BPM / 5
bars (4/4) in 12 s = BPM / 20
```

| BPM | Seconds per beat | Beats in 12 s | Bars in 12 s | Typical style |
|---|---|---|---|---|
| 70 | 0.857 | 14 | 3.5 | slow trap (often counted as 140 half-time) |
| 80 | 0.750 | 16 | 4 | boom bap, lo-fi |
| 90 | 0.667 | 18 | 4.5 | classic hip-hop |
| 100 | 0.600 | 20 | 5 | upbeat |
| 140 | 0.429 | 28 | 7 | trap / drill (double-time feel) |
| 160 | 0.375 | 32 | 8 | fast drill, "battle" energy |

So a 12-second clip is roughly **4 bars at 80 BPM** or **8 bars at 160 BPM**. In practice that is 4–8 lines of verse — enough for a setup and one punchline.

Syllable density (useful for judging if a verse will lip-sync cleanly):

| Flow | Syllables per beat | Syllables in 12 s at 90 BPM |
|---|---|---|
| Relaxed | 2 | ~36 |
| Standard 16th-note flow | 4 | ~72 |
| Chopper / "Eminem cat" speed | 5–6 | ~90–108 |

Faster flows look funnier on a cat, but every syllable is a mouth shape. If the mouth looks smeared, the photo usually is the limit (see doc 01), not the speed.

## 2. Where to put the punchline

- Most viewers decide in the first 1–2 seconds. The first audible word should start within ~0.5 s; a long instrumental intro loses people.
- The punchline lands best in the **last bar** (the final ~2.4–3 s at 80–100 BPM), so the clip loops straight back into the start of the verse.
- Make the loop seamless: if the last frame and first frame are similar (same pose at the mic), the replay feels continuous and is counted as a rewatch.

## 3. Captions and safe zones (1080 × 1920)

Platform UI overlays change with app versions; these are conservative margins:

| Region | Approx. pixels on 1080 × 1920 | Covered by |
|---|---|---|
| Top | 0–~220 | status bar, tabs, search |
| Bottom | ~1500–1920 (bottom ~20%) | caption, username, music ticker |
| Right | ~950–1080 (right ~12%) | like / comment / share / sound buttons |
| Reels profile grid | outside centre 1080 × 1440 | cropped from the grid view |

- Keep burned-in lyric captions in roughly **x 60–940, y 260–1480**; for a 720 × 1280 source that is x 40–627, y 173–987.
- **Never put captions over the mouth.** The mouth is the whole joke. For a frontal head-and-shoulders framing, the mouth usually sits around 45–60% of the frame height; place lyrics above the head (y ≈ 260–600 on 1080 × 1920) or in a band just below the chin if the head is high in frame.
- Caption size: ~48–64 px cap height on 1080 wide; 2 lines max; high-contrast with a stroke or shadow.
- One line per bar is easy to read at 80–100 BPM. At 140+ BPM show half-lines or only the punchline.

## 4. Audio

- Rap clips that already contain the track should be posted **with their own audio**. Muting and adding a trending sound drops the lip-sync.
- Loudness: platforms normalise playback; aim for around −14 LUFS integrated, true peak ≤ −1 dBTP, so it is not turned down or clipped.
- AAC-LC, 44.1 or 48 kHz, 128–320 kbps.

## 5. Export settings if you edit before posting

| Setting | Value |
|---|---|
| Container | MP4 (`+faststart`) |
| Video | H.264 High, yuv420p, same frame rate as source |
| Resolution | source (720 × 1280) or 1080 × 1920 |
| Bitrate | 8–12 Mbps at 720p, 12–20 Mbps at 1080p |
| Audio | keep the original track; AAC 192 kbps if re-encoding |

Burn captions with ffmpeg (subtitle file `lyrics.srt`, styled, kept inside the safe zone):

```bash
ffmpeg -i rap.mp4 -vf "subtitles=lyrics.srt:force_style='Fontsize=18,Outline=2,Alignment=8,MarginV=60'" \
  -c:v libx264 -profile:v high -crf 18 -pix_fmt yuv420p -c:a copy -movflags +faststart out.mp4
```

`Alignment=8` puts captions top-centre (above the head) instead of the default bottom position, which would be under the platform caption.

Write `lyrics.srt` timings on the beat grid: at 90 BPM one bar is 2.667 s, so lines start at 0.000, 2.667, 5.333, 8.000, 10.667.
