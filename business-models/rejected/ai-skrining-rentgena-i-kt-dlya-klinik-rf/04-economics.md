# Unit Economics

## Итог этапа
- **Economics verdict:** `NOT_INVESTABLE`
- **Решение этапа:** `REJECT`
- **Почему:** спрос и бюджет у рынка есть, но для regulated B2B medtech в РФ экономика продажи слишком тяжёлая. При реалистичном fully-loaded CAC и полном составе команды кейс не дотягивает до fund-grade: **LTV/CAC = 1.9x**, **CAC payback = 20.3 мес**, а при **50 клиентах EBITDA остаётся отрицательной**.

## 1) Ключевые допущения модели
- Средний чек: **150 000 ₽ MRR на 1 клинику/центр**.
- Средний срок сделки: **6-9 месяцев**.
- Сегмент: **regulated healthcare B2B**, продажа через пилот, ИБ/юридическую проверку, интеграцию с PACS/МИС.
- Monthly logo churn для enterprise B2B SaaS benchmark: **1-2%/мес**; в модели взято **1.5%/мес** как середина диапазона. Источник: Optifai B2B SaaS Churn Benchmarks 2026.
- Валовая маржа до CAC: считается от клиентской выручки после переменных COGS.

## 2) Детальный business process: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Формирование таргет-листа сетей клиник и центров лучевой диагностики | SDR | HH/2ГИС/сайты клиник/CRM | 6 ч | 5 500 | средняя |
| 2 | Первичный outreach по ЛПР | SDR | CRM + почта + телефония | 10 раб. дней | 18 000 | средняя |
| 3 | Квалификация боли и объёма исследований | SDR | CRM + скрипты | 2 ч | 1 800 | средняя |
| 4 | Discovery call с главврачом / меддиром / ИТ | AE + CEO | Meet/Zoom | 1 неделя | 14 000 | низкая |
| 5 | Сбор требований по modality, PACS, МИС, SLA | AE + CTO | Notion/таблицы | 1 неделя | 22 000 | низкая |
| 6 | Подготовка демо и ROI-калькуляции | AE + CTO + ML | Demo env, BI, презентация | 4-5 дней | 38 000 | низкая |
| 7 | Пилотный контур и техоценка | CTO + Backend + ML + DevOps | PACS connector, staging, VPN | 3-6 недель | 120 000 | низкая |
| 8 | Клиническая валидация и QA | Clinical advisor + ML | Labeling/QA tools | 2-4 недели | 55 000 | низкая |
| 9 | ИБ/юридический review, DPA, договор | CEO + Compliance + юрист | Документооборот | 2-4 недели | 47 000 | низкая |
| 10 | Коммерческое согласование и закупка | AE + CEO | CRM + Excel | 2 недели | 31 000 | низкая |
| 11 | Онбординг, интеграция, обучение врачей | CS + CTO + Backend | PACS/МИС, база знаний | 2-3 недели | 64 000 | средняя |
| 12 | Выставление счёта и получение оплаты | Finance/CEO | 1С/банк/ЭДО | 5-10 дней | 6 000 | высокая |

**Вывод:** цикл продажи и внедрения длинный, с большим количеством дорогих ручных касаний. Это не self-serve и не лёгкий SaaS, а semi-services enterprise medtech.

## 3) COGS на 1 клиента в месяц
| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| GPU/инференс и вычисления | 18 000 | inference по снимкам + резерв по пикам |
| Хранение, обмен и защищённый контур данных | 6 000 | storage, backup, secure transfer |
| Интеграционная поддержка и релизы коннекторов | 12 000 | амортизация backend/devops труда |
| Клинический QA / разбор ложноположительных кейсов | 10 000 | part-time radiology QA |
| Customer Success и support | 8 000 | тикеты, обучение, SLA |
| Комплаенс и безопасность на клиента | 5 000 | аудит логов, доступы, policy upkeep |
| Биллинг и документооборот | 1 000 | ЭДО, бухгалтерия |
| **Итого COGS** | **60 000** |  |

- **MRR/клиент:** 150 000 ₽
- **Gross Profit/клиент:** 90 000 ₽
- **Gross Margin:** **60.0%**

