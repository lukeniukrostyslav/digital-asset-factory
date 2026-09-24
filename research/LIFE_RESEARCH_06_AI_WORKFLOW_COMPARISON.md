# LIFE-RESEARCH-06 — AI WORKFLOW COMPARISON

Дата: 24.09.2026

## 1. Цель

Исследовать актуальные AI-возможности Notion и AI-oriented life planner products, затем определить AI-архитектуру Personal Life Command Center без обязательной зависимости от платных AI-интеграций.

## 2. Рынок: что уже существует

### 2.1 Notion AI

Notion официально поддерживает AI для создания баз данных, AI Autofill, суммаризации, извлечения action items, категоризации и перевода.

Basic Autofill работает с содержимым конкретной страницы/строки. Более сложный Custom Agent Autofill может использовать workspace search и web search, выполнять многошаговые инструкции и изменять несколько свойств.

Источник:
https://www.notion.com/en-gb/help/autofill

### 2.2 Notion Custom Agents

Актуальная документация Notion показывает переход от простого AI chat к агентным workflows.

Custom Agents могут:
- читать страницы и базы;
- работать по recurring schedules;
- запускаться при событиях;
- обновлять записи;
- выполнять многошаговые workflows;
- использовать workspace context;
- при разрешении использовать web search.

При этом создание/редактирование Custom Agents требует Business или Enterprise plan.

Источник:
https://www.notion.com/help/custom-agents

### 2.3 Life AI как конкурентный паттерн

В Notion Marketplace уже существует Life AI agent для Life Planner OS.

Он позиционируется как AI, знающий структуру life system, и умеет:
- создавать tasks/action items;
- категоризировать;
- агрегировать информацию;
- строить routines;
- превращать goals в milestones;
- поддерживать journal workflows;
- работать с wishlist и aspirations.

Источник:
https://www.notion.com/custom-agent-templates/life-os

Это важный конкурентный сигнал: покупателю уже предлагается идея AI, который не просто отвечает на вопросы, а действует внутри life-management system.

## 3. Основной вывод

Нельзя делать продукт просто как:

> Notion template + 100 AI prompts.

Такой продукт легко копируется и не создаёт сильной связи между AI и системой.

Наша модель:

> LIFE SYSTEM + CONTEXT + WORKFLOW + AI

AI должен работать поверх уже организованных Goals, Projects, Tasks, Habits и Reviews.

## 4. AI Assistant Hub

Создаётся отдельный раздел:

# AI ASSISTANT

Он содержит готовые workflows.

### CORE 01 — Plan My Day

Вход:
- today's tasks;
- overdue tasks;
- active goals;
- projects;
- optional energy/time constraints.

Выход:
- suggested order;
- 3 most important actions;
- tasks that can be postponed;
- short focus plan.

Важно: AI предлагает план, но пользователь принимает решение.

### CORE 02 — Weekly Review

Вход:
- completed tasks;
- unfinished tasks;
- active projects;
- goals;
- habits;
- notes.

Выход:
- wins;
- unfinished items;
- blockers;
- patterns;
- next-week focus;
- questions for reflection.

### CORE 03 — Goal → Action Plan

Вход:
- goal;
- deadline;
- context;
- available time.

Выход:
- milestones;
- projects;
- first actions;
- possible risks.

### CORE 04 — Project Breakdown

Вход:
- project description.

Выход:
- outcome;
- milestones;
- tasks;
- dependencies;
- next action.

### CORE 05 — Brain Dump → Organized Plan

Пользователь вставляет свободный текст.

AI классифицирует:
- tasks;
- ideas;
- notes;
- projects;
- goals;
- reminders.

После этого пользователь вручную подтверждает, что куда относится.

### CORE 06 — Monthly Review

Вход:
- month tasks;
- projects;
- goals;
- habits;
- notes.

Выход:
- achievements;
- unfinished work;
- lessons;
- priorities;
- next-month focus.

### CORE 07 — Goal Check

AI анализирует:
- цель;
- текущий прогресс;
- последние actions.

Выход:
- what moved forward;
- what stalled;
- next concrete action;
- possible adjustment.

### CORE 08 — Simplify My Week

AI ищет:
- слишком много active tasks;
- duplicate work;
- low-value tasks;
- overloaded days.

Выход:
- candidates to defer;
- candidates to remove;
- grouping suggestions.

Это не автоматическое удаление.

## 5. AI Safety / Human Control

AI не должен самостоятельно принимать важные решения.

Правило:

> AI suggests. User decides.

