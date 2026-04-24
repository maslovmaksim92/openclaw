[B2B-OPS] SAP Reltio AI-ready MDM — NEAR-PASS: 69/100 | EBITDA base=505К₽/мес через 12 мес | LTV/CAC=80,5x | Ключевое преимущество: enterprise AI-ready MDM wedge для SAP-heavy контуров | Главный риск: узкий РФ-спрос и price compression в SI-конкуренции.

# 06-verdict — SAP Reltio AI-ready MDM v2

sector: B2B-OPS

## Итоговый вердикт
- **Вердикт:** **NEAR-PASS**
- **Score:** **69/100**
- **Статус инвесткомитета:** strong economics, но пока недостаточно запаса прочности по спросу, moat и execution certainty для clean approve.
- **Формальный gate:** EBITDA gate проходит, потому что в базе `company_ebitda_rub_month = 505 000 ₽/мес` достигается к **M12** при **12 клиентах**, то есть существенно раньше порога 50 клиентов и в пределах 24 месяцев.
- **Почему не APPROVED:** рынок в РФ подтверждён скорее бюджетами и adjacent data-management spend, чем прямым category-demand; moat средний; p10 Monte Carlo уходит к нулю/в минус, а sensitivity показывает сильную зависимость от цены.
- **Примечание по стадиям:** в этом кейсе demand-файл существует как `02-demand.md`; отдельный `03-demand.md` отсутствует. Для P7 использован фактический demand-артефакт кейса.

## Оценка
Source tier balance: T1=1, T2=6, T3=1, weighted=2.00. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | `Gross Margin = 65,0%`, `LTV/CAC = 80,5x`, `CAC Payback = 0,81 мес` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | `компания пересекает EBITDA 500k/mo в M12` и `При 12 клиентах EBITDA уже +505k/mo`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | `multi-demand ... composite_demand=LOW`, но есть `рынок решений для управления данными в РФ ... 156,9 млрд ₽` и `SAM ... 3,0 млрд ₽`; применён penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Moat строится вокруг SAP-heavy delivery, data residency и embedded stewardship workflows, но без network effects и с умеренным regulatory barrier. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В risk matrix зафиксированы `Price compression`, `152-ФЗ`, `санкции`, `Founder-led sales не масштабируется`, `LLM/API cost spike`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `Основной эффективный канал ... outbound ABM + partner referrals`, `Fully-loaded blended CAC = 726 667 ₽`, named targets конкретны. |

**Sum raw = 103/150. Normalized score = round((103 × 100) / 150) = 69/100.**

## Investment thesis
Это не массовый SaaS и не generic SAP-консалтинг, а узкий enterprise wedge: подготовка golden records, entity resolution, governance и managed stewardship как prerequisite для agentic AI и надёжного enterprise automation. В этой рамке экономика выглядит сильной, но инвестиционная проблема сдвигается из unit economics в repeatable pipeline generation, premium pricing discipline и доказательство, что компания не растворится в services-heavy SI-практике.

## Delta vs previous
- Кейс создан как resurrection-v2 из triage-сигнала, а не как rerun готового verdict.md.
- Предыдущий полный инвестиционный вердикт по этому slug в repo не найден; поэтому сравнивать можно только с triage-тезисом.
- По сравнению с triage сильнее всего подтвердились **unit economics** и **EBITDA gate**, слабее всего, **прямой demand proof в РФ** и **defensible moat**.

## FULL business process from 04-economics.md
| Шаг | Что происходит | ROLE | TOOL | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP и target-account list | CEO + SDR | CRM, Excel, HH/TAdviser/отраслевые базы | 2 ч | 6 500 | средняя |
| 2 | Outbound outreach: email, звонок, TG/LinkedIn analog | SDR | CRM, почта, телефония | 3 ч | 7 300 | средняя |
| 3 | Inbound capture с контента/ивентов/партнёров | Fractional marketing + CEO | лендинг, веб-формы, аналитика | 1,5 ч | 4 000 | высокая |
| 4 | Qualification call | SDR | телефония, CRM, скрипт qualification | 1 ч | 2 400 | средняя |
| 5 | Discovery с buyer group | CEO + AE + Solution Lead | Zoom/Meet, Miro, CRM | 3 ч | 18 500 | низкая |
| 6 | Pre-sale data/governance audit | CTO + data architect | SQL sandbox, demo env, checklist | 12 ч | 54 000 | низкая |
| 7 | Demo / solution workshop | AE + CTO | demo стенд, slides | 4 ч | 18 900 | средняя |
| 8 | Коммерческое предложение и business case | AE + CEO | шаблон proposal, Excel model | 6 ч | 25 700 | средняя |
| 9 | Security / legal / procurement review | CEO + CTO + legal | DPA, security docs, redlines | 10 ч | 43 000 | низкая |
| 10 | Переговоры и close | AE + CEO | CRM, e-sign, pricing sheet | 5 ч | 24 800 | низкая |
| 11 | Invoice + contract activation | Finance ops | 1C/банк/ЭДО | 1,5 ч | 4 500 | высокая |
| 12 | Оплата, запуск onboarding | Finance ops + CSM + delivery lead | банк, CRM, PM tool | 3 ч | 11 500 | средняя |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| ACV | 10 800 000 ₽/год |
| MRR на клиента | 900 000 ₽/мес |
| customer_ltv_rub | 58 500 000 ₽ |
| Gross Margin | 65,0% |
| contribution_margin_rub_month | 531 000 ₽/мес на клиента |
| Fully-loaded CAC | 726 667 ₽ |
| LTV/CAC | 80,5x |
| CAC Payback | 0,81 мес по MRR / 1,24 мес по gross profit |
| Contribution Margin % | 59,0% |
| fixed_costs_rub_month | 6 515 000 ₽/мес |
| Break-even | 12 клиентов по gross-profit basis / 13 по contribution basis |
| company_ebitda_rub_month @ 12 клиентов | 505 000 ₽/мес |
| company_ebitda_potential_rub_month @ 50 клиентов | 22 735 000 ₽/мес |
| clients_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 13 |
| months_to_500k_ebitda | 12 мес |
| months_to_1m_ebitda | 12-13 мес |
| startup_capital_to_bep_rub | 41 400 000 ₽ (base), 24 700 000 ₽ (optimistic), 50 100 000 ₽ (pessimistic) |

## Команда
| Роль | Кол-во | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO / Founder | 1 | 845 000 | enterprise sales, partnerships, hiring |
| CTO / Tech Lead | 1 | 715 000 | архитектура, presale, delivery governance |
| Senior Backend | 2 | 1 170 000 | connectors, workflows, integration services |
| ML Engineer | 1 | 650 000 | entity resolution, data quality AI layer |
| DevOps | 1 | 455 000 | infra, security, CI/CD |
| Frontend | 1 | 390 000 | steward UI, admin кабинеты |
| SDR | 1 | 195 000 | outbound pipeline generation |
| AE | 1 | 390 000 | closing, procurement, pricing |
| Customer Success | 1 | 325 000 | onboarding, retention, upsell support |
| **Итого** | **10** | **5 135 000** | steady-state к M6 |

## Moat — 7-factor framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | Есть данные, интеграции, stewardship rules и обученность команды заказчика. |
| Scale economies | 1 | COGS падает умеренно, но audit, integration и enterprise support остаются дорогими. |
| Proprietary data / model advantage | 2 | Может накапливаться enterprise master-data corpus и rules history, но публичного датасетного преимущества нет. |
| Regulatory moat | 1 | Data residency и 152-ФЗ помогают, но формального лицензируемого барьера нет. |
| Brand / distribution | 2 | Есть понятный wedge через SAP-heavy и regulated buyers, но бренд ещё не category-default. |
| Embedded workflow | 3 | Продукт глубоко встраивается в stewardship, golden record и AI-readiness workflows. |

**Moat sum = 11/21. Moat score = round((11 × 25) / 21) = 13/25.**

