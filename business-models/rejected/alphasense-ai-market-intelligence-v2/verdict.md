# AlphaSense AI Market Intelligence v2 — Full Verdict Package
> Скомпилированный пакет стадий P0/P3/P4/P5/P6/P7 для публикации в GitHub.

## Файл: 00-brief.md

# Краткий бриф

## Кейс
AlphaSense, AI-рынoчная аналитика и enterprise research для strategy, corpdev и M&A-команд

## Почему открыт
- Сигнал описывает самостоятельный GEO-EXPAND wedge: AI-first слой для enterprise research, market intelligence и синтеза внешних и внутренних источников для strategy, corpdev, IR и M&A-команд.
- В открытых кейсах в `pipeline/cases/` нет достаточно близкого кейса именно про AI market intelligence для корпоративной стратегии и research workflow как отдельный платёжеспособный контур.
- Порог Program 1 проходит: raw-файл даёт потенциал 800 000–3 000 000 ₽ EBITDA в месяц, а масштабы AlphaSense с >$500M ARR и 6 500+ корпоративных клиентов подтверждают high-value enterprise категорию.

## Что проверить дальше
- Насколько в РФ этот wedge можно локализовать без доступа к западным premium research-источникам и какие локальные базы данных дадут достаточную глубину.
- Кто станет первым покупателем: strategy, corpdev, IR, private equity, large enterprise procurement intelligence или интеграторы.
- Можно ли поднять экономику через private deployment, managed research workflows и интеграции с внутренними документами клиента.

## Следующий этап
P3-demand-validation.

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: false
source_raw: 2026-04-24-geo-expand-alphasense-ai-rynochnaya-analitika-i-enterprise-research.md
created: 2026-04-24T11:53:00+03:00
---

# 01-intake

## Кейс
alphasense-ai-market-intelligence-v2

## Тип сигнала
new

## Основание создания
Сигнал проходит как новый кейс: в `pipeline/cases/` нет открытого case по AI market intelligence для enterprise research, strategy и corpdev-команд, а заявленный EBITDA-потенциал выше минимального порога Program 1.

## Краткий контекст
AI-платформа собирает earnings calls, filings, broker research, expert calls и внутренние документы в одном workflow, чтобы ускорить исследование рынков, due diligence и подготовку стратегических решений. Для РФ гипотеза выглядит релевантной для крупных компаний, инвестиционных команд и контуров competitive intelligence, где ручной research дорогой и медленный.

## Ключевые сигналы из raw
- CNBC указывает на быстрый рост AlphaSense, оценку $4 млрд и проникновение в 88% компаний S&P 100.
- Официальный релиз AlphaSense подтверждает более $500 млн ARR и 6 500+ корпоративных клиентов.
- В РФ есть частичные аналоги в risk/compliance, но не полноценный слой AI market intelligence enterprise-уровня.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить локализуемость источников, профиль покупателя в РФ и реалистичность high-ticket сервисной упаковки.

## Файл: 02-demand.md

# Demand Validation

## Verdict
Предварительно: **PASS TO NEXT STAGE**.

Почему не early reject:
- Спрос по прямым формулировкам в РФ нишевый, но не нулевой: `анализ рынка` = MEDIUM, score 32; `стратегический анализ` = MEDIUM, score 30; узкие формулировки `market intelligence` и `M&A аналитика` низкие, что типично для enterprise-category с продажей через direct sales, а не через массовый search intent. [T1]
- Profit Gate проходит в нескольких сценариях: 6 клиентов по 120 тыс. ₽/мес при 75% GM дают ~540 тыс. ₽ EBITDA/мес; 3 private-deploy клиента по 350 тыс. ₽/мес при 65% GM дают ~683 тыс. ₽ EBITDA/мес; 2 enterprise annual контракта по 4.2 млн ₽/год дают ~455 тыс. ₽ EBITDA/мес, а с 3-м контрактом уже ~683 тыс. ₽/мес. [T2]

## Demand signals
- `анализ рынка` через multi-demand: demand=MEDIUM, score=32, HH vacancies=29,571, Yandex suggest=100, Google Trends RU=10. [T1]
- `стратегический анализ`: demand=MEDIUM, score=30, HH vacancies=7,666, Yandex suggest=100. [T1]
- `конкурентная разведка`: demand=LOW, score=22, HH vacancies=104. [T1]
- `market intelligence`: demand=LOW, score=18, HH vacancies=39. [T1]
- `M&A аналитика`: demand=LOW, score=7, HH vacancies=77. [T1]

Интерпретация: в РФ широкая боль существует под более приземлёнными JTBD, например анализ рынка, стратегический анализ, конкурентный мониторинг, vendor scanning и due diligence support. Западный ярлык `market intelligence` почти не является поисковым языком закупки. Это снижает PLG-потенциал, но не убивает enterprise-led продажи. [T1][T2]

## Competitors and pricing
### Прямые и смежные аналоги
1. **Crunchbase Pro**: от **$99/мес** при annual billing. Используется для company research, funding, competitor mapping, list building. Это более лёгкий SMB/VC-comparable, но доказывает денежный floor за research tooling. [T2]
2. **Similarweb Team / Sales Intelligence**: стартовые цены публично показываются от **$14,000/год** и отдельные self-serve планы от **$199/мес** на некоторых страницах продукта. Это уже ближе к paid market intelligence для strategy/growth команд. [T2]
3. **Контур.Фокус**: тарифы публично от **33,500 ₽/год**, расширенные пакеты от **89,000 ₽/год**. Это не full market-intelligence stack, но в РФ подтверждает WTP за corporate intelligence/data-room слой. [T2]
4. **Тelemetr**: от **4,900 ₽/мес**, **21,000 ₽/мес**, **49,000 ₽/мес** по публичным тарифам. Это adjacency по competitive/channel intelligence в Telegram. [T2]
5. **TGStat**: публичные premium/analytics-пакеты от **3,360 ₽/мес**, **6,720 ₽/мес**, **20,790 ₽/мес**. Ещё один сигнал, что рынок платит за мониторинг, аналитику и поиск инсайтов. [T2]

Вывод по конкурентам: в РФ уже оплачиваются data + intelligence инструменты в диапазоне от нескольких тысяч ₽/мес за vertical intelligence до десятков тысяч ₽/год за corporate data access и выше в enterprise sales motion. Для AI-first research cockpit реалистичный стартовый чек выглядит как **120–350 тыс. ₽/мес** за команду или **1.2–4.2 млн ₽/год** за enterprise account. [T2][T3]

## Telegram bots/services in RU
Проверка обязательного RU-контура:
- **TGStat**: развитый analytics-сервис по Telegram с публичными платными тарифами. [T2]
- **Telemetr**: сервис аналитики и конкурентного мониторинга Telegram-каналов с платными пакетами. [T2]
- **Datafan / Popsters / LiveDune** используются как смежный social intelligence стек, но больше про SMM и channel analytics, а не corpdev research. [T2]

Вывод: в Telegram already exists платёжеспособность за monitoring/intelligence, но эти продукты покрывают канал/медиа слой, а не synthesis по компаниям, рынкам, M&A и strategy memos. То есть Telegram-рынок полезен как дополнительный datasource/integration wedge, а не как основной product definition. [T2]

## WTP, proof of willingness to pay
1. **Публичные цены на comparable tools** показывают устойчивую готовность платить за research/data access: от 33.5 тыс. ₽/год у Контур.Фокус до 4.9–49 тыс. ₽/мес у Telemetr и 3.36–20.79 тыс. ₽/мес у TGStat, плюс $99/мес у Crunchbase Pro и 5-значные annual контракты у Similarweb Team. [T2]
2. **AlphaSense reported >$500M ARR и 6,500+ customers** в публичных материалах компании, что подтверждает глобальную готовность enterprise-клиентов платить за AI-assisted market intelligence как отдельную категорию. Это нельзя напрямую переносить на РФ, но это сильное доказательство category-level WTP. [T2]
3. **HH.ru вакансии** по близким функциям (`анализ рынка`, `стратегический анализ`) исчисляются тысячами и десятками тысяч, то есть компании уже держат дорогой human workflow. Если продукт экономит хотя бы 0.5 FTE аналитика или ускоряет board/M&A prep, чек **120–350 тыс. ₽/мес** выглядит рациональным. [T1][T2]

Итог по WTP: **подтверждён умеренно-сильно**, но только для mid-market/enterprise motion с внедрением и вертикализированными datasource. Для pure self-serve продукта доказательств недостаточно. [T1][T2]

## Market sizing
### Assumptions
- FX для перевода: **74.835 ₽/$**. [T1]
- Top-down anchor: мировой рынок data & analytics software **$175.17B**. Для addressable wedge market-intelligence/research workflow беру **2.0%** как консервативную долю knowledge/research-intelligence слоя внутри broader analytics stack. Это inference, не прямая quoted category. [T1]
- РФ enterprise software рынок: **~246.7 млрд ₽** в 2024. [T2]
- Bottom-up buyers universe: ~**900** потенциальных организаций в РФ, где такой продукт реалистично покупается (крупные корпорации, публичные компании, крупные банки, PE/VC/platform teams, industrial холдинги, integrators/consultancies). [T2]
- Need penetration: **35%** компаний имеют регулярный research / strategy / corpdev workflow с повторяемой болью. [T1][T2]
- Средний ARR: **900 тыс. ₽/год** на 3–8 seat team plan, либо эквивалент blended mix self-serve + managed research. [T2][T3]

