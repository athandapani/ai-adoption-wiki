---
title: Data Quality and Infrastructure Readiness
domain: [adoption]
status: active
created: 2026-07-15
tags: [data-quality, readiness, infrastructure]
---

## TLDR
The most common AI failure mode isn't picking the wrong tool — it's starting with data that isn't ready, and the Karpathy approach tolerates messy formats without fixing knowledge that was never captured.

## Metadata
- source: playbook Section 3.1, refs [^12] [^1]
- created: 2026-07-15
- category: adoption, readiness

## Related
- [[g7-ai-adoption-by-smes|AI Adoption by SMEs (G7 Report, Mila)]] — depends-on
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[ai-adoption-barriers|Barriers to AI Adoption]]
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[digital-second-brain|Digital Second Brain]]
- [[capability-ambition-gap|Capability-Ambition Gap]]
- [[why-businesses-struggled-with-ai-2024|Why Businesses Struggled with AI in 2024]]
- [[ai-in-traditional-industries|AI in Traditional Industries]]

## Referenced By
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[ai-adoption-barriers|Barriers to AI Adoption]]
- [[capability-ambition-gap|Capability-Ambition Gap]]

## Body

Legacy systems, inconsistent formats, undocumented processes, and knowledge silos mean most
mid-market firms sit on **low-quality input at scale**. The G7/Mila report is cited for the finding
that "access to high-quality, labeled, and structured data remains a major challenge" for SME AI
adoption.

The playbook's honest observation: the Karpathy approach **partially sidesteps** this by tolerating
format heterogeneity in `raw/` — PDFs, Slack exports, call transcripts, all welcome — "but it
cannot compensate for knowledge that was never captured in the first place."

That points to a pre-Second-Brain initiative most firms skip: structured knowledge capture
campaigns before AI activation. Exit interviews, expert sessions, decision logs — the human capture
layer in the [[three-layer-reference-architecture|reference architecture]].

Priyanshi Shah's retrospective on 2024 reaches the same conclusion from the failure side: legacy
systems struggled with AI requirements and "data quality complications plagued rollouts".

## Counter-arguments & Data Gaps

The distinction between *format* heterogeneity and *quality* is the useful part here, and it cuts
against the playbook's own enthusiasm. Tolerating any file format is an ingestion convenience. It
says nothing about whether the content is accurate, current, or contradictory — and compiling
confidently-written garbage into a well-structured wiki produces confidently-written garbage with
better cross-references.

The G7/Mila citation is the weakest evidentiary link in this page: **the source could not be
captured** (9MB PDF, no extractable text layer, no tooling available), so the playbook's
characterization of it is unverified. See
[[g7-ai-adoption-by-smes|AI Adoption by SMEs (G7 Report, Mila)]].

Unaddressed by every source here: how to tell a ready corpus from an unready one *before*
investing. "Data quality is a barrier" is universally agreed and operationally useless without a
diagnostic.

## Notes
_(hand-written notes — preserved across re-ingestion)_
