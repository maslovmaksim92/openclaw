# AI Credit Analysis Corporate Financial Statements
**Статус:** REJECTED
**Итоговый балл:** 62/100
**Дата:** 2026-04-19
**Сектор:** B2B Fintech / Credit Risk / Workflow Automation

---

## Этап 1 — Описание кейса
# 00-brief

## Кейс
ai-credit-analysis-corporate-financial-statements

## Статус
active

## Краткое описание
Сервисная модель: внедрение и сопровождение AI-решения для анализа отчётности юридических лиц в кредитных и риск-процессах банков, МФО, лизинговых и факторинговых компаний.

## Текущее состояние
Источник сигнала: triage от 2026-04-16 по кейсу Банка «ЦентроКредит» / BPMSoft / DeepSeek. Сигнал показывает, что LLM-анализ отчётности юрлиц уже встроен в CRM-контур кредитного процесса, а не используется как экспериментальный copilot. Это важно, потому что речь идёт о регулярной операционной функции кредитного аналитика: чтение отчётности, извлечение ключевых показателей, формирование выводов и передача результата дальше по workflow.

Коммерческий сигнал выглядит сильным. Для финансовых организаций эта задача повторяется по большому числу заявок и клиентов, а значит естественно превращается в high-LTV B2B-внедрение с интеграцией в CRM и банковские системы, настройкой моделей и промптов, требованиями к ИБ, журналированию, on-prem или закрытому контуру, SLA и постоянному сопровождению. Для сегмента SME-кредитования и смежных финансовых продуктов потенциал recurring-выручки реалистично превышает 500 000 ₽ в месяц.

Дополнительно кейс усиливает тезис, что рынок готов платить не просто за «AI-анализ документов», а за управляемый AI-workflow внутри кредитного контура, где важны прослеживаемость, контроль качества и интеграция в существующие процессы принятия решений.

## Ключевая гипотеза
Можно собрать high-LTV service business вокруг AI-анализа финансовой отчётности юрлиц для кредитных и риск-процессов, если подтвердится:
- что банки, МФО, факторинговые и лизинговые компании готовы покупать не точечный модуль, а полный сервисный слой вокруг AI-анализа отчётности;
- что основная ценность возникает в сокращении ручного труда кредитных аналитиков, ускорении рассмотрения заявок и стандартизации выводов по заёмщикам;
- что требования по безопасности, валидации и интеграции создают высокий порог входа и поддерживают крупный средний чек;
- что выручка удерживается не только стартовым внедрением, но и за счёт сопровождения, обновления workflow, поддержки моделей и адаптации под новые типы отчётности и внутренние политики риска.

---

## Этап 2 — Проверка спроса
# 02-demand

## Кейс
ai-credit-analysis-corporate-financial-statements

## Дата проверки
2026-04-19, Europe/Moscow

## Сектор
B2B Fintech / Credit Risk / Workflow Automation

## Итог
**DEMAND = MEDIUM+, LTV Gate = PASS. Early reject не требуется.**

Причина: рынок платит за проверку контрагентов, финанализ и скоринг, в РФ уже есть платные risk/compliance-сервисы с понятным прайсингом, Telegram в low-end и SME-слое уже монетизируется, а economics service-led внедрения в банках и смежных финорганизациях проходят порог high-LTV. До чистого HIGH не дотягиваю, потому что обязательный local demand endpoint технически не ответил, а публичных AI-first цен именно на кредитный анализ отчётности немного.

## 1) Mandatory demand API: localhost / multi-demand
Проверил обязательный источник:
- `http://localhost:9001/multi-demand?keyword=AI анализ финансовой отчетности юридических лиц кредитный анализ`
- fallback: `http://172.17.0.1:9001/multi-demand?keyword=AI анализ финансовой отчетности юридических лиц кредитный анализ`

Результат:
- `localhost:9001` -> `Couldn't connect to server`
- `172.17.0.1:9001` -> `Connection timed out after 20001 milliseconds`

Вывод: обязательная попытка выполнена, но composite demand feed в этом прогоне **не получен по технической причине**.

## 2) Прямые сигналы спроса
### HH.ru, масштаб ручной боли
- `кредитный аналитик` -> **4 888 вакансий**
  - https://hh.ru/search/vacancy?text=%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA
- `финансовый анализ отчетности` -> **2 019 вакансий**
  - https://hh.ru/search/vacancy?text=%D1%84%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7+%D0%BE%D1%82%D1%87%D0%B5%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%B8

Интерпретация: это сильный proxy на объём ручной работы в кредитном и риск-контуре. Если даже часть этого труда автоматизируема, buyer pain реален.

### Объём адресуемой базы
Для грубого TAM беру институциональный слой, где решение действительно может продаваться как workflow, а не как дешёвый data lookup:
- банковский сектор РФ: **306 действующих банков** на 01.03.2026
- МФО в госреестре: **834 организации**
- лизинговый рынок: **100+ компаний** в рэнкинге Эксперт РА
- факторинг: **37 организаций** в обзоре АФК

Итого базовая адресуемая группа для enterprise / mid-market: примерно **1 277 организаций**.

## 3) Реальные конкуренты с ценами
Важно: ниже не только AI-first продукты, а реальные бюджетные альтернативы, из которых покупатель уже оплачивает risk / due diligence / финанализ и которые конкурируют за тот же бюджет кредитного контура.

### Контур.Фокус
Официальные тарифы:
- **31 155 ₽** за тариф «Базовый»
- **82 770 ₽** за тариф «Премиум»
- **115 000 ₽** за тариф «Корпорация»
Источник: https://focus.kontur.ru/price

### Rusprofile
Официальные тарифы:
- **940 ₽/мес** за «Базовый»
- **1 990 ₽/мес** за «Эксперт»
- доп. отчёт по физлицу: **230 ₽**
Источники:
- https://www.rusprofile.ru/subscribe
- https://www.rusprofile.ru/subscribe-plus

### Прима-Информ
Официальные тарифы:
- **16 000 ₽/год** за «Пакет 100»
- **52 000 ₽/год** за «Базовый»
- **65 000 ₽/год** за «Оптима»
- **975 000 ₽/год** за API
Источник: https://www.prima-inform.ru/services