### Расчёты
Top-down:
- TAM global = 175.17B$ × 2.0% = **3.50B$** = **261.9 млрд ₽**. [T1]
- Russia share proxy = 246.7 млрд ₽ / (global enterprise software ~ $750B = 56.1 трлн ₽) ≈ **0.44%**. Это proxy через software-spend share, не прямой category share. [T2][T3]
- TAM RF = 261.9 млрд ₽ × 0.44% = **1.15 млрд ₽**. [T1][T2][T3]
- SAM RF = TAM RF × 35% target-fit = **403 млн ₽**. [T1][T2]
- SOM Y1 = 3% SAM = **12.1 млн ₽**. [T2]
- SOM Y3 = 10% SAM = **40.3 млн ₽**. [T2]

Bottom-up:
- Total buyers = 900. [T2]
- % with need = 35%. [T1][T2]
- ARR avg = 900 тыс. ₽/год. [T2][T3]
- SAM bottom-up = 900 × 35% × 0.9 млн ₽ = **283.5 млн ₽**. [T2]
- SOM Y1 bottom-up = 5% = **14.2 млн ₽**. [T2]
- SOM Y3 bottom-up = 12% = **34.0 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 3.50B$ / 261.9 млрд ₽ [T1] | — | — | top-down |
| TAM (РФ) | 1.15 млрд ₽ [T1][T2][T3] | 810 млн ₽ (900 × 0.9 млн ₽) [T2] | diff ~1.4x, допустимо; top-down шире, включает не только core buyers | **lower = 810 млн ₽** |
| SAM (РФ) | 403 млн ₽ [T1][T2] | 283.5 млн ₽ [T2] | diff ~1.42x, допустимо; bottom-up строже по ICP | **lower = 283.5 млн ₽** |
| SOM Y1 | 12.1 млн ₽ | 14.2 млн ₽ | diff ~17%, близко | **используем 12.1 млн ₽** |
| SOM Y3 | 40.3 млн ₽ | 34.0 млн ₽ | diff ~19%, близко | **используем 34.0 млн ₽** |

### 10 реальных buyers для bottom-up sanity check
1. Сбер
2. Яндекс
3. МТС
4. VK
5. Ростелеком
6. Северсталь
7. Норникель
8. АФК Система
9. X5 Group
10. Магнит

Почему они подходят: у всех есть strategy / M&A / IR / market research / innovation / procurement intelligence контуры и бюджеты на внешние данные, консалтинг или internal analyst teams. [T2]

Sanity check:
- SOM Y1 12.1 млн ₽ при ARR 0.9 млн ₽ = ~13–14 клиентов в год.
- При average deal cycle 4–6 месяцев это тяжело, но реалистично для founder-led enterprise motion, особенно если начать с 3–5 lighthouse клиентов и upsell managed research/private deployment. [T2]
- SOM Y1 = 4.3% от preferred SAM, что укладывается в норму и не выглядит overclaiming. [T2]

## Profit Gate
### Сценарий 1: team subscription
- 6 клиентов × 120 тыс. ₽/мес = 720 тыс. ₽ MRR.
- Gross margin 75%, OPEX lean ops ~0.4 выручки.
- EBITDA ≈ **540 тыс. ₽/мес**.
- Gate: **PASS**.

### Сценарий 2: enterprise/private deployment
- 3 клиента × 350 тыс. ₽/мес = 1.05 млн ₽ MRR.
- Gross margin 65% с учётом onboarding и support.
- EBITDA ≈ **682.5 тыс. ₽/мес**.
- Gate: **PASS**.

### Сценарий 3: hybrid annual contracts
- 2 клиента × 4.2 млн ₽/год = 8.4 млн ₽ ARR.
- Это ~700 тыс. ₽ выручки/мес.
- При 65% margin EBITDA ~455 тыс. ₽/мес, то есть **ниже gate**.
- С 3-м annual клиентом EBITDA ~683 тыс. ₽/мес.
- Gate: **PASS при 3+ клиентах**, иначе borderline.

Итог: Profit Gate **проходим**, если продукт идёт не как дешёвый self-serve, а как B2B enterprise tool с AI synthesis, private datasource integration, analyst workflow automation и опционально managed layer. [T2]

## Key risks
- В РФ низкий search-intent именно по формулировке `market intelligence`; потребуется сильный sales-led packaging на языке стратегии, конкурентного мониторинга, vendor scouting, M&A screening. [T1]
- Доступность premium зарубежных источников ограничена, значит ценность надо собирать из локальных реестров, новостей, тендеров, Telegram, корпоративных сайтов, внутренних документов клиента. [T2]
- Без вертикализации продукт рискует остаться «ещё одним AI search». Лучшая позиция: strategy/copilot для конкретных команд, например corpdev, procurement intelligence, IR, industrial strategy. [T2]

## Recommendation
Идти дальше, но с жёстким фокусом:
- ICP: крупные и upper-midmarket компании с постоянным strategy/corpdev workflow.
- Offer: private research workspace + datasource connectors + memo generation + monitoring.
- Pricing test: 120 тыс. ₽/мес team plan, 250–350 тыс. ₽/мес enterprise plan, 1.8–4.2 млн ₽/год annual private deployment.
- First pilot thesis: заменить кусок ручного analyst workflow, а не продавать «AI для всего research». [T2]

## Sources
- [T1] multi-demand endpoint `http://172.18.0.1:9001/multi-demand?keyword=...` for keywords `анализ рынка`, `стратегический анализ`, `конкурентная разведка`, `market intelligence`, `M&A аналитика`.
- [T1] Банк России, курсы валют, USD/RUB на 24.04.2026.
- [T2] AlphaSense company materials / press coverage on ARR and customer count.
- [T2] Crunchbase pricing page.
- [T2] Similarweb pricing pages.
- [T2] Контур.Фокус pricing page.
- [T2] Telemetr pricing page.
- [T2] TGStat pricing / analytics page.
- [T2] Strategy Partners / TAdviser summaries on Russian enterprise software market.
- [T3] Global enterprise software market proxy and category-share inference used only for top-down normalization.

Sources: T1=2, T2=7, T3=1. Primary evidence basis: T2.

## Market Pulse

> Market Pulse 24.04.2026: растущий интерес.

## Файл: 03-solution.md

---
stage: solution
case: alphasense-ai-market-intelligence-v2
date: 2026-04-25
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
AlphaSense, AI-first платформа для market intelligence, strategy research, corpdev, IR и M&A workflow в enterprise-сегменте.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «искать информацию», а дорогой и повторяемый workflow: собрать сигналы по рынку, конкурентам, транскриптам, отчётности и внутренним документам, затем быстро превратить это в decision-ready memo.
2. В локальном контуре правдоподобный wedge выглядит не как массовый self-serve research tool, а как **enterprise research cockpit** для strategy, corpdev, IR, procurement intelligence и investment-style команд.
3. Наиболее сильная упаковка для РФ, это не просто доступ к данным, а **private workspace + коннекторы к внутренним документам + monitoring + AI synthesis + managed onboarding**. [T2][inference]
4. Главный риск, без локальных источников и без вертикального сценария продукт схлопывается в «ещё один AI search», где ценность и willingness to pay быстро размываются. [T2][inference]

## 1. Какую проблему реально покупают

Покупают не `market intelligence` как термин, а ускорение дорогого исследовательского труда:
- собрать конкурентный ландшафт по рынку и компании;
- быстро подготовить strategy memo, board note или due diligence summary;
- мониторить earnings, новости, filings, тендеры, Telegram и корпоративные сайты;
- искать сигналы по сделкам, партнёрам, vendor landscape и новым вертикалям;
- соединить внешние данные с внутренними документами клиента в одном поисково-аналитическом контуре. [T2][inference]

Это painkiller там, где решение стоит дорого, а ошибка в research бьёт по M&A, капвложениям, запуску нового направления или приоритетам CEO-1. Для обычного SMB или разового ресерча продукт слишком тяжёлый. [T2][inference]

## 2. Целевой ICP в локальном контуре

### Primary ICP
- strategy и corporate development команды крупных компаний;
- IR и competitive intelligence функции;
- крупные банки, инвестиционные подразделения, PE/VC platform teams;
- procurement intelligence и vendor-scouting команды;
- интеграторы, advisory и research-heavy консалтинг, где много повторяемого desk research.

### Фильтр на ICP
Клиент подходит, если одновременно есть:
1. повторяемый research workflow минимум еженедельно;
2. стоимость часа аналитика или менеджера достаточно высока;
3. потребность в мониторинге нескольких источников и сущностей;
4. бюджет owner находится на уровне strategy lead, corpdev lead, CDO, IR lead или руководителя функционального блока;
5. готовность покупать не только данные, но и приватный контур работы с внутренними материалами. [T2][inference]

### Нецелевой сегмент
- SMB, которым нужен эпизодический анализ рынка;
- команды без собственного research workflow;
- пользователи, которым достаточно открытых источников и ручного поиска;
- компании, не готовые платить за приватный deployment или управляемый контур.

## 3. Продуктовый wedge

### Core wedge
**Enterprise research cockpit для decision support**
- unified search по внешним и внутренним источникам;
- AI-synthesis и auto-summary по компаниям, темам и рынкам;
- watchlists, alerts и continuous monitoring;
- memo generation для strategy, corpdev, IR и procurement workflows;
- совместная работа команды в защищённом workspace. [T2][inference]

### Почему wedge сильнее обычного AI search
1. **Workflow-specific value**: продукт встраивается в реальные decision loops, а не только отвечает на вопросы. [T2][inference]
2. **Высокая стоимость ошибки**: в strategy и M&A клиент платит не за «поиск», а за сокращение времени и снижение риска пропустить важный сигнал. [T2][inference]
3. **Private data layer**: подключение внутренних документов, research notes и архивов резко повышает switching cost. [T2][inference]
4. **Monitoring layer**: постоянный трекинг компаний, рынков и тем делает использование повторяемым, а не разовым.
5. **Managed onboarding**: без настройки источников, taxonomies и шаблонов мемо ценность раскрывается хуже, поэтому service layer здесь полезен, а не вреден.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- generic AI search для всех knowledge workers;
- ставка только на англоязычную категорию `market intelligence`;
- web-only продукт без приватного контура и без локальных datasource;
- дешёвый self-serve тариф без внедрения и вертикальных шаблонов.

