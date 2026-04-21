# 2327-msk-hilbert-geo-expand-v2
Статус: REJECTED  
Score: 63/100  
Сектор: GEO-EXPAND  
Дата: 2026-04-21

---

## 00-brief.md

# 00-brief

## Кейс
2327-msk-hilbert-geo-expand-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
2327-msk-hilbert-geo-expand

## Краткое описание
Hilbert: warehouse-native AI decisioning и growth intelligence для B2C-команд. Ранее сигнал закрывался как duplicate отклонённого кейса, но resurrect-режим обязывает прогнать его заново как standalone candidate.

## Что делать дальше
Пройти полный пайплайн P3→P7 с новой аналитикой и в финальном verdict отдельно сравнить standalone-оценку с историческим решением по этой теме.

---

## 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-2327-msk-hilbert-geo-expand.md
created: 2026-04-20T03:49:00+03:00
---

# 01-intake

## Кейс
2327-msk-hilbert-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-17-2327-msk-hilbert-geo-expand-duplicate.md

## Краткий контекст
Hilbert: warehouse-native AI decisioning и growth intelligence для B2C-команд. Ранее сигнал закрывался как duplicate отклонённого кейса, но resurrect-режим обязывает прогнать его заново как standalone candidate.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — 2327-msk-hilbert-geo-expand

## Meta
- source: triage/triage-2026-04-17-2327-msk-hilbert-geo-expand-duplicate.md
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
- `pipeline/raw/raw-2026-04-17-2327-msk-hilbert-geo-expand.md`

## Классификация
Дубликат ранее обработанного сигнала.

## Решение
Новый кейс не создавался и открытый кейс в `pipeline/cases/` не обогащался.

## Почему это дубликат
- Сигнал совпадает по компании, категории и сути гипотезы с уже обработанными Hilbert GEO-EXPAND сигналами.
- По этой теме уже существует оформленный кейс `warehouse-native-ai-decisioning-marketing-operator`, который был ранее рассмотрен и затем отклонён.
- Во входном файле нет materially new данных, которые меняют оценку спроса, LTV или защищаемости гипотезы.

## Почему не было обогащения кейса
- В `pipeline/cases/` нет открытого кейса по теме warehouse-native AI decisioning для growth и marketing команд.
- Требование на добавление supporting signal применяется только к существующим открытым кейсам в `pipeline/cases/`, а здесь релевантный кейс находится в `pipeline/rejected/`.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/raw-2026-04-17-2327-msk-hilbert-geo-expand.md`.

## Вердикт
Сигнал закрыт как дубликат уже обработанной и отклонённой гипотезы по AI-native growth decisioning для B2C-команд.

```
---

## 02-validation.md

Файл отсутствует в кейсе.

---

## 02-demand.md

---
stage: demand-validation
case: 2327-msk-hilbert-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
2327 MSK Hilbert GEO Expand, AI-native growth infrastructure для B2C-команд: warehouse-native decisioning, growth intelligence, прогнозирование поведения, агентное исполнение retention/acquisition/monetization сценариев.

## Итог
**Статус: CONDITIONAL PASS**

По точному RU-спросу картина слабая. Demand API по `warehouse native ai decisioning marketing` вернул **LOW** и `demand_score=0`, а смежные запросы `marketing decision engine` и `growth intelligence platform` тоже остались в зоне **LOW**. Это означает, что в России категория почти точно не покупается по exact label Hilbert.

Но при этом money layer у категории существует. По состоянию на **15 апреля 2026 года** Hilbert закрыла **$28 млн Series A** под тезис AI-native growth infra для consumer companies, а a16z в своей инвестиционной заметке прямо описывает проблему как дорогой и дефицитный слой growth data plumbing. На собственном сайте Hilbert уже продаёт не BI, а связку detect → reason → act → optimize для acquisition, retention и monetization. Параллельно Hightouch публично продаёт **AI Decisioning** как отдельный enterprise-продукт, а Mindbox показывает, что в РФ уже есть платёжеспособный бюджет на CDP, персонализацию и оптимизацию маркетинга, с публичными тарифами **от 150 000 ₽/мес** и **от 400 000 ₽/мес**.

Вывод: exact keyword demand слабый, но adjacent enterprise spend подтверждён и глобально, и локально. Поэтому кейс можно пропускать дальше, однако только условно: в P4-P6 нужно жёстко проверить, защищается ли premium wedge Hilbert поверх локальных substitutes и не превращается ли продукт в тяжёлый semi-service слой.

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

Это ослабляет силу keyword-demand, но не убивает кейс, если есть подтверждённый бюджет в adjacent category.

## 2. Реальные рыночные сигналы и why now
1. **15 апреля 2026 года** a16z объявила об инвестиции в Hilbert и описала pain как сложный слой growth data plumbing, который дорого строить и трудно поддерживать внутри компании.
2. В тот же день Hilbert получила публичный funding signal на **$28 млн Series A**, что подтверждает инвесторскую ставку на отдельную категорию AI-native growth infrastructure для consumer companies.
3. На сайте Hilbert продукт уже продаётся как целостная growth infra, а не просто аналитический dashboard: Detect, Reason, Act, Optimize, плюс claims про запуск после ingestion и переход от decision cycles в месяцы к минутам.
4. Hightouch публично выделяет **AI Decisioning** в отдельный продукт и в документации описывает его как систему автоматизации индивидуальных маркетинговых решений на уровне сообщения, канала и времени отправки.
5. Это усиливает why now: рынок смещается от ручных кампаний и rule-based orchestration к reinforcement-learning / agentic decisioning поверх data warehouse.

### Вывод
Глобально категория коммерчески валидируется. Hilbert не выглядит research-only историей: есть свежий funding event, чёткий buyer narrative и зрелые adjacent vendors, которые продают близкий decisioning слой.

## 3. Конкурентные и ценностные якоря

| Якорь | Публичный сигнал | Что это доказывает |
|---|---|---|
| Hilbert | AI-native growth infrastructure, Detect/Reason/Act/Optimize, фокус на B2C growth | продукт продаётся как операционный слой, а не как консультация |
| a16z | публичная инвестиция в Hilbert от 15.04.2026 | проблема достаточно велика и инвестиционно понятна |
| Hightouch AI Decisioning | отдельный продукт и отдельный pricing layer | category уже монетизируется как enterprise software |
| Mindbox | публичные тарифы от 150k/400k ₽ в месяц | в РФ уже существует бюджет на персонализацию и data-driven marketing |

### Вывод по конкурентному полю
Слой decisioning и personalization monetization реален. Но buyer уже может закрывать часть боли через CDP/CRM/performance stack без покупки нового дорогого growth infra. Значит Hilbert-подобный продукт должен продаваться как measurable uplift layer, а не как очередной data tool.

## 4. Российский контур и кто реально может купить
Реальный ICP в локальном контуре, это не весь рынок, а только компании, у которых уже есть:
- зрелый data warehouse или хотя бы сильный event/data stack,
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
8. betting/gaming/entertainment с сильным retention motion.

### Вывод
Локальный рынок не массовый, но и не микроскопический. Это узкий слой data-mature B2C-компаний с понятным экономическим стимулом к growth optimization.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру **450 000 ₽/мес** как base enterprise чек, или **5,4 млн ₽/год** на клиента. Это выше lower-end substitutes, но сопоставимо с локальным enterprise software budget, если продукт реально влияет на LTV, retention и budget allocation.

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

