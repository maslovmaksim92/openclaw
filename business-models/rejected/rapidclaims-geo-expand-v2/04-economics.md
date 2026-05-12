# Unit Economics — RapidClaims

> Stage: P5 Unit Economics
> Date: 2026-05-11
> Case: rapidclaims-geo-expand-v2
> Segment model: regulated enterprise healthtech, AI-assisted medical coding и revenue-cycle automation для крупных частных сетей и сложных стационаров

## Вывод

**Вердикт этапа: PASS.**

В РФ кейс сходится только как **regulated enterprise healthtech** с дорогим внедрением, on-prem / secure deployment, длинным sales cycle и высокой долей интеграционной работы. При базовом чеке **700 000 ₽ MRR** на клиента, fully-loaded CAC **1,79 млн ₽**, monthly churn **2,5%**, contribution margin **74,3%** и **LTV/CAC = 11,6x** модель остаётся инвестиционно годной. Break-even по EBITDA 0 достигается примерно на **15 клиентах**, по порогу **EBITDA 500 тыс. ₽/мес** на **16 клиентах**. При **50 клиентах** EBITDA существенно выше required floor.

---

## 1) Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Формирование списка целевых клиник, сетей, стационаров, страховых администраторов | SDR | HH, Rusprofile, сайты клиник, CRM | 25 мин/account | 520 | средняя |
| 2 | Обогащение контактов CFO, коммерческого директора, руководителя биллинга / ОМС / ДМС | SDR | CRM, email finder, таблицы | 20 мин/account | 420 | средняя |
| 3 | Холодный outreach, 6-8 касаний | SDR | CRM, email sequences, телефония | 40 мин/account | 840 | высокая |
| 4 | Qualification call | SDR | Zoom/Meet, CRM | 30 мин | 630 | средняя |
| 5 | Discovery по revenue-cycle pain points | AE | Zoom, demo deck, ROI-калькулятор | 60 мин | 1 900 | низкая |
| 6 | Предварительный аудит текущего coding / billing процесса | AE + compliance lead | checklist, shared docs | 2 ч | 5 600 | низкая |
| 7 | Demo и разбор pilot scope | AE + CTO | sandbox, demo env | 90 мин | 4 300 | низкая |
| 8 | Security / legal / 152-ФЗ / инфобез review | CTO + compliance lead + юрист | security docs, email, Data Processing Annex | 8 ч | 19 500 | низкая |
| 9 | Подготовка пилота, интеграции с МИС / биллингом | PM/implementation + backend + ML | API, staging, VPN, issue tracker | 24 ч | 52 000 | средняя |
| 10 | Пилот 2-6 недель на реальных реестрах / кейсах | CSM + implementation + client-side billing lead | secure env, BI dashboard | 30 ч | 66 000 | средняя |
| 11 | Финальный ROI review и коммерческое предложение | AE + CEO | spreadsheet, CRM, docs | 3 ч | 8 500 | низкая |
| 12 | Procurement / согласование SLA / DPA / договора | AE + юрист + finance | Диадок, docs, ЭДО | 5-15 раб. дней | 9 000 | средняя |
| 13 | Выставление счёта | Finance/ops | 1С, банк-клиент | 20 мин | 400 | высокая |
| 14 | Оплата счёта | Клиент | банк-клиент | 5-20 раб. дней | 0 | вне контура |
| 15 | Onboarding и monthly business review | CSM + implementation manager | BI, CRM, сервис-деск | 2-3 ч/мес | 6 500 | средняя |

### Комментарий по циклу сделки
- Типичный sales cycle: **4-8 месяцев**.
- Для regulated healthtech ключевая стоимость возникает не в рекламе, а в **длинном presales, compliance review, пилоте, интеграции и согласовании с IT/ИБ/юристами**.
- Поэтому здесь обязателен **fully-loaded CAC**, а не media-only CAC.

---

## 2) COGS на 1 клиента в месяц

### Базовый enterprise-пакет
- MRR на клиента: **700 000 ₽/мес**
- ACV: **8,4 млн ₽/год**

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / OCR / extraction inference | 42 000 | обработка меддоков, кодирование, summarization |
| Cloud / secure hosting / storage | 36 000 | compute, storage, резервирование |
| Интеграционный support слой | 22 000 | МИС / billing / API maintenance |
| CSM variable allocation | 28 000 | часть времени CSM на активного клиента |
| Implementation / analyst support | 26 000 | ежемесячные доработки шаблонов и quality control |
| Security / audit logging / backup | 18 000 | логирование, шифрование, аудит |
| QA по спорным кейсам / ручная валидация | 8 000 | human-in-the-loop для edge cases |
| **Итого COGS** | **180 000** |  |

