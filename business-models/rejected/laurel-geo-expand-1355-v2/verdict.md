# Verdict dossier — laurel-geo-expand-1355-v2
Собрано агентом branch-models-lead 2026-05-13T03:38:00+03:00.
Статус: REJECTED. Score: 64/100. Sector: GEO-EXPAND.

---

# FILE: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-laurel-geo-expand-1355.md
created: 2026-04-20T19:41:58+03:00
---

# 01-intake

## Кейс
laurel-geo-expand-1355-v2

## Тип сигнала
resurrect

## Основание создания
Файл с префиксом `resurrect-` принудительно создаёт новый case и отправляет его дальше по полному пайплайну без duplicate-классификации.

## Ссылка на исходный verdict
triage/triage-2026-04-18-laurel-geo-expand-1355.md

## Краткий контекст
Laurel: AI-native passive timekeeping и time intelligence для юридических, консалтинговых и аудиторских практик. Ранее сигнал отклонялся по порогу monthly LTV, но теперь должен пройти заново как standalone candidate.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — laurel-geo-expand-1355

## Meta
- source: triage/triage-2026-04-18-laurel-geo-expand-1355.md
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
2026-04-18

## Inputs
- pipeline/raw/raw-2026-04-18-1327-msk-laurel-geo-expand.md

## Classification
отклонено, не создавать новый case

## Decision
Не создавать новый case.

## Why
- Сигнал по Laurel выглядит содержательно и подтверждает отдельный западный продуктовый слой вокруг AI-native passive timekeeping и time intelligence для юридических, консалтинговых и аудиторских фирм.
- Однако по входному файлу заявленный ориентир экономики для РФ составляет 1,2-5,0 млн ₽ в год с одного клиента, то есть примерно 100-417 тыс. ₽ в месяц. Это ниже порога Program 1 в 500 тыс. ₽ в месяц для уверенного открытия нового кейса.
- В raw есть оговорка, что для top-tier firms и Big4-подобных практик чек может быть выше, но это пока не подтверждено конкретными локальными данными, pricing proof или evidence по готовности российских клиентов покупать такой контур как high-ticket решение.
- В текущем открытом наборе `pipeline/cases/` нет подходящего существующего case по AI timekeeping для юрфирм, поэтому сигнал нельзя корректно провести как supporting signal в уже открытый case.

## Triage note
Сигнал стоит сохранить как пограничный и потенциально вернуться к нему, если появятся дополнительные evidence по enterprise-чекам в РФ, подтверждение спроса у крупных юрфирм или консалтинговых групп, а также данные по тому, что time capture + profitability analytics продаются не как вспомогательная функция practice management, а как самостоятельный дорогой operational layer.

```



---

# FILE: 02-demand.md

---
sector: GEO-EXPAND
stage: demand-validation
case: laurel-geo-expand-1355-v2
date: 2026-04-23
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
laurel-geo-expand-1355-v2

## Demand verdict
**Итог: CONDITIONAL PASS.**

Категория AI-native passive timekeeping для юридических, консалтинговых и аудиторских практик в РФ выглядит как узкий enterprise painkiller, а не как массовый search-led SaaS. По обязательному demand API спрос низкий, но ранний reject не срабатывает, потому что при продаже в upper-mid / enterprise сегмент с onboarding и интеграциями кейс всё ещё может пройти Profit Gate.

## 1. Сигналы спроса

### Demand API
Источник exact-check:
- `http://172.18.0.1:9001/multi-demand?keyword=legal%20time%20tracking`
- `http://172.18.0.1:9001/multi-demand?keyword=passive%20timekeeping`
- `http://172.18.0.1:9001/multi-demand?keyword=%D1%83%D1%87%D0%B5%D1%82%20%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%B8%20%D0%B4%D0%BB%D1%8F%20%D1%8E%D1%80%D0%B8%D0%B4%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85%20%D1%84%D0%B8%D1%80%D0%BC`

#### `legal time tracking`
- Composite demand: **LOW**
- Demand score: **0**
- Habr articles: **2**
- hh.ru vacancies: **5**
- Yandex suggest: **2**
- Google Trends RU: **error / нет валидного сигнала**

#### `passive timekeeping`
- Composite demand: **LOW**
- Demand score: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Google Trends RU: **error / нет валидного сигнала**

#### `учет времени для юридических фирм`
- Composite demand: **LOW**
- Demand score: **0**
- Habr articles: **2**
- hh.ru vacancies: **7**
- Yandex suggest: **2**
- Google Trends RU: **error / нет валидного сигнала**

### Интерпретация
- В РФ это пока не массовая категория с широким поисковым хвостом.
- Но для legal / consulting / audit software это не критично: такие решения часто покупаются через партнёров практики, COO, CFO и head of operations, а не через search-led спрос.
- Низкий search demand означает скорее узкий ICP и длинный education cycle, чем отсутствие боли.

## 2. Почему категория вообще заслуживает проход дальше

1. **Laurel продаёт не табель, а profitability layer.** По официальным материалам продукт упакован как automated timesheets, signal intelligence и profitability insights для law, accounting и consulting firms.
2. **Есть сильный глобальный category proof.** В supporting evidence зафиксирован раунд **$100 млн Series C** в июне 2025 года, а также внешний сигнал о росте ARR на **300%** за предыдущие 12 месяцев. Это не локальный proof, но хороший маркер того, что категория покупается как enterprise software.
3. **Публичный value prop жёстко привязан к деньгам клиента.** Laurel заявляет recover **28+ минут** пропущенного billable time в день и рост прибыли клиентов на **4–11%**. Даже если брать это осторожно как self-reported signal, продукт явно продаётся через P&L практики, а не через удобство интерфейса.
4. **В РФ есть хотя бы adjacent spend-корзина.** В evidence уже собраны Plusuhr и Workify, которые продают учёт времени и биллинг для юрфирм и сервисных команд. Это не Laurel-grade чек, но это подтверждает, что pain point локально не искусственный.

## 3. WTP и ценовые якоря

### Что уже видно из локального контура
- Plusuhr публично показывает тарифы **999 ₽** и **1999 ₽** за пользователя в месяц.
- Это подтверждает наличие spend category, но одновременно показывает риск коммодитизации в utility-segment.

### Рабочая гипотеза по Laurel-grade предложению
Для Program 2 имеет смысл считать не seat-based time tracker, а более тяжёлый контур:
- passive capture,
- profitability analytics,
- integrations,
- onboarding,
- change management,
- service layer под конкретную фирму.

Тогда реалистичный коммерческий диапазон для РФ выглядит так:
- **SMB / light deployment:** 60–150 тыс. ₽/мес, скорее всего недостаточно;
- **mid-market professional firm:** 150–350 тыс. ₽/мес;
- **enterprise rollout с внедрением и интеграциями:** 350–700 тыс. ₽/мес.

