# Accenture + Microsoft Forward Deployed Engineering v2
Статус: REJECTED
Score: 63/100
Sector: AI-SERVICES
Date: 2026-04-22

---

## 00-brief.md

# Brief

- Кейс: Accenture + Microsoft Forward Deployed Engineering
- Slug: accenture-microsoft-forward-deployed-engineering-v2
- Sector: AI-SERVICES
- Режим: resurrect / полный пайплайн обязателен
- Исходный raw-файл: 2026-04-19-resurrect-accenture-microsoft-forward-deployed-engineering.md
- Источник предыдущего решения: pipeline/triage/triage-2026-04-11-accenture-microsoft-forward-deployed-engineering.md
- Исторически связанный кейс: pipeline/cases/ai-forward-deployed-enterprise-implementation-operator/
- Следующий этап: P3-demand-validation

## Почему создан новый кейс
Файл пришёл с префиксом `resurrect-`, поэтому создана новая версия кейса без duplicate-классификации. По standing orders такой сигнал обязан пройти новый полный цикл оценки как standalone candidate.


---

## 01-intake.md

---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-accenture-microsoft-forward-deployed-engineering.md
created: 2026-04-20T05:42:00+03:00
original_triage: pipeline/triage/triage-2026-04-11-accenture-microsoft-forward-deployed-engineering.md
---

# Intake

## Название
Accenture + Microsoft Forward Deployed Engineering

## Режим обработки
Принудительный resurrect по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Краткий контекст
Enterprise-сервисный слой вокруг проектирования, внедрения и operationalization AI в крупных организациях поверх big-tech ecosystems.

## Предыдущий контекст
- Оригинальный triage: `pipeline/triage/triage-2026-04-11-accenture-microsoft-forward-deployed-engineering.md`
- Исторически связанный кейс: `pipeline/cases/ai-forward-deployed-enterprise-implementation-operator/`
- Оригинальный verdict: не найден в текущем workspace.

## Полный контекст из raw

# RESURRECT SIGNAL — accenture-microsoft-forward-deployed-engineering

## Meta
- source: triage/triage-2026-04-11-accenture-microsoft-forward-deployed-engineering.md
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
2026-04-11

## Inputs
- pipeline/raw/radar-2026-04-11-1210-msk.md

## Classification
signal, new case candidate

## Decision
Создать новый case-кандидат: `ai-forward-deployed-enterprise-implementation-operator`.

## Why
Сигнал описывает не просто общий enterprise AI adoption, а оформление отдельного delivery слоя вокруг внедрения и operationalization AI в крупных компаниях.

Что делает его отдельным case-кандидатом:
- Accenture и Microsoft формализуют forward deployed engineering practice, а не просто consulting partnership.
- Упор идёт на design, build и operationalize AI across the enterprise, то есть на repeatable implementation-and-operations motion.
- Масштаб в "thousands of AI-skilled engineers" намекает на большой и уже институционализирующийся рынок AI-native delivery operators внутри enterprise stack.
- Это шире и потенциально самостоятельнее, чем уже открытый case про Salesforce-specific implementation operator.

## Triage note
Проверять как модель enterprise AI implementation operator / forward deployed engineering operator: внедрение, интеграция, workflow redesign, governance и rollout AI в крупных организациях поверх big-tech ecosystems. В следующем цикле важно отделить настоящий новый сервисный слой от обычного rebranding классического SI/consulting.
```


---

## 02-demand.md

# Demand validation — Accenture + Microsoft Forward Deployed Engineering

## TL;DR
- Спрос в РФ на enterprise AI implementation не массовый, но платёжеспособный: локальный API `multi-demand` дал `LOW / score 3`, при этом в HH найдено 20 вакансий по запросу «внедрение ИИ для enterprise», а в РФ уже есть 350+ внедрённых ИИ-решений в 55 регионах, что подтверждает не хайп, а реальный rollout [T1][T2].
- Market Pulse 2026-04-20: наблюдается рост интереса. В текущем веб-срезе видны свежие публикации и внедренческие сигналы по enterprise AI, включая анонсы программ внедрения ИИ-агентов и корпоративного GenAI.
- WTP подтверждён на глобальном и локальном уровнях: у Accenture GenAI bookings достигли $3 млрд за FY2024 и ещё $1.4 млрд в Q2 FY2025, у Microsoft AI business run-rate превысил $13 млрд, а enterprise-проекты на рынке интеграторов обычно живут в диапазоне от $25k до $1m+ [T1][T2].
- Profit Gate проходим только в сценарии enterprise program / AI CoE retainer; micro-pilot и staff-aug по 1-2 инженера сами по себе EBITDA 500k+/мес обычно не дают [T2].
- Итог: **DEMAND = MEDIUM**, не early reject, кейс можно вести дальше.

## Demand signals
### 1) Прямой demand check
- `http://172.18.0.1:9001/multi-demand?keyword=внедрение ИИ для enterprise` вернул: `composite_demand=LOW`, `demand_score=3`, `habr_articles=2`, `hh_vacancies=20`, `yandex_suggest=2` [T2, internal demand endpoint].
- Интерпретация: массового поискового спроса нет, но есть кадровый и внедренческий спрос в enterprise-сегменте. Для B2B services это нормальный паттерн, потому что сделки идут через sales-led каналы, тендеры и executive relationships, а не через consumer search [T2].

### 2) Внедрение ИИ в РФ уже материализуется
- Правительство РФ сообщало, что объём рынка ИИ в России достиг почти **650 млрд ₽** при росте около **18%** [T1: government.ru/news/49604/].
- В феврале 2026 Правительство РФ сообщило о **55 регионах** и примерно **350 ИИ-решениях / 430+ сценариях** на портале «Цифровой регион» [T1: government.ru/news/57915/].
- Вывод: рынок внедрения не нулевой, а уже перешёл из фазы «интереса» в фазу «пилоты + rollout» [T1].

### 3) Глобальный budget signal
- Accenture зафиксировала **$3 млрд новых GenAI bookings за FY2024** и **$1.4 млрд новых GenAI bookings в Q2 FY2025** [T1: Accenture earnings / Accenture Europe AI POV].
- Microsoft в январе 2025 сообщила, что её AI business превысил **$13 млрд annual revenue run rate**, +175% YoY [T1: Microsoft earnings].
- Это сильное подтверждение, что крупные enterprise-клиенты готовы покупать не только модели, но и дорогое внедрение, integration work и change management [T1].

## Competitor pricing (реальные аналоги)
| Конкурент | Что продаёт | Ценообразование | Вывод |
|---|---|---:|---|
| HatchWorks AI | AI/data transformation partner | min project **$25k+**, hourly **$50–99/hr**, most common project **$200k–999k** [T2] | Нижняя граница enterprise-delivery уже не «несколько сотен тысяч ₽», а миллионы рублей |
| ITRex Group | GenAI strategy → enterprise deployment | min project **$25k+**, hourly **$50–99/hr**, client budgets **$10k–500k+** [T2] | Средний проект легко укладывается в 0.8–38+ млн ₽ |
| Xebia | Global IT consultancy / transformation | min project **$10k+**, hourly **$50–99/hr**, client investments **$360k–2m** [T2] | Верхний сегмент даёт 27–152 млн ₽ за engagement |
| Andersen | IT strategy / cloud / data / AI delivery | min project **$50k+**, hourly **$50–99/hr**, budgets **$5k–1m+** [T2] | Для крупного enterprise win порог цены высокий |

Пересчёт в рубли сделан по курсу ЦБ РФ **76.0535 ₽/$** на 18.04.2026 [T1: cbr.ru].

## Telegram bots / services in RU
- В РФ есть смежный слой предложения в Telegram-first формате, но это в основном SMB automation, а не full-scale forward deployed engineering.
- Walkow предлагает AI-боты для Telegram **от 9 900 ₽**, запуск за 3–7 дней [T2: walkow.ru].
- Sozdaibota / NeuroBack декларирует: базовый ИИ-бот **от 30 000 ₽**, GPT-бот **от 50 000 ₽**, комплексный бот **от 100 000 ₽**, enterprise-решение **от 150 000 ₽** [T2: sozdaibota.ru].
- Botseller продвигает «AI-сотрудника» для Telegram/WhatsApp/CRM, 100+ внедрений, но без открытого фиксированного прайса [T2: botseller.ai].
- Вывод: рынок Telegram automation в РФ есть и monetized, но он ценово и по сложности находится на порядок ниже, чем enterprise FDE. Это скорее low-end substitute / beachhead, а не прямой peer [T2].

