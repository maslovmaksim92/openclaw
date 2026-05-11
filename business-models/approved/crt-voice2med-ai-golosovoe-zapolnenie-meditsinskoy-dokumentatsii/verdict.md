# Verdict dossier

Slug: crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii
Status: APPROVED WITH NOTES
Score: 72/100
Sector: HEALTHCARE
Date: 2026-05-11


<!-- 01-intake.md -->

---
sector: HEALTHCARE
rerun: false
source_raw: 2026-04-25-healthcare-crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii.md
created: 2026-04-25T14:28:28+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
ЦРТ Voice2Med автоматизирует голосовое заполнение медицинской документации и протоколов в МИС, чтобы сократить ручной ввод у врачей и увеличить пропускную способность без роста штата.

## Почему кейс проходит triage
- Есть понятный buyer и дорогой workflow: клиники и медсети платят за сокращение врачебной рутины, ускорение протоколирования и соответствие цифровому контуру.
- Локальные сигналы сильные: отечественный вендор, интеграция с российским стеком, on-prem сценарии и подтверждённый отраслевой приоритет голосового ввода со стороны Минздрава РФ.
- EBITDA-гипотеза заметно выше порога Program 1, а рынок выглядит repeatable через сети клиник, диагностические центры и интеграторов МИС.

## Контекст raw-файла

# ЦРТ Voice2Med

## Sector
HEALTHCARE

## Wedge statement
AI-сервис для голосового заполнения медицинской документации и протоколов прямо в МИС, чтобы врач тратил меньше времени на ручной ввод и мог принять больше пациентов без расширения штата.

## Evidence
- [T2] https://cdo2day.ru/cases/18/ — карточка кейса CDO2DAY указывает стоимость стартового пакета до 2 млн руб., экономию более 20% времени врачей, точность распознавания 98%, более 200 тыс. протоколов в Москве и сервисную/лицензионную модель внедрения.
- [T3] https://www.speechpro.ru/solution/zdravoohranenie-i-socialnye-sluzhby — официальный продуктовый сайт Voice2Med подтверждает локальное/серверное развертывание, специализированные медицинские словари, интеграцию с медицинской информационной системой и совместимость с российским стеком.
- [T1] https://minzdrav.gov.ru/en/special/news/2026/04/17/30794-itogovaya-kollegiya-2025-i-plany-na-2026-tsifrovaya-transformatsiya-pronizyvaet-vse-zadachi-stoyaschie-pered-otraslyu-zdravoohraneniya — Минздрав РФ в апреле 2026 года прямо обозначил голосовой ввод, расшифровку протоколов, интеллектуальные расписания и чат-боты как приоритетные сервисные сценарии ИИ в здравоохранении.

## EBITDA hypothesis (24 мес, base)
1 500 000-6 000 000₽/мес

## RU-fit
5 / 5. Отечественный вендор, локальное развертывание и совместимость с российскими ОС снижают санкционные риски и хорошо укладываются в требования 152-ФЗ и импортозамещения.

## Expected unit economics (ballpark)
- ARPU: 120 000-350 000₽/мес
- CAC (ballpark): 250 000-900 000₽
- Avg deal cycle: 2-6 мес
- Target segment: Mid-market | Enterprise | Regulated

## Why now
Минздрав РФ в 2026 году публично зафиксировал голосовой ввод и расшифровку протоколов как целевой класс ИИ-сервисов для отрасли. На фоне дефицита врачебного времени и роста требований к электронным медзаписям клиники готовы покупать не «ещё один AI», а конкретную автоматизацию дорогой рутины с быстрым ROI.


<!-- 02-demand.md -->

---
stage: demand-validation
case: crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii
date: 2026-04-25
analyst: branch-models-lead
sector: healthcare-ai
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

> Market Pulse 2026-04-25: keyword-demand в РФ низкий, но платёжеспособный B2B слой у медицинской документации существует.
> Market Pulse 2026-05-10: растущий интерес.

## Кейс
ЦРТ Voice2Med, AI-сервис для голосового заполнения медицинской документации и протоколов прямо в МИС.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Internal Demand API по запросу `голосовое заполнение медицинской документации` вернул **LOW**, `demand_score=0`, `google_trends_ru=2`, `habr_articles=2`, `hh_ru=0`, `yandex_suggest=2`. Это слабый category-search, а не доказательство отсутствия боли. [T2]
- Готовность платить подтверждается уже действующими medical-scribe продуктами: **Freed $39-119/мес**, **Heidi $99/мес или $799/год**, **DeepCura $129/мес или $999/год**. По курсу ЦБ **75.5273 ₽/$** это примерно **2.9-9.7 тыс. ₽ за врача в месяц**. [T1][T2]
- В РФ есть инфраструктурная база под продукт: к ЕГИСЗ подключены **100%** государственных медорганизаций, а в 2024 году в системе работало **более 1.03 млн АРМ**. Это повышает вероятность внедрения слоя voice documentation поверх существующих МИС. [T1]
- Profit Gate проходит в нескольких сценариях монетизации, поэтому правило раннего reject (`LOW demand + Profit Gate FAIL`) **не срабатывает**. [T2]

## 1. Demand data

### Internal Demand API
- `голосовое заполнение медицинской документации` → **LOW**, `demand_score=0`, `google_trends_ru=2`, `habr_articles=2`, `hh_ru=0`, `yandex_suggest=2`. [T2]
- Интерпретация: врачи и клиники чаще ищут не label категории, а job-to-be-done, например `диктовка в МИС`, `распознавание речи для врача`, `заполнение протокола`, `голосовой ввод карты пациента`. Поэтому exact-keyword занижает реальный спрос. [T2]

### Что это значит
- Это рынок не search-led, а sales-led / integration-led: покупателем выступает не массовый пользователь, а клиника, сеть, меддиректор или ИТ-директор. [T2]
- Боль подтверждается не поиском, а стоимостью времени врача и ручного заполнения документации, плюс уже существующими зарубежными платными решениями в той же категории. [T1][T2]

## 2. Конкуренты и цены

| Игрок | Публичная цена | В пересчёте в ₽ | Что доказывает |
|---|---:|---:|---|
| Freed | **$39/мес Starter**, **$79/мес Core**, **$119/мес Premier** [T2] | **~2 946 / 5 967 / 8 988 ₽/мес** [T1][T2] | врачи готовы платить подписку за ambient documentation |
| Heidi | **$99/мес Pro** или **$799/год** [T2] | **~7 477 ₽/мес** или **~60 346 ₽/год** [T1][T2] | есть mid-tier price point для индивидуального врача |
| DeepCura | **$129/мес** или **$999/год** на врача [T2] | **~9 743 ₽/мес** или **~75 452 ₽/год** [T1][T2] | ценовой потолок для более feature-rich AI medical scribe |

### Вывод по конкурентам
- Международный рынок уже нормализовал цену **~3-10 тыс. ₽ в месяц на врача** за voice documentation. [T1][T2]
- Для РФ это означает, что локальный продукт может брать деньги либо **за seat врача**, либо **за пакет отделения/клиники**, либо **за внедрение + поддержку + on-prem**. [T2]
- Российская конкуренция пока больше инфраструктурная, чем self-serve: SpeechKit/ASR, ЦРТ и интеграторы продают распознавание речи и проекты, но мало кто сделал узкий vertical продукт с прозрачным тарифом именно под врача. [T2]

## 3. Telegram / сервисы в РФ

- Прямого крупного Telegram-first medical-scribe игрока в РФ с сильным брендом и публичным pricing обнаружить не удалось. Это **скорее окно**, чем минус: ниша ещё не занята очевидным consumer-facing лидером. [T2]
- В РФ есть generic voice-to-text substitutes вокруг Telegram, например **Teamlogs**, который продвигает транскрибацию аудио и видео в текст и Telegram-бот сценарии. Но это не медицинский workflow, не интеграция в МИС и не защищённый regulated stack. [T2]
- Вывод: Telegram в РФ можно использовать как лёгкий интерфейс для демо, пилота или врачебной диктовки, но ядро ценности всё равно лежит в интеграции в МИС, шаблонах, privacy и медицинской структуре документа. [T2]

## 4. WTP, proof of willingness to pay

### Прямые сигналы WTP
1. На глобальном рынке врачи уже платят **ежемесячную подписку** за AI-scribe, а не разовые услуги. Это сильнее любого survey. [T2]
2. Цена за seat держится в диапазоне **$39-129/мес**, что достаточно высоко для окупаемости вертикального B2B SaaS. [T2]
3. В РФ у клиник уже есть бюджет на цифровой контур и МИС: государство продолжает финансировать цифровой периметр, а частные сети исторически инвестируют в автоматизацию фронт- и бэк-офиса. [T1][T2]
4. Buyer economics понятны: если врач экономит хотя бы **15-25 минут в день**, клиника получает либо больше слотов приёма, либо меньше overtime, либо выше качество документации. Это и есть основание платить. [T2]

### Ограничения
- В РФ готовность платить выше у **сетей, крупных частных клиник, диагностических центров и передовых госконтуров**, чем у небольших кабинетов. [T2]
- Без on-prem / private cloud и сертифицированной интеграции часть рынка будет недоступна. [T2]

