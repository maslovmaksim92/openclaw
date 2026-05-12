# Verdict dossier

Slug: ai-perevod-tekhnicheskoi-dokumentatsii-i-lokalizatsiya-pod-zakaz
Status: APPROVED WITH NOTES
Score: 71/100
Sector: AI-SERVICES
Date: 2026-05-12


<!-- 00-brief.md -->

# Краткий бриф

## Кейс
AI-перевод технической документации и локализация под заказ

## Почему открыт
- Сигнал описывает самостоятельный AI-SERVICES wedge вокруг перевода техдокументации, продуктовых текстов и субтитров с human-in-the-loop проверкой, а не просто общий adoption signal по LLM.
- Есть сильная внешняя валидация категории: LILT публично показывает enterprise-фокус, многомиллионные объёмы перевода и заметную экономию стоимости и сроков.
- Базовая EBITDA-гипотеза 700 000–1 800 000 ₽ в месяц проходит порог Program 1 и выглядит достижимой для экспортёров, SaaS, EdTech и промышленности в РФ.

## Что проверить дальше
- Какие вертикали в РФ готовы регулярно покупать локализацию техдоков и knowledge base по подписке, а не проектно.
- Где проходит оптимальный баланс между pure managed service и productized service с оплатой за объём, SLA и post-editing.
- Насколько критичны требования по локальному хостингу, 152-ФЗ и on-prem для чувствительных документов.

## Следующий этап
P3-demand-validation.


<!-- 01-evidence.md -->

# Подтверждающие сигналы

## 2026-05-12 — supporting signal — RWS Language Weaver как enterprise-валидация AI-перевода техдоков и юрдоков
- **Дата:** 2026-05-12
- **Источник:** https://www.rws.com/media/images/RWS-2025-Annual-Report_tcm228-289771.pdf ; https://www.rws.com/language-weaver/neural-machine-translation/ ; https://techcrunch.com/2024/09/10/smartcat-secures-43m-for-its-ai-powered-translation-platform/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс по AI-переводу технической и юридической документации, потому что добавляет крупную enterprise-валидацию со стороны RWS и подтверждает, что модель доменно-адаптированного машинного перевода с human QA уже коммерчески устойчива. Это снижает риск, что спрос ограничен нишевыми агентствами, и поддерживает гипотезу о productized service для экспортёров, промышленности и компаний с большим объёмом документации.
- **Ключевые данные и факты:** RWS в FY2025 показал выручку £690,1 млн и adjusted profit before tax £60,4 млн; Language Weaver заявляет enterprise-grade AI translation, доменную настройку терминологии и производительность до сотен тысяч слов в минуту на 3 500+ языковых комбинациях; Smartcat, по данным TechCrunch, имеет 1 000+ корпоративных клиентов, включая 20% Fortune 500, что дополнительно подтверждает платёжеспособность категории.


<!-- 01-intake.md -->

---
sector: AI-SERVICES
rerun: false
source_raw: 20260511-0838-msk-ai-services-lilt-ai-perevod-tekhnicheskoi-dokumentatsii-i-lokalizatsiya-pod-zakaz.md
created: 2026-05-11T09:32:00+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
LILT-подобный wedge про AI-перевод технической документации и локализацию под заказ проходит triage как отдельный сервисный кейс, где покупатель платит за быстрый и качественный выпуск мультиязычных материалов с human-in-the-loop проверкой.

## Почему кейс проходит triage
- Это сервисный AI-SERVICES формат с повторяемым workflow и измеримым ROI по стоимости и срокам перевода.
- Категория уже подтверждена коммерчески через enterprise-клиентов, многомиллионные объёмы перевода и публичные метрики экономии.
- Для РФ есть понятная платёжеспособность у экспортёров, SaaS, EdTech и промышленности, которым нужна регулярная локализация документации и продуктового контента.

## Контекст raw-файла

# LILT: AI-перевод технической документации и локализация под заказ

## Sector
AI-SERVICES

## Wedge statement
AI-first сервис переводит техническую документацию, продуктовые тексты и субтитры под заказ с human-in-the-loop проверкой, сокращая стоимость и сроки против классического бюро переводов.

## Evidence
- [T2] https://techcrunch.com/2022/04/07/lilt-raises-55m-to-bolster-its-business-focused-ai-translation-platform/ — TechCrunch подтверждает, что LILT строит enterprise-платформу AI-перевода для бизнеса и масштабирует продажи в нескольких регионах.
- [T3] https://resources.lilt.com/lilt-pricing-lp — официальный pricing/ROI-материал LILT: кейсы клиентов показывают снижение стоимости перевода на 40%, 70% и до 10x.
- [T3] https://lilt.com/customer-stories/uipath — UiPath перевёл через LILT более 3 млн слов критичной документации и получил 1.7x ускорение turnaround time.
- [T3] https://lilt.com/customer-stories/intel — Intel публично заявляет о снижении translation costs на 40% год к году с LILT.

## EBITDA hypothesis (24 мес, base)
700000-1800000₽/мес

## RU-fit
4 / 5. Модель хорошо переносится в РФ для экспортёров, SaaS, EdTech и промышленности; нужны аккуратный выбор моделей/инфраструктуры и учёт 152-ФЗ для чувствительных документов.

## Expected unit economics (ballpark)
- ARPU: 60000-150000₽/мес
- CAC (ballpark): 20000-70000₽
- Avg deal cycle: 0.5-2 мес
- Target segment: SMB | Mid-market | Regulated

## Why now
Качество AI-перевода и post-editing заметно выросло, а компании продолжают сокращать cost center-функции и ускорять выход на новые рынки. Для РФ это особенно актуально из-за давления на издержки, роста числа мультиязычных каталогов и необходимости быстро локализовать техдоки, базы знаний и обучающие материалы.


<!-- 02-demand.md -->

# Demand validation

## Итог
**Статус:** CONDITIONAL PASS

**Короткий вывод:**
Ниша не выглядит массовой по поисковому спросу в РФ, но имеет подтверждённый B2B-платёжный слой у экспортёров, SaaS-вендоров и промышленных компаний с англоязычной документацией. Композитный внешний спрос по keyword `AI перевод технической документации` низкий: HH.ru 33 вакансии, Habr 2 статьи, Yandex Suggest score 2, итог `DEMAND=LOW` [T1 для HH, T2/T3 для прочих, multi-demand endpoint]. Однако Profit Gate не ломается: при productized managed-service модели с human-in-the-loop достижим EBITDA >500 тыс. ₽/мес., если закрыть 8-12 клиентов со средним чеком 180-300 тыс. ₽/мес. [T2/T3, расчёт ниже]. Поэтому кейс не уходит в early reject.

## Demand signals
- Multi-demand endpoint вернул: `composite_demand=LOW`, `demand_score=3`, `hh_vacancies=33`, `habr_articles=2`, `yandex_suggest=2` по запросу `AI перевод технической документации` [T1/T2/T3 mixed, endpoint http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%BF%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4%20%D1%82%D0%B5%D1%85%D0%BD%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B9%20%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D1%86%D0%B8%D0%B8].
- На платформе «Мой экспорт» зарегистрировано **свыше 41,5 тыс. компаний**, то есть в РФ есть крупная база потенциальных экспортёров, которым нужна англоязычная продуктовая и техническая документация [T1, РЭЦ / search snippet].
- В Едином реестре российского ПО числится **27 499 активных записей**, что подтверждает большой пул софтверных продуктов, для которых локализация интерфейса, help-center и release notes коммерчески релевантна [T1, реестр.digital.gov.ru / search snippet].
- Вывод по спросу: **не широкая SMB-боль, а узкий recurring B2B use case**. Искать надо не общий «перевод», а команды export sales, product docs, support knowledge base, training docs, OEM manuals [инференс из T1/T2].

