---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-arphie-geo-expand.md
created: 2026-04-20T07:20:00+03:00
original_verdict: triage/triage-2026-04-17-arphie-geo-expand.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — arphie-geo-expand

## Meta
- source: triage/triage-2026-04-17-arphie-geo-expand.md
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
- `pipeline/raw/raw-2026-04-17-1003-msk-arphie-geo-expand.md`

## Классификация
Новый сигнал, но кейс не создаётся.

## Решение
Кейс в `pipeline/cases/` не создан.

## Почему это не дубль
В `pipeline/cases/` не найден открытый кейс с фокусом на AI-автоматизации RFP, DDQ и security questionnaires для B2B sales, presales и compliance workflows.

## Почему кейс не проходит фильтр
- Сигнал выглядит содержательным и не является шумом: есть продуктовая специализация, seed-раунд $2,9 млн и признаки enterprise traction.
- Однако указанный LTV-сигнал составляет `1 200 000–4 800 000 ₽ в год` на клиента, то есть примерно `100 000–400 000 ₽ в месяц`.
- Это ниже порога `500 000 ₽ в месяц`, который требуется для создания нового кейса по standing orders.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал по Arphie зафиксирован как качественный, но новый кейс не создан из-за недостаточного подтверждённого потенциала monthly LTV по текущему входному материалу.

```
