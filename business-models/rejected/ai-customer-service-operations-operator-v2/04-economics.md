# 04-economics — Unit Economics

## Кейс
AI Customer Service Operations Operator

## Дата расчёта
2026-04-20, Europe/Moscow

## Итог Program 5
**FAIL**

Кейс подтверждает спрос и willingness-to-pay, но на investment fund уровне модель не проходит Profit Gate из-за слишком низкой contribution margin при service-heavy delivery и слишком дорогого enterprise-like CAC.

Ключевые метрики base case:
- **ARPA / MRR на клиента:** 300 000 ₽/мес
- **COGS:** 230 000 ₽/клиент/мес
- **Contribution Margin:** **23,3%**
- **Contribution profit:** **70 000 ₽/клиент/мес**
- **Blended fully-loaded CAC:** **1 322 000 ₽**
- **Churn rate:** **3,5%/мес**
- **LTV:** **2 000 000 ₽**
- **LTV/CAC:** **1,51x**
- **CAC Payback:** **4,4 мес по MRR** и **18,9 мес по contribution profit**
- **Fixed costs:** **5 747 000 ₽/мес**
- **Break-even:** **83 клиента для EBITDA=0**, **90 клиентов для EBITDA=500k/mo**
- **EBITDA при 50 клиентах:** **-2 247 000 ₽/мес**

## 1. ICP и ценовая модель
Целевой клиент: mid-market / enterprise компании с 20-100+ агентами поддержки, уже использующие helpdesk/contact center stack и готовые платить за внедрение AI-слоя, governance, QA, optimisation и managed operations.

Принятый base-case pricing:
- setup fee: не закладываю в core economics, чтобы не маскировать слабую recurring economics;
- retainer: **300 000 ₽/мес**;
- средний контракт: **3,6 млн ₽ ARR**.

Почему это enterprise-like motion, а не SMB:
1. ACV существенно выше **500 000 ₽/год**;
2. обычно нужны 2-4 discovery/presale касания;
3. часто появляется pilot/security/legal step до оплаты;
4. buyer committee, как правило, включает support lead + ops + IT.

## 2. Детальный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP, enrichment и приоритизация аккаунтов | SDR, Growth | hh.ru, CRM, Apollo/аналог, таблицы | 10 ч | 28 000 | Средняя |
| 2 | Первый outbound / paid capture / inbound qualification | SDR | email sequencer, CRM, формы, коллтрекинг | 22 ч | 61 000 | Средняя |
| 3 | Qualification call и booking discovery | SDR, AE | CRM, календарь, AI note-taker | 8 ч | 31 000 | Средняя |
| 4 | Discovery по pain points, SLA, volume, stack | AE | Zoom, Notion, Miro | 12 ч | 58 000 | Низкая |
| 5 | Presale-аудит текущей поддержки и базовая ROI-модель | AE, CTO/Tech Lead | helpdesk sandbox, spreadsheets | 18 ч | 116 000 | Низкая |
| 6 | Solution design: intents, KB, routing, escalation map | CTO/Tech Lead, Senior Backend | Miro, LLM workspace, docs | 24 ч | 156 000 | Низкая |
| 7 | Пилот / proof-of-value до оплаты | CTO/Tech Lead, Backend, CSM | Zendesk/Freshdesk, API, dashboards | 32 ч | 184 000 | Низкая |
| 8 | Security / procurement / legal согласование | AE, CEO | e-sign, DPA/MSA шаблоны, CRM | 14 ч | 73 000 | Низкая |
| 9 | Финальное коммерческое и счёт | AE, CEO | CRM, billing, шаблоны КП | 6 ч | 26 000 | Средняя |
| 10 | Onboarding и запуск первого invoice cycle | CSM, Backend | PM tool, billing, helpdesk, monitoring | 16 ч | 71 000 | Средняя |

**Итого прямой труд и инструменты на 1 выигранного клиента до первого платежа: ~804 000 ₽.**

