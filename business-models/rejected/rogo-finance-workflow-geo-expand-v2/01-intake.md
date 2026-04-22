---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-rogo-finance-workflow-geo-expand.md
created: 2026-04-21T14:16:00+03:00
---

# Intake

## Контекст resurrection
- Тип: принудительный полный пайплайн для повторной аналитики
- Исходный slug: rogo-finance-workflow-geo-expand
- Основание: сигнал ранее не прошёл полный цикл или был маршрутизирован как duplicate/supporting, поэтому должен пройти заново через P3→P7
- Оригинальный triage/verdict: см. блок `Meta.source` внутри полного контекста ниже

## Полный контекст raw-файла

# RESURRECT SIGNAL — rogo-finance-workflow-geo-expand

## Meta
- source: triage/triage-2026-04-15-rogo-finance-workflow-geo-expand.md
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
- `pipeline/raw/raw-2026-04-15-rogo-finance-workflow-geo-expand.md`

## Классификация
supporting signal для существующего кейса

## Matching case
- `pipeline/cases/investment-banking-ai-analyst-operator/`

## Решение
Новый кейс не создавать. Обогатить существующий кейс `investment-banking-ai-analyst-operator`.

## Что добавлено в кейс
В `pipeline/cases/investment-banking-ai-analyst-operator/01-evidence.md` добавлена новая запись на русском языке.

Что именно добавлено:
- дата сигнала: 2026-04-15;
- источник: `https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion`;
- тип: supporting signal;
- краткое объяснение, что сигнал усиливает кейс через подтверждение международной экспансии и enterprise traction;
- ключевые факты: Series C на $75 млн, выход в Европу, 25 000+ ежедневных пользователей из числа bankers and investors, ориентир LTV для РФ 2,5-12,0 млн руб. в год на клиента.

## Почему это supporting signal
Сигнал тематически совпадает с уже открытым кейсом по AI-аналитику для investment banking, PE и corporate finance команд. Он не открывает новую нишу, а усиливает уже существующую гипотезу дополнительным подтверждением спроса, масштаба и географической переносимости модели.

## Что сделано
- Существующий кейс обогащён.
- Raw-файл должен быть перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс усилен: это не новый кейс, а обогащение существующего направления `investment-banking-ai-analyst-operator`.

```

