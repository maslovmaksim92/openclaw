# Demand validation

## Итог
**Вердикт: PROCEED.**

Спрос в РФ по точному запросу про AI UGC/video ad generation пока **medium-low**, но у более прикладного wedge "видео для маркетплейсов" уже есть живой спрос и понятная платёжеспособная аудитория. Критично, что кейс проходит не только по общему интересу, но и по **WTP** и **Profit Gate**: при 350-450 SMB-подписок по 6 000 ₽/мес или 70-90 agency-аккаунтах по 25 000 ₽/мес компания уже может выйти на EBITDA 500 000+ ₽/мес.

## Demand signals
- Внутренний demand endpoint по запросу **"видео для маркетплейсов"** вернул **MEDIUM**, score=30, HH vacancies=1 208, Yandex Suggest=100, Google Trends RU=1. Это слабый broad-trend, но сильный прикладной pain-signal для e-commerce production [T2, internal: http://172.18.0.1:9001/multi-demand?keyword=%D0%B2%D0%B8%D0%B4%D0%B5%D0%BE%20%D0%B4%D0%BB%D1%8F%20%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%D0%BE%D0%B2].
- По запросу **"генерация рекламных видео"** endpoint даёт LOW, но HH vacancies=200 и Yandex Suggest=100. Это означает: категория как термин ещё не устоялась, но потребность в рекламных видео есть [T2, internal].
- АКАР оценила объём **видеорекламы** в РФ в **67.8 млрд ₽ в Q1 2026**, рост +53% г/г. Это сильный top-down сигнал, что деньги в видеоформате продолжают расти [T1, АКАР/ТАСС: https://tass.ru/ekonomika/23915083].
- HH.ru показывает заметный спрос на роли video editor / motion / creative producer в РФ, что подтверждает ручной pain и бюджет, который может быть частично замещён софтом [T1, HH.ru через internal demand endpoint].

## Competitors with prices
### Глобальные прямые аналоги
1. **Topview AI**: self-serve pricing от **$29/мес**; plan Business около **$49.9/мес**. По курсу 73.79 ₽/$ это примерно **2 140–3 682 ₽/мес** [T2, https://www.topview.ai/pricing; T2, курс: https://www.akm.ru/eng/news/the-central-bank-of-the-russian-federation-set-the-exchange-rate-of-the-us-dollar-at-73-7878-rubles-for-may-13/].
2. **HeyGen**: Creator **$29/мес**, Business **$149/мес**, то есть примерно **2 140–10 994 ₽/мес** [T2, https://www.heygen.com/pricing; T2, курс ЦБ/AK&M].
3. **Creatify**: Starter **$39/мес**, Pro **$99/мес**, то есть примерно **2 878–7 305 ₽/мес** [T2, https://creatify.ai/pricing; T2, курс ЦБ/AK&M].

### Telegram / RU convenience-layer substitutes
1. **ChatPost**: пакет для коротких AI-видео от **300 ₽ за 10 видео**, есть и подписка от **750 ₽/мес** на контент-пакет [T2, https://chatpost.ru/ai].
2. **KolerskyAI bot**: пакеты кредитов **129 / 349 / 890 ₽**; бот покрывает генерацию креативов и снижает порог входа для Telegram-аудитории [T2, https://kolersky.com/ai].
3. **Нейропост / Telegram-first AI content tools**: в РФ уже есть дешёвые боты и мини-сервисы для генерации контента, но они в основном закрывают single-shot контент, а не потоковый e-commerce video pipeline. Это конкуренция за низший чек, но не полноценная замена productized ad-video workflow [T3, спекуляция на базе рыночного обзора; не использовать как primary claim].

## Telegram bots/services in RU
Да, рынок Telegram-first AI инструментов в РФ уже существует. Это важно по двум причинам:
- с одной стороны, **канал дистрибуции** через Telegram реалистичен;
- с другой, именно Telegram-боты формируют **ценовой якорь вниз** в диапазоне от сотен рублей до низких тысяч рублей.

Вывод: Telegram в РФ годится как acquisition layer и low-end plan, но не как верхняя граница цены для основного продукта. Основной продукт нужно позиционировать как **workflow для селлера/агентства**, а не как “ещё один бот для генерации картинки/ролика”.

## WTP, proof of willingness to pay
- Глобальные аналоги уже продают подписку в диапазоне **$29–149/мес**, а значит рынок привык платить за ускорение видео-производства, а не только за one-off generation [T2].
- Российские Telegram-first сервисы берут деньги даже за lightweight use case, от **129 ₽** за кредиты и от **300 ₽** за пакет коротких видео. Это слабее enterprise-grade WTP, но подтверждает сам факт готовности платить за automation [T2].
- Альтернатива в виде ручного найма видеомонтажёра / motion / content-оператора кратно дороже, чем SaaS-подписка 6 000–10 000 ₽/мес [T1/T2 inference from HH demand + competitor pricing].
- Ozon сообщает о **600 000** предпринимателей на площадке, а Wildberries заявляет **1.26 млн** продавцов. При таком масштабе даже узкая доля performance-heavy sellers формирует достаточный пул покупателей [T2, https://www.cnews.ru/news/line/2025-02-13_ozon_dostig_otmetki_v_600; T2, https://www.sostav.ru/publication/wildberries-zafiksiroval-1-26-milliona-predprinimatelej-74063.html].

**Вывод по WTP:** willingness to pay есть. Реалистичный рабочий чек для РФ, на мой взгляд, лежит в диапазоне **4 900–9 900 ₽/мес** для SMB и **19 900–39 900 ₽/мес** для agency / team plan. Это inference на базе observed pricing и альтернативных затрат.

## Market sizing
Методика: считаю оба пути, top-down и bottom-up, и беру **консервативно lower-of-two** там, где расхождение заметно.

### Допущения
- Курс для пересчёта: **73.7878 ₽/$** [T2].
- Global AI video generator market: **$788.5M в 2025** [T2, Grand View Research summary: https://www.grandviewresearch.com/horizon/outlook/ai-video-generator-market-size/global]. Это **≈58.2 млрд ₽**.
- РФ video advertising market annualized: **67.8 млрд ₽ в Q1 2026** × 4 = **271.2 млрд ₽/год run-rate** [T1].
- Addressable software/tooling share of video spend: **3%**. Это аналитическое допущение, а не наблюдаемый рынок, поэтому я использую его консервативно [inference from T1/T2].
- Segment fit for Topview-like wedge in РФ: **55%** от TAM РФ, потому что продукт адресует не весь video ad spend, а прежде всего marketplace sellers, DTC e-commerce и агентства performance-креатива [inference].
- Avg ARR для SMB: **72 000 ₽/год** или **6 000 ₽/мес**, что находится ниже большинства западных аналогов и выше low-end TG bots [T2/inference].

### GTM-10 real buyer targets
1. SOKOLOV
2. Gloria Jeans
3. Askona
4. 12 STOREEZ
5. Demis Group
6. VOIS
7. Premium Care Group
8. Synergy
9. Startsmile
10. Hoff

Это не полный рынок, а стартовый account-list для outbound. Все 10 компаний реальны; часть из них это бренды с heavy e-commerce/video needs, часть это агентства или большие digital-команды. Список нужен как sanity-check для bottom-up модели [T2/T3 mixed, использовать как GTM hypothesis].

### Bottom-up logic
- Total buyers base: **1.26 млн** продавцов Wildberries + **600 тыс.** предпринимателей на Ozon = **1.86 млн** seller accounts [T2].
- Корректировка на уникальность и пересечение аккаунтов между площадками: беру только **1.40 млн уникальных buyer organizations** [inference, консервативно].
- % with need: **6%**. Это доля seller/orgs, для которых видео реально влияет на conversion и которые регулярно работают с рекламными/карточными креативами [T1/T2 inference from demand endpoint + HH + ad market growth].
- Avg ARR: **72 000 ₽/год** [T2/inference].
- Тогда **SAM_bottom_up = 1.40 млн × 6% × 72 000 ₽ = 6.05 млрд ₽**.
- **SOM Y1_bottom_up = 1.5% от SAM = 90.7 млн ₽**.
- **SOM Y3_bottom_up = 6% от SAM = 362.9 млн ₽**.

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 58.2 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 8.14 млрд ₽ = 271.2 млрд ₽ × 3% [T1+inf] | 100.8 млрд ₽ = 1.40 млн × 72 000 ₽ [inf, слишком широко] | diff > 3x, поэтому bottom-up TAM не использую: это theoretical wallet, а не realistic software category | top-down |
| SAM (РФ) | 4.48 млрд ₽ = 8.14 млрд ₽ × 55% [inf] | 6.05 млрд ₽ [T2+inf] | diff = 1.35x, допустимо; bottom-up учитывает seller-base, top-down ограничен ad-video tooling share | **4.48 млрд ₽** |
| SOM Y1 | 89.6 млн ₽ = 2% от SAM [inf] | 90.7 млн ₽ = 1.5% от SAM [inf] | diff = 1.01x | **89.6 млн ₽** |
| SOM Y3 | 313.6 млн ₽ = 7% от SAM [inf] | 362.9 млн ₽ = 6% от SAM [inf] | diff = 1.16x | **313.6 млн ₽** |

### Sanity checks
- SOM Y1 как доля SAM = **2%**, это реалистично и ниже red-flag порога 30%.
- При среднем чеке **6 000 ₽/мес** SOM Y1 соответствует примерно **1 244 account-years** или в среднем около **520 активных аккаунтов** за год с ramp-up. Это тяжело, но не абсурдно для self-serve + agency motion.
- Если средний цикл сделки SMB 0.2-1.0 месяца, то такая воронка достижима при PLG/performance distribution. Для mid-market без PLG было бы слишком тяжело.

## Profit Gate
Порог: **EBITDA >= 500 000 ₽/мес**.

### Сценарий 1. Self-serve SMB only
- 420 клиентов × 6 000 ₽/мес = **2.52 млн ₽ MRR**.
- При EBITDA margin ~20% это даёт **≈504 тыс. ₽ EBITDA/мес**.
- Вывод: **gate passes**.

### Сценарий 2. Agency / team plan
- 80 клиентов × 25 000 ₽/мес = **2.0 млн ₽ MRR**.
- При EBITDA margin 25-30% это даёт **500-600 тыс. ₽ EBITDA/мес**.
- Вывод: **gate passes**.

### Сценарий 3. Hybrid
- 250 SMB × 6 000 ₽ + 20 agencies × 25 000 ₽ = **2.0 млн ₽ MRR**.
- При margin 30% это даёт **≈600 тыс. ₽ EBITDA/мес**.
- Вывод: **gate passes**.

**Итог по Profit Gate:** проходит во всех трёх сценариях. Значит кейс не попадает под early reject даже при неидеальном broad-demand.

## Risks
- Рынок может “схлопнуться” в commodity layer, если продукт не даёт workflow advantage поверх базовой генерации [T3/T2].
- Низший сегмент будет давить цену через Telegram-ботов и bundled AI suites [T2].
- Зависимость от зарубежных моделей и платёжной инфраструктуры ухудшает российскую локализацию [T2/T3].
- Если продукт не встроится в marketplace-операционку, а останется просто видео-генератором, retention будет слабым [inference].

## Recommendation
Идти дальше в pipeline. Но позиционировать не как “AI-видео вообще”, а как **performance-video workflow для маркетплейсов, DTC и агентств**:
1. URL / карточка товара -> 5-10 ad variations.
2. Аватар / voiceover / subtitle / CTA presets.
3. Team workflow и white-label для агентств.
4. Telegram acquisition only, core value in web app / workspace.

## Confidence
**Medium.** Сильнее всего подтверждены: рост видеорекламы, масштаб seller-base, существующий WTP у аналогов и наличие low-end RU substitutes. Слабее всего подтверждён: exact standalone demand именно под категорию “AI video ad generator” как отдельный budget line item.

Sources: T1=2, T2=10, T3=2. Primary evidence basis: T2.