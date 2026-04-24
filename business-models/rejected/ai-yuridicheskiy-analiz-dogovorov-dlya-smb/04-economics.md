---
stage: unit-economics
case: ai-yuridicheskiy-analiz-dogovorov-dlya-smb
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

# 04-economics

## Кейс
AI-first юридический анализ и redline типовых договоров для SMB в РФ, модель монетизации: managed subscription с AI-первичным разбором и human legal QA.

## Executive summary
**Итог: НЕ investment grade.**

- Базовая модель для расчёта: **60 000 ₽ MRR на клиента** за пакет до 40 документов в месяц, SLA 1 рабочий день, human-in-the-loop.
- **COGS на клиента: 21 800 ₽/мес**, gross margin = **63,7%**.
- **Contribution margin after variable acquisition/servicing: 58,3%**.
- **Blended fully-loaded CAC: 477 000 ₽**.
- **LTV: 1 365 000 ₽**, при месячном churn **2,8%** и contribution profit **38 200 ₽/клиент/мес**.
- **LTV/CAC = 2,86x**, это **ниже инвестиционного порога 3,0x**.
- **CAC Payback = 7,95 мес** по формуле CAC / MRR на клиента, что формально в норме для mid-market B2B, но не компенсирует слабое отношение LTV/CAC.
- Даже при **50 клиентах** модель даёт около **-2 780 000 ₽ EBITDA/мес**, то есть порог Profit Gate не пройден.

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Целевой сегмент | SMB / lower mid-market РФ | 20-500 сотрудников, регулярный договорный поток |
| ARPA / MRR на клиента | 60 000 ₽/мес | середина между low-end legal service и team subscription из 02-demand |
| Документов в пакете | 40 / мес | типовой SMB volume |
| Средний churn | 2,8% / мес | взят как mid-market B2B benchmark, см. источники [T4][inference] |
| New paying customers | 1,5 / мес | реалистично для founder-led B2B legal sales |
| Startup capital | 18 000 000 ₽ | для расчёта runway |
| CAC segment multiplier | x1,6 | mid-market B2B по условию задания |

## 2. Подробный бизнес-процесс от лида до оплаты

| Шаг | Роль | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---|
| 1. Захват inbound/outbound лида | SDR | amoCRM, Telegram, email, landing | 20 мин | 500 | средняя |
| 2. Квалификация по ICP/BANT | SDR | amoCRM, чек-лист ICP | 30 мин | 750 | средняя |
| 3. Discovery call | AE / founder | Zoom/Meet, Notion | 45 мин | 2 200 | низкая |
| 4. Сбор 2-3 тестовых договоров | Клиент + AE | secure upload, cloud storage | 1 день cycle time | 400 | средняя |
| 5. AI-first разбор и red flags | AI pipeline | OCR, LLM, RAG, rules engine | 10 мин machine time | 180 | высокая |
| 6. Юридический QA и redline | Legal ops / senior юрист | Word/OnlyOffice, clause playbook | 2,5 ч | 3 000 | низкая |
| 7. Демо результата и pilot proposal | AE / founder | Zoom, proposal doc | 1 ч | 2 900 | низкая |
| 8. Безопасность/согласование данных | Founder + tech lead | NDA, DPA, security FAQ | 3 дня cycle time | 2 500 | низкая |
| 9. Коммерческое предложение и договор | AE + юрист | шаблон договора, ЭДО | 2 ч | 3 200 | средняя |
| 10. Счёт и оплата | Finance ops | банк-клиент, ЭДО | 30 мин | 600 | высокая |
| 11. Онбординг workspace и playbooks | CSM + legal ops | Notion, knowledge base | 3 ч | 4 200 | средняя |
| 12. Ежемесячная обработка пакета | AI + legal ops + CSM | LLM stack, helpdesk | 40 документов / мес | 21 800 | средняя |

### Вывод по процессу
- Бутылочное горлышко не inference, а **legal QA + presale**.
- Воронка требует нескольких ручных касаний, поэтому raw CAC нельзя считать только от рекламного бюджета.

## 3. COGS на клиента в месяц

