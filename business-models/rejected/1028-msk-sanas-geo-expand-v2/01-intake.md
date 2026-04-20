---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1028-msk-sanas-geo-expand.md
created: 2026-04-19T23:24:43+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/triage-2026-04-17-1028-msk-sanas-geo-expand.md
- Базовый slug: `1028-msk-sanas-geo-expand`
- Новый slug кейса: `1028-msk-sanas-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 1028-msk-sanas-geo-expand

## Meta
- source: triage/triage-2026-04-17-1028-msk-sanas-geo-expand.md
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
- `pipeline/raw/raw-2026-04-17-1028-msk-sanas-geo-expand.md`

## Классификация
new case

## Решение
Открыть новый кейс: `pipeline/cases/voice-accent-translation-contact-center-operator/`.

## Почему
- В `pipeline/cases/` нет открытого кейса по real-time accent translation для live-операторов контакт-центров.
- Текущий сигнал по Sanas сильнее предыдущих версий темы по экономике и масштабу: raw указывает ориентир `3 000 000-18 000 000 ₽ в год` на крупного клиента, то есть примерно `250 000-1 500 000 ₽ в месяц`.
- Верхняя часть диапазона даёт уверенный проход по порогу Program 1 `> 500 000 ₽/мес`.
- Сигнал также подтверждает, что категория уже валидирована на глобальном рынке через крупные BPO, contact center deployments, 39 стран и стратегическое партнёрство с Teleperformance.

## Что создано
- Создан кейс `pipeline/cases/voice-accent-translation-contact-center-operator/`.
- В `00-brief.md` зафиксированы модель, экономика, основания для повторного открытия темы и гипотеза локализации.
- В `01-evidence.md` добавлен первичный evidence-блок по Sanas с ключевыми фактами и источниками.

## Что сделано
- Создан новый открытый кейс.
- Исходный raw-файл подготовлен к переносу в `pipeline/raw/processed/`.

## Вердикт
Сигнал принят как новый кейс. Тема voice accent translation для enterprise-контакт-центров повторно открыта, потому что текущий raw показывает более сильную экономику и более убедительную глобальную валидацию категории.

```
