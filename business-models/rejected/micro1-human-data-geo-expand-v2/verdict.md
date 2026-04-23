# verdict.md

Собранный артефакт по кейсу `micro1-human-data-geo-expand-v2`.


<!-- SOURCE: 01-intake.md -->

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-micro1-human-data-geo-expand.md
created: 2026-04-21T00:38:19+03:00
---

# 01-intake

## Кейс
micro1-human-data-geo-expand-v2

## Тип intake
resurrect

## rerun_of
micro1-human-data-geo-expand

## Ссылка на оригинальный verdict
triage/triage-2026-04-14-micro1-human-data-geo-expand.md

## Дата intake
2026-04-21, Europe/Moscow

## Полный контекст raw file

# RESURRECT SIGNAL — micro1-human-data-geo-expand

## Meta
- source: triage/triage-2026-04-14-micro1-human-data-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-micro1-human-data-geo-expand.md

## Классификация
кандидат в новый кейс

## Решение
Открыть новый кейс: `human-data-ai-trainers-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы не покрывают отдельно human data operations, expert workforce orchestration и AI trainers для обучения и оценки frontier-моделей.
- Сигнал по micro1 сильный по коммерческому масштабу: по TechCrunch компания выросла примерно с 7 млн долларов ARR в начале 2025 года до более 100 млн долларов ARR к 4 декабря 2025 года.
- Это не просто рекрутинг или generic аутсорс разметки. Сигнал указывает на формирование отдельного операционного слоя: подбор, верификация, управление качеством и координация тысяч экспертов в сотнях доменов для AI-лабораторий и крупных корпоративных клиентов.
- По экономике кейс проходит порог для открытия: `ltv_signal` в raw указан как 3-12 млн руб. в год на клиента, то есть примерно 250 000-1 000 000 руб. в месяц. Верхняя часть диапазона превышает порог `> 500 000 руб./мес.`.
- Локализация трудная, что повышает потенциальную ценность сервисного слоя: нужны русскоязычные и доменные эксперты, процессы верификации, quality control, secure workflows и управление supply под чувствительные use cases.
- В raw отмечено, что прямой зрелый локальный аналог глобального масштаба неочевиден, что поддерживает GEO-EXPAND гипотезу.

## Что сделано
- Создан новый кейс `pipeline/cases/human-data-ai-trainers-operator/`.
- В `00-brief.md` зафиксированы описание модели, стартовые факты и ключевая гипотеза для следующего validation block.
- Исходный raw-файл подлежит переносу в `pipeline/raw/processed/`.

## Пометка для следующего шага
Дальше проверять не только рынок разметки, а именно категорию managed human data operations. Нужны подтверждения по:
- buyer profile: frontier labs, enterprise AI teams, data vendors, model evaluation команды;
- unit economics: цена за expert hour, за evaluation program, за managed pool, за SLA и recurring contracts;
- глубине moat: supply quality, screening, multilingual coverage, domain expertise, security и compliance;
- российским и СНГ-аналогам, чтобы понять, есть ли реальное окно для GEO-EXPAND;
- степени productization: где заканчивается агентская услуга и начинается repeatable operator model.

## Вердикт
Сигнал достаточно сильный для открытия отдельного кейса: тема выглядит как правдоподобная high-LTV категория на стыке AI infrastructure, expert operations и managed human data layer.

```


<!-- SOURCE: 02-demand.md -->

---
stage: demand-validation
case: micro1-human-data-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
micro1: managed human data operations, orchestration доменных экспертов и production-layer для post-training, RL, evaluation и сложных датасетов для frontier AI labs и enterprise AI-команд.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Exact-demand в РФ по формулировкам `human data operations`, `model evaluation services`, `AI trainers`, `ai training data services` и `expert data for AI` выглядит как **LOW**. [T2]
- Но adjacent-спрос по более приземлённым русскоязычным категориям уже заметен: `разметка данных для ИИ` и `оценка моделей ИИ` дают вакансии и высокий suggest-хвост, то есть базовая buyer-потребность существует, просто локальный рынок пока описывает её более общими словами. [T2]
- Глобальный category proof сильный: micro1 публично продаёт white-glove human data engine для frontier AI labs, говорит о 130 000+ vetted experts в 100+ доменах и 60+ языках, а TechCrunch на **4 декабря 2025 года** писал о росте компании примерно с **$7 млн ARR** в начале 2025 года до **$100+ млн ARR** к декабрю 2025 года. [T1]
- Это не self-serve SaaS и не массовый SMB-продукт. Для РФ тезис выглядит как узкий GEO-EXPAND high-ticket слой для крупных AI-команд, интеграторов, data vendors и enterprise-контуров, где нужен managed supply доменных экспертов, quality control и secure workflows. [T1/T2/T3]

## 1) Спрос и сигналы рынка

### Demand API
- `AI trainers` → LOW, Google Trends RU 1, HH vacancies 0, Yandex suggest 100. [T2]
- `human data operations` → LOW, Google Trends RU 0, HH vacancies 0, Yandex suggest 2. [T2]
- `model evaluation services` → LOW, Google Trends RU 0, HH vacancies 1, Yandex suggest 2. [T2]
- `expert data for AI` → LOW, Google Trends RU 0, HH vacancies 2, Yandex suggest 2. [T2]
- `ai training data services` → LOW, Google Trends RU 0, HH vacancies 1, Yandex suggest 2. [T2]
- `разметка данных для ИИ` → LOW, Google Trends RU 0, HH vacancies 58, Yandex suggest 100. [T2]
- `оценка моделей ИИ` → LOW, Google Trends RU 0, HH vacancies 234, Yandex suggest 100. [T2]

### Интерпретация
- По exact-labels рынок в РФ пока не созрел. Покупатели не ищут `human data engine` как оформленную категорию. [T2]
- Но подлежащая боль уже есть: data labeling, evaluation, supply доменных специалистов, QA и контроль качества AI-output. Просто локальная упаковка спроса более фрагментирована и часто скрыта внутри broader AI-services / annotation / model eval budgets. [T2/T3]
- Следовательно, низкий exact-demand не равен отсутствию бюджета. Он означает длинный sales cycle, высокий education burden и необходимость продавать через более понятные входы, например `оценка моделей`, `разметка`, `экспертная валидация`, `RLHF/evals as a service`. [T2]

## 2) Category proof и why now
1. micro1 на собственном сайте позиционирует себя как **human data layer powering frontier AI** и white-glove data engine для AI labs. Это важный признак, что продаётся не просто marketplace фрилансеров, а управляемая production-система. [T1]
2. На product-страницах micro1 заявляет **130 000+ vetted candidates**, покрытие **100+ доменов** и **60+ языков**, плюс собственный data platform, quality dashboard и AI recruiter agent Zara. Это усиливает тезис о repeatable operator model, а не о ручном агентстве. [T1]
3. TechCrunch на **4 декабря 2025 года** писал, что micro1 вырос примерно с **$7 млн ARR** в начале 2025 года до **$100+ млн ARR**, работая с ведущими AI labs и Fortune 100. Это очень сильный внешний сигнал реальной willingness to pay за managed human data layer. [T1]
4. Adjacent proof есть и у Mercor: TechCrunch на **27 октября 2025 года** описывал pivot компании в сторону поставки доменных экспертов для обучения foundation models и раунд **$350 млн** при оценке **$10 млрд**. Значит, рынок платит не только за annotation, а за orchestration expert labor around model training. [T3]

## 3) Что это значит для GEO-EXPAND в РФ
- В РФ кейс вряд ли полетит как чистый копипаст глобального AI lab motion, потому что число локальных frontier labs ограничено. [T2/T3]
- Но он может зайти как сервисный слой для:
  - крупных enterprise AI-команд,
  - системных интеграторов и data vendors,
  - компаний с sensitive domains: legal, finance, healthcare, industrial,
  - команд, которым нужны экспертные evals, red-teaming, prompt/rubric design, human QA и domain-specific datasets. [T1/T2]
