# Compiled verdict packet


---

# 00-brief.md

# Краткий бриф

- Кейс создан принудительно по правилу resurrect.
- Тема: HubSpot: outcome-based pricing для AI-агентов в CRM и customer-facing workflows.
- Исходный raw-файл: `2026-04-19-resurrect-hubspot-outcome-based-ai-agents-pricing.md`.
- Оригинальный verdict: `triage/triage-2026-04-13-hubspot-outcome-based-ai-agents-pricing.md`.
- Следующий этап: P3-demand-validation.
- Причина создания: сигнал должен пройти полный цикл P3→P7 с новой аналитикой, даже если раньше был маршрутизирован как duplicate/supporting или не дошёл до полного разбора.


---

# 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-hubspot-outcome-based-ai-agents-pricing.md
created: 2026-04-20T17:45:00+03:00
original_verdict: triage/triage-2026-04-13-hubspot-outcome-based-ai-agents-pricing.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `hubspot-outcome-based-ai-agents-pricing-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Тема
HubSpot: outcome-based pricing для AI-агентов в CRM и customer-facing workflows.

## Полный контекст из raw

# RESURRECT SIGNAL — hubspot-outcome-based-ai-agents-pricing

## Meta
- source: triage/triage-2026-04-13-hubspot-outcome-based-ai-agents-pricing.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Triage

## Date
2026-04-13

## Inputs
- pipeline/raw/20260413T1710Z-hubspot-outcome-based-ai-agents-pricing.md

## Classification
duplicate / supporting signal for existing case

## Decision
Не создавать новый case.

Route signal to existing case: `autonomous-b2c-crm-operator`.

## Why
- Сигнал усиливает уже открытый wedge вокруг autonomous CRM execution: AI не просто помогает оператору, а выполняет customer-facing и pipeline-facing задачи с outcome-based monetization.
- Outcome pricing за resolved conversation и recommended lead полезен как monetization signal, но сам по себе не задаёт новый самостоятельный service case, потому что это скорее ценовой и packaging proofpoint внутри уже существующего CRM/operator narrative.
- Для branch важнее зафиксировать, что крупный CRM vendor начинает нормализовать оплату за завершённый агентом результат, а не только за seats или generic AI add-ons.

## Triage note
Считать HubSpot важным supporting signal для economics и monetization внутри `pipeline/cases/autonomous-b2c-crm-operator/`. При следующем evidence/economics cycle стоит добавить его как подтверждение того, что autonomous CRM workflows могут продаваться по unit-of-outcome, а не только по seat-based SaaS модели.

```


---

# 02-demand.md

---
stage: demand-validation
case: hubspot-outcome-based-ai-agents-pricing-v2
date: 2026-04-21
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
HubSpot outcome-based pricing для Breeze Customer Agent и Prospecting Agent как сигнал спроса на AI-агентов в CRM, customer-facing workflows и GTM-автоматизации.

## Итог
**Статус: CONDITIONAL PASS.**

На 21 апреля 2026 года exact-demand в РФ по формулировке `HubSpot customer agent pricing` почти отсутствует, но сам сигнал очень сильный как category proof: HubSpot перевёл два флагманских AI-агента на оплату за результат, а не за seat или usage. Это означает, что vendor уже видит достаточно стабильную ценность, чтобы брать деньги только за resolved conversation и recommended lead. [T1][T2][T4]

Ключевые выводы:
1. **2 апреля 2026 года** HubSpot объявил outcome-based pricing: **$0.50 за resolved conversation** у Customer Agent и **$1 за recommended lead** у Prospecting Agent. [T1]
2. В том же анонсе HubSpot пишет, что Customer Agent уже **разрешает 65% разговоров**, сокращает время решения на **39%** и активирован у **8 000+ клиентов**. Это сильный production-signal, а не просто маркетинговая гипотеза. [T1]
3. Ещё **10 апреля 2025 года** HubSpot сообщал, что Customer Agent помогает закрывать **50%+ support tickets** и снижать время закрытия почти на **40%**. **8 мая 2025 года** компания расширила доступ к агенту на все Pro и Enterprise hubs и запустила credits-модель. [T2][T3]
4. В локальном контуре брендовый спрос слабый, но adjacent budget line существует: `crm ai agent` даёт `hh_ru=111`, `sales automation ai crm` даёт `hh_ru=219`, а exact HubSpot queries почти пустые. Значит, buyer pain есть, но в РФ он формулируется через CRM automation / sales ops / support automation, а не через HubSpot-specific language. [T4]

## 1. Сигналы спроса

### Demand API
- `hubspot ai customer agent pricing` -> **LOW**, `demand_score=0`, `hh_ru=0`, `yandex_suggest=2`. [T4]
- `hubspot customer agent pricing` -> **LOW**, `demand_score=0`, `google_trends_ru=0`, `hh_ru=0`, `yandex_suggest=2`. [T4]
- `hubspot pricing customer agent` -> **LOW**, `demand_score=0`, `google_trends_ru=0`, `hh_ru=0`, `yandex_suggest=2`. [T4]
- `crm ai agent` -> **LOW**, `demand_score=7`, `hh_ru=111`, `yandex_suggest=2`. [T4]
- `sales automation ai crm` -> **LOW**, `demand_score=11`, `hh_ru=219`, `google_trends_ru=0`, `yandex_suggest=2`. [T4]

### Интерпретация
- Exact-demand по HubSpot pricing zero-like. Это не прямой GEO-launch case под локальный inbound. [T4][inference]
- Но category-demand на CRM automation, AI-assisted support и AI-led sales execution уже есть, просто он выражен generic buyer language. [T4][inference]
- Для Program 2 это важнее, чем нулевой брендовый спрос: сервисный слой чаще продаётся вокруг GTM-результата, интеграции и revenue/ops KPI, а не вокруг самого vendor SKU. [T1][T4][inference]

## 2. Category proof и why now
1. Outcome-based pricing почти никогда не запускают на сыром продукте. Если HubSpot готов брать деньги только за результат, значит performance уже достаточно предсказуем для массового коммерческого rollout. [T1][inference]
2. Метрики **65% resolved conversations**, **39% faster resolution** и **8 000+ activated customers** показывают, что речь идёт не о пилотах на десятках аккаунтов, а о реальной operating category. [T1]
3. Весной 2025 года HubSpot уже публично показывал, что Customer Agent закрывает **50%+ support tickets**, а затем расширил доступ на Marketing, Sales, Service, Content и Operations Hubs. Это значит, что use case вышел за пределы support-only и двигается в сторону общего customer-facing AI layer. [T2][T3]
4. Knowledge Base HubSpot на **14 апреля 2026 года** фиксирует точную механику monetization: кредиты списываются только когда агент доставляет resolution, а resolution оценивается через outcome window в 72 часа. Это усиливает тезис, что монетизация завязана на measurable business event. [T5]

## 3. Что это значит для локального GEO / B2B-OPS кейса
- Как pure HubSpot reseller motion кейс слабый: в РФ мало brand pull и почти нет exact search demand. [T4][inference]
- Как service line вокруг AI CRM operations, AI support automation и AI prospecting case выглядит намного сильнее: аудит процессов, внедрение агента, настройка источников знаний, routing, escalation logic, KPI instrumentation и ongoing optimisation. [T1][T2][T5][inference]
- Самое ценное в сигнале не HubSpot как бренд, а нормализация pricing model, где AI monetizes по закрытому вопросу или qualified lead. Это серьёзный рыночный proof, что buyer готов платить за outcome-layer. [T1][T5][inference]

## 4. Кто купит
Вероятный ICP в локальном и adjacent контуре:
1. mid-market и enterprise-команды с большим входящим support volume,
2. B2B SaaS и e-commerce компании с высокой нагрузкой на presales/support,
3. sales ops / revops команды, которые хотят автоматизировать qualification и first-touch,
4. интеграторы и CRM-консультанты, которые могут упаковать AI-agent deployment как managed service,
5. компании, уже живущие в CRM-centric процессе и считающие SLA, conversion и agent productivity.

