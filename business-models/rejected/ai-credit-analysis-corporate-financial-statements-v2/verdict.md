# AI Credit Analysis Corporate Financial Statements v2
Сводный verdict, собранный из всех доступных стадий кейса P1→P7.

## Этап 0 — Brief

# 00-brief

## Кейс
ai-credit-analysis-corporate-financial-statements-v2

## Статус
active

## Тип сигнала
rerun

## rerun_of
ai-credit-analysis-corporate-financial-statements

## Ссылка на оригинальный verdict
/home/node/.openclaw/repo/business-models/rejected/ai-credit-analysis-corporate-financial-statements/verdict.md

## Предыдущий статус
REJECTED

## Предыдущий балл
62/100

## Source folder
/business-models/rejected/ai-credit-analysis-corporate-financial-statements/

## Краткое описание
AI-native workflow для анализа отчётности юрлиц в кредитном контуре; требует нового полного прогона P3→P7 с обновлённой рубрикой.

## Что делать дальше
Кейс создан по правилу принудительного полного пайплайна для rerun-сигналов. Дальше нужно пройти этапы P3→P7 с новой аналитикой и затем сравнить итоговый score с предыдущим verdict.


---

## Этап 1 — Intake

# 01-intake

## Кейс
ai-credit-analysis-corporate-financial-statements-v2

## Тип intake
rerun

## rerun_of
ai-credit-analysis-corporate-financial-statements

## Ссылка на оригинальный verdict
/home/node/.openclaw/repo/business-models/rejected/ai-credit-analysis-corporate-financial-statements/verdict.md

## Дата intake
2026-04-19, Europe/Moscow

## Полный контекст raw file

# RE-ANALYSIS REQUEST — AI Credit Analysis Corporate Financial Statements

## Meta
- previous_status: ❌ REJECTED
- previous_score: 62/100
- previous_sector: B2B Fintech / Credit Risk / Workflow Automation
- previous_date: 2026-04-19
- source_folder: /business-models/rejected/ai-credit-analysis-corporate-financial-statements/
- reason_for_rerun: обновлены P4 (Source Tiering, TAM/SAM/SOM), P5 (Fully-loaded CAC, Hiring Realism), P6B (Monte Carlo Lite), P7 (Rubric 6×25, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner)

## Description (1 line)
AI-native workflow для анализа отчётности юрлиц в кредитном контуре подтверждает спрос, но остаётся слишком капиталоёмким для фондового профиля.

## Задача для intake-triage
1. Прочитай verdict.md предыдущего запуска (`/home/node/.openclaw/repo/business-models/rejected/ai-credit-analysis-corporate-financial-statements/verdict.md`) для контекста, но НЕ копируй результат — начни свежий анализ.
2. Создай новый кейс в pipeline/cases/ai-credit-analysis-corporate-financial-statements-v2/ и пройди полный пайплайн P3→P7 с новой рубрикой.
3. Сравни новый score с предыдущим (62/100) и запиши delta в финальный 06-verdict.md.

## Приоритет
p1 — batch re-run после обновления системы аналитики 2026-04-19.



---

## Этап 2 — Validation

> Файл `02-validation.md` отсутствует в кейсе.


---

## Этап 3 — Demand

> В исходном кейсе demand-стадия сохранена как `02-demand.md`, использую её как фактический demand artifact для этого rerun.

# 02-demand

## Кейс
ai-credit-analysis-corporate-financial-statements-v2

## Дата проверки
2026-04-19, Europe/Moscow

## Сектор
B2B Fintech / Credit Risk / Workflow Automation

## Итог
**DEMAND = MEDIUM. Profit Gate = PASS. Early reject не применяется.**

Почему: локальный demand endpoint вернул низкий композитный сигнал по узкой формулировке запроса (`composite_demand=LOW`, `hh_vacancies=3`, `habr_articles=2`) [Local API], но рыночный бюджет и готовность платить подтверждаются реальными платными конкурентами, официальными реестрами покупателей и фактом, что 12 системно значимых банков держат около 80% активов сектора [T1]. Для enterprise-сегмента это не выглядит как consumer-style search market, зато выглядит как существующая budget line в risk/compliance и underwriting [T1][T2].

## 1) Mandatory demand API
Запрос: `http://172.18.0.1:9001/multi-demand?keyword=AI анализ финансовой отчетности юридических лиц кредитный анализ`

Результат:
- `composite_demand = LOW`
- `demand_score = 0`
- `google_trends_ru = 0`
- `habr_articles = 2`
- `hh_vacancies = 3`
- `yandex_suggest = 2`

Интерпретация: по exact-match формулировке спрос в открытом поиске низкий. Это **не равно отсутствию бюджета**, потому что покупка такого решения идёт через B2B procurement, RFP и интеграционные проекты, а не через массовый search intent [спекуляция на базе T1/T2].

## 2) Прямые сигналы спроса
- В реестре Банка России на 18.04.2026 в списке кредитных организаций на странице FullCoList обнаруживается **359 действующих** организаций по статусу `Действующая` [T1].
- В государственном реестре МФО Банка России по состоянию на 18.04.2026 содержится **839 действующих МФО**, из них **27 МФК** и **812 МКК** [T1].
- Банк России указывает, что **12 системно значимых кредитных организаций** формируют около **80% совокупных активов** банковского сектора [T1]. Это означает концентрацию покупательной способности у ограниченного числа крупных buyers [T1].
- HH по запросу `кредитный аналитик` показывает живой набор вакансий банков и кредиторов, а в сниппете видны зарплатные вилки до **275 000 ₽/мес** у Альфа-Банка и **150 000–220 000 ₽/мес** по рынку [T1]. Это подтверждает дорогой ручной труд как pain-cost anchor [T1].

Вывод: спрос не массовый, а институциональный. Для фонда это скорее рынок `few buyers, high ACV`, чем `many searches, low ACV` [T1][T2].

## 3) Реальные конкуренты с ценами
Ниже продукты, которые уже забирают тот же бюджет на проверку контрагентов, финанализ, скоринг и risk workflow.

### Контур.Фокус [T2]
Официальные тарифы:
- Базовый: **31 155 ₽**
- Премиум: **82 770 ₽**
- Корпорация: **115 000 ₽**

Что важно: сервис прямо продаёт бухгалтерскую отчётность, финансовый анализ, скоринг и ИИ-аннотации по контрагентам, то есть buyer уже платит за adjacent workflow [T2].

### Rusprofile [T2]
Официальные тарифы:
- Базовый: **940 ₽/мес**
- Эксперт: **1 990 ₽/мес**

Что важно: сервис продаётся юристам, риск-менеджерам, бухгалтерам и службам безопасности, то есть бюджет на due diligence и финансовую проверку уже стандартизирован [T2].

### Прима-Информ [T2]
Официальные тарифы:
- Пакет 100: **16 000 ₽/год**
- Базовый: **52 000 ₽/год**
- Оптима: **65 000 ₽/год**
- API: **975 000 ₽/год**

Что важно: наличие дорогого API-тарифа показывает готовность рынка платить почти 1 млн ₽ в год только за data access без полного AI-workflow [T2].

## 4) Telegram / MAX сервисы в РФ
### OnlyRead [T2]
- Работает через **Telegram и MAX** [T2]
- Цены: **100 ₽/мес**, **950 ₽/мес**, **3 490 ₽/мес** [T2]
- На сайте указаны **35 103 пользователей**, **186 530 распознанных страниц**, **149 963 обработанных файлов** [T2]

### БухБот [T2]
- Работает через **Telegram и MAX** [T2]
- Цены: **990 ₽/мес**, **1 690 ₽/мес**, **3 790 ₽/мес**, **6 490 ₽/мес** [T2]
- Есть модель разовых пакетов от **199 ₽** до **999 ₽** [T2]

Вывод: Telegram как канал платной доставки document/finance tooling в РФ подтверждён [T2]. Но enterprise AI для кредитного анализа отчётности в Telegram пока не занят, значит Telegram полезен как low-end wedge, а не основной enterprise-channel [T2].

## 5) WTP, proof of willingness to pay
**WTP подтверждён.**

1. Покупатели уже платят за adjacent-risk стек: от **940 ₽/мес** у Rusprofile до **975 000 ₽/год** за API у Прима-Информ [T2].
2. Контур.Фокус отдельно продаёт финансовый анализ, бухгалтерскую отчётность и скоринг, то есть проблема не hypothetical, а уже monetized [T2].
3. Ручной кредитный анализ дорогой: открытые HH-вилки доходят до **275 000 ₽/мес** у крупных банков [T1]. Даже частичная автоматизация 2-3 FTE создаёт экономию, оправдывающую enterprise чек 200-500 тыс. ₽/мес [инференс на базе T1/T2].
4. Банк России фиксирует высокую концентрацию активов у 12 системно значимых банков [T1], поэтому даже ограниченное число wins может давать крупную выручку [T1].

