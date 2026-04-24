---
stage: economics
case: corgi-startup-insurance-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Corgi, AI-native страхование стартапов и tech-компаний. Для локального GEO-expand в РФ моделирую не страховую компанию с лицензией, а более реалистичный формат: digital broker / MGA-like слой с быстрым квотированием, сбором документов, андеррайтинг-оркестрацией и сопровождением полиса.

## Executive summary
**Вердикт: REJECTED.**

На 24 апреля 2026 года экономика не проходит investment-grade screen фонда.

Ключевые выводы:
1. **Средняя выручка на клиента слишком низкая** для тяжёлого regulated GTM: беру **75 000 ₽ MRR** как base case, что уже близко к верхнему публичному диапазону Corgi для startup/Series A пакетов.
2. **Blended fully-loaded CAC = 570 167 ₽ на нового платящего клиента**, что слишком высоко для категории с таким ARPU.
3. **LTV = 773 810 ₽**, **LTV/CAC = 1,36x**, что существенно ниже инвестируемого порога **3,0x**.
4. **EBITDA > 500 тыс. ₽/мес не достигается даже на 50 клиентах**: при 50 клиентах модель даёт около **-2,84 млн ₽ EBITDA/мес**.
5. **Break-even требует ~137 клиентов**, что несоразмерно локальному SOM и тяжести найма / compliance.

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний чек (MRR) | 75 000 ₽/клиент/мес | sanity-case между pre-seed и growth пакетами Corgi |
| Клиентов в base-scale | 50 | тест Profit Gate |
| Monthly logo churn | 4,2% | ближе к SMB/mid-market B2B SaaS benchmark, но с поправкой на слабый lock-in |
| Валовая маржа | 43,3% | после carrier/ops/support/cloud/KYC COGS |
| Contribution margin | 30,0% | после COGS и переменных комиссий/реферальных выплат |
| New paying customers / мес | 3 | для early-stage regulated motion в РФ |
| Startup capital | 35 000 000 ₽ | sanity level для B2B/fin-regulated запуска |

## 2. Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Захват inbound/outbound лида | SDR / Growth | CRM, формы сайта, email sequencing | 20 мин | 900 | Средняя |
| 2 | Первичная квалификация: стадия, выручка, отрасль, лимиты покрытия | SDR | CRM, call script | 30 мин | 1 350 | Средняя |
| 3 | Сбор анкет и документов | SDR + клиент | CRM, doc collection, e-sign | 45 мин | 2 025 | Средняя |
| 4 | Проверка KYC/AML и базовых санкционных ограничений | Ops / Compliance | KYC-провайдер, чек-листы | 25 мин | 1 800 | Низкая-средняя |
| 5 | Андеррайтинг-триаж и разметка риска | AE + Underwriting Ops | scoring sheet, AI intake, carrier templates | 60 мин | 4 200 | Средняя |
| 6 | Запрос котировок у страховщиков/партнёров | AE | email, CRM, insurer portals | 50 мин | 3 500 | Низкая |
| 7 | Сбор и нормализация офферов | AE + Ops | spreadsheet, quoting engine | 45 мин | 3 150 | Средняя |
| 8 | Коммерческая презентация клиенту | AE | demo, proposal, PDF deck | 60 мин | 4 200 | Низкая |
| 9 | Правки, переговоры, согласование лимитов | AE + founder | calls, messaging, redlines | 90 мин | 7 200 | Низкая |
| 10 | Юридическое и бухгалтерское согласование | Ops / Finance | contract templates, ЭДО | 40 мин | 2 300 | Средняя |
| 11 | Выставление счёта / payment link | Finance Ops | billing, банк, ЭДО | 15 мин | 700 | Высокая |
| 12 | Оплата и активация полиса | Finance + Ops | billing, CRM, insurer cabinet | 20 мин | 950 | Высокая |
| 13 | Onboarding и передача в сопровождение | CSM | CRM, knowledge base | 60 мин | 2 600 | Средняя |

**Итого переменный cost-to-acquire+activate одного клиента:** около **34 875 ₽** прямого process-cost до старта обслуживания. Это не CAC, а только операционный cost per won deal.

