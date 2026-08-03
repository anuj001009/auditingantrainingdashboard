# Auditing & Training Dashboard

Sales-ops tooling for the Topmate HubSpot CRM (portal 244132076).

## Contents
- **dashboard.html** — Contact-management & coaching dashboard: contact bifurcation by stage/owner, workable-contact scoring, fresh-contact trends, rep scorecard, disposition-integrity audit, and the 15-min 1:1 rep-coaching module.
- **disposition.html** — Disposition workspace with three tabs:
  - *Audit the Kills* — review every NI/DQ/DNP/FU-DNP and mark each a **Real No** or a **Forced No**.
  - *Message Playbook* — current vs approved replacement message per stage, with A/B variants.
  - *Adherence* — capture what reps actually send and track on-script % before vs after training.
- **storyteller.html** — Daily Storyteller: a standalone, offline-friendly page that serves a fresh motivational story each day. Rotates through inspiring people (Nimsdai Purja, Wangari Maathai, Shackleton, Katherine Johnson…), history, geography, and fun facts, plus a "spark word of the day." Browse by category, hit *Surprise me*, and save favourites (stored in browser localStorage).
- **index.html** — landing page linking the tools.

## Important: live data requires Cowork
These pages pull live HubSpot data through the Claude **Cowork** bridge (`window.cowork.callMcpTool`).
On a plain static host (e.g. GitHub Pages) that bridge does not exist, so the data-driven views
(Audit tab, owner dropdowns, the whole contact dashboard) will not load. The **Message Playbook**
and the manual **Adherence** capture work fully standalone (they use browser localStorage).

This repo is therefore primarily for version control, backup, and sharing the standalone tools.
