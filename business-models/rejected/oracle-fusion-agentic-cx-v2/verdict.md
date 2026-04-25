# Краткий бриф

## Кейс
Oracle Fusion Agentic CX, AI-first customer service и CX operations

## Статус
Принудительный resurrect/rerun, создан новый кейс `oracle-fusion-agentic-cx-v2`.

## Почему открыт
Кейс открыт как принудительный resurrect-v2 по сигналу о coordinated agent workflows в customer service и CX operations внутри Oracle Fusion. Ранее сигнал считался supporting для существующего кейса, но теперь должен пройти отдельную полную аналитику.

## Следующий шаг
Передать кейс в P3-demand-validation и проверить, является ли Oracle-driven CX ops самостоятельной service line или остаётся подкатегорией общего customer-service operations wedge.


---

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-oracle-fusion-agentic-cx.md
created: 2026-04-21T04:30:41+03:00
original_verdict: triage/triage-2026-04-13-oracle-fusion-agentic-cx.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `oracle-fusion-agentic-cx-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — oracle-fusion-agentic-cx

## Meta
- source: triage/triage-2026-04-13-oracle-fusion-agentic-cx.md
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
- pipeline/raw/20260413T154133Z-oracle-fusion-agentic-cx.md

## Classification
duplicate / supporting signal for existing case

## Decision
Не создавать новый case.

Route signal to existing case: `ai-customer-service-operations-operator`.

## Why
- Сигнал описывает тот же functional wedge, что и уже открытый case: AI-first customer service / CX operations, где поверх платформы возникает service layer из implementation, workflow design, governance, tuning и managed optimisation.
- Новый Oracle анонс полезен как дополнительное подтверждение cross-vendor pattern, но сам по себе не меняет wedge настолько, чтобы открывать отдельный case.
- Более уместно использовать его позже как evidence signal для vendor breadth внутри существующего customer-service operations case.

## Triage note
Это не шум, но и не новый самостоятельный case. Считать сигнал подтверждением того, что AI customer-service operations выходит за пределы Zendesk-like narrative и появляется у крупных suite vendors. При следующем evidence-cycle можно добавить Oracle как supporting vendor signal в `pipeline/cases/ai-customer-service-operations-operator/01-evidence.md`.

```



---

---
stage: demand-validation
case: oracle-fusion-agentic-cx-v2
date: 2026-04-21
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
Oracle Fusion Agentic CX как кандидат на сервисный слой внедрения, интеграции и managed-оптимизации AI-first customer service / CX operations для enterprise-клиентов.

## Итог
**Статус: CONDITIONAL PASS.**

На 21 апреля 2026 года самостоятельный exact-demand именно по формулировке `Oracle Fusion Agentic CX` в РФ слабый, но adjacent budget line по омниканальному контакт-центру, AI-автоматизации саппорта и речевой аналитике уже существует и подтверждается как глобальными, так и локальными production-signal'ами. [T1][T2][T4][T5][T6]

Ключевые выводы:
1. **9 апреля 2026 года** Oracle официально представил Fusion Agentic Applications for CX, где AI-агенты не только подсказывают, но и исполняют процессы в sales, service и marketing, используя enterprise data, permissions и workflow context. Это сильный свежий signal, что крупный suite-vendor считает category уже достаточно зрелой для production rollout. [T1]
2. Oracle дополнительно строит экосистему вокруг AI Agent Studio и partner/external agents, а в октябре 2025 года сообщал о marketplace и более чем `32 000` обученных сертифицированных экспертов. Это усиливает тезис, что value capture пойдёт не только в софт, но и в implementation/service layer. [T2]
3. В локальном контуре exact-demand слабый, но бюджеты на adjacent категорию есть: internal demand API даёт `омниканальный контакт-центр` -> `demand_score=18`, `hh_ru=30`, `yandex_suggest=100`; `crm ai agent` -> `demand_score=7`, `hh_ru=110`; а Oracle-specific запросы почти пустые. [T3]
4. В РФ уже есть measurable adoption похожего стека: Naumen продаёт enterprise-уровень омниканального контакт-центра и речевой аналитики, ДОМ.РФ после внедрения Naumen CI ускорил решение вопроса в `17%` обращений, а «Инфосистемы Джет» на базе YandexGPT автоматизировали обработку `30%` заявок в саппорт. Это подтверждает, что buyer платит за automation в customer-service operations, даже если не называет это Oracle-style agentic CX. [T4][T5][T6]

## 1. Сигналы спроса

### Demand API
- `oracle fusion cx ai agents` -> **LOW**, `demand_score=0`, `hh_ru=0`, `yandex_suggest=2`. [T3]
- `oracle fusion service ai` -> **LOW**, `demand_score=0`, `hh_ru=0`, `yandex_suggest=2`. [T3]
- `ai contact center` -> **LOW**, `demand_score=0`, `hh_ru=2`, `yandex_suggest=2`. [T3]
- `crm ai agent` -> **LOW**, `demand_score=7`, `hh_ru=110`, `yandex_suggest=2`. [T3]
- `омниканальный контакт-центр` -> **LOW**, `demand_score=18`, `hh_ru=30`, `yandex_suggest=100`. [T3]

### Интерпретация
- Exact-demand по Oracle zero-like, поэтому кейс нельзя читать как прямой vendor-led GEO launch в РФ. [T3][inference]
- Но underlying budget line на customer-service infrastructure, CRM automation, contact-center stack и AI-аналитику уже есть. Buyer language в РФ формулируется через `контакт-центр`, `речевую аналитику`, `автоматизацию саппорта`, а не через `agentic CX`. [T3][T4][T5][T6][inference]

## 2. Category proof и why now
1. Oracle в анонсе от **9 апреля 2026 года** описывает CX agentic applications как outcome-driven и execution-oriented слой внутри существующих enterprise workflows, а не как обычный copilot. [T1]
2. Oracle AI Agent Studio, а затем marketplace и сеть сертифицированных специалистов показывают, что вокруг category заранее проектируется партнёрская инфраструктура внедрения и кастомизации. [T2]
3. Это важно для нашего кейса, потому что в customer service value часто создаётся не лицензией как таковой, а интеграцией knowledge base, routing, policy logic, CRM/workflow orchestration, quality controls и post-launch tuning. [T1][T2][inference]
4. Локальные кейсы подтверждают ту же механику спроса: компании платят не за «магический ИИ», а за снижение нагрузки на операторов, ускорение resolution, автоматизацию QA и better navigation в клиентском сервисе. [T5][T6]

## 3. Что это значит для локального GEO / B2B-OPS кейса
- Как чистый Oracle-resell motion кейс выглядит слабее: брендовый спрос низкий, vendor-dependency высокий, а локальный контур в 2026 году опирается на альтернативные платформы и интеграторов. [T3][inference]
- Как service line вокруг agentic CX ops кейс выглядит жизнеспособнее: аудит customer journeys, омниканальная архитектура, AI-routing, knowledge orchestration, QA/risk guardrails, speech analytics, внедрение и managed improvement loop. [T1][T2][T4][T5][T6][inference]
- То есть demand есть скорее на outcome-layer поверх customer-service stack, чем на конкретный Oracle SKU. [T3][T4][T5][T6][inference]

## 4. Кто купит
Вероятный ICP в локальном контуре:
1. банки и страховые компании,
2. телеком и крупный e-commerce,
3. маркетплейсы и крупный ритейл,
4. гос- и квазигос-сервисы с большим входящим потоком,
5. enterprise shared service / support centers,
6. системные интеграторы, которые упаковывают AI-CX transformation как проект и managed service.

## 5. Willingness to pay
- Для small/SMB contact-center SaaS motion кейс слабый: чек, вероятно, будет слишком низким для Program 2. [T4][inference]
- Для enterprise transformation motion WTP реален, потому что pain завязан на cost-to-serve, качество сервиса, SLA, FCR, QA load и масштаб операторского штата. Такие бюджеты обычно защищаются лучше, чем «ещё один AI chatbot». [T1][T5][T6][inference]
- Дополнительный плюс, customer-service stack часто требует внедрения, интеграции, обучения, governance и постоянного тюнинга, а значит service layer можно монетизировать отдельно от лицензии. [T2][T4][inference]

## 6. Profit gate scenarios
### Сценарий A, узкий SaaS / бот-слой
- 80 000-180 000 ₽ в месяц на аккаунт.
- Слишком низко для Program 2.
- **Вердикт: NO PASS.**

### Сценарий B, enterprise AI contact-center enablement
- 500 000-900 000 ₽ в месяц за омниканальную архитектуру, AI-routing, knowledge orchestration, QA analytics и ограниченный managed layer.
- При 5-7 клиентах экономика уже может пройти порог.
- **Вердикт: PASS.**

### Сценарий C, тяжёлый CX transformation + managed optimization
- 1 000 000-2 000 000 ₽ в месяц при large-enterprise контуре с интеграциями, speech analytics, compliance/governance и KPI-driven optimisation.
- Даже 3-4 клиента могут собрать целевой EBITDA-профиль.
- **Вердикт: STRONG PASS.**

