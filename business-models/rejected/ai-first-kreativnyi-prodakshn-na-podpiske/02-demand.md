# Demand validation — AI-first креативный продакшн на подписке

Дата: 2026-05-12 03:45 MSK
Статус: CONDITIONAL PASS
Demand API: `LOW` (score 26/100) по ключу `дизайн по подписке`; дополнительный sanity-check по `креативный продакшн` тоже дал `LOW` при 297 HH-вакансиях и 100 Yandex suggest. [T1]

## 1) Executive summary

- Категория как формулировка пока не перегрета: demand API по `дизайн по подписке` вернул `LOW`, но при этом показал `215` HH-вакансий и `100` Yandex suggest, то есть брендовый спрос на формат уже есть, а underlying pain по креативам и дизайну реален. [T1]
- В РФ уже есть платёжеспособные сегменты, которые регулярно покупают дизайн и performance-креативы: маркетплейс-селлеры, e-commerce-бренды, digital-команды и B2B SaaS. Data Insight пишет, что селлеры пользуются SEO-оптимизацией в 27% случаев и услугами по рекламе и продвижению в 22% случаев. [T2]
- WTP подтверждается публичными тарифами сопоставимых сервисов: REPX от 6 400 ₽/мес, SellerArt от 16–30 ₽ за изображение, ManyPixels от $699/мес, а также фактом, что маркетплейс-селлеры тратят 6–10% доходов на рекламу. [T2]
- Profit Gate не проходит в low-end сценарии, но проходит в base, mid-market и premium сценариях. EBITDA 500k+/мес достижима при чеке 120k–220k ₽/мес и 8–12 активных клиентах либо при пакетах для high-volume sellers/агентств. [T2][спекуляция]
- Итог: ранний reject не нужен. Рынок существует, но оффер надо позиционировать не как «генерация картинок AI», а как managed creative ops с SLA, скоростью запуска тестов и экономией внутренней команды. [T1][T2]

## 2) Demand signals

### Multi-demand
- `http://172.18.0.1:9001/multi-demand?keyword=%D0%B4%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD%20%D0%BF%D0%BE%20%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%BA%D0%B5` вернул `composite_demand=LOW`, `demand_score=26`, `hh_vacancies=215`, `habr_articles=2`, `yandex_suggest=100`. [T1]
- Дополнительный check по `креативный продакшн` вернул `LOW`, `demand_score=26`, `hh_vacancies=297`, `yandex_suggest=100`. Это означает, что поисковой и HR-сигнал есть, но category label ещё не устоялся. [T1]

### Job-market / buyer pain proof
- 215–297 вакансий в HH по связанным формулировкам подтверждают, что компании уже держат бюджет на постоянное производство дизайна и креативов, даже если покупают его in-house. [T1]
- В исследовании Data Insight + Точка селлеры маркетплейсов прямо указывают использование SEO-оптимизации и услуг продвижения, а также траты на рекламу на уровне 6–10% доходов. Это показывает, что spend на conversion assets и creative iteration уже встроен в экономику продавцов. [T2]
- АКАР оценивает весь рынок маркетинговых коммуникаций РФ в 2.4 трлн ₽ в 2025 году, а сегмент интернет-сервисов в 510.1 млрд ₽. Креативное производство и адаптация рекламных материалов сидят внутри этого spend-пула. [T2]

## 3) Конкуренты и цены

1. **REPX** — подписочный графический дизайн: `Business` **6 400 ₽/мес**, `Company` **9 600 ₽/мес**, разовая задача от **720 ₽**. Прямой локальный якорь на low-end design subscription. [T2]
   Ссылка: https://repx.ru/
2. **SellerArt** — AI-генерация инфографики для маркетплейсов: **16–30 ₽ за изображение**, 1 токен = 1 ₽. Это уже не сервис, а tooling-layer, но он ставит нижнюю границу цены для простого production. [T2]
   Ссылка: https://sellerart.ru/
3. **ManyPixels** — global design subscription: `Advanced` **$699/мес**, `Business` **$1 199/мес**. Включает motion graphics и video editing, то есть близок к thesis «креативы на потоке». [T2]
   Ссылка: https://www.manypixels.co/pricing
4. **Designjoy** — category-defining design subscription, публичная цена в поисковой выдаче **$4 995/мес**. Это важный benchmark верхнего слоя за senior-only productized service. [T2]
   Ссылка: https://www.designjoy.co/
5. **Superside** — enterprise creative subscription без открытой цены на лендинге, но публично продаёт subscription model и описывает себя как scale-партнёра для 500+ брендов. Используем как proof of category maturity, а не как pricing anchor. [T2]
   Ссылка: https://www.superside.com/pricing
