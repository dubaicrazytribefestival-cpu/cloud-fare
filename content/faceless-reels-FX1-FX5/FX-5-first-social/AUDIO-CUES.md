# FX-5 audio cues (for the downstream VO / music / SFX pass)

Draft video: `reel_draft_silent.mp4`, 33.00 s, 30 fps, 990 frames, no audio track. All timings below are generated from the same timeline the renderer uses (`build/reel.js` → `build/timeline.json`), so the on-screen captions are locked to them. Lay audio on top; do not re-time the picture.

## Voice-over lines (start/end = first word appears / last word finishes on screen)

| ID | Start (s) | End (s) | Line | Per-word caption onsets (s) |
|---|---|---|---|---|
| VO1 | 0.30 | 1.95 | Your first bachata social, minute by minute. | Your 0.30 · first 0.48 · bachata 0.69 · social, 0.95 · minute 1.27 · by 1.51 · minute. 1.63 |
| VO2 | 2.25 | 3.20 | Nine o'clock. You walk in. | Nine 2.25 · o'clock. 2.41 · You 2.71 · walk 2.85 · in. 3.01 |
| VO3 | 3.40 | 7.90 | Nine-oh-five. You watch. Everyone is counting their own steps. | Nine-oh-five. 3.40 · You 4.27 · watch. 4.57 · Everyone 5.16 · is 5.75 · counting 6.00 · their 6.59 · own 7.01 · steps. 7.31 |
| VO4 | 9.40 | 13.20 | Nine-fifteen. Someone asks you. You say yes. | Nine-fifteen. 9.40 · Someone 10.44 · asks 11.03 · you. 11.44 · You 11.98 · say 12.32 · yes. 12.67 |
| VO5 | 15.40 | 19.80 | Nine-eighteen. You miss a step. You both laugh. | Nine-eighteen. 15.40 · You 16.58 · miss 16.96 · a 17.40 · step. 17.63 · You 18.28 · both 18.65 · laugh. 19.09 |
| VO6 | 21.40 | 24.40 | Ten-thirty. Now you're the one asking. | Ten-thirty. 21.40 · Now 22.27 · you're 22.60 · the 23.05 · one 23.38 · asking. 23.71 |
| VO7 | 27.40 | 31.60 | Comment FIRST and we'll send you the first-social checklist. | Comment 27.40 · FIRST 27.94 · and 28.36 · we'll 28.67 · send 29.03 · you 29.40 · the 29.71 · first-social 30.02 · checklist. 30.78 |

Notes for VO: warm, friendly, a little cheeky, brisk. First spoken word ("Your") must start at 0.30 s. Each caption word turns coral at its onset, so a VO read that matches these onsets within ±0.1 s will look synced. "Nine o'clock" = the clock's 9:00 stop; say the times as written ("nine-oh-five", "nine-fifteen", "nine-eighteen", "ten-thirty"). If a line runs long, trim pauses, not words.

## SFX

| Time (s) | Cue |
|---|---|
| 0.00 | Fast clock ticking / ratchet whirr under the spinning hands (0.00-2.20) |
| 0.00 | Nervous wobble/rattle on the NERVES meter (0.00-2.20, low in mix) |
| 1.20 | Soft pop per headline word (6 pops, 1.20-1.60) |
| 2.20 | Alarm-clock bell DING, clock stops on 9:00 (hard stop of ticking) |
| 2.50 | Door creak + swing whoosh, room noise/chatter swells in |
| 3.00 | Whip whoosh (scene change to 9:05) |
| 4.60 | Tiny "bloop" (sweat drop) |
| 5.70 | Light ticks on the beat as "1 2 3 4" bubbles count (5.7-9.0) |
| 7.10 | Water sip / gulp |
| 9.00 | Whip whoosh (scene change to 9:15) |
| 11.10 | Friendly "boop" as the open hand + DANCE? bubble pops |
| 12.62 | Bright pop/chime for YES! bubble |
| 15.00 | Whip whoosh (scene change to 9:18) |
| 17.00 | Swish (turn) |
| 18.00 | Cartoon stumble "boing" (lands in the music drop-out) |
| 18.60 | Two short giggle pops (HA HA bubbles) |
| 19.50 | Counter tick ("people who noticed: 0") |
| 21.00 | Whip whoosh (scene change to 10:30) |
| 23.00 | Friendly "boop" (YOU offers the open hand) |
| 24.40 | Heart pop / sparkle |
| 27.00 | Whip whoosh + soft thud as the coral end card drops in |
| 28.80 | Button pop on COMMENT "FIRST" pill |

## Music

- Mood: upbeat, playful, warm instrumental bachata (guitar requinto + bongo/güira), royalty-free, nothing sensual or slow. Tempo **126 BPM** (the on-screen dancers' basic steps and the "1 2 3 4" count bubbles are animated at 126 BPM, one count = 0.476 s).
- The four tiny ink couples on the hook's dance floor (0.00–2.60 s) also step at 126 BPM, so the music needs to be at that tempo and on the grid from 0.00 s.
- Starts at 0.00 s already playing (no fade-in), ducked to about -18 dB under VO.
- Drop-outs (hard cuts, silence apart from SFX):
  - **2.20–2.55 s**: Full cut on the bell DING; music re-enters (door opens) at 2.55
  - **18.00–18.45 s**: Short stop on the stumble; back in for the laugh at 18.45
- 22.40 s: optional small lift/fill when NERVES hits 0%.
- 27.00–33.00 s: end card; keep music up under VO7, short button/ending on 32.5–33.0 s.
