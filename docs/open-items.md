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

(`creative.md`)

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

(`upcoming.md`)

- **Monterrey, Mexico keynote (late October 2026)** — title, exact
  venue, exact date.
  *Location:* `## 2026` section, first entry.
  *To resolve:* fill in title, host institution, and exact date.

- **Audio Developer Conference (ADC) keynote, Bristol (November
  2026)** — title, exact date.
  *Location:* `## 2026` section, second entry.
  *To resolve:* fill in title and exact date. ADC25 ran November
  10–12, 2025; ADC26 is likely a similar mid-November window.

## Bristol student supervision details

(`teaching.md`; mirror in `engage.md`
`## Research collaboration and PhD supervision` as needed)

- **Final-year Computer Science dissertation supervisees** — names,
  project titles, academic years.
  *Location:* `teaching.md` `### Bristol student supervision`.
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

(`upcoming.md`)

Kyle wants forthcoming travel — including conferences he's
attending purely as an attendee — surfaced so collaborators know
where to find him. The intro on `upcoming.md` was extended in PR #12
to invite attendance-only entries; entries themselves are still
needed.

- **Forthcoming conference attendances** — names, dates, cities for
  conferences Kyle plans to attend in the next 12 months.
  *To resolve:* one bullet per planned trip on `upcoming.md` with a
  type tag (`[Attending]` for attendee-only) and city. After the
  conference, the bullet can move to the `cv.md` "Conferences and
  events attended" section.

## External evidence links

(`cv.md`)

- **NYT 2022 black-hole article URL** — Kyle confirmed the citation
  ("Scientists tune into new ways of perceiving black holes",
  May 7, 2022); the URL itself isn't on file.
  *Location:* `cv.md` `## Press and media`, `### 2022`, top entry.
  *To resolve:* wrap a hyperlink around the existing italicized
  title.

## Missing publication metadata

(`cv.md`)

- **Holloway et al. *Assistive Technology* paper — publication
  year.** The entry on `cv.md` `## Publications` → `### Recent`
  cites *A review of innovation strategies and processes to improve
  access to AT* in *Assistive Technology* **33**(sup1), 68–86 — but
  has no year. The volume number suggests 2021 (the journal's
  volume 33 covers 2021), but this hasn't been verified against the
  journal record.
  *Location:* `cv.md` `## Publications` → `### Recent`, fourth bullet.
  *To resolve:* confirm the year and add it after the page range,
  matching the format of the surrounding entries (e.g. "**33**(sup1),
  68–86 (2021)").

## Major gaps

- **Get-in-touch section on `index.md`** — removed in PR #2 per
  Kyle's request, never repopulated. The site has no contact
  surface today.
  *Location:* `index.md`, after `## Recent work at Bristol`.
  *To resolve:* Kyle to provide which channels to publish (LinkedIn,
  GitHub, email, ORCID, etc.) and the format he wants. The 2024
  rewrite in `_briefing/website-updates.txt` lines 14–17 lists
  LinkedIn (`KyleKeane`), GitHub (`KyleKeane`), and an email of
  the form `kyle ~at~ kylekeane.com`.

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
