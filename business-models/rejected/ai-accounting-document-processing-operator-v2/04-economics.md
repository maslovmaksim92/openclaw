# 04-economics

## P5 verdict
- **Итог:** FAIL.
- **Почему:** при реалистичном RU B2B service-led GTM fully-loaded CAC получается слишком высоким для текущего ARPA, а команда и фиксированные расходы слишком тяжёлые, чтобы выйти на **EBITDA 500k+/мес при 50 клиентах**. Даже при не катастрофическом LTV/CAC бизнес не выглядит fund-grade на этой стадии.
- **Ключевой вывод:** категория monetized, но именно для нового независимого игрока без сильного дистрибуционного канала через 1С/БПО/unit economics на early scale не сходится.

## Базовые допущения модели
- Сегмент: **mid-market B2B / service-led AI-оператор** для потока первички, интеграции с 1С/ERP и human-in-the-loop.
- Базовый прайс для модели: **30 000 ₽ MRR на клиента** + **80 000 ₽ onboarding one-off**. Это выше mass-market 1С/Entera и отражает managed workflow, а не commodity OCR.
- Базовый объём: 2 000-5 000 страниц/мес на клиента.
- Горизонт модели: steady-state на 12-м месяце после набора минимальной команды.
- Валютa: RUB, gross salaries + **30% страховые взносы**.

## Pricing anchor и sanity
| Якорь | Публичный прайс | Что значит для модели | Источник |
|---|---:|---|---|
| 1С:Распознавание первичных документов | 40 000 ₽/год за 10 000 стр.; 3 000 000 ₽/год за 1 000 000 стр. | Категория реальна, но mass-market OCR pricing низкий и давит на нижнюю границу | 1С: https://v8.1c.ru/its/services/1s-raspoznavanie-pervichnykh-dokumentov/cena-1s-raspoznavanie-pervichnykh-dokumentov/ |
| Entera | 76 000 ₽/год и 112 000 ₽/год на типовых тарифах | Managed слой продаётся дороже 1С, но всё ещё заметно ниже enterprise custom workflow | Entera: https://entera.pro/price2026 |
| Модель P5 | 360 000 ₽ ARR + 80 000 ₽ onboarding | Требуется premium over commodity OCR, иначе не собрать ни COGS, ни sales motion | Inference |

## Подробный бизнес-процесс: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Генерация лида через партнёра/поиск/контент | Marketing / SDR | hh-like lead lists, сайт, Telegram, Bitrix24/amoCRM | 1-7 дней до первого контакта | 6 500 | средняя |
| 2 | Первичный outreach и квалификация ICP | SDR | CRM, телефония, email, мессенджеры | 30-45 мин | 2 200 | средняя |
| 3 | Intro-call, discovery боли и объёма документов | AE | CRM, Meet/Zoom | 60 мин | 4 500 | низкая |
| 4 | Сбор 20-50 образцов документов и доступов | AE + Solution engineer | защищённый upload, почта, Telegram, shared folder | 2-5 дней | 6 000 | низкая |
| 5 | Тестовый pilot / sample processing | ML engineer + backend + operator QA | OCR/LLM stack, cloud, internal QA | 1-2 недели | 28 000 | средняя |
| 6 | Demo результатов, ROI-калькуляция, согласование scope | AE + founder | CRM, spreadsheet, презентация | 1-2 встречи | 8 500 | низкая |
| 7 | Security / legal / procurement review | Founder + AE | договоры, почта, ЭДО | 1-3 недели | 12 000 | низкая |
| 8 | Коммерческое предложение и согласование цены | AE | CRM + CPQ spreadsheet | 2-5 дней | 4 500 | средняя |
| 9 | Подписание договора и счёт | Ops / finance | Диадок/СБИС/1С, банк | 2-7 дней | 3 000 | высокая |
| 10 | Внедрение: mapping, интеграция, workflow setup | Solution engineer + backend + CS | 1С/ERP API, cloud, PM board | 1-3 недели | 35 000 | низкая |
| 11 | Обучение команды клиента и запуск | CS | call, база знаний, чат поддержки | 3-5 дней | 7 500 | средняя |
| 12 | Ежемесячная обработка документов и review exceptions | Ops reviewer + ML + backend | OCR/LLM stack, queue, dashboard | ежемесячно | 9 500 | средняя |
| 13 | Выставление ежемесячного счёта и оплата | Finance / CS | 1С, банк, ЭДО | 1-2 дня | 1 200 | высокая |

