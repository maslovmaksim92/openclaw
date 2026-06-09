---
stage: economics
updated: 2026-06-09T05:10:00+03:00
verdict: REJECTED
---

# 04-economics

## Executive summary
- Модель для GEO-expand Helicone в РФ приходится считать не как чистый self-serve SaaS, а как `managed AI observability / gateway layer` для mid-market и enterprise.
- При реалистичном чеке **150,000 ₽/клиент/мес** и fully-loaded blended CAC **3,964,444 ₽** экономика не проходит investment gate.
- **LTV/CAC = 0.55x**, что ниже даже базового порога 1.0x и сильно ниже investable-порога 3.0x.
- На полном составе fixed cost base = **6,146,000 ₽/мес**. При contribution **87,000 ₽ на клиента** break-even наступает только примерно с **70.6 клиента**, то есть около **10,596,552 ₽ MRR**.
- Даже при **50 клиентах** monthly contribution = **4,350,000 ₽**, это ниже fixed cost base, следовательно кейс формально не проходит profit gate.

## Модель monetization
**Что продаём:** локализованный managed слой над Helicone-классом продукта: gateway, routing, observability, dashboards, security review, support SLA, частично on-prem / private deployment.

**Рабочая модель чека:**
- Setup / pilot fee: 300-600K ₽ единовременно.
- Recurring MRR: **150K ₽/мес**.
- Контракт: 12 месяцев.
- Сегмент: mid-market / lower enterprise B2B infra.

Это уже лучший-case wrapper. Сам исходный vendor pricing у Helicone начинается от low-end devtool уровней и Team plan на сайте стоит от **$799/мес**, поэтому для РФ высокий чек достигается только через сервисную надстройку, а не через прямую перепродажу продукта. [E1]

## 1) Business process, от lead до payment
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов | SDR | HH/market maps, Excel/CRM | 2 ч | 2 500 | Низкая |
| 2 | Обогащение контактов | SDR | CRM + prospecting stack | 1 ч | 1 200 | Средняя |
| 3 | Холодный outreach 40-60 касаний | SDR | Почта, Telegram, CRM sequences | 3 дня | 8 000 | Средняя |
| 4 | Discovery call | AE + CEO | Zoom/Meet, CRM | 1 ч | 9 000 | Низкая |
| 5 | Solution scoping | AE + CTO | Miro, docs, calculator | 2-3 дня | 22 000 | Низкая |
| 6 | Demo + security Q&A | AE + CTO | Demo env, docs | 1-2 дня | 18 000 | Низкая |
| 7 | Pilot proposal | AE + CEO | Proposal template, CRM | 1 день | 12 000 | Средняя |
| 8 | Pilot / PoC | Backend + DevOps + CTO | K8s, dashboards, gateway | 2-4 недели | 95 000 | Низкая |
| 9 | Procurement / legal / DPA | CEO + AE | Word, e-sign, legal | 1-3 недели | 35 000 | Низкая |
| 10 | Contract signing | CEO | e-sign / bank docs | 2 дня | 6 000 | Средняя |
| 11 | Implementation / onboarding | Backend + CSM + DevOps | Jira, docs, Slack/Telegram | 2 недели | 45 000 | Средняя |
| 12 | First invoice and payment | Finance + CEO | Банк, 1C/учёт | 3-10 дней | 3 000 | Высокая |

**Итог:** длинный enterprise-like motion на 8-14 недель. Для такого цикла сырой self-serve CAC неприменим, нужен fully-loaded CAC с учётом SDR, AE, инструментов и founder/solution effort.

## 2) COGS breakdown на 1 клиента / месяц
| Компонент COGS | ₽/клиент/мес | Комментарий |
|---|---:|---|
| Upstream vendor / gateway / observability stack | 18,000 |  |
| Cloud + storage + egress на клиента | 14,000 |  |
| SRE/DevOps support allocation | 10,000 |  |
| Customer Success + support allocation | 8,000 |  |
| Onboarding/integration amortization | 9,000 |  |
| Security/compliance amortization | 2,000 |  |
| Billing / FX / admin variable | 2,000 |  |
| **Итого COGS** | **63,000** |  |
| **Revenue / клиент / мес** | **150,000** |  |
| **Contribution / клиент / мес** | **87,000** |  |
| **Contribution Margin %** | **58.0%** |  |