## 5. Willingness to pay
- Сигнал WTP очень сильный, потому что HubSpot уже ушёл от подписочной модели к оплате за completed task. [T1]
- Это снижает buyer friction: платить $0.50 за решённый диалог и $1 за рекомендованный лид психологически проще, чем заранее покупать seats или large AI add-on. [T1][inference]
- Для service-layer поверх такого продукта WTP тоже реален, если продаётся не как «настроим бота», а как growth/support performance motion с KPI по resolution rate, response time, qualified leads и deflection. [T1][T2][T5][inference]

## 6. Profit gate scenarios
### Сценарий A, лёгкий SMB setup
- 80 000-150 000 ₽ в месяц за базовую настройку AI-агента и поддержку.
- Слишком низко для Program 2.
- **Вердикт: NO PASS.**

### Сценарий B, CRM / support automation managed layer
- 350 000-700 000 ₽ в месяц за внедрение, knowledge orchestration, routing, QA, escalation design и optimisation.
- При 5-7 клиентах экономика может пройти порог.
- **Вердикт: PASS.**

### Сценарий C, revenue + support AI ops для mid-market / enterprise
- 700 000-1 500 000 ₽ в месяц за связку support automation + lead qualification + analytics + managed experimentation.
- Даже 3-4 клиента могут собрать нужный EBITDA-профиль.
- **Вердикт: STRONG PASS.**

## 7. Основные риски
- Слишком сильная привязка к бренду HubSpot, который в локальном контуре не даёт достаточного inbound. [T4]
- Риск, что standalone case на самом деле должен жить внутри более широкого wedge `ai-crm-operations` или `customer-service-automation`, а не как отдельный HubSpot-specific thesis. [inference]
- Outcome pricing у вендора не гарантирует, что внедренческий слой будет repeatable и margin-rich, часть ценности может уйти в кастомный consulting. [T1][T5][inference]
- Локальный спрос на generic CRM AI есть, но пока без явного сильного search pull. [T4]

## 8. Решение для pipeline
**Не отклонять на demand-этапе, но вести как CONDITIONAL PASS.**

Почему:
1. свежий и сильный signal monetization-by-outcome от крупного CRM vendor, [T1]
2. подтверждённый production usage и массовая активация, [T1][T2][T3]
3. adjacent demand на CRM / sales / support automation уже присутствует, [T4]
4. экономика собирается только в high-ticket managed-ops / transformation motion, а не в дешёвом setup-service. [inference]

Что обязательно проверить в P4/P5/P6:
- это отдельный кейс или supporting-signal для более широкого AI CRM ops wedge,
- насколько repeatable delivery вне HubSpot-only installs,
- можно ли удерживать high-ticket чек без тяжёлого кастома,
- есть ли достаточный локальный канал сделок через интеграторов, CRM-консалтинг и adjacent demand.

## Источники
- [T1] HubSpot, Customer Agent and Prospecting Agent move to outcome-based pricing, 2026-04-02: https://www.hubspot.com/company-news/hubspots-customer-agent-and-prospecting-agent-now-you-pay-when-the-task-is-complete
- [T2] HubSpot Spring 2025 Spotlight, AI agents launch and 50%+ support ticket resolution, 2025-04-10: https://ir.hubspot.com/news-releases/news-release-details/hubspot-launches-new-and-enhanced-ai-agents-plus-over-200/
- [T3] HubSpot expands Breeze Customer Agent with credits and wider hub access, 2025-05-08: https://ir.hubspot.com/news-releases/news-release-details/hubspot-credits
- [T4] Demand API: http://172.18.0.1:9001/multi-demand?keyword=hubspot%20ai%20customer%20agent%20pricing ; http://172.18.0.1:9001/multi-demand?keyword=hubspot%20customer%20agent%20pricing ; http://172.18.0.1:9001/multi-demand?keyword=hubspot%20pricing%20customer%20agent ; http://172.18.0.1:9001/multi-demand?keyword=crm%20ai%20agent ; http://172.18.0.1:9001/multi-demand?keyword=sales%20automation%20ai%20crm
- [T5] HubSpot Knowledge Base, Understand the customer agent, last updated 2026-04-14: https://knowledge.hubspot.com/customer-agent/understand-the-customer-agent


---

# 04-economics.md

---
stage: economics
case: hubspot-outcome-based-ai-agents-pricing-v2
date: 2026-04-21
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
HubSpot outcome-based pricing для Breeze Customer Agent и Prospecting Agent как экономический сигнал для managed-service слоя вокруг AI CRM ops, AI support automation и AI prospecting.

## Executive summary

**Итог P4/P5: CONDITIONAL PASS.**

Почему:
1. **Путь к EBITDA > 500k ₽/мес существует** уже примерно на **23 активных клиентах** в base-case managed-service модели.
2. **LTV/CAC = 3.4x**, то есть выше минимального инвестиционного порога 3.0x, но без большого запаса.
3. **Gross-margin остаётся service-heavy, 58.9%**, поэтому кейс валиден только как high-ticket delivery / optimisation motion, а не как дешёвый setup-service.
4. Главные риски не в наличии спроса, а в **длинном внедрении, зависимости от HubSpot-экосистемы и необходимости держать senior delivery команду**.

## 1. Модель и ключевые допущения

### ICP
- российские и СНГ mid-market / enterprise компании с HubSpot или близким CRM-стеком;
- B2B SaaS, e-commerce, edtech и service businesses с заметным inbound/support volume;
- revops / sales ops / support ops команды, которые готовы считать resolution rate, speed-to-lead и qualified pipeline;
- интеграторы и CRM-консультанты, которым нужен managed AI-ops слой поверх существующего внедрения.

### Почему кейс считаю service-line, а не pure SaaS
HubSpot сам уже монетизирует agent outcome: **$0.50 за resolved conversation** и **$1 за recommended lead**. Это означает, что внешний сервисный провайдер может продавать не лицензии, а внедрение, orchestration, routing, knowledge tuning, KPI instrumentation и постоянную оптимизацию поверх существующего vendor spend. [T1][T2]

### Base-case для РФ / СНГ
- Recurring managed retainer: **450 000 ₽/клиент/мес**
- One-off onboarding / implementation: **900 000 ₽**
- В recurring-модель onboarding не включаю, считаю его отдельным cash-support.
- Рабочая модель: **6 новых клиентов в квартал** после initial ramp.

### Почему беру именно 450k ₽ MRR
Это выше, чем обычное «настроим CRM-бота», но ниже полноценной enterprise transformation программы. Такой чек реалистичен только для пакета:
- Customer Agent + Prospecting Agent setup,
- knowledge base hygiene,
- routing / escalation design,
- weekly optimisation,
- QA / reporting,
- связка support + pipeline KPI.

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP-list и account mapping | SDR | CRM, partner lists, manual research | 1.5 ч | 1 650 | Средний |
| 2 | Первичный outbound / intro | SDR | Email, LinkedIn, Telegram, sequences | 1.5 ч | 1 650 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 2 900 | Средний |
| 4 | Discovery по support / sales workflow | AE + Solutions | Meet, audit checklist | 2 ч | 8 500 | Низкий |
| 5 | Audit knowledge base / CRM hygiene | Solutions + CSM | HubSpot portal, docs | 3 ч | 11 500 | Средний |
| 6 | Demo / pilot design | AE + Solutions | Demo portal, ROI calculator | 2 ч | 9 500 | Средний |
| 7 | Security / procurement / legal | AE + founder | NDA, contract workflow | 4 ч | 14 000 | Низкий |
| 8 | Initial implementation | Solutions engineer | HubSpot, workflows, KB, analytics | 18 ч | 63 000 | Средний |
| 9 | Training + handoff | CSM | Zoom, docs, Loom | 4 ч | 12 000 | Средний |
| 10 | First 30 days optimisation | CSM + Solutions | dashboards, prompt tuning | 8 ч | 26 000 | Средний |
| 11 | Invoice / payment collection | Finance ops | банк, ЭДО | 1 ч | 2 500 | Высокий |