- Значит, локальный wedge это не generic "нанимаем людей для AI", а **managed expert data operations** с безопасным контуром, quality governance и SLA. [T1/T2]

## 4) Buyer и бюджет
### Вероятные buyer'ы
- Head of AI / VP AI / Chief Data Officer
- Руководители model evaluation / post-training / AI quality
- Product owners AI-platform / LLM initiatives
- Крупные интеграторы, которые строят AI delivery для enterprise-клиентов
- Data vendors и аутсорс-платформы, которым нужен white-label слой expert operations

### Budget bucket
- AI R&D / post-training budget
- data operations / data labeling / evaluation budget
- professional services budget вокруг enterprise AI
- vendor budget на managed expert pools и secure annotation/evals

### Вывод
Buyer и бюджет выглядят реальными, но они enterprise-heavy и не лежат в массовом спросе. Это сразу отсекает SMB-motion, зато поддерживает GEO-EXPAND high-LTV thesis. [T1/T2/T3]

## 5) TAM / SAM / SOM в рублях

### Подход и допущения
Беру консервативный локальный motion как managed expert data operations, а не как pure staffing.

- Базовый контракт: **500 000 ₽/мес** за узкий managed pool / evaluation program.
- Более сильный enterprise-контур: **1 200 000 ₽/мес** за multi-domain expert data ops, QA и governance.

### TAM
Если взять **1 200** потенциальных buyer-контуров в РФ/СНГ, где есть заметные AI-программы, интеграторы и data-heavy enterprise-команды, и усреднённый чек **6 млн ₽/год**, получаем:

**TAM ≈ 7,2 млрд ₽/год**

### SAM
Реально addressable слой в ближайшие 24 месяца, где есть зрелость бюджета и потребность в доменных данных, оцениваю в **180** аккаунтов.

**SAM ≈ 1,08 млрд ₽/год**

### SOM
Реалистичный ранний захват:
- **6 клиентов** × **6 млн ₽/год** = **36 млн ₽/год**
- Upside-сценарий: **10 клиентов** × **9,6 млн ₽/год** = **96 млн ₽/год**

### Интерпретация
Sizing не выглядит безумным, если продавать как enterprise service layer. Но это именно узкий GEO-EXPAND сценарий, а не массовый локальный software market. [T2/T3]

## 6) Profit Gate

### Сценарий A: annotation / eval vendor-lite
- Цена: **500 000 ₽/мес**
- Валовая маржа: **45%**
- Валовая прибыль на клиента: **225 000 ₽/мес**
- Для выхода на **500 000 ₽ EBITDA/мес** при fixed costs **1,8 млн ₽/мес** нужно около **11 клиентов**
- **Вердикт:** STRETCH

### Сценарий B: managed expert data ops
- Цена: **1 200 000 ₽/мес**
- Валовая маржа: **50%**
- Валовая прибыль на клиента: **600 000 ₽/мес**
- Для той же цели достаточно **4 клиентов**
- **Вердикт:** PASS

### Сценарий C: white-label layer для интегратора / AI vendor
- Цена: **800 000 ₽/мес**
- Валовая маржа: **48%**
- Валовая прибыль на клиента: **384 000 ₽/мес**
- Нужно **6-7 клиентов**
- **Вердикт:** PASS WITH EXECUTION RISK

### Общий вывод по Profit Gate
- Как commodity labeling business кейс выглядит посредственно.
- Как managed expert operations для high-stakes AI workflows кейс проходит gate.
- Значит, ранний reject на P3 не нужен, но дальше в P4/P5 придётся жёстко проверить CAC, hiring realism и способность собирать repeatable supply-side moat.

## 7) Основные риски
- Локальный exact-demand слабый и buyer education дорогой. [T2]
- Очень тяжёлый supply side: screening, trust, quality control, compliance и удержание доменных экспертов. [T1/T3]
- Риск, что рынок скатится в staffing/agency economics вместо productized operator model. [T1/T2]
- Сильная зависимость от нескольких крупных клиентов и ограниченного числа реальных AI buyers в регионе. [T2/T3]
- Вероятный overlap с соседними кейсами про data labeling, AI services и workforce orchestration, который надо проверить на поздних этапах. [T2]

## 8) Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Кейс не стоит отклонять на P3. Несмотря на слабый exact-demand в РФ, есть сильный глобальный category proof, понятный enterprise buyer, правдоподобный путь к high-LTV и достаточно чёткий wedge в виде managed expert data operations. Но это рабочая гипотеза только в узком enterprise GEO-EXPAND формате, не как массовый локальный продукт.

## Источники
- micro1 homepage: https://www.micro1.ai/ [T1]
- micro1 AI labs / human data engine: https://www.micro1.ai/data-engine/ai-labs [T1]
- TechCrunch, Micro1 crossed $100M ARR, 2025-12-04: https://techcrunch.com/2025/12/04/micro1-a-scale-ai-competitor-touts-crossing-100m-arr/ [T1]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20trainers [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=human%20data%20operations [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=model%20evaluation%20services [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=expert%20data%20for%20AI [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=ai%20training%20data%20services [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%82%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B4%D0%BB%D1%8F%20%D0%98%D0%98 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D1%86%D0%B5%D0%BD%D0%BA%D0%B0%20%D0%BC%D0%BE%D0%B4%D0%B5%D0%BB%D0%B5%D0%B9%20%D0%98%D0%98 [T2]
- TechCrunch, Mercor Series C and pivot to domain experts for model training, 2025-10-27: https://techcrunch.com/2025/10/27/mercor-quintuples-valuation-to-10b-with-350m-series-c/ [T3]

Sources: T1=3, T2=7, T3=1. Primary evidence basis: T1/T2.

> Market Pulse 2026-04-21: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, продуктовых страниц, внедренческих материалов и/или коммерческих сигналов, чем в прошлых срезах.

## Market Pulse
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.


<!-- SOURCE: 04-economics.md -->

---
stage: economics
case: micro1-human-data-geo-expand-v2
date: 2026-04-23
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
sector: GEO-EXPAND
---

# 04-economics — Unit Economics

## Кейс
micro1 GEO Expand v2, managed human data operations и orchestration доменных экспертов для post-training, evals, RLHF, red-teaming и production-grade human QA для enterprise AI-команд.

## Executive summary

**Итог P5: CONDITIONAL PASS.**

Почему:
1. **Путь к EBITDA > 500k ₽/мес есть**, если продавать не как commodity-разметку, а как managed expert data ops с ARPA около **1,2 млн ₽/мес**.
2. При таком позиционировании бизнес выходит на operating break-even примерно на **21 клиенте**, а при **50 клиентах** даёт запас по EBITDA.
3. Главный риск не в gross profit, а в **supply-side execution**: набор, верификация, удержание и контроль качества редких экспертов.
4. Модель **не investment grade** для фонда на раннем этапе, потому что высокая зависимость от founder-led sales, длинного enterprise cycle и ручного delivery сохраняется.

## 1. Модель и ключевые допущения

### ICP
- крупные enterprise AI-команды;
- интеграторы и AI delivery-подрядчики;
- data vendors и model-eval команды;
- sensitive verticals: legal, finance, healthcare, industrial.

### Монетизация, base case для РФ/СНГ
- Recurring managed program: **1 200 000 ₽/клиент/мес**
- One-off onboarding / scoping / secure setup: **700 000 ₽**
- В recurring входят: managed pool экспертов, QA, program management, workflow governance, отчётность и SLA.

