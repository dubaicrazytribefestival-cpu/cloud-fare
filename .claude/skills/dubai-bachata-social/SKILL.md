---
name: dubai-bachata-social
description: Run the Dubai Bachata / Latin Crazy Tribe social media engine, AI-run with minimal human input. Use for the weekly content run ("write week N", the Monday automation), weekly approval and scheduling ("approve week N", "approve P2"), comment replies and the Reply Bank, DM and WhatsApp communication scripts, account audits, competitor benchmarks, hashtag scans and the monthly report for @dubaibachata and the LCT account network.
---

# Dubai Bachata Social Engine

One system for planning, producing, approving, scheduling, communicating and reporting for Dubai Bachata (Saj & Emi, B-YOU Method, JLT) and the Latin Crazy Tribe network.

## Operating mode: AI-run, minimal human

The AI workflow runs the system end to end. The owner has exactly two weekly touchpoints:
1. **One approval message** per week, after the Monday run ("approve week 3", or "approve week 3 except P2", or edits). That single message approves every listed post, time and collaborator for scheduling.
2. **One filming session** at the Thursday class, from the shot lists. Reels are edited AI-assisted (paid tools such as Higgsfield need a yes each time).

Everything else (research, writing, design, hooks, scheduling after approval, comment replies from the approved Reply Bank, reporting) is Claude's job. Never ask the owner for something the data or this file already answers. Nothing is published that the owner has not approved, either per week or through the Reply Bank.

## Skill chain (use these, in this order, on every piece of content)

All installed in `.claude/skills/`. Shared business context for every marketing skill: `.claude/product-marketing.md`.

| Step | Skill | Use |
|---|---|---|
| 1. Angle | `social`, `marketing-psychology` | Pick the pillar and the psychological driver |
| 2. Hook (mandatory) | `negative-hooks` | 3 hook options from the right family, one marked; soft for a community brand |
| 3. Structure | `instagram-skills/skills/ig-carousel-planner`, `ig-content-planner`, `ig-repurposer` | Carousel spine, weekly plan, repurposing |
| 4. Caption | `instagram-skills/skills/ig-caption-writer`, `ig-hashtag-strategist` | Hook in the first 125 characters, 3–5 hashtags |
| 5. Human pass (mandatory) | `humanizer`, `instagram-skills/skills/ig-humanizer`, `copywriting` | Remove AI tells; must read like Saj & Emi talking |
| 6. Conversion | `emails`, `referrals`, `community-marketing`, `churn-prevention`, `events` | Communication stage, retention, festival campaigns |

### The 8-step content pipeline (owner rule, 2 Nov: follow on every reel and carousel)

Run these 8 steps, in order, for every piece of content and for every weekly run. Save each step's output in the post's brief in Drive (00 - Plan & Briefs) so the owner can see the working.

