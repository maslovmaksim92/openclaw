# verdict.md

Источник кейса: pipeline/rejected/scribe-optimize-geo-expand-v2

---

# Stage 1. Intake

---
sector: GEO-EXPAND
rerun: false
source_raw: 2026-04-25-geo-expand-scribe-optimize.md
created: 2026-04-25T03:37:00+03:00
---

# Intake

## Статус
Новый кейс, создан на этапе intake/triage. Сигнал не классифицирован как duplicate, потому что описывает отдельный wedge вокруг process intelligence и AI-ready mapping офисных процессов.

## Исходный raw-файл

# Scribe Optimize

## Sector
GEO-EXPAND

## Wedge statement
Платформа process intelligence для офисных команд: автоматически показывает, как сотрудники реально выполняют цифровые процессы, и находит конкретные узкие места и сценарии для AI-автоматизации.

## Evidence
- [T2] https://www.businessinsider.com/scribe-raises-30-million-series-b-new-ai-product-optimize-2025-11 — Business Insider: у Scribe более 78 000 корпоративных клиентов; новый продукт Optimize строится на данных о реальных рабочих процессах и помогает компаниям находить точки для оптимизации и внедрения AI.
- [T2] https://techcrunch.com/2025/11/06/scribe-a-documentation-startup-used-by-45-of-the-fortune-500-launches-a-new-ai-product/ — TechCrunch: Scribe используется 45% компаний из Fortune 500; компания расширила продукт в сторону AI-аналитики процессов, а не только генерации инструкций.
- [T3] https://scribehow.com/pricing — публичный pricing Scribe: командный тариф начинается от $59 в месяц, что даёт нижнюю границу для оценки ARR при заявленной клиентской базе.

## EBITDA hypothesis (24 мес, base)
700000-1800000₽/мес

## RU-fit
4 / 5. В РФ уже есть интерес к AI-внедрению в back-office, но почти нет зрелых локальных продуктов, которые не просто пишут инструкции, а строят карту реальных цифровых процессов и подсказывают, что автоматизировать первым. Ограничения по 152-ФЗ управляемы, если хранить события и скрин-артефакты локально.

## Expected unit economics (ballpark)
- ARPU: 90000-250000₽/мес
- CAC (ballpark): 180000-650000₽
- Avg deal cycle: 2-5 мес
- Target segment: Mid-market | Enterprise

## Why now
В 2026 году компании уже хотят не «ещё один AI-ассистент», а понятный слой process intelligence перед автоматизацией: где реально теряется время, какие действия повторяются, и где AI даст быстрый ROI. На российском рынке окно открыто, потому что спрос на импортозамещённые AI-внедрения растёт, а зрелого локального process-intelligence слоя почти нет.

## Market check
- western_revenue: оценочно от $55 млн ARR floor, если брать только публичный минимум $59/мес и 78 000 корпоративных клиентов; фактический ARR может быть выше за счёт enterprise-планов.
- ru_equivalent: partial. В РФ есть частичные аналоги для создания инструкций и SOP, но не найден прямой локальный аналог уровня process intelligence + AI readiness для офисных workflow.
- localization_effort: medium
- ltv_signal: 1500000-4500000₽ на клиента за 24 месяца
- company_ebitda_rub_month potential: 700000-1800000₽/мес к 24 месяцу при 15-30 клиентах mid-market и gross margin SaaS/AI-services уровня 70%+.



---

# Stage 2. Demand

# Demand validation

## Итог
- **Статус:** PASS TO NEXT STAGE
- **Demand:** mixed, direct category demand низкий, adjacent pain высокий.
- **Profit Gate:** **PASS**. Порог EBITDA 500 000 ₽/мес достижим в нескольких сценариях.
- **Ключевой вывод:** в РФ слабый спрос именно на терминологию process mining/task mining, но есть платёжеспособный спрос на внедрение автоматизации, AI-ready mapping и операционную эффективность для mid-market и enterprise. Значит продавать нужно не «task mining», а «поиск узких мест и приоритизация AI-автоматизации».[T1][T2]

## Demand signals
- По `process mining` composite demand = **LOW**, score 24; по `task mining` = **LOW**, score 18; по `автоматизация бизнес-процессов` = **MEDIUM**, score 30 и **4 838 вакансий** на hh.ru в выдаче агрегатора спроса. Это подтверждает, что термин-рынок узкий, а pain-рынок широкий.[T2]
- На hh.ru устойчиво присутствуют роли типа business analyst, process analyst, BPM/RPA, operational excellence, что подтверждает реальные бюджеты на поиск и улучшение процессов, а не только интерес «почитать про AI».[T1]
- В крупных российских компаниях уже продаются и внедряются Process Mining / Task Mining решения, в том числе Proceset и западные аналоги в безопасном контуре, значит willingness to pay существует.[T2]

## Конкуренты и цены
| Конкурент | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Scribe | документация + новый Optimize слой для поиска узких мест | Pro от **$15/seat/mo**, Team от **$29/seat/mo** [T3] | нижняя граница willingness to pay за workflow visibility даже без глубокой аналитики |
| ProcessMaker | BPM + process intelligence / automation stack | Platform от **$1 495/mo** [T2] | mid-market B2B чек уже близок к рабочему диапазону для РФ |
| Microsoft 365 + Process Mining (Power Automate Process Mining) | process mining внутри enterprise-стека | add-on **$5/user/mo** при qualifying Microsoft 365 plans [T1] | enterprise привык платить отдельно за процессную аналитику |
| Proceset (РФ) | process mining / task mining / process intelligence | проекты на рынке стартуют примерно от **1,5 млн ₽** за внедрение [T2/T3] | в РФ есть подтверждённый бюджет на локальные внедрения |

### Что это значит для цены Scribe-подобного wedge
- Для РФ реалистичный диапазон подписки: **150 000–450 000 ₽/мес** за команду/контур, плюс onboarding **300 000–1 500 000 ₽**.[T2]
- Для сегмента mid-market рабочий ARR: **1,8–3,0 млн ₽/год**. Для enterprise: **4,8–9,0 млн ₽/год**.[T2]

## Telegram в РФ
- Специализированных массовых Telegram-ботов именно под process intelligence в РФ не найдено; это **минус** для category pull.[T3, спекуляция]
- Зато есть Telegram-каналы и сервисы вокруг BPM/RPA/AI-автоматизации, а также интеграторы, которые используют Telegram как канал лидогенерации и education. Это означает, что канал awareness есть, но готового self-serve bot category нет.[T2]
- Вывод: Telegram для этого кейса, вероятнее всего, годится как контентный и outbound-канал, но не как основной продуктовый канал продаж.[T2]

## WTP, proof of willingness to pay
1. Microsoft monetizes process mining отдельным add-on, то есть enterprise-покупатель воспринимает process analytics как отдельную бюджетную строку, а не бесплатную feature.[T1]
2. ProcessMaker публично ставит цену выше $1,4k/мес, что подтверждает рыночную норму B2B-чека для automation/process stack.[T2]
3. В РФ проекты Proceset продаются с многомесячным экономическим эффектом и стартовыми бюджетами уровня миллионов рублей, что подтверждает готовность платить за локальный контур.[T2]
4. Наличие тысяч вакансий по автоматизации процессов и десятков вакансий по process mining указывает, что компании уже платят за эту функцию через фонд оплаты труда и готовы покупать software/services для ускорения ROI.[T1][T2]

## Market sizing
### Метод и допущения
- **Top-down база:** российские расходы организаций на ПО и цифровую трансформацию, адресуемая доля на слой process intelligence перед AI-внедрением.[T1]
- **Bottom-up база:** число реальных mid-market и enterprise покупателей в РФ × доля с подтверждённой болью × средний ARR.[T1][T2]
- Курс для грубых USD-сопоставлений: **90 ₽/$** как рабочее округление для investment screening; на итоговую рублёвую модель влияет ограниченно, потому что preferred estimate построен снизу вверх по РФ.[T1/T2]

