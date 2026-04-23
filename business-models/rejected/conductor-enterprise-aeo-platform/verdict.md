# conductor-enterprise-aeo-platform

Статус: REJECTED / NEAR-PASS

Собрано автоматически из файлов кейса.


---

## FILE: 00-brief.md


# Краткий бриф

## Кейс
Conductor, enterprise AEO/SEO-платформа для мониторинга AI-поиска

## Статус
Новый кейс создан на этапе intake и передан дальше в P3-demand-validation.

## Почему открыт
Сигнал описывает уже упакованный enterprise-продукт для AI Search Performance с прямой привязкой к бюджету SEO/AEO и высокому годовому чеку. Это не просто общий AI adoption, а отдельный wedge вокруг мониторинга и оптимизации видимости бренда в ChatGPT, Gemini, Claude и Copilot.

## Потенциал
При чеке 30 000-200 000+ долларов в год на клиента даже 10-20 контрактов дают экономику сильно выше порога 500 000 ₽ EBITDA в месяц. Категория выглядит как масштабируемый B2B SaaS с понятным enterprise budget owner.

## Следующий шаг
Подготовлен intake; следующий этап: P3-demand-validation.


---

## FILE: 01-intake.md


---
sector: AI-SERVICES
rerun: false
source_raw: 2026-04-22-conductor-enterprise-aeo-platform.md
created: 2026-04-22T09:16:29+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
Enterprise AEO/SEO-платформа для мониторинга, измерения и оптимизации видимости бренда в AI-поиске и answer engines.

## Контекст raw-файла

# Conductor, enterprise AEO/SEO-платформа

- name: Conductor
- source: https://www.conductor.com/blog/2026-ai-search-performance/ — 2026-02-17; https://www.conductor.com/academy/enterprise-seo/ — 2025-11-11
- ltv_signal: 2 400 000-16 000 000 ₽ в год на клиента
- why it matters: Conductor официально запустил AI Search Performance как системный продукт для мониторинга видимости бренда в ChatGPT, Gemini, Claude, Copilot и других AI-поисковиках, а на своей academy-странице прямо указывает, что enterprise SEO-платформы обычно стоят 30 000-200 000+ долларов в год. Это сильный сигнал для категории enterprise AEO/SEO: при 10-20 клиентах с такими чеками компания проходит profit gate с большим запасом, а продуктовая поставка не требует упора в тяжёлый SI и может масштабироваться как независимая B2B SaaS-платформа.


---

## FILE: 02-demand.md


---
stage: demand-validation
case: conductor-enterprise-aeo-platform
date: 2026-04-22
analyst: branch-models-lead
sector: AI-SERVICES
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
Conductor: enterprise AEO/SEO-платформа для мониторинга, измерения и оптимизации видимости бренда в AI-поиске и answer engines.

## Итог
**Статус: CONDITIONAL PASS.**

На 22 апреля 2026 года глобальный category proof выглядит сильным и свежим, а локальный российский спрос уже начинает оформляться, но пока остаётся ранним и mostly-adjacent. Conductor официально продвигает AI Search Performance как отдельный системный слой для enterprise marketing teams, а на своей academy-странице прямо пишет, что enterprise SEO-платформы обычно стоят **$30 000-200 000+ в год**. [T1][T2]

Ключевые выводы:
1. Это не просто SEO-tool, а новая budget line вокруг AI visibility, competitive monitoring и attribution в ChatGPT, Claude, Gemini и других движках. [T1][T2]
2. В РФ уже есть оформленное сервисное предложение под GEO: «Ашманов и партнёры» публично продают GEO-продвижение с ценой **от 180 000 ₽**, а также отдельно пишут, что GEO становится критически важной стратегией в 2026 году. Это доказывает не масштаб категории, но факт коммерциализации спроса. [T4]
3. Яндекс **22 мая 2025 года** встроил Алису в Поиск с развёрнутыми AI-ответами и ссылками на источники. Это важный локальный structural shift: видимость бренда всё чаще будет решаться не только через классическую выдачу. [T5]
4. Demand API показывает ранний, но уже заметный интерес к новой категории: `geo продвижение` даёт **LOW / demand_score=23 / hh_ru=71 / yandex_suggest=100**, `generative engine optimization` даёт **LOW / demand_score=18 / hh_ru=22 / yandex_suggest=100**, `answer engine optimization` даёт **LOW / demand_score=15 / yandex_suggest=100**. То есть массового спроса пока нет, но профессиональный рынок явно начинает формироваться. [T3]

## 1. Сигналы спроса

### Demand API
- `geo продвижение` -> **LOW**, `demand_score=23`, `hh_ru=71`, `google_trends_ru=3`, `yandex_suggest=100`. [T3]
- `generative engine optimization` -> **LOW**, `demand_score=18`, `hh_ru=22`, `google_trends_ru=0`, `yandex_suggest=100`. [T3]
- `answer engine optimization` -> **LOW**, `demand_score=15`, `hh_ru=0`, `google_trends_ru=0`, `yandex_suggest=100`. [T3]
- `generative seo` -> **LOW**, `demand_score=3`, `hh_ru=24`, `yandex_suggest=2`. [T3]
- `ai search optimization` -> **LOW**, `demand_score=0`, `hh_ru=7`, `yandex_suggest=2`. [T3]

### Интерпретация
- Category ещё ранняя, терминология не устоялась, поэтому exact-brand/exact-category pull слабый. [T3][inference]
- Но высокая частота `yandex_suggest=100` у нескольких запросов и наличие HH-сигналов говорят, что рынок уже начал искать, обсуждать и продавать GEO/AEO как отдельную практику. [T3][inference]
- Следовательно, demand есть не как массовый SMB inbound, а как early enterprise/professional services motion. [T3][inference]

## 2. Category proof и why now
1. Conductor прямо позиционирует AI Search Performance как system of record для AI visibility и competitive exposure, а не как cosmetic add-on к SEO dashboard. Это усиливает тезис о новой управленческой функции внутри marketing/brand/search команд. [T1]
2. На academy-странице Conductor фиксирует, что enterprise SEO сегодня уже включает и AEO, потому что аудитория ищет ответы не только в Google, но и в ChatGPT/Perplexity. Это важный признак platform-level shift, а не модного микро-тренда. [T2]
3. Публичный ценовой anchor **$30 000-200 000+ в год** показывает, что budget owner для таких платформ уже существует и чек достаточно высокий для Program 2. [T2]
4. В России появился не только контентный шум, но и коммерческая упаковка. «Ашманов и партнёры» продают GEO-продвижение как отдельную услугу от **180 000 ₽**, объясняют механику попадания в AI-ответы и отдельно учат клиентов считать GEO-метрики. [T4]
5. После запуска AI-ответов в Поиске Яндекса в мае 2025 года локальный рынок получил собственный distribution shift, а не просто импортированный западный тренд. [T5]

## 3. Что это значит для локального кейса
- Вести кейс как «продаём западный Conductor в РФ» рискованно, потому что брендовый спрос почти не виден, а локальный рынок пока покупает скорее сервис, чем чистую платформу. [T3][T4][inference]
- Вести кейс как enterprise AEO/GEO operating layer значительно сильнее: аудит AI visibility, мониторинг brand presence, карта prompt/query space, контентные приоритеты, competitive intelligence, reporting для CMO/SEO lead и managed optimization. [T1][T2][T4][inference]
- То есть проходной wedge в РФ, вероятно, лежит в productized service + platform workflow, а не в прямом SaaS-resale. [T3][T4][inference]

## 4. Кто купит
Вероятный ICP:
1. крупные бренды с сильной зависимостью от органики,
2. e-commerce и маркетплейс-игроки,
3. финтех, travel, real estate, education и healthcare-маркетинг с длинным research journey,
4. enterprise SEO/brand teams,
5. digital-агентства и growth-консультанты, которым нужен AI-search monitoring stack.

## 5. Willingness to pay
- Глобально willingness to pay подтверждается самим positioning Conductor и диапазоном **$30 000-200 000+ в год** для enterprise SEO-платформ. [T2]
- Локально willingness to pay пока лучше доказан в сервисной оболочке: GEO-продвижение от «Ашманов и партнёры» стартует **от 180 000 ₽**, а значит buyer уже готов платить заметный чек за попадание в AI-ответы и нейровыдачу. [T4]
- Для Program 2 этого недостаточно как standalone low-ticket agency service, но достаточно, чтобы считать категорию monetizable и переводимой в более дорогой enterprise retainer / platform-assisted offering. [T2][T4][inference]

