[FINTECH] 1C RPD Fintech v2 — NEAR-PASS: 65/100 | EBITDA base=11К₽/мес через 24 мес | LTV/CAC=12.4x | Ключевое преимущество: подтверждённый локальный WTP внутри 1С-экосистемы | Главный риск: модель не даёт 500К₽ EBITDA в base за 24 мес.

# verdict.md

sector: FINTECH
status: rejected
result: near-pass
score: 65/100
case_slug: 1c-rpd-fintech-v2
updated_at: 2026-04-21 06:34 MSK

## Stage 1 — Intake (01-intake.md)
- Кейc создан как resurrect standalone candidate из triage-сигнала по AI-автоматизации бухгалтерской первички внутри 1С.
- Исходный тезис: локальная категория уже коммерциализирована в РФ, поэтому кейс нужно прогнать через полный P3→P7, даже если он концептуально пересекается с общим accounting-document-processing thesis.
- Новый slug: `1c-rpd-fintech-v2`.

## Stage 2 — Validation (02-validation.md)
- Файл `02-validation.md` в кейсе отсутствует.
- В качестве фактической validation-основы использован следующий доступный артефакт: `02-demand.md`.

## Stage 3 — Demand (02-demand.md, фактически demand-stage)
- Спрос в РФ оценён как `MEDIUM-HIGH`.
- Публичный прайс 1С подтверждает willingness-to-pay до `3 000 000 ₽/год` за high-volume пакеты распознавания первички.
- hh-прокси показывает стоимость ручной обработки первички на уровне `80-140 тыс. ₽/мес`, что поддерживает ROI-thesis.
- Preferred SAM: `1.575 млрд ₽`, SOM Y1: `45 млн ₽`.
- Source tier balance: `T1=7, T2=4, T3=0`, weighted `2.64`.

## Stage 4 — Economics (04-economics.md)
- Базовый recurring чек: `125 000 ₽/мес`, setup fee `350 000 ₽`.
- COGS на клиента: `55 000 ₽/мес`, gross profit `70 000 ₽/мес`, `GM=56.0%`.
- `customer_ltv_rub = 4 666 667 ₽`, `CAC = 375 000 ₽`, `LTV/CAC = 12.4x`.
- `contribution_margin_rub_month = 60 000 ₽`, `fixed_costs_rub_month = 3 031 000 ₽/мес`.
- Break-even: `50.5` клиентов, ориентир `M24`, `startup_capital_to_bep_rub ≈ 32.5 млн ₽`.

## Stage 5 — Critic (05-critic.md)
- Base-case в 12 месяцев остаётся глубоко отрицательным по EBITDA, а на `M24` даёт лишь `11 239 ₽/мес`.
- Sensitivity и Monte Carlo показывают широкий downside: `p10 EBITDA @M24 = -2.06 млн ₽/мес`, `p50 = 11 239 ₽/мес`, `p90 = 853 584 ₽/мес`.
- Главные риски: кастомный delivery вместо productized rollout, price compression от 1С/крупных платформ, platform/vendor risk, data residency и санкционные ограничения.
- Competitor-thesis: category реальна, но value capture поверх 1С остаётся слабо защищённым.

## Stage 6 — Verdict (06-verdict.md)
- Финальный статус: **NEAR-PASS / rejected-folder**.
- Score rubric: `65/100`.
- Причина: рынок и unit economics на клиента сильные, но бизнес не проходит главный approve-gate по прибыли компании в base-сценарии.
- При `50` клиентах `company_ebitda_rub_month ≈ -31 000 ₽/мес`; `500К₽ EBITDA` достигаются только примерно при `59-60` клиентах, то есть вне допустимого порога `<=50` и `<=24 мес`.

## Инвесткомитет: краткий вывод
Это сильный локальный vertical operator thesis для 1С-heavy backoffice automation, но пока не venture-grade approve. Чтобы перейти в approve-zone, нужно доказать более высокий ARPA, более низкие fixed costs и repeatable 1С-channel motion, который выводит компанию на `company_ebitda_rub_month >= 500К₽/мес` при `40-45` клиентах.

## GitHub path
- rejected/1c-rpd-fintech-v2/verdict.md
