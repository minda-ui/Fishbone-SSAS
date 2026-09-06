---
title: Knowledge base operations (Drive, GitHub, Smartsheet)
category: Processes
status: active
sensitive: false
created: 2026-09-06
updated: 2026-09-06
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
| Smartsheet | sheet `Document Register` | `2561022001022852` | https://app.smartsheet.eu/sheets/g3jgjhG9wxGP3rq4Mq9g9vVvp67mC4fvc662PXX1 |
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
scheme.

## Conventions in force

- Prefix `FSS`. Documents `FSS0000001` (seven digits, no space). Assets `FSS 0001` (four digits,
  with a space). See the Decisions article for why.
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

## Open questions

- None at setup beyond those in the Decisions article.

## Changes

| Date | Change | Change-log ref |
|---|---|---|
| 2026-09-06 | Created at setup | `Outputs/change-log-2026-09-06-initial-setup.md` |
| 2026-09-06 | Employers folder id, OneDrive source, history line | `Outputs/change-log-2026-09-06-legacy-scheme-documents-copied.md` |
| 2026-09-06 | History line: the owner uploaded the whole OneDrive master into `Raw/` and moved it out again to the My Drive root (`1jSFpIOcKb7yANA0hJVtjWb_80rMfvo5c`); the four scheme documents were copied from it by id; Drive downloads above about 8 MB fail in the connector | `Outputs/change-log-2026-09-06-loan-security-and-governing-documents.md` |
| 2026-09-06 | History line: Session 4's 23 copies and the first Gmail search; the email citation convention and the connector's attachment limit | `Outputs/change-log-2026-09-06-ssas-folder-extraction.md` |

## Sources

- `../../Outputs/change-log-2026-09-06-initial-setup.md`, 2026-09-06.
