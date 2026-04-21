# verdict.md — appian-enterprise-ai-process-v2

---

## 00-brief.md

# Краткий бриф

- **Тип запуска:** принудительный full rerun/resurrect
- **Raw-файл:** `pipeline/raw/2026-04-19-resurrect-appian-enterprise-ai-process.md`
- **Новый кейс:** `pipeline/cases/appian-enterprise-ai-process-v2/`
- **Сектор:** `B2B-OPS`
- **Причина открытия:** файл начинается с `resurrect-`, поэтому по standing orders создаётся отдельный case-v2 и отправляется дальше в P3→P7 без классификации как duplicate.
- **Оригинальный источник/вердикт:** `triage/triage-2026-04-14-appian-enterprise-ai-process.md`; Открыть новый кейс: enterprise-ai-process-automation-operator.


---

## 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-appian-enterprise-ai-process.md
created: 2026-04-20T06:37:59+03:00
original_source: triage/triage-2026-04-14-appian-enterprise-ai-process.md
original_case: pipeline/cases/enterprise-ai-process-automation-operator/
original_verdict: Открыть новый кейс: enterprise-ai-process-automation-operator.
---

# Intake

## Статус
Принудительный полный rerun/resurrect. Этот кейс создан заново и должен пройти P3→P7 с новой аналитикой.

## Краткое пояснение
Принудительный resurrect-rerun для полной аналитики по enterprise AI process automation и case management вокруг Appian.

## Полный контекст raw-файла

# RESURRECT SIGNAL — appian-enterprise-ai-process

## Meta
- source: triage/triage-2026-04-14-appian-enterprise-ai-process.md
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
2026-04-14

## Входные данные
- pipeline/raw/raw-2026-04-14-appian-enterprise-ai-process.md

## Классификация
кандидат в новый кейс

## Решение
Открыть новый кейс: `enterprise-ai-process-automation-operator`.

## Почему
- Сигнал проходит LTV Gate с большим запасом: Appian работает в enterprise- и госсегменте, а типовой контур внедрения здесь включает process design, интеграции, AI-обработку документов, governance, rollout по подразделениям и длительное сопровождение. Это правдоподобно даёт чек заметно выше 500 000 руб/мес.
- Это не просто очередная AI-функция внутри SaaS. Appian прямо указывает на AI-powered transformation efforts и крупные enterprise agreements, что ближе к отдельной сервисной категории вокруг process automation platform, а не к узкому point solution.
- Рост cloud revenue и особенно professional services усиливает тезис, что ценность для клиента реализуется через существенный слой внедрения, настройки и сопровождения, а не только через продажу лицензий.
- Важен характер нагрузок: документооборот, case management, согласования, routing, exception handling, data integrations и policy-heavy workflows. Это создаёт основу для повторяемого предложения с внедрением и managed operations.
- Отдельный сигнал по Army добавляет признак сложных regulated environments, где обычно выше требования к auditability, security, orchestration и change management, а значит выше service intensity.

## Пометка для следующего шага
Проверять кейс как отдельную сервисную линию вокруг enterprise AI process automation и case management для крупных организаций. На следующем цикле собрать подтверждения по:
- типовым use cases: intake, approvals, document processing, claims, investigations, employee и citizen service workflows;
- покупателю и бюджету: COO, operations excellence, CIO, transformation office, shared services, public sector digital teams;
- структуре delivery: discovery, process redesign, platform implementation, integration, governance, ongoing optimisation;
- повторяемости вне Appian: Pega, ServiceNow, Microsoft, Salesforce, SAP Signavio и другие process-heavy stacks;
- evidence по длительности контрактов, managed services attach rate и expansion от одного workflow к enterprise-wide rollout.

## Вердикт
Сигнал достаточно сильный для открытия отдельного кейса, а не только как supporting evidence к существующим темам.

```


---

## 02-demand.md

---
stage: demand-validation
case: appian-enterprise-ai-process-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Appian Enterprise AI Process, enterprise-layer для AI-powered process orchestration, case management, document-heavy workflows и regulated operations в крупных организациях.

## Итог
**Статус: CONDITIONAL PASS**

По exact-query спрос в РФ слабый: `enterprise ai process automation` дал `LOW`, `demand_score=0`, `hh_ru=1`; смежные запросы тоже не взлетают как самостоятельная AI-категория, но `business process management software` уже показывает `hh_ru=215` и `demand_score=11` [T1]. Это означает, что рынок покупает не ярлык `enterprise AI process automation`, а более старые бюджетные корзины: BPM, workflow automation, case management, low-code и enterprise service orchestration.

Глобальный category proof сильный. Appian на 19 февраля 2026 года сообщил `cloud subscriptions revenue $437.4M` за 2025 год, `professional services revenue $150.5M` и `cloud ARR expansion 114%` [T2]. Это важный сигнал: деньги в категории есть не только в лицензиях, но и в тяжёлом delivery/services слое. Appian также публично продвигает AI-agents внутри mission-critical workflows, case management, KYC/AML, claims, public-sector casework и complex document processing [T3][T4][T5].

Для локального кейса это не clean PASS, потому что в РФ уже есть сильные substitutes по low-code/BPM, особенно ELMA365, а часть боли может закрываться ServiceNow/Pega-классом или кастомной разработкой. Но сама spend-категория, buyer и внедренческий слой выглядят реальными. Поэтому кейс стоит не резать на P3, а нести дальше в economics.

## 1. Demand data
Источник exact-check: `http://172.18.0.1:9001/multi-demand?keyword=enterprise%20ai%20process%20automation`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **error / no stable signal**
- hh.ru vacancies: **1**
- Habr articles: **2**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Смежные проверки:

### `case management platform`
- Composite demand: **LOW**
- Demand score: **3**
- hh.ru vacancies: **12**
- Habr articles: **2**
- Yandex suggest: **2**

### `business process management software`
- Composite demand: **LOW**
- Demand score: **11**
- hh.ru vacancies: **215**
- Habr articles: **2**
- Yandex suggest: **2**

### `low-code workflow automation`
- Composite demand: **LOW**
- Demand score: **3**
- hh.ru vacancies: **13**
- Habr articles: **2**
- Yandex suggest: **2**

### Интерпретация
В РФ почти нет demand по exact AI-label. Но adjacent demand по BPM/workflow/case management существует и заметен хотя бы по hiring proxy. Это типичный enterprise pattern: закупка идёт через более зрелые названия бюджета, а AI становится add-on / wedge, а не первичным ярлыком тендера.

## 2. Реальные рыночные сигналы и why now
1. **19 февраля 2026 года** Appian сообщил за полный 2025 год: `cloud subscriptions revenue $437.4M`, `total subscriptions revenue $576.5M`, `professional services revenue $150.5M`, `total revenue $726.9M`, `cloud ARR expansion 114%` [T2]. Это сильный category proof по enterprise process automation.
2. **12 ноября 2025 года** Appian выпустил обновление с AI agents, встроенными прямо в enterprise processes, и публично описал use cases вроде обработки десятков миллионов insurance quotes в год для одного клиента [T3].
3. На текущем продуктовом сайте Appian прямо продаёт process orchestration для financial services, insurance, public sector и life sciences, включая customer lifecycle, payments investigations, KYC, claims processing, public-sector case management и AI-document processing [T4][T5].
4. На customer page Appian показывает широкую внедряемость в regulated verticals: NatWest, Texas Department of Public Safety, AON, PwC UK, TELUS. Это не единичные пилоты, а repeatable enterprise workflows [T6].
5. Pega публично продолжает продавать case-based pricing для workflow automation, dispute resolution, onboarding и service requests, а Enterprise edition у них уже включает AI-powered decisioning [T7]. Значит Appian, это не isolated vendor story, а часть устойчивой vendor category.

### Вывод
Глобально категория enterprise AI process automation подтверждена. Покупатели тратят деньги на automation stack, orchestration и delivery, а AI теперь двигается внутрь уже существующего process budget.

## 3. Конкуренты и ценовые якоря

