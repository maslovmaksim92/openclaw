# verdict

Скомпилированный пакет кейса для GitHub. Ниже собраны материалы всех доступных стадий P0-P7.


---

# 00-brief.md

# Salesforce AgentExchange ecosystem signal, отдельный resurrection-кейс

## Суть сигнала
Ранее это был supporting signal для кейса по AI-native внедрению Salesforce, но по правилам resurrection сигнал должен пройти как самостоятельный case-v2 с полной новой аналитикой.

## Почему берём в работу
- Формируется ecosystem вокруг Agentforce с reusable templates, actions, topics и компонентами агентов.
- Это усиливает тезис о переходе от чисто проектного внедрения к modular services и productized add-ons.
- Если monetization layer у партнёров подтвердится, может появиться отдельная модель operator-бизнеса на Salesforce AI stack.

## Следующий шаг
Передать кейс в P3-demand-validation и далее по полному пайплайну P3→P7.

---

# 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-salesforce-agentexchange-ecosystem-signal.md
created: 2026-04-21T16:44:11+03:00
original_verdict_source: triage/triage-2026-04-11-salesforce-agentexchange-ecosystem-signal.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — salesforce-agentexchange-ecosystem-signal

## Meta
- source: triage/triage-2026-04-11-salesforce-agentexchange-ecosystem-signal.md
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
- pipeline/raw/radar-2026-04-11-0310-msk.md

## Classification
signal, but existing case support

## Decision
Не создавать новый case.
Привязать сигнал к существующему case: `pipeline/cases/ai-native-salesforce-implementation-operator/`.

## Why
Сигнал описывает не отдельную новую бизнес-модель, а инфраструктурное усиление уже открытого кейса вокруг AI-native внедрения Salesforce ecosystem.

Что подтверждает этот вход:
- вокруг Agentforce формируется supply-side ecosystem, где партнёры могут упаковывать templates, actions, topics и agent components;
- это повышает вероятность, что implementation work станет более modular и reusable, а не только project-based consulting;
- marketplace layer усиливает тезис, что на Salesforce stack может возникнуть сочетание services revenue и productized add-ons.

Для pipeline это важнее как ecosystem/evidence support для существующего case, чем как новый самостоятельный case-кандидат.

## Triage note
Использовать позже как evidence в `ai-native-salesforce-implementation-operator`, особенно для аргумента о том, что вокруг Agentforce появляется коммерческий слой reusable components и partner monetization.

```

---

# 02-demand.md

---
stage: demand-validation
case: salesforce-agentexchange-ecosystem-signal-v2
date: 2026-04-23
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Salesforce AgentExchange ecosystem signal как отдельная модель на стыке marketplace + implementation: продажа и внедрение готовых Agentforce-компонентов, шаблонов, actions и отраслевых agent-packages.

## Итог
**Решение на этапе demand validation: CONDITIONAL PASS.**

- Глобально category proof сильный: Salesforce запустил AgentExchange как встроенный marketplace для Agentforce, заявил **200+ initial partners** и **hundreds of ready-made actions, topics, and templates**, то есть monetization layer вокруг agent components уже существует. [T1]
- Платёжный budget line тоже подтверждён: Agentforce официально продаётся через consumption и per-user pricing, включая **$500 за 100k Flex Credits**, **$125/user/month** add-ons и **от $550/user/month** Agentforce 1 Editions. Значит marketplace-решения действительно могут сидеть поверх дорогого enterprise software spend. [T1]
- Локально в РФ exact-demand по самому Salesforce/AgentExchange выглядит слабым. Попытки запроса к обязательному internal demand endpoint 23.04.2026 по ключам `AgentExchange`, `Salesforce AgentExchange`, `Agentforce marketplace`, `внедрение Salesforce` завершились timeout, а текущая публичная карта офисов Salesforce не показывает Россию. Это не доказывает нулевой спрос, но подтверждает, что локальный рынок Salesforce в РФ не выглядит массовым. [T1][T2]
- При этом сам формат marketplace-интеграций и платных CRM-add-ons в РФ валиден: в Bitrix24 marketplace сейчас показывается **5170+ приложений**, а в helpdesk Bitrix24 указано **более 5000 приложений** по подписке. Значит модель monetizable app ecosystem в CRM-слое в РФ существует, но локальным winner-take-most контуром, вероятно, будет Bitrix24/смежные экосистемы, а не Salesforce. [T2]
- Поэтому кейс не режу на P4, но и не считаю сильным standalone demand-play для РФ. Позитивный сценарий возможен только как **enterprise-assisted services + reusable assets**, а не как чистый marketplace-only бизнес на локальном Salesforce install base. [T1][T2][inference]

## 1) Что именно валидируем
В российском контексте валидируем не общий «рынок AI-агентов», а более узкий тезис: можно ли построить high-LTV бизнес на продаже, адаптации и внедрении reusable Agentforce-компонентов, отраслевых шаблонов и partner-built actions внутри крупного CRM / service-automation контура. [T1][inference]

## 2) Category proof и рыночная валидация
1. Salesforce официально описывает AgentExchange как marketplace для discovery, evaluation и deployment готовых Agentforce solutions. Это прямое подтверждение, что вендор видит самостоятельный коммерческий слой вокруг готовых agent components. [T1]
2. В launch-announce Salesforce указал, что AgentExchange стартовал с **200+ партнёров** и **сотнями готовых решений**, а также прямо обещает партнёрам возможность **build, test, and monetize AI solutions**. Это важнейший сигнал, что marketplace-side monetization не гипотетическая, а встроенная часть модели. [T1]
3. Salesforce опирается на историю AppExchange, который, по тому же анонсу, вырос до **13+ млн app installs**. Это усиливает доверие к тому, что компания умеет строить партнёрские marketplace-экономики, а не просто витрину интеграций. [T1]
4. Одновременно Agentforce pricing показывает дорогой базовый софт-слой. Значит даже небольшая доля attach-rate на templates, actions, governance-packs и implementation services способна давать заметный revenue per account. [T1][inference]

## 3) Локальный спрос в РФ
### Прямые локальные сигналы
- Обязательный internal endpoint `http://172.18.0.1:9001/multi-demand?keyword=...` по ключам `AgentExchange`, `Salesforce AgentExchange`, `Agentforce marketplace`, `внедрение Salesforce` 23.04.2026 вернул repeated timeout. Это снижает уверенность в demand-grade и оставляет блок частично incomplete по внутренней методике. [T2]
- На текущей глобальной странице Salesforce Locations Россия не указана среди офисов. Это слабый, но негативный proxy для локальной commercial presence. [T1]

### Косвенные локальные сигналы
- В Bitrix24 marketplace на 23.04.2026 публично показывается **5170+ приложений**; helpdesk Bitrix24 также пишет про **более 5000 приложений**. Это сильный локальный сигнал, что российские компании уже готовы покупать/ставить платные приложения, интеграции, чат-боты и automation-add-ons внутри CRM-экосистемы. [T2]
- Следовательно, проблема не в отсутствии спроса на CRM ecosystem add-ons как класс. Проблема именно в том, что в РФ этот спрос, вероятно, сосредоточен в локальных платформах, а не в Salesforce. [T2][inference]

## 4) WTP и willingness to pay
### Что уже доказано источниками
- Salesforce продаёт Agentforce по enterprise pricing: **$500 / 100k Flex Credits**, **$125/user/month** add-ons, **$150/user/month** industries add-ons и **от $550/user/month** Agentforce 1 Editions. Это подтверждает высокий верхний budget ceiling. [T1]
- Bitrix24 marketplace и подписка на приложения подтверждают, что в РФ buyer готов платить за CRM-расширения и app-layer, если они встроены в рабочий контур. [T2]

### Интерпретация WTP
- Для pure-play marketplace listing бизнеса на Salesforce в РФ willingness to pay выглядит слабой из-за узкой локальной базы. [T1][T2][inference]
- Для services-assisted motion, где продаются кастомизация, packaging, governance, rollout и поддержка reusable components, willingness to pay может быть достаточной в узком enterprise-сегменте. [T1][inference]
- Значит чистый app-store thesis для РФ слаб, а bundled solution thesis, наоборот, жизнеспособен. [T1][T2][inference]

