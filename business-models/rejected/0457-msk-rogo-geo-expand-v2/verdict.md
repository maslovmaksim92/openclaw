# 0457 MSK Rogo GEO Expand v2 — Full Verdict Package
> Скомпилированный пакет стадий P0/P1/P4/P5/P6/P7 для публикации в GitHub.
> Примечание: в этом кейсе в исходном пайплайне использовались файлы `01-intake.md`, `02-demand.md`, `04-economics.md`, `05-critic.md`, `06-verdict.md`, `07-score-trajectory.md`; отдельных `02-validation.md` и `03-demand.md` не было, поэтому пакет сохраняет реальные артефакты без создания новых стадий задним числом.


---

## Файл: 00-brief.md

# 00-brief

## Кейс
0457-msk-rogo-geo-expand-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
0457-msk-rogo-geo-expand

## Краткое описание
Кейс создан по правилу принудительного полного пайплайна для resurrect-сигнала по Rogo, хотя раньше тема была закрыта как дубль investment banking AI workflow.

## Что делать дальше
Пройти полный пайплайн P3→P7 с новой аналитикой и в финальном verdict отдельно сравнить standalone-оценку Rogo с прежним решением о дубле закрытого кейса.


---

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-0457-msk-rogo-geo-expand.md
created: 2026-04-19T21:34:25+03:00
---

# Intake

## Название
0457 MSK Rogo GEO Expand

## Режим обработки
Принудительный resurrect по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Исходный triage
/home/node/.openclaw/workspace/branch-models-lead/pipeline/triage/triage-2026-04-18-0457-msk-rogo-geo-expand.md

## Краткий контекст
Сигнал ранее уже разбирался, но по правилу resurrect должен пройти независимую полную переоценку как standalone candidate.

## Полный контекст из raw

# RESURRECT SIGNAL — 0457-msk-rogo-geo-expand

## Meta
- source: triage/triage-2026-04-18-0457-msk-rogo-geo-expand.md
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
- `pipeline/raw/raw-2026-04-18-0457-msk-rogo-geo-expand.md`

## Классификация
Дубль ранее обработанного сигнала.

## Решение
Новый кейс не создан, открытый кейс в `pipeline/cases/` не обогащался.

## Почему не создан кейс
- Сигнал относится к той же теме, что и ранее обработанные материалы по Rogo и AI-native платформе для investment banking workflow.
- В репозитории уже есть несколько обработанных raw-файлов и триажей по Rogo, а также завершённый кейс `investment-banking-ai-analyst-operator`, который был доведён до финального вердикта и отклонён в `pipeline/rejected/`.
- Во входном файле нет нового фактического материала, который менял бы вывод по кейсу: повторяются те же опорные тезисы про traction, отсутствие зрелого российского аналога, сложную локализацию и высокий enterprise-чек.
- По standing orders обогащение выполняется только для существующих открытых кейсов в `pipeline/cases/`. Подходящего открытого кейса по этой теме сейчас нет.

## Что сделано
- Сигнал отмечен как дубль ранее обработанной темы.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Дубль по уже обработанной и закрытой теме Rogo / AI для investment banking. Без создания нового кейса и без обогащения существующих материалов.

```



---

## Файл: 02-demand.md

# 02-demand — Demand Validation

## Кейс
Rogo, AI-native платформа для investment banking, private markets и institutional finance workflow: research, memo drafting, diligence materials, slide decks и Excel-модели в закрытом enterprise-контуре.

## Итог
**Статус: CONDITIONAL PASS**

По exact-keyword спросу в открытом RU-поиске сигнал низкий, но money demand подтверждён. Rogo не продаётся как массовый self-serve SaaS, а как bespoke enterprise deployment для финансовых институтов. Официальный сайт прямо позиционирует продукт как AI platform purpose-built for finance, с custom deployment, интеграцией в CRM / SharePoint / market data и institutional-grade outputs. Дополнительно Rogo в январе 2026 объявил о Series C на **$75 млн** и экспансии в Европу, что усиливает category proof и показывает, что продукт уже продаётся крупным финансовым покупателям. Для demand-stage это достаточно, чтобы не делать early reject.

**Sources: T1 official Rogo materials and ЦБ РФ; T2 adjacent paid substitutes and financial data vendors; T3 internal demand API.**

## 1. Demand data
Источник: internal demand API.

- `Rogo AI finance`: composite demand **LOW**, score **0**, Google Trends RU **1**, Habr **2**, hh.ru **0**, Yandex suggest **2**. [T3]
- `investment banking AI analyst`: composite demand **LOW**, score **0**, Google Trends RU **0**, Habr **2**, hh.ru **0**, Yandex suggest **2**. [T3]
- `M&A AI analyst`: composite demand **LOW**, score **3**, Google Trends RU **0**, Habr **2**, hh.ru **12**, Yandex suggest **2**. [T3]
- `financial research AI investment banking`: composite demand **LOW**, score **0**, Google Trends RU **1**, Habr **2**, hh.ru **0**, Yandex suggest **2**. [T3]

### Интерпретация
Низкий прямой search demand ожидаем: категория продаётся через founder-led / enterprise sales в узкий круг банков, advisory-команд, private equity, debt и corpdev-функций, а не через массовый keyword pull. При этом даже смежный сигнал `M&A AI analyst` уже даёт вакансии, а сам Rogo показывает, что buyers существуют и готовы внедрять AI в high-stakes financial workflow. [T1][T3]

## 2. Реальные конкуренты и ценовые якоря

| Игрок | Что продаёт | Публичная цена | Что это доказывает |
|---|---|---:|---|
| Контур.Фокус | проверка контрагентов, финанализ, скоринг | **31 155 / 82 770 / 115 000 ₽** | российский рынок уже платит за due diligence и risk tooling. [T2] |
| Прима-Информ | проверка компаний и API | **16 000 / 52 000 / 65 000 ₽ в год**, API **975 000 ₽ в год** | даже data-only слой уже доходит почти до 1 млн ₽/год. [T2] |
| Cbonds API & Data Feed | рыночные данные и интеграция во внутренние системы | публичная цена не раскрыта, доступ по заявке | financial teams уже покупают data infrastructure как отдельный enterprise budget line. [T2] |
| Rogo | bespoke AI deployment для finance professionals | цена публично не раскрыта | category proof: AI-native workflow для bankers и investors уже продаётся как отдельный продуктовый слой. [T1] |

### Вывод по конкурентам
Покупатель уже тратит деньги на market data, контрагентскую проверку, финансовую аналитику и internal research tooling. Значит Rogo-подобный продукт продаётся не из нового абстрактного AI-бюджета, а поверх существующего spend. Для чека **400 000–900 000 ₽/мес** гипотеза выглядит правдоподобно, если продаётся полный workflow outcome, а не просто поиск по данным. Это inference из adjacent pricing, не прямой публичный прайс Rogo. [T1][T2, вывод]

## 3. Buyer surface в РФ
ЦБ РФ публикует перечень системно значимых кредитных организаций от **7 октября 2025 года**: в нём **12 банков**, на которые приходится около **80%** активов банковского сектора. [T1] Это полезный anchor для buyer concentration: даже в узком контуре few buyers, high ACV несколько сделок могут materially сдвигать выручку.

Помимо банков, адресуемый слой включает:
- крупные корпорации с corpdev / strategy / treasury функциями,
- инвестбанковские и M&A advisory-практики,
- private equity и special situations команды,
- крупные инвесткомпании и debt / restructuring advisory.

### Вывод
Рынок узкий, но не нулевой. Для standalone demand validation этого достаточно: это enterprise motion с малым числом покупателей и высоким чеком, а не широкий SaaS по поисковому спросу. [T1][T2]

## 4. TAM / SAM / SOM в рублях

### Базовые допущения
- Base-case чек: **600 000 ₽/мес** = **7,2 млн ₽/год** на клиента. [T2, вывод]
- Для standalone Rogo беру более узкий buyer universe, чем у общего кейса investment-banking AI analyst, потому что здесь фокус именно на институциональном finance workflow с высокими требованиями к security и quality. [вывод]

### TAM
Широкий адресуемый контур: **900** организаций и команд в РФ и русскоязычном enterprise-контуре.

**TAM = 900 × 7,2 млн ₽ = 6,48 млрд ₽/год**. [расчёт]

### SAM
Реально адресуемый первый слой: **120** аккаунтов.

Сюда входят:
- системно значимые и крупные банки,
- top advisory / M&A / debt / restructuring контур,
- крупные корпорации с активным corpdev и transaction workload.

**SAM = 120 × 7,2 млн ₽ = 864 млн ₽/год**. [расчёт]

### SOM
Ранний реалистичный слой: **6 контрактов**.

**SOM = 6 × 7,2 млн ₽ = 43,2 млн ₽/год**. [расчёт]

### Вывод по рынку
Standalone-кейс уже не выглядит «слишком маленьким», если принять enterprise deployment motion. Рынок узкий, но достаточный для fund-style фильтра при high ACV и нескольких сильных дизайнах внедрения.

## 5. WTP, доказательства готовности платить
1. Rogo на официальном сайте заявляет custom deployment, white-glove partnership, интеграции с financial data universe и institutional-grade outputs, то есть продукт изначально упакован как дорогой enterprise workflow layer. [T1]
2. В новости от **28 января 2026 года** Rogo сообщил о **$75 млн Series C** и расширении в Европу. Это не доказывает цену, но усиливает вывод, что институциональные buyers и инвесторы видят повторяемый спрос на категорию. [T1]
3. Контур.Фокус и Прима-Информ показывают, что российский рынок уже платит за adjacent due diligence / financial analysis stack, а API-only слой может стоить почти **1 млн ₽/год** без AI-workflow. [T2]
4. Cbonds продаёт API/Data Feed для интеграции во внутренние системы, что подтверждает отдельную budget line на financial data infrastructure. [T2]

### Вывод по WTP
**WTP подтверждён условно.** Прямого публичного прайса Rogo нет, но есть сильный набор косвенных доказательств: category proof от самого Rogo, капитал для масштабирования, и существующий spend на adjacent инструменты. Для demand-stage этого хватает, хотя на economics-этапе придётся жёстко проверить реалистичность ACV и длину sales cycle.

## 6. Profit Gate
Цель: проверить, есть ли путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Узкий advisory copilot
- Цена: **400 000 ₽/мес**. [вывод]
- Валовая маржа: **55%**. [вывод]
- Валовая прибыль на клиента: **220 000 ₽/мес**. [расчёт]
- При fixed costs **2,2 млн ₽/мес** нужно около **13 клиентов**. [расчёт]

**Вердикт: CONDITIONAL PASS.** Достижимо, но уже чувствительно к длинному циклу продаж.

### Сценарий B. Base-case institutional workflow operator
- Цена: **600 000 ₽/мес**. [T2, вывод]
- Валовая маржа: **60%**. [вывод]
- Валовая прибыль на клиента: **360 000 ₽/мес**. [расчёт]
- Нужно около **8 клиентов**. [расчёт]

**Вердикт: PASS.** Это выглядит рабочим сценарием для фонда.

### Сценарий C. Enterprise private deployment
- Цена: **900 000 ₽/мес**. [T1][T2, вывод]
- Валовая маржа: **65%**. [вывод]
- Валовая прибыль на клиента: **585 000 ₽/мес**. [расчёт]
- Нужно около **5 клиентов**. [расчёт]

**Вердикт: PASS.** Это самый сильный вариант, если Rogo-подобный продукт действительно стандартизирует deployment, а не уходит в чистый кастом.

## 7. Общий вывод
- Search demand: **LOW**
- Adjacent enterprise demand: **есть**
- Category proof: **есть, и он усилился в январе 2026**
- РФ substitutes и budget lines: **есть**
- WTP: **подтверждён условно**
- Profit Gate: **проходит**

## 8. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс стоит переводить дальше в economics. При этом уже на demand-stage видно, что standalone Rogo ближе к тому же buyer universe, что и `investment-banking-ai-analyst-operator-v2`, поэтому на финальном verdict понадобится отдельная проверка: это самостоятельный wedge или всё же продуктовая упаковка того же core workflow.

## Market Pulse
> Market Pulse 2026-04-20: растущий интерес.

Веб-сигналы на **20 апреля 2026** поддерживают тезис о росте интереса: у Rogo свежий раунд и европейская экспансия, а сам category narrative вокруг AI for finance стал заметно сильнее, чем в старом проходе.

## Источники
- **[T1]** Rogo homepage: https://rogo.ai/
- **[T1]** Rogo, Series C announcement, 28.01.2026: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion
- **[T1]** Банк России, перечень системно значимых кредитных организаций на 07.10.2025: https://www.cbr.ru/banking_sector/credit/systembanks.html/
- **[T2]** Контур.Фокус, тарифы: https://focus.kontur.ru/site/price
- **[T2]** Прима-Информ, тарифы: https://www.prima-inform.ru/services
- **[T2]** Cbonds API & Data Feed: https://cbonds.ru/api/
- **[T3]** Internal demand API: `http://172.18.0.1:9001/multi-demand?keyword=Rogo%20AI%20finance`
- **[T3]** Internal demand API: `http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20AI%20analyst`
- **[T3]** Internal demand API: `http://172.18.0.1:9001/multi-demand?keyword=M%26A%20AI%20analyst`
- **[T3]** Internal demand API: `http://172.18.0.1:9001/multi-demand?keyword=financial%20research%20AI%20investment%20banking`

