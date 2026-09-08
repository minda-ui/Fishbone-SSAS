# Fishbone SSAS - Knowledge Base

> **Status: AUTHORITATIVE. Version 11, 2026-09-08**, superseding version 10 of 2026-09-07 (in
> `Archive/`) after a second open-questions pass: the FCP sister knowledge base's own records
> answer question 7 (the borrower's accounts carry 41,500, not RMT's understood 40,147.80) and
> most of question 10's residual (the valuation's special assumption is confirmed still unmet, now
> due 01/11/2026, and two of the four trustees are also the borrower's own directors); the
> transfer-form email thread read in full explains, without fully resolving, question 11's
> single-signature point (Empowered Lending's own process asked for one signature plus a verbal
> bank-detail callback, not a second physical signature). Questions 3, 5, 8 and 9's certificate and
> notification points were checked again and remain open. Version 10 followed the signed Metro
> Bank transfer form being filed and read: checklist item A10 is
> closed (A11 was not needed), the loan's Drawdown date of 24/04/2025 is now verified rather than
> resting on an email description, and a new question is open on whether the account's
> two-signature mandate was met, since the form carries only one signature. Version 9 followed
> Companies House's Form MR01, registration certificate and full certified copy
> of the mortgage deed being filed and read: checklist item A6 is closed, and the charges register's
> further-advances entry is resolved as the deed's own standard clause 4.2, not a revolving
> facility. Version 8 followed the Land Registry official copies for TY59507 and the
> administrator's scheme valuation as at 5 April 2025: the loanback's 50 percent test verified at
> 49.58 percent and the 1,791.00 reimbursement to the principal employer confirmed paid. Version 7
> followed a pass through the open questions: the principal employer's
> company number and change of name settled from Companies House's emails, the 2019 and 2021 loan
> agreements identified as Holdings-to-Properties loans, and a consolidated letter to the
> administrator drafted. Version 6 followed the heads of terms, loan application, board minute and
> repayment schedule; version 5 the signed loan agreement. Version 4 followed
> the extraction of 23 more scheme documents from the owner's `SSAS` folder and the first search
> of the owner's Gmail. Version 3 followed the loanback security documents;
> version 2 followed the first six Raw items; version 1 was built at setup, before any
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

**Gmail holds documents the Wiki lists as missing.** The owner's mailbox was searched on
2026-09-06 (Session 4 entry): the repayment schedule, the Companies House and Land Registry
registration documents, two Deeds of Adherence and the 2021-22 accounts exist there as
attachments (the signed loan agreement did too, and was saved on 2026-09-07). The Gmail connector
reads bodies but **cannot download attachments**, so until a person saves them into `Raw/` they
are cited as `(email)` and remain "not on file". The working list, with filenames and thread
links, is `Outputs/attachments-to-download-from-gmail.md`; it is ticked and replaced as items
arrive.
Do not treat an email citation as equal to a filed document, and never send, reply to or forward
mail (section 6a).

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
Processes, Suppliers. `Employers/` was added 2026-09-06 with its first article; `Assets/` received
its first article the same day.

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
| Scheme financials and returns | None live. No QuickBooks connector exists for the scheme; do not use the group's Intuit connector, which on 2026-09-04 was found to point at Fishbone Properties Ltd. | Accounts and HMRC returns, when filed in `Raw/`, are the financial source. Year end is 5 April (administrator's email of 19/01/2023). |
| Scheme correspondence | Owner's Gmail (`minda@fishboneconstruction.co.uk`, also receiving the `fishbonedrylining` addresses), read-only through the Gmail connector | First searched 2026-09-06. Bodies readable; **attachments not downloadable by the tooling**. Cite by thread URL with `(email)`; the citation convention is in `Wiki/Processes/knowledge-base-operations.md`. Not a substitute for `Raw/`: a document found in mail is still "not on file" until saved. |

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
| Loanback monitor | Monthly | Confirm the borrower's monthly payment arrived in the scheme's bank account on time, recompute the balance against the agreement's schedule, flag any late or missing payment, flag the approach of the final payment date, and flag if the security's valuation basis has lapsed. Read-only. | The loan agreement of 16/04/2025, its repayment schedule and Metro Bank statements in `Raw/`. The security deed (2026-09-06), the agreement and the schedule (2026-09-07) are on file; only the statements are missing. |
| Compliance calendar | Monthly | From the Wiki: scheme year end, HMRC Pension Scheme Return and Event Report deadlines, trustee meeting cadence, any registration or declaration renewals. Rewrites `Outputs/risk-register.md`. Read-only. | Trust deed, HMRC registration and the administrator's timetable in `Raw/`. |
| Weekly Smartsheet sync | Weekly | Section 3a resync of the asset register into the Wiki. | ~~A `Wiki/Assets/` article exists.~~ Met 2026-09-06 (`Wiki/Assets/loanback-fishbone-commercial-properties.md`). Still needs an `FSS 0001` row to sync against, and the routine has not been created. |
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
- **Every PDF and image in `Raw/` is Drive-only and is never committed to git**, whatever it
  contains: the 36 filed on 2026-09-06 include signatures, bank details, an NI number, payroll
  figures and phone photographs, and the ones still to come are bank and administrator documents.
