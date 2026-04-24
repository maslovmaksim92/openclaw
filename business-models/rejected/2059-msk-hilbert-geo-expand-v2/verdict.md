# verdict
Источник pipeline: /home/node/.openclaw/workspace/branch-models-lead/pipeline/rejected/2059-msk-hilbert-geo-expand-v2

## Стадия 1. Intake
---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-2059-msk-hilbert-geo-expand.md
created: 2026-04-20T03:12:00+03:00
---

# 01-intake

## Кейс
2059-msk-hilbert-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-17-2059-msk-hilbert-geo-expand-duplicate.md

## Краткий контекст
Hilbert: warehouse-native AI decisioning / growth intelligence для B2C-команд. Ранее сигнал закрывался как duplicate отклонённого кейса, но resurrect-режим обязывает прогнать его заново как standalone candidate.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — 2059-msk-hilbert-geo-expand

## Meta
- source: triage/triage-2026-04-17-2059-msk-hilbert-geo-expand-duplicate.md
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
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-2059-msk-hilbert-geo-expand.md`

## Классификация
Дубликат ранее обработанного сигнала.

## Решение
Новый кейс не создавался и открытый кейс не обогащался.

## Почему это дубликат
- Сигнал полностью совпадает по компании, категории и сути гипотезы с ранее обработанным Hilbert GEO-EXPAND сигналом.
- По этому сигналу уже был создан и затем полноценно оценён кейс `warehouse-native-ai-decisioning-marketing-operator`.
- Итоговый вердикт по кейсу уже зафиксирован в `pipeline/rejected/warehouse-native-ai-decisioning-marketing-operator/06-verdict.md` как **REJECTED**.

## Почему кейс не переоткрывается
- Во входном файле нет новых фактов, которые меняют economics, спрос или defendability относительно уже проведённой оценки.
- В `pipeline/cases/` нет открытого кейса по этой теме, который следовало бы обогатить supporting signal.
- Повторное создание того же кейса без нового materially stronger evidence нарушило бы чистоту пайплайна.

## Статус raw-файла
Файл подлежит переносу в `pipeline/raw/processed/`.

## Вердикт
Сигнал закрыт как дубликат уже обработанной и отклонённой гипотезы по warehouse-native AI decisioning для marketing/growth команд.

```



## Стадия 2. Demand / Validation
---
stage: demand-validation
case: 2059-msk-hilbert-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
sector: GEO-EXPAND
---

# 02-demand — Demand Validation

## Кейс
2059 MSK Hilbert GEO Expand, AI-native growth infrastructure для B2C-команд: warehouse-native decisioning, growth intelligence, прогнозирование поведения, приоритизация действий и агентное исполнение retention / acquisition / monetization сценариев.

## Итог
**Статус: CONDITIONAL PASS**

По точному RU-спросу категория выглядит слабой. Demand API по `warehouse native ai decisioning marketing` вернул **LOW** и `demand_score=0`, а смежные запросы `marketing decision engine` и `growth intelligence platform` тоже остались в зоне **LOW**. Это означает, что в РФ категория почти не покупается по exact label Hilbert.

Но слой денег у категории существует. На **15 апреля 2026 года** Hilbert закрыла **$28 млн Series A**, а a16z описала pain как дорогой и дефицитный слой growth data plumbing. На сайте Hilbert продукт продаётся не как BI, а как связка detect → reason → act → optimize для acquisition, retention и monetization. Параллельно Hightouch уже продаёт **AI Decisioning** как отдельный enterprise-продукт, а Mindbox показывает, что в РФ существует платёжеспособный бюджет на CDP, персонализацию и lifecycle automation, с тарифами **от 150 000 ₽/мес** и **от 400 000 ₽/мес**.

Вывод: exact keyword demand слабый, но adjacent enterprise spend подтверждён и глобально, и локально. Поэтому кейс можно пропускать дальше, однако условно: в P4-P6 нужно жёстко проверить, защищается ли premium wedge Hilbert поверх локальных substitutes и не превращается ли продукт в тяжёлый semi-service слой.

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
- `marketing decision engine` → **LOW**, `google_trends_ru=1`, `hh_ru=8`, `habr_articles=2`, `yandex_suggest=2`
- `growth intelligence platform` → **LOW**, `google_trends_ru=0`, `hh_ru=2`, `habr_articles=2`, `yandex_suggest=2`

### Интерпретация
В РФ нет сильного evidence, что buyer уже формулирует потребность как warehouse-native AI decisioning или growth intelligence platform. Покупка, если и происходит, идёт через более знакомые бюджеты и названия:
- CDP,
- CRM marketing,
- персонализация,
- lifecycle automation,
- аналитика роста,
- оптимизация маркетинговых решений.

Это ослабляет силу keyword-demand, но не убивает кейс, если есть подтверждённый budget layer в adjacent category.

## 2. Реальные рыночные сигналы и why now
1. **15 апреля 2026 года** a16z объявила об инвестиции в Hilbert и описала pain как сложный слой growth data plumbing, который дорого строить и трудно поддерживать внутри компании.
2. В тот же день Hilbert получила публичный funding signal на **$28 млн Series A**, что подтверждает инвесторскую ставку на отдельную категорию AI-native growth infrastructure для consumer companies.
3. На сайте Hilbert продукт уже продаётся как целостная growth infra, а не просто аналитический dashboard: Detect, Reason, Act, Optimize, плюс claims про запуск после ingestion и переход от decision cycles в месяцы к минутам.
4. Hightouch публично выделяет **AI Decisioning** в отдельный продукт и в документации описывает его как систему автоматизации индивидуальных маркетинговых решений на уровне сообщения, канала и времени отправки.
5. Это усиливает why now: рынок смещается от ручных кампаний и rule-based orchestration к decisioning и agentic execution поверх data warehouse.

## 3. Конкурентные и ценностные якоря

| Якорь | Публичный сигнал | Что это доказывает |
|---|---|---|
| Hilbert | AI-native growth infrastructure, Detect/Reason/Act/Optimize, фокус на B2C growth | продукт продаётся как операционный слой, а не как консультация |
| a16z | публичная инвестиция в Hilbert от 15.04.2026 | проблема достаточно велика и инвестиционно понятна |
| Hightouch AI Decisioning | отдельный продукт и отдельный pricing layer | category уже монетизируется как enterprise software |
| Mindbox | публичные тарифы от 150k/400k ₽ в месяц | в РФ уже существует бюджет на персонализацию и data-driven marketing |

### Вывод по конкурентному полю
Слой decisioning и personalization monetization реален. Но buyer уже может закрывать часть боли через CDP / CRM / performance stack без покупки нового дорогого growth infra. Значит Hilbert-подобный продукт должен продаваться как measurable uplift layer, а не как ещё один data tool.

## 4. Российский контур и кто реально может купить
Реальный ICP в локальном контуре, это не весь рынок, а только компании, у которых уже есть:
- зрелый data warehouse или сильный event/data stack,
- ощутимый маркетинговый бюджет,
- growth / CRM / performance команда,
- регулярные retention и monetization циклы,
- потребность в быстрой приоритизации acquisition-retention-monetization решений.

### Buyer archetypes
1. крупный e-commerce,
2. grocery delivery,
3. travel и ticketing,
4. fintech с lifecycle marketing,
5. subscription-сервисы,
6. marketplaces,
7. телеком с развитым CRM-маркетингом,
8. betting / gaming / entertainment с сильным retention motion.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру **450 000 ₽/мес** как base enterprise чек, или **5,4 млн ₽/год** на клиента.

### TAM
Берём **1 500** потенциально релевантных B2C-аккаунтов в РФ и близком контуре.

**TAM = 1 500 × 5,4 млн ₽ = 8,1 млрд ₽/год**

### SAM
Реально адресуемый слой, где уже есть data maturity и growth-команда:
- **250** аккаунтов.

**SAM = 250 × 5,4 млн ₽ = 1,35 млрд ₽/год**

### SOM
Ранний реалистичный захват:
- **12 клиентов**.

**SOM = 12 × 5,4 млн ₽ = 64,8 млн ₽/год**

## 6. WTP и доказательства готовности платить
1. Hilbert получила funding не как generic analytics tool, а как AI-native growth infra.
2. Hightouch уже монетизирует AI Decisioning как отдельный продукт.
3. Mindbox показывает, что локальные buyers уже платят заметные суммы за CDP, персонализацию и маркетинговую оптимизацию.
4. Но локально пока не доказано, что buyer готов массово платить именно за более тяжёлый warehouse-native / agentic growth infra слой с premium выше CDP и CRM automation substitutes.