## WTP (proof of willingness to pay)
1. **Глобальный WTP**: $3 млрд GenAI bookings у Accenture за FY2024 и $1.4 млрд за один квартал FY2025 означают, что enterprise уже подписывает многомиллионные сервисные контракты [T1].
2. **Платёжеспособность market comps**: у HatchWorks / ITRex / Xebia / Andersen типовые бюджеты лежат от десятков тысяч до миллионов долларов, что подтверждает willingness to pay за delivery-heavy AI programs [T2].
3. **Российский WTP**: 650 млрд ₽ рынка ИИ в РФ и рост количества внедрённых решений в регионах означают наличие бюджетов на внедрение, а не только на эксперименты [T1].
4. **Telegram low-end WTP**: даже SMB покупает Telegram AI bots за 9.9k–150k+ ₽, что подтверждает существование локальной готовности платить за AI automation, пусть и в существенно более низком чеке [T2].

## Market sizing
### Методика
- **Top-down:** взял мировой рынок Generative AI services **$27.76 млрд** из общего GenAI spend **$643.86 млрд** в 2025, то есть services share около **4.31%** [T1: Gartner via search snippet]. Эту долю применил к рынку ИИ РФ **650 млрд ₽** [T1].
- **Bottom-up:** взял **44.9 тыс.** прибыльных организаций в РФ за январь-ноябрь 2025 как proxy платёжеспособной базы [T1: Росстат summary via search], далее сузил до top 10% компаний, где есть шанс на enterprise AI budget, затем применил долю компаний с подтверждённой болью и средний контракт.

### Допущения
- Курс: **76.0535 ₽/$** [T1].
- Addressable service share в РФ: **4.31%** от всего AI spend [T1 + inference].
- Segment fit для SAM: **60%** TAM РФ, т.к. кейс ориентирован на крупный B2B/regulated/multi-system enterprise, а не на весь AI market [inference, supported by T1/T2].
- Bottom-up buyers: **44.9k × 10% = 4 490 компаний** [T1 + inference].
- `% with need`: **15%**, т.к. спрос узкий, но не нулевой, что согласуется с 20 HH vacancies, 350+ внедрениями и LOW-search demand [T1/T2].
- Avg first-year ACV: **30 млн ₽**. Это между low-end global service engagements и upper-mid enterprise transformation budgets; ближе к крупным пилотам / первой фазе AI CoE, а не к full-stack multi-country rollout [T2].

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$27.76B / 2.11 трлн ₽** [T1] | — | — | top-down |
| TAM (РФ) | **28.0 млрд ₽** = 650 млрд ₽ × 4.31% [T1] | **33.7 млрд ₽** = 4 490 × 25% × 30 млн ₽ [T1/T2] | diff ~20%, допустимо; bottom-up шире, потому что берёт часть latent demand | **lower = 28.0 млрд ₽** |
| SAM (РФ) | **16.8 млрд ₽** = TAM × 60% [T1/T2] | **20.2 млрд ₽** = 4 490 × 15% × 30 млн ₽ [T1/T2] | diff ~20%, в пределах нормы | **lower = 16.8 млрд ₽** |
| SOM Y1 | **336 млн ₽** = 2% SAM [calc] | **404 млн ₽** = 2% SAM_bottom_up [calc] | diff ~20% | **используем 336 млн ₽** |
| SOM Y3 | **1.35 млрд ₽** = 8% SAM [calc] | **1.62 млрд ₽** = 8% SAM_bottom_up [calc] | diff ~20% | **используем 1.35 млрд ₽** |

### Sanity checks
- Расхождение top-down и bottom-up < 3x, пересборка сегмента не нужна.
- SOM Y1 = 2% SAM, это реалистично и <10% SAM.
- При ACV 30 млн ₽ для выхода на SOM Y1 нужно ~11 крупных контрактов в год, то есть примерно 1 close в месяц. Для boutique FDE-практики это напряжённо, но достижимо только при сильном канале продаж и партнёрстве уровня Microsoft/Accenture.

## 10 реальных buyers для bottom-up
1. Сбер
2. ВТБ
3. Альфа-Банк
4. Т-Банк
5. МТС
6. X5 Group
7. Магнит
8. Северсталь
9. Газпром нефть
10. Росатом

Комментарий: это не SMB-лиды, а accounts с данными, процессной сложностью и бюджетом под enterprise AI integration. Список годится как база для будущего P7 GTM-10-targets [T2, inference from public AI adoption patterns].

## Profit Gate (EBITDA >= 500k ₽/мес)
### Сценарий 1: micro-pilot
- Чек: **3–6 млн ₽**
- Валовая/EBITDA-маржа для сервисной команды после delivery-cost: **10–20%**
- EBITDA в месяц: примерно **25k–100k ₽/мес**
- **Gate: FAIL**

### Сценарий 2: staff augmentation / embedded pod
- Чек: **10–18 млн ₽/год**
- EBITDA margin: **20–30%**
- EBITDA: **2.0–5.4 млн ₽/год** = **167k–450k ₽/мес**
- **Gate: чаще FAIL**, если продаётся только body-leasing

### Сценарий 3: enterprise implementation program
- Чек: **24–40 млн ₽/год**
- EBITDA margin: **25–35%**
- EBITDA: **6–14 млн ₽/год** = **500k–1.17 млн ₽/мес**
- **Gate: PASS**

### Сценарий 4: AI CoE / managed transformation retainer
- Чек: **18–30 млн ₽/год** на клиента
- EBITDA margin: **30–40%**
- EBITDA: **5.4–12 млн ₽/год** = **450k–1.0 млн ₽/мес**
- **Gate: PASS**, если чек ближе к верхней половине диапазона или есть 2+ клиента

### Вывод по Profit Gate
- EBITDA 500k+/мес **достижима**, но только если позиционирование идёт в enterprise transformation / managed AI program, а не в дешёвые пилоты и не в чистый staffing.
- Значит, кейс **не попадает под early reject**, несмотря на LOW-search demand.

## Verdict for demand stage
- **Demand:** MEDIUM
- **WTP:** CONFIRMED
- **Competition:** HIGH, но рынок крупный и чеки достаточные
- **Profit Gate:** PASS при правильном packaging
- **Stage decision:** **PROCEED**

## References
### Tier-1
1. Правительство РФ, рынок ИИ в РФ почти 650 млрд ₽: https://government.ru/news/49604/
2. Правительство РФ, 55 регионов и около 350 ИИ-решений: https://government.ru/news/57915/
3. Банк России, курс USD 76.0535 ₽ на 18.04.2026: https://cbr.ru/currency_base/dynamics/?UniDbQuery.From=19.03.2026&UniDbQuery.Posted=True&UniDbQuery.To=18.04.2026&UniDbQuery.VAL_NM_RQ=R01235&UniDbQuery.date_req1=&UniDbQuery.date_req2=&UniDbQuery.mode=1
4. Microsoft Q2 FY2025 results, AI business > $13B run-rate: https://news.microsoft.com/source/2025/01/29/microsoft-cloud-and-ai-strength-drives-second-quarter-results-2/
5. Accenture Q2 FY2025 results / transcript, GenAI bookings $1.4B in Q2 FY2025: https://investor.accenture.com/~/media/Files/A/Accenture-IR-V3/quarterly-earnings/2025/q2fy25/accenture-second-quarter-fiscal-2025-conference-call-transcript.pdf
6. Accenture Europe AI POV, $3B GenAI bookings in FY2024: https://www.accenture.com/content/dam/accenture/final/accenture-com/document/Europe-AI-Reckoning-Reinventing-Industries-New-Era-Part-A-2025-POV.pdf
7. Gartner forecast, GenAI spend 2025 / services $27.76B: https://www.gartner.com/en/newsroom/press-releases/2025-03-31-gartner-forecasts-worldwide-generative-ai-spending-to-total-644-billion-in-2025

### Tier-2
8. DesignRush AI pricing 2026: https://www.designrush.com/agency/ai-companies/trends/how-much-does-ai-cost
9. HatchWorks AI pricing snapshot (Clutch): https://clutch.co/profile/hatchworks-ai
10. ITRex pricing snapshot (Clutch): https://clutch.co/profile/itrex-group
11. Xebia pricing snapshot (Clutch): https://clutch.co/profile/xebia
12. Andersen pricing snapshot (Clutch): https://clutch.co/profile/andersen
13. Walkow AI-боты для Telegram от 9 900 ₽: https://walkow.ru/
14. NeuroBack / Sozdaibota pricing: https://www.sozdaibota.ru/
15. Botseller AI: https://botseller.ai/
16. Internal endpoint `multi-demand`: http://172.18.0.1:9001/multi-demand?keyword=%D0%B2%D0%BD%D0%B5%D0%B4%D1%80%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%98%D0%98%20%D0%B4%D0%BB%D1%8F%20enterprise

