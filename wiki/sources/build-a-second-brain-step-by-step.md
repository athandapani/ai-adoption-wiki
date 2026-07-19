---
title: "Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step"
source: raw/2026-07/Build a Second Brain - Karpathy's LLM Wiki Method, Step by Step.md
domain: [second-brain]
status: active
created: 2026-07-15
tags: [source, karpathy, llm-wiki, obsidian]
description: "Three-layer architecture (sources, wiki, schema) with four slash-command operations — capture, sync, lint, digest — and the 100-articles/400,000-words figure."
---

## TLDR
Three-layer architecture (sources, wiki, schema) with four slash-command operations — capture, sync, lint, digest — and the 100-articles/400,000-words figure.

## Metadata
- source: askglitch.com (Professor Glitch), published 2026-05-02 — playbook ref [^9]
- created: 2026-07-15
- category: llm-wiki methodology

## Source Link
[Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step](https://www.askglitch.com/blog/build-a-second-brain)

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[andrej-karpathy|Andrej Karpathy]]
- [[obsidian|Obsidian]]
- [[digital-second-brain|Digital Second Brain]]
- [[karpathy-llm-wiki-to-working-second-brain|From Karpathy's LLM Wiki to a Working Second Brain]]
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[andrej-karpathy|Andrej Karpathy]]

## Body

**Three layers:**
- **Sources** — raw, immutable documents the AI reads but never edits
- **Wiki** — AI-generated summaries, entity profiles, concepts, cross-references, actively
  maintained
- **Schema** — a `CLAUDE.md` specifying folder structure, naming conventions, workflows

**Four operations:** `/capture <url>` (ingest and update affected pages), `/sync` (reconcile
batches), `/lint` (broken links, contradictions, coverage gaps), `/digest` (weekly synthesis).

The reach claim: "Karpathy's vault...became a research artifact of around **100 articles and
400,000 words**, all written and maintained by the agent."

**This vault's own command structure descends from this shape** — `/jarvis-ingest` is `/capture` +
`/sync`, `/jarvis-lint` is `/lint`. See
[[wiki-schema-design-for-ai-adoption-wiki|the schema ADR]].

## Counter-arguments & Data Gaps

The **400,000 words** figure quietly refutes the method's own headline claim. If Karpathy's personal
research vault on a *single topic* is 400k words (~530k tokens), it does not fit in a 1M-token
context alongside a working query budget — and an enterprise wiki would be multiples larger. The
"no RAG needed, it all fits in context" premise fails at the scale of the exemplar used to sell it.

The `/lint` operation is listed and never specified. Across every Karpathy-method source here,
maintenance is the stage that gets one line: detect "broken links, contradictions, and coverage
gaps". Nobody describes how contradiction detection actually works, what it costs to run over a
large corpus, or what its false-positive rate is. It's the layer that determines whether the wiki
rots, and it's a bullet point.

Pseudonymous author; commentary on the gist rather than the gist.

## Notes
_(hand-written notes — preserved across re-ingestion)_