- A pension scheme's records are personal data about its members by nature. Treat every member,
  trustee, benefit, contribution and bank document as `sensitive: true`. Bank statements and
  member documents stay Drive-only and are never copied into git.
- **Member-personal folders do not belong in `Raw/` at all** (payslips, identity documents,
  personal bank statements, transfer and application forms). On 2026-09-06 the whole OneDrive
  master was dropped into `Raw/` and the owner moved it out again once it was flagged; a session
  that finds such material in `Raw/` reports it, registers it `skipped`, cites any scheme-level
  fact by URL without repeating personal figures, and does not copy it anywhere.
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

## 7. Scheme snapshot and open questions (as of 2026-09-08, after the second open-questions pass)

The Wiki is the authoritative record; start at `Wiki/index.md`. This section is a one-screen
orientation, refreshed when a Raw item changes the picture. Lines marked **verified** are cited in
a Wiki article from a document in `Raw/`; lines marked `(email)` rest on an email body in the
owner's Gmail whose attachment has not been saved; lines marked `(unverified)` are pointers found
elsewhere and must be recounted before use.

- **What it is (verified).** Fishbone SSAS, an occupational, defined-contribution,
  investment-regulated pension scheme: application 28/09/2021 `(email)`, governing documents
  signed by the company and both member trustees on or before 14/10/2021 (photographs; the
  administrator asked for them back undated so its director could date them `(email)`),
  commencement 28/10/2021, registered with HMRC on 03/12/2021 (PSTR 20005255RF) and with The
  Pensions Regulator on 04/08/2022 (PSR 12018880, two members at 03/12/2021). Established by
  Fishbone Drylining Ltd, company number 07948220 (the November 2023 re-declaration's 07948020 is
  a typing error), **renamed Fishbone Construction Ltd by special resolution notified to Companies
  House on 31/10/2024** `(email: Companies House's own acknowledgements; the certificate is not on
  file)`. Trustees: M Gaudiesius, A Prutkovas, **I Fedonina (joined 05/01/2024, on
  the bank mandate May 2024; her deed of appointment is at the administrator, not on file)** and
  Empowered Trustees Ltd (12291059). Administrator Empowered Pensions (Empowered Pensions Ltd
  04735293; Empowered Administration Ltd 14471886 trading as Empowered Pensions from 2025;
  Empowered Lending Ltd 14029489 for loans); current contact Claudine Mudali `(email)`. The trust
  deed and rules on file are unsigned, undated copies; the administration agreement is on file
  but unreadable by the tooling; the 2018 fee schedule is on file; the November 2023 schedule is
  in Gmail. **Scheme year end 5 April** `(email)`. Articles: `Processes/scheme-establishment-2021`,
  `Processes/scheme-rules`, `Finance/hmrc-registration`, `Finance/tpr-scheme-registration-2022`,
  `Finance/scheme-accounts-and-returns` (active from 2026-09-07), `Employers/*`, `People/*`,
  `Suppliers/empowered-pensions`.