### Вывод по WTP
**WTP подтверждён, но premium positioning пока подтверждён ограниченно.**

## 7. Profit Gate
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

## 8. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс стоит двигать дальше в economics, потому что:
1. global category proof заметно усилился свежим funding signal от **15 апреля 2026 года**;
2. category money layer существует и у Hilbert-like vendors, и у локальных substitutes;
3. Profit Gate проходит в нескольких конфигурациях.

Но в P4-P6 нужно особенно жёстко проверить:
- реально ли защищается premium против CDP / CRM substitutes,
- сколько скрытого services load в onboarding и аналитике,
- насколько repeatable обещание `decision cycles from months to minutes`,
- не является ли Hilbert по факту дорогим overlay для already-mature data teams.

## Market Pulse
Market Pulse 20.04.2026: осторожно позитивный.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=warehouse%20native%20ai%20decisioning%20marketing
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=marketing%20decision%20engine
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=growth%20intelligence%20platform
- Hilbert homepage: https://hilberts.ai/
- a16z, Investing in Hilbert, 2026-04-15: https://a16z.com/announcement/investing-in-hilbert/
- Hightouch pricing: https://hightouch.com/pricing/
- Hightouch AI Decisioning docs: https://hightouch.com/docs/ai-decisioning/overview
- Mindbox tariffs: https://mindbox.ru/tariffs/

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
Market Pulse 22.04.2026: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.



## Стадия 3. Solution / GTM Fit
---
stage: solution
case: 2059-msk-hilbert-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
2059 MSK Hilbert GEO Expand, warehouse-native AI decisioning / growth intelligence слой для B2C-команд: обнаружение сигналов, reasoning, выбор действия и исполнение retention / acquisition / monetization сценариев поверх data warehouse.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную «AI-аналитику», а дорогую задачу growth-команд, как быстрее принимать и исполнять маркетинговые решения на основе first-party data.
2. В локальном контуре кейс выглядит жизнеспособно только как overlay над уже зрелым CRM / CDP / DWH стеком, а не как самостоятельный SMB SaaS.
3. Самый реалистичный wedge, decisioning layer для нескольких критичных use cases: churn prevention, next-best-offer, reactivation, frequency control, channel selection.
4. Главный риск, продукт легко схлопывается в дорогую надстройку над Mindbox, внутренним data-science слоем или ручной CRM-оркестрацией, если не доказан measurable uplift и короткий time-to-value.

## 1. Какую проблему реально решает продукт

Hilbert-подобный продукт продаёт не ещё один dashboard, а устранение трёх дорогих потерь:
- ручного decisioning по сегментам и правилам, который быстро устаревает;
- медленного цикла гипотеза → сбор данных → приоритизация → запуск → измерение результата;
- недоиспользования warehouse и event-data в реальных retention / monetization сценариях.

Для зрелого B2C-бизнеса это painkiller, если уже есть большой поток событий, много кампаний и заметный budget owner на growth-метрики. Тогда даже умеренный uplift по retention, conversion или ARPU может окупать платформу лучше, чем ещё один headcount в CRM или DS.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- крупный e-commerce;
- grocery / delivery;
- travel и ticketing;
- fintech с сильным lifecycle marketing;
- subscription-сервисы;
- marketplace;
- betting / gaming / entertainment;
- telecom и digital-first consumer brands.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. свой DWH или зрелый event/data stack;
2. отдельная CRM / retention / growth команда;
3. регулярные acquisition-retention-monetization циклы;
4. buyer с бюджетом на measurable uplift, а не только на «аналитику вообще»;
5. готовность менять operating model, а не просто купить новый интерфейс.

### Нецелевой сегмент
- SMB без зрелой data-инфраструктуры;
- компании, где CRM живёт на простых rule-based рассылках;
- команды без owner'а на growth PnL;
- buyers, которым дешевле добавить аналитика или data scientist, чем внедрять отдельный decisioning layer.

## 3. Продуктовый wedge

### Core wedge
**Warehouse-native growth decisioning**
- использует first-party data напрямую из DWH;
- помогает обнаруживать паттерны и выбирать действие;
- ускоряет путь от сигнала к исполнению;
- работает как learning / optimization layer поверх существующего CRM-маркетинга.

### Что делает wedge сильнее обычной CRM automation
1. **Decisioning вместо фиксированных правил**. Система не только исполняет сценарии, а выбирает лучшее действие, канал, timing и приоритет.
2. **Direct-to-warehouse architecture**. Не нужно поднимать ещё один тяжёлый data silo ради работы с customer signals.
3. **Faster experimentation loop**. Growth-команда быстрее проверяет гипотезы по reactivation, upsell, churn и frequency control.
4. **Revenue-uplift framing**. Продукт можно продавать как слой incremental revenue, а не как ещё одну data-платформу.
5. **Agentic execution narrative**. Если detect → reason → act работает реально, ценность заметно выше BI и ручной аналитики.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как general-purpose AI growth platform;
- попытка идти в mid-market без зрелого DWH;
- обещание «магической персонализации» без чётких KPI pilot;
- слабая интеграция с локальным CRM / CDP / data stack.

### Вариант, который выглядит реалистично
- вход через enterprise pilot на одном monetizable use case;
- buyer сверху, CMO, head of CRM, director of retention, chief digital officer;
- обязательный co-buying со стороны data / martech owner;
- KPI pilot: uplift в retention, conversion, ARPU, repeat purchase или снижение churn;
- внедрение как overlay над существующим стеком, а не rip-and-replace.

## 5. Почему клиент купит это, а не Mindbox или свой стек

У локального клиента уже есть substitutes:
- Mindbox и похожие CDP / CRM automation решения;
- свой DWH + BI + DS + ESP;
- rule-based orchestration внутри текущего martech-стека;
- сильная growth / CRM команда, которая закрывает decisioning вручную.

Hilbert-подобный слой может выиграть только в трёх вещах:
1. **быстрее доводит decisioning до production**, чем внутренняя команда;
2. **даёт measurable uplift**, а не просто новые инсайты и скоринг;
3. **объединяет detect / reason / act**, а не оставляет последний шаг на ручное исполнение.

Если этих преимуществ нет, продукт в глазах локального buyer'а станет дорогой аналитической надстройкой над уже оплаченным стеком.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего CRM / DWH / campaign workflow;
2. выбор одного денежного use case, например churn reduction или next-best-offer;
3. подключение данных, сегментов и каналов активации;
4. 6-10 недель pilot на ограниченном трафике или когорте;
5. сравнение с control / baseline;
6. rollout в соседние сценарии только после доказанного uplift.

### Кто должен быть buyer'ом
- CMO;
- head of CRM / retention;
- growth director;
- chief digital officer;
- martech owner;
- data platform owner как технический co-buyer.

### Кто редко будет настоящим buyer'ом
- отдельный CRM-менеджер без бюджета;
- IT без бизнес-спонсора;
- procurement без владельца growth-метрик.

## 7. Конкурентная позиция

### Против локальных CDP / CRM automation платформ
Преимущество существует, только если Hilbert реально даёт более умный decisioning и measurable uplift поверх уже работающих campaign systems.

### Против in-house data science
Преимущество возникает, если time-to-value короче, а стоимость владения ниже, чем строить собственный orchestration + intelligence слой.

### Против BI / manual analytics
Шанс есть, если продукт не останавливается на insight generation и реально помогает довести решение до действия.

## 8. Основные риски solution-fit

1. **Feature risk**: часть функциональности быстро втягивается в CDP / CRM / ESP stack.
2. **Build-vs-buy risk**: зрелые data-команды решат собрать decisioning сами.
3. **Attribution risk**: uplift сложно честно доказать без нормального эксперимента.
4. **Services risk**: внедрение может деградировать в консалтинг и ручную аналитику.
5. **Localization risk**: западный growth stack и локальный martech-контур отличаются, что может удорожить интеграции.
6. **Narrow ICP risk**: реальный рынок уже, чем кажется из общей категории personalization / CRM.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит enterprise sale с участием solution / data / CSM ресурсов;
- не съедает ли onboarding и аналитический слой gross margin;
- сколько pilot-to-rollout conversion нужно для выхода на 500k+ EBITDA/мес;
- сколько клиентов реально можно дотянуть до production без превращения модели в агентство;
- есть ли в РФ 6-12 клиентов, готовых платить premium поверх Mindbox и собственного data stack.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как enterprise decisioning overlay для data-mature B2C-команд. Продолжать дальше имеет смысл, если economics подтвердит software-first модель, приемлемый services load и доказуемое преимущество над локальными substitutes не на уровне narrative, а на уровне uplift и скорости внедрения.


