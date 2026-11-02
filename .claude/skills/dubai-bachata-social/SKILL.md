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
| 5. Human pass (mandatory) | `instagram-skills/skills/ig-humanizer`, `copywriting` | Remove AI tells; must read like Saj & Emi talking |
| 6. Conversion | `emails`, `referrals`, `community-marketing`, `churn-prevention`, `events` | Communication stage, retention, festival campaigns |

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

Each brand has its own content. Before proposing or posting anything, check which brand the footage belongs to.

| Account | Content that belongs here | Never post here |
|---|---|---|
| @dubaibachata | Saj & Emi's weekly classes in JLT (Foundation, Improvers, Advanced), beginner tips, student stories, class montages, Monday practice | Bacha Fusion / BachaZouk weekender footage, guest teachers (Tonio & Liza, Rami & Nefeli, Henar, Papi J), Jack & Jill, pool parties, festival passes |
| @bachazouk.dubai (Bacha Fusion) | Bacha Fusion Weekender, BachaZouk workshops, guest-teacher classes and demos, Jack & Jill. Drive: "bachafusion marketing" (1w9YJ8EjeQonu_pOeJbCsHPxlldqdzprf), "Amaze raw" | Beginner class promos for @dubaibachata |
| @latincrazytribe | Parties (Room 44, SoBe, TT DXB), Halloween, Slasher Friday, Mad House | Class teaching content as its main post |
| @latincrazyfestival.dubai | Latin Crazy Festival 26–29 March 2027 | Weekender content |

Weekender footage may reach @dubaibachata only as a Collab invite from @bachazouk.dubai, and only if the owner asks. @dubaibachata's own footage lives in "Dubai Bachata Explainer" and the Thursday class shoots.

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

## Drive pipeline

LCT-Business-Vault / 08 - Content Operations / Dubai Bachata (`1V1YqH45zmqx-UpM6WpGCeUXR0_d-3Cah`)

| Folder | ID | Holds |
|---|---|---|
| 00 - Plan & Briefs | `1XIDsHNQrrcggC3teZ7FOwIF98CFJGAs1` | Weekly briefs, reports, competitor summaries |
| 01 - To Review | `1HBl19htfDRHaFlqg0MqKtnqIYXwNFdVv` | One subfolder per week, one per post, each with a copy doc |
| 02 - Final Poster | `1FPsR2_mcnIYhvv54xy-q-Zl5a5n8K8dI` | Approved posts |
| 03 - Posted | `1KaEHASOloxpuJuHfF06Tuvfifs4sokmc` | Live posts |

Drive takes text only. Images go on a review page (Artifact) and are uploaded straight to Instagram at scheduling time.

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
- The Supermetrics trial ends 13 Nov 2026. If calls return TRIAL_EXPIRED, stop and tell the owner; a paid plan must include "AI Chats".
- Instagram throttles bursts: space one account's scheduled posts at least 5 minutes apart.
