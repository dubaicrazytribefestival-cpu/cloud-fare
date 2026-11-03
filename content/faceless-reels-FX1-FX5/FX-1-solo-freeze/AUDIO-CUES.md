# FX-1 "200 moves. Zero solo." Audio cues

These cues are for `reel_draft_silent.mp4` (33.50 s, 30 fps, 1005 frames). The picture is locked. Every time below comes from the render code (`build/reel.js`, the `VO` and `CAP` tables), so the audio can go on top without re-editing the video. Frame number = seconds × 30.

## 1. Voice-over (start/end = when the caption shows the first and last word)

The caption reveals each word at the time listed. Read the VO so that each word lands on or just before its caption word. A VO line can run up to about 0.3 s past its "end" time before the caption box disappears.

| # | Start | End (last word) | Caption box off | Line |
|---|---|---|---|---|
| 1a | 0.30 | 2.10 | (headline) | "You know two hundred moves with a partner…" Big on-screen headline: YOU: 1.22 · 200 1.32 · MOVES 1.42 · WITH 1.52 · A 1.62 · PARTNER. 1.72 |
| 1b | 2.30 | 2.95 | 3.50 | "…zero when it's solo." Headline: ZERO 2.30 · WHEN 2.47 · IT'S 2.60 · SOLO. 2.73 |
| 2 | 4.60 | 4.90 | 5.95 | "Sound familiar?" |
| 3 | 6.75 | 7.92 | 9.05 | "You think everyone's watching." |
| 4 | 9.25 | 13.32 | 14.20 | "Reality? They're counting their own steps. Research says people notice us about half as much as we think." |
| 5 | 14.20 | 19.22 | 20.20 | "With a partner, the lead gives you cues. Alone, nobody does, and twenty combos means twenty choices. So your brain buffers." |
| 6 | 20.30 | 21.61 | 22.60 | "The fix: basic first. Always." |
| 7 | 22.60 | 24.37 | 25.15 | "Then add one thing. Shoulders, arms, or a pause." |
| 8 | 25.15 | 27.90 | 28.65 | "And listen for one instrument. Move to that, not to what your hips are doing." |
| 9 | 28.65 | 29.57 | 30.55 | "Same guy. Three tools." |
| 10 | 30.80 | 32.21 | 33.05 | "Learn it with us in JLT. Comment SOLO." |

Note on 1a: the brief has the first spoken word ("You") at 0.30 s. On screen, the claim starts landing at 1.22 s, as the brief's hook timing asks. The counter label "MOVES YOU KNOW" is on screen from frame 0. The VO runs ahead of the headline here, and that is intended.

Word-level times (the caption word turns coral at these times):

```
4.60 Sound  4.90 familiar?
6.75 You  7.00 think  7.35 everyone's  7.92 watching.
9.25 Reality?  9.59 They're  9.90 counting  10.25 their  10.49 own  10.67 steps.
10.95 Research  11.29 says  11.51 people  11.78 notice  12.06 us  12.21 about
12.46 half  12.67 as  12.82 much  13.03 as  13.17 we  13.32 think.
14.20 With  14.44 a  14.57 partner,  14.95 the  15.15 lead  15.39 gives  15.66 you  15.87 cues.
16.14 Alone,  16.45 nobody  16.76 does,  17.04 and  17.24 20  17.40 combos  17.71 means  17.99 20  18.15 choices.
18.54 So  18.70 your  18.94 brain  19.22 buffers.
20.30 The  20.56 fix:  20.86 basic  21.21 first.  21.61 Always.
22.60 Then  22.81 add  22.99 one  23.17 thing.  23.45 Shoulders,  23.86 arms,  24.11 or  24.26 a  24.37 pause.
25.15 And  25.31 listen  25.57 for  25.73 one  25.90 instrument.  26.30 Move  26.49 to  26.63 that,
26.85 not  27.02 to  27.15 what  27.34 your  27.54 hips  27.73 are  27.90 doing.
28.65 Same  28.94 guy.  29.23 Three  29.57 tools.
30.80 Learn  31.04 it  31.19 with  31.40 us  31.54 in  31.69 JLT.  31.90 Comment  32.21 SOLO.
```

Lines 4 and 5 are brisk (about 4.5 words per second). If the VO can't fit, slow the delivery a little but keep the first word of each line on its time.

## 2. Music

