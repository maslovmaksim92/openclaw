---
sector: LEGAL
rerun: true
source_raw: 2026-04-19-resurrect-darrow-geo-expand.md
created: 2026-04-20T11:18:00+03:00
---

# 01-intake

## Кейс
darrow-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-16-darrow-geo-expand-followup.md

## Краткий контекст
Standalone legaltech-кейс по upstream litigation intelligence, поиску массовых нарушений и упаковке оснований для исков. Требуется новая аналитика P3→P7 как для самостоятельного кандидата, а не только supporting signal.

## Следующий шаг
Передать кейс в P3-demand-validation: подтвердить high-LTV сценарии, сложность локализации, доступность buyer'ов и наличие устойчивого GEO-EXPAND окна.

## Полный контекст из raw

# RESURRECT SIGNAL — darrow-geo-expand

## Meta
- source: triage/triage-2026-04-16-darrow-geo-expand-followup.md
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
- `pipeline/raw/raw-2026-04-16-1259-msk-darrow-geo-expand.md`

## Классификация
Поддерживающий сигнал для существующего открытого кейса.

## Решение
Сигнал добавлен в кейс `plaintiff-legal-claims-automation-operator`.

## Что именно добавлено
- В `pipeline/cases/plaintiff-legal-claims-automation-operator/01-evidence.md` добавлен новый supporting signal по Darrow.
- Зафиксированы факты о 80+ ведущих юрфирмах-клиентах, 50+ типах causes of action, 5 млн+ сигналов в месяц и litigation pipeline на $22 млрд+.
- Добавлено, что Darrow валидирует upstream-слой litigation intelligence: поиск, приоритизацию и упаковку оснований для массовых исках и претензионной работы.
- Уточнён высокий потенциальный LTV для РФ, если локализовать контур под арбитраж, суды общей юрисдикции, ФАС, Роспотребнадзор и трудовые споры.

## Почему это усиливает кейс
Darrow подтверждает, что plaintiff-side legal AI может начинаться не только на стадии обработки меддокументов и подготовки demand-пакетов, но и раньше, на этапе выявления самих litigation opportunities. Это делает кейс шире и сильнее: появляется дополнительный дорогой слой сервиса вокруг поиска массовых нарушений, оценки перспективы и подготовки юридического пайплайна.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен подтверждающий GEO-EXPAND сигнал по Darrow для `plaintiff-legal-claims-automation-operator`.

```

