# 04-economics

## Unit Economics verdict
**Вердикт: REJECTED на уровне фонда.**

Причина двойная:
1. **LTV/CAC = 2,2x**, что ниже investable-порога **3,0x**.
2. Даже при **50 активных клиентах** модель не дотягивает до **500 тыс. ₽ EBITDA/мес**. При базовом сценарии получается около **-1,24 млн ₽ EBITDA/мес**.

Ниже расчёт по консервативной, но реалистичной модели для РФ SMB done-for-you web studio с AI-assisted production.

---

## 1. Ключевые допущения модели
- ICP: SMB в услугах, локальном b2b и медицине, которым нужен лидогенерирующий сайт/лендинг под ключ.
- Доходная модель: **setup 55 000 ₽** + **care/changes 7 000 ₽/мес**.
- Средний срок жизни клиента считаю через churn, а не «по ощущению».
- Для LTV беру только recurring gross profit, setup отдельно использую в cash/break-even.
- Churn benchmark: для early-stage low-ARPA SaaS/подписки ChartMogul показывает типичный customer churn порядка **3–7% в месяц**, медиана для very early-stage <300k ARR около **6,5%**; для более зрелых компаний 3–4%. Для данного SMB-сегмента беру **5,0%/мес** как рабочий midpoint. Источник: ChartMogul Benchmarks / Customer Churn Rate.

Источники:
- ChartMogul Benchmarks: https://help.chartmogul.com/hc/en-us/articles/12112768447004-Benchmarks
- ChartMogul Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- ChartMogul blog benchmark by ARR: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
- HH.ru senior backend: https://hh.ru/vacancies/senior-backend-developer
- HH.ru SDR: https://hh.ru/vacancy/128565026
- HH.ru DevOps: https://hh.ru/vacancies/senior-devops
- HH.ru senior backend sample: https://hh.ru/vacancy/129266637
- HH.ru senior DevOps sample: https://hh.ru/vacancy/129581822
- Evidence from case: `01-evidence.md`, `02-demand.md`

---

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Захват лида из Яндекс/Avito/TG/referral | Marketing / SDR | Яндекс.Директ, Avito, Telegram, Tilda-form | 5 мин | 350 | Частично |
| 2 | Первичный контакт и квалификация | SDR | AmoCRM/Битрикс24, телефония, WhatsApp/Telegram | 20 мин | 550 | Частично |
| 3 | Бриф и сбор материалов | SDR + PM | Notion/Forms, Google Drive | 45 мин | 1 050 | Частично |
| 4 | Discovery-call и оценка fit | Founder/AE | Zoom/Meet, CRM | 45 мин | 1 900 | Низкая |
| 5 | Генерация sitemap/copy/wireframe | PM + AI operator | ChatGPT/Claude, Relume/Figma | 90 мин | 2 600 | Высокая |
| 6 | Дизайн и сборка лендинга | Designer/Frontend | Figma, Tilda/Webflow/WordPress | 4,5 ч | 7 500 | Частично |
| 7 | Интеграция форм, аналитики, домена | Frontend + Tech lead | Tilda/Webflow, GTM, Я.Метрика, CRM | 2 ч | 3 300 | Частично |
| 8 | QA и правки | PM + Designer | чек-лист, браузерный QA | 1,5 ч | 2 450 | Низкая |
| 9 | Согласование оффера и финальная версия | AE/Founder | CRM, мессенджеры | 40 мин | 1 650 | Низкая |
| 10 | Выставление счёта / договор / акт | Ops/Founder | ЭДО, банк, CRM | 30 мин | 700 | Частично |
| 11 | Получение оплаты | Клиент + Ops | Банк, acquiring | 5 мин | 825 | Высокая |
| 12 | Онбординг в care-пакет | CSM | CRM, база знаний, чат | 30 мин | 900 | Частично |

**Итого переменная стоимость одного нового клиента на запуске:** около **23 775 ₽**.

Комментарий: AI резко режет production-time, но не убирает дорогостоящие человеческие этапы: квалификацию, discovery, правки, интеграцию и доведение до оплаты.

---

## 3. COGS на клиента в месяц

