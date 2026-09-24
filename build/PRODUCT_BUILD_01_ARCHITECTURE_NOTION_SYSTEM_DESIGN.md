# PRODUCT-BUILD-01 — ARCHITECTURE / NOTION SYSTEM DESIGN

Дата: 24.09.2026

## Status

PRODUCT-BUILD-01: 100%

Цель блока: превратить Final Product Specification в техническую архитектуру Notion-системы до начала визуальной сборки.

## 1. Architecture principle

Core architecture:

LIFE AREAS
    ↓
GOALS
    ↓
PROJECTS
    ↓
TASKS
    ↓
REVIEWS

HABITS связаны с LIFE AREAS и могут участвовать в REVIEWS.

NOTES / CAPTURE являются входным слоем и не должны перегружать core databases.

AI ASSISTANT использует структурированный контекст этих баз, но не является обязательной частью данных.

Notion официально поддерживает Relations и Rollups для связи данных между базами. Это позволяет связать Tasks ↔ Projects, Projects ↔ Goals и агрегировать связанные данные. citeturn0search0turn0search12

## 2. Core databases

V1 Core будет состоять из 8 основных databases:

1. Life Areas
2. Goals
3. Projects
4. Tasks
5. Habits
6. Reviews
7. Captures
8. Notes

Calendar не создаётся отдельной database: календарные представления строятся поверх Tasks / Projects / Reviews там, где это полезно.

Это уменьшает количество сущностей и снижает сложность.

## 3. Life Areas database

Purpose:
верхний уровень организации жизни.

Core properties:

- Name
- Status
- Description
- Color/Icon
- Goals relation
- Projects relation
- Tasks relation
- Habits relation

Default sample areas:

Work
Personal
Family
Health
Learning
Finance
Home

Users can customize.

## 4. Goals database

Purpose:
долгосрочные outcomes.

Properties:

- Goal — title
- Life Area — relation, one
- Status — status
- Target Date — date
- Progress — number/formula
- Projects — relation
- Notes — text/page content

Goal status:
- Not Started
- Active
- On Hold
- Completed
- Archived

Rule:
Goal is outcome, not task.

## 5. Projects database

Purpose:
turn goals into concrete outcomes.

Properties:

- Project — title
- Goal — relation, one
- Life Area — relation
- Status
- Start Date
- Target Date
- Tasks — relation
- Next Action — text
- Progress — formula/rollup
- Notes

Project status:
- Planning
- Active
- Waiting
- Completed
- Archived

Architecture:

Goal
→ Project
→ Task

## 6. Tasks database

Purpose:
execution layer.

Properties:

- Task — title
- Status
- Due
- Priority
- Project — relation
- Goal — optional relation
- Life Area — relation
- Habit — optional relation
- Notes
- Created
- Last Edited

Task status:
- To Do
- In Progress
- Done
- Cancelled

Priority:
- Low
- Medium
- High

Core mobile view should expose only:
Task / Status / Due / Priority / Project.

Notion database properties support Status, Select, Date, Formula, Relation, Rollup, Checkbox and Button types, so the architecture can remain native without custom code. citeturn0search2

## 7. Habits database

Properties:

- Habit — title
- Life Area — relation
- Frequency — select
- Status
- Start Date
- Target
- Notes

V1 intentionally avoids complicated streak formulas.

Habit statuses:
- Active
- Paused
- Completed
- Archived

## 8. Reviews database

One database with Review Type:

- Weekly
- Monthly
- Quarterly
- Yearly

Properties:

- Review — title
- Type
- Period
- Date
- Status
- Focus
- Related Goals
- Related Projects
- Related Tasks
- Notes

Each review uses a database template.

Notion database templates can replicate page structures and predefined properties, which is appropriate for repeated Weekly/Monthly/Quarterly/Yearly reviews. citeturn0search4

## 9. Captures database

Purpose:
fast inbox.

Properties:

- Capture — title
- Type
- Created
- Processed
- Area
- Destination
- Notes

Capture Type:
- Task
- Idea
- Note
- Reminder
- Event
- Other

Rule:
Capture is an inbox, not a permanent dumping ground.

Processing flow:

CAPTURE
→ CLARIFY
→ MOVE TO DESTINATION
→ ARCHIVE CAPTURE

## 10. Notes database

Purpose:
persistent reference information.

Properties:

- Note — title
- Type
- Life Area
- Project
- Goal
- Tags
- Created
- Updated

Note Type:
- Reference
- Journal
- Idea
- Learning
- Personal

Notes are deliberately separated from Captures.

## 11. Relations map

Primary relations:

Life Areas
↕ Goals
↕ Projects
↕ Tasks

Life Areas
↕ Habits

Goals
↕ Projects

Projects
↕ Tasks

Reviews
↔ Goals
↔ Projects
↔ Tasks
↔ Habits

Notes
↔ Life Areas
↔ Projects
↔ Goals

Captures
→ destination during processing

Notion supports one-page relation limits when appropriate, which will be used for fields such as Goal on a Project and Project on a Task where the default relationship should be singular. citeturn0search3

## 12. Rollups

Rollups will be used selectively.

Examples:

Project:
- number of related Tasks;
- completed Tasks;
- progress indicator.

Goal:
- number of related Projects;
- completed Projects;
- progress summary.

Life Area:
- active Goals;
- active Projects.

Avoid excessive rollups because they increase complexity and can create confusing database views.

## 13. Formula policy

Formulas are allowed only where they create visible user value.

Examples:
- overdue indicator;
- completion percentage;
- simple status summary.

No formula should be required for basic use.

Technical identifiers used by formulas should remain stable across language editions.