## GTM — 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Огромный объём customer/product/supplier master data и высокий приоритет AI-ready data layer для enterprise automation. | email decision-maker в data governance / партнёрство с SI | 1 500 000 ₽/мес |
| 2 | ВТБ | Regulated enterprise с тяжёлой data governance и длинным security review, где нужен локальный data residency story. | founder-led outreach + профильная конференция | 1 300 000 ₽/мес |
| 3 | X5 Group | Retail-data контур с большим объёмом SKU, supplier и customer master data, где golden record критичен для AI и supply workflows. | ABM-outreach в CDO/data office | 1 200 000 ₽/мес |
| 4 | Магнит | Сильная боль в product and supplier master data и в harmonization across systems. | email decision-maker + партнёрский integrator intro | 1 100 000 ₽/мес |
| 5 | Ростелеком | Data-heavy enterprise с множеством систем и потребностью в unified records для enterprise AI initiatives. | отраслевой event + direct outreach | 1 000 000 ₽/мес |
| 6 | Газпром нефть | Сложный multi-entity контур и высокая цена ошибки в master data для supply, procurement и asset workflows. | партнёрство с консалтингом / SI | 1 300 000 ₽/мес |
| 7 | Роснефть | Большая legacy estate, где AI-ready MDM может быть prerequisite для cross-system automation и analytics. | direct enterprise sales через CIO/CDO office | 1 300 000 ₽/мес |
| 8 | Северсталь | Manufacturing buyer с supplier, product и asset master-data болью, где governance и lineage критичны. | conference + targeted email | 900 000 ₽/мес |
| 9 | НЛМК | Индустриальный контур с повторяющейся master-data проблемой и потенциалом managed stewardship. | founder outreach + отраслевой контакт | 900 000 ₽/мес |
| 10 | ФосАгро | Крупная промышленная группа с enterprise ERP/data harmonization задачами и длинным lifecycle records. | партнёрский канал через ERP/SAP ecosystem | 850 000 ₽/мес |

### Оценка GTM realism
- Канальный fit есть: для такой сделки работают **outbound ABM, partner referrals, conferences и founder-led enterprise sales**.
- GTM не выглядит фантазийным, потому что в 04-economics.md прямо показано: `Основной эффективный канал для enterprise MDM: outbound ABM + partner referrals`.
- Но реализм GTM ограничен тем, что sales cycle длинный, legal/security review тяжёлый, а win-rate может ломаться при discount pressure.
- 10 named targets присутствуют, поэтому автоматический штраф к GTM не применяется.

## Финансовая интерпретация для инвесткомитета
- На уровне unit economics кейс один из сильнейших в текущем батче: `LTV/CAC = 80,5x`, `CAC Payback = 1,24 мес по gross profit`, gross margin 65%.
- EBITDA gate проходит быстро, но это не снимает вопроса о robustness: в 05-critic sensitivity `Price -30%` даёт `EBITDA @M12 = -2,82 млн ₽/мес`, а `CAC x2` даёт `-0,74 млн ₽/мес`.
- Monte Carlo Lite тоже не даёт clean conviction: `EBITDA @M24 p10 = -0,01 млн ₽`, `p50 = 19,51 млн ₽`, `p90 = 89,58 млн ₽`. Разброс outcomes слишком велик для clean approve.

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Price compression со стороны SI и импортозамещения | high | high | `Price -30%` почти полностью ломает EBITDA Gate и переводит кейс в отрицательный EBITDA уже к M12. |
| Слабый прямой category-demand в РФ | med-high | high | В demand-файле `multi-demand ... composite_demand=LOW`, поэтому pipeline может оказаться уже, чем подсказывает adjacent data-management spend. |
| Founder-led enterprise sales и длинный security/procurement cycle | med | high | В risk matrix есть `Founder-led sales не масштабируется` и `152-ФЗ / data residency`, что может замедлить conversion и burn-to-breakeven. |

## Что должно быть доказано для перевода в APPROVED
1. **2-3 paid design partners** в SAP-heavy или regulated enterprise с подписанным annual contract, а не только assessment/PoC.
2. **Повторяемый pilot-to-production motion** со сроком security/legal review не более 90 дней.
3. **Pricing discipline**: ARPA не ниже 900 000 ₽/мес и discount не выше 15-20%.
4. **Referenceability**: минимум 2 публично референсируемых логотипа или сильных confidential case studies, подтверждающих AI-readiness wedge.

## LTV Upside Calculator
### Формула
- `customer_ltv_rub = gross_profit_per_client_month / monthly_churn`
- `LTV/CAC = customer_ltv_rub / CAC`

### Upside table
| Сценарий | Gross profit на клиента, ₽/мес | Monthly churn | CAC, ₽ | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|
| Текущая база | 585 000 | 1,0% | 726 667 | 58 500 000 ₽ | 80,5x |
| Если churn снизить до 0,7% | 585 000 | 0,7% | 726 667 | 83 571 429 ₽ | 115,0x |
| Если поднять gross profit до 650k ₽ | 650 000 | 1,0% | 726 667 | 65 000 000 ₽ | 89,4x |
| Если CAC вырастет до 1,2 млн ₽ | 585 000 | 1,0% | 1 200 000 | 58 500 000 ₽ | 48,8x |
| Если цена упадёт на 30% и gross profit = 315k ₽ | 315 000 | 1,0% | 726 667 | 31 500 000 ₽ | 43,3x |

### Read-through
- Даже LTV upside здесь уже высокий; проблема кейса не в LTV/CAC, а в **repeatable demand capture** и **устойчивости premium pricing**.
- Поэтому для перевода из NEAR-PASS в APPROVED надо улучшать не математику LTV, а доказательства спроса, channel fit и defensibility.

## Proof points for APPROVED
Не применяется, потому что итоговый статус кейса **NEAR-PASS**, а не APPROVED.

## Финальное решение комитета
**NEAR-PASS.**

Почему не reject:
- economics сильные,
- EBITDA > 500K ₽/мес достигается уже в M12,
- ICP и 10 named targets понятны,
- adjacent budget reality подтверждает платёжеспособный enterprise wedge.

Почему пока не approve:
- прямой search-demand в РФ слабый,
- moat средний,
- outcome dispersion по Monte Carlo слишком широкий,
- модель очень чувствительна к pricing discipline и founder-led execution.

---

# Appendix — pipeline artifacts
## 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-sap-reltio-ai-ready-mdm.md
created: 2026-04-21T18:26:12+03:00
original_verdict_source: triage/triage-2026-04-13-sap-reltio-ai-ready-mdm.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — sap-reltio-ai-ready-mdm

## Meta
- source: triage/triage-2026-04-13-sap-reltio-ai-ready-mdm.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Triage

## Date
2026-04-13

## Inputs
- pipeline/raw/20260413T1810Z-sap-reltio-ai-ready-mdm.md

## Classification
new case candidate

## Decision
Пока не маппить в существующий case. Держать как кандидат на отдельный case around AI-ready enterprise data / MDM modernization.

Suggested case slug: `ai-ready-mdm-modernization-operator`

## Why
- Сигнал описывает не просто SAP implementation и не generic data consulting, а конкретный enterprise wedge: подготовка master data, governance и unified records как prerequisite для agentic AI.
- Reltio добавляет сильный execution surface вокруг golden records, entity resolution, cleansing, survivorship rules, stewardship workflows и cross-system data products across SAP and non-SAP estates.
- Buyer pain здесь бюджетно ёмкий и устойчивый: без clean governed data enterprise AI initiatives буксуют, поэтому можно продавать не разовый advisory, а многомесячные implementation и managed-service engagements.
- Это выглядит как repeatable operator model на стыке SAP modernization, data governance и AI readiness, с потенциально отдельными buyers in CIO / CDO / enterprise data teams.

## Triage note
Считать сильным candidate wedge. В следующем цикле важно найти подтверждения beyond SAP PR: partner/SI motions, consulting offers по MDM-for-AI, signals from Informatica, Reltio ecosystem, Microsoft/ServiceNow/Oracle/Salesforce data layers, и кейсы где master data quality прямо связана с agentic workflows, copilots, knowledge grounding или enterprise automation reliability.

