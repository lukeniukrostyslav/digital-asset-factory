# PRODUCT-BUILD-03 — RELATIONS / ROLLUPS / FORMULAS

Дата: 24.09.2026

## Status

PRODUCT-BUILD-03: 100%

Цель: зафиксировать и проверить логику связей, агрегатов и минимальных формул для Core databases.

## 1. Official Notion capability check

Актуальная документация Notion подтверждает:
- Relations связывают страницы между разными databases.
- Two-way relations синхронизируют связь в обеих databases.
- Rollups агрегируют свойства связанных страниц.
- Rollup нельзя строить поверх другого rollup.
- Формулы могут работать с Relation и Rollup properties.
- Database buttons доступны на всех планах, но отдельные button actions могут быть plan-dependent.

Источники:
https://www.notion.com/help/relations-and-rollups
https://www.notion.com/en-gb/help/formula-syntax
https://www.notion.com/help/database-buttons

## 2. RELATION MATRIX

Life Areas ↔ Goals:
Goals → Life Areas, limit 1; Life Areas получает reciprocal Goals.

Goals ↔ Projects:
Projects → Goals, limit 1; Goals получает reciprocal Projects.

Life Areas ↔ Projects:
Projects → Life Areas, limit 1; Life Areas получает reciprocal Projects.

Projects ↔ Tasks:
Tasks → Projects, limit 1; Projects получает reciprocal Tasks.

Life Areas ↔ Tasks:
Tasks → Life Areas, limit 1; Life Areas получает reciprocal Tasks.

Life Areas ↔ Habits:
Habits → Life Areas, limit 1; Life Areas получает reciprocal Habits.

Reviews ↔ Goals / Projects / Tasks / Habits:
Reviews использует multi-relations; обратные свойства также multi-relations.

Notes:
опциональные relations к Life Areas, Goals и Projects.

Captures:
не получают постоянную сложную relation-сеть; Capture остаётся inbox record.

## 3. HIERARCHY RULE

Primary hierarchy:

Life Area
↓
Goal
↓
Project
↓
Task

Hierarchy поддерживается relation limits и workflow, а не сложными formulas.

## 4. PROJECT ROLLUPS

Projects получают только полезные aggregates:

- Task Count = Tasks → Count all.
- Completed Task information — через простой проверенный механизм, без rollup-of-rollup.
- Progress — Number 0–100 в V1.

Notion официально не поддерживает rollup поверх другого rollup. citeturn0search1

## 5. GOAL ROLLUPS

Goals:
- Project Count;
- optional Active Project Count.

Goal Progress в V1 — прямое Number property 0–100.

Это надёжнее сложной многоуровневой автоматизации.

## 6. LIFE AREA ROLLUPS

Secondary:
- Goal Count;
- Project Count;
- Active Habit Count.

Не показывать их на главном mobile view.

## 7. TASK FORMULAS

Основная derived state:

Overdue:
задача не Done + Due заполнен + Due раньше сегодня.

Концептуальная формула:

and(prop("Status") != "Done", !empty(prop("Due")), prop("Due") < today())

Due Today:
Due совпадает с сегодняшней датой.

Формулы должны быть проверены непосредственно в Notion перед release.

Notion formulas поддерживают property references и date functions. citeturn0search9

## 8. FILTER VS FORMULA RULE

Если информацию можно получить обычным database view filter — использовать filter.

Formula использовать только когда derived value действительно нужен пользователю.

Это уменьшает техническую сложность.

## 9. PROJECT PROGRESS

V1:
Progress = Number 0–100.

Optional display formula допускается только если она улучшает UX.

Не строить прогресс на нескольких вложенных rollups в V1.

## 10. HABIT LOGIC

V1 не создаёт отдельный daily habit-event engine.

Habit database хранит:
- Habit;
- Frequency;
- Status;
- Start Date;
- Target.

Полный Habit Log может стать будущим модулем.

## 11. REVIEW LOGIC

Reviews связываются с:
- Goals;
- Projects;
- Tasks;
- Habits.

Сложные aggregates не нужны.

Review — reflection layer с guided prompts и linked views.

## 12. FORMULA POLICY

Tier 1 — core:
простые status/date formulas.

Tier 2 — optional:
простые progress displays.

Tier 3 — future:
advanced analytics.

V1 не зависит от Tier 3.

## 13. PROPERTY NAME STABILITY

Formula-dependent properties должны иметь стабильные внутренние имена.

Visible labels могут локализоваться в пяти editions.

Notion formulas ссылаются на свойства по именам, поэтому необдуманное переименование может нарушить formulas. citeturn0search9

## 14. BUTTON POLICY

Buttons — только UX accelerators.

Допустимые кандидаты:
- Task → Complete;
- Capture → Processed;
- Review → Start Review.

Core workflow обязан работать и без buttons, потому что некоторые button actions зависят от плана. citeturn0search0

## 15. NO-AUTOMATION PRINCIPLE

Если buttons/automations недоступны, пользователь всё равно должен иметь возможность:
- создать task;
- завершить task;
- назначить project;
- создать goal;
- провести review;
- обработать capture.

## 16. TEST MATRIX

R1 — Goal relation:
Goal → Life Area → Project.
Expected: reciprocal relations отображаются.

R2 — Task relation:
Task → Project.
Expected: Project показывает Task.

R3 — Status:
Task → Done.
Expected: views фильтруют правильно.

R4 — Overdue:
past Due + To Do.
Expected: Overdue view/indicator.

R5 — Rollup:
2 Tasks в Project.
Expected: Task Count = 2.

R6 — Goal progress:
20 → 40.
Expected: display обновляется.

R7 — Review:
Weekly Review links Goal, Project, Task.
Expected: reciprocal relations.

R8 — Blank:
blank workspace не содержит sample history.

## 17. SAFETY RULES

Не создавать:
- бессмысленные relation loops;
- duplicate parent properties;
- rollup chains;
- unnecessary self-relations;
- mandatory AI dependencies;
- formulas там, где достаточно view filter.

## 18. MOBILE RULE

Relations могут существовать в database, но быть скрыты в mobile primary view.

Task mobile:
Task / Status / Due / Priority / Project.

Secondary:
Goal / Life Area / Habit / Notes / Created.

## 19. IMPLEMENTATION ORDER

1. Reciprocal relations.
2. Relation limits.
3. Essential rollups.
4. Core formulas.
5. Test records.
6. Relation tests.
7. Formula tests.
8. Mobile property visibility test.
9. Checkpoint.

## 20. ACCEPTANCE

PRODUCT-BUILD-03 complete at architecture/implementation specification level.

Этот checkpoint фиксирует design и проверенные возможности Notion; он не заявляет, что физический Notion workspace уже изменён.

## 21. NEXT

PRODUCT-BUILD-04 — Views / Mobile UX.

Build:
- Home;
- Today;
- This Week;
- Overdue;
- Active Goals;
- Active Projects;
- Habits;
- Reviews;
- Capture;
- Notes;
- mobile layouts.

## 22. Status

PRODUCT-BUILD-03 — 100%.
