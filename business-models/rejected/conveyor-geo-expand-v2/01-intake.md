---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-conveyor-geo-expand.md
created: 2026-04-20T10:27:00+03:00
original_verdict: triage/triage-2026-04-19-conveyor-geo-expand-supporting.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `conveyor-geo-expand-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — conveyor-geo-expand

## Meta
- source: triage/triage-2026-04-19-conveyor-geo-expand-supporting.md
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
2026-04-19

## Входные данные
- `pipeline/raw/raw-2026-04-19-conveyor-geo-expand.md`

## Классификация
поддерживающий сигнал для существующего открытого кейса

## Решение
Существующий кейс обогащён, новый кейс не создавался.

## Совпадающий кейс
- `pipeline/cases/conveyor-customer-trust-workflow/`

## Почему
- Сигнал совпадает по теме, нише и технологии с уже открытым кейсом `Conveyor`: AI-автоматизация security questionnaires, vendor security reviews, trust center workflows и RFP/RFx.
- В raw-файле есть полезные подтверждающие данные о коммерческой тяге и продуктовой зрелости, поэтому сигнал подходит для обогащения существующего кейса.
- Создание нового кейса не требуется, так как тема уже присутствует в `pipeline/cases/`.

## Что добавлено в кейс
- В `pipeline/cases/conveyor-customer-trust-workflow/01-evidence.md` добавлена запись на русском языке.
- Зафиксированы дата, источник, тип сигнала, объяснение, как сигнал усиливает кейс, и ключевые факты.
- Добавлены данные: 400+ клиентов, референс-клиенты уровня Zendesk, Atlassian, Qualtrics, Carta, Netflix и Zapier, автоматизация 90%+ вопросов в security questionnaires, расширение в RFP/RFx automation.

## Что сделано
- Кейс `conveyor-customer-trust-workflow` обогащён.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал обработан как supporting signal для открытого кейса. Кейс обогащён новыми подтверждающими данными.

```