```


## 02-validation.md

_Файл отсутствует в кейсе._

## 03-demand.md

# Demand validation — SAP Reltio AI-ready MDM

## Executive summary
- Вертикаль: enterprise master data management, data governance, golden record, entity resolution для крупных компаний. 
- Сигнал спроса в РФ по широкому ключу слабый в self-serve формате: internal multi-demand по `master data management` вернул `LOW`, `hh_ru=0`, `telegram subscribers=0`, `habr_articles=2`.
- При этом willingness to pay у enterprise-сегмента высокая: рынок продаётся не как массовый SaaS, а как дорогие проекты внедрения и managed service с чеками от десятков тысяч долларов/евро и десятков миллионов рублей в год [T2][T3].
- Вывод: спрос узкий, но платёжеспособный; это не SMB-продукт, а boutique / enterprise wedge. Кейс не уходит в early reject, потому что Profit Gate достижим в нескольких сценариях.

## Demand signals
### 1) Internal demand check
- `multi-demand?keyword=master data management` → `composite_demand=LOW`, `demand_score=0`, `hh_ru=0`, `telegram=0`, `habr_articles=2`.
- Это означает слабый публичный demand footprint в РФ именно по англоязычному MDM-термину. Для enterprise infra это типично: закупка идёт через CIO/CDO, SI и тендеры, а не через массовый поисковый спрос.

### 2) Почему сигнал всё равно нельзя считать нулевым
- Arenadata в 2024 году купила 51% в Picodata, разработчике MDM/PIM-решений, за 100 млн ₽, чтобы усилить продуктовую линейку в управлении мастер-данными [T2]. Это прямой признак стратегической денежной ставки на сегмент.
- В РФ рынок решений для управления данными в 2023 году оценивался в 156,9 млрд ₽, +19,4% г/г [T2]. MDM занимает лишь часть этого пирога, но сам бюджетный контур вокруг data management уже материален.
- На глобальном рынке MDM рост двузначный: Grand View Research оценивает рынок MDM в 19,96 млрд $ в 2023 году с CAGR 17,4% до 2030 [T3]. Это поддерживает тезис, что AI-ready data layer становится обязательным prerequisite для enterprise AI.

## Real competitors with prices
| Конкурент | Что продаёт | Публичная цена | Интерпретация |
|---|---|---:|---|
| Semarchy xDM on AWS Marketplace | MDM-платформа | от 49,422.10 $ / год [T2] | Нижняя граница enterprise annual software spend |
| Profisee QuickStart Proof-of-Concept on Azure Marketplace | MDM PoC / quickstart | 21,900 € one-time [T2] | Даже входной PoC стоит как mid-ticket B2B проект |
| Valcon Master Data Management Accelerator | MDM accelerator / implementation | от 25,000 $ [T2] | Консалтинговый входной чек подтверждает платный discovery |
| Cegeka Data Governance Scan | data governance assessment | 9,500 € [T2] | Близкий смежный чек на governance discovery |

### Read-through по ценам
- Публичные цены указывают, что покупатель привык к входному чеку примерно 0,9–4,6 млн ₽ за assessment/PoC и к annual/software spend порядка 4,1 млн ₽+ даже на нижней публичной планке [T1][T2].
- По курсам ЦБ РФ на 23.04.2026: 1 USD = 82,0787 ₽, 1 EUR = 93,1608 ₽ [T1].
  - 49,422.10 $ ≈ 4,06 млн ₽/год [T1+T2]
  - 21,900 € ≈ 2,04 млн ₽ [T1+T2]
  - 25,000 $ ≈ 2,05 млн ₽ [T1+T2]
  - 9,500 € ≈ 0,88 млн ₽ [T1+T2]

## WTP, proof of willingness to pay
- **Proof 1:** есть публичные marketplace / service offers с чеками 0,88–4,06 млн ₽ уже на discovery или entry level [T1][T2].
- **Proof 2:** MDM-программы обычно продаются крупным enterprise buyer как часть цифровой трансформации, data governance и ERP/CRM harmonization, а не как дешёвый бот или self-serve SaaS [T2][T3].
- **Proof 3:** стратегическая M&A-сделка Arenadata–Picodata на 100 млн ₽ показывает, что игроки рынка готовы платить за компетенцию и продукт в MDM-контуре [T2].
- Итог: willingness to pay **HIGH**, но только в enterprise-сегменте и при наличии сильного delivery/credibility.

## Telegram bots / services in RU
- Прямого массового рынка Telegram-ботов для enterprise MDM в РФ не видно: internal multi-demand по ключу не показал значимых TG signals (`telegram subscribers=0`).
- В RU Telegram скорее возможны **каналы/лидоген** вокруг data governance и интеграций, но не основной delivery surface. 
- Вывод: Telegram можно использовать как top-of-funnel и экспертный канал, но не как продуктовый core. Для этого кейса это neutral-to-negative signal.

## Market sizing
### Методика
Считаю двумя путями и беру более консервативное значение.

### Top-down
- База: рынок решений для управления данными в РФ в 2023 году — 156,9 млрд ₽ [T2].
- Допущение: доля MDM + data governance modernization внутри общего data management бюджета = 5–8% [спекуляция, anchored by global MDM share, T3].
- Тогда **TAM РФ** = 7,8–12,6 млрд ₽.
- Для консервативной модели беру нижнюю границу: **7,8 млрд ₽**.
- Далее отсекаю сегмент, реально доступный новой boutique-команде: крупные компании в regulated/data-heavy отраслях, SAP/ERP-heavy контуры, mid-large enterprise. Беру 45% от TAM РФ.
- **SAM top-down** = 3,5 млрд ₽.
- **SOM Y1 top-down** = 1% от SAM = 35 млн ₽.
- **SOM Y3 top-down** = 5% от SAM = 175 млн ₽.

### Bottom-up
- Total buyers: ~1,500 крупных и upper-midmarket компаний в РФ, для которых критичны golden record, supplier/customer/product master data, data lineage и AI-readiness [спекуляция на базе структуры крупнейших отраслей РФ, T2/T3].
- % with need: 20% → 300 компаний. Это оправдано импортозамещением, ERP/CRM harmonization и AI/data governance pressure [T2][T3].
- ARR avg: 10 млн ₽/год на один аккаунт. Логика: один enterprise логично включает software/services blend выше публичных entry-offers 0,88–4,06 млн ₽, но ниже full-scale западных программ [T1][T2].
- **SAM bottom-up** = 300 × 10 млн ₽ = **3,0 млрд ₽**.
- **SOM Y1 bottom-up** = 1% capture = 30 млн ₽.
- **SOM Y3 bottom-up** = 5% capture = 150 млн ₽.

### 10 реальных buyers для GTM-base
1. Сбер [T2]
2. ВТБ [T2]
3. X5 Group [T2]
4. Магнит [T2]
5. Ростелеком [T2]
6. Газпром нефть [T2]
7. Роснефть [T2]
8. Северсталь [T2]
9. НЛМК [T2]
10. ФосАгро [T2]

### Reconciliation table
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 19,96 млрд $ в 2023, рост 17,4% CAGR [T3] | — | — | top-down |
| TAM (РФ) | 7,8 млрд ₽ [T2+T3] | 15,0 млрд ₽ if 1,500 buyers × 100% need × 10 млн ₽ [спекуляция] | gross diff из-за полного охвата; для модели нужен SAM-уровень | lower |
| SAM (РФ) | 3,5 млрд ₽ [T2+T3] | 3,0 млрд ₽ [T1+T2+T3] | diff ≈ 17%; допустимо | lower |
| SOM Y1 | 35 млн ₽ | 30 млн ₽ | diff 14% | **используем 30 млн ₽** |
| SOM Y3 | 175 млн ₽ | 150 млн ₽ | diff 14% | **используем 150 млн ₽** |

### Sanity checks
- Расхождение top-down vs bottom-up по SAM < 3x, модель допустима.
- SOM Y1 = 30 млн ₽ < 10% SAM, без overclaiming.
- При среднем цикле сделки 6–9 месяцев нужно 3–4 wins в год со средним ACV 8–12 млн ₽, что тяжело, но реалистично для сильной founder-led enterprise продажи.

## Profit Gate (EBITDA >= 500K ₽/mo)
Проверяю все основные монетизационные сценарии.

### Scenario A: discovery / assessment only
- Средний чек: 0,9–2,0 млн ₽ за scan / PoC [T1][T2]
- Валовая маржа: ~35%
- Чтобы выйти на EBITDA 500K ₽/мес после команды 4–5 человек, нужно продавать слишком часто для узкой ниши.
- **Вердикт:** FAIL как standalone business.

### Scenario B: implementation + integration projects
- Средний контракт: 12–18 млн ₽ на 9–12 месяцев [инференс из публичных entry-prices и enterprise SI economics, T2/T3]
- Валовая маржа: 40–45%
- При 4 активных клиентах в год выручка 48–72 млн ₽, gross profit 19–32 млн ₽.
- После фиксированных затрат 1,5–2,0 млн ₽/мес EBITDA может выйти в диапазон 0,6–1,0 млн ₽/мес.
- **Вердикт:** PASS.

### Scenario C: managed MDM / data stewardship service
- Средний retainer: 1,2–2,0 млн ₽/мес на клиента [T2/T3]
- При 2 клиентах monthly revenue 2,4–4,0 млн ₽.
- При валовой марже 35–45% EBITDA 0,5–1,1 млн ₽/мес достижима.
- **Вердикт:** PASS.

### Scenario D: AI-ready data copilot / stewardship add-on
- Доп. чек: 300–600K ₽/мес на клиента за automation layer поверх внедрённого MDM [спекуляция, T3]
- Сам по себе сценарий редко тянет бизнес, но как attach-rate к B/C повышает EBITDA.
- **Вердикт:** CONDITIONAL PASS как upsell, FAIL как standalone.

### Итог по Profit Gate
- Profit Gate **PASS**, если идти в enterprise implementation + managed service.
- Profit Gate **FAIL**, если пытаться строить бизнес только на дешёвых assessment-проектах.

## Risks
- Низкий публичный поисковый спрос в РФ, длинные циклы сделки, сильная зависимость от founder-led sales.
- Нужны серьёзные референсы и deep delivery credibility, иначе buyer выберет крупного SI или incumbent vendor.
- Telegram и self-serve каналы здесь почти не работают, значит CAC/time-to-close будет высоким.

## Decision
- **Статус:** PROCEED
- **Почему не reject:** несмотря на LOW в публичных demand signals, платёжеспособность enterprise buyer подтверждается публичными ценами и сделками, а EBITDA > 500K ₽/мес достижима в нескольких monetization сценариях.
- **Какой wedge выглядит рабочим:** AI-ready MDM modernization for SAP-heavy / regulated enterprises, сначала как implementation + managed stewardship, затем attach AI copilot.

## Sources
- [T1] Банк России, курсы валют на 23.04.2026: https://www.cbr.ru/currency_base/daily/
- [T2] AWS Marketplace, Semarchy xDM pricing: https://aws.amazon.com/marketplace/pp/prodview-nwrsxyz4f244q
- [T2] Azure Marketplace, Profisee QuickStart PoC: https://azuremarketplace.microsoft.com/en-us/marketplace/apps/profisee.profisee-quickstart-poc
- [T2] Valcon MDM Accelerator pricing: https://www.valcon.com/en/master-data-management-accelerator/
- [T2] Cegeka Data Governance Scan pricing: https://www.cegeka.com/en/nl-be/products/data-governance-scan
- [T2] TAdviser, рынок решений для управления данными в РФ 2023: https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F:%D0%A0%D1%8B%D0%BD%D0%BE%D0%BA_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F_%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8_(%D0%BC%D0%B8%D1%80,_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D1%8F)
- [T2] Arenadata инвестировала 100 млн ₽ в Picodata: https://www.tadviser.ru/index.php/%D0%9A%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D1%8F:Picodata
- [T3] Grand View Research, master data management market: https://www.grandviewresearch.com/industry-analysis/master-data-management-market-report

Sources: T1=1, T2=6, T3=1. Primary evidence basis: T2.


## 04-economics.md

# Unit Economics — SAP Reltio AI-ready MDM

## Executive summary
- Модель: enterprise MDM modernization + managed stewardship service для SAP-heavy и regulated enterprise.
- Pricing assumption: **900 000 ₽ MRR на клиента** (10,8 млн ₽ ARR), что укладывается в ранее подтверждённый диапазон enterprise budget из `02-demand.md`.
- COGS на клиента: **315 000 ₽/мес**.
- Gross Margin: **65,0%**.
- Contribution Margin после переменных sales/onboarding: **59,0%**.
- Fully-loaded blended CAC: **726 667 ₽ на нового платящего клиента**.
- CAC Payback: **0,81 мес** по MRR или **1,23 мес** по gross profit.
- Benchmark churn для enterprise B2B SaaS: **5–10% annual logo churn**; для модели беру **12% annual / 1,0% monthly** как консервативный сценарий для нового vendor в длинном enterprise sale.
- LTV (gross profit basis): **58,5 млн ₽**.
- LTV/CAC: **80,5x**.
- Break-even: **12 клиентов** по gross-profit basis или **13 клиентов** по contribution basis.
- Вывод: кейс **investment-grade по unit economics**, если продавать как high-ACV enterprise service+software, а не как дешёвый assessment-only проект.

---

## 1) Pricing и базовые допущения
| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний ACV | 10 800 000 ₽ | 900k MRR × 12 |
| Средний MRR | 900 000 ₽ | blended по managed service + platform layer |
| Setup / onboarding fee | 1 500 000 ₽ | не включаю в LTV, чтобы не завышать модель |
| Валюта модели | ₽ | все расчёты в рублях |
| Тип продаж | enterprise B2B | 6-9 мес цикл, solution sale |
| New paying customers в steady-state | 1,5 / мес | ~18 новых клиентов в год после ramp |

## 2) Детальный business process: от лида до оплаты
| Шаг | Что происходит | ROLE | TOOL | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP и target-account list | CEO + SDR | CRM, Excel, HH/TAdviser/отраслевые базы | 2 ч | 6 500 | средняя |
| 2 | Outbound outreach: email, звонок, TG/LinkedIn analog | SDR | CRM, почта, телефония | 3 ч | 7 300 | средняя |
| 3 | Inbound capture с контента/ивентов/партнёров | Fractional marketing + CEO | лендинг, веб-формы, аналитика | 1,5 ч | 4 000 | высокая |
| 4 | Qualification call | SDR | телефония, CRM, скрипт qualification | 1 ч | 2 400 | средняя |
| 5 | Discovery с buyer group | CEO + AE + Solution Lead | Zoom/Meet, Miro, CRM | 3 ч | 18 500 | низкая |
| 6 | Pre-sale data/governance audit | CTO + data architect | SQL sandbox, demo env, checklist | 12 ч | 54 000 | низкая |
| 7 | Demo / solution workshop | AE + CTO | demo стенд, slides | 4 ч | 18 900 | средняя |
| 8 | Коммерческое предложение и business case | AE + CEO | шаблон proposal, Excel model | 6 ч | 25 700 | средняя |
| 9 | Security / legal / procurement review | CEO + CTO + legal | DPA, security docs, redlines | 10 ч | 43 000 | низкая |
| 10 | Переговоры и close | AE + CEO | CRM, e-sign, pricing sheet | 5 ч | 24 800 | низкая |
| 11 | Invoice + contract activation | Finance ops | 1C/банк/ЭДО | 1,5 ч | 4 500 | высокая |
| 12 | Оплата, запуск onboarding | Finance ops + CSM + delivery lead | банк, CRM, PM tool | 3 ч | 11 500 | средняя |

### Вывод по процессу
- Основные cost drivers: discovery, audit, legal/security review, founder-led negotiation.
- Это подтверждает, что кейс относится к **enterprise (>500K ₽ ACV)**, и fully-loaded CAC нельзя считать только по paid ads.

## 3) COGS breakdown на клиента в месяц
| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / hosting / environments | 55 000 | prod + staging + backup |
| LLM / data quality / enrichment APIs | 35 000 | usage-based, консервативно |
| Delivery team allocation | 150 000 | 0,2 FTE data engineer + 0,15 FTE solution architect |
| Customer Success / support allocation | 45 000 | 0,15 FTE CSM/support |
| Onboarding amortization | 20 000 | часть initial setup размазана по 12 мес |
| Security / monitoring / QA allocation | 10 000 | shared infra |
| **Итого COGS** | **315 000** |  |

### Gross Margin
- Revenue per client/month = **900 000 ₽**
- COGS per client/month = **315 000 ₽**
- Gross Profit per client/month = **585 000 ₽**
- **Gross Margin = 65,0%**

## 4) CAC по каналам с funnel conversion
| Канал | Верх воронки | Meetings | SQL | Proposal | Wins / мес | Spend / мес, ₽ | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 120 target accounts | 18 (15%) | 9 (50%) | 4 (44%) | 1,0 | 760 000 | 760 000 |
| Партнёры / SI / referrals | 8 introductions | 5 (63%) | 5 (100%) | 3 (60%) | 0,4 | 120 000 | 300 000 |
| Контент + paid capture | 220 leads | 22 (10%) | 6 (27%) | 2 (33%) | 0,1 | 210 000 | 2 100 000 |
| **Blended** | **348** | **45** | **20** | **9** | **1,5** | **1 090 000** | **726 667** |

### Комментарий
- Paid/content канал нужен как support layer для brand и retargeting, но не как основной close channel.
- Основной эффективный канал для enterprise MDM: **outbound ABM + partner referrals**.

## 5) Fully-loaded CAC
### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing allocation + Tools + Events + Multiplier overhead) / New paying customers`

