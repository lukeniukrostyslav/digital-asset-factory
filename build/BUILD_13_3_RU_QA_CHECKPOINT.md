# BUILD-13.3 — RU QA CHECKPOINT

Date: 2026-09-24

## Result
RU task data uses the current secondary Tasks data source:
collection://11a94817-9c61-4e94-8955-86955a8e1889

The legacy RU Upcoming view used the primary Tasks source and therefore did not validate current task appearance.

## Correction
Created a new Upcoming view using the current RU Tasks source:
view://3e529a2f-45ae-81b8-8cd9-000cb97541b6

Configuration:
- filter: Срок >= 2026-09-24
- sort: Срок ascending
- display: Задачи, Срок, Приоритет, Статус

## QA status
RU datasource mismatch is corrected for the new view.
Physical Android rendering is still unverified.
The older legacy view remains and is not treated as current-source QA evidence.

## Progress
BUILD-13.3: 45%
BUILD-13.2: 35%
BUILD-13.1: 60%
