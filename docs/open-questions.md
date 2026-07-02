# Open questions for Kyle

> **Note:** the current active backlog of placeholders and missing
> details is in [`open-items.md`](open-items.md). This file is the
> historical record of resolved decisions.

Things to confirm with Kyle before publishing or before the next merge
pass. Each item names the affected page(s) so we know exactly where to
update once the answer is known.

The first ten items came verbatim from the "Open questions" section at
the bottom of `_briefing/seed.md`, which is the spine document for the
site. New questions accumulate here.

- [x] **University of Bristol start date.** *Affects: `work.md`.* Resolved
  Phase 2: **June 2024 – present** (the previous live site was right; CV
  intro had said 2023). The Work entry has been updated.
- [x] **MIT lecturer end date.** *Affects: `work.md`.* Resolved Phase 2:
  the CV's "September 2022 – present" was a typo. Correct end date is
  **May 2024**, right before Bristol started in June. The Work entry
  now reads "September 2022 – May 2024".
- [x] **Indico Data Solutions end date.** *Affects: `work.md`.* Confirmed
  Phase 2: **March 2015 – October 2015** is correct (the previous live
  site's "Oct 2016" was wrong). The reconciled tag has been removed from
  the entry.
- [x] **2022 grant total.** *Affects: `funding.md`.* Resolved Phase 2 by
  removing **all** dollar amounts from the Funding & Recognition page —
  year-header totals, per-grant amounts, and the "Grant support as
  researcher" figures. The original $205K-vs-$305K discrepancy is now
  moot.
- [x] **MIT Institute Award name.** *Affects: `funding.md`.* Confirmed
  Phase 2: **MIT Institute Award — James N. Murphy Award (2018)** is
  the correct name and year. No change to the page; the *(reconciled)*
  tag was removed.
- [x] **6.450 vs 6.811 course number.** *Affects: `teaching.md`,
  `work.md`.* Resolved Phase 2: all four numbers (**6.450 / 6.811 /
  2.78 / HST.420**) are correct cross-listings of the same course.
  Teaching's heading now lists all four; Work mentions the cross-listing
  in the role description.
- [x] **3.008 dates.** *Affects: `teaching.md`.* Confirmed Phase 2 as
  Winter 2017 + Winter 2018 — **SUPERSEDED July 2026** by Kyle's
  evidence-first adjudication (recorded in
  `_briefing/web-presence-inventory-2026-07.md`): MIT News calls the
  January 2019 trip the inaugural run (thirteen students) and MIT TLL
  documents the January 2020 *Around the Globe* offering. The site now
  shows January 2019 and January 2020, with the July 2017 Climber
  launch weekend and August 2018 Chennai pilot as distinct earlier
  engagements.
- [x] **International multiday workshops.** *Affects: `teaching.md`.*
  Confirmed Phase 2: keep all visible (Sichuan, Al-Faisal, IIT
  Delhi/Madras, LV Prasad Eye Institute, UTEC, etc.). No change.
- [x] **Phone number on the public site.** *Affects: `index.md`.*
  Resolved Phase 2 by removing the **entire** "Get in touch" section
  from About — phone, email, LinkedIn, GitHub. Kyle will repopulate the
  contact section himself when he's decided what to publish.
- [x] **Bristol-era material gap.** *Affects: most pages.* Resolved
  by Phase 4 (2024–2025 Bristol additions across teaching, speaking,
  publications, work, research, media) and Phase 6 (Bristol courses
  and supervision in `teaching.md`, current research themes in
  `research.md`, Bristol-era talks consolidated in `engage.md`, the
  Bristol Senior Lecturer role and Spatial Sound Lab affiliation in
  `cv.md`).
- [x] **Carl V. Thompson Research Group affiliation.** *Affects:
  `work.md`.* Surfaced by the Phase 2.5 briefing audit
  (`docs/briefing-audit.md`). The "Research Scientist (Solid-State
  Dewetting)" entry on the Work page lists Kyle as part of MIT's Carl V.
  Thompson Research Group, January 2016 – January 2017. Kyle's CV
  verification document
  (`_briefing/claude-cv-verification.txt`) flagged this as "NOT VERIFIED
  — no direct evidence of this affiliation found despite extensive
  searching." Both Kyle and Carl V. Thompson were in MIT Materials
  Science during overlapping years, so it's plausible, but no
  publication or institutional record confirms it externally. **Resolved:
  Kyle confirms he was a research scientist under Carl V. Thompson, even
  though external evidence is sparse. Entry stays as written; the verifier's
  "NOT VERIFIED" flag reflects the limits of public records, not the
  accuracy of Kyle's account.**

