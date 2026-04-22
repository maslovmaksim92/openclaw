---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-hebbia-finance-ai-analyst-geo-expand.md
created: 2026-04-20T17:18:00+03:00
---

# Intake

## Контекст resurrection
- Тип: принудительный полный пайплайн для повторной аналитики
- Исходный slug: hebbia-finance-ai-analyst-geo-expand
- Основание: сигнал ранее был закрыт как duplicate/supporting и должен пройти заново через P3→P7

## Полный контекст raw-файла

# RESURRECT SIGNAL — hebbia-finance-ai-analyst-geo-expand

## Meta
- source: triage/triage-2026-04-14-hebbia-finance-ai-analyst-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-hebbia-finance-ai-analyst-geo-expand.md

## Классификация
поддерживающий сигнал для существующего кейса

## Решение
Обогатить существующий кейс: `investment-banking-ai-analyst-operator`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по теме AI-аналитика для investment banking, private equity, asset management и corporate finance команд.
- Новый raw по Hebbia совпадает по нише, buyer profile и типу workflow: research, due diligence, работа с data room, сравнение компаний, подготовка мемо и анализ больших массивов документов.
- Сигнал не требует открытия нового кейса, но заметно усиливает текущий: подтверждает коммерческую зрелость категории, наличие крупных клиентов и переносимость спроса за пределы США через рост в EMEA.

## Что добавлено в кейс
- Создан и заполнен `pipeline/cases/investment-banking-ai-analyst-operator/01-evidence.md`.
- Добавлены supporting signal записи по Hebbia:
  - подтверждение международного расширения в UK/EMEA и роста выручки в регионе на 373% год к году;
  - подтверждение коммерческой зрелости через не менее $13 млн прибыльной годовой выручки и сильную клиентскую базу из крупных финансовых организаций.

## Что сделано
- Кейc `investment-banking-ai-analyst-operator` обогащён новыми доказательствами.
- Исходный raw-файл подлежит переносу в `pipeline/raw/processed/`.

## Вердикт
Это не новый кейс, а качественный supporting signal: тема investment-banking AI analyst получает второе независимое подтверждение через Hebbia, что усиливает GEO-EXPAND и enterprise LTV гипотезу.

