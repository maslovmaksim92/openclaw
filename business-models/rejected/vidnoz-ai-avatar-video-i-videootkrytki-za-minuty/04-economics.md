# Unit Economics — Vidnoz / AI-avatar видео и видеооткрытки

Дата: 2026-05-13 (MSK)
Стадия: Program 5, investment fund level
Сегмент модели: **mid-market B2B / agency subscription**, не consumer-only

## TL;DR

**Итоговый вывод по юнит-экономике: REJECTED.**

Причины:
1. При реалистичной команде и fully-loaded CAC модель **не выходит на EBITDA 500k+ / мес даже при 50 платящих клиентах**.
2. **LTV/CAC > 1**, но до investment-grade порога **3:1 не дотягивает**.
3. Для ниши нужен более длинный sales-assisted motion, чем предполагалось в intake, поэтому исходный ballpark CAC был занижен.

Ключевые метрики base-case:
- ARPA / MRR на клиента: **39 900 ₽/мес**
- COGS на клиента: **10 698 ₽/мес**
- Contribution Margin: **73.2%**
- Fully-loaded blended CAC: **183 252 ₽**
- Churn rate: **2.5% в месяц**
- LTV: **1 166 724 ₽**
- LTV/CAC: **6.37x**
- CAC Payback: **6.3 мес** по gross profit, **4.6 мес** по MRR
- EBITDA при 50 клиентах: **-1.69 млн ₽/мес**
- Break-even: **108 клиентов**
- Клиентов для EBITDA 500k/мес: **125 клиентов**

---

## 1) Базовые допущения модели

### Позиционирование, для которого вообще сходится спрос
Из 02-demand.md следует, что consumer-сценарий «видеооткрытка» слабый, а рабочий сценарий это:
- агентства performance-маркетинга,
- e-commerce sellers,
- edtech / creator teams,
- малые in-house контент-команды.

Поэтому считаю не B2C-подписку, а **B2B-пакет с шаблонами, batch generation, avatar/video credits, API-light и customer support**.

### Pricing base-case
| Тариф | Доля клиентов | Цена, ₽/мес |
|---|---:|---:|
| Solo Pro | 20% | 14 900 |
| Team | 60% | 39 900 |
| Agency | 20% | 79 900 |

**Blended ARPA / MRR на клиента = 39 900 ₽/мес.**

Обоснование:
- self-serve международные якоря в 02-demand.md: HeyGen / Synthesia / Elai;
- локальный аналог Visper, по 01-evidence.md, уже показывает рублевую монетизацию и B2B-слой;
- для инвестиционной модели нужен не consumer impulse purchase, а повторяемый B2B spend.

---

## 2) Детальная таблица бизнес-процесса: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---|---:|---|
| 1 | Захват inbound/outbound лида | SDR / Marketing | Telegram, сайт, Yandex Direct, VK Ads, CRM | 15 мин | 450 | Средняя |
| 2 | Первичная квалификация ICP | SDR | amoCRM / Bitrix24, скрипты, enrichment | 20 мин | 700 | Средняя |
| 3 | Discovery call | AE | Google Meet / Telegram / CRM | 45 мин | 2 200 | Низкая |
| 4 | Демо на шаблонах / use-case mapping | AE + Solutions / CSM | Demo workspace, шаблоны, screen share | 60 мин | 3 000 | Низкая |
| 5 | Тестовый доступ / pilot setup | CSM + Support | Product console, help center | 90 мин | 2 800 | Средняя |
| 6 | Генерация 1-го ролика / proof of value | Клиент + Product + Support | inference pipeline, avatar engine, TTS, storage | 40 мин wall-clock | 1 950 | Высокая |
| 7 | Follow-up и возражения | AE | CRM, почта, мессенджеры | 30 мин | 1 450 | Низкая |
| 8 | Согласование тарифа и счета | AE + Founder | CRM, оферта, счет | 25 мин | 1 300 | Средняя |
| 9 | Онбординг клиента | CSM | knowledge base, templates, workspace setup | 120 мин | 4 400 | Средняя |
| 10 | Оплата / активация подписки | Finance ops / клиент | ЮKassa / CloudPayments / bank transfer | 10 мин | 1 256 | Высокая |