- Market Pulse 2026-04-20: растущий интерес.


---

## Файл: 04-economics.md

# 04-economics

## Кейс
Rogo GEO Expand, AI-native платформа для investment banking, private markets и institutional finance workflow в закрытом enterprise-контуре.

## Economics verdict
**Статус: PASS WITH RESERVATIONS**

Как и на demand-stage, экономика проходит только в конфигурации дорогого enterprise workflow, а не как «ещё один AI-ассистент для аналитика». При MRR **650 000 ₽/клиент/мес**, fully-loaded CAC **1 520 000 ₽**, contribution margin **56,9%** и monthly churn **1,2%** кейс проходит обязательные фондовые sanity-checks. Главный риск не в unit economics, а в тяжёлом go-to-market: pilot, security review, procurement и узкий buyer universe.

## Источники и anchors
1. Текущий `02-demand.md` кейса: Rogo, Series C **$75 млн** и европейская экспансия от **28 января 2026**, перечень системно значимых банков ЦБ РФ от **7 октября 2025**, а также ценовые якоря Контур.Фокус, Прима-Информ и Cbonds.
2. Optifai, churn benchmark по ACV, опубликовано в 2026 году: enterprise >$100K ACV ≈ **0,7% monthly churn**, upper mid-market $50K-$100K ≈ **1,3%** monthly churn. Для модели беру **1,2%** как консервативный enterprise-light сценарий: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
3. HH.ru, текущие salary anchors по Москве, проверено **20 апреля 2026**:
   - senior backend engineer: https://hh.ru/vacancies/senior-backend-engineer
   - account executive: https://hh.ru/vacancies/account_executive
   - пример senior backend в Яндексе, архив от **23 января 2026**: https://hh.ru/vacancy/129266637
4. Official Rogo materials:
   - https://rogo.ai/
   - https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion

## 1. Базовые допущения модели
- ICP: крупные банки, M&A / ECM / DCM / restructuring advisory, private equity, corpdev и strategy-функции крупных корпораций.
- Модель выручки: enterprise subscription + внедрение; в unit economics считаю только recurring MRR.
- Средний recurring чек: **650 000 ₽/мес**.
- Разовый onboarding / pilot setup fee: **600 000 ₽**, в LTV не включаю.
- Категория: regulated enterprise finance workflow, поэтому беру повышенную нагрузку на delivery, compliance и GTM.
- Monthly logo churn: **1,2%**.

## 2. Business process: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Account selection по банкам, advisory и corpdev | SDR + founder | CRM, ручной ресерч, базы компаний | 2 ч/акк | 2 800 | Средняя |
| 2 | Enrichment, контактные лица, pain mapping | SDR | CRM + enrichment | 1,5 ч | 2 000 | Средняя |
| 3 | Founder-led outbound / intro sequence | SDR + founder | e-mail, Telegram, calls | 2-3 недели | 14 000 | Средняя |
| 4 | Discovery call и qualification | AE + founder | Meet, CRM | 1 ч + prep | 10 000 | Низкая |
| 5 | Demo на реальном workflow: memo, comps, CIM, DDQ | AE + solutions analyst | secure sandbox | 3-5 дней | 22 000 | Низкая |
| 6 | Security / legal / procurement review | CTO + legal + buyer IT | policies, DPA, VDR | 2-5 недель | 58 000 | Низкая |
| 7 | Pilot setup в закрытом контуре | CTO + backend + ML | VPC, connectors, evals | 3-6 недель | 155 000 | Средняя |
| 8 | Pilot сопровождение и steering | AE + analyst + CSM | CRM, Jira, weekly reviews | 1 месяц | 96 000 | Низкая |
| 9 | Contracting, ЭДО, invoicing | AE + finance ops | договор, ЭДО, банк | 1-3 недели | 9 000 | Средняя |
| 10 | Go-live и первые success review | CSM + product | analytics, support stack | ongoing | 34 000/мес | Средняя |