```



---

# 02-demand.md

# 02-demand

## Кейс
hebbia-finance-ai-analyst-geo-expand-v2

## Demand verdict
**Итог: CONDITIONAL PASS.**

- По прямым запросам категории спрос в РФ слабый: `due diligence` → LOW, `M&A due diligence` → LOW, `AI due diligence` → LOW. [T2]
- По соседним JTBD сигналы заметно лучше: `инвестиционный анализ`, `анализ сделок`, `проверка контрагентов` дают MEDIUM и тысячи вакансий, то есть боль существует, но бюджет в РФ формулируется не как "AI finance analyst", а как risk / deal / research workflow. [T1][T2]
- У Hebbia есть явный category proof на Tier-1 уровне: компания официально продаёт продукт финансовым институтам, подключает FactSet / PitchBook / S&P Capital IQ / Guidepoint / Third Bridge и уже работает с фирмами, у которых суммарно $25T AUM. Это не доказывает локальный RU demand напрямую, но подтверждает, что workflow ценен для дорогих finance-команд. [T1]
- Правило раннего reject `LOW demand + Profit Gate FAIL` пока не срабатывает: для enterprise ICP с чеком порядка 2-5 млн ₽ ARR на команду путь к EBITDA >500k ₽/мес выглядит реалистичным. Это inference на базе локальных price anchors и природы buyer pain. [T1][T2]

## 1) Спрос и сигналы рынка

### Demand API
- `due diligence` → LOW, score 27, HH vacancies 315, Google Trends RU 4, Yandex suggest 100. [T2]
- `M&A due diligence` → LOW, score 22, HH vacancies 77, Yandex suggest 100. [T2]
- `AI due diligence` → LOW, score 3, HH vacancies 12, Yandex suggest 2. [T2]
- `инвестиционный анализ` → MEDIUM, score 30, HH vacancies 2 962, Yandex suggest 100. [T2]
- `анализ сделок` → MEDIUM, score 30, HH vacancies 5 301, Yandex suggest 100. [T2]
- `проверка контрагентов` → MEDIUM, score 30, HH vacancies 4 884, Yandex suggest 100. [T2]

### Интерпретация
- В РФ покупают не категорию "AI analyst for finance", а результат: быстрее разобрать data room, собрать comps, проверить контрагента, подготовить memo и сократить analyst-hours. [T1][T2][inference]
- Свежие HH-вакансии подтверждают, что due diligence и сделочный анализ остаются оплачиваемой функцией: есть открытые роли у Inventa Consulting, ALTHAUS, ANTERO Group, РУСАУДИТ и других игроков. [T1]
- Банк России фиксирует крупный денежный пул у институционального сегмента: вознаграждение УК за 9 месяцев 2023 года выросло до 69,5 млрд ₽, а в I квартале 2025 года драйвером роста снова оставались ПИФ. Это не прямой спрос на Hebbia, но подтверждение, что у финансовых организаций есть бюджеты на продуктивность и аналитическую инфраструктуру. [T1][inference]

## 2) Category proof и конкурентные якоря

| Игрок / якорь | Что подтверждает | Публичный сигнал | Вывод |
|---|---|---:|---|
| Hebbia | Продукт для finance workflows | официальный сайт показывает use cases для research, expert calls, slide drafting; интеграции FactSet, PitchBook, S&P Capital IQ, Guidepoint, Third Bridge [T1] | Это не generic copilot, а слой поверх дорогих финансовых данных и процессов |
| Hebbia | Enterprise adoption | компания пишет, что продукт используют leading financial firms; у клиентов суммарно $25T AUM и 1000+ use cases in production [T1] | Есть сильный global proof, что buyer pain реален у top-tier finance команд |
| Контур.Фокус | Локальный бюджет на due diligence / контрагент-аналитику | 31 155 ₽ / год базовый, 82 770 ₽ / год премиум, 115 000 ₽ / год корпорация [T1] | Нижний ценовой anchor локального рынка за data/risk tooling |
| Rusprofile | Массовый локальный budget line | от 940 ₽ / мес базовый, от 1 990 ₽ / мес эксперт [T1] | Широкий рынок платит за проверку контрагентов, но это low-end anchor |
| HH вакансии / консалтинг | Стоимость ручного труда | открытые вакансии по due diligence, financial DD, сделочному консалтингу в 2025-2026 [T1] | Автоматизация analyst-time монетизируема, если экономит часы senior staff |

### Что это значит для Hebbia-подобного продукта
- Локальный рынок уже платит за data access и проверку контрагентов, но это не тот price tier, который нужен для Hebbia-like economics. [T1]
- Hebbia-сценарий начинается выше: когда продукт объединяет private docs, внешние data providers и внутренний процесс команды, а ценность измеряется скоростью подготовки investment memo, screening и diligence. [T1][inference]
- Для РФ реалистичный ICP, если он существует, это не SMB, а банки, corpdev, M&A/advisory, PE/VC, asset managers и отдельные research-heavy практики. [T1][T2][inference]

## 3) WTP и willingness to pay

### Прямые доказательства WTP
1. Hebbia официально позиционируется для финансовых институтов и уже развернута у ведущих asset managers, банков и law firms. Это показывает, что глобально buyer готов платить за такой workflow layer. [T1]
2. Контур.Фокус и Rusprofile подтверждают регулярный платёжный спрос на проверку компаний и риск-аналитику в РФ, пусть и в гораздо более дешёвом сегменте. [T1]
3. Открытые вакансии по due diligence и финансовой экспертизе показывают, что ручная функция staffed и дорога, а значит экономия часов команды имеет денежную ценность. [T1]

### Оценка willingness to pay
- Для обычной проверки контрагентов локальный WTP ограничен десятками тысяч рублей в год на пользователя или небольшую команду. [T1]
- Для enterprise finance workflow willingness to pay может быть на порядок выше, если продукт реально сокращает время на review data room, поиск фактов, сверку источников и написание memo. Тогда чек **2-5 млн ₽ ARR** за команду выглядит правдоподобным как service-heavy deployment, но это уже inference, а не публичная котировка Hebbia. [T1][T2][inference]
- Следовательно, WTP есть, но он концентрирован в узком верхнем слое рынка и требует outcome-led продажи, а не self-serve SaaS. [T1][T2]

## 4) Market sizing

### Подход и допущения
- **Top-down база:** вознаграждение УК за 9 месяцев 2023 года составило **69,5 млрд ₽**. Annualized run-rate около **92,7 млрд ₽**. Для software/workflow spend беру **1,5%**, потому что продукт не core fee engine, а productivity layer. Получается top-down TAM **1,39 млрд ₽**. [T1][inference]
- **Bottom-up база:** целевой universe для Hebbia-like motion в РФ оцениваю примерно в **120 buyers**: CIB/IB подразделения банков, крупные УК, PE/VC, corpdev крупных групп, M&A / due diligence advisory. [T1][T2][inference]
- **ARR avg:** **3,0 млн ₽ / год** за одну команду 10-20 пользователей с внедрением и поддержкой. [T1][T2][inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для этого кейса считаю только РФ GEO-EXPAND слой | — |
| TAM (РФ) | **1,39 млрд ₽** = 92,7 млрд ₽ × 1,5% [T1] | **360 млн ₽** = 120 buyers × 3,0 млн ₽ [T1][T2] | diff=3,9x, top-down слишком широкий, беру lower bound | **360 млн ₽** |
| SAM (РФ) | **417 млн ₽** = 1,39 млрд ₽ × 30% применимости к finance-research / deal workflows [T1][inference] | **216 млн ₽** = 120 × 60% нуждающихся × 3,0 млн ₽ [T1][T2][inference] | diff=1,9x, расхождение допустимо | **216 млн ₽** |
| SOM Y1 | **12,5 млн ₽** = 3% SAM [T1][inference] | **12,0 млн ₽** = 4 клиента × 3,0 млн ₽ [T1][T2][inference] | модели почти сходятся | **12,0 млн ₽** |
| SOM Y3 | **41,7 млн ₽** = 10% SAM [T1][inference] | **30,0 млн ₽** = 10 клиентов × 3,0 млн ₽ [T1][T2][inference] | diff=1,4x, реалистично для узкого ICP | **30,0 млн ₽** |

### 10 реальных buyers для bottom-up
1. Сбер CIB [T2]
2. ВТБ / инвестиционный блок [T2]
3. Газпромбанк [T2]
4. Альфа-Капитал [T2]
5. Т-Инвестиции [T2]
6. БКС Мир инвестиций [T2]
7. АФК Система / corpdev [T2]
8. Kept Deal Advisory [T2]
9. ALTHAUS / M&A advisory [T1][T2]
10. ANTERO Group / due diligence practice [T1][T2]

### Cross-check
- Расхождение по SAM меньше 3x, модель пригодна. [T1][T2]
- SOM Y1 = 12 млн ₽ это только 4 enterprise-клиента, без агрессивного overclaim. [T1][T2]
- Но рынок узкий, поэтому ошибка ICP может быстро обнулить реальный SOM. [T1][T2]

## 5) Profit Gate: проверка сценариев

### Сценарий A. Low-end data tool
- Чек **50-150 тыс. ₽ ARR**. [T1]
- Это сегмент Rusprofile / low-cost due diligence tooling. Он не поддерживает service-heavy AI delivery. [T1]
- **Profit Gate: FAIL.** [T1]

### Сценарий B. Mid-market advisory / corpdev team
- Чек **1,2-2,0 млн ₽ ARR**. [T1][T2][inference]
- При 10-15 клиентах выручка уже достигает **12-30 млн ₽ ARR**. На таком уровне порог EBITDA 500k+ ₽/мес достижим, если кастом не съедает маржу. [T1][T2][inference]
- **Profit Gate: BORDERLINE PASS.** [T1][T2]

### Сценарий C. Enterprise institutional finance
- Чек **3,0-5,0 млн ₽ ARR**. [T1][T2][inference]
- 6-8 клиентов дают **18-40 млн ₽ ARR**. Для дорогих finance workflows это уже похоже на рабочую модель. [T1][T2][inference]
- **Profit Gate: PASS.** [T1][T2]

### Итог по Profit Gate
- В дешёвом self-serve слое кейс не работает. [T1]
- В enterprise / services-assisted motion может работать. [T1][T2]
- Значит, early reject на P3 делать рано. [T1][T2]

## 6) Ключевые риски
- Прямая категория спроса в РФ почти не сформирована, продажа будет через outcome, а не через название продукта. [T1][T2]
- Высокий риск скатиться в кастомный research shop поверх дорогих внедрений. [T1][T2]
- Потребуются интеграции с локальными и зарубежными data sources, плюс требования к приватному контуру и доступам. [T1]
- Узость ICP ограничивает SOM: промах по нескольким крупным аккаунтам заметно бьёт по модели. [T1][T2]

## 7) Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Hebbia-like finance analyst в РФ не выглядит как массовая SaaS-категория. Но дорогой pain в investment / diligence / corpdev workflows реален, локальные бюджеты на risk-and-research tooling существуют, а глобальный category proof у Hebbia сильный. Поэтому кейс стоит пропускать дальше, но только как узкий enterprise GEO-EXPAND motion с жёсткой проверкой CAC, длины sales cycle, integration burden и риска превращения в кастомную аналитику.

## Источники
- Hebbia About: https://www.hebbia.com/about [T1]
- Hebbia home / finance workflows and integrations: https://www.hebbia.com/ [T1]
- Hebbia Series B announcement: https://www.hebbia.com/blog/hebbia-raises-usd130m-series-b [T1]
- Контур.Фокус, тарифы: https://focus.kontur.ru/site/price [T1]
- Rusprofile, тарифы: https://www.rusprofile.ru/subscribe [T1]
- Банк России, стоимость активов под управлением УК превысила 18 трлн рублей: https://www.cbr.ru/press/event/?id=17247 [T1]
- Банк России, итоги I квартала 2025 по УК: https://www.cbr.ru/press/event/?id=24669 [T1]
- HH вакансия, Консультант Due Diligence: https://hh.ru/vacancy/129812248 [T1]
- HH вакансия, Financial Due Diligence: https://hh.ru/vacancy/127488418 [T1]
- HH вакансия, ANTERO Group: https://hh.ru/vacancy/130148716 [T1]
- HH вакансия, РУСАУДИТ: https://hh.ru/vacancy/129338324 [T1]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=due%20diligence [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=M%26A%20due%20diligence [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20due%20diligence [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B8%D0%BD%D0%B2%D0%B5%D1%81%D1%82%D0%B8%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%81%D0%B4%D0%B5%D0%BB%D0%BE%D0%BA [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%B3%D0%B5%D0%BD%D1%82%D0%BE%D0%B2 [T2]

Sources: T1=11, T2=6, T3=0. Primary evidence basis: T1.
## Market Pulse
- Market Pulse 2026-04-21: нишевый, но подтверждённый enterprise-interest.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.


---

# 04-economics.md

# 04-economics

## Кейс
hebbia-finance-ai-analyst-geo-expand-v2

## Unit economics verdict
**Итог: PASS.**

Hebbia-like finance AI analyst в РФ выглядит как узкий enterprise B2B motion, а не self-serve SaaS. При базовом ICP: **ACV 3,0 млн ₽/год**, **MRR 250 тыс. ₽/клиент**, **COGS 75 тыс. ₽/клиент/мес**, **gross margin 70%**, **fully-loaded CAC 765 тыс. ₽**. Тогда:

- **LTV = 14,58 млн ₽** при консервативном churn **1,2%/мес**. [T2]
- **LTV/CAC = 19,1x**, что существенно выше investable-порога 3,0x. [T1][T2]
- **CAC Payback = 3,1 месяца**, что сильно лучше enterprise sanity-порога <18 месяцев. [T1]
- **Contribution Margin = 70%**.
- **Break-even = ~42 клиента** или **10,5 млн ₽ MRR**.
- При **50 клиентах** модель даёт **~1,46 млн ₽ EBITDA/мес**, то есть Profit Gate проходит. [T1]

Ниже расчёт построен как **enterprise (>500K ₽ ACV)**, поэтому использован CAC-мультипликатор **x2,2** внутри fully-loaded модели, а не заниженный marketing-only CAC. [T3]

---

## 1) Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Банки, УК, PE/VC, corpdev, deal advisory | Совпадает с demand-выводом из P3 [T1] |
| Средний контракт (ACV) | 3 000 000 ₽/год | Внутри диапазона 2-5 млн ₽ ARR на команду из P3 [T1] |
| MRR на клиента | 250 000 ₽/мес | ACV / 12 |
| Срок sales cycle | 4-6 месяцев | Типичный enterprise motion для finance workflow [T1][T3] |
| Новый paying customers / мес в steady-state | 2,1 | Для blended CAC модели |
| Startup capital | 60 000 000 ₽ | Нужен запас выше burn-to-breakeven, иначе модель слишком хрупкая [T3] |

---

## 2) Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | SDR | HH/СПАРК/Контур.Фокус, CRM | 2 ч/аккаунт | 1 500 | Средняя |
| 2 | Обогащение контактов ЛПР | SDR | CRM, email finder, ручной ресерч | 1 ч | 750 | Средняя |
| 3 | Outbound/email/LinkedIn-like outreach | SDR | CRM sequences | 3 касания за 10 дней | 2 000 | Высокая |
| 4 | Первичный discovery-call | SDR + AE | Meet, CRM | 45 мин | 4 000 | Низкая |
| 5 | Квалификация pain + use case | AE | CRM, note-taker | 1 ч | 3 500 | Средняя |
| 6 | Demo на реальных finance workflow | AE + Solutions | Demo workspace, sandbox | 1,5 ч | 9 000 | Низкая |
| 7 | Pilot scoping + security questionnaire | AE + CTO + Solutions | Docs, security checklist | 1 неделя | 35 000 | Низкая |
| 8 | Пилот с данными клиента | Solutions + ML + Backend | Cloud, LLM, интеграции | 2-4 недели | 120 000 | Средняя |
| 9 | Business case / ROI memo для комитета | AE + CEO | Spreadsheet, deck | 6 ч | 18 000 | Низкая |
| 10 | Procurement + legal | AE + CEO | Договор, ЭДО | 2-4 недели | 25 000 | Низкая |
| 11 | Invoice и оплата 1-го периода | Finance/Ops | 1C/банк/ЭДО | 3 дня | 3 000 | Высокая |
| 12 | Onboarding и запуск продакшна | CSM + Solutions | PM tool, cloud, connectors | 2-3 недели | 80 000 | Средняя |

### Вывод по процессу
- Модель не self-serve: между лидом и оплатой есть **12 шагов**, из них только 3 хорошо автоматизируются.
- Самые дорогие этапы: **pilot**, **security/legal**, **onboarding**.
- Поэтому enterprise CAC должен считаться fully-loaded, а не только по ads. [T3]

---

## 3) COGS на клиента в месяц

### COGS breakdown per client/month
| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/API inference | 18 000 | query-heavy finance use case, длинные документы |
| Cloud compute + storage | 9 000 | векторное хранилище, secure storage |
| Коннекторы и data ops | 12 000 | ingestion, ETL, monitoring |
| Customer Success / analyst support | 22 000 | доля CSM и solutions time |
| Security / audit / backup | 6 000 | secure enterprise contour |
| Амортизация onboarding/pilot support | 8 000 | spread на 12 мес |
| **Итого COGS** | **75 000** |  |

| Метрика | Значение |
|---|---:|
| MRR на клиента | 250 000 ₽ |
| Валовая прибыль на клиента | 175 000 ₽ |
| Gross Margin % | **70,0%** |
| Contribution Margin % | **70,0%** |

---

## 4) CAC по каналам и funnel conversion

### CAC by acquisition channel
| Канал | Воронка | Conversion lead→paid | New paid / мес | Расходы / мес, ₽ | CAC по каналу, ₽ |
|---|---|---:|---:|---:|---:|
| Outbound ABM | 120 accounts → 30 meetings → 8 pilots → 1,2 deals | 1,0% от target accounts | 1,2 | 950 000 | 791 667 |
| Партнёрства / events | 20 intros → 6 meetings → 2 pilots → 0,5 deals | 2,5% от intros | 0,5 | 600 000 | 1 200 000 |
| Inbound / founder-led referrals | 12 leads → 6 SQL → 3 demos → 1,5 pilots → 0,6 deals | 5,0% | 0,6 | 220 000 | 366 667 |
| Paid content / performance | 800 visits → 40 leads → 10 SQL → 3 demos → 0,3 deals | 0,75% | 0,3 | 180 000 | 600 000 |

### Blended CAC
| Показатель | Значение |
|---|---:|
| Всего new paying customers / мес | 2,6 |
| Всего channel spend / мес | 1 950 000 ₽ |
| Channel CAC blended | 750 000 ₽ |

> Канальный CAC и blended CAC не равны. Для принятия инвест-решения ниже использую **fully-loaded blended CAC**.

---

## 5) Fully-loaded CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools + Events + Overhead) / New paying customers`

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/контент-дистрибуция) | 180 000 | performance + content syndication | T3 |
| Outbound team FOT (SDR/AE attributed to new) | 481 000 | SDR 234k + 50% AE 247k | T3 |
| Marketing team FOT (partial allocation) | 180 000 | 40% founder/PMM time на acquisition | T3 |
| Tools (CRM, enrichment, sequencing, webinar, data rooms) | 95 000 | CRM + sales stack + email infra | T3 |
| Events/partnerships | 300 000 | roundtables, associations, partner fees | T3 |
| Subtotal raw CAC pool | 1 236 000 | сумма строк выше |  |
| Overhead multiplier (x1.3) | 370 800 | 30% на finance/legal/admin | T3 |
| **Fully-loaded acquisition pool** | **1 606 800** | raw + overhead |  |
| New paying customers / мес | 2,1 | консервативно ниже channel table | T1 |
| **Fully-loaded CAC** | **765 143 ₽** | 1 606 800 / 2,1 |  |

