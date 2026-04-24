---
stage: economics
case: ai-nalogovyi-copilot-dlya-msb
date: 2026-04-25
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
AI-налоговый copilot для МСБ, который проверяет УПД, счета-фактуры, книги покупок и продаж, готовит черновики пояснений в ФНС и снижает ручную нагрузку бухгалтера.

## Executive summary

**Итог P5: REJECTED для фонда.**

Что получилось в base case:
- **MRR на клиента:** 35 000 ₽/мес
- **COGS:** 8 200 ₽/клиент/мес
- **Gross Margin:** 76,6%
- **Fully-loaded blended CAC:** 252 590 ₽
- **LTV:** 893 333 ₽
- **LTV/CAC:** 3,54x
- **CAC Payback:** 7,2 мес
- **Contribution Margin:** 69,4%

Почему всё равно reject:
1. **Profit gate не пройден.** Даже при **50 клиентах EBITDA = -3,25 млн ₽/мес**.
2. **Break-even слишком далеко:** около **184 клиентов**.
3. **Burn-to-breakeven слишком тяжёлый:** около **73,6 млн ₽**.
4. Метрики на одного клиента выглядят рабочими, но **fixed cost база для regulated tax workflow слишком тяжёлая** относительно чека 25–60 тыс. ₽.

## 1. Модель и ключевые допущения

### ICP
- бухгалтерские аутсорсеры с 50–300 клиентами;
- МСБ с НДС-контуром и заметным объёмом первички;
- налоговые консультанты и аутсорс-команды, отвечающие на требования ФНС.

### Монетизация, base case
- Подписка: **35 000 ₽/клиент/мес**
- Onboarding fee: **30 000 ₽** за первичную настройку и шаблоны
- Average deal cycle: **1,5–2,5 месяца**
- Считаю recurring unit economics отдельно, onboarding не включаю в MRR.

### Почему беру 35 000 ₽ MRR
Это середина диапазона из intake, но ниже enterprise-tax консалтинга. Для МСБ и бухгалтерских аутсорсеров чек выше 50–60 тыс. ₽/мес без сильной интеграции в 1С/ЭДО и доказанного compliance moat выглядит слишком оптимистично.

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листа бухгалтерских фирм и МСБ | SDR | HH, Rusprofile, 2ГИС, CRM | 35 мин | 700 | Низкий |
| 2 | Первый outreach, e-mail/звонок/Telegram | SDR | amoCRM, телефония, почта | 20 мин | 400 | Средний |
| 3 | Qualification call | SDR + AE | Meet, скрипт, CRM | 30 мин | 1 300 | Средний |
| 4 | Discovery по текущему налоговому процессу | AE | Meet, questionnaire, Miro | 45 мин | 1 700 | Низкий |
| 5 | Запрос примеров УПД/требований/пояснений | AE + клиент | ЭДО, secure upload, CRM | 25 мин | 900 | Средний |
| 6 | Demo на тестовых документах | AE + founder | Demo stand, 1С mock, экранный показ | 60 мин | 3 000 | Низкий |
| 7 | Пилотный расчёт ROI и scope | AE + founder | калькулятор ROI, шаблон КП | 40 мин | 2 000 | Низкий |
| 8 | Security / legal / DPA / 152-ФЗ check | Founder + подрядчик | NDA, договор, checklist | 50 мин | 2 500 | Низкий |
| 9 | Пилотная настройка коннекторов и шаблонов | CTO + backend | API, 1С коннектор, OCR пайплайн | 4 ч | 10 500 | Средний |
| 10 | Обучение бухгалтера клиента | CSM | Zoom, база знаний, шаблоны | 1 ч | 1 300 | Средний |
| 11 | Пилот 2–4 недели и weekly review | CSM + AE | CRM, support desk, аналитика | 3 ч | 5 200 | Средний |
| 12 | Коммерческое предложение и согласование | AE + founder | CRM, pricing sheet, ЭДО | 1 ч | 2 400 | Низкий |
| 13 | Выставление счёта и акт/УПД | Finance ops | 1С, банк, Диадок/СБИС | 20 мин | 350 | Высокий |
| 14 | Оплата и production onboarding | CSM + backend | банк, ЭДО, runbook | 1,5 ч | 2 600 | Средний |