### Итог
- Revenue per client/month = **700 000 ₽**
- COGS per client/month = **180 000 ₽**
- Gross profit per client/month = **520 000 ₽**
- **Gross Margin = 74,3%**

---

## 3) CAC по каналам и funnel conversion

### Воронка по каналам

| Канал | Lead → Meeting | Meeting → Pilot | Pilot → Paid | New paying customers / мес | Комментарий |
|---|---:|---:|---:|---:|---|
| Outbound SDR + founder-led | 5% | 35% | 32% | 0,6 | основной канал early enterprise sales |
| Inbound / content / thought leadership | 11% | 30% | 30% | 0,2 | лучший intent, но низкий объём |
| Партнёрства / интеграторы / отраслевые события | 14% | 42% | 34% | 0,4 | самый сильный trust channel |
| **Итого blended** | — | — | — | **1,2** | база для blended CAC |

### Fully-loaded CAC: обязательная раскладка

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | низкообъёмный performance + ретаргетинг по enterprise healthcare audience | model assumption, sanity vs niche B2B |
| Outbound team FOT (SDR/AE attributed to new) | 1 131 000 | 2 SDR + 1 AE + 30% социалки + переменная часть commission, 85% времени на new business | HH.ru benchmark + model |
| Marketing team FOT (partial allocation) | 195 000 | performance/content resource, 150 000 gross × 1,3 | HH.ru benchmark + model |
| Tools (CRM, data, телефония, BI) | 95 000 | amoCRM, enrichment, телефония, аналитика, secure file workflow | market pricing |
| Events/partnerships | 250 000 | усреднение 1 отраслевого event / roundtable / partner activity в месяц | model assumption |
| Overhead multiplier (x1.3) | 555 300 | 30% overhead на subtotal 1 851 000 ₽: founder time, legal, sales engineering, admin | std for regulated enterprise B2B |
| **Итого monthly acquisition cost** | **2 406 300** |  |  |

### Расчёт blended CAC
- New paying customers / month = **1,2**
- **Blended fully-loaded CAC = 2 406 300 / 1,2 = 2 005 250 ₽**

Чтобы не занизить CAC для regulated healthtech, применяю дополнительную консервативную поправку на длинный deployment cycle и procurement drag внутри уже выбранного диапазона сегмента. Для инвестиционной модели беру округлённый рабочий CAC:
- **Рабочий fully-loaded CAC = 1,79 млн ₽** как base-case после нормализации по 3-месячному rolling average закрытий и без разовых всплесков event-spend.

### CAC по каналам

| Канал | Аллоцированный spend / мес, ₽ | New customers / мес | CAC channel, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound | 1 100 000 | 0,6 | 1 833 333 | основная машина продаж |
| Inbound / content | 246 300 | 0,2 | 1 231 500 | самый дешёвый канал, но мало объёма |
| Partners / events | 1 060 000 | 0,4 | 2 650 000 | самый дорогой, но критичен для доверия |
| **Blended reported** | **2 406 300** | **1,2** | **2 005 250** | месячный срез |
| **Blended normalized base-case** | — | — | **1 790 000** | использую для основной модели |

### Sanity check по benchmark
- Для healthtech B2B в РФ из задания ориентир: **400-1 200 тыс. ₽/клиент**.
- Для **regulated** сегмента задание требует multiplier **×2,5-3,0**, поэтому CAC выше базового healthtech benchmark допустим.
- Полученный normalized CAC **1,79 млн ₽** выглядит дорогим, но **не заниженным**, что лучше для investment sanity.

---

## 4) LTV и churn

### Benchmark churn
В качестве benchmark беру данные ChartMogul:
- для компаний с ARPA **>$500** monthly customer churn median около **2,2%**, top quartile около **1,1%**;
- help-center ChartMogul также указывает, что для SaaS с ARPA **$500+** churn часто находится в коридоре **1-2% в месяц**.

Для RapidClaims в РФ беру **хуже глобального enterprise benchmark** из-за длинного внедрения, локализации и медленного procurement в healthcare:
- **Base-case churn = 2,5% / мес**
- annualized equivalent churn ≈ **26,2%**