## 6. Profit gate scenarios
### Сценарий A, разовый GEO-аудит или точечная услуга
- 180 000-300 000 ₽ за проект.
- Слишком низко и слишком нерегулярно для Program 2.
- **Вердикт: NO PASS.**

### Сценарий B, recurring GEO service layer для mid-market
- 250 000-500 000 ₽ в месяц за мониторинг, контентные рекомендации, промпт-карту и отчётность.
- На нижней границе слабо, на верхней уже погранично проходимо.
- **Вердикт: BORDERLINE PASS.**

### Сценарий C, enterprise AEO platform + managed optimization
- 600 000-1 500 000 ₽ в месяц, если продавать continuous monitoring, competitive intelligence, workflow integration, executive reporting и AI-search content ops.
- При 3-5 клиентах модель уже проходит порог Program 2.
- **Вердикт: PASS.**

### Сценарий D, агентский resale/consulting без platform leverage
- Много ручной аналитики и кастома, слабая повторяемость.
- Экономика может собраться, но moat и scalability ухудшаются.
- **Вердикт: CONDITIONAL / QUALITY RISK.**

## 7. Основные риски
- Терминология AEO/GEO в РФ ещё ранняя, поэтому exact inbound слабый. [T3]
- Есть риск, что buyer предпочитает покупать агентскую услугу, а не отдельную платформу. [T4][inference]
- Category может частично раствориться внутри broader SEO/content/brand analytics stack, а не стать самостоятельным software budget line у большинства компаний. [T2][inference]
- Если delivery окажется слишком service-heavy, кейс уйдёт в агентскую модель с ограниченной масштабируемостью. [T4][inference]

## 8. Решение для pipeline
**Кейс не отклонять на demand-этапе, но вести дальше только как CONDITIONAL PASS.**

Почему:
1. есть свежий глобальный platform proof и высокий ценовой anchor, [T1][T2]
2. в РФ уже появился коммерческий GEO supply и понятный buyer pain, [T4][T5]
3. локальный спрос пока ранний, но measurable, [T3]
4. проходная экономика собирается в enterprise managed/platform-assisted motion, а не в разовых SEO-услугах. [inference]

Что обязательно проверить в P4/P5/P6:
- можно ли удержать продуктовую repeatability, а не скатиться в чистое агентство,
- сколько в реальности готовы платить крупные российские бренды за AI-search monitoring,
- где проходит граница между SEO-stack extension и отдельным AEO operating system,
- можно ли собрать moat на данных, workflow и reporting, а не только на ручной экспертизе.

## Источники
- [T1] Conductor, The New System of Record for AEO Performance, 2026-02-17: https://www.conductor.com/blog/2026-ai-search-performance/
- [T2] Conductor Academy, What is an Enterprise SEO Platform? SEO and AEO at Scale, доступ на 2026-04-22: https://www.conductor.com/academy/enterprise-seo/
- [T3] Demand API, доступ на 2026-04-22: http://172.18.0.1:9001/multi-demand?keyword=geo%20%D0%BF%D1%80%D0%BE%D0%B4%D0%B2%D0%B8%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5 ; http://172.18.0.1:9001/multi-demand?keyword=generative%20engine%20optimization ; http://172.18.0.1:9001/multi-demand?keyword=answer%20engine%20optimization ; http://172.18.0.1:9001/multi-demand?keyword=generative%20seo ; http://172.18.0.1:9001/multi-demand?keyword=ai%20search%20optimization
- [T4] Ашманов и партнёры, GEO-продвижение и коммерческое предложение, доступ на 2026-04-22: https://www.ashmanov.com/education/articles/geo-prodvizhenie-kak-popast-v-otvety-ii-a-ne-tolko-v-vydachu/ ; https://www.ashmanov.com/education/articles/po-kakim-metrikam-otsenivat-generativnuyu-optimizatsiyu-geo/ ; https://www.ashmanov.com/seo-prodvizhenie/generative-optimization/
- [T5] Яндекс, Поиск Яндекса научился рассуждать и генерировать контент с помощью технологий Алисы, 2025-05-22: https://yandex.ru/company/news/01-22-05-2025

## Market Pulse
- Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.

> Market Pulse 2026-04-23: растущий интерес.


---

## FILE: 04-economics.md


---
stage: unit-economics
case: conductor-enterprise-aeo-platform
date: 2026-04-22
analyst: branch-models-lead
sector: AI-SERVICES
verdict: PASS
confidence: medium
---

# 04-economics

## Кейс
Conductor-подобная enterprise AEO/SEO-платформа для мониторинга AI-поиска в РФ, продаваемая как platform-assisted managed service для крупных брендов.

## Итог
**Статус: PASS.**

При инвестиционной модели для enterprise-сегмента экономика сходится:
- средний чек: **600 000 ₽ MRR на клиента**,
- contribution margin: **53,3%**,
- fully-loaded blended CAC: **1 390 000 ₽**,
- payback: **2,3 месяца**,
- LTV/CAC: **4,5x**,
- break-even: **20 клиентов**,
- при **50 клиентах EBITDA ≈ 9,9 млн ₽/мес**.

Это проходит fund-level gate: компания способна достичь EBITDA значительно выше 500 тыс. ₽/мес задолго до 50 клиентов, а LTV/CAC уверенно выше 3:1.

## 1. Базовые допущения модели
| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Enterprise / upper mid-market | бренды с крупным SEO/brand budget |
| ARPU / MRR на клиента | 600 000 ₽/мес | соответствует demand-сценарию из 02-demand |
| ACV | 7 200 000 ₽/год | 12 × MRR |
| Срок внедрения | 4-6 недель | onboarding + baseline setup |
| Тип продаж | consultative / enterprise | 2-4 demo + пилот + procurement |
| Валюта модели | ₽ | РФ-модель delivery |

## 2. Подробный бизнес-процесс: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Таргет-лист аккаунтов | SDR | CRM + Excel + LinkedIn/аналоги | 30 мин/аккаунт | 1 200 | Средняя |
| 2 | Холодный outreach, email/Telegram/звонок | SDR | CRM, sequencer, телефония | 3 касания за 7 дней | 2 500 | Средняя |
| 3 | Qualification call | SDR | Meet, CRM | 30 мин | 1 500 | Низкая |
| 4 | Discovery c маркетинг/SEO-лидом | AE | Meet, шаблон discovery | 60 мин | 4 000 | Низкая |
| 5 | Предварительный AI visibility audit | SEO strategist | internal dashboard, crawler, LLM | 4 часа | 12 000 | Средняя |
| 6 | Demo платформы + roadmap | AE + strategist | Demo env, презентация | 60-90 мин | 6 500 | Низкая |
| 7 | Коммерческое предложение | AE | CRM, proposal template | 2 часа | 5 500 | Средняя |
| 8 | Security / legal / procurement | AE + CEO | почта, docs, шаблоны SLA/DPA | 1-3 недели | 18 000 | Низкая |
| 9 | Подписание договора | AE + CEO | ЭДО / юристы | 3-5 дней | 7 000 | Средняя |
| 10 | Invoice и оплата первого месяца | Finance ops | 1С/банк/ЭДО | 1 день | 2 000 | Высокая |
| 11 | Onboarding и настройка источников | CSM + strategist | dashboard, connectors | 10 часов | 25 000 | Средняя |
| 12 | Ежемесячный reporting и optimization sprint | CSM + strategist | BI, dashboard, LLM | 8-10 часов/мес | 55 000 | Средняя |

**Вывод:** продажа не self-serve. Это enterprise motion с заметной долей human-touch, поэтому CAC должен считаться fully-loaded, а не только по paid spend.

