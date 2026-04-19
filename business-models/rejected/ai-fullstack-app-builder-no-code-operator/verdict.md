# AI-first full-stack конструктор приложений по текстовому описанию
**Статус:** NEAR-PASS
**Итоговый балл:** 69/100
**Дата:** 2026-04-19
**Сектор:** GEO-EXPAND

---

## Этап 1 — Описание кейса

# Краткий бриф

## Дата открытия кейса
2026-04-18

## Кейс
AI-first full-stack конструктор приложений по текстовому описанию для фаундеров, SMB и продуктовых команд без собственной сильной разработки.

## Модель
Пользователь описывает продукт или внутренний сервис на естественном языке, после чего платформа генерирует интерфейс, backend, базовую бизнес-логику и позволяет быстро довести результат до рабочего MVP или production-light сценария. Локальная адаптация для РФ может строиться вокруг русскоязычного UX, шаблонов под типовые SMB-задачи, интеграций с российскими платёжками, auth, БД и хостингом.

## Почему это может быть интересно
- На западном рынке уже подтверждён массовый платёжный спрос на AI-first app builder категорию.
- В РФ сохраняется большой слой клиентов, которым нужен быстрый запуск MVP, лендингов, кабинетов, внутренних инструментов и micro-SaaS без найма полноценной команды разработки.
- Категория понятна по монетизации: подписка для соло-фаундеров, SMB, агентств и команд, плюс более дорогие командные и enterprise-тарифы.

## Сигналы экономики
- По входному сигналу Lovable достиг примерно 75 млн долларов ARR и 180 000+ платящих пользователей.
- Оценочный LTV/чек в локальном рынке может составлять примерно 60 000-180 000 ₽ в год на одного SMB/индивидуального пользователя и 300 000-1 200 000 ₽ в год на команду.
- Верхняя часть диапазона превышает порог Program 1 и допускает high-LTV сегмент через агентства, студии, внутренние продуктовые команды и SMB с повторным использованием.

## Предварительная гипотеза
Это не просто no-code, а отдельный AI-native слой создания цифровых продуктов, где ценность возникает из сокращения времени до запуска и снижения зависимости от дефицитной разработки. Если подтвердится спрос в РФ на создание внутренних сервисов и клиентских MVP «по описанию», кейс может быть интересен как массовый SMB-инструмент с возможностью апсейла в командный сегмент.

## Что проверить дальше
- Насколько в РФ уже заняты похожие сценарии локальными no-code платформами и AI-обвязками.
- Какие вертикали дают самый высокий чек: агентства, e-commerce, internal tools, micro-SaaS, образовательные продукты.
- Какие ограничения критичны для локального продукта: качество кода, деплой, интеграции, безопасность, vendor lock-in, сопровождение generated apps.

---

## Этап 2 — Проверка спроса

# 02-demand

## Кейс
`ai-fullstack-app-builder-no-code-operator`

## Дата проверки
2026-04-19 (Europe/Moscow)

## Сектор
GEO-EXPAND

## Итог этапа
PASS

## Composite demand
MEDIUM

## Почему не HIGH
Категория глобально уже доказана, но в РФ пока скорее выглядит как смесь `AI app builder + no-code + Telegram/mini-app builders`, а не как отдельный зрелый software-class с прозрачным локальным лидером.

Что не даёт поставить HIGH:
- mandatory endpoint `http://localhost:9001/multi-demand?keyword=...` в текущем рантайме вернул **Connection refused**;
- прямой российский Lovable/Bolt-class лидер с публичным traction не найден;
- локальный спрос лучше подтверждается через adjacent слой: чат-боты, mini apps, лендинги, конструкторы автоворонок и Telegram-first automation.

## LTV gate
PASS, но только для enterprise / agency / managed-build motion

## Проверка всех monetization scenarios

### 1) Solo founder / indie self-serve
- Якоря: Lovable Pro **$25/мес**, Bolt Pro **$25/мес**.
- В рублях по курсу ЦБ РФ на **2026-04-18**: около **1 901 ₽/мес**.
- Даже при годовом удержании это слишком низкий ARPU для fund-return profile.
- Вердикт: **FAIL**.

### 2) Team seat-based SaaS
- Якоря: Bolt Teams **$30/user/month**, v0 Team **$30/user/month**, v0 Business **$100/user/month**.
- В рублях: примерно **2 282 ₽/user/month** и **7 605 ₽/user/month**.
- Даже команда из 20 пользователей на v0 Business даёт около **152 тыс. ₽/мес**, что всё ещё ниже порога.
- Вердикт: **FAIL** как standalone SaaS tier.

### 3) SMB subscription + credits + hosting
- Якоря: Lovable Business **$50/мес**, Bolt Pro/Teams, upsell через usage, domains, hosting, rollovers.
- Это уже лучше, но публичные self-serve планы всё равно находятся в low-ticket диапазоне.
- Вердикт: **FAIL** без крупного volume expansion.

### 4) Agency / studio workspace
- Логика: один аккаунт может вести много клиентских MVP, лендингов, кабинетов и внутренних tools.
- При продаже как productized service возможен чек **80-250 тыс. ₽/мес** на агентство или digital studio.
- Это уже интересно, но всё ещё ниже жёсткого порога **500 тыс. ₽/мес** на одного клиента.
- Вердикт: **PARTIAL / чаще FAIL**.

### 5) Enterprise private deployment / internal app factory
- Для крупных компаний, банков, ритейла, интеграторов и внутренних product/platform teams можно продавать не просто подписку, а `secure AI app factory`: private deployment, RBAC, audit, templates, integrations, SLA, governance, сопровождение generated apps.
- Реалистичный enterprise диапазон для РФ: **600 тыс. - 1,2 млн ₽/мес** на клиента при managed rollout и нескольких внутренних use cases.
- Вердикт: **PASS**.

## GEO-EXPANSION
YES

## Обоснование GEO
На Западе категория уже доказана публичными app-builder игроками с понятным pricing и сильным usage signal. В РФ нет очевидного зрелого AI-native лидера именно в классе `generate full-stack app from prompt`, зато есть развитый adjacent слой Telegram/no-code/chatbot/mini-app продуктов. Это создаёт окно не для pure self-serve копии, а для локализованного enterprise/agency wedge.

## Сигналы спроса

### 1) Mandatory demand endpoint
Проверялись запросы:
- `ai app builder`
- `конструктор приложений ai`
- `no-code ai app builder`
- `telegram mini app constructor`

Результат:
- `http://localhost:9001/multi-demand` в текущем рантайме недоступен;
- техническая ошибка: **connection refused**;
- exact local demand datapoint по обязательному источнику **не получен**.

### 2) Реальные конкуренты с ценами
Для конвертации USD использован курс ЦБ РФ на **2026-04-18**: **1 USD = 76.0535 ₽**.
Источник: `https://www.cbr-xml-daily.ru/daily_json.js`

#### Direct global competitors
1. **Lovable**
   - Pro: **$25/мес ≈ 1 901 ₽/мес**
   - Business: **$50/мес ≈ 3 803 ₽/мес**
   - Enterprise: custom
   - Источник: `https://lovable.dev/pricing`

2. **Bolt.new**
   - Pro: **$25/мес ≈ 1 901 ₽/мес**
   - Teams: **$30/user/month ≈ 2 282 ₽/user/month**
   - Enterprise: custom
   - Источник: `https://bolt.new/pricing`

3. **v0 by Vercel**
   - Team: **$30/user/month ≈ 2 282 ₽/user/month**
   - Business: **$100/user/month ≈ 7 605 ₽/user/month**
   - Enterprise: custom
   - Источник: `https://v0.dev/pricing`

Вывод по pricing landscape:
- глобальный рынок уже нормализовал pricing на уровне **$25-100 за пользователя/месяц**;
- низкий и средний слой сильно коммодитизируется;
- fund-level economics собираются только через enterprise controls, private deployment, security и managed adoption.