## 3) CAC по каналам с funnel conversion
| Канал | Lead volume / мес | Meeting rate | SQL rate | Pilot rate | Win rate | New paying / мес | Spend / мес, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound SDR + AE | 1 200 target accounts | 2.5% | 30% | 33% | 15% | 0.45 | 1 360 000 | 3 022 222 |
| Партнёры / интеграторы | 12 intro | 100% | 33% | 50% | 50% | 0.25 | 350 000 | 1 400 000 |
| Content / inbound | 40 inbound leads | 15% | 50% | 33% | 20% | 0.20 | 520 000 | 2 600 000 |
| **Blended** |  |  |  |  |  | **0.90** | **2 230 000** raw / **3 568 000** fully-loaded | **3,964,444** |

### FULLY-LOADED CAC
Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier overhead) / New paying customers
```

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 120 000 | минимальный performance слой для retargeting + branded demand capture | assumption + market sanity |
| Outbound team FOT (SDR/AE attributed to new) | 676 000 | SDR 221K + AE 455K fully-loaded, 100% на new logo | HH.ru benchmark [E3][E4][E5] |
| Marketing team FOT (partial allocation) | 180 000 | 0.5 marketing generalist gross 138K + taxes/overheads | assumption |
| Tools (CRM, prospecting, enrichment, analytics) | 145 000 | CRM + email infra + data providers + call stack | market stack assumption |
| Events / partnerships | 280 000 | 1 отраслевой event / roundtable + partner spiffs | enterprise B2B assumption |
| Overhead multiplier | x1.6 | mid-market B2B infra, длинный cycle, founder + SE time | user instruction sanity |
| **Итого raw spend** | **2 230 000** | сумма строк 1-5 |  |
| **Итого fully-loaded spend** | **3 568 000** | raw × 1.6 |  |
| **New paying customers / мес** | **0.90** | blended funnel |  |
| **Fully-loaded CAC** | **3,964,444** | 3 568 000 / 0.90 |  |

### Sanity check по CAC
- Для mid-market SaaS пользовательский benchmark = 60-250K ₽, для enterprise B2B в РФ = 300-900K ₽.
- Полученный CAC **3.96M ₽** выше benchmark, но здесь это объясняется плохим product-market fit в РФ, vendor-risk, узким ICP и длинным pre-sale. Это не ошибка формулы, а сигнал неинвестируемости.

## 4) LTV с churn rate
Для раннего mid-market B2B infra SaaS беру **4% monthly logo churn**. Это хуже mature benchmark и отражает vendor-risk, слабый local urgency и высокий substitute pressure.

Benchmark-источник: Optifai на данных 939 B2B SaaS компаний даёт **1.5-3% monthly churn для mid-market** и **1-2% для enterprise**; наш кейс хуже benchmark, что логично для зарубежного devtool-вендора без сильного локального moat. [E2]

Формула:

```text
LTV = MRR per customer × Gross Margin % / Monthly churn
```

Расчёт:
- MRR = **150 000 ₽**
- Gross Margin = **58.0%**
- Monthly churn = **4.0%**
- **LTV = 2,175,000 ₽**

## 5) LTV/CAC
- **LTV/CAC = 0.55x**
- Investment grade threshold: **>= 3.0x**
- Verdict: **FAIL**

## 6) CAC Payback
Формула:

```text
CAC Payback = CAC / MRR per customer
```

- CAC Payback = **26.4 мес**
- Норма: <12 мес, для enterprise допускаемо <18 мес
- Verdict: **FAIL**

## 7) Contribution Margin %
- Revenue / клиент / мес = **150 000 ₽**
- COGS / клиент / мес = **63 000 ₽**
- Contribution / клиент / мес = **87 000 ₽**
- **Contribution Margin = 58.0%**

Для SaaS это уже не выдающийся уровень, а для wrapper + services слоя он ещё и не перекрывает тяжёлую fixed-cost базу.

## 8) Full team table
| Роль | Нужно чел. | Функции | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---:|---:|---|---:|
| CEO | 1 | Фандрайзинг, продажи tier-1, стратегия | 650,000 | 0 (founder) | 0 | +30% | 845,000 |
| CTO / Tech Lead | 1 | Архитектура, security, delivery | 550,000 | 2 | 2 | +30% | 715,000 |
| Senior Backend | 2 | Gateway, integrations, data plane | 450,000 | 1-2 | 1.5 | +30% | 585,000 |
| ML Engineer | 1 | Routing/evals, AI observability logic | 500,000 | 2-3 | 2 | +30% | 650,000 |
| DevOps | 1 | K8s, infra, on-prem deployment | 350,000 | 1-2 | 1 | +30% | 455,000 |
| Frontend | 1 | Dashboards, admin UI | 300,000 | 1 | 1 | +30% | 390,000 |
| SDR | 1 | Outbound prospecting | 170,000 | 0.5-1 | 1 | +30% | 221,000 |
| AE | 1 | Discovery, pilot, closing | 350,000 | 1-2 | 2-3 | +30% | 455,000 |
| Customer Success | 1 | Onboarding, renewal, support | 250,000 | 1 | 1 | +30% | 325,000 |
| **Итого** | **10** |  |  |  |  |  | **5,226,000** |

### Cumulative FOT timeline M1-M12
| Месяц | Кто в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO | 845 000 |
| M3 | CEO, CTO, Backend #1 | 2 145 000 |
| M4 | + DevOps, SDR | 2 821 000 |
| M5 | + Backend #2, AE | 3 861 000 |
| M6 | + ML, Frontend | 4 901 000 |
| M7 | + Customer Success | 5 226 000 |
| M8 | full team | 5 226 000 |
| M9 | full team | 5 226 000 |
| M10 | full team | 5 226 000 |
| M11 | full team | 5 226 000 |
| M12 | full team | 5 226 000 |

Проверка realism:
- В M1 нет 5+ наймов, значит time-to-hire не нарушен.
- Но даже при аккуратном ramp-up уже с M6 burn становится слишком высоким для слабого local demand.

## 9) Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| Core cloud / observability infra (non-client-specific) | 250,000 |
| Legal + бухгалтерия + data/privacy counsel | 180,000 |
| Software / corp tools / security stack | 120,000 |
| Travel / meetings / enterprise procurement | 150,000 |
| Recruiting / HR ops | 120,000 |
| G&A / admin reserve | 100,000 |
| Team FOT | 5,226,000 |
| **Итого fixed cost base** | **6,146,000** |

## 10) Break-even
### По числу клиентов
Формула:

```text
Break-even clients = Fixed costs / Contribution per client
```

- Fixed costs = **6,146,000 ₽/мес**
- Contribution per client = **87,000 ₽/мес**
- **Break-even = 70.6 клиента**, округляя вверх, **71 клиент**

### По выручке в месяц
- Break-even MRR = **10,596,552 ₽/мес**

### Проверка profit gate at 50 clients
- Revenue at 50 clients = **7,500,000 ₽/мес**
- Contribution at 50 clients = **4,350,000 ₽/мес**
- Fixed cost base = **6,146,000 ₽/мес**
- **EBITDA before growth investments = -1,796,000 ₽/мес**

Итог: даже на **50 клиентах** бизнес остаётся ниже нуля, то есть company EBITDA **не достигает +500K ₽/мес**. Формальный profit gate = **FAIL**.

## Burn-to-breakeven и runway
- Steady-state burn = FOT 5,226,000 + fixed non-FOT 920,000 + acquisition 3,568,000 = **9,714,000 ₽/мес**.
- Средний burn по M1-M12 с учётом hire ramp = **8,385,833 ₽/мес**.
- При startup capital = **40 000 000 ₽** runway = примерно **4.8 мес**.
- Cumulative burn за первые 12 месяцев = **100,630,000 ₽**.
- Так как break-even внутри горизонта 12 месяцев не достигается, требуемый startup capital до BEP здесь **сильно выше 40M ₽**, ориентирно **80M+ ₽**.

## Final economics verdict
**REJECTED.**

Почему:
1. Fully-loaded CAC = **3,964,444 ₽** на нового клиента, это разрушает unit economics.
2. **LTV/CAC = 0.55x < 1.0x**, то есть каждый новый клиент в этой GEO-expand модели экономически убыточен.
3. Даже при **50 клиентах** EBITDA не достигает +500K ₽/мес.
4. Для прохождения гейта пришлось бы либо резко поднять ARPU выше 250-300K ₽/мес, либо сократить CAC в 2.5-3 раза, либо иметь локальный moat. Ничего из этого спросом не подтверждено.

## Sources
- [E1] Helicone pricing, просмотрено 2026-06-09: https://www.helicone.ai/pricing
- [E2] Optifai, B2B SaaS churn benchmarks (939 companies), просмотрено 2026-06-09: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [E3] HH.ru, senior backend developer Moscow listings, просмотрено 2026-06-09: https://hh.ru/vacancies/senior-backend-developer
- [E4] HH.ru, machine learning engineer Moscow listings, просмотрено 2026-06-09: https://hh.ru/vacancies/machine-learning-engineer
- [E5] HH.ru, DevOps Moscow listings, просмотрено 2026-06-09: https://hh.ru/vacancies/devops
- [E6] HH.ru, CTO Moscow listings, просмотрено 2026-06-09: https://hh.ru/vacancies/tehnicheskij-direktor-cto
- [E7] HH.ru, Sales Executive / Account Executive SaaS Moscow listings, просмотрено 2026-06-09: https://hh.ru/vacancy/129749266 ; https://hh.ru/vacancy/129384172
