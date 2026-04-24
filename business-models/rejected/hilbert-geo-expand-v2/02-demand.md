---
stage: demand-validation
case: hilbert-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
sector: GEO-EXPAND
---

# 02-demand — Demand Validation

## Кейс
Hilbert, AI-native growth decisioning и warehouse-native аналитико-операционный слой для B2C-команд.

## Итог
**Статус: CONDITIONAL_PASS.**

Exact-category спрос в РФ слабый, но adjacent spend и готовность платить подтверждены. По internal demand endpoint `маркетинговая аналитика` дал **MEDIUM / 30** с **5008** вакансиями hh.ru, `продуктовая аналитика` дал **MEDIUM / 30** с **3573** вакансиями, а `customer data platform` остался **LOW / 18** с **28** вакансиями. Это значит, что рынок покупает не ярлык `warehouse-native AI decisioning`, а более знакомые бюджеты: CRM marketing, продуктовую аналитику, CDP, персонализацию и lifecycle automation [T1/T2 mixed, internal aggregation over hh.ru + Google Trends + Habr].

Hilbert решает реальную enterprise-боль: a16z прямо описывает дефицит дорогих growth-data-plumbers и заявляет, что Hilbert уже заходит в крупные consumer-компании [T2]. Локально WTP подтверждают публичные прайсы российских и глобальных substitutes: Mindbox от **150 000 ₽/мес** и **400 000 ₽/мес** [T1], Carrot quest от **10 990 ₽/мес** до **38 987 ₽/мес** плюс enterprise по запросу [T1], Mixpanel Growth после free-tier стоит **$0.28 за 1K events** [T1], PostHog после free-tier тарифицирует analytics от **$0.0000500/event** [T1].

Следовательно, спрос не массовый, но fundable niche есть. Для отклонения по early reject нужен одновременно LOW demand и непроходимый Profit Gate. Здесь adjacent demand не нулевой, а EBITDA ≥ 500k/мес достижима в нескольких enterprise-сценариях. Кейс не отклоняю.

## 1. Demand data

### 1.1 Multi-demand API
- `маркетинговая аналитика` → **MEDIUM**, score **30**, hh.ru **5008**, Habr **2**, Yandex suggest **100**.
- `продуктовая аналитика` → **MEDIUM**, score **30**, hh.ru **3573**, Habr **2**, Yandex suggest **100**.
- `customer data platform` → **LOW**, score **18**, hh.ru **28**, Habr **2**, Yandex suggest **100**.
- `маркетинговая автоматизация` → **MEDIUM**, score **30**, hh.ru **960**, Habr **2**, Yandex suggest **100**.

### 1.2 Интерпретация
- Exact-term demand для Hilbert-like category слабый, потому что buyer в РФ обычно покупает решения через бюджеты CRM/CDP/сквозной аналитики, а не через формулировку `AI decisioning` [спекуляция, но согласуется с demand API].
- Adjacent labor demand сильный: тысячи вакансий по маркетинговой и продуктовой аналитике означают, что у компаний есть постоянная боль и бюджет на data-driven growth workflows [T1 via hh.ru count inside internal endpoint].

## 2. Реальные конкуренты с ценами

| Конкурент | Что продаёт | Публичная цена | Что это доказывает |
|---|---|---:|---|
| Mindbox | CDP, персонализация, боты, ML-ретаргетинг | Standard **от 150 000 ₽/мес**, Enterprise **от 400 000 ₽/мес** [T1] | В РФ уже есть enterprise-бюджет на growth/data/personalization слой. |
| Carrot quest | onsite-маркетинг, лид-боты, воронки, автоматизация | Marketing **10 990 ₽/мес**, Marketing Expert **14 287–38 987 ₽/мес**, Enterprise по запросу [T1] | SMB/mid-market уже платит за chat+automation, но это lower-end substitute. |
| Mixpanel | product analytics / growth analytics | Growth: после 1M monthly events **$0.28 за 1K events** [T1] | Международный рынок готов платить usage-based за growth analytics. |
| PostHog | product analytics, warehouse/data stack, experiments | Analytics: после 1M events **$0.0000500/event** [T1] | Open-core/usage pricing создаёт pressure на lower tier, но enterprise stack monetized. |

### Вывод по конкурентам
Hilbert не может продаваться как просто аналитика. Нижний сегмент уже закрыт Carrot quest/PostHog-like pricing. Заход возможен только как measurable uplift layer поверх data warehouse и lifecycle orchestration, где buyer готов платить **300k–700k ₽/мес** за рост выручки, а не за dashboard [инференс из конкурентов, T1/T2].