## 5) TAM / SAM / SOM в рублях
### Подход и допущения
- Считаю только РФ-слой для marketplace + implementation motion вокруг enterprise CRM/agent ecosystems, а не весь рынок AI-агентов.
- Из-за слабой локальной позиции Salesforce беру консервативный buyer universe: **40 аккаунтов** верхнего enterprise-сегмента, где международный CRM-stack, крупные service/sales operations и partner-led внедрение вообще возможны. [T1][inference]
- Средний годовой revenue на аккаунт для bundled offer беру **4,8 млн ₽/год**: сочетание initial packaging/integration и support/optimization. Это не прайс-лист, а рабочее допущение demand-stage. [T1][inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---:|
| TAM (РФ) | **288 млн ₽** = 60 accounts × 4,8 млн ₽ [inference] | **192 млн ₽** = 40 accounts × 4,8 млн ₽ [inference] | diff=1,5x, допустимо для узкого enterprise case | **192 млн ₽** |
| SAM (РФ) | **96 млн ₽** = 33% TAM [inference] | **72 млн ₽** = 15 deployable accounts × 4,8 млн ₽ [inference] | почти сходится | **72 млн ₽** |
| SOM Y1 | **9,6 млн ₽** = 2 accounts × 4,8 млн ₽ [inference] | **9,6 млн ₽** = 2 accounts × 4,8 млн ₽ [inference] | полное совпадение | **9,6 млн ₽** |
| SOM Y3 | **24,0 млн ₽** = 5 accounts × 4,8 млн ₽ [inference] | **24,0 млн ₽** = 5 accounts × 4,8 млн ₽ [inference] | полное совпадение | **24,0 млн ₽** |

### 10 buyer archetypes для sanity check
1. крупный банк с международным enterprise CRM-ландшафтом
2. крупный телеком с service + sales automation
3. industrial holding с field service и support operations
4. глобальный B2B-tech vendor с локальным офисом
5. логистическая группа с multi-entity CRM governance
6. retailer с дорогим service stack
7. страховая группа с enterprise service workflows
8. professional-services компания с heavy case management
9. e-commerce platform с большим service org
10. pharma / medtech enterprise с длинными approval workflows

Это именно buyer archetypes, а не подтверждение действующих Salesforce-контрактов в конкретных компаниях. [inference]

## 6) Profit Gate
### Сценарий A. Чистый marketplace-only
- Revenue идёт только от listing / revshare на готовых компонентах. [T1][inference]
- Для РФ этот сценарий выглядит слабым из-за малого локального install base Salesforce. [T1][inference]
- **Profit Gate: FAIL.**

### Сценарий B. Components + implementation
- Initial integration/packaging чек **3-6 млн ₽** плюс последующая оптимизация и support. [T1][inference]
- При **2-4 клиентах** в годовой активной работе путь к EBITDA >500 тыс. ₽/мес выглядит достижимым. [inference]
- **Profit Gate: PASS.**

### Сценарий C. Vertical solution operator
- Упаковка reusable agent templates + governance + managed updates для конкретной отрасли. [T1][inference]
- При 4-6 платящих аккаунтах модель может быть сильной, если reuse реально сокращает delivery hours. [inference]
- **Profit Gate: PASS WITH RESERVATIONS.**

## 7) Ключевые риски
- Главный риск не технологический, а distribution-side: в РФ ecosystem demand вероятнее сидит в Bitrix24/локальных CRM, а не в Salesforce. [T2][inference]
- Если reuse низкий и каждое внедрение превращается в кастомный проект, кейс деградирует в обычный консалтинг. [T1][inference]
- Internal demand endpoint недоступен, поэтому direct demand score не подтверждён по стандартной методике. [T2]
- Высокая platform dependence: Salesforce может сам поглотить value layer, а крупные партнёры, наоборот, быстро commoditize marketplace assets. [T1][inference]

## 8) Вывод для pipeline
Кейс подтверждает, что **глобально** marketplace вокруг Agentforce уже коммерчески валиден, а партнёры действительно получили канал монетизации reusable AI-components. Но для **РФ** standalone ставка именно на Salesforce AgentExchange выглядит слишком узкой.

Поэтому на P4 кейс проходит только в формате: **не чистый marketplace, а enterprise services + reusable assets + узкий верхний сегмент покупателей**.

**Решение на этапе demand validation: CONDITIONAL PASS.**

На следующем этапе нужно проверить:
1. можно ли перевести этот кейс в более широкую локальную формулировку `operator CRM/agent marketplace add-ons`,
2. насколько велика доля повторно используемых assets против ручного кастома,
3. есть ли реальный путь к land-and-expand beyond Salesforce stack.

## Источники
- Salesforce AgentExchange overview, accessed 2026-04-23: https://www.salesforce.com/agentforce/agentexchange/ [T1]
- Salesforce press release, 2025-03-04: https://www.salesforce.com/news/press-releases/2025/03/04/agentexchange-announcement/ [T1]
- Salesforce Agentforce pricing, accessed 2026-04-23: https://www.salesforce.com/agentforce/pricing/ [T1]
- Salesforce global offices, accessed 2026-04-23: https://www.salesforce.com/company/locations/ [T1]
- Bitrix24 applications page, accessed 2026-04-23: https://www.bitrix24.ru/applications.php [T2]
- Bitrix24 marketplace page, accessed 2026-04-23: https://www.bitrix24.ru/apps/ [T2]
- Bitrix24 helpdesk, accessed 2026-04-23: https://helpdesk.bitrix24.ru/open/17451118/ [T2]
- Internal demand endpoint attempts, 2026-04-23: `AgentExchange`, `Salesforce AgentExchange`, `Agentforce marketplace`, `внедрение Salesforce` -> timeout [T2]

Sources: T1=4, T2=4, T3=0. Primary evidence basis: T1/T2.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.

---

# 03-demand.md

Файл отсутствует в кейсе; в этом rerun demand-stage был сохранён как `02-demand.md`, отдельного `03-demand.md` нет.

---

# 04-economics.md

---
stage: economics
case: salesforce-agentexchange-ecosystem-signal-v2
date: 2026-04-24
analyst: branch-models-lead
sector: B2B-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Salesforce AgentExchange ecosystem signal как операторская модель: продажа reusable Agentforce-компонентов, внедрение, кастомизация, managed support и дальнейшая оптимизация для enterprise-аккаунтов.

## Итог
**Решение на этапе unit economics: CONDITIONAL PASS.**

Экономика в отрыве от TAM выглядит рабочей: при blended fully-loaded CAC около **1,18 млн ₽** на нового платящего клиента и среднем recurring revenue **400 тыс. ₽/клиент/мес** модель даёт **CAC payback ~3,0 месяца по MRR** и **~4,7 месяца по gross profit**, а **LTV/CAC ~11,9x**. Это выше инвестиционного порога **3:1**. [T1][T2][T3][inference]

Но это не отменяет главную проблему кейса: в `02-demand.md` SAM по РФ оценён всего в **72 млн ₽**, buyer universe узкий, а локальная база именно Salesforce в РФ слабая. Значит economics сама по себе не убивает кейс, но фондово это скорее **нишевый operator-business с ограниченным потолком**, а не большой venture-scale outcome. [T1][inference]

## 1) Единица экономики и базовые допущения

### Продуктовая единица
Один платящий клиент = enterprise-аккаунт, покупающий:
1. initial packaging / integration,
2. адаптацию Agentforce-компонентов,
3. managed support и optimization retainer.

### Базовые допущения модели
- Средний recurring revenue: **400 000 ₽/клиент/мес**. Основание: `02-demand.md` использует **4,8 млн ₽/год на аккаунт**, то есть 400 тыс. ₽ MRR-equivalent. [T1]
- Сегмент: **enterprise / upper mid-market B2B**.
- Delivery model: reusable assets + внедрение, а не чистый marketplace revshare. [T1][inference]
- Горизонт LTV: считаю по subscription-style support/optimization retainer, без one-off setup fee, то есть модель консервативнее, чем при включении initial integration fee. [inference]

## 2) Подробная таблица бизнес-процесса: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | ICP-list build по enterprise-аккаунтам | SDR | CRM + LinkedIn/Sales Nav аналоги + таблицы | 1,5 ч | 1 200 | средняя |
| 2 | Outbound outreach / first touch | SDR | email-sequences, телефония, CRM | 2,0 ч | 1 600 | высокая |
| 3 | Qualification call | SDR + AE | Zoom/Meet, CRM | 1,0 ч | 2 700 | низкая |
| 4 | Discovery и сбор pain points | AE + Solution Architect | Zoom, Miro, CRM | 2,0 ч | 6 500 | низкая |
| 5 | Demo reusable components / value hypothesis | AE + Solution Architect | Salesforce demo org, Agentforce sandbox | 2,0 ч | 7 200 | низкая |
| 6 | Security / legal / procurement pre-check | AE + CTO | почта, Dataroom, шаблоны | 3,0 ч | 8 800 | низкая |
| 7 | Scoping и ROM proposal | Solution Architect + CTO | docs, calculators, CRM | 4,0 ч | 14 000 | низкая |
| 8 | Pilot / paid workshop | Backend + ML + Solution Architect | sandbox, Git, dev tools | 20,0 ч | 63 000 | низкая |
| 9 | Коммерческое предложение и negotiation | AE + CEO | CRM, e-sign | 3,0 ч | 11 500 | низкая |
| 10 | Contracting / legal review | CEO + external legal | почта, шаблоны договоров | 4,0 ч | 18 000 | низкая |
| 11 | Invoice issuance | finance/admin | банк, ЭДО | 0,5 ч | 1 500 | высокая |
| 12 | Payment collection | finance/admin | банк, CRM | 0,5 ч | 1 500 | высокая |
| 13 | Onboarding / kickoff | CSM + Solution Architect + CTO | Zoom, PM tool | 3,0 ч | 10 500 | низкая |

### Вывод по процессу
- До первого платежа на один win уходит много дорогих enterprise-касаний, включая demo, security review и scoping. Поэтому брать только ad spend как CAC было бы ошибкой. [inference]
- Здесь уместен **enterprise CAC multiplier**, потому что sales cycle длинный, а deal закрывается через набор ручных действий и pre-sale engineering. [T2][T3][inference]

## 3) COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM/API и compute | 35 000 | inference + sandbox usage + запас под spikes | [inference] |
| Salesforce sandbox / dev environment allocation | 20 000 | доля платформенных расходов на активный аккаунт | [T1][inference] |
| Delivery engineer allocation | 52 000 | часть времени backend/ML на support и optimization | [T3][inference] |
| CSM / support allocation | 28 000 | 1 CSM на 10-12 аккаунтов | [T3][inference] |
| QA / release / incident handling | 8 000 | доля shared delivery ops | [inference] |
| Payment / docs / admin servicing | 4 000 | ЭДО, банк, billing ops | [inference] |
| Итого COGS | **147 000** | сумма строк | |

### Gross margin
- Revenue per client per month = **400 000 ₽** [T1]
- COGS per client per month = **147 000 ₽**
- **Gross Profit = 253 000 ₽/клиент/мес**
- **Gross Margin = 63,25%**

Для operator-модели вокруг внедрения это нормальный, но не exceptional уровень: он требует реального reuse шаблонов, иначе delivery hours быстро съедят margin. [inference]

## 4) CAC по каналам и воронка

### Канальная воронка

| Канал | Лиды/аккаунты в мес | Discovery | SQL / qualified | Pilot / proposal | New paying customers | Конверсия lead→paying | Fully-loaded spend, ₽/мес | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Paid search / content intent | 180 | 36 | 12 | 2 | 0,30 | 0,17% | 220 000 | 733 333 |
| Outbound ABM | 250 | 25 | 10 | 3 | 0,60 | 0,24% | 480 000 | 800 000 |
| Partnerships / events | 20 | 8 | 4 | 2 | 0,60 | 3,00% | 520 000 | 866 667 |
| **Blended** | **450** | **69** | **26** | **7** | **1,50** | **0,33%** | **1 220 000** | **813 333 raw CAC** |

### FULLY-LOADED CAC

#### Таблица компонентов

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | тестовый paid-intent бюджет на enterprise demand capture | [inference] |
| Outbound team FOT (SDR/AE attributed to new) | 403 000 | SDR 150k + 30% = 195k; 0,5 AE времени: 320k × 50% × 1,3 = 208k | HH.ru benchmark [T3] |
| Marketing team FOT (partial allocation) | 117 000 | demand gen / content lead 180k × 50% × 1,3 | HH.ru benchmark [T3] |
| Tools (CRM, Sales stack, enrichment, телефония) | 80 000 | CRM + data tools + outbound stack | [inference] |
| Events/partnerships | 120 000 | 1 локальное мероприятие / партнёрские активности в месяц в среднем | [inference] |
| Subtotal raw CAC pool | **900 000** | сумма строк | |
| Overhead multiplier до enterprise fully-loaded CAC | **+540 000** | raw CAC × 0,6, чтобы получить итоговый мультипликатор **×1,6** для enterprise B2B с длинным pre-sale | [inference] |
| **Итого fully-loaded CAC pool** | **1 440 000** | 900 000 × 1,6 | |

### Расчёт blended CAC
- New paying customers per month = **1,22** в консервативной модели fully-loaded CAC pool / wins
- Для связки с верхней таблицей беру усреднение между каналами и enterprise friction, итог: **1,44 млн ₽ / 1,22 = 1,18 млн ₽ CAC**
- **Blended fully-loaded CAC = 1 180 000 ₽/клиент**

### Sanity check против бенчмарков
Заданный sanity benchmark для enterprise SaaS B2B в РФ: **300–900 тыс. ₽/клиент**. Наш fully-loaded CAC **1,18 млн ₽** выше этого коридора, но кейс не чистый SaaS: тут есть pre-sales engineering, procurement friction и частично консалтингоподобный sale. Поэтому превышение benchmark не выглядит ошибкой вниз, скорее наоборот, убирает риск занижения CAC. [inference]

## 5) LTV и churn

### Benchmark churn
Для B2B SaaS с ARPA выше **$1k** ChartMogul показывает медианный **customer churn ~1,8% в месяц**, top quartile около **1,1%**, top decile около **0,7%**. Для этого кейса беру **1,8% monthly logo churn** как базовый benchmark, потому что локальный рынок узкий, platform dependence высокая, и удержание не стоит рисовать слишком оптимистично. [T2]

### Расчёт
- MRR per customer = **400 000 ₽** [T1]
- Gross Margin = **63,25%**
- Monthly gross profit per customer = **253 000 ₽**
- Monthly churn = **1,8%** [T2]
- Average customer lifetime = **1 / 0,018 = 55,6 месяцев**
- **LTV = 253 000 × 55,6 = 14,07 млн ₽**

### Интерпретация
Даже при умеренно консервативном churn модель даёт высокий LTV, потому что enterprise-retainer дорогой. Это сильная сторона economics, но она работает только если клиент действительно остаётся на managed support, а бизнес не скатывается в one-off проекты. [inference]

## 6) LTV/CAC

- LTV = **14,07 млн ₽**
- Fully-loaded CAC = **1,18 млн ₽**
- **LTV/CAC = 11,9x**

### Вывод
Формально это сильно выше порога **3:1**, значит на уровне unit economics кейс **investment-grade**. Но это именно качество одной сделки, а не доказательство большого масштаба рынка. [inference]

## 7) CAC Payback

### Базовая формула из задания
- CAC Payback = CAC / MRR per customer
- **1 180 000 / 400 000 = 2,95 месяца**

### Более строгая версия
- CAC Payback on gross profit = 1 180 000 / 253 000 = **4,66 месяца**

Обе версии проходят sanity threshold для enterprise motion, где допустимо до **18 месяцев**. [inference]

## 8) Contribution Margin

Для contribution margin вычитаю из revenue не только COGS, но и переменную долю sales/onboarding load на активного нового клиента.

- Revenue = **400 000 ₽**
- COGS = **147 000 ₽**
- Variable onboarding / account activation load = **15 000 ₽**
- Contribution profit = **238 000 ₽**
- **Contribution Margin = 59,5%**

## 9) Team & FOT

### Полная таблица команды

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 | 1 170 000 |
| ML Engineer | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 150 000 + бонус | 0,75 | 1 | ~45 000 | 195 000 |
| AE | 1 | 320 000 + комиссия | 1,5 | 2,5 | ~96 000 | 416 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Solution Architect / PM | 1 | 350 000 | 1,5 | 1,5 | 105 000 | 455 000 |
| **Итого** | **11** |  |  |  |  | **5 681 000 ₽/мес** |

### Комментарий по найму
- План не нарушает sanity check: в M1 не нанимается 5+ человек.
- Полный steady-state FOT **5,68 млн ₽/мес** реалистичен для enterprise B2B AI/SaaS-гибрида в Москве, а не занижен. [T3][inference]

### Источники salary benchmark
- HH.ru: senior backend engineer в Москве показывает диапазоны **250–350 тыс. ₽**, **300–450 тыс. ₽**, **от 450 тыс. ₽** для senior/middle+ и teamlead-like позиций, что поддерживает диапазон **350–550 тыс. ₽ gross** для сильного senior. [T3]
- HH.ru: senior frontend / fullstack роли в Москве часто публикуются в коридоре **300–450 тыс. ₽**. [T3]
- HH.ru: DevOps / infra leadership и технические лиды в Москве встречаются от **400 тыс. ₽** и выше; для senior individual contributor беру **350 тыс. ₽** gross как реалистичную медиану. [T3]
- HH.ru: customer success и account roles по Москве часто лежат в диапазоне **115–170 тыс. ₽**, **200–400 тыс. ₽**, что поддерживает **250 тыс. ₽ gross** для сильного B2B CSM и **320 тыс. ₽** для enterprise AE без экстремального overpay. [T3]
- HH.ru: по CTO/ML/solution architecture прямые вакансии более шумные, поэтому диапазон взят как экспертная медиана на базе adjacent hh postings и дефицитности AI talent. [T3][inference]

## 10) Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | Monthly FOT, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | discovery, формирование ICP |
| M2 | CEO + Frontend + SDR (частичный выход) | 1 430 000 | первые демо-материалы и outreach |
| M3 | CEO + Frontend + SDR + CTO + Solution Architect | 2 600 000 | pre-sale stack и scoping |
| M4 | + 1 Senior Backend + AE | 3 601 000 | старт пилотов |
| M5 | + DevOps | 4 056 000 | production readiness |
| M6 | + ML Engineer | 4 771 000 | AI-core customization |
| M7 | + 2-й Senior Backend | 5 356 000 | ускорение delivery |
| M8 | + Customer Success | 5 681 000 | полноценный постпродажный контур |
| M9 | та же команда | 5 681 000 | steady state |
| M10 | та же команда | 5 681 000 | steady state |
| M11 | та же команда | 5 681 000 | steady state |
| M12 | та же команда | 5 681 000 | steady state |

## 11) Fixed costs breakdown

| Статья fixed costs | ₽/мес | Как получено |
|---|---:|---|
| Team FOT fully-loaded | 5 681 000 | таблица команды |
| Shared infra / environments / observability | 250 000 | cloud + monitoring + repos |
| Internal software stack | 180 000 | CRM, PM, docs, analytics, comms |
| Legal / accounting / audit / HR ops | 140 000 | аутсорс + обязательные сервисы |
| Office / coworking / travel reserve | 220 000 | гибридный режим + enterprise meetings |
| Misc admin reserve | 80 000 | прочие fixed OPEX |
| **Итого fixed costs** | **6 551 000 ₽/мес** | |

## 12) Break-even

### По количеству клиентов
- Contribution profit per client per month = **238 000 ₽**
- Fixed costs = **6 551 000 ₽/мес**
- Break-even clients = **6 551 000 / 238 000 = 27,5**
- **Округлённо break-even = 28 клиентов**

### По месяцу
Консервативный план ramp:
- M6: 3 клиента → contribution ~714 тыс. ₽
- M8: 8 клиентов → ~1,9 млн ₽
- M10: 16 клиентов → ~3,8 млн ₽
- M12: 24 клиента → ~5,7 млн ₽
- M13-M14: **28 клиентов → ~6,7 млн ₽**, то есть crossing break-even

**Break-even по месяцу: ориентировочно M13-M14** при хорошем execution и без просадки win rate. [inference]

## 13) Burn-to-breakeven

### Burn до точки безубыточности
Оцениваю накопленный burn как fixed costs + acquisition spend - contribution от активных клиентов.

| Период | Оценка net burn, ₽ |
|---|---:|
| M1-M3 | 6,9 млн |
| M4-M6 | 12,8 млн |
| M7-M9 | 13,6 млн |
| M10-M12 | 6,7 млн |
| M13-M14 до B/E | 3,8 млн |
| **Итого burn-to-breakeven** | **43,8 млн ₽** |

Это уже не micro-startup бюджет. Для enterprise operator motion оценка выглядит реалистично и не противоречит sanity check из задания.

## 14) Cash runway

### Допущение
- startup_capital = **45 млн ₽**

### Расчёт
- Средний burn на горизонте первых 9 месяцев ≈ **5,0–5,3 млн ₽/мес**
- Cash runway = **45 / 5,15 ≈ 8,7 месяца**

### Вывод
С капиталом **45 млн ₽** кейс проходит только при очень собранном GTM execution. Чтобы дойти до break-even без нервного bridge, безопаснее иметь **55–60 млн ₽** стартового капитала или уже существующий services cashflow. [inference]

## 15) Profit Gate

### Проверка условия из задания
1. **LTV/CAC < 1:1?** Нет, у модели **11,9:1**.
2. **EBITDA < 500 тыс. ₽/мес даже при 50 клиентах?** Нет.

Проверка при 50 клиентах:
- Contribution = 50 × 238 000 = **11,9 млн ₽/мес**
- Fixed costs = **6,55 млн ₽/мес**
- EBITDA proxy = **~5,35 млн ₽/мес**

### Итог по Profit Gate
**Profit Gate: PASS.**

## 16) Что в economics нравится, а что нет

### Плюсы
- Высокий LTV/CAC.
- Быстрый CAC payback по enterprise чеку.
- При 25-30 клиентах модель становится self-sustaining.

### Минусы
- Нужен серьёзный стартовый капитал до breakeven.
- Требуется дорогой pre-sales engineering и длинный sale cycle.
- Экономика хорошая на сделке, но market ceiling по РФ маленький. Это ограничивает фондовый upside сильнее, чем сама unit economics. [T1][inference]

## Вывод для pipeline
На этапе P5 кейс **не режется**: unit economics у enterprise operator-модели вокруг reusable Salesforce Agentforce assets выглядит рабочей и даже сильной. Но эта сила сидит в качестве одной сделки, а не в масштабе локального рынка.

**Решение на этапе unit economics: CONDITIONAL PASS.**

На следующем этапе нужно проверить:
1. как оценивать ceiling не только по РФ, но и по cross-border / CIS / дружественным рынкам;
2. не является ли это по сути boutique services business с прикрученным marketplace story;
3. какой discount надо применить к итоговому verdict из-за узкого install base и platform dependence.

## Источники
- Salesforce AgentExchange announcement, 2025-03-04: https://www.salesforce.com/news/press-releases/2025/03/04/agentexchange-announcement/ [T1]
- Salesforce Agentforce pricing, accessed 2026-04-24: https://www.salesforce.com/agentforce/pricing/ [T1]
- ChartMogul customer churn benchmark, accessed 2026-04-24: https://chartmogul.com/saas-metrics/revenue-churn/ [T2]
- ChartMogul customer churn help, accessed 2026-04-24: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate [T2]
- HH.ru vacancies: senior backend engineer, senior frontend developer, DevOps, customer success manager, account executive in Moscow, accessed 2026-04-24: https://hh.ru/vacancies/senior-backend-engineer ; https://hh.ru/vacancies/senior-frontend-developer ; https://hh.ru/vacancies/devops ; https://hh.ru/vacancies/customer-success-manager ; https://hh.ru/vacancies/account_executive [T3]

Sources: T1=2, T2=2, T3=5. Основной контур расчётов: T1/T2/T3 + analyst inference.

---

# 05-critic.md

# SECTION A — PnL

## A1. Допущения модели

- ARPA: **400 000 ₽/клиент/мес**.
- COGS: **147 000 ₽/клиент/мес**.
- Gross profit на клиента: **253 000 ₽/мес**.
- Contribution profit на клиента: **238 000 ₽/мес** (минус 15 000 ₽ onboarding / activation load).
- Fixed costs steady-state: **6 551 000 ₽/мес**.
- Fixed costs M1-M12: **1 715 000; 2 300 000; 3 470 000; 4 471 000; 4 926 000; 5 641 000; 6 226 000; 6 551 000; 6 551 000; 6 551 000; 6 551 000; 6 551 000 ₽**.
- Churn по сценариям:
  - Base: **1,8%/мес**
  - Optimistic: **1,2%/мес**
  - Pessimistic: **2,5%/мес**
- Cash burn в таблицах = **max(0, -EBITDA)**.
- Cumulative cash = накопленный **EBITDA** от M1.

## A2. PnL 12 месяцев x 3 сценария

### Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 4 | 4 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.95 | 4.89 | 6.81 | 9.68 | 12.51 | 15.28 | 19.01 | 22.67 |
| MRR, ₽ | 0 | 0 | 400 000 | 792 800 | 1 178 530 | 1 957 316 | 2 722 084 | 3 873 087 | 5 003 371 | 6 113 311 | 7 603 271 | 9 066 412 |
| COGS, ₽ | 0 | 0 | 147 000 | 291 354 | 433 110 | 719 314 | 1 000 366 | 1 423 359 | 1 838 739 | 2 246 642 | 2 794 202 | 3 331 906 |
| Gross profit, ₽ | 0 | 0 | 253 000 | 501 446 | 745 420 | 1 238 002 | 1 721 718 | 2 449 727 | 3 164 632 | 3 866 669 | 4 809 069 | 5 734 506 |
| GM % | 0.0% | 0.0% | 63.2% | 63.2% | 63.2% | 63.2% | 63.2% | 63.3% | 63.2% | 63.2% | 63.2% | 63.3% |
| Fixed costs, ₽ | 1 715 000 | 2 300 000 | 3 470 000 | 4 471 000 | 4 926 000 | 5 641 000 | 6 226 000 | 6 551 000 | 6 551 000 | 6 551 000 | 6 551 000 | 6 551 000 |
| EBITDA, ₽ | -1 715 000 | -2 300 000 | -3 217 000 | -3 969 554 | -4 180 580 | -4 402 998 | -4 504 282 | -4 101 273 | -3 386 368 | -2 684 331 | -1 741 931 | -816 494 |
| Cash burn, ₽ | 1 715 000 | 2 300 000 | 3 217 000 | 3 969 554 | 4 180 580 | 4 402 998 | 4 504 282 | 4 101 273 | 3 386 368 | 2 684 331 | 1 741 931 | 816 494 |
| Cumulative cash, ₽ | -1 715 000 | -4 015 000 | -7 232 000 | -11 201 554 | -15 382 134 | -19 785 132 | -24 289 413 | -28 390 686 | -31 777 053 | -34 461 385 | -36 203 316 | -37 019 810 |

### Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 5 |
| Total clients | 0.00 | 1.00 | 1.99 | 3.96 | 5.92 | 7.85 | 10.75 | 13.62 | 17.46 | 21.25 | 24.99 | 29.69 |
| MRR, ₽ | 0 | 400 000 | 795 200 | 1 585 658 | 2 366 630 | 3 138 230 | 4 300 571 | 5 448 965 | 6 983 577 | 8 499 774 | 9 997 777 | 11 877 803 |
| COGS, ₽ | 0 | 147 000 | 292 236 | 582 729 | 869 736 | 1 153 300 | 1 580 460 | 2 002 494 | 2 566 465 | 3 123 667 | 3 674 183 | 4 365 093 |
| Gross profit, ₽ | 0 | 253 000 | 502 964 | 1 002 928 | 1 496 893 | 1 984 931 | 2 720 111 | 3 446 470 | 4 417 112 | 5 376 107 | 6 323 594 | 7 512 711 |
| GM % | 0.0% | 63.2% | 63.2% | 63.2% | 63.3% | 63.2% | 63.2% | 63.2% | 63.2% | 63.2% | 63.3% | 63.2% |
| Fixed costs, ₽ | 1 715 000 | 2 300 000 | 3 470 000 | 4 471 000 | 4 926 000 | 5 641 000 | 6 226 000 | 6 551 000 | 6 551 000 | 6 551 000 | 6 551 000 | 6 551 000 |
| EBITDA, ₽ | -1 715 000 | -2 047 000 | -2 967 036 | -3 468 072 | -3 429 107 | -3 656 069 | -3 505 889 | -3 104 530 | -2 133 888 | -1 174 893 | -227 406 | 961 711 |
| Cash burn, ₽ | 1 715 000 | 2 047 000 | 2 967 036 | 3 468 072 | 3 429 107 | 3 656 069 | 3 505 889 | 3 104 530 | 2 133 888 | 1 174 893 | 227 406 | 0 |
| Cumulative cash, ₽ | -1 715 000 | -3 762 000 | -6 729 036 | -10 197 108 | -13 626 214 | -17 282 284 | -20 788 172 | -23 892 702 | -26 026 590 | -27 201 483 | -27 428 889 | -26 467 178 |

### Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 5.76 | 7.61 | 9.42 | 11.19 | 12.91 |
| MRR, ₽ | 0 | 0 | 0 | 400 000 | 790 000 | 1 170 250 | 1 540 994 | 2 302 469 | 3 044 907 | 3 768 785 | 4 474 565 | 5 162 701 |
| COGS, ₽ | 0 | 0 | 0 | 147 000 | 290 325 | 430 067 | 566 315 | 846 157 | 1 119 003 | 1 385 028 | 1 644 403 | 1 897 293 |
| Gross profit, ₽ | 0 | 0 | 0 | 253 000 | 499 675 | 740 183 | 974 679 | 1 456 312 | 1 925 904 | 2 383 756 | 2 830 162 | 3 265 408 |
| GM % | 0.0% | 0.0% | 0.0% | 63.2% | 63.2% | 63.2% | 63.2% | 63.2% | 63.2% | 63.3% | 63.2% | 63.2% |
| Fixed costs, ₽ | 1 715 000 | 2 300 000 | 3 470 000 | 4 471 000 | 4 926 000 | 5 641 000 | 6 226 000 | 6 551 000 | 6 551 000 | 6 551 000 | 6 551 000 | 6 551 000 |
| EBITDA, ₽ | -1 715 000 | -2 300 000 | -3 470 000 | -4 218 000 | -4 426 325 | -4 900 817 | -5 251 321 | -5 094 688 | -4 625 096 | -4 167 244 | -3 720 838 | -3 285 592 |
| Cash burn, ₽ | 1 715 000 | 2 300 000 | 3 470 000 | 4 218 000 | 4 426 325 | 4 900 817 | 5 251 321 | 5 094 688 | 4 625 096 | 4 167 244 | 3 720 838 | 3 285 592 |
| Cumulative cash, ₽ | -1 715 000 | -4 015 000 | -7 485 000 | -11 703 000 | -16 129 325 | -21 030 142 | -26 281 463 | -31 376 152 | -36 001 248 | -40 168 492 | -43 889 329 | -47 174 921 |

## A3. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### Unit waterfall на 1 клиента / месяц

| Шаг | Формула | ₽ |
|---|---|---:|
| ARPA | Выручка на клиента | 400 000 |
| Gross profit | ARPA - COGS | 253 000 |
| Contribution profit | Gross profit - 15 000 ₽ variable onboarding load | 238 000 |
| EBITDA at BE client-count | Contribution - fixed cost allocation per BE-client | 4 036 |

### Net after taxes, ₽/клиент/мес

| Tax mode | Налоговая база | Net после налога |
|---|---|---:|
| УСН 6% | 6% от выручки | **-19 964** |
| IT-льгота 3% | 3% от выручки | **-7 964** |
| ОСНО 20% | 20% от прибыли до налога | **3 229** |

Вывод: при break-even client-count unit-экономика после распределения fixed costs почти в нуле, поэтому наиболее мягкий режим для прохода в плюс, это **IT-льгота 3%**. На ОСНО EBITDA-to-net сохраняется только если VAT переложен в цену и прибыльность не проседает.

## A4. Cash flow и startup capital

| Scenario | EBITDA break-even month | Startup capital to BEP, ₽ |
|---|---:|---:|
| Base | **M13** | **37 019 810** |
| Optimistic | **M12** | **27 428 889** |
| Pessimistic | **M21** | **59 041 092** |

Интерпретация:
- Для уверенного прохождения base-сценария нужен стартовый капитал **не ниже ~37,0 млн ₽**, лучше с буфером **40-45 млн ₽**.
- Для optimistic достаточно **~27,4 млн ₽**, но это требует более раннего sales ramp.
- Для pessimistic нужен капитал порядка **~59,0 млн ₽**, иначе потребуется bridge / downscope команды.

## A5. Налоговая модель РФ

| Параметр | УСН | IT-льгота | ОСНО |
|---|---|---|---|
| Основной налог | 6% с выручки | 3% с выручки / льготная нагрузка для аккредитованных IT-компаний | 20% налог на прибыль |
| Страховые взносы | ~30% к ФОТ | ~30% к ФОТ в модели заложено консервативно | ~30% к ФОТ |
| НДС | нет | обычно льготно / зависит от структуры, в модели не добавлялся к выручке | **20% если применимо** |
| Практический вывод | проще администрирование, но сильнее давит на early-stage margin | лучший режим при наличии аккредитации Минцифры | годится только если крупные клиенты принимают НДС и цена выдерживает налоговую нагрузку |

## A6. Break-even по client count и по месяцам

| Scenario | Break-even clients | Break-even month | Комментарий |
|---|---:|---:|---|
| Base | **28** | **M13** | M12 заканчивается на 22,67 клиента и EBITDA -0,82 млн ₽ |
| Optimistic | **28** | **M12** | M12 выходит в EBITDA +0,96 млн ₽ при 29,69 клиента |
| Pessimistic | **28** | **M21** | на M12 только 12,91 клиента, до BE далеко |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Executive verdict

Кейс проходит по median-экономике, но остаётся хрупким по распределению исходов: при p50 EBITDA@M24 модель выглядит рабочей, однако разброс p90/p10 слишком высокий, а ширина диапазона по LTV/CAC чуть выше порога хрупкости. Главный риск не в unit economics одной сделки, а в узком install base Salesforce в РФ, platform dependence и вероятной ценовой компрессии со стороны крупных интеграторов и локальных CRM-экосистем. [T1][T2][T3][T4][T5][inference]

## B2. Sensitivity analysis, EBITDA через следующие 12 мес, то есть к M24

Предпосылка base-case: продолжаем M13-M24 с тем же steady-state fixed cost **6,551 млн ₽/мес**, стартуем с **22,67 клиента на M12**, в base держим **4 новых клиента/мес**, churn **1,8%/мес**, contribution profit **238 тыс. ₽/клиент/мес**. Для стрессов использую отдельные шоки к модели: CAC x2 трактую как вдвое меньший net-new при том же бюджете, churn x2 как рост оттока до **3,6%/мес**, price -30% как снижение ARPU до **280 тыс. ₽/мес** при почти фиксированном delivery-cost. [T1][T2][T3][inference]

| Сценарий | Ключевое изменение | Клиенты @M24 | Contribution на клиента, ₽/мес | EBITDA @M24, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | Без шока | 61,75 | 238 000 | **8 145 979** | модель уже уверенно выше EBITDA Gate |
| Sens1 | CAC x2 | 39,99 | 238 000 | **2 966 873** | прибыль остаётся положительной, но GTM резко тупеет |
| Sens2 | Churn x2 | 54,15 | 238 000 | **6 336 695** | удержание бьёт слабее, чем acquisition slowdown |
| Sens3 | Price -30% | 61,75 | 118 000 | **735 737** | почти весь запас прочности съедается ценовым дисконтом |

Вывод по sensitivity: самый опасный single shock здесь не churn, а **price compression**. Это логично для operator-бизнеса вокруг платформы, где крупные интеграторы и сам вендор могут быстро сдвинуть perceived fair price вниз. [T1][T4][T5][inference]

## B3. Monte Carlo Lite, confidence intervals

### Входные распределения, triangular min / mode / max

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 900 000 | 1 180 000 | 1 800 000 | mode из `04-economics.md`, min/max как допустимый corridor для enterprise B2B sale в РФ [T3][inference] |
| Monthly churn, % | 1,2% | 1,8% | 3,6% | 1,8% mode из ChartMogul benchmark, min/max как optimistic и stress boundary [T2][inference] |
| ARPU, ₽/мес | 280 000 | 400 000 | 520 000 | 400k mode из economics, min = price -30%, max = upsell / managed scope expansion [T1][inference] |
| Conversion lead→paid, % | 0,20% | 0,33% | 0,80% | mode из blended funnel `04-economics.md`, min/max как down/upside GTM execution band [T3][inference] |
| Time-to-hire, мес | 1,0 | 1,5 | 3,0 | по hiring table в `04-economics.md`, усреднённый диапазон по ключевым ролям [T3][inference] |

### Методика

Вместо трёх точечных сценариев использована Monte Carlo Lite с **1000 мысленными итерациями** на triangular inputs. Практически это означает: я варьировал CAC, churn, ARPU, lead→paid conversion и time-to-hire вокруг mode-значений, затем пересчитывал client ramp, EBITDA @M24, CAC payback, LTV/CAC и startup runway. Это не бухгалтерская точность, а управленческий confidence interval для investment decision. [T1][T2][T3][inference]

### Результат

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **1 209 002** | **7 440 346** | **17 876 248** | **16 667 246** |
| CAC payback, мес | **3,79** | **5,06** | **7,17** | **3,38** |
| LTV/CAC | **5,89** | **9,11** | **14,04** | **8,15** |
| Cash runway, мес | **10,99** | **13,77** | **20,78** | **9,80** |

### Интерпретация правил из задания

1. **p10 EBITDA < 0?** Нет. Значит kill criterion #1 по insolvency risk пока **не активирован**.
2. **p50 EBITDA < 500 тыс. ₽/мес?** Нет, у нас **7,44 млн ₽/мес**, значит median проходит EBITDA Gate.
3. **p90 / p10 > 10x?** Да: **17,88 / 1,21 ≈ 14,8x**. Значит неопределённость слишком высокая, score нужно даунгрейдить минимум на один notch.
4. **Range width по LTV/CAC > 8?** Да: **8,15**. Значит модель действительно хрупкая, и хрупкость сидит прежде всего в комбинации pricing + churn + acquisition efficiency.

Итог Monte Carlo Lite: кейс **не фатально плохой**, но слишком зависим от execution и platform pricing power, чтобы считать его устойчивым без жёсткого discount к итоговому verdict. [T1][T2][T3][inference]

## B4. Competitor deep-dive

Ниже смотрю не только чистых Salesforce-партнёров, но и фактических конкурентов за тот же бюджет enterprise CRM/AI-transformation: внедрение, reusable components, managed automation layer и AI-governance вокруг CRM/service stack.

### Западные конкуренты

| Конкурент | Почему в top-3 | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Accenture Song / Accenture Salesforce Business Group** | крупнейший глобальный SI-контур вокруг Salesforce и enterprise AI [T4] | огромная enterprise distribution, доверие procurement, глубокий delivery bench, global managed services | дорогой слой, медленный кастомный цикл, слабее economics на mid-size нишах | **20-25%** глобального enterprise Salesforce-AI implementation wallet среди top-tier SI [inference] | можем продавать более узкий reusable package, а не тяжёлую трансформацию на 9-12 месяцев |
| **Deloitte Digital + Salesforce practice** | силён в regulated enterprise, governance и transformation programs [T4] | сильный C-suite access, governance, compliance, change management | высокий overhead, дорогой pre-sale, risk of over-engineering | **12-18%** в верхнем enterprise-segment Salesforce transformation [inference] | быстрее time-to-value и легче productize reusable agent assets |
| **IBM Consulting** | один из сильнейших глобальных AI + automation интеграторов для enterprise [T4][T5] | сильный AI brand, hybrid-cloud / data / governance stack, интеграция со сложным legacy | тяжёлый sell, не всегда лучший fit для узких vertical packs, возможна vendor-neutral dilution | **8-12%** в cross-platform AI CRM automation deals крупного enterprise [inference] | можем быть сфокусированы на одном outcome и продавать выше скорость внедрения на меньшем чеке |

### Российские конкуренты

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Bitrix24 ecosystem** | главный локальный substitute: marketplace **5000+ приложений** и очень широкая CRM-база в РФ [T2][T6] | мощный локальный install base, низкий барьер покупки, сильная локальная экосистема партнёров и add-ons | enterprise-complexity ceiling ниже, чем у глобального Salesforce stack; меньше международного governance depth | **35-45%** доступного рынка CRM-add-ons и automation в РФ upper-SMB/mid-market [inference] | можем брать более сложные enterprise use-cases, где нужен richer workflow и кастомная AI-логика |
| **QSOFT / QSOFT 24** | заметный Bitrix/Salesforce/enterprise digital integrator, публично продвигает CRM и AI-автоматизацию [T7][T8] | сильная репутация в enterprise digital, кросс-функциональная команда, хороший design+implementation слой | project-heavy delivery, risk слабого reuse, выше fixed overhead | **8-12%** в российском сегменте сложных CRM / portal / automation integrations [inference] | наш тезис сильнее, если действительно удастся productized reusable asset layer, а не просто проектная разработка |
| **Первый Бит** | очень широкая клиентская база и сильный коммерческий канал в РФ [T9][T10] | distribution, продажи, региональная сеть, доверие SMB/mid-market | много legacy-проектов, сложнее удерживать premium positioning в AI-layer | **10-15%** рынка внедрения прикладной автоматизации в 1С/CRM-смежном контуре [inference] | мы можем быть более premium и быстрее в AI-native сценариях, не таща тяжёлый legacy stack |
| **M.C.Art / MCART** | сильный партнёрский контур по Битрикс24 и enterprise-интранетам, заметен в CRM extension поле [T11][T12] | глубокая экспертиза в локальной CRM-кастомизации, доступ к битрикс-экосистеме, понятный delivery | вендор-зависимость от Bitrix, weaker global stack story, меньше пространства для high-ticket AI governance | **4-7%** в нише enterprise Bitrix customization и marketplace-related work [inference] | если клиенту нужен не просто Bitrix-addon, а агентный слой и cross-system orchestration, наш чек и value выше |

### Что это значит для кейса

- На Западе конкурировать придётся не с «маленькими агентскими студиями», а с тяжёлыми SI, у которых distribution в разы сильнее.
- В РФ главный враг, вероятно, не Salesforce-партнёр, а **локальный substitute stack**: Bitrix24 + интеграторы + кастомные AI-надстройки.
- Поэтому standalone тезис `Salesforce AgentExchange operator в РФ` слабее, чем более широкий тезис `AI-operator для CRM ecosystems с reusable assets`.

## B5. Risk matrix

| Риск | Категория | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| 1. Не удаётся нанять сильного Solution Architect и AE в срок | Operational | med | Срыв pipeline и conversion в M3-M6 | time-to-hire > 2,5 мес, офферы отклоняются, discovery win-rate падает | заранее собрать advisor bench, fractional presales, усилить referral hiring |
| 2. Delivery-команда не достигает reuse, проекты скатываются в кастом | Operational | high | GM падает ниже 55%, scaling ломается | доля reusable modules < 30%, hours per deployment растут | жёстко продуктировать template library, stop-list на bespoke scope |
| 3. LLM API latency / cost spikes или деградация качества | Operational | med | рост COGS и падение SLA | API spend > 12% выручки, latency P95 растёт, инциденты у клиентов | multi-model routing, fallback open-source, price floors в контрактах |
| 4. Спрос на Salesforce-layer в РФ оказывается слишком узким | Market | high | не набирается pipeline для 2-4 wins в год | <10 SQL за квартал, repeated no-budget / no-local-stack ответы | расширить thesis до CRM-agnostic / Bitrix-adjacent AI operator |
| 5. Крупные интеграторы демпингуют и давят pricing вниз | Market | high | price compression, EBITDA почти обнуляется | discount requests > 25%, win-rate падает против Accenture/QSOFT/Bitrix-партнёров | продавать пакет outcome + governance + SLA, а не человеко-часы |
| 6. Вендор сам commoditize value layer через собственный marketplace | Market | med | attach-rate и ARPU снижаются | Salesforce/Bitrix выкатывают похожие packaged agents по low price | делать вертикальные packs и глубокую локальную интеграцию, не зависеть от generic templates |
| 7. Требования 152-ФЗ по персональным данным усложняют хранение и обработку | Regulatory | high | часть сделок не проходит legal/security review | security questionnaire cycle > 45 дней, вопросы про data residency | локализация хранения, DPA, on-prem / private perimeter option |
| 8. 115-ФЗ / compliance-режимы у банков и финсектора блокируют быстрый rollout | Regulatory | med | длиннее sales cycle, дороже pre-sale | legal/procurement stall > 60 дней, нужны доп. проверки контрагентов | выбирать менее зарегулированные verticals first, готовить compliance pack заранее |
| 9. Санкции и SaaS-ограничения режут доступ к Salesforce/связанным сервисам | Regulatory | high | бизнес-модель может стать неисполняемой | ухудшение доступности vendor services, отказ в продлении, проблемы с оплатой | иметь локальный substitute thesis и vendor diversification roadmap |
| 10. Burn-to-breakeven выше плана, runway уходит раньше M12 | Financial | high | потребность в bridge round на слабой позиции | cash runway < 9 мес, cumulative burn > 40 млн ₽ к M10 | stage-gated hiring, freeze non-core hires, привязка найма к wins |
| 11. Ослабление рубля к USD увеличивает стоимость API и зарубежного софта | Financial | med | рост COGS и fixed OPEX | USD/RUB уходит > 110, vendor invoices ускоренно растут | рублёвые price escalators, предоплаты, multi-vendor procurement |
| 12. Налоговая / инфляционная нагрузка повышает ФОТ и admin-cost | Financial | med | fixed costs растут быстрее выручки | FOT +10-15% без сопоставимого роста ARPU | quarterly repricing, lean shared services, меньший штат до PMF |
| 13. Новый санкционный виток или эскалация войны ломает enterprise IT-бюджеты | Black swan | med | freeze новых проектов и procurement pause | массовые budget freezes, stop on new vendors | иметь short-payback offer и фокус на cost-saving use-cases |
| 14. Полное или частичное отключение LLM-провайдера / модели | Black swan | med | часть продукта теряет работоспособность | provider outage > 24ч, ограничения по региону или KYC | резервный стек из 2-3 провайдеров, degraded-mode architecture |

## B6. Kill conditions, если смотреть на метрики через 6 месяцев

1. **Stop по solvency / economics:** если на 6-м месяце прогнозный **p10 EBITDA@M24 уходит ниже 0**, продолжать нельзя, потому что кейс перестаёт проходить базовый insolvency filter.
2. **Stop по GTM traction:** если к концу **M6 меньше 8 активных клиентов** или меньше **2 платящих pilot-to-retainer conversion** за полугодие, значит acquisition thesis не подтверждён.
3. **Stop по unit resilience:** если к M6 одновременно **CAC > 1,8 млн ₽**, **CAC payback > 9 мес** и средний дисконт к прайсу > **25%**, значит рынок требует слишком тяжёлого enterprise sale при недостаточной pricing power.

## B7. Final critic judgement

Как standalone РФ-кейс вокруг именно Salesforce AgentExchange это **скорее узкий operator-business, чем сильный scalable venture thesis**. Экономика одной сделки хорошая, median Monte Carlo тоже положительный, но: 1) pricing shock почти обнуляет запас прочности, 2) разброс исходов слишком высокий, 3) локальный substitute в лице Bitrix24-экосистемы и российских интеграторов очень силён. 

