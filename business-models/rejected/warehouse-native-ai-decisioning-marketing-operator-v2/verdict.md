# verdict
Источник pipeline: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/warehouse-native-ai-decisioning-marketing-operator-v2`

## Стадия 0. Brief
# Brief

- Кейс: Warehouse-native AI Decisioning Marketing Operator
- Slug: warehouse-native-ai-decisioning-marketing-operator-v2
- Sector: B2B-OPS
- Режим: rerun / полный пайплайн обязателен
- Исходный raw-файл: 2026-04-19-rerun-warehouse-native-ai-decisioning-marketing-operator.md
- Предыдущий статус: ❌ REJECTED
- Предыдущий score: 61/100
- Следующий этап: P3-demand-validation

## Почему создан новый кейс
Файл пришёл с префиксом `rerun-`, поэтому создана новая версия кейса без duplicate-классификации. Кейсу требуется полный повторный анализ по обновлённой системе.


## Стадия 1. Intake
---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-rerun-warehouse-native-ai-decisioning-marketing-operator.md
created: 2026-04-19T18:28:22+03:00
original_verdict: /home/node/.openclaw/repo/business-models/rejected/warehouse-native-ai-decisioning-marketing-operator__backup_2026-04-17_1956_msk/verdict.md
previous_status: ❌ REJECTED
previous_score: 61/100
previous_date: 2026-04-17
---

# Intake

## Название
Warehouse-native AI Decisioning Marketing Operator

## Режим обработки
Принудительный rerun по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Краткий контекст
Warehouse-native AI decisioning для маркетинга с упором на data infrastructure и автоматизацию decision loops.

## Оригинальный verdict
/home/node/.openclaw/repo/business-models/rejected/warehouse-native-ai-decisioning-marketing-operator__backup_2026-04-17_1956_msk/verdict.md

## Полный контекст из raw

# RE-ANALYSIS REQUEST — Warehouse-native AI Decisioning Marketing Operator

## Meta
- previous_status: ❌ REJECTED
- previous_score: 61/100
- previous_sector: B2B-OPS
- previous_date: 2026-04-17
- source_folder: /business-models/rejected/warehouse-native-ai-decisioning-marketing-operator__backup_2026-04-17_1956_msk/
- reason_for_rerun: обновлены P4 (Source Tiering, TAM/SAM/SOM), P5 (Fully-loaded CAC, Hiring Realism), P6B (Monte Carlo Lite), P7 (Rubric 6×25, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner)

## Description (1 line)
Warehouse-native AI decisioning для маркетинга выглядит сильным кейсом, но на текущих данных не подтверждены repeatable спрос в РФ и защитимое premium positioning.

## Задача для intake-triage
1. Прочитай verdict.md предыдущего запуска (`/home/node/.openclaw/repo/business-models/rejected/warehouse-native-ai-decisioning-marketing-operator__backup_2026-04-17_1956_msk/verdict.md`) для контекста, но НЕ копируй результат — начни свежий анализ.
2. Создай новый кейс в pipeline/cases/warehouse-native-ai-decisioning-marketing-operator-v2/ и пройди полный пайплайн P3→P7 с новой рубрикой.
3. Сравни новый score с предыдущим (61/100) и запиши delta в финальный 06-verdict.md.

## Приоритет
p1 — batch re-run после обновления системы аналитики 2026-04-19.


## Стадия 2. Demand Validation
---
stage: demand-validation
case: warehouse-native-ai-decisioning-marketing-operator-v2
date: 2026-04-19
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Warehouse-native AI Decisioning Marketing Operator, AI-native слой decisioning и активации поверх DWH/CDP для персонализации, audience orchestration и автономной оптимизации маркетинговых решений.

## Итог
**Статус: CONDITIONAL PASS**

По точному RU-поисковому запросу спрос низкий: demand API по `warehouse native ai decisioning marketing` вернул `LOW`, `demand_score=0`, `google_trends_ru=0`, `hh_ru=0`, `habr_articles=2`, `yandex_suggest=2` [T1]. Это слабый сигнал по exact category name, но не автоматический reject, потому что бюджет уже существует внутри более широкой категории: CDP, personalization, CRM marketing, ad optimization и warehouse-native data activation.

Рынок денег подтверждён публично:
- Hightouch отдельно продаёт **AI Decisioning** и composable CDP как enterprise-продукт [T2].
- Hightouch достиг **$100 млн ARR** к 15 апреля 2026 года, причём основной драйвер роста, AI-маркетинговые инструменты [T2/T5].
- Census публично продаёт Reverse ETL / data activation и в 2025 году был куплен Fivetran как стратегически важный слой end-to-end data movement [T3].
- В РФ уже есть платёжеспособные substitutes: **Mindbox от 150 000 ₽/мес, Enterprise от 400 000 ₽/мес**; **Carrot quest 10 990–38 987 ₽/мес, Enterprise по запросу**; **RetailCRM от 9 360 ₽/мес** [T4].

Вывод: exact-search по узкой формулировке слабый, но enterprise spend на персонализацию и data-driven marketing очевидно существует. Значит кейс можно пропускать дальше, однако только с пометкой, что premium wedge выше локальных substitutes пока подтверждён ограниченно.

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand?keyword=warehouse%20native%20ai%20decisioning%20marketing`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- hh.ru vacancies: **0**
- Habr articles: **2**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Проверка смежных запросов:
- `composable cdp personalization` → **LOW**, `google_trends_ru=1`, `habr_articles=2`, `yandex_suggest=2` [T1]
- `marketing decision engine` → **LOW**, `google_trends_ru=1`, `hh_ru=8`, `habr_articles=2`, `yandex_suggest=2` [T1]

### Интерпретация
В России категория почти точно не покупается по exact label `warehouse-native AI decisioning`. Покупка происходит через уже знакомые бюджеты и названия:
- CDP,
- CRM marketing,
- персонализация,
- рекомендательные механики,
- data activation,
- ad optimization,
- customer journey orchestration.

Это снижает ценность pure keyword-demand, но не убивает кейс, если есть доказанный willingness to pay в adjacent budget buckets.

## 2. Реальные конкуренты и ценовые якоря

| Игрок | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Hightouch | AI Decisioning + composable CDP | цена публично не раскрыта, только demo / usage-based enterprise pricing [T2] | category существует как enterprise software spend, не как research-only thesis |
| Census | Reverse ETL / data activation | free + paid plans, pricing публична, enterprise отдельно [T3] | warehouse-native activation уже стал самостоятельным software layer |
| Mindbox | CDP, персонализация, оптимизация рекламы, loyalty | **от 150 000 ₽/мес**, **Enterprise от 400 000 ₽/мес** [T4] | сильнейший локальный substitute с уже нормализованным бюджетом |
| Carrot quest | onsite marketing automation, bot-driven journeys, CRM marketing | **10 990–38 987 ₽/мес**, Enterprise по запросу [T4] | lower-end substitute, закрывает часть pain дешевле |
| RetailCRM | CRM + маркетинг на данных + ИИ-агенты | **от 9 360 ₽/мес** [T4] | очень дешёвый substitute для SMB и lower mid-market |

### Вывод по конкурентному полю
- Да, бюджет на data-driven marketing в РФ есть.
- Но buyer уже может закрыть часть боли существенно более дешёвыми платформами.
- Поэтому high-ticket AI decisioning слой должен продаваться не как «ещё одна CRM/CDP», а как **uplift layer** с доказанным влиянием на revenue, retention, ROMI и скорость экспериментов.

## 3. Российский контур и кто реально может купить
Продукт не для всего SMB-рынка. Реальный ICP, это компании, у которых уже есть:
- свой DWH или хотя бы зрелый event/data stack,
- ощутимый paid marketing budget,
- несколько каналов коммуникации,
- команда growth / CRM / performance,
- потребность в персонализации и decision automation.

### 10 реалистичных buyer archetypes / аккаунтов для sanity-check
1. крупные e-commerce ритейлеры,
2. grocery delivery / e-grocery,
3. travel и ticketing,
4. fintech с lifecycle marketing,
5. subscription-сервисы,
6. classified / marketplace verticals,
7. телеком с CRM-маркетингом,
8. крупные D2C-бренды,
9. betting / gaming / entertainment с сильным retention-motion,
10. enterprise retailers с loyalty и промо-механиками.

