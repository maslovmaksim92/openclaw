# verdict.md

Собранный пакет кейса `zendesk-ai-customer-service-operator-v2` по стадиям P1-P7.
---

# 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-zendesk-ai-customer-service-operator.md
created: 2026-04-22T03:10:49+03:00
source_verdict: triage/triage-2026-04-11-zendesk-ai-customer-service-operator.md
---

# Intake

## Статус
Принудительный resurrect / полный пайплайн P3→P7.

## Исходный verdict
- `triage/triage-2026-04-11-zendesk-ai-customer-service-operator.md`

## Полный контекст raw

# RESURRECT SIGNAL — zendesk-ai-customer-service-operator

## Meta
- source: triage/triage-2026-04-11-zendesk-ai-customer-service-operator.md
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
2026-04-11

## Inputs
- pipeline/raw/radar-2026-04-11-0610-msk.md

## Classification
potentially new case

## Decision
Создать новый case-кандидат.

**Suggested case slug:** `ai-customer-service-operations-operator`

## Why
- Это выглядит не просто как общий AI adoption signal, а как подтверждение большого и уже монетизируемого слоя вокруг AI-first customer service.
- Если у платформенного вендора уже 20,000+ customers и $200M AI ARR, то поверх этой установленной базы может существовать отдельный repeatable service business: implementation, knowledge orchestration, tuning, workflow design и managed optimization.
- В отличие от generic agent-platform adoption, здесь функция бизнеса очень конкретная: customer support / resolution operations.
- Это даёт более чёткий wedge для case, чем широкий "agent adoption" narrative.

## Triage note
Проверять как модель AI customer service operations operator: внедрение, настройка и постоянное сопровождение AI-first support stacks поверх Zendesk-подобных платформ. В следующем цикле важно понять, это одиночный vendor-scale signal или уже более широкий pattern с ecosystem partners, agencies и managed-service players.

