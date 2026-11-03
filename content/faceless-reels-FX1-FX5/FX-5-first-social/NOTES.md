# FX-5 "Your first bachata social, minute by minute." (DRAFT, silent)

Status: draft for owner review. Not posted, uploaded or published anywhere.

## What's in this folder
- `reel_draft_silent.mp4`: 1080x1920, 30 fps, 33.00 s (990 frames), H.264 High / yuv420p, CRF 20, +faststart, no audio track, about 3.1 MB (3,113,737 bytes).
- `cover.jpg`: 1080x1920, frame at t = 1.95 s (full hook headline "YOUR FIRST SOCIAL, MINUTE BY MINUTE", spinning clock, NERVES 99%).
- `frames/`: check stills at 0.0, 0.5, 1.2, 2.2, 3.0 and 15.0 s, plus 18.4, 18.8, 24.8 and 29.5 s.
- `caption.txt`: caption (line 1 from the spec plus a short body), 5 hashtags, pinned comment, DM reply for FIRST.
- `AUDIO-CUES.md`: VO lines with exact start/end and per-word onsets, the SFX list with timestamps, music mood/BPM (126) and drop-outs (2.20–2.55 s, 18.00–18.45 s). Generated from the renderer's own timeline, so the captions are locked to it.
- `build/`: `index.html` + `reel.js` (canvas, `draw(t)` is a pure function of time), `render.js` (Playwright steps t at 30 fps, pipes JPEG frames into ffmpeg; `node render.js stills` / `node render.js video`), `timeline.json`, fonts (Anton, Inter 600/800, self-hosted woff2 copied from the FX-1 build so the series matches).

## Scenes as built
| Time | Visual | Headline |
|---|---|---|
| 0.0–2.2 | Big alarm clock (bells ringing, hands spinning with motion trails, clock wobbling), tall NERVES meter shaking at 99%, and a dance floor at the clock's feet with four tiny ink couples doing a bachata basic at 126 BPM, coral music notes floating up | builds word by word 1.20–1.60: YOUR FIRST SOCIAL, / MINUTE BY MINUTE |
| 2.2–3.0 | Clock snaps to 9:00 with a shake + coral DING burst; clock zooms away, door pops in and swings open on a floor of grey couples doing a basic | 9:00 / YOU ARRIVE |
| 3–9 | YOU (coral tag) by the wall with water; sweat drop 4.6; couples with "1 2 3 4" count bubbles from 5.7; sip at 7.1; NERVES 90% | 9:05 / YOU WATCH |
| 9–15 | Dancer walks in, offers an open hand, "DANCE?" 11.1; "YES!" + nod 12.6; NERVES 70% | 9:15 / SOMEONE ASKS YOU |
| 15–21 | Basic, a turn at 17.0, stumble + "OOPS" 18.0, both laugh "HA HA" 18.6, "NOBODY CARES." stamp, "PEOPLE WHO NOTICED: 0" 19.5; NERVES 50 then 30% | 9:18 / YOU MESS UP. NOBODY CARES. |
| 21–27 | YOU walks over to a newcomer (Warm Grey) by the wall, "DANCE?" 23.0, coral heart 24.4, they dance; NERVES 0% (coral) | 10:30 / YOU'RE ASKING OTHERS |
| 27–33 | Coral end card drops in: SEND THIS TO YOUR "ONE DAY" FRIEND. · dancing couple · FOUNDATION · SUN 8 PM / THU 7:30 PM · JLT · COMMENT "FIRST" pill (pulses from 28.8) | (end card) |

Word-by-word captions carry every VO line (Inter Semibold 56 px, active word coral, bottom of the safe area). "DUBAI BACHATA" wordmark top left the whole time. Whip transitions with speed lines at 3, 9, 15, 21 and 27 s. Something changes on screen at least every 2–3 s.

## Revision 2 (coordinator feedback)
- Tiny ink couples dance on a floor line around the clock from frame 0, stepping on the 126 BPM basic, so frame 0 reads as a dance social.
- Clock enlarged (r 385 → 400, repositioned) and NERVES meter lengthened (550 → 750 px). Measured on the rendered frame 0, the clock + meter group's bounding box is x 43–1020, y 598–1480, which is **41.6% of the frame area**. The clock alone is 32%.
- Hook headline moved down. Top of the caps is now about y 316, clearly below the 285 px line. The later time headlines are about 20 px lower too.
- Partner in the 10:30 dance is Warm Grey #A69F94, so YOU (ink, coral tag) stands out.
- Captions moved slightly lower (Inter Semibold 54 px, baselines 1548/1616, all inside y 1635) to make room for the taller hook.
- Fixed the OOPS star overlapping the HA HA bubble at 18.6 s.
- VO, SFX and music timings are unchanged. AUDIO-CUES.md was re-checked against the regenerated timeline.json, and every VO start/end, word onset and SFX time matches.

## 8-point first-3-seconds checklist (honest, after revision 2)
1. Frame 0 already moving: PASS. Hands spin with trails, bells ring, the meter shakes and the couples step, all from frame 0. No fade or black frame.
2. Frame 0 instantly recognisable: PASS, with a caveat. Alarm clock + NERVES 99% + a dance floor of couples reads as "nervous about a dance night". The couples are small (about 110 px tall each, four of them). They read clearly at full size, but on a phone they are background detail rather than the hero, and the word "bachata" first shows at 0.69 s in the caption.
3. Biggest element owns at least 40% of the frame and moves from frame 1: PASS by the brief's definition (clock + meter group = 41.6% of the frame by bounding box, moving from frame 1). The clock alone is 32%.
4. Something extraordinary before 3 s: PASS. The clock slams to 9:00 with a shake and a DING burst at 2.20 s, then the door swings open onto the floor at 2.5–2.9 s.
5. Claim lands at 1.2–1.6 s, word by word, big, high contrast: PASS. The Anton headline pops one word per 0.08 s from 1.20 to 1.60 s, with "FIRST" on a coral block. Caveat: the small VO captions start at 0.30 s.
6. First spoken word within 0.5 s and it is the subject: PASS on paper. "Your" is cued at 0.30 s in AUDIO-CUES.md, but the draft is silent, so this depends on the audio pass.
7. Works on mute: PASS.
8. About the viewer: PASS. "YOUR first social" and the second person throughout.

Result: **8/8 by the checklist's wording.** The soft spots are #2 (small couples), #3 (met by the group, not the clock alone) and #6 (needs the VO laid on its cue).

## Limitations / for the owner
- SILENT draft: no VO, music or SFX (no TTS or music available here). The audio pass should follow AUDIO-CUES.md. The bell at 2.20 s and the music drop-out are what make the hook land with sound.
- Figures are simple pictograms. The turn is a horizontal squash and the stumble is a lean plus a kicked leg, so it reads as cartoon. No sensual poses, no alcohol, no prices, no competitor or fusion-style names.
- The wordmark is inside the top 285 px by design (brand rule).
- The 2.2–2.6 s transition briefly shows the shrinking clock behind the door as it pops in. This is intentional motion, but it is a little busy on a frame-by-frame look.
- Venue name "Dance Case Studio" appears only in the caption body and the DM (from the spec), not on screen.
- Caption body lines 2–7 are mine, built from the scene table. Line 1, hashtags, pinned comment and DM are verbatim from the spec.
