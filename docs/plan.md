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
- [x] Bristol-era material gap — resolved by Phase 4 + Phase 6
  Bristol-era additions across all 7 pages

## Phase 2.5 — Briefing-folder content audit

Done. Output: [`docs/briefing-audit.md`](briefing-audit.md). Findings:

- [x] Audit `_briefing/seed.md` — 80 H3 sub-sections audited. 75 ✅
  Migrated, 2 🚧 fixed in this PR (outdated `[In progress at MIT]` /
  `[In progress on MITx]` markers removed from `research.md`),
  1 ❌ Intentionally not migrated (Get-in-touch, removed in PR #2),
  1 ⚠️ Conflict surfaced (Carl V. Thompson Research Group affiliation
  — added to `docs/open-questions.md` for Kyle's confirmation), and
  the 6.450 cross-listing already-resolved by PR #2.
- [x] Audit `_briefing/claude-cv-verification.txt` — every CV claim
  cross-checked. The bulk is sourced enrichment material that feeds
  Phase 3 (citation counts, course evaluations, specific student
  projects, computational-thinking framework, Bristol research
  interests, Project Aakaar). All "NOT VERIFIED" flags resolved by
  Kyle's PR #2 answers, except Thompson group (now in
  `open-questions.md`). Aira intermediary claim resolved by Kyle's
  May-2024 MIT end date — no Aira layover.
- [x] Audit `_briefing/website-updates.txt` — most items map to Phase 3
  (Bristol-era rewrites of About, Teaching, Research, Advocacy,
  Creative, Work) or Phase 4 (COMS30054 course, 2024–2025 talks, recent
  publications). Two outdated in-progress markers removed in this PR.
- [x] Audit `_briefing/recent-records.txt` — four pointers, all 2024–
  2025 material; all defer to Phase 4. One new item not in
  `website-updates.txt`: Thompson & Keane (2025) ADC poster.

## Phase 3 — Enrich from `_briefing/claude-cv-verification.txt`

Done. Pass-by-pass enrichment with sourced detail (no fabrication).
A second-pass briefing audit confirmed zero truly lingering items;
this PR also added evidence/citation links for several already-migrated
claims so the public site is one click from a verifiable source.

- [x] **About** (`index.md`) — added the personal-context line
  ("didn't use a computer until my second year of college") to the
  Career summary
- [x] **Research** (`research.md`) — new "Current research at Bristol"
  section; Computational Thinking Framework with Dr. Peter Barendse
  added to the STEM-learning section; W3C WAI and PhET inline links
  added to the accessibility section
- [x] **Advocacy** (`advocacy.md`) — new "Project Aakaar" section
  (past tense per Kyle: ran through MIT tenure, currently inactive);
  W3C WAI and PhET inline links added to the DIAGRAM section
- [x] **Teaching** (`teaching.md`) — 6.811 enriched with: teaching team
  (Miller / Leonard / Greenberg / Young + Seth Teller honoring),
  student evaluations (6.2–6.4 / 7.0), five representative student
  projects (anonymous framing); 3.008 cross-links forward to Project
  Aakaar
- [x] **Publications** (`publications.md`) — new "Scholarly impact"
  section at top with citation count and ORCID
  (`0000-0003-3243-4412`) link
- [x] **Speaking** (`speaking.md`) — DeepLearn Spring 2022 instructor
  entry added
- [x] **Advising** (`advising.md`) — Mark Vrablic entry enhanced with
  IAP teaching-partner credit + MEng 2020; new "Workshop collaborators"
  subsection naming Andrew Ringler and Abhinav Gandhi
- [x] **Work, Funding, Skills, Creative, Media** — verified against the
  briefing; no Phase-3-class additions warranted (Funding fully covered
  by Phase 2's dollar-amount removal)
- [x] **Future evidence-link sweep** (Phase 5 polish): NYT 2022
  black-hole article URL, Apple Siri integration source, Wolfram|Alpha
  step-by-step solver canonical URL — resolved in the
  "Audit follow-up — evidence links" section below

## Phase 4 — Add 2024–2025 Bristol material

Done. Per Kyle's "keep existing prose, add only new content" rule, the
2024 rewrites of About / Teaching intro / Research intro / Advocacy
intro / Creative intro / Work-Bristol entry from
`_briefing/website-updates.txt` were **not** adopted verbatim. Instead,
each page received targeted Bristol-era additions where there was new
content to surface. The verbatim rewrites remain in
`_briefing/website-updates.txt` if Kyle ever wants to adopt them.

- [x] Added **COMS30054 Interactive Devices** to `teaching.md` under a
  new "Taught courses at Bristol" H2 above the MIT subjects
- [x] Added 17 × 2024–2025 talks to the top of `speaking.md` "Recent
  and invited talks":
  - WBUR On Point (July 2025); Macro Hive Conversations (July 2025);
    Uncommon Senses V + UN Web TV (May 2025); Marburg + Karlsruhe
    (March / April 2025); MIT Spatial Sound Lab (March 2025); Pervasive
    Media Studio + ReachSci (December 2024); Bristol Immersive
    Interaction + Bristol CDT + Microsoft Norway + MIT Comparative
    Media Studies + Microsoft Research Cambridge + Northeastern
    (October–November 2024); Harvard Law School (April 2024)
- [x] Added to `publications.md`:
  - Ben-Ami et al. (2025), *Memory & Cognition*, **53**(1), 325–340
  - Roberts-Morgan et al. (IDC '24), *Sense-O-Nary*
  - Thompson & Keane (2025), Audio Developer Conference (ADC25) poster
    — *Architecting Perceptible Space*
- [x] Added a new "Recent work at Bristol" H2 to `index.md` after
  Education, summarizing the Bristol focus areas
- [x] Extended `work.md` Bristol entry with a sub-list of current
  research/teaching themes and partnerships
- [x] Extended `research.md` "Current research at Bristol" with a
  forward-looking paragraph on sonification, tactile data
  representation, and inclusive AI
- [x] Added a new "## 2025" section to `media.md` with the WBUR On
  Point and Macro Hive Conversations interviews (also linked from
  `speaking.md`)

## Audit follow-up — evidence links

Done in PR #8.

- [x] **Wolfram|Alpha step-by-step solver** linked inline from
  `skills.md` and `work.md` to
  `https://www.wolframalpha.com/examples/pro-features/step-by-step-solutions`
- [x] **NYT 2022 black-hole article** cited by title + date on
  `media.md` 2022 section. Anthropic's web crawler is blocked from
  `nytimes.com`, so the canonical URL couldn't be verified by
  automated search; Kyle confirmed the citation. If the URL surfaces,
  wrap it around the title in a one-line follow-up.
- [x] **Apple Siri integration source** intentionally not linked
  (current `skills.md` framing is accurate without a public source)

## Open items file

Done in PR #12.

- [x] New `docs/open-items.md` — single backlog file capturing every
  placeholder, "(date to be confirmed)" entry, and known gap across
  the public site. Structured per page with file paths and resolution
  notes so future edits are mechanical.
- [x] `docs/open-questions.md` got a one-line pointer to the new
  file at the top; historical content untouched.
- [x] `upcoming.md` intro extended to invite attendance-only travel
  entries (tagged `[Attending]`), so the page works for both
  speaking commitments and just-traveling-there items.

## Speaking restructure + Upcoming page + Bristol supervision

Done in PR #11.

- [x] `speaking.md` restructured: new `## Keynote speeches` and
  `## Panel discussions` H2s above `## Recent and invited talks`.
  Existing chronological structure preserved below.
- [x] Four new entries added (all placeholders pending dates):
  Cambodia keynote (2025), *XR for Good* panel at Bristol, London
  Technology Club at the Savile Club, Nanyang Technological
  University (NTU) Singapore seminar.
- [x] New `upcoming.md` page (nav 15) — chronological list of
  confirmed upcoming engagements, each tagged by type (`[Keynote]`,
  `[Performance]`, `[Event]`, `[Exhibition]`). Two entries on launch:
  Monterrey, Mexico keynote (late Oct 2026) and Audio Developer
  Conference (ADC) keynote in Bristol (Nov 2026).
- [x] `media.md` `nav_order` 15 → 16 to accommodate Upcoming.
- [x] `teaching.md` COMS30054 updated to "Co-teacher". New "Bristol
  student supervision" sub-section under "Taught courses at Bristol"
  with a forward-link to advising.md.
- [x] `advising.md` got a new "Bristol student supervision" H2
  above "Featured advisees" capturing dissertation supervision and
  the MSc supervision activities (conversion MSc + immersive
  technology MSc team).

## Events / Performances / Exhibitions

Done in PR #10. Three new top-level pages were added to surface
Kyle's artistic and curatorial practice surfaced from
`_briefing/performances-and-events.md`. Plus several bonus additions
to existing pages, plus a full removal of the dropped Wolfram
MicroMasters references from internal docs.

- [x] New `exhibitions.md` (nav 12) with the *ECHO — reSOUND New
  York* installation at HERO/Rockefeller Center.
- [x] New `performances.md` (nav 13) with seven entries: Dissolve
  Music 2024 *Sound, Body, Dance*; ECHO takeover with Joshue Ott;
  Buckets; Gong; DENORMALIZED; Spatial DJ Sound Lounge; Good
  Vibrations.
- [x] New `events.md` (nav 14) with three entries: Access Bristol;
  Emergent Harmonics; Unstuffy 01.
- [x] `media.md` renumbered to nav 15. New "## 2024" section with
  Black Hole Reverb album. New sqi.mit.edu blog link and YouTube
  link added to "## 2022" alongside the existing MIT Quest entry.
- [x] `speaking.md` got the Dissolve Music 2025 lightning-talk added
  at the top of "Recent and invited talks".
- [x] `work.md` Bristol entry got a third sub-bullet for the MIT
  Spatial Sound Lab co-lead role on the *Accessible Technology and
  Disability Justice* theme (with Nelly Kate Anderson).
- [x] All Wolfram MicroMasters AI+D references removed from
  `_briefing/claude-cv-verification.txt`, `docs/briefing-audit.md`,
  and `docs/plan.md`.

## Bristol-era prose rewrites

Done in PR #9. The six "Replace text with" rewrites that Kyle had
parked in `_briefing/website-updates.txt` were adopted across the
public site, with per-page tweaks to preserve content already shipped
in earlier PRs.

- [x] **About** (`index.md`) — adopted the rewrite's first 2
  paragraphs as the new "About me". Career summary (incl. the "didn't
  use a computer until college" line from PR #5), Education, and
  "Recent work at Bristol" stay unchanged.
- [x] **Teaching** (`teaching.md`) — adopted the rewrite, with the
  closing sentence tweaked to keep the specific MIT OCW
  "Learn to Build Your Own Videogame" link.
- [x] **Research** (`research.md`) — adopted the rewrite as a new
  "Research direction" section between "Current research at Bristol"
  and "Earlier research themes". Both existing sections stay.
- [x] **Advocacy** (`advocacy.md`) — adopted the 3-paragraph rewrite
  as the new intro. Project Aakaar (PR #5) stays.
- [x] **Creative** (`creative.md`) — adopted with paragraph 3's
  bolder phrasings ("quantum consciousness", "co-create something
  radical", etc.) softened to a grounded close.
- [x] **Work** (`work.md`) — replaced the existing 2-paragraph
  Bristol description with the rewrite's 2 sentences. The PR #6
  sub-list stays underneath.
- [x] `docs/briefing-audit.md` — six rows flipped from ❌ to ✅.
- [x] `_briefing/website-updates.txt` — annotated with a note at top
  that all six rewrites have been adopted.

## Phase 5 — Polish

Done in PR #7. The link-text sweep and heading-hierarchy audit turned
out to already be enforced by the `accessibility` job in
`.github/workflows/pr-build-check.yml` (one H1 per page, no
heading-skips, no "click here" / "read more" anchor text, every img
has alt). Site-wide audit confirmed zero violations.

- [x] Added `jekyll-sitemap` to a new `plugins:` block in
  `_config.yml`. GitHub Pages auto-generates `/sitemap.xml`.
- [x] Per-page descriptions reviewed; enhanced four short ones
  (`advising.md`, `speaking.md`, `creative.md`, `media.md`) to be
  more specific about what each page covers.
- [x] Open Graph + Twitter Card + canonical meta tags added to
  `_layouts/default.html` `<head>`. Twitter card type is `summary`
  (no canonical image yet); `og:image` is conditional on a
  `page.image` front-matter field for future use.
- [x] **Link-text sweep** — already enforced by CI. No source
  violations.
- [x] **Heading hierarchy** — already enforced by CI. No source
  violations.

## Phase 6 — Sitemap redesign (May 2026)

Restructured the 16-page brain dump into a 7-page top nav with a
footer-only CV. Driven by Kyle's brief: clean, assertive, future-first
homepage; a dedicated booking page; an explicit philosophy page that
sets the framing on Kyle's terms rather than letting visitors
typecast him as a disability advocate first.

New top nav: **About · Philosophy · Engage · Upcoming · Research ·
Teaching · Creative**.

- [x] Add `philosophy.md` (nav 2). Lead declares Kyle's primary
  identity (researcher / educator / consultant / artist); names the
  WHO ICF participation model; sections on language (literal-language
  preference, refusal of tone-policing, stance on the metaphorical
  use of *blind*), sight loss in his life (skeleton placeholder for
  the personal arc), engagement standards, structural advocacy, and
  source of perspective.
- [x] Add `engage.md` (nav 3). Engagement standards block, then nine
  H2s for keynotes / guest lectures and master classes / workshops /
  panels / consulting / artistic booking / supervision / symposia /
  contact.
- [x] Promote `upcoming.md` to nav 3 → 4 and rewrite as the consolidated
  forward-facing hub (forthcoming engagements, currently working on,
  recently).
- [x] Rewrite `index.md` to lead with what Kyle does, not how he sees;
  six descriptive-text links replace the old career-summary wall.
- [x] Add `cv.md` (footer-only, not in nav). Consolidates work,
  publications, funding, skills, and media.
- [x] Rewrite `research.md` — promote current Bristol themes
  (audio-tactile graphics, spatial audio for echolocation,
  perception-aware AI, cross-modal interaction); compress PhD-era
  quantum and earlier topics to short paragraphs with CV links.
- [x] Rewrite `creative.md` as a categorical directory (Installations
  / Performances / Recordings / Earlier creative practice). Absorbs
  `exhibitions.md` and `performances.md`.
- [x] Rewrite `teaching.md` — Bristol courses and supervision first;
  MIT subjects condensed to a list under "Previously taught at MIT";
  international workshops, summer schools, and short courses
  preserved as proof points for Engage.
- [x] Retire 11 pages with `redirect_to` front-matter:
  `work` → `/cv.html`; `publications` → `/cv.html`; `funding` →
  `/cv.html`; `skills` → `/cv.html`; `media` → `/cv.html`;
  `speaking` → `/engage.html`; `events` → `/engage.html`;
  `exhibitions` → `/creative.html`; `performances` → `/creative.html`;
  `advising` → `/teaching.html`; `advocacy` → `/philosophy.html`.
- [x] Add `_layouts/redirect.html` (custom redirect template) so
  retired-page stubs satisfy the project's accessibility lint
  (descriptive link text, exactly one H1).
- [x] Add `jekyll-redirect-from` to `_config.yml` plugins.

PR: [#13](https://github.com/KyleKeane/kylekeane.github.io/pull/13).

## Phase 7 — Stabilization (May 2026)

Doc-cleanup pass after content stabilised. Three external-research
batches merged (PRs #15, #16, #17); Kyle paused content additions
for the foreseeable future. This pass brings the project docs in
sync with the post-restructure site.

- [x] Add `cv.md` to the top nav as the 8th item.
- [x] Update `CLAUDE.md` file-layout tree, nav-order line, and
  working-branch convention.
- [x] Update `README.md` file tree and editing guidance.
- [x] Update `docs/style-guide.md` nav-order list.
- [x] Annotate `docs/content-sources.md` page-map table with the
  Phase 6 restructure note.
- [x] Update `docs/open-items.md` to reference current pages
  (`engage.md`, `creative.md`, `cv.md`) instead of retired ones.
- [x] Resolve the `Bristol-era material gap` open question.

## Phase 8 — Persona-tagged CV + media recovery (June 2026)

Kyle asked for a unified CV whose entries carry persona tags
(academic, educator, creative, advocate) with filtered views per
persona, plus a research pass to recover press coverage he had lost
track of. No JavaScript; everything statically generated.

- [x] Split `cv.md` into the `_cv/` collection (113 per-entry
  markdown files, verbatim bodies, persona + specialty tags).
- [x] Add `_includes/cv-sections.html` and regenerate `cv.md` from
  the collection; rendered text verified identical to the old page
  (only addition: the filtered-views list).
- [x] Add the four persona views: `cv-academic.md`, `cv-educator.md`,
  `cv-creative.md`, `cv-advocacy.md` (linked from cv.md, not in nav).
- [x] CI: fail the build if any `_cv/` entry lacks `personas:`.
- [x] Recover and add press: NYT URL (2022), CNN (2022), Time Out
  New York (2025), M. Leona Godin (2026), BioSpectrum India (2020),
  G3ict (2019), MISTI interview + video (2021).
- [x] Fix Holloway et al. year/DOI (2021); move the MIT News
  black-hole-echoes item from 2021 to 2022; update citation count to
  500+ with a Google Scholar link.
- [x] Restore the Get-in-touch section on `index.md` (links only).
- [x] `upcoming.md`: Zero Project Conference (Feb 2026) moved to
  Recently with session details; ADC Bristol 26 dates added.
- [x] `teaching.md`: PPAT archives, MISTI interview, BioSpectrum
  India links.
- [x] Docs: CLAUDE.md / README / style-guide CV-entry recipes;
  open-items resolutions; persona-tag adjudication checklist in
  open-questions.md.
- [ ] Kyle reviews the persona-tag judgment calls
  (`docs/open-questions.md`, June 2026 section).
- [ ] Kyle confirms ECHO's closing date vs. the reSENSE season
  (`docs/open-items.md`).

## Phase 9 — VALUE → PRINCIPLES → EVIDENCE reflow (June 2026)

Kyle asked for a complete informational-architecture redesign: the
site should flow from his anchor value through principles to the
evidence of work done, with a homepage that reads as a semantic table
of contents and prominent future-focused content. One anchor value
(Full participation); three principles as nav sections.

- [x] `nav_label` support in `_includes/header.html` (short nav pills
  for long titles).
- [x] `full-participation.md` — the value hub (philosophy.md verbatim
  + "The principles" section), nav 2.
- [x] `every-sense.md` — principle page absorbing research.md +
  creative.md, nav 3.
- [x] `build-with-people.md` — principle page absorbing teaching.md,
  nav 4.
- [x] `rigor-across-boundaries.md` — principle page (career arc,
  earlier research themes, talk recordings), nav 5.
- [x] `whats-next.md` — broadened upcoming.md with per-principle
  "Where the work is heading" sections, nav 6.
- [x] index.md — value statement + "What's on this site" semantic ToC
  (page name first, then description).
- [x] engage.md nav 3→7; links to renamed pages updated site-wide.
- [x] philosophy/research/teaching/creative/upcoming converted to
  redirect stubs; advocacy/exhibitions/performances/advising
  re-pointed (16 stubs total).
- [x] Principle-page skeleton documented in docs/style-guide.md.
- [x] Docs updated (CLAUDE.md, README, style-guide, open-items).
- [x] `principles:` tags on every `_cv/` entry (one action, many
  principles) + four evidence views (`/cv-full-participation.html`,
  `/cv-every-sense.html`, `/cv-build-with-people.html`,
  `/cv-rigor.html`) + CI lint + schema docs.
- [ ] Comprehensive media-sweep findings integrated as `_cv/press/`
  entries (sweep in progress at time of writing).
- [ ] Kyle fills the sparse future-focused slots on whats-next.md and
  reviews the reflow judgment calls in docs/open-items.md.

## Phase 10 — Works, coverage metadata, and the topic layer (June 2026)

Kyle asked for accomplishment-centric organization: each major work as
a primary record with its media coverage attached as metadata, plus an
obsessive topic-tag layer filterable from the website.

- [x] `_cv/works/` section: 12 major accomplishments (sonification,
  ECHO, HCDI, PPAT, the Wolfram|Alpha/Siri engineering, the DIAGRAM
  standards, measurement reversal, CodeSeal, Access Bristol, Emergent
  Harmonics, the Ayala drumline era, Project Aakaar), each carrying
  the full tag set and rendered as "Selected works" on every CV view.
- [x] `about:` keys on press entries attach coverage to works;
  auto-collected "Coverage and recognition" sublists.
- [x] `type:` labels on all press entries (news-article, syndication,
  talk-recording, podcast, ...).
- [x] Obsessive `specialties:` tags on all ~160 entries: places,
  institutions, subjects, formats (~150 distinct tags).
- [x] `/topics.html` auto-enumerating index + one filtered page per
  tag (topics/<tag>.md, generated; include gains a specialty param).
- [x] Entry points from cv.md and the homepage semantic ToC.
- [ ] Kyle reviews the works framing and tag vocabulary.

## Phase 11 — Facet-first portfolio teardown (June 2026)

Kyle's verdict on Phase 9: principles as nav buried the content. The
rebuild inverts the surface — a facet-first professional portfolio for
humans (elevator pitch → highlights → archive), with the
value/principle layer preserved as the deeper second refraction
pattern for deep-divers and machines.

- [x] Nav: About, Research, Teaching, Creative, Advocacy, What's next,
  Engage, CV (facet pages revived at their original URLs).
- [x] Each facet page: short Overview pitch + Highlights (works links
  into /cv.html anchors) + curated detail + "Full record" archive
  links.
- [x] index.md: elevator pitch, facet cards, selected highlights, the
  "Going deeper" second-pattern section, education, contact.
- [x] full-participation.md off-nav (content untouched); principle
  pages converted to redirects (every-sense→creative,
  build-with-people→teaching, rigor→research); chained stubs
  re-pointed; advocacy.md revived as a facet page.
- [x] All links rewired; whats-next simplified; evidence views and
  topic layer untouched.
- [x] Docs updated (CLAUDE.md two-pattern IA, style-guide facet
  skeleton).
- [ ] Kyle reviews the facet pitches and highlight selections.

## Out of scope (for now)

- Custom domain / CNAME (kylekeane.github.io is the live URL)
- JavaScript, search, or interactive widgets
- Blog / `_posts/` collection
- Image / multimedia pipeline beyond plain `<img alt="...">`
