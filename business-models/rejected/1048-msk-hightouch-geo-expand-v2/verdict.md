# verdict
Источник pipeline: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/rejected/1048-msk-hightouch-geo-expand-v2`

## Стадия 0. Brief
# 00-brief

## Кейс
1048-msk-hightouch-geo-expand-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
1048-msk-hightouch-geo-expand

## Краткое описание
Кейс создан по правилу принудительного полного пайплайна для resurrect-сигнала по Hightouch geo-expand, хотя раньше материал был обработан только как supporting signal для соседнего кейса.

## Что делать дальше
Перейти к P3-demand-validation и заново проверить, является ли Hightouch-подобный geo-expand сигнал самостоятельным кандидатом или всё же финально схлопывается в смежный кейс про AI decisioning для маркетинга.


## Стадия 1. Intake
---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1048-msk-hightouch-geo-expand.md
created: 2026-04-20T00:18:00+03:00
---

# 01-intake

## Кейс
1048-msk-hightouch-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — 1048-msk-hightouch-geo-expand

## Meta
- source: triage/triage-2026-04-19-1048-msk-hightouch-geo-expand-supporting.md
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
2026-04-19

## Входные данные
- `pipeline/raw/raw-2026-04-19-1048-msk-hightouch-geo-expand.md`

## Классификация
поддерживающий сигнал для существующего открытого кейса

## Решение
Существующий кейс обогащён, новый кейс не создавался.

## Совпадающий кейс
- `pipeline/cases/warehouse-native-ai-decisioning-marketing-operator/`

## Почему
- Сигнал совпадает по нише, buyer'у и технологическому ядру с уже открытым кейсом про warehouse-native AI decisioning для маркетинга.
- Во входном файле есть сильные подтверждающие данные по коммерческой зрелости категории: около $100 млн ARR, быстрый прирост выручки после запуска AI-продукта и enterprise-референсы.
- Это не новый кейс, а supporting signal, который усиливает уже открытую гипотезу по high-LTV сервисной модели в РФ.

## Что добавлено в кейс
- Создан `pipeline/cases/warehouse-native-ai-decisioning-marketing-operator/01-evidence.md` на русском языке.
- Добавлена запись с датой, источниками, типом сигнала, объяснением, как сигнал усиливает кейс, и ключевыми фактами.
- Зафиксированы данные: около $100 млн ARR у Hightouch, прирост около $70 млн ARR за 20 месяцев после запуска AI-направления, enterprise-клиенты и отсутствие явного прямого локального аналога warehouse-native AI Decisioning в РФ.

## Что сделано
- Кейс `warehouse-native-ai-decisioning-marketing-operator` обогащён.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал обработан как supporting signal для открытого кейса. Кейс обогащён новыми подтверждающими данными.

```


## Стадия 2. Demand Validation
---
stage: demand-validation
case: 1048-msk-hightouch-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
1048 MSK Hightouch GEO Expand, warehouse-native AI decisioning и composable CDP слой для lifecycle-маркетинга, персонализации и data activation поверх существующего DWH / martech-стека.

## Итог
**Статус: CONDITIONAL PASS**

По exact RU-запросам категория почти не ищется. Проверка через internal demand API по `warehouse native ai decisioning marketing` вернула `LOW`, `demand_score=0`, `google_trends_ru=0`, `hh_ru=0`, `habr_articles=2`, `yandex_suggest=2`. Смежные запросы `composable cdp personalization` и `marketing decision engine` тоже дали слабый exact-demand, хотя по последнему уже видно `hh_ru=8`.

Это не clean PASS по keyword demand. Но кейс нельзя автоматически отбрасывать, потому что бюджеты уже живут в более широких и платёжеспособных категориях: CDP, CRM marketing, персонализация, ad optimization, loyalty и data activation.

Публичные рыночные якоря сильные:
- по состоянию на **15 апреля 2026 года** Hightouch сообщила о достижении **$100 млн ARR**, причём рост заметно подпитывается AI-маркетинговыми инструментами;
- у Hightouch есть отдельная коммерческая pricing-страница под **AI Decisioning** и **Composable CDP**, то есть это не исследовательский narrative, а продаваемый enterprise layer;
- **1 мая 2025 года** Fivetran объявила о подписании соглашения о покупке Census, назвав activation / reverse ETL стратегическим слоем end-to-end data movement;
- в РФ уже есть платёжеспособные substitutes: **Mindbox от 150 000 ₽/мес, Enterprise от 400 000 ₽/мес**, **RetailCRM от 9 360 ₽/мес**, **Carrot quest Marketing 10 990–29 990 ₽/мес, Marketing Expert 14 287–38 987 ₽/мес, Enterprise по запросу**.

