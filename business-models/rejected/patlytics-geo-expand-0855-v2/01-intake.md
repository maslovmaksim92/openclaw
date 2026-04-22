---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-patlytics-geo-expand-0855.md
created: 2026-04-21T05:31:04+03:00
---

# 01-intake

## Кейс
patlytics-geo-expand-0855-v2

## Тип intake
resurrect

## rerun_of
patlytics-geo-expand-0855

## Ссылка на оригинальный verdict
triage/triage-2026-04-15-patlytics-geo-expand-0855.md

## Дата intake
2026-04-21, Europe/Moscow

## Полный контекст raw file

# RESURRECT SIGNAL — patlytics-geo-expand-0855

## Meta
- source: triage/triage-2026-04-15-patlytics-geo-expand-0855.md
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
- pipeline/raw/20260415T052901Z_patlytics_geo_expand.md

## Классификация
supporting signal для существующего кейса

## Решение
Обогатить кейс `enterprise-contract-operations-agents`, новый кейс не создавать.

## Почему
- Сигнал тематически совпадает с уже открытым кейсом по enterprise legal / contract operations и подтверждает движение рынка в сторону более специализированных юридических AI-workflows.
- Patlytics показывает traction в дорогом патентном сегменте: более 40% клиентов из AmLaw 100 и примерно 10x рост выручки за 2025 год.
- Сам по себе raw-сигнал не тянет на отдельный новый кейс Program 1, потому что указанный `ltv_signal` составляет лишь около 600 000-2 500 000 ₽ в год на клиента, то есть ниже порога `> 500 000 ₽/мес.`.

## Что добавлено в кейс
- В `pipeline/cases/enterprise-contract-operations-agents/01-evidence.md` добавлен supporting signal по Patlytics.
- Зафиксированы источник, дата, краткое объяснение, как сигнал усиливает кейс, и ключевые факты: full patent lifecycle, доля клиентов из AmLaw 100, рост выручки примерно в 10 раз за 2025 год, отсутствие прямого локального full-stack AI-аналога и ориентир по LTV.

## Что сделано
- Кейс `enterprise-contract-operations-agents` обогащён.
- Новый кейс не создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен supporting signal о Patlytics как подтверждение спроса на специализированные enterprise legal AI-workflows в дорогих IP/patent-процессах.

```
