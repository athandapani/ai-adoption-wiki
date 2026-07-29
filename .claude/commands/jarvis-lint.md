---
description: Report-only health check of the wiki — contradictions, stale claims, orphans, graph safety
---

Run a health check over `wiki/`. **Report, don't fix — nothing changes as a result of this
command** except the `log.md` entry at the end.

Check five categories:

1. **Contradictions** — pages making claims that conflict with each other. On this subject the
   live tensions are known and expected; flag *new* ones, and flag any that have been resolved
   away without being recorded in a `## Counter-arguments & Data Gaps` section. Known standing
   tensions (these are features, not defects):
   - "RAG retrieves, a wiki compounds" vs. the 300–500% RAG-ROI claims
   - BCG's "94% will keep spending regardless of ROI" vs. "only 6% see meaningful impact"
   - OECD's "cultural resistance is a minor barrier" (6–7%) vs. McKinsey's "change management
     is the top barrier"

2. **Stale claims** — this vault is dense with dated statistics. Flag any page whose central
   claim is tied to a survey or forecast now more than ~18 months old, and any `status: active`
   page whose source predates a known newer edition. Candidates for `status: revisiting`.

3. **Orphan pages** — pages with no inbound links from any `## Related` / `## Referenced By`
   section. These are invisible in the graph demo (`showOrphans: false` in the shared Obsidian
   graph config, and they float unconnected in `wiki-graph-explorer`).

4. **Graph safety** — the failure mode that produces no error message. Report:
   - any page whose frontmatter fails to parse, or lacks `title` / `tags`
   - any explicitly-set `status` value outside `active` / `revisiting` / `dormant` (an absent
     `status` is not an error — the parser defaults it to `"unknown"` — but this vault should
     still set it explicitly)
   - any **dangling wikilink** — a `[[target]]` anywhere in the body with no matching filename
     or frontmatter title, case-insensitively (silently dropped by the graph builder, logged at
     DEBUG only)
   - any ambiguous wikilink — a `[[target]]` matching more than one page's filename/title,
     which resolves to whichever match the vault walk encounters first rather than a specific
     intended page
   - any filename collision with the sibling `second-brain` vault (shared Obsidian graph)

   Cross-check by running:
   `cd ../wiki-graph-explorer && npm run build:graph -- --vault ../ai-adoption-wiki/wiki --out local-build`
   and comparing the reported node/edge counts against the page count in `index.md`.

5. **New-article candidates** — concepts referenced repeatedly across pages but with no page of
   their own, and `raw/` sources not yet represented in `wiki/`.

Finish by appending to `log.md`:
`## [YYYY-MM-DD] lint | <N contradictions, N stale, N orphans, N graph-safety issues, N candidates found>`
