---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-clay-geo-expand.md
created: 2026-04-20T08:44:00+03:00
---

# 01-intake

## Кейс
clay-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-clay-geo-expand.md

## Краткий контекст
Standalone GEO-EXPAND кейс по AI-native GTM, sales enrichment и outbound stack. Исходный проход признал сигнал интересным, но недостаточным по high-LTV monthly potential; текущий rerun требует полноценной новой аналитики.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить buyer в РФ, реалистичный monthly чек enterprise-сценария, service layer и окно для локализации без reliance на западный data stack.

## Полный контекст из raw

# RESURRECT SIGNAL — clay-geo-expand

## Meta
- source: triage/triage-2026-04-15-clay-geo-expand.md
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
- `pipeline/raw/2026-04-15-clay-geo-expand.txt`

## Классификация
Шум / недостаточно сильный сигнал для открытия нового кейса.

## Решение
Новый кейс не создан.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: сигнал относится к AI-native GTM / sales enrichment / outbound stack, а не к уже открытым кейсам по marketing implementation, CRM-операциям, customer service, contract ops или enterprise software implementation.
- При этом signal pack пока недостаточен для открытия отдельного кейса по standing orders: в raw-файле указан потенциальный LTV `180 000–900 000 ₽ в год` для SMB/MM и `1 500 000–6 000 000 ₽+ в год` для enterprise, то есть только верхняя граница enterprise-диапазона приближается к порогу `500 000 ₽ в месяц`, но не даёт уверенного запаса выше него.
- Сигнал подтверждает интересный GEO-EXPAND продуктовый класс, но пока больше похож на гипотезу о локализации западной платформы, чем на уже достаточно оформленную high-LTV service/operator-модель для российского рынка.
- Для открытия кейса не хватает более жёстких локальных подтверждений: кто именно buyer в РФ, какой реалистичный месячный чек у managed service или implementation layer, и можно ли стабильно собрать модель выше `500 000 ₽/мес`, а не только в редком верхнем enterprise-сценарии.

## Что сделано
- Отдельный кейс не создавался.
- Исходный raw-файл помечен как обработанный и перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал признан интересным, но недостаточным для открытия нового кейса на текущем проходе: категория выглядит перспективной, однако обязательный порог по high-LTV monthly potential пока не подтверждён с нужной уверенностью.
```
