# verdict.md — 0827-msk-conveyor-geo-expand-v2

- status: REJECTED
- score: 18/100
- sector: GEO-EXPAND
- date: 2026-04-20
- github_path: business-models/rejected/0827-msk-conveyor-geo-expand-v2/verdict.md
- note: исходный rerun-кейс имеет schema deviation, demand сохранён в `02-demand.md`, файлы `02-validation.md` и `03-demand.md` отсутствуют.


---

# FILE: 00-brief.md

# Краткий бриф

## Что это
Принудительно переоткрытый кейс `0827-msk-conveyor-geo-expand-v2` из backlog resurrect/rerun для новой аналитики по полному пайплайну.

## Почему кейс создан
- Файл `2026-04-19-resurrect-0827-msk-conveyor-geo-expand.md` подпадает под обязательное правило Force Full Pipeline.
- Для resurrect/rerun intake не применяет логику duplicate, а всегда создаёт новый case version.
- Кейс передаётся дальше на P3 demand validation и последующие этапы с новой методологией оценки.

## Что известно на старте
- Sector: `GEO-EXPAND`.
- Оригинальный triage verdict: см. `01-intake.md`.
- Полный исходный контекст сохранён без сокращений.

## Следующий шаг
Перейти к P3-P7 и заново оценить спрос, экономику, moat, риски и финальный verdict.


---

# FILE: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-0827-msk-conveyor-geo-expand.md
created: 2026-04-19T23:24:43+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/triage-2026-04-18-0827-msk-conveyor-geo-expand.md
- Базовый slug: `0827-msk-conveyor-geo-expand`
- Новый slug кейса: `0827-msk-conveyor-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 0827-msk-conveyor-geo-expand

## Meta
- source: triage/triage-2026-04-18-0827-msk-conveyor-geo-expand.md
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
- `pipeline/raw/2026-04-18-0827-msk-conveyor-geo-expand.md`

## Классификация
дубликат ранее обработанного сигнала

## Решение
Новый кейс не открывать и существующие открытые кейсы не обогащать.

## Почему
- Файл подтверждает уже известный сюжет по Conveyor: AI-native автоматизация security questionnaires, trust center и customer trust workflow для enterprise B2B-продаж.
- Подходящего открытого кейса в `pipeline/cases/` для обогащения не найдено.
- Во входном raw-файле `ltv_signal` указан как `1200000-6000000 RUB в год`, то есть примерно `100000-500000 ₽ в месяц` на клиента.
- Standing orders для Program 1 требуют потенциал `> 500000 ₽ в месяц`, а здесь верхняя граница только достигает порога, но не превышает его.
- Сигнал не шумовой, но не даёт новых данных, которые переводят тему в открытый кейс по текущим правилам intake.

## Что сделано
- Новый кейс в `pipeline/cases/` не создавался.
- `01-evidence.md` не обновлялся, так как совпадающего открытого кейса нет.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это supporting signal по уже известной теме Conveyor, но не по существующему открытому кейсу. Сигнал усиливает уверенность в категории customer trust workflow, однако на текущих данных тема всё ещё не проходит фильтр Program 1 по месячному LTV, поэтому новый кейс не открывается.

```


---

# FILE: 02-demand.md

---
stage: demand-validation
case: 0827-msk-conveyor-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: REJECT
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
0827 MSK Conveyor GEO Expand, AI-native customer trust workflow для B2B software vendors: security questionnaires, trust center, RFP/RFX automation и ускорение enterprise security review.

## Итог
**Статус: REJECT**

Глобально категория реальна. У Conveyor есть живой продукт, публичные customer outcomes, официальный pricing и свежий раунд. Это не fake category. Но для локального geo-expand кейса evidence всё ещё слабый: в РФ exact-demand почти отсутствует, buyer universe узкий, а публичный ценовой якорь Conveyor начинается слишком низко для уверенного прохождения нашего profit gate.

Ключевая проблема не в том, что security questionnaire automation никому не нужна. Проблема в том, что локально это выглядит как **узкий слой tooling для зрелых B2B vendors с enterprise sales**, а не как достаточно широкий и дорогой standalone market. На demand-stage этого достаточно, чтобы кейс не пропускать дальше.

## 1. Demand data
Источник exact-check: `http://172.18.0.1:9001/multi-demand?keyword=Conveyor%20security%20questionnaire%20automation`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Дополнительные смежные проверки:

### `trust center automation`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **1**
- Yandex suggest: **2**

### `security questionnaire software`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **2**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `RFP security questionnaire automation`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### Интерпретация
Search-demand в РФ почти нулевой по всем разумным входам. Для узкого B2B security / presales workflow это не автоматический стоп-фактор, но и сильных локальных косвенных сигналов здесь нет. Категория выглядит импортной и очень нишевой.

## 2. Реальные рыночные сигналы и why now
1. На главной странице Conveyor заявляет **95% accurate answers**, **80% less time on tedious tasks**, **3x reduction in questionnaires** и **90% faster turnaround times**. Это сильный category proof того, что painpoint реален и measurable.
2. В customer stories Conveyor показывает заметные результаты у реальных B2B vendors: например, Sprout Social автоматизирует **98%** security questionnaires, Lucid Software тратит на questionnaires на **91% меньше времени**, Temporal сообщает про **$100K+ annually saved**, Alteryx связывает процесс с **over half a billion in security-influenced revenue**.
3. **12 июня 2025 года** Conveyor официально объявила о **$20M Series B** и прямо описала customer trust / security reviews как растущий revenue bottleneck для B2B software.
4. В том же официальном анонсе компания пишет, что среди клиентов есть команды уровня **Atlassian, Zendesk, Qualtrics** и другие enterprise buyers, то есть это не ранний пилотный шум.
5. Продукт в 2025-2026 годах расширился от questionnaire automation в сторону AI agents и trust center automation, что усиливает why-now, но не меняет базовый факт: core buyer по-прежнему ограничен компаниями, которые регулярно проходят customer security review.

### Вывод
Глобальный спрос на категорию подтверждён. Компании действительно платят за ускорение security review и снижение ручной нагрузки. Но этот proof привязан к B2B software vendors с активным enterprise sales motion, а не к широкому горизонтальному рынку.

## 3. Конкурентные и ценностные якоря

| Якорь | Публичный сигнал | Что это доказывает |
|---|---|---|
| Conveyor pricing | Professional starts at **$9,600/year** и включает **20 questionnaire credits**, **100 trust center credits** | категория реально монетизируется, но стартовый чек низкий для нашего фильтра |
| Conveyor official outcomes | 95% accuracy, 80% less time, 90% faster turnaround | value proposition не косметический |
| SafeBase pricing | free foundation + higher tiers by contact | trust center / questionnaire category имеет отдельный бюджетный слой |
| Whistic pricing | кастомный TPRM package с AI copilot и trust center | соседний рынок risk / assessment automation тоже платёжеспособен |
| G2 | у Conveyor **150 reviews** и рейтинг **4.6/5** | продукт уже заметно внедрён, это не pre-PMF история |

