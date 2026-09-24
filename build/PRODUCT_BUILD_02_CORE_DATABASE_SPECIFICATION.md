# PRODUCT-BUILD-02 — CORE DATABASE BUILD

Дата: 24.09.2026

## Status

PRODUCT-BUILD-02: 100%

Цель:
создать окончательную спецификацию 8 Core Databases до физической сборки Notion workspace.

## 1. LIFE AREAS

### Purpose
Верхний уровень личной системы.

### Required properties

| Property | Type | Required |
|---|---|---|
| Life Area | Title | YES |
| Status | Status | YES |
| Description | Text | NO |
| Goals | Relation → Goals | NO |
| Projects | Relation → Projects | NO |
| Tasks | Relation → Tasks | NO |
| Habits | Relation → Habits | NO |

### Status
- Active
- Paused
- Archived

### Default Sample Areas
- Work
- Personal
- Family
- Health
- Learning
- Finance
- Home

Other remains available.

---

## 2. GOALS

### Purpose
Хранит outcomes, а не действия.

### Properties

| Property | Type | Required |
|---|---|---|
| Goal | Title | YES |
| Life Area | Relation → Life Areas | YES |
| Status | Status | YES |
| Target Date | Date | NO |
| Progress | Number | NO |
| Projects | Relation → Projects | NO |
| Notes | Text/Page | NO |

### Status
- Not Started
- Active
- On Hold
- Completed
- Archived

### Rule
A goal describes a desired outcome.

Example:
GOOD — Launch my portfolio website.
BAD — Write homepage copy.

---

## 3. PROJECTS

### Purpose
Связывает Goal с конкретным результатом.

### Properties

| Property | Type | Required |
|---|---|---|
| Project | Title | YES |
| Goal | Relation → Goals | YES |
| Life Area | Relation → Life Areas | YES |
| Status | Status | YES |
| Start Date | Date | NO |
| Target Date | Date | NO |
| Tasks | Relation → Tasks | NO |
| Next Action | Text | NO |
| Progress | Formula/Rollup | NO |
| Notes | Text/Page | NO |

### Status
- Planning
- Active
- Waiting
- Completed
- Archived

### Rule

Project = result with multiple actions.

---

## 4. TASKS

### Purpose
Execution layer.

### Properties

| Property | Type | Required |
|---|---|---|
| Task | Title | YES |
| Status | Status | YES |
| Due | Date | NO |
| Priority | Select | YES |
| Project | Relation → Projects | NO |
| Goal | Relation → Goals | NO |
| Life Area | Relation → Life Areas | NO |
| Habit | Relation → Habits | NO |
| Notes | Text/Page | NO |
| Created | Created Time | YES |
| Last Edited | Last Edited Time | YES |

### Status
- To Do
- In Progress
- Done
- Cancelled

### Priority
- Low
- Medium
- High

### Mobile default
Only:
Task / Status / Due / Priority / Project.

---

## 5. HABITS

### Purpose
Повторяемые behaviours.

### Properties

| Property | Type | Required |
|---|---|---|
| Habit | Title | YES |
| Life Area | Relation → Life Areas | YES |
| Frequency | Select | YES |
| Status | Status | YES |
| Start Date | Date | NO |
| Target | Number | NO |
| Notes | Text/Page | NO |

### Frequency
- Daily
- Weekdays
- Weekly
- Custom

### Status
- Active
- Paused
- Completed
- Archived

### V1 rule
No complicated streak engine.

---

## 6. REVIEWS

### Purpose
Feedback loop.

### Properties

| Property | Type | Required |
|---|---|---|
| Review | Title | YES |
| Type | Select | YES |
| Period | Date | YES |
| Status | Status | YES |
| Focus | Text | NO |
| Goals | Relation → Goals | NO |
| Projects | Relation → Projects | NO |
| Tasks | Relation → Tasks | NO |
| Habits | Relation → Habits | NO |

### Type
- Weekly
- Monthly
- Quarterly
- Yearly

### Status
- Planned
- In Progress
- Completed

### Templates
Four database templates:

Weekly Review
Monthly Review
Quarterly Review
Yearly Review

---

## 7. CAPTURES

### Purpose
Inbox for fast input.

### Properties