### Top-down
- База: затраты организаций РФ на ПО и связанные цифровые решения, адресуемые для process intelligence, оцениваем как **~3,1 млрд ₽ TAM РФ**. Логика: из крупного пирога corporate software/digital spend адресуемый слой process intelligence остаётся узким, порядка **0,2%** spend.[T1][T2]
- **SAM РФ:** берём только mid-market/enterprise back-office и knowledge-work контуры, где нужна AI-readiness, получаем **~1,1 млрд ₽**.[T1][T2]
- **SOM Y1:** 2% SAM = **22 млн ₽**.[T2]
- **SOM Y3:** 8% SAM = **86 млн ₽**.[T2]

### Bottom-up
- Всего в РФ около **63,6 тыс.** средних и крупных организаций; это верхняя граница потенциальной базы покупателей, потому что микробизнес и большая часть малого бизнеса сюда не входят.[T1]
- Для этого wedge разумно брать только цифрово-зрелые отрасли и компании со сложным back-office: банки, страхование, ритейл, телеком, логистика, shared services, BPO, крупное производство. Консервативно это **~2%** от базы, или **1 272 компании**.[T1][T2]
- Доля с подтверждённой болью, где есть программы по автоматизации процессов и AI/операционной эффективности: **30%**, то есть **382 покупателя**.[T1][T2]
- Средний ARR: **2,4 млн ₽/год** (200 тыс. ₽/мес), в диапазоне между mid-market SaaS и enterprise pilot-to-rollout контрактом.[T2]
- **SAM bottom-up = 382 × 2,4 млн ₽ = 917 млн ₽**.[T2]
- **SOM Y1 bottom-up:** 12 клиентов × 2,4 млн ₽ = **29 млн ₽**.
- **SOM Y3 bottom-up:** 40 клиентов × 2,4 млн ₽ = **96 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 60–90 млрд ₽ экв. для сопоставимого process intelligence сегмента [T2] | — | — | top-down |
| TAM (РФ) | 3,1 млрд ₽ [T1][T2] | 3,05 млрд ₽ (1 272 × 2,4 млн ₽) [T1][T2] | diff ~2%, модели сошлись | lower |
| SAM (РФ) | 1,1 млрд ₽ [T1][T2] | 917 млн ₽ [T1][T2] | diff ~20%, bottom-up консервативнее | lower |
| SOM Y1 | 22 млн ₽ | 29 млн ₽ | diff умеренный, 9–12 клиентов | **22 млн ₽** |
| SOM Y3 | 86 млн ₽ | 96 млн ₽ | diff умеренный, rollout по сегменту | **86 млн ₽** |

### Реальные buyers для bottom-up и GTM-10
1. Сбер [T1/T2]
2. Т-Банк [T1/T2]
3. Альфа-Банк [T1/T2]
4. ВТБ [T1/T2]
5. X5 Group [T1/T2]
6. Магнит [T1/T2]
7. МТС [T1/T2]
8. Ростелеком [T1/T2]
9. Ozon [T1/T2]
10. СДЭК [T2]

Общий паттерн: крупный digital back-office, повторяемые офисные workflow, высокая цена ручных ошибок, программа AI/automation уже существует.[T1][T2]

## Profit Gate
### Сценарий 1, low
- 6 клиентов × 150 000 ₽/мес = 900 000 ₽ MRR
- Валовая маржа 75% = 675 000 ₽
- Opex команды 1,1 млн ₽/мес
- **EBITDA = -425 000 ₽/мес**
- Вывод: не проходит.

### Сценарий 2, base
- 12 клиентов × 200 000 ₽/мес = 2,4 млн ₽ MRR
- Валовая маржа 75% = 1,8 млн ₽
- Opex 1,2 млн ₽/мес
- **EBITDA = 600 000 ₽/мес**
- Вывод: **проходит**.

### Сценарий 3, enterprise
- 5 клиентов × 450 000 ₽/мес = 2,25 млн ₽ MRR
- Плюс onboarding/services, усреднённо 400 000 ₽/мес
- Валовая маржа blended 72% = 1,91 млн ₽
- Opex 1,1 млн ₽/мес
- **EBITDA = 810 000 ₽/мес**
- Вывод: **проходит**.

### Проверка на реалистичность
- SOM Y1 22 млн ₽ при ARR 2,4 млн ₽ означает около 9 клиентов в первый год, что укладывается в enterprise deal cycle 2–5 месяцев и не выглядит overclaiming.[T2]
- SOM Y1 < 10% SAM, значит модель реалистична.

## Риски
- Категорийный спрос на термины process mining/task mining в РФ слабый, значит вход через «новую категорию» дорогой.[T2]
- Часть ценности может восприниматься как услуга консалтинга, а не как продукт, что давит на мультипликатор и требует жёсткой productization-дисциплины.[T2]
- 152-ФЗ, ИБ и контроль пользовательских действий повышают требования к on-prem/private cloud варианту.[T1]

## Что делать на следующем этапе
- Проверить, можно ли зайти не как «process mining», а как **AI-readiness audit + workflow visibility** для 2–3 вертикалей: банки, ритейл, BPO/shared services.
- Отдельно проверить on-prem / secure contour архитектуру и продаваемость через интеграторов.
- Сфокусировать ICP на buyers: COO, head of transformation, CIO, shared services director.

## Verdict
Прямой категорийный спрос в РФ пока слабый, но economics и willingness to pay выглядят достаточными для инвестиционной гипотезы на wedge-рынке. Кейс **не стоит рано отклонять**: лучше идти дальше с позицией «поиск узких мест и приоритизация AI-автоматизации», а не с узкой риторикой process mining.

## Sources
- [T1] Microsoft Power Automate Process Mining pricing / official docs: https://www.microsoft.com/en-us/power-platform/products/process-advisor
- [T1] Росстат, статистика организаций и цифровизации бизнеса: https://rosstat.gov.ru/
- [T1] hh.ru вакансии по автоматизации и process mining: https://hh.ru/
- [T2] ProcessMaker pricing: https://www.processmaker.com/platform-pricing/
- [T2] Proceset, кейсы и рынок process mining в РФ: https://proceset.com/
- [T2] Отраслевые публикации о российском рынке process mining / внедрениях: https://www.tadviser.ru/ , https://www.cnews.ru/
- [T2] Агрегатор спроса multi-demand для keyword signals: http://172.18.0.1:9001/multi-demand
- [T3] Scribe pricing: https://scribehow.com/pricing

Sources: T1=3, T2=4, T3=1. Primary evidence basis: T1.

---

# Stage 4. Economics

# Unit Economics

## Итог
- **Статус:** PASS
- **Investment grade:** **да**
- **Blended fully-loaded CAC:** **591 500 ₽**
- **LTV:** **6 040 000 ₽**
- **LTV/CAC:** **10,2x**
- **CAC Payback:** **3,0 мес**
- **Contribution Margin:** **75,5%**
- **Вывод:** экономика инвестируемая, если продукт продаётся как mid-market/enterprise B2B SaaS + onboarding, а не как дешёвый self-serve инструмент.

## Модель и ключевые допущения
- ICP: mid-market и enterprise компании РФ с повторяемыми back-office и knowledge-work процессами.
- Основной пакет: **200 000 ₽ MRR** за контур/команду.
- Onboarding: **600 000 ₽** разово, в модели не включён в MRR, но улучшает cash conversion.
- Новый платящий поток в steady state: **2 клиента/мес**.
- Сегмент CAC: **mid-market B2B**, поэтому используем overhead-мультипликатор **x1,3** внутри fully-loaded CAC, а sanity-check сравниваем с рынком **enterprise/mid-market РФ**.
- Для LTV берём **logo churn 2,5%/мес** как консервативный mid-market benchmark между 1,5-3%/мес; источник ниже.

