# MOBILE LANGUAGE QA CHECKPOINT 01

The multilingual workbook was rebuilt with a mobile-safe selector architecture.

Selector:
- Dashboard J2
- simple Data Validation list sourced from hidden Lists sheet
- English / Русский / Italiano / Español

Compatibility approach:
- core UI labels use IF-based formulas instead of INDEX/MATCH;
- formulas recalculate on open;
- workbook calculation is set to automatic.

Actual recalculation test performed for all four languages using a spreadsheet engine.

Verified outputs:
- Dashboard title changes in all four languages.
- Monthly income changes in all four languages.
- Budget Category changes in all four languages.
- Transactions Tracker changes in all four languages.
- Debt Tracker label changes.
- Savings Goals label changes.
- Annual Review title changes.

The workbook passed this structural/recalculation QA.

Important: the mobile app itself was not remotely controlled; final device UI verification still needs to be performed by opening the supplied workbook in the user's Excel mobile app.
