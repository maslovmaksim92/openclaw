---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1007-msk-sanas-accent-translation-geo-expand.md
created: 2026-04-19T22:31:00+03:00
---

# 01-intake

## Кейс
1007-msk-sanas-accent-translation-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — 1007-msk-sanas-accent-translation-geo-expand

## Meta
- source: triage/triage-2026-04-19-1007-msk-sanas-accent-translation-geo-expand.md
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
- `pipeline/raw/raw-2026-04-19-1007-msk-sanas-accent-translation-geo-expand.md`

## Классификация
supporting signal для существующего открытого кейса

## Решение
Обогатить существующий кейс `pipeline/cases/voice-accent-translation-contact-center-operator/`.

## Почему
- Сигнал напрямую совпадает с уже открытым кейсом по real-time accent translation и speech enhancement для enterprise-контакт-центров.
- Во входном файле есть новые подтверждения зрелости категории: 1 млрд+ минут речи через платформу, присутствие в 50+ странах, $65 млн Series B и стратегическое партнёрство с Teleperformance.
- Экономика остаётся релевантной для Program 1 в верхнем сегменте: для very large BPO и крупных enterprise-контрактов указаны 10+ млн ₽ в год, что поддерживает гипотезу high-LTV.

## Что добавлено в кейс
- В `pipeline/cases/voice-accent-translation-contact-center-operator/01-evidence.md` добавлен новый supporting signal на русском языке.
- Зафиксированы дата, ссылки на источники, тип сигнала, объяснение, как именно сигнал усиливает кейс, и ключевые факты по traction, финансированию, географии и LTV.

## Что сделано
- Существующий кейс обогащён.
- Raw-файл перенесён в `pipeline/raw/processed/raw-2026-04-19-1007-msk-sanas-accent-translation-geo-expand.md`.

## Вердикт
Кейс обогащён: добавлен supporting signal по Sanas, усиливающий доказательную базу по нише voice accent translation для enterprise-контакт-центров.
```

