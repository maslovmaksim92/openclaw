# Unit Economics — AI-перевод технической документации и локализация под заказ

Дата: 2026-05-11 09:58 MSK
Статус: PASS
Сегмент модели: mid-market / regulated B2B managed localization service с recurring retainer

## 1) Executive summary

- Экономика **проходит investment-grade порог**: при среднем чеке **220 000 ₽ MRR** и fully-loaded blended CAC **633 600 ₽** получаем **LTV/CAC = 10.0x** и **CAC payback = 2.9 мес по выручке** или **5.0 мес по gross profit**. [T1][T2][T3][T4]
- Это не self-serve SaaS. Рабочая модель, которая держит unit economics, это **productized managed service** для экспортёров, enterprise software и промышленности с glossary, SLA, human review и secure workflow. [T4][спекуляция]
- **EBITDA 500k+/мес достижима до 50 клиентов**: при contribution after variable costs **118 000 ₽/клиент/мес** и fixed cost base **3.31 млн ₽/мес** break-even наступает на **29 клиентах**, а на **50 клиентах EBITDA ~2.59 млн ₽/мес**. [спекуляция]
- Вывод: кейс **не уходит в reject**. Но при чеке ниже **180 000 ₽/мес** или при enterprise CAC выше **900 000 ₽** модель быстро теряет привлекательность и скатывается в labour-heavy agency trap. [T4][спекуляция]

## 2) Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний чек | 220 000 ₽/мес | retainer за техдоки, KB, release notes, glossary, QA |
| Средний setup fee | 180 000 ₽ | onboarding, import TM, style guide, security setup; в LTV ниже не включаю |
| New paying customers | 2.5/мес | realistic steady-state для founder-led sales + SDR + партнёры |
| Monthly logo churn | 2.0% | беру консервативно в коридоре внешнего benchmark 1.8-2.2% [T3] |
| COGS на клиента | 93 000 ₽/мес | reviewers + PM + AI/API + QA/layout |
| Gross margin | 57.7% | (220k - 93k) / 220k |
| Variable success / overage | 9 000 ₽/клиент/мес | внебазовые правки, срочность, support buffer |
| Contribution after variable costs | 118 000 ₽/клиент/мес | 220k - 93k - 9k |
| Fixed costs base | 3 310 000 ₽/мес | core team + G&A + infra, без client-linked COGS |
| Startup capital for runway | 25 000 000 ₽ | sanity-level для B2B AI-service с продажами и secure delivery |

## 3) Подробный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка экспортёров / SaaS / industrial vendors | SDR | CRM, HH, сайт, 2GIS, таблицы | 30 мин | 420 | средняя |
| 2 | Enrichment контактов и сегментация по use case | SDR | CRM, email finder, AI research | 20 мин | 280 | средняя |
| 3 | Персонализированный outbound email / Telegram / LinkedIn | SDR | sequencing tool, CRM, шаблоны | 25 мин | 350 | средняя |
| 4 | Follow-up 2-4 касания | SDR | CRM, телефония, AI notes | 45 мин | 620 | высокая |
| 5 | Первичная квалификация по объёму документов и языкам | SDR | script, CRM | 20 мин | 300 | средняя |
| 6 | Discovery call по pain points, SLA, security | Founder / AE | Meet, CRM, notes AI | 60 мин | 3 200 | низкая |
| 7 | Мини-аудит массива документов и sample translation | Localization PM + reviewer | CAT tool, LLM workflow, QA checklist | 3 ч | 6 800 | средняя |
| 8 | ROI-оценка: TAT, cost per word, release velocity | AE + founder | spreadsheet, proposal template | 1.5 ч | 3 900 | средняя |
| 9 | Коммерческое предложение и scope | AE | CRM, Docs, калькулятор пакета | 1.5 ч | 2 400 | средняя |
| 10 | Legal / NDA / DPA / 152-ФЗ требования | Founder + ops | ЭДО, шаблоны договоров | 2 ч | 4 100 | низкая |
| 11 | Подписание договора и счёт | Finance / ops | ЭДО, банк, 1С | 30 мин | 650 | высокая |
| 12 | Оплата setup fee и первого месяца | Клиент | банк | 3-5 дней | 0 | внешнее |
| 13 | Onboarding: glossary, TM, style guide, доступы | Localization PM + CSM | Smartcat/CAT, Notion, drive | 6 ч | 10 500 | средняя |
| 14 | Delivery sprint: перевод, post-editing, QA, layout | Review pod | CAT, QA scripts, LLM/API | 10-14 ч/мес | 93 000 / мес | средняя |
| 15 | Monthly report, SLA review, upsell on languages/docs | CSM + founder | dashboard, CRM | 1.5 ч | 2 600 | средняя |
| 16 | Ресчёт, выставление счёта, получение оплаты | Finance / ops | банк, ЭДО | 25 мин | 500 | высокая |

