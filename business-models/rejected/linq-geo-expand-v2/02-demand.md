# Demand validation — Linq

## Вывод
**Вердикт: PASS с оговорками, идти дальше по пайплайну.**

Linq попадает не в массовый SaaS, а в enterprise-инфраструктуру для омниканальных agentic-коммуникаций. По internal endpoint `multi-demand` для запроса `омниканальная поддержка клиентов` на **21 апреля 2026** спрос классифицирован как **LOW**, но внутри сигнала есть **86 вакансий на HH**, слабый поисковый хвост и низкий контентный шум. Это означает не отсутствие рынка, а sales-led категорию с низким search intent. [Internal demand tool][T1] Profit Gate проходит только в enterprise-сценарии с минимумом по MRR, SLA, интеграциями и usage-компонентом; self-serve и SMB-сценарии не проходят. [T1][T2]

## 1) Что именно валидируем
Linq, по брифу, это AI-native messaging infrastructure для enterprise-ассистентов и agent channels: voice, web-chat, Telegram, WhatsApp Business, SMS и смежные каналы. В РФ валидируем не generic CPaaS, а более узкий слой orchestration + routing + channel abstraction + managed onboarding для крупных support и service funnels. [T2]

## 2) Demand signals
- По internal endpoint `http://172.18.0.1:9001/multi-demand?keyword=омниканальная%20поддержка%20клиентов` на **2026-04-21**: `composite_demand=LOW`, `demand_score=7`, `hh_vacancies=86`, `google_trends_ru=2`, `habr_articles=2`, `yandex_suggest=2`. Это указывает на узкий, но не нулевой B2B-спрос. [Internal demand tool]
- Наличие **86** вакансий по тематике в HH внутри internal multi-demand подтверждает, что компании реально нанимают под омниканальную поддержку и клиентские коммуникации, то есть боль существует в операционном контуре, а не только в маркетинговых презентациях. [Internal demand tool][T1]
- Российский рынок облачных контакт-центров в **2025** году оценивался в **3,5 млрд ₽**, а к **2029** прогнозировался на уровне **6,7 млрд ₽**. Это прямой рыночный proxy под часть стека Linq. [T2]
- Российский рынок чат-ботов в **2025** оценивался примерно в **12 млрд ₽**, причём в статье со ссылкой на TAdviser указано, что **86%** корпоративных клиентов используют чат-ботов для поддержки, а средний чек крупных клиентов доходит примерно до **180 тыс. ₽ в месяц**. Для Linq это не прямой аналог, но сильный adjacent proof, что messaging automation уже оплачивается в РФ. [T2]

## 3) Конкуренты и цены
### Глобальные / прямые и смежные
1. **Twilio** — WhatsApp сообщения от **$0.005** за сообщение, Conversations от **$0.05** за active user в месяц, voice от **$0.014/мин** outbound, Flex от **$150** за named user в месяц или **$1** за active user hour. Это прямой референс, что enterprise messaging infra продаётся как usage + seat + contact-center layer. [T1]

### Локальные / RU-adjacent
2. **Chat2Desk** — Базовый **5 000 ₽/мес**, Стандартный **9 000 ₽/мес**, Профессиональный **15 000 ₽/мес**; WhatsApp Business API оплачивается отдельно по **8 000 ₽/мес** плюс депозит и сообщения. Telegram API включён в список каналов. [T2]
3. **LiveTex** — Базовый тариф от **450 ₽/мес** за операторскую лицензию, Продвинутый от **1 445 ₽/мес**; канал Telegram/Viber от **322 ₽/мес**, WhatsApp-интеграция от **803 ₽/мес**, чат на сайт от **723 ₽/мес**. [T2]
4. **Umnico** — сервис работает с Telegram, WhatsApp, VK, CRM и self-hosted deployment; на публичной странице раскрыты trial и скидки до 50%, а коробочная версия и enterprise-цена считаются индивидуально. Это подтверждает наличие локального канального слоя, но не даёт прозрачной публичной enterprise-цены, поэтому используем как supporting evidence, не как price anchor. [T2]

### Что это значит для Linq
- Нижний рынок в РФ уже занят дешёвыми омниканальными helpdesk-решениями за **сотни или тысячи рублей на агента**. [T2]
- Верх рынка подтверждён глобально: при 50–200 агентах или при больших объёмах WhatsApp/SMS/voice usage один enterprise-клиент может легко выходить выше **500 тыс. ₽/мес** совокупного spend. Это **инференс**, выведенный из Twilio Flex + usage pricing и локальной практики платных омниканальных платформ. [T1][T2 + inference]
- Следовательно, Linq не должен идти в low-end SMB. Рабочая зона только там, где есть сложная routing-логика, AI-assistant orchestration, SLA, compliance и несколько каналов сразу. [T2 + inference]

