# V1.9 FORMULA HARDENING CHECKPOINT

Date: 24.09.2026

## Purpose
A focused compatibility hardening pass was performed after inspecting the v1.8 workbook formulas.

## Issues found and fixed
- Removed remaining inline month-array constants from Dashboard helper formulas, Cash Flow helper formulas and Budget actual formulas.
- Fixed Budget Shopping actual formula to reference the category cell A11 rather than the planned-value cell B11.
- Recalculation was tested with LibreOffice.

## QA fixture
A synthetic January/February dataset was used.
Verified after recalculation:
- Budget Housing actual = 1000
- Budget Food actual = 500
- Budget Debt Payments actual = 200
- Spending Insights Housing = 1000
- Spending Insights Food = 500
- Annual Review January income = 3000
- Annual Review January expenses = 1700
- Annual Review January net savings = 1300
- Annual Review January debt paid = 200
- Cash Flow January income = 3000
- Cash Flow January expenses = 1700
- Cash Flow January net cash flow = 1300

## Result
Production candidate: Personal_Money_Command_Center_v1.9_CONNECTED_SYSTEM.xlsx

A9 remains 0% because this is targeted formula hardening, not the complete final QA gate. Android Excel, all-language, blank-state, visual and packaging tests are still required.

Intermediate file is intentionally not released to the user.
