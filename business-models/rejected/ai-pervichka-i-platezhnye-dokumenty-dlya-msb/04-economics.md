# Unit economics

## Итог
- **Статус:** FAIL
- **Сегмент модели:** mid-market B2B fintech / automation для бухгалтерских аутсорсеров и document-heavy МСБ.
- **Базовый тариф для модели:** **25 000 ₽/клиент/мес**.
- **COGS:** **5 500 ₽/клиент/мес**.
- **Contribution Margin:** **78%**.
- **Blended fully-loaded CAC:** **499 000 ₽/новый платящий клиент**.
- **Monthly churn assumption:** **2,5%/мес**.
- **LTV:** **780 000 ₽**.
- **LTV/CAC:** **1,56x**.
- **CAC Payback:** **20,0 мес**.
- **Break-even:** **329 клиентов** или **~8,23 млн ₽ MRR/мес**.
- **Вывод фонда:** не investment-grade. При **50 клиентах** EBITDA остаётся глубоко отрицательной, а **LTV/CAC < 3x**.

## 1) Business process, от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Генерация лида из Яндекс.Директ / VK / outbound / партнёров | Marketing + SDR | Яндекс.Директ, VK Ads, amoCRM | 15 мин | 1 900 | medium |
| 2 | Первичный контакт и qualification | SDR | телефония, email, amoCRM | 20 мин | 460 | medium |
| 3 | Discovery call | AE | Zoom/Телемост, amoCRM | 45 мин | 2 190 | low |
| 4 | Demo продукта и разбор кейса по 1С/ЭДО | AE + Product | demo-стенд, презентация | 60 мин | 4 470 | low |
| 5 | Оценка потока документов, интеграций и pilot scope | CTO/Tech Lead + AE | Notion, API docs, 1С-коннекторы | 90 мин | 7 450 | low |
| 6 | Коммерческое предложение, согласование SLA и security/legal | AE + CEO | шаблон КП, договор, e-sign | 90 мин | 5 650 | low |
| 7 | Онбординг: подключение почты, ЭДО, шаблонов, реквизитов | CSM + Backend | админка, 1С, S3, queue workers | 6 ч | 14 040 | medium |
| 8 | Настройка extraction/validation/prompt rules под клиента | ML Engineer + Backend | OCR/LLM pipeline, rules engine | 4 ч | 12 480 | low |
| 9 | Pilot support, исправление ошибок, обучение бухгалтера | CSM | helpdesk, Telegram, knowledge base | 4 ч | 8 120 | medium |
| 10 | Выставление счёта, получение оплаты, активация тарифа | Finance ops + CSM | банк-клиент, ЭДО, CRM | 30 мин | 1 120 | high |

**Итого labour + onboarding cost на 1 нового клиента до первой оплаты:** около **57 900 ₽**. Это не заменяет CAC, а лишь показывает внутреннюю себестоимость sales/onboarding workflow. Основной CAC формируется маркетингом, SDR/AE и длинным циклом продаж.

## 2) COGS на клиента в месяц

### COGS breakdown
| Компонент | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| OCR/LLM inference | 1 800 | ~2 000 документов/мес на клиента, blended cost ~0,9 ₽/док | внутренняя модель на базе 02-demand + типового usage для IDP |
| Storage, очереди, резервирование | 350 | объектное хранилище, очереди, бэкапы | внутренняя оценка infra |
| 1С/ЭДО/API processing | 900 | коннекторы, webhook handling, retries | внутренняя оценка infra |
| Переменный support / CSM | 1 200 | ~0,37 FTE CSM на 50 клиентов | расчёт из FOT |
| Manual exception handling / QA | 1 000 | выборочная ручная валидация и edge cases | расчёт из FOT ops |
| Платёжная и документооборотная обработка | 250 | банк/ЭДО/подпись | внутренняя оценка |
| Амортизация онбординга | 0 | вынесено в CAC, а не в COGS | модель автора |
| **Итого COGS** | **5 500** |  |  |

**Gross profit на клиента:** 25 000 - 5 500 = **19 500 ₽/мес**.

## 3) CAC по каналам с funnel conversion

### Channel CAC
| Канал | Spend, ₽/мес | Воронка | New paying / мес | CAC raw, ₽ | Комментарий |
|---|---:|---|---:|---:|---|
| Paid ads | 180 000 | 600 clicks → 30 leads (5%) → 9 SQL (30%) → 3 pilots (33%) → 1,2 wins (40%) | 1,2 | 150 000 | канал годится для demand capture, но дорог для холодного старта |
| Outbound | 620 000 | 1 200 accounts → 96 replies (8%) → 24 meetings (25%) → 9 pilots (37,5%) → 2,2 wins (24%) | 2,2 | 282 000 | основной early-stage канал для аутсорсеров и multi-client бухгалтерий |
| Events / partners | 100 000 | 20 intros → 10 demos (50%) → 5 pilots (50%) → 1,5 wins (30%) | 1,5 | 66 700 | хороший CAC, но мало объёма |

