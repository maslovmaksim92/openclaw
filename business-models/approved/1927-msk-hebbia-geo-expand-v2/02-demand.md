# 02-demand

## Demand validation summary
- **Итог по спросу:** **MEDIUM**. Прямой брендовый спрос на Hebbia в РФ почти отсутствует, но спрос на класс решения, то есть AI-поиск по документам, knowledge assistant и RAG в закрытом контуре, уже подтверждается вакансиями, локальными платными продуктами и ростом корпоративного GenAI-рынка. [Internal][T1][T2]
- **Решение для фонда:** кейс **не проходит Early Reject**, потому что при слабом бренд-запросе у категории есть коммерческий рынок в РФ, а Profit Gate достижим в нескольких сценариях. [Internal][T2]
- **Ключевая оговорка:** в РФ вероятнее зайдёт не «Hebbia как бренд», а локализованный enterprise knowledge copilot для банков, телекома, промышленности и крупных сервисных компаний, желательно on-prem или в закрытом контуре. [T2]

## Product and buyer hypothesis
Hebbia по сути продаёт AI-слой над корпоративными документами: поиск, извлечение инсайтов, cited answers, work with internal knowledge, аналитические workflows для knowledge workers. Для РФ это не SMB-инструмент, а B2B-продукт для средних и крупных компаний с большим массивом внутренних документов и высокими требованиями к доступам и безопасности. [T2]

**Наиболее вероятные buyers в РФ:**
1. Сбер
2. Т-Банк
3. ВТБ
4. Альфа-Банк
5. МТС
6. ВымпелКом (билайн)
7. Северсталь
8. Норникель
9. СИБУР
10. X5 Group

Это и есть GTM-10 targets для bottom-up расчёта: все 10 компаний крупные, документно-интенсивные и уже активно автоматизируют knowledge-work и внутренние сервисы. [T2]

## Demand evidence
### 1) Internal demand probe
Проверка `multi-demand` по релевантным ключам дала смешанную картину:
- `Hebbia enterprise AI knowledge assistant` -> composite_demand=LOW, score=0. [Internal]
- `AI поиск по документам для компаний` -> composite_demand=LOW, score=7, при этом **hh_vacancies=179**. Это значит, что пользовательский поисковый шум низкий, но B2B hiring signal уже есть. [Internal]
- `юридический AI copilot для документов` -> composite_demand=LOW, score=0. [Internal]

**Вывод:** в РФ это не search-led рынок, а sales-led enterprise рынок. Для такого сегмента Google Trends/Yandex suggest недооценивают реальную платёжеспособность, а hh-сигнал и наличие платных локальных решений более показательные. [T1][Internal]

### 2) Hiring and market activity
- На hh.ru по релевантному запросу из internal demand probe найдено **179 вакансий**, связанных с AI-поиском по документам/корпоративным знаниям. Это прямой признак того, что компании уже тратят бюджет на внедрение подобных систем. [T1][Internal]
- CNews со ссылкой на Yandex B2B Tech сообщает, что рынок GenAI-решений в РФ в 2024 году вырос до **58 млрд ₽**, то есть корпоративный бюджет на прикладной AI уже сформирован. [T2]
- Росстат публиковал, что в январе-сентябре 2025 года финансовый результат организаций составил **24.1 трлн ₽ прибыли** и **17.2 тыс. убыточных** против **46.4 тыс. прибыльных** организаций, что косвенно задаёт верхнюю границу числа средних и крупных компаний, способных покупать enterprise software. [T1]

## Competitors with prices
### Direct and adjacent competitors in RF-accessible market
| Конкурент | Что продаёт | Прайс | Комментарий |
|---|---|---:|---|
| Yandex Search API / AI Search | поиск + генеративные ответы поверх поиска/данных | **5,080 ₽ за 1,000 генеративных запросов** в Search API [T1] | инфраструктурный building block, а не готовый analyst copilot |
| TEAMLY | база знаний + AI-ассистент для компании | **299 ₽/редактор/мес** за тариф Start и **399 ₽/редактор/мес** за Business; enterprise AI в закрытом контуре по запросу [T2] | локальная альтернатива для internal knowledge workflows |
| Just AI JAICP | conversational AI / knowledge bots / RAG c on-prem | **21,450 ₽/мес** Start Chat, **26,950 ₽/мес** Start Calls, Enterprise по запросу [T2] | особенно силён там, где важны боты и омниканальные каналы |
| BotHelp | чат-боты и автоворонки в мессенджерах | от **1,000 ₽/мес** и выше по публичным тарифам [T2] | ближе к TG/distribution layer, чем к Hebbia, но конкурирует за бюджет автоматизации диалогов |

**Вывод по конкурентам:** рынок не пустой. В РФ уже есть минимум три платных способа закрывать adjacent job-to-be-done: knowledge base + AI, AI-боты с RAG, AI-search infrastructure. Значит, WTP существует, но окно для Hebbia-подобного игрока лежит выше по стеку, в workflow-heavy enterprise analyst copilot. [T1][T2]

