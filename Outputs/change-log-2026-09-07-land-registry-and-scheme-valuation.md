# Change log: Land Registry documents and the 2024-25 scheme valuation filed

**2026-09-07, a routine check of `Raw/`** (section 0's Detect step), prompted by the owner asking
to "check /Raw folder". Ten new files had appeared since the open-questions pass earlier the same
day (`Outputs/change-log-2026-09-07-outstanding-items-pass.md`): six substantive documents and
four exact-size duplicates of files already on file.

## What was found

**Three HM Land Registry documents for title TY59507** (checklist items A6 to A9's A7, A8, A9 in
`Outputs/attachments-to-download-from-gmail.md`, matching the filenames the checklist already
named from Dollman & Pritchard's email of 26/01/2026):

- `Official Copy of Register - EDOC REGISTRATION - TY59507.pdf` (87,598 bytes, Drive id
  `1jUrfqIVIYC0pxkPpsYLoI5fTTFgrws-i`)
- `Official Copy of Title Plan - EDOC REGISTRATION - TY59507.pdf` (214,182 bytes, Drive id
  `1iXJgmt01pQiuRDx6w7kz6AuqbEO09SAO`)
- `Registration Completion Sheet - EDOC REGISTRATION - TY59507.pdf` (39,407 bytes, Drive id
  `1aw3P_w9mkS7uqbk8fp_qzPxbhHzMtc6b`)

Read as page images (register 3 pages, plan 2 pages, completion letter 1 page). The register
shows the charge dated 29 April 2025 entered 18/07/2025 in favour of the four trustees, with a
restriction on further disposals without their consent; a note that the chargees are "under an
obligation to make further advances" (s.49(3) Land Registration Act 2002), not previously
identified from the mortgage deed's unsummarised clauses; the freehold history (Fishbone
Commercial Properties Ltd proprietor since 30/05/2023, price 140,000); that the title also covers
2 and 2A Ferndale Avenue (only 145 High Street East is charged); a 125-year lease of part of 2
Ferndale Avenue from 1996; and an 1905 building-scheme restrictive covenant, both pre-dating and
unconnected to the scheme. The completion letter confirms the official copy was issued to Dollman
& Pritchard 24/01/2026, two days ahead of the email that reported it — not a discrepancy.

**Three documents from the administrator dated 5 April 2025**, not on the Gmail attachments
checklist and most likely obtained from the administrator's client portal rather than email:

- `2025-04-05 Fishbone SSAS Scheme Valuation Prepared.pdf` (162,172 bytes, Drive id
  `18Vh0I_8DAuknzEh3oe89x5hbuk7zOb7t`) — a 9-page bundle: client information, portfolio valuation,
  revaluation movement, a full Metro Bank transaction list for the year, and member information
  (sensitive: dates of birth, National Insurance numbers, addresses, spouse names and individual
  fund values, not quoted into the Wiki)
- `2025-04-05 Fishbone SSAS Portfolio Valuation.pdf` (68,204 bytes, Drive id
  `1Ha-Ycxles61LGrrqMQyxGvliHMG7saQH`) — a standalone copy of the bundle's portfolio valuation page
- `2025-04-05 Fishbone SSAS Statement of Account.pdf` (76,013 bytes, Drive id
  `1bEvrou-98ZWwbQJJKNawqQuhYwA3NnBF`) — a Statement of Income and Expenditure and a Balance Sheet
  for the year to 5 April 2025, not duplicated elsewhere

These verify the scheme's net asset value at 5 April 2025 as **83,701.24** (a Metro Bank deposit
only; the loan, advanced 29/04/2025, shows at nil), and the year's income and expenditure:
contributions 245.00, bank interest 846.00, fees 1,660.00, other expenditure 1,791.00, net
decrease 2,360.00, opening net assets 86,062.00. The Metro Bank transaction list identifies the
1,791.00 "other expenditure" as paid on 02/12/2024 to Fishbone Drylining Ltd's HSBC account —
resolving open question 6 in `CLAUDE.md` section 7, which had only the reimbursement request, not
its payment.

**Four duplicate uploads**, byte-identical to files already registered `done`, carrying a `(1)`
suffix: `Receipted Invoice (1).pdf`, `Completion Statement (1).pdf`,
`Legal Mortgage 29 April 2025 (1).pdf`, `FishboneSSAS_Loanback(£41.5k)_LA01801_2025-04-xx (1).pdf`.
Registered `skipped`; no new content.

## What this settles

- **Open question 2 (the 50 percent test at April 2025)**: answered. 41,500 / 83,701.24 = 49.58
  percent, verified from the administrator's own valuation, not the quotation arithmetic used
  before. The scheme's Metro Bank transaction list shows no movement between 05/04/2025 and the
  loan's drawdown on 29/04/2025 beyond ordinary interest, so the value at completion (16/04/2025)
  was materially the same.
- **Open question 6 (the 1,791.00 reimbursement)**: answered. Paid 02/12/2024.
- **Part of open question 1 (Land Registry official copies)**: the three documents are now on
  file; only the Companies House registration certificate (checklist item A6) remains outstanding.
- **New open question**: the register's "obligation to make further advances" does not match
  anything identified so far in the loan agreement (a single drawdown, nothing redrawable) or the
  mortgage deed's summarised clauses; clauses 6.11-29 of the deed were not read this session either.

## Articles updated

- `Wiki/Assets/loanback-fishbone-commercial-properties.md`: Land Registry facts added, 50 percent
  test row in the HMRC table updated to verified, open questions updated, footnotes 17-22 added.
- `Wiki/Finance/scheme-accounts-and-returns.md`: year-to-05/04/2025 accounts added as verified key
  facts, status raised from `draft` to `active`, open questions updated.
- `Wiki/Employers/fishbone-construction-ltd.md`: the 1,791.00 reimbursement confirmed paid.
- `Wiki/Finance/transfers-in.md`: the 50 percent test figure updated from the quotation estimate
  (49.8 percent) to the verified 49.58 percent; reciprocal link to Scheme accounts and returns.
- `Wiki/index.md`: summary lines for the loanback, the employer and transfers-in refreshed.
- `Outputs/attachments-to-download-from-gmail.md`: A7 to A9 ticked; a note added that the three
  valuation documents arrived outside the checklist.
- `Outputs/kb-registers.md`: ten new `Processed items` rows (six `done`, four `skipped`).

## Not done this session

- The Companies House registration certificate (checklist item A6) is still only an email
  attachment.
- Clauses 6.11 to 29 of the Legal Mortgage were not read; the further-advances question may be
  answered there.
- No attempt was made to re-download the 8.8 MB administration agreement (open question 8): a
  person still needs to read it.

## Commit

`KB: process 10 raw items (Land Registry official copies for TY59507; scheme valuation, portfolio
valuation and statement of account as at 5 April 2025; four duplicate uploads skipped)`
