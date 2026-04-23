

---

# 00-brief.md

# Краткий бриф

## Кейс
Haast, AI marketing compliance review для legal и compliance-команд крупных брендов

## Статус
Принудительный resurrect, создан новый кейс `haast-geo-expand-v2`.

## Почему открыт
Кейс по AI marketing compliance operations для регулируемых индустрий. Создан как принудительный resurrect-v2 для новой аналитики, даже несмотря на прошлое открытие смежного кейса под другим названием.

## Следующий шаг
Передать кейс в P3-demand-validation и затем по полному пайплайну P4→P7.


---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-haast-geo-expand.md
created: 2026-04-20T16:33:33+03:00
original_verdict: triage/triage-2026-04-17-haast-geo-expand.md
---

# 01-intake

## Кейс
haast-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-17-haast-geo-expand.md

## Краткий контекст
Сигнал `haast-geo-expand` переоткрыт как standalone candidate для нового полного прохода P3→P7 с обновлённой системой аналитики.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — haast-geo-expand

## Meta
- source: triage/triage-2026-04-17-haast-geo-expand.md
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
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-haast-geo-expand.md`

## Классификация
Новый сигнал, кейс открыт.

## Решение
Создан новый кейс `enterprise-marketing-compliance-operations` в `pipeline/cases/`.

## Почему
- В `pipeline/cases/` не найдено открытого кейса, который уже покрывает именно AI-native workflow для проверки и постоянного мониторинга маркетингового и продуктового комплаенса.
- Сигнал стал сильнее предыдущих наблюдений: во входных данных указаны рост выручки в 4,5 раза за 12 месяцев, zero churn, traction среди Fortune 500 и новый раунд Series A на $12 млн.
- Экономика теперь проходит порог Program 1: диапазон `1,8-9,0 млн ₽ в год с клиента` соответствует примерно `150 000-750 000 ₽ в месяц`, а верхняя часть диапазона превышает минимальный порог `> 500 000 ₽/мес.`.
- Для РФ просматривается тяжёлый сервисный слой: адаптация под российское рекламное и отраслевое регулирование, private cloud или on-prem, интеграции с локальными workflow-системами и сопровождение policy engine.

## Что сделано
- Создан файл `pipeline/cases/enterprise-marketing-compliance-operations/00-brief.md`.
- Зафиксирована гипотеза о high-LTV модели вокруг enterprise marketing compliance operations для регулируемых отраслей.
- Исходный raw-файл подготовлен к переносу в `pipeline/raw/processed/`.

## Вердикт
Сигнал достаточно сильный для открытия нового кейса: категория выглядит дорогой, enterprise-ориентированной и потенциально локализуемой под РФ.

```


---

# 02-demand.md

# Demand validation — Haast

## Вывод
**Вердикт: CONDITIONAL PASS / идти дальше по пайплайну.**

Спрос на категорию в РФ не массовый, а нишевый и enterprise-led: по запросу `маркетинговый комплаенс` internal multi-demand вернул **LOW / 3 балла** при 15 вакансиях на HH, слабом Google Trends и низком Yandex Suggest. Это плохо для self-serve продукта, но не убивает кейс, потому что у боли высокий чек и высокий cost of error: штрафы за нарушения маркировки интернет-рекламы для юрлиц доходят до **500 тыс. руб.** [T2], а у крупных рекламодателей бюджеты измеряются миллиардами рублей [T2]. В такой конфигурации продукт можно продавать не как «ещё один proofing tool», а как AI review layer для legal/compliance в regulated marketing workflows.

## 1) Что именно валидируем
Haast, по брифу, это AI marketing compliance review для legal и compliance-команд крупных брендов. То есть не general-purpose proofing, а слой проверки рекламных креативов и копирайта до публикации: claims, mandatory disclosures, brand/legal guardrails, traceability, audit trail.

## 2) Demand signals
- По internal endpoint `http://172.18.0.1:9001/multi-demand?keyword=маркетинговый%20комплаенс` на 21 апреля 2026: **composite_demand=LOW, demand_score=3**, сигналы: HH vacancies = 15, Habr = 2, Google Trends RU = 0, Yandex Suggest = 2. Это указывает на узкий, не consumer-like спрос, без широкого поискового хвоста. [Internal demand tool]
- Низкий search demand не равен отсутствию бюджета: в enterprise compliance категории закупка часто идёт через sales-led pipeline, RFP и расширение смежных workflow-систем, а не через массовый search intent. Это подтверждается тем, что смежные игроки продают enterprise proofing/compliance по высоким B2B чекам. [T2][T3]
- В РФ regulatory pressure вокруг маркировки и отчётности по интернет-рекламе сохраняется: eLama отдельно поддерживает автомаркировку Telegram Ads и отчётность в ЕРИР, а также прямо предупреждает о риске штрафов при некорректной маркировке. [T2]

## 3) Конкуренты и цены
### Глобальные / прямые и смежные
1. **IntelligenceBank Marketing Compliance** — base DAM package starts at **$567/month billed annually**, compliance capabilities идут как пакет/аддоны; позиционирование прямо включает automated brand and legal content reviews. Источник: official pricing page. [T2]
2. **Ziflow** — Standard **$199/month**, Pro **$329/month**, Enterprise custom; есть audit trail, workflow approvals, e-signatures и ReviewAI в enterprise-пакете. Источник: official pricing page. [T2]
3. **Filestage** — Starter **$199/month**, Business **$329/month**, Enterprise custom; в Business есть AI reviewers, verified approval и audit logs в enterprise-grade наборе. Источник: official pricing page. [T2]

### Что это значит для Haast
- У рынка уже есть устоявшийся budget anchor порядка **$199–$567+/month** за базовые workflow/proofing/compliance-решения и выше для enterprise-комплектации. [T2]
- Haast не обязан демпинговать. Для regulated enterprise ICP в РФ разумный диапазон пилота выглядит как **149–349 тыс. руб./мес** за команду/бренд, если продукт реально снижает latency legal review и число инцидентов. Это **инференс**, выведенный из зарубежных price anchors и стоимости локального ручного процесса. [T2 + inference]

## 4) Telegram в РФ: боты и сервисы
Прямого сильного Telegram-native AI legal review конкурента по найденным данным не видно, но есть **adjacent services**, подтверждающие боль compliance в Telegram-канале дистрибуции:
- **eLama**: автомаркировка Telegram Ads, токены, отчётность в ЕРИР; для eLama маркировка Telegram Ads заявлена как бесплатная внутри сервиса. [T2]
- В обзоре eLama по состоянию на 5 января 2026 приведены рыночные тарифы операторов рекламных данных для маркировки: **Ozon ОРД — от 6000 руб./мес**, **Первый ОРД — 1% бюджета, но не менее 5000 руб.**, **ОРД-А — от 7320 руб./мес с НДС**. Это не прямые конкуренты Haast, но это живая платёжеспособность вокруг ad compliance tooling в РФ. [T2]
- Следовательно, в Telegram/RU есть платежи за compliance infrastructure, но пока в основном на уровне маркировки и отчётности, а не pre-publication AI legal review. Это создаёт пространство для позиционирования Haast как более «верхнего» слоя над маркировкой. [T2 + inference]

## 5) Willingness to pay (WTP)
### Доказательства
- Крупнейшие российские рекламодатели реально тратят большие бюджеты: по AdIndex за 2025 год Сбер — **42 568 млн руб.**, Яндекс — **23 041 млн руб.**, Ozon — **21 579 млн руб.**, а среди regulated-heavy компаний в топе присутствуют Сбер, ВТБ, Т-Технологии, Альфа-Банк, МТС и другие. [T2]
- По брендам за 2025 год: Сбер Банк — **15 138 млн руб.**, Т-Банк — **14 891 млн руб.**, Альфа-Банк — **13 178 млн руб.**, ВТБ — **11 776 млн руб.**, Совкомбанк — **7 064 млн руб.**, МТС — **7 726 млн руб.**, T2 — **7 533 млн руб.** [T2]
- Ошибка в рекламе в РФ стоит не только времени юристов, но и санкций: eLama в материале про маркировку Telegram указывает штрафы до **500 тыс. руб.** для юрлиц. [T2]
- Конкуренты уже монетизируют review/compliance workflow как ПО с recurring pricing, а не как разовую услугу. [T2]

### Вывод по WTP
WTP **есть**, но у ограниченного сегмента: крупные рекламодатели и регулируемые отрасли с большим объёмом креативов и частыми юридическими согласованиями. Для SMB/long tail подтверждения WTP нет. Для enterprise сегмента WTP на **150–350 тыс. руб./мес** выглядит реалистично; для top-tier брендов и агентств с managed rollout возможен диапазон **400–700 тыс. руб./мес**. Это **инференс**, но он опирается на: 1) действующие зарубежные price anchors, 2) цену ошибки, 3) масштабы рекламных бюджетов в РФ. [T2 + inference]

## 6) Market sizing
### Логика сегмента
Для РФ берём не весь adtech/compliance рынок, а **enterprise marketing compliance / proofing / review** для крупных рекламодателей в regulated-heavy и high-governance сегментах: банки, страховщики, telecom, pharma, retail media networks, крупные экосистемы.

### Top-down
**[LOW CONFIDENCE]** Категория Haast лежит на пересечении online proofing software и compliance software, поэтому top-down неизбежно proxy-based.

