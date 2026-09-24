# PRODUCT-BUILD-04 — VIEWS / MOBILE UX

Дата: 24.09.2026

## Status

PRODUCT-BUILD-04: 100%

## 1. Цель

Создать view-архитектуру Personal Life Command Center, в которой одна и та же информация показывается через разные рабочие контексты, без дублирования данных.

Notion поддерживает несколько views одного database, включая Table, Board, Timeline, Calendar, List, Gallery и Chart; у каждой view могут быть собственные filters, sorts, groups и property visibility. citeturn0search3turn0search5

## 2. UX PRINCIPLE

MOBILE-FIRST, NOT DESKTOP-SHRUNK.

Главный сценарий:

Home
→ Today
→ Capture
→ Execute
→ Review.

На мобильном пользователь не должен открывать сложную таблицу, чтобы выполнить основное действие.

## 3. HOME

Home — dashboard, не database.

Состав:

1. Welcome / current focus
2. Today
3. Quick Capture
4. Active Goals
5. Active Projects
6. Upcoming Reviews
7. Optional AI Assistant
8. Secondary navigation

Главный экран не показывает все 8 databases одновременно.

Priority:
Today > Capture > Goals/Projects > Reviews > secondary modules.

## 4. TODAY

Today — главный execution view.

Источник:
Tasks database.

Filter:
- Status != Done
- Due is today

Optional second section:
- overdue open tasks.

Sort:
Priority descending;
Due ascending.

Visible mobile properties:
Task
Status
Due
Priority
Project

Hidden/secondary:
Goal
Life Area
Habit
Created
Last Edited
Notes

## 5. OVERDUE

Источник:
Tasks.

Filter:
- Status != Done
- Due before today

Sort:
Due ascending.

Purpose:
одна задача — понять, что требует решения.

Не добавлять charts.

## 6. THIS WEEK

Источник:
Tasks.

Filter:
- Status != Done
- Due within current week.

Sort:
Due ascending;
Priority descending.

Layout:
List.

Reason:
минимальная плотность информации и хорошая мобильная читаемость.

## 7. TASKS — MASTER VIEW

Master Tasks view.

Layout:
Table/List depending on workspace usage.

Properties:
Task
Status
Due
Priority
Project
Life Area

Additional properties hidden by default.

Purpose:
полный operational database.

## 8. TASKS — BOARD

Board grouped by Status:

To Do
In Progress
Done
Cancelled

Use case:
desktop planning.

Mobile:
не является primary execution view.

## 9. GOALS

Goals database views:

### Active Goals
Filter:
Status = Active.

Properties:
Goal
Life Area
Progress
Target Date
Projects count

### Goal Board
Board grouped by Status.

### Goal Timeline
Optional only if Target Date is populated.

Do not make timeline mandatory.

## 10. PROJECTS

### Active Projects

Filter:
Status = Active.

Properties:
Project
Goal
Life Area
Next Action
Progress
Target Date

Sort:
Target Date ascending.

### Project Board

Board grouped by Status.

### Project Timeline

Optional desktop planning view.

## 11. HABITS

Primary view:
List.

Filter:
Status = Active.

Properties:
Habit
Frequency
Life Area
Target

Secondary:
Paused
Completed
Archived.

V1 deliberately avoids a complex streak dashboard.

## 12. REVIEWS

Views:

### Upcoming Reviews
Status != Completed.

Sort:
Period ascending.

### Weekly
Type = Weekly.

### Monthly
Type = Monthly.

### Quarterly
Type = Quarterly.

### Yearly
Type = Yearly.

The review page itself contains linked views and prompts.

## 13. CAPTURE

Capture database is designed as an inbox.

Primary view:
Inbox.

Filter:
Processed = false.

Sort:
Created descending.

Mobile properties:
Capture
Type
Created
Processed

Secondary:
Life Area
Destination.

Workflow:

Capture
→ Clarify
→ Choose Destination
→ Move/Create
→ Mark Processed.

## 14. NOTES

Primary:
Recent Notes.

Sort:
Updated descending.

Secondary views:
- Reference
- Journal
- Idea
- Learning
- Personal

Mobile:
show title, type, updated date.

## 15. LIFE AREAS

Primary:
Active Life Areas.

Layout:
List.

Properties:
Life Area
Status
Goal Count
Project Count
Habit Count.

