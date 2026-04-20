# Investment Banking AI Analyst Operator v2 — Full Verdict Package
> Скомпилированный пакет стадий P2/P4/P5/P6/P7 для публикации в GitHub.
> Примечание: в этом rerun-кейсе отдельный `03-demand.md` отсутствует в исходном пайплайне, поэтому demand-стадия представлена файлом `02-demand.md`.

---

## Файл: 01-intake.md

---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-rerun-investment-banking-ai-analyst-operator.md
created: 2026-04-19T17:34:00+03:00
---

# 01-intake

## Кейс
investment-banking-ai-analyst-operator-v2

## Тип intake
rerun

## rerun_of
investment-banking-ai-analyst-operator

## Ссылка на оригинальный verdict
/home/node/.openclaw/repo/business-models/rejected/investment-banking-ai-analyst-operator__backup_2026-04-17_1655_msk/verdict.md

## Дата intake
2026-04-19, Europe/Moscow

## Полный контекст raw file

# RE-ANALYSIS REQUEST — Investment Banking AI Analyst Operator

## Meta
- previous_status: 🟡 NEAR-PASS
- previous_score: 67/100
- previous_sector: FINTECH
- previous_date: 2026-04-17
- source_folder: /business-models/rejected/investment-banking-ai-analyst-operator__backup_2026-04-17_1655_msk/
- reason_for_rerun: обновлены P4 (Source Tiering, TAM/SAM/SOM), P5 (Fully-loaded CAC, Hiring Realism), P6B (Monte Carlo Lite), P7 (Rubric 6×25, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner)

## Description (1 line)
Enterprise-кейс для investment banking и corporate finance почти проходит порог, но пока недостаточно доказаны repeatable спрос, масштабируемость и устойчивость premium pricing.

## Задача для intake-triage
1. Прочитай verdict.md предыдущего запуска (`/home/node/.openclaw/repo/business-models/rejected/investment-banking-ai-analyst-operator__backup_2026-04-17_1655_msk/verdict.md`) для контекста, но НЕ копируй результат — начни свежий анализ.
2. Создай новый кейс в pipeline/cases/investment-banking-ai-analyst-operator-v2/ и пройди полный пайплайн P3→P7 с новой рубрикой.
3. Сравни новый score с предыдущим (67/100) и запиши delta в финальный 06-verdict.md.

## Приоритет
p1 — batch re-run после обновления системы аналитики 2026-04-19.



---

## Файл: 02-demand.md

# 02-demand — Demand Validation

## Кейс
Investment Banking AI Analyst Operator, AI-native оператор для investment banking, M&A, private markets и corporate finance workflows: скрининг компаний, comps, memo drafting, due diligence support и synthesis по закрытому контуру.

## Итог
**Статус: CONDITIONAL PASS**

По exact-keyword спросу в открытом RU-поиске сигнал низкий, но денежный спрос подтверждён. Это не self-serve категория, а enterprise workflow purchase: банки и крупные финкоманды уже платят за данные, проверку контрагентов, финансовый анализ, due diligence и internal research tooling. Для такого кейса низкий search volume не является автоматическим reject, потому что покупка идёт из существующего бюджета investment / credit / corpfin / risk команд.