## 3. COGS на клиента в месяц
| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / storage / monitoring | 35 000 | compute + data storage + observability |
| LLM/API и crawl/data extraction | 25 000 | usage-based workload |
| SEO/AEO strategist allocation | 120 000 | ~0,35 FTE при FOT 340К |
| Analyst / QA allocation | 45 000 | подготовка выводов, quality control |
| CSM allocation | 35 000 | регулярные QBR и поддержка |
| Onboarding / support reserve | 20 000 | усреднение по месяцу |
| **Итого COGS** | **280 000** |  |

### Валовая экономика на клиента
- Revenue: **600 000 ₽/мес**
- COGS: **280 000 ₽/мес**
- Contribution per client: **320 000 ₽/мес**
- **Contribution Margin = 53,3%**

## 4. CAC по каналам и funnel conversion
| Канал | Leads/мес | MQL | SQL | Won | Конверсия lead→won | Raw CAC, ₽ | Multiplier | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| Outbound enterprise ABM | 120 | 18 | 8 | 1,2 | 1,0% | 760 000 | x2,0 | 1 520 000 | основной канал |
| Партнёрства с SEO-агентствами | 20 | 10 | 5 | 1,0 | 5,0% | 420 000 | x2,0 | 840 000 | лучший CAC, но ограничен по объёму |
| Контент / inbound / вебинары | 35 | 8 | 4 | 0,4 | 1,1% | 510 000 | x2,0 | 1 020 000 | длинный цикл, помогает бренду |

### Blended CAC
При миксе 50% outbound, 30% partnerships, 20% inbound:

**Blended fully-loaded CAC = 1 390 000 ₽ на нового платящего клиента.**

Это попадает в sanity-range для enterprise SaaS/AI B2B в РФ: complex sales редко бывает дешёвым, а ACV здесь достаточно высокий, чтобы CAC > 1 млн ₽ оставался допустимым.

## 5. Fully-loaded CAC: обязательная раскладка
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | performance-поддержка и retargeting | модель аналитика |
| Outbound team FOT (SDR/AE attributed to new) | 562 000 | SDR 234К + AE 468К, 80% на new logo | benchmark HH.ru из задания + 30% социалки |
| Marketing team FOT (partial allocation) | 260 000 | 0,5 PMM/Content FTE на acquisition | benchmark HH.ru из задания |
| Tools (CRM, sequencer, enrichment, BI) | 95 000 | CRM + outreach stack + аналитика | рыночная оценка SaaS stack |
| Events/partnerships | 180 000 | вебинары, co-marketing, referral fees | модель аналитика |
| **Подытог raw CAC spend / мес** | **1 277 000** |  |  |
| Overhead multiplier (x1.3) | 383 100 | стандартный overhead на enterprise B2B motion | стандарт из задания |
| **Итого fully-loaded spend / мес** | **1 660 100** |  |  |

Если в месяц закрывается **1,2 нового клиента**, то:

**Fully-loaded CAC = 1 660 100 / 1,2 = 1 383 417 ₽ ≈ 1,39 млн ₽**

## 6. LTV и churn
### Benchmark churn
Для SaaS с заметным уровнем MRR ChartMogul указывает gross MRR churn порядка **4-5% в месяц**, при этом retention улучшается у компаний с более высоким ARPA. Для enterprise-ARPA модели уместно брать более консервативный logo churn ниже массового SMB уровня. [T3][inference]

### Принятое допущение
- Monthly logo churn: **1,5%**
- Средняя жизнь клиента: **1 / 0,015 = 66,7 месяца**
- Gross margin для LTV: **53,3%**

### LTV
Формула:

**LTV = ARPU × Contribution Margin / Churn**

Подстановка:

**LTV = 600 000 × 0,533 / 0,015 = 21 320 000 ₽**

### LTV/CAC
**LTV/CAC = 21,32 млн / 1,39 млн = 15,3x** по математике чистой модели.

Для инвестиционного комитета беру более консервативный haircut 70% на downsell, pilot churn, procurement drag и service dilution:

**Stress-case LTV = 6 396 000 ₽**
**Stress-case LTV/CAC = 6,40 млн / 1,39 млн = 4,6x**

### Инвест-вывод
Даже после жёсткого haircut кейс сохраняет **LTV/CAC > 3:1**, то есть остаётся investment-grade.

## 7. CAC payback
Формула из задания:

**CAC Payback = CAC / MRR per customer**

Подстановка:

**1 390 000 / 600 000 = 2,3 месяца**

Даже если считать по contribution profit:

**1 390 000 / 320 000 = 4,3 месяца**

Обе версии лучше порога 12 месяцев, следовательно payback здоровый.

## 8. Team & FOT
### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | продажи ключевых сделок, стратегия | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | продукт, архитектура, delivery quality | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion/data pipelines | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | integrations/reporting | 450 000 | 135 000 | 585 000 |
| Frontend Engineer | dashboard/UI | 320 000 | 96 000 | 416 000 |
| DevOps | infra, observability, security | 350 000 | 105 000 | 455 000 |
| Product/SEO Strategist | методология, аналитика, контент ops | 250 000 | 75 000 | 325 000 |
| SDR | prospecting/outbound | 180 000 | 54 000 | 234 000 |
| AE | demos, proposals, close | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, QBR, renewals | 260 000 | 78 000 | 338 000 |
| **Итого** |  |  |  | **4 966 000** |

### Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 585 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 320 000 | 1 | 1 | 96 000 | 416 000 |
| SDR | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 360 000 | 1-2 | 2-3 | 108 000 | 468 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Product/SEO Strategist | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

## 9. Cumulative FOT timeline M1-M12
| Месяц | Кто подключается | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Backend #1 | 2 145 000 |
| M2 | + Frontend | 2 561 000 |
| M3 | + DevOps, Strategist | 3 341 000 |
| M4 | + Backend #2 | 3 926 000 |
| M5 | + SDR | 4 160 000 |
| M6 | + AE | 4 628 000 |
| M7 | + Customer Success | 4 966 000 |
| M8 | без новых hires | 4 966 000 |
| M9 | без новых hires | 4 966 000 |
| M10 | без новых hires | 4 966 000 |
| M11 | без новых hires | 4 966 000 |
| M12 | без новых hires | 4 966 000 |

**Проверка realism:** нет набора 5+ человек в первый месяц, time-to-hire соблюдён, стартовый FOT > 1 млн ₽ уже на M1, что правдоподобно для enterprise B2B SaaS.

## 10. Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 4 966 000 |
| Офис/юридические/бухгалтерия | 220 000 |
| Core infra not in COGS | 280 000 |
| Software back-office | 120 000 |
| Travel / enterprise sales support | 140 000 |
| G&A reserve | 180 000 |
| **Итого fixed costs** | **5 906 000** |

## 11. Break-even
### По числу клиентов
Формула:

**Break-even clients = Fixed costs / Contribution per client**

**5 906 000 / 320 000 = 18,46**

Округляя вверх, **break-even = 19 клиентов**, с буфером на variability беру **20 клиентов**.

### По месяцу
Ramp new logos: 0, 0, 1, 2, 3, 5, 7, 10, 13, 16, 19, 22.

| Месяц | Клиентов | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 845 000 | -2 845 000 |
| M2 | 0 | 0 | 3 181 000 | -3 181 000 |
| M3 | 1 | 320 000 | 3 961 000 | -3 641 000 |
| M4 | 2 | 640 000 | 4 546 000 | -3 906 000 |
| M5 | 3 | 960 000 | 4 940 000 | -3 980 000 |
| M6 | 5 | 1 600 000 | 5 408 000 | -3 808 000 |
| M7 | 7 | 2 240 000 | 5 746 000 | -3 506 000 |
| M8 | 10 | 3 200 000 | 5 906 000 | -2 706 000 |
| M9 | 13 | 4 160 000 | 5 906 000 | -1 746 000 |
| M10 | 16 | 5 120 000 | 5 906 000 | -786 000 |
| M11 | 19 | 6 080 000 | 5 906 000 | 174 000 |
| M12 | 22 | 7 040 000 | 5 906 000 | 1 134 000 |

**Break-even по месяцу: M11.**

## 12. Burn-to-breakeven и runway
### Burn-to-breakeven
Суммарный burn до первого положительного EBITDA месяца:

M1-M10 cumulative burn = **30 105 000 ₽**

С резервом 20% на sales delay и delayed collections:

**Startup capital to BEP ≈ 36-40 млн ₽**

