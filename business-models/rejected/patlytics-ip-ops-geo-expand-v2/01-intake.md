---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-patlytics-ip-ops-geo-expand.md
created: 2026-04-21T10:38:23+03:00
original_verdict: triage/triage-2026-04-14-patlytics-ip-ops-geo-expand.md
---

# 01-intake

## Кейс
patlytics-ip-ops-geo-expand-v2

## Тип intake
resurrect

## rerun_of
patlytics-ip-ops-geo-expand

## Ссылка на оригинальный verdict
triage/triage-2026-04-14-patlytics-ip-ops-geo-expand.md

## Дата intake
2026-04-21, Europe/Moscow

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — patlytics-ip-ops-geo-expand

## Meta
- source: triage/triage-2026-04-14-patlytics-ip-ops-geo-expand.md
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
2026-04-14

## Входные данные
- pipeline/raw/raw-2026-04-14-patlytics-ip-ops-geo-expand.md

## Классификация
новый сигнал, но кейс не открываем

## Решение
Не открывать новый кейс на этом этапе.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы не покрывают вертикаль полного цикла patent operations / IP operations как отдельную сервисную модель.
- По экономике сигнал не проходит порог для открытия нового кейса в Program 1: в raw-файле указан `ltv_signal: 1500000-6000000 ₽ в год на клиента`, то есть примерно 125 000-500 000 руб. в месяц. Верхняя граница только касается порога, но не даёт запаса выше требования `> 500 000 руб./мес.`.
- GEO-EXPAND логика выглядит правдоподобно, но `localization_effort: hard`: для локального рынка потребуются адаптация под процессы Роспатента, русскоязычные документы, местные патентные бюро и корпоративные IP-процессы.
- Сигнал подтверждает рост продуктовой категории, но пока не подтверждает достаточно тяжёлый recurring service layer с высоким ежемесячным чеком, например managed implementation, интеграции, secure deployment и постоянное сопровождение больших IP-портфелей.

## Что сделано
- Новый кейс не создан.
- Подтверждено, что совпадающего открытого кейса для обогащения нет.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Пометка для следующего шага
Вернуться к теме, если появятся дополнительные сигналы, подтверждающие хотя бы один из пунктов:
- enterprise LTV уверенно выше 500 000 руб. в месяц на клиента или контур;
- спрос со стороны крупных корпораций с большими IP-портфелями, а не только патентных фирм;
- тяжёлый сервисный слой: внедрение, интеграции, защищённый контур, recurring сопровождение;
- повторяемые российские сценарии вокруг patent operations, patent prosecution или корпоративного IP workflow.

## Вердикт
Сигнал содержательный, но пока недостаточно сильный для открытия нового кейса в Program 1: LTV пограничный, локализация тяжёлая, открытого matching case нет, сервисная экономика не подтверждена.

```