### Вывод по рынку
Это не universal SaaS, а узкий enterprise growth layer. Но даже при консервативной рамке SAM остаётся выше **1 млрд ₽/год**, а ранний SOM даёт meaningful revenue base.

## 6. WTP и доказательства готовности платить
1. Hilbert получила funding не как generic analytics tool, а как AI-native growth infra. Это косвенное, но сильное подтверждение, что рынок верит в большой бюджетный слой.
2. Hightouch уже монетизирует AI Decisioning как отдельный продукт, значит willingness to pay за decisioning layer не теоретический.
3. Mindbox показывает, что локальные buyers уже привыкли платить заметные суммы за CDP, персонализацию и маркетинговую оптимизацию.
4. Но локально пока **не доказано**, что buyer готов массово платить именно за более тяжёлый warehouse-native / agentic growth infra слой с premium выше CDP и CRM automation substitutes.

### Вывод по WTP
**WTP подтверждён, но premium positioning пока подтверждён ограниченно.**

Именно поэтому verdict здесь CONDITIONAL PASS, а не clean PASS.

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

### Интерпретация
Математика Profit Gate сходится. Главная неизвестность не в unit economics на бумаге, а в том, можно ли реально удержать premium-чек поверх Mindbox-класса substitutes без тяжёлой кастомной аналитической команды в delivery.

## 8. Общий вывод
- Exact search demand: **LOW**
- Global category proof: **есть и усилился свежим раундом Hilbert**
- Adjacent enterprise budget: **подтверждён**
- Локальные substitutes: **сильные**
- WTP: **есть, но premium wedge ещё надо доказать**
- Profit Gate: **проходит**

## 9. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс стоит двигать дальше в economics, потому что:
1. global category proof заметно усилился свежим funding signal от **15 апреля 2026 года**;
2. category money layer существует и у Hilbert-like vendors, и у локальных substitutes;
3. Profit Gate проходит в нескольких конфигурациях.

Но в P4-P6 нужно особенно жёстко проверить:
- реально ли защищается premium против CDP/CRM substitutes,
- сколько скрытого services load в onboarding и аналитике,
- насколько repeatable обещание «decision cycles from months to minutes»,
- не является ли Hilbert по факту дорогим overlay для already-mature data teams.

## Market Pulse
Market Pulse 20.04.2026: осторожно позитивный.

Свежий раунд Hilbert резко усилил сигнал по global category validation, но локальная покупаемость всё ещё выглядит больше budget-transfer story, чем exact-demand story.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=warehouse%20native%20ai%20decisioning%20marketing
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=marketing%20decision%20engine
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=growth%20intelligence%20platform
- Hilbert homepage: https://hilberts.ai/
- Hilbert startup program: https://hilberts.ai/startup-program
- a16z, Investing in Hilbert, 2026-04-15: https://a16z.com/announcement/investing-in-hilbert/
- Hightouch pricing: https://hightouch.com/pricing/
- Hightouch AI Decisioning docs: https://hightouch.com/docs/ai-decisioning/overview
- Mindbox tariffs: https://mindbox.ru/tariffs/

---

## 03-demand.md

Файл отсутствует в кейсе.

---

## 04-economics.md

---
stage: economics
case: 2327-msk-hilbert-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
verdict: PASS_WITH_CONSTRAINTS
confidence: medium
investment_grade: false
sector: GEO-EXPAND
---

# 04-economics — Unit Economics

## Кейс
2327-msk-hilbert-geo-expand-v2, warehouse-native AI decisioning и growth intelligence для data-mature B2C-команд с локализацией под РФ.

## Executive summary

**Итог P4: PASS WITH CONSTRAINTS.**

Экономика может сойтись только как узкий enterprise growth-infra motion, где продукт продаётся не как ещё один CDP/BI-инструмент, а как слой `decisioning + experimentation + orchestration + measurable uplift`.

Ключевые выводы:
1. **Low-end сценарий не работает**: при чеке 180–250 тыс. ₽/мес кейс быстро превращается в дорогой overlay над существующим data stack и не дотягивает до устойчивой EBITDA.
2. **Base enterprise сценарий проходит**: при среднем recurring-контракте около **420 тыс. ₽/мес** и умеренно productized delivery компания может выйти на **EBITDA > 500 тыс. ₽/мес**.
3. **Главный риск не в спросе, а в hidden services load**: discovery, data mapping, feature/event hygiene, integration с CRM/CDP/warehouse и постоянная аналитическая настройка могут быстро съесть маржу.
4. **Investment grade пока нет**: LTV/CAC выглядит рабочим, но локальный PMF не доказан, а конкурентное давление со стороны Mindbox/Hightouch-класса substitutes остаётся высоким.

## 1. Модель и ключевые допущения

### ICP
- крупный e-commerce;
- grocery delivery;
- travel / ticketing;
- fintech с развитым lifecycle marketing;
- subscription и media-сервисы;
- marketplace / classified-платформы;
- betting / gaming / entertainment с сильным retention motion.

### Base-case для РФ
- Средний recurring-контракт: **420 000 ₽/клиент/мес**
- Разовый setup / implementation fee: **650 000 ₽**
- Setup fee использую как cash support, но **не включаю в MRR**.
- Модель предполагает продажу в data-mature компании, где уже есть warehouse, CRM / CDP и growth-команда.

### Почему беру 420k ₽ MRR
В `02-demand.md` уже зафиксировано, что локальные substitutes вроде Mindbox закрывают часть боли по тарифам **от 150k ₽/мес** и **от 400k ₽/мес**. Значит Hilbert-подобный слой имеет смысл только если:
- продаётся выше mid-market automation layer,
- приносит measurable uplift по retention / monetization,
- и не требует слишком тяжёлой кастомной аналитической команды.

Чек ниже **300k ₽/мес** делает модель слишком хрупкой. Чек выше **600k ₽/мес** пока не подтверждён локальным PMF.

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP mapping по B2C accounts | SDR / analyst | CRM, Rusprofile, manual research | 2 ч | 2 200 | Низкий |
| 2 | Первичный outreach | SDR | Email, Telegram, phone | 1.5 ч | 1 700 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 200 | Средний |
| 4 | Discovery по data stack и growth process | AE + founder | Workshop, questionnaire | 2.5 ч | 11 000 | Низкий |
| 5 | Tech / data feasibility review | Solutions engineer | Warehouse map, event audit | 3 ч | 13 500 | Низкий |
| 6 | Demo и ROI narrative | AE + solutions | Demo env, сценарии uplift | 2 ч | 9 500 | Низкий |
| 7 | Pilot scoping и KPI definition | AE + CSM | SOW, KPI model | 3 ч | 13 000 | Низкий |
| 8 | Integration / onboarding | Solutions + CSM | CDP/CRM connectors, runbooks | 14 ч | 49 000 | Средний |
| 9 | Pilot 4–6 недель | CSM + analyst | dashboards, support | 12 ч | 36 000 | Средний |
| 10 | Security / procurement / legal | AE + founder + ops | contract workflow | 7 ч | 22 000 | Низкий |
| 11 | Commercial proposal / negotiation | AE + founder | pricing calculator, CRM | 4 ч | 16 000 | Низкий |
| 12 | Production rollout после оплаты | CSM + solutions | playbooks, monitoring | 8 ч | 27 000 | Средний |

