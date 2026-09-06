# 2026-09-06 - Session 2 - OneDrive SSAS folder found; six legacy scheme documents copied and processed

- Owner asked (a) to check the folder `SSAS` on OneDrive, then (b) to copy its files, except
  those with personal data, into the Fishbone SSAS folder on Google Drive and process them per
  this knowledge base's rules. Both done, with one limit recorded under "What could not be done".

## What was found

- **The master of the scheme's papers is on OneDrive, not Google Drive.** Folder `Documents/SSAS`
  on the OneDrive of `info@fishbonedrylining.onmicrosoft.com`, created October 2021, last activity
  April 2025, about 105 MB in nine sub-folders (`2023`, `Andrejus`, `Certificates`, `Irina`,
  `Metro Bank account`, `Minda`, `New folder`, `Redeclaration`, `2023/Andrejus`). The Google Drive
  folder `Collaboration Space / Other / Staff (SSAS)` that `CLAUDE.md` version 1 pointed at is a
  partial copy made on 2024-11-25 by `anastasia@fishboneconstruction.co.uk`. Ids and the finding
  are recorded in `Wiki/Processes/knowledge-base-operations.md`.
- Documents present only on OneDrive, not in the Drive copy: `Admistration Agreement.pdf`,
  `SASS price list.pdf`, `Schemes rules.pdf` (three copies), `The Pension Regulator Certificate.pdf`
  (three copies), `Aviva transfer Mr Mindaugas Gaudiesius.pdf`, `Pension letter.docx`,
  `Pension letter 1.docx`, `Passport certificated copy.pdf`, and everything added to `Irina/`
  after November 2024.

## What could not be done, and why

- **No file could be copied from OneDrive itself.** The egress proxy refuses the SharePoint host
  (HTTP 403 on CONNECT) and the Microsoft 365 connector returns extracted text only, which for
  these scanned PDFs is empty. So the six documents below were copied **from the Google Drive
  partial copy** with Drive's own copy operation, byte for byte (sizes verified equal). The four
  scheme-level documents that exist only on OneDrive, the administration agreement, the price
  list, the scheme rules and the TPR certificate, **are still not on file** and need a person to
  drag them from OneDrive into `Raw/`.

## Copied into `Raw/` (six files, all Drive-only, not mirrored to git)