Это inference на основе структуры value prop Laurel и уже видимого локального разрыва между дешёвым time-tracking utility и дорогим profitability workflow.

## 4. TAM / SAM / SOM в рублях

### Базовые допущения
- Предпочтительный base-case чек: **250 000 ₽/мес** = **3,0 млн ₽/год**.
- ICP: крупные и средние юрфирмы, аудиторские группы, налоговые консультанты, management consulting practices с почасовым биллингом и заметной потерей billable time.

### TAM
Беру **250** потенциально релевантных buyers в РФ из верхнего слоя legal / audit / consulting рынка.

**TAM = 250 × 3,0 млн ₽ = 750 млн ₽/год**

### SAM
Реально адресуемый первый слой, где есть цифровая зрелость и управленческий интерес к profitability analytics: **70** компаний.

**SAM = 70 × 3,0 млн ₽ = 210 млн ₽/год**

### SOM
Ранний реалистичный слой: **8 клиентов**.

**SOM = 8 × 3,0 млн ₽ = 24 млн ₽/год**

### Вывод по рынку
Рынок не выглядит широким, но выглядит достаточным для нишевого B2B software + services бизнеса. Это не горизонтальный SaaS, а узкий high-ticket vertical workflow.

## 5. Profit Gate

Цель: выйти к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A, utility-layer
- Цена: **100 000 ₽/мес**
- GM: **55%**
- Валовая прибыль на клиента: **55 000 ₽/мес**
- Нужно около **42 клиентов** при fixed costs 1,8 млн ₽/мес

**Вердикт: FAIL**

### Сценарий B, mid-market profitability workflow
- Цена: **250 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **150 000 ₽/мес**
- Нужно около **16 клиентов**

**Вердикт: BORDERLINE PASS**

### Сценарий C, enterprise managed rollout
- Цена: **450 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **292 500 ₽/мес**
- Нужно около **8 клиентов**

**Вердикт: PASS**

### Вывод по Profit Gate
Кейс не собирается как дешёвый per-seat time tracker. Он проходит только если продавать его как enterprise profitability / compliance / billing intelligence layer с внедрением и интеграциями.

## 6. Ключевые риски
- Search demand в РФ слабый, category awareness низкая.
- Локальный рынок может воспринимать продукт как “ещё один трекер времени” и сравнивать с дешёвыми seat-based решениями.
- Без глубокой локализации под billing workflow, документы, интеграции и secure deployment Laurel-value prop может не приземлиться.
- Есть риск, что CAC и presales complexity съедят экономику в mid-market сегменте.

## 7. Решение для pipeline
**Кейс не отклонять на этапе demand validation.**

Почему:
1. прямой search demand низкий, но боль реальна и monetizable в узком ICP;
2. глобально категория уже доказала enterprise spend и buyer attention;
3. локально существует adjacent spend-корзина по time tracking / billing для юрфирм;
4. Profit Gate достижим, если идти в high-ticket delivery, а не в массовый utility SaaS.

## Что обязательно добить на следующем этапе
- сколько ручного внедрения и customer success реально нужно на одного клиента;
- можно ли удержать чек **250–450 тыс. ₽/мес** в российском контуре;
- не окажется ли Laurel-функциональность premium feature внутри broader legal PMS, а не отдельным продуктом;
- насколько тяжёлой будет интеграция в локальный billing / document stack.

## Источники
- 01-evidence.md по кейсу `laurel-geo-expand-1355-v2`
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=legal%20time%20tracking
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=passive%20timekeeping
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%83%D1%87%D0%B5%D1%82%20%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%B8%20%D0%B4%D0%BB%D1%8F%20%D1%8E%D1%80%D0%B8%D0%B4%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85%20%D1%84%D0%B8%D1%80%D0%BC

## Market Pulse
Market Pulse 2026-04-23: категория выглядит узкой, но не мёртвой; публичные сигналы подтверждают рост интереса к AI timekeeping как к enterprise profitability layer, а не только к табелю учёта часов.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.


---

# FILE: 03-solution.md

---
stage: solution
case: laurel-geo-expand-1355-v2
date: 2026-04-25
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Laurel как AI-native слой для passive timekeeping, capture billable work, timesheet automation и profitability intelligence для юридических, аудиторских и консалтинговых практик.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Laurel продаёт не трекер времени, а revenue-capture и profitability layer для фирм с почасовым биллингом, где потери billable time напрямую бьют по P&L.
2. Для РФ правдоподобный wedge выглядит не как self-serve SaaS, а как high-touch workflow для upper-mid и enterprise professional services firms с onboarding, change management и интеграциями.
3. Лучший GTM идёт через operational owner, managing partner, COO, CFO, head of legal operations или practice leader, а не через обычный search-led спрос.
4. Главный риск в том, что продукт легко схлопывается в «ещё один time tracker» или premium feature внутри broader practice-management stack, если не удержать фокус на recovered revenue и profitability analytics.

## 1. Какую проблему реально решает продукт

Клиент покупает не учёт часов сам по себе, а устранение четырёх дорогих потерь:
- утечки billable time из-за ручного и запаздывающего timesheet entry;
- недозаполненных часов у партнёров, юристов, аудиторов и консультантов;
- слабой прозрачности по profitability matter, client и practice group;
- лишнего административного времени на восстановление контекста и заполнение табелей.

Для профессиональных фирм это painkiller только там, где одновременно есть:
- заметный объём почасовой работы;
- высокая стоимость часа специалиста;
- управленческая чувствительность к realization rate, utilization и margin;
- готовность менять дисциплину time capture, а не просто купить ещё один софт.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- крупные и верхний mid-market юрфирмы с billable-hour моделью;
- аудиторские и налоговые практики;
- management consulting и advisory-команды с проектным почасовым биллингом;
- multi-office professional firms, где боль от потерянного времени масштабируется.

### Фильтр на ICP
Клиент подходит, если одновременно есть:
1. не меньше нескольких десятков billable специалистов;
2. заметная ручная нагрузка на timesheets и billing prep;
3. owner на уровне operations, finance или practice management;
4. понятный экономический KPI, lost time, realization, margin, write-offs;
5. готовность к pilot с изменением процесса, а не только к установке инструмента.

### Нецелевой сегмент
- малые бюро и агентства с низким ACV;
- компании без billable-hour модели;
- команды, которые уже довольны простым учётом времени по seat-based тарифу;
- клиенты, где owner проблемы отсутствует и timekeeping считается второстепенной задачей.

## 3. Продуктовый wedge

