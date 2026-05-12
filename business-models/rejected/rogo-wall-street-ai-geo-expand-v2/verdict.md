# Rogo Wall Street AI — Full Verdict Package
> Скомпилированный пакет стадий пайплайна для публикации в GitHub.
> Примечание: в этом кейсе отсутствуют `02-validation.md` и `03-demand.md`; фактическая demand-стадия представлена файлом `02-demand.md`.

---

## Файл: 00-brief.md

# Rogo Wall Street AI, geo-expand сигнал по AI-аналитике для investment banking

## Суть сигнала
Rogo ранее был учтён как supporting signal для существующего кейса, но по правилам resurrection должен пройти повторную полную оценку как отдельный standalone candidate.

## Почему берём в работу
- Сигнал относится к enterprise workflow с потенциально высоким чеком и длинным контрактом.
- В историческом triage уже были признаки коммерческого масштаба и сильной категории.
- Нужна новая независимая аналитика, даже если в финале кейс окажется близким к существующему.

## Следующий шаг
Передать кейс в P3-demand-validation и далее по полному пайплайну P3→P7.


---

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-rogo-wall-street-ai-geo-expand.md
created: 2026-04-21T15:56:07+03:00
original_verdict_source: triage/triage-2026-04-14-rogo-wall-street-ai-geo-expand.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — rogo-wall-street-ai-geo-expand

## Meta
- source: triage/triage-2026-04-14-rogo-wall-street-ai-geo-expand.md
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
2026-04-14

## Входные данные
- pipeline/raw/20260414T1927Z-rogo-wall-street-ai-geo-expand.md

## Классификация
поддерживающий сигнал для существующего кейса

## Решение
Обогатить существующий кейс: `investment-banking-ai-analyst-operator`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по теме AI-аналитика для investment banking, private equity и institutional finance команд.
- Новый raw-файл совпадает с кейсом по нише, buyer profile и типу enterprise-workflow: financial modeling, due diligence, investment memos, IC/IPO/deal materials.
- Сигнал не открывает новую категорию, а усиливает уже существующий кейс свежими коммерческими метриками и подтверждением масштаба категории.

## Что добавлено в кейс
- В `pipeline/cases/investment-banking-ai-analyst-operator/01-evidence.md` добавлен supporting signal по Forbes.
- Зафиксированы ключевые факты: рост выручки Rogo с $2 млн в 2024 до более $15 млн в 2025, 25 000+ пользователей в 150 фирмах и ориентир потенциального LTV для РФ на уровне 2,5-7,0 млн руб. в год на корпоративного клиента.

## Что сделано
- Кейc `investment-banking-ai-analyst-operator` обогащён новым доказательством.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это supporting signal для существующего high-LTV кейса: Rogo дополнительно подтверждает, что vertical AI для investment banking уже имеет выраженный enterprise traction и заслуживает дальнейшей разработки как сервисный бизнес под локализацию в РФ.

```



---

## Файл: 02-demand.md

---
stage: demand-validation
case: rogo-wall-street-ai-geo-expand-v2
date: 2026-04-23
analyst: branch-models-lead
sector: FINTECH
verdict: PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Rogo как AI-платформа для investment banking, private equity, corpdev и institutional finance workflow с локальным тезисом про GEO-expand в РФ.

## Итог
**Статус: PASS.**

На российском контуре прямой search demand по формулировкам уровня `investment banking ai` остаётся слабым, но underlying job-to-be-done подтверждён. В соседнем Rogo-кейсе по той же категории internal multi-demand давал **LOW / 3** для `investment banking ai`, а по более реальному workflow-запросу `инвестиционный аналитик` доходил до **MEDIUM / 30** с большим числом вакансий. Для этой категории это нормальный паттерн: бюджет рождается не из SEO, а из дорогого труда аналитиков, M&A/advisory workflow и длинных enterprise-продаж. [Internal case evidence]

Дополнительно 23 апреля 2026 года я повторно попытался сходить в обязательный endpoint `http://172.18.0.1:9001/multi-demand?keyword=...`, но все запросы (`инвестиционный банкинг`, `M&A аналитика`, `финансовая аналитика`) вернулись по timeout без данных. Поэтому в этом цикле использую ранее зафиксированные результаты по соседним Rogo-case и помечаю текущую проверку как технически недоступную. [Internal demand tool, endpoint timeout on 2026-04-23]

## 1) Что именно валидируем
Не generic AI-чат, а AI analyst copilot для high-finance workflow: comps, memo drafting, due diligence, screening, market maps, management materials, investment committee packs. Buyer в РФ, если он существует, это не массовый retail и не SMB, а узкий пул инвестбанков, брокеров, управляющих компаний и corpdev/M&A-команд крупных групп. [T2]

## 2) Demand signals
- Обязательный internal endpoint `multi-demand` на **2026-04-23** по трём проверочным запросам не ответил и вернул timeout, то есть новых внутренних demand-данных в этом цикле нет. [Internal demand tool]
- В соседнем demand-файле по той же категории ранее был зафиксирован результат `investment banking ai` = **LOW / 3** и `инвестиционный аналитик` = **MEDIUM / 30**. Это подтверждает слабый спрос на AI-label и живой спрос на underlying роль/workflow. [Internal case evidence]
- Банк России публикует широкую адресуемую базу regulated finance buyers: **311 кредитных организаций**, **497 профессиональных участников рынка ценных бумаг** и **341 управляющая компания**. Не все они купят Rogo-like продукт, но это уже >1 тыс. организаций в ядре финансового контура. [T1]
- AK&M по итогам 2025 года фиксировал **399 сделок M&A с российскими активами** на **$41.12 млрд**, то есть сам deal-flow и advisory workload в стране сохраняются. [T2]
- Официальный анонс Rogo от **28 января 2026 года** сообщает о **$75 млн Series C**, суммарном финансировании **$165 млн+**, **25 000+ financial professionals using Rogo daily** и клиентах уровня **Rothschild & Co, Moelis, Nomura, Lazard, GTCR**. Это сильный category-validity signal. [T2]

## 3) Конкуренты и цены
### Реальные конкуренты / близкие substitutes с публичными ценами
1. **Koyfin** — Plus **$39/мес**, Premium **$79/мес**, Advisor Core **$209/мес**, Advisor Pro **$299/мес**. Official pricing page. Это lower-end research workstation anchor. [T2]
2. **TIKR** — Free **$0**, Plus **$24.95/мес**, Pro **$54.95/мес**. Official pricing page. Это pricing anchor для аналитического research stack. [T2]
3. **Finviz Elite** — **$39.50/мес**, annual effective **$24.96/мес**, lifetime **$299.50**. Official pricing page. Это дешёвый public-markets research substitute. [T2]

### Интерпретация
- Уже существует нормализованная подписочная трата на research tooling на уровне **$25-299/мес за пользователя**. [T2]
- Rogo продаёт не retail terminal, а secure team workflow для investment memo/comps/diligence, поэтому локальный якорь цены должен быть выше, примерно **250-600 тыс. руб./мес за команду** плюс onboarding/integration. Это inference из публичных global anchors и стоимости времени finance-команд. [T2 + inference]

## 4) Telegram в РФ: боты и сервисы
- Прямого Telegram-native enterprise AI-конкурента под investment banking / corpdev в РФ я не нашёл. [T3, спекуляция с оговоркой]
- На рынке есть в основном adjacent Telegram-сервисы: retail-investing каналы, брокерские сигнальные боты, новостные и алертинговые продукты. Это подтверждает наличие интереса к финаналитике в Telegram как канале, но не наличие сильного direct competitor именно в IB workflow. [T3]
- Следовательно, Telegram-контур в РФ показывает либо раннюю стадию категории, либо отсутствие сформированного локального лидера. Для Rogo-like wedge это скорее плюс, чем минус. [T3 + inference]

## 5) WTP, proof of willingness to pay
### Что подтверждает готовность платить
- Платные research terminals и screeners уже давно существуют и живут на recurring pricing, значит spending line за аналитику нормализована. [T2]
- В историческом triage по исходному Rogo-сигналу уже был зафиксирован ориентир потенциального LTV для локального клиента **2.5-7.0 млн руб. в год**. Это не бухгалтерский факт, а рабочий диапазон, но он согласуется с observed enterprise motion. [Internal case context]
- OpenAI в кейсе про Rogo писала, что ещё после выхода из stealth продукт обслуживал **5 000+ bankers**, экономил аналитикам **10+ часов в неделю** и увеличил ARR в **27 раз**. Это не независимый аудит, но сильный proof, что buyers реально платят за экономию analyst-hours. [T2]
- На фоне активного найма инвестиционных аналитиков и сохраняющегося M&A/deal workload логика замещения части дорогого ручного труда бюджетом в **3.6-7.2 млн руб./год** выглядит правдоподобной. [T2 + inference]

