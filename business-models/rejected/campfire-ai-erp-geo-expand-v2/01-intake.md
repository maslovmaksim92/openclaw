---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-campfire-ai-erp-geo-expand.md
created: 2026-04-20T08:06:00+03:00
---

# 01-intake

## Кейс
campfire-ai-erp-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-campfire-ai-erp-geo-expand.md

## Краткий контекст
Standalone GEO-EXPAND кейс по AI-native ERP, close automation и finance operations. Нужно заново проверить, можно ли собрать в РФ high-LTV пакет через сервисный слой, интеграции и enterprise deployment, несмотря на пограничную экономику из исходного triage.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить buyer, бюджет, частоту использования, интеграции, сложность локализации и реалистичность выхода на высокий LTV в РФ.

## Полный контекст из raw

# RESURRECT SIGNAL — campfire-ai-erp-geo-expand

## Meta
- source: triage/triage-2026-04-14-campfire-ai-erp-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-campfire-ai-erp-geo-expand.md

## Классификация
низкий LTV для Program 1, кейс не открываем

## Решение
Не открывать новый кейс и не обогащать существующие кейсы.

## Почему
- Сигнал описывает AI-native ERP и бухгалтерскую платформу для finance-команд, что само по себе выглядит как интересный GEO-EXPAND wedge.
- Однако в raw-файле указана экономика `1,5-6,0 млн ₽ в год на клиента`, то есть примерно `125 000-500 000 ₽ в месяц`.
- Для Program 1 порог сформулирован как `> 500 000 ₽/мес.`, а здесь верхняя граница лишь достигает 500 000 ₽ в месяц, но не превышает её.
- Подходящего открытого кейса в `pipeline/cases/` по AI-native ERP / AI-бухгалтерии / finance close automation сейчас нет, поэтому обогащать существующий кейс нечем.
- Локализация также обозначена как `hard`: нужна глубокая адаптация под российский бухучёт, налоговый учёт, 1С, банк-клиенты, ЭДО и комплаенс, что ухудшает профиль запуска при пограничной экономике.

## Что сделано
- Новый кейс не создан.
- Существующие кейсы не обновлялись.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал качественный и стратегически интересный, но для Program 1 пока недостаточно сильный: подтверждённый LTV находится на границе порога, а не выше него. Возвращаться к теме имеет смысл, если появятся новые данные о более высоком enterprise ACV, крупных mid-market внедрениях или отдельном сервисном слое с recurring-выручкой поверх AI-native ERP.

```

