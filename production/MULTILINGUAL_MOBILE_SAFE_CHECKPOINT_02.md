# MULTILINGUAL MOBILE-SAFE CHECKPOINT 02

Дата: 24.09.2026

## Что реально выполнено

Создана версия:
Personal_Money_Command_Center_v1.3_MOBILE_SAFE.xlsx

Изменения:
- язык по умолчанию English;
- мобильный Language Selector на Dashboard;
- список языков: English, Русский, Italiano, Español;
- Data Validation использует отдельный диапазон Lists;
- основные пользовательские подписи переведены на четыре языка;
- Dashboard;
- Budget;
- Transactions;
- Debt Tracker;
- Savings Goals;
- Annual Review;
- названия месяцев Annual Review;
- категории Budget.

## Реальная проверка

Для каждого из четырёх языков файл был отдельно сохранён с выбранным языком и пересчитан spreadsheet engine.

Проверенные значения:

English:
- Personal Money Command Center
- Monthly income
- Category
- Transactions Tracker
- Debt
- Goal
- Annual Financial Review

Русский:
- Личный финансовый центр
- Ежемесячный доход
- Категория
- Учёт операций
- Долг
- Цель
- Годовой финансовый обзор

Italiano:
- Centro di Controllo Finanziario Personale
- Entrate mensili
- Categoria
- Registro transazioni
- Debito
- Obiettivo
- Revisione finanziaria annuale

Español:
- Centro de Control Financiero Personal
- Ingresos mensuales
- Categoría
- Control de transacciones
- Deuda
- Objetivo
- Revisión financiera anual

## Ограничение

Автоматизированная проверка подтверждает формулы и пересчёт. Она не может физически нажать элементы управления внутри Excel Android на устройстве пользователя. Финальная device QA будет выполнена в общем QA-проходе.

## Правило

Не считать мобильную совместимость полностью закрытой только на основании автоматического теста. Финальная проверка на Android остаётся частью A9.
