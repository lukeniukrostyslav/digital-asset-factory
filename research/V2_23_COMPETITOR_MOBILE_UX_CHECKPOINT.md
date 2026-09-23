# V2.23 — COMPETITOR + MOBILE UX RESEARCH CHECKPOINT

Date: 2026-09-24

## Purpose

This checkpoint converts current competitor evidence and the real Android screenshots into concrete product requirements. It does not claim final Android compatibility.

## Current competitor observations

### Analysistabs Personal Budget Planner & Tracker

The current product positions a connected workbook around:
- 12-month planning
- transaction logging
- period selector
- live dashboard
- six KPI cards
- planned-vs-actual views
- category analysis
- sample and blank workbooks
- no macros and no external links
- one-time purchase positioning

Source:
https://analysistabs.org/product/personal-budget-planner-tracker/

### Analysistabs Income & Expense

The current product also emphasizes:
- connected tabs
- dashboard
- reports by person/category
- planned vs actual
- budget
- transactions
- settings for currency/language/preferences

Source:
https://analysistabs.org/product/income-expense-excel-template-family-budgeting/

### FinancialAha

Current product pages emphasize:
- dashboard-first presentation
- savings rate
- target vs actual
- category breakdown
- 12-month history in some products
- editable allocation assumptions
- cross-sheet connected calculations

Source:
https://www.financialaha.com/ultimate-spreadsheet-templates/personal-budgeting/50-30-20-budget/

## Product requirements derived from research

1. Dashboard must communicate the current financial snapshot immediately.
2. KPI hierarchy must remain visually strong on mobile.
3. Working sheets must look like parts of the same product, not generic raw Excel tables.
4. Inputs, calculated cells and reference values must be visually distinguishable.
5. Blank and sample versions remain important commercial deliverables.
6. Multilingual support must be systematic rather than partial.
7. Mobile compatibility is a release gate, not a marketing claim.
8. No bank credentials, macros or external workbook dependencies for core calculations.
9. Competitor features are requirements to benchmark against, not text/design to copy.

## Android compatibility constraints

Microsoft currently lists .xlsx as supported for opening/editing on Android and lists Data Validation viewing as supported. Microsoft also documents that mobile feature support differs from desktop Excel.

Sources:
https://support.microsoft.com/en-us/excel/why-can-t-i-open-my-excel-file
https://support.microsoft.com/en-us/excel/what-s-new-in-excel-on-mobile-platforms

Because this project has produced an actual Android repair prompt in testing, compatibility must be established empirically for the generated workbook. Desktop/LibreOffice success alone is insufficient.

## V2.23 remediation plan

### A. Multilingual system
Audit every user-facing string across all 15 sheets:
- English
- Russian
- Italian
- Spanish

Create one authoritative translation map and ensure every displayed interface string has a language-aware source.

### B. Mobile visual system
Rework:
- column widths
- header truncation
- input/calculated distinction
- repeated Yes/No presentation
- excessive empty rows/columns where they harm navigation
- sheet-specific visual hierarchy

### C. Dashboard
Preserve the connected KPI architecture while keeping the Android-safe compatibility core as the technical baseline.

### D. Compatibility layering
Reintroduce visual/UX features one at a time only after the Android core is accepted. After each layer:
- ZIP/XML inspection
- openpyxl validation
- formula count/error scan
- LibreOffice round-trip
- rendered visual review
- regression against blank/sample expectations

## Release rule

No intermediate workbook will be delivered. The next user-facing workbook is the final commercial candidate only after the full gate is passed.

## Status

This checkpoint is research and implementation planning. It does not close A7 or A9 by itself.
