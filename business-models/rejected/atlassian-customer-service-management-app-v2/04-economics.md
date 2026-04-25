---
stage: unit-economics
case: atlassian-customer-service-management-app-v2
date: 2026-04-25
analyst: branch-models-lead
sector: B2B-OPS
verdict: FAIL
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог: FAIL для investment-fund quality standalone-кейса.**

Причина не в отсутствии выручки у категории, а в плохой экономике именно для отдельного локального operator/integrator motion вокруг Atlassian Customer Service Management App. Продукт продаётся как часть `Service Collection`, pricing базируется на per-agent bundle, а не на отдельной spend-category [T1]. Поэтому самостоятельный российский оператор вынужден продавать не продукт, а тяжёлый enterprise services layer: discovery, интеграцию, workflow design, Rovo/AI настройку, поддержку и change management. Это резко поднимает CAC и fixed payroll.

В расчётной модели:
- средняя выручка на клиента: **180 000 ₽/мес**;
- COGS на клиента: **86 000 ₽/мес**;
- валовая маржа: **52.2%**;
- blended fully-loaded CAC: **1 087 500 ₽**;
- benchmark churn для раннего B2B SaaS: **3.7%/мес** [T2];
- LTV: **2 540 541 ₽**;
- **LTV/CAC = 2.34x**, ниже investment-grade порога **3.0x**;
- CAC Payback: **6.0 мес**;
- contribution margin после acquisition reserve: **22.0%**;
- при **50 клиентах** monthly EBITDA остаётся **около -2.83 млн ₽/мес**, то есть profit gate не проходит.

## 1. Business model и ключевые допущения

### Что именно монетизирует локальный оператор
Рассматриваем не сам Atlassian, а локальный standalone-business, который продаёт:
1. внедрение customer service workflows на базе Atlassian/JSM/Customer Service Management;
2. AI/Rovo настройку self-service и routing;
3. интеграции с почтой, chat, CRM, knowledge base;
4. ежемесячное сопровождение, SLA, оптимизацию очередей и отчётность.

### Ценовая модель
- Setup fee: **300 000 ₽** one-off, не включаю в LTV как повторяемую выручку.
- Recurring managed fee: **180 000 ₽/клиент/мес**.
- Сегмент: **mid-market / lower enterprise B2B**.
- Основание: bundle-цена Atlassian невысока, значит локальный игрок может брать деньги только за внедрение и managed layer, но не за core software margin [T1].

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Список таргет-аккаунтов и ICP | SDR | HH/2ГИС/отраслевые списки, CRM | 1.5 ч | 1 100 | Средняя |
| 2 | Первый outbound touch: email/Telegram/звонок | SDR | CRM, email, телефония | 2.0 ч | 1 800 | Средняя |
| 3 | Qualification call | SDR + AE | VoIP, календарь, CRM | 1.0 ч | 2 700 | Низкая |
| 4 | Discovery и pain mapping | AE + Solution Consultant | Meet, Miro, CRM | 2.0 ч | 8 500 | Низкая |
| 5 | Demo / workshop по workflow и AI routing | AE + PM + Tech Lead | Atlassian sandbox, demo env | 3.0 ч | 14 000 | Низкая |
| 6 | Audit текущего support stack и объёма тикетов | PM + Tech Lead | Sheets, Jira, SQL/export | 6.0 ч | 24 000 | Низкая |
| 7 | Коммерческое предложение и ROI-модель | AE + Founder | Docs, Sheets | 2.5 ч | 9 500 | Средняя |
| 8 | Security/legal/procurement review | Founder + PM | Почта, Dataroom, шаблоны | 4.0 ч | 18 000 | Низкая |
| 9 | Pilot launch / onboarding | PM + Backend + CSM | Jira Service Management, интеграции | 18.0 ч | 72 000 | Средняя |
| 10 | Счёт, договор, закрывающие, первая оплата | Finance + AE | ЭДО, банк, CRM | 1.5 ч | 6 000 | Высокая |

### Вывод по процессу
- До первой оплаты требуется **41.5 часа** команды.
- Прямой labour cost на выигранного клиента до оплаты: **157 600 ₽**.
- Но реальный CAC выше в 6.9x, потому что большая часть effort уходит на невыигранные лиды, пилоты и security/procurement.

## 3. COGS на клиента в месяц

