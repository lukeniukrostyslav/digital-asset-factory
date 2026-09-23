# COMPETITOR RESEARCH CHECKPOINT 03

Date: 24.09.2026

## Current market signals reviewed

Recent public market references show that personal-finance spreadsheet products increasingly compete on a connected system rather than a single budget table. Current examples emphasize combinations of transactions, budget, bills, savings goals, debt, net worth, cash flow, dashboards and low-friction setup. Some current products also emphasize mobile usability and minimizing the number of input tabs.

Relevant observations:
- Tools Without Code presents a 9-tab connected personal-finance system with only two input tabs and automatic recalculation.
- Tidy Ledgers' current Gumroad product combines dashboard, planned-vs-actual budget, transactions, bills, savings goals, debt and net worth in one workbook.
- FinancialAha's 2026 comparison explicitly evaluates setup ease, feature depth, visual design, customization, mobile usability and value, confirming these as useful QA dimensions for this category.
- Etsy search results show heavy competition and a wide price range, including low-price commodity templates and more complete bundles.
- Current consumer budgeting coverage also increasingly treats account aggregation, spending categorization, bills and goals as one workflow.

## Product response

The Personal Money Command Center should therefore be evaluated as a connected operating system for personal-finance organization, not as a simple budget spreadsheet.

The current v1.7 production pass improves that connection by:
- fixing transaction summary formulas so income/expense totals use the Amount column correctly;
- connecting Dashboard debt and savings KPIs to their source sheets;
- replacing the previous Dashboard net-worth shortcut with an asset-minus-liability calculation;
- connecting Bills KPIs to the selected month/year;
- connecting Cash Flow monthly income/expense rows to Transactions by date and type;
- adding a user-editable Year control to Setup;
- preserving the multilingual architecture and mobile-safe formula approach;
- retaining the zero-budget/no-bank-credentials positioning.

## QA implication

These improvements are production work, not final acceptance. A9 remains separate and must test formulas, blank states, edge cases, language switching, Excel/LibreOffice opening, and Android Excel behavior before publication.

## Competitive boundary

The product deliberately does not copy competitor wording, branding, artwork or proprietary implementation. The research is used only to identify category expectations and measurable UX requirements.