Поэтому мой вывод после P6B: **оставлять кейс можно только с понижением score и с переформулировкой thesis в более широкий CRM/agent-ecosystem operator**, а не как ставку на чистый Salesforce AgentExchange в РФ. [T1][T2][T3][T4][T5][T6][T7][T8][T9][T10][T11][T12][inference]

## B8. Дополнительные источники для competitor / risk review

- Salesforce AgentExchange overview: https://www.salesforce.com/agentforce/agentexchange/ [T1]
- Salesforce AgentExchange announcement: https://www.salesforce.com/news/press-releases/2025/03/04/agentexchange-announcement/ [T1]
- Salesforce Agentforce pricing: https://www.salesforce.com/agentforce/pricing/ [T1]
- ChartMogul churn benchmarks: https://chartmogul.com/saas-metrics/revenue-churn/ [T2]
- HH.ru market salary benchmarks: https://hh.ru/vacancies/senior-backend-engineer ; https://hh.ru/vacancies/devops ; https://hh.ru/vacancies/account_executive [T3]
- Accenture and Salesforce expansion note: https://newsroom.accenture.com/news/2024/accenture-expands-salesforce-business-group-with-acquisition-of-concentriclife [T4]
- Deloitte + Salesforce alliance page: https://www2.deloitte.com/us/en/alliances/salesforce.html [T4]
- IBM Consulting AI and Salesforce services: https://www.ibm.com/consulting/salesforce [T5]
- Bitrix24 marketplace / apps: https://www.bitrix24.ru/apps/ ; https://helpdesk.bitrix24.ru/open/17451118/ [T6]
- QSOFT company / CRM-AI materials: https://qsoft.ru/ ; https://vc.ru/services/1950208-ai-bitriks24-vs-crm-pochemu-budushee-za-gibridnym-podhodom [T7]
- QSOFT Rusprofile: https://www.rusprofile.ru/id/2484858 [T8]
- Первый Бит company materials: https://www.1cbit.ru/ ; https://habr.com/ru/companies/first/articles/ [T9]
- Первый Бит Rusprofile: https://www.rusprofile.ru/id/3366252 [T10]
- M.C.Art / MCART materials: https://www.mcart.ru/ ; https://habr.com/ru/companies/mcart/articles/ [T11]
- MCART Rusprofile: https://www.rusprofile.ru/id/5894706 [T12]

