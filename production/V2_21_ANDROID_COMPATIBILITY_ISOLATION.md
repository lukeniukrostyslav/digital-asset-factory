# V2.21 — ANDROID COMPATIBILITY ISOLATION CANDIDATE

Date: 24.09.2026

## User result

The first Android-clean rebuild produced the same Excel repair prompt and prolonged "Подготовка..." state.

Therefore the previous hypothesis (LibreOffice extension alone) was insufficient.

## New isolation strategy

The new Android-test candidates were rebuilt from the pre-LibreOffice release-candidate workbooks using openpyxl.

For compatibility isolation:
- removed workbook definedNames used only for print titles/filter metadata;
- removed the Planned vs Actual chart and its drawing/chart package parts;
- preserved all 15 worksheets;
- preserved formulas;
- preserved data-validation controls;
- preserved tables;
- preserved workbook content and core layout.

The candidates contain:
- 0 definedNames;
- 0 charts;
- 0 macros;
- valid XML across all package parts;
- the repaired Cash Flow formulas remain present.

## Important correction

A prior audit incorrectly reported 0 defined names for the LibreOffice-generated candidate. The workbook actually contained print-title and filter-database defined names. This checkpoint corrects that record.

## Test goal

This is an isolation candidate, not the final commercial design.

If Android opens it, we will reintroduce nonessential visual features one at a time and retest. If it still fails, the next investigation will target remaining OOXML features and formulas.

No final release is claimed.