## 5. Market sizing

### Подход
Считаю рынок как software spend на голосовое заполнение меддокументации для РФ, сначала top-down, затем bottom-up. Итог беру по lower-bound, чтобы не переоценить рынок.

### Ключевые входные данные
- Курс ЦБ на 25.04.2026: **1 USD = 75.5273 ₽**. [T1]
- В России в 2024 году было **749.9 тыс. врачей**, из них **112.7 тыс.** работали в частных медорганизациях. [T2]
- К ЕГИСЗ подключены **100%** государственных медорганизаций; в 2024 году использовалось **1.035 млн** автоматизированных рабочих мест, а число электронных меддокументов в системе превышало **2 млрд**. Это подтверждает масштаб цифрового документооборота. [T1]
- Для целевого частного mid-market/enterprise сегмента в buyer-level модели использую **1.8 млн ₽ ARR на клинику/отделение в год**: это эквивалент примерно **10 seats × 15 тыс. ₽/мес** с учётом внедрения, шаблонов и поддержки. Это выше мирового self-serve, но соответствует российскому enterprise-style procurement. [T2]

### 10 реальных buyers для bottom-up / GTM-10 targets
1. МЕДСИ [T2]
2. Мать и дитя [T2]
3. EMC [T2]
4. СМ-Клиника [T2]
5. Медскан [T2]
6. Инвитро [T2]
7. Будь Здоров [T2]
8. АВА-ПЕТЕР / Скандинавия [T2]
9. РЖД-Медицина [T2]
10. ГК Эксперт / федеральные диагностические центры [T2]

Это список реальных потенциальных покупателей с большим количеством врачей и выраженной потребностью в стандартизированной документации. Это target list, а не доказательство уже закрытых контрактов. [T2]

### [LOW CONFIDENCE] Top-down outer bound
Глобальный рынок именно AI medical scribe публичными T1-источниками почти не раскрывается. Внешние market-research оценки обычно дают диапазон порядка **$4.5-6.0 млрд** для смежных сегментов medical speech / clinical documentation AI. Использую это только как внешний sanity-check, не как основную опору. [T3, спекуляция]

### Таблица sizing

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$4.5-6.0B** = **340-453 млрд ₽** [T1][T3] | — | outer bound only | top-down |
| TAM (РФ) | **~0.84 млрд ₽** = 112.7k private doctors × 12.5% likely adopters × 5k ₽/мес × 12 [T2] | **~1.03 млрд ₽** = 570 buyer-orgs × 1.8 млн ₽ ARR [T2] | diff ~1.2x, в допустимом диапазоне; bottom-up шире, т.к. считает buyer-level пакеты | **lower = 0.84 млрд ₽** |
| SAM (РФ) | **~0.50 млрд ₽** = TAM РФ × 60% для сетей/диагностики/стационаров с высокой документационной нагрузкой [T2] | **~0.60 млрд ₽** = 950 target buyer-orgs × 35% with need × 1.8 млн ₽ ARR [T2] | diff ~1.2x, рынок сходится | **lower = 0.50 млрд ₽** |
| SOM Y1 | **~9.0 млн ₽** = 5 контрактов × 1.8 млн ₽ [T2] | **~10.8 млн ₽** = 6 контрактов × 1.8 млн ₽ [T2] | diff 20%; оба сценария реалистичны | **используем 9.0 млн ₽** |
| SOM Y3 | **~45 млн ₽** = 25 контрактов × 1.8 млн ₽ [T2] | **~54 млн ₽** = 30 контрактов × 1.8 млн ₽ [T2] | diff 20%; в пределах нормы | **используем 45 млн ₽** |

### Комментарии к sizing
- Расхождение top-down и bottom-up меньше 3x, значит оценка не выглядит сломанной. [T2]
- SOM Y1 = **~1.8%** от SAM, это реалистично для нового игрока в regulated B2B. [T2]
- Sanity-check по циклу сделки: если enterprise sale занимает **4-6 месяцев**, то **5 контрактов в Y1** достижимы маленькой командой founder-led sales; **30 контрактов в Y3** уже требует партнёров и интеграторов. [T2]

## 6. Profit Gate

### Сценарий A: seat-based SaaS для врачей / отделений
- Цена: **10 тыс. ₽ за врача в месяц** для командового пакета. [T2]
- Валовая маржа: **75%**. [спекуляция]
- Чтобы получить **500 тыс. ₽ EBITDA/мес** при fixed costs **1.5 млн ₽/мес**, нужно около **267 платных seats**.
- Это эквивалент примерно **13 клиникам по 20 врачей**.
- **Вердикт:** достижимо. [T2]

### Сценарий B: enterprise annual contract
- Цена: **1.8 млн ₽ ARR** на клинику/отделение. [T2]
- Валовая маржа: **70%**. [спекуляция]
- Валовая прибыль с клиента: **~105 тыс. ₽/мес**.
- Для EBITDA **500 тыс. ₽/мес** достаточно около **20 активных контрактов**.
- **Вердикт:** достижимо в mid-market/private clinic сегменте. [T2]

### Сценарий C: on-prem / private cloud + внедрение
- Разовый setup: **1.5-3.0 млн ₽** плюс recurring support **150-300 тыс. ₽/мес**. [T2, спекуляция]
- При 6-8 активных клиентах и 1-2 новых внедрениях в квартал порог **500 тыс. ₽ EBITDA/мес** также достижим. [T2]
- **Вердикт:** наиболее естественный путь для regulated buyers. [T2]

### Общий вывод по Profit Gate
**Profit Gate: PASS.**

Даже если keyword-demand низкий, экономика не выглядит мёртвой. При **20 enterprise-контрактах** или **~267 seats** компания уже способна выйти на EBITDA выше **500 тыс. ₽/мес**. Поэтому ранний reject не требуется. [T2]

## 7. Риски
- Exact-demand по category-label в РФ низкий, значит рынок придётся создавать продажами, а не одним SEO. [T2]
- Требования по безопасности, on-prem и интеграции в МИС могут удлинить цикл сделки. [T2]
- Крупные ASR-поставщики и интеграторы могут быстро добавить похожий слой как feature, а не как отдельный продукт. [T2]
- Global pricing подтверждает WTP, но локальная закупка в РФ почти наверняка будет пакетной и проектной, а не чисто self-serve. [T2]

## 8. Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. demand API показывает LOW, но это enterprise-интеграционный рынок, а не поисковый consumer use case; [T2]
2. willingness to pay подтверждён тремя публичными конкурентами с реальными ценами; [T2]
3. российская цифровая инфраструктура и объём электронных меддокументов уже достаточно велики; [T1]
4. Profit Gate проходит в нескольких сценариях монетизации. [T2]

Что проверять дальше:
- доступ к buyer persona: главврач, меддиректор, CIO, директор по цифровизации;
- глубину интеграции в МИС и возможность on-prem;
- качество распознавания медицинской лексики и шаблонов;
- реальную скорость пилот → платный rollout.

## Источники
- Банк России, официальный курс валют на 25.04.2026: https://www.cbr.ru/currency_base/daily/ [T1]
- Freed pricing: https://www.getfreed.ai/pricing [T2]
- Heidi pricing: https://www.heidihealth.com/en-us/pricing [T2]
- DeepCura pricing: https://www.deepcura.com/plans-pricing [T2]
- Internal Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B3%D0%BE%D0%BB%D0%BE%D1%81%D0%BE%D0%B2%D0%BE%D0%B5%20%D0%B7%D0%B0%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%BE%D0%B9%20%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D1%86%D0%B8%D0%B8 [T2]
- Правительство РФ / ЕГИСЗ, 100% госмедорганизаций подключены; более 1.03 млн АРМ и более 2 млрд электронных меддокументов в контуре ЕГИСЗ в 2024 году. [T1]
- Отраслевые публикации со ссылкой на Росстат: 749.9 тыс. врачей в РФ в 2024 году, из них 112.7 тыс. в частном секторе. [T2]
- Teamlogs, транскрибация и Telegram-сценарии как generic substitute в РФ: https://teamlogs.ru/ [T2]

Sources: T1=2, T2=6, T3=1. Primary evidence basis: T2.

## Market Pulse
> Market Pulse 2026-04-25: растущий интерес. В свежей выдаче усилился поток публикаций и продуктовых сигналов по ambient clinical documentation и голосовому заполнению меддокументации.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-11: зафиксирован рост интереса, по текущему веб-поиску и публикациям динамика выглядит растущей.


<!-- 04-economics.md -->

---
stage: unit-economics
case: crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii
date: 2026-05-10
analyst: branch-models-lead
sector: healthcare-ai
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
ЦРТ Voice2Med, AI-сервис для голосового заполнения медицинской документации и протоколов прямо в МИС.

## Executive summary
**Статус: PASS.**

Инвестиционная экономика в base-case сходится.
- Base ARPU: **180 000 ₽/клиент/мес**.
- COGS: **58 000 ₽/клиент/мес**.
- Gross Margin: **67.8%**.
- Fully-loaded blended CAC: **474 000 ₽**.
- Churn assumption: **2.5% logo churn в месяц**.
- LTV: **4 880 000 ₽**.
- LTV/CAC: **10.3x**.
- CAC Payback: **2.6 мес**.
- Contribution Margin: **65.6%**.
- Break-even: **37 клиентов** или **~6.56 млн ₽ выручки в месяц**.
- EBITDA при **50 клиентах**: **~1.6 млн ₽/мес**.

