# LIFE-RESEARCH-05 — ONBOARDING COMPARISON

Дата: 24.09.2026

## 1. Цель

Исследовать, как конкурирующие Notion Life Planner продукты вводят нового пользователя в систему, и сформировать onboarding, который минимизирует learning curve.

## 2. Исследованные модели

### Life Planner 2026 — Chaima Create

Notion Marketplace: 4.9/5, 55 ratings. В отзывах отдельно отмечен интерактивный guide перед началом работы. Пользователи также отмечают лёгкую навигацию и понятную организацию.

Источник:
https://www.notion.com/templates/my-personal-life-planner

Вывод:
интерактивное объяснение до начала редактирования снижает неопределённость.

### Ultimate Life Planner — Planora

Notion Marketplace: 4.9/5, 78 ratings. Отзыв нового пользователя прямо отмечает, что dashboard помогает новичку освоиться и является достаточно простым для обучения, несмотря на большое количество страниц.

Источник:
https://www.notion.com/templates/ultimate-life-planner-762

Вывод:
для сложного продукта особенно важен отдельный entry point для новичка.

### Life Planner — Planora

4.9/5, 82 ratings. Пользователь отмечает наличие YouTube links для редактирования формул; другой новый пользователь пишет, что сначала немного разбирается в системе самостоятельно.

Источник:
https://www.notion.com/templates/life-planner-694

Вывод:
внешние tutorial resources помогают, но часть обучения не должна зависеть от YouTube.

### All-in-One Life Planner — NotionWithRo

Описание продукта прямо указывает на встроенный tutorial для beginners и отдельный 5-minute video tutorial для первоначальной настройки iOS.

Источник:
https://notionwithro.gumroad.com/l/life-planner-2024

Вывод:
короткий onboarding tutorial + отдельная mobile setup инструкция — рабочая модель.

### Life Planner 417

4.9/5, 400+ ratings. Отзывы хвалят то, что всё уже разложено и пользователю не нужно самостоятельно строить систему.

Источник:
https://www.notion.com/templates/life-planner-417

Вывод:
onboarding должен не заставлять пользователя проектировать систему, а сразу давать рабочий маршрут.

### Life Planner 892

4.9/5, 400+ ratings. Отзыв подчёркивает простоту и полноту без чрезмерной сложности.

Источник:
https://www.notion.com/templates/life-planner-892

Вывод:
onboarding должен объяснять только необходимое, а не превращаться в отдельный курс Notion.

### Plannuary 740

4.9/5, 100+ ratings. Отзывы отмечают лёгкую навигацию и редактирование; один пользователь называет шаблон простым для первых journaling workflows.

Источник:
https://www.notion.com/templates/life-planner-740

## 3. Главная проблема рынка

У life-planner продуктов есть противоречие:

Больше функций → выше perceived completeness.

Но:

Больше функций → выше learning curve → выше риск, что новичок не начнёт пользоваться системой.

Поэтому Personal Life Command Center должен отделять:

### CORE
то, что пользователь должен понять в первый день.

### OPTIONAL
то, что пользователь может открыть позже.

### ADVANCED
AI, дополнительные modules, глубокие настройки.

## 4. Новый onboarding architecture

### STEP 0 — Language

Первый экран:

**Choose your language**

- English
- Italiano
- Français
- Deutsch
- Русский

После выбора пользователь сразу попадает в соответствующую локализованную Home.

### STEP 1 — Start Here

Короткое объяснение:

> This system helps you organize your life, focus on what matters, and review your progress.

Не объяснять все databases.

Только:
- what it is;
- where to start;
- what Today means;
- как использовать Capture.

### STEP 2 — Set Your Life Areas

Пользователь выбирает/создаёт несколько сфер:

- Work
- Personal
- Family
- Health
- Learning
- Finance
- Home
- Other

Не требовать заполнить всё.

### STEP 3 — Create ONE Goal

Первый goal должен быть один.

Причина: пользователь сразу получает опыт полного цикла:

Goal → Project → Task.

Не просить создать 10 целей.

### STEP 4 — Create ONE Task

Пользователь создаёт одну конкретную задачу.

Например:

Prepare presentation.

Затем она появляется в Today.

### STEP 5 — First Win

После завершения первой задачи показать:

> Your system is ready.

И предложить:

- Add another task
- Create a project
- Start a habit
- Open Weekly Review

