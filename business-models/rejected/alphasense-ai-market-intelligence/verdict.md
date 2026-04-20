# AlphaSense AI Market Intelligence — Full Verdict Package
> Скомпилированный пакет стадий P0/P1/P4/P5/P6/P7 для публикации в GitHub.
> Примечание: в этом кейсе в исходном пайплайне использовались файлы `01-evidence.md` и `02-demand.md`; отдельных `02-validation.md` и `03-demand.md` не было, поэтому пакет сохраняет реальные артефакты без создания новых стадий задним числом.

---

## Файл: 00-brief.md

# 00-brief

## Кейс
alphasense-ai-market-intelligence

## Статус
active

## Тип сигнала
new

## Краткое описание
AI-платформа market intelligence для инвестбанкинга, корпоративной стратегии и competitive intelligence с enterprise-чеками, длинным циклом удержания и потенциалом локального сервиса поверх премиального контента.

## Почему взят в работу
Сигнал показывает подтверждённый enterprise-спрос: AlphaSense сообщала о более чем 500 млн USD ARR и 6 500+ корпоративных клиентах. Для локального рынка это указывает на модель с высоким чеком, высоким switching cost и потенциалом EBITDA выше 500 000 руб./мес. при относительно небольшом числе B2B-клиентов.

---

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: false
source_raw: 2026-04-19-geo-expand-alphasense-ai-market-intelligence.md
created: 2026-04-19T20:48:38+03:00
---

# Intake

## Название
AlphaSense AI Market Intelligence

## Режим обработки
Новый кейс. Duplicate-проверка не нашла уже открытого кейса с тем же фокусом на premium market intelligence, private content и AI-поиск для high-stakes research.

## Краткий контекст
Платформа решает задачу AI-поиска и аналитики по премиальным рыночным источникам, earnings calls, экспертным транскриптам и внутренним документам. На российском рынке это выглядит как потенциально дорогой B2B-сервис для инвестбанкинга, M&A, strategy, IR и competitive intelligence.

## Полный контекст из raw

name: AlphaSense
source: https://www.alpha-sense.com/press/alphasense-surpasses-500m-in-arr/ ; https://www.alpha-sense.com/press/alphasense-surpasses-usd400m-in-arr-accelerating-growth-with-private-content-expansion-and-generative-ai-innovation ; https://www.cnbc.com/2024/05/14/alphasense-cnbc-disruptor-50.html
sector: GEO-EXPAND
western_revenue: По данным компании, AlphaSense превысила $500 млн ARR к 7 октября 2025 года и обслуживает 6 500+ корпоративных клиентов. Ранее, 12 марта 2025 года, компания сообщала о $400 млн ARR и 6 000+ клиентах. Это подтверждает устойчивую enterprise-тягу и крупные чеки.
ru_equivalent: none
localization_effort: hard
ltv_signal: 1800000-9000000+ ₽ в год с одного корпоративного клиента в РФ. Логика LTV: продукт продаётся не по массовому SMB-сценарию, а как критичный research-инструмент для инвестбанкинга, M&A, корпоративной стратегии, IR и competitive intelligence. Для локального рынка это означает длинные контракты, командные лицензии, высокий switching cost и потенциал апсейла на data-packages, private content и AI-workflows.
why_it_matters: GEO-EXPAND сигнал. AlphaSense решает задачу, для которой в России пока не найден прямой локальный аналог: AI-поиск и аналитика поверх премиальных рыночных источников, брокерских отчётов, earnings calls, expert transcripts и внутренних документов компании в одном workflow. На российском рынке есть BI, мониторинг СМИ, базы контрагентов и отдельные research-инструменты, но быстрый поиск не выявил прямой отечественный продукт с сопоставимым data moat, enterprise UX и AI-слоем именно для high-stakes market intelligence. Основной барьер локализации не в интерфейсе, а в сборке локального premium-контента, лицензиях на источники и построении доверия у банков, корпстратегии и консультантов.

---

## Файл: 01-evidence.md

# Evidence

