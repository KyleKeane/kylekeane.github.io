# _research/ — source material, not published

This folder holds the source documents the website is built from. **None
of these files are published.** Jekyll ignores any top-level directory
that starts with an underscore, and `_research/` is also listed in
`_config.yml`'s `exclude:` block as belt-and-suspenders.

## Files

| File | What it is |
|---|---|
| `seed.md` | The spine. A single unified markdown source whose `##` sections map 1:1 to the site's pages. The starting point for any content extraction. |
| `claude-cv-verification.txt` | A fact-checked verification of Kyle's CV — citation counts, source-by-source confirmation, gap analysis. Best for adding sourced detail to existing pages. |
| `website-updates.txt` | Kyle's 2024–2025 Bristol-era updates: new course (COMS30054), recent talks, recent publications. |
| `recent-records.txt` | Small record-system extract with one or two newer items not yet in the other files. |

## When to use which

See [`docs/content-sources.md`](../docs/content-sources.md) for the
recommended merge order and what each source is best at filling in.
