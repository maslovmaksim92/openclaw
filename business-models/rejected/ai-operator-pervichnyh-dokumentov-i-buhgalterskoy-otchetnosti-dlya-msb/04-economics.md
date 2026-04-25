# 04-economics

## P4 Unit Economics, investment fund level

### Executive summary
- **Модель:** AI-оператор первичных документов и бухгалтерской отчётности для МСБ в формате hybrid managed service, а не pure SaaS.
- **Рабочий ICP:** МСБ с 50-300 первичных документов в месяц, 1С + ЭДО, болью на закрытии периода, сверках и ручном переносе документов.
- **Базовый тариф для расчёта:** **35 000 ₽/клиент/мес**.
- **COGS на клиента:** **13 900 ₽/мес**.
- **Contribution margin:** **60,3%**.
- **Blended fully-loaded CAC:** **219 500 ₽**.
- **Churn benchmark:** **2,5%/мес** для B2B SaaS / tech-enabled service с mid-market motion, взят консервативно между 2-3% как рабочий benchmark. [T5][inference]
- **LTV (gross profit basis):** **843 000 ₽**.
- **LTV/CAC:** **3,84x**.
- **CAC payback:** **6,3 мес**.
- **Ключевая проблема:** при даже приемлемой unit economics на клиента модель **не проходит fund-level Profit Gate** из-за тяжёлой fixed-cost базы, сложного внедрения, длинного ramp и необходимости ops-слоя. При **50 клиентах EBITDA остаётся глубоко отрицательной**.
- **Итог:** **REJECTED**. Причина не в том, что клиентская unit economics совсем сломана, а в том, что компания в реалистичном RU-исполнении не выходит на **EBITDA ≥ 500 тыс. ₽/мес к 50 клиентам**.

---

## 1. Бизнес-процесс: every step from lead to payment

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листов и сегментация | SDR | HH/2ГИС/CRM/таблицы | 45 мин | 1 200 | Low |
| 2 | Первичный outbound / outreach | SDR | почта, телефон, Telegram, CRM | 20 мин | 700 | Medium |
| 3 | Квалификация лида | SDR | CRM, скрипт, чек-лист | 25 мин | 900 | Medium |
| 4 | Discovery call | AE + founder | видеозвонок, CRM, demo deck | 60 мин | 5 200 | Low |
| 5 | Аудит документооборота и pain points | AE + бухгалтер-аналитик | шаблон аудита, 1С/ЭДО checklist | 90 мин | 6 800 | Low |
| 6 | Подготовка пилота / оффера | AE + CTO | калькулятор юнита, шаблон КП | 60 мин | 4 500 | Medium |
| 7 | Техподключение: 1С, ЭДО, банк, почта | implementation / backend | API-коннекторы, ETL, VPN | 4-6 ч | 18 000 | Medium |
| 8 | Загрузка документов и OCR/LLM extraction | AI pipeline | OCR, LLM, rules engine | 10-15 мин на пакет | 1 800 | High |
| 9 | Валидация исключений и бухгалтерское ревью | бухгалтер-ревьюер | 1С, ЭДО, QA interface | 45-60 мин | 7 500 | Low |
| 10 | Подтверждение клиентом спорных кейсов | клиент + CS | Telegram/email/web app | 15 мин | 500 | Medium |
| 11 | Проведение в учёте и формирование отчётности | бухгалтер-ревьюер | 1С, отчётные формы | 30-45 мин | 4 300 | Low |
| 12 | Инвойс, акт, списание оплаты | finance ops | CRM, банк, ЭДО | 15 мин | 700 | High |

### Вывод по процессу
- Автоматизация сильна на extraction / routing / reminders, но слабее всего автоматизируются **исключения, спорные документы, сверки и ответственность за отчётность**.
- Поэтому это не software-only SaaS, а **tech-enabled accounting ops**. Это и поднимает fixed-cost базу.

---

## 2. COGS breakdown на 1 клиента в месяц

