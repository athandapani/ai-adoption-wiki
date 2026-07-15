---
title: Attribution Problems in the Source Playbook
domain: [cross-domain]
status: active
created: 2026-07-15
tags: [meta, verification, source-criticism, playbook]
---

## TLDR
Verifying all 43 of the playbook's references against their captured sources found one fabricated concept, four of five invented per-employee spend figures, a scrambled five-posture taxonomy, an invented report title, and a central thesis that its own primary source explicitly contradicts.

## Metadata
- source: derived from verification of all 43 captures in `raw/2026-07/`
- created: 2026-07-15
- category: synthesis, source-criticism

## Related
- [[capability-ambition-gap|Capability-Ambition Gap]] — the clearest fabrication
- [[the-new-normal-ai-adoption-in-smes|The New Normal: The Status Quo of AI Adoption in SMEs]] — the paper that doesn't contain it
- [[five-human-postures-toward-ai|Five Human Postures Toward AI]] — taxonomy scrambled in transit
- [[five-faces-of-ai-readiness|The 5 Faces of Human Readiness for AI Adoption]] — the actual archetypes
- [[ai-spending-by-industry-2026|AI Spending by Industry 2026]] — four of five figures don't match
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]] — contradicts the playbook's own thesis
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — the thesis in question
- [[knowledge-attrition-cost|The Cost of Knowledge Attrition]] — rests on an untraceable $300K figure
- [[ai-spending-benchmarks|AI Spending Benchmarks]] — "BCG Radar 6" appears to be invented
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]] — the tension the playbook never acknowledges

## Referenced By
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[digital-second-brain|Digital Second Brain]]

## Body

This vault was compiled from a single seed document. Every one of its 43 references was fetched
and checked against what the playbook claims it says. Most check out. A meaningful minority do
not, and the failures cluster in the playbook's most load-bearing claims.

**A fabricated concept.** Section 1.2 attributes a named analytical frame — the
"capability-ambition gap" — to a 2025 academic study, in quotation marks. The study is Schwaeke
et al., *The new normal: The status quo of AI adoption in SMEs* (Journal of Small Business
Management). Its full 108,008-character text contains the word "ambition" **zero times**, and
"digital security" zero times. The paper is a systematic literature review of 106 articles
organized by the technology–organization–environment model. It characterizes nothing as a
capability-ambition gap. See [[capability-ambition-gap|Capability-Ambition Gap]].

**Invented spend figures.** Section 6.5 lists five per-employee AI spend figures citing AI Stack
Hub. Only professional services ($3,470) matches. Technology is $11,200, not $5,200.
Manufacturing is $900, not $1,800. Healthcare is $4,200, not $2,800. Logistics has no figure in
the source at all. The section then derives its headline "$360K–$700K per year" budget
recommendation from the manufacturing and logistics numbers — so the recommendation does not
follow from the cited source.

**A scrambled taxonomy.** Section 8.4's five employee postures are renamed from the WEF's
originals, and two are substantively different concepts. The playbook's "Anxious" (fears job
displacement) is the WEF's "AI opposed", not its sceptics; its "Skeptics" (doubt reliability) is
the WEF's "sceptics", not its "cautious" (data security and ethics). Interventions end up attached
to the wrong archetypes.

**An invented title.** Sections 6.1 and Appendix B cite "BCG Radar 6: AI Investments Surge, CEOs
Take the Lead (2026)". The report is called **AI Radar 2026**. "BCG Radar 6" appears in none of
the three captured sources that report its findings.

**An absent primary source.** Appendix B recommends ingesting the "Andrej Karpathy LLM Wiki
GitHub Gist (April 2026)" as the "Original architecture specification". The gist is never cited
anywhere in the playbook. Every claim about Karpathy's method traces to secondary commentary. The
"17 million views" claim in Section 2.2 has no source at all — the one reference reporting gist
metrics says "5,000+ stars, 1,400+ forks".

**And the thesis problem.** Reference [^6], the playbook's own primary source for the Karpathy
method, states that the method "scales effectively for individuals and small teams" and
acknowledges that "organizational collections require traditional RAG systems". The playbook's
entire argument is that enterprises should adopt it instead of RAG. Its source says the opposite,
and the playbook does not mention this.

## Counter-arguments & Data Gaps

The strongest defense of the playbook: most of it is fine. The shadow-AI section (4.5) is
excellent — every figure traces cleanly to Netskope and IBM via [^26]. The governance tiers
(4.2), the lean CoE model (5.1–5.4), the tool pricing table (10.1), and the critical success
factors (12.2) all reproduce their sources faithfully. This is not a document of invented
research; it is a mostly-sound document with a specific failure mode.

That failure mode is worth naming precisely: **the errors are directional**. Manufacturing spend
is doubled, not halved. The 2.5-hours-searching figure is used and the 1.8-hour one from another
cited source is not. The 95%-of-pilots-fail figure appears in two of its own sources and in none
of its text. The "85% say AI exceeded expectations" figure does appear. Every discrepancy found
points the same way — toward a larger investment case.

What would change this conclusion: access to the playbook's drafting process. These patterns are
equally consistent with LLM-assisted synthesis that hallucinated plausible figures and citations,
which would make it careless rather than motivated. The observable result is the same.

This page is not an argument against using the playbook. It is an argument for reading its
citations, which is what this vault is for.

## Notes
_(hand-written notes — preserved across re-ingestion)_
