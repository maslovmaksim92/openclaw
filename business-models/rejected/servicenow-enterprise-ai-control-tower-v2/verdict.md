[B2B-OPS] ServiceNow Enterprise AI Control Tower v2 — NEAR-PASS: 66/100 | EBITDA base=682К₽/мес через 12 мес | LTV/CAC=13,2x | Ключевое преимущество: высокий enterprise ACV и vendor-neutral governance wedge | Главный риск: weak moat и слишком капиталоёмкий GTM.

# ServiceNow Enterprise AI Control Tower v2 — 06-verdict
sector: B2B-OPS
status: NEAR-PASS
score: 66/100
date: 2026-05-12
slug: servicenow-enterprise-ai-control-tower-v2

## Итог
**Вердикт инвесткомитета: NEAR-PASS.**

Кейс не проходит в APPROVED, хотя базовая юнит-экономика сильная и formal profit gate на 50 клиентах выполняется. Причина в том, что median-case из critic остаётся слабым: acquisition engine, длинный procurement tail, substitute pressure и weak moat не дают достаточно надёжного пути к investment-grade профилю. Это хороший кандидат для наблюдения и повторной оценки после первых локальных платящих логотипов, но пока не фондовый approve.

## Стадия 1. Intake
- Тезис: enterprise control-plane для AI governance, inventory, risk/compliance и orchestration поверх heterogeneous AI stack.
- Почему сейчас: крупные платформы уже формализуют AI governance как board-level budget line, а enterprise buyers вынуждены считать inventory, policy и risk по множеству моделей и агентов.
- Контекст: кейс был resurrected как standalone candidate, чтобы заново пройти полный пайплайн по новым правилам scoring и finance-risk.

## Стадия 2. Validation
- В папке кейса отдельный файл `02-validation.md` отсутствует.
- Функцию validation фактически выполняют `01-evidence.md`, `02-demand.md`, `04-economics.md` и `05-critic.md`.
- Это process-gap, но не блокер для verdict: evidence по рынку, economics и finance-risk присутствует и согласуется.

## Стадия 3. Demand
Source tier balance: T1=5, T2=8, T3=7, weighted=1.90. Penalty applied: -5 баллов to criterion #3

- Exact-demand в РФ по `enterprise ai platform`, `ai governance platform` и `enterprise workflow automation` остаётся LOW.
- Но adjacent budget line подтверждена: `service desk` даёт `demand_score=30`, `hh_ru=543`, `ITSM` даёт `demand_score=26`, `hh_ru=467`, а `контроль ИИ платформы` даёт proxy через `hh_ru=286`.
- Bottom-up модель даёт **SAM_bottom_up = 264 млн ₽/год**, **SOM Y1 = 28,8 млн ₽/год**, **SOM Y3 = 86,4 млн ₽/год**.
- Вывод: рынок не нулевой, но узкий, sales-heavy и category-creation-heavy. Для РФ это не массовый SaaS, а enterprise niche с ограниченным buyer universe.

## Стадия 4. Economics
### Ключевые метрики
- customer_ltv_rub: **20 240 000 ₽**
- CAC fully-loaded: **1 532 000 ₽**
- LTV/CAC: **13,2x**
- CAC payback: **5,1 мес**
- Gross Margin: **75,9%**
- contribution_margin_rub_month: **268 000 ₽/мес на клиента**
- fixed_costs_rub_month: **6 892 000 ₽/мес**
- Break-even clients: **21 operational / 26 stress-case**
- clients_to_500k_ebitda: **23-24**
- clients_to_1m_ebitda: **26**
- months_to_500k_ebitda: **12**
- months_to_1m_ebitda: **12**
- company_ebitda_rub_month base: **681 986 ₽/мес на M12**
- company_ebitda_potential_rub_month: **6 508 000 ₽/мес при 50 клиентах**
- startup_capital_to_bep_rub: **54 851 048 ₽**

### Полный бизнес-процесс из 04-economics.md
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам, телекому, ритейлу, industrial | SDR | HH, сайты компаний, CRM, таблицы | 25 мин/account | 520 | средняя |
| 2 | Обогащение контактов CIO / CDO / Head of Risk / Head of Platform | SDR | CRM, email finder, Telegram, ручной ресерч | 20 мин/account | 420 | средняя |
| 3 | Outbound-sequence 5-8 касаний | SDR | email sequences, CRM, телефония | 35 мин/account | 730 | высокая |
| 4 | Qualification call | SDR | Meet/Zoom, CRM | 30 мин/SQL | 630 | средняя |
| 5 | Discovery с business + IT owner | AE | Zoom, deck, ROI-calculator | 90 мин | 2 100 | низкая |
| 6 | Подготовка tailored demo и architecture fit | AE + Solution Architect/CTO | sandbox, demo env, diagrams | 4 ч | 10 500 | низкая |
| 7 | Demo + workshop по governance / risk / inventory | AE + CTO + CEO | Zoom / onsite | 2 ч | 7 900 | низкая |
| 8 | Security review / legal / procurement Q&A | AE + CTO + юрист | docs, почта, Dataroom | 8 ч | 21 000 | низкая |
| 9 | Пилот 4-6 недель на 1-2 use cases | CSM + backend + ML + DevOps | cloud env, connectors, PM board | 32 ч | 78 000 | средняя |
| 10 | Коммерческое предложение и business case | AE + CEO | CRM, spreadsheet, docs | 4 ч | 11 000 | низкая |
| 11 | Согласование договора и DPA/ИБ приложений | AE + юрист | Диадок, Word, email | 7-15 раб. дней | 9 500 | средняя |
| 12 | Выставление счёта | Finance/Ops | 1С, банк-клиент | 20 мин | 400 | высокая |
| 13 | Оплата счёта | Клиент | банк-клиент | 5-20 раб. дней | 0 | вне контура |
| 14 | Onboarding, SSO, RBAC, initial integrations | CSM + backend + DevOps | API, IAM, Jira | 18-24 ч | 42 000 | средняя |
| 15 | Ежемесячный governance review / QBR | CSM + AE | BI, CRM, dashboards | 2 ч/мес | 5 500 | средняя |