This is important because Notion formulas can reference database properties directly. citeturn0search13

## 14. Database layouts

Every major database receives a deliberate page layout:

Goals:
- goal title;
- status;
- target;
- progress;
- projects;
- notes.

Projects:
- outcome;
- status;
- dates;
- next action;
- tasks;
- notes.

Tasks:
- task;
- status;
- due;
- priority;
- project;
- notes.

Reviews:
- review metadata;
- guided sections;
- linked context.

Notion layouts can bring important properties forward and hide secondary properties, and the resulting layouts can be viewed on mobile. citeturn0search7

## 15. Mobile views

### Tasks

Today:
Due is today.

Overdue:
Due before today and not Done.

This Week:
Due within current week.

Inbox:
Tasks without project/area where appropriate.

### Projects

Active Projects:
Status = Active.

Waiting:
Status = Waiting.

### Goals

Active Goals:
Status = Active.

### Habits

Active Habits:
Status = Active.

### Reviews

Next Review:
upcoming review.

## 16. Database buttons

Buttons may be used only for low-risk repetitive actions.

Potential V1 buttons:

Task:
- Complete

Capture:
- Mark Processed

Review:
- Start Review

Habit:
- Mark Complete where technically reliable.

Notion database buttons can perform one-click actions, but some button actions are plan-dependent. Therefore no core workflow should depend exclusively on paid button functionality. citeturn0search1

## 17. Home architecture

Home is not a database.

Home contains linked views:

1. Welcome / current date
2. Quick Capture
3. Today Tasks
4. Active Projects
5. Active Goals
6. Habit snapshot
7. Next Review
8. AI Assistant
9. Language Hub
10. Help / Quick Start

Mobile order:

TODAY
→ QUICK CAPTURE
→ KEY ACTIONS
→ GOALS
→ PROJECTS
→ REVIEW

Desktop can expose more navigation, but the information hierarchy remains the same.

## 18. Today architecture

Today is also not a separate database.

It is a focused dashboard built from linked Task and Habit views.

Sections:

- Must Do
- Other Tasks
- Habits
- Notes / Capture
- End of Day

This avoids duplicating task data.

## 19. Capture architecture

Capture should be one prominent button/link.

The user creates a Capture record quickly.

Then:

Process:
1. Identify type.
2. Choose destination.
3. Create/move relevant item.
4. Mark Capture processed.

No requirement to fill every metadata field.

## 20. Review architecture

Review templates should be database templates.

Weekly Review:
- What went well?
- What remains?
- What blocked me?
- Which goals moved?
- Which projects need attention?
- What matters next week?

Monthly:
- achievements;
- unfinished work;
- life-area check;
- lessons;
- next priorities.

Quarterly:
- major outcomes;
- direction;
- goal review;
- life-area balance.

Yearly:
- highlights;
- changes;
- lessons;
- future priorities.

## 21. AI architecture

AI Assistant page contains:

### CORE
Plan My Day
Weekly Review
Goal → Action Plan

### FULL
Project Breakdown
Brain Dump
Monthly Review
Goal Check
Simplify My Week

Each workflow includes:
- What it does;
- What context to provide;
- prompt/instructions;
- expected output;
- human review;
- apply manually.

## 22. Context architecture

AI Context Pack should expose clean summaries rather than raw database complexity.

Suggested context:

CURRENT DATE
ACTIVE GOALS
ACTIVE PROJECTS
TODAY TASKS
OVERDUE TASKS
ACTIVE HABITS
CURRENT REVIEW
USER PRIORITIES

No automatic export to external AI in V1.

## 23. Multilingual architecture

Five editions:

EN
IT
FR
DE
RU

Each edition has:
- same database architecture;
- same property identifiers where formulas require stability;
- localized visible labels;
- localized templates;
- localized sample data;
- localized AI;
- localized Quick Start.

Language Hub:

English
Italiano
Français
Deutsch
Русский

## 24. Sample architecture

Sample workspace includes fictional data:

- 7 Life Areas;
- 3–5 Goals;
- 4–6 Projects;
- 15–25 Tasks;
- 4–6 Habits;
- one Weekly Review;
- one Monthly Review;
- example Notes;
- example Captures.

Enough to demonstrate relationships without becoming overwhelming.

## 25. Blank architecture

Blank workspace:
- no personal sample data;
- default Life Areas may be offered as optional starter records;
- no fake completed history;
- onboarding starts from Language → Life Area → Goal → Project → Task.

## 26. Architecture acceptance gate

Before visual polish:

- all 8 core databases exist;
- relations work;
- one-to-one limits applied where appropriate;
- rollups work;
- formulas work;
- templates work;
- views work;
- mobile views exist;
- no duplicate databases for Today/Home;
- Sample and Blank are separate;
- all five editions share architecture;
- no mandatory paid feature;
- core system works without AI.

## 27. Important design decision

We intentionally reject the common architecture:

HOME
→ 20 databases
→ 50 widgets
→ dozens of formulas
→ multiple integrations.

Instead:

HOME
→ 8 core databases
→ focused views
→ selective relations
→ selective formulas
→ optional AI
→ optional modules.

This is the technical foundation for the product's differentiation.

## 28. Next block

PRODUCT-BUILD-02 — Core Database Build.

Build order:

1. Life Areas
2. Goals
3. Projects
4. Tasks
5. Habits
6. Reviews
7. Captures
8. Notes

Then:
- relations;
- rollups;
- formulas;
- templates;
- views;
- mobile layouts.

## 29. Status

PRODUCT-BUILD-01 — Architecture / Notion System Design: 100%.

Research program remains: 100%.