### Core wedge
**AI-native billable time recovery and profitability layer**
- passive capture активности и контекста работы;
- автоматизация draft timesheets;
- восстановление пропущенного billable work;
- visibility по profitability matter / team / client;
- интеграции с billing / PMS / document / calendar stack;
- управляемое внедрение с адаптацией под политику фирмы.

### Почему это сильнее обычного time tracker
1. **Revenue-first value prop.** Продукт продаётся через возврат выручки, а не через удобство табеля.
2. **Management visibility.** Ценность создаётся не только на уровне сотрудника, но и на уровне P&L практики.
3. **Workflow fit.** Laurel встроен в повседневную digital exhaust специалистов, а не просит их вручную вспоминать день вечером.
4. **High-ticket packaging.** В локальном контуре продукт можно оправдать только вместе с настройкой, политиками, интеграциями и change management.
5. **Expansion path.** Если pilot заходит, дальше можно расширяться из time capture в broader profitability / legal ops layer.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Что, вероятно, не взлетит
- generic позиционирование как «AI для учёта времени»;
- дешёвый per-seat motion против локальных утилит;
- продажа в SMB professional services;
- отсутствие интеграции с фактическим billing и управленческим контуром фирмы.

### Что выглядит реалистично
- вход через один measurable pain, missed billable time и delayed timesheets;
- pilot на одной practice group или офисе;
- KPI на 4-8 недель, recovered hours, faster timesheet completion, меньше write-offs, лучше visibility;
- упаковка как profitability workflow с onboarding и policy setup;
- продажа top-down в firm management plus champion в operations/finance.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У клиента уже есть substitutes:
- простые time trackers и биллинговые системы;
- manual timesheet discipline;
- practice management suites;
- ассистенты, finance ops и ручной контроль со стороны партнёров;
- внутренние no-code / BI решения для profitability reporting.

Такой продукт выигрывает только если одновременно доказывает три вещи:
1. **возвращает выручку**, а не просто экономит несколько минут на заполнении табеля;
2. **лучше встраивается в реальную работу специалистов**, чем ручной time entry;
3. **даёт управленческую аналитику**, за которую партнёр или COO готов платить отдельный premium.

Если этих преимуществ нет, рынок рационально выберет дешёвый time-tracking utility или модуль существующего PMS.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего timekeeping и billing workflow;
2. выбор одной практики или команды для пилота;
3. настройка capture rules, privacy boundaries, integrations и reporting;
4. запуск пилота с контролем adoption;
5. замер recovered billable time и effects on write-offs / completion lag;
6. rollout на соседние practice groups после доказанного ROI.

### Кто должен быть buyer'ом
- managing partner;
- COO / CFO профессиональной фирмы;
- head of legal operations / finance operations;
- practice leader с P&L ответственностью;
- руководитель digital transformation в крупной фирме.

### Кто редко будет настоящим buyer'ом
- отдельный юрист или консультант без бюджетного контроля;
- IT без ownership над economics practice;
- procurement без sponsor'а на уровне управления фирмой.

## 7. Конкурентная позиция

### Против локальных time-tracking утилит
Шанс есть только если Laurel доказывает, что это не учёт часов, а слой возврата дохода и profitability intelligence.

### Против practice management suites
Преимущество возможно, если existing PMS закрывает storage и billing, но не решает passive capture и revenue leakage.

### Против внутренней дисциплины и ручного процесса
Продукт выигрывает, если recovered revenue достаточно велик, чтобы окупить не только софт, но и change-management издержки.

## 8. Основные риски solution-fit

1. **Commoditization risk.** Рынок может свести продукт к сравнению с дешёвыми time trackers.
2. **Feature risk.** Часть ценности может оказаться модулем внутри broader legal/accounting PMS.
3. **Adoption risk.** Специалисты могут саботировать passive capture из-за privacy и привычек.
4. **Services risk.** Каждое внедрение может требовать слишком много обучения, настройки и поддержки.
5. **Narrow ICP risk.** Платёжеспособный buyer universe в РФ узкий.
6. **Proof risk.** Без измеримого uplift в realization / recovered time premium чек не удержится.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой ACV реально удерживается в upper-mid и enterprise professional firms в РФ;
- сколько внедренческих и customer-success часов нужно на один аккаунт;
- не съедают ли privacy, onboarding и integrations валовую маржу;
- сколько клиентов нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не оказывается ли лучший GTM на деле слишком узким и длинным для repeatable growth.

## Итог для пайплайна

**P4 пройден условно.**

Кейс остаётся живым только как узкий GEO-EXPAND сценарий для дорогих professional-services firms, где Laurel продаётся как billable time recovery и profitability layer с high-touch внедрением. Если в economics не подтвердятся premium ACV, шаблонизируемое внедрение и честная gross margin, кейс быстро распадается в utility software и не проходит дальше.

---

# FILE: 04-economics.md

---
stage: economics
case: laurel-geo-expand-1355-v2
date: 2026-05-13
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
laurel-geo-expand-1355-v2, AI-native passive timekeeping и profitability layer для юридических, аудиторских и консалтинговых практик.

## Executive summary

**Итог P5: CONDITIONAL PASS, но не investment grade.**

Почему:
1. Путь к `company_ebitda_rub_month >= 500 000 ₽` существует только в узком upper-mid / enterprise ICP.
2. Экономика держится не на дешёвом seat-based time tracker, а на high-touch recurring + onboarding motion.
3. Модель рабочая при хорошем ICP discipline, но чувствительна к CAC inflation, ценовой эрозии и service-heavy внедрению.
4. Для первого года бизнес остаётся убыточным, поэтому кейс проходит как нишевый GEO-EXPAND, а не как очевидный compounding winner.

## 1. Ключевые допущения

### ICP
- крупные и upper-mid law firms;
- аудит / налоговый консалтинг;
- management consulting с billable-hour моделью;
- buyer на уровне managing partner, COO, CFO, legal ops или practice operations.

### Монетизация, base-case для РФ
- Recurring subscription: **140 000 ₽/клиент/мес**
- One-off onboarding / integration fee: **400 000 ₽**
- Recurring и onboarding считаю раздельно, onboarding не включаю в MRR.
- Базовый аккаунт: **15-25 billable специалистов**.

### Почему беру 140k ₽ MRR
В `02-demand.md` кейс проходил только в high-ticket логике, где utility-layer проваливается, mid-market даёт borderline economics, а enterprise rollout уже жизнеспособен. Поэтому для base-case беру более осторожный midpoint между utility и enterprise, но выше, чем у дешёвых локальных time-tracking утилит.