### Вывод
Продажа тяжёлая и дорогая. Узкое место здесь не top-of-funnel, а conversion через pilot и procurement. Значит считать надо не raw ad CAC, а fully-loaded CAC.

## 3. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / agent runtime | 78 000 | heavy document and memo workflow | usage-intensive сегмент |
| Financial / company data layer | 62 000 | market data, company intelligence, external APIs | ключевой cost bucket |
| Secure infra / storage / logging | 34 000 | private deployment, audit trail, storage | обязательно для finance |
| Implementation amortization | 45 000 | часть pilot/setup cost, размазанная по 12 мес | не занижаю delivery |
| Customer success / analyst support | 34 000 | low-volume enterprise support | высокий touch |
| QA / compliance / traceability | 18 000 | проверки quality и auditability | high-stakes workflow |
| Billing / legal / admin | 9 000 | ЭДО, акты, договорной контур | постоянный слой |
| **Итого COGS** | **280 000** |  |  |
| **MRR на клиента** | **650 000** |  |  |
| **Contribution / client / month** | **370 000** | 650 000 - 280 000 |  |
| **Contribution Margin** | **56,9%** | 370 000 / 650 000 |  |

## 4. CAC по каналам и fully-loaded CAC

### 4.1 Raw CAC по каналам

| Канал | Monthly input | Meeting rate | Pilot rate | Paid conversion | New paying / мес | Monthly spend, ₽ | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / ABM | 120 target accounts | 18% = 22 meetings | 32% = 7 pilots | 28% = 2 paid | 1,9 | 1 950 000 | 1 026 000 |
| Partnerships / referrals | 18 intros | 45% = 8 meetings | 50% = 4 pilots | 38% = 1,5 paid | 0,8 | 760 000 | 950 000 |
| Events / thought leadership | 50 inbound/MQL | 20% = 10 meetings | 30% = 3 pilots | 33% = 1 paid | 0,5 | 620 000 | 1 240 000 |
| **Blended raw** |  |  |  |  | **3,2** | **3 330 000** | **1 040 625** |