### Базовые предпосылки
- Тариф: **35 000 ₽/мес**.
- Средний клиент: 150-250 документов/мес, 1 юрлицо, 1С + ЭДО, ежемесячное закрытие периода.
- Модель: hybrid AI + human exception handling.

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| OCR / LLM inference | 1 800 | распознавание + классификация + валидация пакета документов | [inference] |
| Cloud / storage / monitoring | 900 | compute, storage, резервные копии, логи | [inference] |
| 1С / ЭДО / интеграционный слой | 1 500 | коннекторы, обмен, support integration layer | [T1][T2][inference] |
| Бухгалтер-ревьюер exception handling | 7 500 | ~0,032 FTE fully-loaded бухгалтера-ревьюера на клиента | [T3][inference] |
| Customer success / support | 1 200 | 0,004 FTE CS + коммуникации | [T3][inference] |
| Платёжная и документооборотная обработка | 300 | эквайринг/банк/ЭДО документы | [inference] |
| **Итого COGS** | **13 200** | сумма строк | — |
| Резерв на ошибки, переработки, корректировки | 700 | 2% от выручки как quality reserve | [inference] |
| **Total COGS** | **13 900 ₽** | 13 200 + 700 | — |

### Gross profit на клиента
- Revenue = **35 000 ₽/мес**
- COGS = **13 900 ₽/мес**
- **Gross profit = 21 100 ₽/мес**
- **Gross margin = 60,3%**

---

## 3. CAC by acquisition channel с funnel conversion

### Funnel assumptions
ICP достаточно узкий, поэтому продажи идут через партнёров 1С/аутсорсеров, исходящий outbound и контент/inbound.

| Канал | Leads/мес | Qualified | Demo/diagnostic | Pilot/offer | New paying | CVR lead→paying | Monthly channel cost, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound SMB finance ops | 180 | 54 | 27 | 12 | 3 | 1,7% | 780 000 | 260 000 |
| Партнёры 1С / аутсорс-бухгалтерии | 60 | 30 | 18 | 10 | 4 | 6,7% | 420 000 | 105 000 |
| Контент / inbound / вебинары | 90 | 27 | 12 | 5 | 1 | 1,1% | 270 000 | 270 000 |
| **Blended** | **330** | **111** | **57** | **27** | **8** | **2,4%** | **1 470 000** | **183 750** |

### Fully-loaded CAC (обязательный расчёт)

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | performance + ретаргетинг на узкий ICP | [inference] |
| Outbound team FOT (SDR + AE attributed to new) | 642 000 | SDR 221 000 + AE 421 000 fully-loaded, 100% на new sales | [T3][inference] |
| Marketing team FOT (partial allocation) | 195 000 | 1 demand gen / marketer 390 000 fully-loaded × 50% времени | [T3][inference] |
| Tools (CRM, телефония, enrichment, email) | 93 000 | amoCRM/Bitrix + телефония + рассылки + enrichment stack | [T4][inference] |
| Events / partnerships | 240 000 | вебинары, партнёрские rev-share advance, офлайн-ивенты | [inference] |
| Overhead multiplier (x1.3) | 405 000 | 30% на subtotal 1 350 000 ₽ | [T6][inference] |
| **Итого acquisition spend** | **1 755 000** | сумма строк | — |
| **New paying customers / мес** | **8** | blended funnel | — |
| **Fully-loaded CAC** | **219 375 ₽** | 1 755 000 / 8 | — |

### Sanity-check vs RU benchmark
- Для **mid-market B2B SaaS / tech-enabled service в РФ** ориентир **60-250 тыс. ₽ CAC** выглядит разумным, а enterprise-heavy кейсы могут быть выше. [T6]
- Наш CAC **219 тыс. ₽** находится у верхней границы mid-market и потому **не выглядит искусственно заниженным**.
- Это важно, потому что более низкий CAC здесь был бы red flag: buyer education, интеграции и presale слишком тяжёлые.

---

## 4. LTV с churn rate

### Churn benchmark
- Для B2B subscription / SaaS-сегмента безопасный рабочий benchmark monthly logo churn для mid-market motion находится около **2-3% в месяц**. [T5]
- Для этой модели беру **2,5%/мес** как консервативный midpoint, потому что:
  1. продукт связан с бухгалтерским циклом и потому retention выше, чем у utility SaaS;
  2. но риск churn повышают ошибки, интеграционные проблемы, недоверие к AI и уход обратно в аутсорс/инхаус-бухгалтера. [inference]

