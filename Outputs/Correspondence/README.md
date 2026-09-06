# Correspondence

Filed copies of official documents the scheme issues or receives: trustee resolutions and minutes,
formal letters, and administrator, HMRC, bank, borrower, solicitor or valuer notices, incoming and
outgoing, post and email. Each is named by its permanent document number so the filed copy and the
register entry agree.

## The register

**Smartsheet `Document Register`, sheet id `2561022001022852`**, in the workspace
`Fishbone SSAS` (`4028917527930755`).
https://app.smartsheet.eu/sheets/g3jgjhG9wxGP3rq4Mq9g9vVvp67mC4fvc662PXX1

Created 2026-09-06 by cloning the Fishbone Holdings Ltd register (itself the FP and FCP schema), so
all four read alike: `Document No.` (primary), `Direction` (Outgoing/Incoming), `Date`, `Category`,
`Title`, `Entities involved`, `Description`, `Status` (Draft/Issued/Superseded/Void), `File link`,
plus the `Health` RYGB column formula.

**It is currently empty. No `FSS#######` number has been issued.** Until the first row exists,
this folder stays empty too.

## How a document gets filed

1. **The register issues the number, not the folder.** Add the row first; take the next number in
   sequence. Numbers are permanent and never reused: a superseded document keeps its number and is
   set to `Superseded`, and its replacement takes a new number. Nothing is renumbered.
2. **Number format `FSS0000001`**: prefix plus seven digits, zero-padded, no space. This matches
   the sister entities' `FP0000001`, `FCP0000001` and `FH0000001`, and is deliberately distinct from
   the *asset* register's `FSS 0001` (four digits, with a space), which numbers scheme assets, not
   documents.
3. **File the copy here** as
   `FSS#######_<direction>_<counterparty>_<subject>_<YYYY-MM-DD>.<ext>`, `direction` being `in` or
   `out`.
4. **Put the file's Drive link in the row's `File link` cell**, so the register entry and the filed
   copy point at each other. Where the document only ever existed as email, link the Gmail thread
   rather than leaving the cell blank.
5. Record the batch in that session's change-log entry.

## Rules

- **Never file a copy here without a register row behind it.** A filed copy with no entry implies a
  number that nothing issued, which is worse than no copy at all.
- **Automation is read-only against the register.** `CLAUDE.md` section 6a forbids writing to
  Smartsheet without an explicit human decision. The append exception proposed in section 5 has not
  been decided for this scheme, so every row is added by a person, or by an assistant acting on a
  specific instruction.
- Pension and member documents are sensitive by default (section 6b): the copy may live here on
  Drive, but personal data is not quoted into the Wiki; the article cites the file and sets
  `sensitive: true`.

## History

Created 2026-09-06 together with the register, so the numbering and the filing exist together
from the start rather than one preceding the other.