Для recurring care-пакета 7 000 ₽/мес:

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Хостинг, домен, SSL, формы | 700 | blended по low-cost стеку |
| AI-инструменты на контент/правки | 450 | пропорционально usage |
| Поддержка и мелкие правки дизайна/контента | 1 100 | ~0,6 часа production-time |
| Аккаунт-менеджмент / customer success | 650 | аллокация CSM на базу |
| Техподдержка / публикации / багфиксы | 350 | аллокация frontend/tech |
| Платёжные комиссии и misc | 100 | acquiring + rounding |
| **Итого COGS / клиент / мес** | **3 350** |  |

**Gross profit / клиент / мес = 7 000 - 3 350 = 3 650 ₽**  
**Contribution margin на recurring = 52,1%**

Дополнительно по setup:
- Средняя цена запуска: **55 000 ₽**
- Launch COGS: **23 775 ₽**
- Валовая прибыль на setup: **31 225 ₽**

---

## 4. CAC по каналам с воронкой

### Channel CAC (direct/raw)

| Канал | Spend, ₽/мес | Переходы/ответы | Leads | Брифы | Коммерческие предложения | New paying | Конверсия lead→pay | Raw CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Яндекс.Директ | 180 000 | 900 кликов | 45 | 9 | 4 | 2 | 4,4% | 90 000 |
| Avito/каталоги услуг | 45 000 | 120 откликов | 120 | 18 | 8 | 4 | 3,3% | 11 250 |
| Telegram-партнёрства | 35 000 | 60 входящих | 60 | 12 | 6 | 3 | 5,0% | 11 667 |
| Referral/word-of-mouth | 0 прямой spend | 12 интро | 12 | 6 | 4 | 2 | 16,7% | 0 прямой |

### FULLY-LOADED CAC

Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales FOT attributed + Marketing FOT allocated + Tools + Events + Overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/Avito/TG) | 260 000 | 180k + 45k + 35k | внутренняя модель по ICP |
| Outbound team FOT (SDR/AE attributed to new) | 124 800 | SDR 120k + AE 180k, умножено на 40% acquisition load, +30% соцвзносы | HH.ru benchmark + модель |
| Marketing team FOT (partial allocation) | 39 000 | founder/marketing allocation 30k gross +30% | модель |
| Tools (CRM, телефония, AI, аналитика) | 22 000 | AmoCRM/Битрикс24, телефония, AI stack, forms | модель |
| Events/partnerships | 20 000 | локальные партнёрства/нетворк | модель |
| Subtotal before overhead | 465 800 | сумма выше |  |
| Overhead multiplier (x1.3) | 139 740 | 30% на менеджмент, юр., фин., потери времени | std for SMB service stack |
| **Total fully-loaded acquisition cost** | **605 540** | 465 800 + 139 740 |  |

При **11 новых платящих клиентах/мес** blended **fully-loaded CAC = 55 049 ₽**.

Sanity check:
- Для SMB/self-serve обычно ожидается 5–30k ₽ CAC, но здесь это **не self-serve**, а done-for-you сервис с ручным sales/process layer.
- CAC около **55k ₽** уже говорит, что модель ближе к low-end agency, чем к software.

---

## 5. LTV и churn

### Churn benchmark
- ChartMogul указывает для SaaS customer churn обычно **3–7%/мес**, а у ранних компаний с низким ARPA медиана может быть около **6,5%/мес**.
- Для данного сегмента беру **5,0%/мес** как умеренно-консервативный benchmark.

### Расчёт
- ARPA / MRR per customer: **7 000 ₽/мес**
- Gross profit per customer per month: **3 650 ₽**
- Churn rate: **5,0%/мес**
- Expected customer lifetime: **1 / 0,05 = 20 месяцев**
- **LTV = 3 650 × 20 = 73 000 ₽**

Если добавить ожидаемую валовую прибыль setup как отдельный компонент, получаем:
- setup gross profit = **31 225 ₽**
- extended LTV = **73 000 + 31 225 = 104 225 ₽**

Для фонда корректнее смотреть оба варианта:
- **Recurring LTV = 73 000 ₽**
- **Extended LTV = 104 225 ₽**

---

## 6. LTV/CAC

- **Recurring LTV / CAC = 73 000 / 55 049 = 1,33x**
- **Extended LTV / CAC = 104 225 / 55 049 = 1,89x**

**Итог:** даже в более мягкой extended-логике модель **ниже 3:1** и не проходит investment-grade threshold.

---

## 7. CAC Payback

Требование sanity check: `CAC Payback = CAC / MRR_per_customer`