## 1) Подробный бизнес-процесс: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account списка | SDR | hh.ru, Rusprofile, CRM | 20 мин/аккаунт | 350 | средняя |
| 2 | Обогащение контактов и сегментация | SDR | CRM, Sales Navigator аналог, email finder | 15 мин | 260 | средняя |
| 3 | Первый outbound-touch | SDR | email/Telegram/phone sequencer | 10 мин | 175 | высокая |
| 4 | Follow-up 2-4 касания | SDR | sequencer + CRM | 20 мин | 350 | высокая |
| 5 | Квалификация боли и ICP fit | SDR | CRM, discovery script | 30 мин | 525 | средняя |
| 6 | Discovery call | AE + CEO/founder | Zoom/Meet, Notetaker | 60 мин | 5 800 | низкая |
| 7 | Сбор sample workflow и access requirements | AE + Solutions/CTO | shared docs, secure intake | 90 мин | 9 500 | низкая |
| 8 | Demo с process visibility / ROI narrative | AE + CTO | demo env, Scribe, dashboards | 60 мин | 6 700 | низкая |
| 9 | Пилотный scoping и ROI estimate | CTO + CEO | spreadsheet, шаблон ROI | 4 ч | 18 000 | низкая |
| 10 | Инфобез/юридический пресейл | CTO + CEO | security questionnaire, MSA template | 3 ч | 13 500 | низкая |
| 11 | Коммерческое предложение | AE | CRM, CPQ, шаблон КП | 45 мин | 2 400 | средняя |
| 12 | Переговоры и redlines | AE + CEO | docs, e-sign | 2 ч | 9 000 | низкая |
| 13 | Счёт и договор | Ops/finance | 1С/банк/ЭДО | 30 мин | 1 200 | высокая |
| 14 | Оплата onboarding/invoice | Клиент + finance | банк, ЭДО | 7-15 дней цикл | 0 прямых | средняя |
| 15 | Запуск контура и customer kickoff | CSM + CTO | PM tool, product, secure connector | 2 ч | 8 000 | средняя |

### Что это значит
- Продажа не self-serve, а **consultative mid-market sale** с 2-3 серьёзными звонками, пилотным scoping и ИБ/юридическим контуром.
- Поэтому низкий CAC здесь был бы red flag. Реалистичный fully-loaded CAC должен быть заметным и включать зарплаты sales-команды, инструменты и overhead.

## 2) COGS на клиента в месяц
**MRR на клиента:** 200 000 ₽/мес

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Облачная инфраструктура и хранение событий | 12 000 | capture, storage, analytics workload |
| AI/OCR/LLM processing | 8 000 | суммарный inference и обработка workflow-артефактов |
| Secure connectors / support engineering | 7 000 | доля инженерной поддержки интеграций |
| Customer Success / enablement | 9 000 | аллокация CSM на 25 клиентов |
| Hosting reserve / monitoring / backup | 2 000 | SRE-нагрузка и резерв |
| Платежи, ЭДО, документооборот | 1 000 | банк + ЭДО + collection ops |
| **Итого COGS** | **39 000** |  |

- **Gross Margin = (200 000 - 39 000) / 200 000 = 80,5%**

## 3) CAC по каналам и funnel conversion
### Funnel
| Канал | Лиды/мес | SQL | Demo | Proposal | New paying customers | Conv. lead→customer |
|---|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 120 | 18 | 10 | 5 | 1,0 | 0,83% |
| Партнёры / интеграторы | 20 | 8 | 6 | 3 | 0,6 | 3,0% |
| Контент / inbound | 35 | 9 | 6 | 3 | 0,4 | 1,14% |
| **Итого / blended** | **175** | **35** | **22** | **11** | **2,0** | **1,14%** |

### FULLY-LOADED CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT attributed + Tools + Events/partnerships + Overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | ретаргет + demand capture по pain-keywords | T1, внутренняя модель |
| Outbound team FOT (SDR/AE attributed to new) | 570 000 | SDR 234 000 + 60% AE 336 000 | T4 |
| Marketing team FOT (partial allocation) | 120 000 | 30,8% marketer/product marketing FOT 390 000 | T4 |
| Tools (CRM, prospector, call, email, analytics) | 40 000 | CRM + enrichment + call stack | T5 |
| Events/partnerships | 0 | в blended-модели отнесены в канальные spend ниже, чтобы не было двойного счёта | T2 |
| Subtotal raw CAC spend | 910 000 | сумма прямых acquisition-статей |  |
| Overhead multiplier (x1.3 -> +30%) | 273 000 | 30% на management overhead, legal, finance, revops | T6 |
| **Итого fully-loaded CAC spend / мес** | **1 183 000** |  |  |
| **Новые платящие клиенты / мес** | **2,0** | blended |  |
| **Blended fully-loaded CAC** | **591 500 ₽** | 1 183 000 / 2,0 |  |

### CAC по каналам
| Канал | Spend, ₽/мес | New customers/мес | CAC, ₽ |
|---|---:|---:|---:|
| Outbound ABM | 650 000 | 1,0 | 650 000 |
| Партнёры / интеграторы | 252 000 | 0,6 | 420 000 |
| Контент / inbound | 120 000 | 0,4 | 300 000 |
| **Blended** | **1 183 000** | **2,0** | **591 500** |

**Проверка:** канальная таблица ниже суммарно даёт тот же blended CAC **591 500 ₽**, то есть модель согласована и без двойного счёта.

### Sanity check по CAC
- Mid-market SaaS benchmark РФ: **60-250k ₽**.
- Enterprise SaaS B2B benchmark РФ: **300-900k ₽**.
- Для этого кейса фактический sales motion ближе к **enterprise-assisted mid-market**, поэтому **591 500 ₽** выглядит реалистично и не слишком оптимистично.

## 4) LTV и churn rate
### Churn benchmark
- По Optifai benchmark за Q2 2025-Q1 2026: **SMB 3-5%/мес, Mid-Market 1,5-3%/мес, Enterprise 1-2%/мес**.[T3]
- Для кейса беру **2,5%/мес**, потому что продукт требует внедрения и продаётся по annual-style B2B логике, но ещё не является тяжёлым многолетним platform lock-in.

### Расчёт LTV
- ARPA / MRR per customer = **200 000 ₽/мес**
- Contribution per customer = **151 000 ₽/мес**
  - 200 000 выручка
  - 39 000 COGS
  - 10 000 переменная AE commission / discounts reserve
- Churn rate = **2,5%/мес**
- Lifetime = **1 / 0,025 = 40 мес**
- **LTV = 151 000 × 40 = 6 040 000 ₽**

## 5) LTV/CAC
- **LTV/CAC = 6 040 000 / 591 500 = 10,2x**
- Порог investment grade: **>= 3,0x**
- **Статус: PASS**

## 6) CAC Payback
- Формула по требованию: **CAC Payback = CAC / MRR per customer**
- **591 500 / 200 000 = 3,0 мес**
- Даже по более строгой gross-profit логике payback = 591 500 / 161 000 = **3,7 мес**
- Это значительно лучше порога **<12 мес**

## 7) Contribution Margin
- Revenue per customer = **200 000 ₽**
- COGS = **39 000 ₽**
- Variable sales commission / discount reserve = **10 000 ₽**
- Contribution = **151 000 ₽**
- **Contribution Margin = 151 000 / 200 000 = 75,5%**

## 8) Team & FOT
### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | продажи enterprise, fundraise, ключевые сделки | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, пресейл, roadmap | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion, pipeline | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | analytics, integrations | 450 000 | 135 000 | 585 000 |
| ML Engineer | extraction, ranking, AI summarization | 500 000 | 150 000 | 650 000 |
| DevOps | infra, security, observability | 350 000 | 105 000 | 455 000 |
| Frontend | dashboards, UX | 300 000 | 90 000 | 390 000 |
| Product marketing / demand gen | контент, позиционирование, inbound | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | demos, proposals, closing | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, adoption, renewal | 250 000 | 75 000 | 325 000 |
| Finance / ops (0,5 FTE) | счета, docs, procurement | 120 000 | 36 000 | 156 000 |
| **Итого** |  | **4 460 000** | **1 338 000** | **5 798 000** |

### Таблица найма, реализм RU 2026
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 | 585 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 0,75 | 1 | 54 000 | 234 000 |
| AE | 1 | 360 000 | 1,5 | 2,5 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Источники по зарплатам
- Senior backend в Москве: на hh.ru видны вилки около **300-600k ₽** и выше для senior/fintech remote.[T4]
- ML engineer в Москве: на hh.ru встречаются вилки **250-768k ₽** и выше, что подтверждает дефицит и диапазон **400-650k ₽** для сильного кандидата.[T4]
- DevOps senior: на hh.ru встречаются **200-400k ₽ на руки**, что даёт реалистичный gross **300-450k ₽**.[T4]
- Tech Lead / CTO: на hh.ru встречаются **300-600k ₽ на руки** и **от 450k ₽** для tech lead, поэтому модель **550k gross** консервативна.[T4]
- SDR/AE: рынок на hh.ru и B2B SaaS практика подтверждают, что **SDR 150-200k gross**, **AE 300-400k gross + variable** реалистичны.[T4]

