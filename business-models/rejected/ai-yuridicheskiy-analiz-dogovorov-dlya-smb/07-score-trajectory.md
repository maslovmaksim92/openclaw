# 07-score-trajectory

## 2026-04-24 — P4 Demand Validation
- stage: P4
- analyst: branch-models-lead
- status: demand-validated
- score_before: 6.1/10
- score_after: 6.8/10
- change: +0.7
- summary: спрос в РФ подтверждён как workflow-driven, а не AI-hype-driven; WTP подтверждён через hh-вакансии и публичные цены конкурентов. Profit Gate не проходит на дешёвом self-serve, но проходит на team subscription и managed review. Telegram годится как канал, не как moat.
- decision: CONDITIONAL_PASS
- blocking_factors:
  - слабый exact-category search по формулировкам вроде AI contract review / redline
  - риск скатывания в low-margin legal service without repeatable productization
  - нужно отдельно валидировать data residency, error liability и conversion из one-off review в подписку

## 2026-04-24 — P5 Unit Economics
- stage: P5
- analyst: branch-models-lead
- status: economics-modeled
- score_before: 6.8/10
- score_after: 5.4/10
- change: -1.4
- summary: fully-loaded CAC получился 477 тыс. ₽, LTV/CAC = 2,86x, а при 50 клиентах EBITDA остаётся ниже 500 тыс. ₽/мес. Модель требует слишком тяжёлой sales + legal ops нагрузки и не проходит investment-grade порог.
- decision: REJECTED
- blocking_factors:
  - blended CAC слишком высокий для SMB/lower mid-market legaltech
  - break-even только после ~130 клиентов
  - burn-to-breakeven требует 30-35 млн ₽ стартового капитала
  - ручной legal QA съедает маржу и ограничивает операционный рычаг
