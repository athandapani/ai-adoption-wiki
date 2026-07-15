---
title: "AI Spending by Industry 2026"
source: raw/2026-07/AI Spending by Industry 2026 - Budget Data by Sector.md
domain: [spend, industry]
status: active
created: 2026-07-15
tags: [source, spend, per-employee, mis-citation]
---

## TLDR
The per-employee spend source — where four of the playbook's five cited figures don't match, and the fifth doesn't exist.

## Metadata
- source: aistackhub.ai, published 2026-04 — playbook ref [^33]
- created: 2026-07-15
- category: spend, per-employee benchmarks

## Related
- [[ai-spending-benchmarks|AI Spending Benchmarks]] — contradicts (Section 6.5's figures don't match this source)
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]] — depends-on
- [[ai-in-traditional-industries|AI in Traditional Industries]]
- [[gartner|Gartner]]
- [[vendor-lock-in-and-tco|Vendor Lock-in and TCO Underestimation]]
- [[gartner-ai-spending-forecast-2026|Gartner's $2.52T AI Spending Forecast]]
- [[smb-technology-spending-2026|SMB Technology Spending Statistics 2026]]

## Referenced By
- [[ai-spending-benchmarks|AI Spending Benchmarks]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]
- [[ai-in-traditional-industries|AI in Traditional Industries]]

## Body

Per-employee AI spend, verbatim:

- Professional Services: **"$3,470"**
- Technology/SaaS: **"$11,200"**
- Manufacturing: **"$900"**
- Healthcare: **"$4,200"**
- Financial Services: **"$8,400"**
- Global AI spending: "$2.59 trillion in 2026"

**No logistics/distribution figure appears in this source.**

Its actual argument: "The flip happens at scale: SMBs spend 52% on SaaS subscriptions. Enterprises
spend 41% on implementation" — and real AI costs are "typically **2–3× the tool subscription
budget**" because firms underestimate data prep, training, and integration.

## Counter-arguments & Data Gaps

**Playbook Section 6.5 cites this source for five figures. One matches.**

| Sector | Playbook | This source |
|---|---|---|
| Professional services | ~$3,470 | $3,470 ✅ |
| Technology | ~$5,200 | **$11,200** ❌ |
| Manufacturing | ~$1,800 | **$900** ❌ |
| Healthcare services | ~$2,800 | **$4,200** ❌ |
| Logistics/distribution | ~$2,100 | **absent** ❌ |

This matters beyond bookkeeping. Section 6.5 uses the manufacturing and logistics numbers to derive
its headline recommendation — "a realistic starting AI budget is **$360K–$700K per year**" for a
200-employee traditional-industry firm. Manufacturing is doubled; logistics is invented. **The
recommendation does not follow from the cited source.**

Note the direction: every discrepancy inflates traditional-industry spend and deflates tech's,
narrowing the apparent gap and making the recommendation look moderate.

The source's own best insight — that real costs run 2–3× the subscription line — is the one thing
the playbook doesn't take from it, despite Section 3.4 being about exactly that.

Unbylined research-team content on an affiliate-style site.

## Notes
_(hand-written notes — preserved across re-ingestion)_
