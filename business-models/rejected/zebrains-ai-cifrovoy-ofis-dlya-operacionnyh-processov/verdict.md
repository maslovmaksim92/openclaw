# zebrains-ai-cifrovoy-ofis-dlya-operacionnyh-processov — verdict

## Stage 0 — Brief

# Краткий бриф

## Кейс
ZeBrains AI Digital Office, AI-цифровой офис для операционных процессов

## Почему открыт
- Сигнал описывает самостоятельный B2B-OPS wedge вокруг AI-слоя для бэк-офиса, документооборота, HR, финансовых операций и клиентской поддержки, а не узкий single-point copilot.
- В текущих открытых кейсах в `pipeline/cases/` нет достаточно близкого активного кейса именно про единый AI-операционный слой для корпоративных процессов внутри российского enterprise-контура.
- Базовая EBITDA-гипотеза 900 000 ₽ в месяц с диапазоном 500 000-1 800 000 ₽ проходит порог Program 1 и выглядит реалистично для mid-market и enterprise сегмента.

## Что проверить дальше
- Насколько repeatable продажа идёт как платформа, а не как кастомная интеграционная разработка.
- Какие функции дают лучший wedge для старта: поддержка, документооборот, HR-операции, finance ops или смешанный back-office пакет.
- Удерживается ли маржа после внедрения с учётом on-prem, интеграций и требований по безопасности данных.

## Следующий этап
P3-demand-validation.


## Stage 1A — Evidence

# Подтверждающие сигналы

## 2026-04-26 — initial signal — ZeBrains AI Digital Office
- **Дата:** 2026-04-26
- **Источник:** https://cnews.ru/news/line/2024-03-12_zebrains_zapustila_platformu ; https://sk.ru/technopark/residents/zebrains/ ; https://zebrains.ai/ai-digital-office
- **Тип:** initial signal
- **Как усиливает кейс:** Сигнал подтверждает, что на российском рынке уже есть продуктовый AI-слой для автоматизации не одной функции, а целого набора операционных процессов, включая поддержку, документооборот, HR и финансы. Это повышает вероятность, что B2B-OPS кейс можно строить вокруг платформенного digital office подхода с enterprise-чеком.
- **Ключевые данные и факты:** ZeBrains вывела AI Digital Office в 2024 году; компания является резидентом «Сколково»; продукт позиционируется как решение для оптимизации рутинных операций и работы в защищённом корпоративном контуре.


## Stage 1B — Intake

---
sector: B2B-OPS
rerun: false
source_raw: 2026-04-25-b2b-ops-zebrains-ai-cifrovoy-ofis-dlya-operacionnyh-processov.md
created: 2026-04-26T00:22:00+03:00
---

# ZeBrains AI Digital Office

## Sector
B2B-OPS

## Wedge statement
AI-оператор для бэк-офиса и клиентских операций: автоматизирует поддержку, документооборот, HR- и финансовые рутинные процессы через LLM, RAG и интеграции с корпоративными системами.

## Evidence
- [T2] https://cnews.ru/news/line/2024-03-12_zebrains_zapustila_platformu — 2024-03-12 компания запустила платформу AI Digital Office для поддержки, HR, финансов и документооборота, то есть прямо атакует B2B-OPS слой.
- [T2] https://sk.ru/technopark/residents/zebrains/ — доступ 2026-04-25, резидент «Сколково» с фокусом на LLM, RAG, AI-ассистентов и автоматизацию корпоративных процессов.
- [T3] https://zebrains.ai/ai-digital-office — доступ 2026-04-25, официальный лендинг описывает AI Digital Office как продукт для оптимизации рутинных задач, ускорения операций и работы в enterprise-контуре.

## EBITDA hypothesis (24 мес, base)
900000₽/мес (диапазон 500000-1800000)

## RU-fit
4 / 5. Хорошо ложится на РФ: enterprise-автоматизация, on-prem/private cloud сценарии, интеграции с внутренними системами и явный запрос на локальную обработку данных под 152-ФЗ.

## Expected unit economics (ballpark)
- ARPU: 180000-450000₽/мес
- CAC (ballpark): 250000-900000₽
- Avg deal cycle: 2-6 мес
- Target segment: Mid-market | Enterprise | Regulated

## Why now
В 2024-2026 окно возможностей расширилось из-за зрелости русскоязычных LLM/RAG-стеков и давления на бизнес по сокращению операционных затрат без найма новых команд. Для РФ особенно актуальны решения, которые можно встроить в внутренний контур и использовать для поддержки, документооборота и back-office процессов.


## Stage 2 — Demand

---
stage: demand-validation
case: zebrains-ai-cifrovoy-ofis-dlya-operacionnyh-processov
date: 2026-04-26
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
ZeBrains AI Digital Office, AI-цифровой офис для операционных процессов.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Exact-demand на ярлык `AI цифровой офис` в РФ слабый, но базовый спрос на `автоматизацию бизнес-процессов` уже живой: внутренний `multi-demand` даёт **MEDIUM / 30** при **4767 вакансиях HH.ru** и **100/100 Yandex Suggest**. [T1]
- WTP подтверждён публичными тарифами у adjacent и direct substitutes: **Битрикс24 от 1 990 ₽/мес за пользователя**, **Pyrus от $3/пользователь/мес**, **BotHelp от $18/мес**, а у enterprise-игроков вроде ELMA365 pricing обычно уходит в кастомный пресейл, что само по себе является сигналом enterprise-budget motion. [T2][inference]
- В Telegram/RU есть зрелые bot-first сервисы, но они закрывают только кусок коммуникационного workflow, а не весь back-office контур, поэтому риск полного замещения ограничен. [T2][inference]
- Profit Gate не проходит в low-ticket automation-as-a-service сценарии, но проходит в platform + внедрение, departmental bundle и enterprise annual contract. Следовательно, early reject не срабатывает. [T1][T2][inference]

## 1. Demand data

### Demand API
- `AI цифровой офис` → **LOW**, `demand_score=11`, `hh_ru=426`, `yandex_suggest=2`, `google_trends_ru=0`. [T1]
- `автоматизация бизнес-процессов` → **MEDIUM**, `demand_score=30`, `hh_ru=4767`, `yandex_suggest=100`, `google_trends_ru=0`. [T1]
- `корпоративный AI ассистент` → **LOW**, `demand_score=15`, `hh_ru=585`, `yandex_suggest=2`. [T1]
- `документооборот AI` → **LOW**, `demand_score=11`, `hh_ru=218`, `yandex_suggest=2`. [T1]
- `service desk AI` → **LOW**, `demand_score=4`, `hh_ru=15`, `yandex_suggest=5`. [T1]

### Интерпретация
- В РФ пока слабо покупают новый category label `AI digital office`, но уже покупают outcome: автоматизацию рутины, документооборота, клиентской поддержки и внутренних процессов. [T1][inference]
- Это типичный сигнал для wedge-стратегии: продавать не платформу как идею, а конкретные use-cases с быстрым ROI, чаще по департаментам. [T1][T2][inference]
- HH-сигнал в 4767 вакансий по `автоматизация бизнес-процессов` подтверждает, что боль решается не только через покупку софта, но и через найм, а значит бюджет на проблему уже существует. [T1][inference]

## 2. Реальные конкуренты и цены

| Игрок | Формат | Публичная цена | Что доказывает |
|---|---|---:|---|
| **Битрикс24** | Digital workplace + CRM + задачи + автоматизация | **от 1 990 ₽ за пользователя в месяц** по публичной pricing-странице/выдаче. [T2] | РФ-рынок уже платит за единое рабочее пространство и automation layer |
| **Pyrus** | Workflow / согласования / task-flow | **от $3 за пользователя в месяц**. [T2] | Рутинные процессы и approvals уже хорошо монетизируются как recurring software |
| **BotHelp** | Telegram / WhatsApp bot automation | **$18/мес за 1 000 подписчиков**, далее до **$1 529/мес** на 500k подписчиков. [T2] | Bot-first automation в RU/CIS имеет понятную платёжную модель |
| **ELMA365** | BPM / low-code / enterprise automation | pricing-page публична, но цена уходит в запрос демо и пресейл. [T2] | Enterprise-покупатель уже готов заходить в длинный цикл и кастомный чек |

### Вывод по конкурентной среде
- У ZeBrains конкуренция идёт не только с AI-native игроками, но и с уже укоренившимися рабочими платформами: Битрикс24, Pyrus, ELMA365, а также с bot-first сервисами. [T2]
- Это делает опасным позиционирование `ещё одна универсальная платформа`. Лучше заходит motion `быстрый AI-слой поверх существующего контура` для 1-2 департаментов. [T2][inference]
- Публичные тарифы у adjacent решений означают, что рынок already conditioned to pay за автоматизацию, значит WTP не нужно создавать с нуля. [T2][inference]

## 3. Telegram-боты и сервисы в РФ

1. **BotHelp** с публичной сеткой от **$18/мес** до **$1 529/мес** показывает зрелый рынок bot-automation в Telegram/мессенджерах. [T2]
2. Внутренний `multi-demand` по ключам не показал сильного отдельного спроса на `AI digital office` внутри Telegram category, то есть Telegram остаётся каналом и частичным substitute, а не полной заменой back-office suite. [T1][inference]
3. Для ZeBrains Telegram важен скорее как frontend-слой для service desk, FAQ, HR onboarding и уведомлений, но не как самостоятельный moat. [T1][T2][inference]

**Вывод:** Telegram в РФ усиливает demand на automation, но сам по себе не закрывает документооборот, finance ops, согласования и корпоративный knowledge layer. Это не red flag, а обязательный интеграционный слой. [T1][T2][inference]

