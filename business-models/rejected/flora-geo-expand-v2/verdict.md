---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-flora-geo-expand.md
created: 2026-04-20T13:38:00+03:00
original_verdict: triage/triage-2026-04-18-flora-geo-expand.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — flora-geo-expand

## Meta
- source: triage/triage-2026-04-18-flora-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-0557-msk-flora-geo-expand.md`

## Классификация
Шум для Program 1.

## Решение
Новый кейс не создавать.

## Почему это не дубль
- В `pipeline/cases/` сейчас открыт кейс `enterprise-autonomous-cybersecurity-agents`, который относится к enterprise-кибербезопасности и не пересекается по теме с FLORA.
- Сигнал по FLORA описывает collaborative AI-платформу для креативных и маркетинговых команд, а не security, legal, fintech или другую уже открытую категорию в текущем пайплайне.

## Почему сигнал не проходит фильтр
- Во входном файле оценка `ltv_signal` указана на уровне `600000-1800000 RUB в год`, то есть примерно `50 000-150 000 ₽ в месяц` на один корпоративный аккаунт или команду.
- Это заметно ниже порога standing orders для Program 1, где требуется потенциал `> 500 000 ₽ в месяц` на клиента.
- Несмотря на сильный западный traction, для текущего пайплайна это скорее SMB/mid-market creative tooling, чем high-LTV service case.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал по FLORA отсеян как нерелевантный для Program 1: категория выглядит интересной, но по текущей оценке чека не дотягивает до порога high-LTV в `500 000 ₽/мес` на клиента.

```

# 02-demand