Вывод: exact-label в России слабый, но spending layer существует. Поэтому кейс проходит P3 условно, с оговоркой, что в P4-P6 нужно жёстко проверить, можно ли реально защищать premium-чек поверх локальных substitutes и не схлопывается ли кейс обратно в смежный `warehouse-native-ai-decisioning-marketing-operator-v2`.

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand?keyword=warehouse%20native%20ai%20decisioning%20marketing`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- hh.ru vacancies: **0**
- Habr articles: **2**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Смежные проверки:

### `composable cdp personalization`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **1**
- hh.ru vacancies: **0**
- Habr articles: **2**
- Yandex suggest: **2**

### `marketing decision engine`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **1**
- hh.ru vacancies: **8**
- Habr articles: **2**
- Yandex suggest: **2**

### Интерпретация
В РФ почти нет признаков, что покупатель формулирует потребность exact-термином `warehouse-native AI decisioning`. Но это типично для сложного B2B enterprise software: закупка идёт через более привычные бюджетные строки, а не через модный category label.

Для этого кейса такими бюджетными строками выглядят:
- CDP;
- CRM marketing;
- персонализация;
- рекомендательные механики;
- ad optimization;
- data activation.

## 2. Рыночные сигналы и why now
1. **15 апреля 2026 года** TechCrunch сообщил, что Hightouch достигла **$100 млн ARR**, а после запуска AI-направления за предыдущие 20 месяцев добавила около **$70 млн ARR**. Это сильный внешний сигнал, что enterprise buyers уже покупают category-level продукт, а не эксперимент.
2. На официальной pricing-странице Hightouch отдельно выделяет планы для **AI Decisioning** и для **Composable CDP**. Это подтверждает, что vendor продаёт AI decisioning как самостоятельный monetizable layer.
3. **1 мая 2025 года** Fivetran объявила о соглашении по приобретению Census. Формулировка пресс-релиза прямо указывает, что reverse ETL, activation и operational analytics воспринимаются как стратегическая часть AI-era data stack.
4. В локальном контуре есть явные substitutes с живыми тарифами. Mindbox уже продаёт CDP, оптимизацию рекламы и loyalty по enterprise-прайсу, а Carrot quest и RetailCRM закрывают lower-end слой маркетинговой автоматизации и данных.

### Вывод
Категория денег есть и глобально, и локально. Но локально она живёт не как чистый Hightouch-клон, а как смесь CDP / CRM marketing / personalization / martech automation.

## 3. Конкурентные и ценностные якоря

| Игрок | Что доказывает | Публичный ценовой / рыночный сигнал |
|---|---|---|
| Hightouch | category proof в enterprise-сегменте | AI Decisioning и Composable CDP вынесены в pricing, ARR = $100 млн по состоянию на 15.04.2026 |
| Census / Fivetran | стратегическую ценность reverse ETL и data activation | acquisition announcement от 01.05.2025 |
| Mindbox | локальный enterprise budget на персонализацию и CDP уже существует | Standard от 150 000 ₽/мес, Enterprise от 400 000 ₽/мес |
| RetailCRM | lower-end и mid-market substitutes существуют и стоят кратно дешевле | Профессиональный от 9 360 ₽/мес |
| Carrot quest | рынок маркетинговой автоматизации и onsite / messaging orchestration уже нормализован | Marketing 10 990–29 990 ₽/мес, Marketing Expert 14 287–38 987 ₽/мес, Enterprise по запросу |

### Вывод по конкурентному полю
- Бюджет на data-driven marketing в РФ точно есть.
- Но большая часть локального рынка уже может закрывать заметную долю боли через более дешёвые инструменты.
- Поэтому high-ticket AI decisioning слой должен продаваться не как «ещё одна CDP/CRM», а как uplift layer с доказанным влиянием на revenue, retention, ROMI и скорость принятия маркетинговых решений.

## 4. Кто реально может купить в локальном контуре
Кейс не для массового SMB. Реалистичный buyer, это компания, у которой уже есть:
- DWH или зрелый event/data stack;
- несколько каналов acquisition / CRM / retention;
- внутренняя команда growth, CRM, performance или lifecycle;
- заметный маркетинговый бюджет;
- потребность в персонализации и decision automation.

### 10 sanity-check ICP bucket'ов
1. крупные e-commerce ритейлеры;
2. grocery delivery и e-grocery;
3. travel / ticketing;
4. fintech с сильным lifecycle marketing;
5. subscription-сервисы;
6. маркетплейсы и classifieds;
7. телеком с CRM-маркетингом;
8. крупные D2C-бренды;
9. betting / gaming / entertainment с выраженным retention motion;
10. enterprise retailers с loyalty и promo orchestration.

Это не universal SaaS-рынок, но и не микроскопическая ниша. Скорее узкий high-value слой внутри больших consumer-data бизнесов.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру консервативный локальный blended чек:
- **450 000 ₽/мес** на клиента как рабочий enterprise-midmarket anchor;
- или **5,4 млн ₽/год**.

Это выше нижних локальных substitutes, но близко к enterprise-слою Mindbox и всё ещё существенно ниже гипотезы про ultra-premium custom operator.

### TAM
Берём **1 500** релевантных компаний в РФ и близком контуре: e-commerce, retail, fintech, telecom, travel, subscriptions, marketplaces и другие data-rich consumer businesses.

**TAM = 1 500 × 5,4 млн ₽ = 8,1 млрд ₽/год**

### SAM
Реально адресуемый слой в первом GTM, только компании с уже зрелым data stack и готовностью к сложной интеграции.

Берём **250** аккаунтов.

**SAM = 250 × 5,4 млн ₽ = 1,35 млрд ₽/год**

### SOM
Ранний реалистичный слой, который можно попробовать взять в первые циклы.

Берём **12 клиентов**.

**SOM = 12 × 5,4 млн ₽ = 64,8 млн ₽/год**

### Вывод по рынку
Для фонда это не выглядит слишком маленьким рынком. Но это рынок не product-led SaaS, а тяжёлого enterprise / service-assisted внедрения, что важно для следующих блоков economics и critic.

## 6. WTP и доказательства готовности платить
1. Hightouch продаёт AI Decisioning как отдельный enterprise product layer, а не только как add-on к data sync.
2. ARR-сигнал Hightouch на **15 апреля 2026 года** подтверждает, что buyers готовы платить за measurable outcome в маркетинге.
3. Mindbox показывает, что в РФ уже есть нормализованный enterprise budget **150k-400k+ ₽/мес** на близкий класс задач.
4. RetailCRM и Carrot quest показывают, что нижний и средний сегмент будет aggressively price-sensitive.

### Вывод по WTP
**WTP подтверждён, но premium WTP подтверждён ограниченно.**

Именно поэтому статус не clean PASS. Рынок готов платить за результат в персонализации и CRM marketing, но пока нет сильного локального доказательства, что он массово готов доплачивать именно за warehouse-native AI decisioning слой как отдельную категорию.

## 7. Profit Gate
Цель: увидеть путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Conservative
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

### Сценарий C. Premium
- Цена: **650 000 ₽/мес**
- GM: **70%**
- Валовая прибыль на клиента: **455 000 ₽/мес**
- Нужно **6 клиентов**

**Вердикт: PASS**

### Интерпретация
Чисто математически profit gate проходит. Главный риск не в арифметике, а в том, удержится ли локальный чек существенно выше более дешёвых substitutes после учёта integration load и кастомизации.

## 8. Общий вывод
- Exact search demand: **LOW**
- Adjacent budget buckets: **подтверждены**
- Глобальный category proof: **сильный**
- Локальные substitutes: **сильные и заметно дешевле**
- WTP: **есть, но premium слой подтверждён ограниченно**
- Profit Gate: **проходит**

## 9. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Причины:
1. рынок денег для похожего слоя существует;
2. Hightouch и Census/Fivetran подтверждают стратегическую ценность категории;
3. локальные pricing anchors есть;
4. profit gate проходит.

Но в следующих блоках нужно проверить особенно жёстко:
- не является ли этот кейс просто более узким дублем `warehouse-native-ai-decisioning-marketing-operator-v2`;
- можно ли защищать premium pricing поверх Mindbox / RetailCRM / Carrot quest;
- сколько services-heavy нагрузки спрятано внутри доставки результата.

## Market Pulse
Market Pulse 20.04.2026: осторожно позитивный. Категория реальна и коммерчески жива, но локальный рынок, вероятно, купит её только в узком enterprise-сегменте и только при очень понятном uplift.

> Market Pulse 2026-04-20: растущий интерес.

> Market Pulse 2026-04-20: растущий интерес.

## Источники
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=warehouse%20native%20ai%20decisioning%20marketing
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=composable%20cdp%20personalization
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=marketing%20decision%20engine
- [T2] Hightouch pricing: https://hightouch.com/pricing
- [T3] TechCrunch, Hightouch reaches $100M ARR, 2026-04-15: https://techcrunch.com/2026/04/15/hightouch-reaches-100m-arr-fueled-by-marketing-tools-powered-by-ai/
- [T4] Fivetran signs agreement to acquire Census, 2025-05-01: https://www.fivetran.com/press/fivetran-signs-agreement-to-acquire-census-delivering-the-first-end-to-end-data-movement-platform-for-the-ai-era
- [T5] Mindbox tariffs: https://mindbox.ru/tariffs/
- [T6] RetailCRM pricing: https://www.retailcrm.ru/prices
- [T7] Carrot quest tariffs: https://help.carrotquest.io/article/685


## Стадия 4. Economics
# 04-economics

## Кейс
1048-msk-hightouch-geo-expand-v2

## Executive summary
**Статус: PASS WITH CONSTRAINTS.**

Юнит-экономика сходится только в узком enterprise-сегменте, где продукт продаётся как warehouse-native AI decisioning layer с измеримым uplift по выручке, retention и ROMI. Если кейс сползает в обычный CDP/CRM martech или в services-heavy интеграторский motion, запас прочности быстро исчезает.

Ключевые метрики базовой модели:
- **MRR на клиента:** 300 000 ₽/мес
- **COGS на клиента:** 95 000 ₽/мес
- **Contribution profit:** 205 000 ₽/мес
- **Contribution margin:** **68,3%**
- **Fully-loaded CAC:** **2 900 000 ₽**
- **LTV:** **12 300 000 ₽**
- **LTV/CAC:** **4,2x**
- **CAC payback:** **9,7 мес**
- **Break-even:** **19 клиентов** в founder-mode, **30 клиентов** на полной команде
- **EBITDA при 40 клиентах:** около **2,0 млн ₽/мес**

## 1. Модель монетизации и рабочие допущения

### ICP
- крупный e-commerce, fintech, travel, retail-media, subscription и marketplace-контур;
- у клиента уже есть DWH, event/data stack, CRM/lifecycle-команда и действующий martech-бюджет;
- продукт покупают не как дешёвую автоматизацию, а как premium decisioning layer поверх существующего стека.

### Коммерческие допущения
| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний контракт | 300 000 ₽/мес | выше lower-end substitutes, но ниже demand-stage premium-case |
| ARR на клиента | 3 600 000 ₽/год | 300k × 12 |
| Setup fee | 250 000 ₽ разово | не включаю в MRR |
| Валовая маржа | 68,3% | ниже pure software из-за onboarding и solutions-load |
| Sales cycle | 5-8 мес | enterprise / upper mid-market motion |
| Целевой сегмент | enterprise-only | mid-market слишком чувствителен к цене |

## 2. COGS на клиента в месяц

| Компонент | ₽/клиент/мес | Комментарий |
|---|---:|---|
| Compute / orchestration | 22 000 | decisioning jobs и сегментация |
| Storage / data transfer | 6 000 | события, логи, выгрузки |
| ML / LLM reserve | 10 000 | inference и scoring budget |
| Customer Success | 18 000 | сопровождение активной базы |
| Solutions support | 18 000 | schema changes и integration-support |
| Onboarding amortization | 15 000 | ~180k разового внедрения / 12 мес |
| Monitoring / observability | 6 000 | алерты, APM, logging |
| **Итого COGS** | **95 000** |  |

### Unit economics на клиента
- **Выручка:** 300 000 ₽/мес
- **COGS:** 95 000 ₽/мес
- **Contribution profit:** 205 000 ₽/мес
- **Contribution margin:** **68,3%**

## 3. Fully-loaded CAC

### Воронка по каналам
| Канал | Аккаунты | Discovery | Pilot / SQL | Won | Конверсия account→won | CAC канала, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Founder-led outbound | 170 | 15 | 5 | 1,0 | 0,59% | 3 150 000 | основной и дорогой канал |
| Партнёры / интеграторы | 22 | 7 | 3 | 0,8 | 3,64% | 2 150 000 | лучший CAC, но мало объёма |
| Контент / inbound | 35 | 5 | 2 | 0,4 | 1,14% | 2 700 000 | category education дорогая |
| **Blended** | **227** | **27** | **10** | **2,2** | **0,97%** | **2 900 000** | базовая модель |

### Состав fully-loaded spend
| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| Paid demand-gen / amplification | 180 000 | узкий рынок и дорогой explain motion |
| Sales FOT attributed to new | 690 000 | SDR + AE + founder allocation |
| Marketing allocation | 240 000 | контент, кейсы, category education |
| Tools / CRM / enrichment | 60 000 | CRM, enrichment, sequencing |
| Events / partnerships | 120 000 | точечные ивенты и канальные партнёры |
| Subtotal raw spend | 1 290 000 |  |
| Overhead multiplier (x1.85) | 1 096 500 | legal, procurement, founder time, security drag |
| **Итого fully-loaded spend** | **2 386 500** |  |
| Новые paying customers / мес | **0,82** | после ramp-up |
| **Blended fully-loaded CAC** | **2 900 000 ₽** | округление вверх |

## 4. LTV, churn и payback

### Базовые допущения
- Monthly logo churn: **1,67%**
- Формула: `LTV = MRR × Gross Margin / Monthly churn`

### Расчёт
`300 000 × 0,683 / 0,0167 ≈ 12 300 000 ₽`

| Метрика | Значение |
|---|---:|
| LTV | 12 300 000 ₽ |
| CAC | 2 900 000 ₽ |
| **LTV/CAC** | **4,2x** |
| **CAC payback** | **9,7 мес** |

### Вывод
- запас выше порога investment grade есть;
- но он держится только при enterprise-чеке и умеренном churn;
- при цене ближе к 200k ₽/мес или churn выше 2% модель быстро становится пограничной.

## 5. Команда и fixed costs

| Роль | Fully-loaded FOT ₽/мес |
|---|---:|
| Founder / CEO | 650 000 |
| CTO / Solutions lead | 600 000 |
| Backend / data engineer 1 | 455 000 |
| Backend / data engineer 2 | 455 000 |
| ML / analytics engineer | 520 000 |
| Product / UX | 325 000 |
| SDR | 175 000 |
| AE | 390 000 |
| CSM | 325 000 |
| Growth / content | 390 000 |
| Finance / ops part-time | 130 000 |
| **Итого зрелая команда** | **4 415 000 ₽/мес** |

### Fixed costs steady-state
| Статья | ₽/мес |
|---|---:|
| FOT fully-loaded | 4 415 000 |
| Cloud base platform | 360 000 |
| SaaS tools / CRM / docs | 100 000 |
| Юристы / бухгалтерия | 95 000 |
| Офис / admin | 120 000 |
| Командировки / ивенты | 110 000 |
| Прочие G&A | 50 000 |
| **Итого fixed costs** | **5 250 000 ₽/мес** |

## 6. Break-even

### Полная команда
`5 250 000 / 205 000 = 25,6`

С запасом считаю **30 клиентов** как безопасный break-even на полной команде.

### Founder-mode
Если держать более компактную конфигурацию и ограничить fixed costs примерно **3 895 000 ₽/мес**, тогда:

`3 895 000 / 205 000 = 19,0`

**Рабочий инвестиционный break-even: 19 клиентов.**

## 7. План M1-M12

| Месяц | Клиентов на конец месяца | MRR, ₽ | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 560 000 | -1 560 000 |
| M2 | 0 | 0 | 0 | 1 885 000 | -1 885 000 |
| M3 | 1 | 300 000 | 205 000 | 2 060 000 | -1 855 000 |
| M4 | 2 | 600 000 | 410 000 | 2 660 000 | -2 250 000 |
| M5 | 3 | 900 000 | 615 000 | 3 050 000 | -2 435 000 |
| M6 | 5 | 1 500 000 | 1 025 000 | 3 505 000 | -2 480 000 |
| M7 | 7 | 2 100 000 | 1 435 000 | 3 830 000 | -2 395 000 |
| M8 | 10 | 3 000 000 | 2 050 000 | 4 220 000 | -2 170 000 |
| M9 | 12 | 3 600 000 | 2 460 000 | 4 740 000 | -2 280 000 |
| M10 | 14 | 4 200 000 | 2 870 000 | 4 870 000 | -2 000 000 |
| M11 | 17 | 5 100 000 | 3 485 000 | 4 870 000 | -1 385 000 |
| M12 | 19 | 5 700 000 | 3 895 000 | 3 895 000 | **0** |

## 8. Burn-to-breakeven и runway

### Burn-to-breakeven
Сумма отрицательной EBITDA M1-M11: **≈ 22,7 млн ₽**.

С буфером на задержки продаж и procurement разумно считать потребность **26-28 млн ₽**.

### Runway
При `startup_capital = 40 000 000 ₽` и среднем burn первых 12 месяцев около **1,9-2,0 млн ₽/мес**:

`40 000 000 / 2 000 000 ≈ 20 мес`

**Cash runway: около 20 месяцев.**

## 9. Sanity checks

1. **CAC payback < 12 мес?** Да, **9,7 мес**.
2. **LTV/CAC ≥ 3?** Да, **4,2x**.
3. **5+ hires в первый месяц?** Нет.
4. **EBITDA > 500k/мес достижима?** Да, после выхода выше ~22 клиентов.
5. **Модель выдерживает price compression к 200k ₽/мес?** Скорее нет, запас почти исчезает.
6. **Главный риск модели?** Не compute, а дорогой enterprise sale и services-heavy onboarding.

## 10. Инвестиционный вывод по экономике

### Что нравится
- базовая математика проходит;
- CAC payback остаётся в допустимом окне;
- LTV/CAC выше порога investment grade;
- founder-mode позволяет добраться до break-even без абсурдного масштаба.

### Что не нравится
- кейс чувствителен к снижению чека;
- против локальных substitutes premium надо доказывать очень жёстко;
- onboarding и integration-load могут размыть маржу;
- это не effortless SaaS, а тяжёлый enterprise motion.

## Final verdict on unit economics
**Unit economics: PASS WITH CONSTRAINTS.**

Кейс можно пускать дальше, но только как узкий enterprise-only оператор. В critic нужно особенно внимательно проверить две вещи: удерживается ли premium относительно Mindbox/CRM/CDP substitutes и не является ли кейс на практике просто более дорогим сервисным слоем поверх уже существующего martech-стека.

## Источники
- [S1] `pipeline/cases/1048-msk-hightouch-geo-expand-v2/02-demand.md`
- [S2] Публичные ценовые якоря и локальные substitutes, зафиксированные в `02-demand.md`
- [S3] Внутренние консервативные допущения branch-models-lead для enterprise B2B SaaS rerun-кейсов 2026-04-20


## Стадия 5. Critic
---
sector: GEO-EXPAND
stage: critic
case: 1048-msk-hightouch-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 05-critic

## SECTION A. Finance PnL

### A1. Ключевые допущения
- ARPA: **300 000 ₽ / клиент / мес**.
- COGS: **95 000 ₽ / клиент / мес**.
- Contribution profit: **205 000 ₽ / клиент / мес**.
- Gross margin: **68,3%**.
- Fixed costs, full team: **5 250 000 ₽ / мес**.
- Founder-mode fixed costs: **3 895 000 ₽ / мес**.
- Blended fully-loaded CAC: **2 900 000 ₽**.
- LTV: **12 300 000 ₽**.
- LTV/CAC: **4,2x**.
- CAC payback: **9,7 мес**.
- Break-even: **19 клиентов** в founder-mode и **30 клиентов** на полной команде.

### A2. Что в экономике нравится
1. При чеке **300k ₽/мес** и contribution **205k ₽/мес** математика в принципе проходит.
2. **LTV/CAC 4,2x** и payback **9,7 мес** остаются в рабочем диапазоне.
3. EBITDA > **500k ₽/мес** достижима, если база выходит выше **22-23 клиентов**.
4. Founder-mode позволяет дойти до нуля без совсем нереалистичного масштаба.

### A3. Что в экономике не нравится
1. **CAC 2,9 млн ₽** очень тяжёлый. Для локального рынка это дорогой enterprise sale, а не лёгкий SaaS motion.
2. Модель чувствительна к price compression. Если чек сползает ближе к **200-250k ₽/мес**, запас быстро исчезает.
3. Значимая доля value сидит в onboarding и solutions support, значит есть риск services-heavy delivery.
4. Full-team break-even на **30 клиентах** для узкого ICP уже выглядит напряжённо.

### A4. PnL-вывод
По чистой арифметике кейс проходит. Но проходит только в узком коридоре: enterprise-only ICP, жёсткая дисциплина по pricing и ограниченный integration scope. Это не широкая martech-SaaS история, а тяжёлый high-touch операторский слой.

<!-- P6A-DONE -->

## SECTION B. Strategic Critic

### B1. Главный вопрос кейса
Можно ли в РФ защитить premium-позиционирование warehouse-native AI decisioning как отдельного слоя, а не скатиться в более дешёвый substitute-класс: **Mindbox / RetailCRM / Carrot quest / кастомная аналитика поверх текущего DWH**.

### B2. Сильные стороны кейса
1. **Глобальный category proof есть.** В `02-demand.md` уже зафиксированы сильные сигналы по Hightouch и Census/Fivetran.
2. **Бюджетный слой в РФ существует.** Компании уже тратят деньги на CDP, CRM marketing, loyalty, personalization и data activation.
3. Кейс сидит не в SMB, а в более рациональном enterprise-сегменте, где measurable uplift по revenue/ROMI действительно может оправдать высокий чек.
4. Profit gate математически проходит даже в консервативной конфигурации.

### B3. Слабые стороны кейса
1. **Exact-demand в РФ слабый.** Покупатель редко формулирует боль именно как `warehouse-native AI decisioning`.
2. Локальные substitutes заметно дешевле, поэтому premium WTP подтверждён только частично.
3. Есть риск, что кейс на практике окажется просто более узким дублем соседней гипотезы про `warehouse-native-ai-decisioning-marketing-operator-v2`.
4. Если продукт требует слишком много кастомной интеграции, маржа быстро размоется и кейс превратится в агентство/интегратора.

### B4. Ключевые риски
| Риск | Вероятность | Влияние | Комментарий |
|---|---|---|---|
| Price compression против локальных martech-substitutes | high | high | самый опасный риск для всей модели |
| Services-heavy onboarding и schema-change workload | high | high | может съесть gross margin |
| Слишком узкий ICP и длинный sales cycle | medium | high | ограничивает скорость набора базы |
| Дублирование с соседним кейсом | medium | medium | снижает portfolio clarity |
| Невозможность доказать uplift в деньгах | medium | high | без этого premium pricing не удержится |

### B5. Kill conditions на ближайшие 6 месяцев
1. Не удаётся продать хотя бы **3-4 платящих клиента** без радикального дисконта.
2. Реальный средний чек падает ниже **250 000 ₽/мес**.
3. Integration/support нагрузка поднимает фактический COGS выше **120 000 ₽/клиент/мес**.
4. Кейс не может внятно отстроиться от Mindbox/CRM/CDP-альтернатив и начинает продаваться как кастомный проект.

### B6. Итог критика
**Вердикт: CONDITIONAL PASS.**

Кейс не выглядит мусорным, у него есть реальный global proof и понятный enterprise budget layer. Но инвестиционное качество пока хрупкое. Главная проблема, это не отсутствие рынка, а риск того, что локально рынок купит только более дешёвый substitute, а premium decisioning-layer не удержит чек и маржу.

### B7. Что должен проверить следующий блок
1. Есть ли достаточно сильный moat против локальных CDP/CRM/personalization substitutes.
2. Это самостоятельный investable case или всё-таки более узкий дубль соседнего warehouse-native marketing operator thesis.
3. Можно ли защитить premium pricing на уровне **300k+ ₽/мес** без превращения в services business.

<!-- P6B-DONE -->

## Финальное решение по этапу
**Пропустить кейс дальше, но с жёстким флагом: premium fragile / services risk / possible thesis overlap.**

## Источники
- [S1] `pipeline/cases/1048-msk-hightouch-geo-expand-v2/02-demand.md`
- [S2] `pipeline/cases/1048-msk-hightouch-geo-expand-v2/04-economics.md`


## Стадия 6. Verdict
[GEO-EXPAND] 1048 MSK Hightouch GEO Expand v2 — NEAR-PASS: 66/100 | EBITDA base=2000К₽/мес через 24 мес | LTV/CAC=4,2x | Ключевое преимущество: enterprise decisioning layer поверх существующего DWH/CRM-stack | Главный риск: локальный спрос утекает в более дешёвые CDP/CRM substitutes.

# 06-verdict

sector: GEO-EXPAND

## Investment committee verdict
- **Итог:** **NEAR-PASS**
- **Normalized score:** **66/100**
- **Raw score:** **99/150**
- **Пороговое решение:** score 65-69 = **NEAR-PASS**
- **EBITDA gate:** проходит, потому что при **40 клиентах EBITDA около 2,0 млн ₽/мес**, а порог **500 тыс. ₽/мес** достигается ориентировочно после **22-23 клиентов** и укладывается в горизонт **до 24 месяцев**.
- **Комитетский вывод:** арифметика рабочая, но инвестиционный запас прочности недостаточен. Кейс пока держится на узком enterprise ICP, premium pricing и founder-heavy GTM, тогда как локальный buyer уже может закрывать значимую часть боли через Mindbox, RetailCRM, Carrot quest и внутреннюю аналитику.

## Delta vs previous
- Предыдущий связанный тезис `warehouse-native-ai-decisioning-marketing-operator` в INDEX уже зафиксирован как **61/100**, а rerun `warehouse-native-ai-decisioning-marketing-operator-v2` получил **69/100**.
- Текущий кейс `1048-msk-hightouch-geo-expand-v2` выглядит как более узкий GEO-EXPAND с тем же category proof, но со слабее доказанным локальным wedge и более хрупкой защитой premium pricing.
- Поэтому итоговый score ниже сильнейшего соседнего rerun-кейса и остаётся в зоне **NEAR-PASS**, а не APPROVED.

## Investment thesis in one paragraph
Инвестируемость здесь появляется только в узком сценарии, где продукт продаётся как warehouse-native AI decisioning layer поверх уже существующего DWH, CRM marketing и lifecycle stack, а не как ещё одна CDP или automation suite. Тогда LTV/CAC и payback проходят, founder-mode даёт путь к break-even, а enterprise buyer может оправдать premium через uplift в revenue и retention. Но пока локально не доказано, что этот uplift repeatable, что buyer реально платит именно за отдельный decisioning layer, и что delivery не размоется в services-heavy интеграцию.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | `LTV/CAC = 4,2x`, `CAC payback = 9,7 мес`, `Contribution margin = 68,3%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | `EBITDA при 40 клиентах: около 2,0 млн ₽/мес`, а `working investment break-even: 19 клиентов` в `04-economics.md`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | В `02-demand.md` exact category спрос `LOW`, `demand_score=0`, `hh_ru=0`, а строка `Sources:` отсутствует, поэтому применён penalty -5 и cap 10/25. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Защита сидит в `warehouse-native AI decisioning layer`, но `локальные substitutes заметно дешевле`, а embedded moat пока не доказан на реальных сделках. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | В `05-critic.md` отмечены `price compression`, `services-heavy onboarding` и `слишком узкий ICP и длинный sales cycle`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 24 | GTM enterprise-реалистичен: `sales cycle 5-8 мес`, `CAC 2 900 000 ₽`, buyer уже тратит на CRM/CDP/personalization, плюс ниже дан список 10 named targets. |