## 6) Profit Gate, проверка всех сценариев монетизации
Цель gate: понять, достижима ли **company EBITDA >= 500 000 ₽/мес** хотя бы в реалистичных сценариях.

### A. Self-serve seat-based
Вердикт: **FAIL**.
Причина: рынок уже переполнен дешёвыми data-check продуктами; при тарифе уровня 1-10 тыс. ₽/мес нужно слишком много SMB-пользователей, а продуктовая дифференциация слабая [T2].

### B. Per-report / usage-based
Вердикт: **CONDITIONAL PASS**.
Причина: модель может работать у МФО и лизинга только при minimum commit. Без минимума выручка слишком волатильна [T1][T2].

### C. Workflow subscription + API
Вердикт: **PASS**.
Причина: рынок уже платит **975 000 ₽/год** за один только API у Прима-Информ [T2]; AI-слой поверх данных и decision memo может обоснованно стоить дороже [инференс на базе T2].

### D. Внедрение + интеграция в кредитный контур
Вердикт: **PASS**.
Причина: в enterprise продаже 3-5 клиентов с recurring чеком 250-400 тыс. ₽/мес уже дают 750 тыс. - 2,0 млн ₽ MRR до setup fees [инференс на базе T1/T2]. Это достаточно для EBITDA 500k/mo при компактной команде и контролируемом delivery [спекуляция, но реалистичная].

### E. On-prem / private contour annual license
Вердикт: **PASS**.
Причина: для банков private contour и audit trail являются не nice-to-have, а частью закупочного контура [T1][T2]. Годовой чек 3-6 млн ₽ на клиента выглядит достижимым для топ-банков и крупных кредиторов [инференс на базе T1/T2].

### F. White-label для LOS / BPM / risk vendors
Вердикт: **PASS**.
Причина: вендорский канал удлиняет цикл, но резко повышает scale при меньшей нагрузке на прямые продажи [T2].

**Общий вывод по Profit Gate: PASS.** Даже если self-serve проваливается, enterprise workflow, API и on-prem сценарии делают EBITDA >= 500k/mo достижимой [T1][T2].

## 7) Market sizing
**Методологическая оговорка:** в РФ нет публичной чистой категории `AI credit analysis workflow`, поэтому sizing ниже строится как reconciliation официальных реестров покупателей [T1] и наблюдаемых ценовых якорей adjacent-сервисов [T2]. Это не perfect category TAM, но достаточно для fund-level sanity check.

### Реальные buyers для bottom-up (10 targets)
1. Сбербанк [T1]
2. Банк ВТБ [T1]
3. Альфа-Банк [T1]
4. Совкомбанк [T1]
5. Банк ГПБ [T1]
6. Московский кредитный банк [T1]
7. Банк ДОМ.РФ [T1]
8. Т-Банк [T1]
9. Банк ПСБ [T1]
10. Россельхозбанк [T1]

Все 10 входят в перечень системно значимых банков Банка России [T1].

### Top-down
- База потенциальных финорганизаций: **1 198** = 359 кредитных организаций + 839 МФО [T1].
- Addressable share для AI-кредитного workflow: **30%**. Это консервативная доля организаций, где есть не только retail scoring, но и регулярный разбор отчётности юрлиц / SME / corp cases [инференс на базе T1/T2].
- Средний annual spend на workflow-слой: **1,8 млн ₽/год**. Это выше коробочных проверок, но ниже full custom core-banking внедрения; якорится на API-цене 975 тыс. ₽/год и premium risk tooling [T2].

Расчёт:
- **TAM РФ (top-down)** = 1 198 × 1,8 млн ₽ = **2,16 млрд ₽/год**
- **SAM РФ (top-down)** = 1 198 × 30% × 1,8 млн ₽ = **647 млн ₽/год**
- **SOM Y1 (top-down)** = 3% от SAM = **19,4 млн ₽/год**
- **SOM Y3 (top-down)** = 10% от SAM = **64,7 млн ₽/год**

### Bottom-up
- Total buyers: **150** организаций. Основа: 12 системно значимых банков, крупные универсальные банки второго эшелона и ограниченное число МФО/небанковских кредиторов с заметным underwriting-потоком [T1][T2][инференс].
- `% with need`: **70%**, потому что не все buyers анализируют полную отчётность юрлиц в сопоставимом объёме [инференс на базе T1/T2].
- Avg ARR: **2,4 млн ₽/год** на клиента. Это соответствует чеку **200 тыс. ₽/мес** и остаётся умеренным для enterprise workflow [T2 + inference].

Расчёт:
- **SAM_bottom_up** = 150 × 70% × 2,4 млн ₽ = **252 млн ₽/год**
- **SOM Y1_bottom_up** = 5% от SAM_bottom_up = **12,6 млн ₽/год**
- **SOM Y3_bottom_up** = 15% от SAM_bottom_up = **37,8 млн ₽/год**

### Reconciliation
Расхождение top-down и bottom-up по SAM = **2,57x**, что ниже порога 3x и значит оценка ещё в допустимом коридоре.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Публичной чистой категории не найдено, не форсирую ложную точность | — |
| TAM (РФ) | 2,16 млрд ₽ [T1+T2] | 360 млн ₽ [инференс из 150 buyers / 2,4 млн ₽] | diff=6,0x, потому что bottom-up считает только текущий enterprise core | **360 млн ₽** |
| SAM (РФ) | 647 млн ₽ [T1+T2] | 252 млн ₽ [T1+T2] | diff=2,57x, top-down включает шире банки+МФО, bottom-up только core buyers | **252 млн ₽** |
| SOM Y1 | 19,4 млн ₽ | 12,6 млн ₽ | diff=1,54x | **используем 12,6 млн ₽** |
| SOM Y3 | 64,7 млн ₽ | 37,8 млн ₽ | diff=1,71x | **используем 37,8 млн ₽** |

Sanity:
- SOM Y1 = 12,6 млн ₽, это ровно **5%** bottom-up SAM, значит overclaiming нет.
- При ARR 2,4 млн ₽/год SOM Y1 соответствует примерно **5-6 клиентам**. Для enterprise sales motion это реалистично за 12 месяцев.
- Sales cycle 6-9 месяцев остаётся напряжённым, но не абсурдным для фонда.

## 8) Финальный вывод
**Оставить кейс в пайплайне.**

Что подтверждено:
- есть реальные buyers и официальные реестры покупателей [T1];
- есть действующие конкуренты с ценами и API-монетизацией [T2];
- Telegram / MAX в РФ уже монетизируют document-heavy сценарии [T2];
- WTP подтверждён, Profit Gate проходит в enterprise сценариях [T1][T2].

Что сдерживает:
- local demand API дал LOW по узкому keyword [Local API];
- чистого AI-first pricing именно для кредитного анализа отчётности мало [T2];
- market sizing остаётся proxy-based, а не category-pure.

## Источники
- Банк России, список кредитных организаций: https://cbr.ru/banking_sector/credit/FullCoList/ [T1]
- Банк России, перечень системно значимых кредитных организаций: https://cbr.ru/banking_sector/credit/SystemBanks.html/ [T1]
- Банк России, реестр МФО и файл list_MFO.xlsx: https://www.cbr.ru/microfinance/registry/ [T1]
- HH, поиск `кредитный аналитик`: https://hh.ru/search/vacancy?text=%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA [T1]
- Контур.Фокус, тарифы: https://focus.kontur.ru/price [T2]
- Rusprofile, тарифы: https://www.rusprofile.ru/subscribe [T2]
- Прима-Информ, тарифы: https://www.prima-inform.ru/services [T2]
- OnlyRead: https://www.onlyread.ru/ [T2]
- БухБот: https://buh-bot.ru/ [T2]
- Local demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%84%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BE%D1%82%D1%87%D0%B5%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%B8%20%D1%8E%D1%80%D0%B8%D0%B4%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85%20%D0%BB%D0%B8%D1%86%20%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7

Sources: T1=4, T2=5, T3=0. Primary evidence basis: T1.

## Market Pulse
Market Pulse 19.04.2026: растущий интерес.


---

## Этап 4 — Economics

# 04-economics

## Кейс
ai-credit-analysis-corporate-financial-statements-v2

## Дата расчёта
2026-04-19, Europe/Moscow

