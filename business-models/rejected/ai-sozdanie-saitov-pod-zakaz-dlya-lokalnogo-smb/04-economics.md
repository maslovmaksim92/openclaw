---
case: ai-sozdanie-saitov-pod-zakaz-dlya-lokalnogo-smb
stage: unit-economics
updated_at: 2026-04-24T23:59:00+03:00
analyst: branch-models-lead
---

# 04-economics — Unit Economics

## Executive summary

**Вердикт этапа: FAIL.**

Кейс выглядит рабочим как маленький lifestyle / agency-enabled бизнес, но **не проходит инвестиционный фильтр фонда**. Даже в premium-конфигурации `site + SEO + Telegram + CRM + monthly optimization` модель остаётся слишком тяжёлой по fixed cost и acquisition.

Базовая модель:
- **MRR на клиента:** 30 000 ₽/мес
- **COGS:** 7 500 ₽/клиент/мес
- **Contribution Margin:** 75.0%
- **Blended fully-loaded CAC:** 195 000 ₽
- **Monthly churn benchmark:** 4.0%
- **LTV:** 562 500 ₽
- **LTV/CAC:** 2.88x
- **CAC Payback:** 6.5 мес
- **Break-even:** ~244 клиента или ~7.32 млн ₽ выручки/мес
- **EBITDA at 50 clients:** около **-4.27 млн ₽/мес**

**Итог:** кейс не investment grade. Причина не в отсутствии спроса, а в том, что delivery и GTM остаются слишком services-heavy при слишком низком ARPU.

---

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | локальный service SMB в РФ | стоматологии, beauty, home services, локальные медцентры, ремонт, авто-сервисы |
| Коммерческое предложение | managed website subscription | сайт + базовое SEO + формы + Telegram/WhatsApp + ежемесячные правки |
| Средний чек | **30 000 ₽/мес** | выше low-end рынка 4.9-20k ₽, но внутри заявленного в кейсе ARPU 25-35k ₽ |
| New paying customers / мес в steady-state | 4 | 2 outbound, 1 paid inbound, 1 partner/referral |
| Startup capital | **25 млн ₽** | проверка runway для раннего старта |
| Monthly logo churn | **4.0%** | консервативно для SMB-подписки с ARPA около $300-350 |
| Gross margin basis | выручка минус COGS delivery | sales & marketing вынесены отдельно |

**Почему беру 30 000 ₽, а не выше:** в `02-demand.md` premium bundled-offer проходит в коридоре 20-30k ₽/мес. Для инвестпроверки нельзя ставить 40-50k ₽ без внешнего подтверждения рынка, иначе модель искусственно «дорисовывается» до PASS.

---

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Генерация холодного и платного лида | SDR + marketer | Яндекс.Директ, VK Ads, Telegram outreach, amoCRM | 1-14 дней | 6 500 | Средняя |
| 2 | Первичный контакт и qualification | SDR | amoCRM, телефония, WhatsApp/Telegram, email | 20-30 мин | 900 | Средняя |
| 3 | Discovery call | AE / founder | Zoom/Meet, call notes AI, CRM | 45-60 мин | 2 000 | Средняя |
| 4 | Аудит текущего сайта / карточек / SEO | AE + CS | чек-лист, Serpstat/Яндекс, Notion | 1-2 ч | 1 500 | Низкая |
| 5 | Подготовка коммерческого предложения | AE + founder | шаблон КП, калькулятор пакета, PDF proposal | 1-3 ч | 1 800 | Средняя |
| 6 | Follow-up, согласование scope и цены | AE | CRM, мессенджеры, телефония | 3-10 дней | 2 300 | Низкая |
| 7 | Договор и счёт | founder + ops | ЭДО, банк-клиент, шаблон договора | 1 день | 700 | Высокая |
| 8 | Оплата первого месяца / setup-fee | client + ops | банк-клиент, CRM, таблица активации | 1 день | 300 | Высокая |
| 9 | Onboarding: бриф, домен, хостинг, доступы, CRM/forms | CS + PM + no-code builder specialist | Tilda/WordPress/Hostinger, Figma, CRM, чат | 3-5 раб. дней | 4 800 | Средняя |
| 10 | Сборка и публикация сайта | builder specialist + designer/QA | AI-builder, CMS, Figma, image AI, analytics | 2-4 дня | 5 500 | Средняя |
| 11 | Ежемесячное сопровождение: правки, SEO, контент, формы | CS + SEO/content ops | CMS, Яндекс Метрика, GSC/Я.Вебмастер, чат | 2-4 ч/мес | 4 300 / мес | Средняя |
| 12 | Продление, upsell, повторный платёж | CS + founder/AE | CRM, billing, шаблон отчёта | 30-60 мин/мес | 1 100 / мес | Средняя |

