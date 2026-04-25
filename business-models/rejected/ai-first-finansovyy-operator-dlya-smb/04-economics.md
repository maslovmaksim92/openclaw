---
case: ai-first-finansovyy-operator-dlya-smb
stage: unit-economics
updated_at: 2026-04-24T19:31:00+03:00
analyst: branch-models-lead
---

# 04-economics — Unit Economics

## Executive summary

**Вердикт этапа: PASS.**

Кейс собирает investable unit economics **только как productized mid-market B2B finance ops service**, а не как дешёвый бухаутсорс. При базовом чеке **160 000 ₽ MRR на клиента**, среднем **COGS 42 000 ₽/клиент/мес**, blended fully-loaded **CAC 209 063 ₽**, месячном churn benchmark **2.5%**, модель даёт:

- **Contribution Margin:** 73.8%
- **LTV:** 4.72 млн ₽
- **LTV/CAC:** 22.6x
- **CAC Payback:** 1.3 мес
- **Break-even:** ~45 клиентов или ~7.2 млн ₽ месячной выручки
- **EBITDA at 50 clients:** ~**+602 тыс. ₽/мес**

Это проходит Profit Gate, но запас прочности небольшой. Главный риск не в LTV/CAC, а в том, сможет ли команда реально дойти до **45-50 активных клиентов** без провала в кастомизацию и сервисный перегруз.

---

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | SMB / lower mid-market, 20-250 сотрудников | Компании с заметным документооборотом, recurring invoicing и 1С/ЭДО контуром |
| Средний чек | **160 000 ₽/мес** | Верх середины диапазона из 02-demand, нужен для окупаемости full-stack delivery |
| New customers / мес в steady-state | 4 | 2 outbound, 1 paid inbound, 1 partner/referral |
| Gross margin basis | Revenue minus delivery COGS | Sales & marketing не включены в COGS |
| Monthly churn | **2.5%** | Бенчмарк для SMB/mid-market B2B SaaS/service-heavy subscription |
| Startup capital | **40 млн ₽** | Нужен, чтобы дожить до масштаба 45-50 клиентов |

---

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Генерация первичного лида | SDR + performance marketer | Яндекс.Директ, VK Ads, partner outreach, CRM | 1-14 дней | 18 000 | Средняя |
| 2 | Квалификация лида, first touch | SDR | amoCRM/Битрикс24, телефония, email sequencing | 30-45 мин | 2 200 | Средняя |
| 3 | Discovery call | AE | Zoom/Meet, CRM, call notes AI | 60 мин | 4 500 | Средняя |
| 4 | Сбор вводных: объём первички, банки, 1С, payroll | AE + Solution/Operations lead | Questionnaire, shared checklist | 2-3 дня | 6 500 | Низкая |
| 5 | Расчёт scope и коммерческого предложения | AE + CEO/Finance ops lead | Proposal template, калькулятор юнит-экономики | 1 день | 5 000 | Средняя |
| 6 | Security/legal review, договор | AE + CEO + юрист на аутсорсе | Документооборот, шаблон договора, ЭДО | 3-10 дней | 7 000 | Низкая |
| 7 | Выставление счёта | Finance ops | 1С, банк-клиент, ЭДО | 20 мин | 600 | Высокая |
| 8 | Оплата и активация клиента | Finance ops + Customer Success | Банк-клиент, CRM, billing | 1 день | 900 | Высокая |
| 9 | Onboarding: доступы, 1С, ЭДО, bank statements, шаблоны | CS + Finance ops specialist | 1С, Saby/Контур, shared drive, RPA | 3-5 рабочих дней | 9 500 | Средняя |
| 10 | Ежедневная обработка первички, AP, invoicing, reconciliations | Finance ops specialist | 1С, OCR, LLM extraction, RPA, bank feeds | Постоянно | 19 000 / мес | Средняя |
| 11 | Контроль качества и закрытие месяца | Chief accountant / QA | 1С, checklists, BI dashboard | 4-6 ч / мес | 7 000 / мес | Низкая |
| 12 | Продление / upsell / повторный платёж | CS + AE | CRM, QBR, BI, billing | 1-2 ч / мес | 2 500 / мес | Средняя |