Это уже само по себе выше, чем «лёгкий SaaS CAC», и подтверждает, что перед нами не self-serve, а дорогой service-assisted enterprise sale.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / AI usage / voice / reranking | 35 000 | inference + prompt/versioning + guardrails |
| Cloud, storage, observability | 18 000 | baseline infra + логирование + мониторинг |
| Helpdesk/connectors/sandbox licenses | 12 000 | тестовые стенды, интеграционные коннекторы |
| Delivery labor: CSM + solution ops + QA share | 145 000 | регулярный разбор диалогов, tuning, релизы |
| QA / annotation / audits | 14 000 | ручная проверка сложных кейсов и knowledge updates |
| Variable admin / payment / communication | 6 000 | связь, мелкие подрядчики, финоперации |
| **Итого COGS** | **230 000** |  |

### Валовая экономика
- Revenue: **300 000 ₽/мес**
- COGS: **230 000 ₽/мес**
- Contribution profit: **70 000 ₽/мес**
- Contribution Margin: **23,3%**

Для investment-grade SaaS/AI это слишком низко: большая часть value съедается ручным delivery.

## 4. CAC by channel с funnel conversion

### 4.1 Channel funnels
| Канал | Верх воронки / мес | Discovery | SQL / Pilot | New paying customers / мес | Raw CAC, ₽ | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Paid search / performance | 120 лидов | 18 | 6 | 0,6 | 400 000 | 880 000 |
| Outbound SDR/AE | 900 аккаунтов | 24 | 8 | 0,5 | 1 050 000 | 2 310 000 |
| Партнёрства / events | 18 intro | 8 | 3 | 0,3 | 800 000 | 1 760 000 |
| Content / referral / founder-led inbound | 30 лидов | 10 | 4 | 0,3 | 1 120 000 | 2 464 000 |
| **Blended** | — | — | — | **1,7** | **780 000** | **1 322 000** |

### 4.2 Fully-loaded CAC: обязательная раскладка
| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ / VK / search) | 180 000 | base performance budget | внутренняя модель P5 |
| Outbound team FOT (SDR/AE attributed to new) | 481 000 | SDR 224k + 60% AE 257k | hh.ru salary benchmark, 20.04.2026 |
| Marketing team FOT (partial allocation) | 286 000 | 1 growth marketer fully on acquisition | hh.ru salary benchmark, 20.04.2026 |
| Tools (CRM, sequencer, enrichment, analytics) | 95 000 | CRM + outreach + data tools | внутренняя модель P5 |
| Events / partnerships | 150 000 | small sponsor/events/partner revshare budget | внутренняя модель P5 |
| Overhead multiplier (x1.3) | 358 000 | 30% на acquisition ops overhead | стандарт fully-loaded CAC |
| **Итого raw+overhead / мес** | **1 550 000** |  |  |

Дальше применяю **enterprise CAC multiplier = 2,2 / 1,3 = 1,69x поверх raw+overhead**, потому что чек **3,6 млн ₽ ARR**, есть pilot/security/legal step и длинный пресейл.

- Enterprise-adjusted acquisition cost / мес = **2 247 000 ₽**
- New paying customers / мес = **1,7**
- **Blended fully-loaded CAC = 2 247 000 / 1,7 = 1 322 000 ₽**

### Sanity check по RU benchmark
User benchmark для complex B2B / enterprise SaaS в РФ: **300-900k ₽+**, а для regulated/сложных циклов ещё выше. Наш blended CAC **1,322 млн ₽** находится **выше комфортного диапазона**, но это логично для service-led модели с пилотом и дорогим solutioning. Это не выглядит заниженной оценкой, наоборот, ближе к реалистичной.

## 5. LTV и churn

### Benchmark source по churn
Согласно **ChartMogul Help Center**, для SaaS с **ARPA $500+** типичный customer churn находится на уровне **1-2% в месяц**. 

Для данного кейса я не беру этот benchmark напрямую, а ставлю **3,5%/мес**, потому что:
1. это не pure software, а service-led operator layer;
2. часть value может быть internalized клиентом после 3-6 месяцев;
3. высокий platform risk: Zendesk / Freshworks / Fin / AI-native vendors могут закрывать часть use case нативно.

То есть **3,5%/мес** это осознанно более жёсткая и реалистичная инвестиционная поправка к SaaS benchmark.

### LTV calculation
Формула: **LTV = contribution profit per month / churn rate**