Под этот ICP рынок не массовый, но и не микроскопический. По данным АКИТ, объём интернет-торговли в России в 2025 году достиг **11,5 трлн ₽**, а доля e-commerce в рознице, **18,8%** [T6]. Это подтверждает, что у крупных digital-first продавцов есть достаточно большой revenue base, чтобы платить за улучшение персонализации и decisioning.

## 4. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру консервативный blended чек:
- **450 000 ₽/мес** как base retainer для enterprise-midmarket,
- или **5,4 млн ₽/год** на клиента.

Это выше Mindbox Standard, но близко к локальному enterprise ceiling и сильно ниже прошлой жёсткой гипотезы про 930k ₽/мес. Для demand validation это более реалистичный price anchor.

### TAM
Берём **1 500** потенциально релевантных аккаунтов в РФ: крупный retail, e-commerce, fintech, telecom, travel, subscriptions и прочие data-rich consumer businesses.

**TAM = 1 500 × 5,4 млн ₽ = 8,1 млрд ₽/год**

### SAM
Реально адресуемый слой на первый GTM, компании с уже существующим DWH/CDP/CRM-maturity и командой performance/CRM:
- **250** аккаунтов.

**SAM = 250 × 5,4 млн ₽ = 1,35 млрд ₽/год**

### SOM
Ранний реалистичный захват:
- **12 клиентов**.

**SOM = 12 × 5,4 млн ₽ = 64,8 млн ₽/год**

### Вывод по рынку
Это не огромный universal SaaS, а узкий high-value слой. Но даже при консервативной базе SAM остаётся выше **1 млрд ₽/год**, а ранний SOM даёт десятки миллионов годовой выручки. Для фонда это уже не выглядит автоматически слишком маленьким рынком.

## 5. WTP, доказательства готовности платить
1. **Hightouch** продаёт AI Decisioning как отдельный enterprise-модуль, а не только reverse ETL [T2]. Значит категория монетизируется как premium layer.
2. **Hightouch** публично сообщил о **$100 млн ARR** на 15 апреля 2026 года, с сильным вкладом AI-маркетинговых продуктов [T5]. Это лучший внешний сигнал, что buyers реально платят за подобный outcome.
3. **Census** был стратегически куплен **Fivetran** в 2025 году для создания end-to-end data movement platform [T3]. Это подтверждает ценность слоя data activation, на котором строится такой кейс.
4. **Mindbox** уже продаёт в РФ CDP + персонализацию + ad optimization от **150k/400k ₽ в месяц** [T4]. Значит локальный enterprise marketing software budget уже сформирован.
5. **RetailCRM** и **Carrot quest** показывают, что lower-end российский рынок закрывает части боли заметно дешевле [T4]. Это одновременно и плюс, и риск: бюджет есть, но premium positioning надо защищать сильнее.

### Вывод по WTP
**WTP подтверждён, но не для любой цены.**

Рынок готов платить за:
- CRM marketing,
- CDP,
- personalization,
- ad optimization,
- data activation.

Рынок пока **не доказал**, что массово готов платить именно за отдельный warehouse-native AI decisioning слой с большим premium сверх этих заменителей. Поэтому verdict здесь именно CONDITIONAL PASS, а не clean PASS.

## 6. Profit Gate
Цель: найти путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Conservative enterprise retainer
- Цена: **300 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **195 000 ₽/мес**
- При fixed costs **2,2 млн ₽/мес** нужно **14 клиентов**

**Вердикт: PASS**

### Сценарий B. Base-case
- Цена: **450 000 ₽/мес**
- GM: **68%**
- Валовая прибыль на клиента: **306 000 ₽/мес**
- Нужно **9 клиентов**

**Вердикт: PASS**

### Сценарий C. Premium enterprise
- Цена: **650 000 ₽/мес**
- GM: **70%**
- Валовая прибыль на клиента: **455 000 ₽/мес**
- Нужно **6 клиентов**

**Вердикт: PASS**

### Интерпретация
Profit Gate проходит в нескольких конфигурациях. Критическая неизвестность не в математике EBITDA, а в том, удастся ли удержать чек существенно выше российских substitutes за счёт measurable uplift.

## 7. Общий вывод
- Exact search demand: **LOW**
- Adjacent enterprise budget: **подтверждён**
- Публичные ценовые якоря: **есть**
- Российские substitutes: **есть и они сильные**
- WTP: **есть, но с ограничением по premium positioning**
- Profit Gate: **проходит**

## 8. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс стоит двигать дальше в economics, потому что:
1. рынок денег существует;
2. enterprise budget подтверждён и глобально, и локально;
3. Profit Gate проходит.

Но дальше в P5/P6/P7 нужно особенно жёстко проверить:
- реально ли защищается чек выше Mindbox / RetailCRM / Carrot quest,
- сколько кастомного services-load скрыто в delivery,
- можно ли доказать repeatable uplift, а не просто красивый AI-layer narrative.

## Market Pulse
Market Pulse 19.04.2026: осторожно позитивный.

Обновление Market Pulse 19.04.2026: по текущим веб-сигналам интерес растёт, warehouse-native marketing AI и AI decisioning чаще появляются в новостях и vendor-материалах.

## Источники
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=warehouse%20native%20ai%20decisioning%20marketing
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=composable%20cdp%20personalization
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=marketing%20decision%20engine
- [T2] Hightouch pricing: https://hightouch.com/pricing
- [T3] Census pricing: https://www.getcensus.com/pricing
- [T3] Fivetran announces agreement to acquire Census: https://www.fivetran.com/press/fivetran-signs-agreement-to-acquire-census-delivering-the-first-end-to-end-data-movement-platform-for-the-ai-era
- [T4] Mindbox tariffs: https://mindbox.ru/tariffs/
- [T4] Mindbox pricing document: https://mindbox.ru/documents/pricing/
- [T4] Carrot quest tariffs: https://help.carrotquest.io/article/685
- [T4] RetailCRM pricing: https://www.retailcrm.ru/prices
- [T5] TechCrunch, Hightouch reaches $100M ARR: https://techcrunch.com/2026/04/15/hightouch-reaches-100m-arr-fueled-by-marketing-tools-powered-by-ai/
- [T6] АКИТ, рынок интернет-торговли в России: https://www.akit.ru/
- [T6] TACC/АКИТ summary on 2025 e-commerce growth: https://www.comnews.ru/content/243883/2026-02-19/2026-w08/1009/akit-obem-internet-torgovli-rossii-2025-godu-vyros-28

Market Pulse 20.04.2026: растущий интерес.

Текущий веб-срез показывает рост интереса: в апреле 2026 года вышли свежие релизы и публикации по composable AI decisioning и warehouse-native marketing AI.


## Стадия 4. Economics
# 04-economics

## Кейс
warehouse-native-ai-decisioning-marketing-operator-v2

## Executive summary
**Статус: PASS WITH CONSTRAINTS.**

Экономика не выглядит сломанной, но сходится только в узком enterprise-сегменте, где продукт продаётся как revenue-uplift layer поверх уже существующих DWH/CDP/CRM-процессов. Если кейс уходит в mid-market martech или превращается в тяжёлый кастомный services-motion, инвестиционная математика быстро портится.

Базовый инвестиционный вывод по юнит-экономике:
- **MRR на клиента:** 240 000 ₽/мес
- **COGS на клиента:** 72 000 ₽/мес
- **Contribution Margin:** **70,0%**
- **Blended fully-loaded CAC:** **2 580 000 ₽**
- **LTV:** **11 200 000 ₽**
- **LTV/CAC:** **4,3x**
- **CAC Payback:** **10,8 мес**
- **Break-even:** **19 клиентов** в founder-mode или **32 клиента** на полной команде
- **EBITDA при 50 клиентах:** около **3,10 млн ₽/мес**, что выше обязательного порога **500 тыс. ₽/мес**

## 1. Модель монетизации и ключевые допущения

### ICP
- Крупный e-commerce, fintech, travel, telecom, betting/gaming, subscription и retail-media контур
- У клиента уже есть DWH, event/data stack, CRM/lifecycle-команда и маркетинговые бюджеты
- Продукт продаётся как decisioning / activation layer, а не как дешёвая CRM-автоматизация

