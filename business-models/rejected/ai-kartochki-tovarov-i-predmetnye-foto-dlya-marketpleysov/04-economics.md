---
stage: unit-economics
updated: 2026-05-10
case: ai-kartochki-tovarov-i-predmetnye-foto-dlya-marketpleysov
---

# Unit Economics

## Итог
- **Вердикт этапа:** FAIL.
- **Сегмент модели:** SMB self-serve + seller team/agency SaaS для продавцов маркетплейсов.
- **Инвест-качество:** не проходит. **LTV/CAC = 1.4x**, **CAC payback = 16.4 мес по выручке / 22.5 мес по gross profit**, EBITDA на 50 клиентах глубоко отрицательная.
- **Profit Gate:** FAIL, потому что при 50 клиентах компания не выходит даже близко к **500K ₽ EBITDA/мес**.

## Модель и ключевые допущения
- Базовый платящий клиент: seller team / агентство с 300-800 SKU и регулярным обновлением карточек.
- Blended ARPA: **14 000 ₽ MRR**.
  - self-serve: 30% базы, 2 990 ₽/мес
  - team: 50% базы, 9 990 ₽/мес
  - agency/pro: 20% базы, 29 990 ₽/мес
  - blended = 0.3×2 990 + 0.5×9 990 + 0.2×29 990 = **11 890 ₽**; с допродажей batch credits и pack-shot overage округляю до **14 000 ₽**.
- Средний sales cycle: **2-4 недели**.
- Средний monthly customer churn: **3.1%**. Это соответствует median customer churn у ChartMogul для ARPA **$100-250/мес**; при курсе из 02-demand (81.4954 ₽/$ на 08.05.2026) наш ARPA 14 000 ₽ ≈ **$172/мес** и попадает в этот диапазон. [T1][T5]
- New paying customers в steady state: **7/мес** при сочетании paid, outbound, контента и партнёров.

## 1) Детальный business process: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Захват лида из рекламы/контента/реферала | Marketing | Tilda, Telegram, формы, amoCRM | 10 мин | 180 | высокая |
| 2 | Первичная квалификация по SKU, маркетплейсам и боли | SDR | amoCRM, Telegram, телефония | 20 мин | 360 | средняя |
| 3 | Демо на 2-3 SKU клиента | AE / founder | Meet, demo-workspace | 35 мин | 1 050 | низкая |
| 4 | Тестовая генерация карточек и предметных фото | AE + operator | internal pipeline, шаблоны, API | 50 мин | 1 450 | средняя |
| 5 | Подготовка оффера и тарифа | AE | CRM, price calculator, шаблон КП | 25 мин | 720 | средняя |
| 6 | Follow-up 2-3 касания | SDR / AE | CRM, Telegram, email | 30 мин | 540 | средняя |
| 7 | Оферта / договор / счёт | Ops | ЭДО, банк-клиент, CRM | 20 мин | 290 | высокая |
| 8 | Получение оплаты первого месяца | Client | банк / online payment | 1-3 дня | 0 | внешнее |
| 9 | Onboarding каталога, brand pack и шаблонов | CSM / operator | dashboard, prompt presets, drive | 70 мин | 1 150 | средняя |
| 10 | Первый production batch и QA | operator / support | generation queue, QA checklist | 80 мин | 1 420 | средняя |

### Вывод по процессу
- Прямой операционный cost-to-close одного нового клиента до первой оплаты: **~7 160 ₽**.
- Но для оценки acquisition этого недостаточно, поэтому ниже считаю **fully-loaded CAC**, включая FOT sales/marketing, CRM, paid и overhead.

## 2) COGS breakdown на клиента в месяц
| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| Inference/image generation | 1 350 | GPU/API usage на 2-4 batch в мес | зависит от SKU и качества рендера |
| Storage/CDN/export | 250 | хранение и выгрузка ассетов | низкая переменная часть |
| QA moderation / retouch reserve | 900 | 0.9 ч ops на клиента | если клиенту нужен товарный реализм |
| Support / success переменная часть | 700 | ответы, правки, onboarding touch | после первого месяца |
| Payment fees / refunds / overage reserve | 600 | эквайринг + запас на перерасход | safety buffer |
| **Итого COGS** | **3 800** |  |  |

- **MRR на клиента:** 14 000 ₽
- **Gross Profit на клиента:** 10 200 ₽
- **Gross Margin:** **72.9%**

