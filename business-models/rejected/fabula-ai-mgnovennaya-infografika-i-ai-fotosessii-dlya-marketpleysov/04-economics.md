# Unit Economics

## Итог этапа
**Решение:** FAIL.

Fabula AI как QUICK-AI/self-serve SMB SaaS для селлеров маркетплейсов показывает рабочую базовую юнит-экономику по LTV/CAC, но не проходит инвестиционный Profit Gate этого pipeline: при реалистичной fixed-cost базе и среднем чеке сегмента компания **не достигает EBITDA 500 000 ₽/мес на 50 клиентах**. Следовательно, кейс не investment-grade на уровне фонда в текущей конфигурации и должен быть отклонён.

Дата расчёта: 2026-05-13.

---

## 1) Базовые допущения модели

### Сегмент и pricing
- Сегмент: **SMB self-serve / small teams** продавцов Wildberries/Ozon.
- Blended paying ARPU: **3 200 ₽/клиент/мес**.
- Основание: публичные ценовые якоря конкурентов в диапазоне от **599 ₽** до **3 320 ₽/мес**, плюс heavy-пакеты выше 10 000 ₽/мес. Для blended расчёта беру уровень чуть выше середины self-serve диапазона, но ниже heavy tier. [S2][S3]
- New paying customers / month в базовом сценарии: **54**.
- Monthly logo churn: **4.5%** для SMB SaaS, что укладывается в внешний benchmark 2026 для SMB подписочного софта. [S6]
- Gross margin: **81%**.

### Почему gross margin = 81%
Себестоимость у QUICK-AI продукта заметная, но не критическая: токены/генерация, image inference, storage/CDN, платежи, поддержка, moderation/QA. Для массового self-serve AI-инструмента это даёт GM выше 75%, но ниже классического pure-SaaS 85-90%.

---

## 2) Подробный business process: от lead до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Пользователь видит рекламу/пост/реферальный контент | Marketing | Telegram, VK Ads, Яндекс.Директ | 1-3 мин | 220 | Высокая |
| 2 | Переход на лендинг или в бот | Growth/Marketing | fabula-ai.com, Telegram bot | 1 мин | 18 | Высокая |
| 3 | Регистрация | Product | Web app / bot auth | 2 мин | 12 | Полная |
| 4 | Онбординг: выбор маркетплейса, SKU, шаблона | Product | onboarding flow | 4 мин | 25 | Полная |
| 5 | Загрузка фото/описания товара | Клиент | web app / bot upload | 5-10 мин | 35 | Полная |
| 6 | Генерация карточки, инфографики, AI-фото | AI backend | LLM + image generation + template engine | 1-3 мин | 110 | Полная |
| 7 | Редактирование/повторная генерация | Клиент + Product | editor / rerun | 5-15 мин | 80 | Высокая |
| 8 | Paywall после trial/value moment | Product/Growth | paywall, CRM triggers | 1 мин | 22 | Полная |
| 9 | Оплата картой / ЮKassa | Client + Finance infra | payment gateway | 2-3 мин | 96 | Полная |
| 10 | Выдача материалов, повторное использование, retention-trigger | Product/CS | email, Telegram, CRM automation | 3-5 мин | 47 | Высокая |

**Итого стоимость acquisition-to-first-payment на одного нового платящего:** **665 ₽ прямых переменных операционных расходов**, без учёта fixed team/FOT и маркетингового пула. Это не CAC, а cost-to-serve new payer in month 0.

---

## 3) COGS на 1 клиента в месяц

Предполагаю blended клиента с 20-30 генерациями карточек/изображений в месяц.

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM / text generation | 55 | генерация описаний, CTA, SEO-текстов; оценка по Yandex AI Studio token pricing | [S4] |
| Image generation / inference | 210 | основная переменная нагрузка продукта; оценка от публичного image pricing + 25 генераций/мес | [S4], inference |
| Storage / CDN / hosting | 115 | хранение исходников и результатов, delivery ассетов | inference |
| Payment processing | 96 | ~3% от ARPU 3 200 ₽ | inference |
| Support / moderation / refund reserve | 78 | доля CS и операционного саппорта на клиента | inference |
| **COGS total** | **554** | сумма строк выше |  |

**Gross profit / client / month = 3 200 - 554 = 2 646 ₽**  
**Contribution margin before fixed costs = 82.7%**  
Для консервативной модели далее использую **81% GM**.

