# ai-adoption-wiki

A public LLM wiki on **AI adoption in mid-market enterprises** ($50M–$500M ARR), built with the
Karpathy pattern: raw sources in `raw/`, compiled by an LLM into a maintained, cross-linked
`wiki/`.

Obsidian is the IDE. The LLM is the programmer. The wiki is the codebase.

## Why this exists

Two reasons:

1. **It's a real knowledge base** on a real question — how mid-market firms ($50M–$500M ARR,
   lean IT, no AI team) actually adopt AI, and why a Digital Second Brain is the highest-leverage
   investment available to them.
2. **It's the public demo vault** for the sibling [`wiki-graph-explorer`](../wiki-graph-explorer)
   tool, which turns a Karpathy-pattern wiki's backlink structure into a clickable
   force-directed graph. That tool's private dogfooding vault (`second-brain`) can never be
   published; this one is built to be.

## Source

Compiled from *AI Adoption in Mid-Market Enterprises: The Digital Second Brain Playbook* plus
the 43 sources it cites — OECD, BCG, Gartner, McKinsey, Forrester, NIST, WEF, and others. Every
source was fetched and archived into `raw/2026-07/` before compilation.

## Layout

- `raw/` — source materials, archived into `<YYYY-MM>/` by ingestion month. The LLM reads,
  never rewrites.
- `wiki/sources/`, `wiki/entities/`, `wiki/concepts/`, `wiki/synthesis/` — the LLM-maintained
  wiki, organized by content type. `domain` (adoption / second-brain / governance / spend /
  change-management / risk / tooling / industry / cross-domain) is a frontmatter tag that cuts
  across these folders, not a folder itself.
- `index.md` — catalog of every page, one TLDR line each.
- `log.md` — append-only record of every ingest/lint operation.

## Viewing the graph

```bash
cd ../wiki-graph-explorer
npm install
npm run build:graph -- --vault ../ai-adoption-wiki/wiki --out local-build
npm run dev     # http://localhost:3000/graph
```

Or just open `GitFiles/` as an Obsidian vault and use the built-in graph view.

## Workflow

- `/jarvis-ingest` — compile new `raw/` sources into `wiki/` pages, with a confirm step before
  anything is written.
- `/jarvis-lint` — report-only health check: contradictions, stale claims, orphan pages,
  missing-article candidates.

## A note on the numbers

The playbook is dated 2026 and cites figures that are, in several cases, unverifiable against
primary sources. Pages here report what each source **claims**, with attribution. Where sources
disagree — and they do, notably on whether RAG or a compiled wiki is the right architecture, and
on whether enterprise AI spending is producing returns — the tension is preserved in each page's
`## Counter-arguments & Data Gaps` section rather than resolved away.
