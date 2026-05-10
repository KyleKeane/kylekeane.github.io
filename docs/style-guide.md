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
- `nav_order` controls the order of nav items. Current order:
  1. About (homepage), 2. Work, 3. Teaching, 4. Research, 5. Advocacy,
  6. Advising, 7. Speaking, 8. Publications, 9. Funding, 10. Skills,
  11. Creative, 12. Media.

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

- Keep the voice from `_research/seed.md`. First person, direct, warm.
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
- [ ] `_research/` files are not in `_site/` after build
  (`find _site -name 'seed*'` returns nothing)
