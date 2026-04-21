---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-infinitus-geo-expand.md
created: 2026-04-20T18:14:00+03:00
original_verdict: triage/triage-2026-04-18-infinitus-geo-expand.md
---

# Intake

## Режим обработки
Принудительный полный пайплайн по правилу `rerun-/resurrect-`. На этапе intake файл не классифицируется как duplicate.

## Оригинальный источник
- Raw-файл: `2026-04-19-resurrect-infinitus-geo-expand.md`
- Исторический источник: `triage/triage-2026-04-18-infinitus-geo-expand.md`

## Полный контекст из raw

# RESURRECT SIGNAL — infinitus-geo-expand

## Meta
- source: triage/triage-2026-04-18-infinitus-geo-expand.md
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
- `pipeline/raw/raw-2026-04-18-2227-msk-infinitus-geo-expand.md`

## Классификация
Дубликат / supporting signal для существующего открытого кейса.

## Решение
Обогатить кейс `patient-facing-healthcare-ai-agents-operator`.

## Почему
- В `pipeline/cases/` уже есть подходящий открытый кейс по patient-facing healthcare AI-агентам для клиник, страховщиков и медицинских операторов.
- Сигнал по Infinitus не требует открытия нового контейнера: он попадает в ту же смежную нишу healthcare voice AI для patient access, patient navigation и координации между клиниками, страховщиками и пациентами.
- По силе рынка сигнал полезен как подтверждение enterprise-grade спроса: во входном файле указаны 100+ млн автоматизированных минут, 6+ млн звонков, 125000+ провайдеров и использование в 44% Fortune 50.
- Экономика также сильная: во входном файле указан ориентир `3 000 000-18 000 000 ₽ в год` на одного крупного клиента в РФ, что поддерживает high-LTV характер уже открытого кейса.

## Что сделано
- Кейс `pipeline/cases/patient-facing-healthcare-ai-agents-operator/01-evidence.md` обогащён новым evidence entry на русском языке.
- Добавлено: дата, source URL, тип `supporting signal`, краткое объяснение, как сигнал усиливает кейс, и ключевые данные/факты по масштабу Infinitus и LTV.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён. Добавлен supporting signal по Infinitus как подтверждение спроса на healthcare voice AI для patient access и административной координации в медицинских workflow.

```
