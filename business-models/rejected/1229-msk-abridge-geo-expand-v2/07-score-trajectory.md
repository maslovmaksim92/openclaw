# 07-score-trajectory

## 2026-04-20 07:27:23 MSK — P3 Demand Validation
- stage: P3
- signal: demand_validation
- score_before: 0
- score_after: -25
- verdict_delta: moved_to_rejected
- rationale:
  - direct demand API for `ambient clinical documentation` in RU returned LOW
  - RU proxy demand exists for broader medical documentation, but not for standalone ambient scribe category
  - Profit Gate failed across solo, SMB clinic, and enterprise monetization scenarios
  - case rejected at demand stage per rule: DEMAND=LOW and Profit Gate FAIL