## Persona-CV redesign questions (June 2026)

During the June 2026 migration, every CV entry in `_cv/` was tagged
with one or more personas (`academic`, `educator`, `creative`,
`advocate`) so the filtered views at `/cv-academic.html`,
`/cv-educator.html`, `/cv-creative.html`, and `/cv-advocacy.html` can
be generated. Most tags are obvious; these were judgment calls. To
change one, edit the `personas:` line in the named file.

- [ ] **Head of User Experience, Indico Data Solutions.** *Affects:
  `_cv/roles/080-head-of-user-experience-indico.md`.* Tagged
  `[educator]` (developer relations and documentation read as
  education); it fits no persona perfectly. OK, or would you rather
  tag it `[academic]` so it sits with the career-history strand?
- [ ] **Bristol Senior Lecturer role tagged with all four personas.**
  *Affects: `_cv/roles/010-senior-lecturer-bristol.md`.* The role
  description spans teaching, research, sonification, and AT, so it
  appears on every filtered view. Confirm that's the intent.
- [ ] **Skills sections.** *Affects: `_cv/skills/*.md`.* Tagged:
  programming languages → all four; software development →
  academic+educator+advocate; accessibility → advocate;
  quantitative analysis → academic; organisational →
  academic+educator+advocate. Adjust to taste.
- [ ] **WBUR On Point and Macro Hive press items.** *Affects:
  `_cv/press/2025-a-wbur-on-point.md`,
  `_cv/press/2025-c-macro-hive-conversations.md`.* Tagged
  `[academic, advocate]` — they're expert commentary rather than
  coverage of creative work. OK?
- [ ] **Perkins "Astronomy and Sonification".** *Affects:
  `_cv/press/2022-c-perkins-astronomy-sonification.md`.* Tagged
  `[creative, advocate]` (blind-education resource about the
  sonification). Should `academic` be added?
- [ ] **UROP grants (one per year, 2015–2022).** *Affects:
  `_cv/grants/*-mit-urop.md`.* All tagged `[academic, educator]`.
  OK as a blanket rule?
- [x] **NYT print headline.** **Resolved by Kyle, 2 July 2026: keep
  the parenthetical** (online title + remembered print headline).

## June 2026 deep-research questions

- [x] **"Researcher at Aira" billing.** **Resolved by Kyle, 2 July
  2026: real — Researcher at Aira, approximately 2022–2024,**
  concurrent with the MIT EECS lectureship; now
  `_cv/roles/025-researcher-aira.md`, corroborated by the University
  of Bristol profile ("previous roles at Aira and MIT"). This
  supersedes the earlier briefing-audit note that there was "no Aira
  layover" — correct about a layover, but the role ran concurrently.
- [ ] **CodeSeal talk year corrected to 2017.** *Affects:
  `rigor-across-boundaries.md`, `_cv/press/2017-c-...`.* The site
  previously dated the CodeSeal platform talk to 2018 (from the
  YouTube upload date); the Wolfram Technology Conference 2017
  presentations page dates it 20 October 2017. Corrected — confirm.
- [x] **PhD completion date.** **Resolved by Kyle, 2 July 2026: keep
  2012** as shown across the site.
