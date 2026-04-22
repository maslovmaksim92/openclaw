---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-prorata-geo-expand-refresh.md
created: 2026-04-21T11:51:00+03:00
original_verdict: triage/triage-2026-04-19-prorata-geo-expand-refresh.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `prorata-geo-expand-refresh-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — prorata-geo-expand-refresh

## Meta
- source: triage/triage-2026-04-19-prorata-geo-expand-refresh.md
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
- `pipeline/raw/raw-2026-04-19-0427-msk-prorata-geo-expand-refresh.md`

## Классификация
Дубликат / supporting signal для существующего открытого кейса.

## Совпавший кейс
- `pipeline/cases/ai-content-licensing-and-attribution-platform/`

## Решение
Кейс обогащён новым supporting signal, новый кейс не создавался.

## Что добавлено в кейс
- В `pipeline/cases/ai-content-licensing-and-attribution-platform/01-evidence.md` добавлен supporting signal по ProRata.
- Зафиксировано подтверждение, что у ProRata более 1000 публикаций и авторов-партнёров по странице publishers.
- Добавлено пояснение, что этот сигнал усиливает гипотезу о коммерческой жизнеспособности AI-native платформы лицензирования контента, атрибуции и revenue share.
- Отмечено, что во входном сигнале также сохраняется важный контекст: заметная внешняя валидация модели и отсутствие прямого российского аналога такого класса.

## Почему это не новый кейс
- Сигнал полностью совпадает с уже открытым кейсом по AI-native платформе лицензирования контента и атрибуции.
- Новый raw-файл не открывает отдельную категорию, а усиливает уже существующую гипотезу дополнительным подтверждением traction и market validation.

## Вердикт
Существующий кейс `ai-content-licensing-and-attribution-platform` обогащён. Добавлен supporting signal, усиливающий тезис о наличии сетевого эффекта на стороне правообладателей и high-LTV потенциала инфраструктурной модели.

```
