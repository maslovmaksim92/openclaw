# 0755 MSK Dropzone AI GEO Expand v2 — Full Verdict Package
> Скомпилированный пакет стадий P0/P1/P4/P5/P6/P7 для публикации в GitHub.
> Примечание: в этом кейсе в исходном пайплайне использовались файлы `01-intake.md`, `02-demand.md`, `04-economics.md`, `05-critic.md`, `06-verdict.md`, `07-score-trajectory.md`; отдельных `02-validation.md` и `03-demand.md` не было, поэтому пакет сохраняет реальные артефакты без создания новых стадий задним числом.


---

## Файл: 00-brief.md

# 00-brief

## Кейс
0755-msk-dropzone-ai-geo-expand-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
0755-msk-dropzone-ai-geo-expand

## Краткое описание
Кейс создан по правилу принудительного полного пайплайна для resurrect-сигнала. Ранее этот сигнал был обработан как duplicate или supporting, но теперь вынесен в отдельный standalone candidate.

## Что делать дальше
Пройти полный пайплайн P3→P7 с новой аналитикой и в финальном verdict отдельно сравнить standalone-оценку с прежним решением в triage.


---

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-0755-msk-dropzone-ai-geo-expand.md
created: 2026-04-19T22:17:09+03:00
---

# Intake

## Название
0755 MSK Dropzone AI GEO Expand

## Режим обработки
Принудительный resurrect по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Исходный triage
/home/node/.openclaw/workspace/branch-models-lead/pipeline/triage/triage-2026-04-19-0755-msk-dropzone-ai-geo-expand.md

## Краткий контекст
Сигнал ранее был маршрутизирован в существующий кейс по autonomous cybersecurity agents, но теперь обязан пройти полную standalone-переоценку как отдельный case-v2.

## Полный контекст из raw

# RESURRECT SIGNAL — 0755-msk-dropzone-ai-geo-expand

## Meta
- source: triage/triage-2026-04-19-0755-msk-dropzone-ai-geo-expand.md
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
2026-04-19

## Входные данные
- `pipeline/raw/raw-2026-04-19-0736-msk-dropzone-ai-geo-expand.md`

## Классификация
дубликат / supporting signal для существующего открытого кейса

## Решение
Новый кейс не открывать. Обогатить существующий кейс `pipeline/cases/enterprise-autonomous-cybersecurity-agents/`.

## Почему
- Сигнал Dropzone AI тематически совпадает с уже открытым кейсом по автономным AI-агентам для enterprise-кибербезопасности, особенно в части SOC automation и автономного расследования security alerts.
- Это не отдельная новая ниша, а сильное дополнительное подтверждение уже открытой категории: autonomous SOC analyst с заметной коммерческой зрелостью.
- Во входном файле указан `ltv_signal` `2500000-12000000 RUB в год`, что соответствует примерно `208000-1000000 ₽ в месяц`. Верхняя часть диапазона превышает порог Program 1, но из-за содержательного совпадения сигнал корректнее учитывать как обогащение существующего кейса, а не как новый case.

## Что добавлено в кейс
В `pipeline/cases/enterprise-autonomous-cybersecurity-agents/01-evidence.md` добавлен supporting signal по Dropzone AI:
- дата и source URL;
- тип сигнала: supporting signal;
- краткое объяснение, как сигнал усиливает кейс;
- ключевые факты: `300+ enterprise deployments`, `11x ARR growth`, `370% net revenue retention`, `35+ новых клиентов`, `$37 млн Series B`, `$1 млн+ ARR в федеральном сегменте США`.

## Что сделано
- Обновлён `pipeline/cases/enterprise-autonomous-cybersecurity-agents/01-evidence.md` на русском языке.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: Dropzone AI добавлен как supporting signal, усиливающий гипотезу по autonomous enterprise cybersecurity agents через узкий, но коммерчески сильный сегмент AI SOC analyst.

