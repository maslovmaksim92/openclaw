# 02-demand

## Demand validation summary
- **Продукт**: Hebbia, AI workflow для institutional intelligence, поиска по большим массивам документов, инвестиционного ресерча и due diligence. Категория в РФ ближе не к массовому AI search, а к узкому слою research workflow для buy-side, sell-side, investment banking и corpdev команд. [T2: https://www.hebbia.com/]
- **Итог по спросу в РФ**: **LOW**. Обязательный endpoint `multi-demand?keyword=Hebbia` вернул **LOW / score 15**, а более описательные запросы `institutional intelligence workflow` и `поиск по документам для инвестфонда` дали **LOW / score 0**. Это указывает на отсутствие оформленного локального спроса именно на standalone-категорию Hebbia-подобного research workflow. [T2: internal demand endpoint]
- **Решение по гейту**: **EARLY REJECT на P4**. Demand слабый, а Profit Gate не проходит ни в self-serve, ни в team SaaS, ни в enterprise/on-prem сценарии до уровня **EBITDA ≥ 500 тыс. ₽/мес** при реалистичном количестве клиентов в РФ. [T1][T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=Hebbia` → **LOW**, score **15**; Google Trends RU = 0, Habr = 2, HH = 0, Yandex suggest = 100. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=institutional%20intelligence%20workflow` → **LOW**, score **0**. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D0%BE%D0%B8%D1%81%D0%BA%20%D0%BF%D0%BE%20%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D0%BC%20%D0%B4%D0%BB%D1%8F%20%D0%B8%D0%BD%D0%B2%D0%B5%D1%81%D1%82%D1%84%D0%BE%D0%BD%D0%B4%D0%B0` → **LOW**, score **0**. [T2: internal demand endpoint]
- Поддерживающий запрос `инвестиционная аналитика ИИ` тоже остается слабым: **LOW**, score **7**, хотя там уже есть **68 вакансий HH**. Это говорит скорее о спросе на людей и generic AI/analytics, чем на готовый Hebbia-like workflow tool. [T1/T2: internal demand endpoint + HH proxy]

### 2) Russia demand proxies
- На конец IV квартала 2025 года в РФ было **497 профессиональных участников рынка ценных бумаг**, включая **156 инвестиционных советников**. Это верхний регулируемый контур потенциальных institutional buyers, но он сам по себе не доказывает спрос на отдельный AI research workflow. [T1: Банк России, https://www.cbr.ru/securities_market/]
- На 30.09.2025 Банк России фиксировал **341 управляющую компанию** и **32 НПФ**. Это добавляет институциональный buy-side слой, который теоретически может покупать исследовательские платформы. [T1: Банк России, https://www.cbr.ru/RSCI/]
- Перечень системно значимых кредитных организаций содержит **12 банков**, на которые приходится около **80% активов банковского сектора**. Именно этот слой может быть покупателем сложного knowledge workflow, но это узкий enterprise-сегмент, а не массовый рынок. [T1: Банк России, https://www.cbr.ru/banking_sector/credit/systembanks.html/]
- В РФ уже есть платные сервисы для проверки компаний, арбитража и контрагентов, например Контур.Фокус и Casebook. Это подтверждает наличие бюджета на data/research tooling, но также показывает, что значительная часть боли закрывается более узкими local data products, а не LLM-native institutional workspace. [T2: https://focus.kontur.ru/tariffs ; https://company.rt.ru/projects/casebook]

### 3) Category and competitive proof outside Russia
- Платный спрос на investment/document research software подтверждается реальными подписками: BamSEC продается по **$69/мес** за Pro и **$149/мес** за Pro+; Koyfin стоит **$39/мес** за Plus и **$79/мес** за Premium; FinChat продает Plus за **$24/мес** и Pro за **$64/мес**. Это доказывает, что категория monetizes глобально, но в основном через более узкие use cases и lower-price research tooling, чем heavy enterprise workflow Hebbia. [T2: https://www.bamsec.com/pricing ; https://www.koyfin.com/pricing/ ; https://finchat.io/pricing]
- Для РФ это важный негативный сигнал: если в зрелом англоязычном рынке заметная часть конкурентов стоит на уровне **$24-149/мес**, то локальному продукту будет трудно продавать дорогое standalone-решение без уникальных данных, локальных интеграций и сильного compliance moat. [T2 inference from competitor pricing]

## Competitor landscape with prices

| Конкурент | Что продает | Цена | Вывод для Hebbia в РФ |
|---|---|---:|---|
| BamSEC | SEC filings search, earnings transcripts, document analysis | **$69/мес Pro**, **$149/мес Pro+** [T2] | пользователи привыкли платить за узкий research tooling заметно меньше enterprise-цены Hebbia-like продукта. |
| Koyfin | market intelligence, financial data, dashboards, research workflows | **$39/мес Plus**, **$79/мес Premium**, **$209/мес Advisor Core** [T2] | strong price anchor для аналитического ПО, особенно вне крупнейших фондов и IB-команд. |
| FinChat | AI investment research and company intelligence | **$24/мес Plus**, **$64/мес Pro** [T2] | LLM-enabled equity research уже commoditizes по цене. |
| Контур.Фокус | проверка контрагентов, комплаенс и корпоративная аналитика по РФ | **33 500 ₽/год Basic**, **89 000 ₽/год Premium** [T2] | в РФ уже есть привычный ценовой якорь за business intelligence по юрлицам, существенно ниже enterprise knowledge workspace. |
| Casebook | судебная аналитика, арбитраж и проверка рисков | ориентир **102 000 ₽/год за лицензию** по закупочному кейсу Ростелекома [T2, с оговоркой] | локальный buyer платит за точечный legal/research tool, а не за дорогой горизонтальный workflow layer. |

**Источники по ценам**: BamSEC pricing page. [T2: https://www.bamsec.com/pricing] Koyfin pricing page. [T2: https://www.koyfin.com/pricing/] FinChat pricing page. [T2: https://finchat.io/pricing] Контур.Фокус tariffs page. [T2: https://focus.kontur.ru/tariffs] Casebook procurement note Ростелекома. [T2: https://company.rt.ru/projects/casebook]

## Telegram bots/services in Russia
- В RU Telegram есть сервисные боты для проверки контрагентов и судебной информации, например `@egrul_bot`, который в каталоге TGStat показывается как бот с примерно **11.4K MAU**. Это полезный proxy, что базовая corporate lookup потребляется даже в Telegram-формате. [T2: https://tgstat.ru/en/chat/@egrul_bot]
- Есть арбитражные и картотечные боты вроде `@KadArbitrRuBot`, которые закрывают быстрые точечные запросы по судебной информации. [T2: https://www.b2b-center.ru/market/telegram-bot-kad-arbitr-ru-bot-dlia-kad-arbitr-ru/tender-4568824/]
- Но признаков крупного Telegram-native продукта именно для institutional intelligence workflow в РФ не видно. Это означает, что Telegram в данном кейсе скорее канал алертов и легкого lead-gen, а не полноценный deployment layer. Это **вывод по рынку**, а не прямой факт продажи Hebbia-аналога. [T2 inference]

## WTP (willingness to pay)
- WTP подтверждается тем, что рынок уже платит за специализированные research/data products: **33.5-89 тыс. ₽/год** за Контур.Фокус, около **102 тыс. ₽/год** за Casebook по закупочному ориентиру, и **$24-209/мес** за международные research-инструменты. [T2]
- Однако эти платежи в основном относятся к **узким data tools**, а не к дорогому orchestration/workflow продукту. Следовательно, прямое extrapolation на Hebbia нельзя делать без оговорок. [T2 inference]
- Реалистичный local WTP для первого пилота выглядит как **300-900 тыс. ₽/год за команду** либо **1.5-3.0 млн ₽/год** для enterprise-private deployment в крупнейших банках/УК. Это **оценка-инференс**, основанная на ценах соседних продуктов и enterprise procurement логике, а не публичный прайс Hebbia. [T2 inference]
- При этом доказательств, что в РФ уже есть очередь buyers, готовых платить именно за standalone institutional intelligence workflow, не найдено. Поэтому секцию WTP нужно трактовать как **ограниченно подтвержденную**. [T1/T2]

## Market sizing

### Assumptions
- **[LOW CONFIDENCE]** Категория в РФ не сформирована как отдельный рынок, поэтому sizing строится через proxy на regulated institutional research buyers и spend на adjacent tools. [T1/T2]
- Для перевода долларовых цен в рубли использую курс Банка России около **76 ₽/$** на 18.04.2026. [T1: Банк России, https://www.cbr.ru/currency_base/daily/]
- Средний годовой чек для top-down беру **0.6 млн ₽/год** как blended contract value между low-end team plan и редкими enterprise пилотами. Это консервативный proxy. [T2 inference]
- Для bottom-up ядра беру только buyers, где действительно есть регулярный document-heavy investment workflow: крупные банки с CIB/research, инвестдома, управляющие компании и НПФ. [T1/T2]

### GTM-10 real buyers for RF expansion
1. Сбербанк, CIB и research-контур. [T1/T2]
2. ВТБ, investment banking / markets. [T1/T2]
3. Газпромбанк. [T1/T2]
4. Альфа-Банк. [T1/T2]
5. Т-Банк. [T1/T2]
6. БКС Мир инвестиций. [T2]
7. Атон. [T2]
8. Ренессанс Капитал. [T2]
9. УК Альфа-Капитал. [T2]
10. УК Первая. [T2]

### Top-down calculation
- **TAM world**: как широкий ceiling использую глобальный spend-коридор на public-markets / research tooling по comparable vendors; в пересчете на enterprise/search-heavy layer разумный порядок величины составляет **$1-3 млрд**. Это **спекулятивный диапазон**, потому что прямого Tier-1 глобального отчета по exact-category нет. [T2/T3, speculation]
- **TAM RF** = (497 профучастников РЦБ + 341 УК + 32 НПФ + 12 системно значимых банков) × 0.6 млн ₽ = **529.2 млн ₽**. Дубликаты между категориями возможны, поэтому это скорее ceiling и я дополнительно дисконтирую в SAM. [T1+T2]
- **SAM RF** = TAM × 25% segment fit = **132.3 млн ₽**. Беру только организации с тяжелым research/compliance/doc workflow и бюджетом на knowledge tools. [T1+T2]
- **SOM Y1** = SAM × 3% = **4.0 млн ₽**. [T2]
- **SOM Y3** = SAM × 10% = **13.2 млн ₽**. [T2]

### Bottom-up calculation
- **Total buyers** = **72** high-priority buyers: 12 системно значимых банков + 20 крупнейших инвестдомов/брокеров + 20 крупнейших УК + 20 НПФ/insurance-investment контуров. Это уже очищенный enterprise сегмент, а не весь регулируемый рынок. [T1+T2]
- **% with need** = **65%**, потому что не всем нужен AI workflow поверх документов, но у большинства крупных игроков есть M&A/research/compliance-intensive команды. [T1+T2 inference]
- **ARR avg** = **1.5 млн ₽/год** как средний чек для pilot-to-production у team/department level. [T2 inference]
- **SAM bottom-up** = 72 × 65% × 1.5 млн ₽ = **70.2 млн ₽**. [T1+T2]
- **SOM Y1 bottom-up** = 4% от SAM = **2.8 млн ₽**. [T2]
- **SOM Y3 bottom-up** = 12% от SAM = **8.4 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$1-3 млрд** [T2/T3, speculation] | — | прямого Tier-1 по exact-category нет | top-down range |
| TAM (РФ) | **529.2 млн ₽** [T1/T2] | **108.0 млн ₽** до need-фильтра, если взять 72 buyers × 1.5 млн ₽ [T1/T2] | diff ~4.9x, top-down содержит дубли и ceiling, поэтому ниже ориентир надежнее | **lower** |
| SAM (РФ) | **132.3 млн ₽** [T1/T2] | **70.2 млн ₽** [T1/T2] | diff ~1.9x, приемлемо после фильтрации сегмента | **70.2 млн ₽** |
| SOM Y1 | **4.0 млн ₽** | **2.8 млн ₽** | diff умеренный; берем консервативный lower | **2.8 млн ₽** |
| SOM Y3 | **13.2 млн ₽** | **8.4 млн ₽** | diff умеренный; берем lower | **8.4 млн ₽** |

### Sanity checks
- Расхождение по **SAM** меньше 3x, после сегментации модель выглядит согласованной. [T1/T2]
- **SOM Y1 = 2.8 млн ₽**, это лишь около **4% SAM**, значит overclaiming нет. [T2]
- При среднем цикле сделки **6-9 месяцев** Y1 SOM означает примерно **2-3 клиента** по 1.0-1.5 млн ₽ ARR, что операционно достижимо, но этого недостаточно для прохождения Profit Gate. [T2 inference]

## Profit Gate: company EBITDA >= 500K/mo

### Сценарий 1. Self-serve / prosumer research tool
- Цена: **25 тыс. ₽/мес** за пользователя, или **300 тыс. ₽/год**. [T2 inference from global comps]
- Реалистично в РФ в горизонте 12-18 месяцев: **15-20 платных пользователей** при LOW category demand. [T2]
- Выручка: **4.5-6.0 млн ₽ ARR**. [T2]
- При gross margin 75%, но с учетом sales, support, data/LLM и разработки EBITDA будет около **0-150 тыс. ₽/мес**, то есть **ниже порога**. [T2 inference]
- **Итог**: FAIL. [T2]

### Сценарий 2. Team SaaS for investment / strategy desks
- Цена: **1.2 млн ₽/год** за команду. [T2 inference]
- Реалистично: **5-8 клиентов** за первые 2-3 года, потому что рынок узкий и нужен trust-heavy outbound. [T1/T2]
- Выручка: **6-9.6 млн ₽ ARR**. [T2]
- Даже при 30% EBITDA margin это **150-240 тыс. ₽/мес**. [T2]
- **Итог**: FAIL. [T2]

### Сценарий 3. Enterprise / private deployment
- Цена: **3-4 млн ₽/год** на клиента. [T2 inference]
- Реалистично: **2-3 клиента** в РФ на раннем этапе, потому что buyer universe очень ограничен. [T1/T2]
- Выручка: **6-12 млн ₽ ARR**. [T2]
- Из-за кастомизации, инфобеза, интеграций и дорогого enterprise sales реальная EBITDA margin вероятно **10-20%**, то есть **50-200 тыс. ₽/мес**. [T2]
- **Итог**: FAIL. [T2]

### Вывод по гейту
- При текущем уровне спроса и узости buyer universe продукт может найти отдельные пилоты, но **не дотягивает до EBITDA 500 тыс. ₽/мес** ни в одном реалистичном сценарии для РФ. [T1/T2]
- Следовательно, правило **DEMAND=LOW + Profit Gate FAIL** выполняется, кейс должен быть **REJECTED на P4**. [T1/T2]

Sources: T1=4, T2=12, T3=1. Primary evidence basis: T2.