## 5. Onboarding Principle: ONE COMPLETE LOOP

Главная механика onboarding:

LANGUAGE
↓
LIFE AREA
↓
ONE GOAL
↓
ONE PROJECT
↓
ONE TASK
↓
TODAY
↓
COMPLETE
↓
REVIEW

Пользователь должен не просто прочитать инструкцию, а выполнить полный цикл системы.

## 6. Three-layer help system

### Layer 1 — Inline hints

Очень короткие подсказки непосредственно рядом с элементом.

### Layer 2 — Quick Start

PDF / Notion guide на 5–10 минут.

Содержит:
- Start Here;
- navigation;
- Goals;
- Projects;
- Tasks;
- Habits;
- Reviews;
- AI Assistant;
- mobile tips.

### Layer 3 — Advanced Guide

Для пользователей, которые хотят настроить систему глубже:

- database customization;
- views;
- formulas;
- relations;
- advanced AI workflows;
- optional modules.

Advanced Guide не должен быть обязательным.

## 7. Sample Workspace

Обязательный компонент.

Пользователь получает:

### SAMPLE

Заполненная демонстрационная жизнь:

- несколько life areas;
- goals;
- projects;
- tasks;
- habits;
- weekly review;
- monthly review;
- AI examples.

Задача Sample — показать, как система выглядит после настройки.

## 8. Blank Workspace

Отдельная чистая версия.

Важно:
Sample и Blank не должны смешиваться.

Пользователь должен понимать:

**Sample = learn**

**Blank = build my own**

## 9. Anti-overwhelm rules

### O1
Не показывать все databases на первом экране.

### O2
Не заставлять пользователя менять цвета, icons, covers и дизайн.

### O3
Не требовать настройки formulas.

### O4
Не требовать widgets.

### O5
Не требовать integrations.

### O6
Не заставлять создавать десятки goals/tasks.

### O7
Не делать 30–60 минут обязательного обучения.

### O8
Первый полезный результат должен быть достигнут быстро.

## 10. Mobile onboarding

На Android/iOS onboarding должен работать без desktop.

Первый пользовательский маршрут:

Language → Start Here → Goal → Task → Today.

Каждый экран должен быть коротким.

Никаких длинных instructional pages перед первым действием.

## 11. Multilingual onboarding

Каждая из пяти editions получает полностью локализованный onboarding:

EN
IT
FR
DE
RU

Переводятся:

- onboarding titles;
- descriptions;
- buttons;
- hints;
- sample content;
- review prompts;
- AI instructions;
- Quick Start;
- advanced help.

Внутренние технические identifiers сохраняются стабильными.

## 12. AI onboarding

AI Assistant нельзя показывать как сложный отдельный продукт.

После базового цикла пользователю предлагаются 3 готовых workflow:

### AI 1 — Plan My Day
На основе задач и целей помогает сформировать порядок действий.

### AI 2 — Weekly Review
Помогает разобрать завершённое, незавершённое и следующие приоритеты.

### AI 3 — Turn Goal Into Actions
Помогает превратить большую цель в несколько конкретных действий.

Пользователь получает готовые prompts/instructions, а не обязан самостоятельно создавать AI workflows.

## 13. Onboarding acceptance gate

Перед релизом проверить:

- новый пользователь понимает, куда нажать;
- язык выбирается сразу;
- Sample можно открыть без настройки;
- Blank можно начать без чтения документации;
- первый Goal создаётся быстро;
- первая Task появляется в Today;
- первый completed action понятен;
- AI workflows находятся после базового onboarding;
- мобильный onboarding работает;
- все 5 языков имеют одинаковую логику;
- нет обязательных внешних integrations.

## 14. Итог

Onboarding Personal Life Command Center должен быть не «инструкцией на 30 страниц», а **первым успешным использованием продукта**.

Формула:

**SHOW → DO → SEE RESULT → EXPAND**

Пользователь сначала делает одно простое действие, получает результат и только потом открывает более глубокие функции.

Это одновременно отвечает двум повторяющимся сигналам из отзывов:
- пользователям нравится готовая, простая структура;
- новым пользователям иногда требуется помощь с освоением Notion и большой функциональностью.

## 15. Status

LIFE-RESEARCH-05: 100%

Следующий блок:
LIFE-RESEARCH-06 — AI workflow comparison.
