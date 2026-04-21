# 07-score-trajectory

## 2026-04-21 15:54 MSK — P4 Demand Validation
- stage: P4 Demand Validation
- case: `langfuse-geo-expand-v2`
- decision: **REJECTED (early)**
- score_trajectory:
  - demand: **20/100**
  - market_size: **32/100**
  - monetization: **18/100**
  - profit_gate: **FAIL**
  - overall_after_p4: **24/100**
- rationale:
  - mandatory endpoint по `Langfuse` вернул LOW, несмотря на умеренный инженерный след
  - comparable pricing подтверждает WTP глобально, но не дает достаточной ценовой власти в РФ
  - все проверенные сценарии монетизации не дают надежного пути к EBITDA 500 тыс. ₽/мес
- next_action: переместить кейс в `pipeline/rejected/langfuse-geo-expand-v2/`