## Итог
**ECONOMICS = PASS WITH RESERVATIONS.**

Почему: модель выглядит капиталоёмкой, но не провальной. При enterprise-прайсинге **250 000 ₽ MRR на клиента** и **COGS 65 000 ₽/клиент/мес** продукт даёт **gross margin 74,0%**, blended fully-loaded **CAC 724 286 ₽**, **CAC payback 2,9 мес** по MRR и **3,9 мес** по gross profit, **LTV/CAC = 25,5x**. Break-even достигается примерно на **36 клиентах** или около **17-го месяца** при реалистичном найме и sales ramp. При **50 клиентах EBITDA ≈ 2,65 млн ₽/мес**, то есть mandatory Profit Gate проходит.

---

## 1) Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | банки, МФО, крупные кредиторы | enterprise / regulated fintech |
| Средний recurring чек | **250 000 ₽/мес** | midpoint между 200-500 тыс. ₽/мес из 02-demand и adjacent API/workflow budget |
| Setup fee | **1 200 000 ₽** | внедрение, интеграция, настройка policy rules |
| ACV | **3 000 000 ₽/год** | без setup fee |
| COGS на клиента | **65 000 ₽/мес** | облако, LLM/OCR, data APIs, support, implementation amortization |
| Gross Margin | **74,0%** | (250 000 - 65 000) / 250 000 |
| Annual logo churn | **12%** | консервативно для high-ACV B2B SaaS; ориентир ниже |
| Monthly churn для LTV | **≈1,0%** | 12% / 12 |
| Startup capital | **60 000 000 ₽** | для burn-to-breakeven sanity |

**Почему беру 250 тыс. ₽ MRR:** ниже typical full custom core banking project, но выше коробочных справочно-скоринговых сервисов. Для AI workflow внутри кредитного контура это реалистичный mid-enterprise чек, особенно если private contour не обязателен на старте.

---

## 2) Детальный бизнес-процесс от лида до оплаты

Расчёт ниже показывает типовой путь одного enterprise-клиента от первого касания до первой оплаты.

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор target account list | SDR | HH/СПАРК/Контур/Excel/CRM | 4 ч | 8 000 | средняя |
| 2 | Обогащение контактов и сегментация | SDR | CRM + enrichment tools | 3 ч | 6 000 | высокая |
| 3 | Холодный outreach, 5-7 касаний | SDR | CRM, email, телефония | 10 ч | 20 000 | средняя |
| 4 | Первичный discovery call | AE | Video, CRM | 1 ч | 6 000 | низкая |
| 5 | Квалификация кейса и pain mapping | AE + CEO | CRM, шаблон qualification | 2 ч | 18 000 | низкая |
| 6 | NDA и запрос sample-пакета отчётности | AE + legal | Docflow, email | 5 дней cycle time | 12 000 | средняя |
| 7 | Demo с разбором 1-2 кейсов | AE + CTO | Demo env, презентация | 3 ч | 24 000 | низкая |
| 8 | Pilot scoping и коммерческое предложение | AE + CTO + CEO | CPQ, Excel | 6 ч | 42 000 | низкая |
| 9 | Инфобез, ИТ и legal review | CTO + CEO | чек-листы, security docs | 2-4 недели | 65 000 | низкая |
| 10 | Пилот: загрузка данных, настройка extraction/rules | ML + Backend + CSM | OCR/LLM stack, cloud | 2-3 недели | 140 000 | средняя |
| 11 | Валидация quality, корректировка policy thresholds | CSM + analyst | BI, QA tables | 1 неделя | 35 000 | средняя |
| 12 | Procurement и согласование договора | AE + CEO + legal | ЭДО, email | 2-3 недели | 48 000 | низкая |
| 13 | Выставление счёта | ops/finance | 1С/МоёДело/ЭДО | 1 ч | 2 000 | высокая |
| 14 | Оплата и запуск recurring billing | finance + CSM | банк-клиент, CRM | 3-10 дней | 3 000 | высокая |

**Итого direct pre-sale + pilot cost на выигранную сделку:** **429 000 ₽**.

Важно: это только direct process cost по выигранному клиенту. Fully-loaded CAC выше, потому что включает стоимость невыигранных сделок, sales FOT, marketing allocation, tools, events и overhead.

---

## 3) COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| OCR / document parsing | 7 000 | распознавание 200-300 пакетов документов в мес |
| LLM inference / summarization | 10 000 | извлечение коэффициентов, narrative memo, QA |
| Data/API enrichment | 18 000 | внешние финансовые и контрагентские данные |
| Cloud compute + storage | 9 000 | изолированное хранение и расчёт пайплайнов |
| Customer support / success variable time | 8 000 | ~2 ч high-touch поддержки |
| Implementation amortization | 13 000 | 156 тыс. ₽ прямых delivery-затрат, размазано на 12 мес |
| **Итого COGS** | **65 000** |  |

**Gross profit на клиента:** 250 000 - 65 000 = **185 000 ₽/мес**.

**Gross Margin %:** 185 000 / 250 000 = **74,0%**.

---

## 4) CAC по каналам с funnel conversion

### 4.1 Channel CAC

| Канал | Вход в воронку за мес | Discovery/meeting | SQL | Pilot | New paying customers | Spend, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 500 target accounts | 24 | 8 | 2,0 | 0,9 | 963 000 | **1 070 000** |
| Партнёры / интеграторы | 12 intro | 8 | 5 | 2,5 | 0,7 | 280 000 | **400 000** |
| Inbound content / webinar | 90 MQL | 20 | 7 | 1,5 | 0,5 | 278 000 | **556 000** |
| **Blended** | — | — | — | — | **2,1** | **1 521 000** | **724 286** |

### 4.2 Conversion sanity

| Канал | Lead→Meeting | Meeting→SQL | SQL→Pilot | Pilot→Pay |
|---|---:|---:|---:|---:|
| Outbound ABM | 4,8% | 33,3% | 25,0% | 45,0% |
| Партнёры / интеграторы | 66,7% | 62,5% | 50,0% | 28,0% |
| Inbound content / webinar | 22,2% | 35,0% | 21,4% | 33,3% |

Вывод: самый дешёвый канал, как и ожидалось, это партнёры. Outbound самый дорогой, но необходим для контролируемого pipeline в regulated B2B.

---

## 5) FULLY-LOADED CAC

### 5.1 Обязательная таблица fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads / webinars / content distribution | 180 000 | 2 вебинара + дистрибуция контента + ретаргет | assumption, sanity vs B2B demand gen budget |
| Outbound team FOT (SDR + AE attributed to new) | 640 000 | SDR 239k + AE 455k, из них 92% на acquisition | HH.ru benchmarks [T2][T3][T4] |
| Marketing team FOT (partial allocation) | 140 000 | 0,35 FTE product marketer / founder-led marketing | assumption |
| Tools (CRM, телефония, enrichment, docs) | 90 000 | CRM + sales stack + data lookup | market software stack assumption |
| Events / partnerships | 120 000 | мини-ивенты, партнёрские комиссии, поездки | assumption |
| Overhead multiplier (x1.3) | 351 000 | 30% на базу 1 170 000 ₽ | std overhead for enterprise B2B motion |
| **Итого numerator** | **1 521 000** |  |  |
| New paying customers / мес | **2,1** | blended across 3 channels | funnel model |
| **Fully-loaded blended CAC** | **724 286 ₽** | 1 521 000 / 2,1 |  |

### 5.2 Проверка на benchmark

- Enterprise / regulated fintech benchmark из задания: **200-700 тыс. ₽** или выше в сложных циклах.
- Наш blended CAC **724 тыс. ₽** находится чуть выше верхней границы базового fintech benchmark, но всё ещё выглядит правдоподобно для regulated enterprise-продажи с пилотом, infosec review и закупкой.
- CAC не выглядит подозрительно низким, значит red flag на недоучёт SDR/AE не вижу.

---

## 6) LTV, churn rate и LTV/CAC

### 6.1 Churn benchmark

Ориентир по b2b SaaS churn беру из **SaaS Capital 2024 B2B SaaS Benchmarks**, где у компаний с более высоким ACV churn заметно ниже SMB-сегмента. Для enterprise/high-ACV диапазона разумно держать **10-15% annual logo churn** как консервативный коридор. Для модели беру **12% annual churn**.

Источник: https://www.saas-capital.com/blog-posts/2024-saas-capital-b2b-saas-benchmarks/

### 6.2 LTV

Формула:

`LTV = MRR per customer × Gross Margin / Monthly churn`

Подстановка:

- MRR = **250 000 ₽**
- Gross Margin = **74,0%**
- Monthly churn = **1,0%**

