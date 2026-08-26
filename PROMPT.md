# MyGoTo — Cursor project picker prompt

Paste the block below into **any** Cursor project chat when you want recommendations from your personal catalog.

**Live catalog:** https://saffinxavier.github.io/mygoto/  
**Repo:** https://github.com/saffinxavier/mygoto  

You can also click **Copy project prompt** on the catalog page.

---

```text
You are helping me set up THIS Cursor project using my personal MyGoTo catalog.

Catalog (live): https://saffinxavier.github.io/mygoto/
Fallback: https://github.com/saffinxavier/mygoto (open index.html) or local MyGoTo repo.

Do this:
1. Inspect this repo (README, package manifests, scripts, main folders, stack).
2. From the MyGoTo catalog, recommend ONLY 3–7 items that fit THIS project. Do not dump the whole catalog.
3. For each pick, give: name, category, why it fits here, exact Cursor how-to (from the card’s Cursor / Install fields), and when to skip.
4. Prefer: skills for agent workflow, tools/ui-kits for code deps, guidelines for UI audits. Skip unrelated platforms.
5. End with a short install order I can run in the terminal / Cursor Agent.

Keep answers short and action-first.
```

---

## How to use

1. Open the target project in Cursor.
2. Paste the prompt (or use the catalog Copy button).
3. Optionally add one line: what you are building this week.
4. Install only the 3–7 picks the agent recommends.