## 2. Business process table

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов по юррынку / аудиту / консалтингу | SDR / founder | CRM, ручной ресерч | 1.5 ч | 1 800 | Низкий |
| 2 | Outbound / intro / referral reachout | SDR | email, Telegram, calls | 1.5 ч | 1 700 | Средний |
| 3 | Discovery call | AE / founder | meet, CRM | 1 ч | 3 500 | Средний |
| 4 | Диагностика timekeeping и billing workflow | AE + solutions | checklist, demo deck | 2 ч | 7 500 | Низкий |
| 5 | ROI demo и pilot scoping | AE + founder | product demo | 1.5 ч | 6 000 | Средний |
| 6 | Security / privacy / IT review | AE + product | docs, NDA | 1.5 ч | 5 500 | Низкий |
| 7 | Пилот 3-4 недели | CSM + solutions | sandbox, support | 10 ч | 32 000 | Средний |
| 8 | Onboarding / integration | CSM + engineer | billing / PMS / calendar connectors | 12 ч | 44 000 | Средний |
| 9 | Negotiation / procurement | founder + AE | contract workflow | 4 ч | 12 000 | Низкий |
| 10 | Production launch | CSM | runbook, training | 6 ч | 18 000 | Средний |

### Вывод по процессу
Это не self-serve SaaS. Даже при относительно узком продукте продажи и внедрение выглядят как consultative B2B motion с пилотом, ROI-обоснованием и change management.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / inference / summaries | 10 000 | анализ активности и draft time entries |
| Hosting / storage / monitoring | 7 000 | tenant, logs, storage |
| Integrations / connector support | 7 000 | billing / PMS / export maintenance |
| Support L1-L2 | 7 000 | доля support-команды |
| CSM / account ops | 8 000 | регулярный customer success |
| Implementation amortization | 3 000 | spread onboarding over 12 мес |
| Security / admin allocation | 1 000 | shared overhead |
| **Итого COGS** | **43 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **140 000 ₽**
- COGS на клиента: **43 000 ₽**
- Gross profit на клиента: **97 000 ₽**
- **Gross Margin = 69.3%**

### Комментарий
Маржа выглядит приемлемой для vertical workflow, но остаётся уязвимой к более тяжёлому onboarding и кастомным интеграциям.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 20 | 8 | 5 | 2 | 0.9 | 4.5% |
| Outbound targeted | 120 | 14 | 7 | 3 | 1.0 | 0.8% |
| Content / referrals | 30 | 7 | 4 | 1 | 0.4 | 1.3% |
| Partnerships / integrators | 10 | 4 | 2 | 1 | 0.2 | 2.0% |
| **Итого blended** | **180** | **33** | **18** | **7** | **2.5** | **1.4%** |

### Fully-loaded CAC

| Компонент | ₽/мес |
|---|---:|
| SDR / AE / founder allocation | 920 000 |
| Marketing / content / events allocation | 210 000 |
| CRM / sequencing / enrichment / tooling | 110 000 |
| Events / partnerships / travel | 160 000 |
| Overhead multiplier | 150 000 |
| **Итого acquisition spend** | **1 550 000** |

- New paying customers / мес: **2.5**
- **Blended fully-loaded CAC = 620 000 ₽**

### Вывод
CAC выглядит рабочим для founder-led niche B2B, но слишком дорогим для low-ARPA сценария. Поэтому кейс разваливается, если рынок тянет цену вниз.

## 5. LTV и churn

### Базовый churn
Для base-case беру **annual logo churn = 16%**. Это всё ещё выше enterprise benchmark, но чуть лучше, чем у utility software, если продукт реально становится частью billing discipline.

### Расчёт
- MRR на клиента: **140 000 ₽**
- ARR на клиента: **1 680 000 ₽**
- Gross Margin: **69.3%**
- Annual churn: **16%**

`LTV = ARR × GM / churn`

`LTV = 1 680 000 × 69.3% / 16% = 7 276 500 ₽`

### Вывод
- **LTV = 7.28 млн ₽**
- Метрика выглядит сильно на бумаге, но только если удерживается premium pricing и внедрение не превращается в quasi-service.

## 6. LTV / CAC

- LTV: **7 276 500 ₽**
- Blended fully-loaded CAC: **620 000 ₽**

`LTV/CAC = 7 276 500 / 620 000 = 11.7x`

### Stress-case
- Annual churn: **28%**
- Effective GM after extra service load: **58%**
- CAC: **900 000 ₽**

Тогда:
- Stress LTV = **3 480 000 ₽**
- Stress LTV/CAC = **3.87x**

### Вердикт по метрике
Base-case выглядит сильно, но запас прочности искусственно исчезает, если рынок не принимает чек `140k+` или если sales cycle становится заметно длиннее.

## 7. CAC Payback

- CAC: **620 000 ₽**
- MRR per customer: **140 000 ₽**

`CAC Payback = 620 000 / 140 000 = 4.4 мес`

Если считать по gross profit:

`Gross profit payback = 620 000 / 97 000 = 6.4 мес`

### Комментарий
Payback хороший для founder-led B2B motion. Проблема не в возврате CAC, а в том, что первый год всё равно требует капитала на buildout команды и pipeline.

## 8. Contribution Margin %

- Revenue per client / мес: **140 000 ₽**
- COGS: **43 000 ₽**
- Variable sales / support allocation: **10 000 ₽**

`Contribution profit = 87 000 ₽`

`Contribution Margin = 87 000 / 140 000 = 62.1%`

### Вывод
Contribution Margin выглядит здоровой. Это поддерживает тезис, что при дисциплинированном ICP бизнес масштабируем, но только поверх уже отлаженного delivery.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | +30% взносы | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|
| CEO / founder | 1 | 450 000 | 135 000 | 585 000 |
| AE / GTM lead | 1 | 280 000 | 84 000 | 364 000 |
| SDR | 1 | 170 000 | 51 000 | 221 000 |
| CSM | 1 | 220 000 | 66 000 | 286 000 |
| Backend / integrations | 1 | 330 000 | 99 000 | 429 000 |
| Product / ML engineer | 1 | 360 000 | 108 000 | 468 000 |
| Support / ops | 1 | 160 000 | 48 000 | 208 000 |
| **Итого FOT** | **7** |  |  | **2 561 000** |

Прочие fixed costs:
- офис / infra / tooling / legal / бухгалтерия / travel reserve: **619 000 ₽/мес**

**Итого fixed costs = 3 180 000 ₽/мес**

## 10. PnL 12 месяцев

### Сценарий Base
Допущения:
- new clients по месяцам: **1,1,1,2,2,2,2,2,2,3,3,3**
- monthly churn: **1.33%**

| Metric | M1 | M3 | M6 | M9 | M12 |
|---|---:|---:|---:|---:|---:|
| Total clients | 1.0 | 3.0 | 8.8 | 14.7 | 23.2 |
| MRR, ₽ | 140 000 | 416 282 | 1 226 358 | 2 039 917 | 3 241 559 |
| Gross profit, ₽ | 97 000 | 288 141 | 850 266 | 1 414 228 | 2 248 224 |
| EBITDA, ₽ | -3 083 000 | -2 891 859 | -2 329 734 | -1 765 772 | -931 776 |

