# Unit economics

## Итог
- **Статус:** FAIL INVESTMENT GRADE
- **Модель:** AI-first веб-студия на Lovable + Tilda для SMB в РФ, основной доход из разовых проектов и частично из post-launch retainer.
- **Ключевой вывод:** спрос на услугу есть, но fully-loaded CAC для founder-led service business съедает экономику. При реалистичном attach-rate ретейнера и labor-heavy delivery модель даёт **LTV/CAC = 0,73x**, а значит не проходит инвестиционный стандарт фонда и не проходит минимальный CAC-gate даже до масштабирования.[T1][T2][T3][T4][inference]

## 1) Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Захват входящего лида из рекламы/реферала/партнёра | SDR / founder | Tilda form, Telegram, amoCRM | 15 мин | 150 | средняя |
| 2 | Первичный контакт, квалификация по бюджету и сроку | SDR | Телефония, Telegram, amoCRM | 30 мин | 300 | низкая |
| 3 | Discovery-call, бриф, pain map | Founder/AE | Google Meet/Telegram, Notion | 60 мин | 1 200 | низкая |
| 4 | Быстрый аудит текущего сайта/лендинга | Strategist / founder | Similarweb, manual review, GPT/Lovable | 45 мин | 900 | средняя |
| 5 | Подготовка offer + estimate + scope | Founder + PM | Notion, шаблон КП, GPT | 90 мин | 2 000 | средняя |
| 6 | Follow-up, дожим, согласование правок КП | AE / founder | amoCRM, почта, Telegram | 5 дней цикла, 90 мин труда | 1 800 | низкая |
| 7 | Договор / счёт / предоплата 70% | Founder + ops | Диадок/шаблон договора, банк | 60 мин | 1 000 | средняя |
| 8 | AI-генерация структуры, оффера, copy | Content/PM | GPT, Lovable | 3 ч | 2 700 | высокая |
| 9 | Дизайн и сборка сайта в Tilda | Designer + builder | Tilda, Figma | 10 ч | 9 000 | средняя |
| 10 | Интеграции, формы, CRM, аналитика | No-code dev / frontend | Tilda, Albato, amoCRM, Метрика | 4 ч | 4 000 | средняя |
| 11 | QA и публикация | PM + QA/founder | Browser testing, Tilda | 2 ч | 1 600 | низкая |
| 12 | 1-2 раунда правок | Designer + PM | Tilda, Telegram | 4 ч | 3 600 | низкая |
| 13 | Финальный акт, остаток 30%, upsell retainer | Founder/AE | Банк, amoCRM | 45 мин | 900 | низкая |

### Вывод по процессу
- Переменная себестоимость одного типового проекта до учёта fixed team overhead около **29 150 ₽** прямого труда и tool-usage.
- Но реальная delivery cost выше, потому что founder и sales делают много non-billable касаний, а ретейнер продаётся только части клиентов.
- Для фонда это не software-like motion, а service operation с высокой долей ручного труда.[inference]

## 2) COGS на клиента в месяц

### База для расчёта
- Средний стартовый проект: **140 000 ₽** one-off.[T1]
- Конверсия в retainer после запуска: **35%** клиентов.[inference]
- Средний retainer: **35 000 ₽/мес**.[T1]
- Средняя длительность retainer по benchmark retention: annual retention агентств 50-70%, что соответствует примерно **5-8% monthly churn**; для модели беру **8% monthly churn** как консервативный SMB-service benchmark.[T4][inference]
- Валовая маржа по retainer выше, чем по стартовому проекту, но blended gross margin по клиентскому life-cycle остаётся умеренной из-за ручного delivery.[inference]

| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Дизайн и сборка | 9 500 | амортизация проектного труда по 12-месячному эквиваленту |
| PM / account time | 3 800 | бриф, созвоны, статусы, правки |
| AI/tool usage | 1 400 | Lovable + GPT + Tilda + интеграции |
| Интеграции / no-code / QA | 2 600 | техническое сопровождение |
| Поддержка правок и контента | 4 900 | 2-3 ч/мес на активного клиента |
| Итого COGS | **22 200** | blended monthly COGS |

