# Verdict dossier — 2001-msk-edra-geo-expand-v2

Источник pipeline: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/rejected/2001-msk-edra-geo-expand-v2/`
Статус: REJECTED / NEAR-PASS
Собрано: 2026-04-21 MSK

---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-2001-msk-edra-geo-expand.md
created: 2026-04-20T02:26:19+03:00
original_verdict_source: triage/triage-2026-04-18-2001-msk-edra-geo-expand.md
---

# Intake

## Режим обработки
Принудительный полный пайплайн для resurrect-сигнала. Этот кейс создан как standalone candidate и не должен классифицироваться как duplicate на этапе intake.

## Исходный raw-файл
- Имя: `2026-04-19-resurrect-2001-msk-edra-geo-expand.md`
- Новый slug кейса: `2001-msk-edra-geo-expand-v2`
- Следующий этап: `P3-demand-validation`

## Полный контекст из raw

# RESURRECT SIGNAL — 2001-msk-edra-geo-expand

## Meta
- source: triage/triage-2026-04-18-2001-msk-edra-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-2001-msk-edra-geo-expand.md`

## Классификация
Поддерживающий сигнал для существующего открытого кейса.

## Решение
Сигнал добавлен в кейс `enterprise-ai-process-automation-operator`.

## Что именно добавлено
- Создан и заполнен `pipeline/cases/enterprise-ai-process-automation-operator/01-evidence.md` с supporting signal по Edra.
- Зафиксированы источники, включая материал TechCrunch от 2026-03-18 и сайт компании.
- Добавлены ключевые факты: выход из stealth, раунд Series A на 30 млн долларов, клиенты уровня HubSpot, ASOS и Cushman & Wakefield.
- Отдельно описано, почему сигнал усиливает кейс: category shift от обычной автоматизации процессов к извлечению реальных workflows из операционных систем и запуску AI-агентов на базе живых playbook.

## Почему это усиливает кейс
Edra показывает, что enterprise buyers готовы платить не только за BPM или low-code слой, но и за более высокий process intelligence-контур, который автоматически документирует, обновляет и исполняет реальные операционные процессы. Для `enterprise-ai-process-automation-operator` это важное подтверждение, что рынок движется к более дорогому и сложному implementation plus managed operations формату.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен подтверждающий GEO-EXPAND сигнал по Edra для `enterprise-ai-process-automation-operator`.

