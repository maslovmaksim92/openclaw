---
stage: verdict
case: smart-engines-ai-buhgalteriya-pervichka-v2
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

[FINTECH] Smart Engines AI бухгалтерия первичка v2 — REJECTED: 58/100 | EBITDA base=-4.72M ₽/мес на 50 клиентах | LTV/CAC=6.0x | Ключевое преимущество: подтверждённая B2B-боль и рабочий retention | Главный риск: fixed cost base и break-even только около 174 клиентов.

# 06-verdict

## Итог
**REJECTED.**

Кейс не проходит Program 5 на уровне фонда.

## Почему отклонён
1. Demand есть, retention выглядит рабочим, и LTV/CAC формально хороший.
2. Но **экономика не выдерживает реалистичный hiring plan и fixed cost base**.
3. При базовом blended pricing **55 000 ₽/клиент/мес** и contribution **38 000 ₽/клиент/мес** компания:
   - выходит в break-even только около **174 клиентов**;
   - достигает **EBITDA +500K/мес** только около **188 клиентов**;
   - на **50 клиентах** остаётся на уровне **-4.72M ₽/мес EBITDA**.
4. По standing order этого достаточно для отклонения, даже если LTV/CAC > 3.

## Что именно ломает инвесткейс
- Низкий ценовой якорь рынка из-за 1С / OCR-alternatives.
- Необходимость тяжёлой команды: backend, ML, integrations, enterprise sales, onboarding.
- Длинный путь до break-even и высокий burn-to-breakeven.
- Слишком капиталоёмкая модель для фонда, если смотреть на blended mid-market сценарий, а не на единичные bank-only сделки.

## Что могло бы спасти кейс
Кейс имел бы шанс на revisit только если подтвердится хотя бы одно из трёх:
1. Реальный **ACV > 1.5M-2.0M ₽ в год** без разрушения win rate.
2. Продажи идут в основном через **OEM / bank / 1С partner channel**, где acquisition cost и onboarding cost радикально ниже.
3. Продукт уходит из OCR-категории в более дорогой слой: AP automation, автопроводки, exception handling, отчётность, managed finance ops.

## Решение по pipeline
- Написать `04-economics.md` и `06-verdict.md`.
- Перенести кейс в `pipeline/rejected/smart-engines-ai-buhgalteriya-pervichka-v2/`.
- Зафиксировать негативный сдвиг в `07-score-trajectory.md`.