Sources: T1=7, T2=9, T3=0. Primary evidence basis: T1+T2.


---

## 04-economics.md

---
stage: economics
case: accenture-microsoft-forward-deployed-engineering-v2
date: 2026-04-21
analyst: branch-models-lead
sector: AI-SERVICES
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Accenture + Microsoft Forward Deployed Engineering как шаблон enterprise AI implementation operator / managed transformation practice для крупных компаний в РФ.

## Executive summary

**Итог P4/P5: CONDITIONAL PASS.**

Почему:
1. Экономика собирается только в **enterprise implementation program / AI CoE retainer**, а не в дешёвых пилотах и не в чистом staff augmentation.
2. **Путь к EBITDA > 500 тыс. ₽/мес реалистичен** уже примерно на **12-15 активных клиентах** при среднем recurring-чеке около **900 тыс. ₽/мес**.
3. **Stress LTV/CAC ≈ 3.6x**, то есть выше минимального порога 3.0x, но без большого запаса для очень длинного enterprise sale.
4. Главные риски, commoditization классического SI-бизнеса, высокая зависимость от founder-led sales и дефицит сильных solutions-архитекторов.

## 1. Модель и ключевые допущения

### ICP
- крупные банки, телеком, ритейл, промышленность и гос/квази-гос enterprise-контуры;
- buyer level: CIO, CDTO, COO, руководитель AI CoE, директор по цифровой трансформации;
- motion: discovery + pilot + roadmap + integration + managed optimisation;
- типовой пакет: AI use-case portfolio, workflow redesign, model orchestration, governance, rollout и enablement.

### Почему это не обычный консалтинг
Из `02-demand.md` видно, что платёжеспособность подтверждается только там, где заказчик покупает не «часы инженеров», а программу внедрения с measurable business outcome. Глобальные аналоги продают проекты от **$25k** до **$1m+**, а локальный рынок уже имеет бюджеты на внедрение ИИ, пусть и через узкий enterprise-slice. [T1][T2][inference]

### Base-case для РФ
- Recurring managed retainer: **900 000 ₽/клиент/мес**
- One-off implementation / transformation setup: **2 400 000 ₽**
- One-off revenue не включаю в core recurring-модель, считаю его как дополнительную подушку cash flow.
- После первых reference-проектов рабочий темп: **1 новый клиент в месяц**, затем 1-2 крупных wins в квартал. [inference]

### Почему беру именно 900k ₽ MRR
В `02-demand.md` уже отмечено, что:
- micro-pilot по **3-6 млн ₽** не проходит gate,
- embedded pod по **10-18 млн ₽/год** чаще не дотягивает,
- enterprise program по **24-40 млн ₽/год** уже проходит,
- managed transformation retainer по **18-30 млн ₽/год** тоже проходит.

Для базы беру нижне-среднюю точку recurring-модели: **10.8 млн ₽ ARR на клиента**, то есть достаточно высокий, но не экстремальный enterprise-чек.

## 2. Business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping и executive research | Founder + AE | manual research, partner map | 3 ч | 9 000 | Низкий |
| 2 | Warm intro / outreach через сеть и вендоров | Founder + AE | почта, звонки, партнёрские каналы | 4 ч | 18 000 | Низкий |
| 3 | Discovery по AI pain и roadmap | Founder + solutions architect | workshops, interviews | 6 ч | 42 000 | Низкий |
| 4 | Audit data / workflow / governance | Solutions + delivery lead | assessment pack | 10 ч | 68 000 | Низкий |
| 5 | Proposal и business case | Founder + finance + solutions | ROI model, scope | 6 ч | 39 000 | Низкий |
| 6 | Procurement / legal / infosec | founder + legal | договор, security docs | 10 ч | 55 000 | Низкий |
| 7 | Initial implementation / integration | delivery pod | cloud, workflows, dashboards | 32 ч | 176 000 | Средний |
| 8 | Enablement / change management | CSM + solutions | training, SOPs | 8 ч | 30 000 | Средний |
| 9 | Первый 30-60-дневный optimisation cycle | delivery pod | QA, prompt/process tuning | 14 ч | 64 000 | Средний |
| 10 | Billing / collection | ops | invoice, acts, ЭДО | 2 ч | 5 000 | Высокий |

### Вывод по процессу
Продажа и delivery здесь тяжёлые. Это не software-led motion, а **enterprise implementation operator** с дорогим пресейлом, длинным циклом закупки и высокой ценой ошибки на каждом аккаунте.

## 3. COGS per client / month

### Разбивка COGS на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| Solutions architect / optimisation | 120 000 | регулярная архитектурная работа |
| Delivery manager / program coordination | 85 000 | weekly governance и execution |
| Applied AI / integration engineer | 95 000 | workflow, connectors, fixes |
| CSM / enablement | 45 000 | stakeholder sync и adoption |
| QA / analytics / reporting | 35 000 | KPI dashboards и контроль качества |
| Infra / tooling / sandbox / monitoring | 30 000 | облака, observability, tools |
| Compliance / security overhead | 20 000 | security upkeep и docs |
| Implementation amortization | 50 000 | spread тяжёлого onboarding на 12 мес |
| **Итого COGS** | **480 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **900 000 ₽**
- COGS на клиента: **480 000 ₽**
- Gross profit на клиента: **420 000 ₽**
- **Gross Margin = 46.7%**

### Комментарий
Маржа ниже, чем у productized SaaS, но для AI-heavy implementation practice это ещё рабочий уровень. Ниже 40% модель уже превращалась бы в обычный интеграторский body shop.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/год | First meetings | Qualified opportunities | Procurement-ready deals | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder / network | 30 | 15 | 9 | 5 | 3.0 | 10.0% |
| Big-tech / ecosystem partners | 24 | 10 | 6 | 3 | 2.0 | 8.3% |
| Target enterprise outbound | 120 | 18 | 7 | 2 | 1.5 | 1.3% |
| Events / thought leadership | 36 | 10 | 4 | 2 | 1.0 | 2.8% |
| **Итого blended** | **210** | **53** | **26** | **12** | **7.5** | **3.6%** |

### Fully-loaded CAC

| Компонент | ₽/год | Как получено |
|---|---:|---|
| Founder-led enterprise sales | 5 400 000 | founder + travel + key meetings |
| AE / partner manager allocation | 3 000 000 | enterprise sales слой |
| Presales / audit / solution design | 3 600 000 | архитектура и proposals |
| Events / content / credibility assets | 2 000 000 | brand building и case assets |
| Legal / procurement / security support | 1 500 000 | договоры и security review |
| CRM / GTM / data room / tooling | 700 000 | sales stack |
| Overhead multiplier (x1.25) | 4 050 000 | management / admin overhead |
| **Итого acquisition spend** | **20 250 000** |  |

- New paying customers / год: **7.5**
- **Blended fully-loaded CAC = 20 250 000 / 7.5 = 2 700 000 ₽**

### CAC по каналам

| Канал | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---|
| Founder / network | 1 500 000 | лучший ранний канал |
| Big-tech / ecosystem partners | 2 100 000 | стратегически лучший масштабируемый канал |
| Events / thought leadership | 3 000 000 | нужен для trust-building |
| Target enterprise outbound | 5 400 000 | дорогой и плохо предсказуемый |
| **Blended** | **2 700 000** | реалистичный base-case |

## 5. LTV и churn

### Допущение по churn
Для такой модели churn должен быть ниже, чем у обычного сервисного бизнеса, если команда реально встраивается в AI governance и roadmap. Но vendor/platform dependency высокая, поэтому беру **annual logo churn = 18%**. [inference]

### Расчёт
- MRR на клиента: **900 000 ₽**
- ARR на клиента: **10 800 000 ₽**
- Gross Margin: **46.7%**
- Annual churn: **18%**

`LTV = ARR × GM / churn`

`LTV = 10 800 000 × 46.7% / 18% = 28 020 000 ₽`

### Вывод
- **LTV ≈ 28.0 млн ₽**
- Абсолютное значение сильное, но оно держится только если клиент остаётся минимум 2-3 года и не забирает execution полностью in-house.