### Вывод по WTP
WTP **есть**, но только в узком верхнем сегменте. Для retail, small advisory shops и широкого SMB подтверждения нет. Для крупных банков, брокеров, УК и corpdev-команд цена **300-600 тыс. руб./мес** выглядит реалистично; для secure deployment и white-glove rollout возможен уровень **700 тыс. - 1.0 млн руб./мес**. [T2 + inference]

## 6) Market sizing
### Логика сегмента
Считаем не весь fintech, а узкий рынок **AI analyst/copilot for investment research, deal screening, comps, memo and diligence workflows** в РФ.

### Top-down
**[LOW CONFIDENCE]** Публичного чистого глобального TAM по этой подкатегории почти нет, поэтому top-down строится через категорийный proxy и затем режется по сегменту.

- В соседнем ранее оценённом кейсе по той же вертикали использовался глобальный proxy порядка **$2.3 млрд** для investment research / financial analytics software. Это low-confidence оценка, поэтому использую её лишь как направляющий ориентир. [T3]
- В российском regulated-finance universe Банк России даёт **1149** организаций в ядре addressable-base = 311 banks + 497 prof participants + 341 management companies. [T1]
- Если принять, что только **30%** этого universe потенциально вообще addressable для broader TAM и annual budget на Rogo-like решение составляет **4.8 млн руб./год**, то **TAM РФ ≈ 1.65 млрд руб.** = 1149 × 30% × 4.8 млн. [T1/T2 + inference]
- Для реального segment-fit в горизонте 3 лет беру **10%** universe, тогда **SAM_top-down ≈ 551.5 млн руб.** [T1/T2 + inference]
- Реалистичный capture: **Y1 = 3% SAM**, **Y3 = 10% SAM**. Тогда **SOM Y1 ≈ 16.5 млн руб.**, **SOM Y3 ≈ 55.1 млн руб.** [inference]

### Bottom-up
Строю от реальных buyers в РФ.

#### 10 реальных buyers
1. Сбер CIB [T2]
2. ВТБ [T2]
3. Альфа-Банк CIB [T2]
4. Газпромбанк [T2]
5. БКС Мир инвестиций [T2]
6. Атон [T2]
7. Совкомбанк / Sovcombank CIB [T2]
8. УК Первая [T2]
9. УК Альфа-Капитал [T2]
10. Т-Капитал [T2]

#### Расчёт
- Беру **150** достижимых buyers в первые 3 года: крупные банки, брокеры, УК, plus corpdev/M&A-команды крупных групп. [T1/T2 + inference]
- `% with need` = **25%**. Это доля организаций с реально повторяющимся research/deal workflow и budget authority. [T2 + inference]
- `ARR avg` = **4.8 млн руб./год**. Это эквивалент **400 тыс. руб./мес** на команду, что находится внутри WTP-коридора. [T2 + inference]

Тогда:
- **SAM_bottom-up = 150 × 25% × 4.8 млн = 180 млн руб.**
- Для расширенного слоя corpdev/M&A добавляю ещё **150** крупных нефинансовых групп с attach-rate **15%**, это ещё **108 млн руб.** [T2 + inference]
- Итого **SAM_bottom-up = 288 млн руб.**
- **SOM_bottom_up Y1 = 5% × 288 млн = 14.4 млн руб.**
- **SOM_bottom_up Y3 = 15% × 288 млн = 43.2 млн руб.**

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $2.3B [T3] | — | Proxy only, низкая точность | top-down |
| TAM (РФ) | 1.65 млрд ₽ [T1/T2+inf] | 0.96 млрд ₽ [T1/T2+inf] | diff=1.7x, bottom-up жёстче режет corpdev | lower |
| SAM (РФ) | 551.5 млн ₽ [T1/T2+inf] | 288 млн ₽ [T1/T2+inf] | diff=1.9x, приемлемо | lower |
| SOM Y1 | 16.5 млн ₽ | 14.4 млн ₽ | diff=1.15x | **используем 14.4 млн ₽** |
| SOM Y3 | 55.1 млн ₽ | 43.2 млн ₽ | diff=1.28x | **используем 43.2 млн ₽** |

### Sanity check
- Preferred SOM Y1 = **14.4 млн руб.** при ACV **4.8 млн руб.** означает примерно **3 клиента** в год 1, что реалистично для founder-led enterprise motion.
- Даже при sales cycle **6-9 месяцев** три сделки за год выглядят достижимо.
- SOM Y1 заметно ниже 10% SAM, red flag overclaiming нет.

## 7) Profit Gate, EBITDA >= 500k руб./мес
Проверяю все основные сценарии монетизации.

### Сценарий A, self-serve seats
- Цена: **25 тыс. руб./мес за seat**
- 40 seat-equivalent
- Выручка: **1.0 млн руб./мес**
- Валовая прибыль при GM 85%: **0.85 млн руб./мес**
- При OPEX 1.8-2.2 млн руб./мес EBITDA отрицательная
- **Gate: FAIL**

### Сценарий B, team plan для бутик-команд
- Цена: **150 тыс. руб./мес**
- 10 клиентов
- Выручка: **1.5 млн руб./мес**
- Валовая прибыль при GM 80%: **1.2 млн руб./мес**
- При OPEX 1.8-2.2 млн руб./мес EBITDA отрицательная или около нуля
- **Gate: FAIL / borderline**

### Сценарий C, enterprise secure SaaS
- Цена: **400 тыс. руб./мес**
- 8 клиентов
- Выручка: **3.2 млн руб./мес**
- Валовая прибыль при GM 78%: **2.5 млн руб./мес**
- При OPEX 1.9-2.2 млн руб./мес EBITDA: **0.3-0.6 млн руб./мес**
- **Gate: PASS, но на нижней границе**

### Сценарий D, enterprise + onboarding/integration
- Цена: **500 тыс. руб./мес эквивалент + 1.5 млн руб. onboarding**, усреднённо **625 тыс. руб./мес** в первый год
- 6 клиентов
- Выручка: **3.75 млн руб./мес эквивалент**
- Валовая прибыль при GM 72%: **2.7 млн руб./мес**
- При OPEX 2.0-2.4 млн руб./мес EBITDA: **0.3-0.7 млн руб./мес**
- **Gate: PASS**

### Итог по Profit Gate
Profit Gate **проходит**, но только как дорогой enterprise/high-trust продукт. В seat-based и mid-market моделях кейс не бьётся.

## 8) Риски
1. Узкий buyer universe, значит потолок РФ-only истории ограничен. [T1/T2]
2. Длинный procurement cycle, требования к ИБ и приватности данных. [T2]
3. Feature substitution через Excel, Cbonds, СПАРК, Интерфакс, Bloomberg-like workflow и внутренних аналитиков. [T2 + inference]
4. Telegram/RU не показывает явного лидера категории, но это может означать не только окно возможностей, но и сырость рынка. [T3]

## 9) Инвестиционная интерпретация
Это не broad SaaS. Это узкий enterprise wedge для дорогих finance workflows. Для фонда кейс выглядит живым, если ставка делается на few-large-accounts GTM, secure deployment, data integrations и workflow lock-in. Для PLG/массового retail сценария кейс слабый.

## Финальный вывод
- **Demand:** низкий по AI-ярлыку, но достаточный на уровне реального job-to-be-done.
- **Competitor pricing:** есть, рынок за аналитику уже платит.
- **Telegram/RU:** прямой конкурентный слой слабый.
- **TAM/SAM/SOM:** рынок РФ не огромный, но достаточный для прибыльной enterprise-модели.
- **WTP:** подтверждён.
- **Profit Gate:** проходит только в enterprise/hybrid monetization.

**Решение на этапе demand validation: PASS.**

## Источники
- Банк России, банковский сектор: https://www.cbr.ru/banking_sector/ [T1]
- Банк России, профессиональные участники рынка ценных бумаг: https://www.cbr.ru/securities_market/registries/ [T1]
- Банк России, управляющие компании: https://www.cbr.ru/RSCI/registers/ [T1]
- AK&M, итоги рынка M&A с российскими активами за 2025 год: https://www.akm.ru/news/ak_m_vypustilo_itogi_rynka_m_a_s_rossiyskimi_aktivami_za_2025_god/?sphrase_id=455401 [T2]
- Rogo, Series C and European expansion, 2026-01-28: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion [T2]
- OpenAI, Rogo scales AI-driven financial research with OpenAI o1: https://openai.com/index/rogo/ [T2]
- Koyfin pricing: https://www.koyfin.com/pricing/ [T2]
- TIKR pricing: https://www.tikr.com/pricing [T2]
- Finviz Elite pricing: https://finviz.com/elite.ashx [T2]
- Global proxy, investment research software market: https://www.verifiedmarketreports.com/product/investment-research-software-market/ [T3]
- Internal demand endpoint attempts on 2026-04-23: `инвестиционный банкинг`, `M&A аналитика`, `финансовая аналитика` all timeout [Internal demand tool]