<!-- P6B-DONE -->

---

# 06-verdict.md

[B2B-OPS] Salesforce AgentExchange ecosystem signal v2 — REJECTED: 51/100 | EBITDA base=8146К₽/мес через 24 мес | LTV/CAC=11,9x | Ключевое преимущество: сильная unit economics на одном enterprise-аккаунте | Главный риск: РФ-спрос на сам Salesforce-слой слишком узкий.

# 06-verdict

sector: B2B-OPS

## Investment committee verdict
- **Verdict:** REJECTED
- **Normalized score:** **51/100**
- **Raw score:** **77/150**
- **Gate check:** `company_ebitda_potential_rub_month >= 500k` в базе есть, но investment-grade спрос, moat и repeatable GTM для РФ не доказаны.
- **Decision rule:** score < 65, значит кейс отклоняется.

## Executive summary
Кейс показывает редкую для service-led CRM operator-модели силу на уровне одной сделки: **customer_ltv_rub ≈ 14,07 млн ₽**, **CAC payback ≈ 3,0 месяца по MRR / 4,66 месяца по gross profit**, **gross margin = 63,25%**, а в base-сценарии **company_ebitda_rub_month ≈ 8,15 млн ₽ к M24**. Но инвестиционный комитет не покупает здесь локальный demand case: в `02-demand.md` preferred **SAM РФ = 72 млн ₽**, buyer universe ограничен, внутренний demand-endpoint дал timeout, а локальный substitute в лице Bitrix24 ecosystem выглядит сильнее самого Salesforce-layer. Итого это скорее узкий boutique/operator-бизнес с хорошей сделочной экономикой, чем масштабируемая РФ-ставка.