### Формула
`LTV = Monthly gross profit per client / monthly churn`

### Расчёт
- Monthly revenue per client = **35 000 ₽**
- Monthly gross profit per client = **21 100 ₽**
- Monthly churn = **2,5%**
- **LTV = 21 100 / 0,025 = 844 000 ₽**

### Альтернативы
| Сценарий | Churn / мес | LTV, ₽ |
|---|---:|---:|
| Оптимистичный | 2,0% | 1 055 000 |
| Базовый | 2,5% | 844 000 |
| Стресс | 3,5% | 603 000 |

---

## 5. LTV/CAC ratio

- **LTV = 844 000 ₽**
- **Fully-loaded CAC = 219 375 ₽**
- **LTV/CAC = 3,84x**

### Вывод
- Формально **>= 3:1**, то есть на уровне клиента экономика выглядит **проходной**.
- Но для investment grade этого недостаточно, если fixed-cost и burn profile ломают equity story на уровне компании.

---

## 6. CAC Payback

Формула:
`CAC Payback = CAC / MRR per customer`

- CAC = **219 375 ₽**
- MRR per customer = **35 000 ₽**
- **CAC Payback = 6,27 мес**

### Вывод
- По правилу sanity-check это **нормально**: меньше 12 месяцев.
- Но payback хороший только при условии, что клиент реально доходит до стабильного production-режима и не создаёт сверхнормативные exception-costs.

---

## 7. Contribution Margin %

Формула:
`Contribution Margin % = (Revenue - COGS) / Revenue`

- Revenue = **35 000 ₽**
- COGS = **13 900 ₽**
- Contribution per client = **21 100 ₽**
- **Contribution Margin = 60,3%**

### Интерпретация
- Для software-only SaaS это слабовато.
- Для tech-enabled accounting ops это ещё приемлемо, но показывает, что scale зависит не только от роста клиентов, а от жёсткого контроля exception handling.

---

## 8. Full team table: роли, функции, зарплаты

### Team & FOT

| Роль | Нужно чел. | Функция | Salary gross ₽/мес (RU 2026) | Time-to-hire, мес | Ramp до 80% productivity, мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---:|---|---:|---:|---:|---:|---:|
| CEO / founder | 1 | продажи, fundraising, ключевые клиенты | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO / Tech Lead | 1 | архитектура, security, delivery | 550 000 | 2,0 | 2,0 | 165 000 | 715 000 |
| Senior Backend | 2 | интеграции 1С/ЭДО, backend core | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | extraction, routing, quality models | 500 000 | 2,5 | 2,0 | 150 000 | 650 000 |
| DevOps | 1 | infra, monitoring, deploy, backups | 350 000 | 1,5 | 1,0 | 105 000 | 455 000 |
| Frontend / product engineer | 1 | reviewer UI, client cabinet | 280 000 | 1,0 | 1,0 | 84 000 | 364 000 |
| SDR | 1 | outbound pipeline | 170 000 | 0,75 | 1,0 | 51 000 | 221 000 |
| AE | 1 | discovery, demo, close | 324 000 | 1,5 | 2,5 | 97 200 | 421 200 |
| Customer Success | 1 | onboarding, retention, approvals | 220 000 | 1,0 | 1,0 | 66 000 | 286 000 |
| Бухгалтер-ревьюер / operations | 2 | исключения, контроль проводок, отчётность | 180 000 | 1,0 | 1,0 | 54 000 | 234 000 each |
| Product / BizOps | 1 | процессы, тарифы, аналитика | 300 000 | 2,0 | 1,5 | 90 000 | 390 000 |

### Комментарий по найму
- На бумаге можно захотеть 7-8 человек с первого месяца, но это **нереалистично** по time-to-hire.
- Отдельный риск: бухгалтер-ревьюер не редкий найм, но CTO/ML/AE для такого домена нанимаются не мгновенно.
- Поэтому revenue ramp всегда отстаёт от burn ramp.

---

## 9. Cumulative FOT timeline M1-M12

