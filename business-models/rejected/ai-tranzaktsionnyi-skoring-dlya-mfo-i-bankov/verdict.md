---
stage: verdict
case: ai-tranzaktsionnyi-skoring-dlya-mfo-i-bankov
date: 2026-05-09
analyst: branch-models-lead
verdict: REJECTED
---

[FINTECH] AI транзакционный скоринг для МФО и банков — REJECTED: 41/100 | EBITDA при 50 клиентах остаётся около -1,3 млн ₽/мес | LTV/CAC=4,2x | Сильная сторона: реальная боль и подтверждённый willingness to pay | Стоп-фактор: слишком тяжёлая fixed-cost база и поздний break-even.

# 06-verdict — REJECTED

## Investment one-liner
`[FINTECH] AI транзакционный скоринг для МФО и банков — REJECTED: 41/100 | EBITDA при 50 клиентах остаётся около -1,3 млн ₽/мес | LTV/CAC=4,2x | Сильная сторона: реальная боль и подтверждённый willingness to pay | Стоп-фактор: слишком тяжёлая fixed-cost база и поздний break-even.`

## Решение
**Кейс отклонён на этапе P5 Unit Economics.**

## Почему
1. **Profit Gate FAIL:** при реалистичной модели команда + compliance + integrations компания не достигает **EBITDA > 500 000 ₽/мес даже при 50 клиентах**.
2. **Break-even слишком поздний:** требуется **62-64 активных клиента** и около **95-110 млн ₽** капитала до operating breakeven.
3. **Слишком тяжёлый fixed-cost floor:** steady-state fixed costs около **6,8 млн ₽/мес** до acquisition burn.
4. **Рынок узкий относительно cost base:** чтобы выйти в устойчивость, компании нужно занять слишком большую долю SAM, рассчитанного в `02-demand.md`.
5. **Standalone venture-scale upside слабый:** кейс больше похож на niche infra-vendor или модуль внутри более крупной risk/platform-компании.

## Что в кейсе осталось сильным
- есть реальная боль;
- willingness to pay подтверждён;
- LTV/CAC = **4,2x**;
- CAC payback = **6,6 мес**.

## Но этого недостаточно
На фондовом уровне важна не только эффективность одной сделки, но и способность собрать широкий рынок поверх приемлемого cost base. Здесь именно эта часть и ломается.

## Финальный статус
**REJECTED. Перенести в `pipeline/rejected/`.**