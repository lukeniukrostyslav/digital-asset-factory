# A4 / A5 / A7 PRODUCTION CHECKPOINT — V1.8

Date: 24.09.2026

## Production candidate
Personal_Money_Command_Center_v1.8_CONNECTED_SYSTEM.xlsx

## Completed improvements

### Dashboard
- Review month is now explicit.
- Debt balance, savings funded, and net worth are clearly separated KPIs.
- Dashboard remains connected to source modules.

### Budget
- Actual spending is calculated from Transactions for the selected month/year.
- Planned values remain user inputs.
- Difference remains Planned minus Actual.

### Spending Insights
- Category totals now use the selected review month/year instead of all historical transactions.
- Share of expenses is calculated from the selected-month category totals.

### Annual Review
- Monthly income is derived from Transactions.
- Monthly expenses are derived from Transactions.
- Monthly net savings is calculated as income minus expenses.
- Debt-paid amount is derived from the Debt Payments transaction category.

### Compatibility
- Month matching moved to the hidden Lists sheet instead of relying on inline array constants that produced cross-engine calculation errors.
- Bills dashboard formulas now use the same month list.
- Workbook calculation-on-open behavior retained.

## Verification

A synthetic QA dataset containing January and February transactions, debt, savings, net worth and bills was recalculated with LibreOffice.

Verified expected values:
- Total income: 6200
- Total expenses: 1700
- Net cash flow: 4500
- Debt balance: 1200
- Savings funded: 400
- Net worth: 3200
- January housing actual: 1000
- January food actual: 500
- January debt-payment actual: 200
- January bill total: 100
- January unpaid bill count: 1
- Annual Review January income: 3000
- Annual Review January expenses: 1700
- Annual Review January net savings: 1300
- Annual Review January debt paid: 200

## Remaining

A9 full QA is still not complete. Device-level Android Excel testing, all-language review, blank-state testing, final PDF generation, final AI prompt pack, guide, license, packaging and publication remain before final delivery.

Intermediate files are intentionally not released to the user.