### План подключения команды
- **M1:** CEO, 1 Senior Backend
- **M2:** CTO
- **M3:** Frontend, бухгалтер-ревьюер #1
- **M4:** DevOps
- **M5:** SDR
- **M6:** AE
- **M7:** Senior Backend #2
- **M8:** ML Engineer
- **M9:** Customer Success
- **M10:** Product/BizOps
- **M11:** бухгалтер-ревьюер #2
- **M12:** без новых наймов

| Месяц | Кто в штате к концу месяца | Monthly FOT, ₽ |
|---|---|---:|
| M1 | CEO, Backend1 | 1 326 000 |
| M2 | + CTO | 2 041 000 |
| M3 | + Frontend, Reviewer1 | 2 639 000 |
| M4 | + DevOps | 3 094 000 |
| M5 | + SDR | 3 315 000 |
| M6 | + AE | 3 736 200 |
| M7 | + Backend2 | 4 282 200 |
| M8 | + ML | 4 932 200 |
| M9 | + CS | 5 218 200 |
| M10 | + Product/BizOps | 5 608 200 |
| M11 | + Reviewer2 | 5 842 200 |
| M12 | без изменений | 5 842 200 |

### Sanity check
- В M1 команда не раздута, нарушений time-to-hire нет.
- Но уже к M8-M12 FOT почти **5,0-5,8 млн ₽/мес**, что типично для серьёзного B2B/ops-heavy контура и сразу делает путь к break-even длинным.

---

## 10. Fixed costs breakdown

Ниже беру fixed cost base для стадии после формирования ядра команды, без переменной части COGS.

| Fixed cost item | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 842 200 | как в M11-M12 |
| Office / legal / accounting / admin | 220 000 | юрлицо, бухгалтерия, документооборот, минимальный офис/коворкинг |
| Infra base not in COGS | 180 000 | общая dev/prod база, мониторинг, security |
| Software stack internal | 140 000 | dev tools, repos, analytics, PM tools |
| Compliance / legal reserve | 120 000 | договоры, ИБ, претензии, регуляторика |
| Founder travel / sales overhead | 150 000 | встречи, командировки, партнёры |
| **Total fixed OPEX / мес** | **6 652 200 ₽** | без переменного COGS |

### Важное замечание
Если пытаться урезать fixed cost слишком сильно, то ломается либо delivery quality, либо скорость найма, либо enterprise readiness. Поэтому агрессивный оптимизм здесь опасен.

---

## 11. Break-even по client count и по month

### Break-even by client count
Формула:
`Break-even clients = Fixed OPEX / contribution per client`

- Fixed OPEX = **6 652 200 ₽/мес**
- Contribution per client = **21 100 ₽/мес**
- **Break-even = 315 клиентов**

### Conservative trimmed team scenario
Даже если убрать Product/BizOps, второго reviewer и снизить founder cash comp, fixed OPEX можно теоретически опустить до **~5,0 млн ₽/мес**.

- 5 000 000 / 21 100 = **237 клиентов**

### Вывод
- Реальный break-even лежит в диапазоне **237-315 клиентов**, а не 30-50.
- Следовательно, тезис из demand stage о достаточности 25-50 клиентов для уверенного EBITDA не выдерживает full fund-level расчёта.

### Break-even by month
Берём консервативный ramp новых платящих клиентов:

| Месяц | Активные клиенты | MRR, ₽ | GP / contribution, ₽ | EBITDA before tax, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | -1 726 000 |
| M2 | 0 | 0 | 0 | -2 441 000 |
| M3 | 2 | 70 000 | 42 200 | -2 956 800 |
| M4 | 4 | 140 000 | 84 400 | -3 409 600 |
| M5 | 7 | 245 000 | 147 700 | -3 787 300 |
| M6 | 11 | 385 000 | 232 100 | -4 204 100 |
| M7 | 16 | 560 000 | 337 600 | -4 744 600 |
| M8 | 22 | 770 000 | 464 200 | -5 368 000 |
| M9 | 28 | 980 000 | 590 800 | -5 775 400 |
| M10 | 35 | 1 225 000 | 738 500 | -5 913 700 |
| M11 | 42 | 1 470 000 | 886 200 | -6 016 000 |
| M12 | 50 | 1 750 000 | 1 055 000 | **-5 997 200** |