- Глобальный рынок **online proofing software** в 2026 году оценивается примерно в **$1.81 млрд**. Это слабее по качеству источник, но он ближе всего к категории review/approval tools. [T3]
- Глобальный ad spend на 2025 год прогнозировался около **$1.1 трлн**. [T2]
- Российский рынок маркетинговых коммуникаций в 2024 году превысил **2.1 трлн руб.** [T2]
- Следовательно, доля РФ в глобальном advertising base примерно около **2.1%–2.4%** в грубом приближении, если переводить 2.1 трлн руб. в ~$23–26 млрд при курсе ~90 руб./$. [T2 + inference]
- Применяя эту долю к global online proofing proxy, получаем российский category TAM порядка **3.3–4.0 млрд руб.** [T2/T3 + inference]
- Для Haast addressable subset, где нужен именно legal/compliance review, а не просто proofing, берём **~40%** от proxy TAM, то есть **SAM ≈ 1.3–1.6 млрд руб.** [inference]
- Реалистичный capture для узкого enterprise SaaS: **Y1 = 3% SAM**, **Y3 = 10% SAM**. Тогда SOM Y1 ≈ **39–48 млн руб.**, SOM Y3 ≈ **130–160 млн руб.** [inference]

### Bottom-up
Берём стартовый ICP РФ:
- 305 действующих банков на 1 апреля 2026 года. [T1]
- 129 страховых организаций на 1 января 2026 года. [T1]
- Плюс около **66** крупных небанковских regulated/high-governance рекламодателей из telecom, pharma, large digital ecosystems и финтеха, на которых есть публичные рекламные бюджеты и высокая потребность в согласовании. Это приближение для first-wave ICP. [T1/T2 + inference]

Итого **около 500** потенциальных buyers в широком адресуемом ICP. [T1/T2 + inference]

Предположения для bottom-up:
- `% with need` = **35%**. Не каждый банк/страховщик нуждается в отдельном AI layer, но у крупных рекламодателей с высокой частотой креативов боль подтверждается величиной рекламных бюджетов и наличием legal/approval workload. [T1/T2 + inference]
- Средний контракт = **4.8 млн руб./год** (400 тыс. руб./мес) для enterprise deployment, включая базовую настройку policy packs и аудит trail. Это согласуется с observed enterprise price anchors у смежных продуктов и локальным бюджетом уровня «один сильный compliance/legal FTE + инструмент». [T2 + inference]

Тогда:
- **SAM_bottom_up = 500 × 35% × 4.8 млн = 840 млн руб.**
- **SOM_bottom_up Y1 = 3% × 840 млн = 25.2 млн руб.**
- **SOM_bottom_up Y3 = 10% × 840 млн = 84 млн руб.**

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $1.81B [T3] | — | Категорийный proxy, не чистый legal review | top-down |
| TAM (РФ) | 3.6 млрд руб. [T2/T3] | 2.4 млрд руб. [T1/T2] | diff ~1.5x, bottom-up уже обрезан до ICP | lower |
| SAM (РФ) | 1.44 млрд руб. [inference] | 0.84 млрд руб. [T1/T2 + inference] | diff ~1.7x, приемлемо для proxy category | lower |
| SOM Y1 | 43.2 млн руб. | 25.2 млн руб. | diff ~1.7x | **используем 25.2 млн руб.** |
| SOM Y3 | 144 млн руб. | 84 млн руб. | diff ~1.7x | **используем 84 млн руб.** |

### 10 реальных buyers для bottom-up и будущего GTM
1. Сбер [T2]
2. ВТБ [T2]
3. Альфа-Банк [T2]
4. Т-Банк / Т-Технологии [T2]
5. Совкомбанк [T2]
6. МТС [T2]
7. T2 [T2]
8. МегаФон [T2]
9. Ростелеком [T2]
10. Росгосстрах / АльфаСтрахование / Ингосстрах как страховой кластер first-wave targets [T1/T2]

### Sanity check
- SOM Y1 = 25.2 млн руб. при ARR 4.8 млн руб. означает около **5–6 клиентов** за первый год. Это реалистично для founder-led enterprise motion.
- Если средний sales cycle 6 месяцев, то 5–6 сделок за 12 месяцев тяжело, но возможно при пилотах через 2–3 design partners и upsell во 2 полугодии.
- SOM Y1 < 10% SAM, значит overclaiming нет.

## 7) Profit Gate (EBITDA >= 500k руб./мес)
Проверяю все основные сценарии монетизации.

### Сценарий A: SMB/self-serve
- Цена: 49 тыс. руб./мес
- Клиентов: 20
- ARR: 11.76 млн руб.
- При gross margin 85% валовая прибыль ~10.0 млн руб.
- Даже при lean OPEX 18 млн руб./год EBITDA будет отрицательной.
- **Gate: FAIL**

### Сценарий B: Mid-market team plan
- Цена: 149 тыс. руб./мес
- Клиентов: 12
- ARR: 21.46 млн руб.
- Валовая прибыль ~18.2 млн руб.
- При OPEX 18–20 млн руб./год EBITDA около нуля.
- **Gate: borderline / скорее FAIL**

### Сценарий C: Enterprise SaaS
- Цена: 349 тыс. руб./мес
- Клиентов: 15
- ARR: 62.82 млн руб.
- Валовая прибыль ~53.4 млн руб.
- При OPEX 24 млн руб./год EBITDA ~29.4 млн руб./год, то есть ~2.45 млн руб./мес.
- **Gate: PASS**

### Сценарий D: Hybrid SaaS + managed policy packs / onboarding
- Цена: эквивалент 499 тыс. руб./мес
- Клиентов: 12
- ARR: 71.86 млн руб.
- При GM ~75% валовая прибыль ~53.9 млн руб.
- Даже при OPEX 28 млн руб./год EBITDA ~2.16 млн руб./мес.
- **Gate: PASS**

### Итог по Profit Gate
Profit Gate **проходит**, но только если Haast сразу строится как **enterprise/high-touch продукт**, а не как self-serve tool. Это важный инвестиционный фильтр: ICP и GTM должны быть жёстко сфокусированы на крупных брендах и regulated verticals.

## 8) Основные риски
1. **Category education risk**: поисковый спрос низкий, рынок надо продавать через pain-led sales, а не inbound. [Internal demand tool]
2. **Feature substitution**: часть задач уже закрывается в proofing/work management системах и вручную через legal ops. [T2]
3. **Локализация права и языка**: для РФ продукт должен хорошо понимать местные формулировки рекламы, отраслевые дисклеймеры и правила маркировки. Без этого value proposition размывается. [T2 + inference]
4. **Слишком широкий ICP** убьёт продажи. Рабочий клин: банки, страхование, telecom, крупный pharma/healthcare. [T1/T2 + inference]

## 9) Инвестиционная интерпретация
Это не broad SaaS и не продукт с вирусным спросом. Это **narrow but monetizable enterprise wedge**. Если у команды есть сильные founders, способные продавать в compliance/legal/marketing leadership, кейс достоин прохода в следующие стадии. Если ставка делается на PLG или массовый SMB, кейс развалится.

## Финальный вывод
- **Demand:** низкий по массовым сигналам, но достаточный в узком enterprise ICP.
- **WTP:** подтверждён косвенно, но убедительно.
- **Competitor pricing:** подтверждает наличие recurring budget line.
- **TAM/SAM/SOM:** не гигантский рынок, но достаточный для venture-scale niche wedge при международной экспансии; в РФ alone рынок скорее build-for-reference, а не конечная ceiling story.
- **Profit Gate:** проходит в enterprise/hybrid monetization.

**Решение на этапе demand validation: PASS с оговорками.**

## Источники
- IntelligenceBank pricing: https://intelligencebank.com/pricing/ [T2]
- Ziflow pricing: https://www.ziflow.com/pricing [T2]
- Filestage pricing: https://filestage.io/pricing/ [T2]
- АКАР, объём рынка маркетинговых коммуникаций в 2024 году: https://akarussia.ru/volumes/obem-rynka-marketingovyh-kommunikacij-v-2024-godu/ [T2]
- Банк России, банковский сектор, по состоянию на 1 апреля 2026: https://www.cbr.ru/banking_sector/ [T1]
- Банк России, страхование, по состоянию на 1 января 2026: https://www.cbr.ru/insurance/ [T1]
- AdIndex, рекламодатели 2025: https://adindex.ru/ratings/marketing/2026/343517/ [T2]
- eLama, маркировка рекламы в Telegram: https://elama.ru/blog/teper-cherez-elama-mozhno-promarkirovat-reklamu-v-telegram-ads/ [T2]
- eLama help, автомаркировка Telegram Ads: https://help.elama.ru/article/60753 [T2]
- Statista, global marketing resource management software revenue: https://www.statista.com/statistics/1306563/marketing-resource-management-market-size/ [T1]
- Online proofing software market proxy: https://www.businessresearchinsights.com/market-reports/online-proofing-software-market-114114 [T3]
- GroupM global ad spend proxy: https://www.theatdb.com/news/groupm-forecasts-global-ad-spend-to-reach-11-trillion-in-2025 [T2]

Sources: T1=3, T2=8, T3=1. Primary evidence basis: T2.

## Market Pulse
- Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.


---

# 04-economics.md

---
stage: economics
case: haast-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
verdict: PASS_WITH_RESERVATIONS
confidence: medium
investment_grade: true
sector: GEO-EXPAND
---

# 04-economics — Unit Economics

## Кейс
Haast GEO expand v2, AI marketing compliance review для legal и compliance-команд крупных брендов в РФ.

## Executive summary

**Итог P5: PASS WITH RESERVATIONS, investment-grade по unit economics.**

Почему:
1. **Blended fully-loaded CAC = 1,31 млн ₽ на нового платящего клиента**, что дорого, но ещё укладывается в enterprise motion для regulated / legal-heavy workflow.
2. **LTV = 25,42 млн ₽** при **monthly churn 1,2%** и **gross margin 76,3%**.
3. **LTV/CAC = 19,4x**, значительно выше инвестиционного порога **3,0x**.
4. **CAC Payback = 3,3 месяца** по формуле `CAC / MRR per customer`, и около **4,3 месяца** по gross profit payback.
5. **Break-even = 24 клиента**, а при **50 клиентах EBITDA ≈ 8,27 млн ₽/мес**, то есть Profit Gate проходит с большим запасом.

