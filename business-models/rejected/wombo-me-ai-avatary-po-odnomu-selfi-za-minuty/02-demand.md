# Demand validation

## Итог
**Решение: EARLY REJECT.** Сигнал спроса по РФ низкий, а ни один реалистичный сценарий монетизации не показывает достижимую EBITDA ≥ 500 000 ₽/мес без перехода в совсем другой продуктовый сегмент. [T1][T2]

## Demand snapshot
- Composite demand API по ключу `AI аватары по селфи` вернул **LOW / score 0**: Google Trends RU = 0, HH = 0 вакансий, Yandex Suggest = 2, Habr = 2. Это прямой индикатор слабого локального pull, а не только слабого SEO. [T1]
- В РФ есть локальные попытки монетизации через Telegram и web, но они выглядят как нишевые entertainment-инструменты, а не как категория с устойчивым массовым spend. Например, NeuroAvatar заявляет 10 000+ активных пользователей и 50 000+ сгенерированных изображений, что подтверждает наличие интереса, но не масштабного рынка. [T2]
- WTP существует, потому что пользователи реально платят за пакетную генерацию и подписки, но evidence ближе к impulse purchase, чем к регулярной незаменимой боли. [T2]

## Конкуренты и цены
| Конкурент | Формат | Цена | Что это доказывает |
|---|---|---:|---|
| NeuroAvatar | RU web/Telegram | 149 ₽ за 10 генераций, 499 ₽ за 25, 949 ₽ за 50 | В РФ есть транзакционный WTP на дешёвые credit-паки. [T2] |
| CheeseAI | RU Telegram/web | 99 ₽ за 10 генераций, 199 ₽ за 25, 349 ₽ за 50 | Порог покупки в РФ очень низкий, рынок приучен к микрочеку. [T2] |
| Aragon.ai | Global web | $29 за Starter, $49 за Basic, $69 за Premium | На глобальном рынке headshot/avatar-use case monetizable, но цена сильно выше RU mass-market tolerance. [T2] |
| Photoleap | Global mobile app | free trial + paid avatar bundles/upsell, точный прайс зависит от стора | Есть рабочая consumer mechanics через bundle/upsell, но pricing power прячется за app-store funnel. [T2] |

## Telegram и RU services
- RU-рынок не пустой: есть NeuroAvatar и CheeseAI как локальные сервисы; это подтверждает, что канал Telegram подходит для доставки value proposition. [T2]
- Но demand API не показывает заметного Telegram-scale спроса и не фиксирует сильного external pull. Подтверждение слабое, не fund-scale. [T1]
- Вывод: Telegram годится как дешёвый канал теста, но не как доказательство большого standalone-рынка. [T1][T2]

## WTP / willingness to pay
- **Доказано:** пользователи платят 99–949 ₽ за credit packs в RU и $29–69 за headshot/avatar packs globally. Это прямое подтверждение willingness to pay. [T2]
- **Не доказано:** высокий repeat usage. В брифе repeat рассматривается как гипотеза, а demand API не даёт признаков регулярного поиска или B2B найма под эту категорию. [T1]
- **Интерпретация:** платить готовы за novelty, профили, дейтинг, мемы и разовые фотосессии, но пока нет сильного evidence, что это превращается в стабильный monthly habit в РФ. [T1][T2]

## Market sizing [LOW CONFIDENCE]
Ниже расчёт сделан в узком сегменте **quick AI avatars / one-selfie avatar packs** для РФ. Верхняя граница top-down опирается на внешние market-report estimates по AI avatar niche, поэтому секция помечена как low confidence. [T2][T3]

### Допущения
- Курс для пересчёта: 1 USD = 79,5527 ₽ по ЦБ РФ на 25 апреля 2026. [T1]
- В РФ 136 млн internet users и 106 млн social media identities, значит Россия остаётся крупным consumer visual market. [T2]
- Но локальный intent низкий: demand API LOW, HH = 0. Поэтому для РФ беру консервативный lower-bound при reconciliation. [T1]

### GTM-10 targets для bottom-up / white-label adjacent
1. VK [T2]
2. Mamba [T2]
3. Twinby [T2]
4. TenChat [T2]
5. hh.ru [T1/T2]
6. Авито Работа [T2]
7. Skillbox [T2]
8. Skyeng [T2]
9. Нетология [T2]
10. SETTERS [T2]

### Таблица market sizing
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 63 642 160 000 ₽ (≈ $800M) [T3] | — | — | top-down |
| TAM (РФ) | 1 164 651 528 ₽ [T2][T3] | 968 760 000 ₽ [T2][T3] | diff=20%, обе оценки вокруг ~1,0–1,2 млрд ₽; беру lower bound из-за слабого intent | **968 760 000 ₽** |
| SAM (РФ) | 174 697 729 ₽ [T1][T2][T3] | 140 400 000 ₽ [T2][T3] | diff=24%, узкий сегмент quick-avatar / prosumer / white-label-adjacent | **140 400 000 ₽** |
| SOM Y1 | 3 493 955 ₽ | 2 808 000 ₽ | diff=24% | **2 808 000 ₽** |
| SOM Y3 | 13 975 818 ₽ | 11 232 000 ₽ | diff=24% | **11 232 000 ₽** |