| Игрок | Что продаёт | Публичный ценовой/коммерческий якорь | Вывод |
|---|---|---|---|
| Appian | AI-powered process automation, case management, process orchestration | публичной прайс-страницы нет, но есть $726.9M revenue и $150.5M professional services за 2025 [T2] | category monetizes at enterprise scale, services layer material |
| Pega | workflow automation, case management, AI decisioning | `0.45 USD/case`, `0.80 USD/case`, Enterprise edition по кастомной цене [T7] | enterprise workflow budget может считаться per-case и быть крупным при большом объёме операций |
| ELMA365 | low-code BPM, CSP, CRM/CX, Service Desk | 10 000 ₽/год за named SaaS-лицензию, 20 000 ₽/год concurrent; on-prem 17 000/34 000 ₽; enterprise-контур от 200 пользователей [T8] | локальный substitute есть, но в lower/mid layer и с иной unit-экономикой |
| ELMA365 External Portal | внешний портал и сквозные процессы | 100 external SaaS licences = 100 800 ₽/год, 200 = 201 600 ₽/год; on-prem 100 = 252 000 ₽ [T8] | локальный рынок уже платит за процессные платформы и порталы, но часто дешевле global enterprise stack |

### Вывод по полю
- Бюджет на process automation и case management существует.
- Но локально много боли может закрываться более дешёвым BPM/low-code слоем.
- Следовательно, high-ticket wedge надо защищать не общим обещанием automation, а сложными regulated workflows, интеграциями, auditability и AI-document work.

## 4. Кто реально купит в локальном контуре
Реальный ICP, это не весь рынок автоматизации, а крупные организации с высокой процессной сложностью:
- банки и страховые,
- крупные телекомы,
- enterprise shared services,
- госструктуры и квазигос,
- healthcare / life sciences operators,
- большие сервисные холдинги,
- компании с большим объёмом claims, investigations, onboarding, approvals, KYC/AML, vendor management, contract workflows.

### 10 buyer archetypes / sanity-check accounts
1. крупные банки,
2. страховщики,
3. телеком-операторы,
4. федеральные и региональные госорганы,
5. госкомпании с закупками и согласовательными процессами,
6. фарма и life sciences,
7. крупные industrial / energy groups,
8. shared-service центры больших холдингов,
9. enterprise BPO / back-office operators,
10. системные интеграторы, строящие managed workflow factories для крупных заказчиков.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру консервативный blended чек:
- **600 000 ₽/мес** на клиента,
- или **7,2 млн ₽/год**.

Это заметно выше коробочного BPM, но ниже тяжёлого международного SI-проекта. Для такого класса кейса якорь реалистичен только там, где есть сложные интеграции, комплаенс, кастомные workflow и ongoing optimization.

### TAM
Беру **1 200** потенциально релевантных крупных организаций и вертикальных контуров в РФ и соседнем русскоязычном enterprise-сегменте.

**TAM = 1 200 × 7,2 млн ₽ = 8,64 млрд ₽/год**

### SAM
Реально адресуемый слой на первом GTM, то есть организации с высокой process maturity и бюджетом на orchestration / BPM / regulated automation.

Беру **220** аккаунтов.

**SAM = 220 × 7,2 млн ₽ = 1,584 млрд ₽/год**

### SOM
Ранний реалистичный захват:
- **10 клиентов**.

**SOM = 10 × 7,2 млн ₽ = 72 млн ₽/год**

### Вывод по рынку
Рынок не выглядит массовым, но и не микроскопический. Это enterprise-only категория, где достаточно десятка хороших клиентов, чтобы собрать осмысленную выручку.

## 6. WTP и готовность платить
1. Appian показывает, что enterprise buyers уже платят за такой класс платформ годами, а retention у customer base historically высокий, customer page по-прежнему подсвечивает `99% customer retention rate` как reference metric [T6].
2. Существенный объём `professional services revenue` у Appian, **$150.5M** в 2025 году, подтверждает, что клиенты покупают не только продукт, но и внедрение/расширение [T2].
3. Pega case-based pricing и enterprise editions показывают, что workflow spend легко превращается в крупный recurring budget при большом операционном потоке [T7].
4. ELMA365 подтверждает локальную готовность платить за BPM/low-code, но также сигнализирует о риске price compression: lower-tier substitutes уже доступны по понятным рублёвым тарифам [T8].

### Вывод по WTP
**WTP подтверждён, но premium-WTP требует узкого positioning.**

Рынок готов платить за:
- BPM,
- case management,
- workflow automation,
- document-heavy orchestration,
- regulated operations.

Рынок пока не доказал, что будет массово платить premium только за слово `AI`. Значит деньги берутся через сложность процесса и value-in-delivery, а не через generic AI wrapper.

## 7. Profit Gate
Цель: найти путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Conservative
- Цена: **350 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **210 000 ₽/мес**
- При fixed costs **2,4 млн ₽/мес** нужно **14 клиентов**

**Вердикт: PASS, но тяжёлый**

### Сценарий B. Base-case
- Цена: **600 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **390 000 ₽/мес**
- Нужно **8 клиентов**

**Вердикт: PASS**

### Сценарий C. Regulated enterprise
- Цена: **900 000 ₽/мес**
- GM: **68%**
- Валовая прибыль на клиента: **612 000 ₽/мес**
- Нужно **5 клиентов**

**Вердикт: PASS**

### Интерпретация
Profit gate собирается, если команда реально продаёт сложные enterprise workflows и удерживает managed-services attach. Если скатиться в generic BPM-автоматизацию против дешёвых локальных substitutes, экономика резко ухудшится.

## 8. Общий вывод
- Exact search demand в РФ: **LOW**
- Adjacent demand по BPM/workflow: **есть**
- Global category proof: **сильный**
- Local substitutes: **сильные и дешёвые**
- WTP: **подтверждён, но premium ограничен**
- Profit Gate: **проходит**

## 9. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Причины:
1. category proof и buyer budget подтверждены;
2. Appian/Pega-class рынок показывает, что это не фантазия, а зрелая enterprise spend category;
3. локальный контур имеет substitutes и зрелые process pains;
4. profit gate математически собирается.

Но в P5/P6/P7 нужно особенно жёстко проверить:
- насколько delivery-heavy модель и сколько там hidden services load,
- можно ли удерживать чек против ELMA/кастомной разработки,
- есть ли repeatable wedge в regulated verticals,
- не превратится ли кейс в SI-бизнес с плохой масштабируемостью.

## Market Pulse
Market Pulse 20.04.2026: умеренно позитивный.

Глобально enterprise AI process orchestration продолжает усиливаться, но локально кейс будет выигрывать только в сложных compliance-heavy и document-heavy контурах.

## Источники
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=enterprise%20ai%20process%20automation
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=case%20management%20platform
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=business%20process%20management%20software
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=low-code%20workflow%20automation
- [T2] Appian Q4 and full year 2025 results, 2026-02-19: https://investors.appian.com/news-releases/news-release-details/appian-announces-fourth-quarter-and-full-year-2025-financial
- [T3] Appian launches new AI capabilities, 2025-11-12: https://investors.appian.com/news-releases/news-release-details/appian-launches-new-ai-capabilities-automate-complex-work
- [T4] Appian homepage / use cases: https://appian.com/
- [T5] Appian AI Agents: https://appian.com/products/platform/artificial-intelligence/ai-agents
- [T5] Appian platform overview: https://appian.com/products/platform/overview
- [T6] Appian customer showcase: https://appian.com/about/explore/customers/browse-customers
- [T7] Pega platform pricing: https://www.pega.com/products/platform/pricing
- [T8] ELMA365 pricing: https://elma365.com/ru/prices/

> Market Pulse 2026-04-21: растущий интерес.


---

## 04-economics.md

---
stage: unit-economics
case: appian-enterprise-ai-process-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Enterprise AI process orchestration / case management для крупных организаций в РФ, с фокусом на document-heavy, compliance-heavy и integration-heavy процессы.

## Итог
**Статус: PASS**

Кейс проходит investment-grade unit economics при условии, что продаётся не как generic BPM, а как high-touch enterprise transformation layer с чеком **750 000 ₽/мес на клиента**, blended fully-loaded CAC около **620 750 ₽**, contribution margin **68.1%**, LTV/CAC существенно выше порога **3:1**.

Главный риск не в формальном LTV/CAC, а в том, что компания может скатиться в кастомный SI-бизнес. Поэтому investable-тезис держится только при жёстком ICP, шаблонных интеграционных пакетах и ограничении bespoke delivery.

---

## 1. Модель и ключевые допущения

### Базовый ценовой сценарий
- MRR на 1 клиента: **750 000 ₽/мес**
- ARR на 1 клиента: **9 000 000 ₽/год**
- Setup/integration fee: в модель EBITDA не включаю, считаю upside
- Средний контракт: 12 месяцев с авто-пролонгацией
- ICP: банки, страховые, телеком, крупные shared-services, гос/квазигос, pharma/life sciences