### Fully-loaded CAC, обязательная раскладка
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools/CRM + Events + Overhead multiplier) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 180 000 | base media spend | модель канала |
| Outbound team FOT (SDR + AE attributed to new) | 689 000 | SDR 170k gross + AE 360k gross, оба ×1,3 соцвзносы | HH.ru benchmark из задания + модель автора |
| Marketing team FOT (partial allocation) | 130 000 | 50% от marketing/product growth нагрузки | внутренняя аллокация |
| Tools (CRM, enrichment, телефония, email) | 58 000 | amoCRM + телефония + email + prospecting stack | внутренняя оценка |
| Events / partnerships | 95 000 | 1 отраслевой ивент/мес + партнёрские активации | внутренняя оценка |
| Subtotal raw CAC pool | 1 152 000 | сумма прямых acquisition затрат | расчёт автора |
| Overhead multiplier (x1.3) | 346 000 | 30% поверх raw pool на management overhead | стандарт enterprise B2B, по инструкции |
| **Итого fully-loaded CAC pool** | **1 498 000** |  |  |
| **New paying customers / мес** | **3,0** | blended из всех каналов | модель автора |
| **Blended fully-loaded CAC** | **499 000 ₽** | 1 498 000 / 3,0 | расчёт автора |

### Sanity check по CAC
- Для **mid-market B2B / fintech** пользовательский benchmark из задания: **200–700k ₽ CAC**. Полученный **499k ₽** лежит в коридоре, значит модель не выглядит заниженной.
- При попытке считать только ads spend CAC упал бы до **150k ₽**, что было бы слишком оптимистично и нарушало бы требование fully-loaded подхода.

## 4) LTV и churn rate

### Churn benchmark
- Для B2B SaaS с ACV ниже enterprise разумный benchmark annual logo churn около **20–30% в год**, что эквивалентно примерно **1,9–2,9% в месяц**.
- Для модели беру **2,5% monthly churn** как середину диапазона, потому что продукт требует внедрения в 1С/ЭДО, но сегмент всё ещё SMB/mid-market, а не тяжёлый enterprise.

Источник benchmark churn:
- SaaS Capital, churn benchmarking: https://www.saas-capital.com/blog-posts/saas-churn-benchmarks/
- CXL summary of B2B SaaS churn ranges: https://cxl.com/blog/saas-churn-benchmarks/

### LTV calculation
Формула:

`LTV = ARPU × Gross Margin % / Monthly churn`

- ARPU = **25 000 ₽/мес**
- Gross Margin = **78%**
- Monthly churn = **2,5%**

`LTV = 25 000 × 0,78 / 0,025 = 780 000 ₽`

**LTV = 780 000 ₽**.

## 5) LTV/CAC ratio

`LTV/CAC = 780 000 / 499 000 = 1,56x`

- Требование investment-grade: **>= 3,0x**.
- Факт: **1,56x**.

**Вывод:** модель окупаемая на горизонте жизни клиента, но для фонда слабая. Это **ниже investable threshold**.

## 6) CAC Payback

`CAC Payback = CAC / MRR per customer = 499 000 / 25 000 = 19,96 мес`

**CAC Payback = 20,0 месяцев**.

Sanity check:
- базовый порог: **< 12 мес**
- допустимо для enterprise: **< 18 мес**
- факт: **20 мес**

**Вывод:** payback слишком длинный.

## 7) Contribution Margin %

`Contribution Margin % = (Revenue - COGS) / Revenue`

`(25 000 - 5 500) / 25 000 = 78%`

**Contribution Margin = 78%**.

Для software + AI-automation это нормально, но высокая валовая маржа не компенсирует дорогой CAC и тяжёлый fixed cost base.

## 8) Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | продажи, fundraising, ключевые партнёры | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, 1С/ЭДО интеграции | 550 000 | 165 000 | 715 000 |
| Senior Backend x2 | ingestion, API, очереди, интеграции | 450 000 ×2 | 270 000 | 1 170 000 |
| ML Engineer | extraction, validation, quality loop | 500 000 | 150 000 | 650 000 |
| DevOps | infra, observability, security | 350 000 | 105 000 | 455 000 |
| Frontend | операторская панель / кабинет | 300 000 | 90 000 | 390 000 |
| Product Manager | workflow design, backlog, analytics | 350 000 | 105 000 | 455 000 |
| SDR | outbound pipeline | 170 000 | 51 000 | 221 000 |
| AE | demo, пилот, closing | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, retention, support | 250 000 | 75 000 | 325 000 |
| **Итого** |  |  |  | **5 694 000 ₽/мес** |

### Hiring realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 each | 585 000 each |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 | 0,75 | 1 | 51 000 | 221 000 |
| AE | 1 | 360 000 | 1,5 | 2,5 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Cumulative FOT timeline M1-M12
Допущение: компания не может реалистично нанять всю команду в M1, поэтому команда подключается постепенно.