| # | Step | What to produce | How |
|---|---|---|---|
| 1 | Viral Hook Writer | 10 hooks for the first 3 seconds, ranked 1–10 with a one-line reason each | `viral-hook-writer` + `negative-hooks` (mix at least 4 families) + `marketing-psychology`. Each hook max 10 words, readable on frame 1, works on mute |
| 2 | A/B Hook Tester | Take hooks #1 and #2 and give ONE answer: which wins and why | `ab-hook-tester`. Score both against step 7's benchmark. Then the real test: the owner posts the loser as an Instagram **Trial Reel** (shown to non-followers only) within 24 h of the main reel. Compare 3-second hold and views after 48 h, and log the winner in the brief so the hook bank learns |
| 3 | Caption & Hashtags | Caption (hook in the first 125 characters), 3–5 hashtags, and the first comment to pin | `caption-and-hashtags`, `ig-caption-writer`, `ig-hashtag-strategist` |
| 4 | Content Audit | Every @dubaibachata post from the last 90 days judged against the account's own median (reach, saves, shares) | `content-audit` + Supermetrics IGI, report `AccountMedia`. Flag winners (≥1.5× median) and losers (≤0.5×). Name the pattern behind each group |
| 5 | Content Calendar | The next 2 weeks planned (4 posts a week: day, format, hook, collab, time) | `content-calendar`, built from the audit's winning patterns |
| 6 | Content Research | Outliers from niche accounts (posts ≥2× that account's own median views or likes), with the hook and format broken down and our own version proposed | `content-research` + Supermetrics IGPD2 `BusinessDiscoveryMedia` on the benchmark list. If an account returns no posts, write "no data", never "inactive". Never name competitors in published content |
| 7 | Virality check | Every hook must pass all 8 points of the `virality` checklist (frame 0 already moving · recognisable on frame 0 · biggest element ≥40% of frame · something extraordinary before 3 s · claim lands at 1.2–1.6 s word by word · first spoken word within 0.5 s · works on mute · about the viewer). Write the hook as a 0.0 / 0.5 / 1.2 / 3.0 s timeline | `virality` (Ootto, built from 262 posts / 3.5M views) + our own benchmark: @dubaibachata posts ≥1.5× median reach. Also apply its Rule 4: a comment keyword in the caption's first line, and the DM must deliver something real |
| 8 | Humanizer (mandatory, before writing) | Every caption, script and on-screen line passes the humanizer | `humanizer` (blader/humanizer, MIT) + `ig-humanizer`. Must read like Saj & Emi talking |

The instagram-skills bundle runs in draft-only mode (its "Tier 0"). Never use its Publora publishing path or ask for a Publora key: publishing goes through Supermetrics (Workflow B).

## Sources of truth (read before producing anything)

| What | Where |
|---|---|
| Business context | `.claude/product-marketing.md` |
| Brand guide (palette, type, layout) | Drive file `1-BzhKKkz8c8uGV07ydqOAE5Aea4B8Ka8` (Dubai Bachata Brand Guide.md) |
| Hook skill | `.claude/skills/negative-hooks/SKILL.md` (Drive copy `1N4hmcsOaO4MG10YXH30pGzJHmFF3ZcNL`) |
| Communication playbook | `references/communication-playbook.md` (next to this file) |
| Competitor map and retention playbook | https://claude.ai/artifact/XA6vRJnxsM2SzpiRgmAnrq |
| Week 1 review page (format reference) | https://claude.ai/artifact/DzMBdZeTkXRKfDNf6z8sih |

Markdown files on Drive download as base64: decode with `base64 -d` into the scratchpad before reading.

## Facts you may use (never invent others)

- Teachers: Saj & Emi · Method: B-YOU · Brand family: Latin Crazy Tribe (LCT)
- Venue: Dance Case Studio, Fortune Executive Tower, Cluster T, JLT, Dubai
- Classes: SUN 8 PM Foundation · 9 PM Improvers Social | THU 7:30 Foundation · 8:30 Improvers Social · 9:30 Advanced
- Practice: MON Practice Session at D World Dance Studio, AED 30 (time to confirm)
- Levels: Foundation → Improvers Social → Intermediate Social → Advanced (BachaZouk). New Foundation group the first Sunday of every month.
- Prices: only the AED 50 trial may appear publicly. 4-class and 8-class packages and private lessons: "message us on WhatsApp", never a number.
- Bring-a-friend: friend buys a package → the student gets 1 class free.
- Never: sensual framing, competitor names, published package prices.
- Links: classes → bachataindubai.dance; parties and festival → latincrazytribe.com. WhatsApp: +971 58 642 5833 / +971 52 779 9915. Full facts in `.claude/product-marketing.md`.
- LCT nights: Thu Room 44 · Fri SoBe · Sat TT DXB. LCT Festival 2027: **26–29 March 2027** (confirmed 31 Oct 2026; never use 1–5 April). Full Pass and Premium Pass; reveals from mid-November; student showcase planned.
- DM keywords: START, CLASS, SOCIAL, PRACTICE, SUNDAY, BACHATA
- Bio link (UTM): `https://bachataindubai.dance?utm_source=instagram&utm_medium=social&utm_campaign=bio-link&utm_content=dubaibachata`

## Accounts and roles

| Role | Accounts | Job |
|---|---|---|
| Faces | @sajknightsbachata (13.5k), @emi_dancer_dubai (9.2k) | Personality and demos; highest engagement in the market |
| Brands | @dubaibachata (classes), @bachazouk.dubai, @latincrazytribe (parties), @latincrazyfestival.dubai | Convert to bookings, entries, tickets |
| Amplifiers | @dance_dubai_videos (34k), @socialdancejournal, @latinnightsdubai | Reach; add as Collab partners |
| Merge (owner's call) | @sajyemi | Point bio to @dubaibachata |

### Account separation (owner rule, 2 Nov: never mix)

Bacha Fusion and BachaZouk are **events**, not Dubai Bachata. Never open, search, propose or use their folders, footage, captions or teachers for @dubaibachata unless the owner explicitly says so in that request. This applies to the "bachafusion marketing" Drive folder (and its subfolders "Saj video", "raw instagram"), "Amaze raw", and any weekender, workshop, guest-teacher, Jack & Jill or pool-party material.

| Account | Content that belongs here |
|---|---|
| @dubaibachata | Saj & Emi's weekly classes in JLT (Foundation, Improvers, Advanced), beginner tips, student stories, class montages, Monday practice. Sources: the Dubai Bachata Drive folder (1V1YqH45zmqx-UpM6WpGCeUXR0_d-3Cah), "Dubai Bachata Explainer", and the Thursday class shoots. |
| @bachazouk.dubai / Bacha Fusion (events) | Weekenders, BachaZouk workshops, guest teachers, Jack & Jill. Only when the owner asks. |
| @latincrazytribe | Parties (Room 44, SoBe, TT DXB, Halloween, Slasher Friday, Mad House). |
| @latincrazyfestival.dubai | Latin Crazy Festival 26–29 March 2027. |

When @dubaibachata has no finished footage, say so and plan around the next class shoot. Do not fill the gap with event content.

Default Collab rule: every brand post adds one face and one amplifier as collaborators (Instagram allows up to 3 invited collaborators; each must accept in the app).

Publishing is connected for @dubaibachata only: Supermetrics team `1323081`, Instagram Insights (`IGI`) account id `17841475085186019`. Other accounts need their own IGI connection before they can be published to.

## Content rules

- Mix: 80% teaching, entertainment and people; 20% promotion. Class or ticket details go on the last slide and in the caption, never in the hook.
- Pillars, ranked by proven performance:
  1. Mindset and etiquette carousels (nerves, asking, a "no") for reach and comments
  2. Saj & Emi on camera (demos, footwork, behind the scenes) for follows
  3. Move fixes with a person ("mistake → fix", 10–15 s) for saves
  4. Student progress (B-YOU Path graduations, road to the LCT stage) for bookings
  5. Event proof and artist reveals for tickets
- Hooks (every post, no exceptions): run the `negative-hooks` skill. Pick the family that fits, keep reel hooks to 12 words or fewer, give 3 options and mark one. Community brand: soft, never shaming. The body must deliver the hook's promise.
- Every post ends with "Follow for a new move every week" plus one action (DM keyword or link in bio). Use the DM keywords that have scripts in the communication playbook.
- Captions: hook in the first 125 characters, 3–5 hashtags, then the humanizer pass. It must sound like a person, not a brand.
- Visuals: carousels 1080×1350 JPEG, reel covers 1080×1920 JPEG, rendered from HTML with Playwright. Two looks (owner, 30 Oct 2026): **mindset carousels use the dark look** (Ink #171717 background, Paper White text, key phrases in Coral #EF7768); **class, promo and reel covers use the cream editorial collage** (Cream base, Ink Anton headlines, Inter body, one Coral accent, black text on coral for CTAs).
- Cadence (owner, 31 Oct): @dubaibachata 4 original posts a week (Mon move-fix reel, Wed mindset carousel, Fri Saj & Emi demo or student story, Sun class or party moment). Each one goes out as a Collab with one face or brand account and one amplifier, so a single post reaches several audiences. Saj accepts Collab invites. @bachazouk.dubai and the festival get 1–2 a week only when there is news. Quality and human feel beat volume.
- Logo: the Latin Crazy Tribe logo goes on slides and covers (original colours, on a clean paper panel).
- Posting time: let the data decide. Use IGI `online_followers` by hour once @dubaibachata has 100+ followers; until then 7 PM Dubai.

## Mascots (owner rule, 6 Nov 2026)

Two separate characters, never mixed or called "new":
- **Main mascot**: the original bearded cartoon (drawn in code, FX-6 style) that represents Saj. Voice: Saj's cloned Higgsfield voice ("Saj-voice-1"). Default for brand and teaching reels.
- **Young mascot**: a younger bearded 2D cartoon in the black tee with the coral music-note pin (AI-generated pose set: base, talk half/open, blink, point, thumbs-up, OK, peace, wave, thinking; Higgsfield base job 6bdb6b09). Voice: Higgsfield preset "Marcus" (6f98d3dd-324f-4845-8c28-c1d1647a06cd, speech_rate 15). Used for beginner-relatable reels such as FX-7.

## Heritage and naming stance (owner rule, 6 Nov 2026: check every post)

Background: the FX-6 reel ("5 styles of bachata", 5 Nov) drew comments calling it "false information", "lying to people" and **"cultural appropriation"**. Critics are Dominican dancers and allies who see outsiders relabelling and teaching their heritage dance. Full report: Claude Doc "FX-6 Backlash Report: Bachata is Dominican".

**Our stance (one line):** "Bachata is Dominican. We start every student at the roots, and we respect the dances it inspired by calling them what they are."

1. **Origin first.** Bachata comes from the Dominican Republic (music and dance, UNESCO Intangible Cultural Heritage since Dec 2019). Say it plainly; credit it whenever history, styles or culture come up.
2. **"Bachata" means Dominican bachata.** Never use "Dominican style" as one option among many.
3. **Honest names for other dances.** Sensual, Moderna, Fusion, BachaZouk are dances that grew from or are danced to bachata music. Name them as their own dances, with their place of origin ("Sensual, a dance from Spain"), never as "styles of bachata" or "types of bachata".
4. **Roots before branches.** Foundation teaches the basic step, footwork, musicality and culture first. That is the message, and it must be true in class.

**Never write or show:**
- "the 5 styles of bachata", "styles/types/kinds of bachata", "all of them are bachata", "real vs fake bachata"
- Dominican bachata numbered or drawn as one item in a list or one branch of a tree (it is the trunk and the roots)
- Claims that rank dances, call one "better", or say a dance "evolved past" its origin
- Defining Dominican culture on Dominicans' behalf (what Dominicans "think", "dance" or "recognise") without a Dominican source
- Stereotypes, flags or Dominican imagery used as decoration with no credit or context
- #BachataStyles, #BachataSensual and similar debate hashtags on @dubaibachata (use #DominicanBachata, #BachataDubai)

**Use instead:** "Bachata, from the Dominican Republic" · "the dances that grew out of bachata" · "they all trace back to the Dominican Republic" · Dominican bachata as trunk and roots, other dances as branches.

**Events stay separate and honest:** Bacha Fusion and BachaZouk are fusion events built on bachata music. Market them as fusion, never as "bachata", and keep them off @dubaibachata (see Account separation).

**Heritage-topic check (add to the 8-step pipeline, before content-audit):** any post that touches history, origins, styles, culture or "what bachata is" must pass:
1. Does any line, label, number or visual put Dominican bachata on the same level as its offshoots? → fix.
2. Does any word call another dance a "style/type of bachata"? → rename.
3. Is the origin credited in the video AND the caption?
4. Would a Dominican dancer read it as respectful? If unsure, soften or ask the owner.
5. Flag it to the owner as "heritage topic" when sending for approval, and plan to check comments within 2 hours of posting.

**When critics comment ("not bachata", "appropriation", "misinformation"):** never argue, never delete or hide honest criticism. Reply once: thank them, agree on the shared point (bachata is Dominican), say where we start students, invite them. Saj replies from his own account in first person. Hide only harassment, spam, or replies aimed at our leads (e.g. "Don't do it" under DM-keyword comments). Draft reply: "Thank you, and agreed: bachata is Dominican 🇩🇴. That's where every one of our students starts."

## Drive pipeline

LCT-Business-Vault / 08 - Content Operations / Dubai Bachata (`1V1YqH45zmqx-UpM6WpGCeUXR0_d-3Cah`)

| Folder | ID | Holds |
|---|---|---|
| 00 - Plan & Briefs | `1XIDsHNQrrcggC3teZ7FOwIF98CFJGAs1` | Weekly briefs, reports, competitor summaries |
| 01 - To Review | `1HBl19htfDRHaFlqg0MqKtnqIYXwNFdVv` | One subfolder per week, one per post, each with a copy doc |
| 02 - Final Poster | `1FPsR2_mcnIYhvv54xy-q-Zl5a5n8K8dI` | Approved posts |
| 03 - Posted | `1KaEHASOloxpuJuHfF06Tuvfifs4sokmc` | Live posts |

Drive takes text only. Images go on a review page (Artifact) and are uploaded straight to Instagram at scheduling time.


### Media folders (owner rule, 3 Nov: save every file by format)
Inside both "01 - To Review" and "02 - Final Poster", save media into these subfolders. Never loose files.

| Format | 01 - To Review | 02 - Final Poster |
|---|---|---|
| 1. Carousels (image slides, 1080×1350) | 1ZTzrnGUvrXaWbqmhPLs6QefQT1_CPLSA | 1Pd5YccxSfFYvYQPyoL3wMa-zr6Q30jEK |
| 2. Stories (1080×1920) | 1CL6CIzNZozoAibLJyInppUXpl-pi4MQw | 1GDMrmBeyP4fl0dvP3Y18Q4JgyF1-dsc- |
| 3. Reels (9:16 video + cover) | 1Tc97-YbFm3tOLGoNK9gDdSaGfU-fYUln | 1A1nm7VDcGeVAdvXfV78brqWSPlMU6bnk |
| 4. 4:5 Carousel Videos (1080×1350 video slides) | 1enc5oW4S8qGvj2oMipSFOPoI8bxGFk4D | 1vwYkptTI44HzZRfpCTeaup-G0Shozti0 |

Two content tracks: **faceless** (animated explainers and graphic carousels, made by the reel-making agent; concept bank in 00 - Plan & Briefs, "Faceless explainer bank") and **recorded** (anything Saj & Emi film: briefs, shot lists and raw footage go in the Drive folder "Recorded by Saj y Emi", id 1OAA1iOLBZTZZH4RgCLKuEHkj8I1DkROB). Faceless is the priority track (owner, 3 Nov).

### Agent team (owner, 11 Nov 2026)

| Agent | Job | Hands to |
|---|---|---|
| Content finder & tracker | Outliers, trends, sounds, post results | Story planner (outliers) and story bank (results) |
| **Story planner** (`.claude/agents/story-planner.md`) | Picks one of 10 story formats (`storytelling-templates` skill), writes hook, timed script, on-screen text, shot list, caption | Reel maker: `content/<CODE>-<slug>/STORY-BRIEF.md` |
| Reel maker | Visuals, voice, music, SFX, export | Owner review |

In Workflow A step 5, the reels subagent is the story planner: launch it with the week brief and the finder's outliers. It logs every story and result in `content/STORY-BANK.md`. Storytelling covers **2 primary accounts**: @dubaibachata (informative) and @latincrazytribe (party), each with its own playbook in `storytelling-templates/references/account-playbooks.md`. Other accounts only on request.

**Content Hub (Notion, owner, 11 Nov 2026):** all agents read and write the Notion Content Hub (page `415eb2e4-50ad-81bb-a9eb-e904b1310c5d`, data source `collection://37649437-cc5a-4864-a478-dbc304017ada`). Status flow: Idea → Brief → In production → Review → Approved → Scheduled → Posted → Reported. The content tracker writes post metrics into each row at 48 h and 7 days and sets `Reported`. The owner approves by setting Status to `Approved`, or by leaving a comment on the row. Reel maker handoff (Drive folder per post code, Media link, Status): `content/REEL-MAKER-HUB-PROTOCOL.md`.

Name files `YYYY-MM-DD_<post-code>_<slide-or-part>` (e.g. `2026-11-03_P2_slide-01.jpg`). Nothing is scheduled until the owner has seen the actual media and said yes to that post.

## Workflows

### A. Weekly run (Monday automation, or "write week N")

1. Pull last 7 days for @dubaibachata (IGI, report `AccountMedia`: reach, likes, comments, saves, reel shares, avg watch time). Note the best and worst post and why.
2. Pull competitor and network activity for the last 7 days (IGPD2 `BusinessDiscoveryMedia`, handles in the Benchmark list below). Flag anything new: offers, launches, reveal campaigns.
3. Write the week brief (3 posts, dates, pillar, hook family, CTA, DM keyword, collaborators) and save it to `00 - Plan & Briefs`.
4. Create `01 - To Review / Week N (dates)` and one folder per post.
5. Launch two background subagents with the brief, `.claude/product-marketing.md`, the brand guide and the skill chain above (they must run `negative-hooks` and the humanizer pass): one for carousels (slides + copy doc), one for reels (script, shot list, on-screen text, cover, caption). Each uploads its copy docs to the post folders. They never publish.
6. Check every rendered image and every hook yourself, then publish a review page with all slides, covers, hooks and captions, and add a link doc to the week folder.
7. Run Workflow C (comments) and Workflow F (communication check).
8. Send the owner one message: the review link, the planned times and collaborators, what to film on Sunday, comment items that need them, and "Reply 'approve week N' to schedule everything."

### B. Approve and schedule ("approve week N", or a single post "approve P2 with collabs @x @y")

A weekly approval covers every post in that week's review page with the times and collaborators shown there. Run the steps below for each approved post.

1. For each image, in order: `creative_picker` action `create_upload_url` (ds_id `IGI`, account_id above, params `filename`, `content_type` `image/jpeg`, `size`), then `curl -X PUT -H "Content-Type: image/jpeg" --data-binary @file "<upload_url>"`; expect HTTP 200.
2. `manage_social_media` action `publish` with `validate_only: true`: account_id, `content_type` (`CAROUSEL`, `IMAGE` or `VIDEO`), caption, `upload_ref` (comma-separated in slide order), `publish_at` (e.g. `2026-11-04T19:00`), `timezone` `Asia/Dubai`, `platform_options` `{"collaborators": [...]}`. Fix anything it flags.
3. If the post, time and collaborators match what the owner approved, run the same call without `validate_only`. If anything changed after approval, show the change and get a yes first. If the result returns an approval link, give it to the owner.
4. Move the post folder to `02 - Final Poster`, then to `03 - Posted` once it is live.
5. Reels need the edited video first. Ask for the file, then upload it the same way with `content_type` `video/mp4`.

### C. Comments (weekly, inside the Monday run)

`list_comments` on every post from the last 14 days. The Reply Bank is ON (owner, 31 Oct): comments that match a Reply Bank type in `references/communication-playbook.md` get that reply posted with `comment`. List what was posted in the Monday message. Questions about price, complaints, personal stories and anything unclear always go to the owner. Never delete or hide a comment without the owner's say-so.

### F. Communication: the next stage (viewer → lead → student → regular)

Follow `references/communication-playbook.md`.
- Every post's CTA uses a DM keyword that has a script in the playbook. If a new keyword is needed, write its script first and tell the owner to add it to Instagram's automated responses.
- Instagram DMs and WhatsApp are not reachable from here. Claude writes and updates the scripts and quick replies; the owner pastes them into Instagram automations and WhatsApp Business once.
- Monthly: ask for counts per WhatsApp label (New lead, Trial booked, Attended trial, Package, Missed 2, Graduated, Festival interest) and report trial → package, Foundation → Improvers, and students active after 90 days.

### D. Monthly report (first Monday of the month)

Followers, reach, saves and shares, the top 3 and bottom 3 posts and why, bookings from DM keywords and UTM (ask the owner for counts), the competitor benchmark, and next month's plan. Publish as a page and save the summary to `00 - Plan & Briefs`.

### E. Research on demand

- Account or competitor: IGPD2 `BusinessDiscoveryAccount` + `BusinessDiscoveryMedia`.
- Hashtag: IGPD2 `HashtagSearchMedia` (`result_type` `top_media` or `recent_media`).
- Trend or reel: Instagram links cannot be opened here. Ask for screenshots or the video file; for video use Higgsfield `video_analysis_create` and `virality_predictor` (these use credits, so confirm first).

## Benchmark list

Schools: ricbanks.d.a, bachatadubai, onstagestudiodubai, bnfdanceacademy, jamesandalex, dcdancesportacademydubai, nefeli_mourtou, dancestudiosdubai, point.dancestudio, danceverseglobal
Festivals: dubai_latin_festival, fujairah_latin_festival, latin.notion
Own network: latincrazytribe, sajknightsbachata, emi_dancer_dubai, sajyemi, latinnightsdubai, dance_dubai_videos, socialdancejournal, latincrazyfestival.dubai, bachazouk.dubai, dubaibachata

Known data gap: for some accounts IGPD2 returns followers but no posts at all (even years back). Report that as "no data", never as "inactive".

## Guardrails

- No publishing, scheduling, commenting or paid generation without owner approval: a weekly "approve week N", a per-post yes, or the enabled Reply Bank for simple comments. Paid generation (Higgsfield credits, ManyChat) always needs a separate yes.
- No invented numbers, prices, testimonials or dates.
- Heritage: follow "Heritage and naming stance" above. Never call other dances "styles of bachata"; bachata is Dominican.
- The Supermetrics trial ends 13 Nov 2026. If calls return TRIAL_EXPIRED, stop and tell the owner; a paid plan must include "AI Chats".
- Instagram throttles bursts: space one account's scheduled posts at least 5 minutes apart.
