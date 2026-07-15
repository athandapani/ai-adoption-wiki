# Node registry — ai-adoption-wiki

Scratch planning artifact. **Not part of the vault** (`plans/` sits outside `wiki/`, so the
graph builder never walks it).

Purpose: freeze the complete node list *before* writing any page. `wiki-graph-explorer` drops
dangling wikilinks **silently** — a link to a slug that doesn't exist costs an edge with no
error. This file is the closure check.

Rules enforced here:
- Node ID = filename minus `.md`. Globally unique across all four folders.
- No collision with the sibling `second-brain` vault (shared Obsidian graph at `GitFiles/`).
- Every link target below must appear in this registry.

## Collision check against `second-brain` (41 slugs) — PASSED

Its slugs, for reference: `llm-wiki-pattern`, `agent-vs-compiler-wiki`,
`wiki-schema-design-for-second-brain`, `karpathy-coding-discipline`,
`karpathy-coding-guidelines`, `wiki-operational-practices`, `deterministic-compiler-pipeline`,
`memory-lifecycle-management`, `applied-ai-transformation-positioning`,
`digital-technology-office-pmo`, `initiative-capacity-planning-tool`, `megamind-slack-bot`,
`vendor-evaluation-business-case-skill`, `accenture`, `archer-aviation`, `hirschvogel`,
18 `people/` slugs, 6 `sources/` slugs, 4 `synthesis/` slugs.

Deliberate avoidances:
- `llm-wiki-pattern` (taken) → this repo uses **`karpathy-llm-wiki-method`**
- `wiki-schema-design-for-second-brain` (taken) → **`wiki-schema-design-for-ai-adoption-wiki`**
- `karpathy-coding-discipline` / `karpathy-coding-guidelines` (taken) → **`andrej-karpathy`**
- `agent-vs-compiler-wiki` (taken) → this repo's equivalent tension lives in **`rag-vs-llm-wiki`**

No other overlaps. Safe.

---

## `sources/` — 43 nodes (one per playbook reference)

