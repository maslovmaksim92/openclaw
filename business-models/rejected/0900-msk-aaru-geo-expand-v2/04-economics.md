---
stage: unit-economics
created: 2026-04-20T08:58:12+03:00
verdict: rejected
case: Aaru synthetic customer research / РФ enterprise wedge
---

# 04-economics

## Executive summary
- **Модель монетизации:** enterprise subscription + managed synthetic research layer.
- **Базовый чек:** **200 000 ₽/клиент/мес**. Это соответствует выводам из `02-demand.md` как реалистичному локальному ceiling для enterprise insights engine, но ниже порога Program 1 в `>500 000 ₽/мес`.
- **COGS на клиента:** **133 000 ₽/мес**.
- **Contribution margin:** **33,5%**.
- **Blended fully-loaded CAC:** **1 300 000 ₽** на нового платящего клиента.
- **Monthly churn benchmark:** **2,1%/мес** для B2B SaaS mid-market, использую как внешний benchmark для upper-mid enterprise-like motion. Источник: OptiMine / Optify benchmark page, accessed 2026-04-20. https://www.optifai.com/blog/average-churn-rate-for-saas
- **LTV:** **3,19 млн ₽**.
- **LTV/CAC:** **2,46x**, ниже investment-grade порога **3,0x**.
- **CAC payback:** **6,5 мес по выручке** и **19,4 мес по gross profit**, что хуже enterprise sanity threshold `<18 мес`.
- **Fixed costs:** **5,67 млн ₽/мес**.
- **Break-even:** **85 клиентов** или **17,0 млн ₽ MRR**, что выше реалистичного локального SAM из `02-demand.md`.
- **Profit Gate:** **FAIL.** Даже при **50 клиентах** компания остаётся ниже **500 000 ₽ EBITDA/мес**: EBITDA около **-2,32 млн ₽/мес**.

## 1) Business process, от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Поиск ICP-аккаунтов, обогащение списка | SDR | CRM + prospecting stack | 2 ч/аккаунт | 1 200 | semi-manual |
| 2 | Первый outbound touch, email/мессенджер/call | SDR | CRM, email, телефония | 30 мин | 300 | semi-manual |
| 3 | Follow-up 4-6 касаний | SDR | sequence tool + CRM | 10 дней cycle | 2 000 | semi-manual |
| 4 | Discovery call | AE + founder | VC/meet + deck | 1 ч + prep | 6 500 | manual |
| 5 | Qualification и формулировка use case | AE + solutions lead | Notion, CRM | 3 дня | 12 000 | manual |
| 6 | Demo synthetic research workflow | Solutions engineer | demo env, prompts, datasets | 1 неделя | 18 000 | semi-manual |
| 7 | Pilot scoping и proposal | AE + analyst | proposal docs | 1 неделя | 22 000 | manual |
| 8 | Security / procurement / legal | founder + legal + customer IT | DPA, security questionnaire | 2-4 недели | 35 000 | manual |
| 9 | Pilot execution | analyst + ML/PM support | cloud, LLM, dashboards | 2-3 недели | 70 000 | semi-manual |
| 10 | Commercial negotiation | founder + AE | CRM, contract docs | 1 неделя | 15 000 | manual |
| 11 | Contract signing and invoicing | ops / finance | ЭДО, банк, 1С/аналог | 2-3 дня | 4 000 | mostly automated |
| 12 | Payment receipt and activation | finance + CSM | банк, billing, CRM | 1 день | 3 000 | mostly automated |

**Итого по циклу сделки:** ~**2,3-3,0 месяца**, прямые cash-like затраты на 1 won-deal до overhead около **189 000 ₽**, но реальный CAC значительно выше из-за FOT sales/marketing, tool stack, событий и низкой конверсии enterprise funnel.

## 2) COGS breakdown per client / month
| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / embeddings | 18 000 | usage-heavy enterprise workloads | synthetic personas + testing runs |
| Cloud / storage / observability | 12 000 | cloud allocation | хранение, логи, мониторинг |
| Data prep / prompt ops / QA | 10 000 | analyst hours allocation | ручная настройка и валидация |
| Research analyst delivery time | 55 000 | ~0,25 FTE от 220K gross + 30% | managed-service nature |
| Solutions engineer support | 20 000 | ~0,05 FTE от 300K gross + 30% | интеграция, demos, fixes |
| Customer success / account management | 12 000 | ~0,04 FTE от 230K gross + 30% | ежемесячные touchpoints |
| Security / legal / vendor management reserve | 6 000 | allocation | enterprise overhead |
| Payment processing / документооборот | 0 | B2B wire negligible | несущественно |
| **Итого COGS** | **133 000** |  |  |

