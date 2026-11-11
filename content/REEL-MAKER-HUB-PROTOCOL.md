# Reel maker ↔ Content Hub protocol

This is how every reel and carousel moves from brief to review. It applies to any reel-making agent or person.

**Content Hub (Notion):** https://app.notion.com/p/415eb2e450ad81bba9ebe904b1310c5d
Database "Content", data source `collection://37649437-cc5a-4864-a478-dbc304017ada`

## 1. Pick up work
- Take rows with **Status = Brief**. The brief is in the row's page, with a repo copy at `content/<CODE>-<slug>/STORY-BRIEF.md`.
- Set **Status → In production** when you start.
- Paid tools (Higgsfield etc.) need the owner's yes each time. Ask with a comment on the row.

## 2. Save the media to Google Drive
Path: `Dubai Bachata › 01 - To Review › <format folder> › <CODE>/`

| Format | Folder ID |
|---|---|
| 1. Carousels | `1ZTzrnGUvrXaWbqmhPLs6QefQT1_CPLSA` |
| 2. Stories | `1CL6CIzNZozoAibLJyInppUXpl-pi4MQw` |
| 3. Reels | `1Tc97-YbFm3tOLGoNK9gDdSaGfU-fYUln` |
| 4. 4:5 Carousel Videos | `1enc5oW4S8qGvj2oMipSFOPoI8bxGFk4D` |

One folder per post, named with the hub Code (e.g. `LCT-01`). Inside it:
- Reels: `<CODE>_final.mp4`, `<CODE>_voice-only.mp4`, `<CODE>_cover.jpg`, `<CODE>_POST.txt` (caption, hashtags, first comment), `<CODE>_NOTES.md` (voice, music track + licence, anything not done)
- Carousels: `<CODE>_slide-01.jpg` …, `<CODE>_POST.txt`
- New version: add `_v2`, `_v3`. Never overwrite the previous version.

## 3. Hand back in the hub
On the row:
- **Media link** = the Drive folder URL
- **Status → Review**
- **Needs from owner** = one line on what to check (e.g. "check the music cuts at 2.2 s")
- Anything open goes in as a comment on the row

## 4. After review
- **Approved** → move the folder to `02 - Final Poster / <same format folder>` and update the Media link.
- **A comment asking for changes** → make a new version (`_v2`), keep the Media link pointing at the folder, set **Status → Review** again.
- **Posted** → move the folder to `03 - Posted` (`1KaEHASOloxpuJuHfF06Tuvfifs4sokmc`), set **IG link**.
- Never post to Instagram yourself. Only the owner approves.
