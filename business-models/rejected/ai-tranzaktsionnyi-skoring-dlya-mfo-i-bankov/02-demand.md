---
stage: demand-validation
case: ai-tranzaktsionnyi-skoring-dlya-mfo-i-bankov
date: 2026-05-09
analyst: branch-models-lead
sector: FINTECH
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
AI-транзакционный скоринг для МФО и банков.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Exact-demand по формулировкам `транзакционный скоринг`, `кредитный скоринг`, `скоринг мфо` в РФ низкий по category label, но это не означает отсутствия бюджета: сам job-to-be-done встроен в core lending workflow банков и МФО. `multi-demand` даёт LOW, но Банк России фиксирует рост использования кредитных оценок БКИ со стороны МФО в **1,6 раза** за 2025 год. [T1]
- WTP подтверждён: на рынке есть реальные скоринговые и кредитно-аналитические сервисы с публичным pricing, от **140 ₽ за отчёт** у локального TG/web-инструмента до **99 €/мес** и **499 €/мес** у B2B scoring SaaS, а также **$4 485-7 485/год** у behavioural scoring provider. [T2]
- В РФ Telegram уже используется в adjacent-слое кредитной аналитики, но сейчас это в основном broker/consumer tooling, а не полнофункциональный B2B decision engine для банка или МФО. Значит TG важен как интерфейс оповещений и lightweight workflow, но не как основной moat. [T2][T3][inference]
- Profit Gate не проходит в low-ticket per-report motion, но проходит в SaaS/API и enterprise white-label сценариях. Поэтому mandatory early reject **не срабатывает**. [T1][T2][inference]

## 1. Demand data

### Demand API
- `кредитный скоринг` → **LOW**, `demand_score=22`, `hh_vacancies=83`, `yandex_suggest=100`. [T1]
- `транзакционный скоринг` → **LOW**, `demand_score=15`, `hh_vacancies=3`, `yandex_suggest=100`, `google_trends_ru=1`. [T1]
- `скоринг мфо` → **LOW**, `demand_score=18`, `hh_vacancies=27`, `yandex_suggest=100`. [T1]
- `андеррайтинг займов` → **LOW**, `demand_score=7`, `hh_vacancies=64`, `yandex_suggest=2`. [T1]
- `антифрод мфо` → **LOW**, `demand_score=18`, `hh_vacancies=13`, `yandex_suggest=100`. [T1]

### Интерпретация
- В РФ category-level search спрос слабый, но это типично для инфраструктурного fintech software: покупают не по ярлыку `AI-транзакционный скоринг`, а по KPI `одобрение`, `loss rate`, `speed to decision`, `антифрод`, `PDN-compliance`. [T1][inference]
- Банк России в 2026 году сообщил, что количество кредитных оценок, предоставленных МФО со стороны БКИ, **выросло в 1,6 раза** за 2025 год. Это сильнее, чем search intent, доказывает реальный production-demand на scoring inputs. [T1]
- Банк России также оценивает, что каждый рубль затрат на кредитный отчёт во втором полугодии 2025 года потенциально снижает просрочку более чем на **337 ₽**, то есть value proposition у risk-data уже monetized и понятен рынку. [T1]
- Вывод: demand слаб по терминологии, но силён по операционному применению. Для фонда это **не reject**, а `PASS WITH RESERVATIONS`. [T1][inference]

## 2. Реальные конкуренты и цены

| Игрок | Формат | Публичная цена | Что доказывает |
|---|---|---:|---|
| **RocketFin** | B2B credit scoring SaaS | **99 €/мес** Starter, **499 €/мес** Pro, API **+99 €/мес**, credit packs **50-250 €**. [T2] | Рынок принимает recurring pricing за automated credit scoring и API-access |
| **Credolab** | Behavioural / alternative-data scoring для lenders | **$4 485/год** за Credolight и **$7 485/год** за Credoone при объёме до 100k uploads/year. [T2] | Альтернативный и behavioural scoring уже продаётся как отдельный risk layer |
| **Scanify** | RU credit-history analysis для брокеров и юристов, web + Telegram | **140 ₽ за 1 отчёт**, **4 000 ₽ за 100 отчётов**. [T2] | В РФ уже платят за автоматизированный кредитный анализ даже в low-end workflow |
| **SCORISTA** | Прямой конкурент по андеррайтингу и risk automation для МФО | pricing public не раскрыт, продаётся как B2B risk platform. [T2] | На локальном рынке есть специализированный игрок именно под МФО и online underwriting |

