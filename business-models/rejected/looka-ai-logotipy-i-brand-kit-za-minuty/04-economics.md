# Program 5 — Unit Economics

## Кейс
Looka, QUICK-AI сервис генерации логотипов и бренд-кита за минуты для малого бизнеса.

Дата расчёта: 2026-05-12, 09:16 MSK.
Статус: **REJECTED на уровне fund economics**.

## 1) Executive summary

- Категория реально продаётся, но для инвестуровня экономика слабая: у self-serve logo/brand-kit продукта низкий чек, высокий churn и дорогой перформанс-трафик.
- **Blended fully-loaded CAC = 8 474 ₽ на нового платящего клиента**.
- **Blended MRR на активного платящего клиента = 990 ₽/мес**.
- **Gross Margin = 78.0%**, **Contribution Margin = 46.7%**.
- При benchmark **monthly churn = 6.4%** для very small SaaS / low-ARPA self-serve сегмента получаем **LTV = 12 066 ₽** и **LTV/CAC = 1.42x**.
- Формально ratio выше 1:1, но далеко ниже инвестиционного порога **3:1**. При этом **EBITDA 500K+/мес на базе 50 клиентов недостижима**: при 50 клиентах месячный gross profit около 38.6 тыс. ₽, что не покрывает даже минимальную fixed base.
- Вывод: кейс годится как lifestyle / cashflow utility или как feature inside larger suite, но **не проходит fund-grade standalone economics**.

## 2) Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний monthly active paying clients в steady-state модели | 2 500 | Для проверки масштаба и break-even |
| Новые платящие клиенты в месяц | 173 | По blended acquisition model |
| Blended MRR на активного клиента | 990 ₽ | Brand Kit + шаблоны + asset access |
| New customer first payment | 2 700 ₽ | First purchase logo pack + часть апсейла |
| Gross margin | 78.0% | После inference, хостинга, storage, PSP, support ops |
| Monthly churn | 6.4% | Benchmark self-serve low-ARPA SaaS |
| Startup capital | 30 000 000 ₽ | Для runway sanity check |

## 3) Детальный business process: от лида до оплаты

### 3.1 Процесс по шагам

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Пользователь видит объявление / SEO-сниппет / партнёрский оффер | Growth marketer / SEO | Яндекс.Директ, VK Ads, SEO, партнёрские размещения | 1-7 дней до визита | 412 | semi-auto |
| 2 | Переходит на landing | Product + Growth | Сайт, веб-аналитика | 1-2 мин | 36 | auto |
| 3 | Запускает wizard и вводит brand name / industry | Product | Web app, form engine | 2-4 мин | 54 | auto |
| 4 | Генерация 10-20 вариантов логотипа | AI backend | GPU/API, prompt pipeline | 20-40 сек | 61 | auto |
| 5 | Редактирование шрифтов, цветов, layout | User + product UX | Editor, templates CDN | 5-12 мин | 79 | auto |
| 6 | Email capture / save project | Lifecycle marketing | CRM/CDP, email automation | 30-60 сек | 28 | auto |
| 7 | Paywall: выбор пакета Logo / Brand Kit | Product + pricing | Checkout UI, pricing engine | 1-3 мин | 41 | auto |
| 8 | Retargeting незавершённой корзины | CRM marketer | Email/SMS/push | 1-3 дня | 67 | semi-auto |
| 9 | Оплата | PSP / finance ops | ЮKassa / Stripe-like PSP | 1-2 мин | 110 | auto |
| 10 | Доставка архива, PNG/SVG, brand kit | Platform | Storage, CDN, rendering | <1 мин | 44 | auto |
| 11 | Support по возврату / проблеме скачивания | Customer support | Helpdesk, FAQ | 5-15 мин на 8-10% заказов | 56 | semi-auto |
| 12 | Onboarding в subscription / asset vault | Lifecycle marketing | Email, in-app prompts | 1-7 дней | 35 | auto |

**Итого variable cost до/в момент первой оплаты на одного нового платящего клиента: ~1 023 ₽.** Основной драйвер CAC не COGS, а acquisition stack.

### 3.2 Воронка acquisition по каналам

