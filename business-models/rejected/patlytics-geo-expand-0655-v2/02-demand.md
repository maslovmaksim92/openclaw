# 02-demand

## Вывод
- **Composite demand:** LOW по `multi-demand` для `patent ai` (score 15), `patent analytics` (15), `patent search` (15), `патентный поиск` (22), `intellectual property management` (7). Это слабый сигнал для нового standalone SaaS в РФ. [T2]
- **Итог по кейсу:** **REJECTED**. Причина: низкий подтверждённый спрос в РФ + ни один сценарий монетизации не выводит локальную компанию на EBITDA >= 500 тыс. ₽/мес. без слишком узкого enterprise-sales motion.

## Что именно продаёт Patlytics
Patlytics позиционируется как AI-платформа для patent workflow, prosecution, portfolio management и litigation support для IP-команд и патентных юрфирм. Для РФ это означает необходимость локализации под Роспатент, русскоязычные шаблоны, закрытый контур и local data handling. Это увеличивает CAC и срок сделки. [T2]

## Demand signals
### multi-demand endpoint
- `patent ai` -> LOW, score 15; Google Trends RU 1/100, HH 3, Telegram 0. [T2]
- `patent analytics` -> LOW, score 15; Google Trends RU 0/100, HH 0, Telegram 0. [T2]
- `patent search` -> LOW, score 15; Google Trends RU 1/100, HH 0, Telegram 0. [T2]
- `патентный поиск` -> LOW, score 22; Google Trends RU 2/100, HH 109, Telegram 0. Но это ближе к услуге поиска/экспертизы, а не к подписке на patent-AI SaaS. [T2]
- `intellectual property management` -> LOW, score 7; Google Trends RU 0/100, HH 138, Telegram 0. [T2]

### Интерпретация
- В РФ есть спрос на патентную функцию как сервис и юридическую практику, но **не видно сильного публичного pull именно на отдельный patent-AI SaaS**. [T1][T2]
- HH и поисковые сигналы подтверждают наличие профессии и задач, но не подтверждают наличие широкого бюджета на новый специализированный стек. Это **supporting evidence, не primary demand proof**. [T1][T2]

## Конкуренты и цены
Минимум 3 реальных аналога с публичной ценой:
1. **AppColl**: docketing от **$89/user/mo**, patent & trademark management от **$130/user/mo**, IP search от **$75/mo**, invention management от **$350/mo per 100 users**. Это примерно **7.9k-31.0k ₽/мес.** по курсу ЦБ РФ 1 USD = 87.15 ₽ на 22.04.2026. [T2][T1]
2. **Alt Legal**: планы **$199/mo**, **$390/mo**, enterprise custom. Это примерно **17.3k-34.0k ₽/мес.** [T2][T1]
3. **IPzen**: публично заявляет цены от **€5,000/year** за 2 users и от **€19,500/year** за business tier. Это примерно **438.8k-1.71m ₽/год** по курсу ЦБ РФ 1 EUR = 87.76 ₽ на 22.04.2026. [T2][T1]

### Что это значит для РФ
- Глобальный референс по цене существует, но он в основном лежит в диапазоне **~200k-1.7m ₽ в год** на аккаунт/команду. [T2][T1]
- Для РФ после локализации и сужения TAM реалистичный ACV для local launch выглядит как **300k-1.2m ₽/год** для юрфирмы и **0.8-2.0m ₽/год** для крупного enterprise-account. Это вывод по reconciliation публичных цен конкурентов и локальной buying power, а не прямой прайс-лист РФ. [T2, inference]

## Telegram / RU services check
- По demand-endpoint Telegram subscribers = 0 по всем релевантным англоязычным запросам. [T2]
- При web-поиске не найдено заметных массовых **Telegram-ботов в РФ**, которые бы уже выступали distribution channel для patent-AI workflow. Это отрицательный сигнал по consumer-like pull. [T2]
- В РФ есть **веб-сервисы**, а не TG-first продукты: Online Patent, Роспатент/FIPS search tools, IPChain-инфраструктура, патентные бюро с кабинетами клиента. Но это другой рынок, ближе к filing/search service, а не к AI operating system для patent teams. [T1][T2]

## WTP, proof of willingness to pay
### Что подтверждено
- Клиенты глобально **платят** за patent management software: публичные цены AppColl, Alt Legal и IPzen это прямое доказательство willingness to pay. [T2]
- В РФ компании платят за патентных поверенных, поиск, регистрацию и сопровождение IP, потому что поток заявок и институт патентных поверенных существует, а Роспатент публикует устойчивый объём заявок. [T1]

### Что не подтверждено
- Не найдено надёжного доказательства, что в РФ уже есть массовый бюджет именно на **AI-native patent workflow SaaS** с западным positioning Patlytics. [T1][T2]
- Следовательно, **WTP в РФ есть на outcome/service**, но **WTP на отдельный software layer слабее и спекулятивен**. [T1][T2]

## Market sizing
**[LOW CONFIDENCE]** Точный рынок patent-AI software в РФ публично не раскрывается, поэтому оценка собрана через reconciliation T1-операционных метрик (заявители, патентные поверенные) и T2-публичных цен конкурентов.