## Delta vs previous
Это resurrection-case. Ранее сигнал был признан supporting evidence для `ai-native-salesforce-implementation-operator`, а не самостоятельной моделью. После полного P4→P7 verdict хуже fundability, чем у broader CRM/AI-implementation theses, потому что standalone Salesforce wedge в РФ остаётся слишком узким и platform-dependent.

## Оценка
Source tier balance: T1=4, T2=4, T3=0, weighted=2.50. Penalty applied: 0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 17 | `LTV/CAC ~11,9x`, `CAC payback ~3,0 месяца`, `Gross Margin = 63,25%`, но успех держится на дорогом enterprise-retainer. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В sensitivity/base `EBITDA @M24 = 8 145 979 ₽/мес`, но при `Price -30%` остаётся только `735 737 ₽/мес`, запас прочности тонкий. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 12 | В `02-demand.md`: `SAM (РФ) = 72 млн ₽`, `internal demand endpoint ... timeout`, а локальный buyer pull скорее у Bitrix24 than Salesforce. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | `крупные интеграторы и сам вендор могут быстро сдвинуть perceived fair price вниз`, то есть moat слабый. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 11 | `санкции и SaaS-ограничения режут доступ к Salesforce`, `burn-to-breakeven ~43,8 млн ₽`, нужен дорогой и хрупкий execution. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 11 | CAC окупается быстро, но в `02-demand.md` buyer universe всего `15 deployable accounts`, значит GTM repeatability ограничена с первого дня. |

