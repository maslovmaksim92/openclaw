---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-0703-msk-aibidia-geo-expand.md
created: 2026-04-19T22:17:09+03:00
---

# Intake

## Название
0703 MSK Aibidia GEO Expand

## Режим обработки
Принудительный resurrect по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Исходный triage
/home/node/.openclaw/workspace/branch-models-lead/pipeline/triage/triage-2026-04-19-0703-msk-aibidia-geo-expand-supporting.md

## Краткий контекст
Сигнал ранее был обработан как supporting signal для кейса enterprise transfer pricing automation, но по правилу resurrect теперь должен пройти полный пайплайн как отдельный кейс.

## Полный контекст из raw

# RESURRECT SIGNAL — 0703-msk-aibidia-geo-expand

## Meta
- source: triage/triage-2026-04-19-0703-msk-aibidia-geo-expand-supporting.md
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
2026-04-19

## Входные данные
- `pipeline/raw/2026-04-19-0703-msk-aibidia-geo-expand.md`

## Классификация
поддерживающий сигнал для существующего открытого кейса

## Решение
Существующий кейс обогащён, новый кейс не создавался.

## Совпадающий кейс
- `pipeline/cases/enterprise-transfer-pricing-automation-platform/`

## Почему
- Сигнал полностью совпадает по нише, покупателю и технологии с уже открытым кейсом про AI-платформу для трансфертного ценообразования и cross-border tax compliance.
- Во входном файле есть новые подтверждающие данные о масштабе клиентов, международной выручке и инвестициях, поэтому его корректно трактовать как supporting signal, а не как новый кейс.
- Тема уже открыта в `pipeline/cases/`, поэтому создание отдельного кейса не требуется.

## Что добавлено в кейс
- Создан и заполнен `pipeline/cases/enterprise-transfer-pricing-automation-platform/01-evidence.md` на русском языке.
- Добавлена запись с датой, источниками, типом сигнала, объяснением, как сигнал усиливает кейс, и ключевыми фактами.
- Зафиксированы данные: $28 млн Series B, 100+ корпоративных клиентов, средний масштаб клиента около €7 млрд выручки, 7000+ управляемых юрлиц и доля США выше 15% в выручке компании.

## Что сделано
- Кейс `enterprise-transfer-pricing-automation-platform` обогащён.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал обработан как supporting signal для открытого кейса. Кейс обогащён новыми подтверждающими данными.

```
