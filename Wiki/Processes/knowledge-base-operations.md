---
title: Knowledge base operations (Drive, GitHub, Smartsheet)
category: Processes
status: active
sensitive: false
created: 2026-09-06
updated: 2026-09-09
sources:
  - ../../Outputs/change-log-2026-09-06-initial-setup.md
related:
  - ../Decisions/2026-09-06-kb-structure-and-recount-rule.md
---

# Knowledge base operations (Drive, GitHub, Smartsheet)

The systems this knowledge base runs on, their ids, the conventions in force, and the full text of
the rules that `CLAUDE.md` summarises. `CLAUDE.md` states the boundary; this article carries the
detail.

## Systems and ids

| System | Object | Id | Notes |
|---|---|---|---|
| Google Drive | `Fishbone SSAS - Knowledge Base` (root) | `1Ow2wOI2hQE3ugsxeZqk2xf7P5f9IT7oV` | Primary copy. Owner only at 2026-09-06. |
| Google Drive | `Raw/` | `1ntYVPRv8xacjjIYqrMi9EVBVv_0PUzuj` | |
| Google Drive | `Wiki/` | `11BDCN8sZkkaUbIBhh_M678CSxT0aSsZc` | |
| Google Drive | `Wiki/_templates/` | `1C0Wpd38AOGPyTSyF6QY4hIZx31te1bUC` | |
| Google Drive | `Wiki/Assets/` | `1AjPA9rBMKc1l6cxkfShqChmQLviRYStC` | |
| Google Drive | `Wiki/Employers/` | `1L1pXYtz6V23Ux9RemPzgwmlnBS98IeCY` | Created 2026-09-06 with its first article. |
| Google Drive | `Wiki/Suppliers/` | `1dsyopaf7I56WYlCe9aodmBDgBevqbuDs` | |
| Google Drive | `Wiki/People/` | `18n0ICd5Xhq4J9nXqEVNqubmArAdJuU8R` | |
| Google Drive | `Wiki/Finance/` | `1faqBE6PO43FL2rhaph1vfoK3PvIRd9cx` | |
| Google Drive | `Wiki/Processes/` | `18wSOoqkksBJyB2AvNeV9xYP8rRXxVTDn` | |
| Google Drive | `Wiki/Decisions/` | `1tttRSI8ai7g8CPbKsvB5Q7ElRZ5qRGBU` | |
| Google Drive | `Outputs/` | `1UexLyW2u4xI2S0vPSxFiP1ajVlURvD03` | |
| Google Drive | `Outputs/Correspondence/` | `1imVVuNyQrGDV4wz2FFIi3eU_qhNDuqx_` | |
| Google Drive | `Archive/` | `1BdaI30eW8-d9sZHII3Wc2h4pfvNoqPb2` | |
| GitHub | `minda-ui/Fishbone-SSAS` | | Mirror, synced from Drive. Drive-only files are never committed. |
| Smartsheet | workspace `Fishbone SSAS` | `4028917527930755` | https://app.smartsheet.eu/workspaces/mvpWVxqMpQQgm3HVV9fq98jgr97xffjh3pc3fp21 |
| Smartsheet | sheet `Asset Register - Database` | `4114082175256452` | https://app.smartsheet.eu/sheets/Fvm62Rqgp9QFcr574P7pgGMrqH7gfRX8G6Fj2MW1 |
| Smartsheet | sheet `Tasks` | `8617681802626948` | https://app.smartsheet.eu/sheets/2pR6xcwVqwggXxFWhHvhWGqV5HRxrg43R4g3qFj1 |
| Smartsheet | sheet `Document Register` (this KB's own) | `2561022001022852` | https://app.smartsheet.eu/sheets/g3jgjhG9wxGP3rq4Mq9g9vVvp67mC4fvc662PXX1 — superseded for new entries 2026-09-09; never held a row. |
| Smartsheet | workspace `Fishbone Group - Documents` | `5815486484113283` | Adopted 2026-09-09. |
| Smartsheet | sheet `Document Register` (group) | `7352854736144260` | https://app.smartsheet.eu/sheets/4W2xwP9c2gfCpvWPGJmPHg2P2QwJfxPmWXpCvC21 — where this scheme's new documents are numbered from 2026-09-09 (`FS` prefix). Automation may append rows only. |
| Smartsheet | sheet `Document System - Change Requests` (group) | `8918834172004228` | https://app.smartsheet.eu/sheets/hrx6rP255gm8qVVQgX47GjQmqHGWRf576Vmm5hF1 — feedback queue for the group policy. Automation may append rows only. |
| Smartsheet | folder `Reports & Dashboards` | `4148450360092547` | Reports and sights only. |
| Smartsheet | report `Open Tasks` | `6471752932788100` | Tasks where Status is not Done, by Due Date. |
| Smartsheet | report `Register Health` | `8718055188334468` | Id, class, counterparty, the three health columns, loan terms, value, note. |

**Legacy source of the scheme's papers:** OneDrive of `info@fishbonedrylining.onmicrosoft.com`, folder
`Documents/SSAS` (drive `b!qDoSBVJDtU2A7ycK1dJS-aPdON0W8lNHvktFsewN0k69J-Fpz23-TIiSYUWNAuiA`, item
`016RXTF4M6XCHJJG5CPRE3YHGRYE5RVFLJ`), created October 2021, last activity April 2025. The Google Drive
folder `Collaboration Space / Other / Staff (SSAS)` (`1Q7C8BIAD9pGfoBa9a-RF-EmGdS7xXqw0`) is a partial copy of
it made in November 2024. **Bytes cannot be pulled from OneDrive by the tooling** (the egress proxy blocks the
SharePoint host and the Microsoft 365 connector returns extracted text only, which is empty for scanned PDFs),
so copying into `Raw/` is done from the Google Drive copy with `copy_file`; anything that exists only on
OneDrive has to be dragged across by a person.

Sister knowledge bases, for linked facts: `Fishbone Commercial Properties Ltd - Knowledge Base`
(Drive `1zC8LmkCLr7BEaqcAlxgAXyz5Bfm73Z7C`, Smartsheet workspace `3788897575561091`);
`Fishbone Holdings Ltd` (Smartsheet workspace `6810956824110979`); `Fishbone Group` knowledge base
(Drive `1pOHvl8X64E-x3rRb-6Wrc9zsHZ2mgi73`), whose `Wiki/Org-Fishbone-SSAS.md` is a stub about this
scheme. **Read in full 2026-09-09** while verifying the group document-numbering policy before
adopting it: a real, active database dating to 2026-09-03, with its own `CLAUDE.md`,
`current-state.md`, `open-issues.md`, `external-source-register.md` and `processed-items-ledger.md`
control files and a `Wiki/Process-Document-Numbering-and-Filing.md` article (v1.1) that is the
canonical source of the policy summarised below.

## Conventions in force

- Assets: prefix `FSS`, four digits with a space (`FSS 0001`), in this KB's own Smartsheet Asset
  Register. See the Decisions article for why.
- **Documents, adopted 2026-09-09: the group's `FS` prefix**, seven digits, no space
  (`FS0000001`), registered in the group-wide Smartsheet Document Register rather than this KB's
  own (both now `Systems and ids` rows above). Per-entity prefixes across the group: `FC`
  Construction, `FP` Properties, `FH` Holdings, `FW` Waste, `FA` Amfa Furniture, `FM` Commercial
  Properties, `FS` SSAS, `FG` group-level. Numbers are never reused; a superseded document keeps
  its number, marked `Superseded`/`Void`, and the replacement gets a new one that references it.
  **Dedup-on-entry**: before minting a number, search the group register by **Source key** (the
  document's Drive file id, or a Gmail thread id) and by title + date + counterparty; reuse the
  matching id if one exists. **What qualifies**: statutory accounts, certificates, title
  registers/plans, leases and tenancies, loan/mortgage documents, board/intercompany letters and
  minutes, legal/lender/insurer/Companies House/HMRC correspondence, valuations,
  completion/redemption statements, property- or project-tied invoices and receipts. Not
  registered: marketing, generic bills with no property/entity tie, duplicates, routine automated
  notifications. **Filing**: the group's shared Collaboration Space library, co-located with the
  thing the document belongs to, named `<ID> - <Category> - <Short Title>.<ext>`; move (never
  copy) to preserve the file id so existing links keep resolving. **Inter-KB hand-off (`§7a`)**:
  a document already on the group register may be dropped, as a new file under its existing ID,
  into a sibling KB's `Raw/` inbox with a short covering note
  (`YYYY-MM-DD_handoff_<fromEntity>-to-<toEntity>_<ID>.md`); the sender annotates its own register
  row (`Direction = Internal`, "sent to `<KB>` `<date>`") rather than creating a second number or
  row; the receiver reuses the ID already in the filename and never re-numbers it. This is the
  only write this KB may make into another knowledge base (`CLAUDE.md` section 6a). Feedback on
  the policy (an ambiguity, a document that doesn't fit) goes to the group's Document System -
  Change Requests sheet, never a local fork of the rules.
- Dates in filenames and front matter are ISO `YYYY-MM-DD`. Dates in prose may be UK `DD/MM/YYYY`
  when quoting a document that uses them.
- Money is written as a plain number in GBP unless the source is in another currency. No currency
  symbol in tables, to keep them sortable.
- Wiki filenames are kebab-case and carry no date, except Decisions articles, which are prefixed
  with the decision date.

## Wiki maintenance rules, in full

1. One subject per article. If an article starts covering two things, split it and cross-link.
2. Front matter is mandatory and follows `_templates/article.md` exactly: `title`, `category`
   (one of the existing category folders), `status` (`draft | active | superseded | archived`),
   `sensitive`, `created`, `updated`, `sources` (every Raw file or live URL cited), `related`
   (every article linked, kept bidirectional).
3. Every fact carries a citation: a footnote to a Raw file with a page, sheet, clause or email
   date, or the live source URL with the date read. A statement with no citation is marked
   `(unverified)`.
4. A figure copied from a sister knowledge base, an earlier session or `CLAUDE.md` section 7 is
   not a citation. Recount it from the document, or mark it `(unverified)`.
5. Links between articles are relative and kebab-case. Link the first mention of any entity. Add
   the target to `related:` on both ends. Never link to `Outputs/`.
6. A link to an article that does not exist yet is satisfied by creating a `draft` stub with an
   "Open questions" section, never by leaving a dead link.
7. Personal data (bank details, National Insurance numbers, dates of birth, home addresses,
   individual benefit and contribution figures) is never quoted into the Wiki. Cite the Raw file
   and set `sensitive: true`. Member and trustee articles are `sensitive: true` by default.
8. Every article ends with a Changes table naming the change-log entry behind each edit, and a
   Sources list. Bump `updated` on every edit.
9. Every article is listed in `Wiki/index.md`, alphabetically within its category, in the form
   `- [Title](Category/file.md) - one-line description`.
10. Superseding an article: set the old one `status: superseded`, add a note at the top naming the
    replacement, and archive-then-recreate on Drive. Never delete.

## Raw processing workflow, in full

1. **Detect.** List `Raw/` on Drive (and any sub-folders). Diff the listing against the
   `Processed items` table of `Outputs/kb-registers.md`. Ignore rows registered `skipped`. Anything
   not in the table is new.
2. **Register.** Add a `pending` row for each new item before reading it: path, size, what it
   appears to be from its name, whether it is Drive-only.
3. **Read and classify.** Read the item respecting `CLAUDE.md` section 3d (side-by-side tables
   and HMRC forms as images). Decide which categories and existing articles it touches. If it
   belongs to another entity's knowledge base, copy it there, register it `skipped` here with the
   destination, and stop.
4. **Extract.** List the facts it establishes, each with its location in the document. Note
   contradictions with anything already in the Wiki.
5. **Update the Wiki.** Create or update articles per the rules above. Cite every fact. Add
   reciprocal `related:` links. Move any figure the item changes into the article's Changes table
   with the old and new values.
6. **Check.** Front matter valid, links resolve both ways, `index.md` lists every article,
   `sensitive` set where needed, nothing personal quoted.
7. **Log.** Set the row to `done`, or `partial` with a note saying what remains. Write the
   session's change-log entry. Add rows to `Wiki structure changes` for any new or renamed
   article or category. Refresh `CLAUDE.md` section 7 if the picture changed (archive-then-recreate).
8. **Outputs only when requested.** Do not generate deliverables unprompted.
9. **Commit.** Mirror Drive to git, one batch per commit, message
   `KB: process <n> raw items (<summary>)`. Drive-only files are not committed.

## History

- 2026-09-06: knowledge base and Smartsheet workspace created at setup. No Raw items, no
  Smartsheet rows, no document numbers.
- 2026-09-06, later: the OneDrive `SSAS` folder found and inventoried; six scheme-level documents
  copied from the Google Drive partial copy into `Raw/` and processed; `Wiki/Employers/` created
  with its first article; nine articles written. Still no Smartsheet rows and no document numbers.
- 2026-09-06, Session 4: 23 further scheme documents copied from the owner's `SSAS` folder (My
  Drive root) into `Raw/`; the owner's **Gmail** searched for the first time and found to hold, as
  attachments, most of the documents the Wiki lists as missing (loan agreement, repayment
  schedule, registration certificates, deeds of adherence, 2021-22 accounts). **The Gmail
  connector reads thread bodies and lists attachment names but cannot download attachments**;
  a person saves them into `Raw/`. Email facts are cited by thread URL
  (`https://mail.google.com/mail/u/0/#all/<threadId>`) with the marker `(email)` and, where the
  fact rests on an attachment, `(attachment not on file)`; an email citation is weaker than a
  filed document and is superseded once the document reaches `Raw/`. Search results over about
  60 KB and long threads are written to the session's tool-results folder and parsed with
  Python. Phone photographs (JPEG) are decoded with PyMuPDF because PIL is not installed.
- 2026-09-07: the owner saved the first attachment from the download checklist
  (`Outputs/attachments-to-download-from-gmail.md`) into `Raw/`: the signed loan agreement
  LA01801. Processed the same day; the checklist is ticked and replaced as items arrive.
- 2026-09-09: a file claiming to be a "Fishbone Group" document numbering & filing policy notice
  (v1.1) appeared in `Raw/`, initially flagged as unverified rather than adopted (`CLAUDE.md`
  version 12). The owner then explicitly confirmed it was genuinely theirs and asked for full
  adoption; this session independently verified the group knowledge base, its Document Register
  and Change Requests Smartsheet sheets, and the Drive-ownership basis for the policy's `§7a`
  hand-off before adopting. Documents (not assets) now register under the group's `FS` prefix;
  this KB's own, never-used, local Document Register is superseded for new entries. `CLAUDE.md`
  version 13.

## Open questions

- None at setup beyond those in the Decisions article. No document has yet been registered under
  `FS` for this scheme, and the `§7a` inter-KB hand-off has not yet been used.

## Changes

| Date | Change | Change-log ref |
|---|---|---|
| 2026-09-06 | Created at setup | `Outputs/change-log-2026-09-06-initial-setup.md` |
| 2026-09-06 | Employers folder id, OneDrive source, history line | `Outputs/change-log-2026-09-06-legacy-scheme-documents-copied.md` |
| 2026-09-06 | History line: the owner uploaded the whole OneDrive master into `Raw/` and moved it out again to the My Drive root (`1jSFpIOcKb7yANA0hJVtjWb_80rMfvo5c`); the four scheme documents were copied from it by id; Drive downloads above about 8 MB fail in the connector | `Outputs/change-log-2026-09-06-loan-security-and-governing-documents.md` |
| 2026-09-06 | History line: Session 4's 23 copies and the first Gmail search; the email citation convention and the connector's attachment limit | `Outputs/change-log-2026-09-06-ssas-folder-extraction.md` |
| 2026-09-07 | History line: the first Gmail attachment saved by the owner and processed | `Outputs/change-log-2026-09-07-loan-agreement-filed.md` |
| 2026-09-09 | Group document policy adopted: document numbering moved to the group `FS` register; systems-and-ids table and conventions updated | `Outputs/change-log-2026-09-09-group-policy-adopted.md` |

## Sources

- `../../Outputs/change-log-2026-09-06-initial-setup.md`, 2026-09-06.
