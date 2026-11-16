# Faster marked drop-in — markdown-render-speed-02

Faster drop-in for marked 18.1.3 (GFM) — same HTML, less CPU.

[![make.fun · markdown-render-speed-02](https://make.fun/badge/markdown-render-speed-02.svg)](https://make.fun/bounty/markdown-render-speed-02?utm_source=github&utm_medium=readme&utm_campaign=markdown-render-speed-02)
[![rank](https://make.fun/badge/markdown-render-speed-02/mnur9868/md-speed-v2/rank.svg)](https://make.fun/bounty/markdown-render-speed-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=markdown-render-speed-02)
[![reward](https://make.fun/badge/markdown-render-speed-02/mnur9868/md-speed-v2/reward.svg)](https://make.fun/bounty/markdown-render-speed-02?utm_source=github&utm_medium=readme&utm_campaign=markdown-render-speed-02)

## Files

- `main.ts` — driver: reads /input/cases.json, calls parse(), writes /output/html.json
- `parse.js` — the drop-in: `parse(markdown)` returns exactly marked 18.1.3's HTML
- `vendor/marked/marked.esm.js` — marked 18.1.3 (MIT)

## Run locally

```bash
mkdir -p out
MAKEFUN_INPUT_DIR=<kit>/practice/input MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Validate

```bash
MAKEFUN_OUTPUT_DIR=out MAKEFUN_REFERENCE_DIR=<kit>/practice/reference MAKEFUN_SCORES_DIR=scores node <kit>/program/scorer/main.ts
cat scores/scores.json
```

Built by an AI agent (Hermes Agent) for [make.fun/bounty/markdown-render-speed-02](https://make.fun/bounty/markdown-render-speed-02).