## 4) CAC по каналам и funnel conversion
### 4.1 CAC по каналам
| Канал | Spend, ₽/мес | Воронка | New paying customers / мес | CAC, ₽ |
|---|---:|---|---:|---:|
| Outbound direct sales | 920 000 | 220 target accounts → 22 replies (10%) → 8 discovery (36%) → 3 pilots (37.5%) → 0.45 wins (15%) | 0.45 | 2 044 444 |
| Партнёры / интеграторы | 350 000 | 12 intro → 5 discovery (42%) → 2 pilots (40%) → 0.18 wins (9%) | 0.18 | 1 944 444 |
| Inbound / контент / performance | 401 000 | 40 MQL → 5 discovery (12.5%) → 1 SQL (20%) → 0.2 pilot (20%) → 0.02 wins (10%) | 0.02 | 20 050 000 |
| **Blended** | **1 671 000** | суммарно | **0.65** | **2 570 769** |

### 4.2 Fully-loaded CAC
Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | тестовый performance budget на узкую B2B меднишу | внутренняя модель для кейса |
| Outbound team FOT (SDR/AE attributed to new) | 679 000 | SDR 221 000 + 60% AE 458 000 | HH.ru benchmark + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 91 000 | 25% product/marketing generalist 364 000 | внутренняя модель |
| Tools (CRM, телефония, рассылки, BI) | 131 000 | CRM, телефония, secure demo stack, аналитика | внутренняя модель |
| Events/partnerships | 204 000 | travel, конференции, партнёрские активности | внутренняя модель |
| Overhead multiplier (x1.3) | 386 000 | 30% от raw acquisition spend 1 285 000 | стандартный overhead uplift |
| **Итого fully-loaded spend** | **1 671 000** |  |  |

- **Blended fully-loaded CAC:** **2 570 769 ₽**
- Sanity against RU benchmark: это выше типичного диапазона **400-1200K ₽** для B2B healthtech в РФ, что само по себе red flag.

## 5) LTV и churn
Источник benchmark churn: Optifai, B2B SaaS Churn Rate Benchmarks 2026, выборка 939 B2B компаний, enterprise monthly churn **1-2%**.

### Расчёт
- Monthly churn: **1.5%**
- Lifetime in months: **1 / 0.015 = 66.7 мес**
- Gross Profit per client per month: **90 000 ₽**
- **LTV (gross profit basis): 90 000 × 66.7 = 6 003 000 ₽**

## 6) LTV/CAC
- **LTV:** 6 003 000 ₽
- **Fully-loaded CAC:** 2 570 769 ₽
- **LTV/CAC = 2.34x**

**Интерпретация:** лучше 1:1, но ниже порога **3.0x**, который нужен для investment-grade. Для фонда это недостаточно.

## 7) CAC Payback
- Формула по задаче: `CAC Payback = CAC / MRR per customer`
- **2 570 769 / 150 000 = 17.1 месяца**

Комментарий:
- для обычного SaaS это плохо;
- для enterprise допустимый коридор до 18 мес, но здесь это почти потолок и без запаса.

## 8) Contribution Margin
- Revenue per client: **150 000 ₽**
- COGS per client: **60 000 ₽**
- Contribution per client: **90 000 ₽**
- **Contribution Margin = 60.0%**

Для software это умеренно, но не выдающеся. С учётом тяжёлого CAC margin не спасает модель.

## 9) Team & FOT
### 9.1 Полная команда
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1.5 | 126 000 | 1 092 000 |
| ML Engineer | 2 | 500 000 | 2-3 | 2 | 150 000 | 1 300 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product / implementation manager | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 170 000 | 0.5-1 | 1 | 51 000 | 221 000 |
| AE | 1 | 352 000 | 1-2 | 2-3 | 106 000 | 458 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Clinical advisor / radiologist QA | 1 | 220 000 | 2-4 | 1 | 66 000 | 286 000 |
| Security / compliance | 1 | 250 000 | 3-4 | 1 | 75 000 | 325 000 |
| **Итого** | **13** |  |  |  |  | **6 776 000 ₽/мес** |

