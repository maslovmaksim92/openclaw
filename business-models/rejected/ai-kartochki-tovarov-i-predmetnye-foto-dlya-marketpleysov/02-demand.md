---
stage: demand-validation
sector: ECOMMERCE_ENABLEMENT
updated: 2026-05-10T11:05:00+03:00
---

# 02-demand

## Demand validation summary
- Категория уже валидирована рынком: PhotoRoom продаёт Pro-план за $9.99 в месяц и Teams за $89.99 за место в годовом биллинге, а SellerArt и Picaz уже продают аналогичные workflows продавцам маркетплейсов в РФ. Это означает, что buyer платит не за «AI ради AI», а за ускорение вывода SKU и рост CTR карточки. [T2]
- По demand endpoint наиболее релевантный запрос, «карточки товаров для маркетплейсов», даёт **MEDIUM**: demand_score 30, hh.ru vacancies 1124, yandex_suggest 100. Запрос «дизайнер инфографики маркетплейсов» даёт LOW, но с 384 вакансиями, что подтверждает боль и текущие ручные расходы. [T1/T2]
- В РФ уже есть local willingness to pay: Picaz продаёт тарифы 1 490-6 990 ₽/мес, SellerArt 6 990-24 990 ₽/мес, а Telegram-first инструменты NEALS и Upak берут 399-1 990 ₽/мес и 790-3 490 ₽/мес соответственно. [T2]
- Вывод: спрос не взрывной и не consumer-scale, но для B2B SaaS в seller tooling выглядит достаточным. Категория проходит дальше как SMB self-serve + agency/team + API/enterprise motion. [T1][T2]

## Competitors и цены
| Игрок | Что продаёт | Цена | Комментарий |
|---|---|---:|---|
| PhotoRoom | AI product photos, background removal, batch editing | $9.99/мес Pro; Teams from $89.99 per seat/year | Глобальный category leader, сильный anchor по WTP. [T2] |
| Pebblely | AI product photos for ecommerce | $19/мес Basic, $39/мес Pro, $59/мес Team | Прямой comparable по AI product imagery. [T2] |
| Picaz | AI-карточки и визуал для маркетплейсов | 1 490 / 2 990 / 6 990 ₽ в месяц | Локальный RU self-serve pricing. [T2] |
| SellerArt | Инфографика и генерация креативов для селлеров | 6 990 / 13 990 / 24 990 ₽ в месяц | Локальный mid-market/agency price point. [T2] |
| NEALS | Telegram/Mini App для AI-фото и генерации | 399 / 990 / 1 990 ₽ в месяц | Подтверждает TG-native low-ticket слой в RU. [T2] |
| Upak | Telegram-first AI-визуал/контент | 790 / 1 490 / 3 490 ₽ в месяц | Подтверждает, что RU-аудитория готова платить прямо в Telegram. [T2] |

## Buyers и budget owners
1. Бренды и продавцы с широким SKU-каталогом на Ozon и Wildberries. [T1][T2]
2. Агентства, которые ведут карточки и креативы под marketplace-канал. [T2]
3. Aggregators и сервисные команды, которым нужна пакетная генерация изображений и карточек. [T2, inference]

### 10 реальных buyer candidates
- SOKOLOV
- Gloria Jeans
- Befree
- Ralf Ringer
- Polaris
- Kitfort
- Synergetic
- ErichKrause
- 12 STOREEZ
- Vivienne Sabo

Это не «клиенты уже купили», а реальные бренды с большим каталогом на маркетплейсах, для которых стоимость ручного продакшна карточек и фото заметна. [T2, inference]

## Telegram bots/services в РФ
- **NEALS** продаётся как Telegram/Mini App и показывает low-end подписку 399-1 990 ₽/мес. [T2]
- **Upak** тоже идёт через Telegram-first сценарий с тарифами 790-3 490 ₽/мес. [T2]
- Следствие: Telegram в РФ уже работает как канал distribution и оплаты, но пока в основном для micro-SMB и creator-like use case, а не для enterprise. [T2, inference]

## Willingness to pay
- WTP подтверждён уже самим фактом существования нескольких платящих категорий: global SaaS, RU web SaaS и TG-native tools. [T2]
- Нижняя граница понятного self-serve чека в РФ сегодня выглядит как **1 490-2 990 ₽/мес**. Это видно по Picaz, NEALS и Upak. [T2]
- Для seller teams и агентств подтверждённый price band выше, **6 990-24 990 ₽/мес**, что видно по SellerArt и старшим тарифам Picaz. [T2]
- Значит, рынок уже платит не только разово «за дизайн карточки», но и за recurring workflow. Это ключевой сигнал для investable SaaS-кейса. [T2, inference]

## Market sizing