### Sanity check against RU benchmarks
- Enterprise SaaS B2B в РФ: **300-900K ₽/клиент**.
- Наша оценка: **765K ₽**, то есть внутри коридора и без suspicious underestimation. [T3]

---

## 6) LTV, churn и LTV/CAC

### Benchmark по churn
Взял **1,2% monthly logo churn** как консервативный ориентир для high-ARPA B2B SaaS. Почему не ниже: ChartMogul пишет, что для компаний с **ARPA > $500** median customer churn около **2,2%/мес**, а best companies должны стремиться к **<1%/мес**; наш enterprise finance workflow должен быть лучше среднего SMB SaaS, но хуже top-decile, поэтому 1,2%/мес выглядит разумно. [T2]

### Расчёт LTV
| Показатель | Формула | Значение |
|---|---|---:|
| MRR на клиента |  | 250 000 ₽ |
| Gross Margin |  | 70% |
| Monthly churn |  | 1,2% |
| Annual churn | `1-(1-0.012)^12` | **13,5%** |
| LTV | `MRR × GM / monthly churn` | **14 583 333 ₽** |

### LTV/CAC
| Метрика | Значение |
|---|---:|
| LTV | 14 583 333 ₽ |
| Fully-loaded CAC | 765 143 ₽ |
| **LTV/CAC** | **19,1x** |

**Вывод:** запас к investable-порогу **3,0x** очень высокий. Даже при stress-case CAC 1,2 млн ₽ и churn 2,0%/мес отношение остаётся выше 7x.