| Статья COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM/OCR/inference | 1 800 | ~45 ₽ на документ x 40 | [inference] |
| Storage, security, infra | 900 | облако, хранение файлов, резерв | [inference] |
| Legal QA | 12 000 | 10 ч/мес x 1 200 ₽ внутренней cost/hour | [T2][inference] |
| Customer success / support | 4 500 | ~2,5 ч/мес x 1 800 ₽ | [T2][inference] |
| Onboarding amortization | 1 800 | 4 200 ₽ / 2,3 мес average retention start | [inference] |
| Billing / ЭДО / прочее | 800 | банк, ЭДО, сервисы | [inference] |
| **Итого COGS** | **21 800** |  |  |

### Gross margin
- Revenue per client = **60 000 ₽/мес**
- COGS per client = **21 800 ₽/мес**
- **Gross profit = 38 200 ₽/мес**
- **Gross margin = 63,7%**

## 4. CAC по каналам и funnel conversion

### Funnel by channel
| Канал | Leads/мес | SQL | Demo | Pilot | New paying | Lead→pay conversion |
|---|---:|---:|---:|---:|---:|---:|
| Контент + SEO | 30 | 12 | 8 | 4 | 1,0 | 3,3% |
| Платный performance | 45 | 10 | 6 | 3 | 0,5 | 1,1% |
| Outbound / founder-led | 140 | 18 | 10 | 5 | 0,7 | 0,5% |
| Партнёры / referrals | 8 | 5 | 4 | 3 | 0,8 | 10,0% |
| **Всего blended** | **223** | **45** | **28** | **15** | **3,0** raw / **1,5** net steady-state | **0,7% net** |

### Fully-loaded CAC, обязательная таблица
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый performance budget | [inference] |
| Outbound team FOT (SDR attributed to new) | 195 000 | 150 000 gross + 30% взносы | [T2][inference] |
| Marketing team FOT (partial allocation) | 90 000 | 300 000 gross marketer x 30% x 23% времени на acquisition | [T2][inference] |
| AE / founder sales allocation | 170 000 | доля sales time на new logo | [T2][inference] |
| Tools (CRM, prospecting, телефония, ЭДО) | 45 000 | amoCRM + телефония + парсинг/рассылки | [inference] |
| Events / partnerships | 30 000 | small offline/partner activity | [inference] |
| Subtotal raw acquisition cost | 650 000 | сумма строк выше |  |
| Overhead multiplier | 390 000 | raw CAC pool x 0,6 для mid-market B2B => итоговый множитель x1,6 | условие задания |
| **Fully-loaded CAC pool** | **1 040 000** | 650 000 x 1,6 |  |
| **New paying customers / мес** | **2,18 raw** / **1,5 net** | conservative steady-state | [inference] |
| **Blended fully-loaded CAC** | **477 000 ₽** | 1 040 000 / 2,18 = 477 000 |  |

### CAC по каналу
| Канал | Channel spend, ₽/мес | New paying / мес | CAC channel, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Контент + SEO | 140 000 | 1,0 | 140 000 | самый здоровый канал, но медленный ramp |
| Платный performance | 180 000 | 0,5 | 360 000 | приемлемо только как тестовый объём |
| Outbound | 480 000 | 0,7 | 686 000 | дорого из-за длинного цикла и ручных касаний |
| Партнёры | 90 000 | 0,8 | 113 000 | лучший CAC, но объём ограничен |
| **Blended** | **1 040 000** | **2,18** | **477 000** | fully-loaded |

### Sanity check по CAC
- Для complex B2B legal workflow **477 000 ₽ CAC** попадает в диапазон enterprise/mid-market sanity и явно не выглядит заниженным.
- Значение заметно выше self-serve SaaS, что логично из-за demo, pilot, security review и legal согласований.

## 5. LTV и churn

### Churn benchmark
- Для B2B SaaS нормальным диапазоном часто считают **3-8% monthly** для SMB и существенно ниже для enterprise. Для данного кейса я беру **2,8% monthly** как оптимистичный lower mid-market benchmark с human service layer. [T4][inference]

### LTV calculation
- MRR per client = **60 000 ₽**
- Contribution profit per client per month = **38 200 ₽**
- Churn rate = **2,8% / мес**
- Lifetime = **1 / 0,028 = 35,7 мес**
- **LTV = 38 200 x 35,7 = 1 365 000 ₽**