AI не должен:
- удалять задачи без подтверждения;
- менять цели без подтверждения;
- утверждать медицинские/финансовые решения;
- обещать результаты;
- выдавать предположение как факт;
- автоматически перестраивать всю систему без user approval.

## 6. AI workflow UX

Каждый workflow имеет одинаковую структуру:

### WHAT IT DOES
Короткое объяснение.

### INPUT
Что AI использует.

### RUN
Готовая инструкция / prompt.

### REVIEW
Пользователь проверяет результат.

### APPLY
Пользователь вручную применяет изменения.

Так AI остаётся полезным даже без автоматизации.

## 7. V1: no mandatory AI subscription

Ключевое коммерческое решение:

Продукт не должен переставать работать, если у пользователя нет платного Notion AI.

Основная версия должна работать как обычный Notion system.

AI Hub предоставляет:
- готовые prompts;
- structured instructions;
- context templates;
- copy/paste workflows;
- инструкции для ChatGPT / Claude / Gemini / Notion AI, где применимо.

Таким образом, AI является усилителем, а не единственной точкой ценности.

## 8. AI Context Pack

Чтобы AI давал более качественные ответы, продукт должен иметь стандартный Context Pack.

Он включает:

- Life Areas;
- active Goals;
- Projects;
- Tasks;
- Habits;
- current Review;
- user priorities.

Пользователь может скопировать relevant context в AI.

В будущем возможно автоматическое подключение к Notion AI/Agents.

## 9. AI Prompt Architecture

Каждый prompt должен содержать:

1. ROLE
2. CONTEXT
3. INPUT
4. TASK
5. CONSTRAINTS
6. OUTPUT FORMAT
7. HUMAN REVIEW

Пример:

ROLE:
You are my personal planning assistant.

CONTEXT:
Use only the information I provide.

TASK:
Turn my goal into a realistic action plan.

CONSTRAINTS:
Do not invent deadlines or commitments.

OUTPUT:
Goal → milestones → projects → next actions.

HUMAN REVIEW:
Ask me to confirm before I change my system.

## 10. Multilingual AI

AI Hub должен иметь пять локализованных editions:

- English
- Italiano
- Français
- Deutsch
- Русский

Переводятся:
- workflow names;
- instructions;
- prompt templates;
- output formats;
- review prompts;
- onboarding.

При этом пользователю можно разрешить получить AI output на выбранном языке.

## 11. AI workflow tiers

### FREE / CORE

3 workflows:
- Plan My Day
- Weekly Review
- Goal → Action Plan

### STANDARD

Все CORE +:
- Project Breakdown
- Brain Dump
- Monthly Review
- Goal Check
- Simplify My Week

### PREMIUM / FUTURE

Возможные advanced workflows:
- recurring review automation;
- deeper cross-database analysis;
- web research;
- calendar-aware planning;
- automatic classification;
- custom agents.

Эти advanced features не должны быть обязательными для V1.

## 12. Competitive differentiation

Конкурентный AI Life AI показывает, что рынок уже движется к agentic life management.

Наше отличие должно быть не в заявлении «у нас тоже есть AI».

Отличие:

1. AI встроен в конкретный life-management workflow.
2. Каждый AI workflow имеет human approval.
3. Система работает и без платного AI.
4. Пять локализованных editions.
5. Mobile-first.
6. Sample + Blank.
7. Quick Start.
8. AI workflows связаны с Goals → Projects → Tasks → Reviews.
9. Один набор workflow работает через разные AI-платформы.

## 13. Что НЕ делать в V1

Не включать как обязательную часть:
- autonomous agent;
- automatic deletion;
- automatic goal rewriting;
- mandatory web browsing;
- mandatory calendar integration;
- mandatory external API;
- complex automations;
- promises of productivity outcomes.

Это уменьшает техническую хрупкость и делает продукт независимее от изменений AI-платформ.

## 14. AI acceptance gate

Перед релизом проверить каждый workflow:

- prompt понятен;
- input определён;
- output format определён;
- AI не должен выдумывать данные;
- human review присутствует;
- английская версия работает;
- IT/FR/DE/RU локализации присутствуют;
- workflow понятен на mobile;
- workflow можно использовать без paid automation;
- инструкции не зависят от одного AI provider.

## 15. Итоговая AI-модель

Personal Life Command Center должен продавать не «набор промптов».

Он должен продавать:

> **A structured personal system that AI can understand and help operate.**

Формула:

SYSTEM
+
CONTEXT
+
WORKFLOW
+
AI
+
HUMAN CONTROL

## 16. Research status

LIFE-RESEARCH-06: 100%

Следующий блок:
LIFE-RESEARCH-07 — Pricing / Offer Architecture.
