# Fishbone SSAS - Knowledge Base

> **Status: AUTHORITATIVE. Version 2, 2026-09-06**, superseding version 1 of the same day (in `Archive/`)
> after the first six Raw items were filed and processed. Version 1 was built at setup, before any
> source material was filed, by copying the structure of the `Fishbone Commercial Properties Ltd - Knowledge Base`
> (the group's most mature example, its `CLAUDE.md` version 2 of 2026-09-03 as corrected to
> 2026-09-05) and the Smartsheet layout of the `Fishbone Holdings Ltd` workspace. Why each part is
> the way it is, and what was deliberately left out, is in
> `Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md`.
> `README.md` is a short pointer to this file. Where the two differ, this file wins.

This file gives Claude the context it needs to work in this knowledge base without re-explaining
the setup each session: where the database lives (section 1), how the Wiki is maintained (2), how
new items are processed (3), how the change log works (4), what runs automatically (5, nothing
yet), the governance boundary automation operates under (6), and a short standing snapshot of the
scheme with its open questions (7).

---

## 0. Start every session here

**Before doing anything else, read the newest change-log entries in `Outputs/`.** They are named
`change-log-YYYY-MM-DD-<slug>.md`, one per session or run. `Outputs/kb-registers.md` lists every
one of them in order in its `Change-log entries` table; start there rather than sorting filenames,
because entries from the same day sort by slug, not by time of day. Then scan that same file's
`Processed items` table for rows still `pending` or `partial`. This applies to every kind of
session: a one-off question, a drafting request, a Smartsheet edit, not only formal Raw
processing. Another session may already have investigated the same thing or corrected the same
figure.

**Recount before you rely.** A figure stated in this file, in a change-log entry, in a sister
knowledge base or in a Smartsheet cell is a dated snapshot of what a past session believed. It is
not evidence. Before acting on a number (a loan balance, a contribution total, a count of files or
rows, a date), recompute it from the source document or the live sheet and cite where it came
from. If it cannot be recounted, say so and mark it `(unverified)`. The rule and the failures
behind it are in `Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md`.

**If the task touches the loanback to Fishbone Commercial Properties Ltd**, also read the latest
change-log entries in `Fishbone Commercial Properties Ltd - Knowledge Base` (Drive folder id
`1zC8LmkCLr7BEaqcAlxgAXyz5Bfm73Z7C`). The loan is that company's liability and this scheme's asset;
its terms, its security and its repayment record live in both places and must agree. Link, never
copy, so there is one place to correct each fact.

---

## 1. Database structure

### Where it lives
- **Primary copy: Google Drive**, `My Drive / Fishbone SSAS - Knowledge Base`
  (folder id `1Ow2wOI2hQE3ugsxeZqk2xf7P5f9IT7oV`). Source of truth.
- **Mirror: git repository** `minda-ui/Fishbone-SSAS`, same folder layout. Synced from Drive, never
  the other way. Sensitive Raw files (bank statements, member documents) are Drive-only.
- When the two disagree, Drive wins.

### Folders
```
Fishbone SSAS - Knowledge Base/
├── CLAUDE.md          <- this file (standing context)
├── README.md          <- short human-facing pointer to this file
├── Raw/               <- inbox: source material exactly as received; never edited (+ README.md)
├── Wiki/              <- one fact per article, topic-organised; index.md; _templates/
│   ├── index.md
│   ├── _templates/article.md
│   ├── Assets/        <- what the scheme holds: loanbacks, bank accounts, any property
│   ├── Employers/     <- the principal employer and any participating employer
│   ├── Suppliers/     <- administrator, bank, accountant, valuer, solicitor
│   ├── People/        <- trustees and members
│   ├── Finance/       <- contributions, scheme accounts, HMRC returns, tax
│   ├── Processes/     <- how things are done here, including this knowledge base itself
│   └── Decisions/     <- why things are the way they are, including this structure
├── Outputs/           <- deliverables, dated change-log entries, kb-registers.md (+ README.md)
│   └── Correspondence/  <- filed copies of numbered documents, one per FSS####### row in the
│                          Document Register. Empty until the first number is issued
└── Archive/           <- superseded versions of replaced files, each renamed with its reason
```