- **Known asset: loanback to Fishbone Commercial Properties Ltd (verified in the main).** 41,500
  lent under **loan agreement LA01801 made 16/04/2025, on file since 2026-09-07**: 5.50 percent
  flat (no base-rate link), 8.25 percent default rate, repayable within five years of drawdown by
  equal capital instalments with interest monthly in arrears, early repayment without penalty,
  set-up and transaction fees of 395.00 and the legal costs borne by the borrower, ten events of
  default including a change of control, signed through Signable by all four trustees and by the
  borrower's two directors. Secured by a first legal mortgage dated 29/04/2025 over 145 High
  Street East, Wallsend NE28 7RL (part of title TY59507), executed by all four trustees and by the
  borrower (13687238) acting by M Gaudiesius and A Prutkovas; the deed caps borrowing at 50
  percent of the scheme's value. Completion costs 1,352.20, net advance 40,147.80, solicitors
  Dollman & Pritchard (ref AJA/FIS53.1). **Heads of terms (07/04/2025), the application
  (17/03/2025), the trustees' board minute and indemnity letter (18/03/2025, signed 04/04/2025)
  and the administrator's repayment schedule (ref K0555) are on file since 2026-09-07:** the
  property was declared to the lender at 145,000, and the schedule is **60 level payments of
  790.13 from 29/05/2025 to 28/04/2030**, the last 790.48, interest 5,908.15 in total, balance
  31,495.87 after the 28/08/2026 payment; that is what the borrower pays. **The agreement's
  clause 7 describes equal capital instalments instead**, so the contract wording and the
  schedule differ; the trustees should have the administrator confirm which governs. **Charge
  registered at Companies House (Form MR01, certificate given 08/05/2025) and at the
  Land Registry (charge dated 29/04/2025, entered 18/07/2025)**, all on file and verified since
  2026-09-07, including a full certified copy of the mortgage deed via the Companies House
  filing. The register's note that the chargees are under an obligation to make further advances
  (s.49(3) Land Registration Act 2002) is the deed's own clause 4.2, a standard covenant tied to
  the Maximum Amount, not a revolving facility. A repayment schedule was sent to RMT
  Accountants 17/12/2025 `(email)`. **The 50 percent test is verified at 49.58 percent**: the
  administrator's own scheme valuation puts the net assets at 83,701.24 on 5 April 2025, eleven
  days before the agreement, and no bank movement is evidenced between then and Drawdown. The
  March 2025 valuation of the security assumed repairs still in progress; **confirmed 2026-09-08
  from the FCP knowledge base**: the special assumption remains unmet, completion now due
  01/11/2026, and the valuation's three-month validity lapsed 05/06/2025. Two of the four trustees
  (M Gaudiesius, A Prutkovas) are also the borrower's own directors overseeing the repairs, so the
  knowledge is on both sides of the table by the FCP knowledge base's own account, though no
  formal notice to the trustees is on file either side. **RMT Accountants' understanding of the
  loan as 40,147.80 (the net advance) is answered**: the borrower's own accounts for the 18 months
  to 30/04/2025 record it at **41,500**, matching the trustees' figure (FCP knowledge base).
  Article: `Assets/loanback-fishbone-commercial-properties`. No `FSS 0001` row yet.
- **Bank (verified in part).** Metro Bank pension scheme account, opening request signed by both
  member trustees 31/10/2021; 2024 mandate on file adding the third trustee, signing rule one
  member trustee plus one authorised administrator together, single signature under 1,500;
  account number on the mandate, never quoted. Bank details were sent by the administrator on
  19/01/2023 `(email)`. **The loan advance left the account on 24/04/2025**, verified since
  2026-09-07 from the signed Metro Bank transfer form itself (Faster Payment, £41,500 to Dollman &
  Pritchard Solicitors, ref AJA/FIS53.1, signed by M Gaudiesius alone); whether the account's
  two-signature mandate (one member trustee plus one authorised administrator, above 1,500) was
  met some other way is not shown on the form. **No bank-issued statement is on file**, but the
  administrator's own
  transaction list for the year to 05/04/2025 (filed 2026-09-07) reproduces every entry on the
  account for that year: opening 86,061.69, closing 83,701.24, fees, interest and Irina Fedonina's
  contributions itemised. The year of the loanback itself (to 05/04/2026) is not yet covered.
  Fishbone Properties Ltd's Starling statements show weekly 35.00 payments to "Metro SSAS Account"
  `(unverified)`.
