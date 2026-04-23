---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-superdial-healthcare-voice-geo-expand.md
created: 2026-04-22T00:29:00+03:00
---

# 01-intake

## Кейс
superdial-healthcare-voice-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-superdial-healthcare-voice-geo-expand.md

## Краткий контекст
SuperDial: healthcare voice automation для звонков в страховые компании и revenue cycle workflows. Ранее сигнал был отклонён на triage как ниже порога LTV, но resurrect-режим требует новой standalone-оценки без duplicate-классификации.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — superdial-healthcare-voice-geo-expand

## Meta
- source: triage/triage-2026-04-15-superdial-healthcare-voice-geo-expand.md
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
- `pipeline/raw/raw-2026-04-15-superdial-healthcare-voice-geo-expand.md`

## Классификация
шум / недостаточный LTV для открытия нового кейса

## Решение
Новый кейс не открывать.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы в healthcare рядом по тематике, но не покрывают именно AI-автоматизацию телефонных звонков клиник и billing-команд страховщикам как отдельную high-LTV сервисную модель.
- Сигнал по SuperDial качественный и подтверждает, что ниша существует: в raw-файле указаны $15 млн финансирования, партнёрство с Omega Healthcare и заметный операционный объём звонков в revenue cycle workflows.
- Но по экономике сигнал всё ещё не проходит порог для нового кейса. Указанный `ltv_signal: 1 500 000-5 000 000 ₽ в год на клиента` соответствует примерно `125 000-416 000 ₽ в месяц` на клиента, то есть остаётся ниже рабочего порога `> 500 000 ₽/мес.`.
- Это также не supporting signal для существующего открытого кейса: релевантного case container по healthcare voice / payer-call automation сейчас нет.
- По сути это повторное подтверждение уже замеченного рынка, но не новый достаточно сильный аргумент для открытия отдельного кейса.

## Что сделано
- Зафиксировано решение не открывать новый кейс.
- Новый evidence entry в существующие открытые кейсы не добавлялся, потому что подходящий кейс отсутствует.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Что могло бы изменить решение позже
- Подтверждённый контрактный бюджет уровня `> 500 000 ₽ в месяц` на одного клиента.
- Несколько независимых сигналов по той же модели с enterprise ACV, интеграциями, compliance и recurring managed service layer.
- Появление отдельного устойчивого wedge по healthcare revenue cycle voice automation, который будет достаточно широким и дорогим для самостоятельного case container.

## Вердикт
Сигнал полезный для наблюдения за рынком, но пока недостаточный для открытия нового кейса: LTV ниже порога, а подходящего открытого кейса для обогащения нет.

```
