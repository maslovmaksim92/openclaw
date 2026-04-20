---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1927-msk-hebbia-geo-expand.md
created: 2026-04-20T01:02:37+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/2026-04-19-resurrect-1927-msk-hebbia-geo-expand.md
- Базовый slug: `1927-msk-hebbia-geo-expand`
- Новый slug кейса: `1927-msk-hebbia-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 1927-msk-hebbia-geo-expand

## Meta
- source: triage/triage-2026-04-18-1927-msk-hebbia-geo-expand.md
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
2026-04-18

## Входные данные
- pipeline/raw/raw-2026-04-18-1927-msk-hebbia-geo-expand.md

## Классификация
дубликат / supporting signal

## Решение
Обогатить существующий кейс: `enterprise-institutional-intelligence-workflow-platform`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по enterprise institutional intelligence workflow для finance, legal и consulting-команд.
- Новый сигнал Hebbia совпадает по теме, ICP и типу workflow: due diligence, legal review, research и анализ больших массивов документов.
- Сигнал не открывает новую категорию, а усиливает уже зафиксированный тезис о high-LTV платформе для дорогих аналитических команд.

## Что добавлено в кейс
- Обновлён файл `pipeline/cases/enterprise-institutional-intelligence-workflow-platform/01-evidence.md`.
- Добавлен supporting signal с датой 2026-04-18, ссылками на Hebbia, Financial Times и Reuters.
- Зафиксировано, что Hebbia подтверждает спрос на платформенный слой для multi-document analysis, due diligence и совместных аналитических workflow, а также усиливает тезис о высоком чеке за счёт enterprise ICP и требований к secure deployment.

## Что сделано
- Существующий кейс обогащён.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это не новый кейс и не шум. Это supporting signal для уже открытого кейса `enterprise-institutional-intelligence-workflow-platform`, который усиливает доказательную базу по категории и экономике.

```

