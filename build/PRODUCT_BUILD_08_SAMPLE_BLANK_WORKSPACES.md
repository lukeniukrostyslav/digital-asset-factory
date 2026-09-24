# PRODUCT-BUILD-08 — SAMPLE / BLANK WORKSPACES

Дата: 24.09.2026

## Status

PRODUCT-BUILD-08: 100%

## 1. Цель

Создать две чётко разделённые версии продукта:

SAMPLE — готовая демонстрационная система с полностью вымышленными данными.

BLANK — чистая рабочая система для пользователя.

Главный принцип:

SAMPLE = LEARN
BLANK = BUILD

## 2. SAMPLE WORKSPACE

Sample должен демонстрировать полный основной цикл:

Capture
→ Clarify
→ Goal
→ Project
→ Task
→ Today
→ Review
→ Adjust

Он не должен быть просто набором случайных записей.

Каждая sample-запись должна существовать для демонстрации конкретной функции.

## 3. SAMPLE LIFE AREAS

7 fictional areas:

1. Work
2. Personal
3. Family
4. Health
5. Learning
6. Finance
7. Home

Статусы:
Active / Paused / Archived.

## 4. SAMPLE GOALS

4 fictional goals:

### Goal 1 — Work
"Prepare a clearer weekly workflow."

Life Area:
Work

Status:
Active

Progress:
45%

### Goal 2 — Health
"Build a consistent morning routine."

Life Area:
Health

Status:
Active

Progress:
30%

### Goal 3 — Learning
"Complete a structured learning project."

Life Area:
Learning

Status:
Active

Progress:
60%

### Goal 4 — Home
"Organize the home workspace."

Life Area:
Home

Status:
Completed

Progress:
100%

Все данные являются fictional sample data.

## 5. SAMPLE PROJECTS

5 projects:

1. Weekly Workflow Setup
→ Work Goal

2. Morning Routine
→ Health Goal

3. Learning Sprint
→ Learning Goal

4. Workspace Organization
→ Home Goal

5. Personal Planning Reset
→ Personal Life Area

Каждый project имеет:
- Goal where applicable;
- Life Area;
- Status;
- Target Date;
- Next Action;
- Progress.

## 6. SAMPLE TASKS

20 tasks.

Распределение:

Work — 5
Health — 4
Learning — 4
Home — 3
Personal — 2
Finance — 1
Family — 1

Statuses должны демонстрировать:
- To Do;
- In Progress;
- Done;
- Cancelled.

Priorities должны демонстрировать:
- High;
- Medium;
- Low.

Dates должны включать:
- today;
- future;
- past;
- no date.

Это позволяет проверить Today, Overdue и This Week.

## 7. SAMPLE HABITS

5 habits:

1. Morning planning
2. Daily walk
3. Learning session
4. Evening reset
5. Weekly review

Разные frequencies:
Daily
Weekdays
Weekly

Без сложного streak engine.

## 8. SAMPLE REVIEWS

Минимум:

1 Weekly Review
2 Monthly Review

Weekly Review:
содержит связанные Goals, Projects, Tasks и Habits.

Monthly Review:
демонстрирует месячный reflection workflow.

Статусы:
Completed / In Progress.

## 9. SAMPLE CAPTURES

5 captures:

1. Task idea
2. Project idea
3. Note
4. Reminder
5. Question

Некоторые:
Processed = true

Некоторые:
Processed = false

Это демонстрирует Inbox workflow.

## 10. SAMPLE NOTES

5 notes:

- Reference
- Journal
- Idea
- Learning
- Personal

Каждая note имеет понятную связь с соответствующей Life Area или Project, если это полезно.

## 11. SAMPLE RELATION INTEGRITY

Каждая sample relation должна быть проверяема.

Пример:

Work
↓
Prepare a clearer weekly workflow
↓
Weekly Workflow Setup
↓
Prepare weekly task list
↓
Today

Нельзя создавать orphan records без причины.

Исключение:
Capture может временно не иметь destination.

## 12. SAMPLE STATUS DISTRIBUTION

Sample обязан демонстрировать не только Active.

Используются:

Not Started
Active
On Hold
Completed
Archived

и для Projects:

Planning
Active
Waiting
Completed
Archived.

Так пользователь видит, как система работает с разными состояниями.

## 13. SAMPLE MOBILE OBJECTIVE

Sample должен быть понятен на телефоне.

Проверяем:

Home
Today
Capture
Goals
Projects
Tasks
Habits
Reviews

Не перегружать mobile views sample properties.

## 14. SAMPLE TEACHING LAYERS

Sample показывает:

Layer 1:
как создать task.

Layer 2:
как связать task с project.

Layer 3:
как project связан с goal.

Layer 4:
как goal относится к Life Area.

Layer 5:
как Review помогает изменить систему.

Это обучение через данные, а не через длинную инструкцию.

## 15. BLANK WORKSPACE

