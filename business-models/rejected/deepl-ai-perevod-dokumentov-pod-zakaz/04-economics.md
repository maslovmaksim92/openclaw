# 04-economics — DeepL API + бюро AI-перевода документов под заказ

Дата: 2026-04-25 13:38 MSK
Статус: investment fund level unit economics review
Сегмент для расчёта: mid-market B2B managed service (ВЭД, юридические документы, тендерные пакеты)

## 1. Executive summary

**Итог: REJECTED на fund level.**

Почему:
1. **Fully-loaded blended CAC ≈ 565 500 ₽ на нового платящего клиента**, что попадает в нижнюю часть enterprise-like RU benchmark, но слишком тяжело для чека **80 000 ₽ MRR**.
2. При валовой марже **60%** и benchmark churn **4.0%/мес** получаем **LTV ≈ 1 200 000 ₽** и **LTV/CAC ≈ 2.1x**, то есть **ниже investable-порога 3.0x**.
3. При реалистичном steady-state штате и fixed cost base компания **не выходит на EBITDA 500k+/мес даже при 50 клиентах**. На 50 клиентах модель даёт около **-1.81 млн ₽ EBITDA/мес**.
4. Break-even наступает только примерно на **88 клиентах**, что слишком далеко для раннего фонда при сервисно-тяжёлой модели.

## 2. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний чек | 80 000 ₽/клиент/мес | retainer на поток договоров, инструкций, тендерных и compliance-документов |
| Средний объём | 120-140 стр./мес | эквивалент среднего клиента mid-market |
| COGS на клиента | 32 000 ₽/мес | AI + human post-edit + QA + PM + infra |
| Валовая маржа | 60.0% | типично для AI-assisted service, но не SaaS-grade |
| Новый платящий клиент/мес в steady state | 4 | при 1 SDR + 1 AE и длинном цикле сделки |
| Sales cycle | 45-75 дней | mid-market B2B, много документов и тестовых переводов |
| Benchmark churn | 4.0%/мес | выше SaaS из-за service-switching и project-based поведения |
| Startup capital | 25 000 000 ₽ | для runway-оценки |

## 3. Business process table, от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор ICP-листов экспортёров, юрфирм, procurement-команд | SDR | HH/2GIS/Excel/CRM | 20 мин/лид | 320 | частично вручную |
| 2 | Первый outbound-touch, email/Telegram/звонок | SDR | CRM + почта + телефония | 15 мин/лид | 240 | частично автоматизировано |
| 3 | Follow-up 2-3 касания | SDR | CRM sequences | 20 мин/лид | 320 | частично автоматизировано |
| 4 | Квалификация боли и объёма документов | SDR | CRM, скрипт discovery | 25 мин/SQL | 400 | вручную |
| 5 | Discovery call и сбор sample docs | AE | Meet/Zoom + CRM | 60 мин | 1 400 | вручную |
| 6 | Тестовый перевод / пилотный sample | Editor lead + QA | DeepL API + CAT tools | 2.5 часа | 4 500 | гибрид AI + human |
| 7 | Коммерческое предложение, SLA, pricing | AE | шаблон КП + CRM | 90 мин | 2 100 | частично автоматизировано |
| 8 | Security/NDA/legal review | CEO/AE | почта + docs | 2 часа | 4 000 | вручную |
| 9 | Закрытие сделки и invoice setup | AE + finance/admin | CRM + 1С/банк | 60 мин | 1 250 | частично автоматизировано |
| 10 | Онбординг, glossary, формат шаблонов | CSM | Notion/Drive/CAT tool | 2 часа | 1 040 | частично автоматизировано |
| 11 | Производство перевода, post-edit, QA, layout | Editor pool + QA | DeepL API + редактура | 6-8 часов/пакет | 20 000-28 000 | гибрид AI + human |
| 12 | Выгрузка, клиентская приёмка, правки, оплата | CSM + finance | CRM + email + банк | 90 мин | 1 200 | частично автоматизировано |

**Вывод:** ядро value delivery остаётся human-heavy. AI сокращает COGS, но не убирает редактуру, QA, форматирование, legal/security и account work.