**Вывод по процессу:** это не self-serve SaaS. Продажа ближе к light enterprise workflow software с пилотом, интеграцией и ручным exception handling. Поэтому CAC и time-to-close должны считаться как у mid-market B2B, а не как у простого SMB SaaS.

## COGS breakdown на 1 клиента в месяц
**Базовый клиент:** 30 000 ₽ MRR

| Статья COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| OCR / AI inference | 2 500 | page-based processing + LLM checks | Internal estimate anchored to category economics |
| Cloud / storage / monitoring | 1 500 | compute, object storage, logs, backup | Internal estimate |
| Human exception review | 3 500 | ~10-12 часов reviewer time на клиента в месяц | hh бухгалтер/оператор вакансии + Internal |
| Customer support / success variable part | 1 200 | доля CS времени | Internal |
| 1С/ERP integration maintenance reserve | 800 | share of engineer support pool | Internal |
| Payment / EDO / misc variable | 500 | per-client service ops | Internal |
| **Итого COGS** | **10 000** |  |  |

- **Gross profit / клиент / мес:** 20 000 ₽
- **Gross margin:** **66,7%**

## CAC по каналам с funnel conversion
### Funnel assumptions
| Канал | Верх воронки | Qualified | Demo/Pilot | New paying customers | Conv. lead→customer |
|---|---:|---:|---:|---:|---:|
| Партнёры 1С / БПО / интеграторы | 12 интро/мес | 6 | 3 | 1,2 | 10,0% |
| Outbound SDR | 600 аккаунтов/мес | 48 ответов | 18 встреч | 1,5 | 0,25% |
| Paid search / content capture | 220 лидов/мес | 24 | 6 | 1,0 | 0,45% |
| **Blended** | — | — | — | **3,7** | — |

### CAC по каналам
| Канал | Spend, ₽/мес | Как получено | New paying customers / мес | CAC, ₽ | Комментарий |
|---|---:|---|---:|---:|---|
| Партнёрский | 240 000 | partner manager allocation + MDF + travel | 1,2 | 200 000 | самый дешёвый канал, но зависит от сети партнёров |
| Outbound | 520 000 | SDR + AE attributed + tools + data | 1,5 | 346 667 | реалистично для сложной B2B продажи |
| Paid search / content | 360 000 | Яндекс.Директ + лендинг + marketing allocation | 1,0 | 360 000 | захват существующего спроса, объём ограничен |
| **Blended raw CAC** | **1 120 000** | сумма по каналам | **3,7** | **302 703** | до overhead |

## FULLY-LOADED CAC
### Компоненты
| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | базовый тестовый media budget для capture существующего спроса | Internal model |
| Outbound team FOT (SDR/AE attributed to new) | 429 000 | SDR 170k gross + 30%; AE 350k gross + 30% × 50% allocation | HH.ru benchmark range + Internal |
| Marketing team FOT (partial allocation) | 156 000 | growth/marketing 120k gross + 30%, 100% на acquisition | HH-like RU market benchmark + Internal |
| Tools (CRM, data, телефония, рассылки) | 55 000 | CRM + телефония + data enrichment + email stack | Bitrix24 official pricing anchor + Internal |
| Events/partnerships | 120 000 | мини-ивенты, партнёрские MDF, travel | Internal |
| **Raw acquisition spend** | **940 000** | сумма выше |  |
| Overhead multiplier (x1.6 для mid-market B2B) | 564 000 | 940k × 0.6 | Standardized assumption per brief |
| **Fully-loaded spend / мес** | **1 504 000** | raw + overhead |  |

### Fully-loaded CAC formula
`Fully-loaded CAC = 1 504 000 / 3,7 = 406 486 ₽ за нового платящего клиента`

### Sanity vs benchmark
- Для **mid-market SaaS** в brief указан sanity corridor **60-250k ₽** CAC.
- Полученный CAC **406k ₽** выше corridor, но это уже ближе не к обычному SaaS, а к integration-led workflow продаже с пилотом и внедрением.
- **Red flag:** чтобы опустить CAC ниже 250k ₽, нужно либо резко поднять конверсию пилот→контракт, либо продавать через сильный партнёрский канал, либо иметь существенно более высокий ACV.

