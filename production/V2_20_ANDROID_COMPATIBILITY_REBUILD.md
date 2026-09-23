# V2.20 — ANDROID OPENING FAILURE / COMPATIBILITY REBUILD

Date: 24.09.2026

## User device test

The Android Excel test produced:
"Ошибка в части содержимого ... Выполнить попытку восстановления?"

After selecting Yes, the workbook remained on "Подготовка..." for an extended period.

## Root-cause investigation

The candidate ZIP is structurally valid and can be opened by desktop-side parsers, but its workbook.xml was written by LibreOffice and contained a LibreOffice-specific <extLst> / loext extension.

This is a compatibility risk for Excel Android. The issue is therefore treated as a real release blocker, not as an Android user error.

## Compatibility rebuild

Created new Android-test candidates by removing the LibreOffice-specific workbook extension while leaving workbook sheets, formulas, tables, charts, validations and other package members intact.

Validation after rebuild:
- both files open with openpyxl;
- all 15 sheets preserved;
- no workbook extLst remains;
- no macros;
- ZIP package integrity preserved.

## Test instruction

The previous candidates should no longer be used for Android validation.

The rebuilt Android-test candidates are the correct files for the next physical test.

## Release status

A9 remains below 100% until the user confirms the rebuilt candidates open and function correctly on Android.

No final commercial release is claimed yet.