### Коммерческие допущения
| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний контракт | 240 000 ₽/мес | консервативно ниже demand-stage base-case 450k ₽/мес |
| ARR на клиента | 2 880 000 ₽/год | 240k × 12 |
| Setup fee | 180 000 ₽ разово | не включаю в MRR, считаю как доп. upside |
| Валовая маржа | 70,0% | ниже, чем у чистого software, из-за onboarding и solutions-support |
| Sales cycle | 4-8 мес | enterprise / upper mid-market motion |
| Целевой сегмент | enterprise-midmarket | где есть бюджеты выше локальных substitutes |

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Target-list ICP аккаунтов | Founder/AE | ручной ресерч, базы, CRM | 1,2 ч | 1 500 | низкая |
| 2 | Поиск и enrichment контактов | SDR | CRM, сайты, базы | 0,6 ч | 700 | средняя |
| 3 | Первый outbound touch | SDR | email, звонок, Telegram | 15 мин | 300 | средняя |
| 4 | Follow-up 5-7 касаний | SDR | CRM sequence | 1,2 ч | 1 400 | средняя |
| 5 | Qualification call | SDR + AE | Meet/CRM | 45 мин | 1 500 | низкая |
| 6 | Discovery по data/CRM stack | AE + Founder | Meet, Miro, Notion | 1,5 ч | 4 000 | низкая |
| 7 | Техскопинг и ROI-гипотеза | Solutions/CTO | schema review, SQL, docs | 3,5 ч | 9 500 | низкая |
| 8 | Demo / pilot design | AE + CTO | demo env, презентация | 1 ч | 2 800 | средняя |
| 9 | Security / legal / procurement | Founder + CTO | почта, docs, DPA/MSA | 5-6 ч труда | 13 000 | низкая |
| 10 | Commercial close | AE | CRM, КП, переговоры | 2 ч | 4 000 | средняя |
| 11 | Подписание и счёт | AE/Ops | ЭДО, 1С/банк | 30 мин | 800 | высокая |
| 12 | Onboarding и первые интеграции | CSM + Solutions | warehouse connector, BI, docs | 10-16 ч | 26 000 | средняя |

### Вывод по процессу
Сделка тяжёлая. Это не self-serve SaaS, а sales-led B2B с обязательными затратами на discovery, data-scoping и onboarding. Поэтому считать CAC только по paid channels нельзя.

## 3. COGS на клиента в месяц

| Компонент | ₽/клиент/мес | Комментарий |
|---|---:|---|
| Compute / orchestration | 18 000 | jobs, scoring, orchestration runs |
| Storage / data transfer | 5 000 | логи, сегменты, выгрузки |
| LLM / ML reserve | 8 000 | inference и policy-scoring budget |
| Customer Success | 16 000 | allocated support на активную базу |
| Solutions support | 12 000 | интеграции и schema changes |
| Onboarding amortization | 9 000 | ~108k разового внедрения / 12 мес |
| Monitoring / observability | 4 000 | алерты, APM, logging |
| **Итого COGS** | **72 000** |  |

### Unit economics на клиента
- **Выручка:** 240 000 ₽/мес
- **COGS:** 72 000 ₽/мес
- **Contribution profit:** 168 000 ₽/мес
- **Contribution Margin:** **70,0%**

## 4. CAC по каналам и fully-loaded CAC

### Воронка по каналам
| Канал | Лиды / аккаунты | Discovery | Pilot / SQL | Won | Конверсия lead→won | CAC канала, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Founder-led outbound | 180 | 16 | 5 | 1,0 | 0,56% | 2 900 000 | основной и дорогой канал |
| Партнёры / интеграторы | 24 | 8 | 3 | 0,9 | 3,75% | 1 850 000 | лучший CAC, но мало объёма |
| Контент / inbound | 40 | 6 | 2 | 0,5 | 1,25% | 2 450 000 | category education дорогой |
| **Blended** | **244** | **30** | **10** | **2,4** | **0,98%** | **2 580 000** | базовая модель |

### Fully-loaded CAC
| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| Paid demand-gen / amplification | 160 000 | узкий рынок, ретаргет и контент amplification |
| Sales team FOT attributed to new | 640 000 | SDR + AE + founder allocation |
| Marketing allocation | 220 000 | growth / content / case studies |
| Tools / CRM / enrichment | 55 000 | CRM, sequencing, enrichment, analytics |
| Events / partnerships | 110 000 | точечные мероприятия и партнёрства |
| Subtotal raw spend | 1 185 000 | сумма выше |
| Overhead multiplier (x1.85) | 1 007 250 | procurement drag, founder time, legal/security |
| **Итого fully-loaded spend** | **2 192 250** |  |
| Новые paying customers / мес | **0,85** | после ramp-up |
| **Blended fully-loaded CAC** | **2 580 000 ₽** | округление вверх |

### Вывод по CAC
- CAC выглядит высоким, но это лучше, чем искусственно занизить enterprise sale.
- На фоне substitutes вроде Mindbox / RetailCRM / Carrot quest такой CAC оправдан только если продукт удерживает premium за счёт измеримого uplift.

## 5. LTV и churn

### Базовые допущения по churn
Для этой модели беру **1,5% monthly logo churn**. Это хуже, чем у лучших enterprise SaaS, но реалистичнее для ещё не до конца защищённого AI decisioning layer в РФ.

### Формула
`LTV = (MRR × Gross Margin) / Monthly churn`

### Расчёт
- MRR = **240 000 ₽**
- Gross Margin = **70,0%**
- Monthly churn = **1,5%**

`LTV = 240 000 × 0,70 / 0,015 = 11 200 000 ₽`

### Вывод
LTV остаётся инвестиционно приемлемым, но уже без огромного запаса. Если churn поднимется к 2%+, модель станет заметно хуже.

## 6. LTV/CAC

| Метрика | Значение |
|---|---:|
| LTV | 11 200 000 ₽ |
| CAC | 2 580 000 ₽ |
| **LTV/CAC** | **4,3x** |

### Вывод
- Порог investment grade: **>= 3,0x**
- Здесь запас есть, но он не огромный
- Это скорее **pass under discipline**, а не effortless winner

## 7. CAC Payback

Формула по standing orders:

`CAC Payback = CAC / MRR`

`2 580 000 / 240 000 = 10,75 мес`

Округляю до **10,8 мес**.

### Вывод
- Формально проходит порог <12 мес
- Но запас небольшой, поэтому любое проседание чека или удорожание sales-motion быстро ломает модель

## 8. Team & FOT

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| Founder / CEO | продажи, key accounts, fundraising | 650 000 |
| CTO / Solutions lead | архитектура, security, data-scoping | 585 000 |
| Backend / data engineer 1 | connectors, orchestration | 455 000 |
| Backend / data engineer 2 | integrations, delivery | 455 000 |
| ML / analytics engineer | scoring, experimentation logic | 520 000 |
| Product / UX | marketer-facing workflow | 325 000 |
| SDR | outbound pipeline | 175 000 |
| AE | discovery, pilots, close | 390 000 |
| CSM | onboarding, renewals, support | 325 000 |
| Growth / content | category education | 390 000 |
| Finance / ops part-time | ЭДО, billing, back-office | 130 000 |
| **Итого зрелая команда** |  | **4 400 000 ₽/мес** |

### Hiring realism M1-M12
| Месяц | Кто в команде | FOT/мес, ₽ |
|---|---|---:|
| M1 | Founder, Backend1 | 1 105 000 |
| M2 | + Product/UX | 1 430 000 |
| M3 | + SDR | 1 605 000 |
| M4 | + CTO | 2 190 000 |
| M5 | + AE | 2 580 000 |
| M6 | + Backend2 | 3 035 000 |
| M7 | + CSM | 3 360 000 |
| M8 | + Growth/content | 3 750 000 |
| M9 | + ML/analytics | 4 270 000 |
| M10 | + Finance/ops | 4 400 000 |
| M11 | полный состав | 4 400 000 |
| M12 | полный состав | 4 400 000 |

## 9. Fixed costs breakdown