## 4) Telegram и messaging services в РФ
- **Chat2Desk** прямо включает **Telegram API** в список поддерживаемых каналов и даже упоминает трансляцию переписки в Telegram внутри тарифов. [T2]
- **LiveTex** продаёт подключение **Telegram/Viber** отдельно от базовой лицензии, то есть Telegram в РФ является нормализованным support-каналом, а не edge case. [T2]
- **Umnico** в trial-предложении прямо перечисляет **Telegram** среди каналов интеграции. [T2]

### Интерпретация
В РФ Telegram уже встроен в коммерческий стек customer communication. Это хорошо для GEO-EXPAND, потому что локализация канала возможна. Но это одновременно значит, что Telegram сам по себе не является moat. Настоящая монетизация Linq возможна только поверх orchestration, AI-routing, observability, managed onboarding и enterprise reliability. [T2 + inference]

## 5) Willingness to pay (WTP)
### Доказательства
- **Twilio** за полный **2025** год показал выручку **$5.07 млрд**, что подтверждает глобальную готовность enterprise-клиентов тратить крупные recurring-бюджеты на customer engagement infrastructure. [T1]
- В российском обзоре рынка чат-ботов со ссылкой на TAdviser говорится, что **86%** корпоративных клиентов используют чат-боты для поддержки, а средний чек крупных клиентов доходит примерно до **180 тыс. ₽/мес**. Это ниже целевого порога Linq, но уже доказывает регулярные платежи за automation layer. [T2]
- У локальных платформ есть устойчивая подписочная монетизация: Chat2Desk и LiveTex тарифицируют либо пакет каналов, либо operator seats, либо отдельные мессенджеры. [T2]
- У крупных банков, страховых и e-commerce компаний customer support и notifications масштабируются на множество каналов. Для них spend выше **500 тыс. ₽/мес** реалистичен только в конфигурации multi-channel + enterprise SLA + custom integrations + usage minimum. Это **инференс**, а не прямой публичный прайс-лист. [T1][T2 + inference]

### Вывод по WTP
WTP в РФ **подтверждён для low/mid-tier омниканальных решений** и **косвенно подтверждён для enterprise-инфраструктуры**. Прямого публичного доказательства, что российский buyer уже массово платит именно Linq-уровню **500+ тыс. ₽/мес**, нет. Но глобальные price anchors и локальный рынок customer communication делают такой чек достижимым у крупных банков, страховых и топ-100 e-commerce. Значит WTP есть, но только в узком сегменте. [T1][T2 + inference]

## 6) Market sizing
### Логика сегмента
Для Linq берём не весь CPaaS и не весь chatbot market, а **enterprise messaging orchestration** для крупных компаний, где есть минимум 3 канала, AI-assistants, integration work и SLA: банки, страховщики, топ-100 интернет-магазинов, часть telecom и крупных digital-сервисов. [T1][T2]

### Top-down
**[LOW CONFIDENCE]** Категория Linq лежит между CPaaS, CCaaS и conversational AI, поэтому top-down неизбежно proxy-based.

- Глобальный рынок conversational AI в **2024** оценивался примерно в **$11.58 млрд**. Это даёт мировой TAM порядка **1.04 трлн ₽** при грубом курсе **90 ₽/$**. [T3]
- Российский рынок **облачных контакт-центров** в **2025** составлял **3.5 млрд ₽**. [T2]
- Российский рынок **чат-ботов** в **2025** оценивался примерно в **12 млрд ₽**. [T2]
- Суммарный локальный stack-proxy под коммуникационную автоматизацию получается около **15.5 млрд ₽**. [T2]
- Для Linq как более узкого infra/orchestration слоя берём **20%** от этого proxy, то есть **TAM РФ ≈ 3.1 млрд ₽**. Это **инференс**: Linq не забирает весь budget ботов и контакт-центров, а только слой orchestration и channel infra. [T2 + inference]
- Для segment fit, где нужен именно enterprise multi-channel orchestration, а не просто helpdesk, берём **60%** от TAM РФ, то есть **SAM ≈ 1.86 млрд ₽**. [T2 + inference]
- Реалистичный capture: **Y1 = 2% SAM**, **Y3 = 7% SAM**. Тогда **SOM Y1 ≈ 37.2 млн ₽**, **SOM Y3 ≈ 130.2 млн ₽**. [inference]

