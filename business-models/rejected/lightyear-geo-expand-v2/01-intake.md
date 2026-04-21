---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-lightyear-geo-expand.md
created: 2026-04-20T22:33:00+03:00
---

# 01-intake

## Кейс
lightyear-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-lightyear-geo-expand.md

## Краткий контекст
Standalone кейс по enterprise telecom procurement и telecom expense management с высоким потенциальным чеком и интеграционной сложностью. Требуется новая аналитика P3→P7, даже если исторически сигнал считался дубликатом или недостаточным по LTV.

## Следующий шаг
Передать кейс в P3-demand-validation: подтвердить high-LTV сценарии, сложность локализации, доступность buyer'ов и наличие устойчивого GEO-EXPAND окна.

## Полный контекст из raw

# RESURRECT SIGNAL — lightyear-geo-expand

## Meta
- source: triage/triage-2026-04-15-lightyear-geo-expand.md
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
- `pipeline/raw/raw-2026-04-15-lightyear-geo-expand.md`

## Классификация
Новый сигнал, открыть новый кейс.

## Решение
Создан новый кейс `enterprise-telecom-procurement-expense-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: сигнал относится к специализированному контуру enterprise telecom procurement и telecom expense management, а не к уже открытым кейсам по compliance, contract operations, SRE, marketing или investment banking.
- Lightyear выглядит как AI-native слой для дорогой корпоративной функции с высоким средним чеком: закупка connectivity, управление inventory, счета и telecom spend в одном workflow.
- В raw-файле зафиксирован потенциальный LTV для РФ на уровне `1 800 000-7 000 000 ₽ в год` на крупного клиента, то есть верхняя часть диапазона превышает порог `500 000 ₽ в месяц` для открытия нового кейса.
- Для локального рынка ожидается существенный сервисный слой, а значит сигнал больше похож на будущую операторскую модель, чем на простую продуктовую фичу.

## Что сделано
- Создан кейс `pipeline/cases/enterprise-telecom-procurement-expense-operator/`.
- В кейсе создан файл `00-brief.md` с формулировкой модели, текущим состоянием и core hypothesis.
- Исходный raw-файл обработан и перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал признан достаточно сильным для открытия нового кейса: это отдельный enterprise-wedge с дорогими workflow, выраженной интеграционной сложностью и потенциалом high-LTV managed-сервиса на локальном рынке.
```

