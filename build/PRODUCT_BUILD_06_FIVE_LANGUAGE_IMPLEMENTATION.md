# PRODUCT-BUILD-06 — FIVE-LANGUAGE IMPLEMENTATION

Дата: 24.09.2026

## Status

PRODUCT-BUILD-06: 100%

## 1. Цель

Подготовить единую языковую архитектуру Personal Life Command Center для:

- English
- Italiano
- Français
- Deutsch
- Русский

Главное правило:

ОДНА АРХИТЕКТУРА → ПЯТЬ ЛОКАЛИЗОВАННЫХ ПРЕДСТАВЛЕНИЙ.

Язык не должен создавать пять разных продуктов.

## 2. NOTION LANGUAGE REALITY

Notion официально поддерживает English, French, German и Italian среди языков интерфейса; Russian в текущем списке интерфейсных языков Notion не указан. Поэтому русский edition продукта нельзя строить на предположении, что системный интерфейс Notion станет русским. Локализуем собственные страницы, headings, database labels, onboarding и инструкции. citeturn0search5

На мобильном язык приложения Notion следует языковому приоритету системы пользователя. citeturn0search5

## 3. FIVE EDITIONS

### EN
English

### IT
Italiano

### FR
Français

### DE
Deutsch

### RU
Русский

Каждая edition имеет одинаковые:
- databases;
- relations;
- views;
- formulas;
- templates;
- onboarding logic;
- AI workflows.

Различаются:
- visible labels;
- instructions;
- examples;
- review prompts;
- support text.

## 4. INTERNAL STABILITY

Formula-sensitive properties должны сохранять стабильные внутренние названия.

Не переводить property names, если от их точного имени зависит formula.

Вместо этого:

Internal:
Status
Life Area
Goal
Project
Task
Due
Priority
Progress

Visible/localized presentation:
переводится на уровне пользовательского интерфейса/страницы там, где это безопасно.

Причина: formulas могут ссылаться на properties и relation data. citeturn0search4turn0search1

## 5. CORE GLOSSARY

| EN | IT | FR | DE | RU |
|---|---|---|---|---|
| Personal Life Command Center | Centro di Controllo della Vita Personale | Centre de Pilotage de Vie Personnelle | Persönliches Lebens-Cockpit | Личный центр управления жизнью |
| Home | Home | Accueil | Startseite | Главная |
| Today | Oggi | Aujourd’hui | Heute | Сегодня |
| This Week | Questa settimana | Cette semaine | Diese Woche | Эта неделя |
| Goals | Obiettivi | Objectifs | Ziele | Цели |
| Projects | Progetti | Projets | Projekte | Проекты |
| Tasks | Attività | Tâches | Aufgaben | Задачи |
| Habits | Abitudini | Habitudes | Gewohnheiten | Привычки |
| Calendar | Calendario | Calendrier | Kalender | Календарь |
| Life Areas | Aree della vita | Domaines de vie | Lebensbereiche | Сферы жизни |
| Notes | Note | Notes | Notizen | Заметки |
| Captures | Catture | Captures | Erfassungen | Входящие |
| Reviews | Revisioni | Revues | Rückblicke | Обзоры |
| Weekly Review | Revisione settimanale | Revue hebdomadaire | Wochenrückblick | Недельный обзор |
| Monthly Review | Revisione mensile | Revue mensuelle | Monatsrückblick | Месячный обзор |
| Quarterly Review | Revisione trimestrale | Revue trimestrielle | Quartalsrückblick | Квартальный обзор |
| Yearly Review | Revisione annuale | Revue annuelle | Jahresrückblick | Годовой обзор |
| Quick Capture | Cattura rapida | Capture rapide | Schnellerfassung | Быстрая запись |
| AI Assistant | Assistente IA | Assistant IA | KI-Assistent | AI-ассистент |
| Settings | Impostazioni | Paramètres | Einstellungen | Настройки |
| Start Here | Inizia qui | Commencez ici | Hier starten | Начните здесь |
| Overdue | In ritardo | En retard | Überfällig | Просрочено |
| Active | Attivo | Actif | Aktiv | Активно |
| Completed | Completato | Terminé | Abgeschlossen | Завершено |
| In Progress | In corso | En cours | In Bearbeitung | В работе |
| To Do | Da fare | À faire | Zu erledigen | К выполнению |
| High | Alta | Haute | Hoch | Высокий |
| Medium | Media | Moyenne | Mittel | Средний |
| Low | Bassa | Faible | Niedrig | Низкий |