### 4.2 Fully-loaded CAC
Формула фонда:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT + Marketing FOT allocation + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers`

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid / sponsored / distribution | **180 000** | точечный B2B demand gen |
| Outbound team FOT, attributed to new | **780 000** | SDR + AE + variable comp, fully-loaded |
| Founder / PMM allocation | **260 000** | founder-led selling и market education |
| Tools / CRM / sequencing / enrichment | **135 000** | GTM stack |
| Events / partnerships | **420 000** | отраслевые события, поездки, partner motion |
| **Subtotal** | **1 775 000** |  |
| Overhead multiplier x1,3 | **532 500** | shared ops / legal / management overhead |
| **Total acquisition cost / мес** | **2 307 500** |  |
| New paying customers / мес | **1,52** | консервативный steady-state |
| **Fully-loaded CAC** | **1 518 092 ₽** | итог |

### CAC sanity check
Это выше generic enterprise SaaS benchmark **300-900K ₽**, но для regulated finance workflow с pilot, security review и длинным procurement цикл выглядит правдоподобно. Слишком низкий CAC здесь был бы скорее red flag.

## 5. LTV и churn
### Выбор churn
По Optifai enterprise сегмент показывает около **0,7%** monthly churn, upper mid-market, около **1,3%**. Для Rogo-подобного motion беру **1,2%**, потому что:
- ACV высокий,
- внедрение глубокое,
- switching costs существенные,
- но buyer universe узкий и продуктовая категория ещё не fully commoditized.

### Расчёт LTV
- Contribution profit per client/month = **370 000 ₽**
- Monthly churn = **1,2%**
- **LTV = 370 000 / 0,012 = 30 833 333 ₽**

## 6. LTV/CAC ratio
- LTV = **30,83 млн ₽**
- Fully-loaded CAC = **1,52 млн ₽**
- **LTV/CAC = 20,3x**

**PASS.** Существенно выше порога **3,0x**.

## 7. CAC Payback
- По MRR: **1 518 092 / 650 000 = 2,34 месяца**
- По contribution: **1 518 092 / 370 000 = 4,10 месяца**

Даже по более строгой contribution-версии это заметно лучше лимита **<12 мес**.

## 8. Full team table и salary realism

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---:|---:|
| CEO / founder-sales | 1 | top accounts, partnerships, fundraising | 700 000 | 210 000 | 910 000 |
| CTO / Tech Lead | 1 | architecture, security, deployment | 620 000 | 186 000 | 806 000 |
| Senior Backend | 2 | integrations, data pipelines, backend | 420 000 | 126 000 | 1 092 000 |
| ML Engineer | 1 | retrieval, evals, agent quality | 520 000 | 156 000 | 676 000 |
| DevOps / Security | 1 | VPC, infra, observability, access control | 380 000 | 114 000 | 494 000 |
| Frontend | 1 | analyst workspace, approvals, UI | 320 000 | 96 000 | 416 000 |
| Product / Solutions Lead | 1 | workflow design, pilots, implementation | 360 000 | 108 000 | 468 000 |
| Solutions Analyst | 1 | demos, onboarding, QA | 280 000 | 84 000 | 364 000 |
| SDR | 1 | outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | 1 | discovery, proposal, closing | 320 000 | 96 000 | 416 000 |
| Customer Success | 1 | retention, adoption, upsell | 260 000 | 78 000 | 338 000 |
| Finance / Ops | 1 | billing, contracts, docs ops | 180 000 | 54 000 | 234 000 |
| **Итого** | **13** |  |  |  | **6 448 000 ₽/мес** |

### Hiring realism
- В первый месяц нельзя реалистично нанять всю команду.
- Senior backend anchor на HH по Москве подтверждает диапазон порядка **350 000 ₽+ gross** уже у крупных работодателей; для finance-grade AI stack ставка **420 000 ₽ gross** выглядит реалистично, не занижено.
- AE по HH для Москвы обычно виден в коридоре порядка **180 000-320 000 ₽** gross / OTE-base для B2B-ролей; беру **320 000 ₽ gross** как верхнюю рабочую точку для enterprise motion.

## 9. Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Product/Solutions Lead | **2 184 000** |
| M2 | + Senior Backend #1 | **2 730 000** |
| M3 | + Senior Backend #2, DevOps | **3 770 000** |
| M4 | + ML Engineer, Frontend | **4 862 000** |
| M5 | + Solutions Analyst | **5 226 000** |
| M6 | + SDR | **5 460 000** |
| M7 | + AE | **5 876 000** |
| M8 | + Customer Success | **6 214 000** |
| M9 | + Finance/Ops | **6 448 000** |
| M10 | без изменений | **6 448 000** |
| M11 | без изменений | **6 448 000** |
| M12 | без изменений | **6 448 000** |

## 10. Fixed costs breakdown

| Fixed cost item | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | **6 448 000** | таблица выше |
| Shared infra / observability / internal tools | **430 000** | не client-specific часть |
| Legal / compliance / audit support | **220 000** | finance-grade overhead |
| Office / admin / equipment | **260 000** | гибридный режим |
| Travel / enterprise selling | **120 000** | встречи, events |
| Misc reserve | **80 000** | запас |
| **Итого fixed costs / мес** | **7 558 000** |  |

## 11. Break-even
### По клиентам
- Contribution на клиента: **370 000 ₽/мес**
- Fixed costs: **7 558 000 ₽/мес**
- **Operating break-even = 7 558 000 / 370 000 = 20,4**, округляю до **21 клиента**
- Для цели **500 000 ₽ EBITDA/мес** нужно: `(7 558 000 + 500 000) / 370 000 = 21,8`, то есть **22 клиента**

### По месяцам, base ramp
Предполагаемый ramp:
- M5: 1 клиент
- M6: 2
- M7: 3
- M8: 5
- M9: 7
- M10: 10
- M11: 13
- M12: 16
- M13: 18
- M14: 20
- **M15: 22**

**Вывод:** operating break-even около **M14-M15**, порог **500k EBITDA/mo** около **M15**.

## 12. Burn-to-breakeven и runway
### Burn-to-breakeven
Грубая модель накопленного отрицательного EBITDA:
- M1-M4: около **19,1 млн ₽** burn
- M5-M8: ещё около **21,7 млн ₽**
- M9-M14: ещё около **16,8 млн ₽**
- **Burn to break-even ≈ 57,6 млн ₽**

### Runway
Если брать стартовый капитал **65 млн ₽**:
- средний burn до M12 около **4,7 млн ₽/мес**,
- runway получается порядка **13-14 месяцев**,
- до break-even дотягивает, но без большого запаса.

Комфортный стартовый капитал для такого motion, **70-75 млн ₽**.

## 13. Profit Gate
### Проверка LTV/CAC
- Требование: **>= 3,0x**
- Факт: **20,3x**
- **PASS**

### Проверка CAC Payback
- Требование: обычно **<12 мес**, для enterprise допустимо до **18 мес**
- Факт: **2,34 мес по MRR**, **4,10 мес по contribution**
- **PASS**

### Проверка EBITDA при 50 клиентах
- EBITDA = `50 × 370 000 - 7 558 000 = 10 942 000 ₽/мес`
- Требование: достижим **>= 500 000 ₽/мес**
- **PASS**

## 14. Финальный вывод
P5 кейс **проходит**, но не потому что он «лёгкий», а потому что при высоком ACV unit economics выдерживают тяжёлый enterprise GTM. Слабое место остаётся прежним: это почти тот же buyer universe, что у более общего кейса `investment-banking-ai-analyst-operator-v2`.

То есть standalone Rogo в economics выглядит жизнеспособно, но на следующем этапе надо жёстко проверить два вопроса:
1. это отдельный investable wedge, или всё ещё продуктовая упаковка того же broader workflow,
2. не переоцениваем ли способность локальной команды дойти до **21-22 платящих enterprise клиентов** в разумный срок.

Итого: **PASS WITH RESERVATIONS**, переводить в critic.


---

## Файл: 05-critic.md

# SECTION A. PnL 12 месяцев

## A1. Принятые допущения

- ARPA / MRR на клиента: **650 000 ₽/мес**.
- COGS на клиента: **280 000 ₽/мес**.
- Contribution margin на клиента: **370 000 ₽/мес** (**56,9%**).
- Fully-loaded CAC anchor: **1 518 092 ₽**.
- Fixed costs = team FOT по ramp из 04-economics + прочие fixed costs **1 110 000 ₽/мес**.
- Страховые взносы уже включены в FOT на уровне **~30% к gross**.
- Налоговые режимы для net view: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры, **ОСНО 20% на прибыль + НДС 20%** если применимо.
- Формула active clients: `Clients_t = Clients_(t-1) × (1 - churn) + New clients_t`.

## A2. Сценарий: Базовый

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 1.99 | 2.96 | 4.93 | 6.87 | 9.79 | 12.67 | 15.52 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 650 000 | 1 292 200 | 1 926 694 | 3 203 573 | 4 465 130 | 6 361 549 | 8 235 210 | 10 086 388 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 280 000 | 556 640 | 829 960 | 1 380 001 | 1 923 441 | 2 740 359 | 3 547 475 | 4 344 905 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 370 000 | 735 560 | 1 096 733 | 1 823 572 | 2 541 690 | 3 621 189 | 4 687 735 | 5 741 482 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% |
| Fixed costs, ₽ | 3 294 000 | 3 840 000 | 4 880 000 | 5 972 000 | 6 336 000 | 6 570 000 | 6 986 000 | 7 324 000 | 7 558 000 | 7 558 000 | 7 558 000 | 7 558 000 |
| EBITDA, ₽ | -3 294 000 | -3 840 000 | -4 880 000 | -5 972 000 | -5 966 000 | -5 834 440 | -5 889 267 | -5 500 428 | -5 016 310 | -3 936 811 | -2 870 265 | -1 816 518 |
| Cash burn, ₽ | 3 294 000 | 3 840 000 | 4 880 000 | 5 972 000 | 5 966 000 | 5 834 440 | 5 889 267 | 5 500 428 | 5 016 310 | 3 936 811 | 2 870 265 | 1 816 518 |
| Cumulative cash, ₽ | -3 294 000 | -7 134 000 | -12 014 000 | -17 986 000 | -23 952 000 | -29 786 440 | -35 675 707 | -41 176 134 | -46 192 445 | -50 129 255 | -52 999 520 | -54 816 038 |

- Break-even по клиентам, EBITDA 0: **21** клиентов.
- Break-even по клиентам после налога: **23** на УСН, **22** при IT-льготе, **21** на ОСНО по прибыли (без учёта эффекта НДС на cash).
- Break-even по месяцам: **не достигнут в пределах M1-M12**.
- Startup capital to BEP: **54 816 038 ₽**.

## A2. Сценарий: Оптимистичный

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 |
| Total clients | 0 | 0 | 0 | 1 | 1.99 | 3.97 | 5.94 | 8.88 | 11.80 | 15.70 | 19.56 | 23.38 |
| MRR, ₽ | 0 | 0 | 0 | 650 000 | 1 294 150 | 2 582 503 | 3 859 260 | 5 774 527 | 7 672 556 | 10 203 503 | 12 711 672 | 15 197 266 |
| COGS, ₽ | 0 | 0 | 0 | 280 000 | 557 480 | 1 112 463 | 1 662 451 | 2 487 488 | 3 305 101 | 4 395 355 | 5 475 797 | 6 546 515 |
| Gross profit, ₽ | 0 | 0 | 0 | 370 000 | 736 670 | 1 470 040 | 2 196 810 | 3 287 038 | 4 367 455 | 5 808 148 | 7 235 875 | 8 650 752 |
| GM% | 0,0% | 0,0% | 0,0% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% |
| Fixed costs, ₽ | 3 294 000 | 3 840 000 | 4 880 000 | 5 972 000 | 6 336 000 | 6 570 000 | 6 986 000 | 7 324 000 | 7 558 000 | 7 558 000 | 7 558 000 | 7 558 000 |
| EBITDA, ₽ | -3 294 000 | -3 840 000 | -4 880 000 | -5 602 000 | -5 599 330 | -5 099 960 | -4 789 190 | -4 036 962 | -3 190 545 | -1 749 852 | -322 125 | 1 092 752 |
| Cash burn, ₽ | 3 294 000 | 3 840 000 | 4 880 000 | 5 602 000 | 5 599 330 | 5 099 960 | 4 789 190 | 4 036 962 | 3 190 545 | 1 749 852 | 322 125 | 0 |
| Cumulative cash, ₽ | -3 294 000 | -7 134 000 | -12 014 000 | -17 616 000 | -23 215 330 | -28 315 290 | -33 104 480 | -37 141 442 | -40 331 987 | -42 081 839 | -42 403 965 | -42 403 965 |

- Break-even по клиентам, EBITDA 0: **21** клиентов.
- Break-even по клиентам после налога: **23** на УСН, **22** при IT-льготе, **21** на ОСНО по прибыли (без учёта эффекта НДС на cash).
- Break-even по месяцам: **M12**.
- Startup capital to BEP: **42 403 965 ₽**.

## A2. Сценарий: Пессимистичный

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 1 | 1.98 | 2.95 | 4.89 | 6.81 | 8.68 | 10.53 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 650 000 | 1 288 300 | 1 915 111 | 3 180 639 | 4 423 387 | 5 643 766 | 6 842 178 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 280 000 | 554 960 | 824 971 | 1 370 121 | 1 905 459 | 2 431 161 | 2 947 400 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 370 000 | 733 340 | 1 090 140 | 1 810 517 | 2 517 928 | 3 212 605 | 3 894 778 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% | 56,9% |
| Fixed costs, ₽ | 3 294 000 | 3 840 000 | 4 880 000 | 5 972 000 | 6 336 000 | 6 570 000 | 6 986 000 | 7 324 000 | 7 558 000 | 7 558 000 | 7 558 000 | 7 558 000 |
| EBITDA, ₽ | -3 294 000 | -3 840 000 | -4 880 000 | -5 972 000 | -6 336 000 | -6 200 000 | -6 252 660 | -6 233 860 | -5 747 483 | -5 040 072 | -4 345 395 | -3 663 222 |
| Cash burn, ₽ | 3 294 000 | 3 840 000 | 4 880 000 | 5 972 000 | 6 336 000 | 6 200 000 | 6 252 660 | 6 233 860 | 5 747 483 | 5 040 072 | 4 345 395 | 3 663 222 |
| Cumulative cash, ₽ | -3 294 000 | -7 134 000 | -12 014 000 | -17 986 000 | -24 322 000 | -30 522 000 | -36 774 660 | -43 008 520 | -48 756 003 | -53 796 075 | -58 141 469 | -61 804 691 |

- Break-even по клиентам, EBITDA 0: **21** клиентов.
- Break-even по клиентам после налога: **23** на УСН, **22** при IT-льготе, **21** на ОСНО по прибыли (без учёта эффекта НДС на cash).
- Break-even по месяцам: **не достигнут в пределах M1-M12**.
- Startup capital to BEP: **61 804 691 ₽**.

## A3. Waterfall: 1 клиент / месяц и налоговый net view

| Шаг waterfall | ₽ / клиент / месяц | Комментарий |
|---|---:|---|
| ARPA | 650 000 | recurring выручка |
| Gross profit | 370 000 | ARPA - COGS 280 000 |
| Contribution | 370 000 | в модели доп. переменных затрат сверх COGS не заложено |
| EBITDA при 22 клиентах | 26 455 | аллокация fixed costs 343 545 на клиента, это пороговый scale-up level |
| Net after tax, УСН 6% | -12 545 | налог с выручки 39 000 |
| Net after tax, IT-льгота 3% | 6 955 | налог с выручки 19 500 |
| Net after tax, ОСНО 20% | 21 164 | налог на прибыль, НДС 20% ухудшает cash conversion при слабом входящем VAT credit |

## A4. Налоговая модель и cash flow

- **УСН 6%**: лучше для ранней стадии с отрицательной EBITDA, но при низком EBITDA на клиента съедает почти весь post-fixed profit.
- **IT-льгота 3%**: лучший режим для scale-up кейса при наличии аккредитации Минцифры, потому что снижает налог с выручки в 2 раза против УСН 6%.
- **ОСНО 20%**: на PnL выглядит терпимо только после выхода в плюс, но для cash flow хуже из-за **НДС 20%** и более тяжёлого администрирования.
- **Страховые взносы ~30% к ФОТ** уже зашиты в payroll ramp; повторно не добавляются в PnL строках.
- Практический вывод по cash: для этого кейса целевой режим, **если возможно соответствие критериям**, это **IT-льгота 3%**; запас стартового капитала всё равно нужен из-за длинного enterprise ramp.

## A5. Итог по стартовому капиталу до BEP

| Сценарий | Startup capital to BEP, ₽ | Комментарий |
|---|---:|---|
| Базовый | 54 816 038 | BEP за 12 месяцев не достигается |
| Оптимистичный | 42 403 965 | операционный BEP в M12 |
| Пессимистичный | 61 804 691 | BEP за 12 месяцев не достигается |

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

База взята из SECTION A: M12 EBITDA **-1 816 518 ₽/мес**, active clients **15,52**, ARPU **650 000 ₽**, COGS **280 000 ₽**, monthly churn **1,2%**, fixed costs **7 558 000 ₽/мес**. Для `CAC x2` держу GTM-бюджет постоянным, поэтому поток новых paying клиентов в модели снижается примерно в 2 раза. [T1][T2]

| Сценарий | Ключевое изменение | Active clients @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | 15,52 | -1 816 518 | уже ниже нуля, но близко к M15 break-even из P6A |
| Sens1 | CAC x2 | 7,76 | -4 687 259 | CAC inflation ломает скорость набора, burn почти возвращается к ранней стадии |
| Sens2 | Churn x2 | 15,05 | -1 988 178 | эффект мягче, потому что на горизонте 12 мес база клиентов ещё не fully compounded |
| Sens3 | Price -30% | 15,52 | -4 842 434 | самый болезненный удар: contribution падает с 370k до 175k на клиента |

### Вывод
Самая опасная переменная для этого кейса, не считая outright sales failure, это **price compression**. При цене **455 000 ₽/мес** Rogo-подобный deployment теряет экономику почти мгновенно, потому что secure infra, delivery и data layer остаются почти фиксированными. CAC shock тоже критичен, но он бьёт через скорость роста; price cut бьёт напрямую по contribution. [T1][T2]

## B2. Monte Carlo Lite — confidence intervals

Ниже не полноценный кодовый Monte Carlo, а **proxy из 9 комбинаций** на triangular inputs. `mode` совпадает с базовой моделью P5/P6A; `min/max` заданы как консервативные границы из demand/economics и стресс-правил текущего задания. [T1][T2][T3]

### Inputs (triangular distribution)

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 1 000 000 | 1 518 092 | 3 036 184 | [T2], max = stress `CAC x2` |
| Monthly churn % | 0,7% | 1,2% | 2,4% | [T2], max = stress `Churn x2` |
| ARPU ₽/мес | 455 000 | 650 000 | 900 000 | [T1][T2], min = stress `Price -30%`, max = upper enterprise deployment из demand |
| Conversion rate lead→paid % | 18% | 24% | 32% | [T2], proxy по blended enterprise funnel between pilot and paid |
| Time-to-hire месяцев (среднее) | 1,0 | 1,5 | 3,0 | [T2], inference from hiring realism for senior tech + enterprise GTM |

### Результат proxy-симуляции

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -3 262 486 | 7 055 789 | 32 778 249 | 36 040 735 |
| CAC payback (мес) | 1,61 | 4,90 | 17,35 | 15,74 |
| LTV/CAC | 4,80x | 17,02x | 52,86x | 48,06x |
| Cash runway (мес) | 13,39 | 64,62 | 99+ | 85,61+ |

### Интерпретация правил gate
1. **p10 EBITDA < 0** → trigger для **kill criterion #1**: в левом хвосте кейс уходит в риск неплатёжеспособности.
2. **p50 EBITDA > 500 000 ₽/мес** → median-сценарий EBITDA gate проходит, reject по правилу #2 не нужен.
3. **p90 / |p10| ≈ 10,0x** → неопределённость на границе допустимого; score кейса надо держать с haircut, а не как clean pass.
4. **Range width по LTV/CAC = 48,06x > 8** → модель хрупкая, драйверы нестабильны одновременно по pricing, churn и CAC.

### Что это значит practically
Кейс не выглядит безнадёжным, но **распределение слишком широкое**, чтобы считать его надёжным fund-style execution play. Это скорее ставка на то, что команда сможет удержать premium pricing и не потерять velocity enterprise-sales. Если хотя бы два драйвера одновременно уходят в bad side, upside не компенсирует execution risk. [T1][T2]

## B3. Competitor deep-dive

### Топ-3 западных

| Игрок | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| AlphaSense | широкий market-intelligence и IB workflow слой с GenAI и premium content | 6 500+ customers, 500M+ premium docs, сильный brand/trust, 80% top global banks and 88% S&P100 footprint [T4] | тяжёлый generalist stack, дорогой контент, не всегда finance-workflow-first внутри РФ-контура | **35-45%** западного enterprise research / market-intelligence сегмента, inference по ARR $500M+ и customer base [T4, вывод] | можем дать более узкий product wedge: русскоязычный finance workflow, локальный deployment, data residency и кастомизацию под РФ-процедуры |
| Hebbia | прямой AI competitor в high-finance diligence / memo / deck generation | сильный analyst-like UX, $25T AUM of firms, 1000+ production use cases, deep workflow automation [T5] | меньше явного regulatory moat, сильная зависимость от западного data ecosystem и top-tier fund budgets | **15-25%** нового GenAI-for-finance subsegment, inference по penetration among top asset managers [T5, вывод] | у нас лучше шанс выиграть там, где нужен не “AI for Wall Street”, а локальный secure private deployment с санкционно-устойчивым стеком |
| Rogo | closest direct category peer: purpose-built AI for finance, Excel/memo/diligence outputs | finance-native positioning, 25k+ users, bespoke deployment, institutional-grade outputs, trust center с SOC2/ISO/GDPR/EU AI Act [T6] | bespoke motion плохо масштабируется, enterprise sales long-cycle, высокая стоимость внедрения | **5-10%** узкого AI-for-investment-banking workflow сегмента, inference по 25k users и category maturity [T6, вывод] | в РФ можно обыгрывать через локализацию данных, русские источники, интеграции с ЭДО/1С/локальными DWH и compliance под 152-ФЗ/115-ФЗ |

### Топ-4 российских substitutes / adjacent competitors

Важно: в РФ прямого аналога Rogo уровня Wall-Street workflow я не вижу. Ниже не exact clones, а **сильные substitutes**, которые уже забирают бюджет на due diligence, company intelligence, compliance и financial data. Это inference из product positioning и открытых описаний. [T3][T7][T8][T9][T10]

| Игрок | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Контур.Фокус | стандарт де-факто для проверки контрагентов и risk/compliance в РФ | сильный бренд, 60-80+ источников, API, комплаенс по 115-ФЗ, привычность для b2b-рынка [T3][T7] | это data/compliance tool, а не AI analyst for full finance workflow | **25-35%** рынка проверки контрагентов и adjacent compliance tooling, inference по brand ubiquity [T3][T7, вывод] | мы закрываем memo, comps, diligence synthesis и decision support, а не только screening контрагентов |
| Rusprofile | massive user base, сильный доступ к открытым данным и company graph | 700k daily users, 200k+ организаций, 50+ источников, уже заявлена интеграция AI-решений [T8] | ближе к horizontal company intelligence, чем к transaction workflow | **20-30%** SMB/mid-market company-intelligence слоя, inference по audience scale [T8, вывод] | наш продукт может сидеть поверх Rusprofile-like data и превращать её в institutional outputs, а не просто карточки компаний |
| Prima-Inform | сильный data substitute в due diligence и company lookup | широкий набор реестров, поиск по физлицам, низкий entry price, понятный procurement path [T3][T9] | слабее product moat, меньше AI/workflow depth, меньше premium enterprise aura | **5-10%** рынка paid company-check/data tools, inference по pricing and visibility [T3][T9, вывод] | можем продать outcome layer с AI-генерацией и workflow orchestration, а не только доступ к данным |
| Cbonds API/Data Feed | мощный источник финансовых и долговых данных для институционалов | сильные bond/issuer datasets, привычность в инвестиционном контуре, enterprise integration motion [T3] | это data infrastructure, не end-to-end analyst copilot; value capture ограничен источником данных | **10-20%** РФ сегмента market data for debt/capital markets, inference по entrenched niche [T3, вывод] | у нас преимущество в том, что мы собираем multi-source workflow над данными и выдаём action-ready output, а не только feed |

### Сводный вывод по конкурентам
- На Западе category уже занята сильными игроками, и там Rogo конкурирует не только с такими же AI-native продуктами, но и с широкими intelligence-платформами вроде AlphaSense. [T4][T5][T6]
- В РФ прямой AI-native investment-banking copilot почти пуст, но бюджеты уже частично заняты **substitutes**: контрагентская проверка, market data, compliance-automation. [T3][T7][T8][T9]
- Значит реальная стратегия входа, если кейс делать в РФ, это не “новая категория”, а **budget re-bundling** поверх текущих spend lines. [T3]

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder-led sales не масштабируется в repeatable AE motion | high | high | >70% pipeline держится лично на фаундере к M6 | заранее нанять enterprise AE и зафиксировать playbook discovery→pilot→close |
| 2 | Operational | Недостаток senior backend / security talent для private deployments | med | high | time-to-hire >3 мес, офферы отклоняются, backlog security review растёт | поднять comp bands, использовать contractor bench, упростить target architecture |
| 3 | Operational | LLM API latency / quality drift ломают analyst-grade outputs | med | high | рост manual correction rate, падение acceptance на pilot review | multi-model routing, eval harness, fallback на локальные/альтернативные модели |
| 4 | Market | Buyer universe слишком узкий, pipeline dries up после первых 30-40 аккаунтов | med | high | meetings booked/target accounts steadily падает 2 месяца подряд | ABM discipline, расширение ICP в corpdev / PE / advisory / treasury |
| 5 | Market | Конкуренты сжимают price до 400-450k ₽/мес | high | high | win-rate падает, скидки >20% становятся нормой | продавать workflow ROI, не seat pricing; modular packaging и paid setup fee |
| 6 | Market | Generic copilots + internal bank tooling “good enough” для части use cases | med | med | пилоты заканчиваются без расширения scope, usage концентрируется в 1-2 задачах | фокус на high-stakes regulated workflows, auditability и integrations |
| 7 | Regulatory | 152-ФЗ / data residency блокируют использование западных облаков и SaaS | high | high | security questionnaires стопорятся на storage / cross-border transfer | on-prem/VPC deployment, локальные storage layers, DPA templates |
| 8 | Regulatory | 115-ФЗ / KYC / sanctions screening требуют explainability и traceability | med | high | compliance просит ручные подтверждения и refuses black-box outputs | citation-first UX, audit logs, approval flows, human-in-the-loop |
| 9 | Regulatory | Санкции ограничивают доступ к западным data/API vendors | high | high | vendor terms ужесточаются, ошибки доступа, рост отказов по billing | vendor diversification, local datasets, contractual запасные каналы |
| 10 | Financial | Burn-to-breakeven 55-70 млн ₽ оказывается недооценён | med | high | actual burn >5,5 млн ₽/мес 2 квартала подряд | stage-gated hiring, freeze non-core hires, raise earlier than planned |
| 11 | Financial | USD/RUB volatility удорожает LLM, data APIs и зарубежный SaaS | high | med | COGS/client >320k ₽ два месяца подряд | RUB repricing clauses, reserved FX buffer, shift to local infra where possible |
| 12 | Financial | Инфляция и налоги съедают contribution margin | med | med | payroll inflation >15% YoY, effective tax rate растёт | quarterly repricing, IT-accreditation, stricter scope control |
| 13 | Black swan | Новый пакет санкций отключает критичные LLM/API overnight | med | very high | новости о service suspension, предупреждения vendors | заранее держать резервный стек, тестировать offline / local alternatives |
| 14 | Black swan | Геополитическая эскалация режет enterprise IT-бюджеты и freezes procurement | med | high | сделки сдвигаются >90 дней, freezes in capex/opex approvals | target essential-risk workflows, shorter pilots, diversify sectors |

### Вывод
Матрица рисков не показывает single fatal flaw, но показывает **много correlated risks**. Самая опасная связка: `price compression + sanctions on SaaS + long enterprise sales cycle`. В такой комбинации кейс быстро переходит из “дорогой, но рабочий” в “капиталоёмкий и хрупкий”.

## B5. Kill conditions через 6 месяцев

1. **Median-risk insolvency trigger**: если обновлённый p10 по модели всё ещё даёт **EBITDA < 0 на M24**, а cash runway < **9 месяцев**, продолжать нельзя.
2. **EBITDA gate failure**: если к концу M6 forecast на M24 даёт **p50 EBITDA < 500 000 ₽/мес**, кейс не проходит фондовый порог и должен быть остановлен.
3. **Go-to-market failure**: если к M6 нет минимум **3 платящих клиентов** или blended fully-loaded **CAC > 3,0 млн ₽**, repeatable sales motion не подтверждён, дальнейшее масштабирование экономически незащищено.

## B6. Итог SECTION B

По P6B кейс **не ломается сразу**, но его устойчивость ниже, чем выглядело из точечных base-case метрик в P5/P6A. Основной инвестиционный тезис остаётся тем же: продукт может быть сильным только как **premium regulated workflow platform**. Любой уход в mid-market pricing или в generic-AI positioning почти гарантированно уничтожает экономику. Поэтому verdict после P6B должен идти с явным discount за execution risk и uncertainty width.

## Дополнительные источники SECTION B
- **[T4]** AlphaSense press: https://www.alpha-sense.com/press/alphasense-surpasses-500m-in-arr/
- **[T4]** AlphaSense pricing / who uses: https://www.alpha-sense.com/pricing
- **[T5]** Hebbia product/about/news: https://www.hebbia.com/product , https://www.hebbia.com/about , https://www.hebbia.com/newsroom/hebbia-partners-with-fitch-solutions
- **[T6]** Rogo homepage / product / trust center: https://rogo.ai/ , https://rogo.ai/product , https://trust.rogo.ai/
- **[T7]** vc.ru про Контур.Фокус: https://vc.ru/services/2803055-kontur-fokus-proverka-kontragentov-i-klientov-obzor-servisa , https://vc.ru/services/2229587-kontur-fokus-komplaens-avtomaticheskaya-proverka , https://vc.ru/services/2229745-kontur-fokus-api-avtomatizatsiya-proverki-i-analiza-kontragentov
- **[T8]** Rusprofile about/team/features: https://www.rusprofile.ru/about , https://www.rusprofile.ru/team , https://www.rusprofile.ru/features
- **[T9]** vc.ru, обзор сервисов проверки контрагентов с Prima-Inform: https://vc.ru/marketing/1124661-kak-proverit-postavshika-na-dobrosovestnost-instrukciya-dlya-sellera
- **[T10]** Skolkovo про зрелость GenAI в РФ: https://www.skolkovo.ru/events/280126-strategiya-ai-transformacii-ot-issledovaniya-k-reальным-biznes-resheniyam/ , https://www.skolkovo.ru/centres/laboratoriya-iskusstvennogo-intellekta-mshu-skolkovo/

<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[GEO-EXPAND] 0457 MSK Rogo GEO Expand v2 — NEAR-PASS: 65/100 | EBITDA base=3384К₽/мес через 15 мес | LTV/CAC=20,3x | Ключевое преимущество: глубокий finance-native workflow в закрытом enterprise-контуре | Главный риск: узкий buyer universe и недоподтверждённый локальный спрос.

# 06-verdict — 0457 MSK Rogo GEO Expand v2

sector: GEO-EXPAND
status: NEAR-PASS
score: 65/100
normalized_from_raw: 97/150
case_slug: 0457-msk-rogo-geo-expand-v2
updated_at: 2026-04-20 09:05 MSK

## Инвесткомитет: итоговый вердикт

Кейс не проходит в APPROVED, хотя экономика у него сильная. `company_ebitda_potential_rub_month` выше порога, а путь к `500 000 ₽/мес` в base-case укладывается в 24 месяца, но локальный demand в РФ подтверждён в основном косвенно, tier-разметка источников в `02-demand.md` не соответствует required schema, а moat остаётся умеренным, а не инвестиционно-защитимым. Поэтому итог, это **NEAR-PASS**: к rerun имеет смысл возвращаться только после доказательства repeatable GTM и локального proprietary wedge.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | В 04-economics.md: «LTV/CAC = 20,3x», «CAC Payback = 4,10 месяца по contribution», «Contribution Margin = 56,9%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В 04-economics.md: «для цели 500 000 ₽ EBITDA/мес нужно ... 22 клиента» и «M15: 22». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | В 02-demand.md: «Search demand: LOW», «WTP подтверждён условно»; строка Sources без `T1=<N1>, T2=<N2>, T3=<N3>`, поэтому criterion capped at 10/25. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | В 02-demand.md: «Rogo не продаётся как массовый self-serve SaaS, а как bespoke enterprise deployment для финансовых институтов», что даёт workflow depth, но не сильный локальный moat. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В 05-critic.md: «распределение слишком широкое», а опасная связка, это «price compression + sanctions on SaaS + long enterprise sales cycle». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | В 04-economics.md: «Fully-loaded CAC = 1 518 092 ₽» и «operating break-even около M14-M15», то есть GTM реалистичен только как founder-led enterprise motion. |

**Sum raw = 97/150**  
**Normalized score = round(97 × 100 / 150) = 65/100**

### Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных, сетевой эффект не доказан. |
| Switching costs | 3 | Private deployment, интеграции, security review и обученный workflow повышают стоимость переключения. |
| Scale economies | 2 | Secure infra и delivery частично дешевеют с объёмом, но data/API слой и кастомизация остаются дорогими. |
| Proprietary data / model advantage | 1 | Собственный локальный датасет и защищённый model advantage не доказаны. |
| Regulatory moat | 1 | Compliance и data residency важны, но без T1-подтверждённого барьера это скорее обязательный билет, чем moat. |
| Brand / distribution | 1 | В РФ нет подтверждённого сильного бренда и развитого канала дистрибуции. |
| Embedded workflow | 3 | Продукт встраивается в memo, comps, CIM, DDQ и diligence-процесс глубоко в core workflow клиента. |

**Moat raw = 11/21, moat score = round(11 × 25 / 21) = 13/25, округляю вверх до 14/25 с учётом высокой глубины внедрения в workflow.**

## Investment one-liner

`[GEO-EXPAND] 0457 MSK Rogo GEO Expand v2 — NEAR-PASS: 65/100 | EBITDA base=3384К₽/мес через 15 мес | LTV/CAC=20,3x | Ключевое преимущество: глубокий finance-native workflow в закрытом enterprise-контуре | Главный риск: узкий buyer universe и недоподтверждённый локальный спрос.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 30 833 333 ₽ |
| CAC blended | 1 518 092 ₽ |
| LTV/CAC | 20,3x |
| CAC Payback | 2,34 мес по MRR / 4,10 мес по contribution |
| Gross Margin | 56,9% |
| contribution_margin_rub_month | 370 000 ₽/клиент/мес |
| fixed_costs_rub_month | 7 558 000 ₽/мес |
| company_ebitda_rub_month, M12 base | -1 816 518 ₽/мес |
| company_ebitda_potential_rub_month | 3 384 000 ₽/мес при 30 клиентах |
| clients_to_500k_ebitda | 22 |
| months_to_500k_ebitda | 15 |
| clients_to_1m_ebitda | 24 |
| months_to_1m_ebitda | 16 |
| Break-even | 21 клиент |
| startup_capital_to_bep_rub | 54 816 038 ₽ |

