# 2026-09-06 - Session 1 - Initial setup

- Owner asked for a new knowledge base for **Fishbone SSAS**, the group's small self-administered
  pension scheme, following the group's standard structure as modelled on the Fishbone Commercial
  Properties Ltd knowledge base, plus the matching Smartsheet workspace. Both were built this
  session. Nothing has been filed into either yet; this entry records the empty structure so the
  next session can check it against the owner's specification before anything goes in.

## What was read first

- FCP knowledge base on Drive (`1zC8LmkCLr7BEaqcAlxgAXyz5Bfm73Z7C`): `CLAUDE.md` v2, `README.md`,
  `Raw/README.md`, `Outputs/README.md`, `Outputs/kb-registers.md`, `Outputs/Correspondence/README.md`,
  `Wiki/index.md`, `Wiki/_templates/article.md`, `Wiki/Decisions/2026-09-03-drive-primary-and-archiving.md`,
  and the change-log entries for the Smartsheet register and Document Register creations.
- Smartsheet: column definitions of the FCP `Property Register - Database` and `Document Register`;
  the Fishbone Holdings Ltd `Investment Register - Database`, `Tasks` and `Document Register`, and
  its two reports; the `4. Property maintenance` register and the `1. General` `Tasks` sheet for
  the RYGB convention.
- The Fishbone Group knowledge base's stub `Wiki/Org-Fishbone-SSAS.md`, the Loans wiki's SSAS
  loanback facility page, and a listing of the legacy Drive folder `Staff (SSAS)`.

## What was created: Google Drive

Root folder `Fishbone SSAS - Knowledge Base`, id `1Ow2wOI2hQE3ugsxeZqk2xf7P5f9IT7oV`, in My Drive
beside the sister knowledge bases.

```
Fishbone SSAS - Knowledge Base/
├── CLAUDE.md
├── README.md
├── Raw/README.md
├── Wiki/
│   ├── index.md
│   ├── _templates/article.md
│   ├── Assets/            (empty)
│   ├── Suppliers/         (empty)
│   ├── People/            (empty)
│   ├── Finance/           (empty)
│   ├── Processes/knowledge-base-operations.md
│   └── Decisions/2026-09-06-kb-structure-and-recount-rule.md
├── Outputs/
│   ├── README.md
│   ├── kb-registers.md
│   ├── change-log-2026-09-06-initial-setup.md   (this file)
│   └── Correspondence/README.md
└── Archive/               (empty)
```

Folder ids are in `Wiki/Processes/knowledge-base-operations.md`. Mirrored to git
`minda-ui/Fishbone-SSAS`.

Categories not created, deliberately: `Tenants/`, `Properties/`, `Contracts/`. Reasons in the
Decisions article. `Assets/`, `Suppliers/`, `People/` and `Finance/` are created empty because
each has a first article that plainly exists to be written (the loanback, the bank, the trustees,
the contributions); they are the four the next session will fill.

## What was created: Smartsheet

Workspace **`Fishbone SSAS`**, id `4028917527930755`.
https://app.smartsheet.eu/workspaces/mvpWVxqMpQQgm3HVV9fq98jgr97xffjh3pc3fp21

| Object | Id | Cloned from | Rows |
|---|---|---|---|
| `Asset Register - Database` | `4114082175256452` | Fishbone Holdings Ltd `Investment Register - Database` (`2206154623158148`), 65 columns, formulas intact | 0 |
| `Tasks` | `8617681802626948` | Fishbone Holdings Ltd `Tasks` (`3298244547446660`), 10 columns, `Owner` CONTACT_LIST, `Health` formula | 0 |
| `Document Register` | `2561022001022852` | Fishbone Holdings Ltd `Document Register` (`6709754250528644`), 10 columns, `Health` formula | 0 |
| folder `Reports & Dashboards` | `4148450360092547` | | |
| report `Open Tasks` | `6471752932788100` | Holdings report of the same name: Task ID, Health, Title, Owner, Due Date, Status, Source Doc No., Category; filter Status is not Done; sorted by Due Date | |
| report `Register Health` | `8718055188334468` | Holdings report of the same name: ID, Asset class, Counterparty, Status, Health-Docs, Health-Lease, Health-Finance, Loan, % Rate, Loan expiry / term end, Fixed Rate expires, Total Value, Note | |

Schema changes after cloning, both on the Asset Register: the `ID` column description now reads
`FSS 0001` and names the two namespaces; `Asset class` gained the option `Loanback receivable`
(first in the list) and a reworded description. Nothing else was renamed, retyped or reordered,
so the sheets stay comparable with the FP, FCP and FH ones column for column.

RYGB health formulas, all inherited unchanged from the Holdings sheets, which took them from the
`4. Property maintenance` and `1. General` convention: `Health-Docs` (Red under 2 weeks to the
earliest certificate expiry, Yellow 2 to 6 weeks, Green beyond, Blue none or not in operation),
`Health-Lease` (Red within 90 days of expiry, break or review, Yellow within 365, Green beyond,
Blue vacant or no dates), `Health-Finance` (Red within 30 days of term end or fixed-rate expiry,
Yellow within 90, Green beyond, Blue no dates), Tasks `Health` (Green done or over 6 weeks, Yellow
2 to 6 weeks, Red blocked, overdue or under 2 weeks, Blue no due date), Document Register `Health`
(Green issued, Yellow draft under 6 weeks, Red stale draft or no status, Blue superseded or void).

## Decisions recorded

- **Prefix `FSS`.** Documents `FSS0000001`; assets `FSS 0001`. See the Decisions article.
- **Recount rule** written into `CLAUDE.md` section 0 and the Decisions article: no session may
  treat a figure stated by an earlier session, a sister knowledge base or a Smartsheet cell as
  standing fact without recounting it from the source.
- Clone source was the Holdings workspace rather than FCP's, because Holdings is the FCP schema
  plus the columns a non-property entity needs, and already carries the formula health columns.

## What was deliberately not done

- **No Raw items filed.** The scheme's legacy papers sit in `Collaboration Space / Other /
  Staff (SSAS)` (`1Q7C8BIAD9pGfoBa9a-RF-EmGdS7xXqw0`). They were listed, not read or copied.
  `CLAUDE.md` section 7 points at them as `(unverified)`.
- **No Wiki article about the scheme itself.** Only the Decisions and Processes articles exist.
  Writing an Assets or People article from pointers would have created unsourced facts.
- **No Smartsheet row, no `FSS` number.** Numbers are permanent; the first are issued by the
  owner's instruction against real documents.
- **No routine, no sharing change.** Owner only on both systems.

## Knowledge base updated

- `Outputs/kb-registers.md` created with this entry indexed, four folder guides registered
  `skipped`, the structure rows, and the Smartsheet objects under Outputs produced.
- `Wiki/index.md` created listing the two articles and naming the four empty categories.

## Next step

For the owner, in order:
1. **Check the structure against the specification** before filing anything.
2. Say whether the `Staff (SSAS)` folder should be copied into `Raw/` wholesale or document by
   document; then the first processing session builds `People/`, `Finance/` and `Assets/` from
   the trust deed, the HMRC registration and the loanback agreement.
3. Decide whether the section 6a append exception applies to this workspace.