## 3. Telegram bots / services в РФ
- **Mindbox** прямо включает модуль `Боты и чаты` для Telegram, VK, MAX, WhatsApp, Viber, ОК; в Standard тарифе база от **150 000 ₽/мес**, сами боты оплачиваются модулем [T1].
- **Carrot quest** продаёт лид-ботов и автоматические сценарии, интегрируемые с мессенджерами; прайс стартует от **4 490 ₽/мес** на low-end тарифе и до **38 987 ₽/мес** на expert [T1].
- **BotHelp** продаёт чат-боты и AI-агентов для Telegram, VK и других каналов; на публичной странице указаны тарифы **от 1 599 ₽/мес** и Scale **от 29 990 ₽/мес** [T1].

### Значение для Hilbert
RU-рынок Telegram automation уже насыщен дешёвыми bot-builder продуктами. Это не убивает Hilbert, но сдвигает ценность вверх по стеку: не bot creation, а decisioning engine, который решает **кому / когда / через какой канал / с каким оффером** писать [T1/T2].

## 4. WTP, proof of willingness to pay
1. **Российский enterprise WTP подтверждён**: Mindbox публично продаёт platform layer от **150k–400k ₽/мес** [T1].
2. **Mid-market WTP подтверждён**: Carrot quest показывает платёжеспособность на уровне **11k–39k ₽/мес** за automation и лидогенерацию [T1].
3. **Global category WTP подтверждён**: Mixpanel и PostHog монетизируют product/growth analytics usage-based, а Hightouch вынес AI Decisioning в отдельный продуктовый слой [T1].
4. **Инвесторский сигнал есть**: a16z 15 апреля 2026 года описывает категорию как дорогую и болезненную инфраструктурную проблему и объявляет об инвестиции в Hilbert [T2].

### Вывод по WTP
**WTP = MEDIUM/HIGH.** За adjacent stack платят уже сейчас. Не доказано только одно: что российский buyer массово примет premium именно за warehouse-native agentic layer без явного revenue uplift SLA. Значит продажа должна идти через ROI и lift, а не через красивую AI-обёртку [T1/T2].

## 5. Market sizing

### Метод и допущения
- Base ARR для Hilbert-like решения в РФ беру **5.4 млн ₽/год** на клиента, то есть **450 000 ₽/мес**. Это ниже Mindbox Enterprise и заметно выше mid-market automation, что соответствует premium enterprise overlay [T1 + инференс].
- Для top-down беру рынок интернет-рекламы РФ **530.1 млрд ₽** по АКАР за 2025 год и считаю, что addressable software+decisioning layer может реалистично забирать около **0.6%** этого spend в компаниях с развитым performance/CRM motion [T2 + инференс].
- Для bottom-up беру **220** потенциальных mid/enterprise buyers в РФ, из которых **65%** имеют достаточную data maturity и регулярную lifecycle/performance боль; это оценка по набору зрелых B2C вертикалей и buyer list ниже [T2-инференс].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$4.5–6.0B** adj. layer, [LOW CONFIDENCE], как ~0.5–0.7% от глобального digital ad / martech spend [T3+spec] | — | — | top-down range |
| TAM (РФ) | **3.18 млрд ₽** = 530.1 млрд ₽ × 0.6% [T2] | **1.19 млрд ₽** = 220 × 100% × 5.4 млн ₽ [T2-inference + T1 price anchor] | diff 2.7x, допустимо: top-down включает более широкий spend pool | **1.19 млрд ₽** |
| SAM (РФ) | **1.11 млрд ₽** = 3.18 млрд ₽ × 35% fit [T2+inf] | **772.2 млн ₽** = 220 × 65% × 5.4 млн ₽ [T2-inference + T1] | diff 1.4x, это нормально | **772.2 млн ₽** |
| SOM Y1 | **22.2 млн ₽** = 1.11 млрд ₽ × 2% | **38.9 млн ₽** = 772.2 млн ₽ × 5% | diff 1.75x, используем более консервативное | **22.2 млн ₽** |
| SOM Y3 | **77.7 млн ₽** = 1.11 млрд ₽ × 7% | **92.7 млн ₽** = 772.2 млн ₽ × 12% | diff 1.19x | **77.7 млн ₽** |