## 4) Что цены конкурентов говорят о willingness to pay
WTP подтверждён напрямую:
1. Рынок уже платит не только за справки, но и за постоянный мониторинг, скоринг, API и проверку физлиц.
2. Прайс якорится от **940 ₽/мес** в low-end до **975 000 ₽/год** за API в mid/high-end, то есть бюджетная строка на автоматизацию и риск-анализ уже существует.
3. Для банков и МФО покупка такого слоя логична, потому что даже один кредитный аналитик стоит примерно **150 000-275 000 ₽/мес** по открытым вакансиям HH, а решение продаётся как сокращение ручного разбора отчётности, ускорение SLA и стандартизация выводов.
4. Следовательно, оффер уровня `интеграция + workflow + контроль качества + журналирование` может обоснованно продаваться существенно дороже реестрового lookup-инструмента.

## 5) Telegram bots / services в RU
### OnlyRead
Подтверждено:
- OCR и PDF-инструменты работают через **Telegram и MAX**
- есть API и сценарии для бухгалтеров, логистов и документооборота
- цены:
  - **100 ₽/мес** за 30 страниц
  - **950 ₽/мес** за 500 страниц
  - **3 490 ₽/мес** за 2 000 страниц
- на сайте заявлены **35 001 пользователей** и **185 735 страниц распознано**
Источник: https://www.onlyread.ru/

### БухБот
Подтверждено:
- сервис работает в **Telegram или MAX**
- разбирает документы, письма ФНС, договоры, PDF, Word, фото и голос
- цены:
  - **990 ₽/мес**
  - **1 690 ₽/мес**
  - **3 790 ₽/мес**
  - **6 490 ₽/мес**
Источник: https://buh-bot.ru/

### Вывод по Telegram в РФ
- Telegram как канал монетизации для финансово-документных задач в РФ **доказан**.
- Но я не нашёл сильного Telegram-native enterprise-решения именно для AI-кредитного анализа отчётности юрлиц в банках.
- Это хорошо для wedge: в low-end рынок уже обучен пользоваться ботами, а enterprise-слой остаётся свободнее и дороже.

## 6) TAM / SAM / SOM в рублях
Ниже расчёт не по всему объёму кредитования, а по **рынку spend на software + service layer** вокруг анализа отчётности и кредитного workflow.

### TAM
Допущения:
- адресуемая база = **1 277 организаций**
- средний годовой spend на решение класса `скоринг + финанализ + workflow + мониторинг` = **2.4 млн ₽/год**
  - это около **200 000 ₽/мес**
  - выше коробочных справочных сервисов, но заметно ниже типового enterprise-managed rollout

Расчёт:
- **TAM = 1 277 x 2 400 000 ₽ = 3.06 млрд ₽/год**

### SAM
Допущения:
- реально достижимый сейчас сегмент: банки, крупные МФО и часть лизинга/факторинга, где есть поток SME/corporate underwriting
- консервативно беру **490 организаций**:
  - 180 банков
  - 250 МФО
  - 40 лизинговых и факторинговых игроков
- средний чек для service-led модели = **3.6 млн ₽/год**
  - это около **300 000 ₽/мес**

Расчёт:
- **SAM = 490 x 3 600 000 ₽ = 1.764 млрд ₽/год**

### SOM
Допущения:
- достижимая доля за 3-5 лет = **25 клиентов** в узком сегменте
- средний реализованный чек = **6.0 млн ₽/год** на клиента
  - это около **500 000 ₽/мес**, что совпадает с гипотезой high-LTV в brief

Расчёт:
- **SOM = 25 x 6 000 000 ₽ = 150 млн ₽/год**

### Вывод по рынку
Для service business фондового масштаба ниша не гигантская, но достаточно крупная: даже при узком go-to-market и без выхода за пределы РФ получается **SOM 150 млн ₽/год**, а TAM превышает **3 млрд ₽/год**.

## 7) LTV Gate: проверка всех сценариев монетизации
Проверяю все основные сценарии.

### Сценарий A. Self-serve SaaS / seat-based
- Продавать только доступ к интерфейсу финанализа без интеграции рискованно.
- На этом уровне рынок уже занят более дешёвыми сервисами проверки контрагентов.
- **Вердикт: FAIL как standalone-модель.**

### Сценарий B. Usage-based per report / per borrower
- Работает, если продукт встроен в поток заявок и биллинг привязан к объёму кейсов.
- Может быть хорошим входом для МФО и части лизинга.
- Но без minimum commit модель хрупкая.
- **Вердикт: PASS с условием минимального годового коммита.**

### Сценарий C. Внедрение + интеграция в CRM / BPM / LOS
- Это самый естественный коммерческий сценарий.
- Setup **1.5-4.0 млн ₽** плюс поддержка **200k-600k ₽/мес** выглядит реалистично для банков и крупных небанковских кредиторов.
- **Вердикт: PASS.**

### Сценарий D. Managed underwriting / analyst copilot as a service
- Продаётся не софт, а ускорение кредитного контура и снижение ручной нагрузки.
- Один клиент с заметным потоком SME-кейсов может давать **500k-1.5m ₽/мес**.
- **Вердикт: PASS.**

### Сценарий E. On-prem / private contour / annual license
- Для банковского контура это часто обязательный формат.
- Годовая лицензия + SLA + доработки могут держать чек **3-12 млн ₽/год**.
- **Вердикт: PASS.**

### Сценарий F. White-label / embedded для вендоров CRM и кредитных платформ
- Продажа через BPM/CRM/LOS-партнёров удлиняет цикл, но резко расширяет distribution.
- Модель `setup + revshare/minimum guarantee` реалистична.
- **Вердикт: PASS.**

### Общий итог LTV Gate
**LTV Gate = PASS.**

Ключевой вывод: дешёвый standalone-инструмент для одной кнопки финанализа неинтересен, но `enterprise workflow + integration + control layer` уверенно проходит порог high-LTV.

## 8) Финальный verdict по спросу
**Спрос подтверждён достаточно, чтобы не делать early reject.**

Почему не REJECT:
- есть реальные платные конкуренты в РФ с ценами и API-уровнем monetization;
- buyer budget на risk / due diligence / скоринг уже существует;
- Telegram в РФ уже монетизирует документные и бухгалтерские сценарии;
- LTV проходит почти во всех серьёзных monetization-моделях, кроме commodity self-serve.

Почему пока не ставлю HIGH:
- обязательный `multi-demand` не ответил;
- публичных AI-first цен именно на анализ финансовой отчётности мало;
- часть рынка пока выглядит как consulting-heavy sale, а не чистый software pull.

## Решение
**ОСТАВИТЬ В ПАЙПЛАЙНЕ И ПЕРЕХОДИТЬ К СЛЕДУЮЩЕМУ ЭТАПУ.**

