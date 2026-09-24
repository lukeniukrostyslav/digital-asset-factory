# PRODUCT-BUILD-12 — FINAL RELEASE / PUBLICATION GATE

Дата: 24.09.2026

## Status

PRODUCT-BUILD-12: 25% — RELEASE GATE DEFINED; PHYSICAL RELEASE NOT PASSED

Важно:
не объявлять V1.0.0 выпущенным. Финальный release зависит от физического Notion workspace, mobile acceptance, formulas, duplication, final package и controlled checkout.

## 1. RELEASE OBJECTIVE

V1.0.0 должен одновременно пройти:

A. Live workspace
B. Mobile
C. Desktop
D. Relations / formulas
E. Sample / Blank
F. Five-language
G. AI
H. Commercial package
I. Store listing
J. Checkout / delivery

## 2. CURRENT FACTUAL STATE

Completed:
- research program;
- architecture specification;
- core database specification;
- relations/rollups/formula specification;
- views/mobile UX specification;
- onboarding;
- five-language architecture;
- AI workflows;
- sample/blank specification;
- static QA;
- commercial package specification;
- store/checkout specification.

Not physically completed:
- live Notion workspace;
- physical Android acceptance;
- physical formula execution;
- physical Sample → Blank duplication;
- final release files;
- controlled checkout;
- publication.

## 3. LIVE WORKSPACE GATE

Required core databases:

1. Life Areas
2. Goals
3. Projects
4. Tasks
5. Habits
6. Reviews
7. Captures
8. Notes

Required dashboards:

Home
Today

Required navigation:

Home
Today
Capture
Goals
Projects
Reviews

## 4. RELATION GATE

Test chain:

Life Area
→ Goal
→ Project
→ Task

Additional:
Life Area → Habit
Review ↔ Goals/Projects/Tasks/Habits.

PASS criteria:
relations appear in both directions where configured;
limits work;
no broken relation;
no orphan record except intentional Capture inbox items.

## 5. FORMULA GATE

Physical test:

1. Create open task with past Due.
2. Verify Overdue state.
3. Change task to Done.
4. Verify Overdue state disappears.
5. Create today's task.
6. Verify Today view.
7. Change property names only through controlled procedure.

No formula is release-ready until executed successfully in the live workspace.

## 6. ROLLUP GATE

Create Project A.

Add:
Task 1
Task 2

Expected:
Task Count = 2.

No rollup-of-rollup.

## 7. MOBILE GATE

Physical Android acceptance must test:

Home
Today
Capture
Goals
Projects
Tasks
Habits
Reviews
Language Hub
AI Assistant

For each:
- opens;
- readable;
- primary action visible;
- no required horizontal scrolling;
- relation selection usable;
- no critical truncation;
- no broken links.

Notion currently supports database import only on desktop/web, not mobile, so workspace construction/import must be performed on desktop/web; mobile is the usage/acceptance environment. citeturn0search1

## 8. DESKTOP GATE

Test:

- Home dashboard;
- table views;
- board views;
- calendar;
- project/goal pages;
- review pages;
- settings/help.

## 9. SAMPLE GATE

Required:

7 Life Areas
4 Goals
5 Projects
20 Tasks
5 Habits
Weekly Review
Monthly Review
5 Captures
5 Notes

Check:
all relations;
Today;
Overdue;
This Week;
review examples;
status examples.

## 10. BLANK GATE

Blank must contain:
architecture;
views;
templates;
onboarding;
help;
AI instructions;
language structure.

Blank must not contain:
fictional personal history.

Expected user records:
Goals 0
Projects 0
Tasks 0
Habits 0
historical Reviews 0
Captures 0
Notes 0

## 11. SAMPLE → BLANK DUPLICATION GATE

Perform actual duplication in Notion.

Confirm:
- Blank opens;
- relations work;
- views work;
- templates work;
- no Sample records leak into Blank;
- Sample remains intact.

Notion officially supports duplicating public template pages and their sub-pages. citeturn0search11

## 12. FIVE-LANGUAGE GATE

Physical test:

EN
IT
FR
DE
RU

Check:
Start Here;
Home;
Today;
Goals;
Projects;
Tasks;
Reviews;
AI prompts;
Help.

Check long-label layout, especially German, French and Russian.

## 13. AI GATE

Run all 8 workflows with controlled fictional context:

1. Plan My Day
2. Weekly Review
3. Goal → Action Plan
4. Project Breakdown
5. Brain Dump → Organized Plan
6. Monthly Review
7. Goal Check
8. Simplify My Week

