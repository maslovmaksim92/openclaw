# 07-score-trajectory

## 2026-04-19 — Program 4 Demand Validation
- stage: P4
- verdict: REJECTED
- summary: Demand API по всем релевантным ключам LOW; точечный enterprise WTP есть, но локальный рынок слишком узкий и labour-heavy, Profit Gate не проходит ни в одном сценарии монетизации.
- demand_api: LOW (`data labeling`=15, `RLHF`=18, `разметка данных для ИИ`=22, `оценка LLM`=26)
- market_view: узкий B2B сервисный сегмент, сильная концентрация спроса, слабая пригодность для fund-level outcome
- profit_gate: FAIL
- decision_rule: DEMAND=LOW + Profit Gate FAIL => EARLY REJECT
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/expert-human-data-ops-for-ai-models-operator-v2/02-demand.md
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/expert-human-data-ops-for-ai-models-operator-v2/06-verdict.md