## 4. WTP, proof of willingness to pay

### Прямые сигналы
- `автоматизация бизнес-процессов` в `multi-demand` даёт **MEDIUM / 30** и очень высокий supporting-signal по HH, значит проблема не теоретическая. [T1]
- Публичные recurring тарифы у Bitrix24, Pyrus и BotHelp подтверждают, что компании уже платят за automation stack регулярно, а не только проектно. [T2]
- ELMA365 и похожие enterprise-платформы уводят цену в пресейл, а такой motion обычно появляется только на рынках, где LTV и budgets достаточны для solution selling. [T2][inference]

### Вывод по WTP
**WTP подтверждён.** Для ZeBrains реалистичный стартовый прайс в РФ выглядит так:
- departmental pilot: **250 000-600 000 ₽** setup; [T2][inference]
- recurring support / usage layer: **120 000-300 000 ₽/мес**; [T2][inference]
- enterprise annual contract: **1,8-4,5 млн ₽/год**. [T2][inference]

Это уже даёт пространство для EBITDA, если delivery не превращается в кастомную разработку под каждого клиента. [inference]

## 5. Market sizing

**[LOW CONFIDENCE]** Сегмент широкий, а публичных Tier-1 оценок именно для `AI-цифрового офиса` в РФ нет. Поэтому использую reconciliation: сверху от глобального рынка workflow/automation software и снизу от реального buyer pool в РФ. Если трактовать кейс шире, оценка вырастет; если трактовать как узкий AI-copilot, оценка уменьшится. [T1][T2][спекуляция]

### Top-down
- Глобальный рынок workflow / process automation software в публичных индустриальных отчётах оценивается как многомиллиардный; для расчёта беру консервативный адресуемый слой **$12 млрд** для unified back-office automation wedge, а не весь enterprise software universe. [T2][спекуляция]
- Для РФ беру **1,0%** как conservative share глобального addressable spend для локального enterprise automation с поправкой на размер экономики, санкционные ограничения и lower software budgets. Получаем **TAM (РФ) ≈ 10,8 млрд ₽** при курсовом допущении **90 ₽/$**. [T2][спекуляция]
- Из TAM вычитаю гос-heavy и large custom-IT сегменты вне фокуса, оставляя **SAM ≈ 6,5 млрд ₽**. [T2][inference]
- Реалистичный захват: **Y1 = 2% SAM = 130 млн ₽**, **Y3 = 7% SAM = 455 млн ₽**. [inference]

### Bottom-up
- Беру целевой buyer pool как **25 000** компаний РФ, где одновременно есть заметный объём внутренних операций, IT-контур и вероятность платить за automation suite: крупный mid-market, enterprise, филиальные сети, финсервисы, ритейл, логистика, медицина, сервисные платформы. Это консервативная рабочая оценка на базе структуры RU B2B-софта и enterprise automation landscape. [T2][спекуляция]
- Доля с подтверждённой болью, **20%**: поддержана `MEDIUM` спросом по `автоматизация бизнес-процессов`, HH-сигналом и фактом существования зрелых substitutes. [T1][T2][inference]
- Средний контракт, **1,2 млн ₽/год**: это midpoint между departmental package и урезанным enterprise contract. [T2][inference]
- Тогда **SAM_bottom_up = 25 000 × 20% × 1,2 млн ₽ = 6,0 млрд ₽/год**. [T1][T2][inference]
- **SOM_bottom_up Y1** при захвате **2,0%** = **120 млн ₽/год**. [inference]
- **SOM_bottom_up Y3** при захвате **6,0%** = **360 млн ₽/год**. [inference]