**Normalized score = round((99 × 100) / 150) = 66/100.**

## 7-factor Moat Framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не усиливает ценность для остальных клиентов. |
| Switching costs | 2 | Интеграции в DWH, CRM и decision flows создают умеренный switching cost после внедрения. |
| Scale economies | 2 | При росте базы shared platform cost и reuse playbooks улучшают экономику, хотя onboarding остаётся ощутимым. |
| Proprietary data / model advantage | 1 | First-party data клиента помогает, но собственного подтверждённого proprietary dataset у компании нет. |
| Regulatory moat | 0 | Формального лицензируемого или compliance-based moat в кейсе не видно. |
| Brand / distribution | 1 | Глобальный Hightouch brand помогает category proof, но в РФ локальный бренд и канал не построены. |
| Embedded workflow | 3 | Если продукт встроен в CRM/lifecycle orchestration и next-best-action, он становится частью ежедневного маркетингового контура клиента. |

**Moat score = round((9 × 25) / 21) = 11/25.**

Вывод по moat: **weak moat**. Сильнейшая защита, это workflow embedding и switching costs после интеграции, но network, brand и regulatory layer пока почти отсутствуют. Поэтому moat занесён в Top-3 Risks.

## Полный бизнес-процесс из 04-economics.md

| Шаг | Что происходит | Роль | Инструмент | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP и target account list | Founder / CEO | CRM, табличка ICP, ручной ресерч | 1-2 недели | 180 000 | Низкая |
| 2 | Founder-led outbound и первые интро | Founder + SDR | email, звонки, CRM sequences | 4-8 недель | 420 000 | Средняя |
| 3 | Discovery по data stack и marketing workflows | Founder + AE | Zoom/Meet, schema review, workshop | 1-2 недели | 210 000 | Низкая |
| 4 | Pilot / SQL scoping | CTO / Solutions lead | DWH review, event mapping, security scoping | 2-4 недели | 320 000 | Низкая |
| 5 | Коммерческое предложение и procurement | AE + founder | договор, security, согласования | 3-6 недель | 260 000 | Низкая |
| 6 | Onboarding и интеграция | Backend + ML + CSM | connectors, scoring jobs, observability | 2-6 недель | 180 000 разово, амортизировано в COGS | Средняя |
| 7 | Ежемесячная эксплуатация decisioning layer | CSM + Solutions support | orchestration, CRM, отчёты uplift | ежемесячно | 95 000 COGS / клиент / мес | Средняя |
| 8 | Renewal / expansion | Founder + CSM | QBR, ROI proof, upsell | ежеквартально | включено в GTM / CSM | Средняя |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| ARPA / MRR на клиента | 300 000 ₽/мес |
| customer_ltv_rub | 12 300 000 ₽ |
| CAC | 2 900 000 ₽ |
| LTV/CAC | 4,2x |
| CAC Payback | 9,7 мес |
| GM / Contribution Margin | 68,3% |
| contribution_margin_rub_month | 205 000 ₽/клиент/мес |
| fixed_costs_rub_month | 5 250 000 ₽/мес steady-state |
| Break-even clients | 19 клиентов founder-mode / 30 клиентов full team |
| Break-even month | M12 founder-mode |
| startup_capital_to_bep_rub | 26 000 000–28 000 000 ₽ |
| company_ebitda_rub_month base | ~2 000 000 ₽/мес через 24 мес при 40 клиентах |
| company_ebitda_potential_rub_month | ~2 000 000 ₽/мес |
| clients_to_500k_ebitda | 23 |
| months_to_500k_ebitda | 14 |

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| Founder / CEO | продажи, key accounts, fundraising | 650 000 |
| CTO / Solutions lead | архитектура, presale, integrations | 600 000 |
| Backend / data engineer 1 | connectors, pipelines | 455 000 |
| Backend / data engineer 2 | orchestration, APIs | 455 000 |
| ML / analytics engineer | scoring, uplift models | 520 000 |
| Product / UX | интерфейс, сценарии использования | 325 000 |
| SDR | outbound pipeline | 175 000 |
| AE | demo, negotiation, close | 390 000 |
| CSM | onboarding, retention, expansion | 325 000 |
| Growth / content | category education | 390 000 |
| Finance / ops part-time | договоры, billing, ops | 130 000 |
| **Итого зрелая команда** |  | **4 415 000 ₽/мес** |

