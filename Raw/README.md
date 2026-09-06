# Raw

Inbox and source folder. Place new source material here exactly as received.

- Do not edit, rename or delete files after adding them. Add a new file for corrections.
- Preferred name: `YYYY-MM-DD_<source>_<short-description>.<ext>`. Verbal statements from a
  trustee or member are written up as `YYYY-MM-DD_owner-note_<subject>.md`, statement separated
  from commentary.
- **Nothing stays here unprocessed.** "Processed" means: the item has a row in the `Processed items`
  table of `../Outputs/kb-registers.md` with status `done` (every fact it carries is in a Wiki
  article that cites it) or `skipped` (with the reason). Until then its row says `pending` or
  `partial`, and the next session's Detect step (`CLAUDE.md` section 3b) will pick it up.
- The file itself is not moved once processed: it stays here as the citable source. What "leaves"
  Raw is the knowledge, into `Wiki/`. A file that turns out to belong to another entity's knowledge
  base is copied there and registered `skipped` here with a note saying where it went.
- This README is the exception: it is a folder guide, not source material, and is registered
  `skipped` so the Detect step does not keep re-flagging it.
- Sub-folders are fine; the change log records the full path from `Raw/`.

Expected first items for this scheme (none on file yet): the trust deed and rules, HMRC scheme
registration and Pension Scheme Tax Reference, the trustee and member list, the loanback agreement
with Fishbone Commercial Properties Ltd, Metro Bank statements, and the scheme's annual returns.
Several of these exist elsewhere on Drive (see `CLAUDE.md` section 7) and should be copied in, not
linked, so that this knowledge base can cite them.
