---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-superdial-geo-expand.md
created: 2026-04-21T23:04:00+03:00
original_verdict_source: triage/triage-2026-04-14-superdial-geo-expand.md
---

# 01-intake

## Кейс
superdial-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-superdial-geo-expand.md

## Краткий контекст
Standalone GEO-EXPAND-кейс по voice automation для healthcare revenue cycle, звонков в клиники и payer/billing workflows. Исторически сигнал не был открыт как кейс, но resurrect-режим требует новой полной оценки как самостоятельного кандидата.

## Следующий шаг
Передать кейс в P3-demand-validation: заново оценить спрос, LTV, сервисный слой, интеграции и потенциал enterprise-бюджета.

## Полный контекст из raw

# RESURRECT SIGNAL — superdial-geo-expand

## Meta
- source: triage/triage-2026-04-14-superdial-geo-expand.md
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
2026-04-14

## Входные данные
- `pipeline/raw/raw-2026-04-14-superdial-geo-expand.md`

## Классификация
шум / недостаточный LTV для открытия нового кейса

## Решение
Новый кейс не открывать.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие кейсы про ambient clinical documentation и autonomous medical coding находятся рядом по медконтексту, но не покрывают именно AI-автоматизацию телефонных звонков клиник и billing-команд страховщикам как отдельную модель.
- Сигнал по SuperDial сам по себе качественный: компания привлекла $15 млн, заявляет seven-figures revenue, десятки тысяч звонков в неделю и кейс с 10 000+ claim status calls в месяц у клиента West Coast Dental.
- Но по экономике сигнал не проходит порог для нового кейса. В raw-файле указан `ltv_signal: 1 500 000-5 000 000 ₽ в год на клиента`, что соответствует примерно `125 000-416 000 ₽ в месяц` на клиента и остаётся ниже рабочего порога `> 500 000 ₽/мес.`.
- Локализация отмечена как hard, а зрелого российского аналога нет, но без более сильного подтверждения бюджета и enterprise ACV открывать отдельный кейс рано.
- На текущем этапе это скорее полезный рынок-наблюдение по healthcare revenue cycle voice automation, чем доказанный high-LTV service wedge для отдельного case container.

## Что сделано
- Зафиксировано решение не открывать новый кейс на этом сигнале.
- Исходный raw-файл подлежит перемещению в `pipeline/raw/processed/`.

## Что могло бы изменить решение позже
- Появление подтверждённого бюджета уровня `> 500 000 ₽ в месяц` на одного клиента или на типовой контракт.
- Доказательства, что речь идёт не о точечной голосовой автоматизации, а о более широком enterprise revenue cycle workflow с интеграциями, QA, compliance и recurring service layer.
- Повторные сигналы по тому же wedge от других компаний или интеграторов в healthcare billing / payer operations.

## Вердикт
Сигнал интересный, но пока недостаточный для открытия нового кейса: LTV ниже порога, а отдельная high-LTV сервисная модель ещё не подтверждена.

```