Expected:
no invented deadlines;
no destructive action;
no fabricated facts;
human review remains required.

## 14. COMMERCIAL FILE GATE

Generate final:

START-HERE.pdf
LICENSE.txt
README.txt
VERSION.txt
RELEASE-MANIFEST.txt
AI package
PRINTABLES
LANGUAGES
SUPPORT

Generate Sample and Blank delivery assets.

## 15. FILE INTEGRITY

For every final file:

- exists;
- opens;
- correct language;
- correct version;
- no draft markers;
- no temporary files.

Generate SHA-256.

Record hashes in RELEASE-MANIFEST.txt.

## 16. NOTION BACKUP

Before publication, export the final workspace for backup.

Notion currently supports workspace export in HTML/Markdown/CSV formats; individual pages can also be exported as PDF. citeturn0search7

Store release backup separately from customer package.

## 17. MARKETPLACE GATE

If using Notion Marketplace:

- creator profile;
- eligible payment setup if selling directly;
- publish template as Notion Site;
- enable Duplicate as template;
- submit listing;
- select language;
- set price;
- select access locking;
- submit for review.

Notion states that paid Marketplace submissions require review, and direct payment onboarding uses Stripe. citeturn0search0

## 18. CHANNEL SEPARATION

If selling both through Notion Marketplace and a third-party checkout, maintain separate template copies/Notion Site links.

Notion explicitly warns that after direct Marketplace payment onboarding, existing paid template links can become Marketplace checkout links and may no longer work as third-party duplication links. citeturn0search0turn0search8

## 19. MARKETPLACE LOCALIZATION

Notion currently supports template localization on Marketplace, allowing translated versions of a listing/template while sharing the same Marketplace link/slug. citeturn0search10

For our product:
EN / IT / FR / DE / RU localization remains the target.

Physical Marketplace availability of every language must be checked during listing submission.

## 20. STORE CHECKOUT GATE

For selected launch channel:

1. open listing;
2. verify title;
3. verify price;
4. checkout;
5. complete controlled purchase;
6. verify delivery;
7. open Start Here;
8. open Sample;
9. open Blank;
10. verify license;
11. verify support;
12. verify links.

No public launch before controlled test passes.

## 21. VERSION GATE

Release candidate:

V1.0.0-rc1

Only after every blocking test passes:

V1.0.0

If a blocker is discovered:
V1.0.0-rc2 or higher.

Never silently replace a release without versioning.

## 22. BLOCKING FAILURES

Any of these blocks release:

- broken relation;
- formula failure;
- broken mobile primary view;
- inaccessible Sample;
- Sample data inside Blank;
- missing language asset;
- broken AI prompt;
- missing license;
- missing final file;
- broken delivery link;
- incorrect price;
- checkout failure;
- unsupported listing claim.

## 23. FINAL RELEASE DECISION

Release status options:

NOT READY
RELEASE CANDIDATE
READY FOR PUBLICATION
PUBLISHED

Current status:

NOT READY.

Reason:
physical production gates have not yet been executed.

## 24. NEXT OPERATIONAL STEP

The project now leaves the documentation/build-spec phase.

Next action is physical implementation:

1. construct live Notion workspace;
2. configure databases;
3. configure relations;
4. configure views;
5. configure templates;
6. configure formulas;
7. populate Sample;
8. create Blank;
9. build language editions;
10. run Android test;
11. fix blockers;
12. create final package;
13. controlled checkout;
14. publication.

## 25. IMPORTANT TECHNICAL LIMITATION

Current available tooling in this project does not provide a direct Notion workspace editing connector.

Therefore this checkpoint must not pretend that the live workspace was created or modified.

GitHub remains the source of truth for the product architecture/specification and release documentation until a real Notion workspace is connected/created.

## 26. FINAL PROJECT SCOREBOARD

Research: 100%
Build specification: 100%
Static QA: 100%
Physical workspace: 0%
Physical mobile QA: 0%
Physical formula QA: 0%
Physical duplication QA: 0%
Final package: 0%
Store setup: 0%
Checkout: 0%
Publication: 0%

## 27. CURRENT OVERALL

Documentation/specification phase:
COMPLETE.

Physical production phase:
NOT STARTED.

Therefore:
PRODUCT-BUILD-12 = 25% for this gate, not 100%.

## 28. Status

PRODUCT-BUILD-12 — 25%.
Final release NOT READY.