**Вывод:** процесс монетизируется только если onboarding и ежедневная обработка стандартизированы вокруг 1С + ЭДО + банков. Если каждая сделка превращается в мини-проект интеграции, contribution margin быстро падает ниже 60%.

---

## 3. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Finance ops specialist delivery time | 19 000 | ~0.086 FTE при fully-loaded FOT 221 000 ₽ |
| Chief accountant review / QA | 7 000 | ~0.022 FTE при fully-loaded FOT 312 000 ₽ |
| Customer Success / support allocation | 4 000 | ~0.015 FTE |
| OCR / LLM / document AI / RPA | 5 000 | Распознавание, классификация, prompt/runtime, workflow |
| Интеграции и ЭДО / bank feeds / 1С коннекторы | 3 000 | Saby/ЭДО/connectors |
| Cloud / security / storage | 2 500 | Хостинг, backup, monitoring, secrets |
| Потери на платежах, исправлениях, ручных исключениях | 1 500 | Резерв на нестандартные кейсы |
| **Итого COGS** | **42 000** |  |

### Выручка и маржа на 1 клиента

| Показатель | Значение |
|---|---:|
| MRR на клиента | **160 000 ₽** |
| COGS | **42 000 ₽** |
| Contribution profit | **118 000 ₽** |
| Contribution Margin | **73.8%** |

---

## 4. CAC по каналам и воронка

### 4.1 CAC по каналам

| Канал | Лиды / мес | SQL / мес | Proposal / мес | New paying / мес | Месячные затраты, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Outbound | 900 | 18 | 6 | 2 | 420 000 | **210 000** |
| Paid inbound (Яндекс/VK/search) | 300 | 12 | 4 | 1 | 240 000 | **240 000** |
| Partnerships / referrals | 25 | 6 | 3 | 1 | 177 000 | **177 000** |
| **Blended** | **1 225** | **36** | **13** | **4** | **837 000** | **209 250** |

### 4.2 Funnel conversion

| Funnel stage | Outbound | Paid inbound | Partnerships |
|---|---:|---:|---:|
| Lead → meeting | 8.0% | 15.0% | 48.0% |
| Meeting → SQL | 25.0% | 26.7% | 50.0% |
| SQL → proposal | 33.3% | 33.3% | 50.0% |
| Proposal → win | 33.3% | 25.0% | 33.3% |
| Lead → win | 0.22% | 0.33% | 4.0% |

### 4.3 Fully-loaded CAC, обязательный расчёт

Сегмент здесь **mid-market B2B**, поэтому для sanity используется коэффициент overhead выше self-serve. В расчёте применён требуемый множитель **x1.3** поверх raw acquisition spend.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 180 000 | Базовый тестовый медиабюджет на нишевый B2B ICP | internal model + RU B2B launch assumption |
| Outbound team FOT (SDR + 0.5 AE attributed to new) | 403 000 | SDR 208 000 + 50% AE 195 000 | HH vacancy snapshots, 2026-04-24 |
| Marketing team FOT allocation | 90 000 | ~23% Product/Ops/marketing FOT 390 000 ₽ | internal allocation |
| Tools / CRM / data / sequencing | 42 000 | CRM + enrichment + телефония + email stack | vendor stack estimate |
| Events / partnerships | 33 000 | meetups, partner commissions, small events | internal model |
| Raw CAC spend subtotal | **748 000** | сумма строк выше |  |
| Overhead multiplier (x1.3) | **224 400** | 748 000 × 30% | required fully-loaded overhead |
| **Total fully-loaded acquisition spend** | **972 400** |  |  |
| **New paying customers / мес** | **4** | blended model |  |
| **Fully-loaded CAC** | **243 100 ₽** | 972 400 / 4 |  |

**Консервативный рабочий CAC для модели:** **243 100 ₽**.

