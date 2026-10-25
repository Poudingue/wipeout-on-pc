# wipeout-on-pc

Docs-only index of open-source WipEout projects, published on GitHub Pages from `main`.

## Layout

- `README.md`: legend and index. `reimplementations.md`, `emulator-helpers.md`, `tools.md`: one table per category.
- The md tables are the source of truth. `index.html` fetches and parses them client-side.
- `.nojekyll` must stay: without it Pages runs Jekyll and the raw `.md` files are not served.

## Rules

- **Only useful files in git.** No interim scripts, scratch data, or tool output. One-off helpers (health checks, bulk table edits) live in `$LOCALAPPDATA/Temp/claude/`, never in the repo.
- Every table cell that carries a status starts with its emoji as the first character, or the `index.html` facets break.
- Changing a column or emoji means updating the README legend and the `index.html` tooltips in the same commit.
- Gaps and to-dos go in each category file's "Gaps" section. There is no BACKLOG.md.
- Check `index.html` over HTTP (`python -m http.server`), not `file://`, because `fetch` is blocked there.
- Quality (💎🥇🥈🥉🚧) is the primary quality verdict: an opinionated review of the code. Signals badges are individual facts, never a quality verdict on their own, and carry no aggregate grade.
- 🤖 marks AI-assisted repos (agent config files, AI co-author trailers, README statement). Absence means no evidence, not a guarantee.
