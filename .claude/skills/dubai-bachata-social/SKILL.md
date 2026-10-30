---
name: dubai-bachata-social
description: Run the Dubai Bachata / Latin Crazy Tribe social media engine. Use for the weekly content run ("write week N", the Monday automation), approving and scheduling posts ("approve P2"), account audits, competitor benchmarks, hashtag scans, comment replies and the monthly report for @dubaibachata and the LCT account network.
---

# Dubai Bachata Social Engine

One system for planning, producing, approving, scheduling and reporting Instagram content for Dubai Bachata (Saj & Emi, B-YOU Method, JLT) and the Latin Crazy Tribe network. The owner approves; Claude does the rest. Nothing is published or scheduled without the owner's explicit approval of that post.

## Sources of truth (read before producing anything)

| What | Where |
|---|---|
| Brand guide (palette, type, layout) | Drive file `1-BzhKKkz8c8uGV07ydqOAE5Aea4B8Ka8` (Dubai Bachata Brand Guide.md) |
| Hook skill (10 negative-hook families) | Drive file `1N4hmcsOaO4MG10YXH30pGzJHmFF3ZcNL` (negative-hooks-skill.md) |
| Competitor map and retention playbook | https://claude.ai/artifact/XA6vRJnxsM2SzpiRgmAnrq |
| Week 1 review page (format reference) | https://claude.ai/artifact/DzMBdZeTkXRKfDNf6z8sih |
| Instagram craft rules | `instagram-skills` bundle (carousel spine, 125-character caption hook, 3–5 hashtags, humanizer) |

Markdown files on Drive download as base64: decode with `base64 -d` into the scratchpad before reading.

## Facts you may use (never invent others)

- Teachers: Saj & Emi · Method: B-YOU · Brand family: Latin Crazy Tribe (LCT)
- Venue: Dance Case Studio, Fortune Executive Tower, Cluster T, JLT, Dubai
- Classes: SUN 8 PM Foundation · 9 PM Improvers | MON 9–11 PM Practice Night | THU 7:30 Foundation · 8:30 Improvers · 9:30 Advanced (owner to confirm Thu vs Wed)
- No partner needed. Trial AED 50 (per website; confirm before quoting). No other prices.
- LCT nights: Thu Room 44 · Fri SoBe · Sat TT DXB. LCT Festival: 1–5 Apr 2027 (moved from 26–30 Mar).
- DM keywords: START, CLASS, SOCIAL, PRACTICE, SUNDAY, BACHATA
- Bio link (UTM): `https://bachataindubai.dance?utm_source=instagram&utm_medium=social&utm_campaign=bio-link&utm_content=dubaibachata`

## Accounts and roles

| Role | Accounts | Job |
|---|---|---|
| Faces | @sajknightsbachata (13.5k), @emi_dancer_dubai (9.2k) | Personality and demos; highest engagement in the market |
| Brands | @dubaibachata (classes), @bachazouk.dubai, @latincrazytribe (parties), @latincrazyfestival.dubai | Convert to bookings, entries, tickets |
| Amplifiers | @dance_dubai_videos (34k), @socialdancejournal, @latinnightsdubai | Reach; add as Collab partners |
| Merge (owner's call) | @sajyemi | Point bio to @dubaibachata |

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
- Hooks: use the hook skill. Pick the family that fits, keep reel hooks to 12 words or fewer, give 3 options and mark one. Community brand: soft, never shaming. The body must deliver the hook's promise.
- Every post ends with "Follow for a new move every week" plus one action (DM keyword or link in bio).
- Captions: hook in the first 125 characters, 3–5 hashtags, run the humanizer pass.
- Visuals: carousels 1080×1350 JPEG, reel covers 1080×1920 JPEG, rendered from HTML with Playwright. Cream base, Ink headlines in Anton, Inter body, one Coral accent, black text on coral for CTAs.
- Weekly volume: @dubaibachata 4 posts (Mon reel, Wed carousel, Fri reel, Sun promo), @bachazouk.dubai 2, festival 2. Everything else is a Collab or a repost.

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
3. Write the week brief (4 posts, dates, pillar, hook family, CTA) and save it to `00 - Plan & Briefs`.
4. Create `01 - To Review / Week N (dates)` and one folder per post.
5. Launch two background subagents with the brief, brand guide and hook skill: one for carousels (slides + copy doc), one for reels (script, shot list, on-screen text, cover, caption). Each uploads its copy docs to the post folders. They never publish.
6. Check every rendered image yourself, then publish a review page with all slides, covers, hooks and captions, and add a link doc to the week folder.
7. Tell the owner: review link, what needs filming at the Sunday class, open questions.

### B. Approve and schedule ("approve P2 with collabs @x @y")

1. For each image, in order: `creative_picker` action `create_upload_url` (ds_id `IGI`, account_id above, params `filename`, `content_type` `image/jpeg`, `size`), then `curl -X PUT -H "Content-Type: image/jpeg" --data-binary @file "<upload_url>"`; expect HTTP 200.
2. `manage_social_media` action `publish` with `validate_only: true`: account_id, `content_type` (`CAROUSEL`, `IMAGE` or `VIDEO`), caption, `upload_ref` (comma-separated in slide order), `publish_at` (e.g. `2026-11-04T19:00`), `timezone` `Asia/Dubai`, `platform_options` `{"collaborators": [...]}`. Fix anything it flags.
3. Show the owner the exact post, time and collaborators, and get an explicit yes. Then run the same call without `validate_only`. If the result returns an approval link, give it to the owner.
4. Move the post folder to `02 - Final Poster`, then to `03 - Posted` once it is live.
5. Reels need the edited video first. Ask for the file, then upload it the same way with `content_type` `video/mp4`.

### C. Comments ("reply to comments on P2")

`list_comments` for the post, draft replies in the brand voice (warm, short, a question back), show them, and post only the approved ones with `comment`. Never delete or hide without the owner's say-so.

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

- No publishing, scheduling, commenting or paid generation without the owner's explicit yes for that item.
- No invented numbers, prices, testimonials or dates.
- The Supermetrics trial ends 13 Nov 2026. If calls return TRIAL_EXPIRED, stop and tell the owner; a paid plan must include "AI Chats".
- Instagram throttles bursts: space one account's scheduled posts at least 5 minutes apart.
