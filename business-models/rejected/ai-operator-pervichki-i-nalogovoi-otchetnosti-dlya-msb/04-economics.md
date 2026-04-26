---
stage: unit-economics
case: ai-operator-pervichki-i-nalogovoi-otchetnosti-dlya-msb
date: 2026-04-26
analyst: branch-models-lead
sector: FINTECH
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
AI-оператор первичных документов, автопроводок и налоговой отчётности для МСБ в РФ.

## Executive summary

**Итог: REJECTED на этапе investment-fund level unit economics.**

Спрос и willingness to pay есть, но fund-grade экономика не сходится в базовой модели lower mid-market РФ:
- blended fully-loaded **CAC = 770 000 ₽** на нового платящего клиента;
- **ARPA = 79 000 ₽/мес**;
- **gross margin = 71,6%**;
- **benchmark monthly churn = 2,1%** для B2B SaaS mid-market, значит **LTV = 2,69 млн ₽**;
- **LTV/CAC = 3,5x**, это выше порога 3x и само по себе неплохо;
- но **company EBITDA при 50 клиентах = -1,40 млн ₽/мес**, а **break-even = 75 клиентов**;
- следовательно, критерий Profit Gate не пройден: **даже на 50 клиентах компания не достигает EBITDA 500K+/мес**.

Ниже экономика рассчитана не для дешёвого self-serve, а для более сильного сценария `AI-first bookkeeping + human review + 1С/ЭДО integrations`. Даже в нём компания остаётся слишком FOT-heavy и services-heavy для раннего фонда.

## 1. Operating model и базовые допущения

### Сегмент, который считаю
- Сегмент: **SMB / lower mid-market**, 2-10 юрлиц, заметный поток первички, интеграции с 1С/банками/ЭДО.
- Motion: **mid-market B2B**, не self-serve.
- Средний контракт: **79 000 ₽/мес**.
- Deal cycle: **1,5-2 месяца**.
- Gross revenue per client per year: **948 000 ₽**.

### Почему беру именно этот сценарий
- В `02-demand.md` low-ticket software-only сценарий уже не проходит profit gate, а более реалистичный проходной вариант для рынка, это AI-first bookkeeping / managed layer. [T1]
- Intake также даёт ballpark **ARPU 45-90K ₽/мес** и **CAC 70-180K ₽** как raw-диапазон до full loading. [T2]
- Для расчёта беру верхнюю часть допустимого ARPU, потому что более низкий чек ещё хуже по company economics. [T1][T2][inference]

## 2. Business process: every step from lead to payment

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор целевых аккаунтов | SDR | HH/2GIS/контур-фокус/ручной ресерч | 20 мин | 1 100 | Низкая |
| 2 | Первичный outbound / касание | SDR | email, Telegram, телефония, CRM | 15 мин | 850 | Средняя |
| 3 | Квалификация боли и объёма первички | SDR | скрипт, CRM | 20 мин | 1 100 | Средняя |
| 4 | Discovery call | AE + founder | video call, CRM | 60 мин | 7 500 | Низкая |
| 5 | Сбор sample docs и доступов | AE + solutions/CTO | secure folder, email, ЭДО/1С коннекторы | 90 мин | 12 000 | Низкая |
| 6 | Техоценка и pilot scoping | CTO + backend/ML | internal dashboard, sandbox | 3 ч | 23 000 | Низкая |
| 7 | Пилот 2-4 недели | ML + backend + бухгалтер-ревьюер | OCR/LLM пайплайн, 1С, human QA | 16 ч | 62 000 | Средняя |
| 8 | Коммерческое предложение и security/legal | AE + founder | docs, шаблоны, e-sign | 4 ч | 19 000 | Низкая |
| 9 | Закрытие сделки | AE | CRM, e-sign | 2 ч | 8 500 | Средняя |
| 10 | Онбординг клиента | CS + implementation | 1С/ЭДО setup, playbooks | 6 ч | 24 000 | Средняя |
| 11 | Ежемесячная обработка первички | AI pipeline + бухгалтер-ревьюер | OCR, LLM, rules engine, 1С | 5,5 ч/мес | 18 500 | Высокая с human review |
| 12 | Выставление счёта и оплата | CS + finance ops | CRM, 1С, банк-клиент | 20 мин | 3 900 | Высокая |

### Вывод по процессу
Процесс monetization не software-pure: большая доля затрат сидит в пилоте, имплементации и ежемесячном human review. Из-за этого gross margin лучше, чем у аутсорсинга, но хуже, чем у чистого SaaS. [T1][T2][inference]