| # | slug | title | status | capture |
|---|---|---|---|---|
| 1 | `sme-ai-adoption-oecd-insights` | SME AI Adoption in 2025: Key Insights from OECD Research | active | ok |
| 2 | `rsm-middle-market-ai-survey-2025` | AI Adoption by Mid-Market Firms (RSM 2025 Survey) | active | ok |
| 3 | `state-of-smb-ai-automation-2026` | State of SMB AI Automation 2026 | active | ok |
| 4 | `bcg-revenue-benchmark-post` | How Much Should Your Mid-Size Enterprise Be Spending on AI? | active | ok |
| 5 | `the-new-normal-ai-adoption-in-smes` | The New Normal: The Status Quo of AI Adoption in SMEs | revisiting | 403 paywall |
| 6 | `llm-knowledge-bases-karpathy` | LLM Knowledge Bases: Karpathy's Self-Improving Second Brain | active | ok |
| 7 | `turning-institutional-knowledge-into-ai-assets` | Turning Institutional Knowledge into Strategic AI Assets | active | ok |
| 8 | `karpathy-llm-wiki-to-working-second-brain` | From Karpathy's LLM Wiki to a Working Second Brain | active | ok |
| 9 | `build-a-second-brain-step-by-step` | Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step | active | ok |
| 10 | `rag-knowledge-management-roi` | RAG: Transform Enterprise Knowledge \| 300-500% ROI | revisiting | ok |
| 11 | `from-information-silos-to-enterprise-brain` | From Information Silos to Enterprise Brain | revisiting | ok |
| 12 | `g7-ai-adoption-by-smes` | AI Adoption by SMEs (G7 Report, Mila) | revisiting | PDF, no text layer |
| 13 | `why-businesses-struggled-with-ai-2024` | Why Businesses Struggled with AI in 2024 | dormant | ok |
| 14 | `gartner-ai-spending-forecast-2026` | Gartner's $2.52T AI Spending Forecast | active | ok |
| 15 | `ai-literacy-training-explained` | AI Literacy Training Explained | active | ok |
| 16 | `ai-skills-gap-widens` | AI Skills Gap Widens as Training Lags Behind | active | ok |
| 17 | `ai-literacy-new-workplace-skill` | AI Literacy: The New Workplace Skill | active | ok |
| 18 | `ai-implementation-cost-2026` | AI Implementation Cost 2026: SaaS vs Custom vs API-First | active | ok |
| 19 | `build-vs-buy-ai-framework` | Build vs Buy AI: Decision Framework for Mid-Market | revisiting | ok — possible mis-citation |
| 20 | `datagrail-privacy-ai-trends-2026` | Privacy and AI Trends Report 2026 | active | ok |
| 21 | `145-ai-laws-2025` | 145 AI Laws Were Passed in 2025 | active | ok |
| 22 | `ai-governance-challenges-shadow-ai` | AI Governance Challenges: Shadow AI, Rules & Readiness | active | PENDING |
| 23 | `ai-governance-framework-for-smbs` | AI Governance for SMBs: ISO 42001 Framework | active | PENDING |
| 24 | `ai-coe-without-hiring-an-army` | How to Build an AI CoE Without Hiring an Army | active | PENDING |
| 25 | `ai-hallucinations-in-the-enterprise` | AI Hallucinations in the Enterprise: Risks Explained | active | PENDING |
| 26 | `shadow-ai-hidden-risk-enterprise` | Shadow AI — The Hidden Risk in Your Enterprise | active | PENDING |
| 27 | `change-management-ai-adoption-playbook` | Change Management for AI Adoption: A 2026 Playbook | active | PENDING |
| 28 | `indian-ceos-doubling-down-on-ai` | Indian CEOs Are Doubling Down on AI Investments | active | PENDING |
| 29 | `ai-investments-surge-2026-bcg` | AI Investments Set to Surge in 2026: BCG Report | revisiting | PENDING (MSN) |
| 30 | `vanilla-graph-agentic-rag` | How Enterprises Use Vanilla, Graph, and Agentic RAG | active | PENDING |
| 31 | `ai-cost-statistics-2026` | AI Cost Statistics 2026: Forecasting, ROI, Budget Risk | active | PENDING |
| 32 | `smb-technology-spending-2026` | SMB Technology Spending Statistics 2026 | active | PENDING |
| 33 | `ai-spending-by-industry-2026` | AI Spending by Industry 2026 | active | PENDING |
| 34 | `ai-use-cases-and-trends-2026` | AI Use Cases and Key Statistics and Trends for 2026 | active | PENDING |
| 35 | `overcoming-ai-resistance` | Overcoming AI Resistance: Change Management for AI | active | PENDING |
| 36 | `five-faces-of-ai-readiness` | The 5 Faces of Human Readiness for AI Adoption | active | PENDING |
| 37 | `resistant-employees-know-why` | Your Resistant Employees Know Why Your AI Adoption Is Failing | active | PENDING (Forbes) |
| 38 | `the-67-billion-warning` | The $67 Billion Warning: How AI Hallucinations Hurt Enterprises | active | PENDING |
| 39 | `managing-ai-hallucination-risk` | Managing AI Hallucination Risk | active | PENDING |
| 40 | `ai-enterprise-km-guide-2026` | AI Enterprise Knowledge Management Complete Guide 2026 | active | PENDING |
| 41 | `best-ai-for-knowledge-management-2026` | Best AI for Knowledge Management in 2026 | active | PENDING |
| 42 | `karpathy-second-brain-how-to-build-it` | How to Build Karpathy's Second Brain | revisiting | PENDING (Facebook) |
| 43 | `ai-coe-should-work-itself-out-of-a-job` | Your AI CoE Should Work Itself Out of a Job | active | PENDING |

Status rationale: `revisiting` = capture incomplete, source contested, or figure unverified.
`dormant` = superseded by newer data (ref 13 is a Jan-2025 retrospective on 2024, superseded by
refs 1/2/3).

