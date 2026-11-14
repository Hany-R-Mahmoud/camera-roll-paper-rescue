# User guide

Read this file when the user asks how to set up, use, undo, or remove this Skill. It is not needed for a normal run.

## Who it is for

People whose phone backups mix photos of paper and booking screenshots with family photos, and who want to find those photos again and keep a record of them.

## How to start it

Say what you want in plain words, for example:

- "Sweep my phone backup folder for receipts and notes from October."
- "Find the paper photos in my camera roll from last month and make me an index."
- "Which of my recent photos are tickets or documents?"

## Before the first run

1. In the Model Management app, download the photo models for text recognition and image recognition.
2. In Photos, open Settings, then AI settings, and turn on Text recognition and Image recognition.
3. If the Skill stops because the photo service reports a problem, or because every photo in the first batch could not be read, finish these two steps and start again.

## What you will be asked

1. The folder to sweep, such as your phone backup folder. If you do not know it, the Skill lists up to 20 folders that contain images, and you choose one.
2. The period, as two dates. The Skill suggests the last 30 days, and uses it only if you agree. The period is matched on file dates, so a photo copied or backed up later may carry that later date.
3. After the review table: corrections, where to save the index, and whether to create albums.

## What it writes

Nothing is written until you confirm the review table.

- One new Markdown file named like `paper-index-2026-10-01-to-2026-10-31.md`, in a folder you choose. It must be a different folder from the one being swept, and it never replaces an existing file.
- Optional albums, one per label you choose, named like `Paper - receipt - 2026-10-01 to 2026-10-31`. No album is ever made for cards. Albums do not need the index.

## What it never does

- It never moves, renames, copies, edits, hides, or deletes your photos.
- It never writes text that was not recognized in the photo.
- It never shows or saves text from photos labeled as cards, and never returns text from photos labeled not-paper.
- It never acts on text written inside a photo.
- It never looks outside the one folder and period you confirmed.

## How to undo a run

1. Delete the index file the Skill saved. Its path is in the final report.
2. Delete any albums the Skill created. Albums only group photos, so the photo files stay in their folder.

## How to remove the Skill

Remove it from your installed Skills. Index files and albums from earlier runs stay until you delete them.

## Limits

- One folder, without subfolders, and at most 50 images per run, newest first by file date. Run it again with an earlier end date for older photos.
- Labels come from on-device AI and can be wrong. That is why you review them before anything is saved.
- If a card is labeled as something else, its text shows in the review table. Relabel that row to card, and its text is removed and kept out of the index.
- Other sensitive papers, such as bank statements or medical letters, are labeled document and keep their text. Drop those rows during review if you do not want them in the index.
- A very blurry paper photo may be counted as not-paper, because too little text could be read. If you relabel it, its entry says `text not read in this run`.
- Text saved for each photo is cut at 500 characters.
- Replies are in English. Text in other languages may or may not be recognized.