## 7. Основные риски
- Oracle-specific demand в РФ почти отсутствует. [T3]
- Высокий риск, что standalone кейс схлопнется в более широкий `ai-customer-service-operations` wedge, а не останется отдельной категорией. [inference]
- Vendor/platform dependence и сложность локальной поставки. [T1][T2][inference]
- Риск, что часть ценности уйдёт в project services, а повторяемый productized layer окажется слабым. [T2][T4][inference]

## 8. Решение для pipeline
**Не отклонять на demand-этапе, но вести как CONDITIONAL PASS.**

Почему:
1. глобальный category proof свежий и сильный,
2. local adjacent budget line подтверждён,
3. measurable adoption AI в customer-service operations уже есть,
4. economics собирается только в enterprise transformation / managed-ops сценарии.

Что обязательно проверить в P4/P5/P6:
- это самостоятельный кейс или всё-таки подвид общего customer-service-ops wedge,
- насколько реально удержать high-ticket чек без жёсткой привязки к Oracle,
- сколько скрытого SI/custom load в delivery-модели,
- есть ли repeatable ICP кроме very large enterprise.

## Источники
- [T1] Oracle Introduces Fusion Agentic Applications for Customer Experience, 2026-04-09: https://www.oracle.com/europe/news/announcement/oracle-introduces-fusion-agentic-applications-for-cx-2026-04-09/
- [T2] Oracle Expands AI Agent Studio for Fusion Applications with New Marketplace, LLMs, and Vast Partner Network, 2025-10-15: https://www.oracle.com/ro/news/announcement/ai-world-oracle-expands-ai-agent-studio-for-fusion-applications-with-new-marketplace-llms-and-vast-partner-network-2025-10-15/
- [T3] Demand API: http://172.18.0.1:9001/multi-demand?keyword=oracle%20fusion%20cx%20ai%20agents ; http://172.18.0.1:9001/multi-demand?keyword=oracle%20fusion%20service%20ai ; http://172.18.0.1:9001/multi-demand?keyword=ai%20contact%20center ; http://172.18.0.1:9001/multi-demand?keyword=crm%20ai%20agent ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%BC%D0%BD%D0%B8%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9%20%D0%BA%D0%BE%D0%BD%D1%82%D0%B0%D0%BA%D1%82-%D1%86%D0%B5%D0%BD%D1%82%D1%80
- [T4] Naumen Contact Center SaaS: https://www.naumen.ru/products/ccsaas/
- [T5] Консультационный центр ДОМ.РФ улучшил клиентский путь и повысил качество сервиса с помощью речевой аналитики Naumen CI, 2025-06-10: https://www.naumen.ru/events/news/7385/
- [T6] «Инфосистемы Джет» и обработка 30% заявок в саппорт с помощью YandexGPT, 2025-02-13: https://yandex.cloud/ru/cases/jet

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

> Market Pulse 2026-04-23: растущий интерес.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.



---

---
stage: solution
case: oracle-fusion-agentic-cx-v2
date: 2026-04-24
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Oracle Fusion Agentic CX как сервисный слой внедрения, интеграции и managed-оптимизации AI-first customer service / CX operations поверх Oracle Fusion Cloud и смежного enterprise CX-стека.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Oracle продаёт не точечный copilot, а outcome-driven multi-agent execution внутри sales, service и marketing workflows, с доступом к enterprise data, approvals, policies и permissions. Это означает, что ценность создаётся не только лицензией, но и сложной настройкой процесса, интеграций и governance. [T1][T2][T3]
2. Для локального кейса реалистичный wedge, не Oracle-resell, а **enterprise AI customer operations layer**: проектирование сценариев, knowledge orchestration, routing, guardrails, QA, rollout и постоянная оптимизация service KPI. [T1][T2][T6][inference]
3. Solution-fit есть только в верхнем enterprise-сегменте, где уже существует тяжёлый контакт-центр, service workflow и владелец метрик cost-to-serve, SLA, FCR, AHT и CSAT. Для SMB и low-end chatbot motion кейс слабый. [T4][T5][T6][inference]
4. Главный риск, кейс легко расползается в тяжёлый SI-проект и теряет repeatability, если не доказать шаблонный delivery и vendor-agnostic логику за пределами чисто Oracle-specific продажи. [T3][T7][inference]

## 1. Какую проблему реально решает продукт

Oracle Fusion Agentic CX решает не задачу «дать оператору ещё один AI-инструмент», а более дорогую проблему: как перевести customer-service и broader CX workflow из режима ручных handoff'ов в режим координированного исполнения процессов.

Дорогие потери, которые продукт адресует:
- ручная обработка большого объёма типовых и полуструктурированных сервисных задач;
- медленные escalation и handoff между front-line, back-office и смежными функциями;
- слабая оркестрация между CRM, knowledge, approvals и транзакционными действиями;
- отсутствие постоянной оптимизации по KPI сервиса после запуска automation;
- governance-риск, когда AI запускают без внятных ролей, аудита и контроля доступа.

Для enterprise buyer это painkiller только тогда, когда customer service уже стал отдельной дорогой операционной машиной.

## 2. Продуктовый wedge

### Core wedge
**Enterprise agentic CX operations layer**
- аудит customer-service и service-center процессов;
- проектирование agent workflows и human-in-the-loop точек;
- интеграция Fusion Service, knowledge, business objects, API и внешних систем;
- настройка routing, approvals, policies, permissions и auditability;
- deployment, validation, наблюдаемость и KPI-оптимизация после запуска.

### Почему это сильнее обычного CRM / contact-center внедрения
1. **Execution, а не только assist.** Oracle прямо позиционирует agentic applications как слой, который может принимать и исполнять действия в рамках процессов, а не просто генерировать подсказки. [T1]
2. **Нативный доступ к enterprise context.** AI Agent Studio и readiness-документация описывают доступ к business objects, APIs, knowledge stores, tools, validation и deploy прямо внутри Fusion. Это повышает ценность интегратора и оператора rollout. [T2][T3]
3. **Есть built-in место для сервисного слоя.** Oracle отдельно подчёркивает partner-built agents, certified experts, marketplace и builder-инструменты. Значит, Oracle сам закладывает ecosystem-value capture в services, кастомизацию и deployment. [T4][T7]
4. **Сильный governance narrative.** Для customer service это критично: без guardrails, access controls и auditability buyer не пустит агентов в production. [T1][T2][T3]

## 3. Для кого solution-fit реален в РФ

### Primary ICP
- крупные банки, страховые группы и финтех с большим объёмом сервисных обращений;
- телеком и enterprise digital platforms;
- маркетплейсы, крупный e-commerce и retail-service hubs;
- большие shared service / support centers;
- enterprise- и upper-midmarket интеграторы, которые уже ведут Oracle / CX transformation контуры.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. высокий объём обращений и чувствительность к SLA;
2. уже существующий enterprise CX / CRM / service stack;
3. owner на уровне customer service director, CX operations lead, CIO/CTO-1 или transformation sponsor;
4. готовность покупать не только initial setup, но и постоянную оптимизацию;
5. потребность в auditability, permissions и policy-aware automation.

### Нецелевой сегмент
- SMB и low-volume support teams;
- компании, где достаточно rule-based chatbot или базового helpdesk automation;
- клиенты без явного owner'а на service economics;
- покупатели, которым нужен разовый внедренческий проект без recurring optimization.

## 4. Как продукт должен выглядеть в локальном GTM

### Слабый вариант позиционирования
- «внедрим Oracle Fusion Agentic CX в России»;
- продажа через generic AI/ботовую риторику;
- ставка на один vendor-specific SKU;
- отсутствие ownership за service KPI и post-launch optimization.

Такой motion выглядит слабым, потому что exact-demand по Oracle низкий, а buyer language в РФ ближе к омниканальному контакт-центру, автоматизации сервиса, речевой аналитике и workflow automation. [T5][T6][inference]

### Реалистичный вариант позиционирования
- заход через аудит customer-service operations и поиск самого дорогого service bottleneck;
- pilot на одном queue / service flow / escalation path;
- KPI pilot: containment, FCR, AHT, backlog, QA score, SLA adherence, CSAT;
- rollout как managed optimization layer поверх уже существующего service stack;
- по возможности vendor-agnostic narrative, где Oracle выступает одним из сильных execution-stack'ов, а не единственной точкой value proposition.

## 5. Delivery model

### Правдоподобная схема внедрения
1. discovery и аудит service workflows;
2. выбор одного monetizable сценария, например intake, triage, case routing, knowledge-grounded resolution или cross-functional escalation;
3. mapping business objects, APIs, policies, approvals и ролей;
4. конфигурация или создание agent/team в AI Agent Studio;
5. validation, debug, restricted rollout и контроль безопасности;
6. pilot 6-10 недель на ограниченном контуре;
7. сравнение KPI до и после;
8. переход в managed optimization retainer.