### Почему беру 1,2 млн ₽ MRR
- В 02-demand уже показано, что **500k ₽/мес** это нижняя граница узкого пилота, а рабочий enterprise-контур скорее ближе к high-touch managed service.
- TechCrunch пишет, что micro1 работает с leading AI labs и Fortune 100, а многие эксперты получают около **$100/час**. Это поддерживает тезис, что дешёвая модель здесь экономически не складывается и цена должна включать дорогой expert labor + orchestration premium. [T1]
- Сайт micro1 описывает не marketplace, а white-glove engine с recruiting, vetting, training, QA и performance tracking. Значит, продавать нужно как managed operations layer, а не как почасовую биржу. [T1]

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping и shortlist ICP | SDR + founder | CRM, research, referrals | 2 ч | 4 000 | Низкий |
| 2 | Founder-led intro / outbound | Founder + SDR | email, Telegram, warm intros | 2 ч | 8 000 | Низкий |
| 3 | Discovery по use case и бюджету | Founder + AE | call, questionnaire | 1.5 ч | 10 000 | Низкий |
| 4 | Scoping human data workflow | Solutions lead + domain lead | template, workshop | 3 ч | 24 000 | Низкий |
| 5 | Security / compliance pre-check | Founder + ops | NDA, checklist | 2 ч | 9 000 | Низкий |
| 6 | Pilot design и sample task | PM + domain reviewer | platform, rubric, QA sheet | 6 ч | 42 000 | Средний |
| 7 | Paid / semi-paid pilot | PM + expert pool | managed execution | 20 ч | 130 000 | Низкий |
| 8 | Commercial negotiation | Founder + AE | pricing model, proposal | 3 ч | 18 000 | Низкий |
| 9 | Contract / procurement | AE + ops | ЭДО, договор, счёт | 4 ч | 16 000 | Средний |
| 10 | Production onboarding | PM + QA lead + platform ops | runbook, dashboard, SLA | 14 ч | 85 000 | Средний |

### Вывод по процессу
Продажа тяжёлая и enterprise-консультативная. До оплаты много ручной работы, поэтому CAC будет высоким, а масштабируемость в первый год ограничена founder bandwidth.

## 3. COGS per client / month

### Разбивка COGS на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| Выплаты экспертам / subject-matter pool | 420 000 | mix из domain experts и reviewers |
| QA lead и human data supervision | 80 000 | allocation на клиента |
| Program manager / account operations | 70 000 | allocation на клиента |
| Platform / infra / storage / tooling | 45 000 | secure workspace, tracking, reporting |
| Recruiting / vetting refresh allocation | 35 000 | постоянное обновление пула |
| Security / compliance / audit allocation | 30 000 | controlled workflows |
| Support / client reporting | 20 000 | weekly review, incident handling |
| Onboarding amortization | 35 000 | spread one-off setup over 20 мес |
| **Итого COGS** | **735 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **1 200 000 ₽**
- COGS на клиента: **735 000 ₽**
- Gross profit на клиента: **465 000 ₽**
- **Gross Margin = 38,8%**

### Комментарий
Для чистого SaaS маржа слабая, но для managed expert operations это нормально. Экономика держится не на софте, а на orchestration premium поверх дорогого человеческого supply.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|
| Founder network / warm intros | 16 | 7 | 3 | 1.0 | 6,3% |
| Targeted outbound enterprise | 90 | 10 | 3 | 0.7 | 0,8% |
| Partnerships / integrators | 12 | 5 | 2 | 0.5 | 4,2% |
| Content / events / thought leadership | 20 | 4 | 1 | 0.2 | 1,0% |
| **Итого blended** | **138** | **26** | **9** | **2,4** | **1,7%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Founder + AE + SDR attributed compensation | 1 250 000 | new biz allocation |
| Marketing / content / events | 420 000 | нишевые enterprise-активности |
| Tools / CRM / enrichment / outreach | 180 000 | sales stack |
| Pilot presales burn not reimbursed | 760 000 | sample tasks, scoping, QA |
| Overhead multiplier | 570 000 | admin, ops, management |
| **Итого acquisition spend** | **3 180 000** |  |

- New paying customers / мес: **2,4**
- **Blended fully-loaded CAC = 3 180 000 / 2,4 = 1 325 000 ₽**

### Вывод
CAC высокий, но для high-ticket enterprise service с дорогим presales это реалистично. Если реальный funnel окажется хуже и новых клиентов будет не 2,4, а 1,5 в месяц, CAC быстро уходит выше 2 млн ₽.

## 5. LTV и churn

### База
- MRR на клиента: **1 200 000 ₽**
- ARR на клиента: **14 400 000 ₽**
- Gross Margin: **38,8%**
- Annual logo churn: **18%**

`LTV = ARR × GM / churn`

`LTV = 14 400 000 × 38,8% / 18% = 31 040 000 ₽`

### Stress-case
- Effective GM: **32%**
- Annual churn: **28%**

`Stress LTV = 14 400 000 × 32% / 28% = 16 457 000 ₽`

### Вывод
Даже stress-case остаётся высоким за счёт большого чека. Но это работает только если клиент не воспринимает поставщика как заменяемое агентство.

## 6. LTV / CAC

- Base LTV: **31,0 млн ₽**
- Stress LTV: **16,5 млн ₽**
- CAC: **1,325 млн ₽**

### Результат
- **Base LTV/CAC = 23,4x**
- **Stress LTV/CAC = 12,4x**

### Интерпретация
Формально метрика выглядит очень сильной. Я не считаю это признаком лёгкого бизнеса, а скорее следствием того, что при удачном закрытии каждый клиент крупный и долго живёт. Практический риск здесь в другом: не в LTV, а в том, сколько таких клиентов реально можно добыть и удержать локально.

## 7. CAC Payback

### Revenue payback
`1 325 000 / 1 200 000 = 1,1 мес`

### Gross profit payback
`1 325 000 / 465 000 = 2,85 мес`

### Комментарий
На бумаге payback отличный, но это верно только если клиент быстро доходит до full recurring scope. Если 2-3 месяца идут как узкий пилот на 400-600k ₽/мес, реальный payback будет ближе к **5-7 месяцам**.

## 8. Contribution Margin %

- Revenue per client / мес: **1 200 000 ₽**
- COGS: **735 000 ₽**
- Variable commission / success load: **55 000 ₽**

`Contribution profit = 410 000 ₽`

`Contribution Margin = 410 000 / 1 200 000 = 34,2%`

### Вывод
Contribution Margin рабочая. Она подтверждает, что бизнес может стать прибыльным, но не при маленьком чеке и не при ручном хаотичном delivery.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / CEO | 1 | 700 000 | 0 | 0 | 210 000 | 910 000 |
| GTM lead / AE | 1 | 350 000 | 1,5 | 2 | 105 000 | 455 000 |
| SDR / research | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| Program manager | 2 | 260 000 | 1 | 1,5 | 78 000 | 676 000 |
| QA / human data lead | 2 | 300 000 | 1,5 | 2 | 90 000 | 780 000 |
| Recruiter / expert ops | 2 | 220 000 | 1 | 1 | 66 000 | 572 000 |
| Platform ops / analyst | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Backend / platform engineer | 2 | 380 000 | 2 | 2 | 114 000 | 988 000 |
| ML / workflow engineer | 1 | 480 000 | 2,5 | 2 | 144 000 | 624 000 |
| Finance / legal ops | 0,5 | 140 000 | 1 | 1 | 42 000 | 182 000 |
| **Итого** | **13,5** |  |  |  |  | **5 733 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 5 733 000 |
| Core infra not in COGS | 420 000 |
| Admin / бухгалтерия / legal / ЭДО | 170 000 |
| Office / travel / enterprise meetings | 220 000 |
| Buffer на compliance / hiring friction | 257 000 |
| **Итого fixed costs** | **6 800 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **410 000 ₽**
- Fixed costs: **6 800 000 ₽/мес**

