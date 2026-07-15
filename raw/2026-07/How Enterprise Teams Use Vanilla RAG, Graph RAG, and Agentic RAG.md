---
title: "How enterprise teams use Vanilla RAG, Graph RAG, and Agentic RAG to build knowledge bases that empower teams and drive ROI"
source: "https://www.linkedin.com/pulse/how-enterprise-teams-use-vanilla-rag-graph-agentic-build-sverdlik-xop9f"
author:
  - "[[Dmitry Sverdlik]]"
published: 2025-09-09
created: 2026-07-15
description: "Three RAG architectures compared — Vanilla, Graph, Agentic — with the 141%-over-3-years ROI figure."
playbook_ref: 30
capture_method: "webfetch-extract"
tags:
  - "clippings"
  - "rag"
  - "roi"
ingested: true
ingested_date: "2026-07-15"
---

> **Capture note:** structured extraction via WebFetch, not a verbatim clipping. Canonical text
> at the `source` URL.

# How enterprise teams use Vanilla RAG, Graph RAG, and Agentic RAG

**Author:** Dmitry Sverdlik
**Published:** 2025-09-09

## The three architectures

| Approach | Function | Use case |
|---|---|---|
| Vanilla RAG | "Like Google for internal documents" — direct semantic matching | Fact-based questions, rapid prototyping |
| Graph RAG | Maps relationships via knowledge graphs; handles inference across sources | Questions requiring contextual connections |
| Agentic RAG | "Full expert team: Each member is a specialist in their field" | Multiple specialized domains needing coordination |

## Real implementations cited

- Uber's Genie chatbot (Vanilla RAG): served "70,000+ questions with 48.9% helpfulness"
- BMW's multi-agent system: manages infrastructure across "1,300 applications"

## ROI (verbatim)

"Proper knowledge bases deliver 141% ROI within 3 years, translating to $1.5 million annually for
typical enterprises."

## Core argument

The real organizational challenge isn't selecting an LLM model; it's leveraging institutional
knowledge effectively. Strategic RAG selection — progressing from Vanilla to Graph to Agentic —
unlocks trapped expertise in documents and communications.

## Verification note

This confirms the playbook's "141% over 3 years" figure in Section 6.3, which had no visible
attribution there.

But note the **tension the playbook creates by citing this source at all**: Section 6.3 uses this
RAG-ROI figure to argue internal knowledge systems are under-invested, while Section 2.3 argues
RAG is the *wrong* architecture for mid-market and should be replaced by a compiled wiki. The
141% figure measures RAG knowledge bases, not Karpathy wikis. Uber's Genie — cited here as a
success — scores "48.9% helpfulness", which is not obviously a strong endorsement of anything.
