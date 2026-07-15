---
title: "How to build Karpathy's Second Brain using AI for knowledge management"
source: "https://www.facebook.com/groups/868876935222403/posts/1310342537742505/"
author:
  - "[[Success Steps]]"
published: 2026-05-15
created: 2026-07-15
description: "Facebook group post giving copy-paste prompts for building Karpathy's LLM wiki; the source of the playbook's directory structure."
playbook_ref: 42
capture_method: "playwright-fulltext"
tags:
  - "clippings"
  - "second-brain"
  - "llm-wiki"
  - "karpathy"
ingested: true
ingested_date: "2026-07-15"
---

> **Capture note:** full text retrieved via Playwright (public group post, no login required).
> Canonical text at the `source` URL.

# How to build Karpathy's Second Brain using AI for knowledge management

**Author:** "Success Steps" (Admin), in the group *AI | AI Prompts & Automation for Business*
**Published:** 2026-05-15

## Reach claims (verbatim)

"karpathy dropped a full GitHub Gist. 5,000+ stars. 1,400+ forks. Two days."

## The Karpathy quote (verbatim)

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about
> what it all means. The LLM's job is everything else." — Andrej Karpathy

## The concept (verbatim excerpts)

> "Instead of the AI searching your raw files every time, the AI reads your sources once and
> compiles a structured wiki. Summaries, cross-references, connections between ideas,
> contradictions flagged."

> "Every new source you add makes the wiki richer. Every question you ask can get filed back in.
> Knowledge compounds instead of resetting."

> "His result: ~100 articles, ~400,000 words on a single research topic. He didn't write a word of
> it. The AI wrote, linked, categorized, and maintained all of it."

> "No database. No embeddings. No vector store. Just folders and text files."

Explicitly contrasted against "ChatGPT file uploads, NotebookLM, and most RAG systems" — "Zero
accumulation."

## The folder structure (verbatim)

```
my-knowledge-base/
├── raw/            # Your source material. AI reads but never modifies.
│   └── assets/     # Images, screenshots, diagrams
├── wiki/           # AI-maintained wiki. You read. AI writes.
├── outputs/        # Reports, analyses, answers from queries
└── CLAUDE.md       # The schema file that makes this whole thing work
```

## Prerequisites (verbatim)

- "Any AI coding tool that reads local files (Claude Code, Cursor, Codex, or similar)"
- "A text editor (Obsidian recommended, but VS Code, Notepad, anything works)"
- "10+ source documents on a topic you care about"
- "30 minutes for initial setup, then 10 minutes per source after that"

## Schema conventions it recommends

YAML frontmatter per wiki page with `title`, `created`, `last_updated`, `source_count`.
Stated intent: "The schema is the difference between a generic chatbot and a disciplined wiki
maintainer."

## Notes on the playbook's use of this source

Section 10.3's directory tree is this post's tree, renamed `my-knowledge-base/` → `my-second-brain/`
and otherwise reproduced faithfully.

**But Section 2.2's "17 million views" claim is not here.** This source reports "5,000+ stars.
1,400+ forks. Two days." — the playbook says the approach "gained 17 million views after a GitHub
gist post in April 2026". No source in the reference list supports 17 million views, and this post
(dated May 2026, the only one citing gist metrics) contradicts the April date implicitly.

Note also what this source is: **an anonymous admin's Facebook group post**. The playbook's
Appendix B recommends ingesting the "Andrej Karpathy LLM Wiki GitHub Gist (April 2026)" as the
"Original architecture specification" — but the gist itself is **never cited** in the playbook.
Every claim about Karpathy's method traces to secondary commentary: this post, ref [^6], ref [^9],
ref [^8]. The primary source is absent from a document whose central thesis rests on it.