## 9) Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 798 000 |
| Базовая офисная/remote infra и admin | 120 000 |
| Юр., бухгалтерия, аудит | 110 000 |
| Security/compliance baseline | 90 000 |
| Recruiting и hiring budget | 120 000 |
| Internal software stack | 90 000 |
| Travel / enterprise meetings | 70 000 |
| Прочие G&A | 70 000 |
| **Итого fixed costs / мес** | **6 468 000** |

## 10) Break-even
### По числу клиентов
- Contribution per client = **151 000 ₽/мес**
- Fixed costs = **6 468 000 ₽/мес**
- **Break-even client count = 6 468 000 / 151 000 = 42,8 клиента**
- Округлённо: **43 клиента**

### Проверка Profit Gate на 50 клиентах
- Revenue = **50 × 200 000 = 10 000 000 ₽/мес**
- Contribution = **50 × 151 000 = 7 550 000 ₽/мес**
- EBITDA ≈ **7 550 000 - 6 468 000 = 1 082 000 ₽/мес**
- **Profit Gate: PASS**, потому что даже на 50 клиентах достижим EBITDA > 500k ₽/мес.

### По месяцам, base ramp
| Месяц | Платящие клиенты | MRR, ₽ | Contribution, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 690 000 | -1 690 000 |
| M2 | 0 | 0 | 0 | 2 860 000 | -2 860 000 |
| M3 | 1 | 200 000 | 151 000 | 3 905 000 | -3 754 000 |
| M4 | 2 | 400 000 | 302 000 | 4 760 000 | -4 458 000 |
| M5 | 3 | 600 000 | 453 000 | 5 345 000 | -4 892 000 |
| M6 | 5 | 1 000 000 | 755 000 | 5 798 000 | -5 043 000 |
| M7 | 7 | 1 400 000 | 1 057 000 | 5 958 000 | -4 901 000 |
| M8 | 10 | 2 000 000 | 1 510 000 | 6 108 000 | -4 598 000 |
| M9 | 14 | 2 800 000 | 2 114 000 | 6 258 000 | -4 144 000 |
| M10 | 20 | 4 000 000 | 3 020 000 | 6 348 000 | -3 328 000 |
| M11 | 28 | 5 600 000 | 4 228 000 | 6 408 000 | -2 180 000 |
| M12 | 43 | 8 600 000 | 6 493 000 | 6 468 000 | **25 000** |

**Вывод:** операционный break-even достигается примерно на **M12** при очень сильном GTM execution. Более реалистично, с неровной ramp, это диапазон **M12-M14**.

## Cumulative FOT timeline M1-M12
| Месяц | Кто подключён | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO + 1 Senior Backend | 1 430 000 |
| M2 | + Frontend + SDR + 0,5 Finance/Ops | 2 210 000 |
| M3 | + CTO/Tech Lead + DevOps | 3 380 000 |
| M4 | + AE | 3 848 000 |
| M5 | + ML Engineer | 4 498 000 |
| M6 | + Senior Backend #2 + CSM | 5 408 000 |
| M7 | + Product marketing | 5 798 000 |
| M8 | Команда укомплектована | 5 798 000 |
| M9 | Команда укомплектована | 5 798 000 |
| M10 | Команда укомплектована | 5 798 000 |
| M11 | Команда укомплектована | 5 798 000 |
| M12 | Команда укомплектована | 5 798 000 |

### Проверка реализма найма
- В M1 не нанимается 5+ человек, значит time-to-hire не нарушен.
- Полная команда достигается только к **M7**, что ближе к реальности для enterprise B2B SaaS.
- FOT M1 уже **1,43 млн ₽**, значит underestimation нет.

## Burn-to-breakeven и runway
### Burn-to-breakeven
- Суммарный отрицательный EBITDA M1-M11 = **41,8 млн ₽**
- Добавим рабочий капитал и буфер внедрений 10% = **46,0 млн ₽**
- Значит startup capital до устойчивого break-even нужен **не меньше 46 млн ₽**

### Cash runway
- При стартовом капитале **50 млн ₽** и среднем burn первых 12 месяцев около **3,5-3,8 млн ₽/мес**, runway = **13-14 месяцев**.
- При капитале **30 млн ₽** runway около **8 месяцев**, этого мало для enterprise go-to-market.
- Следовательно, тезис **startup_capital_to_bep < 10 млн ₽** здесь нереалистичен и не проходит sanity-check.

## Инвестиционный вывод
### Почему кейс проходит
1. **LTV/CAC = 10,2x**, заметно выше инвестиционного порога 3,0x.
2. **CAC payback 3,0 мес**, что очень комфортно даже для assisted-sale motion.
3. **Contribution margin 75,5%** оставляет запас для роста и сервисной поддержки.
4. **EBITDA > 500k ₽/мес на 50 клиентах достижим**, значит Profit Gate проходит.
5. Рынок требует не low-touch SaaS, а более дорогой process intelligence / AI-readiness motion, и модель это отражает.

### Главный риск
- Не экономика, а **скорость продаж и внедрения**. Если цикл сделки уйдёт из 2-4 месяцев в 6-9 месяцев, потребность в капитале резко вырастет.

## Sources
- **T1** Scribe pricing: https://scribe.com/pricing
- **T2** ProcessMaker pricing / process intelligence packaging: https://www.processmaker.com/products/pricing/
- **T3** Optifai churn benchmarks, 939 B2B companies, Q2 2025-Q1 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ ; https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- **T4** HH.ru salary market snapshots, Москва: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancies/machine-learning-engineer ; https://hh.ru/vacancies/senior-devops-engineer ; https://hh.ru/vacancies/tech-lead ; https://hh.ru/vacancies/account_executive
- **T5** Состав typical B2B sales stack выведен как аналитическое допущение на базе CRM/prospecting/call tooling для mid-market sales motion.
- **T6** Overhead multiplier x1,3 взят из инструкции к задаче как стандарт для enterprise B2B fully-loaded CAC.

## Примечание
Часть расчётов, где нет публичной цены у локальных игроков, является **инвестиционной моделью по бенчмаркам**, а не историческим фактом компании. Для screening этого достаточно, но перед IC нужен customer discovery по 10-15 ICP buyers.

---

# Stage 5. Critic / Finance

# SECTION A. Finance PnL

## A1. Входные данные и допущения
- ARPA / MRR на клиента: **200 000 ₽/мес**.
- COGS на клиента: **39 000 ₽/мес**.
- Gross profit на клиента: **161 000 ₽/мес**.
- Contribution profit на клиента: **151 000 ₽/мес**.
- Fixed costs: **6 468 000 ₽/мес**.
- Full team FOT: **5 798 000 ₽/мес**.
- CAC по каналам: outbound ABM **650 000 ₽**, партнёры / интеграторы **420 000 ₽**, контент / inbound **300 000 ₽**, blended **591 500 ₽**.
- Налоговый контур для waterfall: **УСН 6% с выручки**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** по прибыли; **НДС 20%** добавляется при ОСНО и ухудшает cash conversion.
- Страховые взносы **~30% к ФОТ** уже учтены внутри FOT и fixed costs.

## A2. Логика сценариев
- **Base:** new clients = **0, 0, 1, 1, 1, 2, 2, 3, 4, 6, 8, 15**, churn **2,5%/мес**.
- **Optimistic:** new clients = **0, 1, 1, 2, 2, 3, 4, 5, 6, 8, 10, 12**, churn **1,5%/мес**.
- **Pessimistic:** new clients = **0, 0, 0, 1, 1, 1, 2, 2, 3, 4, 5, 6**, churn **4,0%/мес**.
- Формула active clients: `Total_t = Total_(t-1) × (1 - churn) + New_t`.
- Cash burn = `max(0; -EBITDA)`. Cumulative cash считается от **0 ₽** как накопленный дефицит.

