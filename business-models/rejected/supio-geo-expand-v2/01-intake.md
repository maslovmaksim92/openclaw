---
sector: LEGAL
rerun: true
source_raw: 2026-04-19-resurrect-supio-geo-expand.md
created: 2026-04-22T00:29:00+03:00
---

# 01-intake

## Кейс
supio-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-17-supio-geo-expand.md

## Краткий контекст
Supio: plaintiff-side legal claims automation, medical record review, chronology и demand preparation для litigation workflow. Ранее сигнал не открывал новый кейс, но resurrect-режим требует отдельной полной переоценки.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — supio-geo-expand

## Meta
- source: triage/triage-2026-04-17-supio-geo-expand.md
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
- `pipeline/raw/raw-2026-04-17-1758-msk-supio-geo-expand.md`

## Классификация
Новый сигнал, но кейс не проходит порог по LTV.

## Решение
Не создавать новый кейс в `pipeline/cases/`.

## Почему это не дубль
В `pipeline/cases/` не найден открытый кейс с фокусом именно на plaintiff-side legal AI для personal injury, mass tort, медицинских хронологий, demand letters и claims workflow. Текущий открытый кейс `enterprise-institutional-intelligence-workflow-platform` относится к другой категории: это enterprise-платформа для document-heavy аналитики в финансах, legal и strategy, а не вертикальный plaintiff litigation workflow.

## Почему кейс не проходит фильтр
- Во входном сигнале указан ожидаемый LTV для РФ на уровне `1,8-6,0 млн ₽ в год` на клиента.
- Это соответствует примерно `150-500 тыс. ₽ в месяц`, то есть верхняя граница только достигает порога, но не превышает требование Program 1 `>500 тыс. ₽ в месяц`.
- Сигнал выглядит качественным и тематически осмысленным, но по текущей оценке экономики не даёт достаточного запаса по high-LTV recurring-модели для открытия нового кейса.

## Что сделано
- Новый кейс не создан.
- Причина решения зафиксирована в этом triage-отчёте.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал отнесён к новым, но отклонён на этапе triage: при текущей оценке экономики тема не проходит порог Program 1 по месячному LTV.

```