### Вариант, который выглядит реалистично
- enterprise-first продажа в команды strategy, corpdev, IR и procurement intelligence;
- private deployment или хотя бы изолированный workspace;
- локальные и смешанные источники: реестры, новости, тендеры, сайты, Telegram, внутренние документы клиента;
- шаблоны под конкретные workflow: competitor monitoring, market scan, vendor scouting, board brief, M&A pre-screen;
- onboarding как productized service с настройкой watchlists, taxonomy и search recipes. [T2][inference]

## 5. Почему клиент будет покупать именно это, а не текущий стек

У клиента уже есть substitutes:
- ручной research аналитиков;
- консалтинг и ad hoc подрядчики;
- Контур.Фокус, Similarweb, Crunchbase, TGStat, Telemetr и другие точечные источники;
- внутренние knowledge base и папки с документами;
- general-purpose AI search и copilots.

Продукт выигрывает только если даёт одновременно:
1. **один рабочий контур вместо 5-10 разрозненных инструментов**;
2. **быстрый synthesis в memo-ready формате**;
3. **monitoring и alerts без ручного обхода источников**;
4. **совместную работу команды и приватный knowledge layer**;
5. **вертикальную упаковку под strategy/corpdev workflow**, а не просто поиск по документам. [T2][inference]

Если этого нет, клиент останется на наборе точечных data tools плюс ручной analyst workflow.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. pilot с одним конкретным workflow, например competitor monitoring или vendor scouting;
2. подключение локальных внешних источников и внутренних документов клиента;
3. настройка watchlists, тегов, запросов и шаблонов выходных memo;
4. переход от pilot к annual contract или managed subscription;
5. расширение на соседние команды, например strategy → IR → procurement intelligence. [T2][inference]

### Кто должен быть buyer'ом
- head of strategy;
- corpdev lead;
- руководитель competitive intelligence;
- IR lead;
- директор по развитию, трансформации или исследовательскому блоку.

### Кто редко будет настоящим buyer'ом
- отдельный аналитик без бюджетных полномочий;
- массовый SMB-owner;
- casual knowledge worker без повторяемого high-stakes workflow.

## 7. Конкурентная позиция

### Против точечных data tools
Шанс есть, если платформа собирает данные из разных контуров и добавляет synthesis + monitoring, а не просто дублирует один источник.

### Против консалтинга и ручного research
Шанс есть, если время до actionable memo действительно сжимается с дней до часов, а команда может повторять это системно.

### Против general AI search
Шанс есть, если есть приватный deployment, workflow templates, team collaboration и источники, которые не лежат в обычном открытом вебе.

## 8. Основные риски solution-fit

1. **Data coverage risk**: без качественных локальных источников продукт теряет глубину.
2. **Genericity risk**: без вертикального сценария платформа выглядит как generic AI search. [T2][inference]
3. **Long sales cycle risk**: enterprise buyer долго принимает решение и требует proof of trust.
4. **Service creep risk**: onboarding и аналитическая помощь могут превратить продукт в research agency-light. [inference]
5. **Security risk**: работа с внутренними документами требует сильного доверия, приватности и понятного deployment mode.
6. **Category language risk**: термин `market intelligence` сам по себе слаб в локальном inbound, значит GTM должен идти через язык конкретных задач.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- achievable ACV для team, private deployment и managed enterprise plan;
- сколько pilots и annual-клиентов нужно для EBITDA >500k ₽/мес;
- объём service load на onboarding и поддержку;
- CAC и sales cycle для founder-led enterprise motion;
- достаточно ли локальных datasource, чтобы оправдать premium pricing;
- не превращается ли модель в consulting-heavy workflow без product leverage.

## Итог для пайплайна

**P4 пройден условно.**

Кейс выглядит сильным как GEO-EXPAND opportunity для enterprise research cockpit, если продавать его как дорогой workflow layer для strategy, corpdev и competitive monitoring, а не как массовый AI search. Двигать дальше стоит, потому что problem-value и buyer economics правдоподобны, но только при условии, что на P5 подтвердится достаточный ACV и controllable service complexity.

## Источники
- [T2] 02-demand.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/alphasense-ai-market-intelligence-v2/02-demand.md
- [T2] 01-intake.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/alphasense-ai-market-intelligence-v2/01-intake.md
- [T2] 00-brief.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/alphasense-ai-market-intelligence-v2/00-brief.md

Примечание: выводы solution-fit основаны на синтезе P3-demand и материалов кейса; пометки `[inference]` обозначают аналитическую интерпретацию, а не новый первичный источник.

## Файл: 04-economics.md

---
stage: economics
case: alphasense-ai-market-intelligence-v2
date: 2026-04-25
analyst: branch-models-lead
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P5: PASS.**

Кейс проходит инвестиционный фильтр на fund-level economics при условии, что продукт продаётся как **upper-midmarket / enterprise research cockpit** для strategy, corpdev, IR и competitive intelligence, а не как дешёвый self-serve AI search.

Ключевые выводы:
- Blended MRR на клиента в base-case: **220 000 ₽/мес**.
- COGS на клиента: **57 000 ₽/мес**.
- Gross Margin: **74.1%**.
- Fully-loaded blended CAC: **1 034 000 ₽**.
- Benchmark churn для enterprise B2B SaaS: беру **1.8% logo churn в месяц** как консервативный mid-point для high-touch B2B-подписки на базе отраслевых бенчмарков retention/churn. [T4]
- LTV = **9.06 млн ₽**.
- LTV/CAC = **8.8x**.
- CAC Payback = **4.7 мес**.
- Contribution Margin: **72.7%**.
- Break-even: **41 клиент** или **M12** в base ramp.
- При **50 клиентах** проект выходит на **~1.6 млн ₽ EBITDA/мес**, то есть profit gate проходит.

## 1. Pricing и базовые допущения

### ICP для экономики
- Клиент: крупная компания, банк, industrial holding, corpdev / strategy / IR / procurement intelligence команда.
- Sales motion: sales-led, 2-5 месяцев, обычно pilot → annual / rolling contract.
- Delivery: onboarding, настройка watchlists, подключение внутренних документов, шаблоны memo, user training.

### Blended pricing
| Тарифный слой | Доля сделок | Цена, ₽/мес | Комментарий |
|---|---:|---:|---|
| Team plan | 35% | 120 000 | 3-8 пользователей, без private deployment |
| Business plan | 40% | 220 000 | базовый private workspace + monitoring |
| Enterprise plan | 25% | 420 000 | private deployment / повышенный support / security review |

**Blended MRR на клиента = 220 000 ₽/мес**.

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов и обогащение списка | SDR | CRM, LinkedIn/SalesNav-аналоги, Контур.Фокус, TGStat | 35 мин | 1 400 | 40% |
| 2 | Первый outbound / warm intro / партнёрский интро | SDR / CEO | email, Telegram, phone, партнёрская сеть | 20 мин | 1 100 | 25% |
| 3 | Qualification call | SDR | CRM, calendar, call notes | 30 мин | 1 600 | 35% |
| 4 | Discovery c buyer | AE + CEO | Zoom/Meet, AI note taker, шаблон discovery | 60 мин | 5 700 | 30% |
| 5 | Сбор pain points и источников клиента | AE + solutions lead | Notion, CRM, intake template | 90 мин | 7 800 | 30% |
| 6 | Подготовка demo-песочницы и sample memo | Product + ML + backend | internal admin, LLM/RAG stack, dataset connectors | 6 ч | 18 500 | 55% |
| 7 | Demo / workshop | AE + CEO + product | Zoom, demo workspace | 75 мин | 8 400 | 25% |
| 8 | Security / IT review | CTO + AE | security docs, DPA, architecture pack | 4 ч | 13 800 | 20% |
| 9 | Коммерческое предложение и ROI-калькулятор | AE | CRM, CPQ, шаблон ROI | 2 ч | 5 600 | 45% |
| 10 | Negotiation + legal | CEO + AE | contract workflow, e-sign | 5 ч | 19 000 | 20% |
| 11 | Onboarding и настройка workspace | CSM + solutions engineer | product admin, source connectors, training deck | 10 ч | 24 700 | 45% |
| 12 | Запуск usage и первый monthly check-in | CSM | BI dashboard, usage alerts, playbook | 2 ч | 4 600 | 50% |
| 13 | Выставление счёта и оплата | finance ops | ЭДО, банк-клиент, 1С | 40 мин | 1 300 | 70% |

**Итого cost-to-first-payment на 1 нового клиента: ~113 500 ₽ прямого человеческого времени и infra-cost**, но это не весь CAC. Реальный CAC выше из-за неполной конверсии воронки, постоянного FOT sales/marketing и overhead.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / reranking / summarization API | 8 000 | usage-based estimate | high-intent аналитические запросы и memo generation |
| Search / vector / application infra | 12 000 | cloud + search cluster allocation | на активный enterprise workspace |
| Data ingestion / parsing / monitoring | 15 000 | workers + storage + ETL allocation | новости, сайты, документы, watchlists |
| Secure storage / backup / logging | 5 000 | cloud allocation | документы клиента и аудит |
| Customer Success и support | 10 000 | CSM FOT allocation | high-touch adoption layer |
| Onboarding amortization | 5 000 | 60 000 ₽ one-off / 12 мес | productized setup |
| Payment / docs / admin variable | 2 000 | ЭДО + финоперации | низкая доля |

**Итого COGS = 57 000 ₽/клиент/мес**.

### Gross margin
- Revenue per client = **220 000 ₽/мес**
- COGS per client = **57 000 ₽/мес**
- Gross Profit per client = **163 000 ₽/мес**
- **Gross Margin = 74.1%**