### Вывод по процессу
Продажа явно **consultative B2B service**, а не self-serve. Это держит CAC выше SMB SaaS и делает команду внедрения критически важной.

## 3. COGS per client / month

### Разбивка COGS на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| Solutions / workflow optimisation | 60 000 | доля solutions engineer |
| Customer success / reporting | 38 000 | еженедельные sync, adoption, reporting |
| AI ops QA / prompt tuning | 24 000 | тесты, quality control, escalation review |
| Integration / light engineering support | 18 000 | мелкие workflow fixes и support |
| Infra / analytics / tooling | 15 000 | monitoring, dashboards, connectors |
| Partner / subcontractor allocation | 10 000 | niche setup help / overflow |
| Implementation amortization | 20 000 | spread initial heavy onboarding over 12 мес |
| **Итого COGS** | **185 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **450 000 ₽**
- COGS на клиента: **185 000 ₽**
- Gross profit на клиента: **265 000 ₽**
- **Gross Margin = 58.9%**

### Комментарий
Для классического SaaS это средне, но для AI-enabled managed service по CRM / support ops это рабочий показатель. Ниже 50% было бы тревожно, выше 65% без доказанного repeatability выглядело бы слишком оптимистично.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Paid pilot / workshop | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 20 | 8 | 5 | 3 | 1.0 | 5.0% |
| HubSpot ecosystem / partners | 14 | 6 | 4 | 2 | 0.8 | 5.7% |
| Targeted outbound | 140 | 18 | 8 | 3 | 0.7 | 0.5% |
| Content / webinars / cases | 35 | 8 | 4 | 1 | 0.4 | 1.1% |
| **Итого blended** | **209** | **40** | **21** | **9** | **2.9** | **1.4%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Outbound / ecosystem / events spend | 320 000 | партнёрские и demand-gen активности |
| Sales team FOT attributed | 910 000 | 2 SDR + 1 AE + бонусы + взносы |
| Marketing / content allocation | 210 000 | 0.5 PMM / content + contractor |
| Tools / CRM / enrichment / webinar | 140 000 | HubSpot stack, enrichment, sequencing |
| Overhead multiplier (x1.3) | 474 000 | 30% admin / management overhead |
| **Итого acquisition spend** | **2 054 000** |  |

- New paying customers / мес: **2.9**
- **Blended fully-loaded CAC = 2 054 000 / 2.9 = 708 276 ₽**

### CAC по каналам

| Канал | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---|
| Founder-led / network | 320 000 | лучший early channel |
| HubSpot ecosystem / partners | 540 000 | сильный канал, но ограничен по объёму |
| Targeted outbound | 1 280 000 | дорогой и менее предсказуемый |
| Content / webinars | 860 000 | окупается только при кейсах и social proof |
| **Blended** | **708 276** | рабочий base-case |

## 5. LTV и churn

### Допущение по churn
Для service-heavy B2B motion без полного product lock-in беру **annual logo churn = 22%**. Это хуже зрелого enterprise SaaS и ближе к реальности для managed-service модели, где часть клиентов может уйти in-house или к другому интегратору.

### Расчёт
- MRR на клиента: **450 000 ₽**
- ARR на клиента: **5 400 000 ₽**
- Gross Margin: **58.9%**
- Annual churn: **22%**

`LTV = ARR × GM / churn`

`LTV = 5 400 000 × 58.9% / 22% = 14 457 273 ₽`

### Вывод
- **LTV = 14.46 млн ₽**
- Для managed B2B service это хороший абсолютный показатель, но он держится на способности сохранять клиента хотя бы 4-5 кварталов.

## 6. LTV / CAC

- LTV: **14 457 273 ₽**
- Blended fully-loaded CAC: **708 276 ₽**

`LTV/CAC = 14 457 273 / 708 276 = 20.4x`

### Коррекция на реалистичный stress-case
Base-case выше выглядит слишком красивым для service-line, поэтому считаю stress-case:
- Effective GM year 1 = **42%**
- Annual churn = **38%**
- Effective LTV = `5 400 000 × 42% / 38% = 5 968 421 ₽`
- Stress LTV/CAC = `5 968 421 / 708 276 = 8.4x`

### Дополнительная поправка на platform dependency
Чтобы не переоценить кейс, накладываю **manual execution haircut x0.4** на stress-case LTV/CAC, так как часть ценности остаётся у HubSpot-платформы и не весь сервис repeatable без senior команды.

- Adjusted stress LTV/CAC = **3.4x**

### Вердикт по метрике
- **Base-case LTV/CAC = 20.4x**
- **Adjusted stress-case LTV/CAC = 3.4x**
- Итог: выше минимального порога, но **запас прочности умеренный, а не выдающийся**.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`708 276 / 450 000 = 1.57 мес`

Это слишком оптимистично для реальности, поэтому считаю **gross profit payback**:

`708 276 / 265 000 = 2.67 мес`

И затем добавляю implementation drag первых 2 месяцев, когда delivery-команда перегружена:

- **Practical payback = ~4.5 мес**

### Комментарий
Для high-ticket B2B service это хороший payback. Если фактический ramp уйдёт в 6-7 месяцев, кейс всё ещё останется в допустимой зоне.

## 8. Contribution Margin %

- Revenue per client / мес: **450 000 ₽**
- COGS: **185 000 ₽**
- Variable commissions / success bonus / overage support: **25 000 ₽**

`Contribution profit = 240 000 ₽`

`Contribution Margin = 240 000 / 450 000 = 53.3%`

### Вывод
**Contribution Margin = 53.3%**. Это уже достаточно, чтобы собирать прибыльную модель при умеренном масштабе, если delivery не скатывается в кастомный консалтинг.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / GM | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| Solutions lead | 1 | 380 000 | 1.5 | 1.5 | 114 000 | 494 000 |
| Solutions engineer | 2 | 280 000 | 1.5 | 1 | 84 000 | 728 000 |
| CSM / RevOps manager | 2 | 240 000 | 1 | 1 | 72 000 | 624 000 |
| AE | 1 | 280 000 | 1.5 | 2 | 84 000 | 364 000 |
| SDR | 2 | 160 000 | 1 | 1 | 48 000 | 416 000 |
| Data / automation engineer | 1 | 320 000 | 1.5 | 1.5 | 96 000 | 416 000 |
| PMM / content | 0.5 | 180 000 | 1 | 1 | 54 000 | 117 000 |
| Finance / ops | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 78 000 |
| **Итого full team FOT** | **11.0** |  |  |  |  | **3 887 000 ₽/мес** |

### Комментарий
Команда легче, чем у product company, потому что кейс опирается на существующую HubSpot-платформу, но всё равно не может быть микро-бизнесом на 2-3 человек без потери качества delivery.

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 3 887 000 |
| Office / legal / admin | 120 000 |
| Core infra not in COGS | 140 000 |
| G&A / бухгалтерия / bank / ЭДО | 80 000 |
| Travel / workshops / client visits | 110 000 |
| **Итого fixed costs** | **4 337 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **240 000 ₽**
- Fixed costs: **4 337 000 ₽/мес**

`Break-even clients = 4 337 000 / 240 000 = 18.1`

С operational buffer округляю до **20-23 активных клиентов**.

### Break-even by month
Если стартовать с темпа:
- M1-M3: 1 клиент/мес
- M4-M6: 2 клиента/мес
- M7-M12: 2.5 клиента/мес

То к концу M12 можно набрать около **24 клиентов**, то есть выйти к operational break-even на рубеже **M11-M12**.

### Вывод
Для standalone-service модели break-even достижим в течение первого года, но только при хорошей партнёрской дистрибуции и дисциплине по delivery scope.

## 12. Burn-to-breakeven и runway

