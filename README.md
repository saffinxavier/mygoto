# MyGoTo

Personal click-to-open catalog of Cursor skills, tools, UI kits, and platforms.

**Live:** https://saffinxavier.github.io/mygoto/  
**Repo:** https://github.com/saffinxavier/mygoto

## Open locally

Open `index.html` in a browser (no build step).

## Project picker prompt

When starting work in **any** Cursor project:

1. Open [PROMPT.md](PROMPT.md) and copy the prompt block, **or**
2. On the catalog page, click **Copy project prompt**, then paste into that project’s Cursor chat.

The agent will inspect the repo and recommend only 3–7 catalog items, with Cursor install/use steps.

## GitHub Pages

Deploys from `main` via `.github/workflows/pages.yml`.

First-time setup (once): repo **Settings → Pages → Source → GitHub Actions**.

## Data

Catalog entries live only in `index.html` (`entries` array). Each card includes `summary`, `useFor`, `skipWhen`, optional `installHint`, and `cursorHow` (how to use it with Cursor).