**Вывод:** процесс лучше обычной веб-студии по скорости запуска, но он всё ещё сервисный. Автоматизация ускоряет продакшн, но не убирает человеческие касания в продаже, брифинге, правках и retention.

---

## 3. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| AI-builder / CMS / hosting / domain allocation | 1 500 | Tilda/Hostinger/WordPress stack + домен/SSL |
| Builder specialist / контент-правки | 1 800 | ~0.01-0.015 FTE при стандартизированном шаблонном delivery |
| SEO / контент ops allocation | 1 400 | локальное SEO, базовые тексты, метатеги, indexing hygiene |
| Customer Success / support allocation | 1 200 | 1-2 обращения, мелкие правки, monthly report |
| Designer / QA allocation | 900 | шаблонная визуальная полировка и контроль качества |
| Формы / CRM / виджеты / интеграции | 400 | лид-формы, мессенджеры, квизы, call-tracking light |
| Платёжные потери / багфиксы / резерв ручных исключений | 300 | мелкие ручные доработки, возвраты, доп. доменные работы |
| **Итого COGS** | **7 500** |  |

### Выручка и маржа на 1 клиента

| Показатель | Значение |
|---|---:|
| MRR на клиента | **30 000 ₽** |
| COGS | **7 500 ₽** |
| Contribution profit | **22 500 ₽** |
| Contribution Margin | **75.0%** |

COGS для такого сервиса выглядит хорошим, но проблема ниже по P&L: на scale компанию душат acquisition и core-team burn.

---

## 4. CAC по каналам и воронка

### 4.1 CAC по каналам

| Канал | Лиды / мес | Meetings / мес | SQL / мес | Proposal / мес | New paying / мес | Месячные затраты, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound | 900 | 45 | 18 | 8 | 2 | 500 000 | **250 000** |
| Paid inbound (Яндекс / VK / search) | 160 | 24 | 10 | 4 | 1 | 190 000 | **190 000** |
| Partnerships / referrals | 20 | 8 | 5 | 3 | 1 | 90 000 | **90 000** |
| **Blended** | **1 080** | **77** | **33** | **15** | **4** | **780 000** | **195 000** |

### 4.2 Funnel conversion

| Funnel stage | Outbound | Paid inbound | Partnerships |
|---|---:|---:|---:|
| Lead → meeting | 5.0% | 15.0% | 40.0% |
| Meeting → SQL | 40.0% | 41.7% | 62.5% |
| SQL → proposal | 44.4% | 40.0% | 60.0% |
| Proposal → win | 25.0% | 25.0% | 33.3% |
| Lead → win | 0.22% | 0.63% | 5.0% |

### 4.3 Fully-loaded CAC, обязательный расчёт

