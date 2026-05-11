---
stage: unit-economics
case: ai-veb-studiya-i-mvp-pod-zakaz-na-bolt-new
date: 2026-05-11
analyst: branch-models-lead
sector: AI-SERVICES
verdict: REJECTED
confidence: medium
---

# 04-economics

## Executive summary
**Итог: REJECTED.**

Для AI-first веб-студии на Bolt.new экономика выглядит приемлемо на уровне одного проекта, но **не investment-grade на уровне фонда**. Ключевая проблема в том, что бизнес продаёт в основном **разовую разработку**, а не sticky recurring продукт. При реалистичном fully-loaded CAC, низком attach rate на support и слабых switching costs модель даёт:

- **COGS / активный клиент / мес:** **24 000 ₽**
- **Contribution Margin:** **52,0%**
- **Fully-loaded blended CAC:** **170 000 ₽**
- **LTV:** **152 000 ₽**
- **LTV/CAC:** **0,89x**
- **CAC Payback:** **19,4 мес**
- **Break-even:** **72 активных клиента** или **3,96 млн ₽ выручки / мес**
- **EBITDA при 50 активных клиентах:** **-550 000 ₽ / мес**

**Profit Gate FAIL:**
1. **LTV/CAC < 1:1**
2. **EBITDA < 500k ₽/мес даже при 50 клиентах**

Следовательно, кейс уходит в **rejected**.

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | SMB и lower mid-market в РФ | Нужны быстрые лендинги, корпоративные сайты, простые MVP и Telegram Mini App |
| Setup fee | 160 000 ₽ | Внутри validated ценового коридора из 02-demand.md |
| Support retainer | 25 000 ₽/мес | Основано на ценовых якорях fast web support в 02-demand.md |
| Retainer attach rate | 35% | Нижняя граница realistic attach для commoditized studio service |
| Active-client blended revenue | 55 000 ₽/мес | Смесь новых build-проектов, доработок и части клиентов на support |
| COGS / активный клиент / мес | 24 000 ₽ | Delivery labor + PM + AI/tools + support |
| Gross margin | 52,0% | Для AI-assisted studio это уже не software-like margin |
| New paying customers / мес | 6 | Реалистично для founder-led sales + 1 SDR + 1 AE |
| Sales cycle | 3-6 недель | Квалификация, бриф, demo, КП, договор, оплата |
| Monthly logo churn на recurring-support | 7,0% | Консервативно хуже зрелых агентств из-за low switching cost |
| Startup capital | 25,0 млн ₽ | Ниже этой суммы runway до breakeven выглядит слишком хрупким |

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Захват входящего лида с сайта, Telegram, партнёрки, рекламы | Маркетинг / SDR | Tilda, Telegram, формы, amoCRM | 10 мин | 180 | высокая |
| 2 | Первичный контакт и qualification | SDR | amoCRM, телефония, Telegram | 25 мин | 520 | частичная |
| 3 | Сбор брифа, определение scope и дедлайна | SDR / AE | Notion, Google Forms, CRM | 30 мин | 780 | частичная |
| 4 | Быстрый pre-sale аудит, подбор шаблона и стеков | Tech lead / PM | Bolt.new, Figma, Notion | 1,5 ч | 3 000 | частичная |
| 5 | Discovery call и упаковка оффера | Founder / AE | Google Meet, презентация, CRM | 1,0 ч | 2 600 | низкая |
| 6 | Черновой estimate, тайминг, коммерческое предложение | AE / PM | шаблон КП, docs, CRM | 45 мин | 1 250 | частичная |
| 7 | Follow-up, работа с возражениями, правки scope | AE / Founder | почта, Telegram, CRM | 1,0 ч | 2 200 | низкая |
| 8 | Договор, счёт, ЭДО | Ops / Founder | Диадок, банк, 1С | 35 мин | 700 | высокая |
| 9 | Получение оплаты и постановка в delivery | Ops / PM | банк-клиент, CRM, Notion | 20 мин | 350 | высокая |
| 10 | Onboarding, сбор доступов, контента, домена | PM / CSM | Telegram, Notion, Figma, хостинг | 1,5 ч | 2 100 | частичная |

**Итого прямой cost-to-close одного клиента:** **13 680 ₽**.

Это не CAC, а операционная цена закрытия сделки без учёта marketing/sales overhead.

## 3. COGS breakdown на клиента в месяц

База: **55 000 ₽ выручки на активного клиента в месяц**.

