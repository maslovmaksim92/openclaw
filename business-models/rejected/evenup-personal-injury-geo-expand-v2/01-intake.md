---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-evenup-personal-injury-geo-expand.md
created: 2026-04-20T12:44:00+03:00
---

# Intake: EvenUp Personal Injury GEO-EXPAND

## Статус
Создан новый resurrect-case для полного повторного прохода пайплайна.

## Контекст из raw
# RESURRECT SIGNAL — evenup-personal-injury-geo-expand

## Meta
- source: triage/triage-2026-04-16-evenup-personal-injury-geo-expand-followup-0927.md
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
2026-04-16

## Входные данные
- `pipeline/raw/raw-2026-04-16-0927-msk-evenup-personal-injury-geo-expand.md`

## Классификация
supporting signal для существующего открытого кейса

## Решение
Новый кейс не открывать.
Обогатить существующий кейс: `pipeline/cases/plaintiff-legal-claims-automation-operator/`.

## Почему
- Сигнал полностью совпадает с уже открытым кейсом по plaintiff-side legal ops, claims automation и personal injury workflow.
- Это не новая категория, а дополнительное подтверждение масштаба рынка, стратегической валидации и высокого LTV в вертикали.
- В raw есть полезные факты для усиления кейса: 2000+ юрфирм-клиентов, около 10 000 кейсов в неделю, оценка выше $2 млрд, участие LexisNexis и отсутствие заметного локального аналога.

## Что добавлено в кейс
- В `pipeline/cases/plaintiff-legal-claims-automation-operator/01-evidence.md` добавлен supporting signal по EvenUp.
- Зафиксирована связка из капитальной валидации, стратегического инвестора LexisNexis и масштабного продуктового penetration в personal injury law.
- Добавлены данные из raw о 2000+ клиентах, 10 000 кейсов в неделю, valuation > $2 млрд и LTV-сигнале `1,2-5,0 млн ₽ в год` для РФ.

## Что сделано
- Существующий кейс обогащён.
- Подготовлен triage-отчёт на русском.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: новый сигнал EvenUp подтверждает, что plaintiff legal claims automation остаётся сильным GEO-EXPAND направлением с высоким чеком, дорогой локализацией и потенциалом repeatable implementation-слоя.

```
