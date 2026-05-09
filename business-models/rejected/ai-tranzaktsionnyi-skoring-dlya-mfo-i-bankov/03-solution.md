---
stage: solution
case: ai-tranzaktsionnyi-skoring-dlya-mfo-i-bankov
date: 2026-05-09
analyst: branch-models-lead
sector: FINTECH
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
AI-транзакционный скоринг для МФО и банков: внешний scoring/API слой, который использует транзакционные данные, БКИ и цифровой след для автоматизации андеррайтинга и улучшения качества решений по онлайн-кредитованию.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт закрывает не абстрактный «AI для финтеха», а core-risk workflow, где скорость и качество решения напрямую влияют на approve-rate, default-rate и cost-to-serve.
2. Лучший wedge в РФ выглядит не как дешёвый per-report инструмент, а как decisioning layer поверх существующего стека банка или МФО: scoring + rules + explainability + integration + monitoring.
3. Наиболее реалистичный вход, digital-first МФО, BNPL/embedded lenders и банки со слабым покрытием thin-file / new-to-credit сегментов.
4. Главный риск, решение легко превращается в тяжёлый кастомный risk-consulting проект под каждого клиента и теряет repeatable software economics.

## 1. Какую проблему реально решает продукт

Покупают не просто «ещё одну ML-модель». Покупают снижение четырёх дорогих потерь:
- слишком медленного решения по онлайн-заявкам;
- высокой доли ручного андеррайтинга и ручных эскалаций;
- плохой оценки thin-file клиентов, где классической кредитной истории недостаточно;
- лишних просадок по default-rate, fraud-loss и cost of acquisition одобренного заёмщика.

Если продукт помогает безопасно одобрять больше заявок, быстрее принимать решение и сокращать долю ручной проверки, он становится painkiller для lending P&L, а не nice-to-have аналитической надстройкой.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- online-first МФО с большим потоком заявок;
- банки с цифровым потребкредитованием и POS/карточными сценариями;
- BNPL, instalment и embedded finance игроки;
- кредитные платформы и интеграторы, готовые white-label'ить risk-decision слой.

### Buyer map
- директор по рискам / head of risk;
- руководитель кредитного конвейера или underwriting;
- digital lending lead;
- CTO / CIO, если проект заходит через интеграцию в decision engine;
- COO или P&L-owner кредитного продукта, если кейс продаётся через ROI.

### Фильтр на ICP
Клиент выглядит целевым, если одновременно есть:
1. достаточный поток онлайн-заявок;
2. заметная доля ручного underwriting-review;
3. чувствительность к approve-rate и loss-rate;
4. доступ к транзакционным данным или готовность подключать альтернативные источники;
5. готовность внедрять отдельный scoring layer, а не только покупать сырые данные БКИ.

### Нецелевой сегмент
- маленькие кредитные брокеры и агентские схемы без собственного risk-контура;
- офлайн-кредиторы с низким объёмом заявок;
- организации, где нет owner'а на уровне риска и кредитного P&L;
- клиенты, ожидающие разовую модель «настроить один раз и забыть» без recurring monitoring.

## 3. Продуктовый wedge

### Core wedge
**Transaction-aware underwriting decision layer**:
- скоринг на базе транзакций, БКИ и цифрового следа;
- API/decision engine для pre-approval и full underwriting;
- explainability и reason-codes для risk-команды;
- мониторинг drift, quality и cut-off performance;
- очередь исключений для ручного review и policy overrides.

### Почему это сильнее, чем просто score API
1. Ценность возникает не в score как числе, а в месте внутри decision workflow.
2. Buyer покупает uplift в approve-rate и снижение bad-rate, а не только доступ к новой модели.
3. Продукт можно продавать как recurring risk layer с долгим stickiness после интеграции.
4. Поверх scoring естественно наращиваются antifraud, affordability checks, champion-challenger и portfolio monitoring.
5. Для regulated buyer важны explainability, audit trail и контроль версий, это повышает защиту от commodity-конкуренции.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Что, скорее всего, не взлетит
- продажа как generic AI-score без связи с текущим decision flow;
- low-ticket per-report инструмент для широкой массы кредиторов;
- чёрный ящик без reason-codes, QA и governance;
- self-serve SaaS без поддержки интеграции и валидации модели.

