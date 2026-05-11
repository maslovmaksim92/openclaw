---
stage: economics
sector: FINTECH
updated: 2026-05-11T04:09:00+03:00
verdict: REJECTED
---

# 04-economics

## Executive summary
- Модель выручки, которая выглядела проходной на P4, ломается на unit economics уровня фонда после пересчёта в fully-loaded CAC и реалистичный FOT для regulated B2B fintech в РФ.
- Базовый пакет беру как **55 000 ₽ MRR на клиента** плюс **120 000 ₽ onboarding fee**. Это верхняя часть реалистичного диапазона из 02-demand и уже не «дешёвый бот». [D1]
- Даже при таком чеке и приемлемом **LTV/CAC = 6,9x** компания **не проходит Profit Gate**, потому что при **50 клиентах** месячная recurring-выручка всего **2,75 млн ₽**, валовая прибыль **1,825 млн ₽**, а фиксированная база команды и G&A уже **6,08 млн ₽/мес**.
- Следствие: acquisition сам по себе не убивает кейс, но **операционная база слишком тяжёлая для объёма рынка и ARPU**, поэтому инвестиционный вердикт на этой стадии, **REJECTED**.

## Модель и ключевые допущения
| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | МСБ-импортёры/экспортёры, бух-аутсорс, ВЭД-агенты | Regulated workflow, не self-serve [D1] |
| Сегмент CAC multiplier | 2,5x | Regulated fintech, длинный цикл согласований |
| Цена подписки | 55 000 ₽/клиент/мес | upper-mid сценарий из demand, иначе экономика ещё хуже [D1] |
| Onboarding fee | 120 000 ₽ | настройка шаблонов, 1С/ЭДО, банк-профили |
| Средний gross churn | 14% в год | беру консервативно около границы retention 85% как бенчмарка для здорового B2B SaaS [S1] |
| Месячный churn | 1,17% | 14% / 12 |
| Целевая база для стресс-теста | 50 клиентов | обязательный Profit Gate |
| Startup capital для runway | 35 млн ₽ | realistic pre-seed/seed для команды такого типа |

## 1) Детальный бизнес-процесс от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор таргет-аккаунтов ВЭД/МСБ | SDR | HH/Контур/Excel/TG/CRM | 25 мин | 420 | Полуавто |
| 2 | Первичный outbound/email/TG/звонок | SDR | CRM + телефония + почта | 20 мин | 335 | Полуавто |
| 3 | Квалификация по порогам 181-И, объёму ВЭД, числу платежей | SDR | Скрипт в CRM | 15 мин | 250 | Полуавто |
| 4 | Discovery-call | AE | Meet/телефония/CRM | 45 мин | 1 250 | Ручной |
| 5 | Сбор 2-3 типовых кейсов клиента и документов | AE + solutions/compliance | CRM + secure upload | 60 мин | 2 100 | Ручной |
| 6 | Демо pre-check контракта/инвойса/назначения платежа | AE + CTO | Demo env | 60 мин | 2 700 | Ручной |
| 7 | Пилот с human-in-the-loop | AE + ops/compliance + backend | Sandbox + LLM/OCR + Jira | 5 рабочих дней | 18 000 | Полуавто |
| 8 | Security/compliance review, согласование доступа | CTO + compliance/ops | Notion/Docs | 2-5 дней | 8 500 | Ручной |
| 9 | Коммерческое предложение и договор | AE + CEO | CRM + docs + ЭДО | 2 дня | 6 300 | Ручной |
| 10 | Онбординг: шаблоны, маршруты, роли | CSM + backend | 1С/ЭДО/CRM/admin panel | 5-10 дней | 28 000 | Полуавто |
| 11 | Первый боевой пакет документов и платёж | Ops/compliance + клиент | Product + bank-client + ЭДО | 1 день | 6 500 | Полуавто |
| 12 | Ежемесячная операционная поддержка и exception handling | CSM + ops/compliance | Product + helpdesk | 2-4 ч/мес | 8 500 | Полуавто |
| 13 | Выставление счёта и оплата | Finance/admin | 1С/ЭДО/банк | 20 мин | 350 | Авто/полуавто |

### Вывод по процессу
- Это не software-only воронка, а **sales-assisted + onboarding-heavy + compliance-heavy** процесс.
- Самые дорогие шаги, пилот, security review и onboarding. Именно они тянут CAC и снижают масштабируемость.