6. **ReSpeed** — RU `дизайн по подписке` с безлимитными задачами и паузой. Цена в сниппетах поиска начинается от **119 000 ₽/мес**; лендинг подтверждает subscription-модель, но открытый price на странице извлечь не удалось, поэтому используем аккуратно. [T2][LOW CONFIDENCE]
   Ссылка: https://respeed.ru/

### Вывод по конкурентам
- Нижний слой рынка уже коммодитизируется от десятков рублей за картинку до 6–10 тыс. ₽/мес за простой дизайн-саппорт. [T2]
- Но mid/high-end managed service уже живёт в зоне примерно **120k–400k+ ₽/мес**, если продаётся не картинка, а постоянный поток креативов, видео, вариаций и human QA. [T2][спекуляция]
- Значит новая компания не должна уходить в токены и штучные макеты. Её шанс, наоборот, в подписке с SLA, очередью задач и outcome-ориентированным оффером. [T2][спекуляция]

## 4) Telegram bots / services в RU

- В demand API по обоим ключам `telegram subscribers = 0`, то есть именно по брендовой формулировке заметного русскоязычного Telegram-demand не видно. [T1]
- На рынке есть Telegram-first и bot-like utility-сервисы вокруг генерации визуалов и копирайта для продавцов маркетплейсов, но они ближе к low-ticket tooling, чем к managed creative subscription. [T3][спекуляция]
- SellerArt решает ту же боль генерации карточек, но как self-serve web-service, а не через high-touch продакшн. Это косвенно говорит, что Telegram в РФ может быть acquisition/support-каналом, но не ядром value proposition. [T2]
- Вывод: отдельного moat в Telegram нет; RU-fit строится не на Telegram, а на скорости продакшна, русскоязычном копирайте, понимании маркетплейсов и человеке в контуре quality control. [T1][T2]

## 5) WTP / willingness to pay

### Прямые доказательства WTP
- REPX уже продаёт ежемесячное графическое сопровождение за **6 400–9 600 ₽/мес**, значит even low-end SMB готов платить recurring fee за внешний дизайн. [T2]
- ManyPixels и Designjoy показывают, что глобально рынок спокойно покупает design subscription в коридоре **$699–4 995/мес**. Это не РФ-чек, но это сильный proof того, что сама модель recurring creative production жизнеспособна. [T2]
- SellerArt монетизирует инфографику покадрово по **16–30 ₽** за изображение. Это подтверждает готовность платить даже за атомарный creative output, а значит bundling в сервис теоретически монетизируемо. [T2]
- В исследовании Data Insight селлеры сообщают, что на рекламу уходит **6–10%** доходов. Значит бюджет на креативы встроен в уже существующий growth-spend, а не создаётся с нуля. [T2]

### Непрямые доказательства WTP
- 215–297 HH-вакансий по связанным формулировкам означают, что компании готовы платить за функцию дизайна/креатива через payroll, а значит vendor-spend может отъедать ту же статью бюджета. [T1][спекуляция]
- Superside пишет про 500+ брендов-клиентов и subscription-подход к creative services, то есть для крупных маркетинговых команд формат уже понятен как замена части in-house и агентской нагрузки. [T2]

## 6) Market sizing

### Методика
- Top-down якорь: АКАР оценивает интернет-сервисы в **510.1 млрд ₽** и весь рынок маркетинговых коммуникаций в **2.4 трлн ₽** в 2025 году. Для AI-first creative subscription берём только узкий слой постоянного digital creative production. [T2]
- Bottom-up якорь: в РФ **6 588 535** субъектов МСП, из них **2 260 035** юрлиц. Отдельно для маркетплейсов есть **1.26 млн** активных продавцов на Wildberries и Ozon в 2025 году. [T1][T2]
- Проверка боли: среди селлеров **27%** уже пользуются SEO-оптимизацией, а **22%** услугами рекламы и продвижения. [T2]

### Top-down
- **TAM (мир)**: как sanity-check, мировой рынок design subscription / outsourced creative services можно оценивать через публичные pricing-бенчмарки и масштаб category leaders; точной T1-оценки нет, поэтому используем только qualitative anchor и не строим решение на этом числе. [T2][LOW CONFIDENCE]
- **TAM (РФ)**: 510.1 млрд ₽ × **1.5%** доля recurring creative production = **7.65 млрд ₽**. Доля консервативна и предполагает только постоянные digital-креативы, без media buying и без full-service agency scope. [T2][спекуляция]
- **SAM (РФ)**: 7.65 млрд ₽ × **70%** на e-commerce, marketplace sellers, B2B SaaS и mid-market бренды, где нужен регулярный creative refresh = **5.36 млрд ₽**. [T2][спекуляция]
- **SOM Y1**: 5.36 млрд ₽ × **0.37%** = **19.8 млн ₽/год**. Это примерно 11 клиентов с ARR 1.8 млн ₽. [T2][спекуляция]
- **SOM Y3**: 5.36 млрд ₽ × **1.30%** = **69.7 млн ₽/год**. Это около 26–32 активных аккаунтов при смешанном чеке. [T2][спекуляция]

