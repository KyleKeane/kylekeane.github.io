# CLAUDE.md — guide for Claude Code sessions

You're working on Dr. Kyle Keane's personal website. Read this file first.
It exists because Claude Code sessions sometimes lose their connection to
the GitHub MCP and have to restart, so the repo itself is the canonical
source of truth for the project plan and procedures.

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
├── index.md                        # Home / About. permalink: /
├── work.md                         # permalink: /work.html
├── teaching.md                     # permalink: /teaching.html
├── research.md                     # permalink: /research.html
├── advocacy.md                     # permalink: /advocacy.html
├── advising.md                     # permalink: /advising.html
├── speaking.md                     # permalink: /speaking.html
├── publications.md                 # permalink: /publications.html
├── funding.md                      # permalink: /funding.html
├── skills.md                       # permalink: /skills.html
├── creative.md                     # permalink: /creative.html
├── media.md                        # permalink: /media.html
├── _config.yml                     # title, description, exclude rules
├── _layouts/default.html           # the only layout
├── _includes/header.html           # skip link, site title, nav
├── assets/css/style.scss           # custom CSS
├── _briefing/                      # source material; NOT published
│   ├── README.md
│   ├── seed.md                     # the spine — original unified outline
│   ├── claude-cv-verification.txt  # fact-checked CV verification
│   ├── website-updates.txt         # 2024–2025 Bristol-era updates
│   └── recent-records.txt          # recent publication / poster records
├── docs/                           # project docs; NOT published
│   ├── plan.md                     # phased roadmap with checkboxes
│   ├── open-questions.md           # things to confirm with Kyle
│   ├── content-sources.md          # what to merge from each _briefing/ file
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
to `false`). The nav order today is set by `nav_order: 1..12` matching the
seed.md outline.

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

The current development branch is **`claude/audit-restructure-website-3vJZx`**.

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
