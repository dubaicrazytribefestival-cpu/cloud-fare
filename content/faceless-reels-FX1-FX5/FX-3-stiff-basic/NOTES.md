# FX-3 "Why your bachata basic looks stiff": draft notes

DRAFT for owner review. Nothing has been posted, uploaded or published.

## What was made
- `reel_draft_silent.mp4`: 1080x1920, 30 fps, H.264 yuv420p, +faststart, 32.50 s (975 frames), about 2.6 MB (2,633,200 bytes), no audio track.
- `cover.jpg`: 1080x1920, hook headline "WHY YOUR BASIC LOOKS STIFF" + LOCKED KNEES sticker + CLANK on the robot figure (no caption bar).
- `frames/`: check stills at 0.0, 0.5, 1.3, 2.0, 3.0 and 15.0 s.
- `caption.txt`: caption (line 1 from spec + body), 5 hashtags, pinned comment, DM reply.
- `AUDIO-CUES.md`: VO lines with exact start/end (matching the burned-in captions), SFX timestamps, music mood/BPM (125) and drop-outs.
- `build/`: `index.html` + `reel.js` (canvas, everything drawn from time t), `timeline.js` (single source of caption/VO/SFX timing), `render.js` (Playwright frame stepper), `sheet.py` (contact sheet), local Anton/Inter fonts copied from the FX-1 build so the series matches.
  Rebuild: `cd build && node render.js all ./seq && ffmpeg -framerate 30 -i seq/f%05d.png -c:v libx264 -crf 20 -pix_fmt yuv420p -movflags +faststart ../reel_draft_silent.mp4`

## Scene plan as rendered
| Time | What happens |
|---|---|
| 0.0-3.0 | Social dance floor in the background from frame 0 (perspective floor, 3 small ink couples stepping the basic on the 125 BPM beat, small disco ball with coral sparkles). Robot figure (scaled up, thicker limbs) (locked straight legs, robot arms, hip shoved sideways each step) doing the basic (side, together, side, tap) in front of a big metronome swinging hard. Headline builds word by word from 1.3 s. X-ray sweep 1.82-2.22 s, knees glow coral + "CLANK!" burst + shake + freeze at 2.0 s, LOCKED KNEES sticker at 2.08 s. |
| 3.0-10.0 | Whip. Side by side: left PUSHING THE HIP + cross icon (straight legs, push arrow, grey "WEIGHT STUCK" blob between the feet); right SHIFTING THE WEIGHT + tick icon (soft knees, coral weight blob moving under the standing foot, coral arrows showing the shift, pelvis tilts so the hip follows). |
| 10.0-21.0 | Drill: SOFT KNEES / FULL WEIGHT / 1-2-3-TAP build in; knee rings; big count number + 8-count strip (1 2 3 TAP / 5 6 7 TAP); SLOW (half speed) then FULL SPEED from 17.84 s. |
| 21.0-27.0 | ROBOT MODE: ON, padlocks appear on the knees, spring open at 22.6 s, figure blends from robot to smooth, coral confetti, SAME BASIC. NO ROBOT. |
| 27.0-32.5 | End card: FIX IT IN ONE CLASS. / FOUNDATION with Saj & Emi / Sun 8 PM / Thu 7:30 PM · JLT / coral COMMENT "BASIC" panel, small figure still dancing. |

The basic is side, together, side, tap. Every figure in the reel (robot, smooth figure, drill, unlock scene, end card and the background couples) uses the same step function, modelled as: 1 R steps right, 2 L closes, 3 R steps right, 4 L taps; 5 L steps left, 6 R closes, 7 L steps left, 8 R taps. Checked numerically: after counts 1, 3, 5 and 7 the feet are a step apart; after 2 and 6 they are back together at stance width; on 4 and 8 the free foot taps beside the standing foot with no weight change. Smooth version: weight goes fully over the stepping foot, knees bent, pelvis tilts (standing side higher). Stiff version: legs straight, weight stays between the feet, the hip is pushed out on each step.

## 8-point first-3-seconds checklist (virality skill), honest result
1. Frame 0 already moving: PASS (figure mid-step and pendulum mid-swing; frame 0 and frame 1 differ).
2. Recognisable on frame 0: PASS. Frame 0 shows a social dance floor (couples dancing the basic, disco ball) with the robot dancer in front, the same setting as the other reels in the series. The word "bachata" itself appears only in the wordmark until the caption at 0.3 s.
3. Biggest element owns at least 40% of the frame and moves from frame 1: PASS (by span; area still the weakest point). After the fix, the robot figure is about 15% taller and its limbs about 55% thicker than in v1, and the metronome is 25% bigger. Together they span about 1,040 px of height (about 54% of the frame, nearly 80% of the safe area) and about 830 px of width (about 77%), and they move from frame 1. The solid ink and grey shapes still fill well under 40% of the pixels.
4. Something extraordinary before 3 s: PASS (X-ray sweep, knees light up, CLANK burst, screen shake and freeze at 2.0 s, sticker slam at 2.08 s).
5. Claim lands about 1.2-1.6 s, word by word, big, high contrast: PASS (WHY YOUR BASIC LOOKS STIFF builds 1.30-1.90 s, Anton 100 px, ink on cream with STIFF in coral).
6. First spoken word within 0.5 s and it is the subject: PASS on paper (caption "Your" at 0.30 s; AUDIO-CUES.md locks the VO there). The draft itself is silent, so this depends on the VO being laid exactly as cued.
7. Works on mute: PASS (every VO line is a burned-in word-by-word caption with the active word in coral).
8. About the viewer: PASS ("Your basic looks stiff").
Result: 8/8 (v2). Honest caveat: point 3 passes by span, not by pixel area.

## v2 changes (coordinator request)
- Added the background dance floor to scenes 0-3 s: a back floor line with perspective lines, 3 small ink couples (semi-transparent so they stay background) stepping the basic on the 125 BPM grid, and a disco ball with rotating facets and coral sparkles. The couples keep dancing through the 2.0-2.5 s freeze.
- Robot figure scale 1.5 -> 1.72 (about +15% height), limb thickness x1.35 (about +55% stroke width), metronome x1.25 (+25%). Height was capped at about +15% because a 25% taller figure would have hidden its head behind the headline; the extra weight went into thickness and the metronome instead. The headline is now 90 px with a cream outline so it stays readable where it crosses the top of the head.
- No timing changes: all captions, VO and SFX times in AUDIO-CUES.md are unchanged and still match.

## Limitations / owner to-do
- Silent draft: no VO, music or SFX yet (see AUDIO-CUES.md). Not uploaded to Drive (instruction was draft only).
- Figures are simple 2D front-view pictograms. Soft knees are shown as a bent-knee zigzag plus a lower hip; in some poses the free leg looks a little like a kick sideways. Bachata hip action is simplified to a pelvis tilt over the standing leg. Saj/Emi should glance at scene 3 and the drill for accuracy.
- The 3.0 s check still is mid whip-transition (coral streaks, incoming scene sliding in); that is intentional.
- Wordmark sits at y=300 (just inside the safe area) rather than in the very top corner, to keep all text out of the top 285 px.
- Owner to-do: add DM keyword "BASIC" to the Instagram automations; confirm "FOUNDATION with Saj & Emi" wording on the end card.
- No prices, no competitor names, nothing from Bacha Fusion or BachaZouk, no sensual poses.