- [ ] **Ayala drumline era details.** *Affects: `every-sense.md`
  "High school indoor drumline".* Research sourced the ensemble's
  record to wgi.org: 1999 WGI Scholastic A World Championship
  (96.75), 2000 PSO 6th, 2001 PSO 7th, 2002 PSO silver (92.65, 0.20
  behind Choctawhatchee), with Caleb Rothe (now WGI Hall of Fame)
  instructing and Mark Stone directing the band. The enriched section
  assumes you marched during the 1999–2002 window (inferred from your
  2002 Governor's Scholarshare award at Ayala). Confirm the seasons
  you marched and whether *Puzzles* / *Opportunities* map to specific
  years — the pre-2004 show titles are not on the indexable web
  (Wayback captures of the old Ayala band site are the remaining
  lead).
- [ ] **"NASA Chandra data" wording.** *Affects: `index.md` Overview,
  `rigor-across-boundaries.md`.* Your sentence says the sonification
  "took the NASA Chandra data into the *New York Times*". The 2022
  echo search behind the sonification used NICER data per MIT's
  release, and research confirmed the NASA/Chandra V404 Cygni
  sonification (Nov 2022, SYSTEM Sounds) is a separate project that
  does not credit you. Confirm whether "Chandra" is the right word or
  whether it should be "NICER" / "X-ray" — left unedited because the
  sentence is yours.

- [ ] **Springer CoCreate chapter authorship.** *Affects:
  `_cv/publications/chapters-010-springer-cocreate-ip.md`.* Your CV
  listed the chapter as "Al-Wabil, Al-Megren, Keane, et al.", but the
  indexed author list (Semantic Scholar) is Almoaiqel, Al-Megren,
  Oleksak, Alfajhan, Al-Wabil — no Keane. Per the source-conflict
  rule the entry now shows the indexed authors and frames your
  relationship as founder of the initiative it documents. If you
  contributed a section or should be credited differently, say how
  and the entry will be updated. (If you are not an author at all, it
  may belong as a supporting link on Build with people rather than in
  your publications.)
- [ ] **CoCreate 2020 exhibition date.** *Affects:
  `build-with-people.md`.* Sources conflict on whether the concluding
  CoCreate exhibition at Alfaisal College of Engineering was
  31 January 2020 (launch month) or 31 January 2021 (end of the
  year-long fellowship, matching the Hopin virtual showcase). Which
  is right?

- [ ] **Kellogg Scholar year.** *Affects: `_cv/scholarships/070-kellogg-scholar-cal-poly.md`.*
  The site (from seed.md) says Kellogg Scholar, Cal Poly Pomona, 2002;
  the June 2026 deep-research report says 2006. Which year is right?
- [ ] **Wolfram Summer School 2013.** *Affects: `teaching.md`,
  `_cv/`.* The site lists Summer School roles for 2015, 2017, 2018
  (Program Director); the June 2026 deep-research report also lists
  2013 (and 2019) as faculty years. Confirm which years to show.

### From the July 2026 web-presence inventory

- [x] **Wolfram Summer School years shown.** Resolved by the July 2026
  Wayback crawl — the entry above records the adjudicated years and
  titles now shown on the site.
- [x] **Supervisee name spelling.** **Resolved by Kyle, 2 July 2026:
  "Indrayud Mandal" is correct.** (The MISTI page's "Biswas Mandal"
  and the CV's "Mandel" are both superseded.)
- [x] **LVPEI January 2020.** **Resolved by Kyle, 2 July 2026: no —
  January 2019 only**, as the site shows.

- [x] **Wolfram Summer School / Summer Camp years.** **Resolved
  evidence-first, 2 July 2026** (Wayback-verified year rosters):
  School — Instructor 2017, Program Director 2018 & 2019; Camp —
  Instructor 2013, Program Director 2018 & 2019. Two source claims are
  contradicted by the archived rosters and are treated as errors
  unless Kyle overrides: seed.md's "2015 — Instructor — Wolfram Summer
  Camp" (two complete post-season 2015 rosters omit him) and the
  recollection of an "Academic Director" title (the camp's Academic
  Directors in 2018/2019 were Chip Hurst and Mads Bahrami; Kyle's
  attested title on both programmes was Program Director).

## Adding to this list

When a new question comes up, add a checkbox here with:

1. A short title in **bold**
2. *Affects: `<file(s)>`* — so we know what page(s) to update
3. Enough context that Kyle can answer cold without rereading the source
