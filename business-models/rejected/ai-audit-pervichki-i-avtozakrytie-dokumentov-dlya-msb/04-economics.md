# Unit Economics

## Итог
- **Статус:** FAIL
- **Сегмент модели:** mid-market B2B SaaS для бухгалтерского аутсорса и document-heavy SMB, 1С-first.
- **Главный вывод:** при нормальном hire-plan и fully-loaded CAC продукт может быть эффективным на уровне одного клиента, но **не дотягивает до инвестиционного profitability gate**. Даже на **50 платящих клиентах** EBITDA остаётся глубоко отрицательной.
- **Причина reject:** для AI-core продукта под 1С/ЭДО нужна слишком тяжёлая команда внедрения и разработки относительно доступного ARPA в РФ SMB. Unit economics по клиенту терпимая, но fund-level economics плохая.

## 1) Основные допущения модели
- ICP: бухгалтерский аутсорс 20-200 клиентских юрлиц и multi-entity SMB с большим потоком первички.
- Средний контракт: **35 000 ₽/мес** на клиента.
- One-time onboarding fee: **40 000 ₽**, в MRR/EBITDA не включаю как устойчивую выручку.
- Средний цикл сделки: **2 месяца**.
- Валовая маржа до sales & fixed overhead считается после прямого COGS.
- Для churn беру ориентир **2.5% в месяц** для B2B SaaS SMB/mid-market, что соответствует бенчмаркам порядка 2-3% monthly churn для не-enterprise B2B SaaS. [T6]

## 2) Подробный бизнес-процесс: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Генерация лида через партнёра, outbound или вебинар | SDR / маркетинг | HH-база, CRM, e-mail, Telegram, вебинар-платформа | 20 мин | 900 | Низкая |
| 2 | Первый контакт и квалификация | SDR | Bitrix24/amoCRM, телефония | 30 мин | 1 400 | Низкая |
| 3 | Discovery-call по pain и объёму документов | AE | CRM, Meet/Telegram | 60 мин | 3 500 | Низкая |
| 4 | Сбор sample docs и доступов | AE + solutions/CS | защищённый upload, почта, 1С-коннектор | 90 мин | 5 000 | Средняя |
| 5 | Pilot setup: правила, OCR, маппинг, тестовые проводки | CSM + backend/ML | 1С-коннектор, OCR/LLM, облако | 6 ч | 18 000 | Средняя |
| 6 | Pilot run на 1-2 неделях документов | CSM + клиентский бухгалтер | AI pipeline, dashboard | 4 ч | 12 000 | Средняя |
| 7 | Разбор ошибок и ROI-калькуляция | AE + CSM | BI, ROI sheet | 2 ч | 7 000 | Низкая |
| 8 | Согласование коммерческого предложения | AE + CEO | CRM, шаблон КП | 2 ч | 8 000 | Низкая |
| 9 | Юридическое согласование и DPA/152-ФЗ | CEO + юрист аутсорс | шаблоны договора | 3 ч | 12 000 | Низкая |
| 10 | Выставление счёта | back-office / CEO | банк, 1С | 20 мин | 800 | Высокая |
| 11 | Оплата и активация | back-office + CSM | банк, CRM, product admin | 30 мин | 1 200 | Высокая |
| 12 | Ежемесячное сопровождение и обработка инцидентов | CSM + support | helpdesk, CRM, Telegram | 1.5 ч/мес | 4 500 | Средняя |

**Вывод:** sales motion не self-serve. Это pilot-led B2B продажа с заметной долей ручного presale и onboarding, поэтому CAC и burn выше, чем у лёгкого SMB SaaS.

## 3) COGS на 1 клиента в месяц
Предполагаю клиента с 1 500-2 500 документами в месяц и регулярной сверкой/закрытием.

| Статья COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| OCR / распознавание и извлечение | 1 600 | usage-based inference + распознавание пакета первички | T1, T2, внутренняя модель |
| LLM / правила валидации / классификация | 1 000 | inference и повторные проверки | внутренняя модель |
| Облако, хранение, резервирование | 700 | storage + compute + secure backups | внутренняя модель |
| Интеграции и мониторинг | 600 | коннекторы 1С/ЭДО, логирование | внутренняя модель |
| Customer support / success variable | 1 500 | ~1.5 ч/мес поддержки на портфель | внутренняя модель |
| Платежи и прочие переменные | 300 | банк, документооборот, misc | внутренняя модель |
| **Итого COGS** | **5 700** |  |  |

- **Выручка на клиента:** 35 000 ₽/мес
- **Contribution per client before CAC:** 29 300 ₽/мес
- **Contribution Margin:** **83.7%**