## 2026-04-19 — primary signal — https://www.alpha-sense.com/press/alphasense-surpasses-500m-in-arr/ ; https://www.alpha-sense.com/press/alphasense-surpasses-usd400m-in-arr-accelerating-growth-with-private-content-expansion-and-generative-ai-innovation ; https://www.cnbc.com/2024/05/14/alphasense-cnbc-disruptor-50.html
- **Тип:** primary signal
- **Как усиливает кейс:** официальный рост AlphaSense до более 500 млн USD ARR и 6 500+ корпоративных клиентов подтверждает, что рынок enterprise market intelligence достаточно крупный и платёжеспособный. Это делает кейс релевантным для локальной сервисной или productized-service модели с высоким средним чеком.
- **Ключевые данные и факты:** компания сообщала о 400 млн USD ARR 12 марта 2025 года, а к 7 октября 2025 года превысила 500 млн USD ARR; клиентская база выросла до 6 500+ корпоративных клиентов; use case сфокусирован на research, strategy, M&A и competitive intelligence.

---

## Файл: 02-demand.md

# 02-demand

## Demand validation verdict
- **Итог по спросу:** нишевый, но реальный enterprise-спрос в РФ; не mass-market, а high-touch сегмент для банков, corp strategy, M&A, IR и competitive intelligence. **Статус: PASS WITH CONSTRAINTS.**
- **Composite demand API:** `LOW`, score `18/100` по ключу `market intelligence`; сигналы: HH.ru `35` вакансий, Habr `2`, Yandex Suggest `100`, Google Trends RU `0`. Это указывает не на отсутствие рынка, а на слабую массовую формулировку запроса и высокую долю demand-by-sales, а не demand-by-search. [T2]
- **Ключевой вывод:** в РФ есть платёжеспособный спрос на adjacent-workflows, где уже покупают контрагентную разведку, медиа/репутационный мониторинг и корпоративный ресёрч. Прямой AlphaSense-аналог в RU не подтверждён, но подтверждён бюджет на substitute-инструменты и на ручную аналитику. [T1][T2]

## Demand evidence
1. AlphaSense сама сообщала о `>$500 млн ARR` и `6 500+` корпоративных клиентах на 7 октября 2025 года, а ранее о `$400 млн ARR` и `6 000+` клиентах на 12 марта 2025 года. Это сильный сигнал willingness-to-pay именно в enterprise market intelligence. [T1]  
   Sources: https://www.alpha-sense.com/press/alphasense-surpasses-500m-in-arr/ , https://www.alpha-sense.com/press/alphasense-surpasses-usd400m-in-arr-accelerating-growth-with-private-content-expansion-and-generative-ai-innovation/
2. В РФ виден спрос на функции competitive intelligence и strategy research через вакансии: по API для ключа `market intelligence` найдено `35` вакансий HH.ru. Это не огромный рынок, но и не ноль. [T1/T2]  
   Source: http://172.18.0.1:9001/multi-demand?keyword=market%20intelligence
3. В РФ существует платящий рынок смежных решений: компании уже покупают базы компаний, судебную/санкционную проверку, медиа-мониторинг и social listening. Значит бюджетная строка для «собрать и объяснить внешнюю информацию» реально существует. [T1][T2]

## Competitor set and pricing
| Игрок | Что закрывает | Публичная цена | Вывод |
|---|---|---:|---|
| Контур.Фокус | контрагенты, связи, проверки, мониторинг | от **31 155 ₽/год** до **115 000 ₽/год** по публичным тарифам [T1] | Бюджет на company intelligence уже есть, но продукт уже и глубже уходит в compliance, чем в strategy research |
| Casebook | судебная аналитика, проверка компаний, мониторинг | **78 000 ₽/год** за 1 пользователя, **108 000 ₽/год** за 2 пользователей [T2] | Показывает готовность платить за legal/business intelligence seat-based |
| Seldon.Basis | проверка контрагентов, риски, связи | от **54 000 ₽/год** по публичному тарифу [T2] | Нижняя граница WTP для database-like intelligence |
| Brand Analytics | медиа и соцмедиа intelligence | от **35 000 ₽/мес** до **810 000 ₽/мес**, AI-пакет от **30 000 ₽/мес** [T1] | Верхняя граница enterprise WTP за мониторинг + аналитический слой |