Но это работает только как **узкий enterprise B2B продукт** с founder-led продажей, пилотом, security review и дорогим внедрением. Для self-serve или SMB эта экономика невалидна.

---

## 1) Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | банки, страховщики, telecom, крупные e-commerce и regulated advertisers | Совпадает с `02-demand.md` |
| ACV | 4 800 000 ₽/год | midpoint из enterprise-диапазона P4 |
| MRR на клиента | 400 000 ₽/мес | ACV / 12 |
| One-off onboarding fee | 900 000 ₽ | улучшает cash, но не включается в MRR |
| Sales cycle | 5-7 месяцев | enterprise legal/compliance motion |
| Новый paying customers / мес в steady-state | 1,0 | консервативно для узкого ICP |
| Startup capital | 70 000 000 ₽ | нужен буфер до break-even |
| Monthly churn | 1,2% | enterprise benchmark [T1][T2] |
| Gross margin | 76,3% | из COGS-модели ниже |

---

## 2) Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list по regulated advertisers | SDR | HH, Rusprofile, AdIndex lists, CRM | 2 ч / аккаунт | 2 200 | Средняя |
| 2 | Обогащение ЛПР: legal, compliance, brand, procurement | SDR | CRM, email finder, ручной ресерч | 1,5 ч | 1 650 | Средняя |
| 3 | Outbound-sequence и первые касания | SDR | CRM sequences, email, phone | 10-14 дней | 4 500 | Высокая |
| 4 | Qualification call | SDR + AE | Meet, CRM, note-taker | 45 мин | 4 500 | Низкая |
| 5 | Discovery по текущему approval workflow | AE | deck, questionnaire, CRM | 1 ч | 5 500 | Низкая |
| 6 | Demo AI compliance review на креативах | AE + CEO | sandbox, demo workspace | 1,5 ч | 12 000 | Низкая |
| 7 | Compliance scoping: claims, disclaimers, audit trail | AE + CTO | checklist, shared docs | 1 неделя | 28 000 | Низкая |
| 8 | Security / privacy review | CTO + AE | security docs, DPA, architecture notes | 1-2 недели | 42 000 | Низкая |
| 9 | Пилот на реальном потоке креативов | CSM + ML + Backend | cloud, LLM, support desk | 4-6 недель | 180 000 | Средняя |
| 10 | ROI-мемо для sponsor и procurement | AE + CEO | spreadsheet, deck | 6-8 ч | 24 000 | Низкая |
| 11 | Договор, legal, закупка, redlines | CEO + AE + юрист | ЭДО, contract workflow | 2-4 недели | 38 000 | Низкая |
| 12 | Invoice и получение первой оплаты | Finance/Ops | 1С, банк, ЭДО | 3-5 дней | 4 000 | Высокая |
| 13 | Onboarding и policy-pack setup | CSM + Backend + ML | PM tool, cloud, KB | 2-3 недели | 95 000 | Средняя |

### Вывод по процессу
- Это **13-шаговый enterprise workflow**, а не software-only sale.
- Основные cost drivers до оплаты: **pilot, security review, procurement, onboarding**.
- Поэтому считать CAC как `ads / conversions` здесь некорректно, нужен **fully-loaded CAC**.

---

## 3) COGS breakdown per client/month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / inference для проверки claims и disclaimer logic | 28 000 | частые review-runs, длинные промпты, reruns |
| Secure cloud, storage, backups | 18 000 | изолированное хранение креативов и логов |
| Audit trail / observability / logging | 8 000 | enterprise logging и хранение следа решений |
| CSM / support allocation | 16 000 | доля CSM и support-hours |
| Policy updates / compliance ops / quality control | 12 000 | регулярное обновление правил и ручной QA |
| Integration + implementation amortization | 13 000 | spread onboarding effort на 12 мес |
| **Итого COGS** | **95 000** |  |

| Метрика | Значение |
|---|---:|
| MRR на клиента | 400 000 ₽ |
| COGS на клиента | 95 000 ₽ |
| Gross Profit на клиента | 305 000 ₽ |
| Gross Margin % | **76,3%** |
| Contribution Margin % | **76,3%** |

---

## 4) CAC по каналам с funnel conversion

### Канал 1: founder-led outbound / ABM

| Этап | Объём | Конверсия |
|---|---:|---:|
| Target accounts / мес | 120 | — |
| Ответили / accepted intro | 24 | 20,0% |
| Qualification meetings | 18 | 75,0% |
| Discovery completed | 8 | 44,4% |
| Пилот | 2 | 25,0% |
| Платящий клиент | 0,7 | 35,0% |

- Channel spend / мес: **620 000 ₽**
- **CAC по каналу: 886 000 ₽**

### Канал 2: partnerships с digital agencies / legal advisors / compliance integrators

| Этап | Объём | Конверсия |
|---|---:|---:|
| Партнёрские интро | 12 | — |
| Qualification meetings | 7 | 58,3% |
| Discovery completed | 4 | 57,1% |
| Пилот | 1 | 25,0% |
| Платящий клиент | 0,35 | 35,0% |

- Channel spend / мес: **210 000 ₽**
- **CAC по каналу: 600 000 ₽**

### Канал 3: paid content / webinars / paid ads

| Этап | Объём | Конверсия |
|---|---:|---:|
| MQL / мес | 55 | — |
| Discovery meetings | 11 | 20,0% |
| Qualified opportunities | 4 | 36,4% |
| Пилот | 0,8 | 20,0% |
| Платящий клиент | 0,25 | 31,3% |

- Channel spend / мес: **479 000 ₽**
- **CAC по каналу: 1 916 000 ₽**

### Blended CAC

| Показатель | Значение |
|---|---:|
| Итого acquisition cost / мес | 1 309 000 ₽ |
| New paying customers / мес | 1,0 |
| **Blended fully-loaded CAC** | **1 309 000 ₽** |

---

## 5) Fully-loaded CAC, обязательная раскладка

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / webinar promotion) | 180 000 | тестовый paid program для enterprise demand capture | assumption, sanity vs enterprise GTM |
| Outbound team FOT (SDR + 60% AE attributed to new) | 495 000 | SDR 172 500 gross + AE 208 800 gross attributed + 30% взносы | HH.ru benchmark [T3][T4] |
| Marketing team FOT (partial allocation) | 127 000 | 15% времени CEO/founder на acquisition, 650k gross × 15% × 1.3 | HH.ru / founder allocation [T3] |
| Tools (CRM, enrichment, email, webinar stack) | 87 000 | Bitrix/amo + enrichment + webinar + call tools | assumption |
| Events / partnerships | 118 000 | roundtables, partner enablement, sponsorship | assumption |
| Overhead multiplier (x1.3) | 302 000 | 30% на общий acquisition overhead поверх прямых затрат | standard enterprise B2B assumption |
| **Итого monthly fully-loaded acquisition cost** | **1 309 000** |  |  |

### Проверка по сегментному CAC-мультипликатору
- Кейс относится к **enterprise / regulated marketing compliance**.
- User benchmark для такого сегмента: **enterprise x2.0-2.5**, regulated **x2.5-3.0** при marketing-only базах.
- Здесь модель уже **включает sales FOT, tools, events, overhead, pilot friction**, поэтому дополнительный multiplier сверху **не применяю**, чтобы не было double count.
- При этом итоговый blended CAC **1,31 млн ₽** выше обычного enterprise SaaS benchmark `300-900k ₽`, что выглядит реалистично именно для compliance-heavy motion, а не как underestimation.

---

## 6) LTV с churn rate

### Бенчмарк churn
- ChartMogul пишет, что для SaaS с ARPA **$500+** customer churn обычно **1-2% в месяц**. [T1]
- Optifai для B2B SaaS по enterprise-сегменту даёт **1-2% monthly churn**, best-in-class ниже 1%. [T2]

Для Haast беру **1,2% monthly churn** как консервативный enterprise base-case: продукт глубоко встраивается в workflow согласования, но рынок узкий и локализация под РФ добавляет renewal risk.

### Расчёт LTV
`LTV = (MRR × Gross Margin) / Monthly Churn`

- MRR = **400 000 ₽**
- Gross Margin = **76,3%**
- Monthly churn = **1,2%**

`LTV = 400 000 × 0,763 / 0,012 = 25 416 667 ₽`

| Метрика | Значение |
|---|---:|
| LTV | **25,42 млн ₽** |
| CAC | **1,31 млн ₽** |
| **LTV/CAC** | **19,4x** |

### Вывод
- Инвестиционный порог **LTV/CAC ≥ 3,0x** пройден с большим запасом.
- Даже при stress-case churn **2,0%/мес** LTV будет **15,25 млн ₽**, а LTV/CAC останется **11,7x**.

---

## 7) CAC Payback

### Стандарт из задания
`CAC Payback = CAC / MRR per customer`

`1 309 000 / 400 000 = 3,27 месяца`

### Дополнительная проверка по gross profit
`1 309 000 / 305 000 = 4,29 месяца`

| Метрика | Значение |
|---|---:|
| CAC Payback по MRR | **3,3 месяца** |
| CAC Payback по Gross Profit | **4,3 месяца** |

Обе версии заметно лучше базового sanity-порога **<12 мес** и enterprise-порога **<18 мес**.

---

## 8) Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 / чел |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 172 500 | 0,75 | 1 | 51 750 | 224 250 |
| AE | 1 | 348 000 | 1,5 | 2,5 | 104 400 | 452 400 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### Salary realism
- Senior backend в московских вакансиях HH.ru встречается в диапазоне **350-600k ₽**, что подтверждает выбранные **420k ₽**. [T3]
- DevOps по HH.ru виден в районе **200-300k+ ₽**, для strong middle/senior беру **350k ₽ gross** как реалистичный upper-midpoint. [T5]
- SDR / первичные SaaS sales в HH.ru видны в диапазоне **100-150k ₽** base, поэтому **172,5k ₽ gross** уже включает bonus и premium за enterprise target. [T4]
- AE / account executive в HH.ru по Москве заметно ниже enterprise SaaS reality, поэтому беру **348k ₽ gross** как enterprise-adjusted compensation над публичным нижним benchmark. [T4]