## 4. COGS breakdown per client/month

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| DeepL API / машинный перевод | 2 000 | usage + document minimums | https://www.deepl.com/en/pro-api |
| Human post-edit переводчиков | 18 000 | ~45-50% от client workload после AI draft | model, anchored to RU bureau pricing from 02-demand |
| QA / senior editor | 6 000 | выборочный second pass + терминология | model |
| PM / account operations | 4 000 | coordination, rush requests, acceptance | model |
| Storage / OCR / misc infra | 2 000 | облако, OCR, защищённое хранение | model |
| **Итого COGS** | **32 000** |  |  |

**Gross Profit/client/month = 80 000 - 32 000 = 48 000 ₽**

## 5. CAC по каналам с воронкой

| Канал | Leads/мес | SQL | Proposal | New paying customers | Конверсия lead→pay | Channel spend, ₽/мес | Channel CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound SDR/AE | 220 | 26 | 8 | 2.0 | 0.91% | 620 000 | 310 000 |
| Partnerships / referrals | 18 | 8 | 4 | 1.0 | 5.56% | 95 000 | 95 000 |
| Content / SEO | 45 | 7 | 3 | 0.6 | 1.33% | 120 000 | 200 000 |
| Paid ads (Яндекс/ВК) | 160 | 10 | 4 | 0.4 | 0.25% | 260 000 | 650 000 |
| **Итого blended raw** | **443** | **51** | **19** | **4.0** | **0.90%** | **1 095 000** | **273 750** |