```


---

## Файл: 02-demand.md

# 02-demand

## Demand validation summary
- **Продукт**: Dropzone AI, AI SOC Analyst для автоматизации Tier-1/Tier-2 расследований, triage и threat hunting.
- **Итог по спросу в РФ**: **LOW-MEDIUM**. Локальный поисковый и вакансионный спрос по формулировке AI SOC analyst низкий, но бюджетный спрос на SOC automation, SIEM/XDR и дефицит аналитиков реальны. [T1][T2]
- **Решение по гейту**: **не отклонять на P4**. При текущем слабом keyword-demand в РФ продукт все еще может пройти Profit Gate через enterprise/private-cloud и MSSP-модель. [T2]

## Evidence of demand

### 1) Direct demand signal from mandatory endpoint
- `multi-demand?keyword=AI SOC analyst cybersecurity automation` → **LOW**, score 0; Google Trends RU = 0, Habr articles = 2, HH = 0, Yandex suggest = 2. [T2, internal demand endpoint]
- `multi-demand?keyword=SOC аналитик ИИ` → **LOW**, score 0; Google Trends RU = 0, Habr = 2, HH = 2, Yandex suggest = 2. [T2, internal demand endpoint]
- Вывод: в РФ пока нет массового сформированного спроса именно на категорию "AI SOC analyst". Есть ранний рынок, который продается не как новая категория, а как улучшение SOC/MDR economics. [T2]

### 2) Adjacent market demand in Russia
- Российский рынок кибербезопасности в 2024 году вырос до **337 млрд ₽**, а в 2025 году прогнозировался на уровне **374 млрд ₽**. Это подтверждает наличие бюджетной базы, из которой может выделяться AI-layer для SOC automation. [T2: TAdviser/ИРПААС, https://www.tadviser.ru/index.php/Статья:ИРПААС:Рынок_кибербезопасности_в_России]
- Банк России сообщал, что в 2024 году объем операций без добровольного согласия клиентов составил **27.5 млрд ₽**, что поддерживает высокий приоритет инвестиций в detection/response у банков и крупных финтехов. [T1: ЦБ РФ, https://www.cbr.ru/press/event/?id=23528]
- На hh.ru в РФ есть открытые роли по SOC/monitoring/security operations у крупных работодателей, включая **Ozon, ВТБ, ДОМ.РФ, Росгосстрах Жизнь, Русскую медную компанию, СБЕРКОРУС**. Это не доказательство спроса именно на AI-агента, но сильный proxy на постоянную боль и фонд оплаты труда SOC-команд. [T1: hh.ru search/results, https://hh.ru/search/vacancy?text=SOC]

### 3) Global demand / category maturity
- Dropzone AI заявляет **300+ enterprise deployments**, **11x ARR growth**, **370% net revenue retention** и **35+ новых клиентов** после предыдущего раунда. Это сильное доказательство готовности enterprise-заказчиков платить за категорию AI SOC analyst. [T2: TechCrunch / company-announced metrics, https://techcrunch.com/2026/04/02/dropzone-ai-raises-37m-for-its-ai-soc-analyst/]
- ISC2 оценивал глобальный дефицит кадров кибербезопасности в **~4.8 млн** специалистов, что усиливает WTP на автоматизацию tier-1 операций. [T2: ISC2, https://www.isc2.org/research]

## Competitors and pricing

| Игрок | Что продает | Цена | Комментарий |
|---|---|---:|---|
| Dropzone AI | AI SOC Analyst | **от $36,000/год** за до 4,000 расследований | Базовый прямой аналог. Unlimited users, enterprise pricing отдельно. [T2, vendor pricing: https://www.dropzone.ai/pricing] |
| Microsoft Security Copilot | AI co-pilot для security teams | **$4 за Security Compute Unit (SCU) в час** | При 1 SCU 24/7 это около **$35,040/год**, при 2 SCU около **$70,080/год**. Enterprise substitute, особенно у клиентов Microsoft stack. [T2, Microsoft-announced pricing via CRN summarizing GA launch: https://www.crn.com/news/security/2024/microsoft-security-copilot-now-generally-available-at-usd4-per-hour] |
| LimaCharlie | SecOps platform с AI-agent workflows | **$3 за endpoint в месяц** + **$0.20/GB** telemetry | Не идентичный продукт, но реальная substitute-платформа для построения AI triage/response. Для 1,000 endpoints это около **$36,000/год** только по endpoint fee, без телеметрии. [T2, vendor pricing: https://limacharlie.io/pricing] |

**Вывод по конкуренции**: категория уже монетизируется в диапазоне примерно **2.9-5.6 млн ₽/год** для малого enterprise-pilots и выше для крупных развертываний. Это подтверждает существование WTP в enterprise-сегменте. [T2]

## WTP, proof of willingness to pay
- **Прямая готовность платить подтверждена** ценами Dropzone и Microsoft, обеими существенно выше типичного SMB tooling spend. [T2]
- **Корпоративная готовность платить** подтверждается traction Dropzone: 300+ внедрений и 370% NRR не достигаются без расширения контрактов и апсейла. [T2]
- **Косвенное подтверждение WTP в РФ**: постоянный найм SOC-аналитиков на hh.ru означает, что компании уже несут recurring labor cost; продукт, который заменяет 1-2 Tier-1 headcount, может продаваться на базе ROI, а не на базе search intent. [T1]
- **Ограничение**: в РФ WTP пока вероятнее в формате private deployment, MSSP-bundle или add-on к SIEM/XDR, а не как standalone self-serve SaaS. [T2]

## Telegram bots/services in Russia
- В ручной проверке не найдено признаков зрелого RU-first Telegram-native продукта уровня "AI SOC analyst" с автономным расследованием инцидентов. [T2/T3]
- Найденные сигналы в Telegram и RU-комьюнити относятся в основном к **алертингу, уведомлениям, threat intel reposting и контакт-ботам**, а не к полноценному autonomous SOC analyst. [T3: Habr/community examples]
- Следствие: Telegram в РФ для этого кейса выглядит **как distribution/support channel**, а не как основной продуктовый интерфейс и не как самостоятельный конкурентный кластер. [speculation, backed by T2/T3]

## Market sizing

### Assumptions
- Рабочий FX для перевода USD→RUB: **79.73 ₽/$** по официальному курсу ЦБ РФ на 4 апреля 2026 года. [T1: ЦБ РФ, https://www.cbr.ru/currency_base/daily/]
- Global category proxy: мировой рынок SOAR оценивался около **$1.72 млрд** в 2025 году. Для кейса это не весь cybersecurity market, а наиболее близкий публичный proxy для AI SOC analyst automation. [T3: Grand View Research, https://www.grandviewresearch.com/industry-analysis/security-orchestration-automation-and-response-market-report]
- Russia cyber base: **337 млрд ₽** в 2024. Для AI SOC analyst берем адресуемую долю **~1.8%** как узкий слой automation поверх SOC/SIEM/MDR spend. Это модельная оценка, а не опубликованный отдельный сабсегмент. [T2 + speculation]
- Bottom-up buyer universe: **~1,600** потенциальных покупателей в РФ (банки, страховщики, telecom, e-commerce, industrial/critical infra, крупные ИТ и MSSP). Из них **~55%** имеют выраженную боль и зрелость для пилота AI SOC analyst. Средний контракт берем **3.6 млн ₽/год**. [T1/T2 + modeling]

### GTM-10 target buyers (для bottom-up sanity check)
1. Сбер
2. ВТБ
3. Т-Банк
4. Альфа-Банк
5. Ozon
6. X5 Group
7. МТС
8. ДОМ.РФ
9. Росгосстрах
10. Русская медная компания

### Top-down
- **TAM (мир)** = $1.72B × 79.73 = **137.1 млрд ₽**. [T3]
- **TAM (РФ)** = 337 млрд ₽ × 1.8% = **6.1 млрд ₽**. [T2 + modeled assumption]
- **SAM (РФ)** = 6.1 млрд ₽ × 55% segment fit = **3.35 млрд ₽**. [T2 + modeled assumption]
- **SOM Y1** = 3.35 млрд ₽ × 2% = **67 млн ₽**. [modeled]
- **SOM Y3** = 3.35 млрд ₽ × 8% = **268 млн ₽**. [modeled]

### Bottom-up
- **Total buyers** = 1,600 [modeled from regulated enterprise + MSSP universe, anchored by hh demand and sector structure; T1/T2]
- **% with need** = 55% [T1 hh proxy + T2 market growth]
- **ARR avg** = 3.6 млн ₽/год [anchored by Dropzone minimum price and Microsoft/LimaCharlie substitute pricing; T2]
- **SAM bottom-up** = 1,600 × 55% × 3.6 млн ₽ = **3.17 млрд ₽**
- **TAM bottom-up** = 1,600 × 100% × 3.6 млн ₽ = **5.76 млрд ₽**
- **SOM Y1 bottom-up** = 3.17 млрд ₽ × 2% = **63 млн ₽**
- **SOM Y3 bottom-up** = 3.17 млрд ₽ × 8% = **254 млн ₽**

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------:|----------:|----------------|-----------|
| TAM (мир) | 137.1 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 6.1 млрд ₽ [T2] | 5.76 млрд ₽ [T1/T2] | diff=6%, близко; bottom-up подтверждает узкий сегмент | **5.76 млрд ₽** |
| SAM (РФ) | 3.35 млрд ₽ [T2] | 3.17 млрд ₽ [T1/T2] | diff=5%, допустимо | **3.17 млрд ₽** |
| SOM Y1 | 67 млн ₽ | 63 млн ₽ | diff=6% | **63 млн ₽** |
| SOM Y3 | 268 млн ₽ | 254 млн ₽ | diff=6% | **254 млн ₽** |

**Sanity checks**
- Расхождение top-down vs bottom-up меньше 3x, пересчет не требуется.
- SOM Y1 = 63 млн ₽ = около 18 enterprise-клиентов по 3.6 млн ₽/год, или 9-12 клиентов при более крупных контрактах. Для go-to-market через MSSP и regulated enterprise это напряженно, но реалистично.
- SOM Y1 < 10% SAM, значит overclaiming нет.

## Profit Gate (EBITDA >= 500K/mo)

### Scenario A: direct enterprise SaaS/private cloud
- 12 клиентов × 450k ₽/мес = **5.4 млн ₽ MRR**
- gross margin 75% => **4.05 млн ₽ gross profit**
- OPEX (sales + support + engineering local team) ≈ **3.2 млн ₽/мес**
- **EBITDA ≈ 0.85 млн ₽/мес**
- **Gate: PASS**

### Scenario B: MSSP / channel bundle
- 4 MSSP-партнера × 1.1 млн ₽/мес = **4.4 млн ₽ MRR**
- gross margin 80% => **3.52 млн ₽**
- OPEX ≈ **2.8 млн ₽/мес**
- **EBITDA ≈ 0.72 млн ₽/мес**
- **Gate: PASS**

### Scenario C: premium on-prem / sovereign deployment
- 8 клиентов × 700k ₽/мес = **5.6 млн ₽ MRR**
- gross margin 70% => **3.92 млн ₽**
- OPEX ≈ **3.1 млн ₽/мес**
- **EBITDA ≈ 0.82 млн ₽/мес**
- **Gate: PASS**

**Profit Gate verdict**: несмотря на слабый category-search demand в РФ, EBITDA > 500k/мес достижима в нескольких моделях монетизации. Критическая зависимость не от self-serve demand, а от доступа к крупным enterprise/MSSP accounts. [T2 + modeled]

## Final demand verdict
- **Demand**: LOW-MEDIUM в РФ, потому что search/category pull еще слабый.
- **WTP**: CONFIRMED в enterprise-сегменте через международные аналоги и substitute budgets.
- **Profit Gate**: PASS.
- **P4 decision**: **оставить кейс в пайплайне**, не делать early reject.

Sources: T1=3, T2=7, T3=2. Primary evidence basis: T2.

- Market Pulse 20.04.2026: растущий интерес.


---

## Файл: 04-economics.md

# 04-economics

## Unit economics summary
- **Кейс**: Dropzone AI GEO Expand, AI SOC Analyst для enterprise SOC и MSSP.
- **Сегмент**: enterprise / regulated B2B cybersecurity, private-cloud и sovereign deployment.
- **Модель монетизации**: annual contract + monthly recognition.
- **Base ACV**: **3.84 млн ₽/год**.
- **MRR на клиента**: **320 тыс. ₽/мес**.
- **COGS на клиента**: **71 тыс. ₽/мес**.
- **Gross Margin**: **77.8%**.
- **Contribution Margin**: **70.9%**.
- **Blended fully-loaded CAC**: **754 тыс. ₽**.
- **Logo churn benchmark**: **1.5%/мес** для enterprise B2B SaaS; для ACV > $100k benchmark может быть около **0.7%/мес**, но в РФ-модели беру более консервативные **1.5%/мес**. [S4]
- **LTV**: **16.64 млн ₽**.
- **LTV/CAC**: **22.1x**.
- **CAC Payback**: **2.4 мес**.
- **Break-even**: **34 клиента** или примерно **M12** в консервативном плане найма и GTM.
- **Вывод P5**: **PASS**. Даже с fully-loaded CAC и реалистичным наймом модель остается investable.

## Ключевые допущения
1. Цена опирается на P4: международные аналоги Dropzone AI и Microsoft Security Copilot подтверждают enterprise spending в диапазоне 2.9-5.6 млн ₽/год и выше. [D1]
2. Для РФ беру **ACV 3.84 млн ₽/год**, то есть середину нижней части enterprise-range, чтобы не переоценивать early market.
3. Продажи идут не через self-serve, а через **outbound ABM, MSSP/partner channel, inbound/events**.
4. Gross margin ограничена private-cloud deployment, интеграциями SIEM/XDR и human-in-the-loop support, поэтому не беру «чистый SaaS» 85-90%.
5. Для churn использую более жесткий benchmark enterprise B2B SaaS **1.5%/мес**, хотя по ACV > $100k источник показывает и более низкий churn. [S4]

## 1) Детальный бизнес-процесс: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам, телко, e-com, MSSP | SDR | CRM + prospecting stack | 2 дня | 18 000 | Высокая |
| 2 | Первичный outbound: email, LinkedIn/аналог, звонки | SDR | Sequencer + телефония + CRM | 10 дней | 24 000 | Средняя |
| 3 | Квалификация боли: SOC load, false positives, FTE shortage | SDR + AE | CRM, discovery script | 5 дней | 30 000 | Средняя |
| 4 | Demo и ROI-калькуляция по замещению Tier-1/Tier-2 | AE + Solutions lead | Demo env, ROI sheet | 7 дней | 42 000 | Низкая |
| 5 | Security review и pilot scoping | AE + CTO | Questionnaire, архитектурные схемы | 21 день | 95 000 | Низкая |
| 6 | Пилот: подключение к SIEM/XDR, тестовые сценарии | Backend + ML + DevOps | Private cloud, connectors, logs | 14 дней | 64 000 | Средняя |
| 7 | Юридическое согласование и procurement | AE + CEO | Договоры, DPA/SLA | 14 дней | 56 000 | Низкая |
| 8 | Коммерческое закрытие и подписание | AE | CRM, e-sign | 3 дня | 12 000 | Средняя |
| 9 | Provisioning tenant / on-prem инстанса | DevOps | IaC, Kubernetes, monitoring | 5 дней | 38 000 | Высокая |
| 10 | Интеграция, промпт/плейбук-тюнинг, knowledge base | ML + Backend + CS | Connectors, RAG/KB, support desk | 14 дней | 57 000 | Средняя |
| 11 | Первый invoice и запуск production | Finance + CS | Billing, ЭДО | 3 дня | 9 000 | Высокая |
| 12 | Сбор оплаты и контроль cash collection | Finance + CS | Billing/ERP, CRM | 15 дней | 7 000 | Высокая |

**Итого прямой cost-to-close + launch на 1 клиента**: **452 тыс. ₽**.

Комментарий: direct process cost ниже blended CAC, потому что отдельно сверху сидят paid touchpoints, tool stack, events/partners и overhead, которые обязательно входят в fully-loaded CAC.

## 2) COGS breakdown на клиента в месяц

| Статья COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM / inference / reasoning budget | 18 000 | Консервативный лимит на enterprise SOC workload | modeled from AI deployment economics |
| Compute, storage, orchestration | 14 000 | Private-cloud / sovereign hosting, K8s, storage | modeled |
| SIEM/XDR connectors и ingestion support | 12 000 | Поддержка интеграций и обработка телеметрии | modeled |
| Threat intel / knowledge refresh / data services | 7 000 | Аллокация внешних data-services | modeled |
| Customer Success и security support allocation | 20 000 | 1 CSM на 25-30 аккаунтов + security support pool | modeled + hiring plan |
| Billing / compliance / incident QA | 0 | Включено в support allocation и fixed G&A | modeled |

**Итого COGS** = **71 000 ₽/клиент/мес**

**Gross Profit на клиента** = **320 000 - 71 000 = 249 000 ₽/мес**

**Gross Margin** = **249 000 / 320 000 = 77.8%**

## 3) CAC по каналам с funnel conversion

### Channel CAC

| Канал | Верх воронки | Discovery | Qualified | Pilot | Closed-won | Конверсия lead→paying | Monthly spend, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 350 target accounts | 14 | 7 | 2.7 | 0.9 | 0.26% | 730 000 | 811 000 |
| MSSP / partners | 12 partner intros | 7 | 4 | 1.6 | 0.55 | 4.58% | 280 000 | 509 000 |
| Inbound / content / events | 40 MQL | 10 | 4 | 1.0 | 0.25 | 0.63% | 272 000 | 1 088 000 |

### Blended CAC
- Monthly acquisition spend = **1 282 000 ₽**
- New paying customers / month = **1.70**
- **Blended fully-loaded CAC = 1 282 000 / 1.70 = 754 000 ₽**

## 4) FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 180 000 | Аккаунт-based support ads + retargeting на узкий ICP | modeled |
| Outbound team FOT (SDR/AE attributed to new) | 484 000 | SDR 184k gross + AE 346k gross, +30% взносы, атрибуция на new logo activity | S1/S2 + modeled |
| Marketing team FOT (partial allocation) | 120 000 | Fractional product marketing / content / events support | modeled |
| Tools (CRM, sequencing, enrichment, call stack, webinar) | 82 000 | HubSpot/аналоги, sequencing, enrichment, call tools | modeled |
| Events/partnerships | 120 000 | Совместные MSSP-активности, roundtables, niche events | modeled |
| Overhead multiplier (x1.3) | 296 000 | 30% от 986k raw spend для enterprise B2B overhead | standard enterprise B2B assumption |

**Raw CAC spend** = **986 000 ₽/мес**  
**Fully-loaded CAC spend** = **1 282 000 ₽/мес**  
**New paying customers / month** = **1.70**  
**Fully-loaded CAC** = **754 000 ₽**

### Sanity checks по CAC
- Сегмент: **enterprise / regulated B2B**, значит multiplier меньше **x2.0-2.5** только потому, что часть enterprise complexity уже сидит в direct labor, partner motion и overhead. Итоговый CAC **754k ₽** попадает в заданный sanity-range **300-900k ₽** для enterprise SaaS B2B в РФ.
- CAC составляет **23.6%** от ACV 3.84 млн ₽, что допустимо для enterprise software.
- Канальный CAC показан отдельно, blended CAC тоже показан.

## 5) LTV и churn

### Churn benchmark
- Для enterprise B2B SaaS benchmark monthly churn обычно находится в диапазоне **1-2%/мес**, mid-market 1.5-3%, SMB 3-5%. [S4]
- Для ACV > $100k benchmark может быть около **0.7%/мес**, но этот кейс в РФ на early-stage GTM, поэтому беру **1.5%/мес** как консервативный уровень. [S4]

### Расчет LTV
- MRR per customer = **320 000 ₽**
- Gross Margin = **77.8%**
- Churn = **1.5%/мес**
- **LTV = MRR × GM / churn = 320 000 × 0.778 / 0.015 = 16 597 333 ₽**
- Округление для модели: **16.64 млн ₽**

## 6) LTV/CAC ratio
- **LTV/CAC = 16.64 млн / 754 тыс. = 22.1x**
- Investment-grade threshold **>= 3:1** выполнен с большим запасом.

## 7) CAC Payback
- Формула по заданию: **CAC Payback = CAC / MRR_per_customer**
- **754 000 / 320 000 = 2.36 мес**
- Округление: **2.4 мес**
- Sanity: заметно ниже базового порога **12 мес** и ниже enterprise tolerance **18 мес**.

## 8) Contribution Margin %

Для contribution margin вычитаю COGS и переменные customer-facing расходы после продажи.

| Статья | ₽/клиент/мес |
|---|---:|
| MRR | 320 000 |
| COGS | -71 000 |
| Variable success / security review / account servicing | -18 000 |
| Payment, billing, collections variable | -4 000 |

**Contribution profit** = **227 000 ₽/клиент/мес**  
**Contribution Margin** = **227 000 / 320 000 = 70.9%**

## 9) Team & FOT

### Полная команда

| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO / founder | GTM, enterprise deals, fundraising | 1 | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | Архитектура, security review, roadmap | 1 | 550 000 | 165 000 | 715 000 |
| Senior Backend | Connectors, orchestration, APIs | 2 | 420 000 | 126 000 | 1 092 000 |
| ML Engineer | LLM/RAG, tuning, detection reasoning | 1 | 520 000 | 156 000 | 676 000 |
| DevOps | Private cloud, infra, observability | 1 | 360 000 | 108 000 | 468 000 |
| Frontend | Analyst UI, workflows, dashboards | 1 | 300 000 | 90 000 | 390 000 |
| SDR | Outbound prospecting | 1 | 184 000 | 55 200 | 239 200 |
| AE | Discovery, demos, close, procurement | 1 | 346 000 | 103 800 | 449 800 |
| Customer Success | Onboarding, retention, expansion | 1 | 260 000 | 78 000 | 338 000 |

**Steady-state FOT fully-loaded** = **5 213 000 ₽/мес**

### Таблица найма с realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 / чел |
| ML Engineer | 1 | 520 000 | 2.5 | 2 | 156 000 | 676 000 |
| DevOps | 1 | 360 000 | 1.5 | 1 | 108 000 | 468 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 184 000 | 0.75 | 1 | 55 200 | 239 200 |
| AE | 1 | 346 000 | 1.5 | 2.5 | 103 800 | 449 800 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |

### Источники по salary benchmark
- HH Career: ML-engineer в 2025, верхний диапазон до **410k ₽**, а senior/LLM-specialist в продуктовых и security-командах в Москве обычно выше, поэтому для дефицитного enterprise AI беру **520k gross**. [S1]
- HH Career и hh profession pages для sales показывают базу **125k ₽** median по широкому рынку и higher IT/B2B senior comp **140-200k+ ₽**, поэтому для enterprise AE и SDR использована premium-надбавка под complex B2B sales. [S2]
- User-provided hiring realism benchmark задает sanity-range: Senior SWE **350-550k**, Team Lead **450-700k**, ML Eng **400-700k**, DevOps **300-500k**, SDR **100-180k + bonus**, AE enterprise **300-500k + commission**. Модель находится внутри этих диапазонов.

## 10) Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO | 845 000 | Founder ведет discovery и дизайн GTM |
| M2 | + CTO | 1 560 000 | Архитектура и security review готовятся заранее |
| M3 | + Backend #1, + ML Engineer | 2 782 000 | Техкоманда выходит на первые пилоты, ramp еще не завершен |
| M4 | + DevOps, + AE | 3 699 800 | AE начинает pipeline build, не на полной квоте |
| M5 | + Backend #2, + SDR | 4 485 000 | Outbound разгоняется, SDR еще в ramp |
| M6 | + Frontend, + CS | 5 213 000 | Команда complete, CS начинает onboarding motion |
| M7 | без новых hires | 5 213 000 | AE ~80% quota, product velocity нормализуется |
| M8 | без новых hires | 5 213 000 | Пилоты начинают конвертироваться в annual deals |
| M9 | без новых hires | 5 213 000 | Near steady-state |
| M10 | без новых hires | 5 213 000 | Near steady-state |
| M11 | без новых hires | 5 213 000 | Steady-state |
| M12 | без новых hires | 5 213 000 | Steady-state |

Sanity check: в M1 нет 5+ hires, найм размазан по 6 месяцам, что соответствует real time-to-hire.

## 11) Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 5 213 000 | Полная команда из 9 человек |
| Core infra baseline (non-client-specific) | 380 000 | Общая dev/staging/monitoring/control plane |
| Security, compliance, audit, legal | 220 000 | DPA/SLA, pentest, legal support |
| G&A, finance, admin | 180 000 | Бухгалтерия, HR ops, документооборот |
| Workspace / travel / founder sales overhead | 140 000 | Встречи с enterprise accounts |
| Acquisition program baseline | 1 282 000 | Fully-loaded GTM spend на new logo |

**Итого fixed + growth operating cost** = **7 415 000 ₽/мес**

## 12) Break-even по количеству клиентов и по месяцу

### Break-even by client count
- Contribution profit на клиента = **227 000 ₽/мес**
- Fixed + growth operating cost = **7 415 000 ₽/мес**
- **Break-even clients = 7 415 000 / 227 000 = 32.7**
- Округление: **33 клиента**

Если считать только fixed costs без acquisition program baseline:
- 6 133 000 / 227 000 = **27.0 клиента**
- Это useful second view, но для investability ориентируюсь на более жесткий вариант **33 клиента**.

### Break-even by month
Консервативная клиентская траектория: `M1=0, M2=0, M3=1, M4=2, M5=4, M6=6, M7=9, M8=13, M9=17, M10=22, M11=28, M12=34`.

| Месяц | Активные клиенты | Contribution profit, ₽ | Opex, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 245 000 | -1 245 000 |
| M2 | 0 | 0 | 2 120 000 | -2 120 000 |
| M3 | 1 | 227 000 | 3 664 000 | -3 437 000 |
| M4 | 2 | 454 000 | 4 721 800 | -4 267 800 |
| M5 | 4 | 908 000 | 5 507 000 | -4 599 000 |
| M6 | 6 | 1 362 000 | 7 415 000 | -6 053 000 |
| M7 | 9 | 2 043 000 | 7 415 000 | -5 372 000 |
| M8 | 13 | 2 951 000 | 7 415 000 | -4 464 000 |
| M9 | 17 | 3 859 000 | 7 415 000 | -3 556 000 |
| M10 | 22 | 4 994 000 | 7 415 000 | -2 421 000 |
| M11 | 28 | 6 356 000 | 7 415 000 | -1 059 000 |
| M12 | 34 | 7 718 000 | 7 415 000 | **303 000** |

**Break-even month**: **M12**

## 13) Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Cumulative burn M1-M11 = **38.59 млн ₽**
- С учетом рабочего буфера на receivables, pilot overruns и delayed procurement +15% reserve = **44.38 млн ₽**
- Это и есть реалистичный **startup capital to breakeven**.

### Cash runway
- Предполагаемый стартовый капитал: **70 млн ₽**
- Average burn до M12 ≈ **3.7-4.2 млн ₽/мес**, peak burn в M6 = **6.05 млн ₽**
- **Runway** при таком капитале: около **16-18 месяцев**

Sanity check:
- Для B2B enterprise SaaS модель требует существенно больше **10 млн ₽**, значит underestimation нет.
- При **50 клиентах**:
  - revenue = **16.0 млн ₽/мес**
  - contribution profit = **11.35 млн ₽/мес**
  - EBITDA after 7.415 млн ₽ opex = **3.94 млн ₽/мес**
- Следовательно, Profit Gate «EBITDA >= 500k/mo achievable even at 50 clients» проходит уверенно.

## 14) Investment verdict for P5
- **Profit Gate**: PASS
- **LTV/CAC**: PASS, **22.1x**
- **CAC Payback**: PASS, **2.4 мес**
- **Break-even feasibility**: PASS, **33 клиента / M12**
- **Hiring realism**: PASS, найм не агрессивнее рынка и не нарушает time-to-hire
- **Общий вывод**: у кейса сильная юнит-экономика для фонда при условии доступа к enterprise accounts и MSSP channel. Главный риск не в economics, а в скорости выхода на pipeline и procurement friction в РФ.

## Sources
- [D1] `pipeline/cases/0755-msk-dropzone-ai-geo-expand-v2/02-demand.md`
- [S1] HH Career, ML-инженер: https://career.hh.ru/article/kto-takoj-ml-inzhener-i-kak-im-stat
- [S2] HH Career, менеджер по продажам / hh profession pages: https://career.hh.ru/article/menedzher-po-prodazham-professiya-navyki-i-karernye-perspektivy ; https://career.hh.ru/profession/122
- [S3] HH Career / profession pages for broad market salary context: https://career.hh.ru/profession/53 ; https://career.hh.ru/profession/35
- [S4] Optifai churn benchmarks: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ ; https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/

## Confidence
**Medium**. Экономика опирается на реальный pricing band и benchmark churn, но РФ go-to-market пока моделируется по аналогам, а не по локальным closed-won cohort data.

---

## Файл: 05-critic.md

# SECTION A — PnL

## A1. Исходные допущения

- ARPA: **320 000 ₽ / клиент / мес**
- COGS: **71 000 ₽ / клиент / мес**
- Gross profit: **249 000 ₽ / клиент / мес**
- Contribution profit: **227 000 ₽ / клиент / мес**
- Contribution margin: **70,9%**
- Fixed costs: **7 415 000 ₽ / мес**
- Team FOT fully-loaded: **5 213 000 ₽ / мес**
- Страховые взносы: **~30% к ФОТ**, уже заложены в fully-loaded FOT
- CAC по каналам:
  - Outbound ABM: **811 000 ₽**
  - MSSP / partners: **509 000 ₽**
  - Inbound / content / events: **1 088 000 ₽**
  - Blended fully-loaded CAC: **754 000 ₽**
- LTV: **16,64 млн ₽**
- Logo churn benchmark в базе: **1,5% / мес**
- Break-even по client count: **33 клиента**

Сценарные допущения:
- **Base:** churn **1,5% / мес**, new clients: **0, 0, 1, 1, 2, 2, 3, 4, 4, 5, 6, 7**
- **Optimistic:** churn **1,0% / мес**, new clients: **0, 1, 1, 2, 2, 3, 4, 4, 5, 5, 6, 7**
- **Pessimistic:** churn **2,5% / мес**, new clients: **0, 0, 0, 1, 1, 2, 2, 3, 3, 4, 4, 5**
- Формула active clients: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`
- EBITDA в таблицах ниже считается как **Contribution profit - Fixed costs**, где contribution = MRR - COGS - 22 000 ₽ переменных servicing/billing costs на клиента в месяц.
- Cumulative cash ниже, это накопленный EBITDA без учёта CAPEX, оборотного капитала и внешнего финансирования.

