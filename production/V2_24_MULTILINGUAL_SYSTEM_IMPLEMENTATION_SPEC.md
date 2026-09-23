# V2.24 — MULTILINGUAL SYSTEM IMPLEMENTATION SPEC

Date: 2026-09-24

## Objective

Convert the workbook from partial localization to a coherent four-language interface without translating the internal calculation data model.

Languages:
- English
- Русский
- Italiano
- Español

## Current verified gap

The current Android deep-rebuild candidate contains 56 translation keys. These cover the main Dashboard, transaction, debt, savings, annual-review and month vocabulary, but not all static interface text.

Static interface text still requires authoritative keys on:
- Start Here
- Setup
- Bills
- Net Worth
- Accounts
- Spending Insights
- Lists
- Budget category display labels
- status values such as Yes/No and Paid/Unpaid

## Required translation key families

### Global
app_title, start_here, dashboard, budget, transactions, debt_tracker, savings_goals, annual_review, setup, bills, net_worth, accounts, spending_insights, cash_flow, translations, lists

### Start Here
choose_language, set_up, build_budget, record_activity, track_bills, track_debt, track_goals, review_position, review_dashboard, important, organization_tool_notice

### Setup
setting, value, notes, currency, default_language, month, privacy, year, local_workbook, preferred_currency_note, language_options_note, review_month_note, privacy_note, year_calculation_note

### Bills
bill, category, due_date, amount, frequency, paid, notes, yes, no, unpaid, paid_status

### Net Worth
asset_liability, type, starting_value, current_value, change, notes

### Accounts
account, type, current_balance, include_in_net_worth, notes, yes, no

### Spending Insights
category, current_month, share_of_expenses

### Cash Flow
period, income, expenses, net_cash_flow, notes

### Budget
category labels must be separated into:
1. stable internal calculation identifiers;
2. translated display labels.

This prevents translation from breaking SUMIFS criteria.

## Data-model rule

Do not translate internal calculation values such as Income, Expense, Savings, Debt or category IDs when they are used as formula criteria.

Instead:
- store stable internal values;
- display localized labels;
- use the translation layer only for presentation.

## Mobile UX rule

Every translated header must fit the intended mobile viewport.

Do not solve truncation by shrinking all text. Prefer:
1. sensible column widths;
2. short localized labels where the meaning remains clear;
3. wrapped header text only where needed;
4. reduced decorative whitespace;
5. consistent input-row heights.

## Status values

Yes/No and Paid/Unpaid must be reviewed carefully because they can be both:
- user-facing labels;
- formula criteria.

The implementation should preserve stable internal values and localize only their display representation where practical.

## Acceptance test

For Blank and Sample workbooks, run:

1. English interface scan.
2. Russian interface scan.
3. Italian interface scan.
4. Spanish interface scan.
5. Search for accidental remaining English interface strings.
6. Formula error scan.
7. Formula count regression.
8. Data-validation regression.
9. LibreOffice round-trip.
10. OOXML structure scan.
11. Mobile visual review.
12. Physical Android Excel test.
13. Final visual regression.

## Commercial requirement

The final package must contain a genuinely coherent multilingual interface, not a Dashboard-only language switch.

No intermediate workbook is released during this implementation.
