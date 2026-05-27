# 07-score-trajectory

```yaml
- date: 2026-05-12
  stage: P5
  analyst: branch-models-lead
  change: created
  scores:
    demand: 3.4
    unit_economics: 4.2
    moat: 2.8
    market: 3.1
    founder_fit: 2.5
    investability: 3.5
  summary:
    previous_status: CONDITIONAL_PASS at demand stage
    current_status: PASS at unit economics stage
    rationale:
      - unit economics собираются только в enterprise/mid-market GTM с чеком около 500K ₽ MRR
      - fully-loaded CAC после нормализации до 656K ₽ остаётся в enterprise benchmark
      - LTV/CAC 23.8x и payback 1.3 месяца проходят investment-grade пороги
      - break-even достигается на 18 клиентах, EBITDA при 50 клиентах существенно выше 500K ₽/мес
      - основной риск смещается из economics в market narrowness, long sales cycle и implementation-heavy delivery

- date: 2026-05-12
  stage: P6A
  analyst: branch-models-lead
  change: appended
  scores:
    investability: 3.9
    capital_efficiency: 4.1
    downside_resilience: 3.4
  summary:
    previous_status: PASS at unit economics stage
    current_status: PASS_WITH_RESERVATIONS pending final verdict
    rationale:
      - PnL подтверждает ранний EBITDA break-even на 18 клиентах, в base-case уже к M5
      - startup_capital_to_bep_rub выглядит умеренным для enterprise GTM, около 4.45 млн ₽ в base и 15.88 млн ₽ в pessimistic
      - при 50 клиентах EBITDA остаётся существенно выше mandatory gate 500K ₽/мес во всех рабочих сценариях
      - экономическая прочность держится только при high-ACV positioning и контроле implementation-heavy delivery
      - главный residual risk не в математике, а в узости рынка и зависимости от enterprise sales execution

- date: 2026-05-27
  stage: P7
  analyst: branch-models-lead
  change: rewritten_with_append
  scores:
    unit_economics: 20
    ebitda_potential: 19
    market_demand: 10
    moat: 11
    execution_risk: 17
    gtm_realism: 20
    normalized_score: 65
  summary:
    previous_status: PASS_WITH_RESERVATIONS pending final verdict
    current_status: NEAR-PASS routed to rejected bucket
    rationale:
      - raw total по rubric 6x25 составил 97 из 150, нормализованный итог 65 из 100
      - criterion #3 capped at 10 из 25, потому что в demand-файле нет строки Sources T1/T2/T3 и сработал default penalty
      - moat остаётся слабым, 9 из 21 по 7-factor framework, потому что у кейса нет network effects и локального distribution moat
      - company_ebitda_potential_rub_month проходит gate, но investment margin of safety ломается из-за слабого прямого спроса и price compression risk
      - комитет переводит кейс в near-pass и ждёт 3-5 локальных платящих enterprise pilot-to-production кейсов для возврата к approve review
```