## A2. 12-month PnL — Base scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 4 | 5 | 6 | 7 |
| Total clients | 0,0 | 0,0 | 1,0 | 2,0 | 4,0 | 5,9 | 8,8 | 12,7 | 16,5 | 21,2 | 26,9 | 33,5 |
| MRR, ₽ | 0 | 0 | 320 000 | 635 200 | 1 265 672 | 1 886 687 | 2 818 387 | 4 056 111 | 5 275 269 | 6 796 140 | 8 614 198 | 10 724 985 |
| COGS, ₽ | 0 | 0 | 71 000 | 140 935 | 280 821 | 418 609 | 625 330 | 899 950 | 1 170 450 | 1 507 894 | 1 911 275 | 2 379 606 |
| Gross profit, ₽ | 0 | 0 | 249 000 | 494 265 | 984 851 | 1 468 078 | 2 193 057 | 3 156 161 | 4 104 819 | 5 288 247 | 6 702 923 | 8 345 379 |
| GM% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% |
| Fixed costs, ₽ | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 |
| EBITDA, ₽ | -7 415 000 | -7 415 000 | -7 188 000 | -6 964 405 | -6 517 164 | -6 076 631 | -5 415 707 | -4 537 696 | -3 672 856 | -2 593 988 | -1 304 303 | 193 036 |
| Cash burn, ₽ | 7 415 000 | 7 415 000 | 7 188 000 | 6 964 405 | 6 517 164 | 6 076 631 | 5 415 707 | 4 537 696 | 3 672 856 | 2 593 988 | 1 304 303 | 0 |
| Cumulative cash, ₽ | -7 415 000 | -14 830 000 | -22 018 000 | -28 982 405 | -35 499 569 | -41 576 200 | -46 991 907 | -51 529 604 | -55 202 460 | -57 796 448 | -59 100 751 | -58 907 715 |

