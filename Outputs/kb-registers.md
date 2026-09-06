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

No source material has been filed in `Raw/` yet. Candidate first items are listed in
`Raw/README.md` and `CLAUDE.md` section 7.

## Wiki structure changes

| Date | Change | Reason |
|---|---|---|
| 2026-09-06 | Created `Wiki/index.md`, `Wiki/_templates/article.md`; category folders `Assets`, `Suppliers`, `People`, `Finance`, `Processes`, `Decisions` | Initial setup on the FCP model; `Assets` replaces `Properties` for a pension scheme; `Tenants`, `Properties` and `Contracts` deliberately not created |
| 2026-09-06 | Added `Wiki/Decisions/2026-09-06-kb-structure-and-recount-rule.md` and `Wiki/Processes/knowledge-base-operations.md` | Record why the structure is as it is, the `FSS` prefix, the recount rule, and the systems and ids in force |
| 2026-09-06 | Added `CLAUDE.md` (version 1) at the root as the standing context; `README.md` as a pointer | Owner instruction: follow the group standard |

## Outputs produced

| Output path | Date | Built from (wiki articles) | Requested by |
|---|---|---|---|
| Smartsheet: workspace `Fishbone SSAS` (`4028917527930755`) with sheets `Asset Register - Database` (`4114082175256452`), `Tasks` (`8617681802626948`), `Document Register` (`2561022001022852`), folder `Reports & Dashboards` (`4148450360092547`) holding reports `Open Tasks` (`6471752932788100`) and `Register Health` (`8718055188334468`) | 2026-09-06 | None. Schema cloned from the Fishbone Holdings Ltd workspace; all sheets empty | Owner |