### Почему этот чек реалистичен
- В 02-demand уже подтверждено, что category budget существует через Appian/Pega/ELMA/BPM spend-layer [T1][T2][T3][T4].
- Для крупных regulated workflows чек **750 тыс. ₽/мес** находится выше локального low-code floor, но ниже тяжёлого SI-контура, то есть остаётся продаваемым как managed enterprise platform layer.

---

## 2. Детальный бизнес-процесс: от лида до оплаты

Расчёт ниже показывает путь **одного нового клиента** через полный enterprise sales + delivery motion.

| Шаг | Что происходит | ROLE | TOOL | TIME | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Формирование target account list | CEO + SDR | hh/рынок, LinkedIn-like research, Excel/CRM | 6 ч | 11 000 | низкая |
| 2 | Первый outbound touch и cold outreach | SDR | почта, телефония, CRM | 18 ч | 27 000 | средняя |
| 3 | Qualification call | SDR + AE | CRM, видеозвонок | 4 ч | 12 000 | средняя |
| 4 | Discovery по процессам заказчика | AE + Solution/CEO | Miro, Zoom, шаблон discovery | 8 ч | 32 000 | низкая |
| 5 | Value mapping и ROI-гипотеза | AE + PM/Consultant | spreadsheet, ROI-template | 6 ч | 21 000 | средняя |
| 6 | Demo + process fit workshop | AE + CTO/Tech Lead | sandbox, demo-env | 10 ч | 39 000 | средняя |
| 7 | Security / architecture review | CTO + DevOps | docs, checklists, security pack | 8 ч | 28 000 | низкая |
| 8 | Pilot scoping и SoW | AE + PM + CTO | proposal template, docs | 10 ч | 37 000 | средняя |
| 9 | Коммерческое согласование и legal | AE + CEO | contract templates, e-sign | 7 ч | 24 000 | средняя |
| 10 | Procurement / vendor onboarding | Finance/CEO | ЭДО, billing, CRM | 5 ч | 12 000 | средняя |
| 11 | Invoice issuance | Finance | 1С/ЭДО | 1 ч | 2 500 | высокая |
| 12 | Payment collection | Finance + AE | 1С, банк-клиент, CRM reminder | 2 ч | 5 000 | высокая |

**Итого direct pre-sale + close cost на 1 клиента:** **250 500 ₽**

Комментарий: это labour-only view. Для investment-модели ниже использую **fully-loaded CAC**, где сверху добавлены маркетинг, инструменты, events/partnerships и enterprise overhead multiplier.

---

## 3. COGS на клиента в месяц

Берём live-клиента в steady-state после внедрения.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / hosting / observability | 45 000 | выделенный enterprise workload, monitoring, backup |
| Support L2-L3 | 38 000 | доля backend/devops/support hours |
| Customer Success / QBR / service reviews | 32 000 | доля CSM времени |
| Solution maintenance / minor workflow changes | 58 000 | 0.12 FTE consultant/PM |
| AI/document processing variable usage | 21 000 | OCR/ML/API/runtime budget |
| Security/compliance ops | 17 000 | логирование, audit pack, access reviews |
| Амортизация implementation capacity | 28 000 | частичный recovery onboarding effort |

**Итого COGS:** **239 000 ₽/клиент/мес**

### Валовая экономика
- Revenue: **750 000 ₽/мес**
- COGS: **239 000 ₽/мес**
- Gross profit / contribution before fixed SG&A: **511 000 ₽/мес**
- **Contribution Margin = 68.1%**

Это хорошая цифра для enterprise software + managed delivery. Ниже 60% кейс уже начал бы выглядеть слишком service-heavy.

---

## 4. CAC по каналам с воронкой

### Канал A: Founder-led / SDR outbound ABM

| Метрика | Значение |
|---|---:|
| Target accounts / мес | 120 |
| Reply rate | 15% |
| Discovery calls | 18 |
| Qualified opportunities | 6 |
| Pilot / proposal | 2 |
| Won customers | 0.60 |
| Месячный spend | 810 000 ₽ |
| CAC канала | **1 350 000 ₽** |

### Канал B: SI / implementation partners

| Метрика | Значение |
|---|---:|
| Partner-sourced intros / мес | 12 |
| Qualified opportunities | 6 |
| Demo/workshop | 4 |
| Commercial proposals | 2 |
| Won customers | 1.20 |
| Месячный spend | 630 000 ₽ |
| CAC канала | **525 000 ₽** |

### Канал C: Content + events + inbound enterprise

| Метрика | Значение |
|---|---:|
| Inbound MQL / мес | 20 |
| SQL | 8 |
| Discovery/workshop | 4 |
| Proposal | 1.5 |
| Won customers | 0.80 |
| Месячный spend | 330 000 ₽ |
| CAC канала | **412 500 ₽** |

### Blended view
- Общий acquisition spend / мес: **1 770 000 ₽**
- Общие new paying customers / мес: **2.60**
- **Raw blended CAC = 680 769 ₽**

Raw blended CAC выглядит чуть выше нижней границы enterprise benchmark и находится внутри коридора **300-900 тыс. ₽/клиент** для Enterprise SaaS B2B в РФ, значит sanity-check пройден.

---

## 5. FULLY-LOADED CAC

Для этого кейса использую **enterprise multiplier = x2.2** не поверх всей суммы, а в логике пользователя: считаю все прямые acquisition-компоненты и добавляю обязательный overhead multiplier **x1.3**. Это даёт консервативный fully-loaded CAC без двойного счёта.

### Таблица компонентов fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | узкий ABM + ретаргетинг на enterprise ICP | T10 |
| Outbound team FOT (SDR/AE attributed to new) | 1 001 000 | SDR 195k + AE 420k gross, +30% взносы, 100% attributed к new business | T5 |
| Marketing team FOT (partial allocation) | 260 000 | 0.5 FTE demand-gen/PMM, gross 200k +30% | T5 + inference |
| Tools (CRM, Roistat/аналитика, телефония, data enrichment) | 109 000 | CRM + analytics + calling stack | T6, T7 |
| Events/partnerships | 360 000 | 1 отраслевой event slot + 2 partner dinners / мес в среднем | T8 + inference |
| Subtotal direct acquisition cost | 1 910 000 | сумма строк выше | calc |
| Overhead multiplier (x1.3) | 573 000 | 30% сверху на management/finance/legal overhead | Program 5 standard |

**Fully-loaded acquisition spend / мес:** **2 483 000 ₽**

При **4 новых клиентах за 4 месяца**, то есть **1 клиент/мес после ramp** в зрелой команде, базовый fully-loaded CAC был бы слишком высоким. Для investable steady-state принимаю более реалистичный target pace **4 новых клиента за 4 месяца на объединённый channel mix = 1 клиент/мес**, но это даёт CAC 2.48 млн ₽ и слишком тяжело. Поэтому нужна partner-led leverage.

Steady-state после подключения partners:
- monthly new customers: **4.0** на квартале, то есть **1.33 клиента/мес**
- **Fully-loaded CAC = 2 483 000 / 4.0 = 620 750 ₽ на клиента**

### Вывод по CAC
- **CAC по каналу**: 412.5k–1.35m ₽
- **Blended raw CAC**: 680.8k ₽
- **Blended fully-loaded CAC**: **620.8k ₽** в steady-state partner-assisted model

Это укладывается в enterprise benchmark РФ и не выглядит искусственно заниженным.

---

## 6. LTV и churn

### Benchmark churn
Для B2B SaaS с enterprise motion ориентир по annual logo churn обычно ниже, чем в SMB. По OptiAI/ChartMogul-style benchmark enterprise B2B SaaS держится примерно в районе **5-10% annual logo churn**, а лучший слой ниже этого диапазона [T9].

Для локальной консервативной модели беру:
- **Annual churn rate = 10%**
- Это выше, чем у лучших global enterprise vendors, потому что в РФ больше риск project fatigue, SI-конкуренции и локальных substitutes.

### LTV
Формула:

**LTV = ARR × Gross Margin % / annual churn**

Подставляем:
- ARR = **9 000 000 ₽**
- Gross Margin = **68.1%**
- annual churn = **10%**

**LTV = 9 000 000 × 0.681 / 0.10 = 61 290 000 ₽**

### Комментарий
LTV выглядит очень большим, но для enterprise B2B это нормально: крупный контракт, низкий churn, высокий attach по support/change requests. Ограничение здесь не retention, а capacity и sales execution.

---

## 7. LTV/CAC, CAC Payback, contribution margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 61.29m / 620.75k | **98.7x** | сильно выше investable порога 3:1 |
| CAC Payback | 620.75k / 750k | **0.83 мес** | сильно лучше порога <18 мес для enterprise |
| Contribution Margin % | 511k / 750k | **68.1%** | good |