## Стадия 4. Economics
---
stage: economics
case: 2059-msk-hilbert-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
2059 MSK Hilbert GEO Expand, AI-native growth infrastructure / warehouse-native decisioning для data-mature B2C-команд.

## Executive summary

**Итог P5: CONDITIONAL PASS.**

Экономика выглядит инвестиционно терпимой только как **enterprise software + measured onboarding**, а не как широкий mid-market SaaS.

Что получилось в базовой модели:
- **Средний чек:** 450 000 ₽ MRR на клиента.
- **COGS:** 170 000 ₽ на клиента в месяц.
- **Contribution margin:** 62,2%.
- **Blended fully-loaded CAC:** 823 000 ₽.
- **LTV:** 13 995 000 ₽.
- **LTV/CAC:** 17,0x.
- **CAC payback:** 1,8 месяца по выручке, 2,9 месяца по contribution profit.
- **Break-even:** около **27 клиентов**.
- **500k+ EBITDA/мес:** около **29 клиентов**.
- **На 50 клиентах EBITDA достижима:** около **6,5 млн ₽/мес**.

Вывод: profit gate проходит. Но инвестиционный тезис остаётся условным, потому что модель очень чувствительна к двум вещам: 
1. сможет ли продукт удержать onboarding в рамках software-first delivery, 
2. не вырастет ли CAC выше 1,2-1,5 млн ₽ при реальном enterprise sales cycle.

---

## 1. Ключевые допущения модели

### Pricing
Беру **450 000 ₽/мес** как базовый MRR на клиента.

Почему это реалистично:
- в `02-demand.md` уже использован base-case **450 000 ₽/мес**;
- Mindbox на 24 апреля 2026 года публично показывает **Enterprise от 400 000 ₽/мес**;
- Hilbert продаётся как более тяжёлый decisioning / growth infra слой, значит premium vs CDP допустим, но не бесконечен.

### Сегмент
Это **enterprise / upper mid-market B2C**:
- e-commerce,
- delivery,
- travel,
- subscription,
- fintech lifecycle marketing,
- telecom / marketplace.

### Delivery-модель
- контракт annualized, оплата ежемесячная;
- first deal идёт через pilot + rollout;
- внедрение 6-10 недель;
- нужен DWH / event stack / CRM owner у клиента.

### Churn
Для enterprise SaaS ориентир по customer churn обычно **1-2% в месяц** у высоко-ARPA продуктов. 
Источник benchmark: ChartMogul Help Center, обновление 2025, для SaaS с ARPA **$500+** customer churn обычно **1-2% в месяц**. 

Для Hilbert-like overlay беру **консервативно 2,0% monthly churn**, то есть верхнюю границу benchmark, потому что продукт новый, discretionary и требует доказательства uplift.

---

## 2. Подробный бизнес-процесс: от лида до оплаты

Ниже стоимость дана **в пересчёте на одного нового платящего клиента**, то есть с учётом неудачных касаний и части несостоявшихся сделок.

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов и enrichment | SDR + founder | HH/рынок, CRM, enrichment stack | 6 ч | 55 000 | средняя |
| 2 | Outbound sequence, письма, LinkedIn/VK/Telegram, follow-up | SDR | CRM, sequencer, email | 2-3 недели | 95 000 | высокая |
| 3 | Первичный квалифицирующий созвон | SDR + founder | Meet, CRM | 1 ч + prep | 70 000 | средняя |
| 4 | Discovery с buyer и data owner | Founder/AE | Meet, Miro, CRM | 1-2 недели | 85 000 | низкая |
| 5 | Demo + use-case workshop | Founder + CTO/solution lead | Demo env, slides, BI | 1 неделя | 110 000 | низкая |
| 6 | Pilot scoping, ROI-кейс, техоценка | Founder + CTO + backend/ML | Docs, SQL, sandbox | 2 недели | 150 000 | низкая |
| 7 | Security / legal / procurement review | Founder + CTO + external legal | DPA, SLA, security docs | 2-4 недели | 120 000 | низкая |
| 8 | Коммерческие переговоры и закрытие | Founder + AE | CRM, CPQ, docs | 1 неделя | 70 000 | средняя |
| 9 | Onboarding: schema mapping, интеграции, first agent setup | CTO + backend + ML + CSM | DWH, ETL, product | 4-6 недель | 160 000 | низкая |
| 10 | Счёт, документооборот, первый платёж | Finance ops | ЭДО, банк, billing | 2-3 дня | 10 000 | высокая |

### Что важно
- **Шаги 1-8 = acquisition motion**. Это ядро CAC.
- **Шаг 9 = onboarding cost**, он не должен распухать, иначе компания превращается в semi-service.
- Полная стоимость от первого касания до первого платежа по выигранному клиенту около **925 000 ₽**, из них **765 000 ₽** предоплатный sales+marketing слой и **160 000 ₽** onboarding.

---

## 3. COGS на клиента в месяц

Базовый клиент: 1 бренд, 1-2 активных сценария, monthly optimization, без кастомной разработки под каждого.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Облачная инфраструктура / хранение / ETL share | 35 000 | доля общих infra-cost на 25-50 клиентов |
| LLM / аналитический compute / orchestration | 25 000 | inference + batch reasoning + monitoring |
| Data connectors / activation integrations | 15 000 | амортизация интеграционного слоя |
| Onboarding amortization | 55 000 | 160k onboarding, амортизация на 3 месяца initial recovery |
| Customer Success / support share | 30 000 | 1 CSM на ~8-10 клиентов |
| Solution / analytics support share | 10 000 | точечные настройки и разбор uplift |
| Security / logging / QA / compliance share | 10 000 | SIEM/logging/backup/QA доля |
| Payment ops / billing / docs | 5 000 | ЭДО + финоперации |
| Резерв на SLA credits и incident handling | 15 000 | 3-4% buffer от выручки |
| **Итого COGS** | **170 000** |  |

### Gross profit на клиента
- Revenue: **450 000 ₽/мес**
- COGS: **170 000 ₽/мес**
- **Gross profit: 280 000 ₽/мес**
- **Gross margin / Contribution margin: 62,2%**

Для enterprise AI infra это нормальный, но не выдающийся показатель. Если onboarding начнёт жить дольше 2-3 месяцев, margin быстро сползёт ниже 55%.

---

## 4. CAC по каналам и воронка конверсии

### 4.1. Channel CAC

| Канал | Верх воронки / мес | Meeting rate | SQL rate | Proposal/Pilot rate | Win rate | New paying customers / мес | Monthly spend, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / SDR | 500 target accounts | 12% (60) | 40% (24) | 25% (6) | 33% (2) | 2 | 1 800 000 | 900 000 |
| Партнёры / SI / martech ecosystem | 30 intro | 50% (15) | 60% (9) | 44% (4) | 25% (1) | 1 | 650 000 | 650 000 |
| Контент / вебинары / inbound | 220 leads | 18% (40) | 20% (8) | 50% (4) | 25% (1) | 1 | 720 000 | 720 000 |
| **Blended** | 750 mixed leads/accounts | — | — | — | — | **4** | **3 170 000** | **792 500** |

### 4.2. Fully-loaded CAC

Берём не raw ad CAC, а fully-loaded enterprise CAC.

**Формула:**

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools + Events + Overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс / VK / performance support) | 550 000 | paid acquisition + retargeting + webinar support | модель аналитика, sanity vs RU B2B SaaS spend |
| Outbound team FOT attributed to new | 780 000 | SDR 195k + 50% AE 228k + 42% founder sales time 357k | HH.ru benchmarks + модель загрузки |
| Marketing team FOT (partial allocation) | 160 000 | частичная загрузка founder/growth ops на acquisition content | модель аналитика |
| Tools / CRM / enrichment / webinar stack | 110 000 | CRM + data enrichment + sequencer + webinar tools | модель аналитика |
| Events / partnerships | 300 000 | co-marketing, breakfasts, partner revshare, travel | модель аналитика |
| Subtotal before overhead | 1 900 000 | сумма прямых acquisition-cost |  |
| Overhead multiplier (x1.3) | 570 000 | 30% поверх subtotal | стандарт fully-loaded allowance |
| **Total fully-loaded acquisition cost / мес** | **2 470 000** |  |  |