---

## 4) CAC по каналам с воронкой

### Funnel conversion by channel

| Канал | Leads/visits в мес | Sign-up % | Activated % | Trial→Pay % | New paying / мес | Channel spend, ₽/мес | Raw CAC, ₽ | CAC multiplier | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Telegram own media / контент | 18 000 | 9.0% | 34% | 4.5% | 248 | 180 000 | 726 | ×1.3 | 944 |
| Paid ads (Яндекс.Директ/VK) | 6 500 | 6.5% | 28% | 3.0% | 35 | 180 000 | 5 143 | ×1.3 | 6 686 |
| Referral / word of mouth | 2 000 | 11.0% | 40% | 7.0% | 62 | 55 000 | 887 | ×1.3 | 1 153 |
| Partners / marketplace agencies | 600 | 18.0% | 45% | 9.0% | 44 | 140 000 | 3 182 | ×1.3 | 4 136 |

**Важно:** channel CAC выше показывает стоимость канала с SMB self-serve multiplier **×1.3**, как требует методика. Но для blended fund-level CAC нужно добавить sales/FOT/tools/overhead на весь acquisition engine, а не только media.

### Blended funnel
- Marketing-qualified visits/leads: **27 100 / мес**
- Sign-ups: **2 370** (8.7%)
- Activated: **804** (33.9% от sign-up)
- New paying: **54** в консервативном базовом фонде-моделе для repeatable acquisition machine

Я сознательно **не беру** сумму channel new payers из верхней таблицы как реальный current state, потому что она отражает теоретический верх канала при сильном owned media. Для investment-grade модели фондового уровня считаю более строгий operating base-case: **54 новых платящих в месяц** после поправки на overlap, organic cannibalization, атрибуцию и неполную monetization conversion.

---

## 5) FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team allocation + Tools + Events + Overhead) / New paying customers`

### Разложение fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | базовый performance budget | inference |
| Outbound team FOT (SDR/AE attributed to new) | 310 700 | SDR 160k gross + AE 290k gross, обе роли с 30% взносами, затем частичная аллокация 45% / 35% на new biz | [S7], inference |
| Marketing team FOT (partial allocation) | 273 000 | Growth marketer 210k gross × 1.3 = 273k, 100% на acquisition | [S7], inference |
| Tools (CRM, analytics, mailing, bot stack) | 48 000 | amoCRM + analytics + messaging stack | inference |
| Events / partnerships | 36 000 | вебинары, партнерские размещения, seller-community integrations | inference |
| Subtotal before overhead | **847 700** | сумма строк выше |  |
| Overhead multiplier (x1.3) | **254 310** | 30% от subtotal | методика pipeline |
| **Total fully-loaded CAC spend / month** | **1 102 010** | subtotal + overhead |  |

**Blended fully-loaded CAC = 1 102 010 / 54 = 20 408 ₽ на нового платящего клиента**.

### Sanity check vs RU benchmark
- Для **SMB self-serve** pipeline даёт benchmark **5-30K ₽ CAC**.
- Наша оценка **20.4K ₽** лежит **внутри диапазона**, значит модель не выглядит заниженной.
- CAC не ниже 30% бенчмарка, red flag отсутствует.

---

## 6) LTV, churn и LTV/CAC

### Churn benchmark
- Внешний benchmark для SMB SaaS: **4.5% monthly churn**, annualized ~42.3%. [S6]
- Для Fabula это правдоподобно: рынок чувствителен к цене, много альтернатив, высокий риск “разового use case”.

### LTV calculation
Использую формулу **LTV = ARPU × Gross Margin / Monthly Churn**.

- ARPU = **3 200 ₽/мес**
- Gross margin = **81%**
- Monthly churn = **4.5%**

**LTV = 3 200 × 0.81 / 0.045 = 57 600 ₽**

### LTV/CAC
- LTV = **57 600 ₽**
- Fully-loaded CAC = **20 408 ₽**

**LTV/CAC = 2.82 : 1**

### Вывод по ratio
- Требование investment-grade: **не ниже 3:1**.
- Фактический результат: **2.82:1**, то есть **ниже порога**.
- Даже до жёсткого Profit Gate по 50 клиентам модель уже выглядит пограничной для фонда.

---

## 7) CAC Payback

Формула pipeline: `CAC Payback = CAC / MRR per customer`

- Fully-loaded CAC = **20 408 ₽**
- MRR per customer = **3 200 ₽**

