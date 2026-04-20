---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1755-msk-hebbia-geo-expand.md
created: 2026-04-20T01:49:02+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/triage-2026-04-17-1755-msk-hebbia-geo-expand.md
- Базовый slug: `1755-msk-hebbia-geo-expand`
- Новый slug кейса: `1755-msk-hebbia-geo-expand-v2`
- Предыдущее решение: Ранее сигнал был принят как новый кейс `enterprise-institutional-intelligence-workflow-platform`.

## Полный контекст raw

# RESURRECT SIGNAL — 1755-msk-hebbia-geo-expand

## Meta
- source: triage/triage-2026-04-17-1755-msk-hebbia-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-17

## Входные данные
- pipeline/raw/raw-2026-04-17-hebbia-geo-expand.md

## Классификация
новый кейс

## Решение
Создать новый кейс: `enterprise-institutional-intelligence-workflow-platform`.

## Почему
- В `pipeline/cases/` нет открытого кейса по unified institutional intelligence workflow для finance, legal и consulting-команд.
- Сигнал Hebbia шире, чем узкий investment banking use case: он описывает отдельную платформенную категорию для due diligence, covenant review, research, data room и совместных аналитических workflow в high-stakes среде.
- По экономике сигнал проходит порог Program 1: ориентир 2,5-15,0 млн ₽ в год на клиента соответствует примерно 208 000-1 250 000 ₽ в месяц, а верхняя часть диапазона уверенно выше порога 500 000 ₽/мес.
- Несмотря на наличие ранее отклонённого смежного кейса в архиве rejected, этот сигнал достаточно широкий, чтобы открыть новый кейс с более крупным ICP и более устойчивой категорией, охватывающей не только investment banking, но и legal/consulting workflow.

## Что создано
- Создан кейс `pipeline/cases/enterprise-institutional-intelligence-workflow-platform/00-brief.md`.
- Добавлен `pipeline/cases/enterprise-institutional-intelligence-workflow-platform/01-evidence.md` с первичным сигналом и ключевыми фактами.

## Что сделано
- Новый кейс создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это новый кейс, а не шум: Hebbia даёт сильный GEO-EXPAND сигнал в категории enterprise institutional intelligence workflow с потенциально высоким LTV на российском рынке при продаже в банки, крупные юрфирмы и консалтинг.
```