| Raw file | Origin | Bytes |
|---|---|---|
| `Trust deed (Fishbone SSAS, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | `Staff (SSAS)/Trust deed.pdf` | 377,344 |
| `Board minutes (Fishbone Drylining Ltd resolution to establish the scheme, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | `Staff (SSAS)/Board minutes.pdf` | 237,322 |
| `HMRC notification of registration 2021-12-06 (Certificates - Fishbone SSAS.pdf, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | `Staff (SSAS)/Certificates/Fishbone SSAS.pdf` | 704,718 |
| `TPR re-declaration summary 2023-11-07 (Redeclaration - 8. Summary and check, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | `Staff (SSAS)/Redeclaration/8. Summary & check ... .pdf` | 128,236 |
| `TPR re-declaration summary 2023-11-07 copy 2 (Redeclaration - 8. Summary and check 2, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | `Staff (SSAS)/Redeclaration/8. Summary & check ... 2.pdf` | 133,879 |
| `Metro Bank pension scheme account opening - signature page 2021-10-31 (Document_2021-11-01_103325.pdf, copied from Drive Staff (SSAS) legacy folder 2026-09-06).pdf` | `Staff (SSAS)/Document_2021-11-01_103325.pdf` | 197,748 |

Origin names were kept inside the new titles so the copies can be matched back to both legacy
folders by name.

## Deliberately not copied (personal data, or duplicates)

- **Personal identity and pay documents**, all member folders: passports, driving licences,
  credit score reports (the one at the root is password-protected and could not be opened, and
  the same file sits in `Irina/`), payslips, "Pension Contributions (Fishbone)" schedules
  (per-member amounts), employment letters, bank and pension statements, Aviva transfer and
  questionnaire forms, SSAS application forms, "To whom it may concern" letters, `Details.docx`
  and the O2 bills used as proof of address, unlabelled photographs and scans.
- **`EP Minda.pdf`, `EP Andrej.pdf`** (root) and the two `New folder/Document_2023-01-20_*.pdf`:
  read to classify; they are Empowered Pensions "Authority Form - Information Only Request" forms
  for each member trustee (blank and signed 20/01/2023 versions) carrying dates of birth and
  National Insurance numbers. Excluded; referred to by name only in the People articles.
- **`Minda/Fishbone SSAS.pdf`, `Andrejus/Fishbone SSAS.pdf`, `2023/Andrejus/Fishbone SSAS.pdf`**
  (708,681 bytes each): the first page was rendered and is the same HMRC registration letter as
  the `Certificates/` copy (704,718 bytes), a second scan. Not copied; the `Certificates/` copy is
  the one on file.
- The three GUID-named PDFs in `2023/Andrejus/`: unread, in a member folder, treated as member
  documents.

## Read, extracted, and written into the Wiki

Every document was read as rendered page images (section 3d); the TPR forms also have a text
layer, which was diffed to compare the two copies. Nine articles created, one category created:

| Article | What it carries |
|---|---|
| `Wiki/Processes/scheme-establishment-2021.md` | resolution, deed, bank request 31/10/2021, HMRC registration 03/12/2021; both governing copies unsigned and undated; rules not attached |
| `Wiki/Employers/fishbone-construction-ltd.md` (**new category `Employers/`**) | principal employer; company number 07948220 on the deed against 07948020 on the TPR form; PAYE 475/JA99759; EPSR 12018880 |
| `Wiki/People/m-gaudiesius.md` | member trustee; no identifiers repeated |
| `Wiki/People/a-prutkovas.md` | member trustee; no identifiers repeated |
| `Wiki/People/empowered-trustees.md` | corporate trustee, registration 12291059 |
| `Wiki/Suppliers/empowered-pensions.md` | scheme administrator; two addresses as written by HMRC and TPR; agreement and price list not on file |
| `Wiki/Suppliers/metro-bank.md` | account opening request signed 31/10/2021; nothing else on file |
| `Wiki/Finance/hmrc-registration.md` | PSTR 20005255RF; registered 03/12/2021; obligations from the letter |
| `Wiki/Finance/tpr-re-declaration-2023.md` | re-enrolment date 07/11/2023; two draft copies, submission not evidenced |

Why `Employers/` was created: a SSAS has sponsoring and participating employers as a first-class
concept, and the principal employer is neither a person, a supplier nor an asset. Created with
its first article, per `CLAUDE.md` section 1; added to `index.md` and to the template's category
list.

## Findings a person should look at

1. **Two company numbers.** The trust deed and board minutes say 07948220; the TPR re-declaration
   says 07948020. One is a typing error, most likely on the TPR form; confirm at Companies House.
2. **The governing documents on file are unsigned, undated copies.** The executed deed and the
   rules should be with Empowered Pensions Ltd.
3. **The next automatic enrolment re-enrolment date is November 2026**, three years after
   07/11/2023, and no submission receipt for the 2023 re-declaration is on file.
4. **The HMRC letter's obligations** (Event Reports, authorised employer loan conditions) have not
   been checked against the loanback to Fishbone Commercial Properties Ltd, whose agreement is
   still not on file anywhere found.

## Knowledge base updated

- `CLAUDE.md` replaced by version 2 (archive-then-recreate): `Employers/` in the folder tree and
  category list; section 6b notes the Raw PDFs are Drive-only; section 7 rebuilt, separating what
  is now verified from a filed document from what is still a pointer; the OneDrive source
  recorded.
- `Wiki/index.md`, `Wiki/_templates/article.md`, `Wiki/Processes/knowledge-base-operations.md`
  and `Outputs/kb-registers.md` replaced by archive-then-recreate; the previous versions are in
  `Archive/` with their reasons.
- No Smartsheet row and no `FSS` number: section 6a forbids writing to the sheets without an
  explicit decision, and the instruction covered Drive and the Wiki.

## Next step

1. Drag `Admistration Agreement.pdf`, `SASS price list.pdf`, `Schemes rules.pdf` and
   `The Pension Regulator Certificate.pdf` from OneDrive `Documents/SSAS` into Drive `Raw/`; the
   next session processes them.
2. Decide whether the six documents should take `FSS0000001` to `FSS0000006` in the Document
   Register, and whether the scheme's known holdings (the loanback, the Metro account) should take
   `FSS 0001` and `FSS 0002` in the Asset Register.
3. Ask Empowered Pensions Ltd for the executed deed, the rules, the loanback agreement and the
   filing history (Pension Scheme Returns, Event Reports).
