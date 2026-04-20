---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-1229-msk-abridge-geo-expand.md
created: 2026-04-20T00:18:00+03:00
---

# 01-intake

## Кейс
1229-msk-abridge-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — 1229-msk-abridge-geo-expand

## Meta
- source: triage/triage-2026-04-18-1229-msk-abridge-geo-expand.md
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
- `pipeline/raw/raw-2026-04-18-1229-msk-abridge-geo-expand.md`

## Классификация
Новый сигнал, кейс открыт.

## Решение
Создать новый кейс: `pipeline/cases/ambient-clinical-documentation-operator`.

## Почему
- В `pipeline/cases/` не найден открытый кейс по ambient clinical documentation, который можно было бы обогатить как duplicate или supporting signal.
- Сигнал по Abridge подтверждает зрелую западную категорию: более 100 health systems в феврале 2025, более 200 health systems в октябре 2025 и прогноз более 80 млн разговоров врач-пациент в 2026 году через 250 крупнейших health systems США.
- Во входном файле указан `ltv_signal` `1 500 000-6 000 000 ₽ в год` с одной крупной клиники или сети, то есть примерно `125 000-500 000 ₽ в месяц`. Верхняя граница находится на пороге Program 1, а для сети клиник, private deployment, интеграций и сервисного слоя месячный LTV может превышать `500 000 ₽`.
- На российском рынке во входном материале не найден прямой зрелый аналог уровня enterprise ambient AI для клинической документации внутри hospital-grade workflow.

## Что сделано
- Создан кейс `pipeline/cases/ambient-clinical-documentation-operator/00-brief.md`.
- Исходный raw-файл подготовлен к переносу в `pipeline/raw/processed/`.
- Триаж-отчёт оформлен на русском языке.

## Вердикт
Сигнал проходит фильтр Program 1 как новый кейс: нишевой enterprise healthcare workflow с подтверждённой западной категорией и правдоподобным high-LTV потенциалом для крупных клиник и медсетей в РФ.

```