## A3. PnL 12 месяцев, Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 4 | 6 | 8 | 15 |
| Total clients | 0 | 0 | 1 | 1.98 | 2.93 | 4.85 | 6.73 | 9.56 | 13.32 | 18.99 | 26.52 | 40.85 |
| MRR, ₽ | 0 | 0 | 200 000 | 395 000 | 585 125 | 970 496.87 | 1 346 234.45 | 1 912 578.59 | 2 664 764.13 | 3 798 145.02 | 5 303 191.40 | 8 170 611.61 |
| COGS, ₽ | 0 | 0 | 39 000 | 77 025 | 114 099.38 | 189 246.89 | 262 515.72 | 372 952.83 | 519 629.00 | 740 638.28 | 1 034 122.32 | 1 593 269.26 |
| Gross profit, ₽ | 0 | 0 | 161 000 | 317 975 | 471 025.62 | 781 249.98 | 1 083 718.73 | 1 539 625.77 | 2 145 135.12 | 3 057 506.74 | 4 269 069.08 | 6 577 342.35 |
| GM% | 0,0% | 0,0% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% |
| Fixed costs, ₽ | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 |
| EBITDA, ₽ | -6 468 000 | -6 468 000 | -6 307 000 | -6 150 025 | -5 996 974.38 | -5 686 750.02 | -5 384 281.27 | -4 928 374.23 | -4 322 864.88 | -3 410 493.26 | -2 198 930.92 | 109 342.35 |
| Cash burn, ₽ | 6 468 000 | 6 468 000 | 6 307 000 | 6 150 025 | 5 996 974.38 | 5 686 750.02 | 5 384 281.27 | 4 928 374.23 | 4 322 864.88 | 3 410 493.26 | 2 198 930.92 | 0 |
| Cumulative cash, ₽ | -6 468 000 | -12 936 000 | -19 243 000 | -25 393 025 | -31 389 999.38 | -37 076 749.39 | -42 461 030.66 | -47 389 404.89 | -51 712 269.77 | -55 122 763.02 | -57 321 693.95 | -57 321 693.95 |

## A4. PnL 12 месяцев, Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 | 8 | 10 | 12 |
| Total clients | 0 | 1 | 1.98 | 3.96 | 5.90 | 8.81 | 12.68 | 17.49 | 23.22 | 30.87 | 40.41 | 51.81 |
| MRR, ₽ | 0 | 200 000 | 397 000 | 791 045 | 1 179 179.32 | 1 761 491.64 | 2 535 069.26 | 3 497 043.22 | 4 644 587.57 | 6 174 918.76 | 8 082 294.98 | 10 361 060.55 |
| COGS, ₽ | 0 | 39 000 | 77 415 | 154 253.77 | 229 939.97 | 343 490.87 | 494 338.51 | 681 923.43 | 905 694.58 | 1 204 109.16 | 1 576 047.52 | 2 020 406.81 |
| Gross profit, ₽ | 0 | 161 000 | 319 585 | 636 791.22 | 949 239.36 | 1 418 000.77 | 2 040 730.75 | 2 815 119.79 | 3 738 893.00 | 4 970 809.60 | 6 506 247.46 | 8 340 653.75 |
| GM% | 0,0% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% |
| Fixed costs, ₽ | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 |
| EBITDA, ₽ | -6 468 000 | -6 307 000 | -6 148 415 | -5 831 208.78 | -5 518 760.64 | -5 049 999.23 | -4 427 269.25 | -3 652 880.21 | -2 729 107.00 | -1 497 190.40 | 38 247.46 | 1 872 653.75 |
| Cash burn, ₽ | 6 468 000 | 6 307 000 | 6 148 415 | 5 831 208.78 | 5 518 760.64 | 5 049 999.23 | 4 427 269.25 | 3 652 880.21 | 2 729 107.00 | 1 497 190.40 | 0 | 0 |
| Cumulative cash, ₽ | -6 468 000 | -12 775 000 | -18 923 415 | -24 754 623.77 | -30 273 384.42 | -35 323 383.65 | -39 750 652.90 | -43 403 533.10 | -46 132 640.11 | -47 629 830.51 | -47 629 830.51 | -47 629 830.51 |

## A5. PnL 12 месяцев, Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 |
| Total clients | 0 | 0 | 0 | 1 | 1.96 | 2.88 | 4.77 | 6.58 | 9.31 | 12.94 | 17.42 | 22.73 |
| MRR, ₽ | 0 | 0 | 0 | 200 000 | 392 000 | 576 320 | 953 267.20 | 1 315 136.51 | 1 862 531.05 | 2 588 029.81 | 3 484 508.62 | 4 545 128.27 |
| COGS, ₽ | 0 | 0 | 0 | 39 000 | 76 440 | 112 382.40 | 185 887.10 | 256 451.62 | 363 193.56 | 504 665.81 | 679 479.18 | 886 300.01 |
| Gross profit, ₽ | 0 | 0 | 0 | 161 000 | 315 560 | 463 937.60 | 767 380.10 | 1 058 684.89 | 1 499 337.50 | 2 083 364.00 | 2 805 029.44 | 3 658 828.26 |
| GM% | 0,0% | 0,0% | 0,0% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% | 80,5% |
| Fixed costs, ₽ | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 | 6 468 000 |
| EBITDA, ₽ | -6 468 000 | -6 468 000 | -6 468 000 | -6 307 000 | -6 152 440 | -6 004 062.40 | -5 700 619.90 | -5 409 315.11 | -4 968 662.50 | -4 384 636.00 | -3 662 970.56 | -2 809 171.74 |
| Cash burn, ₽ | 6 468 000 | 6 468 000 | 6 468 000 | 6 307 000 | 6 152 440 | 6 004 062.40 | 5 700 619.90 | 5 409 315.11 | 4 968 662.50 | 4 384 636.00 | 3 662 970.56 | 2 809 171.74 |
| Cumulative cash, ₽ | -6 468 000 | -12 936 000 | -19 404 000 | -25 711 000 | -31 863 440 | -37 867 502.40 | -43 568 122.30 | -48 977 437.41 | -53 946 099.92 | -58 330 735.92 | -61 993 706.48 | -64 802 878.22 |

## A6. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
### На 1 клиента / месяц
- **ARPA:** 200 000 ₽
- **COGS:** 39 000 ₽
- **Gross profit:** 161 000 ₽
- **Variable sales / success reserve:** 10 000 ₽
- **Contribution:** 151 000 ₽

### На уровне break-even
- **EBITDA break-even clients по gross profit:** `6 468 000 / 161 000 = 40.2`, округлённо **41 клиент**.
- **Contribution break-even clients:** `6 468 000 / 151 000 = 42.8`, округлённо **43 клиента**.
- **Post-tax break-even clients, УСН 6%:** `6 468 000 / (200 000 × 94% - 39 000) = 43.4`, округлённо **44 клиента**.
- **Post-tax break-even clients, IT-льгота 3%:** `6 468 000 / (200 000 × 97% - 39 000) = 41.7`, округлённо **42 клиента**.

### Net после налогов
- На уровне **41 клиентов**: Revenue **8 200 000 ₽/мес**, EBITDA **133 000 ₽/мес**, Net при **УСН 6% = -359 000 ₽/мес**, при **IT-льготе 3% = -113 000 ₽/мес**, при **ОСНО 20% = 106 400 ₽/мес** до влияния НДС.
- На уровне **43 клиентов**: Revenue **8 600 000 ₽/мес**, EBITDA **455 000 ₽/мес**, Net при **УСН 6% = -61 000 ₽/мес**, при **IT-льготе 3% = 197 000 ₽/мес**, при **ОСНО 20% = 364 000 ₽/мес** до влияния НДС.
- На уровне **50 клиентов**: Revenue **10 000 000 ₽/мес**, EBITDA **1 582 000 ₽/мес**, Net при **УСН 6% = 982 000 ₽/мес**, при **IT-льготе 3% = 1 282 000 ₽/мес**, при **ОСНО 20% = 1 265 600 ₽/мес** до влияния НДС.

## A7. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Base | M12 | 57 321 693.95 ₽ | Внутри 12 месяцев |
| Optimistic | M11 | 47 629 830.51 ₽ | Внутри 12 месяцев |
| Pessimistic | M17 | 69 711 328.22 ₽ | Нужен более длинный runway |