Sources: T1=3, T2=6, T3=2. Primary evidence basis: T2.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-10: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.


---

## Файл: 04-economics.md

---
stage: unit-economics
case: rogo-wall-street-ai-geo-expand-v2
date: 2026-05-11
analyst: branch-models-lead
sector: FINTECH
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Rogo-like enterprise AI copilot для investment banking, private equity, corpdev и institutional finance workflow в РФ: secure deployment, white-glove onboarding, длинный sales cycle, regulated buyer.

## Executive summary

**Статус: PASS.**

С точки зрения фонда кейс экономически бьётся только как дорогой enterprise B2B SaaS с внедрением и высоким ACV. В PLG/self-serve логике не бьётся. При рабочем чеке **450 тыс. ₽ MRR на клиента** и fully-loaded blended CAC **1.70 млн ₽** модель даёт:

- **COGS / клиент / месяц:** 95 тыс. ₽
- **Contribution Margin:** **78.9%**
- **Monthly logo churn benchmark:** **1.5%/мес**
- **LTV:** **23.7 млн ₽**
- **LTV/CAC:** **13.9x**
- **CAC payback:** **3.8 мес**
- **Break-even:** **21 клиента** на fixed-cost basis или **26 клиентов** с включённым acquisition engine
- **EBITDA > 500 тыс. ₽/мес достижима задолго до 50 клиентов**

Инвестиционный вывод: юнит-экономика сильная на бумаге, но зависима от узкого buyer universe и sales execution. Это не масштабный SMB SaaS, а few-large-accounts business.

## 1) Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | банки, брокеры, УК, corpdev/M&A крупных групп | regulated / enterprise buyers |
| Средний чек подписки | 450 000 ₽/мес | внутри demand-диапазона 300–600 тыс. ₽/мес |
| Onboarding fee | 1 500 000 ₽ one-off | не включаю в MRR, считаю upside |
| Gross revenue per client/month | 450 000 ₽ | базовая unit-экономика |
| Variable COGS per client/month | 95 000 ₽ | модель + hosting + support + security ops |
| Gross profit per client/month | 355 000 ₽ | 450 000 - 95 000 |
| Contribution Margin | 78.9% | 355 000 / 450 000 |
| Sales cycle | 6–9 мес | enterprise fintech motion |
| New paying customers at scale | 1.18 / мес | ~14 клиентов в год |
| Segment CAC multiplier | x2.5 | regulated fintech / enterprise sanity rule |

## 2) Детальный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR | Snov.io, CBR registry, ручной research | 2 ч | 1 200 | средняя |
| 2 | Enrichment контактов | SDR | Snov.io, корпоративный email finder | 1 ч | 600 | высокая |
| 3 | Холодное касание email/LinkedIn/Telegram | SDR | Snov.io sequences, почта | 1.5 ч | 900 | высокая |
| 4 | Follow-up 1–3 | SDR | sequence automation + ручные ответы | 2 ч | 1 200 | высокая |
| 5 | Qualification call | SDR + AE | CRM, Meet | 1 ч | 2 200 | низкая |
| 6 | Demo под workflow клиента | AE + founder | Demo env, презентация | 1.5 ч | 4 500 | низкая |
| 7 | Discovery по use-cases и security | AE + CTO | Notion/CRM, чек-листы ИБ | 2 ч | 6 200 | низкая |
| 8 | Pilot scoping | CTO + ML Eng | sandbox, sample docs | 3 ч | 9 000 | низкая |
| 9 | Pilot deployment | ML Eng + Backend | cloud, vector DB, connectors | 12 ч | 31 000 | средняя |
| 10 | Pilot support и tuning | ML Eng + CSM | monitoring, prompt/config tools | 8 ч | 19 000 | средняя |
| 11 | Procurement / legal / DPA | AE + founder + legal | шаблоны договора, ЭДО | 6 ч | 18 000 | низкая |
| 12 | Security review | CTO + DevOps | IAM, logging, policy docs | 8 ч | 24 000 | низкая |
| 13 | Финальное коммерческое предложение | AE | CRM, CPQ/Excel | 1 ч | 2 600 | средняя |
| 14 | Счёт и закрывающие документы | Finance ops | 1С/МойСклад/ЭДО | 0.5 ч | 700 | высокая |
| 15 | Оплата | Клиент | bank transfer | 7–30 дней | 0 | высокая |
| 16 | Onboarding и enablement | CSM + AE + ML Eng | knowledge base, trainings | 10 ч | 26 000 | средняя |

### Вывод по процессу
Самые дорогие шаги не в lead-gen, а в **pilot + security + procurement**. Поэтому кейс требует enterprise multiplier для CAC и не должен оцениваться как обычный SaaS self-serve.

## 3) COGS breakdown на 1 клиента / месяц

| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / inference / reranking | 32 000 | консервативный лимит на heavy document workflows |
| Secure cloud + vector/storage | 18 000 | isolated workload, encrypted storage |
| Коннекторы / ingestion / ETL | 12 000 | загрузка документов, индексация, sync |
| Monitoring / logging / observability | 6 000 | per-tenant аллокация |
| Support engineer / ML tuning | 20 000 | ~0.04 FTE на активного клиента |
| Customer Success variable layer | 4 000 | QBR, обучение, ответы |
| Security ops / резерв на инциденты | 3 000 | IAM, audit trail, access review |
| Billing / docs / bank fees | 0 000 | несущественно, округлено в admin |
| **Итого COGS** | **95 000** |  |

**Выручка на клиента:** 450 000 ₽/мес  
**Валовая прибыль на клиента:** 355 000 ₽/мес  
**Contribution Margin:** **78.9%**

## 4) Fully-loaded CAC

