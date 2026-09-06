---
title: "Decision: how this knowledge base is structured, and why every figure is recounted"
category: Decisions
status: active
sensitive: false
created: 2026-09-06
updated: 2026-09-06
sources:
  - ../../Outputs/change-log-2026-09-06-initial-setup.md
  - https://drive.google.com/drive/folders/1zC8LmkCLr7BEaqcAlxgAXyz5Bfm73Z7C
related:
  - ../Processes/knowledge-base-operations.md
---

# Decision: how this knowledge base is structured, and why every figure is recounted

**Decided by** the owner, 2026-09-06, at the setup of this knowledge base, by instruction to
follow the Fishbone group's standard structure as modelled on the Fishbone Commercial Properties
Ltd knowledge base (the group's most mature example).

## 1. The structure, and what each part is for

| Part | Why it exists |
|---|---|
| `CLAUDE.md` at the root | Standing context read first by every session. Rules that apply to every session live here; scheme-specific narrative does not. |
| `README.md` | One paragraph for a human, pointing at `CLAUDE.md`. Where the two differ, `CLAUDE.md` wins. |
| `Raw/` | The inbox and the only citable source. Files are never edited or renamed; a fact in the Wiki must trace back to a file here or to a live source. "Processed" means a `done` or `skipped` row in `Processed items`; nothing stays unregistered. |
| `Wiki/` | One fact per article, topic-organised, every article in `index.md`, every article with the front matter in `_templates/article.md` and a Changes table. This is the knowledge; everything else is plumbing. |
| `Outputs/` | Snapshots built from the Wiki, the dated change-log entries, and `kb-registers.md`. Deliverables are regenerated, not edited. |
| `Outputs/Correspondence/` | One filed copy per `FSS#######` row in the Smartsheet Document Register, so the number, the register entry and the copy always agree. |
| `Archive/` | Every superseded version of a standing file, renamed `<original> (archived YYYY-MM-DD, superseded by <reason>).<ext>`. The listing is the file's own changelog. |

### Wiki categories chosen, and the ones deliberately not created

The sister knowledge bases use `Properties`, `Tenants`, `Suppliers`, `People`, `Finance`,
`Processes` and `Decisions`. A pension scheme's business is different, so:

- **`Assets/` replaces `Properties/`.** What the scheme holds is loanbacks to sponsoring
  employers, a bank account, and possibly property or other investments. "Assets" covers all of
  them; "Properties" would cover one kind that is not yet known to exist. The Smartsheet register
  is named `Asset Register - Database` for the same reason.
- **`Suppliers/` stays**: the scheme has an administrator, a bank, and will have an accountant,
  a valuer and a solicitor.
- **`Tenants/` is not created.** The scheme lets no property on file. If it ever does, the
  tenant is recorded in the asset's article until a second tenant makes a category worth having.
- **`Contracts/` is not created.** The FCP index carries the heading with no folder behind it.
  Here a contract (the loanback agreement, a bank mandate) is filed under the asset, supplier or
  person it belongs to.
- **`People/`, `Finance/`, `Processes/`, `Decisions/` stay** as in every sister knowledge base.

A category is created when its first article exists, never before, and the creation is logged in
`Wiki structure changes`. Empty placeholder folders would make the Detect step and the index lie
about what is known.

### The prefix `FSS`

Chosen to sit beside the group's existing prefixes: `FP` (Fishbone Properties Ltd), `FCP`
(Fishbone Commercial Properties Ltd), `FH` (Fishbone Holdings Ltd), `FCD` (Fishbone Construction
Ltd). Two namespaces share it, following the FCP and FH convention exactly:

- `FSS0000001`: a document number, seven digits, no space. Matches `FP0000001`, `FCP0000001`,
  `FH0000001`. Every row of the Document Register and every file in `Outputs/Correspondence/`.
- `FSS 0001`: an asset id, four digits, with a space. Matches `FCP 0001` and `FH 0001`. Every row
  of the Asset Register.

They never collide. A session that reads one as the other has made an error.

### Smartsheet

The workspace is named `Fishbone SSAS`, the real name, never a Smartsheet default. The three
sheets were **cloned** from the Fishbone Holdings Ltd workspace rather than built from scratch, so
that column names, spelling, picklists and formulas stay identical across the group. The Holdings
register was chosen over the FCP one because it is the FCP register plus `Asset class` and
`Counterparty` columns, and because its health columns already carry the group's RYGB column
formulas, whereas the FCP register's are still manual picklists. The only schema changes made:
the `ID` and `Asset class` descriptions were reworded for the scheme, and `Loanback receivable`
was added to `Asset class`. Every at-risk field is governed by an RYGB formula copied unchanged:
`Health-Docs`, `Health-Lease`, `Health-Finance` on the register, `Health` on Tasks (Green = done or
due in over 6 weeks, Yellow = 2 to 6 weeks, Red = blocked, overdue or under 2 weeks, Blue = no due
date) and `Health` on the Document Register (Green = issued, Yellow = draft under 6 weeks,
Red = stale draft or no status, Blue = superseded or void). No new status scheme was invented.
`Owner` on Tasks is a contact column. `Reports & Dashboards` holds reports and sights only.

## 2. The recount rule

**Every session must recount facts and figures from the source, rather than trust a prior
session's stated numbers as standing fact.** This applies to a loan balance, a contribution total,
a payment date, a count of files, rows or open questions, and to anything copied from a sister
knowledge base. A number written down by an earlier session is a dated snapshot of what that
session believed; it is not evidence, and it goes stale without anyone editing it.

Concretely:

1. Before acting on a figure found in `CLAUDE.md`, a change-log entry, a Wiki article, a
   Smartsheet cell or a sister knowledge base, open the source it cites and recompute it. Cite
   the source and the date in whatever you write.
2. If the source cannot be reached, write the figure with `(unverified)` and the date and place
   it was last seen, and add an open question.
3. When a recount disagrees with the recorded figure, do not silently overwrite: record both,
   dated, in the article's Changes table and in the change-log entry, and correct `CLAUDE.md`
   section 7 by striking through the old value.
4. A colour in an RYGB column is a formula over dates that someone typed. Recompute from the
   dates; do not trust the colour.

**Why the rule exists.** Three failures in the sister knowledge bases in the fortnight before this
one was created, all recorded in the FCP `CLAUDE.md` and its Decisions articles:

- The FCP corpus survey of 2026-09-03 reported "all 20 files". A recount the next day found the
  Properties Ltd archive alone held 23 CLAUDE-titled files against the 16 reported. The first
  attempt at correcting it replaced the wrong 16 with an equally unverified 17, reasoning from the
  old number instead of counting.
- The Fishbone Properties Ltd context file carried a fabricated "known bug" about a spreadsheet
  total for 17 days, propagated into other documents, because nobody re-checked it against the
  live sheet.
- In a sister workspace on 02/09/2026 a bank statement's side-by-side tables flattened into
  interleaved columns and a real GBP 11,000 payment was missed by a session that trusted the
  extracted text.

For a pension scheme the stakes are higher than for a property company: loanback balances, the
rate against base rate, and contribution totals are what HMRC compliance rests on. A wrong number
inherited from a sister knowledge base and repeated here becomes a fact nobody can trace.

## 3. What was deliberately not done at setup

- No source material was filed in `Raw/` and no Wiki article about the scheme itself was written.
  Everything known at setup is pointers to documents elsewhere on Drive, listed in `CLAUDE.md`
  section 7 as `(unverified)`. Writing articles from pointers would have manufactured exactly the
  kind of untraceable fact the recount rule forbids.
- No Smartsheet row was added and no `FSS` number was issued. Numbers are permanent, so the first
  ones should be issued against real documents, by the owner's instruction.
- No routine was created; `CLAUDE.md` section 5 lists the proposals and their prerequisites.
- Access was not widened: owner only on Drive and Smartsheet.

## Open questions

- Whether the owner wants the legacy `Staff (SSAS)` Drive folder copied into `Raw/` wholesale or
  document by document. Copying is the recommended route so this knowledge base can cite files
  it controls.
- Whether the section 6a append exception (automation may append rows and comments to the
  Document Register and Tasks) should apply here. Undecided for FCP too.

## Changes

| Date | Change | Change-log ref |
|---|---|---|
| 2026-09-06 | Created at setup | `Outputs/change-log-2026-09-06-initial-setup.md` |

## Sources

- `../../Outputs/change-log-2026-09-06-initial-setup.md`, 2026-09-06: what was built and the ids.
- Fishbone Commercial Properties Ltd - Knowledge Base, Drive folder `1zC8LmkCLr7BEaqcAlxgAXyz5Bfm73Z7C`:
  `CLAUDE.md` version 2 (2026-09-03, corrected to 2026-09-05), sections 1, 4, 6d and 7;
  `Wiki/Decisions/2026-09-03-claude-md-v2-from-corpus.md`; `Outputs/change-log-2026-09-05-document-register-created.md`.
  Read 2026-09-06.
- Smartsheet workspace `Fishbone Holdings Ltd` (id `6810956824110979`): sheets `Investment Register - Database`
  (`2206154623158148`), `Tasks` (`3298244547446660`), `Document Register` (`6709754250528644`); column definitions read 2026-09-06.
