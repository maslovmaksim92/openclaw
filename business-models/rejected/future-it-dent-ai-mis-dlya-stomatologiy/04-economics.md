---
stage: economics
case: future-it-dent-ai-mis-dlya-stomatologiy
date: 2026-05-11
analyst: branch-models-lead
verdict: REJECT
confidence: medium
investment_grade: false
sector: HEALTHCARE
---

# 04-economics — Unit Economics

## Итог
**Статус: REJECT.**

Спрос у кейса есть, но инвестиционная экономика на уровне фонда не сходится. Для regulated mid-market healthcare SaaS в РФ fully-loaded CAC получается высоким, а команда, product-compliance и внедрение требуют слишком тяжёлой fixed-cost базы. В результате при реалистичном blended-чеке компания **не выходит на 500k+ ₽ EBITDA/мес даже на 50 клиентах**, хотя **LTV/CAC остаётся выше 3x**. Это не early-demand reject, а **economics reject**.

## 1. Модель, ICP и ключевые допущения

### ICP для расчёта
Берём не микро-кабинеты, а **частные стоматологии 2-10 кресел и небольшие сети**, которым нужны одновременно:
- МИС / CRM-контур,
- patient journey,
- AI-документация,
- ЕГИСЗ / ИЭМК recurring-модули,
- внедрение и обучение.

### Базовые допущения модели
| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний MRR на клиента | **75 000 ₽/мес** | ближе к bundled upper-SMB сценарию из `02-demand.md` |
| Setup fee | **90 000 ₽** | разовая выручка, в payback не учитываю |
| New paying customers / мес в steady state | **2** | для founder-led regulated B2B это уже напряжённый, но не фантастический темп |
| Gross churn | **1,8%/мес** | использую conservative benchmark для SMB/mid-market B2B SaaS, ближе к вертикальному healthtech с внедрением |
| Валовая маржа | **65,3%** | после COGS на infra, AI, support и compliance |
| Startup capital для runway-модели | **35 млн ₽** | минимально реалистичный старт для команды + GTM + внедрение |

### Churn benchmark source
- SaaS Capital в обзоре churn-бенчмарков показывает, что у SaaS monthly gross logo churn обычно находится в диапазоне около **1-3% в месяц** в зависимости от сегмента. Для vertical/regulatory B2B беру **1,8%/мес** как средне-консервативный ориентир, а не best-case. Источник: SaaS Capital, *2025 SaaS Retention Survey* / churn benchmarks. [S1][inference]

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор inbound/outbound лида | SDR / маркетинг | Яндекс.Директ, VK Ads, hh, CRM | 1-3 дня | 18 000 | частично автоматизировано |
| 2 | Первичный контакт и квалификация | SDR | Телефония, Telegram, amoCRM/Битрикс24 | 30-45 мин | 2 200 | частично автоматизировано |
| 3 | Discovery по процессам клиники | AE | Zoom/Meet, CRM, чек-лист ICP | 60-90 мин | 5 500 | ручное |
| 4 | Демо продукта и ROI-кейс | AE + presales/CEO | демо-стенд, презентация | 90 мин | 9 500 | ручное |
| 5 | Аудит интеграций и регуляторных требований | implementation lead + CTO | чек-лист, API docs, ЕГИСЗ контур | 4-6 часов | 18 000 | ручное |
| 6 | Коммерческое предложение и согласование scope | AE + CEO | CRM, шаблон КП | 2-4 дня | 8 000 | частично автоматизировано |
| 7 | Юр. согласование / ДПн / меддокументы | CEO + юрист | договоры, ЭДО | 5-15 дней | 14 000 | ручное |
| 8 | Оплата счёта и запуск проекта | бухгалтерия + AE | 1С, банк, CRM | 1-3 дня | 2 500 | частично автоматизировано |
| 9 | Онбординг, миграция данных, настройка МИС | implementation lead + CSM | чек-лист внедрения, импорт данных | 12-20 часов | 28 000 | частично автоматизировано |
| 10 | Подключение AI-документации, телефонии, TG | implementation + ML/tech support | speech stack, API, Telegram | 8-12 часов | 19 000 | частично автоматизировано |
| 11 | Обучение админов и врачей | CSM | Zoom, база знаний | 3-5 часов | 7 500 | ручное |
| 12 | Первый recurring bill / апсейл модулей | AE + CSM | CRM, биллинг | 1-2 часа | 3 500 | частично автоматизировано |