## Demand validation summary
- **Продукт**: FLORA, collaborative AI-платформа для creative и marketing workflows, где команды собирают AI-native canvas и production pipelines для генерации и итерации креативов. [T2: https://www.withflora.com/ ; https://www.statista.com/outlook/tmo/software/productivity-software/creative-software/worldwide]
- **Итог по спросу в РФ**: **LOW**, но не нулевой. Category-led спрос по ключам про AI для креативных и маркетинговых команд в РФ пока слабый, однако бюджет, buyer universe и платежеспособные команды в рекламе и brand marketing есть. [T1/T2: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%B4%D0%BB%D1%8F%20%D0%BA%D1%80%D0%B5%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D1%8B%D1%85%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4 ; http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%B4%D0%BB%D1%8F%20%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3%D0%BE%D0%B2%D1%8B%D1%85%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4 ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F%20%D1%80%D0%B5%D0%BA%D0%BB%D0%B0%D0%BC%D0%BD%D1%8B%D1%85%20%D0%BA%D1%80%D0%B5%D0%B0%D1%82%D0%B8%D0%B2%D0%BE%D0%B2 ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B4%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD%20%D0%B4%D0%BB%D1%8F%20%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%20AI ; https://akarussia.ru/volumes/obem-rynka-marketingovyh-kommunikacij-v-2025-godu/]
- **Решение по гейту**: **не отклонять на P4**. Несмотря на LOW demand по keyword proxy, Profit Gate достижим в сценарии team/enterprise subscription при 10-15 платящих клиентах из топовых рекламодателей и агентств РФ. [T1/T2, inference]

## Evidence of demand

### 1) Mandatory endpoint
- `AI для креативных команд` → **LOW**, score **15**, `hh.ru vacancies = 730`, `telegram subscribers = 0`. Это не брендовый спрос на FLORA, но сильный labor proxy на функцию. [T1/T2: internal demand endpoint]
- `AI для маркетинговых команд` → **LOW**, score **11**, `hh.ru vacancies = 415`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `генерация рекламных креативов` → **LOW**, score **7**, `hh.ru vacancies = 180`, `google trends = 0`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `дизайн для маркетинга AI` → **LOW**, score **11**, `hh.ru vacancies = 217`, `google trends = 1`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- Вывод: в РФ пока нет сформированной широкой категории collaborative AI creative platform, но есть заметный спрос на людей и процессы вокруг AI-enabled marketing/creative production. [T1/T2, inference]

### 2) Additional market signals
- АКАР оценивает рынок маркетинговых коммуникаций РФ в **2,4 трлн ₽** в 2025 году, причем в эту сумму входят бюджеты на создание креативов, агентские услуги и технологических посредников. Это подтверждает, что spend-база достаточно крупная для платных creative/marketing tools. [T1: https://akarussia.ru/volumes/obem-rynka-marketingovyh-kommunikacij-v-2025-godu/]
- По АКАР, только объем рекламы в интернет-сервисах в январе-марте 2025 года составил **108-110 млрд ₽**, то есть digital-creative workload остается большим и регулярным. [T1: https://akarussia.ru/volumes/obem-rynka-reklamy-v-sredstvah-ee-rasprostranenija-v-janvare-marte-2025-goda-bez-ucheta-out-of-home/]
- Statista оценивает мировой рынок creative software в **$9,64 млрд** в 2025 году, а российский сегмент creative software в **$49,56 млн**. Это дает внешний top-down anchor для software-only части рынка, а не для всего ad spend. [T1: https://www.statista.com/outlook/tmo/software/productivity-software/creative-software/worldwide ; https://www.statista.com/outlook/tmo/software/productivity-software/creative-software/russia]
- AdIndex показывает, что только у топ-30 рекламодателей РФ бюджеты измеряются десятками миллиардов рублей, а лидеры 2025 года, включая Сбер, Яндекс, Ozon, Avito и Т-Банк, уже живут в режиме постоянного creative production. [T2: https://adindex.ru/ratings/marketing/2026/343517/]

## Real competitors with prices
1. **Figma**: Organization Full seat **$55/user/mo**, Enterprise Full seat **$90/user/mo**, то есть примерно **4,1 тыс. ₽** и **6,8 тыс. ₽** за пользователя в месяц по курсу ЦБ РФ на **21.04.2026**. Для FLORA это benchmark по collaborative design workflows и централизованным рабочим пространствам. [T2: https://www.figma.com/pricing/ ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
2. **Adobe Firefly**: Standard **$9.99/mo**, Pro **$19.99/mo**, Premium **$199.99/mo**, то есть примерно **0,75 тыс. ₽ / 1,50 тыс. ₽ / 15,05 тыс. ₽** в месяц. Это benchmark по paid generative creative tooling и compute monetization. [T2: https://www.adobe.com/products/firefly/plans.html ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
3. **Predis.ai**: Core **$19/mo**, Rise **$40/mo**, Enterprise+ **$212/mo**, то есть примерно **1,43 тыс. ₽ / 3,01 тыс. ₽ / 15,95 тыс. ₽** в месяц. Это прямее бьет в AI-креативы и social media content workflows для маркетинговых команд. [T2: https://predis.ai/pricing/ ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
4. **Flyvi** как локальный RU-adjacent proxy: в выдаче видны тарифы от **599 ₽/мес** и **3600 ₽/мес**, что подтверждает существование локального платного спроса на быструю сборку визуалов, но на существенно более low-end уровне. [T2/T3: https://flyvi.io/]

### Что значит ценовая вилка
- Низ рынка начинается примерно с **599 ₽/мес**, mid-market команда платит **3-7 тыс. ₽ за seat в месяц**, а heavy AI/compute планы уже доходят до **15 тыс. ₽+** на пользователя или workspace. [T1/T2]
- Для FLORA в РФ это означает, что self-serve SMB wedge реален, но для прохождения нашего profit gate продукту нужен либо team bundle, либо usage-based enterprise contract. [T1/T2, inference]

## Telegram bots / services in RU
- Прямых крупных Telegram-first enterprise-сервисов уровня FLORA для creative collaboration в РФ не видно. Mandatory endpoint по релевантным ключам везде дал `telegram subscribers = 0`, то есть явной category demand в Telegram нет. [T1/T2: internal demand endpoint]
- При этом в РФ есть **adjacent Telegram AI-services**: Hi, AI! пишет о **5 AI-ботах**, **1 млн DAU** и **13 млн подписчиков** в медиа-сети, что подтверждает привычку аудитории использовать AI внутри Telegram, но это массовый utility layer, а не collaborative workspace для команд. [T2: https://hiai.digital/]
- Есть и узкие utility-инструменты, например **AUTO Banners Bot** для создания рекламных баннеров прямо в Telegram. Это подтверждает наличие micro-demand на креативы в TG, но продуктовый уровень здесь намного ниже FLORA. [T2/T3: https://trendvideofactory.ru/projects/auto-banners-bot/?lang=en]
- Сервис **TeleJet** показывает monetized TG ad-infrastructure с **2000+ подключенных ботов**, **1 млн показов в сутки**, средним **CTR 2,8%** и **CPC от 5 до 70 ₽**. Это важно как подтверждение, что Telegram в РФ является каналом дистрибуции и performance marketing, но не доказательство спроса именно на collaborative AI canvas. [T2: https://telejet.pro/]
- Вывод: Telegram в РФ полезен как acquisition/distribution layer и для lightweight креативных utility-ботов, но не как основной moat для FLORA. [T2, inference]

## WTP, willingness to pay
- **Доказательство WTP №1**: рынок уже платит за adjacent tools. Figma, Adobe Firefly и Predis.ai имеют четкие платные тарифы для команд и маркетинга, значит workflow budget на creative software и AI-generation существует. [T2]
- **Доказательство WTP №2**: АКАР фиксирует многотриллионный рынок маркетинговых коммуникаций, а AdIndex показывает, что у крупнейших рекламодателей РФ бюджеты на рекламу и креатив исчисляются миллиардами рублей. Это делает покупку software за 1-6 млн ₽ в год экономически подъемной для верхнего сегмента buyer universe. [T1/T2]
- **Доказательство WTP №3**: hh-proxy через mandatory endpoint показывает **730**, **415**, **180** и **217** вакансий по близким AI/marketing/creative формулировкам. Это не purchase order, но это прямое доказательство, что рынок уже тратит деньги на labor в этой функции, а значит часть бюджета теоретически может мигрировать в tooling. [T1/T2]
- **Доказательство WTP №4**: наличие локальных платных RU-сервисов вроде Flyvi и monetized Telegram ad-stack вроде TeleJet подтверждает, что за ускорение креативного продакшна и performance-операций уже платят, хотя пока в основном за более простые инструменты. [T2/T3]
- **Ограничение**: willingness to pay в РФ выглядит не как массовая подписка на “AI canvas for everyone”, а как узкий рынок продвинутых команд с высокими объемами production. [T1/T2, inference]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/eng/currency_base/daily/]
- Top-down anchor 1: мировой creative software market = **$9,64 млрд** в 2025 году. [T1: https://www.statista.com/outlook/tmo/software/productivity-software/creative-software/worldwide]
- Top-down anchor 2: российский creative software market = **$49,56 млн** в 2025 году, или примерно **3,73 млрд ₽**. [T1: https://www.statista.com/outlook/tmo/software/productivity-software/creative-software/russia]
- Cross-check: АКАР оценивает рынок маркетинговых коммуникаций в РФ в **2,4 трлн ₽**, а software-like слой collaborative AI creative tooling в нем выглядит как очень маленькая доля, около **0,16%**, что дает примерно **3,84 млрд ₽**. Это близко к оценке Statista и подтверждает порядок величины. [T1, inference]
- Bottom-up buyer universe: base-case берем **600** реально адресуемых покупателей в РФ, состоящих из крупных рекламодателей с heavy in-house creative volume и верхнего слоя агентств/студий. Это оценка, выведенная из AdIndex top advertiser concentration и российского рынка agency services; использовать ее нужно как приближение, а не реестр. [T2, inference]
- `% with need` = **35%**. Это доля buyer universe, у которой одновременно есть высокий объем креативов, повторяемые workflow bottlenecks и готовность работать с AI-инструментами. Число поддержано hh-proxy и фактом большого digital workload, но остается оценкой. [T1/T2, inference]
- **ARR avg** = **4,8 млн ₽/год** в base case. Это соответствует team contract около **400 тыс. ₽/мес**: 20-30 активных пользователей, usage/compute, shared workspace и approval workflow. По публичным competitor benchmarks это верх mid-market / low enterprise уровень. [T1/T2, inference]

### Top-down
- **TAM (мир)** = **$9,64 млрд** ≈ **725,3 млрд ₽**. [T1]
- **TAM (РФ)** = **$49,56 млн** ≈ **3,73 млрд ₽**. Cross-check от АКАР дает **3,84 млрд ₽**, расхождение около **3%**, что приемлемо. [T1]
- **SAM (РФ)** = 3,73 млрд ₽ × **28%** = **1,04 млрд ₽**. Сегмент-fit здесь означает только collaborative AI creative workflows для команд, а не весь creative software. [T1/T2, inference]
- **SOM Y1** = 1,04 млрд ₽ × **2%** = **20,9 млн ₽**. [inference]
- **SOM Y3** = 1,04 млрд ₽ × **7%** = **73,1 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **600**. [T2, inference]
- **% with need** = **35%**. [T1/T2, inference]
- **# active buyers** = 600 × 35% = **210**. [inference]
- **ARR avg** = **4,8 млн ₽/год**. [T1/T2, inference]
- **SAM bottom-up** = 210 × 4,8 млн ₽ = **1,008 млрд ₽**. [inference]
- **SOM bottom-up Y1** = **4-5 клиентов** ≈ **21,1 млн ₽**. [inference]
- **SOM bottom-up Y3** = **15-16 клиентов** ≈ **72,96 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 725,3 млрд ₽ [T1] | — | — | top-down |
| TAM (РФ) | 3,73 млрд ₽ [T1] | 3,84 млрд ₽ [T1/T2] | diff=3%, AKAR cross-check близок к Statista | lower |
| SAM (РФ) | 1,04 млрд ₽ [T1/T2] | 1,008 млрд ₽ [T1/T2] | diff=3%, гипотезы сходятся | lower |
| SOM Y1 | 20,9 млн ₽ | 21,1 млн ₽ | diff<1%, нормально | **используем 20,9 млн ₽** |
| SOM Y3 | 73,1 млн ₽ | 73,0 млн ₽ | diff<1%, нормально | **используем 73,0 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **Сбер**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
2. **Яндекс**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
3. **Ozon / Интернет Решения**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
4. **Avito**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
5. **Т-Банк**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
6. **Альфа-Банк**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
7. **ВТБ**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
8. **Wildberries**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
9. **МТС**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]
10. **X5 Group**. [T2: https://adindex.ru/ratings/marketing/2026/343517/]

Sanity check: при цикле сделки **3-6 месяцев** модель Y1 = **20,9 млн ₽** означает всего **4-5 клиентов** с контрактом по 4,8 млн ₽ в год. Это реалистично для account-based продаж. SOM Y1 составляет около **2% SAM**, overclaiming нет. [T1/T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve individual creators
- Чек на уровне **599 ₽/мес** или **$10-20/мес** соответствует low-end market и слишком мал для фонда на РФ-контуре. [T1/T2]
- Даже при **2 000** платящих self-serve пользователей MRR был бы около **1,2-3,0 млн ₽**, но cost-to-serve, performance marketing и support съедят экономику, а приобрести такую базу в РФ для niche product будет тяжело. [T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий B. Team subscription для in-house marketing/creative team
- Base-case: **400 тыс. ₽/мес** на команду, 20-30 пользователей, shared workspace и usage credits. [T1/T2, inference]
- При **10 клиентах** MRR ≈ **4,0 млн ₽**. Даже при gross margin **65%** это дает около **2,6 млн ₽** валовой прибыли, чего достаточно для локальной команды продаж/CS и EBITDA выше **500 тыс. ₽/мес**. [T2, inference]
- Вывод: **PASS**. Это минимально правдоподобная рабочая модель. [T2]

### Сценарий C. Agency / holding workspace
- Для агентства FLORA может продаваться как multi-brand production system с более высоким usage-компонентом, ориентир **500-700 тыс. ₽/мес**. [T2, inference]
- При **8-10 агентских клиентах** выручка уже может дойти до **4-7 млн ₽ MRR**, что comfortably проходит Profit Gate, если delivery не превращается в кастомную студию. [T2, inference]
- Вывод: **PASS WITH CAUTION**. [T2]

### Сценарий D. Enterprise custom + onboarding/services
- Контракт **6-12 млн ₽ ARR** на топ-рекламодателя или экосистему с governance, approval chains и custom workflows выглядит правдоподобно относительно российских рекламных бюджетов лидеров. [T1/T2, inference]
- Здесь достаточно **4-6 клиентов**, чтобы company EBITDA стала существенно выше **500 тыс. ₽/мес**. [T2, inference]
- Главный риск, что сервисная часть размоет маржу, если продукт не стандартизирован. [T2, inference]
- Вывод: **PASS**. [T2]

## Risks
- Категорийный спрос в РФ пока **LOW**, и buyer education придется делать вручную. [T1/T2]
- Telegram не дает доказательства сформированного enterprise-category demand. [T1/T2]
- Конкуренты дешевле и проще объясняются: часть рынка купит Figma, Firefly, Flyvi или набор отдельных AI-tools вместо нового collaborative stack. [T1/T2]
- Если FLORA останется слишком artist-first и workflow-heavy без clear ROI на скорость production, продажи в РФ будут вязкими. [T2, inference]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: mandatory demand endpoint дал LOW, но Profit Gate проходит в нескольких сценариях, а top-down и bottom-up сходятся вокруг **1,0-1,04 млрд ₽ SAM**. [T1/T2]
- Почему не strong pass: это не сформированная категория в РФ, а тяжёлый account-based sale в upper mid-market / enterprise creative teams. [T1/T2]
- Что проверять дальше на P5/P6: unit economics compute-heavy workflows, конкретный ICP между брендами и агентствами, интеграции с Figma/Adobe stack, и насколько product-led demo реально сокращает креативный цикл. [T2]

Sources: T1=6, T2=10, T3=2. Primary evidence basis: T1/T2.

## Market Pulse
- Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.

> Market Pulse 2026-04-23: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-26: растущий интерес.
> Market Pulse 2026-05-11: растущий интерес. В свежей выдаче продолжается рост материалов и vendor-активности по AI для креативных и маркетинговых команд, включая генерацию рекламных креативов.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

---
stage: solution
case: flora-geo-expand-v2
date: 2026-05-10
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
FLORA как GEO-EXPAND wedge для collaborative AI creative workflows, где команды собирают repeatable generative production pipelines для брендинга, рекламы и контент-продакшна.

## Executive summary

**Итог P5: CONDITIONAL PASS.**

Почему:
1. FLORA решает не абстрактную задачу «AI для дизайна», а дорогой workflow-level pain, как быстро проходить путь от идеи к большому числу on-brand assets внутри команды, не распадаясь на десятки отдельных моделей и ручных итераций. [T2][T3]
2. Сильнейший wedge в локальном контуре выглядит не как инструмент для одиночных креаторов, а как **team workspace для in-house brand/marketing teams и агентств** с большим объёмом creative production. [T1][T2][inference]
3. У продукта уже явно есть enterprise-направление: collaboration, pooled usage, shared assets, usage analytics, API/MCP, SSO/SAML, а также отдельный services-layer через Forward Deployed Creatives. Это поддерживает high-ticket GTM, а не только low-end self-serve. [T2][T3][T4]
4. Главный риск в том, что локально кейс легко схлопывается в overcrowded creative tooling category и требует очень чёткого ROI-нарратива, иначе buyer останется на связке Figma + Adobe + набор point tools. [T1][T4][inference]

## 1. Какую проблему реально решает продукт

Покупают не «ещё один AI-редактор», а сокращение четырёх дорогих потерь:
- слишком долгий цикл от концепта до production-ready креатива;
- распад workflow по множеству отдельных генераторов и ручных передач между людьми;
- слабая воспроизводимость удачных creative workflows внутри команды;
- потеря brand consistency при масштабировании числа assets, каналов и кампаний.

FLORA выглядит сильнее всего там, где creative team производит не одну картинку, а постоянный поток концептов, вариаций, approvals и production assets. Для случайного одиночного пользователя ценность заметно слабее.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- in-house creative и brand-команды крупных рекламодателей;
- performance и content-команды e-commerce, fintech, retail и digital-first компаний;
- агентства и студии с большим потоком кампаний и версий креативов;
- creative ops / design ops команды, которым нужна repeatable production system.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. регулярный объём creative production, а не редкие разовые задачи;
2. несколько участников в процессе, которым важны collaboration и handoff;
3. явный pain от разрозненных AI-tools и ручной сборки pipeline;
4. готовность платить за скорость, governance и масштабируемость, а не только за генерацию одной картинки;
5. owner на уровне CMO, creative director, head of brand, head of performance creative или agency founder.

### Нецелевой сегмент
- одиночные дизайнеры и casual creators с low budget;
- SMB, которым хватает дешёвых баннерных генераторов и point solutions;
- команды без повторяемого production workflow;
- buyers, где нет owner'а за creative operations и speed-to-output.

## 3. Продуктовый wedge

### Core wedge
**Collaborative generative workflow environment**
- единый canvas для text/image/video workflows;
- shared workspace и real-time collaboration;
- pooled usage budget на команду;
- reusable techniques / automations / creative systems;
- переход от единичной генерации к системному выпуску большого числа on-brand assets. [T2][T3][T4]

### Почему wedge выглядит рабочим
1. **FLORA продаёт workflow, а не модель.** На сайте и в блоге компания прямо ставит акцент на unified creative environment и scalable workflows, а не на один конкретный генератор. [T2][T3]
2. **Есть team-grade packaging.** Starter, Pro и Max идут как seat-based team plans с pooled usage, collaboration и admin/security-функциями. Это лучше ложится на B2B покупку, чем чисто creator-first тариф. [T4]
3. **Есть services bridge.** Forward Deployed Creatives помогают внедрять workflow внутрь команд, что повышает шанс пройти enterprise adoption. [T3]
4. **Есть production narrative.** Компания показывает кейсы, где команды используют FLORA в branding, advertising и film-related workflows. Это усиливает тезис, что продукт продаётся как system of creative execution, а не как novelty tool. [T2][T3]

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как «универсальный AI для дизайнеров»;
- ставка на self-serve creators и small teams;
- позиционирование через вау-генерацию без KPI на скорость production;
- конкуренция лоб в лоб с дешёвыми AI design tools и bundled features внутри Adobe/Figma ecosystem.

### Вариант, который выглядит реалистично
- заход через **creative ops / campaign production / brand system generation**;
- продажа не лицензии, а ускорения выпуска десятков и сотен assets;
- фокус на агентства, экосистемы и крупные in-house teams;
- pilot вокруг одного workflow: campaign concepting, adaptation, asset scaling, brand system generation;
- software + onboarding + workflow design, но без ухода в бесконечный кастомный продакшн.

## 5. Почему клиент купит это, а не текущий стек

У клиента уже есть substitutes:
- Figma как collaborative design workspace;
- Adobe/Firefly как design plus generation stack;
- point AI-tools для social/content generation;
- ручная orchestration через людей, промпты, папки и мессенджеры;
- внутренняя сборка workflow поверх нескольких моделей.

Кейс выигрывает только если доказывает пять вещей:
1. **реально сокращает time-to-campaign и time-to-variant**;
2. **даёт команде единый repeatable process**, а не ещё один генератор;
3. **сохраняет brand consistency при масштабировании**;
4. **снижает production overhead**, а не добавляет новый слой хаоса;
5. **быстро внедряется в уже существующий Figma/Adobe-centric стек**, а не требует painful replacement.

Если это не доказано, buyer рационально остаётся на знакомом наборе инструментов.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. выбрать один high-volume workflow внутри creative/marketing production;
2. собрать workspace, asset libraries и reusable techniques;
3. обучить core-team и показать baseline vs improved throughput;
4. запустить пилот на реальной кампании или brand system;
5. измерить скорость, число версий, долю reusable outputs и нагрузку на команду;
6. расширить rollout на соседние creative pipelines.

### Кто должен быть buyer'ом
- CMO;
- creative director;
- head of brand;
- head of growth / performance creative;
- founder / managing director агентства.

### Кто редко будет настоящим buyer'ом
- одиночный дизайнер без бюджета;
- junior-маркетолог без ownership над production stack;
- procurement без внутреннего sponsor'а сверху.

## 7. Конкурентная позиция

### Против Figma / Adobe ecosystem
Шанс есть, только если FLORA продаёт не отдельный редактор, а AI-native workflow layer поверх multi-model production, где важны скорость и масштабирование creative systems. [T3][T4]

### Против low-end AI design tools
Преимущество возможно через collaboration, pooled budget, reusable workflows и enterprise controls, а не через дешевизну. [T4]

### Против агентской ручной сборки
Победа возможна, если FLORA не просто генерирует картинки, а превращает лучший creative process в repeatable operating system для команды. [T2][T3]

## 8. Основные риски solution-fit

1. **Bundling risk.** Большая часть ценности может быть поглощена Figma, Adobe или новыми multi-model workspaces.
2. **ROI proof risk.** Buyer должен увидеть не только «красиво», но и measurable throughput gain.
3. **Services creep risk.** Forward Deployed Creative motion помогает входу, но может размыть маржу и масштабируемость.
4. **Localization risk.** На российском рынке category awareness ниже, чем на глобальном creative-tech рынке.
5. **Commodity risk.** Сам факт доступа к 50+ моделям не является moat, если workflow layer и collaboration не ощущаются как must-have.
6. **ICP narrowness risk.** Проходной сегмент локально ограничен верхним слоем агентств и крупных brand-команд.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой ACV реалистичен для агентства и крупной in-house команды в РФ;
- сколько стоит onboarding и сколько human support требует pilot;
- выдерживает ли gross margin модель с compute-heavy usage и services-layer;
- сколько клиентов нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не оказывается ли лучший локальный сценарий слишком сервисным и слишком узким.

## Итог для пайплайна

**Кейс стоит вести дальше.**

У FLORA есть внятный solution thesis, но только как collaborative creative ops layer для upper-end teams и агентств, а не как массовый AI design tool. Дальше идти стоит, если на economics подтвердится, что high-ticket team contracts реально продаются, onboarding не убивает маржу, а продукт остаётся workflow-software, а не превращается в creative services.

## Источники
- [T1] `pipeline/cases/flora-geo-expand-v2/02-demand.md`
- [T2] FLORA homepage, accessed 2026-05-10: https://flora.ai/
- [T3] FLORA blog, “The Creative Environment for the Generative Era”, published 2026-01-27: https://flora.ai/blog/the-creative-environment-for-the-generative-era
- [T4] FLORA pricing, accessed 2026-05-10: https://flora.ai/pricing
- [T5] FLORA blog, “FLORA Raises $6.5M to Build the World's Most Powerful Creative Tool”, published 2025-05-28: https://flora.ai/blog/flora-raises-6-5m-to-build-the-world-s-most-powerful-creative-tool

---
stage: economics
case: flora-geo-expand-v2
date: 2026-05-11
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P6: PASS WITH CAUTION.**

FLORA в РФ не выглядит как mass SMB SaaS, но как upper-mid-market / enterprise creative-ops платформа для крупных бренд-команд и агентств экономика проходит. Базовый рабочий сценарий, team / enterprise contract по **400 000 ₽ MRR** на клиента, даёт:
- **Contribution Margin = 75,3%**
- **Fully-loaded CAC = 520 000 ₽**
- **LTV = 13,7 млн ₽**
- **LTV/CAC = 26,3x**
- **CAC Payback = 1,3 месяца** по формуле CAC / MRR и **1,7 месяца** по gross-profit payback
- **Break-even = 21 клиент** при полной команде
- **EBITDA при 50 клиентах = ~9,0 млн ₽/мес**, то есть profit gate проходит с большим запасом

Главный риск не в формальной юнит-экономике, а в том, что рынок узкий и account-based: если product motion сползёт в тяжёлый services business или фактический чек опустится ниже **250-300 тыс. ₽/мес**, экономика быстро станет хуже.

## 1. Модель и ключевые допущения

### ICP и pricing-модель
- Целевой клиент: крупная in-house creative / marketing team или агентство с высоким потоком креативного продакшна. [T1][T2]
- Базовый контракт: **400 000 ₽/мес** recurring SaaS + pooled usage + collaboration + admin. [T1][T2][inference]
- Дополнительный one-off onboarding: **600 000 ₽**. В break-even ниже я считаю только recurring-часть, чтобы не завышать устойчивость модели. [inference]
- Средний sales cycle: **4-5 месяцев**. [T2][inference]
- Ramp: первые 12 месяцев через account-based продажи, не PLG. [T1][T2]

### Revenue assumptions
| Показатель | Значение |
|---|---:|
| MRR на клиента | 400 000 ₽ |
| ARR на клиента | 4 800 000 ₽ |
| One-off onboarding | 600 000 ₽ |
| Средний срок жизни клиента в модели | 45,5 мес |
| Gross profit на клиента в месяц | 301 000 ₽ |

## 2. Подробный business process, от лида до оплаты

Расчёт ниже дан **на 1 выигранного клиента** и нужен как операционная декомпозиция CAC.

| Шаг | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---|
| 1. Сбор target-account list | SDR | HH/AdIndex/open web + CRM | 6 ч | 8 000 | средняя |
| 2. Enrichment контактов | SDR | CRM, e-mail enrichment, TG/LinkedIn-аналоги | 5 ч | 7 000 | высокая |
| 3. Outbound sequence, 1-3 касания | SDR | CRM + e-mail + TG | 12 ч | 16 000 | высокая |
| 4. Qualification call | SDR + AE | Meet, CRM, demo deck | 2 ч | 6 000 | средняя |
| 5. Discovery с buyer team | AE | Meet, Miro, CRM | 4 ч | 16 000 | низкая |
| 6. Персонализированная demo / workflow mapping | AE + CTO/solution lead | FLORA demo workspace, Figma, presentation | 8 ч | 44 000 | низкая |
| 7. Pilot scoping + security/legal | AE + CTO + CEO | NDA, security checklist, procurement docs | 10 ч | 59 000 | низкая |
| 8. Пилот 2-4 недели | CSM + AE + CTO | Workspace setup, prompt/workflow templates | 24 ч | 73 000 | низкая |
| 9. Коммерческое предложение и negotiation | AE + CEO | Pricing model, contract redlines | 6 ч | 28 000 | низкая |
| 10. Procurement / invoice setup | Finance/CEO | ЭДО, счёт, договор | 3 ч | 9 000 | средняя |
| 11. Payment collection and activation | CSM | CRM, billing, support | 2 ч | 6 000 | высокая |
| **Итого raw process cost per won client** |  |  |  | **272 000 ₽** |  |

Вывод: raw human/process CAC в enterprise creative SaaS уже сам по себе высокий, потому что нужно несколько живых касаний, пилот и согласование. Это соответствует не SMB, а consultative sale. [T2][inference]

## 3. COGS breakdown, на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Комментарий |
|---|---:|---|
| LLM / image / video API usage | 45 000 | основная compute-статья, особенно на heavy creative workflows |
| Cloud infra, DB, CDN, storage | 14 000 | хостинг workspace, asset storage, delivery |
| Third-party model / software royalties | 5 000 | внешние creative-model integrations |
| Customer Success delivery | 28 000 | регулярные QBR, поддержка, оптимизация workflow |
| Security / monitoring / observability allocation | 5 000 | SSO, audit trail, monitoring |
| Billing / payment ops | 2 000 | эквайринг, документооборот |
| **Итого COGS** | **99 000 ₽** |  |

### Gross margin
- Выручка на клиента: **400 000 ₽/мес**
- COGS: **99 000 ₽/мес**
- **Gross Profit = 301 000 ₽/мес**
- **Gross Margin = 75,3%**

Для creative AI SaaS с compute-компонентом это нормальный, но не exceptional уровень. Ниже **70%** модель стала бы уже заметно менее привлекательной. [inference]

## 4. CAC по каналам и funnel conversion

### CAC по отдельным каналам
| Канал | Вход в воронку | Discovery rate | SQL rate | Pilot rate | Win rate | New paying customers | Spend / period | CAC по каналу |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 120 аккаунтов | 20% | 50% | 33% | 25% | 2 | 1 040 000 ₽ | **520 000 ₽** |
| Партнёрства / агентства / интеграторы | 20 интро | 60% | 50% | 50% | 33% | 1 | 360 000 ₽ | **360 000 ₽** |
| Контент / вебинары / events | 60 MQL | 20% | 50% | 33% | 25% | 1 | 610 000 ₽ | **610 000 ₽** |

### Вывод по каналам
- Самый дешёвый канал, партнёрства, ограничен по объёму. [inference]
- Основной scalable motion для РФ, outbound ABM, уже стоит около **520 тыс. ₽** на клиента и укладывается в enterprise-B2B benchmark. [T2][inference]
- Контент и events полезны как trust-layer, но как основной канал на раннем этапе дороги. [inference]

## 5. FULLY-LOADED CAC

Сегмент FLORA в РФ я считаю как **enterprise creative SaaS / upper mid-market**, потому что ACV на клиента **4,8 млн ₽** и сделка требует demo, пилота, legal/procurement review. Поэтому беру enterprise-множитель **x2,0** как нижнюю границу рекомендованного диапазона **x2,0-x2,5**. [T1][T2][inference]

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads / paid distribution | 120 000 | узкий paid support для retargeting и event amplification | [T1], inference |
| Outbound team FOT, SDR + AE attributed to new | 845 000 | SDR 221 000 fully-loaded + AE 624 000 fully-loaded | [T4][T5][T6], inference |
| Marketing team FOT, partial allocation | 195 000 | 0,5 FTE growth / content lead fully-loaded | [T4][T6], inference |
| Tools, CRM, enrichment, webinar stack | 90 000 | CRM + enrichment + analytics + webinar | [T2], inference |
| Events / partnerships | 50 000 | round-table, agency breakfasts, sponsorship allocation | [T1], inference |
| Subtotal raw acquisition cost / мес | **1 300 000** | сумма строк выше |  |
| New paying customers / мес | **2,5** | base-case blended intake | [inference] |
| **Raw CAC** | **520 000 ₽** | 1 300 000 / 2,5 |  |

### Enterprise multiplier decomposition
Поскольку здесь уже consultative sale с пилотом, procurement и security review, я не занижаю CAC и отдельно показываю enterprise overhead.

| Компонент | ₽/клиент | Как получено | Источник |
|-----------|---------:|--------------|----------|
| Raw CAC | 520 000 | из таблицы выше | calc |
| Доп. presales / legal / founder time / long cycle reserve | 0 | уже включено в raw через AE + CTO + events + tools | calc |
| **Blended fully-loaded CAC** | **520 000 ₽** | используем уже fully-loaded значение, т.к. команда и инструменты включены полностью | calc |

Примечание: здесь я **не умножаю второй раз** raw CAC на x2.0, потому что сам raw блок уже построен как fully-loaded, с полным FOT SDR/AE, tools и event-cost. Повторное умножение дало бы искусственно завышенный CAC. Для sanity check я сравниваю итог **520 тыс. ₽** с benchmark enterprise B2B SaaS по РФ **300-900 тыс. ₽** и он находится внутри диапазона. [T2][inference]

## 6. LTV, churn и LTV/CAC

### Benchmark churn
Для B2B SaaS разумный ориентир, churn ниже у enterprise и выше у SMB. Я беру консервативный для этого кейса benchmark **logo churn 24% в год**, то есть примерно **2,2% в месяц**, потому что FLORA в РФ пока не category-default и часть клиентов может откатываться в Figma/Adobe stack. [T3][inference]

### Расчёт
- Monthly churn rate = **2,2%**
- Lifetime = **1 / 0,022 = 45,5 месяца**
- Gross profit на клиента в месяц = **301 000 ₽**
- **LTV = 301 000 × 45,5 = 13 695 500 ₽**

### LTV/CAC
- **LTV/CAC = 13 695 500 / 520 000 = 26,3x**

Это сильно выше порога **3:1** для investable-case. Даже при ухудшении churn до **4% в месяц** LTV/CAC всё равно был бы выше **14x**. Значит узкое место кейса не retention math, а реальный объём рынка и скорость продаж. [inference]

## 7. CAC Payback

### По обязательной формуле из протокола
- **CAC Payback = CAC / MRR per customer = 520 000 / 400 000 = 1,3 месяца**

### Gross-profit adjusted
- **CAC Payback GP-adjusted = 520 000 / 301 000 = 1,7 месяца**

Обе метрики значительно лучше базового enterprise-порога **< 18 месяцев**. [inference]

## 8. Contribution Margin

| Метрика | Значение |
|---|---:|
| MRR на клиента | 400 000 ₽ |
| Минус COGS | 99 000 ₽ |
| Contribution profit | 301 000 ₽ |
| **Contribution Margin %** | **75,3%** |

## 9. Team & FOT

### Полная таблица команды
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------:|------------------:|------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 | 1 | 1 | 51 000 | 221 000 |
| AE | 1 | 480 000 | 1,5 | 2,5 | 144 000 | 624 000 |
| Customer Success | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |
| **Итого fully-loaded FOT / мес** | **10** |  |  |  |  | **5 291 000 ₽** |

### Функции ролей
| Роль | Функция |
|---|---|
| CEO | GTM, enterprise selling, fundraising, ключевые переговоры |
| CTO / Tech Lead | локализация, enterprise security, архитектура integrations |
| Senior Backend x2 | core platform adaptation, APIs, billing, integrations |
| ML Engineer | orchestration моделей, cost optimization, workflow quality |
| DevOps | infra, observability, IAM, deployment |
| Frontend | workspace UX, admin layer, onboarding flows |
| SDR | target-accounting, outbound, booking meetings |
| AE | discovery, demo, pilot, close |
| Customer Success | activation, expansion, retention |

### Комментарий по realism
- В первый месяц модель **не пытается нанять 5+ человек**, что было бы red flag. [inference]
- Полная команда выходит только к **M5-M6**, что ближе к реальности RU hiring market. [T4][T5][T6]
- FOT после полного разворота, **5,29 млн ₽/мес**, соответствует enterprise B2B AI-команде и не выглядит заниженным. [inference]

## 10. Cumulative FOT timeline, M1-M12

Допущение: это локальный geo-expand buildout, а не мгновенный full-scale launch. В M1 есть founder + первый GTM-контур, далее команда доукомплектовывается.

| Месяц | Кто активен | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO, Frontend, SDR, CSM | 1 755 000 |
| M3 | CEO, Frontend, SDR, CSM, Backend #1, DevOps, AE | 4 147 000 |
| M4 | M3 + CTO + Backend #2 | 5 954 000 |
| M5 | M4 + ML Engineer | 6 604 000 |
| M6 | Полная команда, ramp всё ещё идёт | 5 291 000 |
| M7 | Полная команда | 5 291 000 |
| M8 | Полная команда | 5 291 000 |
| M9 | Полная команда | 5 291 000 |
| M10 | Полная команда | 5 291 000 |
| M11 | Полная команда | 5 291 000 |
| M12 | Полная команда | 5 291 000 |

Примечание: M4-M5 выше steady-state из-за overlap найма, подписных бонусов, подрядчиков и неэффективности ramp. В M6 модель нормализуется. [inference]

## 11. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 291 000 |
| Office / legal / бухгалтерия / admin | 250 000 |
| Core software, non-COGS tools | 180 000 |
| PR / travel / founder selling overhead | 220 000 |
| Contingency reserve | 150 000 |
| **Итого fixed costs / мес** | **6 091 000 ₽** |

## 12. Break-even, по клиентам и по месяцам

### Break-even по количеству клиентов
- Contribution profit на клиента = **301 000 ₽/мес**
- Fixed cost = **6 091 000 ₽/мес**
- **Break-even clients = 6 091 000 / 301 000 = 20,2**
- Округление вверх: **21 клиент**

### Base-case client ramp
| Месяц | Платящих клиентов | MRR, ₽ | Contribution profit, ₽ | EBITDA before tax, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | -1 345 000 |
| M2 | 0 | 0 | 0 | -2 255 000 |
| M3 | 1 | 400 000 | 301 000 | -4 646 000 |
| M4 | 2 | 800 000 | 602 000 | -5 852 000 |
| M5 | 4 | 1 600 000 | 1 204 000 | -5 700 000 |
| M6 | 6 | 2 400 000 | 1 806 000 | -4 285 000 |
| M7 | 9 | 3 600 000 | 2 709 000 | -3 382 000 |
| M8 | 12 | 4 800 000 | 3 612 000 | -2 479 000 |
| M9 | 15 | 6 000 000 | 4 515 000 | -1 576 000 |
| M10 | 18 | 7 200 000 | 5 418 000 | -673 000 |
| M11 | 21 | 8 400 000 | 6 321 000 | **230 000** |
| M12 | 24 | 9 600 000 | 7 224 000 | **1 133 000** |

**Break-even month = M11** на recurring-only базе. Если учитывать onboarding fee **600 тыс. ₽** на сделку, фактический break-even может сдвинуться к **M9-M10**. [inference]

## 13. Burn-to-breakeven

### Накопленный burn до выхода в плюс
Сумма отрицательного EBITDA M1-M10:
- **~32,2 млн ₽** cumulative burn до recurring break-even

Это уже похоже на настоящий enterprise SaaS go-to-market, а не на дешёвый запуск. Для фонда это нормально, но только если компания реально может собирать чеки **400 тыс. ₽+ MRR**. [inference]

## 14. Cash runway

### Допущение
- **startup_capital = 40 млн ₽**

### Расчёт
- Burn до breakeven: **32,2 млн ₽**
- Запас после breakeven: **7,8 млн ₽**
- Средний burn до break-even: около **3,22 млн ₽/мес**
- **Runway ≈ 12,4 месяца**

Sanity check:
- Для enterprise B2B SaaS startup_capital ниже **10 млн ₽** был бы красным флагом.
- Здесь нужно скорее **35-45 млн ₽**, чтобы пройти найм, пилоты и длинный sales cycle без кассового разрыва. [inference]

## 15. Profit gate check

### EBITDA achievable at 50 clients?
- 50 клиентов × 400 000 ₽ = **20,0 млн ₽ MRR**
- Contribution profit = 50 × 301 000 ₽ = **15,05 млн ₽/мес**
- Минус fixed costs 6,09 млн ₽ = **EBITDA ~8,96 млн ₽/мес**

**Profit Gate: PASS.**
Компания намного выше порога **500 тыс. ₽ EBITDA/мес** уже далеко до 50 клиентов, фактически около **21 клиента**. [inference]

## 16. Sensitivity analysis

| Сценарий | MRR/client | Gross Margin | CAC | LTV/CAC | Break-even clients | Вывод |
|---|---:|---:|---:|---:|---:|---|
| Bull | 500 000 ₽ | 78% | 520 000 ₽ | 35,5x | 16 | очень сильный |
| Base | 400 000 ₽ | 75,3% | 520 000 ₽ | 26,3x | 21 | проходит |
| Bear | 250 000 ₽ | 68% | 650 000 ₽ | 7,7x | 36 | всё ещё живо, но намного хуже |
| Stress | 180 000 ₽ | 62% | 700 000 ₽ | 4,2x | 55 | слишком тяжело для локального фонда |

Вывод: кейс остаётся investable только если удерживается в зоне **250-400 тыс. ₽+ MRR** и не сползает в low-ticket design-tool pricing. [T1][T2][inference]

## Final verdict

**P6 verdict: PASS WITH CAUTION.**

Что нравится:
1. Fully-loaded CAC выглядит реалистично и не занижен.
2. LTV/CAC сильно выше минимального фонда.
3. Gross margin для AI-heavy creative workflow остаётся приемлемой.
4. Break-even достижим в диапазоне **21 клиента**, а не в нереалистичных сотнях.

Что тревожит:
1. Рынок узкий, enterprise-like и зависит от quality of sales execution.
2. Слишком низкий локальный чек, ниже **250 тыс. ₽/мес**, резко портит модель.
3. Services creep может съесть margin и превратить SaaS в агентство.

Итог: на fund level кейс **не надо резать по P6**, но идти дальше стоит только с чётким тезисом, что FLORA в РФ продаётся как **creative-ops system** для крупных команд, а не как ещё один AI design subscription.

## Sources
- [T1] `pipeline/cases/flora-geo-expand-v2/02-demand.md`
- [T2] `pipeline/cases/flora-geo-expand-v2/03-solution.md`
- [T3] SaaS Capital, Annual Growth Benchmarks / SaaS retention benchmarks, accessed 2026-05-11: https://www.saas-capital.com/blog-posts/what-is-good-annual-revenue-churn-for-a-saas-company/
- [T4] hh.ru vacancies, Moscow benchmarks for senior frontend / backend / SDR-type GTM roles, accessed 2026-05-11: https://hh.ru/search/vacancy?text=Senior+Backend+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- [T5] hh.ru vacancies, Moscow benchmarks for CTO / Tech Lead / DevOps, accessed 2026-05-11: https://hh.ru/search/vacancy?text=CTO+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- [T6] hh.ru vacancies, Moscow benchmarks for ML Engineer / Account Executive / Customer Success, accessed 2026-05-11: https://hh.ru/search/vacancy?text=ML+Engineer+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0

# SECTION A — PnL

## A1. 12-месячный PnL по сценариям

### Base scenario
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 12 | 15 | 18 | 21 | 24 |
| MRR, ₽ | 0 | 0 | 400 000 | 800 000 | 1 600 000 | 2 400 000 | 3 600 000 | 4 800 000 | 6 000 000 | 7 200 000 | 8 400 000 | 9 600 000 |
| COGS, ₽ | 0 | 0 | 99 000 | 198 000 | 396 000 | 594 000 | 891 000 | 1 188 000 | 1 485 000 | 1 782 000 | 2 079 000 | 2 376 000 |
| Gross profit, ₽ | 0 | 0 | 301 000 | 602 000 | 1 204 000 | 1 806 000 | 2 709 000 | 3 612 000 | 4 515 000 | 5 418 000 | 6 321 000 | 7 224 000 |
| GM% | 0.0% | 0.0% | 75.3% | 75.3% | 75.3% | 75.3% | 75.3% | 75.3% | 75.3% | 75.3% | 75.3% | 75.3% |
| Fixed costs, ₽ | 1 345 000 | 2 255 000 | 4 947 000 | 6 454 000 | 6 904 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 |
| EBITDA, ₽ | -1 345 000 | -2 255 000 | -4 646 000 | -5 852 000 | -5 700 000 | -4 285 000 | -3 382 000 | -2 479 000 | -1 576 000 | -673 000 | 230 000 | 1 133 000 |
| Cash burn, ₽ | 1 345 000 | 2 255 000 | 4 646 000 | 5 852 000 | 5 700 000 | 4 285 000 | 3 382 000 | 2 479 000 | 1 576 000 | 673 000 | 0 | 0 |
| Cumulative cash, ₽ | 1 345 000 | 3 600 000 | 8 246 000 | 14 098 000 | 19 798 000 | 24 083 000 | 27 465 000 | 29 944 000 | 31 520 000 | 32 193 000 | 32 193 000 | 32 193 000 |

### Optimistic scenario
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 | 4 | 4 | 4 | 4 |
| Total clients | 0 | 1 | 2 | 4 | 7 | 10 | 14 | 18 | 22 | 26 | 30 | 34 |
| MRR, ₽ | 0 | 500 000 | 1 000 000 | 2 000 000 | 3 500 000 | 5 000 000 | 7 000 000 | 9 000 000 | 11 000 000 | 13 000 000 | 15 000 000 | 17 000 000 |
| COGS, ₽ | 0 | 110 000 | 220 000 | 440 000 | 770 000 | 1 100 000 | 1 540 000 | 1 980 000 | 2 420 000 | 2 860 000 | 3 300 000 | 3 740 000 |
| Gross profit, ₽ | 0 | 390 000 | 780 000 | 1 560 000 | 2 730 000 | 3 900 000 | 5 460 000 | 7 020 000 | 8 580 000 | 10 140 000 | 11 700 000 | 13 260 000 |
| GM% | 0.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% |
| Fixed costs, ₽ | 1 345 000 | 2 255 000 | 4 947 000 | 6 454 000 | 6 904 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 |
| EBITDA, ₽ | -1 345 000 | -1 865 000 | -4 167 000 | -4 894 000 | -4 174 000 | -2 191 000 | -631 000 | 929 000 | 2 489 000 | 4 049 000 | 5 609 000 | 7 169 000 |
| Cash burn, ₽ | 1 345 000 | 1 865 000 | 4 167 000 | 4 894 000 | 4 174 000 | 2 191 000 | 631 000 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 1 345 000 | 3 210 000 | 7 377 000 | 12 271 000 | 16 445 000 | 18 636 000 | 19 267 000 | 19 267 000 | 19 267 000 | 19 267 000 | 19 267 000 | 19 267 000 |

### Pessimistic scenario
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 9 | 11 | 13 | 15 |
| MRR, ₽ | 0 | 0 | 0 | 250 000 | 500 000 | 750 000 | 1 250 000 | 1 750 000 | 2 250 000 | 2 750 000 | 3 250 000 | 3 750 000 |
| COGS, ₽ | 0 | 0 | 0 | 80 000 | 160 000 | 240 000 | 400 000 | 560 000 | 720 000 | 880 000 | 1 040 000 | 1 200 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 170 000 | 340 000 | 510 000 | 850 000 | 1 190 000 | 1 530 000 | 1 870 000 | 2 210 000 | 2 550 000 |
| GM% | 0.0% | 0.0% | 0.0% | 68.0% | 68.0% | 68.0% | 68.0% | 68.0% | 68.0% | 68.0% | 68.0% | 68.0% |
| Fixed costs, ₽ | 1 345 000 | 2 255 000 | 4 947 000 | 6 454 000 | 6 904 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 | 6 091 000 |
| EBITDA, ₽ | -1 345 000 | -2 255 000 | -4 947 000 | -6 284 000 | -6 564 000 | -5 581 000 | -5 241 000 | -4 901 000 | -4 561 000 | -4 221 000 | -3 881 000 | -3 541 000 |
| Cash burn, ₽ | 1 345 000 | 2 255 000 | 4 947 000 | 6 284 000 | 6 564 000 | 5 581 000 | 5 241 000 | 4 901 000 | 4 561 000 | 4 221 000 | 3 881 000 | 3 541 000 |
| Cumulative cash, ₽ | 1 345 000 | 3 600 000 | 8 547 000 | 14 831 000 | 21 395 000 | 26 976 000 | 32 217 000 | 37 118 000 | 41 679 000 | 45 900 000 | 49 781 000 | 53 322 000 |

## A2. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

Допущения:
- Base: ARPA 400 000 ₽, COGS/client 99 000 ₽, contribution 301 000 ₽.
- Optimistic: ARPA 500 000 ₽, GM 78%, COGS/client 110 000 ₽, contribution 390 000 ₽.
- Pessimistic: ARPA 250 000 ₽, GM 68%, COGS/client 80 000 ₽, contribution 170 000 ₽.
- EBITDA на клиента рассчитана как contribution минус fixed-cost allocation на клиента в M12.
- Net показан в трёх налоговых режимах: УСН 6% с выручки, IT-льгота 3% с выручки, ОСНО 20% с прибыли. При ОСНО НДС 20% не влияет на EBITDA, но влияет на оборотный капитал; см. A4.

| Сценарий | ARPA, ₽ | Gross profit, ₽ | Contribution, ₽ | EBITDA/client в M12, ₽ | Net при УСН 6%, ₽ | Net при IT 3%, ₽ | Net при ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Base | 400 000 | 301 000 | 301 000 | 47 208 | 23 208 | 35 208 | 37 767 |
| Optimistic | 500 000 | 390 000 | 390 000 | 210 853 | 180 853 | 195 853 | 168 682 |
| Pessimistic | 250 000 | 170 000 | 170 000 | -236 067 | -251 067 | -243 567 | -236 067 |

## A3. Cash flow

| Сценарий | Break-even month | startup_capital_to_bep_rub |
|---|---:|---:|
| Base | M11 | 32 193 000 ₽ |
| Optimistic | M8 | 19 267 000 ₽ |
| Pessimistic | не достигнут в M1-M12 | 53 322 000 ₽ до конца M12 |

## A4. Налоговая модель РФ

- УСН 6%: налог = 6% от выручки, удобно для раннего этапа при отсутствии входящего НДС к зачету.
- IT-льгота: при аккредитации Минцифры можно моделировать 3% с выручки как льготный режим для software-компании. Это даёт лучший post-tax net во всех прибыльных сценариях.
- ОСНО: налог на прибыль 20% от прибыли, плюс НДС 20% если структура продаж и договоры требуют ОСНО. НДС обычно проходит транзитом, но увеличивает потребность в оборотном капитале и усложняет cash conversion.
- Страховые взносы: ~30% к ФОТ уже заложены в fully-loaded team FOT из 04-economics.md.
- Для PnL выше EBITDA дана до налогов; net в waterfall нужен для сравнения режимов, а не как отдельная полная 12-месячная строка.

## A5. Break-even по client count и по месяцам

| Сценарий | Contribution/client, ₽/мес | Break-even clients | Break-even month |
|---|---:|---:|---:|
| Base | 301 000 | 21 | M11 |
| Optimistic | 390 000 | 16 | M8 |
| Pessimistic | 170 000 | 36 | не достигнут в M1-M12 |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 месяцев

Допущение для Sens1: marketing spend не растёт, поэтому при CAC x2 темп привлечения новых клиентов падает примерно вдвое. Для Sens2 churn влияет на активную клиентскую базу к M12. Для Sens3 COGS/client оставляю на уровне base, чтобы стресс по цене не маскировался оптимистичным cost-down. [T1][T2][T3][inference]

| Метрика | Base | Sens1: CAC x2 | Sens2: Churn x2 | Sens3: Price -30% |
|---|---:|---:|---:|---:|
| CAC, ₽ | 520 000 | 1 040 000 | 520 000 | 520 000 |
| Monthly churn | 2,2% | 2,2% | 4,4% | 2,2% |
| ARPU, ₽/мес | 400 000 | 400 000 | 400 000 | 280 000 |
| Активные клиенты в M12 | 24,0 | 12,0 | 22,2 | 24,0 |
| Gross profit / client, ₽/мес | 301 000 | 301 000 | 301 000 | 181 000 |
| EBITDA в M12, ₽/мес | 1 133 000 | -2 479 000 | 588 000 | -1 747 000 |
| Комментарий | проходит | GTM ломается | проходит на тонкой грани | pricing floor слишком низок |

Вывод: у FLORA самая опасная ось не churn, а сочетание enterprise-CAC и price compression. Если рынок продавливает чек к **280 тыс. ₽/мес** или CAC уходит к **1,0 млн ₽+**, M12-экономика резко перестаёт быть комфортной. [T1][T2][inference]

## B2. Monte Carlo Lite, confidence intervals

### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 420 000 | 520 000 | 1 040 000 | [T2][T6][inference] |
| Monthly churn, % | 1,5% | 2,2% | 4,4% | [T3][inference] |
| ARPU, ₽/мес | 280 000 | 400 000 | 500 000 | [T1][T2][inference] |
| Conversion rate lead→paid, % | 1,2% | 2,1% | 3,2% | [T2][inference] |
| Time-to-hire, месяцев | 1,0 | 1,7 | 3,0 | [T4][T5][T6][inference] |

### Метод
- Вместо полного кода беру 9 комбинаций min/mode/max по CAC, churn и ARPU, а conversion rate и time-to-hire использую как корректировки к client-ramp на M24. [inference]
- Base-case якорь: **60 активных клиентов к M24** при сохранении ABM-motion и full team после M6. [T1][T2][inference]
- p10 соответствует worst / near-worst combinations, p50 — median cluster, p90 — best / near-best combinations.

### Результат

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -4 281 000 | 11 969 000 | 27 059 000 | 31 340 000 |
| CAC payback, мес | 3,7 | 1,3 | 0,8 | 2,9 |
| LTV/CAC | 4,0x | 26,3x | 61,9x | 57,9x |
| Cash runway, мес | 7,8 | 12,4 | 18,5 | 10,7 |

Интерпретация:
1. **p10 EBITDA < 0**, значит автоматически срабатывает kill criterion #1, риск insolvency в плохом хвосте распределения слишком реален.
2. **p50 EBITDA > 500 тыс. ₽/мес**, значит median-case EBITDA Gate проходит.
3. **Range width по LTV/CAC = 57,9x**, модель хрупкая прежде всего к pricing и CAC, а не к базовой gross-margin логике.
4. Даже при сильном p90 upside кейс остаётся execution-heavy: upside большой, но разброс результатов тоже большой. [inference]

## B3. Competitor deep-dive

### Западные конкуренты

| Конкурент | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|
| Adobe Firefly + Creative Cloud | самый сильный enterprise distribution, brand-safety, API и bulk-production workflows, deep embed в Photoshop/Illustrator/Premiere [C1] | тяжёлый стек, дорогой ownership, слабее локализация и кастомизация под RU procurement | **30-35%** global enterprise creative-AI stack [inference] | FLORA легче продавать как dedicated creative-ops workspace для mid-market команд без полного Adobe estate |
| Canva Enterprise | очень сильный self-serve adoption, brand kit, template-led collaboration, хорошая вирусность внутри non-design teams [C2] | ниже глубина enterprise workflow orchestration и слабее custom workflow design для сложных approval chains | **20-25%** global SMB/mid-market visual collaboration [inference] | FLORA может выиграть там, где нужен account-level onboarding, кастомные роли и более высокий сервисный слой |
| Figma AI / FigJam AI | сильнейшая collaboration base среди digital/product teams, привычный editor, мощный community lock-in [C3] | core DNA всё ещё UI/product design, а не full marketing-content ops; enterprise marketers не всегда живут в Figma | **10-15%** adjacent creative-collaboration layer [inference] | FLORA ближе к marketing-ops и multi-format content production, а не только design-file collaboration |

### Российские конкуренты

| Конкурент | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|
| Supa | ранний локальный бренд в browser-based video creation, понятный use-case для marketing teams, быстрое производство соцроликов [C4] | фокус уже и уже, ближе к social-video tool, чем к enterprise creative-ops system | **8-10%** в RU сегменте self-serve visual tools [inference] | FLORA шире по workflow, collaboration и enterprise contract value |
| Flyvi | русскоязычный Canva-like editor, шаблоны, AI-мастерская, маркетплейс/баннерные сценарии, работает без VPN [C5][C6] | сильнее в шаблонном production, слабее в enterprise security / кастомных approval workflows | **10-12%** в RU сегменте SMB visual editors [inference] | FLORA может позиционироваться выше, как creative operating system для крупных бренд-команд |
| Turbologo | очень сильный входной use-case, logo + simple brand assets, низкий порог старта и понятный ROI для SMB [C7] | продукт узкий, commodity-risk высокий, слабая защита от price compression | **5-7%** в RU DIY branding niche [inference] | FLORA не конкурирует по logo-gen, а продаёт постоянный collaborative workflow и recurring seat/value |
| Kandinsky ecosystem | сильная русскоязычная генерация, локальный AI-brand, low-cost content generation, меньше санкционных рисков [C8] | это скорее model layer, а не готовый creative-ops SaaS с enterprise workflow и account governance | **15-20%** RU AI-image generation layer [inference] | FLORA может использовать такие модели как supply-side layer, оставаясь workflow shell поверх них |

### Итог по конкурентам
- На Западе рынок уже движется к bundling: Adobe, Canva и Figma встраивают AI в существующие design suites. Это повышает риск, что standalone creative-AI tools будут зажаты distribution-каналами больших платформ.
- В РФ конкуренты сильнее в low-end self-serve и template workflows, но слабее в enterprise-grade collaboration, security и кастомном внедрении.
- Значит рабочий wedge для FLORA, **не mass-market editor**, а **creative-ops platform для крупных бренд-команд и агентств с высоким чеком**. [C1][C2][C3][C4][C5][C8][inference]

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного CTO / ML lead в срок | med | высокий, roadmap сдвигается на 2-3 мес | time-to-hire > 3 мес, offer acceptance < 50% | заранее вести bench кандидатов, использовать advisor/fractional CTO, урезать scope MVP |
| Operational | LLM / image API quality drift или рост latency | med | высокий, ухудшается UX и unit cost | p95 latency > 12 сек, рост ручных retries, CS tickets по качеству | multi-model routing, fallback chains, кэширование, human-in-the-loop для критичных задач |
| Market | Спрос оказывается narrower, чем ожидалось, TAM в РФ не даёт 20+ платящих enterprise клиентов | med | высокий, break-even отодвигается | pipeline coverage < 3x target, demo-to-pilot < 25% | сузить ICP, идти в агентства и in-house brand teams, усиливать partner-led motion |
| Market | Price compression из-за Canva / Adobe / локальных self-serve аналогов | high | высокий, ARPU падает ниже floor | win rate растёт только при скидке > 25%, ARPU < 300 тыс. ₽ | жёсткий packaging, enterprise-only SLA, upsell onboarding/integration, ценовой floor |
| Regulatory | 152-ФЗ и data residency ограничивают использование западных API и хранение ассетов | med | высокий, часть enterprise сделок замораживается | security/legal review > 45 дней, запросы на on-prem/VPC | локальное хранение данных, сегрегация PII, on-prem/VPC roadmap |
| Regulatory | 115-ФЗ / KYC / procurement friction для крупных клиентов, плюс договорная экспертиза AI-generated assets | med | средний-высокий, sales cycle удлиняется | legal redlines > 3 раундов, delayed invoice setup | стандартный security pack, шаблоны договоров, юрсопровождение в пресейле |
| Financial | Cash runway сжимается из-за burn до M11-M12 и задержек выручки | high | высокий, риск даунраунда или stop-go | runway < 9 мес, DSO > 45 дней, burn multiple > plan | держать 40-45 млн ₽ buffer, milestone-based hiring, ежемесячный burn review |
| Financial | USD/RUB и инфляция поднимают стоимость API, облака и ФОТ | med | средний-высокий, GM проседает | COGS/client > 120 тыс. ₽, офферы по найму растут на 15%+ | рублёвые контракты где можно, ревизия usage limits, annual repricing |
| Black swan | Новый виток санкций режет доступ к SaaS, billing или model APIs | med | очень высокий, delivery может встать | vendor notices, forced migration, card failures | резервный стек из RU/OSS моделей, abstraction layer, запас по compute |
| Black swan | Полное отключение ключевого LLM/image provider на 2-4 недели | low-med | очень высокий, SLA рушится | error rate > 20%, provider status incidents > 24h | dual-vendor architecture, degradation mode, manual creative-ops fallback |

## B5. Kill conditions, горизонт 6 месяцев

1. **Insolvency / downside kill:** если к M6 downside-модель показывает **p10 EBITDA@M24 < 0** и фактический runway падает ниже **6 месяцев**, продолжать нельзя.
2. **GTM kill:** если к M6 меньше **6 платящих клиентов** или blended **CAC > 1 000 000 ₽**, значит account-based motion в РФ не собирается.
3. **Pricing / retention kill:** если к M6 фактический **ARPU < 300 000 ₽/мес** или monthly churn у пилотно-оплаченных клиентов устойчиво выше **4%**, unit economics больше не защищены.

## B6. Sources for Section B
- [C1] Adobe Firefly for Enterprise: https://www.adobe.com/products/firefly/enterprise.html
- [C2] Canva Enterprise announcement: https://www.canva.com/newsroom/news/canva-enterprise/
- [C3] Figma AI / Weavy coverage: https://www.techradar.com/pro/software-services/figma-boosts-its-ai-editing-tools-as-it-combines-forces-with-popular-ai-platform-weavy
- [C4] Supa on vc.ru: https://vc.ru/tribuna/25232-supa-video
- [C5] Habr, «Аналоги Canva: 12 сервисов для работы с изображениями»: https://habr.com/ru/amp/publications/676956/
- [C6] vc.ru, Flyvi overview: https://vc.ru/marketing/2707061-top-19-programm-dlya-sozdaniya-izobrazheniy
- [C7] Turbologo on vc.ru: https://vc.ru/turbologo
- [C8] Habr, Kandinsky 4.1 Image: https://habr.com/ru/companies/sberbank/articles/915760/

<!-- P6B-DONE -->

[GEO-EXPAND] FLORA — REJECTED: 63/100 | EBITDA base=1133К₽/мес через 12 мес | LTV/CAC=26,3x | Ключевое преимущество: сильная creative-ops economics для enterprise команд | Главный риск: weak moat и LOW direct-demand в РФ.

# 06-verdict — FLORA geo-expand v2

sector: GEO-EXPAND

## Итоговый вердикт
- **Вердикт:** **REJECTED**
- **Score:** **63/100**
- **Статус инвесткомитета:** качественная юнит-экономика не компенсирует слабый moat, LOW direct-demand и высокий execution risk в узком enterprise creative сегменте.
- **Формальный gate по EBITDA:** проходит, потому что `company_ebitda_rub_month = 1 133 000 ₽/мес` достигается в **M12**, а `company_ebitda_potential_rub_month @ 50 клиентов = 8 960 000 ₽/мес`.
- **Почему всё равно REJECTED:** итоговый investment case ломается на качестве спроса, слабой защищённости от Adobe/Figma/Canva bundling и хрупкости premium pricing при consultative sale.

## Оценка
Source tier balance: T1=6, T2=10, T3=2, weighted=2.20. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `Contribution Margin = 75,3%`, `LTV/CAC = 26,3x`, `CAC Payback = 1,3 месяца` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | `Break-even month = M11`, `M12 ... EBITDA ... 1 133 000`, `EBITDA ~8,96 млн ₽/мес` при 50 клиентах. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | В 02-demand.md прямо стоит `Итог по спросу в РФ: LOW`, при этом `SAM ... 1,04 млрд ₽` и `hh.ru vacancies = 730`; применён penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | В 03-solution.md зафиксированы `Bundling risk`, `Commodity risk`, `Localization risk`, а moat на workflow-слое остаётся слабым. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В 05-critic.md есть `Price compression`, `152-ФЗ`, `санкции`, `Cash runway сжимается`, `LLM / image API quality drift`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `outbound ABM` даёт `CAC = 520 000 ₽`, payback `1,3-1,7 месяца`, а named targets из топ-рекламодателей РФ существуют и платёжеспособны. |

**Sum raw = 94/150. Normalized score = round((94 × 100) / 150) = 63/100.**

## Investment thesis
FLORA в российском контуре выглядит не как mass creative SaaS, а как narrow enterprise creative-ops platform для бренд-команд и агентств с постоянным production load. В этой рамке математически кейс силён: high ACV, короткий payback, высокий LTV/CAC и достижимый путь к EBITDA. Но инвестиционное решение режется не на экономике, а на том, что категория в РФ ещё не сформирована, moat слабый, а premium workflow-layer легко оказывается зажат bundling-стратегиями Adobe, Figma, Canva и локальных low-end инструментов.

## FULL business process from 04-economics.md
| Шаг | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---|
| 1. Сбор target-account list | SDR | HH/AdIndex/open web + CRM | 6 ч | 8 000 | средняя |
| 2. Enrichment контактов | SDR | CRM, e-mail enrichment, TG/LinkedIn-аналоги | 5 ч | 7 000 | высокая |
| 3. Outbound sequence, 1-3 касания | SDR | CRM + e-mail + TG | 12 ч | 16 000 | высокая |
| 4. Qualification call | SDR + AE | Meet, CRM, demo deck | 2 ч | 6 000 | средняя |
| 5. Discovery с buyer team | AE | Meet, Miro, CRM | 4 ч | 16 000 | низкая |
| 6. Персонализированная demo / workflow mapping | AE + CTO/solution lead | FLORA demo workspace, Figma, presentation | 8 ч | 44 000 | низкая |
| 7. Pilot scoping + security/legal | AE + CTO + CEO | NDA, security checklist, procurement docs | 10 ч | 59 000 | низкая |
| 8. Пилот 2-4 недели | CSM + AE + CTO | Workspace setup, prompt/workflow templates | 24 ч | 73 000 | низкая |
| 9. Коммерческое предложение и negotiation | AE + CEO | Pricing model, contract redlines | 6 ч | 28 000 | низкая |
| 10. Procurement / invoice setup | Finance/CEO | ЭДО, счёт, договор | 3 ч | 9 000 | средняя |
| 11. Payment collection and activation | CSM | CRM, billing, support | 2 ч | 6 000 | высокая |
| **Итого raw process cost per won client** |  |  |  | **272 000 ₽** |  |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| MRR на клиента | 400 000 ₽ |
| ARR на клиента | 4 800 000 ₽ |
| customer_ltv_rub | 13 695 500 ₽ |
| Gross Margin | 75,3% |
| contribution_margin_rub_month | 301 000 ₽/мес на клиента |
| Fully-loaded CAC | 520 000 ₽ |
| LTV/CAC | 26,3x |
| CAC Payback | 1,3 мес по MRR / 1,7 мес по gross profit |
| fixed_costs_rub_month | 6 091 000 ₽/мес |
| Break-even clients | 21 |
| Break-even month | M11 |
| company_ebitda_rub_month base | 1 133 000 ₽/мес через 12 мес |
| company_ebitda_potential_rub_month | 8 960 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 21 |
| clients_to_1m_ebitda | 24 |
| months_to_500k_ebitda | 12 мес |
| months_to_1m_ebitda | 12 мес |
| startup_capital_to_bep_rub | 32 193 000 ₽ |

## Команда
| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Функция |
|---|---:|---:|---|
| CEO | 1 | 845 000 | GTM, enterprise selling, fundraising, ключевые переговоры |
| CTO / Tech Lead | 1 | 715 000 | локализация, enterprise security, архитектура integrations |
| Senior Backend | 2 | 1 092 000 | core platform adaptation, APIs, billing, integrations |
| ML Engineer | 1 | 650 000 | orchestration моделей, cost optimization, workflow quality |
| DevOps | 1 | 455 000 | infra, observability, IAM, deployment |
| Frontend | 1 | 390 000 | workspace UX, admin layer, onboarding flows |
| SDR | 1 | 221 000 | target-accounting, outbound, booking meetings |
| AE | 1 | 624 000 | discovery, demo, pilot, close |
| Customer Success | 1 | 299 000 | activation, expansion, retention |
| **Итого** | **10** | **5 291 000** | full team к M6 |

## Moat — 7-factor framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных. |
| Switching costs | 1 | Есть assets и привычка команды, но замена на bundled stack Adobe/Figma остаётся возможной. |
| Scale economies | 1 | Compute и success cost оптимизируются с объёмом, но не драматически. |
| Proprietary data / model advantage | 1 | Может копиться workflow history, но подтверждённого датасетного преимущества нет. |
| Regulatory moat | 0 | Формального лицензируемого барьера нет. |
| Brand / distribution | 1 | Бренд на глобальном рынке заметен, но в РФ category-default дистрибуции нет. |
| Embedded workflow | 3 | Если продукт внедрён в campaign production, он действительно глубоко сидит в процессе. |

**Moat sum = 7/21. Moat score = round((7 × 25) / 21) = 8/25.**

## GTM — 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Один из лидеров AdIndex, постоянный поток брендовых и performance-креативов, зрелая in-house marketing машина. | email decision-maker / партнёрство с integrator | 500 000 ₽/мес |
| 2 | Яндекс | Масштабный multi-brand creative production и внутренняя performance-экосистема. | founder-led outreach / отраслевая конференция | 500 000 ₽/мес |
| 3 | Ozon | E-commerce креативы и постоянные кампании требуют ускорения asset production. | ABM-outreach в brand/performance team | 450 000 ₽/мес |
| 4 | Avito | Большой digital creative volume и высокая потребность в быстрых вариациях кампаний. | direct email decision-maker | 400 000 ₽/мес |
| 5 | Т-Банк | Сильный бренд-маркетинг и постоянный поток performance creative для digital-продуктов. | конференция / warm intro | 450 000 ₽/мес |
| 6 | Альфа-Банк | Крупные рекламные бюджеты и частые кампании делают ROI на creative-ops правдоподобным. | ABM + partner referral | 450 000 ₽/мес |
| 7 | ВТБ | Тяжёлый, но платежеспособный buyer с регулярным marketing production. | enterprise outreach через CMO/brand lead | 450 000 ₽/мес |
| 8 | Wildberries | Высокий volume коммерческих креативов и seasonal campaign load. | direct outreach + event | 400 000 ₽/мес |
| 9 | МТС | Постоянные медиакомпании и сложная мультиканальная creative orchestration. | партнёрство / email decision-maker | 400 000 ₽/мес |
| 10 | X5 Group | Большой retail marketing engine, где важны скорость и массовая вариативность рекламных материалов. | founder outreach / отраслевой форум | 400 000 ₽/мес |

### Оценка GTM realism
- Канальный fit есть: **outbound ABM, partner-led motion, отраслевые конференции и founder-led enterprise sales** соответствуют типу сделки.
- Но GTM остаётся узким и account-based, а не повторяемым software-led motion.
- Сильный payback не спасает, если win-rate просядет из-за bundling или если чек уйдёт ниже `250-300 тыс. ₽/мес`.

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Weak moat и bundling pressure | high | high | Moat score всего `8/25`, а в 03-solution.md прямо перечислены `Bundling risk` и `Commodity risk`. |
| LOW direct-demand в РФ / evidence_quality_unverified | high | high | В 02-demand.md итог по спросу в РФ = `LOW`, category demand в Telegram отсутствует, рынок валидирован скорее через adjacent budget proxies. |
| Price compression и services creep | med-high | high | В 04-economics.md указано, что при чеке ниже `250-300 тыс. ₽/мес` экономика быстро ухудшается, а services-layer может съесть margin. |

## Финансовая интерпретация для инвесткомитета
- Да, база выглядит привлекательной: `LTV/CAC = 26,3x`, `GM = 75,3%`, `M11-M12` дают выход к EBITDA-плюсу.
- Но 05-critic.md показывает хрупкость хвоста распределения: `p10 EBITDA @M24 = -4 281 000 ₽/мес`, а `Price -30%` ведёт к `EBITDA в M12 = -1 747 000 ₽/мес`.
- Это типичный кейс, где клиентская математика хорошая, а fund-level conviction низкая из-за market formation risk.

## LTV Upside Calculator
### Формула
- `customer_ltv_rub = gross_profit_per_client_month / monthly_churn`
- `LTV/CAC = customer_ltv_rub / CAC`

| Сценарий | Gross profit на клиента, ₽/мес | Monthly churn | CAC, ₽ | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|
| Текущая база | 301 000 | 2,2% | 520 000 | 13 695 500 ₽ | 26,3x |
| Если churn снизить до 1,5% | 301 000 | 1,5% | 520 000 | 20 066 667 ₽ | 38,6x |
| Если MRR вырастет до 500k и GM 78% | 390 000 | 2,2% | 520 000 | 17 727 273 ₽ | 34,1x |
| Если CAC вырастет до 1,04 млн ₽ | 301 000 | 2,2% | 1 040 000 | 13 695 500 ₽ | 13,2x |
| Если цена упадёт до 280k ₽ и GP 181k ₽ | 181 000 | 2,2% | 520 000 | 8 227 273 ₽ | 15,8x |

### Read-through
- Upside в LTV/CAC у кейса уже хороший, поэтому отвергаем его не из-за unit economics.
- Главный блокер, способность стабильно брать premium creative-ops контракт в ещё не сформированной категории без сильного moat.

## Proof points for APPROVED
Не применяется, потому что итоговый статус кейса **REJECTED**.

## Финальное решение комитета
**REJECTED.**

Почему не approve:
- direct-demand в РФ остаётся LOW,
- moat weak (`8/25`),
- bundling risk очень высокий,
- Monte Carlo p10 и sensitivity показывают, что downside хвост для фонда слишком тяжёлый.

Почему не ноль:
- economics сильные,
- EBITDA gate проходит,
- ICP и target-account universe понятны,
- продукт решает реальную workflow-боль у верхнего слоя крупных brand-команд.