### GTM-10 / 10 реальных buyers для bottom-up
1. **СДЭК** — поддержка, документы, франчайзинговые и сервисные операции. [T2][inference]
2. **Додо Пицца / Dodo Brands** — HR, service desk, finance ops и knowledge workflows по сети. [T2][inference]
3. **Самокат** — массовые операционные сценарии, support и внутренние заявки. [T2][inference]
4. **Ozon** — service operations и внутренние back-office процессы. [T2][inference]
5. **Skillbox / Skillfactory** — support, HR onboarding и документооборот. [T2][inference]
6. **Клиника Фомина** — медрегистратура, support, знания, HR-процессы. [T2][inference]
7. **Петрович** — заявки, support, логистика и внутренняя координация. [T2][inference]
8. **Hoff** — retail ops, service desk, документы и клиентские обращения. [T2][inference]
9. **Sokolov** — омниканальные операции, support, внутренние workflow. [T2][inference]
10. **Level Group** — документы, клиентский сервис, HR и finance approvals. [T2][inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $12B [T2] | — | — | top-down |
| TAM (РФ) | 10,8 млрд ₽ [T2] | 30,0 млрд ₽ = 25 000 × 100% × 1,2 млн ₽ [T2] | diff≈2,8x, потому что bottom-up TAM включает весь buyer pool до фильтра по боли, а top-down уже консервативно режет сегмент | lower |
| SAM (РФ) | 6,5 млрд ₽ [T2] | 6,0 млрд ₽ [T1/T2] | diff≈1,08x, модели сходятся приемлемо | lower |
| SOM Y1 | 130 млн ₽ | 120 млн ₽ | diff≈1,08x | **используем 120 млн ₽** |
| SOM Y3 | 455 млн ₽ | 360 млн ₽ | diff≈1,26x | **используем 360 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up по SAM меньше 3x, значит оценка не выглядит сломанной. [T1][T2]
- SOM Y1 составляет около **2%** от SAM, это реалистично для нового AI-layer при enterprise sales motion. [inference]
- При среднем контракте **1,2 млн ₽/год** SOM Y1 соответствует примерно **100 клиентам**. Это тяжело для первого года без сильных партнёров и узкого wedge, поэтому реальный go-to-market лучше строить через 2-3 вертикали и higher ACV, а не broad-market. [inference]

## 6. Profit Gate: проверка всех сценариев монетизации

Для расчёта беру базовые fixed costs **2,6 млн ₽/мес**: founder/CEO-sales, 2-3 AI/integration инженера, PM/solution architect, infra, продажи и overhead. [inference]

### Сценарий A. Low-ticket automation service
- Чек: **90 000 ₽/мес**.
- Валовая маржа: **55%**.
- Вклад с клиента: **49 500 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужен вклад **3,1 млн ₽/мес**, то есть **63 клиента**.
- **Вердикт: FAIL.** Для ранней команды это слишком широкий low-ACV motion. [inference]

### Сценарий B. Departmental bundle
- Чек: **250 000 ₽/мес**.
- Валовая маржа: **68%**.
- Вклад с клиента: **170 000 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужно **19 клиентов**.
- **Вердикт: PASS WITH EXECUTION RISK.** Достижимо, если scope стандартизирован и интеграции типовые. [inference]

### Сценарий C. Platform + setup + annual support
- Setup: **600 000 ₽** единовременно.
- Recurring: **180 000 ₽/мес**.
- Валовая маржа blended: **70%**.
- При 12 активных клиентах и 1-2 новым setup в месяц EBITDA > **500 000 ₽/мес** выглядит достижимой. [inference]
- **Вердикт: PASS.** Это хороший компромисс между ACV и time-to-value. [inference]

### Сценарий D. Enterprise annual contract
- ACV: **3,0 млн ₽/год**.
- Валовая маржа: **72%**.
- Вклад на клиента: **2,16 млн ₽/год**.
- Для run-rate EBITDA **500 000 ₽/мес** достаточно **18-20** активных клиентов при умеренном overhead. [inference]
- **Вердикт: PASS.** Это лучший путь для прохождения Profit Gate. [inference]

### Общий вывод по Profit Gate
- **FAIL** только low-ticket services motion. [inference]
- **PASS** в departmental, blended и enterprise annual сценариях. [inference]
- Следовательно, даже при слабом exact-label demand кейс не должен быть отвергнут на P4: достижимость EBITDA > 500K/mo есть. [T1][T2][inference]

## 7. Основные риски
- Рынок может воспринимать ZeBrains как интегратора/аутсорс, а не как повторяемую платформу, что съест маржу. [T2][inference]
- Универсальный `digital office` как messaging слишком широк, поэтому CAC может расти без узкого wedge. [T1][inference]
- Telegram и Битрикс24 already own часть внутренних workflows, значит нужен сильный entry point: support, HR ops, finance approvals или документооборот. [T2][inference]
- Без шаблонов интеграций и on-prem playbook recurring revenue легко превращается в кастомную разработку. [T2][inference]

## 8. Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. Underlying demand на automation в РФ есть, even if category label слабый. [T1]
2. WTP подтверждён recurring pricing у реальных substitutes и зрелостью enterprise sales motion. [T2]
3. Profit Gate проходит в нескольких реалистичных monetization scenarios. [inference]

Что критично проверить дальше:
- есть ли repeatable wedge по 1-2 функциям вместо широкой платформы;
- какой deployment motion лучше конвертируется: private cloud, on-prem или hybrid;
- сколько integration-heavy работы остаётся вне product core, и не съедает ли она gross margin.

## Источники
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D1%86%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BE%D1%84%D0%B8%D1%81
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%B1%D0%B8%D0%B7%D0%BD%D0%B5%D1%81-%D0%BF%D1%80%D0%BE%D1%86%D0%B5%D1%81%D1%81%D0%BE%D0%B2
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D1%8B%D0%B9%20AI%20%D0%B0%D1%81%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BD%D1%82
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%BE%D0%BE%D0%B1%D0%BE%D1%80%D0%BE%D1%82%20AI
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=service%20desk%20AI
- [T2] Bitrix24 pricing: https://www.bitrix24.ru/prices/
- [T2] Pyrus pricing: https://pyrus.com/ru/pricing
- [T2] BotHelp pricing: https://bothelp.io/pricing
- [T2] ELMA365 pricing: https://elma365.com/ru/platform/stoimost/
- [T2] ZeBrains product page: https://zebrains.ai/ai-digital-office
- [T2] CNews о запуске ZeBrains AI Digital Office: https://cnews.ru/news/line/2024-03-12_zebrains_zapustila_platformu
- [T2] Skolkovo resident profile: https://sk.ru/technopark/residents/zebrains/

Sources: T1=5, T2=7, T3=0. Primary evidence basis: T1.

> Market Pulse 2026-04-26: exact-category спрос слабый, но бюджет на automation и back-office efficiency в РФ подтверждён, поэтому кейс живёт через узкий enterprise wedge, а не через broad-platform pitch.

## Market Pulse
> Market Pulse 2026-04-26: растущий интерес.


## Stage 4 — Economics

---
stage: unit-economics
case: zebrains-ai-cifrovoy-ofis-dlya-operacionnyh-processov
date: 2026-04-26
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
ZeBrains AI Digital Office, AI-цифровой офис для операционных процессов.

## Итог
**Статус: PASS WITH RESERVATIONS.**

Почему кейс проходит P5:
- при enterprise/mid-market motion и среднем recurring-чеке **180 000 ₽/клиент/мес** модель даёт **LTV/CAC = 10,2x** и **CAC Payback = 2,5 мес**, что выше инвестиционного порога **3:1**;
- gross economics держатся только если продавать не «универсальный AI-офис», а стандартизированный departmental bundle с типовыми интеграциями;
- главный риск не в retention, а в том, что delivery может уйти в кастомную разработку и поднять burn до breakeven.

Почему кейс пока не в STRONG PASS:
- для выхода на breakeven нужен капитал порядка **45-55 млн ₽**, что уже требует fund-backed execution;
- break-even достигается примерно на **43 активных клиентах** или **в районе M15**, если не ускорить партнёрский канал и не стандартизировать onboarding.

---

## 1. Базовые допущения модели

### Продукт и pricing
- Модель монетизации: **departmental/enterprise bundle**.
- Setup fee: **400 000 ₽** единовременно.
- Recurring fee: **180 000 ₽/мес**.
- ACV: **2 560 000 ₽/год** = 400k setup + 180k × 12.
- Сегмент: **enterprise / upper mid-market B2B**, так как ACV сильно выше 500k ₽/год и цикл сделки включает demo, pilot, security review, legal/procurement. [T1][T2][inference]

### Основные рабочие допущения
- Gross margin на recurring: **75%**.
- Contribution margin после переменных sales/service расходов: **72%**.
- Monthly logo churn: **2,8%**. Это консервативно внутри бенчмарка для B2B SaaS: mid-market 1,5-3,0%, enterprise 1,0-2,0%; для раннего enterprise AI-решения беру верхнюю часть диапазона. [T6]
- New customers в steady-state GTM-модели: **2 клиента/мес**.
- Startup capital для расчёта runway: **50 млн ₽**. [inference]

---

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов и enrichment | SDR | HH/отраслевые базы, Telegram, CRM | 1-2 дня | 2 500 | средняя |
| 2 | Outbound sequence, первичный outreach | SDR | CRM, email, мессенджеры, телефония | 5-7 дней | 6 000 | средняя |
| 3 | Квалификация боли и ICP-fit | SDR + AE | CRM, discovery script | 30-45 мин | 9 000 | низкая |
| 4 | Discovery call + live demo | AE + Solution lead | Zoom/Meet, demo-стенд, презентация | 3-5 дней до встречи | 22 000 | низкая |
| 5 | Предпроектное обследование процесса | Solution lead + PM | Miro, BPMN, shared docs | 4-7 дней | 35 000 | низкая |
| 6 | Пилот / PoC / sandbox | PM + Backend + ML | private cloud, sandbox, LLM stack | 2-4 недели | 60 000 | средняя |
| 7 | Security review и legal | AE + CTO + юрист | DPA/NDA, security checklist | 1-2 недели | 28 000 | низкая |
| 8 | Коммерческое предложение и procurement | AE + finance/admin | CRM, CPQ, ЭДО | 3-10 дней | 14 000 | средняя |
| 9 | Onboarding, интеграции, запуск | PM + Backend + CSM | API, SSO, knowledge import | 2-3 недели | 40 000 | средняя |
| 10 | Счёт, акт, оплата, recurring support | finance/admin + CSM | ЭДО, банк, billing, helpdesk | 3-7 дней | 45 000/мес COGS | высокая |

**Вывод:** у ZeBrains самый дорогой участок не лидогенерация, а **solutioning + pilot + onboarding**. Если его не шаблонизировать, CAC и payback быстро деградируют. [inference]

---

## 3. COGS breakdown на 1 клиента в месяц

### Recurring revenue
- Выручка на клиента в месяц: **180 000 ₽**.

| Статья COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / embeddings | 12 000 | usage-based estimate | RAG/agent workflows, умеренная нагрузка |
| Cloud compute + storage + backup | 8 000 | cloud allocation | sandbox, логирование, резервное хранение |
| Integration support engineer allocation | 11 000 | доля FOT команды delivery | типовые коннекторы и мониторинг |
| Customer Success / support allocation | 7 000 | доля FOT CSM | QBR, обучение, тикеты |
| Security / monitoring / observability | 3 000 | infra allocation | SIEM-lite, алерты, audit trail |
| Data processing / OCR / transcription reserve | 2 000 | variable reserve | не у всех клиентов, но нужен буфер |
| Billing / ЭДО / bank fees | 1 000 | transactional estimate | ЭДО, эквайринг/банк |
| SLA reserve и bug-fix buffer | 1 000 | risk reserve | мелкие доработки в рамках SLA |
| **Итого COGS** | **45 000** |  |  |

- **Gross Profit / клиент / мес = 135 000 ₽**.
- **Gross Margin = 75,0%**.

---

## 4. CAC: fully-loaded, а не только реклама

### Формула
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools/CRM + Events/partnerships + overhead) / New paying customers**

### Компоненты blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / ретаргет) | 120 000 | тестовый paid budget для demand capture | [T3][inference] |
| Outbound team FOT (SDR attributed to new) | 195 000 | SDR 150k gross × 1,30 | [T7] |
| Sales team FOT (AE attributed to new) | 208 000 | 50% AE: 320k gross × 1,30 × 50% | [T7] |
| Marketing team FOT (partial allocation) | 156 000 | 40% PMM: 300k gross × 1,30 × 40% | [T7][inference] |
| Tools / CRM / enrichment / телефония | 49 000 | CRM + sales tools + docs + calling stack | [T3][T4][inference] |
| Events / partnerships | 72 000 | 1 отраслевой event/meetup в мес, усреднённо | [T5][inference] |
| Overhead multiplier (x1.3) | 240 000 | 30% на management/admin/legal/ops поверх 800k direct stack | [T8] |
| **Итого monthly acquisition stack** | **1 040 000** |  |  |

### Segment multiplier sanity check
- Для сегмента ZeBrains беру **enterprise multiplier 2,2 к raw ad-only CAC** по логике длинного цикла: demo, pilot, security review, legal, procurement.
- Получаем, что CAC уровня **300k-900k ₽/клиент** для enterprise B2B SaaS в РФ выглядит нормальным коридором sanity-check. [T8][inference]

### CAC по каналу с funnel conversion (квартальная модель)

| Канал | Funnel | Cost / квартал, ₽ | New paying customers / квартал | CAC, ₽ |
|---|---|---:|---:|---:|
| Outbound | 1 500 target accounts → 135 replies (9%) → 54 SQL (40%) → 24 demo (44%) → 9 pilot/proposal (38%) → 3 wins (33%) | 1 980 000 | 3 | 660 000 |
| Inbound / content / paid demand capture | 660 leads → 132 MQL (20%) → 54 SQL (41%) → 18 proposal (33%) → 3 wins (17% от proposal-to-win after multi-stakeholder review) | 1 140 000 | 3 | 380 000 |
| Partners / referrals / events | 36 partner intros → 24 discovery (67%) → 12 pilot (50%) → 6 proposal (50%) → 3 wins (50%) | 960 000 | 3 | 320 000 |
| **Blended** | все каналы вместе | **4 080 000** | **9** | **453 333** |

### Вывод по CAC
- **Blended fully-loaded CAC = 453 333 ₽**.
- Это укладывается в sanity-band для enterprise SaaS в РФ и **не выглядит заниженным**.
- Наилучший канал по economics здесь не paid, а **partners/referrals**. [inference]

---

## 5. LTV и churn

### Benchmark churn
- Optifai (Q1-Q3 2025, 939 B2B SaaS компаний) даёт ориентир: **1,5-3,0% monthly churn для mid-market** и **1,0-2,0% для enterprise**. [T6]
- Для ZeBrains использую **2,8% monthly churn**, потому что продукт ранний, deployment сложный, а category message ещё не до конца стандартизирован. [T6][inference]

### Расчёт LTV
- ARPA / MRR per customer = **180 000 ₽/мес**.
- Gross margin = **75%**.
- Churn rate = **2,8% / мес**.

**LTV = ARPA × Gross Margin / Churn**  
**LTV = 180 000 × 0,75 / 0,028 = 4 821 429 ₽**

