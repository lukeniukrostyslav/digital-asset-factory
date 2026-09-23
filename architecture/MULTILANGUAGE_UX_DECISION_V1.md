# MULTILINGUAL UX DECISION V1

## Decision

Personal Money Command Center v1.0 will be built as one multilingual Excel workbook, with English as the default language and a visible language selector.

Initial supported languages:
1. English — default / launch market
2. Spanish
3. Italian
4. Russian

The architecture should allow additional languages later without rebuilding the workbook.

## User experience

A visible selector will appear on the Dashboard:

Language / Idioma / Lingua / Язык
[ English ▼ ]

When the user changes the selection, user-facing interface labels, instructions, dashboard headings and help text should switch to the selected language.

The user's financial data must NOT be translated or modified automatically.

## What is translated

- Dashboard labels
- Worksheet titles where practical
- Instructions
- Input guidance
- Status labels
- Category labels supplied by the template
- Error/input messages where practical
- Quick-start instructions inside the workbook

## What is not translated automatically

- User-entered transaction descriptions
- Creditor names
- Account names
- Personal notes
- User-created free text

## Technical approach

Use a dedicated hidden/protected Translations sheet containing stable keys and language columns.

Example:

| Key | English | Spanish | Italian | Russian |
|---|---|---|---|---|
| dashboard_title | Personal Money Command Center | Centro de Control Financiero Personal | Centro di Controllo Finanziario Personale | Личный финансовый центр |
| income | Income | Ingresos | Entrate | Доходы |
| expenses | Expenses | Gastos | Spese | Расходы |

The Dashboard language selector uses Excel Data Validation. Excel supports in-cell drop-down lists through Data Validation. Formula logic can then return the matching localized text. Microsoft documents both Data Validation lists and the SWITCH function for conditional returns.

## Design rule

Do NOT create four separate copies of the entire workbook.

Preferred architecture:
one workbook + one data model + one translation layer + language selector.

This reduces maintenance and keeps formulas/data consistent across languages.

## Commercial strategy

The launch listing and primary marketing materials remain English-first for the US market.

Multilingual support is an added product capability, not a reason to delay the English launch.

Localized store listings can be prepared separately after the English product is stable.

## QA requirement

Every supported language must pass:
- label visibility check;
- formula integrity check;
- no clipped/truncated text;
- no broken dropdowns;
- no untranslated template labels in the main user interface;
- correct currency/date presentation where supported;
- workbook opens correctly in supported Excel environments.

## Future languages

The translation table is intentionally extensible. Additional languages can be added as new columns without changing the core data model.