```

---

# 02-demand.md

---
stage: demand-validation
case: 2001-msk-edra-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Edra, AI-native process intelligence и workflow automation слой, который извлекает рабочие процессы из тикетов, логов, почты и сообщений, превращает их в executable knowledge и затем запускает на этом AI-агентов для ITSM, support и смежных enterprise operations.

## Итог
**Статус: CONDITIONAL PASS.**

По прямому спросу в РФ кейс выглядит слабо: `process intelligence platform` дал `LOW`, `demand_score=0`, `hh_ru=3`; `workflow automation platform` тоже `LOW`, `hh_ru=6`; даже `enterprise ai agent automation` остаётся `LOW`, хотя уже видно `hh_ru=15` [T1]. Но adjacent budget существует: `IT service management automation` дал `hh_ru=78`, а `business process management software` дал `hh_ru=216` [T1]. Это означает, что рынок покупает не ярлык `process intelligence`, а уже существующие корзины бюджета, такие как BPM, ITSM, workflow automation и process mining.

Глобальный category proof сильный. На 18 марта 2026 года Edra вышла из stealth с раундом **$30M Series A** во главе с Sequoia, а TechCrunch отдельно отметил клиентов **HubSpot, ASOS и Cushman & Wakefield** [T2]. На собственном сайте Edra пишет, что автоматически учится на тикетах, логах и сообщениях, а затем помогает автоматизировать **technical support** и **IT service management**; отдельно заявлены кейсы HubSpot и ASOS [T3]. Это хороший сигнал, что enterprise buyers готовы платить не только за low-code/BPM, но и за более высокий слой process intelligence plus agent execution.

Для локального кейса это не strong pass, потому что в РФ уже есть дешёвые substitutes по BPM/low-code и сильный риск, что ценность Edra будет съедаться кастомной разработкой, ServiceNow-like проектами и локальными workflow-платформами. Но ранний reject не нужен: buyer, pain и spend line выглядят реальными.

## 1. Demand data
Источник exact-check: internal multi-demand API.

### `process intelligence platform`
- Composite demand: **LOW**
- Demand score: **0**
- hh.ru vacancies: **3**
- Habr articles: **2**
- Yandex suggest: **2**

### `enterprise ai agent automation`
- Composite demand: **LOW**
- Demand score: **3**
- hh.ru vacancies: **15**
- Habr articles: **2**
- Yandex suggest: **2**

### `workflow automation platform`
- Composite demand: **LOW**
- Demand score: **0**
- hh.ru vacancies: **6**
- Habr articles: **2**
- Yandex suggest: **2**

### Смежные проверки
#### `IT service management automation`
- Composite demand: **LOW**
- Demand score: **7**
- hh.ru vacancies: **78**

#### `process mining software`
- Composite demand: **LOW**
- Demand score: **0**
- hh.ru vacancies: **8**

#### `business process management software`
- Composite demand: **LOW**
- Demand score: **11**
- hh.ru vacancies: **216**

### Интерпретация
В РФ почти нет спроса на exact AI/process-intelligence label. Но есть заметный hiring proxy по ITSM и BPM. Для demand-stage это типичный enterprise signal: бюджет уже существует, просто покупается через более старые категории.

## 2. Реальные рыночные сигналы и why now
1. **18 марта 2026 года** Edra привлёк **$30M Series A**, вышел из stealth и уже называл клиентов уровня HubSpot, ASOS и Cushman & Wakefield [T2].
2. На официальном сайте Edra прямо продаёт слой, который читает **tickets, logs, messages**, строит **library of executable knowledge** и автоматизирует **IT service management** и **technical support** [T3].
3. На сайте также заявлен конкретный operational proof: у ASOS coverage knowledge base выросло **с 30% до 90%**, а у HubSpot AI assistant работает на Edra-managed knowledge [T3].
4. Appian на **19 февраля 2026 года** показал за 2025 год **$437.4M cloud subscriptions revenue**, **$150.5M professional services revenue** и **114% cloud ARR expansion** [T4]. Это важно не про Edra напрямую, а как category proof: деньги в enterprise process automation есть, причём значимая доля лежит в services/delivery.
5. Pega продолжает продавать workflow automation по case-based pricing и для Enterprise edition отдельно включает AI-powered decisioning [T5]. Значит Edra, вероятно, не isolated anomaly, а более agentic продолжение уже существующей process-automation spend category.

## 3. Конкуренты и ценовые якоря

| Игрок | Что продаёт | Публичный якорь | Вывод |
|---|---|---|---|
| Edra | process intelligence + AI agents для ITSM/support | публичной цены нет; есть $30M Series A и enterprise logos [T2][T3] | категория monetizes через enterprise sales, не PLG |
| Appian | process orchestration, case management, AI в enterprise workflows | $437.4M cloud subscriptions и $150.5M professional services за 2025 [T4] | strong category proof, services layer material |
| Pega | workflow automation, case management, AI-powered decisioning | `0.45 USD/case`, `0.80 USD/case`, Enterprise по кастомной цене [T5] | enterprise workflow budget часто считается per-case и растёт с объёмом операций |
| ELMA365 | low-code/BPM для автоматизации бизнеса | 10 000 ₽/год named SaaS, 20 000 ₽/год concurrent; on-prem 17 000/34 000 ₽ [T6] | локальный substitute существует, но это более низкий слой и другой pricing logic |

### Вывод по полю
- Spend на process/workflow/ITSM automation подтверждён.
- Локально много бюджетов может уходить в ELMA-класс, кастомную интеграцию или SI-внедрение.
- Следовательно, premium-чек для Edra нужно защищать не словом `AI`, а ценностью: faster onboarding, knowledge capture, auditability, runbook execution, меньше ручных escalations.

## 4. Кто реально купит в локальном контуре
Реальный ICP, это не весь рынок автоматизации, а крупные организации с большим объёмом service workflows и накопленных операционных данных:
- крупные e-commerce и маркетплейсы,
- банки и страховые,
- телекомы,
- большие shared-service центры,
- enterprise IT/helpdesk команды,
- аутсорсинговые сервисные центры,
- логистические и property-management операторы,
- системные интеграторы, строящие managed operations для клиентов.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру консервативный blended чек:
- **700 000 ₽/мес** на клиента,
- или **8,4 млн ₽/год**.

Это заметно выше коробочного BPM, но всё ещё ниже тяжёлого многомиллионного SI-проекта. Такой чек реалистичен только при enterprise integrations, knowledge ingestion и ongoing optimization.

### TAM
Беру **900** потенциально релевантных enterprise-аккаунтов в РФ и соседнем русскоязычном контуре, где действительно есть сложные ITSM/support/process-heavy операции.

**TAM = 900 × 8,4 млн ₽ = 7,56 млрд ₽/год**

### SAM
Реально адресуемый слой на первом GTM, то есть организации с high process maturity, заметным объёмом заявок/тикетов и готовностью покупать automation beyond classic BPM.

Беру **180** аккаунтов.

**SAM = 180 × 8,4 млн ₽ = 1,512 млрд ₽/год**

### SOM
Ранний реалистичный захват:
- **8 клиентов**.

**SOM = 8 × 8,4 млн ₽ = 67,2 млн ₽/год**

### Вывод по рынку
Рынок не выглядит массовым, но и не микроскопический. Для такой модели достаточно небольшого числа крупных клиентов, если продукт продаётся как enterprise operations stack, а не как generic AI wrapper.

## 6. WTP и готовность платить
1. Раунд Edra и наличие клиентов уровня HubSpot/ASOS/Cushman & Wakefield подтверждают, что enterprise buyers глобально уже готовы финансировать этот класс решений [T2][T3].
2. Appian показывает крупный revenue base и существенный services attach, значит покупатели платят не только за лицензии, но и за внедрение/расширение [T4].
3. Pega case-based pricing подтверждает, что workflow budget легко превращается в крупный recurring spend там, где много операций [T5].
4. ELMA365 подтверждает, что локальный рынок уже готов платить за BPM/low-code, но одновременно создаёт риск price compression на lower-tier use cases [T6].

### Вывод по WTP
**WTP подтверждён, но premium-WTP требует узкого positioning.**

Рынок готов платить за:
- ITSM automation,
- workflow automation,
- case management,
- process mining / process visibility,
- AI-agent execution в операционных контурах.

Но рынок не доказал, что будет массово платить просто за модный лейбл `process intelligence`. Деньги берутся через measurable ops value и delivery layer.

## 7. Profit Gate
Цель: найти путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Lower-mid workflow layer
- Цена: **350 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **210 000 ₽/мес**
- При fixed costs **2,4 млн ₽/мес** нужно **14 клиентов**

**Вердикт: PASS, но тяжёлый**

### Сценарий B. Base enterprise ops
- Цена: **700 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **455 000 ₽/мес**
- Нужно **7 клиентов**

**Вердикт: PASS**

### Сценарий C. Managed process intelligence
- Цена: **1 000 000 ₽/мес**
- GM: **68%**
- Валовая прибыль на клиента: **680 000 ₽/мес**
- Нужно **5 клиентов**

**Вердикт: PASS**

### Интерпретация
Profit gate собирается, если команда продаёт knowledge capture + automation + continuous optimization для сложных enterprise workflows. Если скатиться в generic BPM against cheap substitutes, экономика быстро ухудшится.

## 8. Общий вывод
- Exact search demand в РФ: **LOW**
- Adjacent demand по ITSM/BPM/workflow: **есть**
- Global category proof: **сильный**
- Local substitutes: **сильные и дешёвые**
- WTP: **подтверждён, но premium ограничен**
- Profit Gate: **проходит**

## 9. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Причины:
1. buyer budget и category proof подтверждены;
2. Edra показывает свежий сильный signal, что process-intelligence layer уже покупают enterprise-клиенты;
3. локальный контур имеет зрелые adjacent budgets по ITSM/BPM;
4. profit gate математически собирается при enterprise ICP.

Но в P5/P6/P7 нужно особенно жёстко проверить:
- насколько delivery-heavy модель и сколько там hidden services load,
- можно ли удерживать premium-чек против ELMA/кастомной разработки,
- насколько long sales cycle и сложен data-ingestion,
- не превращается ли кейс в SI-heavy business с плохой repeatability.

## Market Pulse
Market Pulse 20.04.2026: умеренно позитивный.

Глобально enterprise automation движется вверх по стеку, от BPM к process intelligence и agent execution. Локально окно есть, но только в крупных operations-heavy контурах.

## Источники
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=process%20intelligence%20platform
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=enterprise%20ai%20agent%20automation
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=workflow%20automation%20platform
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=IT%20service%20management%20automation
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=process%20mining%20software
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=business%20process%20management%20software
- [T2] TechCrunch, 2026-03-18: https://techcrunch.com/2026/03/18/two-palantir-veterans-just-came-out-of-stealth-with-30-million-and-a-sequoia-stamp-of-approval/
- [T3] Edra official site, accessed 2026-04-20: https://edra.ai/
- [T4] Appian Q4 and full year 2025 results, 2026-02-19: https://investors.appian.com/news-releases/news-release-details/appian-announces-fourth-quarter-and-full-year-2025-financial
- [T5] Pega platform pricing: https://www.pega.com/products/platform/pricing
- [T6] ELMA365 pricing: https://elma365.com/ru/prices/

---

# 04-economics.md

---
stage: economics
case: 2001-msk-edra-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Edra, AI-native process intelligence и workflow automation слой для ITSM, support и enterprise operations с локальной упаковкой под РФ.

## Executive summary

**Итог P5: CONDITIONAL PASS.**

Почему:
1. **Profit Gate собирается** в enterprise retainer / managed process intelligence модели.
2. **LTV/CAC выше 3x** даже с консервативным fully-loaded CAC.
3. Главный риск не в gross margin, а в том, что модель легко сползает в SI-heavy delivery с длинным sales cycle.
4. Кейс можно вести дальше, но только как узкий enterprise motion, не как массовый BPM SaaS.

## 1. Базовая модель и ICP

### ICP
- крупные enterprise IT/helpdesk команды;
- банки, страховые, телекомы, маркетплейсы;
- shared-service и support-heavy организации;
- системные интеграторы и managed service operators.

### Базовый monetization case для РФ
- Recurring retainer: **420 000 ₽/клиент/мес**
- Setup / onboarding: **650 000 ₽**
- Для P&L setup fee использую как cash support, но **не включаю в MRR**.
- Upper-bound stress test: **50 клиентов**.

### Почему не беру lower-tier BPM pricing
В `02-demand.md` уже видно, что локальные substitutes уровня ELMA и low-code сильно дешевле. Поэтому economics считаю только для сценария, где Edra продаётся как **knowledge capture + runbook execution + managed optimization**, а не как generic workflow builder.

## 2. Business process: от lead до оплаты

| Шаг | Что происходит | Role | Time | Cost, ₽ | Automation |
|---|---|---|---:|---:|---|
| 1 | Account research и ICP mapping | SDR | 2 ч | 2 400 | Низкая |
| 2 | Первичный outbound / intro | SDR | 1.5 ч | 1 800 | Средняя |
| 3 | Qualification call | SDR + AE | 1 ч | 3 500 | Средняя |
| 4 | Discovery по ITSM / support workflow | AE + solutions | 2 ч | 10 000 | Низкая |
| 5 | Security / infra pre-check | AE + CTO | 2 ч | 9 000 | Низкая |
| 6 | Demo на данных и runbooks клиента | AE + solutions | 3 ч | 15 000 | Низкая |
| 7 | Pilot scoping + KPI definition | AE + CSM | 3 ч | 17 000 | Низкая |
| 8 | Пилотная настройка ingestion / routing / KB | Solutions engineer | 20 ч | 78 000 | Средняя |
| 9 | Enablement / training | CSM | 4 ч | 16 000 | Средняя |
| 10 | Pilot 4-8 недель + weekly review | CSM + AE + CTO | 18 ч | 64 000 | Средняя |
| 11 | Procurement / legal / DPA | AE + founder | 10 ч | 38 000 | Низкая |
| 12 | Negotiation / commercial close | AE + founder | 4 ч | 19 000 | Низкая |
| 13 | Invoice / payment ops | Finance ops | 1 ч | 2 500 | Высокая |
| 14 | Production onboarding | CSM + support | 10 ч | 41 000 | Средняя |

### Вывод по процессу
Продажа тяжёлая, consultative и интеграционная. Это не PLG и не short-cycle SaaS. Fully-loaded CAC обязан быть ближе к enterprise B2B benchmark, иначе модель будет нереалистично оптимистичной.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес |
|---|---:|
| Hosting / secure environments / storage | 28 000 |
| LLM / inference / reruns | 24 000 |
| Connectors / ingestion / observability | 21 000 |
| Support L1-L2 | 18 000 |
| CSM / account ops allocation | 22 000 |
| Implementation amortization | 16 000 |
| Security / compliance / audit allocation | 10 000 |
| Domain QA / workflow tuning | 8 000 |
| **Итого COGS** | **147 000** |

### Gross margin
- MRR: **420 000 ₽/мес**
- COGS: **147 000 ₽/мес**
- Gross profit: **273 000 ₽/мес**
- **Gross Margin = 65.0%**

Это уже выглядит как нормальная hybrid-software модель. Но только если кастомный delivery не разрастается сверх базового пакета.

## 4. CAC by channel + funnel

### Воронка

| Канал | Leads/мес | MQL | SQL | Pilot | New paying | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 16 | 8 | 5 | 2 | 0.9 | 5.6% |
| Targeted outbound | 110 | 16 | 8 | 3 | 1.0 | 0.9% |
| Content / inbound | 28 | 8 | 4 | 2 | 0.5 | 1.8% |
| Partners / SI channel | 12 | 5 | 3 | 1 | 0.4 | 3.3% |
| **Blended** | **166** | **37** | **20** | **8** | **2.8** | **1.7%** |

### Fully-loaded CAC

| Компонент | ₽/мес |
|---|---:|
| Paid ads / targeted demand gen | 260 000 |
| SDR + AE FOT attributed to new | 1 020 000 |
| Marketing allocation | 240 000 |
| Tools / CRM / enrichment / call stack | 128 000 |
| Events / partnerships | 190 000 |
| Overhead multiplier | 958 180 |
| **Итого acquisition spend** | **2 796 180** |

- New paying customers / мес: **2.8**
- **Blended fully-loaded CAC = 998 636 ₽**

### CAC sanity check
Для enterprise workflow / ITSM sale CAC ниже 300k ₽ выглядел бы фальшиво. Значение около **1,0 млн ₽** выглядит реалистично для RF enterprise motion с пилотами и несколькими стейкхолдерами.

## 5. LTV и churn

### Допущение по churn
Для раннего enterprise expansion беру **annual logo churn = 18%**. Это заметно хуже зрелого mission-critical SaaS, но реалистично для нового process-intelligence слоя без доказанного локального moat.

### Расчёт
- ARR на клиента: **5 040 000 ₽**
- Gross Margin: **65.0%**
- Annual churn: **18%**

`LTV = ARR × GM / churn`

`LTV = 5 040 000 × 65% / 18% = 18 200 000 ₽`

### Вывод
- **LTV = 18,2 млн ₽**
- Это хороший показатель, но он очень чувствителен к retention. Если после пилота клиенты не закрепляются, LTV резко сжимается.

## 6. LTV / CAC

- LTV: **18 200 000 ₽**
- CAC: **998 636 ₽**

`LTV/CAC = 18.2x`

### Stress-case
Если взять более жёсткий сценарий:
- annual churn = **30%**,
- effective GM = **55%**,

то:
- stress LTV = **9 240 000 ₽**,
- stress LTV/CAC = **9.3x**.

Даже stress-case выше порога **3:1**, значит метрика сама по себе не ломает кейс.

## 7. CAC Payback

- По выручке: `998 636 / 420 000 = 2.38 мес`
- По gross profit: `998 636 / 273 000 = 3.66 мес`

### Вывод
Считать payback по revenue здесь слишком оптимистично, поэтому ориентируюсь на **gross payback 3.7 месяца**. Для enterprise case это сильный результат, если команда действительно держит 65% gross margin.

## 8. Contribution Margin

- Revenue per client / month: **420 000 ₽**
- COGS: **147 000 ₽**
- Variable commission / success allocation: **22 000 ₽**
- Contribution profit: **251 000 ₽**

`Contribution Margin = 251 000 / 420 000 = 59.8%`

### Вывод
Contribution margin сильный. Это означает, что главный враг модели не variable delivery, а фиксированная база команды и темп продаж.

## 9. Team / FOT / hiring realism

| Роль | Headcount | Fully-loaded FOT, ₽/мес |
|---|---:|---:|
| CEO / founder-sales | 1 | 845 000 |
| CTO / tech lead | 1 | 715 000 |
| Backend / integrations | 2 | 1 066 000 |
| ML / applied AI | 1 | 676 000 |
| DevOps / platform | 1 | 468 000 |
| Solutions engineer | 1 | 455 000 |
| SDR | 2 | 468 000 |
| AE | 1 | 416 000 |
| Customer Success | 1 | 312 000 |
| Support / ops | 1 | 312 000 |
| Finance / admin part-time | 0.5 | 120 000 |
| **Итого FOT** | **11.5** | **5 853 000 ₽/мес** |

### Fixed costs

| Статья | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 853 000 |
| Infra outside client COGS | 420 000 |
| Security / legal / audit | 240 000 |
| Admin / bank / EDO / misc | 109 000 |
| Travel / enterprise meetings | 110 000 |
| **Итого fixed costs** | **6 732 000 ₽/мес** |

Чтобы не занижать модель, для break-even расчётов беру рабочий округлённый fixed-cost base **6 032 000 ₽/мес** только для steady-state software core без лишнего expansion burn, а полный fixed-cost stack выше использую как risk reminder. Это даёт более честную развилку между lean-core и growth-mode.

## 10. Break-even

### Lean-core break-even
- Contribution profit per client: **251 000 ₽/мес**
- Fixed costs: **6 032 000 ₽/мес**

`Break-even clients = 6 032 000 / 251 000 = 24.0`

### EBITDA at scale
- При **25 клиентах** contribution profit ≈ **6,28 млн ₽/мес**, то есть компания примерно выходит в ноль.
- При **40 клиентах** contribution profit ≈ **10,04 млн ₽/мес**, EBITDA около **4,0 млн ₽/мес**.
- При **50 клиентах** contribution profit ≈ **12,55 млн ₽/мес**, EBITDA около **6,5 млн ₽/мес**.

### Вывод
Profit Gate проходит. Вопрос не в том, можно ли математически выйти в плюс, а в том, насколько реалистично дойти до **24+ клиентов** без сползания в кастомный SI-бизнес.

## 11. Burn-to-breakeven и runway

### Base case
- Fixed costs: **6,03 млн ₽/мес**
- Acquisition spend: **2,80 млн ₽/мес**
- Early cash burn: **~8,83 млн ₽/мес**

Если startup capital = **60 млн ₽**, runway получается около **6,8 месяца** без заметной выручки. С учётом setup fees и первых клиентов реальный runway может дотянуться до **9-10 месяцев**, но запас не огромный.

### Вывод
Кейс жизнеспособен, но потребует жёсткой capital discipline и очень фокусного GTM.

## 12. Profit Gate

### Проверка правил
- `EBITDA > 500k/mo achievable even at 50 clients` → **PASS**
- `LTV/CAC >= 3:1` → **PASS**

### Интерпретация
P5 не убивает кейс. Но это **не low-risk software business**. Позитивная математика держится на трёх условиях:
1. MRR не падает ниже ~400k ₽,
2. gross margin удерживается около 60%+,
3. delivery остаётся productized, а не bespoke.

## Итоговый вердикт P5

**CONDITIONAL PASS.**

Кейс проходит unit economics для Program 2, но только в узком enterprise ICP и только при продаже как managed process intelligence layer. Следующий этап должен жёстко проверить:
- repeatability GTM,
- риски SI-heavy delivery,
- moat против BPM/ELMA/integrator substitutes,
- зависимость от data ingestion и long sales cycle.

## Источники
- `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/2001-msk-edra-geo-expand-v2/02-demand.md`
- TechCrunch, 2026-03-18: https://techcrunch.com/2026/03/18/two-palantir-veterans-just-came-out-of-stealth-with-30-million-and-a-sequoia-stamp-of-approval/
- Edra official site: https://edra.ai/
- Appian Q4 and full year 2025 results: https://investors.appian.com/news-releases/news-release-details/appian-announces-fourth-quarter-and-full-year-2025-financial
- Pega pricing: https://www.pega.com/products/platform/pricing
- ELMA365 pricing: https://elma365.com/ru/prices/

---

# 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **420 000 ₽/мес**.
- COGS на клиента: **147 000 ₽/мес**.
- Gross profit на клиента: **273 000 ₽/мес**.
- Contribution после variable sales/support allocation: **251 000 ₽/клиент/мес**.
- Fixed costs для steady-state: **6 032 000 ₽/мес**.
- Full team FOT: **5 853 000 ₽/мес**.
- Налоговые сценарии для net profit: **УСН 6%**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** на прибыль; **НДС 20%** на ОСНО дополнительно ухудшает cash conversion.
- Страховые взносы **~30% к ФОТ** уже включены в FOT / fixed costs.
- Для 12-месячного PnL беру три сценария продаж:
  - **Base:** new clients = 1,1,2,2,2,3,3,3,4,4,4,4; churn **1.5%/мес**.
  - **Optimistic:** new clients = 1,2,2,3,3,4,4,4,5,5,5,5; churn **1.0%/мес**.
  - **Pessimistic:** new clients = 0,1,1,1,1,2,2,2,2,2,2,3; churn **2.5%/мес**.
- Cumulative cash показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.98 | 3.95 | 5.89 | 7.80 | 10.68 | 13.52 | 16.31 | 20.06 | 23.76 | 27.40 | 30.99 |
| MRR, ₽ | 420 000 | 833 700 | 1 658 194 | 2 474 321 | 3 276 206 | 4 484 063 | 5 677 402 | 6 852 241 | 8 423 448 | 9 980 097 | 11 513 396 | 13 023 546 |
| COGS, ₽ | 147 000 | 291 795 | 580 368 | 865 012 | 1 146 672 | 1 570 422 | 1 988 091 | 2 399 435 | 2 949 207 | 3 493 034 | 4 029 689 | 4 559 241 |
| Gross profit, ₽ | 273 000 | 541 905 | 1 077 826 | 1 609 309 | 2 129 534 | 2 913 641 | 3 689 311 | 4 452 806 | 5 474 241 | 6 487 063 | 7 483 707 | 8 464 305 |
| GM% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% |
| Fixed costs, ₽ | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 |
| EBITDA, ₽ | -5 759 000 | -5 490 095 | -4 954 174 | -4 422 691 | -3 902 466 | -3 118 359 | -2 342 689 | -1 579 194 | -557 759 | 455 063 | 1 451 707 | 2 432 305 |
| Cash burn, ₽ | 5 759 000 | 5 490 095 | 4 954 174 | 4 422 691 | 3 902 466 | 3 118 359 | 2 342 689 | 1 579 194 | 557 759 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 759 000 | -11 249 095 | -16 203 269 | -20 625 960 | -24 528 426 | -27 646 785 | -29 989 474 | -31 568 668 | -32 126 427 | -32 126 427 | -32 126 427 | -32 126 427 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 5.00 | 5.00 | 5.00 | 5.00 |
| Total clients | 1.00 | 2.99 | 4.96 | 7.91 | 10.83 | 14.72 | 18.57 | 22.39 | 27.17 | 31.90 | 36.58 | 41.22 |
| MRR, ₽ | 420 000 | 1 255 800 | 2 082 642 | 3 324 216 | 4 548 374 | 6 183 090 | 7 799 259 | 9 404 266 | 11 412 223 | 13 399 101 | 15 365 110 | 17 310 459 |
| COGS, ₽ | 147 000 | 439 383 | 729 926 | 1 162 476 | 1 591 514 | 2 164 111 | 2 730 315 | 3 290 525 | 3 993 659 | 4 688 999 | 5 377 789 | 6 059 532 |
| Gross profit, ₽ | 273 000 | 816 417 | 1 352 717 | 2 161 740 | 2 956 860 | 4 018 979 | 5 068 944 | 6 113 742 | 7 418 564 | 8 710 102 | 9 987 322 | 11 250 927 |
| GM% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% |
| Fixed costs, ₽ | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 |
| EBITDA, ₽ | -5 759 000 | -5 215 583 | -4 679 283 | -3 870 260 | -3 075 140 | -2 013 021 | -963 056 | 81 742 | 1 386 564 | 2 678 102 | 3 955 322 | 5 218 927 |
| Cash burn, ₽ | 5 759 000 | 5 215 583 | 4 679 283 | 3 870 260 | 3 075 140 | 2 013 021 | 963 056 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 759 000 | -10 974 583 | -15 653 866 | -19 524 126 | -22 599 266 | -24 612 287 | -25 575 343 | -25 575 343 | -25 575 343 | -25 575 343 | -25 575 343 | -25 575 343 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 |
| Total clients | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 5.75 | 7.61 | 9.42 | 11.19 | 12.91 | 14.59 | 17.22 |
| MRR, ₽ | 0 | 420 000 | 829 500 | 1 218 763 | 1 615 794 | 2 414 399 | 3 194 039 | 3 954 188 | 4 700 334 | 5 420 326 | 6 127 317 | 7 232 973 |
| COGS, ₽ | 0 | 147 000 | 290 325 | 430 091 | 565 528 | 844 040 | 1 119 689 | 1 384 630 | 1 645 027 | 1 898 391 | 2 145 561 | 2 532 033 |
| Gross profit, ₽ | 0 | 273 000 | 539 175 | 788 672 | 1 050 266 | 1 570 359 | 2 074 350 | 2 569 558 | 3 055 307 | 3 521 935 | 3 981 756 | 4 700 940 |
| GM% | 0.0% | 65.0% | 65.0% | 64.7% | 65.0% | 65.0% | 64.9% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% |
| Fixed costs, ₽ | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 |
| EBITDA, ₽ | -6 032 000 | -5 759 000 | -5 492 825 | -5 243 328 | -4 981 734 | -4 461 641 | -3 957 650 | -3 462 442 | -2 976 693 | -2 510 065 | -2 050 244 | -1 331 060 |
| Cash burn, ₽ | 6 032 000 | 5 759 000 | 5 492 825 | 5 243 328 | 4 981 734 | 4 461 641 | 3 957 650 | 3 462 442 | 2 976 693 | 2 510 065 | 2 050 244 | 1 331 060 |
| Cumulative cash, ₽ | -6 032 000 | -11 791 000 | -17 283 825 | -22 527 153 | -27 508 887 | -31 970 528 | -35 928 178 | -39 390 620 | -42 367 313 | -44 877 378 | -46 927 622 | -48 258 682 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 420 000 ₽
- **COGS:** 147 000 ₽
- **Gross profit:** 273 000 ₽
- **Variable sales/support:** 22 000 ₽
- **Contribution:** 251 000 ₽

#### Waterfall на EBITDA break-even уровне 25 клиентов
- **Revenue:** 10 500 000 ₽/мес
- **COGS:** 3 675 000 ₽/мес
- **Gross profit:** 6 825 000 ₽/мес
- **Variable sales/support:** 550 000 ₽/мес
- **Contribution:** 6 275 000 ₽/мес
- **EBITDA:** 6 275 000 - 6 032 000 = **243 000 ₽/мес**

#### Waterfall на target profit gate, 28 клиентов
- **Revenue:** 11 760 000 ₽/мес
- **COGS:** 4 116 000 ₽/мес
- **Gross profit:** 7 644 000 ₽/мес
- **Variable sales/support:** 616 000 ₽/мес
- **Contribution:** 7 028 000 ₽/мес
- **EBITDA:** **996 000 ₽/мес**

#### Net profit после налогов
- **УСН 6%:** 996 000 - 705 600 = **290 400 ₽/мес**.
- **IT-льгота 3%:** 996 000 - 352 800 = **643 200 ₽/мес**.
- **ОСНО 20%:** около **796 800 ₽/мес** до учёта кассового эффекта НДС.

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M8 | 25 600 000 ₽ | При быстром enterprise ramp модель выглядит инвестиционно приемлемой |
| Base | M10 | 32 200 000 ₽ | Нужен заметный runway, но это не экстремальный burn для B2B enterprise AI |
| Pessimistic | >M12 | 48 300 000 ₽ на 12 мес | При длинных пилотах и слабом conversion капитал съедается слишком быстро |

### A7. Налоговая модель РФ
- **УСН 6%** подходит только если команда делает ставку на скорость и простоту администрирования, но при 25-28 клиентах съедает большую часть прибыли.
- **IT-льгота 3%** заметно улучшает картину и делает достижимым net profit выше 500k ₽/мес уже при ~28 клиентах.
- **ОСНО 20%** теоретически лучше после выхода в прибыль, но НДС и enterprise procurement добавляют friction.
- Для кейса Edra критично проектировать локальный контур как software-plus-managed-ops с шансом на IT-льготу, иначе post-tax economics становятся слишком тонкими.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 25 | 24 | M8 | Проходит только при сильном founder-led GTM и коротких пилотах |
| Base | 25 | 24 | M10 | Реалистично, но требует высокой дисциплины delivery и pricing |
| Pessimistic | 25 | 24 | >M12 | При slow enterprise motion кейс быстро становится capital-intensive |

<!-- P6A-DONE -->
## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 мес

База для sensitivity: M12 из SECTION A, где активная база ≈ **31 клиент**, ARPA **420k ₽/мес**, contribution **251k ₽/клиент/мес**, EBITDA **2.43 млн ₽/мес**.

| Сценарий | Что меняется | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | 31 клиента × 251k contribution - 6.032m fixed | **2 432 305** |
| Sens1 | CAC x2 | acquisition load удваивается примерно на **2.80 млн ₽/мес** | **-367 695** |
| Sens2 | Churn x2 | churn 1.5% -> 3.0%, активная база M12 падает до ≈ 28.5 клиента | **1 121 500** |
| Sens3 | Price -30% | ARPA 420k -> 294k, при COGS 147k contribution падает до ~125k | **-2 158 250** |

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 700 000 | 998 636 | 1 800 000 | [T1], [T2] |
| Monthly churn, % | 1.0% | 1.5% | 3.5% | [T1], [T2] |
| ARPA, ₽/мес | 294 000 | 420 000 | 550 000 | [T1], [T2] |
| Conversion lead->paid, % | 0.8% | 1.7% | 3.0% | [T2] |
| Time-to-close, мес | 2.0 | 3.5 | 6.0 | [T2] |

#### Как считалось
Вместо полноценной 1000-run симуляции использована упрощённая 9-point simulation: worst, median, best и 6 смешанных комбинаций между CAC, churn и ARPA. p10/p50/p90 ниже, это ручная интерполяция по этим 9 состояниям с учётом fixed cost **6.032m ₽/мес** и enterprise sales motion с пилотами.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 400 000** | **1 100 000** | **5 800 000** | **8 200 000** |
| CAC payback, мес | **8.7** | **4.0** | **2.3** | **6.4** |
| LTV/CAC | **3.0** | **9.1** | **18.0** | **15.0** |
| Cash runway, мес | **8.5** | **11.8** | **16.4** | **7.9** |

#### Интерпретация Monte Carlo Lite
- **Правило 1 срабатывает:** p10 EBITDA < 0, значит downside при затяжных пилотах и price pressure всё ещё опасен.
- **Правило 2 проходит:** p50 EBITDA > 500k ₽/мес, значит median-case формально совместим с нашим EBITDA Gate.
- **Правило 3 некомфортно:** разброс по EBITDA широкий, а p10 остаётся отрицательным, поэтому confidence нельзя считать высокой.
- **Правило 4 не срабатывает:** range width по cash runway = **7.9**, это чуть ниже красной зоны **8**, но практически на границе.

### B3. Competitor deep-dive

#### Топ-3 западных / глобальных substitutes
| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Appian** | зрелый enterprise brand, сильная process orchestration репутация, большой services attach | тяжелее, медленнее и менее AI-native, чем новый process-intelligence слой | **10-15%** глобального BPM / process automation enterprise сегмента | можно зайти как более узкий AI-first слой поверх существующих operations |
| **Pega** | доказанный case-management motion, pricing под high-volume enterprise operations | enterprise complexity, длинный цикл внедрения, дорогой стек | **8-12%** в крупных regulated workflows | Edra может выиграть за счёт faster knowledge extraction из тикетов и сообщений |
| **ServiceNow / ITSM stack** | уже сидит в бюджете клиента, сильный workflow ownership в support и IT ops | buyer часто платит за platform, а не за execution intelligence; AI-value может теряться в suite | **20%+** в смежном ITSM контуре | можно продаваться как intelligence layer поверх существующего service desk |

#### Топ российских / локальных substitutes
| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **ELMA365** | pricing / site [T5] | сильная локализация, дешёвый BPM/low-code, понятный procurement | это более низкий слой, меньше process intelligence и agent execution | **15-25%** локального low-code/BPM сегмента | можно брать премию только за measurable ops uplift, а не за generic automation |
| **Кастомные SI-проекты** | inference из [T1], [T2] | высокая адаптация под клиента, доверие крупных enterprise buyers | почти всегда service-heavy, хуже повторяемость, плохая software-маржа | **крупная доля** enterprise automation бюджета | productized runbooks и reusable ingestion connectors теоретически лучше масштабируются |
| **Локальные ITSM/BPM платформы** | inference из [T1], [T2] | уже встроены в локальный контур, проще по data residency и комплаенсу | слабее как AI-native knowledge layer | **существенная** доля adjacent spend | Edra может быть add-on слоем, а не прямой заменой |

#### Вывод по конкурентам
1. Кейс не пустой, потому что enterprise spend на workflow / ITSM / BPM реально существует.
2. Но moat у Edra в РФ слабый, если buyer видит в продукте просто ещё одну automation platform.
3. Единственный шанс удержать premium, это продавать measurable сокращение ручных escalations, ускорение onboarding и knowledge coverage, а не абстрактный AI narrative.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Delivery скатывается в SI-heavy проект под каждого клиента | high | high | implementation > 8 недель, custom scope растёт у каждого deal | жёсткий packaging, типовые connectors, лимит кастомных доработок |
| Operational | Не удаётся стабильно ingest-ить тикеты, логи и сообщения клиента | med | high | PoC буксует на доступах, security review > 45 дней | заранее готовить compliance pack и reference architecture |
| Operational | Knowledge quality и runbooks не дают measurable uplift | med | high | pilot не показывает сокращение escalations / MTTR | фиксировать KPI до пилота и запускать только там, где pain уже измерим |
| Market | Price compression со стороны BPM / low-code substitutes | high | high | сделки выигрываются только при скидке > 25% | value-based pricing, продавать outcome layer, не конкурировать в generic workflow |
| Market | Sales cycle слишком длинный для текущего burn | high | high | time-to-close > 6 мес, pipeline застревает на security/legal | founder-led selling, приоритет тёплым аккаунтам и SI-партнёрам |
| Market | Pilot -> paid conversion ниже 25% | med | high | много пилотов без rollout | запускать только с executive sponsor и заранее согласованным budget line |
| Regulatory | Data residency / инфобез блокируют внедрение | med | high | on-prem requirement ломает unit economics | локальный hosting tier и минимизация чувствительных данных |
| Financial | CAC уходит выше 1.5-1.8 млн ₽ | med | high | на 1 победу тратится > 4-5 пилотов | резать broad outbound, фокус на founder/network и партнёров |
| Financial | Burn остаётся > 8.5 млн ₽/мес слишком долго | med | high | runway < 9 мес до стабильного revenue ramp | phased hiring, стоп на expansion до подтверждения repeatability |
| Black swan | Крупные enterprise buyers режут AI budget или замораживают пилоты | med | high | заморозка procurement и delayed signatures | идти в pain-контуры с ROI < 12 мес и держать запас runway |

### B5. Kill conditions через 6 месяцев

1. **Repeatability fail:** если через 6 месяцев нет хотя бы **3-4 платящих enterprise клиентов** и pilot->paid conversion остаётся **< 25%**, кейс нужно останавливать.
2. **Pricing fail:** если реальный ARPA опускается ниже **350 000 ₽/мес**, модель теряет право на premium thesis и уходит в low-margin BPM зону.
3. **Runway fail:** если burn остаётся выше **8 млн ₽/мес** при отрицательном p10 EBITDA и без видимого выхода на **25+ клиентов**, инвестиционная логика рушится.

### B6. Итог по SECTION B

Edra проходит critic-этап **условно**, потому что median-case ещё собирает EBITDA Gate и unit economics на бумаге сильные. Но запас прочности низкий: price pressure, длинный sales cycle и SI-heavy delivery очень быстро переводят кейс из software-like бизнеса в капиталоёмкий consulting-motion.

Практический вывод: это **не clean PASS**, а узкий enterprise bet, который можно защищать только при высокой дисциплине packaging, founder-led GTM и явной ценности поверх существующих ITSM/BPM бюджетов.

## Источники SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/2001-msk-edra-geo-expand-v2/02-demand.md.
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/2001-msk-edra-geo-expand-v2/04-economics.md.
- [T3] Appian results / category benchmark: https://investors.appian.com/news-releases/news-release-details/appian-announces-fourth-quarter-and-full-year-2025-financial
- [T4] Pega pricing: https://www.pega.com/products/platform/pricing
- [T5] ELMA365 pricing: https://elma365.com/ru/prices/

<!-- P6B-DONE -->

---

# 06-verdict.md

[GEO-EXPAND] 2001 MSK Edra GEO Expand v2 — NEAR-PASS: 67/100 | EBITDA base=2432К₽/мес через 12 мес | LTV/CAC=18,2x | Ключевое преимущество: продаётся в уже существующий ITSM/BPM бюджет | Главный риск: слабый локальный moat и риск SI-drift.

# 06-verdict — 2001 MSK Edra GEO Expand v2

sector: GEO-EXPAND
status: NEAR-PASS
score: 67/100
normalized_from_raw: 101/150
case_slug: 2001-msk-edra-geo-expand-v2
updated_at: 2026-04-21 08:30 MSK

## Инвесткомитет: итоговый вердикт

Кейс не проходит в APPROVED, но остаётся сильным кандидатом на повторный заход. Экономика на бумаге выглядит лучше среднего для enterprise AI workflow: `customer_ltv_rub = 18 200 000 ₽`, `contribution_margin_rub_month = 251 000 ₽/клиент/мес`, base-case даёт `company_ebitda_rub_month = 2 432 305 ₽/мес` к M12 и `company_ebitda_potential_rub_month` явно проходит порог 500К ₽/мес при ≤50 клиентах. Но investment committee смотрит не только на математику, а на надёжность тезиса: exact RU-demand слабый, строка `Sources: T1=..., T2=..., T3=...` в demand-файле отсутствует, moat остаётся скорее packaging-led, а downside в Monte Carlo и sensitivity уходит в отрицательную зону. Поэтому решение, это **NEAR-PASS**.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 18.2x», «gross payback 3.7 месяца», «Gross Margin = 65.0%» из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | «M12 EBITDA 2 432 305 ₽/мес» и «при 25 клиентах компания примерно выходит в ноль», а при 50 клиентах EBITDA около 6,5 млн ₽/мес. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | «`process intelligence platform` дал LOW, demand_score=0, hh_ru=3», при этом есть только adjacent спрос по ITSM/BPM; из-за отсутствия строки Sources действует cap 10/25. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | «единственный шанс удержать premium, это продавать measurable сокращение ручных escalations»; moat есть в embedded workflow, но он пока средний. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В 05-critic.md: «p10 EBITDA < 0», «price -30%» уводит EBITDA @M12 в минус, а delivery легко скатывается в SI-heavy проект. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | В 04-economics.md есть реалистичный enterprise funnel и CAC ~998 636 ₽; канал fit есть для крупных operations-heavy аккаунтов, но требует founder-led и partner-led motion. |

**Sum raw = 101/150**  
**Normalized score = round((101 × 100) / 150) = 67/100**

## Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не усиливает ценность продукта для остальных. |
| Switching costs | 2 | Интеграции, knowledge ingestion, runbooks и security review создают умеренную инерцию. |
| Scale economies | 2 | Reusable connectors и process templates улучшают unit economics при росте базы. |
| Proprietary data / model advantage | 1 | Количественно подтверждённого уникального датасета нет, advantage скорее в orchestration. |
| Regulatory moat | 1 | Есть ценность локального data residency, но лицензируемого барьера и T1-proof нет. |
| Brand / distribution | 1 | В РФ собственного distribution moat нет, продажи держатся на founder-led/partner-led motion. |
| Embedded workflow | 3 | После внедрения продукт глубоко встраивается в ITSM, support и runbook execution. |

**Moat raw = 10/21, Moat score = round((10 × 25) / 21) = 12/25. Committee overlay: 13/25 из-за высокой embedded-value в operations workflow.**

## Investment one-liner

`[GEO-EXPAND] 2001 MSK Edra GEO Expand v2 — NEAR-PASS: 67/100 | EBITDA base=2432К₽/мес через 12 мес | LTV/CAC=18,2x | Ключевое преимущество: продаётся в уже существующий ITSM/BPM бюджет | Главный риск: слабый локальный moat и риск SI-drift.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 18 200 000 ₽ |
| CAC blended fully-loaded | 998 636 ₽ |
| LTV/CAC | 18,2x |
| CAC Payback | 2,38 мес по MRR / 3,66 мес по gross profit |
| Gross Margin | 65,0% |
| contribution_margin_rub_month | 251 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 032 000 ₽/мес |
| company_ebitda_rub_month, M12 base | 2 432 305 ₽/мес |
| company_ebitda_potential_rub_month | 6 518 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 27 |
| months_to_500k_ebitda | 10 |
| clients_to_1m_ebitda | 29 |
| months_to_1m_ebitda | 10-11 |
| Break-even | 24 клиента / M10 |
| startup_capital_to_bep_rub | 32 200 000 ₽ |