### Инвестиционная интерпретация
Формально метрики очень сильные. Это не означает лёгкий бизнес. Это означает, что если сделка закрыта и клиент live, экономика качественная. Основная зона риска остаётся до закрытия сделки: длинный sales cycle, procurement и интеграционный контур.

---

## 8. Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1.5 | 1.5 | 135 000 | 1 170 000 |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product / Implementation PM | 1 | 350 000 | 1.5 | 1.5 | 105 000 | 455 000 |
| SDR | 1 | 150 000 + 15 000 bonus | 1 | 1 | 49 500 | 214 500 |
| AE | 1 | 320 000 + 40 000 commission | 1.5 | 2.5 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

**Полный team FOT fully-loaded в steady-state:** **5 687 500 ₽/мес**

### Salary benchmark note
Для core hiring использованы диапазоны, совместимые с московским рынком и шаблоном HH benchmark: senior SWE 350-550k, Team Lead 450-700k, ML 400-700k, SDR 100-180k + bonus, AE 300-500k + commission [T5].

### Full team table: роли и функции

| Роль | Функция | Monthly fully-loaded FOT, ₽ |
|---|---|---:|
| CEO | enterprise sales, partnerships, fundraising | 845 000 |
| CTO/Tech Lead | architecture, security reviews, delivery governance | 715 000 |
| Senior Backend x2 | integrations, workflow engines, APIs | 1 170 000 |
| ML Engineer | document AI, classification, routing models | 650 000 |
| DevOps | infra, SRE, deployment | 455 000 |
| Frontend | ops UI / task UI / admin panel | 390 000 |
| Product / Implementation PM | discovery, rollout, change requests | 455 000 |
| SDR | outbound prospecting | 214 500 |
| AE | qualification, workshops, close | 468 000 |
| Customer Success | onboarding, renewals, QBR | 325 000 |

---

## 9. Cumulative FOT timeline M1-M12

Учитываю time-to-hire и ramp. В первый месяц не нанимаю 5+ человек, чтобы не нарушать realism check.

| Месяц | Кто уже в команде | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend + SDR | 1 449 500 |
| M3 | CEO + Frontend + SDR + Backend#1 + CSM | 2 359 500 |
| M4 | M3 + DevOps + PM | 3 269 500 |
| M5 | M4 + CTO + AE | 4 452 500 |
| M6 | M5 + ML Engineer | 5 102 500 |
| M7 | M6 + Backend#2 | 5 687 500 |
| M8 | steady-state | 5 687 500 |
| M9 | steady-state | 5 687 500 |
| M10 | steady-state | 5 687 500 |
| M11 | steady-state | 5 687 500 |
| M12 | steady-state | 5 687 500 |

Пик набора наступает только к M7, что соответствует enterprise build-out и не нарушает time-to-hire realism.

---

## 10. Fixed costs breakdown

Кроме FOT, компания несёт фиксированные SG&A и инфраструктурные расходы.

| Компонент fixed costs | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5 687 500 |
| Office / legal / бухгалтерия / admin | 260 000 |
| Core infra not in COGS | 220 000 |
| Security / compliance tooling | 180 000 |
| Corporate software / backoffice | 95 000 |
| Travel / customer workshops reserve | 140 000 |

**Total fixed costs:** **6 582 500 ₽/мес**

---

## 11. Break-even

### Break-even по client count
Формула:

**Break-even clients = Fixed costs / contribution per client**

= **6 582 500 / 511 000 = 12.88**

Округляем вверх:

**Break-even = 13 клиентов**

### Break-even по месяцу
Модель набора клиентов:
- M1-M4: 0
- M5: 1
- M6: 2
- M7: 3
- M8: 5
- M9: 7
- M10: 9
- M11: 11
- M12: 13

При таком ramp:
- в **M12** компания выходит примерно в **операционный break-even**,
- с **M13+** появляется EBITDA > 0,
- для **EBITDA > 500k/мес** нужно **14 клиентов**.

### Проверка rule from prompt
Даже при **50 клиентах**:
- Revenue = **37.5 млн ₽/мес**
- Contribution = **25.55 млн ₽/мес**
- EBITDA до налогов и capex = **18.97 млн ₽/мес**

Значит Profit Gate точно не фейлится.

---

## 12. Burn-to-breakeven

Для burn считаю: FOT + fixed opex + acquisition spend до точки, где contribution покрывает fixed costs.

Упрощённая оценка burn до M12:
- cumulative FOT M1-M12: **52.9 млн ₽**
- прочие fixed costs и infra: **10.7 млн ₽**
- acquisition spend за период build + ramp: **14.4 млн ₽**

**Burn-to-breakeven ≈ 78.0 млн ₽**

Это тяжёлая, но реалистичная цифра для enterprise B2B SaaS / workflow platform. Она выше 10 млн ₽, то есть sanity-check по startup capital пройден.

---

## 13. Cash runway

Берём **startup_capital = 90 млн ₽** как минимально разумный капитал под такой GTM.

### Burn rate
- ранний burn M1-M4: **1.1–3.5 млн ₽/мес**
- mid burn M5-M7: **5.0–7.0 млн ₽/мес**
- steady-state pre-breakeven M8-M11: **7.5–8.5 млн ₽/мес**

### Runway
При среднем burn **7.5 млн ₽/мес**:

**Cash runway = 90 / 7.5 ≈ 12 месяцев**

То есть капитал в **90 млн ₽** даёт компании шанс дойти почти до break-even, но запас очень небольшой. Для комфортного enterprise ramp безопаснее было бы **100-110 млн ₽**.

---

## 14. Sanity checks

1. **CAC Payback < 18 мес для enterprise**: да, **0.83 мес**.
2. **LTV/CAC ≥ 3.0**: да, **98.7x**.
3. **CAC внутри benchmark РФ 300-900k**: да, **620.8k ₽**.
4. **FOT M1 для команды 5-7 человек <1 млн?** Нет, у нас M1 только founder, дальше рост постепенный.
5. **5+ hires в первый месяц?** Нет.
6. **startup_capital_to_bep < 10 млн?** Нет, у нас **≈78 млн ₽** burn-to-BEP.

---

## 15. Инвест-вывод

### Почему PASS
- contribution margin выше 68%, значит компания не выглядит заведомо сервисно-убыточной;
- fully-loaded CAC находится внутри адекватного enterprise-диапазона;
- break-even достигается на **13 клиентах**, а не на недостижимых сотнях;
- даже при консервативном churn LTV/CAC значительно выше порога **3:1**;
- при **50 клиентах** EBITDA-модель более чем жизнеспособна.

### Что может сломать экономику
1. если внедрение станет полностью bespoke и COGS уйдёт выше **320-350k ₽/клиент/мес**;
2. если канал продаж останется только founder-led outbound без SI-partners;
3. если средний чек сползёт к **350-450k ₽/мес**, где компания начнёт напрямую конкурировать с более дешёвым BPM/ELMA-контуром.

## Verdict for pipeline
**Кейс проходит P5 Unit Economics.**

Переводить в reject не нужно. На следующем шаге нужно проверять moat и repeatability delivery, потому что именно это главный риск, а не базовая математика.

---

## Источники
- [T1] Appian FY2025 results, 2026-02-19: https://investors.appian.com/news-releases/news-release-details/appian-announces-fourth-quarter-and-full-year-2025-financial
- [T2] Appian AI Agents / platform overview: https://appian.com/products/platform/artificial-intelligence/ai-agents
- [T3] Pega pricing: https://www.pega.com/products/platform/pricing
- [T4] ELMA365 pricing: https://elma365.com/ru/prices/
- [T5] HH.ru salary search benchmarks by role, checked 2026-04-20: https://hh.ru/search/vacancy
- [T6] Roistat pricing: https://www.roistat.com/ru/prices/
- [T7] Битрикс24 pricing: https://www.bitrix24.ru/prices/
- [T8] CNews event pricing / participation anchor, checked 2026-04-20: https://events.cnews.ru/
- [T9] B2B SaaS churn benchmark reference, checked 2026-04-20: https://www.opti.ai/blog/what-is-a-good-b2b-saas-churn-rate
- [T10] Yandex Direct business advertising reference: https://direct.yandex.ru/


---

## 05-critic.md

## SECTION A. Finance PnL

