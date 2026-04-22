# 02-demand

## Demand validation summary
- **Продукт**: Oracle Fusion Agentic Finance & Supply Chain, AI-слой для автоматизации финансовых и supply-chain процессов поверх enterprise ERP/SCM. Основа спроса завязана на Oracle Fusion и adjacent digital transformation в крупных компаниях. [T1][T2]
- **Итог по спросу в РФ**: **LOW**. Обязательный endpoint по ключам `Oracle Fusion finance supply chain`, `Oracle Fusion AI agent ERP`, `Oracle Fusion SCM Russia` вернул composite demand **LOW**, score **0**, `hh.ru vacancies = 0`, `google trends RU = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- **Итог по Profit Gate**: **FAIL**. Во всех рассмотренных сценариях монетизации выйти на **500 тыс. ₽ EBITDA в месяц** в РФ ненадежно: buyer universe узкий, Oracle-специфичный installed base в РФ после 2022 года сузился, а локальный рынок смещен в сторону 1С и кастомных интеграторов. [T1][T2]
- **Решение P4**: **EARLY REJECT**. Одновременно выполняются оба условия: direct demand = LOW и Profit Gate не проходит. [T2]

## Evidence of demand

### 1) Mandatory endpoint
- `Oracle Fusion finance supply chain` → **LOW**, score **0**, `hh.ru vacancies = 0`, `google trends RU = 0`, `habr articles = 2`, `yandex suggest = 2`, `telegram subscribers = 0`. [T2: http://172.18.0.1:9001/multi-demand?keyword=Oracle%20Fusion%20finance%20supply%20chain]
- `Oracle Fusion AI agent ERP` → **LOW**, score **0**, те же слабые сигналы. [T2: http://172.18.0.1:9001/multi-demand?keyword=Oracle%20Fusion%20AI%20agent%20ERP]
- `Oracle Fusion SCM Russia` → **LOW**, score **0**, явных закупочных сигналов также нет. [T2: http://172.18.0.1:9001/multi-demand?keyword=Oracle%20Fusion%20SCM%20Russia]
- Интерпретация: в РФ нет заметной самостоятельной категории спроса именно под Oracle Fusion AI-агентов для finance/supply chain. [T2, inference]

### 2) Дополнительные сигналы рынка
- Oracle в официальном релизе по FY2025 сообщил, что annualized revenue по **Fusion Cloud ERP** превысил **$4 млрд**. Это подтверждает глобальный спрос на сам стек Oracle Fusion, но не локальный российский спрос. [T1: Oracle FY2025 results]
- По данным исследования Panorama Consulting среди компаний, внедряющих ERP, только **26,2%** достигли более 80% бизнес-benefits, а **43,8%** получили меньше половины ожидаемой выгоды. Это подтверждает боль вокруг оптимизации процессов и post-implementation automation. [T2: Panorama Consulting, 2024 ERP Report]
- Росстат через публикации, цитируемые Интерфаксом, оценивает, что ERP используют около **29,9%** средних и **57%** крупных организаций РФ. То есть базовый рынок ERP в РФ реален, но он не равен спросу именно на Oracle-layer. [T1: Росстат, цит. Интерфакс]
- TAdviser оценивает рынок ERP-систем в РФ примерно в **90 млрд ₽** в 2024 году, при этом спрос смещается в локальные решения и проекты импортозамещения. Для Oracle-specific wedge это сужает addressable share. [T2: TAdviser]

## Real competitors with prices
1. **1С:Fresh ERP**: тариф **ERP** от **1 900 ₽/мес на пользователя** при 5 пользователях, то есть ориентир **от 9 500 ₽/мес** или **114 000 ₽/год** за минимальный пакет. Это основной локальный substitute для finance/operations automation в РФ. [T1: https://1cfresh.com/price]
2. **Microsoft Dynamics 365 Finance**: публичная цена **$210 за пользователя в месяц**. По грубому курсу 100 ₽/$ это около **21 000 ₽/польз./мес**. [T2: Microsoft pricing page/search snippet]
3. **Odoo**: план **Standard €19.90/польз./мес**, **Custom €29.90/польз./мес**, то есть примерно **1 990–2 990 ₽/польз./мес** при курсе 100 ₽/€. [T2: https://www.odoo.com/pricing]
4. **Интеграционные Telegram/1C-боты в РФ**: типовой ценовой диапазон **40–120 тыс. ₽** за bot/service setup плюс support, например услуги по интеграции Telegram с 1С и корпоративными workflows. Это не прямой ERP-конкурент, но реальный substitute для lightweight approval/notification use cases. [T2/T3: market vendor pages]

### Что означает ценовая вилка
- Локальный buyer уже имеет более дешевые substitutes: 1С cloud-тарифы начинаются на уровне десятков тысяч рублей в месяц за минимальные команды, а Odoo и Dynamics задают понятный benchmark по user-based pricing. [T1][T2]
- Oracle-specific AI overlay пришлось бы продавать заметно дороже инфраструктурных ботов и ближе к enterprise services, но при этом demand evidence по РФ для Oracle Fusion layer отсутствует. [T2, inference]

## Telegram bots / services in RU
- Специализированных популярных Telegram-ботов в РФ именно для **Oracle Fusion finance/supply chain automation** не найдено; mandatory endpoint по всем ключам дал `telegram subscribers = 0`. [T2]
- В РФ есть adjacent рынок Telegram-first automation: боты согласования, уведомлений и 1С-интеграций, которые закрывают часть workflow pain без покупки отдельной Oracle-centric платформы. [T2/T3]
- Вывод: Telegram существует как легковесный delivery/integration channel, но не как подтвержденный канал спроса на Oracle Fusion agentic layer. [T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: компании уже платят за core ERP/finance stack, например 1С:Fresh ERP и Dynamics 365 имеют публичные регулярные тарифы. Значит willingness to pay за автоматизацию финансовых и supply-chain процессов как класс существует. [T1][T2]
- **Доказательство WTP №2**: глобальный Oracle Fusion Cloud ERP annualized revenue > **$4 млрд** показывает, что крупные enterprise buyers платят за платформу и расширения вокруг нее. [T1]
- **Доказательство WTP №3**: рынок Telegram/1С automation в РФ показывает готовность платить десятки и сотни тысяч рублей за workflow automation, но это более дешевый и локальный substitute. [T2/T3]
- **Ключевое ограничение**: локальный WTP именно за Oracle Fusion AI-agent overlay в РФ не доказан. Данные endpoint = LOW, поисковый след слабый, hh proxy = 0, Telegram = 0. Поэтому WTP в РФ надо считать **косвенным, а не подтвержденным прямыми покупками**. [T2]

## Market sizing

### Методика и допущения
- Для top-down берется мировой anchor Oracle Fusion Cloud ERP annualized revenue **>$4 млрд** как proxy глобального TAM у существующего Oracle Fusion ecosystem. [T1]
- Для РФ top-down стартуем от рынка ERP в РФ **90 млрд ₽** и берем только **40%** foreign/large-enterprise transformation layer, затем **5%** как Oracle-relevant wedge. Это дает консервативный Oracle-specific TAM. [T2 + inference]
- Для bottom-up buyer pool берем **500 крупнейших компаний РФ** как realistic universe крупных multi-entity buyers; penetration ERP берем **90%** как upper proxy для top-tier enterprises, а долю с острой болью берем **43%** на основе ERP underperformance data Panorama. [T1][T2 + inference]
- Средний контракт для Oracle-specific managed overlay принимаю **3 млн ₽/год**. Это выше SaaS-ботов и ниже full-scale ERP SI project, что соответствует узкому AI/workflow-optimization слою. [T1][T2 + inference]

### Top-down
- **TAM (мир)** = **$4,0 млрд** ≈ **400 млрд ₽** при курсе 100 ₽/$ как proxy текущего глобального spend вокруг Fusion Cloud ERP. [T1 + inference]
- **TAM (РФ)** = 90 млрд ₽ × 40% × 5% = **1,8 млрд ₽**. [T2 + inference]
- **SAM (РФ)** = TAM РФ × 60% (только finance/supply chain transformation wedge) = **1,08 млрд ₽**. [T2 + inference]
- **SOM Y1** = SAM × 2% = **21,6 млн ₽**. [inference]
- **SOM Y3** = SAM × 8% = **86,4 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **500** крупнейших компаний РФ с комплексными supply-chain/finance workflows. [T2: РБК 500 / крупные корпоративные рейтинги]
- **% with need** = **38,7%** = ERP penetration 90% × pain share 43%. Это proxy доли enterprise-организаций, где pain достаточно велик, чтобы рассматривать optimization overlay. [T1][T2 + inference]
- **TAM_bottom_up (РФ)** = 500 × 90% × 3 млн ₽ = **1,35 млрд ₽**. [T1][T2 + inference]
- **SAM_bottom_up (РФ)** = 500 × 90% × 43% × 3 млн ₽ = **580,5 млн ₽**. [T1][T2 + inference]
- **SOM_bottom_up Y1** = SAM_bottom_up × 1,5% = **8,7 млн ₽**. [inference]
- **SOM_bottom_up Y3** = SAM_bottom_up × 6% = **34,8 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 400 млрд ₽ [T1] | — | — | top-down |
| TAM (РФ) | 1,8 млрд ₽ [T2] | 1,35 млрд ₽ [T1/T2] | diff=33%, допустимо: top-down включает весь Oracle-relevant wedge, bottom-up ограничен 500 крупнейшими buyer-ами | lower |
| SAM (РФ) | 1,08 млрд ₽ [T2] | 580,5 млн ₽ [T1/T2] | diff=1,86x, допустимо: bottom-up строже учитывает только проблемные внедрения | lower |
| SOM Y1 | 21,6 млн ₽ | 8,7 млн ₽ | diff=2,48x, обе оценки ниже fund-scale уровня | **используем 8,7 млн ₽** |
| SOM Y3 | 86,4 млн ₽ | 34,8 млн ₽ | diff=2,48x, даже upper case остается узким | **используем 34,8 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **X5 Group** [T2]
2. **Магнит** [T2]
3. **Ozon** [T2]
4. **СИБУР** [T2]
5. **Северсталь** [T2]
6. **НЛМК** [T2]
7. **ФосАгро** [T2]
8. **РЖД** [T2]
9. **Росатом** [T2]
10. **Ростех** [T2]

Sanity check: при enterprise sales cycle **9-12 месяцев** даже 3-4 сделки в Y1 уже выглядят напряженно для новой команды, поэтому bottom-up SOM Y1 = **8,7 млн ₽** ближе к реалистичной верхней границе. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Advisory / audit-only
- Возможный чек: **1,0–1,5 млн ₽** за Oracle/ERP process assessment. [T2/T3]
- Реалистичный поток при LOW demand: **1 проект в квартал**, средняя месячная выручка **0,33–0,50 млн ₽**. Для delivery нужны founder + analyst + solution architect, то есть EBITDA уходит в ноль или минус. [T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий B. SaaS / copilot overlay
- Реалистичный чек: **100–250 тыс. ₽ MRR** на enterprise account. [T1][T2, inference]
- Чтобы получить **500 тыс. ₽ EBITDA/мес**, нужен портфель минимум **8-10** платящих крупных клиентов при gross margin 75% и низком churn. При текущем direct demand это не выглядит достижимым в обозримом горизонте РФ. [T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий C. Managed optimization service
- Возможный чек: **250–400 тыс. ₽/мес** на клиента за ongoing optimization + bot/integration support. [T2/T3]
- Даже при **3 клиентах** monthly revenue составит **0,75–1,2 млн ₽**, но для выполнения SLA потребуется команда delivery/support, и EBITDA 500 тыс. ₽/мес остается ненадежным. [T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий D. SI / implementation partner
- Возможный проектный чек: **3–6 млн ₽** за кастомное внедрение. [T2/T3]
- Но это services-heavy модель с длинным пресейлом, высокой зависимостью от founder labor и низкой повторяемостью. Даже при одной крупной сделке раз в полгода profit gate не превращается в устойчивую monthly EBITDA machine. [T2, inference]
- Вывод: **FAIL**. [T2]

## Risks
- Oracle-specific installed base в РФ после волны импортозамещения ограничен и политически/операционно сложен. [T2]
- По всем mandatory keywords direct demand в РФ = **LOW**. [T2]
- Локальные substitutes, прежде всего 1С и легкие Telegram/1С integrations, снижают willingness to pay за отдельный AI layer. [T1][T2]
- Category risk высокий: боль есть, но buyer чаще решает ее через SI, кастомизацию и локальные ERP, а не через новый отдельный vendor. [T2]

## Verdict for P4
- **P4 verdict**: **REJECTED (early)**.
- Обоснование: demand endpoint вернул **LOW**, а Profit Gate не проходит ни в advisory, ни в SaaS overlay, ни в managed service, ни в SI сценарии. [T2]
- Следствие: кейс не продолжаем в P5-P7, оформляем reject на P4 и переносим кейс в `pipeline/rejected/`. [T2]

Sources: T1=4, T2=10, T3=3. Primary evidence basis: T2.