- Contribution profit = **70 000 ₽/мес**
- Churn = **3,5%/мес**
- **LTV = 70 000 / 0,035 = 2 000 000 ₽**

## 6. LTV/CAC ratio
- **LTV = 2 000 000 ₽**
- **Fully-loaded CAC = 1 322 000 ₽**
- **LTV/CAC = 1,51x**

### Вывод
Investment-grade порог по задаче: **минимум 3:1**.

Фактический результат: **1,51x**, то есть **сильно ниже investable уровня**.

## 7. CAC Payback
Обязательная sanity-формула по задаче:
- **CAC Payback = CAC / MRR_per_customer = 1 322 000 / 300 000 = 4,4 месяца**

Но для фонда важнее payback по валовому вкладу:
- **CAC Payback по contribution profit = 1 322 000 / 70 000 = 18,9 месяца**

### Вывод
- по формальному MRR payback цифра выглядит терпимо;
- по реальной unit economics payback уже **слишком длинный**;
- это ещё один признак, что gross margin слишком низкий.

## 8. Team & FOT

### 8.1 Полная таблица команды
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|---------|-------------------:|------------------:|-----------------------:|
| CEO / Founder | продажи, fundraise, key accounts | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | solution architecture, AI ops | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | integrations, workflow engine | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | production support, data flows | 450 000 | 135 000 | 585 000 |
| ML Engineer | prompts, evals, routing quality | 500 000 | 150 000 | 650 000 |
| DevOps | infra, observability, security | 350 000 | 105 000 | 455 000 |
| Frontend | ops UI / internal tooling | 300 000 | 90 000 | 390 000 |
| SDR | outbound | 172 000 | 52 000 | 224 000 |
| AE | enterprise sales | 330 000 | 99 000 | 429 000 |
| Customer Success | onboarding, retention, QA loop | 250 000 | 75 000 | 325 000 |
| Growth Marketer | paid, content, partner pipeline | 220 000 | 66 000 | 286 000 |
| **Итого FOT fully-loaded** |  |  |  | **5 489 000 ₽/мес** |

### 8.2 Hiring realism table
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | +30% | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | +30% | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | +30% | 585 000 each |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | +30% | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | +30% | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | +30% | 390 000 |
| SDR | 1 | 172 000 | 0,5 | 1 | +30% | 224 000 |
| AE | 1 | 330 000 | 1,5 | 2,5 | +30% | 429 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | +30% | 325 000 |

### 8.3 Cumulative FOT timeline M1-M12
Реалистичный найм без нарушения правила time-to-hire:

| Месяц | Кто в штате | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + CTO | 1 560 000 |
| M3 | + Senior Backend #1 | 2 145 000 |
| M4 | + AE | 2 574 000 |
| M5 | + SDR + DevOps | 3 253 000 |
| M6 | + Senior Backend #2 + Growth | 4 124 000 |
| M7 | + ML Engineer | 4 774 000 |
| M8 | + Frontend + CSM | 5 489 000 |
| M9 | полный штат | 5 489 000 |
| M10 | полный штат | 5 489 000 |
| M11 | полный штат | 5 489 000 |
| M12 | полный штат | 5 489 000 |

План не нарушает sanity check: нет найма 5+ человек в первый месяц, но даже при таком аккуратном сценарии к M8 компания уже приходит к FOT почти **5,5 млн ₽/мес**.

## 9. Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Core FOT fixed portion | 5 327 000 | весь штат, кроме части CSM уже вынесенной в variable delivery |
| Fixed software stack | 160 000 | CRM, PM, knowledge, analytics, security |
| Baseline cloud / infra | 80 000 | минимальная постоянная инфраструктура |
| Legal / finance / accounting | 90 000 | бухгалтерия, договоры, сопровождение |
| Office / admin / misc | 90 000 | связь, HR ops, прочее |
| **Итого fixed costs** | **5 747 000 ₽/мес** |  |

## 10. Break-even по клиентам и по месяцам

### Break-even by client count
Формула: **fixed costs / contribution profit per client**

- EBITDA = 0: **5 747 000 / 70 000 = 82,1**, округляю до **83 клиентов**
- EBITDA = 500k/mo: **(5 747 000 + 500 000) / 70 000 = 89,2**, округляю до **90 клиентов**

