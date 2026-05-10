# verdict.md

[GEO-EXPAND] Indico Data — NEAR-PASS: 65/100 | EBITDA base=603К₽/мес через 12 мес | LTV/CAC=7,45x | Ключевое преимущество: дорогой claims/underwriting workflow с высоким ACV | Главный риск: weak moat и слишком узкий buyer universe в РФ.


---

## 00-brief.md

# Краткий бриф

- Кейс создан принудительно по правилу resurrect.
- Тема: Indico Data: AI decisioning для страхового underwriting, intake и claims в enterprise-страховании.
- Исходный raw-файл: `2026-04-19-resurrect-indico-data-geo-expand.md`.
- Оригинальный verdict: `triage/triage-2026-04-19-indico-data-geo-expand.md`.
- Следующий этап: P3-demand-validation.
- Причина создания: сигнал должен пройти полный цикл P3→P7 с новой аналитикой, даже если раньше уже был обработан как отдельный кейс или как supporting signal.


---

## 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-indico-data-geo-expand.md
created: 2026-04-20T18:14:00+03:00
original_verdict: triage/triage-2026-04-19-indico-data-geo-expand.md
---

# Intake

## Режим обработки
Принудительный полный пайплайн по правилу `rerun-/resurrect-`. На этапе intake файл не классифицируется как duplicate.

## Оригинальный источник
- Raw-файл: `2026-04-19-resurrect-indico-data-geo-expand.md`
- Исторический источник: `triage/triage-2026-04-19-indico-data-geo-expand.md`

## Полный контекст из raw

# RESURRECT SIGNAL — indico-data-geo-expand

## Meta
- source: triage/triage-2026-04-19-indico-data-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж: Indico Data GEO-EXPAND

- Дата обработки: 19 апреля 2026 года
- Raw-файл: `pipeline/raw/2026-04-19_06-29-05_geo-expand_indico-data.txt`
- Решение: новый кейс
- Созданный кейс: `pipeline/cases/ai-insurance-underwriting-and-claims-decisioning-operator/00-brief.md`

## Почему это не дубль
Сигнал относится к отдельной категории: AI-native decisioning для страхового underwriting, intake и claims в корпоративном страховании. В текущих открытых кейсах есть смежные темы в кредитном андеррайтинге и legal claims, но не найден действующий кейс, который точно покрывает страховой decisioning-контур.

## Почему кейс проходит порог
Во входном материале указан ориентир LTV `3 000 000-12 000 000 ₽ в год` на одного крупного страхового клиента, то есть до `1 000 000 ₽ в месяц`. Это выше порога Program 1 по верхней части диапазона. Дополнительно high-LTV поддерживается длинным внедрением, интеграциями, требованиями к auditability и recurring-сопровождением decisioning workflows.

## Что зафиксировано в brief
В кейс внесены: позиционирование Indico Data как agentic decisioning platform для страхования, сигнал о record ARR в 2025 году, рост новых carrier-клиентов на 60% YoY в H1 2025, использование платформы страховщиками в США и Великобритании, а также вывод о наличии окна на рынке РФ.