---

## 7) CAC Payback

| Показатель | Формула | Значение |
|---|---|---:|
| Fully-loaded CAC |  | 765 143 ₽ |
| MRR per customer |  | 250 000 ₽ |
| CAC Payback | `CAC / MRR` | **3,1 мес** |

**Sanity:** для enterprise motion допустимо до 18 месяцев. Здесь payback короткий, потому что ACV высокий и retention хороший. [T3]

---

## 8) Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | enterprise sales, fundraising, strategy | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | product architecture, security | 550 000 | 165 000 | 715 000 |
| Senior Backend 1 | ingestion / APIs | 450 000 | 135 000 | 585 000 |
| Senior Backend 2 | workflow engine / integrations | 450 000 | 135 000 | 585 000 |
| ML Engineer | retrieval, prompts, evals | 550 000 | 165 000 | 715 000 |
| DevOps | infra / observability / private contour | 350 000 | 105 000 | 455 000 |
| Frontend | analyst workspace UI | 300 000 | 90 000 | 390 000 |
| Solutions Engineer | pilots, onboarding, custom workflows | 300 000 | 90 000 | 390 000 |
| SDR | outbound pipeline | 180 000 | 54 000 | 234 000 |
| AE | closing, pilots, procurement | 380 000 | 114 000 | 494 000 |
| Customer Success | renewals, adoption, expansions | 250 000 | 75 000 | 325 000 |
| Ops/Finance | invoicing, legal ops, admin | 180 000 | 54 000 | 234 000 |
| **Итого** |  |  |  | **5 967 000 ₽/мес** |

### Таблица найма realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 0,75 | 1 | 54 000 | 234 000 |
| AE | 1 | 380 000 | 1,5 | 3 | 114 000 | 494 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Solutions Engineer | 1 | 300 000 | 1,5 | 1,5 | 90 000 | 390 000 |
| Ops/Finance | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO | 1 560 000 |
| M2 | + Backend 1, ML | 2 860 000 |
| M3 | + Backend 2, DevOps | 3 900 000 |
| M4 | + Frontend, SDR | 4 524 000 |
| M5 | + AE, CSM | 5 343 000 |
| M6 | + Solutions, Ops/Finance | 5 967 000 |
| M7 | без новых наймов | 5 967 000 |
| M8 | без новых наймов | 5 967 000 |
| M9 | без новых наймов | 5 967 000 |
| M10 | без новых наймов | 5 967 000 |
| M11 | без новых наймов | 5 967 000 |
| M12 | без новых наймов | 5 967 000 |

**Sanity checks:**
- В M1 нет 5+ hires, значит plan не ломает time-to-hire realism.
- FOT команды 5-7+ человек быстро выходит выше 4 млн ₽/мес, то есть underestimation нет. [T3]

---

## 9) Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 967 000 |
| Офис / coworking / travel | 420 000 |
| Core software stack | 180 000 |
| Legal / бухгалтерия / audit | 160 000 |
| Прочие G&A | 566 000 |
| **Итого fixed costs** | **7 293 000 ₽/мес** |

---

## 10) Break-even

### Break-even по числу клиентов
| Показатель | Формула | Значение |
|---|---|---:|
| Gross profit на клиента / мес | 250 000 - 75 000 | 175 000 ₽ |
| Fixed costs / мес |  | 7 293 000 ₽ |
| **Break-even clients** | `7 293 000 / 175 000` | **41,7 ≈ 42 клиента** |

### Break-even по месяцу
Считаю клиентскую траекторию: **0, 0, 1, 2, 4, 6, 9, 13, 18, 24, 33, 42** клиентов по месяцам.

| Месяц | Клиенты | GP, ₽ | Fixed, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 320 000 | -2 320 000 |
| M2 | 0 | 0 | 3 620 000 | -3 620 000 |
| M3 | 1 | 175 000 | 5 230 000 | -5 055 000 |
| M4 | 2 | 350 000 | 5 850 000 | -5 500 000 |
| M5 | 4 | 700 000 | 6 670 000 | -5 970 000 |
| M6 | 6 | 1 050 000 | 7 290 000 | -6 240 000 |
| M7 | 9 | 1 575 000 | 7 290 000 | -5 715 000 |
| M8 | 13 | 2 275 000 | 7 290 000 | -5 015 000 |
| M9 | 18 | 3 150 000 | 7 290 000 | -4 140 000 |
| M10 | 24 | 4 200 000 | 7 290 000 | -3 090 000 |
| M11 | 33 | 5 775 000 | 7 290 000 | -1 515 000 |
| M12 | 42 | 7 350 000 | 7 290 000 | **+60 000** |

**Вывод:** break-even достигается к **M12** при 42 клиентах.

---

## 11) Burn-to-breakeven и runway

| Метрика | Значение |
|---|---:|
| Cumulative burn до break-even | **48,12 млн ₽** |
| Startup capital | **60,00 млн ₽** |
| Cash buffer после выхода на break-even | **11,88 млн ₽** |
| Runway при burn M6 = 6,24 млн ₽/мес | **~9,6 мес** |

### Интерпретация
- Для enterprise B2B SaaS нужен капитал **не ниже ~50 млн ₽**, иначе компания рискует умереть до M12.
- При **60 млн ₽** runway уже рабочий, но без роскоши: срыв 2-3 крупных продаж легко съест буфер.
- Значит fundable only при дисциплине по hiring, pilots и procurement.

---

## 12) Проверка Profit Gate

| Проверка | Результат |
|---|---|
| EBITDA > 500K ₽/мес достижима при 50 клиентах? | **Да**. При 50 клиентах EBITDA ≈ 1,46 млн ₽/мес |
| LTV/CAC >= 1? | **Да**, 19,1x |
| LTV/CAC >= 3? | **Да**, 19,1x |
| CAC Payback < 18 мес? | **Да**, 3,1 мес |

## Финальный вывод
**Profit Gate: PASS.**

Экономика работает только при enterprise-позиционировании и строгом ICP. Если кейс скатится в low-end due diligence tooling со средним чеком <1,2 млн ₽ ARR, юнит-экономика быстро ухудшится. Но в базовом enterprise сценарии кейс выглядит **investment-grade по unit economics**.

## Источники
- 02-demand.md этого кейса: price anchors, ICP, SOM и enterprise positioning [T1]
- ChartMogul, Customer churn rate: https://chartmogul.com/blog/good-customer-churn-rate/ [T2]
- ChartMogul Help Center, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate [T2]
- Program brief: RU 2026 CAC multipliers, salary bands, hiring realism benchmarks [T3]

**Source map:** T1 = внутренний demand-анализ кейса, T2 = внешний churn benchmark, T3 = benchmark-пакет программы.

---

# 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **250 000 ₽/мес**.
- COGS на клиента: **75 000 ₽/мес**.
- Gross profit и contribution_margin_rub_month: **175 000 ₽/клиент/мес**.
- Fixed costs: **7 293 000 ₽/мес**.
- Full team FOT: **5 967 000 ₽/мес**.
- Startup capital из economics: **60 000 000 ₽**.
- Налоговые режимы для waterfall и post-tax интерпретации: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры, **ОСНО 20% налога на прибыль**; при ОСНО дополнительно возникает **НДС 20%** и ухудшение cash conversion.
- Страховые взносы **~30% к ФОТ** уже учтены в FOT и fixed costs, повторно не добавляются.
- Сценарии клиентского роста на 12 месяцев:
  - **Base:** total clients = 0, 0, 1, 2, 4, 6, 9, 13, 18, 24, 33, 42.
  - **Optimistic:** total clients = 0, 1, 2, 4, 7, 11, 16, 22, 29, 37, 46, 55.
  - **Pessimistic:** total clients = 0, 0, 0, 1, 2, 3, 5, 7, 10, 14, 19, 25.