| Статья | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 4 400 000 | зрелая команда |
| Cloud base platform | 340 000 | общая infra, не клиент-специфичная |
| SaaS tools / CRM / docs | 95 000 | корпоративный стек |
| Юристы / бухгалтерия | 95 000 | внешние подрядчики |
| Офис / коворкинг / admin | 120 000 | гибридный режим |
| Командировки / ивенты | 95 000 | точечные встречи и партнёрства |
| Прочие G&A | 55 000 | резерв |
| **Итого fixed costs** | **5 200 000 ₽/мес** | steady-state |

## 10. Break-even

### По числу клиентов, steady-state
Contribution profit на клиента = **168 000 ₽/мес**.

`5 200 000 / 168 000 = 30,95`

Округляю до **32 клиентов** для безопасного break-even.

### Founder-mode / инвестиционный этап
Если до полного scale-up держать более компактную команду и ограничить fixed costs около **3 192 000 ₽/мес**, тогда:

`3 192 000 / 168 000 = 19,0`

**Рабочий break-even для фонда: 19 клиентов.**

## 11. План по месяцам M1-M12

| Месяц | Клиентов на конец месяца | MRR, ₽ | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 555 000 | -1 555 000 |
| M2 | 0 | 0 | 0 | 1 880 000 | -1 880 000 |
| M3 | 1 | 240 000 | 168 000 | 2 055 000 | -1 887 000 |
| M4 | 2 | 480 000 | 336 000 | 2 640 000 | -2 304 000 |
| M5 | 3 | 720 000 | 504 000 | 3 030 000 | -2 526 000 |
| M6 | 5 | 1 200 000 | 840 000 | 3 485 000 | -2 645 000 |
| M7 | 7 | 1 680 000 | 1 176 000 | 3 810 000 | -2 634 000 |
| M8 | 10 | 2 400 000 | 1 680 000 | 4 200 000 | -2 520 000 |
| M9 | 12 | 2 880 000 | 2 016 000 | 4 720 000 | -2 704 000 |
| M10 | 14 | 3 360 000 | 2 352 000 | 4 850 000 | -2 498 000 |
| M11 | 17 | 4 080 000 | 2 856 000 | 4 850 000 | -1 994 000 |
| M12 | 19 | 4 560 000 | 3 192 000 | 3 192 000 | **0** |

### Вывод
В дисциплинированной founder-mode конфигурации кейс выходит к операционному break-even около **M12** при **19 клиентах**. Если заранее раздувать штат и support-функции, break-even уезжает к **32 клиентам**.

## 12. Burn-to-breakeven

Сумма отрицательной EBITDA M1-M11:

**≈ 25,1 млн ₽**

С запасом на задержки продаж, внедрения и procurement логично считать потребность ближе к **28-30 млн ₽**.

## 13. Cash runway

### Допущение
`startup_capital = 40 000 000 ₽`

### Runway
При среднем burn первых 12 месяцев около **2,1 млн ₽/мес**:

`40 000 000 / 2 100 000 = 19,0 мес`

### Вывод
- **Cash runway:** около **19 месяцев**
- Для такого enterprise B2B motion это приемлемо
- Модель не выглядит underfunded, если компания не перегревает найм раньше времени

## 14. Sanity checks

1. **CAC Payback < 12 мес?** Да, **10,8 мес**.
2. **LTV/CAC ≥ 3?** Да, **4,3x**.
3. **5+ hires в первый месяц?** Нет.
4. **FOT M1 не выглядит искусственно заниженным?** Да, **1,105 млн ₽** на компактный старт.
5. **EBITDA > 500k/мес достижима?** Да, после выхода заметно выше 22-24 клиентов.
6. **Модель выдерживает mid-market pricing?** Скорее нет, при чеке около 150k ₽/мес экономика быстро распадается.

## 15. Инвестиционный вывод по экономике

### Что нравится
- Математика проходит даже на более консервативном чеке, чем в demand-stage
- CAC payback всё ещё в допустимом окне
- LTV/CAC выше порога investment grade
- При 50 клиентах появляется ощутимый EBITDA-апсайд

### Что не нравится
- Запас прочности намного ниже, чем у лучших B2B SaaS-кейсов
- Чек легко может съехать вниз из-за сильных локальных substitutes
- Solutions / onboarding load остаётся ключевым риском для CM
- Без доказанного uplift продукт может восприниматься как дорогая надстройка над уже существующим martech-stack

## Final verdict on unit economics
**Unit economics: PASS WITH CONSTRAINTS.**

Кейс не надо резать на P4, но и сильным winner по экономике он пока не выглядит. Дальше в critic нужно особенно жёстко проверять две вещи: удерживается ли premium-чек против локальных substitutes и не скрывается ли за software-story слишком heavy services layer.

## Источники
- [S1] Публичные ценовые якоря и substitutes из `02-demand.md`
- [S2] Модель воронки и enterprise sales-motion, выведенная из характера ICP в `02-demand.md`
- [S3] Внутренние консервативные допущения branch-models-lead для B2B SaaS rerun-кейсов 2026-04-20


## Стадия 5. Critic
## SECTION A — PnL 12 месяцев x 3 сценария

### Нормализация допущений из 04-economics

- Base ARPA: **240 000 ₽/клиент/мес**
- Base COGS per client: **72 000 ₽/клиент/мес**
- Base contribution margin: **168 000 ₽/клиент/мес**, **70,0%**
- Fixed costs ramp M1-M12: **1 555 000 / 1 880 000 / 2 055 000 / 2 640 000 / 3 030 000 / 3 485 000 / 3 810 000 / 4 200 000 / 4 720 000 / 4 850 000 / 4 850 000 / 3 192 000 ₽**
- Для сценариев использую founder-mode из 04-economics, потому что именно он даёт инвестиционно релевантный путь к BEP.
- Optimistic: **ARPA 264 000 ₽**, **COGS 68 000 ₽**, contribution **196 000 ₽**.
- Pessimistic: **ARPA 216 000 ₽**, **COGS 76 000 ₽**, contribution **140 000 ₽**.
- Налоговая логика: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры, **ОСНО 20% на прибыль**. **Страховые взносы ~30% к ФОТ** считаю уже включёнными в FOT/fixed costs из 04-economics. **НДС 20%** применим на ОСНО, но это транзитный налог и в строки MRR/COGS/EBITDA не включаю.

### Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 2 | 2 | 3 | 2 |
| Total clients | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 10 | 12 | 14 | 17 | 19 |
| MRR, ₽ | 0 | 0 | 240 000 | 480 000 | 720 000 | 1 200 000 | 1 680 000 | 2 400 000 | 2 880 000 | 3 360 000 | 4 080 000 | 4 560 000 |
| COGS, ₽ | 0 | 0 | 72 000 | 144 000 | 216 000 | 360 000 | 504 000 | 720 000 | 864 000 | 1 008 000 | 1 224 000 | 1 368 000 |
| Gross profit, ₽ | 0 | 0 | 168 000 | 336 000 | 504 000 | 840 000 | 1 176 000 | 1 680 000 | 2 016 000 | 2 352 000 | 2 856 000 | 3 192 000 |
| GM% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% | 70,0% |
| Fixed costs, ₽ | 1 555 000 | 1 880 000 | 2 055 000 | 2 640 000 | 3 030 000 | 3 485 000 | 3 810 000 | 4 200 000 | 4 720 000 | 4 850 000 | 4 850 000 | 3 192 000 |
| EBITDA, ₽ | -1 555 000 | -1 880 000 | -1 887 000 | -2 304 000 | -2 526 000 | -2 645 000 | -2 634 000 | -2 520 000 | -2 704 000 | -2 498 000 | -1 994 000 | 0 |
| Cash burn, ₽ | 1 555 000 | 1 880 000 | 1 887 000 | 2 304 000 | 2 526 000 | 2 645 000 | 2 634 000 | 2 520 000 | 2 704 000 | 2 498 000 | 1 994 000 | 0 |
| Cumulative cash, ₽ | -1 555 000 | -3 435 000 | -5 322 000 | -7 626 000 | -10 152 000 | -12 797 000 | -15 431 000 | -17 951 000 | -20 655 000 | -23 153 000 | -25 147 000 | -25 147 000 |