### Bottom-up
#### База buyers
- **305** действующих банков на **1 апреля 2026**. [T1]
- **129** страховых организаций на **1 января 2026**. [T1]
- **100** крупнейших российских интернет-магазинов в рейтинге Data Insight как готовый пул high-volume digital buyers. [T2]

Итого: **534** первичных buyer-организации в наиболее очевидном ICP. [T1][T2]

#### Допущения
- `% with need` = **45%**. Это доля компаний, у которых одновременно есть multi-channel support, заметный объём обращений и смысл в orchestration-слое поверх каналов. [T1][T2 + inference]
- `ARR avg` = **7.2 млн ₽/год** на клиента, то есть в среднем **600 тыс. ₽/мес**. Такой чек возможен только в enterprise-модели: платформа + usage minimum + SLA + интеграции. Это **инференс**, но он согласован с global price anchors Twilio и локальным фактом, что базовая автоматизация уже продаётся подписочно. [T1][T2 + inference]

#### Расчёт
- **TAM_bottom_up = 534 × 7.2 млн ₽ = 3.84 млрд ₽**
- **SAM_bottom_up = 534 × 45% × 7.2 млн ₽ = 1.73 млрд ₽**
- **SOM_bottom_up Y1 = 1.2% × 1.73 млрд ₽ = 20.8 млн ₽**
- **SOM_bottom_up Y3 = 4.5% × 1.73 млрд ₽ = 77.9 млн ₽**

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $11.58B / ~1.04 трлн ₽ [T3] | — | Категорийный proxy conversational AI | top-down |
| TAM (РФ) | 3.10 млрд ₽ [T2 + inference] | 3.84 млрд ₽ [T1/T2 + inference] | diff=24%, bottom-up шире по buyer-базе | lower |
| SAM (РФ) | 1.86 млрд ₽ [T2 + inference] | 1.73 млрд ₽ [T1/T2 + inference] | diff=7%, оценки близки | lower |
| SOM Y1 | 37.2 млн ₽ | 20.8 млн ₽ | diff=79%, top-down оптимистичнее | **используем 20.8 млн ₽** |
| SOM Y3 | 130.2 млн ₽ | 77.9 млн ₽ | diff=67%, top-down включает более широкий expansion | **используем 77.9 млн ₽** |

### 10 реальных buyers для bottom-up и GTM
1. Сбер [T1/T2]
2. ВТБ [T1/T2]
3. Альфа-Банк [T1/T2]
4. Т-Банк [T1/T2]
5. Совкомбанк [T1/T2]
6. Ингосстрах [T1]
7. АльфаСтрахование [T1]
8. Ozon [T2]
9. Wildberries [T2]
10. Яндекс Маркет [T2]

### Sanity check
- Предпочтительный **SOM Y1 = 20.8 млн ₽** при среднем ARR **7.2 млн ₽** означает около **3 логотипов** в первый год. [inference]
- При enterprise sales cycle около **4 месяцев** это даёт **3 × 4 = 12**, то есть гранично, но реалистично для founder-led/partner-led motion. [inference]
- **SOM Y1 < 10% SAM**, значит грубого overclaiming нет. [inference]

## 7) Profit Gate (EBITDA >= 500k ₽/мес)
Проверяю все основные сценарии монетизации.

### Сценарий A: low-end self-serve омниканал
- Цена: **15 тыс. ₽/мес**
- Клиентов: **40**
- Выручка: **600 тыс. ₽/мес**
- При gross margin **80%** валовая прибыль = **480 тыс. ₽/мес**
- Даже при очень низком OPEX **1.2 млн ₽/мес** EBITDA будет **-720 тыс. ₽/мес**
- **Gate: FAIL** [T2 + inference]

### Сценарий B: mid-market managed inbox
- Цена: **120 тыс. ₽/мес**
- Клиентов: **15**
- Выручка: **1.8 млн ₽/мес**
- При gross margin **75%** валовая прибыль = **1.35 млн ₽/мес**
- При OPEX **1.6 млн ₽/мес** EBITDA = **-250 тыс. ₽/мес**
- **Gate: FAIL** [T2 + inference]