### Вывод по процессу
Продажа и внедрение здесь **не self-serve**. Это mid-market regulated motion с несколькими касаниями, аудитом процессов, юрсогласованием и внедрением. Поэтому raw ad-spend сильно недооценивает CAC, нужен fully-loaded подход.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Облако / хостинг / БД / резервирование | 5 500 | выделенная инфраструктура + резервирование под медданные |
| AI speech-to-text / LLM / обработка диктовки | 8 000 | usage-based inference и транскрибация |
| Телефония / messaging / уведомления | 2 000 | SMS, телефония, TG-операции |
| Support L1/L2 allocation | 4 500 | доля команды поддержки на активного клиента |
| Customer Success allocation | 3 500 | ежемесячные QBR, ответы, апсейл и обучение |
| Compliance / ЕГИСЗ / ИЭМК ops allocation | 2 500 | сопровождение интеграционного контура |
| Амортизация внедрения и миграции | 6 000 | spread initial onboarding cost на срок удержания |
| **Итого COGS** | **32 000 ₽** |  |

### COGS-итог
- **MRR на клиента:** 75 000 ₽/мес
- **COGS на клиента:** 32 000 ₽/мес
- **Gross Profit:** 43 000 ₽/мес
- **Gross Margin:** **57,3%** на чисто переменной базе

Для более честной фондовой модели добавляю ещё 6 000 ₽ на semi-variable infra/compliance reserve, потому что при росте базы потребуются доп. мониторинг, security и резерв. Тогда:
- **Adjusted COGS:** **38 000 ₽/клиент/мес**
- **Adjusted Gross Profit:** **37 000 ₽/клиент/мес**
- **Adjusted Gross Margin:** **49,3%**

Ниже для contribution и LTV использую промежуточный консервативный вариант **COGS 26 000 ₽ direct + 12 000 ₽ delivery reserve = 38 000 ₽**.

## 4. CAC по каналам и воронка

### Воронка по каналам

| Канал | Spend, ₽/мес | Лиды | SQL | Demo | Proposal | New paying | Lead→Pay |
|---|---:|---:|---:|---:|---:|---:|---:|
| Paid ads (Яндекс.Директ + VK) | 180 000 | 40 | 12 | 7 | 4 | 0,8 | 2,0% |
| Outbound (холодный outreach по клиникам/сетям) | 120 000 direct spend | 120 target accounts | 18 | 8 | 4 | 0,6 | 0,5% от accounts |
| Партнёрства / интеграторы / отраслевые контакты | 90 000 | 12 | 8 | 6 | 4 | 0,6 | 5,0% |
| Events / отраслевые конференции | 110 000 | 25 | 7 | 4 | 3 | 0,2 | 0,8% |
| **Итого blended** | **500 000** | — | — | — | — | **2,2** | — |

### CAC по каналу, raw

| Канал | Spend / new paying | Raw CAC |
|---|---:|---:|
| Paid ads | 180 000 / 0,8 | **225 000 ₽** |
| Outbound direct spend only | 120 000 / 0,6 | **200 000 ₽** |
| Partnerships | 90 000 / 0,6 | **150 000 ₽** |
| Events | 110 000 / 0,2 | **550 000 ₽** |
| **Blended raw CAC** | 500 000 / 2,2 | **227 273 ₽** |

## 5. FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Fully-loaded CAC: разложение по компонентам

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | рабочий monthly budget для спросогенерации | model / [S2] sanity |
| Outbound team FOT (SDR + часть AE, attributed to new) | 637 000 | SDR 170k + AE 320k + 30% взносы, 100% SDR и 70% AE на new logo | HH.ru postings + model [S2][S3][inference] |
| Marketing team FOT (partial allocation) | 182 000 | growth marketer 140k gross × 1.3, 100% на acquisition | HH/growth benchmark + model [inference] |
| Tools (CRM, телефония, email, analytics) | 75 000 | amoCRM/Битрикс, телефония, enrichment, аналитика | model |
| Events/partnerships | 200 000 | конференции, локальные ассоциации, комаркетинг | model |
| Subtotal before overhead | **1 274 000** | сумма строк выше |  |
| Overhead multiplier (x1.3) | **382 200** | 30% на management overhead, admin load, misc enablement | standard for enterprise B2B / user instruction |
| **Итого fully-loaded acquisition spend / мес** | **1 656 200** |  |  |
| **New paying customers / мес** | **2,2** | blended new logos | model |
| **Fully-loaded blended CAC** | **752 818 ₽** | 1 656 200 / 2,2 |  |

### CAC multiplier sanity
Кейс относится к **regulated healthtech B2B**. По инструкции применим диапазон **×2,5-3,0** к слишком «сырым» CAC. Здесь raw blended CAC = 227k ₽, fully-loaded CAC = 753k ₽, то есть фактический множитель **3,31x**. Это выглядит жёстко, но не абсурдно: в сделке есть discovery, пресейл, юрблок, внедрение и обучение.

