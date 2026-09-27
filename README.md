# IB Tracker

Fortnightly tracker for the first term of the IB Diploma (DP1, 28 Sep – 21 Dec 2026; dates follow the official Catalan school calendar 2026–27).
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

- Open the live page and bookmark it (⌘D), or in Safari choose **File → Add to Dock** to open it like an app. If you do, keep using that same one: the Dock app and the Safari tab keep separate saved progress.
- Always use the same Mac, the same browser and the same address, or the ticks won't be there.
- Backup files download to the Downloads folder. Move them into one folder (for example `Documents/IB Tracker backups`) or upload them to `backups/` here.

## Backing up and restoring

1. *Backup & restore* → **Download backup file**. You get `ib-tracker-backup-YYYY-MM-DD.json`.
2. Keep the files in one folder, or upload them to [`backups/`](backups/) in this repository
   (GitHub → `backups` → *Add file* → *Upload files* → *Commit*). Git keeps every version.
3. To recover: *Restore from file* → choose the file → **Replace progress**.
   The progress being replaced is kept as a snapshot first, so a restore can itself be undone.

A backup file can move progress between the two versions (download from one, restore into the other).

## Changing the tracker without losing progress

Progress is saved against item positions, for example `s2.phy.3` = Sprint 2, Physics, 4th item.
Code changes never delete saved progress, but moving items changes what a saved tick points to. So:

- **Add** new items at the **end** of a list. Safe.
- **Reword** an item without changing its meaning. Safe.
- **Do not reorder or delete** items in a sprint that already has ticks. To retire one, reword it to start with "(Dropped)".
- **Do not change** `LS_KEY` (`dp1-term1-v1`) or the sprint/subject ids (`s1`–`s6`, `phy`, `mat`, `eng`, `bus`, `his`, `lit`, `core`, `hab`).
- **Download a backup file before any edit**, then open the page and check the ticks still look right.
- For Term 2, copy `index.html` to a new file and give it a new `LS_KEY` (e.g. `dp1-term2-v1`), so each term keeps its own record.

Edit on GitHub: open `index.html` → pencil icon → change → *Commit changes*. The live page updates in 1–2 minutes.