### 3) Telegram / RU services check
Прямого Telegram-native аналога уровня Lovable/Bolt в РФ публично не найдено. Но найден сильный adjacent слой, который закрывает low-end часть job-to-be-done и будет давить на рынок снизу.

1. **Salebot**
- позиционирование: чат-боты, сайты, интернет-магазины, CRM, ИИ для ответов клиентам;
- публичные цены: **0 ₽**, **2 999 ₽/мес**, **3 999 ₽/мес**;
- заявляет **15 000+ компаний** и **120 000 000+ клиентов**, взаимодействующих через платформу.
- Источник: `https://salebot.pro/#tariff`

2. **Botmother**
- позиционирование: конструктор ботов для мессенджеров;
- публичные цены: **$49/мес**, **$159/мес**, **$169/мес**;
- это примерно **3 727 ₽**, **12 093 ₽**, **12 853 ₽** в месяц.
- Источник: `https://botmother.com/price`

3. **LeadConverter**
- позиционирование: чат-боты для Telegram/VK/MAX + mini-landings + AI integration;
- публично видимый free tier: **0 ₽/мес**, AI integration декларируется как настройка за ~5 минут;
- важен как признак того, что локальный рынок уже привык к быстрому no-code / bot-first созданию цифровых сценариев.
- Источник: `https://leadconverter.ru/tariffs`

Интерпретация:
- в РФ есть реальный спрос на быструю сборку digital workflows без команды разработки;
- но низ рынка уже занят более дешёвыми Telegram/chatbot builders;
- значит новый игрок не должен стартовать как “ещё один дешёвый конструктор”, иначе pricing pressure будет слишком сильным.

### 4) Proof of willingness to pay
WTP подтверждён, но основной платящий слой раздваивается.

Что подтверждено:
1. **Global self-serve WTP**
   - Lovable, Bolt и v0 открыто продают платные планы.
2. **Global category traction**
   - во входном brief зафиксирован strong signal: Lovable на уровне **~$75 млн ARR** и **180 000+ paying users**.
3. **Enterprise workflow WTP**
   - OpenAI пишет про Rogo, что платформа обслуживает **5 000+ bankers**, а ARR вырос в **27 раз**; это другой вертикальный рынок, но это сильный сигнал, что дорогостоящие professionals готовы платить за AI, встроенный в ежедневный workflow.
4. **RU behavior proof**
   - Salebot заявляет **15 000+ компаний**, то есть российский SMB-рынок уже платит за конструкторы, автоматизацию и low-code инфраструктуру.

Что это не доказывает:
- не видно публичного доказательства, что в РФ уже есть массовый self-serve спрос именно на full-stack prompt-to-app builder;
- low-end слой доказан лучше, чем premium app-factory слой.

### 5) TAM / SAM / SOM в рублях
Ниже bottom-up модель. Часть расчёта является **inference**, а не прямой официальной статистикой.

#### База для расчёта
- В Едином реестре субъектов МСП числится около **6,7 млн** субъектов малого и среднего предпринимательства в РФ.
- Для TAM беру только **5%** от этой базы как сегмент, у которого регулярно возникает потребность в быстрых MVP, личных кабинетах, внутренних инструментах, витринах, mini-apps и автоматизации.
- Это даёт **335 000** потенциальных buyer-units.
- Для blended annual spend беру **120 000 ₽/год** на один аккаунт или команду. Это выше Telegram/chatbot low-end, но ниже тяжёлого enterprise проекта.

#### TAM
- **335 000 × 120 000 ₽/год = 40,2 млрд ₽/год**.

#### SAM
- Беру **15%** TAM как реально достижимый цифрово-зрелый сегмент: агентства, e-commerce SMB, EdTech, сервисные бизнесы, product teams, внутренние automation-heavy команды.
- Это **50 250** buyer-units.
- **50 250 × 120 000 ₽/год = 6,03 млрд ₽/год**.

#### SOM
- Беру 3-летний реалистичный захват **500 клиентов**.
- Для SOM использую более высокий blended ACV **240 000 ₽/год**, так как целевой entry-point должен быть выше массового low-end и включать шаблоны, hosting, support и integrations.
- **500 × 240 000 ₽/год = 120 млн ₽/год**.

#### Вывод по размеру рынка
- **TAM: 40,2 млрд ₽/год**
- **SAM: 6,0 млрд ₽/год**
- **SOM: 120 млн ₽/год**

Это уже выглядит достаточно крупно для venture-scale категории, но только если брать не массовый freemium-конструктор, а продукт с выходом в более дорогой SMB/team/enterprise сегмент.

## Сводка по demand verdict

### Demand
**MEDIUM**

### Почему PASS
- глобальная категория уже платёжеспособна;
- есть минимум 3 реальных конкурента с публичным pricing;
- в РФ существует сильный adjacent Telegram/no-code/service layer;
- buyer-job повторяемый: быстро собрать MVP, кабинет, внутренний инструмент, mini-app, воронку, automation;
- TAM/SAM/SOM в рублях достаточно велики для fund-level интереса.

### Почему не HIGH
- mandatory demand endpoint недоступен;
- российский прямой category leader не найден;
- low-end рынка уже сильно занят дешёвыми substitutes;
- большая часть публичного pricing сегодня лежит в low-ticket диапазоне.

## Финальный вывод
Кейс **проходит demand-stage** как **MEDIUM demand / GEO-EXPAND** opportunity.

Инвестиционный смысл есть только в позиции `AI app factory`, а не в копировании low-end self-serve тарифов Lovable/Bolt. В РФ low-end будет сдавлен Telegram- и chatbot-конструкторами, а fund-return profile появляется только при enterprise / agency / managed deployment motion, где продаются безопасность, приватный контур, шаблоны, интеграции и сопровождение generated apps.

## Источники
- Lovable pricing: `https://lovable.dev/pricing`
- Bolt pricing: `https://bolt.new/pricing`
- v0 pricing: `https://v0.dev/pricing`
- OpenAI / Rogo case: `https://openai.com/index/rogo/`
- Salebot tariffs: `https://salebot.pro/#tariff`
- Botmother price: `https://botmother.com/price`
- LeadConverter tariffs: `https://leadconverter.ru/tariffs`
- Курс USD/RUB ЦБ РФ: `https://www.cbr-xml-daily.ru/daily_json.js`

## Ограничения прохода
- `localhost:9001/multi-demand` недоступен из рантайма, exact local demand datapoint не получен.
- TAM/SAM/SOM содержат аналитические допущения по доле цифрово-активных МСП и blended annual spend.
- Чек enterprise **600 тыс. - 1,2 млн ₽/мес** является аналитическим inference, а не публичным прайсом локального игрока.
- Для strong HIGH verdict нужно будет отдельно подтвердить российский прямой спрос, например через работающий demand-feed, локальные customer interviews или продажи ранних pilot contracts.

> Market Pulse 2026-04-19: растущий интерес.

---

## Этап 3 — Юнит-экономика

# 04-economics

## Кейс
ai-fullstack-app-builder-no-code-operator

## Дата расчёта
2026-04-19, Europe/Moscow

## Итог
**ECONOMICS = PASS. Инвестиционный профиль проходит, но только для enterprise / agency-managed app factory motion, а не для дешёвого self-serve SaaS.**

Ключевой вывод: low-end подписка уровня Lovable/Bolt в РФ не даёт фондовой экономики, но enterprise-модель `secure AI app factory + managed delivery + governance + integrations` собирает высокий ARPA, приемлемый CAC и быстрый payback.

- **Средняя выручка на клиента в месяц (ARPA)**: **780 000 ₽/мес**
- **COGS**: **298 000 ₽/мес на клиента**
- **Contribution Profit**: **404 000 ₽/мес на клиента**
- **Contribution Margin %**: **51.8%**
- **Blended CAC**: **1 550 000 ₽**
- **Churn benchmark**: **1-2%/мес для SaaS с ARPA $500+**
- **Принятый churn для модели**: **1.8%/мес**
- **LTV**: **22 446 667 ₽**
- **LTV/CAC**: **14.5x**
- **CAC Payback**: **3.8 месяца**
- **Break-even**: **12 активных клиентов / месяц 9**

