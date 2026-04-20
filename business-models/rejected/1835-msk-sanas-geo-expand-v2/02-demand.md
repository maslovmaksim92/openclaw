# 02-demand

## Demand validation summary
- **Продукт**: Sanas, real-time Accent Translation / Language Translation / Noise Cancellation для контакт-центров и voice-heavy customer support. Компания пишет, что в 2025 году adoption превысил **750 000 пользователей globally**, а в 2024 году продуктом пользовались **30 000+ contact center agents**. [T2: https://www.sanas.ai/about-us]
- **Итог по спросу в РФ**: **LOW**. Обязательный endpoint `multi-demand` по релевантным запросам вернул LOW: `accent translation contact center` = **LOW / score 0**, `голосовой перевод колл-центр` = **LOW / score 3**, `смягчение акцента операторов` = **LOW / score 0**. [T2: internal demand endpoint]
- **Решение по гейту**: **EARLY REJECT**. При низком прямом спросе в РФ и отсутствии локально подтвержденного enterprise WTP Profit Gate не проходит ни в consumer Telegram, ни в SMB SaaS, ни в enterprise-сценарии. [T1][T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=accent%20translation%20contact%20center` → **LOW**, score **0**; HH = 0, Google Trends RU = 1, Yandex suggest = 2. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=%D0%B3%D0%BE%D0%BB%D0%BE%D1%81%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BF%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4%20%D0%BA%D0%BE%D0%BB%D0%BB-%D1%86%D0%B5%D0%BD%D1%82%D1%80` → **LOW**, score **3**; HH = 38, Habr = 2, Yandex suggest = 2. Это говорит скорее о существовании общей темы voice/translation, чем о сформированном category pull именно под accent translation для контакт-центров. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%BC%D1%8F%D0%B3%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B0%D0%BA%D1%86%D0%B5%D0%BD%D1%82%D0%B0%20%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BE%D0%B2` → **LOW**, score **0**. [T2: internal demand endpoint]

### 2) Russia demand proxies
- По данным «ТМТ Консалтинг» в пересказе MANGO OFFICE, российский рынок облачных контакт-центров в 2025 году составит около **3,5 млрд ₽**, а сама платформа MANGO OFFICE обслуживает **50 000+** компаний и госорганизаций. Это подтверждает существование базовой CCaaS-инфраструктуры, но не доказывает отдельный сформированный спрос на accent-translation layer. [T2: https://www.mango-office.ru/journal/tidings/mango-office-vozglavila-rossiyskiy-rynok-oblachnykh-kontakttsentrov/]
- По релевантным HH-сигналам ниша существует только как крайний edge-case: в `multi-demand` запрос `голосовой перевод колл-центр` дал **38 вакансий**, однако это общий voice/translation proxy, а не доказательство бюджета именно под accent conversion. [T1/T2: hh.ru via internal demand endpoint]
- В РФ есть компании с реальной иностранной voice-коммуникацией, но они концентрируются в нескольких вертикалях: travel/hospitality, private healthcare, premium service, outsourcing/BPO. Это **инференс** из клиентских примеров MANGO OFFICE и наблюдаемого найма multilingual support roles. [T2 inference from MANGO + HH proxies]

### 3) Global/category demand
- Sanas показывает, что глобально категория monetizes: в 2025 году у компании появился стратегический инвестор Teleperformance, а adoption превысил **750 000 пользователей**. [T2: https://www.sanas.ai/about-us]
- В customer story Teleperformance Sanas утверждает **22% рост CSAT**, **37,5% снижение AHT**, **14% improvement in FCR**, а также то, что Samsung запросил дополнительные лицензии после успешного запуска в TP India. Это прямой признак реального enterprise WTP на глобальном рынке. [T2: https://www.sanas.ai/customer-stories/tp]
- Глобальный рынок call center AI software оценивается в **$1,99 млрд** в 2024 году и должен расти примерно на **23,8% CAGR** до 2030 года. Для Sanas это релевантный верхнеуровневый proxy, но для РФ это лишь косвенный ориентир. [T2: https://www.marketsandmarkets.com/Market-Reports/call-center-ai-market-29862374.html]

## Competitor landscape with prices

| Конкурент | Что продает | Цена | Вывод для кейса |
|---|---|---:|---|
| Krisp Call Center AI | шумоподавление, accent conversion, voice translation add-on | **от $10/agent/mo** для call center core, то есть около **760 ₽/agent/mo** по курсу ЦБ РФ на 18.04.2026; meeting tiers: **$16/mo** или **$8/mo annual** для core, **$30/mo** или **$15/mo annual** для advanced [T1][T2] | Низкий price floor на per-seat utility layer. Это давит вниз на standalone pricing Sanas-like продукта в РФ. |
| VoicePing | voice translation для meetings/events | annual small plan **$41.25/mo** за 450 минут, **$82.50/mo** за 800 минут, **$165/mo** за 2000 минут; premium **$330/mo**; enterprise **$9.90/user/mo** [T2] | Видно, что рынок monetizes через usage/minutes и events, а не через дорогой always-on contact-center layer. |
| TranslateBot (Telegram) | перевод голоса и speech-to-text в Telegram | **$3.95/mo** Active или **$10/mo** maximum intensive usage [T2] | Consumer TG-рынок в разы дешевле enterprise contact-center economics. |
| Speakly Voice Bot | Telegram voice translator | Basic **$35.99/год** или Pro **$89.99/год** [T2] | Еще один сигнал, что массовый voice-translation спрос в Telegram низкочековый и не поддерживает фондовый SaaS-кейс. |

**Курс для перевода в ₽**: USD = **76,0535 ₽** по данным Банка России на **18 апреля 2026 года**. [T1: https://www.cbr.ru/currency_base/daily/]

## Telegram bots/services in Russia
- Telegram как consumer-канал уже занят: TranslateBot продает перевод голоса и speech-to-text прямо в Telegram по **$3.95–10/мес**. [T2: https://translatebot.io/]
- Speakly продает Telegram voice translation с бесплатным tier и подписками **$35.99/год** и **$89.99/год**. [T2: https://speakly.bot/ru/]
- Внутренний `multi-demand` не показывает сколько-нибудь заметного Telegram pull именно под `accent translation contact center`: в блоке telegram subscribers в обязательных запросах стоит **0**. [T2: internal demand endpoint]
- **Вывод**: в РФ/Telegram есть consumer utility use-case для перевода голоса, но нет убедимых признаков, что Telegram является каналом для дорогого B2B accent-translation продукта в контакт-центрах. [T2]

## WTP (willingness to pay)
- **Глобально WTP подтвержден**: кейс TP показывает внедрение на крупном enterprise-контуре и расширение лицензий после эффекта на CSAT/AHT/FCR. Это хороший глобальный proof-of-budget. [T2: https://www.sanas.ai/customer-stories/tp]
- **В РФ прямого WTP-доказательства нет**: я не нашел локальных кейсов, где российская компания публично платила за accent conversion для операторов. Следовательно, перенос global WTP в РФ является **инференсом**, а не фактом. [T2 inference]
- **Низкий consumer WTP виден в Telegram**: $3.95–10/мес у TranslateBot и <$90/год у Speakly. [T2]
- **Возможный enterprise WTP** в РФ мог бы идти из бюджета контакт-центра, CX или BPO-оператора, если продукт реально улучшает CSAT и AHT. Но без локальных reference customers это остается гипотезой. [T2 inference from TP story + RU market structure]

## Market sizing

### Assumptions
- **TAM world**: беру глобальный рынок call center AI software **$1,99 млрд** как наиболее близкий внешний top-down proxy. По курсу ЦБ РФ это около **151,3 млрд ₽**. [T1+T2]
- **TAM RF top-down**: российский рынок CCaaS в 2025 году около **3,5 млрд ₽**. Для Sanas-подобного слоя беру только **10%** этого spend как voice translation / accent / speech enhancement overlay. Получаю **350 млн ₽** TAM РФ. Это **оценка-инференс**. [T2]
- **Bottom-up buyer universe**: из **50 000+** клиентов MANGO OFFICE адресуемы только организации с заметной долей multilingual voice interactions. Консервативно беру **150 компаний** (0,3% базы) как рабочий buyer universe. Это узкий сегмент, а не весь рынок. [T2 inference]
- **ARR avg**: для РФ считаю **1,8 млн ₽/год** на клиента, то есть **150 тыс. ₽/мес**. Это выше consumer bots, но ниже тяжелого enterprise deployment. [T2 inference from competitor prices]
- **% with need**: **100%** в bottom-up уже заложено отбором buyer universe; это список только тех компаний, у кого multilingual voice-операции хотя бы теоретически есть. [T2 inference]

### GTM-10 real buyers for RF expansion
1. ВкусВилл. [T2: MANGO customer list]
2. М.Видео-Эльдорадо. [T2: MANGO customer list]
3. Роза Хутор. [T2: MANGO customer list]
4. VALO. [T2: MANGO customer list]
5. Гатчинская клиническая межрайонная больница. [T2: MANGO customer example]
6. Ростелеком Контакт-центр. [T2: official company site / obvious contact-center operator, https://www.rtkit.ru/]
7. Voxys. [T2: official company site, https://www.voxys.ru/]
8. Neovox. [T2: official company site, https://neovox.ru/]
9. Class Assist. [T2: official company site, https://class-assistance.com/]
10. GMS Clinic. [T2: official company site, https://www.gmsclinic.ru/]

### Top-down calculation
- **TAM world** = **151,3 млрд ₽**. [T1+T2]
- **TAM RF** = **3,5 млрд ₽ × 10%** = **350 млн ₽**. [T2]
- **SAM RF** = TAM × **80% segment fit** (не весь overlay spend доступен новому игроку) = **280 млн ₽**. [T2 inference]
- **SOM Y1** = SAM × **3%** = **8,4 млн ₽**. [T2]
- **SOM Y3** = SAM × **10%** = **28,0 млн ₽**. [T2]

### Bottom-up calculation
- **Total buyers** = **150 компаний**. [T2 inference]
- **% with need** = **100%**, потому что universe уже отфильтрован по multilingual voice-use-case. [T2 inference]
- **ARR avg** = **1,8 млн ₽/год**. [T2 inference]
- **SAM bottom-up** = 150 × 1,8 млн ₽ = **270 млн ₽**. [T2]
- **SOM Y1 bottom-up** = 270 млн ₽ × **3%** = **8,1 млн ₽**. [T2]
- **SOM Y3 bottom-up** = 270 млн ₽ × **10%** = **27,0 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **151,3 млрд ₽** [T1+T2] | — | — | top-down |
| TAM (РФ) | **350 млн ₽** [T2] | — | TAM РФ считаю только top-down, bottom-up начинаю с buyer universe | top-down |
| SAM (РФ) | **280 млн ₽** [T2] | **270 млн ₽** [T2] | diff ≈ **3,7%**, оценки близки, значит сегмент выбран последовательно | **270 млн ₽** |
| SOM Y1 | **8,4 млн ₽** | **8,1 млн ₽** | diff ≈ **3,6%**, беру lower bound | **8,1 млн ₽** |
| SOM Y3 | **28,0 млн ₽** | **27,0 млн ₽** | diff ≈ **3,7%**, беру lower bound | **27,0 млн ₽** |

**Sanity check**:
- Разница между top-down и bottom-up по SAM меньше 3x, пересборка не нужна. [T2]
- SOM Y1 < 10% SAM, значит допущение реалистично. [T2]
- При ARR 1,8 млн ₽/год SOM Y1 означает около **4-5 клиентов** в первый год. С учетом enterprise sales cycle 6-9 месяцев это уже верхняя граница реализма для новой категории без локальных references. [T2 inference]

## Profit Gate: can EBITDA >= 500K ₽/month be achieved?

### Scenario A: Telegram / consumer bot
- Цена: **300-760 ₽/мес** на пользователя по TranslateBot / Speakly / Krisp utility comparables. [T1+T2]
- Чтобы получить хотя бы **500 тыс. ₽ EBITDA/мес**, нужен многотысячный платящий consumer volume. Обязательный demand endpoint такого объема не поддерживает. [T2]
- **Вердикт**: FAIL. [T2]

### Scenario B: SMB / mid-market SaaS add-on for call centers
- Цена: **150 тыс. ₽/мес** на клиента как рабочее допущение. [T2]
- При gross margin ~75% и минимальной локальной команде/инфраструктуре с fixed opex около **2,0 млн ₽/мес** нужно примерно **17-18 клиентов**, чтобы выйти на **EBITDA > 500 тыс. ₽/мес**. Это уже **30+ млн ₽ ARR**. [T2 inference]
- На рынке с SAM около **270 млн ₽**, LOW-demand сигналами и без локальных кейсов такой масштаб для нового standalone игрока выглядит малореалистичным. [T2]
- **Вердикт**: FAIL. [T2]

### Scenario C: enterprise high-touch deployment
- Цена: **250-300 тыс. ₽/мес** на клиента, если продавать как managed rollout для BPO/large contact centers. Это допущение уже выше прямых market benchmarks и требует сильной интеграции. [T2 inference]
- Даже при **300 тыс. ₽/мес** нужно около **10 клиентов**, чтобы пройти **500 тыс. ₽ EBITDA/мес** после локализации, sales, support и inference costs. [T2 inference]
- Для РФ я не вижу подтвержденного local WTP на 10 enterprise logos именно под accent conversion. Global proof есть, local proof нет. Значит сценарий остается теоретическим, но не доказанно достижимым. [T2]
- **Вердикт**: FAIL / not proven achievable. [T2]

**Итог по Profit Gate**: **FAIL**. Теоретическая возможность существует только в узком enterprise сценарии, но она не подтверждена локальным спросом, локальными references и реалистичным pipeline. По правилам фонда это недостаточно, чтобы засчитать gate как пройденный. [T2]

## Risks
- Категория в РФ не оформлена, поиск почти нулевой. [T2]
- Consumer Telegram-рынок уже приучен к очень низкому чеку. [T2]
- Enterprise rollout требует локализации, интеграций и reference logos, которых в РФ не видно. [T2]
- Продукт легко превращается в feature/add-on внутри CCaaS, а не в отдельную компанию. [T2]

## Verdict for P4
- **Demand = LOW**. [T2]
- **Profit Gate = FAIL**. [T2]
- Следовательно, кейс подлежит **EARLY REJECT** на P4: написать verdict и перевести в rejected. [T2]

## Market Pulse
> Market Pulse 2026-04-20: спрос в РФ слабый, локальный high-ticket WTP не доказан.

Sources: T1=2, T2=18, T3=0. Primary evidence basis: T2, с T1 для FX conversion и HH-derived demand proxy.