# LIFE-RESEARCH 03 — FEATURE MATRIX + MULTILINGUAL ARCHITECTURE

Дата: 24.09.2026

## 1. Feature matrix — observed competitors

Legend: ✓ clearly advertised/visible; ~ partial or inferred; — not observed.

| Product / source | Dashboard | Daily | Weekly | Monthly | Goals | Habits | Projects | Tasks | Finance | Wellness | Travel | Journal | Reviews | AI | Mobile |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Notion Life Planner 417 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Notion Life Planner 892 | ✓ | ~ | ✓ | ✓ | ~ | ~ | ~ | ✓ | — | — | — | ~ | — | — | ~ |
| Plannuary Life Planner 740 | ✓ | ~ | ✓ | ✓ | ~ | ~ | ~ | ✓ | — | — | — | ~ | — | — | ~ |
| Planora Life Planner 694 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Planora Life Planner 2026 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Grace Digitals Life Planner 14 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ✓ | ~ | ✓ | ~ | — | ~ |
| Chaima Create 2026 Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Diana M Life Planner 219 | ✓ | ~ | ✓ | ✓ | ✓ | ~ | ~ | ✓ | — | — | — | ~ | ~ | — | ~ |
| Heyismail 2026 Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Desbyseb Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Liv Life Planner 986 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ~ | ~ | ~ | — | ~ |
| Etsy 2026 Life Planner / Second Brain | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | ~ |
| Etsy Ultimate Life Planner / Second Brain | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | ~ |
| Etsy French Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ✓ | ~ | ~ | ~ | — | ~ |
| Etsy Coquette Life Planner 2026 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ~ | ✓ | ~ | ~ | — | ~ |
| Creative Market That Girl Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | — | ~ |
| Creative Market All-in-One Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | — | ✓ |
| Creative Market Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ✓ | ~ | — | ~ |
| Gumroad Something Organized Ultimate Life Planner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ |
| Gumroad AI Second Brain | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ~ | ✓ | ✓ | ✓ |
| Notion Second Brain premium systems | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ✓ | ✓ | ~ | ~ |

Sources checked include Notion Marketplace, Etsy, Creative Market and Gumroad listings documented in the research files.

## 2. Multilingual market finding

A current Etsy listing explicitly targets a French Notion life planner. Reviews include French-language feedback praising the template as beautiful and easy to use daily in French.

Source:
https://www.etsy.com/es/listing/1834793903/plantilla-de-planificador-de-vida-notion

This supports treating localization as a product feature rather than an afterthought.

## 3. Notion language constraint

Official Notion documentation currently lists English, French, German and Italian among supported interface languages. Russian is not currently listed.

Source:
https://www.notion.com/help/change-your-language

Therefore we separate:

Layer A — Notion application UI:
controlled by Notion.

Layer B — our product content:
controlled by us and available in:
- English
- Italian
- French
- German
- Russian

## 4. Multilingual technical architecture

We should NOT make V1 depend on a fragile single database whose property names dynamically change with a language selector.

Notion formulas can reference database property names, for example prop("Title"), so changing property names can affect formulas.

Official formula documentation:
https://www.notion.com/help/formula-syntax

A current competitor also warns that changing property names may affect formula functionality:
https://somethingorganized.gumroad.com/l/getlgd

### Recommended architecture

One product with five localized editions sharing the same logic specification:

1. EN — English
2. IT — Italiano
3. FR — Français
4. DE — Deutsch
5. RU — Русский

Each edition gets:
- localized dashboard labels;
- localized onboarding;
- localized page titles;
- localized review prompts;
- localized AI workflow instructions;
- localized Quick Start PDF.

Internal database/formula identifiers remain stable.

## 5. Language Hub

First page:

LANGUAGE / SPRACHE / LANGUE / LINGUA / ЯЗЫК

Options:
- English
- Italiano
- Français
- Deutsch
- Русский

Each option opens its localized Home dashboard.

This is more robust than pretending Notion itself dynamically translates the template.

## 6. Translation QA

Every language edition must pass:
- terminology consistency;
- no missing visible strings;
- no accidental English leftovers;
- formulas unchanged;
- database relations unchanged;
- buttons/links work;
- mobile readability;
- desktop readability;
- onboarding understandable to a first-time user.

## 7. Initial glossary

| English | Italian | French | German | Russian |
|---|---|---|---|---|
| Personal Life Command Center | Centro di Controllo della Vita Personale | Centre de Pilotage de Vie Personnelle | Persönliches Lebens-Cockpit | Личный центр управления жизнью |
| Home | Home | Accueil | Startseite | Главная |
| Today | Oggi | Aujourd’hui | Heute | Сегодня |
| This Week | Questa settimana | Cette semaine | Diese semaine | Эта неделя |
| Goals | Obiettivi | Objectifs | Ziele | Цели |
| Projects | Progetti | Projets | Projekte | Проекты |
| Tasks | Attività | Tâches | Aufgaben | Задачи |
| Habits | Abitudini | Habitudes | Gewohnheiten | Привычки |
| Calendar | Calendario | Calendrier | Kalender | Календарь |
| Life Areas | Aree della vita | Domaines de vie | Lebensbereiche | Сферы жизни |
| Weekly Review | Revisione settimanale | Revue hebdomadaire | Wochenrückblick | Недельный обзор |
| Monthly Review | Revisione mensile | Revue mensuelle | Monatsrückblick | Месячный обзор |
| Yearly Review | Revisione annuale | Revue annuelle | Jahresrückblick | Годовой обзор |
| Quick Capture | Cattura rapida | Capture rapide | Schnellerfassung | Быстрая запись |
| AI Assistant | Assistente IA | Assistant IA | KI-Assistent | AI-ассистент |
| Settings | Impostazioni | Paramètres | Einstellungen | Настройки |

Note: glossary is a first-pass product glossary and will be reviewed by context during content production.

## 8. Mandatory product requirement

The multilingual requirement is now mandatory for the product specification.

V1 must include:
- 5 language editions;
- language hub;
- localized Quick Start;
- localized AI workflows;
- localized review system;
- localized listing copy where supported;
- stable internal identifiers.

## 9. Research conclusion

The emerging differentiation package is:

Simple + ready-to-use + mobile-first + multilingual + strong onboarding + AI workflows + low external dependency.

Multilingual support will be implemented as product architecture, not as machine-translated labels added at the end.

## Status

LIFE-RESEARCH-01: 100%
LIFE-RESEARCH-02: 100%
LIFE-RESEARCH-03: 100%

Next:
LIFE-RESEARCH-04 — Mobile UX comparison and mobile-first specification.