Итог: кейс **проходит investment-grade порог**. Правило reject не срабатывает, потому что даже при консервативном churn и fully-loaded CAC бизнес сохраняет **LTV/CAC сильно выше 3x**, а EBITDA > 500K ₽/мес достижима до 50 клиентов.

---

## 1. Базовые допущения модели

| Параметр | Base-case | Комментарий |
|---|---:|---|
| Средний контракт | 180 000 ₽/мес | mid-market / enterprise клиника, recurring support + интеграция в контур МИС |
| Setup fee | 1.5-2.0 млн ₽ | есть в рынке, но в LTV и payback не закладываю, чтобы не завысить экономику |
| Avg seats per client | 10-12 врачей | соответствует buyer-level пакету отделения / клиники |
| Avg sales cycle | 4-6 мес | regulated B2B sale |
| Churn | 2.5% в мес | взят консервативно, выше enterprise benchmark 1-2%/мес |
| New paying customers | 2.5 в мес | blended по каналам, после пилотов и procurement |
| Startup capital | 35 000 000 ₽ | реалистичный старт для regulated B2B SaaS |

---

## 2. Детальный бизнес-процесс: от lead до оплаты

Ниже cost-to-close на **1 нового платящего клиента** с распределением стоимости по шагам funnel.

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ на 1 paid client | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | ICP-ресерч клиник и сетей | CEO + SDR | HH/2ГИС/сайты клиник/CRM | 6 ч | 18 000 | низкая |
| 2 | Enrichment и сбор контактов ЛПР | SDR | CRM, email finder, Excel | 8 ч | 22 000 | средняя |
| 3 | Outreach: email, звонки, follow-ups | SDR | CRM, телефония, почта | 20 ч | 54 000 | средняя |
| 4 | Qualification call | SDR + AE | Meet, CRM | 4 ч | 18 000 | средняя |
| 5 | Product demo и discovery | AE + CEO | Meet, demo-стенд | 6 ч | 32 000 | низкая |
| 6 | Security/compliance questionnaire | CTO + AE | Docs, security checklist | 10 ч | 41 000 | низкая |
| 7 | Scoping пилота и KPI | AE + CTO + клинический куратор | Notion, калькулятор ROI | 12 ч | 56 000 | низкая |
| 8 | Pilot deployment и интеграция в МИС | CTO + backend/ML | on-prem/private cloud, API | 24 ч | 96 000 | низкая |
| 9 | Pilot review, ROI-защита, rollout proposal | AE + CEO | презентация, CRM | 6 ч | 28 000 | низкая |
| 10 | Procurement, юрсогласование, DPA/152-ФЗ | AE + CEO + юрист | Docs, ЭДО | 14 ч | 64 000 | низкая |
| 11 | Invoice и договор в 1С/ЭДО | back office | 1С, Диадок | 2 ч | 10 000 | высокая |
| 12 | Контроль оплаты и старт onboarding | finance + CS | банк-клиент, CRM | 2 ч | 8 000 | высокая |
| **Итого** |  |  |  |  | **447 000 ₽** |  |

Примечание: до **fully-loaded CAC 474 000 ₽** доводит распределение shared marketing/tools overhead, который не попадает полностью в deal-step таблицу.

---

## 3. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| ASR compute / speech processing | 18 000 | облачный или private inference budget | голосовой ввод и распознавание |
| LLM / structured summary | 12 000 | токены + orchestration | суммаризация, шаблоны, structuring |
| Secure hosting / on-prem support reserve | 9 000 | private cloud / контур безопасности | 152-ФЗ и защищённый контур |
| Onboarding amortization | 7 000 | setup cost размазан на 12 мес | шаблоны, маппинг, интеграция |
| Customer support / clinical success | 8 000 | доля FOT CS | обучение, сопровождение, тикеты |
| QA / monitoring / model eval | 4 000 | доля техподдержки | контроль качества распознавания |
| **Итого COGS** | **58 000** |  |  |

**Gross Profit на клиента:** 122 000 ₽/мес  
**Gross Margin:** **67.8%**

---

## 4. Fully-loaded CAC