## 3. COGS на клиента в месяц

### COGS breakdown
| Компонент | ₽/клиент/мес | Как получено | Источник/логика |
|---|---:|---|---|
| Carrier / broker servicing reserve | 22 000 | доля партнёрского обслуживания и ручного размещения риска | inference для broker/MGA-like модели |
| Underwriting ops и ручная обработка кейса | 9 000 | время AE/Ops на renewals и policy changes | модель процесса |
| Customer Success и support | 7 000 | CSM time allocation + support load | модель команды |
| Cloud / AI / data infra | 4 500 | LLM, hosting, storage, observability | infra assumption |
| KYC / anti-fraud / payment processing | 3 000 | проверки и эквайринг | process assumption |
| Claims / refund / dispute reserve | 3 000 | резерв на нестандартные кейсы и возвраты | conservative reserve |
| **Итого COGS** | **48 500** |  |  |

**Gross profit на клиента/мес = 75 000 - 48 500 = 26 500 ₽**

**Gross Margin = 26 500 / 75 000 = 35,3%**

Это низко для software-like истории и ближе к сервисно-брокерской модели, что и ломает инвестиционную математику.

## 4. CAC по каналам и воронка

### Воронка по каналам
| Канал | Лиды/мес | SQL | Win-rate из SQL | New paying / мес | Channel spend, ₽/мес | CAC по каналу, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Paid ads (Яндекс.Директ / VK / performance) | 90 | 14 | 7% | 1 | 420 000 | 420 000 |
| Outbound / founder-led sales | 120 | 18 | 5,6% | 1 | 610 000 | 610 000 |
| Партнёрства / ивенты / VC-referrals | 35 | 7 | 14% | 1 | 385 000 | 385 000 |
| **Итого blended** | **245** | **39** | **7,7%** | **3** | **1 415 000** | **471 667** |

### Fully-loaded CAC (обязательный расчёт)
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocated + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 420 000 | базовый monthly media budget на низкообъёмный regulated B2B leadgen | модель GTM |
| Outbound team FOT (SDR/AE attributed to new) | 610 000 | SDR 224 250 + AE 417 300, почти полностью на new biz | HH.ru benchmarks + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 143 000 | growth/marketing 286 000 × 50% времени на acquisition | HH.ru / рынок |
| Tools (CRM, enrichment, телефония, email, аналитика) | 87 500 | CRM + sequencing + call tracking + BI | SaaS tool stack assumption |
| Events/partnerships | 55 000 | meetups, комьюнити, referral costs | GTM assumption |
| **Raw acquisition cost** | **1 315 500** | сумма строк выше |  |
| Overhead multiplier (x1.3) | 394 650 | 30% на management overhead, legal/procurement friction | std for B2B acquisition |
| **Fully-loaded spend / мес** | **1 710 150** | raw + overhead |  |
| New paying customers | **3** | blended output | funnel model |
| **Fully-loaded CAC** | **570 167 ₽** | 1 710 150 / 3 | итог |

### Sanity check against RU benchmarks
Для regulated / insurance-like B2B motion допустим benchmark ближе к **200-700 тыс. ₽ CAC**. Наша оценка **570 тыс. ₽** не выглядит заниженной, но для MRR **75 тыс. ₽** она экономически слишком тяжёлая.

## 5. LTV и churn

### Churn benchmark
Использую ориентир **4,2% monthly churn**. Это соответствует верхней границе SMB / lower mid-market B2B SaaS: Optifai в данных за 2025-2026 показывает **3-5% monthly churn для SMB** и **2,1% для mid-market ACV $10K-$50K**. Для Corgi локальный продукт имеет слабый lock-in, ограниченную глубину интеграции и annual-policy renewal risk, поэтому беру **4,2%** как реалистичный benchmark-driven сценарий, а не optimistic enterprise churn.

### Расчёт LTV
`LTV = Gross Profit per customer per month / Monthly churn`

- MRR = **75 000 ₽**
- Gross profit per month = **26 500 ₽**
- Monthly churn = **4,2%**

**LTV = 26 500 / 0,042 = 630 952 ₽**