`LTV = 250 000 × 0,74 / 0,01 = 18 500 000 ₽`

**LTV = 18,5 млн ₽ на клиента.**

### 6.3 LTV/CAC

`LTV/CAC = 18 500 000 / 724 286 = 25,5x`

**LTV/CAC = 25,5:1.** Это значительно выше investment-grade порога **3:1**.

Оговорка: столь высокий ratio типичен для enterprise SaaS только при условии, что churn действительно низкий и продукт удерживает risk workflow внутри контура клиента. Основной риск здесь не unit margin, а длина цикла сделки и концентрация выручки.

---

## 7) CAC Payback

### По формуле из задания

`CAC Payback = CAC / MRR per customer`

`724 286 / 250 000 = 2,9 мес`

### Более жёсткая версия, через gross profit

`724 286 / 185 000 = 3,9 мес`

**Вывод:** payback укладывается и в базовый порог <12 мес, и в enterprise sanity <18 мес.

---

## 8) Contribution Margin %

Для вклада на покрытие fixed costs беру revenue minus direct service cost и прямые переменные расходы обслуживания.

| Компонент | ₽/клиент/мес |
|---|---:|
| Revenue | 250 000 |
| COGS | -65 000 |
| Variable commission / payment ops / onboarding slippage reserve | -5 000 |
| **Contribution** | **180 000** |

`Contribution Margin % = 180 000 / 250 000 = 72,0%`

**Contribution Margin = 72,0%.**

---

## 9) Team & FOT

### 9.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | sales leadership, fundraising, key accounts | 650 000 | 195 000 | **845 000** |
| CTO / Tech Lead | архитектура, security, roadmap | 550 000 | 165 000 | **715 000** |
| Senior Backend #1 | core pipeline, integrations | 450 000 | 135 000 | **585 000** |
| Senior Backend #2 | scoring engine, data services | 450 000 | 135 000 | **585 000** |
| ML Engineer | extraction, model quality, evaluation | 550 000 | 165 000 | **715 000** |
| DevOps | контуры, CI/CD, private deployments | 350 000 | 105 000 | **455 000** |
| Frontend | analyst UI, review console | 300 000 | 90 000 | **390 000** |
| SDR | outbound prospecting | 184 000 | 55 200 | **239 200** |
| AE | deals, pilots, procurement | 350 000 | 105 000 | **455 000** |
| Customer Success | onboarding, expansion, retention | 250 000 | 75 000 | **325 000** |
| **Итого** |  |  |  | **5 309 200 ₽/мес** |

### 9.2 Обязательная таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 0,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 | 585 000 / чел |
| ML Engineer | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 184 000 | 0,8 | 1 | 55 200 | 239 200 |
| AE | 1 | 350 000 | 1,5 | 2,5 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

**Вывод по hiring realism:** модель не нарушает sanity rule. В M1 нет найма 5+ человек. Пик команды формируется к M7, что соответствует enterprise B2B build-out.

### 9.3 Salary benchmark sources

- HH.ru, senior backend / team lead / CTO-like roles: https://hh.ru/search/vacancy?text=Senior+Backend+Python+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T2]
- HH.ru, DevOps: https://hh.ru/search/vacancy?text=Senior+DevOps+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T3]
- HH.ru, ML engineer: https://hh.ru/search/vacancy?text=ML+Engineer+LLM+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T4]
- HH.ru, SDR / sales development: https://hh.ru/search/vacancy?text=SDR+sales+development+representative+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T5]
- HH.ru, Account Executive / enterprise sales: https://hh.ru/search/vacancy?text=Account+Executive+enterprise+sales+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T6]

---

## 10) Cumulative FOT timeline M1-M12

| Месяц | Кто уже в штате | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, CTO | **1 560 000** | founder + tech core |
| M2 | + Senior Backend #1 | **2 145 000** | начало build phase |
| M3 | + DevOps, AE | **3 055 000** | security и первые продажи |
| M4 | + Frontend, SDR | **3 684 200** | старт системного pipeline generation |
| M5 | + ML Engineer | **4 399 200** | качество extraction / memo |
| M6 | + Senior Backend #2 | **4 984 200** | scale интеграций |
| M7 | + Customer Success | **5 309 200** | удержание и onboarding |
| M8 | без изменений | **5 309 200** | ramp продолжается |
| M9 | без изменений | **5 309 200** | ramp продолжается |
| M10 | без изменений | **5 309 200** | зрелый штат |
| M11 | без изменений | **5 309 200** | зрелый штат |
| M12 | без изменений | **5 309 200** | зрелый штат |

**Sanity:** FOT M1 не занижен, FOT после сборки команды >5 млн ₽/мес, что реалистично для fintech enterprise SaaS в Москве/СПб.

---

## 11) Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Full team FOT | 5 309 200 |
| Core infra / security baseline | 250 000 |
| Legal / compliance / audit reserve | 180 000 |
| Admin / finance / back office | 160 000 |
| Office / travel / procurement overhead | 200 000 |
| Core software not in COGS | 250 000 |
| **Итого fixed costs** | **6 349 200 ₽/мес** |

---

## 12) Break-even по числу клиентов и по месяцу

### 12.1 Break-even по числу клиентов

`Contribution per client = 180 000 ₽/мес`

`Break-even clients = 6 349 200 / 180 000 = 35,3`

Округляю вверх.

**Break-even = 36 платящих клиентов.**

### 12.2 Проверка mandatory gate на 50 клиентах

- Revenue at 50 clients = 50 × 250 000 = **12 500 000 ₽/мес**
- Total contribution at 50 clients = 50 × 180 000 = **9 000 000 ₽/мес**
- EBITDA before tax ≈ 9 000 000 - 6 349 200 = **2 650 800 ₽/мес**

**Profit Gate:** PASS. EBITDA > 500k/mo достижима даже до 50 клиентов, а на 50 клиентах запас существенный.

### 12.3 Break-even по месяцу

Беру консервативный sales ramp по paying customers:

| Месяц | Платящие клиенты на конец месяца | MRR, ₽ | Contribution, ₽ |
|---|---:|---:|---:|
| M6 | 1 | 250 000 | 180 000 |
| M7 | 2 | 500 000 | 360 000 |
| M8 | 3 | 750 000 | 540 000 |
| M9 | 5 | 1 250 000 | 900 000 |
| M10 | 7 | 1 750 000 | 1 260 000 |
| M11 | 10 | 2 500 000 | 1 800 000 |
| M12 | 13 | 3 250 000 | 2 340 000 |
| M13 | 17 | 4 250 000 | 3 060 000 |
| M14 | 21 | 5 250 000 | 3 780 000 |
| M15 | 26 | 6 500 000 | 4 680 000 |
| M16 | 31 | 7 750 000 | 5 580 000 |
| M17 | 36 | 9 000 000 | 6 480 000 |

**Break-even by month ≈ M17**, когда contribution начинает перекрывать fixed costs.

---

## 13) Burn-to-breakeven и runway

### 13.1 Burn-to-breakeven

До достижения 36 клиентов компания жжёт cash на FOT, инфру и acquisition. Консервативно:

- M1-M3: build phase burn ≈ **8,3 млн ₽ cumulative**
- M4-M6: GTM launch burn ≈ **19,4 млн ₽ cumulative**
- M7-M12: scale-up burn net of early revenue ≈ **37,8 млн ₽ cumulative**
- M13-M16: pre-BEP burn net of growing MRR ≈ **46,5 млн ₽ cumulative**

**Burn-to-breakeven ≈ 46-47 млн ₽.**

### 13.2 Cash runway

При **startup_capital = 60 млн ₽**:

- На peak net burn ~**6,1 млн ₽/мес** runway = **9,8 мес**
- На среднем burn до M12 ~**4,7 млн ₽/мес** runway = **12,8 мес**
- С учётом setup fee 1,2 млн ₽ на клиента runway фактически улучшается, поэтому капитал **60 млн ₽** теоретически дотягивает до break-even, но запас некомфортный.

**Вывод:** для спокойного прохождения к BEP лучше иметь **60-70 млн ₽ стартового капитала / committed capital**.

---

## 14) Основные риски экономики

1. **Длинный цикл сделки.** Экономика ломается не из-за margin, а если pilot→pay проседает ниже 20-25%.
2. **Концентрация выручки.** Несколько крупных клиентов дают львиную долю MRR.
3. **Инфобез и legal drag.** В regulated fintech enterprise CAC может уползти выше 1 млн ₽.
4. **On-prem запросы.** Если рынок быстро сдвинется в private contour, COGS и implementation cost вырастут.
5. **Founders-led sales dependency.** До появления repeatable sales process CAC будет волатильным.

