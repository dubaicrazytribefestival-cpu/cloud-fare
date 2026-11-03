# FX-4 "The music tells you when to show off." (draft, silent)

Status: DRAFT for owner review. Nothing has been posted, uploaded or published.

## Files
- `reel_draft_silent.mp4`: 1080x1920, 30 fps, 32.0 s, 960 frames, H.264 yuv420p, +faststart, no audio track, ~3.1 MB
- `cover.jpg`: 1080x1920, the frozen "THE BREAK." moment (2.6 s)
- `frames/`: check stills pulled from the encoded MP4 at 0.0, 0.5, 1.2, 2.2, 3.0 and 15.0 s
- `caption.txt`: caption, 5 hashtags, pinned comment, DM line
- `AUDIO-CUES.md`: locked VO start/end times, SFX list, music mood/BPM, drop-out timing
- `build/`: `reel.js` (canvas scene code, `draw(t)`), `index.html`, `render.js` (Playwright → ffmpeg), fonts (Anton, Inter 600, copied from the FX-1 build so the series matches)

Re-render: `cd build && node render.js video` (or `node render.js stills 0,2.2,15 <dir>`).

## What's in it
| Time | Scene |
|---|---|
| 0–2.2 | A bachata social from frame 0: DJ booth (coral DJ panel, DJ bobbing in headphones), a spinning disco ball with coral sparkles, and three small ink couples in open hold stepping a basic on the 126 BPM beat along a floor line. In front, a waveform races across the full width (coral peaks) with the big ink dancer bouncing on it. The social floor freezes with everything else at 2.2. Claim builds word by word 1.20–1.75: THE MUSIC TELLS YOU / WHEN TO [SHOW OFF] |
| 2.2–3.0 | THE BREAK: waveform flatlines, dancer snaps into a freeze pose, coral flash + shake, freeze-frame corner brackets, "♪ MUSIC: SILENCE" chip, THE [BREAK.] slams in |
| 3–10 | Timeline: 6 phrases of 8 counts in 3 rows (counts 1–8 in 52 px Anton, phone-readable), a coral playhead lights the counts, coral pause markers on the gaps (BREAK / CHANGE / BREAK). Below, 4 grey figures keep stepping while the ink "YOU" dancer freezes in each gap. Headlines MOST SONGS HAVE [BREAKS] → LISTEN FOR THE [CHANGE] |
| 10–17.5 | Three options, chips 1 PAUSE · 2 SLOW DOWN · 3 HIT THE ACCENT with a big headline that lands ~0.1 s before each option starts (so 15.0 s already shows HIT THE ACCENT!): pause (hands on hips, pause icon), slow down (slow torso sway with ghost trails + HALF SPEED), hit the accent (fist-up pose with coral starburst). A mini waveform with the break gap runs under the playhead |
| 17.5–20 | STYLING. three mini dancers repeating the options, coral "0 NEW MOVES" |
| 20–26 | The circle: 6 grey figures stepping around the dancer ("WAIT FOR IT…"); at 21.4 the music strip flatlines, dancer freezes, coral spotlight + ring, grey figures stop, lean in, coral "!" pops over each, then they clap/cheer. THAT'S [MUSICALITY.] |
| 26–32 | End card: HEAR IT IN [CLASS.] · Foundation · Sun 8 PM / Thu 7:30 PM · JLT · "Beginner bachata with Saj & Emi" · small dancer on a waveform · pulsing coral panel COMMENT "MUSIC" |

Word-by-word captions (ink pill, cream text, active word coral) carry every VO line. "DUBAI BACHATA" wordmark top left the whole time. All text sits between y=300 and y=1600 (inside the 285 px top/bottom margins). Palette is only Cream/Ink/Coral/Warm Grey; figures are faceless pictograms; no sensual poses, no prices, no competitor or Bacha Fusion/BachaZouk mentions.

## Music drop-out (editor action needed)
The spec wants a real drop-out. This draft is silent, so the break is shown visually. **The editor must line the chosen song's drop-out up with 2.2 s** (silence 2.2–3.0 s, music back at 3.0 s). Second freeze at 21.4–23.4 s. Full details in `AUDIO-CUES.md`.

## 8-point first-3-seconds checklist (honest)
1. Frame 0 already moving: **PASS.** Waveform scrolling, dancer mid-bounce, notes floating at frame 0; no fade, no empty frame.
2. Something recognisable on frame 0: **PASS.** Frame 0 shows a bachata social: DJ booth, disco ball and couples stepping on the floor, plus the music waveform. It's a pictogram (no real venue or logo), but it reads as "a dance night" at a glance.
3. Biggest element ≥40% and moving from frame 1: **PASS as a group.** Waveform + dancer block covers roughly y 640–1480 (~44% of the frame) and moves constantly. The waveform alone is about 31%.
4. Something extraordinary before 3 s: **PASS.** At 2.2 s the waveform flatlines, the dancer freezes, a coral flash and a shake.
5. Claim lands 1.2–1.6 s word by word: **PASS.** First word pops at 1.20, last at 1.59, fully settled by 1.75. Big Anton, ink on cream with a coral pill on SHOW OFF. (The 1.2 s still shows the frame just before the first word appears.)
6. First spoken word within 0.5 s and it's the subject: **PASS by design, not verifiable in a silent file.** VO now opens on the viewer, "Your music tells you exactly when to show off.", cued at 0.30 s, and the caption shows "Your music…" from 0.30 s. The on-screen headline stays "THE MUSIC TELLS YOU WHEN TO SHOW OFF". It only truly passes once the VO is laid to `AUDIO-CUES.md`.
7. Works on mute: **PASS.** Every VO line is on screen as captions and the break is shown visually.
8. About the viewer: **PASS (moderate).** "Tells *you* when to show off" plus "everyone else keeps stepping" frames it as the viewer's own dancing.

Result: 8/8 by design. 7/8 can be verified in the silent draft, and #6 is set up correctly (caption + cue at 0.30 s, opens with "Your") but needs the VO recorded to confirm.

## Limitations
- Silent: no VO, music or SFX. VO timings are estimates at a brisk pace; the VO should be fitted to the locked windows in `AUDIO-CUES.md`.
- The "turn to look" in the circle is shown as a lean, a head nudge and "!" marks, because the figures have no faces.
- "Slow body roll" is drawn as a slow, neutral torso sway with ghost trails, deliberately not sensual.
- The small "PHRASE n · 8 COUNTS" labels above the timeline are still small (24 px); the count numbers themselves are now large.
- The social-floor couples and the DJ are small (about 150 px tall) so the waveform and main dancer stay dominant; at phone size they read as "people dancing", not individual moves.
- The disco ball hangs in the top 285 px; it's a graphic, not text, but the IG top bar may partly cover it.
- DM songs are TBC: caption.txt says "[3 songs: owner to choose]". The owner must add the MUSIC keyword auto-reply before posting.

## Revision 2 (coordinator fixes)
1. Frame-0 bachata social added (DJ booth, disco ball, 3 couples stepping at 126 BPM).
2. Opening VO is now "Your music tells you exactly when to show off." (caption updated; headline unchanged).
3. Timeline count numbers enlarged (26 px Inter → 52 px Anton in 54x86 cells); option headlines and chips pop ~0.4 s earlier, so the 15.0 s still shows HIT THE ACCENT!.
Video, cover, stills and AUDIO-CUES.md re-rendered/updated together.