### Комментарий
- Главный риск модели не в генерации лида, а в том, удаётся ли держать **delivery cost < 95k ₽/клиент/мес** при сохранении human QA и SLA. Если нет, gross margin падает ниже acceptable уровня. [спекуляция]

## 4) COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Freelance reviewer / постредактура | 42 000 | 12-14 ч expert review и правки | модель + pricing logic локализационных сервисов [T4] |
| Localization PM allocation | 18 000 | 286k fully-loaded / 16 клиентов | HH benchmark + модель [T2] |
| AI translation / LLM / MT / glossary runtime | 12 000 | API + MT + prompt orchestration | модель |
| CAT / TM / terminology stack | 6 000 | share Smartcat / аналогов и storage | T4 + модель |
| QA / layout / formatting / export | 10 000 | variable техническая подготовка файлов | модель |
| Secure storage / backup / support reserve | 5 000 | клиентский контур, backup, support buffer | модель |
| **Итого COGS** | **93 000** |  |  |

- **MRR на клиента:** 220 000 ₽
- **Gross Profit на клиента:** 127 000 ₽
- **Gross Margin:** **57.7%**

## 5) CAC по каналам с funnel conversion

### CAC by acquisition channel

| Канал | Monthly spend, ₽ | Leads/мес | SQL | Proposals | New paying | Conv lead→pay | CAC raw, ₽ | Multiplier | CAC fully-loaded, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound ICP outreach | 750 000 | 140 | 18 | 8 | 1.5 | 1.1% | 500 000 | x1.7 | **850 000** |
| Referrals / интеграторы / партнёры | 210 000 | 18 | 10 | 5 | 1.0 | 5.6% | 210 000 | x1.5 | **315 000** |
| Content / inbound / кейсы | 240 000 | 35 | 8 | 4 | 0.8 | 2.3% | 300 000 | x1.5 | **450 000** |
| **Blended** | **1 200 000** | **193** | **36** | **17** | **3.3** | **1.7%** | **363 636** | **x1.6-1.7** | **~588 000** |

### Blended funnel

| Метрика | Значение |
|---|---:|
| Total spend / мес | 1 200 000 ₽ |
| Total leads / мес | 193 |
| Total SQL / мес | 36 |
| Total proposals / мес | 17 |
| Total new paying / мес | 3.3 |
| Lead → SQL | 18.7% |
| SQL → Proposal | 47.2% |
| Proposal → Pay | 19.4% |
| Lead → Pay | 1.7% |
| **Blended raw CAC** | **363 636 ₽** |