`Break-even clients = 6 800 000 / 410 000 = 16,6`

С учётом execution slippage округляю до **18-21 клиентов**.

### Проверка на 50 клиентов
- Revenue: `50 × 1 200 000 = 60 000 000 ₽/мес`
- COGS: `50 × 735 000 = 36 750 000 ₽/мес`
- Gross profit: **23 250 000 ₽/мес**
- Variable commissions / success load: `50 × 55 000 = 2 750 000 ₽/мес`
- Contribution profit: **20 500 000 ₽/мес**
- Fixed costs: **6 800 000 ₽/мес**
- **EBITDA = 13 700 000 ₽/мес**

### Вывод
Profit gate проходит, если удерживается high-ticket managed-service positioning.

## 12. Burn-to-breakeven

### Base case
- Fixed costs: **6,8 млн ₽/мес**
- Acquisition spend: **3,18 млн ₽/мес**
- Total pre-scale burn: **~9,98 млн ₽/мес**

Если набор клиентов идёт так:
- M1-M3: 1 клиент/мес
- M4-M6: 1,5 клиента/мес
- M7-M12: 2 клиента/мес

то к концу M12 можно выйти примерно на **18 клиентов**, то есть подойти к breakeven только к концу первого года.

### Burn-to-breakeven
Суммарно до устойчивого operating break-even проекту потребуется порядка **80-95 млн ₽**.

## 13. Основные экономические риски
1. **Supply-side moat дорогой**: screening и удержание экспертов могут съесть маржу.
2. **Founder bottleneck**: без сильного founder-led motion ранний funnel может схлопнуться.
3. **Риск agency economics**: если клиенты будут покупать разовые проекты вместо recurring program, модель ухудшится.
4. **Низкая локальная плотность buyers**: теоретический высокий LTV бесполезен, если pipeline слишком узкий.
5. **Security/compliance friction** в sensitive domains может удлинять цикл сделки на месяцы.

## 14. Profit Gate

### Проверка правила
- `company EBITDA < 500K/mo achievable even at 50 clients` → **нет, не нарушено**
- `LTV/CAC < 1:1` → **нет, не нарушено**

### Итог
На уровне P5 кейс **проходит**, но только в конфигурации high-ARPA managed expert operations. В low-end сценарии, похожем на обычную разметку или staffing, он быстро теряет инвестиционную привлекательность.

## Итоговый вердикт P5

**CONDITIONAL PASS.**

Кейс экономически жизнеспособен как узкий GEO-EXPAND оператор для enterprise AI-команд. Но он остаётся execution-heavy и зависит от редкого сочетания трёх факторов: дорогих клиентов, устойчивого expert supply и дисциплины в productization. Для фонда это пока не clean investment-grade asset, но как следующий шаг пайплайна кейс можно двигать дальше.

## Источники
- 02-demand.md по кейсу micro1-human-data-geo-expand-v2.
- micro1 homepage: https://www.micro1.ai/
- micro1 AI Labs / data engine: https://www.micro1.ai/data-engine/ai-labs
- TechCrunch, 2025-12-04, Micro1 crossed $100M ARR: https://techcrunch.com/2025/12/04/micro1-a-scale-ai-competitor-touts-crossing-100m-arr/
- Salary / hiring levels по РФ 2026: модельные допущения branch-models-lead, согласованные с обычными hh.ru диапазонами для Москвы/СПб.


<!-- SOURCE: 05-critic.md -->

## SECTION A — PnL

### Принятые допущения
- ARPA / MRR на клиента: **1 200 000 ₽/мес**.
- COGS на клиента: **735 000 ₽/мес**.
- Gross profit на клиента: **465 000 ₽/мес**.
- Gross Margin: **38.8%**.
- Contribution profit на клиента: **410 000 ₽/мес**.
- Fixed costs: **6 800 000 ₽/мес**, включая FOT **5 733 000 ₽/мес**.
- Страховые взносы: **~30% к ФОТ**, уже учтены в fully-loaded FOT.
- Annual churn: **18%**, в модели разложен в monthly churn **1.64%**.
- Сценарии отличаются только скоростью net new client additions, pricing и cost stack без изменений.

### Базовый сценарий
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1.0 | 1.0 | 1.0 | 1.5 | 1.5 | 1.5 | 2.0 | 2.0 | 2.0 | 2.0 | 2.0 | 2.0 |
| Total clients | 1.0 | 2.0 | 3.0 | 4.4 | 5.8 | 7.2 | 9.1 | 11.0 | 12.8 | 14.6 | 16.3 | 18.1 |
| MRR | 1 200 000 | 2 380 318 | 3 541 277 | 5 283 195 | 6 996 542 | 8 681 787 | 10 939 392 | 13 159 969 | 15 344 125 | 17 492 457 | 19 605 553 | 21 683 991 |
| COGS | 735 000 | 1 457 945 | 2 169 032 | 3 235 957 | 4 285 382 | 5 317 595 | 6 700 378 | 8 060 481 | 9 398 276 | 10 714 130 | 12 008 401 | 13 281 444 |
| Gross profit | 465 000 | 922 373 | 1 372 245 | 2 047 238 | 2 711 160 | 3 364 193 | 4 239 015 | 5 099 488 | 5 945 848 | 6 778 327 | 7 597 152 | 8 402 546 |
| GM% | 38.8% | 38.7% | 38.7% | 38.8% | 38.7% | 38.7% | 38.7% | 38.8% | 38.7% | 38.8% | 38.8% | 38.8% |
| Fixed costs | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 |
| EBITDA | -6 335 000 | -5 877 627 | -5 427 755 | -4 752 762 | -4 088 840 | -3 435 807 | -2 560 985 | -1 700 512 | -854 152 | -21 673 | 797 152 | 1 602 546 |
| Cash burn | 6 335 000 | 5 877 627 | 5 427 755 | 4 752 762 | 4 088 840 | 3 435 807 | 2 560 985 | 1 700 512 | 854 152 | 21 673 | 0 | 0 |
| Cumulative cash | -6 335 000 | -12 212 627 | -17 640 382 | -22 393 144 | -26 481 984 | -29 917 791 | -32 478 777 | -34 179 289 | -35 033 441 | -35 055 114 | -34 257 962 | -32 655 415 |
- Break-even по client count, gross basis: **14.6 клиента**.
- Break-even по client count, contribution basis: **16.6 клиента**, practically **17-21 клиентов**.
- Break-even по месяцам: **M11**.
- Startup capital to BE: **35 055 114 ₽**.