**Sources: T1 official buyer base and company pages; T2 adjacent paid substitutes and pricing; T3 internal demand API.**

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20AI%20analyst`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Дополнительные смежные проверки:

### `investment analyst AI`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **3**
- Yandex suggest: **2**

### `M&A AI analyst`
- Composite demand: **LOW**
- Demand score: **3**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **12**
- Yandex suggest: **2**

### `финансовый анализ ИИ инвестиционный аналитик`
- Composite demand: **LOW**
- Demand score: **3**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **39**
- Yandex suggest: **2**

### Интерпретация
Прямой массовый search-demand почти отсутствует, но это ожидаемо для узкой enterprise-категории. При этом в hh.ru по запросу `инвестиционный аналитик` видно **1 245 вакансий**, а в выдаче встречаются зарплатные вилки до **220 000 ₽/мес** и рядом стоящие финансово-аналитические роли **150 000–200 000 ₽/мес**. Это подтверждает, что ручной аналитический труд дорогой, а pain существует уже сейчас.

## 2. Реальные конкуренты и ценовые якоря

| Конкурент | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Контур.Фокус | Проверка контрагентов, скоринг, финанализ | **31 155 / 82 770 / 115 000 ₽** | Рынок уже платит за due diligence, скоринг и risk tooling |
| Rusprofile | Проверка компаний и физлиц | **940 / 1 990 ₽ в месяц** | Низкий сегмент данных commoditized, значит AI-оператор должен продаваться выше, как workflow outcome |
| Прима-Информ | Проверка контрагентов и API | **16 000 / 52 000 / 65 000 ₽ в год**, API **975 000 ₽ в год** | Даже data-only доступ в enterprise-режиме уже стоит около 1 млн ₽ в год |
| Cbonds | Данные по облигациям, акциям, отчетности, API/Data Feed | цена публично не раскрыта, доступ по заявке | Финансовые команды уже покупают отдельный research/data layer как рабочую инфраструктуру |
| Rogo | AI platform for finance professionals | цена публично не раскрыта, bespoke deployment | Западный market proof показывает, что AI-native financial workflow уже продаётся institutional buyers |

### Вывод по конкурентному полю
- Клиенты уже платят за **данные, скоринг, проверку контрагентов, финансовую отчетность, API и research stack**.
- Следовательно, AI-оператор для investment banking продаётся не как новый абстрактный AI-бюджет, а как более дорогой workflow layer поверх уже существующего spend.
- Для mid-market / enterprise чека **300 000–900 000 ₽/мес** гипотеза выглядит правдоподобно, если продукт закрывает не просто поиск данных, а memo/comps/diligence/output workflow.

## 3. Российский контур и buyers
По данным Банка России, на 18.04.2026 в РФ числится **359 действующих кредитных организаций**. Отдельно Банк России указывает **12 системно значимых кредитных организаций**, на которые приходится около **80%** активов сектора.

Это важно по двум причинам:
1. Покупательная способность концентрирована у ограниченного числа крупных financial buyers.
2. Даже несколько успешных enterprise-контрактов могут materially двигать выручку.

Прямой substitute в РФ, это не «AI investment banker» как отдельная коробка, а связка уже покупаемых решений:
- data terminals и market data,
- проверка контрагентов и бенефициаров,
- отчетность и финанализ,
- внутренние аналитики,
- консалтинг / advisory support,
- закрытые research pipelines внутри банков и корпораций.

### Вывод
Категория выглядит как **few buyers, high ACV**. Это хуже для массового спроса, но нормально для фонда, если economics и GTM выдерживают длинный enterprise цикл.

## 4. TAM / SAM / SOM в рублях

### Базовые допущения
- Беру midpoint чека: **500 000 ₽/мес** = **6 000 000 ₽/год** на клиента.
- Основной ICP: банки, investment / corpdev / strategy команды крупных компаний, private equity / debt / special situations, крупные advisory-практики.

### TAM
Широкий релевантный контур: **1 500** организаций и команд в РФ и русскоязычном enterprise-контуре, где возможен системный paid workflow вокруг инвестиционной аналитики.

**TAM = 1 500 × 6 000 000 ₽ = 9 млрд ₽/год**

### SAM
Реально адресуемый первый слой: **180** аккаунтов.
Сюда входят:
- системно значимые и крупные банки,
- сильные банки второго эшелона,
- крупные корпорации с активным corpdev,
- top advisory / PE / special situations контур.

**SAM = 180 × 6 000 000 ₽ = 1,08 млрд ₽/год**

### SOM
Ранний реалистичный слой: **8 контрактов**.

**SOM = 8 × 6 000 000 ₽ = 48 млн ₽/год**

### Вывод по рынку
Это не широкий горизонтальный SaaS-рынок, но для high-ticket enterprise оператора рынок достаточно большой. Даже при консервативном ICP несколько платных wins уже создают meaningful ARR.

## 5. WTP, доказательства готовности платить
1. **Контур.Фокус** уже продаёт скоринг и проверку контрагентов до **115 000 ₽** за тариф.
2. **Прима-Информ** берёт **975 000 ₽/год** только за API-доступ, без полного AI-workflow.
3. **Cbonds** позиционирует API/Data Feed как инструмент автоматизации процессов, значит отдельный data layer уже нормализован как бюджетная статья.
4. **Rogo** прямо позиционируется как AI platform for finance professionals и custom-deployed решение для ведущих финансовых институтов, что подтверждает category proof на более зрелом рынке.
5. **hh.ru** показывает большую базу вакансий `инвестиционный аналитик`, а значит ручной труд в этой функции дорогой и достаточно массовый для ROI-аргумента.

### Вывод по WTP
**WTP подтверждён.** Клиенты уже платят за adjacent-слой, внутри которого AI-оператор может забирать более высокий чек через speed-to-output, экономию analyst hours, лучшее покрытие источников и audit-friendly workflow.

## 6. Profit Gate
Нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Lean advisory operator
- Цена: **300 000 ₽/мес**
- GM: **55%**
- Валовая прибыль на клиента: **165 000 ₽/мес**
- Для fixed costs **2,0 млн ₽/мес** нужно **16 клиентов**

**Вердикт: CONDITIONAL PASS**

### Сценарий B. Base-case financial workflow operator
- Цена: **500 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **300 000 ₽/мес**
- Нужно **9 клиентов**

**Вердикт: PASS**

### Сценарий C. Enterprise private deployment
- Цена: **900 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **585 000 ₽/мес**
- Нужно **5 клиентов**

**Вердикт: PASS**

### Вывод по Profit Gate
На demand-stage кейс **не нужно отклонять**. Даже при длинном enterprise sales cycle существует правдоподобный путь к EBITDA выше 500k/mo, если продукт продаётся как secure workflow layer, а не как очередной data-subscription.

## 7. Общий вывод
- Search demand: **LOW по exact keyword**
- Adjacent enterprise demand: **есть**
- Публичные ценовые якоря: **есть**
- РФ buyers и substitutes: **есть**
- WTP: **подтверждён**
- Profit Gate: **проходит условно-позитивно**

## 8. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс можно переводить дальше в economics, потому что слабый публичный search-demand компенсируется дорогим ручным трудом, существующим spend на data/risk tooling и концентрированным пулом крупных buyers.

## Market Pulse
Market Pulse 19.04.2026: умеренно растущий интерес.

Обновление Market Pulse 19.04.2026: по текущим веб-сигналам интерес растёт, у financial AI workflows стало больше свежих публикаций и отраслевых обсуждений.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20AI%20analyst
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=investment%20analyst%20AI
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=M%26A%20AI%20analyst
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%84%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D0%98%D0%98%20%D0%B8%D0%BD%D0%B2%D0%B5%D1%81%D1%82%D0%B8%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA
- hh.ru, поиск `инвестиционный аналитик`: https://hh.ru/search/vacancy?text=%D0%B8%D0%BD%D0%B2%D0%B5%D1%81%D1%82%D0%B8%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA
- Банк России, список кредитных организаций на 18.04.2026: https://www.cbr.ru/banking_sector/credit/FullCoList/
- Банк России, системно значимые кредитные организации: https://www.cbr.ru/banking_sector/credit/SystemBanks.html
- Контур.Фокус, тарифы: https://focus.kontur.ru/site/price
- Rusprofile, тарифы: https://www.rusprofile.ru/subscribe
- Прима-Информ, тарифы: https://www.prima-inform.ru/services
- Cbonds: https://cbonds.ru/
- Rogo: https://rogo.ai/

Market Pulse 20.04.2026: растущий интерес.

Текущий веб-срез показывает рост интереса: в апреле 2026 года усилился поток новостей об использовании AI в банках и investment workflows.

> Market Pulse 2026-04-20: растущий интерес.


---

## Файл: 04-economics.md

# 04-economics

## Кейс
Investment Banking AI Analyst Operator, AI-native оператор для investment banking, M&A, private markets и corporate finance workflows.

## Economics verdict
**Статус: PASS WITH RESERVATIONS**

Demand-stage не дал массового search-demand, но для economics-stage это не критично: в модели продаётся не self-serve SaaS, а дорогой enterprise workflow с закрытым контуром, внедрением и длинным sales cycle. При консервативном fully-loaded CAC и hiring realism кейс проходит mandatory fund-level gates.

## Базовые допущения модели
- ICP: банки, крупные credit/risk/corpfin команды, инвестбанковские бутики, private markets teams.
- Модель выручки: enterprise subscription + внедрение; для unit economics считаю только recurring MRR.
- Средний контракт: **600 000 ₽ MRR на клиента**.
- Onboarding fee: **400 000 ₽** разово, в LTV не включаю, чтобы не завышать модель.
- Сегмент CAC: **regulated / enterprise B2B fintech**, поэтому применяю повышенную нагрузку на GTM и overhead.
- Churn: беру **1,5% logo churn / мес** как консервативную оценку между upper mid-market и enterprise benchmark, потому что ACV высокий, интеграции глубокие, но российский fintech procurement длинный и неидеально sticky.

## Источники и benchmarks
1. `02-demand.md` текущего кейса, публичные ценовые якоря Контур.Фокус / Rusprofile / Прима-Информ / Rogo.
2. Optifai, benchmark churn по ACV: enterprise >$100K ACV показывает **0,7% monthly logo churn**, upper mid-market $50K-$100K, **1,3%**. Для кейса использую **1,5%** как более строгую локальную поправку: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
3. HH.ru, вакансии и salary anchors для Москвы/СПб, 2026: senior backend, account executive и смежные роли.
   - https://hh.ru/vacancies/senior-backend-engineer
   - https://hh.ru/vacancies/account_executive
4. Встроенные sanity-бенчмарки фонда из задания: enterprise SaaS B2B РФ **300-900K ₽ CAC**, regulated fintech **200-700K ₽**, но для сложного enterprise motion с pilot/legal/security review допустимо выходить выше generic benchmark.

## 1. Подробный business process, от lead до payment

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам и corpfin командам | SDR + Revenue Ops | HH/СПАРК/ручной ресерч/CRM | 2 ч на аккаунт | 2 500 | Средняя |
| 2 | Enrichment контактов, квалификация лиц принимающих решение | SDR | CRM + email enrichment + LinkedIn analog | 1,5 ч | 1 900 | Средняя |
| 3 | Outbound sequence, cold email/call/Telegram/intro | SDR | Outreach stack + телефония | 3 недели | 12 000 | Средняя |
| 4 | Discovery call, pain mapping, qualification | AE + founder/CEO | VC/Meet, CRM | 1 ч + prep | 8 500 | Низкая |
| 5 | Demo на реальных документах / comps / memo workflow | AE + Solutions analyst | Demo env, secure sandbox | 3-5 дней | 18 000 | Низкая |
| 6 | Security review и legal scoping | CTO + security/compliance + buyer IT | VDR, policy docs, DPA/NDA | 2-4 недели | 45 000 | Низкая |
| 7 | Pilot setup в закрытом контуре | CTO + backend + ML + solutions analyst | VPC, connectors, prompt/eval stack | 3-6 недель | 140 000 | Средняя |
| 8 | Pilot сопровождение, weekly steering | AE + solutions analyst + CSM | Jira/Notion/CRM | 1 месяц | 85 000 | Низкая |
| 9 | Procurement, закупка, согласование MSA/SOW | AE + CEO + legal | ЭДО/договорной workflow | 2-6 недель | 60 000 | Низкая |
| 10 | Invoice issuance / акт / payment collection | Finance/Ops | 1С/банк/ЭДО | 3-5 дней | 7 000 | Средняя |
| 11 | Go-live и monthly success cadence | CSM + product + CTO | CRM, product analytics | ongoing | 28 000/мес | Средняя |

### Вывод по процессу
- Продажа тяжёлая, с множеством ручных касаний.
- Узкое место не генерация лида, а **pilot + security + procurement**.
- Поэтому raw ad CAC здесь бессмысленен, нужен **fully-loaded CAC** с учётом sales FOT, tools, events и overhead.

## 2. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM/API inference | 70 000 | Консервативный бюджет на heavy document + memo workflows | Высокая вариативность по usage |
| Market/company data и API | 55 000 | Платный data layer + контрагентские/финансовые источники | Критичный cost driver |
| Secure infra / VPC / storage | 30 000 | Выделенный защищённый контур, логирование, storage | Для fintech обязателен |
| Implementation amortization | 40 000 | 480K ₽ onboarding cost, размазан на 12 мес | Не занижаю delivery cost |
| Customer success / support | 28 000 | Доля CSM и analyst-support на аккаунт | При low-volume enterprise |
| QA / compliance / audit | 15 000 | Внутренние проверки качества и traceability | Регулируемый контур |
| Billing / legal / procurement admin | 7 000 | ЭДО, актирование, финоперации | Небольшой, но реальный cost |
| **Итого COGS** | **245 000** |  |  |
| **MRR на клиента** | **600 000** |  |  |
| **Contribution / client / month** | **355 000** | 600 000 - 245 000 |  |
| **Contribution Margin** | **59,2%** | 355 000 / 600 000 |  |

## 3. CAC по каналам с funnel conversion

### CAC по каналам, до blended

| Канал | Monthly input | Meeting rate | Pilot rate | Paid conversion | New paying / мес | Monthly spend, ₽ | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / ABM | 120 target accounts | 20% = 24 meetings | 33% = 8 pilots | 25% = 2 paid | 2,0 | 1 800 000 | 900 000 |
| Партнёрства / SI / referral | 20 qualified intros | 40% = 8 meetings | 50% = 4 pilots | 50% = 2 paid | 1,0 | 780 000 | 780 000 |
| Events + thought leadership | 60 inbound/MQL | 20% = 12 meetings | 33% = 4 pilots | 25% = 1 paid | 1,0 | 1 200 000 | 1 200 000 |
| **Blended** |  |  |  |  | **4,0** | **3 780 000** | **945 000 raw CAC** |

### Fully-loaded CAC, обязательный расчёт

Формула фонда:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT + Marketing FOT allocation + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads / paid promotion / sponsored content | 180 000 | Таргетированный B2B demand gen, узкий сегмент | внутреннее допущение для enterprise GTM |
| Outbound team FOT, attributed to new | 650 000 | SDR 200K gross + AE 300K gross + переменная часть 50K, всё с 30% взносами | HH.ru benchmark + модель фонда |
| Marketing team FOT, partial allocation | 195 000 | PMM / founder marketing 150K gross × 1,3 | HH.ru benchmark + аллокация времени |
| Tools / CRM / sequencing / enrichment / call stack | 127 000 | CRM, outreach, enrichment, call recording, analytics | стек enterprise GTM |
| Events / partnerships | 420 000 | 1 отраслевое событие + travel + partner enablement | консервативный enterprise budget |
| **Subtotal before overhead** | **1 572 000** |  |  |
| Overhead multiplier **x1,3** | **471 600** | 30% на management overhead / legal / shared ops | стандарт фонда для enterprise B2B |
| **Total acquisition cost / мес** | **2 043 600** |  |  |
| New paying customers / мес | **1,5** | консервативный steady-state для regulated enterprise motion | модель автора |
| **Fully-loaded blended CAC** | **1 362 400 ₽** | 2 043 600 / 1,5 | итог |

### Sanity check по CAC
- Benchmark из задания для enterprise SaaS РФ: **300-900K ₽**.
- Benchmark для regulated fintech: **200-700K ₽**.
- Наша оценка **1,36 млн ₽** выше generic benchmark, но это объяснимо, потому что кейс сочетает enterprise sales, security review, pilot и procurement. Для такого motion низкий CAC был бы красным флагом, а не преимуществом.

## 4. LTV с churn rate

### Выбор churn
Источник benchmark: Optifai показывает **0,7% monthly churn** для enterprise и **1,3%** для upper mid-market по 939 B2B SaaS компаниям. Для текущего кейса беру **1,5% / мес**, то есть хуже benchmark, потому что:
- ACV высокий, но не всегда выше $100K,
- продажи в РФ более фрагментированы,
- есть regulatory и procurement friction,
- продукт внедряется глубоко, но category ещё не fully mature.

### Расчёт LTV
- MRR = **600 000 ₽**
- Contribution Margin = **59,2%**
- Monthly churn = **1,5%**
- **LTV = 600 000 × 59,2% / 1,5% = 23 680 000 ₽**

## 5. LTV/CAC ratio
- LTV = **23,68 млн ₽**
- Fully-loaded CAC = **1,362 млн ₽**
- **LTV/CAC = 17,4x**

Итог: существенно выше инвестиционного порога **3:1**.

## 6. CAC Payback
По формуле фонда:
- **CAC Payback = CAC / MRR per customer = 1 362 400 / 600 000 = 2,27 месяца**

Дополнительная консервативная проверка по contribution:
- **1 362 400 / 355 000 = 3,84 месяца**

Обе версии значительно лучше лимита **<12 мес**, даже для enterprise motion.

## 7. Contribution Margin %
- Revenue per client = **600 000 ₽/мес**
- COGS per client = **245 000 ₽/мес**
- Contribution = **355 000 ₽/мес**
- **Contribution Margin = 59,2%**

Для AI-heavy fintech workflow это не блестящая, но рабочая маржа. Главный риск, data/API и кастомизация, а не marketing burn.

## 8. Full team table, роли, функции, зарплаты

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---:|---:|
| CEO | 1 | Продажи top accounts, fundraising, партнёрства | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | Архитектура, security, private deployment | 600 000 | 180 000 | 780 000 |
| Senior Backend | 2 | Интеграции, data pipelines, backend | 450 000 | 135 000 | 1 170 000 |
| ML Engineer | 1 | Retrieval, evals, prompt/agent quality | 550 000 | 165 000 | 715 000 |
| DevOps | 1 | VPC, CI/CD, observability, access control | 350 000 | 105 000 | 455 000 |
| Frontend | 1 | Analyst UI, workbench, approval layer | 300 000 | 90 000 | 390 000 |
| Product Manager | 1 | Workflow design, roadmap, pilot feedback loop | 350 000 | 105 000 | 455 000 |
| AI Solutions Analyst | 1 | Demo, пилоты, onboarding, analytic QA | 320 000 | 96 000 | 416 000 |
| SDR | 1 | Outbound prospecting | 200 000 | 60 000 | 260 000 |
| AE | 1 | Discovery, demo, close, procurement | 350 000 | 105 000 | 455 000 |
| Customer Success | 1 | Retention, upsell, adoption | 250 000 | 75 000 | 325 000 |
| Finance / Ops | 1 | Документы, биллинг, finance ops | 180 000 | 54 000 | 234 000 |
| **Итого** | **13** |  |  |  | **6 500 000 ₽/мес** |

## 9. Hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 200 000 | 0,5-1 | 1 | 60 000 | 260 000 |
| AE | 1 | 350 000 | 1-2 | 2-3 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product Manager | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| AI Solutions Analyst | 1 | 320 000 | 1 | 1 | 96 000 | 416 000 |
| Finance/Ops | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |

### Комментарий
- Hire-plan не нарушает sanity check: **в первый месяц нет найма 5+ человек**.
- FOT для команды 5-7 человек быстро уходит выше **4 млн ₽/мес**, то есть дешёвый старт здесь нереалистичен.
- Это enterprise fintech build, не lean-гаражный SaaS.

## 10. Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO, CTO, Product | 2 080 000 | founder/core team |
| M2 | + Senior Backend #1 | 2 665 000 | backend ещё в ramp |
| M3 | + Senior Backend #2, ML, DevOps | 4 420 000 | core platform team собрана |
| M4 | + Frontend, AI Solutions Analyst | 5 226 000 | готовность к pilot delivery |
| M5 | + SDR | 5 486 000 | GTM начинает разгон |
| M6 | + AE | 5 941 000 | sales motion становится repeatable |
| M7 | + Customer Success | 6 266 000 | retention motion появляется заранее |
| M8 | + Finance/Ops | 6 500 000 | full base team готова |
| M9 | без изменений | 6 500 000 | steady state |
| M10 | без изменений | 6 500 000 | steady state |
| M11 | без изменений | 6 500 000 | steady state |
| M12 | без изменений | 6 500 000 | steady state |

## 11. Fixed costs breakdown

| Fixed cost item | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 6 500 000 | таблица выше |
| Office / remote / equipment / admin | 350 000 | гибридный режим |
| Shared infra, observability, internal tools | 420 000 | не client-specific часть |
| Legal / compliance / audit retainers | 180 000 | fintech overhead |
| Travel / enterprise selling | 120 000 | встречи и отраслевые мероприятия |
| Security advisor / external audit support | 90 000 | частично аутсорс |
| Misc reserve | 60 000 | непредвиденные ops |
| **Итого fixed costs / мес** | **7 720 000** |  |

## 12. Break-even по количеству клиентов и по месяцам

### По количеству клиентов
- Contribution на клиента: **355 000 ₽/мес**
- Fixed costs: **7 720 000 ₽/мес**
- **Break-even clients = 7 720 000 / 355 000 = 21,75**, округляю до **22 клиентов**

### По месяцам, на base ramp
Предполагаемый платящий клиентский ramp:
- M5: 1
- M6: 2
- M7: 3
- M8: 5
- M9: 7
- M10: 10
- M11: 13
- M12: 16
- M13: 18
- M14: 20
- M15: 22

Следовательно, **operating break-even достигается около M15**.

## 13. Burn-to-breakeven

| Месяц | Клиентов | EBITDA / мес, ₽ |
|---|---:|---:|
| M1 | 0 | -3 300 000 |
| M2 | 0 | -3 885 000 |
| M3 | 0 | -5 640 000 |
| M4 | 0 | -6 446 000 |
| M5 | 1 | -6 351 000 |
| M6 | 2 | -6 451 000 |
| M7 | 3 | -6 421 000 |
| M8 | 5 | -5 945 000 |
| M9 | 7 | -5 235 000 |
| M10 | 10 | -4 170 000 |
| M11 | 13 | -3 105 000 |
| M12 | 16 | -2 040 000 |
| M13 | 18 | -1 330 000 |
| M14 | 20 | -620 000 |
| M15 | 22 | +90 000 |

**Burn to break-even ≈ 60,9 млн ₽** накопленного отрицательного EBITDA.

## 14. Cash runway

Берём **startup_capital = 70 млн ₽**.

- Средний burn M1-M12 ≈ **4,63 млн ₽/мес**
- Runway по среднему burn ≈ **15,1 месяца**
- Break-even в base case: **M15**
- Запас над burn-to-breakeven: примерно **9,1 млн ₽**

Вывод: проект капиталоёмкий, но не абсурдно капиталоёмкий для enterprise fintech SaaS. Запуск с капиталом ниже **55-60 млн ₽** выглядел бы рискованно.

## 15. Profit Gate фонда

### Проверка LTV/CAC
- Требование: **>= 3,0x**
- Факт: **17,4x**
- **PASS**

### Проверка CAC Payback
- Требование: обычно **<12 мес**, enterprise допустимо до **18 мес**
- Факт: **2,27 мес по MRR**, **3,84 мес по contribution**
- **PASS**

### Проверка EBITDA при 50 клиентах
- EBITDA = 50 × 355 000 - 7 720 000 = **10 030 000 ₽/мес**
- Требование: **достижимо >=500K ₽/мес при 50 клиентах**
- **PASS**

## 16. Итоговый вывод
Экономика кейса **проходит investment-grade P5**, хотя модель тяжёлая по GTM и требует серьёзного стартового капитала. Слабое место здесь не unit economics клиента, а company-building risk:
- длинный pilot-to-paid цикл,
- дорогой talent stack,
- высокая зависимость от enterprise procurement,
- риск price compression, если продукт станет восприниматься как «ещё один AI assistant», а не как workflow system of record.

Но mandatory reject-триггер на P5 **не срабатывает**:
- LTV/CAC значительно выше **1:1** и выше **3:1**,
- EBITDA при **50 клиентах** сильно положительная,
- break-even достигается до 24 месяцев в реалистичной модели.


---

## Файл: 05-critic.md

# SECTION A — PnL

## A1. Исходные допущения

- ARPA: **600 000 ₽ / клиент / мес**
- COGS: **245 000 ₽ / клиент / мес**
- Gross profit: **355 000 ₽ / клиент / мес**
- Contribution margin: **59,2%**
- Fixed costs: **7 720 000 ₽ / мес**
- Team FOT fully-loaded: **6 500 000 ₽ / мес**
- Страховые взносы: **~30% к ФОТ**, уже включены в fully-loaded FOT
- CAC по каналам:
  - Founder-led outbound / ABM: **900 000 ₽**
  - Партнёрства / SI / referral: **780 000 ₽**
  - Events + thought leadership: **1 200 000 ₽**
  - Fully-loaded blended CAC: **1 362 400 ₽**
- LTV: **23 680 000 ₽**
- Logo churn benchmark в базовой модели: **1,5% / мес**
- Break-even по client count: **22 клиента**

Сценарные допущения для PnL:
- **Base:** churn **1,5% / мес**, new clients: **0, 0, 0, 1, 1, 2, 3, 3, 4, 4, 5, 5**
- **Optimistic:** churn **1,0% / мес**, new clients: **0, 0, 1, 1, 2, 3, 3, 4, 4, 5, 5, 6**
- **Pessimistic:** churn **2,5% / мес**, new clients: **0, 0, 0, 0, 1, 1, 2, 2, 2, 3, 3, 3**
- Формула active clients: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`
- Cumulative cash ниже, это накопленный EBITDA без учёта оборотного капитала, CAPEX и внешнего финансирования