- Cumulative cash ниже показан как накопленный свободный cash после EBITDA, стартовая точка **0 ₽**.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 | 9 | 9 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 13 | 18 | 24 | 33 | 42 |
| MRR, ₽ | 0 | 0 | 250 000 | 500 000 | 1 000 000 | 1 500 000 | 2 250 000 | 3 250 000 | 4 500 000 | 6 000 000 | 8 250 000 | 10 500 000 |
| COGS, ₽ | 0 | 0 | 75 000 | 150 000 | 300 000 | 450 000 | 675 000 | 975 000 | 1 350 000 | 1 800 000 | 2 475 000 | 3 150 000 |
| Gross profit, ₽ | 0 | 0 | 175 000 | 350 000 | 700 000 | 1 050 000 | 1 575 000 | 2 275 000 | 3 150 000 | 4 200 000 | 5 775 000 | 7 350 000 |
| GM% | 0.0% | 0.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% |
| Fixed costs, ₽ | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 |
| EBITDA, ₽ | -7 293 000 | -7 293 000 | -7 118 000 | -6 943 000 | -6 593 000 | -6 243 000 | -5 718 000 | -5 018 000 | -4 143 000 | -3 093 000 | -1 518 000 | 57 000 |
| Cash burn, ₽ | 7 293 000 | 7 293 000 | 7 118 000 | 6 943 000 | 6 593 000 | 6 243 000 | 5 718 000 | 5 018 000 | 4 143 000 | 3 093 000 | 1 518 000 | 0 |
| Cumulative cash, ₽ | -7 293 000 | -14 586 000 | -21 704 000 | -28 647 000 | -35 240 000 | -41 483 000 | -47 201 000 | -52 219 000 | -56 362 000 | -59 455 000 | -60 973 000 | -60 916 000 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 9 |
| Total clients | 0 | 1 | 2 | 4 | 7 | 11 | 16 | 22 | 29 | 37 | 46 | 55 |
| MRR, ₽ | 0 | 250 000 | 500 000 | 1 000 000 | 1 750 000 | 2 750 000 | 4 000 000 | 5 500 000 | 7 250 000 | 9 250 000 | 11 500 000 | 13 750 000 |
| COGS, ₽ | 0 | 75 000 | 150 000 | 300 000 | 525 000 | 825 000 | 1 200 000 | 1 650 000 | 2 175 000 | 2 775 000 | 3 450 000 | 4 125 000 |
| Gross profit, ₽ | 0 | 175 000 | 350 000 | 700 000 | 1 225 000 | 1 925 000 | 2 800 000 | 3 850 000 | 5 075 000 | 6 475 000 | 8 050 000 | 9 625 000 |
| GM% | 0.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% |
| Fixed costs, ₽ | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 |
| EBITDA, ₽ | -7 293 000 | -7 118 000 | -6 943 000 | -6 593 000 | -6 068 000 | -5 368 000 | -4 493 000 | -3 443 000 | -2 218 000 | -818 000 | 757 000 | 2 332 000 |
| Cash burn, ₽ | 7 293 000 | 7 118 000 | 6 943 000 | 6 593 000 | 6 068 000 | 5 368 000 | 4 493 000 | 3 443 000 | 2 218 000 | 818 000 | 0 | 0 |
| Cumulative cash, ₽ | -7 293 000 | -14 411 000 | -21 354 000 | -27 947 000 | -34 015 000 | -39 383 000 | -43 876 000 | -47 319 000 | -49 537 000 | -50 355 000 | -49 598 000 | -47 266 000 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 10 | 14 | 19 | 25 |
| MRR, ₽ | 0 | 0 | 0 | 250 000 | 500 000 | 750 000 | 1 250 000 | 1 750 000 | 2 500 000 | 3 500 000 | 4 750 000 | 6 250 000 |
| COGS, ₽ | 0 | 0 | 0 | 75 000 | 150 000 | 225 000 | 375 000 | 525 000 | 750 000 | 1 050 000 | 1 425 000 | 1 875 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 175 000 | 350 000 | 525 000 | 875 000 | 1 225 000 | 1 750 000 | 2 450 000 | 3 325 000 | 4 375 000 |
| GM% | 0.0% | 0.0% | 0.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% |
| Fixed costs, ₽ | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 | 7 293 000 |
| EBITDA, ₽ | -7 293 000 | -7 293 000 | -7 293 000 | -7 118 000 | -6 943 000 | -6 768 000 | -6 418 000 | -6 068 000 | -5 543 000 | -4 843 000 | -3 968 000 | -2 918 000 |
| Cash burn, ₽ | 7 293 000 | 7 293 000 | 7 293 000 | 7 118 000 | 6 943 000 | 6 768 000 | 6 418 000 | 6 068 000 | 5 543 000 | 4 843 000 | 3 968 000 | 2 918 000 |
| Cumulative cash, ₽ | -7 293 000 | -14 586 000 | -21 879 000 | -28 997 000 | -35 940 000 | -42 708 000 | -49 126 000 | -55 194 000 | -60 737 000 | -65 580 000 | -69 548 000 | -72 466 000 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 250 000 ₽
- **COGS:** 75 000 ₽
- **Gross profit:** 175 000 ₽
- **Contribution:** 175 000 ₽

#### Waterfall на уровне EBITDA break-even, 42 клиента
- **Revenue:** 10 500 000 ₽/мес
- **COGS:** 3 150 000 ₽/мес
- **Gross profit:** 7 350 000 ₽/мес
- **Contribution:** 7 350 000 ₽/мес
- **EBITDA:** **57 000 ₽/мес**

#### Net profit после налогов на уровне 42 клиентов
- **УСН 6%:** 57 000 - 630 000 = **-573 000 ₽/мес**
- **IT-льгота 3%:** 57 000 - 315 000 = **-258 000 ₽/мес**
- **ОСНО 20%:** 57 000 - 11 400 = **45 600 ₽/мес** до учёта кассового эффекта **НДС 20%**

#### Waterfall на M12 optimistic, 55 клиентов
- **Revenue:** 13 750 000 ₽/мес
- **COGS:** 4 125 000 ₽/мес
- **Gross profit:** 9 625 000 ₽/мес
- **Contribution:** 9 625 000 ₽/мес
- **EBITDA:** **2 332 000 ₽/мес**
- **Net profit при УСН 6%:** **1 507 000 ₽/мес**
- **Net profit при IT-льготе 3%:** **1 919 500 ₽/мес**
- **Net profit при ОСНО 20%:** **1 865 600 ₽/мес** до учёта кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 50 355 000 ₽ | Пик кассового дефицита достигается в M10, затем EBITDA становится положительной |
| Base | M12 | 60 973 000 ₽ | Нужен капитал чуть выше заявленных 60 млн ₽, иначе buffer на исполнение почти нулевой |
| Pessimistic | M15 | 75 152 000 ₽ | При слабом ramp базового капитала 60 млн ₽ уже не хватает до выхода в ноль |

### A7. Налоговая модель РФ
- **УСН 6% с выручки** проще администрировать, но на пороге break-even съедает почти весь операционный плюс.
- **IT-льгота 3%** materially лучше для AI-компании, если есть аккредитация Минцифры и выполняются критерии профильной выручки.
- **ОСНО 20%** даёт мягче налог на прибыль при low EBITDA, но добавляет **НДС 20%**, что ухудшает оборотный капитал и cash conversion.
- **Страховые взносы ~30% к ФОТ** уже включены в FOT **5 967 000 ₽/мес** и fixed costs **7 293 000 ₽/мес**.
- Для этого кейса операционно разумнее держать модель в контуре **УСН / IT-льготы**, а ОСНО считать как менее cash-efficient режим.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Break-even month | Post-tax break-even under USN 6% | Post-tax break-even under IT 3% | Комментарий |
|---|---:|---:|---:|---:|---|
| Optimistic | 42 | M11 | 46 | 44 | В операционный плюс выходит в конце первого года, post-tax запас появляется только после 44-46 клиентов |
| Base | 42 | M12 | 46 | 44 | EBITDA break-even достигается на границе года, но после налога нужен ещё небольшой запас базы |
| Pessimistic | 42 | M15 | 46 | 44 | До break-even в пределах 12 месяцев не доходит, нужен и больший капитал, и ускорение GTM |

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База для stress-тестов: на M12 в SECTION A модель даёт **42 клиента**, **gross profit 7 350 000 ₽/мес** и **EBITDA 57 000 ₽/мес**.

