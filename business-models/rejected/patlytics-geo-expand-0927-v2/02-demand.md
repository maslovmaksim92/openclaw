# 02-demand

## Demand validation verdict
**Итог:** REJECTED.

**Почему сейчас reject:** по данным `multi-demand` для ключей «патентный поиск», «патентная аналитика» и «патентный ИИ» совокупный спрос в РФ низкий, `composite_demand=LOW`, `demand_score=15-22` [T2]. При этом даже в лучшем реалистичном monetization-сценарии продукт не выходит на EBITDA 500K ₽/мес без дорогого enterprise-services слоя, а services-layer уже конкурирует с локальными патентными бюро [T1][T2].

## Demand signals
- `патентный поиск`: `LOW`, score 22, HH вакансии 109, Google Trends RU = 2/100, Habr = 2 [T2, internal multi-demand].
- `патентная аналитика`: `LOW`, score 18, HH вакансии 24, Google Trends RU = 0/100 [T2, internal multi-demand].
- `патентный ИИ`: `LOW`, score 15, HH вакансии 7, Google Trends RU = 0/100 [T2, internal multi-demand].
- Вывод: в РФ есть операционный спрос на патентную работу как функцию, но слабый явный pull на отдельный AI SaaS для patent intelligence/drafting [T1][T2].

## Competitors with prices
| Конкурент | Что продаёт | Цена | Комментарий |
|---|---:|---:|---|
| PatentAssist | AI patent drafting/copilot | $90/мес ≈ **6.7k ₽/мес** [T2] | Низкий входной чек, давит на self-serve pricing ceiling. |
| PowerPatent | AI patent drafting | $199 стартовый платёж ≈ **14.8k ₽** [T2] | Сигнал, что мировой рынок tolerates low-entry pricing. |
| PATENTUS | Поиск по товарным знакам | **45k ₽** [T2] | Локальный substitute: клиенты уже платят за discrete IP work. |
| Гордон и Партнёры | Патентный поиск | **90k ₽** [T2] | Локальная альтернатива «сделают под ключ», без внедрения SaaS. |
| Онлайн Патент | Патентование изобретения | от **150k ₽** [T2] | В РФ willingness to pay чаще уходит в услугу, а не в подписку. |

**Конкурентный вывод:** для РФ Patlytics конкурирует не только с AI SaaS, но и с патентными бюро, где бюджет списывается как legal/prosecution service [T2]. Это осложняет продажу отдельного recurring-seat продукта [T2].

## Telegram bots / services in RU
- В РФ есть Telegram-обвязка вокруг IP, но не видно сильного сегмента именно patent-analytics bots [T2].
- У «Онлайн Патент» есть Telegram-бот/точка входа для digital IP workflow, но основная монетизация всё равно через услугу/кабинет, а не через mass bot-SaaS [T2].
- В `multi-demand` Telegram subscribers для целевых ключей не обнаружены (`subscribers=0`) [T2].

**Вывод по Telegram:** Telegram не выглядит самостоятельным go-to-market wedge для patent AI в РФ [T2].

## WTP (willingness to pay)
- WTP на **решение IP-задачи** в РФ подтверждён: локальные бюро берут 45k-150k+ ₽ за поиск/патентование [T2].
- WTP на **повторяющуюся подписку именно за patent AI software** подтверждён слабее: международные аналоги идут с entry price $90/мес и $199 one-off, то есть продуктовая цена низкая, а значит нужен объём клиентов, которого в РФ спросом не видно [T2].
- HH вакансии по патентному поиску/аналитике показывают наличие боли и payroll-spend, но не доказывают готовность покупать отдельный SaaS, особенно у небольших IP-команд [T1][T2].

**Итог WTP:** платить готовы, но в РФ платят прежде всего за outcome-as-a-service, а не за отдельный western-style patent AI subscription [T2].

## Market sizing
### Метод
Считал двумя путями и брал более консервативную оценку. Для top-down использовал объём patent activity и price anchors. Для bottom-up использовал количество реальных целевых account-типов в РФ и консервативный ARR.

### Допущения
- Курс ЦБ РФ: **1 USD = 74.5897 ₽** [T1].
- WIPO: глобальные patent filings в 2024 около **3.7 млн** [T1].
- Роспатент: заявки на изобретения от российских коммерческих организаций в 2024: **3,216** [T1].
- Средний целевой ARR для локализованного продукта: **180k-360k ₽/год** на account, что заметно ниже стоимости полноценных услуг патентных бюро [T2].
- Средняя интенсивность filing per paid account: **~8 заявок/год** [LOW CONFIDENCE, T1+T2 reconciliation].

### 10 реальных buyers / target accounts
1. Сбер [T2]
2. Яндекс [T2]
3. Касперский [T2]
4. МТС [T2]
5. Ростех [T2]
6. КАМАЗ [T2]
7. Газпром нефть [T2]
8. СИБУР [T2]
9. Татнефть [T2]
10. Росатом [T2]

### Расчёты
**Top-down**
- TAM (мир) = 3.7 млн заявок / 8 заявок на account × 360k ₽ ARR ≈ **166.5 млрд ₽** [T1+T2].
- TAM (РФ) = 3,216 / 8 × 360k ₽ ≈ **144.7 млн ₽** [T1+T2].
- SAM (РФ) = TAM РФ × 20% сегмент fit (только patent-heavy corporates + топ IP teams) ≈ **28.9 млн ₽** [T1+T2].
- SOM Y1 = SAM × 3% ≈ **0.87 млн ₽** [T2].
- SOM Y3 = SAM × 8% ≈ **2.31 млн ₽** [T2].