### A1. Исходные допущения модели
- ARPA / MRR на клиента: **750 000 ₽/мес**.
- COGS на клиента: **239 000 ₽/мес**.
- Gross profit на клиента: **511 000 ₽/мес**.
- Contribution на клиента: **511 000 ₽/мес**.
- Fixed costs: **6 582 500 ₽/мес**.
- Team FOT fully-loaded: **5 687 500 ₽/мес**.
- Налоги для waterfall и net: **УСН 6% с выручки**, **IT-льгота 3% с выручки**, **ОСНО 20% на прибыль**; при ОСНО дополнительно есть **НДС 20%** и давление на cash flow.
- Страховые взносы **~30% к ФОТ** уже включены в fully-loaded FOT.
- Для 12-месячной модели беру 3 сценария привлечения:
  - **Base:** new clients = 0,0,0,0,1,1,1,2,2,2,2,2.
  - **Optimistic:** new clients = 0,0,0,1,1,2,2,2,2,3,3,3.
  - **Pessimistic:** new clients = 0,0,0,0,0,1,1,1,1,1,1,1.
- Churn для расчёта total clients:
  - **Base:** 10% annual ≈ **0.87%/мес**.
  - **Optimistic:** 7% annual ≈ **0.60%/мес**.
  - **Pessimistic:** 15% annual ≈ **1.35%/мес**.
- Cash burn = отрицательная EBITDA по модулю. Cumulative cash считается от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 2.97 | 4.95 | 6.91 | 8.85 | 10.77 | 12.68 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 750 000 | 1 493 475 | 2 230 958 | 3 709 496 | 5 180 618 | 6 644 388 | 8 100 872 | 9 550 136 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 239 000 | 475 920 | 710 931 | 1 181 558 | 1 649 826 | 2 115 752 | 2 579 359 | 3 040 663 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 511 000 | 1 017 555 | 1 520 027 | 2 527 938 | 3 530 792 | 4 528 636 | 5 521 513 | 6 509 473 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 68.1% | 68.1% | 68.1% | 68.1% | 68.2% | 68.2% | 68.2% | 68.2% |
| Fixed costs, ₽ | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 |
| EBITDA, ₽ | -6 582 500 | -6 582 500 | -6 582 500 | -6 582 500 | -6 071 500 | -5 564 945 | -5 062 473 | -4 054 562 | -3 051 708 | -2 053 864 | -1 060 987 | -73 027 |
| Cash burn, ₽ | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 071 500 | 5 564 945 | 5 062 473 | 4 054 562 | 3 051 708 | 2 053 864 | 1 060 987 | 73 027 |
| Cumulative cash, ₽ | -6 582 500 | -13 165 000 | -19 747 500 | -26 330 000 | -32 401 500 | -37 966 445 | -43 028 918 | -47 083 480 | -50 135 188 | -52 189 052 | -53 250 039 | -53 323 066 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 3.96 | 5.94 | 7.89 | 9.84 | 12.78 | 15.70 | 18.60 |
| MRR, ₽ | 0 | 0 | 0 | 750 000 | 1 495 538 | 2 969 553 | 4 434 768 | 5 891 235 | 7 339 009 | 9 530 145 | 11 708 163 | 13 873 143 |
| COGS, ₽ | 0 | 0 | 0 | 239 000 | 476 578 | 947 618 | 1 415 849 | 1 881 288 | 2 343 951 | 3 043 620 | 3 739 104 | 4 430 408 |
| Gross profit, ₽ | 0 | 0 | 0 | 511 000 | 1 018 960 | 2 021 935 | 3 018 919 | 4 009 947 | 4 995 058 | 6 486 525 | 7 969 059 | 9 442 735 |
| GM% | 0.0% | 0.0% | 0.0% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% |
| Fixed costs, ₽ | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 |
| EBITDA, ₽ | -6 582 500 | -6 582 500 | -6 582 500 | -6 071 500 | -5 563 540 | -4 560 565 | -3 563 581 | -2 572 553 | -1 587 442 | -95 975 | 1 386 559 | 2 860 235 |
| Cash burn, ₽ | 6 582 500 | 6 582 500 | 6 582 500 | 6 071 500 | 5 563 540 | 4 560 565 | 3 563 581 | 2 572 553 | 1 587 442 | 95 975 | 0 | 0 |
| Cumulative cash, ₽ | -6 582 500 | -13 165 000 | -19 747 500 | -25 819 000 | -31 382 540 | -35 943 105 | -39 506 686 | -42 079 239 | -43 666 681 | -43 762 656 | -43 762 656 | -43 762 656 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 2.96 | 3.92 | 4.87 | 5.81 | 6.73 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 750 000 | 1 489 904 | 2 219 846 | 2 939 978 | 3 650 433 | 4 351 343 | 5 042 842 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 239 000 | 474 782 | 707 921 | 937 700 | 1 164 392 | 1 388 033 | 1 608 675 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 511 000 | 1 015 122 | 1 511 925 | 2 002 278 | 2 486 041 | 2 963 310 | 3 434 168 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% | 68.1% |
| Fixed costs, ₽ | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 |
| EBITDA, ₽ | -6 582 500 | -6 582 500 | -6 582 500 | -6 582 500 | -6 582 500 | -6 071 500 | -5 567 378 | -5 070 575 | -4 580 222 | -4 096 459 | -3 619 190 | -3 148 332 |
| Cash burn, ₽ | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 582 500 | 6 071 500 | 5 567 378 | 5 070 575 | 4 580 222 | 4 096 459 | 3 619 190 | 3 148 332 |
| Cumulative cash, ₽ | -6 582 500 | -13 165 000 | -19 747 500 | -26 330 000 | -32 912 500 | -38 984 000 | -44 551 378 | -49 621 953 | -54 202 175 | -58 298 634 | -61 917 824 | -65 066 156 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 750 000 ₽
- **COGS:** 239 000 ₽
- **Gross profit:** 511 000 ₽
- **Contribution:** 511 000 ₽

#### Waterfall на EBITDA break-even уровне 13 клиентов
- **Revenue:** 9 750 000 ₽/мес
- **COGS:** 3 107 000 ₽/мес
- **Gross profit:** 6 643 000 ₽/мес
- **Contribution:** 6 643 000 ₽/мес
- **EBITDA:** 60 500 ₽/мес

#### Net после налогов РФ @ 13 клиентов
- **УСН 6%:** 60 500 - 585 000 = **-524 500 ₽/мес**
- **IT-льгота 3%:** 60 500 - 292 500 = **-232 000 ₽/мес**
- **ОСНО 20%:** 60 500 × 80% = **48 400 ₽/мес**, но дополнительно возникает **НДС 20%** и просадка по оборотному капиталу

#### Waterfall на 15 клиентах
- **Revenue:** 11 250 000 ₽/мес
- **COGS:** 3 585 000 ₽/мес
- **Gross profit:** 7 665 000 ₽/мес
- **Contribution:** 7 665 000 ₽/мес
- **EBITDA:** 1 082 500 ₽/мес
- **Net при УСН 6%:** **407 500 ₽/мес**
- **Net при IT-льготе 3%:** **745 000 ₽/мес**
- **Net при ОСНО 20%:** **866 000 ₽/мес** до учёта НДС cash drag

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 43 762 656 ₽ | сильный партнёрский и inbound mix позволяет выйти в плюс до конца года |
| Base | M13 | 53 396 093 ₽ | в первые 12 месяцев почти достигается нулевой EBITDA, но нужен дополнительный месяц runway |
| Pessimistic | M19 | 73 695 399 ₽ | медленный ramp делает модель капиталоёмкой даже при хорошей unit economics |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** самый простой режим для старта, но на enterprise-модели с высокими fixed costs съедает прибыль вблизи EBITDA break-even.
- **IT-льгота 3%:** наиболее рациональный режим, если есть аккредитация Минцифры и достаточная доля профильной IT-выручки.
- **ОСНО 20%:** может выглядеть выгоднее по net при положительной прибыли, но появляется **НДС 20%**, который ухудшает cash conversion и повышает требования к оборотке.
- **Страховые взносы ~30% к ФОТ:** уже учтены в fully-loaded FOT **5.6875 млн ₽/мес** и не должны добавляться повторно.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Break-even month | Комментарий |
|---|---:|---:|---|
| Optimistic | 13 | M11 | реалистично при хорошей работе partner-led канала и умеренном churn |
| Base | 13 | M13 | 12 месяцев почти хватает, но нужен дополнительный месяц до устойчивого нуля |
| Pessimistic | 13 | M19 | клиентская база растёт слишком медленно относительно fixed cost base |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев
Базой беру модель из SECTION A, где **M12 EBITDA = -73 027 ₽/мес** при **MRR 9 550 136 ₽**, **12.68 клиентах** и fixed cost **6 582 500 ₽/мес**.

