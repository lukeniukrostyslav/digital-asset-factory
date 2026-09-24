# PRODUCT-BUILD-07 — AI ASSISTANT HUB

Дата: 24.09.2026

## Status

PRODUCT-BUILD-07: 100%

## 1. Цель

Создать AI Assistant Hub как необязательный слой поверх Personal Life Command Center.

AI не заменяет пользователя и не становится обязательным компонентом системы.

Главное правило:

AI SUGGESTS → HUMAN DECIDES.

## 2. CURRENT NOTION AI CAPABILITY CHECK

Актуальная документация Notion подтверждает, что Notion Agent может работать с содержимым workspace, отвечать на вопросы и выполнять разовые задачи. citeturn0search5

Custom Agents предназначены для более специализированных workflows и могут читать предоставленные им pages/databases, запускаться по событиям и расписанию и выполнять действия. Их создание требует Business или Enterprise. citeturn0search0

Custom Agents используют Notion credits, причём расход зависит от объёма прочитанного контента, количества действий и частоты запусков. citeturn0search10

Следствие для продукта:
V1 AI workflows должны работать как prompts/instructions и не зависеть от Custom Agents.

## 3. AI HUB STRUCTURE

AI Assistant Hub содержит:

1. Plan My Day
2. Weekly Review
3. Goal → Action Plan
4. Project Breakdown
5. Brain Dump → Organized Plan
6. Monthly Review
7. Goal Check
8. Simplify My Week

Дополнительно:
- AI Context Pack
- AI Safety / Human Review
- Prompt Library
- AI Help

## 4. AI CONTEXT PACK

Purpose:
дать AI структурированный контекст без необходимости копировать весь workspace вручную.

Context Pack sections:

### Life Areas
Active Life Areas.

### Goals
Active Goals:
Goal / Status / Progress / Target Date / Life Area.

### Projects
Active Projects:
Project / Status / Goal / Life Area / Next Action / Target Date / Progress.

### Tasks
Open Tasks:
Task / Status / Due / Priority / Project.

### Habits
Active Habits:
Habit / Frequency / Status / Life Area.

### Current Review
Latest relevant Weekly/Monthly Review.

### Current Focus
User manually states:
- current priority;
- constraints;
- important deadlines;
- things to avoid.

## 5. CONTEXT SAFETY

AI should not receive unnecessary information.

Context principle:

MINIMUM USEFUL CONTEXT.

Do not automatically expose:
- unrelated Notes;
- archived records;
- unnecessary personal history;
- external apps;
- private databases not needed for the workflow.

Notion Custom Agents use explicitly granted access to pages/databases and connected tools, which supports a least-privilege design. citeturn0search0turn0search8

## 6. STANDARD PROMPT ARCHITECTURE

Every workflow uses:

ROLE
CONTEXT
INPUT
TASK
CONSTRAINTS
OUTPUT FORMAT
HUMAN REVIEW

This structure is consistent across all five language editions.

## 7. WORKFLOW 1 — PLAN MY DAY

### Goal

Turn current tasks and priorities into a realistic daily plan.

### Context

- open tasks;
- due dates;
- priorities;
- active projects;
- today's constraints.

### Task

Suggest:
1. Must do
2. Should do
3. Could do
4. One thing to remove/defer

### Constraints

- do not invent deadlines;
- do not create obligations;
- do not assume available time;
- flag conflicts;
- keep plan realistic.

### Output

Morning plan:
- Top 1
- Top 3
- Optional
- Defer / Remove
- Questions for user

Human review:
user chooses final plan.

## 8. WORKFLOW 2 — WEEKLY REVIEW

### Goal

Turn the weekly review into decisions.

### Input

Current Weekly Review + completed/open tasks + active projects/goals.

### Output

- Wins
- Stalled items
- Important unfinished items
- Things to stop
- Things to continue
- Proposed next actions
- Questions needing user decision

AI must not mark Goals or Projects completed automatically.

## 9. WORKFLOW 3 — GOAL → ACTION PLAN

### Goal

Turn one goal into a practical sequence.

### Input

Goal:
definition
target date
Life Area
constraints.

### Output

- success definition;
- milestones;
- candidate projects;
- candidate next actions;
- risks;
- assumptions.

AI does not create final commitments automatically.

## 10. WORKFLOW 4 — PROJECT BREAKDOWN

### Goal

Break a project into actionable tasks.

### Input

Project:
Goal
Target Date
Next Action
constraints.

### Output

- project outcome;
- milestones;
- task candidates;
- dependencies;
- first next action;
- possible blockers.

Rule:
tasks must be concrete actions.

## 11. WORKFLOW 5 — BRAIN DUMP → ORGANIZED PLAN

### Goal

Turn unstructured thoughts into categories.

### Input

User brain dump.

### Output

Sections:

Tasks
Projects
Ideas
Notes
Questions
Decisions
Someday / Later

