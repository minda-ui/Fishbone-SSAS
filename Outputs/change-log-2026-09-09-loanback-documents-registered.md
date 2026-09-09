# Change log: the loanback's 13 documents registered FS0000001 to FS0000013

**2026-09-09, at the owner's request** ("register the loanback documents under FS"), following the
same-session adoption of the Group Document Numbering & Filing Policy v1.1
(`Outputs/change-log-2026-09-09-group-policy-adopted.md`).

## What was done

Checked the group Smartsheet **Document Register** (workspace `Fishbone Group - Documents`, sheet
id `7352854736144260`) first: it held two rows (`FA0000001`, `FC0000001`), neither a match by
Source key or by title for any loanback document (dedup-on-entry, satisfied). Then appended 13 new
rows, `FS0000001` to `FS0000013`, one per qualifying document already on file about the loanback to
Fishbone Commercial Properties Ltd:

| No. | Document | Category | Date |
|---|---|---|---|
| FS0000001 | Loanback Application V2.2024 | Loan | 17/03/2025 |
| FS0000002 | Board Minute and Indemnity Letter | Board minute | 18/03/2025 |
| FS0000003 | Loanback Heads of Terms EP/LB/60 | Loan | 07/04/2025 |
| FS0000004 | Loan Agreement LA01801 | Loan | 16/04/2025 |
| FS0000005 | Dollman & Pritchard invoice 33194 | Invoice | 16/04/2025 |
| FS0000006 | Dollman & Pritchard completion statement | Legal | (undated in the source) |
| FS0000007 | Legal Mortgage, 145 High Street East, Wallsend | Mortgage | 29/04/2025 |
| FS0000008 | Loanback repayment schedule (ref K0555) | Loan | 29/04/2025 |
| FS0000009 | Companies House Form MR01, certificate and certified deed | Certificate | 08/05/2025 |
| FS0000010 | HM Land Registry official copy of register, TY59507 | Title register | 18/07/2025 |
| FS0000011 | HM Land Registry official copy of title plan, TY59507 | Title plan | 24/01/2026 |
| FS0000012 | HM Land Registry registration completion sheet, TY59507 | Legal | 24/01/2026 |
| FS0000013 | Metro Bank transfer form (loanback drawdown) | Bank | 24/04/2025 |

Each row carries: Entity `FS - Fishbone SSAS`; Direction `Incoming` (all but FS0000002 and
FS0000013, which are `Internal` — the trustees' own governance record and the scheme's own bank
instruction); Status `Issued`; `Source key` the Drive file id of the document already in `Raw/`;
`File link` a direct Drive URL to that file; and a `Description` citing
`Wiki/Assets/loanback-fishbone-commercial-properties.md` (or `Wiki/Suppliers/dollman-pritchard.md`
/ `Wiki/Suppliers/metro-bank.md` where more specific) and cross-referencing related rows by number
(e.g. FS0000008's description notes it differs from FS0000004's clause 7 wording).

**Not registered under the group policy's own exclusions**: the administrator's scheme-wide 5
April 2025 valuation, portfolio valuation and statement of account (Finance-level documents about
the whole scheme, not the loanback transaction itself — a separate registration exercise if
wanted, not assumed here).

## What was left undone, and why

**Collaboration Space filing.** The group policy's filing step (move the file into the group's
shared Collaboration Space, co-located with the thing it belongs to, named
`<ID> - <Category> - <Short Title>.<ext>`) was not carried out. Checked the Collaboration Space
root (`1YNj5BIpKVzcmI4U1DRkgu7kcnSDizGEi`): Fishbone Properties Ltd, Fishbone Commercial
Properties, Fishbone Construction, Fishbone Waste and Furniture by Fishbone (Amfa) each have a
company-level folder there; **no "Fishbone SSAS" folder exists**. Creating one, or otherwise moving
these files into a shared space outside this KB's own Drive tree, is a step beyond the two narrow
exceptions the owner actually confirmed on `CLAUDE.md` section 6a (appending to the two named
Smartsheet sheets, and the `§7a` `Raw/` hand-off) — it was not assumed here. Each register row's
`Location` cell says so explicitly and points back to the file's current location in this KB's own
`Raw/` via `Source key` and `File link` instead. This is flagged as a new open item, not resolved
by guessing.

**Section 6a note.** Appending these 13 rows was the exception the owner explicitly adopted; no
new exception was taken for Collaboration Space filing, and no Drive folder was created or moved
without asking first.

## Wiki updated

`Wiki/Assets/loanback-fishbone-commercial-properties.md`: new paragraph naming all 13 document
numbers and the pending-filing note; the group Document Register cited as a source (footnote 28);
`related:` unchanged (no new entity introduced).

## Commit

`KB: register the loanback's 13 documents FS0000001-FS0000013 in the group Document Register, per
the owner's request; Collaboration Space filing flagged as pending, not assumed`