## 4. CAC по каналам и воронка

### Воронка по каналам
| Канал | Leads/мес | Meetings | SQL | Pilots | New paying | Lead→Pay conversion |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led outbound | 420 | 24 | 8 | 3 | 0.8 | 0.19% |
| Inbound / content / webinars | 95 | 18 | 7 | 3 | 0.9 | 0.95% |
| Partners / referrals | 30 | 12 | 6 | 2 | 0.5 | 1.67% |
| **Итого / blended** | **545** | **54** | **21** | **8** | **2.2** | **0.40%** |

### Fully-loaded CAC: раскладка по компонентам

#### Канал 1. Founder-led outbound
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 0 | канал не ads-driven | internal model |
| Outbound team FOT (SDR/AE attributed to new) | 525 200 | SDR 180k + AE allocation 224k gross, всё ×1.3 соцвзносы | [T5][T6] |
| Marketing team FOT (partial allocation) | 71 500 | 25% marketing manager 220k gross ×1.3 | [T5] |
| Tools (CRM, Sales Nav, enrichment, call stack) | 55 000 | CRM + prospecting stack | internal model |
| Events/partnerships | 40 000 | roundtables / founder dinners allocation | internal model |
| Overhead multiplier (x1.7) | 484 190 | 0.7 × subtotal 691 700 | enterprise sales sanity |

**Fully-loaded outbound CAC = 1 176 000 / 0.8 = 1 470 000 ₽**.

#### Канал 2. Inbound / content / webinars
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | retargeting + content amplification | internal model |
| Outbound team FOT (AE attributed to new) | 62 400 | 15% AE gross 320k ×1.3 | [T6] |
| Marketing team FOT (partial allocation) | 100 100 | 35% marketing manager 220k gross ×1.3 | [T5] |
| Tools (CRM, webinar, analytics) | 35 000 | martech stack | internal model |
| Events/partnerships | 30 000 | monthly webinar / content event allocation | internal model |
| Overhead multiplier (x1.5) | 173 750 | 0.5 × subtotal 347 500 | mid-market B2B sanity |

**Fully-loaded inbound CAC = 521 250 / 0.9 = 579 000 ₽**.

#### Канал 3. Partners / referrals
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 0 | не используется | internal model |
| Outbound team FOT (SDR/AE attributed to new) | 210 000 | AE 20% + CEO partner time, fully-loaded | [T5][T6] |
| Marketing team FOT (partial allocation) | 0 | маркетинг не основной драйвер | internal model |
| Tools (CRM, legal, partner ops) | 20 000 | partner ops stack | internal model |
| Events/partnerships | 110 000 | rev share, co-marketing, joint events | internal model |
| Overhead multiplier (x1.7) | 238 000 | 0.7 × subtotal 340 000 | enterprise partnership sanity |

**Fully-loaded partner CAC = 578 000 / 0.5 = 1 156 000 ₽**.

### Blended CAC
- Total fully-loaded acquisition spend = **2 275 250 ₽/мес**
- New paying customers = **2.2/мес**
- **Blended fully-loaded CAC = 1 034 000 ₽**

### Sanity check по CAC
- Для enterprise / data-heavy B2B в РФ пользователь дал sanity-range **300-900k ₽**, для complex enterprise motion допускается выход выше диапазона.
- Наш blended CAC **1.03 млн ₽** слегка выше верхней границы, и это оправдано, потому что сделка включает security review, pilot, legal и high-touch onboarding.
- CAC **не выглядит заниженным**. Это важно: underestimating CAC здесь был бы red flag.

## 5. LTV и churn

### Churn benchmark
Для enterprise/high-touch B2B SaaS использую **1.8% logo churn в месяц** как консервативную оценку. Это соответствует примерно **19.6% annual logo churn** и находится в допустимом коридоре для high-touch B2B-подписок; бенчмарки retention/churn указывают, что у более зрелых B2B SaaS gross revenue retention обычно держится в зоне 90%+, а churn materially ниже SMB SaaS. [T4]

### LTV
Формула:

`LTV = (MRR per customer × Gross Margin) / Monthly Churn`

Расчёт:
- MRR per customer = **220 000 ₽**
- Gross Margin = **74.1%**
- Monthly churn = **1.8%**

`LTV = 220 000 × 0.741 / 0.018 = 9 056 667 ₽`

**LTV = 9.06 млн ₽**.

## 6. LTV/CAC

- LTV = **9.06 млн ₽**
- Blended CAC = **1.034 млн ₽**

`LTV/CAC = 9.06 / 1.034 = 8.8x`

**Вывод: выше порога 3:1, инвестиционный фильтр проходит уверенно.**

## 7. CAC Payback

Формула:

`CAC Payback = CAC / MRR per customer`

`1 034 000 / 220 000 = 4.7 мес`

**CAC Payback = 4.7 месяца**, что значительно лучше предельного коридора <12 месяцев, и даже для enterprise-модели выглядит комфортно.

## 8. Contribution Margin

Для contribution margin вычитаю из выручки COGS и чисто переменную sales-комиссию.

- Revenue per client = **220 000 ₽**
- COGS = **57 000 ₽**
- Variable commission / success payout = **3 000 ₽** в среднем на клиента в месяц

`Contribution Margin = (220 000 - 57 000 - 3 000) / 220 000 = 72.7%`

**Contribution Margin = 72.7%**.

## 9. Team & FOT

### Полная команда
| Роль | Функция | Salary gross, ₽/мес | Страх. взносы 30% | FOT fully-loaded, ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder | продажи key accounts, fundraising, partnerships | 700 000 | 210 000 | 910 000 |
| CTO / Tech Lead | архитектура, security, enterprise deployment | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion / API / integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | search / platform / data connectors | 420 000 | 126 000 | 546 000 |
| ML Engineer | ranking, summarization quality, RAG | 500 000 | 150 000 | 650 000 |
| DevOps | infra, observability, security ops | 350 000 | 105 000 | 455 000 |
| Frontend | analyst workspace, dashboards | 300 000 | 90 000 | 390 000 |
| Product Manager | workflow templates, roadmap, adoption | 300 000 | 90 000 | 390 000 |
| Marketing Manager | content, webinars, inbound | 220 000 | 66 000 | 286 000 |
| SDR | outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | discovery, demo, negotiation | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, training, expansion | 240 000 | 72 000 | 312 000 |

**Итого fully-loaded FOT = 5 902 000 ₽/мес**.

### Таблица найма и реализм
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 700 000 | 0 (founder) | 0 | 210 000 | 910 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| AE | 1 | 360 000 | 1.5 | 2.5 | 108 000 | 468 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Product Manager | 1 | 300 000 | 2 | 1.5 | 90 000 | 390 000 |
| Marketing Manager | 1 | 220 000 | 1.5 | 1 | 66 000 | 286 000 |

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO | 910 000 | founder-led start |
| M2 | + CTO | 1 625 000 | архитектура и pre-sales security |
| M3 | + Backend #1 | 2 171 000 | начинается core platform build |
| M4 | + Frontend | 2 561 000 | первая usable analyst UI |
| M5 | + Backend #2 | 3 107 000 | закрываем connectors / platform debt |
| M6 | + ML Engineer | 3 757 000 | качество synthesis и ranking |
| M7 | + DevOps + PM | 4 602 000 | private deployments становятся реалистичны |
| M8 | + Marketing Manager | 4 888 000 | inbound и webinars запускаются |
| M9 | + SDR | 5 122 000 | outbound scale-up |
| M10 | + AE | 5 590 000 | формализуем enterprise sales |
| M11 | + Customer Success | 5 902 000 | onboarding и expansion layer |
| M12 | состав без изменений | 5 902 000 | steady-state team |

Проверка realism:
- В первый месяц нет найма 5+ человек, red flag отсутствует.
- FOT M1-M3 выглядит высоким, но правдоподобным для B2B enterprise SaaS с founder + senior engineering.
- Полный team build занимает 11 месяцев, что соответствует реальному time-to-hire для senior и enterprise roles.

## 10. Fixed costs breakdown

| Компонент fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 5 902 000 | команда из 12 человек |
| Cloud base / corp infra not in COGS | 220 000 | dev/staging, observability, backups |
| Legal / accounting / ЭДО / compliance | 120 000 | договоры, бухгалтерия, security docs |
| Office / coworking / travel | 180 000 | гибридный режим + встречи с enterprise buyers |
| Corp software (Notion, Jira, Slack, Google, BI) | 80 000 | внутренний стек |
| Recruiting / HR / admin reserve | 50 000 | неравномерные расходы |

**Итого fixed costs = 6 552 000 ₽/мес**.

## 11. Break-even

### Break-even по количеству клиентов
- Contribution profit per client = **160 000 ₽/мес**
- Fixed costs = **6 552 000 ₽/мес**

`Break-even clients = 6 552 000 / 160 000 = 40.95`

**Break-even = 41 клиент**.

### Break-even по месяцу
Допущение ramp новых клиентов:
- M1: 0
- M2: 0
- M3: 1
- M4: 2
- M5: 4
- M6: 6
- M7: 9
- M8: 13
- M9: 18
- M10: 24
- M11: 32
- M12: 41

| Месяц | Клиентов на конец месяца | MRR, ₽ | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 560 000 | -1 560 000 |
| M2 | 0 | 0 | 0 | 2 275 000 | -2 275 000 |
| M3 | 1 | 220 000 | 160 000 | 2 821 000 | -2 661 000 |
| M4 | 2 | 440 000 | 320 000 | 3 211 000 | -2 891 000 |
| M5 | 4 | 880 000 | 640 000 | 3 757 000 | -3 117 000 |
| M6 | 6 | 1 320 000 | 960 000 | 4 407 000 | -3 447 000 |
| M7 | 9 | 1 980 000 | 1 440 000 | 5 252 000 | -3 812 000 |
| M8 | 13 | 2 860 000 | 2 080 000 | 5 538 000 | -3 458 000 |
| M9 | 18 | 3 960 000 | 2 880 000 | 5 772 000 | -2 892 000 |
| M10 | 24 | 5 280 000 | 3 840 000 | 6 240 000 | -2 400 000 |
| M11 | 32 | 7 040 000 | 5 120 000 | 6 552 000 | -1 432 000 |
| M12 | 41 | 9 020 000 | 6 560 000 | 6 552 000 | 8 000 |