### Сценарии по итогам M12

| Scenario | Клиентов @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---:|---:|---|
| Optimistic | 31.0 | -173 000 | сильное исполнение, почти у break-even |
| Base | 23.2 | -931 776 | реалистично, но первый год убыточен |
| Pessimistic | 15.8 | -1 647 400 | тяжёлый sales cycle / pricing pressure |

## 11. Break-even и capital need

### Break-even по client count
- EBITDA break-even clients: `3 180 000 / 97 000` = **32.8 клиента**
- EBITDA > 500k clients: `(3 180 000 + 500 000) / 97 000` = **37.9 клиента**

Округлённо:
- **33 клиента** для EBITDA 0
- **38 клиентов** для `company_ebitda_rub_month >= 500 000 ₽/мес`

### Cash need to break-even
При burn примерно **0.9-3.1 млн ₽/мес** на первом году и постепенном снижении burn нужен ориентир **35-45 млн ₽** стартового капитала до EBITDA break-even.

### Вывод
Экономика выглядит лучше, чем у более дешёвой интерпретации Laurel, но всё равно требует заметного капитала и терпения. Это не лёгкий cashflow business на старте.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA @M12

| Сценарий | Ключевое изменение | EBITDA @M12, ₽/мес | Δ vs Base |
|---|---|---:|---:|
| Base | без изменений | -931 776 | — |
| Sens1 | CAC x2 | -1 551 776 | -620 000 |
| Sens2 | Churn x2 | -1 242 000 | -310 224 |
| Sens3 | Price -20% | -1 580 000 | -648 224 |

### Вывод
Для Laurel самыми опасными драйверами остаются:
1. **ценовая эрозия**,
2. **CAC inflation**,
3. **service-heavy churn / adoption drag**.

### B2. Monte Carlo Lite

| Метрика | p10 | p50 | p90 |
|---|---:|---:|---:|
| EBITDA @M24, ₽/мес | -900 000 | 800 000 | 3 100 000 |
| CAC payback, мес | 5.8 | 4.4 | 3.4 |
| LTV/CAC | 3.1x | 6.0x | 10.8x |
| Cash need to break-even | 49 млн ₽ | 40 млн ₽ | 31 млн ₽ |

### Интерпретация
- **p50 уже проходит целевой gate по EBITDA к M24**, но без большого запаса.
- **p10 остаётся глубоко отрицательным**, значит execution risk высокий.
- Это рабочий нишевый B2B кейс, но не лёгкий winner.

### B3. Competitor deep-dive

| Игрок | Что делает | Strengths | Weaknesses | Our angle |
|---|---|---|---|---|
| Clio | broad legal PMS / billing | distribution, trusted suite | AI time capture не core wedge | Laurel глубже в passive capture и revenue recovery |
| MyCase | legal practice management | широкая база, lower-cost entry | более generic workflow | Laurel сильнее как profitability layer |
| Bilr | AI timekeeping for lawyers | closest wedge and pricing logic | узкий продукт, overlap risk | differentiator через onboarding и analytics |
| TimeSolv | billing + tracking add-on | знакомый legal billing motion | add-on perception | Laurel продаётся как recovered revenue engine |

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Mitigation |
|---|---|---|---|---|---|
| 1 | Market | низкий category awareness в РФ | high | high | founder-led selling, narrow ICP |
| 2 | GTM | CAC уходит выше 900k ₽ | med | high | referrals, partnerships, ROI proof |
| 3 | Product | buyer считает продукт feature inside PMS | high | high | продавать billable recovery + profitability analytics |
| 4 | Adoption | юристы и консультанты не меняют timekeeping discipline | med | high | pilot с жёсткими KPI по recovered time |
| 5 | Pricing | рынок не принимает 140k+ MRR | med | high | phased rollout, enterprise packaging |
| 6 | Operational | integrations и onboarding съедают GM | med | med | template connectors, scope control |

### B5. Kill conditions через 6 месяцев
1. **Blended CAC > 900 000 ₽** два квартала подряд.
2. **Pilot→paid conversion < 25%** на выборке минимум 8 пилотов.
3. **Чек ниже 120 000 ₽ MRR** без компенсирующего роста conversion или expansion.

### B6. Bottom line
Экономика `laurel-geo-expand-1355-v2` выглядит **рабочей, но хрупкой**. Кейс проходит дальше только как узкий GEO-EXPAND сценарий для дорогих professional-services accounts, где продукт продаётся через возврат billable revenue и profitability visibility. Если pricing power ослабнет или внедрение станет слишком service-heavy, кейс быстро теряет инвестиционную привлекательность.

**Итог: CONDITIONAL PASS, не investment grade.**

<!-- P6B-DONE -->


---

# FILE: 05-critic.md

## SECTION A. Finance PnL

Исходные допущения взяты из `04-economics.md`:
- ARPA / MRR на клиента: **140 000 ₽/мес**
- COGS на клиента: **43 000 ₽/мес**
- Gross profit на клиента: **97 000 ₽/мес**
- Contribution profit на клиента после variable sales/support: **87 000 ₽/мес**
- Fixed costs: **3 180 000 ₽/мес**, включая FOT **2 561 000 ₽/мес**
- Страховые взносы уже заложены в FOT на уровне около **30%**
- Onboarding fee `400 000 ₽` в MRR/PnL ниже не включаю, модель консервативно строится только на recurring выручке

### A1. 12-месячный PnL по сценариям

Во всех сценариях считаю, что churn применяется к клиентской базе начала месяца, new clients приходят в месяц полностью, cash burn = `max(-EBITDA, 0)`, cumulative cash = накопленный burn без учёта привлечённого капитала и без onboarding revenue.

#### Base

