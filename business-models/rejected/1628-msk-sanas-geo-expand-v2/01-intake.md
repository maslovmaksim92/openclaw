---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1628-msk-sanas-geo-expand.md
created: 2026-04-20T01:49:02+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/triage-2026-04-18-1628-msk-sanas-geo-expand.md
- Базовый slug: `1628-msk-sanas-geo-expand`
- Новый slug кейса: `1628-msk-sanas-geo-expand-v2`
- Предыдущее решение: Ранее сигнал был принят как новый кейс `voice-accent-translation-contact-center-operator`.

## Полный контекст raw

# RESURRECT SIGNAL — 1628-msk-sanas-geo-expand

## Meta
- source: triage/triage-2026-04-18-1628-msk-sanas-geo-expand.md
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
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-1628-msk-sanas-geo-expand.md`

## Классификация
new case

## Решение
Открыть новый кейс: `pipeline/cases/voice-accent-translation-contact-center-operator/`.

## Почему
- В `pipeline/cases/` нет открытого кейса по real-time accent translation и live voice normalization для enterprise-контакт-центров.
- Во входном raw-файле указан ориентир `1 200 000-6 000 000 ₽ в год` с одного среднего контакт-центра в РФ, то есть примерно `100 000-500 000 ₽ в месяц`.
- Средний сегмент находится на границе порога Program 1, но для крупных аутсорсеров и enterprise BPO во входном сигнале отдельно указан более высокий потенциал, поэтому верхний сегмент проходит критерий `>500 000 ₽ в месяц`.
- Сигнал подтверждает зрелую западную категорию с enterprise-внедрениями и показывает отсутствие заметного локального лидера в РФ именно в узком классе accent translation для операторских коммуникаций.

## Что создано
- Создан кейс `pipeline/cases/voice-accent-translation-contact-center-operator/`.
- В `00-brief.md` зафиксированы суть кейса, логика открытия и предварительная экономика.

## Что сделано
- Создан новый открытый кейс.
- Raw-файл перенесён в `pipeline/raw/processed/raw-2026-04-18-1628-msk-sanas-geo-expand.md`.

## Вердикт
Сигнал принят как новый кейс. Тему real-time accent translation для enterprise-контакт-центров имеет смысл держать в активном пайплайне как пограничный, но перспективный high-LTV кейс для верхнего сегмента рынка.

```

