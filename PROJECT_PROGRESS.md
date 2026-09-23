# PROJECT PROGRESS

Дата контрольной точки: 24.09.2026

## Все блоки

| Блок | Назначение | Прогресс |
|---|---|---:|
| **A0** | Foundation — GitHub, архитектура, правила, zero-budget policy | **50%** |
| **A1** | Market Research — исследование рынка и конкурентов | **100%** |
| **A2** | Product Selection — выбор и коммерческая валидация первой ниши | **100%** |
| **A3** | Product Architecture — состав и структура продукта | **100%** |
| **A4** | Product Creation — создание материалов продукта | **95%** |
| **A5** | Spreadsheet — Excel/Sheets система | **99%** |
| **A6** | PDF — printable/digital версия | **60%** |
| **A7** | Design — профессиональный визуальный дизайн | **45%** |
| **A8** | Packaging — финальная упаковка | **35%** |
| **A9** | QA — техническая, визуальная и содержательная проверка | **0%** |
| **A10** | Store Setup — настройка канала продаж | **0%** |
| **A11** | Listing — title, description, keywords, previews, FAQ | **0%** |
| **A12** | Publication — фактическая публикация | **0%** |
| **A13** | Market Test — первые реальные данные продаж | **0%** |
| **A14** | Iteration — улучшения на основании данных | **0%** |
| **A15** | Product Factory — масштабирование линейки | **0%** |

## Latest production pass — v1.7

После дополнительного конкурентного research pass выполнен connected-dashboard refinement.

### Что реально завершено
- Исправлены формулы итогов Transactions: доходы и расходы теперь берутся из Amount по Type.
- Dashboard Debt Balance связан с Debt Tracker.
- Dashboard Savings связан с Savings Goals.
- Dashboard Net Worth рассчитывается как Assets − Liabilities.
- Bills this month и Unpaid bills учитывают выбранные Month + Year.
- В Setup добавлен редактируемый Year.
- Cash Flow теперь автоматически получает месячные Income / Expenses из Transactions по дате и типу.
- Dashboard system insights сохранены.
- Выполнен синтетический тест через LibreOffice с январскими тестовыми данными.

## Новые checkpoints
- research/COMPETITOR_RESEARCH_CHECKPOINT_03.md
- production/A5_A7_V1_7_CONNECTED_DASHBOARD_CHECKPOINT.md

## Конкурентный research — актуальный вывод

Современные продукты категории конкурируют не одной таблицей бюджета, а связанной системой: transactions + budget + bills + savings + debt + net worth + cash flow + dashboard/insights. Отдельно заметны критерии setup ease, feature depth, visual design, customization, mobile usability и value.

Источники research за 24.09.2026:
- FinancialAha comparison
- Tools Without Code personal finance OS
- Tidy Ledgers current Gumroad product
- Tiller Excel finance templates
- Etsy budget spreadsheet marketplace signals

## QA rule

A9 остаётся 0% до отдельного полного QA-прохода. Автоматический расчёт отдельных формул не считается финальной QA.

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

A7 visual refinement → A6 final PDF materials → A9 full QA → A8 final package → A10/A11 store preparation → A12 publication.

Intermediate files are not released to the user. Final commercial ZIP will be delivered only after production and QA are complete.