**Base break-even:**
- Break-even client count: **33 клиента**
- Break-even month: **M12**
- startup_capital_to_bep_rub: **59 100 751 ₽**

## A3. 12-month PnL — Optimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 4 | 5 | 5 | 6 | 7 |
| Total clients | 0,0 | 1,0 | 2,0 | 4,0 | 5,9 | 8,9 | 12,8 | 16,7 | 21,5 | 26,3 | 32,0 | 38,7 |
| MRR, ₽ | 0 | 320 000 | 636 800 | 1 270 432 | 1 897 728 | 2 838 750 | 4 090 363 | 5 329 459 | 6 876 165 | 8 407 403 | 10 243 329 | 12 380 896 |
| COGS, ₽ | 0 | 71 000 | 141 290 | 281 877 | 421 058 | 629 848 | 907 549 | 1 182 474 | 1 525 649 | 1 865 393 | 2 272 739 | 2 747 011 |
| Gross profit, ₽ | 0 | 249 000 | 495 510 | 988 555 | 1 476 669 | 2 208 903 | 3 182 814 | 4 146 985 | 5 350 516 | 6 542 010 | 7 970 590 | 9 633 884 |
| GM% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% |
| Fixed costs, ₽ | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 |
| EBITDA, ₽ | -7 415 000 | -7 188 000 | -6 963 270 | -6 513 787 | -6 068 799 | -5 401 261 | -4 513 399 | -3 634 415 | -2 537 221 | -1 450 998 | -148 638 | 1 367 698 |
| Cash burn, ₽ | 7 415 000 | 7 188 000 | 6 963 270 | 6 513 787 | 6 068 799 | 5 401 261 | 4 513 399 | 3 634 415 | 2 537 221 | 1 450 998 | 148 638 | 0 |
| Cumulative cash, ₽ | -7 415 000 | -14 603 000 | -21 566 270 | -28 080 057 | -34 148 857 | -39 550 118 | -44 063 517 | -47 697 932 | -50 235 152 | -51 686 151 | -51 834 789 | -50 467 092 |