### Оптимистичный сценарий
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1.5 | 1.5 | 2.0 | 2.0 | 2.0 | 2.5 | 2.5 | 2.5 | 3.0 | 3.0 | 3.0 | 3.0 |
| Total clients | 1.5 | 3.0 | 4.9 | 6.8 | 8.7 | 11.1 | 13.4 | 15.7 | 18.4 | 21.1 | 23.8 | 26.4 |
| MRR | 1 800 000 | 3 570 477 | 5 911 916 | 8 214 951 | 10 480 213 | 13 308 321 | 16 090 043 | 18 826 141 | 22 117 362 | 25 354 603 | 28 538 747 | 31 670 666 |
| COGS | 1 102 500 | 2 186 917 | 3 621 048 | 5 031 657 | 6 419 130 | 8 151 346 | 9 855 151 | 11 531 011 | 13 546 884 | 15 529 694 | 17 479 983 | 19 398 283 |
| Gross profit | 697 500 | 1 383 560 | 2 290 867 | 3 183 293 | 4 061 082 | 5 156 974 | 6 234 892 | 7 295 130 | 8 570 478 | 9 824 909 | 11 058 764 | 12 272 383 |
| GM% | 38.8% | 38.8% | 38.8% | 38.8% | 38.7% | 38.8% | 38.8% | 38.8% | 38.8% | 38.7% | 38.8% | 38.8% |
| Fixed costs | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 |
| EBITDA | -6 102 500 | -5 416 440 | -4 509 133 | -3 616 707 | -2 738 918 | -1 643 026 | -565 108 | 495 130 | 1 770 478 | 3 024 909 | 4 258 764 | 5 472 383 |
| Cash burn | 6 102 500 | 5 416 440 | 4 509 133 | 3 616 707 | 2 738 918 | 1 643 026 | 565 108 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash | -6 102 500 | -11 518 940 | -16 028 073 | -19 644 779 | -22 383 697 | -24 026 723 | -24 591 831 | -24 096 701 | -22 326 223 | -19 301 315 | -15 042 550 | -9 570 167 |
- Break-even по client count, gross basis: **14.6 клиента**.
- Break-even по client count, contribution basis: **16.6 клиента**, practically **17-21 клиентов**.
- Break-even по месяцам: **M8**.
- Startup capital to BE: **24 591 831 ₽**.

### Пессимистичный сценарий
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.5 | 0.5 | 0.5 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 | 1.5 | 1.5 | 1.5 | 1.5 |
| Total clients | 0.5 | 1.0 | 1.5 | 2.5 | 3.4 | 4.4 | 5.3 | 6.2 | 7.6 | 9.0 | 10.3 | 11.7 |
| MRR | 600 000 | 1 190 159 | 1 770 639 | 2 941 597 | 4 093 350 | 5 226 213 | 6 340 495 | 7 436 501 | 9 114 530 | 10 765 038 | 12 388 474 | 13 985 283 |
| COGS | 367 500 | 728 972 | 1 084 516 | 1 801 728 | 2 507 177 | 3 201 055 | 3 883 553 | 4 554 857 | 5 582 650 | 6 593 586 | 7 587 940 | 8 565 986 |
| Gross profit | 232 500 | 461 187 | 686 122 | 1 139 869 | 1 586 173 | 2 025 158 | 2 456 942 | 2 881 644 | 3 531 880 | 4 171 452 | 4 800 534 | 5 419 297 |
| GM% | 38.8% | 38.7% | 38.7% | 38.8% | 38.8% | 38.7% | 38.7% | 38.8% | 38.7% | 38.8% | 38.8% | 38.8% |
| Fixed costs | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 | 6 800 000 |
| EBITDA | -6 567 500 | -6 338 813 | -6 113 878 | -5 660 131 | -5 213 827 | -4 774 842 | -4 343 058 | -3 918 356 | -3 268 120 | -2 628 548 | -1 999 466 | -1 380 703 |
| Cash burn | 6 567 500 | 6 338 813 | 6 113 878 | 5 660 131 | 5 213 827 | 4 774 842 | 4 343 058 | 3 918 356 | 3 268 120 | 2 628 548 | 1 999 466 | 1 380 703 |
| Cumulative cash | -6 567 500 | -12 906 313 | -19 020 191 | -24 680 322 | -29 894 149 | -34 668 991 | -39 012 049 | -42 930 405 | -46 198 525 | -48 827 073 | -50 826 539 | -52 207 242 |
- Break-even по client count, gross basis: **14.6 клиента**.
- Break-even по client count, contribution basis: **16.6 клиента**, practically **17-21 клиентов**.
- Break-even по месяцам: **не достигнут в горизонте 12 месяцев**.
- Startup capital to BE: **52 207 242 ₽**.

### Waterfall на 1 клиента в месяц
- ARPA: **1 200 000 ₽**.
- Gross profit: **465 000 ₽** = 1 200 000 - 735 000.
- Contribution profit: **410 000 ₽** после variable success / sales load **55 000 ₽** на клиента.
- EBITDA на client-equivalent fixed allocation при company break-even: **около 0 ₽** на уровне **16,6 клиента по gross basis** или **17-21 клиентов по contribution basis**.
- Net after tax при положительной прибыли на 1 клиенте до fixed allocation:
  - **УСН 6%**: **338 000 ₽**.
  - **IT-льгота 3%**: **374 000 ₽**.
  - **ОСНО 20% на прибыль**: **328 000 ₽**, при этом **НДС 20%** добавляется к счёту при применимости, но не считается доходом PnL.

### Налоговая модель РФ
- **УСН 6%**: налог с выручки, ориентир **72 000 ₽ на клиента в месяц**.
- **IT-льгота / аккредитация Минцифры**: ориентир **3% с выручки**, то есть **36 000 ₽ на клиента в месяц**.
- **ОСНО**: налог на прибыль **20%** с положительной базы, плюс **НДС 20%** к реализации если нет льгот/освобождений.
- **Страховые взносы ~30% к ФОТ** уже включены в fully-loaded FOT **5 733 000 ₽/мес** и в fixed costs **6 800 000 ₽/мес**.

### Вывод по cash flow
- Базовый сценарий требует около **35,1 млн ₽** стартового капитала до operating break-even.
- Оптимистичный сценарий требует около **24,6 млн ₽**.
- Пессимистичный сценарий не выходит на EBITDA break-even за 12 месяцев и требует не менее **52,2 млн ₽** на покрытие burn в рассматриваемом горизонте.

<!-- P6A-DONE -->

## SECTION B — Finance Risk + Competitor

### 1) Sensitivity analysis: EBITDA через 12 мес

База взята из SECTION A. Для Sens1 предполагаю, что при CAC x2 объём новых платящих клиентов за тот же sales budget падает примерно в 2 раза. Для Sens2 удваиваю monthly churn с 1,64% до 3,28%. Для Sens3 снижаю цену на 30% при неизменном cost stack.

| Scenario | Допущение | Clients @M12 | EBITDA @M12, ₽/мес |
|---|---|---:|---:|
| Base | как в модели P6A | 18,1 | 1 602 546 |
| Sens1 | CAC x2 | 9,0 | -2 598 696 |
| Sens2 | Churn x2 | 16,8 | 999 180 |
| Sens3 | Price -30% | 18,1 | -4 902 637 |

Вывод: модель особенно хрупкая к price compression и ухудшению acquisition efficiency. Сам churn болезненный, но не убивает бизнес мгновенно, если сохраняется high-ticket pricing.

### 2) Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 1 000 000 | 1 325 000 | 2 200 000 | P5 funnel + blended CAC [T1] |
| Monthly churn % | 1,0% | 1,64% | 3,3% | P5/P6A base + stress uplift [T1] |
| ARPU ₽/мес | 840 000 | 1 200 000 | 1 500 000 | P5 pricing band, base 1,2 млн ₽ [T1] |
| Conversion rate lead→paid % | 1,0% | 1,7% | 3,0% | P5 blended funnel 1,7% и улучшение от partner motion [T1] |
| Time-to-hire месяцев | 1,0 | 1,5 | 3,0 | P5 hiring table, роли 1,0-2,5 мес [T1] |

Ниже упрощённая Monte Carlo Lite: вместо 1000 прогонов использую 9 комбинаций вокруг min/mode/max для CAC, churn и ARPU, а conversion/time-to-hire применяю как qualitative modifiers для runway и execution risk.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | -4 320 000 | 10 300 000 | 24 920 000 | 29 240 000 |
| CAC payback (мес) | 21,0 | 2,85 | 1,31 | 19,69 |
| LTV/CAC | 4,8x | 21,4x | 23,2x | 18,4x |
| Cash runway (мес) | 5,2 | 5,5 | 6,1 | 0,9 |

