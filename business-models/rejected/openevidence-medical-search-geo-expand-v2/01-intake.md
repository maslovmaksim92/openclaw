---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-openevidence-medical-search-geo-expand.md
created: 2026-04-21T04:30:41+03:00
original_verdict: triage/triage-2026-04-15-openevidence-medical-search-geo-expand.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `openevidence-medical-search-geo-expand-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — openevidence-medical-search-geo-expand

## Meta
- source: triage/triage-2026-04-15-openevidence-medical-search-geo-expand.md
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
- `pipeline/raw/raw-2026-04-15-openevidence-medical-search-geo-expand.md`

## Классификация
шум / дубликат ранее оценённого сигнала

## Решение
Новый кейс не открывать.

## Почему
- Сигнал дублирует уже обработанный материал по OpenEvidence из `pipeline/triage/triage-2026-04-14-openevidence-geo-expand.md`.
- Подходящего открытого кейса в `pipeline/cases/` по evidence-based medical search / clinical decision support для врачей по-прежнему нет, поэтому обогащать `01-evidence.md` нечего.
- Экономика сигнала не изменилась: указанный `ltv_signal` остаётся в диапазоне `1 200 000-6 000 000 ₽ в год на клиента`, то есть примерно `100 000-500 000 ₽ в месяц`. Это всё ещё не превышает рабочий порог `> 500 000 ₽/мес.` для открытия нового кейса.
- Новых фактов, которые materially усиливают гипотезу отдельной high-LTV service-модели для локального рынка, в raw-файле нет.

## Что сделано
- Зафиксировано, что это повторный сигнал по уже рассмотренной теме OpenEvidence.
- Новый кейс не создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это повтор уже оценённого сигнала без новых данных, меняющих решение. Кейc не открыт, потому что LTV всё ещё не проходит порог, а отдельная high-value сервисная модель не подтверждена.

```

