# 07-score-trajectory

## 2026-05-09 — P3 Demand Validation
- stage: P3-demand-validation
- analyst: branch-models-lead
- score_before: BRIEF
- score_after: PASS_WITH_RESERVATIONS
- trajectory: category-level search demand по транзакционному скорингу в РФ слабый, но production-demand на кредитные оценки и underwriting automation подтверждён данными Банка России; кейс остаётся живым за счёт сильного WTP и проходящего profit gate в SaaS/API и enterprise-сценариях.
- key_deltas:
  - По multi-demand все точные формулировки (`кредитный скоринг`, `транзакционный скоринг`, `скоринг мфо`) остались в зоне LOW, поэтому чисто category-led inbound thesis не подтверждён.
  - При этом Банк России сообщил, что количество кредитных оценок, предоставленных МФО со стороны БКИ, выросло в 1,6 раза за 2025 год, что подтверждает реальный рыночный usage scoring-инструментов.
  - Появился доказанный willingness to pay: публичные цены конкурентов лежат от 140 ₽ за отчёт до 99-499 €/мес и 4 485-7 485 $/год.
  - Top-down и bottom-up оценка рынка РФ сошлись близко: SAM ≈ 181-188 млн ₽, SOM Y1 ≈ 7,2 млн ₽.
  - Profit gate провален только в commodity per-report motion; в mid-market SaaS/API, hybrid и enterprise white-label сценариях company EBITDA > 500k ₽/мес достижима.
  - Итоговый статус смещён в PASS WITH RESERVATIONS: рынок не массовый, но инвестиционно интересен как узкий B2B infrastructure wedge.
- artifact: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-tranzaktsionnyi-skoring-dlya-mfo-i-bankov/02-demand.md

## 2026-05-09 — P5 Unit Economics
- stage: P5-unit-economics
- analyst: branch-models-lead
- score_before: PASS_WITH_RESERVATIONS
- score_after: REJECTED
- trajectory: при реалистичном enterprise/regtech GTM кейс оказался не сломан по CAC и LTV/CAC, но сломан по fixed-cost floor и позднему breakeven; на уровне фонда это делает standalone-компанию неинвестиционной.
- key_deltas:
  - Fully-loaded CAC пересчитан по enterprise/regulatory логике и составил **1 049 000 ₽** на нового платящего клиента, что существенно выше ballpark-оценки intake, но остаётся правдоподобным для pilot-heavy fintech sales.
  - LTV рассчитан через gross profit и churn 2,5% в месяц, итог **4,4 млн ₽**, поэтому **LTV/CAC = 4,2x** и сам по себе канал привлечения не является причиной отказа.
  - **CAC Payback = 6,6 мес** по формуле CAC / MRR, то есть GTM экономически терпим.
  - Основной провал найден в cost base: steady-state fixed costs достигли **6,8 млн ₽/мес**, а contribution на клиента при blended MRR **160 тыс. ₽** составил только **110 тыс. ₽/мес**.
  - Реальный break-even получился на уровне **62-64 клиентов**, а при **50 клиентах EBITDA остаётся отрицательной: около -1,3 млн ₽/мес**, что напрямую нарушает Profit Gate программы.
  - До operating breakeven компании нужно **≈95-110 млн ₽** капитала, при том что адресуемый рынок, оценённый на P3, остаётся сравнительно узким.
  - Статус кейса ухудшён с PASS_WITH_RESERVATIONS до **REJECTED**: продукт может жить как niche infra-vendor или модуль в большом risk stack, но как standalone venture-scale актив не проходит.
- artifact: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-tranzaktsionnyi-skoring-dlya-mfo-i-bankov/04-economics.md