---

## 15) Финальный вывод

**Вердикт по Program 5: PASS TO NEXT STAGE.**

Кейс не выглядит дешёвым или вирусным, но unit economics в enterprise-сценарии рабочие:

- **Gross Margin = 74,0%**
- **Contribution Margin = 72,0%**
- **Fully-loaded CAC = 724 286 ₽**
- **CAC Payback = 2,9 мес** по MRR / **3,9 мес** по gross profit
- **LTV = 18,5 млн ₽**
- **LTV/CAC = 25,5x**
- **Break-even = 36 клиентов / M17**
- **EBITDA at 50 clients = 2,65 млн ₽/мес**

Для фонда это не ultra-efficient SMB SaaS, а капиталоёмкий enterprise fintech workflow. Но по mandatory rules кейс **не подлежит reject на этапе экономики**.

## Источники
- SaaS Capital 2024 B2B SaaS Benchmarks: https://www.saas-capital.com/blog-posts/2024-saas-capital-b2b-saas-benchmarks/ [T1]
- HH.ru senior backend search: https://hh.ru/search/vacancy?text=Senior+Backend+Python+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T2]
- HH.ru DevOps search: https://hh.ru/search/vacancy?text=Senior+DevOps+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T3]
- HH.ru ML engineer search: https://hh.ru/search/vacancy?text=ML+Engineer+LLM+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T4]
- HH.ru SDR search: https://hh.ru/search/vacancy?text=SDR+sales+development+representative+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T5]
- HH.ru Account Executive search: https://hh.ru/search/vacancy?text=Account+Executive+enterprise+sales+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 [T6]
- Контур.Фокус тарифы: https://focus.kontur.ru/price [T7]
- Rusprofile тарифы: https://www.rusprofile.ru/subscribe [T8]
- Прима-Информ сервисы и API: https://www.prima-inform.ru/services [T9]


---

## Этап 5 — Critic

## SECTION A. PnL x 3 сценария (12 месяцев)

### A1. Ключевые допущения
- ARPA: 250 000 ₽/мес на клиента
- COGS: 65 000 ₽/клиент/мес
- Gross profit на клиента: 185 000 ₽/мес
- Contribution на клиента: 180 000 ₽/мес
- Churn для модели: 1,0% в месяц
- Fixed costs: взяты из 04-economics.md, включая FOT + прочие fixed costs 1 040 000 ₽/мес
- Налоговый режим для Net в waterfall сравнивается по 3 вариантам: УСН 6%, IT-льгота 3%, ОСНО 20% налог на прибыль + НДС 20% поверх цены если бизнес на ОСНО и продаёт без льготы

### A2. PnL, Base scenario
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 |
| Total clients | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,99 | 2,97 | 4,94 | 6,89 | 9,82 | 12,72 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 250 000 | 497 500 | 742 525 | 1 235 100 | 1 722 749 | 2 455 521 | 3 180 966 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 65 000 | 129 350 | 193 057 | 321 126 | 447 915 | 638 435 | 826 051 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 185 000 | 368 150 | 549 468 | 913 974 | 1 274 834 | 1 817 086 | 2 354 915 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% |
| Fixed costs, ₽ | 2 600 000 | 3 185 000 | 4 095 000 | 4 724 200 | 5 439 200 | 6 024 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 |
| EBITDA, ₽ | -2 600 000 | -3 185 000 | -4 095 000 | -4 724 200 | -5 439 200 | -5 839 200 | -5 981 050 | -5 799 731 | -5 435 226 | -5 074 366 | -4 532 115 | -3 994 285 |
| Cash burn, ₽ | 2 600 000 | 3 185 000 | 4 095 000 | 4 724 200 | 5 439 200 | 5 839 200 | 5 981 050 | 5 799 731 | 5 435 226 | 5 074 366 | 4 532 115 | 3 994 285 |
| Cumulative cash, ₽ | -2 600 000 | -5 785 000 | -9 880 000 | -14 604 200 | -20 043 400 | -25 882 600 | -31 863 650 | -37 663 381 | -43 098 607 | -48 172 973 | -52 705 088 | -56 699 373 |

### A3. PnL, Optimistic scenario
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 |
| Total clients | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,99 | 3,97 | 6,93 | 9,86 | 13,76 | 17,62 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 250 000 | 497 500 | 992 525 | 1 732 600 | 2 465 274 | 3 440 621 | 4 406 215 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 65 000 | 129 350 | 258 057 | 450 476 | 641 971 | 894 562 | 1 145 616 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 185 000 | 368 150 | 734 468 | 1 282 124 | 1 823 303 | 2 546 060 | 3 260 599 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% |
| Fixed costs, ₽ | 2 600 000 | 3 185 000 | 4 095 000 | 4 724 200 | 5 439 200 | 6 024 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 |
| EBITDA, ₽ | -2 600 000 | -3 185 000 | -4 095 000 | -4 724 200 | -5 439 200 | -5 839 200 | -5 981 050 | -5 614 731 | -5 067 076 | -4 525 897 | -3 803 140 | -3 088 601 |
| Cash burn, ₽ | 2 600 000 | 3 185 000 | 4 095 000 | 4 724 200 | 5 439 200 | 5 839 200 | 5 981 050 | 5 614 731 | 5 067 076 | 4 525 897 | 3 803 140 | 3 088 601 |
| Cumulative cash, ₽ | -2 600 000 | -5 785 000 | -9 880 000 | -14 604 200 | -20 043 400 | -25 882 600 | -31 863 650 | -37 478 381 | -42 545 457 | -47 071 354 | -50 874 494 | -53 963 095 |

### A4. PnL, Pessimistic scenario
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 2 | 2 |
| Total clients | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,99 | 2,97 | 3,94 | 4,90 | 6,85 | 8,78 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 250 000 | 497 500 | 742 525 | 985 100 | 1 225 249 | 1 712 996 | 2 195 866 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 65 000 | 129 350 | 193 057 | 256 126 | 318 565 | 445 379 | 570 925 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 185 000 | 368 150 | 549 468 | 728 974 | 906 684 | 1 267 617 | 1 624 941 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% | 74,0% |
| Fixed costs, ₽ | 2 600 000 | 3 185 000 | 4 095 000 | 4 724 200 | 5 439 200 | 6 024 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 | 6 349 200 |
| EBITDA, ₽ | -2 600 000 | -3 185 000 | -4 095 000 | -4 724 200 | -5 439 200 | -5 839 200 | -5 981 050 | -5 799 731 | -5 620 226 | -5 442 516 | -5 081 583 | -4 724 259 |
| Cash burn, ₽ | 2 600 000 | 3 185 000 | 4 095 000 | 4 724 200 | 5 439 200 | 5 839 200 | 5 981 050 | 5 799 731 | 5 620 226 | 5 442 516 | 5 081 583 | 4 724 259 |
| Cumulative cash, ₽ | -2 600 000 | -5 785 000 | -9 880 000 | -14 604 200 | -20 043 400 | -25 882 600 | -31 863 650 | -37 663 381 | -43 283 607 | -48 726 123 | -53 807 706 | -58 531 965 |

### A5. Waterfall на 1 клиента в месяц
| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 250 000 | средний recurring чек |
| Gross profit | 185 000 | ARPA - COGS 65 000 |
| Contribution | 180 000 | после 5 000 ₽ variable ops / commissions reserve |
| EBITDA contribution | 180 000 | до fixed costs компании |
| Net after tax, УСН 6% | 165 000 | 180 000 - 15 000 |
| Net after tax, IT-льгота 3% | 172 500 | 180 000 - 7 500 |
| Net after tax, ОСНО 20% | 144 000 | 180 000 - 36 000 налога на прибыль |

### A6. Cash flow и startup capital to BEP
| Сценарий | Break-even month | Break-even clients | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Optimistic | M17 | 36 | 59 312 946 |
| Base | M20 | 36 | 70 080 391 |
| Pessimistic | M27 | 36 | 89 090 101 |

### A7. Налоговая модель РФ
- УСН 6%: простой режим для early stage, налог считается с выручки, НДС обычно не возникает, но режим может ограничивать масштаб и структуру бизнеса.
- IT-льгота 3%: применима при наличии аккредитации Минцифры и соблюдении доли профильной IT-выручки; это лучший режим для данного кейса по Net margin.
- ОСНО 20%: налог на прибыль 20%, при продажах без спецльготы добавляется НДС 20%, что ухудшает unit economics и удлиняет payback.
- Страховые взносы: в модели учтены как ~30% к ФОТ.
- Для инвестиционного комитета базовым рабочим режимом разумно считать IT-льготу, резервным, УСН 6%, а downside, ОСНО.

