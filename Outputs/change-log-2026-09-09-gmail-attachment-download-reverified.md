# Change log: Gmail attachment download re-verified as still unavailable

**2026-09-09, at the owner's request** ("save the remaining Gmail attachments into `Raw/`"),
following the Collaboration Space filing earlier the same session
(`Outputs/change-log-2026-09-09-collaboration-space-filing.md`).

## What was checked

`CLAUDE.md` section 0 already states, from the 2026-09-06 Session 4 finding, that "the Gmail
connector reads bodies but cannot download attachments." Per section 0's own recount rule, this
was re-verified against this session's actual tooling rather than repeated on trust:

- `mcp__Gmail__get_message` and `mcp__Gmail__get_thread`, called with `messageFormat: FULL_CONTENT`
  (the format that includes `attachments`), were inspected directly. Tested live against the
  thread for checklist item B1 (`195f547bc88cc4d4`, the borrower's blank Deed of Adherence): each
  attachment object returned only three fields — `filename`, `mimeType`, and an opaque `id` (an
  encoded string, not a Drive file id or a usable download token). No field carries the file's
  bytes, and no `base64`/`content`/`data` field is present.
- No tool equivalent to a `GetMessageAttachment` call (fetch-by-attachment-id) is exposed in this
  session's Gmail toolset. The `create_draft`/`send_message` tools' own `Attachment` schema
  documents such an ID as "retrievable in a separate `GetMessageAttachment` request", confirming
  the underlying Gmail API supports it, but no callable tool wraps it here.

**Conclusion: the limitation is confirmed unchanged.** Nothing in this session's tooling can turn
an attachment's metadata into a saved file in `Raw/`. This is not a permissions or workspace
question (unlike the group-policy and Collaboration Space findings earlier this session) — it is a
tooling gap that only a person, working outside this session, can close.

## What was done

Nothing was saved into `Raw/`; no Wiki article changed. `Outputs/attachments-to-download-from-gmail.md`
is unchanged and remains the working checklist: Groups B (Deeds of Adherence), C (accounts, fees,
Xero invoices), D (establishment pack) and E (transfers in) are all still outstanding, exactly as
listed there. A person still needs to open each thread link, download the named file, and drop it
into `Raw/` (Drive folder `1ntYVPRv8xacjjIYqrMi9EVBVv_0PUzuj`) unrenamed, per that file's own
instructions.

## Not done

- No file was written to `Raw/` under any name standing in for an attachment — inventing a
  placeholder would misrepresent an unfiled document as filed.
- `CLAUDE.md` was not replaced: nothing it claims turned out to be wrong, so there is nothing to
  retract or correct (section 6d rule 2 only applies to a claim that turns out to be wrong).

## Commit

`KB: re-verify that Gmail attachments still cannot be downloaded by this session's tooling; no
files saved, checklist unchanged`