- **Transfers in and contributions (verified in part).** Three Aviva plans and one Nest plan;
  quoted values sum to 99,956.22 (Aviva) and about 107,196 with Nest (individual figures are in
  `Raw/`, not the Wiki). The first director's Aviva transfer was received June 2023 `(email)`;
  the second director's needed a MoneyHelper appointment in July 2023 and its completion is not
  evidenced; the third member's Aviva transfer drew amber flags in July 2025 and its completion
  is not evidenced `(email)`. Payroll pension contributions of the principal employer in
  December 2022 to May 2023 were labelled "Aviva Salary Sacrifice Pension"; the administrator
  says SSAS contributions are simply transferred to the Metro Bank account `(email)`; Fishbone
  Properties Ltd says it contributes for its employee. Nothing on file shows a contribution
  received. Articles: `Finance/transfers-in`, `Finance/contributions`.
- **Employers (verified in part).** Fishbone Drylining Ltd is the principal employer. Fishbone
  Properties Ltd (09687012) employs the third member; a Deed of Adherence for it was raised
  22/04/2025 and a signed scan returned 22/05/2025, completion not evidenced `(email)`. A Deed of
  Adherence for the borrower was sent 09/04/2025 and the administrator then said it was already
  adhered `(email)`. TPR re-declaration at 07/11/2023 lists the SSAS and Aviva; **next
  re-enrolment date is November 2026.** Article: `Employers/fishbone-properties-ltd`.
