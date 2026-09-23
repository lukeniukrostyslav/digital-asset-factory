# A3 — PRODUCT ARCHITECTURE SPECIFICATION

Дата: 23.09.2026
Версия: 1.0

## 1. Product identity

Working name: Personal Money Command Center
Positioning: an all-in-one personal money organization, planning and tracking toolkit.
Primary language: English.
Primary launch market: United States.
Launch price: $9.99 USD.
Planned regular price: $12.99 USD.

This product is an organizational tool, not financial advice.

## 2. Customer job-to-be-done

The customer wants one ready-made system to:
- see income and spending in one place;
- plan a monthly budget;
- record transactions;
- track debts;
- track savings goals;
- review financial progress over time;
- use a printable version when desired;
- optionally use AI prompts to reflect on their own financial information.

The product must minimize setup friction and avoid requiring the customer to design a spreadsheet from scratch.

## 3. Final deliverable architecture

### 01 — Excel Dashboard
Main overview with:
- selected month;
- income;
- expenses;
- savings;
- debt overview;
- budget status;
- recent transactions;
- savings-goal progress;
- spending by category.

### 02 — Budget Planner
Monthly planning:
- income categories;
- fixed expenses;
- variable expenses;
- planned vs actual;
- category totals;
- monthly remaining amount.

### 03 — Transactions Tracker
Transaction log:
- date;
- description;
- category;
- account/payment method;
- income/expense type;
- amount;
- optional note.

### 04 — Debt Tracker
Debt organization:
- creditor/name;
- current balance;
- minimum payment;
- planned payment;
- due date;
- interest-rate field where the customer knows it;
- status/progress.

No claim that the tracker guarantees debt payoff.

### 05 — Savings Goals
Goal tracking:
- goal name;
- target amount;
- current amount;
- target date;
- remaining amount;
- progress percentage.

### 06 — Annual Review
Year-end/period review:
- income summary;
- spending summary;
- savings summary;
- debt snapshot;
- major spending categories;
- reflection prompts;
- next-period planning.

### 07 — Printable PDF
Printer-friendly worksheets for:
- monthly snapshot;
- budget;
- transactions;
- savings goals;
- debt tracking;
- monthly review;
- annual review.

PDF is a companion, not a replacement for the editable spreadsheet.

### 08 — AI Prompt Pack
Prompts for using the customer's own data to:
- summarize spending;
- identify recurring categories;
- review a budget;
- organize goals;
- prepare questions for a financial professional.

Prompts must include a reminder not to share unnecessary sensitive personal information and must not present AI output as professional financial advice.

### 09 — Quick Start Guide
A short onboarding document:
1. Download files.
2. Open the Excel workbook.
3. Read the instructions.
4. Enter categories/settings.
5. Add current income and expenses.
6. Set savings goals and debts if relevant.
7. Review the dashboard.
8. Use the printable pages or AI prompts as desired.

## 4. File package

Commercial package target:

Personal_Money_Command_Center_v1.0.zip

Inside:
- 01_Excel/Personal_Money_Command_Center.xlsx
- 02_Printable/Personal_Money_Command_Center_Printable.pdf
- 03_AI_Prompts/AI_Prompt_Pack.pdf
- 04_Guide/Quick_Start_Guide.pdf
- 05_License/License_and_Use.txt
- README.txt

Optional future folder:
- 06_Bonus/

## 5. Version strategy

- v1.0 — first commercial release.
- v1.1 — bug fixes / clarity improvements only.
- v1.2 — minor feature improvements.
- v2.0 — substantial architecture or feature changes.

Every public version receives its own GitHub checkpoint.

## 6. UX principles

The customer should be able to understand the product without a tutorial video.

Rules:
- clear labels;
- consistent terminology;
- visible input areas;
- protected/calculated areas where practical;
- no unnecessary complexity;
- no broken formulas;
- no placeholder text in release files;
- usable on desktop first, with mobile readability considered for PDF and preview materials.

## 7. Safety and trust

The product must:
- avoid financial-advice claims;
- avoid guaranteed savings/debt/investment outcomes;
- avoid collecting customer financial data;
- clearly distinguish user-entered information from calculations;
- avoid requiring bank credentials or API connections.

## 8. A3 acceptance criteria

A3 is considered architecturally complete when:
- deliverables are fixed;
- file/package structure is fixed;
- core fields are fixed;
- versioning rules are fixed;
- UX principles are fixed;
- safety boundaries are fixed;
- the architecture is saved in GitHub.

## 9. Next blocks

A4 — finalize/create production materials.
A5 — complete spreadsheet implementation.
A6 — complete printable PDF.
A7 — visual design.
A8 — packaging.
A9 — QA.