### 4.1 Формула

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Marketing FOT allocation + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers`

### 4.2 Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс/VC/нишевые placements) | 250 000 | точечный account-based demand capture, не mass performance | модель фонда, conservative assumption |
| Outbound team FOT (SDR + AE attributed to new) | 754 000 | SDR 180k gross x1.3 + AE 400k gross x1.3 | HH.ru вакансии SDR и AE |
| Marketing team FOT (partial allocation) | 182 000 | 0.5 FTE product marketing 280k gross x1.3 | внутренняя аллокация по enterprise GTM |
| Tools (CRM, sequencing, data) | 110 000 | Bitrix24 + Snov.io + прочий stack | Bitrix24 pricing, Snov.io pricing |
| Events / partnerships | 400 000 | отраслевые roundtables, small private events, travel | модель фонда для enterprise fintech |
| Overhead multiplier (x1.3) | 509 000 | 30% к subtotal 1.696 млн ₽ | стандарт enterprise B2B / regulated sales motion |
| **Итого fully-loaded acquisition spend / мес** | **2 205 000** |  |  |

### 4.3 New paying customers

На зрелом темпе беру **1.30 новых paying customers / месяц**. Это эквивалент **15.6 клиента в год**, что для founder-led enterprise motion агрессивно, но ещё реалистично.

### 4.4 Blended CAC

**Blended fully-loaded CAC = 2 205 000 / 1.30 = 1 696 154 ₽ ≈ 1.70 млн ₽ на нового платящего клиента.**

### 4.5 CAC по каналам и funnel conversion

| Канал | Вход потока | Следующий шаг | SQL / pilot | Won | Конверсия lead→won | Spend / мес, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 1 200 target accounts | 96 first meetings | 24 pilots / proposals | 1.00 | 0.083% | 1 430 000 | 1 430 000 |
| Партнёрства / отраслевые ивенты | 30 тёплых интро | 9 meetings | 4 pilots | 0.20 | 0.67% | 585 000 | 2 925 000 |
| Inbound content / PR | 40 inbound leads | 10 discovery | 4 SQL | 0.05 | 0.13% | 190 000 | 3 800 000 |
| **Blended** | — | — | — | **1.25** | — | **2 205 000** | **1 764 000** |

Примечание: blended по каналам чуть выше, чем базовый 1.70 млн ₽, из-за округления win-rate. Для модели использую **1.70–1.76 млн ₽** как рабочий коридор.

### 4.6 Sanity check against RU benchmarks

- База из задания: **Fintech B2B в РФ 200–700k ₽/клиент**, но для **regulated / enterprise** допускается multiplier **x2.5–3.0**.
- Наш raw CAC до multiplier = **1.696 млн / 1.3 ≈ 1.30 млн ₽**.
- Это заметно выше generic fintech benchmark, но объяснимо, потому что здесь не обычный fintech SaaS, а **enterprise AI с pilot, security review, legal и procurement-heavy motion**.
- Красный флаг “слишком дешёвого CAC” здесь отсутствует, наоборот модель скорее консервативна.

## 5) LTV и churn rate

### 5.1 Churn benchmark

Для enterprise B2B SaaS бенчмарк Optifai за Q2 2025 – Q1 2026 показывает **1–2% monthly churn** для enterprise сегмента. Для Rogo-like secure finance workflow беру **1.5%/мес** как консервативную середину диапазона.

### 5.2 LTV calculation

| Параметр | Значение |
|---|---:|
| ARPA / month | 450 000 ₽ |
| Gross profit / month | 355 000 ₽ |
| Monthly logo churn | 1.5% |
| Expected customer lifetime | 66.7 мес |
| **LTV** | **23 666 667 ₽** |

Формула: `LTV = Gross profit per month / monthly churn = 355 000 / 0.015`

## 6) LTV/CAC ratio

| Метрика | Значение |
|---|---:|
| LTV | 23.67 млн ₽ |
| CAC | 1.70 млн ₽ |
| **LTV/CAC** | **13.9x** |

**Вывод:** сильно выше минимального investable threshold **3.0x**. Главный риск тут не unit economics, а ограниченная ёмкость рынка и execution risk по сложным сделкам.

## 7) CAC Payback

| Параметр | Значение |
|---|---:|
| CAC | 1.70 млн ₽ |
| MRR per customer | 450 000 ₽ |
| Payback on revenue basis | 3.8 мес |
| Payback on gross profit basis | 4.8 мес |

Формула sanity check из задания: `CAC Payback = CAC / MRR_per_customer = 1.70 млн / 450k = 3.8 мес`

Это лучше, чем требование **<18 мес** для enterprise.

## 8) Full team table

| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Ramp до 80% productivity, мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | продажи, fundraising, ключевые клиенты | 1 | 700 000 | 0 | 0 | 210 000 | 910 000 |
| CTO / Tech Lead | архитектура, security review, roadmap | 1 | 600 000 | 2.5 | 2 | 180 000 | 780 000 |
| Senior Backend | ingestion, APIs, auth, enterprise controls | 2 | 450 000 | 1.5 | 1.5 | 270 000 | 1 170 000 |
| ML Engineer | retrieval, evals, prompts, tuning | 2 | 500 000 | 2.5 | 2 | 300 000 | 1 300 000 |
| DevOps | infra, observability, IAM | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | analyst UI, admin panels | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | outbound prospecting | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| AE | demo, pilot, close | 1 | 400 000 | 1.5 | 2.5 | 120 000 | 520 000 |
| Customer Success | onboarding, adoption, renewals | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| **Итого** |  | **11** |  |  |  |  | **6 071 000 ₽/мес** |

### Комментарий по источникам зарплат
Берусь за диапазоны, согласованные с заданием, и калибрую их по HH.ru вакансии/сводкам: senior backend, ML engineer, DevOps, SDR, AE, CSM, CTO. Для enterprise AI в Москве/СПб взяты значения ближе к медиане верхней половины диапазона.

## 9) Hiring realism и cumulative FOT timeline M1–M12

### 9.1 План найма

| Месяц | Кто подключается | Комментарий |
|---|---|---|
| M1 | CEO, CTO | founder-led старт, без mass hiring |
| M2 | Backend #1 | core platform |
| M3 | Backend #2, SDR | закрываем delivery и начинаем outbound |
| M4 | ML #1 | pilot quality |
| M5 | Frontend | analyst workflow UI |
| M6 | AE | когда уже есть pipe и demo motion |
| M7 | DevOps | растёт security/performance pressure |
| M8 | ML #2 | масштабирование pilot→prod |
| M9 | Customer Success | первые live accounts и renewals |
| M10-M12 | pause hiring | сначала доказываем продажу и удержание |

### 9.2 FOT monthly M1–M12

| Месяц | FOT fully-loaded, ₽/мес |
|---|---:|
| M1 | 1 690 000 |
| M2 | 2 275 000 |
| M3 | 3 094 000 |
| M4 | 3 744 000 |
| M5 | 4 134 000 |
| M6 | 4 654 000 |
| M7 | 5 109 000 |
| M8 | 5 759 000 |
| M9 | 6 071 000 |
| M10 | 6 071 000 |
| M11 | 6 071 000 |
| M12 | 6 071 000 |

Sanity check пройден:
- в M1 нет 5+ наймов,
- FOT для зрелой 11-чел команды > 6 млн ₽/мес, значит явной недооценки нет.

## 10) Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded | 6 071 000 |
| Core software / dev tools / workspace | 120 000 |
| Office / coworking / admin | 180 000 |
| Legal / accounting / HR ops | 140 000 |
| Security / audit reserve / compliance docs | 250 000 |
| Travel / executive BD | 180 000 |
| Misc reserve | 120 000 |
| **Итого fixed costs** | **7 061 000** |

Если включать growth acquisition engine как обязательный operating layer, то:

`Fixed + acquisition = 7.061 млн + 2.205 млн = 9.266 млн ₽/мес`

## 11) Break-even

### 11.1 Break-even по количеству клиентов

| Режим | Формула | Клиентов |
|---|---|---:|
| Без acquisition engine | 7 061 000 / 355 000 | 19.9 |
| С acquisition engine | 9 266 000 / 355 000 | 26.1 |

**Округляю:**
- **20 клиентов** для operating break-even,
- **27 клиентов** для full-growth break-even.

### 11.2 Break-even по месяцам

Модель ramp активных клиентов:

| Месяц | Активные клиенты | GP, ₽/мес |
|---|---:|---:|
| M1-M6 | 0 | 0 |
| M7 | 1 | 355 000 |
| M8 | 3 | 1 065 000 |
| M9 | 6 | 2 130 000 |
| M10 | 11 | 3 905 000 |
| M11 | 18 | 6 390 000 |
| M12 | 27 | 9 585 000 |

**Итог:**
- operating break-even проходит между **M11 и M12**,
- full-growth break-even достигается в **M12**.

## 12) Burn-to-breakeven

Приближённая модель net burn с учётом non-payroll fixed costs и постепенного запуска acquisition:

| Месяц | Операционные затраты, ₽ | GP, ₽ | Net burn / profit, ₽ |
|---|---:|---:|---:|
| M1 | 2 100 000 | 0 | -2 100 000 |
| M2 | 2 700 000 | 0 | -2 700 000 |
| M3 | 3 650 000 | 0 | -3 650 000 |
| M4 | 4 300 000 | 0 | -4 300 000 |
| M5 | 4 750 000 | 0 | -4 750 000 |
| M6 | 5 250 000 | 0 | -5 250 000 |
| M7 | 6 050 000 | 355 000 | -5 695 000 |
| M8 | 6 700 000 | 1 065 000 | -5 635 000 |
| M9 | 7 450 000 | 2 130 000 | -5 320 000 |
| M10 | 8 150 000 | 3 905 000 | -4 245 000 |
| M11 | 8 900 000 | 6 390 000 | -2 510 000 |
| M12 | 9 266 000 | 9 585 000 | **+319 000** |

**Cumulative burn to break-even ≈ 46.2 млн ₽.** С учётом буфера на delays / failed pilots разумно держать **55–60 млн ₽ стартового капитала**.

## 13) Cash runway

Берём **startup_capital = 60 млн ₽**.

| Показатель | Значение |
|---|---:|
| Startup capital | 60.0 млн ₽ |
| Peak monthly burn | ~5.7 млн ₽ |
| Average burn до B/E | ~4.2 млн ₽ |
| Cash runway at projected burn | ~14 мес |
| Cash at M12 | ~13.8 млн ₽ |

**Вывод:** капитал **<10 млн ₽** был бы нереалистичен. Для такого enterprise B2B AI кейса нужен стартовый капитал порядка **55–60 млн ₽**.

## 14) Profit Gate

Проверка из задания:

1. **EBITDA < 500k/mo achievable even at 50 clients?**  
   Нет. При 50 клиентах gross profit = **17.75 млн ₽/мес**. Даже после fixed + acquisition модель глубоко прибыльна.

2. **LTV/CAC < 1:1?**  
   Нет. Получается **13.9x**.

**Итог Profit Gate: PASS.**

## 15) Инвестиционный вывод

### Что нравится
- очень сильная валовая экономика на клиента,
- короткий payback относительно enterprise SaaS,
- высокий чек позволяет пережить длинный цикл сделки,
- break-even не требует сотен клиентов.

### Что тревожит
- рынок РФ узкий, buyer universe ограничен,
- sales execution тяжёлый: pilot, security, legal, procurement,
- нужна founder-led продажа, эту машину трудно делегировать слишком рано,
- модель красивая по unit economics, но может упереться в market size и velocity.

## Финальный вердикт

**PASS.**

Для фонда это годится как **нишевой enterprise fintech AI** с few-large-accounts GTM. Не как venture-scale broad SaaS, а как disciplined high-ACV business. Следующий ключевой вопрос уже не про unit economics, а про реальную скорость закрытия первых 5–10 клиентов в РФ-контуре.

## Источники
- Rogo official site: https://www.rogo.ai/
- Rogo Series C announcement, 2026-01-28: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion
- Optifai, B2B SaaS churn benchmark, Q2 2025–Q1 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- HH.ru, работа senior backend developer в Москве: https://hh.ru/vacancies/senior-backend-developer
- HH.ru, Senior backend developer / Яндекс 360: https://hh.ru/vacancy/129266637
- HH.ru, работа machine learning engineer в Москве: https://hh.ru/vacancies/machine-learning-engineer
- HH.ru, SDR / Sales Development Representative (IT / SaaS): https://hh.ru/vacancy/129774256
- HH.ru, работа account executive в Москве: https://hh.ru/vacancies/account_executive
- HH.ru, DevOps-инженер, зарплатная сводка: https://hh.ru/article/skills_devops
- Bitrix24 pricing: https://www.bitrix24.com/prices/
- Snov.io pricing: https://snov.io/pricing

## Примечание по точности
Часть GTM-метрик, расходов на ивенты и распределения acquisition spend не имеет публичной отчётности у Rogo и поэтому является **консервативной инвестиционной моделью**, а не бухгалтерическим фактом. Для stage-level fund screening этого достаточно.

---

## Файл: 05-critic.md

## SECTION A - PnL (12 месяцев, 3 сценария)
### Допущения модели
- Источник входных данных: `04-economics.md`.
- ARPA базового сценария: **450 000 ₽/мес на клиента**.
- COGS на клиента: **95 000 ₽/мес**.
- Contribution на клиента: **355 000 ₽/мес**.
- Fixed costs: **7 061 000 ₽/мес**, из них team FOT fully-loaded **6 071 000 ₽/мес**.
- Growth acquisition engine: **2 205 000 ₽/мес**. Для PnL ниже использую full-growth view, то есть **fixed + acquisition = 9 266 000 ₽/мес** в базе.
- НДС 20% не включён в MRR/COGS/PnL как транзитный поток, но отражён в налоговой модели ниже как фактор для ОСНО.

### Базовый сценарий
- ARPA 450k ₽, churn 1,5%, COGS 95k ₽, fixed+acquisition 9,266 млн ₽/мес.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 3,0 | 5,0 | 7,0 | 9,0 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 3,0 | 5,9 | 10,9 | 17,7 | 26,4 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 450 000 | 1 343 250 | 2 673 101 | 4 883 005 | 7 959 760 | 11 890 363 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 95 000 | 283 575 | 564 321 | 1 030 857 | 1 680 394 | 2 510 188 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 355 000 | 1 059 675 | 2 108 780 | 3 852 148 | 6 279 366 | 9 380 175 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 78,9% | 78,9% | 78,9% | 78,9% | 78,9% | 78,9% |
| Fixed costs, ₽ | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 |
| EBITDA, ₽ | -9 266 000 | -9 266 000 | -9 266 000 | -9 266 000 | -9 266 000 | -9 266 000 | -8 911 000 | -8 206 325 | -7 157 220 | -5 413 852 | -2 986 634 | 114 175 |
| Cash burn, ₽ | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 9 266 000 | 8 911 000 | 8 206 325 | 7 157 220 | 5 413 852 | 2 986 634 | 0 |
| Cumulative cash, ₽ | -9 266 000 | -18 532 000 | -27 798 000 | -37 064 000 | -46 330 000 | -55 596 000 | -64 507 000 | -72 713 325 | -79 870 545 | -85 284 397 | -88 271 031 | -88 156 856 |

**Waterfall на 1 клиента в M12 и итог Net в компании (M12):**
| Метрика | Значение |
|---|---:|
| ARPA | 450 000 ₽ |
| Gross profit / client | 355 000 ₽ |
| Contribution / client | 355 000 ₽ |
| EBITDA / client after fixed allocation M12 | 4 321 ₽ |
| Net income M12 при УСН 6% | -599 246 ₽ |
| Net income M12 при IT-льготе 3% | -242 535 ₽ |
| Net income M12 при ОСНО 20% | 91 340 ₽ |

**Cash flow и break-even:**
| Показатель | Значение |
|---|---:|
| startup_capital_to_bep_rub | 88 271 031 ₽ |
| Break-even client count | 26,1 |
| Break-even month | M12 |

### Оптимистичный сценарий
- ARPA +10%, churn 1,0%, COGS 90k ₽, fixed+acquisition 9,566 млн ₽/мес.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 3,0 | 5,0 | 7,0 | 9,0 | 11,0 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 3,0 | 6,0 | 10,9 | 17,8 | 26,6 | 37,3 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 495 000 | 1 480 050 | 2 950 250 | 5 395 747 | 8 806 790 | 13 173 722 | 18 486 984 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 90 000 | 269 100 | 536 409 | 981 045 | 1 601 234 | 2 395 222 | 3 361 270 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 405 000 | 1 210 950 | 2 413 841 | 4 414 702 | 7 205 555 | 10 778 500 | 15 125 715 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 81,8% | 81,8% | 81,8% | 81,8% | 81,8% | 81,8% | 81,8% |
| Fixed costs, ₽ | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 |
| EBITDA, ₽ | -9 566 000 | -9 566 000 | -9 566 000 | -9 566 000 | -9 566 000 | -9 161 000 | -8 355 050 | -7 152 160 | -5 151 298 | -2 360 445 | 1 212 500 | 5 559 715 |
| Cash burn, ₽ | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 566 000 | 9 161 000 | 8 355 050 | 7 152 160 | 5 151 298 | 2 360 445 | 0 | 0 |
| Cumulative cash, ₽ | -9 566 000 | -19 132 000 | -28 698 000 | -38 264 000 | -47 830 000 | -56 991 000 | -65 346 050 | -72 498 210 | -77 649 507 | -80 009 952 | -78 797 453 | -73 237 738 |

**Waterfall на 1 клиента в M12 и итог Net в компании (M12):**
| Метрика | Значение |
|---|---:|
| ARPA | 495 000 ₽ |
| Gross profit / client | 405 000 ₽ |
| Contribution / client | 405 000 ₽ |
| EBITDA / client after fixed allocation M12 | 148 865 ₽ |
| Net income M12 при УСН 6% | 4 450 495 ₽ |
| Net income M12 при IT-льготе 3% | 5 005 105 ₽ |
| Net income M12 при ОСНО 20% | 4 447 772 ₽ |

**Cash flow и break-even:**
| Показатель | Значение |
|---|---:|
| startup_capital_to_bep_rub | 80 009 952 ₽ |
| Break-even client count | 23,6 |
| Break-even month | M11 |

### Пессимистичный сценарий
- ARPA -10%, churn 2,5%, COGS 110k ₽, fixed+acquisition 9,066 млн ₽/мес.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 3,0 | 4,0 | 5,0 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 3,0 | 5,9 | 9,8 | 14,5 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 405 000 | 1 204 875 | 2 389 753 | 3 950 009 | 5 876 259 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 110 000 | 327 250 | 649 069 | 1 072 842 | 1 596 021 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 295 000 | 877 625 | 1 740 684 | 2 877 167 | 4 280 238 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 72,8% | 72,8% | 72,8% | 72,8% | 72,8% |
| Fixed costs, ₽ | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 |
| EBITDA, ₽ | -9 066 000 | -9 066 000 | -9 066 000 | -9 066 000 | -9 066 000 | -9 066 000 | -9 066 000 | -8 771 000 | -8 188 375 | -7 325 316 | -6 188 833 | -4 785 762 |
| Cash burn, ₽ | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 9 066 000 | 8 771 000 | 8 188 375 | 7 325 316 | 6 188 833 | 4 785 762 |
| Cumulative cash, ₽ | -9 066 000 | -18 132 000 | -27 198 000 | -36 264 000 | -45 330 000 | -54 396 000 | -63 462 000 | -72 233 000 | -80 421 375 | -87 746 691 | -93 935 523 | -98 721 285 |

**Waterfall на 1 клиента в M12 и итог Net в компании (M12):**
| Метрика | Значение |
|---|---:|
| ARPA | 405 000 ₽ |
| Gross profit / client | 295 000 ₽ |
| Contribution / client | 295 000 ₽ |
| EBITDA / client after fixed allocation M12 | -329 841 ₽ |
| Net income M12 при УСН 6% | -5 138 337 ₽ |
| Net income M12 при IT-льготе 3% | -4 962 050 ₽ |
| Net income M12 при ОСНО 20% | -4 785 762 ₽ |

**Cash flow и break-even:**
| Показатель | Значение |
|---|---:|
| startup_capital_to_bep_rub | 98 721 285 ₽ |
| Break-even client count | 30,7 |
| Break-even month | не достигнут за 12 мес |

### Налоговая модель РФ
| Режим | Как считаю | Эффект на модель |
|---|---|---|
| УСН 6% | 6% с выручки | болезненно в убыточные месяцы, но просто для early stage |
| IT-льгота 3% | 3% с выручки при аккредитации Минцифры и соблюдении критериев | лучший cash outcome в большинстве SaaS-сценариев |
| ОСНО 20% | 20% с прибыли + НДС 20% если применимо | при убытке profit tax = 0, но VAT/admin burden выше |
| Страховые взносы | ~30% к ФОТ | уже включены в team FOT 6,071 млн ₽/мес |

**Вывод по налогам:** для этого кейса базовый operating contour рационально целиться в **IT-льготу 3%**, запасной режим, **УСН 6%**. ОСНО имеет смысл только если структура клиентов/контрактов и входной НДС компенсируют рост admin burden.

<!-- P6A-DONE -->

## SECTION B - Finance Risk + Competitor

### 1) Sensitivity analysis, EBITDA через 12 месяцев

База взята из SECTION A. Для чувствительности меняю по одному фактору при прочих равных. Для CAC x2 считаю, что при неизменном acquisition budget 2,205 млн ₽/мес темп новых клиентов падает примерно вдвое.

| Сценарий | Ключевое изменение | Clients @M12 | MRR @M12 | EBITDA @M12 |
|---|---|---:|---:|---:|
| Base | без изменений | 26,4 | 11,89 млн ₽ | **0,11 млн ₽** |
| Sens1 | CAC x2 | 13,2 | 5,95 млн ₽ | **-4,58 млн ₽** |
| Sens2 | Churn x2, с 1,5% до 3,0% | 25,9 | 11,64 млн ₽ | **-0,09 млн ₽** |
| Sens3 | Price -30%, до 315 тыс. ₽/мес | 26,4 | 8,32 млн ₽ | **-3,45 млн ₽** |

**Вывод:** модель особенно хрупкая к price compression и ухудшению CAC. Даже умеренный удар по churn уже уводит базу ниже нуля.

### 2) Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 300 000 | 1 700 000 | 2 200 000 | [I1] |
| Monthly churn, % | 1,0% | 1,5% | 2,5% | [I1] |
| ARPU, ₽/мес | 405 000 | 450 000 | 495 000 | [I1] |
| Conversion rate lead→paid, % | 0,08% | 0,10% | 0,13% | [I1] |
| Time-to-hire, мес | 1,0 | 1,5 | 2,5 | [I1] |

#### Метод
Вместо полного кода использую 9 комбинаций по ключевым трём драйверам, где:
- best = CAC_min + churn_min + ARPU_max,
- median = CAC_mode + churn_mode + ARPU_mode,
- worst = CAC_max + churn_max + ARPU_min,
- ещё 6 смешанных комбинаций вокруг центра.

Для EBITDA @M24 считаю steady-state с тем же acquisition budget 2,205 млн ₽/мес, где новые клиенты в месяц = acquisition spend / CAC, первые закрытия начинаются после M6, как в исходной модели. Это не бухгалтерский forecast, а стресс-тест инвестиционной устойчивости.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24, ₽/мес | **-4,72 млн ₽** | **-1,95 млн ₽** | **1,96 млн ₽** | **6,68 млн ₽** |
| CAC payback, мес | 5,43 | 3,78 | 2,63 | 2,81 |
| LTV/CAC | 5,64x | 13,92x | 30,77x | **25,13x** |
| Cash runway, мес | 12,7 | 30,7 | 24+ | 11,3+ |

**Интерпретация правил:**
1. **p10 EBITDA < 0, критерий kill #1 срабатывает.** В хвосте распределения модель уходит в риск insolvency.
2. **p50 EBITDA < 500 тыс. ₽/мес, значит медианный сценарий не проходит EBITDA Gate.**
3. p90/p10 в прямом виде некорректен, потому что p10 отрицательный; это ещё хуже, чем просто 10x dispersion, так как знак прибыли меняется.
4. **Range width по LTV/CAC = 25,13x > 8**, значит модель реально хрупкая к цене, churn и эффективности продаж.

### 3) Competitor deep-dive

#### Топ-3 западных
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Rogo** | AI-native finance workflow, 25k+ daily users, сильный brand signal в IB/PE, white-glove enterprise motion [W1] | дорогой enterprise motion, длинный цикл внедрения, вероятно слабая локализация под РФ и data residency | **~10-15%** в узкой нише AI-native finance copilot, оценка по category mindshare [inf] | локальный on-prem/RF-hosted контур, русскоязычные источники, дешевле вход и быстрее кастомизация под 152-ФЗ/санкции |
| **Hebbia** | сильный document reasoning для diligence и deal docs, доверие крупных фондов и банков, security posture [W2] | heavy-doc workflow, но не очевиден как локальный workflow-layer для РФ-финанса; дорогое внедрение | **~20-25%** в AI-for-finance/document-intelligence сегменте [inf] | локальные интеграции, lower CAC на РФ buyers, лучшее покрытие русских документов и внутреннего комплаенса |
| **AlphaSense** | гигантский контентный moat, 1 500+ млн документов, mature enterprise search, сильная позиция в market intelligence [W3] | продукт шире и тяжелее, чем нужен узкому РФ finance-copilot use case; высокая цена и зависимость от западного контента | **~35-45%** в broader market-intelligence/search layer [inf] | у нас более узкий workflow fit под M&A/IB в РФ, меньше лишней платформенной сложности, лучше sovereign deployment |

#### Топ-4 российских и локальных substitutes
| Конкурент | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Visiology** | vc.ru и Rusprofile [R1][R2] | сильный российский BI/on-premise narrative, enterprise selling motion, знакомый procurement-путь | это BI-платформа, а не finance copilot; слабее в memo/comps/diligence reasoning | **~10-15%** в adjacent RU enterprise BI+AI contour [inf] | мы глубже по analyst workflow, retrieval, deal docs и vertical prompts |
| **Just AI / Jay Knowledge Hub** | Habr [R3] | зрелый enterprise AI stack, knowledge assistants, интеграции и российский вендорский контур | не сфокусирован на high-finance workflow; риск быть general-purpose platform | **~8-12%** в RU enterprise knowledge-assistant niche [inf] | лучшее verticalization под банкиров, PE и corpdev, меньше time-to-value |
| **Yandex DataLens + Нейроаналитика** | vc.ru [R4] | мощная дистрибуция, низкий барьер входа, знакомость бренда, хороший слой BI/аналитики | не решает глубокий due diligence / IC memo / comps workflow end-to-end | **~15-20%** в mass-market RU analytics-with-AI layer [inf] | мы продаём outcome, а не generic dashboard AI |
| **CraftTalk / Skolkovo AI assistants** | Skolkovo [R5] | российский AI-assistant vendor, enterprise security narrative, контакт с regulated sector | больше CX/contact-center DNA, чем investment workflow DNA | **~3-5%** в adjacent enterprise assistant segment [inf] | у нас уже ICP-специфичный finance wedge и выше готовность buyers платить за mission-critical use case |

**Итог по конкурентам:** прямого локального лидера уровня Rogo в РФ я не вижу. Но substitutes много, и главный риск не в одном killer-конкуренте, а в том, что бюджет распылится между BI, knowledge assistant, internal tooling и ручной работой аналитиков.

### 4) Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | founder-led sales не масштабируется в повторяемый motion | med | high | <3 SQL/мес после M4, founder закрывает 100% demo сам | нанять AE только после repeatable pitch, ввести stage-gates по pipeline |
| Operational | качество ответов на длинных финансовых документах плавает | med | high | >15% pilot sessions требуют ручного rework | eval harness, golden sets, human-in-the-loop, ограничение use cases |
| Operational | зависимость от внешних LLM API и latency spikes | high | high | рост COGS/tenant >20% за 2 мес, SLA incidents | multi-model routing, fallback на локальные модели, ценовые лимиты |
| Market | buyer universe в РФ слишком узкий | high | high | pipe концентрируется в 10-15 аккаунтах, expansion stalls | расширить ICP в corpdev, big-4-like advisory, крупные холдинги |
| Market | price compression из-за generic copilots и BI-with-AI | high | high | discounting >20%, win-rate падает при цене >400k ₽ | пакетировать secure deployment, шаблоны workflow, onboarding fee |
| Market | конкуренты/substitutes решают 70% JTBD “достаточно хорошо” | med | med | pilots заканчиваются на стадии “оставим Power BI + analyst team” | продавать measurable ROI, hours saved, memo turnaround, audit trail |
| Regulatory | 152-ФЗ и data residency блокируют облачный deployment | high | high | security review длится >90 дней, юристы требуют on-prem only | on-prem / VPC first, локальное хранение, DPA и модель доступа |
| Regulatory | 115-ФЗ / AML / KYC контур ограничивает использование внешних данных и генерации | med | high | compliance asks for full lineage, запрет на black-box outputs | citations-by-default, logs, approval workflows, explainability layer |
| Financial | cash runway съедается длинным sales cycle | high | high | M6 cash runway <9 мес при 0-1 клиентах | урезать hiring pace, держать runway buffer 18 мес, milestone financing |
| Financial | USD/RUB и инфляция давят на COGS и зарплаты | high | med | COGS/client >110k ₽, ожидания senior hires растут >15% | рублёвые контракты с индексатором, multi-vendor infra, reserve 10-15% |
| Black swan | новый санкционный пакет режет доступ к западному SaaS / модели | med | high | письмо о прекращении сервиса, billing failures, geo-block | open-source fallback, российские LLM, запасной infra stack |
| Black swan | отключение ключевого LLM-провайдера или резкая деградация модели | med | high | резкий рост ошибок/latency, отсутствие capacity | abstraction layer, заранее протестированные backup models, BYOM |

### 5) Kill conditions, горизонт 6 месяцев
1. **Kill #1, insolvency risk:** на ревью в M6 обновлённый forward forecast всё ещё показывает **p10 EBITDA@M24 < 0** **или** cash runway < 6 мес.
2. **Commercial kill:** к M6 нет минимум **2 платящих клиента** **или** нет pipeline на **≥6 qualified pilots** с суммарным weighted ARR ≥ 18 млн ₽.
3. **Unit-economics kill:** к M6 либо **blended CAC > 3,0 млн ₽**, либо **payback > 9 мес по revenue**, либо price realization падает ниже **350 тыс. ₽/мес** на клиента.

### 6) Итоговый investment stance после SECTION B

SECTION A давал формальный PASS по unit economics, но SECTION B заметно ухудшает картину риска. Ключевой вывод такой:
- база хрупкая к CAC и цене,
- медианный M24-расклад не проходит EBITDA gate,
- tail risk по ликвидности и санкционному/LLM-контуру существенный,
- конкурентная угроза в РФ не от одного прямого лидера, а от пачки adjacent substitutes.

**Итог:** кейс остаётся интересным как high-ACV niche play, но score должен быть **downgraded на риск/variance**, а инвестиционное решение нельзя принимать без подтверждения первых 2-3 платящих enterprise logos.

### Источники SECTION B
- [I1] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/rogo-wall-street-ai-geo-expand-v2/04-economics.md`
- [W1] Rogo, Series C and European expansion: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion
- [W2] Hebbia official site: https://www.hebbia.com/
- [W3] AlphaSense official site: https://www.alpha-sense.com/
- [R1] vc.ru про Visiology: https://vc.ru/
- [R2] Rusprofile по Visiology / юрлицу: https://www.rusprofile.ru/
- [R3] Habr, Just AI / knowledge assistants: https://habr.com/
- [R4] vc.ru, Яндекс DataLens / нейроаналитика: https://vc.ru/
- [R5] Skolkovo, AI assistant vendors / CraftTalk: https://sk.ru/