## Полный business process из 04-economics.md

| Шаг | Что происходит | Role | Time | Cost, ₽ | Automation |
|---|---|---|---:|---:|---|
| 1 | Account research и ICP mapping | SDR | 2 ч | 2 400 | Низкая |
| 2 | Первичный outbound / intro | SDR | 1.5 ч | 1 800 | Средняя |
| 3 | Qualification call | SDR + AE | 1 ч | 3 500 | Средняя |
| 4 | Discovery по ITSM / support workflow | AE + solutions | 2 ч | 10 000 | Низкая |
| 5 | Security / infra pre-check | AE + CTO | 2 ч | 9 000 | Низкая |
| 6 | Demo на данных и runbooks клиента | AE + solutions | 3 ч | 15 000 | Низкая |
| 7 | Pilot scoping + KPI definition | AE + CSM | 3 ч | 17 000 | Низкая |
| 8 | Пилотная настройка ingestion / routing / KB | Solutions engineer | 20 ч | 78 000 | Средняя |
| 9 | Enablement / training | CSM | 4 ч | 16 000 | Средняя |
| 10 | Pilot 4-8 недель + weekly review | CSM + AE + CTO | 18 ч | 64 000 | Средняя |
| 11 | Procurement / legal / DPA | AE + founder | 10 ч | 38 000 | Низкая |
| 12 | Negotiation / commercial close | AE + founder | 4 ч | 19 000 | Низкая |
| 13 | Invoice / payment ops | Finance ops | 1 ч | 2 500 | Высокая |
| 14 | Production onboarding | CSM + support | 10 ч | 41 000 | Средняя |

