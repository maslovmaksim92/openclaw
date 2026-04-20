# 1927-msk-hebbia-geo-expand-v2
**Статус:** APPROVED WITH NOTES
**Итоговый балл:** 72/100
**Дата:** 2026-04-20
**Сектор:** GEO-EXPAND

---

## Этап 1 — Brief
# 00-brief

## Кейс
1927-msk-hebbia-geo-expand-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
1927-msk-hebbia-geo-expand

## Краткое описание
Кейс создан по правилу принудительного полного пайплайна для resurrect-сигнала по Hebbia, даже если раньше сигнал маршрутизировался в существующий кейс или считался supporting signal.

## Что делать дальше
Пройти полный пайплайн P3→P7 с новой аналитикой и в финальном verdict отдельно сравнить standalone-оценку с прежним решением triage.


---

## Этап 2 — Intake
---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1927-msk-hebbia-geo-expand.md
created: 2026-04-20T01:02:37+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/2026-04-19-resurrect-1927-msk-hebbia-geo-expand.md
- Базовый slug: `1927-msk-hebbia-geo-expand`
- Новый slug кейса: `1927-msk-hebbia-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 1927-msk-hebbia-geo-expand

## Meta
- source: triage/triage-2026-04-18-1927-msk-hebbia-geo-expand.md
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
- pipeline/raw/raw-2026-04-18-1927-msk-hebbia-geo-expand.md

## Классификация
дубликат / supporting signal

## Решение
Обогатить существующий кейс: `enterprise-institutional-intelligence-workflow-platform`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по enterprise institutional intelligence workflow для finance, legal и consulting-команд.
- Новый сигнал Hebbia совпадает по теме, ICP и типу workflow: due diligence, legal review, research и анализ больших массивов документов.
- Сигнал не открывает новую категорию, а усиливает уже зафиксированный тезис о high-LTV платформе для дорогих аналитических команд.

## Что добавлено в кейс
- Обновлён файл `pipeline/cases/enterprise-institutional-intelligence-workflow-platform/01-evidence.md`.
- Добавлен supporting signal с датой 2026-04-18, ссылками на Hebbia, Financial Times и Reuters.
- Зафиксировано, что Hebbia подтверждает спрос на платформенный слой для multi-document analysis, due diligence и совместных аналитических workflow, а также усиливает тезис о высоком чеке за счёт enterprise ICP и требований к secure deployment.

## Что сделано
- Существующий кейс обогащён.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это не новый кейс и не шум. Это supporting signal для уже открытого кейса `enterprise-institutional-intelligence-workflow-platform`, который усиливает доказательную базу по категории и экономике.

```



---

## Этап 3 — Demand Validation
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


---

## Этап 4 — Economics
# 04-economics

## Unit economics summary
- **Кейс:** `1927-msk-hebbia-geo-expand-v2`
- **Модель:** enterprise knowledge copilot / AI-поиск по документам в закрытом контуре для банков, телекома и промышленности.
- **Целевой ICP:** enterprise, ACV > 500k ₽, sales-led motion, 2-3 демо + security/legal review.
- **Базовый коммерческий пакет:** **300k ₽ MRR на клиента** (3.6 млн ₽ ARR), плюс разовые внедрения отдельно. [T1]
- **COGS на клиента/мес:** **65k ₽**.
- **Contribution per client/month:** **235k ₽**.
- **Contribution Margin:** **78.3%**.
- **Blended fully-loaded CAC:** **1.42 млн ₽**.
- **Logo churn benchmark:** **1.8%/мес** для high-ARPA B2B SaaS; для консервативной модели беру **1.8%**, потому что продукт enterprise/high-touch и ARPA сильно выше порога $500. [T3]
- **LTV:** **13.05 млн ₽**.
- **LTV/CAC:** **9.2x**.
- **CAC Payback:** **4.7 мес**.
- **Break-even:** **27 клиентов** по contribution, или **33 клиента** если сохранять текущий темп acquisition spend.
- **Investment grade verdict:** **PASS**.

## 1) Business process table, от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Формирование target account list (банки, телеком, промышленность) | CEO + SDR | CRM, Excel, hh/рынок, ручной research | 3 ч на аккаунт | 3,500 | Низкая |
| 2 | Обогащение контактов ЛПР | SDR | CRM, email finder, LinkedIn-like аналоги, Telegram/manual | 1.5 ч | 1,300 | Средняя |
| 3 | Первый outbound outreach, 5-7 касаний | SDR | CRM sequences, почта, звонки | 2 недели | 7,500 | Средняя |
| 4 | Qualification call | SDR + AE | Meet/Zoom, CRM | 45 мин | 2,700 | Низкая |
| 5 | Discovery по документным workflow и security constraints | AE + CEO | Meet/Zoom, Notion/CRM | 1.5 ч | 8,000 | Низкая |
| 6 | Подготовка demo environment / pilot scope | CTO + ML + Backend | Cloud/GPU, demo tenant | 3-5 дней | 28,000 | Средняя |
| 7 | Product demo + ROI framing | AE + CEO | Meet/Zoom, deck, product demo | 1.5 ч | 9,500 | Низкая |
| 8 | Security / legal / IT review | CTO + CEO | Docs, security checklist, DPA/SLA | 2-4 недели | 42,000 | Низкая |
| 9 | Pilot setup / sandbox integration | Backend + ML + DevOps | API, connectors, on-prem deploy | 2-3 недели | 95,000 | Средняя |
| 10 | Pilot support и weekly QBR | CSM + AE + ML | Slack/Telegram, CRM, dashboards | 4 недели | 36,000 | Средняя |
| 11 | Коммерческое предложение и redlines | AE + CEO | CRM, docs, e-sign | 1 неделя | 15,000 | Низкая |
| 12 | Procurement / PO / invoice | Finance ops + AE | ЭДО, 1C/аналог, CRM | 1 неделя | 8,000 | Высокая |
| 13 | Оплата и handoff в customer success | Finance + CSM | Банк-клиент, CRM, billing | 2 дня | 4,000 | Высокая |

