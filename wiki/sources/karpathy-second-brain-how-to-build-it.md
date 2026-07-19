---
title: "How to Build Karpathy's Second Brain"
source: raw/2026-07/How to Build Karpathy's Second Brain Using AI for Knowledge Management.md
domain: [second-brain]
status: revisiting
created: 2026-07-15
tags: [source, karpathy, llm-wiki, facebook, playwright]
description: "An anonymous Facebook group post — and the actual source of the playbook's directory structure, the Karpathy quote, and its gist metrics."
---

## TLDR
An anonymous Facebook group post — and the actual source of the playbook's directory structure, the Karpathy quote, and its gist metrics.

## Metadata
- source: facebook.com/groups (Success Steps, Admin), published 2026-05-15 — playbook ref [^42]
- created: 2026-07-15
- category: llm-wiki methodology

## Source Link
[How to build Karpathy's Second Brain using AI for knowledge management](https://www.facebook.com/groups/868876935222403/posts/1310342537742505/)

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[andrej-karpathy|Andrej Karpathy]]
- [[digital-second-brain|Digital Second Brain]]
- [[obsidian|Obsidian]]
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]]
- [[karpathy-llm-wiki-to-working-second-brain|From Karpathy's LLM Wiki to a Working Second Brain]]
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]
- [[andrej-karpathy|Andrej Karpathy]]
- [[obsidian|Obsidian]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]

## Body

Captured via **Playwright** (public group post, no login required).

**The folder structure** — the playbook's Section 10.3 tree, renamed `my-knowledge-base/` →
`my-second-brain/` and otherwise identical:

```
my-knowledge-base/
├── raw/            # Your source material. AI reads but never modifies.
│   └── assets/     # Images, screenshots, diagrams
├── wiki/           # AI-maintained wiki. You read. AI writes.
├── outputs/        # Reports, analyses, answers from queries
└── CLAUDE.md       # The schema file that makes this whole thing work
```

**Gist metrics:** "karpathy dropped a full GitHub Gist. **5,000+ stars. 1,400+ forks. Two days.**"

**The Karpathy quote** the playbook uses: "The human's job is to curate sources, direct the
analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

Prerequisites: "Any AI coding tool that reads local files (Claude Code, Cursor, Codex, or
similar)"; "Obsidian recommended, but VS Code, Notepad, anything works"; "10+ source documents";
"30 minutes for initial setup, then 10 minutes per source after that".

On the contrast with RAG: explicitly against "ChatGPT file uploads, NotebookLM, and most RAG
systems" — "Zero accumulation." And: "No database. No embeddings. No vector store."

## Counter-arguments & Data Gaps

**Consider the provenance.** The playbook's implementation blueprint — the directory structure it
recommends mid-market enterprises adopt — comes from an **anonymous admin's post in a Facebook
group** called "AI Prompts & Automation for Business". That is the reference. Meanwhile Karpathy's
actual gist, which this post is summarizing, is never cited.

**The "17 million views" claim isn't here.** The playbook's Section 2.2 says the approach "gained 17
million views after a GitHub gist post in April 2026". This source — the only reference reporting
gist metrics — says 5,000+ stars and 1,400+ forks, and is dated **May 2026**. The view count has no
source anywhere.

Status `revisiting` on provenance, not content: the structure it describes is coherent and matches
refs [^8] and [^9], so the substance is corroborated. The citation is the problem.

## Notes
_(hand-written notes — preserved across re-ingestion)_