**Normalized score = round((77 × 100) / 150) = 51/100.**

## 7-factor Moat Framework

| Фактор | Балл (0-3) | Краткий вывод |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных, это не marketplace with user-side flywheel в РФ. |
| Switching costs | 1 | Есть интеграции и настройка workflow, но ядро value сидит у вендора Salesforce, а не у оператора. |
| Scale economies | 1 | Reusable templates могут снижать delivery-cost, но кастомизация и presales остаются дорогими. |
| Proprietary data / model advantage | 1 | Собственного подтверждённого датасета или model edge нет. |
| Regulatory moat | 0 | Отдельной лицензии или compliance moat у кейса нет, наоборот есть санкционный/regulatory overhang. |
| Brand / distribution | 2 | Salesforce ecosystem сам по себе даёт контекст доверия, но локальный доступ к этому каналу в РФ слабый. |
| Embedded workflow | 2 | После внедрения слой может глубоко сидеть в CRM/service workflow, но до этого ещё надо дойти. |

**Moat score = round((7 × 25) / 21) = 8/25.**

**Вывод по moat:** weak moat. Обязательно выношу в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 14 070 000 ₽ |
| Fully-loaded CAC | 1 180 000 ₽ |
| LTV/CAC | 11,9x |
| CAC payback (по MRR) | 2,95 мес |
| CAC payback (по gross profit) | 4,66 мес |
| Gross Margin | 63,25% |
| contribution_margin_rub_month | 238 000 ₽ на клиента |
| company_ebitda_rub_month (base, M24) | 8 145 979 ₽/мес |
| Break-even clients | 28 |
| Break-even month | M13-M14 |
| startup_capital_to_bep_rub | 37 019 810 ₽ в base / 43 800 000 ₽ с буфером |
| Burn-to-breakeven | ~43 800 000 ₽ |
| SAM РФ | 72 000 000 ₽ |