### 4.3. Fully-loaded CAC result

Если компания привлекает **3 новых платящих клиента в месяц**, тогда:

**Fully-loaded CAC = 2 470 000 / 3 = 823 333 ₽**

Округляю до **823 000 ₽ CAC**.

### Sanity check against benchmark
- Для enterprise SaaS в РФ task brief даёт ориентир **300-900k ₽ CAC**.
- Наша оценка **823k ₽** находится **у верхней границы, но внутри реалистичного диапазона**.
- Это нормально для сложной сделки с DWH, security review и pilot.

Итог: blended raw CAC 792,5k ₽ и fully-loaded CAC 823k ₽ близки, что выглядит логично. Явного занижения CAC не вижу.

---

## 5. LTV и churn

### Benchmark
На основе данных ChartMogul для SaaS с высоким ARPA customer churn обычно **1-2% monthly**. 
Для Hilbert-like decisioning overlay я беру **2,0% monthly churn** как консервативный сценарий, потому что:
- продукт новый;
- buyer может вернуться в Mindbox / Braze / in-house stack;
- часть клиентов может отвалиться после pilot, если uplift плохо доказывается.

### LTV formula
`LTV = MRR × Gross Margin / Monthly Churn`

Подставляем:
- MRR = **450 000 ₽**
- Gross Margin = **62,2%**
- Monthly churn = **2,0%**

`LTV = 450 000 × 0.622 / 0.02 = 13 995 000 ₽`

**LTV = ~14,0 млн ₽ на клиента**

Это высокий LTV, но он объясним при enterprise ACV и низком churn. Самая большая чувствительность тут в churn: если реальный churn будет не 2%, а 4%, LTV сразу падает вдвое.

---

## 6. LTV/CAC, CAC payback, contribution margin

### LTV/CAC
- LTV = **13 995 000 ₽**
- CAC = **823 000 ₽**

`LTV/CAC = 13 995 000 / 823 000 = 17,0x`

**Результат: 17,0x**

Инвестиционный порог **>=3,0x** проходит с большим запасом.

### CAC Payback
По инструкции sanity check:

`CAC Payback = CAC / MRR per customer`

`823 000 / 450 000 = 1,83 месяца`

**Payback по выручке = 1,8 месяца**

Более строгий вариант, через contribution profit:

`823 000 / 280 000 = 2,94 месяца`

**Payback по gross profit = 2,9 месяца**

Оба значения сильно лучше enterprise-порога `<18 мес`.

### Contribution Margin %
`(Revenue - COGS) / Revenue = (450 000 - 170 000) / 450 000 = 62,2%`

**Contribution Margin = 62,2%**

---

## 7. Team & FOT

### 7.1. Полная таблица команды

| Роль | Функция | Salary gross, ₽/мес | Страх. взносы 30% | Fully-loaded FOT, ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | sales, fundraising, product narrative, key accounts | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | architecture, security, delivery quality | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | data pipelines, product backend | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | connectors, activation, infra logic | 450 000 | 135 000 | 585 000 |
| ML Engineer | decisioning, modeling, experimentation | 500 000 | 150 000 | 650 000 |
| DevOps | infra, CI/CD, reliability, cost control | 350 000 | 105 000 | 455 000 |
| Frontend | UI, analyst console, reporting | 300 000 | 90 000 | 390 000 |
| SDR | outbound pipeline generation | 150 000 | 45 000 | 195 000 |
| AE | discovery, proposal, close | 350 000 | 105 000 | 455 000 |
| Customer Success | onboarding, QBR, retention | 250 000 | 75 000 | 325 000 |
| **Итого** |  | **4 000 000** | **1 200 000** | **5 200 000** |

### 7.2. Hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1.5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 150 000 + bonus | 0.5-1 | 1 | 45 000 | 195 000 |
| AE | 1 | 350 000 + commission | 1-2 | 2-3 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Benchmarks по зарплатам
Использую task brief как коридор и sanity-check через HH.ru:
- senior backend в Москве встречается в диапазоне **400-600k ₽**;
- ML engineer по live postings доходит до **512-768k ₽ gross**;
- SDR для B2B SaaS встречается около **100-150k ₽** base;
- account executive / B2B software sales встречается около **150-250k ₽** base и выше, плюс variable.

### 7.3. Cumulative FOT timeline M1-M12

План найма с учётом time-to-hire и без unrealistic mass hiring в первый месяц.

| Месяц | Кто подключается | FOT_monthly, ₽ |
|---|---|---:|
| M1 | Founder only | 845 000 |
| M2 | + SDR | 1 040 000 |
| M3 | + CTO, + Backend #1 | 2 340 000 |
| M4 | + Backend #2, + Frontend, + DevOps, + AE | 4 225 000 |
| M5 | + ML Engineer | 4 875 000 |
| M6 | + CSM | 5 200 000 |
| M7 | full team | 5 200 000 |
| M8 | full team | 5 200 000 |
| M9 | full team | 5 200 000 |
| M10 | full team | 5 200 000 |
| M11 | full team | 5 200 000 |
| M12 | full team | 5 200 000 |

### Комментарий по realism
- В **M1 не нанимается 5+ человек**, значит sanity check пройден.
- **FOT M1-M6** выглядит дорогим, но реалистичным для enterprise AI infra.
- После **25+ клиентов** потребуется как минимум ещё 1 AE и 1 CSM. В seed-модели они пока не включены, поэтому после break-even margin будет чуть хуже, чем в статике.

---

## 8. Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT | 5 200 000 | полная команда из 10 человек |
| Core cloud / shared infra not in per-client COGS | 300 000 | базовая платформа, observability, storage reserve |
| SaaS tools / admin stack | 120 000 | Notion/Jira/Git/CRM/admin |
| Legal / бухгалтерия / HR / payroll ops | 180 000 | аутсорс + точечный legal |
| Office / travel / founders meetings | 150 000 | гибридная модель, не full office |
| Acquisition program (ongoing) | 900 000 | поддержание pipeline после старта |
| Misc / contingency | 250 000 | буфер на рекрутинг, инциденты, командировки |
| **Итого fixed costs / мес** | **7 100 000** |  |

Это база для steady-state. В ранние месяцы burn ниже, потому что команда нанимается ступенчато, но к M6 компания выходит именно на этот порядок затрат.

---

## 9. Break-even

### 9.1. Break-even по количеству клиентов

Contribution profit на 1 клиента:
- **280 000 ₽/мес**

Fixed costs:
- **7 100 000 ₽/мес**

`Break-even clients = 7 100 000 / 280 000 = 25,4`

С operational buffer округляю до **27 клиентов**.

### 9.2. 500k+ EBITDA threshold

Чтобы получать **EBITDA >= 500 000 ₽/мес**, нужно покрыть:
- 7,1 млн fixed costs
- +0,5 млн target EBITDA

`(7 100 000 + 500 000) / 280 000 = 27,1`

Округляю до **29 клиентов**.

### 9.3. Проверка на 50 клиентах

- Revenue: `50 × 450 000 = 22 500 000 ₽/мес`
- COGS: `50 × 170 000 = 8 500 000 ₽/мес`
- Gross profit: **14 000 000 ₽/мес**
- EBITDA after fixed costs: `14 000 000 - 7 100 000 = 6 900 000 ₽/мес`

Даже если добавить ещё 400k ₽ на масштабирование команды, EBITDA всё равно будет **~6,5 млн ₽/мес**.

**Следовательно, Profit Gate PASS.**

### 9.4. Break-even по месяцам

Осторожный ramp новых платящих клиентов:
- M6: 1
- M7: 2 cumulative
- M8: 4
- M9: 6
- M10: 9
- M11: 12
- M12: 15
- M13: 18
- M14: 21
- M15: 24
- M16: 27

При таком темпе **операционный break-even наступает около M16**.

Это довольно долгий цикл. Для фонда это значит, что без достаточного стартового капитала компания может задохнуться до выхода на self-sustaining run-rate.

---

## 10. Burn-to-breakeven и cash runway

### 10.1. Burn-to-breakeven

Упрощённая модель burn по стадиям:
- M1: 1,7 млн ₽
- M2: 2,0 млн ₽
- M3: 3,3 млн ₽
- M4: 5,5 млн ₽
- M5: 6,4 млн ₽
- M6: 6,8 млн ₽
- M7-M12: 5,0-6,2 млн ₽ net burn после первых клиентов
- M13-M16: burn быстро снижается и около M16 становится нулевым

