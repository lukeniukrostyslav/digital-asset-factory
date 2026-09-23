# V2.5 COMPETITOR BENCHMARK CHECKPOINT

Date: 24.09.2026

## Fresh benchmark findings

Current 2026 competitors were reviewed for concrete product requirements.

### Requirements confirmed
- FinancialAha: broad connected financial picture, dashboard, goals, debt, net worth and projections; one-time purchase positioning.
- Tiller: automation is the differentiator for bank-connected workflows; subscription required for that service.
- Analysistabs: sample-data and blank versions, period selector, dashboard, planned-vs-actual, print-ready output and explicit Excel compatibility.
- Finta: remaining budget, spending, income, savings rate, budget status, top categories and plan-vs-actual are prominent dashboard concepts.
- Sheets & Cells: 12-month planning, dashboard, savings projections, formula-only/no-macro positioning, print readiness.
- Sort & Keep: multi-file regional editions, debt/savings/net-worth coverage, example data, one-time purchase, explicit limitation that the spreadsheet is not professional financial/tax/investment advice.

## Product response
The Personal Money Command Center will preserve its core differentiator:
- manual-entry and privacy-oriented;
- no bank credentials or external account connection;
- connected workbook rather than isolated trackers;
- four-language UI;
- dashboard + budget + transactions + bills + debt + savings + accounts + net worth + cash flow + annual review;
- printable PDF and AI prompt pack;
- clear quick-start flow;
- no financial guarantees.

## New QA gates added
1. Verify a first-time user can understand the workflow from Start Here/Quick Start.
2. Verify Dashboard KPIs are internally consistent for month + year.
3. Verify sample/blank state behavior.
4. Verify print output at Letter width.
5. Verify formula-only behavior without macros/external links.
6. Verify multilingual terminology consistency.
7. Verify all claims and product copy avoid financial-advice promises.

A9 remains 0% until these tests are actually executed.

## Release policy
Intermediate files remain unreleased. Final ZIP only after all required production and QA gates pass.
