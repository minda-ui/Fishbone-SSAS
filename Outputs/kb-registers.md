# Knowledge base registers - Fishbone SSAS

Standing indexes over the whole knowledge base. Unlike the dated change-log entries beside this
file, which are written once and never touched again, this file is current state: it is replaced
(archive-then-recreate, per `CLAUDE.md` section 1) whenever a row is added.

Three of its four tables answer "what is the state of the knowledge base now", not "what happened
in a session". The fourth, the entry index, is the chronology.

## Change-log entries

One file per session or run, in `Outputs/`, newest first. Never edited after it is written; a
correction is a new entry that references the old one.

| Date | Entry | File |
|---|---|---|
| 2026-09-06 | Session 2 - OneDrive SSAS folder found; six legacy scheme documents copied from the Drive partial copy and processed; nine articles; Employers category | `Outputs/change-log-2026-09-06-legacy-scheme-documents-copied.md` |
| 2026-09-06 | Session 1 - Initial setup: Drive knowledge base and Smartsheet workspace created, empty | `Outputs/change-log-2026-09-06-initial-setup.md` |

## Processed items

Status: `pending` = registered, not started; `partial` = started, work remains (see notes);
`done` = fully reflected in the wiki; `skipped` = deliberately not processed (reason in notes).

| Raw path | Processed (date) | Status | Wiki articles created / updated | Notes |
|---|---|---|---|---|
| `Raw/README.md` | 2026-09-06 | skipped | none | Folder guide explaining `Raw/` to a human; structural file, not source material. Registered so section 3b Detect stops re-flagging it. |
| `Outputs/README.md` | 2026-09-06 | skipped | none | Folder guide explaining `Outputs/`; not an output and not source material. |
| `Outputs/kb-registers.md` | 2026-09-06 | skipped | none | This file. A standing index, not source material and not a deliverable. |
| `Outputs/Correspondence/README.md` | 2026-09-06 | skipped | none | Folder guide for the correspondence filing area. The folder is empty until the first `FSS#######` number is issued. |
| `Raw/Trust deed (Fishbone SSAS, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | 2026-09-06 | done | Processes/scheme-establishment-2021, Employers/fishbone-construction-ltd, People/m-gaudiesius, People/a-prutkovas, People/empowered-trustees | Unsigned, undated 4-page copy of the trust deed; rules referred to but not attached. Read as page images. 377,344 bytes. Drive only. |
| `Raw/Board minutes (Fishbone Drylining Ltd resolution to establish the scheme, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | 2026-09-06 | done | Processes/scheme-establishment-2021, Employers/fishbone-construction-ltd, People/m-gaudiesius, People/a-prutkovas, People/empowered-trustees, Suppliers/empowered-pensions | Unsigned, undated 1-page resolution of the directors of Fishbone Drylining Ltd to establish the scheme and appoint trustees and administrator. 237,322 bytes. Drive only. |
| `Raw/HMRC notification of registration 2021-12-06 (Certificates - Fishbone SSAS.pdf, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | 2026-09-06 | done | Finance/hmrc-registration, Processes/scheme-establishment-2021, Suppliers/empowered-pensions | HMRC form PODS 8, issued 06/12/2021 to Empowered Pensions Ltd: scheme registered 03/12/2021, PSTR 20005255RF. 2 pages, read as images. 704,718 bytes. A second scan of the same letter (708,681 bytes) sits in three member folders and was not copied. Drive only. |
| `Raw/TPR re-declaration summary 2023-11-07 (Redeclaration - 8. Summary and check, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | 2026-09-06 | done | Finance/tpr-re-declaration-2023, Employers/fishbone-construction-ltd, People/m-gaudiesius, Suppliers/empowered-pensions | Employer's automatic enrolment re-declaration "Summary and check" page, re-enrolment date 07/11/2023, 4 pages, text layer. Carries the submitter's phone number: sensitive. 128,236 bytes. Drive only. |
| `Raw/TPR re-declaration summary 2023-11-07 copy 2 (Redeclaration - 8. Summary and check 2, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | 2026-09-06 | done | Finance/tpr-re-declaration-2023 | Second draft of the same form, 5 pages; differs only in boilerplate and a repeated "Scheme 3" entry for the SSAS (diffed against copy 1). 133,879 bytes. Drive only. |
| `Raw/Metro Bank pension scheme account opening - signature page 2021-10-31 (Document_2021-11-01_103325.pdf, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | 2026-09-06 | done | Suppliers/metro-bank, Processes/scheme-establishment-2021, People/m-gaudiesius, People/a-prutkovas | Page 8 of Metro Bank's Pension Scheme Account Opening Request, declaration signed by both member trustees 31/10/2021. Signatures only, no account details. 197,748 bytes. Drive only. |

Documents known to exist but **not on file** (cannot be copied by the tooling; see the Session 2
entry): `Admistration Agreement.pdf`, `SASS price list.pdf`, `Schemes rules.pdf`,
`The Pension Regulator Certificate.pdf`, all in OneDrive `Documents/SSAS`. They get a row here
when a person drops them into `Raw/`.

## Wiki structure changes

| Date | Change | Reason |
|---|---|---|
| 2026-09-06 | Created `Wiki/index.md`, `Wiki/_templates/article.md`; category folders `Assets`, `Suppliers`, `People`, `Finance`, `Processes`, `Decisions` | Initial setup on the FCP model; `Assets` replaces `Properties` for a pension scheme; `Tenants`, `Properties` and `Contracts` deliberately not created |
| 2026-09-06 | Added `Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md` and `Wiki/Processes/knowledge-base-operations.md` | Record why the structure is as it is, the `FSS` prefix, the recount rule, and the systems and ids in force |
| 2026-09-06 | Added `CLAUDE.md` (version 1) at the root as the standing context; `README.md` as a pointer | Owner instruction: follow the group standard |
| 2026-09-06 | Created category `Wiki/Employers/` with `fishbone-construction-ltd.md`; category added to `index.md` and to the template | The principal employer is a first-class concept for a SSAS and fits none of the existing categories; created with its first article per section 1 |
| 2026-09-06 | Added `Processes/scheme-establishment-2021.md`, `People/m-gaudiesius.md`, `People/a-prutkovas.md`, `People/empowered-trustees.md`, `Suppliers/empowered-pensions.md`, `Suppliers/metro-bank.md`, `Finance/hmrc-registration.md`, `Finance/tpr-re-declaration-2023.md`; `index.md` rebuilt | First six Raw items processed (Session 2) |
| 2026-09-06 | `CLAUDE.md` replaced by version 2; `knowledge-base-operations.md` gained the Employers id, the OneDrive source and a history line | Session 2: the legacy source turned out to be OneDrive, and section 7 could be rebuilt from filed documents |

## Outputs produced

| Output path | Date | Built from (wiki articles) | Requested by |
|---|---|---|---|
| Smartsheet: workspace `Fishbone SSAS` (`4028917527930755`) with sheets `Asset Register - Database` (`4114082175256452`), `Tasks` (`8617681802626948`), `Document Register` (`2561022001022852`), folder `Reports & Dashboards` (`4148450360092547`) holding reports `Open Tasks` (`6471752932788100`) and `Register Health` (`8718055188334468`) | 2026-09-06 | None. Schema cloned from the Fishbone Holdings Ltd workspace; all sheets empty | Owner |
