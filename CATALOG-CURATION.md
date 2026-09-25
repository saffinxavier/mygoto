# MyGoTo — catalog curation prompt

Reusable instructions for reviewing the catalog and evaluating new candidates.
Use this when you have new links to consider — not for picking tools in another project (that is [PROMPT.md](PROMPT.md)).

**Live catalog:** https://saffinxavier.github.io/mygoto/  
**Source of truth:** `index.html` → `entries` array  
**Standing brief:** [OBJECTIVES.md](OBJECTIVES.md) and `AGENTS.md` (Codex) or `.cursor/rules/my-goto.mdc` (Cursor)

---

## How to use

1. Open this MyGoTo repo in Codex or Cursor.
2. Copy the **Prompt** block below into chat.
3. Paste your candidate URLs (and optionally note prune aggressiveness).
4. Let the agent propose removes/adds; confirm before it edits if you want a review pass first.

---

## Prompt

```text
You are curating my personal MyGoTo catalog (Codex and Cursor go-to links).

Read and follow:
- OBJECTIVES.md
- AGENTS.md when using Codex, or .cursor/rules/my-goto.mdc when using Cursor

Single source of truth: the `entries` array in index.html only.
Do not create duplicate JSON/CSV copies. Keep the app static (no framework/build step).
Do not replace PROMPT.md (that is the project-picker prompt).

## Principle
Optimise for quality, usefulness, and long-term value — not list size.
When uncertain about an item, explain why it may or may not be worth keeping; do not auto-add.

## Categories (exact)
skill | tool | ui-kit | guideline | platform | security | automation

## Entry shape (every card)
id, name, category, tags, summary, useFor, skipWhen, codexHow, cursorHow, link, sourceNote, optional installHint and codexInstallHint
- Plain English; short and scannable.
- Prefer canonical repo/docs URLs.
- If only a short/share link exists, still add and set sourceNote to verify destination.
- Check assistant-specific setup. Set codexInstallHint to a Codex command when installHint is Cursor-only, or null when no Codex command is verified.

## Process

### 1. Review the existing list
- Analyse every current entry in index.html `entries`.
- Flag items that are outdated, dead, redundant, low-quality, vague dump leftovers, or no longer worth keeping.
- Remove those from `entries` (delete the objects).
- Keep items that are still useful and distinct.

### 2. Evaluate new candidates
Paste candidates below (URLs and/or names). For each:
- What it is (1–2 sentences).
- Usefulness, quality, relevance, durability for a Codex and Cursor go-to catalog.
- Verdict: ADD | SKIP | UNCERTAIN (with reason).
- If ADD: category + note any overlap with an existing entry.
- Do not add just because it was mentioned.
- Do not add duplicates or near-duplicates of something already listed (update the existing card instead if needed).

### 3. Apply changes
- Edit only index.html `entries` (and this file / OBJECTIVES.md only if the curation process itself needs an update).
- For each ADD, write a full card matching the entry shape above.
- After edits: no duplicate ids; Graphify (or any given id) appears at most once; filters/categories still valid.

### 4. Report
End with a short summary:
- Removed: id — reason
- Added: id — one-line why
- Skipped / uncertain: name — reason

## Prune aggressiveness (optional; default = hard removes only)
- hard_only: remove clear weak/dead/redundant items; keep borderline REVIEW items unless I say otherwise
- also_trim_overlap: also drop overlapping siblings when a stronger card already covers the job
- aggressive: hard removes + clear overlap trim for a tighter list

Default for this run: hard_only
Override: ________

## Candidates to evaluate
(paste URLs / names below)

```

---

## Notes from prior curation (examples of SKIP reasons)

Useful patterns — not hard rules:

- Inspiration-only moodboards / unverified share links → usually remove or skip
- Meta-skill packs that overlap a harness you already keep → prefer one primary
- Third animation library when Motion + GSAP already cover the stack → skip
- Hub pages when specific products are already cards → remove hub
- Unofficial WhatsApp gateways → skip unless you live in that automation (ToS risk)
- Niche GPU research OCR vs everyday PDF OCR → skip if Stirling (or similar) covers light use
- Paid QA SaaS replaceable by Sentry/Playwright → skip for this personal catalog
- One-off marketing toys (e.g. launch video skills) → skip
- DESIGN.md catalogs that overlap Taste / UI UX Pro Max / Awesome Design Skills → skip unless you actually use that CLI weekly