Sources:  
- Контур.Фокус: https://focus.kontur.ru/order?utm_source=focus&utm_medium=mainpage  
- Casebook: https://casebook.ru/price  
- Seldon.Basis: https://basis.myseldon.com/ru/tariffs  
- Brand Analytics: https://br-analytics.ru/tariffs

## Telegram bots/services in RU
- **@egrul_bot / egrul.itsoft.ru**: бот для проверки юрлиц по ЕГРЮЛ. Функция полезна для quick company lookup, но это не market intelligence platform. [T2]  
  Source: https://egrul.itsoft.ru/
- **TGStat**: Telegram analytics service с публичными тарифами от `1 500 ₽/мес` до `7 900 ₽/мес`; полезен как канал-аналитика, но не заменяет multi-source research workflow. [T2]  
  Source: https://tgstat.ru/premium
- **DataFan / similar Telegram delivery layers** встречаются как способы доставлять отчёты и алерты, но не как полноценный substitute AlphaSense-класса. [T3, спекуляция]

**Вывод по Telegram:** в RU есть боты и сервисы для узких фрагментов workflow, но не найден Telegram-native продукт, который закрывает premium research, transcript search, expert calls, earnings intelligence и внутренние документы в одном окне. Это скорее подтверждает окно для high-touch решения, чем угрозу commoditization. [T2]

## WTP, willingness to pay
- Факт покупки смежных intelligence-инструментов по ценам от `31 тыс. ₽/год` до `810 тыс. ₽/мес` подтверждает, что компании уже платят за внешнюю информацию и алерты. [T1][T2]
- Для продукта уровня AlphaSense нельзя опираться на lower-end тарифы как на целевой чек. Более реалистичный чек для локальной managed/platform модели в РФ, исходя из brief и adjacent benchmarks, это **1,8–3,6 млн ₽ ARR** на клиента при команде 3-15 пользователей и кастомных алертах/аналитике. [T2, inference from T1/T2 benchmarks]
- Дополнительное подтверждение WTP: отдельные вакансии по market/competitive intelligence означают, что компании уже несут payroll-cost на ту же задачу. При замещении 1 аналитика или ускорении due diligence продукт может окупаться даже при чеке 150-300 тыс. ₽/мес. [T1/T2]

## Market sizing
### Assumptions
- Курс для пересчёта: **76,0536 ₽/$** по курсу ЦБ РФ на 18.04.2026. [T1]  
  Source: https://www.cbr.ru/currency_base/daily/
- Глобальный рынок analytics & BI platforms: **$41,92 млрд в 2024** с ростом до **$49,51 млрд в 2025** по Gartner. Использую его как верхний proxy-TAM для software-layer, внутри которого market intelligence является узким сегментом. [T1]  
  Source: https://www.gartner.com/en/newsroom/press-releases/2025-04-03-gartner-says-worldwide-analytics-and-bi-platforms-market-achieved-41-point-9-billion-dollars-in-2024
- Доля РФ в мировой экономике: **$2,66 трлн** ВВП РФ в 2026 как прокси на верхнюю границу addressable share. [T2]  
  Source: https://www.worldometers.info/gdp/russia-gdp/
- Buyer universe bottom-up: **500** крупнейших компаний (РБК 500), **352** действующие кредитные организации (ЦБ РФ), **200** крупнейших консалтинговых групп (RAEX). [T1][T2]  
  Sources: https://companies.rbc.ru/rbc500/ , https://www.cbr.ru/banking_sector/credit/coinfo/?id=65289 , https://raex-rr.com/business/consulting/ranking_of_consulting_groups/

### 10 реальных buyers для bottom-up и GTM
1. Сбербанк [T1/T2]
2. ВТБ [T1/T2]
3. Газпром нефть [T2]
4. ЛУКОЙЛ [T2]
5. Роснефть [T2]
6. Норникель [T2]
7. Северсталь [T2]
8. АФК Система [T2]
9. X5 Group [T2]
10. Яков и Партнёры / ex-McKinsey Russia successor [T2]