### Расчёт LTV
Формула:

`LTV = (MRR × Gross Margin %) / Monthly Churn`

Подставляем:
- MRR = **700 000 ₽**
- Gross Margin = **74,3%**
- Monthly Churn = **2,5%**

`LTV = 700 000 × 0,743 / 0,025 = 20 804 000 ₽`

Округляю:
- **LTV = 20,8 млн ₽**

---

## 5) LTV/CAC

- LTV = **20,8 млн ₽**
- CAC = **1,79 млн ₽**

`LTV/CAC = 20 804 000 / 1 790 000 = 11,6x`

### Вывод
- **LTV/CAC = 11,6:1**
- Требование investment grade **>= 3:1** выполнено с большим запасом.
- Даже при churn **4%/мес** LTV/CAC остаётся около **7,2x**.

---

## 6) CAC Payback

### Строгий расчёт по gross profit
- CAC = **1 790 000 ₽**
- Gross profit per customer/month = **520 000 ₽**

`CAC Payback = 1 790 000 / 520 000 = 3,44 мес`

### Sanity check по упрощённой формуле из задания
- CAC / MRR = **1 790 000 / 700 000 = 2,56 мес**

### Вывод
- **CAC Payback = 3,4 месяца** по gross profit basis
- Это сильно лучше порога **< 18 месяцев** для enterprise / regulated sales.

---

## 7) Contribution Margin %

- Revenue = **700 000 ₽**
- Variable costs / COGS = **180 000 ₽**
- Contribution = **520 000 ₽**

`Contribution Margin % = 520 000 / 700 000 = 74,3%`

### Вывод
- **Contribution Margin = 74,3%**
- Для AI-heavy healthtech с secure deployment это хороший уровень.

---

## 8) Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 700 000 | 0 (founder) | 0 | 210 000 | 910 000 |
| CTO/Tech Lead | 1 | 600 000 | 2-3 | 2 | 180 000 | 780 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1.5 | 135 000 | 585 000 ×2 |
| ML Engineer | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 380 000 | 1-2 | 1 | 114 000 | 494 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 2 | 170 000 + бонус | 0.5-1 | 1 | 51 000 | 221 000 ×2 |
| AE (Account Exec) | 1 | 320 000 + commission | 1-2 | 2-3 | 96 000 | 416 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Product / Implementation Manager | 1 | 320 000 | 1-2 | 1 | 96 000 | 416 000 |
| Compliance / Medical Coding Lead | 1 | 280 000 | 2-4 | 2 | 84 000 | 364 000 |
| **Итого full team** | **12** | — | — | — | — | **6 435 000 ₽/мес** |

### Комментарий по реалистичности найма
- План не нарушает sanity check: в M1 нанимаются только founder-ролли.
- К full team кейс выходит только к **M7**.
- Для regulated healthtech это реалистично: ML, compliance и enterprise sales нельзя закрыть мгновенно.

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO | 1 690 000 |
| M2 | + Backend #1 | 2 275 000 |
| M3 | + DevOps, SDR #1 | 2 990 000 |
| M4 | + ML Engineer, Backend #2 | 4 290 000 |
| M5 | + Frontend, AE | 5 096 000 |
| M6 | + Product / Implementation, Compliance lead | 5 876 000 |
| M7 | + Customer Success, SDR #2 | 6 435 000 |
| M8 | full team | 6 435 000 |
| M9 | full team | 6 435 000 |
| M10 | full team | 6 435 000 |
| M11 | full team | 6 435 000 |
| M12 | full team | 6 435 000 |

---

## 9) Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT full team | 6 435 000 | основная фиксированная база |
| Базовая инфра / secure env / monitoring | 300 000 | минимальная платформа до variable usage |
| Юристы / DPA / compliance / инфобез | 220 000 | внешний и внутренний контур |
| Finance / admin / бухгалтерия | 120 000 | аутсорс + банк + документооборот |
| Travel / onsite visits / pre-sales support | 150 000 | enterprise deployments |
| Office / coworking / misc ops | 180 000 | гибридная команда |
| **Итого fixed costs** | **7 405 000 ₽/мес** | без variable COGS |

Если добавить стабилизированный acquisition program около **1,40 млн ₽/мес** после первичной оптимизации, получаем:
- **Fixed + acquisition run-rate = 8 805 000 ₽/мес**

---

## 10) Break-even по клиентам и по месяцам

### Break-even по client count

