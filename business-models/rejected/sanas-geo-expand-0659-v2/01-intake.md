---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-sanas-geo-expand-0659.md
created: 2026-04-21T18:05+03:00
source_triage: triage/triage-2026-04-15-sanas-geo-expand-0659.md
original_verdict: resurrect-full-pipeline
---

# Intake

## Статус
Принудительный resurrect/re-run. Кейс создан как standalone candidate и должен пройти полный пайплайн P3→P7 без классификации как duplicate.

## Исходный verdict
- `triage/triage-2026-04-15-sanas-geo-expand-0659.md`

## Полный контекст raw-файла

# RESURRECT SIGNAL — sanas-geo-expand-0659

## Meta
- source: triage/triage-2026-04-15-sanas-geo-expand-0659.md
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
- `pipeline/raw/2026-04-15-0659-sanas-geo-expand.md`

## Классификация
supporting signal для существующего открытого кейса

## Решение
Новый кейс не открывать.
Обогатить существующий кейс: `pipeline/cases/ai-customer-service-operations-operator/`.

## Почему
- Сигнал не открывает новый market container, а усиливает уже существующий кейс вокруг AI customer service operations и voice-heavy contact center workflows.
- Он добавляет полезный угол, которого не было в таком виде: подтверждённую коммерцию Sanas, явный enterprise-фокус на accent translation и разрыв между западным продуктом и российскими решениями, которые ближе к речевой аналитике и QA.
- Оценка LTV в raw остаётся достаточно высокой для existing case: 1,2-6,0 млн руб. в год на mid-market или enterprise call center аккаунт.

## Что добавлено в кейс
- В `pipeline/cases/ai-customer-service-operations-operator/01-evidence.md` добавлен supporting signal по Sanas.
- Зафиксированы факты про ARR $21 млн, около 50 клиентов и enterprise-позиционирование продукта для call center/CX.
- Отдельно отражено, что найденный локальный ориентир Ruspeech относится скорее к аналитике звонков и AI QA, а не к real-time accent translation, что усиливает гипотезу о рыночном окне.

## Что сделано
- Существующий кейс обогащён новым evidence entry.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: сигнал Sanas усиливает гипотезу, что в customer service operations есть отдельный дорогой voice-слой, который можно упаковывать как сервис внедрения, локализации и сопровождения для крупных контакт-центров.

```