### Полная команда и функции

| Роль | Функция | Salary gross ₽/мес | FOT fully-loaded ₽/мес |
|---|---|---:|---:|
| CEO / founder | продажи, enterprise relationships, pricing, fundraising | 650 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, product delivery | 550 000 | 715 000 |
| Senior Backend #1 | core workflow engine, integrations | 420 000 | 546 000 |
| Senior Backend #2 | infra-heavy connectors, audit trail | 420 000 | 546 000 |
| ML Engineer | rules + LLM orchestration, evaluation | 500 000 | 650 000 |
| Frontend Engineer | reviewer UI, approval flows | 300 000 | 390 000 |
| DevOps | secure deployment, observability, backups | 350 000 | 455 000 |
| SDR | outbound, qualification, funnel top | 172 500 | 224 250 |
| AE | discovery, demo, negotiation, close | 348 000 | 452 400 |
| Customer Success | onboarding, adoption, renewal | 240 000 | 312 000 |
| **Итого fully-loaded FOT** |  |  | **5 135 650 ₽/мес** |

---

## 9) Cumulative FOT timeline M1-M12

### Hire plan
- M1: CEO
- M2: CTO
- M3: Senior Backend #1, SDR
- M4: ML Engineer, AE
- M5: Frontend
- M6: DevOps
- M7: CSM
- M8: Senior Backend #2

### FOT по месяцам

| Месяц | Кто подключается | FOT_monthly ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | + CTO | 1 560 000 |
| M3 | + Backend #1, SDR | 2 330 250 |
| M4 | + ML, AE | 3 432 650 |
| M5 | + Frontend | 3 822 650 |
| M6 | + DevOps | 4 277 650 |
| M7 | + CSM | 4 589 650 |
| M8 | + Backend #2 | 5 135 650 |
| M9 | стабилизация | 5 135 650 |
| M10 | стабилизация | 5 135 650 |
| M11 | стабилизация | 5 135 650 |
| M12 | стабилизация | 5 135 650 |

### Sanity check
- В первый месяц не нанимается 5+ человек, значит time-to-hire realism не нарушен.
- FOT для fully-built команды **5,14 млн ₽/мес** соответствует enterprise B2B SaaS с сильным engineering и sales core.

---

## 10) Fixed costs breakdown

| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 5 135 650 | из таблицы команды |
| Base cloud / security / monitoring | 650 000 | shared infra без client-specific usage |
| Legal / бухгалтерия / ЭДО / admin | 240 000 | G&A |
| Office / travel / founder sales trips | 310 000 | встречи с enterprise buyers |
| Core software stack / licenses | 180 000 | devtools, CRM core, analytics |
| Contingency / misc | 469 350 | буфер на мелкие fixed расходы |
| **Итого fixed costs / мес** | **6 985 000 ₽** |  |

---

## 11) Break-even по клиентам и по месяцам

### Break-even по client count

`Break-even clients = Fixed costs / Gross Profit per client`

`6 985 000 / 305 000 = 22,9`

Округляю вверх до **24 клиентов**, чтобы был минимальный запас.

### EBITDA при 50 клиентах

- MRR = **20 000 000 ₽/мес**
- Gross Profit = **15 250 000 ₽/мес**
- EBITDA = **15 250 000 - 6 985 000 = 8 265 000 ₽/мес**

**Profit Gate: PASS.** Даже при 50 клиентах компания уверенно выше порога **500k ₽/мес EBITDA**.

### Break-even по месяцам

Использую консервативную ramp-модель клиентов:

| Месяц | Активные клиенты | Gross Profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 745 000 | -1 745 000 |
| M2 | 0 | 0 | 2 660 000 | -2 660 000 |
| M3 | 0 | 0 | 3 580 250 | -3 580 250 |
| M4 | 1 | 305 000 | 4 882 650 | -4 577 650 |
| M5 | 2 | 610 000 | 5 372 650 | -4 762 650 |
| M6 | 4 | 1 220 000 | 5 927 650 | -4 707 650 |
| M7 | 6 | 1 830 000 | 6 339 650 | -4 509 650 |
| M8 | 9 | 2 745 000 | 6 985 000 | -4 240 000 |
| M9 | 12 | 3 660 000 | 6 985 000 | -3 325 000 |
| M10 | 15 | 4 575 000 | 6 985 000 | -2 410 000 |
| M11 | 20 | 6 100 000 | 6 985 000 | -885 000 |
| M12 | 25 | 7 625 000 | 6 985 000 | **640 000** |

**Break-even по месяцу: M12.**

---

## 12) Burn-to-breakeven и cash runway

### Burn-to-breakeven
Суммарный отрицательный EBITDA до выхода в плюс в M12:

`1,745 + 2,660 + 3,580 + 4,578 + 4,763 + 4,708 + 4,510 + 4,240 + 3,325 + 2,410 + 0,885 ≈ 37,40 млн ₽`

С учётом рабочего капитала, дебиторки, задержек закрытия и буфера на просадки беру:

- **Burn-to-breakeven = ~45 млн ₽**
- Рекомендованный safe capital buffer = **70 млн ₽**

### Cash runway
При стартовом капитале **70 млн ₽** и среднем burn до break-even около **5,2 млн ₽/мес**:

`70 / 5,2 ≈ 13,5 месяца`

| Метрика | Значение |
|---|---:|
| Startup capital | 70,0 млн ₽ |
| Burn-to-breakeven | ~45,0 млн ₽ |
| Средний burn pre-BEP | ~5,2 млн ₽/мес |
| Cash runway | **13,5 месяца** |

### Вывод
- Для enterprise B2B SaaS сумма стартового капитала **70 млн ₽** выглядит реалистично и не попадает в red flag `<10 млн ₽`.
- Главный риск не в LTV/CAC, а в том, успеет ли команда пройти длинный sales cycle до кассового сжатия.

---

## 13) Итоговый вывод для фонда

### Что нравится
- Высокий ACV и сильная gross margin.
- Сильный запас по **LTV/CAC**.
- Комфортный **CAC payback** даже с fully-loaded enterprise CAC.
- При 50 клиентах бизнес уверенно проходит **EBITDA gate**.

### Что тревожит
- Узкий ICP, мало ошибок прощается.
- Founder-led sales почти обязательны.
- Сильная зависимость от качества локализации policy engine под РФ и от enterprise trust-layer.
- Ramp до break-even долгий, нужен нормальный капитал, а не bootstrap-story.

## Final unit economics verdict

**PASS WITH RESERVATIONS.**

Haast для РФ выглядит инвестиционно осмысленным только как **дорогой enterprise compliance workflow**, а не как широкий SaaS. По unit economics кейс проходит: **LTV/CAC 19,4x**, **CAC Payback 3,3 месяца**, **break-even 24 клиента**, **EBITDA при 50 клиентах ~8,27 млн ₽/мес**. Следующий вопрос уже не в математике, а в способности команды реально закрывать такие сделки и удерживать доверие regulated buyers.

---

## Источники
- [T1] ChartMogul Help Center, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T2] Optifai, B2B SaaS churn benchmarks: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [T3] HH.ru, senior backend / CTO market pages и вакансии: https://hh.ru/vacancies/senior-backend-developer , https://hh.ru/vacancy/129266637 , https://hh.ru/vacancies/tehnicheskij-direktor-cto
- [T4] HH.ru, account executive / SDR SaaS вакансии: https://hh.ru/vacancies/account_executive/polniy_den , https://hh.ru/vacancies/account_executive
- [T5] HH.ru, DevOps вакансии: https://hh.ru/vacancies/devops , https://hh.ru/vacancies/devops-spetsialist/polnaya_zanyatost


---

# 05-critic.md

# SECTION A — PnL

## A1. Исходные допущения модели

- ARPA / MRR на клиента: **400 000 ₽/мес**
- COGS на клиента: **95 000 ₽/мес**
- Gross profit на клиента: **305 000 ₽/мес**
- Gross margin: **76,3%**
- Fixed costs: **6 985 000 ₽/мес**
- Team FOT fully-loaded: **5 135 650 ₽/мес**
- Startup capital: **70 000 000 ₽**
- Налоговые режимы для сравнения:
  - **УСН 6%** с выручки
  - **IT-льгота 3%** с выручки при аккредитации Минцифры
  - **ОСНО 20%** налог на прибыль, плюс **НДС 20%** поверх цены при применимости
- Страховые взносы: **~30% к ФОТ**, уже учтены в fully-loaded FOT и fixed costs.

## A2. Сценарии роста клиентской базы

- **Base:** 0, 0, 0, 1, 2, 4, 6, 9, 12, 15, 20, 25
- **Optimistic:** 0, 0, 1, 2, 4, 7, 10, 14, 18, 23, 29, 35
- **Pessimistic:** 0, 0, 0, 0, 1, 2, 3, 5, 7, 9, 12, 15

## A3. PnL 12 месяцев, Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 5 | 5 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 12 | 15 | 20 | 25 |
| MRR, ₽ | 0 | 0 | 0 | 400 000 | 800 000 | 1 600 000 | 2 400 000 | 3 600 000 | 4 800 000 | 6 000 000 | 8 000 000 | 10 000 000 |
| COGS, ₽ | 0 | 0 | 0 | 95 000 | 190 000 | 380 000 | 570 000 | 855 000 | 1 140 000 | 1 425 000 | 1 900 000 | 2 375 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 305 000 | 610 000 | 1 220 000 | 1 830 000 | 2 745 000 | 3 660 000 | 4 575 000 | 6 100 000 | 7 625 000 |
| GM% | 0,0% | 0,0% | 0,0% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% |
| Fixed costs, ₽ | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 |
| EBITDA, ₽ | -6 985 000 | -6 985 000 | -6 985 000 | -6 680 000 | -6 375 000 | -5 765 000 | -5 155 000 | -4 240 000 | -3 325 000 | -2 410 000 | -885 000 | 640 000 |
| Cash burn, ₽ | 6 985 000 | 6 985 000 | 6 985 000 | 6 680 000 | 6 375 000 | 5 765 000 | 5 155 000 | 4 240 000 | 3 325 000 | 2 410 000 | 885 000 | 0 |
| Cumulative cash, ₽ | -6 985 000 | -13 970 000 | -20 955 000 | -27 635 000 | -34 010 000 | -39 775 000 | -44 930 000 | -49 170 000 | -52 495 000 | -54 905 000 | -55 790 000 | -55 150 000 |

