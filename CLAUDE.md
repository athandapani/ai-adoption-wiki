# ai-adoption-wiki — repo-wide guidance

This repo is a **public** LLM wiki (Karpathy pattern): `raw/` sources get compiled into a
maintained `wiki/` by an LLM, confirmed by a human before anything is written. The wiki schema
and workflows live in `.claude/commands/*.md`, not here — this file stays general.

It is a sibling of, and follows the conventions of, the private `second-brain` repo. The two
deliberate schema deviations are recorded below and in
`wiki/synthesis/wiki-schema-design-for-ai-adoption-wiki.md`.

Subject matter: AI adoption in mid-market enterprises ($50M–$500M ARR), compiled from
*The Digital Second Brain Playbook* and its 43 cited sources.

## Purpose

Unlike `second-brain`, this vault exists to be **published**. It is the public demo vault for
the sibling `wiki-graph-explorer` tool:

```bash
cd ../wiki-graph-explorer
npm run build:graph -- --vault ../ai-adoption-wiki/wiki --out local-build
npm run dev     # http://localhost:3000/graph
```

Everything here is compiled from public sources. No private or personal content ever lands in
this repo — that is what `second-brain` is for, and it is hard-blocked from publication by
`wiki-graph-explorer/lib/second-brain-path-check.ts`.

## Coding discipline (Karpathy's four principles)

1. **Think Before Coding** — surface assumptions and ambiguity before implementing anything.
2. **Simplicity First** — minimum change that solves the problem. Nothing speculative, no
   features beyond what was asked.
3. **Surgical Changes** — minimal diffs, no speculative abstractions, match existing
   conventions, clean up anything orphaned.
4. **Goal-Driven Execution** — work toward verifiable success criteria; caution over speed.
   Nothing gets called done without proof it actually works.

## Hard rules

- Raw file **content** is never modified. The only sanctioned write to `raw/` is
  `/jarvis-ingest` tagging processed files (`ingested:`/`ingested_date:` frontmatter) and
  relocating them into `<YYYY-MM>/` subfolders.
- Nothing is written to `wiki/` without the human confirming first ("separate vaults" —
  curated wiki vs. speculative agent writes stay trustworthy because that line is never
  crossed unreviewed).
- **Nothing private, personal, or `second-brain`-derived is ever committed here.** This vault
  is published.
- Pages report what a source **claims**, attributed. They do not assert contested figures as
  ground truth. Many playbook statistics are 2026-dated and unverifiable — attribute, don't
  launder.

## Schema constraints imposed by the graph explorer

These are not style preferences. `wiki-graph-explorer` parses this vault, and violating any of
these **silently** drops a node or an edge — no error is raised.

- **YAML frontmatter is mandatory**, and must carry `title`, `tags`, `status`. A page without
  parseable frontmatter is skipped entirely.
- **Wikilinks only count inside `## Related` and `## Referenced By`.** A link in `## Body` is
  invisible to the graph. The heading must be exactly that — H2, case-sensitive, nothing else
  on the line.
- **Node ID is the filename** minus `.md`, not the title. Wikilink targets must match
  filenames, and filenames must be globally unique across all folders.
- **Dangling links are dropped silently.** Every `[[target]]` must resolve to a real file.
- Edges are undirected and deduped — `Related` and `Referenced By` are equivalent to the
  parser. Keep both honest anyway, for Obsidian backlinks and human readers.

## Deviations from `second-brain`'s schema

1. **`status:` is `active` / `revisiting` / `dormant`** (not `current` / `superseded`).
   The explorer's `StatusDot` only colors `active` (green) and `revisiting` (amber);
   everything else renders neutral gray. Mapping: `active` = well-sourced and current;
   `revisiting` = thin, contested, or a stale-dated claim; `dormant` = superseded or
   historical.
2. **`domain:` vocabulary is subject-appropriate**: `adoption`, `second-brain`, `governance`,
   `spend`, `change-management`, `risk`, `tooling`, `industry`, `cross-domain`. Still a
   cross-cutting frontmatter tag, never a folder.

## Obsidian note

`.obsidian/` lives at the **`GitFiles` root**, one level up — so this vault and `second-brain`
share a single Obsidian graph, and Obsidian resolves `[[slug]]` vault-wide. Slugs here must
not collide with `second-brain`'s pages or the two vaults will silently cross-link. Notably
`llm-wiki-pattern` and `wiki-schema-design-for-second-brain` are already taken there; this
repo uses `karpathy-llm-wiki-method` and `wiki-schema-design-for-ai-adoption-wiki`.

This does not affect `wiki-graph-explorer`, which walks one vault path only.