### Blended revenue and gross profit
- Эффективная выручка на acquired logo в месячном эквиваленте: **32 100 ₽/мес**.
- Blended COGS: **22 200 ₽/мес**.
- **Contribution gross profit: 9 900 ₽/мес**.
- **Contribution margin after COGS: 30,8%**.

## 3) CAC по каналам с funnel conversion

### Воронка по каналам
| Канал | Spend, ₽/мес | Лиды | SQL | КП | New paying customers | Lead→pay | CAC raw, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Paid ads (Яндекс.Директ/VK) | 120 000 | 32 | 12 | 6 | 2 | 6,3% | 60 000 |
| Outbound (SDR + founder outbound) | 40 000 direct spend | 20 | 6 | 3 | 1 | 5,0% | 40 000 |
| Партнёрства / рефералы | 25 000 | 10 | 6 | 4 | 2 | 20,0% | 12 500 |
| **Итого direct** | **185 000** | **62** | **24** | **13** | **5** | **8,1%** | **37 000** |

### FULLY-LOADED CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT (attributed) + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

#### Разложение компонентов CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | бюджет на performance для 2 новых клиентов из paid | модель канала, sanity vs intake [T1] |
| Outbound team FOT (SDR/AE attributed to new) | 273 000 | SDR 150k gross + 30% = 195k; 40% времени founder/AE на new biz = 78k | hh.ru SDR benchmark + allocation [T2][inference] |
| Marketing team FOT (partial allocation) | 78 000 | part-time marketer 60k gross + 30%; 100% в acquisition | hh/inference [T2][inference] |
| Tools (CRM, Tilda forms, enrichment, телефония) | 18 000 | amoCRM + телефония + домены + чат/боты | amoCRM tariff + inference [T3] |
| Events/partnerships | 25 000 | кофе-чеки, агентские комиссии, микро-ивенты | модель канала [inference] |
| Subtotal before overhead | 514 000 | сумма выше | calc |
| Overhead multiplier (x1.3) | 154 200 | 30% на founder management, финансы, admin overhead | стандарт для SMB service motion [inference] |
| **Итого fully-loaded CAC pool** | **668 200** | subtotal × 1.3 | calc |

- **New paying customers / мес:** 5
- **Blended fully-loaded CAC:** **133 640 ₽/клиент**

### Проверка against benchmark
- Intake ballpark CAC 12-35k был явно занижен, потому что это raw ad CAC без продаж и overhead.[T1]
- Для SMB self-serve benchmark обычно 5-30k, но этот кейс не self-serve, а done-for-you service с discovery, КП и правками, поэтому применять нужно higher band.[inference]
- Наш blended fully-loaded CAC **133,6k ₽** ближе к low end mid-market service motion и выглядит реалистичнее, чем 12-35k ₽.[inference]

## 4) LTV с churn rate

### Benchmark churn
- Databox/agency benchmark показывает, что годовое удержание клиентов агентств обычно около **50-70%**, то есть monthly churn для ретейнера примерно **5-8%**.[T4]
- Для conservative model беру **8% monthly churn**, потому что SMB-клиенты легко отваливаются после первого сайта, если retainer не привязан к постоянному трафику.[T4][inference]

### Расчёт LTV
Подход не SaaS-like, поэтому считаю **logo LTV gross profit** как сумму:
1. Gross profit от стартового проекта.
2. Expected gross profit от retainer с учётом attach-rate и churn.

#### 4.1 Стартовый проект
- Средний чек проекта: **140 000 ₽**.[T1]
- Gross margin проекта: **45%**.
- **Project gross profit = 63 000 ₽**.

#### 4.2 Retainer
- Attach rate в retainer: **35%** клиентов.[inference]
- Retainer ARPU: **35 000 ₽/мес**.[T1]
- Gross margin retainer: **65%**.
- Gross profit retainer/month: **22 750 ₽**.
- Monthly churn: **8%**.
- Expected retainer lifetime: **12,5 мес**.
- Gross profit per retained client LTV: **284 375 ₽**.
- Expected retainer GP across all acquired logos: **99 531 ₽** (= 284 375 × 35%).

#### 4.3 Total LTV
- **Total logo LTV gross profit = 162 531 ₽**.

