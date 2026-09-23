# V2.14 — COMPETITOR RESEARCH & PRODUCT GAP CHECKPOINT

Date: 24.09.2026

## Fresh competitor findings

### Tiller
Current Tiller materials describe a spreadsheet product with automatic daily bank transaction/balance feeds, budgets, spending insights, cash flow and net worth. Tiller's 2026 annual price is $99 after the trial. Its Excel workflow requires Microsoft 365/Excel Online and a Tiller subscription.

Sources:
- https://help.tiller.com/en/articles/3279649-what-is-tiller-and-how-does-it-work
- https://tiller.com/excel/
- https://community.tiller.com/t/update-to-tillers-annual-price-starting-in-august-2026/34853

Implication for our product:
- Do not try to compete on automated bank connectivity in v1.0.
- Keep the deliberate manual/private positioning clear.
- Emphasize one-time purchase, no bank credentials, no macros/external links, and portability.

### Analysistabs
The current Personal Budget Planner & Tracker is listed as a one-time purchase and currently shows $19 sale pricing. It includes Sample Data and Blank versions, a period selector, a live dashboard and planned-vs-actual tracking.

Source:
- https://analysistabs.org/product/personal-budget-planner-tracker/

Implication for our product:
- Sample + Blank must remain mandatory.
- Period selection, connected dashboard and planned-vs-actual are table-stakes features.
- Our package must continue to justify value through broader connected coverage: bills, accounts, debt, savings goals, net worth, annual review, printable pack and AI prompt pack.

### Finta
Finta's current free 2026 Google Sheets template includes remaining budget, spending, income, savings rate, budget status, top categories and a plan-vs-actual chart.

Source:
- https://www.finta.io/templates/google-sheets-budget-template

Implication for our product:
- Budget Remaining and Savings Rate are retained as explicit dashboard KPIs.
- Top spending category and connected cash-flow views remain useful differentiators.
- Do not claim superiority; use these findings only to define completeness and QA requirements.

## Product-positioning rule

The product should compete on a connected manual-entry workflow:
Start Here -> Setup -> Accounts -> Transactions -> Budget -> Bills -> Debt -> Savings -> Dashboard -> Spending Insights -> Cash Flow -> Net Worth -> Annual Review.

Core boundaries remain:
- no bank credentials;
- no bank/API connection required;
- no financial, tax, legal or investment advice;
- no guaranteed outcomes.

## QA consequence

The fresh benchmark reinforces five release requirements:
1. setup must be understandable without external help;
2. blank and sample workbooks must both work;
3. dashboard metrics must reconcile to source sheets;
4. mobile-safe formulas and language switching must not introduce errors;
5. the commercial package must remain usable without subscriptions or connected bank accounts.