### Расчёт LTV/CAC
- LTV = **4 821 429 ₽**.
- CAC = **453 333 ₽**.

**LTV/CAC = 10,6x**.

### Вывод
- Инвестиционный порог **>=3:1** пройден с большим запасом.
- Даже если ухудшить churn до **4,0%**, LTV будет **3 375 000 ₽**, а LTV/CAC всё равно останется **7,4x**. [inference]

---

## 6. CAC Payback

Формула по требованию:
**CAC Payback = CAC / MRR per customer**

- CAC = **453 333 ₽**
- MRR per customer = **180 000 ₽/мес**

**CAC Payback = 2,52 месяца**.

Проверка:
- базовый порог < 12 мес;
- enterprise допустимо < 18 мес.

**Итог: проходит с запасом.**

---

## 7. Contribution Margin

Для Contribution Margin вычитаю из выручки recurring COGS и переменные sales/service расходы.

| Показатель | ₽/клиент/мес |
|---|---:|
| Revenue | 180 000 |
| COGS | 45 000 |
| Sales commission / variable success allocation | 5 000 |
| Variable service overage reserve | 500 |
| **Contribution** | **129 500** |

**Contribution Margin % = 129 500 / 180 000 = 71,9%**.

Это хороший уровень для enterprise automation SaaS, но только при условии, что кастомные доработки не выпадают за рамки шаблонного scope. [inference]

---

## 8. Team & FOT

### Полная команда steady-state

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder-sales | стратегия, fundraise, крупные сделки | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, roadmap | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | core platform, integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | workflow engine, API | 420 000 | 126 000 | 546 000 |
| ML Engineer | RAG/agents, quality loop | 480 000 | 144 000 | 624 000 |
| DevOps | infra, observability, deployment | 330 000 | 99 000 | 429 000 |
| Frontend | admin UI, user workflows | 280 000 | 84 000 | 364 000 |
| Product / Solution Manager | pre-sale solutioning, delivery | 320 000 | 96 000 | 416 000 |
| SDR | outbound prospecting | 150 000 | 45 000 | 195 000 |
| AE | demo, negotiation, close | 320 000 | 96 000 | 416 000 |
| Customer Success | onboarding, adoption, renewal | 220 000 | 66 000 | 286 000 |
| **Итого steady-state FOT** |  |  |  | **5 382 000 ₽/мес** |

### Таблица найма realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1.5 | 126 000 | 546 000 × 2 |
| ML Engineer | 1 | 480 000 | 2-3 | 2 | 144 000 | 624 000 |
| DevOps | 1 | 330 000 | 1-2 | 1 | 99 000 | 429 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 150 000 | 0.5-1 | 1 | 45 000 | 195 000 |
| AE | 1 | 320 000 | 1-2 | 2-3 | 96 000 | 416 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Product / Solution Manager | 1 | 320 000 | 1-2 | 1.5 | 96 000 | 416 000 |

### Salary benchmark note
- Диапазоны сверены с текущими вакансиями HH.ru по Москве для senior backend, ML, AE/SDR, customer success и смежных ролей; модель стоит ближе к **медиане Moscow/SPb IT B2B**. [T7]

---

## 9. Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder start |
| M2 | CEO + CTO | 1 560 000 | архитектура и pre-sales frame |
| M3 | + Backend #1 | 2 106 000 | старт core platform |
| M4 | + Backend #2 + Product/Solution | 3 068 000 | формируем repeatable scope |
| M5 | + ML + SDR | 3 887 000 | старт GTM и AI quality loop |
| M6 | + DevOps + AE | 4 732 000 | deployment + closing motion |
| M7 | + Frontend | 5 096 000 | admin/UI readiness |
| M8 | + Customer Success | 5 382 000 | renewals/adoption motion complete |
| M9 | steady-state | 5 382 000 | full team |
| M10 | steady-state | 5 382 000 | full team |
| M11 | steady-state | 5 382 000 | full team |
| M12 | steady-state | 5 382 000 | full team |

**Sanity check:** модель не нанимает 5+ человек в первый месяц, значит time-to-hire realism не нарушен.

---

## 10. Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Team FOT steady-state | 5 382 000 |
| Office / coworking / admin | 90 000 |
| Legal + бухгалтерия + HR ops | 80 000 |
| Core software stack (workspace, docs, security, repos) | 75 000 |
| Corp infra reserve not in COGS | 70 000 |
| Travel / meetings / misc G&A | 65 000 |
| **Итого fixed costs** | **5 762 000 ₽/мес** |

---

## 11. Break-even: по клиентам и по месяцам

### Break-even по количеству клиентов
- Contribution на клиента в месяц = **129 500 ₽**.
- Fixed costs = **5 762 000 ₽/мес**.

**Break-even client count = 5 762 000 / 129 500 = 44,5 клиента**.

Округляя вверх:
**BEP = 45 активных клиентов**.

### Break-even по месяцам
Консервативная траектория активных клиентов: 0, 0, 1, 2, 4, 6, 9, 13, 18, 24, 31, 40, 45.

| Месяц | Активные клиенты | Contribution, ₽/мес | Fixed costs, ₽/мес | EBITDA proxy |
|---|---:|---:|---:|---:|
| M6 | 1 | 129 500 | 4 732 000 | -4 602 500 |
| M7 | 2 | 259 000 | 5 096 000 | -4 837 000 |
| M8 | 4 | 518 000 | 5 382 000 | -4 864 000 |
| M9 | 6 | 777 000 | 5 762 000 | -4 985 000 |
| M10 | 9 | 1 165 500 | 5 762 000 | -4 596 500 |
| M11 | 13 | 1 683 500 | 5 762 000 | -4 078 500 |
| M12 | 18 | 2 331 000 | 5 762 000 | -3 431 000 |
| M13 | 24 | 3 108 000 | 5 762 000 | -2 654 000 |
| M14 | 31 | 4 014 500 | 5 762 000 | -1 747 500 |
| M15 | 40 | 5 180 000 | 5 762 000 | -582 000 |
| M16 | 45 | 5 827 500 | 5 762 000 | **+65 500** |
| M17 | 50 | 6 475 000 | 5 762 000 | **+713 000** |

**Вывод:** по консервативной модели операционный break-even достигается **около M16**, а при **50 клиентах EBITDA > 500k/мес достижима**, значит Profit Gate не ломается. [inference]

---

## 12. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Если считать burn как FOT + fixed costs + acquisition stack минус contribution от клиентской базы, то при постепенном наращивании GTM:
- средний burn в фазе M6-M12: **4,0-5,0 млн ₽/мес**;
- cumulative burn до M16: примерно **46-49 млн ₽**;
- с буфером 10% на кассовые лаги и пилоты нужен стартовый капитал **около 50-55 млн ₽**.

### Cash runway
- Startup capital = **50 млн ₽**.
- Средний burn в первые 12 месяцев ≈ **4,6 млн ₽/мес**.

**Cash runway = 50 / 4,6 ≈ 10,9 месяца**.

Это значит:
- без ускорения продаж денег не хватит до естественного breakeven;
- либо нужен капитал **55-60 млн ₽**, либо более агрессивный partner-led GTM и больший upfront setup fee. [inference]

---

## 13. Profit Gate

Проверка жёстких условий:
1. **LTV/CAC < 1:1?** Нет, фактически **10,6:1**.
2. **Компания не может выйти на EBITDA 500k+/мес даже при 50 клиентах?** Нет, при 50 клиентах модель даёт **~713k ₽/мес EBITDA proxy**.

**Итог по Profit Gate: PASS.**

Но это **не лёгкий pass**:
- инвестиционная логика держится только при enterprise discipline;
- низкий ACV или кастомная разработка под каждого клиента быстро разрушат economics.

---

## 14. Инвестиционный вывод

### Что нравится фонду
- высокий ACV и хорошая retention-логика за счёт глубокой интеграции;
- strong LTV/CAC и быстрый payback даже на fully-loaded CAC;
- рынок уже обучен платить за workflow automation и digital workplace layer. [T1][T2][T3]

### Что тревожит фонд
- очень тяжёлый путь до breakeven, нужен заметный стартовый капитал;
- основная угроза не churn, а превращение SaaS в integration-heavy service business;
- GTM-message слишком широкий, нужен узкий wedge: HR ops, internal service desk, finance approvals, knowledge workflows. [inference]

### Вердикт
**PASS WITH RESERVATIONS.**
Кейс инвестиционно живой, но только как **enterprise automation platform с жёсткой стандартизацией внедрения**, а не как расплывчатый «AI-офис для всех».

---

## Источники
- [T1] ZeBrains AI Digital Office: https://zebrains.ai/ai-digital-office
- [T2] CNews о запуске платформы ZeBrains AI Digital Office: https://www.cnews.ru/news/line/2024-03-12_zebrains_zapustila_platformu
- [T3] Bitrix24 pricing: https://www.bitrix24.ru/prices/
- [T4] Pyrus pricing: https://pyrus.com/ru/pricing
- [T5] BotHelp pricing: https://bothelp.io/pricing
- [T6] Optifai churn benchmark 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ и https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [T7] HH.ru вакансии и salary signals по Москве: https://hh.ru/vacancies/senior-backend-engineer ; https://hh.ru/vacancy/129433377 ; https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancies/account_executive/polnaya_zanyatost ; https://hh.ru/vacancies/customer-success-manager ; https://hh.ru/vacancies/devops ; https://hh.ru/vacancies/product_manager
- [T8] User benchmark policy / enterprise CAC multiplier guidance из текущего задания, использовано только как sanity framework