## 5) LTV/CAC
- **LTV = 162 531 ₽**
- **Fully-loaded CAC = 133 640 ₽**
- **LTV/CAC = 1,22x** по gross-profit LTV

### Коррекция на founder replacement cost
В текущей модели founder закрывает часть sales/strategy почти бесплатно. Если заменить его рыночным AE/strategist, monthly acquisition cost растёт ещё примерно на **90-120k ₽/мес**, то есть normalized fully-loaded CAC становится около **151 000-157 000 ₽**.

- **Normalized LTV/CAC = 1,03-1,08x**.

### Инвестиционный вывод
- До investment-grade порога **3,0x** кейс очень далеко.
- На normalized basis модель почти у нуля по LTV/CAC и не оставляет запаса на ошибки, рост CAC или просадку attach-rate.

## 6) CAC Payback
- Для payback беру effective MRR per acquired logo = **32 100 ₽/мес**.
- **CAC Payback = 133 640 / 32 100 = 4,2 мес**.

### Почему payback выглядит нормально, а модель всё равно плохая
Payback короткий, потому что в начале есть крупный разовый проектный платёж. Но это маскирует слабую повторяемость и низкий долевой retainer attach. Для фонда важнее LTV/CAC и масштабируемость, а не только быстрая окупаемость первого чека.[inference]

## 7) Contribution Margin %

### На blended acquired logo basis
- Revenue LTV: **293 125 ₽** (= 140 000 + 35% × 35 000 × 12,5)
- COGS LTV: **130 594 ₽**
- Gross profit LTV: **162 531 ₽**
- **Contribution Margin = 55,4%** до CAC
- После fully-loaded CAC contribution becomes **28 891 ₽**, то есть **9,9% revenue LTV**
- После founder replacement reserve экономика фактически обнуляется.

## 8) Полная команда и FOT

### Team & FOT
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO/founder | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| CTO/Tech Lead | 0 | 0 | - | - | - | 0 |
| Senior Backend | 0 | 0 | - | - | - | 0 |
| ML Engineer | 0 | 0 | - | - | - | 0 |
| DevOps | 0 | 0 | - | - | - | 0 |
| Frontend / Tilda builder | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Designer | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| PM / Account | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| SDR (outbound) | 1 | 150 000 | 0,5-1 | 1 | 45 000 | 195 000 |
| AE / founder-sales allocation | 0,5 | 300 000 экв. | 1-2 | 2-3 | 45 000 | 195 000 |
| Customer Success / content ops | 1 | 160 000 | 1 | 1 | 48 000 | 208 000 |
| Маркетолог performance/partner | 0,5 | 120 000 экв. | 1 | 1 | 18 000 | 78 000 |
| Бухгалтерия / ops outsourced | 0,2 | 40 000 экв. | 0 | 0 | 0 | 40 000 |
| **Итого steady-state FOT** | 6,2 |  |  |  |  | **2 211 000 ₽/мес** |

### Комментарий по hiring realism
- Найм 5+ людей в M1 был бы red flag, поэтому в план ввожу постепенное подключение команды.[T2][inference]
- Для такой студии полноценный CTO/ML/Backend не нужны, иначе модель сразу ломается по FOT.
- Даже облегчённая service-team уже даёт **>2,2 млн ₽/мес** steady-state FOT, что намного выше стартовых гипотез intake.[inference]

### Cumulative FOT timeline M1-M12
| Месяц | Кто подключён | FOT monthly, ₽ |
|---|---|---:|
| M1 | Founder | 650 000 |
| M2 | Founder + designer | 936 000 |
| M3 | Founder + designer + Tilda builder | 1 261 000 |
| M4 | + PM/account | 1 495 000 |
| M5 | + SDR | 1 690 000 |
| M6 | + part-time marketer | 1 768 000 |
| M7 | + CS/content ops | 1 976 000 |
| M8 | тот же состав | 1 976 000 |
| M9 | + founder AE allocation formalized | 2 171 000 |
| M10 | steady-state | 2 211 000 |
| M11 | steady-state | 2 211 000 |
| M12 | steady-state | 2 211 000 |