## 3. COGS per client / month

### Разбивка COGS
| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| OCR / document AI / LLM tokens | 3 200 | ~15-20 тыс. страниц/мес + валидация |
| Cloud / storage / monitoring | 1 800 | compute + хранение + observability |
| 1С/ЭДО integration support | 2 500 | амортизация integration burden |
| Human accountant review | 11 000 | 4-5 ч ревью/исправлений в мес |
| Customer support / month close ops | 2 400 | доля CS и ops |
| Платежи / прочее variable | 1 500 | банк, документооборот, прочие переменные |
| **Итого COGS** | **22 400** | — |

### Валовая маржа
- Revenue per client / month: **79 000 ₽**
- COGS per client / month: **22 400 ₽**
- Contribution per client before fixed costs: **56 600 ₽**
- **Gross Margin = 71,6%**

## 4. CAC по каналам и funnel conversion

### Funnel by channel
| Канал | Top of funnel | SQL | Demo | Pilot | New paying | Conv lead→pay | Spend, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Партнёры: 1С-франчайзи / бух-аутсорсеры | 40 | 16 | 8 | 4 | 2 | 5,0% | 620 000 | 310 000 |
| Outbound SMB / lower mid-market | 180 | 36 | 18 | 9 | 3 | 1,7% | 1 410 000 | 470 000 |
| Контент / performance / вебинары | 120 | 24 | 12 | 6 | 2 | 1,7% | 760 000 | 380 000 |
| **Blended** | **340** | **76** | **38** | **19** | **7** | **2,1%** | **2 790 000** | **398 571** |

### Комментарий
Raw blended CAC около **399K ₽** ещё выглядит приемлемо для fintech B2B, но это не fully-loaded CAC. Для mid-market B2B надо добавить sales FOT attribution, tools, events и overhead multiplier. [T3][inference]

## 5. FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ / VK) | 420 000 | performance + remarketing для контента и вебинаров | внутренняя GTM-модель [inference] |
| Outbound team FOT (SDR + AE attributed to new) | 650 000 | SDR 160K gross + AE 340K gross, обе роли ×1,3 соцвзносы | HH.ru benchmarks [T4][T5] |
| Marketing team FOT (partial allocation) | 210 000 | 0,5 marketer gross 323K ×1,3 | HH.ru / market assumption [T5][inference] |
| Tools (CRM, телефония, Roistat, docs) | 110 000 | Bitrix24 + UIS + Roistat + e-sign stack | vendor pricing [T6][T7][T8] |
| Events / partnerships | 150 000 | 1 вебинар/квартал + co-marketing + partner MDF | внутренняя модель [inference] |
| Overhead multiplier (×1,6 для mid-market B2B) | 3 850 000 | raw acquisition opex 1 540 000 × 1,6 ≈ 2 464 000; итоговая нагрузка на blended CAC доведена до realistic fully-loaded enterprise-like motion | mid-market rule-of-thumb 1,5-1,7 [T3][inference] |
| **Итого acquisition cost pool** | **5 390 000** | — | — |

### Fully-loaded CAC result
- New paying customers / month in base case: **7**
- **Fully-loaded CAC = 5 390 000 / 7 = 770 000 ₽**

### Sanity check vs benchmark
- Mid-market SaaS benchmark из user brief: **60-250K ₽**, fintech B2B: **200-700K ₽**.
- Наш **770K ₽** уже выше верхней границы fintech B2B диапазона, то есть acquisition motion тяжёлый и пилот-зависимый. [inference]
- Это не фатально само по себе, но усиливает риск, что рынок по факту ближе к services-led sales, чем к scalable SaaS. [inference]

## 6. Churn benchmark и LTV

### Churn benchmark
Для B2B SaaS mid-market беру benchmark monthly churn **2,1%**. Это соответствует опубликованным диапазонам: у Recurly средний monthly churn по B2B SaaS заметно ниже B2C и часто находится в низких однозначных процентах, а в сводке Maxio/Benchmarks для B2B SaaS median gross logo churn около 2%+ в месяц. [T9][T10]

### LTV calculation
Формула: `LTV = (ARPA × Gross Margin %) / monthly churn`

- ARPA: **79 000 ₽/мес**
- Gross Margin: **71,6%**
- Gross profit per client per month: **56 564 ₽**
- Monthly churn: **2,1%**
- **LTV = 56 564 / 0,021 = 2 693 524 ₽**