### Ключевой вывод
- **Даже при 50 клиентах EBITDA около -6,0 млн ₽/мес** на fully-loaded базе.
- Компания **не достигает +500 тыс. ₽ EBITDA/мес даже близко**.
- Profit Gate по уровню компании провален.

---

## 12. Burn-to-breakeven

### Оценка burn
- Средний monthly burn в M1-M12 при описанном ramp = примерно **4,7-5,0 млн ₽/мес**.
- До выхода хотя бы на operational break-even компании нужно довести базу до **~240-315 клиентов**.
- Даже при net adds 8-10 клиентов/мес после стабилизации путь до break-even составляет **24-30+ месяцев**.

### Burn-to-breakeven estimate
- При среднем burn **4,8 млн ₽/мес** и горизонте **18 месяцев** до попытки догнать более зрелый sales engine требуется **~86 млн ₽** cash consumption.
- Это без тяжёлых просадок по churn, без внеплановых доработок по 1С/ЭДО и без плохой дебиторки.

### Вывод
Для категории с высокой интеграционной сложностью и умеренным ARPU это слишком капиталоёмкая история для фонда, если нет сильного channel advantage.

---

## 13. Cash runway

### Допущение
- `startup_capital = 40 000 000 ₽`

### Расчёт
- При среднем burn **4,8 млн ₽/мес**:
- **Cash runway = 40 000 000 / 4 800 000 = 8,3 месяца**

### Интерпретация
- Runway **короче реального времени до scale-ready GTM**, значит компании почти наверняка потребуется новый раунд до unit-stable стадии.
- Чтобы честно дотянуться хотя бы до near-break-even режима, нужен капитал скорее **70-90 млн ₽**, либо очень сильный партнёрский канал с дешёвым привлечением и delivery leverage.

---

## 14. Investment committee verdict

### Что хорошо
- На уровне **одного клиента** юнит проходит: contribution margin 60,3%, payback 6,3 мес, LTV/CAC 3,84x.
- Есть реальная боль, обязательные workflows и рынок, который уже платит за бухгалтерский outcome.

### Что ломает кейс
1. **Слишком тяжёлая fixed-cost база** для такого ARPU.
2. **Exception handling не исчезает**, а значит software gross margin ограничен.
3. **Длинный hire ramp** и сложный внедренческий контур делают burn-front-loaded.
4. **При 50 клиентах EBITDA остаётся сильно отрицательной**, то есть обязательный Profit Gate не пройден.
5. Без крупного channel partner или радикального повышения чека до уровня managed BPO + multi-entity bundle equity story слабая.

## Final decision
- **Profit Gate: FAIL**
- **LTV/CAC gate: PASS**
- **Fund-level verdict: REJECTED**

Причина reject: **компания не достигает EBITDA ≥ 500 тыс. ₽/мес даже при 50 клиентах на реалистичной fully-loaded модели**.

---

## Sources
- **T1:** ФНС и нормативный контур по электронной отчётности / УПД, использованы в demand stage и evidence.
- **T2:** Saby, 1С, Контур, Т-Банк, 1С:БухОбслуживание, использованы в demand stage для price anchors и market reality.
- **T3:** HH.ru salary benchmark по ролям в Москве/СПб для finance ops / product / engineering / sales. https://hh.ru/
- **T4:** CRM / sales tooling price anchors, например amoCRM / Bitrix24 pricing pages. https://www.amocrm.ru/ ; https://www.bitrix24.ru/prices/
- **T5:** churn benchmark по B2B subscriptions / SaaS, рабочий диапазон 2-3% monthly. https://recurly.com/research/churn-rate-benchmarks/ ; https://www.saastr.com/b2b-saas-churn-benchmarks/
- **T6:** RU CAC sanity benchmark из инвестиционной практики для SMB / mid-market / enterprise B2B SaaS, задан в программных инструкциях этого цикла.

## Bottom line
У кейса есть спрос и может быть нормальная экономика на одного клиента, но **на уровне фонда история неинвестируема**: чтобы добраться до устойчивого break-even, нужно слишком много капитала, людей и времени относительно attainable ARPU в российском МСБ-бухгалтерском сегменте.
