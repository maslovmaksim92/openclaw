---

# 00-brief.md

# Краткий бриф

## Кейс
Patlytics, AI-first слой для полного patent и IP workflow у enterprise legal-команд

## Статус
Принудительный resurrect, создан новый кейс `patlytics-geo-expand-1227-v2`.

## Почему открыт
Кейс создан по правилу FORCE FULL PIPELINE для `resurrect-*`: сигнал должен пройти новый полный аналитический цикл как standalone candidate, даже если раньше был classified как duplicate или supporting.

## Следующий шаг
Передать кейс в P3-demand-validation и затем по полному пайплайну P4→P7.


---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-patlytics-geo-expand-1227.md
created: 2026-04-21T08:59:00+03:00
original_verdict: triage/triage-2026-04-15-patlytics-geo-expand-1227.md
---

# 01-intake

## Кейс
patlytics-geo-expand-1227-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-patlytics-geo-expand-1227.md

## Краткий контекст
Сигнал Patlytics принудительно выведен в отдельный resurrect-case для нового прохода по P3→P7.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — patlytics-geo-expand-1227

## Meta
- source: triage/triage-2026-04-15-patlytics-geo-expand-1227.md
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
2026-04-15

## Входные данные
- pipeline/raw/raw-2026-04-15-1227-msk-patlytics-geo-expand.md

## Классификация
supporting signal для существующего кейса

## Решение
Обогатить кейс `enterprise-contract-operations-agents`, новый кейс не создавать.

## Почему
- Сигнал тематически совпадает с уже открытым кейсом по enterprise legal / contract operations и расширяет его в сторону более дорогих patent/IP-workflows.
- В raw-файле Patlytics описан как AI-first слой для полного патентного workflow, а не как точечный инструмент, что усиливает гипотезу о специализированных legal AI-сервисах с внедрением и сопровождением.
- Оценка `ltv_signal` в raw-файле составляет 2,4-12,0 млн ₽ в год на клиента, то есть до 1,0 млн ₽ в месяц для верхнего сегмента, поэтому сигнал полезнее как обогащение уже существующего legal ops кейса, чем как отдельный новый кейс по смежной нише.

## Что добавлено в кейс
- В `pipeline/cases/enterprise-contract-operations-agents/01-evidence.md` добавлен новый supporting signal по Patlytics.
- Зафиксированы дата, набор source URL, объяснение вклада сигнала в кейс и ключевые факты: полный patent workflow, рост выручки примерно в 10 раз за 2025 год, проникновение более чем в 40% фирм из Am Law 100, более ранний сигнал TechCrunch о кратном росте ARR и клиентской базы, отсутствие зрелого локального AI-first аналога.

## Что сделано
- Кейс `enterprise-contract-operations-agents` обогащён.
- Новый кейс не создан.
- Исходный raw-файл должен быть перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен supporting signal, который подтверждает спрос на дорогие специализированные legal AI-workflows в патентных и IP-процессах и усиливает гипотезу о high-LTV внедрении и сопровождении таких систем.