## 6. STATUS VOCABULARY

Tasks:

To Do / In Progress / Done / Cancelled

IT:
Da fare / In corso / Completata / Annullata

FR:
À faire / En cours / Terminée / Annulée

DE:
Zu erledigen / In Bearbeitung / Erledigt / Abgebrochen

RU:
К выполнению / В работе / Выполнено / Отменено

Goals:

Not Started / Active / On Hold / Completed / Archived

Projects:

Planning / Active / Waiting / Completed / Archived

Habits:

Active / Paused / Completed / Archived

Reviews:

Planned / In Progress / Completed

## 7. ONBOARDING TRANSLATION

### Start Here

EN:
Create one goal, one project and one task.

IT:
Crea un obiettivo, un progetto e un'attività.

FR:
Créez un objectif, un projet et une tâche.

DE:
Erstelle ein Ziel, ein Projekt und eine Aufgabe.

RU:
Создайте одну цель, один проект и одну задачу.

### Core loop

EN:
Capture → Clarify → Plan → Execute → Review → Adjust

IT:
Cattura → Chiarisci → Pianifica → Esegui → Revisiona → Adatta

FR:
Capturer → Clarifier → Planifier → Exécuter → Réviser → Ajuster

DE:
Erfassen → Klären → Planen → Ausführen → Überprüfen → Anpassen

RU:
Зафиксировать → Прояснить → Спланировать → Выполнить → Пересмотреть → Скорректировать

## 8. EMPTY STATES

### Today

EN:
No tasks due today. Add your next action.

IT:
Nessuna attività prevista per oggi. Aggiungi la tua prossima azione.

FR:
Aucune tâche prévue aujourd’hui. Ajoutez votre prochaine action.

DE:
Heute sind keine Aufgaben fällig. Füge deine nächste Aktion hinzu.

RU:
На сегодня задач нет. Добавьте следующее действие.

### Goals

EN:
Create one goal to give your system direction.

IT:
Crea un obiettivo per dare una direzione al tuo sistema.

FR:
Créez un objectif pour donner une direction à votre système.

DE:
Erstelle ein Ziel, um deinem System eine Richtung zu geben.

RU:
Создайте одну цель, чтобы задать системе направление.

### Capture

EN:
Drop anything here. Process it later.

IT:
Salva qui qualsiasi cosa. Elaborala più tardi.

FR:
Déposez tout ici. Traitez-le plus tard.

DE:
Halte hier alles fest. Verarbeite es später.

RU:
Запишите сюда всё, что приходит в голову. Разберите позже.

## 9. REVIEW PROMPTS

Weekly Review core prompts:

EN:
- What moved forward?
- What worked?
- What did not work?
- What matters now?
- What should I stop?
- What should I continue?
- What are my next actions?

IT:
- Cosa è andato avanti?
- Cosa ha funzionato?
- Cosa non ha funzionato?
- Cosa conta adesso?
- Cosa dovrei smettere di fare?
- Cosa dovrei continuare?
- Quali sono le mie prossime azioni?

FR:
- Qu’est-ce qui a avancé ?
- Qu’est-ce qui a fonctionné ?
- Qu’est-ce qui n’a pas fonctionné ?
- Qu’est-ce qui compte maintenant ?
- Que devrais-je arrêter ?
- Que devrais-je continuer ?
- Quelles sont mes prochaines actions ?

