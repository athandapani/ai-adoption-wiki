---
title: Andrej Karpathy
domain: [second-brain]
status: active
created: 2026-07-15
tags: [entity, person, llm-wiki, second-brain]
---

## TLDR
Author of the LLM Wiki gist that the playbook's entire thesis rests on — and which the playbook never cites.

## Metadata
- created: 2026-07-15
- category: person, researcher

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]]
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]]
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]]
- [[karpathy-llm-wiki-to-working-second-brain|From Karpathy's LLM Wiki to a Working Second Brain]]
- [[digital-second-brain|Digital Second Brain]]
- [[tiago-forte|Tiago Forte]]
- [[obsidian|Obsidian]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[digital-second-brain|Digital Second Brain]]

## Body

Karpathy published a GitHub gist describing an LLM-maintained wiki: raw sources compiled by an LLM
into structured markdown that the LLM then maintains and queries. Reported reach: "5,000+ stars.
1,400+ forks. Two days."

His statement of the division of labour is the method in one sentence:

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about
> what it all means. The LLM's job is everything else."

His own artifact: **~100 articles, ~400,000 words** on a single research topic, written and
maintained entirely by the agent. "No database. No embeddings. No vector store. Just folders and
text files."

## Counter-arguments & Data Gaps

**The gist is never cited in the playbook.** It has no numbered reference and no URL. Appendix B
recommends ingesting "Andrej Karpathy LLM Wiki GitHub Gist (April 2026)" as the "Original
architecture specification" — the playbook recommends reading the primary source it didn't read.

Every claim about the method in this vault therefore traces to secondary commentary: refs [^6],
[^8], [^9], and a Facebook group post [^42]. This vault inherits that gap; the gist was not fetched
here either, because no URL was available to fetch.

**The "17 million views" claim (Section 2.2) has no source at all.** The only reference reporting
gist metrics says 5,000+ stars and 1,400+ forks. The playbook also dates the gist to April 2026,
while ref [^42] — the source of the metrics — is dated May 2026.

Karpathy describes a **personal research workflow**. He is not on record recommending it for
enterprises, and ref [^6] explicitly says organizational collections still need RAG. The playbook's
extension of his method to mid-market enterprises is its own argument, presented as his.

## Notes
_(hand-written notes — preserved across re-ingestion)_