| Месяц | Кто уже в штате | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend + Backend #1 | 1 820 000 |
| M3 | M2 + SDR + CSM | 2 366 000 |
| M4 | M3 + CTO + AE + DevOps | 4 004 000 |
| M5 | M4 + Backend #2 | 4 589 000 |
| M6 | M5 + Product Manager | 5 044 000 |
| M7 | M6 + ML Engineer | 5 694 000 |
| M8 | full team | 5 694 000 |
| M9 | full team | 5 694 000 |
| M10 | full team | 5 694 000 |
| M11 | full team | 5 694 000 |
| M12 | full team | 5 694 000 |

**Sanity checks:**
- В первый месяц не нанимается 5+ человек, значит план не ломает time-to-hire realism.
- Но уже к M7 получается burn уровня **5,7 млн ₽/мес только по FOT**, что для SMB fintech wedge очень тяжело.

## 9) Fixed costs breakdown

| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT | 5 694 000 | full team after M7 |
| Infra / cloud / monitoring | 220 000 | production, storage, logs, backups |
| Software / internal tools | 160 000 | dev tools, analytics, support stack |
| Legal / accounting / compliance | 110 000 | договоры, отчётность, безопасность |
| Admin / misc / travel | 90 000 | командировки и операционные мелочи |
| **Итого fixed costs / мес** | **6 274 000 ₽** | без COGS и без acquisition spend |

Если включать acquisition budget как обязательный operating layer, общий monthly burn поднимается до **~7 772 000 ₽/мес**.

## 10) Break-even

### Break-even по числу клиентов
Использую contribution per client = **19 500 ₽/мес**.

`Break-even clients = 6 274 000 / 19 500 = 321,7`

С запасом на недозагрузки support и неполную предсказуемость беру **329 клиентов**.

### Break-even по месяцу
Если компания к концу Y1 выходит только на **50 клиентов**, то:
- MRR = **1 250 000 ₽/мес**
- Gross profit = **975 000 ₽/мес**
- EBITDA до acquisition spend = **975 000 - 6 274 000 = -5 299 000 ₽/мес**

**Вывод:** break-even не достигается в горизонте первых 12 месяцев. Даже при агрессивном росте до **100 клиентов** EBITDA всё ещё отрицательная. На текущем cost base break-even начинается только после **320+ клиентов**.

## Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Burn после сборки команды: **~7,77 млн ₽/мес** с acquisition.
- Чтобы MRR × GM% превысил fixed costs, нужно **~6,27 млн ₽ gross profit**, то есть **~321–329 клиентов**.
- Если net adds идут по 4–5 клиентов/мес после M6, компания не достигает break-even даже за 4+ года.

### Cash runway
Берём `startup_capital = 24 млн ₽`.

`Runway = 24 000 000 / 7 772 000 = 3,1 мес`

Даже если считать усреднённый burn по M1-M12 около **5,1 млн ₽/мес**, runway будет:

`24 000 000 / 5 100 000 = 4,7 мес`

**Вывод:** для такого плана запуска капитал **24 млн ₽** недостаточен. Чтобы дойти до break-even без резкого ужатия команды и CAC, нужен заметно больший капитал. Это соответствует sanity warning из задания: для B2B enterprise-like SaaS капитал до BEP существенно выше **10 млн ₽**.

## Проверка Profit Gate

Условие на reject из задания:
- reject, если **EBITDA < 500k ₽/мес achievable even at 50 clients**, или
- reject, если **LTV/CAC < 1:1**.

Факт:
- при **50 клиентах EBITDA = -5,3 млн ₽/мес**, то есть условие **не выполняется**;
- **LTV/CAC = 1,56x**, это выше 1:1, но всё равно сильно ниже investment-grade.

**Результат Profit Gate: FAIL**.

## Verdict
Кейс экономически **не проходит** в текущем виде.

Почему:
1. **Слишком дорогой go-to-market** для ARPU **25k ₽/мес**.
2. **CAC Payback 20 мес** слишком длинный.
3. **LTV/CAC 1,56x** далеко ниже целевого **>=3x**.
4. Даже при **50 клиентах** бизнес не приближается к EBITDA **500k+ ₽/мес**.
5. Для fund-level investability нужно либо:
   - поднять ARPU в 2-3 раза,
   - резко перейти в white-label / channel sales,
   - либо упростить команду и снизить burn минимум на 35-45%.

На стадии инвестиционного фильтра это **REJECTED**.

## Sources
- [T1] pipeline/cases/ai-pervichka-i-platezhnye-dokumenty-dlya-msb/01-intake.md
- [T2] pipeline/cases/ai-pervichka-i-platezhnye-dokumenty-dlya-msb/02-demand.md
- [T3] SaaS Capital churn benchmarks: https://www.saas-capital.com/blog-posts/saas-churn-benchmarks/
- [T4] CXL churn benchmark summary: https://cxl.com/blog/saas-churn-benchmarks/
- [T5] Salary benchmark ranges supplied in task prompt, HH.ru-based guidance for Moscow/SPb 2026

Primary evidence basis: T1 + T2, with T3/T4 only for churn sanity benchmark.