**Суммарный cash burn до break-even: ~58-62 млн ₽**.

Для enterprise AI infra это тяжёлая, но не абсурдная цифра. Ниже **10 млн ₽** модель точно была бы нереалистичной, и здесь sanity check пройден.

### 10.2. Cash runway

Если `startup_capital = 60 000 000 ₽` и средний burn первых 12 месяцев около **5,7 млн ₽/мес**, тогда:

`Runway = 60 000 000 / 5 700 000 = 10,5 месяца`

**Статический runway = ~10,5 месяца.**

Но так как revenue начинает появляться после M6, эффективный runway чуть длиннее, примерно **12-13 месяцев**, если команда удерживает CAC и не распухает в delivery headcount.

Вывод: для этой модели безопаснее иметь **не меньше 70-75 млн ₽ стартового капитала**, иначе риск кассового разрыва до break-even слишком высок.

---

## 11. Чувствительность модели

### Bull case
- MRR 550k ₽
- COGS 170k ₽
- CAC 750k ₽
- churn 1,5%

Тогда модель выглядит очень сильной, break-even падает к 21-23 клиентам.

### Bear case
- MRR 400k ₽
- COGS 220k ₽
- CAC 1,2 млн ₽
- churn 3%

Тогда:
- contribution = 180k ₽
- break-even = 40+ клиентов
- seed burn до break-even заметно растёт

Именно bear case является главным инвестиционным риском. Если onboarding и pre-sale становятся слишком кастомными, экономика быстро деградирует.

---

## 12. Итоговый вердикт по economics

**Вердикт: CONDITIONAL PASS.**

Почему не reject:
1. **LTV/CAC намного выше 1:1 и выше 3:1**.
2. **500k+ EBITDA/мес достижима задолго до 50 клиентов**.
3. CAC находится в реалистичном enterprise диапазоне, а не выглядит искусственно заниженным.

Почему всё ещё conditional:
1. break-even поздний, около **M16**;
2. до break-even нужно примерно **60 млн ₽** сжигания;
3. сервисная нагрузка на pilot/onboarding остаётся главным риском схлопывания margin;
4. модель держится на предположении, что средний чек **>=450k ₽** и churn **не хуже 2%/мес**.

## Что нужно проверить на следующем этапе
1. Есть ли moat против Mindbox / Braze / in-house DS не только по narrative, но по удержанию клиента.
2. Насколько реально стандартизировать onboarding и не держать под каждого клиента mini-consulting squad.
3. Есть ли у Hilbert защита от price compression, когда buyer скажет: «это ещё один decisioning layer поверх уже купленного martech stack».

## Источники
- Hilbert homepage: https://hilberts.ai/
- a16z, Investing in Hilbert, 2026-04-15: https://a16z.com/announcement/investing-in-hilbert/
- Mindbox tariffs, accessed 2026-04-24: https://mindbox.ru/tariffs/
- Hightouch AI Decisioning docs, accessed 2026-04-24: https://hightouch.com/docs/ai-decisioning/overview
- ChartMogul Help Center, Customer Churn Rate, accessed 2026-04-24: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- HH.ru search, senior backend engineer Moscow, accessed 2026-04-24: https://hh.ru/vacancies/senior-backend-engineer
- HH.ru search, machine learning engineer Moscow, accessed 2026-04-24: https://hh.ru/vacancies/machine-learning-engineer
- HH.ru search, account executive Moscow, accessed 2026-04-24: https://hh.ru/vacancies/account_executive
- HH.ru search, account executive full-time Moscow, accessed 2026-04-24: https://hh.ru/vacancies/account_executive/polniy_den


## Стадия 5. Critic Finance
## SECTION A. Finance PnL

### A1. Допущения модели
- База из `04-economics.md`: ARPA **450 000 ₽/мес**, COGS **170 000 ₽/клиент/мес**, gross profit / contribution **280 000 ₽/клиент/мес**, fixed costs steady-state **7 100 000 ₽/мес**.
- Для PnL беру три сценария new clients / churn:
  - **Base:** new clients = 0,0,1,1,1,1,2,2,2,3,3,3; churn **2,0%/мес**.
  - **Optimistic:** new clients = 0,1,1,1,2,2,2,3,3,3,4,4; churn **1,5%/мес**.
  - **Pessimistic:** new clients = 0,0,0,1,1,1,1,1,2,2,2,2; churn **3,0%/мес**.
- Формула клиентов: `Total clients(t) = Total clients(t-1) × (1-churn) + New clients`.
- Cumulative cash показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.94 | 3.88 | 5.80 | 7.68 | 9.53 | 12.34 | 15.09 | 17.79 |
| MRR, ₽ | 0 | 0 | 450 000 | 891 000 | 1 323 180 | 1 746 716 | 2 611 782 | 3 457 546 | 4 284 395 | 5 554 707 | 6 789 613 | 8 005 821 |
| COGS, ₽ | 0 | 0 | 170 000 | 336 600 | 499 834 | 659 426 | 985 562 | 1 304 962 | 1 620 327 | 2 098 445 | 2 564 520 | 3 023 310 |
| Gross profit, ₽ | 0 | 0 | 280 000 | 554 400 | 823 346 | 1 087 290 | 1 626 220 | 2 152 584 | 2 664 068 | 3 456 262 | 4 225 093 | 4 982 511 |
| GM% | 0.0% | 0.0% | 62.2% | 62.2% | 62.2% | 62.2% | 62.3% | 62.3% | 62.2% | 62.2% | 62.2% | 62.2% |
| Fixed costs, ₽ | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 |
| EBITDA, ₽ | -7 100 000 | -7 100 000 | -6 820 000 | -6 545 600 | -6 276 654 | -6 012 710 | -5 473 780 | -4 947 416 | -4 435 932 | -3 643 738 | -2 874 907 | -2 117 489 |
| Cash burn, ₽ | 7 100 000 | 7 100 000 | 6 820 000 | 6 545 600 | 6 276 654 | 6 012 710 | 5 473 780 | 4 947 416 | 4 435 932 | 3 643 738 | 2 874 907 | 2 117 489 |
| Cumulative cash, ₽ | -7 100 000 | -14 200 000 | -21 020 000 | -27 565 600 | -33 842 254 | -39 854 964 | -45 328 744 | -50 276 160 | -54 712 092 | -58 355 830 | -61 230 737 | -63 348 226 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 4 |
| Total clients | 0.00 | 1.00 | 1.99 | 2.96 | 4.91 | 6.84 | 8.74 | 11.61 | 14.44 | 17.22 | 20.96 | 24.65 |
| MRR, ₽ | 0 | 450 000 | 893 250 | 1 329 851 | 2 210 053 | 3 076 902 | 3 930 748 | 5 225 721 | 6 497 335 | 7 745 874 | 9 430 186 | 11 089 734 |
| COGS, ₽ | 0 | 170 000 | 337 450 | 503 054 | 834 020 | 1 163 274 | 1 486 949 | 1 973 272 | 2 454 994 | 2 927 553 | 3 563 626 | 4 189 457 |
| Gross profit, ₽ | 0 | 280 000 | 555 800 | 826 797 | 1 376 033 | 1 913 628 | 2 443 799 | 3 252 449 | 4 042 341 | 4 818 321 | 5 866 560 | 6 900 277 |
| GM% | 0.0% | 62.2% | 62.2% | 62.2% | 62.3% | 62.2% | 62.2% | 62.2% | 62.2% | 62.2% | 62.2% | 62.2% |
| Fixed costs, ₽ | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 |
| EBITDA, ₽ | -7 100 000 | -6 820 000 | -6 544 200 | -6 273 203 | -5 723 967 | -5 186 372 | -4 656 201 | -3 847 551 | -3 057 659 | -2 281 679 | -1 233 440 | -199 723 |
| Cash burn, ₽ | 7 100 000 | 6 820 000 | 6 544 200 | 6 273 203 | 5 723 967 | 5 186 372 | 4 656 201 | 3 847 551 | 3 057 659 | 2 281 679 | 1 233 440 | 199 723 |
| Cumulative cash, ₽ | -7 100 000 | -13 920 000 | -20 464 200 | -26 737 403 | -32 461 370 | -37 647 742 | -42 303 943 | -46 151 494 | -49 209 153 | -51 490 832 | -52 724 272 | -52 923 995 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.97 | 2.91 | 3.82 | 4.71 | 6.57 | 8.37 | 10.12 | 11.82 |
| MRR, ₽ | 0 | 0 | 0 | 450 000 | 886 500 | 1 309 905 | 1 720 608 | 2 119 000 | 2 957 430 | 3 768 707 | 4 553 146 | 5 311 051 |
| COGS, ₽ | 0 | 0 | 0 | 170 000 | 334 900 | 494 852 | 649 563 | 799 378 | 1 116 139 | 1 422 844 | 1 719 966 | 2 007 286 |
| Gross profit, ₽ | 0 | 0 | 0 | 280 000 | 551 600 | 815 053 | 1 071 045 | 1 319 622 | 1 841 291 | 2 345 863 | 2 833 180 | 3 303 765 |
| GM% | 0.0% | 0.0% | 0.0% | 62.2% | 62.2% | 62.2% | 62.2% | 62.3% | 62.3% | 62.2% | 62.2% | 62.2% |
| Fixed costs, ₽ | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 | 7 100 000 |
| EBITDA, ₽ | -7 100 000 | -7 100 000 | -7 100 000 | -6 820 000 | -6 548 400 | -6 284 947 | -6 028 955 | -5 780 378 | -5 258 709 | -4 754 137 | -4 266 820 | -3 796 235 |
| Cash burn, ₽ | 7 100 000 | 7 100 000 | 7 100 000 | 6 820 000 | 6 548 400 | 6 284 947 | 6 028 955 | 5 780 378 | 5 258 709 | 4 754 137 | 4 266 820 | 3 796 235 |
| Cumulative cash, ₽ | -7 100 000 | -14 200 000 | -21 300 000 | -28 120 000 | -34 668 400 | -40 953 347 | -46 982 302 | -52 762 680 | -58 021 389 | -62 775 526 | -67 042 346 | -70 838 581 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 450 000 ₽
- **COGS:** 170 000 ₽
- **Gross profit:** 280 000 ₽
- **Contribution:** 280 000 ₽