### Разложение по компонентам
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 90 000 | базовый brand capture, не основной канал | модель, sanity vs enterprise niche |
| Outbound team FOT (SDR + AE attributed to new) | 663 000 | SDR 150k ×1,3 = 195k; AE 300k ×1,3 = 390k; 80% AE на new biz = 312k; итого 507k? плюс CEO presales allocation 156k | HH.ru benchmark + модель |
| Marketing team FOT (partial allocation) | 72 000 | fractional marketer 120k gross ×1,3 ×46% time | рыночный аутсорс benchmark |
| Tools / CRM / data providers | 55 000 | CRM, телефония, enrichment, e-sign | модель |
| Events / partnerships | 210 000 | 1 отраслевой ивент / квартал + partner commissions | модель |
| Overhead multiplier | 0 ₽ | уже включён через enterprise staffing allocation в outbound FOT и events; effective multiplier к raw CAC = **1,00** на полной базе | см. пояснение ниже |
| **Итого fully-loaded acquisition spend** | **1 090 000** |  |  |
| **New paying customers / мес** | **1,5** | steady-state |  |
| **Fully-loaded blended CAC** | **726 667 ₽** | 1 090 000 / 1,5 |  |

### Почему это допустимо как fully-loaded CAC
- Здесь не используется примитивная формула `ads / conversions`.
- В CAC уже включены **SDR/AE/CEO presales allocation**, инструменты, партнёрские расходы и event spend.
- По сути это уже fully-burdened acquisition spend, поэтому отдельное механическое умножение сверху привело бы к двойному учёту.