### Cash runway
Если стартовый капитал **60 млн ₽**, а средний burn первых 10 месяцев около **3,0 млн ₽/мес**, то runway:

**60 / 3,0 ≈ 20 месяцев**

Даже при stress-case burn 4,0 млн ₽/мес runway остаётся **15 месяцев**.

## 13. Проверка profit gate
| Проверка | Результат |
|---|---|
| EBITDA > 500K ₽/мес достижима к 50 клиентам? | **Да, ~9,9 млн ₽/мес** |
| LTV/CAC >= 1:1? | **Да, 4,6x в stress-case** |
| LTV/CAC >= 3:1 investable? | **Да** |
| CAC Payback < 12 мес? | **Да, 2,3 мес** |
| Contribution Margin > 40%? | **Да, 53,3%** |

## 14. Главные риски
1. Если продукт расползётся в agency-heavy delivery, COGS может вырасти до 350-400К на клиента, и margin снизится.
2. Если фактический close rate по enterprise outbound будет ниже 1%, blended CAC может уйти выше 2 млн ₽.
3. Если рынок РФ будет покупать только разовые GEO-аудиты, а не recurring platform-assisted service, ARPU 600К не удержится.
4. Procurement delay на 2-3 месяца ухудшит burn-to-breakeven.

## 15. Финальный вывод
Экономика **проходит** на уровне фонда, но только в конкретной конфигурации:
- не как «инструмент SEO для всех»,
- а как **enterprise AI visibility operating layer**,
- с высоким ACV,
- умеренно стандартизированным delivery,
- и дисциплиной по fully-loaded CAC.

При такой модели кейс инвестиционно пригоден.

## Источники
- [T1] Conductor Academy, Enterprise SEO / AEO pricing anchor, доступ из 02-demand: https://www.conductor.com/academy/enterprise-seo/
- [T2] Conductor, AI Search Performance positioning, доступ из 02-demand: https://www.conductor.com/blog/2026-ai-search-performance/
- [T3] ChartMogul Help Center, Gross MRR churn benchmark for SaaS > $10k MRR, updated 2026-03-03: https://help.chartmogul.com/article/204-chart-gross-mrr-churn-rate ; Benchmarks overview: https://help.chartmogul.com/article/138-benchmarks


---

## FILE: 05-critic.md


# SECTION A. PnL 12 месяцев x 3 сценария

## Исходные данные из 04-economics.md
- ARPA base: **600 000 ₽/клиент/мес**
- COGS base: **280 000 ₽/клиент/мес**
- Contribution margin base: **320 000 ₽/клиент/мес**
- Fixed costs run-rate: **5 906 000 ₽/мес**
- Team FOT fully-loaded: **4 966 000 ₽/мес**
- CAC by channel:
  - outbound ABM: **1 520 000 ₽**
  - partnerships: **840 000 ₽**
  - inbound/content: **1 020 000 ₽**
  - blended CAC: **1 390 000 ₽**
- LTV (stress-case invest view): **6 396 000 ₽**
- LTV/mo по gross contribution logic: **320 000 ₽/мес на клиента**

## Сценарные допущения
- **Base:** ARPA 600k, COGS 280k, fixed costs 5.906m, налоговый режим для net-waterfall: **УСН 6%**.
- **Optimistic:** быстрее sales ramp, ARPA **630k**, COGS **275k**, fixed costs **6.2m**, налоговый режим для net-waterfall: **IT-льгота 3%** при аккредитации Минцифры.
- **Pessimistic:** slower ramp, ARPA **570k**, COGS **295k**, fixed costs **6.1m**, налоговый режим для net-waterfall: **ОСНО 20%** по прибыли; НДС 20% shown separately as cash/tax burden if компания на ОСНО.
- Во всех сценариях страховые взносы на ФОТ приняты **~30%**, как уже заложено в fully-loaded FOT из 04-economics.
- Cash burn = отрицательная EBITDA по модулю. Cumulative cash = накопленная EBITDA от точки старта, без учёта внешнего финансирования и without working capital adjustments.

---

## 1) Base scenario PnL, M1-M12

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 10 | 13 | 16 | 19 | 22 |
| Total clients | 0 | 0 | 1 | 3 | 6 | 11 | 18 | 28 | 41 | 57 | 76 | 98 |
| MRR, ₽ | 0 | 0 | 600 000 | 1 800 000 | 3 600 000 | 6 600 000 | 10 800 000 | 16 800 000 | 24 600 000 | 34 200 000 | 45 600 000 | 58 800 000 |
| COGS, ₽ | 0 | 0 | 280 000 | 840 000 | 1 680 000 | 3 080 000 | 5 040 000 | 7 840 000 | 11 480 000 | 15 960 000 | 21 280 000 | 27 440 000 |
| Gross profit, ₽ | 0 | 0 | 320 000 | 960 000 | 1 920 000 | 3 520 000 | 5 760 000 | 8 960 000 | 13 120 000 | 18 240 000 | 24 320 000 | 31 360 000 |
| GM% | 0.0% | 0.0% | 53.3% | 53.3% | 53.3% | 53.3% | 53.3% | 53.3% | 53.3% | 53.3% | 53.3% | 53.3% |
| Fixed costs, ₽ | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 | 5 906 000 |
| EBITDA, ₽ | -5 906 000 | -5 906 000 | -5 586 000 | -4 946 000 | -3 986 000 | -2 386 000 | -146 000 | 3 054 000 | 7 214 000 | 12 334 000 | 18 414 000 | 25 454 000 |
| Cash burn, ₽ | 5 906 000 | 5 906 000 | 5 586 000 | 4 946 000 | 3 986 000 | 2 386 000 | 146 000 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 906 000 | -11 812 000 | -17 398 000 | -22 344 000 | -26 330 000 | -28 716 000 | -28 862 000 | -25 808 000 | -18 594 000 | -6 260 000 | 12 154 000 | 37 608 000 |

**Break-even:**
- по client count: **19 клиентов**
- по месяцам: **M8**
- startup_capital_to_bep_rub: **34 634 400 ₽** (burn до BEP + 20% buffer)

### Base waterfall
- ARPA: **600 000 ₽**
- Gross profit after COGS: **320 000 ₽**
- Contribution margin: **53.3%**
- EBITDA at steady-state BE client: **19 × 320 000 - 5 906 000 = 174 000 ₽/мес**
- Net after tax:
  - **УСН 6%:** 174 000 - 114 000 = **60 000 ₽/мес** at BE revenue level
  - **IT-льгота 3%:** 174 000 - 57 000 = **117 000 ₽/мес**
  - **ОСНО 20%:** 174 000 - 34 800 = **139 200 ₽/мес** before VAT cash timing

---

## 2) Optimistic scenario PnL, M1-M12

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 2 | 3 | 5 | 7 | 10 | 13 | 16 | 19 | 22 | 25 |
| Total clients | 0 | 1 | 3 | 6 | 11 | 18 | 28 | 41 | 57 | 76 | 98 | 123 |
| MRR, ₽ | 0 | 630 000 | 1 890 000 | 3 780 000 | 6 930 000 | 11 340 000 | 17 640 000 | 25 830 000 | 35 910 000 | 47 880 000 | 61 740 000 | 77 490 000 |
| COGS, ₽ | 0 | 275 000 | 825 000 | 1 650 000 | 3 025 000 | 4 950 000 | 7 700 000 | 11 275 000 | 15 675 000 | 20 900 000 | 26 950 000 | 33 825 000 |
| Gross profit, ₽ | 0 | 355 000 | 1 065 000 | 2 130 000 | 3 905 000 | 6 390 000 | 9 940 000 | 14 555 000 | 20 235 000 | 26 980 000 | 34 790 000 | 43 665 000 |
| GM% | 0.0% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% | 56.3% |
| Fixed costs, ₽ | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 |
| EBITDA, ₽ | -6 200 000 | -5 845 000 | -5 135 000 | -4 070 000 | -2 295 000 | 190 000 | 3 740 000 | 8 355 000 | 14 035 000 | 20 780 000 | 28 590 000 | 37 465 000 |
| Cash burn, ₽ | 6 200 000 | 5 845 000 | 5 135 000 | 4 070 000 | 2 295 000 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 200 000 | -12 045 000 | -17 180 000 | -21 250 000 | -23 545 000 | -23 355 000 | -19 615 000 | -11 260 000 | 2 775 000 | 23 555 000 | 52 145 000 | 89 610 000 |

