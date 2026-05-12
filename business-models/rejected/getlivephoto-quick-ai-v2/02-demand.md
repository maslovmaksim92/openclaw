---
stage: demand-validation
case: getlivephoto-quick-ai-v2
date: 2026-04-21
analyst: branch-models-lead
sector: QUICK-AI
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

> Market Pulse 2026-04-25: растущий интерес.

## Кейс
GetLivePhoto, consumer-first Telegram-сервис оживления фото в короткое MP4-видео.

## Итог
**Статус: CONDITIONAL PASS**

В РФ есть заметный consumer intent именно по use case `оживить фото`: demand API показывает `demand_score=29`, `google_trends_ru=58`, `yandex_suggest=100`, при этом сам GetLivePhoto уже упаковал продукт в понятный Telegram-flow с генерацией за **20–40 секунд** и публичными тарифами от **79 ₽** до **990 ₽** [T1][T2]. Это не enterprise-категория и не hiring-driven рынок, поэтому `composite_demand=LOW` здесь не должен трактоваться как отсутствие спроса, скорее как слабый B2B/hiring след.

Ключевой вопрос не в наличии интереса, а в монетизации. При текущей сетке цен продукт может собрать выручку 500k+ ₽/мес, но для прохода program gate по **EBITDA 500k+ ₽/мес** нужен либо сильный органический/виральный канал, либо дешёвый Telegram/media acquisition. Иначе paid CAC быстро съест экономику. Поэтому кейс не стоит резать на P3, но на P4/P5 нужно жёстко проверить unit economics и acquisition reality.

## 1. Спрос и сигналы рынка

### Demand API
- `оживить фото` → **LOW**, `demand_score=29`, `google_trends_ru=58`, `hh_vacancies=5`, `yandex_suggest=100`. [T2]
- `оживление фото` → **LOW**, `demand_score=20`, `google_trends_ru=6`, `hh_vacancies=14`, `yandex_suggest=100`. [T2]
- `photo to video` → **LOW**, `demand_score=16`, `google_trends_ru=3`, `hh_vacancies=1`, `yandex_suggest=100`. [T2]
- `говорящее фото` → **LOW**, `demand_score=15`, `google_trends_ru=1`, `hh_vacancies=6`, `yandex_suggest=100`. [T2]

### Интерпретация
- Для QUICK-AI это выглядит как **реальный consumer pull**, а не B2B category creation: люди ищут конкретный эффект, а не категорию software. [T2]
- Высокий `yandex_suggest=100` по нескольким запросам и заметный Google Trends по `оживить фото` означают, что use case уже понятен без длинного обучения. [T2]
- Сам GetLivePhoto продаёт ценность максимально просто: Telegram, без регистрации, результат за 20–40 секунд, короткое MP4 для соцсетей и пересылки. Это усиливает конверсионность импульсного спроса. [T1]

## 2. Product proof и конкурентное поле

### GetLivePhoto
- Официальный сайт обещает генерацию за **20–40 секунд**, формат **MP4 480p**, сценарии по текстовой команде и работу прямо в Telegram. [T1]
- Публичные тарифы: **79 ₽** за 1 оживление, **139 ₽** за 2, **349 ₽** за 6, **549 ₽** за 10, **990 ₽** за 20. [T1]

### Смежные рыночные якоря
- Hedra публично пишет, что у сервиса **20+ млн пользователей**, а базовые creator-планы стартуют от **$15/мес**. Это другой формат продукта, но сильный сигнал, что photo/video-AI consumer creation глобально уже коммерциализирован. [T3]
- Vidnoz Gen monetizes image-to-video через credit model и платные пакеты. Это подтверждает, что пользователи готовы платить не только за full-suite video AI, но и за отдельные image-to-video сценарии. [T4]
- В Telegram-каталогах сама категория выглядит живой: карточка «Оживить фото» на alltelegram показывает **70 287 активных пользователей**, а findmini для схожего бота `@fotoshag_bot` показывает **12.8K monthly users**. Это вторичные источники, но они поддерживают тезис о наличии локального пользовательского спроса. [T5][T6]

## 3. WTP и готовность платить

### Прямые факты
1. GetLivePhoto уже продаёт первый use case за **79 ₽** и пакетный апселл до **990 ₽**. [T1]
2. В оффере value proposition завязан на эмоцию, скорость и простоту, то есть на классический impulse buy, а не на долгий evaluation cycle. [T1]
3. Глобальные и adjacent-игроки вроде Hedra и Vidnoz тоже монетизируют image/video generation по подписке или кредитам. [T3][T4]

### Вывод по WTP
- **WTP подтверждён**, но это low-ticket, high-volume consumer spend. [T1][T3][T4]
- Основной риск не в willingness to pay, а в том, хватит ли органического и repeat demand, чтобы выйти на нужную месячную прибыль. Это inference из публичной цены и типа продукта. [T1][T2]

## 4. TAM / SAM / SOM

### Подход
Для P3 беру прагматичный bottom-up, а не большой top-down entertainment TAM.

- Средний чек для грубой оценки беру **349 ₽** как базовый популярный consumer пакет. [T1]
- Адресуемый контур: RU Telegram users, которые регулярно покупают impulse AI/fun content, семейные memory-use cases, поздравления и social sharing. [T1][T2]