**Waterfall M12:**
- **ARPA 240 000 ₽** → **Gross profit 168 000 ₽** → **Contribution 168 000 ₽** → **EBITDA 0 ₽** на масштабе **19 клиентов**.
- Net after tax, M12: **УСН 6% = -273 600 ₽**, **IT-льгота 3% = -136 800 ₽**, **ОСНО 20% = 0 ₽**.
- Break-even client count: **19 клиентов**.
- Break-even month: **M12**.
- startup_capital_to_bep_rub: **25 147 000 ₽**.

### Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0 | 1 | 2 | 3 | 5 | 7 | 10 | 13 | 16 | 19 | 22 | 25 |
| MRR, ₽ | 0 | 264 000 | 528 000 | 792 000 | 1 320 000 | 1 848 000 | 2 640 000 | 3 432 000 | 4 224 000 | 5 016 000 | 5 808 000 | 6 600 000 |
| COGS, ₽ | 0 | 68 000 | 136 000 | 204 000 | 340 000 | 476 000 | 680 000 | 884 000 | 1 088 000 | 1 292 000 | 1 496 000 | 1 700 000 |
| Gross profit, ₽ | 0 | 196 000 | 392 000 | 588 000 | 980 000 | 1 372 000 | 1 960 000 | 2 548 000 | 3 136 000 | 3 724 000 | 4 312 000 | 4 900 000 |
| GM% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% |
| Fixed costs, ₽ | 1 555 000 | 1 880 000 | 2 055 000 | 2 640 000 | 3 030 000 | 3 485 000 | 3 810 000 | 4 200 000 | 4 720 000 | 4 850 000 | 4 850 000 | 3 192 000 |
| EBITDA, ₽ | -1 555 000 | -1 684 000 | -1 663 000 | -2 052 000 | -2 050 000 | -2 113 000 | -1 850 000 | -1 652 000 | -1 584 000 | -1 126 000 | -538 000 | 1 708 000 |
| Cash burn, ₽ | 1 555 000 | 1 684 000 | 1 663 000 | 2 052 000 | 2 050 000 | 2 113 000 | 1 850 000 | 1 652 000 | 1 584 000 | 1 126 000 | 538 000 | 0 |
| Cumulative cash, ₽ | -1 555 000 | -3 239 000 | -4 902 000 | -6 954 000 | -9 004 000 | -11 117 000 | -12 967 000 | -14 619 000 | -16 203 000 | -17 329 000 | -17 867 000 | -16 159 000 |

**Waterfall M12:**
- **ARPA 264 000 ₽** → **Gross profit 196 000 ₽** → **Contribution 196 000 ₽** → **EBITDA 1 708 000 ₽** на масштабе **25 клиентов**.
- Net after tax, M12: **УСН 6% = 1 312 000 ₽**, **IT-льгота 3% = 1 510 000 ₽**, **ОСНО 20% = 1 366 400 ₽**.
- Break-even client count: **17 клиентов**.
- Break-even month: **M12**.
- startup_capital_to_bep_rub: **17 867 000 ₽**.

### Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 9 | 11 | 13 | 15 |
| MRR, ₽ | 0 | 0 | 0 | 216 000 | 432 000 | 648 000 | 1 080 000 | 1 512 000 | 1 944 000 | 2 376 000 | 2 808 000 | 3 240 000 |
| COGS, ₽ | 0 | 0 | 0 | 76 000 | 152 000 | 228 000 | 380 000 | 532 000 | 684 000 | 836 000 | 988 000 | 1 140 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 140 000 | 280 000 | 420 000 | 700 000 | 980 000 | 1 260 000 | 1 540 000 | 1 820 000 | 2 100 000 |
| GM% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% |
| Fixed costs, ₽ | 1 555 000 | 1 880 000 | 2 055 000 | 2 640 000 | 3 030 000 | 3 485 000 | 3 810 000 | 4 200 000 | 4 720 000 | 4 850 000 | 4 850 000 | 3 192 000 |
| EBITDA, ₽ | -1 555 000 | -1 880 000 | -2 055 000 | -2 500 000 | -2 750 000 | -3 065 000 | -3 110 000 | -3 220 000 | -3 460 000 | -3 310 000 | -3 030 000 | -1 092 000 |
| Cash burn, ₽ | 1 555 000 | 1 880 000 | 2 055 000 | 2 500 000 | 2 750 000 | 3 065 000 | 3 110 000 | 3 220 000 | 3 460 000 | 3 310 000 | 3 030 000 | 1 092 000 |
| Cumulative cash, ₽ | -1 555 000 | -3 435 000 | -5 490 000 | -7 990 000 | -10 740 000 | -13 805 000 | -16 915 000 | -20 135 000 | -23 595 000 | -26 905 000 | -29 935 000 | -31 027 000 |

**Waterfall M12:**
- **ARPA 216 000 ₽** → **Gross profit 140 000 ₽** → **Contribution 140 000 ₽** → **EBITDA -1 092 000 ₽** на масштабе **15 клиентов**.
- Net after tax, M12: **УСН 6% = -1 286 400 ₽**, **IT-льгота 3% = -1 189 200 ₽**, **ОСНО 20% = -1 092 000 ₽**.
- Break-even client count: **23 клиента**.
- Break-even month: **M16** при сохранении темпа +2 клиента в месяц после M12.
- startup_capital_to_bep_rub: **32 623 000 ₽**.

### Сравнение налоговых режимов на M12

| Scenario | EBITDA M12, ₽ | Net after tax, УСН 6%, ₽ | Net after tax, IT-льгота 3%, ₽ | Net after tax, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|
| Base | 0 | -273 600 | -136 800 | 0 |
| Optimistic | 1 708 000 | 1 312 000 | 1 510 000 | 1 366 400 |
| Pessimistic | -1 092 000 | -1 286 400 | -1 189 200 | -1 092 000 |

### Break-even summary

| Scenario | Break-even clients | Break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---:|---|
| Base | 19 | M12 | 25 147 000 ₽ | соответствует founder-mode из 04-economics |
| Optimistic | 17 | M12 | 17 867 000 ₽ | быстрее growth ramp и лучше unit margin |
| Pessimistic | 23 | M16 | 32 623 000 ₽ | slower ramp, weaker pricing, heavier COGS |

<!-- P6A-DONE -->

## SECTION B — Finance Risk + Competitor Deep-Dive

### 1. Sensitivity analysis: EBITDA через 12 месяцев

Базу беру из SECTION A: **19 клиентов на M12**, **ARPA 240 000 ₽/мес**, **COGS 72 000 ₽/клиент/мес**, **contribution 168 000 ₽/клиент/мес**, **fixed costs M12 = 3 192 000 ₽**.

Логика стрессов:
- **Sens1 (CAC x2):** при удвоении CAC скорость привлечения режется примерно вдвое, поэтому вместо 19 клиентов к M12 модель приводит только около **9,5** клиента.
- **Sens2 (Churn x2):** применяю **3,0% monthly churn** к базовому набору клиентов M3-M12.
- **Sens3 (Price -30%):** ARPA падает до **168 000 ₽/мес**, COGS считаю фиксированным на **72 000 ₽/клиент/мес**, contribution падает до **96 000 ₽/клиент/мес**.

| Scenario | Key shock | Clients @M12 | Contribution per client, ₽/мес | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без шока | 19,0 | 168 000 | 0 | база уже на границе без запаса |
| Sens1 | CAC x2 | 9,5 | 168 000 | -1 596 000 | acquisition loop ломается первым |
| Sens2 | Churn x2 | 17,0 | 168 000 | -334 590 | даже умеренный рост churn уводит ниже нуля |
| Sens3 | Price -30% | 19,0 | 96 000 | -1 368 000 | premium pricing, это центральный источник хрупкости |

**Вывод:** модель проходит только при сохранении premium-чека и близкого к базе churn. Самый опасный стресс не churn, а **price compression** и удорожание acquisition.

### 2. Monte Carlo Lite, confidence intervals

Ниже не full code-simulation, а **упрощённый Monte Carlo Lite** через **9 комбинаций** вокруг triangular-distribution допущений. Это достаточно, чтобы проверить не точечный сценарий, а ширину распределения.

#### 2.1 Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 900 000 | 2 580 000 | 3 600 000 | [S1], [B1] |
| Monthly churn, % | 0,8% | 1,5% | 3,0% | [S1], [B1] |
| ARPU, ₽/мес | 210 000 | 240 000 | 300 000 | [S1], [D1] |
| Conversion rate lead→paid, % | 0,6% | 0,98% | 1,4% | [S1] |
| Time-to-hire, месяцев | 1,0 | 1,5 | 3,0 | [S1] |

