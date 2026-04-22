---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-patlytics-geo-expand-0927.md
created: 2026-04-21T06:12:41+03:00
---

# 01-intake

## Кейс
patlytics-geo-expand-0927-v2

## Тип intake
resurrect

## rerun_of
patlytics-geo-expand-0927

## Ссылка на оригинальный verdict
triage/triage-2026-04-18-patlytics-geo-expand-0927.md

## Дата intake
2026-04-21, Europe/Moscow

## Полный контекст raw file

# RESURRECT SIGNAL — patlytics-geo-expand-0927

## Meta
- source: triage/triage-2026-04-18-patlytics-geo-expand-0927.md
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
- pipeline/raw/raw-2026-04-18-0927-msk-patlytics-geo-expand.md

## Классификация
дубликат ранее обработанного сигнала, кейс не открываем

## Решение
Не открывать новый кейс и не обогащать существующие кейсы.

## Почему
- Сигнал тематически совпадает с уже обработанными материалами по Patlytics и нише patent AI / IP operations.
- Подходящего открытого кейса в `pipeline/cases/` по этой теме сейчас нет, поэтому это не supporting signal для существующего открытого кейса.
- Хотя верхняя граница нового `ltv_signal` достигает 750 000 ₽ в месяц на одного крупного клиента, диапазон остаётся слишком широким и не даёт уверенного запаса выше порога Program 1 `> 500 000 ₽/мес.`.
- Ранее смежный кейс `enterprise-ai-patent-workflow-operator` уже был отклонён с расчётным LTV 420 000 ₽/мес., и текущий сигнал не добавляет доказательств локального enterprise-спроса в РФ или более сильной сервисной модели.
- Локализация по-прежнему тяжёлая: нужны интеграции с Роспатентом и ЕАПВ, русскоязычные юридические шаблоны и защищённый контур для IP-команд.

## Что сделано
- Новый кейс не создан.
- Существующие открытые кейсы не обновлялись, так как релевантного кейса в `pipeline/cases/` нет.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал усиливает понимание западной тяги Patlytics, но для Program 1 это всё ещё дубликат без достаточного нового апсайда по экономике и локальному спросу. Повторно открывать кейс рано.

```
