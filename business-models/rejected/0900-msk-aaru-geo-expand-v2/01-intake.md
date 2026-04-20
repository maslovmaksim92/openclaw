---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-0900-msk-aaru-geo-expand.md
created: 2026-04-19T23:24:43+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/triage-2026-04-18-0900-msk-aaru-geo-expand.md
- Базовый slug: `0900-msk-aaru-geo-expand`
- Новый slug кейса: `0900-msk-aaru-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 0900-msk-aaru-geo-expand

## Meta
- source: triage/triage-2026-04-18-0900-msk-aaru-geo-expand.md
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
- `pipeline/raw/raw-2026-04-18-0900-msk-aaru-geo-expand.md`

## Классификация
Шум / не создаём новый кейс.

## Решение
Новый кейс не создан.

## Почему не создан кейс
- В `pipeline/cases/` нет открытого кейса для обогащения, поэтому сценарий duplicate/supporting signal к открытому кейсу не применим.
- Тема synthetic customer research по Aaru уже ранее разбиралась, но текущий raw не добавляет нового сильного факта по спросу, дистрибуции или экономике.
- В текущем входном файле указан LTV-сигнал `900000-3600000 ₽ в год`, то есть примерно `75 000-300 000 ₽ в месяц` на клиента, что ниже порога Program 1 в `500 000 ₽ в месяц`.
- Для запуска нового кейса на этом сигнале недостаточно подтверждения, что локальная экономика проходит фильтр high-LTV.

## Что проверено
- Источник: TechCrunch от 2025-12-05 про Series A и headline valuation.
- Источник: Accenture Newsroom от 2025-03-04 про инвестицию и партнёрство.
- Формулировка по рынку РФ: прямой локальный продукт не найден, но это само по себе не компенсирует слабый LTV в текущем raw.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал по теме интересный стратегически, но в текущем виде это не материал для нового открытого кейса: чек ниже порога, новых усиливающих фактов нет, поэтому кейс не создаём.

```
