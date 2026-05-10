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
- [ ] **Future evidence-link sweep** (Phase 5 polish): NYT 2022
  black-hole article URL, Apple Siri integration source, Wolfram|Alpha
  step-by-step solver canonical URL — all flagged in the briefing audit
  as needing verifiable canonical URLs before linking

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

## Out of scope (for now)

- Custom domain / CNAME (kylekeane.github.io is the live URL)
- JavaScript, search, or interactive widgets
- Blog / `_posts/` collection
- Image / multimedia pipeline beyond plain `<img alt="...">`