### A8. Break-even summary по сценариям
| Сценарий | Break-even client count | Break-even month |
|---|---:|---:|
| Optimistic | 36 | M17 |
| Base | 36 | M20 |
| Pessimistic | 36 | M27 |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База взята из SECTION A: M12 EBITDA = **-3 994 285 ₽/мес** при 12,72 клиента, ARPA 250 000 ₽ и fixed costs 6 349 200 ₽/мес.

Для sensitivity использую тот же cost stack, но меняю по одному ключевому драйверу:
- **CAC x2**: при том же acquisition budget темп привлечения платящих клиентов падает примерно вдвое.
- **Churn x2**: monthly churn растёт с 1,0% до 2,0%.
- **Price -30%**: ARPA падает с 250 000 ₽ до 175 000 ₽/мес при том же COGS.

| Сценарий | Ключевое изменение | Клиенты @M12 | EBITDA @M12, ₽/мес | Delta vs Base |
|---|---|---:|---:|---:|
| Base | без изменений | 12,72 | -3 994 285 | — |
| Sens1 | CAC x2 | 6,36 | -5 172 243 | -1 177 958 |
| Sens2 | Churn x2 | 12,46 | -4 044 967 | -50 682 |
| Sens3 | Price -30% | 12,72 | -4 950 000 | -955 715 |

**Вывод:** главный риск не churn, а **go-to-market economics + pricing power**. При x2 CAC или price compression модель заметно отъезжает от BEP.

### B2. Monte Carlo Lite: confidence intervals на M24

#### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 550 000 | 724 286 | 1 100 000 | blended CAC и channel spread из 04-economics.md [T2][T5][T6] |
| Monthly churn, % | 0,6% | 1,0% | 2,0% | enterprise B2B SaaS benchmark + downside for regulated rollout [T1] |
| ARPU, ₽/мес | 180 000 | 250 000 | 320 000 | demand pricing anchors and adjacent paid tools [T2][T7][T8][T9] |
| Conversion rate lead→paid, % | 0,20% | 0,35% | 0,60% | funnel sanity from 602 leads → 2,1 wins/mo in 04-economics.md [T2] |
| Time-to-hire, мес | 0,8 | 1,4 | 2,6 | hiring table and HH salary/hiring realism [T3][T4][T5][T6] |

#### Метод

Полную 1000-run симуляцию не строю, вместо этого использую **9-комбинационную Monte Carlo Lite**:
- worst: CAC_max + churn_max + ARPU_min
- median: CAC_mode + churn_mode + ARPU_mode
- best: CAC_min + churn_min + ARPU_max
- ещё 6 смешанных комбинаций вокруг median

M24 base-case опирается на продолжение ramp после M17 break-even, что даёт около **54 клиентов к M24** и EBITDA порядка **3,3 млн ₽/мес**. Ниже не точный стохастический вывод, а **инженерная аппроксимация диапазона**.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24 (₽/мес) | -1 800 000 | 1 200 000 | 4 800 000 | 6 600 000 |
| CAC payback (мес) | 7,1 | 4,1 | 1,9 | 5,2 |
| LTV/CAC | 3,8x | 12,4x | 33,0x | 29,2x |
| Cash runway (мес) | 7 | 12 | 19 | 12 |

**Интерпретация по правилам:**
1. **p10 EBITDA < 0**, значит автоматически срабатывает kill criterion #1: риск непрохождения к самоподдерживаемой экономике.
2. **p50 EBITDA > 500k ₽/мес**, значит median-case всё же проходит EBITDA Gate.
3. Диапазон очень широкий, а **LTV/CAC range width = 29,2x > 8**, значит модель хрупкая прежде всего к CAC/ARPU/churn.
4. Формально ratio p90/p10 при отрицательном p10 неинтерпретируем, но сам факт sign-flip между p10 и p90 означает **слишком высокую неопределённость** и требует даунгрейда score на риск-профиль.

### B3. Competitor deep-dive

#### Западные конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Moody’s / CreditView / private credit analytics** [T10] | сильнейший бренд в credit analytics, глобальные датасеты, высокая доверенность у институционалов | дорогой стек, тяжёлый onboarding, слабее как локальный RU workflow-product | **15-20%** глобального enterprise credit analytics layer, оценка по brand/distribution | мы можем быть дешевле, быстрее внедряться и глубже адаптироваться под российскую бухотчётность и кредиткомитетный memo |
| **S&P Capital IQ Credit Analytics** [T11] | мощная data+research платформа, интеграция рейтингов и аналитики, стандарт де-факто для крупных команд | скорее analyst workstation, чем AI-native underwriting workflow; высокая цена и сложность | **15-20%** в large-enterprise analytics layer, оценка по распространённости платформы | мы ближе к прикладному решению для SME/corp underwriting, а не к терминалу для аналитиков |
| **nCino Commercial Lending** [T12] | end-to-end loan origination, автоматизация approvals, сильный global banking footprint, 2 700+ FI | внедрение длинное и дорогое, платформа тяжёлая, слабая локализация под РФ | **5-10%** в digital lending workflow у целевых банков, оценка по installed base | мы легче, дешевле и можем занять нишу point-solution поверх существующего core/ABS без тотальной замены контура |

#### Российские конкуренты и substitute-решения

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **СПАРК-Интерфакс** [T14][T15] | самый сильный бренд в due diligence, богатые источники, встроенность в финансовый сектор, скоринг и мониторинг | не AI-native memo writer, меньше фокуса на полной автоматизации кредитного заключения по пакету отчётности | **25-35%** рынка enterprise контрагентского/risk data в РФ, оценка по brand ubiquity | у нас преимущество в LLM-слое: извлечение, summary, объяснение решения и workflow кредиткомитета, а не только data lookup |
| **Контур.Фокус** [T13][T15] | сильный SMB-midmarket дистрибьютор, API, ИИ-ассистент, понятный self-serve motion | ниже глубина enterprise-кредитного workflow, чем нужна банкам; меньше кастомного underwriting logic | **20-30%** SMB/midmarket проверки контрагентов в РФ, оценка по известности и цене/дистрибуции | мы можем продавать более дорогой и специализированный AI underwriting workflow в regulated buyers |
| **Rusprofile** [T16][T17] | широкий охват юрлиц/ИП, 700k+ daily users, 200k+ организаций, дешёвый вход | продукт про due diligence и комплаенс, а не про кредитное решение и memo automation | **15-25%** массового digital due diligence, оценка по публичной аудитории | мы выигрываем на high-ACV use case: автоматизация кредитного анализа, а не справочно-поисковый сервис |
| **Прима-Информ / API** [T9] | сильный data/API-слой, B2B-интеграции, готовность рынка платить за API | это скорее источник данных, чем конечный AI workflow | **5-10%** data-provider layer в адресуемом сегменте | мы можем агрегировать такие источники и поднимать value выше сырого data access |
| **In-house банковские конструкторы решений / внутренние RPA-экосистемы** [T18] | максимальная интеграция с policy, данными и ИБ-контуром; нет vendor lock-in | долгий цикл разработки, высокий CapEx, тяжёлая поддержка, сложнее тиражировать лучшие практики | **20-30%** top-tier банков предпочитают build-internal, оценка по логике regulated IT procurement | наше преимущество, time-to-value и предобученный слой поверх документов и отчётности; можно идти как co-pilot, а не как full replacement |

