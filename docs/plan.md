# Development plan

This is the canonical roadmap for kylekeane.github.io. It travels with
the code so any future session — Kyle, Claude, or anyone else — can pick
up where we left off. Update the checkboxes as you complete work and
commit them along with the changes.

## Phase 0 — Restructure the repo

- [x] Move source material from `assets/content/` to `_briefing/`
- [x] Rename source files for self-description (`seed.md`,
  `claude-cv-verification.txt`, `website-updates.txt`, `recent-records.txt`)
- [x] Update `_config.yml` (real title, description, exclude rules)
- [x] Add viewport meta tag, `<h1>` rendering, and CSS link to
  `_layouts/default.html`
- [x] Move site title in `_includes/header.html` from `<h1>` to a
  non-heading element so each page can have its own H1 from `page.title`
- [x] Add `.gitignore`
- [x] Write `README.md`, `CLAUDE.md`, `_briefing/README.md`
- [x] Write `docs/plan.md` (this file), `docs/open-questions.md`,
  `docs/content-sources.md`, `docs/style-guide.md`

## Phase 1 — Extract every section of seed.md into a page

For each of the 12 sections in `_briefing/seed.md`, create a markdown
page at the repo root with the right front matter and the section's
content (drop the editorial blockquotes, demote headings by one level,
keep `*(from CV)*` provenance tags).

- [x] `index.md` — About (homepage)
- [x] `work.md`
- [x] `teaching.md`
- [x] `research.md`
- [x] `advocacy.md`
- [x] `advising.md`
- [x] `speaking.md`
- [x] `publications.md`
- [x] `funding.md`
- [x] `skills.md`
- [x] `creative.md`
- [x] `media.md`

## Phase 2 — Reconcile open questions with Kyle

Walk through [`open-questions.md`](open-questions.md) with Kyle and
update the affected pages. Each item maps to a specific page; the
question entry says which.

- [x] University of Bristol start date (`work.md`) — **June 2024 –
  present** (live-site date was right; CV intro was wrong)
- [x] MIT lecturer end date (`work.md`) — **September 2022 – May 2024**
  (CV's "present" was a typo; the role ended right before Bristol)
- [x] Indico Data Solutions end date (`work.md`) — **March 2015 –
  October 2015** (CV was right; old live site was wrong)
- [x] 2022 grant total math (`funding.md`) — moot: removed all dollar
  amounts from `funding.md` per Kyle's preference
- [x] MIT Institute Award name (`funding.md`) — confirmed
- [x] 6.450 vs 6.811 course number (`teaching.md`, `work.md`) — all
  four numbers (6.450 / 6.811 / 2.78 / HST.420) are valid
  cross-listings; reflected in both pages
- [x] 3.008 dates typo (`teaching.md`) — confirmed Winter 2017 + 2018
- [x] International workshops not on live site (`teaching.md`) —
  confirmed; keep all visible
- [x] Phone number on public site (`index.md`) — removed; entire
  Get-in-touch section dropped pending Kyle's repopulation
- [ ] Bristol-era material gap (Phase 4 covers this, but flag any
  pieces Kyle wants prioritized)

## Phase 2.5 — Briefing-folder content audit

A safety net before Phase 3 enrichment begins. Goal: confirm every
discrete piece of content in each `_briefing/` file is either
(a) already migrated to a public page, (b) intentionally not migrated
(with reason), or (c) explicitly deferred to Phase 3 or 4.

Output: a new file `docs/briefing-audit.md` with one checklist section
per briefing file, each listing the discrete content items and their
disposition.

- [ ] Audit `_briefing/seed.md` — most content was extracted in Phase 1;
  flag any sub-sections that were dropped (e.g., editorial blockquotes
  are intentional drops; verify nothing else was lost)
- [ ] Audit `_briefing/claude-cv-verification.txt` — every CV claim
  cross-checked against the corresponding page; mark items as already
  matched, scheduled for Phase 3, or intentionally not migrated
- [ ] Audit `_briefing/website-updates.txt` — every 2024–2025 item
  scheduled for Phase 4
- [ ] Audit `_briefing/recent-records.txt` — every record scheduled for
  Phase 4

Run this phase **before** Phase 3 so enrichment work doesn't redo what's
already published.

## Phase 3 — Enrich from `_briefing/claude-cv-verification.txt`

Pass-by-pass per page. The verification file documents citation counts,
source URLs, and identifies which CV claims are externally verified.
Use it to add sourced detail without fabricating.

- [ ] About — confirm bio claims; add citation count if Kyle wants
- [ ] Work — fill MIT-era detail with verified specifics
- [ ] Teaching — verify course numbers, terms, departments
- [ ] Research — add publication-count and citation-count framing
- [ ] Advocacy — verify W3C / DIAGRAM / TeachAccess outcome claims
- [ ] Publications — confirm DOIs / PRA volume + issue numbers
- [ ] Funding — verify grant totals
- [ ] Skills, Speaking, Advising, Creative, Media — sweep for accuracy

## Phase 4 — Add 2024–2025 Bristol material

From `_briefing/website-updates.txt` and `_briefing/recent-records.txt`:

- [ ] Add **COMS30054 Interactive Devices** to `teaching.md` under a
  "Bristol" subsection
- [ ] Add 2024–2025 talks to `speaking.md`:
  - WBUR On Point (July 2025)
  - Macro Hive Conversations (July 2025)
  - Uncommon Senses V + UN Web TV (May 2025)
  - Germany guest lectures (April 2025)
  - Karlsruhe Institute (March 2025)
  - MIT Spatial Sound Lab (March 2025)
- [ ] Add to `publications.md`:
  - Ben-Ami et al. (2025), *Memory & Cognition*
  - Roberts-Morgan et al. (IDC '24), *Sense-O-Nary*
  - Thompson & Keane (2025), Audio Developer Conference poster
- [ ] Update `index.md` (About) with current Bristol research framing
- [ ] Update `work.md` Bristol entry with current activities

## Phase 5 — Polish

- [ ] Add `jekyll-sitemap` plugin (whitelisted on GitHub Pages) to
  `_config.yml`. Generates `/sitemap.xml` automatically.
- [ ] Per-page `description:` front-matter values reviewed by Kyle
- [ ] Open Graph meta tags if Kyle wants social previews
- [ ] Sweep all pages for `click here` / bare-URL link text
- [ ] Check heading hierarchy across all generated pages
  (`grep -oE '<h[1-6]' _site/*.html` and eyeball the result)

## Out of scope (for now)

- Custom domain / CNAME (kylekeane.github.io is the live URL)
- JavaScript, search, or interactive widgets
- Blog / `_posts/` collection
- Image / multimedia pipeline beyond plain `<img alt="...">`