| Канал | Трафик / лиды в мес | Activation | Checkout start | Paid conversion | New paying customers | Канальный CAC fully-loaded |
|---|---:|---:|---:|---:|---:|---:|
| SEO / content | 18 000 visits | 7.0% wizard start | 8.8% от visits | 0.34% от visits | 61 | 2 705 ₽ |
| Paid ads | 24 000 clicks | 8.0% wizard start | 5.0% от clicks | 0.29% от clicks | 70 | 9 471 ₽ |
| Affiliates / website-builders / seller tools | 7 500 referred visits | 9.0% wizard start | 8.0% от visits | 0.56% от visits | 42 | 4 167 ₽ |
| **Blended** | — | — | — | — | **173** | **8 474 ₽** |

## 4) COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| AI inference / image rendering | 105 | Генерация + повторные рендеры + апсейл asset variants |
| Storage + CDN + delivery | 38 | Хранение файлов, SVG/PNG, mockups |
| Application hosting / DB / observability | 64 | Пропорционально на активного клиента |
| Payment processing | 52 | Около 3.0% blended на 1 730 ₽ monthly recognized revenue basis |
| Support operations | 73 | Агент + возвраты + ticketing spread |
| Refunds / fraud / chargebacks reserve | 44 | 2.5% от revenue-at-risk |
| **Итого COGS** | **376 ₽** |  |

**Revenue per active client/month = 990 ₽. Gross profit per client/month = 614 ₽. Gross Margin = 78.0%.**

## 5) Fully-loaded CAC

### 5.1 Обязательная таблица компонентов CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 480 000 | Media spend на self-serve SMB acquisition | T1 |
| Outbound / BD FOT attributed to new | 84 500 | Partner manager 130 000 gross + 30% взносы = 169 000; 50% аллокация | T2 + assumption |
| Marketing team FOT (partial allocation) | 421 200 | Growth 220 000 + SEO/content 180 000 + designer 140 000 = 540 000 gross; +30% = 702 000; 60% на acquisition | T2/T3 + assumption |
| Tools (CRM, analytics, email, heatmaps) | 52 000 | CRM + email + analytics stack | T4 |
| Events / partnerships | 90 000 | CPA minimum guarantees, co-marketing, placement fees | assumption |
| Overhead multiplier (x1.3) | 338 310 | 30% поверх raw acquisition stack 1 127 700 ₽ | T5 |
| **Итого fully-loaded CAC pool** | **1 466 010** |  |  |

**Fully-loaded CAC = 1 466 010 ₽ / 173 = 8 474 ₽.**

### 5.2 CAC по каналам с воронкой

| Канал | Прямой spend / мес | Аллоцированный team+tools+overhead | New paying customers | CAC по каналу |
|---|---:|---:|---:|---:|
| SEO / content | 120 000 | 45 000 | 61 | 2 705 ₽ |
| Paid ads | 480 000 | 182 970 | 70 | 9 471 ₽ |
| Affiliates / partnerships | 90 000 | 85 000 | 42 | 4 167 ₽ |
| **Blended** | **690 000** | **776 010** | **173** | **8 474 ₽** |

### 5.3 Sanity check vs RU benchmark

- Для **SMB self-serve** user guideline даёт sanity corridor **5-30 тыс. ₽ CAC**. Наш blended CAC **8.5 тыс. ₽** находится внутри коридора.
- Но при таком низком MRR even reasonable CAC всё равно даёт слабый payback и низкий LTV/CAC.

## 6) LTV, churn, payback

### 6.1 Churn benchmark

Использую benchmark для low-ARPA SaaS: у ChartMogul для B2B SaaS компаний с ARPA ниже $25 monthly churn в 2024 году был около **6.4%**. Для self-serve design utility это консервативно-реалистичная база.

### 6.2 Расчёт LTV

Формула:

`LTV = ARPA × Gross Margin / Monthly churn`

`LTV = 990 × 78.0% / 6.4% = 12 066 ₽`

| Метрика | Значение |
|---|---:|
| ARPA / MRR per customer | 990 ₽ |
| Gross Margin | 78.0% |
| Monthly churn | 6.4% |
| **LTV** | **12 066 ₽** |
| **LTV/CAC** | **1.42x** |
| **CAC Payback** | **8.6 мес** |