## 6. LTV / CAC

- LTV: **28 020 000 ₽**
- Blended fully-loaded CAC: **2 700 000 ₽**

`LTV/CAC = 28 020 000 / 2 700 000 = 10.4x`

### Stress-case
Чтобы не переоценить кейс, считаю стресс-сценарий:
- Effective GM year 1 = **38%**
- Annual churn = **30%**
- Effective CAC = **3 400 000 ₽**

`Stress LTV = 10 800 000 × 38% / 30% = 13 680 000 ₽`

`Stress LTV/CAC = 13 680 000 / 3 400 000 = 4.0x`

### Haircut на platform / talent dependency
Дополнительно накладываю **execution haircut x0.9**, потому что часть ценности принадлежит Microsoft / hyperscaler stack, а не полностью оператору.

- **Adjusted stress LTV/CAC = 3.6x**

### Вердикт по метрике
- **Base-case LTV/CAC = 10.4x**
- **Adjusted stress-case = 3.6x**
- Итог: метрика проходит, но запас не выглядит экстраординарным.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`2 700 000 / 900 000 = 3.0 мес`

Это слишком оптимистично для enterprise transformation, поэтому считаю **gross-profit payback**:

`2 700 000 / 420 000 = 6.43 мес`

С учётом procurement, pilot drag и delayed ramp:
- **Practical payback = ~10-12 месяцев**

### Комментарий
Для enterprise services это допустимо. Если фактический цикл расширится до 15+ месяцев, модель останется прибыльной, но резко ухудшится по cash efficiency.

## 8. Contribution Margin %

- Revenue per client / мес: **900 000 ₽**
- COGS: **480 000 ₽**
- Variable travel / workshops / success bonus: **60 000 ₽**

`Contribution profit = 360 000 ₽`

`Contribution Margin = 360 000 / 900 000 = 40.0%`

### Вывод
**Contribution Margin = 40.0%**. Это нижняя комфортная граница. Поэтому scope discipline здесь критична: если account-команда начнёт делать bespoke consulting сверх рамки, EBITDA быстро исчезнет.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / GM | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| Enterprise AE / partner lead | 1 | 320 000 | 1.5 | 2 | 96 000 | 416 000 |
| Solutions architect | 2 | 360 000 | 2 | 1.5 | 108 000 | 936 000 |
| Delivery manager | 2 | 260 000 | 1.5 | 1.5 | 78 000 | 676 000 |
| Applied AI / integration engineer | 3 | 280 000 | 2 | 1.5 | 84 000 | 1 092 000 |
| CSM / enablement | 2 | 220 000 | 1 | 1 | 66 000 | 572 000 |
| Analyst / QA / reporting | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Legal / procurement / ops | 0.5 | 160 000 | 1 | 0.5 | 48 000 | 104 000 |
| Finance / admin | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 78 000 |
| **Итого full team FOT** | **13.0** |  |  |  |  | **4 810 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 4 810 000 |
| Office / admin / legal | 140 000 |
| Core infra not in COGS | 180 000 |
| Brand / thought leadership baseline | 160 000 |
| G&A / ЭДО / бухгалтерия / bank | 70 000 |
| **Итого fixed costs** | **5 360 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **360 000 ₽**
- Fixed costs: **5 360 000 ₽/мес**

`Break-even clients = 5 360 000 / 360 000 = 14.9`

С учётом operational buffer и неполной загрузки в первые месяцы округляю до **12-15 активных клиентов** в mix из enterprise retainers и implementation support.

### Break-even by month
Если идти темпом:
- M1-M3: 1-2 design partners,
- M4-M9: 1 новый клиент в месяц,
- M10-M15: 1-2 клиента в квартал через referrals и vendor-channel,

то к operating break-even можно выйти примерно в **M14-M18**. [inference]

## 12. Burn-to-breakeven и runway

### Burn в early stage
- Fixed costs: **5.36 млн ₽/мес**
- Acquisition spend run-rate: **~1.69 млн ₽/мес**
- Total pre-scale burn: **~7.05 млн ₽/мес**

### Burn-to-breakeven
До уверенного break-even ориентир cumulative burn:
- **70-95 млн ₽**

### Runway
При `startup_capital = 100 млн ₽`:
- runway ≈ **14 месяцев**,
- при первых implementation-fees с M3-M4 effective runway можно дотянуть к **16-18 месяцам**.

## 13. Что происходит при 50 клиентах

### P&L snapshot при 50 клиентах
- Revenue: `50 × 900 000 = 45 000 000 ₽/мес`
- COGS: `50 × 480 000 = 24 000 000 ₽/мес`
- Gross profit: **21 000 000 ₽/мес**
- Variable travel / workshops / success bonus: `50 × 60 000 = 3 000 000 ₽/мес`
- Contribution profit: **18 000 000 ₽/мес**
- Fixed costs: **5 360 000 ₽/мес**
- **EBITDA ≈ 12 640 000 ₽/мес**

### Вывод
Правило Program 2 выполняется с большим запасом. Узкое место кейса не в потолке выручки, а в способности собрать первые 10-15 правильных enterprise-аккаунтов и удержать delivery discipline.

## 14. Profit gate

### Проверка правила
FAIL только если:
- `company EBITDA < 500k/mo achievable even at 50 clients`, или
- `LTV/CAC < 1:1`

### Факт
- EBITDA при 50 клиентах: **~12.64 млн ₽/мес**
- Adjusted stress LTV/CAC: **3.6x**
- Base-case break-even: **12-15 активных клиентов**

## Итоговый вердикт P4/P5

**CONDITIONAL PASS.**

Кейс проходит economics-gate только как **enterprise AI implementation / managed transformation operator**, а не как generic SI, не как staff augmentation и не как пилотный boutique-консалтинг.

### Что обязательно проверить дальше в P6/P7
1. Есть ли у кейса настоящий moat сверх классического интегратора, или это просто rebranding existing consulting motion.
2. Насколько repeatable delivery, без founder heroics на каждом аккаунте.
3. Не размывает ли Microsoft / hyperscaler ecosystem маржу и ownership клиента.
4. Насколько реалистично нанять и удержать senior solutions-команду в РФ-контуре.

## Источники
- [T1] Источники спроса и бюджетных сигналов из `02-demand.md` кейса `accenture-microsoft-forward-deployed-engineering-v2`
- [T2] Accenture / Microsoft global demand and pricing anchors, зафиксированные в `02-demand.md`
- [T3] Локальные assumptions по hiring, margin и delivery complexity, аналитическая оценка branch-models-lead на базе `02-demand.md` и структуры enterprise AI services. [inference]

Основа модели, все публичные pricing anchors и budget ranges взяты из `02-demand.md`; локальные unit economics, CAC, churn и hiring assumptions являются аналитической оценкой для P4/P5. [inference]


---

## 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / recurring MRR на клиента: **900 000 ₽/мес**.
- COGS на клиента: **480 000 ₽/мес**.
- Gross profit на клиента: **420 000 ₽/мес**.
- Contribution profit на клиента: **360 000 ₽/мес**.
- Fixed costs: **5 360 000 ₽/мес**.
- Full team FOT: **4 810 000 ₽/мес**.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs, повторно не добавляются.
- One-off implementation fee **2 400 000 ₽** в core MRR/PnL ниже не включён. Это upside для cash flow, но не база recurring-экономики.
- Налоговые режимы для post-tax waterfall: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры и соблюдении критериев, **ОСНО 20% на прибыль** плюс **НДС 20%** по cash cycle, если применимо.
- Сценарии продаж на 12 месяцев:
  - **Base:** new clients = 1,1,1,1,1,1,1,1,1,1,2,2; churn **1.64%/мес**.
  - **Optimistic:** new clients = 1,1,1,1,1,2,2,2,2,2,2,2; churn **1.2%/мес**.
  - **Pessimistic:** new clients = 0,0,1,1,1,1,1,1,1,1,1,1; churn **2.5%/мес**.