### Вывод по конкурентному полю
Конкурентный слой существует и подтверждает реальный budget line. Но публичные данные также показывают, что рынок highly specialized и pricing часто начинается довольно низко для SMB/mid-market use case. Для нашего standalone-case это плохой знак: category real, но ACV ceiling выглядит ограниченным.

## 4. Российский контур и substitutes
Прямого сильного локального аналога Conveyor в открытых сигналах не видно. Возможные substitutes в РФ:
- ручное заполнение security questionnaires силами security/compliance/presales;
- general-purpose LLM + внутренняя база ответов;
- data room / document sharing без полноценной questionnaire automation;
- trust center как часть более широкой compliance / GRC / presales-ops практики;
- аутсорсинг security review response на консультантов или внутренний presales-ops.

### Ключевая проблема локализации
Локальный buyer universe выглядит слишком узким. Нужны компании, которые одновременно:
1. продают сложный B2B продукт,
2. регулярно проходят security review со стороны enterprise клиентов,
3. уже имеют зрелый security/compliance контур,
4. готовы купить отдельный tool, а не закрыть задачу руками или generic AI.

Это делает локализацию возможной, но слабой по масштабу. Для geo-expand кейса такого уровня подтверждения недостаточно.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
- Публичный floor у Conveyor: **$9,600/год** за Professional, то есть меньше **1 млн ₽/год** по порядку величины.
- Для локального кейса беру более оптимистичный средний чек **180 000 ₽/мес** = **2,16 млн ₽/год** на клиента, предполагая enterprise bundle, интеграции и higher-volume usage.
- ICP: зрелые B2B SaaS, fintech, infra, cybersecurity, data/platform vendors с регулярным enterprise security review.

### TAM
Беру **150** потенциально релевантных организаций в РФ и близком русскоязычном контуре.

**TAM = 150 × 2,16 млн ₽ = 324 млн ₽/год**

### SAM
Реально адресуемый digital-mature слой: **35** организаций.

**SAM = 35 × 2,16 млн ₽ = 75,6 млн ₽/год**

### SOM
Ранний реалистичный слой: **5 контрактов**.

**SOM = 5 × 2,16 млн ₽ = 10,8 млн ₽/год**

### Вывод по рынку
Даже при оптимистичном локальном чеке рынок выглядит узким. Главная проблема, что TAM/SAM/SOM не только небольшие, но и зависят от очень специфического buyer profile.

## 6. WTP и доказательства готовности платить
1. **WTP глобально подтверждён**: Conveyor имеет публичный pricing, customer stories, G2 adoption и Series B.
2. SafeBase и Whistic подтверждают, что trust center / assessment automation это отдельная category budget line, а не разовая кастомная услуга.
3. Но публичный ценовой якорь Conveyor слишком мягкий для нашего profitability filter: стартовый пакет находится заметно ниже порога high-LTV operator business.
4. **Локально WTP не подтверждён** на нужной глубине. Нет сильных публичных сигналов, что российские B2B vendors уже массово покупают отдельный security questionnaire automation stack с чеком, достаточным для фонда.

### Вывод по WTP
**Глобально WTP есть, локально и по нашему ACV-фильтру доказательств недостаточно.**

## 7. Profit Gate
Нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Conservative
- Цена: **90 000 ₽/мес**
- GM: **70%**
- Валовая прибыль на клиента: **63 000 ₽/мес**
- Для fixed costs **1,5 млн ₽/мес** нужно **32 клиента**

**Вердикт: FAIL**

### Сценарий B. Base-case
- Цена: **180 000 ₽/мес**
- GM: **75%**
- Валовая прибыль на клиента: **135 000 ₽/мес**
- Нужно **15 клиентов**

**Вердикт: FAIL**

### Сценарий C. Enterprise-heavy
- Цена: **300 000 ₽/мес**
- GM: **78%**
- Валовая прибыль на клиента: **234 000 ₽/мес**
- Нужно **9 клиентов**

**Вердикт: STRETCH**

### Вывод по Profit Gate
Profit gate не собирается убедительно. Чтобы пройти его, нужно либо заметно больше локальных покупателей, либо существенно более высокий ACV, чем подсказывает публичный pricing floor и структура категории.

## 8. Общий вывод
- Search demand в РФ: **LOW**
- Global category proof: **сильный**
- Local category proof: **слабый**
- WTP: **подтверждён глобально, локально недостаточно**
- Localizability: **возможна, но рынок слишком узкий**
- Profit Gate: **не проходит убедительно**

## 9. Решение для пайплайна
**Отклонить на этапе demand validation.**

Причины:
1. глобальная категория реальна, но локальный рынок выглядит слишком нишевым;
2. buyer universe ограничен зрелыми B2B vendors с enterprise security review motion;
3. публичный pricing floor слишком низкий для уверенного high-LTV кейса;
4. profit gate не собирается без слишком смелых допущений по чеку и числу клиентов.

## Market Pulse
Market Pulse 20.04.2026: категория customer trust automation усиливается глобально, но для локального geo-expand evidence всё ещё слабый.

> Market Pulse 2026-04-20: растущий интерес.

> Market Pulse 2026-04-20: растущий интерес.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=Conveyor%20security%20questionnaire%20automation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=trust%20center%20automation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=security%20questionnaire%20software
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=RFP%20security%20questionnaire%20automation
- Conveyor homepage: https://www.conveyor.com/
- Conveyor pricing: https://www.conveyor.com/pricing
- Conveyor customers: https://www.conveyor.com/conveyor-customers
- Conveyor security questionnaire automation: https://www.conveyor.com/platform/security-questionnaire-automation-software
- Conveyor Series B announcement, 2025-06-12: https://www.conveyor.com/blog/series-b
- SafeBase pricing: https://safebase.io/pricing
- Whistic pricing: https://www.whistic.com/pricing
- G2 Conveyor reviews: https://www.g2.com/products/conveyor-conveyor/reviews


---

# FILE: 04-economics.md

---
stage: economics
case: 0827-msk-conveyor-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: FAIL
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
0827 MSK Conveyor GEO Expand, AI-native automation для security questionnaires, trust center и customer trust workflow у B2B software vendors.

## Economics verdict
**Статус: FAIL**

Экономика не складывается для standalone Program 1 кейса. Главная проблема не в том, что продукт нельзя продать вообще, а в том, что локальный ACV слишком низкий относительно тяжёлого enterprise GTM. При реалистичном чеке **180 000 ₽/мес**, fully-loaded CAC около **2,95 млн ₽**, contribution profit **54 000 ₽/клиент/мес** и churn **2,5%/мес** модель даёт **LTV/CAC = 0,73x** и payback **16,4 месяца по MRR**. Даже база в **50 клиентов** не даёт комфортного EBITDA.

