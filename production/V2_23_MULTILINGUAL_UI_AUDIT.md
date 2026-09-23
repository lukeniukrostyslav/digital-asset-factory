# V2.23 — MULTILINGUAL UI AUDIT

Date: 2026-09-24

This audit was run against the current Android deep-rebuild candidate before any next workbook is released.

## Finding

The workbook contains a Translation sheet and several formula-driven localized sheets, but localization is not yet universal.

### Sheets already using language-aware formulas
- Dashboard
- Debt Tracker
- Savings Goals
- Annual Review
- Cash Flow

### Sheets still containing substantial static user-facing English
- Start Here
- Setup
- Bills
- Net Worth
- Accounts
- Spending Insights
- parts of Lists
- Budget category seed values

### Transactions

Transactions currently has no user-facing text cells in the inspected populated range; its interface therefore requires a separate structural review of headers/data-validation labels rather than a simple string replacement.

## Technical implication

Changing only the Dashboard selector cannot be treated as a complete multilingual system. A language selector must drive every user-facing label that is intended to be localized.

## Required implementation

1. Make the Translations sheet the single source of truth.
2. Add keys for all static labels and instructional strings.
3. Replace static interface labels on all user-facing sheets with language-aware formulas where Android compatibility permits.
4. Keep user-entered data and financial category values separate from interface translations.
5. Do not translate formula criteria such as transaction Type values unless the underlying data model is also redesigned; calculations should continue to use stable internal values.
6. Keep month display labels language-aware while retaining stable month logic internally.
7. Audit Yes/No, Paid/Unpaid and other status values separately.
8. Test all four languages from the same blank and sample workbook.

## UX remediation

The Android screenshots also show:
- first-column/header truncation on Accounts;
- excessive blank vertical area on several input sheets;
- inconsistent visual hierarchy between Dashboard and input sheets;
- static English labels remaining beside localized content.

These are release-blocking UX issues for the stated multilingual/mobile goal.

## Acceptance criteria

For each of the four languages:
- every visible interface label is translated or intentionally language-neutral;
- no accidental English remains in the interface;
- no formulas break;
- no data-model criteria are accidentally translated;
- headers fit the intended mobile viewport;
- blank and sample workbooks both pass;
- Android repair prompt is absent on the tested candidate.

This audit does not claim Android compatibility. It defines the work required before A7/A9 can be closed.