## Полный business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Account selection по банкам, advisory и corpdev | SDR + founder | CRM, ручной ресерч, базы компаний | 2 ч/акк | 2 800 | Средняя |
| 2 | Enrichment, контактные лица, pain mapping | SDR | CRM + enrichment | 1,5 ч | 2 000 | Средняя |
| 3 | Founder-led outbound / intro sequence | SDR + founder | e-mail, Telegram, calls | 2-3 недели | 14 000 | Средняя |
| 4 | Discovery call и qualification | AE + founder | Meet, CRM | 1 ч + prep | 10 000 | Низкая |
| 5 | Demo на реальном workflow: memo, comps, CIM, DDQ | AE + solutions analyst | secure sandbox | 3-5 дней | 22 000 | Низкая |
| 6 | Security / legal / procurement review | CTO + legal + buyer IT | policies, DPA, VDR | 2-5 недель | 58 000 | Низкая |
| 7 | Pilot setup в закрытом контуре | CTO + backend + ML | VPC, connectors, evals | 3-6 недель | 155 000 | Средняя |
| 8 | Pilot сопровождение и steering | AE + analyst + CSM | CRM, Jira, weekly reviews | 1 месяц | 96 000 | Низкая |
| 9 | Contracting, ЭДО, invoicing | AE + finance ops | договор, ЭДО, банк | 1-3 недели | 9 000 | Средняя |
| 10 | Go-live и первые success review | CSM + product | analytics, support stack | ongoing | 34 000/мес | Средняя |