### Команда
| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO | 1 | 910 000 | enterprise sales, strategic partnerships, top accounts |
| CTO/Tech Lead | 1 | 780 000 | architecture, security posture, enterprise solutioning |
| Senior Backend | 2 | 1 092 000 | policy engine, connectors, admin workflows |
| ML Engineer | 1 | 650 000 | AI inventory classification, summaries, risk workflows |
| DevOps | 1 | 468 000 | deployments, observability, uptime, infra cost control |
| Frontend | 1 | 390 000 | admin console, dashboards, governance UX |
| SDR | 1 | 234 000 | account mapping, meetings, outbound sequences |
| AE | 1 | 468 000 | discovery, demo, proposal, procurement navigation |
| Customer Success | 1 | 338 000 | onboarding, QBR, retention, expansion |
| Finance/Ops | 0,5 | 182 000 | contracts, billing, reporting, vendor ops |
| **Итого** | **10,5** | **5 512 000 ₽/мес** | heavy enterprise team |

## Стадия 5. Critic
- P6A показывает сильную client-level economics и формальный проход по EBITDA gate в базе уже к M12.
- Но P6B существенно ухудшает картину после учёта acquisition engine: **base EBITDA after CAC @M12 = -1 450 686 ₽/мес**, **p10 EBITDA @M24 = -6 390 341 ₽/мес**, **p50 = -542 153 ₽/мес**, **p90 = 47 580 724 ₽/мес**.
- Это значит, что upside очень большой, но median-case всё ещё не проходит quality gate по предсказуемости.
- Bottom line: модель хороша на уровне unit economics, но слишком хрупка на уровне investable company-building.

## Стадия 6. Verdict
### Оценка
| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC = 13,2:1», «CAC Payback = 5,1 месяца», «Gross Margin = 75,9%» подтверждают сильную клиентскую экономику. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 17 | «EBITDA break-even достигается только в M12», «681 986 ₽» в base и «6,51 млн ₽/мес» при 50 клиентах, но median-case после CAC уже слабый. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | «SAM_bottom_up = 264 млн ₽/год», «service desk demand_score=30, hh_ru=543», но exact category pull LOW и применён tier penalty -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | «в РФ прямой категории почти нет», а value легко утечёт в «локальные AI-платформы, ITSM-слой и экосистемные LLM-вендоры», поэтому moat только на границе investment-grade. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | «Cash runway, мес: p10 7,8 / p50 10,2», heavy hiring и vendor dependency по LLM/санкциям делают execution сложным, но не фатальным. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | Есть 10 named targets, channel fit через founder-led outbound и integrator motion, а payback «5,05 мес» выглядит рабочим для enterprise sales. |

**Итого raw:** 99/150  
**Normalized score:** 66/100

## 7-factor moat framework
| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не усиливает ценность продукта для остальных. |
| Switching costs | 2 | SSO, RBAC, policy-слой, интеграции в ITSM/IAM и обученная governance-практика создают умеренный switching friction. |
| Scale economies | 1 | Shared platform scale есть, но presale, pilot и security review остаются дорогими и human-heavy. |
| Proprietary data / model advantage | 1 | Собственный data advantage возможен, но в evidence нет T1/T2 подтверждения масштаба уникального датасета. |
| Regulatory moat | 1 | Compliance pressure помогает категории, но не создаёт эксклюзивной защиты для молодого вендора без accreditation edge. |
| Brand / distribution | 1 | ServiceNow и Сбер сильнее по brand/distribution, у нового игрока локальный pull пока не доказан. |
| Embedded workflow | 2 | После внедрения продукт действительно встраивается в procurement, risk, inventory и AI governance workflow клиента. |

**Moat raw = 8/21**  
**Moat score = round((8 × 25) / 21) = 10/25**