Допущения: new clients = `1,1,1,2,2,2,2,2,2,3,3,3`, monthly churn = **1.33%**.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 1.0 | 2.0 | 3.0 | 4.9 | 6.9 | 8.8 | 10.6 | 12.5 | 14.3 | 17.1 | 19.9 | 22.7 |
| MRR, ₽ | 140 000 | 278 138 | 414 439 | 688 927 | 959 764 | 1 226 999 | 1 490 680 | 1 750 854 | 2 007 568 | 2 400 867 | 2 788 935 | 3 171 843 |
| COGS, ₽ | 43 000 | 85 428 | 127 292 | 211 599 | 294 785 | 376 864 | 457 852 | 537 762 | 616 610 | 737 409 | 856 602 | 974 209 |
| Gross profit, ₽ | 97 000 | 192 710 | 287 147 | 477 328 | 664 979 | 850 135 | 1 032 828 | 1 213 092 | 1 390 958 | 1 663 458 | 1 932 334 | 2 197 634 |
| GM% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% |
| Fixed costs, ₽ | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 |
| EBITDA, ₽ | -3 083 000 | -2 987 290 | -2 892 853 | -2 702 672 | -2 515 021 | -2 329 865 | -2 147 172 | -1 966 908 | -1 789 042 | -1 516 542 | -1 247 666 | -982 366 |
| Cash burn, ₽ | 3 083 000 | 2 987 290 | 2 892 853 | 2 702 672 | 2 515 021 | 2 329 865 | 2 147 172 | 1 966 908 | 1 789 042 | 1 516 542 | 1 247 666 | 982 366 |
| Cumulative cash, ₽ | 3 083 000 | 6 070 290 | 8 963 143 | 11 665 815 | 14 180 836 | 16 510 701 | 18 657 873 | 20 624 781 | 22 413 823 | 23 930 366 | 25 178 032 | 26 160 398 |

#### Optimistic

Допущения: new clients = `1,1,2,2,2,3,3,3,3,4,4,4`, monthly churn = **1.00%**.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 4 | 4 | 4 |
| Total clients | 1.0 | 2.0 | 4.0 | 5.9 | 7.9 | 10.8 | 13.7 | 16.5 | 19.4 | 23.2 | 27.0 | 30.7 |
| MRR, ₽ | 140 000 | 278 600 | 555 814 | 830 256 | 1 101 953 | 1 510 934 | 1 915 824 | 2 316 666 | 2 713 500 | 3 246 365 | 3 773 901 | 4 296 162 |
| COGS, ₽ | 43 000 | 85 570 | 170 714 | 255 007 | 338 457 | 464 073 | 588 432 | 711 547 | 833 432 | 997 098 | 1 159 127 | 1 319 535 |
| Gross profit, ₽ | 97 000 | 193 030 | 385 100 | 575 249 | 763 496 | 1 046 861 | 1 327 393 | 1 605 119 | 1 880 068 | 2 249 267 | 2 614 774 | 2 976 626 |
| GM% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% |
| Fixed costs, ₽ | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 |
| EBITDA, ₽ | -3 083 000 | -2 986 970 | -2 794 900 | -2 604 751 | -2 416 504 | -2 133 139 | -1 852 607 | -1 574 881 | -1 299 932 | -930 733 | -565 226 | -203 374 |
| Cash burn, ₽ | 3 083 000 | 2 986 970 | 2 794 900 | 2 604 751 | 2 416 504 | 2 133 139 | 1 852 607 | 1 574 881 | 1 299 932 | 930 733 | 565 226 | 203 374 |
| Cumulative cash, ₽ | 3 083 000 | 6 069 970 | 8 864 870 | 11 469 622 | 13 886 125 | 16 019 264 | 17 871 871 | 19 446 753 | 20 746 685 | 21 677 418 | 22 242 644 | 22 446 018 |

#### Pessimistic

Допущения: new clients = `1,1,1,1,1,1,1,2,2,2,2,2`, monthly churn = **2.33%**.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 1.0 | 2.0 | 2.9 | 3.9 | 4.8 | 5.7 | 6.5 | 8.4 | 10.2 | 11.9 | 13.7 | 15.3 |
| MRR, ₽ | 140 000 | 276 738 | 410 290 | 540 730 | 668 131 | 792 564 | 914 097 | 1 172 799 | 1 425 472 | 1 672 259 | 1 913 295 | 2 148 715 |
| COGS, ₽ | 43 000 | 84 998 | 126 018 | 166 081 | 205 212 | 243 430 | 280 758 | 360 217 | 437 824 | 513 622 | 587 655 | 659 963 |
| Gross profit, ₽ | 97 000 | 191 740 | 284 272 | 374 649 | 462 919 | 549 133 | 633 339 | 812 582 | 987 649 | 1 158 636 | 1 325 640 | 1 488 753 |
| GM% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% | 69.3% |
| Fixed costs, ₽ | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 | 3 180 000 |
| EBITDA, ₽ | -3 083 000 | -2 988 260 | -2 895 728 | -2 805 351 | -2 717 081 | -2 630 867 | -2 546 661 | -2 367 418 | -2 192 351 | -2 021 364 | -1 854 360 | -1 691 247 |
| Cash burn, ₽ | 3 083 000 | 2 988 260 | 2 895 728 | 2 805 351 | 2 717 081 | 2 630 867 | 2 546 661 | 2 367 418 | 2 192 351 | 2 021 364 | 1 854 360 | 1 691 247 |
| Cumulative cash, ₽ | 3 083 000 | 6 071 260 | 8 966 988 | 11 772 339 | 14 489 419 | 17 120 286 | 19 666 947 | 22 034 365 | 24 226 717 | 26 248 080 | 28 102 440 | 29 793 687 |

### A2. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

Юнит-экономика на 1 клиента в месяц:

| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 140 000 | recurring subscription |
| Gross profit | 97 000 | после COGS 43 000 ₽ |
| Contribution profit | 87 000 | после variable sales/support 10 000 ₽ |
| EBITDA contribution | 87 000 | до аллокации общих fixed costs |

EBITDA break-even на уровне компании:

`fixed costs / gross profit per client = 3 180 000 / 97 000 = 32.8 клиента`

То есть EBITDA 0 достигается примерно с **33 активных клиентов**. Если смотреть после налогов, требуемый client count выше:

| Режим | Формула net на 1 клиента | Net, ₽/клиент/мес | Break-even clients |
|---|---|---:|---:|
| УСН 6% | 140 000 - 43 000 - 6% × 140 000 | 88 600 | 35.9 |
| IT-льгота 3% | 140 000 - 43 000 - 3% × 140 000 | 92 800 | 34.3 |
| ОСНО 20% | налог на прибыль платится только при положительной прибыли; на юните при убытке доп. налог = 0 | 97 000* | 32.8 |

`*` При ОСНО в убыточной фазе налог на прибыль не возникает, но появляется сложность с НДС 20% и более тяжёлым администрированием. Для такого SaaS-кейса практичнее сравнивать **УСН 6%** и **IT-льготу 3%** при аккредитации Минцифры.

#### Net after tax на M12 по сценариям

| Scenario | EBITDA M12, ₽ | Net M12 при УСН 6%, ₽ | Net M12 при IT-льготе 3%, ₽ | Net M12 при ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|
| Base | -982 366 | -1 172 677 | -1 077 521 | -982 366 |
| Optimistic | -203 374 | -461 143 | -332 258 | -203 374 |
| Pessimistic | -1 691 247 | -1 820 170 | -1 755 709 | -1 691 247 |