---

## 1) Базовые допущения модели

### ICP
Основной клиент для расчёта:
- крупная компания с backlog внутренних digital-tools;
- банк, ритейл, логистика, сервисная сеть, экосистема;
- агентство или студия, штампующие клиентские MVP и личные кабинеты;
- platform / product team, которой нужен быстрый выпуск внутренних приложений и Telegram mini apps без найма дополнительной dev-команды.

### Коммерческая модель
Типовой контракт:
- **разовый setup / внедрение / шаблоны / security hardening**: **2 400 000 ₽**
- **ежемесячный platform retainer**: **420 000 ₽/мес**
- **managed delivery + support + governance**: **240 000 ₽/мес**
- **usage / hosting / additional environments**: **120 000 ₽/мес**
- **итого recurring revenue**: **780 000 ₽/мес**

Почему это реалистично:
- в 02-demand зафиксирован реалистичный enterprise-диапазон **600 тыс. - 1,2 млн ₽/мес**;
- value capture строится не на генерации кода как таковой, а на ускорении запуска внутренних сервисов, снижении time-to-MVP и замещении части подрядной разработки;
- для agency / enterprise покупателя платёж идёт за скорость, приватный контур, шаблоны, RBAC, audit trail и сопровождение generated apps.

---

## 2) Подробная таблица бизнес-процесса: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Подбор target accounts и enrichment | BDR | CRM, Apollo-подобный стек, Excel, Telegram | 25 мин | 1 100 | Средняя |
| 2 | Первый outreach | BDR | e-mail, Telegram, телефония, sequences | 20 мин | 850 | Средняя |
| 3 | Qualification call | AE | CRM, discovery script | 30 мин | 1 900 | Низкая |
| 4 | Demo с показом prompt-to-app сценария | AE + solutions architect | Meet, live demo sandbox | 60 мин | 4 800 | Низкая |
| 5 | Сбор use cases и требований по security | Solutions architect | checklist, Notion, template | 90 мин | 6 000 | Средняя |
| 6 | Мини-pilot на 1-2 сценариях | Presale engineer | AI builder, staging env, repo templates | 6 ч | 18 000 | Средняя |
| 7 | ROI-модель и business case | Solutions architect + finance | spreadsheet, ROI template | 2 ч | 7 500 | Средняя |
| 8 | Коммерческое предложение и scoping | AE + architect | CPQ, SoW template, CRM | 2 ч | 8 700 | Средняя |
| 9 | Procurement / security review / legal | Founder + architect | NDA, DPA, security docs, ЭДО | 8 ч | 24 000 | Низкая |
| 10 | Подписание договора | Founder / AE | ЭДО, e-sign | 1 ч | 2 800 | Высокая |
| 11 | Онбординг, доступы, workspace setup | Delivery lead | Jira, Git, SSO, checklist | 5 ч | 12 500 | Средняя |
| 12 | Настройка шаблонов, guardrails и connectors | Platform engineer | templates, CI/CD, integration layer | 18 ч | 54 000 | Средняя |
| 13 | Интеграция auth, payments, DB, notifications | Full-stack integration engineer | API, SDK, secrets manager | 20 ч | 60 000 | Низкая |
| 14 | UAT и правки первой волны | QA + customer success | test suite, preview env | 14 ч | 28 000 | Средняя |
| 15 | Go-live первого production-light сценария | Delivery lead | deploy pipeline, monitoring | 4 ч | 9 000 | Средняя |
| 16 | Ежемесячная генерация и публикация новых фич | AI platform + engineer review | LLM stack, templates, CI/CD | непрерывно | 92 000 | Высокая |
| 17 | Ручная доработка edge cases | Full-stack engineer | IDE, repo, issue tracker | 20 ч/мес | 68 000 | Низкая |
| 18 | Customer success, SLA и governance review | CSM | dashboard, backlog review | 10 ч/мес | 34 000 | Средняя |
| 19 | Выставление счёта | Finance ops | 1С, ЭДО | 30 мин/мес | 1 200 | Высокая |
| 20 | Получение оплаты и контроль дебиторки | Finance ops | банк, 1С, CRM | 20 мин/мес | 900 | Высокая |

### Вывод по процессу
- Самые дорогие участки, presale pilot, интеграции и ручная доработка edge cases.
- Экономика работает, только если не продавать кастомную разработку с нуля, а стандартизировать шаблоны, коннекторы и rollout playbooks.
- Главный операционный рычаг, уменьшать долю ручного engineering-overrun после 2-3 месяца работы клиента.

---

## 3) Разбивка COGS на клиента в месяц

| Компонент COGS | Логика | ₽/клиент/мес |
|---|---|---:|
| LLM / inference / code generation | генерация UI, backend, тестов, prompts | 58 000 |
| Cloud / hosting / environments / monitoring | staging, production-light, логи, storage | 44 000 |
| Full-stack engineer review | code review и доработка edge cases, 0.4 FTE | 92 000 |
| Customer success / SLA support | ежемесячные sync, приоритизация, обучение | 34 000 |
| QA / release validation | smoke tests, regression, quality gate | 18 000 |
| Поддержка интеграций и коннекторов | auth, payments, webhooks, vendor updates | 36 000 |
| Security / backup / DevOps reserve | secrets, backups, patching | 16 000 |
| **Итого COGS** |  | **298 000** |

### Gross Margin
- Выручка: **780 000 ₽/мес**
- COGS: **298 000 ₽/мес**
- **Gross Profit = 482 000 ₽/мес**
- **Gross Margin = 61.8%**

Для operator-like AI platform это сильный показатель, но он держится только при стандартизированном delivery.

---

## 4) CAC по каналам с funnel conversion

| Канал | Верх воронки | SQL / discovery | Pilot / proposal | Closed won | Конверсия lead→close | Месячные затраты канала, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound enterprise ABM | 180 аккаунтов / 24 лида | 10 | 4 | 0.6 | 2.5% от лида | 1 200 000 | 2 000 000 |
| Партнёры: интеграторы, digital-агентства, dev shops | 18 интро | 10 | 5 | 1.0 | 5.6% от интро | 550 000 | 550 000 |
| Inbound: контент, demo webinar, founder brand | 40 MQL | 10 | 3 | 0.5 | 1.25% от MQL | 700 000 | 1 400 000 |
| Product-led expansion из low-end trial / sandbox | 60 activated accounts | 6 | 2 | 0.2 | 0.33% от activation | 320 000 | 1 600 000 |

### Blended CAC
Расчёт на месячном миксе:
- суммарные затраты = **2 770 000 ₽**
- суммарно новых клиентов = **1.8**
- **Blended CAC = 1 538 889 ₽**

Для консервативности округляю вверх:
- **Blended CAC = 1 550 000 ₽**

### Вывод по CAC
- Партнёрский канал лучший по economics, потому что buyer уже осознал задачу.
- Outbound дорогой, но нужен для формирования первых enterprise logos.
- Product-led funnel полезен как proof layer, но сам по себе не является основным каналом для high-ticket продажи.

---

## 5) LTV с churn rate

### Benchmark source
Внешний benchmark retention:
- **ChartMogul Help Center, updated ~2025**: для SaaS-бизнесов с **ARPA $500+** customer churn обычно находится в диапазоне **1-2% в месяц**.
- Источник: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate

Дополнительный ориентир:
- **ChartMogul blog**: по мере роста ARR churn у зрелых SaaS-компаний снижается, у более крупных компаний медиана уходит примерно к **3.1% customer churn** и ниже в зависимости от сегмента и ARPA.
- Источник: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/

### Выбранный churn для модели
Для этого кейса беру **1.8%/мес**, потому что:
- чек высокий;
- интеграции и шаблоны встраиваются в процессы клиента;
- switching cost выше, чем у обычного self-serve builder;
- но продукт всё ещё частично service-led и чувствителен к качеству delivery.

### Формула
LTV = ARPA x Contribution Margin % / Monthly Churn

