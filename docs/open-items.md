# Open items — placeholders and gaps to fill

This is the current backlog of placeholders, "to be confirmed"
entries, and thin sections across the public site. Fill in details
as Kyle surfaces them (a one-line patch per item; references in
each entry tell you exactly what file and section to update).

For historical context on resolved decisions, see
[`open-questions.md`](open-questions.md). For the architectural
audit of the briefing materials, see
[`briefing-audit.md`](briefing-audit.md).

## How to use this file

Each item below is structured as:

- **What's missing** — short description
- **Where it lives** — file path and section heading
- **What would resolve it** — the specific details needed
- **How to patch** — one-line note about the edit

Mark items resolved by replacing the bullet with `~~strikethrough~~`
text and a "(resolved in PR #NN)" tag. Don't delete entries — they
serve as a log of what was outstanding.

---

## Speaking engagements with placeholders

(`engage.md`)

- **Cambodia keynote (2025)** — title, venue, exact date.
  *Location:* `## Keynotes and invited talks` section.
  *To resolve:* swap the placeholder bullet for a full entry
  matching the format of other talks.

- **"XR for Good" panel at the University of Bristol** — date,
  co-panelists.
  *Location:* `## Panels and moderated discussions` section.
  *To resolve:* add the date and any co-panelists Kyle wants to
  credit.

- **London Technology Club at the Savile Club, London** — exact
  date, talk title or topic.
  *Location:* `## Keynotes and invited talks` section.
  *To resolve:* add date and title; if the format was a panel,
  move to `## Panels and moderated discussions`.

- **Nanyang Technological University (NTU) seminar, Singapore** —
  title, exact date, host school within NTU.
  *Location:* `## Keynotes and invited talks` section.
  *To resolve:* fill in title, date, and host school.

- **Macro Hive Conversations episode** — specific episode title.
  *Location:* `## Keynotes and invited talks` section.
  *Status:* podcast and host (Bilal Hafeez) are linked; only the
  episode title is still flagged as "Full details to come" in
  `_briefing/website-updates.txt`. Optional fill-in.

## Performances with placeholders

(`every-sense.md`)

- **Spatial DJ Sound Lounge (Bristol)** — full date, venue,
  collaborator names.
  *Location:* `### Spatial DJ Sound Lounge` H3 under
  `## Performances`.
  *To resolve:* swap the placeholder description for verified
  details. The brief at `_briefing/performances-and-events.md` §6
  notes nothing was findable on the open web.

- **Good Vibrations (Bristol, wave field synthesis)** — full date,
  venue, collaborator names.
  *Location:* `### Good Vibrations` H3 under `## Performances`.
  *To resolve:* same as above; brief §7 has no findable docs.

## Upcoming engagements with placeholders

(`whats-next.md`)

- **Monterrey, Mexico keynote (late October 2026)** — title, exact
  venue, exact date.
  *Location:* `## 2026` section, first entry.
  *To resolve:* fill in title, host institution, and exact date.

- **Audio Developer Conference (ADC) keynote, Bristol (November
  2026)** — title.
  *Location:* `whats-next.md` confirmed-engagements list.
  *Status update (June 2026):* conference dates confirmed as 9–11
  November 2026 (Bristol Marriott Hotel City Centre) and added to
  `whats-next.md`; Kyle is not yet on the public speaker listing, so
  the keynote itself still rests on his confirmation. Talk title
  still needed.

## Bristol student supervision details

(`build-with-people.md`; mirror in `engage.md`
`## Research collaboration and PhD supervision` as needed)

- **Final-year Computer Science dissertation supervisees** — names,
  project titles, academic years.
  *Location:* `build-with-people.md` `### Bristol student supervision`.
  *To resolve:* one bullet per student, e.g. "**Student Name** —
  Final-year CS dissertation, *Project title*, 2024–25." A
  per-year structure works well as the list grows.

- **MSc Computer Science (conversion) student** — name, project,
  year.
  *Location:* same section.
  *To resolve:* one bullet for the student.

- **MSc Immersive Technologies team project** — student names,
  project title, year.
  *Location:* same section.
  *To resolve:* a single bullet listing the team members and
  project title, or one bullet per team member.