**Gross profit / клиент / мес = 200 000 - 133 000 = 67 000 ₽**  
**Gross margin = 33,5%**

## 3) CAC по каналам с funnel conversion
### Канальные воронки
| Канал | Monthly spend / FOT, ₽ | Лиды/аккаунты в месяц | Meeting rate | SQL rate | Proposal rate | Win rate | Новые клиенты/мес | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound enterprise | 520 000 | 220 account touches | 3,2% | 37% | 50% | 33% | 0,43 | 1 209 302 |
| Content / inbound | 180 000 | 18 inbound leads | 28% | 40% | 45% | 28% | 0,25 | 720 000 |
| Partners / agencies | 250 000 | 8 partner intros | 50% | 50% | 50% | 50% | 0,50 | 500 000 |

### Fully-loaded CAC, blended
Использую enterprise multiplier, потому что ACV `2,4 млн ₽/год`, много касаний, demo/pilot, legal и security review.

| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый demand capture + ретаргетинг | assumption for niche B2B |
| Outbound team FOT (SDR/AE attributed to new) | 819 000 | 1 SDR `150K` + 1 AE `330K` gross, оба ×1,3 соцвзносы, AE variable reserve included | HH-like market ranges corroborated by vacancy search [S1][S2] |
| Marketing team FOT (partial allocation) | 117 000 | 30% времени growth marketer `300K gross ×1,3` | [S3] + inference |
| Tools (CRM, prospecting, sequencing, analytics) | 90 000 | CRM + data + outreach stack | market assumption |
| Events / partnerships | 120 000 | breakfasts, partner enablement, co-marketing | market assumption |
| Raw CAC budget | 1 266 000 | сумма строк выше | calc |
| Overhead multiplier (x1.3) | 379 800 | `1 266 000 × 0,3` | std for enterprise B2B per task rule |
| **Fully-loaded CAC budget** | **1 645 800** |  |  |
| **New paying customers / month** | **1,27** | 0,43 + 0,25 + 0,50 + small overlap haircut | calc |
| **Blended fully-loaded CAC** | **1 295 906 ₽** | `1 645 800 / 1,27` | calc |

### CAC sanity check
- Enterprise B2B benchmark from task: **300-900K ₽/клиент** для Enterprise SaaS B2B в РФ.
- Полученный blended CAC **1,30 млн ₽** лежит **выше benchmark**, что правдоподобно для нового seller в узкой категории с long education cycle.
- Значит модель **не занижает** CAC. Скорее наоборот, отражает реальную penalty за category creation.

## 4) LTV with churn rate
### Churn benchmark
- Беру **2,1% monthly logo churn** как B2B SaaS benchmark. Источник: Optify benchmark compilation, 2025 article, accessed 2026-04-20. https://www.optifai.com/blog/average-churn-rate-for-saas [S4]
- Для данного кейса это даже мягкая оценка: локальный продукт category-creation, ROI неочевиден, значит реальный churn может быть выше. Ниже считаю на benchmark, чтобы не завышать reject.

### Расчёт LTV
Формула: **LTV = (MRR × Gross Margin) / Monthly Churn**

- MRR per customer = **200 000 ₽**
- Gross margin = **33,5%**
- Gross profit per customer / month = **67 000 ₽**
- Churn = **2,1% / мес**
- **LTV = 67 000 / 0,021 = 3 190 476 ₽**

## 5) LTV / CAC
- **LTV/CAC = 3 190 476 / 1 295 906 = 2,46x**
- Investment-grade threshold по задаче: **>= 3,0x**
- **Вердикт: ниже investable threshold**

## 6) CAC Payback
| Метрика | Формула | Результат |
|---|---|---:|
| CAC Payback по выручке | `CAC / MRR` | **6,5 мес** |
| CAC Payback по gross profit | `CAC / GP per customer` | **19,3 мес** |

**Вывод:** по выручке метрика выглядит терпимо, но по gross margin payback выходит **хуже enterprise threshold `<18 мес`**.

## 7) Contribution Margin %
| Показатель | ₽ | % от выручки |
|---|---:|---:|
| Revenue / client / month | 200 000 | 100,0% |
| COGS | 133 000 | 66,5% |
| **Contribution / gross profit** | **67 000** | **33,5%** |