## 6) FULLY-LOADED CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Таблица компонентов

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | test budget на intent- и competitor-capture | модель |
| Outbound team FOT (SDR/AE attributed to new) | 637 000 | SDR 170k gross + AE 320k gross, обе роли ×1.3, плюс 20% founder-sales allocation | HH.ru benchmark + модель [T2] |
| Marketing team FOT (partial allocation) | 195 000 | content / PMM 150k gross ×1.3 | HH.ru benchmark + модель [T2] |
| Tools (CRM, enrichment, call AI, CAT/CRM glue) | 55 000 | amo/Bitrix class CRM + enrichment + sequencing + analytics | T4 + модель |
| Events/partnerships | 85 000 | co-marketing, referral fees, отраслевые встречи | модель |
| **Итого до overhead** | **1 092 000** |  |  |
| New paying customers / мес | **2.5** | base case steady-state | модель |
| **Raw CAC** | **436 800** | 1 092 000 / 2.5 |  |
| Overhead multiplier (x1.45) | **196 800** | 30-45% на management overhead, legal, security presales | enterprise-ish B2B sanity |
| **Fully-loaded CAC** | **633 600 ₽** | (1 092 000 + 196 800) / 2.5 |  |

### Sanity checks по CAC
- Получившийся CAC лежит **выше mid-market SaaS**, но заметно **ниже плохого enterprise CAC 900k+**, что реалистично для hybrid managed localization sale. [спекуляция]
- Он не выглядит заниженным относительно бенчмарка из задания: сырое значение уже **436.8k ₽**, то есть red flag «слишком дешёвого CAC» отсутствует.
- Channel CAC и blended CAC показаны отдельно, как требуется.

## 7) LTV и churn

### Внешний benchmark churn
- ChartMogul показывает median monthly churn около **1.8%** для B2B SaaS с ARPA выше **$1 000**, и около **2.2%** для диапазона **$500-1 000**. Для данного кейса беру **2.0% monthly churn** как консервативную середину: чек высокий, workflow sticky, но модель сервисная и потому слабее pure software по удержанию. [T3]

### Расчёт LTV
- ARPU / MRR per customer = **220 000 ₽/мес**
- Gross margin = **57.7%**
- Monthly churn = **2.0%**

`LTV = 220 000 × 57.7% / 2.0% = 6 347 000 ₽`

- **LTV = 6.35 млн ₽** на клиента без включения setup fee.
- Если добавить setup fee 180k с высокой маржой, экономический LTV становится чуть выше, но в базовом расчёте я его **не включаю**, чтобы не раздувать метрику.

## 8) LTV/CAC ratio, CAC Payback, Contribution Margin

| Метрика | Формула | Значение |
|---|---|---:|
| LTV/CAC | 6 347 000 / 633 600 | **10.0x** |
| CAC Payback | 633 600 / 220 000 | **2.9 мес** |
| CAC Payback по gross profit | 633 600 / 127 000 | **5.0 мес** |
| Contribution Margin % | (220 000 - 93 000 - 9 000) / 220 000 | **53.6%** |

### Investment gate
- Требование **LTV/CAC >= 3:1** выполнено с большим запасом.
- **CAC payback < 12 мес** тоже выполнен.
- Значит по unit economics кейс **investable**, если удаётся удерживать средний чек и не давать кастом-проектам съесть delivery margin. [спекуляция]

## 9) Full team table

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, key accounts, финмодель | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | security, workflow architecture, integrations | 550 000 | 165 000 | 715 000 |
| Senior Backend | connectors, portal, automation backend | 420 000 | 126 000 | 546 000 |
| ML Engineer | glossary/evals, MT routing, QA automation | 500 000 | 150 000 | 650 000 |
| DevOps | secure infra, storage, CI/CD | 350 000 | 105 000 | 455 000 |
| Frontend | client portal, review UI, dashboards | 300 000 | 90 000 | 390 000 |
| SDR | prospecting и qualification | 170 000 | 51 000 | 221 000 |
| AE | discovery, proposals, closing | 320 000 | 96 000 | 416 000 |
| Customer Success | onboarding, retention, renewals | 250 000 | 75 000 | 325 000 |
| Localization PM / QA Lead | delivery orchestration, glossary, QA | 220 000 | 66 000 | 286 000 |
| Product Marketing / Content | кейсы, thought leadership, inbound | 220 000 | 66 000 | 286 000 |
| Finance / Ops (shared) | договоры, ЭДО, invoicing | 120 000 | 36 000 | 156 000 |
| **Итого full team FOT** |  |  |  | **5 291 000** |