### Метод и допущения
- Курс ЦБ РФ на 8 мая 2026: **81.4954 ₽/$**. Для валютных цен ниже использую этот курс. [T1]
- В 2024 оборот интернет-торговли в РФ составил **11.3 трлн ₽**. [T2]
- Ozon сообщил о **600 тыс. активных продавцов** в 2024. Это не весь рынок РФ, но хороший anchor по масштабу seller base. [T1]
- Для top-down я беру долю расходов на создание и обновление карточек/визуала как **0.05% от GMV**. Это inference, но она согласуется с observed pricing у локальных сервисов и с тем, что расход на визуал для seller обычно измеряется малыми долями процента от продаж. [T2, inference]
- Для bottom-up беру **700 тыс.** уникальных sellers в РФ как рабочую оценку across major marketplaces, **25%** из них как каталог-heavy сегмент с регулярной потребностью, и **24 000 ₽ ARR** как средний self-serve/team blended чек. [T1][T2, inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | ~160 млрд ₽ (≈$2.0B) [T2, LOW CONFIDENCE] | — | Использую как грубый внешний anchor по глобальной category validation | top-down |
| TAM (РФ) | 5.65 млрд ₽ [T2 + inference] | 16.8 млрд ₽ [T1/T2 + inference] | diff 3.0x; bottom-up скорее отражает весь seller surface, top-down беру консервативнее | **lower** |
| SAM (РФ) | 3.96 млрд ₽ [T2 + inference] | 4.20 млрд ₽ [T1/T2 + inference] | diff ~6%; оценки сходятся после ограничения на каталог-heavy сегмент | **3.96 млрд ₽** |
| SOM Y1 | 79 млн ₽ | 63 млн ₽ | diff ~25%; реалистично для 1.5-2.0% capture | **79 млн ₽** |
| SOM Y3 | 317 млн ₽ | 252 млн ₽ | diff ~26%; остаётся ниже 10% SAM в Y3 | **317 млн ₽** |

### Top-down
- TAM РФ = 11.3 трлн ₽ × 0.05% = **5.65 млрд ₽**. [T2 + inference]
- SAM РФ = TAM × 70% marketplace-heavy visual segment = **3.96 млрд ₽**. [T2 + inference]
- SOM Y1 = SAM × 2% = **79 млн ₽**. [inference]
- SOM Y3 = SAM × 8% = **317 млн ₽**. [inference]

### Bottom-up
- Total buyers = 700 000 unique marketplace sellers in RU working estimate. [T1/T2 + inference]
- % with need = 25% catalog-heavy sellers with repeat need = **175 000**. [T1/T2 + inference]
- ARR avg = **24 000 ₽/год** blended self-serve/team contract. [T2]
- SAM_bottom_up = 175 000 × 24 000 ₽ = **4.20 млрд ₽**.
- SOM_bottom_up Y1 = 1.5% of SAM = **63 млн ₽**.
- SOM_bottom_up Y3 = 6% of SAM = **252 млн ₽**.

### Sanity check
- SOM Y1 79 млн ₽ при ARPA 24 000 ₽/год требует ~3 292 платящих аккаунта. Это агрессивно, но достижимо только при self-serve + partner motion; pure founder-led enterprise alone не вытянет. [inference]
- Deal cycle для SMB и agencies 1-2 месяца, поэтому Y1 не ломается по sales-capacity. [T2, inference]

## Profit gate scenarios
### Scenario A, self-serve SMB
- Цена: 1 490-2 990 ₽/мес.
- Для EBITDA 500K+/мес нужно примерно 800-1 100 активных платящих аккаунтов при software gross margin 75-80% и lean-команде.
- Вердикт: **проходит**, но требует сильного PLG/distribution и низкого churn.

### Scenario B, agency/team plan
- Цена: 9 900-24 900 ₽/мес.
- 80-120 агентств/команд уже дают 0.8-2.0 млн ₽ MRR; profit gate достижим заметно быстрее.
- Вердикт: **уверенно проходит**.

### Scenario C, API/white-label for integrators
- Цена: 80 000-150 000 ₽/мес за API/пакетный workflow.
- 8-12 клиентов достаточно для EBITDA выше 500K/мес.
- Вердикт: **проходит**.

### Scenario D, hybrid setup + managed creative ops
- Цена: 150 000-300 000 ₽/мес за bundle «генерация + batch ops + human QA».
- 4-6 клиентов достаточно для program threshold.
- Вердикт: **проходит с запасом**.

## Risks
- Спрос есть, но он фрагментирован и может растворяться в «наняли дизайнера/агентство» вместо отдельного SaaS. [T2]
- Category overcrowding высокая: global AI-photo tools и RU niche tools уже выровняли базовые функции. [T2]
- Без distribution moat продукт рискует остаться commodity layer со слабым удержанием. [T2, inference]

## Final assessment
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Кейс не режу на P3, потому что:
- есть подтверждённый recurring WTP в РФ и за рубежом;
- market sizing даёт SAM около **4 млрд ₽** и SOM Y1/Y3, достаточный для fundable niche SaaS;
- profit gate проходит не в одном, а сразу в нескольких сценариях монетизации.

Но идти дальше стоит только с жёстким фокусом на distribution: Ozon/WB sellers, agencies, TG-led acquisition и пакетные workflows, а не как «ещё один генератор картинок». 

## Sources
- [T1] Банк России, курсы валют на 08.05.2026: https://www.cbr.ru/currency_base/daily/
- [T1] Ozon FY2024 results / active sellers 600k: https://ir.ozon.com/news-releases/news-release-details/ozon-holdings-plc-announces-fourth-quarter-and-full-year-2024
- [T2] АКИТ, оборот интернет-торговли в РФ 11.3 трлн ₽ за 2024: https://akit.ru/%D0%B8%D1%82%D0%BE%D0%B3%D0%B8-2024-%D0%B3%D0%BE%D0%B4%D0%B0/
- [T2] PhotoRoom pricing: https://www.photoroom.com/pricing
- [T2] Pebblely pricing: https://pebblely.com/pricing/
- [T2] Picaz pricing: https://picaz.ru/pricing
- [T2] SellerArt pricing: https://sellerart.ru/pricing
- [T2] NEALS pricing: https://neals.ru/pricing
- [T2] Upak pricing: https://upak.ru/pricing
- [T2] Demand endpoint, запросы от 2026-05-10: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%B0%D1%80%D1%82%D0%BE%D1%87%D0%BA%D0%B8%20%D1%82%D0%BE%D0%B2%D0%B0%D1%80%D0%BE%D0%B2%20%D0%B4%D0%BB%D1%8F%20%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%D0%BE%D0%B2

Sources: T1=2, T2=8, T3=0. Primary evidence basis: T2.
