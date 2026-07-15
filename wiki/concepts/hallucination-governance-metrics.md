---
title: Hallucination Governance Metrics
domain: [risk]
status: active
created: 2026-07-15
tags: [hallucination, metrics, dashboard, governance]
---

## TLDR
Hallucination@k, source attribution rate, abstention rate, escalation rate, and incident density — five leadership-dashboard metrics, none of which any source reports anyone actually running.

## Metadata
- source: playbook Section 9.3, ref [^25]
- created: 2026-07-15
- category: risk, metrics

## Related
- [[ai-hallucination-risk|AI Hallucination Risk]] — depends-on
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[ai-hallucinations-in-the-enterprise|AI Hallucinations in the Enterprise]]
- [[four-pillar-governance|Four-Pillar Governance Framework]]
- [[roi-measurement-problem|The ROI Measurement Problem]]
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]]

## Referenced By
- [[ai-hallucination-risk|AI Hallucination Risk]]
- [[hallucination-mitigation|Hallucination Mitigation Architecture]]
- [[four-pillar-governance|Four-Pillar Governance Framework]]

## Body

| Metric | Definition |
|---|---|
| **Hallucination@k** | % of answers containing unsupported claims in a random sample of k queries |
| **Source Attribution Rate** | % of outputs with verifiable citations |
| **Abstention Rate** | % of times the system defers or refuses rather than fabricating |
| **Escalation Rate** | % of outputs routed for human review |
| **Incident Density** | Hallucination incidents per 1,000 queries, by severity |

The projection driving executive attention: by 2030, enterprises embedding responsible AI
guardrails "will scale adoption 40% faster and achieve 25% higher customer retention" than peers.

**Abstention rate is the metric to watch, and the counter-intuitive one.** A rising abstention rate
looks like a system getting worse and is usually a system getting honest. It's the direct
measurement of whether [[hallucination-mitigation|citations-or-silence]] is actually working, and
the one metric here that can't be gamed by making the model more confident.

## Counter-arguments & Data Gaps

**Hallucination@k requires ground truth**, which is the whole problem. Someone must judge whether
each of k answers contains an unsupported claim — a domain expert, reading carefully, at sampling
volume. For a lean IT team this is the most expensive metric on the list and the one the playbook
lists first without costing it.

**Four of five metrics are process, not outcome.** Attribution rate, abstention rate, and escalation
rate all measure system behavior, not correctness. A system can cite 100% of outputs and cite them
wrongly — RAG legal tools do exactly that at 17–33%. Only Hallucination@k and incident density touch
truth, and both need human adjudication.

**Nobody reports running these.** No source in this corpus describes an organization operating a
hallucination dashboard, or publishes a baseline. There is no benchmark for what a good
Hallucination@k looks like in an enterprise, so the metrics are unactionable even if you collect
them.

The "40% faster / 25% higher retention by 2030" projection is an analyst forecast with no
methodology, five years out, from a source that sells AI advisory services.

## Notes
_(hand-written notes — preserved across re-ingestion)_