## Telegram bots/services in RU
Telegram в РФ важен как интерфейс для быстрого доступа к знаниям и внутренним ассистентам, но не как полноценная замена Hebbia-интерфейсу. [T2]

**Найденные RU-сервисы:**
- **Just AI JAICP**: поддерживает Telegram среди 30+ каналов, продаёт ботов и RAG-подключение к документам. Тарифы публичные, есть cloud и on-prem. [T2]
- **Botmother**: конструктор Telegram-ботов для бизнеса, pricing вынесен в публичный оффер. Это подтверждает, что Telegram в РФ остаётся рабочим distribution-каналом для B2B automation. [T2]
- **BotHelp**: автоворонки и чат-боты для мессенджеров, включая Telegram, с 14-дневным trial и платными тарифами. [T2]

**Что это значит для кейса:** Telegram-слой в РФ есть, но enterprise value создаётся не самим ботом, а качеством retrieval, permissions, auditability и работой с внутренними документами. То есть Telegram может быть вторичным каналом доступа, но не ядром продукта. [T2]

## WTP, willingness to pay
### Прямые признаки готовности платить
1. **Публичные тарифы локальных поставщиков**: TEAMLY, JAICP, BotHelp и Yandex Search API уже монетизируют adjacent use cases в рублях. [T1][T2]
2. **Enterprise/on-prem offers по запросу** у TEAMLY и JAICP показывают, что рынок готов платить за закрытый контур и кастомную интеграцию, а не только за seat-based SaaS. [T2]
3. **HH hiring signal** означает, что компании готовы платить не только за софт, но и за людей, которые внедряют AI-поиск, knowledge systems и automation. Когда компании нанимают на эту функцию, они обычно уже закладывают software/integration budget. [T1][Internal]

### WTP assessment
- **SMB:** низкая готовность платить, потому что боль нерегулярная, а внедрение кажется сложным. [T2]
- **Mid-market:** умеренная готовность платить, если есть быстрый ROI в support, compliance, procurement, внутренних знаниях. [T2]
- **Enterprise:** высокая готовность платить за on-prem, права доступа, аудит, интеграции и сокращение времени аналитиков/юристов/операторов. [T2]

**Вывод:** WTP в РФ **есть**, но он концентрирован в enterprise и upper mid-market. [T2]

## Market sizing
### Method and assumptions
- **Top-down база:** рынок GenAI в РФ = **58 млрд ₽** в 2024 году. Для knowledge/search/copilot use cases берём **15% addressable share**, так как это только часть GenAI-стека, связанная с корпоративными знаниями, документами и internal assistants. Получаем TAM РФ около **8.7 млрд ₽**. [T2]
- **Segment fit:** берём **60%** от TAM РФ как сегмент средних и крупных компаний, где реально нужны контроль доступов, citations и работа с массивами документов. Получаем top-down SAM РФ около **5.2 млрд ₽**. [T1][T2]
- **Bottom-up база buyers:** используем оценку порядка **63.6 тыс.** средних и крупных организаций из статистики Росстата по финансовым результатам прибыльных и убыточных организаций. Из них только **8%** считаем реально релевантными для document-heavy AI knowledge copilot, то есть **5,088 buyers**. [T1]
- **ARR avg:** средний контракт **1.2 млн ₽/год**. Это консервативно: эквивалент примерно 100 пользователей по 1,000 ₽/мес или 1 enterprise pilot + support/integration на нижней границе рынка. Он ниже типичного enterprise on-prem чека и потому годится как baseline. [T1][T2]
- **Realistic capture:** Y1 = **2%** от SAM, Y3 = **7%** от SAM. [Inference]

### Sizing calculations
**Top-down**
- TAM (РФ) = 58.0 млрд ₽ × 15% = **8.7 млрд ₽** [T2]
- SAM (РФ) = 8.7 млрд ₽ × 60% = **5.2 млрд ₽** [T1][T2]
- SOM Y1 = 5.2 млрд ₽ × 2% = **104 млн ₽** [Inference]
- SOM Y3 = 5.2 млрд ₽ × 7% = **365 млн ₽** [Inference]

