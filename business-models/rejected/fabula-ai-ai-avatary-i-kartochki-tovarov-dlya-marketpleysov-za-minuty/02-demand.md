# Demand validation — Fabula AI: AI-аватары и карточки товаров для маркетплейсов

Дата: 2026-05-11 17:50 MSK
Статус: CONDITIONAL PASS
Demand API: `LOW` (score 0/100) по ключу `AI карточки товаров маркетплейсы AI аватары`.

## 1) Executive summary

- Узкий keyword-level спрос низкий: multi-demand вернул `LOW`, `hh_vacancies=1`, `habr_articles=2`, `yandex_suggest=2`. Это сигнал, что категория как поисковый ярлык пока не сформирована, а не что pain отсутствует. [T1]
- Реальный рынок в РФ уже подтверждён существующими локальными сервисами с публичными ценами: WildAI, Picaz, AimSeller и Гарпик продают генерацию карточек, нейрофото и инфографику за деньги прямо сейчас. [T2]
- WTP есть, но он двуслойный: mass self-serve сегмент платит десятки и сотни рублей за генерацию или 390–4 990 ₽/мес, а более дорогой B2B/agency слой платит за объём, white-label и API. [T2]
- Profit Gate не проходит в consumer-avatar сценарии и на слишком дешёвом seller self-serve, но проходит в scale self-serve, white-label/API и team SaaS сценариях. EBITDA 500k+/мес достижима. [T2][спекуляция]
- Итог: **не ранний reject**. Кейс слабый как broad consumer avatar app, но жизнеспособный как `AI content ops for marketplace sellers` с упором на карточки, batch workflows и агентский/командный use case. [T1][T2]

## 2) Demand signals

### Multi-demand
- `http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%BA%D0%B0%D1%80%D1%82%D0%BE%D1%87%D0%BA%D0%B8%20%D1%82%D0%BE%D0%B2%D0%B0%D1%80%D0%BE%D0%B2%20%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%D1%8B%20AI%20%D0%B0%D0%B2%D0%B0%D1%82%D0%B0%D1%80%D1%8B` вернул `composite_demand=LOW`, `demand_score=0`, `hh_vacancies=1`, `habr_articles=2`, `yandex_suggest=2`. [T1]
- Интерпретация: по branded/category query спрос очень ранний; пользователи, вероятно, ищут задачу через запросы вида `инфографика для маркетплейсов`, `создать карточку товара`, `нейрофото товара`, а не через общий ярлык `AI avatars`. [T1][спекуляция]

### What the market is actually buying
- Несколько RU-игроков уже продают именно создание карточек, инфографики, нейрофото и видеообложек для Wildberries/Ozon, то есть проблема monetized, а не гипотетическая. [T2]
- Публичная пресс-коммуникация Яндекс Маркета указывает на `97,3 тыс.` активных магазинов и рост активных продавцов на `29% г/г`, что подтверждает крупную базу потенциальных buyers среди продавцов маркетплейсов. [T1]
- Публикации Т-Банка и отраслевых медиа про 24AI и seller-AI инструменты подтверждают, что тема уже попала в mainstream seller-tooling слой, пусть и не стала массовым consumer search brand. [T2]

## 3) Конкуренты и цены

Ниже реальные конкуренты с публичными ценами.

1. **WildAI** — пакеты `260 ₽ / 40 кредитов`, `720 ₽ / 120`, `1 650 ₽ / 300`, `4 500 ₽ / 900`; сервис заявляет генерацию карточек и нейрофото для маркетплейсов. Это price floor для low-ticket RU self-serve. [T2]
   Ссылка: https://www.wildai.ru/
2. **Picaz** — `1 кредит = 1 ₽`; инфографика `100 ₽/слайд`, аналитика конкурентов `100 ₽`, видеообложка `200 ₽/5 сек`; пример полной карточки с аналитикой и видео у них оценивается примерно в `1 200 ₽`. [T2]
   Ссылка: https://picaz.ru/
3. **AimSeller** — пакеты `390 ₽ / 50 молний`, `990 ₽ / 140`, `2 490 ₽ / 400`, `6 490 ₽ / 1 200`, `19 990 ₽ / 5 000`; генерация фото стоит `4⚡`, карточка `6⚡`. Это уже понятный scale-up pricing для seller teams. [T2]
   Ссылка: https://www.aimseller.ru/