### Вывод по процессу
Продажа выглядит как **consultative enterprise sale**. Нельзя считать кейс лёгким SaaS: до оплаты много ручного труда, а после оплаты остаётся существенный implementation load.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / inference / scoring budget | 24 000 | постоянные decisioning workflows |
| Hosting / storage / logs | 18 000 | изолированная среда, вычисления, audit |
| Data / reverse ETL / integration support | 22 000 | коннекторы, data movement, troubleshooting |
| Customer success / account ops | 28 000 | доля CSM на активный аккаунт |
| Solutions / analytics support | 26 000 | настройка decision logic, QA, uplift review |
| Implementation amortization | 20 000 | spread setup effort over 12 мес |
| Security / compliance allocation | 9 000 | правовой и процессный overhead |
| **Итого COGS** | **147 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **420 000 ₽**
- COGS на клиента: **147 000 ₽**
- Gross profit на клиента: **273 000 ₽**
- **Gross Margin = 65.0%**

### Комментарий
На бумаге маржа выглядит хорошей, но она держится только если analytics/support не превращается в постоянный quasi-consulting слой. Это и есть центральный риск кейса.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 18 | 7 | 4 | 2 | 0.8 | 4.4% |
| Targeted outbound | 110 | 16 | 7 | 3 | 0.7 | 0.64% |
| Content / inbound / events | 35 | 8 | 4 | 2 | 0.4 | 1.1% |
| Partners / agencies / data stack ecosystem | 14 | 5 | 3 | 1 | 0.3 | 2.1% |
| **Итого blended** | **177** | **36** | **18** | **8** | **2.2** | **1.2%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid acquisition / category capture | 160 000 | ограниченные тесты по enterprise demand |
| SDR + AE FOT attributed to new | 1 020 000 | 2 SDR + 1 AE + взносы + commissions |
| Marketing allocation | 220 000 | контент, кейсы, ивенты |
| CRM / sequencing / tooling | 110 000 | CRM, enrichment, outreach tools |
| Events / partnerships | 180 000 | профильные конференции, партнёры |
| Overhead multiplier (x1.3) | 507 000 | management / admin / ops overhead |
| **Итого fully-loaded acquisition spend** | **2 197 000** |  |

- New paying customers / мес: **2.2**
- **Blended fully-loaded CAC = 998 636 ₽**

### Sanity check
Для consultative enterprise SaaS в РФ CAC около **1,0 млн ₽** не выглядит заниженным. Ниже **400k ₽** для такого data-heavy motion было бы неправдоподобно.

## 5. LTV и churn

### Базовые допущения
- MRR на клиента: **420 000 ₽**
- ARR на клиента: **5 040 000 ₽**
- Gross Margin: **65%**
- Annual logo churn: **18%**

Формула:

`LTV = ARR × GM / churn`

`LTV = 5 040 000 × 65% / 18% = 18 200 000 ₽`

### Вывод
- **LTV = 18,2 млн ₽**
- Значение сильное, но чувствительно к churn. Если продукт не удерживает доказуемый uplift, клиенты могут откатываться обратно к rule-based stack или локальным substitutes.

## 6. LTV / CAC

- LTV: **18 200 000 ₽**
- Fully-loaded CAC: **998 636 ₽**

`LTV/CAC = 18 200 000 / 998 636 = 18.2x`

### Stress-case
Чтобы не переоценить кейс, считаю также stress-case:
- Effective GM в Year 1: **52%**
- Annual churn: **30%**

`Stress LTV = 5 040 000 × 52% / 30% = 8 736 000 ₽`

`Stress LTV/CAC = 8 736 000 / 998 636 = 8.7x`

### Вердикт по метрике
Даже в stress-case LTV/CAC остаётся выше порога **3:1**. Значит главная проблема кейса не в формальной окупаемости CAC, а в том, насколько repeatable этот GTM и не вырастет ли скрытый service load.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`998 636 / 420 000 = 2.38 мес`

Если считать payback по gross profit:

`998 636 / 273 000 = 3.66 мес`

### Комментарий
Показатель выглядит очень сильным, но это следствие enterprise-чека. На практике реальный cash payback будет длиннее из-за пилотного периода и отсрочек по procurement.

## 8. Contribution Margin %

Для contribution margin беру выручку минус COGS минус variable commission / success load.

- Revenue per client / мес: **420 000 ₽**
- COGS: **147 000 ₽**
- Variable commission + success allocation: **22 000 ₽**

`Contribution profit = 251 000 ₽`

`Contribution Margin = 251 000 / 420 000 = 59.8%`

### Вывод
**Contribution Margin = 59.8%**. Это хороший показатель, если delivery реально productized. Если каждое внедрение потребует много ручного анализа, margin быстро деградирует.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / tech lead | 1 | 520 000 | 2 | 2 | 156 000 | 676 000 |
| Backend / data engineer | 2 | 400 000 | 1.5 | 1.5 | 120 000 | 1 040 000 |
| ML / applied AI engineer | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Solutions engineer | 1 | 360 000 | 1.5 | 1.5 | 108 000 | 468 000 |
| Product / analytics lead | 1 | 340 000 | 1.5 | 1.5 | 102 000 | 442 000 |
| SDR | 2 | 155 000 + бонус | 1 | 1 | 46 500 | 403 000 |
| AE | 1 | 300 000 + комиссия | 1.5 | 2 | 90 000 | 390 000 |
| CSM / implementation | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Finance / ops (part-time) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого full team FOT** | **11.5** |  |  |  |  | **5 252 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 5 252 000 |
| Core infra not in COGS | 260 000 |
| Security / legal / data governance | 180 000 |
| G&A / бухгалтерия / ЭДО / misc | 100 000 |
| Travel / enterprise meetings | 110 000 |
| Office / admin | 130 000 |
| **Итого fixed costs** | **6 032 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **251 000 ₽**
- Fixed costs: **6 032 000 ₽/мес**

`Break-even clients = 6 032 000 / 251 000 = 24.0`

### Lean founder-mode
Если первые 12 месяцев держать компактную команду и fixed costs около **4 200 000 ₽/мес**, тогда:

`4 200 000 / 251 000 = 16.7 клиента`

### Вывод
- На **полной команде** break-even достигается примерно на **24 клиентах**.
- В **lean-mode** порог снижается до **17 клиентов**.
- Для узкого B2C enterprise-слоя это достижимо, но не легко. Ошибка в positioning или слабый onboarding быстро ломают модель.

## 12. Burn-to-breakeven и runway

### Burn base-case
- Fixed costs lean-mode: **4.20 млн ₽/мес**
- Acquisition spend: **2.20 млн ₽/мес**
- Total early burn: **~6.40 млн ₽/мес**

### Burn-to-breakeven
Если компания выходит на **17–24 клиентов** за 15–24 месяца, ориентир burn-to-breakeven будет **55–85 млн ₽** в зависимости от темпа найма и conversion из pilot в paid rollout.

### Runway
При `startup_capital = 90 млн ₽`:

`90 000 000 / 6 400 000 ≈ 14.1 мес`