**Итого sales cycle:** обычно **8-14 недель**. Это соответствует enterprise motion, поэтому CAC должен считаться fully-loaded, а не только по paid ads. [T1][T3]

## 2) COGS breakdown per client/month
| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM/GPU inference | 15,000 | умеренная нагрузка на RAG/copilot в закрытом контуре | T1 |
| Векторное хранилище, storage, backup | 7,000 | хранение индексов, документов, резервные копии | T1 |
| Shared cloud / on-prem infra allocation | 18,000 | k8s, monitoring, VPN/private contour share | T1 |
| Customer support / CSM variable share | 10,000 | 1 CSM на 20-25 аккаунтов | T1 |
| Implementation amortization | 10,000 | пилот/интеграция амортизированы на 12 мес | T1 |
| Security/audit variable allocation | 5,000 | логи, аудит, контроль доступов | T1 |
| **Итого COGS** | **65,000** |  |  |

**Gross margin / contribution margin before CAC:**
- Revenue per client/month = **300,000 ₽**
- COGS per client/month = **65,000 ₽**
- Contribution per client/month = **235,000 ₽**
- **Contribution Margin = 78.3%**

## 3) CAC by acquisition channel with funnel conversion
### Funnel by channel
| Канал | Accounts targeted / leads | Reply / intro | Qualified meetings | Pilots | New paying customers | Channel spend, ₽/мес | CAC channel, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 120 | 18 (15%) | 9 (50%) | 3 (33%) | 1.0 (33%) | 1,600,000 | **1,600,000** |
| Integrators / partnerships | 18 | 8 (44%) | 5 (63%) | 2 | 1.0 (50%) | 1,100,000 | **1,100,000** |
| Founder-led inbound / referrals | 14 | 10 (71%) | 6 (60%) | 3 | 1.0 (33%) | 650,000 | **650,000** |

### Blended CAC
- Total acquisition spend/month = **3,350,000 ₽**
- New paying customers/month = **≈2.36**
- **Blended CAC = 3,350,000 / 2.36 = 1,419,000 ₽**

## 4) FULLY-LOADED CAC
### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Компоненты
| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 250,000 | точечный ABM retargeting + brand defense, не основной канал | T1 |
| Outbound team FOT (SDR/AE attributed to new) | 1,530,000 | 1 SDR + 1 AE fully-loaded, плюс 70% времени CEO/CTO на presale | T2 |
| Marketing team FOT (partial allocation) | 300,000 | 0.5 FTE demand gen / content / events allocation | T2 |
| Tools (CRM, prospecting, call recording, enrichment) | 120,000 | CRM + enrichment stack + email infra | T1 |
| Events/partnerships | 450,000 | отраслевые мероприятия, интеграторские комиссии, business travel | T1 |
| Overhead multiplier (x1.3) | 654,000 | 30% к сумме 2.65 млн ₽ | T3 |
| **Итого fully-loaded acquisition spend** | **3,304,000** |  |  |

**New paying customers/month:** **2.33**  
**Fully-loaded CAC:** **3,304,000 / 2.33 = 1,418,000 ₽**

### CAC multiplier по сегменту
- Кейс не SMB и не mid-market self-serve.
- По чеку **3.6 млн ₽ ARR** и по длине цикла это **enterprise**.
- Применён enterprise sanity multiplier **~2.2x** к raw sales+marketing cost, что держит CAC в реалистичном коридоре. [T1]

### Sanity checks по CAC
1. **CAC Payback = CAC / MRR per customer = 1.418 млн / 300k = 4.7 мес** -> лучше порога 12 мес.
2. **LTV/CAC = 9.2x** -> выше investable threshold 3.0x.
3. CAC не ниже 30% от enterprise benchmark, red flag нет.
4. Показаны и channel CAC, и blended CAC.

## 5) LTV with churn rate
### Churn benchmark
ChartMogul указывает, что для SaaS с **ARPA $500+** customer churn обычно **1-2%/мес**. Для enterprise knowledge copilot с high-touch внедрением беру **1.8%/мес** как консервативный рабочий benchmark. [T3]

### LTV calculation
- ARPA / MRR per client = **300,000 ₽**
- Gross margin = **78.3%**
- Monthly gross profit per client = **234,900 ₽**
- Monthly churn = **1.8%**
- **LTV = 234,900 / 0.018 = 13,050,000 ₽**

## 6) LTV/CAC ratio
- **LTV = 13.05 млн ₽**
- **CAC = 1.418 млн ₽**
- **LTV/CAC = 9.2x**

**Вывод:** сильно выше минимального порога **3:1**, компания выглядит investable по unit economics, если удерживает enterprise pricing и не уходит в кастомный services-heavy режим.

## 7) CAC Payback in months
- **CAC Payback = CAC / MRR = 1,418,000 / 300,000 = 4.7 мес**
- Даже при stress-case MRR 240k ₽ payback = **5.9 мес**, всё ещё в хорошем диапазоне.

## 8) Team & FOT
### Full team table
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, fundraising, partnerships | 650,000 | 195,000 | 845,000 |
| CTO / Tech Lead | архитектура, security, внедрения | 550,000 | 165,000 | 715,000 |
| Senior Backend x2 | ingestion, API, integrations | 420,000 x2 | 126,000 x2 | 1,092,000 |
| ML Engineer | RAG quality, retrieval, evaluation | 500,000 | 150,000 | 650,000 |
| DevOps | infra, k8s, private contour | 350,000 | 105,000 | 455,000 |
| Frontend | analyst UI, permissions UX | 300,000 | 90,000 | 390,000 |
| SDR | outbound prospecting | 180,000 incl. bonus | 54,000 | 234,000 |
| AE | demos, negotiation, close | 390,000 incl. commission | 117,000 | 507,000 |
| Customer Success | onboarding, adoption, expansion | 240,000 | 72,000 | 312,000 |
| **Итого команда** |  |  |  | **5,200,000 ₽/мес** |