## `concepts/` — 30 nodes

| slug | title | domain | status |
|---|---|---|---|
| `mid-market-ai-paradox` | The Mid-Market AI Paradox | adoption | active |
| `capability-ambition-gap` | Capability-Ambition Gap | adoption | active |
| `ai-adoption-barriers` | Barriers to AI Adoption | adoption | active |
| `transformative-integration-gap` | The Transformative Integration Gap | adoption | active |
| `digital-second-brain` | Digital Second Brain | second-brain | active |
| `karpathy-llm-wiki-method` | Karpathy LLM Wiki Method | second-brain | active |
| `rag-vs-llm-wiki` | RAG vs. LLM Wiki | second-brain | revisiting |
| `retrieval-augmented-generation` | Retrieval-Augmented Generation (RAG) | second-brain | active |
| `knowledge-attrition-cost` | The Cost of Knowledge Attrition | second-brain | revisiting |
| `data-quality-readiness` | Data Quality and Infrastructure Readiness | adoption | active |
| `ai-skills-gap` | The AI Skills Gap | change-management | active |
| `ai-literacy` | AI Literacy | change-management | active |
| `generic-solutions-mismatch` | Why Generic AI Solutions Don't Fit | adoption | active |
| `vendor-lock-in-and-tco` | Vendor Lock-in and TCO Underestimation | spend | active |
| `build-vs-buy-mid-market` | Build vs. Buy for Mid-Market | spend | active |
| `roi-measurement-problem` | The ROI Measurement Problem | spend | active |
| `ai-governance-for-lean-orgs` | AI Governance for Lean Organizations | governance | active |
| `three-tier-sme-governance` | Three-Tier SME Governance Framework | governance | active |
| `four-pillar-governance` | Four-Pillar Governance Framework | governance | active |
| `ai-acceptable-use-policy` | AI Acceptable Use Policy | governance | active |
| `shadow-ai` | Shadow AI | risk | active |
| `lean-ai-center-of-excellence` | Lean AI Center of Excellence | governance | active |
| `use-case-prioritization-matrix` | Use Case Prioritization Matrix | governance | active |
| `ai-spending-benchmarks` | AI Spending Benchmarks | spend | active |
| `ai-budget-allocation` | Where the AI Budget Goes | spend | active |
| `adkar-for-ai` | ADKAR Applied to AI | change-management | active |
| `leadership-modeling-imperative` | The Leadership Modeling Imperative | change-management | active |
| `five-human-postures-toward-ai` | Five Human Postures Toward AI | change-management | active |
| `ai-hallucination-risk` | AI Hallucination Risk | risk | active |
| `hallucination-mitigation` | Hallucination Mitigation Architecture | risk | active |
| `hallucination-governance-metrics` | Hallucination Governance Metrics | risk | active |
| `km-tool-landscape` | Knowledge Management Tool Landscape | tooling | active |
| `three-layer-reference-architecture` | Three-Layer Reference Architecture | second-brain | active |
| `ninety-day-governance-launch` | The 90-Day Governance Launch Plan | governance | active |
| `ai-in-traditional-industries` | AI in Traditional Industries | industry | active |

(35 — grew past 30 during layout; acceptable, richer graph.)

## `entities/` — 23 nodes

| slug | title | domain |
|---|---|---|
| `oecd` | OECD | adoption |
| `bcg` | Boston Consulting Group | spend |
| `gartner` | Gartner | spend |
| `mckinsey` | McKinsey | change-management |
| `forrester` | Forrester Research | change-management |
| `ey` | EY | spend |
| `pwc` | PwC | change-management |
| `nist` | NIST | risk |
| `ibm` | IBM | risk |
| `prosci` | Prosci | change-management |
| `world-economic-forum` | World Economic Forum | change-management |
| `datagrail` | DataGrail | risk |
| `vectara` | Vectara | risk |
| `rsm` | RSM | adoption |
| `andrej-karpathy` | Andrej Karpathy | second-brain |
| `tiago-forte` | Tiago Forte | second-brain |
| `glean` | Glean | tooling |
| `guru` | Guru | tooling |
| `notion-ai` | Notion AI | tooling |
| `confluence-atlassian-intelligence` | Confluence + Atlassian Intelligence | tooling |
| `obsidian` | Obsidian | tooling |
| `iso-42001` | ISO/IEC 42001 | governance |
| `eu-ai-act` | EU AI Act | governance |

