# kylekeane.github.io

Personal website of Dr. Kyle Keane, Senior Lecturer in Assistive
Technologies at the University of Bristol. Lives at
<https://kylekeane.github.io>.

This README is the orientation document for new human contributors. If
you're working in a Claude Code session, read [`CLAUDE.md`](CLAUDE.md)
as well — it has the project-management view of the same repo.

## Why the site is built the way it is

Every architectural choice in this repo flows from one fact: **Kyle is
blind and uses a screen reader.** That has a few concrete consequences
that constrain everything else:

- **Plain semantic HTML rendered from plain markdown.** No frameworks,
  no JavaScript bundlers, no CSS-in-JS. The HTML the browser receives
  is the HTML you can read in `_layouts/default.html` plus the markdown
  you can read in the page files.
- **No JavaScript on the public site.** None today, and adding any
  needs Kyle's sign-off. Dynamic features (search boxes, expandable
  sections, image carousels) get in the way of screen readers and add
  failure modes that Kyle can't quickly diagnose.
- **One H1 per page**, sequential heading hierarchy (h2 → h3 → h4, no
  skipping), descriptive link text (never `click here` / `read more` /
  bare URL), `alt` text on every `<img>`. CI enforces all four.
- **Keep the dependency surface tiny.** GitHub Pages-native Jekyll, no
  Bundler, no custom plugins. The site needs to keep working unattended
  for years.

The detailed authoring conventions (front matter, headings, lists,
links, dark mode, tables) are in [`docs/style-guide.md`](docs/style-guide.md).
Read it before adding a page or making non-trivial content edits.

## The stack at a glance