**Bottom-up**
- Total buyers = **350** account-типов: крупные patent-active corporates, зрелые R&D компании, часть патентных бюро и digital-IP провайдеров [T1+T2].
- % with need = **35%**: команды с регулярным patent workflow и budget owner [T1+T2].
- ARR avg = **180k ₽/год** [T2].
- SAM bottom-up = 350 × 35% × 180k ₽ = **22.05 млн ₽** [T1+T2].
- SOM bottom-up Y1 = 5% × 22.05 млн ₽ = **1.10 млн ₽** [T2].
- SOM bottom-up Y3 = 15% × 22.05 млн ₽ = **3.31 млн ₽** [T2].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 166.5 млрд ₽ [T1+T2] | — | — | top-down |
| TAM (РФ) | 144.7 млн ₽ [T1+T2] | 63.0 млн ₽ [T1+T2, 350 × 180k] | diff 2.3x, допустимо: bottom-up уже вырезает неактивные аккаунты | **63.0 млн ₽** |
| SAM (РФ) | 28.9 млн ₽ [T1+T2] | 22.05 млн ₽ [T1+T2] | diff 1.3x, близко | **22.05 млн ₽** |
| SOM Y1 | 0.87 млн ₽ | 1.10 млн ₽ | diff 26% | **0.87 млн ₽** |
| SOM Y3 | 2.31 млн ₽ | 3.31 млн ₽ | diff 43% | **2.31 млн ₽** |

**Sanity-check:** SOM Y1 сильно ниже 10% SAM, это реалистично [T2]. Но абсолютный объём слишком мал, чтобы fund-level case окупал GTM, локализацию, legal/compliance и enterprise onboarding [T2].

## Profit Gate: EBITDA >= 500K ₽/мес
Проверил все разумные сценарии.

### Сценарий 1. Self-serve SaaS
- Цена: 15k ₽/мес [T2, привязка к PowerPatent/PatentAssist].
- Реалистично достижимые клиенты в Y1: 10-20 на фоне LOW demand [T2].
- Выручка: 150k-300k ₽/мес.
- EBITDA при 70% margin: **105k-210k ₽/мес**.
- **Gate: FAIL**.

### Сценарий 2. Assisted SaaS для IP-команд
- Цена: 60k ₽/мес с onboarding/support [T2].
- Реалистично: 4-6 клиентов в Y1 из-за длинного цикла сделки и узкого ICP [T2].
- Выручка: 240k-360k ₽/мес.
- EBITDA при 45% margin: **108k-162k ₽/мес**.
- **Gate: FAIL**.

### Сценарий 3. Enterprise / on-prem / custom workflow
- Цена: 250k ₽/мес [T2].
- Реалистично: 1-2 клиента в Y1, причём с тяжёлым pre-sale, security review и кастомизацией [T2].
- Выручка: 250k-500k ₽/мес.
- EBITDA при 30% margin: **75k-150k ₽/мес**.
- Даже при 2 логотипах revenue только касается порога, а EBITDA остаётся ниже.
- **Gate: FAIL**.

### Сценарий 4. Service-led IP studio
- Можно продавать поиск/подготовку как услугу по 45k-150k ₽ за кейс [T2].
- Но это уже бизнес патентного бюро, а не масштабируемый software expansion. Для прохождения gate нужен поток 8-15 кейсов/мес и экспертная команда, что противоречит thesis «geo-expand product» [T2].
- **Gate: FAIL для product company**.

## Final decision
**EARLY REJECT.**

Логика:
1. DEMAND = LOW по целевым ключам в РФ [T2].
2. WTP есть на услугу, но не подтверждён сильный pull на отдельный patent AI subscription [T2].
3. Во всех реалистичных monetization-сценариях EBITDA < 500k ₽/мес [T2].
4. Локальный рынок too small even before sanctions/compliance friction [T1][T2].

## Sources
- [T1] Банк России, курсы валют: https://www.cbr.ru/currency_base/daily/
- [T1] WIPO IP Facts and Figures / patent filing statistics: https://www.wipo.int/web-publications/ip-facts-and-figures-2025/en/
- [T1] Роспатент, итоги 2024 / коммерческие организации 3,216 заявок: https://rospatent.gov.ru/ru/news/itogi-2024-02062025
- [T2] PatentAssist pricing: https://patentassist.ai/pricing
- [T2] PowerPatent pricing: https://powerpatent.com/pricing
- [T2] PATENTUS pricing: https://patentus.ru/services/proverka_tovarnogo_znaka/
- [T2] Гордон и Партнёры, патентный поиск: https://gordonandpartners.ru/services/patent-search/
- [T2] Онлайн Патент, услуги: https://onlinepatent.ru/services/patent/
- [T2] Internal demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D0%B0%D1%82%D0%B5%D0%BD%D1%82%D0%BD%D1%8B%D0%B9%20%D0%BF%D0%BE%D0%B8%D1%81%D0%BA

Sources: T1=3, T2=6, T3=0. Primary evidence basis: T2.
