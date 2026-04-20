# 02-demand

## Demand validation verdict
- **Итог по спросу:** прямой спрос на `synthetic customer research` и `location intelligence retail` в РФ не подтверждён, а ближайший локальный язык спроса, это `геомаркетинг`, но и там API даёт только `LOW` при score `18/100`. [T1][T2]
- **Ключевой вывод:** в РФ есть платящий спрос на отдельные куски workflow, геоаналитику, consumer research automation и маркетинговые исследования, но не видно широкого и срочного спроса именно на AI-synthetic audience simulation как самостоятельную категорию. [T1][T2]
- **Решение этапа:** **EARLY REJECT**. Спрос низкий, а реалистичный проход Profit Gate до `EBITDA >= 500 000 ₽/мес` в локальном рынке не доказан. [T1][T2]

## Demand evidence
1. API `multi-demand` по запросу `synthetic customer research` вернул `LOW`, score `0/100`, HH.ru `0`, Google Trends RU `0`, Yandex Suggest `2`. Это почти нулевой прямой сигнал категории в РФ. [T1]  
   Source: http://172.18.0.1:9001/multi-demand?keyword=synthetic%20customer%20research
2. API по запросу `геомаркетинг` вернул `LOW`, score `18/100`, HH.ru `27`, Google Trends RU `2`, Yandex Suggest `100`. Значит adjacent pain существует, но он нишевой и сильно фрагментирован по use-cases. [T1]  
   Source: http://172.18.0.1:9001/multi-demand?keyword=%D0%B3%D0%B5%D0%BE%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3
3. API по запросу `market research automation` тоже вернул `LOW`, хотя HH.ru показывает `151` вакансии. Это говорит, что бюджет есть у broader research-automation workflows, но не у конкретного Aaru-формата позиционирования. [T1]  
   Source: http://172.18.0.1:9001/multi-demand?keyword=market%20research%20automation
4. Вывод: в РФ можно продать сервис вокруг existing research budgets, но строить кейс на сильном inbound-demand нельзя. Это demand-by-sales, а не demand-by-search. [T1/T2, inference]

## Competitor set and pricing
| Игрок | Категория | Публичная цена | Что это доказывает |
|---|---|---:|---|
| Геоинтеллект | геоаналитика для ритейла/недвижимости | от **25 000 ₽/мес** за пакет «Старт», **55 000 ₽/мес** за «Стандарт», **120 000 ₽/мес** за «Премиум» [T2] | В РФ платят за location intelligence, но это price band mid-market, а не deep enterprise research stack |
| quantilope | automated consumer intelligence | **от $22 000** за plan Business [T2] | Глобально willingness-to-pay на automation есть, но ценник enterprise и не локализован под РФ |
| aytm | DIY / full-service market research | **от $2 500/мес** за Starter, **от $5 000/мес** за Growth, **от $15 000/мес** за Premium [T2] | Автоматизированное исследование продаётся, но в мире уже crowded set с явным ценовым якорем |
| Pollfish | sample + survey research | **от $0.95** за complete interview [T2] | Нижняя граница цены, при которой часть задач commoditized и может уходить в дешёвые substitute-модели |

Sources:  
- Геоинтеллект: https://geointellect.com/  
- quantilope: https://www.quantilope.com/pricing  
- aytm: https://www.aytm.com/pricing  
- Pollfish: https://www.pollfish.com/pricing/

## Telegram bots/services in RU
- **TGStat Premium** с тарифами примерно от **1 500 ₽/мес** до **7 900 ₽/мес** показывает, что Telegram в РФ monetized как analytics/distribution channel, но это не substitute для buyer simulation или market research platform. [T2]  
  Source: https://tgstat.ru/premium
- Через `multi-demand` и web search не найден Telegram-native бот/сервис в РФ, который бы массово продавал synthetic customer research или predictive audience simulation как отдельный workflow. [T1/T2]
- Вывод по Telegram: есть канальные и аналитические сервисы вокруг Telegram, но нет заметного RU-сегмента Telegram-first решений для Aaru-категории. Это не плюс к спросу, а скорее сигнал узости рынка. [T1/T2, inference]

## WTP, willingness to pay
- Факт существования публичных цен у Геоинтеллекта, quantilope, aytm и Pollfish подтверждает, что за research/location tools платят, но price dispersion огромный, от дешёвого sample-based workflow до enterprise annual spend. [T2]
- Для РФ реалистичный локальный чек по closest substitute выглядит как **25 000-120 000 ₽/мес** за SaaS-слой либо **150 000-300 000 ₽/мес** за кастомный analyst-assisted сервис. Это inference из локального price band Геоинтеллекта и global benchmarks automated research platforms. [T2, inference]
- Это слабое доказательство willingness-to-pay именно за Aaru-like product: бюджеты на adjacent tools есть, но нет подтверждения, что buyer в РФ хочет платить premium за synthetic audiences вместо geoanalytics, survey ops или ручного исследования. [T1/T2]

## Market sizing
### Assumptions
- Курс ЦБ РФ на 20.04.2026: **82,0200 ₽/$**. [T1]  
  Source: https://www.cbr.ru/currency_base/daily/
- В РФ осталось **305** действующих кредитных организаций, это usable proxy для части enterprise buyers с регулярной потребностью в research/location analytics. [T1]  
  Source: https://www.cbr.ru/banking_sector/credit/coinfo/
