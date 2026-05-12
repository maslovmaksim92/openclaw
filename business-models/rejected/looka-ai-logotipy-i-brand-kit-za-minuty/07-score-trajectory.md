# Score trajectory

## 2026-05-11 — Program 4 Demand Validation
- Case: `looka-ai-logotipy-i-brand-kit-za-minuty`
- Stage result: `PASS TO NEXT STEP`
- Demand API: `LOW`, score `15/100`
- Key reason: явный поисковый интент в РФ есть, WTP подтверждён публичными ценами прямых конкурентов, buyer base большой за счёт новых МСП, seller-экономики и заявок на товарные знаки, а Profit Gate достижим в PLG и white-label сценариях.
- Profit Gate: `ACHIEVABLE`, но не в дешёвом logo-only SKU; нужен product-led upsell или B2B white-label.
- Suggested score trajectory:
  - Market demand: 6/10
  - Willingness to pay: 7/10
  - Competition intensity: 4/10
  - Monetization quality: 7/10
  - Overall after P4: 6/10
- Artifact: `02-demand.md`

## 2026-05-12 — Program 5 Unit Economics
- Case: `looka-ai-logotipy-i-brand-kit-za-minuty`
- Stage result: `REJECTED`
- Key reason: fully-loaded CAC оказался слишком тяжёлым для low-ARPA self-serve модели, а churn для подписочного brand-kit сегмента съедает LTV.
- Core metrics:
  - Blended MRR per active client: `990 ₽/мес`
  - Gross Margin: `78.0%`
  - Fully-loaded CAC: `8 474 ₽`
  - Monthly churn benchmark: `6.4%`
  - LTV: `12 066 ₽`
  - LTV/CAC: `1.42x`
  - CAC Payback: `8.6 мес`
  - Contribution Margin: `46.7%`
  - Break-even: `11 255 активных клиентов`
- Profit Gate:
  - EBITDA `500K+/мес` на базе `50 клиентов`: `FAIL`
  - LTV/CAC `< 3:1`: `FAIL` для investment grade
- Updated score trajectory:
  - Market demand: 6/10
  - Willingness to pay: 6/10
  - Competition intensity: 3/10
  - Monetization quality: 3/10
  - Unit economics quality: 2/10
  - Overall after P5: 4/10
- Artifacts:
  - `04-economics.md`
  - `06-verdict.md`