### Top-down
- **TAM (мир):** $41,92 млрд = **3,19 трлн ₽**. [T1]
- **TAM (РФ):** беру **1,95%** от глобального TAM как грубый GDP-share proxy для РФ, получаю **62,1 млрд ₽**. [T1][T2]
- **SAM (РФ):** market intelligence / strategy research / competitive intelligence слой оцениваю в **3%** от верхнего TAM РФ, получаю **1,86 млрд ₽**. [T2, inference]
- **SOM Y1:** 3% от SAM = **55,8 млн ₽**. [T2, inference]
- **SOM Y3:** 10% от SAM = **186,3 млн ₽**. [T2, inference]

### Bottom-up
- **Total buyers:** 500 + 352 + 200 = **1 052** организаций. [T1][T2]
- **% with need:** беру **40%**, потому что не все компании из universe делают M&A, strategy and market scanning регулярно; это даёт **421** активный buyer. [T1/T2-supported inference]
- **ARR avg:** **2,4 млн ₽/год** на клиента, консервативно внутри диапазона brief `1,8–9,0 млн ₽`. [T2]
- **SAM bottom-up:** 421 × 2,4 млн ₽ = **1,01 млрд ₽**. [T2]
- **SOM Y1 bottom-up:** 4% capture = **40,4 млн ₽**. [T2]
- **SOM Y3 bottom-up:** 12% capture = **121,1 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | $41,92B / 3,19 трлн ₽ [T1] | — | — | top-down |
| TAM (РФ) | 62,1 млрд ₽ [T1][T2] | ~2,52 млрд ₽ if 1 052 buyers × 2,4 млн ₽ [T2, upper proxy] | diff ~24,6x, потому что buyer-based proxy уже ближе к SAM, а не к full TAM | lower logic for execution |
| SAM (РФ) | 1,86 млрд ₽ [T2] | 1,01 млрд ₽ [T2] | diff ~1,84x, допустимо для ранней оценки | **1,01 млрд ₽** |
| SOM Y1 | 55,8 млн ₽ | 40,4 млн ₽ | diff ~1,38x | **40,4 млн ₽** |
| SOM Y3 | 186,3 млн ₽ | 121,1 млн ₽ | diff ~1,54x | **121,1 млн ₽** |

**Sanity check:** при ACV `2,4 млн ₽` SOM Y1 `40,4 млн ₽` требует ~`17` клиентов. Для enterprise sales-cycle `6-9` месяцев это тяжело для маленькой команды, но возможно только в managed-intelligence формате с founder-led sales и узким ICP. [T2, inference]

## Profit Gate: EBITDA >= 500 000 ₽/мес
Проверил все базовые сценарии монетизации.

1. **Low-ticket SaaS seats**  
   25 пользователей × 35 000 ₽/мес = **875 000 ₽/мес выручки**. При EBITDA-марже 35% получаем **306 000 ₽/мес EBITDA**. **FAIL.** [T2, based on adjacent pricing]

2. **Hybrid team license**  
   8 клиентов × 180 000 ₽/мес = **1 440 000 ₽/мес выручки**. При EBITDA-марже 40% получаем **576 000 ₽/мес EBITDA**. **PASS.** [T2]

3. **Managed intelligence / analyst-assisted**  
   6 клиентов × 250 000 ₽/мес = **1 500 000 ₽/мес выручки**. При EBITDA-марже 45% получаем **675 000 ₽/мес EBITDA**. **PASS.** [T2]

4. **One-off due diligence studio**  
   4 проекта × 400 000 ₽/мес = **1 600 000 ₽/мес выручки**. При EBITDA-марже 30% получаем **480 000 ₽/мес EBITDA**. **FAIL.** [T2]

**Итог Profit Gate:** достижим, но только в high-touch enterprise-модели. Чистый lower-end SaaS и pure project work не проходят порог. [T2]

## Risks
- Слабый search-demand и низкая частотность прямого термина `market intelligence` в РФ. [T2]
- Главный moat AlphaSense, это не AI-интерфейс, а лицензированный premium-content graph; локально его собрать трудно. [T1][T2]
- Высокий sales effort и необходимость доверия со стороны банков, M&A и corp strategy команд. [T2]

## Final assessment
- **Demand:** LOW на массовом уровне, **MEDIUM в узком enterprise ICP**. [T2]
- **WTP:** подтверждён. [T1][T2]
- **Profit Gate:** проходит в 2 из 4 реалистичных сценариев. [T2]
- **Решение:** **не отклонять на этапе demand**. Идти дальше имеет смысл только с позиционированием как `managed AI market intelligence for high-stakes corporate workflows`, без SMB и без попытки конкурировать за broad BI. [T2]

