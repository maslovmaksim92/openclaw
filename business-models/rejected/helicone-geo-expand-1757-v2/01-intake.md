---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-helicone-geo-expand-1757.md
created: 2026-04-20T17:04:00+03:00
source_triage: triage/triage-2026-04-18-helicone-geo-expand-1757.md
original_verdict: resurrect-full-pipeline
---

# Intake

## Статус
Принудительный resurrect/re-run. Кейс создан как standalone candidate и должен пройти полный пайплайн P3→P7 без классификации как duplicate.

## Исходный verdict
- `triage/triage-2026-04-18-helicone-geo-expand-1757.md`

## Полный контекст raw-файла

# RESURRECT SIGNAL — helicone-geo-expand-1757

## Meta
- source: triage/triage-2026-04-18-helicone-geo-expand-1757.md
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
- `pipeline/raw/raw-2026-04-18-1757-msk-helicone-geo-expand.md`

## Классификация
Новый сигнал, кейс не создаётся.

## Решение
Новый кейс не открывать.

## Почему
- В `pipeline/cases/` не найден существующий открытый кейс по теме AI gateway + LLM observability, который нужно было бы обогатить как дубль или supporting signal.
- Сигнал описывает понятную B2B-категорию: управление вызовами моделей, трассировка, cost tracking, fallback routing и observability для production AI-приложений.
- Однако во входном raw-файле `ltv_signal` указан как `300000-1500000 ₽ в год с одного B2B-клиента в РФ`, то есть примерно `25000-125000 ₽ в месяц`.
- По standing orders Program 1 новый кейс открывается только при потенциале `> 500000 ₽ в месяц`. Текущий сигнал существенно ниже порога.
- Поэтому сигнал полезен как рыночный ориентир по категории, но на текущих данных не даёт основания открывать отдельный кейс.

## Что сделано
- Новый кейс в `pipeline/cases/` не создавался.
- `01-evidence.md` не обновлялся, так как совпадающего открытого кейса нет.
- Raw-файл помечен как обработанный и перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал по Helicone отклонён на этапе Program 1 из-за недостаточного месячного LTV относительно порога. Категория AI gateway и LLM observability выглядит рыночно интересной, но по текущей экономике не проходит фильтр на открытие кейса.
```