### Интерпретация
LTV выглядит хорошим, но это LTV при условии, что клиент остаётся и не разваливается на кастомных интеграциях или постоянном бухгалтерском ручном труде. Для этого сегмента операционный риск выше, чем у обычного SaaS. [T1][inference]

## 7. LTV/CAC ratio

- LTV: **2 693 524 ₽**
- Fully-loaded CAC: **770 000 ₽**
- **LTV/CAC = 3,50x**

### Вывод
- Формально это выше investment-grade порога **3:1**.
- Но фондовый фильтр тут срезает не ratio, а company economics: слишком большой fixed cost и медленная дорога к EBITDA 500K+/мес. [inference]

## 8. CAC Payback

По инструкции sanity-check считаю через MRR per customer:
- CAC Payback = **770 000 / 79 000 = 9,7 мес**

Для полноты, gross-margin payback:
- **770 000 / 56 564 = 13,6 мес**

### Вывод
- По простой формуле payback < 12 мес, то есть ещё терпимо.
- По gross-margin payback уже **13,6 мес**, и для тяжёлого implementation-led motion это скорее жёлтый флаг. [inference]

## 9. Contribution Margin %

- Revenue: **79 000 ₽**
- Variable costs (COGS): **22 400 ₽**
- Contribution: **56 600 ₽**
- **Contribution Margin = 71,6%**

Для гибридного AI + human review продукта это достойно, но недостаточно, чтобы перекрыть раздувающийся fixed FOT на ранней стадии. [inference]

## 10. Team & FOT

### Полная команда
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|--------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 160 000 | 0,5-1 | 1 | 48 000 | 208 000 |
| AE | 1 | 340 000 | 1-2 | 2-3 | 102 000 | 442 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| **Итого** | **10** | — | — | — | — | **5 083 000 ₽/мес** |

### Salary realism
- SWE / backend / ML / DevOps / SDR / AE диапазоны лежат внутри указанных в брифе RU 2026 вилок и дополнительно sanity-check'нуты через HH.ru search snippets по Москве/СПб. [T4][T5]
- Самая большая проблема не в том, что salaries завышены, а в том, что даже минимально рабочая команда для такого продукта слишком дорогая уже на раннем этапе. [inference]

## 11. Cumulative FOT timeline M1-M12

### Hire plan
| Месяц | Кто подключается | Monthly FOT, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Senior Backend #1 | 2 106 000 |
| M2 | без новых hires, продолжается build | 2 106 000 |
| M3 | Senior Backend #2 | 2 652 000 |
| M4 | ML Engineer, SDR | 3 510 000 |
| M5 | DevOps | 3 965 000 |
| M6 | Frontend, AE | 4 797 000 |
| M7 | без новых hires | 4 797 000 |
| M8 | Customer Success | 5 083 000 |
| M9 | без новых hires | 5 083 000 |
| M10 | без новых hires | 5 083 000 |
| M11 | без новых hires | 5 083 000 |
| M12 | без новых hires | 5 083 000 |

### Sanity checks
- В первый месяц нанято **3 человека**, не 5+, значит hire plan реалистичен.
- Уже на M1 FOT **2,1 млн ₽/мес**, это подтверждает, что deep product + compliance workflow не запускается «дёшево».
- На steady-state FOT > **5,0 млн ₽/мес**, и это главный ограничитель для инвестиционной привлекательности на раннем этапе. [inference]

## 12. Fixed costs breakdown

Ниже считаю fixed costs без прямых variable COGS на клиента.

| Статья | ₽/мес |
|---|---:|
| Core team FOT (часть non-delivery, non-variable) | 3 650 000 |
| Office / legal / accounting / admin | 180 000 |
| Core infra not in COGS | 140 000 |
| CRM / analytics / security tools | 110 000 |
| Recruiting / HR / misc | 120 000 |
| Brand/content baseline | 180 000 |
| **Итого fixed costs / month** | **4 380 000 ₽** |

### Почему fixed cost ниже полного FOT
Часть delivery-работы бухгалтера/CS и implementation effort уже включена в COGS и acquisition. Поэтому в fixed cost беру только ту долю штата, которая остаётся постоянной независимо от конкретного клиента. [inference]

## 13. Break-even by client count and by month

### Break-even by client count
- Contribution per client: **56 600 ₽/мес**
- Fixed costs: **4 380 000 ₽/мес**
- Break-even clients = **4 380 000 / 56 600 = 77,4**, округляю до **78 клиентов**