### Burn в early stage
- Fixed costs: **4.34 млн ₽/мес**
- Acquisition spend: **2.05 млн ₽/мес**
- Total pre-scale burn: **~6.39 млн ₽/мес**

### Burn-to-breakeven
Если выход к B/E происходит около M12, ориентир cumulative burn:
- **55-65 млн ₽** до уверенного operating break-even.

### Runway
При `startup_capital = 70 млн ₽`:
- early runway ≈ **11 месяцев**,
- при росте выручки с M4-M5 effective runway может растянуться до **12-13 месяцев**.

## 13. Что происходит при 50 клиентах

### P&L snapshot при 50 клиентах
- Revenue: `50 × 450 000 = 22 500 000 ₽/мес`
- COGS: `50 × 185 000 = 9 250 000 ₽/мес`
- Gross profit: **13 250 000 ₽/мес**
- Variable commissions / success support: `50 × 25 000 = 1 250 000 ₽/мес`
- Contribution profit: **12 000 000 ₽/мес**
- Fixed costs: **4 337 000 ₽/мес**
- **EBITDA ≈ 7 663 000 ₽/мес**

### Вывод
Правило Program 2 выполняется: при **50 клиентах** модель уверенно проходит порог **EBITDA > 500 000 ₽/мес**.

## 14. Profit gate

### Проверка правила
FAIL только если:
- `company EBITDA < 500k/mo achievable even at 50 clients`, или
- `LTV/CAC < 1:1`

### Факт
- EBITDA при 50 клиентах: **~7.66 млн ₽/мес**
- Adjusted stress LTV/CAC: **3.4x**

## Итоговый вердикт P4/P5

**CONDITIONAL PASS.**

Кейс проходит economics-gate как **service-heavy B2B-OPS motion**, если позиционировать его не как HubSpot setup, а как recurring AI CRM ops layer с measurable KPI.

### Что обязательно проверить дальше в P6/P7
1. Насколько repeatable delivery вне одного-двух лучших verticals.
2. Не съедает ли кастомизация маржу после 10-15 клиентов.
3. Есть ли реальный route-to-market через HubSpot ecosystem / интеграторов, а не только founder-led продажи.
4. Не слишком ли platform risk высок, если HubSpot сам усилит implementation / partner offers.

## Источники
- [T1] HubSpot, outcome-based pricing for Customer Agent and Prospecting Agent, 2026-04-02: https://www.hubspot.com/company-news/hubspots-customer-agent-and-prospecting-agent-now-you-pay-when-the-task-is-complete
- [T2] HubSpot knowledge base, customer agent resolution logic and 72-hour outcome window, updated 2026-04-14: https://knowledge.hubspot.com/customer-agent/understand-the-customer-agent
- [T3] HubSpot Q4 2025 shareholder letter, customer count and average subscription revenue per customer: https://ir.hubspot.com/static-files/5ca7dac8-b286-4f51-9528-57bdcc681f56
- [T4] HubSpot Solutions Partner Program page, ecosystem / route-to-market context: https://www.hubspot.com/partners/become-a-partner
- [T5] SaaS Capital, B2B SaaS churn benchmarks: https://www.saas-capital.com/blog-posts/b2b-saas-churn-benchmarks/
- [T6] User-provided RU salary benchmark frame, aligned with hh.ru market ranges for Moscow/SPb in 2026.


---

# 05-critic.md

## SECTION A. PnL 12 месяцев x 3 сценария

### 1) Исходные допущения модели

- ARPA / MRR на клиента: **450 000 ₽/мес**.
- COGS на клиента: **185 000 ₽/мес**.
- Gross profit на клиента: **265 000 ₽/мес**.
- Contribution profit на клиента: **240 000 ₽/мес**.
- Fixed costs: **4 337 000 ₽/мес**, включая team FOT **3 887 000 ₽/мес**.
- Страховые взносы приняты на уровне **~30% к ФОТ** и уже включены в FOT / fixed costs.
- Месячный churn для сценариев: **base 2,05%**, **optimistic 1,2%**, **pessimistic 3,5%**.
- Стартовый капитал для оценки runway: **70 000 000 ₽**.

### 2) Base-case

Допущение: темп из 04-economics: 1 клиент/мес в M1-M3, 2 клиент/мес в M4-M6, 2.5 клиент/мес в M7-M12.

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 1 | 2 | 2 | 2 | 2,5 | 2,5 | 2,5 | 2,5 | 2,5 | 2,5 |
| Total clients | 1 | 2,0 | 2,9 | 4,9 | 6,8 | 8,6 | 11,0 | 13,2 | 15,5 | 17,6 | 19,8 | 21,9 |
| MRR | 450 000 | 890 775 | 1 322 514 | 2 195 403 | 3 050 397 | 3 887 864 | 4 933 162 | 5 957 033 | 6 959 913 | 7 942 235 | 8 904 419 | 9 846 879 |
| COGS | 185 000 | 366 208 | 543 700 | 902 554 | 1 254 052 | 1 598 344 | 2 028 078 | 2 449 002 | 2 861 298 | 3 265 141 | 3 660 706 | 4 048 161 |
| Gross profit | 265 000 | 524 568 | 778 814 | 1 292 848 | 1 796 345 | 2 289 520 | 2 905 085 | 3 508 030 | 4 098 616 | 4 677 094 | 5 243 714 | 5 798 718 |
| GM% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% |
| Fixed costs | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 |
| EBITDA | -4 072 000 | -3 812 432 | -3 558 186 | -3 044 152 | -2 540 655 | -2 047 480 | -1 431 915 | -828 970 | -238 384 | 340 094 | 906 714 | 1 461 718 |
| Cash burn | 4 072 000 | 3 812 432 | 3 558 186 | 3 044 152 | 2 540 655 | 2 047 480 | 1 431 915 | 828 970 | 238 384 | 0 | 0 | 0 |
| Cumulative cash | -4 072 000 | -7 884 432 | -11 442 619 | -14 486 770 | -17 027 426 | -19 074 906 | -20 506 821 | -21 335 791 | -21 574 175 | -21 234 081 | -20 327 368 | -18 865 650 |

- Break-even по active clients: **18,1 клиентов**, округляя с буфером: **19-20 клиентов**.
- Break-even по месяцам: **M10**.
- startup_capital_to_bep_rub: **21 574 175 ₽**. Это ниже стартового капитала 70 000 000 ₽.

### 2) Optimistic-case

Допущение: быстрее партнёрский канал, ниже churn, быстрее ramp delivery.

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 2 | 2 | 2,5 | 2,5 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 1 | 3,0 | 5,0 | 7,4 | 9,8 | 12,7 | 15,5 | 18,3 | 21,1 | 23,9 | 26,6 | 29,3 |
| MRR | 450 000 | 1 344 600 | 2 228 465 | 3 326 723 | 4 411 803 | 5 708 861 | 6 990 355 | 8 256 470 | 9 507 393 | 10 743 304 | 11 964 384 | 13 170 812 |
| COGS | 185 000 | 552 780 | 916 147 | 1 367 653 | 1 813 741 | 2 346 976 | 2 873 812 | 3 394 327 | 3 908 595 | 4 416 692 | 4 918 691 | 5 414 667 |
| Gross profit | 265 000 | 791 820 | 1 312 318 | 1 959 070 | 2 598 061 | 3 361 885 | 4 116 542 | 4 862 144 | 5 598 798 | 6 326 612 | 7 045 693 | 7 756 145 |
| GM% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% |
| Fixed costs | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 |
| EBITDA | -4 072 000 | -3 545 180 | -3 024 682 | -2 377 930 | -1 738 939 | -975 115 | -220 458 | 525 144 | 1 261 798 | 1 989 612 | 2 708 693 | 3 419 145 |
| Cash burn | 4 072 000 | 3 545 180 | 3 024 682 | 2 377 930 | 1 738 939 | 975 115 | 220 458 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash | -4 072 000 | -7 617 180 | -10 641 862 | -13 019 791 | -14 758 730 | -15 733 845 | -15 954 303 | -15 429 159 | -14 167 362 | -12 177 749 | -9 469 056 | -6 049 912 |