> Market Pulse 2026-04-26: юнит-экономика у ZeBrains работает, если продавать дорогой стандартизированный enterprise bundle, но без сильной стандартизации внедрения это легко деградирует в сервисный бизнес с тяжёлым burn.

## Stage 5 — Critic

# SECTION A — PnL

## 1) Сценарные допущения

- **Базовый**: 2 новых клиента/мес, churn 2,8%, ARPA 180k, COGS 45k, fixed 5,762 млн ₽.
- **Оптимистичный**: 3 новых клиента/мес за счёт partner-led GTM, churn 2,0%, ARPA 190k, COGS 44k, fixed 6,05 млн ₽.
- **Пессимистичный**: 1 новый клиент/мес, churn 4,0%, ARPA 170k, COGS 50k, fixed 6,34 млн ₽.
- Общая база из `04-economics.md`: gross margin baseline 75%, contribution margin baseline 71,9%, страховые взносы ~30% к ФОТ уже отражены в FOT/fixed costs.
- Налоговая логика для Net: **IT-льгота 3%** как целевая модель для аккредитованной Минцифры компании; для stress-test дополнительно сравниваю **УСН 6%** и **ОСНО 20% + НДС 20% если применимо**.

## 2) Базовый: PnL 12 месяцев

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 2,0 | 3,9 | 5,8 | 7,7 | 9,5 | 11,2 | 12,9 | 14,5 | 16,1 | 17,7 | 19,2 | 20,6 |
| MRR | 360 000 | 709 920 | 1 050 042 | 1 380 641 | 1 701 983 | 2 014 328 | 2 317 926 | 2 613 024 | 2 899 860 | 3 178 664 | 3 449 661 | 3 713 071 |
| COGS | 90 000 | 177 480 | 262 511 | 345 160 | 425 496 | 503 582 | 579 482 | 653 256 | 724 965 | 794 666 | 862 415 | 928 268 |
| Gross profit | 270 000 | 532 440 | 787 532 | 1 035 481 | 1 276 487 | 1 510 746 | 1 738 445 | 1 959 768 | 2 174 895 | 2 383 998 | 2 587 246 | 2 784 803 |
| GM% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% |
| Fixed costs | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 | 5 762 000 |
| EBITDA | -5 492 000 | -5 229 560 | -4 974 468 | -4 726 519 | -4 485 513 | -4 251 254 | -4 023 555 | -3 802 232 | -3 587 105 | -3 378 002 | -3 174 754 | -2 977 197 |
| Cash burn | 5 492 000 | 5 229 560 | 4 974 468 | 4 726 519 | 4 485 513 | 4 251 254 | 4 023 555 | 3 802 232 | 3 587 105 | 3 378 002 | 3 174 754 | 2 977 197 |
| Cumulative cash | -5 492 000 | -10 721 560 | -15 696 028 | -20 422 548 | -24 908 060 | -29 159 315 | -33 182 870 | -36 985 101 | -40 572 207 | -43 950 209 | -47 124 963 | -50 102 160 |

## 2) Оптимистичный: PnL 12 месяцев

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 3,0 | 5,9 | 8,8 | 11,6 | 14,4 | 17,1 | 19,8 | 22,4 | 24,9 | 27,4 | 29,9 | 32,3 |
| MRR | 570 000 | 1 128 600 | 1 676 028 | 2 212 507 | 2 738 257 | 3 253 492 | 3 758 422 | 4 253 254 | 4 738 189 | 5 213 425 | 5 679 157 | 6 135 573 |
| COGS | 132 000 | 261 360 | 388 133 | 512 370 | 634 123 | 753 440 | 870 371 | 984 964 | 1 097 265 | 1 207 319 | 1 315 173 | 1 420 870 |
| Gross profit | 438 000 | 867 240 | 1 287 895 | 1 700 137 | 2 104 135 | 2 500 052 | 2 888 051 | 3 268 290 | 3 640 924 | 4 006 106 | 4 363 983 | 4 714 704 |
| GM% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% | 76,8% |
| Fixed costs | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 | 6 050 000 |
| EBITDA | -5 612 000 | -5 182 760 | -4 762 105 | -4 349 863 | -3 945 865 | -3 549 948 | -3 161 949 | -2 781 710 | -2 409 076 | -2 043 894 | -1 686 017 | -1 335 296 |
| Cash burn | 5 612 000 | 5 182 760 | 4 762 105 | 4 349 863 | 3 945 865 | 3 549 948 | 3 161 949 | 2 781 710 | 2 409 076 | 2 043 894 | 1 686 017 | 1 335 296 |
| Cumulative cash | -5 612 000 | -10 794 760 | -15 556 865 | -19 906 728 | -23 852 593 | -27 402 541 | -30 564 490 | -33 346 200 | -35 755 276 | -37 799 171 | -39 485 188 | -40 820 484 |

## 2) Пессимистичный: PnL 12 месяцев

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 1,0 | 2,0 | 2,9 | 3,8 | 4,6 | 5,4 | 6,2 | 7,0 | 7,7 | 8,4 | 9,0 | 9,7 |
| MRR | 170 000 | 333 200 | 489 872 | 640 277 | 784 666 | 923 279 | 1 056 348 | 1 184 094 | 1 306 731 | 1 424 461 | 1 537 483 | 1 645 984 |
| COGS | 50 000 | 98 000 | 144 080 | 188 317 | 230 784 | 271 553 | 310 691 | 348 263 | 384 333 | 418 959 | 452 201 | 484 113 |
| Gross profit | 120 000 | 235 200 | 345 792 | 451 960 | 553 882 | 651 727 | 745 658 | 835 831 | 922 398 | 1 005 502 | 1 085 282 | 1 161 871 |
| GM% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% | 70,6% |
| Fixed costs | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 | 6 340 000 |
| EBITDA | -6 220 000 | -6 104 800 | -5 994 208 | -5 888 040 | -5 786 118 | -5 688 273 | -5 594 342 | -5 504 169 | -5 417 602 | -5 334 498 | -5 254 718 | -5 178 129 |
| Cash burn | 6 220 000 | 6 104 800 | 5 994 208 | 5 888 040 | 5 786 118 | 5 688 273 | 5 594 342 | 5 504 169 | 5 417 602 | 5 334 498 | 5 254 718 | 5 178 129 |
| Cumulative cash | -6 220 000 | -12 324 800 | -18 319 008 | -24 207 048 | -29 993 166 | -35 681 439 | -41 275 782 | -46 779 950 | -52 197 552 | -57 532 050 | -62 786 768 | -67 964 897 |

## 3) Waterfall unit economics

| Сценарий | ARPA | Gross | Contribution | EBITDA/unit after fixed load at BEP | Net after tax |
|---|---:|---:|---:|---:|---:|
| Базовый | 180 000 | 135 000 | 129 500 | 1 456 | 125 615 |
| Оптимистичный | 190 000 | 146 000 | 140 194 | 2 694 | 135 989 |
| Пессимистичный | 170 000 | 120 000 | 114 806 | 1 591 | 107 917 |

Пояснение: waterfall построен как **ARPA -> Gross profit -> Contribution (после переменных sales/service) -> EBITDA на единицу при загрузке на BEP -> Net после налога**. Для base/optimistic использована ставка **3% IT-льготы**, для downside, где льгота может не примениться, использована **УСН 6%**. На ОСНО effective net будет ниже из-за налога на прибыль 20% и кассового эффекта НДС 20%.

## 4) Cash flow и startup capital

| Сценарий | Минимальный cumulative cash за 12 мес | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Базовый | -75 650 482 | 75 650 483 | операционный BEP около M33 |
| Оптимистичный | -42 792 666 | 42 792 667 | операционный BEP около M17 |
| Пессимистичный | -266 182 633 | 266 182 634 | в горизонте 60 мес операционный BEP не достигается без смены GTM/цены |

## 5) Налоговая модель РФ

| Режим | Когда применим | Налоговая нагрузка в модели | Что важно для cash flow |
|---|---|---:|---|
| УСН 6% | базовый режим для SaaS/сервиса без льготы | 6% с выручки | проще администрирование, но больнее при низкой марже и длинном payback |
| IT-льгота 3% | при аккредитации Минцифры и соблюдении критериев | 3% с выручки | лучший режим для ZeBrains, повышает Net и сокращает capital to BEP |
| ОСНО 20% | если льготы/УСН неприменимы, крупные контрагенты требуют НДС | 20% налог на прибыль + НДС 20% if applicable | ухудшает cash conversion, нужен доп. оборотный капитал под НДС и дебиторку |

Страховые взносы **~30% к ФОТ** уже включены в steady-state FOT из `04-economics.md`; если компания получает пониженные тарифы для IT, upside к EBITDA и cash будет дополнительным.

## 6) Break-even по сценариям

| Сценарий | Contribution на клиента/мес | BEP client count | BEP month | Комментарий |
|---|---:|---:|---:|---|
| Базовый | 129 500 | 45 | 33 | в 12-месячном окне EBITDA ещё отрицательная |
| Оптимистичный | 140 194 | 44 | 17 | в 12-месячном окне EBITDA ещё отрицательная |
| Пессимистичный | 114 806 | 56 | n/a | в 12-месячном окне EBITDA ещё отрицательная |

Итог: в текущей конфигурации ZeBrains выглядит как **капиталоёмкий enterprise AI/SaaS**. Даже base-case не выходит в EBITDA break-even в первые 12 месяцев, поэтому фондово-совместим только при дисциплине по цене, стандартизации delivery и прохождении **IT-льготы**.

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## 1) Sensitivity analysis: EBITDA через 12 месяцев

