---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1557-msk-norm-ai-geo-expand.md
created: 2026-04-20T01:02:37+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/2026-04-19-resurrect-1557-msk-norm-ai-geo-expand.md
- Базовый slug: `1557-msk-norm-ai-geo-expand`
- Новый slug кейса: `1557-msk-norm-ai-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 1557-msk-norm-ai-geo-expand

## Meta
- source: triage/triage-2026-04-17-1557-msk-norm-ai-geo-expand-followup.md
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
- `pipeline/raw/raw-2026-04-17-1557-msk-norm-ai-geo-expand.md`

## Классификация
Поддерживающий сигнал к существующему кейсу.

## Решение
Кейс `enterprise-compliance-operations-agents` усилен, новый кейс не создавался.

## Почему
- Сигнал относится к той же нише: enterprise compliance-операции, где регуляторные требования и внутренние policy превращаются в исполняемый AI-слой.
- Отдельный новый кейс создавать не нужно, потому что тема уже покрыта существующим кейсом `enterprise-compliance-operations-agents`.
- Новый raw добавляет дополнительные подтверждения по breadth рынка, суммарному привлечённому капиталу, диапазону LTV и слабости зрелых российских аналогов.

## Что добавлено
- В `pipeline/approved/enterprise-compliance-operations-agents/01-evidence.md` добавлена запись на русском языке с supporting signal.
- Зафиксированы новые факты: совокупное финансирование 87 млн долларов, охват клиентов от Fortune 100 до SMB, активы клиентов на 30 трлн долларов, ориентир 3,0-12,0 млн рублей в год с крупного клиента в РФ и высокая сложность локализации.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал не шумовой и не новый кейс. Это supporting signal, который усиливает кейс `enterprise-compliance-operations-agents`.

```

