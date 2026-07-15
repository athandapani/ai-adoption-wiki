---
title: Build vs. Buy for Mid-Market
domain: [spend]
status: revisiting
created: 2026-07-15
tags: [build-vs-buy, spend, strategy]
---

## TLDR
Buy the commodity layer, build the proprietary knowledge layer — a sound recommendation resting on a comparison table that doesn't appear in the source it's cited to.

## Metadata
- source: playbook Section 3.4, attributed to ref [^19]
- created: 2026-07-15
- category: spend, decision framework

## Related
- [[build-vs-buy-ai-framework|Build vs Buy AI: Decision Framework for Mid-Market]] — contradicts (the source compares delivery models, not build vs. buy)
- [[vendor-lock-in-and-tco|Vendor Lock-in and TCO Underestimation]] — depends-on
- [[ai-implementation-cost-2026|AI Implementation Cost 2026: SaaS vs Custom vs API-First]]
- [[the-proprietary-knowledge-moat|The Proprietary Knowledge Moat]]
- [[generic-solutions-mismatch|Why Generic AI Solutions Don't Fit]]
- [[km-tool-landscape|Knowledge Management Tool Landscape]]
- [[ai-skills-gap|The AI Skills Gap]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]]

## Referenced By
- [[vendor-lock-in-and-tco|Vendor Lock-in and TCO Underestimation]]
- [[the-proprietary-knowledge-moat|The Proprietary Knowledge Moat]]
- [[why-mid-market-is-structurally-different|Why Mid-Market Is Structurally Different]]

## Body

**The recommendation is right, and worth separating from its evidence.** For a mid-market firm with
a lean IT team: **buy the commodity layer** (LLM API access, embedding infrastructure, base
knowledge tools) and **build the proprietary knowledge layer** (the wiki content, the schema, the
governance rules, the domain-specific prompts).

It follows from [[the-proprietary-knowledge-moat|the moat argument]] without needing a table:
commodities are cheaper to buy than build and confer no advantage; the knowledge layer is the only
part a competitor cannot acquire.

**The evidence, though, doesn't match.** Section 3.4 presents a six-row Buy-vs-Build comparison
(time to value, customization, data sovereignty, long-term TCO, required IT capability, IP risk)
citing ref [^19]. That source — Damien Clothier's *Build vs Buy AI: Decision Framework for
Mid-Market Companies* — contains no such table. Its actual framework is **five weighted factors**
(Urgency 25%, Technical Complexity 20%, Internal Capability 20%, Budget Constraints 20%, Strategic
Importance 15%) comparing three **delivery models**:

| Model | 18-month cost |
|---|---|
| In-house | $200K–$450K |
| Big 4 consulting | $500K–$2M+ |
| Mid-market consulting | $35K–$250K |

Its conclusion is that mid-market consulting delivers fastest time-to-value at lowest risk — a
recommendation about *who does the work*, not *whether to build*.

Krunal Panchal's cost data (ref [^18]) is the better basis for an actual build-vs-buy call, and it
lands on **API-first** as the mid-market answer: "$115,000–$360,000" year one, balancing "speed with
iterability".

## Counter-arguments & Data Gaps

The playbook's table isn't just unsourced — parts of it are contradicted by the captured evidence.
"Long-term TCO: Buy = Escalating, Build = Stable" is hard to reconcile with custom builds at
$473K–$1.87M in year one plus $2K–$8K/month drift monitoring, versus $163K for SaaS. Build costs
are *less* predictable, not more.

"IP risk: Buy = High (vendor data use), Build = Low" is also stated rather than shown; enterprise
agreements from major vendors contractually exclude training on customer data.

Both ref [^19] and ref [^18] are published by firms selling implementation services, and both
conclude that the reader should engage a firm selling implementation services.

Status `revisiting`: the recommendation survives, the reasoning offered for it does not.

## Notes
_(hand-written notes — preserved across re-ingestion)_
