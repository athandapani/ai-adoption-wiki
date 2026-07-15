---
title: AI Hallucination Risk
domain: [risk]
status: active
created: 2026-07-15
tags: [hallucination, risk, reliability, nist]
---

## TLDR
"Confidently stated but false content" — rates run from 0.7% on the best model to 29.9% on the worst, and RAG-grounded legal tools still hallucinate 17–33% of the time.

## Metadata
- source: playbook Section 9.1, refs [^25] [^38] [^39]
- created: 2026-07-15
- category: risk, reliability

## Related
- [[hallucination-mitigation|Hallucination Mitigation Architecture]] — depends-on
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]
- [[managing-ai-hallucination-risk|Managing AI Hallucination Risk]]
- [[ai-hallucinations-in-the-enterprise|AI Hallucinations in the Enterprise]]
- [[the-67-billion-warning|The $67 Billion Warning]]
- [[nist|NIST]]
- [[vectara|Vectara]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[ai-in-traditional-industries|AI in Traditional Industries]]
- [[ai-literacy|AI Literacy]]

## Referenced By
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]
- [[ai-in-traditional-industries|AI in Traditional Industries]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[ai-literacy|AI Literacy]]

## Body

Hallucinations — NIST's "confidently stated but false content" — are a **strategic risk
multiplier**, not a quirk.

**Rates by model and task:**
- "LLM hallucination rates range from **0.7%** for Google Gemini-2.0-Flash-001 to **29.9%** for TII
  falcon-7B-instruct" (ref [^39])
- "even in the best performing LLM, **7 out of every 1000 prompts** will produce hallucinations"
- Summarization: **1–3%**; reasoning benchmarks: **above 14%** (ref [^25])
- **RAG-grounded legal research tools: 17–33%** on benchmark queries (ref [^25])

That last figure is the most important one here. Grounding reduces fabrication; it does not solve
it. Any architecture in this vault that treats RAG as a hallucination *fix* is overclaiming.

**Sector concern:** 44% of manufacturing decision-makers cite hallucination-driven accuracy issues
as a top concern, vs. a 36% cross-industry average — reflecting the safety-critical nature of
manufacturing decisions.

**The dangerous contexts for mid-market non-tech firms:** compliance document generation
(regulatory language fabricated with confidence); financial modeling support (numbers invented to
complete a coherent-looking table); customer-facing chatbots (policy misrepresented); technical
procedure documentation (safety-critical steps described incorrectly).

## Counter-arguments & Data Gaps

**The $67.4B figure should not be repeated without its provenance.** The playbook states "AI
hallucinations cost businesses an estimated $67.4 billion in losses in 2024". Ref [^38] attributes
it to "a comprehensive study by AllAboutAI, 2025" with **no methodology**. The chain is playbook →
korra.ai → AllAboutAI → unknown. It is a third-hand number with no visible derivation.

**The Air Canada case isn't in either cited source.** The playbook attributes it to [^38][^25];
ref [^38]'s capture explicitly does not mention it. Both cases it cites are real in the world
(*Moffatt v. Air Canada* 2024; *Mata v. Avianca* 2023) — they're just not supported by the
citations attached.

**"0.7–1% on structured tasks" is a precision that doesn't exist.** 0.7% is one model on one
leaderboard, not a range across structured tasks.

**Staleness:** ref [^39] is June 2025 and names Gemini-2.0-Flash as frontier. Model-specific
hallucination rates age faster than anything else in this vault. The underlying leaderboard is
almost certainly **Vectara's** — which the playbook's Appendix B recommends by name while giving it
no reference and no URL.

## Notes
_(hand-written notes — preserved across re-ingestion)_
