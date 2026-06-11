# Style guide

Concrete rules for writing pages on kylekeane.github.io. Kyle is blind
and uses a screen reader; everything below is here because it makes the
site easier to use with assistive technology.

## Front matter on every page

```yaml
---
layout: default
title: <Section title; appears as the H1 and in the nav>
permalink: /<slug>.html
description: <One-sentence summary, used in the <meta name="description">>
nav_include: true
nav_order: <integer; lower comes first>
---
```

Notes:

- `title` is rendered as the page's `<h1>` by the layout — **don't write
  your own `# Heading` in the body.**
- `permalink` should match the URL Kyle expects (the seed.md author chose
  `.html` URLs; we keep them).
- `description` should be a single sentence, no trailing period needed,
  describing what's on the page in plain language.
- `nav_include: true` puts the page in the top nav; omit (or set
  `false`) to keep a page off the nav.
- `nav_label` (optional) gives a short label for the nav pill when the
  full `title` is too long (e.g. "Every sense" for "Every sense at full
  resolution"). The visible label IS the accessible name — never pair
  it with a different `aria-label`.
- `nav_order` controls the order of nav items. The surface is a
  facet-first portfolio. Current order: 1. About, 2. Research,
  3. Teaching, 4. Creative, 5. Advocacy, 6. What's next, 7. Engage,
  8. CV. The 15 retired pages (`philosophy`, `upcoming`,
  `every-sense`, `build-with-people`, `rigor-across-boundaries`,
  `work`, `publications`, `funding`, `skills`, `media`, `speaking`,
  `events`, `exhibitions`, `performances`, `advising`) are redirect
  stubs and are not in the nav; `full-participation.md` (the values
  page) is live but off-nav.

## Facet pages

The four facet pages (`research.md`, `teaching.md`, `creative.md`,
`advocacy.md`) follow a stable skeleton so new content drops in
predictably:

```markdown
## Overview              <- short elevator pitch (Kyle's voice) +
                            a Highlights list of 3-5 works linking
                            to /cv.html#<work-anchor>
## <Content section H2s> <- page-specific curated detail; one H3 per
                            body of work
## Full record           <- links to the matching persona CV view and
                            2-3 example topic pages
```

To add new evidence: one H3 under the right content H2, plus
(optionally) its `_cv/` entry — the curation-vs-archive duplication is
intentional (see CLAUDE.md).

## CV entries (`_cv/`)

The CV pages are generated from one-file-per-entry markdown under
`_cv/`. Two front-matter shapes:

**List-item entries** (publications, grants, grant-support, awards,
scholarships, press, affiliations):

```yaml
---
section: press            # which CV section this belongs to
year: 2026                # press and grants only — drives year grouping
group: recent             # publications only — recent, educational-resources,
                          # reports, chapters, dissertation, physics
personas: [academic, advocate]   # REQUIRED; academic, educator, creative, advocate
principles: [full-participation, rigor]  # REQUIRED; full-participation,
                          # every-sense, build-with-people, rigor — tag
                          # every principle the action evidences
specialties: [spatial-audio]     # optional, free-form kebab-case
---
```

**Titled-subsection entries** (roles, skills, events) add:

```yaml
title: "Senior Lecturer in Assistive Technologies"   # ALWAYS double-quoted
anchor: rd-fellow         # optional; overrides the H3 id to keep an old anchor
```

Body rules:

- Plain markdown, **no headings** (they'd break the page outline), no
  leading `- ` (the include adds list markup).
- Filenames control order: `YYYY-a-slug.md` inside press/grants years
  (a, b, c... within the year; years render newest first); numeric
  prefixes `010-`, `020-`, ... elsewhere (lower renders first; leave
  gaps so entries can be inserted without renumbering).
- Persona tags decide which filtered views (`/cv-academic.html`,
  `/cv-educator.html`, `/cv-creative.html`, `/cv-advocacy.html`) show
  the entry; everything shows on `/cv.html`. When unsure which personas
  apply, pick the closest and add a checkbox to `docs/open-questions.md`
  for Kyle.

## Heading hierarchy

- The layout produces **one `<h1>`** per page from `page.title`.
- Body content starts at **`<h2>` (`##`)**.
- Sub-sections use `<h3>` (`###`), then `<h4>` (`####`).
- **Never skip levels.** Don't go from `##` to `####`. A screen reader
  uses heading levels to build a navigable outline, and skipped levels
  break that outline.

Quick check on a generated page:

```sh
grep -oE '<h[1-6]' _site/<page>.html
```

You should see h1, then a sequence of h2s, with h3s appearing only after
their parent h2.

## Link text

- **Always descriptive.** The text inside `[ ... ](url)` should
  describe the destination, even out of context.
- **Never** write `click here`, `read more`, `here`, `this`, or paste
  a bare URL as link text. Screen readers can list every link on a page
  in isolation; "click here" tells the user nothing about where it goes.

Good:

```markdown
See [the recommended practices for verbal description of interactive scientific graphics](http://...).
```

Bad:

```markdown
For my recommendations on verbal description, [click here](http://...).
```

When the destination is a paper, name the paper and venue. When it's a
person's profile, use their name.

## Images

- **Every `<img>` needs `alt` text.** In markdown that's the text in
  square brackets: `![alt text here](path/to/image.png)`.
- Alt text describes what the image *conveys*, not what it depicts
  decoratively. For a chart: describe the takeaway. For a portrait:
  describe what's relevant about the portrait (whose face, what
  context). For a purely decorative image: use empty alt, `alt=""`.
- If the image needs a long description (a complex chart, for
  example), put the long description in the body text near the image
  and use a short summary alt.

This site currently has no images. When adding one, keep these rules.

## Lists vs. prose

Use a list when the items are parallel, discrete, and order doesn't
matter much. Use prose when the items have natural connective tissue.
A screen reader announces lists explicitly ("list of 5 items, 1 of 5,
..."), so list structure conveys meaning.

## Voice and provenance

- Keep the voice from `_briefing/seed.md`. First person, direct, warm.
- Preserve **`*(from CV)*`** annotations when copying from seed.md.
  They're useful provenance and they don't get in the way of a screen
  reader.

## Emoji, decorative characters, ASCII art

Avoid them in body content. Screen readers either announce them
verbosely ("smiling face emoji") or skip them silently — both are bad.
Decorative em-dashes between words are fine; runs of `===` or `---`
inside body text are not.

## Tables

A simple two-column markdown table is fine. Anything more complex —
merged cells, nested headers, footnotes — is a screen-reader hazard
and should be reformatted as a list or a series of definitions.

If you do use a table, the markdown header row produces `<th>` cells
automatically, which is what screen readers need to associate columns
with values.

## Dark mode

The CSS already supports `prefers-color-scheme: dark`. When picking
colors for any new style, verify both modes look reasonable and that
contrast meets WCAG AA (4.5:1 for body text). Don't introduce
hardcoded backgrounds in a single mode.

## Pre-publish checklist

Before opening a PR, run through:

- [ ] Front matter is present and well-formed on every changed page
- [ ] Every page has exactly one `<h1>` (it's auto-rendered from
  `title`; you didn't write `#` in the body)
- [ ] No `click here` / `read more` / bare-URL link text
  (`grep -i 'click here\|read more' *.md`)
- [ ] Every image has alt text
- [ ] Heading hierarchy is sequential on every page
- [ ] `_briefing/` files are not in `_site/` after build
  (`find _site -name 'seed*'` returns nothing)