| Компонент COGS | ₽ / клиент / мес | Как получено |
|---|---:|---|
| Backend / builder delivery allocation | 9 000 | Часы разработки и сборки на Bolt/new stack |
| Frontend / layout / UI polishing | 4 000 | Доработки интерфейса, адаптив, правки |
| PM / account coordination | 3 500 | Статусы, брифинг, контроль сроков |
| QA / publishing / launch support | 2 000 | Проверка, выкладка, домены, формы |
| AI / LLM / builder tooling | 2 500 | Bolt.new, LLM, дизайн- и dev-tools |
| Hosting / infra / integrations variable | 1 500 | Интеграции, формы, домены, сервисы |
| Customer support / minor edits | 1 500 | Мелкие доработки и сообщения клиента |
| Billing / docs / variable ops | 500 | ЭДО, банк, документооборот |
| **Итого COGS** | **24 000** |  |

**Gross profit / активный клиент / мес = 55 000 - 24 000 = 31 000 ₽.**

## 4. CAC по каналам с funnel conversion

### 4.1 CAC по каналам

| Канал | Spend / мес, ₽ | Поток | Конверсия в SQL | Конверсия SQL→proposal | Конверсия proposal→win | New paying customers / мес | CAC / клиент, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Inbound content / SEO | 190 000 | 55 лидов | 30% | 48% | 25% | 2 | 95 000 |
| Paid ads (Яндекс.Директ / VK) | 380 000 | 130 лидов | 14% | 44% | 20% | 2 | 190 000 |
| Outbound | 260 000 | 320 аккаунтов / 28 ответов / 10 встреч | 40% meeting→SQL | 50% | 20% | 1 | 260 000 |
| Partnerships / referrals | 70 000 | 10 интро | 70% | 57% | 25% | 1 | 70 000 |

### 4.2 Blended funnel

| Метрика | Значение |
|---|---:|
| Общий spend / мес | 900 000 ₽ |
| Raw lead / intro volume | 515 |
| SQL | 32 |
| Proposals | 15 |
| Wins | 6 |
| **Blended CAC без overhead multiplier** | **150 000 ₽** |

## 5. FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Таблица расчёта

| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 260 000 | 2 клиента/мес из performance-потока; иначе pipeline пустой | inference + 02-demand.md T2 |
| Outbound team FOT (SDR/AE attributed to new) | 494 000 | SDR 140k gross + AE 240k gross, оба ×1,3 на страхвзносы | HH.ru вакансии sales / user benchmark / inference |
| Marketing team FOT (partial allocation) | 156 000 | 120k gross performance/content marketer ×1,3 | HH.ru marketing benchmark / inference |
| Tools (CRM, телефония, e-mail, design, analytics) | 40 000 | amoCRM, телефония, рассылки, design/dev stack | inference |
| Events/partnerships | 50 000 | партнёрские комиссии, small meetups, вебинары | inference |
| **Raw acquisition spend** | **600 000** | сумма прямых acquisition cost |  |
| Overhead multiplier (x1.7 для mid-market B2B, доп. нагрузка = 420 000 ₽) | 420 000 | длиннее цикл, больше касаний, founder time, presale delivery | task benchmark |
| **Fully-loaded CAC spend / мес** | **1 020 000 ₽** |  |  |
| **New paying customers / мес** | **6** | founder-led studio без перегруза delivery |  |
| **Fully-loaded blended CAC** | **170 000 ₽** | 1 020 000 / 6 |  |

### Sanity checks
- Сегмент здесь не self-serve SMB SaaS, а **sales-assisted studio / mid-market B2B service**, поэтому применяю multiplier **x1.7** к raw CAC, в рамках заданного диапазона **1.5-1.7**.
- Полученный CAC **170k ₽** выше self-serve benchmark **5-30k ₽**, но находится в коридоре **mid-market SaaS/service 60-250k ₽** из task и выглядит реалистично.
- Если бы считать CAC как `только реклама / сделки`, модель дала бы ложно красивую экономику и не учла бы founder-sales, pre-sale и tool stack.

## 6. LTV и churn benchmark

### Benchmark churn source
AgencyAnalytics в **2025 Marketing Agency Benchmarks Report** отмечает, что значимая доля агентств живёт с клиентом **2-5 лет**. Это соответствует зрелым recurring-агентствам с высокой долей retainers.

Источник: https://agencyanalytics.com/company/newsroom/2025-marketing-agency-benchmarks-report

Для данного кейса этот benchmark **слишком оптимистичен**, потому что:
1. продаётся commoditized fast-build service,
2. switching costs низкие,
3. большая часть выручки разовая,
4. support attach rate низкий.

Поэтому в модели беру **7% monthly churn** на recurring-support слой как консервативное операционное допущение, то есть lifetime около **14,3 месяца**.

### Расчёт LTV

#### 6.1 Upfront economics
| Метрика | Формула | Значение |
|---|---|---:|
| Setup fee | — | 160 000 ₽ |
| Setup COGS | — | 78 000 ₽ |
| **Upfront gross profit** | 160 000 - 78 000 | **82 000 ₽** |