## 1. Ключевые допущения
- Публичный floor у Conveyor по состоянию на апрель 2026: **Professional starting at $9,600/year** с 20 questionnaire credits и 100 trust center credits. Это примерно `~61 000 ₽/мес` по floor, то есть локальный high-ACV сценарий нужно отдельно обосновывать.
- Для локального enterprise-lite кейса беру рабочий чек **180 000 ₽/мес**. Это заметно выше floor и уже включает premium за локализацию, внедрение и поддержку.
- Модель продажи: pilot-led enterprise motion, не self-serve.
- Monthly churn: **2,5%**. Для category-specific tool с ограниченным buyer universe и умеренными switching costs это консервативный, но не катастрофический сценарий.

## 2. Business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка B2B vendors | SDR | CRM, ручной ресерч | 0,5 дня | 4 000 | Средняя |
| 2 | Enrichment контактов security/compliance/revops | SDR | CRM, e-mail finder | 0,5 дня | 4 000 | Средняя |
| 3 | Founder-led outbound и follow-up | SDR + founder | e-mail, calls, Telegram | 2-3 недели | 22 000 | Средняя |
| 4 | Discovery call | AE + founder | Meet, CRM | 1 ч + prep | 12 000 | Низкая |
| 5 | Demo questionnaire/trust-center workflow | AE + solutions | demo env, KB | 3-5 дней | 24 000 | Низкая |
| 6 | Pilot scoping и импорт knowledge base | solutions + backend | docs, connectors | 1-2 недели | 46 000 | Средняя |
| 7 | Security/legal/procurement review | founder + legal | DPA, security docs | 2-4 недели | 58 000 | Низкая |
| 8 | Pilot execution и handholding | CSM + analyst | AI workflow, QA | 2-4 недели | 71 000 | Средняя |
| 9 | Contracting и invoicing | AE + ops | договор, ЭДО | 1-2 недели | 8 000 | Средняя |
| 10 | Первый monthly service cycle | CSM + support | dashboard, support stack | 1 месяц | 72 000 | Средняя |

### Вывод
Сделка длинная, ручная и дорогая. Для этой категории именно procurement + pilot, а не лидогенерация, создают основную нагрузку на CAC.

## 3. Revenue model и COGS

### Revenue assumptions
| Компонент | Значение |
|---|---:|
| Разовый pilot/setup fee | 350 000 ₽ |
| Recurring fee | 180 000 ₽/мес |
| ARPA / MRR в модели | 180 000 ₽/мес |

### COGS per client/month
| Компонент | ₽/мес |
|---|---:|
| LLM / workflow runtime | 14 000 |
| Cloud / storage / audit logs | 8 000 |
| CSM delivery | 16 000 |
| Solutions / QA / rework | 18 000 |
| Support / docs / ops | 10 000 |
| Security / compliance overhead | 12 000 |
| Billing / admin variable | 4 000 |
| Vendor reserve | 6 000 |
| **Итого COGS** | **88 000** |

- Revenue per client: **180 000 ₽/мес**
- Gross profit per client: **92 000 ₽/мес**
- **Gross Margin = 51,1%**

## 4. CAC по каналам

| Канал | Spend / мес, ₽ | Воронка | New paying / мес | Raw CAC |
|---|---:|---|---:|---:|
| Founder-led outbound | 820 000 | 220 accounts -> 24 meetings -> 7 pilots -> 0,55 win | 0,55 | 1 490 909 ₽ |
| Content / webinars | 210 000 | 120 MQL -> 10 demos -> 2 pilots -> 0,12 win | 0,12 | 1 750 000 ₽ |
| Partners / referrals | 180 000 | 10 intros -> 4 meetings -> 1 pilot -> 0,08 win | 0,08 | 2 250 000 ₽ |
| **Blended raw** | **1 210 000** |  | **0,75** | **1 613 333 ₽** |

## 5. Fully-loaded CAC

Формула:

`Fully-loaded CAC = (direct spend + sales FOT allocation + tools + events + overhead) / new paying customers`

| Компонент | ₽/мес |
|---|---:|
| Raw acquisition spend | 1 210 000 |
| Sales / founder allocation | 610 000 |
| Tools / CRM / enrichment | 110 000 |
| Events / partner motion | 120 000 |
| Overhead multiplier | 162 000 |
| **Итого acquisition spend** | **2 212 000** |
| New paying customers / мес | **0,75** |
| **Fully-loaded CAC** | **2 949 333 ₽** |

### Sanity check
Полученный CAC не выглядит заниженным. Для узкой enterprise категории он даже ближе к верхней границе tolerable range, что соответствует demand-stage картине: рынок реальный, но buyer universe маленький.

## 6. LTV
- Gross profit per client/month: **92 000 ₽**
- Monthly churn: **2,5%**
- **LTV = 92 000 / 0,025 = 3 680 000 ₽**

## 7. LTV/CAC
- LTV: **3,68 млн ₽**
- Fully-loaded CAC: **2,95 млн ₽**
- **LTV/CAC = 1,25x** по gross profit

### Более строгая contribution-версия
Если вычесть переменные non-COGS затраты на клиентское ведение и sales commission ещё **38 000 ₽/мес**, то:
- Contribution profit = **54 000 ₽/мес**
- Contribution LTV = `54 000 / 0,025 = 2 160 000 ₽`
- **Contribution LTV/CAC = 0,73x**

Для фонда значима именно эта более строгая версия. По ней кейс не проходит.

## 8. CAC Payback
- По пользовательской формуле: **2 949 333 / 180 000 = 16,4 месяца**
- По contribution profit: **2 949 333 / 54 000 = 54,6 месяца**

### Вывод
Даже MRR-payback находится на грани enterprise-допуска, а contribution-payback полностью неприемлем.

## 9. Team и salary realism

| Роль | Нужно чел. | Salary gross ₽/мес | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|
| Founder / CEO | 1 | 550 000 | 165 000 | 715 000 |
| CTO / Tech Lead | 1 | 480 000 | 144 000 | 624 000 |
| Senior Backend | 1 | 350 000 | 105 000 | 455 000 |
| ML / AI Engineer | 1 | 380 000 | 114 000 | 494 000 |
| Solutions / Analyst | 1 | 220 000 | 66 000 | 286 000 |
| SDR | 1 | 160 000 | 48 000 | 208 000 |
| AE | 1 | 250 000 | 75 000 | 325 000 |
| Customer Success | 1 | 200 000 | 60 000 | 260 000 |
| Ops / Finance | 0,5 | 120 000 | 36 000 | 156 000 |
| **Итого** |  |  |  | **3 523 000 ₽/мес** |

HH-поиск по Москве на 20 апреля 2026 подтверждает, что senior backend и enterprise account roles уже живут в диапазонах, близких к этим ставкам или выше, поэтому модель не выглядит искусственно дешёвой.

## 10. Fixed costs

| Статья | ₽/мес |
|---|---:|
| Team FOT вне client-level COGS | 3 523 000 |
| Shared infra / observability | 180 000 |
| Legal / security baseline | 120 000 |
| Office / admin / misc | 110 000 |
| **Итого fixed costs** | **3 933 000 ₽/мес** |