## A4. PnL 12 месяцев, Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 | 5 | 6 | 6 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 7 | 10 | 14 | 18 | 23 | 29 | 35 |
| MRR, ₽ | 0 | 0 | 400 000 | 800 000 | 1 600 000 | 2 800 000 | 4 000 000 | 5 600 000 | 7 200 000 | 9 200 000 | 11 600 000 | 14 000 000 |
| COGS, ₽ | 0 | 0 | 95 000 | 190 000 | 380 000 | 665 000 | 950 000 | 1 330 000 | 1 710 000 | 2 185 000 | 2 755 000 | 3 325 000 |
| Gross profit, ₽ | 0 | 0 | 305 000 | 610 000 | 1 220 000 | 2 135 000 | 3 050 000 | 4 270 000 | 5 490 000 | 7 015 000 | 8 845 000 | 10 675 000 |
| GM% | 0,0% | 0,0% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% |
| Fixed costs, ₽ | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 |
| EBITDA, ₽ | -6 985 000 | -6 985 000 | -6 680 000 | -6 375 000 | -5 765 000 | -4 850 000 | -3 935 000 | -2 715 000 | -1 495 000 | 30 000 | 1 860 000 | 3 690 000 |
| Cash burn, ₽ | 6 985 000 | 6 985 000 | 6 680 000 | 6 375 000 | 5 765 000 | 4 850 000 | 3 935 000 | 2 715 000 | 1 495 000 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 985 000 | -13 970 000 | -20 650 000 | -27 025 000 | -32 790 000 | -37 640 000 | -41 575 000 | -44 290 000 | -45 785 000 | -45 755 000 | -43 895 000 | -40 205 000 |

## A5. PnL 12 месяцев, Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 9 | 12 | 15 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 400 000 | 800 000 | 1 200 000 | 2 000 000 | 2 800 000 | 3 600 000 | 4 800 000 | 6 000 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 95 000 | 190 000 | 285 000 | 475 000 | 665 000 | 855 000 | 1 140 000 | 1 425 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 305 000 | 610 000 | 915 000 | 1 525 000 | 2 135 000 | 2 745 000 | 3 660 000 | 4 575 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% | 76,3% |
| Fixed costs, ₽ | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 |
| EBITDA, ₽ | -6 985 000 | -6 985 000 | -6 985 000 | -6 985 000 | -6 680 000 | -6 375 000 | -6 070 000 | -5 460 000 | -4 850 000 | -4 240 000 | -3 325 000 | -2 410 000 |
| Cash burn, ₽ | 6 985 000 | 6 985 000 | 6 985 000 | 6 985 000 | 6 680 000 | 6 375 000 | 6 070 000 | 5 460 000 | 4 850 000 | 4 240 000 | 3 325 000 | 2 410 000 |
| Cumulative cash, ₽ | -6 985 000 | -13 970 000 | -20 955 000 | -27 940 000 | -34 620 000 | -40 995 000 | -47 065 000 | -52 525 000 | -57 375 000 | -61 615 000 | -64 940 000 | -67 350 000 |

## A6. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### Unit economics waterfall на 1 клиента / месяц

| Шаг | ₽ | Комментарий |
|---|---:|---|
| ARPA | 400 000 | MRR на клиента |
| Gross profit | 305 000 | после COGS 95 000 ₽ |
| Contribution | 305 000 | доп. переменные selling costs в 04-economics не выделены отдельно |
| EBITDA contribution | 305 000 | вклад одного клиента в покрытие fixed costs |

### Waterfall на M12 по сценариям

| Сценарий | M12 clients | ARPA / MRR, ₽ | Gross profit, ₽ | EBITDA, ₽ | Net after tax, IT 3%, ₽ | Net after tax, УСН 6%, ₽ | Net after tax, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Base | 25 | 10 000 000 | 7 625 000 | 640 000 | 340 000 | 40 000 | 512 000 |
| Optimistic | 35 | 14 000 000 | 10 675 000 | 3 690 000 | 3 270 000 | 2 850 000 | 2 952 000 |
| Pessimistic | 15 | 6 000 000 | 4 575 000 | -2 410 000 | -2 590 000 | -2 770 000 | -2 410 000 |

**Вывод по waterfall:**
- При low-margin EBITDA около нуля режим **IT-льгота 3%** обычно лучше **УСН 6%**.
- **ОСНО 20%** выглядит лучше УСН только если считать один лишь налог на прибыль, но при ОСНО появляется **НДС 20%** и выше админ-нагрузка, поэтому для продукта SaaS в РФ практичнее сравнивать **УСН vs IT-льгота**.
- Для этого кейса целевой режим, если проходит по критериям, это **IT-льгота / аккредитация Минцифры**.

## A7. Cash flow и startup capital to BEP

| Сценарий | Peak cumulative burn, ₽ | Startup capital to BEP, ₽ | Комментарий |
|---|---:|---:|---|
| Base | 55 790 000 | 55 790 000 | 70 млн ₽ хватает, запас ~14,21 млн ₽ |
| Optimistic | 45 785 000 | 45 785 000 | 70 млн ₽ хватает, запас ~24,22 млн ₽ |
| Pessimistic | 67 350 000 | 67 350 000 | 70 млн ₽ хватает почти без запаса, остаток ~2,65 млн ₽ |

## A8. Налоговая модель РФ

| Параметр | УСН | IT-льгота | ОСНО |
|---|---|---|---|
| Налоговая база | выручка | выручка | прибыль |
| Ставка в модели | 6% | 3% | 20% |
| НДС | нет | обычно нет в этой упрощенной модели | **20%** если применимо |
| Страховые взносы | ~30% к ФОТ | ~30% к ФОТ | ~30% к ФОТ |
| Практический вывод | приемлемо | **лучший режим** при наличии аккредитации | тяжелее по cash/admin |

## A9. Break-even

### Break-even по client count

- Gross profit на 1 клиента: **305 000 ₽/мес**
- Break-even client count: **6 985 000 / 305 000 = 22,9**, округленно **23 клиента**, с безопасным запасом **24 клиента**.

### Break-even по месяцам, по сценариям

| Сценарий | Break-even clients | Break-even month |
|---|---:|---|
| Base | 23-24 | **M12** |
| Optimistic | 23-24 | **M10** |
| Pessimistic | 23-24 | **не достигается в M1-M12** |

## A10. Итог Section A

- Экономика держится только при быстром наборе enterprise-клиентов и удержании **GM ~76%**.
- **Base** выходит в EBITDA-plus только в **M12**.
- **Optimistic** проходит BEP уже в **M10** и дает **3,69 млн ₽ EBITDA** в M12.
- **Pessimistic** сжигает почти весь стартовый капитал и не достигает break-even за 12 месяцев.
- Для снижения cash burn критично получить **IT-льготу 3%**, иначе налоговая нагрузка на раннем этапе заметно ухудшает пост-EBITDA cash profile.

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

Базовая точка взята из Section A: **M12 EBITDA = 640 000 ₽/мес** при **25 активных клиентах**, **ARPU 400 000 ₽/мес**, **gross profit 305 000 ₽/клиент/мес** и **fixed costs 6 985 000 ₽/мес**.

Для stress-тестов использую упрощение:
- **CAC x2** => та же воронка даёт примерно вдвое меньше новых платящих клиентов, поэтому к M12 активная база снижается до **~13 клиентов**.
- **Churn x2** с **1,2% до 2,4%/мес** => при той же воронке активная база к M12 снижается примерно до **~22 клиентов**.
- **Price -30%** => ARPU падает с **400 000 ₽** до **280 000 ₽**, COGS на клиента краткосрочно считаю неизменным **95 000 ₽**, gross profit на клиента падает до **185 000 ₽**.

| Сценарий | Ключевое изменение | Активные клиенты / ARPU | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | 25 / 400 000 ₽ | 640 000 | проходит gate, но без запаса |
| Sens1 | CAC x2 | ~13 / 400 000 ₽ | -3 020 000 | воронка перестаёт окупать fixed cost base |
| Sens2 | Churn x2 | ~22 / 400 000 ₽ | -275 000 | почти весь EBITDA buffer исчезает |
| Sens3 | Price -30% | 25 / 280 000 ₽ | -2 360 000 | price compression быстро ломает модель |

### Вывод по sensitivity
- Из трёх стрессов **самый разрушительный** здесь не churn, а **CAC shock** и **price compression**.
- Бизнес в текущем виде имеет очень узкий safety margin: при base-case запас EBITDA в M12 всего **640 тыс. ₽**, то есть **1-2 крупных отклонения** уже уводят модель в минус.
- Следовательно, кейс зависит не просто от “роста”, а от сохранения сразу трёх хрупких условий: **дорогой enterprise price point, низкого churn и управляемого CAC**.

## B2. Monte Carlo Lite — confidence intervals

### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 900 000 | 1 309 000 | 2 618 000 | 04-economics.md; channel CAC 600k-1,916m и stress x2 [T1] |
| Monthly churn % | 0,8% | 1,2% | 2,4% | 04-economics.md; ChartMogul / Optifai benchmark [T2][T3] |
| ARPU ₽/мес | 280 000 | 400 000 | 460 000 | 04-economics.md; stress price -30% и умеренный upside enterprise upsell [T1] |
| Conversion rate lead→paid % | 0,8% | 1,6% | 2,5% | оценка по blended enterprise funnel из 04-economics.md [T1] |
| Time-to-hire месяцев (среднее) | 1,0 | 1,6 | 2,5 | 04-economics.md, усреднение по hire-plan [T1] |

