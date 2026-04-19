# 07-score-trajectory

## 2026-04-19 18:35:04 MSK — P4 Demand Validation
- Stage: P4
- Outcome: CONDITIONAL PASS
- Demand API: LOW (score 18)
- Profit Gate: PASS
- Key update: подтверждены 3+ реальных конкурента с ценами, buyer budget и RF market sizing; ранний reject не применён.
- Artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-accounting-document-processing-operator-v2/02-demand.md

## 2026-04-19 18:39:00 MSK — P5 Unit Economics
- Stage: P5
- Outcome: FAIL
- Economics verdict: REJECTED
- Key update: realistic fully-loaded CAC = 406 486 ₽, LTV/CAC = 2,46x, CAC Payback = 13,5 мес, EBITDA at 50 clients = -4,93 млн ₽/мес, break-even = 297 клиентов.
- Decision: кейс остановлен на P5 и переведён в rejected.
- Artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-accounting-document-processing-operator-v2/04-economics.md
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-accounting-document-processing-operator-v2/06-verdict.md