С учётом нарастающей выручки реалистичный runway: **15–17 месяцев**.

## 13. Что происходит при 30 клиентах

### P&L snapshot при 30 клиентах
- Revenue: `30 × 420 000 = 12 600 000 ₽/мес`
- COGS: `30 × 147 000 = 4 410 000 ₽/мес`
- Gross profit: **8 190 000 ₽/мес**
- Variable commission / success: `30 × 22 000 = 660 000 ₽/мес`
- Contribution profit: **7 530 000 ₽/мес**

Если fixed costs держатся в lean-mode **4.20 млн ₽**, тогда:
- **EBITDA ≈ 3.33 млн ₽/мес**

Если fixed costs на полной команде **6.03 млн ₽**, тогда:
- **EBITDA ≈ 1.50 млн ₽/мес**

### Ключевой вывод
Profit gate проходит уже на **30 клиентах** даже без экстремально агрессивных допущений. Но это работает только если продукт удерживает enterprise-чек и не сползает в кастомную аналитическую студию.

## 14. Profit Gate

### Проверка правила
Условие FAIL: `company EBITDA < 500K/mo achievable even at 50 clients` или `LTV/CAC < 1:1`

### Факт
- LTV/CAC уверенно выше порога.
- EBITDA **> 500 тыс. ₽/мес достижима** уже заметно раньше 50 клиентов.
- Главный риск находится не в формальной арифметике, а в repeatability GTM и сохранении маржи после локализации.

## Итоговый вердикт P4

**PASS WITH CONSTRAINTS.**

Кейс экономически выглядит рабочим как узкий enterprise growth-infra оператор для data-mature B2C-команд. Но он не является investment-grade на текущей стадии, потому что:
1. local PMF пока не доказан;
2. substitutes сильные и понятные buyer'у;
3. hidden services load может резко ухудшить gross margin и churn;
4. успех критически зависит от способности доказать measurable uplift, а не просто "AI decisioning" narrative.

## Что нужно проверить на следующем этапе
1. Насколько честно можно удерживать чек **420k+ ₽/мес** против Mindbox / CRM / CDP substitutes.
2. Не окажется ли фактический churn выше **25–30%** из-за сложного внедрения и слабого internal adoption.
3. Можно ли productize implementation и analytics support, иначе кейс потеряет enterprise software economics.

## Источники
- `pipeline/cases/2327-msk-hilbert-geo-expand-v2/02-demand.md`
- Hilbert homepage: https://hilberts.ai/
- a16z, Investing in Hilbert, 2026-04-15: https://a16z.com/announcement/investing-in-hilbert/
- Hightouch pricing: https://hightouch.com/pricing/
- Hightouch AI Decisioning docs: https://hightouch.com/docs/ai-decisioning/overview
- Mindbox tariffs: https://mindbox.ru/tariffs/

---

## 05-critic.md

## SECTION A. Finance PnL

### A1. Исходные допущения из 04-economics.md
- ARPA / MRR на клиента: **420 000 ₽/мес**.
- COGS на клиента: **147 000 ₽/мес**.
- Gross profit на клиента: **273 000 ₽/мес**.
- Contribution profit на клиента: **251 000 ₽/мес**.
- Fixed costs: **6 032 000 ₽/мес**.
- Team FOT fully-loaded: **5 252 000 ₽/мес**.
- Variable commission / success allocation: **22 000 ₽/клиент/мес**.
- Blended CAC: **998 636 ₽**.
- LTV: **18 200 000 ₽**.
- Налоги РФ для waterfall: **УСН 6% с выручки**, **IT-льгота 3% с выручки**, **ОСНО 20% на прибыль**; при ОСНО учитывается **НДС 20%** как фактор давления на cash conversion.
- Страховые взносы **~30% к ФОТ** уже включены во fully-loaded FOT и fixed cost base.

### A2. Сценарные допущения
- **Base:** текущий чек 420k ₽, churn **1.5%/мес**, выход на 25+ клиентов около второго года.
- **Optimistic:** чек **450k ₽**, churn **1.0%/мес**, немного ниже service load и fixed cost discipline.
- **Pessimistic:** чек **390k ₽**, churn **2.5%/мес**, выше support load и более тяжёлый fixed cost.
- Setup fee **650k ₽** использую только как дополнительный cash support, **не включаю в MRR/PnL-таблицы**, чтобы не завышать recurring economics.

### A3. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 1.00 | 1.98 | 2.96 | 4.91 | 6.84 | 8.73 | 10.60 | 12.44 | 15.26 | 18.03 | 20.76 | 23.45 |
| MRR, ₽ | 420 000 | 833 700 | 1 241 194 | 2 062 577 | 2 871 638 | 3 668 563 | 4 453 535 | 5 226 732 | 6 408 331 | 7 572 206 | 8 718 623 | 9 847 844 |
| COGS, ₽ | 147 000 | 291 795 | 434 418 | 721 902 | 1 005 073 | 1 283 997 | 1 558 737 | 1 829 356 | 2 242 916 | 2 650 272 | 3 051 518 | 3 446 745 |
| Gross profit, ₽ | 273 000 | 541 905 | 806 776 | 1 340 675 | 1 866 565 | 2 384 566 | 2 894 798 | 3 397 376 | 4 165 415 | 4 921 934 | 5 667 105 | 6 401 098 |
| GM% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% |
| Fixed costs, ₽ | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 | 6 032 000 |
| EBITDA, ₽ | -5 781 000 | -5 533 765 | -5 290 239 | -4 799 365 | -4 315 854 | -3 839 597 | -3 370 483 | -2 908 405 | -2 202 259 | -1 506 705 | -821 585 | -146 741 |
| Cash burn, ₽ | 5 781 000 | 5 533 765 | 5 290 239 | 4 799 365 | 4 315 854 | 3 839 597 | 3 370 483 | 2 908 405 | 2 202 259 | 1 506 705 | 821 585 | 146 741 |
| Cumulative cash, ₽ | 5 781 000 | 11 314 765 | 16 605 004 | 21 404 368 | 25 720 223 | 29 559 820 | 32 930 302 | 35 838 708 | 38 040 967 | 39 547 673 | 40 369 258 | 40 515 999 |

### A4. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 1.00 | 1.99 | 3.97 | 5.93 | 7.87 | 9.79 | 12.69 | 15.57 | 18.41 | 21.23 | 24.02 | 26.78 |
| MRR, ₽ | 450 000 | 895 500 | 1 786 545 | 2 668 680 | 3 541 993 | 4 406 573 | 5 712 507 | 7 005 382 | 8 285 328 | 9 552 475 | 10 806 950 | 12 048 881 |
| COGS, ₽ | 140 000 | 278 600 | 555 814 | 830 256 | 1 101 953 | 1 370 934 | 1 777 224 | 2 179 452 | 2 577 658 | 2 971 881 | 3 362 162 | 3 748 541 |
| Gross profit, ₽ | 310 000 | 616 900 | 1 230 731 | 1 838 424 | 2 440 039 | 3 035 639 | 3 935 283 | 4 825 930 | 5 707 671 | 6 580 594 | 7 444 788 | 8 300 340 |
| GM% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% | 68.9% |
| Fixed costs, ₽ | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 | 5 700 000 |
| EBITDA, ₽ | -5 410 000 | -5 122 900 | -4 548 671 | -3 980 184 | -3 417 382 | -2 860 209 | -2 018 607 | -1 185 420 | -360 566 | 456 039 | 1 264 479 | 2 064 834 |
| Cash burn, ₽ | 5 410 000 | 5 122 900 | 4 548 671 | 3 980 184 | 3 417 382 | 2 860 209 | 2 018 607 | 1 185 420 | 360 566 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 5 410 000 | 10 532 900 | 15 081 571 | 19 061 755 | 22 479 138 | 25 339 346 | 27 357 953 | 28 543 373 | 28 903 940 | 28 903 940 | 28 903 940 | 28 903 940 |

