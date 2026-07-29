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
these **silently** drops a node or an edge — no error is raised. (Updated for the generalized
parser shipped in `wiki-graph-explorer` Epic 0utMknV — see that repo's
`docs/design-notes.md` §12–14 for the full rationale.)

- **YAML frontmatter is mandatory**, and must carry `title` and `tags`. A page without
  parseable frontmatter is skipped entirely. `status` is now optional — an absent `status`
  defaults to a neutral `"unknown"` rather than dropping the page, but this vault should keep
  declaring `active`/`revisiting`/`dormant` explicitly since the `StatusDot` coloring depends on it.
- **Wikilinks count anywhere in the page body**, not only inside `## Related` and
  `## Referenced By` — the parser now does a full-body scan. Keep using those two H2 sections
  for structural cross-referencing anyway (Obsidian backlinks, human readers, this vault's own
  editorial convention), but a `[[link]]` mentioned in ordinary prose is no longer invisible to
  the graph.
- **`![[Page Name]]` embed/transclusion syntax is excluded** from graph edges — only bare
  `[[wikilinks]]` count.
- **Wikilink targets resolve case-insensitively against either the target's filename or its
  frontmatter `title`**, regardless of folder — not exact-filename-only. If two pages share a
  title, an ambiguous `[[link]]` resolves to whichever one the vault walk encounters first
  (deterministic across runs, but not something to rely on) — keep titles globally unique in
  practice to avoid this tie-break mattering.
- **Node ID is still the filename** minus `.md`, not the title, and filenames must still be
  globally unique across all folders.
- **Dangling links are dropped silently**, logged at DEBUG level only (not a build warning or
  error) — every `[[target]]` should still resolve to a real file or frontmatter title for
  intentional cross-references.
- Edges are undirected and deduped — `Related` and `Referenced By` are equivalent to the
  parser. Keep both honest anyway, for Obsidian backlinks and human readers.
- `tags` may be a YAML array, a comma/space-separated string, or omitted with inline `#hashtag`s
  in the body merged in — this vault should keep using a YAML array for consistency, but the
  parser accepts all three shapes.

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