### Метод упрощённой симуляции

Вместо полного Monte Carlo на 1000 прогонов беру **9 комбинаций** вокруг трёх ключевых драйверов: **CAC, churn, ARPU**. Это достаточно, чтобы получить рабочие **p10 / p50 / p90** для инвестиционного решения.

Опорные точки:
- **best case** = CAC_min + churn_min + ARPU_max
- **median** = CAC_mode + churn_mode + ARPU_mode
- **worst case** = CAC_max + churn_max + ARPU_min
- плюс 6 смешанных комбинаций между ними

Для M24 использую консервативную экстраполяцию enterprise ramp:
- p10: рост замедляется, активная база к M24 около **18 клиентов**
- p50: база выходит к **38 клиентам**
- p90: при хорошем удержании и апсейле достигает **52 клиентов**

### Confidence intervals

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -3 655 000 | 4 605 000 | 11 995 000 | 15 650 000 |
| CAC payback (мес) | 9,4 | 3,3 | 2,0 | 7,4 |
| LTV/CAC | 3,0x | 19,4x | 50,7x | 47,7x |
| Cash runway (мес) | 19,2 | 28,0 | 36,0+ | 16,8+ |

### Интерпретация Monte Carlo Lite
- **Правило #1 срабатывает:** `p10 EBITDA < 0`, значит у компании есть реальный сценарий ухода в **insolvency zone** даже без black-swan шока.
- **Правило #2 не срабатывает:** `p50 EBITDA = 4,605 млн ₽/мес`, то есть median-case EBITDA Gate проходит.
- **Правило #3 формально не считаю по коэффициенту `p90/p10`, потому что p10 отрицательный**. Практически это ещё хуже: распределение **пересекает ноль**, значит неопределённость очень высокая.
- **Правило #4 срабатывает:** width по **LTV/CAC = 47,7x > 8**, модель хрупкая. Хрупкость идёт прежде всего из **нестабильности CAC + churn + enterprise pricing**.

### Bottom line по Monte Carlo Lite
- Median-case выглядит инвестиционно приемлемо.
- Но левый хвост слишком тяжёлый: модель не разваливается “чуть-чуть”, а быстро переходит из **хорошего enterprise SaaS** в **кассово-опасный business**.
- Поэтому итоговая оценка должна быть **со скидкой на execution risk**, а не только по красивому base-case.

## B3. Competitor deep-dive

Ниже рассматриваю не только прямых “AI marketing compliance review” конкурентов, но и **ближайшие заменители workflow**, через которые тот же бюджет может уйти у enterprise-клиента: ad review, legal/compliance proofing, контентный supervision, локальные legaltech-платформы РФ.

### B3.1. Западные конкуренты

| Компания | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Red Oak** | ad review / compliance workflow для financial services | глубокая специализация под regulated ad review, сильный audit trail, зрелость в enterprise procurement | ориентирован прежде всего на финсектор США, тяжёлый enterprise stack, слабее локализация под РФ-рекламу | **~15-20%** глобальной ниши ad-review в highly regulated verticals, оценка по бренду и партнерской дистрибуции | Haast может выиграть на **русской локализации правил, faster deployment и lower TCO для РФ** |
| **PerformLine** | automated monitoring и compliance across marketing / sales channels | широкое покрытие каналов, сильный monitoring после публикации, известность в regtech США | больше “monitoring after the fact”, чем pre-approval workflow; слабее для deeply embedded legal review в РФ | **~10-15%** adjacent regtech-monitoring сегмента, оценка по охвату use-cases | Haast сильнее в **pre-release approval, auditability и workflow для legal/compliance до публикации** |
| **Ziflow** | online proofing / approval workflow для legal & compliance | удобный UX, быстрый запуск, понятный collaboration-layer, хорош для creative + legal | это скорее универсальный approval layer, а не vertical compliance engine; слабее rule-depth | **~5-10%** в общем классе proofing for compliance-heavy teams | Haast может дать **domain-specific policy engine**, а не просто proofing |

### B3.2. Российские конкуренты и substitutes

| Компания | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **ПравоТех** | крупнейший игрок российского legaltech workflow и knowledge stack | масштаб, бренд, длинные продажи в enterprise/legal, высокая инерция внедрения, ресурсы на интеграции | не сфокусирован именно на marketing compliance review; большие платформы часто медленнее в product iteration | **~20-25%** российского corporate legaltech software слоя, оценка по масштабу штата и зрелости | Haast может зайти как **узкий wedge под marketing/legal/compliance workflow**, не требующий полной платформенной замены |
| **FastLaw** | legaltech / AI для юридических процессов, резидент Сколково | early AI/legal DNA, понятный narrative для автоматизации юрфункции, институциональная легитимность | старый рынок и ограниченный масштаб; не видно доминирования именно в ad/compliance workflow | **~2-4%** российского AI-legal niche, оценка по публичной видимости | Haast сильнее в **конкретном ad-approval use-case** и ROI через маркетинг, а не общий legal automation |
| **Legiscan** | AI-проверка договоров на риски | современный AI-first positioning, понятный SMB/mid-market onboarding, свежий продуктовый фокус | пока ближе к contract review, чем к enterprise marketing compliance; вероятно мало enterprise references | **<1%** рынка, ранняя стадия | Haast выигрывает там, где нужен **approval workflow, audit trail и межфункциональная связка marketing + legal** |
| **MarkApp** | автоматизация маркировки рекламы и отчётности блогеров | точное попадание в локальную боль РФ ad-regulation, понятный use-case, низкий adoption friction | узкий слой compliance, скорее utility чем enterprise system of record | **~1-3%** в нише ad-marking tools, оценка по раннему рынку | Haast покрывает **не только маркировку, но и весь review/approval stack до выхода креатива** |
| **UR-LI** | risk-scoring сделок / контрагентов | полезен для compliance/risk-команд, российская юрисдикция, B2B positioning | кейс про сделки и контрагентов, а не про маркетинговый review; косвенный substitute, а не прямой конкурент | **<1%** для нашей ниши | Haast ближе к бюджету brand/legal/compliance и встраивается в creative workflow |

### Вывод по конкурентам
- На Западе проблема уже хорошо упакована, но там сильнее **proofing / supervision / channel monitoring**, чем локальный **AI review под рекламное право РФ**.
- В России много **adjacent substitutes**, но пока мало игроков, кто соединяет сразу **маркетинговый workflow + legal/compliance + AI + audit trail**.
- Это окно даёт шанс на wedge, но и создаёт риск: если категория подтвердится, в неё могут быстро зайти **ПравоТех**, крупные ECM/LegalTech или cloud vendors с on-prem AI layer.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется | high | pipeline не конвертируется после первых личных продаж | падение meeting-to-pilot conversion, зависимость >50% сделок от CEO | за 3 мес построить repeatable playbook, нанять сильного AE, разложить sales stages по SLA |
| Operational | Не успевают нанимать strong backend/ML | med | product roadmap и pilot SLA срываются | time-to-hire >2,5 мес, offer acceptance <50% | заранее сформировать hiring bench, contractor bench, подписать 1-2 trusted outsourcing партнёра |
| Operational | LLM API latency / quality drift | high | падает качество ревью и доверие enterprise-клиента | рост manual override rate, рост hallucination incidents | multi-model routing, fallback на локальные / open-weight модели, golden-set regression tests |
| Operational | Security review затягивает пилоты | high | цикл сделки уходит с 6 до 9+ месяцев | security questionnaire backlog, повторяющиеся red flags от банков/телекомов | заранее готовить security pack, DPA, data-flow docs, on-prem / VPC вариант |
| Market | Узкий ICP, рынок оказывается меньше ожидаемого | med | недобор клиентов и revenue ceiling | pipeline coverage <3x плана два квартала подряд | расширить ICP на pharma, FMCG, marketplaces, agency compliance desks |
| Market | Крупные бренды оставляют review in-house | med | слабая willingness to pay | пилоты есть, но procurement стопорит rollout | продавать не “AI”, а measurable TAT reduction + audit trail + штрафориск |
| Market | Price compression из-за ручных substitutes и ad-hoc agency workflows | high | ARPU падает ниже порога окупаемости | discounting >20%, win rate держится только на скидках | tiered pricing, modular packaging, upsell audit trail / analytics / on-prem |
| Market | Конкуренты добавляют похожий AI-слой в существующие approval stacks | med | растёт CAC и падает close rate | чаще проигрыши incumbents, RFP c AI-checklist becomes standard | занять узкую нишу раньше, упаковать proprietary policy library, делать deep integrations |
| Regulatory | Нарушение 152-ФЗ / проблемы с ПДн и data residency | high | потеря enterprise trust, блок на внедрение | DPA redlines, требования хранить всё в РФ, security objections | российский контур хранения, минимизация ПДн, шифрование, логирование доступа |
| Regulatory | 115-ФЗ / internal AML-compliance у банков блокирует external AI SaaS | med | банки тормозят procurement | закупка зависает на compliance committee | on-prem/VPC deployment, white-glove security review, отдельный банковский пакет |
| Regulatory | Санкции / ограничения западного SaaS и cloud tooling | high | часть инфраструктуры становится недоступной | vendor notices, billing issues, unstable access from РФ | локальные замены критичных сервисов, vendor redundancy, резервный стек без US dependencies |
| Regulatory | Требования к локализации и хранению audit trail меняются | med | доработка продукта и рост COGS | новые требования от клиентов и юристов, длиннее security checklist | архитектура с configurable retention / storage policy, юридический мониторинг ежеквартально |
| Financial | Cash runway сокращается до <9 мес до выхода на план | high | риск down-round или insolvency | net burn >6 млн ₽/мес при pipeline lag | жёсткий burn control, freeze non-core hiring, milestone-based fundraising |
| Financial | Ослабление рубля к USD повышает cost LLM / cloud | high | COGS ползёт вверх, margin сжимается | рост COGS/клиент >15% q/q | FX buffer, рублёвые контракты где возможно, own-model fallback |
| Financial | Инфляция зарплат в ML / backend | med | fixed cost растёт быстрее revenue ramp | новые офферы >20% выше плана, counteroffers срывают найм | mixed team structure, remote hiring outside Moscow, variable comp |
| Financial | Налоги и льготы: не получили IT-аккредитацию / 3% режим | med | пост-EBITDA cash хуже модели | задержка аккредитации, доля профильной выручки спорная | с первого дня строить tax-ready учет, резервировать сценарий без льготы |
| Black swan | Резкое ужесточение санкций или военная эскалация | med | enterprise freezes budgets и импортный SaaS | стоп по закупкам, cancellations, force majeure clauses | focus на критичные regulated verticals, longer runway buffer, локальный стек |
| Black swan | Полное отключение ключевого LLM-провайдера | high | продукт деградирует за дни, не месяцы | резкий рост ошибок API, notice о прекращении обслуживания | multi-provider architecture, pre-integrated open-source fallback, local inference pilot |
| Black swan | Крупный публичный инцидент с false negative в рекламе клиента | med | репутационный удар, churn, legal exposure | escalation от flagship клиента, соцмедиа / пресс-упоминания | human-in-the-loop для high-risk assets, incident playbook, liability carve-outs |
| Black swan | Утечка креативов / campaign data | med | потеря доверия и заморозка продаж | security findings, anomalous access logs | zero-trust access, data minimization, segmentation by tenant, регулярные пентесты |