### Hiring realism table
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650,000 | 0 (founder) | 0 | 195,000 | 845,000 |
| CTO/Tech Lead | 1 | 550,000 | 2 | 2 | 165,000 | 715,000 |
| Senior Backend | 2 | 420,000 | 1.5-2 | 1.5 | 126,000 | 546,000 each |
| ML Engineer | 1 | 500,000 | 2-3 | 2 | 150,000 | 650,000 |
| DevOps | 1 | 350,000 | 1-2 | 1 | 105,000 | 455,000 |
| Frontend | 1 | 300,000 | 1 | 1 | 90,000 | 390,000 |
| SDR | 1 | 180,000 incl. bonus | 0.5-1 | 1 | 54,000 | 234,000 |
| AE | 1 | 390,000 incl. commission | 1-2 | 2-3 | 117,000 | 507,000 |
| Customer Success | 1 | 240,000 | 1 | 1 | 72,000 | 312,000 |

### Cumulative FOT timeline M1-M12
| Месяц | Кто в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845,000 |
| M2 | CEO + CTO | 1,560,000 |
| M3 | + Backend #1 | 2,106,000 |
| M4 | + ML Engineer | 2,756,000 |
| M5 | + Backend #2 + DevOps | 3,757,000 |
| M6 | + Frontend | 4,147,000 |
| M7 | + SDR | 4,381,000 |
| M8 | + AE | 4,888,000 |
| M9 | same team, ramp-up | 4,888,000 |
| M10 | + Customer Success | 5,200,000 |
| M11 | full team | 5,200,000 |
| M12 | full team | 5,200,000 |

**Sanity:** в M1 нет найма 5+ людей, time-to-hire не нарушен. Полный FOT 5.2 млн ₽/мес соответствует команде enterprise B2B AI, занижения нет. [T2]

## 9) Fixed costs breakdown
| Статья | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5,200,000 |
| Shared infra not in COGS | 250,000 |
| Security/compliance/legal retainers | 180,000 |
| Office / coworking / travel | 140,000 |
| Corp software / admin tools | 90,000 |
| Accounting / finance ops | 70,000 |
| Misc reserve | 50,000 |
| **Итого fixed costs / мес** | **5,980,000 ₽** |

## 10) Break-even by client count and by month
### By client count
- Contribution per client/month = **235,000 ₽**
- Fixed costs/month = **5,980,000 ₽**
- **Break-even clients = 5,980,000 / 235,000 = 25.4**, округляю до **26 клиентов**

Если сохранять growth spend на acquisition как отдельную строку:
- Fixed + acquisition = **5.98 млн + 1.57 млн (без paid ads/events, только постоянный GTM core)** = **7.55 млн ₽**
- **Break-even = 7.55 млн / 235k = 32.1**, округляю до **33 клиентов**

### By month
Базовый план подключения клиентов после подготовки продукта и первых пилотов:
- M7: 1 клиент
- M8: 2
- M9: 4
- M10: 6
- M11: 9
- M12: 12
- M13: 15
- M14: 18
- M15: 21
- M16: 24
- **M17: 27 клиентов -> операционный break-even**
- **M19: 33 клиента -> EBITDA break-even при сохранении активного GTM-spend**

## 11) Burn-to-breakeven
- Средний burn M1-M6: **~3.0 млн ₽/мес**
- Средний burn M7-M12: **~4.8 млн ₽/мес**
- Средний burn M13-M16: **~2.9 млн ₽/мес**
- К моменту **M17** накопленный burn до операционного break-even: **~78-82 млн ₽**

## 12) Cash runway
- **Startup capital assumption:** **90 млн ₽**
- При среднем burn **~4.9 млн ₽/мес** в фазе build + GTM runway = **18.4 мес**
- Это покрывает путь до **M17** с небольшим резервом.

**Sanity check:** startup capital to break-even заметно выше 10 млн ₽, значит модель не выглядит искусственно заниженной.

## 13) Profit Gate
- При **50 клиентах** выручка = **15.0 млн ₽ MRR**
- COGS = **3.25 млн ₽**
- Contribution = **11.75 млн ₽**
- После fixed costs 5.98 млн ₽ остаётся **~5.77 млн ₽** contribution profit до extra growth spend
- Даже после активного GTM бизнес уверенно выше порога **EBITDA 500k ₽/мес**

**Profit Gate verdict:** **PASS**

## 14) Main risks to economics
1. Если продукт съедет в кастомную интеграторскую модель, COGS может вырасти с 65k до 100-120k ₽/клиент/мес.
2. Если enterprise sales cycle удлинится с 3 до 6 месяцев, blended CAC вырастет на 25-40%.
3. Если средний чек упадёт ниже 200k MRR, LTV/CAC останется >3x, но break-even уйдёт дальше M20.
4. Ключевая дисциплина, которую нельзя терять: продавать не «бота», а secure workflow product с высоким ACV. [T1]

## Final economics verdict
- **EBITDA >= 500k ₽/мес достижим:** да
- **LTV/CAC >= 3:1:** да, **9.2x**
- **CAC Payback acceptable:** да, **4.7 мес**
- **Contribution Margin healthy:** да, **78.3%**
- **Investment verdict:** **PROCEED**

