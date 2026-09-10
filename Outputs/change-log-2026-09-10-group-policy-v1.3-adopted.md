# Change log: group document policy v1.3 adopted

**2026-09-10**, following `Outputs/change-log-2026-09-10-group-policy-v1.3-flagged.md`, in which a
third group document-numbering & filing policy notice (v1.3) was found in `Raw/`, independently
verified against the group knowledge base, and raised with the owner for a decision. **The owner
replied: "adopt v1.3."**

## What changed

`CLAUDE.md` replaced by version 18:

- Section 1's register conventions now reference document-numbering & filing policy **v1.3**
  rather than v1.2, and record its two clarifications:
  1. Self-assigned 4-digit property codes (2-digit acquisition year + 2-digit sequence), each
     company keeping its own property register; no central index.
  2. Email-attachment source capture: when an attachment's bytes cannot be captured into Drive,
     register the row with the Gmail thread id as Source key and a flagged plain-text
     transcription as the stored record.
- Section 6a's introductory line now cites all three adoption change-log entries (v1.1, v1.2 and
  this one); the two exceptions themselves (Smartsheet append, `§7a` inter-KB hand-off) are
  unchanged, since neither v1.3 clarification touches them.
- Open question 12 gained a further closing note recording the v1.3 episode.
- The version banner and footer history line updated to record version 18.

## What did not change

As flagged, neither clarification changes this KB's actual behaviour:

- This KB owns no property of its own (the loanback is secured over a property the *borrower*
  owns, not the scheme) — there is nothing for it to self-assign a code to.
- This KB's Gmail tooling gap is a step earlier than what the transcription rule assumes: the
  Gmail connector returns no content field at all for an attachment (filename, mimeType and an
  opaque id only), so there is nothing to transcribe even under the new rule.

No Wiki article changed. No Smartsheet write was made.

## Verification already on record

The independent verification that established this file was genuine — cross-checking the group
knowledge base's own live `CLAUDE.md` and `README.md`, both corroborating FM-CR-0001 (Commercial
Properties) and FP-CR-0001 (Properties), both Accepted 2026-09-10 — was done in the prior entry
(`Outputs/change-log-2026-09-10-group-policy-v1.3-flagged.md`) and is not repeated here.

## Commit

`KB: adopt group document policy v1.3 per owner instruction`
