---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-patlytics-geo-expand-0655.md
created: 2026-04-21T05:31:04+03:00
---

# 01-intake

## Кейс
patlytics-geo-expand-0655-v2

## Тип intake
resurrect

## rerun_of
patlytics-geo-expand-0655

## Ссылка на оригинальный verdict
triage/triage-2026-04-15-patlytics-geo-expand-0655.md

## Дата intake
2026-04-21, Europe/Moscow

## Полный контекст raw file

# RESURRECT SIGNAL — patlytics-geo-expand-0655

## Meta
- source: triage/triage-2026-04-15-patlytics-geo-expand-0655.md
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
- pipeline/raw/raw-2026-04-15-patlytics-geo-expand.md

## Классификация
дубликат ранее обработанного сигнала, кейс не открываем

## Решение
Не открывать новый кейс и не обогащать существующие кейсы.

## Почему
- Сигнал тематически полностью совпадает с уже обработанными материалами по Patlytics и соседним сигналам в нише patent AI / IP operations.
- Подходящего открытого кейса в `pipeline/cases/` по patent AI, patent intelligence или IP operations по-прежнему нет, поэтому это не supporting signal для существующего кейса.
- В текущем raw-файле `ltv_signal` указан как `6 000 000-15 000 000 ₽ на клиента за 3 года`, то есть примерно 167 000-417 000 руб. в месяц. Это остаётся ниже порога Program 1 `> 500 000 руб./мес.`.
- Несмотря на сильный западный спрос, локализация остаётся нетривиальной: нужны адаптация под практику Роспатента, локальные патентные шаблоны, защищённый контур и русскоязычный юридико-патентный корпус.

## Что сделано
- Новый кейс не создан.
- Существующие кейсы не обновлялись, так как релевантного открытого кейса по теме не найдено.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал усиливает общий тезис о спросе на patent AI, но для Program 1 это всё ещё недостаточно сильный кейс: matching case отсутствует, а заявленный LTV остаётся ниже порога открытия нового кейса.

```
