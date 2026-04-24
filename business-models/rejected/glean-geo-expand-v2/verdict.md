[GEO-EXPAND] Glean geo-expand v2 — REJECTED: 58/100 | EBITDA base=81К₽/мес через 24 мес | LTV/CAC=7,5x | Ключевое преимущество: security-first federated search для сложных enterprise-контуров | Главный риск: pricing/CAC pressure ломает median-case.

# Glean geo-expand v2 — полный verdict

sector: GEO-EXPAND
status: REJECTED
score: 58/100
raw_score: 87/150
date: 2026-04-24

## 01-intake
- Кейс переоткрыт как `resurrect` из старого сигнала `glean-geo-expand`.
- Основание rerun, обновлённая аналитическая система P4→P7 и необходимость оценить тему как standalone candidate.
- Контекст: не классифицировать как duplicate автоматически, а прогнать заново по полному пайплайну.

## 02-demand
- Итог P4: **CONDITIONAL PASS**.
- Массовый search-demand по RU core-keyword формально **LOW**, но enterprise hiring demand по RAG/internal search подтверждён вакансиями Ростелеком ИТ, ВкусВилл, Уралсиб, Т-Банк и др.
- Bottom-up SAM РФ: **2.36 млрд ₽**, SOM Y1: **35.4 млн ₽**, SOM Y3: **141.6 млн ₽**.
- Источники по tier-балансу: **T1=17, T2=4, T3=2**, weighted **2.65**, penalty к criterion #3 отсутствует.

## 03-solution
- Реальный wedge, не “поиск ради поиска”, а **secure enterprise knowledge access and internal assistant layer**.
- Рабочий ICP: банки, финтех, телеком, крупный ритейл, IT-heavy enterprise, где есть 3-5+ knowledge systems и дорогой внутренний search latency.
- Наиболее реалистичный GTM, pilot-led motion с SSO, ACL, auditability и KPI-driven rollout, а не self-serve SaaS.
- Ключевой risk: продукт легко схлопывается в feature поверх Microsoft stack, helpdesk knowledge base или internal RAG build.

## 04-economics
- MRR на клиента: **220 000 ₽/мес**.
- COGS на клиента: **110 000 ₽/мес**.
- GM: **50.0%**.
- customer_ltv_rub: **8 800 000 ₽**.
- CAC fully-loaded: **1 176 000 ₽**.
- LTV/CAC: **7.5x**.
- CAC payback: **5.3 мес**, gross profit payback: **10.7 мес**.
- contribution_margin_rub_month: **92 000 ₽/клиент/мес**.
- fixed_costs_rub_month: **4 000 000 ₽/мес**.
- EBITDA break-even: **37 клиентов**, для 500k EBITDA нужно **41 клиент**.
- Startup capital to break-even: **38.0-41.6 млн ₽** в base/pessimistic диапазоне.

## 05-critic
- Sensitivity @M24: base EBITDA **81 424 ₽/мес**, CAC x2 -> **-1 151 503 ₽/мес**, churn x2 -> **-307 834 ₽/мес**, price -30% -> **-2 367 430 ₽/мес**.
- Monte Carlo Lite: p10 EBITDA **-2 504 226 ₽/мес**, p50 EBITDA **81 424 ₽/мес**, p90 EBITDA **2 829 032 ₽/мес**.
- Rule triggered: median-case не проходит обязательный gate `company_ebitda_rub_month >= 500 000 ₽/мес`.
- Bottom line P6: кейс математически жив только у верхней границы распределения и требует структурного сдвига по ARPU/CAC/GM.

## 06-verdict

### Итог инвесткомитета
- **Вердикт:** ❌ REJECTED
- **Normalized score:** **58/100**
- **Raw score:** **87/150**
- **Причина:** base-case не даёт EBITDA 500k+ за 24 месяца, а moat слабый и GTM дорогой.

### Оценка
Source tier balance: T1=17, T2=4, T3=2, weighted=2.65. Penalty applied: -0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование |
|---|----------|-----|------------|-------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «LTV/CAC = 7.5x», но GM лишь «50.0%» и gross payback «10.7 мес». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 10 | Base «EBITDA @M24 ... 81 424 ₽/мес», то есть далеко ниже порога. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | Hiring demand есть, но multi-demand endpoint по core-keyword всё ещё «LOW». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Enterprise wedge реален, но дистрибуция и defensibility против incumbents слабые. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 13 | Длинный sales cycle, high CAC, 152-ФЗ и санкции создают тяжёлый execution profile. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | 10 named targets и pilot motion есть, но CAC 1.176 млн ₽ слишком тяжёлый. |

**Normalized score = round((87 × 100) / 150) = 58/100.**

