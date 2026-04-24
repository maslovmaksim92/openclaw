# Score trajectory

## 2026-04-24 01:45 MSK — P5 Unit Economics
- case: `cleric-geo-expand-v2`
- stage: `P5-unit-economics`
- economics_view: `enterprise-grade ACV есть, но economics неинвестиционные`
- profit_gate: `FAIL for fund-level investment due to LTV/CAC 1.58x`
- market_view: `узкий enterprise infra сегмент с дорогим внедрением и высоким incumbent pressure`
- score_impact:
  - demand_quality: `0`
  - willingness_to_pay: `+1`
  - gross_margin_quality: `-2`
  - go_to_market_efficiency: `-3`
  - capital_intensity: `-2`
  - overall_delta: `-6`
- rationale:
  - средний локальный чек можно собрать только через high-touch enterprise motion;
  - COGS остаётся тяжёлым из-за solution engineering, support и secure deployment;
  - fully-loaded CAC после enterprise adjustment достигает ~5.8 млн ₽;
  - LTV/CAC = 1.58x и break-even наступает только около 38 клиентов;
  - для выхода в break-even нужен слишком большой burn и капитал для GEO-EXPAND кейса.
- artifact: `pipeline/cases/cleric-geo-expand-v2/04-economics.md`