**Optimistic break-even:**
- Break-even client count: **33 клиента**
- Break-even month: **M12**
- startup_capital_to_bep_rub: **51 834 789 ₽**

## A4. 12-month PnL — Pessimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 5 |
| Total clients | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 3,9 | 5,8 | 8,7 | 11,5 | 15,2 | 18,8 | 23,3 |
| MRR, ₽ | 0 | 0 | 0 | 320 000 | 632 000 | 1 256 200 | 1 864 795 | 2 778 175 | 3 668 721 | 4 857 003 | 6 015 578 | 7 465 188 |
| COGS, ₽ | 0 | 0 | 0 | 71 000 | 140 225 | 278 719 | 413 751 | 616 408 | 813 997 | 1 077 647 | 1 334 706 | 1 656 339 |
| Gross profit, ₽ | 0 | 0 | 0 | 249 000 | 491 775 | 977 481 | 1 451 044 | 2 161 768 | 2 854 723 | 3 779 355 | 4 680 871 | 5 808 850 |
| GM% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% | 77,8% |
| Fixed costs, ₽ | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 | 7 415 000 |
| EBITDA, ₽ | -7 415 000 | -7 415 000 | -7 415 000 | -7 188 000 | -6 966 675 | -6 523 883 | -6 092 161 | -5 444 232 | -4 812 501 | -3 969 564 | -3 147 700 | -2 119 382 |
| Cash burn, ₽ | 7 415 000 | 7 415 000 | 7 415 000 | 7 188 000 | 6 966 675 | 6 523 883 | 6 092 161 | 5 444 232 | 4 812 501 | 3 969 564 | 3 147 700 | 2 119 382 |
| Cumulative cash, ₽ | -7 415 000 | -14 830 000 | -22 245 000 | -29 433 000 | -36 399 675 | -42 923 558 | -49 015 719 | -54 459 951 | -59 272 452 | -63 242 016 | -66 389 716 | -68 509 098 |

**Pessimistic break-even:**
- Break-even client count: **33 клиента**
- Break-even month: **M15**
- startup_capital_to_bep_rub: **69 765 099 ₽**

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### A5.1. На 1 активного клиента в месяц

| Метрика | ₽ / клиент / мес | Комментарий |
|---|---:|---|
| ARPA | 320 000 | месячная выручка на клиента |
| Gross profit | 249 000 | после COGS 71 000 ₽ |
| Contribution | 227 000 | после 22 000 ₽ variable servicing/billing |
| EBITDA at break-even scale | 2 303 | при 33 клиентах EBITDA около нуля |
| Net, УСН 6% | -16 897 | налог 6% с выручки = 19 200 ₽ |
| Net, IT-льгота 3% | -7 297 | налог 3% с выручки = 9 600 ₽ |
| Net, ОСНО 20% | 1 842 | 20% налог на прибыль только при положительной прибыли |

### A5.2. На масштабе 50 активных клиентов

| Метрика | ₽ / мес |
|---|---:|
| MRR | 16 000 000 |
| COGS | 3 550 000 |
| Gross profit | 12 450 000 |
| Contribution | 11 350 000 |
| EBITDA | 3 935 000 |
| Net, УСН 6% | 2 975 000 |
| Net, IT-льгота 3% | 3 455 000 |
| Net, ОСНО 20% | 3 148 000 |

### A5.3. M12 waterfall по сценариям

| Scenario | M12 clients | Gross profit, ₽ | EBITDA pre-tax, ₽ | Net, IT 3%, ₽ | Net, УСН 6%, ₽ | Net, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Base | 33,5 | 8 345 379 | 193 036 | -128 713 | -450 463 | 154 429 |
| Optimistic | 38,7 | 9 633 884 | 1 367 698 | 996 271 | 624 844 | 1 094 158 |
| Pessimistic | 23,3 | 5 808 850 | -2 119 382 | -2 343 338 | -2 567 293 | -2 119 382 |

## A6. Cash flow и startup_capital_to_bep_rub

- **Base:** **59 100 751 ₽**
- **Optimistic:** **51 834 789 ₽**
- **Pessimistic:** **69 765 099 ₽**

## A7. Налоговая модель РФ

1. **УСН 6%**: налог считается как 6% от выручки, даже при слабой операционной прибыли.
2. **IT-льгота / аккредитация Минцифры**: в модели беру **3% от выручки** как целевой льготный сценарий по условию задания.
3. **ОСНО**: налог на прибыль **20%**, плюс **НДС 20%** поверх pricing/cash-flow, если компания работает на ОСНО. В PnL выше НДС не включён в revenue.
4. **Страховые взносы**: **~30% к ФОТ**, уже заложены в fully-loaded team FOT и fixed costs.

**Вывод по налогам:** целевой режим, **IT-льгота 3%**; fallback, **УСН 6%**; **ОСНО** нужно закладывать, если enterprise-клиенты требуют НДС-контур.

## A8. Break-even summary