**Break-even month = M12**.

## 12. Burn-to-breakeven и runway

### Burn-to-breakeven
Суммарный отрицательный EBITDA до выхода в ноль:

`1.56 + 2.275 + 2.661 + 2.891 + 3.117 + 3.447 + 3.812 + 3.458 + 2.892 + 2.400 + 1.432 = 29.945 млн ₽`

Добавляю 20% safety buffer на задержки найма, extra security review, более медленную конверсию и дебиторку:

**Startup capital to breakeven = ~36 млн ₽**.

Это выше порога 10 млн ₽ и выглядит реалистично для enterprise B2B SaaS. Red flag отсутствует.

### Cash runway
При стартовом капитале **45 млн ₽**:
- average burn первых 12 месяцев ≈ **2.5 млн ₽/мес**
- runway ≈ **18 месяцев**

При более агрессивном go-to-market и burn **3.0 млн ₽/мес** runway ≈ **15 месяцев**.

**Вывод:** безопасный стартовый капитал для такого кейса, это **40-45 млн ₽**, лучше **50 млн ₽** с запасом.

## 13. Проверка profit gate

### EBITDA при 50 клиентах
- Revenue = 50 × 220 000 = **11 000 000 ₽/мес**
- Contribution profit = 50 × 160 000 = **8 000 000 ₽/мес**
- Fixed costs = **6 552 000 ₽/мес**
- EBITDA = **1 448 000 ₽/мес**

Даже после консервативного округления и возможного роста support-load проект остаётся **выше 500k EBITDA/мес**.

### Вывод по gate
- EBITDA > 500k ₽/мес при 50 клиентах: **да**
- LTV/CAC > 1:1: **да, 8.8x**
- LTV/CAC > 3:1 для investment-grade: **да**

**Profit Gate: PASS**.

## 14. Главные экономические риски

1. **Риск data-cost creep**: если клиенты требуют дорогие premium datasets и heavy ingestion, COGS может уйти выше 70-80k ₽ на клиента.
2. **Риск service creep**: если каждая сделка превращается в кастомный research managed service, gross margin упадёт ниже 70%.
3. **Риск длинного sales cycle**: blended CAC уже высокий, и при падении конверсии lead→pay ниже 0.3% CAC может уйти в 1.3-1.5 млн ₽.
4. **Риск рынка**: для РФ SAM не бесконечен, поэтому после первых 25-40 клиентов нужен upsell, multi-team expansion или multi-geo стратегия.

## 15. Финальный вывод

Кейс **проходит P5** как инвестиционно интересный niche enterprise SaaS, если держать позиционирование в high-value workflow и не скатываться в generic AI-search.

Что делает экономику рабочей:
- высокий ARPA,
- контролируемый COGS,
- payback < 5 месяцев,
- LTV/CAC заметно выше 3x,
- break-even в районе 41 клиента, а не 80-100.

Что может сломать модель:
- кастомная delivery-heavy работа,
- слабая локальная data coverage,
- удлинение цикла продажи без роста ACV.

## Источники
- [T1] 02-demand.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/alphasense-ai-market-intelligence-v2/02-demand.md
- [T2] 03-solution.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/alphasense-ai-market-intelligence-v2/03-solution.md
- [T3] 01-intake.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/alphasense-ai-market-intelligence-v2/01-intake.md
- [T4] SaaS Capital, 2024 Growth Benchmarks и churn/retention материалы: https://www.saas-capital.com/blog-posts/2024-growth-benchmarks-private-saas-company-data/ ; Bessemer benchmarks / State of the Cloud: https://www.bvp.com/atlas/state-of-the-cloud/ ; ChartMogul SaaS churn benchmarks: https://chartmogul.com/resources/saas-metrics-cheat-sheet/
- [T5] hh.ru, вилки compensation для marketing / senior / tech roles, поисковые и аналитические материалы по зарплатам: https://hh.ru/article/32072 ; https://hh.ru/search/vacancy?text=%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BE%D0%BB%D0%BE%D0%B3 ; https://hh.ru/search/vacancy?text=cto
- [T6] hh.ru, вилки compensation для sales roles: https://hh.ru/search/vacancy?text=SDR ; https://hh.ru/search/vacancy?text=account%20executive

Примечание: расчёты CAC, COGS и FOT являются аналитической моделью для fund-level screening. Там, где нет прямого публичного прайса или payroll disclosure, использован консервативный inference на базе материалов кейса и рыночных бенчмарков.

## Файл: 05-critic.md

# SECTION A — PnL (12 месяцев, 3 сценария)

## 1. Принятые допущения для модели

- ARPA / blended MRR на клиента: **220 000 ₽/мес**.
- COGS на клиента: **57 000 ₽/мес**.
- Gross profit на клиента: **163 000 ₽/мес**.
- Gross margin: **74,1%**.
- Contribution profit на клиента после переменной sales-комиссии 3 000 ₽: **160 000 ₽/мес**.
- Страховые взносы: **~30% к ФОТ**, уже учтены в fully-loaded FOT из economics.
- Fixed costs взяты по ramp из 04-economics.md, а не одной плоской ставкой, чтобы сохранить реалистичный hiring curve M1-M12.
- Base scenario использует исходный ramp клиентов из economics; Optimistic = +25% к клиентской базе; Pessimistic = -25% к клиентской базе, с округлением до целых клиентов.
- Для PnL cash burn считается как отрицательная EBITDA по модулю; cumulative cash показывает накопленный дефицит до точки безубыточности.

## 2. Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 | 8 | 9 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 13 | 18 | 24 | 32 | 41 |
| MRR, ₽ | 0 | 0 | 220 000 | 440 000 | 880 000 | 1 320 000 | 1 980 000 | 2 860 000 | 3 960 000 | 5 280 000 | 7 040 000 | 9 020 000 |
| COGS, ₽ | 0 | 0 | 57 000 | 114 000 | 228 000 | 342 000 | 513 000 | 741 000 | 1 026 000 | 1 368 000 | 1 824 000 | 2 337 000 |
| Gross profit, ₽ | 0 | 0 | 163 000 | 326 000 | 652 000 | 978 000 | 1 467 000 | 2 119 000 | 2 934 000 | 3 912 000 | 5 216 000 | 6 683 000 |
| GM% | 0,0% | 0,0% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% |
| Fixed costs, ₽ | 1 560 000 | 2 275 000 | 2 821 000 | 3 211 000 | 3 757 000 | 4 407 000 | 5 252 000 | 5 538 000 | 5 772 000 | 6 240 000 | 6 552 000 | 6 552 000 |
| EBITDA, ₽ | -1 560 000 | -2 275 000 | -2 658 000 | -2 885 000 | -3 105 000 | -3 429 000 | -3 785 000 | -3 419 000 | -2 838 000 | -2 328 000 | -1 336 000 | 131 000 |
| Cash burn, ₽ | 1 560 000 | 2 275 000 | 2 658 000 | 2 885 000 | 3 105 000 | 3 429 000 | 3 785 000 | 3 419 000 | 2 838 000 | 2 328 000 | 1 336 000 | 0 |
| Cumulative cash, ₽ | 1 560 000 | 3 835 000 | 6 493 000 | 9 378 000 | 12 483 000 | 15 912 000 | 19 697 000 | 23 116 000 | 25 954 000 | 28 282 000 | 29 618 000 | 29 618 000 |

## 2. Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 3 | 3 | 3 | 5 | 6 | 8 | 10 | 11 |
| Total clients | 0 | 0 | 1 | 2 | 5 | 8 | 11 | 16 | 22 | 30 | 40 | 51 |
| MRR, ₽ | 0 | 0 | 220 000 | 440 000 | 1 100 000 | 1 760 000 | 2 420 000 | 3 520 000 | 4 840 000 | 6 600 000 | 8 800 000 | 11 220 000 |
| COGS, ₽ | 0 | 0 | 57 000 | 114 000 | 285 000 | 456 000 | 627 000 | 912 000 | 1 254 000 | 1 710 000 | 2 280 000 | 2 907 000 |
| Gross profit, ₽ | 0 | 0 | 163 000 | 326 000 | 815 000 | 1 304 000 | 1 793 000 | 2 608 000 | 3 586 000 | 4 890 000 | 6 520 000 | 8 313 000 |
| GM% | 0,0% | 0,0% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% |
| Fixed costs, ₽ | 1 560 000 | 2 275 000 | 2 821 000 | 3 211 000 | 3 757 000 | 4 407 000 | 5 252 000 | 5 538 000 | 5 772 000 | 6 240 000 | 6 552 000 | 6 552 000 |
| EBITDA, ₽ | -1 560 000 | -2 275 000 | -2 658 000 | -2 885 000 | -2 942 000 | -3 103 000 | -3 459 000 | -2 930 000 | -2 186 000 | -1 350 000 | -32 000 | 1 761 000 |
| Cash burn, ₽ | 1 560 000 | 2 275 000 | 2 658 000 | 2 885 000 | 2 942 000 | 3 103 000 | 3 459 000 | 2 930 000 | 2 186 000 | 1 350 000 | 32 000 | 0 |
| Cumulative cash, ₽ | 1 560 000 | 3 835 000 | 6 493 000 | 9 378 000 | 12 320 000 | 15 423 000 | 18 882 000 | 21 812 000 | 23 998 000 | 25 348 000 | 25 380 000 | 25 380 000 |