**Bottom-up**
- Total buyers = 63,600 организаций × 8% релевантных = **5,088 buyers** [T1][Inference]
- SAM bottom-up = 5,088 × 1.2 млн ₽/год = **6.11 млрд ₽** [Inference]
- SOM bottom-up Y1 = 6.11 млрд ₽ × 2% = **122 млн ₽** [Inference]
- SOM bottom-up Y3 = 6.11 млрд ₽ × 7% = **428 млн ₽** [Inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | — | — | Нет надёжного Tier-1 global dataset под рукой без paywalled report; для инвестрешения опираемся на РФ TAM. | — |
| TAM (РФ) | 8.7 млрд ₽ [T2] | 6.11 млрд ₽ [T1+Inference] | diff=1.42x, в допустимом диапазоне; bottom-up консервативнее | **6.11 млрд ₽** |
| SAM (РФ) | 5.2 млрд ₽ [T1+T2] | 6.11 млрд ₽ [T1+Inference] | diff=1.17x, расхождение небольшое | **5.2 млрд ₽** |
| SOM Y1 | 104 млн ₽ | 122 млн ₽ | diff=1.17x | **104 млн ₽** |
| SOM Y3 | 365 млн ₽ | 428 млн ₽ | diff=1.17x | **365 млн ₽** |

### Sanity checks
- Расхождение top-down и bottom-up меньше 3x, пересчёт не требуется. [Inference]
- SOM Y1 = 104 млн ₽, это около 8.7 млн ₽ MRR и меньше 10% SAM, значит оценка реалистична. [Inference]
- При среднем чеке 1.2 млн ₽/год для достижения SOM Y1 нужно около 87 активных клиентов. Это слишком много для enterprise-heavy motion, поэтому для реального GTM нужен более высокий ACV, порядка 3-6 млн ₽/год, и фокус на 20-35 крупных аккаунтах. Это не ломает Profit Gate, но меняет go-to-market в сторону enterprise sales. [Inference]

## Profit Gate
**Требование:** компания должна иметь путь к **EBITDA >= 500k ₽/мес**.

### Scenario A, low-ticket mid-market SaaS
- 8 клиентов × 150k ₽ MRR = 1.2 млн ₽ выручки/мес
- EBITDA margin 35% после sales/support/inference = **420k ₽/мес**
- **Вердикт:** FAIL

### Scenario B, balanced enterprise SaaS
- 8 клиентов × 180k ₽ MRR = 1.44 млн ₽ выручки/мес
- EBITDA margin 40% = **576k ₽/мес**
- **Вердикт:** PASS

### Scenario C, on-prem / private contour enterprise
- 2 клиента × 500k ₽ MRR эквивалента = 1.0 млн ₽ выручки/мес
- EBITDA margin 55% за счёт высокого gross margin и меньшего числа аккаунтов = **550k ₽/мес**
- **Вердикт:** PASS

### Scenario D, hybrid pilot + integration
- 4 клиента × 250k ₽ MRR = 1.0 млн ₽/мес
- EBITDA margin 45% = **450k ₽/мес**
- плюс 1 интеграционный проект в квартал на 900k ₽ даёт ещё 300k ₽ среднемесячно
- EBITDA эквивалент становится **~585k ₽/мес**
- **Вердикт:** PASS

**Итог по Profit Gate:** достижим. Даже при умеренном спросе бизнес проходит порог EBITDA, если продаёт enterprise/on-prem или hybrid deployment, а не только low-ticket seats. [Inference][T2]

## Risks
1. **Не брендовый, а category-driven спрос.** В РФ почти никто не ищет именно Hebbia. Это повышает CAC и требует прямых продаж. [Internal]
2. **Нужен закрытый контур.** Для банков, промышленности и телекомов cloud-only предложение резко сужает рынок. [T2]
3. **Telegram не является moat.** Бот можно сделать быстро, но ценность лежит в retrieval quality, permissions, audit trail и вертикальных workflow. [T2]
4. **Рынок adjacent, а не perfect-fit.** Часть конкурентов закрывает только бот-слой или knowledge base, а не весь analyst workflow. Это и шанс, и риск: нужно доказать более высокий ROI. [T2]

## Verdict
- **Demand verdict:** PROCEED
- **Demand level:** MEDIUM
- **WTP:** CONFIRMED
- **Profit Gate:** PASS
- **Инвест-логика:** прямой пользовательский шум низкий, но для фонда это не fatal flaw. Для enterprise AI в РФ важнее не search volume, а наличие бюджетов, платных локальных аналогов, hiring signal и возможность продавать high-ACV private deployments. Hebbia-подобный продукт имеет окно в верхнем сегменте рынка, если зайдёт как secure enterprise knowledge copilot, а не как generic chatbot.

Sources: T1=3, T2=6, T3=0. Primary evidence basis: T2.

## Source notes
- [T1] Росстат, финансовые результаты организаций: https://rosstat.gov.ru/
- [T1] Yandex Cloud / Search API pricing snippet: https://yandex.cloud/ru/docs/search-api/pricing
- [T1] hh-related signal via internal demand probe using hh data: http://172.18.0.1:9001/multi-demand
- [T2] CNews on Yandex B2B Tech / GenAI market 58 млрд ₽: https://www.cnews.ru/news/top/2025-11-17_rynok_generativnogo_iskusstvennogo
- [T2] TEAMLY pricing/search snippets and AI enterprise page: https://teamly.ru/ , https://teamly.ru/ai-enterprise/
- [T2] Just AI JAICP platform and tariffs: https://just-ai.com/platforma-jaicp
- [T2] BotHelp pricing snippet / main page: https://bothelp.io/
- [T2] Botmother main site: https://botmother.com/ru