## 6. LTV/CAC
- **LTV/CAC = 1 365 000 / 477 000 = 2,86x**
- Порог investment grade по заданию: **>= 3,0x**
- **Итог: ниже инвестиционного порога.**

## 7. CAC Payback
- Формула по заданию: **CAC Payback = CAC / MRR_per_customer**
- **477 000 / 60 000 = 7,95 месяца**
- Это лучше базового лимита <12 месяцев, но payback в одиночку не спасает модель при слабом LTV/CAC.

## 8. Contribution Margin %

Для contribution margin вычитаю COGS и переменную acquisition/support layer, отнесённую к действующему клиенту.

| Показатель | ₽/клиент/мес |
|---|---:|
| Revenue | 60 000 |
| COGS | -21 800 |
| Variable servicing reserve | -1 500 |
| Variable sales/retention reserve | -1 700 |
| **Contribution profit** | **35 000** |

- **Contribution Margin % = 35 000 / 60 000 = 58,3%**

## 9. Team & FOT

### Полная таблица команды
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder-sales | продажи, партнёры, fundraising | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | продукт, архитектура, безопасность | 550 000 | 165 000 | 715 000 |
| Senior Backend | backend, integrations | 420 000 | 126 000 | 546 000 |
| ML Engineer | OCR/RAG/LLM orchestration | 500 000 | 150 000 | 650 000 |
| Legal Ops / senior юрист | QA redline, playbooks | 250 000 | 75 000 | 325 000 |
| SDR | outbound qualification | 150 000 | 45 000 | 195 000 |
| AE | demos, pilot, closing | 280 000 | 84 000 | 364 000 |
| Customer Success | onboarding, retention | 220 000 | 66 000 | 286 000 |
| Finance/ops part-time | документооборот, счёт, банк | 90 000 | 27 000 | 117 000 |
| **Итого** |  |  |  | **3 978 000** |

### Таблица найма, обязательная
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 420 000 | 2 | 1,5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 3 | 2 | 150 000 | 650 000 |
| DevOps | 0 | 0 | - | - | - | 0 |
| Frontend | 0 | 0 | - | - | - | 0 |
| SDR | 1 | 150 000 + бонус | 1 | 1 | 45 000 | 195 000 |
| AE | 1 | 280 000 + комиссия | 2 | 3 | 84 000 | 364 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Legal Ops / senior юрист | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Finance/ops part-time | 0,5 | 90 000 | 1 | 0,5 | 27 000 | 117 000 |

### Salary benchmark note
- Зарплатные вилки выше находятся внутри рыночных диапазонов HH/ru tech hiring для Москвы и СПб по senior SWE, team lead, ML, SDR, AE и customer-facing ролям. [T2][inference]

### Cumulative FOT timeline M1-M12
| Месяц | Кто в штате | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 780 000 | founder-led validation |
| M2 | CEO, SDR, Legal Ops, finance/ops 0.5 | 1 417 000 | первые наймы реалистичны |
| M3 | + Customer Success, CTO | 2 418 000 | CTO только выходит |
| M4 | + Backend, AE | 3 328 000 | AE ещё в ramp |
| M5 | + ML Engineer | 3 978 000 | полная core-команда |
| M6 | все | 3 978 000 | steady-state |
| M7 | все | 3 978 000 | steady-state |
| M8 | все | 3 978 000 | steady-state |
| M9 | все | 3 978 000 | steady-state |
| M10 | все | 3 978 000 | steady-state |
| M11 | все | 3 978 000 | steady-state |
| M12 | все | 3 978 000 | steady-state |

## 10. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 3 978 000 | core team |
| Office / coworking / admin | 120 000 | гибридный режим |
| Core infra reserve | 150 000 | dev/test/security/monitoring |
| Legal / бухгалтерия / audit | 90 000 | внешние сервисы |
| Software stack internal | 110 000 | Notion, Jira, CRM seats, support stack |
| Misc / travel / contingency | 80 000 | запас |
| **Total fixed cost / мес** | **4 528 000** |  |

## 11. Break-even