## 4) Fully-loaded CAC
### Компоненты blended CAC
Предполагаю зрелый месяц, в котором компания получает **6 новых платящих клиентов**.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 120 000 | тестовый performance budget на ICP-запросы и ретаргет | внутренняя GTM-модель |
| Outbound team FOT (SDR + доля AE, attributed to new) | 455 000 | SDR 170k gross + AE 180k attributed gross, всё ×1.3 | HH.ru benchmarks, внутренняя аллокация |
| Marketing team FOT (partial allocation) | 117 000 | 90k gross attributed на acquisition ×1.3 | внутренняя аллокация |
| Tools (CRM, телефония, enrichment, e-mail) | 38 000 | Bitrix24/amoCRM + телефония + outreach stack | T7 |
| Events / partnerships | 70 000 | вебинар, партнёрские комиссии, co-marketing | внутренняя GTM-модель |
| Overhead multiplier (x1.3) | 240 000 | 30% на management overhead, finance/legal, misc | стандартное допущение B2B sales |
| **Итого fully-loaded CAC spend** | **1 040 000** |  |  |

- **Новые платящие клиенты/мес:** 6
- **Blended fully-loaded CAC:** **173 000 ₽**
- Sanity check: для mid-market SaaS это попадает в рабочий диапазон **60-250k ₽**, то есть CAC не выглядит заниженным.

### CAC по каналам и funnel conversion
| Канал | Верх воронки | SQL | Demo | Pilot | Paid | Конверсия lead→paid | Spend, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Партнёры 1С / бухгалтерские бюро | 24 | 14 | 10 | 6 | 3 | 12.5% | 270 000 | 90 000 |
| Outbound SDR | 900 аккаунтов | 54 replies | 18 | 7 | 1 | 0.11% от аккаунтов | 360 000 | 360 000 |
| Контент / вебинары / inbound | 80 MQL | 18 | 10 | 5 | 2 | 2.5% | 170 000 | 85 000 |
| **Blended** | — | — | — | — | **6** | — | **800 000 raw / 1 040 000 fully-loaded** | **173 000** |

**Вывод:** лучший канал, как и в demand stage, это **партнёры 1С и бухгалтерский аутсорс**. Но он ограничен по scale, а outbound слишком дорогой для ARPA 35k.

## 5) LTV и churn
### Бенчмарк churn
- Для B2B SaaS в SMB/mid-market разумно закладывать **2-3% monthly churn**; в модели беру **2.5%**. [T6]

### Расчёт
- ARPA = **35 000 ₽/мес**
- Gross Margin = **83.7%**
- Monthly churn = **2.5%**
- **LTV = ARPA × GM / churn = 35 000 × 0.837 / 0.025 = 1 171 800 ₽**

## 6) LTV/CAC
- **LTV/CAC = 1 171 800 / 173 000 = 6.8x**
- Формально это выше порога **3:1** и выглядит investable на уровне отдельного клиента.
- Но фондовый profitability gate всё равно **не пройден**, потому что fixed-cost base слишком тяжёлая относительно achievable ARPA и темпа набора клиентов.

## 7) CAC Payback
- **CAC Payback = CAC / MRR per customer = 173 000 / 35 000 = 4.9 месяца**
- По правилу sanity check это нормально, но short payback здесь **не спасает** модель от burn.

## 8) Team & FOT
### Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1.5 | 1.5 | 270 000 | 1 170 000 |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 | 0.5 | 1 | 51 000 | 221 000 |
| AE | 1 | 360 000 | 1.5 | 3 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| **Итого full team** | **10** | — | — | — | — | **5 239 000** |

### Функции команды
| Роль | Функция | Salary gross ₽/мес | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|
| CEO | продажи крупных сделок, финансы, партнёры | 650 000 | 845 000 |
| CTO | архитектура, безопасность, data pipeline | 550 000 | 715 000 |
| Senior Backend x2 | интеграции 1С/ЭДО, core backend | 900 000 | 1 170 000 |
| ML Engineer | extraction, validation, ranking, quality loops | 500 000 | 650 000 |
| DevOps | on-prem/VPC, CI/CD, monitoring | 350 000 | 455 000 |
| Frontend | кабинет бухгалтера, dashboard ошибок | 300 000 | 390 000 |
| SDR | outbound и первичная квалификация | 170 000 | 221 000 |
| AE | demo, pilot, closing | 360 000 | 468 000 |
| Customer Success | pilot onboarding, удержание, support | 250 000 | 325 000 |
| **Итого** |  |  | **5 239 000** |

### Cumulative FOT timeline M1-M12
В первом месяце не нанимаю 5+ человек одновременно, чтобы не нарушать hiring realism.

| Месяц | Кто уже в штате / подключился | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend + SDR + Customer Success | 1 781 000 |
| M3 | CEO + Frontend + SDR + Customer Success + Backend #1 + DevOps + AE | 3 125 000 |
| M4 | M3 + Backend #2 | 3 710 000 |
| M5 | M4 + CTO | 4 425 000 |
| M6 | M5 + ML Engineer | 5 075 000 |
| M7 | полная команда | 5 239 000 |
| M8 | полная команда | 5 239 000 |
| M9 | полная команда | 5 239 000 |
| M10 | полная команда | 5 239 000 |
| M11 | полная команда | 5 239 000 |
| M12 | полная команда | 5 239 000 |