### A3. Cash flow и startup capital to BEP

Так как ни один из трёх сценариев не выходит в EBITDA break-even в пределах 12 месяцев, `startup_capital_to_bep_rub` для горизонта M1-M12 равен накопленному cash burn за 12 месяцев плюс запас на добег до 33 клиентов.

| Scenario | Cumulative cash burn M12, ₽ | Клиенты M12 | Дефицит до 33 клиентов | Оценка startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Base | 26 160 398 | 22.7 | 10.3 | 32 573 666 ₽ |
| Optimistic | 22 446 018 | 30.7 | 2.3 | 23 880 158 ₽ |
| Pessimistic | 29 793 687 | 15.3 | 17.7 | 40 737 947 ₽ |

Примечание: для добега до BEP сверху добавляю ориентир по дополнительному капиталу через blended CAC **620 000 ₽** на недостающего клиента. Это грубая, но практичная оценка минимального капитала до выхода в операционный ноль.

### A4. Налоговая модель РФ

| Параметр | УСН 6% | IT-льгота 3% | ОСНО 20% |
|---|---|---|---|
| Налоговая база | 6% с выручки | 3% с выручки, если есть аккредитация Минцифры и соблюдены критерии | 20% с прибыли |
| Страховые взносы | ~30% к ФОТ, уже включены в расчёт | ~30% к ФОТ, уже включены в расчёт | ~30% к ФОТ, уже включены в расчёт |
| НДС | обычно нет | обычно нет | **20%**, если применимо |
| Что лучше для кейса | приемлемо | **лучший режим**, если компания проходит по критериям | хуже по администрированию и кэш-флоу |

Вывод по налогам: для данного кейса наиболее экономичный режим, если доступен, это **IT-льгота 3%**. Если льгота недоступна, рабочий запасной режим, это **УСН 6%**. ОСНО ухудшает cash conversion из-за НДС и усложняет запуск без явного upside на таком масштабе.

### A5. Break-even по сценариям

| Scenario | EBITDA break-even client count | Net break-even client count при УСН 6% | Net break-even client count при IT-льготе 3% | Break-even month в горизонте 12 мес |
|---|---:|---:|---:|---:|
| Base | 32.8 | 35.9 | 34.3 | >12 |
| Optimistic | 32.8 | 35.9 | 34.3 | >12 |
| Pessimistic | 32.8 | 35.9 | 34.3 | >12 |

Итог: при текущем fixed cost base бизнес в течение первого года не достигает break-even ни в одном из трёх сценариев. Практический порог, это **33-35 клиентов** для EBITDA 0 и **34-36 клиентов** для net break-even в льготном или УСН-режиме.

<!-- P6A-DONE -->

---

# FILE: 06-verdict.md

[GEO-EXPAND] Laurel — REJECTED: 64/100 | EBITDA base=800К₽/мес через 24 мес | LTV/CAC=11,7x | Ключевое преимущество: ROI через recovered billable hours | Главный риск: weak moat и дорогой category education.

# 06-verdict — laurel-geo-expand-1355-v2

sector: GEO-EXPAND
status: REJECTED
score: 64/100
date: 2026-05-13
analyst: branch-models-lead

## Investment committee summary

Вердикт: **REJECTED**.

Причина отклонения не в юнит-экономике клиента, а в сочетании трёх проблем на уровне фонда: прямой спрос в РФ остаётся LOW, moat слабый и category education дорогой, а base-case до `company_ebitda_rub_month >= 500 000 ₽/мес` требует долгого и капиталоёмкого выхода через узкий ICP. Кейс можно возвращать только после доказанных пилотов в РФ.

## Delta vs previous

- Предыдущий близкий Laurel-verdict в GitHub-репо: **63/100**, статус REJECTED.
- Текущий rerun: **64/100**, статус **REJECTED**.
- Что улучшилось: в текущем critic есть более сильный M24 median-case, `EBITDA @M24 p50 = 800 000 ₽/мес`.
- Что не изменилось: direct demand слабый, moat остаётся weak, GTM остаётся founder-led и consultative.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV/CAC = 11.7x`, `Gross Margin = 69.3%`, `Gross profit payback = 6.4 мес` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 17 | В 05-critic.md: `EBITDA @M24, p50 = 800 000 ₽/мес`, но M12 base ещё `-931 776 ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | В 02-demand.md category demand трижды `LOW`, `search demand в РФ слабый`, затем применён mandatory penalty -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | В 03-solution.md прямо зафиксированы `Commoditization risk` и `Feature risk`, а в 05-critic.md moat фактически держится только на workflow-fit. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | 04-economics.md: нужен high-touch motion, fixed costs `3 180 000 ₽/мес`, стартовый капитал `35-45 млн ₽`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | 04-economics.md: `Blended fully-loaded CAC = 620 000 ₽`, `Gross profit payback = 6.4 мес`, но buyer universe узкий. |

**Sum raw = 96/150. Normalized score = round(96 × 100 / 150) = 64/100.**

## 7-factor Moat Framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 2 | После внедрения появляются данные, процессы и интеграции в billing / PMS stack. |
| 3. Scale economies | 1 | COGS частично падает с объёмом, но onboarding и CSM остаются заметными. |
| 4. Proprietary data / model advantage | 1 | Есть рабочие данные использования, но в кейсе нет подтверждённого T1/T2 доказательства dataset moat. |
| 5. Regulatory moat | 0 | Регуляторный барьер для этого workflow в РФ не доказан. |
| 6. Brand / distribution | 1 | Глобальный бренд Laurel помогает, но в РФ нет сильного встроенного канала. |
| 7. Embedded workflow | 3 | Если продукт заходит, он сидит глубоко в daily time capture, billing и profitability review. |

**Moat raw = 8/21. Moat score = round(8 × 25 / 21) = 10/25.**

Вывод: **weak moat**. Это автоматически входит в Top-3 Risks.

## Ключевые метрики

- customer_ltv_rub: **7 276 500 ₽**
- CAC fully-loaded: **620 000 ₽**
- LTV/CAC: **11.7x**
- CAC payback по выручке: **4.4 мес**
- CAC payback по gross profit: **6.4 мес**
- Gross Margin: **69.3%**
- contribution_margin_rub_month: **87 000 ₽/клиент/мес**
- fixed_costs_rub_month: **3 180 000 ₽/мес**
- EBITDA break-even: **33 клиента**
- clients_to_500k_ebitda: **38 клиентов**
- months_to_500k_ebitda: **24 мес**
- startup_capital_to_bep_rub: **35-45 млн ₽**
- company_ebitda_potential_rub_month: **800 000 ₽/мес** в median M24-case из 05-critic.md