Правила gate:
- **p10 EBITDA < 0, правило сработало.** Это автоматически создаёт kill criterion #1, риск неплатёжеспособности при неблагоприятном наборе CAC/ARPU/churn.
- **p50 EBITDA > 500k ₽/мес, правило пройдено.** Median-сценарий всё ещё проходит EBITDA gate.
- **p90/p10 как ratio некорректен из-за отрицательного p10.** Но сам факт перехода знака уже означает очень высокую неопределённость, score надо даунгрейдить на 1 ступень.
- **Range width по LTV/CAC = 18,4x > 8x.** Модель хрупкая, особенно к pricing и CAC.

### 3) Competitor deep-dive

Ниже не только exact peers, но и ближайшие substitutes в сегменте managed human data, expert labor orchestration и enterprise model-evals. Доли рынка, где нет публичного аудита, даны как **грубая оценка по выручке, публичной видимости и числу enterprise accounts**, а не как официальный market share.

#### Западные

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Scale AI | Доминантный бренд в data/evals для frontier AI, сильный гос и enterprise channel, широкий стек от data labeling до evals и agents [T2][T3] | Очень крупный и дорогой vendor, длинный onboarding, слабее fit для кастомного RU/CIS secure delivery | 35-45% глобального high-end data/evals peer-set | Мы можем быть дешевле, быстрее и локальнее в finance/legal-sensitive контурах РФ/СНГ |
| Mercor | Сильный expert-supply motion, мощный fundraising, явно продаёт доменных экспертов для model training [T4] | Больше похож на talent/expert marketplace, чем на full managed delivery layer; риск commoditization | 10-15% | Мы можем продавать не талант как таковой, а SLA-managed human data operations под конкретный workflow |
| Surge AI | Сильная репутация по high-quality RLHF/data labeling, хорошая маржа и качество [T5] | Низкая публичность, зависимость от узкого high-end сегмента, ограниченная локальная доступность | 8-12% | Мы можем выиграть на локальной интеграции, compliance и white-glove сервисе на русском языке |

#### Российские и локальные substitutes

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Toloka | Самый узнаваемый российский player в data labeling / human-in-the-loop, сильная платформа и community [T6][T7] | Сильнее в mass annotation, чем в boutique expert-data ops для frontier/post-training кейсов | 25-35% локального рынка human-data tooling | Мы можем быть более high-touch и domain-expert-heavy, а не marketplace-first |
| Biорг | Крупный российский поставщик разметки данных и CV/NLP dataset ops, enterprise track-record [T8] | Ближе к classic annotation vendor, ниже product moat в expert evals | 8-12% | Мы делаем ставку на evals, RLHF, red-teaming и expert QA, а не только на разметку |
| NLab / Наносемантика | Сильна в conversational AI и labelled-data workflows, присутствует в РФ enterprise AI [T9] | Неочевидный pure-play именно в managed expert data ops, больше adjacency | 5-8% | Более узкий и понятный wedge под enterprise post-training и human-data governance |
| Smartengines / VisionLabs / похожие vertical AI vendors | Есть enterprise доступ и доверие в regulated verticals, могут закрывать часть бюджета как substitute [T10] | Их core не в orchestration внешних доменных экспертов и не в general-purpose human data engine | 3-7% | Мы не vertical tool, а операционный слой поверх AI-команд и интеграторов |

Итог по конкурентам: на Западе рынок уже валидирован и занят крупными игроками, но в РФ exact-peer density пока низкая. Это плюс для раннего входа, но одновременно минус, потому что education burden ложится на нас.

### 4) Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder bottleneck в enterprise sales | high | high | >70% SQL и 100% closing завязаны на founder | Нанять AE, формализовать sales playbook, ограничить кастомные сделки |
| Operational | Неуспех найма QA lead / expert ops | med | high | time-to-hire > 2,5 мес, offer acceptance < 50% | Завести bench, referral program, pre-vetted expert pool |
| Operational | Срыв качества delivery у экспертного пула | med | high | QA reject rate > 8%, SLA breaches > 2 в мес | Двухуровневый QA, gold tasks, reviewer calibration |
| Operational | Зависимость от внешних LLM API / eval stack | high | high | рост API cost > 25%, latency spikes, vendor outages | Multi-vendor routing, local fallback, off-line review workflows |
| Market | Спрос в РФ остаётся нишевым и не масштабируется | med | high | pipeline < 3 enterprise pilots в квартал | Продавать через integrators и vertical-specific wedges |
| Market | Price compression со стороны annotation vendors | high | high | win rate падает, скидки > 20% становятся нормой | Упаковать security + governance + expert SLA, не продавать commodity hours |
| Market | Сильный западный конкурент входит через партнёров | med | med | клиенты начинают сравнивать с Scale/Toloka/Surge на RFP | Локальный compliance moat, быстрый pilot, русскоязычный delivery |
| Regulatory | 152-ФЗ и data residency режут часть use cases | high | high | security review > 60 дней, запрет на cross-border data flow | On-prem / sovereign hosting, data minimization, сегментация данных |
| Regulatory | 115-ФЗ / KYC и договорный контур для выплат экспертам | med | med | задержки выплат, bank compliance flags | Белая payroll-модель, агентские договоры, KYC process |
| Regulatory | Санкции SaaS и отключение западных сервисов | high | high | блокировки billing, потеря доступа к SaaS vendors | Дублировать критический стек на российских или self-hosted решениях |
| Financial | Cash runway оказывается < 6 мес | high | high | burn > 6 млн ₽/мес без роста выручки | Жёсткий hiring freeze, raise/bridge заранее, stage-gated spend |
| Financial | Ослабление рубля к USD повышает infra и API costs | med | med | USD/RUB > +15% к плану | FX buffer, рублёвые контракты, пересмотр pricing quarterly |
| Financial | Инфляция зарплат в AI-ролях | high | med | offers растут быстрее 15% YoY | Больше variable comp, региональный hiring, automation в ops |
| Financial | Налоговая нагрузка выше плановой | med | med | не получена льгота, effective tax rate > план | Проверка структуры юрлица, сценарное налоговое моделирование |
| Black swan | Новые санкции или эскалация войны режут enterprise spending | med | high | frozen budgets, отмена пилотов | Фокус на resilient verticals, экспорт в дружественные рынки |
| Black swan | Полное отключение ключевого LLM-поставщика | med | high | официальный notice, резкое падение доступности API | Multi-model architecture, manual fallback, заранее протестированные альтернативы |

### 5) Kill conditions через 6 мес

1. **Median-quality insolvency risk:** p10 EBITDA @M24 остаётся < 0 и при этом cash runway < 6 мес.
2. **Commercial failure:** меньше 4 платящих recurring клиентов или MRR < 4,8 млн ₽ к концу M6.
3. **Unit economics failure:** blended CAC > 2,2 млн ₽, либо win rate pilot→paid < 20%, либо price realization < 900k ₽/мес.

### 6) Короткий вывод

Кейс остаётся проходным только как high-ticket managed expert data ops. Если рынок выталкивает нас в commodity annotation pricing или CAC закрепляется выше ~2,2 млн ₽, экономика ломается уже в горизонте 6-12 месяцев. Сильная сторона кейса, редкий enterprise buyer и высокий потенциальный LTV. Слабая сторона, очень узкий рынок и высокая зависимость от execution.