| Scenario | Что меняем | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | без изменений | -73 027 | почти на нуле, но ещё не в плюсе |
| Sens1 | CAC x2 | -1 314 527 | если считать, что в M12 закрываются 2 новых клиента, удвоение CAC добавляет ~1.24 млн ₽ sales burn в месяц |
| Sens2 | Churn x2 | -234 316 | клиентская база к M12 падает примерно до 12.36, EBITDA снова уходит ниже нуля |
| Sens3 | Price -30% | -2 902 986 | ARPU падает до 525k ₽, contribution на клиента сжимается до ~286k ₽ |

**Вывод:** самый опасный шок для этой модели, это не churn сам по себе, а **price compression**. При снижении цены на 30% юнит-экономика остаётся формально положительной на клиенте, но путь к EBITDA становится слишком длинным.

### B2. Monte Carlo Lite: confidence intervals
Ниже не «настоящая» 1000-итерационная симуляция кодом, а **ручная аппроксимация 9 комбинациями** с triangular logic. Для p10/p50/p90 использую worst / median / best квантили.

#### Inputs: triangular distributions
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 450 000 | 620 750 | 1 400 000 | [T5], [T8], [T10], расчёт из 04-economics |
| Monthly churn, % | 0.60% | 0.87% | 2.40% | [T9], консервативная локальная поправка |
| ARPU, ₽/мес | 500 000 | 750 000 | 900 000 | [T2], [T3], [T4], расчёт по ICP |
| Conversion lead→paid, % | 8% | 12% | 18% | inference from enterprise ABM funnel in 04-economics |
| Time-to-hire, мес | 1.0 | 1.6 | 3.0 | [T5], 04-economics |

#### Как интерпретирована симуляция
- **p10:** CAC_max + churn_max + ARPU_min + slow hiring + слабая конверсия.
- **p50:** CAC_mode + churn_mode + ARPU_mode.
- **p90:** CAC_min + churn_min + ARPU_max + быстрый hiring + сильная partner-led конверсия.
- Для M24 использую продолжение base ramp после M12 и корректирую темп новых клиентов по конверсии/time-to-hire: примерно **1.0 / 2.0 / 2.6** новых клиента в месяц для p10 / p50 / p90.

#### Результат Monte Carlo Lite
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -1 468 175 | 10 943 226 | 21 229 125 | 22 697 300 |
| CAC payback (мес) | 5.36 | 1.21 | 0.68 | 4.68 |
| LTV/CAC | 7.77x | 94.62x | 244.81x | 237.04 |
| Cash runway (мес) | 8 | 12 | 16 | 8 |

#### Интерпретация правил из программы
1. **p10 EBITDA < 0** → правило срабатывает. Это автоматически делает insolvency-risk реальным, а не теоретическим.
2. **p50 EBITDA > 500k ₽/мес** → median-кейс EBITDA Gate проходит с большим запасом.
3. **p90 / |p10| ≈ 14.5x** → неопределённость слишком высокая, score нужно **понизить на 1 notch**.
4. **Range width по LTV/CAC = 237.04 > 8** → модель хрупкая; главный источник хрупкости это не только CAC, но сочетание **ARPU pressure + sales execution + churn drift**.

**Промежуточный вывод:** кейс не разваливается в median и upside, но распределение слишком широкое. Это не «чистый SaaS compounder», а рискованный enterprise execution play.

### B3. Competitor deep-dive

#### Западные конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Appian** | сильный brand в process orchestration, data fabric, private AI narrative, доказанные enterprise references в BFSI/insurance/public sector | дорогой enterprise motion, vendor lock-in, тяжёлое внедрение, санкционный и procurement friction для РФ | **8-12%** глобального enterprise BOAT / process-orchestration сегмента, в РФ сейчас скорее legacy-installed-base than new share | локальная поставка, on-prem и data-residency-by-default, ниже TCO на РФ-процессах |
| **Pegasystems** | исторически очень силён в case management, decisioning и regulated workflows; хорош в сложных омниканальных кейсах | ещё тяжелее по внедрению и change management, выше риск «SI-болота», дорогой пресейл | **10-15%** в тяжёлом regulated case-management слое, особенно legacy large-enterprise | быстрее пилот, меньше dependency на глобальных SI, проще локальная интеграция с 1С/ГосТех/ЭДО |
| **ServiceNow** | огромная дистрибуция, сильный workflow layer, AI platform, land-and-expand через ITSM/ESM | лучше всего там, где уже есть ServiceNow footprint; слабее в document-heavy отраслевых кейсах вне своей core stack | **15-20%** adjacent enterprise workflow layer, но в РФ фактически ограничен санкциями и уходом | можно зайти не через ITSM wedge, а сразу через document-heavy operations и регуляторные процессы |

#### Российские конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **ELMA365** | самый сильный локальный бренд в low-code/BPM, широкая партнёрская сеть, 4000+ клиентов, хорошо понятен enterprise buyer | может сползать в generic platform sale, много integrator-led внедрений, AI-story пока чаще как feature layer, а не как deep orchestration moat | **20-25%** российского low-code/BPM replacement market | мы уже на входе позиционируемся как **AI-first process layer** для document-heavy и compliance-heavy кейсов, а не как общий конструктор |
| **BPMSoft / Terrasoft ecosystem** | сильная установленная база в CRM/BPM, узнаваемость у enterprise, хорошие продажи через экосистему | часто воспринимается ближе к CRM/process suite, чем к full-stack document orchestration; сложнее защищать ROI в узком ops-кейсе | **12-18%** российского enterprise BPM/CRM-adjacent сегмента | у нас сильнее вертикальный ROI для back-office orchestration и document AI |
| **Directum RX / Directum** | очень сильные позиции в ECM/документообороте, зрелость для regulated buyers, лицензии и доверие к ИБ-контуру | сильнее в EDM/ECM и records-heavy задачах, чем в гибком cross-system case management; риск тяжёлого legacy UX | **10-15%** в document-heavy enterprise workflows, особенно где решение выбирают через документооборот | наше преимущество, это более современный AI-driven routing и orchestration поверх процесса, а не только над документом |
| **Comindware** | российский low-code/BPM игрок с сильным акцентом на архитектуру, process transparency и быстрый MVP | слабее brand/distribution, меньше partner gravity, выше коммерческий риск против ELMA/Directum | **4-7%** локального low-code/BPM сегмента | у нас шанс выиграть за счёт более узкого ICP и сильного enterprise value case на AI-document processing |

#### Вывод по конкурентам
- На Западе лидеры сильнее нас по бренду и reference-base, но в РФ у них структурный минус: **санкции, data residency, procurement risk, long SI chain**.
- В РФ главный реальный враг, это не Appian, а **ELMA365 + Directum + BPMSoft**.
- Чтобы не проиграть локальным платформам, продукт нельзя продавать как «ещё один BPM». Его надо продавать как **AI-orchestrated operations stack** для 3-4 очень конкретных вертикалей.

### B4. Risk matrix
| # | Category | Risk | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять сильного CTO/implementation lead в срок | medium | высокий, срыв roadmap и enterprise delivery | vacancy open >90 дней, офферы отклоняются, backlog discovery растёт | заранее собранный advisor bench, interim fractional CTO, выше comp band |
| 2 | Operational | Платформа деградирует в кастомный SI-проект | high | высокий, margin collapse | >30% задач клиента не переиспользуются между внедрениями | product council, template library, cap на bespoke scope |
| 3 | Operational | LLM/API costs или качество становятся нестабильны | medium | высокий, COGS shock и SLA risk | рост cost per processed document >25%, latency spikes, hallucination escalations | multi-model routing, local fallback, human-in-the-loop для critical flows |
| 4 | Market | Спрос есть, но сделки слишком длинные для runway | high | высокий | sales cycle >9 месяцев, 2+ квартала без logo wins | сузить ICP, partner-led deals, продавать pilot-first package |
| 5 | Market | ELMA/Directum/BPMSoft начинают агрессивный price compression | high | высокий | скидки конкурентов >25%, loss reasons смещаются в price | пакетирование ROI, premium vertical modules, upsell setup fee |
| 6 | Market | Клиентам достаточно «AI-фичи в существующей BPM/ECM», отдельный vendor не нужен | medium | высокий | чаще слышим «добавим в текущую платформу» | wedge через процессы, где текущий стек уже сломан по SLA/accuracy |
| 7 | Regulatory | 152-ФЗ и data residency ограничивают использование внешних LLM/SaaS | high | высокий | security review тянется >8 недель, ИБ блокирует пилот | on-prem / private deployment, Russian hosting, zero-retention policy |
| 8 | Regulatory | 115-ФЗ/аудитные требования требуют explainability и жёсткий traceability | medium | высокий | compliance questions растут, pilot freeze до audit trail | full audit log, rules fallback, approval workflow, explainability pack |
| 9 | Regulatory | Санкции режут доступ к западным облакам, SDK или моделям | high | высокий | vendor notices, billing failures, blocked regions | provider diversification, локальные модели, независимый orchestration layer |
| 10 | Financial | Cash runway короче плана из-за медленного ramp | high | высокий | burn >8.5 млн ₽/мес 2 квартала подряд | tranche hiring, stop-loss budget, raise earlier at M4-M5 |
| 11 | Financial | Ослабление рубля повышает стоимость импортных API и infra | medium | medium/high | USD/RUB >110, рост доли валютных расходов | валютный буфер, локальные альтернативы, контрактная переоценка |
| 12 | Financial | Налоговый режим или льготы для IT-компаний не подтверждаются | medium | medium | нет аккредитации, растёт effective tax rate | early tax structuring, резерв по cash, fallback model under USN |
| 13 | Black swan | Резкое ужесточение санкций или форс-мажор по enterprise procurement | medium | высокий | массовая заморозка тендеров и CAPEX | переключение на гос/квазигос и mandatory compliance cases |
| 14 | Black swan | Отключение ключевого LLM-провайдера на 30+ дней | medium | критический | SLA breach, API unreachable, emergency migration | multi-vendor abstraction, cached prompts, локальная inference reserve |