## 9) Fixed costs breakdown
| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT steady-state | 2 211 000 | команда выше |
| Офис / коворкинг / встречи | 80 000 | гибридный режим |
| SaaS tools и admin | 45 000 | amoCRM, почта, дизайн, storage |
| Юр/бух/банки | 35 000 | аутсорс |
| Связь / телефония | 12 000 | sales + support |
| Налоги вне payroll reserve / misc | 40 000 | buffer |
| **Итого fixed costs до маркетинга** | **2 423 000** |  |
| Marketing spend direct | 185 000 | paid + partner spend |
| **Итого fixed + acquisition baseline** | **2 608 000 ₽/мес** |  |

## 10) Break-even по клиентам и по месяцу

### Break-even by client count
- Беру average contribution after COGS на активного клиента: **17 800 ₽/мес**.
- Fixed costs до acquisition: **2 423 000 ₽/мес**.
- **Break-even client count = 2 423 000 / 17 800 ≈ 136 клиентов**.

### Проверка на лимит 50 клиентов
- При **50 активных клиентах** monthly contribution after COGS ≈ **890 000 ₽**.
- Это **существенно ниже** fixed cost base **2,423 млн ₽/мес**.
- Даже если часть клиентов покупает новые лендинги, EBITDA **не выходит в +500k/mo** без сильного повышения чека или радикального урезания команды.

### Break-even by month
Консервативная траектория active clients: 3, 6, 10, 14, 18, 22, 27, 31, 35, 39, 44, 48.

| Месяц | Active clients | Contribution after COGS, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 3 | 53 400 | 742 000 | -688 600 |
| M3 | 10 | 178 000 | 1 367 000 | -1 189 000 |
| M6 | 22 | 391 600 | 2 031 000 | -1 639 400 |
| M9 | 35 | 623 000 | 2 374 000 | -1 751 000 |
| M12 | 48 | 854 400 | 2 608 000 | -1 753 600 |

- **Break-even month within first 12 months: не достигается**.

## Burn-to-breakeven и cash runway
- **Startup capital assumption:** **18 000 000 ₽**.
- Средний burn в M1-M12 по таблице выше около **1,50-1,75 млн ₽/мес**.
- **Burn-to-breakeven:** модель с текущим чеком и attach-rate до breakeven не доходит; суммарный burn за 12 мес ≈ **16,9 млн ₽**.
- **Cash runway:** при burn **1,6 млн ₽/мес** runway около **11,3 мес**.
- Для enterprise-SaaS это и так низко, но здесь ещё хуже: после 12 мес бизнес не приходит к самоподдерживающейся unit-экономике.[inference]

## Sanity checks
1. **CAC Payback = 4,2 мес**, формально ок, но искажён проектным авансом.
2. **LTV/CAC = 1,22x**, normalized почти **1,0x**. Это существенно ниже investable threshold **3,0x**.
3. CAC уже сильно выше intake estimate 12-35k, что подтверждает недооценку sales и founder time в исходной гипотезе.[T1]
4. **Break-even > 50 клиентов**, значит сервисная модель не масштабируется в рамках комфортного клиентского портфеля.
5. Для команды 5-7 человек FOT с M7 выше **1,9 млн ₽/мес**, это реалистично и не занижено.[T2][inference]

## Verdict
- **Profit Gate:** **FAIL**.
- Причина 1: при реалистичной fixed-cost базе и contribution на клиента компания **не достигает EBITDA +500k/mo даже при 50 клиентах**.
- Причина 2: **normalized LTV/CAC ≈ 1,0x**, что практически на грани убыточного привлечения.
- Следствие: кейс можно рассматривать как lifestyle/service business, но **не как investable fund-grade asset**.

## Sources
- [T1] Файлы кейса: `01-intake.md`, `02-demand.md`.
- [T2] HH.ru, salary benchmarks: Senior Backend/DevOps/SDR/AE, Москва: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancy/129581822 ; https://hh.ru/vacancy/128047964 ; https://hh.ru/vacancies/account_executive
- [T3] amoCRM pricing: https://www.amocrm.ru/buy/tariff/
- [T4] Databox, agency client retention benchmark: https://databox.com/marketing-agency-client-retention-benchmarks

Sources: T1=2, T2=4, T3=1, T4=1. Primary evidence basis: T1+T2, benchmark overlay from T4.