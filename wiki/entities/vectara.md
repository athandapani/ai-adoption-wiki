---
title: Vectara
domain: [risk]
status: revisiting
created: 2026-07-15
tags: [entity, hallucination, leaderboard, uncited]
description: "Named in Appendix B as a recommended primary source for hallucination rates, with no reference, no URL, and no citation anywhere in the playbook."
---

## TLDR
Named in Appendix B as a recommended primary source for hallucination rates, with no reference, no URL, and no citation anywhere in the playbook.

## Metadata
- created: 2026-07-15
- category: organization, AI vendor

## Related
- [[managing-ai-hallucination-risk|Managing AI Hallucination Risk]] — the likely unnamed conduit
- [[ai-hallucination-risk|AI Hallucination Risk]] — depends-on
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]
- [[nist|NIST]]
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]

## Referenced By
- [[ai-hallucination-risk|AI Hallucination Risk]]

## Body

Appendix B lists **"Vectara LLM Hallucination Rate Index (2025)"** as a recommended raw/ ingestion
source, described as "Empirical hallucination rates by model".

It has **no numbered reference, no URL, and no in-text citation** anywhere in the playbook's 43
references.

**It's almost certainly the real origin of the playbook's hallucination numbers.** Ref [^39]
reports "LLM hallucination rates range from **0.7%** for the Google Gemini-2.0-Flash-001 LLM to
**29.9%** for the TII falcon-7B-instruct LLM" — a model-by-model range with that shape and those
endpoints is the signature of Vectara's Hughes Hallucination Evaluation Model leaderboard, which
scores models on summarization faithfulness. Ref [^39] doesn't name Vectara; the playbook names
Vectara without citing it. The two halves never meet.

## Counter-arguments & Data Gaps

The identification here is **inference, not verification**. The 0.7%/29.9% endpoints and
model-by-model structure strongly suggest the HHEM leaderboard, but ref [^39] doesn't attribute
them, and Vectara's leaderboard was not fetched for this vault. Status `revisiting` accordingly.

The consequence matters more than the attribution. The playbook's Section 9.1 says "Best-performing
frontier models: **0.7–1% on structured tasks**" — but HHEM measures *summarization faithfulness
against a provided document*, which is the narrowest and most favorable possible test. Presenting
it as a general "structured tasks" rate overstates reliability considerably. The same leaderboard's
methodology is why ref [^25] can report 1–3% on summarization and **above 14% on reasoning
benchmarks** without contradiction — different tasks, different rates.

Vectara also sells RAG infrastructure, and publishes the benchmark on which grounding looks
necessary.

## Notes
_(hand-written notes — preserved across re-ingestion)_
