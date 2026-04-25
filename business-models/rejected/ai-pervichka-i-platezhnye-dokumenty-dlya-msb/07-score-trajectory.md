## 2026-04-25 — P4 Demand Validation
- stage: P4 Demand Validation
- summary: Спрос подтверждён на уровне MEDIUM; strongest wedge не “чистый OCR”, а workflow первички + ЭДО + платёжки для аутсорсеров и document-heavy МСБ.
- demand_score: MEDIUM
- market_size: TAM РФ ~8,3 млрд ₽, preferred SAM ~5,0 млрд ₽, SOM Y1 ~50 млн ₽.
- profit_gate: PASS, достижим через аутсорсеров и embedded/white-label.
- decision: PASS_TO_NEXT_STAGE
- artifact: pipeline/cases/ai-pervichka-i-platezhnye-dokumenty-dlya-msb/02-demand.md

## 2026-04-25 — P5 Unit Economics
- stage: P5 Unit Economics
- summary: Fully-loaded CAC оказался слишком высоким для ARPU 25k ₽/мес; при 50 клиентах EBITDA остаётся глубоко отрицательной, а LTV/CAC не дотягивает до investment-grade.
- unit_economics_score: FAIL
- blended_fully_loaded_cac: 499000 ₽
- ltv: 780000 ₽
- ltv_cac: 1.56x
- cac_payback: 20.0 months
- contribution_margin: 78%
- break_even_clients: 329
- profit_gate: FAIL
- decision: REJECTED
- artifact: pipeline/cases/ai-pervichka-i-platezhnye-dokumenty-dlya-msb/04-economics.md