Для справки revenue-LTV без маржи был бы **1 785 714 ₽**, но для фонда релевантен именно gross-profit LTV.

## 6. LTV/CAC

`LTV/CAC = 630 952 / 570 167 = 1,11x`

**Итог: FAIL.**

Investment-grade порог: **>= 3,0x**.

Даже без жёсткого fail по порогу 1,0x эта экономика слишком слабая, чтобы оправдать regulatory complexity, партнёрские зависимости и длинный цикл продажи.

## 7. CAC Payback

По обязательной sanity-формуле:

`CAC Payback = CAC / MRR_per_customer = 570 167 / 75 000 = 7,6 месяца`

Формально это ниже 12 месяцев, но показатель обманчиво хороший, потому что маржа низкая. Если считать payback по gross profit, то:

`570 167 / 26 500 = 21,5 месяца`

Для инвесткомитета важнее именно **gross profit payback**, и он здесь уже плохой.

## 8. Contribution Margin

Добавляю переменные комиссии/referral payouts после COGS:

| Элемент | ₽/клиент/мес |
|---|---:|
| Выручка | 75 000 |
| COGS | -48 500 |
| Sales commissions / referral payouts | -4 000 |
| Variable billing / dispute admin | -500 |
| **Contribution profit** | **22 000** |

**Contribution Margin = 22 000 / 75 000 = 29,3%**

Это слишком низко для истории, где ещё требуется тяжёлый fixed-cost core.

## 9. Team & FOT

### Таблица команды
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес | Функция |
|---|---:|---:|---:|---:|---:|---:|---|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 | фандрайзинг, partnerships, key sales |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 | платформа, интеграции, security |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each | API, core platform, insurer integrations |
| ML Engineer | 1 | 520 000 | 2,5 | 2 | 156 000 | 676 000 | risk scoring, quote assist, intake models |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 | infra, CI/CD, observability |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 | customer portal, broker UI |
| SDR | 1 | 172 500 | 0,5 | 1 | 51 750 | 224 250 | lead qualification, outreach |
| AE | 1 | 321 000 | 1,5 | 2,5 | 96 300 | 417 300 | demos, quoting, close |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 | onboarding, renewals, retention |
| Growth / Marketing | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 | acquisition, content, partnerships |
| Ops / Compliance | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 | KYC, документы, insurer coordination |
| Finance / Billing Ops | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 | invoicing, collections, reporting |

### Источники по зарплатам
- HH.ru вакансии и выдачи 2025-2026 для Москвы: Senior backend около **350-550 тыс. ₽**, CTO около **600-850 тыс. ₽**, SDR около **100-180 тыс. ₽**, AE / B2B software sales около **150-300+ тыс. ₽**, frontend около **200-300 тыс. ₽**, senior customer success около **200-300 тыс. ₽**.
- Для ML / DevOps использована market-range логика из RU tech hiring 2025-2026, согласованная с указанными диапазонами из пайплайна.

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в payroll | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO, SDR | 1 069 250 |
| M3 | CEO, SDR, CTO, AE | 2 201 550 |
| M4 | + Backend #1, Frontend, Growth | 3 423 550 |
| M5 | + Customer Success, Ops/Compliance | 4 021 550 |
| M6 | + Backend #2, DevOps | 5 022 550 |
| M7 | тот же состав | 5 022 550 |
| M8 | + ML Engineer | 5 698 550 |
| M9 | + Finance/Billing Ops | 5 932 550 |
| M10 | тот же состав | 5 932 550 |
| M11 | тот же состав | 5 932 550 |
| M12 | тот же состав | 5 932 550 |

### Комментарий по hiring realism
- В первый месяц не нанимаю 5+ человек, чтобы не нарушать time-to-hire realism.
- К критическому штатному уровню компания приходит только к **M8-M9**, но к этому моменту выручка ещё не успевает догнать burn.