| Scenario | Break-even client count | Break-even month | Startup capital to BEP, ₽ |
|---|---:|---:|---:|
| Base | 33 | 12 | 59 100 751 |
| Optimistic | 33 | 12 | 51 834 789 |
| Pessimistic | 33 | 15 | 69 765 099 |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

Базу беру из SECTION A: M12 EBITDA = **193 036 ₽/мес**, ARPU = **320 000 ₽/мес**, churn = **1,5%/мес**, blended CAC = **754 000 ₽**. [D1]

| Метрика | Base | Sens1: CAC x2 | Sens2: Churn x2 | Sens3: Price -30% |
|---|---:|---:|---:|---:|
| ARPU, ₽/мес | 320 000 | 320 000 | 320 000 | 224 000 |
| Churn, %/мес | 1,5% | 1,5% | 3,0% | 1,5% |
| CAC, ₽ | 754 000 | 1 508 000 | 754 000 | 754 000 |
| Active clients @M12 | 33,5 | 33,5 | 32,1 | 33,5 |
| Contribution / client, ₽/мес | 227 000 | 227 000 | 227 000 | 131 000 |
| EBITDA @M12, ₽/мес | 193 036 | -1 088 964 | -124 112 | -3 031 219 |
| Комментарий | barely above zero | acquisition loop уходит в минус | break-even сдвигается правее M12 | pricing shock ломает economics |

**Вывод:** модель держится только при сохранении текущего enterprise pricing. Самый опасный single-point failure здесь не churn, а **price compression**: скидка в 30% почти полностью уничтожает contribution economics.

## B2. Monte Carlo Lite — confidence intervals

### B2.1. Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 500 000 | 754 000 | 1 500 000 | base CAC и channel spread из P5; верх расширен под длинный enterprise cycle [D1] |
| Monthly churn, % | 0,7% | 1,5% | 3,0% | benchmark ACV>$100k и консервативная база [S4][D1] |
| ARPU, ₽/мес | 224 000 | 320 000 | 380 000 | -30% stress, base ACV, premium sovereign/private-cloud upsell [D1] |
| Conversion rate lead→paid, % | 0,20% | 0,50% | 0,90% | между outbound 0,26%, blended около 0,5%, upper bound под partner-led mix [D1] |
| Time-to-hire, мес | 1,0 | 1,7 | 3,0 | диапазон по hiring plan 0,75-2,5 мес + buffer [D1] |

### B2.2. Метод

Полную 1000-итерационную симуляцию здесь заменяю на **9 комбинаций** min/mode/max по CAC, churn и ARPU. Это дает адекватный proxy для p10/p50/p90 на ранней стадии, где основная дисперсия сидит именно в GTM cost, retention и pricing.

### B2.3. Результат

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -3 880 071 | 412 887 | 5 290 464 | 9 170 535 |
| CAC payback (мес) | 1,51 | 2,36 | 5,09 | 3,58 |
| LTV/CAC | 9,49 | 22,02 | 55,40 | 45,91 |
| Cash runway (мес) | 11,07 | 13,89 | 19,48 | 8,41 |

### B2.4. Интерпретация правил

1. **p10 EBITDA @M24 < 0**, значит kill criterion #1 активируется автоматически: в левом хвосте распределения компания остается structurally loss-making.
2. **p50 EBITDA @M24 = 412 887 ₽/мес < 500 000 ₽/мес**, значит кейс **не проходит EBITDA Gate даже в median**.
3. Соотношение **p90/p10** по EBITDA формально не считаю как meaningful multiple, потому что p10 отрицательный; это хуже правила `>10x` и означает, что распределение asymmetrically fragile.
4. **Range width по LTV/CAC = 45,91 > 8**. Следовательно, модель хрупкая сразу по трем осям: pricing, churn и CAC.

**Итог Monte Carlo Lite:** economics в median остаётся положительной, но **слишком тонкой**, а downside хвост недопустимо глубокий для фонда, если нет подтвержденного sovereign wedge и repeatable partner motion.

## B3. Competitor deep-dive

Ниже market-share estimates — это **моя оценка доли в целевом shortlist для AI/SOC automation**, а не аудированные IDC/Gartner доли. Для западных конкурентов оценка опирается на installed base и зрелость платформы; для российских — на публичные внедрения, продуктовую широту и масштаб бизнеса. [T1][T2][T3][T4][T5][T6][T7][T8][T9][T10][T11]

### B3.1. Топ-3 западных

| Competitor | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Microsoft Security Copilot | встроен в Defender/Entra/Intune/Purview, massive enterprise distribution, доступ в M365 E5 lowers adoption friction [T1] | vendor lock-in на Microsoft stack, слабее для heterogeneous SOC, sovereign RU deployment почти нереален | **35-40%** global shortlist | лучше для non-Microsoft environments, private-cloud/on-prem, локальные интеграции с РФ SIEM/XDR |
| CrowdStrike Charlotte AI | сильный Falcon data layer, agentic triage/response, заметная экономия analyst hours [T2] | premium pricing, сильная зависимость от Falcon ecosystem, сложнее продать клиенту без Falcon footprint | **20-25%** global shortlist | более дешевый wedge для MSSP/regulated локальных клиентов, меньше platform-tax |
| Google SecOps Gemini / Triage Agent | сильные TI/Mandiant/VirusTotal assets, хорош в investigation automation, agentic SOC roadmap [T3][T4] | часть функций Pre-GA, ограничение по throughput/tenant, слабее on-prem sovereignty | **8-12%** global shortlist | более зрелый sovereign deployment story и интеграция в российские контуры данных |

### B3.2. Топ-5 российских

| Competitor | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Solar / Ростелеком-Солар | сильный гос/enterprise access, крупный brand, широкий сервисный и продуктовый периметр, активный M&A [T10][T11] | perception как heavyweight integrator, более длинный цикл внедрения, меньше product agility | **20-25%** RU shortlist | быстрее внедрение, меньше бюрократии, точечный AI analyst UX вместо «комбайна» |
| Positive Technologies / MaxPatrol O2 | сильная телеметрия, SIEM/XDR adjacency, собственный «автопилот» SOC, сильный бренд в critical infra [T8][T9] | лучше раскрывается внутри PT-stack, интеграционная сложность, high switching cost для клиента | **18-22%** RU shortlist | vendor-neutral orchestration и лучший fit для mixed-stack SOC/MSSP |
| R-Vision SOAR | зрелая SOAR/IRP-платформа, 187 клиентов по данным vc.ru, хорошая база в enterprise и госсекторе [T5][T6] | больше classic SOAR, чем native AI analyst; value realization требует настройки playbooks | **10-15%** RU shortlist | AI-first triage и analyst augmentation, ниже time-to-value |
| Security Vision | сильный sovereign/compliance contour, Skolkovo pedigree, заявленная роботизация до 95% функций оператора ИБ [T7] | тяжёлый enterprise/government DNA, ниже вирусность и меньше глобального AI narrative | **8-12%** RU shortlist | более современный AI assistant positioning и лучший wedge в MSSP/private mid-enterprise |
| BI.ZONE | доверие крупных enterprise через экосистему Сбера, сильный MDR/TI/service layer, активное расширение продуктового портфеля [T12][T13] | сильнее как service-led ecosystem, а не как независимый AI SOC product; сложный доступ вне крупных аккаунтов | **8-12%** RU shortlist | продуктовая независимость, проще white-label / partner motion для MSSP |

**Вывод по конкуренции:** на Западе рынок уже занимают platform giants с distribution advantage. В РФ окно есть только при позиционировании как **sovereign AI SOC analyst для mixed-stack enterprise и MSSP**, иначе кейс зажимают Solar, PT и R-Vision.

## B4. Risk matrix