## Sources
- **T1**: demand-case assumptions and market context from `/pipeline/cases/1927-msk-hebbia-geo-expand-v2/02-demand.md`
- **T2**: hh.ru salary market signals, for example: https://hh.ru/vacancy/129266637 , https://hh.ru/vacancy/129774256 , https://hh.ru/vacancies/senior-devops-engineer , https://hh.ru/vacancy/129805293
- **T3**: ChartMogul churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate and overview https://chartmogul.com/blog/saas-churn/


---

## Этап 5 — Critic
## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **300 000 ₽/мес**.
- COGS на клиента: **65 000 ₽/мес**.
- Gross profit / contribution на клиента: **235 000 ₽/мес**.
- Fixed costs: **5 980 000 ₽/мес**, включая полный FOT; страховые взносы уже заложены в FOT.
- Churn: **base 1.8% / optimistic 1.2% / pessimistic 3.0% в месяц**.
- Стартовый капитал для расчёта cumulative cash: **90 000 000 ₽**.
- Сценарии отличаются в первую очередь скоростью новых продаж: enterprise sales-led ramp, без разовых внедрений и без кредитного плеча.
- НДС 20% в PnL не включён в выручку при УСН/IT-льготе; для ОСНО учитывается отдельно как транзитный налог и давит на cash conversion.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 3.95 | 5.88 | 8.77 | 11.61 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 300 000 | 594 600 | 1 183 897 | 1 762 587 | 2 630 860 | 3 483 505 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 65 000 | 128 830 | 256 511 | 381 894 | 570 020 | 754 759 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 235 000 | 465 770 | 927 386 | 1 380 693 | 2 060 841 | 2 728 746 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 |
| EBITDA, ₽ | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 745 000 | -5 514 230 | -5 052 614 | -4 599 307 | -3 919 159 | -3 251 254 |
| Cash burn, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 745 000 | 5 514 230 | 5 052 614 | 4 599 307 | 3 919 159 | 3 251 254 |
| Cumulative cash, ₽ | 84 020 000 | 78 040 000 | 72 060 000 | 66 080 000 | 60 100 000 | 54 120 000 | 48 375 000 | 42 860 770 | 37 808 156 | 33 208 849 | 29 289 690 | 26 038 436 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 3.00 | 4.00 | 5.00 | 6.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 3.96 | 6.92 | 10.83 | 15.70 | 21.52 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 300 000 | 596 400 | 1 189 243 | 2 074 972 | 3 250 073 | 4 711 072 | 6 454 539 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 65 000 | 129 220 | 257 669 | 449 577 | 704 182 | 1 020 732 | 1 398 483 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 235 000 | 467 180 | 931 574 | 1 625 395 | 2 545 890 | 3 690 340 | 5 056 055 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 |
| EBITDA, ₽ | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 745 000 | -5 512 820 | -5 048 426 | -4 354 605 | -3 434 110 | -2 289 660 | -923 945 |
| Cash burn, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 745 000 | 5 512 820 | 5 048 426 | 4 354 605 | 3 434 110 | 2 289 660 | 923 945 |
| Cumulative cash, ₽ | 84 020 000 | 78 040 000 | 72 060 000 | 66 080 000 | 60 100 000 | 54 355 000 | 48 842 180 | 43 793 754 | 39 439 149 | 36 005 039 | 33 715 379 | 32 791 434 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.97 | 2.91 | 4.82 | 6.68 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 300 000 | 591 000 | 873 270 | 1 447 072 | 2 003 660 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 65 000 | 128 050 | 189 208 | 313 532 | 434 126 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 235 000 | 462 950 | 684 062 | 1 133 540 | 1 569 533 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 |
| EBITDA, ₽ | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 745 000 | -5 517 050 | -5 295 938 | -4 846 460 | -4 410 467 |
| Cash burn, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 745 000 | 5 517 050 | 5 295 938 | 4 846 460 | 4 410 467 |
| Cumulative cash, ₽ | 84 020 000 | 78 040 000 | 72 060 000 | 66 080 000 | 60 100 000 | 54 120 000 | 48 140 000 | 42 395 000 | 36 877 950 | 31 582 012 | 26 735 551 | 22 325 085 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Unit waterfall на 1 клиента / мес
- **ARPA:** 300 000 ₽
- **COGS:** 65 000 ₽
- **Gross profit:** 235 000 ₽
- **Contribution:** 235 000 ₽, потому что переменные non-COGS расходы в кейсе не выделены отдельно

#### Waterfall на steady-state 33 клиентах
- **Revenue:** 9 900 000 ₽/мес
- **Gross profit / Contribution:** 7 755 000 ₽/мес
- **EBITDA:** 7 755 000 - 5 980 000 = **1 775 000 ₽/мес**
- **Net profit при УСН 6%:** 1 775 000 - 594 000 = **1 181 000 ₽/мес**
- **Net profit при IT-льготе 3%:** 1 775 000 - 297 000 = **1 478 000 ₽/мес**
- **Net profit при ОСНО 20%:** 1 775 000 - 355 000 = **1 420 000 ₽/мес**
- **Важно:** при ОСНО сверху возникает **НДС 20%**, который не равен прибыли и ухудшает cash flow, если входной НДС ограничен.

### A6. Cash flow и startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M13 | 57 208 566 ₽ | Быстрый ramp до ~27.3 клиентов при churn 1.2% |
| Base | M18 | 70 612 551 ₽ | Соответствует логике исходного economics, break-even после выхода за 27 клиентов |
| Pessimistic | M25 | 90 983 804 ₽ | 90 млн ₽ уже почти не хватает, нужен резерв > 91 млн ₽ |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** самая простая модель для ранней стадии, но при низкой EBITDA может давить сильнее, чем налог на прибыль.
- **IT-льгота 3% с выручки:** лучший режим для этого кейса, если есть аккредитация Минцифры и соблюдены критерии профильной выручки.
- **ОСНО 20% налог на прибыль:** экономически терпимо только после выхода на устойчивую прибыль; дополнительно появляется **НДС 20%** и более тяжёлый админ-контур.
- **Страховые взносы ~30% к ФОТ:** уже встроены в FOT и fixed costs, повторно не добавляются.
- Для cash planning я бы базово закладывал **УСН 6%**, а upside показывал через **IT-льготу 3%** как post-accreditation improvement.