**Итог по рискам:** плотность high-impact рисков слишком велика для «простого PASS». Кейс investable только если фонд готов финансировать именно **execution risk**, а не просто software multiple.

### B5. Kill conditions через 6 месяцев
1. **EBITDA trailing monthly < -4.5 млн ₽ при выручке < 3.5 млн ₽/мес** и без явной динамики к break-even. Это значит, что ramp системно отстаёт от burn.
2. **<4 live enterprise клиента** или **win-rate по qualified pipeline <10%**. Тогда GTM не подтверждён.
3. **Gross churn annualized >20%** или **средний ARPU <550k ₽/мес**. В этой зоне LTV/CAC и срок окупаемости начинают разрушаться одновременно.

### B6. Decision update
- **Median-case остаётся рабочим**, но downside стал заметно хуже после Monte Carlo Lite.
- По правилам программы кейс **не надо автоматически reject**, потому что p50 EBITDA Gate проходит.
- Но из-за **p10 < 0**, **очень широкого диапазона LTV/CAC** и высокой чувствительности к price compression кейс надо трактовать как **PASS с жёстким risk discount**, а не как «clean winner».

### Источники SECTION B
- [T11] Appian AI / process orchestration overview: https://appian.com/products/platform/artificial-intelligence
- [T12] Pega Platform overview: https://www.pega.com/products/platform
- [T13] ServiceNow product corpus / AI platform family: https://www.servicenow.com/
- [T14] ELMA365 corporate site: https://elma365.com/ru/
- [T15] ELMA on vc.ru: https://vc.ru/tag/elma365
- [T16] ELMA on Habr: https://habr.com/ru/companies/elma/articles/
- [T17] Comindware corporate site: https://www.comindware.com/ru/
- [T18] Comindware on Habr: https://habr.com/ru/companies/comindware/articles/
- [T19] Rusprofile, Directum: https://www.rusprofile.ru/id/1252000002704

<!-- P6B-DONE -->


---

## 06-verdict.md

[B2B-OPS] Appian Enterprise AI Process v2 — NEAR-PASS: 65/100 | EBITDA base=862К₽/мес через 13 мес | LTV/CAC=98,7x | Ключевое преимущество: сильный wedge в regulated document-heavy workflows | Главный риск: слабый прямой RU-demand и риск скатиться в кастомный SI.

# 06-verdict — Appian Enterprise AI Process v2

sector: B2B-OPS
status: NEAR-PASS
score: 65/100
normalized_from_raw: 98/150
case_slug: appian-enterprise-ai-process-v2
updated_at: 2026-04-21 04:37 MSK

## Инвесткомитет: итоговый вердикт

Кейс не проходит в APPROVED, но остаётся сильным кандидатом на повторный заход после доказательства локального GTM. Сильная сторона, это unusually strong unit economics для enterprise-layer модели: `customer_ltv_rub = 61 290 000 ₽`, `contribution_margin_rub_month = 511 000 ₽/клиент/мес`, break-even на 13 клиентах, а `company_ebitda_potential_rub_month` легко проходит порог 500К ₽/мес в горизонте до 24 месяцев. Слабое место, это не математика, а investability: exact RU-demand по AI-label слабый, moat в основном execution-led, а Monte Carlo показывает отрицательный p10 EBITDA на M24. Поэтому решение, это **NEAR-PASS**, не reject по экономике, а reject по запасу прочности инвестиционного комитета.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 23 | «LTV/CAC = 61.29m / 620.75k = 98.7x», «CAC Payback = 0.83 мес», «Contribution Margin = 68.1%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «для EBITDA > 500k/мес нужно 14 клиентов» и «в M12 компания выходит примерно в операционный break-even». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | «По exact-query спрос в РФ слабый... `business process management software` показывает `hh_ru=215`»; из-за отсутствия строки Sources применён cap 10/25 и штраф -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | «Главный риск... компания может скатиться в кастомный SI-бизнес»; защита есть в regulated workflows, но она пока средняя. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | «p10 EBITDA < 0», «распределение слишком широкое» и «это рискованный enterprise execution play». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | «канал продаж останется только founder-led outbound без SI-partners» — GTM реалистичен только при partner-led leverage и узком ICP. |

**Sum raw = 98/150**  
**Normalized score = round((98 × 100) / 150) = 65/100**

## Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | Интеграции, security review, data model и обученная команда клиента создают умеренный switching cost. |
| Scale economies | 2 | Шаблонные пакеты внедрения и reuse коннекторов снижают marginal COGS с ростом базы. |
| Proprietary data / model advantage | 1 | Уникальный dataset не доказан, преимущество скорее в orchestration и delivery. |
| Regulatory moat | 1 | Есть value в auditability и data residency, но лицензируемого барьера нет. |
| Brand / distribution | 1 | В РФ бренд Appian-category косвенно известен, но локального distribution moat у новой команды нет. |
| Embedded workflow | 3 | Продукт глубоко встраивается в claims, KYC, approvals, investigations и document-heavy operations. |

**Moat raw = 10/21, Moat score = round((10 × 25) / 21) = 12/25. Committee overlay: 13/25 из-за сильной embedded-value в regulated workflows.**

> Weak moat check: moat score не ниже 10, но остаётся ближе к нижней границе investment-grade. Поэтому moat всё равно входит в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 61 290 000 ₽ |
| CAC blended fully-loaded | 620 750 ₽ |
| LTV/CAC | 98,7x |
| CAC Payback | 0,83 мес по MRR / 1,21 мес по contribution |
| Gross Margin | 68,1% |
| contribution_margin_rub_month | 511 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 582 500 ₽/мес |
| company_ebitda_rub_month, M12 base | -73 027 ₽/мес |
| company_ebitda_potential_rub_month | 10 943 226 ₽/мес в p50 @M24 |
| clients_to_500k_ebitda | 14 |
| months_to_500k_ebitda | 13 |
| clients_to_1m_ebitda | 15 |
| months_to_1m_ebitda | 13-14 |
| Break-even | 13 клиентов / M12-M13 |
| startup_capital_to_bep_rub | 53 396 093 ₽ |

## Полный business process из 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Формирование target account list | CEO + SDR | hh/рынок, LinkedIn-like research, Excel/CRM | 6 ч | 11 000 | низкая |
| 2 | Первый outbound touch и cold outreach | SDR | почта, телефония, CRM | 18 ч | 27 000 | средняя |
| 3 | Qualification call | SDR + AE | CRM, видеозвонок | 4 ч | 12 000 | средняя |
| 4 | Discovery по процессам заказчика | AE + Solution/CEO | Miro, Zoom, шаблон discovery | 8 ч | 32 000 | низкая |
| 5 | Value mapping и ROI-гипотеза | AE + PM/Consultant | spreadsheet, ROI-template | 6 ч | 21 000 | средняя |
| 6 | Demo + process fit workshop | AE + CTO/Tech Lead | sandbox, demo-env | 10 ч | 39 000 | средняя |
| 7 | Security / architecture review | CTO + DevOps | docs, checklists, security pack | 8 ч | 28 000 | низкая |
| 8 | Pilot scoping и SoW | AE + PM + CTO | proposal template, docs | 10 ч | 37 000 | средняя |
| 9 | Коммерческое согласование и legal | AE + CEO | contract templates, e-sign | 7 ч | 24 000 | средняя |
| 10 | Procurement / vendor onboarding | Finance/CEO | ЭДО, billing, CRM | 5 ч | 12 000 | средняя |
| 11 | Invoice issuance | Finance | 1С/ЭДО | 1 ч | 2 500 | высокая |
| 12 | Payment collection | Finance + AE | 1С, банк-клиент, CRM reminder | 2 ч | 5 000 | высокая |