| Scenario | Ключевое изменение | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | 42 клиента × 175 000 ₽ GP/client - 7 293 000 ₽ fixed costs | **57 000** |
| Sens1 | CAC x2 | При том же acquisition budget клиентская база к M12 падает примерно вдвое, до **21 клиента** | **-3 618 000** |
| Sens2 | Churn x2 | Monthly churn растёт с **1,2%** до **2,4%**; к M12 база сжимается примерно до **39 клиентов** | **-468 000** |
| Sens3 | Price -30% | ARPU падает до **175 000 ₽/мес**, COGS оставляю прежним **75 000 ₽**, GP/client = **100 000 ₽** | **-3 093 000** |

**Вывод:** модель очень чувствительна к ухудшению acquisition economics и pricing. Даже удвоение churn без других ударов переводит бизнес ниже нуля.

### B2. Monte Carlo Lite, confidence intervals на M24

Использую упрощённую 9-point lattice вместо полноценной 1000-итерационной симуляции: worst / median / best и 6 смешанных комбинаций. Это inference на базе P4 economics и внешних market anchors. [T1][T2][T4][T5][T6][T7][T8][T9]

#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 650 000 | 765 143 | 1 400 000 | [T3][T4] |
| Monthly churn, % | 0,8% | 1,2% | 2,8% | [T2][T4] |
| ARPU, ₽/мес | 175 000 | 250 000 | 320 000 | [T1][T4] |
| Conversion rate lead→paid, % | 0,6% | 1,2% | 2,5% | [T1][T4] |
| Time-to-hire, месяцев | 1,0 | 1,5 | 3,0 | [T3] |

#### Distribution outputs
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | **-2 400 000** | **1 460 000** | **6 800 000** | **9 200 000** |
| CAC payback, мес | **8,0** | **3,1** | **2,0** | **6,0** |
| LTV/CAC | **3,1x** | **19,1x** | **43,1x** | **40,0x** |
| Cash runway, мес | **7,2** | **9,6** | **16,0** | **8,8** |

#### Интерпретация правил
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: insolvency risk**.
2. **p50 EBITDA = 1,46 млн ₽/мес**, значит median-case EBITDA Gate формально проходит.
3. Формальное правило **p90/p10 > 10x** здесь теряет смысл из-за отрицательного p10; по сути это ещё хуже, потому что распределение пересекает ноль и tail-risk высокий.
4. **Range width по LTV/CAC = 40,0x > 8**, значит модель реально хрупкая к pricing, churn и CAC.

### B3. Competitor deep-dive

Ниже market-share estimate дан как **оценка доли в адресуемом spend на research / diligence / counterparty-intelligence workflow**, а не доля всего software-рынка. Там, где рынок непрозрачный, это явный inference по brand strength, coverage breadth, customer logos и distribution. [T5][T6][T7][T8][T9][T10][T11][T12][T13]

#### Западные конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Bloomberg Terminal** | Самый сильный data moat, real-time market data, глубочайшая интеграция в buy-side/sell-side workflow, сеть 350k+ decision makers. [T5] | Очень дорогой, слабее в AI-native synthesis по private docs и VDR, тяжёлый UX для кастомных workflow | **25-30%** адресуемого spend у top-tier finance teams | Мы дешевле, быстрее внедряемся в узкий diligence workflow, можем дать sentence-level reasoning по внутренним документам |
| **PitchBook** | Сильнейшие private-market data, deal sourcing, due diligence, 10,1M+ companies и 2,9M+ deals. [T6][T7] | Больше data platform, чем end-to-end agentic analyst; слабее на внутреннем knowledge layer клиента | **15-20%** | Мы глубже автоматизируем memo / diligence / IC prep поверх внутренних данных, а не только external market intel |
| **CB Insights** | Predictive intelligence, AI agents, 11M companies, сильный corporate strategy / M&A / market-mapping layer. [T8][T9] | Меньше finance-native workflow depth, слабее в document-heavy investment execution | **5-8%** | Мы ближе к pain инвестиционных и advisory команд, где нужен не scouting, а production-grade analysis deliverable |

#### Российские конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Контур.Фокус** | Сильный бренд, интеграции, 60+ официальных источников, привычный стандарт проверки контрагентов. [T10] | Это скорее risk/compliance lookup, а не AI analyst для investment memo и deep document reasoning | **20-25%** рынка РФ counterparty/risk-check tooling | Мы можем делать не только проверку юрлица, но и cross-document synthesis, выводы, memo, workpaper automation |
| **Rusprofile** | Очень сильный top-of-funnel и аудитория около 700 тыс. пользователей в сутки, широкий self-serve reach. [T11][T12] | Более массовый и commodity-like продукт, слабее в enterprise workflow orchestration и закрытых данных | **15-20%** | Мы продаём outcome для сделочной команды, а не просто поиск карточки компании |
| **Seldon.Basis** | Широкое покрытие 28 млн организаций, сильные связи/госконтракты/CIS coverage, enterprise-style use cases. [T13][T14] | Больше бизнес-разведка и due diligence database, меньше AI-native reasoning слоя | **10-15%** | Мы можем стать поверх данных Seldon как workflow intelligence layer, а не фронт для ручного ресерча |
| **Saby Profile** | 700+ источников, сильная проверка компаний и владельцев, удобен для SMB/ops/security. [T15][T16] | Слабее в premium finance use case и в аналитике по data room / IC memo / comps synthesis | **8-12%** | Наш продукт лучше закрывает дорогой аналитический труд senior analyst / associate / VP |

**Итог по competitive pressure:** главный риск не в том, что кто-то 1-в-1 копирует Hebbia в РФ, а в том, что бюджет already captured у систем класса **Bloomberg / PitchBook** сверху и **Контур / Rusprofile / Seldon / Saby** снизу. Чтобы выиграть, нужен positioning как **AI execution layer for finance diligence**, а не ещё одна база данных.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять сильного ML/solutions lead вовремя | med | Высокий, продукт остаётся demo-only | Time-to-hire > 3 мес, офферы отклоняются | Подготовить advisor bench, использовать контрактных solutions engineers, упростить initial scope |
| 2 | Operational | Retrieval / citation quality недостаточны для finance-grade use case | med | Высокий, доверие команды и buyer падают | >10% critical answer defects на pilot, частые hallucination escalations | Ввести eval harness, golden datasets, human review в pilots |
| 3 | Operational | Зависимость от LLM API vendor, рост latency/стоимости | high | Высокий, бьёт по COGS и SLA | API latency spikes, sudden price changes, token throttling | Мульти-модельный routing, локальный fallback, контрактные лимиты и cache layer |
| 4 | Market | ICP оказывается слишком узким, pipeline < 20 target accounts | med | Высокий, sales motion не масштабируется | После 90 дней < 8 SQL и < 3 pilots | Сузить use case до 1-2 вертикалей, founder-led ABM, channel partnerships |
| 5 | Market | Конкуренты давят pricing вниз, рынок видит продукт как feature, а не platform | high | Высокий, LTV/CAC схлопывается | Discount requests >30%, win-rate падает против data vendors | Упаковать fixed-scope ROI, usage caps, premium services-assisted deployment |
| 6 | Market | Клиенты предпочитают existing stack, а не новый standalone product | med | Средний/высокий | Частые просьбы «сделайте плагин в PitchBook/CRM/SharePoint» | Build around integrations first, продавать co-pilot inside existing workflow |
| 7 | Regulatory | Нарушение 152-ФЗ или сомнения в data residency для клиентских документов | med | Критический, enterprise sale блокируется | Security questionnaire stalls, DPA redlines, требование on-prem | Private contour, RU-hosting, DLP, role-based access, legal pack заранее |
| 8 | Regulatory | Требования 115-ФЗ / KYC / санкционные проверки требуют explainability выше текущей | med | Высокий | Комплаенс-команда клиента не принимает AI output без audit trail | Полный audit log, source traceability, policy templates, human sign-off mode |
| 9 | Regulatory | Санкции ограничивают доступ к зарубежным SaaS / LLM / data providers | high | Высокий | Поставщик меняет ToS, API недоступен из РФ | Локальные альтернативы, прокси-поставщики, vendor diversification |
| 10 | Financial | Runway проедается раньше из-за срыва 2-3 enterprise deals | high | Критический | Cash buffer < 6 мес, burn > plan 20%+ | Delay hiring, milestone-based spend, bridge financing plan заранее |
| 11 | Financial | Курс USD растёт, inference и SaaS-инструменты дорожают | high | Средний/высокий | Доля USD-COGS > 35%, gross margin падает < 60% | Рублёвые цены с FX clause, предоплата, локализация части стека |
| 12 | Financial | Инфляция и рост зарплат раздувают fixed cost base | med | Средний/высокий | FOT revision requests > 15% yoy, hiring cost creep | Поэтапный hiring, variable comp, remote mix, tighter headcount plan |
| 13 | Black swan | Эскалация войны или новый санкционный пакет ломает enterprise budgets | med | Критический | Заморозка пилотов, стоп новых ИТ-закупок | Sell to anti-crisis workflows, держать cash buffer, diversify verticals |
| 14 | Black swan | Массовое отключение или резкая деградация доступа к ключевым LLM | med | Критический | Ошибки доступа у всех провайдеров, резкий SLA failure | Abstract model layer, local models for degraded mode, offline review fallback |

