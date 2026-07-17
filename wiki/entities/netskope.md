---
title: Netskope
domain: [risk]
status: active
created: 2026-07-15
tags: [entity, shadow-ai, casb, research, vendor]
description: "Publisher of the Cloud and Threat Report supplying every shadow-AI usage figure in the playbook — and a vendor of the CASB tooling its own data recommends."
---

## TLDR
Publisher of the Cloud and Threat Report supplying every shadow-AI usage figure in the playbook — and a vendor of the CASB tooling its own data recommends.

## Metadata
- created: 2026-07-15
- category: organization, security vendor

## Related
- [[shadow-ai|Shadow AI]] — depends-on
- [[shadow-ai-hidden-risk-enterprise|Shadow AI — The Hidden Risk in Your Enterprise]] — the capture route
- [[ibm|IBM]]
- [[datagrail|DataGrail]]
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[ai-governance-challenges-shadow-ai|AI Governance Challenges: Shadow AI, Rules & Readiness]]

## Referenced By
- [[shadow-ai|Shadow AI]]

## Body

Netskope's **2026 Cloud and Threat Report**, via ref [^26], supplies the usage half of the
playbook's shadow AI section:

- **"~18k prompts/month"** across GenAI tools per average org — up ~6× year-over-year
- **"~223 GenAI-related data policy violations per month"** on average
- **"~47% of GenAI users access tools via personal/unmanaged accounts"**
- Data exposure split: source code **42%**, regulated data **32%**, IP **16%**

Netskope also appears as recommended tooling in the Discover step of the
[[shadow-ai|3-step protocol]] ("CASB/SSE tooling deployment (Netskope, Zscaler)").

The **6× year-over-year growth** is the figure that should drive urgency and the playbook doesn't
use it. 18,000 prompts/month is a snapshot; 6× growth is a trajectory, and it means any governance
baseline set today is measuring a different organization in twelve months.

## Counter-arguments & Data Gaps

**Netskope is a CASB vendor**, and the report's findings support purchasing CASB tooling — from
Netskope, which is named in the remediation step. This isn't disqualifying; Netskope has genuine
network-level visibility nobody else has. But the incentive should be stated, and neither ref [^26]
nor the playbook states it.

The figures also come from **Netskope's own customer telemetry**, which is a non-random sample:
organizations that buy CASB tooling are those that already suspected a shadow AI problem. "Average
org" means average Netskope customer.

Read entirely second-hand through a LinkedIn post; the primary report is never fetched and has no
reference in the playbook.

## Notes
_(hand-written notes — preserved across re-ingestion)_