Сегмент здесь не self-serve SaaS, а **services-heavy SMB B2B motion**. Поэтому беру не «рекламный CAC», а fully-loaded CAC, и для sanity использую минимально допустимый для SMB множитель **x1.3**.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 120 000 | тестовый медиабюджет на локальные B2B verticals | internal model + `02-demand.md` |
| Outbound team FOT (SDR + 0.5 AE attributed to new) | 377 000 | SDR 195 000 + 50% AE 182 000 | HH.ru benchmark snapshots, 2026-04-24 |
| Marketing team FOT (partial allocation) | 70 000 | ~25% founder/ops time на acquisition | internal allocation |
| Tools (CRM, телефония, builder stack, рассылки) | 18 000 | amoCRM + телефония + enrichment + sequencing | vendor stack estimate |
| Events / partnerships | 15 000 | локальные партнёры, referral fee, офлайн-активации | internal model |
| Raw CAC spend subtotal | **600 000** | сумма строк выше |  |
| Overhead multiplier (x1.3) | **180 000** | 600 000 × 30% | standard overhead for SMB B2B |
| **Total fully-loaded acquisition spend** | **780 000** |  |  |
| **New paying customers / мес** | **4** | blended model |  |
| **Fully-loaded CAC** | **195 000 ₽** | 780 000 / 4 |  |

### 4.4 Sanity check по CAC

- Для **SMB self-serve** user-guideline даёт ориентир **5-30k ₽**, но этот кейс туда не попадает, потому что здесь есть human sales, onboarding и service layer.
- Для **mid-market SaaS** ориентир **60-250k ₽**. Наш blended CAC **195k ₽** вписывается в коридор, но уже ближе к верхней зоне.
- **Red flag:** если считать только ads spend, CAC казался бы около 30-50k ₽, что нереалистично. Fully-loaded расчёт возвращает модель к реальности.

---

## 5. LTV и churn benchmark

### 5.1 Churn benchmark

Я беру **4.0% monthly logo churn**.

Почему это разумно:
1. **ChartMogul Help Center** указывает, что для SaaS customer churn «typically 3–7% per month», а также что churn у lower-ARPA бизнесов выше. Для бизнеса с ARPA **$250-500** ChartMogul показывает median monthly customer churn около **3.0%**, top quartile **1.9%**, bottom quartile **4.7%**. Наш чек **30 000 ₽/мес** при курсовом порядке величин примерно попадает в этот диапазон. Значит **4.0%** для локального SMB service subscription выглядит консервативно, но не экстремально. Источники: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate и https://chartmogul.com/saas-metrics/revenue-churn/
2. У этого кейса churn должен быть **хуже классического B2B SaaS**, потому что продуктовая lock-in ниже: сайт для части микробизнеса воспринимается как commodity, а не mission-critical workflow.
3. В `02-demand.md` уже отмечен риск retention у микробизнеса. Значит ставить 2% monthly churn было бы слишком оптимистично.

### 5.2 LTV calculation

Формула:

`LTV = ARPU × Contribution Margin % / Monthly churn`

`LTV = 30 000 × 75.0% / 4.0% = 562 500 ₽`

| Показатель | Значение |
|---|---:|
| ARPU / MRR | 30 000 ₽ |
| Contribution Margin % | 75.0% |
| Monthly churn | 4.0% |
| **LTV** | **562 500 ₽** |

---

## 6. LTV/CAC, CAC payback, contribution margin

| Метрика | Формула | Значение | Verdict |
|---|---|---:|---|
| LTV/CAC | 562 500 / 195 000 | **2.88x** | FAIL for investment grade |
| CAC Payback | 195 000 / 30 000 | **6.5 мес** | PASS baseline |
| Contribution Margin % | (30 000 - 7 500) / 30 000 | **75.0%** | PASS |

### Sanity check against investment grade

- Требование investable: **LTV/CAC ≥ 3.0**. Здесь только **2.88x**.
- Требование payback: **<12 мес** для базового B2B. Здесь **6.5 мес**.
- Это означает неприятную вещь: **юнит на клиенте сам по себе не ужасный, но компания не становится фондовым активом**, потому что blended acquisition слишком дорогой относительно lifetime gross profit.