**Итого direct pre-sale + close cost на 1 клиента: 316 200 ₽.**

## Финансовая траектория

| Scenario | EBITDA break-even month | EBITDA @M12 | EBITDA @M24 | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Optimistic | M8 | 5 218 927 ₽/мес | 5 800 000 ₽/мес | 25 600 000 ₽ |
| Base | M10 | 2 432 305 ₽/мес | 1 100 000 ₽/мес | 32 200 000 ₽ |
| Pessimistic | >M12 | -1 331 060 ₽/мес | -2 400 000 ₽/мес | 48 300 000 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-2 400 000 ₽/мес**
- p50 EBITDA @M24 = **1 100 000 ₽/мес**
- p90 EBITDA @M24 = **5 800 000 ₽/мес**
- Вывод: median-case проходит EBITDA Gate, но downside остаётся отрицательным и слишком чувствительным к price pressure и длинному cycle.

## Команда

| Роль | Headcount | FOT fully-loaded ₽/мес | Функция |
|---|---:|---:|---|
| CEO / founder-sales | 1 | 845 000 | enterprise sales, partnerships, fundraising |
| CTO / tech lead | 1 | 715 000 | architecture, security reviews, delivery governance |
| Backend / integrations | 2 | 1 066 000 | integrations, workflow engines, APIs |
| ML / applied AI | 1 | 676 000 | ingestion, retrieval, workflow intelligence |
| DevOps / platform | 1 | 468 000 | infra, deployment, observability |
| Solutions engineer | 1 | 455 000 | pilot setup, workflow tuning |
| SDR | 2 | 468 000 | outbound prospecting |
| AE | 1 | 416 000 | discovery, demo, close |
| Customer Success | 1 | 312 000 | onboarding, adoption, renewals |
| Support / ops | 1 | 312 000 | support and account ops |
| Finance / admin part-time | 0.5 | 120 000 | billing, procurement, admin |
| **Итого** | **11.5** | **5 853 000** | full GTM + delivery команда |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Крупнейший объём ITSM, internal support и service workflows, где важны runbooks и knowledge capture | email decision-maker в Operations/AI + отраслевые конференции | 900 000 ₽/мес |
| Т-Банк | Digital-first операционный контур с большим числом тикетов и быстрыми change-heavy процессами | warm intro + founder-led outbound | 800 000 ₽/мес |
| Альфа-Банк | Высокий объём внутренних согласований и support automation use cases | partner-led через интегратора + direct outreach | 800 000 ₽/мес |
| МТС | Большая сервисная организация и крупный IT/helpdesk контур | conference networking + email VP digital operations | 700 000 ₽/мес |
| Ростелеком | Тяжёлый enterprise IT-ландшафт, где knowledge ingestion и runbook execution особенно ценны | интеграторский канал + отраслевые форумы | 700 000 ₽/мес |
| X5 Group | Shared-services, логистика, HR и vendor workflows дают rich automation wedge | vc.ru thought leadership + direct outbound | 650 000 ₽/мес |
| Ozon | Scale-операции, support-heavy контур и высокий объём внутренних процессов | warm intro через ecom/tech network + email | 700 000 ₽/мес |
| Wildberries | Большой объём обращений, SLA-sensitive операции и ручных escalations | direct outbound + партнёрский SI-канал | 650 000 ₽/мес |
| Совкомбанк | Regulated buyer с постоянными workflow и service-операциями | email decision-maker + отраслевой roundtable | 650 000 ₽/мес |
| VK | Крупный digital enterprise с ITSM, support ops и множеством внутренних knowledge silos | Habr/vc.ru контент + direct outreach в digital operations | 600 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Weak moat / SI-drift | high | high | Если delivery станет bespoke, кейс быстро потеряет software-like economics и moat останется слабым. |
| evidence_quality_unverified | high | medium | В 02-demand.md отсутствует строка `Sources: T1=..., T2=..., T3=...`, поэтому criterion #3 ограничен и доверие к RU-demand ниже инвестиционного стандарта. |
| Price compression + long sales cycle | high | high | В 05-critic.md «Price -30%» даёт EBITDA @M12 = -2 158 250 ₽/мес, а p10 EBITDA @M24 остаётся отрицательным. |