#### Waterfall на EBITDA break-even уровне 27 клиентов
- **Revenue:** 12 150 000 ₽/мес
- **COGS:** 4 590 000 ₽/мес
- **Gross profit:** 7 560 000 ₽/мес
- **Contribution:** 7 560 000 ₽/мес
- **EBITDA:** **460 000 ₽/мес**

#### Waterfall на target profit gate уровне 29 клиентов
- **Revenue:** 13 050 000 ₽/мес
- **COGS:** 4 930 000 ₽/мес
- **Gross profit:** 8 120 000 ₽/мес
- **Contribution:** 8 120 000 ₽/мес
- **EBITDA:** **1 020 000 ₽/мес**

#### Net после налогов
- **УСН 6%:** `1 020 000 - 783 000 = 237 000 ₽/мес`
- **IT-льгота 3%:** `1 020 000 - 391 500 = 628 500 ₽/мес`
- **ОСНО 20%:** налог на прибыль ≈ `204 000 ₽`, **net ≈ 816 000 ₽/мес**, но с худшим cash conversion из-за НДС.

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M13 | 53 100 000 ₽ | быстрый rollout почти закрывает год в ноль, но капитал всё равно нужен крупный |
| Base | M16 | 64 500 000 ₽ | траектория повторяет `04-economics.md`, капитализация тяжёлая, но не абсурдная |
| Pessimistic | M20 | 76 000 000 ₽ | при более слабом churn и slower enterprise sales кейс становится очень тяжёлым |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** формально возможно, но на пороге 29 клиентов пост-tax прибыль остаётся слабой.
- **IT-льгота 3%:** лучший режим для software-first growth infra, если компания проходит по аккредитации и структуре выручки.
- **ОСНО 20%:** по прибыли выглядит терпимо, но НДС и enterprise procurement ухудшают кассовую дисциплину.
- **Страховые взносы ~30% к ФОТ:** уже учтены в payroll и fixed-cost base.
- Для кейса критично считать не только EBITDA, но и runway до момента, когда клиентская база перевалит за 27-29 логотипов.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Profit-gate clients (>500k EBITDA) | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 27 | 29 | M13 | нужен почти идеальный rollout без services creep |
| Base | 27 | 29 | M16 | рабочая модель, но cash-burn большой и поздний |
| Pessimistic | 27 | 29 | M20 | enterprise cadence становится слишком медленным для комфортного seed-stage риска |

### A9. Короткий вывод
- Экономика Hilbert-подобного decisioning слоя **не ломается**, если чек держится около **450k ₽/мес** и onboarding не превращается в консалтинг.
- Но первые 12 месяцев кейс остаётся глубоко убыточным, поэтому инвестиционный тезис держится на качестве enterprise pipeline и repeatability rollout.
- На следующем этапе главный вопрос уже не в базовой математике, а в **defensibility против Mindbox / Hightouch / in-house stack** и в риске services creep.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База для расчёта: из SECTION A, M12 base-case = **17,79 клиента** и **EBITDA -2,12 млн ₽/мес**. Для stress-test использую тот же fixed-cost base **7,1 млн ₽/мес** и contribution margin из `04-economics.md`.

| Scenario | Что меняется | Логика расчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | без изменений | 17,79 клиента × 280k contribution - 7,1 млн | **-2 117 000** |
| Sens1 | CAC x2 | enterprise funnel сжимается примерно вдвое, M12 база падает до ~8,9 клиента | **-4 608 000** |
| Sens2 | Churn x2 | churn растёт с 2,0% до 4,0%, M12 база падает до ~15,9 клиента | **-2 648 000** |
| Sens3 | Price -30% | ARPU падает до 315k ₽, contribution/клиент падает до ~145k ₽ | **-4 521 000** |

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 700 000 | 823 000 | 1 500 000 | [T1], [T2] |
| Monthly churn % | 1,5% | 2,0% | 4,0% | [T1], [T3] |
| ARPU ₽/мес | 350 000 | 450 000 | 550 000 | [T1], [T4] |
| Conversion rate lead→paid % | 0,8% | 1,2% | 2,0% | [T2] |
| Time-to-hire месяцев | 1,0 | 1,8 | 3,0 | [T1] |

#### Метод
Не делаю полноценный кодовый Monte Carlo. Вместо этого использую 9 комбинаций вокруг min/mode/max для CAC, churn и ARPU и беру worst/base/best как приближение p10/p50/p90. Цель, проверить устойчивость economics без ложной точности.

#### Обязательная таблица confidence intervals

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | **-1 420 000** | **2 180 000** | **6 720 000** | **8 140 000** |
| CAC payback (мес) | **5,8** | **2,9** | **1,7** | **4,1** |
| LTV/CAC | **3,6x** | **17,0x** | **31,1x** | **27,5x** |
| Cash runway (мес) | **9,4** | **12,2** | **14,8** | **5,4** |

#### Интерпретация Monte Carlo Lite
1. **p10 EBITDA @M24 < 0**, значит downside tail остаётся слишком тяжёлым для безусловного green-light.
2. **p50 EBITDA @M24 = 2,18 млн ₽/мес**, поэтому median-case проходит EBITDA gate.
3. **Range width по LTV/CAC = 27,5x**, что намного выше порога 8. Значит модель очень чувствительна к pricing, churn и enterprise CAC.
4. Вывод, economics рабочая, но confidence нужно снижать на одну ступень из-за высокой вариативности и позднего break-even.

### B3. Competitor deep-dive

#### Топ-3 западных конкурента

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Hightouch** | category leader в warehouse-native activation и AI decisioning, сильный enterprise brand, развитый connector stack [T5][T6] | дорогой западный стек, тяжёлый GTM, для РФ прямой доступ ограничен | **20-25% global warehouse-native activation / decisioning subsegment** [estimate] | локальная data residency, русскоязычный support, продажа как uplift-layer поверх текущего DWH |
| **Braze** | зрелый multichannel suite, сильный engagement workflow, enterprise references [T7] | не warehouse-native by default, выше risk data duplication, тяжелее bundle-buy | **15-20% enterprise engagement / orchestration layer** [estimate] | можем заходить как более узкий decisioning overlay без полной замены CRM suite |
| **Simon Data** | warehouse/CDP + personalization narrative, хороший fit для consumer lifecycle [T8] | слабее бренд и moat, ближе к crowded middle | **3-7% upper-mid personalization / CDP overlay** [estimate] | более узкий wedge, быстрее time-to-value и локализация под РФ compliance |