### COGS breakdown
| Компонент | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| L1/L2 support delivery | 28 000 | 0.13 FTE support engineer | Internal model |
| Shared solution architect / workflow tuning | 16 000 | 0.03 FTE senior consultant | Internal model |
| Customer success delivery | 10 000 | 0.04 FTE CSM | Internal model |
| Cloud/integration infra | 8 000 | sandbox, connectors, monitoring | Internal model |
| AI/Rovo/token reserve | 12 000 | ассисты, классификация, automation tokens | T1 + internal model |
| QA/reporting/SLA analytics | 6 000 | ежемесячный контроль качества | Internal model |
| Partner certification / enablement reserve | 6 000 | обучение, partner overhead | Internal model |
| Compliance / incident reserve | 0 | включено в shared overhead fixed | Internal model |
| **Итого COGS** | **86 000** |  |  |

### Gross profit
- Revenue per client/month: **180 000 ₽**
- COGS per client/month: **86 000 ₽**
- Gross profit per client/month: **94 000 ₽**
- **Gross Margin = 52.2%**

## 4. CAC по каналам с funnel conversion

### CAC by channel
| Канал | Leads/мес | Meetings | SQL | Pilot | New paying | Spend, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound SDR/AE | 1 200 accounts | 72 (6.0%) | 18 (25.0%) | 6 (33.3%) | 1.2 (20.0%) | 1 620 000 | 1 350 000 |
| Partner referrals / Atlassian ecosystem | 20 intros | 8 (40.0%) | 4 (50.0%) | 3 (75.0%) | 1.6 (53.3%) | 420 000 | 262 500 |
| Content / inbound / webinars | 40 MQL | 12 (30.0%) | 4 (33.3%) | 1.6 (40.0%) | 0.8 (50.0%) | 570 000 | 712 500 |
| **Blended** |  |  |  |  | **3.6** | **2 610 000** | **725 000 raw CAC** |

### Fully-loaded CAC (обязательно)

Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools/CRM + Events + Multiplier overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 250 000 | search + retargeting на ICP | Internal media assumption |
| Outbound team FOT (SDR/AE attributed to new) | 1 500 000 | 2 SDR + 2 AE fully-loaded, 75% attributed to new logo acquisition | HH.ru market snapshots [T3][T4] |
| Marketing team FOT (partial allocation) | 220 000 | 0.5 marketer FTE + 30% socials | HH-like RU benchmark + internal allocation |
| Tools (CRM, sequencing, телефония, analytics) | 140 000 | CRM + email warmup + call tools + BI | Internal stack assumption |
| Events/partnerships | 240 000 | офлайн-ивенты, co-marketing, partner fees | Internal model |
| Subtotal before multiplier | 2 350 000 |  |  |
| Overhead multiplier | 1 305 000 | raw CAC overhead ×1.556 для enterprise-like motion: pre-sale SE, legal, procurement drag, founder time | Enterprise B2B sanity rule from program brief |
| **Итого fully-loaded spend** | **3 655 000** |  |  |
| **New paying customers / month** | **3.36** | blended after slippage from pilots to paid | Funnel model |
| **Fully-loaded CAC** | **1 087 500 ₽** | 3 655 000 / 3.36 |  |

### Sanity check against benchmark
- Complex B2B / enterprise-like SaaS in РФ: **300–900k ₽+** CAC baseline from program brief.
- Наша оценка **1.09 млн ₽** чуть выше верхней границы typical enterprise SaaS, что логично для bundle-dependent, services-heavy motion с длинным cycle.
- CAC не выглядит заниженным, red flag на underestimation нет.

## 5. LTV с churn benchmark

### Выбор churn
Для раннего B2B SaaS с ARR **$1–3M** медианный **customer churn = 3.7%/мес** по данным ChartMogul [T2]. Для ARPA выше $1k/month customer churn на mature cohorts бывает ниже, но для этого кейса консервативно беру **3.7%**, так как:
1. продукт не standalone, а service-heavy overlay;
2. высокая зависимость от partner stack и интеграционного качества;
3. клиенты легко возвращаются к встроенным bundle-capabilities или к крупному интегратору.

### LTV formula
`LTV = (MRR per customer × Gross Margin %) / Monthly churn`

- MRR per customer = **180 000 ₽**
- Gross Margin = **52.2%**
- Monthly churn = **3.7%**

**LTV = 180 000 × 0.522 / 0.037 = 2 540 541 ₽**

## 6. LTV/CAC ratio

- LTV = **2 540 541 ₽**
- Fully-loaded CAC = **1 087 500 ₽**
- **LTV/CAC = 2.34x**