## LTV и churn rate
### Churn benchmark
- Для **mid-market B2B SaaS** внешний benchmark по monthly logo churn: **1,5-3,0% в месяц**.
- Для модели беру **2,0% / мес** как консервативную середину диапазона.
- Источник benchmark: Optifai, benchmark study по 939 B2B-компаниям, 2025-2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/

### Расчёт
- MRR на клиента = **30 000 ₽**
- Gross profit / клиент / мес = **20 000 ₽**
- Churn = **2,0% / мес**
- **LTV = Gross profit / churn = 20 000 / 0,02 = 1 000 000 ₽**

### Интерпретация
- LTV выглядит приемлемо только если churn удерживается около 2% и клиентский объём не проседает.
- При churn **2,5%/мес** LTV падает до **800 000 ₽**.
- При churn **3,0%/мес** LTV падает до **666 667 ₽**.

## LTV/CAC ratio
- **LTV/CAC = 1 000 000 / 406 486 = 2,46x**
- Порог investment grade по brief: **>= 3,0x**
- **Вердикт:** ниже investable-уровня.

## CAC Payback
- Формула по brief: `CAC Payback = CAC / MRR per customer`
- **CAC Payback = 406 486 / 30 000 = 13,5 мес**
- Базовый порог: **<12 мес**, для enterprise допускается **<18 мес**
- **Вердикт:** погранично терпимо только как quasi-enterprise motion, но слабо для раннего фонда.

## Contribution Margin %
- Revenue / клиент / мес = 30 000 ₽
- COGS / клиент / мес = 10 000 ₽
- Contribution / клиент / мес = 20 000 ₽
- **Contribution Margin = 20 000 / 30 000 = 66,7%**

## Team & FOT
### Полная команда
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 1 170 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 170 000 | 0,5-1 | 1 | 51 000 | 221 000 |
| AE (Account Exec) | 1 | 350 000 | 1-2 | 3 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| **Итого** | **10** |  |  |  |  | **5 226 000** |

### Комментарий по бенчмаркам найма
- Диапазоны согласуются с brief и рыночными уровнями Москвы/СПб для senior SWE, CTO, ML, SDR и AE.
- Для AI core и 1С-интеграции дешёвый найм выглядит нереалистично, особенно по ML/CTO.
- Уже сама минимально жизнеспособная команда даёт **FOT >5,2 млн ₽/мес** после набора.

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в команде | Monthly FOT fully-loaded, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + CTO | 1 560 000 |
| M3 | CEO + CTO + Backend #1 | 2 145 000 |
| M4 | CEO + CTO + Backend #1 + Frontend | 2 535 000 |
| M5 | CEO + CTO + 2×Backend + Frontend + DevOps | 3 575 000 |
| M6 | CEO + CTO + 2×Backend + Frontend + DevOps + ML | 4 225 000 |
| M7 | + SDR | 4 446 000 |
| M8 | + AE | 4 901 000 |
| M9 | + Customer Success | 5 226 000 |
| M10 | полный состав | 5 226 000 |
| M11 | полный состав | 5 226 000 |
| M12 | полный состав | 5 226 000 |

**Sanity:** план не нарушает hiring realism. Массового набора 5+ человек в первый месяц нет.

## Fixed costs breakdown
| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 226 000 | см. таблицу выше |
| Office / legal / accounting / admin | 220 000 | минимальный back-office |
| Core infra baseline | 180 000 | общая облачная платформа, не переменная часть |
| Sales travel / partner enablement | 120 000 | поездки, встречи, демо |
| Software / internal tools | 95 000 | CRM, PM, monitoring, communications |
| Misc reserve | 85 000 | форс-мажор, найм, закупки |
| **Итого fixed costs / мес** | **5 926 000** |  |

## Break-even
### По числу клиентов
- Contribution / клиент / мес = **20 000 ₽**
- Fixed costs / мес = **5 926 000 ₽**
- **Break-even clients = 5 926 000 / 20 000 = 296,3**, округлённо **297 клиентов**

### По месяцу
Если после запуска GTM в steady-state компания добавляет:
- M7: 1 клиент
- M8: 2 клиента
- M9: 3 клиента
- M10+: 4 клиента/мес,

то к break-even по клиентской базе компания выйдет только примерно на **M80+**, что для ранней венчурной модели слишком поздно. Даже если удвоить темп до **8 клиентов/мес**, break-even всё равно будет ближе к **M43-M45**.

