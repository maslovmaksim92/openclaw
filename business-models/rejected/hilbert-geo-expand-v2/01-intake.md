---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-hilbert-geo-expand.md
created: 2026-04-20T17:45:00+03:00
original_verdict: triage/triage-2026-04-17-hilbert-geo-expand.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `hilbert-geo-expand-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Тема
Hilbert: AI-native growth decisioning и warehouse-native аналитико-операционный слой для B2C-команд.

## Полный контекст из raw

# RESURRECT SIGNAL — hilbert-geo-expand

## Meta
- source: triage/triage-2026-04-17-hilbert-geo-expand.md
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
- `pipeline/raw/raw-2026-04-17-hilbert-geo-expand.md`

## Классификация
Новый кейс.

## Решение
Создан новый кейс `warehouse-native-ai-decisioning-marketing-operator` в `pipeline/cases/`.

## Почему это не дубль
- В `pipeline/cases/` не найден открытый кейс с фокусом именно на AI-native growth decisioning и warehouse-native аналитико-операционном слое для B2C-команд.
- Сигнал тематически пересекается со смежными marketing и customer journey направлениями, но отличается акцентом на автономное выявление драйверов выручки, аномалий и рекомендованных действий поверх объединённых продуктовых, маркетинговых и финансовых данных.
- В legacy-слое уже встречались близкие гипотезы, но по standing orders проверка дублей для обогащения идёт по открытым кейсам в `pipeline/cases/`, а там такого контейнера не было.

## Почему кейс проходит фильтр
- Hilbert привлёк 28 млн долларов в Series A 15 апреля 2026 года, что подтверждает внешний спрос и уверенность инвесторов в категории.
- Во входном сигнале указаны клиенты уровня Walmart, FreshDirect, Blank Street и Levain, что усиливает enterprise и upper mid-market валидацию.
- По входному материалу локальный LTV оценивается в 1,8-9,0 млн ₽ в год на клиента, то есть верхняя часть диапазона превышает порог 500 000 ₽ в месяц.
- Для РФ описана реалистичная локализация через коннекторы к локальным CDP, CRM, BI и рекламным кабинетам, а также через private cloud или on-prem для крупных клиентов.

## Что создано
- `pipeline/cases/warehouse-native-ai-decisioning-marketing-operator/00-brief.md`
- `pipeline/cases/warehouse-native-ai-decisioning-marketing-operator/01-evidence.md`

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Создан новый кейс по AI-native growth decisioning для B2C-команд с потенциалом high-LTV service business на рынке РФ.

```