## Conferences and events attended

(`cv.md`)

The existing `## Conferences and events attended` section on `cv.md`
is current to 2023 only. Kyle wants every conference he's attended
documented, even if only as an attendee. Bristol-era attendance
(2024–2026) needs to be surfaced and added.

- **Bristol-era conferences attended (2024–present)** — list of
  conferences Kyle has attended since joining Bristol, even if only
  as an attendee.
  *Location:* `cv.md` `## Conferences and events attended`, under
  the appropriate sub-section (Science and engineering / Software
  and education / Accessibility and disability advocacy) or a new
  "Bristol era" sub-section if useful.
  *To resolve:* one bullet per conference with name, year(s), and
  city if useful. Pattern: "Conference Name: 2024, 2025".

## Upcoming travel and conference attendance

(`whats-next.md`)

Kyle wants forthcoming travel — including conferences he's
attending purely as an attendee — surfaced so collaborators know
where to find him. The intro on `whats-next.md` was extended in PR #12
to invite attendance-only entries; entries themselves are still
needed.

- **Forthcoming conference attendances** — names, dates, cities for
  conferences Kyle plans to attend in the next 12 months.
  *To resolve:* one bullet per planned trip on `whats-next.md` with a
  type tag (`[Attending]` for attendee-only) and city. After the
  conference, the bullet can move to the `cv.md` "Conferences and
  events attended" section.

## External evidence links

(`cv.md` / `_cv/`)

