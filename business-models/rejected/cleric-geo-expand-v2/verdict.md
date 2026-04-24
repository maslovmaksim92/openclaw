---
stage: verdict
case: cleric-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: REJECTED
confidence: medium
---

[GEO-EXPAND] Cleric GEO Expand v2 — REJECTED: 57/100 | EBITDA base=н/д | LTV/CAC=1.58x | Ключевое преимущество: реальная enterprise observability-боль | Главный риск: слишком дорогой GTM и недостаточная unit economics для фонда.

# 06-verdict — Investment Verdict

## Итог

**REJECTED.**

## Почему кейс отклонён

1. **LTV/CAC = 1.58x**, это ниже инвестиционного порога **3.0x** и даже ниже комфортной зоны для enterprise B2B.
2. **CAC Payback = 16.5 месяцев**, что слишком долго для нового GEO-EXPAND motion с узким ICP и тяжёлой enterprise-продажей.
3. **Gross Margin = 52.3%**, то есть продукт ближе к high-touch infra/service layer, чем к software-like SaaS.
4. Break-even достигается только примерно на **38 клиентах** и около **M20**, что создаёт слишком большой burn-to-breakeven.
5. Для выхода на break-even реалистично нужен капитал **80+ млн ₽**, а не лёгкий go-to-market эксперимент.
6. Сильный platform risk: Datadog и другие observability incumbents могут встроить похожий investigation layer быстрее, чем отдельный GEO-EXPAND игрок построит локальный канал.

## Что в кейсе было сильным

- Реальная боль существует: incident investigation, MTTR, on-call overload, operational memory.
- Enterprise buyer в принципе может платить высокий чек за снижение downtime.
- На масштабе 50 клиентов EBITDA-модель теоретически положительная.

## Что сломало инвестиционный тезис

- слишком дорогой fully-loaded CAC;
- слишком узкий локальный ICP;
- длинный цикл сделки с пилотом, security review и procurement;
- низкая повторяемость acquisition motion;
- недостаточно высокий LTV относительно CAC.

## Формулировка для фонда

Кейс выглядит как **интересная продуктовая категория, но плохая инвестиционная гео-экспансия для РФ**. Он требует enterprise-heavy продажи, solution engineering и капитала, при этом не даёт фонду достаточно эффективной юнит-экономики.

## Условие для возможного rerun

Имеет смысл вернуться к теме, только если появится одно из трёх:
1. локальный чек устойчиво сместится в диапазон **600-900K ₽/мес**;
2. модель поставки станет существенно более software-like с **GM > 65%**;
3. будут доказаны повторяемые каналы acquisition с **fully-loaded CAC < 3 млн ₽**.

## Финальный статус

**Отклонить и перенести в `pipeline/rejected/`.**