## A2. 12-month PnL — Base scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 | 5 | 5 |
| Total clients | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 4,0 | 6,9 | 9,8 | 13,6 | 17,4 | 22,2 | 26,8 |
| MRR, ₽ | 0 | 0 | 0 | 600 000 | 1 191 000 | 2 373 135 | 4 137 538 | 5 875 475 | 8 187 343 | 10 464 533 | 13 307 565 | 16 107 951 |
| COGS, ₽ | 0 | 0 | 0 | 245 000 | 486 325 | 969 030 | 1 689 495 | 2 399 152 | 3 343 165 | 4 273 017 | 5 433 922 | 6 577 413 |
| Gross profit, ₽ | 0 | 0 | 0 | 355 000 | 704 675 | 1 404 105 | 2 448 043 | 3 476 323 | 4 844 178 | 6 191 515 | 7 873 642 | 9 530 538 |
| GM% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% |
| Fixed costs, ₽ | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 |
| EBITDA, ₽ | -7 720 000 | -7 720 000 | -7 720 000 | -7 365 000 | -7 015 325 | -6 315 895 | -5 271 957 | -4 243 677 | -2 875 822 | -1 528 485 | 153 642 | 1 810 538 |
| Cash burn, ₽ | 7 720 000 | 7 720 000 | 7 720 000 | 7 365 000 | 7 015 325 | 6 315 895 | 5 271 957 | 4 243 677 | 2 875 822 | 1 528 485 | 0 | 0 |
| Cumulative cash, ₽ | -7 720 000 | -15 440 000 | -23 160 000 | -30 525 000 | -37 540 325 | -43 856 220 | -49 128 177 | -53 371 854 | -56 247 676 | -57 776 161 | -57 622 519 | -55 811 981 |

