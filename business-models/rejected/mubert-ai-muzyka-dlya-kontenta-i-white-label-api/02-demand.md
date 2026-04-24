# Demand Validation — Mubert AI музыка для контента и white-label API

Дата: 2026-04-24
Статус: EARLY REJECT

## 1) Вывод

Спрос в РФ на отдельный AI-сервис генерации роялти-фри музыки и джинглов есть как нишевый supporting use case, но не как самостоятельная fund-scale категория на текущем этапе. По обязательному demand endpoint кейворд `AI music generator royalty free API jingles Russia` вернул `composite_demand=LOW`, `demand_score=0`, `hh_ru=0`, слабые сигналы в Google Trends RU и Yandex Suggest [T2/T3]. При этом глобальный рынок подтверждает willingness to pay, но этот спрос сосредоточен у крупных международных игроков, а не в российском standalone B2B wedge [T2].

Итог: **DEMAND = LOW**, **Profit Gate = FAIL**, поэтому кейс уходит в rejected сейчас.

## 2) Конкуренты и цены

| Игрок | Что продаёт | Цена | Что это значит для кейса |
|---|---|---:|---|
| Suno | AI music generation для creators | Pro $8/мес, Premier $24/мес, есть commercial rights [T1] | Рынок платит, но consumer price point низкий, что давит ARPU в РФ |
| Beatoven.ai | AI music для видео creators | $10/мес или $100/год; $20/мес или $200/год [T1] | Ещё один price anchor в диапазоне $10–20/мес |
| Soundful | AI music для creators/teams | Free, Plus/Pro/Business/Enterprise tiers, коммерческое использование только на premium [T1] | Категория уже коммодитизируется, value уходит в volume/license, а не в уникальный core product |
| Mubert API | API и white-label для apps/platforms | в брифе зафиксирован диапазон $49–499/мес; API ориентирован на apps, games, video editors, UGC platforms [T1/T2] | Для локального игрока это ceiling по SMB/API price, но не доказательство локального спроса |

### Ключевой вывод по конкурентам

- Глобальный price corridor уже прозрачен: примерно **$8–24/мес для creator/self-serve** и **$49–499/мес для API/white-label** [T1/T2].
- При курсе ЦБ РФ на 24.04.2026 **1 USD = 74.8349 ₽** [T1], это даёт ориентиры **~599–1,796 ₽/мес** для consumer и **~3,667–37,342 ₽/мес** для SMB/API.
- Это подтверждает WTP, но одновременно ограничивает локальный ARPA: импортный price ceiling уже низкий, а differentiation у нового локального сервиса слабая [T1/T2].

## 3) Проверка спроса и WTP

### Demand signals

- Multi-demand endpoint по обязательному запросу вернул `LOW` и `demand_score=0`; внутри: `hh_ru=0`, `google_trends_ru=1`, `yandex_suggest=2`, `habr_articles=2` [T2/T3].
- Это означает, что в РФ почти нет observable bottom-up demand именно на standalone AI music generator/API, в отличие от фото, видео и copywriting AI [T2].
- Глобальный сигнал есть: TechCrunch сообщает, что Suno достиг **2 млн платящих подписчиков** и **$300 млн ARR** к 27.02.2026 [T2]. Это сильное доказательство willingness to pay в мире, но не локальной российской плотности спроса.

### WTP proof

- Пользователи уже платят мировым лидерам за коммерческие права и лимиты, значит willingness to pay как класс доказан [T1/T2].
- Однако готовность платить в РФ, вероятно, смещена в сторону **дешёвых обёрток** и **встроенной функции внутри broader creator stack**, а не в отдельный сервис для музыки [T2/T3].
- Следовательно, WTP есть, но **не в форме самостоятельного fundable продукта в РФ**.

## 4) Telegram и сервисы в RU