## Источники
- HH, `кредитный аналитик`: https://hh.ru/search/vacancy?text=%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA
- HH, `финансовый анализ отчетности`: https://hh.ru/search/vacancy?text=%D1%84%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7+%D0%BE%D1%82%D1%87%D0%B5%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%B8
- Банки РФ, 306 на 01.03.2026: https://www.banki.ru/news/lenta/?id=11022515
- МФО, 834 организации: https://bankstoday.net/last-articles/skolko-mfo-rabotaet-v-rossii-i-kak-vybrat-udobnuyu-kompaniyu
- Эксперт РА, рэнкинг лизинговых компаний: https://raexpert.ru/rankings/leasing/9m2025/
- АФК, обзор рынка факторинга: https://asfact.ru/events/itogi-rynka-faktoringa-za-1-kvartal-2025-goda/
- Контур.Фокус pricing: https://focus.kontur.ru/price
- Rusprofile pricing: https://www.rusprofile.ru/subscribe
- Rusprofile Plus: https://www.rusprofile.ru/subscribe-plus
- Прима-Информ pricing: https://www.prima-inform.ru/services
- OnlyRead: https://www.onlyread.ru/
- БухБот: https://buh-bot.ru/

---

## Этап 3 — Юнит-экономика
# 04-economics

## Кейс
`ai-credit-analysis-corporate-financial-statements`

## Дата проверки
2026-04-19 (Europe/Moscow)

## Итог этапа
PASS

## ICP, на котором сходится экономика
- банки с потоком SME / corporate underwriting;
- крупные МФО с ручным анализом бухгалтерской отчётности юрлиц;
- лизинговые и факторинговые компании, где нужен быстрый разбор отчётности, нормализация коэффициентов и audit trail;
- enterprise buyer, которому нужен не просто отчёт, а workflow: ingest документов, анализ, human QA, журналирование, интеграция в LOS / CRM / BPM.

Для small business и standalone self-serve режима экономика не инвестиционная. Модель ниже построена только для enterprise ICP.

## Базовые допущения модели
- Net price: **680 000 ₽/клиент/мес**
- Контракт: **12 месяцев**, чаще с годовым minimum commit
- Отдельный setup fee: **2,0-3,5 млн ₽**, в базовый recurring-case не включаю, считаю upside
- Gross logo churn: **1,7% в месяц**
- COGS: **235 000 ₽/клиент/мес**
- Contribution per client: **445 000 ₽/клиент/мес**
- Blended CAC: **1 550 000 ₽**
- Fixed costs: **4 990 000 ₽/мес**

## Почему беру churn = 1,7% / месяц
В demand-файле кейс уже прошёл LTV gate только в enterprise / integration / managed workflow сценарии. Для такого high-ARPA B2B workflow разумно брать churn существенно ниже median SMB SaaS, но не рисовать unrealistically low значение.

Benchmark: по ChartMogul для компаний уровня **$15M-30M ARR** monthly **customer churn** составляет:
- **1,3%** у top decile;
- **1,7%** у top quartile;
- **4,1%** у median.

Для кредитного workflow с интеграцией в процессы, annual contract и заметными switching costs беру **1,7% в месяц** как верхнюю границу investment-grade enterprise execution, но без агрессивной фантазии.

Источник benchmark:
- ChartMogul, SaaS metrics cheat sheet: https://chartmogul.com/resources/saas-metrics-cheat-sheet/

## 1) Детальная таблица business process: от lead до payment

Все суммы ниже, кроме последнего шага, даны как **полностью распределённая стоимость на 1 выигранного клиента**.

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов: банки, МФО, лизинг, факторинг | SDR + RevOps | CRM, HH/рынок, spreadsheets, enrichment | 1 рабочий день | 22 000 | 75% |
| 2 | Многошаговый outbound и выход на risk / credit decision maker | SDR | Email sequencing, Telegram, CRM | 10-14 дней касаний | 145 000 | 65% |
| 3 | Qualification call и проверка fit по потоку кейсов и стеку | AE | Meet/Zoom, CRM, AI notes | 1 час | 26 000 | 60% |
| 4 | Discovery и demo целевого workflow | AE + founder | Demo env, deck, ROI calculator | 1,5 часа | 42 000 | 45% |
| 5 | Scoping: формы отчётности, API, формат кредитного досье, compliance | Solutions architect + product lead | Notion/Jira, architecture docs, security questionnaire | 4-5 дней | 98 000 | 35% |
| 6 | Подготовка pilot proposal и бизнес-кейса | AE + founder + finance | Proposal docs, pricing model, ROI sheet | 2-3 дня | 86 000 | 45% |
| 7 | Pilot setup: загрузка отчётности, маппинг полей, настройка extraction | Implementation manager + ML engineer | ETL, OCR/LLM pipeline, sandbox | 2 недели | 260 000 | 50% |
| 8 | Валидация коэффициентов, human QA, tuning prompt/policy | Credit analyst SME + ML engineer | Review console, evals, annotation tools | 1-2 недели | 120 000 | 30% |
| 9 | Security / procurement / legal redlines | Founder + ops/legal | Contracting, DPA/SLA, procurement portal | 2-4 недели | 145 000 | 25% |
| 10 | Close won и handoff | AE + CSM | CRM, handoff checklist | 1 день | 38 000 | 65% |
| 11 | Production onboarding, обучение analyst team, роли и доступы | CSM + implementation manager | LMS, help center, admin console | 1 неделя | 72 000 | 55% |
| 12 | Первый production invoice и reconciliation оплаты | Finance ops | Billing, банк, ЭДО, бухгалтерия | 2-3 дня | 14 000 | 85% |

**Итого стоимость пути lead -> первый платёж: ~1 068 000 ₽ прямых затрат.**

Разница до blended CAC **1 550 000 ₽** объясняется потерянными пилотами, невыигранными сделками, долей бренд-маркетинга, участием founder time и общим pipeline overhead.

## 2) COGS breakdown на клиента в месяц

| Компонент COGS | Логика | ₽/клиент/мес |
|---|---|---:|
| OCR / parsing / LLM / compute | извлечение из PDF/сканов, нормализация форм, генерация draft memo | 58 000 |
| Human credit QA | проверка аномалий, exception cases, ручная калибровка выводов | 82 000 |
| Customer success variable time | сопровождение risk / credit teams, обучение, QBR | 24 000 |
| Secure hosting / storage / audit logs | изолированная инфраструктура, архив, журналирование | 28 000 |
| Onboarding amortization | часть внедрения, размазанная по сроку контракта | 26 000 |
| Support / SLA reserve | инциденты, нестандартные запросы, оперативный разбор | 12 000 |
| Billing / admin variable | ЭДО, платёжная и бухгалтерская обработка | 5 000 |
| **Итого COGS** |  | **235 000** |