## Источники SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/micro1-human-data-geo-expand-v2/04-economics.md и SECTION A текущего файла.
- [T2] Scale AI company / products: https://scale.com/
- [T3] Scale AI valuation and market position, Reuters, 2025-06-01: https://www.reuters.com/world/us/meta-talks-investment-scale-ai-that-could-top-10-billion-bloomberg-news-reports-2025-06-08/
- [T4] Mercor growth and model-training expert supply, TechCrunch, 2025-10-27: https://techcrunch.com/2025/10/27/mercor-quintuples-valuation-to-10b-with-350m-series-c/
- [T5] Surge AI positioning and economics, Reuters, 2024-03-13: https://www.reuters.com/technology/ai-data-labeling-startup-surge-raises-1-bln-valuation-2024-03-13/
- [T6] Toloka platform overview: https://toloka.ai/
- [T7] vc.ru о Toloka и рынке разметки данных: https://vc.ru/ai/
- [T8] Биорг, профиль и продукты разметки данных: https://biorg.ai/
- [T9] Наносемантика / NLab: https://nlabteam.com/ и https://habr.com/ru/companies/nanosemantics/
- [T10] Skolkovo AI landscape / local substitutes: https://sk.ru/

<!-- P6B-DONE -->


<!-- SOURCE: 06-verdict.md -->

[GEO-EXPAND] micro1 Human Data GEO Expand v2 — REJECTED: 64/100 | EBITDA base=1603К₽/мес через 12 мес | LTV/CAC=23,4x | Ключевое преимущество: high-ticket managed expert data ops для enterprise AI | Главный риск: рынок в РФ узкий, а delivery слишком human-heavy.

# 06-verdict

sector: GEO-EXPAND
status: REJECTED
normalized_score: 64/100
raw_score: 96/150
investment_committee_decision: REJECTED

## Investment one-liner
[GEO-EXPAND] micro1 Human Data GEO Expand v2 — REJECTED: 64/100 | EBITDA base=1603К₽/мес через 12 мес | LTV/CAC=23,4x | Ключевое преимущество: high-ticket managed expert data ops для enterprise AI | Главный риск: рынок в РФ узкий, а delivery слишком human-heavy.

## Итог инвесткомитета
**Вердикт: REJECTED.**

Почему не approve:
1. Unit economics на бумаге сильные, и base-case проходит EBITDA gate уже к M11-M12.
2. Но прямой спрос в РФ остаётся LOW, buyer universe ограничен несколькими enterprise AI-командами и интеграторами.
3. Moat средний: сильнее обычной разметки, но пока недостаточно жёсткий против Toloka, annotation vendors и service substitutes.
4. Finance-risk профиль остаётся слишком хрупким: при `Price -30%` EBITDA @M12 уходит в `-4 902 637 ₽/мес`, а p10 EBITDA @M24 остаётся отрицательной.
5. Это второй взгляд на категорию: относительно старого кейса `expert-human-data-ops-for-ai-models-operator-v2` новая версия лучше по economics, но всё ещё не дотягивает до investment-grade certainty.