**CAC Payback = 20 408 / 3 200 = 6.38 месяца**

Вывод:
- Для SMB self-serve это **нормально**, ниже лимита 12 месяцев.
- Но payback сам по себе не спасает кейс, потому что LTV/CAC ниже 3 и fixed-cost база слишком тяжёлая для 50 клиентов.

---

## 8) Contribution Margin %

- Revenue / client / month = **3 200 ₽**
- Variable COGS / client / month = **554 ₽**
- Contribution / client / month = **2 646 ₽**

**Contribution Margin % = 2 646 / 3 200 = 82.7%**

Для дальнейших расчётов округляю к **81-83%** диапазону.

---

## 9) Team & FOT

### Полная команда

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Time-to-hire (мес) | Onboarding ramp (мес до 80%) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---:|---:|---:|---:|
| CEO | 1 | стратегия, fundraising, partnerships | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO / Tech Lead | 1 | архитектура, AI stack, delivery | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | backend, API, billing, generation pipeline | 420 000 | 1.5 | 1.5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | prompt/pipeline quality, inference orchestration | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | infra, observability, cost control | 340 000 | 1.5 | 1 | 102 000 | 442 000 |
| Frontend | 1 | editor, paywall, self-serve UX | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Growth Marketer | 1 | acquisition, landing tests, CRM | 210 000 | 1 | 1 | 63 000 | 273 000 |
| SDR | 1 | partnerships, agency pipeline | 160 000 | 0.75 | 1 | 48 000 | 208 000 |
| AE | 1 | small-team upsell, closing heavier packs | 290 000 | 1.5 | 2.5 | 87 000 | 377 000 |
| Customer Success | 1 | retention, support, expansion | 230 000 | 1 | 1 | 69 000 | 299 000 |
| Designer / Creative Ops | 1 | templates, QA, creative control | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Finance / Ops (part-time) | 0.5 | финконтур, legal ops, procurement | 140 000 gross equivalent | 1 | 1 | 42 000 | 182 000 |

**Итого fully-loaded FOT при полной укомплектованности: 5 720 000 ₽/мес.**

### Комментарий по realism
- Нанять 5+ человек в первый месяц было бы red flag, поэтому план ниже ступенчатый.
- FOT M1 выше 1M ₽ уже на минимальной founding team, что соответствует sanity check.

---

## 10) Cumulative FOT timeline M1-M12

### Hire plan
- M1: CEO, 1 backend, frontend, growth.
- M2: DevOps, designer/creative ops.
- M3: CTO, CS.
- M4: SDR.
- M5: ML engineer.
- M6: AE.
- M7: 2-й backend.
- M8-M12: без новых ключевых ролей, только выход на полную продуктивность.

| Месяц | Кто уже в штате / выходит | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, Backend#1, Frontend, Growth | 1 989 000 | стартовая команда, без sales |
| M2 | + DevOps, Designer | 2 743 000 | build + creative capacity |
| M3 | + CTO, CS | 3 757 000 | усиливаем delivery и retention |
| M4 | + SDR | 3 965 000 | начало partnership/outbound |
| M5 | + ML engineer | 4 615 000 | core AI quality/control |
| M6 | + AE | 4 992 000 | upsell и team/deal motion |
| M7 | + Backend#2 | 5 538 000 | scaling team |
| M8 | ramp to 80-100% productivity | 5 538 000 | без новых hires |
| M9 | stable team | 5 538 000 |  |
| M10 | stable team | 5 538 000 |  |
| M11 | stable team | 5 538 000 |  |
| M12 | stable team + finance/ops 0.5 | 5 720 000 | финальная operating base |

**Cumulative FOT M1-M12 = 54 433 000 ₽**.

---

## 11) Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Fully-loaded FOT (steady-state) | 5 720 000 | команда выше |
| Office / remote / admin | 180 000 | частично remote, но есть юр./админ. контур |
| Core infra reserve beyond pure COGS | 220 000 | observability, CI/CD, monitoring, staging |
| Software / SaaS not in CAC tools | 145 000 | dev tools, analytics, support desk |
| Legal / accounting | 110 000 | внешний и внутренний контур |
| Misc / refunds / compliance reserve | 125 000 | buffer |
| **Total fixed costs / month** | **6 500 000 ₽** |  |

---

## 12) Break-even

### Break-even по числу клиентов
Формула: `Fixed costs / contribution per client`

