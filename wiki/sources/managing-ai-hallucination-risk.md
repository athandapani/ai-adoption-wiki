---
title: "Managing AI Hallucination Risk"
source: raw/2026-07/Managing AI Hallucination Risk - A Guide for Enterprise Risk Managers.md
domain: [risk]
status: revisiting
created: 2026-07-15
tags: [source, hallucination, vectara, risk-management]
description: "The least conflicted hallucination source in the corpus — and the likely unnamed conduit for Vectara's leaderboard figures."
---

## TLDR
The least conflicted hallucination source in the corpus — and the likely unnamed conduit for Vectara's leaderboard figures.

## Metadata
- source: resilienceforward.com (David Honour), published 2025-06-10 — playbook ref [^39]
- created: 2026-07-15
- category: risk, hallucination

## Related
- [[ai-hallucination-risk|AI Hallucination Risk]] — depends-on
- [[vectara|Vectara]] — the probable underlying leaderboard
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[ai-hallucinations-in-the-enterprise|AI Hallucinations in the Enterprise]]
- [[the-67-billion-warning|The $67 Billion Warning]]
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]

## Referenced By
- [[ai-hallucination-risk|AI Hallucination Risk]]
- [[vectara|Vectara]]
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]

## Body

**Author:** David Honour.

- "LLM hallucination rates range from **0.7%** for the Google Gemini-2.0-Flash-001 LLM to **29.9%**
  for the TII falcon-7B-instruct LLM"
- "even in the best performing LLM, **7 out of every 1000 prompts** will produce hallucinations"

Its approach is the most measured in the corpus: treat AI systems "with the same rigor applied to
other complex organizational systems" — model selection, prompt engineering, RAG, human oversight,
governance policies, continuous monitoring. A portfolio of controls, not an architecture.

Notably, this source is **not selling anything** — the only hallucination reference here that isn't
published by a vendor whose product is the recommended remedy.

## Counter-arguments & Data Gaps

**The playbook overstates this source's precision.** Section 9.1 reports "Best-performing frontier
models: 0.7–1% on structured tasks". This source gives **0.7% for one specific model** on one
leaderboard — not a range, not "structured tasks". The **"7 out of every 1,000 prompts"** figure
checks out exactly.

**The Vectara connection is inference, not verification.** A 0.7%–29.9% model-by-model range is the
signature of Vectara's HHEM leaderboard, which scores *summarization faithfulness against a provided
document*. If that's right, the playbook's "structured tasks" gloss is materially misleading — HHEM
measures the narrowest, most favorable case. But this source never names Vectara, the playbook
names Vectara without citing it, and the leaderboard wasn't fetched here. Status `revisiting`.

**Staleness is acute.** Published **June 2025**, naming Gemini-2.0-Flash as best-performing. Cited in
a 2026 playbook. Model-specific hallucination rates age faster than any other statistic in this
vault, and this one is over a year old.

## Notes
_(hand-written notes — preserved across re-ingestion)_