Drive folder ids: `Raw/` `1ntYVPRv8xacjjIYqrMi9EVBVv_0PUzuj`, `Wiki/`
`11BDCN8sZkkaUbIBhh_M678CSxT0aSsZc`, `Outputs/` `1UexLyW2u4xI2S0vPSxFiP1ajVlURvD03`,
`Outputs/Correspondence/` `1imVVuNyQrGDV4wz2FFIi3eU_qhNDuqx_`, `Archive/`
`1BdaI30eW8-d9sZHII3Wc2h4pfvNoqPb2`. Wiki category folders are listed in
`Wiki/Processes/knowledge-base-operations.md`.

**Only the Wiki categories this scheme needs exist.** There is no `Tenants/` (the scheme lets no
property on file), no `Properties/` (any property it comes to hold is an asset and goes in
`Assets/`) and no `Contracts/` (a contract is filed under the asset, supplier or person it belongs
to). Create a category when the first article for it exists, add it to `Wiki/index.md` and to the
template's category list, and log it in `Wiki structure changes`. Never create an empty folder
"just in case".

`Raw/README.md`, `Outputs/README.md` and `Outputs/Correspondence/README.md` are folder guides, not
content. They are registered `skipped` in the `Processed items` table of
`Outputs/kb-registers.md` so section 3b's Detect step stops re-flagging them.

