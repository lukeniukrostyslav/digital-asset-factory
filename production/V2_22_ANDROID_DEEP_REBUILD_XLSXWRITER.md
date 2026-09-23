# V2.22 — ANDROID DEEP REBUILD / XlsxWriter CORE

Date: 24.09.2026

## Problem

Two previous Android candidates produced the same Excel repair prompt.

## Investigation

Microsoft documents that .xlsx is supported on Android, but mobile Excel does not support every workbook feature identically. Current Microsoft documentation confirms data validation viewing is supported; it also documents mobile-specific feature limitations. The project therefore needs a conservative OOXML core rather than relying on desktop/LibreOffice round-trips.

## Rebuild

A new compatibility-core workbook was generated directly with XlsxWriter from the approved workbook content, instead of saving the workbook through LibreOffice or openpyxl.

Compatibility isolation:
- 15 worksheets preserved.
- formulas preserved: 261 in Blank / 226 in Sample.
- data validation preserved: 3 collections per workbook.
- hidden translation/list sheets preserved.
- freeze panes removed.
- charts/drawings removed.
- conditional formatting removed.
- Excel tables removed for this isolation candidate.
- defined names removed.
- auto-filters removed.
- macros absent.
- external links absent.
- extLst/LibreOffice extensions absent.
- print-title/filter defined names absent.
- cached formula results populated from the last verified recalculation.

## Internal verification

Blank:
- dashboard cached state: all zero.
- 261 formulas.
- 0 formula-error literals.
- 0 external formula references.
- 15 sheets.
- LibreOffice round-trip reopened successfully.
- 261 formulas remained after round-trip.
- 0 formula-error literals after round-trip.

Sample:
- Dashboard cached metrics:
  - Income 3000
  - Expenses 2000
  - Net Cash Flow 1000
  - Debt Balance 1200
  - Savings 500
  - Net Worth 1800
  - Savings Rate 33.33%
- 226 formulas.
- 0 formula-error literals.
- 0 external formula references.
- 15 sheets.
- LibreOffice round-trip reopened successfully.
- 226 formulas remained after round-trip.
- 0 formula-error literals after round-trip.

## Important limitation

No emulator or physical Android Excel instance is available in the execution environment, so Android opening cannot be certified here. The file given to the user is therefore a single deep-rebuild Android test candidate, not the final commercial package.

If this candidate opens, the next task is to reintroduce visual features one controlled layer at a time and keep the Android-compatible core as the release baseline.
