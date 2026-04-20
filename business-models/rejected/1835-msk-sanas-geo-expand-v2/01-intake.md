---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1835-msk-sanas-geo-expand.md
created: 2026-04-20T01:49:02+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/triage-2026-04-18-1835-msk-sanas-geo-expand.md
- Базовый slug: `1835-msk-sanas-geo-expand`
- Новый slug кейса: `1835-msk-sanas-geo-expand-v2`
- Предыдущее решение: Ранее сигнал был отклонён как шум для Program 1 из-за недостаточного LTV.

## Полный контекст raw

# RESURRECT SIGNAL — 1835-msk-sanas-geo-expand

## Meta
- source: triage/triage-2026-04-18-1835-msk-sanas-geo-expand.md
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
- `pipeline/raw/raw-2026-04-18-1835-msk-sanas-geo-expand.md`

## Классификация
Шум для Program 1, кейс не создаётся.

## Решение
Не открывать новый кейс в `pipeline/cases/`.

## Почему
- В `pipeline/cases/` нет открытого кейса, который нужно обогатить как duplicate или supporting signal.
- Входной сигнал остаётся в теме real-time accent transformation для контакт-центров, но указанный `ltv_signal` составляет только `600 000-3 600 000 ₽ в год` на одного B2B-клиента, то есть примерно `50 000-300 000 ₽ в месяц`.
- Это ниже порога Program 1 `> 500 000 ₽ в месяц`, поэтому сигнал не проходит по economics даже при наличии западного traction и понятной enterprise-боли.
- Следовательно, по standing orders такой сигнал нужно отбраковать, а не переводить в открытый кейс.

## Что сделано
- Новый кейс не создан.
- Raw-файл перенесён в `pipeline/raw/processed/raw-2026-04-18-1835-msk-sanas-geo-expand.md`.

## Вердикт
Сигнал отклонён для Program 1: тема выглядит рыночно понятной, но заявленный LTV недостаточен для открытия нового кейса по текущему порогу.
```

