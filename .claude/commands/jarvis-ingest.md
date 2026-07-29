---
description: Ingest new raw sources into the wiki, with a confirm step before anything is written
---

Run the ingest workflow for this ai-adoption-wiki vault:

1. **Scan** `raw/` at its **root only** (files not yet inside a `<YYYY-MM>/` subfolder).
   Cross-check against `log.md` — anything already logged is done, skip it.

2. **Public-content check**: this vault is published. Before processing any file, scan for
   anything private, personal, credential-like, or `second-brain`-derived. If found, skip that
   file and warn the user explicitly — it belongs in `second-brain`, not here.

3. **Type-specific extraction** — read each remaining file according to its type:
   - **Article/clipping**: lead with the abstract/conclusion; extract the specific, falsifiable
     claim(s). Record the publisher and publication date — they become the `entities/` link and
     the staleness signal.
   - **Report/whitepaper (OECD, BCG, Gartner…)**: extract the headline statistic, the sample
     size and methodology, and the date. Preserve quantified metrics **exactly** as written —
     never round or paraphrase numbers.
   - **Playbook/synthesis document**: extract each section as a candidate `concepts/` page and
     each cited reference as a candidate `sources/` page.

4. **Draft** (do not write yet) every `wiki/` page this batch would create or update, across
   `sources/entities/concepts/synthesis`, using this template:

   ```markdown
   ---
   title:
   source:                  (sources/ pages only — path into raw/)
   domain: []               (adoption | second-brain | governance | spend | change-management | risk | tooling | industry | cross-domain)
   status: active           (active | revisiting | dormant)
   superseded_by:           (if status: dormant)
   created:
   tags: []
   ---

   ## TLDR
   (one precise, specific sentence)

   ## Metadata
   - source:
   - created:
   - category:

   ## Related
   - [[kebab-case-slug|Display Title]] — optional relation hint (contradicts / supersedes / depends-on)

   ## Referenced By
   - [[kebab-case-slug|Display Title]]

   ## Body
   (paraphrase-first; short attributed quotes under ~15 words allowed when precise)

   ## Counter-arguments & Data Gaps
   (strongest opposing view; what this source doesn't address; what would change this conclusion)

   ## Notes
   _(hand-written notes — preserved across re-ingestion)_
   ```

   Filenames are kebab-case slugs of the title. Titles must be globally unique across all of
   `wiki/` (not namespaced per folder) — check before creating a new page; if a page with that
   title already exists, update it instead.

   **Also check for collisions against the sibling `second-brain` vault** — `.obsidian/` sits at
   the `GitFiles` root, so both vaults share one Obsidian graph and `[[slug]]` resolves
   vault-wide. A collision silently cross-links the two.

   Cross-link new pages to existing related concepts/entities wherever genuinely relevant.

5. **Graph-safety check** — `wiki-graph-explorer` parses this vault and drops bad nodes/edges
   silently. Before drafting is done, confirm for every page:
   - frontmatter parses and carries `title` and `tags` (`status` is optional to the parser but
     should still be set explicitly here — see the mapping in "Deviations from `second-brain`'s
     schema" below)
   - if set, `status` is one of `active` / `revisiting` / `dormant`
   - every `[[target]]` — anywhere in the body, not just under `## Related`/`## Referenced By` —
     resolves case-insensitively to a real filename or another page's frontmatter `title`
   - `## Related` / `## Referenced By` are still used for structural cross-referencing even
     though the parser no longer requires it (editorial convention, not a parser requirement)

6. **Contradiction check**: compare drafted content against existing wiki pages. If a new page
   contradicts an existing one, either (a) mark the *older* page `status: dormant` with
   `superseded_by: [[new-page]]`, or (b) if it's a matter of perspective rather than
   supersession, add the tension to the new page's `Counter-arguments & Data Gaps` section.
   Never silently overwrite a conflicting claim — on this subject the disagreements between
   sources are the most interesting content in the vault.

7. **Stop and present a tabulated summary** of everything proposed: new pages, updated pages,
   any pages being marked dormant, and any contradictions flagged. Wait for explicit
   confirmation before writing anything.

8. **On confirmation**:
   - Write all drafted/updated pages. If updating an existing page, preserve its current
     `## Notes` section verbatim.
   - Update `index.md` with a one-line TLDR entry per new/changed page, grouped by folder
     (respect the ~200-line ceiling — if exceeded, split into
     `index/{sources,entities,concepts,synthesis}.md` and turn `index.md` into a table of
     contents).
   - Append an entry to `log.md`: `## [YYYY-MM-DD] ingest | <summary of what was processed>`.
     If `log.md` has entries from a prior month, rotate those into `log/YYYY-MM.md` first and
     leave a one-line pointer.
   - Archive each successfully processed raw file: add `ingested: true` and
     `ingested_date: YYYY-MM-DD` to its frontmatter, then move it from `raw/` into
     `raw/<YYYY-MM>/`, named by the month ingestion happened.
   - Re-run the graph build to confirm node/edge counts moved as expected:
     `cd ../wiki-graph-explorer && npm run build:graph -- --vault ../ai-adoption-wiki/wiki --out local-build`

9. Do not touch anything already inside a `<YYYY-MM>/` subfolder — there is no automatic
   re-ingest on edited raw files in this version. To force reprocessing, the user moves the file
   back to `raw/` root and clears its `ingested` flag manually.