- Проверка RU-ландшафта не выявила сильного самостоятельного локального лидера именно в AI music. На рынке видны в основном обёртки вокруг зарубежных моделей и мульти-нейросетевые сервисы с Telegram-доступом, например Bothub с Telegram-ботом и пакетной моделью оплаты [T2/T3].
- Это плохой знак для отдельного music-only продукта: канал дистрибуции в Telegram существует, но value capture уходит к агрегаторам, а не к vertical music tool [T2/T3].
- Отсутствие заметного публичного RU-native бота/сервиса с прозрачной экономикой и сильным brand pull трактую как отрицательный локальный сигнал. **Это частично inference**, потому что публичные данные по Telegram-финансам ограничены [T3].

## 5) Market sizing

### Логика сегмента

Считаю не весь music-tech рынок, а только адресуемый сегмент для РФ: рекламные агентства, video production, creator tools/platforms и SMB-команды, которые регулярно выпускают коммерческий видеоконтент и нуждаются в легальной фоновой музыке/джинглах.

### 10 реальных buyers для bottom-up

1. Kokoc Group [T2]
2. Realweb [T2]
3. Adventum [T2]
4. AGIMA [T2]
5. Ingate [T2]
6. Okkam [T2]
7. Media Instinct Group [T2]
8. Ашманов и партнёры [T2]
9. Zebra Hero [T2]
10. Ailove [T2]

### Top-down

- В РФ по данным АКАР рекламный рынок в 2025 году вырос примерно до **~904 млрд ₽**, из них интернет-сегмент около **~470 млрд ₽** [T2].
- Для music layer беру только долю коммерческого digital/video production. Консервативно считаю, что addressable share для фоновой музыки, джинглов и sound assets внутри digital/video workflow составляет **0.3%** от интернет-рекламного рынка. Это даёт **TAM РФ ≈ 1.41 млрд ₽**. Доля 0.3% является аналитическим допущением, а не прямой статистикой, поэтому это **reconciliation assumption** [T2/T3].
- Для segment fit (только B2B mid-market, агентства, video-heavy команды, платформы) беру **20%** TAM РФ, получаю **SAM top-down ≈ 282 млн ₽** [T2/T3].
- Реалистичный capture: **3% в Y1** и **10% в Y3**, значит **SOM Y1 ≈ 8.5 млн ₽**, **SOM Y3 ≈ 28.2 млн ₽** [T2/T3].

### Bottom-up

- Rusprofile показывает **103,727 компаний** по ОКВЭД 73.11 «деятельность рекламных агентств» [T2].
- Rusprofile показывает **2,704 компании** по ОКВЭД 59.11.1 «производство кинофильмов, видеофильмов и телевизионных программ» [T2].
- Итого база покупателей в смежных сегментах: **106,431 компаний** [T2].
- Из-за низких прямых demand signals считаю, что только **1.2%** базы реально имеют частую потребность в AI music workflow в ближайшие 12 месяцев. Это даёт **~1,277 buyers**. Доля 1.2% выбрана консервативно именно потому, что explicit demand низкий; это inference [T2/T3].
- Беру **avg ARR = 180,000 ₽/год** (примерно 15,000 ₽/мес) для agency/team плана. Это ниже верхней импортной API-планки и соответствует SMB B2B-покупке без enterprise кастомизации [T1/T2].
- Тогда **SAM bottom-up ≈ 229.9 млн ₽**.
- При capture **3% Y1** получаем **SOM Y1 ≈ 6.9 млн ₽**; при **10% Y3** получаем **SOM Y3 ≈ 23.0 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | ~90 млрд ₽ proxy / ~$1.2 млрд [T2/T3] | — | world TAM собран как proxy по глобальным лидерам и category reports, низкая точность | top-down |
| TAM (РФ) | 1.41 млрд ₽ [T2/T3] | 1.92 млрд ₽ implied max (=106,431 × 1.0 × 180k) [T2] | diff ~36%, bottom-up max завышает полный uptake; беру lower | **1.41 млрд ₽** |
| SAM (РФ) | 282 млн ₽ [T2/T3] | 229.9 млн ₽ [T2/T3] | diff ~23%, в пределах нормы; беру lower | **229.9 млн ₽** |
| SOM Y1 | 8.5 млн ₽ | 6.9 млн ₽ | diff ~19% | **6.9 млн ₽** |
| SOM Y3 | 28.2 млн ₽ | 23.0 млн ₽ | diff ~18% | **23.0 млн ₽** |

