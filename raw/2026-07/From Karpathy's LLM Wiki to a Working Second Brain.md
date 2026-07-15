---
title: "From Karpathy's LLM Wiki to a Working Second Brain: My Implementation with Amazon Quick Desktop"
source: "https://www.doit.com/blog/llm-wiki-second-brain-implementation"
author:
  - "[[Dima Kramskoy]]"
published: 2026-06-12
created: 2026-07-15
description: "A practitioner's implementation of Karpathy's LLM Wiki using Amazon Quick Desktop and MkDocs, with a diff-and-approve write workflow."
playbook_ref: 8
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

# From Karpathy's LLM Wiki to a Working Second Brain: My Implementation with Amazon Quick Desktop

**Author:** Dima Kramskoy, Senior Cloud Architect at DoiT International
**Published:** 2026-06-12

## Description

A practical implementation of Andrej Karpathy's LLM Wiki concept using Amazon Quick Desktop to
build a persistent, structured knowledge base that compounds across conversations rather than
starting fresh each session.

## Implementation approach

Directory structure:

```
~/SecondBrain/
├── raw/            (unprocessed inputs)
├── wiki/           (concepts, entities, projects, sources, logs)
├── SCHEMA.md       (ontology defining page types)
└── mkdocs.yml      (documentation server)
```

Core tooling: MkDocs with Material theme, Amazon Quick Desktop, AWS Lambda/S3/Transcribe (voice
capture pipeline), launchd scheduler.

Key workflow: assistant proposes wiki updates with diffs → user approves/modifies → content
writes to disk → MkDocs auto-refreshes.

## Claims and results

- "15+ wiki pages in the first week", generated from organic conversations
- Self-assessed effectiveness rating: "7/10"
- Voice capture processes audio to structured knowledge at "fractions of a cent per capture"