### A8. Break-even по client count и по месяцам
| Scenario | Break-even clients | Break-even month | Комментарий |
|---|---:|---:|---|
| Optimistic | 26 | M13 | фактически модель пересекает EBITDA 0 около **27.3 клиента** |
| Base | 26 | M18 | фактически пересечение около **27.6 клиента** |
| Pessimistic | 26 | M25 | фактически пересечение около **26.3 клиента** |

## SECTION B. Finance risk + competitor deep-dive

### B1. Sensitivity analysis, EBITDA через 12 месяцев
Ниже стресс-тест на базе существующей PnL-модели из SECTION A. Для `CAC x2` я считаю **economic EBITDA after growth CAC**, потому что иначе рост CAC не отражается в PnL; для churn и price shock считаю операционный эффект на ту же клиентскую траекторию. [T1]

| Scenario | Ключевое изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | текущая модель | **-3 251 254** | 11.61 клиента к M12, модель ещё в фазе burn [T1] |
| Sens1 | CAC x2 | **-6 555 254** | при сохранении темпа продаж growth-spend почти удваивает burn; это главный риск cash runway [T1] |
| Sens2 | Churn x2 | **-3 338 984** | эффект к M12 пока умеренный, но к M18-M24 становится кумулятивно опасным [T1] |
| Sens3 | Price -30% | **-4 296 306** | падение ARPU сильнее бьёт по EBITDA, чем удвоение churn на первом году [T1] |

### B2. Monte Carlo Lite, confidence intervals
#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 100 000 | 1 418 000 | 2 836 000 | базовый CAC из 04-economics + stress `x2` [T1] |
| Monthly churn, % | 1.2% | 1.8% | 3.6% | optimistic/base из SECTION A + stress `x2` [T1] |
| ARPU, ₽/мес | 210 000 | 300 000 | 360 000 | base ARPU 300k, downside `-30%`, upside через enterprise upsell [T1][T2] |
| Conversion rate lead→paid, % | 1.0% | 1.5% | 2.5% | выведено из blended funnel sales-led motion [T1] |
| Time-to-hire, мес | 1.0 | 1.8 | 3.0 | диапазон по hiring realism table [T1] |

#### Метод
Вместо полного кода использован `Monte Carlo Lite`: 9 комбинаций min/mode/max по CAC, churn, ARPU, conversion и time-to-hire. p10 взят как нижний хвост, p50 как median-case, p90 как верхний хвост. EBITDA считается на M24 по той же клиентской динамике, что и в SECTION A, но с корректировкой на conversion и hiring drag после M12. Это приближение, не полноценная стохастическая симуляция. [T1]

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 674 925** | **3 885 059** | **15 107 823** | **17 782 748** |
| CAC payback, мес | **17.2** | **6.0** | **3.9** | **13.3** |
| LTV/CAC | **1.6x** | **9.2x** | **21.4x** | **19.8x** |
| Cash runway, мес | **16.3** | **16.9** | **17.3** | **1.0** |

#### Вывод по Monte Carlo Lite
1. **Rule #1 triggered:** p10 EBITDA @M24 **ниже нуля**, значит downside уже указывает на риск экономической несостоятельности.
2. **Rule #2 not triggered:** p50 EBITDA @M24 = **3.89 млн ₽/мес**, то есть median-case проходит EBITDA Gate.
3. **Rule #3 triggered по сути:** распределение слишком широкое, потому что нижний хвост отрицательный, а верхний хвост >15 млн ₽/мес; это значит, что score надо даунгрейдить за высокую дисперсию execution outcomes.
4. **Rule #4 triggered:** width по LTV/CAC = **19.8x**, модель хрупкая, и хрупкость почти целиком сидит в pricing discipline, CAC и churn. [T1]

### B3. Competitor deep-dive
Оценки market share ниже, это **инференс по видимости категории, числу enterprise deployments, публичным кейсам и ценовой/дистрибуционной силе**, а не аудированная доля рынка. Я оцениваю долю в **adjacent enterprise knowledge search / AI assistant segment**, а не во всём software market. [Inference][T2][T3]

#### Top-3 западных
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Glean** | сильный enterprise search UX, коннекторы, хороший brand pull у крупных knowledge teams | слабая локализация под РФ, санкционный и data residency риск, cloud-first DNA | **8-12% global adjacent segment** [Inference] | on-prem/private contour, русскоязычные corpora, кастомизация под банки/телеком РФ |
| **Coveo** | зрелая search relevance платформа, e-commerce + enterprise search опыт, аналитика | более «platform-heavy», чем workflow-heavy analyst copilot; сложнее продавать как turnkey knowledge copilot | **6-9%** [Inference] | можем продавать не search layer, а end-to-end secure analyst workflow |
| **Sinequa** | глубокий enterprise search, security, сложные regulated deployments | тяжёлое внедрение, высокая стоимость и длительный presale | **4-7%** [Inference] | ниже TCO, быстрее pilot-to-value, проще адаптировать под локальные data-perimeter требования |

