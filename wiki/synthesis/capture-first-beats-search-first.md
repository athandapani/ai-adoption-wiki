---
title: Capture First, Search Second
domain: [cross-domain]
status: active
created: 2026-07-15
tags: [knowledge-management, sequencing, capture]
description: "Teams that build search before building capture end up with excellent search across a thin knowledge base — solve capture, accumulate volume, then optimize retrieval."
---

## TLDR
Teams that build search before building capture end up with excellent search across a thin knowledge base — solve capture, accumulate volume, then optimize retrieval.

## Metadata
- source: derived from playbook Section 12.2
- created: 2026-07-15
- category: synthesis, knowledge-management

## Related
- [[best-ai-for-knowledge-management-2026|Best AI for Knowledge Management in 2026]] — the source of this argument
- [[digital-second-brain|Digital Second Brain]] — depends-on
- [[data-quality-readiness|Data Quality and Infrastructure Readiness]] — the precondition capture cannot fix
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — tolerates format heterogeneity at the capture layer
- [[km-tool-landscape|Knowledge Management Tool Landscape]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[internal-knowledge-is-under-invested|Internal Knowledge Is Systematically Under-Invested]]

## Referenced By
- [[three-layer-reference-architecture|Three-Layer Reference Architecture]]
- [[digital-second-brain|Digital Second Brain]]

## Body

Craig Hunt's framing is the cleanest statement of the sequencing rule:

> "Knowledge teams that ship search before capture work end up with great search across a thin
> knowledge base. Get capture working, accumulate knowledge, then optimize search."

The economic argument underneath it matters more than the sequencing advice. Hunt's diagnosis of
why knowledge management failed at most organizations through 2025: **"the cost of capturing
knowledge exceeded the value to the capturer."** The person who writes the runbook is not the
person who benefits from it. That asymmetry, not tooling, is what kept wikis empty.

What changed in 2026, per the same source: automated capture from meetings and conversations now
produces structured knowledge without manual transcription. The capturer's cost approaches zero,
so the asymmetry stops binding.

This reframes the Second Brain investment. The hard part was never retrieval — vector search has
been adequate for years. The hard part was that nobody wanted to write things down. Any
architecture that still depends on humans volunteering to document will fail for the same reason
it failed before, whether it's RAG or a compiled wiki behind it.

The corollary the playbook draws in Section 3.1 is right and worth keeping: the Karpathy approach
tolerates format heterogeneity in `raw/`, which lowers capture cost further, "but it cannot
compensate for knowledge that was never captured in the first place." Tolerating messy inputs is
not the same as having inputs.

## Counter-arguments & Data Gaps

"Capture first" is easy to over-apply. Capture without any retrieval feedback loop produces a
landfill — volume with no signal about what is worth keeping. Hunt's own timeline (initial
integration in 4–12 weeks, maturity in 6–12 months) implies the two run closer to concurrently
than the slogan suggests.

The sharper objection: capture-first assumes the bottleneck is volume. For a mid-market firm with
a 200-person headcount and thirty years of SharePoint, the bottleneck may be that the existing
corpus is mostly wrong — superseded procedures, stale pricing, contradictory policies. Capturing
more of it faster makes the retrieval problem worse, not better. Nothing in this source addresses
corpus quality as distinct from corpus size.

Note also that this is a vendor-adjacent source (a fractional CTO ranking platforms), and
"capture is now cheap" is convenient for anyone selling automated capture.

## Notes
_(hand-written notes — preserved across re-ingestion)_