## 3) CAC по acquisition channels с funnel conversion

### Канал 1. Founder-led outbound / ABM
| Метрика | Значение |
|---|---:|
| Target accounts за квартал | 720 |
| Positive reply rate | 8,3% |
| Positive replies | 60 |
| Discovery booked | 24 |
| Discovery -> pilot | 50% |
| Pilots | 12 |
| Pilot -> closed won | 25% |
| Closed won | 3 |
| Quarterly spend | 5 700 000 ₽ |
| **CAC** | **1 900 000 ₽** |

### Канал 2. Партнёры / referrals / интеграторы
| Метрика | Значение |
|---|---:|
| Partner intros за квартал | 48 |
| Intro -> discovery | 50% |
| Discoveries | 24 |
| Discovery -> pilot | 42% |
| Pilots | 10 |
| Pilot -> closed won | 30% |
| Closed won | 3 |
| Quarterly spend | 3 300 000 ₽ |
| **CAC** | **1 100 000 ₽** |

### Канал 3. Контент / events / inbound
| Метрика | Значение |
|---|---:|
| MQL за квартал | 150 |
| MQL -> SQL | 24% |
| SQL | 36 |
| SQL -> discovery | 50% |
| Discoveries | 18 |
| Discovery -> pilot | 33% |
| Pilots | 6 |
| Pilot -> closed won | 33% |
| Closed won | 2 |
| Quarterly spend | 3 100 000 ₽ |
| **CAC** | **1 550 000 ₽** |

### Blended CAC
Предполагаемый mix новых клиентов:
- outbound ABM: **45%**;
- partner/referral: **35%**;
- inbound/content: **20%**.

Расчёт:
- `1 900 000 × 0,45 + 1 100 000 × 0,35 + 1 550 000 × 0,20 = 1 550 000 ₽`

**Blended CAC = 1 550 000 ₽**

## 4) LTV с churn rate

Формула contribution-LTV:
- `LTV = Monthly Contribution / Monthly Churn`
- `445 000 / 0,017 = 26 176 471 ₽`

**LTV = ~26,2 млн ₽**

Порог `LTV > 500k ₽` пройден с очень большим запасом.

## 5) LTV / CAC ratio
- `26,18 млн / 1,55 млн = 16,9x`

**LTV/CAC = 16,9:1**

## 6) CAC Payback
Формула:
- `CAC payback = CAC / Monthly Contribution`
- `1 550 000 / 445 000 = 3,48 месяца`

**CAC payback = ~3,5 месяца**

## 7) Contribution Margin %
Формула:
- `(680 000 - 235 000) / 680 000 = 65,4%`

**Contribution Margin = 65,4%**

## 8) Полная таблица команды

| Роль | Функция | FTE | Месячная зарплата, ₽ | Тип |
|---|---|---:|---:|---|
| Founder / CEO | enterprise sales, ключевые сделки, партнёры | 1 | 320 000 | fixed |
| Product Lead | продуктовая стратегия, credit workflow design | 1 | 320 000 | fixed |
| ML / AI Engineer | extraction, prompts, evals, model orchestration | 1 | 340 000 | fixed |
| Backend / Integrations Engineer | API, LOS/CRM/BPM интеграции, data pipelines | 1 | 300 000 | fixed |
| Data / Document Engineer | парсинг отчётности, ETL, schema mapping | 1 | 260 000 | fixed |
| Credit Risk SME | правила анализа, QA policy, calibration | 1 | 250 000 | fixed |
| Account Executive | pipeline, demos, close | 1 | 280 000 | fixed |
| SDR / BDR | outbound prospecting | 1 | 160 000 | fixed |
| Implementation Manager | pilot setup, rollout, enablement | 1 | 220 000 | fixed |
| Customer Success Manager | adoption, renewals, expansion | 1 | 190 000 | fixed |
| Finance / Ops / Legal coordinator | billing, договоры, документооборот | 1 | 150 000 | fixed |
| DevOps / Security engineer | инфраструктура, доступы, аудит | 0,5 | 140 000 | fixed |
| Variable credit QA capacity | ручная проверка клиентских кейсов | 0,3-0,4 FTE на клиента | 82 000 на клиента | **COGS** |

**Итого fixed payroll = 2 930 000 ₽/мес**

## 9) Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| Fixed payroll | 2 930 000 |
| Налоги, взносы, benefits (~24%) | 700 000 |
| Core software stack (CRM, data, monitoring, security, workspace) | 260 000 |
| Legal, accounting, audit, insurance | 170 000 |
| Sales travel / events / partner development | 360 000 |
| Office / remote / admin | 170 000 |
| Brand / content baseline spend | 250 000 |
| Misc G&A reserve | 150 000 |
| **Итого fixed costs** | **4 990 000** |

## 10) Break-even по CLIENT COUNT и по MONTH

### Break-even по числу клиентов
Формула:
- `Break-even clients = Fixed costs / Monthly contribution per client`
- `4 990 000 / 445 000 = 11,21`

**Break-even = 12 активных клиентов**

### Break-even по месяцу
Если ramp такой:
- месяц 1: 0 клиентов
- месяц 2: 1 клиент
- месяц 3: 2 клиента
- месяц 4: 3 клиента
- месяц 5: 5 клиентов
- месяц 6: 7 клиентов
- месяц 7: 9 клиентов
- месяц 8: 11 клиентов
- месяц 9: 12 клиентов

то операционный break-even достигается на **9-м месяце**.

## Проверка fund-level критерия
- LTV > 500k ₽: **PASS**
- LTV/CAC >= 1:1: **PASS**
- LTV/CAC >= 3:1 investment grade: **PASS**
- CAC payback < 12 месяцев: **PASS**
- Contribution margin > 50%: **PASS**

## Главный вывод
Экономика для кейса **сходится** при продаже enterprise workflow, а не коробочного скоринг-виджета.

Что держит модель:
- высокий ACV относительно стоимости внедрения;
- понятный buyer budget, уже подтверждённый ценами конкурентов из demand-этапа;
- switching costs после интеграции в кредитный контур;
- human QA остаётся ограниченным слоем, а не основной фабрикой труда.

