---
title: Retrieval-Augmented Generation (RAG)
domain: [second-brain]
status: active
created: 2026-07-15
tags: [rag, architecture, grounding]
description: "An architecture where the LLM retrieves relevant chunks from an index at query time before generating — the industry default for enterprise knowledge, and the primary hallucination control."
---

## TLDR
An architecture where the LLM retrieves relevant chunks from an index at query time before generating — the industry default for enterprise knowledge, and the primary hallucination control.

## Metadata
- source: playbook Appendix A, Sections 2.3, 9.2
- created: 2026-07-15
- category: second-brain, architecture

## Related
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]] — contradicts
- [[vanilla-graph-agentic-rag|How Enterprise Teams Use Vanilla, Graph, and Agentic RAG]] — depends-on
- [[rag-knowledge-management-roi|RAG Knowledge Management — 300-500% ROI]]
- [[turning-institutional-knowledge-into-ai-assets|Turning Institutional Knowledge into Strategic AI Assets]]
- [[from-information-silos-to-enterprise-brain|From Information Silos to Enterprise Brain]]
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[ai-hallucination-risk|AI Hallucination Risk]]
- [[digital-second-brain|Digital Second Brain]]
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[internal-knowledge-is-under-invested|Internal Knowledge Is Systematically Under-Invested]]

## Referenced By
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]]
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[digital-second-brain|Digital Second Brain]]
- [[capture-first-beats-search-first|Capture First, Search Second]]

## Body

RAG retrieves relevant chunks from a vector index at query time and passes them to the model as
context. It is the dominant enterprise pattern for grounding AI answers in organizational data,
and it does double duty: it's both a knowledge-access architecture and the main structural defense
against [[ai-hallucination-risk|hallucination]].

Dmitry Sverdlik's maturity path is the most useful framing in the corpus:

| Approach | Function | Use case |
|---|---|---|
| **Vanilla RAG** | "Like Google for internal documents" — direct semantic matching | Fact-based questions, rapid prototyping |
| **Graph RAG** | Maps relationships via knowledge graphs; inference across sources | Questions needing contextual connections |
| **Agentic RAG** | "Full expert team: Each member is a specialist in their field" | Multiple domains needing coordination |

Start Vanilla to validate, upgrade to Graph when contextual analysis becomes strategic, go Agentic
for multi-domain complexity.

The reported returns are the ones the playbook leans on throughout: 300–500% first-year ROI
(Stratechi), 312% in six months (10xclaw), 141% over three years (Sverdlik), 40–60% reductions in
query resolution time (Netsolutions).

## Counter-arguments & Data Gaps

The ROI figures are the weakest-sourced numbers in the corpus — a consultancy marketing page, an
undated anonymous case study, and a LinkedIn post, none with methodology. Treat them as directional
claims by interested parties, not measurements.

The grounding promise is also oversold. SID Global Solutions reports that **RAG-grounded legal
research tools still hallucinate 17–33% of the time on benchmark queries**. Retrieval reduces
fabrication; it does not eliminate it, and the confidence RAG buys can make the residual errors
harder to catch.

Sverdlik's own showcase example undercuts the enthusiasm: Uber's Genie served "70,000+ questions
with 48.9% helpfulness". That's the success story.

The playbook's structural criticism has force — retrieval quality does depend on chunking, and
nobody in this corpus reports a principled way to tune it. But the playbook cites RAG's ROI to
argue for a non-RAG architecture, which is the incoherence documented at
[[rag-vs-llm-wiki|RAG vs. LLM Wiki]].

## Notes
_(hand-written notes — preserved across re-ingestion)_
