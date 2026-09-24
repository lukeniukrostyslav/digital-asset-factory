# LIFE-RESEARCH-04 — MOBILE UX COMPARISON AND MOBILE-FIRST SPECIFICATION

Дата: 24.09.2026

## 1. Цель

Определить мобильную UX-архитектуру Personal Life Command Center для Android/iOS и исключить типичные проблемы Notion life-planner продуктов: перегрузку, длинные страницы, сложную навигацию, необходимость постоянной настройки и слабую мобильную пригодность.

## 2. Что подтверждено исследованием

### 2.1. Notion официально поддерживает полноценную работу с рабочим пространством на мобильном

В мобильном приложении есть постоянная нижняя навигация: Home, Search, Inbox и создание новой страницы. Вложенные страницы доступны из Home, а для database pages можно переключаться между представлениями базы данных.

Источник: Notion Help — Workspaces on mobile:
https://www.notion.com/help/workspaces-on-mobile

### 2.2. Базы данных должны использовать разные представления вместо одной перегруженной таблицы

Notion поддерживает Table, List, Board, Gallery, Calendar и Timeline views; одна и та же база может иметь несколько представлений с собственными фильтрами и сортировкой.

Источники:
https://www.notion.com/help/category/database-views
https://www.notion.com/help/guides/using-database-views

Следствие для продукта: мобильные экраны не должны пытаться показывать всю базу. Для каждого сценария нужен специализированный view.

### 2.3. Мобильный layout должен быть проектным ограничением с самого начала

Notion позволяет просматривать database layouts на мобильном; часть расширенного layout builder experience ориентирована на desktop/web. Поэтому продукт нельзя сначала проектировать как desktop dashboard, а потом пытаться уменьшить его для телефона.

Источник:
https://www.notion.com/help/layouts

### 2.4. Отзывы покупателей подтверждают ценность простоты и готовой структуры

Life Planner 892: 4.9/5 на 400+ ratings; отзыв отмечает простоту и полноту без чрезмерной сложности.
Life Planner 417: 4.9/5 на 400+ ratings; пользователи отмечают, что всё уже разложено и легко использовать.
Planora Personal Life Planner: 4.8/5 на 37 ratings; отзыв отдельно отмечает, что система не ощущается перегруженной и экономит время на самостоятельную сборку.
Planora Life Planner: 4.9/5 на 82 ratings; при этом начинающий пользователь указывает на некоторую сложность освоения.
Vicky Chris Life Planner: 5.0/5 на 16 ratings; отзывы хвалят интуитивность, но один пользователь называет большой объём функциональности единственным недостатком и отмечает период привыкания.

Источники:
https://www.notion.com/templates/life-planner-892
https://www.notion.com/templates/life-planner-417
https://www.notion.com/templates/personal-life-planner-494
https://www.notion.com/templates/life-planner-694
https://www.notion.com/it/templates/life-planner-by-vicky-chris

## 3. Вывод по мобильной стратегии

Главный принцип:

> MOBILE-FIRST, NOT DESKTOP-SHRUNK.

Пользователь должен уметь выполнить основные действия одной рукой на телефоне без горизонтального скролла и без необходимости открывать desktop.

## 4. Mobile Core — 5 основных входов

Главная мобильная навигация продукта:

1. HOME
2. TODAY
3. CAPTURE
4. GOALS / PROJECTS
5. REVIEWS

Дополнительные функции должны открываться через Home или вторичную навигацию, а не занимать постоянное место.

### HOME

Показывает только самое важное:

- приветствие / текущая дата;
- Today;
- 3–5 ближайших задач;
- активные проекты;
- ключевые цели;
- habit snapshot;
- ближайшее review;
- быстрые действия.

Не показывать на Home всю систему.

### TODAY

Мобильный execution screen:

- сегодняшние задачи;
- overdue;
- scheduled;
- habits;
- quick notes;
- завершение задачи одним действием.

Главная цель: открыть приложение и сразу понять, что делать сейчас.

### CAPTURE

Одно действие:

- новая задача;
- новая заметка;
- идея;
- событие;
- привычка;
- ссылка.

После capture пользователь не должен проходить длинную форму.

### GOALS / PROJECTS