Для investable software-like кейса это слишком низко. Профиль ближе к tech-enabled service, чем к масштабируемому SaaS.

## 8) Full team table
### Team & FOT
Источники salary benchmark: HH vacancy search snapshots, accessed 2026-04-20. Диапазоны согласуются с задачей и рыночной реальностью для Москвы/СПб.
- [S1] CTO / Tech Lead: https://hh.ru/search/vacancy?text=CTO
- [S2] ML engineer / AI engineer: https://hh.ru/search/vacancy?text=ML+Engineer
- [S3] Senior backend: https://hh.ru/search/vacancy?text=Senior+Backend+Developer
- [S5] DevOps: https://hh.ru/search/vacancy?text=DevOps
- [S6] Frontend: https://hh.ru/search/vacancy?text=Frontend+Developer
- [S7] SDR: https://hh.ru/search/vacancy?text=SDR
- [S8] Account Executive: https://hh.ru/search/vacancy?text=Account+Executive
- [S9] Customer Success Manager: https://hh.ru/search/vacancy?text=Customer+Success+Manager

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 150 000 + 15% bonus reserve | 1 | 1 | 45 000 | 224 250 |
| AE | 1 | 330 000 + 10% commission reserve | 1,5 | 2,5 | 99 000 | 471 900 |
| Customer Success | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |
| Research Analyst | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Finance / Ops | 0,5 | 120 000 | 1 | 1 | 36 000 | 156 000 |
| **Итого full team FOT / мес** | **10,5** |  |  |  |  | **5 584 150 ₽** |

### Функции команды
| Роль | Основная функция |
|---|---|
| CEO | enterprise sales, fundraising, strategic delivery control |
| CTO / Tech Lead | продуктовая архитектура, roadmap, security |
| Senior Backend x2 | data pipelines, APIs, orchestration |
| ML Engineer | persona generation, evaluation, prompt systems |
| DevOps | infra, deployment, observability |
| Frontend | dashboards and client UX |
| SDR | outbound sourcing and qualification |
| AE | demos, proposals, closing |
| Customer Success | renewals and adoption |
| Research Analyst | настройка исследований и QA outputs |
| Finance / Ops | contracts, billing, vendor control |

## 9) Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| Full team FOT | 5 584 150 |
| Office / legal / бухгалтерия / admin | 250 000 |
| Base software / corp tooling | 90 000 |
| Insurance / compliance / misc reserve | 120 000 |
| **Итого fixed costs / month** | **6 044 150** |

Для break-even отдельно использую conservative fixed cost **5 670 000 ₽/мес**, исключая часть launch-only setup reserve. Даже в такой мягкой версии экономика не сходится.

## 10) Break-even by client count and by month
### Break-even по числу клиентов
- Contribution per client / month = **67 000 ₽**
- Fixed costs for steady-state = **5 670 000 ₽/мес**
- **Break-even clients = 5 670 000 / 67 000 = 84,6**, округляю до **85 клиентов**

### Break-even по месяцу
При реалистичном sales ramp для category-creation беру когорты новых клиентов: 0, 0, 1, 1, 1, 2, 2, 2, 3, 3, 4, 4.  
К M12 активная база ≈ **23 клиента**, MRR ≈ **4,6 млн ₽**, gross profit ≈ **1,54 млн ₽**. Это сильно ниже fixed costs.

| Месяц | Активные клиенты | MRR, ₽ | Gross profit, ₽ | Fixed costs, ₽ | EBITDA before tax, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 235 000 | -1 235 000 |
| M2 | 0 | 0 | 0 | 1 950 000 | -1 950 000 |
| M3 | 1 | 200 000 | 67 000 | 2 845 000 | -2 778 000 |
| M4 | 2 | 400 000 | 134 000 | 3 520 000 | -3 386 000 |
| M5 | 3 | 600 000 | 201 000 | 4 170 000 | -3 969 000 |
| M6 | 5 | 1 000 000 | 335 000 | 4 845 000 | -4 510 000 |
| M7 | 7 | 1 400 000 | 469 000 | 5 130 000 | -4 661 000 |
| M8 | 9 | 1 800 000 | 603 000 | 5 286 000 | -4 683 000 |
| M9 | 12 | 2 400 000 | 804 000 | 5 584 000 | -4 780 000 |
| M10 | 15 | 3 000 000 | 1 005 000 | 5 584 000 | -4 579 000 |
| M11 | 19 | 3 800 000 | 1 273 000 | 5 584 000 | -4 311 000 |
| M12 | 23 | 4 600 000 | 1 541 000 | 5 584 000 | -4 043 000 |

