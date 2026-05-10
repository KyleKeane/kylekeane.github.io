# Briefing-folder content audit

This audit confirms every discrete piece of content in `_briefing/` either
lives somewhere on the public site, is formally deferred to a later phase,
or has an explicit reason for not being migrated. It was produced as Phase
2.5 of [`docs/plan.md`](plan.md), before Phase 3 enrichment begins, so
that Phase 3 doesn't double-cover work that's already published.

## Status legend

- ✅ **Migrated** — substance appears on a public page (verbatim, reworded,
  or summarized)
- ⏳ **Phase 3** — deferred to enrichment from
  `_briefing/claude-cv-verification.txt`
- ⏳ **Phase 4** — deferred to 2024–2025 Bristol material in
  `_briefing/website-updates.txt` and `_briefing/recent-records.txt`
- 🚧 **Should be added now** — actionable in this PR (see "Action items
  applied" at the bottom)
- ❌ **Intentionally not migrated** — explicit decision (Kyle's, or
  process-ical)
- ⚠️ **Conflict** — sources disagree, surfaced for resolution

## `_briefing/seed.md` (per-H3 — 80 sub-sections)

### About (4)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| About Me | ✅ | `index.md` | |
| Career summary | ✅ | `index.md` | |
| Education *(from CV)* | ✅ | `index.md` | |
| Get in touch | ❌ | `index.md` | Removed in PR #2 per Kyle; Kyle to repopulate later |

### Work (15)

Every role from `seed.md` lines 49–196 is present in `work.md`. The
Bristol entry's date was updated to **June 2024 – present** in PR #2;
the MIT EECS Lecturer entry's end date was corrected to **May 2024**.
The 6.450 reference in the EECS Lecturer entry was rewritten to mention
the cross-listing (6.450 / 6.811 / 2.78 / HST.420).

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Senior Lecturer in Assistive Technologies | ✅ | `work.md` | June 2024 – present |
| Lecturer (MIT EECS) | ✅ | `work.md` | September 2022 – May 2024; cross-listing reflected |
| AI Research Scientist *(from CV)* | ✅ | `work.md` | |
| Lecturer (Materials Science) | ✅ | `work.md` | |
| Research Scientist (IMEL) | ✅ | `work.md` | |
| Technical Consultant *(from CV)* | ✅ | `work.md` | |
| Research Scientist (Solid-State Dewetting) | ⚠️ | `work.md` | See "Conflicts surfaced" |
| Head of User Experience (Indico) | ✅ | `work.md` | |
| Research Programmer — Educational Software | ✅ | `work.md` | |
| Research Programmer — Special Projects | ✅ | `work.md` | |
| R&D Fellow | ✅ | `work.md` | |
| Graduate Student Researcher | ✅ | `work.md` | |
| Teaching Assistant / Laboratory Instructor | ✅ | `work.md` | |
| Undergraduate Researcher | ✅ | `work.md` | |
| Physics Tutor | ✅ | `work.md` | |

### Teaching (8)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Semester-long subjects taught at MIT | ✅ | `teaching.md` | Includes 10 H4 sub-courses; 6.450 / 6.811 / 2.78 / HST.420 cross-listed |
| Semester-long subjects contributed at MIT | ✅ | `teaching.md` | Includes 7 H4 sub-courses |
| Short courses at MIT and elsewhere | ✅ | `teaching.md` | |
| International multiday workshops *(from CV)* | ✅ | `teaching.md` | All workshops kept visible per Kyle's PR #2 decision |
| Summer schools | ✅ | `teaching.md` | |
| Hackathons judged/mentored/advised | ✅ | `teaching.md` | |
| Standalone workshops | ✅ | `teaching.md` | |
| Future courses | ✅ | `teaching.md` | |

### Research (10)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Effectiveness of computer programming to bolster STEM learning | 🚧 | `research.md` | Removing outdated `*[In progress at MIT]*` marker in this PR |
| Pedagogical effectiveness of interactive STEM graphics | 🚧 | `research.md` | Removing outdated `*[In progress on MITx]*` marker in this PR |
| Accessibility/equivalency of interactive STEM graphics | ✅ | `research.md` | |
| Inverse design of photonic crystals | ✅ | `research.md` | |
| Solid-state dewetting | ✅ | `research.md` | |
| Quantum error detection and correction | ✅ | `research.md` | |
| Partial (reversible) quantum measurements | ✅ | `research.md` | |
| Frustrated magnetism on Kagome lattice | ✅ | `research.md` | |
| Virus capsid self-assembly | ✅ | `research.md` | |
| Differential scattering cross sections | ✅ | `research.md` | |

### Advocacy (5)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| DIAGRAM Center | ✅ | `advocacy.md` | |
| TeachAccess | ✅ | `advocacy.md` | |
| Consulting | ✅ | `advocacy.md` | |
| ATHack@MIT | ✅ | `advocacy.md` | |
| Future projects | ✅ | `advocacy.md` | |

### Advising (2)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Featured advisees | ✅ | `advising.md` | |
| Full supervision roster by year *(from CV)* | ✅ | `advising.md` | |

### Speaking (2)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Recent and invited talks *(from CV)* | ✅ | `speaking.md` | Pre-2024 plus 17 × 2024–2025 talks added in PR #6 (Phase 4) |
| Earlier engagements | ✅ | `speaking.md` | |

### Publications (10)

Every publication listed in `seed.md` lines 679–744 is present in
`publications.md` with the correct citation. The 2024–2025 papers
(Ben-Ami et al., Sense-O-Nary, Thompson & Keane) were added in PR #6
(Phase 4).

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Open-innovation ecosystems for AT *(from CV)* | ✅ | `publications.md` | |
| Collaborative Design (Arduino) | ✅ | `publications.md` | |
| Build Your Own Video Game (Unity) | ✅ | `publications.md` | |
| Interactive Scientific Graphics: Recommended Practices | ✅ | `publications.md` | |
| Quantum State Protection (PhD dissertation) | ✅ | `publications.md` | |
| Simplified quantum error detection | ✅ | `publications.md` | |
| Decoherence suppression by measurement reversal | ✅ | `publications.md` | |
| Near-threshold electron impact (Yates, Keane, Khakoo) | ✅ | `publications.md` | |
| Low-energy electron scattering (methanol/ethanol) | ✅ | `publications.md` | |
| Low energy elastic electron scattering (ethylene) | ✅ | `publications.md` | |

### Funding & Recognition (4)

All four sub-sections are present; dollar amounts were removed in PR #2.

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Grants awarded as PI / co-PI *(from CV)* | ✅ | `funding.md` | Year totals & line-item amounts removed in PR #2 |
| Grant support as researcher *(from CV)* | ✅ | `funding.md` | $500K / $1M figures removed in PR #2 |
| Awards *(from CV)* | ✅ | `funding.md` | |
| Scholarships *(from CV)* | ✅ | `funding.md` | |

### Skills & Conferences (8)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Programming languages *(from CV)* | ✅ | `skills.md` | |
| Software development | ✅ | `skills.md` | |
| Accessibility | ✅ | `skills.md` | |
| Teaching across age groups | ✅ | `skills.md` | |
| Quantitative analysis | ✅ | `skills.md` | |
| Organizational and administrative | ✅ | `skills.md` | |
| Conferences and events attended *(from CV)* | ✅ | `skills.md` | |
| Hackathons mentored *(from CV)* | ✅ | `skills.md` | |

### Creative (5)

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| Textures of my Life | ✅ | `creative.md` | |
| Buddha Around Town | ✅ | `creative.md` | |
| Animation Farm | ✅ | `creative.md` | |
| Kirtan Percussion Accompaniment | ✅ | `creative.md` | Includes Anusara Invocation + Jai Maa Durga H4 sub-pieces |
| High School Indoor Drumline | ✅ | `creative.md` | Includes "Puzzles" + "Opportunities" H4 sub-pieces |

### Media (7)

Every year-section (2015, 2017, 2018, 2019, 2020, 2021, 2022, 2025) is
present in `media.md`. The 2025 section was added in PR #6 (Phase 4)
with WBUR On Point and Macro Hive Conversations.

| Sub-section | Status | Page | Notes |
|---|---|---|---|
| 2022 | ✅ | `media.md` | |
| 2021 | ✅ | `media.md` | |
| 2020 | ✅ | `media.md` | |
| 2019 | ✅ | `media.md` | |
| 2018 | ✅ | `media.md` | |
| 2017 | ✅ | `media.md` | |
| 2015 | ✅ | `media.md` | |

### `seed.md` summary

- 80 sub-sections; 75 ✅ Migrated, 2 🚧 Should-be-added-now (research.md
  in-progress markers), 1 ❌ Intentionally not migrated (Get-in-touch),
  1 ⚠️ Conflict (Carl V. Thompson group), and 1 already-resolved-via-PR-2
  ⚠️ (the 6.450 cross-listing).

## `_briefing/claude-cv-verification.txt` (per-item)

The verification report is ~798 lines of fact-checking. Items broken out
below by their migration status. The report's role going forward is to
supply sourced detail for Phase 3 enrichment.

### Already on the site (action: none)

- Education (PhD, MS, BS) → `index.md`
- Doctoral training narrative & Korotkov advisor → `work.md`, `research.md`
- MIT Materials Science Lecturer (2015–2019) → `work.md`
- IMEL founder narrative → `work.md`
- Course 3.008 → `teaching.md`, `work.md`
- Course 3.016 → `teaching.md`
- Course 3.024 → `teaching.md`
- Course 6.811 / 2.78 / HST.420 → `teaching.md`, `work.md`
- Course 6.a01 → `teaching.md`
- Course 3.a01 → `teaching.md`
- MIT Infinite Mile Award (2018) → `funding.md`
- AI Research Scientist (Quest for Intelligence) → `work.md`
- Wolfram R&D Fellow → `work.md`
- Wolfram Research Programmer → `work.md`
- DIAGRAM grant 2013 → `advocacy.md`, `funding.md`
- MITili grant → `funding.md`
- MIT-India / MISTI funding → `funding.md`
- MIT Materials Science Department support → covered by `work.md` IMEL/role narratives
- Quantum-computing publications (PRA 2010, 2012) → `publications.md`
- Atomic/molecular publications (3 papers, 2007–2009) → `publications.md`
- DIAGRAM "Recommended Practices" report → `publications.md`
- MIT OCW Arduino + Unity workshops → `publications.md`
- Black Hole sonification project → `media.md` (NYT 2022, MIT Quest article)
- MIT News articles (Co-designing AT in India 2019, Spotlight 2018, Q&A 2018, Bringing humanistic ed 2018, MIT TLL 2020) → `media.md`
- DIAGRAM Center / W3C influence narrative → `advocacy.md`
- TeachAccess narrative → `advocacy.md`
- ATHack staff advisor → `advocacy.md`
- Hackathon mentorships (HackPrinceton, HackingArts, LearnLaunch, MakerFaire) → `teaching.md`, `skills.md`
- Wolfram Summer School (2013–2019) → `teaching.md`
- European summer schools (EPFL, Imperial, Hermes, July 2016) → `teaching.md`, `speaking.md`
- India workshops (Delhi, Chennai, Hyderabad, Jan 2019) → `teaching.md`
- IIT Madras 2020 January → `teaching.md`
- Saudi Arabia / Co'Create / Alfaisal partnership → `teaching.md`
- IAP Arduino workshop (Jan 2017) → `teaching.md`, `publications.md`
- IAP Unity workshop (Jan 2017) → `teaching.md`, `publications.md`
- IAP recurring workshops (Wolfram tour, Arduino overview, Algorithmic art, Scientific Programming) → `teaching.md`
- Empow Studios workshops (June 2014) → `teaching.md`, `speaking.md`
- DIAGRAM webinar (Aug 2014) → `speaking.md`
- Wolfram Virtual Conference webinar (Sep 2013) → `speaking.md`
- MassArt guest lecture (Nov 2015) → `speaking.md`
- BU guest lecture (April 2016) → `speaking.md`
- APS March Meeting talks (2007, 2010, 2011) → `speaking.md`
- Coherence in Superconducting Qubits poster (April 2010) → `speaking.md`
- IARPA poster (2009) → `speaking.md`
- Yates/Keane/Khakoo poster (2009) → `speaking.md`
- CSUF Commencement Speaker (2007) → `speaking.md`
- AAPT honorarium (Jan 2017) → `speaking.md`
- DIAGRAM Research Meeting talk (June 2014) → `speaking.md`
- ATIA panel (Jan 2014) → `speaking.md`
- Joint Math Meeting panel (Jan 2014) → `speaking.md`
- EDUPUB Workshop (Oct 2013) → `speaking.md`
- Wolfram Tech Conf 2012 talk → `speaking.md`
- CSUF Colloquium (Nov 2011) → `speaking.md`
- ORCID etc. profile statement (the page existed in pre-PR-2 site as part of "Get in touch") → ❌ removed in PR #2 with the rest of the section
- Apple Siri integration → `skills.md` (mentioned in Software development bullet)
- Step-by-step physics solver / Wolfram|Alpha → `skills.md` (mentioned)
- VPATs / Section 508 → `skills.md` (mentioned)

### Phase 3 — sourced detail to add to existing pages (status: shipped)

These are factual/sourced enrichments that build on already-published
sections. PR #5 (Phase 3) shipped most of them; the remainder are noted
with reasons.

- ✅ **488 total Google Scholar citations** (as of Oct 2025) →
  `publications.md` "Scholarly impact" section
- ✅ **ORCID 0000-0003-3243-4412** → `publications.md` "Scholarly
  impact" section, linked to `https://orcid.org/0000-0003-3243-4412`
- ✅ **Course evaluation scores 6.2–6.4 / 7.0** for 6.811 capstone →
  `teaching.md` 6.450 / 6.811 section
- ✅ **Specific 6.811 student project examples** (color-detection
  iPhone app, hands-free birdwatching binoculars, blind-rider haptic
  bike, motorized joystick, iPad call-for-help app) → `teaching.md`
  (anonymous, representative framing per Kyle)
- ✅ **Computational Thinking Framework** w/ Dr. Peter Barendse →
  `research.md` "Effectiveness of computer programming" section
- ⏳ **Wolfram MicroMasters AI+D** Lecturer & Digital Learning Lead
  role → skipped in PR #5 per Kyle pending date confirmation; revisit
  in a future enrichment pass
- ✅ **6.811 teaching team** (Rob Miller, John Leonard, Julie
  Greenberg, Anna Young, Seth Teller legacy) → `teaching.md` 6.811
  section
- ✅ **Bristol research interests** (AI, AT, HCI, perception,
  acoustics, immersive audio) → new "Current research at Bristol"
  section at top of `research.md`
- ✅ **Project Aakaar** (3D-printed tactile teaching aids; offshoot of
  3.008; international exchange) → new "Project Aakaar" section in
  `advocacy.md`; cross-linked from the 3.008 entry on `teaching.md`.
  Past tense per Kyle: ran through MIT tenure, currently inactive.
- ✅ **Personal context: "did not use a computer until second year of
  college"** → `index.md` Career summary opening sentence
- ⏳ **CSUF early advising** (Khakoo lab undergrad research detail;
  Kellogg Scholar 2002 → 2006 typo possibly) → not addressed in PR #5;
  minor follow-up
- ✅ **Specific verified MIT student collaborators** (Mark Vrablic,
  Abhinav Gandhi, Andrew Ringler) → `advising.md` Mark Vrablic entry
  enhanced + new "Workshop collaborators" subsection naming Ringler
  and Gandhi

### Evidence-link sweep (status: shipped where canonical URL exists)

- ✅ **W3C User-Intent Working Group** → both `research.md` and
  `advocacy.md` now link to the
  [W3C Web Accessibility Initiative](https://www.w3.org/WAI/)
- ✅ **PhET simulations** → both `research.md` and `advocacy.md` link
  to [PhET Interactive Simulations](https://phet.colorado.edu/)
- ⏳ **NYT 2022 black-hole article** → not linked; canonical URL not
  located. Future audit pass.
- ⏳ **Apple Siri integration** → no canonical public source URL.
  Future audit pass.
- ⏳ **Wolfram|Alpha step-by-step solver** → no canonical public URL.
  Future audit pass.

### ✅ Phase 4 — items dependent on 2024–2025 material

- ✅ **Memory & Cognition (Ben-Ami et al. 2025)** → `publications.md`
  (added in PR #6)
- ✅ **WBUR On Point (July 2025)** → `media.md` 2025 section and
  `speaking.md` (added in PR #6)
- ✅ **DeepLearn 2022 Spring** instructor role → `speaking.md`
  (added in PR #5 with "Spring 2022" date)

### ❌ Intentionally not migrated

- **"No patents found"** finding — negative result, not site content
- **"Verification status: 85% verified"** — meta-commentary about the
  verification document
- **"Recommendations for complete verification"** section — process
  notes, not site content

### ⚠️ Conflicts (see consolidated section below)

- MIT end date / Aira intermediary role (resolved by Kyle in this session)
- Indico Data Solutions ("NOT VERIFIED" in report) (resolved in PR #2)
- 6.450 / 6.3900 ("NOT VERIFIED" in report) (resolved in PR #2)
- Carl V. Thompson Research Group ("NOT VERIFIED" in report) (open;
  surfaced for Kyle)
- $1,246,000 grants total ("NOT VERIFIED" in report) (mooted by PR #2's
  removal of all dollar amounts)

## `_briefing/website-updates.txt` (per-item)

This file is Kyle's editing instructions for 2024–2025 updates. Most
items are larger replacements that fit Phase 3 (rewrites of existing
sections to reflect Bristol-era framing) or Phase 4 (new 2024–2025
content).

### About Me — replace text

Kyle's preferred 2024 bio is more specific about Bristol, perception
science, and the 2024 framing. → ❌ **Intentionally not migrated**
verbatim per Kyle's Phase 4 decision ("keep existing prose, add only
new content"). PR #6 added a short "Recent work at Bristol" H2 to
`index.md` capturing the new Bristol focus areas. The full rewrite
remains in `_briefing/website-updates.txt` for a possible future
adoption.

### About Me — Get-in-touch lines (LinkedIn, GitHub, email)

Already removed in PR #2 per Kyle's instruction. He'll repopulate later.
→ ❌ **Intentionally not migrated** for now.

### Teaching — replace text

Bristol-era framing for the Teaching intro. → ❌ **Intentionally not
migrated** verbatim per Kyle's Phase 4 decision. The existing intro
stays; new Bristol content lives in the new "Taught courses at Bristol"
section.

### Teaching — Bristol course COMS30054 Interactive Devices

✅ **Migrated** in PR #6 under a new "Taught courses at Bristol" H2 in
`teaching.md`.

### Research — replace text

Bristol-era framing for Research. → ❌ **Intentionally not migrated**
verbatim per Kyle's Phase 4 decision. PR #6 instead extended the
existing "Current research at Bristol" section (which PR #5 introduced)
with a forward-looking paragraph on sonification, tactile data
representation, and inclusive AI.

### Research — Remove "[In progress at MIT]" line

Outdated marker on the "Effectiveness of computer programming to bolster
STEM learning" section. Kyle is no longer at MIT; this in-progress
marker is wrong. → 🚧 **Should be added now** (this PR).

### Research — Remove "[In progress on MITx]" line

Same situation on the "Pedagogical effectiveness of interactive STEM
graphics" section. → 🚧 **Should be added now** (this PR).

### Advocacy — replace text

Bristol-era framing for Advocacy. → ❌ **Intentionally not migrated**
verbatim per Kyle's Phase 4 decision. The existing intro and Project
Aakaar (added in PR #5) stand. The rewrite remains in
`_briefing/website-updates.txt`.

### Speaking — 2024–2025 engagements

Seventeen new engagements (WBUR On Point, Macro Hive, Uncommon Senses V,
UN Web TV, Karlsruhe Institute, Marburg Blindenstudienanstalt, Marburg
Univ., MIT Spatial Sound Lab, Pervasive Media Studio, ReachSci, Bristol
CDT, Bristol Immersive Interaction, Microsoft Norway, MIT Comparative
Media Studies, Microsoft Research Cambridge MA, Northeastern, Harvard
Law). → ✅ **Migrated** in PR #6 (Phase 4) at the top of `speaking.md`
"Recent and invited talks".

### Speaking — pre-existing engagements (Bristol July 2023, UTEC 2022, etc.)

Already on `speaking.md`. → ✅ Migrated.

### Creative — replace text

A more "immersive multisensory artist" framing. → ❌ **Intentionally
not migrated** verbatim per Kyle's Phase 4 decision. The seed.md
intro stays. The expanded manifesto remains in
`_briefing/website-updates.txt`.

### Publications — Ben-Ami et al. (2025) Memory & Cognition

✅ **Migrated** in PR #6 (Phase 4) with the canonical *Memory &
Cognition* citation (DOI 10.3758/s13421-024-01628-2) and the
PsychArchives preprint as a secondary link.

### Publications — Sense-O-Nary IDC '24

✅ **Migrated** in PR #6 (Phase 4) with the ACM DOI link.

### Work — UoB Senior Lecturer description rewrite

More specific Bristol research focus (multisensory interaction, immersive
audio, agentic AI, human echolocation, fingertip haptics, etc.).
→ ✅ **Migrated** in PR #6 (Phase 4) as a sub-list of "Recent research
and teaching themes" and "Collaborations" under the existing Bristol
description (existing description retained).

## `_briefing/recent-records.txt` (per-item)

Small file — four pointers, all of which are 2024–2025 items.

| Item | Status | Page | Notes |
|---|---|---|---|
| Thompson, A. & Keane, K. (2025) — *Architecting Perceptible Space* — ADC25 poster | ✅ | `publications.md` | Added in PR #6 (Phase 4) |
| Ben-Ami et al. (2025) Memory & Cognition | ✅ | `publications.md` | Added in PR #6 (Phase 4) |
| Lecture at Harvard Law (April 2024) | ✅ | `speaking.md` | Added in PR #6 (Phase 4) |
| Sense-O-Nary IDC '24 | ✅ | `publications.md` | Added in PR #6 (Phase 4) |

## Conflicts surfaced (consolidated)

1. **Carl V. Thompson Research Group affiliation** —
   `claude-cv-verification.txt` says "NOT VERIFIED: no direct evidence
   of this affiliation found despite extensive searching." `seed.md` and
   `work.md` currently present it as a Jan 2016 – Jan 2017 role at MIT.
   **→ Resolved (post-PR #3): Kyle confirms he was a research scientist
   under Carl V. Thompson. The verifier's flag reflects sparse public
   records, not inaccuracy. Entry stays as written.**

2. **Aira intermediary role** —
   `claude-cv-verification.txt` says Kyle "Worked at Aira (AI-powered
   visual assistance technology company) between MIT and Bristol", with
   MIT ending in 2022. Kyle's clarification in this session has MIT
   EECS Lecturer running through May 2024 and Bristol starting June
   2024 — no gap, no Aira layover.
   **→ Resolved: trust Kyle's direct correction. Aira is not added.**

3. **Indico Data Solutions** — `claude-cv-verification.txt` flags as
   "NOT VERIFIED". Kyle confirmed in PR #2 the Indico position is real
   with March 2015 – October 2015 dates.
   **→ Resolved in PR #2.**

4. **6.450 / 6.3900** — `claude-cv-verification.txt` says no evidence
   Kyle taught these courses. Kyle confirmed in PR #2 that 6.450 is one
   of the cross-listing numbers for the AT capstone, and 6.3900 is the
   ML course he co-instructed.
   **→ Resolved in PR #2.**

5. **$1,246,000 grants total** — `claude-cv-verification.txt` couldn't
   verify this figure. Per PR #2 all dollar amounts have been removed
   from the public site.
   **→ Mooted by PR #2.**

## Action items applied in this PR

Two small "🚧 should be added now" edits:

1. **`research.md`** — remove `*[In progress at MIT]*` from the
   "Effectiveness of computer programming to bolster STEM learning"
   section. Outdated; Kyle is no longer at MIT.
2. **`research.md`** — remove `*[In progress on MITx]*` from the
   "Pedagogical effectiveness of interactive STEM graphics" section.
   Same reason.

One open-questions update:

3. **`docs/open-questions.md`** — add the Carl V. Thompson Research
   Group affiliation as a new question for Kyle.

## Open follow-ups

- **Phase 3 enrichment**: shipped in PR #5.
- **Phase 4 2024–2025 material**: shipped in PR #6 (this PR). Six
  prose rewrites (About / Teaching intro / Research intro / Advocacy
  intro / Creative intro / Work-Bristol entry) from
  `_briefing/website-updates.txt` were intentionally **not** adopted
  verbatim per Kyle's "keep existing prose, add only new content"
  rule, and remain available there if Kyle later wants to adopt them.
- **Future evidence-link sweep** (Phase 5 polish): NYT 2022 black-hole
  article URL, Apple Siri integration source, Wolfram|Alpha
  step-by-step solver canonical URL, Wolfram MicroMasters dates.