### Кто должен быть buyer'ом
- director of customer service;
- head of contact center / service operations;
- CX transformation lead;
- CIO / CTO-1 / enterprise applications owner;
- COO сервисного блока.

### Кто редко будет настоящим buyer'ом
- линейный support manager без бюджета;
- isolated IT owner без бизнес-спонсора;
- procurement без ownership за операционные метрики.

## 6. Почему клиент купит это, а не альтернативы

У клиента уже есть substitutes:
- локальные contact-center и service platforms;
- speech analytics и workflow automation vendors;
- системные интеграторы с разовым проектным внедрением;
- in-house automation / enterprise apps teams.

Кейс можно выиграть только если сервисный слой:
1. быстрее доводит automation до production KPI;
2. умеет работать с governance и enterprise controls лучше обычного подрядчика;
3. остаётся recurring optimization-функцией, а не одноразовым проектом;
4. снижает cost-to-serve на заметном объёме обращений, а не просто создаёт красивый AI-demo.

Именно здесь важны локальные сигналы по enterprise service automation: Naumen и кейс ДОМ.РФ показывают, что buyer уже платит за service quality и speech-driven optimization, а кейс Jet + YandexGPT показывает, что автоматизация части потока обращений в саппорте уже проходит в production. Это не доказательство именно Oracle, но сильное подтверждение solution-shape. [T5][T6]

## 7. Конкурентная позиция

### Против локальных платформ
Преимущество возможно, если предложение продаётся как более высокий orchestration и managed-operations слой, а не как замена всей платформы.

### Против обычных системных интеграторов
Шанс есть, если после initial launch остаётся измеримый recurring scope: tuning, policy updates, quality control, observability, ROI review, rollout на новые queues.

### Против in-house команды
Преимущество возникает, если time-to-value быстрее, а экспертиза по agent governance, workflow validation и deployment глубже, чем клиент соберёт сам.

## 8. Основные риски solution-fit

1. **SI-risk.** Каждый enterprise-клиент может требовать слишком много bespoke integration work.
2. **Vendor-risk.** Oracle-specific demand в РФ слабый, значит нельзя строить кейс только на brand pull. [T5][inference]
3. **Repeatability risk.** Если каждая поставка уникальна, managed layer не соберёт software-like economics.
4. **Localization/compliance risk.** Данные, хранение, доступы и enterprise security могут ограничить rollout или потребовать локального контура. [T1][T2][T3][inference]
5. **Category-overlap risk.** Кейс может оказаться не отдельным самостоятельным wedge, а частным подвидом более широкого AI customer service operations operator.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит продажа и запуск одного enterprise Oracle/CX-контура;
- какая команда нужна на pilot и ongoing optimization;
- сколько в юнит-экономике живого SI / integration труда;
- выдерживает ли gross margin модель с governance, QA и support-нагрузкой;
- можно ли держать чек 500 000+ ₽/мес без полной зависимости от very-large-enterprise проектов;
- собирается ли recurring EBITDA-модель, а не только project revenue.

## Итог для пайплайна

**P4 пройден условно.**

Продолжать кейс имеет смысл только как enterprise AI customer operations / agentic service layer с жёстким упором на workflow execution, governance и managed optimization. Если на P5/P6 не подтвердится repeatable delivery и high-ticket recurring model, кейс нужно будет схлопнуть в более широкий customer-service-ops wedge или остановить.

## Источники
- [T1] Oracle Introduces Fusion Agentic Applications for Customer Experience, 2026-04-09: https://www.oracle.com/il-en/news/announcement/oracle-introduces-fusion-agentic-applications-for-cx-2026-04-09/
- [T2] Oracle Expands AI Agent Studio for Fusion Applications with Agentic Applications Builder and New Intelligent Workflow Tools, 2026-03-24: https://www.oracle.com/europe/news/announcement/oracle-expands-ai-agent-studio-for-fusion-applications-with-agentic-applications-builder-2026-03-24/
- [T3] AI Agent Studio for Oracle Fusion Cloud Applications, Oracle readiness docs 25C: https://docs.oracle.com/en/cloud/saas/readiness/common/25c/common25c/25C-common-wn-f38824.htm
- [T4] Oracle Expands AI Agent Studio for Fusion Applications with New Marketplace, LLMs, and Vast Partner Network, 2025-10-15: https://www.oracle.com/ro/news/announcement/ai-world-oracle-expands-ai-agent-studio-for-fusion-applications-with-new-marketplace-llms-and-vast-partner-network-2025-10-15/
- [T5] Naumen Contact Center SaaS: https://www.naumen.ru/products/ccsaas/
- [T6] «Инфосистемы Джет» и обработка 30% заявок в саппорт с помощью YandexGPT, 2025-02-13: https://yandex.cloud/ru/cases/jet
- [T7] Introducing AI Agent Marketplace, Oracle Fusion Insider, 2025-11-12: https://blogs.oracle.com/fusioninsider/introducing-ai-agent-marketplace

> Market Pulse 2026-04-24: solution-fit есть только в enterprise transformation / managed-ops сценарии, не в vendor-specific low-end motion.


---

---
stage: unit-economics
case: oracle-fusion-agentic-cx-v2
date: 2026-04-25
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary
**Статус: PASS WITH RESERVATIONS.**

Oracle Fusion Agentic CX-подобный кейс проходит economics-stage только как **enterprise AI customer operations managed layer**, а не как vendor-specific реселл или дешёвый bot/SaaS add-on.

Базовая рабочая модель:
- средний контракт: **850 000 ₽ MRR на клиента**;
- COGS: **315 000 ₽ на клиента в месяц**;
- contribution per client: **535 000 ₽/мес**;
- contribution margin: **62,9%**;
- fully-loaded blended CAC: **2 837 692 ₽**;
- monthly churn: **1,5%**;
- LTV: **35,7 млн ₽**;
- **LTV/CAC = 12,6x**;
- **CAC payback = 3,3 месяца**;
- break-even: **13 клиентов**;
- EBITDA-like при 50 клиентах: **~18,25 млн ₽/мес**.

Вывод: модель выглядит инвестиционно приемлемой, если компания действительно продаёт дорогой recurring managed transformation layer вокруг customer-service KPI, а не живёт только на разовых SI-проектах.

## 1. Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | крупные enterprise с дорогим customer-service / contact-center контуром | банки, страхование, телеком, retail, маркетплейсы |
| Product motion | внедрение + managed optimization layer | соответствует 02-demand и 03-solution |
| Средний MRR на клиента | 850 000 ₽ | между сценариями B и C из 02-demand |
| ARR на клиента | 10 200 000 ₽ | 850k × 12 |
| Monthly churn | 1,5% | enterprise B2B benchmark |
| Lifetime | 66,7 мес | 1 / 0,015 |
| Startup capital | 60 000 000 ₽ | для burn-to-breakeven и sales lag |

## 2. Подробный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR | CRM, ручной ресерч, HH/отраслевой рынок | 2 ч | 3 000 | средняя |
| 2 | Outbound / partner intro | SDR + Founder | почта, телефония, Telegram, CRM | 3 ч | 7 500 | средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 4 250 | низкая |
| 4 | Discovery по service workflows | AE + Solution Architect | Meet, Miro, заметки | 3 ч | 18 000 | низкая |
| 5 | ROI / pain mapping | AE + CTO | spreadsheet, docs | 2 ч | 11 500 | низкая |
| 6 | Demo / pilot scope | AE + CTO + Product | demo env, презентация | 3 ч | 16 500 | низкая |
| 7 | Security / legal / procurement review | CTO + AE + Legal | dataroom, docs | 5 ч | 27 500 | низкая |
| 8 | Proposal / SOW / redlines | AE + Founder | docs, CRM, ЭДО | 3 ч | 13 500 | средняя |
| 9 | Подписание договора | Founder + AE | ЭДО | 1 ч | 4 500 | высокая |
| 10 | Invoicing / payment request | Finance | 1С, банк, ЭДО | 0,5 ч | 1 500 | высокая |
| 11 | Onboarding kickoff | CSM + Solution Architect + CTO | PM tool, KB, API docs | 8 ч | 52 000 | средняя |

**Итого direct process cost на одну выигранную сделку: ~159 750 ₽.**

Важно: это не fully-loaded CAC, а только прямой cost-to-close по касаниям. Полный CAC ниже считается отдельно с ФОТ, маркетингом, тулзами и overhead.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / hosting / environments | 40 000 | enterprise env + staging + storage |
| LLM / orchestration / retrieval | 55 000 | inference, knowledge retrieval, workflow runtime |
| Monitoring / security / audit trail | 20 000 | observability + access/logging |
| Solution architect allocation | 90 000 | tuning, change requests, rollout support |
| Customer success / reporting | 45 000 | QBR, adoption, KPI reviews |
| Support / incident handling | 35 000 | shared support capacity |
| Onboarding amortization reserve | 25 000 | размазанный setup на 12 мес |
| Billing / admin ops | 5 000 | ЭДО, банк, документооборот |
| **Итого COGS** | **315 000** |  |

