# 2026-09-07 - The signed loan agreement filed from Gmail and processed

- Owner asked "check /Raw" twice. The first check (before this entry) found nothing new. The
  second found one file created at 11:44 UTC: `Raw/FishboneSSAS_Loanback(£41.5k)_LA01801_2025-04-xx.pdf`, 430,685 bytes, Drive id
  `1NMpsFUMZqvQCitzG58s7PLQR3gNQpCcm`. It is item A1 of `Outputs/attachments-to-download-from-gmail.md`,
  the signed loan agreement attached to the Signable confirmation of 16/04/2025, unrenamed as the
  checklist asks. Registered `pending`, read, worked into the Wiki, marked `done` in
  `Outputs/kb-registers.md`.
- **How it was read.** Text extraction through the Drive connector (clean: a contract with no
  side-by-side tables) and, because the signature page's text comes out interleaved, the PDF was
  decoded from the connector's download into the session scratchpad and pages 1, 3, 14 and 15
  rendered as images. 16 pages: cover, contents, twelve pages of agreement and schedules, the
  signature page, and two pages of Signable audit trail.
- **What the agreement says** (all now cited in `Wiki/Assets/loanback-fishbone-commercial-properties.md`
  as [^12]): Empowered Pensions Limited template, reference LA01801, "made on 16 Apr 2025".
  Lender the three member trustees and Empowered Trustees Ltd as trustees of the scheme; borrower
  Fishbone Commercial Properties Ltd. Loan 41,500.00. Interest 5.50 percent per annum, stated
  flat, monthly in arrears from one month after drawdown; default rate 8.25 percent. Repayable
  within five years of drawdown (the day the money leaves the lender's account); first repayment
  within a month; each repayment equal to the balance divided by the repayment dates remaining,
  which is equal capital instalments; part and full early repayment on a month's notice, no
  penalty. Set-up fee 350.00 and transaction fee 45.00 paid by the borrower; legal fees on the
  borrower. Conditions precedent include a board minute of the borrower. Security: a full legal
  mortgage, described as a blanket charge, over 145 High Street East (TY59507); covenants to
  repair and insure; a cross-collateral clause. Ten events of default including a change of
  control. Signed through Signable by the four trustees on 10 and 11/04/2025 and by the two
  directors for the borrower on 10/04/2025; envelope completed by Empowered Lending on 16/04/2025
  with Dollman & Pritchard copied in.
- **What changed in the Wiki.**
  - Loanback article: the "not on file" framing struck; twelve key-facts rows added from the
    agreement; the Loans-wiki paragraph rewritten as a comparison (5.5 percent right but flat,
    not tracking; 60 months right; **790.13 a month is a level annuity, not what clause 7 says**:
    clause 7 gives 691.67 capital plus interest, 881.88 in month one, falling); the timeline
    rewritten around drawdown on or about 24/04/2025; the HMRC table's rate and term rows
    verified and the equal-instalments row opened; open questions updated. Recount: level
    payment on 41,500 at 5.5 percent over 60 months is 792.70, so the Loans wiki's 790.13 is
    that basis to within rounding or a day-count difference.
  - `Finance/hmrc-registration`: the "agreement not on file" sentence struck and corrected.
  - `People/empowered-trustees`: the corporate trustee's written agreement to the loan is now
    evidenced by its Signable signature of 11/04/2025.
  - `Suppliers/dollman-pritchard`: legal fees on the borrower per clause 8.2; the firm was copied
    in on completion of the agreement; its open question answered.
  - `Processes/knowledge-base-operations`: history line.
  - `CLAUDE.md` replaced by **version 5**: section 0's Gmail paragraph, section 5's loanback
    monitor prerequisite, section 7's heading, loanback bullet and open question 1, and the
    footer. All 20 headings preserved (checked before and after).
  - `Outputs/attachments-to-download-from-gmail.md`: item A1 ticked; standing file replaced.
- **Not quoted anywhere**: the members' home addresses on page 3 and the signers' IP addresses
  in the audit trail. The Raw file is Drive-only.
- **Open, for the owner.** The repayment schedule (checklist item A5) is now the most valuable
  single file: it decides whether the borrower's level 790.13 a month is what the parties agreed
  in practice, and therefore whether the HMRC equal-instalments condition is met as run. The
  heads of terms email's three files (A2 to A4), including the trustees' board minute and
  indemnity letter, come next.
- Read-only session otherwise: no email sent, no Smartsheet write.