### Вывод по конкуренции
- Прямой локальный benchmark есть, но с непрозрачным pricing, что типично для enterprise fintech. [T2]
- Публичные цены зарубежных и adjacent-локальных решений показывают, что buyer уже готов платить либо по подписке, либо per-analysis. [T2]
- Это подтверждает WTP, но также означает, что новый игрок должен объяснять, почему он лучше существующего стека `БКИ + rules + antifraud + manual underwriting`. [T1][T2][inference]

## 3. Telegram-боты и сервисы в РФ

Проверка RU-ландшафта показывает, что Telegram присутствует, но в основном как adjacent delivery layer:

1. **Scanify** работает и как web, и как **Telegram-бот** для анализа кредитной истории и подготовки пакета на банкротство. [T2]
2. В выдаче есть consumer/broker-oriented боты вроде **Smart Credit** и каталожные упоминания TG-ботов для кредитной проверки, но evidence по институциональному внедрению у них слабое. [T3]
3. Сильных публичных Telegram-native B2B decisioning платформ для банков и МФО в РФ не найдено. Это скорее говорит о пустом интерфейсном слое, чем о пустом core-risk layer. [T2][T3][inference]

**Вывод:** Telegram в РФ реален как интерфейс для загрузки отчётов, оповещений и простых risk workflows, но не как полноценная замена underwriting engine. Для этого кейса TG надо рассматривать как optional channel, а не ядро продукта. [T2][inference]

## 4. WTP, proof of willingness to pay

### Прямые сигналы
- **RocketFin** публично продаёт automated B2B credit scoring по модели от **99 €/мес** до **499 €/мес** плюс API. [T2]
- **Credolab** продаёт behavioural scoring для lenders в годовом чеке **$4,5-7,5k** до кастомного scorecard layer. [T2]
- **Scanify** монетизирует автоматизированный анализ кредитной истории поштучно и пакетами, что показывает willingness to pay даже на низком чеке в RU adjacent-сегменте. [T2]
- Банк России даёт экономический proof: 1 рубль расходов на кредитный отчёт потенциально снижает просрочку более чем на **337 ₽**. Это очень сильный value anchor для risk-tech закупки. [T1]

### Вывод по WTP
**WTP подтверждён.** Российский buyer не обязательно ищет `AI-транзакционный скоринг` как лейбл, но уже платит за risk scoring, credit data, credit reports и автоматизацию андеррайтинга. Реалистичный локальный pricing для нового игрока выглядит так: **80-150 тыс. ₽/мес** для SaaS/API слоя в mid-market, **250-500 тыс. ₽/мес** для enterprise white-label с интеграцией данных, rules engine и SLA, либо **20-80 ₽ за анализ** в usage-based motion. Это inference, опирающийся на публичный pricing конкурентов и economics существующих кредитных отчётов. [T1][T2][inference]

## 5. Market sizing

### Подход
Считаю не весь banking software рынок, а более узкий wedge: scoring / underwriting decision layer для банков и МФО, прежде всего в digital consumer lending и смежном SME-lending. [T1][T2][inference]

Для top-down беру глобальный сегмент **loan origination** и режу его до scoring/underwriting layer. Для РФ использую консервативную долю и дополнительно режу сегмент до реально addressable банков и МФО. [T2][inference]

Для bottom-up беру реальный buyer pool: **305 действующих банков** в РФ и **264 МФО ЦФО** как консервативно подтверждённую официальную подвыборку цифрово активных МФО. Это даёт минимальный подтверждённый пул **569 организаций** без overclaiming на весь реестр страны. [T1][inference]

### Top-down
- Grand View Research оценивает глобальный сегмент **loan origination** digital lending platform в **$1 787,9 млн** за 2024 год. [T2]
- Для scoring/underwriting decision layer беру **12%** от этого сегмента, потому что кейс не покрывает весь LOS, а только risk decisioning, data ingestion и automated underwriting. Получаем **TAM (мир) ≈ $214,5 млн**. [T2][inference]
- Для РФ беру **1,5%** от глобального wedge, затем округляю консервативно. Получаем **TAM РФ ≈ $3,2 млн**. [T2][inference]
- При sanity-rate **80 ₽/$** получаем **TAM РФ ≈ 258 млн ₽**. [T2][inference]
- В целевой сегмент банков и цифрово активных МФО отношу **70%** TAM, потому что не все лицензированные участники покупают внешний scoring layer отдельно. Получаем **SAM ≈ 181 млн ₽**. [T1][T2][inference]
- Реалистичный захват: **Y1 = 4% SAM = 7,2 млн ₽**, **Y3 = 12% SAM = 21,7 млн ₽**. [inference]