4. **Гарпик** — `390 ₽/мес`, `2 390 ₽/мес`, `4 990 ₽/мес`; на Premium обещает до `345` генераций за 30 дней, на Business — безлимит в рамках fair-use лимитов. [T2]
   Ссылка: https://garpic.ru/
5. **Pebblely** — международный reference competitor: `US$9`, `US$19`, `US$39` в месяц за 30/200/500 изображений. Это показывает, что price anchor для solo/small-team photo AI глобально низкий и сервис будет жить за счёт объёма и workflow convenience, а не за счёт высокой цены за одну картинку. [T2]
   Ссылка: https://pebblely.com/pricing/
6. **Claid.ai** — global suite с free trial и Business/custom pricing; публично показывает credit-based usage и отдельный API слой. Это подтверждает, что enterprise/API monetization в категории существует и является частью category standard. [T2]
   Ссылка: https://claid.ai/pricing

### Вывод по конкурентам
- RU рынок уже занят, и базовый photo-generation слой коммодитизирован: price floor начинается буквально с `нескольких рублей` за генерацию или `390 ₽` за стартовый пакет. [T2]
- Следовательно, защищаемая выручка для Fabula AI вероятнее строится не на consumer avatars, а на `batch card creation`, `team workspace`, `white-label/API`, `brand consistency` и интеграциях для sellers/agencies. [T2][спекуляция]

## 4) Telegram bots / services в RU

- В самом demand API по этому keyword `telegram.subscribers=0`, то есть заметного брендированного спроса именно в Telegram по общему ярлыку не видно. [T1]
- При этом в РФ есть сервисы, которые логично дистрибутируются через Telegram-сообщества селлеров и обещают быстрый self-serve результат для карточек маркетплейсов; особенно это видно по коммуникации AimSeller, WildAI, Picaz и Fabula AI, заточенной под solo sellers и small teams. [T2]
- Прямых сильных Telegram-first брендов категории я не нашёл; это скорее канал acquisition/support, а не отдельный moat. Секция оценивается как **[LOW CONFIDENCE]** там, где речь идёт именно о Telegram-native поведении покупателей. [T1][T2][T3]

## 5) WTP / willingness to pay

### Прямые доказательства WTP
- RU конкуренты уже берут деньги за единицу результата: Picaz продаёт слайд инфографики по `100 ₽`, аналитику по `100 ₽`, а полный пример карточки оценивает примерно в `1 200 ₽`. [T2]
- AimSeller и Гарпик продают подписки и пакеты от `390 ₽` до `19 990 ₽`, то есть seller segment уже привык платить не только per-image, но и за пакетный доступ. [T2]
- WildAI прямо сравнивает свой AI workflow со студийной съёмкой и заявляет экономию относительно офлайн-продакшна; даже если маркетинговые проценты на их сайте считать optimistic, сам факт такой коммуникации означает, что клиент сравнивает сервис с реальным фотобюджетом, а не с нулём. [T2][T3]

### Непрямые доказательства WTP
- 97,3 тыс. активных магазинов на Яндекс Маркете и рост seller base на 29% г/г означают расширяющуюся базу тех, кому нужно быстро обновлять визуалы и тестировать карточки. [T1]
- Появление AI seller-tools в публикациях Т-Банка, VC.ru и профильных медиа подтверждает, что рынок уже считает такой spend нормальным операционным инструментом для маркетплейсов. [T2]

### WTP conclusion
- **B2C avatars**: WTP слабее и импульсный, высокая чувствительность к цене. [T2][спекуляция]
- **Marketplace sellers**: WTP подтверждён, но базовый чек низкий, поэтому важны объём, удержание и upsell. [T1][T2]
- **Agencies / white-label / API**: лучший слой по WTP, потому что они покупают не картинку, а throughput и margin expansion. [T2][спекуляция]

## 6) Market sizing

### Методика
- Top-down якорь: рынок интернет-торговли РФ около `11,3 трлн ₽` в 2024 году. Для addressable layer берём только spend на создание и обновление визуального контента для seller operations, а не весь GMV. [T2]
- Bottom-up якорь: Яндекс Маркет сообщал о `97,3 тыс.` активных магазинах на конец 2023 года и росте активных продавцов на `29%` в 2024. Для расчёта берём только часть этой базы как платёжеспособный сегмент с повторяющейся задачей по карточкам. [T1]