DE:
- Was ist vorangekommen?
- Was hat funktioniert?
- Was hat nicht funktioniert?
- Was ist jetzt wichtig?
- Was sollte ich beenden?
- Was sollte ich fortsetzen?
- Was sind meine nächsten Schritte?

RU:
- Что продвинулось вперёд?
- Что сработало?
- Что не сработало?
- Что сейчас действительно важно?
- Что стоит прекратить?
- Что стоит продолжить?
- Какие следующие действия?

## 10. LOCALIZATION STYLE

EN:
clear, concise, neutral.

IT:
natural contemporary Italian; avoid literal English calques.

FR:
natural French; concise and practical.

DE:
clear standard German; avoid unnecessarily bureaucratic language.

RU:
natural modern Russian; avoid machine-translation tone.

## 11. TRANSLATION QA RULE

Every translated label must pass:

1. Meaning preserved.
2. Action remains obvious.
3. Same hierarchy as EN.
4. No accidental change of database logic.
5. No formula property names altered.
6. No truncation in mobile primary views.
7. Consistent terminology across all pages.

## 12. GENDER / FORMALITY

Keep product voice neutral.

French:
use consistent formal/instructional style.

German:
use consistent informal imperative (du) across the product unless marketplace copy requires another voice.

Italian:
use concise neutral instructions.

Russian:
use polite/neutral imperative without excessive formal bureaucracy.

## 13. NUMBERS / DATES

Do not hard-code one date convention into database logic.

Display conventions may follow locale, while the underlying Date property remains native Notion Date.

Examples for user-facing text:

EN:
September 24, 2026

IT:
24 settembre 2026

FR:
24 septembre 2026

DE:
24. September 2026

RU:
24 сентября 2026

## 14. AI PROMPTS

AI workflow architecture remains identical.

Only:
- instruction language;
- examples;
- output language;
- localized field names in user-facing prompt.

AI must not alter core database architecture.

## 15. LANGUAGE HUB

Create a Language Hub page containing:

English
Italiano
Français
Deutsch
Русский

Each edition points to:
- Start Here;
- Quick Start;
- glossary;
- localized support;
- localized review prompts.

## 16. EDITION STRUCTURE

Each language package:

LANGUAGES/
  EN/
  IT/
  FR/
  DE/
  RU/

Each contains:

START-HERE
QUICK-START
GLOSSARY
REVIEWS
AI
HELP

Core data model remains identical.

## 17. LOCALIZATION SAFETY

Do not translate:
- internal IDs;
- formula code;
- relation targets;
- database identifiers required by implementation.

Translate:
- headings;
- instructions;
- visible labels where safe;
- examples;
- help;
- onboarding;
- review prompts;
- AI instructions.

## 18. MOBILE LANGUAGE QA

For each language test:

Home
Today
Capture
Goal
Project
Task
Review
Language Hub

Check:
- no critical truncation;
- action remains obvious;
- long German/French/Russian labels do not destroy layout;
- relation properties remain usable.

## 19. FIVE-LANGUAGE ACCEPTANCE

L1 English complete.
L2 Italian complete.
L3 French complete.
L4 German complete.
L5 Russian complete.
L6 Glossary consistent.
L7 Onboarding translated.
L8 Review prompts translated.
L9 Help translated.
L10 AI user-facing prompts translated.
L11 Formula/relation architecture unchanged.
L12 Mobile labels reviewed.

## 20. IMPORTANT LIMITATION

This block defines the localization system and translation assets at production-specification level.

It does not claim that a physical Notion workspace has been populated with five editions.

## 21. NEXT

PRODUCT-BUILD-07 — AI ASSISTANT HUB.

Workflows:
1. Plan My Day
2. Weekly Review
3. Goal → Action Plan
4. Project Breakdown
5. Brain Dump → Organized Plan
6. Monthly Review
7. Goal Check
8. Simplify My Week

Core rule:
AI suggests. User decides.

## 22. Status

PRODUCT-BUILD-06 — 100%.