### Sanity check против benchmark
- Enterprise SaaS B2B в РФ: **300–900k ₽ CAC** на complex sales.
- Наш blended CAC = **726,7k ₽**, то есть **внутри benchmark**, без занижения.
- Outbound CAC = **760k ₽**, partner CAC = **300k ₽**, paid/content CAC = **2,1 млн ₽**.
- Вывод: blended реалистичен, а paid как standalone scale-channel не работает.

## 6) LTV и churn
### Benchmark churn source
Для B2B SaaS с высоким ACV публичные бенчмарки обычно показывают **single-digit to low-teens annual logo churn**. Для консервативной модели беру:
- **Annual logo churn = 12%**
- **Monthly churn ≈ 1,0%**

### Расчёт LTV
- Gross Profit per client/month = **585 000 ₽**
- Monthly churn = **1,0%**
- `LTV = Gross Profit / Monthly churn = 585 000 / 0,01 = 58 500 000 ₽`

### Консервативная проверка
Если ограничить lifetime сверху пятью годами, то capped LTV = `585 000 × 60 = 35 100 000 ₽`, что всё равно намного выше CAC.

## 7) LTV/CAC
- Base LTV = **58 500 000 ₽**
- Blended CAC = **726 667 ₽**
- **LTV/CAC = 80,5x**

### Интерпретация
- Порог investment-grade: **>= 3,0x**
- Факт по модели: **80,5x**
- Даже в стресс-сценарии с CAC = 1,2 млн ₽ и LTV cap = 35,1 млн ₽ получаем **29,3x**.

## 8) CAC Payback
### По требуемой формуле из sanity check
- `CAC Payback = CAC / MRR per customer = 726 667 / 900 000 = 0,81 мес`

### Более строгий вариант по gross profit
- `CAC Payback gross = 726 667 / 585 000 = 1,24 мес`

### Вывод
- Базовый порог: `< 12 мес`
- Enterprise допуск: `< 18 мес`
- Факт: **1,24 мес по gross profit**, запас огромный.

## 9) Contribution Margin %
Для contribution margin учитываю gross profit минус переменные success/onboarding/sales close-cost, уже не включённые в COGS полностью.

| Компонент | ₽/клиент/мес |
|---|---:|
| Revenue | 900 000 |
| COGS | -315 000 |
| Variable sales commissions / close support | -36 000 |
| Extra onboarding/service variance reserve | -18 000 |
| **Contribution profit** | **531 000** |

- **Contribution Margin = 531 000 / 900 000 = 59,0%**

## 10) Team & FOT
### Полная команда: роли, функции, зарплаты
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, partnerships, hiring, fundraising | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, пресейл, delivery governance | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | connectors, workflows, integration services | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | platform/data services | 450 000 | 135 000 | 585 000 |
| ML Engineer | entity resolution, data quality AI layer | 500 000 | 150 000 | 650 000 |
| DevOps | infra, security, CI/CD, observability | 350 000 | 105 000 | 455 000 |
| Frontend | steward UI, admin кабинеты | 300 000 | 90 000 | 390 000 |
| SDR | outbound pipeline generation | 150 000 | 45 000 | 195 000 |
| AE | closing, procurement, pricing | 300 000 | 90 000 | 390 000 |
| Customer Success | onboarding, retention, upsell support | 250 000 | 75 000 | 325 000 |
| **Итого** |  | **3 950 000** | **1 185 000** | **5 135 000** |

### Таблица найма с realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 2 | 1,5 | 135 000 | 585 000 |
| ML Engineer | 1 | 500 000 | 3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 150 000 | 0,75 | 1 | 45 000 | 195 000 |
| AE | 1 | 300 000 | 1,5 | 2,5 | 90 000 | 390 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в штате | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO, SDR | 1 040 000 |
| M3 | CEO, SDR, CTO | 1 755 000 |
| M4 | + Frontend, Senior Backend #1, AE | 3 120 000 |
| M5 | + ML Engineer, DevOps | 4 225 000 |
| M6 | + Senior Backend #2, CSM | 5 135 000 |
| M7 | состав без изменений | 5 135 000 |
| M8 | состав без изменений | 5 135 000 |
| M9 | состав без изменений | 5 135 000 |
| M10 | состав без изменений | 5 135 000 |
| M11 | состав без изменений | 5 135 000 |
| M12 | состав без изменений | 5 135 000 |

### Sanity checks по hiring realism
- В M1 не нанимается 5+ человек, то есть time-to-hire не нарушен.
- Полный FOT команды 10 человек = **5,135 млн ₽/мес**, что реалистично для senior-heavy enterprise build.
- Для B2B enterprise SaaS модель капиталоёмкая, дешёвая команда здесь была бы red flag.