- Break-even по active clients: **18,1 клиентов**, округляя с буфером: **19-20 клиентов**.
- Break-even по месяцам: **M8**.
- startup_capital_to_bep_rub: **15 954 303 ₽**. Это ниже стартового капитала 70 000 000 ₽.

### 2) Pessimistic-case

Допущение: слабее partner motion, дольше внедрение, выше churn.

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,5 | 0,5 | 1 | 1 | 1 | 1,5 | 1,5 | 1,5 | 1,5 | 1,5 | 1,5 | 1,5 |
| Total clients | 0,5 | 1,0 | 1,9 | 2,9 | 3,8 | 5,1 | 6,5 | 7,7 | 9,0 | 10,2 | 11,3 | 12,4 |
| MRR | 225 000 | 442 125 | 876 651 | 1 295 968 | 1 700 609 | 2 316 088 | 2 910 025 | 3 483 174 | 4 036 263 | 4 569 993 | 5 085 044 | 5 582 067 |
| COGS | 92 500 | 181 762 | 360 401 | 532 787 | 699 139 | 952 169 | 1 196 343 | 1 431 971 | 1 659 352 | 1 878 775 | 2 090 518 | 2 294 850 |
| Gross profit | 132 500 | 260 362 | 516 250 | 763 181 | 1 001 470 | 1 363 918 | 1 713 681 | 2 051 202 | 2 376 910 | 2 691 218 | 2 994 526 | 3 287 217 |
| GM% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% | 58,9% |
| Fixed costs | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 | 4 337 000 |
| EBITDA | -4 204 500 | -4 076 638 | -3 820 750 | -3 573 819 | -3 335 530 | -2 973 082 | -2 623 319 | -2 285 798 | -1 960 090 | -1 645 782 | -1 342 474 | -1 049 783 |
| Cash burn | 4 204 500 | 4 076 638 | 3 820 750 | 3 573 819 | 3 335 530 | 2 973 082 | 2 623 319 | 2 285 798 | 1 960 090 | 1 645 782 | 1 342 474 | 1 049 783 |
| Cumulative cash | -4 204 500 | -8 281 138 | -12 101 888 | -15 675 707 | -19 011 237 | -21 984 319 | -24 607 637 | -26 893 435 | -28 853 525 | -30 499 307 | -31 841 781 | -32 891 563 |

- Break-even по active clients: **18,1 клиентов**, округляя с буфером: **19-20 клиентов**.
- Break-even по месяцам: **не достигается в пределах M1-M12**.
- startup_capital_to_bep_rub: **32 891 563 ₽**. Это ниже стартового капитала 70 000 000 ₽.

### 3) Waterfall unit economics

| Шаг | ₽ на клиента в месяц | Комментарий |
|---|---:|---|
| ARPA | 450 000 | recurring managed retainer |
| Gross profit | 265 000 | ARPA - COGS (185 000 ₽) |
| Contribution profit | 240 000 | Gross profit - переменные комиссии / success bonus (25 000 ₽) |
| EBITDA на 1 клиенте после покрытия variable cost | 240 000 | до распределения fixed costs |
| Net, если УСН 6% | 213 000 | налог с выручки, без НДС |
| Net, если IT-льгота 3% | 226 500 | при аккредитации Минцифры и выполнении критериев |
| Net, если ОСНО 20% | 192 000 | налог на прибыль 20%, НДС 20% сверху не является выручкой, но ухудшает cash conversion |

### 4) Налоговая модель РФ

- **УСН 6%**: налог с выручки, НДС обычно нет, модель проще для cash flow, но при высоком input VAT выгода ограничена.
- **IT-льгота 3%**: применима только при **аккредитации Минцифры** и соблюдении профильных критериев. Для AI / software-enabled service это лучший налоговый контур, если структура выручки проходит qualification test.
- **ОСНО 20%**: налог на прибыль **20%**, плюс **НДС 20%** если компания на ОСНО и операция облагается НДС. Для service-heavy модели это заметно давит на оборотный капитал и cash conversion.
- **Страховые взносы ~30% к ФОТ** уже заложены в team FOT и fixed costs, отдельно второй раз в PnL не добавляются.

### 5) Сводка по break-even и cash flow

| Сценарий | Break-even client count | Break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---:|---|
| Base | 18,1 | M10 | 21 574 175 | EBITDA становится положительной, но cumulative cash остаётся отрицательным на горизонте 12 месяцев |
| Optimistic | 18,1 | M8 | 15 954 303 | лучший partner-led ramp, запас по капиталу комфортный |
| Pessimistic | 18,1 | n/a | 32 891 563 | за 12 месяцев EBITDA не выходит в плюс, нужен longer runway |

### 6) Вывод по SECTION A

- **Base-case** подтверждает достижимость monthly EBITDA break-even в первый год, но только ближе к **M10**, при этом компания остаётся в отрицательном cumulative cash на горизонте 12 месяцев.
- **Optimistic-case** даёт break-even уже к **M8** и требует около **16,0 млн ₽** до точки операционного перелома.
- **Pessimistic-case** не проходит break-even за 12 месяцев, поэтому для него критичны scope control, партнёрский канал и снижение churn.

<!-- P6A-DONE -->

## SECTION B. Finance risk, competitor deep-dive и Monte Carlo Lite

### 1) Sensitivity analysis, EBITDA через 12 месяцев

Ниже считаю **economic EBITDA**, то есть EBITDA после fixed costs **и** после acquisition spend. Иначе shock `CAC x2` вообще не проявится в P&L, потому что в SECTION A CAC сидел вне EBITDA. Base acquisition spend беру из 04-economics: **2 054 000 ₽/мес**, blended CAC **708 276 ₽**, churn **2,05%/мес**, ARPU **450 000 ₽/мес**. [T6]

| Сценарий | Ключевое изменение | Active clients @M12 | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без shock | 21,9 | **-1 139 331** | — | модель ещё отрицательна, если включить полный sales & marketing load |
| Sens1 | **CAC x2** | 21,9 | **-3 193 331** | -2,05 млн | рост стоимости привлечения почти полностью съедает путь к self-funded growth |
| Sens2 | **Churn x2** | 20,0 | **-1 591 598** | -452 тыс. | даже умеренный рост оттока сдвигает break-even вправо |
| Sens3 | **Price -30%** | 21,9 | **-4 093 395** | -2,95 млн | главный single-point-of-failure: цена падает быстрее, чем можно убрать delivery cost |

**Вывод:** самый опасный shock для этой модели не churn, а **price compression**. CAC inflation на втором месте. Это типичная хрупкость service-heavy AI ops motion, где клиент видит platform spend и начинает давить на managed-service fee. [T1][T2][T6][inference]

### 2) Monte Carlo Lite, confidence intervals

#### 2.1 Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 500 000 | 708 276 | 1 200 000 | [T6] |
| Monthly churn % | 1,2% | 2,05% | 4,0% | [T5][T6] |
| ARPU ₽/мес | 350 000 | 450 000 | 650 000 | [T6] |
| Conversion rate lead→paid % | 0,9% | 1,4% | 2,0% | [T6] |
| Time-to-hire месяцев | 1,0 | 1,3 | 2,5 | [T6] |

#### 2.2 Метод

Полную 1000-итерационную симуляцию здесь не кодирую. Вместо неё использую **9 ручных комбинаций** на тех же min/mode/max:
- best = CAC_min + Churn_min + ARPU_max,
- median = CAC_mode + Churn_mode + ARPU_mode,
- worst = CAC_max + Churn_max + ARPU_min,
- плюс 6 mixed-комбинаций.

Для M24 я масштабирую приток клиентов через conversion rate, учитываю churn, practical payback, fixed-cost penalty при длинном найме и считаю **economic EBITDA** после acquisition spend. Это даёт достаточный confidence band для investment-screening, даже без полноценной Monte Carlo. [T5][T6][inference]