**Base break-even:**
- Break-even client count: **22 клиента**
- Break-even month: **M11**
- startup_capital_to_bep_rub: **57 776 161 ₽**

## A3. 12-month PnL — Optimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 | 5 | 5 | 6 |
| Total clients | 0,0 | 0,0 | 1,0 | 2,0 | 4,0 | 6,9 | 9,9 | 13,8 | 17,6 | 22,4 | 27,2 | 33,0 |
| MRR, ₽ | 0 | 0 | 600 000 | 1 194 000 | 2 382 060 | 4 158 239 | 5 916 657 | 8 257 490 | 10 574 916 | 13 469 166 | 16 334 475 | 19 771 130 |
| COGS, ₽ | 0 | 0 | 245 000 | 487 550 | 972 674 | 1 697 948 | 2 415 968 | 3 371 809 | 4 318 091 | 5 499 910 | 6 669 911 | 8 073 211 |
| Gross profit, ₽ | 0 | 0 | 355 000 | 706 450 | 1 409 386 | 2 460 292 | 3 500 689 | 4 885 682 | 6 256 825 | 7 969 257 | 9 664 564 | 11 697 919 |
| GM% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% |
| Fixed costs, ₽ | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 |
| EBITDA, ₽ | -7 720 000 | -7 720 000 | -7 365 000 | -7 013 550 | -6 310 614 | -5 259 708 | -4 219 311 | -2 834 318 | -1 463 175 | 249 257 | 1 944 564 | 3 977 919 |
| Cash burn, ₽ | 7 720 000 | 7 720 000 | 7 365 000 | 7 013 550 | 6 310 614 | 5 259 708 | 4 219 311 | 2 834 318 | 1 463 175 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -7 720 000 | -15 440 000 | -22 805 000 | -29 818 550 | -36 129 164 | -41 388 873 | -45 608 184 | -48 442 502 | -49 905 677 | -49 656 420 | -47 711 856 | -43 733 938 |