#### 6.2 Recurring economics
| Метрика | Формула | Значение |
|---|---|---:|
| Support retainer | — | 25 000 ₽/мес |
| Support COGS | — | 11 000 ₽/мес |
| Support gross profit | 25 000 - 11 000 | 14 000 ₽/мес |
| Attach rate | — | 35% |
| Weighted recurring GP / new customer | 14 000 × 35% | 4 900 ₽/мес |
| Monthly churn | — | 7,0% |
| Lifetime | 1 / 0,07 | 14,3 мес |
| Recurring LTV | 4 900 / 0,07 | 70 000 ₽ |

#### 6.3 Total LTV
| Метрика | Формула | Значение |
|---|---|---:|
| Upfront GP | — | 82 000 ₽ |
| Recurring LTV | — | 70 000 ₽ |
| **LTV total** | 82 000 + 70 000 | **152 000 ₽** |

## 7. LTV/CAC, CAC payback, contribution margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 152 000 / 170 000 | **0,89x** | ниже порога 1,0x и далеко ниже investable 3,0x |
| CAC Payback | 170 000 / 8 750 | **19,4 мес** | хуже даже enterprise sanity check <18 мес |
| Contribution Margin % | 31 000 / 55 000 | **56,4%** | средне для сервиса, недостаточно для фонда при таком churn |
| EBITDA @ 50 clients | 50 × 31 000 - 2 100 000 | **-550 000 ₽ / мес** | Profit Gate FAIL |

Примечание: для payback использую **weighted recurring MRR per customer = 25 000 × 35% = 8 750 ₽**, потому что payback на разовом setup fee не является признаком качественного recurring бизнеса.

## 8. Team & FOT

### 8.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи, стратегия, key accounts | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | delivery architecture, quality, сложные проекты | 550 000 | 165 000 | 715 000 |
| Senior Backend | backend, integrations, forms, auth, dashboards | 400 000 | 120 000 | 520 000 |
| Frontend | UI, responsive, polish, client edits | 300 000 | 90 000 | 390 000 |
| DevOps / infra | deploy, domains, CI, monitoring | 250 000 | 75 000 | 325 000 |
| Product / Project Manager | scope control, roadmap, delivery ops | 220 000 | 66 000 | 286 000 |
| Designer | templates, brand adaptation, UI kits | 180 000 | 54 000 | 234 000 |
| SDR | outbound, qualification | 140 000 | 42 000 | 182 000 |
| AE | demo, proposal, close | 280 000 | 84 000 | 364 000 |
| Customer Success | support, upsell, retention | 200 000 | 60 000 | 260 000 |
| **Итого** |  |  |  | **4 056 000 ₽ / мес** |

### 8.2 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 400 000 | 1-2 | 1,5 | 120 000 | 520 000 |
| ML Engineer (если AI core) | 0 | — | — | — | — | — |
| DevOps | 1 | 250 000 | 1-2 | 1 | 75 000 | 325 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 140 000 + бонус 15% | 0,5-1 | 1 | 42 000 | 182 000 |
| AE (Account Exec) | 1 | 280 000 + комиссия | 1-2 | 2-3 | 84 000 | 364 000 |
| Customer Success | 1 | 200 000 | 1 | 1 | 60 000 | 260 000 |
| Product / Project Manager | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Designer | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |

### Salary benchmark notes
- Senior backend в Москве по HH обычно лежит в диапазоне **350-550k ₽ gross**. Пример поиска: https://hh.ru/search/vacancy?text=Senior+Backend+Moscow
- Team Lead / CTO-like engineering роли на HH часто лежат в диапазоне **450-700k ₽ gross**. Пример: https://hh.ru/search/vacancy?text=Tech+Lead+Moscow
- SDR / sales development по Москве обычно около **120-200k ₽** total comp. Пример поиска: https://hh.ru/search/vacancy?text=SDR+Moscow
- AE / enterprise sales роли часто находятся около **250-400k ₽ + variable**. Пример поиска: https://hh.ru/search/vacancy?text=Account+Executive+Moscow

## 9. Cumulative FOT timeline M1-M12

Найм раскручивается постепенно. Красный флаг 5+ hires в M1 не нарушаем.

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO / Founder | 780 000 |
| M2 | + Product / Project Manager | 1 066 000 |
| M3 | + Frontend | 1 456 000 |
| M4 | + Designer | 1 690 000 |
| M5 | + Senior Backend | 2 210 000 |
| M6 | + SDR | 2 392 000 |
| M7 | + AE | 2 756 000 |
| M8 | + Customer Success | 3 016 000 |
| M9 | + DevOps | 3 341 000 |
| M10 | + CTO / Tech Lead | 4 056 000 |
| M11 | команда укомплектована | 4 056 000 |
| M12 | команда укомплектована | 4 056 000 |

## 10. Fixed costs breakdown