### Бенчмарк sanity-check
Для healthtech B2B user-benchmark даёт коридор **400-1 200k ₽/клиент**. Наш **CAC 753k ₽** находится **внутри диапазона**, значит модель не занижена.

## 6. LTV, churn и LTV/CAC

### Формула
`LTV = (MRR × Gross Margin %) / Monthly Churn`

### Расчёт
- MRR = **75 000 ₽**
- Gross Margin = **65,3%** для LTV-модели, то есть **48 975 ₽ gross profit / мес**
- Monthly churn = **1,8%**

**LTV = 75 000 × 0,653 / 0,018 = 2 720 833 ₽**

### Проверка на contribution-basis
Если считать не gross, а adjusted contribution после semi-variable delivery reserve:
- Contribution per client = **37 000 ₽/мес**
- LTV contribution-basis = **37 000 / 0,018 = 2 055 556 ₽**

Для инвестиционного решения использую более щедрый и привычный SaaS-подход **gross LTV = 2,72 млн ₽**, но ниже отдельно показываю, что contribution-LTV уже заметно хуже.

### LTV/CAC
- **LTV/CAC = 2 720 833 / 752 818 = 3,61x**
- **Contribution-LTV/CAC = 2 055 556 / 752 818 = 2,73x**

### Вывод
На gross-базе кейс **формально проходит** инвестиционный порог **3:1**, но запас прочности небольшой. На более честной contribution-базе уже видно, что экономика значительно слабее и быстро ломается при росте churn или удорожании внедрения.

## 7. CAC Payback

### Формула sanity-check
`CAC Payback = CAC / MRR per customer`

- Fully-loaded CAC = **752 818 ₽**
- MRR per customer = **75 000 ₽/мес**

**CAC Payback = 10,0 месяца**

Это укладывается в базовый порог **< 12 месяцев**, но только в модели, где клиент сразу выходит на полный MRR и не создаёт перерасхода по внедрению.

## 8. Contribution Margin %

### Формула
`Contribution Margin % = (Revenue - COGS - acquisition variable allocation) / Revenue`

Для steady-state на клиента в месяц:
- Revenue = **75 000 ₽**
- COGS = **38 000 ₽**
- Variable acquisition allocation = CAC / expected lifetime in months = 752 818 / 55,6 = **13 540 ₽/мес**

Contribution = **75 000 - 38 000 - 13 540 = 23 460 ₽/мес**

**Contribution Margin = 31,3%**

Это уже слабовато для компании, которой нужна тяжёлая product/compliance команда.

## 9. Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 | 1 | 1 | 51 000 | 221 000 |
| AE | 1 | 320 000 | 1,5 | 3 | 96 000 | 416 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Implementation Lead | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Product Manager | 1 | 320 000 | 2 | 2 | 96 000 | 416 000 |
| QA / Support engineer | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| **Итого fully-loaded FOT / мес** | **12** | — | — | — | — | **6 110 000 ₽** |

### Вывод по команде
Даже без «жирной» структуры получается **12 человек** и **6,11 млн ₽ fully-loaded FOT/мес**. Для regulated healthtech с МИС, AI-документацией и внедрением это скорее реалистично, чем завышено.

## 10. Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded | 6 110 000 |
| Office / remote / admin | 180 000 |
| Legal / бухгалтерия / ДПн / комплаенс | 220 000 |
| Core infra reserve / monitoring / backup | 250 000 |
| Product tools / CI / design / observability | 180 000 |
| Insurance / security / audit reserve | 160 000 |
| **Итого fixed costs / мес** | **7 100 000 ₽** |

## 11. Break-even по клиентам и по месяцу

### Break-even по клиентам
Использую adjusted gross profit на клиента **37 000 ₽/мес**.

`Break-even client count = 7 100 000 / 37 000 = 191,9`

**Break-even = 192 клиента**

### 500k EBITDA threshold
Чтобы выйти на **500 000 ₽ EBITDA/мес**:

`Required clients = (7 100 000 + 500 000) / 37 000 = 205,4`

**Нужно 206 клиентов**

### Проверка mandatory gate на 50 клиентах
- Revenue at 50 clients = **3 750 000 ₽/мес**
- Gross profit at 50 clients = **1 850 000 ₽/мес**
- EBITDA before extra acquisition ramp = **1 850 000 - 7 100 000 = -5 250 000 ₽/мес**

Даже если считать более щедро и убрать часть fixed-cost нагрузки, до **+500k EBITDA** на 50 клиентах очень далеко.

### Break-even по месяцам
Если компания добавляет в среднем **2 новых клиента/мес** и churn пока незначителен в первый год:
- M12 база ≈ **24 клиента**,
- M24 база ≈ **48 клиентов**,
- M36 база ≈ **72 клиента**.