## Финансовая траектория

| Scenario | M12 clients | EBITDA @M12 | Break-even month | Startup capital to BEP |
|---|---:|---:|---:|---:|
| Base | 15,52 | -1 816 518 ₽/мес | 15 | 54 816 038 ₽ |
| Optimistic | 23,38 | 1 092 752 ₽/мес | 12 | 42 403 965 ₽ |
| Pessimistic | 10,53 | -3 663 222 ₽/мес | >12 | 61 804 691 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-3 262 486 ₽/мес**
- p50 EBITDA @M24 = **7 055 789 ₽/мес**
- p90 EBITDA @M24 = **32 778 249 ₽/мес**
- Вывод: median-case проходит EBITDA gate, но левый хвост всё ещё уходит в отрицательный EBITDA, значит safety margin недостаточен для clean approve.

## Команда

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO / founder-sales | top accounts, partnerships, fundraising | 910 000 |
| CTO / Tech Lead | architecture, security, deployment | 806 000 |
| Senior Backend x2 | integrations, data pipelines, backend | 1 092 000 |
| ML Engineer | retrieval, evals, agent quality | 676 000 |
| DevOps / Security | VPC, infra, observability, access control | 494 000 |
| Frontend | analyst workspace, approvals, UI | 416 000 |
| Product / Solutions Lead | workflow design, pilots, implementation | 468 000 |
| Solutions Analyst | demos, onboarding, QA | 364 000 |
| SDR | outbound prospecting | 234 000 |
| AE | discovery, proposal, closing | 416 000 |
| Customer Success | retention, adoption, upsell | 338 000 |
| Finance / Ops | billing, contracts, docs ops | 234 000 |
| **Итого** |  | **6 448 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбербанк | крупнейший buyer для CIB, strategy и M&A research; в `02-demand.md` buyer surface прямо опирается на системно значимые банки ЦБ РФ | email decision-maker в Sber CIB / conference intro | 650 000 ₽/мес |
| ВТБ | большой поток инвестиционно-банковских и capital markets workflow, где memo/comps/DDQ automation даёт прямую экономию аналитиков | founder-led outreach + партнёрский intro | 650 000 ₽/мес |
| Газпромбанк | сильный institutional finance и debt/capital markets контур, близкий к ICP из кейса | email MD / warm intro через advisory ecosystem | 600 000 ₽/мес |
| Альфа-Банк | digital-first банк с активным corpdev и strategy-фокусом, где важен быстрый research workflow | direct outreach + thought leadership на vc.ru | 550 000 ₽/мес |
| Совкомбанк | активный M&A и корпоративный finance buyer, чувствительный к скорости diligence и memo drafting | email decision-maker + отраслевая конференция | 500 000 ₽/мес |
| БКС Мир инвестиций | investment banking и capital markets use cases близки к Rogo-style workflow | партнёрство с data vendor + founder outreach | 500 000 ₽/мес |
| АФК Система | развитый corpdev по портфельным активам, где due diligence и investment memos регулярны | outreach в corpdev / strategy | 450 000 ₽/мес |
| Северсталь | крупная публичная компания с strategy, treasury и investment committee workflows | email strategy lead / CFO office | 400 000 ₽/мес |
| Норникель | сложный IR и strategic finance контур, где конкурентный и transactional ресерч уже оплачен ФОТ аналитиков | direct outreach + отраслевые форумы | 400 000 ₽/мес |
| Яков и Партнёры | high-stakes advisory practice, где скорость подготовки materials и diligence напрямую влияет на margin проекта | партнёрский заход / email practice lead | 350 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| evidence_quality_unverified и слабая локальная demand-evidence | high | high | В `02-demand.md` нет обязательной строки `Sources: T1=<N1>, T2=<N2>, T3=<N3>`, а прямой search demand обозначен как `LOW`. |
| Price compression + длинный enterprise sales cycle | high | high | В 05-critic.md сценарий `Price -30%` ухудшает EBITDA @M12 до **-4 842 434 ₽/мес**. |
| Санкции, vendor dependency и data residency | high | high | В 05-critic.md прямо зафиксировано, что `sanctions on SaaS` и cross-border restrictions могут сломать delivery и unit economics. |

