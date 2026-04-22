# 02-demand

## Кейс
patlytics-ip-ops-geo-expand-v2

## Итог P4
**Результат: EARLY REJECT.**

Причина: по локальному demand-endpoint три релевантных запроса дают `composite_demand=LOW`, а проверка monetization-сценариев не показывает достижимый **EBITDA >= 500 тыс. ₽/мес.** на рынке РФ при реалистичной локализации и длине sales cycle.

## Demand snapshot
- `patent workflow` -> LOW, hh вакансии 3, Habr 2, yandex suggest 2, Google Trends RU 1. [T2/T3]
- `patent management` -> LOW, hh вакансии 5, Habr 2, yandex suggest 2. [T2/T3]
- `IP management software` -> LOW, hh вакансии 116, но это широкий англоязычный запрос; Google Trends RU 0. [T2/T3]
- Интерпретация: в РФ есть фоновая потребность в IP-учёте и патентной работе, но не видно сильного локального pull именно под отдельный AI-first patent workflow stack. [T2]

## Real competitors with prices
1. **Alt Legal** — от **$60/мес.** за 50 matters, $95/мес. за 250 matters, $195/мес. за 1,000 matters. Это подтверждает SMB-priced сегмент, а не heavy enterprise layer. [T2]
2. **AppColl** — от **$100 за пользователя в месяц**. Для small team из 5 пользователей это около $500/мес. [T2]
3. **IPzen** — от **$110 за пользователя в месяц**. Для команды из 5 пользователей это около $550/мес. [T2]
4. **Online Patent (РФ)** — подача заявки на товарный знак от **35 тыс. ₽**, патентование изобретения от **99 тыс. ₽**. Это подтверждает готовность российского рынка платить за discrete IP jobs, но не за recurring workflow platform на уровне enterprise SaaS. [T2]

## Telegram bots / services in RU
- **@onlinepatentru_bot** — бот сервиса Online Patent, используется как lead-gen/consultation entrypoint, а не как full patent-ops workflow system. [T3]
- Telegram-канал **Online Patent** (~6.2k подписчиков на момент проверки) — есть контент и консультационный трафик, но не признак отдельного software-category pull. [T3]
- Telegram-канал **OPENMARK / Товарные знаки и патенты** — нишевый консультационный контент, масштабы заметно меньше B2B legaltech-mass market. [T3]
- **Вывод:** в РФ Telegram используется как acquisition/support-канал для патентных услуг, а не как самостоятельный distribution proof для patent workflow SaaS. [T2/T3]

## WTP, proof of willingness to pay
- Российские компании уже платят за IP-работу: госпошлины и юридические услуги вокруг заявок, продлений и оспариваний устойчиво существуют. Роспатент и тарифы сервисов вроде Online Patent подтверждают денежный поток в category. [T1][T2]
- HH.ru показывает вакансии по направлениям «патентный поверенный», «специалист по интеллектуальной собственности», то есть компании держат internal/external budget на IP operations. [T2]
- Но публичных признаков готовности российских клиентов платить именно за **новый отдельный software layer** мало. Платёжеспособность доказана скорее для services и filing jobs, чем для AI workflow subscription. [T2]

## Market sizing
### Методика
Считал оба пути, затем взял более консервативное значение.

### Предпосылки
- Курс для пересчёта: **1 USD = 82.8559 ₽** по ЦБ РФ на 2026-04-22. [T1]
- Global proxy market: сегмент **Intellectual Property** у Clarivate дал **$799.4 млн** выручки за 2025 год. Это не чистый software-only TAM, но хороший T1-proxy для адресуемого мирового spend на IP information + workflow stack. [T1]
- В РФ зарегистрировано **2,751 патентных поверенных** на 2025-12-31. [T1]
- В 2024 году в Роспатент поступило **26.7 тыс. заявок на изобретения** и **137.4 тыс. заявок на товарные знаки**. Это подтверждает живой рынок IP operations, но он значительно меньше западных юрисдикций. [T1]
- Для bottom-up использую 10 реальных buyers: Sber, Yandex, Kaspersky, Rosatom, Rostec, Gazprom Neft, Tatneft, Kamaz, Severstal, PhosAgro. Это крупные российские корпорации с постоянной R&D / брендинговой / юридической активностью и явной потребностью в IP governance. [T2]

### Top-down
1. Беру global proxy TAM = $799.4 млн = **66.23 млрд ₽**. [T1]
2. Для РФ использую долю **0.5%** от глобального patent/IP workflow spend как консервативный proxy, исходя из малой доли РФ в мировом patent filing и локального enterprise legaltech budget. Получаем **331.2 млн ₽** TAM РФ. [T1+T2]
3. SAM: берём только B2B enterprise / patent-firm workflow сегмент с реально выраженной потребностью, **45%** от TAM РФ = **149.0 млн ₽**. [T1+T2]
4. SOM Y1: 3% от SAM = **4.5 млн ₽**. SOM Y3: 10% от SAM = **14.9 млн ₽**. Это уже верхняя граница реалистичности; выше был бы overclaiming. [T2]

