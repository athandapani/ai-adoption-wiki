---
title: Guru
domain: [tooling]
status: active
created: 2026-07-15
tags: [entity, vendor, wiki, verification, tooling]
---

## TLDR
Modern wiki at $15–30/user/yr whose verification workflows and staleness detection are the only commercial implementation of the maintenance layer everything else in this vault hand-waves.

## Metadata
- created: 2026-07-15
- category: vendor, software

## Related
- [[km-tool-landscape|Knowledge Management Tool Landscape]] — depends-on
- [[ai-enterprise-km-guide-2026|AI Enterprise Knowledge Management Complete Guide 2026]] — the capture route
- [[best-ai-for-knowledge-management-2026|Best AI for Knowledge Management in 2026]]
- [[glean|Glean]]
- [[notion-ai|Notion AI]]
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — leaves this layer to prompts
- [[capture-first-beats-search-first|Capture First, Search Second]]

## Referenced By
- [[km-tool-landscape|Knowledge Management Tool Landscape]]

## Body

**Category:** Modern wiki + verification.
**Price:** $15–30/user/yr.
**Differentiator:** "Modern wiki + AI search + knowledge card + verification workflow" — knowledge
verification and staleness detection.
**Best fit:** customer-facing teams (customer success, sales).

**The verification workflow is the interesting part.** Ref [^41] names verification-before-publishing
as one of the shifts that made knowledge management viable in 2026: "Knowledge verification
workflows flag stale content before deployment." The playbook's Section 12.2 lists "verify before
publishing widely" as a critical success factor.

Guru is the only tool in the landscape that ships this as a product. Stage 6 of the
[[karpathy-llm-wiki-method|Karpathy pipeline]] — linting and health checks — is the same idea
implemented as a monthly prompt, and is the least-specified stage in every source describing the
method.

For a vault of dated statistics like this one, staleness detection isn't a nice-to-have; it's the
thing that decides whether the knowledge base is an asset or a liability in eighteen months.

## Counter-arguments & Data Gaps

Verification workflows solve the *mechanics* of staleness and not the *judgment*. Something still
has to decide that a claim has expired — Guru surfaces cards for review on a cadence; a human has
to know that Gemini-2.0-Flash is no longer frontier. The tool routes the question, it doesn't
answer it.

No source in this corpus reports outcome data for verification workflows — no measured reduction in
stale-content incidents, no adoption rate for the review prompts. The feature is described, never
evaluated.

## Notes
_(hand-written notes — preserved across re-ingestion)_
