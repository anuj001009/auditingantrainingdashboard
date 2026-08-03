# Auditing & Training Dashboard

Sales-ops tooling for the Topmate HubSpot CRM (portal 244132076).

## Contents
- **dashboard.html** — Contact-management & coaching dashboard: contact bifurcation by stage/owner, workable-contact scoring, fresh-contact trends, rep scorecard, disposition-integrity audit, and the 15-min 1:1 rep-coaching module.
- **disposition.html** — Disposition workspace with three tabs:
  - *Audit the Kills* — review every NI/DQ/DNP/FU-DNP and mark each a **Real No** or a **Forced No**.
  - *Message Playbook* — current vs approved replacement message per stage, with A/B variants.
  - *Adherence* — capture what reps actually send and track on-script % before vs after training.
- **storyteller.html** — **Daily Storyteller**, a standalone, offline-friendly daily companion:
  - *A fresh story every day* (55+ curated stories, chosen deterministically by the date) across four categories — **Inspiring People** (Nimsdai Purja, Dashrath Manjhi, Ramanujan, APJ Abdul Kalam, Arunima Sinha, Kalpana Chawla, Mandela, Marie Curie, Shackleton…), **History**, **Geography**, and **Fun Facts**. Each has a pull-quote, a "spark" bonus fact, and a motivational takeaway.
  - *Spark word of the day* — 30 uplifting words with meanings (Sisu, Ikigai, Jugaad, Seva…).
  - *Daily Journal* — **☀️ Morning planning** and **🌙 Night dump** notes, auto-saved per day, with day-to-day navigation.
  - *Up Next* — a personal reading/explore queue (add, check off, remove).
  - Browse by category, *Surprise me* shuffle, prev/next day, and saveable favourites. All personal data lives in the browser's localStorage.
- **index.html** — landing page linking the tools.
- **server.js** / **package.json** / **Procfile** — a tiny zero-dependency Node static server so the whole thing can be hosted on Railway (or any Node host).

## Deploying to Railway
The site is plain static HTML served by `server.js` (no build step, no dependencies).
1. Push this repo to GitHub (already set up).
2. In [Railway](https://railway.app): **New Project → Deploy from GitHub repo** and pick this repo.
3. Railway auto-detects Node via `package.json` and runs `npm start` (`node server.js`). The server listens on the `PORT` Railway provides — no config needed.
4. Under the service's **Settings → Networking**, click **Generate Domain** to get a public URL.

The landing page is at `/`, and the storyteller at `/storyteller.html`.
To run locally: `npm start` then open `http://localhost:3000`.

## Important: live data requires Cowork
These pages pull live HubSpot data through the Claude **Cowork** bridge (`window.cowork.callMcpTool`).
On a plain static host (e.g. GitHub Pages) that bridge does not exist, so the data-driven views
(Audit tab, owner dropdowns, the whole contact dashboard) will not load. The **Message Playbook**
and the manual **Adherence** capture work fully standalone (they use browser localStorage).

This repo is therefore primarily for version control, backup, and sharing the standalone tools.
