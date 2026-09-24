# PRODUCT-BUILD-09 — FULL TECHNICAL / MOBILE / LOCALIZATION QA

Дата: 24.09.2026

## Status

PRODUCT-BUILD-09: 100% — QA SPECIFICATION + STATIC ARCHITECTURE AUDIT

Важно:
это завершение QA-плана и статического аудита архитектуры. Физическая live Notion workspace ещё не создана/подключена, поэтому этот checkpoint не утверждает прохождение физического Android/mobile acceptance.

## 1. OFFICIAL CAPABILITY AUDIT

Проверено по актуальной документации Notion:

- одна database поддерживает несколько views;
- каждая view имеет собственные layout, property visibility, filters, sorts и groups;
- linked views позволяют показывать один источник данных в разных местах;
- Relations соединяют pages между databases;
- Rollups агрегируют данные через Relations;
- mobile имеет отдельную навигацию и позволяет открывать database views;
- database templates задают свойства и содержимое новых pages.

Источники:
https://www.notion.com/help/views-filters-and-sorts
https://www.notion.com/help/workspaces-on-mobile
https://www.notion.com/help/relations-and-rollups
https://www.notion.com/help/database-templates

## 2. ARCHITECTURE QA

Expected core databases:

1. Life Areas
2. Goals
3. Projects
4. Tasks
5. Habits
6. Reviews
7. Captures
8. Notes

Home и Today:
dashboard / linked views, не отдельные databases.

Result:
PASS — архитектура не содержит дублирующих mobile databases.

## 3. RELATION QA

Expected primary chain:

Life Area → Goal → Project → Task

Additional:

Life Area → Habits
Reviews ↔ Goals
Reviews ↔ Projects
Reviews ↔ Tasks
Reviews ↔ Habits
Notes ↔ Life Areas / Goals / Projects

Rules:

Goal → one Life Area.
Project → one Goal + one Life Area.
Task → one Project where applicable + one Life Area where applicable.
Habit → one Life Area.

Result:
PASS at specification level.

## 4. ROLLUP QA

Allowed:
- Task Count on Projects;
- Project Count on Goals;
- secondary counts on Life Areas.

No rollup-of-rollup architecture.

Official Notion documentation confirms Rollups aggregate values from related pages and supports calculations such as Count all, Count values, Sum and Average depending on property type. citeturn0search14

Result:
PASS.

## 5. FORMULA QA

Core formulas limited to:

- Overdue;
- Due Today where useful;
- simple progress display.

Formula policy:
views first, formulas second.

No complex analytics required for V1.

Result:
PASS at design level.

Physical formula execution remains a live-workspace test.

## 6. VIEW QA

Required primary views:

Home
Today
Overdue
This Week
Tasks Master
Tasks Board
Active Goals
Goal Board
Active Projects
Project Board
Project Timeline
Active Habits
Upcoming Reviews
Weekly
Monthly
Quarterly
Yearly
Capture Inbox
Recent Notes
Active Life Areas
Calendar

Each view has explicit:
- layout;
- filters;
- sorts;
- property visibility.

Notion confirms view settings are independent per view. citeturn0search0

Result:
PASS.

## 7. MOBILE QA SPECIFICATION

Primary mobile flows:

Start Here
→ Life Areas
→ Goal
→ Project
→ Task
→ Today.

Required mobile views:

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

Mobile rule:
no primary action should depend on horizontal scrolling.

Notion mobile provides persistent bottom navigation, search, Inbox, page creation and access to database views. citeturn0search2

Result:
PASS at specification level; physical device test pending live workspace.

## 8. MOBILE PROPERTY QA

Task:
Task / Status / Due / Priority / Project

Project:
Project / Status / Goal / Life Area / Next Action / Target Date

Goal:
Goal / Status / Life Area / Progress / Target Date

Habit:
Habit / Frequency / Life Area / Status

Review:
Review / Type / Period / Status

Secondary properties remain available inside page.

Result:
PASS.

## 9. ONBOARDING QA

Required:

O1 Language.
O2 Start Here.
O3 Life Area.
O4 Goal.
O5 Project.
O6 Task.
O7 Today.
O8 Complete.
O9 Review.
O10 Continue without onboarding.

