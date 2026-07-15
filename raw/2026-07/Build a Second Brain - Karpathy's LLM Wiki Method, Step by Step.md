---
title: "Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step"
source: "https://www.askglitch.com/blog/build-a-second-brain"
author:
  - "[[Professor Glitch]]"
published: 2026-05-02
created: 2026-07-15
description: "A step-by-step guide to Karpathy's LLM Wiki method — a three-layer architecture where the AI maintains a compounding knowledge base in Obsidian and Claude Code."
playbook_ref: 9
capture_method: "webfetch-extract"
tags:
  - "clippings"
  - "second-brain"
  - "llm-wiki"
ingested: true
ingested_date: "2026-07-15"
---

> **Capture note:** structured extraction via WebFetch, not a verbatim clipping. Canonical text
> at the `source` URL.

# Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step

**Author:** Professor Glitch
**Published:** 2026-05-02

## Description

A guide to implementing Andrej Karpathy's LLM Wiki method — a three-layer architecture where AI
maintains a persistent, compounding research knowledge base through structured workflows in
Obsidian and Claude Code.

## The three-layer architecture

- **Layer 1 (Sources):** raw, immutable documents (PDFs, articles, transcripts, notes) in a
  `sources/` folder that the AI reads but never edits.
- **Layer 2 (Wiki):** AI-generated markdown pages — summaries, entity profiles, concepts, and
  cross-references — that the agent actively maintains.
- **Layer 3 (Schema):** a `CLAUDE.md` configuration document specifying folder structure, naming
  conventions, and operational workflows.

## Four core operations

- `/capture <url>` — ingest new sources and update affected wiki pages
- `/sync` — reconcile batches of new sources with the wiki
- `/lint` — health-check for broken links, contradictions, and coverage gaps
- `/digest` — generate weekly synthesis and pattern summaries

## Claims

- "Karpathy's vault...became a research artifact of around 100 articles and 400,000 words, all
  written and maintained by the agent."