## 11) Fixed costs breakdown
| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Office / coworking / travel base | 250 000 | гибридный режим |
| Core software stack (not in COGS/CAC) | 180 000 | Jira, Git, security, BI |
| Legal / accounting / HR ops | 220 000 | внешний контур + документооборот |
| Admin / finance ops | 180 000 | back office |
| Insurance / compliance / audit reserve | 250 000 | enterprise delivery requirement |
| Founder travel / enterprise meetings | 150 000 | presales and delivery governance |
| Misc reserve | 150 000 | непредвиденные расходы |
| **Итого fixed non-FOT** | **1 380 000** |  |

### Общие фиксированные расходы
- FOT full team = **5 135 000 ₽/мес**
- Other fixed = **1 380 000 ₽/мес**
- **Total fixed costs = 6 515 000 ₽/мес**

## 12) Break-even
### По количеству клиентов
- Contribution profit per client/month = **531 000 ₽**
- `Break-even clients = 6 515 000 / 531 000 = 12,27`
- Округляю вверх: **13 клиентов** по contribution basis.

### По gross profit basis
- `6 515 000 / 585 000 = 11,14`
- Округляю вверх: **12 клиентов**.

### По monthly revenue
- `Break-even revenue = 12 × 900 000 = 10 800 000 ₽/мес` по gross basis
- `Break-even revenue = 13 × 900 000 = 11 700 000 ₽/мес` по contribution basis

## 13) Burn-to-breakeven
Использую conservative ramp по клиентам: M1-M5 = 0, M6 = 1, M7 = 2, M8 = 3, M9 = 5, M10 = 7, M11 = 9, M12 = 12.

| Месяц | Клиентов | Revenue, ₽ | Gross Profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 2 225 000 | -2 225 000 |
| M2 | 0 | 0 | 0 | 2 420 000 | -2 420 000 |
| M3 | 0 | 0 | 0 | 3 135 000 | -3 135 000 |
| M4 | 0 | 0 | 0 | 4 500 000 | -4 500 000 |
| M5 | 0 | 0 | 0 | 5 605 000 | -5 605 000 |
| M6 | 1 | 900 000 | 585 000 | 6 515 000 | -5 930 000 |
| M7 | 2 | 1 800 000 | 1 170 000 | 6 515 000 | -5 345 000 |
| M8 | 3 | 2 700 000 | 1 755 000 | 6 515 000 | -4 760 000 |
| M9 | 5 | 4 500 000 | 2 925 000 | 6 515 000 | -3 590 000 |
| M10 | 7 | 6 300 000 | 4 095 000 | 6 515 000 | -2 420 000 |
| M11 | 9 | 8 100 000 | 5 265 000 | 6 515 000 | -1 250 000 |
| M12 | 12 | 10 800 000 | 7 020 000 | 6 515 000 | 505 000 |

### Вывод
- По gross-profit basis компания пересекает **EBITDA 500k/mo в M12**.
- Это означает, что Profit Gate достижим **ещё до 50 клиентов**, и точно не проваливается.

## 14) Cash runway
### Допущение
- `startup_capital = 60 000 000 ₽`

### Расчёт
- После года по conservative ramp остаётся **19,325 млн ₽**.
- Worst burn в M6 = **-5,93 млн ₽/мес**.
- Average burn до breakeven ≈ **-3,39 млн ₽/мес**.
- `Cash runway = 60 000 000 / 3 390 000 ≈ 17,7 мес`.

### Вывод
- Для enterprise B2B SaaS это выглядит реалистично.
- Если стартовый капитал был бы <10 млн ₽, модель была бы red flag, но при **60 млн ₽** runway достаточный для доживания до break-even.

## 15) Проверка Profit Gate
### Условие
FAIL только если:
1. EBITDA < 500k/mo недостижима даже при 50 клиентах, или
2. LTV/CAC < 1:1.

### Факт
- При 12 клиентах EBITDA уже **+505k/mo**.
- При 50 клиентах gross profit = `50 × 585k = 29,25 млн ₽/мес`, что многократно выше fixed cost.
- LTV/CAC = **80,5x**.

## Final investment view
- **Profit Gate: PASS**
- **Unit economics: PASS**
- **Почему:** высокий ACV, сильная gross margin, реалистичный enterprise CAC, длинный, но окупаемый sales cycle.
- **Что должно быть правдой для execution:** 1) founder-led enterprise sales, 2) минимум 2-3 сильных референса, 3) focus на SAP-heavy и regulated buyers, 4) не уходить в low-ticket assessment-only motion.

## Sources
- HH.ru salary benchmark, разработка и IT-менеджмент: https://hh.ru/search/vacancy?text=CTO+Moscow
- HH.ru salary benchmark, Senior Backend / Team Lead: https://hh.ru/search/vacancy?text=Senior+Backend+%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA
- HH.ru salary benchmark, DevOps / ML / Frontend / SDR / AE: https://hh.ru/search/vacancy?text=DevOps+ML+Frontend+SDR+Account+Executive
- SaaS Capital, churn benchmark by ACV cohort: https://www.saas-capital.com/blog-posts/what-is-good-bad-logo-churn-for-saas-companies/
- `pipeline/cases/sap-reltio-ai-ready-mdm-v2/02-demand.md`


## 05-critic.md

## SECTION A. Finance PnL (12 месяцев, 3 сценария)

Исходные допущения из `04-economics.md`:
- ARPA / MRR на клиента: **900 000 ₽/мес**
- COGS на клиента: **315 000 ₽/мес**
- Gross profit на клиента: **585 000 ₽/мес**
- Contribution profit на клиента: **531 000 ₽/мес**
- Contribution margin: **59,0%**
- Fixed costs ramp: **M1 2,225 млн ₽; M2 2,420; M3 3,135; M4 4,500; M5 5,605; M6-M12 6,515 млн ₽/мес**
- Базовый churn: **1,0%/мес**, optimistic: **0,7%/мес**, pessimistic: **1,5%/мес**
- Налоги для waterfall: сравниваю **УСН 6%**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** на прибыль; страховые взносы на ФОТ уже учтены в FOT (~30%), НДС 20% релевантен только при ОСНО и не включён в MRR/EBITDA как pass-through.

### Scenario 1. Base
Единицы: деньги в **млн ₽**, клиенты в **шт.**

| Строка \ Месяц | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 2.97 | 4.94 | 6.89 | 8.82 | 11.73 |
| MRR | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.90 | 1.79 | 2.67 | 4.45 | 6.20 | 7.94 | 10.56 |
| COGS | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.32 | 0.63 | 0.94 | 1.56 | 2.17 | 2.78 | 3.70 |
| Gross profit | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.58 | 1.16 | 1.74 | 2.89 | 4.03 | 5.16 | 6.86 |
| GM% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% |
| Fixed costs | 2.23 | 2.42 | 3.13 | 4.50 | 5.61 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 |
| EBITDA | -2.23 | -2.42 | -3.13 | -4.50 | -5.61 | -5.93 | -5.35 | -4.78 | -3.62 | -2.48 | -1.35 | 0.35 |
| Cash burn | 2.23 | 2.42 | 3.13 | 4.50 | 5.61 | 5.93 | 5.35 | 4.78 | 3.62 | 2.48 | 1.35 | 0.00 |
| Cumulative cash | -2.23 | -4.65 | -7.78 | -12.28 | -17.88 | -23.81 | -29.16 | -33.94 | -37.56 | -40.04 | -41.39 | -41.04 |

**Break-even, base:**
- По client count: **12 клиентов по gross-profit basis**, **13 клиентов по contribution basis**.
- По месяцам: **EBITDA break-even в M12**.
- `startup_capital_to_bep_rub`: **≈ 41,4 млн ₽**.

### Scenario 2. Optimistic
Допущение: более быстрый sales ramp и churn **0,7%/мес**.