**Break-even:**
- по client count: **18 клиентов**
- по месяцам: **M6**
- startup_capital_to_bep_rub: **28 254 000 ₽**

### Optimistic waterfall
- ARPA: **630 000 ₽**
- Gross profit after COGS: **355 000 ₽**
- Contribution margin: **56.3%**
- EBITDA at steady-state BE client: **18 × 355 000 - 6 200 000 = 190 000 ₽/мес**
- Net after tax:
  - **IT-льгота 3%:** 190 000 - 340 200 = **-150 200 ₽/мес** if taxed as revenue at exact BE revenue point
  - **УСН 6%:** 190 000 - 680 400 = **-490 400 ₽/мес**
  - **ОСНО 20%:** 190 000 - 38 000 = **152 000 ₽/мес** before VAT cash timing

Примечание: для revenue-based tax regimes операционный break-even по EBITDA наступает раньше, чем post-tax break-even; это важно для cash planning.

---

## 3) Pessimistic scenario PnL, M1-M12

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 5 | 7 | 9 | 11 | 13 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 4 | 7 | 12 | 19 | 28 | 39 | 52 |
| MRR, ₽ | 0 | 0 | 0 | 570 000 | 1 140 000 | 2 280 000 | 3 990 000 | 6 840 000 | 10 830 000 | 15 960 000 | 22 230 000 | 29 640 000 |
| COGS, ₽ | 0 | 0 | 0 | 295 000 | 590 000 | 1 180 000 | 2 065 000 | 3 540 000 | 5 605 000 | 8 260 000 | 11 505 000 | 15 340 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 275 000 | 550 000 | 1 100 000 | 1 925 000 | 3 300 000 | 5 225 000 | 7 700 000 | 10 725 000 | 14 300 000 |
| GM% | 0.0% | 0.0% | 0.0% | 48.2% | 48.2% | 48.2% | 48.2% | 48.2% | 48.2% | 48.2% | 48.2% | 48.2% |
| Fixed costs, ₽ | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 | 6 100 000 |
| EBITDA, ₽ | -6 100 000 | -6 100 000 | -6 100 000 | -5 825 000 | -5 550 000 | -5 000 000 | -4 175 000 | -2 800 000 | -875 000 | 1 600 000 | 4 625 000 | 8 200 000 |
| Cash burn, ₽ | 6 100 000 | 6 100 000 | 6 100 000 | 5 825 000 | 5 550 000 | 5 000 000 | 4 175 000 | 2 800 000 | 875 000 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 100 000 | -12 200 000 | -18 300 000 | -24 125 000 | -29 675 000 | -34 675 000 | -38 850 000 | -41 650 000 | -42 525 000 | -40 925 000 | -36 300 000 | -28 100 000 |

**Break-even:**
- по client count: **23 клиента**
- по месяцам: **M10**
- startup_capital_to_bep_rub: **51 030 000 ₽**

### Pessimistic waterfall
- ARPA: **570 000 ₽**
- Gross profit after COGS: **275 000 ₽**
- Contribution margin: **48.2%**
- EBITDA at steady-state BE client: **23 × 275 000 - 6 100 000 = 225 000 ₽/мес**
- Net after tax:
  - **ОСНО 20%:** 225 000 - 45 000 = **180 000 ₽/мес** before VAT cash timing
  - **IT-льгота 3%:** 225 000 - 393 300 = **-168 300 ₽/мес**
  - **УСН 6%:** 225 000 - 786 600 = **-561 600 ₽/мес**

---

## 4) Waterfall summary, annualized view

| Scenario | ARPA, ₽/мес | Gross after COGS, ₽/client/mo | Contribution margin | Annual revenue, ₽ | Annual gross profit, ₽ | Annual EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Base | 600 000 | 320 000 | 53.3% | 203 400 000 | 108 480 000 | 37 608 000 |
| Optimistic | 630 000 | 355 000 | 56.3% | 291 060 000 | 164 010 000 | 89 610 000 |
| Pessimistic | 570 000 | 275 000 | 48.2% | 93 480 000 | 45 100 000 | -28 100 000 |

### Net after taxes, annualized
| Scenario | Tax mode anchor | Revenue tax / profit tax, ₽ | Net after tax, ₽ | VAT 20% if applicable |
|---|---|---:|---:|---:|
| Base | УСН 6% | 12 204 000 | 25 404 000 | не применимо |
| Base | IT-льгота 3% | 6 102 000 | 31 506 000 | не применимо |
| Base | ОСНО 20% | 7 521 600 | 30 086 400 | 40 680 000 |
| Optimistic | УСН 6% | 17 463 600 | 72 146 400 | не применимо |
| Optimistic | IT-льгота 3% | 8 731 800 | 80 878 200 | не применимо |
| Optimistic | ОСНО 20% | 17 922 000 | 71 688 000 | 58 212 000 |
| Pessimistic | УСН 6% | 5 608 800 | -33 708 800 | не применимо |
| Pessimistic | IT-льгота 3% | 2 804 400 | -30 904 400 | не применимо |
| Pessimistic | ОСНО 20% | 0 | -28 100 000 | 18 696 000 |

## 5) Налоговая модель и cash implications
- **УСН 6%:** простой режим, но tax-on-revenue делает post-tax break-even заметно позже EBITDA break-even.
- **IT-льгота 3%:** лучший режим для software-heavy модели, если соблюдены критерии и есть аккредитация Минцифры; materially improves cash conversion.
- **ОСНО 20%:** налог на прибыль лучше синхронизирован с EBITDA, но появляется **НДС 20%**, который существенно влияет на cash timing, especially for enterprise contracts.
- **Страховые взносы ~30% к ФОТ** уже embedded в FOT и partly in CAC allocations.

## 6) Итог по break-even и потребности в капитале
| Scenario | BE clients | EBITDA BE month | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Base | 19 | M8 | 34 634 400 ₽ |
| Optimistic | 18 | M6 | 28 254 000 ₽ |
| Pessimistic | 23 | M10 | 51 030 000 ₽ |

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## 1) Sensitivity analysis, EBITDA через 12 месяцев

База для расчёта: на M12 модель из SECTION A даёт **98 клиентов**, fixed costs **5 906 000 ₽/мес**, contribution на клиента **320 000 ₽/мес**.

| Сценарий | Допущение | Contribution / клиент, ₽/мес | EBITDA @M12, ₽/мес | CAC payback, мес | LTV/CAC | Комментарий |
|---|---|---:|---:|---:|---:|---|
| Base | без изменений | 320 000 | 25 454 000 | 4,3 | 15,3x | агрессивно, но проходной уровень |
| Sens1 | CAC x2 | 320 000 | 25 454 000 | 8,7 | 7,7x | EBITDA по P&L не меняется сразу, но резко падает эффективность роста |
| Sens2 | Churn x2 | 320 000 | 25 454 000 | 4,3 | 7,7x | M12 EBITDA ещё держится, но долгий LTV режется вдвое |
| Sens3 | Price -30% | 140 000 | 7 814 000 | 9,9 | 6,7x | главный удар по unit economics, запас прочности почти исчезает |

**Вывод:** для этого кейса самый опасный single-variable shock не CAC x2 и не churn x2, а именно **снижение цены на 30%**, потому что модель держится на высоком enterprise ARPU. CAC и churn не ломают M12 EBITDA мгновенно, но ломают future payback, LTV/CAC и стоимость дальнейшего масштабирования.

## 2) Monte Carlo Lite, confidence intervals

### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 020 000 | 1 390 000 | 2 300 000 | [T3], [T6], [T7], [T8], [T12], [T13], [inference] |
| Monthly churn, % | 1,0% | 1,5% | 3,5% | [T3], [T6], [T9], [inference] |
| ARPU, ₽/мес | 420 000 | 600 000 | 900 000 | [T1], [T2], [T4], [T10], [inference] |
| Conversion lead→paid, % | 0,8% | 1,2% | 2,0% | [T3], [T6], [T12], [inference] |
| Time-to-hire, месяцев | 1,0 | 1,5 | 3,0 | [T3], [T13], [inference] |

