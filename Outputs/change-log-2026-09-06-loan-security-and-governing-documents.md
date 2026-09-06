# 2026-09-06 - Session 3 - Loanback security documents and the remaining governing documents processed; the OneDrive master briefly in Raw/

- Owner asked (a) to check `Raw/` on Google Drive, then (b) "check again and then process them",
  and mid-way (c) said the `SSAS` folder had been moved out of `Raw/` and asked where it now is.
  All three done. Processing followed section 3b: detect, register, read, extract, update, check,
  log, commit.

## What was found in `Raw/`, in order

| Time (UTC) | Event | Evidence |
|---|---|---|
| 21:13 | Folder `SSAS` uploaded into `Raw/`: the whole OneDrive `Documents/SSAS` master, 139 files in 10 folders, file dates preserved (2021 to April 2025) | Drive listing, `createdTime` |
| 21:15 | Three new files uploaded to `Raw/`: `Completion Statement.pdf`, `Legal Mortgage 29 April 2025.pdf`, `Receipted Invoice.pdf` | Drive listing |
| about 21:19 | Owner moved the `SSAS` folder out of `Raw/` to the My Drive root (folder id `1jSFpIOcKb7yANA0hJVtjWb_80rMfvo5c`, parent `0ABNRgppRuUv8Uk9PVA` = "My Drive") after the first check reported it as mostly member-personal | `get_file_metadata` on the folder |
| 21:21 | The four scheme-level documents copied from that folder into `Raw/` by file id, byte for byte | `copy_file` results |

The folder was in `Raw/` for about six minutes. It is recorded here and in the `Processed items`
table as one `skipped` item so section 3b's Detect step has a row for it if it ever reappears.

## The `SSAS` folder, as listed while it was in `Raw/`