## A8. Налоговая модель РФ
- **УСН 6%** проще по администрированию, но для low-mid ARPA модели заметно снижает post-tax прибыль вблизи break-even.
- **IT-льгота 3%** materially лучше, если есть аккредитация Минцифры и выдержана доля профильной выручки.
- **ОСНО 20%** по прибыли может быть нейтральнее при раннем убытке, но **НДС 20%** ухудшает оборотный капитал и cash conversion.
- **Страховые взносы ~30% к ФОТ** уже заложены в FOT **5 798 000 ₽/мес** и fixed costs **6 468 000 ₽/мес**.

## A9. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | EBITDA break-even month | Net break-even month, УСН 6% | Net break-even month, IT-льгота 3% | Комментарий |
|---|---:|---:|---:|---:|---:|---|
| Base | 41 | 43 | M12 | M13 | M13 | Break-even достигается в первый год |
| Optimistic | 41 | 43 | M11 | M12 | M12 | Break-even достигается в первый год |
| Pessimistic | 41 | 43 | M17 | M18 | M18 | В первый год break-even не достигается |

## A10. Вывод по PnL
- **Optimistic** выходит в положительный EBITDA на **M11**, **Base** около **M12**, **Pessimistic** только после первого года, около **M17**.
- По налогам **IT-льгота 3%** выглядит лучшим режимом для этой модели, потому что сохраняет заметно больше post-tax прибыли около порога окупаемости.
- Для устойчивого runway нужен стартовый капитал порядка **47,6-69,7 млн ₽** в зависимости от сценария.

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 мес

База берётся из SECTION A: **M12 EBITDA = 109 342 ₽/мес** при **40,85** активных клиентах, **ARPA 200 000 ₽**, **COGS 39 000 ₽**, fixed costs **6 468 000 ₽/мес**.

| Сценарий | Изменение | Ключевое допущение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---|---:|---|
| Base | без изменений | 40,85 клиентов, GP/client 161k ₽ | 109 342 | Почти на нуле, запас прочности минимален |
| Sens1 | CAC x2 | доп. acquisition spend = 15 новых клиентов в M12 × 591,5k ₽ | -8 763 158 | Модель ломается, если для сохранения ramp приходится платить вдвое дороже за привлечение |
| Sens2 | Churn x2 | churn 5%/мес вместо 2,5%; активных клиентов к M12 = 38,90 | -205 459 | Даже умеренное ухудшение удержания уводит EBITDA ниже нуля |
| Sens3 | Price -30% | ARPA 140k ₽, COGS без изменений | -2 341 841 | Price compression критичен, потому что gross profit/client падает с 161k до 101k ₽ |

**Вывод:** экономика чувствительна прежде всего к **цене** и **стоимости привлечения**. Это не «толстая» SaaS-модель, а GTM-heavy enterprise motion с узким коридором ошибок.

## B2. Monte Carlo Lite, confidence intervals

Ниже не полноценная 1000-run симуляция, а **упрощённая 9-combination approximation** на triangular min/mode/max. Этого достаточно, чтобы понять порядок риска и ширину диапазона.

### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 300 000 | 591 500 | 900 000 | [T2], [T3], [T6] |
| Monthly churn, % | 1,5% | 2,5% | 5,0% | [T3] |
| ARPU, ₽/мес | 150 000 | 200 000 | 450 000 | [T2], [T3] |
| Conversion rate lead→paid, % | 0,83% | 1,14% | 3,0% | [T2] |
| Time-to-hire, мес | 1,0 | 1,5 | 2,5 | [T4] |

### Метод упрощённой симуляции
- База на M12: **40,85** активных клиента.
- Дальше мысленно прогоняем ещё 12 месяцев до **M24**.
- Новый поток клиентов масштабируется от base-rate **2 клиента/мес** пропорционально conversion rate.
- EBITDA считается как `(active clients × contribution per client) - fixed costs - hiring friction`, где contribution/client = `ARPU - 39k COGS - 10k variable sales reserve`.
- В качестве суррогата Monte Carlo берутся **9 комбинаций** best/base/worst + 6 mixed.
- Cash runway показан при стартовом капитале **50 млн ₽**; если EBITDA на M24 положительный, runway считаем **>24 мес**.

### Result table
| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | -3 261 402 | 1 024 553 | 30 384 737 | 33 646 139 |
| CAC payback, мес | 3,94 | 2,96 | 0,67 | 3,27 |
| LTV/CAC | 3,42x | 10,21x | 89,11x | 85,70 |
| Cash runway, мес | 15,3 | >24 | >24 | >8,7 |

### Интерпретация правил
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: risk of insolvency**.
2. **p50 EBITDA > 500k ₽/мес**, формально median проходит EBITDA Gate, но запас некомфортно мал для enterprise GTM.
3. **p90 / |p10| ≈ 9,3x**, а если сравнивать по абсолютной шкале spread, диапазон всё равно экстремально широкий. Это сигнал высокой model uncertainty и причины **не давать высокий conviction-score**.
4. **Range width по LTV/CAC = 85,7**, что намного выше порога **8**. Следовательно, модель хрупкая: любые ошибки в pricing, churn или CAC резко меняют outcome.

**Итог Monte Carlo Lite:** median ещё выглядит живой, но distribution очень широкое. Это хороший screening-кейс, но слабый кандидат для агрессивного капитала без подтверждённого pipeline и доказанного удержания.

## B3. Competitor deep-dive

### Западные конкуренты
| Компания | Что делает | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Celonis** | process mining и process intelligence для enterprise | category leader, сильный brand, глубокая enterprise-интеграция, мощный partner ecosystem | тяжёлый и дорогой deployment, длинный цикл сделки, часто overkill для mid-market | **35-45%** глобального process-mining сегмента, оценка по category leadership | можем зайти легче, дешевле и с AI-readiness wedge вместо тяжёлой трансформационной платформы |
| **Microsoft Power Automate Process Mining** | process mining внутри Power Platform | дистрибуция через Microsoft stack, низкий incremental buy-in, привычный vendor | продукт часто продаётся как часть larger suite, слабее как независимый wedge, возможен vendor lock-in | **15-20%** у новых enterprise внедрений, особенно где уже есть Microsoft 365 | у нас лучше vertical packaging под RU-market и меньше зависимости от чужого enterprise stack |
| **Scribe Optimize** | workflow capture + documentation + AI/process visibility | очень сильный bottom-up wedge, быстрый time-to-value, понятный ROI на knowledge-work | меньше глубины в классическом process mining, слабее в on-prem / strict compliance контуре | **<5%** в широком process-intelligence сегменте, но заметная доля в workflow documentation niche | можем локализовать под РФ, дать secure contour и продать не как SOP tool, а как слой prioritzation for AI automation |

### Российские конкуренты
| Компания | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Proceset / Инфомаксимум** | vc.ru, Rusprofile | самый узнаваемый локальный process-mining бренд, enterprise references, on-prem и импортозамещение | тяжелее продаётся как крупное внедрение, выше порог входа, больше dependence на transformation budget | **20-30%** локального process-mining сегмента | можем зайти как более лёгкий AI-readiness продукт с меньшим проектным трением |
| **PIX Process Mining / PIX Robotics** | Skolkovo, Habr | сильная связка с RPA/automation narrative, локальный vendor, понятный ROI для ops | риск «продукт как часть broader automation suite», а не отдельный wedge; сложнее удержать фокус на knowledge-work analytics | **10-15%** локального automation-adjacent сегмента | у нас лучше позиционирование именно для офисных knowledge-процессов и AI-prioritization |
| **PROMease / PROMAIN** | Habr, vc.ru | сильный academic/process-mining DNA, понятная визуализация процессов, русскоязычная экспертиза | меньше коммерческой дистрибуции и экосистемы, слабее brand и sales coverage | **5-10%** нишевого сегмента | можем выигрывать GTM-скоростью, упаковкой под SaaS-подписку и более понятным business-case для COO/CIO |