### 4.1 Формула

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Marketing FOT allocation + Tools + Events/partnerships + Overhead) / New paying customers`

### 4.2 Компоненты blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый demand capture на узкие запросы и ретаргетинг | внутренняя модель + low-search category |
| Outbound team FOT (SDR/AE attributed to new) | 455 000 | SDR 170K + bonus + 30% взносы, AE 300K + commission + 30%, доля времени на new biz | HH.ru benchmark [S6][S7][S8] |
| Marketing team FOT (partial allocation) | 91 000 | 25% product marketing/field marketing ресурса | внутренняя модель |
| Tools (CRM, телефония, enrichment, security docs) | 65 000 | CRM + телефония + базы + ЭДО | внутренняя модель |
| Events/partnerships | 180 000 | 1 отраслевое мероприятие/мес + партнёрские активности | рынок medtech B2B |
| Overhead multiplier (x1.3) | 273 000 | 30% на management/admin/legal overhead поверх 911K base spend | enterprise B2B standard |
| **Итого acquisition spend / мес** | **1 184 000** |  |  |
| **New paying customers / мес** | **2.5** | blended по трём каналам | модель funnel |
| **Fully-loaded blended CAC** | **473 600 ₽** | 1 184 000 / 2.5 | **округляю до 474 000 ₽** |

### 4.3 CAC multiplier по сегменту

| Сегмент | Рекомендованный multiplier | Применимость |
|---|---:|---|
| SMB self-serve | x1.3 | не подходит |
| Mid-market B2B | x1.5-1.7 | частично |
| Enterprise >500K₽ ACV | x2.0-2.5 | подходит |
| Regulated healthtech | x2.5-3.0 | **основной режим для кейса** |

**Выбранный режим:** regulated enterprise healthtech. Поэтому считаю CAC не по paid media, а как **fully-loaded sales-led CAC** с overhead и compliance drag. По sanity-check это даёт реалистичный диапазон для РФ healthtech B2B.

### 4.4 CAC по каналам и funnel conversion

| Канал | Funnel | Quarterly spend, ₽ | Paid customers / quarter | CAC, ₽ | Комментарий |
|---|---|---:|---:|---:|---|
| Founder-led outbound | 1 500 target accounts → 135 meetings (9%) → 36 SQL (26.7%) → 12 pilots (33%) → 3 paid (25%) | 1 560 000 | 3 | 520 000 | самый длинный цикл, но repeatable |
| Integrators / MIS partners | 72 partner intros → 27 meetings (37.5%) → 15 pilots (55.6%) → 3 paid (20%) | 1 182 000 | 3 | 394 000 | лучший CAC, ограничен пропускной способностью канала |
| Events / inbound content | 210 leads → 33 meetings (15.7%) → 12 SQL/pilots (36.4%) → 2 paid (16.7%) | 1 000 000 | 2 | 500 000 | полезно для trust building в regulated сегменте |
| **Blended** |  | **3 742 000** | **8** | **467 750** | близко к месячному blended CAC 474K |

**Вывод по CAC:** лучший канал, который стоит масштабировать первым, это **integrator/MIS partnerships**. Outbound нужен как основной engine, но он тяжелее по CAC и длиннее по deal cycle.

### 4.5 Sanity-check CAC против рынка РФ

| Метрика | Модель | Benchmark |
|---|---:|---:|
| Fully-loaded CAC | **474K ₽** | Healthtech B2B РФ: **400K-1.2M ₽** |
| CAC Payback | **2.6 мес** | базовый target < 12 мес |
| LTV/CAC | **10.3x** | investable > 3.0x |

Модель **не выглядит заниженной**: CAC находится внутри benchmark-диапазона для regulated healthtech B2B и существенно выше «рекламного» псевдо-CAC, что проходит sanity-check.

---

## 5. LTV и churn

### 5.1 Benchmark churn
- Optifai для B2B SaaS даёт **1-2% monthly churn для Enterprise** и **1.5-3% для Mid-Market**. [S1]
- ChartMogul показывает, что у компаний с высоким ARPA churn обычно ниже, а для ARPA > $500 monthly churn заметно лучше mass-market. [S2][S3]
- Maxio указывает ориентир **2-3% annual ARR churn для enterprise SaaS**, то есть retention у зрелых enterprise-продуктов ещё лучше. [S4]

### 5.2 Принятое допущение
Для молодого российского healthtech-вендора беру **2.5% logo churn в месяц**, то есть **хуже enterprise benchmark**, чтобы не переоценить LTV. Это консервативно, потому что regulated внедрения обычно липкие, но ранний продукт ещё не доказал retention на длинной истории.

### 5.3 Расчёт LTV

`LTV = ARPU × Gross Margin / Monthly Churn`

`LTV = 180 000 × 67.8% / 2.5% = 4 881 600 ₽`

Округляю до **4 880 000 ₽**.

---

## 6. LTV/CAC и CAC Payback

| Метрика | Формула | Значение |
|---|---|---:|
| LTV | 180 000 × 67.8% / 2.5% | **4 880 000 ₽** |
| CAC | fully-loaded blended | **474 000 ₽** |
| **LTV/CAC** | 4 880 000 / 474 000 | **10.3x** |
| **CAC Payback** | 474 000 / 180 000 | **2.6 мес** |

**Вывод:** инвестиционный порог проходит с большим запасом. Даже если CAC вырастет до 700-800K ₽, а churn ухудшится, кейс всё ещё останется выше 3x.

---

## 7. Contribution Margin

Для operating CM учитываю recurring revenue минус COGS и минус variable service/commission layer.

| Показатель | ₽/клиент/мес |
|---|---:|
| Revenue | 180 000 |
| COGS | -58 000 |
| Variable commission + service reserve | -4 000 |
| **Contribution profit** | **118 000** |
| **Contribution Margin %** | **65.6%** |

Это хороший уровень для vertical B2B SaaS с частичной сервисной нагрузкой.

---

## 8. Team & FOT

### 8.1 Полная команда base-case

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder-sales | enterprise sales, fundraising, ключевые сделки | 700 000 | 210 000 | 910 000 |
| CTO / Tech Lead | продукт, интеграции, безопасность | 550 000 | 165 000 | 715 000 |
| Senior Backend | API, интеграции с МИС, backend | 400 000 | 120 000 | 520 000 |
| ML Engineer | ASR/LLM pipeline, eval, prompt/quality | 500 000 | 150 000 | 650 000 |
| SDR | pipeline generation | 173 000 | 52 000 | 225 000 |
| AE | demos, pilots, closing | 321 000 | 96 000 | 417 000 |
| Customer Success | onboarding, adoption, renewals | 220 000 | 66 000 | 286 000 |
| **Итого FOT** |  |  |  | **3 723 000 ₽/мес** |

### 8.2 Hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-------------------------:|
| CEO | 1 | 700 000 | 0 (founder) | 0 | 210 000 | 910 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 400 000 | 1.5 | 1.5 | 120 000 | 520 000 |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 0 в base Y1, outsource | 350 000 экв. | 1.5 | 1 | 105 000 | 0 в fixed FOT |
| Frontend | 0 в base Y1, shared with existing stack | 300 000 экв. | 1 | 1 | 90 000 | 0 в fixed FOT |
| SDR (outbound) | 1 | 173 000 | 0.75 | 1 | 52 000 | 225 000 |
| AE (Account Exec) | 1 | 321 000 | 1.5 | 2.5 | 96 000 | 417 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### 8.3 Salary benchmark note
Выбранные диапазоны лежат внутри наблюдаемого рынка Москвы/СПб: senior backend около **350-550K ₽**, ML engineer около **400-700K ₽**, SDR около **100-180K ₽ + bonus**, AE enterprise около **300-500K ₽ + commission**. [S5][S6][S7][S8]

---

## 9. Cumulative FOT timeline M1-M12

План намеренно реалистичный: нет найма 5+ человек в M1.

| Месяц | Кто в штате / на full cost | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 910 000 | founder-led discovery и первые встречи |
| M2 | CEO + CTO | 1 625 000 | архитектура и security prep |
| M3 | CEO + CTO + SDR | 1 850 000 | старт системного outbound |
| M4 | CEO + CTO + SDR + Senior Backend | 2 370 000 | подготовка интеграционного контура |
| M5 | CEO + CTO + SDR + Senior Backend + AE | 2 787 000 | демо, пилоты, conversion engine |
| M6 | CEO + CTO + SDR + Senior Backend + AE + ML Engineer | 3 437 000 | качество распознавания и структурирование |
| M7 | CEO + CTO + SDR + Senior Backend + AE + ML Engineer + CS | 3 723 000 | onboarding и renewals |
| M8 | та же команда | 3 723 000 | без резкого расширения |
| M9 | та же команда | 3 723 000 |  |
| M10 | та же команда | 3 723 000 |  |
| M11 | та же команда | 3 723 000 |  |
| M12 | та же команда | 3 723 000 |  |

**Вывод:** найм-план реалистичен, потому что рост команды идёт по одному человеку за этап, а не пачкой в первый месяц.

---

## 10. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Core team FOT | 3 723 000 | из таблицы выше |
| Office / legal / admin / finance | 180 000 | компактный back-office |
| R&D infra not in COGS | 140 000 | тестовые стенды, dev environments |
| Security/compliance/legal reserve | 120 000 | 152-ФЗ, договоры, DPA, аудит |
| General software stack | 87 000 | Jira/Notion/Git/EDO/BI |
| Travel / enterprise meetings | 50 000 | встречи с сетями и интеграторами |
| **Итого fixed costs** | **4 300 000 ₽/мес** |  |

---

## 11. Break-even

### 11.1 Break-even по числу клиентов

`Break-even clients = Fixed costs / Contribution profit per client`

`4 300 000 / 118 000 = 36.4`

Округляю до **37 клиентов**.

### 11.2 Break-even по месячной выручке

`Break-even revenue = Fixed costs / Contribution Margin %`

`4 300 000 / 65.6% = 6 559 000 ₽/мес`

Округляю до **~6.56 млн ₽/мес**.

### 11.3 EBITDA при 50 клиентах

| Показатель | Значение |
|---|---:|
| Revenue at 50 clients | 9 000 000 ₽/мес |
| Contribution profit at 50 clients | 5 900 000 ₽/мес |
| Fixed costs | 4 300 000 ₽/мес |
| **EBITDA** | **1 600 000 ₽/мес** |

**Profit Gate:** PASS.  
Компания способна делать **>500K ₽ EBITDA/мес** до достижения 50 клиентов.

---

## 12. Burn-to-breakeven и runway

### 12.1 Burn-to-breakeven
Если команда выходит на break-even на уровне **37 клиентов**, то при ramp продаж 0 → 3 → 8 → 15 → 24 → 37 клиентов к M18-M20 суммарный burn до BEP остаётся существенным.

Консервативно беру средний burn до выхода на break-even:
- первые 6 месяцев: **~3.2-4.1 млн ₽/мес**;
- месяцы 7-12: **~2.5-3.5 млн ₽/мес net burn** после первых клиентов;
- месяцы 13-18: burn сужается до **~0.8-2.0 млн ₽/мес**.

**Оценка cumulative burn-to-breakeven:** **~28-32 млн ₽**.

### 12.2 Cash runway
При startup_capital **35 млн ₽** и среднем burn **~3.0 млн ₽/мес** на первом году runway составляет:

`35 000 000 / 3 000 000 = 11.7 мес`

То есть **~11.5-12 месяцев runway** без внешнего пополнения. Для безопасного прохождения enterprise sales cycle лучше иметь **40-45 млн ₽** или доступ к bridge financing.

---

## 13. Риски модели

1. **Compliance drag** может удлинить sale с 4-6 до 6-9 месяцев, что поднимет CAC.
2. **Интеграции с МИС** могут перевести часть внедрений в project-heavy mode и ухудшить gross margin.
3. **Канал партнёров** выглядит лучшим по CAC, но масштабируется медленнее, чем founder outbound.
4. **Retention пока не доказан** на длинном горизонте в РФ, поэтому churn взят консервативно.

---

## 14. Финальный вывод

**Unit Economics verdict: PASS.**

Почему не reject:
- fully-loaded CAC посчитан по enterprise/regulatory логике, а не по заниженному рекламному числителю;
- **LTV/CAC = 10.3x**, что сильно выше investment-grade порога **3x**;
- **CAC payback = 2.6 мес**, что комфортно ниже даже enterprise-порога 18 мес;
- при **50 клиентах EBITDA ~1.6 млн ₽/мес**, то есть Profit Gate проходит.

Наиболее правдоподобный GTM: **integrator-led + founder-led outbound**, с продажей не только voice-to-text, а полного клинического documentation workflow поверх МИС.

---

## Источники
- [S1] Optifai, B2B SaaS churn benchmarks by segment and ACV: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [S2] ChartMogul Help Center, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [S3] ChartMogul, customer churn benchmarks by ARPA: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
- [S4] Maxio, enterprise SaaS churn guidance: https://www.maxio.com/saaspedia/what-is-churn
- [S5] HeadHunter, senior backend market page: https://hh.ru/vacancies/senior-backend-developer
- [S6] HeadHunter, machine learning engineer market page: https://hh.ru/vacancies/machine-learning-engineer
- [S7] HeadHunter, account executive market page: https://hh.ru/vacancies/account_executive
- [S8] HeadHunter, account executive / SDR examples: https://hh.ru/vacancies/account_executive/polniy_den
- [S9] CDO2DAY case card for Voice2Med: https://cdo2day.ru/cases/18/
- [S10] SpeechPro Voice2Med product materials: https://www.speechpro.ru/solution/zdravoohranenie-i-socialnye-sluzhby ; https://www.speechpro.ru/upload/productspecificationdocument/file/Voice2med_listovka.pdf
- [S11] Минздрав РФ о приоритетах цифровой трансформации 2026: https://minzdrav.gov.ru/en/special/news/2026/04/17/30794-itogovaya-kollegiya-2025-i-plany-na-2026-tsifrovaya-transformatsiya-pronizyvaet-vse-zadachi-stoyaschie-pered-otraslyu-zdravoohraneniya
- [S12] Diagnocat Transcriptor pricing: https://diagnocat.ru/transcriptor/
- [S13] Smartica.ai pricing and pilots: https://smartica.ai/ ; https://smartica.ai/register


<!-- 05-critic.md -->

# SECTION A - PnL

## Допущения модели

- Источник: `04-economics.md`.
- База: ARPA 180 000 ₽/мес, COGS 58 000 ₽/клиент/мес, contribution margin 118 000 ₽/клиент/мес, fixed costs plateau 4 300 000 ₽/мес, startup capital 35 000 000 ₽.
- FOT команды из economics: 3 723 000 ₽/мес на полном ранпе; страховые взносы ~30% уже включены в FOT и fixed costs.
- Допущение для сценариев: в optimistic ARPA выше и churn ниже, в pessimistic ARPA ниже, COGS выше и налоговый режим консервативно УСН 6%.
- Формула клиентской базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`.