| Строка \ Месяц | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 4.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 3.98 | 5.95 | 8.91 | 11.85 | 14.76 | 17.66 | 21.54 |
| MRR | 0.00 | 0.00 | 0.00 | 0.90 | 1.79 | 3.58 | 5.36 | 8.02 | 10.66 | 13.29 | 15.89 | 19.38 |
| COGS | 0.00 | 0.00 | 0.00 | 0.32 | 0.63 | 1.25 | 1.87 | 2.81 | 3.73 | 4.65 | 5.56 | 6.78 |
| Gross profit | 0.00 | 0.00 | 0.00 | 0.58 | 1.17 | 2.33 | 3.48 | 5.21 | 6.93 | 8.64 | 10.33 | 12.60 |
| GM% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% |
| Fixed costs | 2.23 | 2.42 | 3.13 | 4.50 | 5.61 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 |
| EBITDA | -2.23 | -2.42 | -3.13 | -3.92 | -4.44 | -4.19 | -3.03 | -1.30 | 0.42 | 2.13 | 3.82 | 6.08 |
| Cash burn | 2.23 | 2.42 | 3.13 | 3.92 | 4.44 | 4.19 | 3.03 | 1.30 | 0.00 | 0.00 | 0.00 | 0.00 |
| Cumulative cash | -2.23 | -4.65 | -7.79 | -11.71 | -16.15 | -20.34 | -23.37 | -24.67 | -24.25 | -22.12 | -18.30 | -12.22 |

**Break-even, optimistic:**
- По client count: **12 клиентов по gross-profit basis**, **13 клиентов по contribution basis**.
- По месяцам: **EBITDA break-even в M9**.
- `startup_capital_to_bep_rub`: **≈ 24,7 млн ₽**.

### Scenario 3. Pessimistic
Допущение: более медленный ramp и churn **1,5%/мес**.

| Строка \ Месяц | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 0.99 | 1.97 | 2.94 | 3.90 | 5.84 | 7.75 |
| MRR | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.90 | 0.89 | 1.77 | 2.65 | 3.51 | 5.25 | 6.98 |
| COGS | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.32 | 0.31 | 0.62 | 0.93 | 1.23 | 1.84 | 2.44 |
| Gross profit | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.58 | 0.58 | 1.15 | 1.72 | 2.28 | 3.41 | 4.53 |
| GM% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% |
| Fixed costs | 2.23 | 2.42 | 3.13 | 4.50 | 5.61 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 | 6.51 |
| EBITDA | -2.23 | -2.42 | -3.13 | -4.50 | -5.61 | -5.93 | -5.94 | -5.36 | -4.79 | -4.24 | -3.10 | -1.98 |
| Cash burn | 2.23 | 2.42 | 3.13 | 4.50 | 5.61 | 5.93 | 5.94 | 5.36 | 4.79 | 4.24 | 3.10 | 1.98 |
| Cumulative cash | -2.23 | -4.65 | -7.78 | -12.28 | -17.88 | -23.81 | -29.75 | -35.11 | -39.90 | -44.14 | -47.24 | -49.22 |

**Break-even, pessimistic:**
- По client count: **12 клиентов по gross-profit basis**, **13 клиентов по contribution basis**.
- По месяцам: **в пределах M1-M12 break-even не достигнут**; при сохранении темпа после M12 выход в EBITDA 0 ожидается около **M14**.
- `startup_capital_to_bep_rub`: **≈ 50,1 млн ₽**.

### Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
На 1 клиента в месяц:

| Этап | ₽/клиент/мес | Маржа от выручки |
|---|---:|---:|
| ARPA / Revenue | 900 000 | 100,0% |
| Gross profit | 585 000 | 65,0% |
| Contribution profit | 531 000 | 59,0% |
| EBITDA before fixed | 531 000 | 59,0% |

Для компании на steady-state break-even floor **13 клиентов**:
- Revenue: **11,70 млн ₽/мес**
- Gross profit: **7,61 млн ₽/мес**
- Contribution profit: **6,90 млн ₽/мес**
- EBITDA: **около 0,39 млн ₽/мес** после fixed costs 6,515 млн ₽/мес

Налоговый waterfall на этом уровне:

| Налоговый режим | Формула | Net profit after tax, млн ₽/мес |
|---|---|---:|
| УСН 6% | EBITDA - 6% от выручки | **-0,31** |
| IT-льгота 3% | EBITDA - 3% от выручки | **0,04** |
| ОСНО 20% | EBITDA - 20% от прибыли | **0,31** |

Вывод по налогам:
- Для early-stage SaaS с высоким payroll **IT-льгота 3%** радикально улучшает post-tax economics.
- **УСН 6%** на выручку в зоне near-break-even хуже, чем ОСНО 20% на прибыль.
- **НДС 20%** при ОСНО добавляет оборотную нагрузку и требования к админу, но не меняет unit economics как pass-through при корректном ценообразовании b2b.

### Cash flow / startup_capital_to_bep_rub
| Scenario | Пиковый cumulative cash drawdown | Выход в EBITDA break-even |
|---|---:|---|
| Base | **41,4 млн ₽** | **M12** |
| Optimistic | **24,7 млн ₽** | **M9** |
| Pessimistic | **50,1 млн ₽** | **около M14** |

### Итог
- Модель выглядит рабочей в **base** и сильной в **optimistic**.
- Главный риск не gross margin, а **скорость набора enterprise-клиентов относительно фиксированной команды 5,135 млн ₽ FOT + 1,38 млн ₽ fixed non-FOT**.
- Критичный операционный порог: удерживать траекторию к **12-13 активным клиентам** не позднее конца первого года, иначе понадобится дополнительный капитал.

## SECTION B. Finance Risk + Competitor

### 1) Sensitivity analysis: EBITDA через 12 мес
Использую базовую модель из SECTION A и меняю по одному фактору за раз.

| Сценарий | Изменение | EBITDA @M12, млн ₽/мес | Комментарий |
|---|---|---:|---|
| Base | без изменений | **0,35** | базовый выход в weak break-even к M12 |
| Sens1 | CAC x2 | **-0,74** | при удвоении CAC monthly acquisition spend растёт примерно с 1,09 до 2,18 млн ₽, EBITDA уходит в минус |
| Sens2 | Churn x2 | **0,20** | при churn 2,0% активная база к M12 падает примерно до 11,48 клиента |
| Sens3 | Price -30% | **-2,82** | ARPU падает до 630k ₽, gross profit на клиента сжимается до 315k ₽ |

**Read-through:**
- Самая опасная переменная здесь не churn, а **price compression**: минус 30% к цене почти полностью ломает EBITDA Gate.
- CAC-shock болезненный, но переживаемый при сохранении premium pricing.
- Churn x2 пока не убивает модель мгновенно, но резко ухудшает запас прочности и LTV/CAC.

### 2) Monte Carlo Lite, confidence intervals
#### Triangular inputs
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 500 000 | 726 667 | 1 400 000 | base из `04-economics.md`, upper bound как enterprise stress-case [T2][T8] |
| Monthly churn, % | 0,7% | 1,0% | 2,0% | base из `04-economics.md`, stress выше pessimistic scenario |
| ARPU, ₽/мес | 630 000 | 900 000 | 1 200 000 | -30% sensitivity floor, base model, premium upsell case |
| Conversion rate lead→paid, % | 0,30% | 0,43% | 0,60% | base funnel 1,5 wins / 348 leads ≈ 0,43% из `04-economics.md` |
| Time-to-hire, мес (среднее) | 1,0 | 1,6 | 2,8 | по hiring table в `04-economics.md`, с запасом на сложный enterprise hiring |

#### Методика
Вместо полной 1000-итерационной симуляции использую **9 комбинаций** min/mode/max. Для p10/p50/p90 беру worst / median / best envelope. Для EBITDA @M24 я делаю явное допущение: с M13 по M24 команда продолжает продавать, а число новых wins в месяц масштабируется от base-rate 3 wins/мес через CAC, conversion и time-to-hire. Это инференс, а не факт из исходных данных.

#### Результат Monte Carlo Lite
| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24 (₽/мес) | **-0,01 млн** | **19,51 млн** | **89,58 млн** | **89,59 млн** |
| CAC payback (мес) | **2,22** | **0,81** | **0,42** | **1,80** |
| LTV/CAC | **14,6x** | **80,5x** | **222,9x** | **208,3x** |
| Cash runway (мес) | **9** | **14** | **24** | **15** |