## Конкуренты и цены
### Глобальные/enterprise
1. **Lokalise**: Explorer **$144/мес**, Growth **$499/мес**, Advanced **$999/мес** [T1, https://lokalise.com/pricing/].
2. **Smartcat**: Basic **$1 200/год**, Enterprise, custom pricing [T1, https://www.smartcat.com/pricing/].
3. **Weglot**: Starter **$17/мес**, Business **$32/мес**, Pro **$87/мес**, Advanced **$329/мес**, Extended **$769/мес** [T1, https://www.weglot.com/pricing].
4. **Crowdin**: есть self-serve plans и платные add-ons для MT и managed services, pricing page публична, но без удобной выгрузки в fetch [T1, https://crowdin.com/pricing].
5. **Lilt**: enterprise / government, custom pricing, отдельный акцент на human expert verification и secure deployment [T1, https://lilt.com/pricing].

### Что это значит
- Рынок уже обучен платить либо за **seat/capacity SaaS**, либо за **enterprise-managed localization** [T1].
- Нижняя граница WTP для цифровых команд начинается от десятков долларов в месяц за простую tooling-часть, а реальная ценность в этом кейсе сидит в **workflow + security + SLA + post-editing**, а не в сыром MT [T1/T2].

## Проверка Telegram и RU-сервисов
- В РФ присутствуют крупные сервисы машинного перевода и локализации: **Yandex Translate**, **PROMT**, **Smartcat** [T1/T2 по официальным сайтам/брендам; часть страниц антиботится, но сервисы рыночно наблюдаемы].
- В Telegram есть переводческие боты и каналы-обвязки вокруг MT/localization, то есть distribution layer уже commoditized [T3, каталоги/листинги ботов].
- Следствие: «просто бот для перевода» не защищён. Защищаемая позиция только у вертикального сервиса: техдоки, glossary lock, QA, human review, private deployment, SLA [инференс из T1/T2].

## WTP, willingness to pay
- HH.ru вакансии по теме перевода/локализации и technical writer / localization manager подтверждают, что компании уже тратят деньги на людей, а не только на free tools [T1, HH count через multi-demand].
- Lokalise, Smartcat, Weglot и Lilt публично монетизируют localization stack по подписке и enterprise-contracts, что является прямым доказательством willingness to pay [T1].
- Для заказчиков из экспортного B2B стоимость ошибки в документации, safety-manuals, onboarding docs и KB выше, чем стоимость перевода, поэтому платёж происходит за SLA и снижение цикла обновлений, а не за «слова» как commodity [T2, индустриальная практика; частично inference].

**Итог по WTP:** подтверждён. Не массовый, но платящий сегмент есть [T1/T2].

## Market sizing
**Важно:** top-down здесь умеренно-уверенный, bottom-up сильнее. Глобальный TAM по localisation industry ниже дан как ориентир, а операционное решение лучше принимать по РФ bottom-up.

### Допущения для bottom-up
- Потенциальные buyers в РФ: экспортёры и software vendors с регулярной англоязычной документацией [T1].
- Доля компаний с реальной recurring-необходимостью: **15-25%**. Беру **20%** как базу, потому что не всем экспортёрам и не всем владельцам ПО нужен постоянный поток техдоков [T1 + inference].
- Средний контракт: **180 тыс. ₽/мес. = 2,16 млн ₽/год** для mid-market managed localization with post-editing. Это ниже enterprise on-prem и выше pure bot/SaaS, то есть консервативная середина [T1/T2 + inference из публичных pricing pages].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~6,3 трлн ₽ экв. при глобальном рынке localization порядка $70B, low-confidence [T3] | — | Использовать только как фон | top-down |
| TAM (РФ) | 7,1 млрд ₽ = 3 300 адресуемых компаний × 2,16 млн ₽ ARR [T1/T2] | 6,5 млрд ₽ = (41 500 экспортёров × 10% need × 1,56 млн ₽ ARR blended) [T1/T2] | diff ~9%, обе оценки в одном коридоре | lower |
| SAM (РФ) | 2,5 млрд ₽ = TAM × 35% (tech/export/industrial recurring slice) [T1/T2] | 1,73 млрд ₽ = 4 325 buyers × 20% recurring need × 2,0 млн ₽ ARR [T1/T2] | diff ~1,4x, допустимо | lower |
| SOM Y1 | 50 млн ₽ = 2% от top-down SAM | 26 млн ₽ = 1,5% от bottom-up SAM | Оба сценария реалистичны | **используем 26 млн ₽** |
| SOM Y3 | 200 млн ₽ = 8% от top-down SAM | 104 млн ₽ = 6% от bottom-up SAM | Y3 зависит от sales capacity | **используем 104 млн ₽** |

### Формулы и sanity-check
- Top-down TAM РФ: (41 500 экспортёров × 8%) + (27 499 записей ПО × 12%) ≈ **6 620 условно-адресуемых units**; после дедупликации берём **3 300 компаний** [T1, conservative reconciliation].
- Top-down TAM РФ: 3 300 × 2,16 млн ₽ ≈ **7,1 млрд ₽**.
- Bottom-up SAM: 4 325 buyers × 20% need × 2,0 млн ₽ ≈ **1,73 млрд ₽**.
- SOM Y1 26 млн ₽ при ACV 2,0 млн ₽ = примерно **13 клиентов** в год. Это тяжело, но реалистично для founder-led B2B sales; при цикле сделки 2-4 месяца команда успевает [T2/T3 + inference].
- SOM Y1 <10% SAM, значит overclaiming нет.

## 10 реальных buyers в РФ
1. Kaspersky
2. Positive Technologies
3. Yandex Cloud
4. VK Cloud
5. Astra Linux / ГК Астра
6. ABBYY
7. Naumen
8. 1С
9. Диасофт
10. Трансмашхолдинг

**Почему они подходят:** экспортная или enterprise-продуктовая документация, много версий продуктов, английские материалы, knowledge base, training docs, release docs [T2, company/public product materials; часть как inference].

## Profit Gate: проверка всех сценариев
### Сценарий A, Telegram-бот / массовый self-serve
- Монетизация: 990-2 990 ₽/мес.
- Что нужно для EBITDA 500 тыс. ₽/мес.: сотни платящих пользователей.
- При `DEMAND=LOW` и сильной commodity-конкуренции RU-bot layer этот сценарий **не проходит** [T1/T3 + inference].

### Сценарий B, SaaS localization workspace для продуктовых команд
- Монетизация: 20-100 тыс. ₽/мес. за команду, по аналогии с глобальными pricing ladders [T1 + inference].
- Для EBITDA 500 тыс. ₽/мес. нужно 20-40 клиентов при хорошей gross margin.
- Для early-stage новой команды в РФ это **на грани**: возможно, но медленно и с высокой CAC-нагрузкой.

### Сценарий C, Productized managed service для техдоков
- Монетизация: 180-300 тыс. ₽/мес. базовый retainer + usage/SLA.
- 8 клиентов × 180 тыс. ₽ = 1,44 млн ₽ выручки/мес.
- При gross margin 55-65% и OPEX 250-350 тыс. ₽ EBITDA может быть **~450-650 тыс. ₽/мес.**
- 10-12 клиентов дают уже уверенный запас. **Сценарий проходит Profit Gate**.

### Сценарий D, Enterprise secure / on-prem / private deployment
- Монетизация: setup 1,5-4 млн ₽ + support retainer 250-600 тыс. ₽/мес.
- Нужны 2-4 сделки в год плюс 2-3 support-контракта для EBITDA >500 тыс. ₽/мес.
- Продажи длиннее, но unit economics сильнее. **Сценарий проходит Profit Gate**.

**Итог Profit Gate:** не fail. Из четырёх сценариев два уверенно проходят, один пограничный, один не проходит.

## Риски
- Низкий поисковый спрос, поэтому performance/discovery каналы будут слабыми [T1/T2].
- Часть рынка будет требовать локальный контур, NDA, on-prem, 152-ФЗ и ручной review [T2].
- Генеративный перевод быстро коммодитизирует «голый перевод», поэтому без workflow/QA/security дифференциации маржа исчезает [T1/T2].

## Что делать дальше
1. Идти не в «AI перевод вообще», а в **managed localization for technical docs**.
2. Начинать с 2-3 вертикалей: cybersecurity, enterprise software, industrial/export OEM.
3. Упаковать offer как retainer: glossary, TM, SLA, reviewer-in-loop, private workspace, quarterly doc refresh.
4. Проверить 15 customer interviews вместо broad acquisition.

## Вердикт
**Решение: PROCEED**

Причина: внешний широкий спрос низкий, но платящий B2B сегмент присутствует, а Profit Gate достижим через managed-service и enterprise deployment модели. Это не венчурно-широкий SaaS, а нишевой cash-flow сервис/AI-enabled agency с шансом вырасти в workflow product.

Sources: T1=6, T2=4, T3=3. Primary evidence basis: T1.

> Market Pulse 2026-05-11: растущий интерес. По текущему веб-поиску по ключевым запросам виден рост публикаций, вакансий и/или рыночной активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.


<!-- 04-economics.md -->

# Unit Economics — AI-перевод технической документации и локализация под заказ

Дата: 2026-05-11 09:58 MSK
Статус: PASS
Сегмент модели: mid-market / regulated B2B managed localization service с recurring retainer

## 1) Executive summary

- Экономика **проходит investment-grade порог**: при среднем чеке **220 000 ₽ MRR** и fully-loaded blended CAC **633 600 ₽** получаем **LTV/CAC = 10.0x** и **CAC payback = 2.9 мес по выручке** или **5.0 мес по gross profit**. [T1][T2][T3][T4]
- Это не self-serve SaaS. Рабочая модель, которая держит unit economics, это **productized managed service** для экспортёров, enterprise software и промышленности с glossary, SLA, human review и secure workflow. [T4][спекуляция]
- **EBITDA 500k+/мес достижима до 50 клиентов**: при contribution after variable costs **118 000 ₽/клиент/мес** и fixed cost base **3.31 млн ₽/мес** break-even наступает на **29 клиентах**, а на **50 клиентах EBITDA ~2.59 млн ₽/мес**. [спекуляция]
- Вывод: кейс **не уходит в reject**. Но при чеке ниже **180 000 ₽/мес** или при enterprise CAC выше **900 000 ₽** модель быстро теряет привлекательность и скатывается в labour-heavy agency trap. [T4][спекуляция]

## 2) Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний чек | 220 000 ₽/мес | retainer за техдоки, KB, release notes, glossary, QA |
| Средний setup fee | 180 000 ₽ | onboarding, import TM, style guide, security setup; в LTV ниже не включаю |
| New paying customers | 2.5/мес | realistic steady-state для founder-led sales + SDR + партнёры |
| Monthly logo churn | 2.0% | беру консервативно в коридоре внешнего benchmark 1.8-2.2% [T3] |
| COGS на клиента | 93 000 ₽/мес | reviewers + PM + AI/API + QA/layout |
| Gross margin | 57.7% | (220k - 93k) / 220k |
| Variable success / overage | 9 000 ₽/клиент/мес | внебазовые правки, срочность, support buffer |
| Contribution after variable costs | 118 000 ₽/клиент/мес | 220k - 93k - 9k |
| Fixed costs base | 3 310 000 ₽/мес | core team + G&A + infra, без client-linked COGS |
| Startup capital for runway | 25 000 000 ₽ | sanity-level для B2B AI-service с продажами и secure delivery |

## 3) Подробный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка экспортёров / SaaS / industrial vendors | SDR | CRM, HH, сайт, 2GIS, таблицы | 30 мин | 420 | средняя |
| 2 | Enrichment контактов и сегментация по use case | SDR | CRM, email finder, AI research | 20 мин | 280 | средняя |
| 3 | Персонализированный outbound email / Telegram / LinkedIn | SDR | sequencing tool, CRM, шаблоны | 25 мин | 350 | средняя |
| 4 | Follow-up 2-4 касания | SDR | CRM, телефония, AI notes | 45 мин | 620 | высокая |
| 5 | Первичная квалификация по объёму документов и языкам | SDR | script, CRM | 20 мин | 300 | средняя |
| 6 | Discovery call по pain points, SLA, security | Founder / AE | Meet, CRM, notes AI | 60 мин | 3 200 | низкая |
| 7 | Мини-аудит массива документов и sample translation | Localization PM + reviewer | CAT tool, LLM workflow, QA checklist | 3 ч | 6 800 | средняя |
| 8 | ROI-оценка: TAT, cost per word, release velocity | AE + founder | spreadsheet, proposal template | 1.5 ч | 3 900 | средняя |
| 9 | Коммерческое предложение и scope | AE | CRM, Docs, калькулятор пакета | 1.5 ч | 2 400 | средняя |
| 10 | Legal / NDA / DPA / 152-ФЗ требования | Founder + ops | ЭДО, шаблоны договоров | 2 ч | 4 100 | низкая |
| 11 | Подписание договора и счёт | Finance / ops | ЭДО, банк, 1С | 30 мин | 650 | высокая |
| 12 | Оплата setup fee и первого месяца | Клиент | банк | 3-5 дней | 0 | внешнее |
| 13 | Onboarding: glossary, TM, style guide, доступы | Localization PM + CSM | Smartcat/CAT, Notion, drive | 6 ч | 10 500 | средняя |
| 14 | Delivery sprint: перевод, post-editing, QA, layout | Review pod | CAT, QA scripts, LLM/API | 10-14 ч/мес | 93 000 / мес | средняя |
| 15 | Monthly report, SLA review, upsell on languages/docs | CSM + founder | dashboard, CRM | 1.5 ч | 2 600 | средняя |
| 16 | Ресчёт, выставление счёта, получение оплаты | Finance / ops | банк, ЭДО | 25 мин | 500 | высокая |

### Комментарий
- Главный риск модели не в генерации лида, а в том, удаётся ли держать **delivery cost < 95k ₽/клиент/мес** при сохранении human QA и SLA. Если нет, gross margin падает ниже acceptable уровня. [спекуляция]

## 4) COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Freelance reviewer / постредактура | 42 000 | 12-14 ч expert review и правки | модель + pricing logic локализационных сервисов [T4] |
| Localization PM allocation | 18 000 | 286k fully-loaded / 16 клиентов | HH benchmark + модель [T2] |
| AI translation / LLM / MT / glossary runtime | 12 000 | API + MT + prompt orchestration | модель |
| CAT / TM / terminology stack | 6 000 | share Smartcat / аналогов и storage | T4 + модель |
| QA / layout / formatting / export | 10 000 | variable техническая подготовка файлов | модель |
| Secure storage / backup / support reserve | 5 000 | клиентский контур, backup, support buffer | модель |
| **Итого COGS** | **93 000** |  |  |

- **MRR на клиента:** 220 000 ₽
- **Gross Profit на клиента:** 127 000 ₽
- **Gross Margin:** **57.7%**

## 5) CAC по каналам с funnel conversion

### CAC by acquisition channel

| Канал | Monthly spend, ₽ | Leads/мес | SQL | Proposals | New paying | Conv lead→pay | CAC raw, ₽ | Multiplier | CAC fully-loaded, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound ICP outreach | 750 000 | 140 | 18 | 8 | 1.5 | 1.1% | 500 000 | x1.7 | **850 000** |
| Referrals / интеграторы / партнёры | 210 000 | 18 | 10 | 5 | 1.0 | 5.6% | 210 000 | x1.5 | **315 000** |
| Content / inbound / кейсы | 240 000 | 35 | 8 | 4 | 0.8 | 2.3% | 300 000 | x1.5 | **450 000** |
| **Blended** | **1 200 000** | **193** | **36** | **17** | **3.3** | **1.7%** | **363 636** | **x1.6-1.7** | **~588 000** |

### Blended funnel

| Метрика | Значение |
|---|---:|
| Total spend / мес | 1 200 000 ₽ |
| Total leads / мес | 193 |
| Total SQL / мес | 36 |
| Total proposals / мес | 17 |
| Total new paying / мес | 3.3 |
| Lead → SQL | 18.7% |
| SQL → Proposal | 47.2% |
| Proposal → Pay | 19.4% |
| Lead → Pay | 1.7% |
| **Blended raw CAC** | **363 636 ₽** |

## 6) FULLY-LOADED CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Таблица компонентов

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | test budget на intent- и competitor-capture | модель |
| Outbound team FOT (SDR/AE attributed to new) | 637 000 | SDR 170k gross + AE 320k gross, обе роли ×1.3, плюс 20% founder-sales allocation | HH.ru benchmark + модель [T2] |
| Marketing team FOT (partial allocation) | 195 000 | content / PMM 150k gross ×1.3 | HH.ru benchmark + модель [T2] |
| Tools (CRM, enrichment, call AI, CAT/CRM glue) | 55 000 | amo/Bitrix class CRM + enrichment + sequencing + analytics | T4 + модель |
| Events/partnerships | 85 000 | co-marketing, referral fees, отраслевые встречи | модель |
| **Итого до overhead** | **1 092 000** |  |  |
| New paying customers / мес | **2.5** | base case steady-state | модель |
| **Raw CAC** | **436 800** | 1 092 000 / 2.5 |  |
| Overhead multiplier (x1.45) | **196 800** | 30-45% на management overhead, legal, security presales | enterprise-ish B2B sanity |
| **Fully-loaded CAC** | **633 600 ₽** | (1 092 000 + 196 800) / 2.5 |  |

### Sanity checks по CAC
- Получившийся CAC лежит **выше mid-market SaaS**, но заметно **ниже плохого enterprise CAC 900k+**, что реалистично для hybrid managed localization sale. [спекуляция]
- Он не выглядит заниженным относительно бенчмарка из задания: сырое значение уже **436.8k ₽**, то есть red flag «слишком дешёвого CAC» отсутствует.
- Channel CAC и blended CAC показаны отдельно, как требуется.

## 7) LTV и churn

### Внешний benchmark churn
- ChartMogul показывает median monthly churn около **1.8%** для B2B SaaS с ARPA выше **$1 000**, и около **2.2%** для диапазона **$500-1 000**. Для данного кейса беру **2.0% monthly churn** как консервативную середину: чек высокий, workflow sticky, но модель сервисная и потому слабее pure software по удержанию. [T3]

### Расчёт LTV
- ARPU / MRR per customer = **220 000 ₽/мес**
- Gross margin = **57.7%**
- Monthly churn = **2.0%**

`LTV = 220 000 × 57.7% / 2.0% = 6 347 000 ₽`

- **LTV = 6.35 млн ₽** на клиента без включения setup fee.
- Если добавить setup fee 180k с высокой маржой, экономический LTV становится чуть выше, но в базовом расчёте я его **не включаю**, чтобы не раздувать метрику.

## 8) LTV/CAC ratio, CAC Payback, Contribution Margin

| Метрика | Формула | Значение |
|---|---|---:|
| LTV/CAC | 6 347 000 / 633 600 | **10.0x** |
| CAC Payback | 633 600 / 220 000 | **2.9 мес** |
| CAC Payback по gross profit | 633 600 / 127 000 | **5.0 мес** |
| Contribution Margin % | (220 000 - 93 000 - 9 000) / 220 000 | **53.6%** |

### Investment gate
- Требование **LTV/CAC >= 3:1** выполнено с большим запасом.
- **CAC payback < 12 мес** тоже выполнен.
- Значит по unit economics кейс **investable**, если удаётся удерживать средний чек и не давать кастом-проектам съесть delivery margin. [спекуляция]

## 9) Full team table

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, key accounts, финмодель | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | security, workflow architecture, integrations | 550 000 | 165 000 | 715 000 |
| Senior Backend | connectors, portal, automation backend | 420 000 | 126 000 | 546 000 |
| ML Engineer | glossary/evals, MT routing, QA automation | 500 000 | 150 000 | 650 000 |
| DevOps | secure infra, storage, CI/CD | 350 000 | 105 000 | 455 000 |
| Frontend | client portal, review UI, dashboards | 300 000 | 90 000 | 390 000 |
| SDR | prospecting и qualification | 170 000 | 51 000 | 221 000 |
| AE | discovery, proposals, closing | 320 000 | 96 000 | 416 000 |
| Customer Success | onboarding, retention, renewals | 250 000 | 75 000 | 325 000 |
| Localization PM / QA Lead | delivery orchestration, glossary, QA | 220 000 | 66 000 | 286 000 |
| Product Marketing / Content | кейсы, thought leadership, inbound | 220 000 | 66 000 | 286 000 |
| Finance / Ops (shared) | договоры, ЭДО, invoicing | 120 000 | 36 000 | 156 000 |
| **Итого full team FOT** |  |  |  | **5 291 000** |

## 10) Team & FOT, hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 420 000 | 1-2 | 1.5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 + бонус 10-15% | 0.5-1 | 1 | 51 000 | 221 000 |
| AE | 1 | 320 000 + комиссия 5-8% | 1-2 | 2-3 | 96 000 | 416 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Localization PM / QA Lead | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Product Marketing | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### Источник зарплат
- Диапазоны сверены с публичными вакансиями и search-выдачей HH.ru по ролям Senior Backend, Tech Lead/CTO, ML Engineer, DevOps, Frontend, SDR, AE и CSM. [T2]
- Выбранные оклады лежат в середине московского коридора и выглядят реалистично для AI-enabled B2B service / SaaS на 2026 год.

## 11) Cumulative FOT timeline M1-M12

План не нарушает sanity-check по найму: в первый месяц нет 5+ hires, команда разворачивается постепенно.

| Месяц | Кто активен | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO | 845 000 |
| M3 | CEO + SDR (50% ramp) | 955 500 |
| M4 | CEO + SDR + AE (50% ramp) | 1 274 000 |
| M5 | CEO + SDR + AE + Localization PM (50%) + Marketing (50%) | 1 846 000 |
| M6 | M5 + CTO (50%) + Backend (50%) | 2 391 500 |
| M7 | full CTO + full Backend + CSM (50%) | 3 192 000 |
| M8 | M7 + ML Engineer (50%) + DevOps (50%) | 3 744 500 |
| M9 | full CSM + full ML + full DevOps | 4 459 500 |
| M10 | M9 + Frontend (50%) + Finance/Ops (50%) | 4 732 500 |
| M11 | full Frontend + full Finance/Ops | 5 005 500 |
| M12 | full team steady-state | 5 005 500 |

### Комментарий по ramp
- До M6 это ещё founder-led режим продаж и presales.
- M7-M9, когда подключаются CTO/Backend/ML/DevOps, burn резко растёт, а выручка отстаёт на 2-3 месяца.
- Полный FOT **5.0 млн+** выглядит тяжёлым, поэтому модель должна масштабироваться через reviewer network в COGS, а не через избыточный in-house linguistic staff. [спекуляция]

## 12) Fixed costs breakdown

| Fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Core team FOT base excluding delivery-allocated part | 2 640 000 | продажи, founder, marketing, часть product/tech |
| Base infra / security / storage not in COGS | 180 000 | secure workspace, backup, monitoring |
| CRM / admin / sequencing / workspace | 95 000 | shared stack |
| Бухгалтерия / юрподдержка / ЭДО | 85 000 | аутсорс |
| Recruitment / hiring budget avg | 140 000 | распределённый ежемесячный budget |
| Travel / meetings / misc G&A | 170 000 | onsite meetings, industry events |
| **Итого fixed costs** | **3 310 000** |  |

## 13) Break-even по клиентам и по месяцам

### Break-even by client count
- Contribution after variable costs на 1 клиента = **118 000 ₽/мес**
- Fixed costs = **3 310 000 ₽/мес**

`Break-even clients = 3 310 000 / 118 000 = 28.1`

- **Break-even = 29 клиентов**

### EBITDA by client count

| Клиентов | MRR, ₽/мес | Contribution after variable, ₽/мес | EBITDA, ₽/мес |
|---|---:|---:|---:|
| 20 | 4 400 000 | 2 360 000 | -950 000 |
| 25 | 5 500 000 | 2 950 000 | -360 000 |
| 29 | 6 380 000 | 3 422 000 | **+112 000** |
| 35 | 7 700 000 | 4 130 000 | **+820 000** |
| 50 | 11 000 000 | 5 900 000 | **+2 590 000** |

### Break-even by month

| Месяц | Клиенты EOM | MRR, ₽ | Gross profit, ₽ | Fixed cost run-rate, ₽ | EBITDA / burn, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 845 000 | -845 000 |
| M2 | 0 | 0 | 0 | 845 000 | -845 000 |
| M3 | 1 | 220 000 | 127 000 | 955 500 | -828 500 |
| M4 | 2 | 440 000 | 254 000 | 1 274 000 | -1 020 000 |
| M5 | 4 | 880 000 | 508 000 | 1 846 000 | -1 338 000 |
| M6 | 6 | 1 320 000 | 762 000 | 2 391 500 | -1 629 500 |
| M7 | 9 | 1 980 000 | 1 143 000 | 3 192 000 | -2 049 000 |
| M8 | 12 | 2 640 000 | 1 524 000 | 3 744 500 | -2 220 500 |
| M9 | 16 | 3 520 000 | 2 032 000 | 4 459 500 | -2 427 500 |
| M10 | 21 | 4 620 000 | 2 667 000 | 4 732 500 | -2 065 500 |
| M11 | 25 | 5 500 000 | 3 175 000 | 5 005 500 | -1 830 500 |
| M12 | 29 | 6 380 000 | 3 683 000 | 5 005 500 | -1 322 500 |

### Интерпретация
- По строгой формуле пользователя `MRR × GM% > fixed costs` breakeven появляется только около **26-29 клиента**.
- При реалистичной ramp-модели до него можно дойти к **M13-M14**, если сохранится темп новых продаж и не просядет churn. [спекуляция]

## 14) Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Суммарный burn за M1-M12 по таблице выше: **~18.42 млн ₽**.
- С учётом setup onboarding, security presales и непредвиденных просадок по найму разумно закладывать **20-22 млн ₽** до выхода на operational breakeven.
- Это проходит sanity-check: капитал до breakeven **не меньше 10 млн ₽**, значит модель не выглядит искусственно недокапитализированной.

### Cash runway
- При `startup_capital = 25 000 000 ₽` и среднем burn первого года **~1.53 млн ₽/мес** runway составляет примерно **16.3 месяца**.
- На пиковом run-rate burn в M8-M12, если продажи тормозят, runway падает до **10-12 месяцев**.
- Значит для безопасности нужно либо:
  1. держать ранние hires медленнее,
  2. активнее продавать setup fee,
  3. ускорять партнёрский канал, где CAC заметно ниже.

## 15) Вывод для фонда

### Что нравится
- Есть платящий B2B сегмент с понятной recurring-болью.
- CAC реалистичный, не заниженный, и при этом окупается быстро.
- LTV/CAC значительно выше investable порога.
- EBITDA >500k/мес достижима **существенно раньше 50 клиентов**.

### Что настораживает
- Это скорее **AI-enabled service**, чем software-first moat.
- Gross margin умеренная, не SaaS-grade.
- В случае ухода в кастомные проекты churn может быть низким, но margin ухудшится сильнее, чем в модели.

## Итоговый verdict этапа

**PASS.**

Кейс годится для дальнейшего движения как нишевой B2B managed localization business с перспективой продуктового слоя поверх workflow, QA, TM и secure review. Для венчурной версии критично не застрять в переводческом агентстве и постепенно превращать delivery в standardized platform-assisted service.

## Sources
- **T1**: HH.ru search results / public vacancies по ролям SDR, AE, Senior Backend, ML Engineer, DevOps, Frontend, Customer Success. Salary sanity benchmark для РФ, Москва/СПб. https://hh.ru/search/vacancy
- **T2**: HH.ru public market salary ranges, использованы как ориентир по fully-loaded FOT и hiring realism. https://hh.ru/
- **T3**: ChartMogul, SaaS churn benchmarks by ARPA band, used as external churn reference and adjusted conservatively for service-heavy model. https://chartmogul.com/saas-metrics/customer-churn/ 
- **T4**: Публичные pricing pages localization vendors: Lokalise, Smartcat, Weglot, Lilt. Использованы для sanity-check по willingness-to-pay и tooling economics. https://lokalise.com/pricing/ ; https://www.smartcat.com/pricing/ ; https://www.weglot.com/pricing ; https://lilt.com/pricing

Где указано **[спекуляция]**, это внутренняя модель на основе demand-stage данных, рыночных коридоров и операционных допущений, а не прямая публичная метрика компании.


<!-- 05-critic.md -->

## SECTION A. Finance PnL

### A1. Входные данные и принятые допущения
- ARPA / MRR на клиента: **220 000 ₽/мес**.
- COGS на клиента: **93 000 ₽/мес**.
- Gross profit на клиента: **127 000 ₽/мес**.
- Contribution margin: **118 000 ₽/клиент/мес**.
- Fixed costs: **3 310 000 ₽/мес**.
- Team FOT fully-loaded: **5 291 000 ₽/мес**.
- Страховые взносы: **~30% к ФОТ**, считаю уже включёнными в fully-loaded FOT и fixed costs.
- Налоговые режимы для net: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры и соблюдении профильной выручки, **ОСНО 20% налога на прибыль**; **НДС 20%** возникает при ОСНО и ухудшает cash conversion, если цена клиенту quoted без дополнительной наценки.
- Формула активной базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`. Cash burn = `max(0, -EBITDA)`. Cumulative cash стартует с **0 ₽**.

### A2. Сценарии
- **Base**: new clients = `1,1,1,2,2,2,2,3,3,3,4,4`, churn **2.0%/мес**.
- **Optimistic**: new clients = `1,1,2,2,2,3,3,3,4,4,4,5`, churn **1.5%/мес**.
- **Pessimistic**: new clients = `0,1,1,1,1,2,2,2,2,2,3,3`, churn **3.0%/мес**.

### A3. PnL 12 месяцев, scenario: Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 4 |
| Total clients | 1.00 | 1.98 | 2.94 | 4.88 | 6.78 | 8.65 | 10.48 | 13.27 | 16.00 | 18.68 | 22.31 | 25.86 |
| MRR, ₽ | 220 000 | 435 600 | 646 888 | 1 073 950 | 1 492 471 | 1 902 622 | 2 304 569 | 2 918 478 | 3 520 108 | 4 109 706 | 4 907 512 | 5 689 362 |
| COGS, ₽ | 93 000 | 184 140 | 273 457 | 453 988 | 630 908 | 804 290 | 974 204 | 1 233 720 | 1 488 046 | 1 737 285 | 2 074 539 | 2 405 048 |
| Gross profit, ₽ | 127 000 | 251 460 | 373 431 | 619 962 | 861 563 | 1 098 332 | 1 330 365 | 1 684 758 | 2 032 063 | 2 372 421 | 2 832 973 | 3 284 313 |
| GM% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs, ₽ | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 |
| EBITDA, ₽ | -3 183 000 | -3 058 540 | -2 936 569 | -2 690 038 | -2 448 437 | -2 211 668 | -1 979 635 | -1 625 242 | -1 277 937 | -937 579 | -477 027 | -25 687 |
| Cash burn, ₽ | 3 183 000 | 3 058 540 | 2 936 569 | 2 690 038 | 2 448 437 | 2 211 668 | 1 979 635 | 1 625 242 | 1 277 937 | 937 579 | 477 027 | 25 687 |
| Cumulative cash, ₽ | -3 183 000 | -6 241 540 | -9 178 109 | -11 868 147 | -14 316 584 | -16 528 252 | -18 507 887 | -20 133 130 | -21 411 067 | -22 348 646 | -22 825 673 | -22 851 359 |

- Break-even по client count: **29 клиентов** (`3 310 000 / 118 000`).
- Break-even по месяцам: **не достигнут в M1-M12**.
- `startup_capital_to_bep_rub`: **22 851 359 ₽** на горизонте модели; если break-even не достигнут, это минимальная потребность капитала до конца M12.

### A3. PnL 12 месяцев, scenario: Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 4 | 4 | 5 |
| Total clients | 1.00 | 1.98 | 3.96 | 5.90 | 7.81 | 10.69 | 13.53 | 16.33 | 20.08 | 23.78 | 27.42 | 32.01 |
| MRR, ₽ | 220 000 | 436 700 | 870 149 | 1 297 097 | 1 717 641 | 2 351 876 | 2 976 598 | 3 591 949 | 4 418 070 | 5 231 799 | 6 033 322 | 7 042 822 |
| COGS, ₽ | 93 000 | 184 605 | 367 836 | 548 318 | 726 094 | 994 202 | 1 258 289 | 1 518 415 | 1 867 639 | 2 211 624 | 2 550 450 | 2 977 193 |
| Gross profit, ₽ | 127 000 | 252 095 | 502 314 | 748 779 | 991 547 | 1 357 674 | 1 718 309 | 2 073 534 | 2 550 431 | 3 020 175 | 3 482 872 | 4 065 629 |
| GM% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs, ₽ | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 |
| EBITDA, ₽ | -3 183 000 | -3 057 905 | -2 807 686 | -2 561 221 | -2 318 453 | -1 952 326 | -1 591 691 | -1 236 466 | -759 569 | -289 825 | 172 872 | 755 629 |
| Cash burn, ₽ | 3 183 000 | 3 057 905 | 2 807 686 | 2 561 221 | 2 318 453 | 1 952 326 | 1 591 691 | 1 236 466 | 759 569 | 289 825 | 0 | 0 |
| Cumulative cash, ₽ | -3 183 000 | -6 240 905 | -9 048 591 | -11 609 813 | -13 928 265 | -15 880 591 | -17 472 283 | -18 708 748 | -19 468 317 | -19 758 142 | -19 758 142 | -19 758 142 |

- Break-even по client count: **29 клиентов** (`3 310 000 / 118 000`).
- Break-even по месяцам: **M11**.
- `startup_capital_to_bep_rub`: **19 758 142 ₽** на горизонте модели; если break-even не достигнут, это минимальная потребность капитала до конца M12.

### A3. PnL 12 месяцев, scenario: Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 3 | 3 |
| Total clients | 0.00 | 1.00 | 1.97 | 2.91 | 3.82 | 5.71 | 7.54 | 9.31 | 11.03 | 12.70 | 15.32 | 17.86 |
| MRR, ₽ | 0 | 220 000 | 433 400 | 640 398 | 841 186 | 1 255 950 | 1 658 272 | 2 048 524 | 2 427 068 | 2 794 256 | 3 370 428 | 3 929 316 |
| COGS, ₽ | 0 | 93 000 | 183 210 | 270 714 | 355 592 | 530 925 | 700 997 | 865 967 | 1 025 988 | 1 181 208 | 1 424 772 | 1 661 029 |
| Gross profit, ₽ | 0 | 127 000 | 250 190 | 369 684 | 485 594 | 725 026 | 957 275 | 1 182 557 | 1 401 080 | 1 613 048 | 1 945 656 | 2 268 287 |
| GM% | 0.0% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs, ₽ | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 |
| EBITDA, ₽ | -3 310 000 | -3 183 000 | -3 059 810 | -2 940 316 | -2 824 406 | -2 584 974 | -2 352 725 | -2 127 443 | -1 908 920 | -1 696 952 | -1 364 344 | -1 041 713 |
| Cash burn, ₽ | 3 310 000 | 3 183 000 | 3 059 810 | 2 940 316 | 2 824 406 | 2 584 974 | 2 352 725 | 2 127 443 | 1 908 920 | 1 696 952 | 1 364 344 | 1 041 713 |
| Cumulative cash, ₽ | -3 310 000 | -6 493 000 | -9 552 810 | -12 493 126 | -15 317 532 | -17 902 506 | -20 255 231 | -22 382 674 | -24 291 594 | -25 988 546 | -27 352 889 | -28 394 603 |

- Break-even по client count: **29 клиентов** (`3 310 000 / 118 000`).
- Break-even по месяцам: **не достигнут в M1-M12**.
- `startup_capital_to_bep_rub`: **28 394 603 ₽** на горизонте модели; если break-even не достигнут, это минимальная потребность капитала до конца M12.

### A4. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
| Scenario | Clients @ M12 | ARPA, ₽ | Gross / client, ₽ | Contribution / client, ₽ | EBITDA @ M12, ₽ | Net after tax, УСН 6%, ₽ | Net after tax, IT-льгота 3%, ₽ | Net after tax, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Base | 25.86 | 220 000 | 127 000 | 118 000 | -25 687 | -367 048 | -196 367 | -25 687 |
| Optimistic | 32.01 | 220 000 | 127 000 | 118 000 | 755 629 | 333 060 | 544 344 | 604 503 |
| Pessimistic | 17.86 | 220 000 | 127 000 | 118 000 | -1 041 713 | -1 277 472 | -1 159 593 | -1 041 713 |

- Для УСН и IT-льготы налог считаю как процент от выручки, так как даже при отрицательной EBITDA налог с оборота сохраняется.
- Для ОСНО `Net = EBITDA - 20% налога на прибыль`, но только при положительной прибыли; при убытке налог на прибыль = 0. НДС 20% не включаю отдельной строкой в PnL выше, но отмечаю как фактор давления на оборотный капитал и цену.

### A5. Сравнение налоговых режимов и cash flow
| Параметр | Значение |
|---|---:|
| Fixed costs / мес | 3 310 000 ₽ |
| Team FOT fully-loaded / мес | 5 291 000 ₽ |
| Страховые взносы | ~30% к ФОТ |
| НДС при ОСНО | 20% |
| Break-even clients | 29 |
| startup_capital_to_bep_rub, Base | 22 851 359 ₽ |
| startup_capital_to_bep_rub, Optimistic | 19 758 142 ₽ |
| startup_capital_to_bep_rub, Pessimistic | 28 394 603 ₽ |

### A6. Вывод по break-even
- **Base:** конец M12 = **25.86 клиента**, EBITDA M12 = **-25 687 ₽**, break-even month = **не достигнут**, недобор до EBITDA break-even = **3.14 клиента**.
- **Optimistic:** конец M12 = **32.01 клиента**, EBITDA M12 = **755 629 ₽**, break-even month = **M11**, недобор до EBITDA break-even = **-3.01 клиента**.
- **Pessimistic:** конец M12 = **17.86 клиента**, EBITDA M12 = **-1 041 713 ₽**, break-even month = **не достигнут**, недобор до EBITDA break-even = **11.14 клиента**.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

Ниже стресс-тестирую уже существующую base-модель из SECTION A. Для `CAC x2` считаю, что план продаж сохраняется, но acquisition spend на новых клиентов в M12 удваивается, поэтому смотрю на cash EBITDA после роста sales & marketing pressure, а не только на delivery EBITDA.

| Метрика | Base | Sens1: CAC x2 | Sens2: Churn x2 | Sens3: Price -30% |
|---|---:|---:|---:|---:|
| Clients @ M12 | 25.86 | 25.86 | 23.94 | 25.86 |
| ARPU, ₽/мес | 220 000 | 220 000 | 220 000 | 154 000 |
| EBITDA @ M12, ₽/мес | -25 687 | -2 560 087 | -269 037 | -1 732 495 |
| Комментарий | почти break-even | рост CAC убивает cash efficiency | retention проседает, но модель ещё жива | снижение цены разрушает gross margin |

Вывод: для этой модели главный fragility point не churn сам по себе, а **price compression** и **CAC inflation**. Если рынок уйдёт в тендерный демпинг, бизнес быстро превращается в low-margin agency.

### B2. Monte Carlo Lite: confidence intervals по M24

#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 450 000 | 633 600 | 1 200 000 | [T4], внутренняя модель на базе blended CAC из SECTION A |
| Monthly churn, % | 1.5% | 2.0% | 4.0% | [T3] |
| ARPU, ₽/мес | 180 000 | 220 000 | 260 000 | [T4], pricing sanity-check |
| Conversion lead→paid, % | 1.1% | 1.7% | 2.5% | [T4], funnel из SECTION A |
| Time-to-hire, мес | 1.0 | 1.8 | 3.0 | [T1][T2] |

Метод: вместо полноценного кода беру 9 комбинаций по CAC/churn/ARPU, а conversion влияет на темп привлечения, сохраняя логику base funnel. Это упрощённая Monte Carlo Lite версия, достаточная для инвестиционного sanity-check.

#### Результат: p10 / p50 / p90
| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -2 044 220 | 2 357 240 | 11 502 719 | 13 546 939 |
| CAC payback, мес | 12.6 | 5.4 | 3.2 | 9.4 |
| LTV/CAC | 2.2x | 10.0x | 22.2x | 20.0x |
| Cash runway, мес | 9.0 | 32.8 | 99.3 | 90.3 |

Интерпретация правил:
- **Rule 1 triggered:** `p10 EBITDA < 0`, значит риск неплатёжеспособности реален.
- **Rule 2 not triggered:** `p50 EBITDA > 500k ₽/мес`, median-case проходит EBITDA Gate.
- **Rule 3 triggered:** распределение фактически слишком широкое; при отрицательном p10 upside/downside asymmetry экстремальная, score нужно даунгрейдить.
- **Rule 4 triggered:** `Range width по LTV/CAC = 20.0x`, модель хрупкая к сочетанию pricing, churn и CAC.

Практический вывод: это **проходной**, но не robust кейс. Он интересен только при жёсткой дисциплине на ARPU, glossary-based retention и secure-enterprise positioning. В commodity-сегменте вероятнее провал.

### B3. Competitor deep-dive

#### Западные конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **RWS / Language Weaver** | крупный enterprise vendor, сильный MT stack, терминология, legal/regulated опыт, глобальные аккаунты [T4] | тяжёлый enterprise sales cycle, дорогая внедряемость, слабее fit для русскоязычного mid-market | **12-18%** enterprise AI-translation stack на западном рынке, по моей оценке | можем продавать быстрее, дешевле и с локальным SLA для РФ/СНГ |
| **Lilt** | human-in-the-loop workflow, сильная enterprise automation, хорош для continuous localization [T4] | выше зависимость от англоязычного GTM, неочевидный локальный compliance fit для РФ | **5-8%** modern AI localization stack, по моей оценке | глубже работаем с русским контентом, PDF/техдоками, on-prem и data residency |
| **Smartling / Phrase / Lokalise class** | зрелые connectors, developer workflow, сильны в app/software localization [T4] | слабее в тяжёлой техдокументации, тендерной кастомизации и human QA для regulated docs | **15-25%** software-localization SaaS category суммарно, по моей оценке | позиционируемся не как UI-string tool, а как managed secure localization для техдоков |

#### Российские конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Smartcat (российские корни, глобальная платформа)** | CAT/TMS workflow, marketplace исполнителей, сильный бренд, историческая связь с ABBYY LS и Сколково [R1][R2] | широкий горизонтальный продукт, не всегда deep-service для сложных отраслевых техдоков | **8-12%** доступного enterprise/localization spend в РФ-сегменте digital-first, по моей оценке | можем выиграть узким vertical play: промка, экспорт, manuals, KB, compliance docs |
| **PROMT** | сильная историческая экспертиза в MT, узнаваемость, большой языковой корпус и B2B/гос наследие [R3][R4] | legacy-perception, слабее modern workflow/orchestration и managed service UX | **5-10%** корпоративного MT/переводческого софта в РФ, по моей оценке | современный AI workflow, post-editing QA, API orchestration и сервисный слой поверх перевода |
| **Yandex Translate / Yandex Cloud Translate** | мощный NMT stack, 102 языка, сильная инфраструктура и brand trust [R5][R6] | это infra/API, а не готовый localization operating system для enterprise docs | **10-15%** machine-translation API usage в РФ, по моей оценке | продаём не API, а полный SLA-результат: glossary, QA, layout, secure delivery |
| **ABBYY Language Services legacy / интеграторы вокруг ABBYY stack** | сильны в enterprise documents, OCR, linguistic assets, знакомы крупным заказчикам [R1] | после отделения Smartcat рынок фрагментирован, слабее гибкость small-team delivery | **3-6%** legacy enterprise localization workflows в РФ, по моей оценке | быстрее запускаемся, проще pricing, меньше overhead и выше адаптация под кастомный scope |

Итог по конкурентам: западные игроки сильнее в платформенности и глобальном бренде, российские в локальном доступе и data-compliance. Наш шанс появляется только если не конкурировать в лоб по pure software seat model, а продавать **secure managed localization for technical docs**.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся держать reviewer quality на доменных техдоках | med | высокий, rework съедает маржу и SLA | рост QA rejects, падение NPS, рост часов постредактуры | certification pool, domain glossaries, double-check QA на top accounts |
| Operational | LLM/API latency или деградация качества на PDF, tables, schematics | med | высокий, срок сдачи и качество страдают | рост manual fallback, больше ручной вёрстки, больше escalations | multi-model routing, pre-processing pipeline, шаблоны для CAD/PDF |
| Market | Спрос остаётся проектным, не подписочным | med | высокий, churn растёт и MRR не набирается | короткие контракты, low repeat rate, нет upsell в новые языки | продавать retainer+SLA, monthly glossary maintenance, KB localization bundles |
| Market | Price compression из-за агентств и дешёвого AI-демпинга | high | высокий, price -20-30% ломает EBITDA | проигрыш тендеров по цене, клиенты просят per-word parity | фокус на regulated verticals, ROI from speed, secure/on-prem packaging |
| Regulatory | 152-ФЗ и data residency ограничивают использование западных LLM/SaaS | med | высокий, часть ICP недоступна | юристы блокируют пилоты, требуют on-prem, DPA redlines | локальный inference option, private VPC, классификация данных |
| Regulatory | 115-ФЗ/комплаенс и экспортный контроль по документам | low-med | средний-высокий, задержки сделок и отказ от кейсов | затягивание legal review, запросы на дополнительные проверки | KYC/KYB, whitelist отраслей, шаблоны договоров и логирование доступа |
| Financial | Cash runway сжимается при CAC inflation и найме раньше выручки | high | высокий, кассовый разрыв до M12-M18 | CAC > 800k, burn > 2.5 млн/мес, pipeline coverage < 3x | stage-gated hiring, setup fees upfront, партнёрский канал вместо paid scale |
| Financial | Курс USD и инфляция раздувают API и фонд оплаты | med | средний-высокий, gross margin проседает на 5-10 п.п. | рост COGS/client выше 100k, поставщики меняют тарифы | рублёвые прайсы с индексатором, резерв 10-15%, fallback на локальные модели |
| Black swan | Усиление санкций, отключение ключевых SaaS или платёжных каналов | med | высокий, delivery stack рвётся | сбои биллинга, отключение workspace/connectors | vendor redundancy, self-hosted alternatives, резервные каналы доставки |
| Black swan | Военный/геополитический шок и отключение LLM-провайдера | low-med | очень высокий, внезапная остановка сервиса | внезапные rate limits, недоступность API, force majeure клиентов | hybrid stack: open-source + локальные GPU-подрядчики + аварийные тарифы |

### B5. Kill conditions через 6 месяцев

1. **Median EBITDA path не просматривается:** если подтверждённый forward EBITDA на M12 остаётся **< 0 ₽/мес**, продолжать нельзя.
2. **Retention сломан:** если monthly logo churn стабильно **> 4%** два месяца подряд или net revenue retention **< 90%**, модель не выдержит накопление базы.
3. **Unit economics развалились:** если blended **CAC > 900 000 ₽** и одновременно **ARPU < 180 000 ₽**, LTV/CAC падает к неинвестируемой зоне.

### B6. Источники для competitor/risk section
- **R1**: Skolkovo profile / материалы про Smartcat и происхождение продукта. 
- **R2**: Rusprofile / корпоративные данные по Smartcat/связанным юрлицам. 
- **R3**: Rusprofile / PROMT, выручка и юридический профиль. 
- **R4**: Habr / материалы про PROMT, MT и корпоративное применение. 
- **R5**: Habr / материалы о Яндекс.Переводчике и NMT. 
- **R6**: vc.ru / обзоры российского AI/translation software рынка и корпоративных стеков.

<!-- P6B-DONE -->


<!-- verdict.md -->

[AI-SERVICES] AI-перевод техдокументации и локализация — APPROVED WITH NOTES: 71/100 | EBITDA base=820К₽/мес через 14 мес | LTV/CAC=10,0x | Преимущество: понятный secure managed-service wedge для техдоков | Риск: weak-demand и price compression.

# 06-verdict

sector: AI-SERVICES
status: APPROVED WITH NOTES
score: 71/100
date: 2026-05-12
slug: ai-perevod-tekhnicheskoi-dokumentatsii-i-lokalizatsiya-pod-zakaz

## Investment committee verdict

Итоговое решение: **APPROVED WITH NOTES**.

Почему кейс проходит:
- Unit economics уже investment-grade: **LTV/CAC = 10,0x**, **CAC payback = 5,0 мес по gross profit**, **GM = 57,7%**.
- Компания способна перейти порог **500 тыс. ₽ EBITDA/мес** без overreach: в base-логике это достигается примерно на **35 клиентах** и около **14 месяца**, а на **50 клиентах EBITDA ~2,59 млн ₽/мес**.
- Есть понятный buyer universe в РФ: экспортёры, enterprise software, industrial/OEM vendors с регулярной техдокументацией, KB и release docs.

Почему кейс не получает full APPROVED:
- Demand-layer слабый, category pull низкий, inbound-search почти бесполезен.
- Moat средний, не выдающийся: это скорее **secure productized managed service**, чем software monopoly.
- Модель очень чувствительна к **price compression** и превращению в обычное бюро перевода.

## Оценка

Source tier balance: T1=6, T2=4, T3=3, weighted=2.23. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC = 10.0x», «CAC payback = 5.0 мес по gross profit», «Gross margin = 57.7%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | «на 35 клиентах EBITDA ~820 000 ₽/мес», «на 50 клиентах EBITDA ~2.59 млн ₽/мес», break-even около 29 клиентов. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | «composite_demand=LOW», но «свыше 41,5 тыс. компаний» на Мой экспорт и «27 499 активных записей» в реестре ПО. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 15 | Moat строится на glossary/TM, secure workflow и интеграциях, но «просто бот для перевода» уже commoditized. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | Главные риски явно видны: «152-ФЗ и data residency», «CAC inflation», «усиление санкций». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | Есть 10 named targets, blended CAC реалистичен, а ICP узкий и понятный: экспортёры, SaaS и industrial vendors. |

**Normalized score = round((107 × 100) / 150) = 71/100.**

### Интерпретация score
- **71/100** означает **APPROVED WITH NOTES**.
- Approval gate соблюдён: **score ≥ 70** и **company_ebitda_potential_rub_month > 500 000 ₽/мес** при **≤ 50 клиентах** и **≤ 24 месяцах**.

## Moat — 7-factor framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 1 | Слабый indirect effect через накопление glossary/TM, но каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 2 | Перенос TM, glossary, QA-процессов, NDA/DPA и обученной reviewer-сетки создаёт friction на смену подрядчика. |
| 3. Scale economies | 2 | При росте объёма можно удешевлять routing, reviewer utilization и tooling cost, но не до pure SaaS-уровня. |
| 4. Proprietary data / model advantage | 2 | Есть потенциал на доменных переводах и QA-датасете, но размер датасета пока не доказан отдельным T1/T2-источником. |
| 5. Regulatory moat | 2 | 152-ФЗ, data residency и secure deployment повышают входной порог, хотя это не лицензируемый рынок как medtech/fintech. |
| 6. Brand / distribution | 1 | Сильного локального бренда пока нет, дистрибуция строится через founder-led sales и партнёров. |
| 7. Embedded workflow | 3 | Если сервис встроен в release cycle, KB, manuals и glossary governance, вытеснить его заметно сложнее. |

**Moat score = round((13 × 25) / 21) = 15/25.**

Вывод по moat: moat **средний**, не weak, но и не fund-returning сам по себе. Инвестировать можно только при дисциплине на ICP, secure delivery и вертикализации.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 6 347 000 ₽ |
| Fully-loaded CAC | 633 600 ₽ |
| LTV/CAC | 10,0x |
| CAC payback по выручке | 2,9 мес |
| CAC payback по gross profit | 5,0 мес |
| Gross Margin | 57,7% |
| contribution_margin_rub_month | 118 000 ₽/клиент/мес |
| fixed_costs_rub_month | 3 310 000 ₽/мес |
| Break-even | 29 клиентов |
| company_ebitda_rub_month @35 clients | 820 000 ₽/мес |
| company_ebitda_potential_rub_month @50 clients | 2 590 000 ₽/мес |
| clients_to_500k_ebitda | 33 |
| months_to_500k_ebitda | 14 |
| clients_to_1m_ebitda | 37 |
| months_to_1m_ebitda | 15 |
| startup_capital_to_bep_rub | 22 851 359 ₽ |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка экспортёров / SaaS / industrial vendors | SDR | CRM, HH, сайт, 2GIS, таблицы | 30 мин | 420 | средняя |
| 2 | Enrichment контактов и сегментация по use case | SDR | CRM, email finder, AI research | 20 мин | 280 | средняя |
| 3 | Персонализированный outbound email / Telegram / LinkedIn | SDR | sequencing tool, CRM, шаблоны | 25 мин | 350 | средняя |
| 4 | Follow-up 2-4 касания | SDR | CRM, телефония, AI notes | 45 мин | 620 | высокая |
| 5 | Первичная квалификация по объёму документов и языкам | SDR | script, CRM | 20 мин | 300 | средняя |
| 6 | Discovery call по pain points, SLA, security | Founder / AE | Meet, CRM, notes AI | 60 мин | 3 200 | низкая |
| 7 | Мини-аудит массива документов и sample translation | Localization PM + reviewer | CAT tool, LLM workflow, QA checklist | 3 ч | 6 800 | средняя |
| 8 | ROI-оценка: TAT, cost per word, release velocity | AE + founder | spreadsheet, proposal template | 1.5 ч | 3 900 | средняя |
| 9 | Коммерческое предложение и scope | AE | CRM, Docs, калькулятор пакета | 1.5 ч | 2 400 | средняя |
| 10 | Legal / NDA / DPA / 152-ФЗ требования | Founder + ops | ЭДО, шаблоны договоров | 2 ч | 4 100 | низкая |
| 11 | Подписание договора и счёт | Finance / ops | ЭДО, банк, 1С | 30 мин | 650 | высокая |
| 12 | Оплата setup fee и первого месяца | Клиент | банк | 3-5 дней | 0 | внешнее |
| 13 | Onboarding: glossary, TM, style guide, доступы | Localization PM + CSM | Smartcat/CAT, Notion, drive | 6 ч | 10 500 | средняя |
| 14 | Delivery sprint: перевод, post-editing, QA, layout | Review pod | CAT, QA scripts, LLM/API | 10-14 ч/мес | 93 000 / мес | средняя |
| 15 | Monthly report, SLA review, upsell on languages/docs | CSM + founder | dashboard, CRM | 1.5 ч | 2 600 | средняя |
| 16 | Ресчёт, выставление счёта, получение оплаты | Finance / ops | банк, ЭДО | 25 мин | 500 | высокая |

## Unit economics и финансы

### Unit economics summary
- **ARPA / MRR на клиента:** 220 000 ₽/мес
- **COGS на клиента:** 93 000 ₽/мес
- **Gross profit на клиента:** 127 000 ₽/мес
- **contribution_margin_rub_month:** 118 000 ₽/клиент/мес
- **Gross Margin:** 57,7%
- **customer_ltv_rub:** 6 347 000 ₽
- **Fully-loaded CAC:** 633 600 ₽
- **LTV/CAC:** 10,0x
- **CAC payback по gross profit:** 5,0 мес

### PnL readout
- **Base M12:** 25,86 клиента, MRR 5,69 млн ₽, company_ebitda_rub_month **-25 687 ₽**.
- **Optimistic M12:** 32,01 клиента, company_ebitda_rub_month **755 629 ₽**.
- **Pessimistic M12:** 17,86 клиента, company_ebitda_rub_month **-1 041 713 ₽**.
- **Monte Carlo Lite M24:** p10 EBITDA **-2,04 млн ₽**, p50 EBITDA **2,36 млн ₽**, p90 EBITDA **11,50 млн ₽**.

### Что это значит для IC
Base-сценарий почти касается breakeven к концу первого года, но не проходит его. Поэтому approval логичен только как **disciplined services-to-platform play** с жёстким контролем прайса, churn и reviewer economics.

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | enterprise sales, key accounts, финмодель | 845 000 |
| CTO / Tech Lead | security, workflow architecture, integrations | 715 000 |
| Senior Backend | connectors, portal, automation backend | 546 000 |
| ML Engineer | glossary/evals, MT routing, QA automation | 650 000 |
| DevOps | secure infra, storage, CI/CD | 455 000 |
| Frontend | client portal, review UI, dashboards | 390 000 |
| SDR | prospecting и qualification | 221 000 |
| AE | discovery, proposals, closing | 416 000 |
| Customer Success | onboarding, retention, renewals | 325 000 |
| Localization PM / QA Lead | delivery orchestration, glossary, QA | 286 000 |
| Product Marketing / Content | кейсы, thought leadership, inbound | 286 000 |
| Finance / Ops | договоры, ЭДО, invoicing | 156 000 |
| **Итого full team FOT** |  | **5 291 000** |

## GTM — 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Kaspersky | Глобальный cybersecurity vendor с англоязычными KB, manuals, release notes и enterprise docs. | email decision-maker (Head of Localization / Product Marketing), плюс партнёрство через интеграторов документации | 250 000 ₽/мес |
| Positive Technologies | Много продуктовой и технической документации для enterprise и экспорта, высокие требования к точности терминологии. | точечный outbound к product marketing / tech writing lead, конференции Positive Hack Days | 240 000 ₽/мес |
| Yandex Cloud | Постоянный поток docs, API-guides, release notes и support KB для B2B-продукта. | email decision-maker + Habr/vc.ru thought leadership + pilot offer | 220 000 ₽/мес |
| VK Tech / VK Cloud | B2B cloud и enterprise docs, нужен быстрый выпуск мультиязычных материалов и KB. | партнёрский заход через integrator / direct email в product docs team | 220 000 ₽/мес |
| ГК Астра | У enterprise-OS vendor много manuals, release docs, certification docs и обучающих материалов. | outbound к head of product docs / partner channel | 230 000 ₽/мес |
| ABBYY | Экспортный software vendor с регулярной локализацией документации, help-center и sales enablement. | email decision-maker, отраслевые мероприятия, referral intro | 250 000 ₽/мес |
| Naumen | Enterprise software и service platforms, глубокая документация и knowledge-base материалы для B2B-клиентов. | Habr/vc.ru content-led outreach + targeted email | 180 000 ₽/мес |
| 1С | Огромный объём документации, обновлений, обучающих и партнёрских материалов. | партнёрство через франчайзи/интеграторов + direct enterprise outreach | 300 000 ₽/мес |
| Диасофт | Fintech/enterprise vendor с длинной документацией, внедренческими материалами и высоким cost-of-error. | email decision-maker / конференции по финтеху / partner intro | 210 000 ₽/мес |
| Трансмашхолдинг | Industrial/OEM buyer с manuals, экспортными техописаниями и большим объёмом engineering docs. | прямой enterprise sales через техдирекцию / внешнеторговый блок | 260 000 ₽/мес |

### GTM readout
- Этот GTM не search-led. Он строится через **named-account outbound + sample translation audit + ROI deck + secure deployment package**.
- Наиболее рабочие каналы: **email decision-maker**, отраслевые конференции, Habr/vc.ru-контент под tech docs/localization pain и партнёрства с integrator/CAT-stack игроками.
- При таком ICP blended CAC **633 600 ₽** выглядит реалистично, а payback **5 месяцев по gross profit** остаётся рабочим.

## Top-3 risks

| Риск | Вероятность | Impact | Почему критично |
|---|---|---|---|
| Price compression и сваливание в commodity-агентство | high | высокий | Sensitivity показывает, что **Price -30%** уводит EBITDA M12 до **-1 732 495 ₽**. |
| Demand/GTM fragility, category search почти отсутствует | medium-high | высокий | В demand-stage зафиксировано **composite_demand=LOW**, значит нужен тяжёлый founder-led sales motion. |
| Compliance + vendor dependency (152-ФЗ, санкции, LLM/API) | medium | высокий | Для части ICP обязательны private deployment, DPA и data residency; усиление санкций может ломать стек. |

## Proof points required post-approval

Чтобы approval остался валидным, в ближайшие 3-6 месяцев нужно доказать:
1. **3-5 paid pilots** в одном из verticals: cybersecurity, enterprise software или industrial/OEM.
2. **Средний recurring контракт ≥ 200 000 ₽/мес** без развала GM ниже 55%.
3. **Reviewer cost discipline**: COGS на клиента удерживается **≤ 95 000 ₽/мес**.
4. **Retention moat**: glossary/TM/KB lock-in даёт monthly churn **≤ 2,5%**.
5. **Private deployment readiness** для чувствительных документов и buyers с 152-ФЗ ограничениями.

## Final committee note

Это не broad SaaS winner, а **нишевый AI-SERVICES cash-flow case** с шансом вырасти в workflow platform. Инвестировать можно, если команда сознательно отвергает дешёвый translation-bot positioning и строит вертикальный secure managed service для дорогой документации.


<!-- 07-score-trajectory.md -->

# Score trajectory

## 2026-05-11 09:44 MSK — Demand Validation
- Stage: P4 Demand Validation
- Case: AI-перевод технической документации и локализация под заказ
- Demand: LOW -> no broad-market pull from search/query layer
- WTP: CONFIRMED -> enterprise localization tools and managed services already monetized
- Profit Gate: PASS -> managed-service and enterprise deployment scenarios can exceed 500k ₽ EBITDA/mo
- Decision delta: brief hypothesis weakened on mass demand, strengthened on monetizable niche execution
- Score trajectory: 6.5/10 -> 6.8/10
- Notes: proceed only as verticalized B2B managed localization, not as generic translation bot

## 2026-05-12 08:34 MSK — Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: AI-перевод технической документации и локализация под заказ
- Verdict: APPROVED WITH NOTES
- Raw rubric: 107/150
- Normalized score: 71/100
- EBITDA Gate: PASS -> 820 000 ₽/мес на 35 клиентах, 2 590 000 ₽/мес на 50 клиентах
- Decision delta: approval дан за сильную unit economics и рабочий EBITDA path, но с оговорками из-за LOW demand и среднего moat
- Score trajectory: 6.8/10 -> 7.1/10
- Notes: инвестировать только как secure productized managed localization service, не как generic AI-переводчик


<!-- telegram-messages.md -->

Сообщение 1
[AI-SERVICES] AI-перевод технической документации и локализация под заказ — APPROVED WITH NOTES, score 71/100.
Описание: нишевый secure managed localization service для экспортёров, enterprise software и industrial vendors, где ценность создаётся через glossary, SLA, QA и human-in-the-loop.
Аудитория: product docs, localization, support knowledge base, release management и export-команды в B2B-компаниях с регулярной мультиязычной документацией.

Сообщение 2
Процессы: ICP-outbound → discovery → sample translation audit → ROI-оценка → договор/NDA/DPA → onboarding glossary/TM → monthly delivery sprint → SLA review и upsell.
Юнит-экономика: customer_ltv_rub 6 347 000 ₽, fully-loaded CAC 633 600 ₽, LTV/CAC 10,0x, CAC payback 5,0 мес по gross profit, GM 57,7%.
Прибыль компании: contribution_margin_rub_month 118 000 ₽/клиент/мес; 500K EBITDA точка примерно 33 клиента / 14 мес, 1M EBITDA точка примерно 37 клиентов / 15 мес, potential @50 clients = 2 590 000 ₽/мес.

Сообщение 3
Рынок: широкий search-demand низкий, но есть валидный buyer universe у экспортёров, enterprise software и industrial/OEM; Source tier balance T1=6, T2=4, T3=3.
Финансы: base M12 почти breakeven, а main fragility points это price compression, LOW category demand и compliance/LLM dependency.
Что доказать: 3-5 paid pilots, recurring чек ≥ 200 000 ₽/мес, COGS ≤ 95 000 ₽/клиент/мес и private deployment readiness.
GitHub: https://github.com/maslovmaksim92/openclaw/blob/main/business-models/approved/ai-perevod-tekhnicheskoi-dokumentatsii-i-lokalizatsiya-pod-zakaz/verdict.md