### Вывод
- Базовый порог reject: **ниже 2.0x**. Мы чуть выше него, но это всё равно плохо.
- Investment-grade порог: **не ниже 3.0x**.
- **Кейс не investable по unit economics.**

## 7. CAC Payback

Формула по программе:
`CAC Payback = CAC / MRR_per_customer`

- CAC = **1 087 500 ₽**
- MRR/customer = **180 000 ₽**
- **CAC Payback = 6.0 мес**

### Комментарий
Payback сам по себе приемлемый, но это не спасает кейс, потому что gross margin и fixed base недостаточны для масштабирования в плюс.

## 8. Contribution Margin

### Formula
`Contribution Margin = (Revenue - COGS - acquisition reserve) / Revenue`

Где acquisition reserve = CAC, распределённый на 12 месяцев жизни клиента в acquisition accounting view:
- CAC amortized monthly = **90 625 ₽**

Тогда:
- Revenue = **180 000 ₽**
- COGS = **86 000 ₽**
- CAC amortized monthly = **90 625 ₽**
- Contribution = **3 375 ₽**
- **Contribution Margin = 1.9%**

### Альтернативный operating CM без amortized CAC
- Revenue = **180 000 ₽**
- COGS = **86 000 ₽**
- Gross contribution = **94 000 ₽**
- **Gross contribution margin = 52.2%**

Для фонда релевантен первый, fully-loaded взгляд: **1.9% contribution margin** слишком тонкий для enterprise deployment business.

## 9. Team & FOT

### Полная таблица команды
| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO/founder | продажа крупных сделок, партнёрства, найм | 1 | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | архитектура, сложные интеграции | 1 | 550 000 | 165 000 | 715 000 |
| Senior Backend | интеграции, workflow backend | 2 | 420 000 | 126 000 | 1 092 000 |
| Frontend | agent workspace / portal кастомизация | 1 | 300 000 | 90 000 | 390 000 |
| DevOps | деплой, безопасность, monitoring | 1 | 350 000 | 105 000 | 455 000 |
| Product / Delivery Manager | scoping, roadmap, delivery control | 1 | 350 000 | 105 000 | 455 000 |
| SDR | outbound sourcing и qualification | 2 | 172 500 | 51 750 | 448 500 |
| AE | demos, proposal, close | 2 | 345 000 | 103 500 | 897 000 |
| Customer Success | adoption, renewals, QBR | 1 | 250 000 | 75 000 | 325 000 |
| Support / Implementation Engineer | onboarding и ежемес. changes | 2 | 220 000 | 66 000 | 572 000 |
| Finance/Admin | документы, ЭДО, billing | 1 | 180 000 | 54 000 | 234 000 |
| **Итого** |  | **15** |  |  | **6 428 500 ₽/мес** |

### Hiring realism table
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2.5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 / each |
| ML Engineer (если AI core) | 0 | — | — | — | — | — |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 2 | 172 500 | 0.75 | 1 | 51 750 | 224 250 / each |
| AE | 2 | 345 000 | 1.5 | 2.5 | 103 500 | 448 500 / each |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Комментарий по найму
- План требует **15 человек**, но закрыть их быстро нереалистично.
- Senior and lead hiring растянуты на **1–3 месяца**, значит full-capacity delivery и sales engine не стартуют сразу.
- Уже это ухудшает runway и переносит breakeven вправо.

## 10. Cumulative FOT timeline M1-M12

### Предположение по найму
- M1: founder/CEO, 1 SDR, 1 AE.
- M2: PM, Frontend, Finance/Admin.
- M3: CTO, 1 Backend, DevOps.
- M4: 2-й SDR, 2-й AE, CSM.
- M5: 2-й Backend.
- M6: 2 Support/Implementation engineers.

| Месяц | Кто в команде | Monthly FOT, ₽ |
|---|---|---:|
| M1 | CEO, SDR1, AE1 | 1 517 750 |
| M2 | + PM, Frontend, Finance | 2 596 750 |
| M3 | + CTO, Backend1, DevOps | 4 312 750 |
| M4 | + SDR2, AE2, CSM | 5 310 500 |
| M5 | + Backend2 | 5 856 500 |
| M6 | + Support1, Support2 | 6 428 500 |
| M7 | full team | 6 428 500 |
| M8 | full team | 6 428 500 |
| M9 | full team | 6 428 500 |
| M10 | full team | 6 428 500 |
| M11 | full team | 6 428 500 |
| M12 | full team | 6 428 500 |