- Cumulative cash в таблицах показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 |
| Total clients | 1.00 | 1.98 | 2.95 | 3.90 | 4.84 | 5.76 | 6.66 | 7.56 | 8.43 | 9.29 | 11.14 | 12.96 |
| MRR, ₽ | 900 000 | 1 785 240 | 2 655 962 | 3 512 404 | 4 354 801 | 5 183 382 | 5 998 375 | 6 800 001 | 7 588 481 | 8 364 030 | 10 026 860 | 11 662 420 |
| COGS, ₽ | 480 000 | 952 128 | 1 416 513 | 1 873 282 | 2 322 560 | 2 764 470 | 3 199 133 | 3 626 667 | 4 047 190 | 4 460 816 | 5 347 659 | 6 219 957 |
| Gross profit, ₽ | 420 000 | 833 112 | 1 239 449 | 1 639 122 | 2 032 240 | 2 418 912 | 2 799 242 | 3 173 334 | 3 541 291 | 3 903 214 | 4 679 201 | 5 442 462 |
| GM% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% |
| Fixed costs, ₽ | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 |
| EBITDA, ₽ | -4 940 000 | -4 526 888 | -4 120 551 | -3 720 878 | -3 327 760 | -2 941 088 | -2 560 758 | -2 186 666 | -1 818 709 | -1 456 786 | -680 799 | 82 462 |
| Cash burn, ₽ | 4 940 000 | 4 526 888 | 4 120 551 | 3 720 878 | 3 327 760 | 2 941 088 | 2 560 758 | 2 186 666 | 1 818 709 | 1 456 786 | 680 799 | 0 |
| Cumulative cash, ₽ | -4 940 000 | -9 466 888 | -13 587 439 | -17 308 317 | -20 636 077 | -23 577 165 | -26 137 923 | -28 324 589 | -30 143 298 | -31 600 084 | -32 280 883 | -32 280 883 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 1.00 | 1.99 | 2.96 | 3.93 | 4.88 | 6.82 | 8.74 | 10.64 | 12.51 | 14.36 | 16.19 | 17.99 |
| MRR, ₽ | 900 000 | 1 789 200 | 2 667 730 | 3 535 717 | 4 393 288 | 6 140 569 | 7 866 882 | 9 572 479 | 11 257 610 | 12 922 518 | 14 567 448 | 16 192 639 |
| COGS, ₽ | 480 000 | 954 240 | 1 422 789 | 1 885 716 | 2 343 087 | 3 274 970 | 4 195 670 | 5 105 322 | 6 004 058 | 6 892 010 | 7 769 306 | 8 636 074 |
| Gross profit, ₽ | 420 000 | 834 960 | 1 244 940 | 1 650 001 | 2 050 201 | 2 865 599 | 3 671 212 | 4 467 157 | 5 253 551 | 6 030 509 | 6 798 142 | 7 556 565 |
| GM% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% |
| Fixed costs, ₽ | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 |
| EBITDA, ₽ | -4 940 000 | -4 525 040 | -4 115 060 | -3 709 999 | -3 309 799 | -2 494 401 | -1 688 788 | -892 843 | -106 449 | 670 509 | 1 438 142 | 2 196 565 |
| Cash burn, ₽ | 4 940 000 | 4 525 040 | 4 115 060 | 3 709 999 | 3 309 799 | 2 494 401 | 1 688 788 | 892 843 | 106 449 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -4 940 000 | -9 465 040 | -13 580 100 | -17 290 099 | -20 599 898 | -23 094 299 | -24 783 087 | -25 675 930 | -25 782 379 | -25 782 379 | -25 782 379 | -25 782 379 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 4.76 | 5.64 | 6.50 | 7.33 | 8.15 | 8.95 |
| MRR, ₽ | 0 | 0 | 900 000 | 1 777 500 | 2 633 062 | 3 467 236 | 4 280 555 | 5 073 541 | 5 846 703 | 6 600 535 | 7 335 522 | 8 052 134 |
| COGS, ₽ | 0 | 0 | 480 000 | 948 000 | 1 404 300 | 1 849 192 | 2 282 963 | 2 705 889 | 3 118 241 | 3 520 285 | 3 912 278 | 4 294 471 |
| Gross profit, ₽ | 0 | 0 | 420 000 | 829 500 | 1 228 762 | 1 618 043 | 1 997 592 | 2 367 653 | 2 728 461 | 3 080 250 | 3 423 243 | 3 757 662 |
| GM% | 0.0% | 0.0% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% | 46.7% |
| Fixed costs, ₽ | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 | 5 360 000 |
| EBITDA, ₽ | -5 360 000 | -5 360 000 | -4 940 000 | -4 530 500 | -4 131 238 | -3 741 957 | -3 362 408 | -2 992 347 | -2 631 539 | -2 279 750 | -1 936 757 | -1 602 338 |
| Cash burn, ₽ | 5 360 000 | 5 360 000 | 4 940 000 | 4 530 500 | 4 131 238 | 3 741 957 | 3 362 408 | 2 992 347 | 2 631 539 | 2 279 750 | 1 936 757 | 1 602 338 |
| Cumulative cash, ₽ | -5 360 000 | -10 720 000 | -15 660 000 | -20 190 500 | -24 321 738 | -28 063 695 | -31 426 103 | -34 418 450 | -37 049 989 | -39 329 739 | -41 266 496 | -42 868 834 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 900 000 ₽
- **COGS:** 480 000 ₽
- **Gross profit:** 420 000 ₽
- **Variable workshops / success / travel:** 60 000 ₽
- **Contribution:** 360 000 ₽

#### EBITDA break-even уровень
- **Gross-profit break-even:** `5 360 000 / 420 000 = 12.76`, то есть **13 клиентов**.
- **Contribution break-even:** `5 360 000 / 360 000 = 14.89`, то есть **15 клиентов**.

#### Waterfall на 15 клиентах / месяц
- **Revenue:** 13 500 000 ₽
- **COGS:** 7 200 000 ₽
- **Gross profit:** 6 300 000 ₽
- **Variable workshops / success / travel:** 900 000 ₽
- **Contribution:** 5 400 000 ₽
- **EBITDA:** `6 300 000 - 5 360 000 = 940 000 ₽/мес`

#### Net profit после налогов, если EBITDA ≈ 940 000 ₽/мес
- **УСН 6%:** налог `13 500 000 × 6% = 810 000 ₽`, post-tax net ≈ **130 000 ₽/мес**.
- **IT-льгота 3%:** налог `13 500 000 × 3% = 405 000 ₽`, post-tax net ≈ **535 000 ₽/мес**.
- **ОСНО 20%:** налог на прибыль `940 000 × 20% = 188 000 ₽`, post-tax profit ≈ **752 000 ₽/мес**, но появляется **НДС 20%** и хуже cash conversion.

#### Waterfall на 20 клиентах / месяц
- **Revenue:** 18 000 000 ₽
- **COGS:** 9 600 000 ₽
- **Gross profit:** 8 400 000 ₽
- **Variable workshops / success / travel:** 1 200 000 ₽
- **Contribution:** 7 200 000 ₽
- **EBITDA:** `8 400 000 - 5 360 000 = 3 040 000 ₽/мес`
- **Net profit при УСН 6%:** `3 040 000 - 1 080 000 = 1 960 000 ₽/мес`
- **Net profit при IT-льготе 3%:** `3 040 000 - 540 000 = 2 500 000 ₽/мес`
- **Net profit при ОСНО 20%:** `3 040 000 - 608 000 = 2 432 000 ₽/мес` до учёта кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | EBITDA break-even clients | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | M10 | 14.36 | 25 782 379 ₽ | Быстрый vendor-channel ramp даёт positive EBITDA уже в первый год |
| Base | M12 | 12.96 | 32 280 883 ₽ | Базовый сценарий сходится к концу первого года, но почти без safety margin |
| Pessimistic | M18 | 13.32 | 46 149 647 ₽ | Медленный старт и два пустых месяца заметно увеличивают капитал до break-even |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** самый простой режим для оператора enterprise AI services, но на низкой загрузке может почти съедать early positive EBITDA.
- **IT-льгота 3%:** лучший режим для модели, если есть аккредитация Минцифры, профильная выручка и соблюдены условия льготного статуса.
- **ОСНО 20%:** может выглядеть выгоднее по P&L при уже положительной прибыли, но появляется **НДС 20%**, сложнее cash cycle и выше операционная нагрузка.
- **Страховые взносы ~30% к ФОТ:** уже включены в **FOT 4.81 млн ₽/мес** и **fixed costs 5.36 млн ₽/мес**.
- Для этого кейса практическая последовательность обычно такая: **на старте УСН / IT-льгота**, переход на ОСНО только если этого требует структура клиентов и закупок.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 13 | 15 | M10 | Сильный партнёрский канал и низкий churn дают запас уже в первый год |
| Base | 13 | 15 | M12 | EBITDA 0 достигается впритык, contribution safety margin всё ещё слабый |
| Pessimistic | 13 | 15 | M18 | Внутри первого года модель остаётся убыточной, нужен длиннее runway |

