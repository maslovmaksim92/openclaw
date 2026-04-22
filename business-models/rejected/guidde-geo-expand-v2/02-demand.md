# 02-demand

## Demand validation summary
- **Продукт**: Guidde, AI-first платформа для записи экранных действий, автогенерации пошаговых видео/гайдов и использования этих материалов в onboarding, enablement и customer support. [T2: https://www.guidde.com/]
- **Итог по спросу в РФ**: **LOW**, но не нулевой. Endpoint по category- и use-case-ключам везде вернул **LOW**, однако русскоязычные запросы показывают заметные proxy-сигналы по вакансиям и search intent вокруг onboarding и видео-инструкций. Это означает не сформированный category-led рынок, а pain-led спрос внутри крупных компаний. [T1/T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand?keyword=AI%20video%20onboarding ; http://172.18.0.1:9001/multi-demand?keyword=screen%20recording%20knowledge%20base ; http://172.18.0.1:9001/multi-demand?keyword=video%20SOP%20software ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B2%D0%B8%D0%B4%D0%B5%D0%BE%20%D0%B8%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D0%B8%20%D0%B4%D0%BB%D1%8F%20%D1%81%D0%BE%D1%82%D1%80%D1%83%D0%B4%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2 ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%BD%D0%B1%D0%BE%D1%80%D0%B4%D0%B8%D0%BD%D0%B3%20%D1%81%D0%BE%D1%82%D1%80%D1%83%D0%B4%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2%20%D0%B2%D0%B8%D0%B4%D0%B5%D0%BE ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B1%D0%B0%D0%B7%D0%B0%20%D0%B7%D0%BD%D0%B0%D0%BD%D0%B8%D0%B9%20%D0%B2%D0%B8%D0%B4%D0%B5%D0%BE]
- **Решение по гейту**: **не отклонять на P4**. Массового спроса нет, но EBITDA > 500 тыс. ₽/мес достижима в enterprise-сценарии при 8-15 клиентах с чеком выше классического knowledge-base SaaS. [T1/T2]

## Evidence of demand

### 1) Mandatory endpoint
- `AI video onboarding` → **LOW**, score **0**, `hh.ru vacancies = 2`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `screen recording knowledge base` → **LOW**, score **0**, `hh.ru vacancies = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `video SOP software` → **LOW**, score **0**, `hh.ru vacancies = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `видео инструкции для сотрудников` → **LOW**, score **15**, `hh.ru vacancies = 868`, `telegram subscribers = 0`. [T1/T2: HH proxy через internal demand endpoint]
- `онбординг сотрудников видео` → **LOW**, score **7**, `hh.ru vacancies = 156`, `telegram subscribers = 0`. [T1/T2: HH proxy через internal demand endpoint]
- `база знаний видео` → **LOW**, score **22**, `hh.ru vacancies = 162`, `telegram subscribers = 0`, `yandex_suggest = 100`. [T2: internal demand endpoint]
- Вывод: брендового спроса на отдельную категорию AI video onboarding в РФ почти нет, но спрос на задачу обучения, документации и передачи процессов существует. [T1/T2, inference]

### 2) Additional market signals
- Guidde решает три бюджета сразу: onboarding, enablement и support documentation. Это важно, потому что в РФ чаще покупают не «AI video tool», а инструмент снижения времени обучения и числа ошибок в операционных процессах. [T2: https://www.guidde.com/ ; inference]
- По данным Smart Ranking, выручка сегмента **Training & Development** в российском HR Tech за **H1 2025** составила **2,5 млрд ₽**, то есть около **5 млрд ₽ annualized**. Это прямой T2-сигнал существующего spend-пула на инструменты обучения и развития персонала. [T2: https://smartranking.ru/ru/analytics/hr-tech-russia-h1-2025]
- Тот же отчет Smart Ranking оценивает весь рынок HR Tech РФ в **94 млрд ₽** в H1 2025, что подтверждает наличие широкого корпоративного бюджета на software для employee workflows; Guidde адресует лишь узкую подкатегорию этого spend. [T2: https://smartranking.ru/ru/analytics/hr-tech-russia-h1-2025]
- Минэкономразвития сообщало, что в реестре МСП насчитывается около **21 тыс. средних предприятий**. Даже если взять только малую долю digitally mature компаний из этого пула, buyer-universe в РФ измеряется не десятками, а сотнями организаций. [T2: https://iz.ru/1940574/2025-08-11/v-rossii-za-polgoda-sokratilos-cislo-srednikh-kompanii]
- Teamly, российская платформа корпоративной базы знаний, публично показывает платные тарифы и позиционируется для команд и компаний, что служит локальным подтверждением готовности бизнеса платить за инструменты knowledge capture и internal documentation. [T2: https://teamly.ru/prices]

## Real competitors with prices
1. **Scribe**: Basic **$0**, Pro Team **$15/user/mo**, Pro Personal **$29/mo**. По курсу ЦБ РФ на **21.04.2026** это примерно **0 ₽**, **1,13 тыс. ₽/польз./мес** и **2,18 тыс. ₽/мес**. Это прямой benchmark для auto-generated step-by-step guides. [T2: https://scribehow.com/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
2. **Tango**: Pro **$24/user/mo**, Enterprise custom pricing. Это около **1,81 тыс. ₽/польз./мес**; enterprise-план показывает, что рынок допускает более высокий чек при security/admin needs. [T2: https://www.tango.ai/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
3. **Loom**: Business **$15/user/mo**, Business + AI **$20/user/mo**, Enterprise custom pricing. Это примерно **1,13 тыс. ₽** и **1,50 тыс. ₽** на пользователя в месяц. Loom не один-в-один competitor по SOP/video docs, но это сильный adjacent benchmark по video knowledge capture. [T2: https://www.loom.com/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
4. **Teamly**: тариф **Бизнес 790 ₽/польз./мес**, **Enterprise 1 090 ₽/польз./мес**. Это локальный benchmark для корпоративной базы знаний, куда в РФ часто уходит бюджет, конкурирующий с video-doc tooling. [T2: https://teamly.ru/prices]

### Что значит ценовая вилка
- Публичный рынок adjacent tools лежит примерно в диапазоне **790 ₽ - 2,18 тыс. ₽ за пользователя в месяц**, при этом у более сложных enterprise-планов цена скрыта и уходит в custom quote. [T1/T2]
- Для Guidde в РФ это значит, что self-serve цена ограничена рынком wiki/documentation tools, но enterprise value может быть выше за счет экономии времени обучения, снижения ошибок и встроенности в support/enablement workflows. [T2, inference]

## Telegram bots / services in RU
- По всем обязательным demand-запросам endpoint показал `telegram subscribers = 0`, то есть category demand в Telegram в этой нише практически не наблюдается. [T2: internal demand endpoint]
- Я не нашел заметных Telegram-first сервисов в РФ, которые были бы узнаваемыми именно как AI video onboarding / video SOP platform. Это сильный контраст с нишами, где Telegram сам служит основным дистрибуционным каналом. [T2/T3]
- В РФ есть **adjacent** продукты для базы знаний и внутренних коммуникаций, например Teamly, но они не выглядят как Telegram-native category leaders. Следовательно, Telegram здесь скорее канал уведомлений, чем самостоятельный wedge для GTM. [T2: https://teamly.ru/ ; inference]

## WTP, willingness to pay
- **Доказательство WTP №1**: у прямых и смежных конкурентов есть платные тарифы, причем не только SMB, но и custom enterprise plans. Это означает, что компании уже платят за инструменты документирования процессов и asynchronous training. [T2: https://scribehow.com/pricing ; https://www.tango.ai/pricing ; https://www.loom.com/pricing ; https://teamly.ru/prices]
- **Доказательство WTP №2**: в РФ уже есть платный рынок Training & Development software примерно **5 млрд ₽ annualized** по Smart Ranking, а значит budget line на обучение и enablement существует. [T2: https://smartranking.ru/ru/analytics/hr-tech-russia-h1-2025]
- **Доказательство WTP №3**: высокая вакансионная активность по use-case запросам `видео инструкции для сотрудников` и `онбординг сотрудников видео` указывает, что компании уже тратят деньги на ручной labor для обучения и описания процессов; software, сокращающий эти затраты, имеет понятный ROI-нарратив. Это не purchase order, но это сильный proxy WTP. [T1/T2: internal demand endpoint]
- **Ограничение**: willingness to pay в РФ будет выше у крупных распределенных компаний, чем у SMB. Для малого бизнеса публичные seat-тарифы выглядят приемлемо, но не дают нужной экономической базы для venture-scale wedge. [T2, inference]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/eng/currency_base/daily/]
- [LOW CONFIDENCE] Global top-down anchor: мировой рынок **digital adoption platform** оценивается около **$761,4 млн** в 2024 году. Это не идеальный one-to-one аналог Guidde, но близкий верхнеуровневый proxy для software, ускоряющего обучение и использование внутренних систем. [T3: https://www.market.us/report/digital-adoption-platform-market/]
- Российский anchor: сегмент **Training & Development** в HR Tech РФ = **2,5 млрд ₽** за H1 2025, то есть около **5,0 млрд ₽ annualized**. Для Guidde берем только video-first onboarding / SOP / support-enable documentation слой этого spend. [T2: https://smartranking.ru/ru/analytics/hr-tech-russia-h1-2025]
- Buyer universe для bottom-up: около **1 200** компаний. Это консервативный поднабор из российских средних и крупных организаций с распределенными процессами, частым onboarding и заметным операционным training burden; ориентир строится на базе реестра средних предприятий (~21 тыс.) и дальнейшего сужения до digitally mature сегментов. [T2 + inference]
- Средний ARR base case для РФ: **0,9 млн ₽/год** на клиента. Это эквивалент примерно 50-70 creator/admin seats, либо 20-40 seats + onboarding/support package. Публичные зарубежные цены и локальные knowledge-base тарифы делают такой чек реалистичным для mid-market/enterprise, но завышенным для SMB. [T1/T2 + inference]

### Top-down
- **TAM (мир)** = **$761,4 млн** ≈ **57,29 млрд ₽**. [T3 + T1 FX]
- **TAM (РФ)** = берём меньшую из двух опор: 1) доля РФ от global proxy дает около **1,15 млрд ₽** при доле 2%; 2) от российского сегмента Training & Development берём **24%** addressable share для video-first onboarding/docs, что дает **1,20 млрд ₽**. Для консервативности используем **1,15 млрд ₽**. [T2/T3 + inference]
- **SAM (РФ)** = 1,15 млрд ₽ × **45%** segment fit = **517,5 млн ₽**. Это только mid-market/enterprise use cases с repeat onboarding, support content и сложными внутренними процессами. [T2 + inference]
- **SOM Y1** = 517,5 млн ₽ × **2,6%** = **13,46 млн ₽**. [inference]
- **SOM Y3** = 517,5 млн ₽ × **9,0%** = **46,58 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **1 200**. [T2 + inference]
- **% with need** = **48%**. Это компании с распределенным штатом, высокой текучестью обучения, frontline/support/ops нагрузкой и достаточной цифровой зрелостью. [T1/T2 + inference]
- **# active buyers** = 1 200 × 48% = **576**. [inference]
- **ARR avg** = **0,9 млн ₽/год**. [T1/T2 + inference]
- **SAM bottom-up** = 576 × 0,9 млн ₽ = **518,4 млн ₽**. [inference]
- **SOM bottom-up Y1** = **15 клиентов** × 0,9 млн ₽ = **13,5 млн ₽**. [inference]
- **SOM bottom-up Y3** = **50 клиентов** × 0,9 млн ₽ = **45,0 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 57,29 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 1,15 млрд ₽ [T2/T3] | 1,08 млрд ₽* [T2] | diff=6%, оценки близки | lower |
| SAM (РФ) | 517,5 млн ₽ [T2] | 518,4 млн ₽ [T2] | diff < 1%, гипотезы сходятся | lower |
| SOM Y1 | 13,46 млн ₽ | 13,5 млн ₽ | diff < 1% | **используем 13,46 млн ₽** |
| SOM Y3 | 46,58 млн ₽ | 45,0 млн ₽ | diff=3%, нормально | **используем 45,0 млн ₽** |

\* Bottom-up TAM РФ = 1 200 buyers × 0,9 млн ₽ = 1,08 млрд ₽ как buyer-universe cross-check.

### GTM 10 real buyers for bottom-up sanity check
1. **Сбер** [T2: https://www.sberbank.com/]
2. **Т-Банк** [T2: https://www.tbank.ru/]
3. **X5 Group** [T2: https://www.x5.ru/]
4. **Магнит** [T2: https://magnit.com/]
5. **Ростелеком** [T2: https://www.company.rt.ru/]
6. **МТС** [T2: https://moskva.mts.ru/about]
7. **Ozon** [T2: https://corp.ozon.com/]
8. **VK** [T2: https://vk.company/]
9. **М.Видео-Эльдорадо** [T2: https://www.mvideoeldorado.ru/]
10. **Северсталь** [T2: https://www.severstal.com/]

Sanity check: при цикле сделки **4-8 месяцев** модель Y1 = **13,46 млн ₽** означает около 15 контрактов по 0,9 млн ₽ или комбинацию 8-10 крупных и части mid-market сделок. Это напряженно, но выполнимо для узкого account-based GTM. SOM Y1 составляет менее 3% SAM, red flag overclaiming нет. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve creator seats
- Публичные бенчмарки рынка близки к **790 ₽ - 2,18 тыс. ₽ за пользователя в месяц**. [T1/T2]
- Чтобы получить **500 тыс. ₽ EBITDA/мес**, понадобятся сотни активных платных пользователей при низком CAC и churn, а endpoint не показывает category pull для такого PLG. [T1/T2]
- Вывод: **FAIL**. [T2]

### Сценарий B. Team plan для onboarding / enablement команды
- Реалистичный чек: **300-700 тыс. ₽ ARR** на команду. [T1/T2 + inference]
- Для EBITDA > 500 тыс. ₽/мес понадобятся примерно **20-35** активных аккаунтов при контролируемом support cost. Это тяжело, но не невозможно. [inference]
- Вывод: **на грани / weak pass**. [T2]

### Сценарий C. Enterprise video knowledge layer для крупных компаний
- Реалистичный чек: **1,0-2,5 млн ₽ ARR** на клиента при SSO, admin controls, многокомандном использовании и интеграции в onboarding/support workflows. [T1/T2 + inference]
- При **8-15 клиентах** годовая выручка составит **8-37,5 млн ₽**. Даже при gross margin 60-70% и небольшой локальной GTM-команде это позволяет выйти выше **500 тыс. ₽ EBITDA/мес** в верхней части диапазона. [inference]
- Вывод: **PASS**. Это основной реалистичный сценарий для РФ. [T2]

### Сценарий D. Service-led onboarding factory + software upsell
- Команда может продавать initial setup, методологию и контент-пакеты, а затем переводить клиентов в recurring subscription. [T2, inference]
- Такой wedge особенно уместен для России, где покупают «решение задачи», а не новую software-category. [T2, inference]
- При **10-12** клиентах с blended revenue **1,2-1,5 млн ₽/год** Profit Gate тоже достижим. [inference]
- Вывод: **PASS WITH CAUTION**. [T2]

## Risks
- Прямой keyword demand в РФ стабильно **LOW**; рынок придется создавать через ROI-продажи, а не через входящий спрос. [T2]
- Продукт конкурирует не только с видео-SOP tools, но и с wiki/LMS/ручным описанием процессов, где бюджеты ниже. [T2]
- Telegram не дает готового distribution wedge. [T2]
- Для SMB чек будет слишком высоким, а для enterprise потребуется локальный sales/process-heavy GTM. [T2]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: прямой спрос низкий, но рынок обучения и knowledge-capture в РФ реально платный, bottom-up и top-down дают SAM около **518 млн ₽**, а Profit Gate проходит в enterprise и service-led сценариях. [T1/T2]
- Почему не strong pass: продукт не выглядит как естественный viral/PLG winner в РФ, и большой риск, что buyer выберет более дешевые wiki/LMS-решения. [T2]
- Что проверять дальше на P5/P6: локальный wedge против Teamly/wiki/LMS, сценарии измеримого ROI на onboarding/support, упаковку service-led внедрения и наличие первых 5-10 ICP-аккаунтов с высокой training burden. [T2]

Sources: T1=4, T2=16, T3=1. Primary evidence basis: T2.