Что ломает модель:
- уход в low-end сегмент с чеком ниже **450 000 ₽/мес**;
- превращение пилота в бесконечный custom services проект;
- рост blended CAC выше **3,0 млн ₽**;
- рост COGS выше **320 000 ₽/клиент/мес** из-за слишком большого объёма ручной проверки.

## Финальный verdict по Program 5
**PASS**. Для enterprise credit analysis workflow кейс выглядит **investment-grade по unit economics**.

## Источники
- Demand inputs и pricing anchors: `pipeline/cases/ai-credit-analysis-corporate-financial-statements/02-demand.md`
- ChartMogul churn benchmark: https://chartmogul.com/resources/saas-metrics-cheat-sheet/

## Ограничения
- Это инвестиционная модель для enterprise ICP, а не отражение публичного прайса конкретного вендора.
- Setup fee не включён в базовый recurring-case, поэтому итог скорее консервативен.
- Churn benchmark взят из общего SaaS benchmark и адаптирован под high-ARPA B2B workflow SaaS с интеграцией.

---

## Этап 4 — Финансовая модель и критика
# 05-critic

## Кейс
`ai-credit-analysis-corporate-financial-statements`

## Дата проверки
2026-04-19 (Europe/Moscow)

## Итог этапа
**CRITIC = CONDITIONAL PASS.**

Unit economics из `04-economics.md` действительно выглядят сильными, но они держатся только в узком enterprise-сценарии: высокий ACV, ограниченный churn, контролируемый human QA и отсутствие ценовой войны с low-end игроками. Для фонда это не «автоматический PASS», а модель с хорошей отдачей при очень дисциплинированном GTM и delivery.

---

## 1) 12-месячный P&L, 3 сценария

### Базовый сценарий
Допущения: цена 680 000 ₽/клиент/мес, COGS 235 000 ₽/клиент/мес, fixed cost scale-up от 5,2 до 6,0 млн ₽/мес.

| Месяц | MRR, ₽ | COGS, ₽ | Gross Profit, ₽ | Fixed Costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| 1 | 0 | 0 | 0 | 5 200 000 | -5 200 000 |
| 2 | 680 000 | 235 000 | 445 000 | 5 200 000 | -4 755 000 |
| 3 | 1 360 000 | 470 000 | 890 000 | 5 200 000 | -4 310 000 |
| 4 | 2 040 000 | 705 000 | 1 335 000 | 5 400 000 | -4 065 000 |
| 5 | 3 400 000 | 1 175 000 | 2 225 000 | 5 400 000 | -3 175 000 |
| 6 | 4 760 000 | 1 645 000 | 3 115 000 | 5 400 000 | -2 285 000 |
| 7 | 6 120 000 | 2 115 000 | 4 005 000 | 5 700 000 | -1 695 000 |
| 8 | 7 480 000 | 2 585 000 | 4 895 000 | 5 700 000 | -805 000 |
| 9 | 8 160 000 | 2 820 000 | 5 340 000 | 5 700 000 | -360 000 |
| 10 | 8 840 000 | 3 055 000 | 5 785 000 | 6 000 000 | -215 000 |
| 11 | 9 520 000 | 3 290 000 | 6 230 000 | 6 000 000 | 230 000 |
| 12 | 10 200 000 | 3 525 000 | 6 675 000 | 6 000 000 | 675 000 |

### Оптимистичный сценарий

| Месяц | MRR, ₽ | COGS, ₽ | Gross Profit, ₽ | Fixed Costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| 1 | 0 | 0 | 0 | 5 300 000 | -5 300 000 |
| 2 | 680 000 | 235 000 | 445 000 | 5 300 000 | -4 855 000 |
| 3 | 2 040 000 | 705 000 | 1 335 000 | 5 300 000 | -3 965 000 |
| 4 | 3 400 000 | 1 175 000 | 2 225 000 | 5 600 000 | -3 375 000 |
| 5 | 4 760 000 | 1 645 000 | 3 115 000 | 5 600 000 | -2 485 000 |
| 6 | 6 120 000 | 2 115 000 | 4 005 000 | 5 600 000 | -1 595 000 |
| 7 | 7 480 000 | 2 585 000 | 4 895 000 | 6 000 000 | -1 105 000 |
| 8 | 8 840 000 | 3 055 000 | 5 785 000 | 6 000 000 | -215 000 |
| 9 | 10 200 000 | 3 525 000 | 6 675 000 | 6 000 000 | 675 000 |
| 10 | 11 560 000 | 3 995 000 | 7 565 000 | 6 500 000 | 1 065 000 |
| 11 | 12 920 000 | 4 465 000 | 8 455 000 | 6 500 000 | 1 955 000 |
| 12 | 14 280 000 | 4 935 000 | 9 345 000 | 6 500 000 | 2 845 000 |

### Пессимистичный сценарий

| Месяц | MRR, ₽ | COGS, ₽ | Gross Profit, ₽ | Fixed Costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| 1 | 0 | 0 | 0 | 5 000 000 | -5 000 000 |
| 2 | 0 | 0 | 0 | 5 000 000 | -5 000 000 |
| 3 | 680 000 | 235 000 | 445 000 | 5 000 000 | -4 555 000 |
| 4 | 1 360 000 | 470 000 | 890 000 | 5 100 000 | -4 210 000 |
| 5 | 2 040 000 | 705 000 | 1 335 000 | 5 100 000 | -3 765 000 |
| 6 | 2 720 000 | 940 000 | 1 780 000 | 5 100 000 | -3 320 000 |
| 7 | 3 400 000 | 1 175 000 | 2 225 000 | 5 300 000 | -3 075 000 |
| 8 | 4 080 000 | 1 410 000 | 2 670 000 | 5 300 000 | -2 630 000 |
| 9 | 4 760 000 | 1 645 000 | 3 115 000 | 5 300 000 | -2 185 000 |
| 10 | 5 440 000 | 1 880 000 | 3 560 000 | 5 500 000 | -1 940 000 |
| 11 | 6 120 000 | 2 115 000 | 4 005 000 | 5 500 000 | -1 495 000 |
| 12 | 6 800 000 | 2 350 000 | 4 450 000 | 5 500 000 | -1 050 000 |

### Вывод по P&L
- База выходит в положительный EBITDA только в **11-м месяце**.
- Оптимистичный сценарий начинает печатать EBITDA в **9-м месяце**.
- Пессимистичный сценарий **не достигает EBITDA break-even за 12 месяцев**.

---

## 2) Waterfall cost structure, месяц 12, базовый сценарий

