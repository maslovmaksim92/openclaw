---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1525-msk-abridge-geo-expand.md
created: 2026-04-20T02:26:19+03:00
original_verdict_source: triage/triage-2026-04-17-1525-msk-abridge-geo-expand.md
---

# Intake

## Режим обработки
Принудительный полный пайплайн для resurrect-сигнала. Этот кейс создан как standalone candidate и не должен классифицироваться как duplicate на этапе intake.

## Исходный raw-файл
- Имя: `2026-04-19-resurrect-1525-msk-abridge-geo-expand.md`
- Новый slug кейса: `1525-msk-abridge-geo-expand-v2`
- Следующий этап: `P3-demand-validation`

## Полный контекст из raw

# RESURRECT SIGNAL — 1525-msk-abridge-geo-expand

## Meta
- source: triage/triage-2026-04-17-1525-msk-abridge-geo-expand.md
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
- `pipeline/raw/raw-2026-04-17-abridge-geo-expand.md`

## Классификация
кандидат в новый кейс

## Решение
Открыть новый кейс: `ambient-clinical-documentation-operator`.

## Почему
- В `pipeline/cases/` на момент обработки не было открытого кейса по ambient clinical documentation.
- Сигнал по Abridge подтверждает зрелую западную категорию enterprise-уровня: продукт используется более чем в 150 health systems и масштабируется в large healthcare deployments.
- Потенциал экономики проходит порог Program 1: `5 000 000-30 000 000 ₽ в год` с одной сети клиник или крупной медсистемы, то есть выше `500 000 ₽ в месяц`.
- Быстрый обзор российского рынка в raw-материале не показывает заметного локального аналога именно для hospital-grade ambient clinical documentation внутри клинического workflow.
- Локализация тяжёлая, но это не ослабляет кейс, а скорее повышает вероятность service-heavy high-LTV оффера за счёт интеграций, безопасности и медицинской адаптации.

## Что сделано
- Создан кейс `pipeline/cases/ambient-clinical-documentation-operator/`.
- В `00-brief.md` зафиксированы модель, гипотеза и направления дальнейшей проверки.
- В `01-evidence.md` добавлен стартовый сигнал по Abridge.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал достаточно сильный для открытия нового кейса: это правдоподобная high-LTV enterprise-модель в healthcare с GEO-EXPAND потенциалом для крупных клиник и медсетей.

```
