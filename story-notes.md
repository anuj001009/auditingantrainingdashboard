# Daily Storyteller — Story Notes & Nightly Brief

This file is the **inbox** for the nightly Daily Storyteller job. Every night an automated
Claude session reads this file, applies your requests, adds a fresh story or two, and pushes
to `main` (which auto-deploys to Railway).

> Your in-app **Journal** and **Up Next** list live in your browser and can't be read by the
> nightly job. So write anything you want the story system to act on **here** instead.

---

## ✍️ Thoughts & requests  — *edit this section anytime*

<!-- Examples:
- Add more stories about scientists and explorers.
- Keep the tone upbeat — fewer sombre endings.
- Add a story about Kalpana Chawla's childhood.
- Add real photos for the Iceland and Baikal stories.
- Loved the Nimsdai one — more mountaineering, please.
-->

- 

---

## ⚙️ Nightly job rules

- Add **1–2 new, non-duplicate** stories each run (check existing titles in `storyteller.html`).
- Keep the object shape: `cat`, `emoji`, `title`, `who`, `body[]`, `pull`, `spark`, `takeaway`.
- Keep the voice **positive, motivating, exciting, fun** — a mix of inspiring people, history,
  geography, and fun facts. Prefer globally diverse subjects (including Indian figures).
- Map each new story to an existing scene in `ART` / `SCENES` (add a new SVG scene only if needed).
- Optionally add a Wikimedia Commons photo to `PHOTOS` if a well-known file exists.
- Apply everything under **Thoughts & requests**, then move handled items to the log below,
  stamped with the date.
- Run a JS syntax check, then commit and push to `main`.

---

## 🌙 Nightly log  — *the job appends here*

- (nothing yet)