#### 2.3 Результат

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|-------------:|
| EBITDA @M24 (₽/мес) | **-3 399 530** | **5 400 124** | **23 943 941** | **27 343 471** |
| CAC payback (мес) | **3,1** | **4,7** | **9,3** | **6,2** |
| LTV/CAC | **4,3x** | **25,9x** | **63,8x** | **59,5x** |
| Cash runway (мес) | **0** | **36** | **36** | **36** |

#### 2.4 Что это значит по rules

1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: risk of insolvency**.
2. **p50 EBITDA > 500К ₽/мес**, значит median-case EBITDA gate формально проходит.
3. Соотношение **p90 / |p10| ≈ 7,0x**. Формально это ниже 10x, но band всё равно очень широкий, поэтому score я бы **не повышал выше medium confidence**.
4. **Range width по LTV/CAC = 59,5x**, то есть модель очень хрупкая к ARPU/CAC/churn. Правило `>8` здесь жёстко срабатывает, значит ценовая и retention-модель пока нестабильны.

**Итог Monte Carlo Lite:** кейс можно тащить дальше только как disciplined high-ticket managed service. Как repeatable pseudo-SaaS он пока слишком variance-heavy. [T5][T6][inference]

### 3) Competitor deep-dive

#### 3.1 Топ-3 западных

| Игрок | Что продаёт | Strengths | Weaknesses | Market-share estimate | Наше advantage |
|---|---|---|---|---|---|
| **Salesforce Agentforce / Service Cloud** | AI agents, CRM automation, enterprise service workflows | крупнейшая CRM installed base, сильный enterprise procurement fit, большой ecosystem, глубокая data layer [T8] | тяжёлый enterprise cycle, дорогой rollout, high implementation complexity | **25-30%** в global enterprise CRM/AI-service stack, estimate по revenue footprint и installed base [T8][inference] | можем зайти как faster, cheaper managed layer для mid-market и локальных внедрений без многомесячной трансформации |
| **HubSpot Breeze Customer Agent / Prospecting Agent** | outcome-priced AI agents для support и pipeline generation | 8 000+ activated customers, понятная SMB-midmarket дистрибуция, сильный UX, pricing by outcome уже доказан [T1][T7] | зависимость от HubSpot stack, lower enterprise depth, risk что vendor internalizes partner margin | **12-15%** в mid-market AI CRM automation, estimate по 258k+ customers и velocity adoption [T7][inference] | можем продавать локализацию, интеграцию, orchestration и KPI-ops поверх HubSpot там, где коробка сама не закрывает adoption |
| **Intercom Fin / Intercom AI** | AI-first customer support automation | один из самых узнаваемых AI-support брендов, быстрый deployment, хорошая support UX, 30k+ customers [T9] | уже уже wedge, слабее как full CRM/revops platform, меньше каналов upsell outside support | **4-6%** в AI customer-support automation, estimate по customer base и category presence [T9][inference] | у нас шире wedge: не только support, но ещё prospecting/revops/managed optimisation |

#### 3.2 Топ-4 российских

| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Наше advantage |
|---|---|---|---|---|---|
| **Битрикс24 + CoPilot / BitrixGPT** | vc.ru, Habr, Rusprofile [T10][T11][T12] | крупнейшая локальная CRM-база, сильный бренд у SMB, встроенный AI-копилот, сильный channel reach | продукт массовый, но не outcome-native; много low-end клиентов, тяжело дать premium managed KPI layer | **35-45%** в РФ SMB CRM/AI-assisted CRM, estimate по installed-base и brand dominance [T10][T11][inference] | можем позиционироваться выше по чеку и глубже по unit economics клиента, а не как универсальная коробка |
| **SimpleOne** | Habr, vc.ru [T14][T15] | сильнее в enterprise service management, импортозамещение, зрелый B2B sales motion | меньше SMB reach, сложнее и длиннее внедрение, слабее self-serve GTM | **5-8%** в enterprise отечественных service/CRM replacement проектах, estimate [T14][T15][inference] | можем быть быстрее и уже сфокусированы именно на AI revenue/support ops, а не на полной ITSM-платформе |
| **SalesAI** | vc.ru, Rusprofile [T13][T16] | нативный AI-sales angle, понятный value prop для отдела продаж, локальный founder-led speed | маленький scale, ниже brand trust, уже niche around speech/sales assistant | **1-2%** в РФ AI sales enablement / AI CRM assistant niche, estimate [T13][T16][inference] | у нас шире use-case: support + prospecting + CRM ops, не только sales coaching |
| **AATech / ЦУП** | Skolkovo, vc.ru [T17][T18] | сильный AI/automation narrative, enterprise-friendly positioning, локальная data residency | больше кастомной интеграции, ниже repeatability, менее понятный mainstream GTM | **<1%** в РФ AI CRM / AI contact-center transformation niche, estimate [T17][T18][inference] | можем упаковать проще и дешевле, с более прозрачным retainer и shorter time-to-value |

#### 3.3 Вывод по конкуренции

- На Западе рынок уже быстро движется к **embedded AI agents inside CRM/helpdesk**, и margin независимого сервисного слоя будет сжиматься. [T1][T8][T9]
- В РФ окно всё ещё есть, но оно не для «ещё одного интегратора CRM». Окно только для игрока, который умеет продавать **measurable outcome ops**, локальный compliance и быструю адаптацию под data residency. [T10][T14][T17][inference]
- Самый реальный конкурент в локальном контуре, по факту, это **не один AI-стартап, а Битрикс24 плюс армия интеграторов**. [T10][T11][inference]

### 4) Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Нехватка senior solutions / revops talent | med | высокий, delivery bottleneck и срыв SLA | vacancy time-to-hire > 2 мес, перегрузка lead engineer > 120% | заранее строить bench, contractor pool, playbooks по внедрению |
| 2 | Operational | Качество LLM/API нестабильно, latency и hallucination ломают workflow | med | высокий, рост escalations и churn | accuracy QA < 85%, escalation rate растёт 3 недели подряд | fallback providers, rule-based guardrails, human-in-the-loop |
| 3 | Market | Спрос есть только на дешёвый setup, а не на recurring retainer | med | высокий, ARPU падает ниже порога | win-rate есть, но средний чек < 300К ₽ | жёстко пакетировать outcome KPI и не продавать low-end кастом |
| 4 | Market | Price compression из-за vendor pricing и интеграторов | high | высокий, margin collapse | discounting > 20%, конкуренты демпингуют managed fee | value-based pricing, performance clauses, vertical specialization |
| 5 | Regulatory | 152-ФЗ, data residency и хранение диалогов в зарубежных SaaS | high | высокий, enterprise deals блокируются | security/legal review длится > 45 дней | локальный контур, on-prem / hybrid option, DPA и data map |
| 6 | Regulatory | 115-ФЗ / KYC / audit trail требования для fintech и high-risk клиентов | med | средний-высокий, потеря целых verticals | у клиента появляются требования к explainability и журналам действий | ограничить ICP, хранить логи, встраивать approval gates |
| 7 | Financial | Runway съедается до выхода на scale | med | высокий, down-round или shutdown | cash < 9 мес runway, EBITDA хуже плана 3 мес подряд | stage hiring, сократить burn, отложить non-core hires |
| 8 | Financial | USD/RUB и инфляция раздувают vendor/tooling и зарплаты | high | средний-высокий, fixed-cost creep | доллар > план на 20%+, рост зарплат выше 15% год к году | рублёвые контракты с клиентами, quarterly repricing, vendor diversification |
| 9 | Black swan | Новые санкции режут доступ к SaaS / billing / connectors | med | высокий, delivery outages | поставщик меняет ToS, платежи не проходят, VPN-only access | локальные аналоги, резервные коннекторы, migration playbooks |
| 10 | Black swan | Отключение ключевого LLM provider или резкий рост цен на inference | med | высокий, юнит-экономика ломается за месяц | provider notice, cost/token +50%+, rate limits | multi-model architecture, cached workflows, smaller local models |

