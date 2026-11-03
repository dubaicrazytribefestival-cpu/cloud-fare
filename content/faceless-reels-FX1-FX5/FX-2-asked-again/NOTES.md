# FX-2 "Same social. Same song. Only one gets asked again." Draft notes

**Status: DRAFT for owner review. Nothing has been posted, uploaded or published.** The file is silent. There is no VO, music or SFX yet; AUDIO-CUES.md has the timings for adding them.

## What's in the folder
- `reel_draft_silent.mp4`: 1080x1920, 30 fps, H.264 yuv420p, +faststart, no audio track. 30.00 s (900 frames), about 5.2 MB.
- `cover.jpg`: 1080x1920 frame at 2.8 s. It shows the full hook: "SAME SOCIAL. SAME SONG. ONLY ONE GETS ASKED AGAIN.", the A: 0 / B: 3 counters, the "Dance?" bubbles and the tumbleweed.
- `frames/still_{0.0,0.5,1.2,2.2,3.0,15.0}s.png`: check stills taken from the encoded MP4.
- `caption.txt`: caption line 1 + body, 5 hashtags, pinned comment, DM reply for AGAIN, alt text.
- `AUDIO-CUES.md`: exact VO start/end times (locked to the captions), SFX timestamps, music at 128 BPM, and drop-outs at 1.75–3.00 s and 12.40–13.30 s.
- `build/`: `reel.js` (canvas animation; `render(t)` draws any time t), `index.html`, `render.js` (Playwright steps t at 30 fps and pipes PNGs to ffmpeg; `node render.js video` or `node render.js stills <dir> <t…>`), and the fonts (Anton, Inter 600 from Google Fonts, copied from the FX-1 build so the series matches).

## What happens when
| Time | Scene |
|---|---|
| 0–3.0 | (Rev 2: zoomed split, B mirrored, "YOU?" tag 0–2 s, VO line 1 "You and him: …") Split dance floor (disco ball, grey crowd, tiled floor). A couple left, B couple right, coral "A/B · ASKED AGAIN: 0" counters. A's partner has a dizzy spiral and A's gaze line goes to his feet; B has a coral eye-contact line. Headline builds word by word from 1.08 s. Song ends at 1.75 and the couples step apart. Three "Dance?" bubbles fly to B and the counter ticks to 3, slamming at 2.25 with a burst and shake. A tumbleweed rolls past A from 2.15, then a "…" appears above A. |
| 3–9 | REPLAY of A: COMBO 1/6→6/6 ticks, partner spins (squash spin + swoosh arcs), dizzy spiral and sweat drops, gaze to own feet, three coral "YANK!" jolt lines. Headline "DANCER A: 6 COMBOS · 0 EYE CONTACT". |
| 9–15 | REPLAY of B: basic, one turn (10.4–11.4), coral eye-contact line, sparkles and "ha ha!", freeze with "PAUSE ON THE MUSIC" (12.4–13.3), connection meter 20→100%. Headline "DANCER B: 1 TURN · 100% CONNECTION". |
| 15–24 | Three tip cards (3 s each), with B demonstrating: 1 EYES UP (gaze to feet, coral X, then eye line connects), 2 MATCH THEIR LEVEL (YOU meter drops 5→2 to match THEM, then a check), 3 LEAVE SPACE (lets go, coral SPACE bracket, partner plays with notes). |
| 24–26.4 | Split again: "NEXT SOCIAL: A COPIES B." A now has eyes up and an eye line; a bubble flies in and A's counter ticks 0→1 (25.35). |
| 26.4–30 | End card: "BE THE DANCE THEY REMEMBER." with a small dancing couple, "Foundation · Sun 8 PM / Thu 7:30 PM · JLT" and a coral "COMMENT “AGAIN”" panel. |

Style: cream #F3EDE2 background, ink #171717 faceless pictograms (round heads, capsule bodies; partners wear a skirt silhouette), coral #EF7768 as the only accent, warm grey #A69F94 for secondary elements. Headlines are Anton uppercase; small text and captions are Inter 600. The "DUBAI BACHATA" wordmark sits top left the whole time (y≈294). All text stays between y 294 and 1612, inside the 285 px top and bottom margins. Captions use an ink pill with the active word in coral, and the keyword AGAIN stays coral. Scene changes are whip slides with speed lines. There are no prices, no competitor names, no Bacha Fusion or BachaZouk, and no sensual poses.