#### Топ-4 российских конкурента

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Mindbox** | сильнейший локальный бренд в CDP/CRM automation, много enterprise-кейсов, понятный бюджетный якорь [T4][T9] | архитектурно ближе к suite, чем к DWH-native decisioning, плюс vendor lock-in | **25-35% российского enterprise CDP/CRM automation сегмента** [estimate] | warehouse-native позиционирование, меньше data copy, сильнее тезис "не меняем стек, а повышаем отдачу DWH" |
| **Retail Rocket** | сильный retail/e-commerce brand, известен по recommendations и personalization [T10] | уже заточен под retail, слабее как универсальный decisioning layer | **8-15% e-commerce personalization subsegment** [estimate] | шире сценарии, не только recommendations, а full lifecycle decisioning |
| **Altcraft Platform** | локальный enterprise automation/CDP с упором на data control [T11] | слабее AI narrative и category proof, продукт воспринимается как automation stack | **5-10% локального automation/CDP сегмента** [estimate] | более value-dense wedge с акцентом на uplift и эксперименты |
| **Carrot quest** | известность в автоматизации коммуникаций, относительно быстрый запуск [T12] | слабый fit для enterprise DWH-native motion, ниже потолок по ACV | **3-6% mid-market automation сегмента** [estimate] | лучше fit для data-mature enterprise, где buyer платит за decisioning, а не за чат-маркетинг |

#### Вывод по конкурентному полю
- На Западе категория уже валидирована, но лидеры сильны и имеют огромный connector / distribution advantage.
- В РФ рынок скорее занят **сильными substitutes**, а не прямыми копиями Hilbert.
- Поэтому defendable wedge один, **decisioning поверх существующего DWH/CRM-контура с измеримым uplift и локальным compliance**.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Services creep во внедрении | high | high | onboarding >10 недель, >40% команды занято кастомными интеграциями | шаблоны rollout, paid onboarding, жёсткий scope control |
| Operational | Сложно нанять сильного ML / solutions architect вовремя | med | high | вакансии висят >90 дней, founder закрывает delivery personally | advisor bench, contractors, сужение ICP |
| Operational | Рост стоимости LLM / infra | med | med | inference cost per client растёт >20% QoQ | multi-model routing, cost caps, fallback на rules |
| Market | Спрос остаётся нишевым, buyer education слишком дорог | med | high | <8 SQL за квартал despite outbound | продавать через конкретные ROI use cases, а не через новую категорию |
| Market | Build-in-house у крупных data teams | high | high | в discovery часто звучит "сделаем сами" | продавать time-to-value, connectors, experiment ops и governance |
| Market | Mindbox и локальные CDP давят bundle price | high | high | discount >20%, проигрыши из-за suite pricing | narrow premium ICP, value-based pricing, ROI calculator |
| Regulatory | 152-ФЗ / data residency блокируют cloud delivery | high | high | security review >8 недель, требование on-prem/VPC | RU hosting, VPC/on-prem option, минимизация data export |
| Regulatory | Санкции бьют по западным SaaS / API / billing | high | high | vendor access issues, проблемы с оплатой и интеграциями | локальный стек, vendor redundancy, backup providers |
| Financial | Runway сжимается до <9 мес до выхода на 20+ клиентов | high | high | закрытий <1-2 логотипов/мес, burn выше плана | freeze hiring, cut spend, focus only on high-conviction ICP |
| Financial | Нет IT-льготы, налоги и cash conversion хуже ожидаемого | med | med | компания не проходит аккредитацию, net margin падает | заранее проектировать юрструктуру под аккредитацию |
| Black swan | Ключевой LLM/API vendor становится недоступен | med | high | длительный outage / ban / payment failure | резервные модели, локальный inference слой |
| Black swan | Военная или политическая эскалация режет enterprise IT spend | med | high | заморозка тендеров, перенос пилотов | фокус на cost-saving use cases и cash preservation mode |

### B5. Kill conditions на 6-й месяц

1. **Median-case не собирается:** если обновлённый p50 показывает **EBITDA < 500 000 ₽/мес на горизонте M24**, кейс нужно закрывать.
2. **Pipeline не конвертится:** если к концу M6 нет хотя бы **2 paid pilot / 1 полноценно платящего enterprise логотипа**, enterprise motion не оправдан.
3. **Economics деградирует:** если фактический blended **CAC > 1,5 млн ₽**, payback >6 месяцев по contribution или ARPU падает **ниже 400k ₽/мес**, кейс перестаёт быть software-like.

### B6. Bottom line Section B
- Кейс остаётся **живым**, но только как premium enterprise wedge для data-mature B2C-команд.
- Главный риск не в отсутствии рынка, а в том, что **variance велика**, а substitutes и build-in-house очень сильны.
- Поэтому итог, **conditional continue with hard kill triggers**, а не чистый approve.

## Источники SECTION B
- [T1] `04-economics.md` этого кейса.
- [T2] `04-economics.md`, таблица CAC и funnel assumptions.
- [T3] `04-economics.md`, churn benchmark и sensitivity logic.
- [T4] `02-demand.md`, локальные price anchors и buyer budget.
- [T5] Hightouch AI Decisioning overview: https://hightouch.com/docs/ai-decisioning/overview
- [T6] a16z, Investing in Hilbert, accessed 2026-04-24: https://a16z.com/announcement/investing-in-hilbert/
- [T7] Braze product: https://www.braze.com/product/customer-engagement-platform
- [T8] Simon Data platform: https://www.simondata.com/platform
- [T9] Mindbox tariffs: https://mindbox.ru/tariffs/
- [T10] Retail Rocket company materials: https://retailrocket.net/
- [T11] Altcraft product: https://altcraft.com/
- [T12] Carrot quest company site: https://www.carrotquest.io/

<!-- P6B-DONE -->

## Стадия 6. Verdict
[GEO-EXPAND] 2059 MSK Hilbert GEO Expand v2 — REJECTED: 62/100 | EBITDA base=1 020К₽/мес через 16 мес | LTV/CAC=17,0x | Ключевое преимущество: сильная economics у enterprise decisioning overlay | Главный риск: weak moat и недоказанный repeatable спрос в РФ.

# 06-verdict

sector: GEO-EXPAND

## Итоговый вердикт
- Verdict: REJECTED
- Score: 62/100
- Raw score sum: 93/150
- Нормализация: round(93 × 100 / 150) = 62
- Комитет: кейс проходит economics-gate, но не проходит investment committee gate из-за слабой доказанности спроса, слабого moat и хрупкого premium GTM.

