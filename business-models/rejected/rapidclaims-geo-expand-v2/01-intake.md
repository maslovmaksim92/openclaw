---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-rapidclaims-geo-expand.md
created: 2026-04-21T15:56:07+03:00
original_verdict_source: triage/triage-2026-04-15-rapidclaims-geo-expand.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — rapidclaims-geo-expand

## Meta
- source: triage/triage-2026-04-15-rapidclaims-geo-expand.md
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
- `pipeline/raw/raw-2026-04-15-rapidclaims-geo-expand.md`

## Классификация
новый кейс

## Решение
Открыть новый кейс: `autonomous-medical-coding-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено.
- Сигнал по RapidClaims не выглядит шумом: в raw зафиксированы продуктовая специализация на autonomous medical coding и revenue cycle automation, обработка миллионов medical charts, 98% audited accuracy, до 80% снижения coding cost, сокращение AR days на 30% и рост clean claim rate до 99%.
- Это уже не одиночный западный пример. RapidClaims выступает дополнительным подтверждением той же категории рядом с более ранним сигналом по CodaMetrix, значит ниша начинает выглядеть как самостоятельная repeatable-модель.
- По экономике сигнал проходит порог Program 1 по high-LTV потенциалу: `ltv_signal` указан как 2,5-12 млн руб. в год на крупного клиента, то есть примерно 208 000-1 000 000 руб. в месяц. Нижняя часть диапазона пограничная, но верхняя часть уверенно выше порога `>500 000 руб./мес.`.
- Локализация трудная, но именно это повышает сервисную ценность: нужны адаптация под локальные правила оплаты и кодирования, интеграции с МИС, контуры ДМС/страховых администраторов, требования 152-ФЗ и защищённое развёртывание.

## Что сделано
- Создан кейс `pipeline/cases/autonomous-medical-coding-operator/`.
- В `00-brief.md` на русском зафиксированы описание модели, стартовые факты и ключевая гипотеза.
- Исходный raw-файл подготовлен к перемещению в `pipeline/raw/processed/`.

## Вердикт
Сигнал принят как основание для открытия нового кейса. RapidClaims усиливает гипотезу, что autonomous medical coding и revenue cycle automation для крупных медконтуров могут стать отдельной high-LTV сервисной моделью на рынке РФ.

```

