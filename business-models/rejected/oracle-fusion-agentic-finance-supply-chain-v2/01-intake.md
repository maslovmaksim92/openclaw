---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-oracle-fusion-agentic-finance-supply-chain.md
created: 2026-04-21T04:30:41+03:00
original_verdict: triage/triage-2026-04-13-oracle-fusion-agentic-finance-supply-chain.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `oracle-fusion-agentic-finance-supply-chain-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — oracle-fusion-agentic-finance-supply-chain

## Meta
- source: triage/triage-2026-04-13-oracle-fusion-agentic-finance-supply-chain.md
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
2026-04-13

## Inputs
- pipeline/raw/radar-2026-04-11-1606-msk.md

## Classification
potentially new case

## Decision
Создать новый case-кандидат.

**Suggested case slug:** `ai-finance-supply-chain-operations-operator`

## Why
- Это выглядит не как обычный AI adoption signal, а как отдельный functional wedge вокруг finance и supply chain execution внутри enterprise systems.
- Oracle явно продвигает coordinated agent teams, которые работают внутри workflows, approvals, policies, permissions и transactional context, то есть речь идёт про operating layer, а не только про assistant UX.
- Поверх такого стека почти неизбежно возникает service layer: process redesign, integration с ERP и data systems, approval-policy setup, governance, observability, ROI measurement, exception handling и managed optimisation.
- Большая Oracle Fusion installed base повышает шанс, что это может стать repeatable service category для integrators и operators, а не единичным enterprise project.

## Triage note
Проверять как отдельную service line вокруг AI-enabled finance and supply chain operations: Oracle Fusion transformation, workflow redesign, approval and policy orchestration, ERP and data integration, governance and controls, exception routing, value measurement и ongoing optimisation. В следующем цикле важно найти не только vendor messaging, но и partner ecosystem signals, systems integrators, consulting offers и признаки реальных deployment patterns.

```

