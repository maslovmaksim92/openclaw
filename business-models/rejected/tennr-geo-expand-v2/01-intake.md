---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-tennr-geo-expand.md
created: 2026-04-22T00:33:29+03:00
original_verdict_source: triage/triage-2026-04-18-tennr-geo-expand.md
---

# Intake

## Режим
Принудительный rerun/resurrect full pipeline. Кейс создан заново и не классифицируется как duplicate на этапе intake.

## Полный контекст raw-файла

```md
# RESURRECT SIGNAL — tennr-geo-expand

## Meta
- source: triage/triage-2026-04-18-tennr-geo-expand.md
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
- `pipeline/raw/raw-2026-04-18-0157-msk-tennr-geo-expand.md`

## Классификация
Новый сигнал, но кейс не создаётся.

## Решение
Не открывать новый кейс.

## Почему
- В `pipeline/cases/` не найден открытый кейс, который нужно обогатить, поэтому сигнал проверялся как кандидат на новый кейс.
- Сигнал содержательно качественный: Tennr решает реальную B2B-боль в healthcare ops, связанную с intake, triage входящих документов, qualification и patient routing.
- Однако указанный во входном файле LTV-сигнал составляет `1 500 000-6 000 000 ₽ в год` на одного крупного клиента, то есть примерно `125 000-500 000 ₽ в месяц`.
- По standing orders Program 1 новый кейс создаётся только при потенциале `> 500 000 ₽ в месяц`. Здесь верхняя граница диапазона доходит до порога, но не превышает его, поэтому сигнал не проходит фильтр на открытие нового кейса.
- Локализация также отмечена как hard: нужны сложные интеграции с МИС/ЕМК, адаптация под ОМС/ДМС, ПДн и российский медицинский документооборот. Это дополнительно ухудшает профиль для Program 1 при пограничной экономике.

## Что сделано
- Подготовлен triage-отчёт на русском языке.
- Новый кейс в `pipeline/cases/` не создавался.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал не является шумом, но для Program 1 отклонён как новый кейс из-за недостаточного LTV относительно порога открытия. При появлении более сильных данных по контрактам, enterprise rollout или монетизации тему можно пересмотреть повторно.

```
```