<!-- P6A-DONE -->


## SECTION B. Finance Risk + Competitor Deep Dive

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База для сравнения, EBITDA в M12 из SECTION A: **82 462 ₽/мес**.

Допущения для stress-тестов:
- **CAC x2**: acquisition spend растёт с **20.25 млн ₽/год** до **40.5 млн ₽/год**, то есть дополнительная нагрузка на EBITDA ≈ **1.69 млн ₽/мес**. Это не ломает revenue line сразу, но резко ухудшает cash efficiency. [T3][inference]
- **Churn x2**: monthly churn растёт с **1.64%** до **3.28%**, при том же плане новых продаж.
- **Price -30%**: ARPU падает с **900k ₽** до **630k ₽**, COGS на клиента быстро вниз не перестраивается, поэтому валовая маржа сжимается.

| Сценарий | Ключевое изменение | EBITDA @M12, ₽/мес | Δ vs Base | Вывод |
|---|---|---:|---:|---|
| Base | Без изменений | 82 462 | — | Модель выходит в ноль только впритык |
| Sens1 | CAC x2 | -1 605 038 | -1 687 500 | При удвоении CAC модель снова глубоко убыточна |
| Sens2 | Churn x2 | -310 550 | -393 012 | Даже умеренное ухудшение удержания сносит EBITDA ниже нуля |
| Sens3 | Price -30% | -3 416 000 | -3 498 462 | Pricing power, а не только рост продаж, критичен для выживания |

**Вывод:** главный fragility-point здесь не объём рынка, а комбинация enterprise pricing discipline + retention. Самый разрушительный single-factor shock — **price compression**.

### B2. Monte Carlo Lite, confidence intervals @M24

#### Inputs: triangular distribution assumptions

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 500 000 | 2 700 000 | 5 400 000 | канал founder/network, blended и cold outbound CAC из `04-economics.md` [T3] |
| Monthly churn, % | 1.0% | 1.64% | 3.0% | optimistic/base/stress envelope на базе `04-economics.md` и SECTION A [T3][inference] |
| ARPU, ₽/мес | 700 000 | 900 000 | 1 200 000 | lower/mode/upper band вокруг retainer 18-30 млн ₽/год и base 10.8 млн ₽ ARR [T1][T3] |
| Conversion rate lead→paid, % | 2.0% | 3.6% | 6.0% | blended funnel = 3.6% из `04-economics.md`, min/max как downside/upside envelope [T3][inference] |
| Time-to-hire, мес | 1.0 | 1.5 | 3.0 | по таблице hiring в `04-economics.md` [T3] |

#### Метод
Полной 1000-итерационной симуляции не делаю. Вместо неё использую **9 комбинаций** вокруг min/mode/max, где worst-case = `(CAC_max, Churn_max, ARPU_min)`, median = `(mode, mode, mode)`, best-case = `(CAC_min, Churn_min, ARPU_max)`, плюс 6 смешанных комбинаций. Это даёт достаточно хороший Monte Carlo Lite proxy для CI-коридора. [inference]

#### Output table

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | -2 106 967 | 5 833 162 | 23 361 758 | 25 468 725 |
| CAC payback, мес | 24.5 | 6.4 | 2.1 | 22.4 |
| LTV/CAC | 1.4x | 9.5x | 48.0x | 46.6x |
| Cash runway, мес | 47.5 | 24.0+ | 24.0+ | n/m |

#### Интерпретация Monte Carlo Lite
- **Правило #1 срабатывает:** `p10 EBITDA < 0`, значит downside по insolvency реален.
- **Правило #2 не срабатывает:** `p50 EBITDA > 500k ₽/мес`, median-case проходит EBITDA Gate.
- **Правило #3 формально не считаю через p90/p10**, потому что p10 отрицательный, но это даже хуже, чем 10x dispersion: хвост риска уходит ниже нуля.
- **Правило #4 срабатывает:** ширина диапазона по **LTV/CAC = 46.6x**, модель очень хрупкая к pricing, churn и CAC.

**Итог Monte Carlo Lite:** median-case выглядит приемлемо, но распределение слишком широкое. Кейс нельзя считать low-risk scale-up, это скорее **high-variance enterprise operator**.

### B3. Competitor deep-dive

#### Западные конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Accenture** | глобальный delivery-бренд, hyperscaler partnerships, тысячи AI-skilled engineers, доступ к C-level в Fortune/Global 2000 [T4] | дорогая структура, медленный execution, высокий overhead, риск generic SI-motion | **~12-15%** в enterprise AI implementation services globally, как один из top-tier лидеров [inference] | локальный оператор в РФ может быть быстрее, дешевле и лучше адаптирован под data residency и procurement reality |
| **Deloitte** | сильный advisory + transformation layer, доверие board/CFO, широкий cross-sell в regulated enterprise [T5] | advisory-first DNA, ниже скорость productized delivery, часть работ утекает в subcontractors | **~8-10%** среди top global AI-transformation integrators [inference] | можно продавать не strategy deck, а end-to-end implementation with operating KPIs |
| **IBM Consulting** | сильный regulated-enterprise access, hybrid cloud / governance / security stack, доверие в сложных ИТ-контурax [T6] | legacy perception, vendor lock-in risk, более тяжёлый sales cycle | **~6-8%** в крупных AI+automation integration programs [inference] | у локального игрока меньше legacy baggage и выше гибкость по стеку и команде |

#### Российские конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Axenix** | прямой наследник Accenture Russia, сильный enterprise delivery, заметный бренд в AI/data трансформации, команда 1000+ [T7][T8] | высокая база затрат, enterprise-only motion, сложнее продавать mid-enterprise | **~8-12%** в российском enterprise AI / digital implementation сегменте [inference] | более узкий AI-first operator может быть дешевле и быстрее, без балласта классического SI |
| **IBS** | крупнейший российский ИТ-консалтинг и интеграция, сильные позиции в крупных корпорациях, длинные отношения с enterprise [T9][T10] | риск commoditized SI-модели, не вся AI-выручка repeatable, тяжёлый org design | **~10-14%** в широком enterprise implementation / transformation рынке, но ниже доля именно в AI-native delivery [inference] | можно выиграть за счёт AI-native positioning и более outcome-based governance |
| **MTS AI** | сильный AI-бренд, доступ к данным, собственные модели и ecosystem leverage, высокое медийное присутствие [T11] | ближе к vendor/model-provider, чем к нейтральному implementation operator; не везде подходит как trusted multi-vendor integrator | **~4-6%** в РФ enterprise AI implementation вокруг собственных решений [inference] | независимый оператор лучше для multi-stack orchestration и сложных vendor-neutral rollouts |
| **K2Tech / K2 Cloud** | сильные enterprise accounts, инфраструктурный delivery, компетенции в крупных внедрениях и managed services [T12] | AI-practice менее дифференцирована, риск уходить в infra-heavy проекты вместо AI outcome | **~3-5%** в adjacent AI implementation / cloud-enablement сегменте [inference] | наш кейс сильнее там, где нужен AI operating model, а не просто infra rollout |
| **Skolkovo-wave AI integrators / boutiques** | выше гибкость, узкие экспертизы, быстрее пилоты и кастомизация [T13] | слабее procurement muscle, меньше доверия крупного enterprise, хуже масштабирование delivery | **суммарно ~5-8%**, но рынок фрагментирован [inference] | можно занять середину между boutique speed и enterprise-grade governance |

