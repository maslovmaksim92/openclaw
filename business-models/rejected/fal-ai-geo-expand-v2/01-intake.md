---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-fal-ai-geo-expand.md
created: 2026-04-20T13:22:21+03:00
---

# Intake

## Режим обработки
Принудительный полный пайплайн по правилу `rerun-/resurrect-`. На этапе intake файл не классифицируется как duplicate.

## Оригинальный источник
- Raw-файл: `2026-04-19-resurrect-fal-ai-geo-expand.md`
- Исторический источник: см. секцию Meta внутри raw-контента ниже.

## Контекст raw-файла

# RESURRECT SIGNAL — fal-ai-geo-expand

## Meta
- source: triage/triage-2026-04-16-fal-ai-geo-expand.md
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
- `pipeline/raw/raw-2026-04-16-0557-msk-fal-ai-geo-expand.md`

## Классификация
шум / не проходит по LTV

## Решение
Не открывать новый кейс.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` по B2B-платформе AI API, serverless GPU-инференсу и unified access к image/video/audio/3D-моделям не найдено.
- Сигнал выглядит содержательным как GEO-EXPAND наблюдение, но не проходит порог Program 1 по экономике: в raw-файле указан `ltv_signal: 1 800 000 ₽ в год`, то есть около `150 000 ₽ в месяц`.
- Требуемый порог для нового кейса составляет `> 500 000 ₽ в месяц`, а зафиксированная оценка заметно ниже. Поэтому кейс пока рано заводить в активный pipeline.
- Дополнительно в raw-файле отмечено, что в России уже есть частичные аналоги по отдельным сценариям, то есть локальное окно не выглядит настолько острым, чтобы компенсировать недостаточный LTV.

## Что сделано
- Создан triage-отчёт на русском языке без открытия нового кейса.
- Исходный raw-файл подлежит переносу в `pipeline/raw/processed/`.

## Вердикт
Сигнал по fal.ai зафиксирован, но на текущем этапе это не high-LTV opportunity по критериям Program 1. Причина отказа: оценочный LTV ниже порога для открытия нового кейса.
```
