---
stage: verdict
case: 2216-msk-supio-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECTED
confidence: high
---

# 06-verdict — Final Decision

sector: GEO-EXPAND
status: REJECTED
score: 0/100

## Investment One-Liner
[GEO-EXPAND] 2216 MSK Supio GEO Expand v2 — REJECTED: 0/100 | LTV/CAC=0,92x | EBITDA при 50 клиентах = +80k ₽/мес, ниже порога | Ключевое преимущество: сильный global category proof | Главный риск: локальный plaintiff-side legal workflow слишком узкий и экономически неинвестируемый.

## Решение
**REJECTED**

## Почему
Кейс не проходит одновременно demand и economics gates.

### 1. Demand
- global category proof сильный;
- локальный спрос не подтверждён;
- ICP в РФ/СНГ узкий и слабо наблюдаемый;
- willingness-to-pay локально не доказан.

### 2. Unit economics
По `04-economics.md`:
- **LTV/CAC = 0.92x**
- **CAC Payback = 18.9 мес**
- **Contribution Margin = 52.0%**
- **Break-even = 50 клиентов / 9.0 млн ₽ MRR**
- **EBITDA при 50 клиентах = +80k ₽/мес**, ниже обязательного порога **500k ₽/мес**

### 3. Главная причина отказа
Продукт слишком жёстко привязан к американскому plaintiff-side personal injury workflow. Для локального рынка это приводит к сочетанию:
- слабого спроса,
- дорогого enterprise sales cycle,
- тяжёлого внедрения,
- высокого churn risk,
- и недостаточного upside даже при агрессивном масштабе.

## Сравнение с историческим решением
Исторически сигнал по Supio был route-to-existing-case/supporting signal. После standalone-переоценки вывод стал жёстче: как самостоятельный geo-expand investment case проект **неинвестируем**.

## Pipeline action
- Статус: **REJECTED**
- Директория должна быть перенесена в `pipeline/rejected/`

## Investment one-liner
Сильная американская legal AI категория, но слабая локальная переносимость и неинвестируемая unit economics для самостоятельного geo-expand запуска.
