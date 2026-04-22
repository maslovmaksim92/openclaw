---
stage: economics
case: rogo-finance-workflow-geo-expand-v2
date: 2026-04-23
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Rogo GEO Expand v2, enterprise AI для investment banking / corpdev / buy-side workflow automation в РФ.

## Executive summary

**Итог P5: REJECTED.**

Почему:
1. **Profit Gate не пройден.** Даже при **50 клиентах** модель даёт только **-3,44 млн ₽ EBITDA/мес**, то есть порог `EBITDA > 500k ₽/мес` не достигается. [T1][T2]
2. **Break-even требует ~93 клиентов**, что выше реалистичного buyer universe для РФ-контура и выше консервативного SAM из `02-demand.md`. [T1]
3. **LTV/CAC = 5,3x** и payback 5,6 мес сами по себе выглядят нормально, но они не спасают кейс, потому что fixed-cost base и service-heavy delivery делают локальный expansion structurally unprofitable. [T1][T2]
4. Основная проблема не в отсутствии ценности, а в том, что в РФ это слишком узкий enterprise workflow с дорогим внедрением, длинным sales cycle и ограниченным числом покупателей. [T1]

## 1. Модель и ключевые допущения

### ICP
- CIB и corporate finance команды крупных банков;
- buy-side / asset management / special situations;
- corpdev / strategy команды крупных корпораций;
- advisory teams, которым нужен ускоренный memo, comp set, due diligence prep и company research.

### Монетизация, base case для РФ
- Подписка: **200 000 ₽/клиент/мес**
- ARR на клиента: **2,4 млн ₽/год**
- Onboarding / initial setup: **700 000 ₽** one-off
- Для unit economics считаю recurring отдельно, onboarding использую как частичную компенсацию cash burn, но **не включаю в MRR**.

### Почему беру 200k ₽ MRR
Это середина реалистичного диапазона `1,5–3,0 млн ₽ ARR` из `02-demand.md` для enterprise workflow-команды в РФ. Ниже модель не окупает sales motion, выше нужен уже очень сильный локальный PMF и подтверждённый security/compliance trust, чего в кейсе пока нет. [T1]

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target accounts: банки, УК, corpdev, advisory | SDR / founder | Rusprofile, Контур.Фокус, CRM | 2,0 ч | 2 300 | Низкий |
| 2 | Account research и contact mapping | SDR | HH, LinkedIn analogs, Telegram, CRM | 1,5 ч | 1 700 | Низкий |
| 3 | Первичный outbound / intro | SDR | email, phone, Telegram, sequence tool | 1,5 ч | 1 700 | Средний |
| 4 | Qualification call | SDR + AE | Meet, CRM, qualification script | 1,0 ч | 3 200 | Средний |
| 5 | Discovery по текущему workflow клиента | AE + founder | Meet, Miro, questionnaire | 2,0 ч | 9 500 | Низкий |
| 6 | Demo на реальном use case | AE + solutions / analyst | sandbox, prompt templates, demo deck | 2,5 ч | 12 500 | Низкий |
| 7 | Pilot scoping и success criteria | AE + CSM + founder | SOW, ROI calculator, CRM | 3,0 ч | 16 000 | Низкий |
| 8 | Security / legal pre-check | AE + CTO | NDA, trust docs, security checklist | 3,0 ч | 13 500 | Низкий |
| 9 | Пилотная настройка: данные, шаблоны, роли | solutions + CSM | workspace, connectors, prompt config | 14,0 ч | 56 000 | Средний |
| 10 | Enablement команды клиента | CSM + analyst | Zoom, docs, training runbook | 4,0 ч | 15 000 | Средний |
| 11 | Pilot support 4-6 недель | CSM + founder + support | support desk, analytics, weekly reviews | 12,0 ч | 42 000 | Средний |
| 12 | Procurement / legal / pricing negotiation | AE + founder + finance | contract workflow, email, ЭДО | 8,0 ч | 31 000 | Низкий |
| 13 | Invoice и контроль оплаты | finance ops | 1С / банк / ЭДО | 1,0 ч | 2 500 | Высокий |
| 14 | Production onboarding после оплаты | CSM + support + solutions | runbook, monitoring, admin setup | 8,0 ч | 28 000 | Средний |

### Вывод по процессу
Продажа идёт как **enterprise consultative sale**, а не как SaaS self-serve. До оплаты в сделке много ручного труда, пилот, security review и procurement. Это объясняет высокий fully-loaded CAC и ограничивает масштабирование. [T1]