- ~~**NYT 2022 black-hole article URL** — Kyle confirmed the citation
  ("Scientists tune into new ways of perceiving black holes",
  May 7, 2022); the URL itself isn't on file.~~ **Resolved in the
  persona-CV redesign PR (June 2026):** the article is
  [nytimes.com/2022/05/07/science/space/astronomy-black-hole-sound.html](https://www.nytimes.com/2022/05/07/science/space/astronomy-black-hole-sound.html),
  online title *Hear the Weird Sounds of a Black Hole Singing*
  (Dennis Overbye). Kyle's remembered title is kept in the entry
  as the print headline — Kyle to confirm that's right.

## Missing publication metadata

(`cv.md` / `_cv/`)

- ~~**Holloway et al. *Assistive Technology* paper — publication
  year.**~~ **Resolved in the persona-CV redesign PR (June 2026):**
  confirmed 2021, 33(sup1), 68–86, DOI 10.1080/10400435.2021.1970653;
  year and DOI link added to
  `_cv/publications/recent-040-holloway-at-innovation-review.md`.

## Major gaps

- ~~**Get-in-touch section on `index.md`** — removed in PR #2 per
  Kyle's request, never repopulated.~~ **Resolved in the persona-CV
  redesign PR (June 2026):** restored as the final H2 on `index.md`
  with links only (LinkedIn, GitHub, ORCID, Bristol Pure) plus a
  pointer to the Engage page; Kyle chose not to publish an email
  address.

## New items from the June 2026 research pass

- **ECHO closing date vs. the reSENSE season.** `whats-next.md` and
  `every-sense.md` say *ECHO* runs through 31 October 2026, but
  reSOUND New York launched a new season called *reSENSE*
  (23 April – 18 October 2026) per an I Love NY listing — and a June
  2026 fetch of resound-nyc.com found the current season's artwork
  list no longer includes ECHO. It looks likely ECHO has rotated out;
  Kyle to confirm so both pages can be updated.
  *To resolve:* Kyle to confirm whether ECHO continues inside the
  reSENSE season and through what date, then align both pages.

- **Wolfram Blog 2018 Summer School recap byline.** The
  [blog.wolfram.com author archive](https://blog.wolfram.com/author/kyle-keane/)
  shows one post — "The 2018 Wolfram Summer School: A Recap"
  (21 Aug 2018) bylined "Kyle Keane, Education Specialist, Outreach
  & Communications". Consistent with his 2018 Program Director role,
  but the staff title doesn't match his consultant arrangement.
  *To resolve:* Kyle to confirm the post is his; if so it could be
  cited from the teaching or CV pages.

- ~~**CHI 2020 ATHack paper authorship.**~~ **Resolved negative
  (June 2026):** the Semantic Scholar record lists the authors as
  Narain, Ananthabhotla, Méndez, Taylor, Siu, Brugnaro, and Mallozzi —
  Kyle is not among them. Not added. (Whether he appears in its
  acknowledgments is unchecked; ACM blocks fetching.)

- **Scaffolding the Fantastical podcast year.** The episode page
  dates it 14 January 2026, but the CV lists it under press 2025
  (perhaps recording date). *To resolve:* Kyle to confirm which year
  it should sit under; moving it is a one-line `year:` change plus a
  file rename in `_cv/press/`.

- **Monterrey October 2026 keynote** still has no public web
  footprint (searched English and Spanish, June 2026) — title,
  venue, and date all rest on Kyle's confirmation.

- **Persona tags need Kyle's review.** Every `_cv/` entry was tagged
  during the June 2026 migration; the judgment calls are listed for
  adjudication in `docs/open-questions.md`.

## New items from the June 2026 VALUE → PRINCIPLES → EVIDENCE reflow

- **Sparse future-focused sections on `whats-next.md`.** The
  `### Build with people, not for them` and
  `### Rigor across boundaries` H3s under "Where the work is heading"
  have only connective sentences — they are the slots for Kyle's
  forthcoming workshops, programmes, and cross-field collaborations.
  *To resolve:* Kyle supplies items; one bullet each.

- **Placement of "Talk recordings on computational thinking and
  curriculum."** Moved from the old teaching.md to
  `rigor-across-boundaries.md` (it documents the Computational
  Thinking Framework, which lives there). Defensible to move it to
  `build-with-people.md` instead — Kyle to confirm.

- **Two link-text edits inside Kyle's prose** made during the reflow,
  for his sign-off: `engage.md` "the [Philosophy] page" became "the
  [Full participation] page"; the spatial-audio research thread's
  "via the [Creative] page" became "via the [Performances section
  below]" on `every-sense.md`.

## Leads from the June 2026 deep research waves (snippet-confidence — verify before adding)

These surfaced in searches but could not be fetched/confirmed; each
could become a `_cv/` entry or a curated link once verified:

- ~~**Equitable AI Alliance webinar (Zero Project).**~~ **Resolved
  (June 2026):** confirmed by fetch on the
  [Equitable AI Alliance page](https://zeroproject.org/initiatives/equitable-ai-alliance) —
  Kyle co-hosted *Equitable AI Dialogues: How to ensure diversity in
  the world of AI* with David Banes and Jutta Treviranus; now
  mentioned on engage.md. The webinar's date is still unknown — add
  it (and a `_cv/press/` entry) once Kyle supplies it.
- **LVPEI MITra co-design page.**
  [lvpmitra.com/hcdknowmore](https://lvpmitra.com/hcdknowmore)
  describes the Humanistic Co-design workshop with Dr. Beula Christy;
  site refused connections during research.
- **CoCreate Saudi Arabia 2022 page at the King Salman Center's ICDR
  site** — [icdr.org.sa/en/CoCreate](https://www.icdr.org.sa/en/CoCreate);
  refused connections.
- **Project Aakaar listing on MIT Solve** —
  [solve.mit.edu/solutions/60870](https://solve.mit.edu/solutions/60870)
  (snippet does not name Kyle; the Aakaar lineage is documented in the
  MISTI retrospective already linked from Build with people).
- **MIT BeaverWorks online course pages** (bwsix.mit.edu, Design of
  Assistive Technologies 2019/2020/2021) — returned 503 during
  research; would make good links for the BeaverWorks entries.
- **CSUN 2021 pre-conference workshop** — a Google-indexed snippet of
  the CSUN session index shows a Humanistic Co-Design pre-conference
  workshop with Kyle's bio; the page now requires a session. Kyle to
  confirm; if real it belongs in `_cv/events/` or engage.md.
- **Wolfram Demonstrations Project** — snippets say Kyle authored
  31 Demonstrations; the author page could not be fetched to
  enumerate. A link could join the Wolfram-era role entry.
- ~~**Marburg University Library lecture, 2 April 2025**~~ **Resolved
  (June 2026):** confirmed by fetch — the
  [Math4VIP listing](https://www.math4vip.de/inhalt/aktuelles/ki-systeme-und-wie-sie-blinden-nutzern-helfen-vortrag-von-dr-kyle-keane/)
  names Kyle and gives the talk title (*The Importance of Spatial
  Reasoning in AI Systems to Help Blind Users...*); added to
  `_cv/press/2025-g-math4vip-marburg-lecture.md`.
- **Blindness-podcast circuit absence.** Searches of Eyes on Success,
  Blind Abilities, Living Blindfully, Double Tap, AT Banter, AppleVis,
  ACB/NFB archives found no Kyle appearances — noted as an outreach
  opportunity rather than a gap in the record.
- **Rockefeller Center HERO page credit.** A search snippet of
  [rockefellercenter.com/hero-experience](https://www.rockefellercenter.com/hero-experience/)
  shows the full named ECHO credit (Kara, Condry, Keane, oOps.50656,
  KKOL Studio); the page returned 403 during research — verify
  manually and link from `every-sense.md` if good.
- **Ars Technica, May 2022.** "Listen to the X-ray echoes of a black
  hole as it devours a companion star" (Jennifer Ouellette) exists but
  the site blocks automated fetching, so whether it names Kyle is
  unverified —
  [probable URL](https://arstechnica.com/science/2022/05/listen-to-the-x-ray-echoes-of-a-black-hole-as-it-devours-a-companion-star/).
- **Dead project sites with confirmed Wayback snapshots.** The
  CoCreate site (cocreate20.org) refuses connections and
  humanistic.app is a parked domain, but snapshots exist that Kyle
  (or a future session with archive access) can open directly:
  [cocreate20.org snapshot, 21 January 2021](http://web.archive.org/web/20210121045640/https://www.cocreate20.org/);
  [kylekeane.com snapshot, 22 December 2014](http://web.archive.org/web/20141222154613/http://www.kylekeane.com:80/);
  [kylekeane.com snapshot, 26 December 2017](http://web.archive.org/web/20171226170351/http://www.kylekeane.com:80/).
  Consider preserving CoCreate content somewhere durable.
- **Possible thesis acknowledgments** (MIT DSpace blocks fetching):
  Halie Nakamura's 2025 MEng thesis (continuation of the
  Sinha/Keane facial-recognition line,
  [DSpace PDF](https://dspace.mit.edu/bitstream/handle/1721.1/163037/nakamura-halnak-meng-eecs-2025-thesis.pdf))
  and Mihir Trivedi's 2022 MEng thesis
  ([DSpace PDF](https://dspace.mit.edu/bitstream/handle/1721.1/143139/Trivedi-mihirt-meng-eecs-2022-thesis.pdf))
  surfaced on Keane-acknowledgment searches — verify involvement
  before citing.
- **Wolfram Summer Research Program 2013 faculty page** — a snippet
  suggests Kyle appears on the
  [2013 faculty listing](https://education.wolfram.com/summer-research-high-school/faculty/2013/)
  (fetch returned 403). If real, his summer-school involvement starts
  two years earlier than the site currently says (2015).
- **January 2016 Arduino IAP corroboration** — collaborator Andrew
  Ringler's
  [teaching archive](https://andrewringler.com/tag/teaching/)
  (confirmed-fetched) documents a January 2016 run of the Arduino
  course with Kyle, a year before the OCW-published 2017 edition.

## Long-term defers (resolved by skip; revisit if Kyle surfaces details)

- **Wolfram MicroMasters AI+D dates** — role title and platform
  (MITx/edX) known; dates not. Kyle chose to leave the role off the
  public site (PR #10 dropped the audit-trail mention). If dates
  surface later, add an entry to `cv.md` `## Roles` between
  MIT EECS Lecturer and AI Research Scientist.

- **Apple Siri integration source URL** — current `cv.md` `## Skills`
  framing ("XML parser and natural language generation code that
  allowed Apple's Siri to speak the quantitative results...") is
  conservative and accurate. Kyle confirmed no URL hunt (PR #8).
  If Wolfram or Apple ever publishes a canonical source, link it
  inline.

## Notes for future Claude Code sessions

- Each placeholder above includes the file path and section so
  edits are mechanical: read the page, locate the section, swap
  the placeholder with the resolved details.
- Mark items resolved by striking the line through and tagging the
  PR number (e.g. `~~Cambodia keynote — title TBC.~~ Resolved in
  PR #13.`).
- The verified-content baseline lives in
  `_briefing/performances-and-events.md` (artistic items) and the
  CV-verification file at `_briefing/claude-cv-verification.txt`.
  Both files are excluded from the published site.
- Don't add items to this file that have already been addressed by
  documented decisions in `docs/briefing-audit.md`. Cross-check
  before adding anything new.

- **Wolfram Library Archive: "Math and Mathematica 9 for Blind
  Students and Blind Users."** Search snippets attribute this
  conference record (~March 2015) to "Kyle Keane, PhD (Education and
  Accessibility Consultant, Wolfram Research Inc.)" —
  [library.wolfram.com record](https://library.wolfram.com/infocenter/Conferences/8544/)
  (fetch returned 403). If confirmed, it is the earliest public
  accessibility-talk artifact from the Wolfram era.

- **Namesake warning for future research sessions.** YouTube search
  results for "Kyle Keane" are dominated by the YouTuber Primink
  (whose real name is also Kyle Keane) and an audio engineer "Kyle
  Kean" — exclude both when hunting for coverage.

## Leads from the early-life and HCDI research (June 2026)

- **CoCreate KSA scale figures recovered from search indexes of the
  dead cocreate20.org site**: 18 fellows, 18 mentors, 138
  co-creators, 16 affiliates, 25 projects, with fellows committing
  5-10 hours/week for the year. Pending verification against the
  Wayback snapshot
  ([cocreate20.org, 24 May 2022](http://web.archive.org/web/20220524032709/https://cocreate20.org/))
  before publishing the numbers; the humanistic.app self-description
  is likewise recoverable from
  [its 19 July 2024 snapshot](http://web.archive.org/web/20240719110348/https://www.humanistic.app/).
- **Alfaisal CoCreate continuity**: search snippets show a 30 January
  2023 exhibit (refreshable tangible graphics for blind users; MND
  voice bank) and a 17 January 2024 "Social Innovation Exhibit"
  combining MIT Solv[ED] and CoCreate projects
  ([Alfaisal News](https://news.alfaisal.edu/social-innovation-exhibit/),
  server 503s to robots). Confirm and add to build-with-people.md.
- **CoCreate fellow testimony**: Dr. Sarah Almoaiqel's CV lists
  "Co-Create Fellowship in the Humanistic Co-Design Initiative,
  2020-2021" — a named fellow whose career the programme touched.
- **Kellogg honour naming**: Cal Poly Pomona's programme is the
  "Kellogg University Scholars Program" ("the highest distinction
  offered to students in the incoming freshman class" per
  PolyCentric 2003); the CV says "Kellogg Scholar (2002)". Kyle may
  want the fuller name and description.
- **Computational-physics origin story**: the MITili Q&A names
  Dr. Gregory Childers and Dr. James Feagin as the CSUF professors
  whose computational physics classes were Kyle's first computer use
  (second year of college) — natural material for the
  "Sight loss in my life" section on full-participation.md when Kyle
  writes the personal voice.
- **Project Aakaar lineage detail** (MISTI, confirmed): launched at
  the January 2019 LVPEI workshop; founding team Shantanu Landore,
  Sarthak Kapoor, Daksh Pamar; implemented at SKEI Bangalore with a
  Buckingham Browne & Nichols exchange; top-20 in the MIT PKG IDEAS
  Social Innovation Challenge 2021. Could enrich the 3.008 bullet on
  build-with-people.md if Kyle wants the detail.

- **Probable-named syndication leads (fetch-blocked, June 2026)**:
  Newswise and ScienceBlog verbatim reposts of the May 2022 MIT
  echoes release; GuruMeditation (French, gurumed.org, 3 May 2022);
  MSN syndicated videos "How Black Hole Observations Were Turned Into
  Sound". Each almost certainly carries the Keane/Condry paragraph;
  verify before adding.