<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[GEO-EXPAND] Rogo Wall Street AI — REJECTED: 55/100 | EBITDA base=114К₽/мес через 12 мес | LTV/CAC=13,9x | Ключевое преимущество: дорогой enterprise workflow с сильной валовой экономикой | Главный риск: узкий рынок и хрупкость к CAC/price compression.

# 06-verdict — Investment Committee Verdict

sector: GEO-EXPAND
status: REJECTED
score: 55/100
case: rogo-wall-street-ai-geo-expand-v2
analyst: branch-models-lead
verdict_date: 2026-05-12

## Executive verdict
Кейс показывает инвестиционно приятную юнит-экономику на уровне одного клиента, но не проходит committee-grade фильтр по устойчивости компании. В базе EBITDA на M12 всего **114 175 ₽/мес**, а в Monte Carlo медиана на M24 остаётся **-1,95 млн ₽/мес**. Это означает, что красивая LTV/CAC-математика пока не превращается в надёжный company-level outcome для РФ-контура.

Дополнительный стоп-фактор, moat слабый. Категория может жить как локальный enterprise niche play, но пока не доказано, что команда сможет удержать premium price, пройти security-heavy GTM и построить repeatable motion без founder bottleneck.

## Оценка
Source tier balance: T1=3, T2=6, T3=2, weighted=2.09. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | «Contribution Margin: 78.9%», «LTV/CAC: 13.9x», «CAC payback: 3.8 мес». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 13 | «EBITDA @M12 = 114 175 ₽», при этом «p50 EBITDA @M24 = -1,95 млн ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «investment banking ai = LOW / 3», но «SAM_bottom-up = 288 млн руб.» и «399 сделок M&A». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | «прямого локального лидера уровня Rogo в РФ я не вижу», но substitutes много и budget risk высокий. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 12 | «tail risk по ликвидности и санкционному/LLM-контуру существенный». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 15 | «founder-led enterprise motion», «sales cycle 6–9 мес», но buyer list и channel fit понятны. |

