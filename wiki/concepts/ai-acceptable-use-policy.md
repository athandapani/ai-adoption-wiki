---
title: AI Acceptable Use Policy
domain: [governance]
status: active
created: 2026-07-15
tags: [aup, governance, policy]
---

## TLDR
Approved tools list, data classification rules, output verification requirements, violation consequences, quarterly review — required before broad rollout, and useless against AI that arrives through vendors.

## Metadata
- source: playbook Section 4.4, ref [^26]
- created: 2026-07-15
- category: governance, policy

## Related
- [[shadow-ai|Shadow AI]] — depends-on
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[three-tier-sme-governance|Three-Tier SME Governance Framework]]
- [[four-pillar-governance|Four-Pillar Governance Framework]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[ai-literacy|AI Literacy]]
- [[shadow-ai-hidden-risk-enterprise|Shadow AI — The Hidden Risk in Your Enterprise]]
- [[145-ai-laws-2025|145 AI Laws Were Passed in 2025]] — contradicts (vendor-embedded AI evades any AUP)
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]

## Referenced By
- [[shadow-ai|Shadow AI]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[ai-literacy|AI Literacy]]

## Body

Every mid-market firm deploying AI needs a written AUP before broad rollout. Core elements:

1. **Approved tools list** — named, licensed enterprise versions (ChatGPT Enterprise, Claude for
   Business, Microsoft Copilot) vs. prohibited personal/unmanaged instances
2. **Data classification rules** — what categories (PII, IP, customer data, financial data) may and
   may not be submitted
3. **Output verification requirements** — which AI-assisted decisions or documents require human
   review before action
4. **Violation consequences** — clear, proportionate, documented
5. **Quarterly review cycle** — AUPs age rapidly

The sequencing point from [[governance-enables-rather-than-polices|the enablement argument]]
matters more than the contents: **provision the enterprise accounts before publishing the policy.**
An AUP that prohibits personal ChatGPT before offering a sanctioned alternative doesn't reduce
shadow AI, it just makes it unreportable.

## Counter-arguments & Data Gaps

**An AUP addresses roughly half the shadow AI problem.** It governs what employees do
deliberately. It does nothing about the 63.6% of vendors who don't disclose AI subprocessors —
that's an AI risk arriving through a tool the AUP's own approved list blesses. Patrick Spencer's
framing: companies "deploy shadow AI systems through approved tools without visibility into data
flows." No policy document an employee reads can catch that; it needs the vendor questionnaire in
[[four-pillar-governance|Pillar 3]].

Nothing in this corpus measures whether AUPs change behavior. Given that 47% of AI users are on
personal accounts, 78% admit to using non-employer-provided tools, and Kothari reports "58% use AI
at work and 57% hide it" — while AUPs have been standard advice for two years — the prior should
be that policy alone moves very little. The sources that report shadow AI declining attribute it to
DLP tooling and account provisioning, not policy.

The quarterly review cycle is right and almost never happens.

## Notes
_(hand-written notes — preserved across re-ingestion)_