- Mood: upbeat, warm instrumental bachata loop, royalty-free (guitar-led, with requinto, bongo and güira). It should feel playful, not sultry.
- Tempo: **120 BPM**. The on-screen dance is locked to a beat grid at **0.20 + 0.50 × n s**, so beats fall at 0.20, 0.70, 1.20 and so on. COMBO GUY's basic step starts on a count-1 at **21.20 s**. The step is side, together, side, tap (1-2-3-tap, then 5-6-7-tap back), with the taps on beats 4 and 8. The on-screen labels SIDE · TOGETHER · SIDE · TAP light up on those counts from 21.20 to 22.50. (Revision 2 changed only the step pattern; every time in this file is the same as before.) Put the loop's downbeat on 21.20 s and the earlier parts will line up as well (21.20 = 0.20 + 42 beats).
- Level: duck to about −18 dB under the VO, as the brief asks.

| Time | Music |
|---|---|
| 0.00–2.20 | Full, energetic (the social night) |
| **2.20** | **Hard stop on the record scratch** |
| 2.20–6.50 | **Music out.** SFX only: crack, error dings, buffering loop |
| 6.50–9.00 | Optional low tension pad or the sting only, no groove |
| **9.00** | Groove back in on the "boop" (REALITY) |
| **24.20–24.70** | **One-beat drop-out**: the "pause" freeze-frame. Music returns on the beat at 24.70 |
| 25.20 | A guitar figure should be audible here (the guitar scene). Keep the requinto forward from 25.0 to 28.5 |
| **29.70–30.20** | **One-beat drop-out** (his pause in the "Same guy" scene), back on the beat at 30.20 |
| 30.50–33.50 | End card. "Button" ending (a final hit) at **33.20**. The last frame cuts back into frame 0 for the loop |

## 3. SFX

| Time (s) | SFX | What's on screen |
|---|---|---|
| 0.00, 0.65, 1.29, 1.94 | Fast whooshes (one per spin) | Couple spinning |
| 0.00–1.90 | Counter ticks: rapid, slowing as the count approaches 200 | Counter races to 200 |
| 1.90 | Small "lock" click | Counter locks on 200 |
| 2.20 | **Record scratch** + whoosh | Partner yanked off screen to the right |
| 2.20–2.42 | Fast descending tick run | Counter falls from 200 to 0 |
| 2.42 | **Glass crack** + thud (screen shake) | 0 cracks, shards fly |
| 3.50–6.50 | Buffering loop (soft, looping) | Loading wheel over his head |
| 3.75, 4.35, 4.95 | Error "ding" ×3 | brain.exe boxes cascade |
| 5.10–6.20 | Optional mouse-move / click at 6.20 | Cursor heads for WAIT… |
| 6.50 | Whip whoosh | Transition |
| 6.62 | **Dramatic sting** | WHAT YOU THINK |
| 6.9–7.5 | Little pops ×7 (staggered by 0.1 s) | "!!" marks pop over the circle |
| 9.00 | **Comedic "boop"** + flash | REALITY |
| 9.25 | Deflate / shrink | Spotlight shrinks to half |
| 14.00 | Whip whoosh | Split screen |
| 14.2–20.0 | Soft cue "blips", about 4 per second, quiet | Coral cue arrows flow into his hands |
| 16.60–17.40 | **Messy overlapping chimes** (20 hits) | 20 move bubbles pop in and flash |
| 18.30–20.10 | Buffering loop again | Loading wheel |
| 20.45–21.25 | **Pop, pop, pop** (19 pops, about every 0.04 s; can be thinned) | Bubbles pop until 1 is left |
| 21.35 | Soft ding | Coral "1" settles |
| 22.70–24.20 | Optional soft swish per shoulder roll | Shoulder rolls |
| 24.20 | **Soft click** (pause) | Freeze-frame, coral ⏸ icon |
| 25.00 | Whip whoosh, then **guitar strum** at 25.20 | Guitar glows coral |
| 25.70 | Small "nope" buzz (optional) | Arrow at the hips gets crossed out |
| 28.50 | Whip whoosh, **crowd cheer** 28.6–30.5 | The circle cheers, confetti |
| 29.70 | Soft click (pause) | His pause |
| 30.50 | Whip whoosh | End card |
| 31.75 | Pop / stamp | COMMENT "SOLO" panel lands |
| 33.20 | Music button ending | — |