## Revision 2 (coordinator fixes)
1. **The viewer opens the reel.** VO/caption line 1 is now "You and him: same social, same song…" (0.30–1.40 s), with "You" in coral. A coral "YOU?" tag with two arrows, one to Dancer A and one to Dancer B, is on screen from frame 0, pulses, and fades out 1.78–2.00 s.
2. **Split screen zoomed in.** Couples are now scale 1.75 (was 1.3). B's half is mirrored so both leads sit on the outer edges and the "YOU?" arrows land on them. Each couple fills its half, clipped so nothing crosses the divider. The headline was tightened (70/100/100 px) and the counters moved up to y≈624–700.
3. **Clean loop.** In the last 0.3 s (29.70–30.00) the end card crossfades into the exact opening layout (`sceneHook` at t−30). Measured mean pixel difference between the last and first frames is 3.8/255, down from 19 when the stray caption was still showing.
4. **Dancer A's "looking at his feet" line** now runs from the front of his head to just past his front toe. It no longer crosses his body, in the hook, the A replay and tip card 1.
"NEXT SOCIAL: A COPIES B." is kept. AUDIO-CUES.md is updated (VO line 1, the YOU? tag, the loop point).

## Virality 8-point checklist (honest, revision 2)
1. **Frame 0 already moving: PASS.** Couples are mid-step, the YOU? tag and its arrows pulse, notes rise, the disco ball shimmers.
2. **Recognisable on frame 0: PASS.** A dance floor with couples, disco ball and crowd, plus readable "ASKED AGAIN: 0" counters. It's pictogram art rather than footage.
3. **Biggest element ≥40% and moving: PASS.** The split-screen dance panel (counters + two couples + floor, full width, y≈624–1612) is about 51% of the frame. The two couples' own bounding box (heads to feet) is about 36% of the frame (about 41% with the counters). On the coordinator's "panels together ≥50%" reading this passes. Measured by the dancers' silhouettes alone it would not.
4. **Extraordinary event before 3 s: PASS.** Bubbles fly in, the counter races 1-2-3 and slams at 2.25 s with a burst and shake, and a tumbleweed rolls past A.
5. **Claim at ~1.2–1.6 s, word by word, big: PASS.** "SAME SOCIAL. SAME SONG." builds from 1.08 s (visible at 1.2), then "ONLY ONE GETS ASKED AGAIN." at 100 px from 1.62 s.
6. **First spoken word ≤0.5 s and it's the subject: PASS on picture, pending audio.** The "You" caption appears at 0.30 s, and AUDIO-CUES puts the first VO word "You" at 0.30 s. The draft itself is still silent.
7. **Works on mute: PASS.** Every VO line is captioned word by word.
8. **About the viewer: PASS.** "You and him" plus the YOU? tag frame the viewer as A or B from frame 0.

**Result: 8/8 on picture.** Two caveats: #6 depends on the VO being recorded to AUDIO-CUES.md, and #3 passes on the panel measure (51%) rather than the silhouettes (about 36%).

## Limitations / things to check
- Silent draft: no VO, music or SFX (no TTS was available and no audio was downloaded). The audio layer must follow AUDIO-CUES.md.
- Spec item "partner laughs" and "a smile": the figures have no faces (brand rule), so laughter is shown as sparkles plus a small "ha ha!", and connection as a coral dotted eye line.
- Spins are drawn as a horizontal squash-and-stretch of the pictogram with swoosh arcs. They read as spins at speed, but a single still mid-spin shows a very thin figure.
- still_3.0s and still_15.0s land on the first frame of a whip transition, so they still show the outgoing scene (hook and B replay).
- The end card holds about 3.3 s before the loop crossfade starts.
- Before 1.08 s the headline zone (y≈340–600) is empty apart from the wordmark, because the claim builds at 1.2 s per the spec. The YOU? tag sits in the dance panel, not up there.
- With the bigger couples, the "Dance?" bubbles and the YOU? arrows overlap the dancers' bodies. They are outlined, so they stay readable.
- I added one beat not in the spec's on-screen column: the "NEXT SOCIAL: A COPIES B." headline at 24–26.4 s, to set up A's counter ticking to 1.
- The headline "DANCER A: 6 COMBOS · 0 EYE CONTACT" auto-shrinks to fit the width (about 85 px).