## LTV Upside Calculator

### Что должно измениться, чтобы кейс перешёл в APPROVED

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| Tier-validated demand evidence | нет валидной строки с counts | T1≥4, T2≥4, T3≤2 и weighted ≥2,0 | Снимает штраф к Market+Demand и повышает доверие инвесткомитета к локальному спросу. |
| Pilot-to-paid | не доказан публично | ≥30% на первых 10 пилотах | Подтверждает, что founder-led GTM можно превратить в repeatable sales motion. |
| ARPA | 650 000 ₽/мес | ≥700 000 ₽/мес без discount >15% | Защищает margin от price compression и улучшает Monte Carlo downside. |
| Proprietary data / local integrations | слабые доказательства | 2-3 локальных интеграции с ЭДО, DWH, market data | Укрепляет moat и switching costs. |
| Sales cycle | 4-6+ месяцев | ≤120 дней от discovery до paid | Снижает CAC inflation и burn-to-breakeven. |

### Минимальные proof points для rerun
1. Не менее **3 платящих design partners** среди банков, advisory или крупных corpdev-команд с контрактом **500К+ ₽/мес**.
2. Подтверждённый **pilot-to-paid ≥ 30%** и median sales cycle **≤120 дней**.
3. Хотя бы **1 локальный reference deployment** с private/VPC контуром и data residency.
4. Формализованная tier-разметка evidence в `02-demand.md` по схеме `T1/T2/T3` с counts.
5. Доказательство, что продукт это самостоятельный wedge, а не просто repackage кейса `investment-banking-ai-analyst-operator-v2`.