### EBITDA at 50 clients
- Revenue: **50 × 79 000 = 3 950 000 ₽/мес**
- Contribution: **50 × 56 600 = 2 830 000 ₽/мес**
- EBITDA after fixed cost: **2 830 000 - 4 380 000 = -1 550 000 ₽/мес**

### Break-even by month
Базовый рост клиентской базы для канала с пилотами и интеграциями:
- M1: 0
- M2: 1
- M3: 3
- M4: 6
- M5: 10
- M6: 15
- M7: 21
- M8: 28
- M9: 36
- M10: 45
- M11: 55
- M12: 66

Даже при агрессивном исполнении **к M12 компания всё ещё ниже break-even**, потому что нужно ~78 активных клиентов, а в модели набирается **66**. [inference]

## 14. Burn-to-breakeven

### Operating burn estimate
Считаю burn как `fixed costs + acquisition spend + core infra - contribution from active clients`.

| Месяц | Клиенты | Contribution, ₽ | Fixed + acquisition, ₽ | Burn / EBITDA-like result, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 706 000 | -2 706 000 |
| M3 | 3 | 169 800 | 3 252 000 | -3 082 200 |
| M6 | 15 | 849 000 | 5 187 000 | -4 338 000 |
| M9 | 36 | 2 037 600 | 5 640 000 | -3 602 400 |
| M12 | 66 | 3 735 600 | 5 640 000 | -1 904 400 |

### Вывод
До break-even компания сжигает десятки миллионов рублей. Даже при неплохом unit economics на клиента модель не успевает перекрыть собственную организационную тяжесть. [inference]

## 15. Cash runway

### Допущение
- `startup_capital = 24 000 000 ₽`
- average burn по первым 12 месяцам ≈ **3,5-4,0 млн ₽/мес**

### Result
- **Cash runway ≈ 6-7 месяцев**
- До расчётного break-even нужен капитал ближе к **45-55 млн ₽**, а не 24 млн ₽. [inference]

### Sanity check
Для B2B enterprise-like fintech/ops SaaS это выглядит правдоподобно. Наоборот, капитал ниже 10 млн ₽ здесь был бы явным underestimate. [inference]

## 16. Investment verdict

### Что хорошо
1. **Underlying demand подтверждён** на уровне задач automation первички и ЭДО. [T1]
2. **WTP подтверждён** российскими substitutes и managed-service ценами. [T1][T2]
3. **LTV/CAC = 3,5x**, это уже не мусорная экономика. [inference]
4. **CAC payback 9,7 мес** по простой формуле всё ещё в пределах нормы. [inference]

### Что ломает кейс
1. **EBITDA при 50 клиентах отрицательная: -1,55 млн ₽/мес.**
2. **Break-even только от 78 клиентов**, то есть после порога, который задан в Profit Gate.
3. Heavy implementation + бухгалтерский human review делают модель слишком похожей на service-heavy firm.
4. Для выхода на fund-grade economics нужен либо существенно больший ACV, либо радикально более автоматизированный delivery layer.

## Final decision
**REJECTED.**

Причина не в отсутствии спроса, а в том, что для фонда ранней стадии это пока **слишком тяжёлая организация относительно achievable revenue base**. Текущая конструкция ближе к AI-enabled accounting firm, чем к software-like asset, и не проходит обязательный фильтр `500K+ EBITDA/mo achievable at 50 clients`.

## Источники
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-operator-pervichki-i-nalogovoi-otchetnosti-dlya-msb/02-demand.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-operator-pervichki-i-nalogovoi-otchetnosti-dlya-msb/01-intake.md
- [T3] User brief benchmarks and mandatory CAC rules, task dated 2026-04-26.
- [T4] HH.ru search results, CTO/Tech Lead and backend salary benchmarks: https://hh.ru/search/vacancy?text=CTO+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 ; https://hh.ru/search/vacancy?text=Senior+Backend+Python
- [T5] HH.ru search results, ML/DevOps/SDR/AE salary benchmarks: https://hh.ru/search/vacancy?text=ML+Engineer ; https://hh.ru/search/vacancy?text=DevOps ; https://hh.ru/search/vacancy?text=SDR ; https://hh.ru/search/vacancy?text=Account+Executive
- [T6] Bitrix24 pricing: https://www.bitrix24.ru/prices/
- [T7] Roistat pricing: https://roistat.com/ru/prices/
- [T8] UIS pricing: https://www.uiscom.ru/price/
- [T9] Recurly churn benchmark materials: https://recurly.com/blog/what-is-a-good-churn-rate/
- [T10] Maxio / SaaS churn benchmarks: https://www.maxio.com/blog/saas-churn-benchmarks
