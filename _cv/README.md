# _cv/ — the CV database

One markdown file per CV item. The CV pages (`cv.md`, `cv-academic.md`,
`cv-educator.md`, `cv-creative.md`, `cv-advocacy.md`) are generated from
these files by `_includes/cv-sections.html`. Edit an entry once and every
view updates.

## Add an entry (the common case: a new press item)

Create `_cv/press/2026-b-outlet-name.md`:

```markdown
---
section: press
year: 2026
personas: [academic, advocate]
principles: [full-participation, rigor]
---

[Descriptive link text naming the piece and the outlet](https://example.org/article).
```

That's it — one file, five front-matter lines, one markdown line.

## Rules

- `section:` is one of: works, roles, affiliations, publications,
  grants, grant-support, awards, scholarships, press, skills, events.
- **Works** are the major accomplishments (`_cv/works/`); each has a
  `slug:` and a `years:` display string. Press entries that cover a
  work carry `about: <slug>` and are auto-collected under that work
  as "Coverage and recognition" on every CV view.
- `type:` (press only, optional) labels the artifact: news-article,
  syndication, talk-recording, lecture-video, podcast, radio,
  institutional-feature, event-listing, interview, blog-post, album,
  video.
- `personas:` is REQUIRED, one or more of: academic, educator, creative,
  advocate. CI fails the build if it's missing.
- `principles:` is REQUIRED, one or more of: full-participation,
  every-sense, build-with-people, rigor. One action can evidence many
  principles — tag every one that applies. CI fails the build if it's
  missing. Drives the evidence views (`/cv-full-participation.html`,
  `/cv-every-sense.html`, `/cv-build-with-people.html`,
  `/cv-rigor.html`).
- `specialties:` is the free-form topic-tag list (kebab-case):
  places, institutions, subjects, formats — tag generously. Every tag
  automatically appears on `/topics.html`; a filtered page per tag
  lives in `topics/<tag>.md` (copy any existing one to add a page for
  a brand-new tag).
- `year:` is required for press and grants entries (drives the year
  grouping on the page).
- `title:` (roles, skills, events only) is the H3 heading; always wrap
  it in double quotes.
- `anchor:` (optional) overrides the H3 id; only needed to preserve an
  old URL fragment.
- Bodies are plain markdown. NO headings inside a body (they would break
  the page outline). No `- ` list marker at the start — the page wraps
  list entries automatically.

## Ordering

- Within press/grants: files sort A→Z inside their year
  (`2026-a-...`, `2026-b-...`); years are shown newest first.
- Roles, affiliations, skills, events, awards, scholarships: numeric
  prefixes (`010-`, `020-`, ...) sort top to bottom. To insert between
  two entries, pick a number in the gap (e.g. `015-`).
- Publications: `group:` picks the subsection (recent,
  educational-resources, reports, chapters, dissertation, physics);
  files sort A→Z within the group.
