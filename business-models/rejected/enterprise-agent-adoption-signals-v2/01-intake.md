---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-enterprise-agent-adoption-signals.md
created: 2026-04-20T10:27:00+03:00
original_verdict: triage/triage-2026-04-10-enterprise-agent-adoption-signals.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `enterprise-agent-adoption-signals-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — enterprise-agent-adoption-signals

## Meta
- source: triage/triage-2026-04-10-enterprise-agent-adoption-signals.md
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
2026-04-10

## Inputs
- pipeline/raw/radar-web-2026-04-10-1835.md

## Classification
signal, but duplicate cluster

## Decision
Не создавать новый case.
Привязать сигнал к существующему case: `pipeline/cases/openclaw-contours-agency/`.

## Why
Оба сигнала описывают не отдельную SMB/service business model, а усиление общего рынка AI-agent adoption:
- OpenAI указывает на быстрый рост enterprise AI и company-wide agent rollout.
- Anthropic указывает на очень быстрое вырастание coding-agent demand в крупный revenue stream.

Для текущего pipeline это скорее supporting evidence, что рынок агентных внедрений и managed-agent services ускоряется, чем самостоятельный case-кандидат.

## Triage note
Использовать позже как evidence/demand support для `openclaw-contours-agency`, если будет отдельный validation block.
Новый case не открывать, потому что сигнал adoption-heavy и слишком общий относительно уже открытых service-oriented cases.

```

