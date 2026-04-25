[B2B-OPS] ServiceNow Autonomous Enterprise Service Operations — NEAR-PASS: 66/100 | EBITDA base=166К₽/мес через 12 мес | LTV/CAC=11,7x | Ключевое преимущество: глубокая интеграция в service workflows enterprise-клиента | Главный риск: weak moat и vendor/localization dependence в РФ.

# ServiceNow Autonomous Enterprise Service Operations — verdict

sector: B2B-OPS
status: near-pass
score: 66/100
case_slug: servicenow-autonomous-enterprise-service-operations-v2
date: 2026-04-25

## Stage 1. Intake
- Resurrection-кейс из triage от 2026-04-11: гипотеза про бизнес вокруг autonomous enterprise service operators на платформенном слое ServiceNow.
- Уже на intake было понятно, что кейс нельзя оценивать как массовый SaaS. Это enterprise transformation thesis с длинным циклом сделки.

## Stage 2. Demand validation
- Exact-demand в РФ по самостоятельному ярлыку низкий: `enterprise service management → LOW`, `ITSM → LOW`, `service desk → MEDIUM`.
- Сильный положительный сигнал, что adjacent budget line уже существует: hh.ru вакансии 33 / 467 / 547, публичные прайсы Jira Service Management, Freshservice и ITSM365 подтверждают willingness to pay.
- Итог P4: рынок живой только как enterprise/high-touch категория поверх существующего ITSM/service desk spend.

## Stage 3. Validation / solution fit
- Отдельного файла стадии validation в папке кейса не было; вывод reconstructed из demand и economics.
- Валидный wedge, это managed transformation + autonomous operations layer: routing, policy orchestration, approval automation, analytics и постоянная optimisation.
- Невалидный wedge, это дешёвый add-on SaaS или Telegram-first продукт.

## Stage 4. Unit economics
- customer_ltv_rub: **31 000 000 ₽**
- fully-loaded CAC: **2 655 231 ₽**
- LTV/CAC: **11.7x**
- CAC payback: **3.5 мес**
- contribution_margin_rub_month: **465 000 ₽/клиент/мес**
- fixed_costs_rub_month: **7 500 000 ₽/мес**
- break-even: **17 клиентов**
- startup_capital_to_bep_rub: **66 746 991 ₽**

Вывод: клиентская экономика investment-grade, но компания остаётся капиталоёмкой и execution-heavy.

## Stage 5. Critic finance and risk
- base M12 EBITDA: **165 625 ₽/мес**
- company_ebitda_potential_rub_month @50 clients: **15 750 000 ₽/мес**
- clients_to_500k_ebitda: **18**
- months_to_500k_ebitda: **13**
- Monte Carlo p10 / p50 / p90 EBITDA @M24: **-2.88 млн ₽ / 4.74 млн ₽ / 11.99 млн ₽**

Ключевой вывод P6: median-case живой, но downside tail тяжёлый из-за price compression, CAC volatility и vendor/localization risk.

## Stage 6. Final verdict
- **Вердикт:** 🟡 NEAR-PASS
- **Raw score:** 99/150
- **Normalized score:** 66/100
- **Решение:** кейс переводится в `rejected/` как near-pass, потому что economics не компенсирует weak moat и слабый локальный category pull.

## Rubric score
Source tier balance: T1=5, T2=9, T3=2, weighted=2.19. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование |
|---|----------|-----|------------|-------------|
| 1 | Unit Economics | 25 | 20 | LTV/CAC 11.7x и payback 3.5 мес дают investable economics на уровне клиента. |
| 2 | EBITDA Potential | 25 | 21 | EBITDA gate достигается в пределах 24 месяцев, но base M12 ещё почти на нуле. |
| 3 | Market + Demand | 25 | 14 | РФ-спрос идёт через adjacent ITSM/service desk budget, exact-category спрос слабый. |
| 4 | Moat | 25 | 10 | Proprietary data moat и regulatory moat не доказаны, защита держится в основном на embed и switching costs. |
| 5 | Execution Risk | 25 | 15 | Высокая зависимость от enterprise access, 152-ФЗ/data residency и foreign stack. |
| 6 | GTM Realism | 25 | 19 | GTM возможен как partner-led enterprise motion с named targets и ACV 0.9-1.5 млн ₽/мес. |

## 7-factor moat
| Фактор | Балл |
|---|---:|
| Network effects | 0 |
| Switching costs | 2 |
| Scale economies | 1 |
| Proprietary data / model advantage | 0 |
| Regulatory moat | 0 |
| Brand / distribution | 2 |
| Embedded workflow | 3 |

**Moat sum = 8/21, moat score = 10/25.**

## GTM: 10 named targets
1. **Сбер** — большой service ops контур; канал: executive intro / email CIO; контракт: 1.5 млн ₽/мес.
2. **ВТБ** — audit trail и approval pain; канал: ABM + отраслевое мероприятие; контракт: 1.3 млн ₽/мес.
3. **Т-Банк** — зрелые внутренние workflow; канал: founder-led intro; контракт: 1.2 млн ₽/мес.
4. **Ростелеком** — распределённая сервисная организация; канал: integrator partnership; контракт: 1.2 млн ₽/мес.
5. **МТС** — SLA-driven internal ops; канал: конференция + direct outreach; контракт: 1.1 млн ₽/мес.
6. **X5 Group** — SSC и back-office workflows; канал: email COO / Head of SSC; контракт: 950 тыс. ₽/мес.
7. **Магнит** — регионально распределённые service bottlenecks; канал: enterprise outbound; контракт: 900 тыс. ₽/мес.
8. **Северсталь** — зрелая digital-функция; канал: executive intro; контракт: 1.0 млн ₽/мес.
9. **Норникель** — высокий объём внутренних сервисных запросов; канал: email digital transformation owner; контракт: 1.0 млн ₽/мес.
10. **Газпром нефть** — тяжёлые approval flows и compliance; канал: partner-led outreach; контракт: 1.2 млн ₽/мес.

## Top-3 risks
1. **weak_moat_against_local_itsm** — probability high, impact high.
2. **sovereign_and_vendor_dependency** — probability high, impact high.
3. **services_creep_and_procurement_delay** — probability medium, impact high.

## Что доказать для approve
- 3-5 paid pilots в РФ с pilot-to-paid >=30%.
- Sovereign deployment path, закрывающий data residency и procurement objections.
- ARPA не ниже 750К ₽/мес и contribution margin не ниже 55% после внедрения.
- Не менее 2 референсных логотипов с измеримым эффектом по cycle time, SLA или cost-to-serve.

## Финальный тезис
Это хороший enterprise workflow thesis, но пока не investment-grade standalone opportunity для РФ. Правильный статус на 25 апреля 2026 года, это **NEAR-PASS** с повторной оценкой после локальных pilot→paid доказательств и подтверждения sovereign-friendly delivery path.