Месяц 12: выручка **10,2 млн ₽**.

| Статья | ₽ | % от выручки |
|---|---:|---:|
| MRR | 10 200 000 | 100,0% |
| COGS | 3 525 000 | 34,6% |
| Sales & Marketing | 2 400 000 | 23,5% |
| R&D | 2 100 000 | 20,6% |
| G&A | 1 500 000 | 14,7% |
| EBITDA | 675 000 | 6,6% |

Критическое наблюдение: у компании не «software-only» профиль, а hybrid workflow business. При снижении цены или росте ручного QA весь EBITDA-слой исчезает очень быстро.

---

## 3) Cash flow analysis

### Burn rate, месяцы 1-3
Берём EBITDA burn и добавляем cash CAC на новых клиентов.

| Месяц | EBITDA, ₽ | CAC cash out, ₽ | Net burn, ₽ |
|---|---:|---:|---:|
| 1 | -5 200 000 | 0 | -5 200 000 |
| 2 | -4 755 000 | 1 550 000 | -6 305 000 |
| 3 | -4 310 000 | 1 550 000 | -5 860 000 |

### Стартовый капитал до operating BEP
- operating EBITDA break-even в базовом сценарии: **месяц 11**;
- накопленный cash burn до конца месяца 10, с учётом CAC: **47,0 млн ₽**;
- если фонд хочет профинансировать и рост в месяцы 11-12, пик внешней потребности за год: **49,2 млн ₽**.

### Вывод
Раунд меньше **50 млн ₽** делает модель хрупкой: даже при хорошем ACV компания почти весь первый год живёт в режиме отрицательного операционного потока.

---

## 4) Sensitivity analysis

База из `04-economics.md`:
- price: **680 000 ₽/мес**
- COGS: **235 000 ₽/мес**
- contribution: **445 000 ₽/клиент/мес**
- CAC: **1 550 000 ₽**
- churn: **1,7%/мес**
- LTV: **26,2 млн ₽**
- LTV/CAC: **16,9x**
- payback: **3,5 месяца**
- EBITDA month 12 base: **675 000 ₽**

### Сценарий A. CAC x2
- новый CAC: **3 100 000 ₽**
- payback: `3 100 000 / 445 000 = 6,97 месяца`
- LTV/CAC: `26,18 / 3,10 = 8,45x`
- дополнительная cash-потребность на 15 выигранных клиентов за 12 месяцев: **+23,25 млн ₽**
- годовая peak funding need растёт примерно с **49,2 млн ₽** до **72,4 млн ₽**

**Вывод:** unit economics на бумаге ещё живы, но фондовая эффективность резко ухудшается из-за капиталоёмкости GTM.

### Сценарий B. Churn x2
- новый churn: **3,4%/мес**
- новый LTV: `445 000 / 0,034 = 13,09 млн ₽`
- новый LTV/CAC: `13,09 / 1,55 = 8,45x`
- при том же графике продаж ожидаемая активная база к месяцу 12 падает примерно с **13,75** до **12,62** клиента
- month 12 MRR падает примерно на **768 000 ₽**
- month 12 EBITDA падает примерно с **675 000 ₽** до **172 000 ₽**

**Вывод:** модель ещё не ломается мгновенно, но запас прочности почти исчезает, особенно перед сезоном продлений.

### Сценарий C. Price -30%
- новая цена: **476 000 ₽/клиент/мес**
- contribution на клиента: `476 000 - 235 000 = 241 000 ₽`
- month 12 MRR при 15 клиентах: **7,14 млн ₽**
- month 12 Gross Profit: **3,615 млн ₽**
- month 12 EBITDA: `3,615 - 6,0 = -2,385 млн ₽`
- новый payback: `1 550 000 / 241 000 = 6,43 месяца`
- новый break-even по активным клиентам: `6 000 000 / 241 000 = 24,9`, то есть **25 клиентов**

**Вывод:** именно цена, а не churn, является главным kill lever. Если рынок затянет продукт в коробочный low-end, экономика перестаёт быть инвестиционной.

---

## 5) Competitor deep-dive

### 1. Контур.Фокус
**Сильные стороны**
- сильный бренд и доверие в compliance / due diligence;
- существующие продажи в B2B и enterprise;
- понятный budget line у buyer.

**Слабые стороны**
- это скорее data/compliance platform, чем AI-native underwriting workflow;
- слабее в глубоком разборе бухгалтерской отчётности под кредитный меморандум;
- продукт может быть «справочным слоем», а не системой исполнения.

**Copy risk**
- **высокий**. Если AI-разбор отчётности докажет ценность, большой incumbent легко добавит summary, alerts и scoring поверх своей базы.

### 2. Rusprofile
**Сильные стороны**
- экстремально низкий ценовой порог;
- огромная привычность для малого и среднего рынка;
- быстрая проверка контрагентов без сложного внедрения.

**Слабые стороны**
- плохо подходит под enterprise workflow, audit trail и интеграцию в кредитный контур;
- buyer получает данные, но не end-to-end underwriting process;
- низкий ACV ограничивает глубину сервиса.

**Copy risk**
- **средний**. Скопировать enterprise delivery-модель сложнее, но утянуть low-end сегмент и навязать ценовой якорь они могут очень быстро.

### 3. Прима-Информ
**Сильные стороны**
- есть API-слой и привычка продавать более дорогой data access;
- понятна enterprise-логика закупки;
- может быть удобным источником данных для существующих risk-процессов.

**Слабые стороны**
- value proposition ближе к data feed, чем к решению «анализ + действие + QA + журналирование»;
- внедрение может требовать собственной команды клиента;
- меньше AI-first differentiation на уровне user experience.

**Copy risk**
- **средне-высокий**. API-провайдеру проще докрутить AI-слой, чем AI-стартапу быстро построить data moat.

### Общий вывод по конкурентам
Риск не в том, что incumbents уже лучше в AI, а в том, что у них уже есть distribution, budget line и data access. Стартап обязан выигрывать не «наличием LLM», а скоростью кредитного решения, traceability и качеством workflow.

---

## 6) Risk matrix

