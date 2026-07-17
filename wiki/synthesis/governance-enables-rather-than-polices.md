---
title: Governance Enables, It Doesn't Police
domain: [cross-domain]
status: active
created: 2026-07-15
tags: [governance, ai-coe, enablement]
description: "Governance frameworks built for large enterprises fail at mid-market scale by creating bottlenecks that delay adoption more than they reduce risk; the working posture is automated guardrails plus a CoE with an expiry date."
---

## TLDR
Governance frameworks built for large enterprises fail at mid-market scale by creating bottlenecks that delay adoption more than they reduce risk; the working posture is automated guardrails plus a CoE with an expiry date.

## Metadata
- source: derived from playbook Sections 4.1, 11.1, 12.2
- created: 2026-07-15
- category: synthesis, governance

## Related
- [[ai-coe-should-work-itself-out-of-a-job|Your AI CoE Should Work Itself Out of a Job]] — the source of the dissolution argument
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]] — depends-on
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]
- [[three-tier-sme-governance|Three-Tier SME Governance Framework]]
- [[four-pillar-governance|Four-Pillar Governance Framework]]
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]]
- [[shadow-ai|Shadow AI]] — what over-governance produces
- [[use-case-prioritization-matrix|Use Case Prioritization Matrix]]
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]

## Referenced By
- [[why-mid-market-is-structurally-different|Why Mid-Market Is Structurally Different]]
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]]

## Body

Amit Kothari's argument is the sharpest version: a CoE is scaffolding, not foundation. "Real
success is that the team's knowledge lives everywhere. The people move on to other roles, but the
capability stays." He gives it an **18-month timeline with "an end date from day one"** — invoking
Drucker: "The best organizations push capability to where the work happens, not keep it locked in
a central group."

The playbook keeps the sentiment and drops the deadline. Section 12.2's "Make the CoE invisible
over time" is the same idea with nothing operable in it. The end date is the entire mechanism — it
is what converts a stated intention to dissolve into a thing that actually dissolves. Without it,
every CoE has always intended to work itself out of a job.

The enabling posture, assembled across sources, is concrete:

- **Standards that make the right thing easy**, not approval gates. Enterprise AI accounts
  provisioned before the AUP lands, so compliance is the path of least resistance.
- **Automated controls over human gatekeeping** — DLP rules and CASB tooling enforce boundaries
  without a reviewer in the loop.
- **Tiered oversight calibrated to impact** — customer-facing and compliance-relevant AI get
  scrutiny; internal productivity tools don't.
- **A quarterly review cadence** that keeps policy current without standing overhead.

There is a feedback loop the playbook has all the parts for and never assembles. Its
[[shadow-ai|Shadow AI]] section documents 47% of AI users on personal accounts. Its change
management source (ref 27) lists "high shadow-AI usage" as the diagnostic warning sign of a
*Desire* failure in ADKAR. Kothari reports "58% use AI at work and 57% hide it". Put together:
**shadow AI is the measured output of over-governance.** People route around controls that make
their work harder. Governance that polices produces the exact risk it exists to prevent, and the
shadow-AI rate is the cheapest available instrument for detecting it.

That reframes the metric. Shadow AI usage isn't only a security number to drive down — it's a
governance-quality signal to read.

## Counter-arguments & Data Gaps

The dissolution argument is strongest where capability is genuinely distributable and weakest
where it isn't. Model risk management, EU AI Act conformity assessment, and vendor subprocessor
review are specialist functions with real regulatory teeth — €35M or 7% of global revenue under
the AI Act, and California's 2028 attestation regime attaching personal criminal liability to
executives. "Push it to where the work happens" is a poor answer to a compliance obligation that
requires a named accountable expert. Some of this should stay central permanently.

Kothari's 18-month figure has no derivation. It is a plausible-sounding round number.

And the causal claim in this page — that over-governance produces shadow AI — is inference across
three sources, not a finding in any of them. The correlation is consistent with the reverse
direction (permissive environments breed casual tool use) or with a common cause (fast-moving
teams both adopt AI early and dislike process). No source tests it.

## Notes
_(hand-written notes — preserved across re-ingestion)_
