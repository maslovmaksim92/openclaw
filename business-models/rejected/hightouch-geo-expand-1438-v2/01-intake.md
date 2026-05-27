---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-hightouch-geo-expand-1438.md
created: 2026-04-20T17:18:00+03:00
---

# Intake

## Контекст resurrection
- Тип: принудительный полный пайплайн для повторной аналитики
- Исходный slug: hightouch-geo-expand-1438
- Основание: сигнал ранее был закрыт как duplicate/supporting и должен пройти заново через P3→P7

## Полный контекст raw-файла

# RESURRECT SIGNAL — hightouch-geo-expand-1438

## Meta
- source: triage/triage-2026-04-17-hightouch-geo-expand-1438-duplicate.md
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
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-hightouch-geo-expand.md`

## Классификация
Дубликат ранее обработанного сигнала.

## Решение
Новый кейс не создан. Сигнал не добавлялся в `pipeline/cases/`, потому что в открытых кейсах новых оснований для обогащения или открытия не найдено.

## Почему это дубликат
- Содержательно это тот же GEO-EXPAND сигнал по Hightouch AI Decisioning: warehouse-native decisioning слой для lifecycle-маркетинга поверх DWH.
- По этому же сигналу уже существует ранее обработанный triage: `pipeline/triage/triage-2026-04-17-hightouch-geo-expand.md`.
- Тезис уже был развёрнут в отдельный кейс `warehouse-native-ai-decisioning-marketing-operator`, который сейчас находится в `pipeline/rejected/` с финальным вердиктом **REJECTED**.

## Почему кейс не переоткрываю
- Во входном файле нет нового факта, который меняет исходную инвестиционную картину относительно уже рассмотренного кейса.
- Основные данные совпадают с ранее зафиксированными: Hightouch, AI Decisioning, ссылка на TechCrunch от 2026-04-15, масштаб $100 млн ARR и тот же локальный wedge для РФ.
- Поскольку это не новый supporting signal для открытого кейса в `pipeline/cases/`, а повтор уже обработанного материала, файл корректно закрыт без создания нового контейнера.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Дубликат ранее обработанного сигнала по warehouse-native AI decisioning для маркетинга. Новый кейс не создан, существующие открытые кейсы не обогащались.
```