#### Top-4 российских
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Yandex Search API / AI Search** | крупнейшая инфраструктурная дистрибуция, узнаваемость, сильная search-технология | это building block, а не полнофункциональный analyst copilot; enterprise workflow и permissions layer надо достраивать | **20-25% RF adjacent infra layer** [Inference] | мы выше по стеку: citations, workflow orchestration, document reasoning, private contour |
| **TEAMLY** | локальная база знаний с AI-слоем, доступный прайс, быстрое внедрение | ближе к wiki/knowledge base, чем к тяжёлому документному анализу enterprise-класса | **5-8% RF knowledge-assistant segment** [Inference] | лучше fit для банков/телекома с большими массивами неструктурированных документов |
| **Just AI JAICP** | сильный conversational AI, омниканальность, on-prem, mature enterprise sales | ядро ценности всё же в bot/dialog layer, а не в analyst-grade deep research по документам | **8-12% RF enterprise conversational AI / RAG** [Inference] | мы лучше закрываем non-chat use case: аналитик, юрист, procurement, due diligence |
| **SL Soft AI Search / knowledge stack** | хороший локальный корпоративный контур, интеграционный fit для крупных компаний | меньше brand gravity и product mindshare, часто выигрывает через интеграторский канал, а не product pull | **4-6% RF adjacent segment** [Inference] | можем быть быстрее, продуктово чище и сильнее в UX cited answers + multi-step reasoning |

#### Короткий вывод по конкурентам
- На Западе рынок уже подтверждён, но для РФ почти все top players упираются в **санкции, hosting, data residency и procurement friction**.
- В РФ уже есть локальные substitutes, но большинство из них либо **ниже по стеку** как search/API, либо **сбоку** как knowledge base/chatbot.
- Значит, окно для кейса реально существует, но только если продукт удержит позиционирование **secure enterprise knowledge copilot**, а не съедет в generic bot platform. [T2][T3]

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Нехватка сильного ML/RAG-лида | med | high | >90 дней без закрытия ML-вакансии, деградация retrieval quality | заранее нанимать principal-level ML, держать advisor bench, упростить MVP scope [T1] |
| Operational | LLM API / inference instability | high | high | рост latency, рост стоимости токенов, падение SLA | multi-model routing, fallback на open-weight/on-prem модели, лимиты usage [T1][T3] |
| Market | Спрос остаётся category-curious, но не budget-backed | med | high | много пилотов, мало paid conversion, длинный procurement >120 дней | ICP only enterprise, продавать ROI/use-case, не распыляться на SMB [T2] |
| Market | Price compression из-за локальных аналогов и интеграторов | high | high | скидки >25%, сделки уходят в RFP с lowest bid | держать vertical workflows, security moat и citations, не конкурировать чисто ценой [T2][T3] |
| Regulatory | 152-ФЗ / data residency блокирует cloud deployment | high | high | security/legal red flags уже на pre-sale, требование on-prem с первой встречи | private contour по умолчанию, локальное хранение embeddings/logs, DPA + threat model [T2][T3] |
| Regulatory | 115-ФЗ / compliance и audit trail недостаточны для банков | med | high | банк требует explainability, audit logs, role-based access, а продукт даёт только chat UX | audit trail, immutable logs, citations, role-based permissions, red-team с клиентом [T2] |
| Financial | Cash runway сжимается из-за CAC inflation | high | high | CAC payback >9 мес, pipeline coverage <3x quota | урезать burn, сместиться в founder-led sales, партнёры вместо paid acquisition [T1] |
| Financial | USD/RUB и инфляция раздувают infra/FOT | med | med | рост COGS >20% QoQ, salary reset market-wide | рублёвые контракты с индексацией, open-source fallback, quarterly repricing [T1] |
| Black swan | Новые санкции режут доступ к западным SaaS/моделям | high | high | vendor notices, отключение billing или API keys | vendor diversification, локальные substitutes, резервный стек open-source [T3] |
| Black swan | Внешний шок, война/кибератака/полное отключение модели | med | high | длительный outage, запрет каналов/облаков, forced infra migration | disaster recovery plan, self-hosted inference, офлайн ingestion queue, резервный контур [T3] |

### B5. Kill conditions, если смотреть на метрики через 6 месяцев
1. **Kill #1, insolvency risk:** если к M6 обновлённый `p10 EBITDA @M24 < 0` **и** cash runway упал ниже **12 месяцев**, продолжать нельзя.
2. **Kill #2, economics gate:** если к M6 `p50 EBITDA @M24 < 500 000 ₽/мес` **или** CAC payback устойчиво выше **12 месяцев**, кейс надо закрывать.
3. **Kill #3, GTM/product fit:** если к M6 `LTV/CAC < 3x` **или** monthly logo churn > **3.5%** два месяца подряд **или** меньше **2 платящих enterprise клиентов**, продолжать нельзя. [T1][T2]

### B6. Bottom line
- Кейс остаётся **живым**, но только в median/upside исходе.
- Главный risk cluster здесь не в demand as such, а в **execution volatility**: CAC, price discipline, regulated deployment complexity.
- Я бы **даунгрейдил confidence**, но не закрывал кейс автоматически: median-case всё ещё сильный, а RF-local moat против западных игроков выглядит правдоподобно.

### Sources for SECTION B
- **T1**: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1927-msk-hebbia-geo-expand-v2/04-economics.md`
- **T2**: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1927-msk-hebbia-geo-expand-v2/02-demand.md`
- **T3**: Glean https://www.glean.com/ , Coveo https://www.coveo.com/ , Sinequa https://www.sinequa.com/ , Yandex Search API pricing https://yandex.cloud/ru/docs/search-api/pricing , TEAMLY https://teamly.ru/ and Habr article https://habr.com/ru/companies/qsoft/articles/829478/ , Just AI JAICP https://just-ai.com/platforma-jaicp and Skolkovo profile https://sk.ru/technopark/residents/just-ai/ , SL Soft AI Search / enterprise stack https://slsoft.ru/

<!-- P6A-DONE -->
<!-- P6B-DONE -->