### Bottom-up
1. Потенциальные buyers: примерно **450** организаций, где product может быть релевантен в РФ: около 300 патентных/юридических IP-практик и 150 крупных корпораций/НИОКР-групп с собственным IP контуром. [T1][T2]
2. Доля с выраженной болью: **35%**. Основание: низкий общий спрос по direct keyword, но наличие вакансий и устойчивых filing-процессов. Получаем **158** реальных целевых аккаунтов. [T2]
3. Средний контракт: **900 тыс. ₽ ARR**. Это эквивалент ~75 тыс. ₽/мес. за небольшой team license + support; выше для enterprise, ниже для патентных бюро. [T2]
4. **SAM bottom-up = 158 × 900 тыс. ₽ = 142.2 млн ₽.**
5. **SOM bottom-up Y1 = 3% = 4.3 млн ₽**, **Y3 = 10% = 14.2 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 66.23 млрд ₽ [T1] | — | — | top-down |
| TAM (РФ) | 331.2 млн ₽ [T1/T2] | 405.0 млн ₽ [T1/T2] | diff=22%, допустимо; bottom-up шире из-за включения corp IP teams | **331.2 млн ₽** |
| SAM (РФ) | 149.0 млн ₽ [T1/T2] | 142.2 млн ₽ [T1/T2] | diff=5%, оценки согласованы | **142.2 млн ₽** |
| SOM Y1 | 4.5 млн ₽ | 4.3 млн ₽ | diff=5% | **4.3 млн ₽** |
| SOM Y3 | 14.9 млн ₽ | 14.2 млн ₽ | diff=5% | **14.2 млн ₽** |

### 10 реальных buyers для bottom-up
1. Сбер
2. Яндекс
3. Лаборатория Касперского
4. Росатом
5. Ростех
6. Газпром нефть
7. Татнефть
8. КАМАЗ
9. Северсталь
10. ФосАгро

## Profit Gate, all monetization scenarios
### Сценарий 1. SMB SaaS для патентных бюро
- Цена: 75 тыс. ₽/мес. на аккаунт.
- Нужный revenue для EBITDA 500 тыс. ₽/мес. при EBITDA margin 35%: **1.43 млн ₽/мес.**
- Нужно ~**19 клиентов**.
- Для столь узкого рынка и LOW demand это тяжело: требуется почти мгновенно закрыть заметную долю всей serviceable ниши, при том что публичные price anchors у глобальных аналогов ниже. [T2]
- **Вывод:** fail.

### Сценарий 2. Mid-market hybrid SaaS + services
- Цена: 150 тыс. ₽/мес. на аккаунт.
- EBITDA margin реалистично 25% из-за онбординга, кастомизаций, русскоязычной поддержки и интеграций.
- Нужный revenue: **2.0 млн ₽/мес.**, то есть **14 клиентов**.
- Для российского patent-ops сегмента это слишком много; pipeline и sales capacity не сходятся с SOM Y1. [T2]
- **Вывод:** fail.

### Сценарий 3. Enterprise on-prem / private contour
- Цена: 4.5 млн ₽ ARR на клиента.
- Для EBITDA 500 тыс. ₽/мес. нужен минимум revenue run-rate **12 млн ₽ ARR** при 50% gross margin и heavy pre-sales/custom work, то есть примерно **3 крупных клиента**.
- Но sales cycle у enterprise legal/procurement для такого продукта длинный, локализация под Роспатент и русские документы тяжёлая, а спрос по ключам слабый. На Y1 достижение 3 таких клиентов выглядит малореалистично. [T1][T2]
- **Вывод:** fail.

## Decision
- **Demand = LOW**.
- **Profit Gate = FAIL**.
- Следовательно, по правилу early reject кейс надо отклонить и отправить в `pipeline/rejected/`.

## Источники
### T1
1. Clarivate Annual Report 2025, сегмент Intellectual Property: https://annualreport.clarivate.com/financials/segment-information/default.aspx
2. ЦБ РФ, курсы валют: https://www.cbr.ru/currency_base/daily/
3. Роспатент, годовой отчёт 2024: https://rospatent.gov.ru/content/uploadfiles/otchet-2024-ru.pdf
4. Роспатент, отчёт 2025 / реестр патентных поверенных: https://rospatent.gov.ru/ru/documents/reports/otchet-2025.pdf
5. WIPO IP Facts and Figures 2024: https://www.wipo.int/edocs/pubdocs/en/wipo-pub-943-2024-en-ip-facts-and-figures.pdf

### T2
6. Alt Legal pricing: https://altlegal.com/pricing/
7. AppColl pricing summary: https://www.g2.com/products/appcoll/pricing
8. IPzen pricing summary: https://crozdesk.com/software/ipzen/pricing
9. Online Patent pricing: https://onlinepatent.ru/prices/
10. HH.ru search, патентный поверенный / интеллектуальная собственность: https://hh.ru/search/vacancy?text=%D0%BF%D0%B0%D1%82%D0%B5%D0%BD%D1%82%D0%BD%D1%8B%D0%B9+%D0%BF%D0%BE%D0%B2%D0%B5%D1%80%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9

### T3
11. Telegram bot Online Patent: https://t.me/onlinepatentru_bot
12. Telegram channel Online Patent: https://t.me/onlinepatent
13. Telegram channel OPENMARK: https://t.me/openmarkru

Sources: T1=5, T2=5, T3=3. Primary evidence basis: T1.