---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-salesforce-agentforce-it-service-adoption.md
created: 2026-04-21T15:56:07+03:00
original_verdict_source: triage/triage-2026-04-11-salesforce-agentforce-it-service-adoption.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — salesforce-agentforce-it-service-adoption

## Meta
- source: triage/triage-2026-04-11-salesforce-agentforce-it-service-adoption.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Triage

## Date
2026-04-11

## Inputs
- pipeline/raw/radar-2026-04-11-0210-msk.md

## Classification
signal, but existing case support

## Decision
Не создавать новый case.
Привязать сигнал к существующему case: `pipeline/cases/ai-native-salesforce-implementation-operator/`.

## Why
Сигнал не описывает новую отдельную бизнес-модель, а усиливает уже открытый кейс вокруг AI-native внедрения Salesforce ecosystem.

Что подтверждает этот вход:
- enterprise buyers действительно выбирают Agentforce IT Service в заметном количестве;
- замена legacy ITSM/support stack создаёт работу по migration, implementation, integration и workflow redesign;
- окно "from purchase to production in weeks" поддерживает тезис, что скорость внедрения становится продаваемой ценностью.

Для pipeline это скорее demand/adoption evidence по существующему Salesforce implementation operator case, чем новый самостоятельный case-кандидат.

## Triage note
Использовать позже как evidence/demand support для `ai-native-salesforce-implementation-operator`, особенно при проверке размера и повторяемости рынка вокруг Agentforce deployments.

```