**Normalized score = round((82 × 100) / 150) = 55/100.**

## 7-factor Moat Framework
| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| 2. Switching costs | 2 | Есть data room, шаблоны, security review и обученность команды клиента. |
| 3. Scale economies | 1 | COGS на клиента частично оптимизируется, но white-glove delivery остаётся тяжёлой. |
| 4. Proprietary data / model advantage | 1 | Возможен локальный retrieval-layer, но уникальный датасет не доказан. |
| 5. Regulatory moat | 1 | Compliance-heavy контур важен, но лицензируемого барьера нет. |
| 6. Brand / distribution | 1 | Глобальный brand signal Rogo силён, локальной дистрибуции в РФ нет. |
| 7. Embedded workflow | 2 | Продукт встроен в memo/comps/diligence workflow и может стать daily tool. |

**Moat score = round((8 × 25) / 21) = 10/25.**

Вывод: moat погранично слабый. Не полный zero, но недостаточный для investment-grade approve.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 23 666 667 ₽ |
| CAC | 1 696 154 ₽ |
| LTV/CAC | 13.9x |
| CAC Payback | 3.8 мес |
| GM | 78.9% |
| contribution_margin_rub_month | 355 000 ₽ |
| fixed_costs_rub_month | 7 061 000 ₽ |
| company_ebitda_rub_month базовый M12 | 114 175 ₽ |
| company_ebitda_potential_rub_month при 50 клиентах | 8 484 000 ₽+ |
| clients_to_500k_ebitda | 28 |
| months_to_500k_ebitda | 13-14 мес |
| clients_to_1m_ebitda | 29-30 |
| startup_capital_to_bep_rub | 88 271 031 ₽ |
| break-even | 26.1 клиента / M12 |

