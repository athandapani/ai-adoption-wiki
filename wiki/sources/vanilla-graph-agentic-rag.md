---
title: "How Enterprise Teams Use Vanilla, Graph, and Agentic RAG"
source: raw/2026-07/How Enterprise Teams Use Vanilla RAG, Graph RAG, and Agentic RAG.md
domain: [second-brain, spend]
status: active
created: 2026-07-15
tags: [source, rag, architecture, roi]
description: "The RAG maturity path — Vanilla → Graph → Agentic — and the source of the 141%-over-3-years figure the playbook uses to argue against RAG."
---

## TLDR
The RAG maturity path — Vanilla → Graph → Agentic — and the source of the 141%-over-3-years figure the playbook uses to argue against RAG.

## Metadata
- source: linkedin.com (Dmitry Sverdlik), published 2025-09-09 — playbook ref [^30]
- created: 2026-07-15
- category: rag, architecture

## Source Link
[How enterprise teams use Vanilla RAG, Graph RAG, and Agentic RAG to build knowledge bases that empower teams and drive ROI](https://www.linkedin.com/pulse/how-enterprise-teams-use-vanilla-rag-graph-agentic-build-sverdlik-xop9f)

## Related
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]] — depends-on
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]] — contradicts (this is the RAG-maturity answer)
- [[internal-knowledge-is-under-invested|Internal Knowledge Is Systematically Under-Invested]]
- [[ai-budget-allocation|Where the AI Budget Goes]]
- [[rag-knowledge-management-roi|RAG Knowledge Management — 300-500% ROI]]
- [[from-information-silos-to-enterprise-brain|From Information Silos to Enterprise Brain]]
- [[roi-measurement-problem|The ROI Measurement Problem]]

## Referenced By
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]]
- [[internal-knowledge-is-under-invested|Internal Knowledge Is Systematically Under-Invested]]
- [[ai-budget-allocation|Where the AI Budget Goes]]

## Body

**Author:** Dmitry Sverdlik.

| Approach | Function | Use case |
|---|---|---|
| Vanilla RAG | "Like Google for internal documents" | Fact-based questions, prototyping |
| Graph RAG | Relationship mapping via knowledge graphs | Contextual connections across sources |
| Agentic RAG | "Full expert team: Each member is a specialist" | Multi-domain coordination |

Real deployments: Uber's Genie (Vanilla RAG) served "70,000+ questions with 48.9% helpfulness";
BMW's multi-agent system manages "1,300 applications".

**ROI:** "Proper knowledge bases deliver **141% ROI within 3 years**, translating to $1.5 million
annually for typical enterprises."

Strategy: start Vanilla, upgrade to Graph when contextual analysis becomes strategic, go Agentic
for multi-domain complexity.

## Counter-arguments & Data Gaps

**This source supplies the 141% figure the playbook's Section 6.3 uses to argue internal knowledge
is under-invested — and it measures RAG, the architecture Section 2.3 argues against.** The playbook
cites RAG's returns as evidence for replacing RAG. See [[rag-vs-llm-wiki|RAG vs. LLM Wiki]].

It also proposes the direct alternative to the playbook's thesis: a **RAG maturity path** rather
than a compiled wiki. The playbook cites it once, for a number, and never engages the argument.

The showcase example undercuts the enthusiasm: **48.9% helpfulness** on 70,000+ questions is
presented as a success. The 141% ROI and "$1.5 million annually for typical enterprises" figures
have no methodology, and "typical enterprise" is undefined.

A LinkedIn post from September 2025, by a founder in the knowledge-base tooling space.

## Notes
_(hand-written notes — preserved across re-ingestion)_
