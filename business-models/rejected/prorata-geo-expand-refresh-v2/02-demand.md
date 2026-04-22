---
stage: demand-validation
case: prorata-geo-expand-refresh-v2
date: 2026-04-22
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: REJECTED
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
ProRata, AI-native платформа лицензирования контента, атрибуции и revenue share для издателей и создателей контента. [T2]

## Итог
**Статус: REJECTED на этапе Demand Validation.**

- Прямой спрос в РФ по категории стабильно **LOW**: mandatory endpoint по запросам `AI content licensing attribution revenue share`, `лицензирование контента для ИИ`, `атрибуция контента ИИ`, `монетизация контента для AI`, `AI лицензирование для издателей` везде вернул **LOW**, обычно с `demand_score=0`, максимум `3`, `hh=0-22`, `telegram_subscribers=0`, `yandex_suggest=2`. Это означает, что локальная категория пока не сформирована как отдельная закупаемая линия. [T2]
- Глобально category proof есть: ProRata заявляет **1000+** партнёров и **50% revenue share** контент-партнёрам. Но это подтверждает global experimentation, а не готовый платящий рынок в РФ. [T2]
- В России есть adjacent monetization в Telegram и creator economy, но это другой бюджет: авторы уже платят/терпят комиссии за paywall и подписки, а не за AI licensing / attribution infrastructure. [T2]
- Profit Gate не проходит в правдоподобных локальных сценариях: self-serve, mid-market publisher SaaS, enterprise media network и hybrid agency-wrapper. Чтобы выйти на **EBITDA >= 500 тыс. ₽/мес**, нужно слишком много клиентов для слишком сырой категории. [T2][inference]

## 1. Demand signals

### Mandatory endpoint
- `AI content licensing attribution revenue share` → **LOW**, `demand_score=0`, `hh=0`, `telegram=0`, `yandex_suggest=2`. [T2: internal demand endpoint]
- `лицензирование контента для ИИ` → **LOW**, `demand_score=0`, `hh=2`, `telegram=0`, `yandex_suggest=2`. [T2: internal demand endpoint]
- `атрибуция контента ИИ` → **LOW**, `demand_score=0`, `hh=4`, `telegram=0`, `yandex_suggest=2`. [T2: internal demand endpoint]
- `монетизация контента для AI` → **LOW**, `demand_score=3`, `hh=22`, `telegram=0`, `yandex_suggest=2`. [T2: internal demand endpoint]
- `AI лицензирование для издателей` → **LOW**, `demand_score=0`, `hh=0`, `telegram=0`, `yandex_suggest=2`. [T2: internal demand endpoint]

### Интерпретация
- Для РФ это пока не category-led спрос. Даже более «мягкий» запрос про монетизацию контента для AI даёт только слабый hiring proxy, а не признак зрелого софта-рынка. [T2]
- Следовательно, ProRata в РФ пришлось бы продавать не существующую категорию, а объяснять её с нуля. Это повышает CAC, удлиняет цикл сделки и сужает TAM до very-early-adopter сегмента. [T2][inference]