**Вывод:** moat = weak-to-borderline. Порог formal weak moat не пробит, но фактически защита остаётся слишком слабой для approve.

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | крупнейший multi-model и regulated AI buyer, есть сильная боль по inventory, audit trail и vendor-neutral oversight | партнёрство + email decision-maker в AI governance / platform office | 750 000 ₽/мес |
| ВТБ | банк с высокой нагрузкой на risk/compliance и большим числом AI use cases | direct outreach CIO/CDO + конференции по финтеху | 650 000 ₽/мес |
| Т-Банк | быстро масштабирует AI-функции и нуждается в прозрачности по policy и model usage | founder-led email + warm intro через integrator | 550 000 ₽/мес |
| Ростелеком | телеком и гос-adjacent инфраструктура, много distributed AI initiatives и сложный security contour | партнёрский канал с ITSM/интегратором | 500 000 ₽/мес |
| МТС | мультипродуктовый AI-ландшафт и потребность в governance поверх внутренних и внешних моделей | direct outreach CDO / Head of Platform | 500 000 ₽/мес |
| X5 Group | ритейл с большим числом AI-пилотов в supply chain, pricing и ops, нужна централизованная visibility | email decision-maker + retail/IT conference | 450 000 ₽/мес |
| Магнит | похожая проблема распределённого AI-стека и auditability в enterprise retail | партнёрство + direct enterprise outreach | 450 000 ₽/мес |
| Северсталь | industrial buyer с дорогими AI use cases и высокими требованиями к контролю и traceability | enterprise integrator + targeted workshop | 600 000 ₽/мес |
| Норникель | промышленный контур с требованиями к risk, data residency и внутренним approval workflows | прямой вход через CTO/цифровую трансформацию | 600 000 ₽/мес |
| Газпром нефть | крупный regulated enterprise с несколькими AI-командами и тяжёлым procurement/security контуром | конференция + партнёрство с российским внедренцем | 700 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Комментарий |
|---|---|---|---|
| Weak moat и incumbent capture | Высокая | Высокий | Главный риск, потому что governance/control-plane value легко бандлится в ServiceNow, Сбер, Just AI, MWS и соседние ITSM/AI stacks. |
| GTM-cost spiral и длинный procurement tail | Высокая | Высокий | Final fully-loaded CAC уже **1,532 млн ₽**, а median-case EBITDA @M24 остаётся отрицательным. |
| LLM / санкционная / infra dependency | Средняя | Высокий | В risk matrix прямо отмечены provider shocks, latency/cost inflation и риск отключения западных API. |

## LTV Upside Calculator
Чтобы кейс перешёл из NEAR-PASS в APPROVED WITH NOTES, нужен один из апсайд-сценариев:

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| CAC | 1 532 000 ₽ | ≤1 100 000 ₽ | Уменьшает acquisition burn и повышает шанс, что p50 EBITDA @M24 выйдет выше нуля. |
| ARPA | 400 000 ₽/мес | 500 000-550 000 ₽/мес | Ускоряет выход в EBITDA gate и снижает clients_to_500k_ebitda. |
| Churn | 1,5%/мес | ≤1,0-1,2%/мес | Поднимает customer_ltv_rub и запас прочности по LTV/CAC. |
| Partner/integrator mix | 0,5 new clients/мес | ≥1,0 new clients/мес | Стабилизирует GTM и сокращает founder-heavy motion. |
| Product scope | governance + heavy pilot | audit/inventory-first SKU | Снижает presale-engineering load и time-to-value. |

## Что нужно доказать для возврата к approve
1. Не менее 3 локальных платящих enterprise-логотипов в РФ с чеком **450-700К ₽/мес**.
2. Pilot-to-paid conversion не ниже **30%** без роста blended CAC выше **1,1 млн ₽**.
3. Повторяемый wedge против bundled incumbents, например через data residency, on-prem/private-cloud или audit-first SKU.
4. Подтверждённый median-case EBITDA positive после учёта acquisition engine, а не только чистого gross profit.

## Proof points для APPROVED
Сейчас proof points **недостаточны**, но уже есть база для повторной оценки:
1. **Сильная client-level economics:** `LTV/CAC = 13,2x`, `CAC Payback = 5,1 мес`, `Gross Margin = 75,9%`.
2. **Есть крупный buyer universe в regulated enterprise:** банки, телеком, ритейл и industrial уже фигурируют в bottom-up ICP.
3. **Есть формальный путь к EBITDA gate:** `M12 EBITDA = 681 986 ₽` в base и `6,51 млн ₽/мес` при 50 клиентах.
4. **Есть category proof глобально:** ServiceNow уже продаёт AI Control Tower как central governance layer.
5. **Но нет локально доказанного moat и median-case resilience**, поэтому proof пока не дотягивает до approve.

## Финальное решение инвесткомитета
**NEAR-PASS.**

Кейс силён как thesis на enterprise AI governance в РФ и может стать интересным для фонда после 6-12 месяцев реального GTM-proof. Сейчас это не reject по сути продукта, а reject по качеству инвестиционного профиля: слишком дорогой и хрупкий путь к воспроизводимой прибыли, слишком слабая защита против incumbents, слишком широкий диапазон outcomes.