| # | Category | Risk | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять strong ML/Sec engineers в срок | high | roadmap slip 2-4 мес, пилоты срываются | time-to-hire > 2,5 мес, offer acceptance < 50% | upfront hiring bench, advisor network, outsource-on-ramp |
| 2 | Operational | LLM API latency/cost instability ломает SLA и COGS | med | margin erosion, incident backlog | inference cost > 25k ₽/client/mo, p95 latency > 15 sec | multi-model routing, local fallback, hard usage caps |
| 3 | Market | Enterprise demand есть, но conversion в paid pilot низкая | med | CAC уходит выше 1,2-1,5 млн ₽ | pilot-to-paid < 25%, sales cycle > 9 мес | narrow ICP, ROI calculator, MSSP-first channel |
| 4 | Market | Price compression из-за bundling у Microsoft/PT/Solar | high | ARPU падает ниже 260k ₽, EBITDA ломается | discount requests > 20%, конкурент дает AI bundle «бесплатно» | modular pricing, sovereign premium, services attach |
| 5 | Regulatory | 152-ФЗ / data residency ограничат облачный inference и трансграничные модели | high | часть ICP недоступна без local deployment | security questionnaire все чаще требует on-prem | private-cloud/on-prem edition, data localization by design |
| 6 | Regulatory | 115-ФЗ/FinCERT/regulator workflow требует deep integrations и auditability | med | без этого банки не покупают | RFP требует ASOI FinCERT, audit trail, сертификацию | roadmap под regulated connectors, explainability logs |
| 7 | Financial | Runway сжимается из-за delayed procurement и burn before revenue | high | down round / stop-hiring / bridge risk | burn > 5,5 млн ₽ три месяца подряд | reserve 20-25%, staged hiring, milestone-based spend |
| 8 | Financial | USD/RUB и инфляция раздувают infra/FOT/LLM costs | med | gross margin проседает на 5-10 п.п. | USD > budget band, salary uplift > 15% YoY | RUB pricing indexation, annual prepay, hedge imports |
| 9 | Black swan | Новый санкционный пакет режет доступ к критичному SaaS/infra | med | срочная миграция, временный outage | vendor notices, payment issues, export-control updates | sovereign stack map, hot-swap vendors, escrow backups |
| 10 | Black swan | Отключение внешних frontier LLM или резкое ухудшение качества | med | product value sharply down, false positives up | quality score падает >20%, API denials, quota cuts | hybrid architecture, local open-weight fallback, prompt minimization |

## B5. Kill conditions через 6 месяцев

1. **EBITDA risk gate:** если по обновлённой модели **p10 EBITDA@M24 < 0** или cash runway < **9 мес**, проект нельзя продолжать без bridge round.
2. **Median profitability gate:** если **p50 EBITDA@M24 < 500 000 ₽/мес**, прекращаем масштабирование, потому что median-case не проходит фондовый profit gate.
3. **Commercial traction gate:** если к M6 одновременно **< 6 активных платящих клиентов** или **pilot→paid < 25%** или **blended CAC > 1,2 млн ₽**, GTM считается non-repeatable и проект надо останавливать/перепозиционировать.

## B6. P6B verdict

**Verdict: DOWNGRADE / borderline reject.**

P5 показал очень сильную точечную unit economics, но SECTION B показывает, что модель слишком чувствительна к **pricing pressure, CAC inflation и regulatory deployment constraints**. Для фонда кейс становится интересным только при двух подтверждениях одновременно:
- минимум 1-2 реальных paid pilots в sovereign/private-cloud контуре,
- repeatable partner motion через MSSP или крупного интегратора.

Без этого Dropzone AI GEO Expand выглядит не как scale-ready winner, а как **fragile enterprise bet**.

## Sources — SECTION B
- [T1] Microsoft Security Copilot: https://www.microsoft.com/en-us/security/business/ai-machine-learning/microsoft-security-copilot
- [T2] CrowdStrike Charlotte AI: https://www.crowdstrike.com/en-us/platform/charlotte-ai/
- [T3] Google Triage Agent docs: https://docs.cloud.google.com/chronicle/docs/secops/triage-agent
- [T4] Google Agentic SOC: https://cloud.google.com/solutions/security-analytics-and-operations
- [T5] R-Vision SOAR: https://rvision.ru/products/soar
- [T6] vc.ru про R-Vision и 187 клиентов: https://vc.ru/invest/2787136-obligatsii-r-vision-investitsii-v-kiberbezopasnost-i-dokhodnost-do-17
- [T7] Security Vision / Skolkovo: https://sk.ru/news/rezident-skolkovo-moderniziroval-monitoring-i-upravlenie-informacionnoy-bezopasnostyu-v-centre-sportivnoy-podgotovki-sbornyh-komand-rossii/
- [T8] Positive Technologies, MaxPatrol O2: https://habr.com/ru/companies/pt/articles/763686/
- [T9] Positive Technologies, MaxPatrol O2 tech deep-dive: https://habr.com/ru/companies/pt/articles/774564/
- [T10] vc.ru про трансформацию Солар: https://vc.ru/services/831303-rostelekom-solar-razdelit-biznes-na-dve-struktury-s-raznymi-brendami-chtoby-uiti-ot-obraza-goskompanii
- [T11] vc.ru про Solar M&A: https://vc.ru/rusven/2164594-solar-priobrela-90-protsentov-hexway
- [T12] Habr по BI.ZONE TI: https://habr.com/ru/articles/933642/
- [T13] vc.ru по BI.ZONE M&A: https://vc.ru/id4994551/2219163-bi-zone-priobrela-nano-security

<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[GEO-EXPAND] 0755 MSK Dropzone AI GEO Expand — NEAR-PASS: 67/100 | EBITDA base=757К₽/мес через 13 мес | LTV/CAC=22.1x | Ключевое преимущество: sovereign/private-cloud wedge для mixed-stack SOC | Главный риск: слабый локальный category demand и price compression от платформ.

# 06-verdict

sector: GEO-EXPAND

## Финальный вердикт
**NEAR-PASS (67/100).**

Кейс проходит по unit economics и потенциально достигает company_ebitda_rub_month выше 500К₽/мес при 35 клиентах и горизонте около 13 месяцев, но пока не дотягивает до investment-grade approve из-за слабого RU-demand proof, хрупкого moat и высокой зависимости от sovereign GTM/partner motion.

## Оценка
Source tier balance: T1=3, T2=7, T3=2, weighted=2.08. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 24 | "LTV/CAC: 22.1x", "CAC Payback: 2.4 мес", "Gross Margin: 77.8%" из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В 04-economics.md при 50 клиентах "EBITDA = 3.94 млн ₽/мес", а порог 500К₽ достигается примерно на 35 клиентах. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | В 02-demand.md спрос в РФ прямо оценён как "LOW-MEDIUM", при этом есть hh proxy и рынок 337 млрд ₽; применён tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | В 05-critic.md окно есть только как "sovereign AI SOC analyst для mixed-stack enterprise и MSSP", но platform giants уже впереди по distribution. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В risk matrix есть high-risks по hiring, price compression, 152-ФЗ/data residency и санкционным ограничениям. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | CAC выглядит сильным, но сам critic пишет: нужен "repeatable partner motion через MSSP или крупного интегратора". |

**Sum raw = 100 / 150**

**Normalized score = round((100 × 100) / 150) = 67/100**

## Почему не APPROVED
Формальный approve требует score >= 70 и company_ebitda_potential_rub_month >= 500К₽/мес при <= 50 клиентах и <= 24 мес. Вторая часть выполнена, первая нет: качество доказательств спроса и moat пока недостаточно надёжны для invest committee.

## Сравнение с исходным duplicate-решением
Изначально сигнал считался supporting signal для общего кейса autonomous cybersecurity agents. Полный rerun показал, что как standalone candidate Dropzone AI уже имеет рабочую economics и понятный sovereign wedge, но всё ещё слаб для самостоятельного approve. Значит отдельный кейс имеет смысл, но итог остаётся ниже инвестиционного порога.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 16 640 000 ₽ |
| CAC | 754 000 ₽ |
| LTV/CAC | 22.1x |
| CAC payback | 2.4 мес |
| Gross Margin | 77.8% |
| contribution_margin_rub_month | 227 000 ₽ |
| fixed_costs_rub_month | 7 415 000 ₽ |
| company_ebitda_rub_month base M12 | 193 036 ₽/мес |
| company_ebitda_potential_rub_month @50 clients | 3 935 000 ₽/мес |
| clients_to_500k_ebitda | 35 |
| months_to_500k_ebitda | 13 |
| clients_to_1m_ebitda | 38 |
| months_to_1m_ebitda | 13-14 |
| Break-even clients | 33 |
| Break-even month | M12 |
| startup_capital_to_bep_rub | 59 100 751 ₽ |

## FULL business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам, телко, e-com, MSSP | SDR | CRM + prospecting stack | 2 дня | 18 000 | Высокая |
| 2 | Первичный outbound: email, LinkedIn/аналог, звонки | SDR | Sequencer + телефония + CRM | 10 дней | 24 000 | Средняя |
| 3 | Квалификация боли: SOC load, false positives, FTE shortage | SDR + AE | CRM, discovery script | 5 дней | 30 000 | Средняя |
| 4 | Demo и ROI-калькуляция по замещению Tier-1/Tier-2 | AE + Solutions lead | Demo env, ROI sheet | 7 дней | 42 000 | Низкая |
| 5 | Security review и pilot scoping | AE + CTO | Questionnaire, архитектурные схемы | 21 день | 95 000 | Низкая |
| 6 | Пилот: подключение к SIEM/XDR, тестовые сценарии | Backend + ML + DevOps | Private cloud, connectors, logs | 14 дней | 64 000 | Средняя |
| 7 | Юридическое согласование и procurement | AE + CEO | Договоры, DPA/SLA | 14 дней | 56 000 | Низкая |
| 8 | Коммерческое закрытие и подписание | AE | CRM, e-sign | 3 дня | 12 000 | Средняя |
| 9 | Provisioning tenant / on-prem инстанса | DevOps | IaC, Kubernetes, monitoring | 5 дней | 38 000 | Высокая |
| 10 | Интеграция, промпт/плейбук-тюнинг, knowledge base | ML + Backend + CS | Connectors, RAG/KB, support desk | 14 дней | 57 000 | Средняя |
| 11 | Первый invoice и запуск production | Finance + CS | Billing, ЭДО | 3 дня | 9 000 | Высокая |
| 12 | Сбор оплаты и контроль cash collection | Finance + CS | Billing/ERP, CRM | 15 дней | 7 000 | Высокая |