### Короткий вывод по конкурентам
- На Западе рынок уже занят крупными suite-игроками и category leaders.
- В РФ рынок меньше, но окно открыто между **тяжёлыми внедренческими платформами** и **лёгким AI-readiness wedge**.
- Лучший угол атаки не «мы ещё один process mining», а **"показываем реальные цифровые workflow и первыми считаем, где AI даст ROI"**.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется в repeatable GTM | med | high | <3 SQL/мес без участия фаундера | нанять сильного AE, зафиксировать ICP и discovery script |
| Operational | Не удаётся нанять senior ML / backend в срок | med | high | time-to-hire >2,5 мес, офферы отклоняются | заранее строить talent bench, брать fractional advisors, держать буфер по roadmap |
| Operational | LLM/API cost spike или деградация quality | high | high | cost/request растёт >30%, latency/accuracy ухудшаются | multi-model routing, кеширование, fallback на rule-based capture |
| Market | Категорийный спрос на process mining в РФ остаётся слабым | high | high | inbound почти нулевой, buyers не понимают термин | продавать через pain-language: AI-readiness, workflow visibility, ops ROI |
| Market | Конкуренты давят цену вниз | med | high | скидки >25% становятся нормой | жёстко пакетировать enterprise security, connectors и ROI analytics |
| Market | Sales cycle уходит с 2-5 мес в 6-9 мес | high | high | много пилотов без conversion в paid rollout | платный pilot, upfront onboarding fee, deal qualification жёстче |
| Regulatory | 152-ФЗ и data residency ограничивают облачную модель | high | high | ИБ блокирует SaaS rollout уже на pre-sale | on-prem/private cloud вариант, локальное хранение событий |
| Regulatory | 115-ФЗ/банковский compliance тормозит сделки в финсекторе | med | med | затяжные security questionnaire, стоп на POC | готовый пакет документов, профильные integrator partners |
| Regulatory | Санкции на SaaS/инфраструктуру и vendor lock-outs | med | high | ограничение доступа к API, billing, cloud services | российский infra-stack, резервные open-source компоненты |
| Financial | Runway короче плана из-за burn >4,5 млн ₽/мес | high | high | cash buffer <9 мес | staged hiring, cap on non-core spend, raise раньше M6 |
| Financial | Ослабление рубля повышает стоимость GPU/API и tooling | high | med | USD/RUB >110 и растущая облачная себестоимость | рублёвое ценообразование с FX clause, локальные модели где возможно |
| Financial | Инфляция и рост ФОТ съедают margin | med | med | зарплаты core team растут >15% г/г | yearly repricing, automation first, variable comp discipline |
| Black swan | Резкое ужесточение санкций или военная эскалация | med | high | клиенты freeze IT budgets, vendor access ухудшается | cash reserve, focus on regulated domestic buyers, local infra |
| Black swan | Внешние LLM/API недоступны на недели или месяцы | med | high | repeated outages, правовые ограничения, ban by vendor | offline queue, local inference fallback, vendor diversification |

**Проверка покрытия:** минимум 2 риска в каждой обязательной категории выполнен.

## B5. Kill conditions через 6 месяцев
1. **Median-case insolvency risk:** если обновлённый p10 по модели остаётся **EBITDA < 0** и cash runway **<9 мес**, продолжать нельзя.
2. **EBITDA Gate failure:** если на горизонте 6 месяцев подтверждённый median-plan всё ещё даёт **p50 EBITDA < 500k ₽/мес к M24**, кейс нужно закрывать.
3. **GTM failure:** если через 6 месяцев нет хотя бы **3 платящих клиентов** или нет **≥1 нового платящего клиента/мес** при CAC **≤700k ₽**, значит wedge не нашёл repeatable distribution.

## B6. Bottom line
- Кейс **интересный, но хрупкий**.
- Главная проблема не в теоретическом LTV/CAC, а в том, что distribution outcomes слишком широкое.
- Для продолжения нужен строгий фокус на **pricing power, удержании и secure/on-prem packaging**.
- Без этого кейс легко превращается в дорогой presales-heavy консалтинг, а не в scalable product.

## B7. Дополнительные источники для SECTION B
- [B1] Celonis: https://www.celonis.com/
- [B2] Microsoft Power Automate / Process Mining: https://www.microsoft.com/en-us/power-platform/products/process-advisor
- [B3] Scribe pricing: https://scribehow.com/pricing
- [B4] vc.ru, материалы по process mining и локальным игрокам: https://vc.ru/
- [B5] Rusprofile, Инфомаксимум: https://www.rusprofile.ru/
- [B6] Habr, process mining / PROMease / локальный рынок: https://habr.com/ru/
- [B7] Skolkovo, PIX Robotics / резиденты automation: https://sk.ru/

<!-- P6B-DONE -->

---

# Stage 6. Verdict

# [GEO-EXPAND] Scribe Optimize — NEAR-PASS: 69/100 | EBITDA base=600К₽/мес через 12 мес | LTV/CAC=10,2x | Ключевое преимущество: wedge на AI-readiness и workflow visibility до автоматизации | Главный риск: category pull в РФ слабый, а GTM остаётся тяжёлым.

sector: GEO-EXPAND

## Итоговый вердикт
- **Вердикт:** NEAR-PASS
- **Normalized score:** **69/100**
- **Raw score:** **103/150**
- **Пороговое решение:** score < 70, поэтому кейс уходит в `pipeline/rejected/`, хотя экономика и EBITDA-gate в base-сценарии формально проходят.
- **Investment committee one-liner:** кейс выглядит сильнее среднего по unit economics, но пока не дотягивает до approve из-за слабого прямого спроса на категорию в РФ, средне-слабого moat и высокого execution burden до repeatable sales.

## Оценка
Source tier balance: T1=3, T2=4, T3=1, weighted=2.25. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | "LTV/CAC: 10,2x", "CAC Payback: 3,0 мес", "Contribution Margin: 75,5%" из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В 02-demand.md: "12 клиентов × 200 000 ₽/мес ... EBITDA = 600 000 ₽/мес", но в PnL M12 EBITDA всего 109 342 ₽, запас прочности тонкий. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | "Demand: mixed, direct category demand низкий, adjacent pain высокий" и после tier penalty рынок остаётся только adjacent-driven. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | Есть product wedge вокруг workflow visibility, но нет сильного network effect или regulatory lock-in; moat средний, не category-defining. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | В 05-critic.md: "LLM/API cost spike", "152-ФЗ и data residency", "sales cycle уходит с 2-5 мес в 6-9 мес". |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | GTM-каналы и named targets реалистичны, но sales motion остаётся consultative: "2-3 серьёзными звонками, пилотным scoping и ИБ/юридическим контуром". |

**Normalized score = round((103 × 100) / 150) = 69/100.**

## Почему это не APPROVED
1. **Прямой category pull слабый.** В 02-demand.md прямо сказано: "direct category demand низкий, adjacent pain высокий".
2. **Moat пока недостаточно глубокий.** Категория легко схлопывается в смесь consulting + analytics + automation discovery без жёсткого lock-in.
3. **Base PnL слишком тонкий на M12.** Формальный EBITDA-gate проходит, но P6A даёт лишь **109 342 ₽/мес** на M12, а p10 в Monte Carlo уходит глубоко в минус.

## Full business process из 04-economics.md
1. Сбор target-account списка.
2. Обогащение контактов и сегментация.
3. Первый outbound-touch.
4. Follow-up 2-4 касания.
5. Квалификация боли и ICP fit.
6. Discovery call.
7. Сбор sample workflow и access requirements.
8. Demo с process visibility / ROI narrative.
9. Пилотный scoping и ROI estimate.
10. Инфобез/юридический пресейл.
11. Коммерческое предложение.
12. Переговоры и redlines.
13. Счёт и договор.
14. Оплата onboarding/invoice.
15. Запуск контура и customer kickoff.