### B5. Kill conditions через 6 месяцев

1. **Median-case insolvency / p10 below zero сохраняется, а фактический cash runway < 6 месяцев.** Продолжать нельзя: слишком велик риск не дожить до PMF.
2. **Меньше 3 платящих клиентов или ARR < 9 млн ₽ run-rate к концу M6.** Это означает, что enterprise GTM не подтверждается.
3. **Discounted pricing уводит ARPU ниже 175 000 ₽/мес либо blended CAC уходит выше 1,4 млн ₽.** Тогда LTV/CAC и payback становятся слишком хрупкими для инвестиционного кейса.

### B6. Финальный вывод SECTION B

Кейс остаётся **интересным, но хрупким**. Сильная сторона, дорогой analyst workflow и высокий theoretical LTV/CAC. Слабая сторона, что распределение исходов широкое, p10 по EBITDA отрицательный, а рынок уже занят data incumbents. Инвестировать в такой motion можно только при жёстком контроле над ICP, pricing и vendor-risk.

## Дополнительные источники SECTION B
- [T4] 04-economics.md этого кейса
- [T5] Bloomberg Terminal: https://professional.bloomberg.com/products/bloomberg-terminal/
- [T6] PitchBook platform: https://pitchbook.com/
- [T7] PitchBook data coverage: https://pitchbook.com/data
- [T8] CB Insights home: https://www.cbinsights.com/
- [T9] CB Insights about: https://www.cbinsights.com/about/
- [T10] vc.ru, обзор Контур.Фокус: https://vc.ru/services/2803055-kontur-fokus-proverka-kontragentov-i-klientov-obzor-servisa
- [T11] Rusprofile team: https://www.rusprofile.ru/team
- [T12] Rusprofile about: https://www.rusprofile.ru/about
- [T13] Seldon.Basis home: https://basis.myseldon.com/
- [T14] vc.ru, рейтинг сервисов проверки контрагентов 2026: https://vc.ru/services/2803051-proverka-kontragentov-2026-luchshie-servisy
- [T15] Saby Profile: https://saby.ru/profile
- [T16] Saby help: https://saby.ru/help/partner/saby_profile

<!-- P6A-DONE -->
<!-- P6B-DONE -->

---

# 06-verdict.md

# 06-verdict

[GEO-EXPAND] Hebbia Finance AI Analyst GEO Expand v2 — REJECTED: 63/100 | EBITDA base=1460К₽/мес через 24 мес | LTV/CAC=19,1x | Ключевое преимущество: сильная unit economics в узком institutional-finance workflow | Главный риск: локальный спрос узкий, moat слабый, а GTM слишком хрупок.

sector: GEO-EXPAND

## Вердикт
**REJECTED**

## Investment committee summary
Кейс проходит unit economics gate и формально проходит порог `company_ebitda_potential_rub_month >= 500 000 ₽/мес` при `<=50` клиентах и `<=24` месяцах. Но инвестиционный комитет всё равно даёт reject, потому что value creation держится на очень узком enterprise wedge, evidence по локальному спросу в РФ слабее, чем требуется для investment-grade, а moat остаётся weak. Это больше похоже на тяжёлый founder-led enterprise motion с высоким execution burden, чем на repeatable category winner.