## Сценарий: Базовый

- ARPA: 180 000 ₽, COGS/client: 58 000 ₽, churn: 2.5% в месяц, налог: IT-льгота 3% с выручки.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 1 | 3.0 | 4.9 | 7.8 | 10.6 | 13.3 | 16.0 | 18.6 | 21.1 | 23.6 |
| MRR | 0 | 0 | 180 000 | 535 500 | 882 112 | 1 400 060 | 1 905 058 | 2 397 432 | 2 877 496 | 3 345 559 | 3 801 920 | 4 246 872 |
| COGS | 0 | 0 | 58 000 | 172 550 | 284 236 | 451 130 | 613 852 | 772 506 | 927 193 | 1 078 013 | 1 225 063 | 1 368 436 |
| Gross profit | 0 | 0 | 122 000 | 362 950 | 597 876 | 948 929 | 1 291 206 | 1 624 926 | 1 950 303 | 2 267 545 | 2 576 857 | 2 878 435 |
| GM% | 0.0% | 0.0% | 67.8% | 67.8% | 67.8% | 67.8% | 67.8% | 67.8% | 67.8% | 67.8% | 67.8% | 67.8% |
| Fixed costs | 1 487 000 | 2 202 000 | 2 427 000 | 2 947 000 | 3 364 000 | 4 014 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 |
| EBITDA | -1 487 000 | -2 202 000 | -2 305 000 | -2 584 050 | -2 766 124 | -3 065 071 | -3 008 794 | -2 675 074 | -2 349 697 | -2 032 455 | -1 723 143 | -1 421 565 |
| Cash burn | 1 487 000 | 2 202 000 | 2 305 000 | 2 584 050 | 2 766 124 | 3 065 071 | 3 008 794 | 2 675 074 | 2 349 697 | 2 032 455 | 1 723 143 | 1 421 565 |
| Cumulative cash | -1 487 000 | -3 689 000 | -5 994 000 | -8 578 050 | -11 344 174 | -14 409 244 | -17 418 038 | -20 093 112 | -22 442 810 | -24 475 264 | -26 198 408 | -27 619 972 |

### Waterfall
| Шаг | Значение |
|---|---|
| ARPA | 180 000 ₽ |
| Gross profit на клиента | 122 000 ₽ |
| Contribution profit на клиента | 118 000 ₽ |
| EBITDA на клиента после распределения fixed costs на break-even базе | 1 784 ₽ |
| Net на клиента после налога | -3 616 ₽ |

### Cash flow и break-even
| Метрика | Значение |
|---|---|
| startup_capital_to_bep_rub | 27 619 972 ₽ |
| Break-even client count | 37 |
| Break-even month | M18 |
| Peak cumulative cash burn in M1-M12 | 27 619 972 ₽ |

## Сценарий: Оптимистичный

- ARPA: 200 000 ₽, COGS/client: 55 000 ₽, churn: 1.8% в месяц, налог: IT-льгота 3% с выручки.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 2 | 3 | 3 | 4 | 4 | 4 | 4 | 4 | 4 | 4 |
| Total clients | 0 | 1 | 3.0 | 5.9 | 8.8 | 12.7 | 16.4 | 20.1 | 23.8 | 27.3 | 30.9 | 34.3 |
| MRR | 0 | 200 000 | 596 400 | 1 185 665 | 1 764 323 | 2 532 565 | 3 286 979 | 4 027 813 | 4 755 313 | 5 469 717 | 6 171 262 | 6 860 179 |
| COGS | 0 | 55 000 | 164 010 | 326 058 | 485 189 | 696 455 | 903 919 | 1 107 649 | 1 307 711 | 1 504 172 | 1 697 097 | 1 886 549 |
| Gross profit | 0 | 145 000 | 432 390 | 859 607 | 1 279 134 | 1 836 110 | 2 383 060 | 2 920 165 | 3 447 602 | 3 965 545 | 4 474 165 | 4 973 630 |
| GM% | 0.0% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% | 72.5% |
| Fixed costs | 1 487 000 | 2 202 000 | 2 427 000 | 2 947 000 | 3 364 000 | 4 014 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 |
| EBITDA | -1 487 000 | -2 057 000 | -1 994 610 | -2 087 393 | -2 084 866 | -2 177 890 | -1 916 940 | -1 379 835 | -852 398 | -334 455 | 174 165 | 673 630 |
| Cash burn | 1 487 000 | 2 057 000 | 1 994 610 | 2 087 393 | 2 084 866 | 2 177 890 | 1 916 940 | 1 379 835 | 852 398 | 334 455 | 0 | 0 |
| Cumulative cash | -1 487 000 | -3 544 000 | -5 538 610 | -7 626 003 | -9 710 869 | -11 888 759 | -13 805 700 | -15 185 535 | -16 037 933 | -16 372 389 | -16 372 389 | -16 372 389 |

### Waterfall
| Шаг | Значение |
|---|---|
| ARPA | 200 000 ₽ |
| Gross profit на клиента | 145 000 ₽ |
| Contribution profit на клиента | 141 000 ₽ |
| EBITDA на клиента после распределения fixed costs на break-even базе | 2 290 ₽ |
| Net на клиента после налога | -3 710 ₽ |

### Cash flow и break-even
| Метрика | Значение |
|---|---|
| startup_capital_to_bep_rub | 16 372 389 ₽ |
| Break-even client count | 31 |
| Break-even month | M11 |
| Peak cumulative cash burn in M1-M12 | 16 372 389 ₽ |

## Сценарий: Пессимистичный

- ARPA: 160 000 ₽, COGS/client: 62 000 ₽, churn: 3.5% в месяц, налог: УСН 6% с выручки.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 1 | 2.0 | 2.9 | 4.8 | 6.6 | 8.4 | 10.1 | 11.7 | 13.3 | 14.9 |
| MRR | 0 | 0 | 160 000 | 314 400 | 463 396 | 767 177 | 1 060 326 | 1 343 215 | 1 616 202 | 1 879 635 | 2 133 848 | 2 379 163 |
| COGS | 0 | 0 | 62 000 | 121 830 | 179 566 | 297 281 | 410 876 | 520 496 | 626 278 | 728 359 | 826 866 | 921 926 |
| Gross profit | 0 | 0 | 98 000 | 192 570 | 283 830 | 469 896 | 649 450 | 822 719 | 989 924 | 1 151 276 | 1 306 982 | 1 457 237 |
| GM% | 0.0% | 0.0% | 61.3% | 61.3% | 61.3% | 61.3% | 61.3% | 61.3% | 61.2% | 61.3% | 61.3% | 61.3% |
| Fixed costs | 1 487 000 | 2 202 000 | 2 427 000 | 2 947 000 | 3 364 000 | 4 014 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 | 4 300 000 |
| EBITDA | -1 487 000 | -2 202 000 | -2 329 000 | -2 754 430 | -3 080 170 | -3 544 104 | -3 650 550 | -3 477 281 | -3 310 076 | -3 148 724 | -2 993 018 | -2 842 763 |
| Cash burn | 1 487 000 | 2 202 000 | 2 329 000 | 2 754 430 | 3 080 170 | 3 544 104 | 3 650 550 | 3 477 281 | 3 310 076 | 3 148 724 | 2 993 018 | 2 842 763 |
| Cumulative cash | -1 487 000 | -3 689 000 | -6 018 000 | -8 772 430 | -11 852 600 | -15 396 704 | -19 047 254 | -22 524 535 | -25 834 612 | -28 983 335 | -31 976 354 | -34 819 116 |

### Waterfall
| Шаг | Значение |
|---|---|
| ARPA | 160 000 ₽ |
| Gross profit на клиента | 98 000 ₽ |
| Contribution profit на клиента | 94 000 ₽ |
| EBITDA на клиента после распределения fixed costs на break-even базе | 522 ₽ |
| Net на клиента после налога | -9 078 ₽ |

### Cash flow и break-even
| Метрика | Значение |
|---|---|
| startup_capital_to_bep_rub | 34 819 116 ₽ |
| Break-even client count | 46 |
| Break-even month | >M36 |
| Peak cumulative cash burn in M1-M12 | 34 819 116 ₽ |