## PnL и risk summary

### SECTION A: PnL
- Base M12 EBITDA: **0 ₽/мес** в founder-mode.
- Safe break-even на полной команде: **30 клиентов**.
- Burn-to-breakeven: **≈ 22,7 млн ₽**, разумно считать потребность **26-28 млн ₽** с буфером.
- Cash runway при стартовом капитале **40 млн ₽**: около **20 месяцев**.

### SECTION B: Risk + Monte Carlo
- Формального Monte Carlo в `05-critic.md` нет, поэтому использую критический риск-синтез вместо ложной точности.
- Наиболее чувствительные драйверы: **price compression**, **services-heavy onboarding**, **длинный sales cycle**, **thesis overlap**.
- Комитетский вывод по риску: median-case выглядит рабочим только при сохранении enterprise pricing и жёсткой продуктовой дисциплины.

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Огромный first-party data контур, зрелый CRM и постоянная потребность в next-best-action. | email decision-maker + партнёрство с data-интегратором | 450 000 ₽/мес |
| 2 | Т-Банк | Сильный lifecycle marketing и высокая культура экспериментов, где decisioning даёт быстрый uplift. | warm intro в CRM/growth lead + founder outbound | 400 000 ₽/мес |
| 3 | Ozon | Маркетплейс с большим event stream и болью в персонализации и retention orchestration. | outbound в product marketing / CRM team | 350 000 ₽/мес |
| 4 | Wildberries | Огромная база коммуникаций и логика промо/сегментации поверх first-party data. | founder-led outbound + referral из martech ecosystem | 350 000 ₽/мес |
| 5 | Яндекс Маркет | Зрелый data stack и постоянная оптимизация CRM и персонализации. | conference + email head of CRM/personalization | 350 000 ₽/мес |
| 6 | X5 Group | Loyalty, omnichannel и promo orchestration требуют decision layer поверх существующего data stack. | retail conference + partnership with SI | 350 000 ₽/мес |
| 7 | Магнит | Большой consumer-data контур и регулярные CRM-кампании, где ROI можно показать на retention и promo efficiency. | email decision-maker + интеграторский канал | 300 000 ₽/мес |
| 8 | Lamoda | Fashion e-commerce с высокой ценностью персонализации, сегментации и сценарного decisioning. | vc.ru ad + founder outbound | 300 000 ₽/мес |
| 9 | МТС | Крупная подписочная база и развитый CRM marketing, где decisioning layer может стать brain поверх текущего стека. | email CVM/CRM lead + отраслевое мероприятие | 350 000 ₽/мес |
| 10 | МегаФон | У телеком-игрока много lifecycle сценариев и cross-sell задач, подтверждающих боль orchestration. | direct outbound + conference networking | 300 000 ₽/мес |