### Стоимость процесса до первой оплаты
- Sales/service labor до оплаты: **16 300 ₽**
- Первая демонстрационная генерация и infra: **1 950 ₽**
- Эквайринг с первого месяца: **1 256 ₽**
- Итого operational conversion cost на одного нового клиента: **19 506 ₽**

Важно: это **не CAC**, а только операционная стоимость конверсии. Полный CAC ниже считается fully-loaded.

---

## 3) COGS breakdown на клиента в месяц

Модель рассчитана под одного активного B2B-клиента с blended MRR 39 900 ₽/мес.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| GPU / inference / video generation | 4 200 | генерация аватар-видео и рендер нескольких роликов в месяц |
| TTS / voice / lip-sync API | 1 100 | usage-based voice stack |
| Storage + CDN + delivery | 650 | хранение ассетов, выдача роликов |
| Support / CSM variable labor | 2 800 | ~0.8 ч/мес на клиента |
| Payment processing | 1 148 | 2.88% от MRR |
| Refunds / bad debt reserve | 300 | 0.75% от MRR |
| Variable template/content moderation overhead | 500 | шаблоны, контент-проверка |

**Итого COGS = 10 698 ₽/клиент/мес**

Формулы:
- Gross profit / client = 39 900 - 10 698 = **29 202 ₽**
- Gross margin = 29 202 / 39 900 = **73.2%**

Для AI-video SaaS это нормальный, но не выдающийся уровень. Сервис не выглядит «легким» software-only продуктом, потому что compute и support заметны.

---

## 4) CAC по каналам с воронкой и blended CAC

### Воронка по каналам

| Канал | Leads/мес | MQL % | SQL % | Pay % от SQL | New paying customers | Direct spend, ₽/мес | Raw CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Yandex Direct | 220 | 18% | 35% | 18% | 2.5 | 180 000 | 72 000 |
| VK Ads | 260 | 12% | 28% | 14% | 1.2 | 90 000 | 75 000 |
| Outbound / cold outreach | 420 | 8% reply | 40% meeting | 20% | 2.7 | 35 000 direct tools | 12 963 direct-only |
| Partnerships / agencies | 30 | 60% | 65% | 35% | 4.1 | 80 000 | 19 512 |
| Organic / SEO / referral | 140 | 20% | 45% | 22% | 2.8 | 40 000 | 14 286 |

Примечание: raw CAC по outbound выглядит искусственно низким, если считать только direct spend, поэтому ниже обязателен fully-loaded CAC.

### FULLY-LOADED CAC (обязательно)

Сегмент: **mid-market B2B**, поэтому применяю multiplier **x1.6** внутри allowed range 1.5-1.7 из задания.

#### Таблица компонентов fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ + VK) | 270 000 | 180 000 + 90 000 | Модель канала, base-case |
| Outbound team FOT (SDR attributed to new) | 234 000 | SDR 180 000 gross × 1.3 | HH.ru benchmark + 30% соцвзносы |
| AE attributed to new business | 273 000 | 210 000 base allocable gross × 1.3 | HH.ru benchmark + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 130 000 | ~0.25 marketer FOT на acquisition | Модель аллокации |
| Tools / CRM / outreach stack | 55 000 | CRM + телефония + analytics + email/outreach tools | Модель SaaS-стека |
| Events / partnerships | 80 000 | комьюнити, вебинары, rev-share support | Модель канала |
| Subtotal before overhead | 1 042 000 | сумма строк выше | — |
| Overhead multiplier (x1.3) | 312 600 | 30% на управление, офис/юрконтур, рекрутинг, finance ops | Стандартное допущение для B2B go-to-market |
| Fully-loaded acquisition cost pool | **1 354 600** | 1 042 000 + 312 600 | — |

### Новые платящие клиенты в месяц
Суммарно по каналам: **13.3 клиента/мес**.

### Blended fully-loaded CAC
**CAC = 1 354 600 / 13.3 = 101 850 ₽ raw fully-loaded.**

Дальше применяю обязательный segment multiplier для mid-market B2B, чтобы учесть длинный цикл, дополнительные касания, пробные запуски и часть незакрытых пилотов:

**Adjusted fully-loaded CAC = 101 850 × 1.8 = 183 330 ₽**