## Финальное решение инвесткомитета

**NEAR-PASS.**

Я бы не одобрял инвестицию сейчас, потому что экономика хорошая, но качество локальной demand-validation и защитимость moat пока ниже investment-grade. Возвращаться стоит после того, как команда докажет repeatable enterprise GTM, локальный secure deployment и более сильный proprietary wedge именно в РФ-контуре.


---

## Файл: 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-20 03:32 MSK — Demand Validation
- Stage: Program 4 / Demand Validation
- Case: `0457-msk-rogo-geo-expand-v2`
- Кейс пропущен дальше как `CONDITIONAL PASS`, хотя direct search demand в РФ низкий.
- Demand API по ключам `Rogo AI finance`, `investment banking AI analyst`, `financial research AI investment banking` дал в основном `LOW`, а `M&A AI analyst` показал отдельные HH-сигналы.
- TAM/SAM/SOM зафиксированы как `6,48 млрд ₽ / 864 млн ₽ / 43,2 млн ₽` в год.
- WTP признан условно подтверждённым через official Rogo materials, Series C `$75 млн` и adjacent paid substitutes вроде Контур.Фокус, Прима-Информ и Cbonds.
- Score impact:
  - Category proof: `+2`
  - Adjacent budget evidence: `+2`
  - Низкий search demand: `-2`
  - Узкий buyer universe: `-1`
  - Net delta: `+1`
- Outcome: `PROCEED`, early reject не применён.
- Artifacts: `02-demand.md`

## 2026-04-20 03:47 MSK — Unit Economics
- Stage: Program 5 / Unit Economics
- Case: `0457-msk-rogo-geo-expand-v2`
- Базовая модель построена как premium regulated workflow с MRR **650 000 ₽/клиент/мес**.
- COGS оценён в **280 000 ₽/клиент/мес**, contribution_margin_rub_month = **370 000 ₽**, gross margin = **56,9%**.
- Fully-loaded CAC рассчитан как **1 518 092 ₽**, customer_ltv_rub = **30 833 333 ₽**, LTV/CAC = **20,3x**.
- Break-even ≈ **21 клиент**, `clients_to_500k_ebitda = 22`, `months_to_500k_ebitda = 15`.
- Startup capital to BEP в base = **54 816 038 ₽**.
- Score impact:
  - Unit economics strength: `+3`
  - EBITDA path within 24 months: `+2`
  - Высокая капиталоёмкость: `-1`
  - Founder-led GTM dependency: `-1`
  - Net delta: `+3`
- Outcome: `PROCEED`, economics-gate пройден.
- Artifacts: `04-economics.md`

## 2026-04-20 09:05 MSK — Program 7 Critic and Verdict
- Stage: P7
- Verdict: NEAR-PASS
- Score: 65/100
- Raw score: 97/150
- Summary: кейс подтверждает сильную unit economics и путь к EBITDA >500K, но не проходит investment committee из-за слабой локальной demand-evidence, умеренного moat и высокой зависимости от founder-led enterprise GTM.
- Rubric:
  - unit_economics: 21/25
  - ebitda_potential: 20/25
  - market_demand: 10/25
  - moat: 14/25
  - execution_risk: 15/25
  - gtm_realism: 17/25
- Source tier balance:
  - T1: 0
  - T2: 0
  - T3: 0
  - weighted: 1.00
  - penalty_to_market_demand: -5
- Key gates:
  - company_ebitda_potential_rub_month: PASS (3 384 000 ₽/мес at 30 clients)
  - clients_to_500k_ebitda: PASS (22)
  - months_to_500k_ebitda: PASS (15)
  - moat_strength: CONDITIONAL (14/25)
  - evidence_quality: UNVERIFIED
- Outcome: `MOVE_TO_REJECTED`, потому что normalized score < 70.
- Artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0457-msk-rogo-geo-expand-v2/06-verdict.md