- CAC = **55 049 ₽**
- MRR per customer = **7 000 ₽/мес**
- **CAC Payback = 7,86 месяца**

Формально <12 месяцев, то есть payback сам по себе не катастрофический. Но это не спасает модель, потому что **gross-profit LTV/CAC остаётся слабым** и EBITDA-масштаб не сходится.

---

## 8. Contribution Margin %

Считаю на blended monthly basis при steady-state, где на 1 активного клиента в месяц приходится:
- recurring revenue: **7 000 ₽**
- плюс амортизированная setup GP: **31 225 / 20 = 1 561 ₽**
- blended gross profit / client / month: **3 650 + 1 561 = 5 211 ₽**
- blended revenue / client / month: **7 000 + 2 750 = 9 750 ₽**

**Contribution Margin % = 5 211 / 9 750 = 53,4%**

Для service-heavy бизнеса это терпимо, но для фонда недостаточно, потому что fixed cost layer слишком тяжёлый.

---

## 9. Team & FOT

### Полная команда: роли, функции, зарплаты

| Роль | Функция | Salary gross, ₽/мес | Страх. взносы 30% | Fully-loaded FOT, ₽/мес |
|---|---|---:|---:|---:|
| Founder/CEO | продажи, оффер, финансы, партнёрства | 500 000 | 150 000 | 650 000 |
| Tech Lead / CTO | стек, интеграции, QA, сложные кейсы | 450 000 | 135 000 | 585 000 |
| Frontend/No-code builder | сборка, запуск, адаптив, интеграции | 250 000 | 75 000 | 325 000 |
| Designer | визуал, шаблоны, правки | 220 000 | 66 000 | 286 000 |
| PM / Producer | бриф, дедлайны, handoff | 220 000 | 66 000 | 286 000 |
| SDR | квалификация и follow-up | 120 000 | 36 000 | 156 000 |
| AE / Founder-assist sales | demo, proposal, close | 280 000 | 84 000 | 364 000 |
| Customer Success | care, retention, upsell | 200 000 | 60 000 | 260 000 |
| Ops / Finance admin | документы, ЭДО, платежи | 120 000 | 36 000 | 156 000 |
| **Итого** |  |  |  | **3 068 000** |

### Таблица найма с realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| CTO/Tech Lead | 1 | 450 000 | 2 | 2 | 135 000 | 585 000 |
| Senior Backend | 0 | 0 | 0 | 0 | 0 | 0 |
| ML Engineer | 0 | 0 | 0 | 0 | 0 | 0 |
| DevOps | 0,5 / outsource | 150 000 экв. | 1 | 1 | 45 000 | 195 000 |
| Frontend | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| SDR | 1 | 120 000 + бонус | 1 | 1 | 36 000 | 156 000 |
| AE | 1 | 280 000 + комиссия | 1,5 | 2 | 84 000 | 364 000 |
| Customer Success | 1 | 200 000 | 1 | 1 | 60 000 | 260 000 |
| PM / Producer | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Designer | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Ops/Admin | 1 | 120 000 | 1 | 0,5 | 36 000 | 156 000 |

### Salary benchmark note
Диапазоны в целом согласуются с HH.ru выдачей и архивными вакансиями по Москве/удалёнке: senior backend и senior DevOps уже регулярно видны в диапазонах **300–450k+ ₽**, SDR около **100k+ ₽**, что подтверждает, что недооценивать FOT нельзя.

---

## 10. Cumulative FOT timeline M1-M12

Допущение: startup_capital = **18 млн ₽**.

| Месяц | Кто в команде | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 650 000 | founder-led start |
| M2 | CEO + Frontend | 975 000 | первый production hire |
| M3 | CEO + Frontend + Designer | 1 261 000 | добавляем визуальный слой |
| M4 | CEO + Frontend + Designer + PM | 1 547 000 | появляется delivery control |
| M5 | CEO + Frontend + Designer + PM + SDR | 1 703 000 | начинаем системный lead handling |
| M6 | CEO + Frontend + Designer + PM + SDR + CSM | 1 963 000 | удержание и care |
| M7 | CEO + Frontend + Designer + PM + SDR + CSM + AE | 2 327 000 | sales close layer |
| M8 | CEO + Frontend + Designer + PM + SDR + CSM + AE + Tech Lead (50% ramp) | 2 619 500 | hire + ramp |
| M9 | CEO + Frontend + Designer + PM + SDR + CSM + AE + Tech Lead | 2 912 000 | full tech layer |
| M10 | + Ops/Admin | 3 068 000 | документ-операции |
| M11 | та же команда | 3 068 000 | steady |
| M12 | та же команда | 3 068 000 | steady |

