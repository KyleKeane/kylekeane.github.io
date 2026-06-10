# CLAUDE.md — guide for Claude Code sessions

You're working on Dr. Kyle Keane's personal website. Read this file first.
It exists because Claude Code sessions sometimes lose their connection to
the GitHub MCP and have to restart, so the repo itself is the canonical
source of truth for the project plan and procedures.

[`README.md`](README.md) is the orientation document for human
contributors — stack, build flow, common-task recipes (add a page,
retire a page, edit the nav, change styles, edit the header social row).
Read it for anything the file below doesn't cover.

## Who Kyle is and why this matters

Kyle is **blind and uses a screen reader.** Every decision in this repo
flows from that. The site must be:

- **Plain semantic HTML** rendered from plain markdown
- **One H1 per page** (the layout renders it from `page.title`); H2s and
  below come from the markdown
- **Sequential heading hierarchy** — never skip a level (no H2 → H4)
- **Descriptive link text** — never `click here`, `read more`, or a bare URL
- **Alt text on every image** that describes what the image conveys, not
  what it depicts decoratively
- **No JavaScript** unless absolutely necessary — there is none today,
  keep it that way unless Kyle asks
- **No frameworks**, **no remote themes other than Minima**, **no plugins
  outside the GitHub Pages whitelist**
  (<https://pages.github.com/versions/>)

The accessibility checklist for a new page is in
[`docs/style-guide.md`](docs/style-guide.md). Use it.

## The stack (don't change this casually)

- **GitHub Pages-native Jekyll.** No Gemfile, no Bundler, no custom build
  step. The deploy workflow at
  `.github/workflows/jekyll-gh-pages.yml` runs on push and uses
  `actions/jekyll-build-pages` to build. If you find yourself wanting to
  add a Gemfile or a custom plugin, stop and ask Kyle first.
- **Theme:** Minima, imported via `@import "minima"` in
  `assets/css/style.scss`. The custom HTML in `_layouts/default.html`
  is what actually renders pages — Minima only contributes typography
  defaults via the SCSS import.
- **Custom CSS:** `assets/css/style.scss` — 150% base font, dark-mode
  support via `prefers-color-scheme`, focus-visible skip-link styling.

## File layout

```
.
├── index.md                        # About (home). nav 1, permalink: /
├── philosophy.md                   # nav 2, permalink: /philosophy.html
├── engage.md                       # nav 3, permalink: /engage.html
├── upcoming.md                     # nav 4, permalink: /upcoming.html
├── research.md                     # nav 5, permalink: /research.html
├── teaching.md                     # nav 6, permalink: /teaching.html
├── creative.md                     # nav 7, permalink: /creative.html
├── cv.md                           # nav 8 — unified CV generated from _cv/, permalink: /cv.html
├── cv-academic.md, cv-educator.md, # persona-filtered CV views generated
├── cv-creative.md, cv-advocacy.md  # from the same _cv/ entries; linked
│                                   # from cv.md, NOT in the nav
├── _cv/                            # CV database: one markdown file per
│   │                               # entry, persona-tagged; cheat-sheet
│   │                               # in _cv/README.md
│   ├── roles/ affiliations/ publications/ grants/ grant-support/
│   └── awards/ scholarships/ press/ skills/ events/
├── _includes/cv-sections.html      # Liquid rendering the _cv/ entries
├── work.md, publications.md, funding.md, skills.md, media.md,
│                                   # 11 redirect-only stubs using
├── speaking.md, events.md, exhibitions.md, performances.md,
│                                   # _layouts/redirect.html; each forwards
├── advising.md, advocacy.md        # to one of the 8 pages above
├── _config.yml                     # title, description, plugins, exclude
├── _layouts/default.html           # main page layout
├── _layouts/redirect.html          # redirect-stub layout
├── _includes/header.html           # skip link, site title, nav
├── assets/css/style.scss           # custom CSS
├── _briefing/                      # source material; NOT published
│   ├── README.md
│   ├── seed.md                     # the spine — original unified outline
│   ├── claude-cv-verification.txt  # fact-checked CV verification
│   ├── website-updates.txt         # 2024–2025 Bristol-era updates
│   ├── recent-records.txt          # recent publication / poster records
│   ├── performances-and-events.md  # artistic-practice source material
│   └── external-research-brief.md  # external-research evidence brief
├── docs/                           # project docs; NOT published
│   ├── plan.md                     # phased roadmap with checkboxes
│   ├── open-questions.md           # historical record of resolved questions
│   ├── open-items.md               # active backlog of placeholders / gaps
│   ├── content-sources.md          # what to merge from each _briefing/ file
│   ├── briefing-audit.md           # Phase 2.5 briefing-folder audit
│   └── style-guide.md              # accessibility + markdown conventions
├── README.md                       # project overview
├── CLAUDE.md                       # this file
└── .github/workflows/              # deploy workflow
```

`_briefing/` and `docs/` start with characters that Jekyll ignores by
default (the leading underscore, in the case of `_briefing/`) and are
explicitly listed in `_config.yml`'s `exclude:` block as well. They will
not be served.

## Adding or editing a page

Front-matter template for any new page:

```yaml
---
layout: default
title: <Section title shown as H1 and in nav>
permalink: /<slug>.html
description: <One-sentence summary used in <meta name="description">>
nav_include: true
nav_order: <integer; lower numbers come first in the nav>
---
```

Then write the body in markdown. **Do not write your own H1** in the body —
the layout produces it from `title`. Start your body content at H2 (`##`).

If a page should not appear in the top nav, omit `nav_include` (or set it
to `false`). The nav order today is set by `nav_order: 1..8` (the seven
public sections — About, Philosophy, Engage, Upcoming, Research, Teaching,
Creative — plus CV at 8). Retired pages use `_layouts/redirect.html` and
are not in the nav. The four persona CV views (`cv-academic.md`,
`cv-educator.md`, `cv-creative.md`, `cv-advocacy.md`) deliberately omit
`nav_include` — they are reached from links at the top of the CV page.

## Adding a CV entry

The five CV pages are generated from the `_cv/` collection — one small
markdown file per entry. Every entry MUST carry a `personas:` list (one
or more of `academic`, `educator`, `creative`, `advocate`; CI fails the
build if it's missing). Optional `specialties:` adds free-form
kebab-case tags. A new press item is one file,
`_cv/press/2026-b-outlet-name.md`:

```markdown
---
section: press
year: 2026
personas: [academic, advocate]
---

[Descriptive link text naming the piece and outlet](https://example.org/article).
```

Rules that matter:

- **No headings inside entry bodies** — they would corrupt the page
  outline that the layout's table of contents and screen readers
  depend on.
- Roles, skills, and events entries take a double-quoted `title:`
  (rendered as the H3) and an optional `anchor:` to preserve an old
  URL fragment.
- Ordering is by filename: `YYYY-a-slug.md` within press/grants years,
  `010-`/`020-` numeric prefixes elsewhere. Full schema in
  [`_cv/README.md`](_cv/README.md).
- **Curation vs. archive is intentional duplication.** A talk or press
  item lives canonically as a `_cv/` entry and MAY also be hand-added to
  a curated page (teaching.md, engage.md, creative.md, upcoming.md)
  where it fits that page's narrative. Do not "deduplicate" the curated
  mentions against the CV — both are supposed to exist.
- `_includes/cv-sections.html` emits H2 tags with `id` as the first
  attribute because `_layouts/default.html` string-matches on
  `<h2 id="` to build the table of contents. Don't reorder those
  attributes.

## Source-of-truth hierarchy

When adding new content, consult these in order:

1. **`_briefing/seed.md`** — the spine. Every page maps to one `##` section
   here. Use it to keep voice and structure consistent.
2. **`_briefing/claude-cv-verification.txt`** — fact-checked CV with
   citations and source verification. Best for adding citation counts,
   confirming dates, and filling gaps.
3. **`_briefing/website-updates.txt`** — Kyle's 2024–2025 Bristol-era
   updates: new courses, recent talks, recent publications.
4. **`_briefing/recent-records.txt`** — recent publication / poster
   records from Kyle's records system.

When sources disagree, **add the question to
[`docs/open-questions.md`](docs/open-questions.md)** and use the more
specific or more recent source pending Kyle's confirmation. Never invent
content; if seed.md is sparse, leave it sparse.

## Where the plan lives

[`docs/plan.md`](docs/plan.md) has the phased roadmap with checkboxes.
Update it as you complete work — check the box, then commit. That file is
the source of truth for what's done and what's next.

[`docs/open-questions.md`](docs/open-questions.md) is the standing list of
questions to ask Kyle. When something needs his decision, add a checkbox
there with enough context that he can answer cold.

## Working-branch convention

Develop on a fresh `claude/<short-topic>` branch off `main`. Past
branches are merged into `main` — do not resurrect them.

- Develop and commit on a `claude/...` branch
- Push with `git push -u origin <branch>`
- Open a PR (not a draft) when changes are ready for review
- Never push directly to `main` without explicit permission from Kyle

## What NOT to do

- Don't add JavaScript frameworks (React, Vue, Alpine, etc.)
- Don't add a Gemfile or custom Jekyll plugins
- Don't add a remote theme other than Minima
- Don't write your own `<h1>` inside a page body
- Don't use `click here` / `read more` / bare-URL link text
- Don't add images without alt text
- Don't move the `_briefing/` or `docs/` folders into the served tree
- Don't commit `_site/` — it's in `.gitignore`
- Don't push without first running through the verification steps in
  [`docs/style-guide.md`](docs/style-guide.md)