## 2. Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 3 | 3 | 4 | 4 | 6 | 7 |
| Total clients | 0 | 0 | 1 | 2 | 3 | 4 | 7 | 10 | 14 | 18 | 24 | 31 |
| MRR, ₽ | 0 | 0 | 220 000 | 440 000 | 660 000 | 880 000 | 1 540 000 | 2 200 000 | 3 080 000 | 3 960 000 | 5 280 000 | 6 820 000 |
| COGS, ₽ | 0 | 0 | 57 000 | 114 000 | 171 000 | 228 000 | 399 000 | 570 000 | 798 000 | 1 026 000 | 1 368 000 | 1 767 000 |
| Gross profit, ₽ | 0 | 0 | 163 000 | 326 000 | 489 000 | 652 000 | 1 141 000 | 1 630 000 | 2 282 000 | 2 934 000 | 3 912 000 | 5 053 000 |
| GM% | 0,0% | 0,0% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% | 74,1% |
| Fixed costs, ₽ | 1 560 000 | 2 275 000 | 2 821 000 | 3 211 000 | 3 757 000 | 4 407 000 | 5 252 000 | 5 538 000 | 5 772 000 | 6 240 000 | 6 552 000 | 6 552 000 |
| EBITDA, ₽ | -1 560 000 | -2 275 000 | -2 658 000 | -2 885 000 | -3 268 000 | -3 755 000 | -4 111 000 | -3 908 000 | -3 490 000 | -3 306 000 | -2 640 000 | -1 499 000 |
| Cash burn, ₽ | 1 560 000 | 2 275 000 | 2 658 000 | 2 885 000 | 3 268 000 | 3 755 000 | 4 111 000 | 3 908 000 | 3 490 000 | 3 306 000 | 2 640 000 | 1 499 000 |
| Cumulative cash, ₽ | 1 560 000 | 3 835 000 | 6 493 000 | 9 378 000 | 12 646 000 | 16 401 000 | 20 512 000 | 24 420 000 | 27 910 000 | 31 216 000 | 33 856 000 | 35 355 000 |

## 3. Waterfall на steady-state объёме break-even (41 клиент)

| Step | ₽/мес | Комментарий |
|---|---:|---|
| ARPA | 220 000 | blended revenue на 1 клиента |
| Gross | 163 000 | ARPA minus COGS 57 000 ₽ |
| Contribution | 160 000 | Gross minus variable sales commission 3 000 ₽ |
| EBITDA | 0 | На 41 клиентах contribution почти полностью покрывает fixed costs |
| Net after tax, УСН 6% | -541 200 | налог с выручки 541 200 ₽ |
| Net after tax, IT-льгота 3% | -270 600 | при аккредитации Минцифры, налог с выручки 270 600 ₽ |
| Net after tax, ОСНО 20% | 0 | налог на прибыль близок к нулю, НДС 20% не включён в PnL как pass-through |

Вывод по waterfall: на уровне EBITDA break-even бизнес выходит примерно в ноль, но после налога с выручки для УСН 6% и IT-ставки 3% нужен запас по выручке сверх 41 клиента. Для ОСНО pressure переносится в НДС-администрирование, а не в налог на прибыль при нулевой прибыли.

## 4. Cash flow и startup capital to BEP

| Scenario | Peak cumulative cash burn, ₽ | startup_capital_to_bep_rub, ₽ | Комментарий |
|---|---:|---:|---|
| Base | 29 618 000 | 35 541 600 | с safety buffer 20% |
| Optimistic | 25 380 000 | 30 456 000 | с safety buffer 20% |
| Pessimistic | 35 355 000 | 42 426 000 | с safety buffer 20% |

## 5. Налоговая модель РФ

| Режим | Что попадает в модель | Эффект на cash/PnL | Когда реалистично |
|---|---|---|---|
| УСН 6% | 6% с выручки | давит на cash even при низкой прибыли, простое администрирование | ранний SaaS без сложной структуры расходов |
| IT-льгота 3% | 3% с выручки при аккредитации Минцифры | заметно лучше для SaaS, но на чистом BEP всё ещё нужен запас по выручке | если соблюдены условия по аккредитации и профильной выручке |
| ОСНО 20% | 20% налог на прибыль + НДС 20% | при низкой прибыли налог на прибыль мягче, но НДС и администрирование сложнее | enterprise B2B с крупными клиентами, где вычет НДС важен |

Дополнительно: страховые взносы **~30% к ФОТ** уже включены в FOT/fixed costs модели; НДС **20%** для ОСНО не включён в выручку/EBITDA как операционный доход, так как обычно проходит как pass-through при корректной структуре договоров и вычетов.

## 6. Break-even по сценариям

| Scenario | Break-even client count, клиентов | Break-even month by EBITDA | Tax-adjusted comment |
|---|---:|---|---|
| Base | 41 | M12 | для чистой прибыли после налога нужен запас выше EBITDA break-even |
| Optimistic | 41 | M12 | для чистой прибыли после налога нужен запас выше EBITDA break-even |
| Pessimistic | 41 | >M12 | для чистой прибыли после налога нужен запас выше EBITDA break-even |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

Метод: беру base-case из SECTION A на M12, где **41 клиент**, contribution profit **160 000 ₽/клиент/мес**, fixed costs **6 552 000 ₽/мес**, EBITDA **131 000 ₽/мес**. Для CAC x2 предполагаю падение lead→paid примерно в 2 раза, поэтому к M12 достигается только **~21 клиент** вместо 41. Для Churn x2 применяю повышенный monthly churn **3.6%** к cohort-ramp, что даёт **~36 активных клиентов** к M12. Price -30% бьёт по ARPU напрямую, при этом COGS и support почти не снижаются пропорционально. [T3][T5][T6][inference]

| Scenario | Key change | Active clients @M12 | Contribution / client, ₽/мес | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без изменений | 41 | 160 000 | 131 000 | на грани EBITDA break-even |
| Sens1 | CAC x2 | 21 | 160 000 | -3 192 000 | воронка масштабируется слишком медленно |
| Sens2 | Churn x2 | 36 | 160 000 | -792 000 | retention перестаёт держать enterprise economics |
| Sens3 | Price -30% | 41 | 94 000 | -2 698 000 | price compression почти полностью съедает маржу |

Вывод: у модели высокая чувствительность именно к **CAC inflation** и **price compression**. Churn тоже критичен, но менее разрушителен, чем потеря pricing power. Продолжать без подтверждённого premium positioning опасно. [T2][T3][T6][inference]

## 2. Monte Carlo Lite — confidence intervals

### 2.1. Inputs: triangular assumptions

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 900 000 | 1 034 000 | 1 600 000 | [T6] |
| Monthly churn, % | 1.2% | 1.8% | 3.6% | [T4][T6] |
| ARPU, ₽/мес | 180 000 | 220 000 | 280 000 | [T3][T6] |
| Conversion lead→paid, % | 0.25% | 0.40% | 0.65% | [T6] |
| Time-to-hire, мес | 1.0 | 1.6 | 3.0 | [T5][T6] |

Примечание: это не буквальная 1000-run симуляция, а **9-combo Monte Carlo lite** вокруг min/mode/max. p10 соответствует worst/mixed downside, p50 — modal case, p90 — upside с сильным pricing и лучшей конверсией. [inference]

### 2.2. Результаты Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -3 800 000 | 1 200 000 | 8 100 000 | 11 900 000 |
| CAC payback, мес | 8.9 | 4.7 | 3.2 | 5.7 |
| LTV/CAC | 2.3x | 8.8x | 19.2x | 16.9x |
| Cash runway, мес | 11 | 17 | 26 | 15 |

Как читать результат:
- **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1**: высокий риск не дойти до self-sustaining режима.  
- **p50 EBITDA > 500k ₽/мес**, значит median-case формально проходит EBITDA Gate, но запас небольшой относительно enterprise execution risk.  
- Разброс **p90/p10 по абсолютной величине** очень большой, то есть исход зависит от нескольких хрупких допущений одновременно.  
- **Range width по LTV/CAC = 16.9x > 8**, значит модель хрупкая: достаточно просадки pricing, роста churn или CAC inflation, и economics резко деградируют. [T4][T6][inference]

### 2.3. Практический вывод по Monte Carlo

У кейса не «плохая» median-экономика, а **широкий коридор исходов**. Это типичная картина для enterprise AI SaaS, где unit economics выглядят хорошо на бумаге, но очень зависят от того, удержит ли команда:  
1. premium чек,  
2. короткий цикл продажи,  
3. низкий churn после onboarding,  
4. контроль над service creep и LLM/data-cost stack. [T2][T6][inference]

## 3. Competitor deep-dive

### 3.1. Западные конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **AlphaSense** | Сильный бренд категории, 6 500+ customers и >$500M ARR по материалам кейса; глубокий workflow вокруг transcripts, filings, broker research, enterprise search. [T2] | Очень дорогой стек, слабая локализация под РФ, санкционные и data-residency риски для российских клиентов. | **~35-40%** в узком сегменте AI-first enterprise market intelligence. [inference] | Можно выиграть на локальных источниках, private Russian deployment и кастомизации под corpdev/strategy РФ. |
| **CB Insights** | Сильная private-market и market-map база, AI search, 1 600+ markets, 11M companies, 1B data points; доверие Fortune 500. [T11] | Больше заточен под venture/innovation/corporate strategy, чем под локальный research cockpit РФ; высокая цена и англоязычная база. | **~20-25%** в adjacent сегменте strategy / tech-market intelligence. [inference] | Наш выигрыш, более прикладной workflow под российские данные, тендеры, реестры, Telegram и внутренние документы. |
| **PitchBook** | Сильнейшая private capital / deal / valuation intelligence, новые AI-интеграции и generative workflows. [T13] | Фокус на private markets и finance use cases уже, чем у AlphaSense; хуже закрывает широкий market-monitoring контур. | **~15-20%** в invest/PE/corpdev intelligence. [inference] | Можно обыграть через более широкий мульти-источниковый market + competitor monitoring, а не только deal data. |
| **Quid** | Сильный social + market signal layer, 314% ROI и 6-month payback в Forrester-cases, большой акцент на patterns и trend detection. [T12] | Меньше доказанной глубины в finance/corpdev memo workflow, чем у AlphaSense/PitchBook; сложнее продавать как must-have strategy system. | **~8-12%** в signal intelligence / trend mapping. [inference] | Наш плюс, глубже vertical workflow под board memo, competitor scan и vendor scouting в enterprise-контуре. |

