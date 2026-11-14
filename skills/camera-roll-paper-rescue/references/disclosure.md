# Disclosure

## Third-party components and open source libraries

None. The package contains only Markdown files. It includes no libraries, scripts, binaries, models, or data sets, and it calls no outside service.

## Data handling

- The Skill works only on the one folder and period the user confirms, with at most 50 images per run.
- All reading, text recognition, image understanding, saving, and album creation are delegated to the registered NAS experts (`photo-agent`, `file-agent`, `knowledge-agent`).
- The Skill does not choose an AI model and calls no outside service itself. Text recognition and image understanding use the NAS photo capabilities as they are configured on the device.
- Data flow: photo files in the chosen folder go to the photo expert on the NAS. Labels, file paths, dates, and allowed recognized text come back into the Uliya conversation for review. After the user confirms, the index text goes to the knowledge expert and is saved as one Markdown file on the NAS, and album requests go to the photo expert.
- The Uliya conversation and the expert agents use the models the user has set up on the device. If the user runs them on a cloud AI model, the text shown in the review and saved in the index leaves the NAS for that model. Testing uses synthetic sample photos only.
- The Skill instructs the photo expert not to return any text for photos labeled as cards (identity cards, passport and driving licence pages, payment, membership, and business cards) or as not-paper. Card text never goes into the review table or the index.
- A card that the AI labels as something else keeps its text until the user relabels it to card in the review step. Other sensitive papers, such as bank statements or medical letters, are labeled document and keep their text unless the user drops them.
- Text found inside photos is treated as content only. The Skill does not act on anything it says.
- Original photos are only read. Nothing is moved, renamed, copied, edited, hidden, or deleted.

## Principal functionality developed for this hackathon

All of the Skill was written during the UGREEN Hackathon 2026 Round 1 submission period:

- The sweep workflow: health check, bounded image listing sorted by the Skill, batched text-first labeling, user review with corrections, saved index, and optional albums.
- The label rules, including the `unsure` label for text-heavy photos that are not paper, and the rule that a receipt needs a visible total or amount paid.
- The privacy rules that withhold card text and never return text from not-paper photos.
- The count check that places every file in the run list in exactly one count.
- The index format and the completion and failure handling.

## AI tools used and their principal uses

- **Muse (Meta)**: an early explanation of the uliya-skill-kit, research on user needs and gaps in UGREEN AI NAS, and a first ranked list of Skill ideas.
- **Claude Code (Anthropic)**: brainstorming that produced this Skill idea and its name, research on comparable products, idea comparison against the capability catalog, drafting and reviewing this Skill, running the UGREEN static checker, preparing a fact sheet and word counter for the proposal, and giving feedback on the entrant's proposal drafts. The proposal answers were written by the entrant.
- **UGREEN uliya-skill-kit (UGOS Skill Creation Tool)**: the Uliya Skill Development Standard, the capability catalog (version 2.0.0), and the static checker used to validate this package.