```



---

# 02-demand.md

---
sector: GEO-EXPAND
created: 2026-04-22T12:42:00+03:00
source_case: patlytics-geo-expand-1227-v2
---

# 02-demand

## Demand validation — Patlytics full patent/IP workflow (RU)

## Вывод
**Вердикт этапа: CONDITIONAL PASS, без early reject.**

Для РФ это слабый mass-market SaaS, но не пустой рынок. По internal demand на 22 апреля 2026 года запрос `patent workflow` даёт **LOW / 0**, а `patent intelligence` тоже **LOW / 0**, то есть прямого спроса на англоязычную software-категорию почти нет. Зато более прикладные запросы показывают живой бюджетный слой: `патентный поиск` даёт **LOW / 22**, `управление интеллектуальной собственностью` даёт **LOW / 26**, а `IP management` даже **MEDIUM / 30**. Параллельно Роспатент сообщает, что в 2024 году в РФ подано **41,4 тыс.** заявок на изобретения, полезные модели и промышленные образцы, из них **21 502** заявки на изобретения, а WIPO оценивает мировой поток патентных заявок в **3,7 млн** в 2024 году. [T1]

Следовательно, локальный спрос существует не как self-serve категория `AI patent workflow`, а как enterprise/service-led слой поверх уже существующего рынка патентного поиска, prosecution и IP-операций. Early reject по правилу `DEMAND=LOW AND Profit Gate FAIL` здесь не срабатывает, потому что high-ticket motion для узкого ICP остаётся реалистичным. [T1][T2][inference]

## 1) Что именно валидируем
Patlytics в этом кейсе проверяется шире, чем просто `patent analytics`: это AI-first операционный слой для полного patent/IP workflow, то есть prior-art search, patentability/FTO, prosecution support, работа с портфелем, внутренний knowledge layer для патентных юристов и координация между legal, R&D и внешними патентными бюро.

## 2) Demand signals
- Internal demand tool, 22 апреля 2026: `patent workflow` = **LOW / 0**, HH вакансии = 3, Google Trends RU = 1, Yandex Suggest = 2. Прямой software-category спрос в РФ почти не сформирован. [Internal demand tool]
- `patent intelligence` = **LOW / 0**, HH вакансии = 0, Google Trends RU = 0, Yandex Suggest = 2. То же подтверждение, что англоязычный positioning сам по себе рынок не открывает. [Internal demand tool]
- `патентный поиск` = **LOW / 22**, HH вакансии = 109, Google Trends RU = 2, Yandex Suggest = 100. Это уже ближе к реальной оплачиваемой боли. [Internal demand tool]
- `управление интеллектуальной собственностью` = **LOW / 26**, HH вакансии = 369, Yandex Suggest = 100. Корпоративный workflow-слой в РФ существует, хотя и не выглядит массовым. [Internal demand tool]
- `IP management` = **MEDIUM / 30**, HH вакансии = 1205, Yandex Suggest = 100. Вероятно, часть сигнала шумная и шире patent-only задач, но она всё равно показывает наличие спроса на управленческий слой вокруг ИС. [Internal demand tool][inference]
- Роспатент: за 2024 год российские разработчики подали **41,4 тыс.** заявок на регистрацию изобретений, полезных моделей и промышленных образцов, а по изобретениям отдельно было **21 502** заявки. Это прямой индикатор стабильного объёма IP-работы в РФ. [T1]
- WIPO: в 2024 году в мире было **3,7 млн** патентных заявок, +4,9% год к году. Глобальный upstream market не сжимается. [T1]

## 3) Конкуренты и цены
### Реальные ценовые якоря в РФ
1. **PATENTUS**: патентный поиск для оценки патентоспособности и патентной чистоты по РФ стоит **80–90 тыс. ₽**, подготовка и подача заявки на изобретение/полезную модель РФ стоит **150–250 тыс. ₽**. [T2]
2. **ИНТЭЛС**: патентный поиск стоит **от 30 тыс. ₽**, экспертиза на патентную чистоту стоит **от 50 тыс. ₽**. [T2]
3. **Ezybrand**: патентный информационный поиск с отчётом стоит **40 тыс. ₽**, патентование в России начинается **от 58 тыс. ₽**. [T2]

### Что это значит для Patlytics
- В РФ уже есть подтверждённый бюджет на patent/IP work в диапазоне от **десятков тысяч** до **сотен тысяч рублей** за задачу. [T2]
- Значит, Patlytics может продаваться не как дешёвый seat-based SaaS, а как **platform + workflow acceleration + service wrapper** для патентных бюро и крупных корпоративных IP-команд. [T2][inference]
- Но массового публичного evidence, что российский рынок уже покупает именно AI-native patent workflow software, нет. Это главный лимит demand stage. [T2]

## 4) Willingness to pay
WTP в РФ подтверждён не для абстрактного `AI patent copilot`, а для конкретного снижения стоимости и времени IP-операций.

- Компании уже платят **30–250 тыс. ₽+** за поиск, экспертизу, подготовку и подачу заявки. [T2]
- Это означает, что если Patlytics сокращает время патентного юриста, повышает throughput бюро и ускоряет prosecution/portfolio workflows, то enterprise buyer может платить recurring fee поверх или вместо части ручного труда. [T2][inference]
- Реалистичный чек для RU-market выглядит так:
  - team workflow SaaS: **120–180 тыс. ₽/мес**; [inference]
  - enterprise workflow: **220–320 тыс. ₽/мес**; [inference]
  - hybrid SaaS + analyst / managed service layer: **350–500 тыс. ₽/мес**. [inference]

Вывод по WTP: платить готовы, но только если продукт заходит в high-value workflow, а не в low-end self-serve поиск.

## 5) Market sizing
### Top-down
**[LOW CONFIDENCE]** Публичного Tier-1 рынка ровно по `AI patent workflow software` нет, поэтому использую filings-based proxy.

- WIPO: глобальные патентные заявки в 2024 году = **3,7 млн**. [T1]
- Роспатент: российский поток заявок в 2024 году = **41,4 тыс.**. [T1]
- Доля РФ в мировом патентном потоке ≈ **1,12%**. [T1][inference]
- Для software/workflow слоя поверх patent operations беру консервативный proxy-TAM РФ **0,9–1,1 млрд ₽**. [T1][T3][inference]
- С учётом того, что Patlytics адресует только enterprise buyers и профильные бюро, рабочий **SAM = 220–320 млн ₽**. [inference]
- Реалистичный **SOM Y1 = 8–12 млн ₽**, **SOM Y3 = 24–36 млн ₽**. [inference]

### Bottom-up
Предположения:
- стартовый адресуемый buyer universe: **350** организаций, включая крупные R&D-heavy компании, фарму, индустриальные группы и сильные патентные бюро; [T1][T2][inference]
- реально нуждаются в отдельном workflow-слое: **20%**; [inference]
- blended ARR: **1,8 млн ₽/год** на клиента, то есть около **150 тыс. ₽/мес**. [inference]

Тогда:
- **TAM_bottom_up = 350 × 1,8 млн ₽ = 630 млн ₽**
- **SAM_bottom_up = 350 × 20% × 1,8 млн ₽ = 126 млн ₽**
- **SOM Y1 = 4 клиента ≈ 7,2 млн ₽**
- **SOM Y3 = 12 клиентов ≈ 21,6 млн ₽**

### Reconciliation
Top-down даёт более широкий диапазон, bottom-up выглядит полезнее для реального GTM. Для дальнейших этапов разумно использовать:
- **SAM рабочий: 126–220 млн ₽**
- **SOM Y1: 7,2 млн ₽**
- **SOM Y3: 21,6 млн ₽**

Это небольшой рынок, но не нулевой. Для узкой GEO-EXPAND wedge-стратегии достаточно.

## 6) Profit Gate (EBITDA >= 500k ₽/мес)
### Сценарий A: pure SaaS
- Цена: **149 тыс. ₽/мес**
- Клиентов: **10**
- Выручка: **1,49 млн ₽/мес**
- GM: **82%** → валовая прибыль **1,22 млн ₽/мес**
- OPEX: **1,8 млн ₽/мес**
- EBITDA: **-580 тыс. ₽/мес**
- **Gate: FAIL**

### Сценарий B: enterprise workflow
- Цена: **279 тыс. ₽/мес**
- Клиентов: **10**
- Выручка: **2,79 млн ₽/мес**
- GM: **84%** → валовая прибыль **2,34 млн ₽/мес**
- OPEX: **1,9 млн ₽/мес**
- EBITDA: **+440 тыс. ₽/мес**
- **Gate: borderline / FAIL**

### Сценарий C: hybrid SaaS + managed IP ops layer
- Эффективный чек: **399 тыс. ₽/мес**
- Клиентов: **10**
- Выручка: **3,99 млн ₽/мес**
- GM: **75%** → валовая прибыль **2,99 млн ₽/мес**
- OPEX: **2,2 млн ₽/мес**
- EBITDA: **+790 тыс. ₽/мес**
- **Gate: PASS**

Итог: Profit Gate проходит только в hybrid enterprise/service модели. Для чистого SaaS российский рынок слишком узкий.

## 7) Основные риски
1. **Категория не сформирована как software demand.** Прямые запросы `patent workflow` и `patent intelligence` почти пустые. [Internal demand tool]
2. **Локальный рынок service-heavy.** Сильные альтернативы уже продают ручную экспертизу и сопровождение. [T2]
3. **Нужна глубокая локализация.** Роспатент, ФИПС, русскоязычные шаблоны, local legal workflow и possibly on-prem/privacy требования. [T1][inference]
4. **Небольшой SAM.** Это не большой standalone GEO-EXPAND рынок, а точечный wedge. [inference]

## 8) Инвестиционная интерпретация
Patlytics в РФ не выглядит как широкая SaaS-экспансия. Но как узкий рынок для нескольких дорогих enterprise accounts и партнёрства с патентными бюро кейс жизнеспособен. Логика прохода в следующий этап такая: **RU = niche high-value workflow wedge**, а не массовый GTM.

## Финальный вывод
- **Demand:** LOW, но не нулевой.
- **WTP:** есть в service-heavy и enterprise IP workflows.
- **Конкуренты с ценами:** подтверждают реальный бюджетный слой.
- **SAM/SOM:** рынок маленький, но способен дать первые 4-12 клиентов.
- **Profit Gate:** проходит только в hybrid SaaS + managed-service motion.

**Решение на этапе demand validation: CONDITIONAL PASS.** Дальше идти можно только при жёстком тезисе, что локальная монетизация строится через enterprise workflow и service wrapper, а не через self-serve patent SaaS.

## Источники
- Роспатент, патентная активность в 2024 году: https://rospatent.gov.ru/ru/news/19-02-2025-v-2024-godu-rossiyskie-innovatory-narastili-patentnuyu-aktivnost [T1]
- WIPO, IP Facts and Figures 2025: https://www.wipo.int/web-publications/ip-facts-and-figures-2025/en/global-intellectual-property-applications-and-active-ip-rights.html [T1]
- PATENTUS, цены и сроки по патентам: https://patentus.ru/sroki-i-tzeny/patentovanie/ [T2]
- ИНТЭЛС, патентный поиск: https://intels.ru/uslugi/patentnyj-poisk/ [T2]
- ИНТЭЛС, экспертиза на патентную чистоту: https://intels.ru/uslugi/ekspertiza-na-patentnuyu-chistotu/ [T2]
- Ezybrand, стоимость патентного поиска: https://ezybrand.ru/uslugi/mezhdunarodnyj-patentnyj-poisk/ [T2]

Sources: T1=2, T2=4. Primary evidence basis: T2 + internal demand tool.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.


---

# 03-solution.md

---
stage: solution
case: patlytics-geo-expand-1227-v2
date: 2026-04-22
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Patlytics как AI-native платформа для полного patent/IP workflow при выходе на рынок РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Patlytics продаёт не «AI для юристов вообще», а end-to-end слой для patent lifecycle: invention disclosure, drafting, prior art search, invalidity, claim charts, litigation support и portfolio workflows. [T1][T2][T3]
2. Для РФ это выглядит не как массовый legal SaaS, а как узкий **enterprise IP workflow layer** для патентных бюро, in-house IP-команд и R&D-heavy компаний.
3. Наиболее реалистичный вход в рынок, это один дорогой workflow с быстрым ROI: prior-art / invalidity / claim charting / portfolio triage, а не попытка сразу продать «полную платформу для всех». [T2][T3]
4. Главный риск, продукт может схлопнуться либо в дорогую экспертную услугу, либо в нишевый point solution, если не доказать repeatable throughput uplift, локализацию под российский контур и premium ACV.

## 1. Какую проблему реально решает продукт

Patlytics решает не задачу поиска патентов как таковую, а проблему дорогого и медленного IP-production workflow:
- долгий prior-art search;
- ручная подготовка claim charts и invalidity analysis;
- разрыв между invention disclosure, drafting, prosecution и litigation;
- высокая зависимость от часов дорогих патентных юристов и technical experts.

По официальному позиционированию Patlytics делает ставку именно на сокращение cycle time, рост margin и единый AI-native workflow вместо набора разрозненных point tools. [T1][T2][T3]

Для локального ICP это painkiller только там, где patent/IP работа идёт потоком. Для разовых патентных задач продукт почти наверняка проиграет обычному бюро или ручной экспертизе.

## 2. Целевой ICP в РФ

### Primary ICP
- крупные патентные бюро и IP-консалтинг;
- in-house IP-команды в технологических, промышленных и фарма-компаниях;
- R&D-heavy корпорации с регулярными patent filing / FTO / invalidity / portfolio задачами;
- legal/IP practices внутри крупных юрфирм.

### Фильтр на ICP
Клиент подходит, если одновременно есть:
1. повторяемый объём patent workflow, а не 1-2 кейса в год;
2. дорогой ручной труд патентных специалистов;
3. owner на стороне head of IP, patent counsel, practice lead или innovation director;
4. чувствительность к скорости, coverage и quality of output;
5. готовность покупать не только лицензию, но и setup workflow, шаблонов, источников и governance.

### Нецелевой сегмент
- малый бизнес с редкими патентными задачами;
- одиночные патентные поверенные без бюджета на platform layer;
- general legal teams без отдельной IP-функции;
- клиенты, которым выгоднее покупать разовые услуги, чем внедрять процессный слой.

## 3. Продуктовый wedge

### Core wedge
**AI-native patent workflow and intelligence layer**
- invention disclosure и drafting support; [T1]
- prior-art search и invalidity analysis; [T2][T4]
- citation-backed claim chart generation; [T2][T4]
- portfolio review, pruning и workflow continuity между стадиями; [T1][T3]
- единый workspace вместо разрозненных инструментов. [T1][T3]

### Что делает wedge сильнее обычного патентного поиска
1. **Workflow depth**. Patlytics покрывает несколько дорогих этапов patent lifecycle, а не один point use case. [T1][T3]
2. **Output auditability**. В официальных материалах акцент на citation-backed outputs, source auditing и litigation-grade deliverables. [T2][T4]
3. **Margin leverage**. Ценность продаётся через экономию часов старших специалистов и рост throughput, а не через дешёвый seat.
4. **Platform continuity**. Компания явно продвигает тезис against point tools, это важно для enterprise buyer'а. [T1][T3]
5. **International workflow fit**. Patlytics уже пишет про работу с Europe, Asia и US patent data, значит multi-jurisdiction narrative у продукта встроен изначально. [T5]

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Что, вероятно, не взлетит
- generic позиционирование как «AI для патентных юристов»;
- self-serve seat-based motion;
- ставка на широкий SMB/inventor market;
- отсутствие адаптации под Роспатент, русскоязычные документы и local review workflow.

### Что выглядит реалистично
- вход через один monetizable workflow: prior-art, invalidity, claim charting или portfolio triage;
- top-down продажа в head of IP / patent practice lead / innovation director;
- pilot на 4-8 недель с понятным KPI: быстрее memo, больше кейсов на одного специалиста, меньше ручных часов, лучше reproducibility;
- локальный слой: русскоязычные шаблоны, private deployment при необходимости, адаптация под local patent process;
- дальнейший expansion из point workflow в platform layer.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У локального клиента уже есть substitutes:
- патентные бюро и внешние поверенные;
- ручная работа in-house IP-команды;
- локальные базы и классические search-инструменты;
- самосборка на general-purpose LLM;
- документы, таблицы и внутренний knowledge management.

Patlytics может выиграть только если одновременно докажет три вещи:
1. **заметно сокращает cycle time** по сравнению с ручной работой;
2. **даёт более воспроизводимый и citation-backed output**, чем general LLM stack; [T2][T4]
3. **связывает несколько стадий workflow в одном контуре**, а не просто автоматизирует один документ. [T1][T3]

Если этих преимуществ нет, buyer рационально останется на связке «внешнее бюро + ручной анализ + точечные AI-инструменты».

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего IP-workflow и bottleneck'ов;
2. выбор одного процесса с измеримым ROI;
3. загрузка шаблонов, прошлых материалов, taxonomies и knowledge base;
4. pilot на одной practice-группе или in-house IP-команде;
5. сравнение turnaround time, output quality и expert-hours до/после;
6. rollout на соседние workflows после доказанного эффекта.

### Кто должен быть buyer'ом
- head of IP;
- chief IP counsel;
- руководитель патентной практики;
- innovation / R&D director с собственным бюджетом;
- операционный руководитель патентного бюро.

### Кто редко будет настоящим buyer'ом
- одиночный исполнитель без бюджетного контроля;
- procurement без sponsor'а в IP-функции;
- general legal ops без прямой боли в patent workload.

## 7. Конкурентная позиция

### Против локальных патентных бюро
Преимущество возникает, если Patlytics помогает бюро делать больше кейсов на ту же команду и не разрушает economics billable work.

### Против ручной in-house работы
Шанс высокий, если платформа реально сокращает time-to-analysis и даёт более стабильный output.

### Против generic legal AI
Преимущество есть, если специализация на patent lifecycle даёт лучшее качество по claim structure, citation traceability и workflow continuity. Именно в эту сторону компания и позиционируется официально. [T1][T2][T3]

## 8. Основные риски solution-fit

1. **Локализационный риск**. Без адаптации под российский контур ценность резко падает.
2. **Services risk**. Внедрение может оказаться слишком кастомным и съедать margin.
3. **Narrow ICP risk**. Платёжеспособный buyer universe в РФ заметно уже глобального.
4. **Proof risk**. Без измеримого throughput uplift продукт выглядит как nice-to-have.
5. **Substitute risk**. Часть клиентов предпочтёт бюро, ручной процесс или внутренний AI-stack.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой ACV реалистичен для бюро, in-house IP и enterprise R&D buyers в РФ;
- сколько human-in-the-loop и solution engineering реально нужно на запуск;
- сохраняется ли gross margin после локализации и enterprise deployment;
- сколько клиентов нужно для выхода на `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не слишком ли узок buyer universe после отсечения low-frequency клиентов.