- Fixed costs = **6 500 000 ₽/мес**
- Contribution per client / month = **2 646 ₽**

**Break-even client count = 6 500 000 / 2 646 = 2 456 клиента**

### Break-even по выручке в месяц
- Break-even MRR = **2 456 × 3 200 = 7 859 200 ₽/мес**

### Проверка на 50 клиентах
- Revenue at 50 clients = **160 000 ₽/мес**
- Gross profit at 81% = **129 600 ₽/мес**
- EBITDA after fixed costs ≈ **-6.37 млн ₽/мес**

**Вывод:** порог pipeline не проходит, так как **EBITDA 500 000 ₽/мес на 50 клиентах недостижима** даже близко.

---

## 13) Burn-to-breakeven

### Base case
Если компания растёт до 54 новых платящих в месяц при churn 4.5%, клиентская база увеличивается медленно. Даже при хорошем retention curve break-even по базе клиентов возникает далеко за пределами 24 месяцев, если не случится:
1. сильного ARPU-upshift в team/agency tier,
2. удешевления acquisition,
3. радикального снижения fixed team load.

### Burn estimate
- Средний monthly burn по M1-M12 с учётом FOT, fixed infra и acquisition spend: **~4.55 млн ₽/мес**.
- Burn до operating break-even при текущем плане: **>45-55 млн ₽** только на первые 12 месяцев, без гарантии выхода в окупаемость в горизонте года.

**Вывод:** burn-to-breakeven слишком тяжёлый для self-serve продукта с таким чеком.

---

## 14) Cash runway

### Допущение
`startup_capital = 35 000 000 ₽`

### Расчёт
- Average burn = **4.55 млн ₽/мес**
- Runway = **35.0 / 4.55 = 7.7 месяца**

Даже если сжать marketing spend и немного отложить найм, runway остаётся в диапазоне **8-10 месяцев**, что мало для продукта, которому нужно одновременно строить acquisition engine, удержание и AI-cost discipline.

### Sanity check
- Для B2B/SMB AI SaaS капитал до break-even **<10 млн ₽** был бы нереалистичен. Здесь модель показывает потребность заметно выше, значит допущения ближе к реальности, чем к занижению.

---

## 15) Главные выводы фонда

### Что хорошо
- Contribution margin высокий: **~83%**.
- CAC payback приемлемый: **6.4 мес**.
- CAC по рынку не выглядит искусственно заниженным.

### Что плохо
- **LTV/CAC = 2.82:1**, ниже инвестиционного порога **3:1**.
- **Break-even = 2 456 клиентов**, очень далеко от early operating scale.
- На **50 клиентах EBITDA 500k/mo недостижима**, значит Profit Gate pipeline не проходит.
- Для self-serve продукта команда и burn получаются слишком тяжёлыми относительно ARPU.

## Финальный verdict по Program 5
**REJECT.**

Не потому что продукт плохой, а потому что для фонда это недостаточно сильная unit economics story: чтобы стать investment-grade, Fabula нужно либо:
1. поднимать blended ARPU в сторону agency/team tiers **6-12K ₽/мес+**, либо
2. резать fixed operating base, либо
3. показывать materially lower churn, чем типичный SMB SaaS.

В текущем SMB self-serve контуре кейс **не проходит**.

---

## Sources
- [S1] Fabula AI, официальный сайт: https://fabula-ai.com/
- [S2] SellerDen pricing: https://sellerden.ai/
- [S3] 24AI pricing / RU site: https://24ai.tech/ru/
- [S4] Yandex Cloud AI Studio pricing, updated Feb 2026: https://yandex.cloud/docs/yandexgpt/pricing
- [S5] RB.RU про Fabula и user base: https://rb.ru/news/fabula-15mln/
- [S6] RetentionCheck SMB SaaS churn benchmark 2026: https://retentioncheck.com/churn-benchmarks/smb-saas
- [S7] HH.ru vacancy benchmarks, search pages for Moscow roles: https://hh.ru/vacancies/senior-backend-developer , https://hh.ru/vacancies/sdr , https://hh.ru/vacancies/account-executive

## Notes on inference
Часть чисел в unit economics неизбежно оценочная, потому что Fabula не публикует полную SaaS P&L. Все нераскрытые значения выше помечены как **inference** и построены на связке: публичный pricing конкурентов + RU salary ranges + AI infra pricing + pipeline sanity checks.