Each Life Area page may expose linked views for its Goals, Projects and Habits.

## 16. CALENDAR

Calendar is a navigation view, not a separate database.

Primary sources:
Tasks with Due;
Projects with Target Date;
Reviews with Period/Date.

Do not create a second calendar database.

Notion Calendar view displays database items according to their Date property. citeturn0search3

## 17. MOBILE PROPERTY POLICY

Mobile primary views expose only the minimum useful properties.

Rule:
5–6 visible properties maximum where practical.

Everything else remains accessible inside the page.

This is compatible with Notion's property visibility controls per view. citeturn0search3

## 18. PAGE LAYOUT POLICY

Database page layouts should prioritize:

Heading
→ primary properties
→ relevant relations
→ page content
→ secondary details.

Notion layouts can customize which properties are prominent or hidden, and can include tabbed layouts with views of related databases. citeturn0search0

Important:
full layout-builder experience is strongest on desktop/web, while layouts can be viewed on mobile. citeturn0search0

## 19. TASK PAGE LAYOUT

Heading:
Task

Primary:
Status
Due
Priority
Project

Secondary:
Goal
Life Area
Habit
Notes
Created
Last Edited

Body:
Task notes / context.

## 20. PROJECT PAGE LAYOUT

Heading:
Project

Primary:
Status
Goal
Life Area
Progress
Target Date
Next Action

Body:
Project notes.

Related section:
Tasks linked to this project.

Notion tabbed layouts can expose related database views within a page. citeturn0search0

## 21. GOAL PAGE LAYOUT

Heading:
Goal

Primary:
Status
Life Area
Progress
Target Date

Body:
Goal definition / success criteria.

Related:
Projects.

## 22. REVIEW PAGE LAYOUT

Heading:
Review

Primary:
Type
Period
Status
Focus

Body prompts:

1. What happened?
2. What worked?
3. What did not work?
4. What matters now?
5. What should stop?
6. What should continue?
7. What are the next actions?

Related:
Goals / Projects / Tasks / Habits.

## 23. HOME MOBILE NAVIGATION

The product's internal navigation should remain simple.

Primary:
Home
Today
Capture
Goals
Projects
Reviews

Secondary:
Tasks
Habits
Life Areas
Calendar
Notes
AI
Settings

Notion's mobile app already provides persistent bottom navigation and access to search, inbox and page creation, so the template should not attempt to recreate native navigation unnecessarily. citeturn0search4

## 24. DESKTOP VS MOBILE

Desktop:
- dashboards;
- wider tables;
- board;
- timeline;
- calendar;
- deeper analytics.

Mobile:
- list;
- focused database views;
- short pages;
- minimal properties;
- quick capture;
- Today execution.

Same data.
Different presentation.

## 25. VIEW FRAGILITY RULE

Every primary workflow must have one simple view.

No primary workflow should depend on:
- widgets;
- external integrations;
- AI;
- complex formulas;
- paid-only features.

## 26. ACCEPTANCE TESTS

V4.1 Home:
user can reach Today and Capture in one step.

V4.2 Today:
only current open tasks are shown.

V4.3 Overdue:
past open tasks are isolated.

V4.4 This Week:
weekly execution list works.

V4.5 Goals:
active goals are visible without opening master table.

V4.6 Projects:
active projects show next action and target date.

V4.7 Habits:
active habits are visible.

V4.8 Reviews:
next review is easy to find.

V4.9 Capture:
new inbox item can be created and processed.

V4.10 Mobile:
primary views do not require horizontal scrolling for normal operation.

V4.11 Desktop:
full planning views remain available.

V4.12 Blank:
no sample records appear in Blank.

## 27. QUALITY GATE

The view architecture is accepted only when:

- one data source per concept;
- no duplicated databases for mobile;
- filters are explicit;
- sorts are explicit;
- properties are intentionally visible/hidden;
- mobile has a short path to action;
- desktop provides deeper planning;
- optional modules do not clutter core navigation.

## 28. NEXT

PRODUCT-BUILD-05 — ONBOARDING / QUICK START.

Flow:

Language
→ Start Here
→ Choose Life Areas
→ Create ONE Goal
→ Create ONE Project
→ Create ONE Task
→ Open Today
→ Complete
→ Review.

## 29. Status

PRODUCT-BUILD-04 — 100%.
