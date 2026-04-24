# Score trajectory

## 2026-04-24 02:47 MSK — P4 Demand Validation
- case: `superdial-insurer-calls-geo-expand-v2`
- stage: `P4-demand-validation`
- demand: `LOW exact-demand / MEDIUM only in broad DMS adjacency`
- profit_gate: `FAIL for self-serve and mid-market; CONDITIONAL FAIL for enterprise pivot`
- market_view: `adjacent budget exists, but standalone insurer-call category too weak for РФ`
- score_impact:
  - demand_quality: `-2`
  - willingness_to_pay: `-1`
  - market_size: `-1`
  - go_to_market_complexity: `-2`
  - overall_delta: `-6`
- rationale:
  - multi-demand по insurer-call и verification ключам в РФ дал LOW;
  - большой контур ДМС существует, но он не равен addressable рынку payer-call automation;
  - публичные competitor prices показывают commoditized voice layer, а не high-ACV workflow category;
  - путь к EBITDA > 500K ₽/мес требует product pivot за пределы текущего кейса.
- artifact: `pipeline/cases/superdial-insurer-calls-geo-expand-v2/02-demand.md`