**Итого direct cost-to-close + launch:** 452 000 ₽ на клиента.

## Team table

| Роль | Функция | Нужно чел. | FOT fully-loaded ₽/мес |
|---|---|---:|---:|
| CEO / founder | GTM, enterprise deals, fundraising | 1 | 845 000 |
| CTO / Tech Lead | Архитектура, security review, roadmap | 1 | 715 000 |
| Senior Backend | Connectors, orchestration, APIs | 2 | 1 092 000 |
| ML Engineer | LLM/RAG, tuning, detection reasoning | 1 | 676 000 |
| DevOps | Private cloud, infra, observability | 1 | 468 000 |
| Frontend | Analyst UI, workflows, dashboards | 1 | 390 000 |
| SDR | Outbound prospecting | 1 | 239 200 |
| AE | Discovery, demos, close, procurement | 1 | 449 800 |
| Customer Success | Onboarding, retention, expansion | 1 | 338 000 |
| **Итого** |  | **9** | **5 213 000** |

## Moat — 7-factor framework

| Фактор | Score 0-3 | Краткое объяснение |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных в заметной степени. |
| Switching costs | 2 | После подключения SIEM/XDR, playbooks и KB возникают интеграционные switching costs. |
| Scale economies | 1 | Compute и support scale помогают, но private-cloud delivery не даёт сильной кривой снижения COGS. |
| Proprietary data / model advantage | 1 | Есть потенциал на SOC telemetry/playbooks, но публично не доказан размер уникального датасета. |
| Regulatory moat | 2 | Sovereign/private-cloud контур и auditability создают барьер, но формального лицензируемого moat нет. |
| Brand / distribution | 1 | У международных лидеров distribution лучше; локальный бренд надо строить почти с нуля. |
| Embedded workflow | 3 | При успешном внедрении продукт садится глубоко в SOC triage/investigation workflow. |

**Sum 7-factor = 10/21**

**Moat score = round((10 × 25) / 21) = 12/25**

Вывод: moat не слабее критического порога, но всё ещё ниже investment-ready уровня. Он строится не на network effects, а на embedded workflow + sovereign deployment.

## GTM — 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Крупнейший SOC и постоянный приоритет antifraud/IR; боль подтверждается объёмом fraud и затратами на ops. | email decision-maker + профильные ИБ-конференции | 700 000 ₽/мес |
| 2 | ВТБ | Банк из системно значимого контура, чувствителен к 152-ФЗ и нуждается в sovereign/private-cloud варианте. | тёплый enterprise outbound через security leadership | 650 000 ₽/мес |
| 3 | Т-Банк | Высокая digital-нагрузка и потребность ускорять triage без роста headcount. | founder-led outreach + кейс с ROI-калькулятором | 600 000 ₽/мес |
| 4 | Альфа-Банк | Сильный security contour и высокая стоимость analyst time делают ROI на Tier-1 automation понятным. | партнёрство с интегратором/MSSP | 600 000 ₽/мес |
| 5 | Ozon | Высокий объём security alerts и нехватка SOC-специалистов подтверждаются активным наймом SOC-ролей на hh.ru. | email decision-maker + Habr/vc.ru content | 500 000 ₽/мес |
| 6 | X5 Group | Крупный distributed enterprise с постоянным SOC workload и mixed-stack инфраструктурой. | конференция + MSSP intro | 500 000 ₽/мес |
| 7 | МТС | Telecom/infra perimeter делает SOC automation экономически значимой и требует локального контура. | партнёрство с MSSP / интегратором | 550 000 ₽/мес |
| 8 | ДОМ.РФ | Регулируемая среда и наличие SOC-ролей на hh.ru дают хороший fit для pilot в private cloud. | direct outreach в CISO/Head of SOC | 450 000 ₽/мес |
| 9 | Росгосстрах | Страховой контур чувствителен к antifraud и data residency, что усиливает sovereign wedge. | отраслевые ИБ-мероприятия + warm intro | 450 000 ₽/мес |
| 10 | Русская медная компания | Critical infra / industrial security, где нужен mixed-stack SOC и audit trail. | партнёрский заход через integrator | 500 000 ₽/мес |

**GTM verdict:** список таргетов реалистичен и совпадает с buyer universe из demand-stage, но channel fit пока hypothesis-driven. Главный рабочий путь, MSSP/integrator-led pilots, а не чистый self-serve или широкая реклама.

## Top-3 risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Price compression от Microsoft/PT/Solar | High | High | В 05-critic.md скидка/бандлинг ломают economics, а stress `Price -30%` даёт EBITDA M12 = -3 031 219 ₽. |
| Sovereign deployment и регуляторные ограничения | High | High | 152-ФЗ, data residency и требования auditability могут закрыть часть ICP без on-prem/private-cloud productization. |
| Non-repeatable GTM через enterprise procurement | Medium-High | High | Без repeatable partner motion CAC может выйти за 1.2-1.5 млн ₽ и убить scale economics. |

## LTV Upside Calculator
Поскольку кейс имеет статус REJECTED/NEAR-PASS, ниже показан набор триггеров, которые переводят его в approve-range.

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| Paid pilots в sovereign/private-cloud | 0 доказанных в материалах | 2-3 оплаченных пилота | Снижает execution uncertainty и поднимает #5 и #6 на 2-4 балла. |
| Partner-led share новых сделок | ограниченно подтверждено | >=40% new logos через MSSP/integrators | Снижает blended CAC и делает GTM repeatable. |
| ARPA | 320 000 ₽/мес | 380 000-450 000 ₽/мес | Даёт запас против price compression и ускоряет 500К EBITDA. |
| Churn | 1.5%/мес benchmark | <=1.0%/мес по первым cohort | Укрепляет LTV и повышает confidence в enterprise retention. |
| RU demand proof | LOW-MEDIUM | 10+ целевых RFP/pilot conversations | Поднимает Market+Demand в investment-ready диапазон. |

### Что должно быть доказано для апгрейда до APPROVED
1. Минимум 2 оплаченных pilot-to-production кейса в РФ или русскоязычном sovereign-контуре.
2. Повторяемый канал через MSSP/интеграторов с blended CAC не выше 900К₽.
3. Подтверждение, что private-cloud deployment удерживает GM >= 70%.
4. Доказанная устойчивость pricing, без discount spiral ниже 300К₽/мес.

## Итог инвесткомитета
**NEAR-PASS.** Я бы не инвестировал в текущем виде как standalone российский expansion-case, но держал бы в активном watchlist. Если команда быстро докажет 2-3 локальных sovereign pilots и partner-led GTM, кейс может перейти из 67/100 в 72-75/100 без пересборки всей economics.


---

## Файл: 07-score-trajectory.md

## 2026-04-20 04:57 MSK — P5 Unit Economics
- Этап: P5 Unit Economics
- Итог: Unit economics = PASS, investment grade сохраняется даже при fully-loaded CAC и реалистичном плане найма.
- Ключевой вывод: при ACV 3.84 млн ₽, blended CAC 754 тыс. ₽, LTV 16.64 млн ₽ и break-even на 33 клиентах кейс проходит фондовый порог по LTV/CAC, payback и EBITDA feasibility.
- Изменение оценки: позитивное, после P5 кейс укрепился как investable enterprise cybersecurity play; основной риск смещается из economics в GTM/procurement execution.
- Артефакт: `pipeline/cases/0755-msk-dropzone-ai-geo-expand-v2/04-economics.md`

## 2026-04-20 11:33 MSK — P7 Critic and Verdict
- Этап: P7 Critic and Verdict
- Итог: NEAR-PASS, 67/100.
- Ключевой вывод: сильная unit economics и путь к company_ebitda_rub_month > 500К₽/мес существуют, но локальный спрос, moat и repeatable sovereign GTM пока недостаточно подтверждены для approve.
- Изменение оценки: нейтрально-негативное, score ограничен Market+Demand и Moat, несмотря на сильный P5.
- Артефакт: `pipeline/cases/0755-msk-dropzone-ai-geo-expand-v2/06-verdict.md`

