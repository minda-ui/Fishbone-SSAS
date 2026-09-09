# Change log: group document numbering & filing policy (v1.1) adopted in full

**2026-09-09, later the same session** that flagged the "Fishbone Group" policy notice as
unverified (`Outputs/change-log-2026-09-09-group-policy-notice-flagged.md`, `CLAUDE.md` version
12), the owner was asked directly whether it was genuinely theirs and, if so, which parts to
adopt. The owner answered: adopt **completely all** of it, and confirmed the notice is "genuinely
mine / a real group decision."

## What was done before acting on that confirmation

An explicit human decision resolves an ambiguous finding (`CLAUDE.md` section 6a), but the scope
here — a governance change, a new standing Smartsheet write, and a capability to write into
sibling companies' knowledge bases — was serious enough to verify independently rather than act on
the two-word confirmation alone:

- **Re-read the flagged file in full** (`Raw/2026-09-09_group-policy_document-numbering-and-filing-v1.1.md`,
  Drive id `1GuA2WaDGvQLN6icSvT7iKmRk5SxnGCIi`) to get the exact rules rather than working from the
  earlier summary: the ID scheme (`<PREFIX>` + 7 zero-padded digits), the per-entity prefix table
  (`FC`/`FP`/`FH`/`FW`/`FA`/`FM`/`FS`/`FG`), the dedup-on-entry rule, what qualifies for a number,
  the Collaboration Space filing convention, the `§7a` inter-KB hand-off procedure, and the
  Smartsheet URLs and sheet ids for the group Document Register (`7352854736144260`) and Document
  System - Change Requests (`8918834172004228`).
- **Checked whether the two group Smartsheet sheets are actually reachable**: both are. The
  Document Register already carries one row, `FA0000001` (Amfa Furniture Ltd, a Companies House
  change-of-name certificate), noted on the row itself as "First registration on the group
  Document Register (proof-of-concept end-to-end run)". The Change Requests sheet is reachable and
  empty.
- **Checked Drive permissions** on a sibling knowledge base's root folder (Fishbone Commercial
  Properties Ltd, id `1zC8LmkCLr7BEaqcAlxgAXyz5Bfm73Z7C`, previously known to this KB only as a
  read source for cross-referencing the loanback): the only permission on it is `minda@
  fishboneconstruction.co.uk` as owner. No other collaborator.
- **Found and read the "Fishbone Group" knowledge base itself** (Drive `1pOHvl8X64E-x3rRb-6Wrc9zsHZ2mgi73`,
  referenced in this KB's own Wiki since 2026-09-06 as the source of the `Org-Fishbone-SSAS.md`
  stub, but not previously read in full). It is a real, mature, actively maintained database dating
  to 2026-09-03, with its own `CLAUDE.md`, `README.md`, `WORKFLOW.md` and four standing control
  files (`current-state.md`, `open-issues.md`, `external-source-register.md`,
  `processed-items-ledger.md`), all owned by `minda@fishboneconstruction.co.uk`, with dozens of
  real processed-item rows and resolved open issues going back to early September. Its
  `current-state.md`, last updated 2026-09-09, independently records: standing up the "centralised
  group Document Register system" that day (the same two Smartsheet sheets, the same ids); the
  policy amended to v1.1 the same day, adding the `§7a` inter-KB hand-off; and — matching the Drive
  permissions check above exactly — "confirmed 2026-09-09 that all six group `Raw/` folders (group
  + the five sister KBs) are owned by minda@ and the automations run as minda@, so minda@ already
  has write to every `Raw/`." It also records what is *not* yet done: "Pending (Minda): share the
  Smartsheet workspace (Editor) to each company's `info@` and `irina@fishboneproperties.co.uk` (the
  assistant cannot set Smartsheet sharing)."

This is independent, cross-referenced corroboration from a genuinely separate, long-established
database, not just the say-so of the flagged file or a bare "yes" in chat: the group KB's own
account of what it did today matches, in specific detail (sheet ids, the same-day v1.1 amendment,
the same Drive-ownership reasoning), what the flagged file asked this KB to adopt.

## What was adopted

Per the owner's "completely all" answer:

1. **Register prefix and numbering.** This scheme's own *documents* (not assets) now register in
   the group's one Smartsheet Document Register under `FS` + seven zero-padded digits
   (`FS0000001` onward), not this KB's own local Document Register (sheet id `2561022001022852`),
   which is superseded for new entries. That local sheet never held a row, so there is no
   back-catalogue to migrate for this scheme (unlike Properties `FP…` and Holdings `FH…`, which
   the group policy keeps live for now pending a later migration). Asset ids are untouched: `FSS
   0001` (four digits, with a space) remains this scheme's own convention in its own Asset
   Register - Database, which the group policy does not cover.
2. **Reference the policy as adopted.** `CLAUDE.md` section 1's Register conventions and
   `Wiki/Processes/knowledge-base-operations.md`'s "Conventions in force" both now describe the
   `FS` scheme, dedup-on-entry, what qualifies, Collaboration Space filing and the `§7a` hand-off,
   citing the group's `Wiki/Process-Document-Numbering-and-Filing.md` (v1.1) as the canonical
   source.
3. **Smartsheet write access.** `CLAUDE.md` section 6a gains a narrow, dated exception: automation
   may append rows (never edit or delete another entity's row) to the group Document Register and
   Change Requests sheets. This does not extend to the three Fishbone SSAS workspace sheets (Asset
   Register, this KB's own Document Register, Tasks), which remain fully read-only as before.
4. **Inter-KB `Raw/` hand-off.** `CLAUDE.md` section 6a also gains a narrow, dated exception
   permitting the `§7a` procedure exactly as written: only for a document already on the group
   register, add-only into the receiving KB's `Raw/`, with a covering note, annotating (never
   duplicating) this scheme's own register row. No hand-off has been needed yet.

`CLAUDE.md` open question 12 is resolved (struck through with the resolution recorded in place,
per section 6d rule 2); the file is now version 13. The heading list and every `section n`
cross-reference were checked to survive the edit, per section 6d rule 1.

## What was not done

- **No document has yet been registered** under `FS` for this scheme. The natural first
  candidates are the loanback's own paperwork (the loan agreement, mortgage deed, MR01, Land
  Registry charge, repayment schedule, etc.), but assigning the `FSS 0001` asset row and the first
  `FS` document numbers is a larger, already-flagged task (open question 1) and was not done
  speculatively in this session.
- **No `§7a` hand-off was performed.** There is currently no document this scheme needs to pass to
  a sibling KB, so the capability was adopted as a standing rule, not exercised.
- **No Smartsheet write was made** to the group Document Register or Change Requests sheet in this
  session; only reads, to verify reachability.
- The Raw file that started this (`2026-09-09_group-policy_document-numbering-and-filing-v1.1.md`)
  is left exactly where it is; the group policy explicitly asks that it not be assigned a document
  number.
- The scope of this adoption is this specific, dated confirmation. A future file proposing a
  different version, a different workspace, or a wider exception is not covered by it and should
  be treated as unverified in its own right (`CLAUDE.md` open question 12's closing note).

## Commit

`KB: adopt the Fishbone Group document numbering & filing policy v1.1 in full, per the owner's
explicit confirmation, independently verified against the group knowledge base; CLAUDE.md version
13`