### Break-even по количеству клиентов
- Contribution profit per client = **35 000 ₽/мес**
- Fixed cost = **4 528 000 ₽/мес**
- **Break-even clients = 4 528 000 / 35 000 = 129,4**, округляю до **130 клиентов**

### Break-even по месяцу
Консервативный ramp новых платящих клиентов: 0, 1, 2, 4, 6, 8, 10, 12, 15, 18, 21, 24.

| Месяц | Активные клиенты на конец месяца | MRR, ₽ | Contribution profit, ₽ | EBITDA after fixed cost, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | -1 140 000 |
| M2 | 1 | 60 000 | 35 000 | -1 592 000 |
| M3 | 3 | 180 000 | 105 000 | -2 463 000 |
| M4 | 7 | 420 000 | 245 000 | -3 283 000 |
| M5 | 13 | 780 000 | 455 000 | -4 073 000 |
| M6 | 21 | 1 260 000 | 735 000 | -3 793 000 |
| M7 | 31 | 1 860 000 | 1 085 000 | -3 443 000 |
| M8 | 43 | 2 580 000 | 1 505 000 | -3 023 000 |
| M9 | 58 | 3 480 000 | 2 030 000 | -2 498 000 |
| M10 | 76 | 4 560 000 | 2 660 000 | -1 868 000 |
| M11 | 97 | 5 820 000 | 3 395 000 | -1 133 000 |
| M12 | 121 | 7 260 000 | 4 235 000 | -293 000 |

**Вывод:** даже к M12 компания ещё не в безубытке. Точка безубыточности достигается только около **M13-M14**, если рост не срывается.

## 12. Burn-to-breakeven и runway
- Кумулятивный burn до M12 ≈ **27,6 млн ₽**. [inference]
- Burn-to-breakeven с учётом M13-M14 оцениваю в **29-31 млн ₽**.
- При **startup_capital = 18 млн ₽** runway получается примерно **6,6-7,2 месяца**, что недостаточно до фактического break-even.
- Для более реалистичного прохождения до B/E нужен стартовый капитал не меньше **30-35 млн ₽**.

## 13. Profit Gate check

### Проверка при 50 клиентах
- Revenue = **3 000 000 ₽/мес**
- Contribution profit = **1 750 000 ₽/мес**
- Fixed cost = **4 528 000 ₽/мес**
- **EBITDA = -2 778 000 ₽/мес** по contribution approach
- Даже если считать мягче, через gross profit 50 x 38 200 = 1 910 000 ₽, всё равно **ниже 500 000 ₽ EBITDA**.

### Финальный вывод
1. **LTV/CAC = 2,86x**, ниже investable threshold **3,0x**.
2. **При 50 клиентах EBITDA < 500 000 ₽/мес**.
3. Нужный капитал до безубыточности слишком высокий для текущей traction-модели.

**Вердикт: REJECTED.**

## Источники
- [T1] 02-demand.md по кейсу `ai-yuridicheskiy-analiz-dogovorov-dlya-smb`, внутренний артефакт: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-yuridicheskiy-analiz-dogovorov-dlya-smb/02-demand.md
- [T2] HH.ru search pages для salary sanity: CTO https://hh.ru/search/vacancy?text=cto , Tech Lead https://hh.ru/search/vacancy?text=tech%20lead%20python , Senior Backend https://hh.ru/search/vacancy?text=senior%20backend%20python , ML Engineer https://hh.ru/search/vacancy?text=ml%20engineer , SDR https://hh.ru/search/vacancy?text=sdr , Account Executive https://hh.ru/search/vacancy?text=account%20executive , Customer Success https://hh.ru/search/vacancy?text=customer%20success
- [T3] Public pricing benchmarks already validated in 02-demand: Destra Legal https://destralegal.ru , Paxton AI https://www.paxton.ai/pricing , Genie AI https://www.genieai.co/pricing
- [T4] Baremetrics, SaaS churn benchmarks: https://baremetrics.com/blog/what-is-a-good-churn-rate ; Corporate Finance Institute, SaaS metrics overview: https://corporatefinanceinstitute.com/resources/valuation/saas-metrics/

Все числа, кроме публичных прайсов и рыночных диапазонов, являются расчётной моделью analyst estimate на базе кейса и указанных benchmark sources.
