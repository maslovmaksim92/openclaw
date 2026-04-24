---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-smart-engines-ai-buhgalteriya-pervichka.md
created: 2026-04-21T20:36:00+03:00
original_verdict_source: triage/triage-2026-04-16-smart-engines-ai-buhgalteriya-pervichka.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — smart-engines-ai-buhgalteriya-pervichka

## Meta
- source: triage/triage-2026-04-16-smart-engines-ai-buhgalteriya-pervichka.md
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
- `pipeline/raw/raw-2026-04-16-1707-msk-smart-engines-ai-buhgalteriya-pervichka.md`

## Классификация
new case

## Решение
Открыть новый кейс `ai-accounting-document-processing-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` по AI-бухгалтерии, обработке первичных документов и автоматизации бухгалтерских/финоперационных workflow не найдено.
- Сигнал не является дублем открытого кейса: он относится к отдельной вертикали бухгалтерской первички, 1С/ERP-интеграций и AI-автоматизации учётного ввода.
- Потенциал LTV проходит порог Program 1: raw-файл описывает enterprise/B2B-сценарий для банков, аутсорсинговых бухгалтерий и крупных компаний, где можно продавать не только распознавание, но и внедрение, интеграцию, exception handling и managed-сопровождение с потенциалом выше `500 000 ₽/мес`.
- Сигнал особенно силён тем, что он локальный: продукт адаптирован под российские документы, подходит для on-premise/закрытых контуров и лучше ложится на требования ИБ и импортозамещения.

## Что сделано
- Создан новый кейс `pipeline/cases/ai-accounting-document-processing-operator/`.
- В `00-brief.md` на русском языке зафиксированы краткое описание, текущее состояние и ключевая гипотеза.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Открыт новый кейс по AI-автоматизации бухгалтерской первички и смежных финопераций. Smart Engines подтверждает, что локальный рынок готов к enterprise-решениям для массового бухгалтерского workflow, а сервисный слой вокруг интеграции и сопровождения даёт реалистичный потенциал high-LTV модели.

```

