---
title: Karpathy LLM Wiki Method
domain: [second-brain]
status: active
created: 2026-07-15
tags: [second-brain, llm-wiki, karpathy, architecture]
---

## TLDR
A six-stage pipeline where the LLM reads raw sources once and compiles a structured markdown wiki it then maintains — the human curates and reads, the LLM writes.

## Metadata
- source: playbook Section 2.2, refs [^6] [^8] [^9] [^42]
- created: 2026-07-15
- category: second-brain, architecture

## Related
- [[digital-second-brain|Digital Second Brain]] — depends-on
- [[andrej-karpathy|Andrej Karpathy]]
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]] — the contested comparison
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]] — contradicts (scopes the method to individuals and small teams)
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]]
- [[karpathy-llm-wiki-to-working-second-brain|From Karpathy's LLM Wiki to a Working Second Brain]]
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]]
- [[obsidian|Obsidian]]
- [[three-layer-reference-architecture|Three-Layer Reference Architecture]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]

## Referenced By
- [[digital-second-brain|Digital Second Brain]]
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[three-layer-reference-architecture|Three-Layer Reference Architecture]]

## Body

Karpathy's own framing of the division of labour:

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about
> what it all means. The LLM's job is everything else."

The six-stage pipeline:

1. **`raw/` — ingestion.** A flat directory where sources land in any format. No pre-processing.
   *Capture first, organize later.*
2. **Compilation.** The LLM reads all raw sources and generates structured markdown: summaries,
   entity pages, concept pages, cross-references. The human reads the wiki; the LLM writes it.
3. **`wiki/` — visualization.** Compiled markdown opens in Obsidian as a navigable graph;
   backlinks show which pages reference each concept.
4. **Q&A against the wiki.** Natural language questions instead of keyword search. If the wiki
   fits the context window, no RAG is required — *perfect recall*.
5. **Output filing — the learning loop.** New insights get filed back in, so every interaction
   expands the base.
6. **Linting & health checks.** Automated detection of broken links, orphans, stale claims, and
   contradictions — CI/CD for knowledge.

Reported result: **~100 articles, ~400,000 words** on a single research topic, written and
maintained entirely by the agent. "No database. No embeddings. No vector store. Just folders and
text files."

The enterprise adaptation the playbook proposes: maintain separate wikis per domain (engineering,
sales, operations, compliance), then concatenate them for cross-domain queries.

## Counter-arguments & Data Gaps

**The primary source is missing.** Karpathy's gist is never cited in the playbook. Every claim here
traces to secondary commentary — refs [^6], [^8], [^9], and a Facebook group post [^42]. The
playbook's Appendix B recommends ingesting the gist as the "Original architecture specification"
while never having done so itself. The "17 million views" claim has no source at all; the only
reference reporting gist metrics says "5,000+ stars, 1,400+ forks".

**The method's own advocate scopes it smaller than the playbook does.** Ref [^6] says it "scales
effectively for individuals and small teams" and that "organizational collections require
traditional RAG systems". The playbook's central prescription contradicts its primary source
without acknowledging it.

**The context-window premise is load-bearing and undefended.** "If the wiki fits in the model's
context window, no RAG is required" is true and unhelpful — the question is whether an
*enterprise* wiki fits. Karpathy's own artifact is ~400k words, which does not fit in 1M tokens
alongside a working query budget. The domain-partitioning workaround ("concatenate wikis for
cross-domain queries") reintroduces exactly the retrieval problem it claims to eliminate, and no
source describes how partitions get chosen or maintained.

**The economics are unexamined.** Recompiling a wiki means re-reading every source. That's linear
in corpus size per compilation, versus incremental re-indexing for RAG. Dima Kramskoy's honest
practitioner assessment — "7/10", 15+ pages in the first week — is the only real-use datapoint in
the corpus, and it's a personal vault.

## Notes
_(hand-written notes — preserved across re-ingestion)_
