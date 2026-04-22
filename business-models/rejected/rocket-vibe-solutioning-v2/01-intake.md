---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-rocket-vibe-solutioning.md
created: 2026-04-21T15:12:11+03:00
---

# 01-intake

## Кейс
rocket-vibe-solutioning-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом , поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-13-rocket-vibe-solutioning.md

## Краткий контекст
Standalone кейс по AI-native solutioning и strategy operator: market research, competitor tracking, GTM guidance, product strategy и solution design как более дешёвая и стандартизируемая альтернатива классическому consulting layer.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить бюджет владельца проблемы, повторяемость боли, возможность пакетизации AI-native strategy services и реалистичность чека выше 500 тыс. руб. в месяц.

## Полный контекст из raw

# RESURRECT SIGNAL — rocket-vibe-solutioning

## Meta
- source: triage/triage-2026-04-13-rocket-vibe-solutioning.md
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
- pipeline/raw/20260413T152737Z-rocket-vibe-solutioning.md

## Classification
signal, new case candidate

## Decision
Создать новый case: `pipeline/cases/ai-native-solutioning-consulting-operator/`.

## Why
Сигнал выглядит не как очередной AI app builder, а как более конкретная модель AI-native pre-sales and strategy operator: market research, competitor tracking, GTM guidance, product strategy и solution design продаются как более дешёвая альтернатива классическому consulting layer.

Это важно по двум причинам:
- wedge смещён выше по value chain, ближе к budget owner и problem framing, а не только к code generation;
- если такой слой закрепится, вокруг него почти неизбежно появятся repeatable service packages: discovery, ICP and GTM definition, product scoping, competitive intelligence, ongoing planning и human QA/escalation.

## Triage note
Дальше проверить, это единичный startup positioning signal или начало более широкой категории AI-native solutioning / strategy operators. Имеет смысл искать аналоги, pricing/engagement model, признаки enterprise uptake и границу между consulting, research copilot и app-generation workflows.

```