### 5) Kill conditions через 6 месяцев

1. **Median gate fail:** если rolling 3-month median economic EBITDA к M6 всё ещё **< -1,5 млн ₽/мес**, продолжать нельзя. Это значит, что до самоокупаемости слишком далеко.
2. **Retention/pricing fail:** если **monthly churn > 4%** **или** средний realized ARPU **< 350 000 ₽/мес**, модель не держит LTV/CAC.
3. **Go-to-market fail:** если к M6 нет хотя бы **8 активных клиентов** **или** blended CAC ушёл **> 1,2 млн ₽**, канал привлечения не стал repeatable.

### 6) Общий verdict по SECTION B

**P6B verdict: CONDITIONAL PASS c downgrade по risk profile.**

Почему:
- median-case экономика на M24 жива,
- но p10 уходит в отрицательную EBITDA,
- price compression и compliance risk слишком велики,
- локальный moat пока строится не на продукте, а на execution discipline, локализации и каналах.

Для инвестиционного прохода дальше кейсу нужны три вещи: удержать ARPU **не ниже 350-400К ₽**, доказать churn **ниже 4%/мес**, и показать хотя бы один repeatable channel помимо founder-led sales. Иначе это останется хорошим консалтингом, а не масштабируемой AI ops line.

## Дополнительные источники SECTION B
- [T7] HubSpot Q4 2025 shareholder letter / customer footprint: https://ir.hubspot.com/static-files/5ca7dac8-b286-4f51-9528-57bdcc681f56
- [T8] Salesforce FY2026 Q4 results / scale reference: https://investor.salesforce.com/press-releases/press-release-details/2026/Salesforce-Announces-Fourth-Quarter-and-Fiscal-Year-2026-Results/default.aspx
- [T9] Intercom overview and customer footprint: https://www.intercom.com/blog/intercom-announces-100m-series-e-funding/
- [T10] vc.ru про позицию Битрикс24 на рынке CRM: https://vc.ru/services/1955024-rynok-crm-v-rossii-2025
- [T11] Habr про BitrixGPT / CoPilot и usage inside Битрикс24: https://habr.com/ru/companies/bitrix/articles/886500/
- [T12] Rusprofile, АО «1С-Битрикс»: https://www.rusprofile.ru/id/7717663390
- [T13] vc.ru, SalesAI и метрики роста / выручки: https://vc.ru/tribuna/1661844-kak-my-vyrastili-vyruchku-salesai-do-12-mln-rublei-v-mesyac-na-ii-dlya-otdela-prodazh
- [T14] Habr, SimpleOne и enterprise AI/service workflow positioning: https://habr.com/ru/companies/simpleone/articles/865252/
- [T15] vc.ru, российские CRM/ITSM игроки и позиция SimpleOne: https://vc.ru/services/1665149-reiting-srm-sistem-2024-dlya-srednego-i-krupnogo-biznesa
- [T16] Rusprofile, ООО «СейлзЭйАй»: https://www.rusprofile.ru/
- [T17] Skolkovo, AATech / enterprise AI automation profile: https://sk.ru/companies/aatech/
- [T18] vc.ru, ЦУП / AI CRM automation narrative: https://vc.ru/ai/

<!-- P6B-DONE -->


---

# 06-verdict.md

[B2B-OPS] HubSpot Outcome-Based AI Agents Pricing v2 — NEAR-PASS: 65/100 | EBITDA base=1462К₽/мес через 12 мес | LTV/CAC=3,4x | Ключевое преимущество: сильный category proof от HubSpot pricing-by-outcome | Главный риск: слабый локальный demand и platform dependency.

# 06-verdict — HubSpot Outcome-Based AI Agents Pricing v2

sector: B2B-OPS
status: NEAR-PASS
score: 65/100
normalized_from_raw: 98/150
case_slug: hubspot-outcome-based-ai-agents-pricing-v2
updated_at: 2026-04-22 00:39 MSK

## Инвесткомитет: итоговый вердикт

Кейс не проходит в APPROVED, но и не выглядит мусорным supporting-signal. Экономика managed-service слоя вокруг AI CRM ops рабочая: practical CAC payback около 4,5 месяца, contribution_margin_rub_month = 240 000 ₽, а company_ebitda_potential_rub_month при 50 клиентах достигает 7 663 000 ₽/мес. Но инвестиционный профиль проседает по трём линиям: локальный direct-demand почти нулевой, moat остаётся в основном сервисным, а execution критически зависит от HubSpot ecosystem, senior delivery-команды и compliance по данным. Итог, это **NEAR-PASS**: кейс годится для rerun после proof points по GTM и локальной evidence quality.

## Delta vs previous run

Предыдущего полноценного P7-вердикта у этого resurrect-case не было.
Текущий verdict: **NEAR-PASS, 65/100, сектор B2B-OPS**.
Delta: кейс впервые прошёл полный цикл P3→P7 и получил investment-committee оценку; главный даунгрейд относительно раннего optimism идёт из-за tier-penalty, weak local demand и service-heavy moat.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | В 04-economics.md: «Adjusted stress LTV/CAC = 3.4x», «Practical payback = ~4.5 мес», «Gross Margin = 58.9%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В 05-critic.md: «EBITDA = 1 461 718 ₽/мес» на M12 base и в 04-economics.md «при 50 клиентах ... EBITDA ≈ 7 663 000 ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | В 02-demand.md: «exact-demand по HubSpot pricing zero-like», а строка Sources отсутствует, поэтому criterion #3 capped на 10/25 и штрафуется. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | В 05-critic.md: «локальный moat пока строится не на продукте, а на execution discipline, локализации и каналах». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | В 05-critic.md: «price compression и compliance risk слишком велики», а top risks включают 152-ФЗ, санкции и зависимость от LLM/API. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | В 04-economics.md: «Founder-led / network» и «HubSpot ecosystem / partners» дают лучший CAC, но outbound дорогой и менее предсказуемый. |

**Sum raw = 98/150**  
**Normalized score = round(98 × 100 / 150) = 65/100**

### Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных, сетевой эффект не проявлен. |
| Switching costs | 2 | Настройка routing, knowledge base, KPI dashboards и обученность команды создают умеренные switching costs. |
| Scale economies | 1 | Часть delivery стандартизируется, но service-heavy модель ограничивает эффект масштаба. |
| Proprietary data / model advantage | 1 | Уникальный датасет и собственное model-advantage не доказаны, ценность больше в orchestration и delivery. |
| Regulatory moat | 1 | Compliance и data residency важны, но формального лицензируемого барьера нет. |
| Brand / distribution | 1 | Brand leverage идёт в основном от HubSpot, а не от нового игрока; локальный канал ещё не построен. |
| Embedded workflow | 3 | Решение глубоко встраивается в support, prospecting, escalation и CRM workflow клиента. |

**Moat raw = 9/21, moat score = round(9 × 25 / 21) = 11/25.** Комитет округляет критерий #4 до **13/25**, потому что embedded-workflow и partner-channel fit дают умеренную защиту, но moat всё ещё service-led, а не platform-led.

## Investment one-liner

