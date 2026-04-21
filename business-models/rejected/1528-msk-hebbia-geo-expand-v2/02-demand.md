# 02-demand

## Demand validation summary
- **Продукт**: Hebbia как AI-native analyst workspace для investment banking, due diligence, data room review, memo drafting и document comparison.
- **Итог по спросу в РФ**: **LOW**, но не нулевой. Прямой keyword-demand по RU слабый, зато есть узкая enterprise-боль у M&A advisory, инвестбанков, Big Law и corpdev-команд. Обязательный endpoint дал: `Hebbia` = **LOW / 15**, `investment banking ai` = **LOW / 3**, `virtual data room` = **LOW / 15**. [T2: internal demand endpoint]
- **Решение по гейту**: **не отклонять на P4**. Массового self-serve спроса нет, но Profit Gate проходит в enterprise / on-prem / managed-deal-room сценарии при 4-6 платящих клиентах. [T1][T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=Hebbia` → **LOW**, score **15**; Google Trends RU = 0, Habr = 2, Yandex suggest = 100, HH = 0. Это означает слабую известность бренда, но наличие поисковых хвостов. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20ai` → **LOW**, score **3**; HH = 10, остальной спрос слабый. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=virtual%20data%20room` → **LOW**, score **15**; Yandex suggest = 100. В РФ люди ищут категорию VDR, но не готовое AI-решение под бренд Hebbia. [T2: internal demand endpoint]

### 2) Russia demand proxies
- В реестре Банка России на 20.04.2026 числится **252 брокера**, **271 дилер** и **156 инвестиционных советников**. Это не равно TAM продукта, но подтверждает наличие нескольких сотен regulated финансовых организаций, где есть workflows с инвестиционным анализом, сделками и документарной проверкой. [T1: Банк России, https://www.cbr.ru/vfs/finmarkets/files/supervision/list_brokers.xlsx ; https://www.cbr.ru/vfs/finmarkets/files/supervision/list_dealers.xlsx ; https://www.cbr.ru/vfs/finmarkets/files/supervision/List_is.xlsx]
- AK&M оценил рынок M&A в РФ за 2025 год в **3,52 трлн ₽** и **536 сделок**, что подтверждает сохраняющийся объём транзакционной активности, на который может лечь VDR / DD automation. [T2: https://www.akm.ru/news/obem_rynka_sliyaniy_i_pogloshcheniy_rossii_v_2025_godu_vyros_na_2_do_3_52_trln_rubley/]
- Kept отмечает, что в 2025 году на российском M&A-рынке было **499 сделок** на **$42,2 млрд**, при этом активность поддерживали внутренние корпораты и private capital. Это независимая проверка того, что рынок сделок в РФ жив, хотя и уже, чем глобальный. [T2: https://kept.ru/insights/articles/rossiyskiy-rynok-sliyaniy-i-pogloshcheniy-itogi-2025-goda/]
- Поиск по hh.ru по категориям `due diligence`, `M&A`, `investment analyst`, `corporate finance` стабильно показывает десятки релевантных вакансий в Москве и Санкт-Петербурге, а internal demand endpoint для `investment banking ai` видит **10 вакансий**. Это подтверждает существование оплачиваемой ручной функции, которую продукт может ускорять. [T1: HH.ru fact of live job demand; T2: internal demand endpoint]

## Competitive pricing and WTP

### 1) Реальные конкуренты с ценами
- **FirmRoom**: тарифы от **$395/мес** (Starter), **$695/мес** (Standard), **$1,295/мес** (Premium), Enterprise custom. По курсу ЦБ на 20.04.2026 это примерно **30 тыс. ₽ / 53 тыс. ₽ / 98 тыс. ₽ в месяц**. [T2: https://firmroom.com/pricing/ ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]
- **SecureDocs Virtual Data Room**: от **$250/мес** и **$400 flat fee** за подготовку, то есть около **19 тыс. ₽/мес** и **30 тыс. ₽** setup. [T2: https://www.securedocs.com/pricing ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]
- **Drooms**: pricing начинается от **€1,900 в месяц за проект**, то есть около **170 тыс. ₽/мес** по курсу ЦБ. [T2: https://drooms.com/pricing/ ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]
- **LegalScan (РФ)**: от **80 тыс. ₽/мес**; позиционируется как AI legal review для договоров и комплаенса. Это важный локальный price anchor для русскоязычного рынка документов. [T2: https://www.legalscan.ai/]

### 2) Willingness to pay
- Сам факт того, что global VDR vendors продают продукт в диапазоне **19 тыс. ₽-170 тыс. ₽/мес** за room / проект, а локальный RU legal-AI сервис ставит цену **80 тыс. ₽/мес**, доказывает, что рынок платит за снижение времени ревью и безопасный обмен документами. [T2]
- Для Hebbia-подобного продукта WTP выше, чем у простого VDR, только если продаётся не просто storage, а **ускорение analyst-hours, memo drafting, cross-doc comparison и question answering по data room**. Тогда price point **300-900 тыс. ₽/мес** выглядит достижимым в enterprise-сегменте, но это уже inference, а не публично подтверждённый прайс. [T2 + inference]
- [Спекуляция] Для pure self-serve бота без VDR, audit trail и on-prem контуров рынок в РФ вряд ли готов платить существенно выше **30-80 тыс. ₽/мес**. [T3-supported-by-T2]

## Telegram bots / services in RU
- Проверка RU web / Telegram / TGStat-поиска не выявила сильных специализированных Telegram-ботов именно под **investment banking due diligence / VDR AI**. [T2]
- В РФ есть adjacent legal-AI и document-review сервисы, но они в основном поставляются как веб-продукт, а не как secure Telegram workflow. Это снижает риск мгновенного bot-led commodity pressure, но и подтверждает, что рынок требует web/on-prem, а не мессенджер. [T2]
- Вывод: Telegram не является главным каналом доставки ценности в этой категории; максимум, это уведомления и Q&A-слой, а не ядро продукта. [T2]

## Market sizing

### Логика сегмента
- Адресуем не все финансовые организации, а только команды, у которых реально есть M&A, DD, data room review, IC memo и многодокументный анализ: инвестбанки, corpdev крупных корпораций, Big Law, transaction services, PE/VC и debt advisory. [T1][T2]

### Top-down
- **TAM (мир)**: глобальный рынок VDR оценивается примерно в **$2,71 млрд**. По курсу ЦБ это около **206,1 млрд ₽**. Источник не Tier-1, поэтому использовать как верхний ориентир, а не как опорную точку. [T3: https://www.grandviewresearch.com/industry-analysis/virtual-data-room-market-report ; T1 FX]
- **TAM (РФ)**: берём рынок M&A РФ **3,52 трлн ₽** и применяем адресуемую software+workflow долю **0,015%** для DD/VDR/AI-automation слоя. Получаем **528 млн ₽**. Это допущение калибровано на публичных прайсах VDR и на том, что software spend в сделках очень мала относительно notional deal value. [T2 + inference]
- **SAM (РФ)**: берём TAM РФ **528 млн ₽** и применяем segment fit **60%**, так как Hebbia релевантна не всем сделкам, а в первую очередь upper mid-market / крупным advisory workflows. Получаем **317 млн ₽**. [T2 + inference]
- **SOM Y1**: **30 млн ₽**, что соответствует примерно 5 enterprise клиентам с ARR ~6 млн ₽. [T2 + inference]
- **SOM Y3**: **72 млн ₽**, что соответствует примерно 12 enterprise клиентам. [T2 + inference]

### Bottom-up
- **Total buyers**: используем базу из regulated finance + transaction advisors. Из 252 брокеров и 156 инвестсоветников только часть реально ведёт сложные сделки; добавляем крупные банки, top law / transaction firms и corpdev-команды. Рабочая база для TAM = **180 организаций**. [T1 + T2 + inference]
- **% with need**: только примерно **30%** из этой базы регулярно сталкиваются с data room / DD / memo-heavy workload. Получаем **54 активных buyers**. [T1 HH + T2 market reports + inference]
- **ARR avg**: ориентир **6 млн ₽/год** на клиента, то есть **500 тыс. ₽/мес**. Это выше обычного VDR, но ниже стоимости 2-3 сильных аналитиков / юристов и соответствует enterprise-only сценарию. [T2 competitor anchors + inference]
- **SAM bottom-up** = 54 × 6 млн ₽ = **324 млн ₽**.
- **SOM bottom-up Y1** = 5 клиентов × 6 млн ₽ = **30 млн ₽**.
- **SOM bottom-up Y3** = 12 клиентов × 6 млн ₽ = **72 млн ₽**.

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 206,1 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 528 млн ₽ [T2] | 1,08 млрд ₽ [T1+T2+inf] | diff 2,0x, bottom-up шире, т.к. считает весь buyer universe, а top-down привязан к активным сделкам | **528 млн ₽** |
| SAM (РФ) | 317 млн ₽ [T2+inf] | 324 млн ₽ [T1+T2+inf] | diff 2,2%, оценки согласуются | **317 млн ₽** |
| SOM Y1 | 30 млн ₽ | 30 млн ₽ | diff 0% | **используем 30 млн ₽** |
| SOM Y3 | 72 млн ₽ | 72 млн ₽ | diff 0% | **используем 72 млн ₽** |

### 10 реальных buyers для bottom-up
1. Газпромбанк
2. Sber CIB
3. Альфа-Банк
4. Совкомбанк
5. БКС КИБ
6. Ренессанс Капитал
7. АТОН
8. Kept
9. Технологии Доверия
10. ДРТ

Комментарий: этот список нужно перенести как основу для P7 GTM-10-targets. [T2]

### Sanity checks
- Расхождение top-down и bottom-up по SAM меньше 3x, пересборка не требуется.
- SOM Y1 = 30 млн ₽, то есть **9,5%** от preferred SAM 317 млн ₽. Это агрессивно, но всё ещё в допустимом диапазоне <10%. 
- При среднем deal cycle **6-9 месяцев** закрыть 5 enterprise клиентов за год тяжело, но реалистично только при founder-led sales и узком списке аккаунтов. [T2]

## Profit Gate

### Сценарий A, self-serve bot / light SaaS
- Цена: **30-80 тыс. ₽/мес**.
- Для EBITDA 500 тыс. ₽/мес потребуется слишком много клиентов при слабом прямом спросе и дорогом enterprise onboarding.
- **Вердикт**: fail. [T2]

### Сценарий B, team workspace для advisory / legal
- Цена: **150-300 тыс. ₽/мес**.
- Gate достижим только при 10-15 клиентах и хорошем gross margin, но рынок в РФ для такого middle tier узкий.
- **Вердикт**: borderline / слабый. [T2]

### Сценарий C, enterprise / on-prem / managed deal room
- Цена: **500-900 тыс. ₽/мес** плюс setup **1-3 млн ₽**.
- При 4-6 клиентах ARR выходит на **24-54 млн ₽/год**; даже при небольшой delivery-команде можно получить **EBITDA > 500 тыс. ₽/мес**.
- **Вердикт**: pass. Это единственный сценарий, на котором кейс инвестируемо выглядит в РФ. [T2 + inference]

## Verdict for P4
- **Demand = LOW**, но не zero.
- **Profit Gate = PASS ONLY IN NARROW ENTERPRISE WEDGE**.
- Поэтому **ранний reject не применяем**. Кейс стоит нести дальше только как enterprise-only thesis: AI workspace для high-stakes DD / M&A / corpfin команд, с secure deployment и очень узким ICP. 

Sources: T1=6, T2=12, T3=1. Primary evidence basis: T2.

## Market Pulse
> Market Pulse 2026-04-20: растущий интерес.

> Market Pulse 2026-04-21: растущий интерес.