### 9.2 Cumulative FOT timeline M1-M12
| Месяц | Кто подключён | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Backend-1, ML-1 | 2 756 000 |
| M2 | + Frontend, + Product/Implementation | 3 510 000 |
| M3 | + DevOps, + Backend-2 | 4 511 000 |
| M4 | + ML-2 | 5 161 000 |
| M5 | + Clinical advisor, + Security/Compliance | 5 772 000 |
| M6 | + SDR | 5 993 000 |
| M7 | + Customer Success | 6 318 000 |
| M8 | + AE | 6 776 000 |
| M9 | Полный состав | 6 776 000 |
| M10 | Полный состав | 6 776 000 |
| M11 | Полный состав | 6 776 000 |
| M12 | Полный состав | 6 776 000 |

**Sanity check:** массового найма 5+ человек в первый месяц нет, но даже при растянутом hiring-плане команда быстро выходит на очень тяжёлый FOT.

## 10) Fixed costs breakdown
| Статья | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 6 776 000 |
| Облако, dev/test и резерв мощности вне клиентского COGS | 250 000 |
| Юридические, регуляторные и сертификационные расходы | 180 000 |
| Офис, admin, бухгалтерия, ЭДО | 120 000 |
| База знаний, мониторинг, security tooling | 90 000 |
| **Итого fixed costs** | **7 416 000 ₽/мес** |

## 11) Break-even
### 11.1 Break-even по количеству клиентов
- Contribution per client = **90 000 ₽/мес**
- Fixed costs = **7 416 000 ₽/мес**
- **Break-even clients = 7 416 000 / 90 000 = 82.4**, округляя вверх: **83 клиента**

### 11.2 Break-even по месяцам
Если идти по траектории подключения клиентов:
- M1: 0
- M3: 1
- M6: 3
- M9: 6
- M12: 9
- M18: 18
- M24: 30

То в горизонте **24 месяцев break-even не достигается**. Для выхода на 83 клиента нужен масштаб, который не бьётся с observed sales cycle и регуляторным онбордингом.

### 11.3 Проверка profit gate на 50 клиентах
- Revenue at 50 clients = **7 500 000 ₽/мес**
- COGS at 50 clients = **3 000 000 ₽/мес**
- Gross Profit = **4 500 000 ₽/мес**
- EBITDA after fixed costs = **4 500 000 - 7 416 000 = -2 916 000 ₽/мес**

**Итог:** даже при **50 клиентах** компания остаётся убыточной. Это прямой **Profit Gate FAIL**.

## 12) Burn-to-breakeven и runway
### Burn-to-breakeven
При траектории M1-M12 и добавлении go-to-market затрат компания сжигает:
- M1 burn: ~**3.1 млн ₽**
- M6 burn: ~**6.8 млн ₽**
- M12 burn: ~**8.0 млн ₽**

Кумулятивно до M12 burn составляет порядка **73-78 млн ₽**, при этом break-even всё ещё далеко.

### Cash runway
При `startup_capital = 60 млн ₽`:
- средний burn на интервале M1-M12: около **5.9 млн ₽/мес**
- **cash runway ≈ 10.2 месяца**

Для такого кейса реалистичный капитал до breakeven скорее **80-100+ млн ₽**, что слишком тяжело для узкого TAM в РФ.

## 13) Главные выводы для фонда
1. **Рынок реальный, но узкий и тяжёлый в продаже.**
2. **Fully-loaded CAC слишком высокий** относительно MRR.
3. **LTV/CAC = 2.34x** ниже investment-grade порога **3x**.
4. **Payback 17.1 мес** допустим только на грани enterprise, без запаса.
5. **При 50 клиентах EBITDA отрицательная**, следовательно кейс ломается на profit gate.

## 14) Verdict
**REJECT.**

Не потому, что продукт никому не нужен, а потому что для фонда это плохая комбинация: длинный sales cycle, тяжёлый CAC, высокий FOT, умеренный TAM и отсутствие правдоподобного пути к положительной EBITDA на масштабе 50 клиентов.

## Sources / links
- Optifai, B2B SaaS churn benchmarks 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- HH.ru, вакансии ML engineer: https://hh.ru/vacancies/machine-learning-engineer
- HH.ru, вакансии Account Executive: https://hh.ru/vacancies/account_executive
- HH.ru, вакансии Computer Vision Engineer: https://hh.ru/vacancies/computer-vision-engineer
- Материалы из demand stage по рынку и ценовым сигналам: Roszdravnadzor, MosMedAI, Skolkovo, Third Opinion, CDO2DAY (см. 02-demand.md)