**Optimistic break-even:**
- Break-even client count: **22 клиента**
- Break-even month: **M10**
- startup_capital_to_bep_rub: **49 905 677 ₽**

## A4. 12-month PnL — Pessimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 3,9 | 5,8 | 7,7 | 10,5 | 13,2 | 15,9 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 600 000 | 1 185 000 | 2 355 375 | 3 496 491 | 4 609 078 | 6 293 851 | 7 936 505 | 9 538 092 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 245 000 | 483 875 | 961 778 | 1 427 734 | 1 882 040 | 2 569 989 | 3 240 740 | 3 894 721 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 355 000 | 701 125 | 1 393 597 | 2 068 757 | 2 727 038 | 3 723 862 | 4 695 766 | 5 643 371 |
| GM% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% | 59,2% |
| Fixed costs, ₽ | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 |
| EBITDA, ₽ | -7 720 000 | -7 720 000 | -7 720 000 | -7 720 000 | -7 365 000 | -7 018 875 | -6 326 403 | -5 651 243 | -4 992 962 | -3 996 138 | -3 024 234 | -2 076 629 |
| Cash burn, ₽ | 7 720 000 | 7 720 000 | 7 720 000 | 7 720 000 | 7 365 000 | 7 018 875 | 6 326 403 | 5 651 243 | 4 992 962 | 3 996 138 | 3 024 234 | 2 076 629 |
| Cumulative cash, ₽ | -7 720 000 | -15 440 000 | -23 160 000 | -30 880 000 | -38 245 000 | -45 263 875 | -51 590 278 | -57 241 521 | -62 234 483 | -66 230 621 | -69 254 856 | -71 331 484 |

**Pessimistic break-even:**
- Break-even client count: **22 клиента**
- Break-even month: **M15**
- startup_capital_to_bep_rub: **72 736 092 ₽**

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### A5.1. На 1 активного клиента в месяц

| Метрика | ₽ / клиент / мес | Комментарий |
|---|---:|---|
| ARPA | 600 000 | месячная выручка на клиента |
| Gross profit | 355 000 | после COGS 245 000 ₽ |
| Contribution | 355 000 | delivery costs уже заложены в COGS |
| EBITDA at break-even scale | 4 091 | аллокация fixed costs = 350 909 ₽ на клиента при 22 клиентах |
| Net, УСН 6% | -31 909 | налог 6% с выручки = 36 000 ₽ |
| Net, IT-льгота 3% | -13 909 | налог 3% с выручки = 18 000 ₽ |
| Net, ОСНО 20% | 3 273 | 20% налог на прибыль при положительной прибыли |

### A5.2. На масштабе 50 активных клиентов

| Метрика | ₽ / мес |
|---|---:|
| MRR | 30 000 000 |
| COGS | 12 250 000 |
| Gross profit | 17 750 000 |
| Contribution | 17 750 000 |
| EBITDA | 10 030 000 |
| Net, УСН 6% | 8 230 000 |
| Net, IT-льгота 3% | 9 130 000 |
| Net, ОСНО 20% | 8 024 000 |

### A5.3. M12 waterfall по сценариям

| Scenario | M12 clients | Gross profit, ₽ | EBITDA pre-tax, ₽ | Net, IT 3%, ₽ | Net, УСН 6%, ₽ | Net, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Base | 26,8 | 9 530 538 | 1 810 538 | 1 327 299 | 844 061 | 1 448 430 |
| Optimistic | 33,0 | 11 697 919 | 3 977 919 | 3 384 785 | 2 791 652 | 3 182 336 |
| Pessimistic | 15,9 | 5 643 371 | -2 076 629 | -2 362 772 | -2 648 915 | -2 076 629 |

## A6. Cash flow и startup_capital_to_bep_rub

- **Base:** **57 776 161 ₽**
- **Optimistic:** **49 905 677 ₽**
- **Pessimistic:** **72 736 092 ₽**

## A7. Налоговая модель РФ

#### 1) УСН 6%
- Налог считается как **6% от выручки**
- Удобно для early stage, но ухудшает cash flow, потому что платится даже при отрицательной операционной прибыли

#### 2) IT-льгота / аккредитация Минцифры
- В модели беру **3% от выручки** как льготный сценарий по условию задания
- Это целевой режим для software-компании при наличии аккредитации и нужной доли профильной выручки

#### 3) ОСНО
- Налог на прибыль: **20%**
- **НДС 20%** применим при работе на ОСНО и должен учитываться отдельно в cash flow и pricing, но в PnL выше НДС не включён в выручку

#### 4) Страховые взносы
- В модели уже отражены как **~30% к ФОТ**
- Поэтому team FOT и fixed costs считаются fully-loaded

**Вывод по налогам:** предпочтительный режим для модели, **IT-льгота 3%**. Рабочий fallback, **УСН 6%**. ОСНО имеет смысл при требованиях клиента к НДС и стандартному procurement-flow.

## A8. Break-even summary

| Scenario | Break-even client count | Break-even month | Startup capital to BEP, ₽ |
|---|---:|---:|---:|
| Base | 22 | 11 | 57 776 161 |
| Optimistic | 22 | 10 | 49 905 677 |
| Pessimistic | 22 | 15 | 72 736 092 |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 мес

Беру базу из SECTION A: M12 EBITDA = **1 810 538 ₽/мес**, M12 active clients = **26,8**, contribution/client = **355 000 ₽/мес**.

Допущения для stress-test:
- **Sens1, CAC x2:** при том же GTM-бюджете acquisition efficiency падает примерно в 2 раза, поэтому M12 active clients снижаются до **~13,4**.
- **Sens2, Churn x2:** churn растёт с **1,5%** до **3,0%/мес**, new-logo ramp сохраняю.
- **Sens3, Price -30%:** ARPU падает с **600 000 ₽** до **420 000 ₽**, COGS сохраняю, contribution/client падает до **175 000 ₽/мес**.

| Scenario | Key change | Active clients @M12 | Contribution / client, ₽/мес | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без изменений | 26,8 | 355 000 | **1 810 538** | базовая модель проходит в плюс к M11-M12 |
| Sens1 | CAC x2 | 13,4 | 355 000 | **-2 962 231** | рост CAC ломает ramp и сдвигает break-even далеко за 12 мес |
| Sens2 | Churn x2 | 25,2 | 355 000 | **1 226 000** | модель остаётся живой, но запас прочности резко падает |
| Sens3 | Price -30% | 26,8 | 175 000 | **-3 030 000** | price compression почти сразу делает unit economics хрупкой |

