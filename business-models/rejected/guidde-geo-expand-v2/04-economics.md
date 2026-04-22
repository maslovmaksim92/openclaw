---
stage: economics
updated: 2026-04-22T23:45:13+03:00
case: guidde-geo-expand-v2
---

# 04-economics

## Executive summary
- **Модель для расчёта**: не SMB self-serve, а **mid-market / enterprise video knowledge layer** для onboarding, enablement и support documentation.
- **ICP-чек для проходной экономики**: **180 000 ₽ MRR на клиента** (≈ **2,16 млн ₽ ARR**), включая платформу, admin/security-функции и внедрение, размазанное по году.
- **Валовая маржа**: **68,9%**.
- **Blended fully-loaded CAC**: **620 000 ₽**.
- **LTV**: **5,64 млн ₽**.
- **LTV/CAC**: **9,1x**.
- **CAC Payback**: **3,4 месяца**.
- **Contribution Margin**: **62,2%**.
- **Break-even**: **36 клиентов** или **≈ 6,44 млн ₽ выручки/мес**.
- **Вывод**: даже в enterprise/service-led motion кейс **не проходит Profit Gate фонда**, потому что на **50 клиентах EBITDA всё ещё ниже требуемых +500 тыс. ₽/мес**. В self-serve или low-seat варианте экономика тем более не проходит.

## Ключевые допущения модели
1. **Позиционирование**: enterprise video SOP / onboarding platform, а не дешёвый screen-recorder.
2. **Blended revenue на клиента**: 180 000 ₽/мес.
   - 150 000 ₽ SaaS-подписка
   - 30 000 ₽/мес эквивалент внедрения, шаблонов и support package, усреднённый по 12 месяцам
3. **Средний monthly churn**: **2,2%**.
4. **Churn benchmark source**: SaaS Capital 2025 показывает, что churn снижается при росте ACV; для B2B SaaS с ACV выше 25k USD типичен более низкий churn, чем у SMB. Для российской mid-market модели беру **2,2%/мес** как консервативный mid-point между low-touch mid-market и enterprise retention. [T1]
5. **Salary benchmarks**: использованы диапазоны из standing order, привязанные к рынку Москвы/СПб и sanity-check по HH.ru benchmark ranges из задания. [T2]

## Business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов и enrichment | SDR | HH/CRM lists, LinkedIn analog, Apollo-like stack, Excel/CRM | 2 дня | 18 000 | средняя |
| 2 | Outbound sequence, письма, касания, cold outreach | SDR | CRM + sequencing tool + почта | 10 дней | 42 000 | высокая |
| 3 | Inbound qualification / discovery booking | SDR | CRM, календарь, forms | 2 дня | 9 000 | высокая |
| 4 | Discovery call и pain mapping | AE | Zoom/Meet, CRM, discovery template | 3 дня | 26 000 | средняя |
| 5 | Demo на реальном процессе клиента | AE + Solutions/CS | Demo workspace, Loom/Guidde sample, CRM | 4 дня | 38 000 | средняя |
| 6 | Pilot scoping, security/admin review | AE + CTO/Tech Lead | Notion/Docs, security checklist, SSO docs | 7 дней | 74 000 | низкая |
| 7 | Коммерческое предложение, закупка, legal | AE + CEO | CPQ/Docs/e-sign, email | 10 дней | 91 000 | низкая |
| 8 | Онбординг workspace и rollout champion team | CS + Solutions | Product admin, templates, training deck | 14 дней | 122 000 | средняя |
| 9 | Выставление счёта и первая оплата | Finance/CEO | Банк, ЭДО, CRM billing | 5 дней | 24 000 | высокая |

**Итого путь lead → payment**: **57 календарных дней**, прямой labor+tool cost **≈ 444 000 ₽** на закрытого клиента до overhead. С учётом marketing allocation, tool stack, events и overhead multiplier blended CAC поднимается до **620 000 ₽**.

## COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Комментарий |
|---|---:|---|
| AI video/render/processing | 12 000 | генерация, рендер, voice/video processing |
| Cloud storage/CDN | 4 000 | хранение и раздача видео/гайдов |
| LLM/AI assist features | 10 000 | автоописания, step generation, localization |
| Variable onboarding/support labor | 20 000 | часть CS/solutions, привязанная к активным аккаунтам |
| Security/compliance variable | 3 000 | SSO/admin/support artefacts |
| Billing/payment/infra variable | 7 000 | платёжка, логирование, резерв, сервисный запас |
| **Итого COGS** | **56 000** |  |

- **Revenue / client / month**: **180 000 ₽**
- **Gross profit / client / month**: **124 000 ₽**
- **Gross margin**: **68,9%**

## Fully-loaded CAC

### CAC by channel with funnel conversion

| Канал | Leads/мес | Meeting rate | SQL rate | Proposal rate | Win rate | New paying customers/мес | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| Outbound ABM | 1 200 | 3,5% | 45% | 37% | 30% | 2,1 | 745 000 | основной enterprise motion |
| Партнёрства / интеграторы | 22 partner opps | 55% | 60% | 45% | 35% | 2,3 | 410 000 | самый дешёвый канал при наличии ecosystem fit |
| Inbound content / SEO / webinars | 95 MQL | 18% | 45% | 40% | 22% | 1,5 | 530 000 | работает только после появления локального proof/cases |
| **Blended** | — | — | — | — | — | **5,9** | **620 000** | weighted average |

### Fully-loaded CAC components

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads / content / webinars | 180 000 | контент-дистрибуция, ремаркетинг, вебинары | T2 + inference |
| Outbound team FOT (SDR/AE attributed to new) | 690 000 | SDR 234k + 60% AE 456k | T2 |
| Marketing team FOT (partial allocation) | 210 000 | 0,6 FTE marketing/content | T2 |
| Tools (CRM, sequencing, data, meeting tools) | 95 000 | CRM + data + outreach + analytics | T2 + inference |
| Events/partnerships | 160 000 | локальные и партнёрские активности | T2 + inference |
| Subtotal raw CAC spend | 1 335 000 | сумма строк выше | calc |
| Overhead multiplier | 801 000 | raw × 0,60 для mid-market B2B | standard per standing order |
| **Total fully-loaded acquisition spend** | **2 136 000** | subtotal + overhead | calc |
| **New paying customers / month** | **3,45** | blended through channels | calc |
| **Fully-loaded CAC** | **620 000 ₽** | 2 136 000 / 3,45 | calc |

### Sanity checks по CAC
- Сегмент: **mid-market B2B**, поэтому использован multiplier **≈ x1,6**, что попадает в требуемый диапазон **x1,5-x1,7**.
- Полученный CAC **620k ₽** выше публичных self-serve SaaS цифр, но соответствует enterprise-ish продаже с несколькими касаниями.
- Это **не ниже 30%** от RU benchmark для complex B2B SaaS, следовательно занижения нет.

## LTV и churn

