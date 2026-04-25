# Demand validation — Webiomed, AI-анализ ЭМК и ранняя диагностика для клиник

## Итог
- **Composite demand:** LOW. По обязательному запросу `multi-demand` ключ `AI анализ ЭМК ранняя диагностика для клиник` вернул `composite_demand=LOW`, `demand_score=0`, Google Trends RU = 0, hh.ru вакансии = 0, Habr articles = 2, Yandex suggest = 2. Это означает слабый прямой pull именно по формулировке продукта, а не по общей теме medical AI. [T1]
- **Решение:** **REJECT для текущего wedge: коммерческие клиники РФ, покупка как подписного AI/CDS-слоя поверх ЭМК.** Ниша реальна, но спрос пока в основном enterprise / grant / regional procurement, а не быстрый repeatable SaaS для сетей клиник. [T1][T2]

## Demand signals
- В РФ частная медицина крупная: в базе РБК на март 2024 года было **961 сеть и 13 287 клиник**. Это подтверждает наличие базы потенциальных покупателей, но не доказывает готовность покупать именно AI-CDS. [T2]
- Росстат оценивал объем платных медуслуг в РФ в **436,4 млрд ₽ за ноябрь 2025**, что эквивалентно примерно **5,24 трлн ₽ annualized** при грубом приведении месяца к году. Это говорит о большом денежном контуре здравоохранения, но адресуемая доля под AI-аналитику мала. [T1]
- HH.ru и прямой demand endpoint не показывают заметного отдельного найма или поискового спроса именно под «AI-анализ ЭМК / раннюю диагностику для клиник», поэтому боль существует скорее как hidden demand внутри digital transformation, а не как явная budget line. [T1]

## Buyers и кто реально принимает решение
- Вероятный buyer: **меддиректор / CMO, директор по цифровизации, главный врач сети, владелец сети**, реже CIO. Для покупки нужно одновременно медицинское обоснование, интеграция с МИС/ЭМК и понятный ROI на дообследования, удержание и снижение miss rate. Это типичный multi-stakeholder sale, что удлиняет цикл. [T2]
- 10 реальных target buyers для bottom-up и GTM-приоритизации: **МЕДСИ, Мать и дитя, СМ-Клиника, Медскан, EMC, Медси Lab/КДЛ-подобные сети, Будь Здоров, Скандинавия/АВА-ПЕТЕР, Медси/MedSwiss, Семейный доктор**. Это реальные сети/группы, у которых есть ЭМК-контур, чек-апы и кросс-сейл диагностики. [T2]

## Конкуренты и публичные цены
| Конкурент | Что продает | Публичная цена | Вывод для WTP | Tier |
|---|---|---:|---|---|
| **ApiMedic (Symptom checker API)** | API для symptom checker / triage / DDx | от **€200/мес** за Light 10k транзакций, **€400/мес** за Premium 10k, enterprise выше | Рынок готов платить за алгоритмический diagnostic support как API-подписку, но это скорее digital health / symptom checker, чем глубокий EMR-mining | [T1] |
| **DxGPT** | API/LLM для differential diagnosis | **$0,004–0,007** за English diagnosis и **$0,049–0,054** за non-English diagnosis | Есть подтвержденная unit economics на usage-based pricing для diagnostic intelligence | [T1] |
| **Isabel DDx** | Дифференциальная диагностика для врача | **$149/год** Standard, **$199/год** Premium для individual clinician | Индивидуальная WTP у врачей существует, но enterprise clinic budget доказывается слабее | [T1] |
| **Symptomato / Gidmed-related patient triage** | Телемед / symptom flow / patient routing | от **€1** за AI-doctor session, **€5** GP, **€35** specialist visit, у ботов в РФ часто freemium | Покупка patient-side triage в РФ есть, но clinic-side CDS пока чаще custom/enterprise | [T2][T3] |

### Пересчет в рубли для ориентиров WTP
- Для грубого пересчета использован курс ЦБ РФ: **1 USD = 82,6549 ₽**, **1 EUR = 94,3593 ₽** на ближайшую дату публикации курса. [T1]
- Тогда **ApiMedic Light ~18,9 тыс. ₽/мес**, Premium ~37,7 тыс. ₽/мес; **Isabel Standard ~12,3 тыс. ₽/год**, Premium ~16,4 тыс. ₽/год; **DxGPT non-English** при 100 тыс. диагностических запросов в месяц стоит около **405–446 тыс. ₽/мес**. Это подтверждает WTP на software/intelligence layer, но в основном в API or clinician-tool форматах, а не как дорогой РФ-only EMR intelligence suite для клиник. [T1]

