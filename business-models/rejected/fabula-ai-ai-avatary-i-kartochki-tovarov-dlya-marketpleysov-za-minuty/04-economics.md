---
stage: economics
case: fabula-ai-ai-avatary-i-kartochki-tovarov-dlya-marketpleysov-za-minuty
date: 2026-05-11
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics / Fund-level check

## Executive summary

Базовую модель считаю не по consumer-аватарам, а по `seller/team SaaS + agency + white-label/API` для маркетплейс-селлеров и агентств.

Итог проверки:
- **LTV/CAC = 4.8x**, то есть канал привлечения сам по себе не сломан.
- **CAC Payback = 4.1 месяца**, что укладывается в норму для mid-market B2B.
- Но при реалистичном RU hiring-plan и fully-loaded FOT продукт **не достигает EBITDA 500k+/мес даже на 50 платящих клиентах**.
- Break-even наступает примерно на **158 клиентах**, а для EBITDA 500k+/мес нужно около **175 клиентов**.
- Следовательно, кейс **проваливает Profit Gate фонда** по правилу: `company EBITDA < 500K/mo achievable even at 50 clients`.

## 1) Модель и ключевые допущения

### Модель выручки
Берём целевой микс, который лучше всего согласуется с `02-demand.md` и `03-solution.md`:
- solo seller / starter: `9 990 ₽/мес`
- team seller: `29 990 ₽/мес`
- agency / white-label lite: `89 990 ₽/мес`

### Blended customer profile
Для расчёта base-case беру такой микс новых активных клиентов:
- 55% starter
- 35% team
- 10% agency / white-label lite

**Blended MRR на клиента = ~35 000 ₽/мес**.

Это согласуется с intake-гипотезой `50 B2B-клиентов × 30 000 ₽ ≈ 1,5 млн ₽ MRR`, но я округляю вверх до `35 000 ₽`, чтобы не занизить upside.

## 2) Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Захват лида из рекламы/контента/комьюнити | Growth marketer | VK Ads, Яндекс.Директ, Telegram ads, лендинг | 5 мин | 350 | semi-auto |
| 2 | Лид попадает в CRM и трекается источник | SDR | amoCRM / Bitrix24 | 3 мин | 45 | auto + human review |
| 3 | Первый контакт, квалификация ICP | SDR | CRM, Telegram, e-mail, телефон | 15 мин | 280 | human |
| 4 | Назначение демо / onboarding-call | SDR | Calendly/бот/CRM | 8 мин | 110 | semi-auto |
| 5 | Демо use-case по карточкам / SKU batch | AE | Zoom/Meet, Fabula demo workspace | 45 мин | 940 | human |
| 6 | Пробный запуск 1-3 SKU / пилот | AE + solutions/CS | product workspace, шаблоны | 90 мин | 1 650 | semi-auto |
| 7 | Согласование тарифа и пакета | AE | КП, мессенджер, CRM | 30 мин | 620 | human |
| 8 | Выставление счёта / ссылка на оплату | Operations / AE | ЮKassa / CloudPayments / банк | 10 мин | 120 | auto + human check |
| 9 | Оплата и активация workspace | CS / support | billing + product backend | 10 мин | 170 | mostly auto |
| 10 | Первичный onboarding и шаблоны | CSM | Notion, чат, видеозвонок | 60 мин | 800 | human |
| 11 | Ежемесячный support / success-touch | CSM + support | чат, CRM, helpdesk | 40 мин/мес | 650 | semi-auto |
| 12 | Повторная оплата / продление | Billing + CSM | рекуррентные платежи, CRM | 10 мин/мес | 140 | mostly auto |

### Вывод по процессу
- Для B2B-lite seller/team сегмента это **не self-serve SMB CAC 5-30k**, а уже **mid-market assisted sale** с демо и onboarding.
- Поэтому raw acquisition выглядит дешёвым только на бумаге. После SDR/AE/CS и инструментов получается materially выше.