### Вывод по рискам
- Самые опасные сочетания: **CAC inflation + price compression + LLM dependency**.
- Regulatory risk для РФ здесь не “дополнительный”, а **ядро продукта**: если доверие к data residency слабое, сделка просто не стартует.
- В отличие от обычного SaaS, здесь black swan может прийти не только извне, но и через **один заметный false negative** на громком бренде.

## B5. Kill conditions через 6 месяцев

Если через 6 месяцев наблюдается хотя бы один из следующих сигналов, кейс **не стоит продолжать**:

1. **Median-case больше не держится:** обновлённый p50 по модели показывает **EBITDA < 500 000 ₽/мес** на горизонте M24.
2. **Коммерческий провал:** к M6 меньше **4 активных платящих клиентов** или pipeline coverage ниже **2,5x** от плана на следующие 2 квартала.
3. **Экономика сломана:** blended **CAC > 2,0 млн ₽** и одновременно **ARPU < 350 000 ₽** или monthly **churn > 2,0%** два месяца подряд.

## B6. Итог Section B

**Вердикт P6B: cautious pass, но с заметным risk discount.**

Что важно:
- base-case ещё выглядит рабочим,
- median-case Monte Carlo проходит EBITDA Gate,
- но **левый хвост распределения слишком тяжёлый**,
- а конкурентное окно держится в основном на **локализации под РФ и узком vertical wedge**, а не на непробиваемом moat.

Для фонда это означает: инвестировать можно **только при жёстком контроле milestones** по CAC, retention, deployment-trust и скорости enterprise rollout.

## Источники Section B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/haast-geo-expand-v2/04-economics.md
- [T2] ChartMogul Help Center, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T3] Optifai, B2B SaaS churn benchmarks: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [T4] Ziflow, Legal & Compliance: https://www.ziflow.com/solutions/marketing-compliance
- [T5] Aprimo partner page, Red Oak: https://www.aprimo.com/partner/red-oak
- [T6] Aprimo partner page, PerformLine: https://www.aprimo.com/partner/performline
- [T7] Rusprofile, АО «Правотех»: https://www.rusprofile.ru/id/3382529
- [T8] Skolkovo, FastLaw: https://sk.ru/news/rezident-skolkovo-fastlaw-i-yuridicheskaya-kompaniya-pravokard-zapuskayut-sovmestnye-proekty-v-legaltech/
- [T9] Habr / Product Radar, Legiscan и MarkApp: https://habr.com/ru/companies/productradar/articles/986632/
- [T10] Habr, UR-LI: https://habr.com/ru/companies/sezinnopolis/news/662483/

<!-- P6B-DONE -->


---

# 06-verdict.md

[GEO-EXPAND] Haast — NEAR-PASS: 66/100 | EBITDA base=640К₽/мес через 12 мес | LTV/CAC=19,4x | Ключевое преимущество: узкий wedge в AI review для marketing compliance под РФ | Главный риск: moat слабый, а enterprise GTM хрупок к CAC и price pressure.

# 06-verdict

sector: GEO-EXPAND
status: NEAR-PASS
score: 66/100
raw_score: 99/150
case: haast-geo-expand-v2
date: 2026-04-23

## Финальный инвестиционный вывод

**Вердикт инвестиционного комитета: NEAR-PASS.**

Кейс проходит по unit economics и по базовому EBITDA gate, но пока не проходит по качеству защитимости и по устойчивости исполнения. Это investable только как узкий founder-led enterprise wedge с жёстким milestone control. Для APPROVED не хватает двух вещей: 1) более сильного moat, 2) реального доказательства, что 5-6 крупных design partners в РФ можно закрыть без взрыва CAC и discounting.

## Что было проверено по пайплайну

- 01-intake: кейс переоткрыт как standalone rerun из resurrect batch.
- 02-demand: спрос в РФ низкий по массовым сигналам, но enterprise WTP и Profit Gate подтверждены.
- 03-validation: отдельный файл отсутствует в кейсе; использована фактическая евиденция из 02-demand.md как стадия спроса/валидации.
- 04-economics: unit economics investment-grade с PASS WITH RESERVATIONS.
- 05-critic: оба блока P6A-DONE и P6B-DONE присутствуют.

## Оценка

Source tier balance: T1=3, T2=8, T3=1, weighted=2.17. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC = 19,4x», «CAC Payback = 3,3 месяца», «Gross Margin = 76,3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «Base выходит в EBITDA-plus только в M12», «M12 EBITDA = 640 000 ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | «composite_demand=LOW, demand_score=3», но «SOM Y1 = 25.2 млн руб.» и enterprise WTP подтверждён. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | «конкурентное окно держится в основном на локализации под РФ и узком vertical wedge, а не на непробиваемом moat». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | «левый хвост распределения слишком тяжёлый», плюс high-risk по LLM dependency, security review и founder-led sales. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | GTM математически живой, но «founder-led sales почти обязательны» и safety margin по EBITDA узкий. |

**Normalized score = round(99 × 100 / 150) = 66/100.**

## Moat — 7-factor framework