## 3. COGS per client / month

### Разбивка COGS на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM inference / reruns / eval | 24 000 | активный research + synthesis workflow |
| Financial / company data enrichment | 18 000 | внешние data sources и enrichment |
| Secure hosting / storage / audit logs | 16 000 | выделенный контур, хранение, бэкапы |
| Support L1-L2 | 12 000 | доля support engineer |
| CSM / account operations | 18 000 | доля CSM на активный аккаунт |
| Analyst QA / prompt tuning | 10 000 | ручная проверка критичных outputs |
| Implementation amortization | 15 000 | spread initial setup на 12 мес |
| Security / compliance allocation | 8 000 | доступы, policy, admin overhead |
| **Итого COGS** | **111 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **200 000 ₽**
- COGS на клиента: **111 000 ₽**
- Gross profit на клиента: **89 000 ₽**
- **Gross Margin = 44,5%**

### Комментарий
Для AI workflow в finance это правдоподобно, но для фонда слабовато. Такая валовая маржа говорит, что бизнес в РФ пока не pure software, а software plus delivery. [T1]

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 15 | 8 | 5 | 2 | 0,8 | 5,3% |
| Outbound targeted | 140 | 18 | 8 | 3 | 0,7 | 0,5% |
| Content / thought leadership | 30 | 8 | 4 | 2 | 0,4 | 1,3% |
| Partnerships / advisory referrals | 12 | 5 | 3 | 1 | 0,3 | 2,5% |
| **Итого blended** | **197** | **39** | **20** | **8** | **2,2** | **1,1%** |

### Fully-loaded CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

#### Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 220 000 | узкие brand + category tests, retargeting | модель для narrow B2B ICP |
| Outbound team FOT (SDR/AE attributed to new) | 1 235 000 | 2 SDR + 1 AE + 30% взносы + commission, 90% на new biz | HH.ru benchmark + модель [T3] |
| Marketing team FOT (partial allocation) | 260 000 | 0,5 PMM / founder marketing allocation + 30% | HH.ru benchmark + модель [T3] |
| Tools (CRM, outreach, enrichment, call stack) | 155 000 | CRM + sequence + enrichment + call recording + analytics | рыночное допущение |
| Events/partnerships | 280 000 | roundtables, finance events, partner development | рыночное допущение |
| Overhead multiplier (x1.3) | 320 000 | admin/ops/management overhead для acquisition stack | standard enterprise B2B |
| **Итого fully-loaded acquisition spend** | **2 470 000** |  |  |

#### Raw и blended CAC
- New paying customers / мес: **2,2**
- **Blended fully-loaded CAC = 2 470 000 / 2,2 = 1 122 727 ₽**

### CAC по каналам

| Канал | Direct spend + allocated team/tools, ₽/мес | New paying / мес | Raw CAC, ₽ | Multiplier | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|
| Founder-led / network | 300 000 | 0,8 | 375 000 | x1,5 | 562 500 |
| Outbound targeted | 1 180 000 | 0,7 | 1 685 714 | x1,7 | 2 865 714 |
| Content / inbound | 420 000 | 0,4 | 1 050 000 | x1,5 | 1 575 000 |
| Partnerships | 570 000 | 0,3 | 1 900 000 | x1,5 | 2 850 000 |
| **Blended** | **2 470 000** | **2,2** | **1 122 727** | n/a | **1 122 727** |

### Sanity check against RU benchmarks
- Enterprise SaaS B2B в РФ: **300-900k ₽/клиент**
- Fintech / finance B2B: **200-700k ₽/клиент**
- Complex enterprise workflow с пилотом, legal и security review может уходить **выше 1 млн ₽**

**Вывод:** blended CAC **1,12 млн ₽** выше типового benchmark, но для узкого enterprise finance workflow это не выглядит занижением. Наоборот, CAC ниже 500k ₽ здесь был бы red flag. [T1]

## 5. LTV и churn

### Churn benchmark
SaaS Capital показывает, что churn снижается по мере роста ACV, а enterprise B2B cohorts удерживаются лучше SMB. Для раннего geo-expand кейса в узкой вертикали беру **annual logo churn = 18%**: это хуже mature enterprise benchmark, но лучше SMB-профиля. [T2]

### Расчёт
- MRR на клиента: **200 000 ₽**
- ARR на клиента: **2 400 000 ₽**
- Gross Margin: **44,5%**
- Annual churn: **18%**

`LTV = ARR × GM / churn`

`LTV = 2 400 000 × 44,5% / 18% = 5 933 333 ₽`