Blank содержит:

- databases;
- relations;
- rollups;
- formulas;
- views;
- templates;
- navigation;
- onboarding;
- help;
- AI workflows;
- localization structure.

Но не содержит fictional history.

## 16. BLANK DATABASE STATE

Life Areas:
может содержать starter suggestions только если они явно обозначены как optional setup choices.

Goals:
0 user records.

Projects:
0 user records.

Tasks:
0 user records.

Habits:
0 user records.

Reviews:
0 historical reviews.

Captures:
0 records.

Notes:
0 records.

Главное правило:
Blank не должен создавать впечатление, что пользователь уже имеет историю жизни.

## 17. STARTER OPTIONS

Чтобы Blank не выглядел пустым и сложным, Start Here предлагает:

Suggested Life Areas:
Work
Personal
Family
Health
Learning
Finance
Home

Но пользователь сам выбирает.

Это suggestions, а не pre-created personal records.

## 18. SAMPLE → BLANK

Продукт не должен требовать ручного удаления 50 sample records.

Предпочтительный коммерческий workflow:

1. Open Sample.
2. Learn.
3. Duplicate/instantiate Blank.
4. Start personal setup.

Sample остаётся неизменённым.

Blank становится рабочей системой.

## 19. RESET RULE

Если пользователь хочет начать заново:

не использовать Sample как рабочую базу.

Использовать новый Blank copy.

Это предотвращает смешивание fictional и personal data.

## 20. DATABASE TEMPLATES

Sample и Blank используют одинаковые database templates.

Templates должны создавать:
- правильные properties;
- правильные defaults;
- нужную структуру страницы;
- localized guidance where appropriate.

Notion подтверждает, что database templates могут заранее задавать content и properties новых страниц. citeturn0search2

## 21. SAMPLE LOCALIZATION

Sample content должен быть доступен в пяти editions.

EN:
fictional English sample.

IT:
fictional Italian sample.

FR:
fictional French sample.

DE:
fictional German sample.

RU:
fictional Russian sample.

Logic и relations одинаковые.

## 22. LOCALIZATION RULE

Sample names may be translated naturally.

Do not use awkward literal translations.

Example:

Weekly Workflow Setup

IT:
Impostazione del flusso di lavoro settimanale

FR:
Mise en place du flux de travail hebdomadaire

DE:
Wöchentliche Arbeitsorganisation

RU:
Настройка еженедельного рабочего процесса

## 23. FICTIONAL DATA SAFETY

No real personal information.

No real addresses.

No real contact details.

No real financial account numbers.

No real medical records.

No claims that sample users are real people.

All sample data must be obviously fictional.

## 24. SAMPLE QA MATRIX

S1:
7 Life Areas exist.

S2:
4 Goals exist.

S3:
5 Projects exist.

S4:
20 Tasks exist.

S5:
5 Habits exist.

S6:
Weekly + Monthly Reviews exist.

S7:
5 Captures exist.

S8:
5 Notes exist.

S9:
relations resolve correctly.

S10:
Today has relevant sample tasks.

S11:
Overdue contains a past open task.

S12:
This Week contains future/current tasks.

S13:
Completed tasks appear correctly.

S14:
Sample has no broken relations.

## 25. BLANK QA MATRIX

B1:
0 Goals.

B2:
0 Projects.

B3:
0 Tasks.

B4:
0 Habits.

B5:
0 historical Reviews.

B6:
0 Captures.

B7:
0 Notes.

B8:
relations are ready.

B9:
views are ready.

B10:
templates are ready.

B11:
onboarding is ready.

B12:
AI workflows are ready.

B13:
five-language structure is ready.

## 26. DUPLICATION SAFETY

Sample and Blank must not share mutable personal data.

Each edition must be clearly labelled.

Recommended labels:

SAMPLE — Learn how it works

BLANK — Build your own system

## 27. USER EXPERIENCE

Sample opening:

"Explore the system with fictional data. Follow the relationships, open a few tasks, then create your own workspace from Blank."

Blank opening:

"Your workspace is ready. Start with one Life Area, one Goal, one Project and one Task."

## 28. COMMERCIAL QUALITY

The product should never force the buyer to clean a giant demo database before using it.

Sample is optional learning environment.

Blank is the primary working environment.

## 29. ACCEPTANCE

PRODUCT-BUILD-08 complete at architecture/specification level.

This checkpoint does not claim that physical Notion copies have been generated or duplicated.

## 30. NEXT

PRODUCT-BUILD-09 — FULL TECHNICAL / MOBILE / LOCALIZATION QA.

QA layers:
- architecture;
- relations;
- rollups;
- formulas;
- views;
- mobile;
- desktop;
- onboarding;
- five languages;
- AI;
- Sample;
- Blank;
- duplication;
- commercial integrity.

## 31. Status

PRODUCT-BUILD-08 — 100%.