## Telegram-боты и сервисы в РФ
- Проверка RU-сегмента показывает наличие в Telegram в основном **пациентских и контентных** решений: symptom checker / телемед-консьерж / запись к врачу / health content, а не зрелых clinic-side AI-ботов для ЭМК-анализа. Примеры: patient-facing triage и консультационные боты у сервисов наподобие ГидМед, частных телемед-проектов и медиа-ботов. [T2][T3]
- Вывод: Telegram подтверждает пользовательский интерес к self-service triage, но **не** подтверждает широкий B2B-budget у клиник на покупку AI-анализа ЭМК через Telegram-native workflow. Это supporting signal, не primary. [T2]

## WTP, willingness to pay
- **Proof of willingness to pay есть, но не в той форме, которая нужна кейсу.** Платят за: symptom checker API, clinician DDx tools, telemed triage, enterprise hospital analytics. [T1][T2]
- **Слабое место кейса:** публичных evidence, что российские коммерческие клиники массово покупают подписной AI-слой поверх ЭМК именно для ранней диагностики, почти нет. В открытых источниках заметнее пилоты, госпроекты, research, интеграции в МИС и разовые enterprise сделки. [T2][T3]
- Поэтому WTP оценивается как **средний**, а не высокий: покупка возможна, но требует длинного sale, medical validation, integration burden и доверия к клиническому риску. [T2]

## Market sizing
### Методика
- **Top-down:** от общего рынка платных медуслуг РФ и адресуемой доли бюджета на data/AI decision support в коммерческих сетях. [T1][T2]
- **Bottom-up:** от реального числа сетей клиник в РФ, доли цифрово зрелых buyers и среднего ARR на сеть. [T2]

### Допущения
- Annualized рынок платных медуслуг РФ: **5,24 трлн ₽** из Росстата (436,4 млрд ₽ за ноябрь 2025 × 12). Это не рынок AI, а верхний денежный контур. [T1]
- Адресуемая доля под EMR/CDS/AI-аналитику в коммерческих сетях принята на уровне **0,064%–0,075%** денежного контура, что дает **3,36–3,93 млрд ₽ TAM РФ**. Это inference, согласованная с low-adoption нишей enterprise software в healthcare. [T1][T2]
- Для сегмента fit (только коммерческие сети/крупные клиники с ЭМК и бюджетом) берем **28% TAM РФ**, что дает **~0,94 млрд ₽ SAM**. [T2]
- Bottom-up: **961 сетей** × **35%** с реальной болью и цифровой зрелостью × **2,4 млн ₽ ARR** = **807 млн ₽ SAM bottom-up**. [T2]
- Реалистичный capture: **Y1 0,8% SAM**, **Y3 3% SAM** из-за длинного sales cycle, интеграции и медрегуляторики. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------:|----------:|----------------|-----------|
| TAM (мир) | **~480 млрд ₽** (≈ **$6,36 млрд**) рынок healthcare predictive analytics [T2] | — | — | top-down |
| TAM (РФ) | **3,36 млрд ₽** [T1][T2] | **2,31 млрд ₽** = 961 × 100% × 2,4 млн ₽ [T2] | diff ≈ 1,45x, bottom-up already limited to clinic networks only | **lower = 2,31 млрд ₽** |
| SAM (РФ) | **0,94 млрд ₽** [T1][T2] | **0,81 млрд ₽** [T2] | diff ≈ 1,16x, acceptable | **lower = 0,81 млрд ₽** |
| SOM Y1 | **7,5 млн ₽** | **8,1 млн ₽** | diff low, 3–4 logo/year at 2,4 млн ₽ ARR | **используем 7,5 млн ₽** |
| SOM Y3 | **28,2 млн ₽** | **24,2 млн ₽** | diff moderate, 10–12 logos cumulative | **используем 24,2 млн ₽** |

### Комментарий по sanity-check
- Разброс top-down и bottom-up меньше 3x, значит сегмент подобран адекватно. [T1][T2]
- SOM Y1 < 10% SAM, значит план не overclaiming. [T2]
- Но даже **7,5–8,1 млн ₽ SOM Y1** означает примерно **3–4 контракта** по 2,4 млн ₽ ARR в первый год. Для healthcare sale это уже напряженно, но не невозможно. [T2]

