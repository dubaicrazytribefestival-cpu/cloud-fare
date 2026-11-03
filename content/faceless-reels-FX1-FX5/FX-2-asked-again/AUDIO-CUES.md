# FX-2 "Same social. Same song. Only one gets asked again." Audio cues

Picture is locked: 1080x1920, 30 fps, exactly 30.00 s (900 frames). The draft is silent. Lay the audio on top of `reel_draft_silent.mp4` and don't retime the picture. Every time below comes from the renderer's timing table (`build/reel.js`, `VO` array and scene code), so the captions on screen match these VO windows to the frame.

## Voice-over (warm, friendly, a little cheeky, brisk)
Each line should start at its **start** time and finish by its **end** time. Captions reveal word by word across that window, with the time split by word length, so an even delivery lines up best.

| # | Start (s) | End (s) | Line | Note |
|---|---|---|---|---|
| 1 | 0.30 | 1.40 | "You and him: same social, same song…" | First word "You" at 0.30 s. The on-screen "YOU?" tag points at both dancers 0–2 s |
| 2 | 1.55 | 2.90 | "…only one gets asked again." | Land "again" around 2.6 s, just after the counter slam at 2.25 |
| 3 | 3.30 | 5.40 | "Dancer A did six combos." | |
| 4 | 5.70 | 8.60 | "His partner was just trying to survive." | |
| 5 | 9.30 | 11.00 | "Dancer B did one turn." | The turn happens on screen 10.4–11.4 |
| 6 | 11.50 | 13.00 | "And she had fun." | |
| 7 | 15.30 | 16.30 | "Eyes up." | Card 1 |
| 8 | 18.30 | 19.60 | "Match their level." | Card 2 |
| 9 | 21.30 | 23.30 | "Leave space for them to play." | Card 3 |
| 10 | 26.70 | 29.30 | "Comment AGAIN and we'll send you the three tips." | End card. Stress "AGAIN" |

There is no VO from 24.0 to 26.7 s (the "NEXT SOCIAL: A COPIES B." beat). Let music and SFX carry it.

## Music
- Mood: upbeat, light, playful instrumental bachata (royalty-free), with guitar (requinto) lead and bongo/güira groove. Nothing sultry.
- Tempo: **128 BPM** (one beat = 0.47 s). The figures' basic step is animated at 0.47 s per count, so 126–130 BPM will sit right. Put the downbeat at 0.00 s.
- Level: duck to about -18 dB under VO and bring it up between lines.

| Time (s) | Music event |
|---|---|
| 0.00 | Music already playing at full level on frame 0 (no fade in) |
| **1.75** | **Drop-out 1:** the song ends. Hard stop or record scratch at 1.75, when the dancers freeze and step apart |
| 1.75–3.00 | Silence apart from SFX (wind for the tumbleweed) |
| 3.00 | Music back in under a rewind SFX ("REPLAY"). Optional: slightly busier or more frantic for Dancer A |
| 9.00 | Rewind SFX again. Normal relaxed groove for Dancer B |
| **12.40–13.30** | **Drop-out 2:** music pause. Dancer B and partner freeze on screen with a "PAUSE ON THE MUSIC" icon. Cut the music at 12.40 and bring it back on the beat at 13.30 |
| 13.30–29.70 | Music continues |
| 29.70–30.00 | **Loop cross-match:** the picture crossfades from the end card back into the exact opening layout (frame 0), so the replay loops seamlessly. End the music so it flows back into the 0.00 s downbeat: either a short stab at 29.70 that releases into the loop, or cut on the bar so the track restarts cleanly. Avoid a long tail |

## SFX
| Time (s) | SFX | On screen |
|---|---|---|
| 0.00–1.70 | Light party ambience or crowd murmur (optional, low) | Social dance floor, disco ball, notes rising |
| 0.00–2.00 | (Optional) soft "boing" wobble loop, very low | "YOU?" tag pulsing with arrows to both dancers; fades out 1.78–2.00 |
| 1.75 | Record scratch / needle stop | Song ends, couples separate |
| 1.70, 1.80, 1.90 | Three quick whooshes | "Dance?" bubbles fly in |
| 2.05, 2.15, 2.25 | Pop + tick (1, 2, 3) | B's counter ticks 1, 2, 3 |
| 2.25 | Big slam / impact + ding | Counter slams to 3 with burst and shake |
| 2.15–3.30 | Desert wind whistle | Tumbleweed rolls across A's side |
| 2.45 | Cricket chirp or a sad "boop" | "…" above Dancer A |
| 3.00 | Whip whoosh + tape rewind | Cut to "◀◀ REPLAY: DANCER A" |
| 3.00, 4.00, 5.00, 6.00, 7.00, 8.00 | Counter tick (rising pitch) | COMBO 1/6 → 6/6 |
| 3.10, 4.10, 5.10, 6.10, 7.10, 8.10 | Fast spin whoosh (about 0.6 s each) | Partner spins |
| 4.55, 6.55, 8.05 | Comedic "boing" / jolt zap | Coral jolt line + "YANK!" |
| 5.70–8.60 | Small dizzy "wobble" (optional, low) | Spiral over partner's head |
| 9.00 | Whip whoosh + tape rewind | Cut to "REPLAY: DANCER B" |
| 10.40–11.40 | One smooth, soft whoosh | B's one turn |
| 10.60 onwards | Light sparkle chimes + a short giggle (optional) | Sparkles, "ha ha!" |
| 12.40 | Soft click / pause button | Pause icon pops |
| 15.00, 18.00, 21.00 | Whip whoosh + pop | Tip cards 1, 2, 3 slide in |
| 15.75 | Buzzer "nope" (short) | Coral X over looking at feet |
| 16.20 | Bright chime | Coral eye-contact line connects |
| 19.00–19.60 | Three descending blips | YOU level meter drops 5 → 2 |
| 19.60 | Ding | Coral check (levels match) |
| 21.80 | Soft "swish" + guitar strum | SPACE bracket appears, partner styles |
| 24.00 | Whip whoosh | Split screen: "NEXT SOCIAL: A COPIES B." |
| 24.95 | Whoosh | "Dance?" bubble flies to A |
| 25.35 | Pop + celebratory ding | A's counter ticks 0 → 1 |
| 26.40 | Whip whoosh | End card |
| 27.25 | Pop / stamp | Coral "COMMENT “AGAIN”" panel |
| 29.70–30.00 | Music button / loop point | Crossfade to the opening layout |