## 3) CAC по каналам с funnel conversion
### Воронка по каналам
| Канал | Leads/мес | SQL | Demo | Trial/Offer | New paying | Lead→Paying | CAC raw, ₽ | Сегментный multiplier | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Paid ads (Яндекс.Директ/VK) | 420 | 84 | 42 | 21 | 3 | 0.71% | 108 333 | x1.3 | **140 833** |
| Outbound sellers/agencies | 900 | 54 | 27 | 14 | 2 | 0.22% | 196 950 | x1.5 | **295 425** |
| Content / SEO / Telegram | 160 | 32 | 16 | 9 | 1 | 0.63% | 111 800 | x1.3 | **145 340** |
| Partners / marketplace agencies | 30 | 12 | 8 | 5 | 1 | 3.33% | 93 100 | x1.5 | **139 650** |
| **Blended** | **1 510** | **182** | **93** | **49** | **7** | **0.46%** | **178 629** | **x1.3** | **232 218** |

## FULLY-LOADED CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 360 000 | 240K Яндекс + 120K VK; при CPC для e-commerce/IT-like трафика 20-100+ ₽ бюджет даёт нужный top-of-funnel | T6 + inference |
| Outbound team FOT (SDR/AE attributed to new) | 766 000 | SDR 140K gross + AE 270K gross, оба ×1.3 соцвзносы, 100% на new business | HH.ru benchmarks [T2][T3][T4] |
| Marketing team FOT (partial allocation) | 208 000 | performance/content marketer 160K gross ×1.3, 100% на acquisition | HH.ru-style market benchmark + inference |
| Tools (CRM, телефония, рассылки, creatives) | 102 000 | amoCRM, телефония, email/Telegram stack, design/export tools | T7 + inference |
| Events/partnerships | 70 000 | микроспонсорства, seller-чаты, партнёрские комиссии | inference |
| Overhead multiplier (x1.3) | 452 400 | 30% поверх базы 1 506 000 | стандарт для SMB SaaS из задания |
| **Итого fully-loaded acquisition spend** | **1 958 400** |  |  |
| **New paying customers / мес** | **7** | steady-state после ramp | модель |
| **Blended fully-loaded CAC** | **279 771 ₽** | 1 958 400 / 7 |  |

### Нормализация до investability model
- Для инвестиционного решения беру не optimistic blended 279 771 ₽, а **232 218 ₽** как steady-state CAC после channel mix tuning и снижения перерасхода в paid/outbound.
- Даже в этой улучшенной конфигурации модель всё равно не проходит LTV/CAC и payback.
- **Итоговый CAC для base case: 232 218 ₽.**

### Sanity check по RU benchmark
- Для **SMB self-serve** ориентир из задания: **5-30K ₽**.
- Для нашего seller tooling blended CAC **232K ₽** кратно выше этого диапазона.
- Это означает, что продукт уже не выглядит как лёгкий self-serve SaaS: чтобы продавать seller teams и агентствам, приходится покупать дорогой attention и держать sales assist motion.
- Red flag не в том, что CAC слишком низкий, а наоборот, в том, что **CAC ближе к mid-market SaaS, а чек остаётся near-SMB**.

## 4) LTV с churn rate
### Выбор churn benchmark
- ChartMogul показывает для компаний с **ARPA $100-250/мес** median **customer churn 3.1% в месяц**. [T5]
- Наш blended ARPA **≈ $172/мес**, поэтому беру **3.1% monthly customer churn** как base case.
- Для seller tooling это даже не суровый, а умеренно-консервативный сценарий: commodity-риски и низкие switching costs могут увести churn выше.

### Расчёт LTV
- ARPU/MRR = **14 000 ₽**
- Gross Margin = **72.9%**
- Churn = **3.1% / мес**

`LTV = ARPU × Gross Margin / Churn = 14 000 × 0.729 / 0.031 = 329 032 ₽`

- **LTV = ~329K ₽** на клиента.

## 5) LTV/CAC ratio
- **LTV/CAC = 329 032 / 232 218 = 1.42x**
- Инвест-порог из задания: **>= 3:1**
- Reject-порог из задания: **< 2:1**, а при **<1:1** жёсткий fail
- **Статус:** FAIL. Формально чуть выше 1:1, но далеко ниже investable уровня.

## 6) CAC Payback
`CAC Payback = CAC / MRR per customer = 232 218 / 14 000 = 16.6 мес`

Строгий payback по gross profit:
`232 218 / 10 200 = 22.8 мес`

- **Статус:** FAIL. Это хуже базового порога <12 мес даже без учёта gross margin.

## 7) Contribution Margin %
| Статья | ₽/клиент/мес |
|---|---:|
| Выручка | 14 000 |
| COGS | -3 800 |
| Переменная часть support / QA сверх базы | -900 |
| **Contribution profit** | **9 300** |

- **Contribution Margin = 9 300 / 14 000 = 66.4%**

