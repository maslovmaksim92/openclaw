---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-superdial-insurer-calls-geo-expand.md
created: 2026-04-22T00:29:00+03:00
---

# 01-intake

## Кейс
superdial-insurer-calls-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-superdial-insurer-calls-geo-expand.md

## Краткий контекст
SuperDial: AI-автоматизация insurer calls и payer-facing workflows в healthcare revenue cycle. Ранее сигнал трактовался как повторный и ниже порога LTV, но resurrect-режим требует новой полной оценки как отдельного кандидата.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — superdial-insurer-calls-geo-expand

## Meta
- source: triage/triage-2026-04-15-superdial-insurer-calls-geo-expand.md
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
2026-04-15

## Входные данные
- `pipeline/raw/raw-2026-04-15-superdial-insurer-calls-geo-expand.md`

## Классификация
шум / повторный сигнал ниже порога LTV

## Решение
Новый кейс не открывать.

## Почему
- Это ещё один сигнал по той же нише SuperDial, которую уже смотрели ранее: AI-автоматизация телефонных звонков клиник и billing-команд страховщикам в healthcare revenue cycle.
- Подходящего открытого кейса в `pipeline/cases/` по healthcare voice / payer-call automation по-прежнему нет, поэтому обогащать существующий case container нечем.
- Экономика всё ещё не проходит порог для нового кейса. Во входном raw указано `ltv_signal: 900 000-3 600 000 ₽ в год`, а верхняя граница enterprise-контура описана как `5 000 000+ ₽ в год`, что соответствует примерно `75 000-300 000 ₽/мес.` и около `416 000+ ₽/мес.` на верхней границе, то есть всё ещё ниже рабочего порога `> 500 000 ₽/мес.`.
- При этом сигнал полезный как рыночное подтверждение: есть публичные метрики внедрений, заметный объём обработанных звонков и партнёрство с Omega Healthcare. Но этого недостаточно, чтобы открыть отдельный high-LTV кейс.

## Что сделано
- Зафиксировано решение не открывать новый кейс.
- Новый evidence entry в существующие открытые кейсы не добавлялся, потому что подходящий кейс отсутствует.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Что могло бы изменить решение позже
- Подтверждённый бюджет уровня `> 500 000 ₽ в месяц` на одного клиента или типовой enterprise-контур.
- Несколько независимых сигналов по healthcare revenue cycle voice automation с более высоким ACV и явным managed service слоем.
- Появление отдельного открытого кейса по healthcare payer / insurer call automation, если ниша продолжит накапливать сильные сигналы.

## Вердикт
Сигнал полезен для наблюдения за рынком, но пока остаётся ниже порога для нового кейса и не имеет подходящего открытого контейнера для обогащения.

```