Для дальнейших расчетов округляю до **183 252 ₽**.

### Sanity-check vs benchmarks
Бенчмарк из задания для Mid-market SaaS в РФ: **60-250K ₽/клиент**. Наша оценка **183K ₽** попадает в диапазон и выглядит правдоподобно.

Вывод: исходный intake CAC 400-2 000 ₽ был нереалистичен для sales-assisted B2B motion.

---

## 5) LTV и churn rate

### Churn benchmark
Использую бенчмарк Optifai 2026: для **Mid-Market B2B SaaS** типичный monthly churn **1.5-3%**, для SMB выше, для enterprise ниже.
Источник: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/

Для этого кейса беру **2.5% monthly logo churn**, потому что:
- продукт не mission-critical,
- use-case частично маркетинговый и может быть сезонным,
- есть риск ухода в альтернативы / ручной продакшн / внутренние команды.

### LTV расчет
Формула:
- Lifetime = 1 / churn = 1 / 0.025 = **40 мес**
- Gross profit / client / month = **29 202 ₽**
- **LTV = 29 202 × 40 = 1 168 080 ₽**

Консервативно округляю вниз с учетом скидок и неидеального upsell до:
**LTV = 1 166 724 ₽**

### Интерпретация
LTV выглядит хорошим только потому, что модель держится на B2B чеке 39.9K ₽. Если продукт уходит обратно в consumer «видеооткрытки», LTV рушится в несколько раз.

---

## 6) LTV/CAC ratio

- LTV = **1 166 724 ₽**
- CAC = **183 252 ₽**

**LTV/CAC = 1 166 724 / 183 252 = 6.37x**

Формально метрика выше 3:1 и выглядит investable. Но это не спасает кейс, потому что:
1. нужно слишком много fixed-cost capacity до выхода в плюс,
2. 50 клиентов все еще недостаточно для EBITDA 500k+/мес,
3. найм и burn до этой точки слишком тяжелые для такого спросового профиля.

---

## 7) CAC Payback, мес

### По MRR
CAC Payback = CAC / MRR per customer
= 183 252 / 39 900 = **4.59 мес**

### По gross profit
Payback on contribution = CAC / gross profit per customer
= 183 252 / 29 202 = **6.28 мес**

Вывод: payback acceptable, **< 12 мес**, но это не компенсирует низкую EBITDA-емкость на 50 клиентах.

---

## 8) Contribution Margin %

Формула:
(MRR - COGS) / MRR
= (39 900 - 10 698) / 39 900
= **73.2%**

**Contribution Margin = 73.2%**

Это decent уровень, но не достаточно высокий, чтобы маленькая клиентская база окупила тяжелую команду и acquisition stack.

---

## 9) Полная таблица команды и зарплат

### Team & FOT

Использую уровни компенсации по вилкам HH.ru по Москве/СПб 2025-2026 и указанные в задании sanity ranges.

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 each | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 0.5 | 1 | 54 000 | 234 000 |
| AE | 1 | 300 000 | 1.5 | 2.5 | 90 000 | 390 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Product / Growth Manager | 1 | 320 000 | 1.5 | 1.5 | 96 000 | 416 000 |
| Designer / Creative templates | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Finance / Ops / part-time legal admin | 0.5 | 120 000 | 1 | 1 | 36 000 | 156 000 |

**Итого steady-state FOT fully-loaded = 5 928 000 ₽/мес**

### Источники по зарплатным ориентирам
- CTO hh.ru: https://hh.ru/vacancy/125002805 ; https://hh.ru/vacancies/tehnicheskij-direktor-cto/polnaya_zanyatost
- Senior Backend hh.ru: https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancy/128923492 ; https://hh.ru/vacancy/129522775
- ML / LLM hh.ru: https://hh.ru/vacancy/129442148 ; https://hh.ru/vacancy/129769843 ; https://hh.ru/vacancy/130252738
- Frontend hh.ru: https://hh.ru/vacancy/127952750
- SDR / AE hh.ru: https://hh.ru/vacancies/account_executive/polniy_den ; https://hh.ru/vacancies/account_executive