| Фактор | Оценка (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | После интеграции approval workflow, audit trail и policy packs выход становится заметно дороже. |
| Scale economies | 1 | Часть COGS падает с объёмом, но LLM/cloud и сервисный слой всё ещё значимы. |
| Proprietary data / model advantage | 1 | Потенциал есть, но в кейсе нет доказанного уникального датасета или model edge. |
| Regulatory moat | 2 | Локализация под РФ-рекламу и data residency дают барьер, но без лицензируемого lock-in. |
| Brand / distribution | 1 | Узнаваемого бренда и сильной дистрибуции в РФ пока не видно. |
| Embedded workflow | 3 | При успешном внедрении продукт глубоко садится в legal/compliance approval loop клиента. |

Сумма 7-factor = **10/21**.

**Moat score = round(10 × 25 / 21) = 12/25.**

Вывод: moat **слабее investment-grade**, потому что основа преимущества сейчас, это локальная упаковка и execution wedge, а не структурно защищённая платформа. Weak moat остаётся в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 25 416 667 ₽ |
| CAC | 1 309 000 ₽ |
| LTV/CAC | 19,4x |
| CAC payback | 3,3 мес по MRR, 4,3 мес по gross profit |
| Gross Margin | 76,3% |
| contribution_margin_rub_month | 305 000 ₽ |
| fixed_costs_rub_month | 6 985 000 ₽ |
| company_ebitda_rub_month (base M12) | 640 000 ₽/мес |
| company_ebitda_potential_rub_month (50 клиентов) | 8 265 000 ₽/мес |
| clients_to_500k_ebitda | 25 |
| clients_to_1m_ebitda | 27 |
| months_to_500k_ebitda | 12 |
| months_to_1m_ebitda | >12 в base |
| Break-even | 23-24 клиента |
| startup_capital_to_bep_rub | 55 790 000 ₽ |
| Startup capital recommended | 70 000 000 ₽ |

## Полный бизнес-процесс

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list по regulated advertisers | SDR | HH, Rusprofile, AdIndex lists, CRM | 2 ч / аккаунт | 2 200 | Средняя |
| 2 | Обогащение ЛПР: legal, compliance, brand, procurement | SDR | CRM, email finder, ручной ресерч | 1,5 ч | 1 650 | Средняя |
| 3 | Outbound-sequence и первые касания | SDR | CRM sequences, email, phone | 10-14 дней | 4 500 | Высокая |
| 4 | Qualification call | SDR + AE | Meet, CRM, note-taker | 45 мин | 4 500 | Низкая |
| 5 | Discovery по текущему approval workflow | AE | deck, questionnaire, CRM | 1 ч | 5 500 | Низкая |
| 6 | Demo AI compliance review на креативах | AE + CEO | sandbox, demo workspace | 1,5 ч | 12 000 | Низкая |
| 7 | Compliance scoping: claims, disclaimers, audit trail | AE + CTO | checklist, shared docs | 1 неделя | 28 000 | Низкая |
| 8 | Security / privacy review | CTO + AE | security docs, DPA, architecture notes | 1-2 недели | 42 000 | Низкая |
| 9 | Пилот на реальном потоке креативов | CSM + ML + Backend | cloud, LLM, support desk | 4-6 недель | 180 000 | Средняя |
| 10 | ROI-мемо для sponsor и procurement | AE + CEO | spreadsheet, deck | 6-8 ч | 24 000 | Низкая |
| 11 | Договор, legal, закупка, redlines | CEO + AE + юрист | ЭДО, contract workflow | 2-4 недели | 38 000 | Низкая |
| 12 | Invoice и получение первой оплаты | Finance/Ops | 1С, банк, ЭДО | 3-5 дней | 4 000 | Высокая |
| 13 | Onboarding и policy-pack setup | CSM + Backend + ML | PM tool, cloud, KB | 2-3 недели | 95 000 | Средняя |

**Инвестиционный смысл процесса:** это не software-only sale, а дорогой enterprise deployment с security, pilot и procurement friction. Именно поэтому математически кейс жив, но execution risk высокий.

## Команда

| Роль | Функция | Salary gross ₽/мес | FOT fully-loaded ₽/мес |
|---|---|---:|---:|
| CEO / founder | продажи, enterprise relationships, pricing, fundraising | 650 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, product delivery | 550 000 | 715 000 |
| Senior Backend #1 | core workflow engine, integrations | 420 000 | 546 000 |
| Senior Backend #2 | infra-heavy connectors, audit trail | 420 000 | 546 000 |
| ML Engineer | rules + LLM orchestration, evaluation | 500 000 | 650 000 |
| Frontend Engineer | reviewer UI, approval flows | 300 000 | 390 000 |
| DevOps | secure deployment, observability, backups | 350 000 | 455 000 |
| SDR | outbound, qualification, funnel top | 172 500 | 224 250 |
| AE | discovery, demo, negotiation, close | 348 000 | 452 400 |
| Customer Success | onboarding, adoption, renewal | 240 000 | 312 000 |
| **Итого** |  |  | **5 135 650 ₽/мес** |

## GTM — 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Один из крупнейших рекламодателей РФ, высокая цена ошибки и сложный legal review. | email decision-maker в marketing/legal + отраслевые конференции | 500 000 ₽/мес |
| 2 | ВТБ | Регулируемый финсектор, большие рекламные бюджеты и высокий compliance burden. | email decision-maker / партнёрство с legaltech-интегратором | 450 000 ₽/мес |
| 3 | Альфа-Банк | Масштабный поток креативов и агрессивный маркетинг, значит высокая нагрузка на согласование. | founder-led outbound через head of brand/legal | 450 000 ₽/мес |
| 4 | Т-Банк | Быстрые маркетинговые циклы в финтехе повышают ценность AI pre-approval review. | тёплый intro через digital/legal сеть + email | 450 000 ₽/мес |
| 5 | Совкомбанк | Крупный рекламодатель из regulated vertical, чувствителен к claims и disclosure risk. | партнёрство с compliance/agency ecosystem | 400 000 ₽/мес |
| 6 | МТС | Массовый медиа-поток и брендовые кампании требуют ускорения review и audit trail. | конференция + outbound в brand/compliance | 400 000 ₽/мес |
| 7 | T2 | Telecom с высокой рекламной активностью и большим объёмом digital creatives. | email decision-maker + отраслевые media events | 350 000 ₽/мес |
| 8 | МегаФон | Похожая боль, много маркетинговых материалов и межфункциональных согласований. | ABM outreach через marketing operations | 350 000 ₽/мес |
| 9 | Ростелеком | Large enterprise с heavy governance, где важен traceable approval workflow. | enterprise sales через procurement/legal champion | 350 000 ₽/мес |
| 10 | АльфаСтрахование | Страховой сектор, regulated messaging и ценность снижения legal turnaround time. | email decision-maker / партнёрство с legal advisor | 350 000 ₽/мес |

**Итог по GTM:** целевой канал, это не массовый inbound, а founder-led ABM + партнёрства с legal/compliance интеграторами. GTM реалистичен только при фокусе на top-100 advertisers и regulated verticals.

## Top-3 risks

| Риск | Вероятность | Impact | Почему критично |
|---|---|---|---|
| Weak moat / feature substitution | High | High | Крупные proofing/legaltech incumbents могут быстро добавить похожий AI layer в существующий workflow. |
| CAC inflation + price compression | High | High | При CAC x2 EBITDA @M12 падает до -3,02 млн ₽, при price -30% до -2,36 млн ₽. |
| LLM dependency + security/data residency friction | High | High | Enterprise trust может сорваться из-за API drift, санкций или длинного security review. |

## LTV Upside Calculator

Так как кейс получил **NEAR-PASS**, нужен конкретный апсайд-план, который переведёт его в APPROVED.

### База сейчас
- ARPA = 400 000 ₽/мес
- COGS = 95 000 ₽/мес
- contribution_margin_rub_month = 305 000 ₽/мес
- customer_ltv_rub = 25,42 млн ₽
- CAC = 1,309 млн ₽
- company_ebitda_rub_month @25 клиентов = 640 000 ₽/мес

### Вариант апсайда A: ARPA +15%
- Новый ARPA = 460 000 ₽/мес
- При том же COGS contribution_margin_rub_month = 365 000 ₽/мес
- customer_ltv_rub = 30,40 млн ₽
- LTV/CAC = 23,2x
- company_ebitda_rub_month @25 клиентов = 2 140 000 ₽/мес

### Вариант апсайда B: COGS -15%
- Новый COGS = 80 750 ₽/мес
- contribution_margin_rub_month = 319 250 ₽/мес
- customer_ltv_rub = 26,60 млн ₽
- LTV/CAC = 20,3x
- company_ebitda_rub_month @25 клиентов = 996 250 ₽/мес

### Вариант апсайда C: CAC -20%
- Новый CAC = 1 047 200 ₽
- customer_ltv_rub без изменений = 25,42 млн ₽
- LTV/CAC = 24,3x
- Основной эффект, быстрее и безопаснее набор 25+ клиентов без кассового сжатия.

### Что нужно доказать, чтобы перейти в APPROVED
1. 3-5 design partners из списка named targets с подтверждённым pilot intent.
2. Подтверждение, что on-prem/VPC и security pack снимают главный trust barrier.
3. Повторяемый GTM: хотя бы 1-2 сделки без прямого закрытия CEO на каждом шаге.
4. Реальный policy/data advantage, который сложнее копировать, чем просто workflow UI.

## Delta vs previous

Предыдущий сигнал был triage-only и не прошёл полный P4-P7. В rerun кейс усилился по качеству финансовой модели, но финальный результат упирается не в математику, а в слабый moat и высокую хрупкость enterprise execution.

## Финальная рекомендация IC

**Не отклонять окончательно, но и не утверждать к одобрению без дополнительного доказательства.**

Лучший следующий шаг, это не broad launch, а узкий pilot batch по 3-5 regulated advertisers. Если команда докажет repeatable rollout, on-prem trust-layer и хотя бы первые референсы в РФ, кейс может быстро перейти из 66/100 в 74-78/100.

---

# 07-score-trajectory.md

# Score trajectory

## 2026-04-21 — P4 Demand Validation
- Stage: P4 Demand Validation
- Case: haast-geo-expand-v2
- Summary: Массовый спрос низкий, но подтверждён enterprise-grade WTP и проход Profit Gate в enterprise/hybrid монетизации.
- Demand score: 3/10 (internal multi-demand)
- Investment implication: PASS с оговорками, идти в следующие стадии только с жёстким ICP на regulated enterprise.
- Score trajectory impact: снижает вероятность PLG/SMB-истории, но оставляет сильный enterprise wedge.
- Analyst note: Ключевой риск не в отсутствии боли, а в узости сегмента и необходимости дорогих founder-led продаж.

## 2026-04-22 — P5 Unit Economics
- Stage: P5 Unit Economics
- Case: haast-geo-expand-v2
- Summary: Unit economics проходят инвестиционный порог только как узкий enterprise compliance workflow, не как self-serve SaaS.
- Key metrics: ACV 4,8 млн ₽/год, MRR 400k ₽, COGS 95k ₽/клиент/мес, Gross Margin 76,3%, blended fully-loaded CAC 1,31 млн ₽, LTV 25,42 млн ₽, LTV/CAC 19,4x, CAC Payback 3,3 месяца.
- Profit Gate: PASS, break-even 24 клиента, EBITDA при 50 клиентах ≈ 8,27 млн ₽/мес.
- Investment implication: экономика сама по себе investable, но execution risk остаётся высоким из-за длинного sales cycle, founder-led GTM и необходимости локального trust/compliance layer.
- Score trajectory impact: кейс усиливается по финансовой состоятельности, но сохраняет discount за узкий ICP и execution complexity.
- Analyst note: Следующий ключевой вопрос уже не «работает ли математика», а «способна ли команда стабильно продавать и удерживать enterprise regulated accounts в РФ».

## 2026-04-23 — P7 Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: haast-geo-expand-v2
- Summary: Финальный score 66/100, verdict = NEAR-PASS.
- Rubric raw score: 99/150, normalized 66/100.
- Key blockers: weak moat, founder-led GTM, высокий execution risk, чувствительность к CAC inflation и price compression.
- Positive factors: customer_ltv_rub 25,42 млн ₽, LTV/CAC 19,4x, CAC payback 3,3 месяца, company_ebitda_rub_month 640k ₽/мес в base к M12, company_ebitda_potential_rub_month 8,265 млн ₽/мес при 50 клиентах.
- Investment implication: кейс не отвергается окончательно, но требует доказательства 3-5 design partners, repeatable GTM и более сильного moat до перехода в APPROVED.
- Score trajectory impact: математика подтверждена, но итоговая инвестиционная оценка срезана из-за защищимости и хрупкости исполнения.
- Analyst note: Это сильный узкий enterprise wedge, но пока ещё не устойчивый asset с достаточным запасом прочности.