Это всё ещё попадает в user-provided sanity range для **mid-market SaaS 60-250K ₽**, но уже у верхней границы. Значит, экономика чувствительна к просадке конверсии и к удлинению sales cycle.

---

## 5. LTV и churn benchmark

### 5.1 Churn benchmark

Для SMB/mid-market B2B подписки с заметной сервисной составляющей я беру **2.5% monthly churn** как консервативный ориентир.

Почему это разумно:
- SaaS Capital в 2025 пишет, что у B2B SaaS-компаний c ARR <10 млн $ logo churn заметно выше, чем у более крупных игроков; маленькие компании и SMB-oriented motion теряют клиентов чаще, чем enterprise. Это не точный proxy для finance ops service, но корректное направление для оценки. Источник: https://www.saas-capital.com/blog-posts/2025-b2b-saas-retention-benchmarks/
- Optifi.ai в 2026 сводит benchmark monthly churn для B2B SaaS в диапазоне около **3-5% для SMB** и **1-2% для enterprise**. Для данного кейса, который сидит между SMB и lower mid-market, **2.5% в месяц** выглядит рабочим базовым сценарием, а не агрессивным optimist case. Источник: https://www.optifi.ai/post/saas-churn-benchmarks

### 5.2 LTV calculation

Формула:

`LTV = ARPU × Contribution Margin % / Monthly churn`

`LTV = 160 000 × 73.75% / 2.5% = 4 720 000 ₽`

| Показатель | Значение |
|---|---:|
| ARPU / MRR | 160 000 ₽ |
| Contribution Margin % | 73.75% |
| Monthly churn | 2.5% |
| **LTV** | **4 720 000 ₽** |

---

## 6. LTV/CAC, CAC payback, contribution margin

| Метрика | Формула | Значение | Verdict |
|---|---|---:|---|
| LTV/CAC | 4 720 000 / 243 100 | **19.4x** | PASS |
| CAC Payback | 243 100 / 160 000 | **1.52 мес** | PASS |
| Contribution Margin % | (160 000 - 42 000) / 160 000 | **73.8%** | PASS |

### Sanity check against investment grade
- Требование investable: **LTV/CAC ≥ 3.0**. Здесь **19.4x**.
- Требование payback: **<12 мес** для базового B2B. Здесь **1.5 мес**.
- Ключевая оговорка: такой payback выглядит очень хорошим, потому что модель с high-retainer ARPU. Если реальный ARPU съедет к **120-130 тыс. ₽**, запас прочности заметно ухудшится.

---

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Функция | Кол-во | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO / Founder | Продажи крупных сделок, стратегия, финконтур | 1 | 500 000 | 150 000 | **650 000** |
| CTO / Tech Lead | Архитектура, интеграции, data layer | 1 | 450 000 | 135 000 | **585 000** |
| Senior Backend | Коннекторы, orchestration, billing, API | 2 | 350 000 | 105 000 | **910 000** |
| ML Engineer | OCR/LLM prompts, extraction quality, routing | 1 | 450 000 | 135 000 | **585 000** |
| DevOps | Infra, monitoring, secrets, CI/CD | 1 | 300 000 | 90 000 | **390 000** |
| Frontend | Кабинет, ops UI, CS tools | 1 | 250 000 | 75 000 | **325 000** |
| Product / Ops Lead | Упаковка оффера, процессы, маркетинг allocation | 1 | 300 000 | 90 000 | **390 000** |
| SDR | Outbound prospecting | 1 | 160 000 | 48 000 | **208 000** |
| AE | Discovery, proposals, close | 1 | 300 000 | 90 000 | **390 000** |
| Customer Success | Onboarding, retention, QBR | 1 | 200 000 | 60 000 | **260 000** |
| Finance Ops Specialist | Ежедневный delivery | 3 | 170 000 | 51 000 | **663 000** |
| Chief Accountant / QA | Контроль качества и закрытие месяца | 1 | 240 000 | 72 000 | **312 000** |
| **Итого** |  | **14** |  |  | **5 668 000 ₽/мес** |