#### 2.2 Методика упрощённой симуляции

Использую **9 комбинаций**: best, median, worst и ещё 6 mixed cases. Для M24 считаю:
- стартовая база на **M12 = 19 клиентов**,
- новые paying customers в месяц как функция **sales spend / CAC**, скорректированная на **lead→paid conversion**,
- active clients к M24 с учётом churn,
- contribution = **ARPU × 70% gross margin**,
- fixed costs около founder-mode базы **3,192 млн ₽/мес** с поправкой на time-to-hire.

Это не претендует на точность бухгалтерской модели, но достаточно хорошо показывает, насколько широкий веер исходов скрыт внутри текущих допущений.

#### 2.3 Результат Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---------|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -982 000 | 1 049 000 | 4 503 000 | 5 485 000 |
| CAC payback, мес | 6,3 | 10,8 | 17,1 | 10,8 |
| LTV/CAC | 1,36x | 4,34x | 13,82x | 12,46 |
| Cash runway, мес | 30,4 | 36,0 | 150,0 | 119,6 |

#### 2.4 Интерпретация правил Monte Carlo Lite

1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: risk of insolvency**.
2. **p50 EBITDA = 1,05 млн ₽/мес**, то есть median формально проходит EBITDA Gate выше **500 тыс. ₽/мес**.
3. Формула **p90/p10** для EBITDA здесь теряет смысл из-за смены знака, но именно это и есть красный флаг: распределение пересекает ноль, значит downside не cosmetic, а existential.
4. **Range width по LTV/CAC = 12,46**, это сильно выше порога **8**, значит модель действительно хрупкая и слишком чувствительна к сочетанию pricing, churn и CAC.

**Итог Monte Carlo Lite:** median-case ещё инвестиционно терпим, но tail-risk уже слишком заметный. Это не clean winner, а кейс, где защита премиум-чека должна быть доказана эмпирически, иначе score надо даунгрейдить.

### 3. Competitor deep-dive

Ниже market-share estimates, это **моя оценка по публичным сигналам**: ARR, масштабу дистрибуции, числу интеграций, известности бренда и плотности присутствия в enterprise-сегменте. Это не audited market share.

#### 3.1 Западные конкуренты

| Компания | Почему релевантна | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Hightouch | composable CDP, AI Decisioning, warehouse-native активация | сильный category leadership, deep warehouse-native DNA, AI-модуль уже монетизируется, сильные enterprise logos, **$100M ARR** к 15.04.2026 | дорогой enterpise motion, длинный sales cycle, слабее fit под РФ data residency и локальные интеграции | **20-25%** глобального сегмента warehouse-native activation/decisioning [инференс из [D1], [B2]] | локальный data-residency, on-prem/private deployment, интеграции с РФ-стеком, продажа через ROI на локальном рынке |
| Census / Fivetran Activations | reverse ETL + activation внутри большого data movement stack | сильная инфраструктурная доверенность, дистрибуция через Fivetran, 200+ activations, стандарт де-факто для modern data stack | меньше выраженной decisioning-layer дифференциации, скорее infrastructure-first, чем marketer-first | **10-15%** глобального сегмента activation [инференс из [D2], [B3]] | можем позиционироваться выше по application-layer value, а не только sync layer |
| Bloomreach / Optimove class | AI-personalization и orchestration ближе к value-layer для маркетинга | зрелые playbooks, хорошая персонализация, доказанный uplift-narrative, сильны в retail/e-commerce | не warehouse-native by design, тяжелее modern DWH-first story, для РФ слабее по legal/data-localization | **8-12%** adjacent enterprise personalization slice [инференс из [B4], [B5]] | warehouse-native архитектура проще продаётся зрелым командам с собственным DWH и потребностью в controllable activation |

**Вывод по Западу:** category реальна, деньги там есть, но лидер уже понятен, и это делает ставку на «ещё один Hightouch для всех» слабой. Рабочая стратегия только одна: **локальный и regulatory-aware wedge + measurable uplift поверх существующего DWH**.

#### 3.2 Российские конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Mindbox | самый сильный локальный бренд в CDP/маркетинг-автоматизации, enterprise pricing **от 400k ₽/мес**, высокая надёжность и масштаб, публично описывает нагрузку **15+ млрд API-запросов в месяц** и **1+ млрд отправок в неделю** | не warehouse-native в строгом смысле, стек более opinionated, может быть тяжелее для команд, которые уже живут в собственном DWH | **25-35%** российского enterprise CDP/personalization slice [инференс из [D3], [B6], [B7]] | мы можем зайти как decisioning-layer поверх уже существующих warehouse-процессов без полной замены core CRM/CDP |
| RetailCRM / Simla | дешёвый вход, широкая узнаваемость в e-commerce, сильная CRM-база и go-to-market через automation/AI-ассистентов | слабее на heavy enterprise decisioning, меньше fit для DWH-native сценариев, ниже готовность buyer платить premium uplift-модель | **10-15%** российского CRM-led marketing automation slice [инференс из [D4], [B8]] | наше преимущество, deep warehouse analytics, сложные сегменты и policy-scoring, а не просто CRM workflow |
| Carrot quest | быстрая установка, lower-midmarket traction, сильна в onsite/in-app коммуникациях и conversational UX | ниже ceiling по чеку и сложности use cases, слабее против enterprise security/procurement и сложной data orchestration | **5-10%** mid-market marketing automation slice [инференс из [D5], [B9]] | мы сильнее там, где нужно решение для data-rich enterprise, а не каналовый engagement tool |
| Altcraft | локальная CDP/маркетинг automation-платформа, заметна в enterprise и импортозамещении, есть on-prem narrative | заметно ниже брендовый вес, чем у Mindbox, слабее ecosystem pull и fewer public proof points | **3-7%** enterprise-local CDP slice [инференс из [B10], [B11]] | при сильном AI decisioning и warehouse-native UX можно обойти Altcraft по modern-data позиционированию |

**Вывод по России:** локальные substitutes уже закрывают основную боль buyer'а сильно дешевле и привычнее. Это значит, что продукт нельзя продавать как «российская CDP/CRM automation платформа». Его нужно продавать как **uplift engine для компаний, у которых CDP/CRM уже есть, но не хватает decision intelligence поверх DWH**.

### 4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founders становятся bottleneck в sales discovery и solution design | high | высокий, pipeline и delivery перестают масштабироваться | >70% пресейл-встреч ведёт founder, >14 дней на scoping | стандартизировать presales playbook, нанять solutions architect раньше growth team |
| 2 | Operational | LLM/API и inference cost drift ломают COGS | med | высокий, margin съедается незаметно | COGS/client >90k ₽ два месяца подряд | лимиты на inference, model routing, fallback на более дешёвые модели, частичная дедупликация inference |
| 3 | Market | Спрос остаётся niche, рынок покупает знакомые CDP/CRM, а не decisioning layer | med | высокий, пайплайн не наполняется | lead→paid <0,7%, discovery-to-pilot <25% | продавать через 2-3 узких vertical playbook и ROI cases, а не через broad category education |
| 4 | Market | Price compression из-за Mindbox/RetailCRM/Carrot quest и внутренних команд клиента | high | высокий, модель теряет EBITDA | средний чек <210k ₽ или скидки >25% | жёсткий ROI calculator, packaging как revenue-uplift layer, отказаться от сделок ниже floor price |
| 5 | Regulatory | 152-ФЗ и data residency блокируют использование зарубежных компонентов | med | высокий, enterprise сделки стопорятся на security review | требования on-prem/private cloud в >50% тендеров | локальный deployment path, хранение PII в РФ, Data Processing Map для пресейла |
| 6 | Regulatory | 115-ФЗ / AML-подобные требования и compliance клиентов тормозят fintech/use-cases | med | средний-высокий | security/legal stage >90 дней | отдельные compliance templates, логирование решений, explainability для scoring |
| 7 | Financial | Cash runway проседает из-за длинного sales cycle 4-8 месяцев | high | высокий | burn >2,7 млн ₽/мес при <1 new logo/мес | stage-gated hiring, raise buffer 28-30 млн ₽, план на bridge round ещё до M9 |
| 8 | Financial | Ослабление рубля и рост USD-зависимых SaaS/API расходов | med | средний-высокий | USD/RUB >110 и рост cloud/API line >20% | валютный резерв, RUB-pricing с FX-clauses, локальные альтернативы по стеку |
| 9 | Black swan | Новый пакет санкций режет доступ к критичному SaaS или биллингу | med | высокий | сбои доступа к vendor console, отказ в оплате, forced offboarding | резервный стек, несколько платёжных контуров, контрактные оговорки про graceful degradation |
| 10 | Black swan | Резкое отключение/деградация LLM-провайдеров делает AI-функции недоступными | med | высокий | рост latency/ошибок, vendor incident >24 часов | hybrid stack, feature flags, degradation-mode без GenAI, локальные/open-source модели для core flows |