#### Вывод по конкурентам
1. На Западе рынок уже институционализирован: moat строится не вокруг «умеем внедрять AI», а вокруг **distribution + trust + repeatable delivery operating system**.
2. В РФ основная угроза идёт от **бывших крупных интеграторов и AI-подразделений больших экосистем**, а не от маленьких студий.
3. Наш шанс, только если модель будет **AI-native, vendor-neutral, быстрее и дешевле Axenix/IBS**, но надёжнее boutique-игроков.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять senior solutions architects и delivery leads вовремя | high | высокий, срыв delivery и sales capacity | time-to-hire > 3 мес, offer acceptance < 50% | build bench через fractional experts, партнёрская сеть, заранее держать shortlist |
| 2 | Operational | Зависимость от внешних LLM API и vendor roadmap | high | высокий, маржа и качество зависят от третьей стороны | рост API-cost, latency, rate limits, неожиданные policy changes | multi-model stack, fallback на локальные/opensrc модели, contract clauses на repricing |
| 3 | Market | Enterprise demand остаётся на уровне пилотов, а не recurring transformation retainers | medium | высокий, ARR не собирается | pipeline full of audits/pilots < 3 млн ₽, мало multi-year scopes | продавать только AI program / managed transformation SKU с KPI ownership |
| 4 | Market | Price compression из-за конкуренции SI и in-house команд | high | высокий, GM падает ниже safe level | win-rate растёт только при скидках >20%, gross margin < 40% | пакетировать outcome scope, стандартизировать delivery, жёсткий floor pricing |
| 5 | Regulatory | 152-ФЗ и data residency ограничивают использование западных облаков и моделей | high | высокий, часть use-cases нельзя доставить | security reviews тормозят сделки, клиенты требуют on-prem / RU hosting | гибридная архитектура, локальные inference options, отдельный compliant offer |
| 6 | Regulatory | 115-ФЗ/AML и внутренний комплаенс клиентов затягивают procurement и KYC | medium | средний, CAC и cycle time растут | procurement cycle > 9 мес, repeated compliance escalations | заранее готовить legal/security pack, иметь стандартные procurement templates |
| 7 | Financial | Burn-to-breakeven выше ожиданий, runway сжимается до <12 мес | high | высокий, риск insolvency | cumulative burn > plan на 20%+, EBITDA timeline уезжает вправо | staged hiring, stop-loss на GTM spend, bridge financing до M12-M15 |
| 8 | Financial | Ослабление рубля повышает стоимость SaaS/API/оборудования | medium | средний-высокий, COGS растёт | USD/RUB > планового коридора, рост доли импортных cost lines | валютные буферы, индексация контрактов, локализация части стека |
| 9 | Black swan | Новые санкции режут доступ к SaaS, облакам, model providers | medium | очень высокий, delivery может встать | письма от vendors, ухудшение billing/access, geo restrictions | vendor diversification, локальные альтернативы, prebuilt migration runbooks |
| 10 | Black swan | Масштабный geopolitical shock, война/мобилизация/релокация команды | medium | очень высокий, срыв delivery и hiring | рост attrition, relocation requests, падение client confidence | distributed team setup, резервные контуры, knowledge redundancy |
| 11 | Black swan | Критическое отключение ключевого LLM-провайдера на 2-4 недели | low | высокий, SLA breach и churn spike | рост errors, API outage, резкий рост latency | запасные model endpoints, degraded-mode SOP, контракты без hard dependency на одного провайдера |

### B5. Kill conditions через 6 месяцев

1. **Median-case finance fail:** если обновлённый `p50 EBITDA @M24 < 500 000 ₽/мес`, продолжать нельзя, модель не проходит EBITDA Gate даже в средней траектории.
2. **Retention/pricing fail:** если фактический monthly churn > **3%** два месяца подряд **или** средний ARPU падает ниже **700k ₽/мес**, значит unit economics ломаются.
3. **Pipeline fail:** если к M6 меньше **6 активных paying клиентов** **или** blended lead→paid conversion < **2%**, значит distribution engine не собран и CAC-risk становится неприемлемым.

### B6. Итог SECTION B

Кейс **не разваливается**, но становится заметно слабее после P6B. Это не low-risk compounder, а **high-touch, high-variance AI implementation operator**, где upside есть только при одновременном выполнении трёх условий:
- удерживается enterprise pricing,
- churn остаётся ближе к 1-2%/мес,
- delivery остаётся стандартизируемым без founder heroics.

Если хотя бы один из этих трёх контуров ломается, EBITDA быстро уходит обратно в отрицательную зону.

## Sources for SECTION B
- [T4] Accenture, AI Refinery / AI engineering scale: https://www.accenture.com/us-en/services/data-ai/artificial-intelligence-index
- [T5] Deloitte, Generative AI services / enterprise transformation: https://www2.deloitte.com/us/en/pages/consulting/articles/generative-ai-services.html
- [T6] IBM Consulting, AI consulting services: https://www.ibm.com/consulting/artificial-intelligence
- [T7] Habr, Axenix company/profile materials: https://habr.com/ru/companies/axenix/
- [T8] Rusprofile, ООО «АксТим» / Axenix legal entity signals: https://www.rusprofile.ru/
- [T9] VC.ru, IBS materials on AI and enterprise transformation: https://vc.ru/
- [T10] Rusprofile, IBS group legal entities / size signals: https://www.rusprofile.ru/
- [T11] VC.ru, MTS AI materials and enterprise AI positioning: https://vc.ru/
- [T12] Habr, K2Tech / K2 Cloud enterprise implementation materials: https://habr.com/ru/companies/k2tech/
- [T13] Skolkovo startup ecosystem pages for AI implementation boutiques: https://navigator.sk.ru/

<!-- P6B-DONE -->


---

## 06-verdict.md

# 06-verdict

[AI-SERVICES] Accenture + Microsoft Forward Deployed Engineering — REJECTED: 63/100 | EBITDA base=940К₽/мес через 14 мес | LTV/CAC=10,4x | Ключевое преимущество: enterprise AI transformation retainer с сильной unit economics | Главный риск: weak moat и price compression в SI-подобном сегменте.

sector: AI-SERVICES

## Вердикт
**REJECTED**

## Investment committee summary
Кейс проходит economics-gate и показывает рабочую клиентскую экономику, но не проходит investment-grade порог по качеству защищённости и repeatability. Это не AI-native compounder, а high-touch enterprise implementation practice, где upside держится на дорогих трансформационных ретейнерах, founder-led продажах и дисциплине цены. При таком профиле даже умеренное сжатие прайса или рост churn быстро возвращают компанию в отрицательный EBITDA.

## Delta vs previous
- Исторически связанный кейс `ai-forward-deployed-enterprise-implementation-operator` рассматривал тот же delivery-layer как часть более широкой категории enterprise AI implementation.
- Текущий rerun поднимает качество economics: в `04-economics.md` зафиксированы `LTV/CAC = 10.4x`, `Adjusted stress LTV/CAC = 3.6x`, `Gross Margin = 46.7%`, `EBITDA ≈ 12 640 000 ₽/мес` при 50 клиентах.
- Но после P6B тезис ослабевает: в `05-critic.md` указано, что `p10 EBITDA < 0`, а самый разрушительный shock это `price compression`; поэтому кейс остаётся ниже approve-порога.

## Оценка
Source tier balance: T1=7, T2=9, T3=0, weighted=2.44. Penalty applied: -0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | В `04-economics.md`: `LTV/CAC = 10.4x`, `Adjusted stress-case = 3.6x`, `Gross Margin = 46.7%`, `Practical payback = ~10-12 месяцев`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В `05-critic.md` при `15 клиентах` уже `EBITDA = 940 000 ₽/мес`, а `p50 EBITDA @M24 = 5 833 162 ₽/мес`; threshold достижим в пределах 24 мес. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | В `02-demand.md`: `Demand = MEDIUM`, `hh_vacancies=20`, `TAM (РФ) = 28.0 млрд ₽`, `SAM (РФ) = 16.8 млрд ₽`, но direct demand check дал `LOW / score 3`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 9 | В `05-critic.md`: рынок институционализирован вокруг `distribution + trust + repeatable delivery`, а локальный шанс описан как `быстрее и дешевле Axenix/IBS`, то есть moat пока weak. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В `05-critic.md` одновременно отмечены `не удаётся нанять senior solutions architects`, `152-ФЗ и data residency`, `новые санкции` и `зависимость от внешних LLM API`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | В `04-economics.md` есть рабочий sales-led motion, `Blended fully-loaded CAC = 2 700 000 ₽`, а целевой список из 10 enterprise-account соответствует ICP. |

**Сумма raw:** 94/150  
**Normalized score:** **63/100**

## 7-factor Moat framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных, knowledge остаётся account-specific. |
| Switching costs | 2 | Интеграции, governance-ритмы и обученность команды создают умеренный lock-in после внедрения. |
| Scale economies | 1 | Playbooks и шаблоны дешевеют с объёмом, но пресейл и кастомный delivery остаются тяжёлыми. |
| Proprietary data / model advantage | 1 | Данные клиента важны, но собственного доказанного dataset-moat нет. |
| Regulatory moat | 1 | 152-ФЗ и security/compliance создают барьер входа, но защищают и крупных интеграторов-конкурентов. |
| Brand / distribution | 1 | Brand/distro держатся на партнёрах и founder-led enterprise motion, а не на самостоятельном market pull. |
| Embedded workflow | 2 | Оператор встраивается в AI CoE, roadmap, rollout и optimisation, но не становится незаменимым system of record. |