## Оценка
Source tier balance: T1=3, T2=7, T3=1, weighted=2.18. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `Base LTV/CAC = 23,4x`, `Gross profit payback = 2,85 мес`, `Gross Margin = 38,8%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | `EBITDA = 1 602 546 ₽/мес` в M12 base и `13 700 000 ₽/мес` при 50 клиентах, но путь требует `18-21 клиентов`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 12 | `Exact-demand ... LOW`, но `SAM ≈ 1,08 млрд ₽/год` и `оценка моделей ИИ` даёт `HH vacancies 234`; применён штраф -2 за tier balance 2,18. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | `130 000+ vetted experts`, `100+ доменов`, `60+ языков` подтверждают operator thesis, но локально moat пока не hard-to-copy. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | `Founder bottleneck`, `152-ФЗ и data residency`, `санкции SaaS`, `зависимость от внешних LLM API` прямо перечислены в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | `blended fully-loaded CAC = 1 325 000 ₽`, `cycle сделки enterprise-консультативный`, но channel fit и 10 named targets понятны. |

**Normalized score = round((96 × 100) / 150) = 64/100.**

## Moat, 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных, это не marketplace с self-reinforcing liquidity в локальном GEO-EXPAND сценарии. |
| Switching costs | 2 | После настройки secure workflows, QA-рутин, reviewer calibration и managed expert pool смена поставщика болезненна. |
| Scale economies | 1 | Часть recruiting, QA и reporting стандартизируется, но человеческий supply остаётся дорогим. |
| Proprietary data / model advantage | 2 | `130 000+ vetted experts` и `100+ доменов` создают data advantage, но локальный размер и качество российского пула не доказаны отдельно. |
| Regulatory moat | 1 | Compliance и safe delivery важны, но формальный лицензируемый барьер невысок. |
| Brand / distribution | 1 | Глобальный signal micro1 силён, но в РФ локальный trust-brand и каналы дистрибуции ещё не собраны. |
| Embedded workflow | 3 | Если продукт заходит в evals, red-teaming и human QA, он может стать ежедневным операционным слоем AI-команды. |

Сумма 7-factor = **10/21**.
**Moat score = round((10 × 25) / 21) = 12/25.** Это не weak moat по формальному порогу, но для approve-grade защиты всё ещё недостаточно.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 31 040 000 ₽ |
| CAC fully-loaded | 1 325 000 ₽ |
| LTV/CAC | 23,4x |
| CAC payback | 2,85 мес |
| Gross Margin | 38,8% |
| contribution_margin_rub_month | 410 000 ₽ |
| company_ebitda_rub_month, base M12 | 1 602 546 ₽/мес |
| company_ebitda_potential_rub_month | 13 700 000 ₽/мес при 50 клиентах |
| Break-even clients | 18-21 |
| Break-even month | M11 |
| startup_capital_to_bep_rub | 35 055 114 ₽ |
| clients_to_500k_ebitda | 18 |
| months_to_500k_ebitda | 11 |
| clients_to_1m_ebitda | 19 |
| months_to_1m_ebitda | 12 |

## Полный business process (из 04-economics.md)

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping и shortlist ICP | SDR + founder | CRM, research, referrals | 2 ч | 4 000 | Низкий |
| 2 | Founder-led intro / outbound | Founder + SDR | email, Telegram, warm intros | 2 ч | 8 000 | Низкий |
| 3 | Discovery по use case и бюджету | Founder + AE | call, questionnaire | 1.5 ч | 10 000 | Низкий |
| 4 | Scoping human data workflow | Solutions lead + domain lead | template, workshop | 3 ч | 24 000 | Низкий |
| 5 | Security / compliance pre-check | Founder + ops | NDA, checklist | 2 ч | 9 000 | Низкий |
| 6 | Pilot design и sample task | PM + domain reviewer | platform, rubric, QA sheet | 6 ч | 42 000 | Средний |
| 7 | Paid / semi-paid pilot | PM + expert pool | managed execution | 20 ч | 130 000 | Низкий |
| 8 | Commercial negotiation | Founder + AE | pricing model, proposal | 3 ч | 18 000 | Низкий |
| 9 | Contract / procurement | AE + ops | ЭДО, договор, счёт | 4 ч | 16 000 | Средний |
| 10 | Production onboarding | PM + QA lead + platform ops | runbook, dashboard, SLA | 14 ч | 85 000 | Средний |

## Команда

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| Founder / CEO | продажи, partnerships, дизайн enterprise motion | 910 000 |
| GTM lead / AE | discovery, предложения, close | 455 000 |
| SDR / research | account mapping, outbound, enrichment | 234 000 |
| Program manager ×2 | delivery orchestration и account operations | 676 000 |
| QA / human data lead ×2 | QA, calibration, quality control | 780 000 |
| Recruiter / expert ops ×2 | supply-side sourcing и vetting | 572 000 |
| Platform ops / analyst | workflow tracking, dashboards | 312 000 |
| Backend / platform engineer ×2 | secure platform, data flows, tooling | 988 000 |
| ML / workflow engineer | eval tooling и workflow automation | 624 000 |
| Finance / legal ops 0,5 | контракты, выплаты, legal ops | 182 000 |
| **Итого** |  | **5 733 000 ₽/мес** |

## GTM, 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Яндекс Cloud / Yandex AI | У крупной AI-платформы есть постоянная боль в evals, red-teaming и human QA для LLM-продуктов, что совпадает с `model evaluation` и `human QA` тезисом кейса. | email decision-maker + профильные AI-конференции | 1 500 000 ₽/мес |
| 2 | Сбер / GigaChat | Сильный internal AI contour и regulated workflow повышают ценность secure expert-eval layer. | warm intro через enterprise AI ecosystem / конференция | 1 800 000 ₽/мес |
| 3 | Т-Банк | Быстрый AI-product cycle и чувствительность к качеству моделей в finance подходят под managed evaluators и domain experts. | email Head of AI / партнёрский заход | 1 500 000 ₽/мес |
| 4 | МТС AI | Публичный AI-вектор и enterprise-delivery motion создают спрос на scalable human-in-the-loop quality layer. | direct outbound + отраслевое мероприятие | 1 200 000 ₽/мес |
| 5 | VK / VK Predict | Большая ML-инфраструктура и много пользовательских AI-сценариев требуют red-teaming, annotation и model QA. | ABM outbound + vc.ru / Habr visibility touchpoint | 1 200 000 ₽/мес |
| 6 | Ростелеком / RTK AI | Гос и enterprise-проекты делают важными secure workflows и русскоязычный expert pool. | партнёрство с интегратором + email | 1 200 000 ₽/мес |
| 7 | ЦРТ | Речевая и conversational AI-экспертиза повышает спрос на domain evaluators и quality calibration. | email руководителю AI practice | 1 000 000 ₽/мес |
| 8 | IBS | Как крупный интегратор AI/данных, может покупать white-label expert operations под клиентские внедрения. | партнёрский заход через delivery practice | 900 000 ₽/мес |
| 9 | ЛАНИТ | Широкий enterprise AI-портфель и кастомные внедрения делают полезным white-label слой expert data ops. | partner outreach + конференция | 900 000 ₽/мес |
| 10 | GlowByte | Data/AI-интегратор с enterprise delivery может использовать managed expert pool для evals и domain QA у клиентов. | founder-led intro / email decision-maker | 800 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Влияние | Почему это top risk |
|---|---|---|---|
| Узкий локальный buyer universe и дорогой buyer education | Высокая | Высокое | `По exact-labels рынок в РФ пока не созрел`, поэтому GTM зависит от небольшого списка enterprise AI-команд. |
| Price compression и скатывание в agency economics | Высокая | Высокое | `Price -30%` даёт `EBITDA @M12 = -4 902 637 ₽/мес`, а рынок легко давит в staffing/annotation pricing. |
| Supply-side execution и зависимость от LLM / санкций | Высокая | Высокое | `screening и удержание экспертов`, `санкции SaaS`, `внешние LLM API` и `152-ФЗ` одновременно бьют по delivery. |

## Что нужно доказать для approve
1. Минимум 2 paid pilot у российских enterprise AI-команд или интеграторов из top-10 списка.
2. Реализуемый чек не ниже **1,0-1,2 млн ₽/мес** без сползания в staffing-only pricing.
3. Pilot-to-recurring conversion не ниже **30%** и retention не хуже заявленного base churn.
4. Локальный secure contour: data residency, on-prem/VPC или формально допустимый контур под 152-ФЗ.
5. Repeatable supply-side moat: подтверждённый bench доменных экспертов, QA reject rate <8% и понятная unit cost динамика.

## LTV Upside Calculator
Так как кейс получает **REJECTED**, нужен апсайд-калькулятор до near-pass / approve-grade.

### Базовая формула
`customer_ltv_rub = ARR × GM% / annual churn`

### Текущая база
- ARR = 14 400 000 ₽
- GM = 38,8%
- annual churn = 18%
- customer_ltv_rub = **31,0 млн ₽**

### Upside-сценарии
| Сценарий | ARR | GM | Churn | Новый LTV | Что это даёт |
|---|---:|---:|---:|---:|---|
| Base | 14 400 000 ₽ | 38,8% | 18% | 31,0 млн ₽ | Текущий rejected |
| Pricing discipline | 16 800 000 ₽ | 38,8% | 18% | 36,2 млн ₽ | Лучше запас по EBITDA и payback |
| Better retention | 14 400 000 ₽ | 38,8% | 14% | 39,9 млн ₽ | Сильнее recurring-thesis |
| Better delivery mix | 14 400 000 ₽ | 45,0% | 18% | 36,0 млн ₽ | Меньше human-heavy pressure |
| Near-pass target | 16 800 000 ₽ | 45,0% | 14% | 54,0 млн ₽ | Даёт запас для score 65+ |
| Approve-grade target | 18 000 000 ₽ | 50,0% | 12% | 75,0 млн ₽ | Нужен реальный moat, а не только высокая цена |

## Proof points, которые уже есть
1. `TechCrunch ... $100+ млн ARR` подтверждает глобальный category proof.
2. `130 000+ vetted experts`, `100+ доменов`, `60+ языков` показывают, что operator model может быть repeatable.
3. `Base LTV/CAC = 23,4x` и `EBITDA = 1 602 546 ₽/мес` к M12 доказывают, что экономика на high-ticket конфигурации жива.
4. `p50 EBITDA @M24 = 10 300 000 ₽/мес` показывает, что median-case не мёртв.

## Delta vs previous
Это rerun-кейс. Относительно старого `expert-human-data-ops-for-ai-models-operator-v2` вывод улучшился по экономике и формализованному EBITDA potential, но финальный статус остался отрицательным: рынок РФ всё ещё слишком узкий, а moat и GTM не набрали approve-grade margin of safety.

## Финальное решение
**REJECTED.**

Кейс имеет смысл возвращать в пайплайн только если появятся:
- 1-2 оплаченных enterprise design partner,
- подтверждённый secure delivery contour,
- удержание high-ticket pricing без price compression,
- и repeatable supply-side moat, а не просто доступ к фрилансерам.


<!-- SOURCE: 07-score-trajectory.md -->

## 2026-04-21 00:38 MSK — P4 Demand Validation
- Этап: P4 Demand Validation
- Итог: PASS WITH RESERVATIONS.
- Ключевой вывод: exact-demand в РФ по `human data operations`, `AI trainers` и `model evaluation services` остаётся LOW, но adjacent demand по `оценка моделей ИИ` и `разметка данных для ИИ` уже существует.
- Изменение оценки: умеренно позитивное по monetization thesis и умеренно негативное по ширине рынка.
- Артефакт: `pipeline/cases/micro1-human-data-geo-expand-v2/02-demand.md`

## 2026-04-23 02:04 MSK — P5 Unit Economics
- Этап: P5 Unit Economics
- Итог: CONDITIONAL PASS.
- Ключевой вывод: при MRR 1,2 млн ₽, COGS 735 тыс. ₽ и contribution 410 тыс. ₽ экономика проходит EBITDA gate, но требует 18-21 клиента для устойчивого break-even.
- Изменение оценки: позитивное по unit economics и негативное по capital intensity и execution load.
- Артефакт: `pipeline/cases/micro1-human-data-geo-expand-v2/04-economics.md`

## 2026-04-23 13:24 MSK — P7 Critic and Verdict
- Этап: P7 Critic and Verdict
- Итог: REJECTED, 64/100.
- Ключевой вывод: глобальный category proof и сильный LTV/CAC не компенсируют LOW direct demand в РФ, средний moat и хрупкость к price compression / supply-side risk.
- Изменение оценки: умеренно негативное, потому что сильная экономика не дотянула кейс до near-pass без более жёсткого local GTM proof.
- Артефакт: `pipeline/cases/micro1-human-data-geo-expand-v2/06-verdict.md`