### Расчёт
- ARPA = **780 000 ₽/мес**
- Contribution Margin % = **51.8%**
- Monthly churn = **1.8%**

**LTV = 780 000 x 0.518 / 0.018 = 22 446 667 ₽**

Округляю:
- **LTV = 22.45 млн ₽**

### Вывод
- LTV многократно выше минимального порога **500 000 ₽**;
- даже при ухудшении churn до **2.5%/мес** LTV останется около **16.16 млн ₽**.

---

## 6) LTV/CAC ratio

- LTV = **22 446 667 ₽**
- CAC = **1 550 000 ₽**

**LTV/CAC = 14.5x**

### Интерпретация
- инвестиционный порог: **>= 3:1**
- фактический результат: **14.5:1**

Это уверенно проходит порог investment-grade даже с заметным запасом на ухудшение конверсий.

---

## 7) CAC Payback в месяцах

Формула:
CAC Payback = CAC / Monthly Contribution Profit

Где:
- Monthly Contribution Profit = **404 000 ₽/мес**
- CAC = **1 550 000 ₽**

**CAC Payback = 1 550 000 / 404 000 = 3.84 месяца**

### Вывод
Payback меньше 4 месяцев. Для enterprise-led AI operator это сильный результат.

---

## 8) Contribution Margin %

Для contribution margin учитываю:
- COGS;
- partner/referral commission;
- payment processing и документооборот;
- reserve на перерасход engineering hours.

| Показатель | ₽/мес |
|---|---:|
| Выручка | 780 000 |
| COGS | 298 000 |
| Партнёрская комиссия / referral | 39 000 |
| Payment processing / ЭДО / billing ops | 5 000 |
| Резерв на engineering overrun | 34 000 |
| **Contribution Profit** | **404 000** |
| **Contribution Margin %** | **51.8%** |

### Вывод
Более половины выручки после переменных затрат остаётся на покрытие fixed costs, это уже инвестиционно приемлемо.

---

## 9) Полная команда: роли, функции, зарплаты

| Роль | Функция | Формат | Оклад, ₽/мес |
|---|---|---|---:|
| Founder / CEO | enterprise sales, партнёрства, стратегия | fixed | 350 000 |
| Sales lead / AE | pipeline, demo, closing | fixed | 250 000 |
| BDR / SDR | outbound, qualification | fixed | 140 000 |
| Solutions architect | presale, scoping, security requirements | fixed | 280 000 |
| Platform engineer | шаблоны, orchestration, CI/CD | fixed | 300 000 |
| Full-stack integration engineer | connectors, auth, payments, delivery | fixed | 260 000 |
| AI engineer | prompt / codegen quality, evaluation loops | fixed | 300 000 |
| Product manager | roadmap, packaging, instrumentation | fixed | 220 000 |
| QA / release manager | тестирование, quality gate | fixed | 180 000 |
| Customer success lead | adoption, SLA, expansion | fixed | 180 000 |
| Finance / ops manager | billing, procurement, документооборот | fixed | 150 000 |
| DevOps / security engineer | infra, backups, IAM, monitoring | fixed | 240 000 |
| Contract designer / front specialist | polish UI для key accounts | variable / part-time | 130 000 |
| Contract implementation specialist | rollout support | variable / part-time | 140 000 |

### Fixed payroll core
Без переменных contract delivery-ролей:
- **2 850 000 ₽/мес**

### Комментарий
- часть delivery вынесена в COGS и variable pool;
- это защищает fixed base и позволяет масштабировать клиентов быстрее, чем headcount.

---

## 10) Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Fixed payroll core | 2 850 000 |
| Налоги и payroll reserve | 620 000 |
| Офис / coworking / admin | 140 000 |
| CRM, analytics, dev tools, security stack | 230 000 |
| Юридическое сопровождение / бухгалтерия | 90 000 |
| Бренд, контент, events, founder marketing | 190 000 |
| Командировки и enterprise presale travel | 180 000 |
| Прочие G&A | 150 000 |
| **Итого fixed costs / мес** | **4 450 000** |

---

## 11) Break-even по числу клиентов и по месяцу

### Break-even по клиентам
Формула:
Fixed Costs / Contribution Profit per client

- Fixed Costs = **4 450 000 ₽/мес**
- Contribution Profit per client = **404 000 ₽/мес**

**Break-even client count = 11.01**

Округляю вверх:
- **12 активных клиентов**

### Break-even по месяцу
Базовый ramp:
- месяц 1-3: по **1** новому клиенту в месяц;
- месяц 4-6: по **1.5** клиента в месяц в среднем;
- месяц 7-9: по **1.5** клиента в месяц в среднем;
- churn в первый год невысокий и почти не влияет на точку безубыточности.

Тогда:
- к концу месяца 3: **3 клиента**
- к концу месяца 6: **7.5 клиента**
- к концу месяца 9: **12 клиентов**

**Break-even month = месяц 9**.

Если setup fees признаются как cash inflow upfront, cash break-even может наступать ближе к месяцу 7-8, но в базовой модели считаю только recurring contribution.

---

## 12) Чувствительность модели

### Негативный сценарий
Если:
- churn = **2.8%/мес**,
- recurring revenue = **650 000 ₽/мес**,
- contribution margin = **42%**,
- CAC = **1 900 000 ₽**,

то:
- LTV = **9.75 млн ₽**
- LTV/CAC = **5.1x**
- payback = **6.95 месяца**

Даже в этом сценарии модель остаётся выше investment-grade порога.

### Главные риски экономики
1. Превращение в кастомную веб-студию вместо стандартизированного app factory.
2. Слишком высокая доля ручного engineering review на каждый релиз.
3. Давление глобальных low-cost builders на low-end тарифы и ожидания покупателей.
4. Удлинение enterprise procurement cycle свыше 4-6 месяцев.

---

## 13) Финальный вывод

**Юнит-экономика проходит уверенно, но только в high-ticket сегменте.**

Почему PASS:
- LTV далеко выше порога **500 000 ₽**.
- **LTV/CAC = 14.5x**, существенно лучше инвестиционного минимума **3:1**.
- CAC payback меньше **4 месяцев**.
- Break-even достигается на **12 клиентах**, что достижимо для нишевого enterprise/agency оператора.
- Low-end self-serve motion для этого кейса экономически слаб, но enterprise app-factory motion даёт фондовый профиль.

## Решение
**ПЕРЕВЕСТИ КЕЙС ДАЛЬШЕ ПО ПАЙПЛАЙНУ. REJECT по economics НЕ ТРЕБУЕТСЯ.**

---

## Этап 4 — Финансовая модель и критика

# 05-critic

## Кейс
ai-fullstack-app-builder-no-code-operator

## Дата
2026-04-19, Europe/Moscow

## Итог
**CRITIC = CONDITIONAL PASS.**

Экономика на бумаге сильная, но только в узком enterprise / agency-managed wedge. Это не массовый SaaS, а service-led platform business. Для фонда кейс проходит дальше только как гипотеза `secure AI app factory + managed delivery + governance`, где можно удержать ARPA **780 000 ₽/мес** и не скатиться в кастомную студию.

Главный вывод критика: **модель выглядит фондово только при дисциплине delivery, partner-led GTM и жёстком отказе от low-end self-serve сегмента**. Если рынок вытолкнет компанию вниз по цене или вверх по ручному труду, профиль быстро деградирует.

---

## 1) Что именно я проверяю как critic

После 04-economics базовая логика уже понятна:
- ARPA = **780 000 ₽/мес**
- COGS = **298 000 ₽/клиент/мес**
- Gross Profit = **482 000 ₽/клиент/мес**
- Contribution Profit = **404 000 ₽/клиент/мес**
- CAC = **1 550 000 ₽**
- Churn = **1.8%/мес**
- Break-even = **12 клиентов**