| Folder | Files | Contents (classification) |
|---|---|---|
| root | 20 | `Admistration Agreement.pdf` (8,773,870 B), `Schemes rules.pdf` (4,324,101), `SASS price list.pdf` (1,155,128), `The Pension Regulator Certificate.pdf` (1,797,143): scheme-level, copied. `Trust deed.pdf`, `Board minutes.pdf`, `Document_2021-11-01_103325.pdf`: byte-identical to files already on file. `Pension letter.docx`, `Pension letter 1.docx`: identical draft letters from the director of Fishbone Properties Ltd to Nest Pension about a named employee's contributions to the SSAS (member-personal, read to classify, cited by URL only). `Aviva transfer Mr Mindaugas Gaudiesius.pdf`, `EP Minda.pdf`, `EP Andrej.pdf`, `Passport certificated copy.pdf`, `Credit score report.pdf`, six phone photographs of 14/10/2021: member-personal or unclassified, not opened |
| `Redeclaration/` | 2 | the two TPR re-declaration PDFs already on file (byte-identical) |
| `Certificates/` | 1 | the HMRC registration letter already on file (byte-identical) |
| `Metro Bank account/` | 8 | `Sign form.pdf` (8,767,821 B, May 2024, not downloadable at that size), `Details.docx` (trustees' personal details), two O2 bills, four photographs of February 2021: member-personal |
| `Minda/` | 10 | five payslips, three `Statement_n_2022.pdf` (read to classify: personal Lloyds current-account statements), copies of the rules and the HMRC letter |
| `Andrejus/` | 9 | `Andrejus client agreemnet.pdf` (read to classify: Empowered Pensions letter of 14/03/2023 confirming an Aviva transfer out in cash, no advice), `Andrejus Aviva transfer.pdf`, employment letter, three "Pension Contributions (Fishbone)" reports, `Scan0001.pdf`, copies of the rules and the HMRC letter |
| `2023/` | 22 | six monthly "Pension Contributions (Fishbone)" reports from Galaxy Payroll for Fishbone Drylining Limited, December 2022 to May 2023 (one read to classify: per-employee figures, pension labelled "Aviva Salary Sacrifice Pension"); `Statement_12_2022`, `_1_2023`, `_2_2023` (one read: personal Lloyds statement); employment letters; Aviva questionnaires; four `Minda document n.pdf` scans; `To Whom it may concern.docx` (read: confirms the managing director's employment since April 2016 and the sponsoring company; carries an NI number); a copy of the TPR certificate |
| `2023/Andrejus/` | 14 | three UUID-named PDFs (one read to classify: personal NatWest statement), payslips, contribution reports, Aviva questionnaire, `To whom it may concern.pdf`, copies of the TPR certificate, HMRC letter and rules |
| `Irina/` | 50 | `Additional Members SSAS Application Form - Irina.pdf` and `... filled.pdf` (read to classify: Empowered "Additional Member" form for the Fishbone SSAS, role "Member & Trustee", December 2023 and January 2024), ten `ViewPdfForm*.pdf` (one read: Fishbone Properties Ltd payslips), twelve weekly payslips, passport, driving licence and credit report copies, three bank statements, Nest and Aviva forms, `Forms 15 Beverley Place.pdf` (19 MB, not opened), `Nick forms.pdf`, `Nick form.doc`, `Pension letter.pdf`, `To Whom it may concern.pdf`, sign forms, photographs |
| `New folder/` | 3 | `Document_2023-01-20_154647.pdf` (read to classify: signed Empowered authority form for M Gaudiesius, personal identifiers), `Document_2023-01-20_154601.pdf`, one photograph |

Nine files were opened to classify their folders; none of the member-personal content is
repeated in the Wiki. Where a file carries a scheme-level fact (a third member's application,
the payroll pension label, the Nest letter, the Aviva transfer letter, the bank-mandate wording on
the administrator's form) the Wiki states the fact and cites the folder's Drive URL, marked
`(unverified: seen in the legacy folder, not filed here)`.

## Filed into `Raw/` (seven files, all Drive-only, not mirrored to git)

| Raw file | Origin | Bytes |
|---|---|---|
| `Completion Statement.pdf` | uploaded by the owner | 47,191 |
| `Legal Mortgage 29 April 2025.pdf` | uploaded by the owner | 1,611,487 |
| `Receipted Invoice.pdf` | uploaded by the owner | 58,358 |
| `Scheme Administration Agreement - Empowered Pensions (Admistration Agreement.pdf, copied from owner's OneDrive SSAS folder via Drive 2026-09-06).pdf` | `SSAS/Admistration Agreement.pdf` | 8,773,870 |
| `SSAS Scheme Rules - Empowered Pensions (Schemes rules.pdf, copied from owner's OneDrive SSAS folder via Drive 2026-09-06).pdf` | `SSAS/Schemes rules.pdf` | 4,324,101 |
| `Scheme Administration Agreement Schedule 1 fees 2018-04 (SASS price list.pdf, copied from owner's OneDrive SSAS folder via Drive 2026-09-06).pdf` | `SSAS/SASS price list.pdf` | 1,155,128 |
| `TPR scheme registration certificate 2022-08-04 PSR 12018880 (The Pension Regulator Certificate.pdf, copied from owner's OneDrive SSAS folder via Drive 2026-09-06).pdf` | `SSAS/The Pension Regulator Certificate.pdf` | 1,797,143 |

The three owner uploads keep their original names, per the Raw rule that files are never renamed.

## What could not be done, and why

- **The administration agreement was not read.** It is an 8.8 MB scan with no text layer. The
  Drive connector's download failed three times at that size ("session expired") and its text
  extraction returns nothing. Registered `partial`. A person, or a tool that can fetch a file of
  that size, is needed.
- **Clauses 6.11 to 29 of the Legal Mortgage** (PDF pages 14 to 39: covenants, enforcement,
  receivers, costs, notices) were not summarised; the parties, definitions, security, perfection,
  Schedule 1 and execution pages were. Registered `partial`. The plan referred to in Schedule 1
  is not in the scan.
- **Nothing from the `SSAS` folder beyond the four scheme documents was filed**, by the owner's
  earlier instruction to exclude personal data and by the owner's own action in moving the folder
  out.

## Read, extracted, and written into the Wiki

All scans read as page images (section 3d). Five articles created, nine updated, index rebuilt:

| Article | What it carries |
|---|---|
| `Wiki/Assets/loanback-fishbone-commercial-properties.md` (**new; first `Assets/` article**) | loan 41,500, costs 1,352.20, net 40,147.80; first legal mortgage over 145 High Street East NE28 7RL (part of TY59507) dated 29/04/2025, executed by all four trustees and the borrower; loan agreement dated 16/04/2025 not on file; Maximum Amount 50 percent of scheme value; HMRC loan-conditions table; registration of the charge not evidenced |
| `Wiki/People/i-fedonina.md` (**new**) | a third individual trustee, party to and signatory of the mortgage; appointment deed and membership basis not on file |
| `Wiki/Suppliers/dollman-pritchard.md` (**new**) | the trustees' solicitors; ref AJA/FIS53.1; invoice 33194 of 16/04/2025, 1,244.20, receipted; reconciliation to the completion statement |
| `Wiki/Finance/tpr-scheme-registration-2022.md` (**new**) | PSR 12018880; submitted 04/08/2022 by Empowered; commencement 28/10/2021; 2 members at 03/12/2021; trustees and employer as registered; company number 07948220 |
| `Wiki/Processes/scheme-rules.md` (**new**) | the administrator's SSAS rules, unsigned; trustees by deed, max eleven; corporate-trustee consent for lending; participating employers by deed; membership; winding-up |
| `Wiki/Suppliers/empowered-pensions.md` | 2018 fee schedule (establishment 750, annual 500 per member, loanback set-up 250, facility fee 500 or 250, additional member 150, levies); TPR contact; agreement on file but unread |
| `Wiki/People/empowered-trustees.md` | executed the mortgage via its director; TPR register entry; rule 6.3 |
| `Wiki/People/m-gaudiesius.md`, `Wiki/People/a-prutkovas.md` | signed the mortgage as trustee and as borrower's director; TPR register entries; payroll pension labelled Aviva; the 2023 Aviva transfer letter classified |
| `Wiki/Employers/fishbone-construction-ltd.md` | company number now 07948220 on three documents against 07948020 on one; "Principal and Participating Employer", trading from 14/02/2012; participating-employer question for Fishbone Properties Ltd sharpened by rule 12.1 |
| `Wiki/Finance/hmrc-registration.md`, `Wiki/Finance/tpr-re-declaration-2023.md`, `Wiki/Suppliers/metro-bank.md`, `Wiki/Processes/scheme-establishment-2021.md` | cross-links; commencement date; mandate wording; rules now on file |

## Findings a person should look at

1. **The loan agreement dated 16 April 2025 is the missing document.** The security is on file
   and fully executed; the rate, term and repayment schedule are still only the Loans wiki's
   figures. Dollman & Pritchard (ref AJA/FIS53.1) or Empowered Pensions Ltd should have it.
2. **There is a fourth trustee.** Irina Fedonina signed the mortgage as a trustee of the scheme.
   Nothing on file appoints her, admits her as a member, or admits her apparent employer,
   Fishbone Properties Ltd, as a participating employer, which the rules require by deed. The
   TPR registration of 2022 still shows two members and one employer.
3. **Charge registration is not evidenced.** Companies House and Land Registry fees were paid at
   completion; the MR01 against company 13687238 and the restriction on title TY59507 should be
   checked.
4. **The same two people signed for lender and borrower.** Allowed by the rules (6.6), with the
   corporate trustee's execution as the safeguard (6.3.1); worth a minute of the trustees'
   attention all the same, together with the valuation issue the FCP knowledge base flags.
5. **The company number question is now three to one** for 07948220; the November 2023
   re-declaration is the odd one out. Still confirm at Companies House.
6. **Payroll pension contributions in 2022 and 2023 went to Aviva**, on the label in the payroll
   reports. What the SSAS has received, and from whom, needs the Metro Bank statements.

## Knowledge base updated

- `CLAUDE.md` replaced by version 3 (archive-then-recreate): section 5's weekly-sync prerequisite
  marked met; section 6b notes that member-personal folders do not belong in `Raw/`; section 7
  refreshed for the loanback, the fourth trustee, the four documents now on file and the folder
  episode.
- `Wiki/index.md`, `Wiki/Processes/knowledge-base-operations.md`, `Outputs/kb-registers.md` and
  the nine updated articles replaced by archive-then-recreate on Drive; previous versions in
  `Archive/` with their reasons.
- No Smartsheet row and no `FSS` number (section 6a). The first `FSS 0001` row is ready to be
  keyed from the Assets article once the loan agreement fixes the terms.

## Recounts done this session

- Completion statement: 950 + 190 + 40 + 8 + 23 + 28.80 + 14 + 19.40 + 7 + 12 + 15 + 45 =
  1,352.20; 41,500 - 1,352.20 = 40,147.80. Agrees with the statement.
- Invoice: 950 + 96.20 + 198 = 1,244.20. Agrees. Difference to the statement 108.00 = 9.60 +
  19.40 + 7 + 12 + 15 + 45.
- Files in the `SSAS` folder: 20 + 2 + 1 + 8 + 10 + 9 + 22 + 14 + 50 + 3 = 139.

## Next step

1. Obtain the loan agreement of 16/04/2025; then complete the HMRC loan-conditions table, key
   `FSS 0001`, and decide `FSS0000001` onwards for the thirteen documents now in `Raw/`.
2. Ask Empowered Pensions Ltd for the deed appointing the third trustee, the deed of participation
   (if any) for Fishbone Properties Ltd, the executed trust deed and rules, the scheme year end,
   and the filing history (Pension Scheme Returns, Event Reports, TPR scheme returns).
3. Check the charge at Companies House and the restriction at the Land Registry.
4. Have a person read the administration agreement, or drop a smaller (split or compressed) copy
   into `Raw/`.
5. Metro Bank statements from opening to date.