## Налоговая модель

| Режим | Как учтён в модели | Комментарий |
|---|---|---|
| УСН 6% | Использован в pessimistic scenario | Налог считается с выручки, подходит как консервативный baseline для компании без IT-льготы. |
| IT-льгота 3% | Использована в base и optimistic scenarios | Применимо при аккредитации Минцифры и соблюдении профильной структуры выручки. |
| ОСНО 20% | В PnL не выбран как основной сценарий | Нужно учитывать налог на прибыль 20% и НДС 20%, что ухудшит cash conversion и потребность в оборотном капитале. |
| Страховые взносы ~30% к ФОТ | Уже включены | В economics fully-loaded FOT уже дан с взносами. |
| НДС 20% | Условно не включён в MRR/COGS как pass-through | Если компания на ОСНО и цены рынку даны без НДС, EBITDA и cash gap будут хуже, чем в base. |

## Вывод по PnL

- Base-case не выходит на EBITDA break-even в первые 12 месяцев, но при сохранении темпа 3 новых клиента/мес проходит break-even около M14.
- Optimistic scenario выходит на break-even около M11-M12 и требует около 16.4 млн ₽ капитала до BEP.
- Pessimistic scenario в горизонте 12 месяцев и даже до M36 не выходит на break-even без роста ARPA, снижения churn или сокращения fixed costs.

<!-- P6A-DONE -->

# SECTION B - Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

База для расчёта: M12 EBITDA из SECTION A = **-1 421 565 ₽/мес**.

Допущения для sensitivity:
- **CAC x2** интерпретирую как падение acquisition efficiency примерно в 2 раза, то есть new clients по месяцам снижаются с `0,0,1,2,2,3...` до `0,0,0.5,1,1,1.5...` при тех же fixed costs.
- **Churn x2**: 2.5% → **5.0%** в месяц.
- **Price -30%**: ARPU 180 000 ₽ → **126 000 ₽** при неизменном COGS 58 000 ₽.

| Сценарий | Ключевое изменение | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | -1 421 565 | — | уже требует bridge до M18 [SECTION A] |
| Sens1 | CAC x2 | -2 860 782 | -1 439 217 | главная боль, потому что enterprise funnel становится слишком медленным |
| Sens2 | Churn x2 | -1 682 670 | -261 105 | модель терпит ухудшение retention лучше, чем обвал GTM |
| Sens3 | Price -30% | -2 695 626 | -1 274 061 | price compression почти так же опасен, как CAC shock |

**Вывод:** две самые опасные оси для кейса, это **CAC inflation** и **price compression**. При них M12 EBITDA уходит к диапазону **-2.7 ... -2.9 млн ₽/мес**, а потребность в капитале резко растёт.

## 2. Monte Carlo Lite — confidence intervals

### 2.1 Triangular inputs

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 350 000 | 474 000 | 900 000 | base из 04-economics + stress на длинный enterprise sale [S5][S6][S7][S8] |
| Monthly churn, % | 1.5% | 2.5% | 6.0% | benchmark enterprise SaaS + консервативный stress [S1][S2][S3][S4] |
| ARPU, ₽/мес | 126 000 | 180 000 | 220 000 | base ARPU + sensitivity -30% + premium enterprise upside [S9][S10][S12][S13] |
| Conversion rate lead→paid, % | 12% | 18% | 24% | внутренняя funnel-модель regulated B2B из 04-economics [internal] |
| Time-to-hire, мес | 1.0 | 1.7 | 3.0 | hiring realism по core-ролям [S5][S6][S7][S8] |

### 2.2 Упрощённая симуляция

Вместо 1000 прогонов использована **сетка из 9 комбинаций** min/mode/max по CAC, churn и ARPU, с привязкой conversion rate и time-to-hire к более optimistic или stressed режиму.

Контрольные точки:
- **p10**: CAC_max + Churn_max + ARPU_min
- **p50**: CAC_mode + Churn_mode + ARPU_mode
- **p90**: CAC_min + Churn_min + ARPU_max

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -3 423 653 | 1 514 731 | 15 092 320 | 18 515 973 |
| CAC payback, мес | 7.1 | 2.6 | 1.6 | 5.5 |
| LTV/CAC | 1.3x | 10.3x | 30.9x | 29.6x |
| Cash runway, мес | 0 | 24+ | 24+ | 24+ |

### 2.3 Интерпретация Monte Carlo Lite

- **Правило 1:** p10 EBITDA < 0, следовательно **kill criterion #1 активируется**: есть риск не дожить до устойчивой экономики без bridge-финансирования.
- **Правило 2:** p50 EBITDA = **1.51 млн ₽/мес**, значит median-case **проходит EBITDA Gate**.
- **Правило 3:** разброс между p90 и p10 фактически экстремальный, то есть неопределённость **слишком высокая**, score надо **даунгрейдить на 1 notch**.
- **Правило 4:** width по **LTV/CAC = 29.6x > 8**, следовательно модель **хрупкая**, и её устойчивость почти полностью держится на discipline в pricing, churn и CAC.

## 3. Competitor deep-dive

### 3.1 Западные конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Abridge** | сильнейший enterprise brand, глубокие EHR-интеграции, крупные health systems, масштаб в ambient documentation [01-evidence] | заточен под рынок США, тяжёлый для РФ по данным, интеграциям и residency | **20-25%** западного enterprise ambient-scribe сегмента | локализация под МИС РФ, 152-ФЗ, on-prem/private cloud |
| **Suki** | зрелый physician workflow, long-standing market presence, сильный voice UX | дорогой enterprise rollout, меньше moat в локальном compliance outside US | **10-15%** | меньше vendor lock-in, ниже TCO для сетей РФ |
| **Nabla** | быстрый product velocity, сильный AI-note workflow, growing clinic adoption | слабее в legacy hospital procurement и deep local integrations | **8-12%** | лучше fit под российские шаблоны протоколов и юридически значимую документацию |

### 3.2 Российские конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Humarin** | сильная упаковка AI-скрайба, кейсы с клиниками, несколько продуктовых модулей, российское юрлицо [T2] | пока выглядит как ранний category-builder без масштаба ЦРТ | **10-15%** локального AI-scribe сегмента | у Voice2Med сильнее базовая speech-технология и enterprise access |
| **Smartica.ai** | понятный тариф, МИС-интеграции, 152-ФЗ, ранние пилоты [T2] | lower-price сегмент может давить ARPU, меньше enterprise moat | **5-10%** | выше шанс продавать не только seat, но и дорогой enterprise contour |
| **qMS ИИ** | встроенность в МИС-контур, 300+ внедрений у материнской платформы, реестр ПО [01-evidence] | фича может восприниматься как add-on внутри МИС, а не best-of-breed AI layer | **10-15%** через installed base qMS | Voice2Med может продаваться cross-MIS, а не только внутри одной платформы |
| **imotio.DOC** | локальное хранение, Сколково, готовая продуктовая форма [01-evidence] | более узкий footprint и слабее brand distribution | **3-5%** | у ЦРТ выше доверие enterprise buyers и шире канал гос/квази-гос внедрений |
| **iAmbulant / Voice2Med-like modules** | медданные, voice workflow, Сколково и интеграционный narrative [01-evidence] | слабее публичный GTM и pricing transparency | **3-5%** | у ЦРТ сильнее зрелость speech stack и референсы внедрений |

### 3.3 Что это значит для стратегии

1. **Запад доказывает категорию**, но не закрывает локальные требования РФ.
2. **РФ-рынок фрагментирован**, явного winner-takes-all пока нет.
3. Для Voice2Med лучший путь, это позиционирование как **enterprise-grade ambient documentation layer** с on-prem, МИС-интеграцией и сильной ASR-точностью.

## 4. Risk matrix

| Риск | Категория | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Срыв найма CTO/ML и длинный ramp команды | Operational | med | high | vacancy age > 60 дней, offer acceptance < 50% | founder-led hiring, retainers, fractional advisors |
| Интеграции с МИС превращаются в кастомные проекты | Operational | high | high | >25% roadmap уходит в one-off доработки | жёсткий template catalog, API-first scope control |
| Рост стоимости или деградация LLM/API | Operational | med | high | COGS/клиент > 70 000 ₽ два месяца подряд | fallback-провайдеры, локальные модели, кеширование |
| Поиск по категории остаётся низким, outbound не разгоняется | Market | med | med | pipeline < 3 SQL/мес после M4 | сместить GTM в integrator-led и founder-sales |
| Появляется price war, рынок уходит к 3-5 тыс. ₽ за врача | Market | high | high | win rate падает, discount > 25% | продавать workflow ROI и enterprise package вместо seat commodity |
| Крупные МИС или ASR-вендоры встраивают аналог как feature | Market | high | high | 2+ тендера проиграны bundle-решению подряд | партнёрства с МИС, white-label, focus on premium segment |
| Ужесточение требований 152-ФЗ / data residency | Regulatory | med | high | новые требования к локализации и сертификации | on-prem контур, российские облака, DPA by default |
| Попадание продукта под чувствительные трактовки 115-ФЗ/медданных/аудита | Regulatory | low | med | buyers требуют расширенный legal pack и аудит trails | подробный журнал действий, compliance docs, legal review |
| Санкции режут доступ к западному SaaS/компонентам | Regulatory | high | high | отключение billing/API/updates по иностранным сервисам | стек на российских провайдерах, резервные локальные компоненты |
| Runway проседает быстрее плана из-за длинного sale cycle | Financial | high | high | cash < 9 месяцев runway до M6 | резать fixed burn, bridge round заранее, milestone hiring |
| USD растёт, импортные compute/API дорожают | Financial | med | med | USD/RUB > 95 и COGS +15% | рублёвые контракты, pre-buy credits, локальные inference path |
| Инфляция и рост налоговой нагрузки съедают margin | Financial | med | med | payroll inflation > 15% г/г | ежегодная индексация цен, buffer в gross margin |
| Резкое ухудшение внешней обстановки или войны | Black swan | med | high | freeze CAPEX/IT budgets у клиник | фокус на ROI-сейл и cost-saving narrative |
| Полное отключение доступа к ключевому LLM | Black swan | med | very high | latency/errors > 20% сутки подряд | multi-model architecture, local fallback, offline queue |