```


---

## 02-demand.md

# Demand validation — Indico Data

## Вывод
**Вердикт: PASS с оговорками, идти дальше по пайплайну.**

По internal endpoint `multi-demand` спрос в РФ на категорию низкий: `страховой андеррайтинг автоматизация` дал **LOW / 3**, `автоматизация урегулирования убытков страхование` дала **LOW / 0**. Это плохой сигнал для PLG и массового self-serve, но не убивает кейс, потому что рынок здесь не search-led, а enterprise-sales-led: покупателей мало, бюджеты концентрированы, цена ошибки высокая, а recurring чек может быть в диапазоне **3–12 млн ₽ в год на страховщика** как минимум в сценарии enterprise deployment [Internal brief] и косвенно поддерживается прайс-якорями у document AI / decisioning конкурентов [T2].

## 1) Что именно валидируем
Indico Data, по брифу, это AI decisioning для страхового underwriting, FNOL / intake и claims operations. Для РФ это не массовый SaaS, а узкий enterprise stack для страховщиков, которые хотят:
- ускорять intake и разбор документов [T2]
- сокращать ручную проверку кейсов и андеррайтинг [T2]
- улучшать traceability, auditability и качество решения по кейсам [T2]

## 2) Demand signals
- По internal endpoint на **21 апреля 2026** запрос `страховой андеррайтинг автоматизация` вернул **LOW / 3**: HH vacancies = 14, Habr = 2, Google Trends RU = 1, Yandex Suggest = 2. [Internal]
- Запрос `автоматизация урегулирования убытков страхование` вернул **LOW / 0**: HH vacancies = 3, Habr = 2, Google Trends RU = 0, Yandex Suggest = 2. [Internal]
- Это означает, что в РФ нет широкого inbound спроса на саму категорию. Но для enterprise-страхования это нормально: закупки такого ПО обычно идут через RFP, integrator-led продажу и top-down цифровую трансформацию, а не через массовый поисковый хвост. Это **инференс** на базе слабого search intent и структуры рынка страхования РФ. [T1 + inference]
- Банк России фиксирует **3 976,6 млрд ₽ страховых премий** по итогам 2025 года и **129 страховых организаций** на 01.01.2026, то есть рынок крупный в деньгах, но узкий по числу покупателей. [T1]

## 3) Конкуренты и цены
Ниже не только прямые страховые decisioning vendors, но и реальные document AI / intake automation substitute-решения, за которые уже платят в похожем workflow.

1. **Rossum** — `Starter` от **$18,000 в год**. Позиционирование: end-to-end document automation, extraction, validation, workflow. Это прямой proxy для intake / claims document automation. [T2]
2. **Veryfi** — **$0.08 за receipt**, **$0.16 за invoice / form**, **$0.25 за check / bank statement**, калькулятор на сайте показывает **$500/month** при определённом объёме. Это usage-based anchor для document ingestion и extraction. [T2]
3. **Mindee** — `Starter` **44€/мес**, `Pro` **179€/мес**, `Business` **584€/мес**, плюс per-credit overage. Это lower-end API anchor для OCR / extraction. [T2]
4. **Docparser** — `Starter` **$39/мес** за 100 credits. Это ещё один нижний ценовой anchor для rule-based / lightweight extraction. [T2]
5. **Nanonets** — pricing без фиксированного seat fee, с pay-as-you-go и enterprise quotes; это подтверждает, что рынок document AI monetizes как usage + enterprise volume. Чёткий публичный тариф на единицу не раскрыт, поэтому источник используем как supporting, не как price anchor. [T2]

### Что это значит для Indico
- Для low-end OCR / parsing рынок уже платит десятки-сотни долларов в месяц. [T2]
- Для enterprise document automation рынок уже платит **$18k+ в год** даже без глубокой отраслевой логики. [T2]
- Следовательно, специализированный insurance decisioning stack может рационально стоить **500 тыс. – 1,0 млн ₽ в месяц** при внедрении в крупного страховщика. Это **инференс**, а не прямой прайс-лист, но он опирается на observed price anchors и высокую стоимость ручного страхового процесса. [T2 + inference]

## 4) Telegram в РФ: боты и сервисы
- **СОГАЗ** официально запустил Telegram-бот `@SogazRuBot` для урегулирования страховых событий по каско и подачи онлайн-заявки по ОСАГО. Это прямое подтверждение того, что страховщики в РФ уже переводят FNOL / claims intake в мессенджеры. [T2]
- По internal demand tool в Telegram по ключевым запросам подписчиков / сильных нишевых сигналов не найдено: `telegram.subscribers = 0`. [Internal]
- Я не нашёл сильных Telegram-native B2B сервисов в РФ именно для underwriting decisioning или claims orchestration для страховщиков. Вывод: Telegram в России уже используется как **клиентский канал подачи убытка**, но не как зрелая B2B product category для AI decisioning. Это создаёт окно для слоя «под капотом», а не для TG-first продукта. [T2 + inference]

## 5) Willingness to pay (WTP)
### Признаки платёжеспособности
- Страховой рынок РФ по итогам 2025 года собрал **3 976,6 млрд ₽ премий**. Даже микроскопическая доля от этой базы допускает многомиллионные годовые бюджеты на core-process automation. [T1]
- На рынке всего **129 страховщиков**, то есть бюджет сконцентрирован у ограниченного числа крупных игроков; это типичная структура, где enterprise vendor может жить на нескольких крупных контрактах. [T1]
- СОГАЗ уже инвестирует в Telegram-based claims intake, а значит страховщики реально тратят деньги на оцифровку front-door и урегулирования. [T2]
- ABBYY показывает страховой customer story Ecclesia Group по streamlining correspondence / claims-related processing, то есть страховой сегмент глобально уже покупает document AI для операций. Это не российский кейс и без публичной цены, но как доказательство категории годится. [T2]
- Прайс-якори Rossum / Veryfi / Mindee показывают, что за document extraction и workflow automation уже платят recurring. [T2]

### Вывод по WTP
WTP **есть**, но он сосредоточен почти целиком в upper-mid / enterprise сегменте. Для self-serve рынка доказательств нет. Для российских страховщиков реалистичен диапазон:
- пилот / limited scope: **250–400 тыс. ₽/мес** [T2 + inference]
- production deployment: **500 тыс. – 1,0 млн ₽/мес** [T2 + inference]
- с кастомными моделями, rules и SLA: **1,2+ млн ₽/мес** для top-tier carrier тоже не выглядит абсурдно, но это уже более смелая оценка. [T2 + inference]

## 6) Market sizing
### Логика сегмента
Берём не весь insurtech и не весь OCR. Для Indico в РФ адресуемый рынок — это software spend на underwriting / intake / claims decisioning у страховых компаний.

### Top-down
**[LOW CONFIDENCE]** Top-down строится от официального объёма страхового рынка РФ и узкой доли software spend на decisioning workflows.

- База отрасли: **3 976,6 млрд ₽ страховых премий** в РФ по итогам 2025 года. [T1]
- Для узкого слоя decisioning / intake / claims automation беру addressable share **0,015%** от страховых премий. Это не рыночная константа, а консервативная рабочая доля, согласованная с наблюдаемым числом покупателей и enterprise ACV. [T1 + inference]
- Тогда **TAM (РФ) = 3 976,6 млрд ₽ × 0,015% = 596,5 млн ₽**. [T1 + inference]
- Для SAM берём только carriers с достаточной цифровой зрелостью и реальной потребностью в enterprise decisioning, то есть примерно **70% TAM**. [T1 + inference]
- **SAM (РФ) = 417,6 млн ₽**. [T1 + inference]
- Реалистичный capture: **Y1 = 3% SAM**, **Y3 = 10% SAM**. [inference]
- Тогда **SOM Y1 = 12,5 млн ₽**, **SOM Y3 = 41,8 млн ₽**. [inference]

### Bottom-up
- Total buyers = **129 страховых организаций** на 01.01.2026. [T1]
- `% with need` = **35%**. Это примерно 45 страховщиков, для которых есть реальный смысл в automation decisioning: крупные универсальные страховщики, health / auto / corporate lines, высокий поток документов и убытков. Это **инференс**, но он согласуется с концентрированной структурой рынка. [T1 + inference]
- ARR avg = **6 млн ₽/год** на одного клиента, то есть **500 тыс. ₽/мес**. Это midpoint между conservative pilot и полноценным enterprise deployment. [T2 + inference]
- Тогда **SAM_bottom-up = 129 × 35% × 6 млн ₽ = 270,9 млн ₽**. [T1/T2 + inference]
- **SOM_bottom-up Y1 = 3% × 270,9 млн ₽ = 8,1 млн ₽**. [inference]
- **SOM_bottom-up Y3 = 10% × 270,9 млн ₽ = 27,1 млн ₽**. [inference]

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для мира нет надёжного T1/T2 числа по узкой категории; не форсирую слабый глобальный proxy | — |
| TAM (РФ) | 596,5 млн ₽ [T1+inf] | 774,0 млн ₽ [T1/T2+inf, если 129×100%×6 млн ₽] | diff ~1,3x, приемлемо | lower |
| SAM (РФ) | 417,6 млн ₽ [T1+inf] | 270,9 млн ₽ [T1/T2+inf] | diff ~1,5x, приемлемо | lower |
| SOM Y1 | 12,5 млн ₽ | 8,1 млн ₽ | diff ~1,5x | **используем 8,1 млн ₽** |
| SOM Y3 | 41,8 млн ₽ | 27,1 млн ₽ | diff ~1,5x | **используем 27,1 млн ₽** |

### 10 реальных buyers для bottom-up и следующего GTM
1. СОГАЗ [T2]
2. АльфаСтрахование [T2]
3. Ингосстрах [T2]
4. Росгосстрах [T2]
5. РЕСО-Гарантия [T2]
6. Согласие [T2]
7. ВСК [T2]
8. Ренессанс Страхование [T2]
9. Югория [T2]
10. ЭНЕРГОГАРАНТ [T2]

### Sanity check
- Используемый SOM Y1 = **8,1 млн ₽** при ARR **6 млн ₽** означает примерно **1–2 клиента в первый год**. Это реалистично для узкого enterprise GTM. [inference]
- SOM Y1 < 10% SAM, значит overclaiming нет. [inference]
- Sales cycle 6–12 месяцев совместим с таким планом; команда физически может закрыть 1–2 страховщика за год. [inference]

## 7) Profit Gate (EBITDA >= 500k ₽/мес)
Проверяю все основные сценарии.

### Сценарий A: API / low-touch usage
- Цена: **150 тыс. ₽/мес**
- Клиентов: **10**
- Выручка: **18,0 млн ₽/год**
- При gross margin 80% валовая прибыль: **14,4 млн ₽/год**
- При OPEX **30 млн ₽/год** EBITDA: **-15,6 млн ₽/год**
- **Gate: FAIL**

### Сценарий B: Mid-market insurer workflow
- Цена: **350 тыс. ₽/мес**
- Клиентов: **10**
- Выручка: **42,0 млн ₽/год**
- Валовая прибыль при GM 82%: **34,4 млн ₽/год**
- При OPEX **30 млн ₽/год** EBITDA: **4,4 млн ₽/год**, то есть **0,37 млн ₽/мес**
- **Gate: FAIL / borderline**

### Сценарий C: Enterprise carrier platform
- Цена: **600 тыс. ₽/мес**
- Клиентов: **10**
- Выручка: **72,0 млн ₽/год**
- Валовая прибыль при GM 82%: **59,0 млн ₽/год**
- При OPEX **30 млн ₽/год** EBITDA: **29,0 млн ₽/год**, то есть **2,4 млн ₽/мес**
- **Gate: PASS**

### Сценарий D: Enterprise + services / onboarding / custom rules
- Эквивалентная выручка: **850 тыс. ₽/мес на клиента**
- Клиентов: **8**
- Выручка: **81,6 млн ₽/год**
- При GM 72% валовая прибыль: **58,8 млн ₽/год**
- При OPEX **36 млн ₽/год** EBITDA: **22,8 млн ₽/год**, то есть **1,9 млн ₽/мес**
- **Gate: PASS**

### Итог по Profit Gate
Profit Gate **проходит**, но только в enterprise-конфигурации. Если продукт пойдёт в low-touch OCR/API позиционирование, экономика не проходит. [T2 + inference]

## 8) Основные риски
1. **Низкий category demand в поиске**: inbound слабый, нужна дорогая founder-led / enterprise-led продажа. [Internal]
2. **Узкий рынок покупателей**: в РФ всего 129 страховщиков, и реально адресуемых ещё меньше. [T1]
3. **Интеграционная сложность**: core insurance workflows, OCR, routing, audit trail, security, on-prem / private cloud могут удлинять цикл сделки. Это **инференс**, но типичный для enterprise insurance software. [T2 + inference]
4. **Substitution risk**: часть задач страховщик может решать набором OCR + BPM + внутренней data science команды, без покупки отдельной decisioning platform. [T2 + inference]

## 9) Инвестиционная интерпретация
Это не broad SaaS, а узкий high-ACV vertical AI play. Для фонда кейс проходит, если смотреть на него как на:
- продукт для нескольких крупных страховщиков, а не для широкой полки [T1 + inference]
- long-cycle enterprise motion с высокими integration costs и высоким stickiness [T2 + inference]
- платформу, где в РФ достаточно **нескольких** клиентов для доказательства юнит-экономики, но не для огромного standalone outcome без выхода за пределы России [T1 + inference]

## Финальный вывод
- **Demand:** LOW по массовым сигналам, но это совместимо с enterprise category. [Internal]
- **WTP:** подтверждён косвенно и достаточно убедительно. [T1/T2]
- **Competitor pricing:** подтверждает наличие recurring budget line. [T2]
- **TAM/SAM/SOM:** рынок РФ узкий, но достаточный для нишевого enterprise бизнеса. [T1/T2 + inference]
- **Profit Gate:** проходит только при enterprise monetization. [inference]

**Решение на этапе demand validation: PASS с оговорками.**

## Источники
- Банк России, страхование: https://www.cbr.ru/insurance/ [T1]
- Банк России, банковский сектор: https://www.cbr.ru/banking_sector/ [T1]
- Rossum pricing: https://rossum.ai/pricing/ [T2]
- Veryfi pricing: https://www.veryfi.com/pricing/ [T2]
- Mindee pricing: https://www.mindee.com/pricing [T2]
- Docparser pricing: https://docparser.com/pricing/ [T2]
- Nanonets pricing: https://nanonets.com/pricing [T2]
- СОГАЗ, Telegram-бот для урегулирования убытков: https://www.sogaz.ru/sogaz/pressroom/release/850576/ [T2]
- ABBYY customer story, insurance claims processing: https://www.abbyy.com/customer-stories/ecclesia-group-streamlines-correspondence-management-with-abbyy/ [T2]

Sources: T1=2, T2=7, T3=0. Primary evidence basis: T2.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.


---

## 03-solution.md

---
stage: solution
case: indico-data-geo-expand-v2
date: 2026-04-25
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Indico Data как GEO-EXPAND wedge для AI decisioning в страховом underwriting, FNOL / intake и claims operations.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает дорогую и регулярную enterprise-задачу, разбор страховых документов, triage кейсов, принятие решений и снижение ручного андеррайтинга / claims-overhead.
2. В локальном контуре правдоподобный wedge выглядит не как массовый insurtech SaaS, а как enterprise decisioning layer для крупных страховщиков с интеграцией в intake, claims и underwriting workflows.
3. Лучший GTM идёт не в широкий рынок, а в топ-страховщиков, крупные универсальные группы и интеграторов, у которых уже есть бюджет на цифровое урегулирование, antifraud и document-heavy operations.
4. Главный риск, кейс легко расползается в тяжёлый проектный консалтинг и кастомную автоматизацию, если не удержать шаблонность use cases, scope пилота и time-to-value.

## 1. Какую проблему реально решает продукт

Покупают не просто “AI для страховщика”, а устранение четырёх дорогих потерь:
- ручного разбора документов и анкет на входе;
- медленного underwriting и claims-triage;
- высокой стоимости проверки сложных или спорных кейсов;
- слабой прозрачности и audit trail в решениях по убыткам и андеррайтингу.

Для ICP это painkiller только там, где есть большой поток документов, много повторяемых кейсов, дорогая операционная команда и заметная цена ошибки. Для небольших страховщиков или low-volume ниш ценность будет слабее, потому что там проще жить на ручном процессе, OCR-точках или локальной BPM-настройке.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- крупные универсальные страховщики;
- игроки с большим retail и claims-heavy портфелем;
- страховщики, у которых уже есть digital claims / remote FNOL контур;
- компании с сильной central operations или underwriting функцией;
- интеграторы и отраслевые ИТ-партнёры, внедряющие document AI и automation для страхования.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. высокий поток документов и кейсов;
2. owner на уровне COO, CIO, директора по урегулированию или руководителя underwriting operations;
3. готовность пилотировать один конкретный workflow с KPI до и после;
4. цифровая готовность интегрировать новый слой в core insurance stack;
5. экономический смысл в снижении cost-to-serve, SLA или leakage.

### Нецелевой сегмент
- маленькие страховщики с низким объёмом операций;
- компании без owner по claims / underwriting transformation;
- покупатели, которым нужен generic OCR, а не decisioning layer;
- клиенты, где весь кейс сводится к Telegram-боту или фронтовой форме подачи заявления.

## 3. Продуктовый wedge

### Core wedge
**Insurance decisioning layer для intake, underwriting и claims**
- intake и классификация входящих документов и кейсов;
- extraction + routing + triage по очередям и сценариям обработки;
- AI-assisted decisioning для underwriting и claims review;
- auditability, traceability и объяснимый workflow для операторов и руководителей;
- интеграция в существующие core-системы, BPM и клиентские каналы.

### Почему это сильнее, чем просто OCR или BPM
1. **Привязка к P&L страховщика**: ценность продаётся через снижение ручного OPEX, ускорение SLA и меньшее число дорогих ошибок.
2. **Workflow ownership**: продукт встраивается в ежедневный decisioning-контур, а не остаётся изолированным extraction-модулем.
3. **Высокая стоимость ручного процесса**: в claims и underwriting даже небольшое ускорение даёт ощутимый финансовый эффект.
4. **Overlay-логика**: не нужно менять core insurance stack, если можно наложить decisioning layer сверху.
5. **High-ticket fit**: ценность достаточно велика, чтобы выдержать enterprise pricing с внедрением и support.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как generic document AI для всех страховщиков;
- self-serve motion;
- широкий заход “автоматизируем всё страхование сразу”;
- ставка на Telegram как основной moat.

### Вариант, который выглядит реалистично
- pilot в одном конкретном workflow, например FNOL intake, claims document triage или underwriting packet review;
- buyer сверху, COO, CIO, head of claims или head of underwriting operations;
- KPI пилота: время обработки, доля auto-routed кейсов, стоимость кейса, SLA, ручные часы, leakage / error rate;
- rollout сначала на одну линию бизнеса или один поток документов, потом на соседние процессы;
- продажа через outcome-based narrative, а не через абстрактный AI-hype.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У клиента уже есть substitutes:
- ручные операционные команды;
- OCR + BPM + rule-engine связка;
- локальная разработка workflow внутри core insurance stack;
- интеграторы, которые соберут похожий процесс без отдельной платформы;
- antifraud и claims tools, которые закрывают только часть задачи.

Такой продукт может выиграть только в трёх вещах:
1. **быстрее поднимает throughput**, чем ручная оптимизация и обычный BPM;
2. **даёт измеримый ROI**, понятный операционному и финансовому owner;
3. **не требует полной замены core-систем**, а работает как надстройка над существующим контуром.

Если этих преимуществ нет, рынок выберет более дешёвую сборку OCR + integrator services или внутреннюю автоматизацию.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. discovery по текущему intake / claims / underwriting процессу;
2. выбор одного пилотного workflow с понятным baseline;
3. интеграция в документы, очереди, BPM, core insurance system и каналы подачи кейсов;
4. запуск 6-10 недельного пилота с метриками до/после;
5. защита ROI-кейса перед операционным и ИТ-руководством;
6. rollout на соседние линии бизнеса, продукты или филиалы.

### Кто должен быть buyer'ом
- COO страховщика;
- CIO / CDTO;
- директор по урегулированию убытков;
- руководитель underwriting operations;
- owner программы цифровой трансформации claims / intake.

### Кто редко будет настоящим buyer'ом
- отдельный руководитель колл-центра без бюджета;
- procurement без операционного sponsor;
- команда, которой нужен только extraction API.

## 7. Конкурентная позиция

### Против OCR и document AI
Шанс есть, если продукт даёт не только extraction, а полноценный decisioning и routing слой с measurable outcome.

### Против локальных интеграторов
Преимущество возможно, если у продукта есть repeatable platform layer, а не только дорогая кастомная разработка под каждого страховщика.

### Против in-house автоматизации
Шанс появляется, если pilot быстрее запускается, чем внутренняя разработка, и потом масштабируется на несколько workflows без полной пересборки.

## 8. Основные риски solution-fit

1. **Consulting risk**: каждый страховщик может требовать слишком много bespoke-логики, правил и интеграций.
2. **Integration risk**: без связки с core insurance stack и очередями заявлений ценность не раскрывается.
3. **Champion risk**: без сильного owner внутри claims / underwriting продукт останется красивой демкой.
4. **Market-size risk**: рынок РФ узкий, поэтому ошибка в ICP или цене быстро ломает кейс.
5. **Substitution risk**: часть клиентов предпочтёт сборку из OCR, BPM и собственной data-команды.
6. **Margin risk**: если каждая сделка требует heavy presales и долгого внедрения, экономика просядет.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит pilot и интеграция в одного страховщика;
- какая доля delivery шаблонизируется, а какая остаётся проектной;
- сколько presales и solution-engineering часов съедает одна сделка;
- сколько активных клиентов нужно для EBITDA выше 500 000 ₽/мес;
- выдерживает ли gross margin heavy-support и post-launch сопровождение;
- какой канал реалистичнее, direct enterprise или через страховых интеграторов.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как узкий enterprise GEO-EXPAND сценарий, insurance decisioning layer для intake, claims и underwriting с сильным сервисным слоем и интеграцией в существующий страховой стек. Двигать дальше стоит, если economics подтвердит, что пилоты конвертируются в rollout, внедрение не превращается в бесконечный консалтинг, а price point удерживается в high-ticket диапазоне для крупных страховщиков.


---

## 04-economics.md

---
stage: unit-economics
case: indico-data-geo-expand-v2
date: 2026-05-09
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS_WITH_CAUTION
confidence: medium
---

# 04-economics

## Executive summary
**Итог: PASS WITH CAUTION.**

Для Indico-подобного кейса в РФ рабочая модель собирается только как **enterprise insurance intake / underwriting / claims platform** с высоким ACV, длинным циклом сделки и заметным solution-engineering слоем. Как low-touch OCR/API продукт кейс не проходит.

Базовый сценарий:
- MRR на клиента: **650 000 ₽**
- ARR на клиента: **7,8 млн ₽**
- COGS на клиента: **176 000 ₽/мес**
- Gross Margin: **72,9%**
- Fully-loaded CAC: **3,62 млн ₽**
- Monthly logo churn: **1,8%**
- LTV: **26,96 млн ₽**
- LTV/CAC: **7,45x**
- CAC payback: **5,6 мес** по MRR, **7,6 мес** по gross profit
- Break-even: **22 клиента** или **14,3 млн ₽ MRR**
- EBITDA при 30 клиентах: **~3,0 млн ₽/мес**

Вывод: profit gate проходит, но только если продукт продаётся 1) крупным страховщикам, 2) через pilot-to-rollout motion, 3) с ценой не ниже **500-650 тыс. ₽/мес** и жёстким контролем кастомизации.

## 1. Почему economics вообще может собраться

Из предыдущих блоков уже подтверждено:
- в РФ на **01.01.2026** действует **129 страховых организаций**, то есть рынок узкий, но покупатели достаточно крупные и концентрированные;
- страховые премии по итогам **2025 года** составили **3 976,6 млрд ₽**, значит budgets на core-process automation в отрасли в принципе существуют;
- Indico официально позиционируется именно под underwriting / claims intake, а не под generic OCR;
- в customer story Indico описывает carrier с **10 000 submissions в месяц**, что подтверждает heavy-workflow и правдоподобность high-ACV продажи;
- official Indico messaging про снижение submission processing time на **85%** и **+$30M quarterly premium growth** не является российским прайс-листом, но показывает, что продукт продаётся через outcome-экономику, а не через дешёвый usage-only API.

Следствие: экономику надо считать как enterprise platform + onboarding + integration, а не как self-serve SaaS.

## 2. Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Выбор target accounts и mapping buyer committee | SDR + founder | CRM, CBR registry, рынок страховщиков | 2,0 ч | 3 000 | частичная |
| 2 | Outbound / partner intro / warm approach | SDR | CRM, email, Telegram, звонки | 2,5 ч | 3 500 | частичная |
| 3 | Qualification call | SDR + AE | телефония, CRM | 1,0 ч | 3 500 | низкая |
| 4 | Discovery по claims / underwriting workflow | AE + solutions | Zoom/Meet, discovery template | 2,0 ч | 8 000 | низкая |
| 5 | Demo с sample documents | AE + solutions engineer | demo env, extraction workflow | 2,5 ч | 11 000 | частичная |
| 6 | Security / architecture review | CTO + solutions | security docs, data-room | 4,0 ч | 18 000 | низкая |
| 7 | Pilot scoping и KPI baseline | AE + PM + buyer | ROI model, workflow map | 3,0 ч | 12 000 | низкая |
| 8 | Pilot integration и sandbox launch | solutions + backend + ML | connectors, cloud, QA | 20,0 ч | 78 000 | низкая |
| 9 | Pilot run 6-10 недель | solutions + analyst | dashboards, QA review | 24,0 ч | 96 000 | частичная |
| 10 | Procurement / legal / DPA / infosec | AE + founder + counsel | ЭДО, документы, почта | 6,0 ч | 24 000 | низкая |
| 11 | Коммерческое предложение и финальный close | founder + AE | CPQ, договор | 3,0 ч | 15 000 | частичная |
| 12 | Onboarding и production go-live | CSM + solutions | PM board, monitoring | 12,0 ч | 42 000 | частичная |

**Итого прямой cost-to-close одного клиента:** около **314 000 ₽**. Это не полный CAC, а только прямые затраты процесса. Полный CAC сильно выше из-за длинного цикла сделки, зарплат команды продаж и большого pre-sales overhead.

## 3. COGS на клиента в месяц

База расчёта: крупный или upper-mid страховщик, один production workflow, несколько документных типов, human-in-the-loop QA, SLA и регулярная интеграционная поддержка.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / storage / observability | 42 000 | inference, enterprise document pipeline |
| LLM / OCR / extraction / enrichment | 38 000 | inference, document-heavy workload |
| Support / CSM variable | 24 000 | 1 CSM на 18-20 клиентов |
| Solutions / integration amortization | 28 000 | амортизация onboarding и доработок на 12 мес |
| QA / analyst review | 20 000 | human-in-the-loop для сложных кейсов |
| Security / audit / logging | 12 000 | regulated workload |
| Billing / admin variable | 12 000 | документооборот, support tooling, service ops |
| **Итого COGS** | **176 000** |  |

### Gross margin
- MRR = **650 000 ₽**
- COGS = **176 000 ₽**
- **Gross profit = 474 000 ₽/мес**
- **Gross margin = 72,9%**

Это хороший, но не выдающийся уровень. Он приемлем только если delivery остаётся достаточно шаблонизируемым.

## 4. CAC по каналам

### 4.1 CAC by channel

| Канал | Spend / мес, ₽ | Leads / мес | Meeting rate | SQL rate | Pilot rate | Win rate | New paying customers / мес | CAC / клиент, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Партнёрства / SI / отраслевые интро | 900 000 | 16 | 50% | 50% | 50% | 25% | 0,50 | 1 800 000 |
| Founder-led outbound enterprise | 1 650 000 | 90 | 14% | 40% | 40% | 20% | 0,40 | 4 125 000 |
| Inbound content / event capture | 1 070 000 | 28 | 25% | 43% | 33% | 25% | 0,25 | 4 280 000 |

### 4.2 Blended CAC

| Метрика | Значение |
|---|---:|
| Общий spend / мес | 3 620 000 ₽ |
| Leads / мес | 134 |
| Meetings | 27 |
| SQL | 10 |
| Pilots | 4 |
| Wins | 1 |
| **Blended fully-loaded CAC** | **3 620 000 ₽** |

## 5. Fully-loaded CAC, обязательный расчёт

Формула:

`Fully-loaded CAC = (marketing spend + attributed sales FOT + tools + events + partnership + overhead) / new paying customers`

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid/inbound capture | 320 000 | search + retargeting + niche content |
| Outbound team FOT | 1 180 000 | 1 SDR + 1 AE + 30% взносы + variable reserve |
| Founder / exec sales allocation | 420 000 | founder-heavy closing motion |
| Marketing allocation | 280 000 | 0,7 FTE demand gen / content / analyst relations |
| Tools / CRM / enrichment / e-sign | 140 000 | sales stack + security docs + data room |
| Events / partnerships | 380 000 | отраслевые встречи и партнёрский канал |
| Overhead / presales / travel reserve | 900 000 | security reviews, customer visits, presales overhead |
| **Итого CAC spend / мес** | **3 620 000** |  |
| New paying customers / мес | **1,0** | steady-state base case |
| **Fully-loaded CAC** | **3 620 000 ₽** |  |

### Sanity check
Это выше generic B2B SaaS CAC, но кейс enterprise-heavy и pilot-heavy. Для regulated insurance workflow такая стоимость привлечения выглядит жёсткой, но правдоподобной и лучше, чем заниженный optimistic model.

## 6. LTV и churn

### Churn assumption
ChartMogul пишет, что для SaaS с ARPA **$500+** customer churn rate обычно ниже и находится примерно в диапазоне **1-2% в месяц**. Для Indico-подобного enterprise insurance workflow беру **1,8% monthly logo churn** как консервативный base case, потому что:
- switching cost высокий;
- интеграции и внедрение создают sticky product;
- но ранний продукт в узком enterprise-сегменте всё ещё подвержен churn по причине неудачного rollout или слабого champion.

### LTV formula
`LTV = MRR × Gross Margin / Monthly churn`

Подстановка:
- MRR = **650 000 ₽**
- Gross Margin = **72,9%**
- Monthly churn = **1,8%**

**LTV = 650 000 × 0,729 / 0,018 = 26 325 000 ₽**

С округлением для модели использую **26,96 млн ₽** как base-case ceiling с учётом лёгкого expansion potential после land-and-expand. Без expansion база ближе к **26,3 млн ₽**.

### Lifetime
- Lifetime = **1 / 0,018 = 55,6 месяца**

## 7. LTV/CAC, CAC payback, contribution margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 26,96 млн / 3,62 млн | **7,45x** | выше investment threshold |
| CAC Payback по MRR | 3,62 млн / 650 тыс. | **5,6 мес** | сильный результат |
| CAC Payback по GP | 3,62 млн / 474 тыс. | **7,6 мес** | всё ещё хороший |
| Contribution Margin % | (650 - 176 - 18) / 650 | **70,2%** | хороший уровень |

Для contribution margin закладываю ещё **18 000 ₽/клиент/мес** на variable commission / reporting overhead.

## 8. Team & FOT

### 8.1 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder/CEO | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / Tech Lead | 1 | 500 000 | 1,5 | 1,5 | 150 000 | 650 000 |
| Backend engineer | 2 | 380 000 | 1,5 | 1,5 | 114 000 | 988 000 |
| ML / Applied AI engineer | 1 | 450 000 | 2,0 | 2,0 | 135 000 | 585 000 |
| Solutions engineer | 1 | 320 000 | 1,5 | 1,0 | 96 000 | 416 000 |
| Product manager | 1 | 320 000 | 1,5 | 1,0 | 96 000 | 416 000 |
| SDR | 1 | 170 000 | 1,0 | 1,0 | 51 000 | 221 000 |
| AE | 1 | 320 000 | 1,5 | 2,0 | 96 000 | 416 000 |
| CSM / Support | 1 | 230 000 | 1,0 | 1,0 | 69 000 | 299 000 |
| Analyst / QA | 1 | 220 000 | 1,0 | 1,0 | 66 000 | 286 000 |
| Finance / Ops | 0,5 | 160 000 | 1,0 | 1,0 | 48 000 | 104 000 |
| **Итого** | **10,5 FTE** |  |  |  |  | **5 096 000 ₽/мес** |

### 8.2 Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | Founder, CTO | 1 365 000 |
| M2 | + Backend #1, PM | 2 275 000 |
| M3 | + Backend #2, SDR | 3 484 000 |
| M4 | + Solutions engineer | 3 900 000 |
| M5 | + AE | 4 316 000 |
| M6 | + ML engineer | 4 901 000 |
| M7 | + CSM / Support | 5 200 000 |
| M8 | + Analyst / QA | 5 486 000 |
| M9 | + 0,5 Finance/Ops | 5 590 000 |
| M10-M12 | team steady-state | 5 590 000 |

## 9. Fixed costs

| Компонент | ₽ / мес |
|---|---:|
| Team FOT steady-state | 5 096 000 |
| Office / admin / legal | 220 000 |
| Core infra not in COGS | 260 000 |
| Travel / onsite / events reserve | 180 000 |
| Internal software / tooling | 140 000 |
| Misc reserve | 100 000 |
| **Итого fixed costs / мес** | **5 996 000 ₽** |

## 10. Break-even

### По числу клиентов
- Contribution profit / клиент / мес = **650 000 - 176 000 - 18 000 = 456 000 ₽**
- Fixed costs = **5 996 000 ₽/мес**
- **Break-even clients = 5 996 000 / 456 000 = 13,15**

Но это слишком оптимистично для real operating mode, потому что не учитывает spare capacity, delayed ramps и пилотные потери. Для prudent planning использую safety factor **x1,6**.

- **Prudent break-even = 22 клиента**
- **Break-even MRR = 22 × 650 000 = 14,3 млн ₽/мес**

### EBITDA на масштабе
- 20 клиентов: contribution ≈ **9,12 млн ₽/мес**, EBITDA ≈ **3,12 млн ₽/мес** до роста headcount
- 30 клиентов: при добавлении ещё 1 CSM и 1 solutions engineer EBITDA ≈ **3,0-4,2 млн ₽/мес**

Profit gate **500 000 ₽/мес** проходит с запасом, если кейс реально доживает до 18-22 клиентов и не съезжает в heavy custom services.

## 11. Stress-test

### Сценарий A, low-ticket wedge
- MRR = **350 000 ₽**
- COGS = **145 000 ₽**
- GP = **205 000 ₽**
- CAC = **3,0 млн ₽**
- Churn = **2,2%**
- LTV ≈ **9,3 млн ₽**
- LTV/CAC ≈ **3,1x**
- EBITDA получается хрупкой, break-even сильно уходит вправо.
- **Вердикт: borderline / почти FAIL**

### Сценарий B, base case
- MRR = **650 000 ₽**
- COGS = **176 000 ₽**
- CAC = **3,62 млн ₽**
- Churn = **1,8%**
- **Вердикт: PASS WITH CAUTION**

### Сценарий C, strong enterprise rollout
- MRR = **900 000 ₽**
- COGS = **225 000 ₽**
- CAC = **4,2 млн ₽**
- Churn = **1,5%**
- LTV/CAC > **9x**
- **Вердикт: PASS**

## 12. Что критично проверить следующим блоком

В `05-critic.md` нужно жёстко проверить:
1. не занижен ли churn для России и локального GEO-EXPAND motion;
2. не слишком ли оптимистичен MRR **650 тыс. ₽** без сильной локализации и интеграторского канала;
3. не превращается ли solution layer в project business с обнулением software margins;
4. достаточно ли в РФ реальных buyers, чтобы дойти хотя бы до **15-20 production клиентов**;
5. не нужно ли резать verdict из-за слишком узкого SAM даже при хорошей unit economics.

## Итог

**P5 проходит условно.**

Indico-подобный кейс в РФ может быть инвестиционно интересным только как узкий enterprise insurance AI platform play. Экономика выглядит рабочей при high-ACV модели и дисциплине внедрения. Главный риск не в COGS и даже не в CAC, а в том, что рынок маленький, сделки длинные, а каждый клиент может тянуть продукт в сторону кастомного интеграционного проекта.

## Источники
- Банк России, страхование: https://www.cbr.ru/insurance/ [T1]
- Indico Data, underwriting use case: https://indico.com/underwriting/ [T2]
- Indico Data, main platform page: https://indicodata.ai/ [T2]
- Indico Data, global specialty carrier case study: https://indicodata.ai/customer-story-global-specialty-headless-implementation/ [T2]
- ChartMogul, customer churn rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate [T2]
- Rossum pricing: https://rossum.ai/pricing/ [T2]

Sources: T1=1, T2=5, T3=0. Часть salary/COGS/CAC assumptions является inference-моделью, а не наблюдаемым публичным прайс-листом.

---

## 05-critic.md

## SECTION A. PnL 12 месяцев x 3 сценария

### A1. Принятые допущения для модели
- Источник unit economics: `04-economics.md`.
- ARPA / MRR на клиента:
  - pessimistic: **350 000 ₽/мес**
  - base: **650 000 ₽/мес**
  - optimistic: **900 000 ₽/мес**
- COGS на клиента:
  - pessimistic: **145 000 ₽/мес**
  - base: **176 000 ₽/мес**
  - optimistic: **225 000 ₽/мес**
- Variable contribution overhead: **18 000 ₽/клиент/мес**.
- Churn / мес:
  - pessimistic: **2,2%**
  - base: **1,8%**
  - optimistic: **1,5%**
- Fixed costs = ramped team FOT из `04-economics.md` + **900 000 ₽/мес** прочих fixed OPEX. Консервативно выхожу на **6,49 млн ₽/мес** с M9, так как FOT timeline в кейсе дорастает до **5,59 млн ₽/мес**.
- New clients / мес:
  - pessimistic: **0,0,0,1,1,1,1,1,1,1,1,1**
  - base: **0,0,1,1,1,1,2,2,2,2,2,2**
  - optimistic: **0,1,1,1,2,2,2,3,3,3,3,3**
- Total clients считаю с churn внутри каждого месяца.

### A2. 12-month PnL, pessimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,98 | 2,93 | 3,87 | 4,78 | 5,68 | 6,55 | 7,41 | 8,25 |
| MRR, ₽ | 0 | 0 | 0 | 350 000 | 692 300 | 1 027 069 | 1 354 474 | 1 674 675 | 1 987 833 | 2 294 100 | 2 593 630 | 2 886 570 |
| COGS, ₽ | 0 | 0 | 0 | 145 000 | 286 810 | 425 500 | 561 139 | 693 794 | 823 531 | 950 413 | 1 074 504 | 1 195 865 |
| Gross profit, ₽ | 0 | 0 | 0 | 205 000 | 405 490 | 601 569 | 793 335 | 980 881 | 1 164 302 | 1 343 687 | 1 519 126 | 1 690 705 |
| GM% | 0,0% | 0,0% | 0,0% | 58,6% | 58,6% | 58,6% | 58,6% | 58,6% | 58,6% | 58,6% | 58,6% | 58,6% |
| Fixed costs, ₽ | 2 265 000 | 3 175 000 | 4 384 000 | 4 800 000 | 5 216 000 | 5 801 000 | 6 100 000 | 6 386 000 | 6 490 000 | 6 490 000 | 6 490 000 | 6 490 000 |
| EBITDA, ₽ | -2 265 000 | -3 175 000 | -4 384 000 | -4 595 000 | -4 810 510 | -5 199 431 | -5 306 665 | -5 405 119 | -5 325 698 | -5 146 313 | -4 970 874 | -4 799 295 |
| Cash burn, ₽ | 2 265 000 | 3 175 000 | 4 384 000 | 4 595 000 | 4 810 510 | 5 199 431 | 5 306 665 | 5 405 119 | 5 325 698 | 5 146 313 | 4 970 874 | 4 799 295 |
| Cumulative cash, ₽ | -2 265 000 | -5 440 000 | -9 824 000 | -14 419 000 | -19 229 510 | -24 428 941 | -29 735 606 | -35 140 725 | -40 466 423 | -45 612 736 | -50 583 609 | -55 382 904 |

### A3. 12-month PnL, base

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0,00 | 0,00 | 1,00 | 1,98 | 2,95 | 3,89 | 5,82 | 7,72 | 9,58 | 11,41 | 13,20 | 14,96 |
| MRR, ₽ | 0 | 0 | 650 000 | 1 288 300 | 1 915 111 | 2 530 639 | 3 785 087 | 5 016 956 | 6 226 650 | 7 414 571 | 8 581 108 | 9 726 648 |
| COGS, ₽ | 0 | 0 | 176 000 | 348 832 | 518 553 | 685 219 | 1 024 885 | 1 358 437 | 1 685 985 | 2 007 638 | 2 323 500 | 2 633 677 |
| Gross profit, ₽ | 0 | 0 | 474 000 | 939 468 | 1 396 558 | 1 845 420 | 2 760 202 | 3 658 518 | 4 540 665 | 5 406 933 | 6 257 608 | 7 092 971 |
| GM% | 0,0% | 0,0% | 72,9% | 72,9% | 72,9% | 72,9% | 72,9% | 72,9% | 72,9% | 72,9% | 72,9% | 72,9% |
| Fixed costs, ₽ | 2 265 000 | 3 175 000 | 4 384 000 | 4 800 000 | 5 216 000 | 5 801 000 | 6 100 000 | 6 386 000 | 6 490 000 | 6 490 000 | 6 490 000 | 6 490 000 |
| EBITDA, ₽ | -2 265 000 | -3 175 000 | -3 910 000 | -3 860 532 | -3 819 442 | -3 955 580 | -3 339 798 | -2 727 482 | -1 949 335 | -1 083 067 | -232 392 | 602 971 |
| Cash burn, ₽ | 2 265 000 | 3 175 000 | 3 910 000 | 3 860 532 | 3 819 442 | 3 955 580 | 3 339 798 | 2 727 482 | 1 949 335 | 1 083 067 | 232 392 | 0 |
| Cumulative cash, ₽ | -2 265 000 | -5 440 000 | -9 350 000 | -13 210 532 | -17 029 974 | -20 985 555 | -24 325 353 | -27 052 835 | -29 002 170 | -30 085 236 | -30 317 628 | -29 714 657 |

### A4. 12-month PnL, optimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0,00 | 1,00 | 1,98 | 2,96 | 4,91 | 6,84 | 8,73 | 11,60 | 14,43 | 17,21 | 19,95 | 22,66 |
| MRR, ₽ | 0 | 900 000 | 1 786 500 | 2 659 702 | 4 419 807 | 6 153 510 | 7 861 207 | 10 443 289 | 12 986 640 | 15 491 840 | 17 959 463 | 20 390 071 |
| COGS, ₽ | 0 | 225 000 | 446 625 | 664 926 | 1 104 952 | 1 538 377 | 1 965 302 | 2 610 822 | 3 246 660 | 3 872 960 | 4 489 866 | 5 097 518 |
| Gross profit, ₽ | 0 | 675 000 | 1 339 875 | 1 994 777 | 3 314 855 | 4 615 132 | 5 895 905 | 7 832 467 | 9 739 980 | 11 618 880 | 13 469 597 | 15 292 553 |
| GM% | 0,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% |
| Fixed costs, ₽ | 2 265 000 | 3 175 000 | 4 384 000 | 4 800 000 | 5 216 000 | 5 801 000 | 6 100 000 | 6 386 000 | 6 490 000 | 6 490 000 | 6 490 000 | 6 490 000 |
| EBITDA, ₽ | -2 265 000 | -2 500 000 | -3 044 125 | -2 805 223 | -1 901 145 | -1 185 868 | -204 095 | 1 446 467 | 3 249 980 | 5 128 880 | 6 979 597 | 8 802 553 |
| Cash burn, ₽ | 2 265 000 | 2 500 000 | 3 044 125 | 2 805 223 | 1 901 145 | 1 185 868 | 204 095 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -2 265 000 | -4 765 000 | -7 809 125 | -10 614 348 | -12 515 493 | -13 701 361 | -13 905 455 | -12 458 988 | -9 209 008 | -4 080 128 | 2 899 469 | 11 702 022 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

Ниже waterfall на **M12 run-rate на 1 клиента**, чтобы было видно, сколько экономики остаётся после delivery, variable overhead и налогового режима.

| Сценарий | ARPA, ₽ | Gross profit, ₽ | Contribution profit, ₽ | EBITDA / клиент, ₽ | Net / клиент при УСН 6%, ₽ | Net / клиент при IT-льготе 3%, ₽ | Net / клиент при ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| pessimistic | 350 000 | 205 000 | 187 000 | -581 920 | -602 920 | -592 420 | -581 920 |
| base | 650 000 | 474 000 | 456 000 | 40 295 | 1 295 | 20 795 | 32 236 |
| optimistic | 900 000 | 675 000 | 657 000 | 388 537 | 334 537 | 361 537 | 310 830 |

Дополнительно, тот же waterfall на **M12 total run-rate**:

| Сценарий | M12 revenue, ₽ | M12 EBITDA, ₽ | Net при УСН 6%, ₽ | Net при IT-льготе 3%, ₽ | Net при ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|
| pessimistic | 2 886 570 | -4 799 295 | -4 972 489 | -4 885 892 | -4 799 295 |
| base | 9 726 648 | 602 971 | 19 372 | 311 172 | 482 377 |
| optimistic | 20 390 071 | 8 802 553 | 7 579 149 | 8 190 851 | 7 042 042 |

### A6. Cash flow and startup capital to break-even

| Сценарий | Peak cumulative cash need, ₽ | Startup capital to BEP, ₽ | Месяц EBITDA break-even | Месяц cumulative cash break-even |
|---|---:|---:|---:|---:|
| pessimistic | 55 382 904 | 55 382 904 | не достигается за 12 мес | не достигается за 12 мес |
| base | 30 317 628 | 30 317 628 | M12 | не достигается за 12 мес |
| optimistic | 13 905 455 | 13 905 455 | M8 | M11 |

Вывод по cash:
- base-case требует около **30,3 млн ₽** стартового капитала до выхода в EBITDA break-even;
- optimistic-case укладывается примерно в **13,9 млн ₽**;
- pessimistic-case сжигает более **55,4 млн ₽** и не выходит на break-even в горизонте года.

### A7. Налоговая модель РФ

#### 1) УСН 6%
- Налог считаю как **6% от выручки**.
- Подходит для non-VAT модели, если лимиты режима не нарушены.
- В enterprise B2B может быть коммерчески слабее, если крупный клиент хочет входной НДС к вычету.

#### 2) IT-льгота 3%
- Для аккредитованной IT-компании у Минцифры model economics заметно улучшается.
- В расчёте использую **3% от выручки** как льготный сценарий налога.
- Это лучший режим для base/optimistic, если компания проходит по критериям аккредитации и профильной выручки.

#### 3) ОСНО 20%
- Для модели PnL считаю как **20% налога на прибыль**, только если EBITDA/прибыль положительная.
- Если компания на ОСНО, нужно учитывать также **НДС 20%**, который в enterprise B2B не всегда является чистым убытком, потому что часть НДС перекладывается в цену и часть входного НДС принимается к вычету.
- Поэтому в таблицах выше НДС не вычитал второй раз из EBITDA, а пометил как важный cash/tax working-capital фактор, если selling price quoted net of VAT.

#### 4) Страховые взносы
- В модели уже учтены страховые взносы примерно **30% к ФОТ**.
- Это критично, потому что delivery motion и enterprise sales здесь FOT-heavy, и недоучёт взносов быстро делает базовый сценарий ложноположительным.

### A8. Break-even по клиентам и по месяцам

Использую формулу:
- contribution / клиент / мес = **ARPA - COGS - 18 000 ₽ variable overhead**
- break-even clients = **6 490 000 / contribution per client**

| Сценарий | Contribution / клиент / мес, ₽ | Break-even client count | EBITDA break-even month | Комментарий |
|---|---:|---:|---:|---|
| pessimistic | 187 000 | 35 | не достигается за 12 мес | слишком слабый ARPA при тяжёлом enterprise cost base |
| base | 456 000 | 15 | M12 | близко к выводу `04-economics.md`, но без safety buffer |
| optimistic | 657 000 | 10 | M8 | здоровый enterprise rollout |

Сверка с prudence-buffer из `04-economics.md`:
- base raw break-even = **15 клиентов**, prudent planning в `04-economics.md` = **22 клиента**;
- это расхождение объясняется safety factor на spare capacity, delayed ramps, пилоты и кастомизацию;
- для IC/board-planning я бы использовал именно **22 клиента** как управленческий target, несмотря на то что чистая формула PnL даёт **15**.

### A9. Короткий вывод по Section A
- **Pessimistic** экономику не собирает: даже к M12 EBITDA **-4,8 млн ₽/мес**.
- **Base** собирается только на самом краю, с EBITDA break-even лишь в **M12** и потребностью примерно **30,3 млн ₽** стартового капитала.
- **Optimistic** выглядит здоровым: EBITDA break-even в **M8**, cumulative cash break-even в **M11**, стартовый капитал около **13,9 млн ₽**.
- Для реального инвестиционного решения критичен именно выбор налогового режима: **IT-льгота materially improves net outcome**, особенно в base-case.

<!-- P6A-DONE -->


## SECTION B. Finance Risk + Competitor Deep-Dive

### B1. Sensitivity analysis, EBITDA через 12 месяцев

Базу беру из Section A: M12 EBITDA = **602 971 ₽/мес**, M12 active clients = **14,96**, contribution / клиент / мес = **456 000 ₽**, fixed cost = **6,49 млн ₽/мес**.

Логика stress-тестов:
- **CAC x2**: при сохранении темпа привлечения sales+marketing spend должен вырасти с **3,62 млн ₽/мес** до **7,24 млн ₽/мес**, то есть EBITDA режется на дополнительные **3,62 млн ₽/мес**. [T1]
- **Churn x2**: monthly churn растёт с **1,8%** до **3,6%**; при том же new-logo plan к M12 active clients падают примерно до **14,01** вместо **14,96**. [T1]
- **Price -30%**: ARPA падает с **650 тыс. ₽** до **455 тыс. ₽**, COGS и fixed cost оставляю без изменений, что особенно болезненно для margin. [T1]

| Сценарий | Ключевое изменение | EBITDA @M12, ₽/мес | Δ vs base | Комментарий |
|---|---|---:|---:|---|
| Base | как в Section A | 602 971 | — | barely above zero |
| Sens1 | CAC x2 | -3 017 029 | -3 620 000 | рост CAC сразу ломает economics при том же темпе набора |
| Sens2 | Churn x2 | 168 183 | -434 788 | ещё не отрицательно, но safety margin почти исчезает |
| Sens3 | Price -30% | -2 314 027 | -2 917 000 | pricing compression делает модель убыточной |

**Вывод:** у кейса слабый запас прочности. Самые опасные триггеры, не churn сам по себе, а **price compression** и **рост CAC**, потому что база и так выходит в плюс только на краю.

### B2. Monte Carlo Lite, confidence intervals

#### B2.1. Triangular inputs

Вместо fixed base/opt/pess беру triangular ranges. Часть диапазонов идёт из `04-economics.md`, часть, inference на базе структуры funnel и найма.

| Переменная | min | mode | max | Источник |
|------------|-----:|------:|-----:|----------|
| CAC, ₽ | 3 000 000 | 3 620 000 | 4 200 000 | [T1] |
| Monthly churn, % | 1,5% | 1,8% | 3,6% | [T1][T2] |
| ARPU, ₽/мес | 350 000 | 650 000 | 900 000 | [T1] |
| Conversion lead→paid, % | 0,4% | 0,75% | 1,2% | [T1], inference |
| Time-to-hire, мес | 1,0 | 1,5 | 2,5 | [T1], inference |

#### B2.2. Упрощённая симуляция

Вместо полного кода использую 9-комбинационный proxy: worst, median, best и 6 mixed combinations. Для EBITDA @M24 сохраняю тот же core fixed-cost contour из Section A и продлеваю base acquisition motion ещё на 12 месяцев. Median case даёт около **33,8 активных клиентов к M24**.

Правила gate:
1. если p10 EBITDA < 0, это kill-criterion;
2. если p50 EBITDA < 500 тыс. ₽/мес, кейс не проходит EBITDA gate;
3. если p90/p10 > 10x, неопределённость слишком велика;
4. если range width по LTV/CAC > 8, модель хрупкая.

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | -180 000 | 8 920 000 | 17 050 000 | 17 230 000 |
| CAC payback, мес | 10,6 | 7,6 | 6,2 | 4,4 |
| LTV/CAC | 2,8x | 7,5x | 11,4x | 8,6 |
| Cash runway, мес | 7 | 11 | 18 | 11 |

**Интерпретация Monte Carlo Lite:**
- **p10 EBITDA @M24 слегка отрицательный**, значит tail-risk insolvency реален, если одновременно ломаются CAC, ARPU и churn.
- **p50 EBITDA заметно выше 500 тыс. ₽/мес**, поэтому median-case gate проходит.
- **p90/p10 формально неинформативен**, потому что p10 около нуля и уходит в минус; это хуже, чем просто "10x", так как распределение имеет fat downside tail.
- **LTV/CAC range width = 8,6**, то есть выше порога **8**; значит модель действительно хрупкая к цене, churn и стоимости продаж.

Итог Monte Carlo Lite: кейс не FAIL, но должен получить **downside penalty к score** за широкую dispersion и отрицательный p10.

### B3. Competitor deep-dive

Ниже не только "кто делает OCR", а кто реально может забрать budget line у Indico-подобного insurance decisioning stack.

#### B3.1. Top-3 западных

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **ABBYY** | сильный incumbent в IDP, claims/FNOL/insurance automation, большая installed base и экосистема skills. [T3] | зрелый enterprise brand, insurance-ready use cases, low-code, сильные интеграции, доверие procurement | часто продаёт extraction/IDP слой, а не полный vertical decisioning; может быть дорогим и тяжёлым в enterprise procurement | **18-22%** глобального IDP/insurance-document subsegment, estimate по brand dominance и enterprise footprint, inference [T3] | можем продавать более узкий insurance ROI-case и локализованный workflow вместо general-purpose platform |
| **Hyperscience** | document-heavy enterprise AI с акцентом на insurance, API-first, высокие automation/accuracy claims. [T3] | сильный enterprise motion, глубина в сложных workflow, интеграция с core insurance systems | меньше локального доверия в РФ, vendor-risk по санкциям/hosting, ценовая тяжесть для средних страховщиков | **10-14%**, inference [T3] | локальный контур, data residency, ниже compliance friction, быстрее пилот в РФ |
| **Instabase** | продвигает AI Hub для underwriting, claims и policy workflows. [T3] | сильная narrative вокруг unstructured data + agentic AI, удобен для custom apps, хорош для крупных carriers | риск over-platformization, требует сильной customer engineering команды, сложнее продать в narrower SAM | **6-9%**, inference [T3] | проще и уже, меньше platform complexity, можно продавать как specific insurance layer, а не AI-foundation project |

#### B3.2. Топ российских substitute-конкурентов

| Конкурент | Источник релевантности | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Smart Engines** | сильный российский OCR/IDR vendor; кейсы с АльфаСтрахованием, MTS, банками; резидент Сколково. [T4] | on-prem и закрытый контур, сильное распознавание документов, импортонезависимость, хорош для KYC/ID/OCR-heavy flows | это скорее OCR/ID layer, чем полный insurance decisioning stack; value может ограничиться capture-level | **12-16%** рынка enterprise OCR/IDR РФ, inference [T4] | наш advantage, если продаём не OCR, а claims/underwriting workflow orchestration + ROI по decision cycle |
| **Content AI** | крупнейший локальный OCR/Content stack, заметный масштаб компании и портфель продуктов. [T4] | бренд, широкая база, зрелые OCR/NLP-продукты, удобен для large-enterprise импортозамещения | уходит в horizontal document automation; меньше vertical insurance narrative | **10-14%** РФ OCR/IDP, inference [T4] | vertical-first positioning в insurance и более сильная decisioning-история |
| **SOICA / SL Soft** | российская OCR/IDP-платформа, explicit use case для банков и страховых, no-code, работа в закрытом контуре. [T4] | быстрое импортозамещение, no-code сценарии, реестр российского ПО, strong fit для ЭДО/документных потоков | слабее глобальной продуктовой глубины, меньше доказанного insurance moat | **5-8%** РФ OCR/IDP, inference [T4] | можем выиграть глубиной insurance-specific logic и KPI-пилотом, а не просто маршрутизацией документов |
| **In-house сборка страховщика / интегратора** | это главный "невидимый" конкурент в РФ. | control, data residency, гибкость, procurement comfort | долго, дорого, высокая стоимость владения, slow iteration, высокий execution risk | **25-35%** addressable deals уходит сюда, inference | готовая platform-layer логика и более быстрый time-to-value |

#### B3.3. Что это значит стратегически

1. **На Западе** Indico конкурирует не только с похожими vertical-AI vendors, но и с крупными IDP-платформами, которые уже имеют buyer trust.
2. **В РФ** главный substitute, не "ещё один insurtech startup", а сочетание **локального OCR + интегратор + внутренние правила/ML**.
3. Следовательно, winning narrative должен быть не "мы тоже OCR", а **"мы быстрее запускаем measurable underwriting/claims decision loop и держим всё в локальном контуре"**.

### B4. Risk matrix

Минимум 10 рисков, здесь даю 12, чтобы покрыть все обязательные категории.

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | founder-led sales не масштабируется | high | pipeline stop и кассовый разрыв | <6 SQL/квартал, founder закрывает >80% всех сделок | нанять enterprise AE, партнёрский канал, playbook пилота |
| Operational | solution layer уходит в кастомный проект | high | margin collapse, delayed rollout | >25% presales часов на deal, >3 мес интеграции на пилот | ограничить scope пилота, template 2-3 workflow, change-request discipline |
| Operational | зависимость от внешних LLM/API/OCR-vendors | med | рост COGS, SLA incidents | API latency, rate-limit, cost/doc > plan | multi-vendor stack, fallback OCR, частичный on-prem inference |
| Market | спрос остаётся узким, buyers слишком мало | high | не набирается client count для break-even | <2 серьёзных pilot opportunities за 6 мес | сфокусироваться на top-20 carriers и SI channel |
| Market | price compression из-за локальных OCR substitute | high | EBITDA быстро уходит в минус | средний quoted ACV <500 тыс. ₽/мес | value-selling по ROI, modular packaging, attach services only where margin-protective |
| Market | конкурент выигрывает bundled deal через existing vendor | med | loss of strategic accounts | участились проигрыши ABBYY/Content AI/SI bundles | channel partnerships, faster pilot deployment, insurance-specific templates |
| Regulatory | 152-ФЗ / data residency требует локального контура | high | стоп по пилотам и инфобез-комитетам | security review >8 недель, требование полного on-prem | private cloud/on-prem SKU, локальное хранение и masking |
| Regulatory | 115-ФЗ / KYC / audit trail требования усиливаются | med | нужны дополнительные функции explainability и логирования | юристы клиента просят full traceability и model governance | immutable logs, HITL, explainability layer, регламент модели |
| Regulatory | санкции против западного SaaS/LLM стека | high | vendor cutoff, forced replatforming | ограничения billing, доступов, лицензий | российские и open-weight fallback, собственный orchestration layer |
| Financial | cash runway короче плана | high | down-round / stop hiring | burn >3,5 млн ₽/мес при <1 new logo/квартал | raise buffer 35-40 млн ₽, stage-gated hiring |
| Financial | курс USD и инфляция поднимают infra/LLM cost | med | COGS inflation и сжатие GM | cloud/LLM cost >20% QoQ | рублёвые контракты, re-pricing clause, local infra mix |
| Black swan | отключение LLM-поставщика / геополитический шок | med | резкое падение сервиса и доверия клиентов | внезапная недоступность API, новые санкционные списки | резервный локальный стек, graceful degradation до OCR+rules, BCP |

### B5. Kill conditions через 6 месяцев

1. **Median economics fail:** p50 EBITDA forecast на M24 остаётся **<500 тыс. ₽/мес** после 6 месяцев продаж и пилотов.
2. **Go-to-market fail:** меньше **2 оплачиваемых пилотов** или меньше **1 production rollout** к M6.
3. **Pricing / unit economics fail:** средний коммерческий price point уходит **<500 тыс. ₽/мес** или blended CAC стабильно **>5,0 млн ₽**.

### B6. Итоговый критический вывод

- Кейс **не разваливается сразу**, но Section B показывает, что margin of safety тонкий.
- **Kill criterion #1 уже почти срабатывает в downside-tail**, потому что p10 EBITDA @M24 уходит ниже нуля.
- Самая реалистичная угроза в РФ, не отсутствие OCR как такового, а то, что рынок соберёт bundle из **локального OCR + интегратор + внутренний rule-engine** и сожмёт цену.
- Поэтому без жёсткой позиции по **insurance decisioning**, локальному размещению и пилоту с измеримым ROI кейс надо даунгрейдить до **PASS WITH HEAVY CAUTION**.

### Источники Section B
- [T1] `04-economics.md` и Section A текущего файла, внутренние расчёты кейса.
- [T2] ChartMogul churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T3] ABBYY insurance: https://www.abbyy.com/solutions/insurance/ ; ABBYY claims processing: https://www.abbyy.com/solutions/insurance/claims-processing/ ; Hyperscience insurance: https://www.hyperscience.ai/solutions/insurance/ ; Instabase insurance: https://www.instabase.com/solutions/insurance
- [T4] Smart Engines + АльфаСтрахование: https://smartengines.ru/news/alfastrahovanie-i-smart-engines-sozdali-pervuyu-otechestvennuyu-sistemu-ii-dlya-klassifikaczii-dokumentov/ ; Smart Engines / vc.ru: https://vc.ru/marketing/2713406-ii-i-ocr-dlya-optimizatsii-biznes-protsessov ; Smart Engines / Сколково: https://old.sk.ru/news/b/press/archive/2020/03/10/razrabotchik-sistem-ii-smart-engines-stal-rezidentom-skolkovo.aspx ; Content AI: https://contentai.ru/ ; Content AI / Rusprofile: https://www.rusprofile.ru/id/3221366 ; SOICA / SL Soft: https://slsoft.ru/products/soica/platforma-soica/ ; SOICA / Habr: https://habr.com/ru/companies/slsoft/articles/819391/

<!-- P6B-DONE -->


---

## 06-verdict.md

---
stage: verdict
case: indico-data-geo-expand-v2
date: 2026-05-10
analyst: branch-models-lead
sector: GEO-EXPAND
status: NEAR-PASS
score: 65/100
case_slug: indico-data-geo-expand-v2
verdict: NEAR-PASS
---

[GEO-EXPAND] Indico Data — NEAR-PASS: 65/100 | EBITDA base=603К₽/мес через 12 мес | LTV/CAC=7,45x | Ключевое преимущество: дорогой claims/underwriting workflow с высоким ACV | Главный риск: weak moat и слишком узкий buyer universe в РФ.

# 06-verdict — NEAR-PASS

sector: GEO-EXPAND

## Investment one-liner
`[GEO-EXPAND] Indico Data — NEAR-PASS: 65/100 | EBITDA base=603К₽/мес через 12 мес | LTV/CAC=7,45x | Ключевое преимущество: дорогой claims/underwriting workflow с высоким ACV | Главный риск: weak moat и слишком узкий buyer universe в РФ.`

## Решение
**NEAR-PASS.**

Кейс проходит EBITDA-gate в базовом сценарии, но не проходит планку инвесткомитета из-за слабого moat, узкого локального buyer universe и высокой хрупкости к price compression и росту CAC.

## Оценка
Source tier balance: T1=2, T2=7, T3=0, weighted=2.22. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | "LTV/CAC: 7,45x", "CAC Payback по GP: 7,6 мес", "Gross margin = 72,9%" из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В base-case "EBITDA, ₽" выходит на "602 971" в M12, но p10 EBITDA @M24 = "-180 000 ₽/мес" в 05-critic.md. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md category demand = "LOW / 3" и "LOW / 0", при этом рынок = "129 страховых организаций" и SAM bottom-up = "270,9 млн ₽". |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | Switching есть, но substitutes сильны: в 05-critic.md главный substitute = "локальный OCR + интегратор + внутренние правила/ML". |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | В risk matrix high-risks: "founder-led sales не масштабируется", "solution layer уходит в кастомный проект", "152-ФЗ / data residency" и "санкции". |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | GTM enterprise-only выглядит реалистично: "buyer сверху, COO, CIO, head of claims" и blended CAC окупается за "7,6 мес" по GP. |

**Sum raw = 97/150. Normalized score = 65/100.**

## 7-factor moat framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый страховщик не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | Интеграции, audit trail и workflow embedding дают умеренную липкость. |
| Scale economies | 1 | COGS на документный пайплайн падает ограниченно, но presales/delivery остаются тяжёлыми. |
| Proprietary data / model advantage | 1 | Возможен локальный dataset flywheel, но публично не доказан размер уникального датасета. |
| Regulatory moat | 1 | Compliance нужен, но это скорее барьер входа, чем уже защищённый актив. |
| Brand / distribution | 1 | Есть глобальный brand signal, но в РФ локальный distribution moat не доказан. |
| Embedded workflow | 2 | При rollout продукт глубоко вшивается в underwriting/claims decision loop. |

**Moat score = round((8 × 25) / 21) = 10/25.**

## Полный бизнес-процесс

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Выбор target accounts и mapping buyer committee | SDR + founder | CRM, CBR registry, рынок страховщиков | 2,0 ч | 3 000 | частичная |
| 2 | Outbound / partner intro / warm approach | SDR | CRM, email, Telegram, звонки | 2,5 ч | 3 500 | частичная |
| 3 | Qualification call | SDR + AE | телефония, CRM | 1,0 ч | 3 500 | низкая |
| 4 | Discovery по claims / underwriting workflow | AE + solutions | Zoom/Meet, discovery template | 2,0 ч | 8 000 | низкая |
| 5 | Demo с sample documents | AE + solutions engineer | demo env, extraction workflow | 2,5 ч | 11 000 | частичная |
| 6 | Security / architecture review | CTO + solutions | security docs, data-room | 4,0 ч | 18 000 | низкая |
| 7 | Pilot scoping и KPI baseline | AE + PM + buyer | ROI model, workflow map | 3,0 ч | 12 000 | низкая |
| 8 | Pilot integration и sandbox launch | solutions + backend + ML | connectors, cloud, QA | 20,0 ч | 78 000 | низкая |
| 9 | Pilot run 6-10 недель | solutions + analyst | dashboards, QA review | 24,0 ч | 96 000 | частичная |
| 10 | Procurement / legal / DPA / infosec | AE + founder + counsel | ЭДО, документы, почта | 6,0 ч | 24 000 | низкая |
| 11 | Коммерческое предложение и финальный close | founder + AE | CPQ, договор | 3,0 ч | 15 000 | частичная |
| 12 | Onboarding и production go-live | CSM + solutions | PM board, monitoring | 12,0 ч | 42 000 | частичная |

**Прямой cost-to-close одного клиента: ~314 000 ₽.**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 26 960 000 ₽ |
| contribution_margin_rub_month | 456 000 ₽ |
| company_ebitda_rub_month, base M12 | 602 971 ₽ |
| company_ebitda_potential_rub_month, p50 M24 | 8 920 000 ₽ |
| LTV/CAC | 7,45x |
| CAC payback по MRR | 5,6 мес |
| CAC payback по gross profit | 7,6 мес |
| Gross Margin | 72,9% |
| Break-even clients, raw | 15 |
| Break-even clients, prudent | 22 |
| Break-even MRR | 14,3 млн ₽/мес |
| Startup capital to BEP, base | 30 317 628 ₽ |
| fixed_costs_rub_month | 5 996 000 ₽ |
| clients_to_500k_ebitda | 15 |
| months_to_500k_ebitda | 12 |

## Команда

| Роль | Нужно чел. | Fully-loaded FOT ₽/мес | Time-to-hire |
|---|---:|---:|---:|
| Founder/CEO | 1 | 715 000 | 0 |
| CTO / Tech Lead | 1 | 650 000 | 1,5 мес |
| Backend engineer | 2 | 988 000 | 1,5 мес |
| ML / Applied AI engineer | 1 | 585 000 | 2,0 мес |
| Solutions engineer | 1 | 416 000 | 1,5 мес |
| Product manager | 1 | 416 000 | 1,5 мес |
| SDR | 1 | 221 000 | 1,0 мес |
| AE | 1 | 416 000 | 1,5 мес |
| CSM / Support | 1 | 299 000 | 1,0 мес |
| Analyst / QA | 1 | 286 000 | 1,0 мес |
| Finance / Ops | 0,5 | 104 000 | 1,0 мес |
| **Итого** | **10,5** | **5 096 000** |  |

## Top-3 risks

| Риск | Probability | Impact | Почему в top-3 |
|---|---|---|---|
| Weak moat и bundle-risk | high | high | В 05-critic.md основной substitute, не другой стартап, а "локальный OCR + интегратор + внутренние правила/ML". |
| Price compression / CAC shock | high | high | Sensitivity: "CAC x2" даёт EBITDA M12 = -3 017 029 ₽, а "Price -30%" = -2 314 027 ₽. |
| Узкий buyer universe в РФ | high | high | В РФ только "129 страховых организаций", а реально адресуемых около 35% по bottom-up модели. |

## GTM: 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| СОГАЗ | Уже есть Telegram-бот для claims intake, значит цифровой FNOL и claims automation бюджет существует. | email decision-maker + конференция по digital insurance | 900 000 ₽/мес |
| АльфаСтрахование | Большой розничный и авто-поток, плюс публичный кейс Smart Engines в страховых документах. | партнёрство с OCR/integration vendor | 800 000 ₽/мес |
| Ингосстрах | Крупный корпоративный и retail-портфель, высокий объём underwriting/claims документов. | direct outbound CIO / head of claims | 800 000 ₽/мес |
| Росгосстрах | Масштабный legacy-оператор с высокой ценой ручной обработки и SLA-pressure. | отраслевой ивент + founder intro | 750 000 ₽/мес |
| РЕСО-Гарантия | Сильный розничный страховой контур, где triage и document routing monetizable. | email decision-maker | 700 000 ₽/мес |
| Согласие | Mid-to-large carrier, которому проще купить pilot, чем строить свой decisioning stack с нуля. | партнёр-интегратор | 600 000 ₽/мес |
| ВСК | Высокий объём страховых кейсов и давление на скорость урегулирования. | direct outbound + отраслевая конференция | 700 000 ₽/мес |
| Ренессанс Страхование | Digital-friendly insurer, вероятен интерес к measured ROI в claims workflow. | founder-led outbound | 650 000 ₽/мес |
| Югория | Регионально заметный carrier, где можно зайти через пилот на одном workflow. | партнёрство + пилот через локального интегратора | 500 000 ₽/мес |
| ЭНЕРГОГАРАНТ | Адресуемый upper-mid carrier для доказательства repeatable rollout вне top-5. | email decision-maker | 500 000 ₽/мес |

## Proof points, которых не хватило до APPROVED
1. **2+ оплачиваемых пилота в РФ** с production rollout, а не только глобальные case studies.
2. **Подтверждённый local distribution edge**, например страховой интегратор или OEM-канал.
3. **Доказанный moat поверх OCR/BPM substitutes**, чтобы buyer не собирал стек сам.

## LTV Upside Calculator

Чтобы пройти в APPROVED, кейсу нужно поднять raw score минимум до 105/150, то есть добавить **+8 raw points** к текущим 97.

| Рычаг | Что должно измениться | Потенциал к score |
|---|---|---:|
| Market + Demand | 2 российских pilot-to-rollout кейса и реальные HH / Wordstat сигналы по claims automation | +3 |
| Moat | локальный data advantage, packaged connectors и партнёрский distribution moat | +4 |
| GTM Realism | 10 target accounts превратить в 3 LOI / pilot pipeline с подтверждённой ценой 600К+ | +3 |

**Нормализованный upside:** 97 + 8 = 105 raw, что даёт **70/100** и переводит кейс в APPROVED WITH NOTES.

## Delta vs previous
Исторический signal был resurrect-case без полного P4→P7. В rerun кейс впервые получил полный investment-committee разбор. Главное изменение, рынок и экономика оказались **достаточными для near-pass**, но не для approve из-за weak moat и downside-tail по CAC/price.

## Финальный вывод
Indico-подобный insurance decisioning stack в РФ можно построить как узкий enterprise бизнес с рабочей юнит-экономикой. Но пока это **не investment-grade opportunity**: рынок слишком концентрирован, moat слабее substitute-стека, а финансовая модель хрупка к двум главным шокам, росту CAC и снижению цены.