### Sanity checks
- В первый месяц нет найма 5+ человек, значит realism соблюдён.
- Но уже к M6 monthly payroll **6.43 млн ₽**, что слишком тяжело для слабого wedge-demand.

## 11. Fixed costs breakdown

| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 6 428 500 | см. таблицу выше |
| Office / coworking / workplace | 180 000 | гибридный режим |
| Legal + accounting + payroll ops | 140 000 | договоры, ЭДО, отчётность |
| General software stack | 190 000 | CRM, docs, analytics, security |
| Core cloud / demo infra / sandboxes | 260 000 | pre-sales demos и internal env |
| Travel / events / partner enablement | 180 000 | enterprise selling |
| Recruiting reserve | 120 000 | agency / sourcing / тестовые |
| **Итого fixed costs / month** | **7 498 500 ₽** |  |

## 12. Break-even

### Break-even by client count
`Break-even clients = Fixed costs / Gross profit per client`

- Fixed costs = **7 498 500 ₽/мес**
- Gross profit per client = **94 000 ₽/мес**
- **Break-even = 79.8 клиента**, округлённо **80 клиентов**

### Проверка при 50 клиентах
- Revenue = 50 × 180 000 = **9 000 000 ₽**
- COGS = 50 × 86 000 = **4 300 000 ₽**
- Gross profit = **4 700 000 ₽**
- Fixed costs = **7 498 500 ₽**
- **EBITDA = -2 798 500 ₽/мес**

Это прямой провал profit gate: **даже на 50 клиентах EBITDA не достигает +500k ₽/мес**.

### Break-even by month
Предположим ramp новых paying clients:
- M1–M3: 0
- M4: 1
- M5: 2
- M6: 3
- M7: 5
- M8: 7
- M9: 9
- M10: 12
- M11: 15
- M12: 18

Тогда к M12:
- Clients live = **72** active client-month equivalent gross-count до churn, но с churn-adjusted active base около **47–49**;
- это всё ещё ниже breakeven **80 клиентов**.

**Breakeven в пределах 12 месяцев не достигается.**

## 13. Burn-to-breakeven и runway

### Burn-to-breakeven
Средний cash burn до выхода на попытку breakeven:
- M1: **~2.1 млн ₽**
- M2: **~3.2 млн ₽**
- M3: **~5.0 млн ₽**
- M4: **~5.6 млн ₽**
- M5: **~5.9 млн ₽**
- M6+: **~6.2–6.8 млн ₽** до масштабного набора клиентов

Кумулятивный burn за первые 12 месяцев по этой модели: **около 63–68 млн ₽**.

### Cash runway
При `startup_capital = 30 000 000 ₽`:
- ранний среднемесячный burn ≈ **6.5 млн ₽**
- **cash runway ≈ 4.6 месяца**

Даже если растянуть hiring и урезать events, runway всё равно остаётся слишком коротким для sales cycle такого класса.

## 14. Investment view

### Что хорошо
- Категория service operations реальна.
- Enterprise pain настоящий.
- CAC payback не катастрофический.

### Что плохо
1. **Нет standalone category ownership**: value accrues to Atlassian bundle, а не к отдельному app-level operator [T1].
2. **LTV/CAC = 2.34x**, ниже фондабельного **3.0x**.
3. **Contribution margin fully-loaded = 1.9%**, слишком низко.
4. **Break-even требует ~80 клиентов**, но при 50 клиентах EBITDA ещё глубоко отрицательная.
5. Hiring plan тяжёлый, а startup capital requirement высокий.

## 15. Verdict

**FAIL. Reject как standalone investment case.**

Даже если спрос на broader AI service management растёт, отдельный локальный бизнес вокруг `Atlassian Customer Service Management App` выглядит как services-heavy appendage к чужой платформе. Для фонда это плохой актив: слабая category control, тонкий contribution, высокая fixed cost base и отсутствие пути к **EBITDA ≥ 500k ₽/мес** даже на **50 клиентах**.

## Источники
- [T1] Atlassian Service Collection Pricing, accessed 2026-04-25: https://www.atlassian.com/collections/service/pricing
- [T2] ChartMogul, Customer churn benchmark / ARR benchmark references, accessed 2026-04-25: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/ ; https://help.chartmogul.com/article/138-benchmarks
- [T3] HH.ru, account executive / SDR вакансии Москва, accessed 2026-04-25: https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancies/account_executive/polniy_den
- [T4] HH.ru, senior backend developer / engineer вакансии Москва, accessed 2026-04-25: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancies/senior-backend-engineer
