# Demand validation — Captions AI / Mirage

Дата: 2026-04-24
Статус этапа: proceed
Итог по спросу: **MEDIUM**

> Market Pulse 2026-04-25: растущий интерес.

## 1) Executive summary
- Категория AI-видео для маркетинга уже доказала платежеспособность глобально: Captions сообщил 3,2 млн загрузок и $28,4 млн in-app revenue за 365 дней, Creatify сообщил $9 млн+ ARR и 10 000+ команд, HeyGen обслуживает 100 000+ бизнесов [T2].
- В РФ сигнал по узкому запросу «ai video ads» слабый, но по более близкому пользовательскому языку спрос уже не нулевой: endpoint `multi-demand` дал `LOW` для `ai video ads`, но `MEDIUM` для `нейросеть для видео` с 610 HH-вакансиями и score 35 [T1]. Это значит, что рынок существует, но покупает не «AI ads» как термин, а «нейросеть для видео / talking avatar / генерация роликов».
- В РФ уже есть Telegram-native конкуренты и сервисы: NanoReactorBot, Kolersky Video Bot, Ptichka AI [T2/T3]. Это снижает риск отсутствия локального спроса, но повышает риск коммодитизации.
- Profit Gate проходит в нескольких сценариях. Даже без enterprise компания может выйти на EBITDA >500 тыс. ₽/мес через self-serve + agency bundles.

## 2) Demand signals
### Endpoint demand check
- `keyword=ai video ads` → composite_demand=LOW, demand_score=3, HH vacancies=27, Habr=2, yandex_suggest=2 [T1, internal tool].
- `keyword=говорящий аватар` → composite_demand=LOW, demand_score=15, yandex_suggest=100 [T1, internal tool].
- `keyword=нейросеть для видео` → composite_demand=MEDIUM, demand_score=35, HH vacancies=610, Google Trends RU=20, yandex_suggest=100 [T1, internal tool].

**Вывод:** продуктовый спрос в РФ есть, но он выражен через широкую задачу «сделать видео быстрее и дешевле», а не через англоязычный wedge performance-video.

### External evidence of willingness to pay
- Captions pricing: Pro $9.99/мес, Max $24.99/мес, Scale $69.99/мес, enterprise custom [T2, official pricing].
- Creatify pricing: Starter $33/мес, Pro $49/мес, enterprise custom [T2, official pricing].
- HeyGen pricing: Creator $29/мес, Pro $99/мес [T2, official pricing].
- Runway pricing: Standard $12/мес, Pro $28/мес, Unlimited $76/мес [T2, official pricing].
- Kolersky Video Bot: подписка 120/250/500/1000 кредитов за 129/250/490/890 ₽ [T3, публичная страница продукта].
- NanoReactorBot: видео-тарификация pay-as-you-go, например Seedance 1.5 от 10 ₽/с, Kling 2.6 от 12 ₽/с, Sora 2 от 17 ₽/с, Veo 3.1 от 34 ₽/с [T2, официальный сайт].

По курсу ЦБ РФ на 2026-04-24: 1 USD = 74,8349 ₽ [T1]. Значит self-serve рынок уже нормализовал цены примерно в диапазоне **900–7 500 ₽/мес** и micro-usage **10–34 ₽/сек видео**.

## 3) Competitor set with prices
| Игрок | Позиционирование | Цена | Вывод |
|---|---|---:|---|
| Captions | AI short-form editing, avatars, ads | $9.99 / $24.99 / $69.99 в мес ≈ 748 / 1 870 / 5 238 ₽ [T2] | Референс по mobile-first self-serve |
| Creatify | AI video ads для performance marketing | $33 / $49 в мес ≈ 2 469 / 3 667 ₽ [T2] | Прямой аналог ad-creative wedge |
| HeyGen | AI avatars, localization, marketing video | $29 / $99 в мес ≈ 2 170 / 7 409 ₽ [T2] | Показывает готовность платить за avatar-first сценарий |
| Runway | generalist AI video stack | $12 / $28 / $76 в мес ≈ 898 / 2 095 / 5 687 ₽ [T2] | Давит сверху как infra-like suite |
| Kolersky Video Bot | RU Telegram bot | 129 / 250 / 490 / 890 ₽ [T3] | Сильный локальный low-end ceiling |
| NanoReactorBot | RU Telegram mini-app | 10–34 ₽/сек видео [T2] | Локальный usage-based competitor |

## 4) Telegram / RU landscape
- **NanoReactorBot**: Telegram/MAX mini-app, text-to-video, image-to-video, video-to-video, явная pay-as-you-go тарификация в рублях [T2].
- **Kolersky Video Bot**: Telegram-бот с Kling, Veo, Runway, Luma; продаёт подписки в рублях и кредиты [T3].
- **Ptichka AI**: массовый Telegram/MAX consumer bot, уже продаёт AI-фото и трендовые видео в РФ/СНГ [T3].

