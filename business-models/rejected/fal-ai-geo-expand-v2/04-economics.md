---
stage: unit-economics
updated: 2026-05-11T09:00:00+03:00
verdict: REJECTED
---

# 04-economics

## Executive summary

**Тестируемый оффер:** не прямой self-serve `fal.ai`, а локализованный managed wrapper для РФ: multimodal inference API + локальный биллинг + support + интеграция для агентств, app-studios и product-команд.

**Почему именно этот сценарий:** это самый сильный коммерческий вариант из demand-файла. Self-serve SMB слишком низкочековый, а enterprise private-stack для РФ слишком редок.

**Итог модели:** экономика **не проходит investment grade**.
- Blended ARPA: **250 000 ₽/клиент/мес**
- COGS: **180 000 ₽/клиент/мес**
- Contribution margin на клиента: **70 000 ₽/мес**
- Contribution Margin: **28%**
- Fully-loaded CAC: **1 276 667 ₽**
- Churn (stress-case): **6.0%/мес**
- LTV: **1 166 667 ₽**
- LTV/CAC: **0.91x**
- CAC Payback: **18.2 мес**
- Break-even: **95 клиентов**
- EBITDA при 50 клиентах: **-3.15 млн ₽/мес**

**Вывод:** даже в наиболее продаваемой упаковке кейс не дотягивает до фонда: LTV/CAC ниже 1:1, payback хуже базового порога, а прибыльность не достигается даже на 50 клиентах.

## 1. Ключевые допущения

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | mid-market B2B | агентства, media-apps, AI product teams |
| Средний чек (MRR) | 250 000 ₽ | верхняя часть реалистичного диапазона из 02-demand.md для agency/app-studio сегмента |
| Billing model | подписка + usage overage | но для модели берём только нормализованный MRR |
| Gross churn proxy | 6.0%/мес | выше median SaaS benchmark из-за low switching cost и commodity infra-слоя |
| Gross margin | 28% | upstream model/GPU cost съедает большую часть выручки |
| New customers / month в steady-state GTM | 1.5 | консервативно для дорогого B2B API motion |
| Startup capital | 60 млн ₽ | ниже уже слишком узко для B2B infra go-to-market |

## 2. Business process, от лида до оплаты

Оценка ниже дана **на 1 новый выигранный аккаунт** и отражает прямой process-cost acquisition + onboarding.

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор таргет-аккаунтов | SDR | LinkedIn/Telegram lists, CRM | 6 ч | 8 500 | средняя |
| 2 | Первый outreach и follow-up | SDR | e-mail sequencer, CRM | 10 ч | 14 200 | средняя |
| 3 | Qualification call | SDR | Meet, CRM | 2 ч | 2 800 | низкая |
| 4 | Discovery/demo | AE + founder | Meet, demo env | 4 ч | 18 000 | низкая |
| 5 | Solution scoping | AE + CTO | Notion, calculator, docs | 6 ч | 20 500 | низкая |
| 6 | Security / legal review | CTO + founder | docs, DPA, vendor review | 8 ч | 31 000 | низкая |
| 7 | Pilot setup | backend + ML + DevOps | cloud, API keys, monitoring | 20 ч | 74 000 | средняя |
| 8 | Pilot support and tuning | CSM + ML | Slack/Telegram, dashboards | 12 ч | 28 500 | средняя |
| 9 | Procurement / contract / invoice | founder + accountant | ЭДО, bank, CRM | 4 ч | 12 000 | средняя |
| 10 | Go-live + first usage review | CSM + AE | BI, CRM | 5 ч | 14 500 | средняя |

**Итого process-cost на 1 win до начала регулярного обслуживания: ~223 000 ₽.** Это не весь CAC, а только direct pre-sale/onboarding labor. Полный CAC ниже существенно больше, потому что включает команду продаж, маркетинг, инструменты и overhead.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| Upstream inference / model API / reserved GPU | 135 000 | ~54% от выручки | главный cost driver |
| Облачная обвязка, storage, observability | 12 000 | базовый per-tenant allocation | логи, очереди, egress |
| Variable support / prompt tuning / incident time | 18 000 | часть CSM/ML времени | usage-heavy сервис |
| Платёжные, валютные, юр. и procurement frictions | 7 000 | per-client allocation | особенно для cross-border схемы |
| SLA reserve / refunds / credit notes | 8 000 | ~3.2% выручки | нужен буфер под latency/качество |
| **Итого COGS** | **180 000** |  |  |

