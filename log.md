# log

Append-only record of every ingest/lint operation. Rotates into `log/YYYY-MM.md` on month rollover —
this file should only ever hold the current month's entries.

Format: `## [YYYY-MM-DD] <ingest|lint> | <summary>`

## [2026-07-15] ingest | Seed ingest: playbook + 43 references → 110 wiki pages

**Source:** *AI Adoption in Mid-Market Enterprises: The Digital Second Brain Playbook* (user-supplied),
archived to `raw/2026-07/`. Original in `Downloads/` never modified.

**Captures — 43/43 references, 44 raw files:**

| Method | Count | Notes |
|---|---|---|
| `webfetch-extract` | 37 | Structured extraction, not verbatim clippings |
| `playwright-fulltext` | 4 | refs 5, 28, 36, 42 — WebFetch 403/blocked |
| `partial` | 1 | ref 12 (Mila G7 PDF) — no text layer, no extraction tooling available |
| `unreachable` | 1 | ref 29 (MSN) — JS-gated; redundant with refs 4/28/31 |

**Compiled:** 110 pages — 43 `sources/`, 35 `concepts/`, 24 `entities/`, 8 `synthesis/`.
Status: 88 `active`, 20 `revisiting`, 2 `dormant`.

**Graph safety verified:** 1,193 wikilinks in `## Related` / `## Referenced By`, **0 dangling**.
0 frontmatter problems, 0 missing headings, all `status` values in the recognized vocabulary.
Node registry frozen before writing (`plans/node-registry.md`) — the only way to guarantee closure,
since the graph builder drops dangling links silently.

**Slug collisions with sibling `second-brain` vault (shared Obsidian graph at `GitFiles/`):** none.
Two deliberate renames: `karpathy-llm-wiki-method` (theirs: `llm-wiki-pattern`) and
`wiki-schema-design-for-ai-adoption-wiki` (theirs: `wiki-schema-design-for-second-brain`).

**Contradictions preserved, not resolved** (per ingest step 6). The significant findings from
verifying every reference against the playbook's claims:

- **ref [^6] contradicts the playbook's thesis.** Its primary Karpathy source says the method
  "scales effectively for individuals and small teams" and that "organizational collections require
  traditional RAG systems". The playbook's central argument is the opposite, and never mentions this.
- **"Capability-ambition gap" (Section 1.2) is not in the cited paper.** Verified against the full
  108,008-character text of Schwaeke et al.: "ambition" appears 0 times, "digital security" 0 times.
- **Four of five per-employee spend figures (Section 6.5) don't match ref [^33].** Only professional
  services matches. The section's "$360K–$700K" recommendation is derived from the wrong ones.
- **The five WEF postures (Section 8.4) are renamed and two are mismapped.** "Anxious" is the WEF's
  *opposed*; "Skeptics" is its *sceptics*, not its *cautious*. The *cautious* category vanishes.
- **"BCG Radar 6" appears to be an invented title.** The report is *AI Radar 2026*.
- **$300,000/departing-employee (Section 2.4) is not in ref [^10].** It anchors the ROI case.
- **1.8 vs. 2.5 hours/day searching** — refs [^40] and [^10] disagree by ~39%; only the larger is used.
- **Vendor-embedded vs. employee-initiated shadow AI** (refs [^21] and [^26]) are conflated.
- **MIT NANDA's 95%-of-pilots-fail** appears in refs [^37] and [^43] and nowhere in the playbook.

Recorded at `wiki/synthesis/attribution-problems-in-the-playbook.md`.

**What checks out:** the shadow AI section (4.5) is exact against Netskope/IBM; the governance tiers
(4.2), lean CoE model (5.1–5.4), tool pricing (10.1), and critical success factors (12.2) all
reproduce their sources faithfully. The 1.7%-of-revenue benchmark is corroborated three ways.
