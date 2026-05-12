## 2026-04-23 02:17 MSK — Program 4 / Demand Validation
- Stage: P4 Demand Validation
- Case: rapidclaims-geo-expand-v2
- Change: создан 02-demand.md
- Demand score: 5.9/10
- WTP score: 6.8/10
- RU readiness: 4.7/10
- Profit Gate: PASS только в enterprise-assisted сценарии, FAIL в SMB self-serve
- Decision: not rejected at P4, кейс оставлен в пайплайне как узкий enterprise vertical AI
- Notes: internal multi-demand endpoint timeout по ключам `медицинское кодирование`, `medical coding`, `revenue cycle automation`; Telegram-native RU signal не найден

## 2026-05-11 22:23 MSK — Program 5 / Unit Economics
- Stage: P5 Unit Economics
- Case: rapidclaims-geo-expand-v2
- Change: создан 04-economics.md
- Segment: regulated enterprise healthtech, AI-assisted medical coding и revenue-cycle automation
- MRR per client: 700 000 ₽
- COGS per client/month: 180 000 ₽
- Gross Margin: 74,3%
- Fully-loaded CAC: 1,79 млн ₽ base-case, 2,01 млн ₽ reported blended monthly slice
- LTV: 20,8 млн ₽
- Monthly churn used: 2,5%
- LTV/CAC: 11,6x
- CAC Payback: 3,4 мес
- Break-even: 15 клиентов по EBITDA 0, 16 клиентов для EBITDA 500 тыс. ₽/мес
- Decision: PASS на P5, кейс оставлен в пайплайне
- Notes: модель сходится только как high-touch regulated enterprise AI; ключевые риски остаются в локализации, интеграциях и длине procurement cycle
## 2026-05-13 00:14 MSK — Program 7 / Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: rapidclaims-geo-expand-v2
- Change: создан 06-verdict.md
- Verdict: NEAR-PASS
- Raw score: 102/150
- Normalized score: 68/100
- Moat score: 11/25
- company_ebitda_potential_rub_month: 1 442 497 ₽/мес
- clients_to_500k_ebitda: 16
- months_to_500k_ebitda: 24
- Decision: case moved to pipeline/rejected/ как NEAR-PASS
- Notes: сильная unit economics и median EBITDA-gate не компенсируют weak moat, evidence penalty и compliance-heavy GTM.