### Как считалось
**Top-down:**
- Global TAM = $800M niche AI avatar market estimate × 79,5527 ₽ = 63,64 млрд ₽. [T1][T3]
- Russia share = 106 млн social media identities РФ / ~5,79 млрд global social identities ≈ 1,83%. [T2]
- TAM РФ = 63,64 млрд ₽ × 1,83% = 1,16 млрд ₽. [T2][T3]
- SAM РФ = TAM РФ × 15% segment fit для narrow quick-avatar use case = 174,7 млн ₽. Сегмент fit консервативный из-за LOW demand. [T1][T2][спекуляция]
- SOM Y1 = 2% SAM, SOM Y3 = 8% SAM. [спекуляция]

**Bottom-up:**
- Total buyers = 65 000 RU digital-native SMB / creator / HR / edu / dating accounts, которые теоретически могут купить avatar packs или white-label embedding. База выведена из ~1,3 млн новых компаний и ИП в РФ за год, из которых беру 5% как digital-facing visual-first cohort. [T2][спекуляция]
- % with need = 45%: сегменты, где profile imagery, promo creatives и быстрые аватары реально имеют utility. [T2][T3][спекуляция]
- ARR avg = 4 800 ₽/год, что соответствует примерно 1-2 микропокупкам в квартал или одному малому пакету в месяц. Это согласуется с RU пакетами 99–499 ₽. [T2]
- SAM_bottom_up = 65 000 × 45% × 4 800 ₽ = 140,4 млн ₽.
- SOM_bottom_up: Y1 = 2%, Y3 = 8%. Это реалистично и ниже 10%/30% red-flag thresholds.

## Profit Gate: проверка всех сценариев
### 1) B2C one-off packs
- Реалистичный сценарий: 1 500 платящих в месяц × 199 ₽ средний чек = 298 500 ₽ выручки/мес. [T2]
- При gross margin 75% остаётся ~224 000 ₽, но performance CAC даже на дешёвом Telegram/VK трафике легко съест 150–300 ₽ на покупателя. EBITDA уходит в ноль или минус. [T2][спекуляция]
- **Вердикт:** FAIL. EBITDA 500k/mo не просматривается.

### 2) B2C subscription
- Даже 1 000 активных подписчиков × 299 ₽ = 299 000 ₽ MRR. Для 500k EBITDA понадобился бы масштаб существенно выше, а evidence на low churn и repeat usage нет. [T1][T2]
- **Вердикт:** FAIL.

### 3) Telegram bot credits
- 3 000 кредитных покупок × 99 ₽ = 297 000 ₽ GMV/мес. С учётом оплаты моделей, саппорта, комиссий и повторного привлечения EBITDA < 500k. [T2][спекуляция]
- **Вердикт:** FAIL.

### 4) B2B-lite / white-label
- Даже 5 клиентов × 60 000 ₽ MRR = 300 000 ₽ выручки/мес. Для EBITDA 500k нужно скорее 10 клиентов по 100 000 ₽+ или один более широкий platform deal. [спекуляция]
- Но прямых сигналов такого спроса нет: HH = 0 по категории, поисковый спрос низкий, локальный рынок воспринимает продукт как entertainment/creative extra, а не must-have workflow. [T1]
- **Вердикт:** FAIL.

## Почему reject сейчас
1. **Demand LOW по прямому локальному сигналу.** [T1]
2. **WTP есть, но low-ticket и novelty-driven.** [T2]
3. **Ни один monetization path не приводит к достижимой EBITDA ≥ 500 000 ₽/мес на наблюдаемом спросе.** [T1][T2]
4. Чтобы кейс заработал, его пришлось бы перепозиционировать в другой рынок: AI headshots for recruiting, corporate ID, dating-photo optimization или полноценный photo-workflow tool. Это уже другой wedge. [T1][T2]

## Verdict
**REJECTED at Demand Validation.**

## Sources
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%B0%D0%B2%D0%B0%D1%82%D0%B0%D1%80%D1%8B%20%D0%BF%D0%BE%20%D1%81%D0%B5%D0%BB%D1%84%D0%B8
- [T1] ЦБ РФ, курс USD/RUB на 25.04.2026: https://www.cbr.ru/currency_base/daily/
- [T2] DataReportal Russia 2026: https://datareportal.com/reports/digital-2026-russian-federation
- [T2] NeuroAvatar pricing / traction: https://neuroavatar.ru/
- [T2] CheeseAI pricing: https://cheese-ai.ru/
- [T2] Aragon.ai pricing: https://www.aragon.ai/pricing
- [T2] Photoleap AI Avatar page: https://www.photoleapapp.com/features/ai-avatar-generator/
- [T2] Rusprofile / регистрационная активность бизнеса (через деловые публикации с цифрами Rusprofile) [использовано как supporting estimate]
- [T3] Market report / niche AI avatar estimate (supporting only): https://www.globenewswire.com/

Sources: T1=2, T2=7, T3=1. Primary evidence basis: T1.
