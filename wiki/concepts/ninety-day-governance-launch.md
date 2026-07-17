---
title: The 90-Day Governance Launch Plan
domain: [governance]
status: active
created: 2026-07-15
tags: [governance, implementation, roadmap]
description: "Days 1–30 inventory and draft the AUP, 31–60 provision accounts and train, 61–90 audit and report — the playbook's most immediately actionable section."
---

## TLDR
Days 1–30 inventory and draft the AUP, 31–60 provision accounts and train, 61–90 audit and report — the playbook's most immediately actionable section.

## Metadata
- source: playbook Section 11.2, refs [^23] [^26]
- created: 2026-07-15
- category: governance, roadmap

## Related
- [[three-tier-sme-governance|Three-Tier SME Governance Framework]] — depends-on
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[shadow-ai|Shadow AI]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]]
- [[eu-ai-act|EU AI Act]]
- [[iso-42001|ISO/IEC 42001]]
- [[shadow-ai-hidden-risk-enterprise|Shadow AI — The Hidden Risk in Your Enterprise]]
- [[ai-governance-framework-for-smbs|AI Governance for SMBs: ISO 42001 Framework]]

## Referenced By
- [[three-tier-sme-governance|Three-Tier SME Governance Framework]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[shadow-ai|Shadow AI]]

## Body

**Days 1–30 (Foundation)**
- Complete AI system inventory: what's in use, authorized *and* shadow
- Draft the [[ai-acceptable-use-policy|AUP]], reviewed by legal and leadership
- Identify the three initial use cases for the CoE portfolio

**Days 31–60 (Implementation)**
- Deploy approved enterprise AI accounts, replacing personal-account usage
- Run mandatory 15-minute shadow AI awareness training for all staff
- Stand up Basic-tier governance in Notion/Sheets (risk register, tool log, AUP)
- Launch pilot use case #1 with champion network support

**Days 61–90 (Validation)**
- Conduct the first shadow AI audit (network traffic, browser extension inventory)
- Complete a compliance checklist against applicable regulations (EU AI Act, state AI laws)
- Document use case #1 results for executive sponsor reporting
- Set the quarterly review calendar

**The sequencing is right and non-obvious.** Enterprise accounts land in days 31–60, *before* the
first shadow AI audit in 61–90 — so people have a sanctioned path before anyone goes looking for
unsanctioned ones. That's [[governance-enables-rather-than-polices|enabling rather than policing]]
expressed as a calendar, and it's the detail most implementations get backwards.

## Counter-arguments & Data Gaps

**The plan under-scopes its own first task.** "Complete AI system inventory" in 30 days is the
hardest item on the list, not a warm-up. Discovering shadow AI needs network traffic analysis and
CASB tooling — which the plan doesn't deploy until day 61. So the day-1–30 inventory is
self-reported, and per Kothari, **"58% use AI at work and 57% hide it"**. You are asking people to
declare the thing they're hiding, before you've given them the amnesty of a sanctioned alternative.

**The vendor-embedded half is missing entirely.** Nothing in 90 days touches the 63.6% of vendors
who don't disclose AI subprocessors. A firm completes this plan and still doesn't know which of its
approved SaaS tools has AI in it.

**Timeline conflict:** the plan compresses ref [^26]'s Discover/Classify/Govern protocol, which is
itself **8–12 weeks** and starts with discovery — into a 90-day plan where discovery happens twice
(day 1–30 self-report, day 61–90 audit) and the audit lands last.

The 15-minute training duration has no evidence behind it, and sits oddly beside
[[ai-literacy|AI Literacy]]'s 4–8 hour recommendation from the same document.

## Notes
_(hand-written notes — preserved across re-ingestion)_