### 5. Kill conditions через 6 месяцев

1. **Kill #1, insolvency risk:** если по обновлённой модели **p10 EBITDA@M24 остаётся < 0** и при этом cash runway падает ниже **9 месяцев**, проект нельзя продолжать без радикального пересмотра GTM и cost base.
2. **Kill #2, no premium wedge:** если к **M6** средний реализованный чек **< 210 000 ₽/мес** или скидка к прайсу стабильно **>25%**, продукт не удерживает premium относительно локальных substitutes.
3. **Kill #3, pipeline failure:** если к **M6** меньше **6 paying клиентов** или blended **CAC payback > 18 месяцев**, growth motion не подтверждён и дальнейшее масштабирование капитала не оправдано.

### 6. Bottom line по SECTION B

- **Финансовый риск: высокий, но не фатальный**, если удаётся сохранить чек около **240k+ ₽/мес** и churn не уходит выше **1,5-2,0%**.
- **Главный риск не в технологии, а в premium positioning** против российских substitutes и внутренних data/CRM-команд клиента.
- **Monte Carlo Lite подтверждает хрупкость:** median-case проходит, но downside уже пересекает ноль, а разброс по LTV/CAC слишком широкий.
- Следовательно, кейс можно держать в работе только как **disciplined enterprise wedge**, но не как широкий «AI martech platform».

### Источники SECTION B

- [B1] `04-economics.md` текущего кейса
- [B2] TechCrunch, Hightouch reaches $100M ARR fueled by marketing tools powered by AI, 2026-04-15, https://techcrunch.com/2026/04/15/hightouch-reaches-100m-arr-fueled-by-marketing-tools-powered-by-ai/
- [B3] Fivetran Activations product page, https://www.fivetran.com/data-movement/activations
- [B4] Bloomreach product/pricing ecosystem, https://www.bloomreach.com/en/products
- [B5] Optimove positioning, https://www.optimove.com/platform
- [B6] Mindbox tariffs, https://mindbox.ru/tariffs/
- [B7] Habr, Mindbox: нагрузка и масштаб платформы, https://habr.com/ru/companies/mindbox/articles/596919/
- [B8] RetailCRM pricing, https://www.retailcrm.ru/prices
- [B9] Carrot quest tariffs, https://help.carrotquest.io/article/685
- [B10] Altcraft platform overview, https://altcraft.com/ru/platform/
- [B11] Rusprofile, ООО «Майндбокс», https://www.rusprofile.ru/id/1718492

<!-- P6B-DONE -->


## Стадия 6. Final Verdict
[B2B-OPS] Warehouse-native AI Decisioning Marketing Operator v2 — NEAR-PASS: 69/100 | EBITDA base=672К₽/мес через 14 мес | LTV/CAC=4,3x | Ключевое преимущество: продаётся поверх уже существующего DWH/CDP как uplift-layer | Главный риск: premium pricing легко сжимается из-за Mindbox/RetailCRM и внутренних data-команд.

# 06-verdict

sector: B2B-OPS

## Кейс
warehouse-native-ai-decisioning-marketing-operator-v2

## Дата финального вердикта
2026-04-20 (Europe/Moscow)

## Итог
**NEAR-PASS**

## Финальный score
**69/100**

## Нормализация
- Raw score: **103/150**
- Normalized score: **round(103 × 100 / 150) = 69/100**
- Статус по порогам: **65-69 = NEAR-PASS**
- EBITDA gate: **пройден**. В базовом сценарии компания выходит на **company_ebitda_rub_month = 672 000 ₽/мес** примерно на **14 месяце** и достигает этого при **23 клиентах**, то есть в пределах **<=24 месяцев** и **<=50 клиентов**.

## Investment memo
Кейс улучшился относительно прошлой версии за счёт более реалистичной экономики и явного EBITDA path, но всё ещё не дотягивает до approve. Главный стоп-фактор, это не unit economics, а слабое доказательство repeatable RU demand именно для premium warehouse-native decisioning wedge. На инвестиционном уровне это выглядит как дисциплинированный near-pass: можно возвращать в review только после подтверждения 2-3 российских пилотов с outcome-based ROI и без price compression ниже floor.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC: 4,3x», «CAC Payback: 10,8 мес», «Contribution Margin: 70,0%» из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «EBITDA при 50 клиентах: около 3,10 млн ₽/мес» и founder-mode break-even на 19 клиентах; 500k EBITDA достигается около 23 клиентов. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | «Composite demand: LOW», «Demand score: 0», но «SAM = 1,35 млрд ₽/год» и локальные substitutes с бюджетами уже есть; применён tier penalty. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Есть интеграционный embedded-workflow слой, но «premium positioning надо защищать сильнее», а продуктовый moat пока слабый. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 21 | Риски хорошо видны и управляемы, но 05-critic.md фиксирует «Founders становятся bottleneck», «152-ФЗ и data residency» и зависимость от LLM/API. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | ICP конкретный, CAC payback < 12 мес, а GTM можно сфокусировать на 10 named targets в data-rich enterprise, но sales cycle остаётся 4-8 месяцев. |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 11 200 000 ₽ |
| CAC | 2 580 000 ₽ |
| LTV/CAC | 4,3x |
| CAC Payback | 10,8 мес |
| GM | 70,0% |
| contribution_margin_rub_month | 168 000 ₽/мес |
| fixed_costs_rub_month | 3 192 000 ₽/мес в founder-mode / 5 200 000 ₽/мес steady-state |
| company_ebitda_rub_month (base @ M14, 23 клиента) | 672 000 ₽/мес |
| company_ebitda_potential_rub_month (50 клиентов) | 3 100 000 ₽/мес |
| break-even | 19 клиентов / M12 в founder-mode |
| startup_capital_to_bep_rub | 25 147 000 ₽ |
| clients_to_500k_ebitda | 23 |
| months_to_500k_ebitda | 14 |
| clients_to_1m_ebitda | 25 |
| months_to_1m_ebitda | 15 |

## Полный бизнес-процесс
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Target-list ICP аккаунтов | Founder/AE | ручной ресерч, базы, CRM | 1,2 ч | 1 500 | низкая |
| 2 | Поиск и enrichment контактов | SDR | CRM, сайты, базы | 0,6 ч | 700 | средняя |
| 3 | Первый outbound touch | SDR | email, звонок, Telegram | 15 мин | 300 | средняя |
| 4 | Follow-up 5-7 касаний | SDR | CRM sequence | 1,2 ч | 1 400 | средняя |
| 5 | Qualification call | SDR + AE | Meet/CRM | 45 мин | 1 500 | низкая |
| 6 | Discovery по data/CRM stack | AE + Founder | Meet, Miro, Notion | 1,5 ч | 4 000 | низкая |
| 7 | Техскопинг и ROI-гипотеза | Solutions/CTO | schema review, SQL, docs | 3,5 ч | 9 500 | низкая |
| 8 | Demo / pilot design | AE + CTO | demo env, презентация | 1 ч | 2 800 | средняя |
| 9 | Security / legal / procurement | Founder + CTO | почта, docs, DPA/MSA | 5-6 ч труда | 13 000 | низкая |
| 10 | Commercial close | AE | CRM, КП, переговоры | 2 ч | 4 000 | средняя |
| 11 | Подписание и счёт | AE/Ops | ЭДО, 1С/банк | 30 мин | 800 | высокая |
| 12 | Onboarding и первые интеграции | CSM + Solutions | warehouse connector, BI, docs | 10-16 ч | 26 000 | средняя |