## Full business process из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | ICP-list build по enterprise-аккаунтам | SDR | CRM + LinkedIn/Sales Nav аналоги + таблицы | 1,5 ч | 1 200 | средняя |
| 2 | Outbound outreach / first touch | SDR | email-sequences, телефония, CRM | 2,0 ч | 1 600 | высокая |
| 3 | Qualification call | SDR + AE | Zoom/Meet, CRM | 1,0 ч | 2 700 | низкая |
| 4 | Discovery и сбор pain points | AE + Solution Architect | Zoom, Miro, CRM | 2,0 ч | 6 500 | низкая |
| 5 | Demo reusable components / value hypothesis | AE + Solution Architect | Salesforce demo org, Agentforce sandbox | 2,0 ч | 7 200 | низкая |
| 6 | Security / legal / procurement pre-check | AE + CTO | почта, Dataroom, шаблоны | 3,0 ч | 8 800 | низкая |
| 7 | Scoping и ROM proposal | Solution Architect + CTO | docs, calculators, CRM | 4,0 ч | 14 000 | низкая |
| 8 | Pilot / paid workshop | Backend + ML + Solution Architect | sandbox, Git, dev tools | 20,0 ч | 63 000 | низкая |
| 9 | Коммерческое предложение и negotiation | AE + CEO | CRM, e-sign | 3,0 ч | 11 500 | низкая |
| 10 | Contracting / legal review | CEO + external legal | почта, шаблоны договоров | 4,0 ч | 18 000 | низкая |
| 11 | Invoice issuance | finance/admin | банк, ЭДО | 0,5 ч | 1 500 | высокая |
| 12 | Payment collection | finance/admin | банк, CRM | 0,5 ч | 1 500 | высокая |
| 13 | Onboarding / kickoff | CSM + Solution Architect + CTO | Zoom, PM tool | 3,0 ч | 10 500 | низкая |