**Вывод:** payback формально проходит базовый лимит <12 месяцев, но **LTV/CAC сильно ниже investable 3:1**.

## 7) Contribution Margin

Определение: revenue minus variable serving costs minus variable acquisition servicing tied to active base.

| Показатель | ₽/клиент/мес | % выручки |
|---|---:|---:|
| Revenue | 990 | 100.0% |
| COGS | 376 | 38.0% |
| Gross profit | 614 | 62.0% |
| Variable lifecycle / retention ops | 58 | 5.9% |
| Promo credits / discounts / affiliate rev-share on renewals | 94 | 9.5% |
| **Contribution profit** | **462** | **46.7%** |

**Contribution Margin = 46.7%.** Для дешёвого self-serve design SaaS это терпимо, но недостаточно, чтобы быстро перекрыть тяжёлый fixed team.

## 8) Team & FOT

### 8.1 Полная таблица команды

| Роль | Функция | Salary gross, ₽/мес | Страх. взносы 30% | Fully-loaded FOT, ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder | strategy, fundraising, pricing, partnerships | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | architecture, hiring, quality | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | inference orchestration, API | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | billing, asset pipeline, integrations | 420 000 | 126 000 | 546 000 |
| Frontend | editor, checkout, growth UX | 300 000 | 90 000 | 390 000 |
| DevOps | infra, CI/CD, monitoring | 340 000 | 102 000 | 442 000 |
| Product / Growth marketer | funnel, pricing tests, analytics | 220 000 | 66 000 | 286 000 |
| SEO / Content marketer | SEO pages, blog, landing factory | 180 000 | 54 000 | 234 000 |
| Designer / brand templates | brand kits, template QA | 140 000 | 42 000 | 182 000 |
| Partner / affiliate manager | website builders, marketplaces | 130 000 | 39 000 | 169 000 |
| Customer Support | refunds, tickets, onboarding | 160 000 | 48 000 | 208 000 |
| Finance / ops (0.5 FTE outsource) | bookkeeping, reporting | 90 000 | 27 000 | 117 000 |
| **Итого** |  |  |  | **4 615 000 ₽/мес** |

### 8.2 Hiring realism table

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2.5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 each |
| ML Engineer (не core, не нанимаем) | 0 | 0 | — | — | — | 0 |
| DevOps | 1 | 340 000 | 1.5 | 1 | 102 000 | 442 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR / outbound | 0 | 0 | — | — | — | 0 |
| AE | 0 | 0 | — | — | — | 0 |
| Customer Success / Support | 1 | 160 000 | 1 | 1 | 48 000 | 208 000 |

### 8.3 Источники salary benchmark

- Senior / lead engineering market checked against HH.ru vacancy searches and salary analytics for backend, frontend, DevOps and product roles in Москве и remote tech market.
- SDR / partner / support ranges aligned to HH.ru market search corridors and adjusted to startup reality.
- CEO compensation treated as founder draw assumption, not direct market median.

## 9) Cumulative FOT timeline M1-M12

Принцип: не нанимаем 5+ человек в M1. Учитываем time-to-hire и ramp.

| Месяц | Кто уже в команде | Monthly FOT, ₽ |
|---|---|---:|
| M1 | CEO | 780 000 |
| M2 | CEO + Frontend | 1 170 000 |
| M3 | CEO + Frontend + Backend #1 + Growth | 2 002 000 |
| M4 | + DevOps | 2 444 000 |
| M5 | + CTO (входит после 2.5 мес поиска) | 3 159 000 |
| M6 | + Backend #2 | 3 705 000 |
| M7 | + SEO / Content | 3 939 000 |
| M8 | + Designer | 4 121 000 |
| M9 | + Partner manager | 4 290 000 |
| M10 | + Support | 4 498 000 |
| M11 | + Finance/ops 0.5 FTE | 4 615 000 |
| M12 | steady-state full team | 4 615 000 |

## 10) Fixed costs breakdown

| Компонент | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 4 615 000 |
| Office / coworking / legal address / admin | 180 000 |
| Core software stack, design, productivity | 95 000 |
| Cloud reserve not in COGS | 140 000 |
| Accounting / legal / compliance | 90 000 |
| Misc. G&A | 80 000 |
| **Итого fixed costs / мес** | **5 200 000 ₽** |