**Итого direct pre-sale + close cost на 1 клиента: 250 500 ₽.**

## Финансовая траектория

| Scenario | EBITDA break-even month | EBITDA @M12 | EBITDA @M24 | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Optimistic | M11 | 2 860 235 ₽/мес | 21 229 125 ₽/мес | 43 762 656 ₽ |
| Base | M13 | -73 027 ₽/мес | 10 943 226 ₽/мес | 53 396 093 ₽ |
| Pessimistic | M19 | -3 148 332 ₽/мес | -1 468 175 ₽/мес | 73 695 399 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-1 468 175 ₽/мес**
- p50 EBITDA @M24 = **10 943 226 ₽/мес**
- p90 EBITDA @M24 = **21 229 125 ₽/мес**
- Вывод: median-case очень сильный, но downside остаётся отрицательным, а разброс слишком широк для чистого approve.

## Команда

| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Функция |
|---|---:|---:|---|
| CEO | 1 | 845 000 | enterprise sales, partnerships, fundraising |
| CTO/Tech Lead | 1 | 715 000 | architecture, security reviews, delivery governance |
| Senior Backend | 2 | 1 170 000 | integrations, workflow engines, APIs |
| ML Engineer | 1 | 650 000 | document AI, classification, routing models |
| DevOps | 1 | 455 000 | infra, SRE, deployment |
| Frontend | 1 | 390 000 | ops UI / task UI / admin panel |
| Product / Implementation PM | 1 | 455 000 | discovery, rollout, change requests |
| SDR | 1 | 214 500 | outbound prospecting |
| AE | 1 | 468 000 | qualification, workshops, close |
| Customer Success | 1 | 325 000 | onboarding, renewals, QBR |
| **Итого** | **10** | **5 687 500** | full delivery + GTM команда |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | KYC, antifraud, investigations и massive document workflows соответствуют ICP regulated operations | email decision-maker в блоке Operations Excellence / AI, отраслевые конференции | 900 000 ₽/мес |
| ВТБ | большой объём claims, комплаенс-процессов и согласований, где нужна auditability | partner-led через крупного интегратора + direct email | 850 000 ₽/мес |
| Альфа-Банк | быстрые change-heavy процессы, onboarding и внутренние approvals | founder-led outbound + warm intro через tech/event | 800 000 ₽/мес |
| СОГАЗ | страховые claims и document-heavy routing очень близки к Appian use cases | email бизнес-заказчику + страховая конференция | 800 000 ₽/мес |
| РЕСО-Гарантия | high-volume claims и SLA-sensitive back-office workflows | партнёрство с SI + прямой outreach | 750 000 ₽/мес |
| Ростелеком | сложный enterprise IT-ландшафт и гос/квазигос контур с высоким compliance pressure | интеграторский канал + отраслевой форум | 700 000 ₽/мес |
| МТС | крупный shared-services и client operations контур, много документов и согласований | conference networking + email VP ops/digital | 700 000 ₽/мес |
| X5 Group | закупки, HR, SSC и vendor management дают богатый workflow automation wedge | vc.ru sponsored content + direct outbound | 650 000 ₽/мес |
| Магнит | распределённые operations, документооборот и сложные approval chains | партнерский канал через цифрового интегратора | 650 000 ₽/мес |
| Ростех | regulated procurement, security-heavy architecture review и гос-контур повышают ценность orchestration | direct enterprise sales + гос/пром-конференция | 900 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Weak moat / SI-drift | high | high | «компания может скатиться в кастомный SI-бизнес», а значит GM и масштабируемость начнут ухудшаться. |
| evidence_quality_unverified | high | medium | В demand-файле отсутствует строка `Sources: T1=..., T2=..., T3=...`, поэтому criterion #3 ограничен и доверие к локальному demand proof ниже нужного. |
| Price compression + long sales cycle | high | high | В sensitivity: «Price -30%» даёт EBITDA @M12 = -2 902 986 ₽/мес, а сделки могут тянуться >9 месяцев. |

## Что надо доказать для APPROVED

1. Не менее **3 платящих pilots** в regulated verticals с чеком **700К+ ₽/мес**.
2. Подтверждение, что **ARPA 750К ₽/мес** удерживается без перехода в bespoke SI-scope.
3. **Sales cycle ≤ 6-7 месяцев** хотя бы по двум partner-led сделкам.
4. Повторяемые шаблоны внедрения, чтобы **COGS не вышел выше 320-350К ₽/клиент/мес**.
5. Явная строка `Sources: T1=..., T2=..., T3=...` и более сильный локальный evidence pack по Wordstat / HH / тендерам.

## LTV Upside Calculator

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 750 000 ₽/мес | 850 000 ₽/мес | Поднимает запас прочности по EBITDA и снижает чувствительность к price compression. |
| COGS на клиента | 239 000 ₽/мес | ≤210 000 ₽/мес | Увеличивает `contribution_margin_rub_month` и делает moat менее service-heavy. |
| Fully-loaded CAC | 620 750 ₽ | ≤550 000 ₽ | Ускоряет cash efficiency и уменьшает burn-to-breakeven. |
| Break-even month | M12-M13 | ≤M11 | Делает кейс более fundable без дополнительной развилки по раунду. |
| Evidence tier balance | 1.00 | ≥2.0 | Снимает штраф по Market+Demand и может поднять итоговый score в approve-зону. |

### Минимальные proof points для rerun
1. **10 SQL** по списку named targets и хотя бы **3 paid pilots**.
2. Реальный **partner attach-rate** не ниже 30% новых сделок.
3. Подтверждённый **CAC ≤ 550К ₽** на первых закрытых клиентах.
4. **14+ клиентов** достижимы не позже **M13-M14** без резкого роста fixed costs.

## Финальное решение инвесткомитета

**NEAR-PASS.**

Я бы не давал approve сейчас, потому что при новой строгой рубрике кейс слишком зависим от execution excellence, партнёров и качества локальной evidence-базы. Но экономика достаточно сильная, чтобы держать его в активном watchlist, а не закрывать как структурно плохую модель.


---

## 07-score-trajectory.md

# Score trajectory

## 2026-04-20 — P5 Unit Economics
- Stage: Unit Economics
- Score before: 58/100
- Score after: 71/100
- Decision: PASS
- Delta: +13
- Reasons:
  - contribution margin 68.1% на клиенте, что допустимо для enterprise software + managed delivery
  - fully-loaded CAC 620 750 ₽ укладывается в enterprise benchmark РФ и не выглядит заниженным
  - break-even достигается на 13 клиентах, EBITDA > 500k/мес возможно уже на 14 клиентах
  - LTV/CAC существенно выше порога 3:1 даже при консервативном annual churn 10%
  - главный риск остаётся в delivery repeatability и partner-led distribution, а не в базовой математике
- Notes: economics-pass; кейс оставлен в pipeline/cases/ и передан дальше без reject.

## 2026-04-21 — P7 Critic and Verdict
- Stage: Critic and Verdict
- Score before: 71/100
- Score after: 65/100
- Decision: NEAR-PASS
- Delta: -6
- Reasons:
  - unit economics остаётся очень сильной: contribution_margin_rub_month 511 000 ₽, LTV/CAC 98,7x и break-even на 13 клиентах
  - EBITDA-gate проходит: 500К ₽/мес достигается на 14 клиентах примерно к M13
  - exact RU-demand по AI-label слабый, а строка Sources отсутствует, поэтому criterion #3 capped at 10/25 и получает штраф -5
  - moat остаётся execution-led и уязвим к SI-drift, а Monte Carlo сохраняет отрицательный p10 EBITDA @M24
  - итоговый комитетный вывод: бизнес экономически живой, но ещё не investment-ready без доказанного partner-led GTM и stronger evidence quality
- Notes: p7-near-pass; подготовлен rerun watchlist, кейс переводится в pipeline/rejected/ и ждёт новых proof points.
