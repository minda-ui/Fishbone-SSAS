# Change log: group document policy v1.3 found in Raw, verified, flagged for a decision

**2026-09-10**, while checking `Raw/` at the owner's request.

## What was found

A third policy-notice file appeared in `Raw/`: `2026-09-10_group-policy_document-numbering-and-
filing-v1.3.md` (Drive id `1SC4sqboPMmyZ2iPDAljh5xKlKd_uEcxQ`, created 2026-09-10T14:31Z, 4,351
bytes). It states the policy moved from v1.2 to v1.3, adding two clarifications and withdrawing
nothing:

1. **Self-assigned property codes (§3/§7).** A property code is `<PREFIX>` + 4 digits (2-digit
   acquisition year + 2-digit sequence, e.g. `FM2301`). Each company self-assigns its own codes in
   its own property register; the group issues none centrally. Property-tied documents file under
   `<CODE> - <Address>/Documents/` in Collaboration Space.
2. **Email-attachment source capture (§5).** When a record is an email attachment whose bytes
   cannot be captured into Drive, register the row with the Gmail thread id as Source key and a
   plain-text transcription of the attachment as the stored record, flagged as a transcription;
   attach the real binary later if it becomes available, without changing the ID.

## What was checked

Per the standing rule (open question 12, reaffirmed at the v1.2 episode) that each new policy
version is verified and confirmed on its own, never adopted by extension of a prior one, this file
was independently checked against the group knowledge base before anything was done with it:

- The group KB's own live `CLAUDE.md` (Drive id `1_g2ZM4wiBXUGHipDw5j_Kbit3Dr86s4J`, created
  2026-09-10T14:28Z) records, in its own words: **"Revised 2026-09-10: the document policy went to
  v1.3 — resolving two more Change Requests (both Accepted): FM-CR-0001 (Commercial Properties)
  and FP-CR-0001 (Properties)"** — matching the Raw file's text and dates.
- The group KB's own live `README.md` (Drive id `1GkBDBhRFvRQNFQWYAb85GHWlkIAXRvEI`, created
  2026-09-10T14:23Z) independently corroborates the same two clarifications: "self-assigned
  property codes §3/§7, email-attachment source capture §5".
- The group KB's `current-state.md`, `CLAUDE.md`, `README.md` and `WORKFLOW.md` control files as
  they stood before this revision are all now archived, each titled "superseded by policy v1.3 /
  FM-CR-0001 + FP-CR-0001" — consistent with a genuine, tracked version bump rather than an
  injected one-off file.
- All of these files are owned by `minda@fishboneconstruction.co.uk`, the same account that owns
  this KB.

**Conclusion: genuine**, corroborated in the same way v1.2 was.

## Why this one is likely moot for this KB either way

Unlike v1.1 (new Smartsheet access, cross-KB writes) or even v1.2 (narrow but at least on-topic),
neither v1.3 clarification currently changes anything this KB would do:

- **Property codes**: this KB has no property of its own to code. The scheme's only asset is a
  loanback secured by a mortgage over a property the *borrower* owns, not the scheme; property
  codes belong to whichever company holds the property, not to this KB.
- **Email-attachment transcription**: this only helps a KB that can *see* an attachment's content
  but can't save its binary bytes to Drive. This KB's own tooling gap is a step earlier than
  that — the Gmail connector returns no content field at all for an attachment (filename, mimeType
  and an opaque id only), so there is nothing to transcribe even if this clarification is adopted.

## What was done

Registered in `Outputs/kb-registers.md`'s `Processed items` table as `skipped`, pending the
owner's decision, with the verification detail above. **Not adopted**: `CLAUDE.md` still
references v1.2 only. Raised for the owner's decision, noting that adoption would likely be a
paper change only given the above.

## What was not done

No document number was assigned to the notice file itself (it asks not to be, as before). The
file was not archived, since it has not been acted on.

## Commit

`KB: flag group document policy v1.3 found in Raw for owner decision`