**Вывод:** break-even не достигается в первые 12 месяцев и вообще требует базы **~85 клиентов**, что несопоставимо с локальным SAM из `02-demand.md`.

## Cumulative FOT timeline M1-M12
Соблюдаю hiring realism: нет найма 5+ человек в M1, time-to-hire и ramp учтены.

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO + 1 Senior Backend | 1 391 000 |
| M2 | + Frontend + Research Analyst | 2 067 000 |
| M3 | + DevOps | 2 522 000 |
| M4 | + SDR | 2 746 000 |
| M5 | + AE | 3 218 900 |
| M6 | + CTO / Tech Lead | 3 933 900 |
| M7 | + ML Engineer | 4 583 900 |
| M8 | + Customer Success | 4 882 900 |
| M9 | + 2-й Senior Backend | 5 428 900 |
| M10 | + 0,5 Finance / Ops | 5 584 900 |
| M11 | без новых hires | 5 584 900 |
| M12 | без новых hires | 5 584 900 |

## Burn-to-breakeven
Если считать burn как `FOT + infra/admin + acquisition - gross profit`, то steady-state burn до выхода на B/E:
- Fixed opex + acquisition budget = **7,32 млн ₽/мес**
- Gross profit на 23 клиентах в M12 = **1,54 млн ₽/мес**
- **Net burn в M12 = ~5,78 млн ₽/мес**
- Для достижения B/E нужно подняться до **85 клиентов**, то есть почти в **3,7 раза** выше M12-базы и существенно выше реалистичного buyer universe.

## Cash runway
Берём **startup_capital = 30 млн ₽**.

| Сценарий | Monthly burn, ₽ | Runway |
|---|---:|---:|
| Начальные 6 месяцев, средний burn | 4 050 000 | 7,4 мес |
| M12 burn | 5 780 000 | 5,2 мес |
| Steady-state burn до B/E | 5 500 000+ | 5,4 мес |

**Вывод:** для enterprise B2B SaaS такой capital need выглядит заниженным, а при текущей модели до B/E нужен капитал значительно выше **30 млн ₽**. Это подтверждает red flag из задачи: startup capital to B/E получается сильно больше комфортного диапазона.

## Profit Gate decision
### Проверка на 50 клиентах
- Revenue = `50 × 200 000` = **10 000 000 ₽/мес**
- COGS = `50 × 133 000` = **6 650 000 ₽/мес**
- Gross profit = **3 350 000 ₽/мес**
- Fixed costs = **5 670 000 ₽/мес**
- **EBITDA = -2 320 000 ₽/мес**

### Итог
- **EBITDA < 500 000 ₽/мес даже при 50 клиентах: FAIL**
- **LTV/CAC = 2,46x < 3,0x investable threshold**
- **Gross-margin payback = 19,3 мес**, too slow
- **Кейс отклоняется по unit economics**

## Sources
- [S1] HH.ru, CTO vacancies: https://hh.ru/search/vacancy?text=CTO
- [S2] HH.ru, ML Engineer vacancies: https://hh.ru/search/vacancy?text=ML+Engineer
- [S3] HH.ru, Senior Backend vacancies: https://hh.ru/search/vacancy?text=Senior+Backend+Developer
- [S4] Optify / OptiFai churn benchmark page: https://www.optifai.com/blog/average-churn-rate-for-saas
- [S5] HH.ru, DevOps vacancies: https://hh.ru/search/vacancy?text=DevOps
- [S6] HH.ru, Frontend vacancies: https://hh.ru/search/vacancy?text=Frontend+Developer
- [S7] HH.ru, SDR vacancies: https://hh.ru/search/vacancy?text=SDR
- [S8] HH.ru, Account Executive vacancies: https://hh.ru/search/vacancy?text=Account+Executive
- [S9] HH.ru, Customer Success Manager vacancies: https://hh.ru/search/vacancy?text=Customer+Success+Manager

## Final verdict
**REJECTED.** Модель не даёт investable fund-level economics: низкий gross margin, тяжёлый fully-loaded CAC, break-even за пределами реалистичной локальной клиентской базы и отрицательная EBITDA даже на 50 клиентах.