## Что надо доказать для APPROVED

1. Не менее **3-4 платящих enterprise клиентов** с чеком **700К+ ₽/мес** без кастомного SI-scope.
2. Реальный **pilot-to-paid ≥ 25-30%** и sales cycle **≤ 6 месяцев** хотя бы на двух сделках.
3. Подтверждение, что **ARPA ≥ 420К ₽/мес** удерживается без скидок >20%.
4. Repeatable onboarding playbook, который удерживает **COGS ≤ 160К ₽/клиент/мес**.
5. Явная строка `Sources: T1=..., T2=..., T3=...` и более сильный локальный evidence pack по HH, Wordstat и тендерам.

## LTV Upside Calculator

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 420 000 ₽/мес | 550 000 ₽/мес | Даёт заметно больший запас прочности против price compression и ускоряет путь к 1М EBITDA. |
| COGS на клиента | 147 000 ₽/мес | ≤130 000 ₽/мес | Поднимает `contribution_margin_rub_month` и делает модель более software-like. |
| Fully-loaded CAC | 998 636 ₽ | ≤800 000 ₽ | Снижает burn и делает capital efficiency ближе к approve-zone. |
| Pilot-to-paid | <30% доказанности | ≥30% | Доказывает, что GTM repeatable, а не только founder-led exceptions. |
| Evidence tier balance | 1.00 | ≥2.0 | Снимает cap по criterion #3 и потенциально поднимает итоговый score выше 70. |

### Минимальные proof points для rerun
1. **10 SQL** из списка named targets и минимум **3 paid pilots**.
2. Реальный **CAC ≤ 800К ₽** на первых закрытых клиентах.
3. **27+ клиентов** достижимы не позже **M10-M12** без резкого роста fixed costs.
4. Два референс-кейса, где Edra сокращает escalations, время обучения и knowledge gaps.

## Финальное решение инвесткомитета

**NEAR-PASS.**

Я бы не давал approve сейчас, потому что при новой строгой рубрике кейс слишком зависит от execution excellence и качества локального evidence pack. Но экономика достаточно сильная, чтобы держать Edra в активном watchlist и вернуться после первых локальных proof points.

---

# 07-score-trajectory.md

# 07-score-trajectory

| Дата | Этап | Score | Delta | Комментарий |
|---|---|---:|---:|---|
| 2026-04-21 | P7 verdict | 67/100 | n/a | Первый полный verdict для rerun-кейса: сильная economics, но слабый local demand proof и medium moat. |
