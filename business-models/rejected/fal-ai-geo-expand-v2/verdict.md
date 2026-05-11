---
stage: verdict
updated: 2026-05-11T09:03:00+03:00
verdict: REJECTED
---

# 06-verdict

## Итог

**Вердикт: REJECTED.**

Кейс `fal-ai-geo-expand-v2` закрывается с отказом и должен быть перемещён в `pipeline/rejected/`.

## Почему отказ

### 1. Demand gate уже был отрицательным
В `02-demand.md` зафиксировано, что:
- exact-demand по fal.ai в РФ слабый,
- adjacent спрос есть, но он usage-based и низкоарпушный,
- локальные substitutes уже закрывают базовый API/inference layer,
- repeatable high-ticket GEO-EXPAND motion не собирается.

### 2. Unit economics не проходит даже минимальный profit gate
По `04-economics.md`:
- ARPA: **250 000 ₽/мес**
- Contribution Margin: **28%**
- Fully-loaded CAC: **1 276 667 ₽**
- Churn: **6.0%/мес**
- LTV: **1 166 667 ₽**
- **LTV/CAC = 0.91x**
- **CAC Payback = 18.2 мес**
- Break-even: **около 98 клиентов**
- EBITDA при 50 клиентах: **-3.30 млн ₽/мес**

Это означает прямой **Profit Gate FAIL**:
- LTV/CAC ниже 1:1,
- даже при 50 клиентах EBITDA не достигает +500k/mo.

## Инвестиционный вывод

Это не investable GEO-EXPAND opportunity для фонда.

Даже при попытке перепаковать продукт в managed multimodal API с локальным биллингом и support экономика остаётся слабой:
- acquisition дорогой,
- retention хрупкий,
- gross margin низкая,
- масштаб до безубыточности слишком большой для локального спроса.

## Что могло бы изменить решение

Вернуться к теме можно только если появится один из трёх сильных сигналов:
1. подтверждённые локальные enterprise-контракты с чеком **>500k ₽/мес**,
2. продуктовая обвязка, которая делает решение sticky workflow, а не commodity inference layer,
3. доказанный канал продаж с CAC существенно ниже текущего stress-case без деградации качества клиентов.

До этого момента кейс остаётся **REJECTED**.