### Вывод по процессу
Продажа не self-serve. Даже для чека 35 тыс. ₽ остаётся много ручных касаний: discovery, пилот, настройка шаблонов, legal/compliance, обучение. Поэтому CAC для продукта выше, чем у обычного SMB SaaS.

## 3. COGS breakdown per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM inference и reruns | 1 400 | проверка документов, черновики пояснений, повторные прогоны |
| OCR / document parsing | 1 600 | распознавание первички и структурирование полей |
| Облако, storage, резервирование | 900 | RU-hosting, хранение файлов, логи |
| Поддержка L1 | 1 200 | ответы по ошибкам, форматам, онбординг-вопросам |
| CSM allocation | 1 500 | доля customer success на активного клиента |
| Compliance / secure operations | 600 | доступы, аудит, политика хранения |
| Onboarding amortization | 700 | размазано на 12 мес |
| Платежи / ЭДО / сервисные комиссии | 300 | банк, Диадок/СБИС, мелкие сервисы |
| **Итого COGS** | **8 200** |  |

### Валовая маржа
- MRR на клиента: **35 000 ₽**
- COGS: **8 200 ₽**
- Gross Profit: **26 800 ₽**
- **Gross Margin = 76,6%**

## 4. CAC by acquisition channel with funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Партнёры 1С / бухфирмы | 40 | 18 | 10 | 6 | 2,0 | 5,0% |
| Outbound по бухгалтерам и CFO | 180 | 24 | 12 | 5 | 1,5 | 0,83% |
| Performance / ретаргетинг | 120 | 18 | 7 | 3 | 0,8 | 0,67% |
| Контент / вебинары / комьюнити | 60 | 12 | 6 | 2 | 0,7 | 1,17% |
| **Итого blended** | **400** | **72** | **35** | **16** | **5,0** | **1,25%** |

### Fully-loaded CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

#### Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | category search + ретаргетинг на бухгалтеров и CFO | модель для mid-market B2B |
| Outbound team FOT (SDR/AE attributed to new) | 552 500 | SDR 170k + AE 255k base + 85k variable, плюс 30% взносы, 85% времени на new business | HH.ru benchmark + модель |
| Marketing team FOT (partial allocation) | 94 000 | частичная аллокация founder/content и performance-support на acquisition | модель |
| Tools (CRM, LinkedIn/Apollo аналоги, телефония, email) | 55 000 | amoCRM + коллтрекинг + enrich + рассылки | рыночное допущение |
| Events/partnerships | 90 000 | вебинары, партнёрские эфиры, мини-ивенты с бухфирмами | модель |
| Overhead multiplier (x1.3) | 291 450 | 30% на management/admin/ops поверх 971 500 ₽ | методика Program 5 для mid-market B2B |
| **Итого fully-loaded acquisition spend** | **1 262 950** |  |  |

### CAC multiplier по сегменту
Кейс относится к **mid-market B2B / regulated-adjacent**. Для проверки использую multiplier **x1.3 к blended raw spend**, потому что продукт продаётся не как self-serve, а через несколько касаний, пилот и ручной onboarding.

### CAC по каналам

| Канал | Direct spend + allocated team/tools, ₽/мес | New paying / мес | Raw CAC, ₽ | Multiplier | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|
| Партнёры 1С / бухфирмы | 310 000 | 2,0 | 155 000 | x1.3 | 201 500 |
| Outbound | 470 000 | 1,5 | 313 333 | x1.5 | 470 000 |
| Performance / ретаргетинг | 260 000 | 0,8 | 325 000 | x1.3 | 422 500 |
| Контент / вебинары | 222 950 | 0,7 | 318 500 | x1.3 | 414 050 |
| **Blended** | **1 262 950** | **5,0** | **252 590** | n/a | **252 590** |

### Sanity checks against RU benchmarks
- Enterprise SaaS B2B в РФ: **300–900k ₽/клиент**
- Mid-market SaaS: **60–250k ₽/клиент**
- Fintech B2B: **200–700k ₽/клиент**

**Вывод:** blended CAC **252,6k ₽** находится на верхней границе mid-market и в нижней части fintech B2B benchmark. Это не дешёвое привлечение, но и не явный red flag.

## 5. LTV with churn rate

### Churn benchmark
Для B2B SaaS с ARPA порядка **$250–500** ChartMogul в исследовании **Benchmarks 2024** показывает месячный logo churn около **3%** как реалистичный ориентир для этого ценового сегмента. Для base case беру **monthly churn = 3,0%**. Это консервативнее, чем у лучшего enterprise SaaS, и ближе к early-stage mid-market B2B.