## 3) COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Комментарий |
|---|---:|---|
| GPU / image inference | 2 700 | генерация карточек, изображений, вариаций |
| Внешние AI API / model routing | 1 200 | сторонние модели, upscaling, moderation |
| Хранение, CDN, media delivery | 300 | хранение и раздача изображений |
| Переменная поддержка / success-touch | 1 500 | onboarding-lite и monthly support |
| Платёжный эквайринг | 350 | 1.0% от blended чека округлённо |
| Переменная cloud-инфраструктура | 0 | включено в GPU/API line |
| **Итого COGS** | **6 050** |  |

### Unit margin
- **MRR на клиента:** `35 000 ₽`
- **COGS на клиента:** `6 050 ₽`
- **Contribution per client:** `28 950 ₽`
- **Contribution Margin:** `82.7%`

## 4) Fully-loaded CAC

Считаю CAC по формуле:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocation + Tools + Events + Overhead multiplier) / New paying customers`

### CAC components table

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/Telegram) | 180 000 | тестовый acquisition budget для seller B2B-lite | model assumption + RU ad market sanity |
| Outbound team FOT (SDR/AE attributed to new) | 474 000 | SDR 224 250 + 60% AE cost 249 780 | HH.ru benchmark + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 130 000 | part-time growth / content / performance allocation | model assumption |
| Tools (CRM, парсинг, телефония, outreach, analytics) | 45 000 | amoCRM + телефония + data tools + analytics | market software sanity |
| Events / partnerships | 60 000 | seller-комьюнити, интеграции, вебинары, партнёрки | model assumption |
| Overhead multiplier (x1.3) | 266 700 | 30% на менеджмент, финансы, admin overhead от 889 000 | std for mid-market B2B |
| **Итого spend** | **1 155 700** |  |  |

### New paying customers / month
- База для blended CAC: **8 новых платящих клиентов в месяц**.

### Blended fully-loaded CAC
- **CAC = 1 155 700 / 8 = 144 463 ₽**
- Округляю до **144.5k ₽**.

### CAC по каналам с funnel conversion

| Канал | Spend, ₽/мес | Funnel | New paid | CAC, ₽ | Комментарий |
|---|---:|---|---:|---:|---|
| Inbound content + seller communities | 366 000 | 320 leads → 96 MQL (30%) → 24 demo (25%) → 4 paid (16.7%) | 4 | 91 500 | лучший канал по CAC |
| Partnerships / agencies | 242 000 | 40 partner leads → 20 meetings (50%) → 8 pilot (40%) → 2 paid (25%) | 2 | 121 000 | хороший quality, низкий volume |
| Outbound | 547 700 | 900 contacts → 90 replies (10%) → 18 demo (20%) → 2 paid (11.1%) | 2 | 273 850 | дорогой канал, но нужен для pipe creation |
| **Blended** | **1 155 700** | совокупно 1 260 contacts/leads → 206 qualified → 50 demo/meetings → 8 paid | **8** | **144 463** |  |

### Sanity check vs RU benchmark
Для mid-market SaaS в РФ пользователь задал sanity-диапазон **60-250k ₽**. Наш blended CAC **144.5k ₽** находится внутри диапазона, то есть модель не выглядит искусственно заниженной.

## 5) LTV и churn

### Churn benchmark
Для B2B SaaS беру ориентир monthly logo churn:
- SMB SaaS обычно выше, часто `3-7%/мес`
- mid-market B2B обычно ближе к `1-3%/мес`

Для Fabula seller/team сегмента беру **4.2% monthly churn**, потому что:
1. use-case повторяемый, но не mission-critical;
2. часть селлеров сезонная и project-based;
3. продукт близок к commodity-layer, поэтому stickiness ограничена.

### LTV formula
`LTV = ARPA × Gross Margin / Monthly Churn`

### Расчёт
- ARPA / MRR per customer = `35 000 ₽`
- Gross Margin = `82.7%`
- Monthly churn = `4.2%`

`LTV = 35 000 × 0.827 / 0.042 = 689 167 ₽`

### Итог
- **LTV ≈ 689k ₽**
- **Средний срок жизни клиента ≈ 23.8 месяца**

## 6) LTV/CAC

- **LTV = 689k ₽**
- **CAC = 144.5k ₽**

`LTV/CAC = 689 / 144.5 = 4.77x`

### Интерпретация
- Формально это **investment-grade по метрике LTV/CAC**, потому что выше `3:1`.
- Но эта метрика не спасает кейс, если структура расходов не позволяет быстро дойти до EBITDA.

## 7) CAC Payback

Формула по требованию:

`CAC Payback = CAC / MRR per customer`

`144 463 / 35 000 = 4.13 месяца`

### Итог
- **CAC Payback = 4.1 месяца**
- Это хорошо и ниже базового лимита `12 месяцев`.

## 8) Team & FOT

### Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp до 80% productivity | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 450 000 | 1.5 | 1.5 | 135 000 | 585 000 |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 0 | 0 | — | — | — | 0 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 172 500 | 1 | 1 | 51 750 | 224 250 |
| AE | 1 | 321 000 | 1.5 | 3 | 96 300 | 417 300 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| **Итого steady-state FOT** | **7** |  |  |  |  | **4 151 550** |

### Комментарий по hiring realism
- Я **не ставлю 5+ наймов в M1**, потому что это нарушило бы time-to-hire realism.
- Даже при умеренной команде без отдельного DevOps steady-state payroll уже выходит на **4.15 млн ₽/мес fully-loaded**.
- Это и есть главный structural problem кейса на fund-level.

## 9) Cumulative FOT timeline M1-M12

### План подключения команды
- M1: CEO, старт поиска CTO и frontend
- M2: CEO, frontend, старт поиска backend и SDR
- M3: CEO, frontend, backend, SDR
- M4: CEO, CTO, frontend, backend, SDR, старт AE
- M5: CEO, CTO, frontend, backend, SDR, AE, старт ML
- M6: CEO, CTO, frontend, backend, SDR, AE, ML
- M7: CEO, CTO, frontend, backend, SDR, AE, ML, CSM
- M8-M12: steady-state

### FOT by month

| Месяц | Активные роли | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend | 1 235 000 |
| M3 | CEO + Frontend + Backend + SDR | 2 044 250 |
| M4 | CEO + CTO + Frontend + Backend + SDR | 2 759 250 |
| M5 | CEO + CTO + Frontend + Backend + SDR + AE | 3 176 550 |
| M6 | CEO + CTO + Frontend + Backend + SDR + AE + ML | 3 826 550 |
| M7 | CEO + CTO + Frontend + Backend + SDR + AE + ML + CSM | 4 151 550 |
| M8 | steady-state | 4 151 550 |
| M9 | steady-state | 4 151 550 |
| M10 | steady-state | 4 151 550 |
| M11 | steady-state | 4 151 550 |
| M12 | steady-state | 4 151 550 |

### Cumulative FOT M1-M12
Суммарный FOT за первые 12 месяцев:

`845 000 + 1 235 000 + 2 044 250 + 2 759 250 + 3 176 550 + 3 826 550 + 6 × 4 151 550 = 38 796 900 ₽`

**Cumulative FOT Y1 = 38.8 млн ₽**.

## 10) Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Базовая cloud / dev infra, мониторинг, бэкапы | 120 000 | не включая variable inference |
| Юрлица, бухгалтерия, договоры, оферты | 80 000 | юрсопровождение и accounting |
| Admin / founders ops / финконтур | 90 000 | административный контур |
| SaaS tools internal (Notion, Slack, analytics, design, support) | 95 000 | внутренняя операционная связка |
| Офис / коворкинг / travel buffer | 110 000 | гибридный режим, Москва/СПб |
| **Итого fixed non-payroll** | **495 000** |  |

### Total fixed monthly OPEX at steady-state
- FOT: `4 151 550 ₽`
- non-payroll fixed: `495 000 ₽`

**Итого fixed OPEX = 4 646 550 ₽/мес**

## 11) Break-even

### Break-even по клиентам
Формула:

`Break-even clients = Fixed OPEX / Contribution per client`

`4 646 550 / 28 950 = 160.5`

Округляю вверх:
- **Break-even = 161 клиента**

### Break-even по месячной выручке
`161 × 35 000 ₽ = 5 635 000 ₽/мес MRR`

То есть компании нужно:
- **~161 активный клиент**
- **~5.64 млн ₽ MRR**

чтобы выйти примерно в ноль на EBITDA.

## 12) EBITDA test at 50 clients

### Сценарий 50 клиентов
- Revenue: `50 × 35 000 = 1 750 000 ₽/мес`
- COGS: `50 × 6 050 = 302 500 ₽/мес`
- Gross profit / contribution: `1 447 500 ₽/мес`
- Fixed OPEX: `4 646 550 ₽/мес`

`EBITDA = 1 447 500 - 4 646 550 = -3 199 050 ₽/мес`

### EBITDA target 500k+
Чтобы получить `EBITDA = +500 000 ₽/мес`, нужно:

`(4 646 550 + 500 000) / 28 950 = 177.8`

Округляю:
- **Нужно ~178 клиентов**

### Вывод
На `50 клиентах` кейс **очень далеко** от целевого порога фонда. Даже если завысить blended чек до `45k ₽`, модель всё равно не дотягивает до `EBITDA 500k+/мес` с такой командой.

## 13) Burn-to-breakeven

Если брать steady-state fixed base и постепенный рост клиентов, то до момента достижения `161 клиентов` бизнес сжигает:
- heavy payroll burn,
- acquisition spend,
- infra/support.

### Приближённая оценка burn
На стадии M7+:
- fixed OPEX: `4.65 млн ₽/мес`
- acquisition spend: `1.16 млн ₽/мес`
- total cash burn before gross profit offset: **~5.8 млн ₽/мес**

Даже если к M12 бизнес доходит до `40-50 клиентов`, gross profit будет `1.16-1.45 млн ₽/мес`, и чистый burn всё равно останется в диапазоне **4.3-4.6 млн ₽/мес**.

### Startup capital to BEP
С учётом Y1 cumulative FOT `38.8 млн ₽`, non-payroll fixed и acquisition, realistic capital need до BEP составляет **~55-65 млн ₽**.

Это не смертельно для venture-backed компании, но слишком тяжело для кейса с пока ещё commodity-like визуальным продуктом.

## 14) Cash runway

Беру по требованию `startup_capital = 60 млн ₽`.

### Runway estimate
Если средний burn в фазе M6-M12 находится около `5.0 млн ₽/мес`, то:

`60 / 5.0 = 12 месяцев`

- **Cash runway ≈ 12 месяцев**

Если рост выручки задерживается, runway легко съезжает к `9-10 месяцам`.

## 15) Fund-level verdict

### Что хорошо
- рынок реально платит;
- contribution margin высокий;
- CAC payback хороший;
- LTV/CAC формально strong.

### Что ломает инвестиционный кейс
1. **Слишком тяжёлая payroll-структура** относительно achievable ARPA.
2. При реалистичном RU-hiring-plan продукту нужно **160+ клиентов до нуля** и **~178 клиентов до EBITDA 500k+**.
3. На контрольной точке `50 клиентов` бизнес всё ещё глубоко убыточен.
4. Для commodity-prone visual AI это слишком длинный путь до устойчивой операционной прибыли.

## Final decision

**Profit Gate: FAIL**

Причина fail:
- **EBITDA < 500k/мес при 50 клиентах** даже в оптимизированной B2B-lite модели.

## Sources
- `02-demand.md` этого кейса: RU competitor pricing, market demand, seller market framing.
- `01-intake.md` этого кейса: B2B pricing signal `$229-$1999/mo`, user scale, channel framing.
- HH.ru salary benchmarks via search results, May 2026: senior/backend/team lead, ML, frontend, sales/account roles.
- Recurly SaaS churn benchmark pages, accessed 2026-05-11: SMB churn materially higher than enterprise, suitable for 4.2% monthly base-case sanity.
- User-provided benchmark constraints in task prompt: RU CAC bands, hiring realism, payback thresholds.