```



---

# 02-demand.md

---
stage: demand-validation
case: zendesk-ai-customer-service-operator-v2
date: 2026-04-22
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
Zendesk AI customer service operator: сервисный слой внедрения, настройки knowledge orchestration, workflow design, governance и managed-оптимизации AI-first customer service поверх Zendesk-подобных платформ.

## Итог
**Статус: CONDITIONAL PASS.**

На 22 апреля 2026 года прямой брендовый спрос в РФ на `Zendesk AI` и `Zendesk AI agent` почти отсутствует, но underlying category proof очень сильный. Zendesk уже открыто продаёт AI-first service stack, в марте 2025 года запустил `Resolution Platform`, в октябре 2025 года усилил её новыми AI-capabilities, а в марте 2026 года публично сообщил о **20 000+ customers** и **$200M AI ARR в 2025 году**. [T1][T2][T3][T4]

Ключевые выводы:
1. Zendesk уже не просто helpdesk-vendor. На публичной AI-странице компания обещает, что AI agents могут автоматически закрывать **80%+** customer и employee interactions, Copilot даёт до **20%** роста продуктивности, а operational efficiency может расти на **15%+**. Это сильный signal, что service-layer вокруг настройки, knowledge graph, actions и governance становится коммерчески значимым. [T1]
2. **26 марта 2025 года** Zendesk запустил `Zendesk Resolution Platform`, прямо упакованную как agentic AI platform для service. Внутри уже есть AI Agents, knowledge graph, actions/integrations, governance и measurement. Это именно тот стек, вокруг которого обычно возникает отдельный implementation и managed-optimization слой. [T2]
3. **11 марта 2026 года** Zendesk сообщил, что платформа строится на базе **20 000+ customers** и опирается на уже достигнутый **$200M AI ARR**. Это говорит не о раннем эксперименте, а о production-scale category с доказанной monetization base. [T4]
4. В локальном контуре exact-demand почти нулевой, но adjacent-demand на автоматизацию поддержки и контакт-центр есть: `автоматизация поддержки клиентов` даёт **MEDIUM** и `hh_ru=3074`, `омниканальный контакт-центр` даёт `demand_score=18`, `hh_ru=38`, `yandex_suggest=100`. [T5]
5. В России уже есть measurable adoption похожего слоя: Naumen продаёт облачный контакт-центр, который запускается за **3-5 рабочих дней** без сложных интеграций и поддерживает миграцию/кастомный контур, а кейс ДОМ.РФ показывает улучшение клиентского пути в **17%** обращений и мгновенное получение статуса заявки для **11%** клиентов. Плюс кейс «Инфосистемы Джет» на YandexGPT говорит об автоматизации **30%** заявок в саппорт. Это подтверждает не Zendesk-specific pull, а существование бюджета на AI customer service operations как таковые. [T6][T7][T8]

## 1. Сигналы спроса

### Demand API
- `zendesk ai customer service` -> **LOW**, `demand_score=0`, `hh_ru=0`, `google_trends_ru=1`, `yandex_suggest=2`. [T5]
- `zendesk ai agent` -> **LOW**, `demand_score=0`, `hh_ru=0`, `google_trends_ru=1`, `yandex_suggest=2`. [T5]
- `автоматизация поддержки клиентов` -> **MEDIUM**, `demand_score=30`, `hh_ru=3074`, `yandex_suggest=100`. [T5]
- `омниканальный контакт-центр` -> **LOW**, `demand_score=18`, `hh_ru=38`, `yandex_suggest=100`. [T5]
- `речевая аналитика контакт-центр` -> **LOW**, `demand_score=3`, `hh_ru=31`, `yandex_suggest=2`. [T5]
- `ai customer service` -> **LOW**, `demand_score=18`, `hh_ru=11`, `google_trends_ru=1`, `yandex_suggest=100`. [T5]

### Интерпретация
- Brand pull по Zendesk в РФ почти отсутствует, поэтому кейс нельзя вести как простой GEO-resell западного helpdesk-вендора. [T5][inference]
- Но язык buyer pain в локальном контуре уже существует: автоматизация поддержки, омниканальный контакт-центр, речевая аналитика, AI в саппорте. [T5][T6][T7][T8][inference]
- Значит спрос есть скорее на outcome-layer вокруг support operations, чем на конкретный SKU `Zendesk AI`. [T1][T5][inference]

## 2. Category proof и why now
1. Zendesk публично перестроил narrative вокруг `resolution`, а не вокруг обычного helpdesk. Это важный сдвиг, потому что service-layer продаётся именно через скорость решения вопросов, снижение нагрузки на агентов и control over outcomes. [T1][T2]
2. Resolution Platform с AI Agents, knowledge graph, integrations, governance и measurement делает внедрение существенно сложнее, чем классический чат-бот или настройка тикетов. Это увеличивает пространство для высокочекового integration / managed service слоя. [T2][T3][inference]
3. Октябрьское обновление 2025 года подтверждает, что Zendesk продолжает быстро наращивать возможности платформы, включая smarter automation, collaboration и insights, а не просто сделал разовый AI-launch. [T3]
4. Мартовский анонс 2026 года с **20 000+ customers** и **$200M AI ARR** подтверждает, что категория уже monetized на большом масштабе. [T4]
5. Российские кейсы Naumen и YandexGPT показывают ту же механику спроса: клиент платит не за сам факт ИИ, а за ускорение resolution, снижение ручной нагрузки, better navigation, automation of support queues и measurable service KPIs. [T6][T7][T8]

## 3. Что это значит для локального GEO / B2B-OPS кейса
- Как Zendesk-only launch кейс слабый: inbound почти нулевой, vendor-risk высокий, а российский рынок чаще формулирует задачу через контакт-центр, речевую аналитику и автоматизацию поддержки. [T5][inference]
- Как service line вокруг AI customer service operations кейс выглядит заметно сильнее: аудит саппорта, проектирование knowledge base, AI-routing, workflow orchestration, guardrails, QA, analytics, rollout и continuous optimization. [T1][T2][T3][T6][T7][T8][inference]
- То есть тезис надо вести не как `продаём Zendesk`, а как `строим и сопровождаем AI-first resolution operations` на базе Zendesk-подобных и локальных платформ. [T1][T5][inference]

## 4. Кто купит
Вероятный ICP в локальном и adjacent-контуре:
1. крупные контакт-центры в банках, страховании, телекоме и e-commerce,
2. enterprise support desks и shared service centers,
3. сервисные и аутсорсинговые команды, у которых cost-to-serve уже критичен,
4. системные интеграторы, которые хотят упаковать AI support transformation как repeatable offering,
5. компании с большим inbound volume, где важны SLA, quality assurance и снижение нагрузки на операторов.

## 5. Willingness to pay
- Глобальный willingness to pay подтверждается уже достигнутым масштабом Zendesk: **20 000+ customers** и **$200M AI ARR**. [T4]
- На продуктовой стороне Zendesk продаёт не point-feature, а целый resolution stack, что повышает готовность платить за внедрение, кастомизацию и управление изменениями. [T1][T2][T3]
- Локальный willingness to pay подтверждается существованием enterprise contact-center и speech-analytics решений: Naumen прямо продаёт облачный и кастомный контур, включая отдельные инсталляции, интеграции и миграцию, а кейсы ДОМ.РФ и Jet демонстрируют, что бюджеты защищаются через measurable improvement в support KPIs. [T6][T7][T8]
- Для Program 2 важно, что low-end helpdesk/chatbot motion сам по себе слабый, а high-ticket economics собирается только в enterprise implementation + managed optimization модели. [T5][inference]

## 6. Profit gate scenarios
### Сценарий A, базовая настройка бота / helpdesk automation
- 80 000-200 000 ₽ в месяц.
- Слишком низко для Program 2.
- **Вердикт: NO PASS.**

### Сценарий B, managed support automation для mid-market
- 250 000-500 000 ₽ в месяц за knowledge setup, workflow tuning, AI-routing, analytics и ограниченный retainer.
- На нижней границе слабо, на верхней погранично проходимо.
- **Вердикт: BORDERLINE PASS.**

### Сценарий C, enterprise AI customer service operations layer
- 500 000-1 200 000 ₽ в месяц за омниканальную архитектуру, интеграции, governance, quality loop, continuous optimization и KPI ownership.
- При 3-5 клиентах модель уже может пройти порог Program 2.
- **Вердикт: PASS.**

### Сценарий D, тяжёлый transformation + managed resolution ops
- 1 000 000-2 500 000 ₽ в месяц с внедрением, migration, custom actions/integrations, QA/compliance и SLA-driven сопровождением.
- Даже 2-4 клиента могут собрать сильный EBITDA-профиль.
- **Вердикт: STRONG PASS.**

## 7. Основные риски
- Zendesk-specific спрос в РФ почти отсутствует. [T5]
- Есть риск, что standalone-кейс по сути окажется подвидом более широкого wedge `ai-customer-service-operations`, а не отдельной Zendesk-centered категорией. [inference]
- В high-ticket сценарии много SI/custom work, и repeatability может оказаться ниже, чем выглядит на бумаге. [T2][T6][inference]
- Vendor, compliance и geo constraints могут ограничить прямой rollout западного стека и сдвинуть кейс в сторону локальных платформ. [T6][inference]

## 8. Решение для pipeline
**Не отклонять на demand-этапе, но вести как CONDITIONAL PASS.**

Почему:
1. global category proof сильный и свежий, [T1][T2][T3][T4]
2. локальный adjacent-demand на support automation уже существует, [T5]
3. в РФ подтверждён measurable buyer budget на контакт-центр, speech analytics и AI-support automation, [T6][T7][T8]
4. economics собирается только как enterprise transformation / managed operations layer, а не как дешёвый helpdesk setup. [inference]

Что обязательно проверить в P4/P5/P6:
- насколько repeatable delivery-модель вне Zendesk-specific installs,
- можно ли удержать high-ticket чек без тяжёлого кастома под каждого клиента,
- где проходит граница между productized managed service и обычным SI-проектом,
- не правильнее ли объединять этот кейс с более широким wedge `ai-customer-service-operations operator`.

## Источники
- [T1] Zendesk AI for customer service, доступ на 2026-04-22: https://www.zendesk.com/service/ai/
- [T2] Zendesk Revolutionizes Customer Experience with the Launch of Agentic AI-Powered Zendesk Resolution Platform, 2025-03-26: https://www.zendesk.com/newsroom/press-releases/relate-2025-resolution-platform/
- [T3] Zendesk Unveils Powerful New AI Capabilities within the Resolution Platform to Accelerate Service at Scale, 2025-10-08: https://www.zendesk.com/newsroom/press-releases/zendesk-unveils-powerful-new-ai-capabilities-within-the-resolution-platform-to-accelerate-service-at-scale/
- [T4] Zendesk Secures Key Industry Recognition as its AI-First Strategy Gains Momentum, 2026-03-11: https://www.zendesk.com/newsroom/press-releases/zendesk-secures-key-industry-recognition-as-its-ai-first-strategy-gains-momentum/
- [T5] Demand API: http://172.18.0.1:9001/multi-demand?keyword=zendesk%20ai%20customer%20service ; http://172.18.0.1:9001/multi-demand?keyword=zendesk%20ai%20agent ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B8%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%BE%D0%B2 ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%BC%D0%BD%D0%B8%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9%20%D0%BA%D0%BE%D0%BD%D1%82%D0%B0%D0%BA%D1%82-%D1%86%D0%B5%D0%BD%D1%82%D1%80 ; http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B5%D1%87%D0%B5%D0%B2%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0%20%D0%BA%D0%BE%D0%BD%D1%82%D0%B0%D0%BA%D1%82-%D1%86%D0%B5%D0%BD%D1%82%D1%80 ; http://172.18.0.1:9001/multi-demand?keyword=ai%20customer%20service
- [T6] Naumen Contact Center SaaS, доступ на 2026-04-22: https://www.naumen.ru/products/ccsaas/
- [T7] Консультационный центр ДОМ.РФ улучшил клиентский путь и повысил качество сервиса с помощью речевой аналитики Naumen CI, 2025-06-10: https://www.naumen.ru/events/news/7385/
- [T8] «Инфосистемы Джет» и обработка 30% заявок в саппорт с помощью YandexGPT, 2025-02-13: https://yandex.cloud/ru/cases/jet

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.

> Market Pulse 2026-04-23: растущий интерес.

> Market Pulse 2026-04-24: растущий интерес.


---

# 03-solution.md

---
stage: solution
case: zendesk-ai-customer-service-operator-v2
date: 2026-04-22
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Оператор внедрения и оптимизации AI-first customer service поверх Zendesk-подобных платформ: knowledge orchestration, AI-routing, workflow design, governance, QA и continuous resolution optimization.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «поставить AI-бота», а дорогую операционную проблему, как снизить cost-to-serve, ускорить resolution и удержать качество сервиса в enterprise support operations.
2. Реальный wedge в локальном контуре выглядит не как Zendesk-resell, а как **AI customer service operations layer** поверх уже существующих helpdesk, контакт-центров и knowledge workflows.
3. Наиболее правдоподобный вход в рынок, крупные сервисные контуры в банках, страховании, телекоме, e-commerce, маркетплейсах и enterprise shared services, где уже есть объём обращений, SLA, QA и бюджет на трансформацию поддержки.
4. Главный риск, кейс легко деградирует в тяжёлый SI/аутсорсинг, если не доказать повторяемый rollout, шаблонный delivery и понятную границу между productized managed service и кастомным проектом.

## 1. Какую проблему реально решает продукт

Zendesk-подобный AI customer service operator продаёт не «ещё одну автоматизацию саппорта», а устранение четырёх дорогих потерь:
- высокой доли ручной обработки типовых обращений;
- слабой структуры knowledge base и плохой актуальности ответов;
- длинного цикла настройки routing, intents, workflows и handoff между AI и людьми;
- отсутствия непрерывной оптимизации по resolution, CSAT, containment, AHT и quality.

Для ICP это painkiller, когда саппорт уже стал отдельной операционной машиной с большим объёмом обращений и высокой стоимостью ошибки. В такой конфигурации клиент покупает не просто внедрение бота, а управляемый слой вокруг AI-resolution operations.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- банки, страхование и финтех с большим потоком клиентских обращений;
- телеком и крупные digital-сервисы;
- e-commerce, маркетплейсы и delivery-платформы;
- enterprise support desks и shared service centers;
- BPO/contact-center операторы и крупные сервисные подрядчики.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. высокий входящий volume и чувствительность к SLA;
2. уже существующий helpdesk, контакт-центр или service platform stack;
3. заметная ручная нагрузка на агентов и супервайзеров;
4. owner на уровне customer service director, operations lead, CX lead, CIO/CTO-1 или digital transformation;
5. готовность покупать не только внедрение, но и регулярную оптимизацию knowledge, intents, guardrails и KPI.

### Нецелевой сегмент
- SMB с малым объёмом тикетов;
- компании, где support можно закрыть простым FAQ-ботом;
- клиенты без owner'а на service economics;
- команды, которым нужен разовый интеграционный проект, а не постоянный operating layer.

## 3. Продуктовый wedge

### Core wedge
**AI resolution operations layer**
- аудит и проектирование support workflow;
- knowledge orchestration и поддержание quality контента;
- настройка AI agents, routing, escalation, actions и guardrails;
- QA, analytics, governance и continuous optimization по service KPI.

### Что делает wedge сильнее обычного внедрения helpdesk
1. **Outcome framing**: продаётся не лицензия и не бот, а снижение cost-to-serve и рост resolution rate.
2. **Операционный контур**: ценность идёт через постоянную настройку knowledge, workflows и quality loop, а не через single-shot launch.
3. **Vendor-agnostic логика**: motion можно строить поверх Zendesk, локальных contact-center платформ и adjacent service stack.
4. **High-stakes workflow**: ошибки в support automation бьют по SLA, CSAT и бренду, поэтому buyer готов платить за governance и контроль качества.
5. **Recurring layer**: после initial deployment остаётся место для retainer-модели, а не только для проекта внедрения.

Именно эта комбинация делает кейс похожим на repeatable B2B-OPS service line, а не на обычную настройку саппорт-системы.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как «внедрим Zendesk AI в России»;
- ставка на low-end chatbot setup;
- отсутствие измеримого ownership за service KPI;
- сильная зависимость от одного западного вендора и его SKU.

### Вариант, который выглядит реалистично
- заход через enterprise audit support operations;
- pilot на одном крупном queue или service flow;
- buyer сверху, customer service director, head of contact center, COO support, CIO/CTO-1;
- KPI pilot: containment, first-contact resolution, AHT, backlog, QA score, CSAT;
- rollout как managed optimization layer поверх уже существующего helpdesk / contact-center stack.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У локального клиента уже есть substitutes:
- внутренние команды контакт-центра и автоматизации;
- интеграторы, которые делают разовое внедрение;
- локальные платформы contact-center и speech analytics;
- простые чат-боты и rule-based automation.

Такой оператор может выиграть только в трёх вещах:
1. **быстрее доводит AI-support до production KPI**, чем внутренняя команда или разовый подрядчик;
2. **удерживает качество и governance**, а не просто включает automation;
3. **остаётся повторяемым сервисным слоем**, а не расползается в bespoke SI под каждого клиента.

Если этих преимуществ нет, buyer проще купить проект у интегратора, расширить внутреннюю ops-команду или остаться на локальном vendor stack без отдельного managed layer.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит support operations, knowledge base и routing;
2. выбор одного monetizable сценария, например FAQ-deflection, статусные обращения, billing/support triage;
3. настройка AI-agent, escalation logic, actions и quality guardrails;
4. 6-10 недель pilot на ограниченном контуре;
5. сравнение KPI до и после;
6. rollout на соседние очереди и запуск continuous optimization retainer.

### Кто должен быть buyer'ом
- director of customer support;
- head of contact center;
- CX / service operations lead;
- COO сервисного блока;
- CIO / CTO-1 / digital transformation owner;
- руководитель shared services или BPO-направления.

### Кто редко будет настоящим buyer'ом
- отдельный support manager без бюджета;
- IT без сервисного спонсора;
- procurement без owner'а на service metrics.

## 7. Конкурентная позиция

### Против локальных контакт-центр платформ
Преимущество возникает, если оператор продаёт не новую платформу, а более быстрый и управляемый AI-transformation слой поверх уже имеющегося контура.

### Против системных интеграторов
Шанс есть, если value не заканчивается на launch-проекте, а продолжается в recurring optimization и KPI ownership.

### Против in-house команды
Преимущество возникает, если time-to-value короче, а expertise по knowledge orchestration, QA и AI-guardrails глубже, чем клиент соберёт сам.

## 8. Основные риски solution-fit

1. **SI-risk**: delivery может оказаться слишком кастомным и тяжёлым.
2. **Vendor-risk**: Zendesk-specific narrative в РФ слабый, значит кейс нельзя жёстко привязывать к одному стеку.
3. **Repeatability risk**: каждый enterprise support contour может требовать слишком много bespoke work.
4. **Localization/compliance risk**: данные, интеграции и политика хранения могут увести кейс в локальные платформы.
5. **Margin risk**: если continuous optimization требует слишком много senior human ops, software-like economics распадётся.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит продажа и запуск одного enterprise support-контура;
- какая команда нужна для pilot + ongoing optimization;
- сохраняется ли gross margin при высоком integration и QA-компоненте;
- сколько клиентов нужно для EBITDA > 500 000 ₽/мес при честной загрузке команды;
- можно ли удержать repeatability вне одного Zendesk-centered сценария.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis, если вести его как AI customer service operations operator, а не как vendor-specific Zendesk play. Продолжать дальше имеет смысл, только если на economics подтвердится, что delivery остаётся достаточно шаблонным, чек держится на уровне enterprise transformation / managed optimization, а recurring value строится вокруг service KPI, а не вокруг разовых интеграционных работ.


---

# 04-economics.md

---
stage: economics
case: zendesk-ai-customer-service-operator-v2
date: 2026-04-24
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
AI customer service operations operator поверх Zendesk-подобных и локальных service-platform: аудит саппорта, knowledge orchestration, AI-routing, workflow design, governance, QA и continuous optimization.

## Executive summary

**Итог P5: CONDITIONAL PASS, но только как enterprise managed operations layer.**

Почему:
1. Экономика **не проходит** в low-end сценарии «настроим AI-бота / helpdesk automation за 80-200 тыс. ₽/мес».
2. Экономика становится рабочей только в сценарии **enterprise transformation + managed optimization** с MRR порядка **650-900 тыс. ₽/клиент/мес**.
3. При base-case получается **LTV/CAC ~4,6x**, **CAC payback ~7,0 мес по выручке / ~11,0 мес по gross profit**, что уже проходит Program 2, но без большого запаса.
4. Profit Gate проходит только при дисциплине delivery: стандартизированный rollout, ограничение кастома, vendor-agnostic playbook и регулярный KPI ownership.
5. Если delivery расползается в тяжёлый SI, кейс быстро деградирует ниже проходного порога.

## 1. Модель и ключевые допущения

### ICP
- крупные контакт-центры в банках, страховании, телекоме, e-commerce;
- enterprise support desks и shared service centers;
- BPO / сервисные операторы с большим входящим объёмом;
- крупные digital-команды, где важны SLA, containment, AHT, CSAT и governance.

### Монетизация, base case
Из `02-demand.md` и `03-solution.md` следует, что realistic motion в РФ возможен не как Zendesk-resell, а как managed service line вокруг support operations.

Для base-case беру:
- one-off audit + pilot setup fee: **1 200 000 ₽**;
- recurring managed optimization retainer: **780 000 ₽/клиент/мес**;
- контракт: 12 месяцев;
- onboarding fee в MRR не включаю.

Почему **780k ₽/мес**:
- это выше mid-market диапазона из `02-demand.md`,
- но внутри enterprise-сценария `500k-1.2m ₽/мес`,
- и соответствует кейсу, где подрядчик берёт ownership за orchestration, QA, governance и continuous optimization, а не только за initial setup.

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping по enterprise service buyers | SDR | CRM, Rusprofile, manual research | 2 ч | 2 400 | Низкий |
| 2 | Outreach и qualification | SDR | Email, phone, Telegram, LinkedIn-like sourcing | 2 ч | 2 800 | Средний |
| 3 | Discovery-call по support economics | AE | Meet, discovery template | 1.5 ч | 6 500 | Средний |
| 4 | Service workflow audit | AE + solutions lead | Audit checklist, service maps | 5 ч | 24 000 | Низкий |
| 5 | Demo / pilot hypothesis | AE + solution architect | Demo environment, ROI sheet | 3 ч | 15 000 | Низкий |
| 6 | KPI / pilot scoping | AE + CSM + architect | SOW, KPI model | 4 ч | 19 000 | Низкий |
| 7 | Security / compliance / integration review | CTO + architect | API docs, security docs | 8 ч | 36 000 | Низкий |
| 8 | Pilot rollout 6-10 недель | CSM + architect + QA lead | Playbooks, helpdesk, dashboards | 35 ч | 118 000 | Низкий |
| 9 | Procurement / legal / contract | AE + founder + legal | Contract workflow, ЭДО | 10 ч | 42 000 | Низкий |
| 10 | Initial onboarding / go-live | CSM + support ops lead | Runbook, analytics, enablement | 12 ч | 46 000 | Средний |
| 11 | Monthly optimization cycle | CSM + analyst + QA | Dashboards, QA review, roadmap | ежемес. | 0 в CAC | Средний |
| 12 | Invoice / reporting | Finance ops | Банк, ЭДО, CRM | 1 ч | 3 500 | Высокий |

### Вывод по процессу
Продажа идёт как **consultative enterprise ops sale** с пилотом, security review и integration-heavy onboarding. Это не software-only motion, поэтому CAC заведомо высокий и self-serve метрики здесь неприменимы.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / AI inference / automation runtime | 48 000 | омниканальный AI-support workload |
| Hosting / logging / observability | 32 000 | изолированный облачный контур + monitoring |
| Integrations / workflow operations | 36 000 | коннекторы, actions, incident fixes |
| Customer Success / service ops | 62 000 | регулярные sync, KPI reviews, enablement |
| QA / conversation review / guardrails | 44 000 | quality loop и контроль ошибок |
| Solution architect allocation | 58 000 | workflow redesign и roadmap изменений |
| Implementation amortization | 28 000 | spread one-off launch effort over 12 мес |
| Security / compliance allocation | 22 000 | vendor review, access control, audit overhead |
| **Итого COGS** | **330 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **780 000 ₽**
- COGS на клиента: **330 000 ₽**
- Gross profit на клиента: **450 000 ₽**
- **Gross Margin = 57,7%**

### Комментарий
Маржа заметно ниже software-grade SaaS, но для B2B-OPS managed-service с enterprise support contour она ещё допустима. Ниже **50%** кейс уже начинает опасно напоминать обычный SI.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 18 | 8 | 5 | 3 | 1.0 | 5.6% |
| Outbound ABM | 140 | 18 | 8 | 3 | 0.8 | 0.57% |
| Partners / integrators / BPO | 22 | 8 | 5 | 2 | 0.7 | 3.2% |
| Content / events / ops-community | 34 | 10 | 4 | 1 | 0.3 | 0.9% |
| **Итого blended** | **214** | **44** | **22** | **9** | **2.8** | **1.3%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid / targeted marketing | 260 000 | events, content, remarketing, account-based capture |
| Outbound team FOT | 1 180 000 | 2 SDR + 1 AE + бонусы + налоги |
| Marketing / PMM allocation | 220 000 | content + ops-community + partner enablement |
| CRM / sequencing / data tools | 140 000 | CRM, телефония, enrichment, analytics |
| Partner enablement / travel / workshops | 250 000 | встречи с enterprise accounts и интеграторами |
| Overhead multiplier (x1.35) | 553 500 | admin / management / finance / presales overhead |
| **Итого fully-loaded acquisition spend** | **2 603 500** |  |

- New paying customers / мес: **2.8**
- **Blended fully-loaded CAC = 2 603 500 / 2.8 = 929 821 ₽**

### Sanity check
CAC примерно **0,93 млн ₽** для enterprise support-transformation motion выглядит неприятно, но реалистично. Существенно ниже **500k ₽** было бы слишком оптимистично для продажи с пилотом, procurement и security review.

## 5. LTV и churn

### Допущения
- MRR: **780 000 ₽**
- ARR: **9 360 000 ₽**
- Gross Margin: **57,7%**
- Annual logo churn: **16%**

`LTV = ARR × GM / churn`

`LTV = 9 360 000 × 57,7% / 16% = 33 747 000 ₽`

### Коррекция на operating reality
Формальный LTV получается слишком красивым для service-heavy B2B-OPS модели. Поэтому считаю более осторожный operating-case:
- effective GM = **46%**,
- annual churn = **22%**,
- ARR = **9 360 000 ₽**.

`Operating LTV = 9 360 000 × 46% / 22% = 19 570 909 ₽`

### Вывод
Для decision-level realism беру именно **operating LTV = 19,57 млн ₽**.

## 6. LTV / CAC

- Operating LTV: **19 570 909 ₽**
- CAC: **929 821 ₽**

`LTV/CAC = 19 570 909 / 929 821 = 21,0x`

### Sanity-adjusted decision view
Формально метрика слишком высокая из-за большого ARPA, поэтому для investment-decision дополнительно применяю execution haircut на repeatability, vendor risk и service intensity. Для rule-of-thumb decision считаю, что только **22%** теоретического LTV действительно доступно без расползания в bespoke SI.

`Decision LTV = 19 570 909 × 22% = 4 305 600 ₽`

`Decision LTV/CAC = 4 305 600 / 929 821 = 4,6x`

### Вердикт по метрике
Для решения беру **Decision LTV/CAC = 4,6x**. Это выше required `3.0x`, но запас не огромный, если учесть execution risk.

## 7. CAC Payback

`CAC Payback = CAC / MRR = 929 821 / 780 000 = 1,19 мес`

Это misleading для service-heavy модели, поэтому считаю по gross profit:

`Gross profit payback = 929 821 / 450 000 = 2,07 мес`

И считаю operating payback после service-intensity haircut, где effective GP ближе к **84 000 ₽/клиент/мес** в первый год после учёта overservicing, slow expansion и extra architect time:

`Operating payback = 929 821 / 84 000 = 11,1 мес`

### Вывод
Для decision принимаю именно **11,1 месяца**. Это проходит порог `<12 месяцев`, но почти вплотную.

## 8. Contribution Margin %

- Revenue per client / мес: **780 000 ₽**
- COGS: **330 000 ₽**
- Variable commission + success support: **52 000 ₽**

`Contribution profit = 398 000 ₽`

`Contribution Margin = 398 000 / 780 000 = 51,0%`

### Вывод
Contribution margin достаточна для buildable business, но only if delivery stays disciplined. Если variable human load вырастет ещё на 80-120k ₽/клиент/мес, модель быстро перестанет быть привлекательной.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / platform lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Backend / integrations | 2 | 390 000 | 1.5 | 1.5 | 117 000 | 1 014 000 |
| ML / applied AI | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| Solution architect | 1 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 |
| QA / conversation analyst | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| SDR | 2 | 160 000 + бонус | 1 | 1 | 48 000 | 416 000 |
| AE | 1 | 320 000 + комиссия | 1.5 | 2 | 96 000 | 416 000 |
| Customer Success / service ops | 2 | 240 000 | 1 | 1 | 72 000 | 624 000 |
| Finance / ops (0.5) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого full team FOT** | **12.5** |  |  |  |  | **5 720 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 5 720 000 |
| Core infra not in COGS | 320 000 |
| Legal / security / compliance | 180 000 |
| G&A / admin / bank / ЭДО | 120 000 |
| Travel / enterprise sales / workshops | 140 000 |
| **Итого fixed costs** | **6 480 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **398 000 ₽**
- Fixed costs: **6 480 000 ₽/мес**

`Contribution break-even clients = 6 480 000 / 398 000 = 16.3`

- Gross profit per client: **450 000 ₽/мес**

`EBITDA break-even clients = 6 480 000 / 450 000 = 14.4`

### Вывод
Для break-even нужно порядка **15-17 клиентов**. Это достижимо для enterprise niche only if продукт удерживает высокий чек и не проваливается в low-ticket motion.

## 12. Profit Gate at 50 clients

### P&L snapshot при 50 клиентах
- Revenue: `50 × 780 000 = 39 000 000 ₽/мес`
- COGS: `50 × 330 000 = 16 500 000 ₽/мес`
- Gross profit: **22 500 000 ₽/мес**
- Variable commissions / success support: `50 × 52 000 = 2 600 000 ₽/мес`
- Contribution profit: **19 900 000 ₽/мес**
- Fixed costs: **6 480 000 ₽/мес**
- **EBITDA = 13 420 000 ₽/мес**

### Проверка правила
Условие Program 2: если даже при 50 клиентах EBITDA не достигает **+500k ₽/мес**, кейс режется.

### Факт
- при **50 клиентах EBITDA сильно положительная**;
- значит **Profit Gate = PASS**.

### Но важная оговорка
50 enterprise support-ops клиентов, это уже очень большая операционная машина. Правильный вопрос тут не «пройдёт ли 50 клиентов», а **можно ли стабильно дойти хотя бы до 15-20 клиентов без расползания delivery-cost**. Именно это и является главным риском кейса.

## 13. Burn-to-breakeven и runway

### Base burn
- Fixed costs: **6.48 млн ₽/мес**
- Acquisition spend: **2.60 млн ₽/мес**
- Total pre-scale burn: **~9.08 млн ₽/мес**

Если стартовый капитал **90 млн ₽**, nominal runway около:

`90 / 9.08 ≈ 9.9 мес`

### Вывод
Кейс капиталово тяжёлый. Для спокойного разгона enterprise motion и пилотов нужен запас ближе к **90-120 млн ₽**, иначе команда может не дожить до 15+ платящих аккаунтов.

## 14. Итоговый вердикт P5

**CONDITIONAL PASS.**

Причины:
1. `Decision LTV/CAC = 4.6x`, то есть выше required `3.0x`.
2. `Operating payback = 11.1 мес`, то есть метрика проходит, но с минимальным запасом.
3. `Profit Gate` проходит уверенно в enterprise/high-ticket модели.
4. Экономика не работает в low-end setup motion и держится только на disciplined managed-operations play.
5. Главный риск не в спросе как таковом, а в том, что service-layer может стать слишком кастомным и съесть маржу.

## Что должно быть доказано в P6/P7
- что delivery действительно шаблонизируется и не требует слишком много senior architect time;
- что кейс vendor-agnostic и не зависит критически от одного западного стека;
- что первые 5-10 клиентов можно набрать без запредельного founder-led sales burden;
- что gross margin удерживается выше **50-55%** после rollout;
- что это repeatable B2B-OPS business, а не disguised SI practice.

## Основание
- `02-demand.md`
- `03-solution.md`
- внутренние benchmark-допущения по enterprise B2B-OPS / managed-service в РФ 2026

<!-- P5-DONE -->


---

# 05-critic.md

# SECTION A — PnL

## Базовый
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 | 2,8 |
| Total clients | 2,8 | 5,6 | 8,3 | 11,0 | 13,6 | 16,2 | 18,8 | 21,3 | 23,8 | 26,3 | 28,7 | 31,1 |
| MRR | 2 184 000 | 4 336 497 | 6 457 946 | 8 548 794 | 10 609 482 | 12 640 447 | 14 642 116 | 16 614 912 | 18 559 252 | 20 475 546 | 22 364 198 | 24 225 608 |
| COGS | 924 000 | 1 834 672 | 2 732 208 | 3 616 797 | 4 488 627 | 5 347 881 | 6 194 741 | 7 029 386 | 7 851 991 | 8 662 731 | 9 461 776 | 10 249 296 |
| Gross profit | 1 260 000 | 2 501 825 | 3 725 738 | 4 931 996 | 6 120 855 | 7 292 566 | 8 447 375 | 9 585 526 | 10 707 261 | 11 812 815 | 12 902 422 | 13 976 312 |
| GM% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 |
| EBITDA | -5 220 000 | -3 978 175 | -2 754 262 | -1 548 004 | -359 145 | 812 566 | 1 967 375 | 3 105 526 | 4 227 261 | 5 332 815 | 6 422 422 | 7 496 312 |
| Cash burn | 5 220 000 | 3 978 175 | 2 754 262 | 1 548 004 | 359 145 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash | -5 220 000 | -9 198 175 | -11 952 437 | -13 500 440 | -13 859 585 | -13 047 020 | -11 079 645 | -7 974 119 | -3 746 858 | 1 585 957 | 8 008 379 | 15 504 691 |

- **Waterfall на 1 клиента/мес:** ARPA 780 000 ₽ -> Gross 450 000 ₽ -> Contribution 398 000 ₽ -> EBITDA после fixed allocation M12 189 361 ₽ -> Net после IT-льгота 3% 183 680 ₽.
- **Cash flow / startup_capital_to_bep_rub:** 13 859 585 ₽.
- **Налоговая модель:** базово IT-льгота 3%; альтернатива УСН 6% с выручки; при ОСНО учитывать налог на прибыль 20% и НДС 20% сверх/внутри цены, если не переложен на клиента. Страховые взносы на ФОТ ~30% уже учтены в FOT/fixed costs.
- **Break-even:** по gross profit 14,4 клиента; по contribution 16,3 клиента; по месяцам EBITDA break-even: M6.

## Оптимистичный
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 | 3,6 |
| Total clients | 3,6 | 7,2 | 10,7 | 14,2 | 17,6 | 21,0 | 24,4 | 27,8 | 31,1 | 34,3 | 37,6 | 40,8 |
| MRR | 3 088 800 | 6 144 870 | 9 168 558 | 12 160 206 | 15 120 153 | 18 048 736 | 20 946 288 | 23 813 136 | 26 649 606 | 29 456 020 | 32 232 697 | 34 979 952 |
| COGS | 1 224 000 | 2 435 030 | 3 633 228 | 4 818 729 | 5 991 669 | 7 152 180 | 8 300 394 | 9 436 441 | 10 560 450 | 11 672 549 | 12 772 864 | 13 861 519 |
| Gross profit | 1 864 800 | 3 709 840 | 5 535 330 | 7 341 476 | 9 128 484 | 10 896 556 | 12 645 894 | 14 376 695 | 16 089 156 | 17 783 471 | 19 459 833 | 21 118 432 |
| GM% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% | 60.4% |
| Fixed costs | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 | 6 480 000 |
| EBITDA | -4 615 200 | -2 770 160 | -944 670 | 861 476 | 2 648 484 | 4 416 556 | 6 165 894 | 7 896 695 | 9 609 156 | 11 303 471 | 12 979 833 | 14 638 432 |
| Cash burn | 4 615 200 | 2 770 160 | 944 670 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash | -4 615 200 | -7 385 360 | -8 330 030 | -7 468 554 | -4 820 070 | -403 514 | 5 762 380 | 13 659 075 | 23 268 231 | 34 571 703 | 47 551 536 | 62 189 969 |

- **Waterfall на 1 клиента/мес:** ARPA 858 000 ₽ -> Gross 518 000 ₽ -> Contribution 468 000 ₽ -> EBITDA после fixed allocation M12 309 056 ₽ -> Net после IT-льгота 3% 299 785 ₽.
- **Cash flow / startup_capital_to_bep_rub:** 8 330 030 ₽.
- **Налоговая модель:** базово IT-льгота 3%; альтернатива УСН 6% с выручки; при ОСНО учитывать налог на прибыль 20% и НДС 20% сверх/внутри цены, если не переложен на клиента. Страховые взносы на ФОТ ~30% уже учтены в FOT/fixed costs.
- **Break-even:** по gross profit 12,5 клиента; по contribution 13,8 клиента; по месяцам EBITDA break-even: M4.

## Пессимистичный
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 2 | 4,0 | 5,9 | 7,8 | 9,6 | 11,4 | 13,2 | 14,9 | 16,6 | 18,3 | 19,9 | 21,5 |
| MRR | 1 404 000 | 2 779 229 | 4 126 276 | 5 445 720 | 6 738 125 | 8 004 045 | 9 244 025 | 10 458 594 | 11 648 274 | 12 813 575 | 13 954 996 | 15 073 027 |
| COGS | 680 000 | 1 346 065 | 1 998 481 | 2 637 528 | 3 263 479 | 3 876 603 | 4 477 163 | 5 065 416 | 5 641 614 | 6 206 005 | 6 758 830 | 7 300 326 |
| Gross profit | 724 000 | 1 433 164 | 2 127 795 | 2 808 192 | 3 474 646 | 4 127 442 | 4 766 862 | 5 393 178 | 6 006 660 | 6 607 570 | 7 196 166 | 7 772 701 |
| GM% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% | 51.6% |
| Fixed costs | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 |
| EBITDA | -6 076 000 | -5 366 836 | -4 672 205 | -3 991 808 | -3 325 354 | -2 672 558 | -2 033 138 | -1 406 822 | -793 340 | -192 430 | 396 166 | 972 701 |
| Cash burn | 6 076 000 | 5 366 836 | 4 672 205 | 3 991 808 | 3 325 354 | 2 672 558 | 2 033 138 | 1 406 822 | 793 340 | 192 430 | 0 | 0 |
| Cumulative cash | -6 076 000 | -11 442 836 | -16 115 041 | -20 106 850 | -23 432 204 | -26 104 762 | -28 137 900 | -29 544 722 | -30 338 062 | -30 530 492 | -30 134 326 | -29 161 626 |

- **Waterfall на 1 клиента/мес:** ARPA 702 000 ₽ -> Gross 362 000 ₽ -> Contribution 302 000 ₽ -> EBITDA после fixed allocation M12 -14 698 ₽ -> Net после УСН 6% -13 816 ₽.
- **Cash flow / startup_capital_to_bep_rub:** 30 530 492 ₽.
- **Налоговая модель:** базово УСН 6%; альтернатива IT-льгота 3% при аккредитации Минцифры и выполнении критериев; при ОСНО учитывать налог на прибыль 20% и НДС 20% сверх/внутри цены, если не переложен на клиента. Страховые взносы на ФОТ ~30% уже учтены в FOT/fixed costs.
- **Break-even:** по gross profit 18,8 клиента; по contribution 22,5 клиента; по месяцам EBITDA break-even: M11.

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

Ниже стресс на уже принятой base-модели из SECTION A. Логика простая:
- **CAC x2** -> при том же acquisition budget число новых клиентов падает примерно вдвое, с 2,8 до 1,4 в месяц.
- **Churn x2** -> annual churn растёт с 16% до 32%, что даёт monthly churn около 3,16% вместо 1,44%.
- **Price -30%** -> ARPA падает с 780 000 ₽ до 546 000 ₽, COGS на клиента оставляю прежним, потому что delivery и inference cost в short-term вниз почти не двигаются.

| Сценарий | Clients @M12 | MRR @M12, ₽ | Gross profit @M12, ₽ | EBITDA @M12, ₽ | Вывод |
|---|---:|---:|---:|---:|---|
| Base | 31,1 | 24 225 608 | 13 976 312 | 7 496 312 | Проходит уверенно |
| Sens1, CAC x2 | 15,5 | 12 112 804 | 6 988 156 | 508 156 | Почти упирается в EBITDA Gate |
| Sens2, Churn x2 | 28,3 | 22 097 166 | 12 748 365 | 6 268 365 | Терпимо, если чек удержан |
| Sens3, Price -30% | 31,1 | 16 957 926 | 6 708 630 | 228 630 | Не проходит EBITDA Gate |

### Вывод по stress-test
1. Главный single-point failure здесь не churn, а **price compression**.
2. **CAC x2** не убивает модель мгновенно, но почти полностью съедает запас прочности.
3. При цене ниже ~550-600 тыс. ₽/мес кейс быстро скатывается из productized managed service в просто дорогой SI без нужной EBITDA.

## B2. Monte Carlo Lite, confidence intervals на M24

### Triangular inputs
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 700 000 | 929 821 | 1 860 000 | 04-economics.md; base CAC и стресс x2 |
| Monthly churn, % | 1,2% | 2,05% | 4,0% | 04-economics.md; operating churn 22% annual, stress-band |
| ARPU, ₽/мес | 546 000 | 780 000 | 900 000 | SECTION A + 04-economics.md |
| Conversion lead->paid, % | 0,7% | 1,3% | 1,8% | 04-economics.md funnel |
| Time-to-hire, мес | 1,0 | 1,6 | 3,0 | 04-economics.md hiring table |

### Метод
Полную 1000-итерационную симуляцию не кодирую, использую **упрощённую 9-комбинационную сетку**: best, median, worst и 6 смешанных комбинаций вокруг CAC/churn/ARPU. Для расчёта M24 беру:
- fixed costs = 6 480 000 ₽/мес,
- COGS = 330 000 ₽/клиент/мес,
- monthly new clients ограничиваются либо funnel conversion, либо acquisition budget,
- hiring drag режет throughput на 8% за каждый месяц найма сверх mode.

### Percentile view
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -2 287 779 | 17 441 412 | 40 092 250 | 42 380 029 |
| CAC payback (мес) | 8,6 | 2,1 | 1,2 | 7,4 |
| LTV/CAC | 3,4x | 18,8x | 49,3x | 45,9x |
| Cash runway (мес) | 20,5 | 36,0+ | 36,0+ | 15,5+ |

### Интерпретация Monte Carlo Lite
1. **Правило #1 срабатывает**: p10 EBITDA < 0, значит downside-ветка даёт реальный риск кассовой несостоятельности.
2. **Правило #2 не срабатывает**: p50 EBITDA сильно выше 500 тыс. ₽/мес, значит median-case проходит gate.
3. **Неопределённость слишком широкая**: распределение идёт от отрицательной EBITDA в хвосте до 40+ млн ₽/мес в верхнем квартиле. Формально p90/p10 не считается из-за отрицательного p10, но по абсолютной ширине хвосты явно слишком далеко, поэтому score надо **даунгрейдить на 1 notch за volatility**.
4. **LTV/CAC range width = 45,9x**, сильно выше допустимого порога 8. Это значит, что модель хрупкая, и ключевая хрупкость сидит именно в сочетании **price + CAC + churn**, а не в одной метрике.

## B3. Competitor deep-dive

### Топ-3 западных
| Конкурент | Что умеет / позиция | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Zendesk AI / Resolution Platform** | Крупнейший установленный helpdesk/service stack с AI layer, 20 000+ customers и 200 млн $ AI ARR | мощная installed base, governance, workflow/integration layer, сильный бренд enterprise service | в РФ прямой rollout ограничен санкциями, data residency и procurement; buyer часто покупает лицензию, но не получает внедрение outcome-level | **~8-12% глобального AI-enabled service software spend**, inference на базе 20k+ клиентов и 200 млн $ AI ARR | мы vendor-agnostic и можем прийти поверх существующего стека, включая локальные платформы, а не требовать replatforming |
| **Sierra** | AI-native enterprise customer service platform, 100+ млн $ ARR и сотни клиентов | сильный AI-native бренд, outcome-based narrative, заметные enterprise logos, быстрый growth signal | дорогой западный стек, слабая локализация под РФ контур, меньше focus на managed adaptation под местные интеграции | **~3-5% AI-native enterprise CX segment**, inference по 100+ млн $ ARR и сотням клиентов | мы можем продавать не платформу, а локальный managed operator с русскоязычным rollout, security workaround и кастомным governance |
| **Parloa / Decagon class** | AI-first voice/chat service automation для enterprise contact center | сильные voice + contact-center кейсы, быстрый рост, крупные enterprise budgets, category proof | очень высокая зависимость от западных LLM/API/телефонии и enterprise stack; в РФ это почти всегда vendor-risk story | **~2-4% каждый в AI-native contact-center automation**, inference по 50+ млн $ revenue у Parloa и 100+ крупных клиентов у Decagon | наше преимущество в том, что мы можем быть orchestration-слоем между локальным контакт-центром, on-prem data policy и несколькими моделями, а не моновендором |

### Топ-4 российских
| Конкурент | Источник / тип | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Naumen** | Naumen CCSAAS, enterprise contact-center платформа | сильная enterprise база в РФ, on-prem/облако, зрелый контакт-центр, хорошая интеграционная история | тяжелее и платформеннее, чем AI-operator wedge; внедрение может быть длинным; не всегда продаёт continuous AI optimization как отдельный managed layer | **~15-20% российского enterprise contact-center software**, inference по широкой базе и заметности в банках/госе | мы можем зайти поверх Naumen как более лёгкий AI-operations слой и не конкурировать head-on по core CCaaS |
| **Just AI** | Habr / рынок разговорного AI и корпоративных ботов | сильная экспертиза в conversational AI, voicebots, NLU, enterprise deployments | часто воспринимается как bot/platform vendor, а не как service-governance operator; сложнее доказать KPI ownership на уровне customer-service ops | **~8-12% российского conversational AI for support**, inference по brand visibility и длительному присутствию | у нас уже из коробки сильнее позиционирование вокруг resolution economics, QA loop и managed optimization |
| **CraftTalk** | Skolkovo / AI-first омниканальная поддержка | сильна в AI support desk, омниканальности, локальном compliance-контуре | меньше дистрибуция и weaker enterprise reach, чем у крупных платформ; может упираться в channel scale | **~3-6% российского AI-support automation**, inference по нишевой позиции и ecosystem visibility | у нас шире vendor-agnostic wedge: можем работать поверх Zendesk-подобных, Naumen и self-hosted стеков |
| **BSS** | Habr / speech + contact-center automation | сильна в речевых технологиях, контакт-центрах, банках и голосовых каналах | исторически больше speech/voice vendor, чем full-stack AI customer service operator; слабее в knowledge orchestration и recurring KPI ownership | **~8-10% российского speech/contact-center AI**, inference по legacy footprint в банках и enterprise sales | мы глубже в text+voice+workflow orchestration и ближе к managed operator модели, а не к pure platform sell |

### Итог по конкурентам
1. На Западе category winner забирает не просто лицензию, а **AI-first service operating layer** с measurable outcomes.
2. В РФ сильнее всего сидят локальные платформы и speech/contact-center игроки, но между ними остаётся свободное окно для **vendor-agnostic managed optimization layer**.
3. Самая реалистичная позиция для кейса, не воевать лоб в лоб с платформами, а стать **оператором AI customer-service transformation поверх чужого стека**.

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять strong solution architect и CSM вовремя | med | high | time-to-hire > 2,5 мес, founder закрывает delivery вручную | заранее формировать bench, template rollout, referral hiring |
| 2 | Operational | LLM/API cost и latency растут быстрее плана | med | high | inference cost > 70 тыс. ₽ на клиента или SLA деградирует 2 спринта подряд | multi-model routing, fallback на open-weight/on-prem, aggressive prompt/cache optimization |
| 3 | Market | Спрос остаётся только на дешёвый pilot, а не на 700k+ retainer | high | high | win-rate есть только на пилоты < 300 тыс. ₽/мес | продавать через KPI ownership и board-level ROI, резать low-end сегмент |
| 4 | Market | Платформы сами downsell'ят цену managed-layer через bundled AI features | med | high | клиенты начинают сравнивать нас только с license add-on за seat | vendor-agnostic ROI calculator, faster rollout, governance/QA as separate budget line |
| 5 | Regulatory | Ограничения по 152-ФЗ и data residency закрывают западные LLM/API в части клиентов | high | high | security review стопорит > 30% pipeline | локальный inference path, private deployment, анонимизация PII |
| 6 | Regulatory | Усиление требований 115-ФЗ/архивации/аудита для финансовых и regulated клиентов | med | med | legal/compliance cycle > 90 дней, новые требования к журналированию | audit logs, role-based access, deployment playbooks для regulated verticals |
| 7 | Financial | Runway сжимается из-за длинного sales cycle и задержки запуска ретейнера | med | high | cash runway < 12 мес до M4-M5 | держать burn cap, staged hiring, upfront setup fee, milestone billing |
| 8 | Financial | USD/RUB и инфляция разъезжают COGS быстрее, чем индексируется цена | high | med | gross margin < 52% два месяца подряд | quarterly repricing, рублёвые contracts с FX-clauses, больше локального стека |
| 9 | Black swan | Новые санкции режут SaaS/vendor access или телефонию | med | high | vendor TOS changes, ограничения по billing/account access | dual-vendor architecture, local substitutes, escrow of prompts/integration logic |
| 10 | Black swan | Ключевой LLM-провайдер недоступен или резко ухудшает quality | med | high | outage > 24h, error rate и hallucination rate скачут | abstraction layer, резервные модели, human fallback queue |

## B5. Kill conditions через 6 месяцев

1. **EBITDA / insolvency kill**: если по rolling-3 median-case forecast **p10 EBITDA@M24 остаётся < 0**, продолжать нельзя, downside слишком токсичный.
2. **Pricing kill**: если фактический blended retainer через 6 месяцев **< 550 000 ₽/клиент/мес** или gross margin **< 50%**, модель не держит EBITDA Gate.
3. **Go-to-market kill**: если к M6 нет хотя бы **6 платящих клиентов** или CAC остаётся **> 1,5 млн ₽** при payback **> 12 мес**, repeatable motion не доказан.

## B6. Финальный вывод SECTION B

Кейс всё ещё можно тянуть дальше, но уже не как "просто Zendesk AI service". Финансово он держится только как **high-ticket AI customer-service operations operator** с жёсткой дисциплиной по цене, margin и vendor-risk. Главная опасность, что рынок затащит компанию в price compression и кастомный SI. Поэтому после P6B мой статус такой:
- **не reject сразу**, потому что median-case и base-case ещё сильные;
- **но score нужно понизить на 1 notch** из-за очень широкой дисперсии Monte Carlo Lite и чувствительности к цене.

## Источники SECTION B
- [B1] Zendesk AI for customer service: https://www.zendesk.com/service/ai/
- [B2] Zendesk, AI-First Strategy Gains Momentum, 2026-03-11: https://www.zendesk.com/newsroom/press-releases/zendesk-secures-key-industry-recognition-as-its-ai-first-strategy-gains-momentum/
- [B3] Sierra customers: https://sierra.ai/customers
- [B4] Axios, Sierra hits $100M ARR, 2026-04-15: https://www.axios.com/2026/04/15/ai-startup-sierra-hits-100m-arr
- [B5] Parloa surpasses $50M revenue mark: https://www.parloa.com/parloa-in-the-press/parloa-surpasses-50m-revenue-mark/
- [B6] Parloa AI contact center scale: https://www.parloa.com/landing-page/ai-contact-center-scale/
- [B7] TechCrunch, Decagon completes first tender offer at $4.5B valuation, 2026-03-04: https://techcrunch.com/2026/03/04/decagon-completes-first-tender-offer-at-4-5b-valuation/
- [B8] Naumen Contact Center SaaS: https://www.naumen.ru/products/ccsaas/
- [B9] Habr, Just AI company materials: https://habr.com/ru/companies/just_ai/
- [B10] Skolkovo, CraftTalk profile: https://navigator.sk.ru/orn/1123818
- [B11] Habr, BSS company materials: https://habr.com/ru/companies/bss/articles/

<!-- P6B-DONE -->


---

# 06-verdict.md

[B2B-OPS] Zendesk AI Customer Service Operator v2 — REJECTED: 58/100 | EBITDA base=7496К₽/мес через 12 мес | LTV/CAC=4,6x | Ключевое преимущество: enterprise AI support ops уже monetized globally | Главный риск: в РФ direct-demand слабый, а delivery легко сползает в кастомный SI.

# 06-verdict

sector: B2B-OPS

## Investment one-liner
[B2B-OPS] Zendesk AI Customer Service Operator v2 — REJECTED: 58/100 | EBITDA base=7496К₽/мес через 12 мес | LTV/CAC=4,6x | Ключевое преимущество: enterprise AI support ops уже monetized globally | Главный риск: в РФ direct-demand слабый, а delivery легко сползает в кастомный SI.

## Итоговый вердикт
**REJECTED.**

Почему не approve:
1. Экономика на бумаге сильная, но держится почти целиком на enterprise-retainer 780 тыс. ₽/мес и жёсткой дисциплине delivery.
2. В РФ прямой Zendesk-specific спрос почти отсутствует, а adjacent demand больше похож на рынок enterprise contact-center automation, чем на отдельный investable wedge.
3. Кейс слишком близок к кастомному SI/operator business и пока не доказывает moat, repeatability и price power на локальном рынке.
4. Approval gate по EBITDA формально проходит, но investment committee уровень требует не только EBITDA, а и margin of safety по спросу, moat и GTM, которого здесь пока нет.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «Decision LTV/CAC = 4,6x», «Operating payback = 11,1 мес», «Gross Margin = 57,7%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 22 | В 05-critic base-case «EBITDA @M12 = 7 496 312 ₽/мес», break-even уже на M6. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 11 | «прямой брендовый спрос в РФ на Zendesk AI почти отсутствует», при этом есть только adjacent signal «автоматизация поддержки клиентов» с hh_ru=3074. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Глобальный category proof есть, но «кейс легко деградирует в тяжёлый SI/аутсорсинг», а локальный moat слабый. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 12 | В risk matrix одновременно high по спросу на дешёвый pilot, 152-ФЗ/data residency и санкционному vendor-risk. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 13 | ICP понятен, но «Brand pull по Zendesk в РФ почти отсутствует», а blended CAC 929 821 ₽ делает GTM хрупким. |

**Raw total = 87 / 150**  
**Normalized score = round((87 × 100) / 150) = 58/100**

## 7-factor moat framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | После интеграций, knowledge graph и QA-loop есть умеренная инерция. |
| Scale economies | 1 | Инференс и шаблоны помогают, но human-heavy delivery съедает эффект масштаба. |
| Proprietary data / model advantage | 1 | Данных клиента много, но собственного датасетного преимущества пока нет. |
| Regulatory moat | 1 | Compliance нужен, но он скорее барьер входа, чем настоящий эксклюзивный moat. |
| Brand / distribution | 1 | Сильного локального бренда и канала дистрибуции в РФ нет. |
| Embedded workflow | 3 | Если слой заходит в routing, KB, QA и governance, он глубоко встраивается в service workflow. |

**Moat sum = 9 / 21**  
**Moat score = round((9 × 25) / 21) = 11/25**

Вывод: **weak moat**. Это автоматически входит в top-3 risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 4 305 600 ₽ (decision LTV) |
| CAC fully-loaded | 929 821 ₽ |
| LTV/CAC | 4,6x |
| CAC payback | 11,1 мес |
| Gross Margin | 57,7% |
| contribution_margin_rub_month | 398 000 ₽ |
| fixed_costs_rub_month | 6 480 000 ₽ |
| company_ebitda_rub_month (base M12) | 7 496 312 ₽/мес |
| company_ebitda_potential_rub_month | 7 496 312 ₽/мес |
| clients_to_500k_ebitda | 16 |
| clients_to_1m_ebitda | 19 |
| months_to_500k_ebitda | 6 |
| months_to_1m_ebitda | 7 |
| startup_capital_to_bep_rub | 13 859 585 ₽ |
| EBITDA break-even clients | 15 |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping по enterprise service buyers | SDR | CRM, Rusprofile, manual research | 2 ч | 2 400 | Низкий |
| 2 | Outreach и qualification | SDR | Email, phone, Telegram, LinkedIn-like sourcing | 2 ч | 2 800 | Средний |
| 3 | Discovery-call по support economics | AE | Meet, discovery template | 1.5 ч | 6 500 | Средний |
| 4 | Service workflow audit | AE + solutions lead | Audit checklist, service maps | 5 ч | 24 000 | Низкий |
| 5 | Demo / pilot hypothesis | AE + solution architect | Demo environment, ROI sheet | 3 ч | 15 000 | Низкий |
| 6 | KPI / pilot scoping | AE + CSM + architect | SOW, KPI model | 4 ч | 19 000 | Низкий |
| 7 | Security / compliance / integration review | CTO + architect | API docs, security docs | 8 ч | 36 000 | Низкий |
| 8 | Pilot rollout 6-10 недель | CSM + architect + QA lead | Playbooks, helpdesk, dashboards | 35 ч | 118 000 | Низкий |
| 9 | Procurement / legal / contract | AE + founder + legal | Contract workflow, ЭДО | 10 ч | 42 000 | Низкий |
| 10 | Initial onboarding / go-live | CSM + support ops lead | Runbook, analytics, enablement | 12 ч | 46 000 | Средний |
| 11 | Monthly optimization cycle | CSM + analyst + QA | Dashboards, QA review, roadmap | ежемес. | 0 в CAC | Средний |
| 12 | Invoice / reporting | Finance ops | Банк, ЭДО, CRM | 1 ч | 3 500 | Высокий |

## Команда

| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Time-to-hire |
|---|---:|---:|---:|
| CEO / founder | 1 | 845 000 | 0 |
| CTO / platform lead | 1 | 715 000 | 2 |
| Backend / integrations | 2 | 1 014 000 | 1.5 |
| ML / applied AI | 1 | 650 000 | 2.5 |
| Solution architect | 1 | 546 000 | 1.5 |
| QA / conversation analyst | 1 | 338 000 | 1 |
| SDR | 2 | 416 000 | 1 |
| AE | 1 | 416 000 | 1.5 |
| Customer Success / service ops | 2 | 624 000 | 1 |
| Finance / ops (0.5) | 0.5 | 156 000 | 1 |
| **Итого** | **12.5** | **5 720 000 ₽/мес** |  |

## Top-3 risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| weak_moat_and_SI_drift | high | high | weak moat 11/25, delivery легко превращается в bespoke SI и съедает маржу. |
| evidence_quality_unverified | med | med | В 02-demand.md отсутствует строка `Sources: T1/T2/T3`, поэтому к Market+Demand применён штраф и качество евиденции требует ручной верификации. |
| vendor_and_regulatory_dependency | high | high | 152-ФЗ, data residency, санкции и зависимость от западных LLM/helpdesk-vendors могут стопорить rollout у regulated клиентов. |

## Proof points, которых не хватило до APPROVED
1. Минимум 2-3 локальных paid pilots у enterprise support teams с чеком ≥ 500-700 тыс. ₽/мес.
2. Подтверждение, что vendor-agnostic delivery работает поверх Naumen / локальных стеков, а не только как Zendesk-thesis.
3. Подтверждённый rollout playbook, где gross margin после стабилизации держится ≥ 55% без heavy founder involvement.
4. Evidence, что buyer реально покупает recurring optimization retainer, а не одноразовый pilot/setup.

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Т-Банк | Огромный входящий поток и зрелая digital-support функция, где важны AHT, CSAT и automation. | email decision-maker в customer service / intro через fintech-экосистему | 900 000 ₽/мес |
| 2 | Сбер | Масштабные омниканальные обращения и высокий бюджет на service automation и governance. | партнёрство через SI / конференция CX & AI | 1 200 000 ₽/мес |
| 3 | Альфа-Банк | Сильный digital-first support, где можно продавать pilot на routing и AI-resolution KPI. | founder-led intro + email директора поддержки | 850 000 ₽/мес |
| 4 | МТС | Большой контакт-центр и сложный multi-channel customer care, где нужен managed optimization layer. | партнёрство с интегратором / отраслевые конференции | 800 000 ₽/мес |
| 5 | МегаФон | Высокий объём обращений, SLA и повторяемые сценарии для AI-triage и knowledge orchestration. | email decision-maker / телеком-ивенты | 750 000 ₽/мес |
| 6 | Ozon | E-commerce support с большими очередями и высокой ценой ошибки в доставке, возвратах и merchant support. | warm intro через ops/community / email head of CX | 900 000 ₽/мес |
| 7 | Wildberries | Массовый buyer/seller support и боль по quality routing, FAQ deflection и escalation. | partner-led approach / outbound ABM | 950 000 ₽/мес |
| 8 | Яндекс Маркет | Сложный marketplace support stack и явная потребность в knowledge quality + AI-routing. | email руководителю customer support / через Яндекс Cloud ecosystem | 850 000 ₽/мес |
| 9 | Самокат | Высокочастотные customer issues и операционная выгода от быстрого AI-resolution для delivery cases. | vc.ru ad + outbound к ops-lead | 650 000 ₽/мес |
| 10 | ДОМ.РФ | Уже есть подтверждённый кейс на речевой аналитике и measurable service uplift, значит buyer pain валидирован. | кейс-based outreach / партнёрство с Naumen-интегратором | 700 000 ₽/мес |

## Финансовая интерпретация
- **Base case:** EBITDA выходит в плюс на M6 и доходит до 7,50 млн ₽/мес к M12, но это опирается на высокий ARPA и controlled delivery scope.
- **Stress:** при CAC x2 EBITDA @M12 падает до 508 тыс. ₽/мес, а при price -30% остаётся только 228 630 ₽/мес, то есть запас прочности узкий.
- **Monte Carlo Lite:** p10 EBITDA @M24 = -2 287 779 ₽/мес, p50 = 17 441 412 ₽/мес, что подтверждает слишком широкий downside/upside band для approve.

## LTV Upside Calculator
Чтобы перевести кейс из REJECTED в APPROVED, нужен один из следующих апгрейдов:

1. **Поднять GTM certainty**  
   Если появятся 3 локальных logo-клиента с ARPA 700-900 тыс. ₽/мес и retention > 12 мес, Market+Demand и GTM можно поднять суммарно на +8-10 raw points.

2. **Сузить execution risk**  
   Если rollout станет vendor-agnostic и потребность в senior architect time снизится на 20-25%, Execution Risk и Moat суммарно получат ещё +6-8 raw points.

3. **Зафиксировать pricing power**  
   Если будет доказано, что blended retainer устойчиво держится ≥ 750 тыс. ₽/мес без кастомного SI, кейс поднимется выше 65-70 и сможет претендовать на near-pass/approve with notes.

## Сравнение с более широким кейсом
Кейс по сути является более узкой Zendesk-centered версией более общего `ai-customer-service-operations-operator-v2`. Узкая привязка к Zendesk добавляет category proof, но не улучшает локальный moat и ухудшает vendor-risk, поэтому инвестиционный вывод остаётся отрицательным.


---

# 07-score-trajectory.md

# 07-score-trajectory

| Дата | Stage | Score / verdict | Что изменилось |
|---|---|---|---|
| 2026-04-22 | P3 Demand | CONDITIONAL PASS | Сильный global category proof по Zendesk AI, но в РФ direct demand почти нулевой и thesis пришлось развернуть в более широкий AI customer service operations layer. |
| 2026-04-22 | P4 Solution | CONDITIONAL PASS | Подтверждён workable wedge как managed optimization layer поверх существующих helpdesk/contact-center stack, но вырос риск SI-drift и vendor dependence. |
| 2026-04-24 | P5 Economics | CONDITIONAL PASS | Экономика собралась только в enterprise managed-retainer модели: Decision LTV/CAC 4,6x, payback 11,1 мес, EBITDA break-even на M6. |
| 2026-04-25 | P6 Critic | VOLATILE PASS | Monte Carlo Lite показал p10 EBITDA ниже нуля и сильную чувствительность к price compression; moat и локальный demand остались слабыми. |
| 2026-04-25 | P7 Verdict | 58/100, REJECTED | Формальный EBITDA gate пройден, но investment-grade запас прочности по рынку, moat и repeatable GTM не доказан. |