### A5. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 4.76 | 6.64 | 8.47 | 10.26 | 12.00 | 13.70 | 15.36 |
| MRR, ₽ | 0 | 390 000 | 770 250 | 1 140 994 | 1 502 469 | 1 854 907 | 2 588 535 | 3 303 821 | 4 001 226 | 4 681 195 | 5 344 165 | 5 990 561 |
| COGS, ₽ | 0 | 155 000 | 306 125 | 453 472 | 597 135 | 737 207 | 1 028 777 | 1 313 057 | 1 590 231 | 1 860 475 | 2 123 963 | 2 380 864 |
| Gross profit, ₽ | 0 | 235 000 | 464 125 | 687 522 | 905 334 | 1 117 700 | 1 559 758 | 1 990 764 | 2 410 995 | 2 820 720 | 3 220 202 | 3 609 697 |
| GM% | 0.0% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% | 60.3% |
| Fixed costs, ₽ | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 | 6 250 000 |
| EBITDA, ₽ | -6 250 000 | -6 040 000 | -5 835 250 | -5 635 619 | -5 440 978 | -5 251 204 | -4 856 174 | -4 471 019 | -4 095 494 | -3 729 357 | -3 372 373 | -3 024 313 |
| Cash burn, ₽ | 6 250 000 | 6 040 000 | 5 835 250 | 5 635 619 | 5 440 978 | 5 251 204 | 4 856 174 | 4 471 019 | 4 095 494 | 3 729 357 | 3 372 373 | 3 024 313 |
| Cumulative cash, ₽ | 6 250 000 | 12 290 000 | 18 125 250 | 23 760 869 | 29 201 847 | 34 453 051 | 39 309 225 | 43 780 244 | 47 875 738 | 51 605 094 | 54 977 467 | 58 001 780 |

### A6. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
| Scenario | ARPA | Gross profit | Contribution |
|---|---:|---:|---:|
| Base | 420 000 ₽ | 273 000 ₽ | 251 000 ₽ |
| Optimistic | 450 000 ₽ | 310 000 ₽ | 290 000 ₽ |
| Pessimistic | 390 000 ₽ | 235 000 ₽ | 210 000 ₽ |

#### Waterfall на уровне EBITDA break-even
| Scenario | Break-even clients | Revenue | Gross profit | Contribution | EBITDA | Net after tax УСН 6% | Net after tax IT 3% | Net after tax ОСНО 20% |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Base | 24.0 | 10 093 386 ₽ | 6 560 701 ₽ | 6 032 000 ₽ | 0 ₽ | -605 603 ₽ | -302 802 ₽ | 0 ₽ |
| Optimistic | 19.7 | 8 844 828 ₽ | 6 093 103 ₽ | 5 700 000 ₽ | 0 ₽ | -530 690 ₽ | -265 345 ₽ | 0 ₽ |
| Pessimistic | 29.8 | 11 607 143 ₽ | 6 994 048 ₽ | 6 250 000 ₽ | 0 ₽ | -696 429 ₽ | -348 214 ₽ | 0 ₽ |

### A7. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Base | M13 | 40 515 999 ₽ | требуется длиннее 12 месяцев, несмотря на положительный LTV/CAC |
| Optimistic | M10 | 28 903 940 ₽ | точка EBITDA 0 достигается в пределах прогнозного горизонта |
| Pessimistic | M22 | 70 924 339 ₽ | требуется длиннее 12 месяцев, несмотря на положительный LTV/CAC |

### A8. Налоговая модель РФ
- **УСН 6%** удобно для старта, но на enterprise-выручке заметно давит на post-tax margin уже около нулевой EBITDA.
- **IT-льгота 3%** materially улучшает net result, если есть аккредитация Минцифры и соблюдены требования по профильной выручке.
- **ОСНО 20%** выглядит мягче по налогу на прибыль при положительной EBITDA, но добавляет **НДС 20%** и ухудшает оборотный капитал, особенно при длинном procurement cycle.
- **Страховые взносы ~30% к ФОТ** уже сидят в fully-loaded FOT **5 252 000 ₽/мес** и fixed costs **6 032 000 ₽/мес**.

### A9. Break-even по client count и по месяцам
| Scenario | Contribution / client / month | Fixed costs / month | Break-even clients | Break-even month |
|---|---:|---:|---:|---:|
| Base | 251 000 ₽ | 6 032 000 ₽ | 24.0 | M13 |
| Optimistic | 290 000 ₽ | 5 700 000 ₽ | 19.7 | M10 |
| Pessimistic | 210 000 ₽ | 6 250 000 ₽ | 29.8 | M22 |

### A10. Вывод по SECTION A
- **Base:** экономика сходится, но требует длинного горизонта и капитала на разгон; за 12 месяцев EBITDA ещё отрицательная.
- **Optimistic:** при чуть лучшем чеке, lower churn и более чистом delivery кейс выходит на EBITDA plus уже в **M12**.
- **Pessimistic:** модель остаётся убыточной весь первый год и требует самой жёсткой дисциплины по service load, иначе expansion становится слишком капиталоёмким.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев

Беру base-модель из SECTION A и проверяю три stress-фактора по одному. Для `CAC x2` считаю не только unit CAC, но и дополнительное давление на GTM OPEX: monthly acquisition spend растёт с ~2.20 млн ₽ до ~4.39 млн ₽, поэтому M12 EBITDA ухудшается на ~2.20 млн ₽ против base. Для `Churn x2` удваиваю monthly churn с 1.5% до 3.0%. Для `Price -30%` снижаю ARPA с 420k ₽ до 294k ₽ при почти фиксированном delivery load, что и является главным риском price compression.

| Scenario | Ключевое изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | без изменений | -146 741 | почти у нуля, но ещё не break-even |
| Sens1 | CAC x2 | -2 343 741 | GTM-модель резко теряет эффективность, burn снова становится венчурным |
| Sens2 | Churn x2 | -504 697 | экономика формально жива, но break-even сдвигается дальше и ухудшается LTV/CAC |
| Sens3 | Price -30% | -3 101 094 | самый токсичный сценарий, потому что delivery и support не падают пропорционально цене |

### B2. Monte Carlo Lite, confidence intervals

Полную 1000-итерационную симуляцию не запускаю. Вместо этого использую облегчённую схему из 9 комбинаций на базе triangular assumptions и беру p10/p50/p90 как приближение к worst / median / best участкам распределения. Это достаточно, чтобы проверить хрупкость модели.

#### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 700 000 | 998 636 | 1 600 000 | [T1], [T2] |
| Monthly churn, % | 1.0% | 1.5% | 3.0% | [T1], [T2] |
| ARPU, ₽/мес | 320 000 | 420 000 | 520 000 | [T1], [T2], [T3] |
| Conversion rate lead→paid, % | 0.6% | 1.2% | 2.1% | [T1] |
| Time-to-hire, мес | 1.0 | 1.5 | 2.5 | [T1] |

Где:
- **[T1]** `04-economics.md` по кейсу: base CAC, blended conversion, team hiring realism, base ARPU/churn.
- **[T2]** `02-demand.md`: локальный ценовой якорь Mindbox 150k/400k+ ₽ и enterprise budget envelope.
- **[T3]** внешние price/positioning anchors: Hightouch AI Decisioning, Hilbert positioning, enterprise warehouse-native growth stack.

#### 9-combo approximation

| Комбинация | CAC | Churn | ARPU | Интерпретация |
|---|---:|---:|---:|---|
| 1 | min | min | max | best case |
| 2 | mode | mode | mode | median |
| 3 | max | max | min | worst case |
| 4 | min | mode | max | mixed upside |
| 5 | min | max | mode | CAC good, retention bad |
| 6 | mode | min | mode | retention upside |
| 7 | mode | max | min | downside on retention + pricing |
| 8 | max | min | mode | expensive CAC, но продукт держит value |
| 9 | max | mode | min | дорогой CAC и сжатый чек |

#### Confidence interval table

| Метрика | p10 | p50 | p90 | Range width |
|---------|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -2 620 000 | 4 780 000 | 19 140 000 | 21 760 000 |
| CAC payback, мес | 3.3 | 3.7 | 7.6 | 4.3 |
| LTV/CAC | 4.3x | 18.2x | 48.3x | 44.0 |
| Cash runway, мес | 8.9 | 14.3 | 18.2 | 9.3 |

#### Что это значит
- **Правило 1 выполнено:** `p10 EBITDA < 0`, значит kill criterion #1 обязателен, риск неплатёжеспособности реален.
- **Правило 2 не срабатывает:** `p50 EBITDA = 4.78 млн ₽/мес`, то есть median-сценарий проходит EBITDA gate.
- **Правило 3 частично тревожный:** разброс очень большой, хотя из-за отрицательного p10 отношение `p90/p10` формально некорректно. По сути диапазон всё равно слишком широк и требует discount к score за неопределённость.
- **Правило 4 срабатывает:** ширина диапазона по `LTV/CAC` заметно выше 8, значит модель хрупкая и очень чувствительна к сочетанию pricing, churn и CAC.

### B3. Competitor deep-dive

Ниже не пытаюсь посчитать точную рыночную долю по всему martech-рынку. Я оцениваю **долю именно в узком под-сегменте warehouse-native / AI decisioning / data-mature B2C growth infrastructure**. Все доли, это **оценка по публичной видимости, customer footprint, выручке, enterprise presence и числу релевантных кейсов**, а не официальный market-share disclosure.

#### Западные конкуренты

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Hightouch | самый близкий публичный аналог warehouse-native activation + AI Decisioning | сильный warehouse-native narrative, зрелый reverse ETL, enterprise trust, явный AI Decisioning SKU | дорогой и сложный стек, заточен под западный martech/data stack, слабее локализация под РФ и residency | 25-30% глобального узкого subsegment | локальная data residency, русскоязычный delivery, интеграции под РФ CDP/CRM/payment/legal контур |
| GrowthLoop | warehouse-native marketing orchestration и decisioning для enterprise growth teams | сильный GTM на enterprise marketers, близкая ценность для B2C lifecycle команд, хорошая orchestration story | category awareness ниже Hightouch, может требовать heavy enablement и зрелую growth-команду у клиента | 10-15% | более короткий путь к value для РФ-команд, дешевле внедрение, меньше зависимость от западных SaaS |
| RudderStack | сильный customer data pipeline + warehouse activation adjacent substitute | сильная data infrastructure репутация, гибкая developer-first архитектура, хорош как foundational layer | не так силён именно в decisioning outcome layer, нужен дополнительный orchestration/analytics слой | 10-15% в adjacent warehouse activation layer | мы продаём не трубы, а uplift layer: detect/reason/act с ROI narrative для growth-команды |

#### Российские конкуренты

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Mindbox | главный локальный ценовой и category anchor в CRM marketing / CDP / персонализации | сильный бренд, много enterprise B2C кейсов, понятный buyer, зрелый ecosystem fit | больше rule-based CRM/CDP, чем warehouse-native AI decisioning; buyer может получить “достаточно хорошо”, но не full decisioning layer | 35-45% в локальном enterprise CRM-personalization сегменте | более глубокий AI-native decisioning, лучше для data-mature команд, меньше lock-in в rules-first сценарии |
| Retail Rocket | сильный игрок в e-commerce personalization и recommendation infrastructure | сильный e-commerce фокус, понятный performance ROI, legacy footprint в retail | уже воспринимается как более узкий personalization vendor, а не общий growth decisioning layer | 10-15% | у нас шире use cases: acquisition-retention-monetization, а не только рекомендации и onsite personalization |
| Altcraft | локальная CDP / omnichannel automation платформа | локальная инфраструктура, enterprise-friendly compliance, понятная CDP value proposition | скорее CDP/automation, чем AI-native growth intelligence; тяжёлый внедренческий профиль | 8-12% | warehouse-native decisioning поверх существующего data stack, а не очередная “центральная маркетинговая система” |
| enKod | локальный retention marketing automation игрок | более доступный вход, понятен mid-market, быстрее коммерческий цикл | слабее в data depth, enterprise decisioning и сложной ML/warehouse логике | 5-8% | сильнее на high-end enterprise use cases, где нужен decision layer, а не просто lifecycle automation |

#### Вывод по конкурентному полю
- **Главный западный комп**: Hightouch. Это прямое доказательство, что category monetizable.
- **Главный российский комп**: Mindbox. Это главный риск budget substitution: buyer может сказать “зачем нам новый слой, если у нас уже есть CDP/CRM platform?”
- **Реальный wedge Hilbert в РФ** возможен только если продукт продаётся как **incremental profit engine**, а не как “ещё одна маркетинговая платформа”.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Команда не успевает productize onboarding, и delivery превращается в quasi-consulting | high | high | >40 часов ручной настройки на нового клиента, рост кастомных SOW | стандартизировать implementation playbooks, жёстко резать bespoke requests |
| 2 | Operational | Зависимость от внешних LLM API и model latency/quality drift | med | high | рост inference cost на >25%, деградация recommendation quality, SLA incidents | multi-model routing, fallback на rules, лимиты токенов, локальные open-weight резервные контуры |
| 3 | Market | Exact-demand по категории остаётся низким, pipeline не наполняется | med | high | inbound почти нулевой, founder-led канал даёт >60% всех сделок | продавать через ROI/use-case narrative, а не через category keyword |
| 4 | Market | Price compression из-за Mindbox/CDP substitutes | high | high | discounting >20%, проигрыши по причине “дорого относительно текущего стека” | пакетировать uplift SLA, proof-of-value pilot, value-based pricing с KPI guardrails |
| 5 | Regulatory | 152-ФЗ и требования по data residency ограничивают SaaS-архитектуру и cross-border data flows | med | high | security/legal блокируют пилоты, клиенты требуют on-prem / RU-hosting | RU-hosting by default, data minimization, сегментация PII и feature-store |
| 6 | Regulatory | 115-ФЗ / KYC / финмониторинг и compliance burden у fintech/gambling verticals | low | med | затяжной legal review, дополнительные требования к audit trail | отраслевые policy packs, журналирование решений, explainability для критичных use cases |
| 7 | Financial | Cash runway съедается раньше PMF из-за дорогого enterprise GTM | high | high | runway <12 мес при EBITDA всё ещё <0, CAC >1.5 млн ₽ | заморозка найма, сокращение каналов, переход в founder-led/partner-led GTM |
| 8 | Financial | Курс USD и импортная SaaS-инфраструктура давят на COGS и gross margin | med | med | рост infra/LLM счетов >20% QoQ, GM падает ниже 60% | рублёвые контракты, предоплата, замещение части стека локальными компонентами |
| 9 | Black swan | Новый пакет санкций режет доступ к западным SaaS/API/integration stack | med | high | срочные уведомления вендоров, остановка биллинга или API access | список критичных замен, резервный стек, перенос orchestration в контролируемый контур |
| 10 | Black swan | Военный/макро-шок замораживает маркетинговые бюджеты enterprise B2C | med | high | массовая заморозка экспериментов, сдвиг procurement на 1-2 квартала | фокус на retention/cost-saving use cases, shorter pilots, cash conservation mode |