### Вывод
- **LTV = 5,93 млн ₽**
- По unit economics value per retained client достаточная, но она не компенсирует слишком высокий fixed-cost base. [T1][T2]

## 6. LTV / CAC

- LTV: **5 933 333 ₽**
- Blended fully-loaded CAC: **1 122 727 ₽**

`LTV/CAC = 5 933 333 / 1 122 727 = 5,3x`

### Интерпретация
- **Формально метрика выше инвестиционного порога 3:1.**
- Но для фонда этого недостаточно, потому что компания не достигает EBITDA > 500k ₽/мес даже в стресс-тесте на 50 клиентов. Следовательно, reject идёт по Profit Gate, а не по LTV/CAC. [T1]

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`1 122 727 / 200 000 = 5,61 мес`

### Дополнительная проверка
Если смотреть payback по gross profit:

`1 122 727 / 89 000 = 12,62 мес`

### Вывод
- Номинально payback приемлем для enterprise.
- Но gross-profit payback уже на грани, а fixed costs слишком высоки, поэтому cash efficiency слабая. [T1]

## 8. Contribution Margin %

Для contribution margin беру выручку минус COGS минус переменные комиссии / success-support.

- Revenue per client / мес: **200 000 ₽**
- COGS: **111 000 ₽**
- Variable commission + success-support allocation: **8 000 ₽**

`Contribution profit = 81 000 ₽`

`Contribution Margin = 81 000 / 200 000 = 40,5%`

### Вывод
**Contribution Margin = 40,5%**. Для early enterprise AI это терпимо, но слишком мало, чтобы окупить тяжёлую команду в пределах российского buyer base. [T1]

## 9. Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|------------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 252 000 | 1 092 000 |
| ML Engineer | 1 | 520 000 | 2,5 | 2 | 156 000 | 676 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 2 | 160 000 + бонус 15% | 1 | 1 | 96 000 | 416 000 |
| AE | 1 | 320 000 + комиссия 7% | 1,5 | 2,5 | 96 000 | 416 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Solutions / finance analyst | 1 | 320 000 | 1,5 | 1,5 | 96 000 | 416 000 |
| Finance / ops | 0,5 | 95 000 | 1 | 0,5 | 28 500 | 123 500 |
| **Итого full team FOT** | **11,5** |  |  |  |  | **5 902 500 ₽/мес** |

### Функции команды

| Роль | Основная функция |
|---|---|
| CEO | founder-led sales, enterprise trust, fundraising |
| CTO | архитектура, security, customer delivery governance |
| Senior Backend | connectors, workflow engine, document assembly |
| ML Engineer | prompt systems, eval, retrieval quality |
| DevOps | secure deployment, monitoring, access control |
| Frontend | analyst UI, admin panel, collaboration layer |
| SDR | pipeline generation |
| AE | discovery, pilot close, negotiation |
| Customer Success | onboarding, adoption, renewals |
| Solutions / finance analyst | implementation, workflow tuning, domain QA |
| Finance / ops | billing, contracts, ЭДО |

### Salary source note
Диапазоны соответствуют standing benchmark по HH.ru для Москвы/СПб на 2026 год и не противоречат диапазонам из задания: senior SWE 350–550k, team lead 450–700k, ML 400–700k, SDR 100–180k + bonus, AE 300–500k + commission. [T3]

## 10. Cumulative FOT timeline M1-M12

### План найма с учётом time-to-hire и ramp

| Месяц | Кто в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, 1 Backend, 1 Frontend, 1 SDR | 2 210 000 |
| M2 | + Customer Success, + 0,5 Finance/Ops | 2 728 000 |
| M3 | + DevOps, + AE | 3 521 000 |
| M4 | + CTO, + Solutions analyst | 4 493 000 |
| M5 | + 2-й Backend | 5 135 000 |
| M6 | + ML Engineer, + 2-й SDR | 5 902 500 |
| M7 | Полная команда | 5 902 500 |
| M8 | Полная команда | 5 902 500 |
| M9 | Полная команда | 5 902 500 |
| M10 | Полная команда | 5 902 500 |
| M11 | Полная команда | 5 902 500 |
| M12 | Полная команда | 5 902 500 |

### Sanity check по hiring realism
- В M1 не нанимается 5+ полноценных senior ролей, поэтому time-to-hire не нарушен.
- FOT для команды 5-7 человек уже к M4 приближается к **4,5 млн ₽/мес**, что выглядит реалистично.
- Для B2B enterprise AI стартовый капитал **ниже 10 млн ₽** был бы нерелевантен; здесь потребность многократно выше. [T3]