- **Where the legacy papers are.** The master is the owner's `SSAS` folder at the My Drive root
  (id `1jSFpIOcKb7yANA0hJVtjWb_80rMfvo5c`, 139 files), originally OneDrive `Documents/SSAS`. All
  scheme-level documents in it are now in `Raw/` (36 files); everything left is member-personal
  and stays out by the owner's instruction. Google Drive `Collaboration Space / Other / Staff
  (SSAS)` (`1Q7C8BIAD9pGfoBa9a-RF-EmGdS7xXqw0`) is an older partial copy. ~~Three loan agreement
  PDFs dated 2019 and 2021 sit loose in `Collaboration Space / Other`; whether they are scheme
  loans is unknown.~~ Read 2026-09-07: they are loans **from Fishbone Holdings Ltd to Fishbone
  Properties Ltd** (283,000 at 3.8 percent, 01/05/2019; 20,000 at 6 percent, 15/10/2021), now
  registered in the Fishbone Holdings Ltd knowledge base as FH0000010 and FH0000011; nothing to do
  with the scheme. The owner's Gmail is the third source (section 1).

**Open questions, in priority order.**
1. **Save the remaining Gmail attachments into `Raw/`** per
   `Outputs/attachments-to-download-from-gmail.md`: items A1 to A10 all arrived 2026-09-07 (the
   loan pack, the Land Registry official copies, the Companies House Form MR01 with certificate
   and full certified deed, and the signed Metro Bank transfer form); A11 was not needed, so
   **checklist group A (the loanback) is now closed**. Next: **the two Deeds of Adherence**, the
   2021-22 accounts, the 2021 establishment pack, the fee schedule and
   invoices. Then the `FSS 0001` row and `FSS0000001` onwards. Separately, **ask the administrator
   to confirm in writing that the level-payment schedule governs** despite the agreement's
   equal-capital wording. (The Land Registry's "obligation to make further advances" no longer
   needs asking about: it is the deed's own clause 4.2, read 2026-09-07.) A consolidated letter to
   Empowered covering the level-payment question and
   questions 2 to 8 below sits **unsent in the owner's Gmail drafts** (created 2026-09-07; text in
   `Outputs/change-log-2026-09-07-outstanding-items-pass.md`); sending it is the owner's decision.
2. ~~**The 50 percent test at 16/04/2025**~~ Answered 2026-09-07: the administrator's own scheme
   valuation puts the net assets at 83,701.24 on 5 April 2025, so the loan is 49.58 percent,
   verified. Still open: what the value was on the exact date the deed's 50 percent cap is tested
   against, though no bank movement is evidenced between 5 and 16 April that would change the
   answer.
3. **The third trustee and Fishbone Properties Ltd**: her deed of appointment (at the
   administrator), whether the Deed of Adherence was completed, whether TPR and HMRC were told.
   Checked again in Gmail 2026-09-08: no new evidence: still needs the administrator directly.
4. Whether the two other transfers in (second director, third member) completed, and when; the
   "Barnett Waddingham" answer given to Aviva.
5. Metro Bank statements from opening to date, so contributions, the advance and the repayments
   can be reconciled; the accounts and returns for 2022-23 and 2023-24 (only the 05/04/2024
   closing figure is known, from the 2024-25 accounts' comparative column), and the filing
   history.
6. ~~The 1,791.00 expense reimbursement to the sponsoring employer (November 2024): paid or not,
   and authorised.~~ Answered 2026-09-07: paid 02/12/2024, per the administrator's Metro Bank
   transaction list. Whether it was formally authorised beyond the trustee-expenses declaration
   is not addressed by that record.
7. ~~RMT Accountants' figure for the loan (40,147.80) against the trustees' 41,500.~~ Answered
   2026-09-08 from the FCP knowledge base: the borrower's own accounts for the 18 months to
   30/04/2025 record the secured loan at 41,500, matching the trustees; RMT's understanding of
   40,147.80 (the net advance) was not raised with RMT (section 6a).
8. The executed and dated trust deed and rules (at the administrator); the administration
   agreement's terms (a person needs to read the 8.8 MB scan; download failed again 2026-09-08,
   "session expired").
9. ~~Which company number is right (three documents say 07948220), and the Companies House record
   of the name change to Fishbone Construction Ltd.~~ Answered 2026-09-07 from Companies House's
   emails (07948220; NM01 notified 31/10/2024); still wanted: the change-of-name certificate, and
   whether HMRC, TPR and the administrator were told (checked again 2026-09-08: only a client-facing
   announcement letter of 20/11/2024 found, no certificate and no HMRC/TPR/administrator trail).
10. ~~Whether the 2019 and 2021 loan agreements in `Collaboration Space / Other` are scheme loans,~~
    Answered 2026-09-07: Holdings-to-Properties loans, not the scheme's. ~~Still open: whether the
    trustees know the security's valuation assumed repairs not complete.~~ Answered in part
    2026-09-08 from the FCP knowledge base: the assumption is still unmet (completion now due
    01/11/2026); two of the four trustees are also the borrower's directors overseeing the repair
    programme, so the knowledge is on both sides of the table by that knowledge base's own account,
    though no formal notice to the trustees (or from the professional trustee) is on file either
    side.
11. **The signed Metro Bank transfer form for the 41,500 loan advance carries
    only one signature** (M Gaudiesius, Primary Applicant); the 2024 mandate requires a member
    trustee and an authorised administrator together for a payment over 1,500, and Metro Bank's
    own form has no administrator signature line to check that against. **Read in full
    2026-09-08**: Empowered Lending's own release process asked only for a verbal bank-detail
    verification callback plus the one signature, not a second physical signature, which explains
    the form but does not show whether the bank mandate's own two-signature requirement was
    separately met.

---

*Standing context for the Fishbone SSAS knowledge base. Version 11, 2026-09-08, after a second
open-questions pass drawing on the FCP sister knowledge base and a full re-read of the transfer-
form email thread; version 10, the day before, followed the signed
Metro Bank transfer form for the loan advance being filed; version 9, earlier that day, followed
Companies House's Form MR01, certificate and full certified mortgage deed being filed; version 8,
earlier still, followed the Land Registry official copies and the administrator's scheme valuation
as at 5 April 2025; version 7 followed the pass through the open questions; version 6 followed the
loan pack, and version 5 the signed loan agreement; version 4 followed the `SSAS` folder
extraction and the first Gmail search, version 3 the loanback security and governing documents,
version 2 the first Raw items, and version 1 was created at setup from the Fishbone Commercial
Properties Ltd model. See `Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md`.*
