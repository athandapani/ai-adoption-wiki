---
title: Four-Pillar Governance Framework
domain: [governance]
status: active
created: 2026-07-15
tags: [governance, ai-coe, framework]
---

## TLDR
Use Case Intake, Model Risk Management, Vendor Oversight, and Incident Response — the governance structure for a mid-market firm with no dedicated compliance team.

## Metadata
- source: playbook Section 4.3, refs [^24] [^23] [^20] [^25]
- created: 2026-07-15
- category: governance, framework

## Related
- [[ai-coe-without-hiring-an-army|How to Build an AI CoE Without Hiring an Army]] — depends-on
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]]
- [[use-case-prioritization-matrix|Use Case Prioritization Matrix]]
- [[three-tier-sme-governance|Three-Tier SME Governance Framework]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[datagrail-privacy-ai-trends-2026|Privacy and AI Trends Report 2026]]
- [[vendor-lock-in-and-tco|Vendor Lock-in and TCO Underestimation]]
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]
- [[ai-hallucinations-in-the-enterprise|AI Hallucinations in the Enterprise]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]

## Referenced By
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]

## Body

**Pillar 1: Use Case Intake.** A standardized process for evaluating and approving new AI use
cases, driven by a two-by-two of business impact against organizational feasibility. See
[[use-case-prioritization-matrix|Use Case Prioritization Matrix]].

**Pillar 2: Model Risk Management.** Oversight tiered to business impact. Customer-facing AI,
compliance-relevant AI, and decision-support AI for senior leaders all need more scrutiny than
internal productivity tools. **Audit trail retention: 3 years minimum.**

**Pillar 3: Vendor Oversight.** The critical question: does the vendor disclose third-party AI
subprocessors? **63.6% do not.** Vendor questionnaires should cover data processing agreements,
subprocessor transparency, model retraining on customer data, and breach notification timelines.

**Pillar 4: Incident Response.** A defined process for when an AI system produces an unexpected
output with business consequences. Minimum: a **named accountable person per AI system**, a
documented escalation path, and a root-cause analysis template. Track incident density
(hallucination incidents per 1,000 queries by severity) on a leadership dashboard.

## Counter-arguments & Data Gaps

Pillar 3 is the strongest and most under-stated. The subprocessor problem isn't a due-diligence
checkbox — Patrick Spencer's point is that it makes **shadow AI arrive through tools you already
approved**. Your AUP, your DLP rules, and your enterprise account provisioning are all irrelevant
to an AI subprocessor sitting behind a SaaS vendor you signed in 2023. The playbook treats
vendor-embedded and employee-initiated shadow AI as one risk; they need entirely different
controls, and only one of them is addressed by
[[ai-acceptable-use-policy|the AUP]].

Pillar 4's "named accountable person per AI system" is the pillar most likely to fail quietly in a
lean org — it's the one that requires a person rather than a document, and if the CoE dissolves on
schedule per [[governance-enables-rather-than-polices|the 18-month argument]], nobody has said who
inherits the names.

The four pillars come from a consultancy's insights page, with no validation data. The 3-year audit
retention figure comes from a different source (ref [^23]) with no jurisdiction attached.

## Notes
_(hand-written notes — preserved across re-ingestion)_