Задача критика не повторить unit economics, а проверить, насколько модель выдерживает:
1. помесячный P&L на горизонте 12 месяцев;
2. структуру затрат в зрелом месяце;
3. кассовый профиль до безубыточности;
4. sensitivity к ключевым сломам модели;
5. риск давления со стороны конкурентов и substitute layer;
6. kill-conditions, при которых кейс надо закрывать без самообмана.

---

## 2) Модель сценариев: принятые допущения

### Base
- ARPA: **780 000 ₽/мес**
- COGS на клиента: **298 000 ₽/мес**
- Fixed costs: **4 450 000 ₽/мес**
- Активные клиенты по месяцам: **1, 2, 3, 4.5, 6, 7.5, 9, 10.5, 12, 13, 14, 15**
- EBITDA break-even: **месяц 8**

### Optimistic
- ARPA: **840 000 ₽/мес**
- COGS на клиента: **290 000 ₽/мес**
- Fixed costs: **4 700 000 ₽/мес**
- Клиенты: **1, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22**
- EBITDA break-even: **месяц 6**

### Pessimistic
- ARPA: **650 000 ₽/мес**
- COGS на клиента: **340 000 ₽/мес**
- Fixed costs: **4 300 000 ₽/мес**
- Клиенты: **0.5, 1, 1.5, 2, 3, 4, 5, 6, 7, 8, 9, 10**
- EBITDA break-even: **не достигается в первый год**

---

## 3) Полный 12-месячный P&L, 3 сценария

### 3.1 Base scenario

| Месяц | MRR, ₽ | COGS, ₽ | Gross Profit, ₽ | Fixed Costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| 1 | 780 000 | 298 000 | 482 000 | 4 450 000 | -3 968 000 |
| 2 | 1 560 000 | 596 000 | 964 000 | 4 450 000 | -3 486 000 |
| 3 | 2 340 000 | 894 000 | 1 446 000 | 4 450 000 | -3 004 000 |
| 4 | 3 510 000 | 1 341 000 | 2 169 000 | 4 450 000 | -2 281 000 |
| 5 | 4 680 000 | 1 788 000 | 2 892 000 | 4 450 000 | -1 558 000 |
| 6 | 5 850 000 | 2 235 000 | 3 615 000 | 4 450 000 | -835 000 |
| 7 | 7 020 000 | 2 682 000 | 4 338 000 | 4 450 000 | -112 000 |
| 8 | 8 190 000 | 3 129 000 | 5 061 000 | 4 450 000 | 611 000 |
| 9 | 9 360 000 | 3 576 000 | 5 784 000 | 4 450 000 | 1 334 000 |
| 10 | 10 140 000 | 3 874 000 | 6 266 000 | 4 450 000 | 1 816 000 |
| 11 | 10 920 000 | 4 172 000 | 6 748 000 | 4 450 000 | 2 298 000 |
| 12 | 11 700 000 | 4 470 000 | 7 230 000 | 4 450 000 | 2 780 000 |

### 3.2 Optimistic scenario

| Месяц | MRR, ₽ | COGS, ₽ | Gross Profit, ₽ | Fixed Costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| 1 | 840 000 | 290 000 | 550 000 | 4 700 000 | -4 150 000 |
| 2 | 1 680 000 | 580 000 | 1 100 000 | 4 700 000 | -3 600 000 |
| 3 | 3 360 000 | 1 160 000 | 2 200 000 | 4 700 000 | -2 500 000 |
| 4 | 5 040 000 | 1 740 000 | 3 300 000 | 4 700 000 | -1 400 000 |
| 5 | 6 720 000 | 2 320 000 | 4 400 000 | 4 700 000 | -300 000 |
| 6 | 8 400 000 | 2 900 000 | 5 500 000 | 4 700 000 | 800 000 |
| 7 | 10 080 000 | 3 480 000 | 6 600 000 | 4 700 000 | 1 900 000 |
| 8 | 11 760 000 | 4 060 000 | 7 700 000 | 4 700 000 | 3 000 000 |
| 9 | 13 440 000 | 4 640 000 | 8 800 000 | 4 700 000 | 4 100 000 |
| 10 | 15 120 000 | 5 220 000 | 9 900 000 | 4 700 000 | 5 200 000 |
| 11 | 16 800 000 | 5 800 000 | 11 000 000 | 4 700 000 | 6 300 000 |
| 12 | 18 480 000 | 6 380 000 | 12 100 000 | 4 700 000 | 7 400 000 |

### 3.3 Pessimistic scenario

| Месяц | MRR, ₽ | COGS, ₽ | Gross Profit, ₽ | Fixed Costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| 1 | 325 000 | 170 000 | 155 000 | 4 300 000 | -4 145 000 |
| 2 | 650 000 | 340 000 | 310 000 | 4 300 000 | -3 990 000 |
| 3 | 975 000 | 510 000 | 465 000 | 4 300 000 | -3 835 000 |
| 4 | 1 300 000 | 680 000 | 620 000 | 4 300 000 | -3 680 000 |
| 5 | 1 950 000 | 1 020 000 | 930 000 | 4 300 000 | -3 370 000 |
| 6 | 2 600 000 | 1 360 000 | 1 240 000 | 4 300 000 | -3 060 000 |
| 7 | 3 250 000 | 1 700 000 | 1 550 000 | 4 300 000 | -2 750 000 |
| 8 | 3 900 000 | 2 040 000 | 1 860 000 | 4 300 000 | -2 440 000 |
| 9 | 4 550 000 | 2 380 000 | 2 170 000 | 4 300 000 | -2 130 000 |
| 10 | 5 200 000 | 2 720 000 | 2 480 000 | 4 300 000 | -1 820 000 |
| 11 | 5 850 000 | 3 060 000 | 2 790 000 | 4 300 000 | -1 510 000 |
| 12 | 6 500 000 | 3 400 000 | 3 100 000 | 4 300 000 | -1 200 000 |

### Что говорит P&L
- **Base** выглядит рабочим, но запас прочности умеренный. На месяце 7 EBITDA ещё отрицательная: **-112 000 ₽**.
- **Optimistic** уже похож на фондовую историю, потому что к месяцу 12 EBITDA выходит на **7.4 млн ₽/мес**.
- **Pessimistic** разрушает тезис полностью: даже при **10 клиентах** к месяцу 12 компания всё ещё теряет **1.2 млн ₽/мес**.

Иначе говоря, это не robust SaaS, а модель с довольно узким окном исполнения.

---

## 4) Waterfall cost structure, месяц 12, base scenario

Месяц 12 в базе:
- MRR = **11 700 000 ₽**
- EBITDA = **2 780 000 ₽**

### Waterfall

| Блок затрат / прибыли | ₽ | % от MRR |
|---|---:|---:|
| MRR | 11 700 000 | 100.0% |
| COGS | 4 470 000 | 38.2% |
| Gross Profit | 7 230 000 | 61.8% |
| Sales | 1 050 000 | 9.0% |
| Marketing | 440 000 | 3.8% |
| R&D | 1 950 000 | 16.7% |
| G&A | 1 010 000 | 8.6% |
| EBITDA | 2 780 000 | 23.8% |

### Комментарий по waterfall
- Самая тяжёлая статья после COGS, **R&D 1.95 млн ₽/мес**. Это нормально для AI platform, но означает, что продукт не может долго жить на low-ticket тарифах.
- **Sales + Marketing = 1.49 млн ₽/мес**, то есть GTM всё ещё заметно тяжёлый и не выглядит как чистый product-led growth.
- **G&A 1.01 млн ₽/мес** уже ощутим, но не критичен. Главная проблема не G&A, а риск раздувания COGS и presale.

---

## 5) Cash flow analysis

## 5.1 Burn rate, месяцы 1-3

Для cash flow учитываю:
- EBITDA из base scenario;
- setup fee **2 400 000 ₽** на каждого нового клиента как upfront cash inflow;
- новых клиентов в base: **1, 1, 1, 1.5, 1.5, 1.5, 1.5, 1.5, 1.5, 1, 1, 1**.

