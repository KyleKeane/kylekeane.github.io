# Content sources — what's in `_briefing/`

The `_briefing/` folder holds source material the site is built from.
This file describes each source and the order in which to consult them
when extending or correcting a page.

## The four sources

### 1. `_briefing/seed.md` — the spine

A single unified markdown source with every section the website is meant
to have. Each `##` heading maps 1:1 to a page (see the page-to-file map
below). Voice and structure here are canonical: when extending a page,
keep the same tone.

The original seed had editorial blockquotes (`> **Page slug:** ...`,
`> **Page description:** ...`) at the top of each section. Those have
been moved into front-matter (`permalink:`, `description:`) on the
generated pages and should not be re-introduced into the body.

### 2. `_briefing/claude-cv-verification.txt` — the fact-check

A detailed verification report covering every claim in Kyle's CV with
external sources and citation data. Best for:

- Confirming dates, course numbers, institutional affiliations
- Adding citation counts to publications
- Flagging gaps where public information ends (post-2022 / Bristol era)

When seed.md and the verification disagree, the verification usually
wins — but log the disagreement in `docs/open-questions.md`.

### 3. `_briefing/website-updates.txt` — 2024–2025 Bristol updates

Kyle's editing instructions for bringing the site up to date with
Bristol-era material that postdates seed.md. Includes:

- A new course: **COMS30054 Interactive Devices**
- Recent talks (WBUR, Macro Hive, Uncommon Senses V, UN Web TV,
  Germany lectures, Karlsruhe, MIT Spatial Sound Lab) — all 2024–2025
- Recent publications (Ben-Ami et al. 2025, Roberts-Morgan et al.
  IDC '24)
- Updates to the About bio framing

### 4. `_briefing/recent-records.txt` — record-system extract

Small, reinforces the other files plus one item not prominent
elsewhere: Thompson & Keane (2025), *Architecting Perceptible Space*,
Audio Developer Conference poster, Bristol.

## Page → seed.md section map

| Page | seed.md section | seed.md line range |
|---|---|---|
| `index.md` | About | 17–47 |
| `work.md` | Work | 49–196 |
| `teaching.md` | Teaching | 199–415 |
| `research.md` | Research | 419–479 |
| `advocacy.md` | Advocacy | 482–543 |
| `advising.md` | Advising | 547–622 |
| `speaking.md` | Speaking | 625–675 |
| `publications.md` | Publications | 679–744 |
| `funding.md` | Funding & Recognition | 748–836 |
| `skills.md` | Skills & Conferences | 840–929 |
| `creative.md` | Creative | 933–974 |
| `media.md` | Media | 978–1016 |
| `docs/open-questions.md` | Open questions | 1020–1033 |

## Recommended merge order when extending content

1. Start with **`seed.md`** for structure and voice.
2. Use **`claude-cv-verification.txt`** to add specifics (dates, sources,
   citation counts) and to confirm questionable claims.
3. Use **`website-updates.txt`** for everything 2024–2025.
4. Cross-check **`recent-records.txt`** for any item still missing.
5. Anything that can't be resolved goes into
   `docs/open-questions.md` for Kyle.

## What not to do

- **Don't fabricate.** If a source is silent, leave the page silent.
  Sparse is better than wrong on an academic site.
- **Don't import editorial metadata** (the `> **Page slug:**`
  blockquotes from seed.md) into the body of a page. Front-matter is
  the right home.
- **Don't move or rename `_briefing/` files casually.** Other files
  reference them by name (this doc, `CLAUDE.md`, `docs/plan.md`).