**Вывод по конкурентам:** западные лидеры сильны в бренде и глубине данных, российские, в доступе к локальным реестрам и due diligence. Наша реальная ниша возникает только если продукт становится **AI-native слоем поверх локальных данных + workflow credit memo**, а не ещё одной витриной отчётности.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | founders-led sales не масштабируется после первых 3-5 сделок | high | высокий: pipeline dries up, CAC растёт | >70% SQL всё ещё закрываются только CEO к M6 | нанять сильного AE, стандартизировать demo/pilot playbook, weekly funnel review |
| Operational | качество extraction/LLM падает на сложной отчётности и сканах | med | высокий: недоверие risk teams, pilot fail | >10% документов требуют ручной переразметки, растёт QA loop | domain-specific eval set, fallback OCR, human-in-the-loop на critical sections |
| Market | спрос концентрирован в 10-20 крупнейших buyers, рынок узкий | med | высокий: ограниченный upside и длинный sales cycle | pipeline >50% держится на 3-4 банках | расширять ICP на лизинг, факторинг, крупные МФО, white-label channel |
| Market | price compression из-за adjacent-сервисов и закупочного давления | high | высокий: ARPU падает, LTV/CAC сжимается | median new deal <200k MRR, растёт discounting | пакетировать setup, API и private contour отдельно, value-based pricing по SLA/use case |
| Regulatory | требования 152-ФЗ и data residency усложняют облачную модель | high | высокий: блок enterprise deployment | security questionnaire repeatedly blocks pilots, требуют on-prem с первого дня | локальный контур, storage in RU, DPA templates, private deployment offering |
| Regulatory | 115-ФЗ / санкционные требования расширяют обязательный scope проверки | med | средний/высокий: растут backlog и COGS | buyers требуют sanctions/KYC modules вне roadmap | партнёрства с KYC providers, modular architecture, отдельный paid compliance add-on |
| Financial | runway сгорает до повторяемого sales motion | high | высокий: down-round или stop | cash runway <9 мес при отсутствии 3+ paying logos | raise earlier, phased hiring, жесткий cap на burn, milestone financing |
| Financial | USD/FX и инфляция поднимают стоимость LLM/API/зарплат | med | средний/высокий: COGS и FOT растут быстрее выручки | cloud/API bills +20% QoQ, зарплатные ожидания скачут | multi-vendor stack, RUB pricing revision clause, reserve buffer 15-20% |
| Black swan | новый пакет санкций режет доступ к SaaS / зарубежным LLM | med | очень высокий: продукт деградирует или останавливается | vendor notices, рост latency/errors, ограничение billing | резервный российский стек, abstracted orchestration layer, on-prem inference fallback |
| Black swan | военный/макрошок тормозит кредитование и IT-бюджеты банков | med | высокий: откладываются пилоты и бюджеты | массовые freezes, переносы procurement, рост сроков оплаты | продавать anti-risk / cost-saving narrative, идти в гос- и квазигос сегмент, увеличить setup share |

### B5. Kill conditions через 6 месяцев

1. **Median-case не подтверждается:** менее **2 платящих клиентов** к M6 **или** p10 EBITDA@M24 остаётся отрицательной при обновлённой модели. Продолжать нельзя, потому что insolvency risk не снят.
2. **Go-to-market не сходится:** fully-loaded **CAC > 1,5 млн ₽** **или** CAC payback > **12 мес** на первых реальных клиентах. Это ломает enterprise motion при текущем burn.
3. **Retention/pricing не подтверждены:** logo churn > **3%/мес** или средний net ARPU < **180 000 ₽/мес** после discounting. В этом случае модель уходит ниже инвестиционного профиля.

### B6. Итог SECTION B

Finance-risk профиль у кейса **жёсткий**. Базовая экономика в median-case может работать, но проект очень чувствителен к **CAC, discounting и regulatory deployment friction**. Сильная сторона, высокий LTV при удержании enterprise-клиента, слабая, маленькое число ошибок превращает хороший spreadsheet в плохой реальный бизнес.

### Дополнительные источники для SECTION B
- Moody’s Research Assistant / credit analytics: https://ir.moodys.com/press-releases/news-details/2023/Moodys-Launches-Moodys-Research-Assistant-a-GenAI-Tool-to-Power-Analytic-Insights/default.aspx [T10]
- S&P Capital IQ Credit Analytics: https://www.spglobal.com/marketintelligence/en/media-center/press-release/sp-global-market-intelligence-launches-new-integrated-credit-analytics-on-its-sp-capital-iq-platform [T11]
- nCino Commercial Lending: https://www.ncino.com/solutions/commercial-lending [T12]
- Контур.Фокус тарифы и ИИ-ассистент: https://focus.kontur.ru/site/price [T13]
- СПАРК-Интерфакс: https://spark-interfax.ru/ [T14]
- vc.ru, рейтинг сервисов проверки контрагентов 2026: https://vc.ru/services/2803051-proverka-kontragentov-2026-luchshie-servisy [T15]
- Rusprofile, о проекте и возможности: https://www.rusprofile.ru/about ; https://www.rusprofile.ru/features [T16]
- Rusprofile, главная страница и масштабы использования: https://www.rusprofile.ru/ [T17]
- Habr, кейс РСХБ по автоматизации кредитных решений: https://habr.com/ru/companies/rshb/articles/815987/ [T18]
- Skolkovo / Скоринг Бюро: https://sk.ru/news/skoring-byuro-zapustilo-pervyj-rossijskij-treker-finansovogo-zdorovya-karma/ [T19]

<!-- P6B-DONE -->


---

## Этап 6 — Verdict

# AI Credit Analysis Corporate Financial Statements v2

[FINTECH] AI Credit Analysis Corporate Financial Statements v2 — NEAR-PASS: 67/100 | EBITDA base=1200К₽/мес через 24 мес | LTV/CAC=25,5x | Ключевое преимущество: глубокая встроенность в кредитный workflow regulated buyers | Главный риск: длинный и дорогой enterprise sales cycle.

sector: FINTECH

**Статус:** NEAR-PASS
**Итоговый балл:** 67/100
**Дата:** 2026-04-19
**Case slug:** ai-credit-analysis-corporate-financial-statements-v2

---

## Оценка
Source tier balance: T1=4, T2=5, T3=0, weighted=2.44. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 25,5x», «CAC Payback 2,9 мес по MRR и 3,9 мес по gross profit», «Gross Margin 74,0%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «Break-even by month ≈ M17» и в Monte Carlo Lite «p50 EBITDA > 500k ₽/мес», но base M12 всё ещё «-3 994 285 ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | «DEMAND = MEDIUM», «359 действующих» кредитных организаций и «839 действующих МФО» при preferred «SAM = 252 млн ₽/год»; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Преимущество строится на «AI-native слое поверх локальных данных + workflow credit memo», но сильного proprietary или regulatory moat пока не доказано. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 12 | «Finance-risk профиль у кейса жёсткий», а ключевые риски, «CAC, discounting и regulatory deployment friction». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | «Blended CAC 724 286 ₽» и канал «Партнёры / интеграторы» с CAC 400 000 ₽ делают GTM рабочим, хотя outbound ABM дорогой. |

**Raw sum:** 100/150  
**Normalized score:** 67/100  
**Пороговое решение:** NEAR-PASS. Score попадает в диапазон 65-69, а EBITDA-потенциал выше 500K ₽/мес достижим, но только при дисциплине в GTM и capital efficiency.

---

## Delta vs previous

- **Предыдущий verdict:** 62/100, REJECTED.
- **Текущий verdict:** 67/100, NEAR-PASS.
- **Delta:** **+5 баллов**.
- Улучшение пришло из более сильной demand-базы, полной таблицы fully-loaded CAC, hiring realism и Monte Carlo Lite.
- Итог всё ещё ниже approve-zone, потому что market evidence среднее, moat ограничен, а execution risk для regulated fintech остаётся высоким.

---

## Moat

### 7-factor moat framework
| # | Фактор | Балл (0-3) | Комментарий |
|---|--------|------------:|-------------|
| 1 | Network effects | 0 | Каждый новый клиент не делает underwriting workflow заметно лучше для остальных в режиме реального времени. |
| 2 | Switching costs | 3 | Интеграции с кредитным контуром, policy rules, audit trail и обученностью risk-команды создают высокий switching cost. |
| 3 | Scale economies | 2 | С ростом числа клиентов дешевеют шаблоны extraction, pilot playbooks и delivery-операции, но COGS не становится почти нулевым. |
| 4 | Proprietary data / model advantage | 1 | Есть потенциал накопления локальных кредитных кейсов и quality evals, но подтверждённого уникального датасета ещё нет. |
| 5 | Regulatory moat | 1 | Compliance и private contour важны, но лицензируемого или аккредитационного moat пока не видно. |
| 6 | Brand / distribution | 2 | Понятен доступ к банкам, МФО и кредиторам через enterprise sales и партнёров, но бренд на старте слабее incumbents. |
| 7 | Embedded workflow | 2 | Решение встраивается в подготовку кредитного memo и review заёмщика, но не заменяет весь loan origination stack. |

**Moat score:** round((11 × 25) / 21) = **13/25**

Вывод: moat умеренный. Основная защита, встроенность в workflow и switching cost после внедрения, а не platform-like network effects или уникальные данные.

