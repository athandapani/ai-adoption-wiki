---
title: Shadow AI
domain: [governance, risk]
status: active
created: 2026-07-15
tags: [shadow-ai, risk, governance, breach-cost]
description: "Unauthorized employee AI use outside IT visibility — ~18,000 prompts/month per org with 47% on personal accounts, 223 policy violations/month, and +$670,000 in breach costs where it's present."
---

## TLDR
Unauthorized employee AI use outside IT visibility — ~18,000 prompts/month per org with 47% on personal accounts, 223 policy violations/month, and +$670,000 in breach costs where it's present.

## Metadata
- source: playbook Section 4.5, ref [^26] (via Netskope 2026 and IBM 2025)
- created: 2026-07-15
- category: risk, governance

## Related
- [[shadow-ai-hidden-risk-enterprise|Shadow AI — The Hidden Risk in Your Enterprise]] — depends-on
- [[netskope|Netskope]]
- [[ibm|IBM]]
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[145-ai-laws-2025|145 AI Laws Were Passed in 2025]] — contradicts (vendor-embedded shadow AI is a different risk)
- [[datagrail-privacy-ai-trends-2026|Privacy and AI Trends Report 2026]]
- [[ai-governance-challenges-shadow-ai|AI Governance Challenges: Shadow AI, Rules & Readiness]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[adkar-for-ai|ADKAR Applied to AI]]
- [[five-faces-of-ai-readiness|The 5 Faces of Human Readiness for AI Adoption]]

## Referenced By
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[ai-literacy|AI Literacy]]

## Body

**This is the best-sourced section of the playbook.** Every figure traces cleanly to Netskope's
2026 Cloud and Threat Report or IBM's 2025 Cost of a Data Breach Report, via ref [^26].

Scale:
- **~18,000 prompts/month** per average org across GenAI tools — up ~6× year-over-year
- **~223 AI-related data policy violations/month** per organization
- **~47% of GenAI users** access tools via personal/unmanaged accounts

Cost:
- **+$670,000 higher breach costs** in high-shadow-AI environments vs. low/none (IBM)
- **65% more PII** and **40% more IP** compromised per incident
- **20% of organizations** reported a breach involving shadow AI — a figure the playbook omits

What gets exposed:
- Source code: **42%** of violations
- Regulated data (PII, financial, health): **32%**
- Intellectual property: **16%**

**The 3-step protocol** (8–12 weeks):
1. **Discover** (weeks 1–2): network traffic analysis for AI API calls, browser extension audits,
   anonymous employee survey, CASB/SSE tooling (Netskope, Zscaler)
2. **Classify** (weeks 3–4): risk matrix — Critical (PII/PHI/source code → block), High
   (proprietary docs → monitor + DLP), Medium (internal drafts → training), Low (public → approved)
3. **Govern** (weeks 5–12): written AUP, mandatory 15-minute awareness training with real cases,
   DLP rules, enterprise AI account provisioning, monthly violation reports to leadership

## Counter-arguments & Data Gaps

**Two different risks wear this name.** Ref [^26]'s shadow AI is *employee-initiated* — staff
pasting source code into personal ChatGPT. Ref [^21]'s is *vendor-embedded* — AI reaching your data
through approved SaaS whose subprocessors aren't disclosed (63.6% aren't). The playbook conflates
them. They need different controls: DLP and account provisioning for the first, vendor
questionnaires for the second. An org that runs the 3-step protocol perfectly still has the second
problem entirely untouched.

**Read it as a governance signal, not just a threat.** Ref [^27] lists high shadow-AI usage as the
diagnostic warning sign of an ADKAR *Desire* failure. The WEF describes employees who publicly
comply and privately circumvent. Kothari: "58% use AI at work and 57% hide it." Shadow AI is what
people do when sanctioned tools are worse than unsanctioned ones — see
[[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]]. Blocking without
provisioning treats the symptom.

**Source caveat:** ref [^26] is a LinkedIn post relaying two primary reports. The figures are
almost certainly right, but neither Netskope nor IBM was read directly for this vault. Netskope
also sells CASB tooling and is cited in the remediation step of the protocol its own data justifies.

## Notes
_(hand-written notes — preserved across re-ingestion)_
