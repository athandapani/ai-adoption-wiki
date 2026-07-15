---
title: "145 AI Laws Were Passed in 2025. Privacy Teams Are Not Catching a Break."
source: "https://www.kiteworks.com/regulatory-compliance/ai-laws-2025-shadow-ai-privacy/"
author:
  - "[[Patrick Spencer]]"
published: 2026-06-10
created: 2026-07-15
description: "How 145 state AI laws enacted in 2025 create compliance exposure, especially via shadow AI embedded in authorized enterprise software."
playbook_ref: 21
capture_method: "webfetch-extract"
tags:
  - "clippings"
  - "governance"
  - "regulation"
  - "shadow-ai"
ingested: true
ingested_date: "2026-07-15"
---

> **Capture note:** structured extraction via WebFetch, not a verbatim clipping. Canonical text
> at the `source` URL.

# 145 AI Laws Were Passed in 2025. Privacy Teams Are Not Catching a Break.

**Author:** Patrick Spencer
**Published:** 2026-06-10

## Statistics (verbatim)

- "145 AI-related laws in 2025 — with 1,000+ bills introduced or revised"
- "63.6% of AI vendors do not disclose their third-party subprocessors"
- "32.8% of AI systems participate in at least one high-risk activity"
- "42% of companies abandoned AI projects in 2025 due to privacy concerns"
- "mid-sized companies spend $1.5 million annually on manual data subject request handling"

## Core argument

Most AI vendors hide their subprocessors in legal documentation, meaning companies deploy
**shadow AI through approved tools** without visibility into data flows. This hidden
infrastructure undermines data governance frameworks and creates regulatory exposure —
particularly as California's 2028 attestation requirement introduces **personal criminal
liability** for executives signing inaccurate privacy assessments.

## A distinction the playbook flattens

This source's shadow AI is *vendor-embedded* — AI reaching your data through tools you already
approved, invisible because the vendor didn't disclose its subprocessors. The playbook's
Section 4.5 shadow AI is *employee-initiated* — staff pasting data into personal ChatGPT
accounts. Both are real; they need different controls (vendor questionnaires vs. DLP and
enterprise account provisioning). The playbook treats them as one risk.