### Предпосылки
- В 2024 году в РФ подано **21,502** заявки на изобретения; российские заявители подали **15,777**, из них коммерческие организации **3,216**. [T1]
- В реестре Роспатента на 22.04.2026 числится **2,751** патентный поверенный. Не все работают с patent workflow software, и не все являются платёжеспособными seat buyers. [T1]
- Для bottom-up берём **10 реальных buyers/target accounts**: Ростех, Росатом, Сбер, Яндекс, Газпром нефть, КАМАЗ, Татнефть, МТС, Северсталь, Сколтех. Это организации с высокой IP-активностью или очевидной потребностью в системном IP-process. [T1][T2]

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 20.0-35.0 млрд ₽ экв. annual software spend для patent/IP workflow niche, very rough proxy по глобальным pricing bands и числу крупных IP teams [T2/T3] | — | глобальная оценка слишком шумная | top-down |
| TAM (РФ) | **260 млн ₽/год** = (2,751 поверенных x 20% addressable x 25k ₽/мес x 12) + (3,216 компаний x 5% x 600k ₽/год) [T1][T2] | **210 млн ₽/год** = 350 buyers x 70% need x 850k ₽ ARR [T1][T2] | diff ~24%; обе оценки сходятся на sub-0.3 млрд ₽ | **210 млн ₽** |
| SAM (РФ) | **91 млн ₽/год** = TAM x 35% для mid-market/enterprise buyers с реальным fit [T1][T2] | **71 млн ₽/год** = 120 buyers x 70% need x 850k ₽ ARR [T1][T2] | diff ~28%; ограничение из-за enterprise-only motion | **71 млн ₽** |
| SOM Y1 | **2.7 млн ₽** = SAM x 3% [T1][T2] | **3.6 млн ₽** = 6 клиентов x 600k ₽ ARR [T1][T2] | diff ~33%; обе оценки ниже уровня, достаточного для strong venture case | **2.7 млн ₽** |
| SOM Y3 | **9.1 млн ₽** = SAM x 10% [T1][T2] | **10.2 млн ₽** = 12 клиентов x 850k ₽ ARR [T1][T2] | diff ~12% | **9.1 млн ₽** |

### Sanity checks
- Top-down и bottom-up не расходятся более чем в 3 раза, значит сегмент описан консистентно. [T1][T2]
- SOM Y1 < 10% SAM, это реалистично. [inference]
- Даже SOM Y3 ~9.1 млн ₽ ARR даёт лишь ~0.76 млн ₽ выручки в месяц до COGS и fixed opex, то есть **этого мало для локальной EBITDA 500k+/мес**. [inference]

## Profit Gate: проверка всех сценариев
### Сценарий 1. Boutique patent firms
- 25 клиентов x 35k ₽ MRR = **875k ₽/мес выручки**. [T2][inference]
- При 80% gross margin это ~700k ₽ gross profit. Один seller + solutions/support + локализация/hosting/legal уже съедают >700k ₽/мес. **EBITDA < 0**. [inference]

### Сценарий 2. Mid-market IP teams / tech companies
- 10 клиентов x 120k ₽ MRR = **1.2 млн ₽/мес выручки**. [T2][inference]
- Для такого чека нужен длительный enterprise sales cycle, security review, интеграции и локализация под Роспатент. Реалистичный fully-loaded opex локальной команды 0.9-1.4 млн ₽/мес. EBITDA в лучшем случае около нуля, чаще отрицательная. [T1][T2][inference]

### Сценарий 3. Enterprise premium
- 5 клиентов x 250k ₽ MRR = **1.25 млн ₽/мес выручки**. [T2][inference]
- Математически EBITDA 500k+ возможна только при очень lean operating model и наличии 5 крупных accounts почти сразу. Это противоречит observed demand LOW, узкому buyer universe и длинному циклу сделки. Для standalone investable case сценарий нереалистичен. [T1][T2][inference]

### Итог Profit Gate
**FAIL.** На бумаге gate можно пройти только в агрессивном premium-enterprise сценарии, но он не подтверждён спросом и слишком хрупок. Во всех базовых сценариях локальная EBITDA >= 500k ₽/мес **не достигается**. [T1][T2]

## Инвестиционный вывод
- Спрос в РФ на patent operations существует, но он выглядит как **узкий expert market**, а не широкий software category pull. [T1][T2]
- Patlytics в РФ упирается в узкий buyer pool, локализацию под Роспатент и неочевидный software budget поверх уже покупаемых услуг. [T1][T2]
- Для фонда это не проходит как новый venture-scale GEO-expand кейс в РФ сейчас.

## Источники
- Rospatent annual report / statistics and registry pages: структура заявителей и число патентных поверенных. [T1]
- CBR currency rates on 22.04.2026 for USD/EUR conversion. [T1]
- AppColl pricing, Alt Legal pricing, IPzen pricing pages. [T2]
- multi-demand endpoint for RU demand snapshots. [T2]

Sources: T1=4, T2=5, T3=1. Primary evidence basis: T1/T2 mixed, with T1 for market structure and T2 for pricing/demand proxies.