### Проверка при 50 клиентах
- Revenue: **15 000 000 ₽/мес**
- Variable COGS: **11 500 000 ₽/мес**
- Contribution profit: **3 500 000 ₽/мес**
- Fixed costs: **5 747 000 ₽/мес**
- **EBITDA = -2 247 000 ₽/мес**

**Profit Gate: FAIL**, потому что даже при **50 клиентах** компания не выходит на **+500k EBITDA/mo**.

### Break-even by month
Реалистичная траектория активных клиентов для service-heavy GTM:
- M3: 1 клиент
- M6: 4 клиента
- M9: 8 клиентов
- M12: 12 клиентов
- M18: 24 клиента
- M24: 38 клиентов

При этой траектории **break-even не достигается даже к M24**. Чтобы добраться до 83-90 клиентов, нужен либо radically higher price, либо radical automation delivery, либо сильное снижение CAC. В текущем виде модель в разумный инвестиционный горизонт не входит.

## 11. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Даже если взять умеренный план продаж, cumulative burn до теоретического EBITDA break-even превышает **60 млн ₽**. Для service-led компании без сильного moat это слишком тяжёлый путь.

### Cash runway
Допущение: **startup_capital = 40 млн ₽**.

При burn первых 12 месяцев порядка **3,5-4,5 млн ₽/мес** runway составляет примерно **9-11 месяцев**. То есть без дополнительного капитала компания, скорее всего, не доживает до масштаба, на котором экономика начинает улучшаться.

### Sanity verdict по capital needs
Для enterprise B2B AI-оператора `startup_capital_to_bep < 10M ₽` был бы нереалистичен. Здесь наоборот, реалистичная потребность существенно выше, что подтверждает слабость модели для фонда.

## 12. Почему модель не инвестиционного качества
1. **Слишком низкая contribution margin, 23,3%**. Это больше похоже на агентский delivery business, чем на compounding AI software.
2. **Enterprise-like CAC, 1,322 млн ₽**. Длинный цикл сделки съедает возврат капитала.
3. **LTV/CAC = 1,51x**, что сильно ниже required **3:1**.
4. **50 клиентов не дают +500k EBITDA/mo**. Это прямой провал Profit Gate.
5. Даже хороший спрос не спасает модель, если каждый клиент приносит слишком мало валового вклада после обязательного human layer.

## 13. Вывод Program 5
**FAIL.**

На уровне одного клиента revenue выглядит привлекательно, но после fully-loaded CAC, realistic hiring и service-heavy COGS инвестиционная экономика не сходится.

Рекомендация пайплайна:
- записать кейс в **REJECTED**;
- причина reject: **company EBITDA > 500k/mo не достижима даже при 50 клиентах в текущей модели**, а **LTV/CAC остаётся всего 1,51x**.

## Источники
- 02-demand кейса: Zendesk pricing, Freshdesk pricing, Usedesk pricing, Chat2Desk tariffs
- Zendesk pricing: https://www.zendesk.com/pricing/
- Chat2Desk тарифы: https://chat2desk.com/baza-znanij/billing/tarifyi-chat2desk
- Fin pricing / positioning: https://www.fin.ai/ ; https://www.fin.ai/pricing
- ChartMogul churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- hh.ru, Account Executive: https://hh.ru/vacancies/account_executive
- hh.ru, SDR / account executive search results: https://hh.ru/vacancies/account_executive/polnaya_zanyatost
- hh.ru, Senior Backend Engineer: https://hh.ru/vacancies/senior-backend-engineer
- hh.ru, Senior Backend Developer: https://hh.ru/vacancies/senior-backend-developer
- hh.ru, Customer Success Manager: https://hh.ru/vacancies/customer-success-manager
- hh.ru, DevOps: https://hh.ru/vacancies/devops
- hh.ru, Senior DevOps: https://hh.ru/vacancies/senior-devops

Примечание: значения зарплат, churn и CAC multiplier в этой модели частично являются **аналитическими допущениями поверх benchmark-источников**, а не прямыми quote-цифрами из одного источника. Это сделано сознательно для conservative investment test.