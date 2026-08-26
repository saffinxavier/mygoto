# MyGoTo Catalog Objective

## What this project is
- Personal, click-to-open browser catalog for your Cursor go-to links.
- Converts raw WhatsApp-style links into practical cards with plain-English guidance.
- Built as a single-file app (`index.html`) with embedded data.

## Audience
- Primary user: you.
- Usage pattern: open `index.html`, search fast, choose a tool/skill, open link.

## Output style for every entry
- Use plain English.
- Always include:
  - What it is (one-line summary).
  - Use for (example like "use this for dashboard").
  - Skip when (when not to use it).
- Prefer concrete wording over generic statements.
- Keep each field short and scannable.

## Category definitions
- `skill`: Agent skill packs or behavior frameworks.
- `tool`: Libraries, CLIs, frameworks, testing tools, utilities.
- `ui-kit`: Component collections or design-focused UI libraries.
- `guideline`: UI/UX quality standards or best-practice docs.
- `platform`: Hosted products, model playgrounds, and provider portals.
- `security`: Deployment or security-focused resources.
- `automation`: Workflow automation platforms.

## Single source of truth
- Keep the catalog data in `index.html` only, inside the `entries` array.
- Keep `my go to list.txt` as raw capture history only.
- Do not create duplicate JSON/CSV copies unless explicitly requested.

## Append workflow (when adding new tools/skills)
1. Read this file and follow it directly.
2. Resolve canonical URL (repo/docs/site) if possible.
3. If only share link is available, still add the card and set `sourceNote` to verify.
4. Add one new object to `entries` in `index.html` with:
   - `id`, `name`, `category`, `tags`
   - `summary`, `useFor`, `skipWhen`
   - `link`, `sourceNote`, optional `installHint`
5. Keep copy plain-English and decision-friendly.
6. Validate search + filters still work.

## Rule for future agent sessions
- Do not ask for full context again.
- Use this objective file plus `.cursor/rules/my-goto.mdc` as the standing brief.