---

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Функция | Кол-во | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO / Founder | продажи, стратегия, ключевые сделки | 1 | 600 000 | 180 000 | **780 000** |
| CTO / Tech Lead | стек, шаблоны, интеграции, automation | 1 | 500 000 | 150 000 | **650 000** |
| Senior Backend | CMS/integration automation, формы, billing | 2 | 420 000 | 126 000 | **1 092 000** |
| DevOps | хостинг, CI/CD, домены, monitoring | 1 | 320 000 | 96 000 | **416 000** |
| Frontend | шаблоны, мелкие доработки, web UX | 1 | 280 000 | 84 000 | **364 000** |
| SDR (outbound) | лидогенерация и первичный контакт | 1 | 150 000 | 45 000 | **195 000** |
| AE / Founder-led sales | discovery, scope, close | 1 | 280 000 | 84 000 | **364 000** |
| Customer Success / PM | onboarding, retention, monthly ops | 1 | 220 000 | 66 000 | **286 000** |
| **Итого** |  | **9** |  |  | **4 147 000 ₽/мес** |

### 7.2 Обязательная таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 500 000 | 2.5 | 2.0 | 150 000 | 650 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 / чел |
| DevOps | 1 | 320 000 | 1.5 | 1.0 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1.0 | 1.0 | 84 000 | 364 000 |
| SDR (outbound) | 1 | 150 000 | 0.75 | 1.0 | 45 000 | 195 000 |
| AE | 1 | 280 000 | 1.5 | 2.5 | 84 000 | 364 000 |
| Customer Success | 1 | 220 000 | 1.0 | 1.0 | 66 000 | 286 000 |

**Salary benchmark note:** использую midpoint-like gross в коридоре вакансий HH.ru по Москве/удалёнке на 2026-04-24. В выдаче HH видны примеры: frontend до 300k ₽ и 190-260k ₽; backend/lead backend 220-250k ₽ и senior/fintech 400-600k ₽; SDR/B2B SaaS и related sales роли около 100-150k ₽ и выше; account executive / KAM related роли 172.5-320k ₽. Для инвестмодели беру не нижнюю границу, а реалистичный midpoint.

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | **780 000** |
| M2 | CEO | **780 000** |
| M3 | + Frontend | **1 144 000** |
| M4 | + Backend #1 | **1 690 000** |
| M5 | + CTO + SDR | **2 535 000** |
| M6 | + AE | **2 899 000** |
| M7 | + Backend #2 + DevOps | **3 861 000** |
| M8 | + Customer Success | **4 147 000** |
| M9 | Полная команда | **4 147 000** |
| M10 | Полная команда | **4 147 000** |
| M11 | Полная команда | **4 147 000** |
| M12 | Полная команда | **4 147 000** |

**Проверки realism:**
- В первый месяц не нанимается 5+ человек, значит time-to-hire не нарушен.
- Даже без офиса FOT быстро уходит выше 4 млн ₽/мес, что и ломает тезис «маленькая AI-команда быстро дойдёт до прибыли».

### 7.4 Burn-to-breakeven

При фиксированной базе ниже и growth до 4 новых клиентов в месяц компания начинает жить в режиме burn значительно раньше, чем достигает нужного клиентского объёма.

- Contribution profit на 1 клиента: **22 500 ₽/мес**
- Fixed cost база на полном штате: **5 498 000 ₽/мес**
- Для EBITDA > 0 нужно ~**244 клиента**
- Для EBITDA > 500k/мес нужно уже около **267 клиентов**

**Вывод:** до break-even компания успевает сжечь слишком много капитала. В base-case burn-to-breakeven выходит около **95-105 млн ₽**, если реально строить команду и GTM, а не работать как фаундерская микростудия.

### 7.5 Cash runway

При `startup_capital = 25 млн ₽`:
- burn в ранние месяцы: **~1.1-2.9 млн ₽/мес**
- burn после выхода на полный штат, но до масштаба: **~4.8-5.1 млн ₽/мес**
- ориентировочный runway: **6-8 месяцев**

Для B2B subscription service это слишком мало. До break-even такой капитал не дотягивает.

---

## 8. Fixed costs breakdown