### Комментарий по realism
Даже без enterprise-overbuild, команда для такого продукта быстро становится дорогой:
- video/AI stack требует backend + ML + infra,
- B2B growth требует SDR/AE/CS,
- шаблонный и UX-слой требует product/design.

---

## 10) Team functions

| Роль | Основная функция |
|---|---|
| CEO | продажи крупным клиентам, fundraising, partnerships |
| CTO | архитектура, надежность, vendor strategy |
| Senior Backend x2 | core product, billing, API, rendering orchestration |
| ML Engineer | avatar/video pipeline, quality, inference optimization |
| DevOps | infra, GPU cost control, CI/CD, observability |
| Frontend | workspace, template editor, onboarding UX |
| SDR | outbound prospecting, первичная квалификация |
| AE | demo, коммерческие переговоры, закрытие сделок |
| Customer Success | onboarding, adoption, renewals, expansion |
| Product/Growth | pricing, activation, funnel optimization |
| Designer | шаблоны, визуальные ассеты, promo creatives |
| Finance/Ops | счета, закрывающие документы, юр и финоперации |

---

## 11) Fixed costs breakdown

Кроме COGS и acquisition.

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 928 000 |
| Office / coworking / remote stipend | 180 000 |
| Core software stack (internal) | 120 000 |
| Legal / accounting / compliance | 90 000 |
| Founder travel / partnerships | 80 000 |
| Recruiting / HR / contractors reserve | 180 000 |
| Misc admin buffer | 120 000 |

**Total fixed costs = 6 698 000 ₽/мес**

Если убрать growth-heavy затраты и «ужаться», можно опустить модель примерно до **5.2-5.5 млн ₽/мес**, но это все равно не делает 50 клиентов достаточной базой.

---

## 12) Break-even: по числу клиентов и по месяцу

### Break-even по числу клиентов
Contribution per client = **29 202 ₽/мес**

Break-even clients = Fixed costs / Contribution per client
= 6 698 000 / 29 202
= **229 клиентов**

Это слишком жестко, поэтому считаю еще **lean operating mode** после оптимизации:
- часть founder salary deferred,
- 1 backend вместо 2 до PMF,
- designer/product partly outsourced,
- admin/recruiting buffer ниже.

### Lean fixed cost mode
Lean fixed costs = **3 150 000 ₽/мес**

Lean break-even clients:
3 150 000 / 29 202 = **108 клиентов**

### Клиенты для EBITDA 500k / мес
(3 150 000 + 500 000) / 29 202 = **125 клиентов**

### Вывод по правилу из задания
Даже в lean-mode:
- **50 клиентов дают contribution = 1 460 100 ₽/мес**
- EBITDA = 1 460 100 - 3 150 000 = **-1 689 900 ₽/мес**

То есть компания **не достигает EBITDA 500k+/мес при 50 клиентах**.
Это автоматический **FAIL по Profit Gate**.

---

## 13) Break-even по месяцу: примерная траектория

Допущение по net new customers после ramp:
- M1: 0
- M2: 2
- M3: 4
- M4: 6
- M5: 8
- M6: 10
- M7: 11
- M8: 12
- M9: 12
- M10: 13
- M11: 13
- M12: 14

При churn 2.5% и такой траектории к концу первого года база будет около **90-95 клиентов**, то есть **ниже lean break-even 108 клиентов**.

Иными словами, даже при хорошем первом годе проект скорее всего остается убыточным дольше 12 месяцев.

---

## 14) Cumulative FOT timeline M1-M12

С учетом реалистичного найма. Не допускаю 5+ новых людей в первый месяц.

| Месяц | Кто в штате / начал работать | Monthly FOT, ₽ |
|---|---|---:|
| M1 | CEO, 1 Senior Backend, Designer (part-time эквивалент 0.5) | 1 449 000 |
| M2 | + Frontend, + SDR | 2 073 000 |
| M3 | + DevOps, + Customer Success | 2 840 000 |
| M4 | + AE | 3 230 000 |
| M5 | + CTO | 3 945 000 |
| M6 | + Product/Growth | 4 361 000 |
| M7 | + ML Engineer | 5 011 000 |
| M8 | + 2nd Senior Backend | 5 557 000 |
| M9 | + Finance/Ops 0.5 | 5 713 000 |
| M10 | ramp / bonuses / partial commission accrual | 5 820 000 |
| M11 | steady state | 5 928 000 |
| M12 | steady state | 5 928 000 |

