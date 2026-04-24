---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-2216-msk-supio-geo-expand.md
created: 2026-04-20T03:48:00+03:00
---

# 01-intake

## Кейс
2216-msk-supio-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-18-2216-msk-supio-geo-expand.md

## Краткий контекст
Supio: plaintiff-side legal claims automation, разбор меддокументов, chronology и demand preparation для litigation workflow. Ранее сигнал шёл как supporting для существующего кейса, но resurrect-режим требует новой standalone-оценки.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — 2216-msk-supio-geo-expand

## Meta
- source: triage/triage-2026-04-18-2216-msk-supio-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж: Supio GEO-EXPAND

## Дата
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-2216-msk-supio-geo-expand.md`

## Классификация
Поддерживающий сигнал для существующего открытого кейса.

## Совпадающий кейс
- `pipeline/cases/plaintiff-legal-claims-automation-operator/`

## Решение
Новый кейс не создавать. Обогатить существующий кейс через `01-evidence.md`.

## Что добавлено в кейс
В `pipeline/cases/plaintiff-legal-claims-automation-operator/01-evidence.md` добавлен supporting signal по Supio с датой, источниками и кратким объяснением, почему сигнал усиливает кейс. Зафиксированы новые акценты: продукт явно сфокусирован на plaintiff personal injury workflow, есть подтверждение масштаба в 100000+ обработанных кейсов и более $1 млрд settlement value, а также отсутствует быстрый прямой аналог в РФ именно для связки litigation workflow и разбора меддокументов.

## Почему это дубль/поддерживающий сигнал
- Тема полностью совпадает с уже открытым кейсом: automation для plaintiff-side legal claims, medical record review, chronology, demand preparation и litigation workflow.
- Новый raw-файл не открывает новую категорию, а усиливает уже существующую гипотезу дополнительными фактами и более точным позиционированием.

## Что сделано
- Существующий кейс обогащён.
- Новый кейс не создан.
- Raw-файл обработан и подлежит переносу в `pipeline/raw/processed/`.

## Итог
Кейс `plaintiff-legal-claims-automation-operator` обогащён: добавлен supporting signal по Supio с новыми фактами о traction и более точным подтверждением vertical plaintiff litigation wedge.

```