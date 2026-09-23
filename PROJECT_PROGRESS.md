# PROJECT PROGRESS

Дата контрольной точки: 24.09.2026

## Все блоки

| Блок | Назначение | Прогресс |
|---|---|---:|
| **A0** | Foundation — GitHub, архитектура, правила, zero-budget policy | **50%** |
| **A1** | Market Research — исследование рынка и конкурентов | **100%** |
| **A2** | Product Selection — выбор и коммерческая валидация первой ниши | **100%** |
| **A3** | Product Architecture — состав и структура продукта | **100%** |
| **A4** | Product Creation — создание материалов продукта | **97%** |
| **A5** | Spreadsheet — Excel/Sheets система | **100%** |
| **A6** | PDF — printable/digital версия | **60%** |
| **A7** | Design — профессиональный визуальный дизайн | **55%** |
| **A8** | Packaging — финальная упаковка | **35%** |
| **A9** | QA — техническая, визуальная и содержательная проверка | **0%** |
| **A10** | Store Setup — настройка канала продаж | **0%** |
| **A11** | Listing — title, description, keywords, previews, FAQ | **0%** |
| **A12** | Publication — фактическая публикация | **0%** |
| **A13** | Market Test — первые реальные данные продаж | **0%** |
| **A14** | Iteration — улучшения на основании данных | **0%** |
| **A15** | Product Factory — масштабирование линейки | **0%** |

## Latest production pass — v2.0

После свежего конкурентного research pass выполнен Dashboard hardening.

### Реально завершено
- Исправлен semantic mismatch: Dashboard Total Income / Total Expenses / Net Cash Flow теперь считаются только за выбранный Month + Year.
- Dashboard subtitle уточнён как месячный обзор.
- Freeze panes применены к ключевым рабочим листам.
- Gridlines скрыты на ключевых рабочих листах.
- Print fit-to-width настройки применены к рабочим листам.
- Полный пересчёт при открытии сохранён.
- LibreOffice round-trip проверка прошла успешно.
- Синтетический январский тест подтвердил Income 3000 / Expenses 1000 / Net Cash Flow 2000 и Budget Housing Actual 1000.

## Новый checkpoint
- production/V2_0_DASHBOARD_HARDENING_CHECKPOINT.md

## Research focus — 24.09.2026

Свежий research подтверждает, что для personal-finance templates полезно оценивать setup ease, feature depth, visual design, customization, mobile usability и value. Современные Excel/Sheets продукты также конкурируют через связанные dashboard, transaction-driven analysis, bills, goals, debt and net worth. citeturn0search0turn0search1turn0search2

## QA rule

A9 остаётся 0% до отдельного полного QA-прохода.

Обязательны:
- четыре языка;
- blank/edge cases;
- formula integrity;
- desktop opening;
- Android Excel test;
- final visual review;
- PDF/package integrity.

## Commercial assumptions

Product: Personal Money Command Center

Markets:
1. USA
2. Canada
3. UK
4. Australia
5. other English-speaking markets later

Price:
- Launch $9.99 USD
- Planned regular $12.99 USD

Channels:
- Payhip Free
- Gumroad
- Etsy later

## Next production sequence

Finish A7 visual refinement → finish A6 final materials → A9 full QA → A8 final package → A10/A11 store preparation → A12 publication.

Intermediate files are not released. Final commercial ZIP will be delivered only after the full production and QA gates are passed.