Result:
PASS.

## 10. FIVE-LANGUAGE QA

Required editions:

EN
IT
FR
DE
RU

Check:
- terminology;
- onboarding;
- empty states;
- review prompts;
- AI prompts;
- help;
- visible navigation.

Internal formula/relation architecture remains stable.

Result:
PASS at specification level.

## 11. TRANSLATION CONSISTENCY

Canonical terms are fixed in BUILD-06.

No alternative translation should appear for the same core concept inside one edition.

Critical terms:
Goal
Project
Task
Life Area
Review
Capture
Today
Progress
Status
Priority.

Result:
PASS.

## 12. AI QA

Eight workflows:

Plan My Day
Weekly Review
Goal → Action Plan
Project Breakdown
Brain Dump → Organized Plan
Monthly Review
Goal Check
Simplify My Week

Required:
AI suggests.
User decides.

No automatic destructive action.

Result:
PASS at prompt architecture level.

## 13. SAMPLE QA

Expected:

7 Life Areas
4 Goals
5 Projects
20 Tasks
5 Habits
2+ Reviews
5 Captures
5 Notes

Expected scenarios:
Today
Overdue
This Week
Completed
In Progress
Cancelled
different priorities.

Result:
PASS at specification level.

## 14. BLANK QA

Expected user records:

Goals = 0
Projects = 0
Tasks = 0
Habits = 0
historical Reviews = 0
Captures = 0
Notes = 0

Architecture remains available.

Result:
PASS at specification level.

## 15. DUPLICATION QA

Rule:

Sample and Blank are separate learning/working environments.

No requirement to delete sample records manually.

Result:
PASS at product design level.

## 16. COMMERCIAL INTEGRITY QA

No claims of:

- guaranteed productivity;
- guaranteed life improvement;
- guaranteed success;
- autonomous life management.

Product claim remains factual:
a structured personal organization system with optional AI workflows.

Result:
PASS.

## 17. FRAGILITY AUDIT

Potential fragility:

1. Property renaming can affect formulas.
Mitigation:
stable formula-sensitive names.

2. Complex rollups can create maintenance problems.
Mitigation:
minimal rollups.

3. AI availability can vary by plan.
Mitigation:
AI optional.

4. Buttons/actions can vary by plan.
Mitigation:
manual workflows remain.

5. Mobile layouts can become crowded.
Mitigation:
limited primary properties.

6. Widgets/external integrations can break.
Mitigation:
core system does not require them.

Result:
PASS with mitigations documented.

## 18. CURRENT CRITICAL GAPS

The static architecture audit identifies four items that cannot honestly be marked physically passed yet:

G1 — Live Notion workspace construction.
G2 — Real Android/mobile visual acceptance.
G3 — Real formula execution test.
G4 — Real duplication/import test.

These are not hidden.

They move to the operational QA phase after a live workspace is available.

## 19. RELEASE-BLOCKING RULE

PRODUCT-BUILD-09 can be marked complete as QA specification/static audit.

It cannot be interpreted as final product QA.

Final release remains blocked until G1–G4 and subsequent commercial gates are physically tested.

## 20. QA SCOREBOARD

Architecture specification: PASS
Relations design: PASS
Rollup design: PASS
Formula design: PASS
Views specification: PASS
Mobile UX specification: PASS
Onboarding specification: PASS
Five-language specification: PASS
AI prompt architecture: PASS
Sample specification: PASS
Blank specification: PASS
Commercial integrity: PASS

Physical live-workspace QA:
PENDING

## 21. NEXT

PRODUCT-BUILD-10 — COMMERCIAL PACKAGE.

Prepare:

- final folder structure;
- START-HERE.pdf;
- LICENSE.txt;
- AI prompt pack;
- printable reviews;
- five-language support package;
- Sample;
- Blank;
- support documentation;
- versioning;
- asset register;
- release manifest;
- customer delivery structure.

## 22. Status

PRODUCT-BUILD-09 — 100% as specification/static QA.
Physical QA gates remain explicitly pending.
