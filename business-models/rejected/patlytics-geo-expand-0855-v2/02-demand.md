# 02-demand

## Demand validation summary
- **Продукт**: Patlytics, AI-платформа для patent search, drafting, prosecution и portfolio workflows, которую проверяем как GEO-expansion кейс для РФ. [T2: https://patlytics.ai/]
- **Итог по спросу в РФ**: **LOW** по прямой patent-категории. Обязательный endpoint дал `патентный поверенный` → **LOW / 24**, `патентный поиск` → **LOW / 22**; только более широкий запрос `интеллектуальная собственность` поднялся до **MEDIUM / 32**, что говорит скорее о существовании общего IP-рынка, а не зрелого спроса на отдельный patent-AI stack. [T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand]
- **Итог по Profit Gate**: **FAIL**. При рассмотрении SaaS, law-firm workflow, enterprise IP-department и services-assisted сценариев не получается выйти на **500 тыс. ₽ EBITDA/мес** как на надежно достижимую базовую модель для РФ. [T1][T2]
- **Решение P4**: **EARLY REJECT**. Выполняются оба обязательных условия: direct demand = **LOW** и Profit Gate = **FAIL**. [T2]

## Evidence of demand

### 1) Mandatory endpoint
- `патентный поверенный` → **LOW**, score **24**, `hh.ru vacancies = 59`, `google trends RU = 7`, `yandex suggest = 100`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `патентный поиск` → **LOW**, score **22**, `hh.ru vacancies = 109`, `google trends RU = 2`, `yandex suggest = 100`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `интеллектуальная собственность` → **MEDIUM**, score **32**, `hh.ru vacancies = 1112`, `google trends RU = 10`, `yandex suggest = 100`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- Интерпретация: в РФ есть стабильная активность вокруг IP и trademark/legal services, но не видно, что рынок уже сформировал отдельную массовую budget line под AI-first patent operations platform. [T2, inference]

### 2) Дополнительные рыночные сигналы
- Роспатент сообщил, что в 2024 году в России было подано **свыше 26 тыс. заявок на изобретения**, то есть базовый патентный контур существует и не является нулевым. [T1: https://rospatent.gov.ru/ru/news/rospatent-17012025]
- В государственном реестре РФ числится **2 091 патентный поверенный**, что подтверждает наличие профессионального buyer/user слоя, но сам слой по масштабу остаётся ограниченным. [T1: https://rupto.ru/ru/activities/state_registers/patent_attorneys]
- HH proxy из demand endpoint показывает десятки и сотни вакансий по смежным IP-запросам, то есть боль есть, но категория всё ещё выглядит services-led, а не software-led. [T1/T2: hh proxy via internal demand endpoint]

## Real competitors with prices
1. **PatSnap**: `Pro Patent Drafting` **$200/мес**, `Pro Patent Searching` **$400/мес**, базовый tier `Free`. По курсу Банка России на **22.04.2026** это примерно **14,9 тыс. ₽** и **29,8 тыс. ₽** в месяц. [T2: https://www.patsnap.com/pricing ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=22/04/2026]
2. **Онлайн Патент**: `Патентный поиск` **от 50 000 ₽**, `Патент на изобретение` **от 90 000 ₽**, `Товарный знак под ключ` **49 990 ₽**. Это важный локальный price anchor по тому, за что российский buyer уже реально платит. [T2: https://onlinepatent.ru/]
3. **PATENTUS**: `Патентный поиск` **от 40 000 ₽**, `Патент на изобретение` **от 95 000 ₽**. Ещё один локальный price anchor для law-firm / service-heavy workflows. [T2: https://patentus.ru/services/patent_search/ ; https://patentus.ru/services/patent_na_izobretenie/]

### Что означает ценовая вилка
- Глобальный software anchor в patent workflow выглядит как **14,9-29,8 тыс. ₽/мес** на профессиональный аккаунт/команду до enterprise custom. [T1][T2]
- Российский локальный buyer уже платит **40-95 тыс. ₽** за разовые patent/IP сервисы, но это service spend, а не доказанный recurring SaaS budget. [T2]
- Отсюда вывод: willingness to pay за результат есть, willingness to pay за standalone software layer в РФ пока слабее и нуждается в sales-heavy объяснении ROI. [T2, inference]

## Telegram bots / services in RU
- У **Онлайн Патент** есть официальный Telegram-канал `t.me/onlinepatent`, а у **Ezybrand** на сайте прямо указан Telegram-канал о товарных знаках и патентах. Значит, Telegram используется как контентный и lead-gen канал в российском IP-сегменте. [T2: https://onlinepatent.ru/ ; https://ezybrand.ru/]
- Однако я не нашёл заметных Telegram-first ботов именно для patent search / patent drafting / portfolio ops как отдельного SaaS-класса; обязательный endpoint также возвращает `telegram subscribers = 0` для patent-ключей. [T2: internal demand endpoint]
- Вывод: Telegram в РФ работает как marketing/support surface для IP-сервисов, но не как сформированный канал распределения спроса на patent-AI платформу уровня Patlytics. [T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: PatSnap держит публичные подписки **$200-400/мес**, значит в мире patent workflow software покупают и у категории есть коммерческая база. [T2]
- **Доказательство WTP №2**: в России локальные игроки регулярно продают `патентный поиск` за **40-50 тыс. ₽** и `патент на изобретение` за **90-95 тыс. ₽`, что подтверждает ценность solved outcome. [T2]
- **Доказательство WTP №3**: наличие **59-109** HH-вакансий по patent-ключам и **1112** по широкому IP-запросу означает, что компании уже несут payroll-cost на IP-функцию и теоретически могут покупать automation. [T1/T2]
- Но локальный recurring WTP на отдельный AI patent stack не доказан: публичные RU price anchors в основном service-based, а demand endpoint по прямым patent-ключам остаётся LOW. Поэтому вывод по WTP для РФ: **есть outcome-level willingness to pay, нет сильного доказательства software-level willingness to pay**. [T2]

## Market sizing

### Методика и допущения
- Курс пересчёта: **1 USD = 74,5897 ₽** по Банку России на **22.04.2026**. [T1: https://www.cbr.ru/scripts/XML_daily.asp?date_req=22/04/2026]
- Для top-down РФ использую официальный объём patent activity Роспатента и локальные price anchors на patent search / filing services. [T1][T2]
- Для bottom-up считаю buyer pool как сочетание крупных корпоративных IP-держателей и профессиональных patent/IP firms, а средний ARR беру как software + workflow budget, а не как разовую юридическую услугу. [T1][T2]
- **[LOW CONFIDENCE]** Global TAM оцениваю диапазоном по внешним market-report источникам, потому что публичного Tier-1 global number именно по patent management software я не нашёл. Значение использую только как ориентир, а не как главный инвестиционный аргумент. [T3]

### Top-down
- **TAM (мир)**: ориентир **$0,9-1,3 млрд** для patent/IP management software, midpoint **$1,1 млрд** или около **82,0 млрд ₽**. Это low-confidence диапазон из внешних market reports. [T3, LOW CONFIDENCE]
- **TAM (РФ)**: `26 000+` заявок на изобретения × **50 000 ₽** как базовый локальный spend-anchor на patent search/workflow result = примерно **1,30 млрд ₽** annual patent workflow spend. Как addressable software layer беру около **30%** этого spend, получаю **390 млн ₽**. [T1][T2][inference]
- **SAM (РФ)**: только repeat-heavy buyers, где есть регулярный объём и экономический смысл автоматизации, то есть примерно **35%** от TAM РФ = **136,5 млн ₽**. [T1][T2][inference]
- **SOM Y1**: **3%** от SAM = **4,1 млн ₽**. [inference]
- **SOM Y3**: **10%** от SAM = **13,7 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = около **300**: ~**120** patent/IP firms и boutiques + ~**180** крупных компаний с активным IP-контуром. Это приближение на базе официального реестра патентных поверенных и наблюдаемого рынка крупных инновационных компаний. [T1][T2][inference]
- **% with need** = **35%**. Не всем нужен AI-first workflow, но high-volume firms и крупные корпоративные IP-отделы имеют явный automation pain. [T1/T2, inference]
- **ARR avg** = **1,2 млн ₽/год** на покупателя, если продавать не self-serve, а командный workflow / enterprise-lite пакет. [T2, inference]
- **SAM_bottom_up** = 300 × 35% × 1,2 млн ₽ = **126,0 млн ₽**. [T1][T2][inference]
- **SOM_bottom_up Y1** = **4 клиента** × 1,2 млн ₽ = **4,8 млн ₽**. [inference]
- **SOM_bottom_up Y3** = **12 клиентов** × 1,2 млн ₽ = **14,4 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $1,1 млрд / ~82,0 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 390,0 млн ₽ [T1][T2] | 360,0 млн ₽ [T1][T2] | diff=8%, bottom-up back-solves from 300 buyers × 1,2 млн ₽ potential budget | lower |
| SAM (РФ) | 136,5 млн ₽ [T1][T2] | 126,0 млн ₽ [T1][T2] | diff=8%, оценки согласуются | lower |
| SOM Y1 | 4,1 млн ₽ | 4,8 млн ₽ | diff=17%, обе оценки очень малы | **используем 4,1 млн ₽** |
| SOM Y3 | 13,7 млн ₽ | 14,4 млн ₽ | diff=5%, обе оценки не дают fund-scale исхода | **используем 13,7 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **Gorodissky & Partners** [T2: https://gorodissky.com/]
2. **PATENTUS** [T2: https://patentus.ru/]
3. **Зуйков и партнёры** [T2: https://zuykov.com/]
4. **Росатом** [T2: https://rosatom.ru/]
5. **Ростех** [T2: https://rostec.ru/]
6. **Сбер** [T2: https://www.sberbank.com/]
7. **Яндекс** [T2: https://yandex.ru/company/]
8. **Лаборатория Касперского** [T2: https://www.kaspersky.ru/]
9. **СИБУР** [T2: https://www.sibur.ru/]
10. **Газпром нефть** [T2: https://www.gazprom-neft.ru/]

Sanity check: при среднем цикле продажи **6-9 месяцев** команда без локального бренда физически не успеет закрыть много сделок в первый год; SOM Y1 на уровне **4,1 млн ₽** выглядит скорее верхней границей разумного base case. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve patent SaaS
- По публичным global comparables базовая вилка составляет около **14,9-29,8 тыс. ₽/мес**. [T1][T2]
- Даже **20** платящих аккаунтов дали бы лишь **298-596 тыс. ₽ MRR**, чего недостаточно для **500 тыс. ₽ EBITDA/мес** после локализации, sales и support. [T1][T2][inference]
- Вывод: **FAIL**. [T2]

### Сценарий B. Law-firm workflow subscription
- Реалистичный чек в РФ можно оценить в **80-120 тыс. ₽/мес** на фирму, если продавать командный workflow с drafting/search templates. [T2, inference]
- Для EBITDA 500 тыс. ₽/мес понадобятся примерно **20+** фирм при нормальной валовой марже и хотя бы минимальной локальной команде. Для категории с demand LOW это слишком тяжёлый base case. [T1][T2][inference]
- Вывод: **FAIL**. [T2]

### Сценарий C. Enterprise IP department
- Теоретически можно продавать по **1,2-2,4 млн ₽ ARR** в крупный корпоративный IP-отдел. [T2, inference]
- Но для устойчивых **500 тыс. ₽ EBITDA/мес** нужно как минимум **8-10** активных клиентов либо более высокий чек, а buyer universe в РФ ограничен, presale длинный, и патентная функция нередко остаётся services-first. [T1][T2][inference]
- Вывод: **скорее FAIL**. [T2]

### Сценарий D. Services-assisted / reseller
- Партнёрство с патентными бюро повышает шанс первых продаж, но съедает маржу и уводит модель в services-heavy зону. [T2, inference]
- На таком узком SAM этот сценарий лучше для пилотов, чем для выхода на фондовый порог EBITDA. [T2]
- Вывод: **FAIL**. [T2]

## Risks
- Прямой спрос по patent-ключам в РФ остаётся **LOW**. [T2]
- Российский WTP подтверждён прежде всего на разовые services, а не на recurring patent-AI software. [T2]
- Buyer universe ограничен и требует долгих sales cycles. [T1][T2]
- Telegram даёт контентный канал, но не подтверждает product pull. [T2]

## Verdict for P4
- **P4 verdict**: **REJECTED (early)**.
- Обоснование: direct demand по обязательному endpoint = **LOW**, а Profit Gate не проходит ни в одном из рассмотренных monetization scenarios. [T2]
- Следствие: кейс не продолжаем в P5-P7, оформляем reject на P4 и перемещаем папку в `pipeline/rejected/`. [T2]

Sources: T1=5, T2=17, T3=1. Primary evidence basis: T2.
