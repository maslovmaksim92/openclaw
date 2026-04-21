---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1528-msk-hebbia-geo-expand.md
created: 2026-04-20T01:02:37+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/2026-04-19-resurrect-1528-msk-hebbia-geo-expand.md
- Базовый slug: `1528-msk-hebbia-geo-expand`
- Новый slug кейса: `1528-msk-hebbia-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 1528-msk-hebbia-geo-expand

## Meta
- source: triage/triage-2026-04-17-1528-msk-hebbia-geo-expand.md
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
- pipeline/raw/raw-2026-04-17-1528-msk-hebbia-geo-expand.md

## Классификация
новый кейс

## Решение
Создать новый кейс: `investment-banking-ai-analyst-operator`.

## Почему
- В `pipeline/cases/` сейчас нет открытого кейса по AI-аналитику для investment banking, institutional finance и due diligence.
- Сигнал Hebbia описывает не общий AI-поиск, а специализированную платформу для research, VDR, data room, memo, document comparison и сделочных workflow.
- По экономике сигнал проходит порог Program 1: ориентир 5,0-18,0 млн ₽ в год на клиента соответствует примерно 417 000-1 500 000 ₽ в месяц, а верхняя часть диапазона превышает порог 500 000 ₽/мес.
- Для локализации в РФ потребуется тяжёлый сервисный слой: локальные финансовые источники, русскоязычные юридические и финансовые документы, secure deployment и compliance-контур, что делает модель потенциально high-LTV.

## Что создано
- Создан кейс `pipeline/cases/investment-banking-ai-analyst-operator/00-brief.md`.
- В кейсе зафиксированы описание категории, текущее состояние рынка и ключевая гипотеза для РФ.

## Что сделано
- Новый кейс создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это новый кейс, а не шум: Hebbia даёт сильный GEO-EXPAND сигнал в категории AI-native платформ для investment banking, institutional finance и due diligence, с потенциалом high-LTV для РФ.
```