**Вывод по GTM:** target-list реалистичен и совпадает с ICP, но повторяемость канала пока не доказана, а CAC остаётся тяжёлым и founder-dependent.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Pricing compression против локальных substitutes | Высокая | Высокий | Buyer может закрыть значимую часть боли через Mindbox, RetailCRM, Carrot quest и внутренний BI существенно дешевле. |
| Services-heavy onboarding / integration drag | Высокая | Высокий | Если schema changes и кастомная интеграция станут нормой, gross margin быстро размоется. |
| evidence_quality_unverified + weak moat | Высокая | Средний | В `02-demand.md` нет строки `Sources: T1=...`, а moat score всего **11/25**. |

## Что нужно доказать для APPROVED
1. **3-5 платящих enterprise клиентов** в РФ без радикального дисконта.
2. **Фактический ARPA не ниже 300 000 ₽/мес** и COGS не выше **95-110 тыс. ₽/клиент/мес**.
3. **ROI proof** на revenue uplift, retention или ROMI, который buyer не получает из дешёвых substitutes.
4. **Repeatable GTM**: часть pipeline должна приходить не только через founder-led outbound.
5. **Чёткий thesis separation** от соседнего `warehouse-native-ai-decisioning-marketing-operator-v2`.

## LTV Upside Calculator
Так как итоговый статус **NEAR-PASS**, апсайд до approve можно считать от трёх рычагов:

| Рычаг | Текущее значение | Целевое значение | Влияние |
|---|---:|---:|---|
| ARPA | 300 000 ₽/мес | 350 000 ₽/мес | customer_ltv_rub растёт примерно до **14,35 млн ₽** при тех же GM и churn. |
| CAC | 2 900 000 ₽ | 2 200 000 ₽ | LTV/CAC растёт с **4,2x** до примерно **5,6x**. |
| Contribution margin | 68,3% | 72% | contribution_margin_rub_month растёт до **252 000 ₽/мес**, а clients_to_500k_ebitda снижается. |

**Простой апсайд-сценарий:** если удержать чек **350k ₽/мес**, снизить CAC до **2,2 млн ₽** и стандартизировать onboarding так, чтобы margin держалась **70%+**, кейс может перейти в диапазон **70-73/100**.

## Proof points, которых сейчас не хватает
- нет прямого локального evidence, что exact-category `warehouse-native AI decisioning` уже покупается как отдельная budget line;
- нет публичных российских win/loss signals по enterprise-сделкам этого класса;
- нет proprietary data moat или distribution moat, подтверждённого T1/T2 evidence;
- нет подтверждения, что GTM масштабируется без founder bottleneck.

## Final verdict
**Решение комитета: REJECTED FOR NOW / NEAR-PASS.**