## 2) COGS breakdown на клиента в месяц
| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/OCR/распознавание документов | 2 500 | OCR + extraction + классификация пакета |
| Облако, storage, monitoring | 3 000 | compute, хранилище, логи |
| Интеграции 1С/ЭДО/банк-клиент, лицензии и коннекторы | 2 800 | распределённая стоимость коннекторов |
| Human exception review | 6 000 | ~1,5 часа ops/compliance на клиента/мес |
| Customer support / success allocation | 2 500 | доля CSM на сопровождение |
| QA/compliance контроль качества | 1 700 | выборочная проверка и audit trail |
| **Итого COGS** | **18 500** |  |

### Валовая маржа
- ARPU = **55 000 ₽/мес**
- COGS = **18 500 ₽/мес**
- Gross profit = **36 500 ₽/клиент/мес**
- **Contribution Margin = 66,4%**

## 3) CAC по каналам с funnel conversion
| Канал | Leads/мес | Meetings | SQL/Pilot | New paying | Conversion lead→paid | Fully-loaded cost, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound direct | 180 | 18 | 6 | 1,2 | 0,67% | 621 000 | 517 500 |
| Партнёры: бух-аутсорс/ВЭД-агенты | 30 партнёрских интро | 10 | 4 | 1,0 | 3,33% | 325 000 | 325 000 |
| Inbound/content/webinars | 40 | 8 | 2 | 0,4 | 1,00% | 351 000 | 877 500 |
| **Blended** | **250** | **36** | **12** | **2,6** | **1,04%** | **1 297 000** | **498 846** |

### FULLY-LOADED CAC
Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 80 000 | узкий search + ретаргетинг, ниша небольшая | model assumption + [D1] |
| Outbound team FOT (SDR/AE attributed to new) | 572 000 | SDR 160k + AE 280k + бонусы 40k, затем +30% соцвзносы | HH.ru benchmark [S2][S3][S4] |
| Marketing team FOT (partial allocation) | 130 000 | 0,5 FTE content/product marketing | HH.ru style range + model |
| Tools (CRM, телефония, enrichment, рассылки, ЭДО prep) | 95 000 | amo/HubSpot class + телефония + enrichment + storage | market estimate |
| Events/partnerships | 120 000 | вебинары, ассоциации, партнёрский co-marketing | model assumption |
| Overhead multiplier | 300 000 | ~30% на менеджмент, финансы, юр. координацию | standard fully-loaded overlay |
| **Итого blended acquisition cost / мес** | **1 297 000** |  |  |

- **Blended CAC = 1 297 000 / 2,6 = 498 846 ₽**
- Для sanity check это лежит внутри диапазона **200-700k ₽** для B2B fintech РФ и близко к нижней половине **400-1 200k ₽** для regulated workflows, то есть не выглядит занижением.

## 4) LTV с churn rate
### Benchmark churn
- ChartMogul пишет, что SaaS-компании с retention выше **85%** растут в 1,5-3 раза быстрее. Для фонда это означает, что всё заметно хуже 85% retention уже ухудшает качество бизнеса. [S1]
- Для regulated B2B mid-market в РФ беру **14% годового customer churn**, то есть **86% retention**, как умеренно хороший, но не best-in-class сценарий.

### Расчёт
- Monthly churn = **1,17%**
- Gross profit per customer per month = **36 500 ₽**
- **LTV = 36 500 / 0,0117 = 3 119 658 ₽**

## 5) LTV/CAC ratio
- LTV = **3,12 млн ₽**
- Blended fully-loaded CAC = **498 846 ₽**
- **LTV/CAC = 6,3x**

### Интерпретация
- По самому ratio сделка выглядит **инвестиционно допустимой**, потому что выше 3:1.
- Но это **ложноположительный сигнал**, если смотреть только на acquisition и игнорировать структуру fixed costs.

## 6) CAC Payback
Формула по заданию: `CAC Payback = CAC / MRR per customer`

- CAC = **498 846 ₽**
- MRR per customer = **55 000 ₽**
- **CAC Payback = 9,1 месяца**

Вывод: по payback модель формально терпимая, ниже 12 месяцев. Проблема не в payback, а в том, что компания не выдерживает собственный fixed-cost base.

## 7) Contribution Margin %
- Revenue per client = **55 000 ₽/мес**
- COGS per client = **18 500 ₽/мес**
- Contribution = **36 500 ₽/мес**
- **Contribution Margin = 66,4%**

