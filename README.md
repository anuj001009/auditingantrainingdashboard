# Daily Storyteller

A fresh dose of motivation, wonder, and fun — every single day.

A standalone, offline-friendly page that serves a new story each day, plus a light daily journal. Deployed on Railway; auto-redeploys on every push to `main`.

## What's inside
- **A fresh story every day** — 55+ curated stories, chosen deterministically by the date, across four categories:
  - **Inspiring People** — Nimsdai Purja, Dashrath Manjhi, Ramanujan, APJ Abdul Kalam, Arunima Sinha, Milkha Singh, Kalpana Chawla, Nelson Mandela, Marie Curie, Jane Goodall, Shackleton, and more.
  - **History** — the Christmas Truce, the Rosetta Stone, the Antikythera mechanism, the invention of zero, Apollo 13, Machu Picchu…
  - **Geography** — Everest, the green Sahara, Angel Falls, the Mariana Trench, Socotra, the aurora, living root bridges…
  - **Fun Facts** — the octopus, immortal honey, tardigrades, the wood-wide-web, "you are stardust"…
  - Each story carries a pull-quote, a "spark" bonus fact, and a motivational takeaway.
- **Spark word of the day** — 30 uplifting words with meanings (Sisu, Ikigai, Jugaad, Seva…).
- **Daily Journal** — ☀️ Morning planning and 🌙 Night dump notes, auto-saved per day, with day-to-day navigation.
- **Up Next** — a personal reading/explore queue (add, check off, remove).
- Browse by category, *Surprise me* shuffle, prev/next day, and saveable favourites.

All personal data (journal, reading list, favourites) lives in the browser's `localStorage` — nothing leaves your device.

## Files
- **storyteller.html** — the whole app, self-contained (HTML/CSS/JS in one file).
- **index.html** — redirects the site root to the storyteller.
- **server.js** / **package.json** / **Procfile** — a tiny zero-dependency Node static server (honours the `PORT` env var) so it runs on Railway or any Node host.

## Run locally
```
npm start        # serves on http://localhost:3000
```
Or just open `storyteller.html` directly in a browser — it needs no server.

## Deploy
Hosted on Railway from the `main` branch (`npm start` → `node server.js`). Any push to `main` auto-redeploys.