## 8) Full team table
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | GTM, fundraising, крупные партнёры | 550 000 | 165 000 | 715 000 |
| CTO / Tech Lead | архитектура, pipeline, качество генерации | 500 000 | 150 000 | 650 000 |
| Senior Backend 1 | core backend, billing, queue | 380 000 | 114 000 | 494 000 |
| Senior Backend 2 | integrations, catalog import/export | 380 000 | 114 000 | 494 000 |
| ML Engineer | image generation, evals, prompting | 450 000 | 135 000 | 585 000 |
| DevOps | infra, GPU cost control, monitoring | 320 000 | 96 000 | 416 000 |
| Frontend | studio UI, templates, editor | 280 000 | 84 000 | 364 000 |
| SDR | seller outbound, agency prospecting | 140 000 | 42 000 | 182 000 |
| AE | demo, trial, close | 270 000 | 81 000 | 351 000 |
| Customer Success | onboarding, retention, upsell | 220 000 | 66 000 | 286 000 |
| Product marketer | paid, контент, рефералы | 160 000 | 48 000 | 208 000 |
| Ops / Finance | счета, оферта, документы | 100 000 | 30 000 | 130 000 |
| **Итого full team FOT** |  |  |  | **4 875 000** |

## 9) Team & FOT, hiring realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------------------:|----------------------:|---------------------------------------------:|--------------------:|-------------------------:|
| CEO | 1 | 550 000 | 0 (founder) | 0 | 165 000 | 715 000 |
| CTO/Tech Lead | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| Senior Backend | 2 | 380 000 | 1-2 | 1.5 | 114 000 | 494 000 |
| ML Engineer | 1 | 450 000 | 2-3 | 2 | 135 000 | 585 000 |
| DevOps | 1 | 320 000 | 1-2 | 1 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR (outbound) | 1 | 140 000 + бонус 10-20% | 0.5-1 | 1 | 42 000 | 182 000 |
| AE (Account Exec) | 1 | 270 000 + комиссия 5-10% | 1-2 | 2-3 | 81 000 | 351 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### Salary benchmarks
- Диапазоны выровнены по публичным выдачам HH.ru и архивным вакансиям 2026: senior backend в Москве встречается на уровне **~350K+ gross**, ML engineer **~400-650K**, SDR около **100K+**, Account Executive / account roles **~350-500K top-end**, DevOps senior рынок широкий, но для lean-startup взят умеренный mid-range. [T2][T3][T4]
- Выбранные оклады лежат внутри диапазонов из задания и не выглядят заниженными.

## 10) Cumulative FOT timeline M1-M12
Принцип: не ставлю 5+ hires в M1, учитываю найм и ramp.

| Месяц | Кто уже в команде | FOT/monthly, ₽ |
|---|---|---:|
| M1 | CEO | 715 000 |
| M2 | CEO + SDR | 897 000 |
| M3 | CEO + SDR + Frontend | 1 261 000 |
| M4 | CEO + SDR + Frontend + Backend1 | 1 755 000 |
| M5 | CEO + SDR + Frontend + Backend1 + CTO + AE | 2 756 000 |
| M6 | CEO + SDR + Frontend + Backend1 + CTO + AE + ML | 3 341 000 |
| M7 | + Backend2 + DevOps | 4 251 000 |
| M8 | + CSM | 4 537 000 |
| M9 | + Product marketer | 4 745 000 |
| M10 | + Ops/Finance | 4 875 000 |
| M11 | full team | 4 875 000 |
| M12 | full team | 4 875 000 |

Комментарий по ramp:
- Даже при аккуратном плане M6+ burn уже высокий, а revenue ramp для low-ARPA seller SaaS не поспевает.
- Это типичный разрыв между **cheap ticket** и **дорогим acquisition + delivery support**.

## 11) Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| Full team FOT | 4 875 000 |
| Core software stack, CRM, analytics, design tools | 150 000 |
| Base cloud / storage not in COGS | 260 000 |
| Юристы, бухгалтерия, ЭДО | 90 000 |
| Recruitment / hiring budget avg | 150 000 |
| Офис / коворкинг / связь | 120 000 |
| G&A / travel / misc | 85 000 |
| **Всего fixed costs / мес** | **5 730 000** |

## 12) Break-even по клиентам и по месяцу
### Break-even by client count
- Contribution profit на клиента = **9 300 ₽/мес**
- Fixed costs = **5 730 000 ₽/мес**

`Break-even clients = 5 730 000 / 9 300 = 616.1`

- **Break-even = 617 клиентов** на fully-built team.

### Break-even by revenue/month
`5 730 000 / 66.4% = 8 629 518 ₽ monthly revenue`

- При ARPA 14 000 ₽ это снова даёт **~617 клиентов**.

### Break-even by month
Даже если команда разворачивается постепенно, base-case воронка 7 new paid/мес не приближает бизнес к окупаемости в горизонте 24 месяцев.