| Месяц | EBITDA, ₽ | Setup cash inflow, ₽ | Net cash burn / inflow, ₽ |
|---|---:|---:|---:|
| 1 | -3 968 000 | 2 400 000 | -1 568 000 |
| 2 | -3 486 000 | 2 400 000 | -1 086 000 |
| 3 | -3 004 000 | 2 400 000 | -604 000 |

### Вывод
- Burn быстро снижается: **1.57 млн → 1.09 млн → 0.60 млн ₽**.
- Это сильнее, чем выглядит по EBITDA, потому что setup fee частично финансирует рост.
- Но это же и риск, компания может выглядеть cash-positive раньше, чем станет реально устойчивой по recurring economics.

## 5.2 Startup capital needed to BEP

Если смотреть на cumulative cash до первого положительного месячного cash result, то:
- минимальная точка cumulative cash достигается после месяца 3;
- максимальная просадка = **-3 258 000 ₽**.

### Нужный стартовый капитал
- **Минимально до cash break-even: 3.3 млн ₽**
- **Рекомендованный буфер 2x: 6.5-7.0 млн ₽**

Почему нужен буфер выше математического минимума:
1. enterprise оплаты могут сдвигаться на 30-60 дней;
2. pilot и security review часто съедают больше presale hours, чем планируется;
3. setup fee может признаваться не сразу, а по milestone;
4. churn в первые 6 месяцев может быть выше модельного.

## 5.3 Что важнее, cash BEP или EBITDA BEP

- **Cash break-even** в базе достигается примерно на **месяце 5**, если setup fees реально заходят деньгами вовремя.
- **EBITDA break-even** достигается только на **месяце 8**.

Критический вывод: у компании может появиться иллюзия ранней устойчивости. На самом деле устойчивость держится на постоянном притоке новых setup-контрактов. Если новые сделки замедлятся, кассовая картина резко ухудшится.

---

## 6) Sensitivity analysis

### 6.1 CAC x2

Базовые значения:
- CAC = **1 550 000 ₽**
- LTV = **22 446 667 ₽**
- LTV/CAC = **14.5x**
- Contribution Profit = **404 000 ₽/клиент/мес**
- CAC Payback = **3.84 месяца**

Если CAC удваивается:
- новый CAC = **3 100 000 ₽**
- LTV/CAC = **22 446 667 / 3 100 000 = 7.2x**
- CAC Payback = **3 100 000 / 404 000 = 7.67 месяца**

### Вывод
Модель всё ещё формально проходит, но теряет главный плюс, быстрый возврат капитала. Для фонда это ещё терпимо, но уже гораздо менее красиво, особенно при длинном procurement cycle.

### 6.2 Churn x2

База:
- churn = **1.8%/мес**
- LTV = **22 446 667 ₽**

Если churn удваивается:
- churn = **3.6%/мес**
- новый LTV = **780 000 × 0.518 / 0.036 = 11 223 333 ₽**
- LTV/CAC = **11 223 333 / 1 550 000 = 7.2x**

### Вывод
На первый взгляд метрика ещё живая, но это опасная иллюзия. При churn **3.6%/мес** продукт перестаёт быть sticky enterprise platform и начинает походить на временный delivery-инструмент. Для такого класса бизнеса это уже тревожный сигнал качества продукта и внедрения.

### 6.3 Price -30%

Если recurring price падает на 30%:
- новый ARPA = **546 000 ₽/мес**
- COGS оставляем базовым: **298 000 ₽/мес**
- новый Gross Profit = **248 000 ₽/мес**
- new Gross Margin = **45.4%**
- если partner/referral + billing + overrun reserve оставить на прежнем уровне **78 000 ₽/мес**, тогда:
- new Contribution Profit = **170 000 ₽/мес**
- new Contribution Margin = **31.1%**
- новый LTV = **546 000 × 0.311 / 0.018 = 9 438 333 ₽**
- новый LTV/CAC = **9 438 333 / 1 550 000 = 6.1x**
- новый CAC Payback = **1 550 000 / 170 000 = 9.12 месяца**
- новый break-even clients = **4 450 000 / 170 000 = 26.2**, то есть **27 клиентов**

### Вывод
Это самый опасный sensitivity-фактор. Падение цены на 30% не убивает компанию сразу, но ломает весь тезис о capital efficiency. Нужно уже не **12 клиентов**, а **27 клиентов** для break-even, а это совсем другой GTM и совсем другой риск-профиль.

---

## 7) Competitor deep-dive

## 7.1 Lovable

### Сильные стороны
- сильный global brand в AI-native app building;
- понятный self-serve UX и быстрый value demo;
- большая вероятность лучшей data flywheel по prompt patterns и product usage;
- уже нормализует категорию в глазах пользователей.

### Слабые стороны
- pricing якорит рынок слишком низко для локального enterprise-first игрока;
- для РФ есть барьеры по локальным интеграциям, hosting, compliance и procurement;
- self-serve DNA хуже подходит под внедрение в regulated enterprise.

### Copy risk
- **Очень высокий** по UX и positioning на поверхности.
- **Низкий** по масштабу distribution, brand и глобальной product velocity.

### Что это значит для кейса
Копировать Lovable в low-end нельзя. Выиграть можно только через локальные integrations, private deployment и managed rollout.

## 7.2 Bolt

### Сильные стороны
- сильный developer-adjacent сценарий и быстрый path от идеи к working prototype;
- понятная командная модель seat-based usage;
- сильный международный mindshare.

### Слабые стороны
- pricing тоже тянет рынок вниз;
- enterprise differentiation неочевидна без дополнительного service/governance слоя;
- для non-technical buyer может быть менее удобен, чем более opinionated workflow.

### Copy risk
- **Высокий** по функциональному ядру demo-level experience.
- **Средний** по удержанию, потому что без экосистемы и adoption loop копия не удержит качество.

### Что это значит для кейса
Bolt опасен как ceiling на product expectations и floor на willingness to pay. Пользователь захочет product magic как у Bolt, но платить будет только за enterprise result.

## 7.3 v0 by Vercel

### Сильные стороны
- сильнейшая developer ecosystem adjacency;
- natural distribution через Vercel ecosystem;
- высокий trust у product и frontend teams.

### Слабые стороны
- скорее builder for teams, чем полноценный managed app-factory operator;
- не решает локальные procurement / compliance / российские integrations сам по себе;
- enterprise value для non-dev buyer не всегда очевиден.

### Copy risk
- **Средний** по UX.
- **Низкий** по ecosystem moat.

### Что это значит для кейса
v0 особенно опасен в upper-mid segment. Если целевые product teams уже живут в Vercel stack, локальный игрок должен продавать не генерацию интерфейса, а governance, speed of rollout и безопасный delivery under SLA.

## 7.4 Salebot

### Сильные стороны
- сильное локальное знание рынка;
- низкий порог входа;
- уже приучил SMB платить за automation и builder layer;
- большой локальный installed base.

### Слабые стороны
- это не полноценный full-stack app factory;
- слабее подходит для внутренних enterprise apps и сложных интеграционных сценариев;
- бренд тяготеет к bot/automation layer, а не к platform-grade software delivery.

### Copy risk
- **Низкий** сверху вниз, потому что он не про тот же product depth.
- **Высокий** снизу вверх как substitute, который забирает low-end спрос и ломает pricing power.

### Что это значит для кейса
Salebot не прямой killer-конкурент в enterprise, но это очень опасный заменитель на нижнем сегменте. Он не даёт новому игроку спуститься вниз по цене без разрушения экономики.

## 7.5 Botmother

### Сильные стороны
- понятный builder для мессенджеров;
- есть платёжная привычка в рынке;
- уже доказывает WTP за visual/no-code creation.

### Слабые стороны
- ограниченность use-case layer, бот и messaging workflows вместо полноценных приложений;
- слабый fit для secure internal tools и multi-role enterprise systems.

### Copy risk
- **Низкий** как прямой app-builder competitor.
- **Средний** как price anchor для SMB, который будет сравнивать всё новое с ценой конструктора ботов.