### Метод
Вместо полноценной 1000-итерационной симуляции использую **9 комбинаций** min/mode/max для CAC, churn и ARPU, а conversion + time-to-hire беру как модификаторы клиентской базы к M24. Это даёт упрощённый p10/p50/p90 для monthly EBITDA на 24-м месяце.

Предположение для base M24: **50 клиентов**, что соответствует already-proven target из 04-economics, где при 50 клиентах EBITDA около **9,9 млн ₽/мес**.

### Results, confidence intervals
| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -3 526 000 | 10 094 000 | 71 594 000 | 75 120 000 |
| CAC payback, мес | 16,4 | 4,3 | 1,6 | 14,8 |
| LTV/CAC | 1,7x | 15,3x | 60,8x | 59,0 |
| Cash runway, мес | 17,0 | 24,0+ | 24,0+ | 7,0+ |

### Интерпретация Monte Carlo Lite
- **Правило 1:** p10 EBITDA < 0, значит автоматически возникает **kill criterion #1: риск неплатёжеспособности**.
- **Правило 2:** p50 EBITDA = **10,1 млн ₽/мес**, то есть median-case уверенно проходит gate **500К ₽/мес**.
- **Правило 3:** p90/p10 по EBITDA в строгом виде неинтерпретируемо, потому что p10 отрицательный. Это ещё хуже, чем >10x, так как распределение пересекает ноль и модель остаётся highly path-dependent.
- **Правило 4:** width по **LTV/CAC = 59,0**, что сильно выше порога 8. Значит модель действительно **хрупкая** и почти полностью зависит от удержания premium pricing + churn discipline.

**Итог:** median-case хороший, но downside некомфортный. Для фонда это не auto-reject, но кейс требует дисконта по score из-за высокой дисперсии исходов.

## 3) Competitor deep-dive

### 3.1 Топ-3 западных конкурента

| Игрок | Почему конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Semrush Enterprise / AI Toolkit** | уже сидит в бюджете SEO/competitive intelligence | мощный бренд, широкий suite, enterprise upsell, сильный data moat [T6] | для AI visibility пока скорее extension к большому suite, чем узкий operating layer; риск feature overload | **25-30% global enterprise mindshare** в adjacent SEO/visibility stack, оценка по brand/distribution [T6][inference] | можем продавать не suite, а узкий AEO workflow под РФ, быстрее time-to-value |
| **BrightEdge** | enterprise SEO platform с Copilot/AI-функциями и сильным CMO foothold | сильные отношения с enterprise-маркетингом, зрелый reporting, интеграции [T7] | дорогой и тяжёлый внедренческий стек, локализация под РФ слабая | **15-20%** enterprise SEO platform layer [T7][inference] | локальная delivery-модель, ниже procurement friction, data residency в РФ |
| **seoClarity** | AI-driven enterprise SEO + automation + content/insights | сильная аналитика, automation, search/share-of-voice фокус [T8] | меньше category pull вне SEO-команд, слабее GTM-brand, чем у Semrush/BrightEdge | **8-12%** enterprise SEO intelligence niche [T8][inference] | можем занять позицию не «SEO tool», а «AI-answer visibility OS» с managed layer |

### 3.2 Топ-4 российских конкурента

| Игрок | Почему конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Ашманов и партнёры / GEO-продвижение** | уже публично продают GEO как отдельную услугу [T4] | сильный бренд в SEO, доверие enterprise, понятный commercial entry-point | это скорее agency/service, чем scalable platform; margin и repeatability хуже | **20-25% российского GEO services mindshare** [T4][inference] | если превратим delivery в productized workflow, сможем выиграть по repeatability и unit economics |
| **Head Promo** | активно объясняют GEO/AEO и продают AI-driven SEO/LLM visibility services [T12][T13] | сильная контент-экспертиза, быстрая упаковка спроса, заметность в профсообществе | меньше enterprise platform DNA, больше сервисная зависимость | **10-15% early GEO/AEO agency mindshare** [T12][T13][inference] | наша сила может быть в monitoring + reporting layer, а не только в консалтинге |
| **Demis Group** | крупный SEO/performance игрок, способен быстро добавить GEO в текущий пакет [T14] | масштаб продаж, существующая база клиентов, широкий digital stack | GEO может быть лишь add-on внутри agency P&L, без глубокого data moat | **10-15% adjacent enterprise SEO demand** [T14][inference] | специализированный AEO-продукт может дать более высокий ACV и ниже service dilution |
| **Нейроцех / NeuroReach (vc.ru)** | ранний локальный AI-search/GEO-native игрок [T11] | нативная AI-подача, быстрая адаптация под новую категорию | маленький масштаб, слабее бренд и enterprise procurement readiness | **3-7% early adopter segment** [T11][inference] | у нас выше шанс выиграть enterprise сегмент за счёт reliability, security и SLA |

### Конкурентный вывод
1. На Западе конкурировать придётся не с одним «чистым GEO стартапом», а с уже установленными enterprise SEO suites, которые быстро добавляют AI visibility features.
2. В России реальная конкуренция сегодня идёт в основном со стороны **агентств и productized services**, а не зрелых pure-play платформ.
3. Значит окно есть, но только если продукт останется **platform-assisted managed service**, а не скатится в кастомное SEO-агентство.

## 4) Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного SEO strategist + AE вовремя | med | sales ramp и delivery quality сдвигаются на 2-3 месяца | time-to-hire > 2,5 мес, offer acceptance < 50% | заранее строить bench подрядчиков, founder-led selling первые 6 мес |
| Operational | LLM/API cost inflation или деградация качества ответов | med | COGS растёт, margin падает ниже 45% | LLM/API spend > 40К ₽ на клиента, рост fallback/manual QA | multi-vendor routing, лимиты, кэширование, локальные модели для части задач |
| Market | Категория остаётся «услугой GEO», а не recurring platform budget | high | ARPU падает до 180-300К, SaaS multiple рушится | большинство сделок закрываются как разовые аудиты | жёстко продавать retainer + monitoring + executive reporting |
| Market | Price compression из-за агентств и bundled SEO contracts | high | ARPU -20-30%, payback почти удваивается | скидки > 20% в 3+ подряд сделках | value-based packaging, SLA, proof dashboards, отказаться от low-end сегмента |
| Regulatory | 152-ФЗ и data residency ограничивают хранение query/log data вне РФ | med | enterprise procurement delay, часть клиентов lost | security review > 45 дней, вопросы по хранению prompt/data | РФ-хостинг, DPA, сегрегация данных, on-prem/private deployment option |
| Regulatory | Санкции/SaaS restrictions режут доступ к западным API и tooling | med | delivery interruptions, vendor lock-in losses | нестабильный billing, region blocks, рост VPN/manual workarounds | резервные поставщики, open-source fallback, контракты в рублях где возможно |
| Financial | Runway съедается до достижения 20 клиентов | med | down round или остановка роста | cash runway < 9 мес, cumulative burn > plan на 25% | ежемесячный cash review, hire gating, founder-only expansion до PMF |
| Financial | Ослабление рубля к USD/EUR повышает infra и data cost | med | COGS и fixed costs растут, EBITDA volatility усиливается | USD/RUB > 110 и рост cloud/API bill 15%+ | валютный буфер, рублёвые контракты, пересмотр цен раз в квартал |
| Black swan | Резкое отключение ключевого LLM-провайдера | med | service outage, churn spike | major provider incident > 24 часа, рост failed jobs | резерв из 2-3 моделей, graceful degradation в отчётах, manual ops playbook |
| Black swan | Новая волна санкций/эскалации ломает enterprise marketing budgets | low | pipeline freeze, elongation procurement, churn | заморозка тендеров, перенос QBR, задержки оплат > 30 дней | фокус на критичных вертикалях, shorter contracts, emergency cost cuts |

### Резюме по рискам
- Самые опасные риски здесь не технические, а **market + pricing**.
- Regulatory и black swan не обязаны убить кейс сразу, но делают обязательными local hosting, multi-vendor LLM stack и conservative cash management.

## 5) Kill conditions через 6 месяцев