| Layer | What it is |
|---|---|
| Build | [GitHub Pages-native Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) — no Gemfile, no Bundler, no custom plugins. The deploy action `actions/jekyll-build-pages@v1` builds the site on push to `main`. |
| Theme | [Minima](https://github.com/jekyll/minima) (whitelisted on GitHub Pages) imported via `@import "minima"` in `assets/css/style.scss`. Used only for typography defaults; the page HTML comes from the local layout in `_layouts/default.html`. |
| Plugins | [`jekyll-sitemap`](https://github.com/jekyll/jekyll-sitemap) (auto-generates `/sitemap.xml`) and [`jekyll-redirect-from`](https://github.com/jekyll/jekyll-redirect-from) (powers the retired-page stubs). Both on the [GitHub Pages plugin whitelist](https://pages.github.com/versions/). |
| CSS | One file: `assets/css/style.scss`. 150% base font size, dark-mode support via `prefers-color-scheme`, focus-visible skip-link styling, header social row. |
| HTML layouts | Two: `_layouts/default.html` (every public page) and `_layouts/redirect.html` (retired-page stubs). |
| JavaScript | None. |
| Hosting | GitHub Pages. The published URL is the `kylekeane.github.io` user-page default; no custom domain. |
| Deploy | [`.github/workflows/jekyll-gh-pages.yml`](.github/workflows/jekyll-gh-pages.yml) — runs on push to `main`, builds with Jekyll, publishes via `actions/deploy-pages@v4`. |
| PR checks | [`.github/workflows/pr-build-check.yml`](.github/workflows/pr-build-check.yml) — runs on every PR, four jobs (see "What CI enforces" below). |

## Site structure

```
.
├── index.md                        # About (home).        nav 1, /
├── philosophy.md                   # nav 2,  /philosophy.html
├── engage.md                       # nav 3,  /engage.html
├── upcoming.md                     # nav 4,  /upcoming.html
├── research.md                     # nav 5,  /research.html
├── teaching.md                     # nav 6,  /teaching.html
├── creative.md                     # nav 7,  /creative.html
├── cv.md                           # nav 8,  /cv.html — unified CV,
│                                   # generated from _cv/ entries
├── cv-academic.md, cv-educator.md, # persona-filtered CV views
├── cv-creative.md, cv-advocacy.md  # (linked from cv.md, not in nav)
├── _cv/                            # CV database: one markdown file per
│   ├── README.md                   # entry, tagged by persona — see the
│   ├── roles/ affiliations/        # cheat-sheet in _cv/README.md
│   ├── publications/ grants/
│   ├── grant-support/ awards/
│   ├── scholarships/ press/
│   ├── skills/ events/
├── _includes/cv-sections.html      # Liquid that renders _cv/ entries
├── work.md, publications.md, funding.md, skills.md, media.md,
├── speaking.md, events.md, exhibitions.md, performances.md,
├── advising.md, advocacy.md        # 11 redirect stubs forwarding
│                                   # to one of the 8 pages above
├── _config.yml                     # site title, plugins, exclude rules
├── _layouts/default.html           # main page layout
├── _layouts/redirect.html          # layout used by the redirect stubs
├── _includes/header.html           # skip link, site title, social row, nav
├── assets/css/style.scss           # custom CSS
├── _briefing/                      # source material — NOT published
├── docs/                           # project docs — NOT published
├── CLAUDE.md                       # guide for Claude Code sessions
├── README.md                       # this file
└── .github/workflows/              # build / deploy / PR checks
```

The eight pages with `nav_include: true` make up the top nav, ordered
by `nav_order: 1..8`. The eleven redirect stubs exist for inbound-link
continuity from earlier versions of the site — each one is a six-line
markdown file using `_layouts/redirect.html` and a `redirect_to:`
front-matter field.

`_briefing/` and `docs/` are excluded from the build by the `exclude:`
block in `_config.yml`. The "Verify source material is not published"
CI job double-checks that exclusion on every PR.

## How a build happens

1. Push to `main`, or open a PR.
2. **On push to `main`:** `.github/workflows/jekyll-gh-pages.yml` runs,
   builds the site with `actions/jekyll-build-pages@v1`, and deploys
   the artifact via `actions/deploy-pages@v4`. Publish time is roughly
   60–90 seconds.
3. **On every PR:** `.github/workflows/pr-build-check.yml` runs four
   jobs in parallel against the built artifact (see below).

There is no local build step in the normal contributor flow. Push the
branch, open the PR, watch the Actions tab. The "Local preview" section
at the bottom describes the optional `jekyll serve` workflow if you
want it.

## How to make a change

### Edit an existing page

1. Open the markdown file at the repo root (`teaching.md`, `creative.md`,
   etc., or `index.md` for the home / About page).
2. Edit the markdown body. Don't touch the YAML front matter at the top
   unless you mean to.
3. Commit on a `claude/<short-topic>` branch, push, open a PR.

Voice and content rules: see [`docs/style-guide.md`](docs/style-guide.md).
Content sources for non-trivial additions: see
[`docs/content-sources.md`](docs/content-sources.md).

### Add a new page

1. Create `<slug>.md` at the repo root with the standard front matter
   (template from `docs/style-guide.md`):

   ```yaml
   ---
   layout: default
   title: <Section title; appears as the page H1 and as the nav label>
   permalink: /<slug>.html
   description: <one sentence used in the meta description tag>
   nav_include: true
   nav_order: <integer; lower numbers come first in the nav>
   ---
   ```

2. Write the body in markdown. **Do not write your own H1 (`#`)** — the
   layout renders the H1 from `page.title`. Start the body at H2 (`##`).
3. If the page should not appear in the top nav, omit `nav_include` (or
   set it to `false`).
4. The nav reorders automatically on next build.

### Add a CV entry

The CV pages are generated from the `_cv/` collection — one small
markdown file per role, publication, grant, award, press item, etc.
Each entry carries `personas:` tags (`academic`, `educator`, `creative`,
`advocate`) that decide which filtered CV views it appears in
(`/cv-academic.html`, `/cv-educator.html`, `/cv-creative.html`,
`/cv-advocacy.html`); every entry appears on the unified `/cv.html`.

To add a new press item, create `_cv/press/2026-b-outlet-name.md`:

```markdown
---
section: press
year: 2026
personas: [academic, advocate]
---

[Descriptive link text naming the piece and the outlet](https://example.org/article).
```

One file, four front-matter lines, one markdown line — every relevant
CV view updates on the next build. The full schema (sections, ordering,
the `title:`/`anchor:` fields for roles/skills/events) is in
[`_cv/README.md`](_cv/README.md) and
[`docs/style-guide.md`](docs/style-guide.md).

### Retire a page (redirect-stub pattern)

Use this when a page's content has been merged into another page but
you still want the old URL to resolve.

1. Replace the page's body and front matter with a tiny stub:

   ```yaml
   ---
   layout: redirect
   title: <retired page name>
   permalink: /<old-slug>.html
   redirect_to: /<new-target>.html
   ---
   ```

2. The `_layouts/redirect.html` template will render an accessible
   landing page (one H1, descriptive link text) plus a `<meta
   http-equiv="refresh">` tag that bounces the browser. Both behaviors
   matter — the meta-refresh handles the common case; the descriptive
   link is the fallback that satisfies the accessibility lint and
   works for users with refresh disabled.
3. Don't include `nav_include` — retired pages stay out of the nav.

There are eleven examples already at the repo root (`work.md`,
`publications.md`, `funding.md`, `skills.md`, `media.md`, `speaking.md`,
`events.md`, `exhibitions.md`, `performances.md`, `advising.md`,
`advocacy.md`) — copy any of them as a starting point.

### Reorder the nav

Edit the `nav_order:` integer in the affected pages' front matter. The
nav iterates over `nav_include: true` pages sorted by `nav_order` (see
`_includes/header.html`). Lower numbers come first.

### Edit styles

`assets/css/style.scss` is the only stylesheet. The `@import "minima"`
brings in the theme's typography defaults; everything below it is
custom. New styles should:

- Inherit from the existing `@media (prefers-color-scheme: dark)`
  block so dark mode keeps working.
- Use `rem` for sizing (the base font is 150%, and `rem` scales with
  it).
- Avoid hardcoded colours that don't have a dark-mode counterpart.

### Add or change a header link

The header markup is `_includes/header.html`. The `<ul class="site-
socials">` lists Kyle's external profiles; the `<nav aria-label="Main
navigation">` lists the in-site nav. Both are exposed as labelled
landmarks so screen-reader rotor users can navigate them as units.

Each `<li>` in `.site-socials` should have descriptive link text
("LinkedIn", "Bristol Pure profile") rather than a handle or bare URL.
Visual styling is the `.site-socials` block in `assets/css/style.scss`.

## What CI enforces

`.github/workflows/pr-build-check.yml` runs four jobs on every PR. All
four must pass to merge.

| Job | What it checks |
|---|---|
| **Build site** | First verifies every `_cv/` entry has a `personas: [...]` line, then Jekyll builds the site without errors using the same `actions/jekyll-build-pages@v1` action that the deploy workflow uses. The built `_site/` is uploaded as an artifact for the other jobs. |
| **Verify source material is not published** | Greps the built `_site/` for leaked `_briefing/`, `docs/`, `seed*`, `claude-cv-verification*`, `website-updates*`, `recent-records*`, or `CLAUDE.*` files. Fails if any are found. |
| **Accessibility lint of built HTML** | For every HTML page in `_site/`: exactly one `<h1>`, no skipped heading levels, every `<img>` has `alt=`, no `click here` / `read more` link text. |
| **Check internal links** | Runs [lychee](https://github.com/lycheeverse/lychee-action) in offline mode against the built HTML; fails on any broken internal link. |

The accessibility lint is intentionally strict — it codifies the rules
in `docs/style-guide.md` so they don't drift.

## Branch and PR conventions

- Develop on a `claude/<short-topic>` branch off `main`.
- Don't push directly to `main`. Open a PR and let the four checks run.
- Squash-merge is the default — commit history on `main` stays one
  commit per PR.
- Past branches are merged and stay merged — don't resurrect them.

## Where things outside this README live

- [`CLAUDE.md`](CLAUDE.md) — guide for Claude Code sessions: who Kyle
  is, the non-negotiable accessibility constraints, the file layout,
  the source-of-truth hierarchy, the working-branch convention.
- [`docs/style-guide.md`](docs/style-guide.md) — front-matter template,
  heading rules, link-text rules, alt-text rules, table conventions,
  dark-mode notes, pre-publish checklist.
- [`docs/plan.md`](docs/plan.md) — the historical phased roadmap with
  checkboxes. Phases 0–7 are complete as of May 2026.
- [`docs/open-items.md`](docs/open-items.md) — the active backlog of
  placeholders, missing dates, and content gaps across the public
  site. Single source of truth for "what's known to be missing."
- [`docs/open-questions.md`](docs/open-questions.md) — historical
  record of resolved decisions (Bristol start date, MIT end date,
  course numbers, etc.). Useful when content seems contradictory.
- [`docs/content-sources.md`](docs/content-sources.md) — what the
  source material in `_briefing/` is and the merge order to use when
  extending content.
- [`docs/briefing-audit.md`](docs/briefing-audit.md) — Phase 2.5 audit
  record of every claim in the briefing material against the
  published site. Useful for confirming a fact's provenance.
- [`_briefing/README.md`](_briefing/README.md) — what each source file
  in the briefing folder contains and how to use it.

## Local preview (optional)

You don't need to run Jekyll locally — push to a branch and watch the
Actions tab. If you do want to:

```sh
gem install jekyll
jekyll build
jekyll serve
```

`jekyll serve` runs the site on `http://localhost:4000` with
hot-reload. The build matches what GitHub Pages produces in production,
modulo the bundled plugin versions.