### B5. Kill conditions

Если через 6 месяцев видим хотя бы один из пунктов ниже, проект как standalone venture продолжать нельзя:

1. **Median economics fail:** rolling `p50 EBITDA@M24 < 500 000 ₽/мес` или фактический forecast EBITDA остаётся ниже этого порога после обновления воронки и churn. Это означает, что даже median-сценарий не проходит gate.
2. **Retention fail:** logo churn устойчиво `>4% в месяц` два квартала подряд или `net revenue retention < 90%`. Тогда LTV collapses и модель перестаёт быть software-like.
3. **Go-to-market fail:** fully-loaded `CAC > 1.8 млн ₽` **или** к концу M6 меньше `8 платящих клиентов / 3 активных design-partner accounts`, несмотря на founder-led продажи. Это значит, что repeatable GTM не появляется.

### B6. Итог SECTION B

Кейс **не разваливается**, но становится заметно более хрупким, чем это видно из одной только base-модели. Самые опасные зоны:
- **price compression**,
- **service-heavy onboarding**,
- **зависимость от внешнего LLM и санкционного контура**,
- **substitution risk со стороны Mindbox и других CRM/CDP платформ**.

Поэтому мой вывод такой:
- **финансово кейс survivable в median-сценарии**, 
- **но в p10-сценарии уже есть риск неплатёжеспособности**, 
- а значит дальше его можно держать только с явным discount к score за неопределённость и с жёсткими kill conditions.

### B7. Sources / anchors used in SECTION B
- [T1] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/2327-msk-hilbert-geo-expand-v2/04-economics.md`
- [T2] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/2327-msk-hilbert-geo-expand-v2/02-demand.md`
- Hightouch pricing: https://hightouch.com/pricing/
- Hightouch AI Decisioning: https://hightouch.com/docs/ai-decisioning/overview
- GrowthLoop: https://www.growthloop.com/
- RudderStack: https://www.rudderstack.com/
- Mindbox tariffs: https://mindbox.ru/tariffs/
- vc.ru / Habr / Rusprofile / Skolkovo pages used as Russian market anchors for Mindbox, Retail Rocket, Altcraft, enKod

<!-- P6B-DONE -->

---

## 06-verdict.md

[GEO-EXPAND] Hilbert — REJECTED: 63/100 | EBITDA base=633К₽/мес через 14 мес | LTV/CAC=18,2x | Ключевое преимущество: высокий апсайд при enterprise-чеке и measurable uplift | Главный риск: weak moat и низкий exact-demand в РФ.

# 06-verdict

sector: GEO-EXPAND
case: 2327-msk-hilbert-geo-expand-v2
date: 2026-04-21
stage: verdict
analyst: branch-models-lead
status: done
verdict: REJECTED
normalized_score: 63/100
raw_score: 94/150
investment_grade: false
company_ebitda_rub_month_base: 633000
company_ebitda_potential_rub_month: 1500000
clients_to_500k_ebitda: 26
months_to_500k_ebitda: 14
startup_capital_to_bep_rub: 40515999

## Итог инвесткомитета

Hilbert проходит формальный economics-gate, но не проходит investment-grade gate для текущего цикла. Причина не в LTV/CAC, а в том, что локальный exact-demand слабый, moat остаётся слабым, а GTM и delivery слишком завязаны на founder-led enterprise motion и тяжёлый implementation. Для APPROVED здесь не хватает доказанного premium wedge поверх Mindbox/CDP substitutes.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | «LTV/CAC = 18.2x», «Gross Margin = 65.0%», «CAC Payback ... 3.66 мес по gross profit». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | «EBITDA > 500 тыс. ₽/мес достижима» и в base «EBITDA break-even month M13», при 30 клиентах «EBITDA ≈ 1.50 млн ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 8 | «Composite demand: LOW», «Demand score: 0», «hh.ru vacancies: 0», но «SAM = 1,35 млрд ₽/год». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Продукт полезен, но «buyer уже может закрывать часть боли через CDP/CRM/performance stack», значит moat ограничен. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | «hidden services load может резко ухудшить gross margin», есть риск «зависимость от внешних LLM API и model latency/quality drift». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | Есть реалистичный ICP и named targets, но GTM всё ещё «consultative enterprise sale» с CAC около «998 636 ₽». |

**Normalized score = round((94 × 100) / 150) = 63/100.**

## 7-factor Moat Framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | После интеграции в warehouse/CRM/CDP появляются данные, процессы и обученная команда. |
| Scale economies | 1 | COGS частично падает с объёмом, но service load остаётся высоким. |
| Proprietary data / model advantage | 1 | Собственный decisioning layer возможен, но подтверждённого data moat в РФ нет. |
| Regulatory moat | 1 | 152-ФЗ и data residency важны, но это скорее барьер исполнения, чем сильный moat. |
| Brand / distribution | 1 | Есть global signal от a16z/Hilbert, но локального brand/distribution moat нет. |
| Embedded workflow | 3 | При успешном внедрении продукт встраивается в acquisition-retention-monetization циклы клиента. |

**Moat score = round((9 × 25) / 21) = 11/25.**

Вывод: moat слабый, но не нулевой. Ниже approve-уровня. Weak moat остаётся в Top-3 Risks.

