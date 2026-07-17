---
title: Wiki Schema Design for ai-adoption-wiki
domain: [cross-domain]
status: active
created: 2026-07-15
tags: [meta, schema, adr, graph]
description: "This vault inherits second-brain's seven-heading page template unchanged and deviates on exactly two axes — status vocabulary and domain vocabulary — both forced by its purpose as a published graph demo rather than a private notebook."
---

## TLDR
This vault inherits second-brain's seven-heading page template unchanged and deviates on exactly two axes — status vocabulary and domain vocabulary — both forced by its purpose as a published graph demo rather than a private notebook.

## Metadata
- source: derived from second-brain/.claude/commands/jarvis-ingest.md and wiki-graph-explorer's parser
- created: 2026-07-15
- category: schema, architectural decision record

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[obsidian|Obsidian]] — the visualization layer
- [[digital-second-brain|Digital Second Brain]]
- [[three-layer-reference-architecture|Three-Layer Reference Architecture]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]] — why the counter-arguments heading is mandatory here
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]]
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]

## Body

An ADR for this repo, mirroring how `second-brain` documents its own schema decisions.

**Inherited unchanged from `second-brain`.** The seven H2 sections in fixed order (TLDR,
Metadata, Related, Referenced By, Body, Counter-arguments & Data Gaps, Notes); kebab-case
filenames slugged from titles; globally unique titles across folders; piped wikilinks
`[[slug|Display Title]]`; no H1, title in frontmatter; relation hints as freeform trailing text;
`domain` as a cross-cutting frontmatter tag rather than a folder; `raw/<YYYY-MM>/` archiving by
ingestion month. Four folders: `sources/`, `entities/`, `concepts/`, `synthesis/` — `people/` is
dropped, since this vault has no personal content.

**Deviation 1 — `status: active | revisiting | dormant`**, replacing `current | superseded`.

Forced by the consumer. `wiki-graph-explorer`'s `StatusDot` colors only `active` (green) and
`revisiting` (amber); anything else renders neutral gray. `second-brain`'s vocabulary would make
every node in the demo gray, discarding a free signal. Since this vault exists to be looked at,
the renderer's vocabulary wins.

The mapping earns its keep here: `active` = well-sourced and current; `revisiting` = thin,
contested, or a stale-dated claim; `dormant` = superseded or historical. Given what verification
turned up, `revisiting` is doing real work — it marks the pages where the playbook's citation
didn't survive contact with its source.

**Deviation 2 — domain vocabulary.** `second-brain`'s `career / health / travel / education /
investments` is meaningless for research on AI adoption. Replaced with `adoption`, `second-brain`,
`governance`, `spend`, `change-management`, `risk`, `tooling`, `industry`, `cross-domain`. Same
mechanism, different values.

**Constraints the parser imposes** (documented because violating them fails *silently*):
frontmatter must carry `title`/`tags`/`status` or the page is skipped entirely; wikilinks count
only inside `## Related` and `## Referenced By`, so a link in `## Body` is invisible to the graph;
node ID is the filename, not the title; dangling links are dropped with no error. That last one is
why this vault's node registry was frozen before any page was written — closure can't be checked
after the fact from the graph output, because missing edges leave no trace.

**Rejected: adding a frontmatter field for demo color.** Would have preserved `current`/
`superseded` and added a separate freshness key, but it required a parser change in
`wiki-graph-explorer` to read a field only this vault emits. Not worth coupling the tool to one
vault's schema.

**Collision avoidance.** `.obsidian/` sits at the `GitFiles` root, so this vault and `second-brain`
share one Obsidian graph and `[[slug]]` resolves vault-wide. Two slugs were renamed to avoid
silent cross-linking: `karpathy-llm-wiki-method` (theirs: `llm-wiki-pattern`) and this page
(theirs: `wiki-schema-design-for-second-brain`).

## Counter-arguments & Data Gaps

The strongest objection is that Deviation 1 is tail-wagging-dog: the schema now encodes a
rendering detail of one downstream tool, and if `StatusDot` ever learns `current`/`superseded`,
this vault is the odd one out for no reason. A defensible alternative was to fix the tool rather
than bend the vault.

The counter is that `active`/`revisiting`/`dormant` is a *better* vocabulary independent of the
renderer — it describes content freshness, which is what a research vault of dated statistics
actually needs, where `current`/`superseded` describes document lineage, which suits `second-brain`'s
resume-and-journal content. The two vaults want different things; the renderer just surfaced it.

Unresolved: the two vaults now disagree on a core frontmatter key while sharing an Obsidian graph.
Any future Dataview query spanning both will need to handle both vocabularies.

## Notes
_(hand-written notes — preserved across re-ingestion)_