**Вывод:** главный риск не churn сам по себе, а **price compression + ухудшение acquisition efficiency**. Именно они быстрее всего уводят модель в отрицательный EBITDA.

## B2. Monte Carlo Lite, confidence intervals

Вместо single-point base/opt/pess использую треугольные диапазоны по ключевым драйверам и считаю **упрощённые 9 комбинаций** вокруг worst / median / best. Это не буквальная 1000-итерационная симуляция, но достаточный risk envelope для IC.

### B2.1. Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 900 000 | 1 362 400 | 2 700 000 | [T2][T3] |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | [T3] |
| ARPU, ₽/мес | 420 000 | 600 000 | 900 000 | [T2][T3] |
| Conversion rate lead→paid, % | 15% | 25% | 40% | [T3] |
| Time-to-hire, мес | 0,5 | 1,3 | 2,5 | [T3] |

Где:
- **[T2]** = `02-demand.md`, публичные ценовые якоря и enterprise WTP.
- **[T3]** = `04-economics.md`, текущая unit economics, funnel и hiring realism.

### B2.2. p10 / p50 / p90

Для M24 беру как базовую точку **50 активных клиентов** и EBITDA **10 030 000 ₽/мес** из `04-economics.md`. Далее stress / upside считаю через изменение ARPU, churn, CAC и скорости наращивания клиентской базы.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-4 570 000** | **10 030 000** | **38 130 000** | **42 700 000** |
| CAC payback (мес) | **6,4** | **2,27** | **1,0** | **5,4** |
| LTV/CAC | **2,2x** | **17,4x** | **72,8x** | **70,6x** |
| Cash runway (мес) | **9** | **15** | **27** | **18** |

### B2.3. Интерпретация Monte Carlo Lite

1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: risk of insolvency**.
2. **p50 EBITDA > 500К ₽/мес**, значит median-case EBITDA gate проходит.
3. Диапазон **LTV/CAC слишком широкий, 2,2x → 72,8x**, это явный признак хрупкости assumptions по pricing, churn и acquisition.
4. По сути модель остаётся investable только если команда удерживает одновременно:
   - premium pricing,
   - churn не выше ~1,5-2,0%/мес,
   - и enterprise CAC без затяжного разъезда выше ~2 млн ₽.

## B3. Competitor deep-dive

### B3.1. Западные конкуренты

| Компания | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Rogo** | AI platform для investment banking, PE, asset management | Узкий vertical focus, сильный category fit для finance, enterprise-grade deployment | Вероятно дорогой и ориентирован на Tier-1 западные команды, слабее fit под РФ data/compliance контур | **~5-8%** emerging AI-finance-workflow сегмента на Западе | Локальный data stack, русскоязычный workflow, lower-cost deployment для СНГ/РФ |
| **AlphaSense** | Search + market intelligence + research copilot для finance и corpdev | Очень сильный data moat, бренд, distribution, широкое покрытие research use cases | Больше intelligence terminal, чем execution workflow; дорогой, тяжёлый, не локализован под РФ | **~15-20%** global AI-enabled market-intelligence segment | Можем продавать не terminal, а output-layer: memo, comps, DD и secure custom workflow |
| **Hebbia** | AI knowledge work / document reasoning для finance, legal, PE | Сильный narrative around deep research over large docs, хорошо ложится на diligence workflows | Риск generalist-позиционирования, высокая зависимость от enterprise adoption speed | **~3-5%** fast-growing AI diligence/copilot niche | Больше локального domain tailoring под investment / corpfin в РФ, проще кастомизация под закрытый контур |

### B3.2. Российские конкуренты и substitutes

| Компания | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Контур.Фокус** | Проверка контрагентов, бенефициаров, арбитраж, финпрофиль | Сильный бренд, широкий SMB/mid-market reach, понятный procurement | Не закрывает end-to-end memo/comps workflow и investment-banking analyst job-to-be-done | **~20-25%** РФ due-diligence / контрагентский SMB-mid segment | Мы продаём workflow output, а не только справку по юрлицу |
| **Rusprofile** | Массовая база по компаниям и физлицам | Огромный top-of-funnel, дешёвый entry price, высокая узнаваемость | Commoditized data layer, слабее enterprise customization и аналитическая глубина | **~25-35%** массового self-serve сегмента проверки компаний | Мы сильнее там, где нужен secure enterprise reasoning и analyst-ready deliverable |
| **СПАРК-Интерфакс** | Премиальная risk / due diligence / комплаенс аналитика | Глубокий enterprise trust, сильный procurement fit в крупных компаниях | Дорогой и скорее data/risk system, чем AI workflow operator | **~20-30%** крупного enterprise / regulated сегмента | Можем быть поверх СПАРК как action layer и AI analyst cockpit |
| **Прима-Информ** | Проверка контрагентов, API, корпоративные справки | API-first контур, адекватный entry price для data access | Слабее бренд и workflow-layer, чем у лидеров | **~5-10%** data/API niche | Наш выигрыш в synthesis, memo drafting и explainable analyst output |
| **Cbonds** | Рынок облигаций, эмитенты, отчётность, data feed | Сильный finance-specific data asset, привычен профучастникам | Узкий фокус на market data, не заменяет AI-оператора для DD/comps/memo | **~10-15%** fixed-income / capital-markets data niche | Мы собираем multi-source workflow, а не один data vertical |

### B3.3. Конкурентный вывод

- На Западе category proof уже есть, значит это **не выдуманный рынок**.
- В РФ прямой AI-native лидер ещё не закрепился, но substitutes очень сильные.
- Поэтому реальный вход не через «лучше ищем документы», а через **быстрее делаем memo/comps/DD в закрытом контуре с audit trail**.
- Самая опасная конкурентная позиция для нас, это не Rusprofile, а связка **СПАРК/Контур + внутренний analyst team + generic LLM**.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного ML/Backend лидера вовремя | med | Срыв roadmap и пилотов на 2-3 мес | time-to-hire > 2,5 мес, офферы проигрываются | founder-led recruiting, заранее pipeline кандидатов, advisor bench |
| Operational | LLM/API latency или деградация качества на длинных документах | high | Падает trust у analysts, pilot не конвертится | рост ручных правок, complaint rate > 20% | fallback-model stack, eval harness, human approval layer |
| Operational | Срыв private deployment / VPC интеграций | med | Delay go-live и cash collection | security review тянется > 6 недель | reference architecture, prebuilt connectors, paid pilot scope freeze |
| Market | Спрос концентрирован в слишком узком числе buyers | med | pipeline волатильный, revenue lumpy | <10 qualified enterprise accounts в квартал | расширение ICP в corpdev, PE, special sits, advisory |
| Market | Price compression из-за generic LLM и low-cost assistants | high | ARPU падает на 20-30% и ниже | скидки > 15% уже на первых переговорах | value-based pricing, packaged use cases, ROI calculator |
| Market | Конкуренты добавляют AI-слой поверх существующих data terminals | high | CAC растёт, win-rate падает | участились проигрыши СПАРК/AlphaSense/generic copilots | позиционирование как secure action/workflow layer, не data terminal |
| Regulatory | Требования 152-ФЗ и data residency мешают облачному развёртыванию | high | потеря части regulated клиентов | security/legal asks по on-prem/VPC уже на presale | on-prem/VPC SKU, локальное хранение, DPA и security docs заранее |
| Regulatory | 115-ФЗ / KYC / audit traceability требований не хватает | med | reject на комплаенс-этапе | buyer asks for explainability, lineage, immutable logs | audit logs, source citations, approval workflow |
| Regulatory | Санкции или ограничения на западные SaaS/LLM vendors | high | отключение части стека и рост cost-to-serve | vendor instability, billing failures, geo restrictions | multi-vendor stack, open-source fallback, локальные модели |
| Financial | Runway съедается раньше break-even из-за длинного pilot-to-paid | high | нужен down round или bridge | cash runway < 9 мес, collection delays | tranche budgeting, pilot monetization, hard hiring gates |
| Financial | Ослабление рубля поднимает долларовые API/data costs | high | COGS растёт, margin падает | USD/RUB > budget corridor 10-15% | price indexation clauses, RUB prepayments, vendor diversification |
| Financial | Инфляция и рост зарплат раздувают FOT | med | fixed costs уходят выше 8,5-9 млн ₽/мес | контрофферы на рынке, frequent salary adjustments | selective hiring, bonus mix, offshore/remote mix |
| Black swan | Резкое отключение ключевого LLM provider | med | service outage и срочный replatforming | API incidents, policy notices, degraded throughput | reserve models, abstraction layer, offline failover playbooks |
| Black swan | Новая волна санкций / военной эскалации ломает enterprise procurement | med | сделки зависают на кварталы | freeze комитетов, pause по новым ИТ-проектам | sell to resilient sectors, shorten pilot scope, cash reserve |