Sources: T1=5, T2=9, T3=1. Primary evidence basis: T2.
- Market Pulse 20.04.2026: растущий интерес.

---

## Файл: 04-economics.md

(см. исходный файл в pipeline/cases/alphasense-ai-market-intelligence/04-economics.md; для краткости пакет опирается на финальные метрики и выводы из него, полностью сохранённые в 06-verdict.md)

---

## Файл: 05-critic.md

(см. исходный файл в pipeline/cases/alphasense-ai-market-intelligence/05-critic.md; ключевые P6A/P6B выводы отражены в 06-verdict.md)

---

## Файл: 06-verdict.md

[GEO-EXPAND] AlphaSense AI Market Intelligence — NEAR-PASS: 66/100 | EBITDA base=2000К₽/мес через 19-20 мес | LTV/CAC=29,8x | Ключевое преимущество: высокий enterprise ACV и глубокий analyst workflow | Главный риск: слабый локальный data moat и тяжёлый GTM.

# 06-verdict — AlphaSense AI Market Intelligence

sector: GEO-EXPAND
status: NEAR-PASS
score: 66/100
normalized_from_raw: 99/150
case_slug: alphasense-ai-market-intelligence
updated_at: 2026-04-20 06:52 MSK

## Инвесткомитет: итоговый вердикт

Кейс не дотягивает до investment-grade approve, но и не выглядит безнадёжным. Экономика на бумаге сильная, `company_ebitda_potential_rub_month` проходит порог уже при 50 клиентах, однако локальный moat пока слишком слабый: в РФ подтверждён бюджет на adjacent-инструменты, но не доказан repeatable спрос именно на premium market-intelligence stack с дорогим proprietary content layer. Поэтому итог, это **NEAR-PASS** с требованием сначала доказать GTM и data advantage.

## Оценка

Source tier balance: T1=5, T2=9, T3=1, weighted=2.27. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | В 04-economics.md: «LTV/CAC = 29,8x», «CAC Payback = 2,9 месяца», «Contribution Margin = 75,8%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В 04-economics.md: «EBITDA ≈ 2,0 млн ₽/мес» при 50 клиентах, fully-loaded break-even ближе к «M19-M20». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md: «Composite demand API: LOW, score 18/100», при этом «в РФ есть платёжеспособный спрос на adjacent-workflows»; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | В 02-demand.md: «Главный moat AlphaSense, это не AI-интерфейс, а лицензированный premium-content graph; локально его собрать трудно». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В 05-critic.md: «хвост риска жирный», а ключевые риски, это data moat, sales-cycle, vendor dependency и санкционные ограничения. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | В 04-economics.md уже есть blended CAC 722 150 ₽ и enterprise funnel, но победа требует выигрывать у «Контур/Seldon + ручная аналитика + Brand Analytics». |

**Sum raw = 99/150**  
**Normalized score = round(99 × 100 / 150) = 66/100**

### Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый клиент почти не улучшает продукт для остальных; сетевой эффект не доказан. |
| Switching costs | 2 | Есть потенциал переключательных издержек через алерты, привычный research workflow и исторические досье. |
| Scale economies | 2 | LLM/data/cloud unit cost частично падает с объёмом, но premium content остаётся дорогим. |
| Proprietary data / model advantage | 1 | Локальный эксклюзивный датасет не доказан, пока это скорее агрегатор + workflow. |
| Regulatory moat | 1 | Private cloud и data residency важны, но формального регуляторного барьера нет. |
| Brand / distribution | 1 | В РФ бренда и устоявшегося канала продаж пока нет. |
| Embedded workflow | 3 | При удачном внедрении продукт глубоко встраивается в M&A, IR, strategy и competitive intelligence процессы. |

**Moat raw = 10/21, moat score = round(10 × 25 / 21) = 12/25**

## Investment one-liner