| Property | Type | Required |
|---|---|---|
| Capture | Title | YES |
| Type | Select | YES |
| Created | Created Time | YES |
| Processed | Checkbox | YES |
| Life Area | Relation → Life Areas | NO |
| Destination | Select | NO |
| Notes | Text/Page | NO |

### Type
- Task
- Idea
- Note
- Reminder
- Event
- Other

### Destination
- Task
- Project
- Goal
- Note
- Calendar
- Other

### Rule
Capture is temporary.

Flow:

CAPTURE
→ CLARIFY
→ MOVE
→ PROCESS
→ ARCHIVE

---

## 8. NOTES

### Purpose
Permanent reference information.

### Properties

| Property | Type | Required |
|---|---|---|
| Note | Title | YES |
| Type | Select | YES |
| Life Area | Relation → Life Areas | NO |
| Project | Relation → Projects | NO |
| Goal | Relation → Goals | NO |
| Tags | Multi-select | NO |
| Created | Created Time | YES |
| Updated | Last Edited Time | YES |

### Type
- Reference
- Journal
- Idea
- Learning
- Personal

---

# 9. RELATION RULES

Primary chain:

Life Area
→ Goal
→ Project
→ Task

Secondary:

Life Area
→ Habit

Review
↔ Goal
↔ Project
↔ Task
↔ Habit

Notes
↔ Life Area
↔ Goal
↔ Project

Capture
→ temporary destination.

## 10. SINGLE-RELATION RULE

Where the hierarchy expects one parent:

Project → one Goal.
Project → one Life Area.
Task → one Project where applicable.
Task → one Life Area where applicable.
Habit → one Life Area.

This prevents ambiguous hierarchy.

## 11. MULTI-RELATION RULE

Reviews may relate to multiple:
- Goals;
- Projects;
- Tasks;
- Habits.

Notes may relate to multiple contexts only where genuinely useful.

Avoid unnecessary relations.

# 12. PROPERTY NAMING RULE

Internal technical names should remain stable.

Visible labels can be localized in each language edition.

Do not rename formula-dependent properties casually after formulas are created.

# 13. DATABASE ORDER

The build sequence is:

01 Life Areas
02 Goals
03 Projects
04 Tasks
05 Habits
06 Reviews
07 Captures
08 Notes

Then:
Relations
→ Rollups
→ Formulas
→ Templates
→ Views
→ Layouts.

# 14. INITIAL SAMPLE DATA

Life Areas:
7

Goals:
4

Projects:
5

Tasks:
20

Habits:
5

Reviews:
Weekly + Monthly examples

Captures:
5

Notes:
5

The sample should be large enough to demonstrate relations but small enough to avoid overwhelm.

# 15. BLANK DATA

Blank version contains no fictional history.

It may contain starter Life Areas only if the onboarding explicitly marks them as editable examples.

No fake completed tasks.

# 16. CORE DATA QUALITY RULES

No duplicate primary records.

No orphaned required parent relationships.

No broken relations.

No unnecessary formula dependency.

No required paid Notion feature.

No external API.

No mandatory widget.

# 17. MOBILE DATA RULES

Mobile primary properties:

Tasks:
Task / Status / Due / Priority / Project.

Projects:
Project / Status / Target Date / Goal.

Goals:
Goal / Status / Target Date / Progress.

Habits:
Habit / Frequency / Status.

Reviews:
Review / Type / Period / Status.

Captures:
Capture / Type / Processed.

Notes:
Note / Type / Updated.

Secondary properties stay hidden from primary mobile views.

# 18. BUILD ACCEPTANCE

PRODUCT-BUILD-02 is considered complete when:

- all 8 schemas defined;
- required properties defined;
- statuses defined;
- select options defined;
- relation direction defined;
- sample data defined;
- blank rules defined;
- mobile primary properties defined;
- localization-safe identifiers defined.

All criteria are now complete at specification level.

# 19. IMPORTANT

This block defines the production blueprint.

It does NOT claim that the physical Notion workspace has already been created.

Physical workspace creation is the next implementation step.

# 20. NEXT

PRODUCT-BUILD-03 — Relations / Rollups / Formulas.

Implementation sequence:
1. Create databases.
2. Create relations.
3. Verify relation direction.
4. Add selective rollups.
5. Add minimal formulas.
6. Test with sample data.
7. Test blank version.
8. Save checkpoint.

## Status

PRODUCT-BUILD-02 — 100%.