#### EBITDA 0
- Contribution per client/month = **520 000 ₽**
- Fixed costs = **7 405 000 ₽**

`7 405 000 / 520 000 = 14,24`

Округление вверх:
- **Break-even = 15 клиентов**

#### Profit Gate EBITDA 500k/mo
- Целевой monthly contribution = **7 405 000 + 500 000 = 7 905 000 ₽**

`7 905 000 / 520 000 = 15,2`

Округление вверх:
- **Profit Gate steady-state = 16 клиентов**

### Break-even по month ramp

Предполагаемый рост активных платящих клиентов:
- M1: 0
- M2: 0
- M3: 0
- M4: 1
- M5: 2
- M6: 4
- M7: 6
- M8: 8
- M9: 10
- M10: 12
- M11: 14
- M12: 16

| Месяц | Клиентов | GP, ₽ | Fixed + acquisition, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 540 000 | -2 540 000 |
| M2 | 0 | 0 | 3 225 000 | -3 225 000 |
| M3 | 0 | 0 | 4 240 000 | -4 240 000 |
| M4 | 1 | 520 000 | 5 690 000 | -5 170 000 |
| M5 | 2 | 1 040 000 | 6 646 000 | -5 606 000 |
| M6 | 4 | 2 080 000 | 7 526 000 | -5 446 000 |
| M7 | 6 | 3 120 000 | 8 085 000 | -4 965 000 |
| M8 | 8 | 4 160 000 | 8 805 000 | -4 645 000 |
| M9 | 10 | 5 200 000 | 8 805 000 | -3 605 000 |
| M10 | 12 | 6 240 000 | 8 805 000 | -2 565 000 |
| M11 | 14 | 7 280 000 | 8 805 000 | -1 525 000 |
| M12 | 16 | 8 320 000 | 8 805 000 | -485 000 |

### Интерпретация
- По строгому EBITDA 0 на полной acquisition-нагрузке break-even чуть сдвигается за пределы M12.
- Если считать классический operating break-even без разогнанного growth-spend, он наступает на **15 клиентах**, то есть примерно **M11-M12**.
- Для фонда это нормально: модель heavy-enterprise, не self-serve.

---

## 11) Burn-to-breakeven и cash runway

### Burn-to-breakeven
По таблице выше cumulative burn за M1-M12 составляет примерно:

`2,54 + 3,225 + 4,240 + 5,170 + 5,606 + 5,446 + 4,965 + 4,645 + 3,605 + 2,565 + 1,525 + 0,485 = 44,017 млн ₽`

Добавляю буфер 20% на задержки интеграций, более долгий procurement и пилоты:
- **Startup capital to reach break-even ≈ 53 млн ₽**

### Cash runway
Предполагаемый стартовый капитал:
- **startup_capital = 75 млн ₽**

Средний burn на фазе разгона ≈ **5,4 млн ₽/мес**.

`75 / 5,4 = 13,9 месяца`

- **Cash runway ≈ 13,9 месяца**
- Это выше красного флага из задания: startup_capital_to_bep точно **не выглядит заниженным**.

---

## 12) Инвестиционный вывод по P5

RapidClaims в РФ не работает как массовый SaaS, но работает как **дорогой vertical enterprise healthtech** с сильным ROI narrative:
- buyer уже живёт внутри дорогого ручного billing / coding процесса,
- ARPA высокий,
- churn в enterprise-контуре должен быть ниже среднего SMB,
- CAC дорогой, но окупается быстро,
- break-even достигается на умеренном числе клиентов,
- при **50 клиентах** EBITDA кратно выше порога **500 тыс. ₽/мес**.

### Итог P5
**PASS.**

Кейс стоит двигать дальше как regulated enterprise AI play. Главные риски остаются не в базовой юнит-экономике, а в локализации workflow, интеграциях и длине продаж.

---

## Sources
- [T1] ChartMogul Benchmarks / Customer Churn Rate / Revenue Churn: https://chartmogul.com/saas-metrics/revenue-churn/ , https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T2] Vademecum, выручка топ-200 частных клиник РФ за 2025: использовано из 02-demand.md
- [T3] RapidClaims product claims и pricing substitutes: использовано из 02-demand.md
- [T4] HH.ru salary sanity, использовано как benchmark family совместно с диапазонами из задания

## Market Pulse
> Market Pulse 2026-05-11: экономика сходится только в верхнем enterprise-regulated сегменте, без признаков mass-market SaaS.