### Что выглядит реалистично
- заход через 1 пилотный use case: thin-file заёмщики, repeat borrowers, instant approval или antifraud-adjacent pre-check;
- KPI пилота: approve-rate uplift, bad-rate / FPD, share of manual review, time-to-decision;
- внедрение как внешний слой рядом с текущими БКИ, antifraud и rules-engine, а не замена всего risk stack;
- контракт как setup + recurring platform fee + usage / monitoring layer;
- land-and-expand: сначала МФО и digital lenders, затем банки и embedded-finance сценарии.

## 5. Почему клиент купит это, а не текущий стек

У клиента уже есть substitutes:
- БКИ и стандартные кредитные отчёты;
- внутренние scorecards и rules;
- antifraud-платформы;
- manual underwriting;
- кастомная DS-разработка in-house.

Решение выигрывает только если одновременно:
1. даёт measurable uplift против текущего cut-off;
2. встраивается быстрее и дешевле, чем building in-house;
3. не ломает compliance и explainability-требования;
4. позволяет risk-команде контролировать модель, а не терять управление.

Если этого нет, buyer проще расширить rules, докупить ещё один источник данных или нанять внутреннюю data science команду.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего underwriting flow и baseline-метрик;
2. выбор одного сегмента заявок для challenger-пилота;
3. подключение исторических данных и сборка score / policy layer;
4. offline backtesting и calibration;
5. ограниченный online pilot с manual guardrails;
6. rollout на более широкий поток и добавление monitoring / retraining cadence.

### Каналы GTM
- founder-led enterprise sales по digital lenders и МФО;
- партнёрства с кредитными платформами, integrators, decision-engine vendors;
- продажа через конкретный ROI-кейс для risk-owner;
- OEM / white-label motion для поставщиков fintech-инфраструктуры.

## 7. Конкурентная позиция

### Против БКИ и сырых data providers
Преимущество только если продукт превращает данные в готовое решение, а не просто добавляет ещё один источник сигнала.

### Против in-house risk stack
Преимущество, более быстрый pilot, готовые интеграции, champion-challenger логика и внешний domain expertise.

### Против локальных scoring vendors
Шанс есть, если новый игрок лучше закрывает thin-file / transaction-based decisioning и даёт более современный monitoring + explainability слой.

## 8. Основные риски solution-fit

1. **Customization risk**: каждый клиент требует отдельную модель, интеграцию и policy-логику.
2. **Trust risk**: risk-owner не отдаёт критичный decision layer внешнему поставщику без длительной валидации.
3. **Data access risk**: не у всех клиентов достаточно качественных транзакционных данных для сильного uplift.
4. **Compliance risk**: explainability, аудит и модельный риск могут сильно замедлить продажи.
5. **Incumbent lock-in**: у крупных банков уже есть зрелые risk stacks и внутренние DS-команды.
6. **Margin risk**: если каждый pilot требует много ручной аналитики, продукт скатится в consulting-heavy motion.

## 9. Что обязательно проверить на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит pilot и data onboarding одного клиента;
- какой процент delivery можно стандартизировать;
- сколько клиентов нужно для EBITDA > 500 000 ₽/мес в SaaS/API и white-label моделях;
- какой CAC и payback у direct enterprise GTM в regulated fintech;
- где лучше первая точка входа, МФО, embedded finance или mid-tier банк.

## Итог для пайплайна

**P4 пройден условно.**

Кейс выглядит живым как FINTECH infrastructure wedge, если продавать его не как «модель скоринга», а как управляемый decisioning layer для digital lending. Продолжать дальше имеет смысл, потому что pain и buyer budget реальны, но economics нужно защищать от двух срывов: чрезмерной кастомизации и слишком длинного enterprise sale cycle.