Для unit economics и break-even беру **рабочий fixed-cost base 2 100 000 ₽/мес**, а не full 4,056 млн ₽, потому что часть delivery-команды уже сидит в COGS и не должна считаться дважды.

| Компонент | ₽ / мес |
|---|---:|
| CEO / Founder allocation | 500 000 |
| PM / delivery ops fixed layer | 220 000 |
| SDR + AE fixed portion | 450 000 |
| Customer Success fixed portion | 140 000 |
| Admin / legal / accounting | 90 000 |
| Tools / subscriptions fixed base | 120 000 |
| Office / coworking / equipment | 80 000 |
| Founder travel / events / misc overhead | 100 000 |
| Buffer for scope creep / rework | 400 000 |
| **Итого fixed costs** | **2 100 000 ₽ / мес** |

## 11. Break-even по клиентам и по месяцу

### Break-even по client count

| Метрика | Формула | Значение |
|---|---|---:|
| Contribution per active client | 55 000 - 24 000 | 31 000 ₽ |
| Fixed costs | — | 2 100 000 ₽ |
| **Break-even clients** | 2 100 000 / 31 000 | **67,7 ≈ 68 клиентов** |
| Safety break-even with 5% slippage | ~68 × 1,05 | **72 клиента** |

### Break-even по выручке в месяц

| Метрика | Формула | Значение |
|---|---|---:|
| Contribution Margin % | 31 000 / 55 000 | 56,4% |
| Fixed costs | — | 2 100 000 ₽ |
| **Break-even revenue / month** | 2 100 000 / 56,4% | **3,72 млн ₽** |
| Safety break-even revenue | с operational slippage | **3,96 млн ₽ / мес** |

### EBITDA при 50 клиентах

| Метрика | Формула | Значение |
|---|---|---:|
| Revenue @50 active clients | 50 × 55 000 | 2 750 000 ₽ |
| Gross profit @50 | 50 × 31 000 | 1 550 000 ₽ |
| Fixed costs | — | 2 100 000 ₽ |
| **EBITDA @50 clients** | 1 550 000 - 2 100 000 | **-550 000 ₽ / мес** |

Это прямой **Profit Gate FAIL**.

## 12. Burn-to-breakeven и cash runway

Допущение: startup_capital = **25 млн ₽**.

### Burn path
| Период | Средний burn / мес | Месяцев | Cash burn |
|---|---:|---:|---:|
| M1-M3 | 1,30 млн ₽ | 3 | 3,90 млн ₽ |
| M4-M6 | 2,00 млн ₽ | 3 | 6,00 млн ₽ |
| M7-M9 | 2,60 млн ₽ | 3 | 7,80 млн ₽ |
| M10-M12 | 3,00 млн ₽ | 3 | 9,00 млн ₽ |
| **Итого burn до конца M12** |  |  | **26,70 млн ₽** |

Даже если предположить, что break-even достигается ближе к **M15-M18**, потребность в капитале всё равно превышает **25 млн ₽**, потому что найм, CAC и rework съедают маржу раньше, чем растёт support base.

### Burn-to-breakeven
| Метрика | Значение |
|---|---:|
| Startup capital | 25,0 млн ₽ |
| Estimated burn to operational breakeven | 28,0-30,0 млн ₽ |
| Gap | 3,0-5,0 млн ₽ |

### Cash runway
| Метрика | Формула | Значение |
|---|---|---:|
| Начальный капитал | — | 25,0 млн ₽ |
| Средний burn первого года | 26,7 / 12 | 2,23 млн ₽/мес |
| **Cash runway** | 25,0 / 2,23 | **11,2 мес** |

Для B2B enterprise SaaS это уже было бы мало. Для студии с низким moat это тем более слабый профиль.

## 13. Почему модель не investment-grade

1. **Слишком большая доля разовой выручки.** Экономика выглядит лучше на уровне проекта, чем на уровне накопленного recurring cash flow.
2. **Retainer attach rate низкий, churn высокий.** Без устойчивого support base невозможно вытянуть LTV.
3. **Fully-loaded CAC съедает upside.** Founder time, pre-sale и sales FOT нельзя игнорировать.
4. **EBITDA на 50 клиентах отрицательная.** Это критичный fail по порогу программы.
5. **Moat слабый.** Шаблоны, скорость и Bolt.new сами по себе не защищают от копирования.

## 14. Финальный вывод

Кейс может работать как **небольшой founder-led cash-flow agency business**, но **не проходит инвестиционный фильтр фонда**. Для investment-grade версии пришлось бы доказать:
- retainer attach rate **60%+**,
- recurring ARPA **40k+ ₽**,
- churn **≤4%/мес**,
- blended fully-loaded CAC **<100k ₽**,
- EBITDA **>500k ₽/мес** уже в диапазоне **40-50 активных клиентов**.

С текущими допущениями это не достигается.