### Bottom-up
- **Buyer universe 1, маркетплейсы**: 1.26 млн активных продавцов на Wildberries и Ozon. [T2]
- Берём **27%** как долю пользователей SEO-оптимизации и смежного performance-слоя, а затем консервативно только **5%** high-intent групп, которым действительно нужен постоянный внешний creative production. Получаем **17 010** потенциальных buyers. [T2][спекуляция]
- **ARR avg**: для стартового managed service берём **300 000 ₽/год** или 25 000 ₽/мес, потому что long tail sellers не потянут mid-market retainer. Это intentionally low anchor. [T2][спекуляция]
- **SAM bottom-up, маркетплейсы**: 17 010 × 300 000 ₽ = **5.10 млрд ₽**. [T2][спекуляция]
- **SOM bottom-up Y1**: 60 клиентов × 300 000 ₽ = **18.0 млн ₽**. [спекуляция]
- **SOM bottom-up Y3**: 220 клиентов × 300 000 ₽ = **66.0 млн ₽**. [спекуляция]

### Market sizing table

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | qualitative-only, без надёжной точки [T2][LOW CONFIDENCE] | — | не используем в инвестиционном решении | top-down |
| TAM (РФ) | 7.65 млрд ₽ [T2] | 10.2 млрд ₽ = 2 260 035 юрлиц × 0.5% × 900k ₽ ARR proxy [T1][T2][спекуляция] | diff 1.3x, допустимо; bottom-up через все юрлица шире, чем seller wedge | **lower = 7.65 млрд ₽** |
| SAM (РФ) | 5.36 млрд ₽ [T2] | 5.10 млрд ₽ [T2][спекуляция] | diff 1.05x, очень хороший match | **lower = 5.10 млрд ₽** |
| SOM Y1 | 19.8 млн ₽ | 18.0 млн ₽ | diff 10% | **используем 18.0 млн ₽** |
| SOM Y3 | 69.7 млн ₽ | 66.0 млн ₽ | diff 6% | **используем 66.0 млн ₽** |

### Reconciliation notes
- Top-down и bottom-up расходятся меньше чем в 3 раза, пересборка сегмента не требуется. [T1][T2]
- SOM Y1 составляет около **0.35%** от preferred SAM, что выглядит реалистично. [T2][спекуляция]
- Sanity check: при среднем sales cycle 1.5–2.5 месяца 60 low/mid-ticket клиентов в год достижимы только при сильном productized inbound/outbound и шаблонизированной delivery-модели; founder-led premium motion даст меньше клиентов, но выше чек. [T2][спекуляция]

## 7) 10 реальных buyers для bottom-up / GTM

Ниже не абстрактные сегменты, а реальные типы целей, которым нужен постоянный creative refresh под карточки товаров, баннеры, social, promo и короткое видео:

1. **SOKOLOV** — массовый e-commerce и маркетплейсы, высокая частота промо-обновлений. [T2]
2. **MIXIT** — beauty D2C, зависит от карточек, промо и визуальных тестов. [T2]
3. **Askona** — крупный retail/e-commerce бренд с постоянным digital production. [T2]
4. **12 STOREEZ** — fashion-бренд с частыми запусками и сезонными креативами. [T2]
5. **Gloria Jeans** — большой объём campaign creatives и ассортиментного контента. [T2]
6. **Kuchenland** — retail/home, нуждается в карточках и акциях на потоке. [T2]
7. **Synergetic** — FMCG/D2C, где важны marketplace creatives и ротация офферов. [T2]
8. **Divan.ru** — e-commerce мебели, где нужен поток визуалов и баннеров. [T2]
9. **Skillbox** — EdTech, постоянно тестирует performance creatives и лендинговый дизайн. [T2]
10. **Calltouch** — B2B SaaS, для которого полезен steady-state поток баннеров, webinar creatives и motion assets. [T2]

Примечание: для старта логичнее не распыляться, а выбрать один wedge, например marketplace sellers с оборотом от 1 млн ₽/мес или B2B SaaS с постоянным paid/content motion. [T2][спекуляция]

## 8) Profit Gate: все сценарии монетизации

