# Change log: loanback documents filed into the group Collaboration Space

**2026-09-09, at the owner's request** ("create the Fishbone SSAS folder in Collaboration Space"),
following on from the same-session registration of the loanback's 13 documents
(`Outputs/change-log-2026-09-09-loanback-documents-registered.md`), which had flagged Collaboration
Space filing as pending because no "Fishbone SSAS" company folder existed there.

## What was found before acting

Checked the new folder's permissions before copying anything sensitive into it. The Collaboration
Space root (`1YNj5BIpKVzcmI4U1DRkgu7kcnSDizGEi`) — and, once created, the new "Fishbone SSAS"
folder under it — inherits a **domain-wide writer share** to `fishboneconstruction.co.uk`, plus
several named individual accounts: `andrej@fishboneconstruction.co.uk`,
`lana@fishboneconstruction.co.uk`, `irina@fishboneproperties.co.uk`, and two external accounts,
`alexey.glukhov@aggaservices.co.uk` and `agga.services@gmail.com`, plus a personal address,
`sveta_usurt@yahoo.com`. This is far wider than this KB's own Drive tree, which was owner-only at
creation (`CLAUDE.md` section 6b). Several of the loanback documents carry bank account numbers,
signatures, AML identity-verification detail and trustees' home addresses — flagged directly to
the owner rather than assumed, since section 6a asks that an ambiguous or sensitivity-relevant
finding not be resolved by guessing. **The owner confirmed: copy all 13 in as-is, accepting the
wider access.**

## What was done

1. Created folder `Fishbone SSAS` in the group's Collaboration Space
   (`1YNj5BIpKVzcmI4U1DRkgu7kcnSDizGEi/Fishbone SSAS`, id `1ffkF6NaorrL9hR-ilusBNfgfyYlY_sFe`),
   alongside the five sister companies' own folders there.
2. Created a subfolder `Loanback - Fishbone Commercial Properties Ltd`
   (id `1zLFSHjXTB2rCfkTAwP15BN1ZaCD0_W3k`) to co-locate the loanback's own documents, matching the
   nesting pattern the group's own Construction folder uses for a single matter.
3. **Copied** (not moved) all 13 registered documents into that subfolder, renamed to the group
   policy's `<ID> - <Category> - <Short Title>.<ext>` convention, verified by matching byte size
   against the `Raw/` original in every case:

   | No. | New filename |
   |---|---|
   | FS0000001 | Loan - Loanback Application.pdf |
   | FS0000002 | Board minute - Board Minute and Indemnity Letter.pdf |
   | FS0000003 | Loan - Heads of Terms EP-LB-60.pdf |
   | FS0000004 | Loan - Loan Agreement LA01801.pdf |
   | FS0000005 | Invoice - Dollman and Pritchard Invoice 33194.pdf |
   | FS0000006 | Legal - Completion Statement.pdf |
   | FS0000007 | Mortgage - Legal Mortgage 145 High Street East.pdf |
   | FS0000008 | Loan - Repayment Schedule K0555.pdf |
   | FS0000009 | Certificate - Companies House MR01 and Certified Deed.pdf |
   | FS0000010 | Title register - HM Land Registry Official Copy of Register TY59507.pdf |
   | FS0000011 | Title plan - HM Land Registry Official Copy of Title Plan TY59507.pdf |
   | FS0000012 | Legal - HM Land Registry Registration Completion Sheet TY59507.pdf |
   | FS0000013 | Bank - Metro Bank Transfer Form.pdf |

4. Updated all 13 rows in the group Document Register (sheet `7352854736144260`): `File link` now
   points to the Collaboration Space copy; `Location` now names the Collaboration Space path.
   `Source key` was left unchanged (the original `Raw/` file's Drive id), since that is what this
   KB's own Wiki footnotes already cite, and the dedup-on-entry rule keys off it.
5. **Copied rather than moved**, deliberately departing from the group policy's own "move (never
   copy) to preserve the file id" instruction: this KB's `CLAUDE.md` section 1 says a `Raw/` file
   "is never edited, renamed or deleted", and moving it out would contradict that. The original
   files stay exactly where they are in `Raw/`; the Collaboration Space copies are new, separate
   Drive files with their own ids, referenced only from the register's `File link`/`Location`, not
   from any Wiki citation (footnote 28 in the loanback article cites the register itself, not an
   individual file).

## Wiki updated

`Wiki/Assets/loanback-fishbone-commercial-properties.md`: the document-register paragraph now
records that Collaboration Space filing is done, not pending, with the new folder path; `updated`
bumped.

## Not done

- No document was moved out of `Raw/`; the originals are untouched there, per this KB's own
  section 1 rule.
- No further Smartsheet write beyond the 13 rows' `File link`/`Location` cells — no other entity's
  row was touched.

## Commit

`KB: file the loanback's 13 documents into the new Fishbone SSAS folder in Collaboration Space;
copied rather than moved to respect Raw/ immutability; sensitivity of wider Collaboration Space
access flagged and confirmed by the owner before copying; CLAUDE.md version 15`
