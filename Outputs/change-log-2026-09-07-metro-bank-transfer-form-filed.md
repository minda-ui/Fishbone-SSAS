# Change log: signed Metro Bank transfer form filed (checklist A10 closed)

**2026-09-07, a further check of `Raw/`** (section 0's Detect step), prompted by the owner asking
again to "check /Raw folder" after the Companies House MR01 entry earlier the same day. One new
file had appeared.

## What was found

`Emailing Metro SSAS 2404.pdf` (540,102 bytes, Drive id `1obXRb3r5JHFWcb6gkvL5UI5TV-kyU6_t`), 2
pages, read as page images (a bank form with figures, per section 3d). This is checklist item
A10: the signed Metro Bank "Outward Payment Instruction (Faster Payment & CHAPs)" that moved the
loan advance out of the scheme's account.

Page order in the PDF is reversed from the form's own numbering: PDF p.1 is the form's "pg 2"
(Section 6, Security Call Back, and the bank's internal-use box — both blank in this copy); PDF
p.2 is "pg 1", the completed page:

- Customer/Business Name **FISHBONE SSAS**; Debit Account Number present (not repeated: bank
  detail).
- Faster Payment, Payment Date **ASAP**, Amount **£41,500** ("forty one thousand five hundred
  pounds").
- New Beneficiary **Dollman & Pritchard Solicitors**, Business Account; sort code and account
  number present (not repeated: bank detail). Payment Reference **AJA/FIS53.1**, matching the
  solicitors' own matter reference already on file.
- Customer Signature: Primary Applicant **Mindaugas Gaudiesius**, dated **24.04.2025**. Secondary
  Applicant line blank.

## What this settles

- **Checklist item A10** is closed: the transfer form is now on file, not just an email
  description. The Drawdown date of 24/04/2025 (the day the money left the scheme's account,
  which starts the five-year term under the loan agreement) is now verified rather than resting
  on the administrator's email account of it.
- **Checklist item A11** (the blank password-protected form) is not needed: A10 read cleanly as
  page images, so there is nothing left for A11 to stand in for.

## New open question

The signed form carries only the Primary Applicant's signature. The account's 2024 mandate
requires one member trustee and one authorised administrator to sign together for any payment
over 1,500, but Metro Bank's own form has no administrator signature line at all — only Primary
and Secondary Applicant — and the Secondary Applicant line and the bank's internal-use box (ID&V,
T24 input, payment authorised) are all blank in this copy. Whether the administrator's part of
the mandate was satisfied some other way (Empowered Lending's own verification and release
process, as the email trail already describes) is not evidenced on the form itself. Not resolved
by guessing; left open in both `Wiki/Assets/loanback-fishbone-commercial-properties.md` and
`Wiki/Suppliers/metro-bank.md`.

## Articles updated

- `Wiki/Assets/loanback-fishbone-commercial-properties.md`: the Drawdown-date sentence in Details
  changed from `(email)` to verified with a new footnote [^24]; new open question on the single
  signature; Changes row added.
- `Wiki/Suppliers/metro-bank.md`: new Key facts row for the form itself; the "how the loan advance
  was paid" row's citation changed from `(email; form not on file)` to verified; new Details
  paragraph and open question on the single signature; Changes row added.
- `Outputs/attachments-to-download-from-gmail.md`: A10 ticked, A11 marked not needed, header note,
  Count table and closing note updated — Group A (the loanback) is now fully closed.

## Not done this session

- The single-signature question above was not put to the administrator or the bank; that is a
  human decision (section 6a of `CLAUDE.md`).
- Groups B to E of the download checklist (Deeds of Adherence, accounts, fees, the 2021
  establishment pack, transfer-in evidence) remain outstanding.

## Commit

`KB: process 1 raw item (signed Metro Bank transfer form for the loanback; Drawdown date verified;
checklist A10 closed, A11 not needed; single-signature question opened)`