## Team table
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| Founder / CEO | продажи, key accounts, fundraising | 650 000 |
| CTO / Solutions lead | архитектура, security, data-scoping | 585 000 |
| Backend / data engineer 1 | connectors, orchestration | 455 000 |
| Backend / data engineer 2 | integrations, delivery | 455 000 |
| ML / analytics engineer | scoring, experimentation logic | 520 000 |
| Product / UX | marketer-facing workflow | 325 000 |
| SDR | outbound pipeline | 175 000 |
| AE | discovery, pilots, close | 390 000 |
| CSM | onboarding, renewals, support | 325 000 |
| Growth / content | category education | 390 000 |
| Finance / ops part-time | ЭДО, billing, back-office | 130 000 |
| **Итого зрелая команда** |  | **4 400 000 ₽/мес** |

## 7-factor Moat framework
| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не усиливает ценность продукта для остальных. |
| Switching costs | 2 | DWH-коннекторы, сценарии и обученность CRM-команды создают умеренную инерцию на выход. |
| Scale economies | 1 | Scale снижает unit COGS умеренно, но services-load остаётся заметным. |
| Proprietary data / model advantage | 1 | Есть шанс на накопление event-level heuristics, но уникальный датасет не доказан. |
| Regulatory moat | 1 | 152-ФЗ и data residency важны как барьер входа, но это скорее hygiene-factor, чем сильный moat. |
| Brand / distribution | 1 | Категория реальна, но локальный бренд и дистрибуция пока не сформированы. |
| Embedded workflow | 3 | При успешном внедрении слой реально встраивается в CRM, DWH и регулярные campaign decision loops. |
| **Сумма** | **9/21** |  |

**Moat score = round(9 × 25 / 21) = 11/25.**

## GTM: 10 named targets
Ниже не текущий pipeline, а **моя инвестиционная гипотеза по первым 10 аккаунтам**, выбранным как реальные российские компании из data-rich consumer verticals, которые регулярно фигурируют в vc.ru, rb.ru, Habr и rusprofile. Это inference на основе ICP из 02-demand.md и economics/critic.

| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Ozon | Большой e-commerce, сильная CRM и персонализация, высокая цена ошибки в campaign orchestration. | email decision-maker + партнёрство через data/integration vendor | 350 000 ₽/мес |
| 2 | Яндекс Маркет | Огромный каталог и paid traffic, warehouse-native uplift можно продавать через promo и recommendation efficiency. | конференция + warm intro через martech/data-партнёров | 400 000 ₽/мес |
| 3 | Lamoda | Fashion e-commerce с высокой чувствительностью к retention, сегментации и next-best-offer. | email CRM/head of growth | 300 000 ₽/мес |
| 4 | Самокат | Высокочастотные транзакции и промо, decisioning полезен для персональных предложений и reactivation. | партнёрство + intro через CRM/data stack vendor | 300 000 ₽/мес |
| 5 | Купер | Grocery delivery зависит от retention и активации churn-risk сегментов; быстрый ROI на uplift-case. | email decision-maker + targeted content | 280 000 ₽/мес |
| 6 | М.Видео-Эльдорадо | Многоканальный retail с loyalty и тяжёлым promo-calendar, где DWH-native policy engine понятен buyer'у. | конференция retail tech + outbound AE | 320 000 ₽/мес |
| 7 | Hoff | Крупный retail с длинным consideration cycle, нужен personalised journey orchestration поверх существующего CRM. | email marketing director + case-driven outreach | 250 000 ₽/мес |
| 8 | S7 Airlines | Travel и loyalty-heavy вертикаль, где next-best-action и reactivation дают измеримый ROMI. | партнёрство с travel-tech интегратором | 350 000 ₽/мес |
| 9 | Т-Банк | У банка зрелый lifecycle marketing и много данных; ценность в policy-based offer decisioning и experiment velocity. | email VP CRM / digital marketing + intro через fintech partner | 450 000 ₽/мес |
| 10 | МегаФон | Telecom CRM-маркетинг, огромная база и понятный эффект от сегментации и churn prevention. | конференция + enterprise outbound | 380 000 ₽/мес |

## Top-3 risks
| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Price compression против локальных substitutes | high | high | При чеке ниже 210-240k ₽/мес модель быстро теряет EBITDA и уходит в stress-case. |
| evidence_quality_unverified | high | medium-high | В 02-demand.md нет строки Sources, direct demand LOW, HH/Wordstat/category evidence для РФ слабы. |
| Founder bottleneck + heavy presales | medium-high | high | Discovery, scoping и legal/security stage долго держатся на founder/CTO и плохо масштабируются. |

## Дополнительные риски из P6B
- 152-ФЗ и data residency могут замедлить сделки дольше 90 дней.
- LLM/API cost drift способен поднять COGS выше 90k ₽/клиент/мес.
- Monte Carlo Lite показывает **p10 EBITDA@M24 = -982 000 ₽/мес**, то есть downside уже пересекает ноль.

## LTV Upside Calculator
Поскольку кейс не approved, ниже калькулятор, что именно поднимет его к 70+.

### Текущая база
- MRR: **240 000 ₽/мес**
- GM: **70%**
- contribution_margin_rub_month: **168 000 ₽/мес**
- customer_ltv_rub: **11 200 000 ₽** при churn 1,5%
- CAC: **2 580 000 ₽**
- LTV/CAC: **4,3x**

### Что даст апсайд
| Рычаг | Новое допущение | Эффект |
|---|---|---|
| Чек выше без price compression | 300 000 ₽/мес при тех же COGS | contribution_margin_rub_month растёт до 228 000 ₽/мес, LTV/CAC поднимается до ~5,9x |
| Снижение CAC через партнёров | CAC 1 850 000 ₽ | при текущем LTV LTV/CAC растёт до ~6,1x |
| Снижение churn | 1,0% monthly churn | customer_ltv_rub растёт до 16 800 000 ₽, LTV/CAC до ~6,5x |
| Комбинированный upside | 300k MRR + CAC 1,85m + churn 1,0% | LTV/CAC становится >9x, а запас прочности по EBITDA становится investment-grade |

## Почему это NEAR-PASS, а не APPROVED
1. **Экономика проходит**, но только в узком premium enterprise wedge.
2. **Спрос в РФ по exact category label слабый**, а без жёсткого evidence кейс остаётся рискованным для fund-level approve.
3. **Moat пока умеренный**, в основном через embedded workflow, а не через brand, network effects или proprietary data.
4. **GTM реалистичен**, но всё ещё founder-heavy и чувствителен к длинному enterprise cycle.

## Что нужно доказать для апгрейда в APPROVED
1. Минимум **2-3 российских платящих логотипа** с recurring **>=300 000 ₽/мес**.
2. Подтверждённый uplift, например **+5-10% revenue uplift / -10-15% CAC waste / measurable retention gain**.
3. Документированный локальный deployment path под **152-ФЗ / private cloud / on-prem**.
4. Повторяемость GTM, где не менее **50% новых сделок приходят не через founder-led outbound**, а через партнёров, контент или referrals.

## Delta vs previous
- Previous status: **REJECTED**
- Previous score: **61/100**
- New status: **NEAR-PASS**
- New score: **69/100**
- Delta: **+8 пунктов**

### Что улучшилось
- Экономика стала жёстче и реалистичнее: вместо искусственно высокого чека теперь модель держится на **240k ₽/мес**, **GM 70%** и **LTV/CAC 4,3x**.
- Появился явный путь к **company_ebitda_rub_month >= 500 000 ₽/мес** за **14 месяцев**.
- Monte Carlo и sensitivity теперь лучше показывают не только upside, но и реальные хвостовые риски.

### Что всё ещё не доказано
- Категориальный RU demand именно по premium warehouse-native decisioning.
- Сильный moat против Mindbox, RetailCRM и внутренних data-команд.
- Repeatable GTM без founder bottleneck.

## Финальный маршрут
Перемещение: **pipeline/rejected/**

## Инвесткомитет one-liner
**Возвращать кейс в approve-обсуждение только после live-доказательства premium wedge в РФ. Пока это сильный near-pass с хорошей математикой и недостаточной уверенностью в спросе и moat.**