## 11. Break-even
- Contribution profit на клиента: **54 000 ₽/мес**
- Fixed costs: **3 933 000 ₽/мес**
- **Break-even = 72,8 клиента**, округлённо **73 клиента**

### Проверка 50 клиентов
- Contribution profit: `50 × 54 000 = 2 700 000 ₽/мес`
- EBITDA: `2 700 000 - 3 933 000 = -1 233 000 ₽/мес`

Даже при **50 клиентах** EBITDA остаётся отрицательной. Это жёсткий fail по program economics.

## 12. Burn и runway
Даже при аккуратном найме и медленном GTM модель потребует существенный burn до масштаба, который сам по себе выглядит малореалистичным для настолько узкого buyer universe. Проблема не только в капитале, а в том, что рынок вряд ли даст нужные 70+ клиентов без ухода в более широкий adjacent category.

## 13. Итоговый вывод
Что подтверждено:
1. Категория реальна, продукт можно продавать.
2. Есть measurable value, customer outcomes и глобальный category proof.
3. Небольшой локальный бизнес на этой теме теоретически возможен.

Что не проходит:
1. Публичный pricing floor слишком низкий относительно Program 1 economics.
2. Fully-loaded CAC слишком тяжёлый для такого ACV.
3. Contribution LTV/CAC < 1x.
4. Break-even требует ~73 клиента.
5. При 50 клиентах EBITDA всё ещё отрицательная.

**Решение: FAIL на этапе economics.** Кейс полезен как supporting signal для broader trust/compliance workflow, но не тянет standalone investable wedge в текущем виде.