Для AI-assisted managed workflow это нормальный, но не exceptional уровень. Недостаточно высокий, чтобы нести команду enterprise-grade комплаенса и продаж.

## 8) Полная таблица команды
### Team & FOT
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO / Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 2 | 400 000 | 1,5 | 1,5 | 120 000 | 1 040 000 |
| ML Engineer | 1 | 450 000 | 2,5 | 2 | 135 000 | 585 000 |
| DevOps | 1 | 300 000 | 1,5 | 1 | 90 000 | 390 000 |
| Frontend | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product Manager | 1 | 280 000 | 1,5 | 1,5 | 84 000 | 364 000 |
| SDR | 1 | 160 000 | 0,75 | 1 | 48 000 | 208 000 |
| AE | 1 | 320 000 | 1,5 | 3 | 96 000 | 416 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Compliance / Ops specialist | 1 | 220 000 | 1,5 | 1 | 66 000 | 286 000 |
| **Итого** | **11** | **4 100 000** |  |  | **1 230 000** | **5 330 000** |

### Функции команды
| Роль | Основная функция |
|---|---|
| CEO | продажи крупных сделок, fundraising, партнёрства |
| CTO | архитектура, безопасность, интеграции, техриск |
| Senior Backend x2 | workflow engine, API, integrations |
| ML Engineer | OCR/IE/RAG/classification/prompt-evals |
| DevOps | prod infra, observability, security baseline |
| Frontend | кабинет, review UI, audit trail |
| Product | сценарии, приоритизация, onboarding playbooks |
| SDR | первичный outbound и qualification |
| AE | demo, пилоты, коммерция, закрытие сделки |
| CS | внедрение, удержание, расширение |
| Compliance/Ops | human-in-the-loop разбор исключений |

### Cumulative FOT timeline M1-M12
| Месяц | Кто подключён | FOT fully-loaded, ₽/мес | Комментарий |
|---|---|---:|---|
| M1 | CEO | 780 000 | founder-driven старт |
| M2 | CEO + Frontend | 1 105 000 | первый быстрый найм |
| M3 | CEO + Frontend + 1 Backend | 1 625 000 | старт core product |
| M4 | CEO + Frontend + 1 Backend + CTO + DevOps | 2 665 000 | инфраструктурный контур |
| M5 | + Product + 2 Backend | 3 549 000 | закрываем product-delivery слой |
| M6 | + ML Engineer | 4 134 000 | AI-core начинает работать полноценно |
| M7 | тот же состав | 4 134 000 | без агрессивного overhire |
| M8 | + SDR | 4 342 000 | включаем лидогенерацию |
| M9 | + AE + Compliance/Ops | 5 044 000 | идём в пилоты и regulated delivery |
| M10 | + Customer Success | 5 330 000 | нужна функция удержания и онбординга |
| M11 | тот же состав | 5 330 000 | steady-state |
| M12 | тот же состав | 5 330 000 | steady-state |

Проверка realism:
- В M1 нет массового найма 5+ человек, значит time-to-hire не нарушен.
- Даже без офиса FOT к M10 выходит на **5,33 млн ₽/мес**, что и есть главный structural problem кейса.

## 9) Fixed costs breakdown
| Статья fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 330 000 |
| Юр., бухгалтерия, кадровый аутсорс | 120 000 |
| Инфобез / compliance / аудит / policy | 180 000 |
| Non-COGS software stack (Notion/Jira/Git/BI/office) | 110 000 |
| Админка, офис/коворкинг, связь, прочее G&A | 190 000 |
| **Итого fixed costs** | **5 930 000** |

Для консервативности округляю operating fixed base до **6,08 млн ₽/мес** с резервом на комиссии, ошибки найма и непредвиденные внедрения.

## 10) Break-even по числу клиентов и по месяцу
### По клиентам
- Contribution per client = **36 500 ₽/мес**
- Fixed costs = **6 080 000 ₽/мес**
- **Break-even client count = 6 080 000 / 36 500 = 166,6**, округляю до **167 клиентов**

### По месячной выручке
- Break-even MRR = **167 × 55 000 = 9,19 млн ₽/мес**
- Это в **3,3 раза выше**, чем выручка на обязательном стресс-тесте в 50 клиентов.

## Profit Gate at 50 clients
| Метрика | Значение |
|---|---:|
| Клиенты | 50 |
| MRR | 2 750 000 ₽ |
| COGS | 925 000 ₽ |
| Gross profit | 1 825 000 ₽ |
| Fixed costs | 6 080 000 ₽ |
| EBITDA | **-4 255 000 ₽/мес** |