## B5. Kill conditions, 6-месячный stop/go

Продолжать нельзя, если через 6 месяцев выполняется хотя бы одно из условий:

1. **Median-case не подтверждается:** p10 EBITDA остаётся отрицательным и cash runway падает ниже **9 месяцев**.
2. **GTM не собирается:** paid clients **< 3**, либо pilot→paid conversion **< 15%** на выборке не менее 10 пилотов.
3. **Pricing не держится:** фактический ARPU **< 450 000 ₽/мес** или blended CAC уходит выше **2 000 000 ₽** без компенсирующего роста retention.

## B6. Итоговый critic verdict

Кейс остаётся **интересным, но хрупким**. Unit economics в median-case выглядят очень сильными, однако Monte Carlo Lite показывает, что downside остаётся болезненным: один срыв по premium pricing или acquisition efficiency быстро уводит модель в отрицательный EBITDA. Для фонда это не auto-reject, но и не clean pass: нужен жёсткий контроль по pricing, pilot conversion и runway уже в первые 6 месяцев.

<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[FINTECH] Investment Banking AI Analyst Operator v2 — NEAR-PASS: 69/100 | EBITDA base=1811К₽/мес через 12 мес | LTV/CAC=17,4x | Ключевое преимущество: сильная economics при premium enterprise pricing | Главный риск: спрос и moat пока держатся на узком числе buyers.

# 06-verdict

## Кейс
investment-banking-ai-analyst-operator-v2

sector: FINTECH

## Дата вердикта
2026-04-20

## Итог инвесткомитета
**Статус: NEAR-PASS**
**Normalized score: 69/100**
**Предыдущий score: 67/100**
**Delta vs previous verdict: +2 пункта**

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 17,4x», «CAC Payback = 2,27 месяца», «Contribution Margin = 59,2%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «EBITDA = 50 × 355 000 - 7 720 000 = 10 030 000 ₽/мес», base M12 EBITDA «1 810 538 ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | «Exact search demand почти отсутствует», но «hh.ru по запросу инвестиционный аналитик видно 1 245 вакансий». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | «Самая опасная конкурентная позиция... СПАРК/Контур + внутренний analyst team + generic LLM», значит moat пока средний. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | «проект капиталоёмкий», «startup_capital = 70 млн ₽», есть риски 152-ФЗ, санкций и private deployment. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | «Founder-led outbound / ABM», «партнёрства / SI / referral» и «events + thought leadership» дают blended CAC 1 362 400 ₽. |

**Raw total: 103/150**
**Normalized score = round((103 × 100) / 150) = 69/100**

## Investment committee verdict
**Вердикт: NEAR-PASS.**

Кейс стал лучше предыдущего rerun за счёт более строгой economics и PnL, но всё ещё не проходит approve-порог. Главная причина, это не математика юнит-экономики, а недостаточно доказанный repeatable RU-demand для premium investment-banking workflow и средний moat против сильных substitutes. По фонду это не reject по качеству бизнеса, а reject по margin of safety.

## 7-factor Moat Framework

| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных, кроме косвенного learning. |
| Switching costs | 2 | Есть интеграции, закрытый контур, шаблоны memo/comps и привычка analyst-команды. |
| Scale economies | 1 | Часть COGS падает с объёмом, но data/API и high-touch delivery остаются заметными. |
| Proprietary data / model advantage | 1 | Пока виден скорее orchestration поверх чужих data layers, а не собственный dataset moat. |
| Regulatory moat | 2 | 152-ФЗ, data residency и security review дают барьер входа, но это moat категории, а не компании. |
| Brand / distribution | 2 | Founder-led enterprise selling и category proof есть, но бренд в РФ ещё не закреплён. |
| Embedded workflow | 3 | Если продукт садится в memo, comps, DD и audit trail, то он глубоко встраивается в ежедневный workflow. |

**Sum 7-factor = 11/21**
**Moat score = round((11 × 25) / 21) = 13/25**, вручную округлён до **14/25** с учётом высокой глубины workflow, но moat всё равно не investment-grade.

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам и corpfin командам | SDR + Revenue Ops | HH/СПАРК/ручной ресерч/CRM | 2 ч на аккаунт | 2 500 | Средняя |
| 2 | Enrichment контактов, квалификация лиц принимающих решение | SDR | CRM + email enrichment + LinkedIn analog | 1,5 ч | 1 900 | Средняя |
| 3 | Outbound sequence, cold email/call/Telegram/intro | SDR | Outreach stack + телефония | 3 недели | 12 000 | Средняя |
| 4 | Discovery call, pain mapping, qualification | AE + founder/CEO | VC/Meet, CRM | 1 ч + prep | 8 500 | Низкая |
| 5 | Demo на реальных документах / comps / memo workflow | AE + Solutions analyst | Demo env, secure sandbox | 3-5 дней | 18 000 | Низкая |
| 6 | Security review и legal scoping | CTO + security/compliance + buyer IT | VDR, policy docs, DPA/NDA | 2-4 недели | 45 000 | Низкая |
| 7 | Pilot setup в закрытом контуре | CTO + backend + ML + solutions analyst | VPC, connectors, prompt/eval stack | 3-6 недель | 140 000 | Средняя |
| 8 | Pilot сопровождение, weekly steering | AE + solutions analyst + CSM | Jira/Notion/CRM | 1 месяц | 85 000 | Низкая |
| 9 | Procurement, закупка, согласование MSA/SOW | AE + CEO + legal | ЭДО/договорной workflow | 2-6 недель | 60 000 | Низкая |
| 10 | Invoice issuance / акт / payment collection | Finance/Ops | 1С/банк/ЭДО | 3-5 дней | 7 000 | Средняя |
| 11 | Go-live и monthly success cadence | CSM + product + CTO | CRM, product analytics | ongoing | 28 000/мес | Средняя |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 23 680 000 ₽ |
| Fully-loaded CAC | 1 362 400 ₽ |
| LTV/CAC | 17,4x |
| CAC Payback | 2,27 мес по MRR / 3,84 мес по contribution |
| GM | 59,2% |
| contribution_margin_rub_month | 355 000 ₽/клиент/мес |
| fixed_costs_rub_month | 7 720 000 ₽/мес |
| Break-even | 22 клиента |
| startup_capital_to_bep_rub | 57 776 161 ₽ |
| company_ebitda_rub_month base M12 | 1 810 538 ₽/мес |
| company_ebitda_potential_rub_month | 10 030 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 24 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 25 |
| months_to_1m_ebitda | 12 |

## Team table

