---
title: Hallucination Mitigation Architecture
domain: [risk]
status: active
created: 2026-07-15
tags: [hallucination, mitigation, rag, architecture]
---

## TLDR
RAG grounding, citations-or-silence, human-in-the-loop for high-stakes, sandboxed agents, and cross-model validation — five controls, none of which eliminate the problem.

## Metadata
- source: playbook Section 9.2, refs [^25] [^39]
- created: 2026-07-15
- category: risk, architecture

## Related
- [[ai-hallucination-risk|AI Hallucination Risk]] — depends-on
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]
- [[digital-second-brain|Digital Second Brain]]
- [[managing-ai-hallucination-risk|Managing AI Hallucination Risk]]
- [[ai-hallucinations-in-the-enterprise|AI Hallucinations in the Enterprise]]
- [[the-67-billion-warning|The $67 Billion Warning]]
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]]
- [[four-pillar-governance|Four-Pillar Governance Framework]]

## Referenced By
- [[ai-hallucination-risk|AI Hallucination Risk]]
- [[hallucination-governance-metrics|Hallucination Governance Metrics]]
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]]

## Body

1. **RAG / Second Brain grounding** — connect outputs to a verified, maintained knowledge base.
   Every answer comes from indexed, source-traceable documents.
2. **Citations-or-silence** — if a claim can't be supported with a specific source citation, the
   system abstains rather than fabricating.
3. **Human-in-the-loop for high-stakes workflows** — credit decisions, legal documents, compliance
   outputs, safety procedures all require human review before action.
4. **Sandboxed agents** — restrict high-risk tool use, rate-limit sensitive actions, log all
   outputs.
5. **Cross-model validation** — for critical outputs, pass the same query to two models and flag
   disagreements for human review.

David Honour's framing is the right one: treat AI systems "with the same rigor applied to other
complex organizational systems" — model selection, prompt engineering, retrieval grounding, human
oversight, governance policies, continuous monitoring. No single control; a stack.

**Citations-or-silence is the one worth building first.** It's cheap, it's verifiable, and per
[[ai-literacy|AI Literacy]], output verification is the competency employees most lack — a system
that abstains rather than fabricates compensates for the human gap rather than depending on it.

## Counter-arguments & Data Gaps

**Control 1 is weaker than stated.** RAG-grounded legal research tools hallucinate **17–33%** on
benchmark queries. Grounding is necessary and nowhere near sufficient, and a citation-bearing
answer is *more* persuasive than an uncited one — so grounding that fails silently is more
dangerous than no grounding.

**Control 5 is expensive and rarely done.** Cross-model validation doubles inference cost and needs
a disagreement-adjudication path. No source reports anyone operating it in production, and a lean
IT team is the least likely to.

**Control 3 degrades predictably.** Human-in-the-loop assumes reviewers actually review. Automation
bias is well documented: reviewers approving a high-volume stream of mostly-correct outputs stop
reading. No source here addresses review fatigue, which is the mechanism by which HITL controls fail.

Note the incentive: refs [^38] and [^7] both sell RAG-based products, and both conclude the answer
is RAG. Ref [^39], the least conflicted source, is also the most measured — its answer is a
portfolio of controls plus monitoring, not an architecture.

## Notes
_(hand-written notes — preserved across re-ingestion)_
