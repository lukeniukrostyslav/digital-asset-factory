# V2.8 MULTI-MONTH SYNTHETIC QA CHECKPOINT

Date: 24.09.2026

## Fresh market research
The current 2026 benchmark continues to emphasize dashboard summaries, period selection, savings rate, debt/net-worth coverage, sample/blank states, printability and mobile usability. A current comparison also notes that buyers test templates with multiple months of transactions and realistic assets/liabilities, making multi-month regression an important QA criterion. citeturn0search0

## Synthetic test executed
A controlled workbook copy was populated with January and February transactions:
- January income: $3,000
- January expenses: $1,250
- January net cash flow: $1,750
- January budget remaining: $350
- January savings rate: 58.33%
- February income: $4,000
- February expenses: $1,200
- February net cash flow: $2,800
- February budget remaining: $400
- February savings rate: 70%

LibreOffice recalculation confirmed the Dashboard changed correctly when Setup month changed from January to February. This verifies that selected-period logic is not accidentally using all-time transaction totals.

## Blank-state regression
Previously verified blank-state values remain:
- Budget Remaining = 0
- Savings Rate = 0

## QA remaining
- physical Android Excel interaction;
- exhaustive four-language visual/label audit;
- final desktop/mobile visual inspection;
- final PDF content/layout inspection;
- final ZIP integrity and release candidate test.

A9 advances to 35%. No final release yet.