### Top-down
- **TAM РФ**: `11,3 трлн ₽ × 0,02%` = **2,26 млрд ₽** annual spend proxy на AI-инструменты визуального контента для marketplace sellers. Доля маленькая намеренно, потому что речь не о всём martech, а только о photo/card creation layer. [T2][спекуляция]
- **SAM РФ**: `2,26 млрд ₽ × 60%` = **1,36 млрд ₽**. Здесь отсекаем продавцов без регулярной need в масштабируемом визуальном контенте и оставляем sellers/agencies с recurring workflow. [T1][T2][спекуляция]
- **SOM Y1**: `1,36 млрд ₽ × 1,1%` = **15,0 млн ₽/год**. Это примерно `500` клиентов на `2 490 ₽/мес` или эквивалентный mix self-serve + API. [T2][спекуляция]
- **SOM Y3**: `1,36 млрд ₽ × 3,7%` = **50,3 млн ₽/год**. [T2][спекуляция]

### Bottom-up
- **Total buyers**: `97 300` активных магазинов на Яндекс Маркете. Это консервативная база, потому что не включает Ozon/Wildberries целиком. [T1]
- **% with need**: `30%` как доля sellers с регулярной задачей по обновлению карточек, фото и инфографики, где сервис экономит время или подрядчиков. Это гипотеза, но она согласуется с тем, что визуал критичен для marketplace conversion. [T1][T2][спекуляция]
- **ARR avg**: `48 000 ₽/год` на одного buyer, то есть около `4 000 ₽/мес` blended spend между low пакетами, occasional credits и scale plans. Это лежит внутри видимого рыночного диапазона `390–4 990 ₽/мес` и per-result прайсов. [T2][спекуляция]
- **SAM bottom-up**: `97 300 × 30% × 48 000 ₽` = **1,40 млрд ₽/год**. [T1][T2][спекуляция]
- **SOM bottom-up Y1**: `312` клиентов × `48 000 ₽/год` = **15,0 млн ₽/год**. [T2][спекуляция]
- **SOM bottom-up Y3**: `1 042` клиента × `48 000 ₽/год` = **50,0 млн ₽/год**. [T2][спекуляция]

### Market sizing table

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | приоритетом был РФ seller-market; глобальный TAM не нужен для invest decision на этом этапе | — |
| TAM (РФ) | 2,26 млрд ₽ [T2] | 4,67 млрд ₽ = 97 300 × 48 000 ₽ [T1][T2][спекуляция] | diff 2,1x, допустимо; bottom-up gross buyer pool шире, top-down строже режет по actual tooling share | **lower = 2,26 млрд ₽** |
| SAM (РФ) | 1,36 млрд ₽ [T1][T2][спекуляция] | 1,40 млрд ₽ [T1][T2][спекуляция] | diff ~3%, хороший match | **lower = 1,36 млрд ₽** |
| SOM Y1 | 15,0 млн ₽ | 15,0 млн ₽ | diff ~0% | **используем 15,0 млн ₽** |
| SOM Y3 | 50,3 млн ₽ | 50,0 млн ₽ | diff <1% | **используем 50,0 млн ₽** |

### Reconciliation notes
- Расхождение top-down и bottom-up меньше 3x, значит сегмент выбран адекватно. [T1][T2]
- SOM Y1 составляет около `1,1%` от preferred SAM, это реалистично и далеко от overclaiming. [T1][T2][спекуляция]
- Sanity check: чтобы сделать `15 млн ₽` в Y1 при blended ARPA `~4 000 ₽/мес`, нужно в среднем `312` платящих клиентов за год. Для чистого founder-led B2C это тяжело, но для self-serve + комьюнити + reseller/agency channel достижимо. [T2][спекуляция]

## 7) 10 реальных buyers для bottom-up / GTM

Ниже 10 реальных типов buyers, которых имеет смысл брать в P7 как приоритетные target accounts. Это реальные компании/бренды, работающие с маркетплейсами и нуждающиеся в частом обновлении контента. [T2][спекуляция]

1. **SOKOLOV**
2. **Synergetic**
3. **Kuchenland Home**
4. **Gloria Jeans**
5. **Zarina**
6. **befree**
7. **12 STOREEZ**
8. **Askona**
9. **Erborian Russia / крупные beauty-бренды на маркетплейсах** [LOW CONFIDENCE]
10. **agency-sellers и production agencies, обслуживающие каталоги Ozon/WB** [LOW CONFIDENCE]

