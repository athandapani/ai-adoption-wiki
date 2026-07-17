---
title: "From Karpathy's LLM Wiki to a Working Second Brain"
source: raw/2026-07/From Karpathy's LLM Wiki to a Working Second Brain.md
domain: [second-brain]
status: active
created: 2026-07-15
tags: [source, karpathy, implementation, practitioner]
description: "The only first-hand practitioner account in the corpus — a cloud architect's implementation, self-rated 7/10, with a diff-and-approve write workflow."
---

## TLDR
The only first-hand practitioner account in the corpus — a cloud architect's implementation, self-rated 7/10, with a diff-and-approve write workflow.

## Metadata
- source: doit.com (Dima Kramskoy), published 2026-06-12 — playbook ref [^8]
- created: 2026-07-15
- category: llm-wiki methodology, practitioner report

## Related
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — depends-on
- [[digital-second-brain|Digital Second Brain]]
- [[andrej-karpathy|Andrej Karpathy]]
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]]
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]]
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]]
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]]

## Referenced By
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]]

## Body

**Author:** Dima Kramskoy, Senior Cloud Architect at DoiT International.

His structure:

```
~/SecondBrain/
├── raw/         (unprocessed inputs)
├── wiki/        (concepts, entities, projects, sources, logs)
├── SCHEMA.md    (ontology defining page types)
└── mkdocs.yml   (documentation server)
```

Tooling: MkDocs + Material, Amazon Quick Desktop, AWS Lambda/S3/Transcribe for voice capture,
launchd scheduling.

**The workflow detail worth stealing:** assistant proposes wiki updates **with diffs** → user
approves or modifies → content writes to disk. That's the same human-confirmation gate this vault's
own `/jarvis-ingest` enforces, arrived at independently.

Results: "15+ wiki pages in the first week" from organic conversations; voice capture at "fractions
of a cent per capture".

**Self-assessed effectiveness: 7/10.**

## Counter-arguments & Data Gaps

That 7/10 is the most honest number in the entire corpus, and the playbook doesn't mention it.
Every other Karpathy-method source reports unqualified enthusiasm; the one person describing an
actual running system rates it a B-minus.

Scope: this is a **personal** vault, one week old, built by a senior cloud architect with AWS
services and a launchd scheduler. It's evidence that the method works for a technical individual.
It is not evidence for an enterprise deployment — and it remains the closest thing to
implementation evidence in the playbook's 43 references.

DoiT is an AWS partner, and the implementation showcases Amazon Quick Desktop.

## Notes
_(hand-written notes — preserved across re-ingestion)_
