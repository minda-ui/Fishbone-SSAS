# Outputs

This folder holds four kinds of file.

**1. Deliverables** built from the wiki: reports, briefing notes, spreadsheets, letters.

- Name: `YYYY-MM-DD_<type>_<subject>.<ext>`.
- Each output records which wiki articles it was built from (inside the file or in a
  sidecar `.md` with the same name).
- Outputs are snapshots. Regenerate rather than edit when the wiki changes.
- Log every output in the `Outputs produced` table of `kb-registers.md`.

**2. Change-log entries**, one per session or run (see `CLAUDE.md` section 4).

- Name: `change-log-YYYY-MM-DD-<slug>.md`. A second run the same day takes its own slug; a
  follow-up to an entry already written takes `-addendum`, then `-addendum-2`.
- **Written once and never edited.** If an entry turns out to be wrong, write a new entry that
  references it rather than changing the old one.
- Add a row to the `Change-log entries` table of `kb-registers.md` so the chronology stays readable.

**3. `kb-registers.md`**, the standing indexes over the whole knowledge base: the change-log entry
index, `Processed items`, `Wiki structure changes` and `Outputs produced`. Unlike everything else
here it is current state, not a snapshot, so it is replaced by archive-then-recreate (`CLAUDE.md`
section 1) when a row is added.

**4. `Correspondence/`**, filed copies of numbered documents, one file per `FSS#######` entry in
the Smartsheet Document Register. Empty until the first number is issued. Its README gives the
filing procedure. Never put a file there without a register row behind it.

This file, `kb-registers.md` and `Correspondence/README.md` are not themselves outputs; all three
are registered `skipped` in `Processed items` so the section 3b Detect step does not re-flag them.