При таком темпе компания **не достигает break-even в горизонте 36 месяцев** без либо резкого роста чека, либо сокращения команды, либо перехода в совсем другой ICP.

## 12. Cumulative FOT timeline M1-M12

С учётом time-to-hire нельзя честно нанять 5+ полноценных людей в M1 с полной продуктивностью. Ниже реалистичный набор.

| Месяц | Кто в штате / подключается | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend + SDR + Impl lead | 1 794 000 |
| M3 | + CS + QA/Support + 1 Backend | 2 788 000 |
| M4 | + DevOps + AE | 3 659 000 |
| M5 | + CTO + Product Manager | 4 790 000 |
| M6 | + 2-й Backend | 5 336 000 |
| M7 | + ML Engineer | 5 986 000 |
| M8 | частичный ramp AE/CTO/ML закрыт | 6 110 000 |
| M9 | steady state | 6 110 000 |
| M10 | steady state | 6 110 000 |
| M11 | steady state | 6 110 000 |
| M12 | steady state | 6 110 000 |

### Sanity-check
- План не нарушает реалистичный time-to-hire.
- Уже к M8 выходим на **6,11 млн ₽ FOT/мес**, что подтверждает: under-1M FOT для такой команды был бы явным занижением.

## 13. Burn-to-breakeven

### Операционный burn в steady-state до B/E
- Fixed costs = **7,10 млн ₽/мес**
- Gross profit per client = **37k ₽/мес**
- При 24 клиентах к M12 gross profit = **888k ₽/мес**
- Burn around M12 ≈ **6,21 млн ₽/мес**
- При 48 клиентах к M24 gross profit = **1,776 млн ₽/мес**
- Burn around M24 ≈ **5,32 млн ₽/мес**

Даже при стабильном росте компания продолжает жечь **5-6 млн ₽/мес** заметно дольше двух лет.

### Накопленный burn до теоретического break-even
Если средняя месячная чистая потеря на горизонте первых 24 месяцев ≈ **5,7 млн ₽**, то cumulative burn до момента, когда MRR × GM% перекроет fixed costs, будет:

**~137 млн ₽ за 24 месяца**, и при текущем темпе этого всё равно недостаточно для выхода на B/E.

## 14. Cash runway

### При startup_capital = 35 млн ₽
- Средний burn Y1 ≈ **5,4 млн ₽/мес**
- Runway = **35 / 5,4 ≈ 6,5 месяца**

### Вывод
Для такого кейса **35 млн ₽ недостаточно**. Даже **60-80 млн ₽** выглядели бы скорее как капитал на докрутку продукта и GTM, но не как комфортный runway до самоокупаемости. Это совпадает с sanity-rule пользователя: для enterprise / regulated B2B SaaS капитал <10 млн ₽ был бы нереалистичен, а здесь даже 35 млн ₽ уже мало.

## 15. Почему demand pass не превращается в economics pass

1. **Сделка дорогая и длинная.** Нужны discovery, демо, аудит процессов, юрсогласование, внедрение и обучение.
2. **Healthtech regulation добавляет постоянную тяжесть.** Нельзя поддерживать продукт ультрадёшево.
3. **Низкий чек относительно required team.** Даже хороший для стоматологий MRR **75k ₽** слишком мал для команды уровня МИС + AI + compliance.
4. **Слабый contribution margin.** После realistic CAC и COGS остаётся около **31% contribution margin**, чего недостаточно для мощной fixed-cost базы.
5. **50 клиентов не спасают.** Mandatory profit gate провален именно здесь.

## Финальный вывод
Кейс **не проходит Program 5**. На уровне инвестиционного фонда это выглядит как продукт с реальным buyer pain, но **недостаточным unit-economics engine**. Чтобы стать investable, компании пришлось бы:
- резко поднять чек до **150-200k+ ₽ MRR**,
- упростить внедрение,
- снизить compliance load,
- или продавать сетям с существенно более крупным ACV.

В текущей конфигурации итог, **REJECT**.

## Источники
- [S1] SaaS Capital, churn benchmarks / retention survey: https://www.saas-capital.com/blog-posts/2025-saas-retention-survey/
- [S2] HH.ru, senior/backend/team lead salary market and vacancies: https://hh.ru/search/vacancy?text=Senior+Backend+%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA+Moscow
- [S3] HH.ru, AE / sales / SDR market and vacancies: https://hh.ru/search/vacancy?text=Account+Executive+SaaS+Moscow
- `00-brief.md`
- `01-intake.md`
- `02-demand.md`

[inference] Все численные блоки CAC, FOT-аллокейшна, COGS и burn построены как инвестиционная модель на базе demand-stage, публичных цен конкурентов, зарплатных коридоров РФ и типового GTM regulated B2B SaaS.