## 11. Fixed costs breakdown

| Компонент | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5 902 500 |
| Office / coworking / admin | 180 000 |
| Core infra not in COGS | 260 000 |
| Security / legal / audit retainers | 210 000 |
| G&A / бухгалтерия / ЭДО / bank fees | 110 000 |
| Founders travel / enterprise meetings | 180 000 |
| Misc. software / corp stack | 150 000 |
| Founder marketing / PR not in CAC | 200 000 |
| **Итого fixed costs / мес** | **7 192 500 ₽** |

## 12. Break-even by client count and by month

### Break-even по клиентам
- Contribution profit на клиента: **81 000 ₽/мес**
- Fixed costs: **7 192 500 ₽/мес**

`Break-even clients = 7 192 500 / 81 000 = 88,8`, округляю до **89 клиентов**

Чтобы пройти дополнительный фильтр `EBITDA > 500k ₽/мес`, нужен уровень:

`(7 192 500 + 500 000) / 81 000 = 94,97`, то есть **95 клиентов**

### Stress test при 50 клиентах
- Revenue: **10,0 млн ₽/мес**
- Contribution profit: **4,05 млн ₽/мес**
- EBITDA: **-3,14 млн ₽/мес**

**Итог:** даже при **50 клиентах** компания не достигает целевого EBITDA. Profit Gate = **FAIL**. [T1]

### Break-even по месяцам
Базовый ramp клиентов: 0, 0, 1, 2, 3, 4, 6, 8, 10, 12, 14, 16 активных клиентов по месяцам M1-M12.

| Месяц | Активные клиенты | EBITDA, ₽/мес | Кумулятивный burn, ₽ |
|---|---:|---:|---:|
| M1 | 0 | -3 130 000 | 3 130 000 |
| M2 | 0 | -3 738 000 | 6 868 000 |
| M3 | 1 | -4 560 000 | 11 428 000 |
| M4 | 2 | -5 611 000 | 17 039 000 |
| M5 | 3 | -6 302 000 | 23 341 000 |
| M6 | 4 | -7 168 500 | 30 509 500 |
| M7 | 6 | -7 006 500 | 37 516 000 |
| M8 | 8 | -6 844 500 | 44 360 500 |
| M9 | 10 | -6 682 500 | 51 043 000 |
| M10 | 12 | -6 520 500 | 57 563 500 |
| M11 | 14 | -6 358 500 | 63 922 000 |
| M12 | 16 | -6 196 500 | 70 118 500 |

**Вывод:** в рамках M1-M12 break-even не достигается даже близко. [T1]

## 13. Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Кумулятивный burn за первые 12 месяцев: **~70,1 млн ₽**
- При этом к M12 модель всё ещё глубоко убыточна
- Так как EBITDA break-even требует **95 клиентов**, а это выше реалистичного buyer universe для РФ, **burn-to-breakeven в локальном контуре считаю практически неограниченным / неинвестируемым**. [T1]

### Cash runway
При `startup_capital = 75 млн ₽`:
- burn в M12: **~6,2 млн ₽/мес**
- runway: примерно **12 месяцев**
- к концу года компания почти полностью сжигает капитал и всё ещё далека от operating break-even

### Интерпретация
Даже крупный для раннего РФ-стартапа стартовый капитал не приводит модель к устойчивой точке окупаемости. Для фонда это structural no-go. [T1]

## 14. Финальный вывод P5

**Решение: REJECTED.**

Кейс проходит по ценности и способен показать неплохой LTV/CAC на бумаге, но **не проходит ключевой фондовый фильтр по прибыли**. В российском контуре buyer universe слишком мал, sales motion слишком дорогой, а delivery слишком тяжёлый. Даже на 50 клиентах EBITDA остаётся отрицательной, поэтому продолжать кейс как investable geo-expand нецелесообразно. [T1]

## Источники
- `02-demand.md` по кейсу rogo-finance-workflow-geo-expand-v2: market size, ICP, price anchors, profit-gate assumptions. [T1]
- SaaS Capital, churn benchmarks for B2B SaaS: https://www.saas-capital.com/blog-posts/saas-metrics-2-customer-churn-benchmarks/ [T2]
- HH.ru search / salary benchmark references for Moscow/SPb tech and sales roles: https://hh.ru/search/vacancy [T3]
- Банк России, рынок УК за 9 месяцев 2024: https://www.cbr.ru/press/event/?id=23323 [T4]
