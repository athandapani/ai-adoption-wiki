---
title: Three-Tier SME Governance Framework
domain: [governance]
status: revisiting
created: 2026-07-15
tags: [governance, iso-42001, tiering]
---

## TLDR
Basic ($0/mo, 2 weeks, Notion + Sheets), Standard (~$200/mo, 4 weeks, ISO 42001 Lite), Premium ($1,500+/mo, 8+ weeks, full ISO 42001) — with Standard the right starting point for most $50M–$200M firms.

## Metadata
- source: playbook Section 4.2, ref [^23]
- created: 2026-07-15
- category: governance, framework

## Related
- [[ai-governance-framework-for-smbs|AI Governance for SMBs: ISO 42001 Framework]] — depends-on
- [[iso-42001|ISO/IEC 42001]]
- [[eu-ai-act|EU AI Act]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[four-pillar-governance|Four-Pillar Governance Framework]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]

## Referenced By
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]

## Body

Adapted from ISO 42001 for resource-constrained organizations:

| Tier | Coverage | Time | Tooling | Cost/mo |
|---|---|---|---|---|
| **Basic** | EU AI Act Annex A | 2 weeks | Notion + Google Sheets | $0 |
| **Standard** | ISO 42001 Lite | 4 weeks | Airtable + OpenAI Moderation | ~$200 |
| **Premium** | Full ISO 42001, full audit trail | 8+ weeks | OneTrust + IBM Watson | $1,500+ |

**Audit trail retention: 3 years minimum.**

For most mid-market firms in the $50M–$200M range, **Standard** is the appropriate starting point
— it addresses the most material risks without requiring dedicated compliance staff.

The source's actual argument for tiering, which the playbook omits: small businesses face
regulatory penalties **averaging $47,200** for non-compliance yet lack documentation frameworks.
That's the number that justifies the $200/month, and it's missing from the playbook's version.

## Counter-arguments & Data Gaps

**This source is a July 2025 blog post by an author credited only as "admin", cited in a 2026
playbook as current governance guidance.** That matters more than usual here: the EU AI Act's
high-risk provisions became enforceable in **August 2026** — *after* this framework was written.
A tier table whose Basic level covers "EU AI Act Annex A" was designed against a regulatory
landscape that has since changed.

The playbook also silently extends it. It appends "Acceptable Use Policy" to Basic and "shadow AI
controls" to Standard; neither appears in the source. Reasonable additions, undeclared.

Deeper problem: the tiers are defined by **tooling and cost**, not by risk exposure. A 60-person
firm running customer-facing AI on regulated data needs more than a 400-person firm using Copilot
for internal drafting, regardless of revenue. Tier selection should follow from the risk
assessment; here it follows from company size, which is the wrong axis.

The $47,200 average penalty has no methodology or jurisdiction attached. Status `revisiting` on
staleness grounds.

## Notes
_(hand-written notes — preserved across re-ingestion)_
