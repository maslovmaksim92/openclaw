---
sector: LOGISTICS
rerun: true
source_raw: 2026-04-19-resurrect-microsoft-supply-chain-agentic-partner-offerings.md
created: 2026-04-21T03:03:41+03:00
---

# 01-intake

## Кейс
microsoft-supply-chain-agentic-partner-offerings-v2

## Тип сигнала
resurrect

## Основание создания
Файл с префиксом `resurrect-` по standing orders обязан пройти заново как самостоятельный кейс, даже если раньше был supporting signal или candidate под другим кейсом.

## Ссылка на исходный verdict
triage/triage-2026-04-13-microsoft-supply-chain-agentic-partner-offerings.md

## Краткий контекст
Microsoft и партнёрская экосистема вокруг agentic supply chain offerings как кандидат на repeatable service line для внедрения, интеграции и managed operations.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — microsoft-supply-chain-agentic-partner-offerings

## Meta
- source: triage/triage-2026-04-13-microsoft-supply-chain-agentic-partner-offerings.md
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
- pipeline/raw/raw-2026-04-13-microsoft-supply-chain-agentic-partner-offerings.md

## Classification
duplicate / supporting signal for existing case

## Decision
Не создавать отдельный новый case.

Route signal to case: `ai-finance-supply-chain-operations-operator`.

## Why
- Сигнал попадает в тот же enterprise wedge, что и ранее замеченный Oracle narrative: AI начинает встраиваться прямо в finance и supply-chain execution layers, где поверх платформы почти неизбежно нужен service layer из integration, workflow redesign, governance и managed optimisation.
- В отличие от чистого vendor PR, здесь есть важный ecosystem proofpoint: Microsoft показывает не только platform layer, но и partner-built agentic offerings вокруг supply-chain stack, что усиливает гипотезу о repeatable services model.
- Это не новый самостоятельный wedge, потому что core model остаётся той же: оператор внедрения и сопровождения AI-enabled finance / supply-chain operations внутри enterprise systems.

## Triage note
Использовать как supporting evidence для vendor breadth и partner-ecosystem validation внутри `pipeline/cases/ai-finance-supply-chain-operations-operator/`. В следующих evidence и demand cycles проверить, есть ли у integrators и consulting partners реальные service offers, бюджеты и deployment patterns вокруг AI-enabled supply-chain and finance operations.

```