### Bottom-up
- Подтверждённый buyer base: **305 банков** по состоянию на 1 апреля 2026 года плюс **264 МФО**, зарегистрированные в ЦФО. Итого **569 buyers**. [T1]
- Доля buyers с реальной потребностью, **22%**: это digital lenders и risk-heavy организации, где pain подтверждается ростом скорингов БКИ, online channels и lending volume. [T1][inference]
- Средний контракт, **1,5 млн ₽/год**: это эквивалент **125 тыс. ₽/мес** за scoring/API слой с интеграцией и support, без deep enterprise customization. [T2][inference]
- Тогда **SAM_bottom_up = 569 × 22% × 1,5 млн ₽ = 187,8 млн ₽/год**. [T1][T2][inference]
- Для внутреннего TAM РФ в bottom-up беру 40% buyer base с потенциальным интересом и тот же ARR: **569 × 40% × 1,5 млн ₽ = 341,4 млн ₽**. [T1][T2][inference]
- **SOM_bottom_up Y1** при захвате **4%** SAM = **7,5 млн ₽/год**. [inference]
- **SOM_bottom_up Y3** при захвате **12%** SAM = **22,5 млн ₽/год**. [inference]

### GTM-10 / 10 реальных buyers для bottom-up
1. **Т-Банк** — digital-heavy кредитный поток, высокий смысл в automated decisioning. [T2][inference]
2. **Альфа-Банк** — большой объём consumer lending и mature data stack. [T2][inference]
3. **Совкомбанк** — активный retail lender, большой underwriting volume. [T2][inference]
4. **МТС Банк** — цифровой retail и BNPL-like сценарии. [T2][inference]
5. **Ozon Банк** — embedded finance и транзакционные данные платформы. [T2][inference]
6. **Займер** — online-first МФО, natural buyer для scoring automation. [T2][inference]
7. **MoneyMan** — одна из самых заметных digital МФО. [T2][inference]
8. **Webbankir** — онлайн-выдача и repeat underwriting workload. [T2][inference]
9. **еКапуста** — скоринговый и antifraud-intensive поток. [T2][inference]
10. **Быстроденьги** — крупный бренд с потребностью в скорости решения и loss control. [T2][inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $214,5M [T2] | — | — | top-down |
| TAM (РФ) | 258 млн ₽ [T2] | 341,4 млн ₽ [T1/T2] | diff≈1,32x, bottom-up шире за счёт предположения о 40% потенциально addressable buyers | lower |
| SAM (РФ) | 181 млн ₽ [T1/T2] | 187,8 млн ₽ [T1/T2] | diff≈1,04x, модели практически сходятся | lower |
| SOM Y1 | 7,2 млн ₽ | 7,5 млн ₽ | diff≈1,04x | **используем 7,2 млн ₽** |
| SOM Y3 | 21,7 млн ₽ | 22,5 млн ₽ | diff≈1,04x | **используем 21,7 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up меньше 3x, пересмотр сегмента не требуется. [T1][T2]
- SOM Y1 это около **4%** от SAM, что выглядит реалистично. [inference]
- При среднем контракте **1,5 млн ₽/год** SOM Y1 соответствует примерно **5 клиентам** в год, что операционно достижимо для небольшой B2B fintech-команды. [inference]
- Это лучше, чем массовый per-report бизнес, где нужна большая дистрибуция и низкий CAC. [inference]

## 6. Profit Gate: проверка всех сценариев монетизации

Для расчёта беру фиксированные расходы **1,3 млн ₽/мес**: founder/CEO, ML-risk engineer, integrations/backend engineer, customer success / implementation, инфраструктура и общие расходы. [inference]

### Сценарий A. Low-ticket per-report / broker tool
- Цена: **50 ₽ за анализ** blended.
- Валовая маржа: **65%**.
- Contribution: **32,5 ₽** на анализ.
- Для EBITDA **500 000 ₽/мес** нужно около **55 400 анализов в месяц**, что для ранней B2B-компании нереалистично.
- **Вердикт: FAIL.** [inference]

### Сценарий B. Mid-market SaaS/API
- Setup fee: **200 000 ₽**.
- MRR: **125 000 ₽/мес**.
- Валовая маржа: **78%**.
- Contribution на клиента: **97 500 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужно около **19 клиентов**.
- **Вердикт: PASS WITH EXECUTION RISK.** [inference]

### Сценарий C. Enterprise white-label scoring
- Setup fee: **500 000 ₽**.
- MRR: **350 000 ₽/мес**.
- Валовая маржа: **82%**.
- Contribution на клиента: **287 000 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужно около **7 клиентов**.
- **Вердикт: PASS.** [inference]

### Сценарий D. Hybrid scoring + anti-fraud managed layer
- Setup fee: **300 000 ₽**.
- MRR: **220 000 ₽/мес**.
- Валовая маржа: **75%**.
- Contribution на клиента: **165 000 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужно около **11 клиентов**.
- **Вердикт: PASS.** [inference]

### Общий вывод по Profit Gate
- Profit Gate проваливается только в commodity per-report motion. [inference]
- В SaaS/API, enterprise white-label и hybrid managed сценариях порог **500 000 ₽ EBITDA/мес** достижим. [inference]
- Следовательно, even при low exact-demand кейс не подлежит early reject. [T1][T2][inference]

## 7. Основные риски
- Покупатель может предпочесть собрать стек из БКИ, antifraud, rules engine и внутренних DS-ресурсов вместо покупки отдельного vendor layer. [T1][T2][inference]
- Регуляторика tightening усиливает ценность скоринга, но одновременно повышает требования к explainability, data provenance и quality controls. [T1][inference]
- Exact-demand в поиске слабый, поэтому GTM придётся строить через прямые продажи, партнёрства и ROI-calculator, а не через inbound category creation. [T1][inference]
- Telegram-сервисы в РФ задают low-end expectation по удобству, но тянут цену вниз в брокерском сегменте. [T2][T3][inference]

## 8. Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. Есть реальный production-demand на кредитные оценки и скоринги, подтверждённый Банком России. [T1]
2. Есть proof of willingness to pay по нескольким публичным pricing-моделям. [T2]
3. Profit Gate проходит в нескольких реалистичных B2B monetization scenarios. [inference]

Что критично проверить дальше:
- можно ли доказать uplift по approve-rate и default-rate против existing stack;
- можно ли стать system-of-record layer, а не просто дополнительным API;
- можно ли удерживать чек **125-350 тыс. ₽/мес** без долгого кастомного внедрения;
- можно ли взять первые 5-10 клиентов через МФО wedge, а потом расшириться в банки и embedded finance.

## Источники
- [T1] Demand API: `кредитный скоринг` — http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9%20%D1%81%D0%BA%D0%BE%D1%80%D0%B8%D0%BD%D0%B3
- [T1] Demand API: `транзакционный скоринг` — http://172.18.0.1:9001/multi-demand?keyword=%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9%20%D1%81%D0%BA%D0%BE%D1%80%D0%B8%D0%BD%D0%B3
- [T1] Demand API: `скоринг мфо` — http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%BA%D0%BE%D1%80%D0%B8%D0%BD%D0%B3%20%D0%BC%D1%84%D0%BE
- [T1] Demand API: `андеррайтинг займов` — http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%BD%D0%B4%D0%B5%D1%80%D1%80%D0%B0%D0%B9%D1%82%D0%B8%D0%BD%D0%B3%20%D0%B7%D0%B0%D0%B9%D0%BC%D0%BE%D0%B2
- [T1] Demand API: `антифрод мфо` — http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%BD%D1%82%D0%B8%D1%84%D1%80%D0%BE%D0%B4%20%D0%BC%D1%84%D0%BE
- [T1] Банковский сектор, Банк России — https://www.cbr.ru/banking_sector/
- [T1] Интерес граждан к кредитным историям растет, Банк России — https://www.cbr.ru/press/event/?id=28503
- [T1] Тенденции на рынке МФО за 2025 год, Банк России — https://www.cbr.ru/analytics/microfinance/mfo/2025_4/
- [T1] Тенденции на рынке МФО предпринимательского финансирования за 2025 год, Банк России — https://www.cbr.ru/analytics/microfinance/2025/
- [T2] Grand View Research, loan origination digital lending platform — https://www.grandviewresearch.com/horizon/statistics/digital-lending-platform-market/solution/loan-origination/global
- [T2] RocketFin pricing — https://rocketfin.ai/en/pricing
- [T2] Credolab pricing — https://www.credolab.com/pricing
- [T2] Scanify — https://scanify-bot.ru/
- [T2] SCORISTA — https://www.scorista.ru/
- [T3] Smart Credit bot listing — https://ru.telegram-store.com/catalog/bots/smart_credit_bot

Sources: T1=9, T2=5, T3=1. Primary evidence basis: T1.