**Вывод:** локальный дистрибуционный слой уже сместился в Telegram. Если заходить в РФ, web-only продукт будет слабее, чем bot/mini-app + web studio.

## 5) WTP, pain, repeatability
### Pain
- SMB, ecom и агентствам нужны дешёвые креативы под Telegram Ads, VK, маркетплейсы, Reels/Shorts и UGC-like ролики без отдельного продакшна [T2].
- 610 HH-вакансий по широкому паттерну `нейросеть для видео` показывает, что работодатели уже ищут навыки и workflow вокруг AI-видео, а не только классический монтаж [T1].

### Proof of willingness to pay
- Self-serve цены у 4 западных игроков лежат в платёжном коридоре **$12–99/мес** [T2].
- В РФ есть покупки в рублях даже у Telegram-ботов нижнего сегмента, значит порог оплаты у локального пользователя есть уже сейчас [T2/T3].
- Captions ($28,4 млн in-app revenue за 365 дней), Creatify ($9 млн+ ARR), HeyGen profitability/масштаб категории в публичных публикациях подтверждают, что это не только demo-рынок [T2].

### Repeat usage
Repeat usage вероятен у 3 сегментов:
1. performance-агентства, которым постоянно нужны новые вариации креативов [T2];
2. e-commerce sellers/бренды с высокой частотой акций [T2];
3. инфобизнес/edtech/эксперты, которым нужен avatar-led контент сериями [T2/T3].

## 6) Market sizing
**Методика:** считаю и top-down, и bottom-up. Для сопоставления беру узкий сегмент: **AI-инструменты для production short-form marketing video / avatar creatives для SMB, агентств и digital-native брендов в РФ**.

### Top-down
- Российский рынок маркетинговых коммуникаций в 2025 году превысил **2,4 трлн ₽** [T2, АКАР].
- Из них суммарный объём рекламы во всех основных сегментах превысил **980 млрд ₽** [T2, АКАР].
- Видео как сегмент остаётся значимым, а online-video был среди самых быстрорастущих подсегментов [T2, АКАР].
- Для AI-video-creative беру адресуемую долю **0,6%** от всего рынка маркетинговых коммуникаций: это бюджет не на media buying, а на создание, адаптацию, локализацию и тестирование коротких video creatives. Получаем **TAM РФ ≈ 14,4 млрд ₽** [T2 + analyst inference].
- Далее ограничиваемся self-serve SMB/agency сегментом, где AI реально заменяет часть ручного продакшна. Беру **35%** от TAM РФ. **SAM top-down ≈ 5,0 млрд ₽** [T2 + analyst inference].
- Реалистичный capture: **Y1 = 2%**, **Y3 = 8%** от SAM. Получаем **SOM Y1 ≈ 100 млн ₽**, **SOM Y3 ≈ 400 млн ₽**.

### Bottom-up
- В обновлённом реестре ФНС на 2025-07-10 было **6,4 млн субъектов МСП** [T1, ФНС].
- Для этого продукта релевантна не вся база МСП, а digital-heavy слой. Беру **0,6%** от МСП как агентства, e-commerce, edtech, недвижимость, beauty, local services и creator-led SMB с регулярной закупкой креативов. Это **38 400 потенциальных покупателей** [T1 + analyst inference].
- Доля с подтверждённой болью: **50%**. Основание: medium signal по `нейросеть для видео`, 610 HH-вакансий, наличие локальных бот-сервисов и быстрорастущий online-video сегмент [T1/T2]. Получаем **19 200 active-need buyers**.
- Средний ARR беру **180 000 ₽/год**: это эквивалент 15 000 ₽/мес, то есть выше telegram-bot low-end и ниже типового агентского retainer. Для SMB/agency bundle это реалистично [T2/T3 + analyst inference].
- **SAM bottom-up = 19 200 × 180 000 ₽ = 3,456 млрд ₽**.
- Реалистичный capture: **Y1 = 3%**, **Y3 = 10%**. Тогда **SOM Y1 = 103,7 млн ₽**, **SOM Y3 = 345,6 млн ₽**.

### Market sizing table
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | ~59,0 млрд ₽ (USD 788,5M × 74,8349) [T3+T1] | — | global only, low confidence | top-down |
| TAM (РФ) | 14,4 млрд ₽ [T2] | 6,9 млрд ₽* [T1/T2] | diff 2,1x, в bottom-up заложен только digital-heavy слой; допустимо | **6,9 млрд ₽** |
| SAM (РФ) | 5,0 млрд ₽ [T2] | 3,456 млрд ₽ [T1/T2] | diff 1,45x, расхождение в пределах нормы | **3,456 млрд ₽** |
| SOM Y1 | 100 млн ₽ | 103,7 млн ₽ | diff 3,7% | **100 млн ₽** |
| SOM Y3 | 400 млн ₽ | 345,6 млн ₽ | diff 15,8% | **345,6–400 млн ₽** |