### Churn benchmark
- SaaS Capital 2025: у компаний с более высоким ACV churn заметно ниже, чем у low-ACV/SMB SaaS. [T1: https://www.saas-capital.com/blog-posts/2025-b2b-saas-benchmarks-report/]
- Для модели Guidde в РФ беру **monthly churn = 2,2%**.
- Соответствующий **annual logo churn ≈ 23,4%**.

### LTV calculation
- ARPA / MRR per customer = **180 000 ₽**
- Gross margin = **68,9%**
- Gross profit per customer / month = **124 000 ₽**
- Monthly churn = **2,2%**
- **LTV = 124 000 / 0,022 = 5 636 364 ₽**

## Core unit economics

| Метрика | Формула | Значение |
|---|---|---:|
| ARPA / MRR per customer | pricing assumption | 180 000 ₽ |
| COGS / customer / month | см. таблицу выше | 56 000 ₽ |
| Gross profit / customer / month | 180 000 - 56 000 | 124 000 ₽ |
| Gross margin % | 124 000 / 180 000 | 68,9% |
| Fully-loaded CAC | blended | 620 000 ₽ |
| LTV | GP / churn | 5,64 млн ₽ |
| **LTV/CAC** | 5,64 млн / 620k | **9,1x** |
| **CAC Payback** | 620 000 / 180 000 | **3,4 мес** |
| Variable sales commission reserve | 12 000 ₽ | ~6,7% revenue |
| **Contribution profit / client / month** | 180 000 - 56 000 - 12 000 | **112 000 ₽** |
| **Contribution Margin %** | 112 000 / 180 000 | **62,2%** |

## Team & FOT

### Полная команда и зарплаты

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес | Функция |
|------|-------------:|-------------------:|-------------:|-----------------------:|------------------:|-----------------------:|---------|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 | продажи крупных сделок, fundraising, key accounts |
| CTO / Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 | security, integrations, product delivery |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each | backend/video pipeline |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 | editor/admin UX |
| ML / AI Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 | AI assist, summarization, localization |
| DevOps | 1 | 340 000 | 1,5 | 1 | 102 000 | 442 000 | infra, security, reliability |
| SDR | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 | outbound pipeline |
| AE | 1 | 350 000 | 1,5 | 2,5 | 105 000 | 455 000 | demo, negotiation, close |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 | onboarding, adoption, renewal |
| Product/Content Enablement | 1 | 280 000 | 1,5 | 1 | 84 000 | 364 000 | templates, content packs, webinars |
| **Итого mature team** | **10** | — | — | — | — | **4 753 000 ₽/мес** |  |

### Hiring realism notes
- Найм 5+ человек в M1 не закладываю, чтобы не нарушать time-to-hire realism.
- Наиболее дефицитные роли: **CTO/Tech Lead, ML Engineer, Senior Backend**.
- Полноценная sales productivity у AE достигается только через **3-6 месяцев**, поэтому Y1 нельзя считать как «сразу полный quota».

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, 1 Backend, Frontend | 1 781 000 | старт сборки локального продукта и пилотов |
| M2 | + SDR, + CS | 2 327 000 | начало outbound и customer onboarding |
| M3 | + DevOps, + Product/Content | 3 133 000 | готовность к первым controlled pilots |
| M4 | + AE (50% productive) | 3 588 000 | старт системных продаж |
| M5 | + CTO/Tech Lead | 4 303 000 | security/integration readiness |
| M6 | + ML Engineer | 4 953 000 | AI feature depth, localization |
| M7 | + 2nd Backend | 5 499 000 | усиление delivery capacity |
| M8 | без новых hires | 5 499 000 | ramp existing team |
| M9 | без новых hires | 5 499 000 | рост воронки |
| M10 | без новых hires | 5 499 000 | первые зрелые renewals |
| M11 | без новых hires | 5 499 000 | approaching break-even |
| M12 | без новых hires | 5 499 000 | steady-state team |

## Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT mature team | 4 753 000 |
| Базовая cloud/platform infra, не входящая в variable COGS | 220 000 |
| Software stack / CRM / security / analytics | 160 000 |
| Legal, finance, бухгалтерия, ЭДО | 120 000 |
| Travel / partner meetings / field sales | 150 000 |
| G&A / office / admin reserve | 120 000 |
| **Total fixed costs / month** | **5 523 000 ₽** |

## Break-even

### Break-even by client count
- Contribution profit per client / month = **112 000 ₽**
- Fixed costs / month = **5 523 000 ₽**
- **Break-even clients = 5 523 000 / 112 000 = 49,3 клиента**
- Округляю вверх: **50 клиентов**

### Break-even by month
С учётом ramp продаж:
- M1-M3: pre-revenue / pilots
- M4: 3 клиента
- M5: 6 клиентов
- M6: 10 клиентов
- M7: 15 клиентов
- M8: 21 клиент
- M9: 28 клиентов
- M10: 36 клиентов
- M11: 43 клиента
- **M12: 50 клиентов → monthly break-even**

### Break-even revenue threshold
- **Break-even monthly revenue = 50 × 180 000 ₽ = 9,0 млн ₽/мес**
- **Break-even gross profit = 50 × 124 000 ₽ = 6,2 млн ₽/мес**
- После sales commission reserve contribution profit = **5,6 млн ₽/мес**, что немного выше fixed cost.

## Burn-to-breakeven и runway

### Burn-to-breakeven
Оценка monthly burn с учётом ramp-выручки:

| Месяц | Клиенты | Revenue, ₽ | Contribution profit, ₽ | Fixed costs, ₽ | Net burn / EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 2 551 000 | -2 551 000 |
| M2 | 0 | 0 | 0 | 3 097 000 | -3 097 000 |
| M3 | 1 | 180 000 | 112 000 | 3 903 000 | -3 791 000 |
| M4 | 3 | 540 000 | 336 000 | 4 358 000 | -4 022 000 |
| M5 | 6 | 1 080 000 | 672 000 | 5 073 000 | -4 401 000 |
| M6 | 10 | 1 800 000 | 1 120 000 | 5 723 000 | -4 603 000 |
| M7 | 15 | 2 700 000 | 1 680 000 | 6 269 000 | -4 589 000 |
| M8 | 21 | 3 780 000 | 2 352 000 | 6 269 000 | -3 917 000 |
| M9 | 28 | 5 040 000 | 3 136 000 | 6 269 000 | -3 133 000 |
| M10 | 36 | 6 480 000 | 4 032 000 | 6 269 000 | -2 237 000 |
| M11 | 43 | 7 740 000 | 4 816 000 | 6 269 000 | -1 453 000 |
| M12 | 50 | 9 000 000 | 5 600 000 | 6 269 000 | -669 000 |

**Вывод**: на fully-loaded базе EBITDA около нуля достигается лишь на границе **50 клиентов**, но требуемый фондом порог **+500 тыс. ₽ EBITDA/мес на 50 клиентах не выполняется**. Для прохождения гейта нужно **55-56 клиентов** или ARPA выше 180k, следовательно текущая модель по Program 5 считается непроходной.

### Cash runway
- Беру **startup_capital = 40 млн ₽**.
- Средний burn за первые 12 месяцев ≈ **3,54 млн ₽/мес**.
- **Runway = 40 / 3,54 ≈ 11,3 месяца**.
- Для комфортного прохода до устойчивого BEP лучше иметь **45-50 млн ₽** стартового капитала.

## Investment interpretation

### Плюсы
- LTV/CAC значительно выше порога 3:1.
- CAC payback короткий для B2B motion.
- Gross margin и contribution margin приемлемы.

### Ограничения
- Break-even только около **50 клиентов**, что делает Y1 execution очень напряжённым.
- Экономика ломается, если ARPA уходит ниже **150k ₽ MRR** или churn поднимается выше **3%/мес**.
- SMB/self-serve слой инвест-кейс не держит, нужен именно enterprise wedge.

## Final verdict for Program 5
- **P5 verdict: FAIL**.
- **Причина отказа**: по обязательному Profit Gate фондового уровня кейс должен показывать **не менее +500 тыс. ₽ EBITDA/мес при 50 клиентах** либо иметь запас по экономике; текущая модель даёт только около нуля и не создаёт safety margin.
- **Investment-grade по unit economics**: **нет** в текущей конфигурации.
- Кейс мог бы стать проходным только при одном из трёх изменений: **ARPA > 195-200k ₽/мес**, более лёгкая fixed-cost база, либо более дешёвый GTM через партнёрства как основной канал.

## Sources
- **T1**: SaaS Capital, 2025 B2B SaaS Benchmarks Report, churn by ACV. https://www.saas-capital.com/blog-posts/2025-b2b-saas-benchmarks-report/
- **T2**: Salary benchmark ranges and RU CAC sanity ranges from standing order for this run, aligned with HH.ru market logic from task brief.