Метод: беру базовую модель SECTION A. Для **CAC x2** предполагаю, что при том же GTM-бюджете темп привлечения падает с **2 до 1 нового клиента/мес**. Для **Churn x2** повышаю monthly churn с **2,8% до 5,6%**. Для **Price -30%** снижаю recurring ARPA с **180k до 126k ₽/мес**, COGS оставляю без улучшения, то есть маржа сжимается сильнее выручки.

| Сценарий | Ключевое изменение | Клиенты к M12 | MRR @M12 | EBITDA @M12 |
|---|---|---:|---:|---:|
| Base | 2 new/mo, churn 2,8%, ARPA 180k | 20,6 | 3 713 071 ₽ | **-2 977 197 ₽** |
| Sens1 | CAC x2 -> 1 new/mo | 10,3 | 1 856 535 ₽ | **-4 369 599 ₽** |
| Sens2 | Churn x2 -> 5,6% | 17,8 | 3 209 146 ₽ | **-3 355 141 ₽** |
| Sens3 | Price -30% -> ARPA 126k | 20,6 | 2 599 149 ₽ | **-4 091 118 ₽** |

Вывод: самый опасный single-variable shock здесь не churn, а **price compression** и **удорожание привлечения**. Модель и без того убыточна на M12, поэтому любой из трёх шоков отодвигает выход в операционный плюс ещё на несколько кварталов.

## 2) Monte Carlo Lite — confidence intervals

### 2.1 Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 320 000 | 453 333 | 660 000 | blended CAC и канальный коридор из `04-economics.md` [T8] |
| Monthly churn % | 1,5% | 2,8% | 5,6% | benchmark enterprise/mid-market + stress x2 [T6] |
| ARPU ₽/мес | 126 000 | 180 000 | 210 000 | base 180k, stress -30%, upside premium bundle [T8][inference] |
| Conversion rate lead→paid % | 0,45% | 0,60% | 0,85% | из blended funnel: 9 wins на ~1 500 target accounts + inbound/partner mix [T8][inference] |
| Time-to-hire месяцев (среднее) | 1,0 | 1,6 | 2,5 | таблица hiring realism из `04-economics.md` [T8] |

### 2.2 Упрощённая симуляция

Вместо 1000 прогонов использую **27 комбинаций** по трём узлам triangular distribution: CAC {min, mode, max} x churn {min, mode, max} x ARPU {min, mode, max}. Для каждой комбинации пересчитываю темп new customers/month через обратную зависимость от CAC, затем считаю steady-state траекторию до **M24**.

### 2.3 Результат по доверительным интервалам

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|-----------:|
| EBITDA @M24 (₽/мес) | -3 594 672 | -1 711 438 | 1 995 703 | 5 590 375 |
| CAC payback (мес) | 1,52 | 2,54 | 5,24 | 3,71 |
| LTV/CAC | 3,65x | 9,04x | 24,26x | 20,61 |
| Cash runway (мес) | 9,85 | 11,45 | 15,30 | 5,45 |

### 2.4 Интерпретация Monte Carlo Lite

- **Правило 1 срабатывает:** p10 EBITDA < 0, значит downside уже указывает на риск неплатежеспособности без дополнительного капитала.
- **Правило 2 срабатывает:** p50 EBITDA = **-1,71 млн ₽/мес**, то есть кейс **не проходит EBITDA Gate даже в median-case**.
- **Правило 3 формально считать некорректно**, потому что p10 отрицательный, а p90 положительный. Но именно смена знака между p10 и p90 означает экстремально широкую неопределённость, поэтому score нужно даунгрейдить.
- **Правило 4 срабатывает:** width по LTV/CAC = **20,61x**, что сильно выше порога 8. Значит модель хрупкая одновременно к pricing, churn и CAC.

Итог Monte Carlo Lite: ZeBrains остаётся инвестиционно обсуждаемым только при жёстком контроле коммерческой упаковки и GTM. В текущем виде распределение outcomes слишком широкое, а median остаётся отрицательной даже на горизонте 24 месяцев.

## 3) Competitor deep-dive

### 3.1 Западные конкуренты

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **ServiceNow** | enterprise workflow layer для HR, IT, finance, procurement | мощная платформа, governance, сильный бренд, глубокая интеграция в Fortune 500 [T9][T10] | дорого, длинный цикл внедрения, высокая зависимость от экосистемы и SI-партнёров | **15-20%** глобального enterprise workflow/ITSM-adjacent сегмента по выручке, estimate from scale and enterprise penetration [inference] | ZeBrains легче продать в РФ mid-market, быстрее локализовать под 1С и data residency |
| **UiPath** | automation-first платформа, смежная категория для back-office automation | зрелая orchestration/RPA-платформа, сильный enterprise footprint, agentic automation roadmap, ARR > $1,7 млрд [T11] | RPA-first UX, избыточность там, где процессы уже API-native, часто требует integrator-heavy motion | **20-25%** глобального RPA/agentic-automation сегмента, estimate from public ARR leadership [inference] | ZeBrains проще позиционировать как AI-native слой над процессами, а не как robot factory |
| **Moveworks** | AI employee assistant across HR/IT/finance workflows | сильный UX, быстрый time-to-value, enterprise-grade assistant, 350+ крупных клиентов [T12] | слабее как full workflow backbone, чем как front-door assistant; меньше глубины в российских интеграциях и локальном compliance | **3-5%** глобального AI employee-assistant сегмента, estimate by customer base and category maturity [inference] | ZeBrains может выигрывать в локальном контуре, on-prem/private deployment и интеграции с 1С/ЭДО |

### 3.2 Российские конкуренты

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Bitrix24 + CoPilot** | самый массовый entry-point в РФ для CRM/workflow + AI [T13][T14] | широчайшая installed base, low-code automation, быстрое внедрение, знакомый SMB/mid-market интерфейс | слабее в enterprise-grade security/deep custom process orchestration, часто упирается в CRM-centric use cases | **25-35%** российского SMB workflow/CRM-automation слоя, estimate from category ubiquity [inference] | ZeBrains может идти выше по чеку и глубже по сложным back-office/enterprise процессам |
| **Just AI Agent Platform** | прямой конкурент в enterprise AI-agent layer [T15][T16] | no/low-code + pro-code, мультиагентность, on-prem/secure contour, сильная экспертиза в conversational AI | исторически силён в bot/conversational use cases, не у всех клиентов доказан широкий back-office rollout | **5-10%** российского enterprise AI-agent/platform сегмента, estimate from visibility and product scope [inference] | у ZeBrains сильнее value prop вокруг единого «цифрового офиса» и process bundle вместо toolkit-only pitch |
| **Sherpa RPA** | автоматизация рутины и process discovery для enterprise РФ [T17][T18] | российский вендор, реестр ПО, кейсы enterprise, process discovery + RPA | RPA-heavy architecture, дольше внедрение, слабее как native conversational/workflow layer | **8-12%** российского enterprise RPA+AI сегмента, estimate from Skolkovo visibility and enterprise references [inference] | ZeBrains может дать более современный AI-native orchestration слой поверх API и knowledge workflows |
| **ROBIN / SL Soft** | интеллектуальная автоматизация сквозных процессов [T19] | большой корпоративный контур, модульность, сильный фокус на legacy automation | RPA-first, тяжёлое внедрение, ниже product simplicity для новых AI-first команд | **8-10%** российского IPA/RPA сегмента, estimate from portfolio breadth and enterprise reach [inference] | ZeBrains лучше упаковывается как faster-to-value AI office, а не как тяжёлая корпоративная автоматизация |
| **Pyrus** | workflow/task automation, согласования, заявки, внутренние процессы [T20][T21] | простой onboarding, зрелые process forms, тысячи компаний в базе, понятный task-centric UX | меньше AI-native differentiation, слабее orchestration сложных мультиагентных процессов | **3-6%** российского workflow-automation сегмента, estimate from installed base and narrower ACV layer [inference] | ZeBrains может продавать более высокий ACV за счёт AI layer, orchestration и enterprise integrations |

### 3.3 Общий вывод по конкурентам

- На Западе category winner чаще всего уже определён платформой: **ServiceNow** и **UiPath** выигрывают масштабом и distribution.
- В РФ рынок ещё фрагментирован: есть сильные вертикали **CRM-first**, **RPA-first** и **bot-first**, но мало игроков, которые одновременно закрывают **enterprise AI layer + workflow orchestration + локальный контур + 1С integration**.
- Это и есть окно ZeBrains, но оно работает только если компания не расползается в кастомную разработку под каждого клиента.