Sanity check: SOM Y1 / ARR 180k ≈ 38 клиентов в год. Это уже требует стабильного pipeline при нишевом спросе и длинном дообучении value proposition. Для молодого продукта это тяжело, но теоретически возможно. Проблема не в размере SAM как таковом, а в слабом локальном pull и высокой заменимости решения [T2/T3].

## 6) Profit Gate — проверка всех сценариев

### Сценарий A. Self-serve creators
- ARPA: 1,500 ₽/мес [T1]
- Gross margin: 75% (инференс для AI audio infra) [T3]
- Fixed opex: 350k ₽/мес [T3]
- Для EBITDA 500k ₽/мес нужна выручка ~1.13 млн ₽/мес, то есть **~755 платящих пользователей**.
- При observed local demand `LOW` это не выглядит достижимым в обозримом горизонте.
- **Вердикт: FAIL**.

### Сценарий B. Agency/team subscription
- ARPA: 15,000 ₽/мес [T1/T2]
- Gross margin: 80% [T3]
- Fixed opex: 450k ₽/мес [T3]
- Для EBITDA 500k ₽/мес нужна выручка ~1.19 млн ₽/мес, то есть **~79 агентств/команд**.
- На фоне SAM ~230 млн ₽ это математически возможно, но demand evidence не показывает такой плотности покупателей, а конкуренция с импортными и bundled tools высокая.
- **Вердикт: FAIL**.

### Сценарий C. API / white-label
- ARPA: 60,000 ₽/мес [T1/T2]
- Gross margin: 70% [T3]
- Fixed opex: 650k ₽/мес [T3]
- Для EBITDA 500k ₽/мес нужна выручка ~1.64 млн ₽/мес, то есть **~28 API-клиентов**.
- Для РФ это слишком много, учитывая узкий пул реальных платформ, слабый локальный search pull и наличие Mubert как международного incumbency layer [T1/T2].
- **Вердикт: FAIL**.

### Profit Gate conclusion

Ни один из трёх сценариев не показывает убедимый путь к **EBITDA ≥ 500k ₽/мес** при текущем спросе в РФ. Даже если продукт technically working, локальная категория слишком узкая, а unit economics слишком зависят от сложной B2B-продажи или массового self-serve adoption, которого не видно в данных.

## 7) Финальный вердикт

- **Demand:** LOW
- **WTP:** есть глобально, слабый локально как standalone category
- **Market size:** узкий, в РФ скорее десятки/первые сотни миллионов рублей SAM, а не fund-scale platform market
- **Profit Gate:** FAIL
- **Решение:** **REJECTED**

Sources: T1=5, T2=7, T3=5. Primary evidence basis: T2.

## Источники

1. Mubert API, официальный сайт: https://mubert.com/api [T1]
2. Suno Pricing, официальный сайт: https://suno.com/pricing [T1]
3. Beatoven Pricing, официальный сайт: https://www.beatoven.ai/pricing [T1]
4. Soundful Pricing, официальный сайт: https://soundful.com/pricing/ [T1]
5. ЦБ РФ, курс USD на 24.04.2026: https://www.cbr.ru/scripts/XML_daily.asp [T1]
6. TechCrunch про Suno 2 млн paid и $300 млн ARR: https://techcrunch.com/2026/02/27/ai-music-generator-suno-hits-2-million-paid-subscribers-and-300m-in-annual-recurring-revenue/ [T2]
7. Rusprofile, ОКВЭД 73.11: https://www.rusprofile.ru/codes/73.11 [T2]
8. Rusprofile, ОКВЭД 59.11.1: https://www.rusprofile.ru/codes/59.11.1 [T2]
9. АКАР / публикации по рынку рекламы 2025: https://akarussia.ru/volumes/ [T2]
10. Bothub / RU aggregator context: https://bothub.chat/ [T2/T3]
11. multi-demand endpoint по обязательному запросу [T2/T3]