**Raw/** is an inbox and the citable source. Nothing stays there *unprocessed*: every item gets a
`Processed items` row and is worked to `done` or `skipped` (see `Raw/README.md` for what
"processed" means). The file itself is never edited, renamed or deleted. Corrections arrive as new
files. Verbal information from a trustee or member is written up as
`Raw/YYYY-MM-DD_owner-note_<subject>.md`, statement separated from commentary, so the Wiki can
cite it.

**Wiki/** holds Markdown articles with the front matter in `Wiki/_templates/article.md`. Every
article is listed in `Wiki/index.md`. Categories: Assets, Decisions, Employers, Finance, People,
Processes, Suppliers. `Employers/` was added 2026-09-06 with its first article.

**Outputs/** are snapshots. Anything worth keeping is written into the Wiki, not left in Outputs.
Standing always-current files are a deliberate exception to the write-once rule: they carry
current state, so they are replaced rather than appended. `Outputs/kb-registers.md` is the first
one.

**Archive/** is never edited or deleted. Drive files cannot be edited in place by the tooling, so
every replacement of a standing file (`CLAUDE.md`, `README.md`, `Outputs/kb-registers.md`, a Wiki
article) follows archive-then-recreate: rename the old file
`<original> (archived YYYY-MM-DD, superseded by <reason>).<ext>`, move it into `Archive/`, upload
the new file, mirror both to git. Keep the original extension at the end of the archived title so
Drive and git names match character for character. The reason must be specific: done
consistently, the `Archive/` listing is the file's own changelog. **Dated change-log entries are
never replaced at all** (section 4), so they never enter this cycle.

### Live data sources (override Raw for these datasets)

| Dataset | Live source | Status |
|---|---|---|
| Scheme assets (loanbacks, bank accounts, any property: balances, rates, terms, valuations, health) | Smartsheet **Asset Register - Database**, sheet id `4114082175256452`, workspace **Fishbone SSAS** (id `4028917527930755`) | Created 2026-09-06 by cloning the Fishbone Holdings Ltd register, which is the FCP register plus `Asset class` and `Counterparty` columns. **Empty: no `FSS 0001` row exists.** Health-Docs, Health-Lease and Health-Finance are **column formulas** on the group RYGB convention; a colour is only as good as the dates behind it. Read-only for automation. |
| Official documents issued or received (trustee resolutions, HMRC, administrator, bank, borrower, solicitor and valuer correspondence) | Smartsheet **Document Register**, sheet id `2561022001022852`, same workspace | Created 2026-09-06, same schema as the FP, FCP and FH registers plus the `Health` formula. **Empty: no `FSS#######` number issued.** Filed copies go in `Outputs/Correspondence/`. Read-only for automation. |
| Follow-up actions | Smartsheet **Tasks**, sheet id `8617681802626948`, same workspace | Created 2026-09-06 from the Holdings sheet. `Owner` is a contact column, not free text. `Health` is a column formula. **Empty.** Read-only for automation. |
| Scheme bank transactions | None live. Metro Bank statements dropped into `Raw/` | None on file yet; see section 7. |
| Scheme financials and returns | None live. No QuickBooks connector exists for the scheme; do not use the group's Intuit connector, which on 2026-09-04 was found to point at Fishbone Properties Ltd. | Accounts and HMRC returns, when filed in `Raw/`, are the financial source. |

Reports over the sheets live in the workspace folder **Reports & Dashboards** (id
`4148450360092547`): `Open Tasks` (report `6471752932788100`) and `Register Health` (report
`8718055188334468`). That folder holds sights and reports only; an editable data sheet never goes
in it.

When a live source exists, pull it fresh each session and log the sync in the change log even if
nothing changed, so the next session knows how fresh the Wiki is.

### Register conventions
- **Prefix `FSS`** (Fishbone SSAS), chosen 2026-09-06 to sit beside `FP`, `FCP`, `FH` and `FCD`.
- **Asset ids and document numbers are different schemes that share the prefix.** An asset is
  `FSS 0001`: four digits, with a space. A document in the Document Register is `FSS0000001`:
  seven digits, no space, matching every row in `Outputs/Correspondence/`. They never collide; do
  not read one as the other.
- One row per asset. Where several interests belong to the same asset they may sit as further
  rows sharing the id. A **reference-only row** (something not owned by the scheme but relevant,
  marked "REFERENCE ONLY - NOT A SCHEME ASSET", all financial cells blank) is allowed only where
  the interest is physically or contractually part of a scheme asset.
- For a loanback, `Counterparty` is the borrower and `Loan type` is `SSAS loanback`; `Loan` is the
  balance as at a stated date, and the date goes in `Note` with its source.
- Document numbers are permanent and never reused; a superseded document keeps its number.

---

## 2. Wiki maintenance guidelines

Summarised here; the full rules are in
[`Wiki/Processes/knowledge-base-operations.md`](Wiki/Processes/knowledge-base-operations.md)
("Wiki maintenance rules, in full").

- One subject per article. Front matter mandatory (`title, category, status, sensitive, created,
  updated, sources, related`). Status `draft | active | superseded | archived`.
- Every fact from a source is cited with a relative link into `Raw/` (or the live source URL) and
  a location inside it. Unsupported statements are marked `(unverified)`.
- Links between articles are relative, kebab-case, bidirectional (`related:` both ends). Link the
  first mention. Never link to `Outputs/`.
- If a linked article does not exist yet, create a stub in `draft` status with an "Open questions"
  section rather than leaving a dead link.
- Sensitive personal data (bank details, National Insurance numbers, dates of birth, home
  addresses, member benefit figures) is never quoted into the Wiki; point to the Raw file and set
  `sensitive: true`. Member and trustee articles are `sensitive: true` by default.
- Keep a "Changes" table at the foot of every article naming the change-log entry that drove each
  edit. Bump `updated` on every edit.
- **Claims in this file are re-verified, not repeated.** If a task is about to act on a claim here
  that it can cheaply re-check against the live source, do so first.

---

## 3. Workflow for processing new items

### 3a. Live sources
1. Check the change log for the last sync of that source.
2. Pull current rows (Smartsheet `get_columns` then `get_sheet_summary`).
3. Diff against the Wiki; update articles in place, moving old values to "Changes".
4. Cite the live source URL in the article.
5. Log the sync with a timestamp, even if nothing changed.
6. Anomalies (error cells, unexplained flags, a formula cell that has detached) are flagged in
   the article's "Open questions", not fixed by guessing.

### 3b. Raw items
Nine steps, set out in full in
[`Wiki/Processes/knowledge-base-operations.md`](Wiki/Processes/knowledge-base-operations.md)
("Raw processing workflow"). In short: **Detect** (list `Raw/`, diff against the `Processed items`
table of `Outputs/kb-registers.md`, ignoring the folder guides registered `skipped`), **Register**
as `pending` before starting, **Read and classify** (respecting the reading limits in 3d),
**Extract**, **Update the Wiki** with citations and cross-links both ways, **Check** links and
front matter, **Log** (`done` or `partial`), **Outputs only when requested**, **Commit** one batch
per commit with message `KB: process <n> raw items (<summary>)`.

### 3c. Owner notes
Verbal statements from a trustee or member become Raw items at once (see section 1), then follow
3b. Where a later statement refines an earlier one, write a new note that names the one it
clarifies; never edit the earlier note.

### 3d. Reading limits, inherited from the sister knowledge bases
- **Any PDF with side-by-side tables** (bank statements, schedules, benefit statements) is read as
  an image, not as extracted text. In a sister workspace on 02/09/2026 three side-by-side tables
  in a bank statement flattened into interleaved columns and a real GBP 11,000 payment was missed.
- **HMRC forms extract with box numbers and values scrambled.** Read them page by page as rendered
  images, or take the figures from the administrator's or accountant's computation instead.
- CSV bank exports read cleanly; a bank's `Spending Category` column is the bank's guess, not the
  scheme's accounting treatment.

---

## 4. Change log

**One file per session or run**, in `Outputs/`, named `change-log-YYYY-MM-DD-<slug>.md`. A second
run on the same day takes its own slug; a follow-up to an entry already written takes
`-addendum`, then `-addendum-2`. Adopted from the start, matching the Fishbone Properties Ltd and
Fishbone Commercial Properties Ltd knowledge bases.

**An entry is written once and never edited.** If something in a past entry turns out to be
wrong, **write a new entry that references it**; never go back and change the old one. The reader
must be able to see what was believed at the time.

**What does not go in a dated entry** lives in `Outputs/kb-registers.md`, a standing file
replaced by archive-then-recreate when a row is added:

| Table | Answers |
|---|---|
| `Change-log entries` | Every entry file, newest first. The chronology; filename sort does not give it |
| `Processed items` | What has been taken out of `Raw/`, and its status. **Section 3b's Detect step diffs `Raw/` against this table** |
| `Wiki structure changes` | When articles and categories were created, renamed or repointed, and why |
| `Outputs produced` | Deliverables built from the Wiki, and who asked for them |

These are current state, not history, which is why they stay in one file.

---

## 5. Automated processes

**None are live.** Everything below is a proposal, in priority order, and each item must satisfy
section 6a before it is created. When a routine is created, add it to this table with its real
name, schedule and connectors, and remove the "proposed" marker.

| Proposed routine | Cadence | Would do | Prerequisite |
|---|---|---|---|
| Loanback monitor | Monthly | Confirm the borrower's monthly payment arrived in the scheme's bank account on time, recompute the balance against the agreement's schedule, flag any late or missing payment, flag the approach of the final payment date, and flag if the security's valuation basis has lapsed. Read-only. | Loanback agreement and Metro Bank statements in `Raw/`. |
| Compliance calendar | Monthly | From the Wiki: scheme year end, HMRC Pension Scheme Return and Event Report deadlines, trustee meeting cadence, any registration or declaration renewals. Rewrites `Outputs/risk-register.md`. Read-only. | Trust deed, HMRC registration and the administrator's timetable in `Raw/`. |
| Weekly Smartsheet sync | Weekly | Section 3a resync of the asset register into the Wiki. | A `Wiki/Assets/` article exists. |
| Document register and tasks append | On demand | Let automation *append* rows and comments to the Document Register and Tasks, never edit or delete a row, never set a status. | An explicit owner decision on the section 6a append exception. Not decided. |
| Quarterly sweep | Quarterly | Drive and Smartsheet access permissions, `draft` stubs and orphan articles, DST check on routine crons. | Nothing. |

Lessons inherited from the sister knowledge bases, to apply if and when routines are created:
create them through the `claude.ai/code/routines` form (API-created routines lacked connectors and
stopped for permission prompts); bake folder and sheet ids into each prompt because a routine
starts with no memory; crons are UTC, so shift them at each UK clock change.

---

## 6. Governance

### 6a. What automation may do unattended, and what needs a human

**May, without asking:** read Drive and Smartsheet; file documents into `Raw/`; create or update
Wiki articles per sections 2 and 3; rewrite standing Outputs files; append change-log entries;
flag anomalies and risks inside Drive files.

**Must never do without an explicit human decision:** send, reply to or forward external email
(drafting for a human is fine); file anything with HMRC, The Pensions Regulator or Companies
House; make or authorise a payment, a contribution, a loan advance or a benefit; commit the scheme
or its trustees to an obligation; **write to any Smartsheet sheet in this workspace** (all three
are fully read-only for automation, with no append exception yet); reply to the scheme
administrator, the bank, a borrower, a solicitor, a valuer or a member; change Drive or Smartsheet
sharing; resolve an ambiguous or contradictory finding by guessing.

If a routine's prompt ever conflicts with this list, this section wins.

### 6b. Data access
- **Access at creation, 2026-09-06: owner only, on both systems.** The Drive folder tree and the
  Smartsheet workspace were created by `minda@fishboneconstruction.co.uk` and shared with nobody.
  This is a point in time, not a standing state; re-check before sharing anything further, and see
  section 5's proposed quarterly sweep.
- **Every PDF in `Raw/` is Drive-only and is never committed to git**, whatever it contains: the six
  filed on 2026-09-06 include signatures and a phone number, and the ones still to come are bank
  and administrator documents.
- A pension scheme's records are personal data about its members by nature. Treat every member,
  trustee, benefit, contribution and bank document as `sensitive: true`. Bank statements and
  member documents stay Drive-only and are never copied into git.
- Cross-entity facts (the loanback to Fishbone Commercial Properties Ltd, employer contributions
  paid by group companies) are **linked** between knowledge bases, never copied, so there is one
  place to correct each fact.

### 6c. Revisiting this document
Update sections 0 to 3 when structure or process changes; section 4 is maintained continuously;
section 5 must be kept current as routines are created, changed or retired; section 6 is revisited
deliberately, not silently rewritten; section 7 is refreshed whenever a Raw item changes the
picture. Every replacement of this file goes through archive-then-recreate and gets a change-log
entry.

### 6d. Maintaining this file
Four rules, inherited from the FCP knowledge base's corpus survey, each with a real failure behind
it (`Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md` records them):

1. **Check the section list survives a replacement**, and check outbound references too. Before
   writing a new version, list this file's headings; after writing it, confirm every heading is
   still present, every "section n" cross-reference resolves, and every file this document points
   at still contains what is claimed.
2. **Retract in place; never delete a claim that was believed.** A statement here that turns out
   to be wrong gets struck through, dated and corrected, not removed.
3. **The archive suffix must name a specific reason.** Confirm a file was actually superseded
   before writing a "superseded by" suffix; when `createdTime` equals `modifiedTime`, a file in
   `Archive/` was never renamed or moved into it.
4. **Detailed rule sets live in the Wiki, not here.** When a rule needs more than a short
   paragraph, put it in a `Wiki/Processes/` article and link to it.

Keep this file to rules that apply to every session. Scheme-specific history belongs in `Wiki/`
articles and the dated change-log entries.

---

## 7. Scheme snapshot and open questions (as of 2026-09-06, after Session 2)

The Wiki is the authoritative record; start at `Wiki/index.md`. This section is a one-screen
orientation, refreshed when a Raw item changes the picture. Lines marked **verified** are cited in
a Wiki article from a document in `Raw/`; lines marked `(unverified)` are pointers found elsewhere
and must be recounted before use.

- **What it is (verified).** Fishbone SSAS, an occupational and investment-regulated pension
  scheme registered with HMRC on 03/12/2021, PSTR 20005255RF, established by Fishbone Drylining
  Ltd (company number 07948220 per the trust deed, 07948020 per the TPR form; one is wrong), now
  Fishbone Construction Ltd per the sister knowledge bases `(unverified)`. Member trustees
  M Gaudiesius and A Prutkovas; corporate trustee Empowered Trustees Ltd (12291059); scheme
  administrator Empowered Pensions Ltd, East Grinstead. The trust deed and board resolution on
  file are **unsigned, undated copies** and the rules are not attached. Scheme year end unknown.
  Articles: `Processes/scheme-establishment-2021`, `Finance/hmrc-registration`,
  `Employers/fishbone-construction-ltd`, `People/*`, `Suppliers/empowered-pensions`.
- **Bank (verified in part).** Metro Bank pension scheme account, opening request signed by both
  member trustees 31/10/2021. Account number, opening date and every statement are not on file.
  Fishbone Properties Ltd's Starling statements, in that company's knowledge base, show weekly
  35.00 payments to "Metro SSAS Account" referenced with a member's name `(unverified)`.
- **Employer compliance (verified).** The principal employer's TPR re-declaration at its
  re-enrolment date 07/11/2023 lists the SSAS (EPSR 12018880) and Aviva (EPSR TK074521), with 2
  staff both already members. Two drafts on file, no submission receipt. **Next re-enrolment date
  is November 2026.**
- **Known asset: loanback to Fishbone Commercial Properties Ltd `(unverified, nothing on file)`.**
  Reference `K0555` per the Loans wiki on Drive, which states original principal 41,500, 5.5
  percent tracking base rate, 60 months, 790.13 a month, final payment 28/04/2030, balance
  31,495.87 as at 21/08/2026; the FCP accounts to 30/04/2025 show a secured loan of 41,500 and its
  bank statements show 790.13 leaving around the 29th of each month; security stated as 145 High
  Street East, Wallsend (owner statement 26/08/2026), whose March 2025 valuation assumed repairs
  still in progress. **The loan agreement is not on file anywhere found**, and the authorised
  employer loan conditions have not been checked.
- **Where the legacy papers are.** The master is OneDrive `Documents/SSAS` on the
  `info@fishbonedrylining` account (ids in `Wiki/Processes/knowledge-base-operations.md`); Google
  Drive `Collaboration Space / Other / Staff (SSAS)` (`1Q7C8BIAD9pGfoBa9a-RF-EmGdS7xXqw0`) is a
  partial copy of November 2024. Six scheme-level documents were copied into `Raw/` on 2026-09-06.
  **Still only on OneDrive and not copyable by the tooling:** `Admistration Agreement.pdf`,
  `SASS price list.pdf`, `Schemes rules.pdf`, `The Pension Regulator Certificate.pdf`. Everything
  else there is member-personal (payslips, ID documents, contribution schedules, transfers) and
  stays out by the owner's instruction. Three loan agreement PDFs dated 2019 and 2021 sit loose in
  `Collaboration Space / Other`; whether they are scheme loans is unknown.

**Open questions, in priority order.**
1. The four OneDrive-only scheme documents above: a person drags them into `Raw/`.
2. The executed trust deed and the rules, the scheme year end, and the filing history (Pension
   Scheme Returns, Event Reports): ask Empowered Pensions Ltd.
3. The loanback agreement with Fishbone Commercial Properties Ltd and the charge over 145 High
   Street East; then the first `FSS 0001` row and the first `Wiki/Assets/` article, and a check
   against the authorised employer loan conditions.
4. Metro Bank account details and statements from opening to date.
5. Who the members are (the trustees, and apparently a third employee whose papers fill the
   `Irina/` folder), what each has contributed, and whether Fishbone Properties Ltd is a
   participating employer.
6. Which company number is right, 07948220 or 07948020, and the Companies House record of the
   name change to Fishbone Construction Ltd.
7. Whether the trustees know that the valuation supporting the loanback's security assumed
   repairs that are not complete.

---

*Standing context for the Fishbone SSAS knowledge base. Version 2, 2026-09-06, after the first Raw
items; version 1 created the same day at setup from the Fishbone Commercial Properties Ltd model. See
`Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md`.*