### 3.2. Российские и локально-релевантные конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Rusprofile** | Очень сильный контрагентский и реестровый слой: 12 млн юрлиц, 20 млн ИП, 700k+ пользователей в сутки, 200k+ организаций-клиентов. [T7] | Это не AI market intelligence cockpit, а прежде всего counterparty/risk due diligence и company data lookup. | **~30-35%** в российском сегменте company intelligence / due diligence self-serve. [inference] | Мы можем наложить AI-synthesis, monitoring и memo workflow поверх более широкого research-контура. |
| **Контур.Фокус** | Сильный бренд в проверке контрагентов, связи, арбитраж, закупки, официальный data backbone. [T10] | Тоже больше про due diligence и risk-check, чем про strategy/market research synthesis. | **~25-30%** в сегменте проверки контрагентов enterprise-SMB. [inference] | Наш выигрыш, больше пользы для strategy, corpdev, vendor scouting и конкурентного мониторинга, а не только compliance. |
| **Медиалогия** | Лидер по охвату источников в СМИ/соцсетях, 3.2 млрд аккаунтов и 109k СМИ, зрелый мониторинг и алерты. [T9] | Сильнее в PR/SMM/reputation monitoring, чем в deep company/market intelligence и internal-doc synthesis. | **~25-30%** в мониторинге СМИ и соцмедиа для enterprise. [inference] | Наш плюс, можем собрать не только инфополе, но и decision-ready memo по компаниям, рынкам и сделкам. |
| **Brand Analytics** | AI-аналитика упоминаний, Telegram/helpdesk integrations, российский реестр ПО, хранение данных в РФ, BrandGPT. [T8] | Ядро продукта, social listening и reputation analytics; слабее в corpdev / IR / M&A workflows. | **~15-20%** в social listening / customer intelligence. [inference] | Наше преимущество, product definition ближе к strategy research cockpit, а не к маркетинговой аналитике. |

Итог по конкурентам: в РФ нет прямого полного эквивалента AlphaSense, но есть **сильные substitute stacks**. Самый вероятный сценарий покупки, не «заменить один продукт», а **собрать bundle** из Rusprofile/Контур/Медиалогии/Brand Analytics плюс ручной аналитик. Значит продукт должен доказывать не наличие данных, а **снижение времени до memo и reduction of switching between tools**. [T7][T8][T9][T10][T14][inference]

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять senior ML/backend вовремя | med | Высокий, сдвиг roadmap и деградация качества | time-to-hire > 3 мес, offer acceptance < 50% | заранее pipeline кандидатов, remote hiring, дробление roadmap на более простой MVP |
| Operational | LLM API latency/cost spikes | high | Высокий, рост COGS и ухудшение UX | cost/query +30%+, p95 latency > 10 сек | multi-model routing, local fallback, кэширование, лимиты на heavy workflows |
| Market | Спрос есть только на pilot, но не на annual expansion | med | Высокий, CAC не окупается | pilot→annual conversion < 30% | продавать pilot только с заранее согласованным expansion plan и KPI |
| Market | Price compression из-за general-purpose AI copilots | high | Высокий, маржа ломается | скидки >20% в 3+ подряд сделках | жёсткая вертикализация, private deployment, workflow templates, ROI-cases |
| Regulatory | 152-ФЗ и data residency блокируют загрузку внутренних документов | med | Высокий, часть ICP отваливается | юристы клиента требуют локальный контур и DPA addendum | on-prem / isolated VPC, хранение в РФ, минимизация PII |
| Regulatory | Санкции/SaaS restrictions обрывают доступ к зарубежным datasets/API | high | Высокий, часть value proposition исчезает | недоступность поставщика, отказ bill/payment | российские и open-source substitutes, vendor diversification, офлайн ingestion |
| Financial | Runway оказывается короче плана из-за более медленной воронки | high | Высокий, down-round или остановка найма | burn > 3.5 млн ₽/мес три месяца подряд | stop hiring gates, недельный cash review, only-ROI spend policy |
| Financial | Ослабление рубля повышает долларовые infra/API издержки | high | Средне-высокий | USD/RUB > +20% к базовому курсу | валютный буфер, рублёвые договоры где возможно, локальные модели |
| Black swan | Резкое усиление санкций по AI/облакам | med | Очень высокий | блокировки новых аккаунтов, отказ провайдеров | резервные провайдеры, self-hosted stack, запас предоплаченных мощностей |
| Black swan | Геополитический шок/война режет enterprise budgets и удлиняет закупки | med | Очень высокий | заморозка пилотов, CFO approval cycle > 2x | фокус на anti-crisis use cases, shorter pilots, сегменты с устойчивыми CAPEX/OPEX |

## 5. Kill conditions через 6 месяцев

1. **Median-case не подтверждается:** p10 EBITDA остаётся < 0 и фактический pipeline не показывает выход к **p50 EBITDA > 500k ₽/мес** на горизонте 24 месяцев.  
2. **Unit economics ломаются:** фактический **LTV/CAC < 3x** или **CAC payback > 12 мес** на первых 5-7 платящих клиентах.  
3. **Go-to-market не сходится:** за 6 месяцев нет минимум **3 платящих enterprise клиентов** или pilot→paid conversion ниже **25%**.  

## 6. Финальный вывод SECTION B

Кейс остаётся **интересным, но хрупким**. Сильная сторона, высокий ceiling при удачном positioning. Слабая сторона, очень широкая дисперсия исходов: при CAC inflation, churn spike или price compression EBITDA быстро уходит глубоко в минус. Инвестировать время дальше имеет смысл только если команда в первые 6 месяцев докажет, что может продавать **не generic AI search**, а локализованный **enterprise research cockpit** с defensible pricing. [T2][T6][T7][T8][T9][T10][T11][T12][T13][inference]

## Источники SECTION B
- [T7] Rusprofile official pages: https://www.rusprofile.ru/ ; https://www.rusprofile.ru/team ; https://www.rusprofile.ru/about
- [T8] Brand Analytics official site: https://brandanalytics.ru/
- [T9] Медиалогия official site: https://www.mlg.ru/ ; https://www.mlg.ru/products/smm/
- [T10] Контур.Фокус official site: https://kontur-fokus.ru/
- [T11] CB Insights official pricing/product page: https://www.cbinsights.com/what-we-offer/pricing/
- [T12] Quid official site: https://www.quid.com/
- [T13] PitchBook official press pages: https://pitchbook.com/media/press-releases/pitchbook-launches-new-generative-ai-experiences-with-the-introduction-of-pitchbook-navigator-and-upcoming-integration-with-openai ; https://pitchbook.com/media/press-releases/pitchbook-expands-access-to-private-market-intelligence-through-new-llm-partnerships-with-finster-model-ml-and-farsight-ai
- [T14] Хабр, comparison of Russian social monitoring systems: https://habr.com/ru/companies/cian/articles/695480/

<!-- P6B-DONE -->

## Файл: 06-verdict.md

[GEO-EXPAND] AlphaSense AI Market Intelligence v2 — NEAR-PASS: 69/100 | EBITDA base=1448К₽/мес через 14 мес | LTV/CAC=8,8x | Ключевое преимущество: enterprise research cockpit с высоким ACV и глубоким workflow | Главный риск: weak moat и дорогой sales-led GTM.

# 06-verdict

sector: GEO-EXPAND
status: NEAR-PASS
score: 69/100
case: alphasense-ai-market-intelligence-v2
date: 2026-04-26

## Итог инвесткомитета
**Вердикт: NEAR-PASS.**

Кейс проходит по unit economics и по потенциалу `company_ebitda_potential_rub_month >= 500 000 ₽/мес` при **50 клиентах** и горизонте **до 24 месяцев**, но пока не получает approve из-за слабого moat, высокой чувствительности к premium pricing и не до конца доказанного repeatable GTM в РФ.

## Оценка
Source tier balance: T1=2, T2=7, T3=1, weighted=2.10. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 8.8x», «CAC Payback = 4.7 мес», «Gross Margin = 74.1%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | «При 50 клиентах проект выходит на ~1.6 млн ₽ EBITDA/мес» и gate «PASS». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | «анализ рынка = MEDIUM», «стратегический анализ = MEDIUM», но exact термины `market intelligence` и `M&A аналитика` низкие. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | «без локальных источников и без вертикального сценария продукт схлопывается в “ещё один AI search”». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | «p10 EBITDA < 0», есть риски 152-ФЗ, санкций, data-cost creep и service creep. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | «sales-led, 2-5 месяцев, обычно pilot → annual» и blended CAC 1.034 млн ₽ остаётся высоким, но payback рабочий. |

**Sum raw = 103 / 150. Normalized score = round((103 * 100) / 150) = 69/100.**

## Investment committee one-liner
Enterprise research cockpit для strategy, corpdev и IR в РФ выглядит экономически рабочим, но пока не инвестиционного качества из-за хрупкого moat и дорогого enterprise GTM.

## Delta vs previous
По сравнению с предыдущим verdict для `alphasense-ai-market-intelligence` score улучшился с **66/100** до **69/100** за счёт более чёткой RU-валидации JTBD, stronger unit economics framing и формализованного EBITDA-gate. Но финальный статус не меняется: moat и repeatable GTM всё ещё слабее approve-порога.

