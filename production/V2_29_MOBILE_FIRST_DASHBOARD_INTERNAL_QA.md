# V2.29 — MOBILE-FIRST DASHBOARD INTERNAL QA

Дата: 24.09.2026

## Цель

Продолжить работу после физического Android PASS V2.28 и исправить главный оставшийся UX-дефект: Dashboard был слишком широким/мелким для телефона.

## Реализовано в V2.29 internal candidate

Файл:
`Personal_Money_Command_Center_PREMIUM_V2_29_MOBILE_FIRST_INTERNAL.xlsx`

Dashboard переразложен в мобильную 2-колоночную структуру:

- A:H controlled surface;
- крупный title;
- subtitle;
- compact month/year/language controls;
- Financial Snapshot;
- 8 KPI cards, расположенных 2 колонки × 4 ряда;
- Monthly Review;
- Key Insight;
- controlled print area A1:H18;
- Letter + landscape + fit-to-width;
- freeze panes from A4;
- Android-safe language selector остаётся на H3 с backend mirror J2;
- новые локализованные строки добавлены в Translations.

## KPI

- Income
- Expenses
- Net Cash Flow
- Savings Rate
- Debt
- Savings
- Net Worth
- Budget Remaining

## Monthly Review

- Bills this month
- Unpaid bills
- Top spending category
- Total account balances

## Key Insight

Добавлена простая локализованная интерпретация денежного потока:
- positive;
- negative;
- balanced.

Это не финансовый совет, а отображение рассчитанного значения месяца.

## Internal QA

После LibreOffice round-trip:

- 15 sheets: PASS
- Formula count: 334
- Formula error literals: 0
- External links: 0
- Android language Data Validation: H3 -> Lists!$A$1:$A$4
- Backend language mirror: J2 = H3
- Cached sample metrics:
  - Income: 3000
  - Expenses: 2000
  - Net Cash Flow: 1000
  - Savings Rate: 33.33%
  - Debt: 1200
  - Savings: 500
  - Net Worth: 1800
  - Budget Remaining: 0
  - Bills this month: 900
  - Unpaid bills: 0
  - Top spending category: Housing
  - Total account balances: 2300
  - Key Insight: Positive cash flow this month.

## Compatibility hygiene

- VBA/macros: none
- External links: none
- OOXML extLst: removed after round-trip cleanup
- Charts/drawings/tables: not introduced
- Dashboard print area: A1:H18

## Not yet accepted

Physical Android visual acceptance of V2.29 is NOT claimed.

The next physical device gate is to inspect:
1. Dashboard scale;
2. 2-column card readability;
3. language dropdown;
4. Monthly Review;
5. Key Insight;
6. Budget and Transactions readability.

If physical Android visual acceptance passes, proceed to final print/Letter QA and release packaging.

## Release status

V2.29 is an internal candidate only. It is not the commercial release package.