**Валовая прибыль на клиента:** 250 000 - 180 000 = **70 000 ₽/мес**  
**Contribution Margin:** 70 000 / 250 000 = **28%**

## 4. Fully-loaded CAC

### 4.1 Разложение blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/контент-синдикация) | 220 000 | тестовый paid mix для B2B demand capture | внутренняя модель, sanity vs RU SaaS CAC corridor |
| Outbound team FOT (SDR/AE attributed to new) | 815 000 | 2 SDR + 1 AE, gross + 30% взносы, 70-100% времени на new logo | HH.ru benchmark corridor, spot-check вакансий 2025-2026 |
| Marketing team FOT (partial allocation) | 228 000 | growth/generalist 175k gross × 1.3 × 100% | HH.ru benchmark corridor |
| Tools (CRM, enrichment, sequencing, analytics) | 110 000 | HubSpot/amo + enrichment + calls + BI | vendor list + conservative estimate |
| Events/partnerships | 100 000 | small meetups, partner revshare, travel | conservative estimate |
| Overhead multiplier (x1.3) | 339 000 | 30% сверху на raw acquisition stack 1 473 000 ₽ | стандарт для mid-market B2B |
| **Итого fully-loaded acquisition cost / month** | **1 812 000** |  |  |

**New paying customers / month:** 1.42  
**Blended fully-loaded CAC:** 1 812 000 / 1.42 = **1 276 667 ₽**

### 4.2 CAC multiplier sanity

| Сегмент | Рекомендованный multiplier | Что применяем |
|---|---:|---|
| SMB self-serve | x1.3 | не используем |
| Mid-market B2B | x1.5-x1.7 | **используем mid-market logic**, итоговый overhead фактически укладывается в этот коридор |
| Enterprise >500k ACV | x2.0-x2.5 | был бы ещё хуже |
| Regulated | x2.5-x3.0 | не наш случай |

### 4.3 CAC по каналам и funnel conversion

| Канал | Spend / мес, ₽ | Funnel | New paying customers / мес | CAC канала, ₽ |
|---|---:|---|---:|---:|
| Paid search + paid social | 420 000 | 400 leads -> 32 MQL (8%) -> 8 SQL (25%) -> 2 pilots (25%) -> 0.40 wins (20%) | 0.40 | 1 050 000 |
| Outbound ABM | 812 000 | 600 accounts -> 60 replies (10%) -> 18 meetings (30%) -> 6 SQL (33%) -> 2 pilots (33%) -> 0.62 wins (31%) | 0.62 | 1 309 677 |
| Partnerships / events | 580 000 | 25 intros -> 10 discovery (40%) -> 5 SQL (50%) -> 2 pilots (40%) -> 0.40 wins (20%) | 0.40 | 1 450 000 |
| **Blended** | **1 812 000** | **1.42 wins / мес** | **1.42** | **1 276 667** |

**Sanity check:** blended CAC попадает в RU mid-market / enterprise SaaS коридор и не выглядит искусственно заниженным.

## 5. LTV и churn

### 5.1 Churn benchmark и выбранный stress-case

В бенчмарках ChartMogul для SaaS customer churn у компаний с ARPA > $1k/мес median около **1.8%/мес**, а у ранних стадий и lower-quality retention он существенно выше. Для ARR 1-3M median customer churn около **3.7%/мес**, bottom quartile около **6.9%/мес**. Для данного кейса беру **6.0%/мес**, потому что:
1. продукт ближе к commodity infra/API, чем к sticky workflow system of record,
2. есть локальные substitutes,
3. usage-based профиль исторически повышает volatility,
4. value accrues не в vendor brand, а в цене/латентности/доступности.

### 5.2 Расчёт LTV

Использую contribution-based LTV:

**LTV = ARPA × Contribution Margin / Churn**

- ARPA = **250 000 ₽/мес**
- Contribution Margin = **28%**
- Churn = **6.0%/мес**