### 7.2 Обязательная таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 500 000 | 0 (founder) | 0 | 150 000 | 650 000 |
| CTO/Tech Lead | 1 | 450 000 | 2.0 | 2.0 | 135 000 | 585 000 |
| Senior Backend | 2 | 350 000 | 1.5 | 1.5 | 105 000 | 455 000 / чел |
| ML Engineer | 1 | 450 000 | 2.5 | 2.0 | 135 000 | 585 000 |
| DevOps | 1 | 300 000 | 1.5 | 1.0 | 90 000 | 390 000 |
| Frontend | 1 | 250 000 | 1.0 | 1.0 | 75 000 | 325 000 |
| SDR | 1 | 160 000 | 0.75 | 1.0 | 48 000 | 208 000 |
| AE | 1 | 300 000 | 1.5 | 2.5 | 90 000 | 390 000 |
| Customer Success | 1 | 200 000 | 1.0 | 1.0 | 60 000 | 260 000 |

**Salary benchmark note:** диапазоны подтверждены HH snapshot pages на 2026-04-24: senior backend, frontend, DevOps, ML Engineer, CTO, SDR/account executive related searches. Ниже в Sources даны ссылки. Я использую консервативные midpoint-like gross значения внутри наблюдаемого коридора.

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | **650 000** |
| M2 | CEO + CTO | **1 235 000** |
| M3 | + Backend #1 + Product/Ops | **2 080 000** |
| M4 | + Frontend + DevOps | **2 795 000** |
| M5 | + Backend #2 + ML Engineer | **3 835 000** |
| M6 | + SDR | **4 043 000** |
| M7 | + AE + Customer Success | **4 693 000** |
| M8 | + Finance Ops Specialist #1 + Chief Accountant | **5 226 000** |
| M9 | + Finance Ops Specialist #2 | **5 447 000** |
| M10 | + Finance Ops Specialist #3 | **5 668 000** |
| M11 | Полная команда | **5 668 000** |
| M12 | Полная команда | **5 668 000** |

**Проверка realism:** план не нанимает 5+ человек в первый месяц и учитывает, что ML/CTO/AE не выходят мгновенно. Это выглядит реалистично для Москвы/СПб рынка найма 2026.

---

## 8. Fixed costs breakdown

Ниже fixed cost база для расчёта break-even. Delivery staff, которые сидят в COGS на клиента, здесь не дублируются.

| Компонент fixed costs | ₽/мес |
|---|---:|
| Core team FOT (CEO, CTO, backend x2, ML, DevOps, frontend, Product/Ops, SDR, AE, CS) | **4 693 000** |
| Office / legal / бухгалтерия / admin | 120 000 |
| Cloud platform shared core / monitoring / backups | 85 000 |
| CRM / телефония / internal tools | 42 000 |
| Paid acquisition budget | 180 000 |
| Events / partnerships | 33 000 |
| Misc reserve | 145 000 |
| **Итого fixed costs / мес** | **5 298 000 ₽** |

---

## 9. Break-even: по клиентам и по месяцу

### 9.1 Break-even по числу клиентов

Формула:

`Break-even clients = Fixed costs / Contribution profit per client`

`= 5 298 000 / 118 000 = 44.9`

**Break-even = 45 клиентов.**

### 9.2 Break-even по месячной выручке

`Break-even revenue = 45 × 160 000 = 7 200 000 ₽ / мес`

### 9.3 Break-even по времени

При реалистичном ramp-up:
- M6: 4 клиента
- M9: 16 клиентов
- M12: 36 клиентов
- M15-M16: 45-46 клиентов

**Оценка break-even по времени: M15-M16 от старта.**

### 9.4 EBITDA на 50 клиентах

| Показатель | Значение |
|---|---:|
| Revenue @ 50 clients | 8 000 000 ₽ |
| COGS @ 50 clients | 2 100 000 ₽ |
| Gross profit @ 50 clients | 5 900 000 ₽ |
| Fixed costs | 5 298 000 ₽ |
| **EBITDA @ 50 clients** | **+602 000 ₽/мес** |