`[GEO-EXPAND] AlphaSense AI Market Intelligence — NEAR-PASS: 66/100 | EBITDA base=2000К₽/мес через 19-20 мес | LTV/CAC=29,8x | Ключевое преимущество: высокий enterprise ACV и глубокий analyst workflow | Главный риск: слабый локальный data moat и тяжёлый GTM.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 21 540 000 ₽ |
| CAC blended | 722 150 ₽ |
| LTV/CAC | 29,8x |
| CAC Payback | 2,9 мес по MRR |
| Gross Margin | 71,8% |
| contribution_margin_rub_month | 189 500 ₽/клиент/мес |
| fixed_costs_rub_month | 7 474 800 ₽/мес |
| company_ebitda_rub_month, M12 base | -3 446 032 ₽/мес |
| company_ebitda_potential_rub_month | 2 000 200 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 42 |
| months_to_500k_ebitda | 19-20 |
| clients_to_1m_ebitda | 45 |
| months_to_1m_ebitda | 20-21 |
| Break-even | 42 клиента по gross profit / 40 по contribution |
| startup_capital_to_bep_rub | 80 727 656 ₽ |

## Полный business process

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов | CEO + SDR | HH/СПАРК/Контур.Фокус, Excel/CRM | 2 дня | 18 000 | Средний |
| 2 | Enrichment контактов и приоритизация | SDR | Bitrix24, ручной ресёрч, почта | 1 день | 12 000 | Средний |
| 3 | Outreach 6-8 касаний | SDR | e-mail, телефон, Telegram, Bitrix24 | 10 дней | 55 000 | Средний |
| 4 | Первичный qual-call | SDR + CEO | Meet, Bitrix24 | 45 мин | 8 000 | Низкий |
| 5 | Discovery с buyer group | CEO + AE | Meet, презентация, ROI-калькулятор | 5 дней | 32 000 | Низкий |
| 6 | Demo на реальных кейсах | AE + CTO | Demo workspace, RAG prototype | 3 дня | 45 000 | Низкий |
| 7 | Pilot scoping и success criteria | AE + CTO + Analyst | Notion, KPI sheet | 4 дня | 38 000 | Низкий |
| 8 | Пилот 2-4 недели | Analyst + CTO + CS | LLM stack, data pipeline, Slack/Telegram | 21 день | 145 000 | Средний |
| 9 | Security / legal review | CTO + CEO | NDA/DPA, security questionnaire, Диадок | 7 дней | 42 000 | Низкий |
| 10 | Procurement и согласование договора | AE + CEO | Диадок, e-mail, CRM | 10 дней | 36 000 | Низкий |
| 11 | Счёт и закрывающие документы | Finance ops | 1С/Моё дело, Диадок | 2 дня | 9 000 | Высокий |
| 12 | Оплата и активация | Finance ops + CS | Банк-клиент, CRM, onboarding checklist | 2 дня | 7 000 | Высокий |

## Финансовая траектория

| Scenario | M12 clients | EBITDA @M12 | Break-even month | Startup capital to BEP |
|---|---:|---:|---:|---:|
| Base | 22,4 | -3 446 032 ₽/мес | 18 | 80 727 656 ₽ |
| Optimistic | 27,5 | -2 529 595 ₽/мес | 15 | 71 038 618 ₽ |
| Pessimistic | 14,4 | -4 884 687 ₽/мес | 23 | 102 848 207 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-5 143 235 ₽/мес**
- p50 EBITDA @M24 = **5 065 649 ₽/мес**
- p90 EBITDA @M24 = **29 697 740 ₽/мес**
- Вывод: median-case живой, но downside уже уходит в отрицательный EBITDA и короткий runway.

## Команда

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | founder-led sales, enterprise relationships, pricing, fundraising | 780 000 |
| CTO / Tech Lead | architecture, security review, product delivery | 715 000 |
| Senior Backend x2 | ingestion, search, permissions, integrations | 1 170 000 |
| ML Engineer | ranking, summarization, retrieval quality, evals | 650 000 |
| DevOps | infra, observability, deployment, access control | 455 000 |
| Frontend | analyst UX, search workspace, dashboards | 390 000 |
| SDR | cold outreach, lead qualification, meeting setting | 214 500 |
| AE | discovery, pilot, procurement, close | 455 000 |
| Customer Success | onboarding, adoption, renewals, expansion | 325 000 |
| Growth marketer | content, webinars, analyst reports, nurture | 286 000 |
| **Итого** |  | **5 440 500** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбербанк | крупнейший buyer для investment research, corp strategy и market mapping, где скорость due diligence уже оплачивается ФОТ аналитиков | email decision-maker в strategy / CIB + отраслевые конференции | 400 000 ₽/мес |
| ВТБ | большой объём M&A, отраслевого ресёрча и IR-задач, где критичны transcript search и быстрые конкурентные досье | direct outreach + партнёрский warm intro | 400 000 ₽/мес |
| Альфа-Банк | digital-first банк с активной продуктовой и strategy-функцией, где нужен быстрый внешний intelligence | founder-led outbound + контент на vc.ru | 350 000 ₽/мес |
| Яков и Партнёры | стратегия и корпоративный ресёрч продаются клиентам как high-stakes service, значит ускорение research workflow ценно | партнёрство / email practice lead | 300 000 ₽/мес |
| АФК Система | корпоративный центр с инвестиционными и M&A задачами по портфельным компаниям | direct outreach в corp dev / strategy | 300 000 ₽/мес |
| X5 Group | конкурентная разведка, supplier intelligence и strategic planning уже встроены в большой retail workflow | конференция + direct outreach | 250 000 ₽/мес |
| Норникель | крупная публичная компания с IR, market scan и commodity competitor tracking | email IR/strategy decision-maker | 250 000 ₽/мес |
| Северсталь | регулярный стратегический ресёрч и benchmarking по отрасли и CAPEX-проектам | отраслевой ивент + партнёрство с консультантами | 250 000 ₽/мес |
| Газпром нефть | corporate strategy и business development требуют дорогого market intelligence и vendor scan | partner-led intro + direct sales | 300 000 ₽/мес |
| МТС | много направлений бизнеса, где central strategy и corp dev могут покупать общий research workflow | vc.ru ad + email strategy / BI leadership | 250 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Weak moat / отсутствие локального premium-content graph | high | high | Если не собрать собственный data layer, продукт останется дорогим агрегатором без устойчивого преимущества. |
| CAC inflation и длинный enterprise sales cycle | high | high | В 05-critic.md CAC x2 ухудшает EBITDA @M12 до **-4 890 332 ₽/мес**. |
| Vendor dependency и санкционные ограничения на LLM / данные | high | high | Кейс завязан на внешние модели, облака и licensing, что увеличивает риск cost spike и блокировок. |

## LTV Upside Calculator

### Что должно измениться, чтобы кейс перешёл в APPROVED

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 250 000 ₽/мес | 300 000-350 000 ₽/мес | Повышает gross profit и снижает чувствительность к long sales cycle. |
| Blended CAC | 722 150 ₽ | <650 000 ₽ | Делает growth engine менее капиталоёмким и сокращает startup capital to BEP. |
| Churn | 10% годовых | ≤8% годовых | Укрепляет `customer_ltv_rub` и повышает надёжность long-term economics. |
| Data moat | слабый | 2-3 локальных эксклюзивных data-packages | Позволяет защищать цену и win-rate против substitute stack. |
| GTM | founder-led | 3 design partners + 2 канала партнёров | Делает pipeline менее хрупким и подтверждает repeatability. |

### Минимальные proof points для rerun
1. Не менее **3 платящих design partners** с контрактом **300К+ ₽/мес**.
2. Подтверждённый **pilot-to-paid ≥ 30%** на первых 10 пилотах.
3. Хотя бы **1 локальный proprietary data package** или эксклюзивная лицензия, которую нельзя быстро скопировать.
4. Сокращение sales cycle до **≤120-150 дней** без критичного discounting.
5. Не менее **2 reference accounts** в банках, corp strategy или M&A advisory.

## Финальное решение инвесткомитета

**NEAR-PASS.**

Я бы не инвестировал в текущем виде как в готовый approve-кейс, потому что слабость moat и российской demand-evidence делает модель слишком зависимой от ручных продаж и внешних data/LLM-поставщиков. Но кейс достоин rerun после доказательства локального proprietary wedge, потому что unit economics и EBITDA-потенциал здесь объективно сильнее среднего.

---

## Файл: 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-20 01:51 MSK — Demand Validation
- Stage: Program 4 / Demand Validation
- Case: `alphasense-ai-market-intelligence`
- Oldest eligible case processed first by `00-brief.md` mtime.
- Demand API: `LOW` (`18/100`) for keyword `market intelligence`.
- Research conclusion: массовый спрос слабый, но enterprise ICP подтверждён через global benchmark AlphaSense, HH-сигналы и публичные цены российских substitute-инструментов.
- Competitor pricing found: Контур.Фокус, Casebook, Seldon.Basis, Brand Analytics.
- TAM/SAM/SOM: preferred SAM `1,01 млрд ₽`, SOM Y1 `40,4 млн ₽`, SOM Y3 `121,1 млн ₽`.
- Profit Gate: PASS only in hybrid enterprise and managed-intelligence scenarios; FAIL in low-ticket SaaS and one-off project model.
- Score impact:
  - Demand realism: `+2`
  - WTP evidence: `+2`
  - Localization difficulty / content moat: `-2`
  - Go-to-market complexity: `-1`
  - Net delta: `+1`
- Outcome: `PROCEED`, без early reject; кейс оставлен в `pipeline/cases/`.
- Artifacts: `02-demand.md`

## 2026-04-20 02:00 MSK — Unit Economics
- Stage: Program 5 / Unit Economics
- Case: `alphasense-ai-market-intelligence`
- Pricing model set to **250 000 ₽ MRR / 3,0 млн ₽ ACV** на клиента, что соответствует enterprise ICP из `02-demand.md`.
- COGS рассчитан как analyst-assisted enterprise product: **60,5-70,5 тыс. ₽/клиент/мес**, Contribution Margin **75,8%**.
- Fully-loaded blended CAC рассчитан по enterprise формуле: **722 тыс. ₽**; каналами показаны outbound ABM, partnerships/events и inbound.
- LTV рассчитан при annual logo churn **10%**: **21,54 млн ₽**.
- Core efficiency metrics:
  - LTV/CAC: `29,8x`
  - CAC Payback: `2,9 мес`
  - Operating break-even: `32 клиента`
  - Fully-loaded break-even: `40 клиентов`
  - EBITDA at 50 clients: `~2,0 млн ₽/мес`
- Burn-to-breakeven оценён в **~61,7 млн ₽**; минимально реалистичный startup capital для прохождения до BEP в модели: **~70 млн ₽**.
- Economics conclusion: модель **проходит investment-grade sanity checks**, но чувствительна к data licensing, длинному sales cycle и точности enterprise-hiring плана.
- Score impact:
  - Unit economics strength: `+3`
  - Realistic CAC methodology: `+2`
  - Capital intensity / long path to BEP: `-2`
  - Execution risk in enterprise sales: `-1`
  - Net delta: `+2`
- Outcome: `PROCEED` to next stage; reject criteria not triggered.
- Artifacts: `04-economics.md`

## 2026-04-20 06:52 MSK — Program 7 Critic and Verdict
- Stage: P7
- Verdict: NEAR-PASS
- Score: 66/100
- Raw score: 99/150
- Summary: кейс подтверждает сильную unit economics и EBITDA-потенциал, но не проходит investment committee без локального moat и repeatable GTM для premium market-intelligence в РФ.
- Rubric:
  - unit_economics: 21/25
  - ebitda_potential: 20/25
  - market_demand: 14/25
  - moat: 12/25
  - execution_risk: 15/25
  - gtm_realism: 17/25
- Source tier balance:
  - T1: 5
  - T2: 9
  - T3: 1
  - weighted: 2.27
  - penalty_to_market_demand: -2
- Key gates:
  - company_ebitda_potential_rub_month: PASS (2 000 200 ₽/мес at 50 clients)
  - clients_to_500k_ebitda: PASS (42)
  - months_to_500k_ebitda: PASS (19-20)
  - moat_strength: WEAK (12/25)
  - evidence_quality: CONDITIONAL_PASS
- Outcome: `MOVE_TO_REJECTED`, потому что normalized score < 70.
- Artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/rejected/alphasense-ai-market-intelligence/06-verdict.md