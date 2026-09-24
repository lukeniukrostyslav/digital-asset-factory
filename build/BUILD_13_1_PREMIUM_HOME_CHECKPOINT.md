# BUILD-13.1 — PREMIUM HOME CHECKPOINT

Date: 2026-09-24

Status: IMPLEMENTED IN NOTION

## Scope
Reworked the Home / Startseite / Accueil / Главная surfaces across EN, IT, DE, FR, RU.

## Product direction
The Home surface is being moved from database/navigation-first toward action-first UX:
- Today / focus is the dominant entry point.
- Quick capture is visible immediately.
- Tasks, Projects and Goals are framed around action and outcomes.
- The core workflow remains: Capture → Clarify → Plan → Execute → Review → Adjust.
- “AI suggests. You decide.” remains the product principle.

## Localization
Five editions updated:
- EN — Home
- IT — Home
- DE — Startseite
- FR — Accueil
- RU — Главная

## Focus task views
Created mobile-friendly list views using the current task data sources:
- EN: view://3e529a2f-45ae-818b-943d-000cae2db6de
- IT: view://3e529a2f-45ae-8107-8783-000c8175b338
- DE: view://3e529a2f-45ae-81bc-9be4-000c68f173c0
- FR: view://3e529a2f-45ae-818e-b0c9-000c848aa048
- RU: view://3e529a2f-45ae-811d-ac4d-000cce0ef95c

## Important QA note
RU currently has a Notion view-rendering/reference anomaly: fetch reports the inline database blocks as “deleted” even though a new list view was successfully created against the current RU Tasks data source. This remains a verification item and is not marked as resolved.

## Next block
BUILD-13.2 — Premium Dashboard / visual hierarchy / action cards / mobile-first presentation.

## Progress
BUILD-13.1: 60%
Overall product release gate remains open until visual QA, RU view verification, E2E QA and final release checks are completed.
