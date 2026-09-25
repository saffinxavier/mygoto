# MyGoTo agent guidance

- Read `OBJECTIVES.md` when changing catalog data, prompts, or UI behavior; it is the standing brief.
- Keep catalog entries in the `index.html` `entries` array. Each entry needs accurate, plain-English `codexHow` and `cursorHow` guidance.
- Check assistant-specific setup before recommending an install command. Use `codexInstallHint` when the shared command is Cursor-only, or `null` when no Codex command is verified.
- Keep the app static and lightweight, with no framework or build step.