## 2. Что подтверждено глобально, но не локально
- На официальном сайте ProRata пишет, что у неё **1000+ publications and content creators** в партнёрской сети и что она делится с партнёрами **50% of revenues**. Это сильный signal category formation на глобальном рынке. [T2: https://prorata.ai/]
- Axios в январе 2025 писал, что у ProRata было более **400** публикаций в 50/50 revenue-share модели; позже сама компания сообщала уже о **500+** публикациях, а на текущем сайте, доступном 22 апреля 2026, фигурирует **1000+**. Это показывает рост партнёрской базы, но всё ещё не даёт evidence по российским сделкам. [T2: https://www.axios.com/2025/01/24/prorata-ai-plans-pay-creators-shoplifting-content ; https://prorata.ai/]
- Вывод: global proof есть, local proof для РФ нет. [T2]

## 3. Реальные конкуренты / substitute stack с ценами

Ниже не только прямые AI-licensing игроки, но и ближайшие monetization substitutes, за которые publisher/creator уже реально платит. Это важно, потому что в РФ именно substitutes задают реальную ценовую вилку. [T2]

1. **Supertab Connect** — AI/web crawler licensing infrastructure, стартует от **$249/мес**, то есть около **18,6 тыс. ₽/мес** по курсу ЦБ РФ на 22.04.2026 (**74,5897 ₽ за $1**). [T1/T2: https://www.supertab.co/pricing ; https://www.cbr.ru/currency_base/daily/?UniDbQuery.Posted=True&UniDbQuery.To=22.04.2026]
2. **TollBit** — marketplace/rail для on-demand licensing; в документации показаны rate examples **$0.005** за partial-use и **$0.01** за full-use на один URL, то есть примерно **0,37 ₽** и **0,75 ₽** за использование страницы. Это не fixed SaaS fee, а usage-based benchmark. [T2/T1 FX: https://docs.tollbit.com/rates/ ; https://www.cbr.ru/currency_base/daily/?UniDbQuery.Posted=True&UniDbQuery.To=22.04.2026]
3. **ScalePost** — AI attribution / visibility analytics для publishers и brands, Basic **$49/мес**, то есть около **3,7 тыс. ₽/мес**. [T2/T1 FX: https://www.scalepost.ai/pricing ; https://www.cbr.ru/currency_base/daily/?UniDbQuery.Posted=True&UniDbQuery.To=22.04.2026]
4. **PaywallProject** — substitute для publisher monetization, Reporter **$299/мес**, Editor **$998/мес**, Enterprise **$1499/мес**, или примерно **22,3 тыс. / 74,4 тыс. / 111,8 тыс. ₽/мес**. [T2/T1 FX: https://www.paywallproject.com/pricing/ ; https://www.cbr.ru/currency_base/daily/?UniDbQuery.Posted=True&UniDbQuery.To=22.04.2026]
5. **Memberful** — membership/paywall substitute, Standard **$49/мес + 4.9% transaction fee**, около **3,7 тыс. ₽/мес** плюс комиссия. [T2/T1 FX: https://memberful.com/pricing/ ; https://www.cbr.ru/currency_base/daily/?UniDbQuery.Posted=True&UniDbQuery.To=22.04.2026]

### Что это значит
- Прямые AI-licensing rails на публичном рынке стоят **от ~3,7 тыс. ₽ до ~18,6 тыс. ₽ в месяц** либо тарифицируются по usage. [T2]
- Publisher monetization substitutes стоят **~22-112 тыс. ₽/мес** и решают более понятную боль, чем AI attribution. [T2]
- Значит в РФ ProRata пришлось бы либо продаваться очень дёшево как infrastructure utility, либо долго доказывать, почему она дороже привычных paywall/subscription tools. Это плохая стартовая позиция для fund-grade economics. [T2][inference]

## 4. Telegram боты / сервисы в РФ
- **Tribute** заявляет **70 000+ авторов** и **более 4 млрд ₽ выплат** авторам через платформу. Комиссия сервиса указана как **10%**, а в FAQ есть лимиты подписок от **100 ₽** до **300 000 ₽** за транзакцию. Это сильный сигнал, что в Telegram уже есть платёжеспособный creator monetization layer, но он про подписки и донаты, а не про AI licensing. [T2: https://tribute.tg/ ; https://wiki.tribute.tg/faq]
- **Paywall.pw** продаёт доступ к закрытым Telegram-каналам по подписке и продвигает рекуррентные платежи как core value proposition. Публичного прайса на главной нет, но сам продукт подтверждает сформированный спрос на прямую монетизацию Telegram-аудитории. [T2: https://paywall.pw/]
- Mandatory endpoint по всем релевантным AI licensing queries показывает `telegram_subscribers=0`, поэтому direct Telegram-native category demand именно под ProRata-подобный продукт в РФ **не найден**. [T2: internal demand endpoint]

### Вывод по Telegram
- В РФ Telegram monetization как класс существует и масштабен. [T2]
- Но это **не тот же самый** рынок, что AI licensing / attribution. Adjacent pain подтверждён, direct wedge нет. [T2][inference]

## 5. Willingness to pay (WTP)

### Что подтверждает WTP
- Прямой global WTP подтверждается тем, что ProRata, Supertab, TollBit, ScalePost и publisher monetization vendors уже продают licensing/monetization rails, а издатели и creators на них приходят. [T2]
- В Telegram/RU creators уже принимают платные подписки, а Tribute показывает много авторов и миллиарды рублей выплат. Это подтверждает willingness to monetize audience. [T2]
- В России есть большая база каналов/страниц, для которых монетизация важна: по данным Интерфакса со ссылкой на Роскомнадзор, к 27 июня 2025 в перечень вошли **149 тыс.** персональных страниц с аудиторией более 10 тыс. подписчиков; незарегистрированным запрещено распространять рекламу и собирать пожертвования. Это значит, что monetization discipline усиливается. [T2: https://www.interfax.ru/russia/1033434]

### Что НЕ подтверждено
- Я не нашёл признаков, что российские publishers/creators уже готовы массово платить именно за **AI licensing attribution infrastructure** как отдельную статью бюджета. [T2]
- Нет публичных российских кейсов, где media house или creator network купили такой продукт, а не решили задачу юридически, через ad sales, paywall, membership, нативные интеграции или просто ожиданием больших платформенных сделок. [T2][T3]

### Вывод по WTP
**WTP в РФ на monetization есть, на ProRata-категорию как standalone software — не доказан.** Это ключевой негативный фактор. [T2]

## 6. Market sizing

### Подход и допущения
- Для top-down беру не весь российский media market, а только маленькую адресуемую долю, которую теоретически может занять AI licensing / attribution infrastructure внутри existing monetization budgets. [T1][T2]
- Для bottom-up беру узкий buyer universe: крупные digital publishers, media groups, creator networks и premium knowledge creators, для которых licensable archive и вопрос AI reuse реально могут стать продуктовой проблемой. [T2][inference]
- Курс пересчёта: **1 USD = 74,5897 ₽** на **22.04.2026**. [T1]

### Top-down
- **TAM (мир)**: Statista оценивает мировой рынок Digital Newspapers & Magazines в **$41,28 млрд** в 2025 году, или около **3,08 трлн ₽** по курсу ЦБ. Это не рынок AI licensing, а отраслевой anchor. [T1/T2]
- Для AI licensing / attribution infrastructure беру addressable share **0,15%** от global digital news/magazines spend. Получаем **TAM world ≈ 4,62 млрд ₽**. Это аналитическое допущение, потому что чистого T1 global category market ещё нет. [T1/T2][inference]
- **TAM (РФ)**: АКАР оценивает российский рынок маркетинговых коммуникаций в **2,4 трлн ₽** в 2025 году. Для ProRata-подобной infrastructure беру addressable share **0,02%**, потому что category только зарождается и относится к очень узкому monetization-tech слою. Получаем **480 млн ₽**. [T1][inference]
- **SAM (РФ)**: сегмент fit только для профессиональных publishers / creator businesses / media groups, а не всего рынка коммуникаций. Беру **40%** от TAM РФ, получаем **192 млн ₽**. [T1][inference]
- **SOM Y1**: 2% от SAM = **3,84 млн ₽**. [inference]
- **SOM Y3**: 8% от SAM = **15,36 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **250**. Это узкий реестр из крупных media houses, premium digital publishers, creator businesses и educational/news Telegram-first проектов, выделенный из значительно более широкой базы из **149 тыс.** зарегистрированных крупных страниц РКН. То есть в working ICP попадает лишь очень небольшой верхний слой, где есть бренд, архив и риск AI reuse. [T2][inference]
- **% with need** = **30%**. Не всем нужен отдельный AI licensing stack; у многих pain либо слишком ранний, либо может решаться переговорами/юристами, либо ещё не monetized. [T2][inference]
- **ARR avg** = **2,4 млн ₽/год** или **200 тыс. ₽/мес**. Это заметно выше публичных low-end substitutes и предполагает B2B package для publisher group, а не solo creator plan. [T2][inference]
- **SAM_bottom_up = 250 × 30% × 2,4 млн ₽ = 180 млн ₽**. [T2][inference]
- **SOM_bottom_up Y1 = 2% × 180 млн ₽ = 3,6 млн ₽**. [inference]
- **SOM_bottom_up Y3 = 8% × 180 млн ₽ = 14,4 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 4,62 млрд ₽ [T1/T2 + inference] | — | Чистого global category market нет, используем proxy от digital publishing | top-down |
| TAM (РФ) | 480 млн ₽ [T1 + inference] | 600 млн ₽* [T2 + inference] | diff=1,25x, приемлемо; bottom-up шире из-за buyer-universe логики | lower |
| SAM (РФ) | 192 млн ₽ [T1 + inference] | 180 млн ₽ [T2 + inference] | diff=6,7%, гипотезы сходятся | lower |
| SOM Y1 | 3,84 млн ₽ | 3,6 млн ₽ | diff=6,7% | **используем 3,6 млн ₽** |
| SOM Y3 | 15,36 млн ₽ | 14,4 млн ₽ | diff=6,7% | **используем 14,4 млн ₽** |

\* Bottom-up TAM РФ = 250 buyers × 2,4 млн ₽ = 600 млн ₽ как cross-check buyer-universe, а не full-market TAM.

### 10 реальных buyers для bottom-up sanity check
1. **РБК** [T2]
2. **Коммерсантъ** [T2]
3. **Интерфакс** [T2]
4. **ТАСС** [T2]
5. **Forbes Russia** [T2]
6. **vc.ru / Комитет** [T2]
7. **Sports.ru** [T2]
8. **Shkulev Media Holding** [T2]
9. **Wylsacom Media** [T2]
10. **Канал/медиа-сеть с платной подпиской на Tribute уровня top creators** как buyer archetype; конкретный ICP в РФ есть, но массовой стандартизации под AI licensing пока нет. [T2][speculation]

### Sanity check
- SOM Y1 = **3,6 млн ₽** при ARR **2,4 млн ₽** означает примерно **1-2 клиента** в первый год. Это реалистично для раннего enterprise sales, но слишком мало для построения fund-grade компании. [inference]
- SOM Y1 < 10% SAM, overclaiming нет. [inference]
- Даже SOM Y3 = **14,4 млн ₽** означает около **6 клиентов** через три года. Это подтверждает узость рынка. [inference]

## 7. Profit Gate — проверка всех сценариев

### Сценарий A. Self-serve creator / small publisher
- Цена: **15 тыс. ₽/мес**
- GM: **85%**
- Валовая прибыль на клиента: **12,75 тыс. ₽/мес**
- При OPEX **2,5 млн ₽/мес** для EBITDA **500 тыс. ₽/мес** нужно примерно **236 клиентов**.
- Для категории с LOW demand это нереалистично.
- **Вердикт: FAIL.** [T2][inference]

### Сценарий B. Mid-market publisher SaaS
- Цена: **75 тыс. ₽/мес**
- GM: **80%**
- Валовая прибыль на клиента: **60 тыс. ₽/мес**
- Для цели **500 тыс. ₽ EBITDA/мес** нужно примерно **50 клиентов**.
- Это уже около **20% всего buyer universe 250** или **67% active buyers 75**, что для нового category-creation motion слишком агрессивно.
- **Вердикт: FAIL.** [T2][inference]

### Сценарий C. Enterprise media network
- Цена: **200 тыс. ₽/мес**
- GM: **75%**
- Валовая прибыль на клиента: **150 тыс. ₽/мес**
- Для цели нужно примерно **20 клиентов**.
- Но наш консервативный SOM Y3 говорит лишь о **~6 клиентах** за 3 года. Значит Profit Gate противоречит реалистичному market capture. [T1/T2][inference]
- **Вердикт: FAIL.**

### Сценарий D. Hybrid software + legal / monetization advisory wrapper
- Цена: **350 тыс. ₽/мес**
- GM: **55%** из-за heavy services
- Валовая прибыль на клиента: **192,5 тыс. ₽/мес**
- Для цели нужно примерно **16 клиентов**.
- Такой сценарий снижает барьер входа, но убивает масштабируемость и делает бизнес service-heavy. При LOW category demand это не фондовая история. [T2][inference]
- **Вердикт: FAIL.**

## 8. Риски
- В РФ нет сформированного buyer behavior именно под AI licensing / attribution software. [T2]
- Publisher monetization substitutes проще объясняются и уже укоренены. [T2]
- Большие AI licensing deals в мире часто заключаются вручную между платформами и крупными правообладателями, что уменьшает роль независимого software layer. [T2][T3]
- Telegram monetization в РФ силён, но это не автоматически конвертируется в спрос на ProRata-подобный продукт. [T2]

## 9. Финальный вывод для pipeline
**Demand = LOW и Profit Gate = FAIL.**

Следовательно, кейс нужно **отклонить немедленно** на этапе Demand Validation и переместить в `pipeline/rejected/`.

Sources: T1=4, T2=13, T3=1. Primary evidence basis: T2.
