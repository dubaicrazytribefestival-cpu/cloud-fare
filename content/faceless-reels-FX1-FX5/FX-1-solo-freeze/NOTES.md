# FX-1 "200 moves. Zero solo." Draft notes (revision 2)

**Status: DRAFT for owner review. Nothing has been posted or uploaded anywhere (no Drive, no Instagram).**

## Files
| File | What |
|---|---|
| `reel_draft_silent.mp4` | 1080×1920, 30 fps, H.264 yuv420p, crf 20, +faststart. **33.50 s, 1005 frames, 4.67 MB (4,673,595 bytes).** No audio track |
| `cover.jpg` | 1080×1920. The hook at 2.17 s: coral 200 counter, the spinning couple on the social floor, "YOU: 200 MOVES WITH A PARTNER." |
| `frames/still_{0.0,0.5,1.3,2.2,3.0,15}s.jpg` | Check stills taken from the encoded MP4 |
| `caption.txt` | Section 7 caption from the brief. The only change is the CTA in the last paragraph (see below) |
| `AUDIO-CUES.md` | Locked VO start and end times (word level), music BPM and beat grid, drop-outs, SFX timestamps |
| `build/` | `index.html` + `reel.js` (canvas animation, `render(t)`), `render.js` (Playwright → ffmpeg), `stills.js`, `measure.js` (measures the hook's area), local Anton/Inter fonts. Re-render with `node build/render.js` |

## Revision 2 changes (from coordinator feedback)
1. **Basic step: side, together, side, tap.** The lead leg opens on "side" and closes on "together", with a tap on 4 and 8, then the same back the other way. The labels now read SIDE · TOGETHER · SIDE · TAP, with the current count in coral (21.2–22.5 s). The step stays on the 120 BPM grid from 21.20 s. Timing is unchanged, so AUDIO-CUES.md still holds.
2. **Caption CTA is consistent.** In the last paragraph, `DM "SOLO" and we'll send you the details.` became `Comment SOLO and we'll send you the 3-step solo drill.` The class times line is kept. The caption now has no "DM" anywhere, and matches the end card (COMMENT "SOLO") and the caption's first line.
3. **Bigger hook group, label never clips a head.**
   - The couple is taller (610→625 px) and the spin is wider (radius 150→200 px).
   - The counter is a little smaller (270→230 px) and its lock-in bounce is smaller, so it no longer brushes the wordmark.
   - "MOVES YOU KNOW" moved up to y≈600. The highest a head can reach is y≈634, so the label clears every head.
   - The claim moved down slightly (baselines 1522/1634) so the feet no longer touch it.
4. **No hair bun.** PARTNER is now Warm Grey #A69F94 (COMBO GUY stays Ink) in the hook and on the split screen. The background couples are all grey with no bun.
5. **check/ folder deleted.**

## Scene timeline (same as revision 1)
| Time | Scene |
|---|---|
| 0–2.2 | Social night: DJ booth, disco ball and beams, grey couples. COMBO GUY (ink) + PARTNER (grey) spin. The counter races up from 0 (62 on frame 0) and locks at 200 at 1.9. The claim lands word by word from 1.22 to 1.72 |
| 2.2–3.5 | Partner yanked off right. The counter crashes 200→0 and cracks with a shake at 2.42; T-rex freeze. "ZERO WHEN IT'S SOLO." (2.30–2.73) |
| 3.5–6.5 | Shuffle, loading wheel, three cascading "brain.exe has stopped working" boxes (generic, no OS branding). "Sound familiar?" |
| 6.5–9.0 | WHAT YOU THINK: the circle stares, with sightlines, "!!" and a giant coral spotlight |
| 9.0–14.0 | REALITY: the circle looks down counting, the spotlight shrinks to half, plus the small Cornell 2000 citation |
| 14.0–20.0 | Split: THE LEAD GIVES YOU CUES (coral cue arrows) / 20 MOVES = 20 CHOICES (20 flashing bubbles, buffering) |
| 20.0–22.5 | Bubbles pop down to a coral "1", "1 · BASIC FIRST", side-together-side-tap with labels |
| 22.5–25.0 | "2 · ADD ONE THING": a shoulder roll, then a one-beat freeze-frame (coral ⏸) |
| 25.0–28.5 | "3 · DANCE THE GUITAR, NOT YOUR HIPS": a glowing guitar, notes flowing to him, the hips arrow crossed out |
| 28.5–30.5 | "SAME GUY. 3 TOOLS.": the circle cheers, confetti |
| 30.5–33.5 | End card: "SOLO IS EASIER THAN YOU THINK: YOUR BASIC + ONE THING." / Foundation with Saj & Emi · Sun 8 PM / Thu 7:30 PM · JLT · No partner. No dance background. / coral panel with ink text COMMENT "SOLO" |

QA:
- ffprobe confirms 1080×1920, 30/1 fps, 1005 frames, 33.500 s.
- A frame-difference pass over all 1005 frames found no static frame pair (minimum mean difference 0.094).
- I looked at all six check stills, the cover, 15.5 s and 21.5 s.
- There are no prices, competitors, Bacha Fusion or BachaZouk, or sensual poses.

## Virality checklist (first 3 s), honest ticks
| # | Point | Result |
|---|---|---|
| 1 | Frame 0 already moving | ✓ The counter reads 62 and is climbing, the couple is spinning, the beams sweep. No fade |
| 2 | Recognisable on frame 0 | ✓ (caveat) The DJ booth labelled "DJ", disco ball, couples on a floor. Pictograms are less instantly "my world" than real footage |
| 3 | Biggest element ≥40% and moving | **✓ on average, not on every frame.** I measured it with `build/measure.js`: render the hook without scenery, take the bounding box of the counter + label + couple (+ whoosh arcs), and sample every 0.1 s from 0 to 2.1 s. **Average 42.4%, range 36.6–48.8%; 13 of 22 samples are ≥40%.** It dips below 40% when the spin puts one figure behind the other. The solid figures themselves cover only about 12% of the frame, because pictograms are thin |
| 4 | Something extraordinary before 3 s | ✓ Yank at 2.20, crash and crack at 2.42 |
| 5 | Claim lands about 1.2–1.6 s, word by word | ✓ 1.22 → 1.72, big Anton, high contrast |
| 6 | First spoken word within 0.5 s, about the viewer | **Pending audio.** The draft is silent. AUDIO-CUES.md puts "You…" at 0.30 s. "MOVES YOU KNOW" is on screen from frame 0 |
| 7 | Works on mute | ✓ All VO is captioned word by word |
| 8 | About the viewer | ✓ "YOU: 200 MOVES WITH A PARTNER." |

**Result: 6/8 clear passes, #3 passes on average (42%) but not on every frame, #6 pending the audio pass.**

## Remaining weaknesses and things not done
- **Silent only**, with no audio track. There is no TTS or music library here. The brief's AAC/music versions need the downstream audio pass (AUDIO-CUES.md).
- **Not saved to Drive and not sent for approval**, by instruction.
- PARTNER in Warm Grey goes against the brief's "solid ink bodies" for both characters (a deliberate change). It also makes the partner a little closer in tone to the grey background couples, though size and position keep it clear.
- VO in scenes 5 and 6 is dense (about 4.5 words per second). The captions are readable but brisk.
- The 20 move-bubble labels are tiny and overlap on purpose ("messy"). They are decoration and not readable on a phone.
- Confetti and disco beams go into the top and bottom 285 px. They are graphics, not text.
- Owner to-do (brief §8): add the DM keyword "SOLO" to the Instagram automations, with the 3-step drill + Foundation times. Pinned comment and alt text are in brief §7, not in caption.txt.
