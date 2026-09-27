# IB Tracker

Fortnightly tracker for the first term of the IB Diploma (DP1, 28 Sep – 21 Dec 2026; dates follow the school's 2026–27 calendar: partial exams 5–23 Oct, term exams 20–26 Nov).
Live page: https://marcosdagama.github.io/IB-Tracker/

## What it measures

- **Items ticked** per sprint and subject. Each tick stores the date it was made.
- **On time:** share of ticked items that were ticked by the end of their sprint.
- **Self-check ratings** (1–4) for Physics and Maths in every sprint, shown in the *Confidence by sprint* table.
- **Reflection notes** for each sprint.

## Where progress is stored

| Version | Storage | Backup |
|---|---|---|
| Claude page (shared with family) | Shared record on claude.ai | Automatic daily snapshot, restorable from the *Backup & restore* panel, plus backup files |
| This GitHub page | This browser, on this device only (`localStorage`) | Backup files only |

Browsers can clear saved site data (Safari does after a period without visits, and "Clear history" does too).
**Download a backup file every Friday** from the *Backup & restore* panel.

## Using it on a Mac with Safari

- **Add it to the Dock (recommended):** open the live page in Safari → **File → Add to Dock…** → keep the name *IB Tracker* → **Add**. It gets its own teal "IB" icon, opens in its own window without Safari's toolbar, and appears in Launchpad and Spotlight (⌘Space, "IB Tracker").
- Use only the Dock app from then on. The Dock app and a Safari tab keep **separate** saved progress. If ticks were already made in a Safari tab, download a backup file there and use *Restore from file* in the Dock app.
- To remove it: right-click the icon → Options → Remove from Dock (the app itself is in `~/Applications`).
- Always use the same Mac, the same browser and the same address, or the ticks won't be there.
- Backup files download to the Downloads folder. Move them into one folder (for example `Documents/IB Tracker backups`) or upload them to `backups/` here.

## Backing up and restoring

1. *Backup & restore* → **Download backup file**. You get `ib-tracker-backup-YYYY-MM-DD.json`.
2. Keep the files in one folder, or upload them to [`backups/`](backups/) in this repository
   (GitHub → `backups` → *Add file* → *Upload files* → *Commit*). Git keeps every version.
3. To recover: *Restore from file* → choose the file → **Replace progress**.
   The progress being replaced is kept as a snapshot first, so a restore can itself be undone.

A backup file can move progress between the two versions (download from one, restore into the other).

## Public and private versions

This public page leaves out personal details (student's name, school, teachers' names). The private version on claude.ai also shows the teachers.
The source keeps private parts between `<!--PRIVATE-->` and `<!--/PRIVATE-->` markers, which are removed before publishing here.

## Changing the tracker without losing progress

Progress is saved against item positions, for example `s2.phy.3` = Sprint 2, Physics, 4th item.
Code changes never delete saved progress, but moving items changes what a saved tick points to. So:

- **Add** new items at the **end** of a list. Safe.
- **Reword** an item without changing its meaning. Safe.
- **Do not reorder or delete** items in a sprint that already has ticks. To retire one, reword it to start with "(Dropped)".
- **Do not change** `LS_KEY` (`dp1-term1-v1`) or the sprint/subject ids (`s1`–`s6`, `phy`, `mat`, `eng`, `bus`, `his`, `lit`, `core`, `hab`).
- **Download a backup file before any edit**, then open the page and check the ticks still look right.
- For Term 2, copy `index.html` to a new file and give it a new `LS_KEY` (e.g. `dp1-term2-v1`), so each term keeps its own record. Then update `TERM` (name and school date ranges such as exams) and `SPRINTS` (dates, days off, items). The term calendar, timeline and school-day counts are drawn from those two lists automatically.

Edit on GitHub: open `index.html` → pencil icon → change → *Commit changes*. The live page updates in 1–2 minutes.