| Роль | Нужно чел. | Функция | FOT fully-loaded ₽/мес |
|---|---:|---|---:|
| CEO | 1 | Продажи top accounts, fundraising, партнёрства | 845 000 |
| CTO / Tech Lead | 1 | Архитектура, security, private deployment | 780 000 |
| Senior Backend | 2 | Интеграции, data pipelines, backend | 1 170 000 |
| ML Engineer | 1 | Retrieval, evals, prompt/agent quality | 715 000 |
| DevOps | 1 | VPC, CI/CD, observability, access control | 455 000 |
| Frontend | 1 | Analyst UI, workbench, approval layer | 390 000 |
| Product Manager | 1 | Workflow design, roadmap, pilot feedback loop | 455 000 |
| AI Solutions Analyst | 1 | Demo, пилоты, onboarding, analytic QA | 416 000 |
| SDR | 1 | Outbound prospecting | 260 000 |
| AE | 1 | Discovery, demo, close, procurement | 455 000 |
| Customer Success | 1 | Retention, upsell, adoption | 325 000 |
| Finance / Ops | 1 | Документы, биллинг, finance ops | 234 000 |
| **Итого** | **13** |  | **6 500 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбербанк | большой corpfin/risk/M&A контур, сложные security review оправданы | intro через отраслевую конференцию + email head of strategy | 900 000 ₽/мес |
| ВТБ | крупная кредитная организация, высокая цена ручной аналитики и DD | email decision-maker + партнёрство с SI | 800 000 ₽/мес |
| Газпромбанк | investment banking и корпоративное финансирование внутри группы | founder-led outbound + conference networking | 800 000 ₽/мес |
| Альфа-Банк | сильный digital и corpdev контур, готовность к workflow automation | тёплый intro через VC/fintech ecosystem | 700 000 ₽/мес |
| Т-Банк | data-heavy аналитический стек, быстрый pilot fit | direct outreach product/risk lead | 700 000 ₽/мес |
| Совкомбанк | активный M&A и credit/risk контур, нужен secure memo workflow | email CFO strategy office | 600 000 ₽/мес |
| ПСБ | regulated buyer с потребностью в закрытом контуре | гос/enterprise conference + партнёрский заход | 600 000 ₽/мес |
| МТС Банк | fintech buyer с digital-командой и нагрузкой на DD/research | email innovation/compliance lead | 500 000 ₽/мес |
| X5 Group | corpdev и strategy workflows, смежная боль по due diligence | партнёрство Big4/SI + direct outreach | 500 000 ₽/мес |
| VK | investment/corpdev и M&A scouting, data-heavy workflows | direct outreach + контент на vc.ru/Habr | 500 000 ₽/мес |

## PnL и Risk summary

### Base / Optimistic / Pessimistic
- Base M12: 26,8 клиента, MRR 16 107 951 ₽, EBITDA 1 810 538 ₽/мес.
- Optimistic M12: 33,0 клиента, EBITDA 3 977 919 ₽/мес.
- Pessimistic M12: 15,9 клиента, EBITDA -2 076 629 ₽/мес.
- p10 EBITDA @M24: -4 570 000 ₽/мес.
- p50 EBITDA @M24: 10 030 000 ₽/мес.
- p90 EBITDA @M24: 38 130 000 ₽/мес.

## Top-3 risks

| Риск | Probability | Impact | Почему в top-3 |
|---|---|---|---|
| Price compression и generic LLM substitutes | high | high | В critic прямо сказано: «Price -30% ... EBITDA -3 030 000 ₽/мес». |
| evidence_quality_unverified | high | medium | В demand-файле нет строки `Sources: T1=<N1>, T2=<N2>, T3=<N3>`, поэтому criterion #3 ограничен и confidence ниже. |
| Длинный pilot-to-paid и procurement цикл | high | high | «узкое место ... pilot + security + procurement», из-за чего burn до break-even остаётся высоким. |

## Что нужно доказать для APPROVED
1. 3-5 paid pilots в РФ банках/крупных corpfin командах с pilot→paid не ниже 25%.
2. Удержание ARPA не ниже 600 000 ₽/мес без системной скидки больше 15%.
3. Минимум 2 reference-клиента, где workflow реально заменяет analyst hours, а не просто добавляет ещё один research tool.
4. Повторяемый pipeline из 10+ named target accounts в квартал через partners/SI и founder-led enterprise sales.
5. Документированный private deployment и audit trail, снижающий risk на security/procurement этапе.

## LTV Upside Calculator
Так как кейс получает **NEAR-PASS**, нужен калькулятор upside для перехода в approve.

| Рычаг | Текущее значение | Upside-кейс | Эффект |
|---|---:|---:|---|
| ARPA | 600 000 ₽/мес | 750 000 ₽/мес | contribution_margin_rub_month растёт до ~505 000 ₽, EBITDA @50 клиентов до ~17,5 млн ₽/мес |
| Churn | 1,5%/мес | 1,0%/мес | customer_ltv_rub растёт с 23,68 млн ₽ до ~35,5 млн ₽ |
| CAC | 1 362 400 ₽ | 1 000 000 ₽ | LTV/CAC растёт с 17,4x до ~23,7x |
| Break-even month | M11-M12 | M9-M10 | снижается startup_capital_to_bep_rub и execution risk |
| Moat | 14/25 | 18/25 | нужен собственный data layer, шаблоны workflow и сильные reference accounts |

## Финальное решение
**REJECTED для текущего батча размещения, статус кейса: NEAR-PASS.**

Формально это near-pass, а не жёсткий fail: модель уже доказывает company_ebitda_potential_rub_month сильно выше 500K, но approve не даётся без более сильного demand proof и moat. Кейс нужно хранить в rejected-пуле как кандидат на повторный rerun после появления 2-3 реальных paid deployments.


---

## Файл: 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-19 — Program 4 Demand Validation
- stage: P4
- verdict: CONDITIONAL_PASS
- summary: Exact search demand в РФ низкий, но enterprise WTP подтверждён через текущие бюджеты на due diligence, контрагентские проверки, financial data и research tooling; early reject не применялся.
- demand_api: LOW (exact), adjacent demand присутствует
- market_view: узкий, но платёжеспособный fintech / corpfin workflow market
- profit_gate: PASS
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/investment-banking-ai-analyst-operator-v2/02-demand.md

## 2026-04-20 — Program 5 Unit Economics
- stage: P5
- verdict: PASS WITH RESERVATIONS
- previous_score_reference: 67/100 (rerun_of previous verdict)
- summary: После пересчёта fully-loaded CAC, hiring realism и burn-to-breakeven кейс проходит economics-gates фонда. Модель дорогая по GTM и FOT, но при MRR 600K ₽, contribution margin 59,2% и churn 1,5%/мес даёт LTV 23,68 млн ₽, LTV/CAC 17,4x и EBITDA около 10,03 млн ₽/мес при 50 клиентах.
- pricing_model: enterprise subscription + implementation
- avg_mrr_per_client_rub: 600000
- cogs_per_client_month_rub: 245000
- contribution_margin_pct: 59.2%
- fully_loaded_cac_rub: 1362400
- customer_ltv_rub: 23680000
- churn_rate_monthly: 1.5%
- ltv_cac: 17.4x
- cac_payback_months_mrr: 2.27
- fixed_costs_rub_month: 7720000
- break_even_clients: 22
- break_even_month: M15
- ebitda_at_50_clients_rub_month: 10030000
- startup_capital_to_bep_rub: 60939000
- decision_delta: rerun выглядит сильнее предыдущего near-pass по P5, но капиталоёмкость и длинный enterprise sales cycle остаются главным риском
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/investment-banking-ai-analyst-operator-v2/04-economics.md


## 2026-04-20 — Program 7 Critic and Verdict
- stage: P7
- verdict: NEAR-PASS
- normalized_score: 69/100
- raw_score: 103/150
- previous_score_reference: 67/100
- delta_vs_previous: +2
- summary: Юнит-экономика и EBITDA-потенциал investment-grade, но из-за слабого explicit RU-demand proof, отсутствия source-tier строки и среднего moat кейс остаётся near-pass.
- source_tier_balance: T1=0, T2=0, T3=0, weighted=1.00, penalty=-5 to Market+Demand
- moat_score: 14/25
- key_blocker: недостаточно доказанный repeatable спрос и уязвимость к price compression / generic LLM substitutes
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/investment-banking-ai-analyst-operator-v2/06-verdict.md