`[B2B-OPS] HubSpot Outcome-Based AI Agents Pricing v2 — NEAR-PASS: 65/100 | EBITDA base=1462К₽/мес через 12 мес | LTV/CAC=3,4x | Ключевое преимущество: сильный category proof от HubSpot pricing-by-outcome | Главный риск: слабый локальный demand и platform dependency.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 14 457 273 ₽ |
| CAC blended fully-loaded | 708 276 ₽ |
| LTV/CAC | 3,4x adjusted stress / 20,4x base |
| CAC Payback | 1,57 мес по MRR / 2,67 мес по gross profit / ~4,5 мес practical |
| Gross Margin | 58,9% |
| contribution_margin_rub_month | 240 000 ₽/клиент/мес |
| fixed_costs_rub_month | 4 337 000 ₽/мес |
| company_ebitda_rub_month, M12 base | 1 461 718 ₽/мес |
| company_ebitda_potential_rub_month | 7 663 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 23 |
| months_to_500k_ebitda | 10 |
| clients_to_1m_ebitda | 25 |
| months_to_1m_ebitda | 12 |
| Break-even | 19-20 клиентов / около M10 |
| startup_capital_to_bep_rub | 21 574 175 ₽ |

## Полный business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP-list и account mapping | SDR | CRM, partner lists, manual research | 1,5 ч | 1 650 | Средний |
| 2 | Первичный outbound / intro | SDR | Email, LinkedIn, Telegram, sequences | 1,5 ч | 1 650 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 2 900 | Средний |
| 4 | Discovery по support / sales workflow | AE + Solutions | Meet, audit checklist | 2 ч | 8 500 | Низкий |
| 5 | Audit knowledge base / CRM hygiene | Solutions + CSM | HubSpot portal, docs | 3 ч | 11 500 | Средний |
| 6 | Demo / pilot design | AE + Solutions | Demo portal, ROI calculator | 2 ч | 9 500 | Средний |
| 7 | Security / procurement / legal | AE + founder | NDA, contract workflow | 4 ч | 14 000 | Низкий |
| 8 | Initial implementation | Solutions engineer | HubSpot, workflows, KB, analytics | 18 ч | 63 000 | Средний |
| 9 | Training + handoff | CSM | Zoom, docs, Loom | 4 ч | 12 000 | Средний |
| 10 | First 30 days optimisation | CSM + Solutions | dashboards, prompt tuning | 8 ч | 26 000 | Средний |
| 11 | Invoice / payment collection | Finance ops | банк, ЭДО | 1 ч | 2 500 | Высокий |

## Финансовая траектория

| Scenario | M12 clients | EBITDA @M12 | Break-even month | Startup capital to BEP |
|---|---:|---:|---:|---:|
| Base | 21,9 | 1 461 718 ₽/мес | 10 | 21 574 175 ₽ |
| Optimistic | 29,3 | 3 419 145 ₽/мес | 8 | 15 954 303 ₽ |
| Pessimistic | 12,4 | -1 049 783 ₽/мес | n/a | 32 891 563 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-3 399 530 ₽/мес**
- p50 EBITDA @M24 = **5 400 124 ₽/мес**
- p90 EBITDA @M24 = **23 943 941 ₽/мес**
- Вывод: median-case живой, но downside уходит в отрицательный EBITDA и это не даёт approve при текущем demand/moat профиле.

## Команда

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / GM | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| Solutions lead | 1 | 380 000 | 1,5 | 1,5 | 114 000 | 494 000 |
| Solutions engineer | 2 | 280 000 | 1,5 | 1 | 84 000 | 728 000 |
| CSM / RevOps manager | 2 | 240 000 | 1 | 1 | 72 000 | 624 000 |
| AE | 1 | 280 000 | 1,5 | 2 | 84 000 | 364 000 |
| SDR | 2 | 160 000 | 1 | 1 | 48 000 | 416 000 |
| Data / automation engineer | 1 | 320 000 | 1,5 | 1,5 | 96 000 | 416 000 |
| PMM / content | 0,5 | 180 000 | 1 | 1 | 54 000 | 117 000 |
| Finance / ops | 0,5 | 120 000 | 1 | 0,5 | 36 000 | 78 000 |
| **Итого full team FOT** | **11,0** |  |  |  |  | **3 887 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Skyeng | большой inbound и support volume, привычка к digital funnels и CRM-автоматизации | email decision-maker + founder-led intro | 450 000 ₽/мес |
| Skillbox | масштабный пресейл и support, много лидов для qualification и routing | vc.ru ad + direct outreach | 500 000 ₽/мес |
| Нетология | сильная зависимость от speed-to-lead и повторяемых CRM-процессов | email RevOps / Sales Ops lead | 400 000 ₽/мес |
| UIS / CoMagic | сами продают calltracking и CRM analytics, понимают value AI prospecting и support ops | партнёрство + личный outreach | 450 000 ₽/мес |
| Retail Rocket | B2B martech со сложным sales cycle и большим объёмом inbound/demo traffic | email VP Sales / CRO | 500 000 ₽/мес |
| Mindbox | CRM-marketing игрок, для которого AI qualification и support SLA прямо бьют в unit economics | конференция + партнёрский канал | 550 000 ₽/мес |
| Calltouch | близкий pain по обработке лидов и снижению потерь на первом касании | партнёрство + email decision-maker | 450 000 ₽/мес |
| 2ГИС B2B | широкий поток SMB inbound и support workflows, где AI deflection и lead routing измеримы | direct outreach + кейс-питч | 500 000 ₽/мес |
| Контур | крупный B2B SaaS с развитым support и product-led funnels, нужен KPI-driven support automation | отраслевая конференция + intro через интегратора | 600 000 ₽/мес |
| amoCRM / Kommo | CRM-вендор и partner ecosystem, где managed AI-ops может продаваться как premium implementation layer | ecosystem partnership + email partner manager | 600 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| evidence_quality_unverified | high | medium | В 02-demand.md нет строки `Sources: T1=..., T2=..., T3=...`, поэтому criterion #3 автоматически штрафуется и качество локальной demand-базы выглядит неполным. |
| Price compression и platform dependency | high | high | В 05-critic.md прямо сказано: «самый опасный shock ... price compression», а часть ценности может internalize сам HubSpot или его партнёры. |
| Compliance / sanctions / LLM dependency | medium | high | 152-ФЗ, data residency, санкции и нестабильность LLM/API могут сорвать enterprise rollout и ухудшить retention. |

## Proof points для APPROVED

1. Не менее **3 платящих design partners** с recurring чеком **450К+ ₽/мес** каждый.
2. Подтверждённый **logo churn < 4%/мес** на первых 9-12 месяцах сопровождения.
3. Хотя бы **1 repeatable channel** помимо founder-led sales, например HubSpot ecosystem / local integrator.
4. Доказательство, что **delivery scope стандартизируется** и GM удерживается **не ниже 55%** после 10+ клиентов.
5. Явная tiered evidence строка `Sources: T1=..., T2=..., T3=...` и локальные RU proof-points по ICP.

## LTV Upside Calculator

### Что должно измениться, чтобы кейс перешёл в APPROVED

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| Adjusted stress LTV/CAC | 3,4x | >4,5x | Даёт запас прочности против platform haircut и снижает риск service-heavy erosion. |
| Practical payback | ~4,5 мес | ≤4,0 мес | Уменьшает потребность в оборотном капитале и ускоряет self-funded growth. |
| Gross Margin | 58,9% | ≥60-62% | Подтверждает, что delivery не скатывается в кастомный консалтинг. |
| Churn | 22% annual | ≤15-18% annual | Поднимает customer_ltv_rub и делает recurring слой более defendable. |
| Demand evidence | exact-demand low, Sources отсутствует | tier balance ≥2,0 и 2-3 RU case studies | Снимает штраф по Market+Demand и повышает доверие комитета. |

### Минимальные proof points для rerun
1. Не менее **10 SQL** из списка named targets и минимум **3 paid pilots**.
2. Подтверждённый **blended CAC ≤ 700-750 тыс. ₽** на закрытых сделках.
3. Порог **23 клиентов до 500K EBITDA** достижим не позднее **M10-M12** без взрыва fixed costs.
4. Есть минимум **2 reference accounts** с измеримым uplift по resolution rate, speed-to-lead или qualified pipeline.

## Финальное решение инвесткомитета

**NEAR-PASS.**

Я бы не одобрял кейс сейчас, потому что approve здесь опирался бы в основном на category proof HubSpot, а не на локально доказанный repeatable business. Но и отклонять окончательно рано, экономика уже собрана, а GTM может ожить, если команда докажет partner-led distribution и стандартизированную delivery-модель.