## EBITDA test на 50 клиентах
- Revenue = **50 × 30 000 = 1 500 000 ₽/мес**
- COGS = **50 × 10 000 = 500 000 ₽/мес**
- Gross profit = **1 000 000 ₽/мес**
- EBITDA ≈ **1 000 000 - 5 926 000 = -4 926 000 ₽/мес**

**Profit Gate:** при **50 клиентах** компания даже близко не достигает **+500k EBITDA/мес**. Это автоматический FAIL по правилам brief.

## Burn-to-breakeven
### До полной команды и GTM
Ориентировочный cumulative burn до конца M12:
- Сумма FOT M1-M12 = **46,666 млн ₽**
- Fixed overhead вне FOT в среднем ≈ **0,7 млн ₽/мес**, итого ещё **8,4 млн ₽**
- Acquisition burn с M7-M12 ≈ **1,5 млн ₽/мес × 6 = 9,0 млн ₽**
- **Итого burn до конца M12 ≈ 64,1 млн ₽** без учёта существенной выручки

### Вывод
Для выхода к break-even нужна капитализация порядка **70-90 млн ₽** при таком темпе найма и GTM, иначе компания упрётся в cash wall задолго до экономической зрелости.

## Cash runway
- Допущение по startup capital: **35 млн ₽**
- Средний burn после набора GTM-функции: **~6,5 млн ₽/мес**
- **Cash runway = 35 / 6,5 ≈ 5,4 месяца**

Даже если команда будет наниматься медленнее и burn удастся удержать ближе к **4,5-5,0 млн ₽/мес**, runway составит лишь **7-8 месяцев**, что недостаточно для mid-market B2B motion с пилотами, интеграциями и длинным sales cycle.

## Why economics break
1. **ARPA рынка слишком низкий** относительно требуемого service layer. 1С и Entera задают anchor, который ограничивает pricing power на массовом сегменте.
2. **Продажа сложная и дорогая**, потому что клиент хочет пилот, интеграцию, exception handling и надёжность.
3. **Команда дорогая**: AI + 1С/ERP + sales + CS нельзя собрать дешево.
4. **Партнёрский канал обязателен**, но он не бесплатный и требует enablement budget.
5. **На 50 клиентах экономика глубоко отрицательная**, а для фонда это критично.

## Final P5 assessment
| Метрика | Значение | Порог | Статус |
|---|---:|---:|---|
| Gross Margin | 66,7% | >60% | PASS |
| Contribution Margin | 66,7% | >50% | PASS |
| Fully-loaded CAC | 406 486 ₽ | sanity vs segment | WEAK |
| LTV | 1 000 000 ₽ | > CAC materially | PASS |
| LTV/CAC | 2,46x | >=3,0x investable; <2,0x weak | FAIL |
| CAC Payback | 13,5 мес | <12 мес, либо <18 enterprise | WEAK |
| EBITDA at 50 clients | -4,93 млн ₽/мес | >= +0,5 млн ₽/мес | FAIL |
| Break-even clients | 297 | чем ниже, тем лучше | FAIL |
| Capital needed to realistic BEP | 70-90 млн ₽ | >10 млн для B2B SaaS expected | PASS as realism, FAIL as attractiveness |

## P5 verdict for pipeline
- **REJECTED на этапе economics.**
- Demand был условно проходным, но realistic unit economics для независимого игрока без существующего дистрибуционного moat не выдерживает инвестиционный фильтр.
- Теоретически кейс можно спасти только при одном из трёх изменений:
  1. enterprise ACV **в 2-3 раза выше**,
  2. мощный партнёрский канал с CAC **<200k ₽**,
  3. продуктовая архитектура с гораздо меньшим human-in-the-loop.
- В текущем виде фондовый тезис слабый.

## Sources
- 1С pricing: https://v8.1c.ru/its/services/1s-raspoznavanie-pervichnykh-dokumentov/cena-1s-raspoznavanie-pervichnykh-dokumentov/
- Entera pricing: https://entera.pro/price2026
- Churn benchmark: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- HH demand anchors from P4: https://hh.ru/vacancies/bukhgalter_pervichnoy_dokumentacii , https://hh.ru/vacancies/buhgalter-po-obrabotke-pervichnoj-dokumentatsii
