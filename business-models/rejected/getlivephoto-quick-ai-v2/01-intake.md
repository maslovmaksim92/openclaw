---
sector: QUICK-AI
rerun: true
source_raw: 2026-04-19-resurrect-getlivephoto-quick-ai.md
created: 2026-04-20T15:35:00+03:00
original_verdict: triage/triage-2026-04-14-getlivephoto-quick-ai.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — getlivephoto-quick-ai

## Meta
- source: triage/triage-2026-04-14-getlivephoto-quick-ai.md
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
- pipeline/raw/raw-2026-04-14-getlivephoto-quick-ai.md

## Классификация
новый сигнал, новый кейс

## Решение
Создать новый кейс: `animated-photo-on-demand-service`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие кейсы покрывают AI-песни, enterprise-операторов и вертикальные B2B-модели, но не consumer-first сервис оживления фото.
- Сигнал показывает понятный QUICK-AI wedge: одна эмоциогенная услуга, почти нулевое обучение пользователя, получение результата менее чем за минуту и покупка напрямую в Telegram.
- Порог выручки свыше 500 000 ₽/мес выглядит достижимым даже на текущих публичных тарифах: 549 ₽ за пакет 10 оживлений требует около 910 продаж в месяц, а 990 ₽ за пакет 20 оживлений, около 505 продаж в месяц.
- Западный аналог дополнительно усиливает гипотезу: категория photo-to-video и talking-photo уже доказала платёжеспособный спрос и масштаб за пределами локального рынка.

## Что создано
- Создан новый кейс `pipeline/cases/animated-photo-on-demand-service/00-brief.md`.
- В brief зафиксированы гипотеза, сегменты монетизации, западные аналоги и ключевые вопросы для следующего блока валидации.

## Что сделано
- Новый кейс создан.
- Исходный raw-файл обработан и должен быть перемещён в `pipeline/raw/processed/`.

## Вердикт
Сигнал прошёл triage как отдельный QUICK-AI кейс: у модели есть понятная упаковка, импульсный consumer use case, достижимая выручка выше порога и потенциал расширения в B2B/white-label.

```
