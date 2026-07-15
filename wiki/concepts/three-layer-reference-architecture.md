---
title: Three-Layer Reference Architecture
domain: [second-brain]
status: active
created: 2026-07-15
tags: [architecture, second-brain, reference-architecture]
---

## TLDR
Knowledge sources at the bottom, knowledge intelligence in the middle, AI interaction on top — the playbook's reference design for a mid-market Digital Second Brain.

## Metadata
- source: playbook Section 12.1
- created: 2026-07-15
- category: second-brain, architecture

## Related
- [[digital-second-brain|Digital Second Brain]] — depends-on
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]]
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[data-quality-readiness|Data Quality and Infrastructure Readiness]]
- [[km-tool-landscape|Knowledge Management Tool Landscape]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[ai-in-traditional-industries|AI in Traditional Industries]]

## Referenced By
- [[digital-second-brain|Digital Second Brain]]
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[data-quality-readiness|Data Quality and Infrastructure Readiness]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]

## Body

```
LAYER 3: AI INTERACTION (what users experience)
├── Natural language Q&A (Slack bot / intranet chatbot)
├── Proactive alerts ("This process changed last month")
└── Expert finder ("Who knows most about X, per the knowledge graph?")

LAYER 2: KNOWLEDGE INTELLIGENCE (where AI works)
├── LLM Wiki (Karpathy architecture): domain-specific compiled markdown
├── Vector index for RAG fallback on large corpus segments
├── Graph of entity relationships (people, products, customers, projects)
└── Scheduled compilation runs (weekly: new sources → wiki updates)

LAYER 1: KNOWLEDGE SOURCES (what gets ingested)
├── Documentation: Confluence, SharePoint, Notion, Google Docs
├── Communication: Slack channels (filtered), meeting transcripts
├── Operational: ERP/SAP exports, CRM data, project management (Jira)
├── Human capture: exit interviews, expert sessions, decision logs
└── External: industry reports, regulatory documents, supplier documentation
```

**Layer 2 quietly concedes the architecture argument.** It contains both "LLM Wiki (Karpathy
architecture)" *and* "Vector index for RAG fallback on large corpus segments". That's the hybrid
this vault argues for at [[rag-vs-llm-wiki|RAG vs. LLM Wiki]] — compiled wiki as the primary
surface, retrieval underneath for what won't fit. The reference architecture is more honest than
Section 2.3's rhetoric, which spends four paragraphs explaining why RAG is the wrong choice for
mid-market.

**Layer 1's "Human capture" row is the one most likely to be skipped and most likely to matter.**
Exit interviews, expert sessions, and decision logs are the only source of the tribal knowledge
that [[knowledge-attrition-cost|walks out the door]]. Every other row is a system export — already
written down, already available. This row is the actual work.

## Counter-arguments & Data Gaps

**Layer 3 is aspirational.** "Expert finder" and "proactive alerts" describe capabilities no source
in this corpus documents anyone shipping. Proactive alerting on process changes requires detecting
that something changed and knowing who cares — an unsolved problem, presented here as a bullet.

**"Scheduled compilation runs (weekly)" hides the cost model.** Recompiling means re-reading the
corpus. Weekly recompilation of an enterprise wiki is linear in corpus size, every week, forever —
against incremental re-indexing for RAG. Nobody in this corpus has costed it, and the playbook's
own "$20–50K/year in LLM API costs" estimate is for a personal-scale DIY vault.

**Permissioning is missing entirely.** Ref [^41] is explicit that "AI search and synthesis must
honor existing access controls", and the playbook's own Section 12.2 lists permission-respect as a
critical success factor — but no layer here carries an access-control boundary. A Layer 3 expert
finder over Layer 1 HR exports and Slack is a compliance incident waiting to happen.

This diagram is the playbook's own; no source proposes it.

## Notes
_(hand-written notes — preserved across re-ingestion)_