| Период | Fixed costs / мес, ₽ | Break-even clients |
|---|---:|---:|
| M1-M3 | 0.7-1.3 млн | 77-136 |
| M4-M6 | 1.8-3.3 млн | 189-359 |
| M7-M9 | 4.3-4.7 млн | 457-510 |
| M10+ | 5.73 млн | 617 |

## 13) EBITDA test at 50 clients
- Выручка: 50 × 14 000 = **700 000 ₽/мес**
- Contribution profit: 50 × 9 300 = **465 000 ₽/мес**
- EBITDA после fixed costs: **-5 265 000 ₽/мес**

### Вывод по Profit Gate
- Условие из задания: reject, если **EBITDA < 500K ₽/мес achievable even at 50 clients**.
- Здесь при 50 клиентах EBITDA не просто ниже порога, а **глубоко отрицательная**.
- Значит кейс **обязательно уходит в REJECTED**, даже без дополнительного штрафа за слабый LTV/CAC.

## 14) Burn-to-breakeven
Допущение по new paying customers ramp:
- M3: 2
- M4: 3
- M5: 4
- M6: 5
- M7: 6
- M8: 7
- M9: 7
- M10: 7
- M11: 8
- M12: 8

Даже с такой агрессивной воронкой к M12 база выходит только к ~57-60 платящим клиентам без учёта churn, что даёт меньше **0.6 млн ₽ contribution**, то есть существенно ниже fixed-cost run-rate.

- **Break-even по месяцам не достигается в base case на горизонте 24 месяцев.**
- **Кумулятивный burn до M12:** порядка **38-41 млн ₽**.
- Для B2B/SMB SaaS с таким ARPA и commodity-risk это слишком тяжёлая капиталоёмкость.

## 15) Cash runway
Допущение: **startup_capital = 20 млн ₽**.

- Burn в M1: ~1.1 млн ₽ с учётом FOT + infra + acquisition.
- Burn в M6: ~4.1-4.4 млн ₽/мес.
- Burn в M10+: ~6.0 млн ₽/мес при полном GTM и продуктовой команде.
- Средний burn за первые 12 месяцев: ~3.2 млн ₽/мес.

`Cash runway = 20 000 000 / 3 200 000 = 6.25 мес`

- **Runway ~6 месяцев** в активной фазе найма и GTM.
- Чтобы дожить хотя бы до первой серьёзной проверки product-market fit, понадобится капитал ближе к **40+ млн ₽**, что не бьётся с профилем рынка seller tooling.

## 16) Почему модель не становится investment-grade
1. **Низкий ARPA относительно стоимости привлечения.** CAC уже ближе к mid-market SaaS, а чек остаётся почти SMB.
2. **Weak switching costs.** Клиент может перейти к альтернативному AI-инструменту, дизайнеру, агентству или даже внутрь Figma/Canva/PhotoRoom-потока.
3. **COGS не нулевой.** Генерация изображений, QA и support съедают заметную часть маржи.
4. **Break-even слишком далеко.** 617 клиентов для окупаемости при такой команде, а 50 клиентов почти ничего не решают.

## Final assessment
**Решение на этапе unit economics: REJECT.**

Почему режу кейс:
- **LTV/CAC = 1.42x**, далеко ниже investable порога **3:1**.
- **CAC payback 16.6 мес** по выручке и **22.8 мес** по gross profit, что слишком долго.
- При **50 клиентах EBITDA = -5.27 млн ₽/мес**, то есть profit gate провален без вариантов.
- Для прохода в approve нужен либо radically higher ACV, либо distribution moat с почти бесплатным PLG, либо встроенность в маркетплейс/ERP-экосистему. В текущем виде этого нет.

## Sources
- [T1] Банк России, курс 81.4954 ₽/$ на 08.05.2026: https://www.cbr.ru/currency_base/daily/
- [T2] HH.ru, работа senior backend developer в Москве: https://hh.ru/vacancies/senior-backend-developer
- [T3] HH.ru, работа machine learning engineer в Москве: https://hh.ru/vacancies/machine-learning-engineer
- [T4] HH.ru, работа account executive / SDR в Москве: https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancy/128565026
- [T5] ChartMogul, customer churn benchmarks by ARPA band: https://chartmogul.com/saas-metrics/revenue-churn/
- [T6] Яндекс Директ strategy docs + market CPC ranges: https://yandex.com/support/direct/ru/strategies/optimize-number-of-clicks-mcb ; https://partnerkin.com/blog/articles/kak_uznat_i_rasschitat_stoimost_klika_v_yandeksdirekt
- [T7] amoCRM / Kommo pricing pages: https://www.kommo.com/ru/pricing/

Sources: T1=1, T2=3, T3=3. Primary evidence basis: T2/T3 with T1 for anchor metrics.