### Вывод по Profit Gate
- Требование: EBITDA **≥ 500k ₽/мес achievable even at 50 clients**.
- Факт: при 50 клиентах **EBITDA = -4,26 млн ₽/мес**.
- **Profit Gate = FAIL.**

## Burn-to-breakeven
Чтобы дойти до 167 клиентов, компании нужно одновременно:
1. выдержать длинный hiring ramp,
2. профинансировать 9-12 месяцев sales-assisted GTM,
3. пережить отрицательный EBITDA почти на всём горизонте.

### Приближённый burn M1-M12
| Месяц | FOT, ₽ | Прочий fixed+infra+G&A, ₽ | Acquisition spend, ₽ | Total burn, ₽ |
|---|---:|---:|---:|---:|
| M1 | 780 000 | 350 000 | 0 | 1 130 000 |
| M2 | 1 105 000 | 380 000 | 0 | 1 485 000 |
| M3 | 1 625 000 | 420 000 | 0 | 2 045 000 |
| M4 | 2 665 000 | 520 000 | 0 | 3 185 000 |
| M5 | 3 549 000 | 570 000 | 0 | 4 119 000 |
| M6 | 4 134 000 | 620 000 | 0 | 4 754 000 |
| M7 | 4 134 000 | 650 000 | 150 000 | 4 934 000 |
| M8 | 4 342 000 | 680 000 | 350 000 | 5 372 000 |
| M9 | 5 044 000 | 710 000 | 700 000 | 6 454 000 |
| M10 | 5 330 000 | 750 000 | 1 000 000 | 7 080 000 |
| M11 | 5 330 000 | 750 000 | 1 200 000 | 7 280 000 |
| M12 | 5 330 000 | 750 000 | 1 297 000 | 7 377 000 |

- **Суммарный burn за первые 12 месяцев ≈ 55,2 млн ₽** до выхода на зрелую коммерческую конфигурацию.
- Даже если revenue начнёт частично компенсировать burn с M9-M12, до точки безубыточности всё равно потребуется **порядка 50-60+ млн ₽ капитала**.

## Cash runway
- Startup capital = **35 млн ₽**
- Burn на зрелом темпе = **~5,0-7,4 млн ₽/мес**
- Средний burn за M1-M12 = **~4,6 млн ₽/мес**
- **Cash runway ≈ 7,6 месяца**

Вывод: при seed-чеке 35 млн ₽ компании не хватает runway, чтобы спокойно дойти до продуктового и коммерческого maturity. Для этого кейса нужен более крупный капитал, чем оправдано текущим SAM.

## Инвестиционный вывод
### Что в модели хорошо
- ARPU не микроскопический.
- LTV/CAC и payback формально нормальные.
- Боль реальная и regulatory-driven. [D1]

### Что ломает инвестиционную историю
1. **Слишком тяжёлая команда** для такого объёма выручки на ранней стадии.
2. **Низкий ceiling по MRR**: 50 клиентов дают только 2,75 млн ₽ recurring revenue.
3. **Сильная сервисная примесь**: pilot, security review, exception handling и onboarding тянут бизнес в сторону managed services.
4. **Нужен disproportionate capital** к размеру ниши.

## Final verdict
**REJECTED.**

Причина rejection не в том, что нет спроса. Спрос есть. Проблема в том, что при realistic fully-loaded CAC и hiring realism компания **не достигает EBITDA 500k+/мес даже на 50 клиентах**, а break-even требует **167 клиентов**, что слишком далеко для этой ниши и такого operating model.

## Sources
- [D1] Файлы кейса: `02-demand.md`, `01-evidence.md`
- [S1] ChartMogul Benchmarks / retention guidance: https://help.chartmogul.com/hc/en-us/articles/12112768447004-Benchmarks
- [S2] HH.ru, Senior backend developer/engineer Москва: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancy/128441808
- [S3] HH.ru, DevOps Москва: https://hh.ru/vacancies/devops-engineer ; https://hh.ru/vacancy/129441009
- [S4] HH.ru, SDR / AE / Customer Success Москва: https://hh.ru/vacancy/128565026 ; https://hh.ru/vacancies/account_executive/polniy_den ; https://hh.ru/vacancy/128771369 ; https://hh.ru/vacancies/customer-success-manager