\* Bottom-up TAM РФ = 38 400 buyers × 180 000 ₽ = 6,912 млрд ₽.

### 10 реальных buyers для bottom-up sanity check
1. Kokoc Group / Kokoc Performance [T2]
2. Realweb [T2]
3. Adventum [T2]
4. Ingate Performance [T2]
5. Demis Group [T2]
6. Skyeng [T2]
7. Skillbox [T2]
8. Самокат [T2]
9. SOKOLOV [T2]
10. Level Group [T2]

Это не весь рынок, а примеры компаний с постоянной потребностью в performance/video creative и высокой частотой тестирования офферов.

## 7) Profit Gate: can EBITDA exceed 500k ₽/mo?
### Scenario A — self-serve SaaS
- 500 платящих клиентов × 8 000 ₽ ARPA/мес = 4,0 млн ₽ выручки
- Валовая маржа 75% → 3,0 млн ₽ gross profit
- Opex: команда 1,8 млн ₽/мес
- **EBITDA ≈ 1,2 млн ₽/мес**

### Scenario B — agency / team bundles
- 120 клиентов × 25 000 ₽/мес = 3,0 млн ₽ выручки
- Валовая маржа 80% → 2,4 млн ₽
- Opex 1,6 млн ₽
- **EBITDA ≈ 0,8 млн ₽/мес**

### Scenario C — hybrid self-serve + white-label/API
- 300 self-serve × 8 000 ₽ = 2,4 млн ₽
- 20 agency/team accounts × 60 000 ₽ = 1,2 млн ₽
- 3 white-label/API accounts × 150 000 ₽ = 0,45 млн ₽
- Итого выручка 4,05 млн ₽
- При blended GM 72% gross profit ≈ 2,9 млн ₽
- Opex 1,9 млн ₽
- **EBITDA ≈ 1,0 млн ₽/мес**

**Profit Gate verdict:** **PASS**. Порог 500 тыс. ₽/мес достижим в нескольких сценариях без фантастических объёмов.

## 8) Risks
- RU спрос пока формулируется слишком широко, категория может остаться feature-layer поверх generalist models [T1/T2].
- Нижний сегмент быстро уходит в Telegram-боты и pay-as-you-go, поэтому premium SaaS без distribution edge уязвим [T2/T3].
- Compute economics и модерация deepfake/avatar контента могут съедать маржу при росте usage-heavy клиентов [T2/T3].
- Конкуренция идёт сразу с двух сторон: global product suites и local bot wrappers [T2/T3].

## 9) Demand verdict
**Вердикт: PROCEED.**

Почему не reject:
- core category monetizes globally [T2];
- в РФ есть локальный usage и локальные игроки в Telegram [T2/T3];
- market sizing даёт SAM порядка **3,5 млрд ₽** и SOM Y1 около **100 млн ₽**;
- Profit Gate проходит с запасом.

Что нужно проверить на следующем шаге:
1. CAC на Telegram/creator acquisition в РФ.
2. Разницу retention между avatar-first, ad-first и editor-first JTBD.
3. Насколько можно вытащить B2B ARPA в 15–25 тыс. ₽/мес без enterprise sales.

## Sources
- АКАР, объём рынка маркетинговых коммуникаций в 2025 году: https://akarussia.ru/volumes/obem-rynka-marketingovyh-kommunikacij-v-2025-godu/
- ФНС, обновлённый реестр МСП: https://www.nalog.gov.ru/rn77/news/activities_fts/16447933/
- Captions pricing: https://captions.ai/pricing
- Creatify pricing: https://creatify.ai/pricing
- HeyGen pricing: https://www.heygen.com/pricing
- Runway pricing: https://runwayml.com/pricing
- NanoReactorBot: https://nanoreactor.ru/
- Kolersky Video Bot: https://kolersky.com/video_sd_bot
- Ptichka AI: https://ptichka.ai/
- Grand View Research, AI video generator market: https://www.grandviewresearch.com/industry-analysis/ai-video-generator-market-report
- TechCrunch / Captions-Mirage: https://techcrunch.com/2026/03/24/mirage-raises-75m-to-continue-building-models-for-its-ai-video-editing-app-captions/
- TechCrunch / Creatify: https://techcrunch.com/2024/10/29/creatify-raises-15-5m-for-its-ai-platform-that-makes-marketing-videos-from-product-links-or-descriptions/

Sources: T1=3, T2=8, T3=3. Primary evidence basis: T2.

> Market Pulse 2026-04-25: фиксируется рост интереса. В текущей веб-выдаче усилился поток свежих публикаций, запусков и коммерческих предложений по AI-video, talking avatars и генерации рекламных роликов.

## Market Pulse
> Market Pulse 2026-04-26: растущий интерес.
