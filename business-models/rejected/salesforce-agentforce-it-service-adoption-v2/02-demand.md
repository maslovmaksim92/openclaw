# 02-demand

## Demand validation summary
- **Продукт**: внедрение и кастомизация Salesforce Agentforce / Service Cloud для IT service desk, employee support и automation сценариев enterprise-класса. [T2: https://www.salesforce.com/service/pricing/]
- **Итог по спросу в РФ**: **LOW**. Для российского рынка это не массовая категория: Salesforce как стек в РФ маргинален, локальная helpdesk-покупка смещена в Jira/Usedesk/отечественные сервисы, а Telegram-first спрос закрывается локальными платформами. [T2]
- **Итог по Profit Gate**: **FAIL**. Даже при project-based монетизации 500 тыс. ₽ EBITDA/мес не выглядит надежно достижимым: локальный buyer universe слишком узкий, sales cycle длинный, а recurring base для managed service слабый. [T2]
- **Решение P4**: **EARLY REJECT**. Demand в РФ низкий, Profit Gate не проходит по всем основным сценариям монетизации. [T2]

## Evidence of demand

### 1) Mandatory endpoint
- Обязательный endpoint `http://172.18.0.1:9001/multi-demand?keyword=Agentforce` и соседние запросы (`Salesforce`, `Jira Service Management`, `Telegram bot helpdesk`) на **2026-04-23** не вернули данные из-за timeout. Использовать как численное основание спроса нельзя. [T2: internal demand endpoint, operational note]
- Поэтому demand verdict ниже основан на наблюдаемом российском buyer behavior, ценах конкурентов, локальных Telegram/helpdesk сервисах и market-fit ограничениях в РФ. [T2]

### 2) Дополнительные рыночные сигналы
- Salesforce публично продаёт Service Cloud с AI/Agentforce-слоем, то есть глобальный WTP у enterprise-сегмента существует. Но это не доказывает локальный российский спрос. [T2: https://www.salesforce.com/service/pricing/]
- В РФ helpdesk/omnichannel automation уже закрывается локальными и нейтральными вендорами, например Usedesk, включая Telegram и AI-агентов. Это снижает потребность именно в Salesforce-first решении. [T2: https://usedesk.ru/ ; https://usedesk.ru/pricing]
- На hh.ru и в открытом российском инфополе категория спроса выражена скорее вокруг service desk / helpdesk / customer support automation вообще, а не вокруг `Salesforce Agentforce` как отдельного класса закупки. Это означает слабый локальный keyword pull. [T1/T2, inference]

## Real competitors with prices
1. **Salesforce Service Cloud**: Starter **$25/польз./мес**, Pro Suite **$100/польз./мес**, Enterprise **$165/польз./мес**, Unlimited **$330/польз./мес**. Для IT service сценариев это и есть baseline ценового потолка глобального enterprise-вендора. [T2: https://www.salesforce.com/service/pricing/]
2. **Freshservice**: Starter **$19/agent/month**, Growth **$49**, Pro **$99**, Enterprise **custom**. Это прямой ITSM/helpdesk comparable с публичной AI-обвязкой. [T2: https://www.freshworks.com/freshservice/pricing/]
3. **Usedesk (РФ)**: Стандарт **3 499 ₽ за агента в месяц**, Эксперт + ИИ **4 499 ₽ за агента в месяц**, advanced AI hints **+2 000 ₽/агент/мес**, AI-бот от **100 000 ₽** за запуск и **50 000 ₽ за 1 000 закрытых тикетов**. [T2: https://usedesk.ru/pricing]

### Что означает ценовая вилка
- Российский и международный рынок уже задаёт понятный ориентир: от **3,5 тыс. ₽/агент/мес** в локальном SaaS до **$165-330/польз./мес** в enterprise-grade глобальном стеке. [T2]
- Это подтверждает **наличие willingness to pay за helpdesk automation вообще**, но не за узкий проект `Salesforce Agentforce IT service adoption` именно в РФ. [T2]
- Для новой компании/интегратора ценовая власть ограничена: buyer может выбрать более дешёвый локальный SaaS, нейтральный ITSM или собственный Telegram/helpdesk стек. [T2]

## Telegram bots / services in RU
- **Usedesk** прямо позиционируется как мультиканальная поддержка с мессенджерами и AI-агентами; на сайте есть Telegram-канал и Telegram входит в канальную логику продукта. [T2: https://usedesk.ru/ ; https://usedesk.ru/pricing]
- В РФ Telegram уже является нативным каналом клиентского сервиса, поэтому Telegram automation не является дефицитным capability. Скорее дефицитна глубокая enterprise Salesforce-интеграция, а она в РФ нужна очень узкому кругу компаний. [T2, inference]
- Вывод: Telegram-направление в РФ **есть**, но это аргумент **в пользу локальных платформ**, а не в пользу Salesforce Agentforce как standalone инвестиционного кейса. [T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: Salesforce, Freshservice и Usedesk имеют публичные тарифы и продают service automation как оплачиваемую категорию. Значит, willingness to pay за service desk automation и AI-assist доказан. [T2]
- **Доказательство WTP №2**: Usedesk monetizes не только seats, но и AI-слой, и отдельно AI-бота от **100 000 ₽** за запуск. Это особенно релевантно для РФ и показывает, что компании платят за автоматизацию поддержки и Telegram/omnichannel контур. [T2: https://usedesk.ru/pricing]
- **Но ключевое ограничение**: доказан **общий WTP за helpdesk/AI support**, а не WTP за `Salesforce Agentforce IT service adoption` в российской юрисдикции. Локальный buyer скорее платит за vendor-neutral или российский стек. [T2]

## Market sizing

### Методика и допущения
- Секция market sizing для этого кейса **[LOW CONFIDENCE]**, потому что прямого открытого российского рынка именно `Salesforce Agentforce for IT service` не существует как отдельной публичной статистической категории. Поэтому использую conservative proxy через enterprise service desk automation в РФ и отдельный bottom-up по реальным buyers. [T1/T2]
- Курс для sanity-check в рублях не требуется, так как итоговая модель ниже сразу строится в ₽. [T1]
- В top-down использую как proxy общий рынок enterprise service/helpdesk automation в РФ и беру только очень узкую долю, реально адресуемую Salesforce-first проектом. [T2 + inference]
- В bottom-up беру только крупные компании РФ с большим внутренним support-контуром и международной/сложной enterprise-архитектурой, где теоретически возможен demand на тяжёлое внедрение. [T1/T2]

### Top-down
- **TAM (мир)**: как proxy для глобального enterprise service automation берём **≈ 900 млрд ₽** annual software/services pool для service-management и adjacent customer-service tooling; под Salesforce-first IT service adoption адресуемо не более **1%**, то есть **≈ 9,0 млрд ₽**. Это не статистика по Agentforce, а intentional narrow proxy. [T2, inference]
- **TAM (РФ)**: консервативно берём **≈ 6,0 млрд ₽** годового spend pool на enterprise service desk / customer support automation / helpdesk SaaS и смежные внедрения; для Salesforce-first use case адресуемо только **2%**, то есть **120 млн ₽**. [T2, inference]
- **SAM (РФ)**: только крупные компании, где нужен именно сложный enterprise workflow, integration и AI-service desk redesign, то есть **≈ 45 млн ₽**. [T1/T2, inference]
- **SOM Y1** = **SAM × 4% = 1,8 млн ₽**. [inference]
- **SOM Y3** = **SAM × 12% = 5,4 млн ₽**. [inference]

### Bottom-up
- **10 реальных buyers** для sanity-check: Сбер, Т-Банк, Яндекс, VK, Ozon, МТС, Ростелеком, X5 Group, Магнит, Северсталь. Это реальные крупные организации с большим внутренним сервисным контуром и публичным масштабом. [T1/T2]
- **Total buyers** = **30** компаний сопоставимого масштаба в РФ, где теоретически может возникнуть потребность в тяжёлом service automation проекте enterprise-класса. [T1/T2, inference]
- **% with need** = **20%**. Только часть таких компаний имеет одновременно боль, бюджет и допуск к non-local stack. [T2, inference]
- **Avg ARR / project** = **3,6 млн ₽/год** эквивалента на клиента: это примерно разовый проект внедрения **2,4-3,0 млн ₽** + небольшой support tail, а не большой recurring контракт. [T2, inference]
- **SAM_bottom_up** = 30 × 20% × 3,6 млн ₽ = **21,6 млн ₽**. [T1/T2, inference]
- **SOM_bottom_up Y1** = **1 клиент** × 3,6 млн ₽ = **3,6 млн ₽**. [inference]
- **SOM_bottom_up Y3** = **3 клиента** × 3,6 млн ₽ = **10,8 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 9,0 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 120,0 млн ₽ [T2] | 108,0 млн ₽ [T1/T2] | diff=11%, модели сходятся на очень узком рынке | lower |
| SAM (РФ) | 45,0 млн ₽ [T1/T2] | 21,6 млн ₽ [T1/T2] | diff=2,1x, допустимо: bottom-up жёстче режет buyer universe | lower |
| SOM Y1 | 1,8 млн ₽ | 3,6 млн ₽ | diff=2x, обе оценки слишком малы | **используем 1,8 млн ₽** |
| SOM Y3 | 5,4 млн ₽ | 10,8 млн ₽ | diff=2x, обе оценки не дают fund-scale исход | **используем 5,4 млн ₽** |

Sanity check: при среднем цикле сделки **9-12 месяцев** даже **1 закрытый проект в Y1** уже выглядит реалистичным пределом для новой команды. SOM Y1 остаётся значительно ниже порога meaningful EBITDA-scale. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Разовое внедрение / кастомный проект
- Реалистичный чек в РФ: **2,4-3,0 млн ₽** за проект. [T2, inference]
- Для **500 тыс. ₽ EBITDA/мес** нужна конвейерная поставка нескольких высокомаржинальных проектов в год, но рынок слишком узкий и зависим от редких enterprise deals. [T2]
- Вывод: **FAIL**. [T2]

### Сценарий B. Managed service / support retainer
- Реалистичный retainer: **150-300 тыс. ₽ MRR** на клиента после внедрения. [T2, inference]
- Чтобы выйти на **500 тыс. ₽ EBITDA/мес**, нужно 5-8 активных клиентов при сильной delivery-команде и слабом локальном спросе на сам стек. Для РФ это слишком натянуто. [T2]
- Вывод: **FAIL**. [T2]

### Сценарий C. Reseller / агентская модель
- Маржа ниже, зависимость от основного вендора выше, а локальный buyer universe не расширяется. [T2]
- При текущем спросе reseller-модель не спасает economics. [T2]
- Вывод: **FAIL**. [T2]

### Сценарий D. Telegram/AI service add-on поверх helpdesk
- В РФ это реально продаётся, но value capture уходит локальным платформам вроде Usedesk, а не в Salesforce-first implementation story. [T2]
- Это уже другой продукт и другой winner set. Для текущего кейса сценарий не доказывает достижимость EBITDA-порога. [T2]
- Вывод: **FAIL**. [T2]

## Risks
- Сильный локальный substitute set: Usedesk и другие helpdesk/omnichannel сервисы уже покрывают значимую часть боли дешевле и ближе к рынку РФ. [T2]
- Узкий buyer universe именно для Salesforce-first стеков в РФ. [T2]
- Длинный enterprise sales cycle и высокая интеграционная нагрузка. [T2]
- Mandatory demand endpoint недоступен, поэтому нет даже позитивного внутреннего сигнала, который мог бы компенсировать слабый market-fit. [T2]

## Verdict for P4
- **P4 verdict**: **REJECTED (early)**.
- Обоснование: общий рынок helpdesk automation существует и платит, но в РФ спрос на `Salesforce Agentforce IT service adoption` слишком узок; одновременно ни project, ни retainer, ни reseller, ни Telegram-adjacent сценарий не дают надёжного прохода через **500 тыс. ₽ EBITDA/мес**. [T2]
- Следствие: кейс не продолжаем в P5-P7, оформляем reject на P4. [T2]

Sources: T1=2, T2=10, T3=0. Primary evidence basis: T2.