## FULL business process from 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR | Snov.io, CBR registry, ручной research | 2 ч | 1 200 | средняя |
| 2 | Enrichment контактов | SDR | Snov.io, корпоративный email finder | 1 ч | 600 | высокая |
| 3 | Холодное касание email/LinkedIn/Telegram | SDR | Snov.io sequences, почта | 1.5 ч | 900 | высокая |
| 4 | Follow-up 1–3 | SDR | sequence automation + ручные ответы | 2 ч | 1 200 | высокая |
| 5 | Qualification call | SDR + AE | CRM, Meet | 1 ч | 2 200 | низкая |
| 6 | Demo под workflow клиента | AE + founder | Demo env, презентация | 1.5 ч | 4 500 | низкая |
| 7 | Discovery по use-cases и security | AE + CTO | Notion/CRM, чек-листы ИБ | 2 ч | 6 200 | низкая |
| 8 | Pilot scoping | CTO + ML Eng | sandbox, sample docs | 3 ч | 9 000 | низкая |
| 9 | Pilot deployment | ML Eng + Backend | cloud, vector DB, connectors | 12 ч | 31 000 | средняя |
| 10 | Pilot support и tuning | ML Eng + CSM | monitoring, prompt/config tools | 8 ч | 19 000 | средняя |
| 11 | Procurement / legal / DPA | AE + founder + legal | шаблоны договора, ЭДО | 6 ч | 18 000 | низкая |
| 12 | Security review | CTO + DevOps | IAM, logging, policy docs | 8 ч | 24 000 | низкая |
| 13 | Финальное коммерческое предложение | AE | CRM, CPQ/Excel | 1 ч | 2 600 | средняя |
| 14 | Счёт и закрывающие документы | Finance ops | 1С/МойСклад/ЭДО | 0.5 ч | 700 | высокая |
| 15 | Оплата | Клиент | bank transfer | 7–30 дней | 0 | высокая |
| 16 | Onboarding и enablement | CSM + AE + ML Eng | knowledge base, trainings | 10 ч | 26 000 | средняя |