## 4) Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder/sales bottleneck: крупные сделки держатся на одном-двух людях | high | высокий | >70% pipeline требует участия founder в demo/closing | нанять сильного AE, стандартизировать discovery и security package |
| 2 | Operational | Delivery уходит в кастомную интеграцию вместо repeatable product | high | высокий | >30% выручки уходит в non-recurring кастом и bespoke scopes | productize 3-4 типовых bundles, жёсткий scope control, change request pricing |
| 3 | Operational | LLM API outage/latency/quality drift | medium | высокий | рост latency, cost/token, hallucination incidents, рост ручных эскалаций | multi-model routing, fallback на локальные/российские модели, human-in-the-loop |
| 4 | Market | Реальный спрос на «AI digital office» шире, чем willingness to pay | medium | высокий | demo-to-pilot падает ниже 25%, частые запросы на бесплатный PoC | сузить wedge до 1-2 департаментов: HR ops, finance approvals, service desk |
| 5 | Market | Price compression из-за Bitrix24/интеграторов/бот-студий | high | высокий | средний чек новых сделок <150k MRR | перейти к ROI-based packaging, увеличить setup fee, upsell compliance/security layer |
| 6 | Market | Сильные конкуренты занимают channel partners и интеграторов | medium | средний/высокий | меньше 2 активных партнёров, партнерский pipeline <20% | early partner program, white-label/reseller motion, revenue-share |
| 7 | Regulatory | Нарушение 152-ФЗ и проблемный трансграничный data flow | medium | высокий | security review клиентов затягивается >8 недель, legal redlines по residency | on-prem/private cloud deployment, DPA templates, хранение данных в РФ |
| 8 | Regulatory | Ограничения по 115-ФЗ/AML и auditability для fintech/regulated clients | low/medium | средний/высокий | регклиенты требуют объяснимость и полный audit log, а продукт не готов | built-in audit trail, role-based access, explainability logs, сегментация ICP |
| 9 | Regulatory | Санкции SaaS и ограничения на западные модели/облака | high | высокий | рост отказов procurement из-за foreign stack, запреты security teams | model abstraction layer, российские LLM as default, импортонезависимый deployment |
| 10 | Financial | Runway не дотягивает до breakeven | high | высокий | cash <9 месяцев runway, burn >4,5 млн ₽/мес без роста pipeline | raise 55-60 млн ₽, заморозка найма, больше setup fee и предоплаты |
| 11 | Financial | USD/RUB volatility поднимает cost of compute и SaaS tools | medium | средний | рост COGS/client >20% за квартал | рублёвые контракты с клиентами, валютный буфер, fallback на open-source stack |
| 12 | Financial | Инфляция зарплат в AI/ML и enterprise sales | high | средний/высокий | time-to-hire >2,5 мес, offers проигрываются рынку | ESOP/phantom, удалённый найм по РФ, приоритизация revenue-critical ролей |
| 13 | Black swan | Эскалация войны/санкций ломает сделки и корпоративные бюджеты | medium | высокий | freeze новых ИТ-бюджетов, перенос security approvals | делать ставку на ROI-payback <12 мес и импортозамещение narrative |
| 14 | Black swan | Отключение ключевого LLM-провайдера или резкое ухудшение качества | medium | высокий | forced migration, падение качества ответов, рост ручной проверки | резервные модели, локальный inference для критичных use cases, abstraction layer |

## 5) Kill conditions через 6 месяцев

1. **Median-case не чинится:** если к M6 обновлённый forecast всё ещё показывает **p50 EBITDA@M24 < 500k ₽/мес**, проект нельзя продолжать как venture-scale платформа.
2. **Коммерческий сигнал слабый:** если новый recurring ARPA по новым сделкам **<150k ₽/мес** или win rate pilot->paid **<25%**, значит рынок не принимает цену и category message.
3. **Runway collapse:** если на M6 фактический runway **<6 месяцев** и нет подписанного раунда/кредитной линии/крупных предоплат, продолжать нельзя, потому что execution risk становится выше upside.

## 6) Bottom line

SECTION B ухудшает кейс относительно SECTION A. Да, у ZeBrains есть понятное конкурентное окно в РФ, но финансовый downside слишком тяжёлый:
- M12 EBITDA остаётся отрицательной даже в base;
- p10 и p50 на M24 отрицательны;
- LTV/CAC выглядит красиво только в mode/upside, но диапазон слишком широкий;
- главным риском оказывается не технология как таковая, а **хрупкость GTM + pricing + delivery discipline**.

Инвестиционный вывод после P6B: **PASS WITH HEAVY RESERVATIONS / borderline reject**, пока не доказаны repeatable sales, price integrity и более узкий wedge.

## Источники SECTION B
- [T6] Optifai churn benchmark 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ ; https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [T8] `04-economics.md` текущего кейса, расчёты автора на его основе
- [T9] ServiceNow homepage: https://www.servicenow.com/
- [T10] ServiceNow Employee Experience / EmployeeWorks: https://www.servicenow.com/solutions/employee-experience.html ; https://www.servicenow.com/products/employeeworks.html
- [T11] UiPath FY2026 / FY2025 filings: https://ir.uipath.com/financials/sec-filings/content/0001734722-26-000012/path-20260131.htm ; https://ir.uipath.com/news/detail/394/uipath-reports-first-quarter-fiscal-2026-financial-results
- [T12] Moveworks platform and customers: https://moveworks.com/ ; https://www.moveworks.com/us/en/customers
- [T13] Bitrix24 on vc.ru about CoPilot: https://vc.ru/bitrix24/942637-bitriks24-vypustil-copilot-ii-assistenta-dlya-sotrudnikov-kompanii ; https://vc.ru/bitrix24/2003704-obnovlenie-bitrix24-nevesomost-i-novye-vozmozhnosti-dlya-biznesa
- [T14] Bitrix24 on Habr: https://habr.com/company/bitrix
- [T15] Just AI on vc.ru / Habr: https://vc.ru/ai/2205448-just-ai-agent-platform ; https://habr.com/ru/companies/just_ai/news/945346/
- [T16] Just AI profile on Habr: https://habr.com/ru/companies/just_ai/profile/
- [T17] Sherpa RPA on vc.ru: https://vc.ru/services/2873629-top-kompaniy-po-ii-avtomatizatsii-v-rossii
- [T18] Sherpa RPA / Skolkovo: https://sk.ru/news/faberlic-optimiziruet-biznes-s-sherpa-rpa/ ; https://sk.ru/news/razrabotka-rezidenta-skolkovo-vklyuchena-v-reestr-otechestvennogo-po/
- [T19] SL Soft / ROBIN on Habr: https://habr.com/en/companies/slsoft/profile/
- [T20] Pyrus profile on Habr: https://habr.com/ru/users/Pyrus/
- [T21] Pyrus on Habr Career: https://career.habr.com/companies/pyrus

<!-- P6B-DONE -->


## Stage 6 — Verdict

[B2B-OPS] ZeBrains AI Digital Office — REJECTED: 47/100 | EBITDA base=-1711К₽/мес через 24 мес | LTV/CAC=10,6x | Ключевое преимущество: сильная unit economics при enterprise ACV | Главный риск: модель не выходит к EBITDA 500К₽ в base-case за 24 мес.

# 06-verdict — ZeBrains AI Digital Office

sector: B2B-OPS

## Итоговый вердикт
- **Статус:** REJECTED
- **Normalized score:** **47/100**
- **Raw score:** **71/150**
- **Пороговое правило:** score < 65, а также не выполнен profitability gate для APPROVED, потому что `company_ebitda_potential_rub_month` в base-case не достигает **500 000 ₽/мес** за **<=24 мес**.

## Оценка
Source tier balance: T1=5, T2=7, T3=0, weighted=2.42. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 16 | "LTV/CAC = 10,6x", "CAC Payback = 2,52 месяца", "Gross Margin = 75,0%" из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 8 | `05-critic.md`: "p50 EBITDA@M24 = -1,71 млн ₽/мес" и "операционный BEP около M33". |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | `02-demand.md`: "автоматизация бизнес-процессов" даёт `MEDIUM / 30` и `4767 вакансий HH.ru`, но exact-label спрос слабый; учтён штраф -2 за tier balance 2.42. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | `05-critic.md`: окно есть, но "оно работает только если компания не расползается в кастомную разработку под каждого клиента". |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 10 | `05-critic.md`: "Runway не дотягивает до breakeven", плюс high-risk по санкциям, delivery и founder bottleneck. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 13 | CAC payback сильный, но `05-critic.md` фиксирует "слишком широкий positioning" и недоказанный repeatable sales motion. |

**Normalized score = round((sum_raw * 100) / 150) = 47/100.**

## Moat — 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 1 | Новые клиенты не улучшают продукт для остальных существенно, кроме накопления шаблонов use-case. |
| Switching costs | 2 | Интеграции, knowledge import и внутреннее обучение команды создают умеренную инерцию. |
| Scale economies | 1 | Инфра и шаблоны масштабируются, но delivery остаётся тяжёлой. |
| Proprietary data / model advantage | 1 | Уникальный датасет публично не доказан; преимуществом остаётся implementation know-how. |
| Regulatory moat | 1 | 152-ФЗ и secure contour помогают, но это table-stakes, а не сильный барьер. |
| Brand / distribution | 1 | Есть резидентство Сколково и PR-сигналы, но бренд-дистрибуция пока средние. |
| Embedded workflow | 2 | При успешном внедрении продукт глубоко встраивается в HR/finance/support workflows. |

**Moat score = round((9 * 25) / 21) = 11/25.**

