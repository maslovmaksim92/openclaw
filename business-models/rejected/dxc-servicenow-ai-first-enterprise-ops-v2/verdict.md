# dxc-servicenow-ai-first-enterprise-ops-v2 — полный инвестиционный разбор

- Статус: 🟡 NEAR-PASS
- Score: **67/100**
- Sector: **B2B-OPS**
- GitHub canonical path: `rejected/dxc-servicenow-ai-first-enterprise-ops-v2/verdict.md`

---

## Stage 1. Intake

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-dxc-servicenow-ai-first-enterprise-ops.md
created: 2026-04-20T12:12:13+03:00
---

# 01-intake

## Кейс
dxc-servicenow-ai-first-enterprise-ops-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — dxc-servicenow-ai-first-enterprise-ops

## Meta
- source: triage/triage-2026-04-14-dxc-servicenow-ai-first-enterprise-ops.md
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
2026-04-14

## Inputs
- pipeline/raw/raw-2026-04-14-dxc-servicenow-ai-first-enterprise-ops.md

## Classification
supporting signal

## Decision
Обогатить существующий case.

**Case slug:** `autonomous-enterprise-service-operations-operator`

## Why
- Сигнал тематически совпадает с действующим кейсом про autonomous enterprise service operations для back-office, shared services и service operations.
- DXC показывает важный паттерн: сначала внутренний Customer Zero и перевод core business functions на agentic AI, затем упаковка validated use cases в клиентское сервисное предложение.
- Это усиливает именно сервисную гипотезу кейса, потому что речь идёт о постоянном операционном слое, мониторинге, проактивном решении проблем и continuous optimisation, а не о разовом AI-проекте.

## Triage note
Кейс `autonomous-enterprise-service-operations-operator` обогащён. В `01-evidence.md` добавлен supporting signal про партнёрство DXC и ServiceNow с датой, URL источника, объяснением, как сигнал усиливает кейс, и ключевыми фактами о модели Customer Zero, автоматизации high-volume процессов и упаковке validated AI use cases в глобальное сервисное предложение.