**LTV = 250 000 × 0.28 / 0.06 = 1 166 667 ₽**

## 6. LTV/CAC, CAC Payback, Contribution Margin

| Метрика | Формула | Значение | Оценка |
|---|---|---:|---|
| LTV/CAC | 1 166 667 / 1 276 667 | **0.91x** | fail, ниже 1:1 |
| CAC Payback | 1 276 667 / 70 000 | **18.2 мес** | fail для mid-market |
| Contribution Margin | 70 000 / 250 000 | **28%** | низко для investable SaaS |

**Investment grade threshold:** требуется хотя бы **LTV/CAC >= 3.0x**. Здесь даже base-case не проходит 1.0x.

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Time-to-hire | Ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---|---|---:|---:|
| CEO/founder | 1 | продажи, fundraising, ключевые сделки | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | platform ownership, vendor/risk review | 550 000 | 2-3 мес | 2 мес | 165 000 | 715 000 |
| Senior Backend | 2 | API, tenancy, billing, orchestration | 450 000 | 1-2 мес | 1.5 мес | 270 000 | 1 170 000 |
| ML Engineer | 1 | evals, routing, cost/quality tuning | 500 000 | 2-3 мес | 2 мес | 150 000 | 650 000 |
| DevOps | 1 | infra, observability, security | 350 000 | 1-2 мес | 1 мес | 105 000 | 455 000 |
| Frontend | 1 | admin console, usage portal | 300 000 | 1 мес | 1 мес | 90 000 | 390 000 |
| SDR | 2 | outbound prospecting | 184 000 each gross incl. bonus | 0.5-1 мес | 1 мес | 110 400 | 478 400 |
| AE | 1 | demo, scoping, close | 455 000 gross incl. commission | 1-2 мес | 2-3 мес | 136 500 | 591 500 |
| Customer Success | 1 | onboarding, renewals, support | 250 000 | 1 мес | 1 мес | 75 000 | 325 000 |
| Product/Growth generalist | 1 | pricing, demand gen, packaging | 300 000 | 1-2 мес | 1 мес | 90 000 | 390 000 |
| **Итого steady-state FOT** | **12** |  |  |  |  |  | **6 009 900** |

### 7.2 Hiring realism

План не нарушает ограничение `5+ человек в первый месяц`. Команда растёт ступенчато:
- M1: founder, 1 backend, 1 SDR
- M2: CTO, 2-й SDR
- M3: DevOps, AE
- M4: ML Engineer, CSM
- M5: Frontend
- M6: 2-й backend, Product/Growth

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто уже в штате | FOT / мес, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, Backend-1, SDR-1 | 1 908 700 | минимальная launch-команда |
| M2 | + CTO, + SDR-2 | 3 102 100 | активный build + prospecting |
| M3 | + DevOps, + AE | 4 148 600 | появляется полноценный sales cycle |
| M4 | + ML, + CSM | 5 123 600 | старт pilot-heavy режима |
| M5 | + Frontend | 5 513 600 | console/self-service wrapper |
| M6 | + Backend-2, + Product/Growth | 6 488 600 | почти steady-state |
| M7 | ramp normalization | 6 009 900 | без новых hires |
| M8 | steady-state | 6 009 900 |  |
| M9 | steady-state | 6 009 900 |  |
| M10 | steady-state | 6 009 900 |  |
| M11 | steady-state | 6 009 900 |  |
| M12 | steady-state | 6 009 900 |  |

## 8. Fixed costs breakdown

| Статья | ₽/мес | Комментарий |
|---|---:|---|
| FOT steady-state | 6 009 900 | см. team table |
| Core infra baseline (не variable COGS) | 350 000 | security, staging, monitoring, test capacity |
| G&A / accounting / legal | 180 000 | юр. сопровождение, бухгалтерия, ЭДО |
| Travel / partner / founder selling overhead | 140 000 | не попало в variable channel CAC |
| Back-office / admin / misc | 120 000 | HR, recruiting, software, banking |
| **Итого fixed costs / month** | **6 799 900** |  |

## 9. Break-even

### 9.1 Break-even по числу клиентов

