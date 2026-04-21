# 07-score-trajectory

## 2026-04-22 02:02 MSK — P4 Demand Validation
- stage: Demand Validation
- case: norm-ai-geo-expand-v2
- decision: REJECTED
- demand: LOW
- profit_gate: FAIL
- score_trajectory:
  - market_demand: 2/5
  - willingness_to_pay: 2/5
  - market_size_rf: 2/5
  - profitability_path: 1/5
  - total_after_p4: 7/20
- rationale:
  - mandatory multi-demand endpoint по всем релевантным запросам дал LOW / score 0
  - в РФ подтвержден соседний AML/KYC спрос, но не enterprise policy-execution category уровня Norm Ai
  - SAM РФ ограничен low-hundreds-millions ₽
  - EBITDA >= 500k ₽/мес не сходится ни в одном реалистичном monetization scenario
- next_step: move to pipeline/rejected/