| Риск | Вероятность | Влияние, ₽/мес | Early signal | Mitigation |
|---|---|---:|---|---|
| Сдвиг в low-end pricing и давление на чек | Средняя | 2 385 000 | проигрыши сделок против коробочных альтернатив, запросы на price cut >20% | жёстко продавать ROI по SLA и headcount, убирать SMB/commodity сегмент |
| Рост ручного QA и exception handling | Высокая | 1 275 000 | COGS > 320 000 ₽/клиент/мес, доля manual review > 45% кейсов | ограничить scope, строить policy engine, сегментировать кейсы по сложности |
| Удлинение enterprise sales cycle до 9-12 месяцев | Средняя | 1 550 000 | pilots зависают без procurement close, pipeline coverage <3x | партнёрский канал, pre-scoped pilot templates, upfront paid discovery |
| Churn на продлениях из-за слабой интеграции в workflow | Средняя | 503 000 | usage stagnation, QBR без expansion, renewal risk flags за 90 дней | сильный implementation, embedded reporting, executive sponsor map |
| Регуляторные/ИБ требования банка требуют on-prem и доработок | Средняя | 900 000 | security questionnaire >60 дней, новые требования по private contour | заранее готовить on-prem пакет, reference architecture, дорогой setup fee |

---

## 7) Kill conditions

### Kill condition 1
Если к **месяцу 6** активная база меньше **5 клиентов** или pipeline coverage ниже **3x** от квартального плана, кейс не подтверждает воспроизводимый GTM.

### Kill condition 2
Если к **месяцу 9** фактический COGS превышает **320 000 ₽/клиент/мес** два месяца подряд, значит продукт скатывается в services business без software leverage.

### Kill condition 3
Если средний реализованный net price падает ниже **500 000 ₽/клиент/мес** на трёх подряд новых контрактах, инвестиционный кейс нужно закрывать: модель уходит в отрицательный month-12 EBITDA.

---

## Финальный вывод
Кейс можно пропускать дальше только как **узкий enterprise underwriting workflow**, а не как массовый SaaS по анализу отчётности. В базе модель выглядит хорошей, но инвестиционная прочность сидит почти полностью в трёх переменных: **цена, контроль COGS и дисциплина продаж**. Любой серьёзный срыв по одной из них быстро превращает красивую unit economics-таблицу в капиталоёмкий сервисный бизнес.

---

## Этап 5 — Финальный вердикт
# 06-verdict

## Кейс
ai-credit-analysis-corporate-financial-statements

## Дата вердикта
2026-04-19, Europe/Moscow

## Итог
**REJECTED. Итоговый балл: 62/100.**

Кейс подтверждает, что в РФ существует бюджет на risk/compliance и автоматизацию кредитного контура, а unit economics на уровне одного enterprise-клиента выглядит сильной. Но для инвесткомитета решающий стоп-фактор, что путь к `company_ebitda_rub_month >= 500 000 ₽` требует слишком большого стартового капитала, а конкурентная защита остаётся умеренной на фоне действующих data/incumbent игроков с distribution и уже закреплённой budget line.

## Score breakdown
| Критерий | Балл | Макс | Почему |
|---|---:|---:|---|
| Реальный спрос | 16 | 20 | HH показывает 4 888 вакансий по запросу «кредитный аналитик» и 2 019 по «финансовый анализ отчетности», есть 3 реальных конкурента с ценами и подтверждённый WTP, но mandatory multi-demand endpoint не ответил, а публичных AI-first кейсов именно по credit workflow в РФ мало. |
| Прибыль компании / Unit Economics | 13 | 25 | `clients_to_500k_ebitda = 15`, `months_to_500k_ebitda = 12`, `clients_to_1m_ebitda = 16`, `months_to_1m_ebitda = 13`, но `startup_capital_to_bep_rub ≈ 47 000 000 ₽`, а peak funding need достигает 49,2 млн ₽. Это выше допустимого для быстрого инвестиционного прохода. |
| Масштабируемость | 12 | 20 | Workflow частично автоматизирован, но human credit QA, implementation и enterprise onboarding остаются существенной частью delivery. |
| Конкурентное позиционирование | 7 | 15 | Дифференциация есть в AI-native underwriting workflow и traceability, но Контур.Фокус, Rusprofile и data/API-игроки могут быстро добавить AI-слой и давить distribution-каналом. |
| Барьеры входа | 6 | 10 | Интеграции в LOS/CRM/BPM, private contour и security review дают реальные switching costs, но непреодолимого moat пока нет. |
| Качество данных | 8 | 10 | Большинство ключевых цифр опирается на реальные цены, вакансии и benchmark churn, WTP подтверждён, но часть TAM/SAM/SOM и траектория роста остаются аналитическим выводом. |
| **Итого** | **62** | **100** | **Ниже порога 65, кейс отклонён.** |

## Полный бизнес-процесс из 04-economics.md
| № | Шаг | Кто | Инструмент | Время | Стоимость (руб) | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор ICP-аккаунтов: банки, МФО, лизинг, факторинг | SDR + RevOps | CRM, HH/рынок, spreadsheets, enrichment | 1 рабочий день | 22 000 | 75% |
| 2 | Многошаговый outbound и выход на risk / credit decision maker | SDR | Email sequencing, Telegram, CRM | 10-14 дней касаний | 145 000 | 65% |
| 3 | Qualification call и проверка fit по потоку кейсов и стеку | AE | Meet/Zoom, CRM, AI notes | 1 час | 26 000 | 60% |
| 4 | Discovery и demo целевого workflow | AE + founder | Demo env, deck, ROI calculator | 1,5 часа | 42 000 | 45% |
| 5 | Scoping: формы отчётности, API, формат кредитного досье, compliance | Solutions architect + product lead | Notion/Jira, architecture docs, security questionnaire | 4-5 дней | 98 000 | 35% |
| 6 | Подготовка pilot proposal и бизнес-кейса | AE + founder + finance | Proposal docs, pricing model, ROI sheet | 2-3 дня | 86 000 | 45% |
| 7 | Pilot setup: загрузка отчётности, маппинг полей, настройка extraction | Implementation manager + ML engineer | ETL, OCR/LLM pipeline, sandbox | 2 недели | 260 000 | 50% |
| 8 | Валидация коэффициентов, human QA, tuning prompt/policy | Credit analyst SME + ML engineer | Review console, evals, annotation tools | 1-2 недели | 120 000 | 30% |
| 9 | Security / procurement / legal redlines | Founder + ops/legal | Contracting, DPA/SLA, procurement portal | 2-4 недели | 145 000 | 25% |
| 10 | Close won и handoff | AE + CSM | CRM, handoff checklist | 1 день | 38 000 | 65% |
| 11 | Production onboarding, обучение analyst team, роли и доступы | CSM + implementation manager | LMS, help center, admin console | 1 неделя | 72 000 | 55% |
| 12 | Первый production invoice и reconciliation оплаты | Finance ops | Billing, банк, ЭДО, бухгалтерия | 2-3 дня | 14 000 | 85% |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| CAC | 1 550 000 ₽ |
| customer_ltv_rub (по модели из 04-economics.md) | 26 176 471 ₽ |
| customer_ltv_rub, консервативный сценарий | 4 450 000 ₽ |
| customer_ltv_rub, базовый сценарий | 8 900 000 ₽ |
| customer_ltv_rub, оптимистичный сценарий | 22 250 000 ₽ |
| contribution_margin_rub_month | 445 000 ₽/мес на клиента |
| LTV/CAC | 16,9x |
| CAC Payback | 3,5 мес |
| Gross Margin | 65,4% |
| Break-even | 12 клиентов |
| startup_capital_to_bep_rub | 47 000 000 ₽ |
| Инвестиции до 1M EBITDA | 49 200 000 ₽ |