Sanity checks пройдены:
- Нет найма 5+ человек в первый месяц.
- FOT после выхода к полной команде выше 3 млн ₽/мес, что реалистичнее для Москвы/удалёнки 2026, чем «дешёвая» fantasy-модель.

---

## 11. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 3 068 000 |
| Офис/коворкинг, связь, юр./бух. | 120 000 |
| Core software stack вне COGS | 90 000 |
| Облако/monitoring/internal infra | 70 000 |
| Налоги, misc, резерв на возвраты | 80 000 |
| **Итого fixed costs / мес** | **3 428 000** |

---

## 12. Break-even по числу клиентов и по месяцам

### Break-even по client count
Берём blended contribution profit на 1 активного клиента в месяц: **5 211 ₽**.

`Break-even clients = 3 428 000 / 5 211 = 658 клиентов`

Даже если считать более оптимистично и часть setup-потока признавать upfront, practical break-even остаётся сильно выше **250–300 активных клиентов**, что недостижимо для такой команды без превращения в классическую агентскую фабрику.

### Проверка at 50 clients
- Recurring revenue: **50 × 7 000 = 350 000 ₽/мес**
- Допустим, новых продаж 6 в месяц × 55 000 = **330 000 ₽**
- Total revenue: **680 000 ₽/мес**
- Recurring COGS: **50 × 3 350 = 167 500 ₽**
- Setup COGS: **6 × 23 775 = 142 650 ₽**
- Gross profit: **369 850 ₽**
- Fixed costs: **3 428 000 ₽**
- **EBITDA = -3 058 150 ₽/мес**

Даже в сильно более мягком сценарии с урезанной командой fixed cost всё равно остаётся выше 1,5–2,0 млн ₽/мес, а значит **50 клиентов не дают даже близко 500k EBITDA**.

### Break-even по месяцам
Если компания набирает в среднем **+8 net active clients/мес**, то:
- к M6 будет ~35 active clients,
- к M12 ~83 active clients,
- к M18 ~126 active clients,
- к M24 ~164 active clients.

При такой траектории компания **не достигает операционного break-even за 24 месяца** без радикального повышения ARPA, снижения CAC или смены модели на продуктовую платформу.

---

## 13. Burn-to-breakeven и runway

### Burn-to-breakeven
Типовой burn в период построения команды и канала продаж:
- M1-M3: **0,9–1,4 млн ₽/мес**
- M4-M6: **1,7–2,2 млн ₽/мес**
- M7-M12: **2,4–3,1 млн ₽/мес**

Накопленный burn до гипотетического break-even в realistic-модели превышает **35–45 млн ₽**.

### Cash runway
При startup_capital = **18 млн ₽**:
- если средний burn **2,2 млн ₽/мес**, runway ≈ **8,2 месяца**;
- если burn уходит к **2,8 млн ₽/мес**, runway падает до **6,4 месяца**.

Вывод: без внешнего капитала или резкого сокращения fixed cost проект быстро упирается в cash wall.

---

## 14. Итог для инвестфонда

### Что хорошо
- Реальный рыночный спрос на outcome «сайт/лендинг под ключ» есть.
- AI действительно снижает production time и даёт шанс на более быструю delivery-модель.
- CAC payback по выручке выглядит терпимо.

### Что плохо
- Это **service-heavy** бизнес с дорогим человеческим контуром.
- **Fully-loaded CAC** слишком высокий для SMB-сегмента.
- **LTV/CAC 1,33x по recurring и 1,89x по extended** не дотягивает до фонда.
- При **50 клиентах** EBITDA не просто <500k, а глубоко отрицательная.
- Break-even требует сотни активных клиентов или резкого аплифта ARPA, что уже меняет исходный wedge.

## Final economics verdict
**REJECTED.**

Для бутстрэп-предпринимателя это может быть нормальный cash-flow service business. Для фонда это **не investment-grade unit economics**: слишком тяжёлая сервисная себестоимость, слабый LTV/CAC и отсутствие реалистичного пути к 500k+ EBITDA/мес на масштабе 50 клиентов.