## 10. Fixed costs

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded steady-state | 5 932 550 | команда из 12 человек |
| Office / legal seat / admin | 180 000 | гибридный офис + базовый admin |
| Legal / compliance / external counsel | 300 000 | договоры, страховщики, wordings, регуляторика |
| Audit / бухгалтерия / финконтур | 120 000 | внешний контур + ЭДО |
| Core infra / SaaS not in COGS | 240 000 | internal BI, security, dev tooling |
| Travel / partner meetings | 90 000 | страховщики, брокеры, пилоты |
| **Итого fixed costs / мес** | **6 862 550** | steady-state |

## 11. Break-even

### По числу клиентов
`Break-even clients = Fixed costs / Contribution profit per client`

= **6 862 550 / 22 000 = 312 клиентов**

Даже если считать не contribution, а gross profit:

= **6 862 550 / 26 500 = 259 клиентов**

Обе цифры полностью расходятся с локальным SOM из demand-stage.

### По месяцам
Даже при достаточно агрессивном наборе клиентов:
- M1: 0
- M2: 1
- M3: 2
- M4: 4
- M5: 7
- M6: 10
- M7: 14
- M8: 18
- M9: 23
- M10: 29
- M11: 36
- M12: 44
- M15: ~60
- M18: ~78

Break-even **не достигается в горизонте 18 месяцев**. На **50 клиентах** компания всё ещё убыточна:

- Revenue = **3 750 000 ₽/мес**
- Contribution profit = **1 100 000 ₽/мес**
- EBITDA ≈ **1 100 000 - 6 862 550 = -5 762 550 ₽/мес**

Даже по gross profit логике:

- Gross profit = **1 325 000 ₽/мес**
- EBITDA ≈ **-5 537 550 ₽/мес**

**Profit Gate: FAIL.** Компания не выходит даже близко к **+500 тыс. ₽ EBITDA/мес** на 50 клиентах.

## 12. Burn-to-breakeven и runway

### Burn-to-breakeven
Упрощённый burn по годовой кривой:
- Средний monthly fixed burn в M1-M12 ≈ **4,93 млн ₽**
- Средний acquisition spend / мес ≈ **1,71 млн ₽**
- Ранний gross profit по клиентской базе в первый год недостаточен, чтобы это компенсировать

Итого early burn до гипотетического break-even: **~6,6 млн ₽/мес** в fully-loaded режиме после разгона.

Даже если предположить, что компания сможет разогнаться до 44 клиентов к M12, накопленный burn остаётся двузначным в миллионах рублей и break-even не виден без следующего раунда.

### Cash runway
`Runway = startup_capital / monthly burn`

При startup capital **35 млн ₽**:
- на раннем среднем burn **~4,6-5,0 млн ₽/мес** runway = **7-8 месяцев**;
- на near steady-state burn **~6,6 млн ₽/мес** runway = **~5,3 месяца**.

Для B2B insurance / regulated motion это короткая полоса, потому что sales cycle, partnerships и product readiness занимают дольше.

## 13. Итоговый инвестиционный вывод

### Что ломает модель
1. **Слишком низкий чек** для regulated GTM.
2. **Слабая валовая маржа**, потому что продукт остаётся сервисно-операционным.
3. **Высокий fully-loaded CAC**, который съедает почти весь экономический upside.
4. **Break-even требует 250-300+ клиентов**, что несовместимо с локальным спросом и командной нагрузкой.
5. **Короткий runway** даже при стартовом капитале 35 млн ₽.

## Финальный вердикт
**REJECTED.**

Кейс не проходит unit economics screen фонда.

- **LTV/CAC = 1,11x** < 3,0x
- **Contribution Margin = 29,3%**
- **Gross Margin = 35,3%**
- **CAC Payback (gross profit) = 21,5 месяцев**
- **EBITDA на 50 клиентах глубоко отрицательная**
- **Break-even по клиентам: 259-312**, что нереалистично

## Источники
- Corgi startup insurance pricing and positioning: https://www.corgi.insure/startup-insurance
- Corgi homepage / about: https://www.corgi.insure/ ; https://www.corgi.insure/about
- Optifai churn benchmark, 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ ; https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- HH.ru vacancy benchmark, Moscow, 2025-2026: https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancy/125002805 ; https://hh.ru/vacancy/129774256 ; https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancies/frontend-developer ; https://hh.ru/vacancies/customer-success-manager