## Прибыль компании
- Формула: `company_ebitda_rub_month = N × 445 000 ₽ - fixed_costs_rub_month`
- При `fixed_costs_rub_month = 4 990 000 ₽` monthly break-even достигается на **12 клиентах**.
- `clients_to_500k_ebitda = 15` при scale-up fixed costs до 6,0 млн ₽ в базовом сценарии P&L.
- `months_to_500k_ebitda = 12` при траектории клиентов из `05-critic.md`.
- `clients_to_1m_ebitda = 16`.
- `months_to_1m_ebitda = 13` при продолжении той же траектории после месяца 12.
- Базовый P&L month 12: **15 клиентов, MRR 10 200 000 ₽, EBITDA 675 000 ₽**.
- Потенциал `company_ebitda_potential_rub_month` на 16 клиентах: **1 120 000 ₽/мес**.

## Команда для запуска
| Роль | Функция | Занятость | Зарплата (руб/мес) |
|---|---|---|---:|
| Founder / CEO | enterprise sales, ключевые сделки, партнёры | full | 320 000 |
| Product Lead | продуктовая стратегия, credit workflow design | full | 320 000 |
| ML / AI Engineer | extraction, prompts, evals, model orchestration | full | 340 000 |
| Backend / Integrations Engineer | API, LOS/CRM/BPM интеграции, data pipelines | full | 300 000 |
| Data / Document Engineer | парсинг отчётности, ETL, schema mapping | full | 260 000 |
| Credit Risk SME | правила анализа, QA policy, calibration | full | 250 000 |
| Account Executive | pipeline, demos, close | full | 280 000 |
| SDR / BDR | outbound prospecting | full | 160 000 |
| Implementation Manager | pilot setup, rollout, enablement | full | 220 000 |
| Customer Success Manager | adoption, renewals, expansion | full | 190 000 |
| Finance / Ops / Legal coordinator | billing, договоры, документооборот | full | 150 000 |
| DevOps / Security engineer | инфраструктура, доступы, аудит | 0,5 | 140 000 |

Итого fixed payroll: **2 930 000 ₽/мес**.

## Топ-3 риска
| Риск | Вероятность | Влияние |
|---|---|---:|
| Сдвиг в low-end pricing и давление на чек | средняя | 2 385 000 ₽/мес |
| Рост ручного QA и exception handling выше планового уровня | высокая | 1 275 000 ₽/мес |
| Удлинение enterprise sales cycle до 9-12 месяцев | средняя | 1 550 000 ₽/мес |

## Главная причина отклонения
Даже при сильной марже на одного клиента компания требует около **47,0-49,2 млн ₽** стартового капитала до устойчивого выхода в положительный операционный поток. Для модели с умеренным moat и высоким риском ценового давления со стороны incumbents это слишком капиталоёмкий путь к фондовому профилю.

## LTV Upside Calculator
**Сейчас: 62/100. Нужно ещё: 8 баллов до порога 70.**

| Критерий | Сейчас | Макс | Действие | Потенциал +баллов |
|---|---:|---:|---|---:|
| Прибыль компании / Unit Economics | 13/25 | 25/25 | Снизить `startup_capital_to_bep_rub` ниже 15 млн ₽ через paid pilots, setup fee 2,5-3,5 млн ₽ и более лёгкую delivery-модель, чтобы 500K EBITDA достигались без 47+ млн ₽ внешнего капитала | +6 |
| Конкурентное позиционирование | 7/15 | 15/15 | Доказать, что продукт выигрывает не только ценой, а скоростью underwriting decision, traceability и private contour, плюс получить 2-3 reference-кейса против incumbent alternatives | +4 |
| Барьеры входа | 6/10 | 10/10 | Закрепить on-prem/private contour, audit trail и интеграции в LOS/CRM как обязательный стандарт, а не кастомный опцион | +2 |
| Качество данных | 8/10 | 10/10 | Получить прямые данные по pilot conversion, paid discovery и renewal/usage, а также exact local demand feed вместо технического таймаута | +2 |

**Кратчайший путь до 70:** улучшить `Прибыль компании / Unit Economics` (+6) и `Конкурентное позиционирование` (+2 из возможных +4). Без этого кейс остаётся сильной enterprise-гипотезой, но не проходит инвестиционный порог по капиталоёмкости и defensibility.

## Финальный вывод
**REJECTED.**
Возвращаться к кейсу стоит только после доказательства, что setup fee и paid pilots заметно сокращают потребность в капитале, а первые клиенты подтверждают устойчивую цену и низкий уровень ручного QA. Сейчас экономика сделки хорошая, но экономика самой компании ещё слишком тяжёлая для одобрения.

---

## Этап 6 — История прохождения пайплайна
# 07-score-trajectory
## Кейс: ai-credit-analysis-corporate-financial-statements
## Начат: 2026-04-19

История прохождения пайплайна.

### 2026-04-19 — Программа 7 / Critic and verdict
- Статус: REJECTED
- Итоговый балл: 62/100
- Разбивка: спрос 16/20, экономика 13/25, масштаб 12/20, конкуренция 7/15, защита 6/10, данные 8/10
- LTV/CAC: 16,9x | CAC Payback: 3,5 мес | Break-even: 12 клиентов / месяц 9 по unit economics
- Стартовый капитал до BEP: 47 000 000 ₽
- Причина: Кейс подтверждает сильную economics на уровне одного enterprise-клиента, но требует около 47,0-49,2 млн ₽ стартового капитала до устойчивой положительной EBITDA и остаётся уязвимым к ценовому давлению со стороны incumbents.