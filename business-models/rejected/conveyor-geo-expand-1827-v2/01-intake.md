---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-conveyor-geo-expand-1827.md
created: 2026-04-20T09:30:00+03:00
original_verdict: triage/triage-2026-04-17-conveyor-geo-expand-1827-duplicate.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — conveyor-geo-expand-1827

## Meta
- source: triage/triage-2026-04-17-conveyor-geo-expand-1827-duplicate.md
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
- `pipeline/raw/raw-2026-04-17-1827-msk-conveyor-geo-expand.md`

## Классификация
дубликат ранее обработанного сигнала

## Решение
Новый кейс не открывать и существующие открытые кейсы не обогащать.

## Почему
- Файл повторяет уже обработанную тему `Conveyor`: AI-native платформа для автоматизации customer trust workflow, security questionnaires, Trust Center и RFP.
- Подходящего открытого кейса в `pipeline/cases/` для обогащения не найдено.
- По текущему raw-файлу `ltv_signal` указан как `900000-3600000 ₽ в год на клиента`, то есть примерно `75 000-300 000 ₽ в месяц`, что ниже порога Program 1 `> 500 000 ₽ в месяц`.
- Новых данных, которые меняют prior triage по теме и требуют открытия кейса, в сигнале нет.

## Что сделано
- Открытый кейс не создавался.
- `01-evidence.md` в `pipeline/cases/` не обновлялся, так как совпадающего открытого кейса нет.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Повторный сигнал по уже рассмотренной теме. На текущих данных кейс не проходит фильтр Program 1 по месячному LTV и остаётся без открытия нового кейса.

```