### Расчёт
- MRR на клиента: **35 000 ₽**
- Gross Margin: **76,6%**
- Monthly churn: **3,0%**

`LTV = MRR × Gross Margin / Monthly churn`

`LTV = 35 000 × 76,6% / 3,0% = 893 333 ₽`

### Вывод
- **LTV = 893 333 ₽**
- Для SMB/self-serve это хороший LTV, но для фонда важнее то, что абсолютный вклад на клиента слишком мал относительно required team.

## 6. LTV/CAC ratio

- LTV: **893 333 ₽**
- Fully-loaded CAC: **252 590 ₽**

`LTV/CAC = 893 333 / 252 590 = 3,54x`

### Интерпретация
- Формально метрика **выше порога 3:1** и выглядит investment-grade на уровне одного клиента.
- Но фондовый фильтр режет кейс дальше, потому что **вклад с клиента слишком мал, чтобы окупить fixed cost базу в разумный срок**.

## 7. CAC Payback in months

`CAC Payback = CAC / MRR per customer`

`252 590 / 35 000 = 7,2 мес`

### Sanity check
Порог из методики: payback должен быть **<12 мес** для базового B2B. Здесь показатель проходит.

## 8. Contribution Margin %

Для contribution margin вычитаю COGS и переменные продажи/обслуживание.

- Revenue per client / мес: **35 000 ₽**
- COGS: **8 200 ₽**
- Variable commission + variable success support: **2 500 ₽**

`Contribution profit = 35 000 - 8 200 - 2 500 = 24 300 ₽`

`Contribution Margin = 24 300 / 35 000 = 69,4%`

### Вывод
**Contribution Margin = 69,4%**. Для SaaS это хорошо. Проблема не в марже как таковой, а в слишком малом абсолютном contribution на одного клиента.

## 9. Team & FOT

### Full team table

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder | продажи, партнёрства, продукт, ключевые переговоры | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, безопасность, интеграции с 1С/ЭДО | 550 000 | 165 000 | 715 000 |
| Senior Backend | ingestion, API, workflow engine | 380 000 | 114 000 | 494 000 |
| ML Engineer | extraction, classification, prompt/rag quality | 500 000 | 150 000 | 650 000 |
| Frontend / Product engineer | UI бухгалтера, dashboard, QA fixes | 280 000 | 84 000 | 364 000 |
| SDR | outbound и qualification | 170 000 | 51 000 | 221 000 |
| AE | demo, пилоты, negotiation | 340 000 | 102 000 | 442 000 |
| Customer Success | onboarding, обучение, продление | 220 000 | 66 000 | 286 000 |
| **Итого core team** |  |  |  | **4 017 000** |

### Hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 380 000 | 1,5 | 1,5 | 114 000 | 494 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 0 в core team, outsourced | 0 | 0 | 0 | 0 | 0 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 170 000 + бонус | 1 | 1 | 51 000 | 221 000 |
| AE | 1 | 340 000 + комиссия | 1,5 | 2,5 | 102 000 | 442 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### Benchmark notes
- Senior SWE / Backend: **350–550k ₽**
- Team Lead / CTO-lite: **450–700k ₽**
- ML Eng: **400–700k ₽**
- Frontend: **250–400k ₽**
- SDR: **100–180k ₽ + bonus**
- AE: **300–500k ₽ + commission**
- Источник для sanity: вакансии и вилки HH.ru по Москве/СПб, проверка на 2026-04-25.

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT_monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder-only старт |
| M2 | CEO + Backend | 1 339 000 | backend ещё в ramp |
| M3 | + CTO | 2 054 000 | CTO найден к концу 2,5 мес, ramp старт |
| M4 | + ML Engineer | 2 704 000 | ML ещё не на full productivity |
| M5 | + Frontend | 3 068 000 | product shell готовится к пилотам |
| M6 | + SDR | 3 289 000 | первые системные outbound-циклы |
| M7 | + AE | 3 731 000 | AE ещё в ramp, quota не полная |
| M8 | + Customer Success | 4 017 000 | можно удерживать 10–15 активных клиентов |
| M9 | core team full | 4 017 000 | стабильный режим |
| M10 | core team full | 4 017 000 | стабильный режим |
| M11 | core team full | 4 017 000 | стабильный режим |
| M12 | core team full | 4 017 000 | стабильный режим |