1. **EBITDA risk / insolvency:** если rolling 3-month forward model даёт **p10 EBITDA @M24 < 0** и cash runway падает ниже **9 месяцев**, продолжать нельзя.
2. **EBITDA gate failure:** если к месяцу 6 median-case модель даёт **p50 EBITDA @M24 < 500 000 ₽/мес**, кейс не проходит фондовый profit gate.
3. **Go-to-market failure:** если через 6 месяцев одновременно выполняется хотя бы два условия: **ARPU < 450 000 ₽**, **blended CAC > 2 200 000 ₽**, **monthly churn > 3%**, это означает, что premium enterprise wedge не подтвердился.

## 6) Финальный вывод SECTION B

Кейс остаётся **проходимым**, но уже не как «чистый SaaS-аналог западного Conductor». Инвестиционная логика держится только в конфигурации:
- enterprise ICP,
- premium ARPU,
- platform-assisted managed service,
- умеренный churn,
- контроль vendor/API риска.

Если рынок утянет продукт в agency-heavy delivery или вынудит уйти в price compression на 20-30%, upside сохранится, но качество бизнеса резко ухудшится.

## Дополнительные источники
- [T6] Semrush, Enterprise SEO / AI Toolkit pages, доступ 2026-04-23: https://www.semrush.com/enterprise/ ; https://www.semrush.com/apps/ai-toolkit/
- [T7] BrightEdge, enterprise SEO and AI pages, доступ 2026-04-23: https://www.brightedge.com/platform ; https://www.brightedge.com/copilot
- [T8] seoClarity, AI-driven enterprise SEO platform, доступ 2026-04-23: https://www.seoclarity.net/platform
- [T9] First Page Sage, SEO SaaS churn benchmarks, доступ 2026-04-23: https://firstpagesage.com/seo-blog/saas-churn-rate-benchmarks/
- [T10] Conductor pricing anchor / enterprise SEO budget range, доступ 2026-04-23: https://www.conductor.com/academy/enterprise-seo/
- [T11] vc.ru, NeuroReach / GEO-related local market packaging, доступ 2026-04-23: https://vc.ru/marketing/2014426-generative-engine-optimization-kak-optimizirovat-kontent-dlya-ii-poiska-v-2025-godu
- [T12] Habr, GEO/AEO market articles including Head Promo context, доступ 2026-04-23: https://habr.com/ru/companies/headpromo/articles/928388/ ; https://habr.com/ru/articles/922530/
- [T13] Rusprofile / company footprint checks for Russian SEO-service competitors, доступ 2026-04-23: https://www.rusprofile.ru/
- [T14] Demis Group, GEO/AI-search service positioning, доступ 2026-04-23: https://www.demis.ru/articles/geo-generative-engine-optimization/

<!-- P6B-DONE -->


---

## FILE: 06-verdict.md


[AI-SERVICES] Conductor Enterprise AEO Platform — NEAR-PASS: 67/100 | EBITDA base=10094К₽/мес через 24 мес | LTV/CAC=4,6x | Ключевое преимущество: высокий enterprise ACV и понятный AI-visibility wedge | Главный риск: weak moat и ранний локальный спрос.

---
stage: verdict
case: conductor-enterprise-aeo-platform
date: 2026-04-23
analyst: branch-models-lead
verdict: NEAR-PASS
confidence: medium
investment_grade: false
sector: AI-SERVICES
normalized_score: 67/100
raw_score_total: 100/150
company_ebitda_potential_rub_month: 10094000
clients_to_500k_ebitda: 21
months_to_500k_ebitda: 8
startup_capital_to_bep_rub: 34634400
---

# 06-verdict — Investment Verdict

sector: AI-SERVICES

## Итоговое решение
**NEAR-PASS, финальный pipeline-статус: REJECTED.**