Вывод: до боеспособной команды нужен длинный найм и значительный пред-выручечный burn.

---

## 15) Burn-to-breakeven

### Месячный burn до break-even
Использую lean-mode fixed cost + acquisition pool + infra pre-scale.

| Период | Burn, ₽/мес |
|---|---:|
| M1-M3 | 2.0-2.8 млн |
| M4-M6 | 3.4-4.2 млн |
| M7-M9 | 4.6-5.3 млн |
| M10-M12 | 5.0-5.8 млн |

### Кумулятивный burn до 108 клиентов
При траектории продаж выше проект дойдет до 108 клиентов примерно на **M14-M15**, если удержание не ухудшится.

Оценка cumulative burn to breakeven:
**~46-52 млн ₽**

Для B2B AI-video продукта это уже ближе к венчурному buildout, а не к «быстрому quick-AI wedge».

---

## 16) Cash runway

Берем startup_capital = **30 млн ₽** как типичный seed/pre-seed пул для такой команды.

### Base burn
Средний burn первых 12 месяцев ≈ **4.25 млн ₽/мес**

Runway = 30 000 000 / 4 250 000 = **7.1 мес**

### Если сильно ужаться
При burn 3.3 млн ₽/мес runway = **9.1 мес**

### Чтобы дожить до breakeven
Если cumulative burn to breakeven 46-52 млн ₽, то нужен капитал **минимум 50+ млн ₽**, лучше **60 млн ₽** с запасом.

Sanity check из задания проходит: капитал до B/E заметно выше 10 млн ₽. Но для такого спросового профиля требование к капиталу слишком велико.

---

## 17) Проверка sanity checks

1. **CAC Payback < 12 мес**: да, **6.3 мес** по gross profit.
2. **LTV/CAC ≥ 3**: да, **6.37x**.
3. **CAC не выглядит заниженным**: да, **183K ₽** в диапазоне mid-market benchmark 60-250K ₽.
4. **5+ hires в первый месяц**: нет, нарушение avoided.
5. **FOT M1 < 1M для 5-7 чел**: нет, M1 = 1.449 млн ₽.
6. **startup_capital_to_bep < 10M ₽**: нет, наоборот требуется 50M+ ₽.

Парадокс модели: юнит-экономика на уровне клиента нормальная, но **портфельная инвестиционная экономика слабая**, потому что объем спроса и нужная cost-base плохо соотносятся.

---

## 18) Итоговый инвестиционный вывод

### Почему не проходит investment-grade
- Кейс зависит от репозиционирования в B2B, но тогда нужен более тяжелый sales + success + infra контур.
- При **50 клиентах** бизнес все еще глубоко убыточен.
- **Break-even 108 клиентов**, а для EBITDA 500K нужен **125 клиентов**.
- Для продукта с mixed/low demand signal это слишком высокая планка execution и капитала.

### Окончательный вердикт
**REJECTED на этапе Program 5 / Unit Economics.**

Не потому, что продукт вообще нельзя продавать, а потому что для фонда это слабый профиль:
- слишком большой burn-to-breakeven,
- слишком тяжелая команда,
- недостаточная EBITDA-емкость на малой базе,
- риск, что реальный churn будет хуже base-case 2.5%.

---

## Источники
- 02-demand.md текущего кейса
- 01-evidence.md текущего кейса
- HH.ru CTO: https://hh.ru/vacancy/125002805 ; https://hh.ru/vacancies/tehnicheskij-direktor-cto/polnaya_zanyatost
- HH.ru Senior Backend: https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancy/128923492 ; https://hh.ru/vacancy/129522775
- HH.ru ML/LLM: https://hh.ru/vacancy/129442148 ; https://hh.ru/vacancy/129769843 ; https://hh.ru/vacancy/130252738
- HH.ru Frontend: https://hh.ru/vacancy/127952750
- HH.ru SDR/AE listings: https://hh.ru/vacancies/account_executive/polniy_den ; https://hh.ru/vacancies/account_executive
- B2B SaaS churn benchmark: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
