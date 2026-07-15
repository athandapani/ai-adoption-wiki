---
title: Knowledge Management Tool Landscape
domain: [tooling]
status: active
created: 2026-07-15
tags: [tooling, knowledge-management, pricing, vendors]
---

## TLDR
Glean, Guru, Notion AI, Confluence, Slab, Tettra, Microsoft Viva, or a DIY Karpathy wiki — the pricing table checks out against its source, the recommended stacks don't.

## Metadata
- source: playbook Sections 10.1–10.2, refs [^40] [^41]
- created: 2026-07-15
- category: tooling, vendor comparison

## Related
- [[ai-enterprise-km-guide-2026|AI Enterprise Knowledge Management Complete Guide 2026]] — depends-on
- [[best-ai-for-knowledge-management-2026|Best AI for Knowledge Management in 2026]]
- [[glean|Glean]]
- [[guru|Guru]]
- [[notion-ai|Notion AI]]
- [[confluence-atlassian-intelligence|Confluence + Atlassian Intelligence]]
- [[obsidian|Obsidian]]
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[digital-second-brain|Digital Second Brain]]
- [[build-vs-buy-mid-market|Build vs. Buy for Mid-Market]]
- [[generic-solutions-mismatch|Why Generic AI Solutions Don't Fit]]
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[the-proprietary-knowledge-moat|The Proprietary Knowledge Moat]]

## Referenced By
- [[digital-second-brain|Digital Second Brain]]
- [[build-vs-buy-mid-market|Build vs. Buy for Mid-Market]]
- [[capture-first-beats-search-first|Capture First, Search Second]]
- [[the-proprietary-knowledge-moat|The Proprietary Knowledge Moat]]

## Body

| Tool | Category | Best fit | Price | Differentiator |
|---|---|---|---|---|
| **Glean** | Enterprise AI search | 500+ employees, multi-system | $40–100/user/yr ($100K–2M) | 100+ connectors |
| **Guru** | Wiki + verification | Customer-facing teams | $15–30/user/yr | Verification workflows, staleness detection |
| **Notion AI** | Workspace + AI | Notion-native teams | $20 + $10 AI/user/mo | Low migration friction |
| **Confluence + Atlassian Intelligence** | Wiki + AI | Atlassian/engineering-heavy | $5.75–11/user + AI | Deep Jira integration |
| **Slab** | Modern wiki | Mid-market wanting modern UX | $8–15/user/yr | Clean UX, strong AI search |
| **Tettra** | Wiki (SMB) | <100 employees | $4–10/user/mo | Most affordable structured KB |
| **Microsoft Viva / M365 Copilot** | Enterprise AI | Microsoft shops | $30/user/mo | Native to M365 |
| **Custom Karpathy LLM Wiki** | DIY / open | Tech-capable teams, Obsidian users | $0 + LLM API costs | Full sovereignty, self-improving |

Pricing verified against ref [^40] — all seven commercial tools match.

**Guru's differentiator deserves more attention than the playbook gives it.** Verification
workflows and staleness detection are the *only* commercial implementation in this table of the
maintenance layer that [[karpathy-llm-wiki-method|the Karpathy method]] calls "linting" and leaves
entirely to prompts. For a vault of dated statistics — exactly this one — staleness detection is
the feature that decides whether the thing rots.

## Counter-arguments & Data Gaps

**The recommended stacks don't match the source.** The playbook's "Notion AI + Guru + Slack AI:
~$100–150K/year" for $50M–$150M firms doesn't appear in ref [^40], whose startup recommendation is
"Notion AI + Slack AI + Slite ~$20K/yr" — an order of magnitude apart. Only the mid-market row
("Glean + Notion + Guru ~$150K/yr") matches.

**A contradiction the playbook inherits and hides.** Ref [^40] says knowledge workers spend **1.8
hours/day** finding information; ref [^10] says **2.5 hours**. Both are cited. The playbook uses 2.5
to build its $1M–$2M recovered-capacity claim and never mentions 1.8 — a ~39% swing straight into
the headline ROI.

**The DIY row is the playbook's own and is under-costed.** "$0 tooling + LLM API costs" omits the
engineer maintaining it, which for a lean IT team is the binding constraint the entire document is
about. Section 10.2 prices it at "$20–50K/year in LLM API costs" for a team with "a developer
resource" — the developer being free is the assumption doing all the work.

Both sources are affiliate-style comparison sites.

## Notes
_(hand-written notes — preserved across re-ingestion)_