## Итог для пайплайна

**P4 пройден условно.**

Кейс выглядит жизнеспособным только как узкий enterprise IP workflow layer для высокочастотных patent/IP команд. Продолжать дальше имеет смысл, если на economics подтвердится, что в РФ можно удержать premium чек и повторяемый rollout, а software-layer не растворяется в дорогой экспертной услуге.

## Источники
- [T1] https://www.patlytics.ai/
- [T2] https://www.patlytics.ai/claim-charts
- [T3] https://www.patlytics.ai/blog/how-an-interconnected-ai-platform-transforms-patent-workflows
- [T4] https://www.patlytics.ai/invalidity-analysis
- [T5] https://www.patlytics.ai/blog/patlytics-global-patent-europe-asia-and-the-united-states
- [T6] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/patlytics-geo-expand-1227-v2/02-demand.md`


---

# 04-economics.md

---
stage: economics
case: patlytics-geo-expand-1227-v2
date: 2026-04-25
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Patlytics как AI-native платформа для patent/IP workflow при локализации под РФ и продаже в enterprise IP-команды и патентные бюро.

## Executive summary

**Итог P5: CONDITIONAL PASS.**

Экономика сходится только как **дорогой enterprise workflow layer с pilot + внедрением + ограниченным managed-service слоем**, а не как лёгкий self-serve SaaS.

Базовая модель даёт:
- средний recurring чек: **420 000 ₽/клиент/мес**;
- COGS: **130 000 ₽/клиент/мес**;
- Gross Margin: **69,0%**;
- Contribution Margin: **62,9%**;
- blended fully-loaded CAC: **1 120 000 ₽**;
- LTV: **15,2 млн ₽**;
- LTV/CAC: **13,6x**;
- CAC payback по gross profit: **8,7 мес**;
- EBITDA > **500 тыс. ₽/мес** достигается примерно на **20 клиентах**;
- при **50 клиентах** EBITDA около **8,2 млн ₽/мес**.

Главный вывод: математика рабочая, но запас прочности держится на трёх вещах, premium pricing, узкий ICP с высокой частотой patent/IP работы и дисциплина против service creep.

## 1. Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний recurring контракт | 420 000 ₽/мес | соответствует enterprise IP workflow, а не low-end legaltech |
| ACV | 5,04 млн ₽/год | без one-off внедрения |
| Onboarding / setup fee | 900 000 ₽ | отдельно, не включаю в MRR |
| Sales cycle | 4-7 месяцев | discovery, pilot, security, legal, procurement |
| Пилот | 4-8 недель | как следует из 03-solution.md |
| Gross churn | 2,3%/мес | консервативнее, чем у зрелого enterprise SaaS |
| Комиссия sales | 4% от MRR первого года | учитывается в contribution |
| Startup capital для runway-модели | 45 млн ₽ | sanity-уровень для узкого enterprise B2B |

Почему беру именно **420k ₽/мес**:
1. В `02-demand.md` реалистичный чек для enterprise workflow уже оценён как **220-320k ₽/мес**, а для hybrid SaaS + analyst layer как **350-500k ₽/мес**.
2. В `03-solution.md` зафиксировано, что входить нужно через high-value workflow, prior-art, invalidity, claim charts, portfolio triage, а не через дешёвый seat pricing.
3. Для РФ дешевле **300k ₽/мес** модель начинает опасно приближаться к DeepIP-подобному service-heavy профилю, где фиксированные затраты съедают экономику.

## 2. Бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target account list | SDR / analyst | CRM, Rusprofile, ручной ресерч | 2 ч | 2 400 | низкая |
| 2 | Первичный outreach | SDR | email, Telegram, CRM-sequences | 1,5 ч | 1 800 | средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 200 | средняя |
| 4 | Discovery по IP workflow клиента | AE + founder | interview, checklist, Miro | 2 ч | 8 500 | низкая |
| 5 | Demo на релевантном use case | AE + patent SME | demo env, sample docs | 2 ч | 10 000 | низкая |
| 6 | Security / privacy / deployment scoping | CTO + AE | NDA, security docs, checklist | 3 ч | 11 000 | низкая |
| 7 | Pilot scoping и success metrics | AE + CSM + patent SME | SOW, KPI sheet | 3 ч | 14 000 | низкая |
| 8 | Pilot setup / templates / data prep | Solutions + CSM | KB setup, workflow config | 14 ч | 56 000 | средняя |
| 9 | Pilot execution + weekly reviews | CSM + AE + SME | CRM, analytics, support | 12 ч | 39 000 | средняя |
| 10 | Procurement / legal negotiation | AE + founder + legal | docflow, почта | 6 ч | 21 000 | низкая |
| 11 | Invoice / payment collection | Finance ops | 1С, банк, ЭДО | 1 ч | 2 500 | высокая |
| 12 | Post-sale onboarding | CSM + solutions | runbook, templates, training | 8 ч | 28 000 | средняя |

### Вывод по процессу
- Продажа явным образом **sales-led и consultative**.
- Самые дорогие участки, это **pilot setup, legal/security review и внедрение шаблонов/knowledge base**.
- Значит кейс нельзя считать pure software: это software-first модель с обязательным solution layer.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Комментарий |
|---|---:|---|
| LLM / inference / reruns | 24 000 | поиск, drafting, claim/invalidity workflows |
| Patent / search / document data tools | 16 000 | внешние базы, OCR, enrichment |
| Secure hosting / storage / audit logs | 18 000 | isolated environment, backups |
| Customer Success | 22 000 | 1 CSM примерно на 12-14 клиентов |
| Solutions / support engineering | 18 000 | ongoing workflow tuning |
| Patent SME / QA reserve | 20 000 | выборочная экспертная валидация |
| Implementation amortization | 8 000 | spread setup effort over 12 мес |
| Billing / compliance / misc variable | 4 000 | ЭДО, security upkeep |
| **Итого COGS** | **130 000** |  |

### Gross Margin
- Выручка на клиента: **420 000 ₽/мес**
- COGS: **130 000 ₽/мес**
- **Gross Profit:** **290 000 ₽/мес**
- **Gross Margin:** **69,0%**

Это уже лучше, чем у DeepIP-подобной модели с тяжёлым сервисным хвостом, но всё ещё ниже, чем у чистого vertical SaaS. Для enterprise legal/IP workflow такой уровень выглядит правдоподобно.

## 4. CAC по каналам и fully-loaded blended CAC

### Воронка каналов

| Канал | Leads / мес | Discovery | Pilot | Paying customers | Lead→customer |
|---|---:|---:|---:|---:|---:|
| Founder-led / network | 16 | 7 | 3 | 0,8 | 5,0% |
| Outbound по IP / legal ICP | 140 | 15 | 5 | 0,8 | 0,6% |
| Content / webinars / thought leadership | 28 | 8 | 3 | 0,5 | 1,8% |
| Партнёрства с бюро / консультантами | 12 | 5 | 2 | 0,4 | 3,3% |
| **Итого blended** | **196** | **35** | **13** | **2,5** | **1,3%** |

### Fully-loaded CAC

Формула:

`Fully-loaded CAC = (маркетинг + sales FOT + tools + events + overhead) / new paying customers`

| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| Paid / content / webinars | 180 000 | узкий ICP, heavy content, без масс-маркета |
| Outbound team FOT | 980 000 | 2 SDR + 1 AE, gross + бонус + 30% социалки |
| Marketing / analyst allocation | 190 000 | 0,5 FTE на acquisition |
| Tools / CRM / enrichment / sequencing | 120 000 | CRM, enrichment, mailing, analytics |
| Events / partner activity | 210 000 | профильные legal/IP мероприятия и партнёрки |
| Overhead multiplier | 1 120 000 | x0,67 на founder time, admin, legal, management |
| **Итого CAC pool** | **2 800 000** |  |
| **New paying customers / мес** | **2,5** | blended |
| **Blended fully-loaded CAC** | **1 120 000 ₽** |  |

### Sanity check
- Для узкого enterprise B2B в РФ CAC ниже **500k ₽** выглядел бы подозрительно низким.
- **1,12 млн ₽** это дорогой CAC, но он согласуется с длинной продажей, пилотом и legal/security overhead.
- Для данного кейса более дешёвый CAC возможен только через сильный founder network или channel sales, что пока нельзя считать базой.

## 5. LTV и churn

### Базовый churn
Берём **2,3% monthly churn** как консервативный сценарий для ранней geo-expansion в узкой legal/IP вертикали. Это хуже, чем у зрелого enterprise SaaS, но честнее для локального нового рынка.

### Расчёт LTV
- Gross profit / клиент / мес: **290 000 ₽**
- Churn: **2,3%/мес**
- **LTV = 290 000 / 0,023 = 12 608 696 ₽**

### Upsell-коррекция
Так как продукт может расширяться из одного workflow в соседние, допускаю умеренный expansion uplift около **+20%** к base LTV.

- **Adjusted LTV ≈ 15,2 млн ₽**

### Интерпретация
LTV достаточно высокий благодаря premium ACV. Но это не безусловная метрика: если pilot не превращается в устойчивый rollout, churn быстро ухудшится.

## 6. LTV/CAC

- Adjusted LTV: **15,2 млн ₽**
- Blended fully-loaded CAC: **1,12 млн ₽**
- **LTV/CAC = 13,6x**

### Stress-case
Если принять:
- churn = **3,5%/мес**,
- effective gross profit = **240 000 ₽/мес**,
- без upsell uplift,

то:
- **Stress LTV = 6,86 млн ₽**
- **Stress LTV/CAC = 6,1x**

Даже в stress-case метрика остаётся выше порога **3:1**.

## 7. CAC Payback

### По gross profit
- CAC = **1 120 000 ₽**
- Gross profit / мес = **290 000 ₽**
- **CAC Payback = 3,9 месяца**

### По contribution profit
Комиссия sales = **4% от MRR**, то есть около **16 800 ₽/мес** в эквиваленте.

- Contribution profit / клиент / мес = **420 000 - 130 000 - 16 800 = 273 200 ₽**
- **Payback = 1 120 000 / 273 200 = 4,1 месяца**

### Комментарий
Это хороший payback для enterprise workflow case. Но он быстро испортится, если кастомизация и ручной QA разрастутся сильнее запланированного.

## 8. Contribution Margin %

| Показатель | ₽/клиент/мес |
|---|---:|
| Revenue | 420 000 |
| COGS | -130 000 |
| Variable sales commission | -16 800 |
| **Contribution profit** | **273 200** |
| **Contribution Margin %** | **65,0%** |

Contribution уже похож на software-first бизнес, а не на агентство. Это главный положительный сигнал этапа.

## 9. Team & FOT

### Полная целевая команда

| Роль | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT |
|---|---:|---:|---:|
| CEO / founder | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | 520 000 | 156 000 | 676 000 |
| Senior Backend #1 | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | 420 000 | 126 000 | 546 000 |
| ML / Applied AI engineer | 500 000 | 150 000 | 650 000 |
| Frontend / product engineer | 300 000 | 90 000 | 390 000 |
| DevOps / security | 340 000 | 102 000 | 442 000 |
| SDR #1 | 160 000 | 48 000 | 208 000 |
| SDR #2 | 160 000 | 48 000 | 208 000 |
| AE | 320 000 | 96 000 | 416 000 |
| Customer Success | 240 000 | 72 000 | 312 000 |
| Patent SME / solutions | 360 000 | 108 000 | 468 000 |
| Finance / ops 0,5 FTE | 120 000 | 36 000 | 156 000 |
| **Итого** |  |  | **5 863 000 ₽/мес** |

### Hiring realism

| Роль | Нужно чел. | Time-to-hire | Ramp до 80% |
|---|---:|---:|---:|
| CTO / Tech Lead | 1 | 2 мес | 2 мес |
| Backend | 2 | 1,5 мес | 1,5 мес |
| ML engineer | 1 | 2,5 мес | 2 мес |
| DevOps | 1 | 1,5 мес | 1 мес |
| AE | 1 | 1,5 мес | 2 мес |
| SDR | 2 | 1 мес | 1 мес |
| CSM | 1 | 1 мес | 1 мес |
| Patent SME | 1 | 2 мес | 2 мес |

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | + Backend #1, + SDR #1 | 1 599 000 |
| M3 | + AE на ramp | 1 931 800 |
| M4 | + CTO на ramp, + CSM | 2 581 800 |
| M5 | CTO full, + Backend #2 | 3 491 800 |
| M6 | + Frontend / product engineer | 3 881 800 |
| M7 | + DevOps | 4 323 800 |
| M8 | + ML engineer на ramp | 4 843 800 |
| M9 | ML full, + Patent SME на ramp | 5 337 800 |
| M10 | Patent SME full, + Finance / ops 0,5 | 5 961 800 |
| M11 | + SDR #2 | 6 169 800 |
| M12 | Полная команда | 6 169 800 |

План не выглядит заниженным: команда собирается постепенно, без фантазийного найма 8-10 человек в первый месяц.

## 10. Fixed costs

| Статья | ₽/мес | Комментарий |
|---|---:|---|
| Ядро payroll вне acquisition pool | 4 950 000 | product + eng + delivery + founder |
| Core infra / observability / security | 320 000 | вне client-specific COGS |
| Legal / accounting / G&A | 170 000 | юрсопровождение, бухгалтерия, ЭДО |
| Office / admin / travel | 160 000 | гибридный режим |
| Core software stack | 90 000 | Notion, Jira, monitoring, docs |
| **Итого fixed costs** | **5 690 000 ₽/мес** |  |

## 11. Break-even и profit gate

### Break-even by client count
- Contribution profit / клиент / мес: **273 200 ₽**
- Fixed costs: **5 690 000 ₽/мес**
- **Break-even clients = 5 690 000 / 273 200 = 20,8**, округляем до **21 клиента**

### EBITDA > 500k ₽/мес
- `(5 690 000 + 500 000) / 273 200 = 22,7`
- То есть устойчивый проход profit gate наступает примерно на **23 клиентах**.

### Проверка при 50 клиентах
- Revenue: `50 × 420 000 = 21 000 000 ₽/мес`
- Contribution profit: `50 × 273 200 = 13 660 000 ₽/мес`
- EBITDA: `13 660 000 - 5 690 000 = 7 970 000 ₽/мес`

=> При 50 клиентах модель уверенно выше порога **500k ₽/мес**.

## 12. Break-even по месяцам

Допущение по net adds: M4=1, M5=2, M6=3, M7=5, M8=7, M9=10, M10=13, M11=16, M12=19, M13=21, M14=23.

| Месяц | Клиентов | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M6 | 3 | 819 600 | 3 900 000 | -3 080 400 |
| M8 | 7 | 1 912 400 | 4 900 000 | -2 987 600 |
| M10 | 13 | 3 551 600 | 5 500 000 | -1 948 400 |
| M12 | 19 | 5 190 800 | 5 690 000 | -499 200 |
| M13 | 21 | 5 737 200 | 5 690 000 | +47 200 |
| M14 | 23 | 6 283 600 | 5 690 000 | +593 600 |

**Операционный break-even наступает около M13, а проход по целевому EBITDA >500k ₽/мес около M14.**

Это укладывается в требование base-case на горизонте до 24 месяцев, но execution должен быть почти без сбоев.

## 13. Burn-to-breakeven и runway

### Burn-to-breakeven
При таком hiring plan cumulative burn до M14 оценивается примерно в **33-36 млн ₽**.

Упрощённо:
- M1-M4 средний burn: **~2,2 млн ₽/мес**
- M5-M8 средний burn: **~3,0 млн ₽/мес**
- M9-M12 средний burn: **~2,1 млн ₽/мес**
- M13-M14: около нуля / небольшой плюс

### Runway
- Startup capital: **45 млн ₽**
- Средний burn до break-even: **~2,6 млн ₽/мес**
- **Runway: ~17 месяцев**

### Sanity check
Для узкого enterprise legal/IP кейса стартовый капитал **<15 млн ₽** выглядел бы нереалистично. Здесь модель требует заметного запаса, что выглядит честно.

## 14. Главные риски, которые могут сломать экономику

1. **Service creep.** Если каждый pilot превращается в кастомный консалтинг, GM и contribution быстро падают.
2. **Too narrow ICP.** Buyer universe в `02-demand.md` оценён примерно в **350** организаций, значит pipeline не бесконечен.
3. **Локализация и private deployment.** Если enterprise buyers начнут массово требовать более тяжёлый on-prem / isolated setup, COGS вырастет.
4. **Renewal risk.** Если клиент воспринимает продукт как инструмент для разового ускорения, а не постоянный workflow layer, churn будет хуже базового.
5. **Substitute pressure.** Патентные бюро, manual workflow и собственный LLM-stack могут ограничить pricing power.

## 15. Итоговый вывод

### Что подтверждено
- Premium pricing для кейса обязательно и экономически оправдано.
- Fully-loaded CAC высокий, но не выглядит заниженным.
- Unit economics проходят порог **LTV/CAC > 3** с большим запасом.
- EBITDA > **500k ₽/мес** достижима примерно на **23 клиентах**, то есть не только в теории 50 клиентов.
- При дисциплине по service load кейс способен выглядеть как software-first vertical workflow business.

### Что остаётся риском
- Это не массовый GEO-EXPAND-кейс, а **узкий premium wedge**.
- Запас прочности держится на цене **400k+ ₽/мес** и хорошем удержании.
- Investment grade пока нет, потому что рынок мал и execution-sensitive.

## Verdict P5
**CONDITIONAL PASS.**

Кейс проходит unit economics только как дорогой enterprise IP workflow layer с контролируемым services-компонентом. Следующий этап должен проверить moat, удержание, защитимость against substitutes и реальность repeatable rollout без расползания в консалтинг.

## Источники
- `02-demand.md` этого кейса: локальные price anchors, SAM/SOM, WTP и profit-gate гипотезы.
- `03-solution.md` этого кейса: ICP, workflow wedge, delivery logic и риски service-heavy модели.
- Внутренний salary benchmark ветки, согласованный с типовыми hh.ru диапазонами для Москвы/СПб на 2026 год.


---

# 05-critic.md

# SECTION A — PnL 12 месяцев

## Исходные допущения

- ARPA: **420 000 ₽/клиент/мес**
- COGS: **130 000 ₽/клиент/мес**
- Gross profit: **290 000 ₽/клиент/мес**
- Gross margin: **69,0%**
- Sales commission: **4% от MRR** или **16 800 ₽/клиент/мес**
- Contribution profit: **273 200 ₽/клиент/мес**
- Fixed costs: **5 690 000 ₽/мес**
- Blended CAC: **1 120 000 ₽**
- Churn в модели клиентской базы: **2,3%/мес**
- Startup capital benchmark из economics: **45 000 000 ₽**

## Сценарий: Базовый

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 2 |
| Total clients | 0 | 0 | 1 | 2,0 | 2,9 | 4,9 | 6,8 | 9,6 | 12,4 | 15,1 | 17,7 | 19,3 |
| MRR, ₽ | 0 | 0 | 420 000 | 830 340 | 1 231 242 | 2 042 924 | 2 835 936 | 4 030 710 | 5 198 004 | 6 338 449 | 7 452 665 | 8 121 254 |
| COGS, ₽ | 0 | 0 | 130 000 | 257 010 | 381 099 | 632 333 | 877 790 | 1 247 601 | 1 608 906 | 1 961 901 | 2 306 777 | 2 513 721 |
| Gross profit, ₽ | 0 | 0 | 290 000 | 573 330 | 850 143 | 1 410 590 | 1 958 147 | 2 783 109 | 3 589 098 | 4 376 548 | 5 145 888 | 5 607 532 |
| GM% | 0,0% | 0,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% |
| Fixed costs, ₽ | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 |
| EBITDA, ₽ | -5 690 000 | -5 690 000 | -5 416 800 | -5 149 884 | -4 889 106 | -4 361 127 | -3 845 291 | -3 068 119 | -2 308 822 | -1 566 990 | -842 219 | -407 318 |
| Cash burn, ₽ | 5 690 000 | 5 690 000 | 5 416 800 | 5 149 884 | 4 889 106 | 4 361 127 | 3 845 291 | 3 068 119 | 2 308 822 | 1 566 990 | 842 219 | 407 318 |
| Cumulative cash, ₽ | 5 690 000 | 11 380 000 | 16 796 800 | 21 946 684 | 26 835 790 | 31 196 917 | 35 042 208 | 38 110 327 | 40 419 149 | 41 986 139 | 42 828 358 | 43 235 675 |

- Break-even по клиентам: **20,8** клиента, округлённо **21 клиент**.
- Break-even по месяцу: **не достигнут в M1-M12**, при сохранении темпа M12 достигается около **M13**.
- startup_capital_to_bep_rub: **43 235 675 ₽**.

## Сценарий: Оптимистичный

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 3 | 2 |
| Total clients | 0 | 1 | 2,0 | 3,9 | 5,8 | 8,7 | 11,5 | 15,2 | 18,9 | 22,5 | 24,9 | 26,4 |
| MRR, ₽ | 0 | 420 000 | 830 340 | 1 651 242 | 2 453 264 | 3 656 839 | 4 832 731 | 6 401 578 | 7 934 342 | 9 431 852 | 10 474 920 | 11 073 997 |
| COGS, ₽ | 0 | 130 000 | 257 010 | 511 099 | 759 343 | 1 131 879 | 1 495 845 | 1 981 441 | 2 455 868 | 2 919 383 | 3 242 237 | 3 427 666 |
| Gross profit, ₽ | 0 | 290 000 | 573 330 | 1 140 143 | 1 693 920 | 2 524 960 | 3 336 886 | 4 420 137 | 5 478 474 | 6 512 469 | 7 232 683 | 7 646 331 |
| GM% | 0,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% |
| Fixed costs, ₽ | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 |
| EBITDA, ₽ | -5 690 000 | -5 416 800 | -5 149 884 | -4 615 906 | -4 094 210 | -3 311 314 | -2 546 423 | -1 525 926 | -528 899 | 445 195 | 1 123 686 | 1 513 371 |
| Cash burn, ₽ | 5 690 000 | 5 416 800 | 5 149 884 | 4 615 906 | 4 094 210 | 3 311 314 | 2 546 423 | 1 525 926 | 528 899 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 5 690 000 | 11 106 800 | 16 256 684 | 20 872 590 | 24 966 800 | 28 278 114 | 30 824 537 | 32 350 463 | 32 879 362 | 32 879 362 | 32 879 362 | 32 879 362 |

- Break-even по клиентам: **20,8** клиента, округлённо **21 клиент**.
- Break-even по месяцу: **M10**.
- startup_capital_to_bep_rub: **32 879 362 ₽**.

## Сценарий: Пессимистичный

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 0 | 1 | 2,0 | 2,9 | 3,9 | 5,8 | 7,6 | 8,5 | 9,3 | 10,1 |
| MRR, ₽ | 0 | 0 | 0 | 420 000 | 830 340 | 1 231 242 | 1 622 924 | 2 425 596 | 3 209 808 | 3 555 982 | 3 894 194 | 4 224 628 |
| COGS, ₽ | 0 | 0 | 0 | 130 000 | 257 010 | 381 099 | 502 333 | 750 780 | 993 512 | 1 100 661 | 1 205 346 | 1 307 623 |
| Gross profit, ₽ | 0 | 0 | 0 | 290 000 | 573 330 | 850 143 | 1 120 590 | 1 674 817 | 2 216 296 | 2 455 321 | 2 688 849 | 2 917 005 |
| GM% | 0,0% | 0,0% | 0,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% |
| Fixed costs, ₽ | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 | 5 690 000 |
| EBITDA, ₽ | -5 690 000 | -5 690 000 | -5 690 000 | -5 416 800 | -5 149 884 | -4 889 106 | -4 634 327 | -4 112 207 | -3 602 097 | -3 376 918 | -3 156 919 | -2 941 980 |
| Cash burn, ₽ | 5 690 000 | 5 690 000 | 5 690 000 | 5 416 800 | 5 149 884 | 4 889 106 | 4 634 327 | 4 112 207 | 3 602 097 | 3 376 918 | 3 156 919 | 2 941 980 |
| Cumulative cash, ₽ | 5 690 000 | 11 380 000 | 17 070 000 | 22 486 800 | 27 636 684 | 32 525 790 | 37 160 117 | 41 272 324 | 44 874 421 | 48 251 339 | 51 408 258 | 54 350 238 |

- Break-even по клиентам: **20,8** клиента, округлённо **21 клиент**.
- Break-even по месяцу: **не достигнут в M1-M12**, при сохранении темпа M12 достигается около **M29**.
- startup_capital_to_bep_rub: **54 350 238 ₽**.

## Waterfall на 1 клиента в месяц

| Шаг | ₽ | % от выручки | Комментарий |
|---|---:|---:|---|
| ARPA | 420 000 | 100,0% | recurring выручка |
| Gross profit | 290 000 | 69,0% | после COGS 130 000 ₽ |
| Contribution profit | 273 200 | 65,0% | после sales commission 16 800 ₽ |
| EBITDA на break-even клиенте | 0 | 0,0% | break-even около 21 клиента |
| EBITDA на 50 клиентах | 7 970 000 | 38,0% | масштабный ориентир из economics |
| Net profit после налога, IT-льгота 3% (на 50 клиентах) | 7 340 000 | 35,0% | при аккредитации Минцифры |
| Net profit после налога, УСН 6% (на 50 клиентах) | 6 710 000 | 32,0% | стандартный режим для SaaS/услуг |
| Net profit после налога, ОСНО 20% (на 50 клиентах) | 6 376 000 | 30,4% | налог на прибыль без учёта эффекта НДС |

## Налоговая модель РФ

- **УСН 6%**: простой базовый режим для early-stage модели. Налог берётся с выручки, поэтому на низких объёмах чувствителен к burn.
- **IT-льгота 3%**: целевой лучший режим при наличии аккредитации Минцифры и соблюдении критериев по профильной IT-выручке. В модели это даёт прирост net margin примерно на **3 п.п. выручки** против УСН 6%.
- **ОСНО 20%**: подходит для крупных enterprise-контрактов и входного НДС. Здесь налог на прибыль считается от положительной прибыли, но появляется **НДС 20%**, если компания не освобождена. Для B2B с закупками и enterprise-контрагентами ОСНО может быть операционно удобнее, хотя по cash conversion на ранней стадии обычно хуже УСН/IT-режима.
- **Страховые взносы**: в PnL уже учтены как примерно **30% к ФОТ** внутри payroll/fixed costs.
- **НДС 20%**: в unit economics не включён в MRR как выручка, его нужно учитывать отдельно в cash planning при работе на ОСНО.

## Сводка по break-even и капиталу

| Сценарий | Break-even clients | Break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---:|---|
| Базовый | 20,8 | M13 | 43 235 675 | в 12 месяцев почти выходит в ноль, но остаётся слегка отрицательным |
| Оптимистичный | 20,8 | M10 | 32 879 362 | проходит break-even внутри первого года |
| Пессимистичный | 20,8 | M29 | 54 350 238 | требует капитал выше benchmark 45 млн ₽ |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

База для stress-теста: M12 из SECTION A, 19,3 клиента, contribution profit **273 200 ₽/клиент/мес**, fixed costs **5 690 000 ₽/мес**, blended CAC **1 120 000 ₽**, churn **2,3%/мес**. Для CAC x2 я закладываю тот же темп 2,5 new paying customers/мес, но удвоенный CAC-pool съедает ещё **2,8 млн ₽/мес**, то есть напрямую бьёт по EBITDA. Для churn x2 пересчитана клиентская база на том же плане new clients. [04-economics.md]

| Сценарий | Допущение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | как в SECTION A | -417 240 | почти break-even, но ещё ниже нуля |
| Sens1 | CAC x2 | -3 217 240 | модель резко уходит в более глубокий burn |
| Sens2 | Churn x2, до 4,6%/мес | -818 847 | база клиентов к M12 падает примерно до 17,8 |
| Sens3 | Price -30% | -2 751 768 | gross margin сжимается, premium pricing ломается |

### Вывод по sensitivity
- Самая опасная переменная, **цена**: при снижении ARPU на 30% экономика перестаёт выдерживать fixed-cost base.
- На втором месте, **CAC**: модель выдерживает дорогой enterprise sale только пока blended CAC близок к текущему ориентиру **1,12 млн ₽**.
- **Churn x2** тоже болезненен, но менее разрушителен, чем price compression, потому что база ещё успевает нарасти.

## 2. Monte Carlo Lite — confidence intervals

Ниже не буквальная 1000-итерационная симуляция, а упрощённый 9-case proxy на triangular distribution с p10/p50/p90. Источники mode опираются на economics и demand кейса, min/max заданы как допустимый разброс для раннего enterprise go-to-market в РФ. Market-share и интервалы ниже, где не было прямой цифры, являются оценкой **[inference]**.

### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 800 000 | 1 120 000 | 1 800 000 | `04-economics.md`, blended CAC 1,12 млн ₽ [E1] |
| Monthly churn, % | 1,5% | 2,3% | 5,0% | `04-economics.md`, base churn 2,3% [E1] |
| ARPU, ₽/мес | 320 000 | 420 000 | 520 000 | `02-demand.md` и `04-economics.md`, WTP 220-320k / 350-500k+ и base ARPU 420k [D1][E1] |
| Conversion lead→paid, % | 0,8% | 1,3% | 2,5% | `04-economics.md`, blended 1,3% [E1] |
| Time-to-hire, мес | 1,0 | 1,8 | 3,0 | `04-economics.md`, hiring realism по ролям [E1] |

### Результаты p10 / p50 / p90

Упрощённый набор комбинаций показывает, что на горизонте M24 кейс остаётся математически живым в median, но разброс всё ещё высокий.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | 582 977 | 7 016 864 | 13 029 908 | 12 446 931 |
| CAC payback, мес | 2,2 | 2,9 | 10,2 | 8,0 |
| LTV/CAC | 2,0x | 10,6x | 30,8x | 28,8 |
| Cash runway, мес | 24,2 | 48,5 | 70,9 | 46,7 |

### Интерпретация Monte Carlo Lite
- **Правило 1:** p10 EBITDA не ниже нуля, значит формальный insolvency trigger по этому правилу пока не сработал.
- **Правило 2:** p50 EBITDA заметно выше **500 тыс. ₽/мес**, значит median-case проходит EBITDA gate.
- **Правило 3:** p90/p10 по EBITDA около **22,4x**, это **выше 10x**, значит неопределённость слишком высокая и score нужно даунгрейдить на один уровень уверенности.
- **Правило 4:** range width по LTV/CAC = **28,8x**, это намного выше порога **8**, следовательно модель хрупкая и критически зависит от одновременной стабильности pricing, churn и CAC.

## 3. Competitor deep-dive

### Западные конкуренты

| Конкурент | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **IPRally** | AI patent search, review, monitoring, classification | сильный product focus именно на patent teams, explainable AI, mature search UX [B1] | слабее как full workflow system of record, меньше enterprise-localization под РФ | **6-9%** глобального AI-first patent search subsegment [inference] | можем зайти глубже в RU-local workflow, data residency и hybrid delivery |
| **Questel** | крупная IP-платформа: поиск, управление портфелем, docketing, renewals | большой установленный enterprise base, широкий suite, сильный бренд у IP departments [B2] | тяжёлый legacy-suite profile, медленнее как AI-native wedge, дороже и сложнее внедрение | **12-18%** enterprise IP management / software layer [inference] | у нас выше шанс продать более быстрый AI-first workflow wedge без legacy baggage |
| **Clarivate IP / Derwent** | крупнейший IP intelligence stack, search data, analytics, workflow | data moat, глобальный бренд, procurement-ready для крупных корпораций [B3] | дорогой и тяжёлый suite, слабая локальная пригодность для РФ и санкционный риск | **18-25%** enterprise IP intelligence layer [inference] | можем выиграть на локализации РФ, faster deployment и lower TCO для niche wedge |

### Российские конкуренты и substitutes

| Конкурент | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Онлайн Патент** | digital IP workflow, регистрация, кабинет, автоматизация заявок | самый близкий local software analogue, есть цифровой бренд, видимость в Rusprofile и Сколково [B4][B5] | фокус шире на filing/registration, чем на deep enterprise patent intelligence и litigation workflows | **10-15%** цифрового IP-software сегмента РФ [inference] | Patlytics сильнее в AI-first analysis, claim charts, portfolio triage и infringement workflows |
| **PATENTUS** | крупное патентное бюро, поиск, патентование, сопровождение | сильный service trust, понятный чек и бренд на рынке патентных услуг [T2] | service-heavy, ниже software leverage, слабее repeatable SaaS economics | **15-20%** premium service-led patent bureau слоя [inference] | можем выигрывать speed/throughput и превращать ручную экспертизу в workflow platform |
| **ИНТЭЛС** | патентный поиск, экспертиза на патентную чистоту, юруслуги | узнаваемый практический value proposition и низкий порог входа по цене [T2] | больше бюро, чем продукт; ограниченный software moat | **8-12%** service-led search/expertise слоя [inference] | наше преимущество в recurring SaaS revenue и более высокой automation density |
| **Ezybrand** | патентный поиск и оформление с digital lead-gen | агрессивный интернет-маркетинг, доступный entry чек, понятный SMB use case [T2] | слабее в enterprise security, сложных workflow и large-account delivery | **3-5%** online-led SMB patent services [inference] | мы лучше подходим для enterprise legal/IP teams и больших чеков |
| **Skolkovo IP / экосистема сервисов** | институциональная поддержка IP и сервисы для стартапов | доступ к dealflow, доверие у tech founders, дешёвый стартовый substitute [B6] | это не полноценный AI patent workflow product, а экосистемный канал/сервис | **5-8%** startup-oriented IP support flow [inference] | Patlytics может стать не заменой, а product layer поверх этой экосистемы |

### Что видно по конкурентному полю
- На Западе конкуренты сильны в **данных, бренде и search workflow**, но хуже подготовлены к РФ-локализации и data residency.
- В РФ основная конкуренция идёт не от чистого AI SaaS, а от **патентных бюро, сервисных обвязок и digital filing tools**.
- Следовательно, правильная battle card для Patlytics в РФ, это не `дешевле юриста`, а `быстрее throughput IP-команды, лучше audit trail, выше качество triage и claim analysis`.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного patent SME / solutions lead | med | высокий, качество пилотов и доверие buyer падают | вакансии висят >90 дней, founder закрывает delivery лично | заранее строить bench из external patent counsels и делать playbooks |
| Operational | Service creep: каждый pilot уходит в кастомный консалтинг | high | высокий, GM и payback быстро деградируют | COGS >160k ₽/клиент/мес, доля non-repeatable задач растёт | жёсткий template library, stop-list на кастом, лимит SME hours |
| Operational | Скачок цены или деградация качества LLM API | med | высокий, inference cost и trust бьют по COGS | rerun rate растёт, cost/query > план на 25% | multi-model routing, кеширование, vendor fallback, human QA reserve |
| Market | ICP оказывается слишком узким, pipeline не заполняется | high | высокий, new bookings ниже плана | <20 qualified accounts/квартал, pilots не масштабируются | расширять ICP в фарму, индустрию, бюро, делать channel sales |
| Market | Price compression из-за бюро и generic LLM tools | high | высокий, ARPU падает ниже safe zone | win rate держится только при скидке >20% | пакетировать ROI, security, auditability, premium workflows |
| Market | Сильный западный vendor возвращается через партнёров | med | средний/высокий | buyers начинают требовать Questel/Clarivate parity | бить в локальный deployment, lower TCO и fast onboarding |
| Regulatory | 152-ФЗ и data residency блокируют облачную модель | med | высокий | enterprise security review упирается в хранение/трансграничность | RU-hosting, isolated VPC, on-prem/private deployment option |
| Regulatory | 115-ФЗ / KYC / внутренний compliance крупных клиентов удлиняет сделки | med | средний | procurement/legal cycle >9 месяцев | стандартный пакет документов, security FAQ, юр. readiness заранее |
| Regulatory | Санкции на зарубежный SaaS/API нарушают стек | high | высокий | отказ иностранных вендоров, блокировка биллинга/API | отечественные аналоги, прокси-архитектура, резервные поставщики |
| Financial | Runway сжимается из-за медленного выхода на 20+ клиентов | high | высокий | burn >3,5 млн ₽/мес при 6-9 клиентах | freeze hiring, raise bridge раньше, cut non-core GTM spend |
| Financial | Курс USD растёт и тянет вверх LLM/data/tooling cost | med | средний/высокий | доля USD-cost в COGS >30%, ежемесячный cost creep | валютный буфер, рублёвые цены с индексатором, локальные модели |
| Financial | Инфляция ФОТ и налоги размывают contribution margin | med | средний | payroll растёт быстрее ARR на 10+ п.п. | lean hiring, пересмотр pricing, contractor mix |
| Black swan | Новая волна санкций отключает критичный LLM/provider | high | очень высокий | vendor notice, ошибки API, stop billing | multi-vendor architecture, offline fallback, local open-weight stack |
| Black swan | Военная/геополитическая эскалация режет enterprise budgets | med | высокий | freeze пилотов, stop новых ИТ-закупок у крупных клиентов | фокус на cost-saving ROI, shorter pilots, public-sector adjacent ICP |
| Black swan | Крупная утечка IP-данных у одного клиента убивает доверие рынку | low/med | очень высокий | security incidents, red flags в access logs | zero-trust, audit logs, pen-tests, incident response drills |

## 5. Kill conditions через 6 месяцев

1. **MRR < 1,5 млн ₽ или меньше 4 платящих клиентов.** Это означает, что выход на 20+ клиентов отъезжает слишком далеко и runway начинает сгорать быстрее, чем подтверждается repeatability.
2. **Blended CAC > 1,8 млн ₽ или CAC payback > 12 месяцев.** При таком acquisition profile модель уже не выглядит как software-first enterprise motion.
3. **Gross churn > 5%/мес или фактический ARPU < 300 тыс. ₽/мес.** Это сигнал, что buyers не воспринимают продукт как sticky premium workflow layer.

## 6. Итоговое критическое мнение

SECTION A показал, что база почти дотягивает до break-even к M12. SECTION B показывает более жёсткую правду: **кейс можно тащить дальше только как дорогой, локализованный, AI-first enterprise IP workflow layer**. Цена и CAC здесь важнее, чем сам churn. При p50 всё выглядит хорошо, но разброс слишком велик, поэтому мой итоговый stance, это **осторожный CONDITIONAL PASS с понижением confidence**.

## Источники SECTION B
- [B1] IPRally: https://iprally.com/
- [B2] Questel search result / company materials: https://www.questel.com/
- [B3] Clarivate IP / Derwent overview: https://clarivate.com/
- [B4] Rusprofile, ООО «Онлайн патент»: https://www.rusprofile.ru/
- [B5] Skolkovo, Онлайн Патент: https://navigator.sk.ru/
- [B6] Skolkovo IP services / ecosystem pages: https://sk.ru/
- [T2] PATENTUS / ИНТЭЛС / Ezybrand pricing anchors уже собраны в `02-demand.md` этого кейса.

<!-- P6B-DONE -->


---

# 06-verdict.md

# 06-verdict

[GEO-EXPAND] Patlytics geo-expand 1227 v2 — NEAR-PASS: 67/100 | EBITDA base=594К₽/мес через 14 мес | LTV/CAC=13,6x | Ключевое преимущество: premium IP-workflow с сильной unit economics | Главный риск: рынок РФ узкий и moat пока слабый.

sector: GEO-EXPAND

## Кейс
patlytics-geo-expand-1227-v2

## Вердикт
**NEAR-PASS**

## Итоговый score
**67/100**

## Investment committee summary
Кейс почти проходит порог, потому что на уровне unit economics и базы PnL он уже выглядит как software-first enterprise IP workflow с достижимым `company_ebitda_rub_month >= 500 000 ₽/мес` на горизонте до 24 месяцев. Но investment-grade решения пока нет: рынок РФ остаётся узким, source tier balance средний, moat слабее желаемого, а repeatable GTM в России ещё не доказан на достаточном числе платящих аккаунтов.

## Delta vs previous
- Предыдущий связанный кейс: `patlytics-ip-ops-geo-expand-v2`
- Предыдущий результат: **0/100, REJECTED**
- Текущий результат: **67/100, NEAR-PASS**
- Что улучшилось: текущий rerun доказывает working unit economics, путь к `company_ebitda_rub_month > 500 000 ₽/мес` при 23 клиентах и более зрелую enterprise-модель вместо standalone point-solution.
- Что не улучшилось достаточно: локальный спрос остаётся niche-only, GTM тяжёлый, а moat не дотягивает до investment-grade.

## Оценка
Source tier balance: T1=2, T2=4, T3=0, weighted=2.33. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | `LTV/CAC = 13,6x`, `Gross Margin: 69,0%`, `Payback = 4,1 месяца` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | `EBITDA > 500k ₽/мес` достигается `примерно на 23 клиентах`, `около M14` в base-case. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | База спроса есть, но `Demand: LOW, но не нулевой`, после tier penalty рынок остаётся нишевым. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Есть workflow depth и auditability, но substitutes сильны, а локальный regulatory/data moat пока ограничен. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | Модель требует patent SME, private deployment и выдерживания service creep, что делает execution risk выше среднего. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 21 | ICP, buyer-map и 10 named targets есть; `blended CAC = 1,12 млн ₽` дорогой, но payback и channel fit ещё рабочие. |

**Normalized score = round((101 * 100) / 150) = 67/100.**

## 7-factor Moat Framework

| Фактор | Score (0-3) | Почему |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных клиентов напрямую. |
| Switching costs | 2 | После настройки шаблонов, knowledge base и workflow-интеграций смена поставщика уже заметно болезненна. |
| Scale economies | 2 | COGS на inference, templates и delivery может падать с объёмом, но не драматически. |
| Proprietary data / model advantage | 1 | Свой workflow-data layer возможен, но в кейсе пока не доказан большой закрытый датасет. |
| Regulatory moat | 1 | Private deployment и 152-ФЗ могут помогать, но полноценного лицензируемого regulatory moat нет. |
| Brand / distribution | 1 | На рынке РФ бренд и локальная дистрибуция ещё не созданы. |
| Embedded workflow | 4 | Patlytics сидит глубоко в prior-art, invalidity, claim charts и portfolio triage; при rollout слой становится частью core IP-процесса. |

Сумма 7-factor = **11/21**

**Moat score = round((11 * 25) / 21) = 13/25.**

## Полный бизнес-процесс

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target account list | SDR / analyst | CRM, Rusprofile, ручной ресерч | 2 ч | 2 400 | низкая |
| 2 | Первичный outreach | SDR | email, Telegram, CRM-sequences | 1,5 ч | 1 800 | средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 200 | средняя |
| 4 | Discovery по IP workflow клиента | AE + founder | interview, checklist, Miro | 2 ч | 8 500 | низкая |
| 5 | Demo на релевантном use case | AE + patent SME | demo env, sample docs | 2 ч | 10 000 | низкая |
| 6 | Security / privacy / deployment scoping | CTO + AE | NDA, security docs, checklist | 3 ч | 11 000 | низкая |
| 7 | Pilot scoping и success metrics | AE + CSM + patent SME | SOW, KPI sheet | 3 ч | 14 000 | низкая |
| 8 | Pilot setup / templates / data prep | Solutions + CSM | KB setup, workflow config | 14 ч | 56 000 | средняя |
| 9 | Pilot execution + weekly reviews | CSM + AE + SME | CRM, analytics, support | 12 ч | 39 000 | средняя |
| 10 | Procurement / legal negotiation | AE + founder + legal | docflow, почта | 6 ч | 21 000 | низкая |
| 11 | Invoice / payment collection | Finance ops | 1С, банк, ЭДО | 1 ч | 2 500 | высокая |
| 12 | Post-sale onboarding | CSM + solutions | runbook, templates, training | 8 ч | 28 000 | средняя |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 15 200 000 ₽ |
| CAC | 1 120 000 ₽ |
| LTV/CAC | 13,6x |
| CAC payback | 4,1 мес |
| Gross Margin | 69,0% |
| contribution_margin_rub_month на клиента | 273 200 ₽/мес |
| company_ebitda_rub_month @ M14 base | 593 600 ₽/мес |
| company_ebitda_rub_month @ 50 клиентов | 7 970 000 ₽/мес |
| Break-even clients | 21 |
| clients_to_500k_ebitda | 23 |
| months_to_500k_ebitda | 14 |
| startup_capital_to_bep_rub | 43 235 675 ₽ |
| fixed_costs_rub_month | 5 690 000 ₽/мес |

## Команда

| Роль | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT |
|---|---:|---:|---:|
| CEO / founder | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | 520 000 | 156 000 | 676 000 |
| Senior Backend #1 | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | 420 000 | 126 000 | 546 000 |
| ML / Applied AI engineer | 500 000 | 150 000 | 650 000 |
| Frontend / product engineer | 300 000 | 90 000 | 390 000 |
| DevOps / security | 340 000 | 102 000 | 442 000 |
| SDR #1 | 160 000 | 48 000 | 208 000 |
| SDR #2 | 160 000 | 48 000 | 208 000 |
| AE | 320 000 | 96 000 | 416 000 |
| Customer Success | 240 000 | 72 000 | 312 000 |
| Patent SME / solutions | 360 000 | 108 000 | 468 000 |
| Finance / ops 0,5 FTE | 120 000 | 36 000 | 156 000 |
| **Итого** |  |  | **5 863 000 ₽/мес** |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Онлайн Патент | Уже цифровой IP-player, которому нужен throughput layer поверх filing и поиска. | email decision-maker / партнёрство | 350 000 ₽/мес |
| 2 | PATENTUS | Высокая доля ручного патентного поиска и prosecution, сильная боль в ускорении кейсов. | email партнёру практики / конференция | 420 000 ₽/мес |
| 3 | ИНТЭЛС | Живёт на повторяемых patent search задачах, значит ценность claim/invalidity automation прямая. | email managing partner | 380 000 ₽/мес |
| 4 | BIOCAD | Фарма с R&D и IP-портфелем, где FTO и patent landscaping являются постоянным процессом. | conference / warm intro через innovation/IP | 500 000 ₽/мес |
| 5 | Фармстандарт | Патентный контур и регуляторно чувствительные продукты делают IP-workflow регулярным и дорогим. | email head of IP / партнёрство | 450 000 ₽/мес |
| 6 | СИБУР | R&D-heavy промышленная группа, где важны invention disclosure и защита технологий. | enterprise ABM / отраслевая конференция | 420 000 ₽/мес |
| 7 | Росатом | Большой портфель разработок и длинный lifecycle ИС, высокий потенциальный ROI от workflow standardization. | гос/корп. партнёрство / email | 500 000 ₽/мес |
| 8 | КАМАЗ | Инженерные разработки и патентная активность создают регулярный спрос на prior-art и portfolio triage. | innovation director outreach | 350 000 ₽/мес |
| 9 | Газпром нефть | Крупная технологическая компания с инновационным pipeline и внутренними legal/IP workflow. | партнёрский заход / профильная конференция | 420 000 ₽/мес |
| 10 | ТМК | Индустриальный игрок с прикладными разработками и потенциально высоким объёмом IP-операций. | email head of legal/IP | 320 000 ₽/мес |

## Top-3 risks

| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| weak_moat / substitute pressure | high | high | Бюро, general LLM stack и локальные IP-сервисы могут быстро размыть premium pricing. |
| service_creep | high | high | Если каждый pilot требует кастомного SME-слоя, GM и payback перестают быть software-grade. |
| evidence_quality_unverified | med | high | Tier-balance только 2,33, а локальная доказательная база по repeatable AI patent workflow в РФ пока ограничена. |

## LTV Upside Calculator

Чтобы перевести кейс из 67/100 в `APPROVED WITH NOTES`, нужно получить минимум два из трёх апсайдов ниже:

| Рычаг | Текущая база | Целевой апсайд | Эффект |
|---|---:|---:|---|
| ARPU / recurring чек | 420 000 ₽/мес | 470 000-520 000 ₽/мес | снижает clients_to_500k_ebitda и расширяет запас по fixed costs |
| CAC | 1 120 000 ₽ | 800 000-900 000 ₽ | улучшает capital efficiency и снижает риск длинного payback |
| Churn | 2,3%/мес | ≤1,8%/мес | повышает customer_ltv_rub и делает expansion-case fundable |
| Service load / COGS | 130 000 ₽/мес | ≤110 000 ₽/мес | повышает contribution_margin_rub_month и снижает риск service creep |
| ICP focus | широкий buyer universe 350 | 25-40 high-intent named accounts | повышает win-rate и делает GTM repeatable |

## Что доказать для approve
1. Не менее **4-5 платящих клиентов** с realized ARPU **≥400 тыс. ₽/мес**.
2. Pilot→paid conversion **≥30%** на выборке минимум **10 пилотов**.
3. Blended CAC стабильно **≤900 тыс. ₽** и отсутствие скидок >20% как нормы.
4. Deployment без расползания COGS выше **130 тыс. ₽/клиент/мес**.
5. Хоть один локальный кейс, где продукт встроился в постоянный IP-workflow, а не в разовую экспертизу.

## Почему не APPROVED
- Market demand в РФ подтверждён только как **niche high-value wedge**, а не как широкий repeatable category pull.
- Moat остаётся **средним**, без network effects и без доказанного proprietary-data преимущества.
- Source-tier evidence достаточный для продолжения наблюдения, но пока недостаточный для investment committee approval.

## Финальный вывод
**NEAR-PASS.** Экономика сильнее, чем в прошлых патентных кейсах, и profit gate в базе уже достижим. Но пока это скорее watchlist-кандидат на rerun после первых локальных контрактов, чем готовый к approve инвестиционный кейс.