### 7-factor Moat Framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Нет прямых сетевых эффектов. |
| Switching costs | 2 | Интеграции, ACL и rollout создают удержание. |
| Scale economies | 1 | Некоторое удешевление с объёмом есть, но services-heavy слой остаётся. |
| Proprietary data / model advantage | 1 | Уникальный локальный dataset не доказан. |
| Regulatory moat | 1 | Compliance важен, но не даёт уникального преимущества. |
| Brand / distribution | 1 | Локальный бренд и канал слабее крупных вендоров. |
| Embedded workflow | 3 | При успехе продукт встраивается глубоко в daily workflow. |

**Moat sum = 9/21, Moat score = 11/25.**

### FULL business process
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Mapping целевых enterprise accounts | SDR / founder | CRM, HH, market maps | 2 ч | 2 200 | Низкий |
| 2 | Outbound / intro через warm network и ABM | founder / AE | email, Telegram, calls | 2 ч | 3 600 | Низкий |
| 3 | Discovery по knowledge pain | AE / founder | meet, deck, CRM | 1.5 ч | 6 000 | Средний |
| 4 | Audit knowledge landscape и systems inventory | solutions | checklist, workshops | 4 ч | 18 000 | Низкий |
| 5 | Demo / pilot scoping | AE + solutions | demo, ROI sheet | 3 ч | 12 000 | Средний |
| 6 | Security / legal / procurement review | AE + product | docs, DPA, infosec pack | 4 ч | 16 000 | Низкий |
| 7 | Pilot 6-10 недель | solutions + CSM | sandbox, connectors, support | 28 ч | 110 000 | Средний |
| 8 | Production onboarding | CSM + engineer | SSO, ACL, connectors | 24 ч | 95 000 | Средний |
| 9 | Training и rollout | CSM | workshops, runbooks | 8 ч | 28 000 | Средний |
| 10 | Expansion в соседние функции | AE + CSM | QBR, success metrics | 4 ч | 14 000 | Средний |

### Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 8 800 000 ₽ |
| contribution_margin_rub_month | 92 000 ₽/клиент/мес |
| company_ebitda_rub_month @M24 base | 81 424 ₽/мес |
| company_ebitda_potential_rub_month | 500 000+ ₽/мес только после ~41 клиента |
| clients_to_500k_ebitda | 41 |
| months_to_500k_ebitda | >24 мес |
| startup_capital_to_bep_rub | 38 029 969 ₽ base |

### Команда
| Роль | Нужно чел. | FOT fully-loaded ₽/мес |
|---|---:|---:|
| CEO / founder | 1 | 585 000 |
| AE / enterprise sales | 1 | 416 000 |
| SDR / research | 1 | 234 000 |
| Solutions engineer | 1 | 416 000 |
| Backend / integrations engineer | 1 | 442 000 |
| ML / product engineer | 1 | 494 000 |
| CSM / implementation lead | 1 | 299 000 |
| Support / ops | 1 | 221 000 |
| **Итого** | **8** | **3 107 000 ₽/мес** |

### GTM: 10 named targets
1. Ростелеком ИТ — уже строит «умный поиск (RAG)»; канал: email + enterprise AI event; чек: 250 000 ₽/мес.
2. Т-Банк — RAG / AI Platform уже в найме; канал: founder-led intro; чек: 300 000 ₽/мес.
3. Банк Уралсиб — regulated knowledge workflows; канал: email CIO; чек: 250 000 ₽/мес.
4. ВкусВилл — публично упоминает поиск по базе знаний и ассистентов; канал: retail-tech conference; чек: 220 000 ₽/мес.
5. Газпромбанк — LLM/RAG/Agents уже в roadmap; канал: партнёрство с интегратором; чек: 300 000 ₽/мес.
6. ФИНАМ — AI/RAG-найм подтверждает pain; канал: email CTO; чек: 220 000 ₽/мес.
7. Арнест ЮниРусь — RAG-специалист и distributed ops; канал: ABM outreach; чек: 200 000 ₽/мес.
8. МосТрансПроект — AI/RAG в цифровизации; канал: email руководителю цифровизации; чек: 180 000 ₽/мес.
9. SOKOLOV — retail knowledge pain и RAG hiring signal; канал: retail-tech event; чек: 200 000 ₽/мес.
10. DatsTeam — есть knowledge management pain; канал: email COO; чек: 180 000 ₽/мес.

### Top-3 risks
| Риск | Probability | Impact |
|---|---|---|
| weak_moat_and_price_compression | high | high |
| enterprise_cac_and_sales_cycle | high | high |
| compliance_llm_dependency | med | high |

### LTV Upside Calculator
| Рычаг | Текущий уровень | Цель |
|---|---:|---:|
| ARPA | 220 000 ₽/мес | 260 000-300 000 ₽/мес |
| CAC | 1 176 000 ₽ | <= 900 000 ₽ |
| GM | 50.0% | 55-60% |
| New clients / month | 2 | 3+ |
| Monthly churn | 1.25% | <= 1.0% |

## Финальный вывод
Кейс показывает реальную enterprise-боль и рабочую клиентскую unit economics, но не даёт фондового профиля возврата в реалистичном base-case. Поэтому статус, **REJECTED**.