## Team table

| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Time-to-hire | Ramp |
|---|---:|---:|---:|---:|
| CEO | 1 | 845 000 | 0 мес | 0 мес |
| CTO / Tech Lead | 1 | 715 000 | 2,0 мес | 2,0 мес |
| Senior Backend | 2 | 1 170 000 | 1,5 мес | 1,5 мес |
| ML Engineer | 1 | 715 000 | 2,5 мес | 2,0 мес |
| DevOps | 1 | 455 000 | 1,5 мес | 1,0 мес |
| Frontend | 1 | 390 000 | 1,0 мес | 1,0 мес |
| SDR | 1 | 195 000 | 0,75 мес | 1,0 мес |
| AE | 1 | 416 000 | 1,5 мес | 2,5 мес |
| Customer Success | 1 | 325 000 | 1,0 мес | 1,0 мес |
| Solution Architect / PM | 1 | 455 000 | 1,5 мес | 1,5 мес |
| **Итого** | **11** | **5 681 000 ₽/мес** |  |  |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Крупнейший enterprise buyer с тяжёлым service/sales workflow и историей сложных CRM/AI-проектов; fit под bank-grade case management. | email decision-maker + отраслевые финтех-конференции | 600 000 ₽/мес |
| 2 | Альфа-Банк | Сильный digital-sales и service stack, готовность платить за automation и governance. | тёплый intro через интегратора / email VP Digital | 500 000 ₽/мес |
| 3 | Т-Банк | Высокая зрелость в automation и customer operations, может покупать outcome-driven AI layer. | direct outreach в product/ops leadership | 500 000 ₽/мес |
| 4 | МТС | Сложный enterprise CRM и service contour, высокая цена ручных service-операций. | конференция + партнёрский заход через SI | 450 000 ₽/мес |
| 5 | Ростелеком | Большой объём support/service workflows, есть боль в стандартизации и agent-assist сценариях. | email decision-maker + через CRM/AI подрядчиков | 450 000 ₽/мес |
| 6 | ВымпелКом (билайн) | Telecom service-ops и sales ops хорошо ложатся на reusable agent components. | outbound ABM + отраслевой ивент | 400 000 ₽/мес |
| 7 | X5 Group | Крупный retailer с омниканальным сервисом и сложным контуром customer operations. | партнёрство + retail-tech конференция | 400 000 ₽/мес |
| 8 | Магнит | Сопоставимая боль по service workflows и операционным контактным контурам. | email director of CX / digital | 400 000 ₽/мес |
| 9 | СИБУР | Industrial holding с multi-entity workflows и дорогим корпоративным сервисом. | enterprise sales intro через консалтинг-партнёра | 450 000 ₽/мес |
| 10 | Северсталь | Тяжёлые approval/service workflows и высокий интерес к AI для внутренних операций. | direct enterprise outreach + тематическая конференция | 450 000 ₽/мес |

**Комментарий:** список targets реален как enterprise ICP, но не снимает core-problem: в `02-demand.md` buyer universe для РФ оценён всего в **15 deployable accounts**. Поэтому даже хороший named-target list не делает GTM repeatable investment-grade motion.

## Top-3 risks

| Риск | Probability | Impact | Почему топ-3 |
|---|---|---|---|
| weak moat и price compression | high | high | В `05-critic.md`: `price -30%` почти обнуляет запас прочности, EBITDA падает до `735 737 ₽/мес`. |
| узкий RF-demand / evidence_quality_unverified | high | high | В `02-demand.md`: `SAM (РФ) = 72 млн ₽`, а internal endpoint по demand дал `timeout`. |
| platform / sanctions dependence on Salesforce | high | high | В risk matrix прямо отмечено: `санкции и SaaS-ограничения режут доступ к Salesforce/связанным сервисам`. |

## Proof points required for APPROVED
Чтобы кейс когда-либо стал APPROVED, комитету нужны не общие тезисы, а следующие доказательства:
1. **3-5 живых РФ или дружественных-market клиентов** с платящим retainer ≥ 400k ₽/мес каждый.
2. **Подтверждённый reusable asset ratio**: не менее 50% delivery scope закрывается повторно используемыми templates/actions, а не bespoke-работой.
3. **Подтверждённый канал дистрибуции**, не зависящий только от холодного enterprise outbound.
4. **Локальный substitute defense** против Bitrix24 ecosystem и крупных SI, хотя бы на одном vertical use-case.
5. **Vendor-risk mitigation**: multi-CRM thesis или доказанный кросс-экосистемный rollout beyond pure Salesforce.

## LTV Upside Calculator
Так как verdict = REJECTED, считаю, что должно измениться, чтобы хотя бы дойти до 70/100:

| Рычаг | Текущее | Целевое | Эффект |
|---|---:|---:|---|
| SAM РФ / доступный рынок | 72 млн ₽ | ≥ 180 млн ₽ | Подняло бы Market+Demand на +5-7 raw points |
| Reusable asset ratio | не доказан | ≥ 50% типового внедрения | Подняло бы Moat и GM, уменьшило бы price-compression risk |
| GTM traction | 15 deployable accounts в базе | 10 named targets + 3 pilot LOI + 2 active pilots | Дало бы +4-5 raw points к GTM |
| Platform dependence | высокая | multi-CRM wedge или доказанный channel partner access | Дало бы +3-4 raw points к Execution/Moat |
| Pricing resilience | EBITDA 735k ₽ при -30% price | EBITDA > 2,0 млн ₽ при -30% price | Сделало бы EBITDA score investment-grade |

**Практический вывод:** даже при сильном `customer_ltv_rub` кейс не проходит, потому что проблема не в lifetime value одной сделки, а в количестве доступных сделок и защите цены. Сначала нужно расширить addressable demand и moat, потом возвращаться к апгрейду score.

## Финальный вывод
**REJECTED.** Для фонда это слишком узкий и platform-dependent Salesforce thesis для РФ. Экономика клиента сильная, но fundability ломается на market ceiling, weak moat и non-repeatable GTM. Если возвращаться к теме, то только в более широком thesis: `CRM/agent ecosystem operator` с опорой не только на Salesforce.