### Bottom-up ориентиры
- Если продукт делает **3 000 заказов в месяц** при среднем чеке **349 ₽**, это **1,05 млн ₽ выручки/мес**.
- Если делает **5 000 заказов в месяц**, это **1,75 млн ₽ выручки/мес**.
- Для consumer Telegram-бота это выглядит достижимым только при хорошем viral/referral/media channel, но не выглядит математически невозможным. [T1][T5][T6]

### Вывод по размеру возможности
Рынок не похож на большой защищённый SaaS, но как QUICK-AI impulse category он достаточно широк, чтобы собрать выручку выше 500k ₽/мес. Вопрос в качестве канала, repeat rate и refunds, а не в полном отсутствии спроса.

## 5. Profit Gate

Цель: понять, возможен ли путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Low-ticket organic
- 5 000 заказов/мес × **349 ₽** = **1,745 млн ₽ выручки/мес**. [T1]
- При gross margin около **65%** это даёт ~**1,13 млн ₽** gross profit.
- После фиксированных расходов на поддержку, бота, платежи и небольшой маркетинг **0,5 млн ₽ EBITDA** выглядит достижимой. [T1]
- **Вердикт:** PASS.

### Сценарий B. Paid acquisition heavy
- Те же 5 000 заказов/мес, но при заметной зависимости от платного Telegram/short-video трафика.
- Если blended CAC подбирается к **150–250 ₽** на заказ, низкий средний чек быстро убивает вклад в прибыль.
- **Вердикт:** FAIL.

### Сценарий C. Mixed funnel с апселлом
- Микс пакетов с effective ARPPU **450–550 ₽** плюс подарочные/holiday пики.
- Тогда порог по выручке и EBITDA проходится заметно легче уже на **3–4 тыс.** заказов/мес.
- **Вердикт:** CONDITIONAL PASS.

### Общий вывод по Profit Gate
**Profit Gate не провален на уровне demand-stage**, но он полностью зависит от канала дистрибуции. Если growth органический, реферальный или построен на дешёвом creator traffic, модель может работать. Если рост требует тяжёлого performance marketing, экономика становится хрупкой.

## 6. Ключевые риски
- Низкий чек и слабая защита от копирования. [T1][T4]
- Большая зависимость от distribution и креативного маркетинга, а не от уникальной технологии. [T1][T2]
- Возможная commoditization, если image-to-video становится стандартной функцией крупных consumer AI suites. [T3][T4]
- Высокий риск, что разовый emotional purchase не превращается в устойчивый repeat usage. Это пока inference, а не подтверждённый факт. [T1]

## 7. Решение для pipeline
**Кейс проходит P3 с пометкой PASS WITH RESERVATIONS.**

Почему не reject:
1. Есть реальный consumer intent по ключевым запросам в РФ. [T2]
2. Есть рабочая публичная монетизация и понятный impulse value prop. [T1]
3. Формально существует путь к EBITDA 500k+ ₽/мес, если distribution не слишком дорогой. [T1][T5][T6]

Что обязательно проверить дальше:
- CAC по Telegram и short-video каналам,
- долю repeat и gifting behavior,
- сезонность и праздничные пики,
- margin после inference cost и платежей,
- можно ли построить moat сильнее, чем просто «ещё один бот оживления фото».

## Источники
- [T1] GetLivePhoto, официальный сайт и тарифы: https://getlivebot.ru/
- [T2] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%B6%D0%B8%D0%B2%D0%B8%D1%82%D1%8C%20%D1%84%D0%BE%D1%82%D0%BE
- [T2] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%B6%D0%B8%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D1%84%D0%BE%D1%82%D0%BE
- [T2] Demand API: http://172.18.0.1:9001/multi-demand?keyword=photo%20to%20video
- [T2] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D1%8F%D1%89%D0%B5%D0%B5%20%D1%84%D0%BE%D1%82%D0%BE
- [T3] Hedra pricing: https://www.hedra.com/pricing
- [T4] Vidnoz Gen pricing: https://www.vidnoz.com/vidnoz-gen-pricing.html
- [T5] alltelegram, карточка «Оживить фото»: https://alltelegram.com/ru/app/ozhivit-foto
- [T6] findmini, `@fotoshag_bot`: https://www.findmini.app/fotoshag_bot/

Sources: T1=1, T2=4, T3=1, T4=1, T5=1, T6=1. Primary evidence basis: T1/T2.

> Market Pulse 2026-04-21: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, продуктовых страниц, внедренческих материалов и/или коммерческих сигналов, чем в прошлых срезах.

## Market Pulse
- Market Pulse 2026-04-22: растущий интерес.
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 24.04.2026: растущий интерес.

> Market Pulse 2026-04-25: растущий интерес. В свежей выдаче резко вырос поток публикаций и how-to материалов по AI-анимации и оживлению фото.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-10: наблюдается растущий интерес.

> Market Pulse 2026-05-11: зафиксирован рост интереса, по текущему веб-поиску и публикациям динамика выглядит растущей.

> Market Pulse 2026-05-11: растущий интерес.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.