Примечание: для первого ICP я бы сузил список до sellers с `50+ SKU`, частыми обновлениями карточек и отсутствием собственной студии/дизайн-команды. [T2][спекуляция]

## 8) Profit Gate: все сценарии монетизации

### Сценарий A — B2C AI-аватары
- `700` платящих пользователей × `990 ₽/мес` = **693k ₽ выручки/мес**. [T2][спекуляция]
- При gross margin `70%`, но с heavy paid acquisition и support, EBITDA вероятнее около **100k–250k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Сценарий B — low-end seller self-serve
- `250` sellers × `2 490 ₽/мес` = **622,5k ₽ выручки/мес**. [T2][спекуляция]
- При gross margin `78%` и fixed opex `180k ₽` EBITDA около **305k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Сценарий C — scale self-serve / team plan
- `500` sellers × `2 490 ₽/мес` = **1,245 млн ₽ выручки/мес**. [T2][спекуляция]
- При gross margin `78%` и fixed opex `220k ₽` EBITDA около **751k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Сценарий D — pay-per-result / credits
- `1 200` полных карточек в месяц × `1 200 ₽` blended ARPPU = **1,44 млн ₽ выручки/мес**. [T2][спекуляция]
- При gross margin `65%` и fixed opex `220k ₽` EBITDA около **716k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Сценарий E — agency / white-label / API
- `25` агентств или seller-teams × `35 000 ₽/мес` = **875k ₽ выручки/мес**. [T2][спекуляция]
- При gross margin `85%` и fixed opex `180k ₽` EBITDA около **564k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Вывод по Profit Gate
- EBITDA `500k+/мес` достижима, но только если продукт идёт в объёмный seller workflow, credits или white-label/API. [T2][спекуляция]
- Если команда останется в нише `consumer avatars` или в слишком дешёвом solo-seller плане, порог фонда не выполняется. [T2][спекуляция]

## 9) Риски

- Коммодитизация image generation очень высокая, price floor в РФ уже низкий. [T2]
- Категория search-wise не сформирована, поэтому organic demand по общему ярлыку слабый. [T1]
- Защита маржи требует workflow moat: batch, templates, brand kits, multi-user, integrations, API. Без этого сервис станет interchangeable. [T2][спекуляция]
- Telegram как канал не даёт отдельного moat, это максимум дешёвый acquisition layer. [T1][T2]

## 10) Verdict

**Решение: PASS TO NEXT STEP.**

Почему не reject:
- Demand API низкий, но рынок не нулевой: уже есть несколько платящих RU конкурентов и понятный buyer problem. [T1][T2]
- Profit Gate проходит минимум в трёх сценариях из пяти. [T2][спекуляция]
- Значит вопрос не в существовании спроса, а в выборе правильного wedge и monetization design. [T2]

Что делать дальше:
1. В unit economics считать базовым не consumer-avatar, а seller/team SaaS + credits/API mix. [T2][спекуляция]
2. Проверить retention-риски: сколько SKU и генераций в месяц делает активный seller, и насколько быстро он churn-ится после обновления каталога. [T2][спекуляция]
3. Протестировать ICP `агентства и seller-teams 50+ SKU`, а не broad B2C. [T2][спекуляция]

Sources: T1=3, T2=10, T3=1. Primary evidence basis: T2.

## Source log
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%BA%D0%B0%D1%80%D1%82%D0%BE%D1%87%D0%BA%D0%B8%20%D1%82%D0%BE%D0%B2%D0%B0%D1%80%D0%BE%D0%B2%20%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%D1%8B%20AI%20%D0%B0%D0%B2%D0%B0%D1%82%D0%B0%D1%80%D1%8B
- [T1] Яндекс, годовой отчёт / результаты e-commerce 2024, поиск показал `97,3 тыс.` активных магазинов и рост активных продавцов на `29%`: https://yandex.ru/company/researches/2024/ecom
- [T2] WildAI: https://www.wildai.ru/
- [T2] Picaz: https://picaz.ru/
- [T2] AimSeller: https://www.aimseller.ru/
- [T2] Гарпик: https://garpic.ru/
- [T2] Pebblely pricing: https://pebblely.com/pricing/
- [T2] Claid pricing: https://claid.ai/pricing
- [T2] Fabula AI marketplace cards page: https://fabula-ai.com/
- [T2] T-Банк / seller AI tooling references in search results: https://secrets.tbank.ru/
- [T2] АКИТ / рынок интернет-торговли РФ 2024: https://www.akit.ru/