## Источники
- Demand-stage file: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0827-msk-conveyor-geo-expand-v2/02-demand.md`
- Conveyor pricing: https://www.conveyor.com/pricing
- HH.ru senior backend engineer, Москва: https://hh.ru/vacancies/senior-backend-engineer
- HH.ru account executive, Москва: https://hh.ru/vacancies/account_executive


---

# FILE: 05-critic.md

# SECTION A. PnL 12 месяцев

## A1. Принятые допущения

- ARPA / MRR на клиента: **180 000 ₽/мес**.
- COGS на клиента: **88 000 ₽/мес**.
- Gross profit на клиента: **92 000 ₽/мес**.
- Contribution profit на клиента: **54 000 ₽/мес**.
- GM%: **51,1%**.
- Fixed costs: **3 933 000 ₽/мес**.
- Team FOT fully-loaded: **3 523 000 ₽/мес**.
- Страховые взносы: **~30% к ФОТ**, уже включены в FOT и fixed costs.
- CAC по каналам из 04-economics:
  - Founder-led outbound: **1 490 909 ₽** raw CAC
  - Content / webinars: **1 750 000 ₽** raw CAC
  - Partners / referrals: **2 250 000 ₽** raw CAC
  - Blended fully-loaded CAC: **2 949 333 ₽**
- Churn base: **2,5%/мес**.
- Break-even по EBITDA: **73 клиента**.
- Break-even после налога:
  - **УСН 6%: 92 клиента**
  - **IT-льгота 3%: 81 клиент**
  - **ОСНО 20%: 73 клиента** на уровне операционной прибыли, без учёта cash drag от НДС.

Сценарные допущения для PnL, так как в 04-economics нет помесячного new-logo ramp:
- **Base**: churn **2,5%**, new clients по месяцам = **0,0,0,1,1,1,1,1,1,1,1,1**.
- **Optimistic**: churn **1,5%**, new clients по месяцам = **0,0,1,1,1,1,2,2,2,2,2,2**.
- **Pessimistic**: churn **3,5%**, new clients по месяцам = **0,0,0,0,0,1,1,1,1,1,1,1**.
- Формула active clients: `Clients_t = Clients_(t-1) × (1 - churn) + New clients_t`.

## A2. Сценарий: Base

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,98 | 2,93 | 3,85 | 4,76 | 5,64 | 6,50 | 7,33 | 8,15 |
| MRR, ₽ | 0 | 0 | 0 | 180 000 | 355 500 | 526 612 | 693 447 | 856 111 | 1 014 708 | 1 169 341 | 1 320 107 | 1 467 104 |
| COGS, ₽ | 0 | 0 | 0 | 88 000 | 173 800 | 257 455 | 339 019 | 418 543 | 496 080 | 571 678 | 645 386 | 717 251 |
| Gross profit, ₽ | 0 | 0 | 0 | 92 000 | 181 700 | 269 158 | 354 429 | 437 568 | 518 629 | 597 663 | 674 721 | 749 853 |
| GM% | 0,0% | 0,0% | 0,0% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% |
| Fixed costs, ₽ | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 |
| EBITDA, ₽ | -3 933 000 | -3 933 000 | -3 933 000 | -3 879 000 | -3 826 350 | -3 775 016 | -3 724 966 | -3 676 167 | -3 628 588 | -3 582 198 | -3 536 968 | -3 492 869 |
| Cash burn, ₽ | 3 933 000 | 3 933 000 | 3 933 000 | 3 879 000 | 3 826 350 | 3 775 016 | 3 724 966 | 3 676 167 | 3 628 588 | 3 582 198 | 3 536 968 | 3 492 869 |
| Cumulative cash, ₽ | -3 933 000 | -7 866 000 | -11 799 000 | -15 678 000 | -19 504 350 | -23 279 366 | -27 004 332 | -30 680 499 | -34 309 086 | -37 891 284 | -41 428 252 | -44 921 121 |

- Break-even по client count: **73 клиента по EBITDA**, **92 клиента по net на УСН 6%**, **81 клиент по net при IT-льготе 3%**.
- Break-even по месяцам: **не достигается**. При сохранении такого темпа новый steady-state не выводит модель к 73 клиентам даже на длинном горизонте.
- `startup_capital_to_bep_rub`: **44 921 121 ₽** на горизонте M1-M12; до BEP в принципе не доходит.

## A3. Сценарий: Optimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0,00 | 0,00 | 1,00 | 1,98 | 2,96 | 3,91 | 5,85 | 7,76 | 9,65 | 11,50 | 13,33 | 15,13 |
| MRR, ₽ | 0 | 0 | 180 000 | 357 300 | 531 940 | 703 961 | 1 053 402 | 1 397 601 | 1 736 637 | 2 070 587 | 2 399 529 | 2 723 536 |
| COGS, ₽ | 0 | 0 | 88 000 | 174 680 | 260 060 | 344 159 | 514 997 | 683 272 | 849 023 | 1 012 287 | 1 173 103 | 1 331 506 |
| Gross profit, ₽ | 0 | 0 | 92 000 | 182 620 | 271 881 | 359 802 | 538 405 | 714 329 | 887 614 | 1 058 300 | 1 226 426 | 1 392 029 |
| GM% | 0,0% | 0,0% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% |
| Fixed costs, ₽ | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 |
| EBITDA, ₽ | -3 933 000 | -3 933 000 | -3 879 000 | -3 825 810 | -3 773 418 | -3 721 812 | -3 616 979 | -3 513 720 | -3 412 009 | -3 311 824 | -3 213 141 | -3 115 939 |
| Cash burn, ₽ | 3 933 000 | 3 933 000 | 3 879 000 | 3 825 810 | 3 773 418 | 3 721 812 | 3 616 979 | 3 513 720 | 3 412 009 | 3 311 824 | 3 213 141 | 3 115 939 |
| Cumulative cash, ₽ | -3 933 000 | -7 866 000 | -11 745 000 | -15 570 810 | -19 344 228 | -23 066 039 | -26 683 019 | -30 196 739 | -33 608 747 | -36 920 571 | -40 133 713 | -43 249 652 |

- Break-even по client count: **73 клиента по EBITDA**, **92 клиента по net на УСН 6%**, **81 клиент по net при IT-льготе 3%**.
- Break-even по месяцам: **около M57** при продолжении темпа после M12, то есть сильно позже фондового горизонта.
- `startup_capital_to_bep_rub`: **43 249 652 ₽** на горизонте M1-M12.

## A4. Сценарий: Pessimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,96 | 2,90 | 3,79 | 4,66 | 5,50 | 6,31 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 180 000 | 353 700 | 521 320 | 683 074 | 839 167 | 989 796 | 1 135 153 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 88 000 | 172 920 | 254 868 | 333 947 | 410 259 | 483 900 | 554 964 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 92 000 | 180 780 | 266 453 | 349 127 | 428 907 | 505 896 | 580 189 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% | 51,1% |
| Fixed costs, ₽ | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 |
| EBITDA, ₽ | -3 933 000 | -3 933 000 | -3 933 000 | -3 933 000 | -3 933 000 | -3 879 000 | -3 826 890 | -3 776 604 | -3 728 078 | -3 681 250 | -3 636 061 | -3 592 454 |
| Cash burn, ₽ | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 933 000 | 3 879 000 | 3 826 890 | 3 776 604 | 3 728 078 | 3 681 250 | 3 636 061 | 3 592 454 |
| Cumulative cash, ₽ | -3 933 000 | -7 866 000 | -11 799 000 | -15 732 000 | -19 665 000 | -23 544 000 | -27 370 890 | -31 147 494 | -34 875 572 | -38 556 822 | -42 192 883 | -45 785 337 |

- Break-even по client count: **73 клиента по EBITDA**, **92 клиента по net на УСН 6%**, **81 клиент по net при IT-льготе 3%**.
- Break-even по месяцам: **не достигается**; при таком churn и темпе продаж модель не выходит на BEP на разумном горизонте.
- `startup_capital_to_bep_rub`: **45 785 337 ₽** на горизонте M1-M12.

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### На 1 клиенте / месяц

| Шаг waterfall | ₽ / клиент / месяц | Комментарий |
|---|---:|---|
| ARPA | 180 000 | recurring выручка |
| Gross | 92 000 | после COGS 88 000 ₽ |
| Contribution | 54 000 | после доп. client-facing variable затрат 38 000 ₽ |
| EBITDA | -19 | на break-even scale 73 клиента EBITDA около нуля |
| Net, УСН 6% | -10 819 | налог 10 800 ₽ с выручки |
| Net, IT-льгота 3% | -5 419 | налог 5 400 ₽ с выручки |
| Net, ОСНО 20% | -19 | налог на прибыль только при плюсе, но НДС 20% ухудшает cash flow |

### На масштабе 50 клиентов / месяц

| Шаг waterfall | ₽ / месяц |
|---|---:|
| ARPA / Revenue | 9 000 000 |
| Gross | 4 600 000 |
| Contribution | 2 700 000 |
| EBITDA | -1 233 000 |
| Net, УСН 6% | -1 773 000 |
| Net, IT-льгота 3% | -1 503 000 |
| Net, ОСНО 20% | -1 233 000 |

## A6. Cash flow и налоговая модель РФ

- **startup_capital_to_bep_rub**:
  - Base: **44 921 121 ₽** на горизонте M1-M12
  - Optimistic: **43 249 652 ₽** на горизонте M1-M12
  - Pessimistic: **45 785 337 ₽** на горизонте M1-M12
- **УСН 6%**: простой режим, но налог с выручки особенно болезнен при слабом contribution, как в этом кейсе.
- **IT-льгота 3%**: лучший режим, если есть аккредитация Минцифры и компания соответствует критериям, но даже он не спасает economics standalone-кейса.
- **ОСНО 20%**: налог на прибыль выглядит нейтральнее при убытке, но **НДС 20%** ухудшает оборотку и cash conversion, если нет достаточного входящего VAT credit.
- **Страховые взносы ~30% к ФОТ** уже включены в FOT / fixed costs и повторно не добавляются.

## A7. Break-even summary

| Scenario | Break-even client count | Break-even month | Комментарий |
|---|---:|---:|---|
| Base | 73 | n/a | текущий steady-state не выводит модель к BEP |
| Optimistic | 73 | 57 | слишком поздно для investable standalone motion |
| Pessimistic | 73 | n/a | BEP не достигается на разумном горизонте |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

База для расчёта: M12 из SECTION A, где active clients = **8,15**, contribution profit = **54 000 ₽/клиент/мес**, EBITDA = **-3 492 869 ₽**.

### Формулы
- **Sens1, CAC x2**: считаю дополнительный acquisition burden как ещё **+2 949 333 ₽** на каждого нового paying-logo в месяце; при base-ramp это ухудшает cash burn, но даже без него модель уже глубоко ниже нуля.
- **Sens2, Churn x2**: monthly churn растёт с **2,5%** до **5,0%**, new-logo ramp оставляю как в базе P6A.
- **Sens3, Price -30%**: ARPA падает с **180 000 ₽** до **126 000 ₽**, COGS и extra servicing считаю неизменными на коротком горизонте.

| Сценарий | Ключевое изменение | Active clients @M12 | Contribution / client, ₽/мес | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без изменений | 8,15 | 54 000 | -3 492 869 | база уже structurally uninvestable |
| Sens1 | CAC x2 | 8,15 | 54 000 | -6 442 202 | дорогой enterprise GTM делает burn ещё хуже |
| Sens2 | Churn x2 | 6,80 | 54 000 | -3 565 891 | даже умеренное ухудшение retention усиливает провал |
| Sens3 | Price -30% | 8,15 | 0 | -3 933 000 | pricing floor фактически обнуляет contribution |

### Вывод по чувствительности
1. Кейс ломается уже в base-case, поэтому stress-тесты не меняют verdict, а лишь показывают глубину downside.
2. Главная хрупкость, это **price compression**: при снижении цены на 30% short-term contribution исчезает.
3. **CAC inflation** здесь особенно опасен, потому что buyer universe маленький, а sales cycle длинный и ручной.

## B2. Monte Carlo Lite — Confidence Intervals

Ниже использую lite-подход вместо полного 1000-run simulation: **9 комбинаций** по triangular inputs. p10 = downside envelope, p50 = mode-case, p90 = upside envelope.

### B2.1. Triangular inputs

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 2 300 000 | 2 949 333 | 4 200 000 | 04-economics, blended fully-loaded CAC |
| Monthly churn, % | 2,0% | 2,5% | 5,0% | 04-economics + downside inference |
| ARPA, ₽/мес | 126 000 | 180 000 | 300 000 | 02-demand profit-gate scenarios |
| Conversion rate lead→paid, % | 0,20% | 0,34% | 0,55% | inference из 04-economics channel table |
| Time-to-hire, мес | 1,5 | 2,0 | 3,0 | 04-economics, hiring realism |

### B2.2. Метод упрощённой симуляции
- За базу беру ramp M1–M12 из SECTION A.
- Для M13–M24 использую тот же narrow-market контур: downside **0,5** нового клиента/мес, median **1,0**, upside **1,5**.
- EBITDA @M24 считаю как `Active clients × contribution profit per client - fixed costs`.
- LTV/CAC считаю по contribution profit, потому что именно он критичен для фонда в этом кейсе.
- Cash runway интерпретирую от буфера **45 млн ₽** порядка величины, который требуется только для дожития до late-stage ramp в P6A.

### B2.3. 9-combo interpretation -> percentile view

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -4 050 000 | -3 080 000 | -1 180 000 | 2 870 000 |
| CAC payback, мес | n/a | 32,8 | 17,9 | n/a |
| LTV/CAC | 0,0x | 0,73x | 2,03x | 2,03x |
| Cash runway, мес | 10 | 12 | 16 | 6 |

### B2.4. Интерпретация правил
1. **p10 EBITDA < 0** и **p50 EBITDA < 0** → кейс проваливает downside и median-case одновременно.
2. **p50 EBITDA > 500K ₽/мес** не выполняется, значит median-case gate не пройден.
3. Даже **p90** не показывает комфортный upside: модель остаётся below attractive fund-grade return profile.
4. Для этого кейса неопределённость уже не главный риск. Главный вывод проще: **даже mode-case слишком слабый**.

### B2.5. Вывод
Monte Carlo Lite не спасает кейс и не даёт основания для re-open. Это не "широкое распределение с шансом на большой выигрыш", а в первую очередь **слабая базовая экономика с ограниченным upside**.

## B3. Competitor deep-dive

### B3.1. Топ-3 западных конкурента

> Оценки доли рынка ниже, это **инференс** по adjacent сегменту customer trust / TPRM / security questionnaire automation, а не официальные market-share disclosure.

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| SafeBase | trust center, security review sharing, vendor trust workflow | сильный бренд категории, buyer education, self-serve trust center motion | pricing часто начинается с comparatively low entry tier, risk of commoditization | **15–20% adjacent trust-center layer** (инференс) | можно локализовать контент, workflow и поддержку под РФ enterprise контур |
| Whistic | TPRM, assessments, AI-assisted vendor reviews | широкий workflow, AI-позиционирование, network effects вокруг assessments | сильнее в buyer-side TPRM, чем в узком presales workflow; enterprise-heavy selling motion | **20–25% adjacent TPRM / assessment layer** (инференс) | локальный фокус на seller-side response workflow и faster deployment |
| Conveyor | closest direct benchmark по questionnaire automation | сильный category proof, customer outcomes, живой product expansion | публичный pricing floor низкий, buyer universe узкий, category boundary ограничена | **10–15% direct category** (инференс) | локальная интеграция, русскоязычная KB и поддержка, если вообще есть достаточный рынок |

### B3.2. Топ-4 российских конкурента / substitute-set

> В РФ прямых аналогов почти не видно, поэтому ниже в основном **substitute-set**, через который buyer решает ту же задачу без отдельного Conveyor-like продукта.

| Конкурент | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Naumen Service Desk / ITSM | [T1], [T2] | сильный enterprise brand, локальный compliance-контур, много внедрений | не специализирован под security questionnaires, тяжёлый внедренческий слой | **8–12% РФ enterprise ITSM** (инференс) | можно продавать как overlay для presales / security review, не меняя core ITSM |
| Usedesk | [T3] | быстрый helpdesk-style rollout, автоматизация ответов, доступный SMB-mid motion | слабее в enterprise security review и knowledge governance | **3–5% adjacent support stack** (инференс) | более глубокий security/compliance-specific workflow |
| Консалтинг / ручной presales-ops | локальный substitute | нулевой vendor lock-in, решается текущей командой | плохо масштабируется, высокий manual burden, slow turnaround | **крупнейший substitute** | AI-автоматизация и структурированная база ответов |
| General-purpose LLM + внутренний knowledge base | локальный substitute | дешёвый вход, low-friction adoption, уже доступен многим компаниям | слабый audit trail, governance gaps, нет полноценного trust-center workflow | **растущий substitute layer** | domain workflow, templates, permissions, governance |

### B3.3. Вывод по конкурентам
1. На Западе категория доказана, но это **узкий software layer**, а не широкий horizontal category.
2. В РФ biggest threat, это не прямой local champion, а дешёвые substitutes: ручной труд, generic LLM и existing helpdesk / ITSM stack.
3. Это дополнительно давит на pricing power и ухудшает шанс построить standalone high-LTV business.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | AI-ответы по security questionnaire дают ошибки или hallucinations | med-high | высокий, репутационный ущерб и legal friction | override rate > 20%, redlines от security teams | human-in-the-loop, approval workflow, answer provenance |
| Operational | Импорт и поддержание knowledge base клиента слишком ручные | high | высокий, margin erosion | onboarding > 3 недель, много ручного rework | connectors, scoped rollout, paid implementation |
| Market | Buyer universe в РФ слишком мал для repeatable GTM | high | очень высокий | <1 новый логотип/мес даже после нескольких кварталов | расширять wedge в adjacent compliance ops или stop |
| Market | Price compression из-за substitutes и low pricing floor у западных peers | high | очень высокий | win-rate держится только через скидки >20% | ROI-led packaging, premium services, enterprise-only ICP |
| Market | Категория закрывается generic LLM + internal KB без отдельного vendor | high | высокий | частые отказы с формулировкой "сделаем сами" | делать ставку на governance / audit / integrations |
| Regulatory | 152-ФЗ и data residency усложняют хранение security docs | med | высокий | security review fail, требования on-prem | RU-hosted deployment, masking, strict access control |
| Financial | Long sales cycle + высокий CAC быстро сжигают капитал | high | очень высокий | runway < 9 месяцев, pilots не конвертятся | freeze hiring, reduce burn, stop standalone build |
| Financial | Валютная зависимость LLM / infra ухудшает и без того слабый GM | med | средний-высокий | GM < 45%, рост cloud/API bill > 20% | repricing clauses, multi-vendor infra |
| Black swan | Крупные платформы добавляют bundled questionnaire automation | med | высокий | новые AI-features у incumbents, price bundling | либо узкая vertical specialization, либо exit / reposition |

## B5. Kill conditions через 6 месяцев

1. **Demand failure:** если через 6 месяцев pipeline не даёт реалистичный путь хотя бы к **10 активным клиентам в ближайшие 12 месяцев**, standalone motion надо останавливать.
2. **Economics failure:** если contribution LTV/CAC остаётся **< 1,5x** или blended CAC держится **> 2,5 млн ₽**, кейс не подлежит дальнейшему фондуемому развитию.
3. **Pricing failure:** если средний реализованный чек не поднимается хотя бы до **>= 250 000 ₽/мес** без тяжёлых скидок, модель не сможет компенсировать fixed cost base.

## B6. Финальный вывод SECTION B

После risk-layer кейс выглядит ещё слабее, чем после P6A. Здесь нет скрытого upside, который оправдывал бы дальнейший standalone push. Комбинация узкого buyer universe, слабого local demand, низкого pricing floor у бенчмарков и тяжёлого enterprise CAC означает, что **REJECT нужно сохранять без смягчения**.

Практический смысл кейса остаётся только как supporting signal для более широкой темы:
- customer trust automation,
- TPRM / vendor assessment workflows,
- AI-governed compliance knowledge systems.

Но как отдельный geo-expand operator business в РФ этот кейс **не проходит**.

## Источники SECTION B
- T1. Naumen Service Desk: https://www.naumen.ru/products/service_desk/
- T2. Naumen, продуктовые тезисы и описание ITSM-внедрений: https://www.naumen.ru/products/service_desk/
- T3. Usedesk homepage / automation outcomes: https://usedesk.com/
- T4. Whistic homepage: https://www.whistic.com/
- T5. SafeBase pricing: https://safebase.io/pricing
- T6. Conveyor pricing: https://www.conveyor.com/pricing
- T7. Conveyor customers: https://www.conveyor.com/conveyor-customers
- T8. Conveyor Series B announcement: https://www.conveyor.com/blog/series-b
- T9. Demand-stage evidence: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0827-msk-conveyor-geo-expand-v2/02-demand.md`
- T10. Economics-stage evidence: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0827-msk-conveyor-geo-expand-v2/04-economics.md`

<!-- P6B-DONE -->


---

# FILE: 06-verdict.md

[GEO-EXPAND] 0827 MSK Conveyor GEO Expand v2 — REJECTED: 18/100 | EBITDA base=-3493К₽/мес через 12 мес | LTV/CAC=0,73x | Ключевое преимущество: подтверждённая глобальная category pain вокруг security questionnaires | Главный риск: локальный рынок слишком узкий и не окупает enterprise CAC.

# 06-verdict

sector: GEO-EXPAND

## Финальный статус
- Verdict: **REJECTED**
- Normalized score: **18/100**
- Raw score: **27/150**
- Threshold outcome: **<65 = REJECTED**
- Committee note: кейс подтверждает реальность глобальной категории, но не проходит фондовый порог по локальному спросу, EBITDA-потенциалу и capital efficiency.

## Важное замечание по структуре кейса
В кейсе отсутствуют файлы `02-validation.md` и `03-demand.md`; вместо этого demand-аналитика сохранена в `02-demand.md`. Для P7 использована фактическая evidence-база из имеющихся файлов. Из-за отсутствия строки `Sources:` в demand-файле применён дефолтный tier penalty.

## Investment committee one-liner
[GEO-EXPAND] 0827 MSK Conveyor GEO Expand v2 — REJECTED: 18/100 | EBITDA base=-3493К₽/мес через 12 мес | LTV/CAC=0,73x | Ключевое преимущество: подтверждённая глобальная category pain вокруг security questionnaires | Главный риск: локальный рынок слишком узкий и не окупает enterprise CAC.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 4 | «Contribution LTV/CAC = 0,73x» и «payback 54,6 месяца» в 04-economics прямо ниже investment-grade. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 1 | В 05-critic base M12 EBITDA = `-3 492 869 ₽`, optimistic BEP только около `M57`, то есть порог ≤24 мес не достигается. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 5 | В 02-demand: «Search-demand в РФ почти нулевой», `hh.ru vacancies: 0`, TAM всего `324 млн ₽/год`; применён дефолтный penalty -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 6 | Глобальная value есть, но в РФ dominant substitute-set это «ручной труд, generic LLM и existing helpdesk / ITSM stack», поэтому moat weak. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 6 | 05-critic фиксирует `high` риски по buyer universe, price compression, long sales cycle и data residency. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 5 | GTM адресует релевантный ICP, но `Fully-loaded CAC = 2 949 333 ₽` и `0,75 new paying / мес` делают motion нереалистичным. |

**Normalized score = round((27 × 100) / 150) = 18/100.**

## Moat — 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не усиливает продукт для остальных в локальном standalone motion. |
| Switching costs | 1 | Есть KB и шаблоны ответов, но их можно перенести в general-purpose LLM/internal KB. |
| Scale economies | 0 | COGS и human-in-the-loop остаются высокими, scale economics слабы. |
| Proprietary data / model advantage | 1 | Есть потенциальная база ответов клиента, но нет доказанной data moat или крупного локального датасета. |
| Regulatory moat | 0 | Регуляторный барьер не подтверждён T1-источниками и не создаёт защищённого преимущества. |
| Brand / distribution | 1 | У Conveyor есть глобальный category proof, но в РФ бренд и дистрибуция почти отсутствуют. |
| Embedded workflow | 2 | При внедрении продукт встраивается в presales/security review workflow, но глубина ограничена узким use case. |

**Moat score = round((5 × 25) / 21) = 6/25.**

Вывод: **weak moat (<10)**, поэтому риск слабой защищённости вынесен в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 2 160 000 ₽ (contribution) / 3 680 000 ₽ (gross) |
| Fully-loaded CAC | 2 949 333 ₽ |
| LTV/CAC | 0,73x contribution / 1,25x gross |
| CAC Payback | 16,4 мес по MRR / 54,6 мес по contribution |
| Gross Margin | 51,1% |
| contribution_margin_rub_month | 54 000 ₽ / клиент / мес |
| company_ebitda_rub_month базовый | -3 492 869 ₽ в M12 |
| company_ebitda_potential_rub_month | -1 233 000 ₽/мес даже на 50 клиентах |
| clients_to_500k_ebitda | 83 |
| months_to_500k_ebitda | не достигается на горизонте ≤24 мес |
| Break-even | 73 клиента на EBITDA 0 |
| startup_capital_to_bep_rub | 44 921 121 ₽ (base) |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка B2B vendors | SDR | CRM, ручной ресерч | 0,5 дня | 4 000 | Средняя |
| 2 | Enrichment контактов security/compliance/revops | SDR | CRM, e-mail finder | 0,5 дня | 4 000 | Средняя |
| 3 | Founder-led outbound и follow-up | SDR + founder | e-mail, calls, Telegram | 2-3 недели | 22 000 | Средняя |
| 4 | Discovery call | AE + founder | Meet, CRM | 1 ч + prep | 12 000 | Низкая |
| 5 | Demo questionnaire/trust-center workflow | AE + solutions | demo env, KB | 3-5 дней | 24 000 | Низкая |
| 6 | Pilot scoping и импорт knowledge base | solutions + backend | docs, connectors | 1-2 недели | 46 000 | Средняя |
| 7 | Security/legal/procurement review | founder + legal | DPA, security docs | 2-4 недели | 58 000 | Низкая |
| 8 | Pilot execution и handholding | CSM + analyst | AI workflow, QA | 2-4 недели | 71 000 | Средняя |
| 9 | Contracting и invoicing | AE + ops | договор, ЭДО | 1-2 недели | 8 000 | Средняя |
| 10 | Первый monthly service cycle | CSM + support | dashboard, support stack | 1 месяц | 72 000 | Средняя |

## Команда и salary realism

| Роль | Нужно чел. | Salary gross ₽/мес | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|
| Founder / CEO | 1 | 550 000 | 165 000 | 715 000 |
| CTO / Tech Lead | 1 | 480 000 | 144 000 | 624 000 |
| Senior Backend | 1 | 350 000 | 105 000 | 455 000 |
| ML / AI Engineer | 1 | 380 000 | 114 000 | 494 000 |
| Solutions / Analyst | 1 | 220 000 | 66 000 | 286 000 |
| SDR | 1 | 160 000 | 48 000 | 208 000 |
| AE | 1 | 250 000 | 75 000 | 325 000 |
| Customer Success | 1 | 200 000 | 60 000 | 260 000 |
| Ops / Finance | 0,5 | 120 000 | 36 000 | 156 000 |
| **Итого** |  |  |  | **3 523 000 ₽/мес** |

## GTM — 10 named targets

| # | Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Контур | Большой B2B SaaS/документооборот, регулярно проходит enterprise security review и работает с чувствительными данными. | email decision-maker (CISO / presales ops) | 180 000 ₽/мес |
| 2 | Selectel | Облачный провайдер с enterprise-продажами, где security questionnaires и trust center логично встроены в deal cycle. | партнёрство + конференция по cloud/security | 220 000 ₽/мес |
| 3 | Yandex Cloud | Инфраструктурный vendor с большим объёмом security due diligence от enterprise-заказчиков. | тёплый интро через integrator / конференция | 300 000 ₽/мес |
| 4 | VK Tech | B2B platform stack и cloud/enterprise продукты, где buyer trust workflow является частью sales motion. | email decision-maker + отраслевое мероприятие | 220 000 ₽/мес |
| 5 | SberCloud | Enterprise cloud и AI-сервисы, высокий шанс повторяющихся security questionnaires. | партнёрство с интегратором / direct outreach | 250 000 ₽/мес |
| 6 | Arenadata | Data platform vendor для enterprise, где security review часто блокирует сделки. | founder-led outbound в revops/security | 180 000 ₽/мес |
| 7 | Naumen | Enterprise software vendor с тяжёлым B2B sales cycle и требованиями к trust center материалам. | email VP Sales / CISO | 180 000 ₽/мес |
| 8 | Mindbox | B2B SaaS с enterprise-клиентами и повышенными требованиями к data security. | vc.ru ad + точечный outbound | 170 000 ₽/мес |
| 9 | МойСклад | SaaS для SMB/enterprise, где automation security answers может снизить нагрузку на presales/support. | email decision-maker / webinar | 150 000 ₽/мес |
| 10 | Solar | Cybersecurity vendor, которому нужны быстрые ответы на анкеты клиентов и единая knowledge base. | конференция + direct outreach | 240 000 ₽/мес |

Вывод по GTM: target list релевантен, но сам motion остаётся слишком дорогим и медленным. Даже при удачном попадании в named accounts payback не становится инвестиционно комфортным.

## Top-3 Risks

| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| Локальный buyer universe слишком мал | high | very high | 02-demand даёт TAM `324 млн ₽/год`, SAM `75,6 млн ₽/год`, а base-case не собирает достаточное число клиентов. |
| weak moat + substitutes | high | high | 05-critic прямо указывает на давление со стороны ручного труда, generic LLM и existing helpdesk / ITSM stack. |
| evidence_quality_unverified | high | medium-high | В demand-файле нет строки `Sources: T1/T2/T3`, поэтому quality tier не подтверждён и criterion #3 автоматически штрафуется. |

## Что должно быть доказано для возможного re-open
1. Не меньше 10-15 локальных ICP-компаний с подтверждённым повторяющимся security questionnaire volume.
2. Реализованный чек **≥250 000 ₽/мес** без скидок и с contribution margin **≥100 000 ₽/клиент/мес**.
3. Снижение fully-loaded CAC хотя бы до **≤1,2-1,5 млн ₽** через repeatable channel motion.
4. Доказательство, что продукт выигрывает у generic LLM + internal KB по auditability, governance и speed-to-close.

## LTV Upside Calculator

Чтобы довести кейс хотя бы до **contribution LTV/CAC = 3,0x**, нужно выполнить одно из следующих условий или их комбинацию:

| Рычаг | Текущее | Требуется для 3,0x | Комментарий |
|---|---:|---:|---|
| contribution_margin_rub_month | 54 000 ₽ | 221 200 ₽ при churn 2,5% и CAC 2,95 млн ₽ | Это требует почти 4,1x роста contribution на клиента. |
| Fully-loaded CAC | 2 949 333 ₽ | 708 000 ₽ при текущем contribution и churn | CAC нужно снизить примерно на 76%. |
| Monthly churn | 2,5% | 0,61% при текущем contribution и CAC | Для узкого enterprise tool это выглядит нереалистично. |
| ARPA | 180 000 ₽/мес | ~350 000-400 000 ₽/мес при тех же COGS | Нужен enterprise-only repositioning с лучшим pricing power. |

Практический вывод: standalone кейс чинится только при радикальном росте чека или резком падении CAC, а это противоречит текущей evidence-базе.

## Delta vs previous
Предыдущего полноценного P7 verdict по этому slug не найдено; сравнение возможно только с triage-решением от 2026-04-18.
- Было: duplicate/supporting signal, кейс не открывался.
- Стало: полный rerun подтверждает, что категория реальна, но standalone geo-expand кейс всё равно **неинвестируемый**.
- Главный апдейт rerun: теперь rejection основан не на эвристике triage, а на числах по demand, PnL и risk-layer.

## Финальный вердикт инвесткомитета
**REJECTED.**

Почему:
1. Локальный спрос и buyer universe слишком узкие, чтобы оправдать enterprise CAC.
2. `company_ebitda_rub_month` остаётся отрицательной даже на 50 клиентах.
3. Contribution LTV/CAC = `0,73x`, payback по contribution = `54,6 месяца`, moat weak.
4. Кейс полезен как supporting signal для broader trust/compliance workflow, но не как standalone investable wedge.

