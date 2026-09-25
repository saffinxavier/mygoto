# MyGoTo

Personal click-to-open catalog of skills, tools, UI kits, and platforms for Codex and Cursor.

**Live:** https://saffinxavier.github.io/mygoto/  
**Repo:** https://github.com/saffinxavier/mygoto

## Open locally

Open `index.html` in a browser (no build step).

## Project picker prompt

When starting work in **any** Codex or Cursor project:

1. Open [PROMPT.md](PROMPT.md) and copy the matching prompt block, **or**
2. On the catalog page, select **Codex** or **Cursor**, click **Copy project prompt**, then paste it into that project's agent chat.

The agent will inspect the repo and recommend only 3–7 catalog items, with setup and use steps for the selected assistant. The same toggle changes each card's guidance and **Copy prompt** text. Codex is the initial selection; the page remembers your last choice in this browser.

## GitHub Pages

Deploys from `main` via `.github/workflows/pages.yml`.

First-time setup (once): repo **Settings → Pages → Source → GitHub Actions**.

## Data

Catalog entries live only in `index.html` (`entries` array). Each card includes `summary`, `useFor`, `skipWhen`, `codexHow`, `cursorHow`, and optional install hints. Codex-specific commands use `codexInstallHint` when a shared `installHint` would be wrong.