### Комментарий по hiring realism
- В M1 нет массового найма, что соответствует time-to-hire.
- FOT M1-M3 уже быстро растёт выше 2 млн ₽, что типично для regulated B2B продукта.
- Для чека 35 тыс. ₽ такая команда оказывается **слишком дорогой**.

## 10. Fixed costs breakdown

| Компонент fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Core team FOT | 4 017 000 | см. таблицу выше |
| Outsourced DevOps / SRE | 180 000 | вместо штатного DevOps на ранней фазе |
| RU cloud baseline / monitoring / backups | 110 000 | общая база, не на клиента |
| Юрлицо, бухгалтерия, ЭДО, банк | 55 000 | постоянные admin расходы |
| Legal / 152-ФЗ / документы / policy upkeep | 45 000 | внешняя поддержка |
| Office / coworking / travel | 35 000 | минимальный гибридный режим |
| **Итого fixed costs / мес** | **4 442 000** |  |

Для break-even использую более консервативную цифру **4 467 000 ₽/мес**, добавляя резерв 25 000 ₽ на непредвиденные ops-расходы.

## 11. Break-even by client count and by month

### Break-even by client count
- Contribution per client: **24 300 ₽/мес**
- Fixed costs: **4 467 000 ₽/мес**

`Break-even clients = 4 467 000 / 24 300 = 183,8`

То есть нужен парк около **184 клиентов**.

### Stress test at 50 clients
`EBITDA at 50 clients = 50 × 24 300 - 4 467 000 = -3 252 000 ₽/мес`

**Profit gate FAIL:** даже при 50 клиентах EBITDA не просто ниже 500k ₽, а глубоко отрицательная.

### Break-even by month
Base ramp по активным клиентам:
- M3: 1
- M4: 2
- M5: 4
- M6: 6
- M7: 9
- M8: 12
- M9: 16
- M10: 20
- M11: 25
- M12: 30

При таком темпе в течение первых 12 месяцев break-even **не достигается**. Даже если после M12 удаётся добавлять по **8 клиентов в месяц**, операционный break-even получается только около **M32**.

## 12. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Кумулятивный burn по модели до M12 составляет около **39,5 млн ₽**. С продолжением роста после M12 до точки операционного break-even общая потребность в капитале достигает примерно **73,6 млн ₽**.

### Cash runway
Если взять `startup_capital = 30 млн ₽`, то при среднем burn первых 12 месяцев около **3,29 млн ₽/мес** cash runway составляет примерно:

`30 000 000 / 3 290 000 = 9,1 мес`

Но на пике burn M8-M12 компания тратит **3,7–4,2 млн ₽/мес**, поэтому практически runway ближе к **7–8 месяцам** без дополнительного раунда.

### Sanity checks
- `startup_capital_to_bep` существенно выше **10 млн ₽**, что подтверждает enterprise-like тяжесть модели.
- При этом для продукта с чеком **35 тыс. ₽/мес** это уже плохой знак: доход на одного клиента не тянет команду.

## 13. Итоговый вывод

### Что хорошо
- На уровне одного клиента экономика **не сломана**: LTV/CAC > 3x, payback < 12 мес.
- Есть реальная regulatory pain и канал через бухгалтерские фирмы / 1С.
- Gross margin и contribution margin выглядят нормально.

### Что ломает инвестиционный кейс
1. **Слишком маленький ARPU** для required delivery/team complexity.
2. **Слишком далёкий break-even**: около 184 клиентов.
3. **50 клиентов недостаточно** даже для приближения к EBITDA 500k ₽/мес.
4. Нужен большой burn до точки безубыточности, что плохо сочетается с ранним фондовым кейсом.

## Verdict
**REJECTED.**

Основание: кейс проходит клиентский unit economics, но **не проходит fund-level profit gate**. Для возврата в pipeline нужен либо чек заметно выше, либо встроенный канал distribution через крупные бухгалтерские сети, либо более лёгкая productized delivery-модель.

## Sources
- [T1] `01-intake.md`
- [T2] `01-evidence.md`
- [T3] ChartMogul, *SaaS Growth Report / Benchmarks 2024* — ориентир по monthly churn для ARPA $250–500: https://chartmogul.com/saas-metrics/benchmarks/
- [T4] HH.ru, вакансии и salary ranges по Москве/СПб, проверка 2026-04-25: https://hh.ru/
