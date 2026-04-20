# 07-score-trajectory

## 2026-04-21 00:19 MSK — P4 Demand Validation
- stage: P4 Demand Validation
- outcome: REJECTED
- summary: mandatory early reject, потому что `multi-demand` вернул LOW, а profit gate не проходит ни в одном из проверенных monetization сценариев.
- demand_signal: LOW
- profit_gate: FAIL
- notes:
  - global WTP подтверждён, но локальный buyer pull в РФ слабый;
  - в РФ есть дешёвые Telegram/leadgen substitutes с ценами 1 250–10 000 ₽/мес;
  - service-led economics не дают EBITDA >= 500 000 ₽/мес.
