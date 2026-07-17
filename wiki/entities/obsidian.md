---
title: Obsidian
domain: [tooling]
status: active
created: 2026-07-15
tags: [entity, tool, markdown, graph, visualization]
description: "The markdown IDE that serves as the visualization layer for a Karpathy wiki — free, local, with backlinks and a graph view."
---

## TLDR
The markdown IDE that serves as the visualization layer for a Karpathy wiki — free, local, with backlinks and a graph view.

## Metadata
- created: 2026-07-15
- category: tool, software

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[km-tool-landscape|Knowledge Management Tool Landscape]]
- [[digital-second-brain|Digital Second Brain]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]]
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]]
- [[andrej-karpathy|Andrej Karpathy]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[km-tool-landscape|Knowledge Management Tool Landscape]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]

## Body

Obsidian is the recommended visualization layer in the playbook's Section 10.3 starter stack:
**free**, local-first, with backlinks and a graph view that makes a compiled wiki navigable.

Its role in the [[karpathy-llm-wiki-method|method]] is stage 3: compiled markdown opens as a
navigable knowledge graph; backlinks show which pages reference each concept. Ref [^42] is blunt
about how optional it is — "Obsidian recommended, but VS Code, Notepad, anything works" — which is
the point. The wiki is plain markdown files; the IDE is interchangeable.

The playbook's recommended toolchain around it: Claude via API or Claude Code for file access;
Obsidian Web Clipper for capture; Git on the wiki directory for history and rollback; a monthly
LLM-powered linting pass.

**This vault is itself an Obsidian vault** — see
[[wiki-schema-design-for-ai-adoption-wiki|the schema ADR]] for how its `.obsidian/` placement at the
`GitFiles` root creates a shared graph with a sibling repo, and the slug-collision constraint that
follows.

## Counter-arguments & Data Gaps

Obsidian's graph view is famously more decorative than useful past a few hundred nodes — it
degrades into a hairball without deliberate filtering, and "look at the pretty graph" is a known
PKM failure mode that produces engagement rather than insight.

For enterprise use the harder gap is **permissions**. Obsidian is a local markdown editor with no
access-control model. Ref [^41] insists AI knowledge tools must "honor existing access controls",
and the playbook's own Section 12.2 lists permission-respect as a critical success factor — a
shared Obsidian vault has no mechanism for it. That's not a criticism of Obsidian, which was built
for individuals; it's a gap in the playbook's recommendation to use it as an enterprise layer.

Git-on-the-wiki also gives history and rollback but no review gate, no branching model for
contested edits, and no merge strategy for a directory an LLM rewrites wholesale.

## Notes
_(hand-written notes — preserved across re-ingestion)_