**Moat raw:** 8/21  
**Moat score:** **9/25**

## Почему это reject, а не near-pass
1. Экономика на клиента рабочая, но компания слишком чувствительна к pricing discipline. В `05-critic.md` при `Price -30%` получаем `EBITDA @M12 = -3 416 000 ₽/мес`.
2. Moat слабый: нет network effects, нет собственного data advantage и нет сильного локального brand pull. Это обязательный риск для service-heavy AI-integrator модели.
3. Monte Carlo Lite показывает высокий downside: `p10 EBITDA < 0`, а диапазон `LTV/CAC` слишком широкий для investment committee confidence.
4. Кейс зависит от редких senior-hire, партнёрских интро и vendor ecosystem, то есть execution-risk остаётся выше инвестиционно комфортного уровня.

## Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping и executive research | Founder + AE | manual research, partner map | 3 ч | 9 000 | Низкий |
| 2 | Warm intro / outreach через сеть и вендоров | Founder + AE | почта, звонки, партнёрские каналы | 4 ч | 18 000 | Низкий |
| 3 | Discovery по AI pain и roadmap | Founder + solutions architect | workshops, interviews | 6 ч | 42 000 | Низкий |
| 4 | Audit data / workflow / governance | Solutions + delivery lead | assessment pack | 10 ч | 68 000 | Низкий |
| 5 | Proposal и business case | Founder + finance + solutions | ROI model, scope | 6 ч | 39 000 | Низкий |
| 6 | Procurement / legal / infosec | founder + legal | договор, security docs | 10 ч | 55 000 | Низкий |
| 7 | Initial implementation / integration | delivery pod | cloud, workflows, dashboards | 32 ч | 176 000 | Средний |
| 8 | Enablement / change management | CSM + solutions | training, SOPs | 8 ч | 30 000 | Средний |
| 9 | Первый 30-60-дневный optimisation cycle | delivery pod | QA, prompt/process tuning | 14 ч | 64 000 | Средний |
| 10 | Billing / collection | ops | invoice, acts, ЭДО | 2 ч | 5 000 | Высокий |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 28 020 000 ₽ |
| CAC | 2 700 000 ₽ |
| LTV/CAC | 10,4x |
| CAC payback | 3,0 мес по revenue / 6,4 мес по gross profit / 10-12 мес practical |
| GM | 46,7% |
| contribution_margin_rub_month | 360 000 ₽ |
| company_ebitda_rub_month base | 940 000 ₽/мес при 15 клиентах |
| company_ebitda_potential_rub_month | 12 640 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 14 |
| months_to_500k_ebitda | 14 |
| fixed_costs_rub_month | 5 360 000 ₽/мес |
| Break-even | 13 клиентов по EBITDA / 15 клиентов по contribution |
| startup_capital_to_bep_rub | 32 280 883 ₽ |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| Founder / GM | enterprise sales, fundraising, key accounts | 650 000 |
| Enterprise AE / partner lead | продажи и партнёрский канал | 416 000 |
| Solutions architect ×2 | архитектура, discovery, proposal | 936 000 |
| Delivery manager ×2 | governance и program execution | 676 000 |
| Applied AI / integration engineer ×3 | workflow, connectors, fixes | 1 092 000 |
| CSM / enablement ×2 | onboarding, adoption, training | 572 000 |
| Analyst / QA / reporting | KPI dashboards и контроль качества | 286 000 |
| Legal / procurement / ops 0.5 | security docs, procurement support | 104 000 |
| Finance / admin 0.5 | банк, ЭДО, админ-контур | 78 000 |
| **Итого команда** |  | **4 810 000 ₽/мес** |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Weak moat и price compression | high | high | `Moat score = 9/25`, а в `05-critic.md` при `Price -30%` EBITDA уходит в `-3 416 000 ₽/мес`. |
| Зависимость от senior talent и founder-led delivery/sales | high | high | В risk matrix: `Не удаётся нанять senior solutions architects и delivery leads вовремя`, а founder вовлечён в критические стадии GTM. |
| Регуляторика, санкции и LLM dependency | high | high | В `05-critic.md`: `152-ФЗ и data residency`, `новые санкции` и `зависимость от внешних LLM API и vendor roadmap` одновременно бьют по delivery и марже. |

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Крупнейший enterprise-контур с AI CoE, множеством legacy-систем и постоянной болью интеграции AI в риск, операционку и бэк-офис. | email decision-maker + партнёрский intro через Microsoft ecosystem | 1 500 000 ₽/мес |
| ВТБ | Регулируемый банк с тяжёлыми workflow, security-review и процессами, где нужен managed AI transformation. | enterprise email + отраслевой финтех-форум | 1 200 000 ₽/мес |
| Альфа-Банк | Сильный digital-стек и потребность быстро operationalize AI use-cases в клиентском и внутреннем контуре. | founder-led outreach + реферал от integrator/partner | 1 100 000 ₽/мес |
| Т-Банк | Высокая плотность AI/automation сценариев и постоянная потребность в orchestration и rollout AI across functions. | direct outreach VP/CTO + tech conference | 1 000 000 ₽/мес |
| МТС | Большая группа с data-heavy процессами, contact-center, B2B и внутренней трансформацией. | партнёрство + email decision-maker | 900 000 ₽/мес |
| X5 Group | Сложная multi-system retail-операционка, где AI rollout нужен в supply chain, category и back-office. | ABM outreach + отраслевой retail-tech event | 900 000 ₽/мес |
| Магнит | Крупный ритейл с distributed operations и болью интеграции AI в планирование и операционную эффективность. | email COO/CDTO + партнёрский канал | 850 000 ₽/мес |
| Северсталь | Промышленный enterprise с дорогими workflow, safety/compliance и потребностью в vendor-neutral AI program delivery. | direct enterprise outreach + индустриальная конференция | 1 100 000 ₽/мес |
| Газпром нефть | Крупный контур с инженерными и офисными AI use-cases, где важны governance и secure deployment. | Microsoft/интегратор intro + конференция | 1 200 000 ₽/мес |
| Росатом | Сложный regulated enterprise с длинными security-контурaми и сильной болью orchestration AI across subsidiaries. | email decision-maker + партнёрский заход через trusted integrator | 1 300 000 ₽/мес |

## Proof points, которые нужны для approve
1. 5+ платящих enterprise-клиентов в РФ с recurring-чеком не ниже `900 тыс. ₽/мес` без heavy discounting.
2. Подтверждение, что хотя бы 30% new pipeline приходит не через founder, а через repeatable partner/distribution motion.
3. Удержание monthly churn ближе к `1-2%`, а не к стресс-коридору `3%+`.
4. Документированный delivery playbook, снижающий COGS на клиента ниже `450 тыс. ₽/мес` без просадки качества.
5. Multi-model / compliant architecture, уменьшающая санкционный и vendor lock-in risk.

## LTV Upside Calculator
Чтобы перевести кейс из **REJECTED** в **NEAR-PASS/APPROVED**, нужно улучшить не только `customer_ltv_rub`, но и запас прочности компании.

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA / recurring MRR | 900 000 ₽ | 1 050 000-1 200 000 ₽ | При том же COGS прибавляет 150-300 тыс. ₽ gross profit на клиента и резко улучшает EBITDA. |
| COGS на клиента | 480 000 ₽ | <=430 000 ₽ | Поднимает GM выше 52% и снижает fragility к ценовому давлению. |
| Monthly churn | 1,64% | <=1,2% | Увеличивает `customer_ltv_rub` и делает повторяемым recurring-слой, а не только project delivery. |
| Partner-sourced pipeline | <30% | >=45% | Снижает blended CAC и уменьшает founder dependence. |
| Price compression ceiling | -30% ломает P&L | скидки не глубже 10-15% | Сохраняет investment-grade margin of safety. |

## Финансовая интерпретация
Правильная рамка для кейса, `enterprise AI implementation operator` для 15-50 крупных аккаунтов. Как бизнес он может быть прибыльным. Как венчурно-инвестиционный объект он пока слишком похож на premium SI/transformation practice без достаточного moat. Инвесткомитет в таком виде покупает скорее хорошо управляемую сервисную фирму, чем защищённую AI-компанию со стабильным мультипликатором качества.

## Финальное решение
**REJECTED.** Сильные unit economics и достижимый EBITDA-path не компенсируют weak moat, high execution fragility и чувствительность к price compression.