Goals — стратегический уровень.
Projects — конкретные результаты.
Tasks — действия.

На мобильном отображаются карточки/списки, а не широкие таблицы.

### REVIEWS

Отдельный простой вход:

- Weekly Review;
- Monthly Review;
- Quarterly Review;
- Yearly Review.

Каждый review должен быть пошаговым, а не длинной стеной текста.

## 5. Mobile Database Rules

### Rule M1 — No horizontal-scroll dependency

Ключевые мобильные базы не должны требовать горизонтального скролла для понимания основной информации.

### Rule M2 — Card/List first

На телефоне приоритет:

1. List
2. Board/Card
3. Calendar
4. Table только для специальных случаев

### Rule M3 — Minimal visible properties

В основном мобильном view показываются только свойства, необходимые для действия.

Например Task:

- Task name
- Status
- Due
- Priority

Не показывать одновременно все relations, formulas, notes и metadata.

### Rule M4 — One screen = one job

Каждый экран должен отвечать на один вопрос:

- Что мне делать сегодня?
- Что важно на этой неделе?
- Какие цели активны?
- Какие проекты требуют внимания?
- Что нужно пересмотреть?

### Rule M5 — Quick action always visible

На Home и Today должны быть очевидные быстрые действия.

## 6. Mobile page-length rules

Ограничения для V1:

- Home: короткий экран, без длинной ленты;
- Today: максимум несколько основных секций;
- Review: разбить на этапы;
- Goals: список активных целей + прогресс;
- Projects: только активные проекты;
- Notes: быстрый capture + недавние записи.

Длинный справочный контент переносится в Quick Start / Help.

## 7. Mobile onboarding

Первый запуск должен вести пользователя по 5 шагам:

1. Choose language
2. Open Quick Start
3. Set Life Areas
4. Add first Goal
5. Add first Task

После этого пользователь попадает в Today.

Не требовать предварительного ручного заполнения десятков баз.

## 8. Mobile multilingual requirement

Все пять локализованных editions должны иметь одинаковую mobile information architecture:

- English
- Italiano
- Français
- Deutsch
- Русский

Структура и логика идентичны; переводятся интерфейсные labels, onboarding, review prompts, AI instructions и Quick Start.

Внутренние database/property identifiers должны оставаться стабильными там, где это необходимо для формул и связей.

## 9. Что НЕ включать в V1 mobile core

Чтобы избежать fragility:

- сложные внешние widgets;
- обязательные third-party integrations;
- большое количество decorative widgets;
- desktop-only dashboards;
- десятки одновременно открытых databases;
- сложные automations, без которых продукт не работает.

Это соответствует проблемам, выявленным в предыдущем review mining: widgets/integrations могут ломаться, а слишком большая функциональность повышает learning curve.

## 10. Mobile Acceptance Gate

Перед коммерческим релизом:

### Gate M-A — Android

Проверить физически на Android:

- открытие template;
- Home;
- Today;
- Capture;
- Goals;
- Projects;
- Tasks;
- Habits;
- Reviews;
- Language Hub;
- Quick Start;
- AI Assistant Hub.

### Gate M-B — usability

Проверить:

- нет обязательного horizontal scroll;
- основные кнопки/links легко нажимаются;
- пользователь понимает следующий шаг;
- empty state понятен;
- sample data не мешает работе;
- blank version работает;
- navigation возвращает в ожидаемое место.

### Gate M-C — multilingual

Для каждой из 5 editions:

- нет English leftovers;
- labels помещаются в мобильный экран;
- ссылки работают;
- review prompts локализованы;
- AI instructions локализованы;
- Quick Start локализован.

## 11. Итоговая мобильная спецификация

Personal Life Command Center должен восприниматься на телефоне не как большая база Notion, а как простой personal operating system:

HOME → TODAY → ACTION

GOALS → PROJECTS → TASKS

CAPTURE → ORGANIZE → EXECUTE

WEEKLY → MONTHLY → YEARLY REVIEW

Ядро должно быть минимальным; дополнительные life modules подключаются позже.

## 12. Research status

LIFE-RESEARCH-04: 100%

Следующий блок:
LIFE-RESEARCH-05 — Onboarding comparison.