### Что это значит для кейса
Botmother не мешает premium wedge напрямую, но мешает маркетингу broad SMB positioning, потому что покупатели будут задавать вопрос, почему не взять заметно более дешёвый конструктор.

## 7.6 LeadConverter

### Сильные стороны
- Telegram-first, понятный локальному SMB workflow;
- AI integration как маркетинговый триггер;
- низкий барьер запуска.

### Слабые стороны
- продуктовый потолок сильно ниже полного app-factory;
- слабая защита против enterprise требований по RBAC, audit, deployment control.

### Copy risk
- **Низкий** как прямой core-product threat.
- **Высокий** как low-cost substitute на рынке быстрых digital scenarios.

### Что это значит для кейса
LeadConverter опасен не тем, что заберёт enterprise deal, а тем, что постоянно напоминает рынку, что многие задачи можно решить очень дёшево.

---

## 8) Risk matrix

| Риск | Вероятность | Месячный impact, ₽ | Ранний сигнал | Митигация |
|---|---|---:|---|---|
| Скатывание в кастомную студию вместо стандартизированного app factory | 45% | 1 500 000 | средние delivery hours на клиента > 140 ч/мес два месяца подряд | жёсткий каталог шаблонов, запрет на bespoke-фичи без price uplift, delivery scorecard |
| Давление на цену из-за low-end substitutes и глобальных pricing anchors | 40% | 2 100 000 | win-rate падает, а median quoted MRR уходит ниже 650 000 ₽ | позиционирование только на enterprise wedge, продавать compliance/integrations/SLA, не публиковать low-end pricing |
| Удлинение procurement и delayed cash collection | 35% | 1 200 000 | DSO > 75 дней, security review > 60 дней, доля просроченной дебиторки > 15% | 50% setup prepayment, milestone billing, prioritise partner-led deals |
| Рост COGS из-за ручного review и интеграционного оверхеда | 50% | 1 350 000 | COGS на клиента > 360 000 ₽ три месяца подряд | template hardening, connector library, SLA tiers, quarterly repricing low-margin accounts |
| Vendor dependency на frontier LLM / infrastructure stack | 25% | 900 000 | inference cost на проект растёт > 25% QoQ или latency ломает demo-to-go-live | multi-model routing, cache layer, fallback providers, margin guardrails |
| Низкое удержание после первых 2-3 релизов | 30% | 1 600 000 | logo churn > 3%/мес или expansion revenue < 10% от базы | customer success playbooks, QBR, roadmap tied to production use-cases, measure time-to-live-feature |

### Комментарий
Наиболее токсичная комбинация, **price compression + custom delivery creep + delayed collections**. Она не просто ухудшает KPI, а делает бизнес structurally non-scalable.

---

## 9) Kill conditions

Кейс надо закрывать или переводить в hard reject, если выполняется хотя бы одно из условий:

### Kill condition 1
**К месяцу 9 нет минимум 8 активных клиентов с MRR не ниже 650 000 ₽.**

Почему это kill:
- база требует около 12 клиентов для устойчивого EBITDA break-even;
- если к месяцу 9 компания не набрала хотя бы 8 сильных клиентов, значит GTM либо слишком дорогой, либо рынок не принимает premium wedge.

### Kill condition 2
**COGS на клиента держится выше 360 000 ₽/мес три месяца подряд.**

Почему это kill:
- при таком уровне gross profit резко сжимается;
- дальше компания перестаёт быть platform business и превращается в disguised services shop.

### Kill condition 3
**Median realised selling price падает ниже 550 000 ₽/мес на новых сделках в течение квартала.**

Почему это kill:
- это уже почти сценарий `price -30%`;
- тогда payback уходит примерно к **9.1 месяца**, а break-even съезжает к **27 клиентам**;
- фондовый профиль перестаёт существовать.

---

## 10) Финальный verdict critic

### Что нравится
- Базовая экономика в premium сегменте действительно сильная.
- Есть понятный wedge: `enterprise secure AI app factory`.
- Cash profile лучше, чем кажется по EBITDA, из-за setup fee.
- Даже при CAC x2 и churn x2 модель формально ещё жива.

### Что не нравится
- У модели очень узкий коридор права на ошибку.
- Цена, стандартизация и скорость внедрения должны держаться одновременно.
- Low-end рынок уже занят substitute layer и будет постоянно тянуть компанию вниз по чеку.
- Ранний cash positivity может скрыть хрупкость recurring economics.

## Решение критика
**CONDITIONAL PASS.**

Пропускать дальше можно, но только с жёсткой формулировкой:
- не инвестировать тезис в low-end self-serve;
- считать кейс только как enterprise / agency-managed operator;
- отслеживать kill conditions ежемесячно;
- считать главной метрикой не просто ARR growth, а `realised MRR per logo`, `COGS per logo`, `time-to-go-live`, `share of templated delivery`.

Если команда не докажет удержание цены и шаблонного delivery, кейс надо быстро резать, не дожидаясь красивых vanity metrics.

---

## Этап 5 — Финальный вердикт

# 06-verdict

## Кейс
ai-fullstack-app-builder-no-code-operator

## Дата вердикта
2026-04-19

## Статус
**NEAR-PASS**

## Итоговый вывод инвесткомитета
**69/100.** Кейс не дотянул **1 балл** до порога 70 и потому уходит в `pipeline/rejected/` как near-pass. Экономика premium enterprise wedge выглядит сильной, но пока недостаточно доказаны два ключевых тезиса: прямой спрос в РФ именно на full-stack prompt-to-app factory и способность удерживать цену без скатывания в кастомную студию.

## Score breakdown
| Критерий | Балл | Комментарий |
|---|---:|---|
| Реальный спрос | 13/20 | MEDIUM спрос: есть 3 глобальных конкурента с ценами и российский adjacent слой, но нет прямого лидера в РФ и нет exact multi-demand datapoint. |
| Прибыль компании / Unit Economics | 22/25 | 500K EBITDA достигается при 13 клиентах, 1M EBITDA при 15 клиентах; startup_capital_to_bep_rub около 3,3 млн ₽, но окно исполнения узкое. |
| Масштабируемость | 14/20 | Шаблоны, коннекторы и AI-native delivery снижают marginal cost, но модель остаётся service-led и требует engineer review. |
| Конкурентное позиционирование | 8/15 | Дифференциация есть только через enterprise-private deployment, governance и локальные интеграции; копируемость функционального ядра высокая. |
| Барьеры входа | 5/10 | Есть умеренные барьеры через интеграции, шаблоны и внедрение, но нет данных/сети/регуляторного moat. |
| Качество данных | 7/10 | Есть цены, churn benchmark и P&L, но часть TAM/SAM/SOM и enterprise pricing являются inference, mandatory demand endpoint не сработал. |
| **Итого** | **69/100** | **Порог 70 не достигнут, статус: NEAR-PASS.** |

## Почему итог именно такой
1. **Экономика проходит**, но её качество зависит от очень узкого сценария: ARPA **780 000 ₽/мес**, `contribution_margin_rub_month` **404 000 ₽/мес**, `company_ebitda_rub_month` **≈ 802 000 ₽/мес** на 13 клиентах после покрытия fixed costs.
2. **Спрос подтверждён только частично**: есть глобальные аналоги с pricing, есть российский adjacent рынок no-code/ботов, но нет прямого российского лидера и не сработал mandatory demand feed.
3. **Moat слабее экономики**: функциональное ядро быстро копируется, а защита строится в основном на локальных интеграциях, delivery discipline и go-to-market, а не на данных или платформенном эффекте.