**Вывод по найму:** даже аккуратный hire plan даёт очень тяжёлый monthly burn. Для такого ARPA команда выглядит экономически несоразмерной.

## 9) Fixed costs breakdown
| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 239 000 | full team с соцвзносами |
| Облако core / dev / staging сверх COGS | 220 000 | shared infra, monitoring, backup |
| Юридическое и бухгалтерское сопровождение | 120 000 | договоры, 152-ФЗ, vendor docs |
| Офис / коворкинг / admin | 90 000 | гибридный режим |
| Прочий G&A | 110 000 | банки, SaaS, канцелярия, misc |
| **Итого fixed costs** | **5 779 000** |  |

## 10) Contribution Margin %
- Выручка = **35 000 ₽/клиент/мес**
- Переменный COGS = **5 700 ₽/клиент/мес**
- **Contribution Margin = (35 000 - 5 700) / 35 000 = 83.7%**

Это хороший software-like показатель, но при таком fixed-cost base его недостаточно.

## 11) Break-even
### По числу клиентов
- Contribution per client = **29 300 ₽/мес**
- Fixed costs = **5 779 000 ₽/мес**
- **Break-even clients = 5 779 000 / 29 300 = 197.2**, округляю до **198 клиентов**

### По выручке в месяц
- **Break-even revenue/month = 198 × 35 000 = 6 930 000 ₽/мес**

### Проверка gate на 50 клиентах
| Метрика | Значение |
|---|---:|
| Клиенты | 50 |
| MRR | 1 750 000 ₽ |
| COGS | 285 000 ₽ |
| Валовая прибыль | 1 465 000 ₽ |
| Fixed costs | 5 779 000 ₽ |
| **EBITDA** | **-4 314 000 ₽/мес** |

**Итог:** требование Program 5 не выполнено. **Даже на 50 клиентах EBITDA не просто ниже 500k, а сильно отрицательная.**

## 12) Burn-to-breakeven и runway
### Burn-to-breakeven
Если считать, что к M12 компания дорастает лишь до 30 клиентов, то:
- MRR = **1 050 000 ₽**
- GP = **879 000 ₽**
- Fixed costs (full team) = **5 779 000 ₽**
- Burn = **-4 900 000 ₽/мес** примерно

Даже при 60 клиентах:
- GP = **1 758 000 ₽**
- EBITDA = **-4 021 000 ₽/мес**

То есть burn остаётся высоким очень долго, а breakeven отъезжает далеко за пределы комфортного seed-stage диапазона.

### Cash runway
Берём **startup_capital = 25 000 000 ₽**.
- Средний burn M1-M6 ≈ **3.8 млн ₽/мес**
- После разворота полной команды burn ≈ **4.5-5.0 млн ₽/мес** до заметного клиентского масштаба
- **Оценочный runway = 5-6 месяцев** до необходимости нового финансирования

Sanity check пройден в негативную сторону: capital required до breakeven заметно выше 10 млн ₽ и фактически ближе к 50-70 млн ₽, если строить полноценную компанию, а не lifestyle-tool.

## 13) Финальный инвестиционный вывод
### Что хорошо
- Unit economics на уровне одного клиента **не катастрофическая**: CM 83.7%, CAC payback 4.9 мес, LTV/CAC 6.8x.
- Есть более дешёвый и качественный канал через партнёров 1С и бухгалтерский аутсорс.

### Что ломает кейс
1. **ARPA недостаточен** для required team size в AI + integrations + security-heavy продукте.
2. **Break-even только около 198 клиентов**, что для такого сегмента слишком далеко и капиталоёмко.
3. **На 50 клиентах EBITDA = -4.3 млн ₽/мес**, то есть profitability gate Program 5 провален.
4. Чтобы пройти gate, пришлось бы либо сильно поднять чек, либо радикально урезать продукт до OCR/add-on слоя, что уже занято 1С/Saby и ухудшает moat.

## Вердикт
- **Profit Gate:** FAIL
- **LTV/CAC:** PASS
- **Overall investment verdict:** **REJECT**

## Sources
- **T1:** https://v8.1c.ru/its/services/1s-raspoznavanie-pervichnykh-dokumentov/cena-1s-raspoznavanie-pervichnykh-dokumentov/
- **T2:** https://sbis.spb.ru/brand_sbis/document_recognition/
- **T3:** https://hh.ru/vacancies/buhgalter-po-uchetu-pervichnoj-dokumentatsii
- **T4:** https://hh.ru/search/vacancy?text=SDR
- **T5:** https://hh.ru/search/vacancy?text=Account%20Executive
- **T6:** https://www.optifai.ai/blog/saas-churn-rate-benchmarks
- **T7:** https://www.bitrix24.ru/prices/
