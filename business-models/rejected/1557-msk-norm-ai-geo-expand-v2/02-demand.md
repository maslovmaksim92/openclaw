# 02-demand

## Demand validation summary
- **Продукт**: Norm AI, Legal & Compliance AI для regulated content review, supervisory AI, disclosure/comms review, DDQ/RFP automation и contract review. Компания заявляет, что ее клиенты управляют **$30T AUM**, а продукт уже сделал **13,947,967** compliance determinations. [T2: https://www.norm.ai/]
- **Итог по спросу в РФ**: **LOW** по прямому keyword-demand, но **не нулевой** по бюджету и боли у крупных регулируемых организаций. Обязательный endpoint `multi-demand?keyword=Norm AI` вернул **LOW / score 15**. [T2: internal demand endpoint]
- **Решение по гейту**: **не отклонять на P4**. Demand слабый, но Profit Gate проходит в enterprise-only сценарии, если продавать как замену части комплаенс-FTE и ускорение регуляторных согласований. [T1][T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=Norm%20AI` → **LOW**, score **15**; Google Trends RU = 0, Habr = 2, HH = 0, Yandex suggest = 100. Это означает отсутствие сформированного массового спроса по бренду, но наличие поисковых хвостов и узнаваемости термина. [T2: internal demand endpoint]

### 2) Russia demand proxies
- На 1 января 2026 года в РФ действовало **306 банков** и **46 НКО**, то есть только банковский контур дает сотни потенциальных regulated buyers. [T1: Банк России, https://cbr.ru/banking_sector/]
- На 1 января 2026 года в РФ действовало **129 страховых организаций**, **60 страховых брокеров** и **15 обществ взаимного страхования**. Это еще один слой покупателей с высокой нормативной нагрузкой. [T1: Банк России, https://www.cbr.ru/insurance/]
- На конец IV квартала 2025 года Банк России насчитывал **497 профессиональных участников рынка ценных бумаг**. [T1: Банк России, https://www.cbr.ru/securities_market/]
- hh.ru показывает живой найм под compliance-функции: по запросу `compliance officer` в Москве индексируется **49 вакансий**; отдельные роли публикуются с зарплатами **150 тыс. ₽/мес**, **200 тыс. ₽/мес** и **230 тыс. ₽/мес**. Это прямое подтверждение того, что компании уже тратят деньги на ручной compliance capacity. [T1: https://hh.ru/vacancies/compliance_officer ; https://hh.ru/vacancy/129357114 ; https://hh.ru/vacancies/komplaens-menedzher ; https://hh.ru/vacancy/128031598]
- Банк России отдельно ужесточает требования к системно значимым банкам, например по liquidity coverage risk и recovery plans с 2025–2026 годов, что увеличивает нагрузку на внутренние legal/compliance команды. [T1: https://www.cbr.ru/eng/press/event/?id=27989 ; https://www.cbr.ru/eng/press/event/?id=28066]

### 3) Global/category demand
- По данным Grand View Research, глобальный рынок **RegTech** в 2025 году оценен в **$24.34 млрд**, а сегмент **regulatory intelligence** отдельно в **$2.65 млрд**. Для Norm AI это важный сигнал, что категория уже существует и финансируется, даже если в РФ она еще не оформилась как поисковый спрос. [T2: https://www.grandviewresearch.com/industry-analysis/regulatory-technology-market ; https://www.grandviewresearch.com/horizon/statistics/regtech-market/application/regulatory-intelligence/global]
- У самой Norm AI позиционирование заточено под крупнейшие институты, а не SMB, поэтому слабый брендовый спрос в RU не равен отсутствию enterprise-budget. [T2: https://www.norm.ai/]

## Competitor landscape with prices

| Конкурент | Что продает | Цена | Вывод для Norm AI |
|---|---|---:|---|
| VComply PRO GRC Suite | GRC/compliance workflow automation | от **$1,000/мес** [T2] | floor для корпоративного compliance SaaS, даже без глубокой Legal AI логики. |
| ComplyCloud AI Compliance | AI Act / AI compliance workflow | от **€119/мес** [T2] | low-end/self-serve ориентир, но для малого периметра, до 10 IT systems. |
| Sengol Comply | AI compliance monitoring | от **$249/мес** [T2] | нишевой AI-compliance price point для раннего рынка. |
| hh.ru payroll proxy | ручной труд compliance-специалистов | **150–230 тыс. ₽/мес** за одного специалиста [T1] | если продукт экономит 1–2 FTE, enterprise WTP легко уходит в 2–4 млн ₽ ARR. |

**Источники по ценам**: VComply pricing page `modules start at $1,000/mo`. [T2: https://www.v-comply.com/pricing/] ComplyCloud pricing page показывает `AI Compliance from €119/month`, а core compliance tiers `€310–€610/month`. [T2: https://www.complycloud.com/pricing/] Sengol pricing page показывает `Comply from $249/month`, а platform tiers `$49/$149`. [T2: https://www.sengol.ai/products/compliance/pricing ; https://www.sengol.ai/pricing]

## Telegram bots/services in Russia
- В RU Telegram есть крупная AI-дистрибуция как канал продаж и привычка платить внутри мессенджера: Hi, AI! заявляет **35 млн пользователей**, **1 млн DAU** и несколько крупных AI-ботов. Это подтверждает, что Telegram в РФ является реальным каналом AI-distribution, хотя не enterprise procurement channel. [T2: https://hiai.digital/]
- Есть нишевые domain bots с платной моделью. Например Eggella продает Telegram-бота `ИИ Строитель`, который работает с СП/СНиП/ГОСТ и берет **50 ₽ за 16 сообщений** или **100 ₽ за 35 сообщений**. Это слабый, но полезный сигнал, что пользователи в РФ готовы платить за специализированный нормативный AI через Telegram. [T3, supporting only: https://eggella.ru/]
- Есть отраслевые сообщества под legal/compliance: канал `Compliance practice` с ботом обратной связи `@CompliancePBot` и аудиторией около **9.2K**, а также канал `ИИ & Право` примерно на **5.2K** участников. [T2/T3: https://telega.io/analytics/compliance_practice/card/telegram ; https://nicegram.app/hub/group/ai_and_law_rus]
- **Вывод**: Telegram в РФ полезен как **top-of-funnel / education / lead-gen**, но не как основной delivery-модуль для enterprise-grade Norm AI. Для продаж нужен enterprise outbound в банки, страховщики и крупные инвесткомпании. [T2]

## WTP (willingness to pay)
- Базовая готовность платить подтверждается уже существующими spend lines: компании платят **150–230 тыс. ₽/мес** за одного compliance/FIU/KYC специалиста, а также держат отдельные legal/compliance команды. [T1: hh.ru]
- При fully loaded cost 1 FTE на уровне примерно **200–300 тыс. ₽/мес** с налогами и overhead продукт, который экономит хотя бы 1.0–1.5 FTE или сокращает turnaround согласований, может обосновать **2–4 млн ₽ ARR** на одного крупного клиента. Это **вывод-оценка**, а не прямая котировка. [T1+T2 inference from hh.ru pricing floors and competitor benchmarks]
- VComply, ComplyCloud и Sengol показывают, что compliance automation уже monetizes globally даже в low-end сегменте. Для Norm AI, который продается глубже и в enterprise, ценовой коридор должен быть выше low-end SaaS и ближе к high-touch annual contracts. [T2]
- Дополнительный WTP proxy: Norm AI продает не generic LLM access, а снижение regulatory risk и ускорение review cycles, то есть бюджет может идти из legal/compliance/marketing approval budget, а не только из IT. Это улучшает шанс на сделку у крупных regulated firms. [T2: https://www.norm.ai/]

## Market sizing

### Assumptions
- **TAM world**: использую глобальный рынок RegTech **$24.34 млрд** в 2025 как широкий ceiling и сегмент regulatory intelligence **$2.65 млрд** как более близкий functional proxy для Norm AI. [T2]
- **TAM RF top-down**: беру российский контур регулируемых финансовых организаций как proxy для первого реального beachhead: 306 банков + 46 НКО + 129 страховщиков + 60 страховых брокеров + 15 ОВС + 497 профучастников РЦБ = **1,053 организаций**. [T1]
- **ARR avg top-down**: консервативно **1.2 млн ₽/год** на одну организацию как blended entry price для compliance automation. Это ниже enterprise-only сценария и ближе к усредненному рынку. [T1+T2 inference]
- **Segment fit for SAM**: только ~**30%** рынка реалистично адресуемы на старте, поскольку Norm AI нужен прежде всего организациям с большим документооборотом, маркетинговыми approval-потоками и зрелыми legal/compliance командами. [T1+T2 inference]
- **Bottom-up buyers**: беру **10 реальных buyers** как ядро для GTM-10 и экстраполирую на похожие крупные группы. [T1]

### GTM-10 real buyers for RF expansion
1. Сбербанк [T1]
2. ВТБ [T1]
3. Газпромбанк [T1]
4. Альфа-Банк [T1]
5. Т-Банк [T1]
6. Совкомбанк [T1]
7. Банк ДОМ.РФ [T1]
8. Россельхозбанк [T1]
9. АльфаСтрахование [T1/T2]
10. СберСтрахование [T1/T2]

### Top-down calculation
- **TAM RF** = 1,053 организаций × 1.2 млн ₽ ARR = **1.264 млрд ₽**. [T1+T2]
- **SAM RF** = TAM × 30% segment fit = **379 млн ₽**. [T1+T2]
- **SOM Y1** = SAM × 3% realistic capture = **11.4 млн ₽**. [T2]
- **SOM Y3** = SAM × 10% realistic capture = **37.9 млн ₽**. [T2]

### Bottom-up calculation
- **Total buyers** = 173 крупных buyers как рабочий сегмент: 12 системно значимых банков + 129 страховщиков + 32 НПФ/крупных пенсионных контуров. Это не весь рынок, а high-priority ядро. [T1: https://www.cbr.ru/banking_sector/credit/systembanks.html/ ; https://www.cbr.ru/insurance/ ; https://www.cbr.ru/RSCI/]
- **% with need** = 70%, потому что не всем нужен deep legal AI сегодня, но у большинства крупных regulated игроков есть marketing/legal/compliance review load. [T1+T2 inference]
- **ARR avg** = **3.0 млн ₽/год** для enterprise/private-cloud pilot-to-production. [T1+T2 inference]
- **SAM bottom-up** = 173 × 70% × 3.0 млн ₽ = **363.3 млн ₽**. [T1+T2]
- **SOM Y1 bottom-up** = 5% от SAM = **18.2 млн ₽**. [T2]
- **SOM Y3 bottom-up** = 12% от SAM = **43.6 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$24.34B** RegTech, 2025 [T2] | — | — | top-down |
| TAM (РФ) | **1.264 млрд ₽** [T1+T2] | — | bottom-up считаю с уровня SAM, так как список реальных buyers уже filtered | top-down |
| SAM (РФ) | **379 млн ₽** [T1+T2] | **363.3 млн ₽** [T1+T2] | diff ≈ **4.3%**, расхождение небольшое; bottom-up подтверждает, что сегмент выбран адекватно | **363.3 млн ₽** |
| SOM Y1 | **11.4 млн ₽** | **18.2 млн ₽** | diff ≈ **59%**, беру lower bound, так как рынок в РФ еще не category-defined | **11.4 млн ₽** |
| SOM Y3 | **37.9 млн ₽** | **43.6 млн ₽** | diff ≈ **15%**, значения близки | **37.9 млн ₽** |

**Sanity check**:
- Расхождение top-down и bottom-up по SAM меньше 3x, значит sizing не выглядит сломанным. [T1+T2]
- SOM Y1 = 11.4 млн ₽, это около 3–4 enterprise контрактов по 3 млн ₽ ARR или 6–10 более дешевых пилотов. Для года 1 реалистично. [T2]
- При среднем цикле сделки 6–9 месяцев больше 8–10 новых logo за год было бы уже red flag; текущий SOM этого не предполагает. [T2]

## Profit Gate: can EBITDA >= 500K ₽/month be achieved?

### Scenario A: low-touch SaaS / self-serve
- Цена: 50–100 тыс. ₽/мес. [T2/T3 benchmark]
- Нужно 40–60 клиентов для meaningful gross profit. Для РФ-рынка Norm AI это слишком много, category demand не поддерживает. [T2]
- **Вердикт**: FAIL. [T2]

### Scenario B: mid-market compliance SaaS
- Цена: 120–180 тыс. ₽/мес, 15–20 клиентов. [T2]
- Теоретически возможно, но Norm AI слишком high-touch и требует legal engineering. Для mid-market РФ unit economics будут напряженными. [T2]
- **Вердикт**: скорее FAIL / borderline. [T2]

### Scenario C: enterprise / private-cloud / regulated workflow
- Цена: **250–350 тыс. ₽/мес** на клиента, то есть **3–4.2 млн ₽ ARR**. Это согласуется с FTE replacement logic и международными benchmark floors. [T1+T2 inference]
- При **10–12 клиентах** выручка составит **30–50 млн ₽ ARR**. Даже при 70–80% gross margin и lean local team это дает путь к **EBITDA > 500 тыс. ₽/мес**. [T2]
- **Вердикт**: PASS. [T2]

**Итог по Profit Gate**: проходит **только enterprise-only модель**. Если команда попытается идти в self-serve или широкий SMB, кейс почти наверняка сломается. [T2]

## Risks
- В РФ нет сформированной category pull по бренду Norm AI, продажи придется делать через consultative outbound, а не inbound. [T2]
- Требуются глубокая локализация под российское регулирование, язык и внутренние policy engines клиентов. [T1/T2]
- Telegram подтверждает distribution habit, но не снимает длинный procurement cycle в банках и страховщиках. [T2]

## Verdict for P4
- **Demand = LOW**, но **Profit Gate = PASS** в enterprise-only модели. [T2]
- Следовательно, **early reject не нужен**. Кейс должен идти дальше по пайплайну как узкий, high-ticket, execution-heavy expansion thesis. [T2]
- Рекомендация: в следующем этапе считать economics только для enterprise/private-cloud motion и не закладывать массовый SMB funnel. [T2]

## Market Pulse
> Market Pulse 2026-04-20: растущий интерес.

Sources: T1=10, T2=14, T3=2. Primary evidence basis: T1/T2 mixed, with T1 used for buyer universe and labor-cost proxies.
