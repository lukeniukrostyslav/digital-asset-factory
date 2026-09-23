# V2.25 — PRINT / VISUAL QA FINDINGS

Date: 2026-09-24

## Finding

The current V2.24 Android compatibility core intentionally removed print-title and other desktop presentation layers during compatibility isolation.

A LibreOffice PDF render of the current core confirms that Start Here can span multiple printed pages and that the workbook print presentation is not yet the final commercial print experience.

This is expected for the compatibility-isolation candidate and is NOT an Android defect.

## Required final print pass

After Android acceptance:
- restore print areas per sheet where useful;
- fit important review sheets to intended page width;
- keep Dashboard print-ready;
- preserve Letter output for the commercial printable workflow;
- prevent orphaned instruction rows;
- review wrapped text and clipped notes;
- render Blank and Sample to PDF;
- inspect every rendered page;
- confirm no content is cut off.

## Rule

Do not reintroduce print settings into the Android-core candidate until the Android opening gate is passed. Treat print/desktop presentation as a controlled compatibility layer.

## Status

Print UX: open.
Android core: separate release gate.
No user-facing intermediate workbook released.