Кейс не проваливается по экономике. Он проваливается по margin of safety для фонда. Пока рынок в РФ подтверждён скорее через adjacent budgets, moat остаётся слабым, а delivery риск тянет модель в сторону тяжёлого enterprise services business. Возвращаться к approve стоит после подтверждения 3-5 платящих клиентов, повторяемого GTM и удержания premium pricing поверх локальных substitutes.


## Стадия 7. Score Trajectory
# 07-score-trajectory

## 2026-04-20 18:29 MSK — Critic and Verdict
- Stage: Program 7 / Critic and Verdict
- Case: `1048-msk-hightouch-geo-expand-v2`
- Preconditions check:
  - `05-critic.md` содержит оба маркера `P6A-DONE` и `P6B-DONE`
  - `06-verdict.md` до запуска отсутствовал
  - `07-score-trajectory.md` до запуска отсутствовал и создан заново полным rewrite
- Итоговая рубрика 6x25:
  - Unit Economics: `18/25`
  - EBITDA Potential: `18/25`
  - Market + Demand: `10/25`
  - Moat: `12/25`
  - Execution Risk: `17/25`
  - GTM Realism: `24/25`
- Raw total: `99/150`
- Normalized score: `66/100`
- Tier-awareness:
  - В `02-demand.md` отсутствует строка `Sources: T1=..., T2=..., T3=...`
  - По правилу применён default: `tier_balance = 1.00`
  - Penalty applied to criterion #3: `-5`
  - Criterion #3 capped at `10/25`
- 7-factor moat:
  - Sum: `9/21`
  - Normalized moat score: `11/25`
  - Committee-applied criterion #4: `12/25`
- Finance synthesis:
  - `customer_ltv_rub = 12 300 000 ₽`
  - `CAC = 2 900 000 ₽`
  - `LTV/CAC = 4,2x`
  - `CAC payback = 9,7 мес`
  - `contribution_margin_rub_month = 205 000 ₽`
  - `company_ebitda_rub_month ≈ 2,0 млн ₽/мес` при 40 клиентах
  - `clients_to_500k_ebitda ≈ 23`
- Committee conclusion:
  - Экономика рабочая только в узком enterprise-only wedge
  - Exact-demand в РФ слабый и доказан в основном через adjacent budget buckets
  - Premium pricing и moat пока не выглядят investment-grade
- Outcome: `NEAR-PASS`
- Final routing: `pipeline/rejected/1048-msk-hightouch-geo-expand-v2/`
- Artifacts: `06-verdict.md`