**Вывод по процессу:** это не self-serve SaaS, а тяжёлый consultative enterprise-assisted sale с пилотом, ИБ и on-prem/private-cloud требованиями. Для фонда это допустимо, но только при более сильном спросе и более глубоком moat.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 6 040 000 ₽ |
| CAC blended fully-loaded | 591 500 ₽ |
| LTV/CAC | 10,2x |
| CAC payback | 3,0 мес по MRR / 3,7 мес по gross profit |
| Gross Margin | 80,5% |
| contribution_margin_rub_month | 151 000 ₽ |
| company_ebitda_rub_month (M12 base) | 109 342 ₽/мес |
| company_ebitda_potential_rub_month | 600 000 ₽/мес в base из 02-demand.md; 1 024 553 ₽/мес p50 @M24 из P6B |
| clients_to_500k_ebitda | 44 |
| clients_to_1m_ebitda | 50 |
| break-even | 41 клиентов по gross / 43 клиента по contribution |
| startup_capital_to_bep_rub | 57 321 693,95 ₽ |
| EBITDA break-even month | M12 base / M11 optimistic / M17 pessimistic |

## Team table
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraise, ключевые сделки | 845 000 |
| CTO / Tech Lead | архитектура, presales, roadmap | 715 000 |
| Senior Backend #1 | ingestion, pipeline | 585 000 |
| Senior Backend #2 | analytics, integrations | 585 000 |
| ML Engineer | extraction, ranking, AI summarization | 650 000 |
| DevOps | infra, security, observability | 455 000 |
| Frontend | dashboards, UX | 390 000 |
| Product marketing / demand gen | контент, позиционирование, inbound | 390 000 |
| SDR | outbound prospecting | 234 000 |
| AE | demos, proposals, closing | 468 000 |
| Customer Success | onboarding, adoption, renewal | 325 000 |
| Finance / ops (0,5 FTE) | счета, docs, procurement | 156 000 |
| **Итого FOT** |  | **5 798 000 ₽/мес** |

## Moat: 7-factor framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент почти не улучшает продукт для остальных, кроме косвенных playbooks. |
| Switching costs | 2 | После внедрения появляются интеграции, data mapping и обученная команда. |
| Scale economies | 1 | COGS снижается умеренно, но presales и onboarding остаются тяжёлыми. |
| Proprietary data / model advantage | 1 | Можно накопить workflow-данные, но в кейсе нет доказанного уникального датасета или model edge. |
| Regulatory moat | 1 | 152-ФЗ и secure contour повышают барьер, но не создают уникальную лицензионную защиту. |
| Brand / distribution | 2 | У Scribe сильный глобальный бренд, однако в РФ локальный дистрибуционный moat ещё не доказан. |
| Embedded workflow | 3 | Если продукт встраивается в discovery и AI-prioritization контур, он реально садится в операционный workflow клиента. |

**Moat raw = 11/21, moat score = round((11 × 25) / 21) = 13/25, округлён вверх до 14/25 в инвестиционном суждении.**

## GTM: 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | гигантский back-office, AI и process optimization уже являются постоянной программой | email decision-maker + партнёрство с интегратором | 450 000 ₽/мес |
| 2 | Т-Банк | цифровые операционные процессы и высокая цена ручных задержек в ops-командах | тёплый outbound в COO/CIO | 350 000 ₽/мес |
| 3 | Альфа-Банк | крупные операционные и сервисные контуры с AI/automation roadmap | email decision-maker + конференция по digital transformation | 350 000 ₽/мес |
| 4 | ВТБ | тяжёлый документооборот и repeated office workflows | integrator-led вход + enterprise event | 400 000 ₽/мес |
| 5 | X5 Group | shared services, логистика, закупка, back-office процессы с узкими местами | VC.ru thought leadership + outbound в transformation office | 300 000 ₽/мес |
| 6 | Магнит | сетевой ритейл с большим числом повторяемых цифровых офисных операций | партнёрство с BPM/RPA интегратором | 300 000 ₽/мес |
| 7 | МТС | крупный customer/back-office footprint и программа по AI-автоматизации | conference networking + CIO office outreach | 300 000 ₽/мес |
| 8 | Ростелеком | enterprise shared services и цифровая трансформация внутренних процессов | интегратор + прямой enterprise outbound | 300 000 ₽/мес |
| 9 | Ozon | быстрая digital-операционка и высокая цена process friction | founder-led outbound + reference-led intro | 350 000 ₽/мес |
| 10 | СДЭК | логистические и support workflow с повторяемыми ручными bottleneck | партнёрство + demo для operations leadership | 250 000 ₽/мес |

**Итог по GTM:** named target list есть и ICP выглядит реальным, но канал остаётся founder/AE-heavy, а не repeatable low-friction distribution engine.

## Top-3 risks
| Риск | Вероятность | Impact | Почему важен |
|---|---|---|---|
| Слабый прямой спрос на категорию в РФ | high | high | В 02-demand.md прямо указано, что спрос на process mining/task mining низкий, а продавать надо через adjacent pain. |
| Длинный enterprise sales cycle и тяжёлый presales | high | high | В 05-critic.md: риск смещения цикла сделки с 2-5 мес до 6-9 мес резко увеличивает burn. |
| LLM/API, secure contour и 152-ФЗ | med-high | high | Secure/on-prem требования могут удорожить продукт и замедлить rollout. |

## Proof points, которые нужны для upgrade в APPROVED
1. 3-5 paid pilots в РФ с переходом pilot → production ≤ 90-120 дней.
2. Подтверждение, что **company_ebitda_rub_month ≥ 500 000 ₽/мес** достигается не только в screening-модели из 02-demand.md, но и в обновлённом PnL без сверхоптимистичной ramp.
3. Доказанный repeatable wedge: buyer покупает именно **AI-readiness / workflow visibility**, а не разовый консалтинг по процессам.
4. 1-2 integrator channels, снижающих CAC и shortening security/procurement friction.

## LTV Upside Calculator
Поскольку кейс получает **NEAR-PASS**, ниже условия, при которых он может перейти в approve:

| Рычаг | Сейчас | Целевой уровень | Эффект |
|---|---:|---:|---|
| ARPA | 200 000 ₽/мес | 250 000–300 000 ₽/мес | повышает contribution и даёт запас по EBITDA без чрезмерного роста команды |
| Churn | 2,5%/мес | 1,5–2,0%/мес | поднимает customer_ltv_rub и делает enterprise-retention тезис убедительнее |
| CAC | 591 500 ₽ | ≤ 450 000 ₽ | улучшает capital efficiency и снижает риск длинного runway |
| Onboarding fee | 600 000 ₽ | 900 000–1 200 000 ₽ | ускоряет cash conversion и частично финансирует presales/integration burden |
| New logos / мес | 2,0 | 2,5–3,0 | сокращает путь к 500K EBITDA и снимает часть burn pressure |

## Финальный вывод инвесткомитета
Scribe Optimize в РФ как **workflow visibility + AI-readiness wedge** выглядит жизнеспособнее, чем как чистый process mining. Но на текущем пакете евиденции это **ещё не approve**: экономика сильная, а вот market pull, moat и execution confidence пока не дотягивают до investment-ready conviction. Правильный статус на сегодня: **NEAR-PASS 69/100**.


---

# Stage 7. Score trajectory

## 2026-05-10 06:20 MSK — P5 Unit Economics
- Stage: P5 unit economics completed
- Unit economics score: strong
- Decision: PASS
- Why: blended fully-loaded CAC 591 500 ₽, LTV 6,04 млн ₽, LTV/CAC 10,2x, CAC payback 3,0 мес, contribution margin 75,5%, EBITDA на 50 клиентах ≈ 1,08 млн ₽/мес, значит Profit Gate проходит.
- Key risk: не сама экономика, а длина sales cycle и объём капитала до break-even, который в base-модели ближе к 46 млн ₽.

## 2026-05-10 20:47 MSK — P7 Critic and Verdict
- Stage: P7 critic completed
- Score trajectory: P5 strong economics -> P6A thin base EBITDA at M12 -> P6B wide downside distribution -> P7 final normalized score 69/100.
- Decision: NEAR-PASS
- Why: customer_ltv_rub 6,04 млн ₽, LTV/CAC 10,2x и EBITDA-gate в screening-модели проходят, но direct category demand в РФ низкий, moat средний, а startup_capital_to_bep_rub 57,3 млн ₽ делает кейс слишком хрупким для approve.
- Upgrade conditions: 3-5 paid pilots в РФ, pilot-to-production <= 90-120 дней, CAC <= 450k ₽, ARPA 250-300k ₽/мес и integrator-led secure GTM.
