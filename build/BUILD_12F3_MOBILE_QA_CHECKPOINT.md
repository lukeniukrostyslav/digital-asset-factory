# BUILD-12F3 — Mobile QA / Localization Consistency Checkpoint

Date: 2026-09-24

## Verified on Android / Notion

Physical Android screenshots were reviewed for all five editions:
- EN
- IT
- FR
- DE
- RU

## Main-page consistency fix

The localized root pages were normalized so all five editions now use the same top-level structure:

1. Capture → Clarify → Plan → Execute → Review → Adjust.
2. Quick Start section
3. Five Quick Start steps
4. AI suggests. You decide.
5. Edition: XX
6. Home / Today / Capture / Quick Start / AI Assistant Hub / Language Hub
7. Eight core databases

The English edition already contained the Quick Start block. DE, IT, FR and RU were updated to contain the equivalent localized Quick Start block.

The previous "Localized edition." line was removed from the four localized editions and replaced by the consistent "Edition: XX" marker.

## Result

All five root pages now have equivalent structure and block count at the top level. Localization is preserved in navigation labels and Quick Start wording.

## Remaining QA

- RU Upcoming view still needs datasource parity verification/fix: its configured view currently references the primary RU Tasks datasource while the current QA task datasource is the secondary RU Tasks source.
- Physical Android touch/rendering QA beyond the screenshots remains to be completed.