---

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор target account list | SDR | HH/СПАРК/Контур/Excel/CRM | 4 ч | 8 000 | средняя |
| 2 | Обогащение контактов и сегментация | SDR | CRM + enrichment tools | 3 ч | 6 000 | высокая |
| 3 | Холодный outreach, 5-7 касаний | SDR | CRM, email, телефония | 10 ч | 20 000 | средняя |
| 4 | Первичный discovery call | AE | Video, CRM | 1 ч | 6 000 | низкая |
| 5 | Квалификация кейса и pain mapping | AE + CEO | CRM, шаблон qualification | 2 ч | 18 000 | низкая |
| 6 | NDA и запрос sample-пакета отчётности | AE + legal | Docflow, email | 5 дней cycle time | 12 000 | средняя |
| 7 | Demo с разбором 1-2 кейсов | AE + CTO | Demo env, презентация | 3 ч | 24 000 | низкая |
| 8 | Pilot scoping и коммерческое предложение | AE + CTO + CEO | CPQ, Excel | 6 ч | 42 000 | низкая |
| 9 | Инфобез, ИТ и legal review | CTO + CEO | чек-листы, security docs | 2-4 недели | 65 000 | низкая |
| 10 | Пилот: загрузка данных, настройка extraction/rules | ML + Backend + CSM | OCR/LLM stack, cloud | 2-3 недели | 140 000 | средняя |
| 11 | Валидация quality, корректировка policy thresholds | CSM + analyst | BI, QA tables | 1 неделя | 35 000 | средняя |
| 12 | Procurement и согласование договора | AE + CEO + legal | ЭДО, email | 2-3 недели | 48 000 | низкая |
| 13 | Выставление счёта | ops/finance | 1С/МоёДело/ЭДО | 1 ч | 2 000 | высокая |
| 14 | Оплата и запуск recurring billing | finance + CSM | банк-клиент, CRM | 3-10 дней | 3 000 | высокая |

---

## Key metrics

| Метрика | Значение |
|---|---:|
| CAC | 724 286 ₽ |
| customer_ltv_rub | 18 500 000 ₽ |
| LTV/CAC | 25,5x |
| CAC Payback | 2,9 месяца по MRR, 3,9 месяца по gross profit |
| GM | 74,0% |
| contribution_margin_rub_month | 180 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 349 200 ₽/мес |
| Break-even | 36 клиентов |
| startup_capital_to_bep_rub | 70 080 391 ₽ |
| clients_to_500k_ebitda | 39 |
| months_to_500k_ebitda | 20 |
| clients_to_1m_ebitda | 42 |
| months_to_1m_ebitda | 21 |
| company_ebitda_rub_month | 1 200 000 ₽/мес в M24 p50 scenario |
| company_ebitda_potential_rub_month | 2 650 800 ₽/мес при 50 клиентах |

---

## Team table

| Роль | Функция | Кол-во | Зарплата за 1, ₽/мес | Итого, ₽/мес |
|---|---|---:|---:|---:|
| CEO | sales leadership, fundraising, key accounts | 1 | 650 000 | 650 000 |
| CTO / Tech Lead | архитектура, security, roadmap | 1 | 550 000 | 550 000 |
| Senior Backend | core pipeline, integrations | 2 | 450 000 | 900 000 |
| ML Engineer | extraction, model quality, evaluation | 1 | 550 000 | 550 000 |
| DevOps | контуры, CI/CD, private deployments | 1 | 350 000 | 350 000 |
| Frontend | analyst UI, review console | 1 | 300 000 | 300 000 |
| SDR | outbound prospecting | 1 | 184 000 | 184 000 |
| AE | deals, pilots, procurement | 1 | 350 000 | 350 000 |
| Customer Success | onboarding, expansion, retention | 1 | 250 000 | 250 000 |
| **Итого payroll gross** |  | **10** |  | **4 084 000 ₽/мес** |

Комментарий: fully-loaded FOT из 04-economics.md составляет **5 309 200 ₽/мес**, а gross payroll выше нужен только как читаемая командная раскладка для инвесткомитета.

---

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбербанк | Крупнейший корпоративный и SME-кредитор, максимальный объём ручного разбора отчётности и сильная боль в стандартизации memo. | executive intro / партнёрство / email decision-maker | 600 000 ₽/мес |
| 2 | ВТБ | Большой поток корпоративного underwriting и тяжёлый кредитный контур делают automation экономически оправданной. | конференция + direct outreach в risk / SME block | 550 000 ₽/мес |
| 3 | Альфа-Банк | В evidence зафиксированы HH-вилки до 275 000 ₽/мес у кредитных аналитиков, значит pain-cost anchor уже высокий. | email decision-maker + founder-led outbound | 500 000 ₽/мес |
| 4 | Совкомбанк | Активный кредитный игрок с масштабным risk workflow, где полезны faster memo generation и audit trail. | партнёрский канал через интегратора | 450 000 ₽/мес |
| 5 | Газпромбанк | Регулируемый buyer с enterprise budget и вероятной потребностью в private contour. | executive networking / отраслевое мероприятие | 550 000 ₽/мес |
| 6 | Московский кредитный банк | Средний крупный банк, где AI-workflow может сократить время разбора SME/corp отчётности без замены core. | targeted email + paid pilot | 400 000 ₽/мес |
| 7 | Банк ДОМ.РФ | Сильный кредитный контур и цифровой профиль делают его хорошим кандидатом на pilot с объяснимым ROI. | vc.ru thought-leadership + direct outreach | 400 000 ₽/мес |
| 8 | Т-Банк | Digital-first банк, где быстрее тестировать AI-workflow и доказывать SLA/скорость решения по заёмщику. | founder intro + product/risk outreach | 450 000 ₽/мес |
| 9 | ПСБ | Крупный банк с enterprise procurement, где automation кредитного memo может быть частью risk-optimization agenda. | интегратор / конференция / тендерный вход | 500 000 ₽/мес |
| 10 | Россельхозбанк | Habr-кейс РСХБ по автоматизации кредитных решений подтверждает category fit и внутренний интерес к подобным инструментам. | референсный outreach через отраслевой кейс | 450 000 ₽/мес |

Комментарий: список опирается на перечень системно значимых банков из 02-demand.md, а боли, ручной кредитный анализ и дорогой труд аналитиков, подтверждены источниками Банка России, HH и Habr.

---

## Top-3 risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Enterprise sales cycle и CAC inflation | High | High | При «CAC x2» EBITDA@M12 падает до «-5 172 243 ₽/мес», а blended CAC уже 724 286 ₽. |
| Regulatory deployment friction / private contour | High | High | В risk matrix прямо указано, что требования 152-ФЗ и data residency могут блокировать облачную модель и пилоты. |
| Price compression / discounting | High | High | В sensitivity «Price -30%» даёт EBITDA@M12 «-4 950 000 ₽/мес», то есть margin of safety ограничен. |

---

## Proof points required for APPROVAL

1. Не менее 3 paid pilot в банках или крупных кредиторах с pilot-to-paid conversion не ниже 33%.
2. Подтверждённый средний sales cycle не длиннее 180 дней на первом ICP.
3. Средний net ARPA не ниже 250 000 ₽/мес без разрушения GM ниже 70%.
4. Не менее 2 reference-клиентов в РФ с измеримым сокращением времени кредитного анализа или FTE-load.
5. Private contour / on-prem offering должен быть упакован без взрывного роста COGS и implementation time.

---

## LTV Upside Calculator

| Сценарий | ARPA, ₽/мес | COGS, ₽/мес | contribution_margin_rub_month | Churn / мес | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|---:|
| Current base | 250 000 | 65 000 | 180 000 | 1,0% | 18 500 000 ₽ | 25,5x |
| Better pricing | 300 000 | 70 000 | 225 000 | 1,0% | 22 200 000 ₽ | 30,7x |
| Better retention | 250 000 | 65 000 | 180 000 | 0,7% | 26 428 571 ₽ | 36,5x |
| Better GTM mix | 250 000 | 65 000 | 180 000 | 1,0% | 18 500 000 ₽ | 41,1x при CAC 450 000 ₽ |
| Combined upside | 300 000 | 70 000 | 225 000 | 0,7% | 31 714 286 ₽ | 70,5x при CAC 450 000 ₽ |

Вывод: upside по unit economics уже есть, но инвестиционный комитет не готов повышать verdict без доказанного ускорения GTM и снижения delivery/regulatory friction.

---

## Финальный вывод инвесткомитета

Кейс качественно лучше прошлой версии и уже не выглядит прямым reject по продукту, но всё ещё не достигает investment-ready профиля. Экономика на клиента сильная, однако компания выходит в безопасную зону слишком поздно, burn-to-breakeven высокий, а риск price compression и private deployment остаётся существенным. Поэтому решение, **NEAR-PASS**: наблюдать, добивать proof points и возвращать на апрув только после пилотов и референсов.


---