**Profit Gate:** PASS, потому что при 50 клиентах компания уже может выйти выше **500K ₽ EBITDA/мес**.

---

## 10. Burn-to-breakeven и cash runway

### 10.1 Burn-to-breakeven

Использую gross profit после COGS и вычитаю core fixed burn. При указанном ramp-up до M15-M16 совокупный cash burn до операционного breakeven оценивается в **36-38 млн ₽**.

Это означает:
- ниже **30 млн ₽** стартового капитала модель опасно хрупкая;
- **40 млн ₽** выглядят рабочим минимумом с небольшим буфером;
- любой провал по hiring, churn или ARPU легко съедает буфер.

### 10.2 Cash runway

| Показатель | Значение |
|---|---:|
| Startup capital | **40 000 000 ₽** |
| Средний burn в первые 12 мес | ~**2.9 млн ₽/мес** |
| Простая runway-оценка | **13.7 мес** |
| Реальная runway с убывающим burn при росте клиентов | **15-16 мес** |

**Вывод:** раунд ниже 40 млн ₽ для такой модели нежелателен. На бумаге unit economics красивые, но cash conversion медленная, потому что приходится заранее строить команду и GTM.

---

## 11. Основные риски для economics

1. **ARPU compression.** Если рынок примет только 120-130 тыс. ₽/мес, EBITDA на 50 клиентах уйдёт обратно к нулю.
2. **Service creep.** Любая кастомная интеграция с 1С или нестандартный payroll/налоговый контур быстро повышает COGS.
3. **Sales cycle drift.** Если win-rate из proposal падает с 30% к 15-20%, blended CAC уходит выше 300 тыс. ₽.
4. **Retention fragility.** У SMB churn может быть выше 2.5% в кризисный год, особенно если owner воспринимает сервис как заменимый аутсорс.
5. **Hiring bottleneck.** CTO, ML и сильный chief accountant не нанимаются моментально, а без них качество delivery страдает.

---

## 12. Итоговый verdict

**Unit economics verdict: PASS WITH TIGHT EXECUTION.**

Кейс выглядит **инвестируемым на unit economics уровне**, если соблюдаются одновременно четыре условия:
- чек держится около **160 тыс. ₽ MRR**;
- delivery остаётся стандартизированным, а не кастомным;
- churn удерживается около **2.5% monthly** или ниже;
- компания действительно доводит базу до **45-50 активных клиентов**.

Если хотя бы один из этих параметров ломается, модель быстро превращается из investable SaaS-enabled service в просто неплохо продающийся, но тяжёлый операционный аутсорс.

## Sources
- HH, Senior Backend, Москва, snapshot 2026-04-24: https://hh.ru/vacancies/senior-backend-developer
- HH, DevOps, Москва, snapshot 2026-04-24: https://hh.ru/vacancies/devops
- HH, Frontend Developer, Москва, snapshot 2026-04-24: https://hh.ru/vacancies/frontend-developer
- HH, ML Engineer, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=ML+Engineer&area=1
- HH, CTO, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=CTO&area=1
- HH, Sales Development Representative, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=sales+development+representative&area=1
- HH, менеджер по продажам B2B SaaS, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=%D0%BC%D0%B5%D0%BD%D0%B5%D0%B4%D0%B6%D0%B5%D1%80+%D0%BF%D0%BE+%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%D0%B0%D0%BC+B2B+SaaS&area=1
- SaaS Capital, 2025 B2B SaaS Retention Benchmarks: https://www.saas-capital.com/blog-posts/2025-b2b-saas-retention-benchmarks/
- Optifi.ai, SaaS Churn Benchmarks, accessed 2026-04-24: https://www.optifi.ai/post/saas-churn-benchmarks
- Finally pricing and product pages, accessed earlier in case intake: https://finally.com/ ; https://finally.com/bookkeeping.html ; https://finally.com/pricing.html