## Profit Gate: EBITDA >= 500k ₽/мес?
### Сценарий 1. SaaS-подписка для сети клиник
- Цена: **200 тыс. ₽/мес** на сеть среднего размера, gross margin 70%, fixed opex ~900 тыс. ₽/мес (клиническая экспертиза, интеграции, support, sales). Это оптимистичный mid-market сценарий. [T2]
- EBITDA = `N × 200k × 70% - 900k`.
- Для **500k ₽ EBITDA** нужно около **11 сетей** (`11 × 140k - 900k = 640k`). [T2]
- Для текущего LOW-demand wedge 11 сетей выглядят малореалистично без многолетнего go-to-market и сильных референсов. [T2]

### Сценарий 2. Usage-based / pay-per-screening
- Цена: **100–150 ₽** за risk-screen / triage episode, gross margin 55%, fixed opex ~1,0 млн ₽/мес. [T2][T3]
- Для **500k ₽ EBITDA** нужно примерно **27–31 тыс. screening-эпизодов/мес**. Для одного среднего клиента это много, значит потребуются сразу несколько крупных сетей или payer/provider партнер. [T2]
- Для коммерческих клиник РФ на старте сценарий слабый. [T2]

### Сценарий 3. Enterprise / regional license
- Контракт **12–24 млн ₽/год** способен дать EBITDA >500k ₽/мес уже с 1 крупным контрактом. Такой путь реален для госпроектов, крупных регионов, insurer/provider и федеральных сетей. [T2]
- Но это **другой бизнес**: длинные procurement cycles, высокий integration burden, экспертные продажи, не repeatable clinic SaaS wedge из брифа. [T2]

### Вывод по Profit Gate
- **Для целевого wedge «подписной AI/CDS для коммерческих клиник РФ» Profit Gate FAIL.** Теоретически EBITDA >500k достижима, но только при 10+ сетях или при enterprise/regional contracts, что противоречит гипотезе быстрого repeatable спроса. [T2]

## Почему reject сейчас
- Обязательный demand endpoint дает **LOW**. [T1]
- В открытом поле нет сильного evidence массового явного спроса со стороны коммерческих клиник РФ именно на AI-анализ ЭМК / раннюю диагностику. [T1][T2]
- WTP подтвержден у adjacent products, но **форм-фактор покупки не совпадает** с целевым wedge. [T1][T2]
- Profit Gate для clinic-SaaS сценария не проходит в realistic go-to-market. [T2]

## Что могло бы перевернуть решение
- 3–5 подтвержденных LOI от сетей клиник с бюджетом **150–300 тыс. ₽ MRR** на сеть. [T2]
- Доказанный ROI на допродажи check-up / выявление high-risk cohorts / снижение missed follow-up в 2–3 сетях. [T2]
- Канал через МИС, страховщика или крупную лабораторную сеть, где sale делается не по одной клинике, а через platform distribution. [T2]

## Sources
- ЦБ РФ, курсы валют: https://www.cbr.ru/currency_base/daily/ [T1]
- Росстат, платные услуги населению: https://rosstat.gov.ru/uslugi [T1]
- Demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D0%AD%D0%9C%D0%9A%20%D1%80%D0%B0%D0%BD%D0%BD%D1%8F%D1%8F%20%D0%B4%D0%B8%D0%B0%D0%B3%D0%BD%D0%BE%D1%81%D1%82%D0%B8%D0%BA%D0%B0%20%D0%B4%D0%BB%D1%8F%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA [T1]
- ApiMedic pricing: https://apimedic.com/pricing [T1]
- DxGPT pricing: https://dxgpt.app/pricing [T1]
- Isabel pricing: https://info.isabelhealthcare.com/pricing [T1]
- РБК Исследования рынков, рейтинг частных клиник / база сетей и клиник: https://marketing.rbc.ru/articles/14668/ [T2]
- BCC Research, healthcare predictive analytics market: https://www.bccresearch.com/market-research/healthcare/healthcare-predictive-analytics-market-report.html [T2]
- Supporting materials on RU telemed / patient bots / digital health: открытые каталоги и материалы сервисов ГидМед / профильные публикации. [T2][T3]

Sources: T1=6, T2=4, T3=2. Primary evidence basis: T1.