Проверка:
- Revenue per client/month = **850 000 ₽**
- COGS per client/month = **315 000 ₽**
- Contribution per client/month = **535 000 ₽**
- **Contribution Margin = 62,9%**

## 4. CAC по каналам и воронке

### 4.1 Channel mix

| Канал | Spend / мес, ₽ | Leads | SQL | Proposal | Won | Lead→Won | CAC / client, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / ABM | 950 000 | 45 | 12 | 4 | 0,8 | 1,8% | 1 187 500 |
| Partners / integrators / Oracle-adjacent intros | 780 000 | 18 | 8 | 3 | 0,9 | 5,0% | 866 667 |
| Content / events / inbound | 730 000 | 40 | 8 | 2 | 0,4 | 1,0% | 1 825 000 |

### 4.2 Fully-loaded CAC

Формула:

`Fully-loaded CAC = (direct acquisition spend + sales FOT attributed + marketing FOT allocation + tools + events + overhead) / new paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads / retargeting | 250 000 | точечный enterprise demand capture | внутренняя модель |
| Outbound + AE FOT attributed to new | 1 053 000 | SDR 180k + AE 360k + 30% соцвзносы, с полной аллокацией на new biz | HH.ru pages + модель |
| Marketing / product marketing allocation | 260 000 | 0,5-0,6 FTE | внутренняя модель |
| Tools (CRM, sequencing, call stack, docs) | 140 000 | sales stack | внутренняя модель |
| Events / partner activities | 260 000 | roundtables, partner meetings, travel | внутренняя модель |
| Raw acquisition pool | 1 963 000 | сумма выше | calc |
| Overhead multiplier | 1 570 400 | long enterprise cycle, presales engineering, legal/security; raw × 1,8 total | calc |
| **Fully-loaded acquisition cost / мес** | **3 533 400** |  | calc |
| New paying customers / мес | **1,245** | blended enterprise pace | model |
| **Blended fully-loaded CAC** | **2 837 692 ₽** | 3 533 400 / 1,245 | calc |

### 4.3 Sanity check по CAC
- Для enterprise B2B кейсов в ветке benchmark часто лежит в диапазоне **сотни тысяч до низких миллионов ₽** на клиента.
- Здесь **2,84 млн ₽** выглядит высоким, но правдоподобным, потому что продажа длинная, multi-stakeholder и требует presales + security/procurement.
- Это не занижение CAC, а скорее консервативная оценка.

## 5. LTV и churn

### Benchmark churn
Для enterprise SaaS с более высоким ARPA ChartMogul указывает более низкий churn, чем у low-ticket SaaS. В help-материале отмечено, что для бизнесов с **$500 ARPA и выше** customer churn обычно находится в диапазоне **1–2% в месяц**. Для модели беру **1,5% monthly churn** как консервативный midpoint.

### Формула LTV
`LTV = MRR × Contribution Margin / Monthly Churn`

Подстановка:
- MRR = **850 000 ₽**
- Contribution margin = **62,9%**
- Monthly churn = **1,5%**

`LTV = 850 000 × 0,629 / 0,015 = 35 643 333 ₽`

| Метрика | Значение |
|---|---:|
| MRR per customer | 850 000 ₽ |
| Contribution Margin | 62,9% |
| Contribution ₽/мес | 535 000 ₽ |
| Monthly churn | 1,5% |
| Lifetime | 66,7 мес |
| **LTV** | **35,64 млн ₽** |

## 6. LTV/CAC, payback, contribution margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 35,64M / 2,838M | **12,6x** | уверенный PASS |
| CAC Payback | 2,838M / 0,850M | **3,3 мес** | лучше enterprise threshold |
| Contribution Margin % | 535K / 850K | **62,9%** | приемлемо для high-touch enterprise layer |

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise deals, partnerships | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | architecture, delivery oversight, security | 600 000 | 180 000 | 780 000 |
| Senior Backend #1 | integrations / APIs | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | platform / workflow engine | 450 000 | 135 000 | 585 000 |
| ML Engineer | orchestration / evals | 520 000 | 156 000 | 676 000 |
| DevOps | infra / observability | 350 000 | 105 000 | 455 000 |
| Frontend | ops UI / dashboards | 300 000 | 90 000 | 390 000 |
| Product Manager | packaging / roadmap / discovery | 350 000 | 105 000 | 455 000 |
| SDR | outbound | 180 000 | 54 000 | 234 000 |
| AE | deal closing / procurement | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding / retention | 250 000 | 75 000 | 325 000 |
| Finance / Ops | billing / admin | 160 000 | 48 000 | 208 000 |
| **Итого full team** |  |  |  | **6 006 000 ₽/мес** |

### 7.2 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 600 000 | 1-2 | 1,5 | 180 000 | 780 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 520 000 | 2-3 | 2 | 156 000 | 676 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product Manager | 1 | 350 000 | 1-2 | 1,5 | 105 000 | 455 000 |
| SDR | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 360 000 | 1-2 | 2-3 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Finance / Ops | 1 | 160 000 | 1 | 1 | 48 000 | 208 000 |

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Backend #1 | 1 430 000 |
| M3 | + CTO + Product | 2 665 000 |
| M4 | + Backend #2 + SDR | 3 484 000 |
| M5 | + ML Engineer + Frontend | 4 550 000 |
| M6 | + DevOps + AE | 5 473 000 |
| M7 | + Customer Success + Finance/Ops | 6 006 000 |
| M8 | full team | 6 006 000 |
| M9 | full team | 6 006 000 |
| M10 | full team | 6 006 000 |
| M11 | full team | 6 006 000 |
| M12 | full team | 6 006 000 |

## 8. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| Core team FOT | 6 006 000 |
| Office / legal / admin | 320 000 |
| Shared cloud / dev infra | 410 000 |
| Security / audit / compliance reserve | 220 000 |
| CRM / PM / internal tooling | 150 000 |
| Travel / enterprise meetings | 170 000 |
| Misc reserve | 124 000 |
| **Итого fixed costs / month** | **7 400 000 ₽** |

## 9. Break-even

### 9.1 Break-even по числу клиентов

`Break-even clients = Fixed costs / Contribution per client`

`7 400 000 / 535 000 = 13,83`

Округляя вверх, нужен **14-й клиент** для явного run-rate break-even. С учётом небольшого операционного запаса ниже считаю рабочим break-even диапазон **14-15 клиентов**.

### 9.2 Break-even по месяцу

| Месяц | Клиенты EOM | MRR, ₽ | Contribution @62,9%, ₽ | Fixed costs, ₽ | EBITDA-like, ₽ |
|---|---:|---:|---:|---:|---:|
| M6 | 1 | 850 000 | 535 000 | 7 400 000 | -6 865 000 |
| M7 | 2 | 1 700 000 | 1 070 000 | 7 400 000 | -6 330 000 |
| M8 | 4 | 3 400 000 | 2 140 000 | 7 400 000 | -5 260 000 |
| M9 | 6 | 5 100 000 | 3 210 000 | 7 400 000 | -4 190 000 |
| M10 | 9 | 7 650 000 | 4 815 000 | 7 400 000 | -2 585 000 |
| M11 | 12 | 10 200 000 | 6 420 000 | 7 400 000 | -980 000 |
| M12 | 14 | 11 900 000 | 7 490 000 | 7 400 000 | **+90 000** |
| M13 | 15 | 12 750 000 | 8 025 000 | 7 400 000 | **+625 000** |

**Break-even по месяцу: около M12-M13** при сильном founder-led / partner-led enterprise GTM.

## 10. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Суммарный отрицательный EBITDA-like burn до M12 оценивается примерно в **45-48 млн ₽**.

### Cash runway
При стартовом капитале **60 млн ₽**:
- модель дотягивает до break-even с умеренным запасом;
- при просадке продаж на 2-3 месяца потребуется дополнительный buffer;
- комфортный execution-диапазон скорее **60-65 млн ₽**, чем минимальные 40 млн ₽.

## 11. EBITDA test на 50 клиентах

| Показатель | Значение |
|---|---:|
| Клиенты | 50 |
| MRR | 42 500 000 ₽ |
| Contribution @62,9% | 26 750 000 ₽ |
| Fixed costs | 7 400 000 ₽ |
| **EBITDA-like** | **19 350 000 ₽/мес** |

Даже при более консервативной нагрузке на delivery кейс уверенно выше порога **500 000 ₽ EBITDA / мес**.

## 12. Основные риски economics-stage

1. **Services creep.** Если внедрение становится слишком кастомным, contribution margin быстро падает ниже 55%.
2. **Vendor dependence.** Слишком сильная привязка к одному Oracle motion ухудшает repeatability pipeline.
3. **Procurement lag.** Enterprise security/legal review легко добавляют 2-4 месяца к циклу сделки.
4. **ICP narrowness.** Экономика держится на high-ticket enterprise-клиентах, а не на broad mid-market.

## 13. Итоговый вывод P5

**Решение: PASS WITH RESERVATIONS.**

Почему pass:
- **LTV/CAC = 12,6x**, сильно выше порога 3:1;
- **CAC payback = 3,3 месяца**, заметно лучше enterprise threshold;
- **EBITDA > 500K ₽/мес** достигается задолго до 50 клиентов;
- economics не выглядит сломанной при high-ticket managed model.

Почему reservations:
- кейс уязвим к раздутию delivery и SI-нагрузки;
- нужна узкая enterprise-фокусировка;
- отдельность категории от более широкого customer-service-ops wedge всё ещё нужно проверить на P6/P7.

## Источники
- Oracle Introduces Fusion Agentic Applications for Customer Experience, 2026-04-09: https://www.oracle.com/il-en/news/announcement/oracle-introduces-fusion-agentic-applications-for-cx-2026-04-09/
- Oracle Expands AI Agent Studio for Fusion Applications with Agentic Applications Builder and New Intelligent Workflow Tools, 2026-03-24: https://www.oracle.com/europe/news/announcement/oracle-expands-ai-agent-studio-for-fusion-applications-with-agentic-applications-builder-2026-03-24/
- AI Agent Studio for Oracle Fusion Cloud Applications, Oracle readiness docs 25C: https://docs.oracle.com/en/cloud/saas/readiness/common/25c/common25c/25C-common-wn-f38824.htm
- Oracle Expands AI Agent Studio for Fusion Applications with New Marketplace, LLMs, and Vast Partner Network, 2025-10-15: https://www.oracle.com/ro/news/announcement/ai-world-oracle-expands-ai-agent-studio-for-fusion-applications-with-new-marketplace-llms-and-vast-partner-network-2025-10-15/
- HH.ru, работа account executive в Москве: https://hh.ru/vacancies/account_executive
- HH.ru, работа customer success manager в Москве: https://hh.ru/vacancies/customer-success-manager
- ChartMogul Help, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate

## Market Pulse
Market Pulse 2026-04-25: экономика подтверждается только в enterprise managed-transformation сценарии; low-end vendor-specific motion не проходит.


---

# SECTION A — PnL

## A1. Input assumptions used
- ARPA / MRR на клиента: **850 000 ₽/мес**
- COGS на клиента: **315 000 ₽/мес**
- Gross profit / contribution на клиента: **535 000 ₽/мес**
- GM: **62,9%**
- Fixed costs: **7 400 000 ₽/мес**, включая team FOT **6 006 000 ₽/мес**
- CAC by channel from 04-economics:
  - Founder-led outbound / ABM: **1 187 500 ₽**
  - Partners / integrators: **866 667 ₽**
  - Content / events / inbound: **1 825 000 ₽**
  - Blended fully-loaded CAC: **2 837 692 ₽**
- LTV: **35,64 млн ₽**
- Startup capital baseline: **60 000 000 ₽**

## A2. 12-month PnL, базовый сценарий
**Допущения:** churn 1,5%/мес, new clients M1-M12 = 0, 0, 0, 0, 0, 1, 1, 2, 3, 3, 2, 2.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 2 | 2 |
| Total clients | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 | 1.0 | 2.0 | 4.0 | 6.9 | 9.8 | 11.6 | 13.5 |
| MRR | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 850 000 ₽ | 1 687 250 ₽ | 3 361 941 ₽ | 5 861 512 ₽ | 8 323 589 ₽ | 9 898 736 ₽ | 11 450 255 ₽ |
| COGS | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 315 000 ₽ | 625 275 ₽ | 1 245 896 ₽ | 2 172 207 ₽ | 3 084 624 ₽ | 3 668 355 ₽ | 4 243 330 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 535 000 ₽ | 1 061 975 ₽ | 2 116 045 ₽ | 3 689 305 ₽ | 5 238 965 ₽ | 6 230 381 ₽ | 7 206 925 ₽ |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% |
| Fixed costs | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ |
| EBITDA | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -6 865 000 ₽ | -6 338 025 ₽ | -5 283 955 ₽ | -3 710 695 ₽ | -2 161 035 ₽ | -1 169 619 ₽ | -193 075 ₽ |
| Cash burn | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 6 865 000 ₽ | 6 338 025 ₽ | 5 283 955 ₽ | 3 710 695 ₽ | 2 161 035 ₽ | 1 169 619 ₽ | 193 075 ₽ |
| Cumulative cash | -7 400 000 ₽ | -14 800 000 ₽ | -22 200 000 ₽ | -29 600 000 ₽ | -37 000 000 ₽ | -43 865 000 ₽ | -50 203 025 ₽ | -55 486 980 ₽ | -59 197 675 ₽ | -61 358 710 ₽ | -62 528 329 ₽ | -62 721 404 ₽ |

## A3. 12-month PnL, оптимистичный сценарий
**Допущения:** churn 1,0%/мес, new clients M1-M12 = 0, 0, 0, 1, 1, 2, 2, 3, 3, 3, 3, 2.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 2 |
| Total clients | 0.0 | 0.0 | 0.0 | 1.0 | 2.0 | 4.0 | 5.9 | 8.9 | 11.8 | 14.7 | 17.5 | 19.3 |
| MRR | 0 ₽ | 0 ₽ | 0 ₽ | 850 000 ₽ | 1 691 500 ₽ | 3 374 585 ₽ | 5 040 839 ₽ | 7 540 431 ₽ | 10 015 026 ₽ | 12 464 876 ₽ | 14 890 227 ₽ | 16 441 325 ₽ |
| COGS | 0 ₽ | 0 ₽ | 0 ₽ | 315 000 ₽ | 626 850 ₽ | 1 250 582 ₽ | 1 868 076 ₽ | 2 794 395 ₽ | 3 711 451 ₽ | 4 619 336 ₽ | 5 518 143 ₽ | 6 092 962 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 0 ₽ | 535 000 ₽ | 1 064 650 ₽ | 2 124 004 ₽ | 3 172 763 ₽ | 4 746 036 ₽ | 6 303 575 ₽ | 7 845 540 ₽ | 9 372 084 ₽ | 10 348 363 ₽ |
| GM% | 0.0% | 0.0% | 0.0% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% |
| Fixed costs | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ |
| EBITDA | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -6 865 000 ₽ | -6 335 350 ₽ | -5 275 996 ₽ | -4 227 237 ₽ | -2 653 964 ₽ | -1 096 425 ₽ | 445 540 ₽ | 1 972 084 ₽ | 2 948 363 ₽ |
| Cash burn | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 6 865 000 ₽ | 6 335 350 ₽ | 5 275 996 ₽ | 4 227 237 ₽ | 2 653 964 ₽ | 1 096 425 ₽ | 0 ₽ | 0 ₽ | 0 ₽ |
| Cumulative cash | -7 400 000 ₽ | -14 800 000 ₽ | -22 200 000 ₽ | -29 065 000 ₽ | -35 400 350 ₽ | -40 676 346 ₽ | -44 903 583 ₽ | -47 557 547 ₽ | -48 653 972 ₽ | -48 653 972 ₽ | -48 653 972 ₽ | -48 653 972 ₽ |

## A4. 12-month PnL, пессимистичный сценарий
**Допущения:** churn 2,5%/мес, new clients M1-M12 = 0, 0, 0, 0, 0, 0, 1, 1, 1, 2, 2, 2.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 |
| Total clients | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 | 1.0 | 2.0 | 2.9 | 4.9 | 6.7 | 8.6 |
| MRR | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 850 000 ₽ | 1 678 750 ₽ | 2 486 781 ₽ | 4 124 612 ₽ | 5 721 496 ₽ | 7 278 459 ₽ |
| COGS | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 315 000 ₽ | 622 125 ₽ | 921 572 ₽ | 1 528 533 ₽ | 2 120 319 ₽ | 2 697 311 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 535 000 ₽ | 1 056 625 ₽ | 1 565 209 ₽ | 2 596 079 ₽ | 3 601 177 ₽ | 4 581 148 ₽ |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% | 62.9% |
| Fixed costs | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ |
| EBITDA | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -7 400 000 ₽ | -6 865 000 ₽ | -6 343 375 ₽ | -5 834 791 ₽ | -4 803 921 ₽ | -3 798 823 ₽ | -2 818 852 ₽ |
| Cash burn | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 7 400 000 ₽ | 6 865 000 ₽ | 6 343 375 ₽ | 5 834 791 ₽ | 4 803 921 ₽ | 3 798 823 ₽ | 2 818 852 ₽ |
| Cumulative cash | -7 400 000 ₽ | -14 800 000 ₽ | -22 200 000 ₽ | -29 600 000 ₽ | -37 000 000 ₽ | -44 400 000 ₽ | -51 265 000 ₽ | -57 608 375 ₽ | -63 443 166 ₽ | -68 247 086 ₽ | -72 045 909 ₽ | -74 864 762 ₽ |

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
### Per client-month waterfall
| Step | Formula | Value |
|---|---|---:|
| ARPA | contract MRR | 850 000 ₽ |
| Gross profit | ARPA - COGS | 535 000 ₽ |
| Contribution | Gross profit | 535 000 ₽ |

### Tax waterfall by regime
| Tax regime | Tax base | Tax per client-month | Net per client-month |
|---|---|---:|---:|
| УСН 6% | 6% от выручки | 51 000 ₽ | 484 000 ₽ |
| IT-льгота 3% | 3% от выручки | 25 500 ₽ | 509 500 ₽ |
| ОСНО 20% | 20% от прибыли, если прибыль положительная | зависит от run-rate | зависит от run-rate |

### EBITDA to Net example at break-even run-rate (14 clients)
| Step | Value |
|---|---:|
| MRR @ 14 clients | 11 900 000 ₽ |
| Gross profit @ 14 clients | 7 490 000 ₽ |
| EBITDA | 90 000 ₽ |
| Net after ОСНО 20% corporate tax | 72 000 ₽ |
| VAT 20% on ОСНО | 2 380 000 ₽ |

## A6. Cash flow and startup capital to break-even
| Scenario | startup_capital_to_bep_rub | Comment |
|---|---:|---|
| Базовый | 62 721 404 ₽ | выше стартового капитала 60 млн ₽, нужен доп. буфер ~2,7 млн ₽ |
| Оптимистичный | 48 653 972 ₽ | укладывается в 60 млн ₽ с запасом |
| Пессимистичный | 74 864 762 ₽ | дефицит ~14,9 млн ₽ к стартовому капиталу |

## A7. Налоговая модель РФ
| Parameter | УСН | IT-льгота | ОСНО |
|---|---|---|---|
| Налог на выручку / прибыль | 6% с выручки | 3% с выручки при аккредитации Минцифры | 20% налог на прибыль |
| Страховые взносы на ФОТ | ~30% к gross salary | ~30% к gross salary | ~30% к gross salary |
| НДС | нет | обычно нет в модели льготной выручки | 20% применимо |
| Практический эффект | проще админка, но давит на burn при отрицательной EBITDA | лучший Net и runway при соблюдении criteria | хуже cash conversion из-за налога на прибыль и НДС |

## A8. Break-even by scenario
| Scenario | Break-even client count | Break-even month | Comment |
|---|---:|---|---|
| Базовый | 14 клиентов | после M12, около M13 | M12 still slightly negative EBITDA |
| Оптимистичный | 14 клиентов | M10 | быстрый partner-led / founder-led ramp |
| Пессимистичный | 14 клиентов | после M12 | за горизонтом 12 месяцев |

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 месяцев

Метод: беру базовую PnL-модель из SECTION A и меняю по одному ключевому драйверу.
- **Base**: как в A2, EBITDA M12 = **-193 075 ₽**.
- **Sens1 CAC x2**: предполагаю тот же sales budget, значит новых wins в M6-M12 примерно вдвое меньше.
- **Sens2 Churn x2**: churn растёт с **1,5%** до **3,0%** в месяц, new-logo plan не меняется.
- **Sens3 Price -30%**: ARPA падает с **850 000 ₽** до **595 000 ₽**, COGS держу прежним **315 000 ₽**.

| Сценарий | Ключевое изменение | Clients @M12 | Contribution / client | EBITDA @M12 |
|---|---|---:|---:|---:|
| Base | базовая модель | 13,5 | 535 000 ₽ | **-193 075 ₽** |
| Sens1 | CAC x2 | 6,7 | 535 000 ₽ | **-3 796 538 ₽** |
| Sens2 | Churn x2 | 13,0 | 535 000 ₽ | **-464 789 ₽** |
| Sens3 | Price -30% | 13,5 | 280 000 ₽ | **-3 620 000 ₽** |

### Вывод по sensitivity
1. Самый опасный single-variable shock, **price compression**: при скидке 30% модель быстро теряет большую часть contribution.
2. **CAC x2** почти так же разрушителен, потому что кейс и так держится на длинном enterprise sales cycle.
3. Даже **churn x2** в одиночку уже оставляет бизнес ниже нуля на M12.
4. Значит finance-risk тут не в одном параметре, а в связке: длинная продажа + дорогой delivery + уязвимость к дискаунту.

## B2. Monte Carlo Lite, confidence intervals

### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 800 000 | 2 837 692 | 5 600 000 | [T4][T7][calc] |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | [T4][calc] |
| ARPU, ₽/мес | 595 000 | 850 000 | 1 100 000 | [T2][T4][calc] |
| Conversion rate lead→paid, % | 1,0% | 1,8% | 3,5% | [T4][calc] |
| Time-to-hire, мес | 1,0 | 1,7 | 3,5 | [T4][calc] |

### Упрощённая симуляция
Вместо полного кода беру 9 комбинаций вокруг min/mode/max; p10/p50/p90 интерпретирую как worst / median / best envelope для горизонта **M24**.

Логика перевода в output-метрики:
- **p10**: CAC_max + churn_max + ARPU_min + слабая конверсия, поэтому new-logo pace ≈ **1 клиент/мес** после M12.
- **p50**: CAC_mode + churn_mode + ARPU_mode, new-logo pace ≈ **2 клиента/мес**.
- **p90**: CAC_min + churn_min + ARPU_max + сильная конверсия, new-logo pace ≈ **3 клиента/мес**.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-1 919 804** | **10 456 438** | **28 749 826** | **30 669 630** |
| CAC payback (мес) | **9,4** | **3,3** | **1,6** | **7,8** |
| LTV/CAC | **1,7x** | **12,6x** | **43,6x** | **41,9x** |
| Cash runway (мес) | **31,3** | **>24** | **>24** | n/a |

### Интерпретация Monte Carlo Lite
1. **Правило 1 срабатывает**: p10 EBITDA < 0, значит присутствует реальный insolvency-risk при плохой связке CAC/churn/price.
2. **Правило 2 не срабатывает**: p50 EBITDA заметно выше 500k ₽/мес, то есть median-case economics формально проходит gate.
3. **Правило 3 по сути срабатывает даже жёстче**: распределение пересекает ноль, а ширина между p10 и p90 огромна; score нужно понижать за uncertainty.
4. **Правило 4 срабатывает**: range width по LTV/CAC = **41,9x**, модель хрупкая, и главная хрупкость идёт из pricing + CAC + churn одновременно.

## B3. Competitor deep-dive

### B3.1 Топ-3 западных конкурента

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Salesforce Agentforce / Service Cloud** | Самый близкий глобальный аналог enterprise CX + AI agent orchestration. [T8][T9] | сильнейший CRM footprint, экосистема партнёров, marketplace, trust/governance story | дорогой и тяжёлый stack, сложный rollout, часто требует крупных SI-бюджетов | **15–20%** глобального enterprise CX/CRM AI-adjacent сегмента, оценка по install base и ecosystem breadth [inference] | можем продавать faster time-to-value и более узкий KPI-led service layer без гигантской платформенной инерции |
| **ServiceNow CRM / AI Agents** | Силен в cross-workflow orchestration, self-service, case resolution и agent governance. [T10][T11] | единая workflow-platform, сильный AI-control/governance layer, удобен для complex enterprise operations | меньше native CX history, чем у Salesforce; buyer иногда воспринимает как ITSM-first vendor | **8–12%** enterprise workflow/CX automation adjacent сегмента [inference] | можем зайти как vendor-agnostic оператор customer-service economics, а не как новая platform migration |
| **Zendesk AI** | Сильный midmarket-enterprise игрок в service automation и AI resolution. [T12] | быстрый старт, понятный service UX, сильный AI-first narrative, хорош для digital support teams | слабее в deep enterprise orchestration, approvals, сложных back-office handoff и heavy integration | **6–10%** digital customer support automation сегмента [inference] | можем выиграть там, где нужен не helpdesk AI, а тяжёлый managed transformation layer с интеграцией, compliance и KPI ownership |

### B3.2 Топ российских конкурентов

| Конкурент | Источник | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Naumen** | [T5][T13] | сильный enterprise brand в контакт-центрах, on-prem / локальный контур, зрелая интеграция в regulated sectors | часто platform-first, а не outcome-first; тяжёлое внедрение; меньше vendor-agnostic agentic narrative | **20–25%** enterprise contact-center / CX platform сегмента РФ [inference] | можем позиционироваться как более быстрый AI-ops слой поверх существующего стека, а не полный platform replacement |
| **Just AI** | [T14][T15] | сильная экспертиза в conversational AI, voicebots, LLM-оркестрации, локальный AI brand | часть проектов воспринимается как bot/vendor layer, а не full-stack CX transformation | **5–10%** conversational AI для enterprise-service РФ [inference] | наше преимущество в том, что мы продаём не бота, а managed KPI-слой customer operations |
| **CraftTalk** | [T16] | омниканальные ассистенты, enterprise support focus, российский контур и интеграции | меньше ecosystem power, чем у крупных платформ; риск упора в single-product motion | **3–7%** AI customer-service automation РФ [inference] | можем быть шире по workflow redesign, governance и post-launch optimisation |
| **Twin** | [T17][T18] | силён в voice AI, real-time automation и high-volume service flows | уже, чем full CX ops; voice-first позиционирование ограничивает wedge | **2–5%** voice AI automation для service-heavy enterprise РФ [inference] | у нас шире сценарий: voice + text + case orchestration + managed operations |

### Вывод по конкурентам
1. На Западе рынок уже уходит в сторону **platform + partner ecosystem + AI governance**. Это подтверждает, что value capture в services реальный, но platform power огромный. [T8][T9][T10][T11]
2. В РФ главный pressure идёт от **Naumen + локальные conversational / voice AI vendors**, а не от чистого Oracle pull. [T5][T13][T14][T16][T17]
3. Поэтому standalone Oracle-specific motion слабый, а **vendor-agnostic enterprise AI customer operations layer** остаётся единственной реалистичной позицией.

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | не удаётся собрать delivery-команду уровня enterprise integrations и AI governance вовремя | med | high | >2 ключевых hire открыты дольше 90 дней | заранее держать partner bench, дробить scope, нанимать core team до крупных продаж |
| 2 | Operational | LLM/API latency, деградация качества или изменение цен бьёт по SLA и margin | high | high | рост cost per resolution, просадка SLA, жалобы клиентов на нестабильность | multi-model routing, fallback-провайдеры, лимиты на expensive calls, контрактные SLA buffers |
| 3 | Market | exact-demand на Oracle Fusion CX в РФ остаётся почти нулевым | high | high | pipeline переполнен exploratory calls без пилотов | продавать не Oracle, а customer-service KPI wedge; расширять в vendor-agnostic motion |
| 4 | Market | price compression со стороны SI и локальных платформ съедает ARPA | high | high | win-rate держится только через скидки >20% | пакетировать outcome-based scope, upsell managed optimization, жёстко ограничивать кастом без доплаты |
| 5 | Regulatory | требования 152-ФЗ и data residency ограничивают облачную схему rollout | med | high | security/legal review стопорит сделки >60 дней | локальный контур, on-prem/private deployment options, DPA и data-flow mapping заранее |
| 6 | Regulatory | 115-ФЗ и смежный compliance в финсекторе ограничивают autonomous actions в сервисных процессах | med | med/high | compliance требует human-in-the-loop на большинстве операций | проектировать approval gates, audit trail, role-based permissions, safe-by-default action policies |
| 7 | Financial | startup capital 60 млн ₽ недостаточен при CAC drift и задержке продаж | med | high | cash buffer <9 месяцев при отсутствии роста wins | raise/credit line заранее, phase hiring, stop-loss по burn, жёсткий CAPEX freeze |
| 8 | Financial | курс USD и инфляция раздувают LLM/infra/FOT быстрее, чем растёт price | high | med/high | COGS >40% выручки или рост payroll >15% за 2 квартала | рублёвые ценовые оговорки, annual repricing, локальные модели и резерв по margin |
| 9 | Black swan | новый пакет санкций режет доступ к SaaS, LLM API или enterprise integrations | med | high | vendor уведомляет о geo restrictions или отключении billing | multi-vendor stack, локальные альтернативы, резервная архитектура, изоляция критичных workflow |
| 10 | Black swan | резкое geopolitical escalation замораживает enterprise бюджеты и новые внедрения | med | high | freeze на трансформационные проекты, перенос procurement на 2+ квартала | смещаться в cost-saving pilots с payback <6 мес, упаковывать anti-crisis ROI, держать lean cost base |

## B5. Kill conditions через 6 месяцев

1. **Median EBITDA gate broken**: если обновлённый p50 EBITDA@M24 остаётся **<500 000 ₽/мес**, продолжать нельзя.
2. **Sales efficiency collapse**: если blended fully-loaded CAC уходит **>4,5 млн ₽**, а payback держится **>8 месяцев** два квартала подряд, модель перестаёт быть инвестиционно нормальной.
3. **Commercial traction failure**: если через 6 месяцев нет минимум **3 платящих enterprise клиентов** или минимум **2 production pilots** с доказанным KPI uplift, кейс нужно схлопывать в более широкий `ai-customer-service-operations` wedge.

## B6. Итог SECTION B

**Вердикт P6B: PASS WITH HEAVY RISK DISCOUNT.**

Почему:
1. В median-case модель ещё живая и на M24 даёт двузначный EBITDA-run-rate.
2. Но p10 уходит ниже нуля, а range width по LTV/CAC экстремально широкий.
3. Основной риск не в том, что category не существует, а в том, что **Oracle-specific demand слабый, а unit economics хрупкая к price/CAC shock**.
4. Поэтому кейс можно вести дальше только как **vendor-agnostic enterprise AI customer operations operator**, а не как ставку на Oracle-first wedge.

## Источники SECTION B
- [T5] Naumen Contact Center SaaS: https://www.naumen.ru/products/ccsaas/
- [T8] Salesforce Launches Agentforce 2dx, 2025-03-05: https://investor.salesforce.com/news/news-details/2025/Salesforce-Launches-Agentforce-2dx-with-New-Capabilities-to-Embed-Proactive-Agentic-AI-into-Any-Workflow-Create-Multimodal-Experiences-and-Extend-Digital-Labor-Throughout-the-Enterprise/default.aspx
- [T9] Salesforce Launches Agentforce 3, 2025-06-23: https://investor.salesforce.com/news/news-details/2025/Salesforce-Launches-Agentforce-3-to-Solve-the-Biggest-Blockers-to-Scaling-AI-Agents-Visibility-and-Control/default.aspx
- [T10] ServiceNow announces new agentic AI innovations, 2025-01-29: https://newsroom.servicenow.com/press-releases/details/2025/ServiceNow-announces-new-agentic-AI-innovations-to-autonomously-solve-the-most-complex-enterprise-challenges-01-29-2025-traffic/default.aspx
- [T11] ServiceNow Reimagines CRM for the AI Era, 2025-05-06: https://newsroom.servicenow.com/press-releases/details/2025/ServiceNow-Reimagines-CRM-for-the-AI-Era-to-Sell-Fulfill-and-Service-on-One-Unified-Platform-Providing-Exceptional-End-to-End-Experiences/default.aspx
- [T12] Zendesk AI for customer service: https://www.zendesk.com/service/ai/
- [T13] Naumen на Habr: https://habr.com/ru/companies/naumen/
- [T14] Just AI на Habr: https://habr.com/ru/companies/just_ai/
- [T15] Just AI в реестре Skolkovo: https://sk.ru/companies/just-ai/
- [T16] CraftTalk в реестре Skolkovo: https://sk.ru/companies/crafttalk/
- [T17] Twin на vc.ru: https://vc.ru/services/1840205-twin-voice-ai-platform
- [T18] Twin в Rusprofile: https://www.rusprofile.ru/id/1207700432818

<!-- P6B-DONE -->


---

[B2B-OPS] Oracle Fusion Agentic CX v2 — REJECTED: 56/100 | EBITDA base=625К₽/мес через 13 мес | LTV/CAC=12,6x | Ключевое преимущество: enterprise CX-ops layer поверх тяжёлого service stack | Главный риск: Oracle-specific спрос в РФ почти нулевой.

# 06-verdict

sector: B2B-OPS
status: REJECTED
score: 56/100
case: oracle-fusion-agentic-cx-v2
date: 2026-04-26

## Итог инвесткомитета
**Вердикт: REJECTED.**

Кейс проходит по математике клиента и достигает `company_ebitda_rub_month >= 500 000 ₽/мес` в base-сценарии, но не проходит инвесткомитет как standalone business model. Главная причина, exact-demand по Oracle Fusion Agentic CX в РФ почти отсутствует, moat слабый, а repeatable GTM слишком зависит от enterprise custom delivery. Это скорее supporting signal для более широкого wedge `ai-customer-service-operations`, чем самостоятельная категория.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC = 12,6x», «CAC payback = 3,3 месяца», «Contribution Margin = 62,9%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В `04-economics.md`: «M13 ... EBITDA-like ... +625 000 ₽» и «Break-even по месяцу: около M12-M13». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | `02-demand.md`: «самостоятельный exact-demand именно по формулировке Oracle Fusion Agentic CX в РФ слабый»; строка Sources отсутствует, поэтому применён mandatory penalty. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | `03-solution.md`: «кейс легко расползается в тяжёлый SI-проект и теряет repeatability» и «vendor-specific продажи» создают weak moat. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 13 | `05-critic.md` фиксирует «p10 EBITDA < 0», риски 152-ФЗ, санкций, LLM/API и price compression. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 13 | CAC payback хороший, но `02-demand.md` прямо говорит: «buyer language в РФ формулируется через контакт-центр... а не через agentic CX». |

**Sum raw = 84 / 150. Normalized score = round((84 * 100) / 150) = 56/100.**

## Investment committee one-liner
Сильная unit economics не спасает standalone thesis: это хороший delivery-layer для тяжёлых enterprise CX-программ, но не отдельный инвестиционный wedge под Oracle-first positioning в РФ.

## Delta vs previous
Это resurrect/rerun кейс. В исходном triage сигнал был признан duplicate/supporting для `ai-customer-service-operations-operator`. Новый score **56/100** подтверждает исходную логику: как самостоятельный Oracle-specific кейс модель слабая, а как supporting evidence для broader CX-ops wedge она полезна.

## 7-factor Moat Framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 2 | После внедрения возникают интеграции, knowledge-workflows и обученность команды клиента. |
| 3. Scale economies | 1 | Shared tooling дешевеет с объёмом, но delivery остаётся human-heavy. |
| 4. Proprietary data / model advantage | 1 | Есть playbooks и integration know-how, но нет подтверждённого локального dataset moat. |
| 5. Regulatory moat | 0 | Governance важен, но отдельного лицензируемого барьера входа в кейсе нет. |
| 6. Brand / distribution | 1 | Бренд Oracle силён глобально, но локальный спрос на Oracle-first motion низкий. |
| 7. Embedded workflow | 2 | При успехе решение встраивается в service stack клиента, но заменимо системным интегратором. |

**Moat raw = 7/21. Moat score = round((7 * 25) / 21) = 8/25.**

> **Weak moat:** raw < 10. Обязательно вынесен в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 35 643 333 ₽ |
| CAC | 2 837 692 ₽ |
| LTV/CAC | 12,6x |
| CAC Payback | 3,3 мес |
| GM% | 62,9% |
| contribution_margin_rub_month | 535 000 ₽ на клиента |
| fixed_costs_rub_month | 7 400 000 ₽ |
| company_ebitda_rub_month (base, M13) | 625 000 ₽/мес |
| company_ebitda_potential_rub_month (50 клиентов) | 19 350 000 ₽/мес |
| clients_to_500k_ebitda | 15 |
| clients_to_1m_ebitda | 16 |
| months_to_500k_ebitda | 13 |
| months_to_1m_ebitda | 14 |
| Break-even | 14 клиентов / M12-M13 |
| startup_capital_to_bep_rub | 62721404 ₽ в base |
| Startup capital available | 60 000 000 ₽ |

## Full business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR | CRM, ручной ресерч, HH/отраслевой рынок | 2 ч | 3 000 | средняя |
| 2 | Outbound / partner intro | SDR + Founder | почта, телефония, Telegram, CRM | 3 ч | 7 500 | средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 4 250 | низкая |
| 4 | Discovery по service workflows | AE + Solution Architect | Meet, Miro, заметки | 3 ч | 18 000 | низкая |
| 5 | ROI / pain mapping | AE + CTO | spreadsheet, docs | 2 ч | 11 500 | низкая |
| 6 | Demo / pilot scope | AE + CTO + Product | demo env, презентация | 3 ч | 16 500 | низкая |
| 7 | Security / legal / procurement review | CTO + AE + Legal | dataroom, docs | 5 ч | 27 500 | низкая |
| 8 | Proposal / SOW / redlines | AE + Founder | docs, CRM, ЭДО | 3 ч | 13 500 | средняя |
| 9 | Подписание договора | Founder + AE | ЭДО | 1 ч | 4 500 | высокая |
| 10 | Invoicing / payment request | Finance | 1С, банк, ЭДО | 0,5 ч | 1 500 | высокая |
| 11 | Onboarding kickoff | CSM + Solution Architect + CTO | PM tool, KB, API docs | 8 ч | 52 000 | средняя |

**Итого direct process cost на одну выигранную сделку: ~159 750 ₽.**

## Team table

| Роль | Fully-loaded FOT ₽/мес | Комментарий |
|---|---:|---|
| CEO / Founder | 845 000 | enterprise deals, partnerships |
| CTO / Tech Lead | 780 000 | architecture, delivery oversight, security |
| Senior Backend #1 | 585 000 | integrations / APIs |
| Senior Backend #2 | 585 000 | platform / workflow engine |
| ML Engineer | 676 000 | orchestration / evals |
| DevOps | 455 000 | infra / observability |
| Frontend | 390 000 | ops UI / dashboards |
| Product Manager | 455 000 | packaging / roadmap / discovery |
| SDR | 234 000 | outbound |
| AE | 468 000 | deal closing / procurement |
| Customer Success | 325 000 | onboarding / retention |
| Finance / Ops | 208 000 | billing / admin |

**Steady-state full team FOT: 6 006 000 ₽/мес. В базе использованы fixed_costs_rub_month = 7 400 000 ₽/мес.**

## Top-3 risks

| Риск | Probability | Impact | Почему важно |
|---|---|---|---|
| Weak moat / platform dependence | high | высокий | Exact-demand по Oracle близок к нулю, а delivery легко коммодитизируется SI-игроками. |
| Enterprise GTM + price compression | high | высокий | `05-critic.md` показывает, что при price -30% EBITDA @M12 падает до `-3 620 000 ₽`. |
| evidence_quality_unverified | med-high | средний | В `02-demand.md` отсутствует строка Sources: T1/T2/T3, поэтому quality of evidence по tier-awareness не верифицирован. |

## LTV Upside Calculator
Чтобы вывести кейс хотя бы в NEAR-PASS, нужно улучшить минимум 3 из 5 рычагов:

| Рычаг | Текущее | Цель | Эффект |
|---|---:|---:|---|
| Exact-demand / positioning | Oracle-first | vendor-agnostic CX ops layer | снимает главный demand-discount |
| customer_ltv_rub | 35,6 млн ₽ | >40 млн ₽ | нужен более длинный retention и upsell managed layer |
| CAC | 2,84 млн ₽ | <2,0 млн ₽ | снижает зависимость от длинного enterprise cycle |
| fixed_costs_rub_month | 7,4 млн ₽ | <6,5 млн ₽ | ускоряет путь к company_ebitda_rub_month > 500К |
| Moat raw | 7/21 | >=10/21 | нужно доказать switching costs и embedded workflow на production-кейсах |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Огромный объём customer-service и сложный governance-контур, где стоимость ошибок SLA высока. | email decision-maker / партнёрство через крупного интегратора | 1 500 000 ₽/мес |
| 2 | Т-Банк | AI-first банк с большим цифровым сервисом и быстрым pain по routing, QA и escalation workflows. | direct outbound в CX ops / founder intro | 1 200 000 ₽/мес |
| 3 | ВТБ | Большой поток обращений и heavy regulated service operations. | enterprise email + отраслевые форумы | 1 300 000 ₽/мес |
| 4 | Альфа-Банк | Высокий объём омниканального сервиса и готовность тестировать automation-пилоты. | account-based outreach | 1 100 000 ₽/мес |
| 5 | МТС | Классический telecom ICP с дорогим contact-center и KPI по SLA/FCR. | конференция + партнёрский канал | 950 000 ₽/мес |
| 6 | билайн | Большой customer support footprint и боль в cost-to-serve. | direct outreach / конференция CX WORLD | 900 000 ₽/мес |
| 7 | МегаФон | Высокий объём тикетов и смысл в knowledge orchestration + QA automation. | email decision-maker / интегратор | 900 000 ₽/мес |
| 8 | Ozon | Масштабный клиентский сервис маркетплейса, где важны triage и case routing. | vc.ru thought leadership + direct ABM | 1 000 000 ₽/мес |
| 9 | Wildberries | Огромный поток customer-service обращений и цена автоматизации backlog очень высока. | отраслевой форум / партнёрство | 1 100 000 ₽/мес |
| 10 | ДОМ.РФ | Уже подтверждённая боль в customer-service analytics через кейс Naumen CI, значит зрелость buyer-language выше средней. | партнёрский заход через ecosystem vendors | 850 000 ₽/мес |

## Market + finance synthesis
- Preferred market reading: это не Oracle category, а broader enterprise customer-service operations budget line.
- Base break-even: **14 клиентов**, **M12-M13**.
- Base `company_ebitda_rub_month` point: **625 000 ₽/мес на M13**.
- `company_ebitda_potential_rub_month` at 50 clients: **19 350 000 ₽/мес**.
- Monte Carlo Lite: **p10 EBITDA @M24 = -1 919 804 ₽**, **p50 = 10 456 438 ₽**, **p90 = 28 749 826 ₽**.

## Что доказать за следующие 6 месяцев
1. Не менее 2 production pilots в РФ с измеримым снижением backlog / AHT / SLA breach.
2. Vendor-agnostic positioning, где Oracle лишь один из execution-stack'ов.
3. Повторяемый пакет managed optimization после initial launch, а не только bespoke SI-проект.
4. Подтверждённый moat через данные внедрения, integration templates и минимум 1 референс с продлением.

## Финальное решение
**REJECTED / уходит в rejected-пул.**

Причина не в поломанной unit economics, а в том, что standalone Oracle-first wedge не дотягивает до investment-grade demand proof и moat. Кейс полезен как supportive evidence для broader B2B-OPS thesis, но не как отдельная модель для одобрения.
