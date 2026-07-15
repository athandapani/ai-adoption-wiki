---
title: RAG vs. LLM Wiki
domain: [second-brain]
status: revisiting
created: 2026-07-15
tags: [rag, llm-wiki, architecture, contested]
---

## TLDR
"RAG retrieves. A wiki compounds." — the playbook's central architectural claim, which its own primary source contradicts and which no enterprise deployment in the corpus tests.

## Metadata
- source: playbook Sections 2.2, 2.3
- created: 2026-07-15
- category: second-brain, contested architecture

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]] — contradicts
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]] — contradicts (says organizational collections require RAG)
- [[vanilla-graph-agentic-rag|How Enterprise Teams Use Vanilla, Graph, and Agentic RAG]] — contradicts (RAG maturity path)
- [[rag-knowledge-management-roi|RAG Knowledge Management — 300-500% ROI]]
- [[digital-second-brain|Digital Second Brain]]
- [[karpathy-llm-wiki-to-working-second-brain|From Karpathy's LLM Wiki to a Working Second Brain]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]
- [[internal-knowledge-is-under-invested|Internal Knowledge Is Systematically Under-Invested]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[digital-second-brain|Digital Second Brain]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]

## Body

The playbook's case: traditional RAG chunks and embeds raw documents as-is, so retrieval quality
depends on how well chunks represent the original — and at enterprise scale this "degrades rapidly
as the corpus grows past a few hundred documents". Compilation eliminates the failure mode because
the LLM has already read everything and restructured it into a consistent format. **"The compiled
wiki is already optimized for LLM consumption."**

For a lean IT team, the claimed operational wins are real if the premise holds: no vector database
to maintain, no embedding pipelines, no chunk-size tuning, and updates mean re-running a
compilation prompt rather than re-indexing.

**The problem is that this is the playbook's least-supported major claim, and it's the thesis.**

- Its **own primary source** (ref [^6]) says the method "scales effectively for individuals and
  small teams" and that "organizational collections require traditional RAG systems". That is the
  precise opposite of the playbook's conclusion, in the source it cites for the method.
- Ref [^30] describes a **RAG maturity path** — Vanilla → Graph → Agentic — as the enterprise
  answer, and supplies the 141% ROI figure the playbook uses in Section 6.3.
- Every ROI number the playbook cites to argue knowledge systems are under-invested (300–500%,
  312%, 141%) measures **RAG deployments**, not compiled wikis. The evidence supports the
  architecture it argues against.
- The "degrades past a few hundred documents" claim has no citation anywhere.

## Counter-arguments & Data Gaps

The strongest case *for* the wiki approach isn't in the playbook: it's that compilation and
retrieval aren't actually rivals. A compiled wiki is a better *corpus* — deduplicated, structured,
contradiction-flagged. RAG over a compiled wiki should beat RAG over raw documents, which makes
this a preprocessing decision rather than an either/or. The playbook forces a dichotomy that the
technology doesn't require, and in doing so has to argue against the evidence it needs.

The strongest case *against*: compilation is lossy by construction. The LLM decides what mattered
at compile time, and a question nobody anticipated is answered from a summary rather than the
source. RAG's much-criticized chunking at least preserves the original text. For compliance and
audit use — where the playbook itself insists on citation-first grounding — losing the primary text
is a serious cost.

What would change this: a head-to-head evaluation on an enterprise corpus, measuring answer
quality and total cost for compiled-wiki vs. RAG vs. RAG-over-compiled-wiki. Nothing in these 43
sources attempts it. Status stays `revisiting` until something does.

## Notes
_(hand-written notes — preserved across re-ingestion)_