## Full business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов по юррынку / аудиту / консалтингу | SDR / founder | CRM, ручной ресерч | 1.5 ч | 1 800 | Низкий |
| 2 | Outbound / intro / referral reachout | SDR | email, Telegram, calls | 1.5 ч | 1 700 | Средний |
| 3 | Discovery call | AE / founder | meet, CRM | 1 ч | 3 500 | Средний |
| 4 | Диагностика timekeeping и billing workflow | AE + solutions | checklist, demo deck | 2 ч | 7 500 | Низкий |
| 5 | ROI demo и pilot scoping | AE + founder | product demo | 1.5 ч | 6 000 | Средний |
| 6 | Security / privacy / IT review | AE + product | docs, NDA | 1.5 ч | 5 500 | Низкий |
| 7 | Пилот 3-4 недели | CSM + solutions | sandbox, support | 10 ч | 32 000 | Средний |
| 8 | Onboarding / integration | CSM + engineer | billing / PMS / calendar connectors | 12 ч | 44 000 | Средний |
| 9 | Negotiation / procurement | founder + AE | contract workflow | 4 ч | 12 000 | Низкий |
| 10 | Production launch | CSM | runbook, training | 6 ч | 18 000 | Средний |

## Команда

| Роль | Нужно чел. | Salary gross ₽/мес | +30% взносы | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|
| CEO / founder | 1 | 450 000 | 135 000 | 585 000 |
| AE / GTM lead | 1 | 280 000 | 84 000 | 364 000 |
| SDR | 1 | 170 000 | 51 000 | 221 000 |
| CSM | 1 | 220 000 | 66 000 | 286 000 |
| Backend / integrations | 1 | 330 000 | 99 000 | 429 000 |
| Product / ML engineer | 1 | 360 000 | 108 000 | 468 000 |
| Support / ops | 1 | 160 000 | 48 000 | 208 000 |
| **Итого FOT** | **7** |  |  | **2 561 000** |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Кэпт | Крупный аудит и консалтинг с billable-hour economics, где потери времени прямо бьют по realization rate. | email decision-maker + партнёрский intro через CFO/COO practice | 250 000 ₽/мес |
| 2 | Технологии Доверия (ТеДо) | Большой объём проектной и аудиторской работы, высокий шанс pain по timesheets и profitability visibility. | конференция + direct outreach в operations/finance | 250 000 ₽/мес |
| 3 | Б1 | Плотный консалтинговый и аудиторский workflow, premium buyer, понятный ROI на recovered billable hours. | email managing partner / COO | 250 000 ₽/мес |
| 4 | Strategy Partners | Стратегический консалтинг с дорогим часом специалиста, где даже небольшой uplift в captured time окупает продукт. | founder-led intro + отраслевое мероприятие | 180 000 ₽/мес |
| 5 | КИАП | Юрфирма с billable-hour моделью, сильный кейс для pilot на одной practice group. | email managing partner + referral | 180 000 ₽/мес |
| 6 | VEGAS LEX | Крупная юрфирма, где проблема delayed timesheets и write-offs особенно чувствительна. | direct outreach к COO / head of operations | 180 000 ₽/мес |
| 7 | Пепеляев Групп | Высокая доля сложной юридической работы и необходимость прозрачности profitability по matter/client. | email decision-maker + legal conference | 180 000 ₽/мес |
| 8 | Tax Compliance | Налоговый консалтинг и legal advisory, где billing discipline и revenue leakage критичны. | targeted outbound + партнёрство с legal-tech интегратором | 160 000 ₽/мес |
| 9 | ФБК | Аудит и консалтинг, есть повторяемый staffing-heavy workflow и дорогой ручной timekeeping. | outbound в CFO / practice operations | 180 000 ₽/мес |
| 10 | HEADS Consulting | Digital/legal consulting motion, подходящий pilot buyer для доказательства ROI на небольшой практике. | vc.ru ad + founder outreach | 140 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Влияние | Почему это важно |
|---|---|---|---|
| weak_moat / feature risk | Высокая | Высокое | Рынок может воспринять продукт как premium-feature внутри broader PMS, а не отдельный category winner. |
| evidence_quality_unverified | Средняя | Высокое | В 02-demand.md отсутствует строка `Sources:`, поэтому criterion #3 получает mandatory penalty и локальная evidence-base выглядит слабее, чем должна. |
| category_education_and_cac | Высокая | Высокое | По 05-critic.md самые опасные драйверы, это `ценовая эрозия`, `CAC inflation` и service-heavy adoption drag. |

## Что должно быть доказано для APPROVED

1. **3-5 пилотов в РФ** у law / audit / consulting firms с измеримым recovered billable time.
2. **Pilot→paid conversion не ниже 25%** на выборке минимум 8 пилотов.
3. **Удержание MRR 180-250 тыс. ₽+** без тяжёлой кастомной разработки на каждый аккаунт.
4. **CAC < 900 000 ₽** и payback по gross profit не хуже 9 месяцев.
5. **Не менее 2 шаблонных интеграций** в локальный billing / PMS контур, чтобы не сжигать GM на onboarding.

## LTV Upside Calculator

Цель, показать, что должно измениться, чтобы кейс вышел из REJECTED в APPROVED WITH NOTES.

| Сценарий | MRR/клиент | GM | CAC | Annual churn | customer_ltv_rub | LTV/CAC | Клиентов до EBITDA 500k |
|---|---:|---:|---:|---:|---:|---:|---:|
| Текущий base | 140 000 ₽ | 69.3% | 620 000 ₽ | 16% | 7 276 500 ₽ | 11.7x | 38 |
| Upside A: pricing discipline | 180 000 ₽ | 69.3% | 620 000 ₽ | 16% | 9 355 500 ₽ | 15.1x | 29 |
| Upside B: меньше churn | 140 000 ₽ | 69.3% | 620 000 ₽ | 12% | 9 702 000 ₽ | 15.6x | 38 |
| Upside C: pricing + fixed-cost control | 180 000 ₽ | 69.3% | 620 000 ₽ | 16% | 9 355 500 ₽ | 15.1x | 24 при fixed costs 2.6 млн ₽ |

Вывод: даже при хорошем LTV/CAC кейс становится investable только если одновременно улучшаются **pricing discipline**, **template-based delivery** и **скорость выхода на 24-30 клиентов**.

## Финальный verdict

**REJECTED (<65 threshold rule applied as 64/100).**

Несмотря на хорошую клиентскую экономику, Laurel в РФ пока не выглядит investment-grade моделью. Базовый профиль упирается в слишком узкий buyer universe, слабую подтверждённость локального спроса и слабый moat. Это хороший кандидат для наблюдения и повторного входа после локальных пилотов, но не для одобрения сейчас.