| Компонент fixed costs | ₽/мес |
|---|---:|
| Core team FOT | **4 147 000** |
| Shared cloud / hosting core / monitoring / backups | 120 000 |
| CRM / телефония / no-code / internal tools | 36 000 |
| Legal / accounting / admin | 75 000 |
| Paid acquisition budget | 120 000 |
| Events / partnerships / commissions | 15 000 |
| Misc reserve | 985 000 |
| **Итого fixed costs / мес** | **5 498 000 ₽** |

`Misc reserve` здесь нужен не как «подушка на всякий случай», а как реальный буфер на founder travel, подрядчиков, правки сверх шаблона, налоги вне ФОТ, дизайн-оверфлоу и неидеальную загрузку команды. Без него модель выглядела бы слишком «гладкой» и нереалистичной.

---

## 9. Break-even: по клиентам и по месяцу

### 9.1 Break-even по числу клиентов

Формула:

`Break-even clients = Fixed costs / Contribution profit per client`

`= 5 498 000 / 22 500 = 244.4`

**Break-even = 245 клиентов.**

### 9.2 Break-even по месячной выручке

`Break-even revenue = 245 × 30 000 = 7 350 000 ₽ / мес`

### 9.3 Break-even по времени

Если после ramp компания стабильно привлекает **4 новых платящих клиента в месяц**, а monthly churn держится на **4%**, то к M12 портфель будет примерно **25-27 активных клиентов**, к M24 около **90-100**, а break-even сдвигается далеко за горизонт раннего фонда, примерно в зону **M30+** даже без серьёзных ошибок исполнения.

---

## 10. Проверка Profit Gate

### EBITDA при 50 клиентах

| Показатель | Значение |
|---|---:|
| Клиентов | 50 |
| Выручка | 1 500 000 ₽/мес |
| COGS | 375 000 ₽/мес |
| Contribution profit | 1 125 000 ₽/мес |
| Fixed costs | 5 498 000 ₽/мес |
| **EBITDA** | **-4 373 000 ₽/мес** |

Даже если урезать reserve и сделать более агрессивную экономию, компания **всё равно не приближается к +500k EBITDA при 50 клиентах**.

### Profit Gate verdict

**FAIL.**

Причины:
1. **EBITDA > 500k/мес при 50 клиентах недостижима.**
2. **LTV/CAC = 2.88x**, то есть ниже инвестиционного порога **3:1**.
3. Модель требует десятков миллионов рублей до масштаба, но не показывает software-like operating leverage.
4. Если упростить команду сильнее, кейс превращается в фаундерскую студию, а не в фондовый актив.

---

## 11. Финальный вывод по unit economics

Кейс можно запускать как **малую AI-enabled service business**, но **не как инвестиционно-привлекательный venture case**.

Что ломает модель:
- низкий чек относительно объёма человеческих касаний,
- дорогой fully-loaded CAC,
- SMB churn выше, чем хотелось бы,
- break-even наступает слишком поздно и слишком далеко по числу клиентов,
- при 50 клиентах нет даже близкого выхода к EBITDA 500k/мес.

**Итог этапа P5: REJECT.**

---

## Sources

### Использованные материалы кейса
- `00-brief.md`
- `01-evidence.md`
- `02-demand.md`

### Внешние источники для benchmark / sanity
- ChartMogul Help Center, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- ChartMogul, Revenue churn benchmarks by ARPA range: https://chartmogul.com/saas-metrics/revenue-churn/
- HH.ru, frontend developer vacancies Moscow: https://hh.ru/vacancies/frontend-developer
- HH.ru, DevOps vacancies Moscow: https://hh.ru/vacancies/devops
- HH.ru, account executive vacancies Moscow: https://hh.ru/vacancies/account_executive
- HH.ru, SDR search / sales-related vacancies Moscow: https://hh.ru/search/vacancy?text=SDR

### Where inference is used
- Распределение FOT по ролям, клиентская воронка, blended channel mix, reserve и burn-to-breakeven являются **analyst inference** на базе `02-demand.md`, цен конкурентов и рыночных salary/churn benchmarks.
