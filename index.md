# index

Catalog of every page in `wiki/`, one line each (TLDR), grouped by folder. Kept flat; if this file
exceeds ~200 lines, split into `index/{sources,entities,concepts,synthesis}.md` and turn this file
into a table of contents.

Status: `active` (well-sourced, current) · `revisiting` (thin, contested, or stale-dated) ·
`dormant` (superseded or historical). See `wiki/synthesis/wiki-schema-design-for-ai-adoption-wiki.md`.

## Synthesis

- [[adoption-is-a-leadership-problem|Adoption Is a Leadership Problem, Not a Technology Problem]] — Across five independent sources, AI initiatives stall on people and process rather than model capability — but the sources disagree sharply on whether employee resistance is a minor barrier or the whole story.
- [[attribution-problems-in-the-playbook|Attribution Problems in the Source Playbook]] — Verifying all 43 of the playbook's references against their captured sources found one fabricated concept, four of five invented per-employee spend figures, a scrambled five-posture taxonomy, an invented report title, and a central thesis that its own primary source explicitly contradicts.
- [[capture-first-beats-search-first|Capture First, Search Second]] — Teams that build search before building capture end up with excellent search across a thin knowledge base — solve capture, accumulate volume, then optimize retrieval.
- [[governance-enables-rather-than-polices|Governance Enables, It Doesn't Police]] — Governance frameworks built for large enterprises fail at mid-market scale by creating bottlenecks that delay adoption more than they reduce risk; the working posture is automated guardrails plus a CoE with an expiry date.
- [[internal-knowledge-is-under-invested|Internal Knowledge Is Systematically Under-Invested]] — Internal knowledge and RAG take 8% of SMB AI budgets while customer service takes 29% — the playbook calls this systematic under-investment, but the ROI figures it uses to prove the gap are the weakest-sourced numbers in the corpus.
- [[the-proprietary-knowledge-moat|The Proprietary Knowledge Moat]] — A competitor can buy the same model but cannot replicate your accumulated institutional knowledge — which is the strongest strategic argument in the playbook and the one it spends the least time on.
- [[why-mid-market-is-structurally-different|Why Mid-Market Is Structurally Different]] — Mid-market firms ($50M–$500M ARR) have enough institutional knowledge and data complexity to justify sophisticated AI, and neither the headcount to build it the enterprise way nor the greenfield to rebuild AI-native like a startup.
- [[wiki-schema-design-for-ai-adoption-wiki|Wiki Schema Design for ai-adoption-wiki]] — This vault inherits second-brain's seven-heading page template unchanged and deviates on exactly two axes — status vocabulary and domain vocabulary — both forced by its purpose as a published graph demo rather than a private notebook.

## Concepts

- [[adkar-for-ai|ADKAR Applied to AI]] — Awareness, Desire, Knowledge, Ability, Reinforcement — mapped onto AI adoption, with high shadow-AI usage as the diagnostic signal of a Desire-stage failure.
- [[ai-acceptable-use-policy|AI Acceptable Use Policy]] — Approved tools list, data classification rules, output verification requirements, violation consequences, quarterly review — required before broad rollout, and useless against AI that arrives through vendors.
- [[ai-adoption-barriers|Barriers to AI Adoption]] — OECD's D4SME survey ranks maintenance cost (40%) and lack of training time (39%) as the top SME barriers, with management and employee resistance last at 7% and 6% — a finding the playbook's own change-management sections contradict outright.
- [[ai-budget-allocation|Where the AI Budget Goes]] — Customer service takes 29% of SMB AI budget and internal knowledge/RAG takes 8% — the allocation data is the best-sourced finding in the spend section.
- [[ai-governance-for-lean-orgs|AI Governance for Lean Organizations]] — Governance is the mechanism preventing shadow AI breaches, regulatory non-compliance, and hallucination-driven business risk — the question isn't whether to have it, but what the minimum viable structure is.
- [[ai-hallucination-risk|AI Hallucination Risk]] — "Confidently stated but false content" — rates run from 0.7% on the best model to 29.9% on the worst, and RAG-grounded legal tools still hallucinate 17–33% of the time.
- [[ai-in-traditional-industries|AI in Traditional Industries]] — Manufacturing, logistics, professional services, and healthcare admin carry high tribal knowledge and legacy ERP estates — which makes AI both more valuable and harder, and makes the Second Brain the natural first use case.
- [[ai-literacy|AI Literacy]] — 4–8 hours across 2–4 sessions covering foundations, prompting, risks, hands-on practice on real work, and a personal use-case map — with leaders trained first or in parallel, never last.
- [[ai-skills-gap|The AI Skills Gap]] — Mid-market firms are structurally outbid for AI specialists, so the winning response is AI literacy across existing staff rather than AI specialization — yet only half of AI decision-makers train non-technical employees at all.
- [[ai-spending-benchmarks|AI Spending Benchmarks]] — BCG's 1.7%-of-revenue benchmark is well-corroborated across three sources; the sector splits and per-employee figures built on top of it are not.
- [[build-vs-buy-mid-market|Build vs. Buy for Mid-Market]] — Buy the commodity layer, build the proprietary knowledge layer — a sound recommendation resting on a comparison table that doesn't appear in the source it's cited to.
- [[capability-ambition-gap|Capability-Ambition Gap]] — A named concept the playbook attributes in quotation marks to a 2025 academic study that, verified against its full text, does not contain the word "ambition" even once.
- [[data-quality-readiness|Data Quality and Infrastructure Readiness]] — The most common AI failure mode isn't picking the wrong tool — it's starting with data that isn't ready, and the Karpathy approach tolerates messy formats without fixing knowledge that was never captured.
- [[digital-second-brain|Digital Second Brain]] — A living, AI-maintained knowledge system that captures, organizes, cross-links, and makes queryable all institutional knowledge — externalized organizational memory that doesn't leave when employees do.
- [[five-human-postures-toward-ai|Five Human Postures Toward AI]] — WEF identifies five employee archetypes — enthusiasts, curious, cautious, sceptics, opposed — which the playbook renames to enthusiasts, pragmatists, skeptics, anxious, resisters, scrambling two of them in the process.
- [[four-pillar-governance|Four-Pillar Governance Framework]] — Use Case Intake, Model Risk Management, Vendor Oversight, and Incident Response — the governance structure for a mid-market firm with no dedicated compliance team.
- [[generic-solutions-mismatch|Why Generic AI Solutions Don't Fit]] — 27% of SMEs aware of AI solutions but not using them say available support "was not adapted to their needs" — the core argument for anchoring AI to your own knowledge rather than deploying a generic assistant.
- [[hallucination-governance-metrics|Hallucination Governance Metrics]] — Hallucination@k, source attribution rate, abstention rate, escalation rate, and incident density — five leadership-dashboard metrics, none of which any source reports anyone actually running.
- [[hallucination-mitigation|Hallucination Mitigation Architecture]] — RAG grounding, citations-or-silence, human-in-the-loop for high-stakes, sandboxed agents, and cross-model validation — five controls, none of which eliminate the problem.
- [[karpathy-llm-wiki-method|Karpathy LLM Wiki Method]] — A six-stage pipeline where the LLM reads raw sources once and compiles a structured markdown wiki it then maintains — the human curates and reads, the LLM writes.
- [[km-tool-landscape|Knowledge Management Tool Landscape]] — Glean, Guru, Notion AI, Confluence, Slab, Tettra, Microsoft Viva, or a DIY Karpathy wiki — the pricing table checks out against its source, the recommended stacks don't.
- [[knowledge-attrition-cost|The Cost of Knowledge Attrition]] — "$300,000 lost per departing senior employee" is the figure that makes the Second Brain business case close within a year — and it does not appear in the source it's attributed to.
- [[leadership-modeling-imperative|The Leadership Modeling Imperative]] — Supervisors who co-present AI outputs with their team rather than delegating the AI interaction measurably reduce resistance — the highest-leverage single variable in AI adoption.
- [[lean-ai-center-of-excellence|Lean AI Center of Excellence]] — Five components, 3–5 people, three use cases, and a counter-intuitive 40/30/30 split across governance, education, and delivery — with an end date from day one.
- [[mid-market-ai-paradox|The Mid-Market AI Paradox]] — Mid-market firms generate enough institutional knowledge and operational complexity to justify serious AI investment, but are too lean to staff dedicated AI teams — creating both the vulnerability and the opportunity.
- [[ninety-day-governance-launch|The 90-Day Governance Launch Plan]] — Days 1–30 inventory and draft the AUP, 31–60 provision accounts and train, 61–90 audit and report — the playbook's most immediately actionable section.
- [[rag-vs-llm-wiki|RAG vs. LLM Wiki]] — "RAG retrieves. A wiki compounds." — the playbook's central architectural claim, which its own primary source contradicts and which no enterprise deployment in the corpus tests.
- [[retrieval-augmented-generation|Retrieval-Augmented Generation (RAG)]] — An architecture where the LLM retrieves relevant chunks from an index at query time before generating — the industry default for enterprise knowledge, and the primary hallucination control.
- [[roi-measurement-problem|The ROI Measurement Problem]] — 94% of enterprises will keep spending on AI even without measurable ROI — which reflects both conviction and an absence of measurement discipline, since pre-AI baselines are almost never captured.
- [[shadow-ai|Shadow AI]] — Unauthorized employee AI use outside IT visibility — ~18,000 prompts/month per org with 47% on personal accounts, 223 policy violations/month, and +$670,000 in breach costs where it's present.
- [[three-layer-reference-architecture|Three-Layer Reference Architecture]] — Knowledge sources at the bottom, knowledge intelligence in the middle, AI interaction on top — the playbook's reference design for a mid-market Digital Second Brain.
- [[three-tier-sme-governance|Three-Tier SME Governance Framework]] — Basic ($0/mo, 2 weeks, Notion + Sheets), Standard (~$200/mo, 4 weeks, ISO 42001 Lite), Premium ($1,500+/mo, 8+ weeks, full ISO 42001) — with Standard the right starting point for most $50M–$200M firms.
- [[transformative-integration-gap|The Transformative Integration Gap]] — Only 8% of businesses reach "transformative" digital integration and only 6% of AI users see meaningful bottom-line impact — breadth of adoption has decoupled from depth of value.
- [[use-case-prioritization-matrix|Use Case Prioritization Matrix]] — Business impact against organizational feasibility: quick wins, strategic priorities, traps, and rejects — with "traps" (easy, low-return) the quadrant that quietly consumes lean-team capacity.
- [[vendor-lock-in-and-tco|Vendor Lock-in and TCO Underestimation]] — SaaS AI looks cheap per seat and hides cost in integration, drift monitoring, prompt maintenance, and compliance tooling — 47% of AI budgets exceed estimates, and 80–85% of enterprises miss infrastructure forecasts by more than 25%.

## Entities

- [[andrej-karpathy|Andrej Karpathy]] — Author of the LLM Wiki gist that the playbook's entire thesis rests on — and which the playbook never cites.
- [[bcg|Boston Consulting Group]] — Publisher of AI Radar 2026, the source of the 1.7%-of-revenue AI spending benchmark — and of the 94%-will-keep-spending / 6%-see-impact pair.
- [[confluence-atlassian-intelligence|Confluence + Atlassian Intelligence]] — Wiki plus AI at $5.75–11/user plus an AI add-on — the cheapest per-seat option, and the default for anyone already running Jira.
- [[datagrail|DataGrail]] — Publisher of the 2026 Privacy & AI Trends Report and source of the 63.6%-of-AI-vendors-hide-subprocessors figure.
- [[eu-ai-act|EU AI Act]] — Prohibitions in force since February 2025, high-risk requirements enforceable from August 2026, penalties up to €35 million or 7% of global annual revenue.
- [[ey|EY]] — Credited by the playbook with the finding that firms allocating ≥25% of IT budget to AI will rise from 27% to 52% within two years — a figure that checks out, from a survey that's never cited.
- [[forrester|Forrester Research]] — Source of the finding that only half of AI decision-makers train non-technical employees — a figure that grew just 4 percentage points between 2024 and 2025.
- [[gartner|Gartner]] — Source of the $2.52T global AI spending forecast for 2026, the 12–15%-of-SMB-software-spend-by-2027 projection, and the 47%-of-AI-budgets-overrun figure.
- [[glean|Glean]] — Enterprise AI search with 100+ connectors at $40–100/user/yr — the heavyweight option, priced for 500+ employee orgs.
- [[guru|Guru]] — Modern wiki at $15–30/user/yr whose verification workflows and staleness detection are the only commercial implementation of the maintenance layer everything else in this vault hand-waves.
- [[ibm|IBM]] — Publisher of the Cost of a Data Breach Report, source of the +$670,000 shadow-AI breach premium and the 65%-more-PII figure.
- [[iso-42001|ISO/IEC 42001]] — The AI Management System standard underlying the playbook's three-tier governance framework — full conformance at 8+ weeks and $1,500+/month, "Lite" at 4 weeks and $200.
- [[mckinsey|McKinsey]] — Source of the finding that change management and organizational silos are the #1 barrier to AI adoption, outranking technology gaps.
- [[netskope|Netskope]] — Publisher of the Cloud and Threat Report supplying every shadow-AI usage figure in the playbook — and a vendor of the CASB tooling its own data recommends.
- [[nist|NIST]] — Source of the definition the playbook uses for hallucination — "confidently stated but false content" — and of the AI Risk Management Framework.
- [[notion-ai|Notion AI]] — Workspace plus AI at $20 + $10 AI/user/month — the low-migration-friction option for teams already living in Notion.
- [[obsidian|Obsidian]] — The markdown IDE that serves as the visualization layer for a Karpathy wiki — free, local, with backlinks and a graph view.
- [[oecd|OECD]] — The Organisation for Economic Co-operation and Development, whose D4SME survey is the playbook's primary source for global SME AI adoption rates and barriers.
- [[prosci|Prosci]] — Originator of the ADKAR model — Awareness, Desire, Knowledge, Ability, Reinforcement — the change framework the playbook maps onto AI adoption.
- [[pwc|PwC]] — Source of the ~62% wage premium for AI-skilled workers — up from 57% the prior year — the playbook's best lever for converting employee anxiety into motivation.
- [[rsm|RSM]] — Publisher of the 2025 Middle Market AI Survey (US & Canada) — the playbook's only mid-market-specific adoption data.
- [[tiago-forte|Tiago Forte]] — Author of "Building a Second Brain" and the capture-organize-distill-express methodology the playbook names as one of two founding traditions — and then never returns to.
- [[vectara|Vectara]] — Named in Appendix B as a recommended primary source for hallucination rates, with no reference, no URL, and no citation anywhere in the playbook.
- [[world-economic-forum|World Economic Forum]] — Publisher of the five-archetype AI readiness research and the frontstage-compliance/backstage-resistance finding the playbook omits.

## Sources

- [[145-ai-laws-2025|145 AI Laws Were Passed in 2025]] — The regulatory-count source — and the one that identifies vendor-embedded shadow AI as a distinct risk the playbook conflates with the employee-initiated kind.
- [[ai-coe-should-work-itself-out-of-a-job|Your AI CoE Should Work Itself Out of a Job]] — The dissolution argument — an 18-month CoE with an end date from day one — and the source of a shadow-AI statistic the playbook never connects to its own shadow-AI section.
- [[ai-coe-without-hiring-an-army|How to Build an AI CoE Without Hiring an Army]] — The load-bearing source for the playbook's entire Section 5 — five components, 40/30/30, and the four-quadrant matrix, all reproduced faithfully.
- [[ai-cost-statistics-2026|AI Cost Statistics 2026]] — Independently corroborates the 1.7% benchmark and the 27%→52% IT-budget shift — and carries three figures that gut the playbook's productivity math.
- [[ai-enterprise-km-guide-2026|AI Enterprise Knowledge Management Complete Guide 2026]] — The tool pricing table the playbook reproduces accurately — and the source of the 1.8-hours/day figure it quietly discards in favor of a bigger one.
- [[ai-governance-challenges-shadow-ai|AI Governance Challenges: Shadow AI, Rules & Readiness]] — Carries the EU AI Act enforcement timeline and penalties the playbook cites it for and then doesn't report — €35M or 7% of global revenue, enforceable August 2026.
- [[ai-governance-framework-for-smbs|AI Governance for SMBs: ISO 42001 Framework]] — The three-tier governance table the playbook reproduces — from a July 2025 blog post by "admin", written before the EU AI Act's high-risk provisions took effect.
- [[ai-hallucinations-in-the-enterprise|AI Hallucinations in the Enterprise]] — Source of the 44%-of-manufacturing-decision-makers figure, the 17–33% RAG legal hallucination rate, and the 2030 responsible-AI projection.
- [[ai-implementation-cost-2026|AI Implementation Cost 2026: SaaS vs Custom vs API-First]] — Three-model cost breakdown with the hidden-cost line items — and the actual figures that contradict the playbook's build-vs-buy table.
- [[ai-investments-surge-2026-bcg|AI Investments Set to Surge in 2026: BCG Report]] — The one reference in the corpus that could not be captured — an MSN syndication of BCG coverage, redundant with three sources that were.
- [[ai-literacy-new-workplace-skill|AI Literacy: The New Workplace Skill]] — Argues AI literacy is four distinct competencies calibrated by role — and names output verification as the least visible, most consequential gap.
- [[ai-literacy-training-explained|AI Literacy Training Explained]] — The source of the playbook's 4–8 hour AI literacy curriculum and the train-leaders-first rule.
- [[ai-skills-gap-widens|AI Skills Gap Widens as Training Lags Behind]] — News coverage of a Forrester report: only half of AI decision-makers train non-technical employees, and that figure moved just 4 points in a year.
- [[ai-spending-by-industry-2026|AI Spending by Industry 2026]] — The per-employee spend source — where four of the playbook's five cited figures don't match, and the fifth doesn't exist.
- [[ai-use-cases-and-trends-2026|AI Use Cases: An In-Depth Trend Overview for 2026]] — Source of the 70%-of-logistics-companies figure — and not the source of the 20–40% downtime figure the playbook attributes to it.
- [[bcg-revenue-benchmark-post|How Much Should Your Mid-Size Enterprise Be Spending on AI?]] — LinkedIn post carrying BCG's 1.7%-of-revenue benchmark alongside the pair that defines the corpus: 94% will keep spending regardless, 6% see meaningful impact.
- [[best-ai-for-knowledge-management-2026|Best AI for Knowledge Management in 2026]] — The source of the playbook's critical success factors — capture before search, verify before publishing, respect permissions — and of the best diagnosis in the corpus of why knowledge management failed.
- [[build-a-second-brain-step-by-step|Build a Second Brain: Karpathy's LLM Wiki Method, Step by Step]] — Three-layer architecture (sources, wiki, schema) with four slash-command operations — capture, sync, lint, digest — and the 100-articles/400,000-words figure.
- [[build-vs-buy-ai-framework|Build vs Buy AI: Decision Framework for Mid-Market]] — Cited for the playbook's build-vs-buy table, which it doesn't contain — its actual framework compares delivery models, not build against buy.
- [[change-management-ai-adoption-playbook|Change Management for AI Adoption: A 2026 Playbook]] — The ADKAR-for-AI source — and the one that names high shadow-AI usage as the warning sign of a Desire-stage failure.
- [[datagrail-privacy-ai-trends-2026|Privacy and AI Trends Report 2026]] — DataGrail's report and the source of the 63.6%-of-AI-vendors-hide-subprocessors figure — the evidentiary basis for vendor oversight.
- [[five-faces-of-ai-readiness|The 5 Faces of Human Readiness for AI Adoption]] — The WEF's actual five archetypes — enthusiasts, curious, cautious, sceptics, opposed — and the frontstage/backstage resistance finding the playbook drops entirely.
- [[from-information-silos-to-enterprise-brain|From Information Silos to Enterprise Brain]] — The 312%-ROI case study — a 200-employee tech company, with no author, no date, and a single data point generalized across the playbook.
- [[g7-ai-adoption-by-smes|AI Adoption by SMEs (G7 Report, Mila)]] — The playbook's data-readiness citation — a 9MB PDF with no extractable text layer, captured only through what the playbook itself quotes from it.
- [[gartner-ai-spending-forecast-2026|Gartner's $2.52T AI Spending Forecast]] — Coverage of Gartner's $2.52T global AI spending forecast for 2026 — up 44% YoY — framed as negotiation leverage rather than prediction.
- [[indian-ceos-doubling-down-on-ai|Indian CEOs Are Doubling Down on AI Investments]] — Moneycontrol's coverage of BCG's AI Radar 2026 — corroborating the 1.7% benchmark and naming the report the playbook calls "BCG Radar 6".
- [[karpathy-llm-wiki-to-working-second-brain|From Karpathy's LLM Wiki to a Working Second Brain]] — The only first-hand practitioner account in the corpus — a cloud architect's implementation, self-rated 7/10, with a diff-and-approve write workflow.
- [[karpathy-second-brain-how-to-build-it|How to Build Karpathy's Second Brain]] — An anonymous Facebook group post — and the actual source of the playbook's directory structure, the Karpathy quote, and its gist metrics.
- [[llm-knowledge-bases-karpathy|LLM Knowledge Bases: Karpathy's Self-Improving Second Brain]] — The playbook's primary source for the Karpathy method — and the one that explicitly says the method is for individuals and small teams, while organizational collections still require RAG.
- [[managing-ai-hallucination-risk|Managing AI Hallucination Risk]] — The least conflicted hallucination source in the corpus — and the likely unnamed conduit for Vectara's leaderboard figures.
- [[overcoming-ai-resistance|Overcoming AI Resistance]] — The playbook's route to McKinsey's "change management is the #1 barrier" finding — and the source of an 18%-adoption figure that contradicts the playbook's own Section 1.
- [[rag-knowledge-management-roi|RAG Knowledge Management — 300-500% ROI]] — The playbook's ROI anchor — 300–500% first-year returns, 2.5 hours/day searching, 70% knowledge preservation — from a consultancy marketing page with no methodology, and missing the $300K figure attributed to it.
- [[resistant-employees-know-why|Your Resistant Employees Know Why Your AI Adoption Is Failing]] — Carries the 95%-of-AI-pilots-fail finding and the 76%-vs-31% executive perception gap — both absent from the playbook, which cites this source for a single clause.
- [[rsm-middle-market-ai-survey-2025|AI Adoption by Mid-Market Firms (RSM 2025 Survey)]] — LinkedIn summary of RSM's 2025 Middle Market AI Survey: 78–92% of mid-sized firms use AI, 85% say it exceeded expectations, 54% found deployment harder than expected.
- [[shadow-ai-hidden-risk-enterprise|Shadow AI — The Hidden Risk in Your Enterprise]] — The source behind the playbook's best-evidenced section — every shadow AI figure in Section 4.5 traces here, and through here to Netskope and IBM.
- [[smb-technology-spending-2026|SMB Technology Spending Statistics 2026]] — SMB IT budget data — AI at 5% today, Gartner forecasting 12–15% of SMB software spend by 2027 — plus the 3.4%-of-revenue figure that breaks the playbook's arithmetic.
- [[sme-ai-adoption-oecd-insights|SME AI Adoption in 2025: Key Insights from OECD Research]] — Vendor summary of OECD D4SME research: 39% of SMEs use AI, only 8% reach transformative integration, and cost — not resistance — dominates the barrier list.
- [[state-of-smb-ai-automation-2026|State of SMB AI Automation 2026]] — 312 SMBs surveyed with disclosed methodology and no vendor sponsorship — the most trustworthy dataset in the playbook, and the source of the 8%-to-internal-knowledge figure.
- [[the-67-billion-warning|The $67 Billion Warning]] — The origin of the $67.4B hallucination-loss figure — attributed to "AllAboutAI, 2025" with no methodology, making the playbook's citation third-hand.
- [[the-new-normal-ai-adoption-in-smes|The New Normal: The Status Quo of AI Adoption in SMEs]] — A systematic literature review of 106 articles organized by the TOE model — and the paper the playbook credits with a "capability-ambition gap" it does not contain.
- [[turning-institutional-knowledge-into-ai-assets|Turning Institutional Knowledge into Strategic AI Assets]] — RAG guide arguing institutional knowledge needs activation, not creation — the source of the playbook's best strategic framing.
- [[vanilla-graph-agentic-rag|How Enterprise Teams Use Vanilla, Graph, and Agentic RAG]] — The RAG maturity path — Vanilla → Graph → Agentic — and the source of the 141%-over-3-years figure the playbook uses to argue against RAG.
- [[why-businesses-struggled-with-ai-2024|Why Businesses Struggled with AI in 2024]] — A January 2025 retrospective on 2024's AI struggles — data infrastructure, talent, regulation, unclear ROI — superseded by every newer adoption source in the vault.