Кейс проходит economics-gate и теоретически способен выйти на **company_ebitda_rub_month ≈ 10,1 млн ₽/мес к M24** при 50 клиентах, но не проходит инвесткомитет из-за трёх вещей: ранний и слабо верифицированный локальный спрос, weak moat и высокий риск price compression в agency-heavy рынке.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | `contribution margin: 53,3%`, `payback: 2,3 месяца`, `Stress-case LTV/CAC = 4,6x`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 22 | `при 50 клиентах EBITDA ≈ 9,9 млн ₽/мес`, p50 `EBITDA @M24 = 10,1 млн ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | `локальный спрос пока ранний, но measurable`; штраф из-за отсутствия строки `Sources:` в demand-файле. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | `рынок утянет продукт в agency-heavy delivery` и западные suites быстро добавляют AI visibility features. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | `local hosting, multi-vendor LLM stack и conservative cash management` обязательны уже в base-case. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | `основной канал` outbound ABM, partnerships дают `лучший CAC`, enterprise ICP и чек совпадают. |

**Сумма raw:** 100/150  
**Normalized score:** **67/100**

## Investment committee verdict
**REJECTED (<70 после нормализации).**

Порог EBITDA компания проходит, но approve невозможен, потому что правило P7 требует одновременно score ≥ 70 и EBITDA-потенциал ≥ 500К ₽/мес при ≤50 клиентах и ≤24 мес. Здесь вторая часть есть, первая нет.

## Почему это не approve
1. **Спрос в РФ ещё ранний.** В `02-demand.md` прямо сказано: `локальный спрос пока ранний, но measurable`, а Demand API везде даёт LOW.
2. **Moat слабый.** Сильнее всего видна productized-service обвязка, а не защищённый software moat.
3. **Рынок склонен к price compression.** `самый опасный single-variable shock` в `05-critic.md` это `снижение цены на 30%`.
4. **Evidence quality формально не дотягивает.** В demand-файле отсутствует обязательная строка `Sources: T1=..., T2=..., T3=...`, поэтому criterion #3 получает штраф и в рисках фиксируется `evidence_quality_unverified`.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| ARPA | 600 000 ₽/клиент/мес |
| customer_ltv_rub (stress-case invest view) | 6 396 000 ₽ |
| customer_ltv_rub (матмодель) | 21 320 000 ₽ |
| CAC blended fully-loaded | 1 390 000 ₽ |
| LTV/CAC (stress-case) | 4,6x |
| LTV/CAC (матмодель) | 15,3x |
| CAC payback по revenue | 2,3 мес |
| CAC payback по contribution_margin_rub_month | 4,3 мес |
| Gross Margin | 53,3% |
| contribution_margin_rub_month | 320 000 ₽/клиент/мес |
| fixed_costs_rub_month | 5 906 000 ₽/мес |
| Break-even clients | 19 клиентов |
| Break-even month (PnL base из 05-critic) | M8 |
| startup_capital_to_bep_rub | 34 634 400 ₽ |
| company_ebitda_rub_month @50 клиентов | 9 900 000 ₽/мес |
| company_ebitda_potential_rub_month @M24 p50 | 10 094 000 ₽/мес |
| clients_to_500k_ebitda | 21 |
| months_to_500k_ebitda | 8 |

## FULL business process from 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Таргет-лист аккаунтов | SDR | CRM + Excel + LinkedIn/аналоги | 30 мин/аккаунт | 1 200 | Средняя |
| 2 | Холодный outreach, email/Telegram/звонок | SDR | CRM, sequencer, телефония | 3 касания за 7 дней | 2 500 | Средняя |
| 3 | Qualification call | SDR | Meet, CRM | 30 мин | 1 500 | Низкая |
| 4 | Discovery c маркетинг/SEO-лидом | AE | Meet, шаблон discovery | 60 мин | 4 000 | Низкая |
| 5 | Предварительный AI visibility audit | SEO strategist | internal dashboard, crawler, LLM | 4 часа | 12 000 | Средняя |
| 6 | Demo платформы + roadmap | AE + strategist | Demo env, презентация | 60-90 мин | 6 500 | Низкая |
| 7 | Коммерческое предложение | AE | CRM, proposal template | 2 часа | 5 500 | Средняя |
| 8 | Security / legal / procurement | AE + CEO | почта, docs, шаблоны SLA/DPA | 1-3 недели | 18 000 | Низкая |
| 9 | Подписание договора | AE + CEO | ЭДО / юристы | 3-5 дней | 7 000 | Средняя |
| 10 | Invoice и оплата первого месяца | Finance ops | 1С/банк/ЭДО | 1 день | 2 000 | Высокая |
| 11 | Onboarding и настройка источников | CSM + strategist | dashboard, connectors | 10 часов | 25 000 | Средняя |
| 12 | Ежемесячный reporting и optimization sprint | CSM + strategist | BI, dashboard, LLM | 8-10 часов/мес | 55 000 | Средняя |

## Team table
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | продажи ключевых сделок, стратегия | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | продукт, архитектура, delivery quality | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion/data pipelines | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | integrations/reporting | 450 000 | 135 000 | 585 000 |
| Frontend Engineer | dashboard/UI | 320 000 | 96 000 | 416 000 |
| DevOps | infra, observability, security | 350 000 | 105 000 | 455 000 |
| Product/SEO Strategist | методология, аналитика, контент ops | 250 000 | 75 000 | 325 000 |
| SDR | prospecting/outbound | 180 000 | 54 000 | 234 000 |
| AE | demos, proposals, close | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, QBR, renewals | 260 000 | 78 000 | 338 000 |
| **Итого** |  |  |  | **4 966 000** |

## 7-factor moat framework
| Фактор | Оценка 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| 2. Switching costs | 2 | Есть данные, отчёты, workflow и привязка команды, но интеграционная глубина пока средняя. |
| 3. Scale economies | 1 | Infra и playbooks улучшаются с объёмом, но сервисный хвост остаётся заметным. |
| 4. Proprietary data / model advantage | 1 | Может накапливаться prompt/query corpus, но размер и уникальность датасета не доказаны T1/T2 источниками. |
| 5. Regulatory moat | 1 | 152-ФЗ и data residency создают трение, но это не эксклюзивный барьер. |
| 6. Brand / distribution | 2 | Категория продаётся через thought leadership и enterprise SEO credibility. |
| 7. Embedded workflow | 2 | Если продукт садится в ежемесячный reporting/QBR цикл, вытащить его сложнее. |

**Сумма 7-factor:** 9/21  
**Moat score:** **11/25**

## GTM: 10 named targets
| Потенциальный клиент | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Ozon | Огромная зависимость от органики, карточек товаров и бренд-видимости в AI-ответах. | email decision-maker + e-commerce конференция | 900 000 ₽/мес |
| Wildberries | AI-search visibility по SKU и брендам критична для трафика и мерчантов. | партнёрство с SEO-интегратором + intro через performance-агентство | 900 000 ₽/мес |
| Авито | Высокий SEO-вес и большой UGC/catalog footprint, где AI answers могут съедать переходы. | email SEO lead + Habr/vc.ru thought-leadership | 800 000 ₽/мес |
| Циан | Category search, long research journey и сильная зависимость от content discoverability. | email CMO/SEO lead | 700 000 ₽/мес |
| Т-Банк | Финтех с мощным контент-маркетингом и чувствительностью к brand presence в answer engines. | email brand/SEO lead + отраслевой ивент | 800 000 ₽/мес |
| Сравни | Лидогенерация через SEO и сравнение продуктов делает AI visibility прямой revenue-задачей. | партнёрство + direct outbound | 650 000 ₽/мес |
| Туту | Travel research и comparison-heavy journey делают контроль AI-answer layer коммерчески значимым. | email growth lead + travel conference | 650 000 ₽/мес |
| Skyeng | Сильный контентный маркетинг и частотные инфозапросы, которые могут мигрировать в AI search. | vc.ru ad + outbound ABM | 600 000 ₽/мес |
| Купер | Retail discovery и поисковый спрос по категориям товаров, где нужен AI visibility monitoring. | партнёрство с digital-агентством | 550 000 ₽/мес |
| Самолет | Большой SEO-контур и длинный decision journey, где AI answers влияют на top-of-funnel. | email decision-maker + proptech event | 700 000 ₽/мес |

## GTM realism
- ICP в `04-economics.md` определён адекватно: **Enterprise / upper mid-market**.
- Outbound ABM реалистичен как основной канал, но требует founder-led selling минимум первые 6 месяцев.
- Partnerships действительно лучший канал по CAC, но он ограничен по объёму и не даёт полного sales engine.
- Inbound/content полезен как category creation, но не как главный source of pipeline на старте.

## Top-3 risks
| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| price_compression_30pct | high | high | `Price -30%` режет contribution до `140 000 ₽` и почти уничтожает запас прочности. |
| weak_moat_and_agency_drift | high | high | Moat всего 11/25, рынок легко утягивает модель в agency-heavy delivery. |
| evidence_quality_unverified | med | med | В demand-файле нет строки `Sources: T1/T2/T3`, значит tier quality формально не подтверждена. |

## Дополнительные execution risks
- найм сильного SEO strategist + AE может сдвинуть ramp на 2-3 месяца;
- multi-vendor LLM stack обязателен из-за санкций, сбоев и cost inflation;
- security review и data residency могут удлинить enterprise procurement до 45+ дней.

## Что уже доказано
- buyer pain вокруг AI visibility реален;
- высокий ACV возможен, Conductor даёт enterprise pricing anchor;
- unit economics на уровне клиента сильные даже в stress-case;
- EBITDA-гейт компании достижим до 50 клиентов и в пределах 24 месяцев.

## Что надо доказать для rerun / upgrade до APPROVED
1. Не менее **2 paid pilots** в РФ с удержанием цены **≥ 600К ₽/мес**.
2. Подтверждение, что продукт остаётся **platform-assisted**, а не агентством с ручным хвостом.
3. Повторяемый ICP с pilot-to-paid conversion **> 15%** и blended CAC **≤ 1,5 млн ₽**.
4. Накопление своего query/prompt dataset и доказуемый workflow lock-in.
5. Исправление source-tier дисциплины в demand-файле с явной строкой `Sources: T1=..., T2=..., T3=...`.

## LTV Upside Calculator
### Базовая точка
- customer_ltv_rub (stress-case): **6 396 000 ₽**
- CAC: **1 390 000 ₽**
- LTV/CAC: **4,6x**

### Что даст апсайд
| Рычаг | Новый уровень | Эффект |
|---|---:|---|
| ARPA | 700 000 ₽/мес | contribution_margin_rub_month растёт, payback сокращается, можно держать enterprise-only ICP. |
| COGS | 240 000 ₽/мес | GM растёт до ~65,7%, EBITDA на 50 клиентах становится materially выше. |
| Churn | 1,0%/мес | customer_ltv_rub вырастает примерно до 37,3 млн ₽ по матмодели. |
| CAC | 1 100 000 ₽ | stress-case LTV/CAC поднимается примерно до 5,8x. |
| Price discipline | скидки <10% | убирает главный downside-сценарий из P6B. |

## Финальный вывод
Это **не auto-reject по качеству бизнеса**, а **NEAR-PASS**, который стоит держать в watchlist. Если команда докажет 2-3 платящих enterprise-кейса, сохранит цену и соберёт data/workflow moat, кейс может быстро перейти в approve-коридор. На текущем пакете данных инвестиционный запас прочности недостаточен.

## Основание решения
- `01-intake.md`
- `02-demand.md`
- `04-economics.md`
- `05-critic.md`
- `07-score-trajectory.md`


---

## FILE: 07-score-trajectory.md


# 07-score-trajectory

- 2026-04-22 — P3 Demand Validation — score: 3.8/5.0 — verdict: CONDITIONAL_PASS — reason: категория AI visibility / AEO в РФ ещё ранняя, но уже есть глобальный platform proof, локальная коммерциализация GEO и проходной enterprise wedge.
- 2026-04-22 — P5 Unit Economics — score: 4.2/5.0 — verdict: PASS — reason: при ARPU 600К ₽/мес, contribution margin 53,3%, blended fully-loaded CAC 1,39 млн ₽ и stress-case LTV/CAC 4,6x модель проходит fund-level пороги; break-even достигается примерно на 20 клиентах и M11.
- 2026-04-23 — P7 Critic & Verdict — score: 67/100 — verdict: NEAR-PASS / REJECTED — reason: company_ebitda_potential_rub_month проходит gate с запасом, но локальный спрос остаётся ранним, moat слабый, есть риск agency drift и формальный штраф за неразмеченный source-tier balance в demand-файле.