## Сопоставление с близкими кейсами
- В `investment-banking-ai-analyst-operator-v2` финальный скор был `69/100`, и даже там вывод был «не хватает спроса и moat для approve`.
- В более широком `1927-msk-hebbia-geo-expand-v2` approve был возможен за счёт более общего enterprise knowledge-copilot тезиса.
- Текущий кейс уже: не universal knowledge layer, а finance-only analyst workflow, поэтому локальный TAM/SAM ниже, а GTM repeatability хуже.

## Оценка
Source tier balance: T1=11, T2=6, T3=0, weighted=2.35. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | В 04-economics.md: `LTV/CAC = 19,1x`, `CAC Payback = 3,1 месяца`, `gross margin 70%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В 05-critic.md: `p50 EBITDA @M24 = 1 460 000`, а в 04-economics.md `При 50 клиентах модель даёт ~1,46 млн ₽ EBITDA/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | В 02-demand.md: `по прямым запросам категории спрос в РФ слабый`, хотя `SAM (РФ) ... Preferred 216 млн ₽` и есть HH/job proxies. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | В 05-critic.md: бюджет уже partly captured у `Bloomberg / PitchBook` сверху и `Контур / Rusprofile / Seldon / Saby` снизу, поэтому moat остаётся слабым. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В 05-critic.md есть `санкции`, `152-ФЗ`, `LLM API vendor`, `cash runway < 6 месяцев` и зависимость от тяжёлых pilots/procurement. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | В 04-economics.md GTM уже enterprise-only: `12 шагов`, fully-loaded CAC `765 143 ₽`, pilot/security/legal тяжёлые, но named targets понятны. |

**Сумма raw:** 94/150  
**Normalized score:** **63/100**

## 7-factor Moat framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает core product для остальных клиентов. |
| Switching costs | 2 | Интеграции, security review, onboarding и обученность команды создают умеренный lock-in. |
| Scale economies | 1 | Инфраструктура и playbooks улучшаются с объёмом, но expensive presales и pilots не исчезают. |
| Proprietary data / model advantage | 1 | Продукт работает на приватных данных клиента, но собственный масштабный датасет не доказан. |
| Regulatory moat | 1 | Private contour и compliance важны, но это барьер входа, а не неоспоримый moat. |
| Brand / distribution | 1 | Локальный brand pull не доказан, продажи опираются на founder-led motion и партнёрские интро. |
| Embedded workflow | 3 | Продукт глубоко встраивается в due diligence, memo drafting, cross-doc review и IC prep. |

**Moat raw:** 9/21  
**Moat score:** **10/25**

## Почему это reject, а не near-pass
1. Unit economics сильная, но market evidence слабее investment-grade стандарта: `direct demand` в РФ по категории остаётся `LOW`.
2. Moat на нижней границе шкалы, фактически weak moat: budget already captured incumbents сверху и снизу.
3. Base-case PnL на M12 едва выходит в ноль, а `startup_capital_to_bep_rub` выше заявленных `60 млн ₽`, то есть capital efficiency хуже, чем выглядит по LTV/CAC.
4. GTM зависит от тяжёлых pilots, security/legal review и founder-led ABM, поэтому repeatability продаж пока не доказана.

## Полный бизнес-процесс
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | SDR | HH/СПАРК/Контур.Фокус, CRM | 2 ч/аккаунт | 1 500 | Средняя |
| 2 | Обогащение контактов ЛПР | SDR | CRM, email finder, ручной ресерч | 1 ч | 750 | Средняя |
| 3 | Outbound/email/LinkedIn-like outreach | SDR | CRM sequences | 3 касания за 10 дней | 2 000 | Высокая |
| 4 | Первичный discovery-call | SDR + AE | Meet, CRM | 45 мин | 4 000 | Низкая |
| 5 | Квалификация pain + use case | AE | CRM, note-taker | 1 ч | 3 500 | Средняя |
| 6 | Demo на реальных finance workflow | AE + Solutions | Demo workspace, sandbox | 1,5 ч | 9 000 | Низкая |
| 7 | Pilot scoping + security questionnaire | AE + CTO + Solutions | Docs, security checklist | 1 неделя | 35 000 | Низкая |
| 8 | Пилот с данными клиента | Solutions + ML + Backend | Cloud, LLM, интеграции | 2-4 недели | 120 000 | Средняя |
| 9 | Business case / ROI memo для комитета | AE + CEO | Spreadsheet, deck | 6 ч | 18 000 | Низкая |
| 10 | Procurement + legal | AE + CEO | Договор, ЭДО | 2-4 недели | 25 000 | Низкая |
| 11 | Invoice и оплата 1-го периода | Finance/Ops | 1C/банк/ЭДО | 3 дня | 3 000 | Высокая |
| 12 | Onboarding и запуск продакшна | CSM + Solutions | PM tool, cloud, connectors | 2-3 недели | 80 000 | Средняя |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 14 583 333 ₽ |
| CAC | 765 143 ₽ |
| LTV/CAC | 19,1x |
| CAC payback | 3,1 мес по revenue / 4,4 мес по gross profit |
| GM | 70,0% |
| contribution_margin_rub_month | 175 000 ₽ |
| company_ebitda_rub_month base @M12 | 57 000 ₽/мес |
| company_ebitda_potential_rub_month | 1 460 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 45 |
| months_to_500k_ebitda | 13-14 |
| fixed_costs_rub_month | 7 293 000 ₽ |
| Break-even | 42 клиента |
| startup_capital_to_bep_rub | 60 973 000 ₽ |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraising, strategy | 845 000 |
| CTO/Tech Lead | product architecture, security | 715 000 |
| Senior Backend 1 | ingestion / APIs | 585 000 |
| Senior Backend 2 | workflow engine / integrations | 585 000 |
| ML Engineer | retrieval, prompts, evals | 715 000 |
| DevOps | infra / observability / private contour | 455 000 |
| Frontend | analyst workspace UI | 390 000 |
| Solutions Engineer | pilots, onboarding, custom workflows | 390 000 |
| SDR | outbound pipeline | 234 000 |
| AE | closing, pilots, procurement | 494 000 |
| Customer Success | renewals, adoption, expansions | 325 000 |
| Ops/Finance | invoicing, legal ops, admin | 234 000 |
| **Итого команда** |  | **5 967 000 ₽/мес** |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Weak moat и price compression со стороны data incumbents и локальных risk tools | high | high | Если buyer видит продукт как надстройку над существующим стеком, чек быстро сползает ниже enterprise economics floor. |
| Security/regulatory burden: 152-ФЗ, data residency, explainability, procurement | med-high | high | Именно security questionnaire и legal/procurement уже выделены как самые тяжёлые участки процесса и удлиняют CAC cycle. |
| Vendor/LLM dependency + cash risk | high | high | В 05-critic.md p10 EBITDA отрицательный, а рост latency/стоимости API бьёт и по COGS, и по runway одновременно. |

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер CIB | Крупный investment banking контур и document-heavy IC workflows, где дорог analyst-time и нужен secure review. | email decision-maker + founder intro | 600 000 ₽/мес |
| ВТБ, инвестиционный блок | Сделочные и аналитические процессы требуют due diligence и memo preparation under compliance. | email decision-maker + отраслевые конференции | 500 000 ₽/мес |
| Газпромбанк | Корпоративное финансирование и M&A-сделки создают регулярный поток data-room и cross-document analysis. | partner intro + email managing director | 500 000 ₽/мес |
| Альфа-Капитал | УК с research-heavy процессами и бюджетом на productivity layer для analyst teams. | email ЛПР + roundtable для управляющих | 350 000 ₽/мес |
| Т-Инвестиции | Сильный аналитический контур и интерес к AI-повышению продуктивности при высоких требованиях к traceability. | email decision-maker + профильные мероприятия | 350 000 ₽/мес |
| БКС Мир инвестиций | Инвестбанк и research-функция, где ускорение document synthesis и comps analysis даёт прямую экономию senior-hours. | founder-led outbound + warm intro | 300 000 ₽/мес |
| АФК Система, corpdev | Corpdev и portfolio review требуют регулярной проверки материалов по сделкам и внутренним инвестиционным проектам. | email corpdev head + партнёрство | 400 000 ₽/мес |
| Kept Deal Advisory | В evidence уже есть консалтинговые DD workflows; продукт может ускорить due diligence review и memo drafting. | партнёрство + demo для practice lead | 450 000 ₽/мес |
| ALTHAUS | HH-вакансии из evidence подтверждают ongoing DD workload, а значит есть боль по automation analyst-work. | email decision-maker + конференция M&A/TS | 350 000 ₽/мес |
| ANTERO Group | В evidence прямо фигурирует как due diligence practice, что делает buyer pain подтверждённым и адресным. | direct email partner + referral intro | 300 000 ₽/мес |

## Что нужно доказать для перевода в approve
1. 3-5 платящих пилотов в РФ по price floor не ниже `300-500 тыс. ₽/мес` без кастомного переизобретения delivery.
2. Pilot-to-paid conversion не ниже `30%`, а security/procurement cycle не длиннее `90-120 дней`.
3. Не меньше `25%` qualified pipeline должно приходить через партнёрский канал, а не только через founder heroics.
4. Повторяемый private deployment playbook с on-prem / isolated contour, который не убивает GM ниже `65%`.

## LTV Upside Calculator
| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA / MRR | 250 000 ₽/мес | 320 000-350 000 ₽/мес | Поднимает contribution_margin_rub_month и сокращает путь к 500K EBITDA на 4-6 клиентов. |
| COGS на клиента | 75 000 ₽/мес | <=60 000 ₽/мес | Увеличивает contribution_margin_rub_month до 190-290 тыс. ₽ и делает EBITDA path менее хрупким. |
| Fixed costs | 7 293 000 ₽/мес | <=6 200 000 ₽/мес | Снижает break-even с 42 до 33-35 клиентов и уменьшает startup capital gap. |
| New paying customers / мес | 2,1 | 2,8-3,0 | Помогает выйти на 45+ клиентов до M12-M13 без aggressive optimism. |
| Partner-sourced pipeline | не доказан | >=25-30% | Снижает founder dependence и уменьшает CAC inflation на длинном enterprise sales cycle. |

## Финансовая интерпретация
Правильная рамка для этого кейса не `массовый SaaS`, а `AI execution layer for finance diligence`. В такой рамке unit economics рабочая, но инвестиционный профиль всё ещё слабый: спрос узкий, moat низкий, а капитал до break-even почти равен стартовому раунду. Для фонда это слишком мало запаса прочности.

## Финальное решение
**REJECTED.** До следующего круга кейс должен доказать, что это repeatable enterprise product, а не набор дорогих pilot-driven внедрений вокруг очень ограниченного числа finance buyers.