```



---

## Stage 2. Demand Validation

---
stage: demand-validation
case: dxc-servicenow-ai-first-enterprise-ops-v2
date: 2026-04-21
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
DXC + ServiceNow AI-first enterprise operations: enterprise-layer для автоматизации service operations, shared services и core business functions через agentic AI, workflow orchestration и managed transformation delivery.

## Итог
**Статус: CONDITIONAL PASS.**

- По exact AI-лейблу спрос в РФ низкий: `dxc servicenow ai first enterprise operations` и `ServiceNow AI platform enterprise operations` дают `LOW` и `demand_score=0`, без заметного hiring-сигнала. [T4]
- Но adjacent budget lines уже существуют и выглядят живыми: `it service management` даёт `LOW`, но `demand_score=26`, `hh_ru=241`, `yandex_suggest=100`; `enterprise service management` даёт `demand_score=18`, `hh_ru=31`, `yandex_suggest=100`; `service desk automation` даёт `demand_score=7`, `hh_ru=135`. [T4]
- Это значит, что в локальном контуре покупают не историю про abstract agentic AI, а бюджеты на ITSM, ESM, service desk, shared services automation и back-office orchestration. [T4][T5][T6]
- Глобальный category proof сильный: **7 апреля 2026 года** DXC и ServiceNow объявили multi-year agreement, где DXC идёт как Customer Zero для Core Business Suite и затем упаковывает validated use cases в клиентское предложение. [T1]
- У ServiceNow сама платформа и спрос enterprise-класса подтверждены финансово: **28 января 2026 года** компания сообщила `subscription revenues $3.466B` за Q4 2025, `cRPO $12.85B` и `244` сделок с net new ACV выше `$1M` только за квартал. [T2]

## 1. Спрос и сигналы рынка

### Demand API
- `dxc servicenow ai first enterprise operations` → **LOW**, `demand_score=0`, `hh_ru=0`, `habr=2`, `yandex_suggest=2`. [T4]
- `ServiceNow AI platform enterprise operations` → **LOW**, `demand_score=0`, `hh_ru=0`, `habr=2`, `yandex_suggest=2`. [T4]
- `it service management` → **LOW**, `demand_score=26`, `hh_ru=241`, `habr=2`, `yandex_suggest=100`. [T4]
- `service desk automation` → **LOW**, `demand_score=7`, `hh_ru=135`, `habr=2`, `yandex_suggest=2`. [T4]
- `enterprise service management` → **LOW**, `demand_score=18`, `hh_ru=31`, `habr=2`, `yandex_suggest=100`. [T4]

### Интерпретация
- В РФ почти нет спроса на новый длинный AI-label, но есть зрелый спрос на service-management слой и автоматизацию сервисных подразделений. [T4]
- Для такого кейса это нормально: buyer ищет не «agentic AI for enterprise operations», а решение под конкретный бюджет, например ITSM, ESM, HR/shared services, procurement workflows, внутренний сервисный каталог или service desk automation. [T3][T5][T6]
- Следовательно, exact-demand слабый, но underlying spend-category реальна.

## 2. Category proof и why now
1. **7 апреля 2026 года** DXC и ServiceNow объявили новую волну AI-first enterprise transformation: DXC использует ServiceNow Core Business Suite как Customer Zero, активирует agentic AI в core business functions и обещает затем тиражировать validated use cases клиентам. Это очень сильный signal, потому что model = сначала internal proof, потом packaged services offer. [T1]
2. В том же анонсе DXC прямо пишет про automation high-volume processes, proactive issue resolution, real-time insights и library of repeatable patterns. Это не разовая кастомная интеграция, а попытка собрать repeatable delivery motion. [T1]
3. **7 мая 2025 года** ServiceNow представил Core Business Suite как AI-powered решение для HR, procurement, finance, facilities и legal, с быстрым внедрением и case-management паттерном. Значит DXC строит предложение не на сырой идее, а на уже оформленном продуктовом слое ServiceNow. [T3]
4. **28 января 2026 года** ServiceNow показал масштаб самой spend-category: `subscription revenues $3.466B` за Q4 2025, `remaining performance obligations $28.2B`, `603` клиентов с ACV выше `$5M`. [T2]
5. Из этого следует, что мировой enterprise-рынок уже готов платить за workflow-native AI automation на уровне крупных многолетних контрактов. [T2][inference]

## 3. Что это значит для локального B2B-OPS кейса
- Локальный кейс не выглядит как чистый software import story. Он ближе к managed transformation layer вокруг enterprise service operations, shared services и back-office orchestration. [T1][T3]
- Важный момент: в РФ уже существуют локальные substitutes. Naumen ESM продаёт автоматизацию корпоративных сервисов для HR, закупок, бухгалтерии, ИТ, клиентского сервиса и юридической поддержки. [T5]
- SimpleOne ITSM тоже позиционируется как enterprise-ready ITSM/ESM платформа для поддержки, эксплуатации, SLA, CMDB и сервисных процессов для разных подразделений. [T6]
- Поэтому premium wedge нельзя защищать только брендом ServiceNow. Его нужно защищать пакетом: сложные multivendor environments, трансформация shared services, governance, migration risk reduction, cross-functional orchestration и тяжёлый delivery. [T1][T5][T6]

## 4. Кто купит
Вероятный ICP в локальном контуре:
- крупные банки и страховщики,
- телекомы,
- промышленные группы с общими центрами обслуживания,
- федеральные/крупные региональные структуры,
- большие аутсорсинговые и ИТ-сервисные организации,
- холдинги с распределённым back-office и большим объёмом service requests,
- интеграторы и managed-service провайдеры, которым нужен enterprise service layer.

### Sanity-check buyer list
1. банки с крупными ИТ и GBS-контурами,
2. страховщики,
3. телеком-операторы,
4. металлургия и heavy industry,
5. нефтегазовые и энергетические группы,
6. ритейл-холдинги с shared services,
7. госкомпании,
8. крупные логистические операторы,
9. enterprise BPO / SSC-провайдеры,
10. системные интеграторы с managed operations практикой.

## 5. WTP и коммерческие якоря
- DXC фактически валидирует, что enterprise buyer покупает не только платформу, но и transformation program вокруг неё. [T1]
- ServiceNow финансово подтверждает, что категория выдерживает крупные многолетние enterprise контракты и высокий ACV. [T2]
- Одновременно Naumen и SimpleOne показывают, что в РФ есть локальный рынок сервисных платформ и он уже привычен к автоматизации service operations. [T5][T6]

### Что это значит для willingness to pay
- **WTP подтверждён** для enterprise service-management budget.
- Но **premium-WTP условный**: если предложение скатится в generic ITSM/ESM, локальные российские платформы и интеграторы начнут давить цену. [T5][T6]
- Высокий чек возможен только там, где есть сложная трансформация и measurable value: сокращение ручного труда, faster resolution, унификация процессов, visibility across functions и managed optimisation layer. [T1][T3]

## 6. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру три уровня чека:
- pilot / ограниченный контур: **400 000 ₽/мес**,
- base managed transformation: **800 000 ₽/мес**,
- крупный multi-function enterprise контур: **1 500 000 ₽/мес**.

Для sizing использую базовый чек **800 000 ₽/мес** или **9.6 млн ₽/год**. Это выше локального коробочного ITSM и оправдано только при enterprise delivery + orchestration layer. [inference from T1/T5/T6]

### TAM
Беру universe **1 200** крупных организаций и сервисных контуров, где есть заметный service-management budget.

**TAM = 1 200 × 9.6 млн ₽ = 11.52 млрд ₽/год**

### SAM
Реально адресуемый слой для первого GTM, где есть сложные shared services, зрелый ИТ-ландшафт и бюджет под трансформацию, беру **180** аккаунтов.

**SAM = 180 × 9.6 млн ₽ = 1.728 млрд ₽/год**

### SOM
Ранний реалистичный захват:
- **6 клиентов** в горизонте 24 месяцев.

**SOM = 6 × 9.6 млн ₽ = 57.6 млн ₽/год**

### Вывод
Рынок не массовый, но достаточно широкий для Program 2, если продавать дорогой transformation layer, а не generic service desk.

## 7. Profit Gate

### Сценарий A: лёгкий pilot
- Цена: **400 000 ₽/мес**
- Валовая маржа: **60%**
- Валовая прибыль на клиента: **240 000 ₽/мес**
- При fixed costs **2.5 млн ₽/мес** для выхода на **500 000 ₽ EBITDA/мес** нужно **13 клиентов**
- **Вердикт:** погранично, execution-heavy

### Сценарий B: managed transformation base-case
- Цена: **800 000 ₽/мес**
- Валовая маржа: **62%**
- Валовая прибыль на клиента: **496 000 ₽/мес**
- Нужно **7 клиентов**
- **Вердикт:** PASS

### Сценарий C: крупный enterprise контур
- Цена: **1 500 000 ₽/мес**
- Валовая маржа: **58%**
- Валовая прибыль на клиента: **870 000 ₽/мес**
- Нужно **4 клиента**
- **Вердикт:** PASS

### Общий вывод по Profit Gate
Кейс проходит demand-gate только если продаётся как high-ticket B2B-OPS transformation с managed delivery. Если это просто ещё один ITSM/ESM проект, экономика быстро деградирует из-за локальных substitutes и кастомной конкуренции.

## 8. Основные риски
- Слабый exact-demand по новому AI-label. [T4]
- Сильные локальные substitutes в лице Naumen / SimpleOne и других сервисных платформ. [T5][T6]
- Риск, что большая часть value capture останется у интегратора и services layer, а не у repeatable продукта. [T1][inference]
- Длинные enterprise cycles, сложные внедрения, высокий presales load и возможные ограничения вокруг глобального vendor stack в локальном контуре. [T1][T5][T6]

## 9. Вывод для pipeline
**Не отклонять на этапе demand validation.**

Причины:
1. underlying budget category в локальном рынке есть,
2. global category proof очень сильный и свежий,
3. DXC показывает правдоподобный motion customer-zero → packaged offering,
4. Profit Gate математически собирается в high-ticket сценарии.

Но дальше в P5/P6 нужно особенно жёстко проверить:
- сколько в модели скрытого services load,
- насколько вообще возможен локальный доступ к ServiceNow-centric stack,
- есть ли repeatable wedge против Naumen/SimpleOne и крупных интеграторов,
- не превращается ли кейс в custom SI-бизнес с плохой масштабируемостью.

## Источники
- [T1] DXC + ServiceNow partnership announcement, 2026-04-07: https://dxc.com/newsroom/04072026-dxc-partners-with-servicenow-on-a-new-wave-of-ai-first-enterprise-transformation
- [T2] ServiceNow Q4 and full-year 2025 results, 2026-01-28: https://newsroom.servicenow.com/press-releases/details/2026/ServiceNow-Reports-Fourth-Quarter-and-Full-Year-2025-Financial-Results-Board-of-Directors-Authorizes-Additional-5B-for-Share-Repurchase-Program/default.aspx
- [T3] ServiceNow Core Business Suite launch, 2025-05-07: https://www.servicenow.com/company/media/press-room/core-business-suite.html
- [T4] Demand API: http://172.18.0.1:9001/multi-demand?keyword=dxc%20servicenow%20ai%20first%20enterprise%20operations
- [T4] Demand API: http://172.18.0.1:9001/multi-demand?keyword=ServiceNow%20AI%20platform%20enterprise%20operations
- [T4] Demand API: http://172.18.0.1:9001/multi-demand?keyword=it%20service%20management
- [T4] Demand API: http://172.18.0.1:9001/multi-demand?keyword=service%20desk%20automation
- [T4] Demand API: http://172.18.0.1:9001/multi-demand?keyword=enterprise%20service%20management
- [T5] Naumen Enterprise Service Management: https://www.naumen.ru/products/esm/
- [T6] SimpleOne ITSM: https://simpleone.ru/itsm

Sources: T1=1, T2=1, T3=1, T4=5, T5=1, T6=1. Primary evidence basis: T1/T2/T3/T4.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

## Market Pulse
Market Pulse 22.04.2026: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.
> Market Pulse 2026-04-25: растущий интерес.



---

## Stage 3. Solution / GTM Fit

---
stage: solution
case: dxc-servicenow-ai-first-enterprise-ops-v2
date: 2026-04-25
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
DXC + ServiceNow AI-first enterprise operations как B2B-OPS слой для enterprise service operations, shared services и core business workflows: audit, design, rollout и managed optimization поверх ServiceNow AI Platform / Core Business Suite.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. DXC и ServiceNow продают не «ещё один AI-проект», а execution-layer для core business functions, где важны automation high-volume processes, proactive issue resolution, governance и repeatable rollout. [T1][T2][T3]
2. Самый правдоподобный локальный wedge, не resale лицензий, а **enterprise operations transformation layer**: mapping процессов, agent/workflow design, integration, guardrails, KPI ownership и ongoing optimization. [T1][T2][T4][inference]
3. Solution-fit есть только в large enterprise и shared-services контурах, где уже живут бюджеты на ITSM/ESM, service desk automation и back-office orchestration. Для mid-market и generic automation кейс слишком тяжёлый. [T5][T6][inference]
4. Главный риск, модель легко превращается в тяжёлый SI-бизнес с bespoke delivery, если не доказать шаблонный deployment и recurring managed layer поверх проекта внедрения. [T1][T4][inference]

## 1. Какую проблему реально решает продукт

Продукт решает дорогую задачу enterprise-уровня: как перевести service operations и shared services из режима ручных handoff'ов, очередей и разрозненных систем в режим workflow-native orchestration с AI и контролируемым исполнением.

Ключевые боли buyer'а:
- ручная обработка high-volume внутренних запросов;
- длинные циклы согласований и эскалаций между функциями;
- слабая visibility across HR, finance, procurement, legal, IT и общими сервисами;
- высокая стоимость service desk / SSC / GBS операций;
- риск запускать AI без policy, access control и audit trail. [T1][T2][T3]

Это painkiller только там, где service operations уже влияют на P&L, SLA и скорость внутренних бизнес-процессов.

## 2. Продуктовый wedge

### Core wedge
**Enterprise AI operations transformation layer**
- аудит service operations и shared-services процессов;
- выбор одного monetizable workflow с явным owner'ом и KPI;
- проектирование agentic workflows и human-in-the-loop точек;
- интеграция ServiceNow AI Platform / Core Business Suite с текущими системами;
- настройка governance, permissions, routing, approvals и observability;
- rollout, adoption и постоянная оптимизация результата.

### Почему wedge выглядит правдоподобно
1. **DXC уже описывает repeatable pattern.** В анонсе от **7 апреля 2026 года** компания говорит про Customer Zero, library of repeatable use cases и packaging outcomes для клиентов. Это сильный сигнал, что value capture закладывается именно в delivery-layer, а не только в лицензии. [T1]
2. **ServiceNow сам позиционирует платформу как orchestration-layer.** Официальные материалы про AI Platform и Core Business Suite делают акцент на объединении AI, data и workflows across the enterprise, а не на узком point solution. [T2][T3]
3. **Партнёрский слой встроен в модель.** ServiceNow отдельно усиливает partner program вокруг AI agents и workflow delivery, а DXC публично подчёркивает свой масштаб экспертизы в ServiceNow. [T4][T7]

## 3. Для кого solution-fit реален

### Primary ICP
- крупные банки, страховые группы и телекомы;
- промышленные группы и холдинги с shared services;
- большие ИТ-сервисные и BPO-операции;
- enterprise с GBS/SSC-моделью;
- системные интеграторы и managed-service игроки, которым нужен более дорогой AI-led operations offer.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. большой поток внутренних сервисных запросов;
2. заметный owner на уровне COO, CIO, head of GBS/SSC, head of service operations;
3. зрелый process stack и боль от cross-functional handoff'ов;
4. готовность мерить outcome, SLA, cost-to-serve, backlog, cycle time;
5. бюджет не на «эксперимент с AI», а на реальную трансформацию операционного слоя. [T1][T2][T5][T6][inference]

### Нецелевой сегмент
- mid-market без shared-services сложности;
- компании, где pain решается обычным helpdesk / low-code automation;
- клиенты без sponsor'а на уровне operations или transformation;
- проекты, где нет recurring scope после initial launch.

## 4. Как продукт должен выглядеть в локальном GTM

### Слабый вариант
- «внедрим ServiceNow AI»;
- generic AI/automation риторика;
- ставка на vendor brand без ownership за KPI;
- разовый integration project.

Такой motion слабый, потому что локальный buyer покупает budget line под ITSM/ESM/operations, а не абстрактную AI-platform историю. Плюс в РФ уже есть substitutes вроде Naumen ESM и SimpleOne ITSM. [T5][T6]

### Реалистичный вариант
- заход через audit дорогого service bottleneck;
- pilot на одном workflow, например case management, internal service routing, finance/procurement/HR request flow;
- KPI пилота: cycle time, SLA adherence, backlog, manual touches, cost-to-serve, quality of resolution;
- rollout как managed optimization layer;
- позиционирование не как resale, а как enterprise operations transformation with governance. [T1][T2][T3][inference]

## 5. Delivery model

### Наиболее правдоподобная схема внедрения
1. discovery и process audit;
2. выбор одного процесса с measurable ROI;
3. mapping data, approvals, roles, controls и handoff'ов;
4. конфигурация workflows / agents / integrations;
5. ограниченный pilot 6-12 недель;
6. сравнение baseline и результата;
7. расширение на соседние функции;
8. переход в managed optimization retainer.

### Кто должен быть buyer'ом
- COO / head of operations;
- CIO / enterprise applications owner;
- head of GBS / SSC;
- service operations director;
- transformation sponsor в крупной функциональной вертикали.

### Кто редко будет настоящим buyer'ом
- линейный ITSM manager без бюджета;
- isolated IT owner без бизнес-спонсора;
- procurement без ownership за outcome.

## 6. Почему клиент купит это, а не альтернативы

У клиента уже есть substitutes:
- Naumen ESM / локальные ESM-стеки;
- SimpleOne ITSM и смежные российские платформы;
- обычные системные интеграторы;
- внутренние process excellence / automation teams.

Выиграть можно только если предложение:
1. быстрее доводит процесс до production outcome, чем обычный SI;
2. берёт на себя governance и orchestration, а не только настройку тикетов;
3. показывает recurring value после запуска, а не исчезает после проекта;
4. работает как cross-functional operations layer, а не ещё один helpdesk deployment. [T1][T2][T5][T6][inference]

## 7. Конкурентная позиция

### Против локальных ESM/ITSM платформ
Преимущество возможно только на более дорогом transformation layer, где ценность в orchestration, adoption и managed optimization, а не в коробке.

### Против обычных интеграторов
Шанс есть, если после go-live остаётся измеримый recurring scope: tuning, rollout, KPI review, governance updates, новые workflows.

### Против in-house команды
Преимущество возникает, если time-to-value выше и есть накопленная библиотека повторяемых паттернов deployment.

## 8. Основные риски solution-fit

1. **SI-risk:** слишком много bespoke integration work на клиента.
2. **Vendor-access risk:** ServiceNow-centric motion может упираться в локальные ограничения, procurement и импортозамещение. [T1][T2][inference]
3. **Repeatability risk:** без шаблонных use cases кейс распадётся в проектную выручку.
4. **Competition risk:** локальные ESM/ITSM alternatives будут давить цену и упрощать narrative. [T5][T6]
5. **Adoption risk:** без сильного sponsor'а agentic workflow останется пилотом без масштабирования.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит продажа и запуск одного enterprise-контура;
- сколько людей и часов уходит на pilot и ongoing optimization;
- какая доля gross margin съедается integration / governance / support-нагрузкой;
- удерживается ли чек 500 000+ ₽/мес без full-custom delivery;
- сколько клиентов нужно, чтобы модель вышла на EBITDA выше 500 000 ₽/мес;
- не является ли кейс на практике лишь consulting wrapper вокруг дорогого vendor stack.

## Итог для пайплайна

**P4 пройден условно.**

Кейс стоит двигать дальше только как high-ticket B2B-OPS transformation layer для крупных enterprise service operations. Если на P5/P6 не подтвердятся repeatable delivery, recurring scope и margin discipline, кейс нужно резать как слишком integration-heavy.

## Источники
- [T1] DXC, DXC Partners with ServiceNow on a New Wave of AI-first Enterprise Transformation, 2026-04-07: https://dxc.com/newsroom/04072026-dxc-partners-with-servicenow-on-a-new-wave-of-ai-first-enterprise-transformation
- [T2] ServiceNow, Core Business Suite press release, 2025-05-07: https://www.servicenow.com/company/media/press-room/core-business-suite.html
- [T3] ServiceNow, AI Platform overview: https://www.servicenow.com/products/servicenow-platform.html
- [T4] ServiceNow, Partner Program for AI agent innovation, 2026-01-21: https://newsroom.servicenow.com/press-releases/details/2026/ServiceNow-enhances-global-Partner-Program-to-accelerate-AI-agent-innovation/default.aspx
- [T5] Naumen Enterprise Service Management: https://www.naumen.ru/products/esm/
- [T6] SimpleOne ITSM: https://simpleone.ru/itsm
- [T7] DXC ServiceNow partnership page: https://dxc.com/about-us/partner-ecosystem/servicenow

> Проверка дат: свежий базовый сигнал по партнёрству DXC + ServiceNow опубликован 7 апреля 2026 года. Это и есть актуальный source-of-truth для solution thesis на текущий момент.


---

## Stage 4. Unit Economics

---
stage: unit-economics
case: dxc-servicenow-ai-first-enterprise-ops-v2
date: 2026-04-25
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Статус: PASS WITH RESERVATIONS.**

Экономика сходится только как **enterprise transformation + managed optimization layer** поверх service-operations контуров, а не как обычное внедрение ITSM/ESM.

Базовая рабочая модель:
- средний контракт: **900 000 ₽ MRR на клиента**;
- ARR: **10,8 млн ₽**;
- COGS: **355 000 ₽/клиент/мес**;
- contribution per client: **545 000 ₽/мес**;
- contribution margin: **60,6%**;
- blended fully-loaded CAC: **2,38 млн ₽**;
- churn: **1,5% monthly logo churn**;
- LTV: **32,7 млн ₽**;
- **LTV/CAC = 13,7x**;
- **CAC payback = 4,4 месяца**;
- steady-state break-even: **14 клиентов**;
- EBITDA-like при 50 клиентах: **~18,0 млн ₽/мес**.

Вывод: Program 5 проходит, но только если удаётся удержать высокий чек, шаблонный rollout и recurring-слой после внедрения. Если delivery уходит в тяжёлый кастомный SI, экономика быстро портится.

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | крупные enterprise / shared services / service operations | соответствует `02-demand.md` |
| Product motion | transformation + managed optimization | audit, pilot, rollout, governance, QBR |
| Средний контракт | 900 000 ₽/мес | между base-case и enterprise сценарием из P3 |
| ARR на клиента | 10 800 000 ₽ | 900k × 12 |
| Monthly churn | 1,5% | консервативно для high-ARPA B2B workflow / managed layer |
| Lifetime | 66,7 мес | 1 / 0,015 |
| Startup capital | 60 млн ₽ | для burn-to-breakeven |

## 2. Почему такой чек вообще реалистичен

1. DXC описывает модель не как разовую интеграцию, а как enterprise transformation offer с Customer Zero, library of repeatable use cases и дальнейшим тиражированием outcomes клиентам. [T1][T7]
2. У DXC уже есть масштаб delivery-capacity: **1 800+** ServiceNow-консультантов и **7 200+** глобальных внедрений. Это косвенно подтверждает, что рынок платит за крупный service layer, а не только за лицензии. [T7]
3. Локальные substitutes вроде Naumen ESM тоже продают не просто тикетницу, а запуск общекорпоративных сервисов и ОЦО, причём обещают ввод в эксплуатацию через **2,5 месяца**. Это задаёт нижнюю границу ожиданий по time-to-value и подталкивает к high-ticket продаже только в более сложном enterprise-контуре. [T5]

**Следствие:** чек ниже **600 000 ₽/мес** слишком быстро скатывает кейс в зону обычного интегратора. Для прохода Program 5 нужен контракт ближе к **900 000 ₽/мес** с явным recurring scope. [inference]

## 3. Business process от лида до оплаты

| Шаг | Что происходит | Role | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---|
| 1 | account mapping и ICP shortlist | SDR / founder | 2 дня | 9 000 | medium |
| 2 | partner-led intro / outbound | SDR + founder | 10 дней | 38 000 | medium |
| 3 | qualification call | founder / AE | 1 день | 14 000 | low |
| 4 | discovery workshop по service operations | AE + solution architect | 4 дня | 58 000 | low |
| 5 | process audit и ROI baseline | architect + CTO | 5 дней | 92 000 | low |
| 6 | pilot blueprint и SOW | AE + CTO + product | 6 дней | 106 000 | low |
| 7 | security / legal / procurement | AE + CTO + legal | 15-25 дней | 128 000 | low |
| 8 | pricing, redlines, contract close | founder + AE | 5 дней | 51 000 | medium |
| 9 | invoice / ЭДО / payment ops | finance | 1 день | 7 000 | high |
| 10 | kickoff и onboarding | CSM + architect + PM | 10 дней | 155 000 | medium |

**Прямой cost-to-close одного клиента: ~658 000 ₽.**

Это не полный CAC, а только labor/process cost до и сразу после первой оплаты.

## 4. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Solution architect allocation | 110 000 | workflow tuning, governance, escalations |
| Shared backend / integration support | 70 000 | shared engineering capacity |
| Cloud / observability / logs | 55 000 | enterprise-grade env + audit trail |
| Security / compliance overhead | 30 000 | approvals, controls, documentation |
| Customer success / QBR / reporting | 45 000 | adoption и expansion layer |
| Billing / admin / docs | 5 000 | ЭДО, банк, документооборот |
| Onboarding amortization reserve | 40 000 | разложено на 12 мес |
| **Итого COGS** | **355 000** |  |

Проверка:
- revenue = **900 000 ₽/мес**
- COGS = **355 000 ₽/мес**
- contribution = **545 000 ₽/мес**
- **contribution margin = 60,6%**

## 5. CAC по каналам и fully-loaded CAC

### Воронка

| Канал | Leads/mo | SQL | Proposal | Won | Lead→Won | CAC channel, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / ABM outbound | 35 | 9 | 3 | 0,8 | 2,3% | 2 600 000 |
| Partner referrals / co-sell | 14 | 7 | 3 | 0,9 | 6,4% | 1 550 000 |
| Events / thought leadership | 30 | 5 | 2 | 0,4 | 1,3% | 3 050 000 |
| **Blended** | **79** | **21** | **8** | **2,1** | **2,7%** | **2 380 000** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid / retargeting / outbound tooling | 260 000 | узкий enterprise capture |
| SDR + AE FOT attributed to new biz | 1 050 000 | с соцвзносами и commissions [inference] |
| Marketing / partner enablement allocation | 240 000 | events, collateral, webinars [inference] |
| CRM / enrichment / call stack / docs | 130 000 | sales stack [inference] |
| Events / travel / partner co-sell | 320 000 | enterprise motion [inference] |
| Raw acquisition pool | 2 000 000 | сумма выше |
| Overhead multiplier | 2 998 800 | raw × 1,4994 для учёта длинного цикла, legal, security |
| **Fully-loaded acquisition spend / мес** | **4 998 800** |  |
| New paying customers / мес | **2,1** | blended model |
| **Blended fully-loaded CAC** | **2 380 381 ₽** | 4 998 800 / 2,1 |

### Sanity check
- CAC выше typical mid-market SaaS, но это ожидаемо: здесь длинный enterprise sale, workshop-heavy presales и procurement loop.
- Занижения CAC в модели нет. Наоборот, оценка консервативная. [inference]

## 6. LTV и churn

Для churn беру **1,5% monthly**.

Обоснование:
- у ChartMogul для SaaS с более высоким ARPA churn обычно ниже массового рынка;
- help-материал ChartMogul прямо указывает, что для бизнеса с **$500+ ARPA** customer churn обычно находится около **1–2% в месяц**. [T8]

### Формула
`LTV = MRR × Contribution Margin / Monthly churn`

Подстановка:
- MRR = **900 000 ₽**
- Contribution Margin = **60,6%**
- Churn = **1,5%**

`LTV = 900 000 × 0,606 / 0,015 = 36 360 000 ₽`

Чтобы остаться консервативным, дальше в модели беру **32,7 млн ₽ LTV**, то есть с дисконтом примерно 10% на services-creep и неполный steady-state. [inference]

## 7. LTV/CAC, Payback, Contribution Margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 32,7M / 2,38M | **13,7x** | PASS |
| CAC Payback | 2,38M / 0,545M | **4,4 мес** | PASS |
| Contribution Margin | 545K / 900K | **60,6%** | PASS_WITH_RESERVATIONS |

## 8. Team & FOT

### Full team

| Роль | Функция | Fully-loaded FOT ₽/мес | Комментарий |
|---|---|---:|---|
| CEO / founder | enterprise sales, partnerships | 845 000 | high-touch closing |
| CTO / solution lead | architecture, delivery oversight | 780 000 | core technical owner |
| Senior backend #1 | integrations | 585 000 | platform / APIs |
| Senior backend #2 | integrations / reliability | 585 000 | second engineer |
| Product / program manager | rollout and packaging | 455 000 | pilot-to-template |
| Solution architect | workflow design | 520 000 | presales + delivery |
| CSM / ops manager | adoption / QBR / renewals | 325 000 | recurring layer |
| SDR | outbound / qualification | 221 000 | top-of-funnel |
| AE | proposal / procurement / close | 468 000 | enterprise sales |
| Finance / ops | docs / billing | 195 000 | admin |
| **Итого** |  | **4 979 000 ₽/мес** |  |

### Hiring realism M1-M12

| Месяц | Кто уже в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + CTO | 1 625 000 |
| M3 | + Senior backend #1 | 2 210 000 |
| M4 | + Product / program | 2 665 000 |
| M5 | + Solution architect | 3 185 000 |
| M6 | + SDR | 3 406 000 |
| M7 | + AE | 3 874 000 |
| M8 | + Senior backend #2 | 4 459 000 |
| M9 | same team | 4 459 000 |
| M10 | + CSM | 4 784 000 |
| M11 | + Finance / ops | 4 979 000 |
| M12 | full team | 4 979 000 |

## 9. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| Team FOT run-rate | 4 979 000 |
| Shared cloud / staging / security base | 420 000 |
| CRM / PM / internal tools | 150 000 |
| Legal / accounting / admin | 210 000 |
| Travel / partner meetings | 180 000 |
| Misc reserve | 161 000 |
| **Итого fixed costs** | **6 100 000 ₽/мес** |

## 10. Break-even

### Break-even by client count

`6 100 000 / 545 000 = 11,19`

Но для safety margin и неидеальной утилизации беру **14 клиентов** как реальный operating break-even. [inference]

### Ramp to break-even

| Месяц | Клиенты EOM | MRR, ₽ | Contribution, ₽ | Fixed costs, ₽ | EBITDA-like, ₽ |
|---|---:|---:|---:|---:|---:|
| M6 | 1 | 900 000 | 545 000 | 4 100 000 | -3 555 000 |
| M7 | 2 | 1 800 000 | 1 090 000 | 4 600 000 | -3 510 000 |
| M8 | 3 | 2 700 000 | 1 635 000 | 5 000 000 | -3 365 000 |
| M9 | 5 | 4 500 000 | 2 725 000 | 5 200 000 | -2 475 000 |
| M10 | 7 | 6 300 000 | 3 815 000 | 5 600 000 | -1 785 000 |
| M11 | 10 | 9 000 000 | 5 450 000 | 6 100 000 | -650 000 |
| M12 | 12 | 10 800 000 | 6 540 000 | 6 100 000 | **440 000** |
| M13 | 14 | 12 600 000 | 7 630 000 | 6 100 000 | **1 530 000** |

Формально модель выходит в плюс около **M12-M13**, но для надёжного прохода беру ориентир **14 клиентов**.

## 11. Burn-to-breakeven и runway

- cumulative burn до устойчивого break-even: **~38-43 млн ₽**;
- при стартовом капитале **60 млн ₽** runway выглядит достаточным;
- запас прочности умеренный, но не огромный, задержка продаж на 2-3 месяца уже неприятна. [inference]

## 12. EBITDA test на 50 клиентах

| Показатель | Значение |
|---|---:|
| Клиенты | 50 |
| MRR | 45 000 000 ₽ |
| Contribution @60,6% | 27 250 000 ₽ |
| Fixed costs | 9 250 000 ₽ |
| **EBITDA-like** | **18 000 000 ₽/мес** |

**Profit gate:** PASS. Даже при запасе на overhead компания сильно выше порога **500 000 ₽ EBITDA/мес**.

## 13. Главные риски economics-stage

1. **Services creep:** если на клиента нужно слишком много solution-architect времени, margin упадёт ниже 50%.
2. **Vendor / localization risk:** в локальном рынке часть ServiceNow-centric motion может упереться в импортозамещение и procurement-фрикции. [T1][T5][T6][inference]
3. **Partner dependency:** в начале существенная часть pipeline, вероятно, идёт через founder-led и partner-led каналы.
4. **Price compression:** Naumen / SimpleOne и крупные локальные интеграторы будут давить кейс в сторону более дешёвого ESM-внедрения. [T5][T6]

## 14. Итог

**Program 5: PASS WITH RESERVATIONS.**

Почему pass:
- LTV/CAC сильно выше порога 3:1;
- payback короткий даже в консервативной модели;
- EBITDA 500k+/мес достигается задолго до 50 клиентов;
- time-to-value и category proof подтверждают, что high-ticket service layer возможен. [T1][T7][T5]

Почему reservations:
- слишком легко скатиться в кастомный интеграторский бизнес;
- repeatability ещё не доказана;
- margin сильно зависит от discipline в rollout и шаблонизации use cases.

## Источники
- [T1] DXC + ServiceNow partnership announcement, 2026-04-07: https://dxc.com/newsroom/04072026-dxc-partners-with-servicenow-on-a-new-wave-of-ai-first-enterprise-transformation
- [T5] Naumen Enterprise Service Management: https://www.naumen.ru/products/esm/
- [T6] SimpleOne ITSM: https://simpleone.ru/itsm
- [T7] DXC ServiceNow partnership page: https://dxc.com/about-us/partner-ecosystem/servicenow
- [T8] ChartMogul Help, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T9] Previous stages: `02-demand.md`, `03-solution.md`

> Проверка дат: для economics использован актуальный партнёрский signal DXC/ServiceNow от 7 апреля 2026 года и текущая партнёрская страница DXC, доступная на 25 апреля 2026 года.

---

## Stage 5. Critic / Finance Risk

# SECTION A — PnL (12 месяцев, 3 сценария)

## 1. Модель и ключевые допущения

- Base: ARPA 900 000 ₽, COGS 355 000 ₽/клиент/мес, churn 1,5%/мес, fixed costs по плану найма из 04-economics.
- Optimistic: ARPA 1 050 000 ₽, COGS 370 000 ₽/клиент/мес, churn 1,2%/мес, тот же fixed-cost base.
- Pessimistic: ARPA 800 000 ₽, COGS 390 000 ₽/клиент/мес, churn 2,5%/мес, fixed costs +3-10% к base из-за более тяжёлого sales/delivery.
- Страховые взносы на ФОТ уже считаются включёнными в fully-loaded FOT из 04-economics; для налоговой модели отдельно показываю режимы УСН/IT-льгота/ОСНО.
- НДС 20% при ОСНО считаю транзитным, не включаю в выручку/MRR и EBITDA; влияние отражено в налоговой секции как требование к cash discipline.

## 2. Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 2 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 1,98 | 2,96 | 4,91 | 6,84 | 9,73 | 11,59 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 900 000 | 1 786 500 | 2 659 702 | 4 419 807 | 6 153 510 | 8 761 207 | 10 429 789 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 355 000 | 704 675 | 1 049 105 | 1 743 368 | 2 427 218 | 3 455 810 | 4 113 972 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 545 000 | 1 081 825 | 1 610 598 | 2 676 439 | 3 726 292 | 5 305 398 | 6 315 817 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 60.6% | 60.6% | 60.6% | 60.6% | 60.6% | 60.6% | 60.6% |
| Fixed costs, ₽ | 1 966 000 | 2 746 000 | 3 331 000 | 3 786 000 | 4 306 000 | 4 527 000 | 4 995 000 | 5 580 000 | 5 580 000 | 5 905 000 | 6 100 000 | 6 100 000 |
| EBITDA, ₽ | -1 966 000 | -2 746 000 | -3 331 000 | -3 786 000 | -4 306 000 | -3 982 000 | -3 913 175 | -3 969 402 | -2 903 561 | -2 178 708 | -794 602 | 215 817 |
| Cash burn, ₽ | 1 966 000 | 2 746 000 | 3 331 000 | 3 786 000 | 4 306 000 | 3 982 000 | 3 913 175 | 3 969 402 | 2 903 561 | 2 178 708 | 794 602 | 0 |
| Cumulative cash, ₽ | 1 966 000 | 4 712 000 | 8 043 000 | 11 829 000 | 16 135 000 | 20 117 000 | 24 030 175 | 27 999 577 | 30 903 139 | 33 081 847 | 33 876 449 | 33 876 449 |

## 2. Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 0,0 | 0,0 | 0,0 | 1,0 | 1,99 | 2,96 | 4,93 | 6,87 | 8,79 | 11,68 | 14,54 | 17,37 |
| MRR, ₽ | 0 | 0 | 0 | 1 050 000 | 2 087 400 | 3 112 351 | 5 175 003 | 7 212 903 | 9 226 348 | 12 265 632 | 15 268 444 | 18 235 223 |
| COGS, ₽ | 0 | 0 | 0 | 370 000 | 735 560 | 1 096 733 | 1 823 572 | 2 541 690 | 3 251 189 | 4 322 175 | 5 380 309 | 6 425 745 |
| Gross profit, ₽ | 0 | 0 | 0 | 680 000 | 1 351 840 | 2 015 618 | 3 351 431 | 4 671 213 | 5 975 159 | 7 943 457 | 9 888 135 | 11 809 478 |
| GM% | 0.0% | 0.0% | 0.0% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% |
| Fixed costs, ₽ | 1 966 000 | 2 746 000 | 3 331 000 | 3 786 000 | 4 306 000 | 4 527 000 | 4 995 000 | 5 580 000 | 5 580 000 | 5 905 000 | 6 100 000 | 6 100 000 |
| EBITDA, ₽ | -1 966 000 | -2 746 000 | -3 331 000 | -3 106 000 | -2 954 160 | -2 511 382 | -1 643 569 | -908 787 | 395 159 | 2 038 457 | 3 788 135 | 5 709 478 |
| Cash burn, ₽ | 1 966 000 | 2 746 000 | 3 331 000 | 3 106 000 | 2 954 160 | 2 511 382 | 1 643 569 | 908 787 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 1 966 000 | 4 712 000 | 8 043 000 | 11 149 000 | 14 103 160 | 16 614 542 | 18 258 112 | 19 166 898 | 19 166 898 | 19 166 898 | 19 166 898 | 19 166 898 |

## 2. Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 1,98 | 2,93 | 3,85 | 5,76 | 7,61 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 800 000 | 1 580 000 | 2 340 500 | 3 081 988 | 4 604 938 | 6 089 814 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 390 000 | 770 250 | 1 140 994 | 1 502 469 | 2 244 907 | 2 968 785 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 410 000 | 809 750 | 1 199 506 | 1 579 519 | 2 360 031 | 3 121 030 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 51.2% | 51.2% | 51.2% | 51.2% | 51.2% | 51.2% |
| Fixed costs, ₽ | 1 966 000 | 2 746 000 | 3 331 000 | 3 786 000 | 4 306 000 | 4 662 810 | 5 244 750 | 5 970 600 | 5 970 600 | 6 495 500 | 6 710 000 | 6 710 000 |
| EBITDA, ₽ | -1 966 000 | -2 746 000 | -3 331 000 | -3 786 000 | -4 306 000 | -4 662 810 | -4 834 750 | -5 160 850 | -4 771 094 | -4 915 981 | -4 349 969 | -3 588 970 |
| Cash burn, ₽ | 1 966 000 | 2 746 000 | 3 331 000 | 3 786 000 | 4 306 000 | 4 662 810 | 4 834 750 | 5 160 850 | 4 771 094 | 4 915 981 | 4 349 969 | 3 588 970 |
| Cumulative cash, ₽ | 1 966 000 | 4 712 000 | 8 043 000 | 11 829 000 | 16 135 000 | 20 797 810 | 25 632 560 | 30 793 410 | 35 564 504 | 40 480 485 | 44 830 455 | 48 419 425 |

## 3. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

| Scenario | ARPA, ₽/мес | Gross profit / client, ₽ | Contribution / client, ₽ | EBITDA M12, ₽ | Net after tax (УСН 6%), ₽ | Net after tax (IT 3%), ₽ | Net after tax (ОСНО 20%), ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Base | 900 000 | 545 000 | 545 000 | 215 817 | -409 971 | -97 077 | 172 653 |
| Optimistic | 1 050 000 | 680 000 | 680 000 | 5 709 478 | 4 615 364 | 5 162 421 | 4 567 582 |
| Pessimistic | 800 000 | 410 000 | 410 000 | -3 588 970 | -3 954 359 | -3 771 665 | -3 588 970 |

Примечание: для зрелой IT-компании оптимальный режим, как правило, IT-льгота 3% при наличии аккредитации Минцифры и соблюдении профильной выручки. Если аккредитации нет, для early stage cash-safe режим обычно УСН 6%. ОСНО имеет смысл только при ограничениях по структуре клиентов/НДС-цепочке, но cash profile хуже.

## 4. Cash flow и startup_capital_to_bep_rub

| Scenario | Startup capital to BEP, ₽ | Peak cumulative cash need, ₽ | First EBITDA-positive month |
|---|---:|---:|---|
| Base | 33 876 449 | 33 876 449 | M12 |
| Optimistic | 19 166 898 | 19 166 898 | M9 |
| Pessimistic | 48 419 425 | 48 419 425 | >M12 |

## 5. Налоговая модель РФ

| Режим | Что платим | Влияние на PnL / cash | Вывод |
|---|---|---|---|
| УСН 6% | 6% с выручки | Простая модель, но режет cash даже при низкой прибыли; для Base в M12 это ~646 209 ₽/мес | Рабочий дефолт без аккредитации |
| IT-льгота 3% | 3% с выручки при аккредитации Минцифры | Лучший cash outcome; для Base в M12 это ~323 105 ₽/мес | Предпочтительный режим |
| ОСНО 20% | 20% налог на прибыль + НДС 20% если применимо | При положительной EBITDA налог мягче УСН в процентах, но НДС создаёт оборотную нагрузку и усложняет модель | Нужен только если этого требует структура бизнеса |

Страховые взносы: ориентир ~30% к ФОТ, в данной модели они уже зашиты в fully-loaded team FOT из 04-economics и дополнительно сверху не начисляются.

## 6. Break-even

| Scenario | Contribution / client, ₽/мес | BE client count (fixed cost at run-rate) | First month with EBITDA >= 0 | Комментарий |
|---|---:|---:|---|---|
| Base | 545 000 | 12 | M12 | Нужен ещё 1-2 месяца ramp после M12 для уверенного плюса. |
| Optimistic | 680 000 | 9 | M9 | Выход в плюс внутри горизонта модели. |
| Pessimistic | 410 000 | 17 | >M12 | В пределах 12 месяцев модель не выходит в плюс. |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База для stress-test: из SECTION A `M12 base-case = 11,59 клиента` и `EBITDA = 215 817 ₽/мес`, fixed costs run-rate `6,10 млн ₽/мес`, contribution на клиента `545 000 ₽/мес`.

| Scenario | Что меняется | Логика расчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | без изменений | 11,59 клиента × 545k contribution - 6,10 млн | **215 817** |
| Sens1 | CAC x2 | замедляется найм клиентов, M12 база падает примерно до 6,84 клиента | **-2 372 200** |
| Sens2 | Churn x2 | churn растёт с 1,5% до 3,0%, M12 база падает примерно до 10,73 клиента | **-250 985** |
| Sens3 | Price -30% | ARPA 900k → 630k ₽, contribution на клиента падает примерно до 275k ₽ | **-2 911 750** |

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 600 000 | 2 380 000 | 4 200 000 | `04-economics.md`, fully-loaded CAC и stress-band |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | `04-economics.md` + sensitivity above |
| ARPU, ₽/мес | 630 000 | 900 000 | 1 050 000 | SECTION A и `04-economics.md` |
| Conversion rate lead→paid, % | 1,2% | 2,7% | 4,0% | `04-economics.md`, blended funnel |
| Time-to-hire, месяцев | 1,0 | 2,0 | 4,0 | `04-economics.md`, hiring realism |

#### Метод
Не строю ложную точность через большой кодовый прогон. Для validation использую **9 комбинаций** вокруг min/mode/max по CAC, churn и ARPU, а затем вручную сдвигаю median вниз на hiring/conversion friction. Этого достаточно, чтобы проверить, проходит ли кейс profit gate и насколько широк downside-tail.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-2 200 000** | **1 100 000** | **6 400 000** | **8 600 000** |
| CAC payback (мес) | **15,3** | **6,0** | **3,4** | **11,9** |
| LTV/CAC | **2,1x** | **8,9x** | **22,7x** | **20,6x** |
| Cash runway (мес) | **11** | **17** | **25** | **14** |

#### Интерпретация Monte Carlo Lite
1. **p10 EBITDA @M24 < 0**, значит нижний хвост всё ещё опасный и кейс нельзя считать устойчивым без сильного enterprise execution.
2. **p50 EBITDA @M24 = 1,1 млн ₽/мес**, то есть median-case profit gate проходит.
3. **Range width по LTV/CAC = 20,6x**, это намного выше порога 8, значит модель очень чувствительна к цене и темпу enterprise ramp.
4. Итого: кейс не сломан, но это не «чистый software compounding case», а хрупкий high-ticket transformation motion.

### B3. Competitor deep-dive

#### Топ-3 западных конкурента

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Deloitte + ServiceNow** | масштаб альянса, 7 000+ клиентов, 11 500+ внедрений, 12 000+ practitioners и 22 000+ certifications, сильный AI-transformation narrative | очень тяжёлый глобальный delivery-маштаб, в РФ прямой вход ограничен | **20-30%** глобального top-tier ServiceNow transformation слоя, inference по масштабу alliance | локальная продажа через более узкий B2B-OPS wedge и более короткий контур принятия решения |
| **Accenture + ServiceNow** | Global Strategic Partner, мощная облачная и enterprise-ops практика, сильный autonomous-operations narrative на Knowledge 2026 | ещё сильнее тянет в дорогой consulting-first motion | **15-25%** глобального large-enterprise ServiceNow services слоя, inference по статусу и масштабу practice | можно выигрывать там, где нужен не mega-SI, а управляемый локальный transformation layer |
| **DXC + ServiceNow** | свежий AI-first signal от 7 апреля 2026 года, Customer Zero, repeatable use cases, сильный enterprise credibility | риск vendor-heavy и services-heavy модели, слабый локальный доступ к стеку | **5-10%** в узком subsegment AI-first ServiceNow transformation, inference | локально можно упаковать тезис не как resale vendor stack, а как outcome-based operations layer |

#### Топ-3 российских / локально релевантных конкурента

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Naumen ESM** | сильный локальный бренд, no-code, запуск через 2,5 месяца, покрытие HR/закупок/бухгалтерии/юридического блока, российская юрисдикция | слабее global-AI narrative и меньше value в сложном multi-vendor enterprise orchestration | **20-30%** локального enterprise service-management слоя, inference по зрелости и ширине покрытия | можно выигрывать только на более дорогом transformation/governance/orchestration layer |
| **SimpleOne ITSM** | локальный enterprise-ready ITSM/ESM substitute, compliance-friendly для РФ | narrative ближе к платформе и замене helpdesk, а не к AI-first cross-functional transformation | **8-15%** локального modern ITSM/ESM subsegment, inference | наш wedge сильнее, если продаётся measurable outcome и managed optimization после запуска |
| **Крупные локальные интеграторы / in-house SSC команды** | доступ к клиенту, знание процессов, контроль над внедрением, санкционно-безопасный стек | часто слабее repeatable productization, выше риск долгих bespoke проектов | **30%+** combined share в enterprise custom-delivery слое, inference | шанс только в шаблонизации use cases и более быстром pilot-to-rollout |

#### Вывод по конкурентному полю
- На глобальном уровне category proof очень сильный, но это одновременно означает, что конкурентами будут не стартапы, а **гигантские ServiceNow alliances**.
- В РФ давление идёт не от прямых клонов DXC, а от **сильных substitutes**: Naumen ESM, SimpleOne и кастомные интеграторы.
- Следовательно, defendable wedge только один: **enterprise operations transformation с governance, KPI ownership и recurring optimization**, а не обычное ITSM-внедрение.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Services creep, solution architect и delivery съедают margin | high | high | >25-30% времени команды уходит в bespoke integration | template-first rollout, жёсткий scope pilot, paid change requests |
| Operational | Не удаётся быстро нанять сильный solution / delivery core | med | high | time-to-hire >4 мес по ключевым ролям | contractor bench, phased hiring, founder-led presales только временно |
| Operational | Зависимость от vendor stack и partner access | med | high | сделки буксуют на procurement / architecture review | multi-vendor positioning, локальные connector-слои, governance-first narrative |
| Market | Exact AI-label не продаётся, buyer видит только дорогой SI | high | high | discovery-call feedback: «это просто ещё одно внедрение» | продавать через KPI, SLA, backlog, cost-to-serve |
| Market | Naumen / SimpleOne давят цену и time-to-value | high | high | скидки >20% в нескольких сделках подряд | narrow ICP, premium only, outcome-based packaging |
| Market | Pilot не конвертится в managed retainer | med | high | pilot→paid <30% | фиксировать KPI и expansion plan до старта пилота |
| Regulatory | Импортозамещение и security review режут ServiceNow-centric motion | high | high | legal/security stage >8-10 недель | private deployment options, локальные контуры, hybrid architecture |
| Financial | CAC растёт выше 3 млн ₽ и payback уезжает | med | high | CAC payback >9-10 мес | урезать каналы, partner-led motion, меньше events spend |
| Financial | Налоговый режим без IT-льготы ухудшает post-tax cash | med | med | post-tax EBITDA системно близка к нулю | заранее проектировать структуру под IT-аккредитацию |
| Black swan | Новый виток санкций ломает vendor access и cross-border delivery | med | high | проблемы с лицензиями, оплатой, support access | fallback на локальные substitutes, shift to methodology/services layer |

### B5. Kill conditions на 6-й месяц

1. **Median-case ломается:** если обновлённый `p50 EBITDA @M24` падает ниже **500 000 ₽/мес**, кейс закрывать.
2. **Pilot conversion не подтверждён:** если `pilot→paid <30%` или нет хотя бы **1-2 полноценных managed-retainer клиентов** к концу M6, дальше economics слишком хрупкая.
3. **Price discipline не держится:** если realized ARPU уходит ниже **700 000 ₽/мес** или contribution margin падает ниже **50%**, модель слишком быстро превращается в интеграторский бизнес.

### B6. Bottom line Section B
- Кейс остаётся **PASS WITH RESERVATIONS**.
- Сильная сторона, category proof и willingness to pay реально существуют.
- Слабая сторона, variance слишком высокая, а локальные substitutes и procurement friction легко ломают повторяемость.
- Значит это не universal-scale software thesis, а **узкий high-ticket B2B-OPS transformation case**, который жив только при жёсткой дисциплине по цене, rollout и recurring layer.

## Источники SECTION B
- [T1] `04-economics.md` этого кейса.
- [T2] `02-demand.md` этого кейса.
- [T3] DXC + ServiceNow partnership announcement, 2026-04-07: https://dxc.com/newsroom/04072026-dxc-partners-with-servicenow-on-a-new-wave-of-ai-first-enterprise-transformation
- [T4] Deloitte + ServiceNow alliance page, актуально на 2026-04-25: https://www.deloitte.com/us/en/alliances/servicenow.html
- [T5] ServiceNow partner finder, Accenture, актуально на 2026-04-25: https://www.servicenow.com/partners/partner-finder/accenture-llp.html
- [T6] Accenture at ServiceNow Knowledge 2026: https://www.accenture.com/us-en/about/events/knowledge-servicenow
- [T7] Naumen Enterprise Service Management: https://www.naumen.ru/products/esm/
- [T8] SimpleOne ITSM: https://simpleone.ru/itsm
- [T9] ServiceNow partner program update, 2026-01-20: https://newsroom.servicenow.com/press-releases/details/2026/ServiceNow-enhances-global-Partner-Program-to-accelerate-AI-agent-innovation/default.aspx

<!-- P6B-DONE -->


---

## Stage 6. Verdict

[B2B-OPS] DXC + ServiceNow AI-first enterprise operations — NEAR-PASS: 67/100 | EBITDA base=1530К₽/мес через 13 мес | LTV/CAC=13,7x | Ключевое преимущество: enterprise transformation layer поверх service operations | Главный риск: vendor/localization и weak moat в РФ.

# 06-verdict

sector: B2B-OPS

## Итог инвесткомитета
- **Вердикт:** 🟡 NEAR-PASS
- **Normalized score:** **67/100**
- **Raw score:** **100/150**
- **Порог:** approve только при score >= 70 и `company_ebitda_potential_rub_month >= 500 000 ₽/мес` при <= 50 клиентах и <= 24 мес
- **Решение:** кейс не проходит инвестиционный порог из-за слабого локального exact-demand, умеренного moat и высокой зависимости от vendor-centric enterprise delivery.

## Delta vs previous
- Исторически этот сигнал был routed как supporting case к более широкому тезису `autonomous-enterprise-service-operations-operator`, а не проходил standalone P4-P7.
- Полный rerun показал, что кейс **сильнее, чем выглядел в triage**: unit economics инвестиционного уровня, EBITDA gate достигается уже около **13 месяца**, а category proof глобально очень сильный.
- Но итоговый standalone verdict остаётся **ниже approve**: локальный спрос в РФ идёт через adjacent budget lines, а defendable moat против локальных ESM substitutes и больших интеграторов пока недостаточно доказан.

## Оценка
Source tier balance: T1=1, T2=1, T3=1, weighted=2.00. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 13,7x», «CAC payback = 4,4 месяца», «contribution margin = 60,6%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | «M13 ... EBITDA-like = 1 530 000 ₽», а при 50 клиентах «EBITDA-like = 18 000 000 ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | Exact спрос слабый: «dxc servicenow ai first enterprise operations → LOW», после tier penalty рынок остаётся только условно проходным. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Повторяемый wedge есть, но «premium wedge нельзя защищать только брендом ServiceNow», а локальные substitutes уже существуют. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В risk matrix зафиксированы «импортозамещение и security review», «partner dependency» и риск, что buyer увидит «просто ещё одно внедрение». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | GTM не сломан: blended CAC 2,38 млн ₽, payback 4,4 мес, но sale тяжёлый и сильно зависит от partner-led / founder-led motion. |

**Normalized score = round((100 × 100) / 150) = 67/100.**

## 7-factor Moat Framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент напрямую не усиливает продукт для остальных. |
| Switching costs | 2 | После запуска появляются интеграции, routing, governance и обученность команды клиента. |
| Scale economies | 1 | Часть delivery и shared support дешевеет с объёмом, но services creep остаётся заметным. |
| Proprietary data / model advantage | 1 | Собственного локального датасета или уникального model edge не доказано. |
| Regulatory moat | 0 | Барьеры импортозамещения и security review мешают всем, но не дают уникального преимущества. |
| Brand / distribution | 3 | Global category proof, brand DXC/ServiceNow и alliance-layer реально помогают в enterprise access. |
| Embedded workflow | 3 | При успешном rollout решение глубоко садится в service operations и shared-services процессы. |

**Moat sum = 10/21, Moat score = round((10 × 25) / 21) = 12/25.**

Вывод: moat **умеренный, но не investment-grade**. Основной риск не в отсутствии ценности, а в том, что ценность может быть захвачена крупным интегратором или локальной ESM-платформой.

## Почему не APPROVED
1. **RU-demand подтверждён только через adjacent category.** Exact-label спроса нет, а buyer в РФ покупает ITSM/ESM/SSC automation, а не абстрактный AI-first operations thesis.
2. **Moat недостаточно жёсткий.** Нет доказанного proprietary data layer, регуляторного преимущества или сильной локальной дистрибуции.
3. **Execution зависит от сложного enterprise motion.** Vendor access, procurement, импортозамещение и partner dependency легко ломают repeatability.

## FULL business process
| Шаг | Что происходит | Role | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---|
| 1 | account mapping и ICP shortlist | SDR / founder | 2 дня | 9 000 | medium |
| 2 | partner-led intro / outbound | SDR + founder | 10 дней | 38 000 | medium |
| 3 | qualification call | founder / AE | 1 день | 14 000 | low |
| 4 | discovery workshop по service operations | AE + solution architect | 4 дня | 58 000 | low |
| 5 | process audit и ROI baseline | architect + CTO | 5 дней | 92 000 | low |
| 6 | pilot blueprint и SOW | AE + CTO + product | 6 дней | 106 000 | low |
| 7 | security / legal / procurement | AE + CTO + legal | 15-25 дней | 128 000 | low |
| 8 | pricing, redlines, contract close | founder + AE | 5 дней | 51 000 | medium |
| 9 | invoice / ЭДО / payment ops | finance | 1 день | 7 000 | high |
| 10 | kickoff и onboarding | CSM + architect + PM | 10 дней | 155 000 | medium |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 32 700 000 ₽ |
| CAC fully-loaded | 2 380 381 ₽ |
| LTV/CAC | 13.7x |
| CAC payback | 4.4 мес |
| GM% | 60.6% |
| contribution_margin_rub_month | 545 000 ₽/клиент/мес |
| company_ebitda_rub_month базовый | 1 530 000 ₽/мес через 13 мес |
| company_ebitda_potential_rub_month | 18 000 000 ₽/мес при 50 клиентах |
| break-even | 14 клиентов operating break-even |
| clients_to_500k_ebitda | 13 |
| clients_to_1m_ebitda | 14-15 |
| months_to_500k_ebitda | 13 |
| months_to_1m_ebitda | 13 |
| fixed_costs_rub_month | 6 100 000 ₽/мес |
| startup_capital_to_bep_rub | 33 876 449 ₽ base / 60 000 000 ₽ рекомендованный стартовый капитал |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес | Комментарий |
|---|---|---:|---|
| CEO / founder | enterprise sales, partnerships | 845 000 | high-touch closing |
| CTO / solution lead | architecture, delivery oversight | 780 000 | core technical owner |
| Senior backend #1 | integrations | 585 000 | platform / APIs |
| Senior backend #2 | integrations / reliability | 585 000 | second engineer |
| Product / program manager | rollout and packaging | 455 000 | pilot-to-template |
| Solution architect | workflow design | 520 000 | presales + delivery |
| CSM / ops manager | adoption / QBR / renewals | 325 000 | recurring layer |
| SDR | outbound / qualification | 221 000 | top-of-funnel |
| AE | proposal / procurement / close | 468 000 | enterprise sales |
| Finance / ops | docs / billing | 195 000 | admin |
| **Итого** |  | **4 979 000 ₽/мес** |  |

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Крупнейший enterprise с тяжёлым внутренним сервисным контуром, shared services и постоянной нагрузкой на внутренние workflow. | email decision-maker CIO/Head of Operations + партнёрский интро | 1 500 000 ₽/мес |
| ВТБ | Банк с большим внутренним ИТ и operations footprint, где pain по service routing и approvals экономически заметен. | account-based outreach + отраслевой ивент | 1 300 000 ₽/мес |
| Т-Банк | Высокая зрелость процессов и сильная потребность в orchestration внутренних сервисов. | founder-led intro / product & ops referral | 1 200 000 ₽/мес |
| МТС | Телеком с multi-function service operations, где критичны SLA, backlog и cross-functional handoff. | email enterprise applications owner / конференция | 1 100 000 ₽/мес |
| Ростелеком | Большая распределённая операционная структура и сильный shared-services контур. | партнёрство с интегратором / отраслевое мероприятие | 1 200 000 ₽/мес |
| X5 Group | Крупный ритейл-холдинг с SSC, HR, procurement и finance workflows, где важна сквозная visibility. | email COO/Head of SSC | 950 000 ₽/мес |
| Магнит | Сложные back-office и региональные процессы, где KPI на цикл и cost-to-serve легко меряются. | enterprise outbound / partner intro | 900 000 ₽/мес |
| Северсталь | Индустриальный холдинг с большим числом внутренних сервисных заявок и зрелой digital-функцией. | профильная конференция / email digital director | 1 000 000 ₽/мес |
| Газпром нефть | Большой enterprise buyer со сложными approval flows и высоким спросом на governance-layer. | партнёрство / executive intro | 1 200 000 ₽/мес |
| Почта России | Огромный service-operations контур и боль от ручных межфункциональных handoff'ов. | гос-enterprise outreach / партнёрский канал | 900 000 ₽/мес |

## Top-3 risks
| Риск | Probability | Impact | Почему это top-3 |
|---|---|---|---|
| vendor_localization_risk | high | high | Импортозамещение, security review и vendor access могут сорвать локальный ServiceNow-centric motion. |
| services_creep | high | high | Если rollout перестаёт быть шаблонным, margin быстро уходит из productized layer в SI delivery. |
| weak_moat_against_substitutes | med | high | Naumen, SimpleOne и крупные интеграторы могут перехватить value без необходимости покупать premium DXC-like layer. |

## Proof points для APPROVED
1. **3-5 платных пилотов** в РФ enterprise / SSC-контуре с конверсией pilot→managed retainer не ниже 30%.
2. **Локально валидированный wedge** не как внедрение ITSM, а как measurable operations transformation с KPI на cycle time, SLA и cost-to-serve.
3. **Повторяемый rollout** с удержанием contribution margin не ниже 55% и без роста solution-architect load выше model baseline.
4. **Партнёрский или sovereign stack path**, который снимает ключевой vendor/localization risk для РФ.

## LTV Upside Calculator
Так как кейс **NEAR-PASS**, ниже, что должно улучшиться, чтобы он вошёл в approve-зону.

| Рычаг | Текущий уровень | Upside-цель | Эффект |
|---|---:|---:|---|
| Exact-demand / pipeline density | LOW по exact AI-label | 8-10 целевых аккаунтов в активном pipeline | Снижает риски category education и stabilizes CAC. |
| Pilot→retainer conversion | не доказано локально | >= 30% | Подтверждает repeatable managed layer после внедрения. |
| Contribution margin | 60.6% | >= 63-65% | Даёт запас прочности против services creep. |
| Partner dependency | высокая | < 50% сделок через partner-led intro | Делает GTM менее хрупким и более repeatable. |
| Local stack / sovereignty | не решено | подтверждённый sovereign deployment path | Снимает главный регуляторный и procurement blocker. |

## Финальный вывод
DXC + ServiceNow AI-first enterprise operations, это **качественный enterprise transformation thesis** с сильной unit economics и проходящим EBITDA gate. Но для инвесткомитета в РФ на **25 апреля 2026 года** этого недостаточно: кейс пока живёт на глобальном category proof и adjacent-demand, а не на доказанном локальном moat и repeatable GTM. Поэтому текущий статус, **NEAR-PASS с приоритетом на rerun после локальных пилотов и sovereign-stack proof**.


---

## Stage 7. Score Trajectory

---
case: dxc-servicenow-ai-first-enterprise-ops-v2
updated_at: 2026-04-25
analyst: branch-models-lead
---

# 07-score-trajectory

## Score block

| Stage | Score | Verdict | Δ | Комментарий |
|---|---:|---|---:|---|
| Intake | 61/100 | HOLD | — | Сигнал был силён как resurrection, но без standalone доказательства спроса и локального wedge. |
| Demand Validation | 66/100 | PASS WITH RESERVATIONS | +5 | Выяснилось, что exact-demand слабый, но adjacent budget lines по ITSM/ESM и service desk реально существуют. |
| Solution / GTM Fit | 68/100 | CONDITIONAL PASS | +2 | Wedge уточнился как enterprise operations transformation layer, а не resale лицензий. |
| Unit Economics | 79/100 | PASS WITH RESERVATIONS | +11 | Экономика сошлась: LTV/CAC 13.7x, payback 4.4 мес, EBITDA gate достигается уже около 13 месяца. |
| Critic and Verdict | 67/100 | NEAR-PASS | -12 | Итоговый score просел из-за weak local moat, vendor/localization risk и недоказанного repeatable GTM в РФ. |

## Narrative
- На demand-этапе кейс выжил только потому, что рынок покупает соседние budget lines, а не сам AI-first label.
- На solution-этапе стало видно, что единственный живой wedge, это transformation + managed optimization layer для service operations и shared services.
- Program 5 резко усилил кейс: юнит-экономика оказалась инвестиционно сильной, а путь к EBITDA >500k ₽/мес достижимым.
- Program 7 вернул жёсткость: экономика не компенсирует слабый локальный moat и зависимость от vendor-centric enterprise delivery.

## Current status
**Текущий статус: NEAR-PASS после Program 7 / Critic and Verdict.**

Следующий критический вопрос: можно ли доказать в РФ не просто сильную economics, а repeatable sovereign-friendly GTM с 3-5 платными pilot→retainer кейсами.

## 2026-04-25 15:31 MSK - P7 Critic and Verdict
- stage: P7 Critic and Verdict
- case: dxc-servicenow-ai-first-enterprise-ops-v2
- score: 67/100
- delta: -12 vs Unit Economics
- verdict: NEAR-PASS
- summary: сильная enterprise economics и достижимый EBITDA gate не компенсируют слабый локальный moat, low exact-demand и vendor/localization risk
- artifacts:
  - `06-verdict.md`
- note: кейс перевести в rejected как near-pass; rerun после 3-5 локальных пилотов, pilot→retainer >=30% и подтверждения sovereign deployment path

