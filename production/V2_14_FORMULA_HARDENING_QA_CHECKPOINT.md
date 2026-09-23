# V2.14 — FORMULA HARDENING & RELEASE-CANDIDATE QA CHECKPOINT

Date: 24.09.2026

## Fresh QA finding

A new LibreOffice round-trip on the release-candidate workbooks exposed three formula defects in the Cash Flow sheet:

- November income cell B12 was incorrectly linked to Setup!B4 (month text).
- December income cell B13 was incorrectly linked to Setup!B6 (year number).
- Bills this month / Unpaid bills used incomplete SUMPRODUCT formulas that produced #VALUE! during recalculation.

These defects were not accepted as release-ready.

## Repairs applied

Both Blank and Sample workbooks were repaired:

- B12 -> November SUMIFS income calculation.
- B13 -> December SUMIFS income calculation.
- L16 -> SUMIFS bill amount for the selected month.
- L17 -> COUNTIFS unpaid bills for the selected month.
- Sample Bills row was aligned with the actual headers:
  - C = Due Date
  - D = Amount
  - E = Frequency
  - F = Paid?
  - G = Notes

## Verification

After repair:

- LibreOffice round-trip completed for both workbooks.
- Cached formula error scan: 0 errors in Blank.
- Cached formula error scan: 0 errors in Sample.
- Formula parenthesis-balance scan: 0 unbalanced formulas.
- External links: 0.
- VBA/macros: absent.
- Defined names: 0.
- Data validations: 3 per workbook.
- Sample dashboard remained:
  - Income 3000
  - Expenses 2000
  - Net Cash Flow 1000
  - Debt Balance 1200
  - Savings Goals Funded 500
  - Net Worth 1800
  - Savings Rate 33.33%
- Sample Cash Flow Bills this month: 900.
- Blank-state dashboard remained zeroed without formula errors.

## Candidate checksums

Blank workbook:
e6cc8aee3f89a9b7c1029574cdded7717a56a3228eec1d997046a72bcf8d0c02

Sample workbook:
589aba92210ded1d7f9debda3994bb27d091ae531dfc88a88a0a489fb3dab7cd

Candidate ZIP snapshot:
840ac82e59e7b7f065697feececba06a3765c9d633e770dec29f426741c52312

## Remaining release gate

Physical Android Excel interaction remains unverified in the current execution environment. It is not marked complete by inference.

No intermediate commercial file is released to the user.