## 5. Kill conditions через 6 месяцев

1. **p10 EBITDA @M24 остаётся < 0 и фактический runway < 6 месяцев.** Это прямой риск insolvency.
2. **Net new paying customers < 1/мес в среднем за последние 3 месяца** или pipeline < 2 pilot-to-paid conversion за полугодие. Это значит, что CAC и sales cycle сломали модель.
3. **Median-case пересобранной модели даёт EBITDA < 500 000 ₽/мес при горизонте M24** или фактический LTV/CAC < 3x. Это означает, что даже центр распределения уже не investment-grade.

## 6. Финальный вывод по SECTION B

Кейс **остаётся investable, но с заметным risk downgrade**. Главный тезис: продукт жизнеспособен только если команда удерживает одновременно **enterprise ARPU, разумный CAC и локальный compliance moat**. Если рынок сдвигается в commodity-seat pricing или funnel замедляется вдвое, экономика быстро перестаёт быть красивой.

<!-- P6B-DONE -->


<!-- 06-verdict.md -->

[HEALTHCARE] ЦРТ Voice2Med — APPROVED WITH NOTES: 72/100 | EBITDA base=1515К₽/мес через 24 мес | LTV/CAC=10.3x | Ключевое преимущество: локальный healthcare workflow с on-prem и МИС-интеграцией | Главный риск: commodity pricing и кастомные интеграции.

# 06-verdict — Investment Committee Verdict

sector: HEALTHCARE

## Финальный вердикт
**APPROVED WITH NOTES**

- **Normalized score:** **72/100**
- **Raw score:** **108/150**
- **Пороговое решение:** score >= 70 и `company_ebitda_potential_rub_month >= 500 000 ₽/мес` при `<=50` клиентах и `<=24` месяцев выполняются.
- **company_ebitda_rub_month, base @M24:** **1 514 731 ₽/мес**
- **company_ebitda_potential_rub_month:** **1 600 000 ₽/мес** при 50 клиентах
- **clients_to_500k_ebitda:** **41-42 клиента**
- **months_to_500k_ebitda:** **24 месяца в median/base горизонте**, при оптимистичном сценарии быстрее
- **startup_capital_to_bep_rub:** **27 619 972 ₽**

## Оценка
Source tier balance: T1=2, T2=6, T3=1, weighted=2.11. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `LTV/CAC = 10.3x`, `CAC Payback = 2.6 мес`, `Gross Margin = 67.8%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | `p50 EBITDA @M24 = 1 514 731 ₽/мес`, а при 50 клиентах `EBITDA ~1.6 млн ₽/мес` из `05-critic.md` и `04-economics.md`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | `PASS WITH RESERVATIONS`: low exact-search, но `20 пилотных клиник`, `первые оплаченные контракты`, `35 больниц` и penalty по tier balance. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 15 | Локальный healthcare workflow и on-prem полезны, но moat средний: риск feature-parity со стороны МИС и AI-scribe конкурентов. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | `Интеграции с МИС превращаются в кастомные проекты`, `санкции режут доступ к западному SaaS/компонентам` из `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `integrator/MIS partnerships` дают лучший CAC, buyer-list конкретный, а enterprise sale уже уложен в recurring + pilot motion. |

**Normalized score = round((108 × 100) / 150) = 72/100.**

## Почему это approved, а не near-pass
1. Экономика клиента инвестиционного качества уже на текущих допущениях: `LTV/CAC 10.3x`, payback `2.6 мес`, GM `67.8%`.
2. EBITDA-gate проходит в пределах лимита Program 7: `p50 EBITDA @M24 = 1.51 млн ₽/мес`, а порог `500k ₽/мес` достигается до 50 клиентов.
3. В РФ есть прямые локальные сигналы category formation: Voice2Med в `35 больницах`, Smartica.ai с `20 пилотными клиниками`, qMS ИИ в реестре российского ПО и `300+ внедрений` у МИС-контура.
4. Локальный on-prem / private cloud контур плюс интеграции в МИС реально снижают риск импортозамещения и 152-ФЗ.

## Что не даёт поставить 75+
1. Exact-demand в РФ всё ещё search-light и в основном sales-led.
2. Moat средний, а не выдающийся: есть сильный риск price compression до per-seat commodity.
3. Исполнение тяжёлое: интеграции, compliance, enterprise procurement, hiring ML/CTO, зависимость от inference stack.

## FULL business process from 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ на 1 paid client | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | ICP-ресерч клиник и сетей | CEO + SDR | HH/2ГИС/сайты клиник/CRM | 6 ч | 18 000 | низкая |
| 2 | Enrichment и сбор контактов ЛПР | SDR | CRM, email finder, Excel | 8 ч | 22 000 | средняя |
| 3 | Outreach: email, звонки, follow-ups | SDR | CRM, телефония, почта | 20 ч | 54 000 | средняя |
| 4 | Qualification call | SDR + AE | Meet, CRM | 4 ч | 18 000 | средняя |
| 5 | Product demo и discovery | AE + CEO | Meet, demo-стенд | 6 ч | 32 000 | низкая |
| 6 | Security/compliance questionnaire | CTO + AE | Docs, security checklist | 10 ч | 41 000 | низкая |
| 7 | Scoping пилота и KPI | AE + CTO + клинический куратор | Notion, калькулятор ROI | 12 ч | 56 000 | низкая |
| 8 | Pilot deployment и интеграция в МИС | CTO + backend/ML | on-prem/private cloud, API | 24 ч | 96 000 | низкая |
| 9 | Pilot review, ROI-защита, rollout proposal | AE + CEO | презентация, CRM | 6 ч | 28 000 | низкая |
| 10 | Procurement, юрсогласование, DPA/152-ФЗ | AE + CEO + юрист | Docs, ЭДО | 14 ч | 64 000 | низкая |
| 11 | Invoice и договор в 1С/ЭДО | back office | 1С, Диадок | 2 ч | 10 000 | высокая |
| 12 | Контроль оплаты и старт onboarding | finance + CS | банк-клиент, CRM | 2 ч | 8 000 | высокая |
| **Итого** |  |  |  |  | **447 000 ₽** |  |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 4 880 000 ₽ |
| CAC | 474 000 ₽ |
| LTV/CAC | 10.3x |
| CAC Payback | 2.6 мес |
| GM | 67.8% |
| contribution_margin_rub_month | 118 000 ₽/клиент/мес |
| company_ebitda_rub_month @M24 median/base | 1 514 731 ₽/мес |
| company_ebitda_potential_rub_month @50 clients | 1 600 000 ₽/мес |
| Break-even | 37 клиентов / ~6.56 млн ₽ monthly revenue |
| startup_capital_to_bep_rub | 27 619 972 ₽ |
| Cash runway в Monte Carlo p50 | 24+ мес |

## Team table
| Роль | Функция | FOT fully-loaded ₽/мес | Time-to-hire |
|---|---|---:|---:|
| CEO / founder-sales | enterprise sales, fundraising, ключевые сделки | 910 000 | 0 |
| CTO / Tech Lead | продукт, интеграции, безопасность | 715 000 | 2 мес |
| Senior Backend | API, интеграции с МИС, backend | 520 000 | 1.5 мес |
| ML Engineer | ASR/LLM pipeline, eval, quality | 650 000 | 2.5 мес |
| SDR | pipeline generation | 225 000 | 0.75 мес |
| AE | demos, pilots, closing | 417 000 | 1.5 мес |
| Customer Success | onboarding, adoption, renewals | 286 000 | 1 мес |
| **Итого FOT** |  | **3 723 000 ₽/мес** |  |

