---
title: "Managing AI hallucination risk: a guide for enterprise risk managers"
source: "https://resilienceforward.com/managing-ai-hallucination-risk-a-guide-for-enterprise-risk-managers/"
author:
  - "[[David Honour]]"
published: 2025-06-10
created: 2026-07-15
description: "Framework for identifying and mitigating hallucination risk; carries the 0.7%–29.9% model-by-model rate range."
playbook_ref: 39
capture_method: "webfetch-extract"
tags:
  - "clippings"
  - "hallucination"
  - "risk"
  - "vectara"
ingested: true
ingested_date: "2026-07-15"
---

> **Capture note:** structured extraction via WebFetch, not a verbatim clipping. Canonical text
> at the `source` URL.

# Managing AI hallucination risk: a guide for enterprise risk managers

**Author:** David Honour
**Published:** 2025-06-10

## Hallucination rates (verbatim)

- "LLM hallucination rates range from 0.7% for the Google Gemini-2.0-Flash-001 LLM to 29.9% for
  the TII falcon-7B-instruct LLM"
- "even in the best performing LLM, 7 out of every 1000 prompts will produce hallucinations"

The article does **not** provide figures for frontier models on structured tasks, reasoning
benchmarks, or RAG-grounded legal tools.

## Core argument

Hallucination risks can be managed through a structured approach combining model selection,
prompt engineering, retrieval-augmented generation, human oversight, governance policies, and
continuous monitoring — treating AI systems with the same rigor applied to other complex
organizational systems.

## Notes on the playbook's use of this source

The **"7 out of every 1,000 prompts"** figure in Section 9.1 checks out exactly.

The playbook's "Best-performing frontier models: 0.7–1% on structured tasks" **overstates the
precision** of this source: 0.7% here is a single model (Gemini-2.0-Flash-001) on a single
leaderboard, not a "0.7–1% on structured tasks" range.

**This is almost certainly the Vectara leaderboard.** The 0.7%–29.9% model-by-model range is the
signature of Vectara's Hughes Hallucination Evaluation Model leaderboard. Appendix B lists
"Vectara LLM Hallucination Rate Index (2025)" as a recommended source but gives it **no numbered
reference and no URL anywhere in the playbook** — this source is the likely unnamed conduit.

Note the date: **June 2025**, cited in a 2026 playbook. Model-specific hallucination rates age
faster than almost any other statistic in this vault.