## Team table
| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Ramp до 80% productivity, мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | продажи, fundraising, ключевые клиенты | 1 | 700 000 | 0 | 0 | 210 000 | 910 000 |
| CTO / Tech Lead | архитектура, security review, roadmap | 1 | 600 000 | 2.5 | 2 | 180 000 | 780 000 |
| Senior Backend | ingestion, APIs, auth, enterprise controls | 2 | 450 000 | 1.5 | 1.5 | 270 000 | 1 170 000 |
| ML Engineer | retrieval, evals, prompts, tuning | 2 | 500 000 | 2.5 | 2 | 300 000 | 1 300 000 |
| DevOps | infra, observability, IAM | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | analyst UI, admin panels | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | outbound prospecting | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| AE | demo, pilot, close | 1 | 400 000 | 1.5 | 2.5 | 120 000 | 520 000 |
| Customer Success | onboarding, adoption, renewals | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| **Итого** |  | **11** |  |  |  |  | **6 071 000 ₽/мес** |

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер CIB | крупный M&A и ECM/DCM поток, много analyst-hours и security-heavy контур | email decision-maker + warm intro через отраслевую конференцию | 600 000 ₽/мес |
| ВТБ Капитал / ВТБ CIB | регулярные сделки и внутренние research workflows, высокая цена ошибки | email managing director + private event | 600 000 ₽/мес |
| Альфа-Банк CIB | активный корпоративный блок, сложные презентационные и memo workflows | партнёрство + founder outreach | 500 000 ₽/мес |
| Газпромбанк | regulated buyer с corpfin и advisory use-cases | конференция + direct outreach в strategy/corpdev | 550 000 ₽/мес |
| БКС Мир инвестиций | research-heavy broker с плотной работой с инвестматериалами | email head of research + pilot offer | 450 000 ₽/мес |
| Атон | boutique/high-touch wealth и advisory, быстрее пилотный цикл | founder-to-founder intro | 400 000 ₽/мес |
| Совкомбанк CIB | active corpfin контур и потребность в ускорении due diligence | email + targeted roundtable | 450 000 ₽/мес |
| УК Первая | investment committee materials и рынок капитала, важна скорость анализа | партнёрство с data-vendor + outbound | 400 000 ₽/мес |
| Альфа-Капитал | управляющая компания с research и investment memo workload | direct outreach + content-led кейс | 400 000 ₽/мес |
| Т-Капитал | современная digital-first команда, готовность тестировать новый workflow stack | founder outreach + vc.ru / Habr thought-leadership | 450 000 ₽/мес |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| weak_moat_and_price_compression | high | high | Substitute-слой из BI, research terminals и внутренних аналитиков может срезать цену на 20-30%. |
| enterprise_sales_velocity | high | high | При CAC x2 и том же acquisition budget M12 EBITDA падает до **-4,58 млн ₽**. |
| llm_dependency_and_regulatory_contour | med-high | high | Санкции, 152-ФЗ, latency и vendor risk могут сорвать on-prem/VPC rollout. |

## Proof points, которые были бы нужны для APPROVED
1. Минимум 2-3 платящих enterprise logo в РФ или близком контуре с recurring MRR **≥450 тыс. ₽/мес**.
2. Подтверждение, что security review и procurement закрываются не дольше **90 дней**.
3. Повторяемый blended CAC **≤2,0 млн ₽** на платящего клиента.
4. Реальный retention proof, monthly churn **≤1.5%** или annual gross retention **≥85%**.
5. Доказательство локального data/integration moat, а не просто wrapper над LLM + manual services.

## LTV Upside Calculator
Так как verdict = REJECTED, upside считаем через три рычага.

| Рычаг | Текущая база | Upside-case | Эффект |
|---|---:|---:|---|
| ARPA | 450 000 ₽/мес | 550 000 ₽/мес | contribution_margin_rub_month растёт до ~455К₽, EBITDA gate ускоряется на 2-3 мес |
| CAC | 1.70 млн ₽ | 1.20 млн ₽ | LTV/CAC растёт к ~19.7x, sales motion становится менее хрупким |
| Churn | 1.5%/мес | 1.0%/мес | customer_ltv_rub растёт к ~35.5 млн ₽ |

**Upside trigger для re-open:** если одновременно достигаются ARPA ≥ 500К₽, CAC ≤ 1.4М₽ и 2 платящих лого до M6, кейс можно возвращать на повторный critic.

## Сравнение с исходным тезисом
Да, это фактически близкий cousin к ранее уже известной Rogo/finance-analyst категории. Новый standalone verdict полезен тем, что показывает, где именно ломается локальный тезис: не в боли клиента и не в unit economics, а в company-level resilience, moat и go-to-market repeatability.

## Финальное решение IC
**REJECTED.**

Причина отклонения: score существенно ниже порога, а company-level базовый профиль слишком хрупкий. Это хороший candidate для наблюдения и последующего re-open после появления локальных proof points, но не для текущего approve.


---

## Файл: 07-score-trajectory.md

# Score trajectory

## 2026-04-23 — P4 Demand Validation
- Stage: P4 Demand Validation
- Case: rogo-wall-street-ai-geo-expand-v2
- Summary: Прямой search-demand по AI-ярлыку низкий, но underlying investment research / M&A workflow в РФ остаётся платёжеспособным, а Profit Gate проходит в enterprise-модели.
- Demand score: n/a in current run, mandatory multi-demand endpoint timed out; prior adjacent case signals = LOW for `investment banking ai`, MEDIUM for `инвестиционный аналитик`
- Investment implication: PASS, двигать дальше только как high-trust enterprise wedge, не как PLG или массовый SaaS.
- Score trajectory impact: усиливает тезис о нишевом, но монетизируемом рынке с ограниченным SAM и высокой зависимостью от few-large-accounts GTM.
- Analyst note: Главный вопрос дальше не наличие боли, а способность удержать высокий чек при длинном procurement cycle и требованиях к безопасности.

## 2026-05-11 — P5 Unit Economics
- Stage: P5 Unit Economics
- Case: rogo-wall-street-ai-geo-expand-v2
- Summary: Юнит-экономика проходит инвестиционный порог только как enterprise fintech AI с ACV/MRR уровня high-trust B2B, длинным циклом сделки и fully-loaded CAC, включающим pilot, security review и procurement overhead.
- Key metrics: ARPA 450k ₽/мес; COGS 95k ₽/клиент/мес; Contribution Margin 78.9%; blended fully-loaded CAC 1.70 млн ₽; monthly churn 1.5%; LTV 23.7 млн ₽; LTV/CAC 13.9x; CAC payback 3.8 мес.
- Break-even: ~20 клиентов на operating basis и ~27 клиентов с включённым acquisition engine; full-growth break-even достигается около M12 при cumulative burn ~46.2 млн ₽.
- Profit Gate: PASS, потому что EBITDA > 500k ₽/мес достижима сильно раньше 50 клиентов, а LTV/CAC значительно выше 3:1.
- Investment implication: кейс экономически качественный, но это не venture-scale broad SaaS, а узкий few-large-accounts business с высоким execution risk и ограниченным buyer universe.
- Analyst note: Следующий критический тест не в теории маржинальности, а в способности founder-led команды закрыть первые 5–10 regulated enterprise клиентов без расползания цикла продажи и без падения win-rate.

## 2026-05-12 — P7 Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: rogo-wall-street-ai-geo-expand-v2
- Summary: Финальный critic подтверждает сильную экономику на клиента, но не подтверждает company-level устойчивость. База даёт только 114 175 ₽ EBITDA на M12, p50 Monte Carlo на M24 остаётся отрицательной, moat слабый.
- Final score: 55/100
- Verdict: REJECTED
- Key blockers: weak moat, узкий SAM в РФ, сильная чувствительность к CAC и price compression, founder-heavy enterprise GTM, LLM/regulatory dependency.
- Re-open trigger: вернуться к кейсу после появления 2-3 платящих enterprise logos с MRR ≥ 450k ₽, CAC ≤ 1.4-2.0 млн ₽ и повторяемого security/procurement cycle ≤ 90 дней.
- Analyst note: Это качественный watchlist-case, но не текущий approve для фонда. Наиболее вероятный upside лежит в локальном data moat и доказанном repeatable sales motion, а не в ещё более красивой Excel-модели.