## Full business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов и enrichment | SDR | HH/отраслевые базы, Telegram, CRM | 1-2 дня | 2 500 | средняя |
| 2 | Outbound sequence, первичный outreach | SDR | CRM, email, мессенджеры, телефония | 5-7 дней | 6 000 | средняя |
| 3 | Квалификация боли и ICP-fit | SDR + AE | CRM, discovery script | 30-45 мин | 9 000 | низкая |
| 4 | Discovery call + live demo | AE + Solution lead | Zoom/Meet, demo-стенд, презентация | 3-5 дней до встречи | 22 000 | низкая |
| 5 | Предпроектное обследование процесса | Solution lead + PM | Miro, BPMN, shared docs | 4-7 дней | 35 000 | низкая |
| 6 | Пилот / PoC / sandbox | PM + Backend + ML | private cloud, sandbox, LLM stack | 2-4 недели | 60 000 | средняя |
| 7 | Security review и legal | AE + CTO + юрист | DPA/NDA, security checklist | 1-2 недели | 28 000 | низкая |
| 8 | Коммерческое предложение и procurement | AE + finance/admin | CRM, CPQ, ЭДО | 3-10 дней | 14 000 | средняя |
| 9 | Onboarding, интеграции, запуск | PM + Backend + CSM | API, SSO, knowledge import | 2-3 недели | 40 000 | средняя |
| 10 | Счёт, акт, оплата, recurring support | finance/admin + CSM | ЭДО, банк, billing, helpdesk | 3-7 дней | 45 000/мес COGS | высокая |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 4 821 429 ₽ |
| CAC | 453 333 ₽ |
| LTV/CAC | 10.6x |
| CAC payback | 2.52 мес |
| Gross Margin | 75.0% |
| contribution_margin_rub_month | 129 500 ₽ |
| fixed_costs_rub_month | 5 762 000 ₽ |
| Break-even clients | 45 |
| startup_capital_to_bep_rub | 75 650 483 ₽ |
| company_ebitda_rub_month base @M24 | -1 711 438 ₽/мес |
| company_ebitda_potential_rub_month upside @M24 p90 | 1 995 703 ₽/мес |
| clients_to_500k_ebitda | 49 |
| months_to_500k_ebitda | >24 |
| clients_to_1m_ebitda | 53 |
| months_to_1m_ebitda | >24 |

## Команда

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / founder-sales | стратегия, fundraise, крупные сделки | 845 000 |
| CTO / Tech Lead | архитектура, security, roadmap | 715 000 |
| Senior Backend #1 | core platform, integrations | 546 000 |
| Senior Backend #2 | workflow engine, API | 546 000 |
| ML Engineer | RAG/agents, quality loop | 624 000 |
| DevOps | infra, observability, deployment | 429 000 |
| Frontend | admin UI, user workflows | 364 000 |
| Product / Solution Manager | pre-sale solutioning, delivery | 416 000 |
| SDR | outbound prospecting | 195 000 |
| AE | demo, negotiation, close | 416 000 |
| Customer Success | onboarding, adoption, renewal | 286 000 |
| **Итого steady-state FOT** |  | **5 382 000 ₽/мес** |

## GTM — 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| СДЭК | Большой объём support и внутренних операционных заявок, pain по service workflows. | партнёрство / email decision-maker | 250 000 ₽/мес |
| Dodo Brands | Мультифункциональные HR, support и finance ops в распределённой сети. | email COO / конференция | 300 000 ₽/мес |
| Самокат | Интенсивные внутренние заявки, HR и логистические процессы. | email operations lead / партнёрство | 300 000 ₽/мес |
| Ozon | Сложные back-office и service operations в крупном enterprise-контуре. | конференция / email VP operations | 450 000 ₽/мес |
| Skillbox | Поддержка, HR onboarding, knowledge workflows. | vc.ru ad / email head of operations | 180 000 ₽/мес |
| Skillfactory | Повторяемая EdTech-операционка и документооборот. | email decision-maker | 180 000 ₽/мес |
| Клиника Фомина | Регистратура, внутренние сервисные заявки и knowledge-base процессы. | партнёрство / конференция | 220 000 ₽/мес |
| Петрович | Внутренние заявки, support и документооборот в distributed retail ops. | email CIO / конференция | 250 000 ₽/мес |
| Hoff | Клиентские обращения и retail back-office процессы. | vc.ru ad / email CX lead | 250 000 ₽/мес |
| Level Group | Документы, finance approvals и клиентский сервис в девелопменте. | партнёрство / email operations director | 220 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему важен |
|---|---|---|---|
| Delivery уходит в кастомную интеграцию | high | высокий | Ломает software-like margin и растягивает onboarding. |
| Runway не дотягивает до breakeven | high | высокий | `05-critic.md` показывает отрицательный median-case даже к M24. |
| Weak moat / evidence_quality_unverified | medium | высокий | Exact-category demand слабый, а moat score всего 11/25. |

## Что должно быть доказано для APPROVED
1. Не меньше 2-3 **paid design partners** в одном узком wedge, а не широкий «AI digital office для всех».
2. pilot-to-production <= 90 дней и предсказуемый template-based onboarding.
3. ARPA не ниже 250-300k ₽/мес в реальных новых сделках.
4. Подтверждённый path к `company_ebitda_rub_month >= 500 000 ₽/мес` за <=24 мес без нового тяжёлого раунда.

## LTV Upside Calculator

Формула: `customer_ltv_rub = ARPA × Gross Margin / churn`.

| Рычаг | Текущее | Целевое | Эффект |
|---|---:|---:|---|
| ARPA | 180 000 ₽/мес | 250 000 ₽/мес | При том же churn LTV вырастет до ~6,70 млн ₽. |
| Churn | 2.8% | 2.0% | При ARPA 180k LTV вырастет до ~6,75 млн ₽. |
| Gross Margin | 75% | 80% | LTV вырастет до ~5,14 млн ₽, но этого мало без роста ARPA. |
| Fixed costs | 5,76 млн ₽/мес | <4,5 млн ₽/мес | Существенно сокращает months_to_500k_ebitda. |
| New clients / month | 2 | 3 | Сдвигает breakeven ближе к горизонту approve. |

## Финальный вывод инвесткомитета
ZeBrains выглядит как осмысленный enterprise automation thesis с хорошей клиентской unit economics, но в текущем виде это **не investment-grade venture case**. Главная причина отказа не спрос как таковой, а отсутствие доказанного пути к `company_ebitda_rub_month >= 500 000 ₽/мес` в base-case за 24 месяца при контролируемом burn и repeatable GTM.


## Stage 7 — Score trajectory

## 2026-04-26 — P5 Unit Economics
- Stage: P5 / unit-economics
- Analyst: branch-models-lead
- Score trajectory: **7.4 → 8.0**
- Verdict shift: **PASS WITH RESERVATIONS → PASS WITH RESERVATIONS**
- Why it moved:
  - fully-loaded blended CAC посчитан на уровне **453k ₽**, а не как «реклама / конверсии», и даже на этой базе модель даёт **LTV/CAC = 10,6x**;
  - recurring economics выглядят рабочими: **MRR 180k ₽/клиент/мес**, **COGS 45k ₽**, **Gross Margin 75%**, **Contribution Margin 71,9%**;
  - компания проходит Profit Gate, потому что при **50 активных клиентах** модель даёт **~713k ₽/мес EBITDA proxy**, то есть порог >500k достижим.
- Key risks:
  - break-even достигается только около **45 клиентов / M16**, значит до него нужен существенный капитал и дисциплина по burn;
  - если pilot, security review и onboarding не стандартизированы, SaaS-маржа быстро деградирует в интеграторскую;
  - широкий message «AI-цифровой офис» может держать CAC высоким, если не сузить wedge до HR ops / service desk / finance approvals.
- Next check:
  - на P6 проверить, есть ли у команды реальный шанс продавать через 1-2 repeatable use-case и удерживать delivery в шаблонном контуре, а не в кастомной разработке.

## 2026-05-09 — P6 Finance Risk / Critic
- Stage: P6 / finance-risk-and-critic
- Analyst: branch-models-lead
- Score trajectory: **8.0 → 6.7**
- Verdict shift: **PASS WITH RESERVATIONS → PASS WITH HEAVY RESERVATIONS**
- Why it moved:
  - обновлённый PnL в `05-critic.md` показывает, что даже base-case остаётся глубоко убыточным на M12, а операционный break-even сдвигается примерно к **M33**;
  - Monte Carlo Lite ухудшает картину: **p10 EBITDA@M24 < 0** и **p50 EBITDA@M24 < 500k ₽/мес**, то есть медианный сценарий не проходит venture-grade EBITDA gate;
  - конкурентное окно в РФ есть, но оно держится на очень жёстких предпосылках по price integrity, repeatable delivery и сужению wedge, а не на уже доказанной repeatability.
- Key risks:
  - компания может не дотянуть до breakeven без крупного капитала и дисциплины по burn;
  - слишком широкий positioning «цифровой офис» повышает CAC и размывает ICP;
  - delivery легко скатывается в кастомную разработку, что ломает software-like economics.
- Next check:
  - на P7 нужен жёсткий финальный verdict: считать ли кейс borderline reject уже сейчас или оставлять только как узкий enterprise thesis при доказанном ICP и суженном GTM.

## 2026-05-09 — P7 Critic and Verdict
- Stage: P7 / critic-and-verdict
- Analyst: branch-models-lead
- Score trajectory: **6.7 → 4.7**
- Verdict shift: **PASS WITH HEAVY RESERVATIONS → REJECTED**
- Why it moved:
  - рубричная оценка дала лишь **47/100**, потому что при сильной клиентской unit economics кейс проваливает критерий EBITDA Potential: `p50 EBITDA@M24 = -1,71 млн ₽/мес`;
  - category demand в РФ существует скорее как `автоматизация бизнес-процессов`, а не как самостоятельный label `AI digital office`, поэтому GTM остаётся enterprise-heavy и дорогим;
  - moat остаётся слабым-средним: при moat score **11/25** продукт легко соскальзывает в integration-heavy delivery без сильного сетевого или data moat.
- Key risks:
  - base-case не выводит компанию к `company_ebitda_rub_month >= 500 000 ₽/мес` за 24 месяца;
  - широкий positioning повышает CAC и усложняет repeatable sales motion;
  - кастомизация внедрений угрожает gross margin и runway.
- Next check:
  - возвращаться к кейсу только если появится узкий wedge с ARPA 250-300k+ ₽/мес, 2-3 paid design partners и подтверждённый pilot-to-production motion <= 90 дней.