For each task candidate:
suggest destination and next action.

AI must not silently delete information.

## 12. WORKFLOW 6 — MONTHLY REVIEW

### Goal

Identify patterns across the month.

### Input

Monthly Review + Goals + Projects + Tasks + Habits.

### Output

- progress;
- unfinished work;
- repeated friction;
- areas needing attention;
- possible simplifications;
- candidate priorities for next month.

No predictive claims.

## 13. WORKFLOW 7 — GOAL CHECK

### Goal

Challenge a goal constructively.

### Input

Goal + progress + projects + recent review.

### Output

- what supports the goal;
- what does not;
- missing information;
- possible obstacles;
- questions;
- possible next action.

AI should not decide whether the goal is "worth it."

User decides.

## 14. WORKFLOW 8 — SIMPLIFY MY WEEK

### Goal

Reduce unnecessary workload.

### Input

Open tasks + projects + commitments entered by user.

### Output

Classify:

KEEP
DEFER
DELEGATE
DELETE
CLARIFY

Every DELETE/DEFER suggestion must include the reason.

No automatic deletion.

## 15. AI SAFETY RULES

AI must:

- distinguish facts from suggestions;
- identify assumptions;
- ask when essential information is missing;
- avoid invented deadlines;
- avoid invented commitments;
- avoid pretending to know the user's priorities;
- avoid making irreversible changes;
- preserve original user data;
- request human confirmation before consequential actions.

## 16. AI OUTPUT STYLE

Output should be:

Short
Structured
Actionable
Specific
Non-judgmental

Avoid:
- motivational filler;
- long essays;
- generic productivity advice;
- false certainty.

## 17. FIVE-LANGUAGE AI

Every workflow exists in:

EN
IT
FR
DE
RU

The workflow architecture stays identical.

Localized:
- role;
- instructions;
- output headings;
- examples;
- help text.

The user can request output in another language without changing database architecture.

## 18. AI CONTEXT TEMPLATE

Standard context block:

CURRENT DATE:
CURRENT FOCUS:
LIFE AREAS:
GOALS:
PROJECTS:
OPEN TASKS:
HABITS:
LATEST REVIEW:
CONSTRAINTS:

The user may omit any section.

AI must not infer missing sections as facts.

## 19. HUMAN REVIEW GATE

Every AI workflow ends with:

REVIEW BEFORE ACTION

The user verifies:
- facts;
- dates;
- priorities;
- assumptions;
- suggested actions.

Only then should the user update Notion.

## 20. AUTOMATION POLICY

V1:
manual prompts first.

Optional future:
Notion Custom Agents.

Custom Agents can run on schedules/events and act on authorized workspace data, but they require Business or Enterprise and consume credits. citeturn0search0turn0search10

Therefore:
the commercial core product must not require Custom Agents.

## 21. EXTERNAL AI POLICY

The product may provide copy-ready prompts for:
- Notion AI;
- ChatGPT;
- other compatible AI assistants.

The template itself does not require an external API.

This preserves low-friction setup and avoids mandatory third-party credentials.

## 22. PRIVACY GUIDANCE

AI Help page must tell users:

- share only information they are comfortable processing with their chosen AI;
- avoid unnecessary sensitive personal information;
- review AI outputs before acting.

Notion states that information used by Notion AI is shared with AI subprocessors to provide the AI features and describes its data-training policy and security practices in its official documentation. citeturn0search4turn0search6

Product copy must not promise absolute privacy beyond the policies of the selected AI service.

## 23. AI QUALITY TESTS

AI1:
Plan My Day does not invent deadlines.

AI2:
Weekly Review distinguishes completed from open work.

AI3:
Goal → Action Plan preserves the original goal.

AI4:
Project Breakdown creates concrete actions.

AI5:
Brain Dump preserves all input categories.

AI6:
Monthly Review does not invent trends.

AI7:
Goal Check presents questions rather than deciding for user.

AI8:
Simplify My Week does not delete anything automatically.

AI9:
All workflows work without paid Custom Agents.

AI10:
Five-language versions preserve identical logic.

## 24. COMMERCIAL POSITIONING

Do not market this as an autonomous life manager.

Correct positioning:

"Optional AI workflows that help you plan, organize and review your life system."

AI is an assistant layer, not the product's foundation.

## 25. ACCEPTANCE

PRODUCT-BUILD-07 is complete at architecture/prompt specification level.

It does not claim physical Custom Agents have been created.

The product remains functional without Notion AI or Custom Agents.

## 26. NEXT

PRODUCT-BUILD-08 — SAMPLE / BLANK WORKSPACES.

Build:
- fictional Sample;
- clean Blank;
- repeatable database templates;
- sample data consistency;
- reset/duplication rules;
- five-language sample strategy;
- sample-to-blank transition.

## 27. Status

PRODUCT-BUILD-07 — 100%.