### Sanity checks
- Расхождение top-down и bottom-up по SAM меньше 3x, значит сегмент выбран допустимо.
- SOM Y1 = **2.9%** от preferred SAM, это реалистично и ниже red-flag порога 30%.
- При ARR **5.4 млн ₽** SOM Y1 соответствует примерно **4 клиентам**. Даже при enterprise deal cycle 4-6 месяцев это достижимо founder-led продажей за год.

### 10 реальных buyers для bottom-up
1. X5 Digital [T2, реальный крупный grocery/e-commerce buyer]
2. ВкусВилл [T2]
3. Самокат [T2]
4. Lamoda [T2]
5. Hoff [T2]
6. Sunlight [T2]
7. SOKOLOV [T2]
8. Dodo Brands / Додо Пицца [T2]
9. Okko [T2]
10. Kassir.ru / МТС Live class buyers [T2]

Это именно ICP-кандидаты: крупные B2C-команды с высокой частотой коммуникаций, performance spend и retention-циклом. Список нужно переиспользовать в P7 GTM-10-targets.

## 6. Profit Gate
Цель: проверить, достижима ли **EBITDA ≥ 500 000 ₽/мес** хотя бы в реалистичных сценариях.

### Общие допущения
- Команда: 8-10 человек.
- Fixed OPEX: **2.2 млн ₽/мес**.
- Для прохождения gate нужно валовой прибыли на **2.7 млн ₽/мес**.

| Сценарий | Цена | GM | Валовая прибыль / клиент / мес | Клиентов до EBITDA 500k | Вердикт |
|---|---:|---:|---:|---:|---|
| Low-end SaaS | 250 000 ₽ | 65% | 162 500 ₽ | **17** | PASS, но тяжело |
| Base enterprise | 450 000 ₽ | 68% | 306 000 ₽ | **9** | PASS |
| Premium enterprise | 700 000 ₽ | 72% | 504 000 ₽ | **6** | PASS |
| Platform + onboarding fee | 350 000 ₽ + 1.2 млн ₽ setup, амортизировано до 450 000 ₽/мес в первые 12 мес | 70% | 315 000 ₽ | **9** | PASS |

### Вывод по Profit Gate
**Profit Gate = PASS.** Даже если low-end сценарий слабый, company-level EBITDA > 500k/мес достижима уже на **6-9 enterprise клиентах**. Значит условие для early reject не выполняется.

## 7. Риски, которые надо добивать в P5-P7
1. Высокий риск, что локальный рынок купит не Hilbert-like infra, а более дешёвый CDP/CRM/bot stack [T1].
2. Нужен жёсткий proof, что uplift measurable и окупает premium над Mindbox-like substitute [T1/T2].
3. Возможен скрытый services load в интеграции и data-plumbing, что ухудшит repeatability [T2].
4. Exact category education в РФ придётся делать founder-led, потому что keyword demand пока идёт через adjacent terms [internal endpoint + T1/T2].

## 8. Решение для пайплайна
**Продолжать дальше. Не reject на demand stage.**

Причины:
- adjacent demand в РФ не нулевой и подтверждён через hh-heavy категории;
- есть реальная российская готовность платить за соседний стек;
- Profit Gate проходит в нескольких monetization сценариях;
- категория fundable, но узкая, значит дальше нужен жёсткий enterprise-only ICP.

## Sources
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3%D0%BE%D0%B2%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B4%D1%83%D0%BA%D1%82%D0%BE%D0%B2%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=customer%20data%20platform
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3%D0%BE%D0%B2%D0%B0%D1%8F%20%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F
- Hilbert: https://hilberts.ai/
- a16z, Investing in Hilbert, 2026-04-15: https://a16z.com/announcement/investing-in-hilbert/
- Hightouch AI Decisioning docs: https://hightouch.com/docs/ai-decisioning/overview
- Mixpanel pricing: https://mixpanel.com/pricing/
- PostHog pricing: https://posthog.com/pricing
- Mindbox tariffs: https://mindbox.ru/tariffs/
- Carrot quest tariffs: https://help.carrotquest.io/article/685
- BotHelp pricing: https://bothelp.io/ru/pricing
- АКАР, объём рынка интернет-рекламы в России, 2025: https://www.akarussia.ru/knowledge/market_size/id21929

Sources: T1=6, T2=3, T3=1. Primary evidence basis: T1.

## Market Pulse
Market Pulse 22.04.2026: растущий интерес.