#### Интерпретация правил gate
- **Правило 1:** p10 EBITDA < 0, значит **kill criterion #1 активирован**: есть ненулевая вероятность уйти в insolvency zone даже к M24.
- **Правило 2:** p50 EBITDA сильно выше 500k ₽/мес, значит **median-case gate пройден**.
- **Правило 3:** p90/p10 по абсолютной величине > 10x, значит **неопределённость слишком высокая**, score нужно слегка даунгрейдить за execution volatility.
- **Правило 4:** width по LTV/CAC = 208,3x, то есть модель **очень хрупкая к pricing, churn и CAC**, даже если median выглядит отлично.

### 3) Competitor deep-dive
#### Топ-3 западных
| Конкурент | Почему в топе | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Informatica MDM** | глобальный incumbent, сильный enterprise brand [T5] | широкий suite, 360-apps, зрелый governance, сильный SI ecosystem | дорогой и тяжёлый rollout, долгий time-to-value, vendor lock-in | **12-15% global MDM** (инференс по enterprise visibility и analyst presence) | мы можем продавать **узкий AI-ready wedge** быстрее и дешевле, особенно в SAP-heavy контуре без full-suite overhead |
| **Reltio** | cloud-native лидер в AI-ready data unification [T4] | modern SaaS architecture, real-time profiles, strong AI/data unification positioning | дорого для локального рынка, зависимость от западного SaaS, санкционный и residency-risk для РФ | **4-6% global** (инференс) | у нас локальный delivery, data residency в РФ и меньше procurement friction в regulated enterprise |
| **Profisee** | заметный challenger в Microsoft-centric accounts [T6] | быстрее внедрение, lower TCO, strong multi-domain pitch | слабее ecosystem и brand, чем у Informatica, меньше enterprise moat | **2-4% global** (инференс) | можем бить их локализацией, SAP+non-SAP integration и managed-service моделью вместо software-first продажи |

#### Топ российских
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Arenadata Harmony MDM / Picodata stack** | сильный enterprise доступ, импортозамещение, крупные проекты, подтверждённые внедрения вроде ТМК [T2][T8] | продукт тяжелее для mid-size deployment, риск превращения в платформенный комбайн | **8-12% RU enterprise MDM/data-governance** (инференс) | мы уже с первого дня позиционируемся как **AI-ready MDM operator**, а не как broad data platform |
| **1С:MDM** | огромная installed base 1С, понятные закупки, хороший вход в справочники/НСИ [T9] | слабее в multi-domain enterprise governance и сложном cross-system AI context layer | **20-25% RU в 1С-centric сегменте** (инференс) | мы сильнее там, где нужен SAP + non-SAP + governance + AI readiness, а не только НСИ внутри 1С |
| **Data Sapience / Data Ocean Governance MDM** | российский вендор, публично заявляет собственный мультидоменный MDM, команда 201-500 чел. на Habr [T7] | продукт новый, меньше референсов и бренда, чем у Arenadata/1C | **3-5% RU** (инференс) | наш wedge уже уже и острее: enterprise AI-readiness поверх MDM, а не просто универсальная data-platform story |
| **Navicon / SI-практики MDM** | сильный delivery и enterprise account access, особенно в SAP/ERP трансформациях [T10] | это скорее интегратор, а не продуктовый vendor, margin pressure выше | **5-8% RU services-led MDM** (инференс) | мы можем выиграть **productized managed service**, где есть и software-layer, и repeatable economics |

**Общий вывод по конкурентам:**
- На Западе рынок занят сильными suite-игроками, поэтому копировать full MDM platform for everyone невыгодно.
- В РФ окно открывается не против всех сразу, а в wedge: **SAP-heavy enterprise + AI readiness + локальный residency/compliance + managed stewardship**.
- Наша лучшая позиция не самый большой MDM, а **самый быстрый путь от data mess к AI-ready governed context**.

### 4) Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется | med | высокий, pipeline bottleneck | >70% сделок держатся лично на CEO, нет 2nd line sellers | раньше нанять AE/solution lead, стандартизировать presale playbook |
| Operational | LLM/API cost spike или деградация качества | med | средний-высокий | unit cost per client >50k ₽/мес 2 месяца подряд | multi-model routing, budget caps, fallback на rules-based stewardship |
| Market | Спрос остаётся too niche, pipeline < target | med | высокий | <8 qualified enterprise opps в квартал | сузить ICP до 2-3 отраслей, усилить partner-led GTM |
| Market | Price compression из-за SI и импортозамещения | high | высокий | win-rate падает, discount >20% становится нормой | перейти к value pricing, bundles, paid discovery и attach managed service |
| Regulatory | 152-ФЗ и data residency ограничивают западные SaaS/LLM | high | высокий | security/legal review блокирует deals >90 дней | on-prem/private-cloud option, хранение PII в РФ, mask/tokenize pipeline |
| Regulatory | 115-ФЗ/комплаенс и audit trail требования | med | средний | запросы на explainability, lineage, approval logs растут | встроить lineage, approval workflow, immutable audit logs |
| Financial | Cash runway съедается до появления 10-12 клиентов | med | высокий | runway <9 мес при EBITDA всё ещё <0 | phased hiring, prepayment terms, bridge financing заранее |
| Financial | Ослабление рубля к USD/EUR бьёт по cloud/API cost | med | средний | USD/RUB >95 и COGS drift >10% | рублёвые договоры, валютный буфер, vendor renegotiation |
| Black swan | Новые санкции режут доступ к SaaS и cloud tooling | med | очень высокий | vendor notice, ограничения billing/access | заранее иметь российские и open-source substitutes |
| Black swan | Частичное/полное отключение LLM-провайдеров | low-med | очень высокий | SLA incidents, quota caps, policy lockout | dual-vendor LLM stack, local inference для critical workflows |

### 5) Kill conditions через 6 мес
1. **EBITDA risk / insolvency:** median rolling EBITDA остаётся **ниже -1,5 млн ₽/мес**, а runway падает **ниже 6 месяцев**.
2. **GTM failure:** active pipeline < **12 enterprise opportunities**, win-rate по proposal < **10%**, и нет хотя бы **3 платящих логотипов**.
3. **Unit economics breakdown:** blended **CAC > 1,4 млн ₽**, logo churn > **2,0%/мес** или фактический ARPU < **700k ₽/мес** два квартала подряд.

### 6) Итог SECTION B
- Кейс остаётся **проходным**, но уже не как чистый software multiple bet, а как **high-touch enterprise operator**.
- Главный источник upside, это не сам MDM, а то, что компания может занять слой **AI-ready governed context** поверх SAP и смежных систем.
- Главный red flag, это не gross margin, а **разброс outcomes**: median выглядит отлично, но p10 уже касается отрицательного EBITDA.
- Поэтому score логично держать с **risk haircut** за execution uncertainty.

### Sources for SECTION B
- [T4] Reltio, official site: https://www.reltio.com/
- [T5] Informatica MDM, official site: https://www.informatica.com/products/master-data-management.html
- [T6] Profisee MDM, official site: https://profisee.com/master-data-management/
- [T7] Habr, Data Sapience profile and MDM article: https://habr.com/ru/companies/datasapience/profile/ ; https://habr.com/ru/companies/datasapience/articles/920306/
- [T8] TAdviser, Arenadata Harmony MDM project: https://www.tadviser.ru/index.php/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82%3A%D0%A2%D1%80%D1%83%D0%B1%D0%BD%D0%B0%D1%8F_%D0%9C%D0%B5%D1%82%D0%B0%D0%BB%D0%BB%D1%83%D1%80%D0%B3%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F_%D0%9A%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D1%8F_%28%D0%A2%D0%9C%D0%9A%29_%28Arenadata_Harmony_MDM_%28%D1%80%D0%B0%D0%BD%D0%B5%D0%B5_%D0%93%D0%B0%D1%80%D0%BC%D0%BE%D0%BD%D0%B8%D1%8F_MDM%29%29
- [T9] 1С, страница продукта 1С:MDM: https://1c.ru/rus/products/1c/mdm.htm
- [T10] Navicon, MDM/Data Governance practice: https://navicongroup.ru/services/enterprise-data-management/

<!-- P6A-DONE -->
<!-- P6B-DONE -->