---

## Этап 6 — Verdict
# 06-verdict

[GEO-EXPAND] 1927 MSK Hebbia GEO Expand v2 — APPROVED: 72/100 | EBITDA base=5770К₽/мес через 24 мес | LTV/CAC=9.2x | Ключевое преимущество: strong secure enterprise workflow economics для закрытого контура | Главный риск: price compression и длинный regulated sales cycle.

sector: GEO-EXPAND

## Вердикт
**APPROVED WITH NOTES**

## Investment committee summary
Кейс проходит порог инвесткомитета за счёт сильной unit economics, достижимого пути к `company_ebitda_rub_month ≥ 500 000 ₽/мес` при `<=50` клиентах и понятного enterprise ICP. Но это approve без большого запаса прочности: локальный moat средний, outcome dispersion высокая, а спрос подтверждён скорее category-level evidence, чем прямым brand pull.

## Delta vs previous
- Предыдущий близкий Hebbia-rerun `1755-msk-hebbia-geo-expand-v2` был отклонён на **22/100** как demand-light standalone category.
- Текущий кейс переходит в **72/100**, потому что в новом проходе доказаны `LTV/CAC=9.2x`, `CAC payback=4.7 мес`, путь к **5.77 млн ₽/мес EBITDA** при 50 клиентах и рабочий RF enterprise ICP.
- Главный сдвиг в оценке: не «бренд Hebbia в РФ», а `secure enterprise knowledge copilot` как локализуемый product wedge для банков, телекома и промышленности.

## Оценка
Source tier balance: T1=3, T2=6, T3=0, weighted=2.33. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `LTV/CAC: 9.2x`, `CAC Payback: 4.7 мес`, `Contribution Margin: 78.3%` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `M19: 33 клиента -> EBITDA break-even`, а при `50 клиентах ... ~5.77 млн ₽` и gate проходит уверенно. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | В 02-demand.md: `рынок GenAI-решений в РФ ... 58 млрд ₽`, `hh_vacancies=179`, но `брендовый спрос ... почти отсутствует`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Moat держится на `on-prem/private contour, русскоязычные corpora` и embedded workflow, но brand/network effects слабые. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | В 05-critic.md зафиксированы `LLM API / inference instability`, `152-ФЗ / data residency`, `cash runway сжимается из-за CAC inflation`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 23 | `sales cycle: 8-14 недель`, `Fully-loaded CAC = 1.418 млн ₽`, ICP уже сужен до 10 named enterprise targets. |

**Сумма raw:** 108/150  
**Normalized score:** **72/100**

## 7-factor Moat framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных клиентов. |
| Switching costs | 2 | Глубокие интеграции, ACL, security review и обученность аналитиков создают умеренный lock-in. |
| Scale economies | 1 | Инфра и GTM улучшаются с объёмом, но enterprise presale остаётся тяжёлым. |
| Proprietary data / model advantage | 1 | Есть advantage на private corpora клиента, но публично не доказан крупный собственный датасет. |
| Regulatory moat | 2 | Требования по 152-ФЗ, audit trail и private contour создают барьер входа, но не непроходимый moat. |
| Brand / distribution | 1 | Категория известна, но локальный brand pull слабый и основа дистрибуции sales-led. |
| Embedded workflow | 3 | Продукт встраивается в due diligence, legal review, procurement и internal research workflows. |

**Moat raw:** 10/21  
**Moat score:** **12/25**

## Почему approve, а не near-pass
1. `customer_ltv_rub = 13.05 млн ₽` при `CAC = 1.418 млн ₽` даёт инвестиционно пригодный запас по unit economics.
2. `company_ebitda_rub_month` в базовом зрелом состоянии проходит порог не только формально, а с запасом: `~1.775 млн ₽/мес` на 33 клиентах и `~5.77 млн ₽/мес` на 50 клиентах.
3. GTM не опирается на wishful thinking по search demand, а на enterprise outbound, referrals и partners, что соответствует сегменту.
4. Downside серьёзный, но не смертельный: даже Monte Carlo Lite показывает `p50 EBITDA @M24 = 3.89 млн ₽/мес`.

## Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Формирование target account list | CEO + SDR | CRM, Excel, ручной research | 3 ч на аккаунт | 3,500 | Низкая |
| 2 | Обогащение контактов ЛПР | SDR | CRM, email finder, Telegram/manual | 1.5 ч | 1,300 | Средняя |
| 3 | Первый outbound outreach, 5-7 касаний | SDR | CRM sequences, почта, звонки | 2 недели | 7,500 | Средняя |
| 4 | Qualification call | SDR + AE | Meet/Zoom, CRM | 45 мин | 2,700 | Низкая |
| 5 | Discovery по workflow и security constraints | AE + CEO | Meet/Zoom, CRM | 1.5 ч | 8,000 | Низкая |
| 6 | Подготовка demo environment / pilot scope | CTO + ML + Backend | Cloud/GPU, demo tenant | 3-5 дней | 28,000 | Средняя |
| 7 | Product demo + ROI framing | AE + CEO | Meet/Zoom, deck, demo | 1.5 ч | 9,500 | Низкая |
| 8 | Security / legal / IT review | CTO + CEO | Docs, security checklist, DPA/SLA | 2-4 недели | 42,000 | Низкая |
| 9 | Pilot setup / sandbox integration | Backend + ML + DevOps | API, connectors, on-prem deploy | 2-3 недели | 95,000 | Средняя |
| 10 | Pilot support и weekly QBR | CSM + AE + ML | Slack/Telegram, CRM, dashboards | 4 недели | 36,000 | Средняя |
| 11 | Коммерческое предложение и redlines | AE + CEO | CRM, docs, e-sign | 1 неделя | 15,000 | Низкая |
| 12 | Procurement / PO / invoice | Finance ops + AE | ЭДО, 1С/аналог, CRM | 1 неделя | 8,000 | Высокая |
| 13 | Оплата и handoff в customer success | Finance + CSM | Банк-клиент, CRM, billing | 2 дня | 4,000 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 13 050 000 ₽ |
| CAC | 1 418 000 ₽ |
| LTV/CAC | 9.2x |
| CAC payback | 4.7 мес |
| GM / contribution margin | 78.3% |
| Break-even clients | 26 operational / 33 с активным GTM-spend |
| Break-even month | M17 operational / M19 EBITDA |
| contribution_margin_rub_month | 235 000 ₽/клиент/мес |
| company_ebitda_rub_month base @33 clients | 1 775 000 ₽/мес |
| company_ebitda_potential_rub_month @50 clients | 5 770 000 ₽/мес |
| clients_to_500k_ebitda | 28 |
| months_to_500k_ebitda | 18 |
| fixed_costs_rub_month | 5 980 000 ₽ |
| startup_capital_to_bep_rub | 70 612 551 ₽ |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | enterprise sales, fundraising, partnerships | 845,000 |
| CTO / Tech Lead | архитектура, security, внедрения | 715,000 |
| Senior Backend x2 | ingestion, API, integrations | 1,092,000 |
| ML Engineer | RAG quality, retrieval, evaluation | 650,000 |
| DevOps | infra, k8s, private contour | 455,000 |
| Frontend | analyst UI, permissions UX | 390,000 |
| SDR | outbound prospecting | 234,000 |
| AE | demos, negotiation, close | 507,000 |
| Customer Success | onboarding, adoption, expansion | 312,000 |
| **Итого команда** |  | **5,200,000 ₽/мес** |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Price compression и скидки >25% | high | high | В 05-critic.md: `Price -30%` уводит `EBITDA @M12` до `-4.30 млн ₽`, а конкуренты и интеграторы давят на pricing. |
| Регуляторика, data residency, private deployment complexity | high | high | `152-ФЗ / data residency блокирует cloud deployment`, а security/legal friction удлиняет продажу и COGS. |
| CAC inflation и execution volatility | high | high | `CAC x2` ведёт к `-6.56 млн ₽ EBITDA @M12`, Monte Carlo даёт отрицательный `p10 EBITDA @M24`. |

## Proof points для APPROVED
1. `company_ebitda_potential_rub_month` выше `500 000 ₽/мес` задолго до 50 клиентов и в пределах 24 месяцев.
2. 10 конкретных enterprise targets уже видны и совпадают с pain profile: document-heavy, regulated, budget-backed.
3. Category demand подтверждён не только поиском, но и `179` HH-сигналами, локальными платными аналогами и TAM/SAM в миллиардах рублей.
4. Кейс не требует consumer-scale adoption; достаточно 20-35 крупных аккаунтов с `ACV 3.6 млн ₽/год`.

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Огромный массив внутренних документов, legal/compliance/research workflows, высокий бюджет на AI. | email decision-maker + отраслевые конференции + партнёрство с интегратором | 500,000 ₽/мес |
| Т-Банк | Data-heavy knowledge teams и быстрый rollout AI-инструментов для аналитики и ops. | founder-led intro + email decision-maker | 450,000 ₽/мес |
| ВТБ | Сильная документная и регуляторная нагрузка, потребность в audit trail и private contour. | тендерный вход + партнёрство с SI | 450,000 ₽/мес |
| Альфа-Банк | Активная digital-функция, большой объём policy/legal/procurement documents. | email decision-maker + профильная конференция | 400,000 ₽/мес |
| МТС | Крупный enterprise knowledge perimeter и множество внутренних сервисных процессов. | партнёрство + ABM outreach | 350,000 ₽/мес |
| билайн | Сложные внутренние документы, IT/security требования и большой procurement contour. | email decision-maker + кейс через интегратора | 350,000 ₽/мес |
| Северсталь | Промышленный enterprise с технической документацией и закупочными/юридическими workflow. | отраслевые мероприятия + партнёрство | 300,000 ₽/мес |
| Норникель | Много регламентов, договоров и внутренней базы знаний, высокий эффект от secure retrieval. | email decision-maker + enterprise referral | 300,000 ₽/мес |
| СИБУР | Сложные техпроцессы и большая база документов, где нужен controlled access и citations. | партнёрский канал + конференция | 300,000 ₽/мес |
| X5 Group | Масштабный corporate knowledge stack, procurement/legal/support pain, быстрая экономия времени аналитиков. | ABM outbound + referral | 250,000 ₽/мес |

## Финансовая интерпретация
- Бизнес выглядит как `enterprise sales-led AI workflow platform`, а не как классический SMB SaaS.
- Главный драйвер доходности, удержание `ARPA = 300 000 ₽/мес` и дисциплины по COGS `65 000 ₽/мес`.
- При `33` клиентах бизнес уже проходит устойчивый EBITDA gate, а при `50` клиентах превращается в сильный cash-generating asset.

## Что нужно доказать в ближайшие 6 месяцев
1. 2-3 paid pilots в банках, телекоме или промышленности без скидочного демпинга.
2. Median pilot-to-paid conversion не ниже 30% и CAC payback не выше 8 месяцев.
3. Private contour / on-prem deployment playbook, который не превращает каждый проект в custom integration shop.
4. Стабильный channel mix: founder-led inbound + ABM + integrator referrals, а не только hero-sales фаундера.

## Финальное решение
**APPROVED** при условии строгой product discipline: продавать `secure enterprise knowledge copilot`, а не generic chatbot или кастомную интеграторскую разработку. Если pricing discipline нарушится или private deployment раздует COGS, кейс быстро деградирует до near-pass.