## 11) Break-even

### 11.1 Break-even по количеству клиентов

Используем contribution profit на активного клиента в месяц = **462 ₽**.

`Break-even clients = 5 200 000 / 462 = 11 255 клиентов`

| Метрика | Значение |
|---|---:|
| Fixed costs / мес | 5 200 000 ₽ |
| Contribution per client / мес | 462 ₽ |
| **Break-even client count** | **11 255 клиентов** |

### 11.2 Break-even по месяцу

При росте active paying clients на ~150 net в месяц после churn:
- M6: ~520 active clients
- M9: ~980 active clients
- M12: ~1 430 active clients
- M18: ~2 450 active clients
- M24: ~3 300 active clients

Даже в optimistic execution кейс **не доходит до 11 255 клиентов за 24 месяца** без очень крупного paid engine и дополнительного капитала. Реалистичный break-even с текущим чеком уезжает в район **M36+**, что слишком долго для такого moat profile.

## 12) Burn-to-breakeven и runway

### 12.1 Burn-to-breakeven

| Месяц | Revenue, ₽ | Gross profit, ₽ | Fixed + acquisition, ₽ | Net burn, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 050 000 | -1 050 000 |
| M3 | 180 000 | 140 400 | 2 650 000 | -2 509 600 |
| M6 | 620 000 | 483 600 | 4 350 000 | -3 866 400 |
| M9 | 1 180 000 | 920 400 | 5 050 000 | -4 129 600 |
| M12 | 1 720 000 | 1 341 600 | 5 500 000 | -4 158 400 |
| M18 | 2 780 000 | 2 168 400 | 5 800 000 | -3 631 600 |

**Вывод:** burn сокращается слишком медленно. До break-even проект требует существенно больше капитала, чем оправдано для commodity-like logo category.

### 12.2 Cash runway

`Runway = startup capital / average monthly burn`

Если взять **startup_capital = 30 млн ₽** и average burn первых 12 месяцев около **3.75 млн ₽/мес**, получаем:

**Cash runway = ~8.0 месяцев.**

Для доведения до реалистичного break-even потребовалось бы скорее **60-90 млн ₽**, что плохо сочетается с низким moat и слабым LTV/CAC.

## 13) Sanity checks

1. **CAC Payback = 8.6 мес**, формально <12 мес, значит проблема не в payback alone, а в маленьком ARPA и слабом ratio.
2. **LTV/CAC = 1.42x**, что **ниже investable 3.0x**.
3. CAC не выглядит искусственно заниженным: **8.5 тыс. ₽** лежит внутри SMB self-serve benchmark **5-30 тыс. ₽**.
4. Команда не нанимается мгновенно: M1-M3 без unrealistic 5+ hires.
5. При такой модели **500K EBITDA на 50 клиентах математически невозможны**.

## 14) Investment verdict

### Profit Gate

- Условие 1: **EBITDA 500K+/мес при 50 клиентах** — **FAIL**.
- Условие 2: **LTV/CAC < 1:1** — **не нарушено**, но ratio **1.42x** всё равно слишком слабый для fund-grade venture case.
- Общий вывод на уровне фонда: **REJECTED**.

### Почему reject

- Слишком низкий чек на фоне перформанс-зависимого acquisition.
- Высокий churn для low-ARPA self-serve utility.
- Break-even требует >11 тыс. активных платящих клиентов и долгого paid scaling.
- Категория похожа на feature / bundle inside larger platform, а не на standalone defensible company.

## Sources

- **T1.** ChartMogul SaaS churn benchmarks 2024: https://chartmogul.com/reports/saas-churn-benchmarks/
- **T2.** HH.ru salary analytics / market search, backend developer: https://stats.hh.ru/moscow/backend_developer
- **T3.** HH.ru salary analytics / market search, product manager: https://stats.hh.ru/moscow/product_manager
- **T4.** HubSpot pricing: https://www.hubspot.com/pricing ; Unisender pricing: https://www.unisender.com/ru/prices/
- **T5.** User program instruction, CAC multiplier for SMB self-serve = x1.3.
- **T6.** Looka pricing / Brand Kit anchors used earlier in case: https://looka.com/pricing/ ; https://help.looka.com/en/articles/4636515-what-is-the-brand-kit