## 7-factor Moat framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 2 | Интеграция в МИС, шаблоны протоколов и обучение врачей создают умеренный lock-in. |
| 3. Scale economies | 2 | COGS/inference и onboarding amortization улучшаются с объёмом, но не драматически. |
| 4. Proprietary data / model advantage | 2 | Медицинские словари, voice workflow и локальные данные полезны, но размер датасета публично не раскрыт. |
| 5. Regulatory moat | 2 | On-prem, 152-ФЗ, российский стек и enterprise security создают барьер, но не эксклюзивный. |
| 6. Brand / distribution | 3 | ЦРТ как известный локальный speech-вендор имеет trust и доступ к enterprise/government buyers. |
| 7. Embedded workflow | 2 | Продукт глубоко встроен в документацию врача и clinical workflow, если интеграция в МИС завершена. |
| **Итого** | **13/21** |  |

**Moat score = round((13 × 25) / 21) = 15/25.**

## GTM: 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | Крупная сеть, много врачей и высокая стоимость документационной рутины; нужен стандартизированный clinical workflow. | email decision-maker + отраслевые конференции | 250 000 ₽/мес |
| 2 | Мать и дитя | Высокий поток амбулаторных приёмов и формализованные протоколы, ROI от сокращения времени врача очевиден. | warm intro через integrator / vc.ru кейс | 220 000 ₽/мес |
| 3 | EMC | Premium-сегмент, чувствительность к качеству документации и англо/русским clinical notes. | email CIO / medical director | 300 000 ₽/мес |
| 4 | СМ-Клиника | Сетевая частная клиника с большим объёмом повторяемых протоколов и возможностью rollout по филиалам. | партнёрство с МИС-интегратором | 200 000 ₽/мес |
| 5 | Медскан | Уже строит AI-контур, значит buyer education ниже и есть запрос на automation layer поверх МИС. | конференция + direct outreach | 250 000 ₽/мес |
| 6 | Инвитро | Диагностический поток, стандартизированные описания и масштаб для централизованного documentation layer. | partnership / outbound to digital lead | 180 000 ₽/мес |
| 7 | Будь Здоров | Сетевой healthcare operator, боль на throughput врачей и документировании типовых визитов. | email decision-maker | 180 000 ₽/мес |
| 8 | АВА-ПЕТЕР / Скандинавия | Цифрово зрелая сеть, premium care и чувствительность к качеству patient record. | conference networking / targeted outbound | 200 000 ₽/мес |
| 9 | РЖД-Медицина | Большой распределённый контур, on-prem и российский стек особенно релевантны. | государственные/квазигос procurement связи | 300 000 ₽/мес |
| 10 | ГК Эксперт | Федеральные диагностические центры с потоковой документацией и ROI на ускорении протоколов. | integrator-led intro + отраслевое мероприятие | 170 000 ₽/мес |

## Top-3 risks
| Риск | Probability | Impact | Почему в top-3 |
|---|---|---|---|
| Price compression / seat commoditization | high | high | Если рынок уходит к 3-5 тыс. ₽ за врача, premium ARPU 180k на buyer-level пакете сжимается слишком быстро. |
| Интеграции с МИС становятся кастомным проектом | high | high | `>25% roadmap уходит в one-off доработки` ломает scale и ухудшает GM/CAC. |
| Runway и GTM-скорость | high | high | Enterprise sale cycle + compliance могут задержать выход к 41-42 клиентам и растянуть burn. |

## Proof points, которые поддерживают APPROVED
1. `20 пилотных клиник и первые оплаченные контракты` у Smartica.ai подтверждают локальную коммерческую валидность категории.
2. Voice2Med уже применялся `в 35 больницах`, а продуктовая листовка обещает ускорение заполнения протокола `в 2–3 раза`.
3. `100%` госмедорганизаций подключены к ЕГИСЗ, а цифровой документооборот уже масштабен.
4. `p50 EBITDA @M24 = 1.51 млн ₽/мес`, а LTV/CAC даёт запас прочности для approve even with notes.

## Delta vs previous
- Это не rerun-кейс, поэтому сравнение с предыдущим full verdict отсутствует.
- Относительно P4/P5 кейс усилился за счёт локальных proof points по внедрениям и investable PnL, но был снижен по итоговому score из-за среднего moat и execution-heavy GTM.

## Что доказать в ближайшие 6 месяцев
1. Удержать realized ARPU не ниже **150-180 тыс. ₽/мес** на buyer-level пакете.
2. Подтвердить, что pilot→paid conversion не падает ниже **20-25%**.
3. Снизить долю кастомных интеграций и внедрить шаблонный rollout по 2-3 МИС.
4. Доказать churn не хуже **2.5%/мес**, а лучше ближе к **1.5-2.0%/мес**.
5. Зафиксировать 3-5 именованных enterprise logo wins или публичных кейсов.

## Investment committee conclusion
ЦРТ Voice2Med проходит комитет как **APPROVED WITH NOTES**. Это не consumer AI и не search-led SaaS, а тяжёлый локальный healthcare workflow с хорошей клиентской экономикой, реальным EBITDA-потенциалом и понятным compliance-fit для РФ. Одобрение оправдано только при жёсткой дисциплине по pricing, template-интеграциям и partner-led GTM.

<!-- 07-score-trajectory.md -->

# Score trajectory

## 2026-04-25 15:27 MSK — P4 Demand Validation
- case: `crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii`
- stage: `P4-demand-validation`
- demand: `LOW keyword-demand / B2B willingness-to-pay proven`
- profit_gate: `PASS в seat-based, enterprise annual contract и on-prem сценариях`
- market_view: `узкий, регулируемый, но монетизируемый healthcare documentation слой`
- score_impact:
  - demand_quality: `0`
  - willingness_to_pay: `+2`
  - market_size: `+1`
  - competition_intensity: `-1`
  - overall_delta: `+2`
- rationale:
  - internal multi-demand по запросу `голосовое заполнение медицинской документации` показал LOW public demand;
  - три публичных международных competitor pricing page подтверждают реальную готовность врачей и клиник платить за AI medical scribe;
  - российская цифровая инфраструктура медицины достаточно зрелая для внедрения voice documentation поверх МИС;
  - EBITDA > 500K ₽/мес достижима без экстремальных допущений.
- artifact: `pipeline/cases/crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii/02-demand.md`

## 2026-05-10 17:28 MSK — P5 Unit Economics
- case: `crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii`
- stage: `P5-unit-economics`
- pricing_model: `enterprise recurring contract ~180K ₽/клиент/мес + setup вне LTV`
- fully_loaded_cac: `474K ₽`
- ltv: `4.88M ₽`
- ltv_cac: `10.3x`
- cac_payback: `2.6 мес`
- contribution_margin: `65.6%`
- break_even: `37 клиентов / ~6.56M ₽ monthly revenue`
- profit_gate: `PASS, EBITDA ~1.6M ₽/мес на 50 клиентах`
- score_impact:
  - unit_economics_quality: `+3`
  - gtm_feasibility: `+2`
  - regulated_complexity_penalty: `-1`
  - overall_delta: `+4`
- rationale:
  - CAC посчитан fully-loaded по regulated B2B логике, а не только по paid spend;
  - churn взят консервативно на уровне 2.5% в месяц, но LTV/CAC всё равно остаётся значительно выше порога 3x;
  - даже при фиксированных расходах ~4.3M ₽/мес компания выходит выше 500K ₽ EBITDA до 50 клиентов;
  - лучший канал по CAC это integrator/MIS partnerships, что повышает шанс эффективного масштабирования.
- artifact: `pipeline/cases/crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii/04-economics.md`

## 2026-05-11 09:50 MSK — P7 Critic and Verdict
- case: `crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii`
- stage: `P7-critic-verdict`
- verdict: `APPROVED WITH NOTES`
- raw_score: `108/150`
- normalized_score: `72/100`
- score_breakdown:
  - unit_economics: `21/25`
  - ebitda_potential: `20/25`
  - market_demand: `16/25`
  - moat: `15/25`
  - execution_risk: `16/25`
  - gtm_realism: `20/25`
- source_tier_balance: `T1=2, T2=6, T3=1, weighted=2.11, penalty=-2 to market+demand`
- moat_subscore: `13/21 -> 15/25`
- key_metrics:
  - customer_ltv_rub: `4.88M ₽`
  - cac: `474K ₽`
  - ltv_cac: `10.3x`
  - cac_payback: `2.6 мес`
  - company_ebitda_rub_month_base: `1.515M ₽/мес @M24`
  - company_ebitda_potential_rub_month: `1.6M ₽/мес @50 клиентов`
  - startup_capital_to_bep_rub: `27.62M ₽`
- score_impact:
  - moat_penalty: `-2`
  - execution_penalty: `-2`
  - evidence_quality_penalty: `-1`
  - approval_bonus: `+1`
  - overall_delta: `+1`
- rationale:
  - клиентская экономика инвестиционного качества подтверждена: LTV/CAC 10.3x, GM 67.8%, payback 2.6 мес;
  - base/median EBITDA-гейт пройден в пределах 24 месяцев, а порог 500K ₽/мес достигается до 50 клиентов;
  - локальные proof points сильные, но exact-demand в РФ остаётся search-light и moat пока только средний;
  - решение approve дано с оговорками из-за риска commoditization, кастомных интеграций и enterprise GTM complexity.
- artifact: `pipeline/cases/crt-voice2med-ai-golosovoe-zapolnenie-meditsinskoy-dokumentatsii/06-verdict.md`