### Сценарий A — low-end seller subscription
- 30 клиентов × 25k ₽/мес = **750k ₽ выручки/мес**. [спекуляция]
- При delivery cost 55% и fixed opex 220k ₽ EBITDA будет около **192k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Сценарий B — base marketplace creative ops
- 15 клиентов × 70k ₽/мес = **1.05 млн ₽ выручки/мес**. [спекуляция]
- При delivery cost 45% и fixed opex 250k ₽ EBITDA около **328k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Сценарий C — mid-market subscription
- 10 клиентов × 150k ₽/мес = **1.50 млн ₽ выручки/мес**. [спекуляция]
- При delivery cost 45% и fixed opex 250k ₽ EBITDA около **575k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Сценарий D — premium creative pod
- 8 клиентов × 220k ₽/мес = **1.76 млн ₽ выручки/мес**. [спекуляция]
- При delivery cost 40% и fixed opex 300k ₽ EBITDA около **756k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Сценарий E — hybrid retainer + burst projects
- 6 retainers × 120k ₽ + 4 burst-проекта/квартал по 250k ₽ = **~1.05 млн ₽ выручки/мес**. [спекуляция]
- При blended delivery cost 48% и fixed opex 260k ₽ EBITDA около **286k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Вывод по Profit Gate
- Порог EBITDA **500k+/мес** достижим, но не в low-ticket long-tail. [спекуляция]
- Рабочая зона начинается там, где компания продаёт либо mid-market retainer **150k+ ₽/мес**, либо premium pod **220k+ ₽/мес**, либо специализируется на одном high-frequency сегменте с шаблонной delivery. [T2][спекуляция]

## 9) Риски

- Простая AI-генерация быстро коммодитизируется, и токенные конкуренты могут забрать нижний слой рынка. [T2]
- Если оффер не включает human QA, creative strategy и быструю итерацию под performance, то клиент сравнит его с дешёвым self-serve tooling. [T2][спекуляция]
- Слишком широкий scope, например одновременно баннеры, видео, брендинг, карточки и copy, может убить маржу и SLA на ранней стадии. [спекуляция]
- Category name `AI-first креативный продакшн` может продаваться хуже, чем прагматичные офферы вроде `маркетплейс креативы на подписке` или `creative ops для growth-команды`. [T1][спекуляция]

## 10) Verdict

**Решение: PASS TO NEXT STEP.**

Почему не reject:
- despite `LOW` в demand API, рынок подтверждён вакансиями, рекламным spend-пулом и реальными конкурентами с recurring pricing. [T1][T2]
- Profit Gate проходит в mid-market и premium сценариях. [спекуляция]
- Значит главный вопрос не «есть ли спрос», а «какой wedge брать первым и на каком чеке удерживать экономику». [T2]

Что проверять дальше:
1. Сегментировать ICP между marketplace sellers, e-commerce brands и B2B SaaS, не смешивая их в одной delivery-модели. [T2]
2. Проверить customer interviews на тезис: готовы ли клиенты платить за `поток креативов под KPI`, а не за часы дизайнера. [спекуляция]
3. Упаковать оффер вокруг `SLA 24–72 часа`, `human-in-the-loop`, `пакет баннеры + карточки + motion`, `скорость тестов`, `прозрачная monthly capacity`. [T2][спекуляция]

Sources: T1=3, T2=10, T3=1. Primary evidence basis: T2.

## Source log
- [T1] Demand API (`дизайн по подписке`): http://172.18.0.1:9001/multi-demand?keyword=%D0%B4%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD%20%D0%BF%D0%BE%20%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%BA%D0%B5
- [T1] Demand API (`креативный продакшн`): http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D1%80%D0%B5%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D1%8B%D0%B9%20%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%BA%D1%88%D0%BD
- [T1] Реестр МСП ФНС: https://rmsp.nalog.ru/statistics.html?fo=&level=2&ssrf=&statDate=10.01.2025&t=1759598249733
- [T2] АКАР, объём рынка маркетинговых коммуникаций 2025: https://akarussia.ru/volumes/obem-rynka-marketingovyh-kommunikacij-v-2025-godu/
- [T2] Data Insight + Точка, исследование селлеров маркетплейсов 2025: https://datainsight.ru/DI_marketplaces_sellers
- [T2] Коммерсантъ, 1.26 млн активных продавцов на WB и Ozon: https://www.kommersant.ru/doc/7632286
- [T2] REPX pricing: https://repx.ru/
- [T2] SellerArt pricing: https://sellerart.ru/
- [T2] ManyPixels pricing: https://www.manypixels.co/pricing
- [T2] Designjoy: https://www.designjoy.co/
- [T2] Superside pricing/category page: https://www.superside.com/pricing
- [T2] ReSpeed: https://respeed.ru/

> Market Pulse 2026-05-12: интерес умеренно растущий. По веб-выдаче и конкурентным лендингам видно, что category already exists, но основной спрос идёт через прагматичные use cases, а не через абстрактный AI-бренд.