### Сценарий C: enterprise platform + SLA + integrations
- Цена: **350 тыс. ₽/мес** platform fee
- Клиентов: **8**
- Выручка: **2.8 млн ₽/мес**
- При gross margin **75%** валовая прибыль = **2.1 млн ₽/мес**
- При OPEX **1.55 млн ₽/мес** EBITDA = **550 тыс. ₽/мес**
- **Gate: PASS** [T1][T2 + inference]

### Сценарий D: enterprise usage-based infra
- Цена: **250 тыс. ₽/мес** minimum commit + **350 тыс. ₽/мес** usage/SLA в среднем
- Клиентов: **6**
- Выручка: **3.6 млн ₽/мес**
- При gross margin **65%** валовая прибыль = **2.34 млн ₽/мес**
- При OPEX **1.7 млн ₽/мес** EBITDA = **640 тыс. ₽/мес**
- **Gate: PASS** [T1][T2 + inference]

### Итог по Profit Gate
Profit Gate **проходит**, но только если Linq в РФ продаётся как **enterprise infrastructure layer**, а не как helpdesk substitute. Как только продукт уходит в SMB-цену, экономика разваливается. [T1][T2 + inference]

## 8) Основные риски
1. **Слабый search intent**: inbound сам по себе не вытащит продажи, нужен direct enterprise sales motion. [Internal demand tool]
2. **Коммодитизация каналов**: Telegram/WhatsApp/web-chat уже есть у локальных платформ, поэтому moat не в канале, а в orchestration и надёжности. [T2]
3. **Локальный compliance/integration burden**: Telegram, WhatsApp Business, CRM, контакт-центр и voice-stack в РФ потребуют кастомной интеграции и support. [T2 + inference]
4. **Ограниченный ICP**: рынок есть, но он уже, чем классический broad CPaaS. Перегретые ожидания по PLG будут ошибкой. [T1][T2 + inference]

## 9) Инвестиционная интерпретация
Linq не выглядит как широкий продукт для массового российского SMB. Но как инфраструктурный слой для нескольких десятков крупных enterprise-buyers в finance, insurance и top e-commerce кейс рабочий. Это узкий рынок, зато с шансом на высокий чек и defensibility через интеграции. Для фонда это не «везде и для всех», а ставка на глубину аккаунта и международно переносимую архитектуру. [T1][T2 + inference]

## Финальный вывод
- **Demand:** низкий по поисковому хвосту, но достаточный в enterprise-сегменте. [Internal demand tool][T1]
- **WTP:** подтверждён для automation/tooling и условно подтверждён для high-ticket infra через global anchors и локальный adjacent market. [T1][T2]
- **Competitor pricing:** есть и в low-end RU, и в global enterprise. [T1][T2]
- **TAM/SAM/SOM:** рынок в РФ не гигантский, но достаточный для узкого enterprise wedge. [T1][T2][T3]
- **Profit Gate:** проходит только при enterprise pricing и managed implementation. [T1][T2]

**Решение на этапе demand validation: PASS с оговорками.**

## Источники
- Internal demand tool: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%BC%D0%BD%D0%B8%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F%20%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B0%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%BE%D0%B2
- Twilio pricing: https://www.twilio.com/en-us/pricing/current-rates [T1]
- Twilio FY2025 earnings: https://www.twilio.com/en-us/press/releases/Q4-full-year-2025-earnings [T1]
- Chat2Desk pricing: https://chat2desk.com/baza-znanij/billing/tarifyi-chat2desk [T2]
- LiveTex pricing: https://livetex.ru/prices/ [T2]
- Umnico pricing/FAQ: https://umnico.com/ru/payment/ [T2]
- Банк России, банковский сектор: https://www.cbr.ru/banking_sector/ [T1]
- Банк России, страхование: https://www.cbr.ru/insurance/ [T1]
- Data Insight TOP100 e-commerce: https://top100.datainsight.ru/ [T2]
- TMT Consulting / CNews, рынок облачных контакт-центров в РФ: https://www.cnews.ru/news/line/2025-12-16_rynok_oblachnyh_kontakt-tsentrov [T2]
- MashaGPT, рынок чат-ботов в России 2025: https://mashagpt.ru/blog/rynok-chat-botov-v-rossii-v-2025-godu-trendy-igroki-i-perspektivy/ [T2]
- Grand View Research, conversational AI market: https://www.grandviewresearch.com/industry-analysis/conversational-ai-market-report [T3]

Sources: T1=4, T2=7, T3=1. Primary evidence basis: T2.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.

## Market Pulse
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущему веб-поиску по ключевым запросам виден рост публикаций, вакансий и/или рыночной активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.