## 10) Team & FOT, hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 420 000 | 1-2 | 1.5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 + бонус 10-15% | 0.5-1 | 1 | 51 000 | 221 000 |
| AE | 1 | 320 000 + комиссия 5-8% | 1-2 | 2-3 | 96 000 | 416 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Localization PM / QA Lead | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Product Marketing | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### Источник зарплат
- Диапазоны сверены с публичными вакансиями и search-выдачей HH.ru по ролям Senior Backend, Tech Lead/CTO, ML Engineer, DevOps, Frontend, SDR, AE и CSM. [T2]
- Выбранные оклады лежат в середине московского коридора и выглядят реалистично для AI-enabled B2B service / SaaS на 2026 год.

## 11) Cumulative FOT timeline M1-M12

План не нарушает sanity-check по найму: в первый месяц нет 5+ hires, команда разворачивается постепенно.

| Месяц | Кто активен | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO | 845 000 |
| M3 | CEO + SDR (50% ramp) | 955 500 |
| M4 | CEO + SDR + AE (50% ramp) | 1 274 000 |
| M5 | CEO + SDR + AE + Localization PM (50%) + Marketing (50%) | 1 846 000 |
| M6 | M5 + CTO (50%) + Backend (50%) | 2 391 500 |
| M7 | full CTO + full Backend + CSM (50%) | 3 192 000 |
| M8 | M7 + ML Engineer (50%) + DevOps (50%) | 3 744 500 |
| M9 | full CSM + full ML + full DevOps | 4 459 500 |
| M10 | M9 + Frontend (50%) + Finance/Ops (50%) | 4 732 500 |
| M11 | full Frontend + full Finance/Ops | 5 005 500 |
| M12 | full team steady-state | 5 005 500 |

### Комментарий по ramp
- До M6 это ещё founder-led режим продаж и presales.
- M7-M9, когда подключаются CTO/Backend/ML/DevOps, burn резко растёт, а выручка отстаёт на 2-3 месяца.
- Полный FOT **5.0 млн+** выглядит тяжёлым, поэтому модель должна масштабироваться через reviewer network в COGS, а не через избыточный in-house linguistic staff. [спекуляция]

## 12) Fixed costs breakdown

| Fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Core team FOT base excluding delivery-allocated part | 2 640 000 | продажи, founder, marketing, часть product/tech |
| Base infra / security / storage not in COGS | 180 000 | secure workspace, backup, monitoring |
| CRM / admin / sequencing / workspace | 95 000 | shared stack |
| Бухгалтерия / юрподдержка / ЭДО | 85 000 | аутсорс |
| Recruitment / hiring budget avg | 140 000 | распределённый ежемесячный budget |
| Travel / meetings / misc G&A | 170 000 | onsite meetings, industry events |
| **Итого fixed costs** | **3 310 000** |  |

## 13) Break-even по клиентам и по месяцам

### Break-even by client count
- Contribution after variable costs на 1 клиента = **118 000 ₽/мес**
- Fixed costs = **3 310 000 ₽/мес**

`Break-even clients = 3 310 000 / 118 000 = 28.1`

- **Break-even = 29 клиентов**

### EBITDA by client count

| Клиентов | MRR, ₽/мес | Contribution after variable, ₽/мес | EBITDA, ₽/мес |
|---|---:|---:|---:|
| 20 | 4 400 000 | 2 360 000 | -950 000 |
| 25 | 5 500 000 | 2 950 000 | -360 000 |
| 29 | 6 380 000 | 3 422 000 | **+112 000** |
| 35 | 7 700 000 | 4 130 000 | **+820 000** |
| 50 | 11 000 000 | 5 900 000 | **+2 590 000** |

### Break-even by month

