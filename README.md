# kylekeane.github.io

Personal website of Dr. Kyle Keane, Senior Lecturer in Assistive Technologies
at the University of Bristol. Lives at <https://kylekeane.github.io>.

## How the site is built

- **Plain Jekyll** running on the GitHub Pages-native build (no Bundler, no
  Gemfile, no custom plugins) so the site keeps working unattended for years.
- **Theme:** [Minima](https://github.com/jekyll/minima) (whitelisted on GitHub
  Pages) imported only for typography defaults. The HTML is a small custom
  layout in [`_layouts/default.html`](_layouts/default.html).
- **Deploy:** every push to `main` runs the workflow at
  [`.github/workflows/jekyll-gh-pages.yml`](.github/workflows/jekyll-gh-pages.yml),
  which builds and publishes to GitHub Pages automatically.
- **Content:** every page is a single markdown file at the repo root.
  Edit a `.md` file, push, and the change goes live.

## Editing the site

The fastest path:

1. Open the markdown file for the page you want to edit (`teaching.md`,
   `creative.md`, etc., or `index.md` for the home / About page).
2. Edit the markdown. Don't change the YAML front matter at the top unless
   you mean to.
3. Commit and push. GitHub Pages rebuilds in about a minute.

The full conventions — heading rules, link-text rules, alt-text rules, when
to add a new page — live in [`docs/style-guide.md`](docs/style-guide.md).

## Where things live

```
.
├── index.md              # About (home)
├── philosophy.md, engage.md, upcoming.md, research.md,
├── teaching.md, creative.md       # the other six top-nav pages
├── cv.md                 # /cv.html — long-form record (nav 8)
├── work.md, publications.md, funding.md, skills.md, media.md,
├── speaking.md, events.md, exhibitions.md, performances.md,
├── advising.md, advocacy.md       # 11 redirect stubs forwarding to
│                                  # one of the 8 pages above
├── _config.yml           # Site title, description, plugins, exclude rules
├── _layouts/default.html # Main HTML layout
├── _layouts/redirect.html # Layout used by the redirect stubs
├── _includes/header.html # Skip link, site title, nav
├── assets/css/style.scss # Custom CSS (dark mode, 150% font, skip-link styling)
├── _briefing/            # Source material — NOT published. See _briefing/README.md
├── docs/                 # Project plan, style guide, open questions — NOT published
├── CLAUDE.md             # Guide for Claude Code sessions working on this repo
└── .github/workflows/    # GitHub Pages deploy workflow
```

The `_briefing/` and `docs/` folders are excluded from the build by
`_config.yml` — they live in the repo so the project plan, open questions,
and source material travel with the code, but they don't appear on the
public site.

## For future Claude Code sessions

Read [`CLAUDE.md`](CLAUDE.md) first. It tells you who Kyle is, what
accessibility constraints are non-negotiable, where to pick up the work,
and what not to break.

The current development plan with checkboxes is in
[`docs/plan.md`](docs/plan.md). Open questions to ask Kyle are in
[`docs/open-questions.md`](docs/open-questions.md).

## Local preview (optional)

You don't need to run Jekyll locally — push to a branch and watch the
GitHub Actions build instead. If you do want to:

```sh
gem install jekyll
jekyll build
jekyll serve
```