- В глобальном automated research сегменте ценовой ориентир задают quantilope и aytm: от **$22 000** в год у quantilope и от **$2 500/мес** у aytm. [T2]
- В РФ публичный price anchor у локального substitute, Геоинтеллекта, это **25-120 тыс. ₽/мес**. [T2]
- Buyer universe bottom-up для первого захода беру как **200** крупных и средних сетевых ритейлеров, **100** ведущих девелоперов и **305** банков = **605** потенциальных enterprise buyers. Это proxy на локальный high-value сегмент, а не на весь рынок. [T1][T2]

### 10 реальных buyers для bottom-up и GTM
1. X5 Group [T2]
2. Магнит [T2]
3. Лента [T2]
4. О'КЕЙ [T2]
5. DNS [T2]
6. ПИК [T2]
7. Самолет [T2]
8. Эталон [T2]
9. Сбербанк [T1/T2]
10. ВТБ [T1/T2]

### Top-down
- **TAM (мир):** беру proxy через public pricing лидеров automated research. Если считать хотя бы **10 000** глобальных платящих mid-market/enterprise customers со средним чеком **$30 000/год**, получаем около **$300 млн** или **24,6 млрд ₽**. Это консервативный proxy-TAM категории automation layer, не full research spend. [T2, inference]
- **TAM (РФ):** применяю к proxy-TAM долю РФ **~2%** как грубый upper bound по доле в мировом enterprise software/research consumption, получаю **492 млн ₽**. [T1/T2, inference]
- **SAM (РФ):** беру только retail + real estate + banks и only buyers, для которых pain достаточно частый. Допускаю fit у **40%** universe и average ARR **1,2 млн ₽/год**. Получаем **290,4 млн ₽**. [T1/T2, inference]
- **SOM Y1:** реалистичный capture **3%** от SAM = **8,7 млн ₽**. [T2, inference]
- **SOM Y3:** реалистичный capture **10%** от SAM = **29,0 млн ₽**. [T2, inference]

### Bottom-up
- **Total buyers:** **605** организаций. [T1][T2]
- **% with need:** **40%** = **242** buyer'а, где pain по expansion, site selection, market sizing или customer research действительно регулярный. [T1/T2-supported inference]
- **ARR avg:** **1,2 млн ₽/год** как midpoint между локальным SaaS-substitute и high-touch сервисом. [T2, inference]
- **SAM bottom-up:** 242 × 1,2 млн ₽ = **290,4 млн ₽**. [T2]
- **SOM Y1 bottom-up:** 3% capture = **8,7 млн ₽**. [T2]
- **SOM Y3 bottom-up:** 10% capture = **29,0 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 24,6 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 492 млн ₽ [T1][T2] | 726 млн ₽ if 605 buyers × 1,2 млн ₽ as upper proxy [T1/T2] | diff ~1,5x, допустимо: bottom-up upper proxy уже близок к TAM local niche | **492 млн ₽** |
| SAM (РФ) | 290,4 млн ₽ [T1/T2] | 290,4 млн ₽ [T2] | совпадает, т.к. top-down narrowed to same ICP | **290,4 млн ₽** |
| SOM Y1 | 8,7 млн ₽ | 8,7 млн ₽ | совпадает | **используем 8,7 млн ₽** |
| SOM Y3 | 29,0 млн ₽ | 29,0 млн ₽ | совпадает | **используем 29,0 млн ₽** |

**Sanity check:** при ACV **1,2 млн ₽** SOM Y1 требует около **7-8 клиентов**. Для founder-led enterprise sales это возможно только как boutique-service wedge, но недостаточно, чтобы быстро собрать устойчивую компанию с EBITDA `>=500k/мес`. [T2, inference]

## Profit Gate: EBITDA >= 500 000 ₽/мес
Проверил все реалистичные сценарии монетизации.

1. **Low-ticket SaaS**  
   12 клиентов × 60 000 ₽/мес = **720 000 ₽/мес выручки**. При EBITDA-марже 20% это **144 000 ₽/мес EBITDA**. **FAIL.** [T2]

2. **Mid-market platform**  
   8 клиентов × 120 000 ₽/мес = **960 000 ₽/мес выручки**. При EBITDA-марже 25% это **240 000 ₽/мес EBITDA**. **FAIL.** [T2]

3. **Analyst-assisted service**  
   4 клиента × 250 000 ₽/мес = **1 000 000 ₽/мес выручки**. При EBITDA-марже 25-30% это **250 000-300 000 ₽/мес EBITDA**. **FAIL.** [T2]

4. **Enterprise custom program**  
   2 клиента × 500 000 ₽/мес = **1 000 000 ₽/мес выручки**. При EBITDA-марже 30% это **300 000 ₽/мес EBITDA**. **FAIL.** [T2]

**Итог Profit Gate:** в локальном рынке и на подтверждённом SAM кейс **не проходит**. Теоретически выйти выше `500 000 ₽/мес EBITDA` можно только при более высоком ACV или большем buyer universe, но это в текущей evidence-base не доказано и потому остаётся спекуляцией. [T1/T2]

## Risks
- Низкий прямой спрос на категорию в РФ. [T1]
- Сильная зависимость от sales-led education и кастомных внедрений. [T2]
- Локальные substitutes уже закрывают куски задачи дешевле, чем full-stack synthetic research platform. [T2]
- Telegram в РФ не показывает отдельный market wedge для такого продукта. [T1/T2]

## Final assessment
- **Demand:** LOW. [T1]
- **WTP:** частично подтверждён только для adjacent categories. [T2]
- **Profit Gate:** FAIL во всех проверенных реалистичных сценариях. [T2]
- **Решение:** **REJECTED на этапе demand validation** и перенос в `pipeline/rejected/`. [T1/T2]

Sources: T1=5, T2=10, T3=0. Primary evidence basis: T2.