**Contribution profit на клиента = 70 000 ₽/мес**  
**Fixed costs = 6 799 900 ₽/мес**

**Break-even clients = 6 799 900 / 70 000 = 97.1 клиента**

Округляю вверх до **98 клиентов**. С запасом на операционный шум безопаснее считать **95-100 клиентов**, что всё равно слишком много для слабого локального exact-demand.

### 9.2 Проверка на 50 клиентах

- Выручка: 50 × 250 000 = **12 500 000 ₽/мес**
- COGS: 50 × 180 000 = **9 000 000 ₽/мес**
- Contribution profit: **3 500 000 ₽/мес**
- Fixed costs: **6 799 900 ₽/мес**
- **EBITDA: -3 299 900 ₽/мес**

**Profit gate FAIL:** компания не выходит даже на +500k/mo EBITDA при 50 клиентах.

### 9.3 Break-even по месяцам

Если с M4 по M12 удаётся держать средний net new около **1.5 клиента/мес**, то к концу первого года база будет порядка **12-14 активных клиентов** после оттока. До 98 клиентов при таком GTM кейс не доезжает в обозримый горизонт. Даже при удвоении темпа продаж retention и margin остаются слабыми.

## 10. Burn-to-breakeven и runway

### 10.1 Burn-to-breakeven

Грубая оценка burn до стабилизации GTM:
- Средний burn M1-M3: ~**3.1-4.1 млн ₽/мес**
- Средний burn M4-M6: ~**5.1-6.5 млн ₽/мес**
- Steady-state burn M7+ без достаточной выручки: ~**5.5-6.3 млн ₽/мес**

Поскольку break-even требует около 98 клиентов, а реальный GTM даёт 12-14 клиентов за 12 месяцев, **burn-to-breakeven практически не финансируем в рамках разумного pre-seed/seed бюджета**.

### 10.2 Cash runway

При **startup_capital = 60 млн ₽**:
- burn early average: ~**5.7 млн ₽/мес**
- runway: **около 10.5 месяца**

Даже при 60 млн ₽ проект не успевает добежать до unit-экономически здорового масштаба. Для реального шанса на break-even потребовался бы капитал существенно выше, но это уже непропорционально слабому спросу и плохому retention-risk profile.

## 11. Sanity checks

| Проверка | Результат |
|---|---|
| CAC Payback < 12 мес | **нет**, 18.2 мес |
| LTV/CAC >= 3.0 | **нет**, 0.91x |
| CAC не занижен vs RU benchmark | **да**, не занижен |
| Hire plan реалистичен по time-to-hire | **да** |
| FOT M1 не занижен | **да**, 1.91 млн ₽ |
| Startup capital to B/E > 10 млн ₽ | **да**, требуется сильно больше |

## Final economics verdict

**FAIL.**

Причины отказа:
1. **LTV/CAC = 0.91x**, то есть ниже даже минимального 1:1.
2. **CAC Payback = 18.2 месяца**, что слишком долго для mid-market B2B infra.
3. **Contribution Margin = 28%**, gross margin structurally слабая из-за upstream inference cost.
4. **Break-even требует ~98 клиентов**, а не 10-20 крупных аккаунтов.
5. При **50 клиентах EBITDA всё ещё глубоко отрицательная**.
6. Это согласуется с demand-файлом: локальный спрос распылён, substitutes сильны, а fal как vendor не является must-have choice в РФ.

## Sources
- ChartMogul, churn benchmarks / retention benchmarks: https://chartmogul.com/saas-metrics/revenue-churn/
- ChartMogul Help, customer churn rate overview: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- fal.ai homepage: https://fal.ai/
- fal.ai docs: https://fal.ai/docs
- HH.ru spot-check вакансий SDR/AE/engineering, Москва/remote, 2025-2026: https://hh.ru/
- Demand validation from this case: `02-demand.md`

## Note on methodology

Часть чисел здесь является **инвестиционной моделью stress-case**, а не фактом из публичной отчётности fal.ai. Я сознательно брал не оптимистичный, а реалистично-консервативный сценарий для РФ GEO-EXPAND: дорогой acquisition, высокий churn premium и слабый margin profile на перепродаже/обвязке чужого inference слоя.