## 7-factor Moat Framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 2 | После внедрения появляются watchlists, внутренние документы, поисковые рецепты и обученность команды. |
| 3. Scale economies | 1 | Infra и search stack дешевеют умеренно, но onboarding и enterprise support остаются high-touch. |
| 4. Proprietary data / model advantage | 1 | Есть сильный workflow, но в РФ не доказан уникальный локальный dataset advantage. |
| 5. Regulatory moat | 1 | Требования 152-ФЗ и private deployment важны, но не создают эксклюзивный барьер входа. |
| 6. Brand / distribution | 1 | Глобальный бренд AlphaSense силён, но локальная дистрибуция в РФ не подтверждена. |
| 7. Embedded workflow | 3 | При успешном внедрении продукт глубоко встраивается в strategy/corpdev/IR memo workflow. |

**Moat raw = 9/21. Moat score = round((9 * 25) / 21) = 11/25.**

> **Weak moat:** score < 10 raw по 7-factor. Обязательно выносится в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 9 056 667 ₽ |
| CAC | 1 034 000 ₽ |
| LTV/CAC | 8,8x |
| CAC Payback | 4,7 мес |
| GM% | 74,1% |
| contribution_margin_rub_month | 160 000 ₽ на клиента |
| fixed_costs_rub_month | 6 552 000 ₽ |
| company_ebitda_rub_month (base M12) | 131 000 ₽/мес |
| company_ebitda_potential_rub_month (50 клиентов) | 1 448 000 ₽/мес |
| clients_to_500k_ebitda | 45 |
| clients_to_1m_ebitda | 48 |
| months_to_500k_ebitda | 13 |
| months_to_1m_ebitda | 14 |
| Break-even | 41 клиент / M12 |
| startup_capital_to_bep_rub | 35 541 600 ₽ |
| Startup capital available | нет данных |

## Full business process from 04-economics

| Шаг | Процесс | ROLE | TOOL | TIME | COST |
|---|---|---|---|---|---:|
| 1 | Поиск ICP-аккаунтов и обогащение списка | SDR | CRM, LinkedIn/SalesNav-аналоги, Контур.Фокус, TGStat | 35 мин | 1 400 ₽ |
| 2 | Первый outbound / warm intro / партнёрский интро | SDR / CEO | email, Telegram, phone, партнёрская сеть | 20 мин | 1 100 ₽ |
| 3 | Qualification call | SDR | CRM, calendar, call notes | 30 мин | 1 600 ₽ |
| 4 | Discovery c buyer | AE + CEO | Zoom/Meet, AI note taker, шаблон discovery | 60 мин | 5 700 ₽ |
| 5 | Сбор pain points и источников клиента | AE + solutions lead | Notion, CRM, intake template | 90 мин | 7 800 ₽ |
| 6 | Подготовка demo-песочницы и sample memo | Product + ML + backend | internal admin, LLM/RAG stack, dataset connectors | 6 ч | 18 500 ₽ |
| 7 | Demo / workshop | AE + CEO + product | Zoom, demo workspace | 75 мин | 8 400 ₽ |
| 8 | Security / IT review | CTO + AE | security docs, DPA, architecture pack | 4 ч | 13 800 ₽ |
| 9 | Коммерческое предложение и ROI-калькулятор | AE | CRM, CPQ, шаблон ROI | 2 ч | 5 600 ₽ |
| 10 | Negotiation + legal | CEO + AE | contract workflow, e-sign | 5 ч | 19 000 ₽ |
| 11 | Onboarding и настройка workspace | CSM + solutions engineer | product admin, source connectors, training deck | 10 ч | 24 700 ₽ |
| 12 | Запуск usage и первый monthly check-in | CSM | BI dashboard, usage alerts, playbook | 2 ч | 4 600 ₽ |
| 13 | Выставление счёта и оплата | finance ops | ЭДО, банк-клиент, 1С | 40 мин | 1 300 ₽ |

**Итого cost-to-first-payment: ~113 500 ₽ на 1 closed-won до учёта неполной конверсии воронки.**

## Team table

| Роль | Fully-loaded FOT ₽/мес | Комментарий |
|---|---:|---|
| CEO / founder | 910 000 | key accounts, partnerships, fundraising |
| CTO / Tech Lead | 715 000 | архитектура, security, enterprise deployment |
| Senior Backend #1 | 546 000 | ingestion / API / integrations |
| Senior Backend #2 | 546 000 | search / platform / data connectors |
| ML Engineer | 650 000 | ranking, summarization quality, RAG |
| DevOps | 455 000 | infra, observability, security ops |
| Frontend | 390 000 | analyst workspace, dashboards |
| Product Manager | 390 000 | workflow templates, roadmap, adoption |
| Marketing Manager | 286 000 | content, webinars, inbound |
| SDR | 234 000 | outbound prospecting |
| AE | 468 000 | discovery, demo, negotiation |
| Customer Success | 312 000 | onboarding, training, expansion |

**Steady-state full team FOT: 5 902 000 ₽/мес.**

## Почему не APPROVED
Для APPROVED нужен не только score >= 70, но и запас прочности по moat и repeatable GTM. Здесь EBITDA-gate формально проходит, однако:
1. exact-demand в РФ остаётся adjacent, а не core category demand;
2. moat слабый, raw 9/21;
3. blended CAC высокий для early-stage локального go-to-market;
4. модель очень чувствительна к price compression и service creep.

## Top-3 risks

| Риск | Probability | Impact | Почему важно |
|---|---|---|---|
| Weak moat / commoditization | high | высокий | Без локального data advantage и deep workflow differentiation продукт схлопывается в generic AI search. |
| Premium GTM не повторяется | high | высокий | При CAC inflation или скидках 20%+ economics быстро теряют запас прочности. |
| Data residency / sanctions / vendor dependency | med-high | высокий | 152-ФЗ, private deployment и зависимость от зарубежных моделей/источников могут ломать rollout. |

## LTV Upside Calculator
Чтобы перевести кейс из **69/100** в **70+** и сделать его approve-ready, нужно улучшить минимум 2 из 4 рычагов:

| Рычаг | Текущее | Цель | Эффект |
|---|---:|---:|---|
| ARPA / blended MRR | 220 000 ₽ | 260 000-280 000 ₽ | усиливает contribution и сокращает путь к 500К EBITDA |
| CAC | 1 034 000 ₽ | <850 000 ₽ | повышает margin of safety по GTM |
| Moat raw | 9/21 | 11+/21 | переводит кейс из weak moat в defendable workflow layer |
| fixed_costs_rub_month | 6 552 000 ₽ | <6 000 000 ₽ | ускоряет выход к 500К и 1М EBITDA |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Крупная strategy/corpdev машина, постоянный поток market scans и vendor intelligence. | email decision-maker в strategy/innovation + партнёрский интро | 350 000 ₽/мес |
| 2 | ВТБ | Корпоративный банк с heavy research, отраслевыми обзорами и due diligence workflow. | direct enterprise outreach + отраслевые конференции | 320 000 ₽/мес |
| 3 | АФК Система | Холдинг с M&A, strategy и portfolio monitoring по множеству вертикалей. | email corpdev lead / тёплый интро через экосистему | 300 000 ₽/мес |
| 4 | Северсталь | Регулярный конкурентный мониторинг, закупочный scouting и strategy briefs по рынкам. | direct email + кейс через Habr/vc.ru thought leadership | 250 000 ₽/мес |
| 5 | Норникель | Высокая цена стратегической ошибки, много внешних рынков и supplier intelligence. | account-based outreach + конференция CNews/ComNews | 260 000 ₽/мес |
| 6 | X5 Group | Continuous market intelligence для форматов, категорий и vendor landscape. | partnership с digital/advisory integrator + email | 220 000 ₽/мес |
| 7 | Магнит | Нужен регулярный market scan по retail-tech, поставщикам и competitive moves. | decision-maker email + отраслевой ритейл-форум | 220 000 ₽/мес |
| 8 | МТС | Strategy, IR и new ventures требуют multi-source research и memo-ready synthesis. | ABM outreach + конференция по данным/AI | 280 000 ₽/мес |
| 9 | Яндекс | Большой контур новых рынков, инвестиций и competitor tracking. | founder-led intro + targeted content on vc.ru/Habr | 300 000 ₽/мес |
| 10 | Ростелеком | Enterprise strategy, гос/корпоративные тендеры и vendor intelligence в одном контуре. | партнёрство с SI / direct enterprise email | 240 000 ₽/мес |

## Market + finance synthesis
- Preferred SAM: **283,5 млн ₽**.
- SOM Y1: **12,1 млн ₽/год**.
- Base break-even: **41 клиент**, **M12**.
- company_ebitda_potential_rub_month @50 клиентов: **1 448 000 ₽/мес**.
- p50 EBITDA @M24: **1 200 000 ₽/мес**.
- p10 EBITDA @M24: **-3 800 000 ₽/мес**.
- startup_capital_to_bep_rub: **35 541 600 ₽**.

## Что доказать за следующие 6 месяцев
1. 2-3 платных enterprise-клиента с ACV не ниже 2,6-3,0 млн ₽/год.
2. Repeatable pilot → annual conversion выше 30%.
3. Локальный data layer, который нельзя легко собрать из Rusprofile + Контур + Медиалогии вручную.
4. Blended CAC ниже 850 тыс. ₽ и удержание churn вблизи 1,5-1,8%/мес.

## Финальное решение
**NEAR-PASS / в текущем виде уходит в rejected-пул.**

Причина не в математике клиента, а в недостатке margin of safety на уровне компании: economics хорошие, но moat, evidence quality и repeatable GTM ещё не дотягивают до investment-grade approve.
