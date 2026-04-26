---
stage: final-verdict
case: ai-operator-pervichki-i-nalogovoi-otchetnosti-dlya-msb
date: 2026-04-26
analyst: branch-models-lead
sector: FINTECH
verdict: REJECTED
confidence: medium
---

# 06-verdict — Final Verdict

## Решение
**REJECTED.**

## Почему
Кейс проходит по спросу и даже показывает приемлемый `LTV/CAC = 3,5x`, но не проходит обязательный фондовый Profit Gate:
- **EBITDA при 50 клиентах = -1,55 млн ₽/мес**;
- **break-even = 78 клиентов**;
- delivery остаётся слишком human-review-heavy и implementation-heavy;
- для выхода в fund-grade режим нужен либо ACV заметно выше текущего сценария, либо гораздо более автоматизированный product core.

## Что именно сломало инвест-кейс
1. Слишком тяжёлая полная команда и FOT для ранней стадии.
2. Слишком длинный и дорогой путь `lead -> pilot -> внедрение -> monthly review`.
3. Экономика ближе к AI-enabled accounting firm, чем к software-like asset.
4. До break-even нужно 45-55 млн ₽ капитала, что ухудшает risk/reward на seed-этапе.

## Что могло бы спасти кейс в будущем
- поднять ACV в enterprise / multi-entity сегмент;
- убрать значимую часть ручного бухгалтерского ревью из COGS;
- продавать через партнёрский канал с уже готовой базой 1С/бух-аутсорсеров;
- стандартизировать интеграции и сузить wedge до одного повторяемого workflow.

## Артефакт экономики
См. `04-economics.md`.