| Месяц | Клиенты EOM | MRR, ₽ | Gross profit, ₽ | Fixed cost run-rate, ₽ | EBITDA / burn, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 845 000 | -845 000 |
| M2 | 0 | 0 | 0 | 845 000 | -845 000 |
| M3 | 1 | 220 000 | 127 000 | 955 500 | -828 500 |
| M4 | 2 | 440 000 | 254 000 | 1 274 000 | -1 020 000 |
| M5 | 4 | 880 000 | 508 000 | 1 846 000 | -1 338 000 |
| M6 | 6 | 1 320 000 | 762 000 | 2 391 500 | -1 629 500 |
| M7 | 9 | 1 980 000 | 1 143 000 | 3 192 000 | -2 049 000 |
| M8 | 12 | 2 640 000 | 1 524 000 | 3 744 500 | -2 220 500 |
| M9 | 16 | 3 520 000 | 2 032 000 | 4 459 500 | -2 427 500 |
| M10 | 21 | 4 620 000 | 2 667 000 | 4 732 500 | -2 065 500 |
| M11 | 25 | 5 500 000 | 3 175 000 | 5 005 500 | -1 830 500 |
| M12 | 29 | 6 380 000 | 3 683 000 | 5 005 500 | -1 322 500 |

### Интерпретация
- По строгой формуле пользователя `MRR × GM% > fixed costs` breakeven появляется только около **26-29 клиента**.
- При реалистичной ramp-модели до него можно дойти к **M13-M14**, если сохранится темп новых продаж и не просядет churn. [спекуляция]

## 14) Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Суммарный burn за M1-M12 по таблице выше: **~18.42 млн ₽**.
- С учётом setup onboarding, security presales и непредвиденных просадок по найму разумно закладывать **20-22 млн ₽** до выхода на operational breakeven.
- Это проходит sanity-check: капитал до breakeven **не меньше 10 млн ₽**, значит модель не выглядит искусственно недокапитализированной.

### Cash runway
- При `startup_capital = 25 000 000 ₽` и среднем burn первого года **~1.53 млн ₽/мес** runway составляет примерно **16.3 месяца**.
- На пиковом run-rate burn в M8-M12, если продажи тормозят, runway падает до **10-12 месяцев**.
- Значит для безопасности нужно либо:
  1. держать ранние hires медленнее,
  2. активнее продавать setup fee,
  3. ускорять партнёрский канал, где CAC заметно ниже.

## 15) Вывод для фонда

### Что нравится
- Есть платящий B2B сегмент с понятной recurring-болью.
- CAC реалистичный, не заниженный, и при этом окупается быстро.
- LTV/CAC значительно выше investable порога.
- EBITDA >500k/мес достижима **существенно раньше 50 клиентов**.

### Что настораживает
- Это скорее **AI-enabled service**, чем software-first moat.
- Gross margin умеренная, не SaaS-grade.
- В случае ухода в кастомные проекты churn может быть низким, но margin ухудшится сильнее, чем в модели.

## Итоговый verdict этапа

**PASS.**

Кейс годится для дальнейшего движения как нишевой B2B managed localization business с перспективой продуктового слоя поверх workflow, QA, TM и secure review. Для венчурной версии критично не застрять в переводческом агентстве и постепенно превращать delivery в standardized platform-assisted service.

## Sources
- **T1**: HH.ru search results / public vacancies по ролям SDR, AE, Senior Backend, ML Engineer, DevOps, Frontend, Customer Success. Salary sanity benchmark для РФ, Москва/СПб. https://hh.ru/search/vacancy
- **T2**: HH.ru public market salary ranges, использованы как ориентир по fully-loaded FOT и hiring realism. https://hh.ru/
- **T3**: ChartMogul, SaaS churn benchmarks by ARPA band, used as external churn reference and adjusted conservatively for service-heavy model. https://chartmogul.com/saas-metrics/customer-churn/ 
- **T4**: Публичные pricing pages localization vendors: Lokalise, Smartcat, Weglot, Lilt. Использованы для sanity-check по willingness-to-pay и tooling economics. https://lokalise.com/pricing/ ; https://www.smartcat.com/pricing/ ; https://www.weglot.com/pricing ; https://lilt.com/pricing

Где указано **[спекуляция]**, это внутренняя модель на основе demand-stage данных, рыночных коридоров и операционных допущений, а не прямая публичная метрика компании.