## FULL business process из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP mapping по B2C accounts | SDR / analyst | CRM, Rusprofile, manual research | 2 ч | 2 200 | Низкий |
| 2 | Первичный outreach | SDR | Email, Telegram, phone | 1.5 ч | 1 700 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 200 | Средний |
| 4 | Discovery по data stack и growth process | AE + founder | Workshop, questionnaire | 2.5 ч | 11 000 | Низкий |
| 5 | Tech / data feasibility review | Solutions engineer | Warehouse map, event audit | 3 ч | 13 500 | Низкий |
| 6 | Demo и ROI narrative | AE + solutions | Demo env, сценарии uplift | 2 ч | 9 500 | Низкий |
| 7 | Pilot scoping и KPI definition | AE + CSM | SOW, KPI model | 3 ч | 13 000 | Низкий |
| 8 | Integration / onboarding | Solutions + CSM | CDP/CRM connectors, runbooks | 14 ч | 49 000 | Средний |
| 9 | Pilot 4–6 недель | CSM + analyst | dashboards, support | 12 ч | 36 000 | Средний |
| 10 | Security / procurement / legal | AE + founder + ops | contract workflow | 7 ч | 22 000 | Низкий |
| 11 | Commercial proposal / negotiation | AE + founder | pricing calculator, CRM | 4 ч | 16 000 | Низкий |
| 12 | Production rollout после оплаты | CSM + solutions | playbooks, monitoring | 8 ч | 27 000 | Средний |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 18 200 000 ₽ |
| CAC fully-loaded | 998 636 ₽ |
| LTV/CAC | 18.2x |
| CAC payback по revenue | 2.38 мес |
| CAC payback по gross profit | 3.66 мес |
| Gross Margin | 65.0% |
| contribution_margin_rub_month | 251 000 ₽ |
| fixed_costs_rub_month | 6 032 000 ₽ |
| company_ebitda_rub_month @30 клиентов | 1 500 000 ₽/мес |
| Break-even clients | 24 |
| Break-even month (base) | M13 |
| startup_capital_to_bep_rub | 40 515 999 ₽ |
| months_to_500k_ebitda | 14 |
| clients_to_500k_ebitda | 26 |
| clients_to_1m_ebitda | 28 |

## Team table

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / tech lead | 1 | 520 000 | 2 | 2 | 156 000 | 676 000 |
| Backend / data engineer | 2 | 400 000 | 1.5 | 1.5 | 120 000 | 1 040 000 |
| ML / applied AI engineer | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Solutions engineer | 1 | 360 000 | 1.5 | 1.5 | 108 000 | 468 000 |
| Product / analytics lead | 1 | 340 000 | 1.5 | 1.5 | 102 000 | 442 000 |
| SDR | 2 | 155 000 + бонус | 1 | 1 | 46 500 | 403 000 |
| AE | 1 | 300 000 + комиссия | 1.5 | 2 | 90 000 | 390 000 |
| CSM / implementation | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Finance / ops (part-time) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого** | **11.5** |  |  |  |  | **5 252 000 ₽/мес** |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Самокат | retention, частые повторные покупки, сильная CRM-машина и быстрая ценность от decisioning | email decision-maker + профильные retail/CRM конференции | 450 000 ₽/мес |
| 2 | X5 Digital | grocery delivery и промо-оптимизация, высокая частота коммуникаций | партнёрство через data/CRM ecosystem | 500 000 ₽/мес |
| 3 | Ozon | зрелый data stack, marketplace lifecycle и monetization optimization | outbound к CRM/growth lead | 650 000 ₽/мес |
| 4 | Wildberries | огромный объём поведенческих событий и персонализация удержания | конференция + тёплый enterprise outreach | 650 000 ₽/мес |
| 5 | Яндекс Маркет | сложные CRM и performance сценарии, нужен uplift layer поверх существующего стека | email decision-maker | 600 000 ₽/мес |
| 6 | Мегамаркет | marketplace growth, промо и retention orchestration | партнёрство + enterprise event | 450 000 ₽/мес |
| 7 | Avito | marketplace с сильным retention и monetization motion | founder-led intro + outbound | 700 000 ₽/мес |
| 8 | T-Банк | lifecycle marketing и ML-ready growth процессы в fintech | referral intro + targeted outbound | 700 000 ₽/мес |
| 9 | МТС | telecom CRM, churn-prediction и next-best-action use cases | enterprise sales + отраслевые конференции | 550 000 ₽/мес |
| 10 | Okko | subscription economics, churn reduction и content-personalization loops | content-led outreach + email | 420 000 ₽/мес |

**Комментарий:** список targets реалистичен для ICP, но сделка почти везде потребует тяжелого discovery, security review и доказательства measurable uplift. Это не лёгкий SaaS-motion.

## Top-3 Risks

1. **Weak moat / budget substitution**  
   Вероятность: высокая. Влияние: высокое.  
   Buyer может остаться на Mindbox/CDP/CRM stack и не покупать отдельный decisioning layer.

2. **Service-heavy implementation**  
   Вероятность: высокая. Влияние: высокое.  
   Если onboarding и analytics support не productize, gross margin и churn быстро деградируют.

3. **evidence_quality_unverified**  
   Вероятность: средняя. Влияние: среднее-высокое.  
   В кейсе отсутствует строка Sources по tiering, а также нет 02-validation.md и 03-demand.md по целевой схеме, поэтому качество евиденции и процессная полнота ниже стандарта.

## Почему не APPROVED

1. Локальный спрос по exact label слабый: в demand-stage зафиксировано «Composite demand: LOW» и «Demand score: 0».
2. Moat слабый: value есть, но buyer уже имеет substitutes в виде Mindbox/CDP/CRM/performance stack.
3. GTM тяжёлый: enterprise consultative sale, CAC почти 1 млн ₽ и длинный путь через pilot, legal и procurement.
4. P10-риск отрицательный: в Monte Carlo Lite «p10 EBITDA < 0», значит у модели нет достаточного запаса прочности.

## LTV Upside Calculator

Если вернуться к кейсу позже, вот что даст самый сильный апсайд:

| Рычаг | Текущее | Целевое | Эффект |
|---|---:|---:|---|
| ARPA | 420 000 ₽ | 500 000 ₽ | +80 000 ₽ выручки на клиента, лучшее покрытие heavy delivery |
| COGS на клиента | 147 000 ₽ | 125 000 ₽ | +22 000 ₽ к contribution_margin_rub_month |
| contribution_margin_rub_month | 251 000 ₽ | 353 000 ₽ | Снижает clients_to_500k_ebitda примерно с 26 до 19 |
| Annual churn | 18% | 12% | Увеличивает customer_ltv_rub примерно с 18.2 млн ₽ до 27.1 млн ₽ |
| CAC | 998 636 ₽ | 800 000 ₽ | Улучшает capital efficiency и burn-to-breakeven |

**Формула апсайда:** чтобы кейс стал approve-кандидатом, нужно одновременно доказать premium-чек 500К+ ₽, более productized delivery и удержание churn ближе к 12% annual.

## Финальный вердикт

**REJECTED.**

Несмотря на сильную формальную unit economics и достижимый company_ebitda_potential_rub_month выше 500 тыс. ₽/мес, кейс пока не проходит порог инвестиционного одобрения. Основная причина, это не математическая слабость, а слабая защищаемость premium wedge и недостаточно подтверждённый локальный repeatable demand.

## Следующий шаг

Если появятся 2-3 локальных design partners из data-mature B2C с подтверждённым uplift и ARPA 500К+ ₽/мес, кейс стоит rerun как near-pass/approve candidate.

---

## 07-score-trajectory.md

# 07-score-trajectory

| Дата | Stage | Score | Verdict | Комментарий |
|---|---|---:|---|---|
| 2026-04-21 | P7 Critic and Verdict | 63/100 | REJECTED | Сильная unit economics и EBITDA potential не компенсируют слабый локальный demand proof, weak moat и service-heavy GTM. |