## Полный бизнес-процесс из 04-economics.md
| № | Шаг | Кто | Инструмент | Время | Стоимость (руб) | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Подбор target accounts и enrichment | BDR | CRM, Apollo-подобный стек, Excel, Telegram | 25 мин | 1 100 | Средняя |
| 2 | Первый outreach | BDR | e-mail, Telegram, телефония, sequences | 20 мин | 850 | Средняя |
| 3 | Qualification call | AE | CRM, discovery script | 30 мин | 1 900 | Низкая |
| 4 | Demo с показом prompt-to-app сценария | AE + solutions architect | Meet, live demo sandbox | 60 мин | 4 800 | Низкая |
| 5 | Сбор use cases и требований по security | Solutions architect | checklist, Notion, template | 90 мин | 6 000 | Средняя |
| 6 | Мини-pilot на 1-2 сценариях | Presale engineer | AI builder, staging env, repo templates | 6 ч | 18 000 | Средняя |
| 7 | ROI-модель и business case | Solutions architect + finance | spreadsheet, ROI template | 2 ч | 7 500 | Средняя |
| 8 | Коммерческое предложение и scoping | AE + architect | CPQ, SoW template, CRM | 2 ч | 8 700 | Средняя |
| 9 | Procurement / security review / legal | Founder + architect | NDA, DPA, security docs, ЭДО | 8 ч | 24 000 | Низкая |
| 10 | Подписание договора | Founder / AE | ЭДО, e-sign | 1 ч | 2 800 | Высокая |
| 11 | Онбординг, доступы, workspace setup | Delivery lead | Jira, Git, SSO, checklist | 5 ч | 12 500 | Средняя |
| 12 | Настройка шаблонов, guardrails и connectors | Platform engineer | templates, CI/CD, integration layer | 18 ч | 54 000 | Средняя |
| 13 | Интеграция auth, payments, DB, notifications | Full-stack integration engineer | API, SDK, secrets manager | 20 ч | 60 000 | Низкая |
| 14 | UAT и правки первой волны | QA + customer success | test suite, preview env | 14 ч | 28 000 | Средняя |
| 15 | Go-live первого production-light сценария | Delivery lead | deploy pipeline, monitoring | 4 ч | 9 000 | Средняя |
| 16 | Ежемесячная генерация и публикация новых фич | AI platform + engineer review | LLM stack, templates, CI/CD | непрерывно | 92 000 | Высокая |
| 17 | Ручная доработка edge cases | Full-stack engineer | IDE, repo, issue tracker | 20 ч/мес | 68 000 | Низкая |
| 18 | Customer success, SLA и governance review | CSM | dashboard, backlog review | 10 ч/мес | 34 000 | Средняя |
| 19 | Выставление счёта | Finance ops | 1С, ЭДО | 30 мин/мес | 1 200 | Высокая |
| 20 | Получение оплаты и контроль дебиторки | Finance ops | банк, 1С, CRM | 20 мин/мес | 900 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| CAC | 1 550 000 ₽ |
| customer_ltv_rub, консервативный | 4 040 000 ₽ |
| customer_ltv_rub, базовый | 8 080 000 ₽ |
| customer_ltv_rub, оптимистичный | 20 200 000 ₽ |
| contribution_margin_rub_month | 404 000 ₽/мес |
| Gross Margin | 61,8% |
| LTV/CAC | 5,2x |
| CAC Payback | 3,8 мес |
| fixed_costs_rub_month | 4 450 000 ₽/мес |
| Break-even | 12 клиентов / месяц 9 |
| startup_capital_to_bep_rub | 3 300 000 ₽ |
| Инвестиции до 1M EBITDA | 7 000 000 ₽ |

## Прибыль компании
- `company_ebitda_rub_month` при **13 клиентах**: **≈ 802 000 ₽/мес** по формуле `13 × 404 000 − 4 450 000`.
- **500K EBITDA** достигается при **13 клиентах**, ориентир по времени, **месяц 9**.
- **1M EBITDA** достигается при **15 клиентах**, ориентир по времени, **месяц 12**.
- Реалистичный потенциал на горизонте 12 месяцев, `company_ebitda_potential_rub_month`: **1 610 000 ₽/мес** при удержании цены и templated delivery.

## Команда для запуска
| Роль | Функция | Занятость | Зарплата (руб/мес) |
|---|---|---|---:|
| Founder / CEO | enterprise sales, партнёрства, стратегия | full | 350 000 |
| Sales lead / AE | pipeline, demo, closing | full | 250 000 |
| BDR / SDR | outbound, qualification | full | 140 000 |
| Solutions architect | presale, scoping, security requirements | full | 280 000 |
| Platform engineer | шаблоны, orchestration, CI/CD | full | 300 000 |
| Full-stack integration engineer | connectors, auth, payments, delivery | full | 260 000 |
| AI engineer | prompt / codegen quality, evaluation loops | full | 300 000 |
| Product manager | roadmap, packaging, instrumentation | full | 220 000 |
| QA / release manager | тестирование, quality gate | full | 180 000 |
| Customer success lead | adoption, SLA, expansion | full | 180 000 |
| Finance / ops manager | billing, procurement, документооборот | full | 150 000 |
| DevOps / security engineer | infra, backups, IAM, monitoring | full | 240 000 |
| Contract designer / front specialist | polish UI для key accounts | part | 130 000 |
| Contract implementation specialist | rollout support | part | 140 000 |

**Итого команда:** 14 ролей, фиксированный ФОТ ядра **2 850 000 ₽/мес**.

## Топ-3 риска
| Риск | Вероятность | Влияние |
|---|---|---:|
| Скатывание в кастомную студию вместо стандартизированного app factory | высокая, 45% | 1 500 000 ₽/мес |
| Давление на цену из-за low-end substitutes и глобальных pricing anchors | средняя-высокая, 40% | 2 100 000 ₽/мес |
| Рост COGS из-за ручного review и интеграционного оверхеда | высокая, 50% | 1 350 000 ₽/мес |

## Что конкретно не дало пройти порог
1. **Спрос**: нет прямого российского лидера и нет exact demand-feed. Это ограничило критерий спроса до **13/20**.
2. **Конкурентная защита**: копирование ядра возможно за 3-6 месяцев, если не будет локального compliance и strong deployment moat. Это ограничило критерий позиционирования до **8/15**.
3. **Барьеры входа**: интеграции и enterprise motion дают только умеренную защиту. Это ограничило критерий барьеров до **5/10**.

## LTV Upside Calculator
**Сейчас: 69/100. Нужно ещё: 1 балл до порога 70.**

| Критерий | Сейчас | Потолок | Что сделать | Потенциал |
|---|---:|---:|---|---:|
| Реальный спрос | 13/20 | 20/20 | Получить 2-3 российских paid pilot contracts или LOI с чеком от 600 000 ₽/мес и показать локальный pipeline через работающий demand-feed | +3…5 |
| Конкурентное позиционирование | 8/15 | 15/15 | Доказать уникальность через private deployment, Russian stack connectors, security templates и SLA, которые нельзя быстро повторить self-serve игрокам | +2…4 |
| Барьеры входа | 5/10 | 10/10 | Нарастить шаблонную библиотеку, integration depth и governance layer с lock-in по данным и процессам | +1…3 |

**Кратчайший путь к 70+:** добавить один сильный proof point по российскому спросу. Даже **+1 балл** по критерию спроса переведёт кейс в approved с замечаниями.

## Следующее действие
Не закрывать гипотезу окончательно. Запускать только как **enterprise / agency-managed AI app factory**, а перед relaunch доказать российские пилоты, устойчивую цену не ниже **650 000 ₽/мес** и COGS не выше **360 000 ₽/клиент/мес**.

---

## Этап 6 — История прохождения пайплайна

# 07-score-trajectory
## Кейс: ai-fullstack-app-builder-no-code-operator
## Начат: 2026-04-19

История прохождения пайплайна.

### 2026-04-19 - Программа 7 / Critic and verdict
- Статус: NEAR-PASS
- Итоговый балл: 69/100
- Разбивка: спрос 13/20, экономика 22/25, масштаб 14/20, конкуренция 8/15, защита 5/10, данные 7/10
- LTV/CAC: 5,2:1 | CAC Payback: 3,8 мес | Break-even: месяц 9 / 12 клиентов
- Стартовый капитал до BEP: 3 300 000 ₽
- Причина: Экономика premium wedge сильная, но пока недостаточно доказаны прямой спрос в РФ и защитимое позиционирование без скатывания в кастомную студию.