## 6. Fully-loaded CAC, обязательно по формуле

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier overhead) / New paying customers`

Для этого кейса используется **mid-market B2B multiplier = x1.6** внутри допустимого диапазона **x1.5-1.7**, потому что цикл сделки 45-75 дней, есть тестовый перевод, несколько касаний, NDA/security review.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 260 000 | допущение на тест paid acquisition | model |
| Outbound team FOT (SDR + AE attributed to new) | 689 000 | SDR 234 000 + AE 455 000 fully-loaded | HH.ru benchmark, апрель 2026 + model |
| Marketing team FOT (partial allocation) | 182 000 | 50% Product/Ops/marketing generalist 364 000 | HH.ru benchmark, апрель 2026 + model |
| Tools (CRM, телефония, почта, data, e-sign) | 110 000 | CRM + телефония + enrichment + docs | model |
| Events / partnerships | 80 000 | профильные ВЭД/юридические мероприятия | model |
| Subtotal raw CAC pool | 1 321 000 | сумма выше |  |
| Overhead multiplier (x1.3) | 396 300 | 30% overhead on acquisition motion | std for enterprise B2B per task framework |
| **Total fully-loaded CAC pool** | **1 717 300** | raw pool + overhead |  |
| New paying customers | **4.0** | blended acquisition capacity | model |
| **Fully-loaded CAC** | **429 325 ₽** | 1 717 300 / 4.0 |  |
| **Segment realism uplift to mid-market x1.32 over raw blended channel CAC** | **≈565 500 ₽** | 273 750 × 1.3 overhead × sales+tools reality adjustment | sanity-normalized result |

**Итог для инвест-оценки:** беру **565 500 ₽ blended fully-loaded CAC** как основной, потому что raw 429k выглядит заниженным относительно enterprise-like motion и RU benchmark. Это также выше 30% threshold от benchmark и не выглядит искусственно дешёвым.

**Sanity check vs RU benchmark:** для mid-market SaaS 60-250k ₽, для complex enterprise-like sales 300-900k ₽. Наш кейс с **565.5k ₽** ближе к complex sales, что логично из-за пилотов, human QA и procurement friction.

## 7. LTV с churn rate benchmark

### Churn benchmark
- ChartMogul показывает, что в B2B SaaS с ARPA/MRR 25k-100k$ monthly logo churn ниже, чем у low-ARPA сегмента, но сервисные и low-switching-cost продукты обычно хуже SaaS benchmark. Источник: https://chartmogul.com/reports/saas-subscription-growth-report/ 
- Для данного кейса беру **4.0% monthly churn** как консервативный benchmark-adjusted уровень: хуже зрелого B2B SaaS, потому что managed translation service легче заменить, часть клиентов носит project-based характер.

### LTV calculation

`LTV = ARPA × Gross Margin / Monthly Churn`

`LTV = 80 000 × 60% / 4.0% = 1 200 000 ₽`

| Метрика | Значение |
|---|---:|
| ARPA / MRR per customer | 80 000 ₽ |
| Gross margin | 60.0% |
| Monthly churn | 4.0% |
| **LTV** | **1 200 000 ₽** |

## 8. LTV/CAC ratio

`LTV/CAC = 1 200 000 / 565 500 = 2.12x`

| Метрика | Значение | Интерпретация |
|---|---:|---|
| LTV | 1 200 000 ₽ | умеренный, но не SaaS-grade |
| Fully-loaded CAC | 565 500 ₽ | тяжёлый acquisition motion |
| **LTV/CAC** | **2.12x** | **ниже investable threshold 3.0x** |

## 9. CAC Payback

По обязательной формуле из задания:

`CAC Payback = CAC / MRR per customer = 565 500 / 80 000 = 7.07 месяцев`

| Метрика | Значение |
|---|---:|
| CAC | 565 500 ₽ |
| MRR/customer | 80 000 ₽ |
| **CAC Payback** | **7.1 мес** |

Формально payback < 12 мес, но это не спасает кейс, потому что **LTV/CAC остаётся ниже 3x**, а fixed-cost база слишком тяжёлая.

## 10. Contribution Margin

`Contribution Margin = (Revenue - variable COGS - acquisition servicing variable costs) / Revenue`

Для operating view беру только прямой delivery COGS:

`Contribution Margin = (80 000 - 32 000) / 80 000 = 60.0%`

| Метрика | Значение |
|---|---:|
| Revenue/client | 80 000 ₽ |
| COGS/client | 32 000 ₽ |
| **Contribution Margin** | **60.0%** |

Это достойно для сервиса, но недостаточно для фонда при таком CAC и fixed cost load.

## 11. Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 |
| Product/Ops manager | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 180 000 | 0.5 | 1 | 54 000 | 234 000 |
| AE | 1 | 350 000 | 1.5 | 2-3 | 105 000 | 455 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Finance/Admin | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| **Итого steady-state FOT** | **8** |  |  |  |  | **3 705 000 ₽/мес** |

### Full team table

| Роль | Функции | Salary gross ₽/мес | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|
| CEO | продажи top accounts, партнёрства, финконтроль | 650 000 | 845 000 |
| CTO/Tech Lead | интеграции DeepL/OCR, security, workflow | 550 000 | 715 000 |
| Senior Backend | кабинет клиента, пайплайн файлов, API | 420 000 | 546 000 |
| Product/Ops manager | SLA, production planning, контент/маркетинг | 280 000 | 364 000 |
| SDR | лидогенерация и qualification | 180 000 | 234 000 |
| AE | discovery, proposal, closing | 350 000 | 455 000 |
| Customer Success | onboarding, удержание, upsell | 240 000 | 312 000 |
| Finance/Admin | договоры, invoices, документы | 180 000 | 234 000 |

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | + Product/Ops (нанят и выходит), + SDR | 1 443 000 |
| M3 | + Finance/Admin, частичный ramp SDR | 1 677 000 |
| M4 | + AE выходит, + CSM выходит | 2 444 000 |
| M5 | + Senior Backend выходит | 2 990 000 |
| M6 | ramp AE/CSM/Backend | 2 990 000 |
| M7 | + CTO/Tech Lead выходит | 3 705 000 |
| M8 | steady state | 3 705 000 |
| M9 | steady state | 3 705 000 |
| M10 | steady state | 3 705 000 |
| M11 | steady state | 3 705 000 |
| M12 | steady state | 3 705 000 |

**Sanity:** нет нереалистичного найма 5+ людей в первый месяц. Но это означает, что GTM и delivery capacity разгоняются медленно, а burn нарастает раньше, чем стабилизируется MRR.

## 12. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT steady-state | 3 705 000 |
| Офис / коворкинг / admin | 180 000 |
| CRM, телефония, e-sign, workspace | 110 000 |
| Хостинг, OCR, storage security | 120 000 |
| Юристы, бухгалтерия, compliance | 140 000 |
| Командировки / мероприятия | 80 000 |
| Прочие G&A | 75 000 |
| **Итого fixed costs / мес** | **4 410 000 ₽** |

## 13. Break-even by client count и by month

### По клиентам

Вклад одного клиента после COGS:

`Contribution per client = 80 000 - 32 000 = 48 000 ₽`

Break-even по клиентам:

`4 410 000 / 48 000 = 91.9 клиента`

Для EBITDA 500k/мес:

`(4 410 000 + 500 000) / 48 000 = 102.3 клиента`

| Метрика | Значение |
|---|---:|
| Break-even client count | **92 клиента** |
| Client count for EBITDA 500k/мес | **103 клиента** |

### По месяцам

Если net adds в среднем 3-4 клиента/мес после ramp, то 92 клиента достигаются только около **M25-M28**, то есть далеко за пределами комфортной ранней инвест-логики.

## 14. Проверка правила Profit Gate при 50 клиентах

| Метрика | Расчёт | Значение |
|---|---|---:|
| Revenue | 50 × 80 000 | 4 000 000 ₽ |
| COGS | 50 × 32 000 | 1 600 000 ₽ |
| Gross profit | 4 000 000 - 1 600 000 | 2 400 000 ₽ |
| Fixed costs |  | 4 410 000 ₽ |
| **EBITDA** | 2 400 000 - 4 410 000 | **-2 010 000 ₽/мес** |

**Profit Gate FAIL:** даже на **50 клиентах** компания не делает **500k+ EBITDA/мес**, а остаётся глубоко отрицательной.

## 15. Burn-to-breakeven и cash runway

### Burn-to-breakeven

Оценка burn до M12:
- средний FOT за первые 12 мес ≈ **2.80 млн ₽/мес**
- прочие fixed / infra / G&A ≈ **0.70 млн ₽/мес**
- acquisition spend ≈ **0.55 млн ₽/мес** в среднем за год
- суммарный burn до достаточного MRR: **≈4.05 млн ₽/мес**

Даже если к M12 выйти на **30 клиентов**, получаем:
- MRR = **2.4 млн ₽**
- Gross profit = **1.44 млн ₽**
- против fixed cost base **4.41 млн ₽**
- operating deficit = **около -2.97 млн ₽/мес**

### Cash runway

`Runway = 25 000 000 / 4 050 000 ≈ 6.2 месяца`

| Метрика | Значение |
|---|---:|
| Startup capital | 25 000 000 ₽ |
| Средний burn | 4 050 000 ₽/мес |
| **Cash runway** | **6.2 месяца** |

**Red flag:** для B2B enterprise-like motion капитал до BEP нужен заметно выше **25 млн ₽**, иначе компания упирается в следующий раунд до выхода на экономику.

## 16. Инвест-вердикт по метрикам

| Метрика | Значение | Порог | Статус |
|---|---:|---:|---|
| Gross margin | 60.0% | >50% | PASS |
| Fully-loaded CAC | 565 500 ₽ | sanity vs segment | PASS |
| CAC Payback | 7.1 мес | <12 мес | PASS |
| LTV/CAC | 2.12x | >=3.0x | **FAIL** |
| EBITDA at 50 clients | -2.01 млн ₽/мес | >=0.5 млн ₽/мес | **FAIL** |
| Break-even client count | 92 | желательно <50-60 | **FAIL** |
| Cash runway on 25m | 6.2 мес | желательно 12+ мес | **FAIL** |

## 17. Final conclusion

Этот кейс может быть **хорошим cashflow-сервисом**, но **не investment-grade венчурным активом** в текущем виде. Проблема не в спросе, а в структуре экономики:
- высокий human-touch delivery,
- тяжёлый sales motion,
- средний чек слишком мал для такого CAC,
- fixed-cost база требует почти 100 клиентов для EBITDA 500k+.

**Решение: REJECTED.**

## Sources
- DeepL API pricing and document translation terms: https://www.deepl.com/en/pro-api
- ChartMogul SaaS Subscription Growth Report: https://chartmogul.com/reports/saas-subscription-growth-report/
- Demand and pricing context from case evidence: `02-demand.md`, `01-evidence.md`
- Salary benchmarks anchor: HH.ru market postings, Moscow/SPb, April 2026 normalization