## `synthesis/` — 8 nodes

| slug | title | domain |
|---|---|---|
| `capture-first-beats-search-first` | Capture First, Search Second | cross-domain |
| `governance-enables-rather-than-polices` | Governance Enables, It Doesn't Police | cross-domain |
| `why-mid-market-is-structurally-different` | Why Mid-Market Is Structurally Different | cross-domain |
| `internal-knowledge-is-under-invested` | Internal Knowledge Is Systematically Under-Invested | cross-domain |
| `adoption-is-a-leadership-problem` | Adoption Is a Leadership Problem, Not a Technology Problem | cross-domain |
| `the-proprietary-knowledge-moat` | The Proprietary Knowledge Moat | cross-domain |
| `attribution-problems-in-the-playbook` | Attribution Problems in the Source Playbook | cross-domain |
| `wiki-schema-design-for-ai-adoption-wiki` | Wiki Schema Design for ai-adoption-wiki | cross-domain |

---

## Totals

| Folder | Nodes |
|---|---|
| `sources/` | 43 |
| `concepts/` | 35 |
| `entities/` | 23 |
| `synthesis/` | 8 |
| **Total** | **109** |

Expected edges: ~330–380 (undirected, deduped).

## Standing contradictions to preserve (not resolve)

These are the most valuable content in the vault. Each gets a `— contradicts` relation hint and
a `## Counter-arguments & Data Gaps` entry:

1. **`llm-knowledge-bases-karpathy` explicitly scopes the no-RAG claim to individuals and small
   teams, and says organizational collections still need RAG.** The playbook extends the method
   to enterprises anyway. This is the single sharpest tension in the vault, and the playbook
   never acknowledges it.
2. `rag-knowledge-management-roi` (300–500% RAG ROI) vs. the playbook's "RAG retrieves, a wiki
   compounds" framing — the playbook cites RAG ROI figures to justify a non-RAG architecture.
3. `bcg-revenue-benchmark-post`: 94% will keep spending regardless of ROI vs. only 6% see
   meaningful impact.
4. `sme-ai-adoption-oecd-insights` (resistance is 6–7% of barriers) vs. McKinsey via
   `change-management-ai-adoption-playbook` (change management is *the top* barrier). The
   playbook asserts both, in Sections 1.3 and 8.1, without reconciling them.
5. `145-ai-laws-2025` vendor-embedded shadow AI vs. `shadow-ai-hidden-risk-enterprise`
   employee-initiated shadow AI — different risks, different controls, conflated by the playbook.
6. `build-vs-buy-ai-framework` — the playbook's build-vs-buy table does not appear in the cited
   source, which actually compares delivery models. Possible mis-citation.

## Unverified figures (flagged, not laundered)

- **$300,000 per departing senior employee** — playbook attributes to ref 10; not present in the
  capture of ref 10.
- **312% ROI / 141% over 3 years** — ref 11 confirms 312%; the "141% over 3 years" figure has no
  cited source in the playbook (ref 30 is a RAG-architecture piece).
- **$67.4B hallucination losses in 2024** — ref 38 headline; methodology unknown.
- **17 million views / 5,000+ stars on Karpathy's gist (April 2026)** — playbook Section 2.2;
  the gist itself is not in the reference list. No primary source.
- **Vectara LLM Hallucination Rate Index** — named in Appendix B but has **no numbered
  reference** and no URL anywhere in the playbook. Entity page will say so.

These are why `attribution-problems-in-the-playbook` exists as a synthesis page.