## Delta vs previous
- Предыдущий близкий verdict по теме: `2327-msk-hilbert-geo-expand-v2` = **63/100**, REJECTED.
- Текущий rerun: **62/100**, REJECTED.
- Delta: **-1 балл**.
- Что ухудшило оценку: обязательный tier-awareness penalty по спросу, более жёсткая оценка moat, явная фиксация риска evidence_quality_unverified.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | `LTV/CAC = 17,0x`, `Payback по gross profit = 2,9 месяца`, `Contribution Margin = 62,2%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | `500k+ EBITDA/мес... около 29 клиентов`, `операционный break-even наступает около M16`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 12 | `Composite demand: LOW`, `Demand score: 0`, но `SAM = 1,35 млрд ₽/год`; применён штраф за отсутствие строки Sources. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | `buyer уже может закрывать часть боли через CDP / CRM / performance stack`, значит moat пока слабый. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | `до break-even нужно примерно 60 млн ₽`, `services creep во внедрении` и `152-ФЗ / data residency` остаются существенными. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `fully-loaded CAC = 823 333 ₽`, ICP узкий, но понятный; named targets можно собрать по data-mature B2C сегментам РФ. |

**Normalized score = round((93 × 100) / 150) = 62/100.**

## Почему не approve
1. Economics сильнее, чем итоговый score, но инвестиционное решение ломается на спросе и moat.
2. Exact RU-demand остаётся LOW, buyer не покупает категорию под её собственным названием.
3. Продукт пока выглядит как premium overlay над уже купленными CRM/CDP/data-стеками, а не как новый must-have system of record.
4. Weak moat + высокий capital burn до break-even = слишком хрупкий профиль для approve.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 13 995 000 ₽ |
| CAC fully-loaded | 823 000 ₽ |
| LTV/CAC | 17,0x |
| CAC payback по выручке | 1,8 мес |
| CAC payback по contribution | 2,9 мес |
| GM / contribution margin | 62,2% |
| contribution_margin_rub_month | 280 000 ₽ |
| fixed_costs_rub_month | 7 100 000 ₽ |
| company_ebitda_rub_month @ 27 клиентов | 460 000 ₽/мес |
| company_ebitda_potential_rub_month @ 29 клиентов | 1 020 000 ₽/мес |
| company_ebitda_rub_month @ 50 клиентов | 6 900 000 ₽/мес |
| clients_to_500k_ebitda | 29 |
| clients_to_1m_ebitda | 29 |
| months_to_500k_ebitda | 16 |
| startup_capital_to_bep_rub | 64 500 000 ₽ |
| break-even clients | 27 |

## Полный бизнес-процесс
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов и enrichment | SDR + founder | HH/рынок, CRM, enrichment stack | 6 ч | 55 000 | средняя |
| 2 | Outbound sequence, письма, follow-up | SDR | CRM, sequencer, email | 2-3 недели | 95 000 | высокая |
| 3 | Первичный квалифицирующий созвон | SDR + founder | Meet, CRM | 1 ч + prep | 70 000 | средняя |
| 4 | Discovery с buyer и data owner | Founder/AE | Meet, Miro, CRM | 1-2 недели | 85 000 | низкая |
| 5 | Demo + use-case workshop | Founder + CTO | Demo env, slides, BI | 1 неделя | 110 000 | низкая |
| 6 | Pilot scoping, ROI-кейс, техоценка | Founder + CTO + backend/ML | Docs, SQL, sandbox | 2 недели | 150 000 | низкая |
| 7 | Security / legal / procurement review | Founder + CTO + legal | DPA, SLA, security docs | 2-4 недели | 120 000 | низкая |
| 8 | Коммерческие переговоры и закрытие | Founder + AE | CRM, CPQ, docs | 1 неделя | 70 000 | средняя |
| 9 | Onboarding: mapping, интеграции, first agent setup | CTO + backend + ML + CSM | DWH, ETL, product | 4-6 недель | 160 000 | низкая |
| 10 | Счёт, ЭДО, первый платёж | Finance ops | ЭДО, банк, billing | 2-3 дня | 10 000 | высокая |

## Команда
| Роль | Функция | Fully-loaded FOT, ₽/мес |
|---|---|---:|
| CEO / Founder | sales, fundraising, product narrative, key accounts | 845 000 |
| CTO / Tech Lead | architecture, security, delivery quality | 715 000 |
| Senior Backend #1 | data pipelines, product backend | 585 000 |
| Senior Backend #2 | connectors, activation, infra logic | 585 000 |
| ML Engineer | decisioning, modeling, experimentation | 650 000 |
| DevOps | infra, CI/CD, reliability, cost control | 455 000 |
| Frontend | UI, analyst console, reporting | 390 000 |
| SDR | outbound pipeline generation | 195 000 |
| AE | discovery, proposal, close | 455 000 |
| Customer Success | onboarding, QBR, retention | 325 000 |
| **Итого** |  | **5 200 000** |

## 7-factor Moat Framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 1 | Есть интеграции и модель decision loops, но замена теоретически возможна на in-house или suite. |
| Scale economies | 1 | Infra/COGS улучшаются с объёмом, но не радикально. |
| Proprietary data / model advantage | 1 | Собственные клиентские данные есть, но публично не доказан уникальный датасет уровня moat. |
| Regulatory moat | 0 | Регуляторный барьер скорее мешает, чем защищает. |
| Brand / distribution | 2 | Есть сигнал от a16z и category narrative, но в РФ бренд не укоренён. |
| Embedded workflow | 2 | При удачном rollout слой реально садится в CRM/growth workflow клиента. |
| **Итого** | **7/21** | **Moat score = round((7 × 25) / 21) = 8/25** |

**Вывод по moat:** weak moat. Обязательно фиксируется в Top-3 Risks.

## GTM: 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Ozon | Большой e-commerce, loyalty и retention-механики, зрелый data stack и персонализация. | email decision-maker + конференции eCom | 650 000 ₽/мес |
| 2 | Wildberries | Огромный consumer traffic, промо и CRM-циклы, высокий потенциал uplift через decisioning. | партнёрство с martech-integrator + direct outreach | 650 000 ₽/мес |
| 3 | Яндекс Маркет | Data-mature marketplace с множеством каналов и promo-решений. | direct email head of CRM / growth | 600 000 ₽/мес |
| 4 | Самокат | Частые повторные покупки, churn/reactivation critical, сильная потребность в next-best-action. | direct outreach + профильные product/data events | 500 000 ₽/мес |
| 5 | Купер | Grocery-delivery retention и frequency control хорошо соответствуют product wedge. | email VP marketing / CRM lead | 450 000 ₽/мес |
| 6 | T-Банк | Lifecycle marketing, event-rich customer base и зрелая data-команда. | warm intro через martech/data community | 600 000 ₽/мес |
| 7 | МТС | Массовая CRM-машина, много сегментов и частые decisioning-задачи по каналам и офферам. | конференция + enterprise account-based outreach | 550 000 ₽/мес |
| 8 | МегаФон | Сильный telecom CRM, upsell/cross-sell и retention pain совпадают с use cases кейса. | email decision-maker + партнёрство с интегратором | 500 000 ₽/мес |
| 9 | OneTwoTrip | Travel CRM чувствителен к reactivation и персонализированным офферам. | direct outreach head of CRM | 400 000 ₽/мес |
| 10 | Okko | Подписка, удержание и monetization сценарии требуют быстрого decisioning по аудиториям. | email CMO / growth lead | 400 000 ₽/мес |

## Top-3 Risks
| Риск | Probability | Impact | Почему это в топ-3 |
|---|---|---|---|
| Weak moat / price compression against substitutes | high | high | Buyer уже может закрывать боль через Mindbox, Hightouch-подобный стек или in-house команду. |
| evidence_quality_unverified | high | medium | В `02-demand.md` нет строки `Sources: T1=..., T2=..., T3=...`, поэтому criterion #3 штрафуется автоматически. |
| Services creep и длинный enterprise rollout | high | high | `onboarding 4-6 недель`, `до break-even нужно примерно 60 млн ₽`, значит delivery может съесть software-like margin. |

## Финансовые proof points
- `LTV/CAC = 17,0x` и `CAC Payback по gross profit = 2,9 месяца` подтверждают, что проблема не в unit economics на уровне клиента.
- `company_ebitda_potential_rub_month = 1 020 000 ₽/мес` при 29 клиентах за ~16 месяцев означает формальный PASS по EBITDA-gate.
- Но p10 Monte Carlo даёт `EBITDA @M24 = -1 420 000 ₽/мес`, поэтому downside остаётся слишком тяжёлым для approve.

## LTV Upside Calculator
Так как кейс REJECTED, считаем что должно улучшиться до near-pass/approve.

### Вариант A: улучшить demand + GTM, не трогая продукт
- текущий score: 62/100
- если добавить верифицированные T1/T2-источники, снять штраф по criterion #3 и поднять Market+Demand с 12 до 17, общий score станет **65/100**
- если дополнительно доказать 2-3 pilot-to-rollout кейса и поднять GTM с 20 до 22, score станет **67/100**

### Вариант B: улучшить moat
- если показать proprietary dataset / benchmark advantage и поднять moat с 8 до 14, score станет **68/100**

### Вариант C: путь к approve
- Market+Demand: 17/25
- Moat: 14/25
- Execution Risk: 18/25
- тогда raw sum = 108, normalized = **72/100**, то есть APPROVED с notes

## Что нужно доказать для пересмотра
1. 2-3 реальных pilot-to-rollout кейса в data-mature B2C аккаунтах РФ или соседнего контура.
2. Источники спроса по tier-system: минимум одна явная строка `Sources: T1, T2, T3` и сильнее, чем текущий LOW exact-demand.
3. Доказательство moat: proprietary benchmark, integration depth, measurable uplift, который труднее повторить в Mindbox или in-house.
4. Стандартизированный onboarding, чтобы delivery не превращался в консалтинг.

## Финальный вывод инвесткомитета
Hilbert-подобный growth decisioning слой выглядит сильным на уровне математики клиента и даже проходит EBITDA-gate компании, но для approve этого недостаточно. На текущем массиве evidence кейс остаётся **REJECTED: 62/100**. Это не economics fail, а **market/moat fail**.

