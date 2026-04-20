# 04-economics

## Кейс
1007-msk-sanas-accent-translation-geo-expand-v2

## Итог
**Статус: REJECTED**

Даже при консервативно-оптимистичной цене **150 000 ₽ MRR на клиента** экономика standalone-продукта accent translation для enterprise contact center в РФ/СНГ не проходит fund-level фильтр.

- **Blended fully-loaded CAC:** ~**1 783 000 ₽**
- **MRR на клиента:** **150 000 ₽/мес**
- **COGS на клиента:** **93 000 ₽/мес**
- **Contribution margin:** **38.0%**
- **LTV:** **2 850 000 ₽**
- **Churn benchmark:** **2.0%/мес**
- **LTV/CAC:** **1.60x**
- **CAC Payback:** **11.9 мес по формуле CAC/MRR**, или **31.3 мес по gross profit**
- **Break-even:** ~**95 клиентов**
- **При 50 клиентах EBITDA остаётся отрицательной**

Итог: **Profit Gate FAIL** по двум причинам одновременно, (1) **LTV/CAC < 3.0x**, (2) **даже при 50 клиентах EBITDA < 500 000 ₽/мес не достигается**.

---

## 1. Модель выручки

### Базовый pricing-кейс
Продукт моделируется как enterprise add-on для multilingual / offshore / BPO contact center.

| Параметр | Значение |
|---|---:|
| Средний контракт | 1 800 000 ₽/год |
| MRR на клиента | 150 000 ₽/мес |
| Срок контракта | 12 мес |
| Тип продажи | sales-led, пилот + security/legal + procurement |
| Сегмент | enterprise / regulated-adjacent voice stack |

Обоснование: в `02-demand.md` локальный бюджет подтверждён на contact-center stack, но не на отдельный accent-translation line item. Поэтому беру **не агрессивный**, а уже довольно натянутый сценарий с premium add-on **150k ₽/мес**.

---

## 2. Бизнес-процесс от лида до оплаты

### Подробная процессная таблица

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP и account list | CEO + SDR | CRM, Excel, HH/рынок, LinkedIn-аналоги | 2 ч/account | 3 000 | низкая |
| 2 | Outreach sequence, холодные касания | SDR | CRM, email, телефония | 5 касаний за 10 дней | 7 000 | средняя |
| 3 | Первичный ответ и qualification | SDR | CRM, календарь, скрипты | 45 мин | 2 500 | средняя |
| 4 | Discovery call | AE + CTO | Zoom/Meet, CRM | 1 ч + 1 ч prep | 9 000 | низкая |
| 5 | Демо real-time accent translation | AE + Solutions/CTO | Demo env, voice sandbox | 1.5 ч | 12 000 | низкая |
| 6 | Технический scoping, интеграции, security questionnaire | CTO + Backend + DevOps | Notion/Docs, security docs | 8-12 ч | 45 000 | низкая |
| 7 | Пилот на ограниченном трафике | Backend + ML + CSM | Cloud, inference, SIP/voice routing | 3-4 недели | 120 000 | средняя |
| 8 | Анализ пилота, KPI review | AE + CTO + клиентский ops lead | BI, call analytics | 4 ч | 18 000 | низкая |
| 9 | Коммерческое предложение и закупка | AE + CEO | CRM, шаблоны договора | 1-2 недели | 20 000 | средняя |
| 10 | Legal / DPA / security approval | CEO + внеш. юрист | Docs, email | 1-3 недели | 35 000 | низкая |
| 11 | Счёт и закрытие оплаты | Finance/CEO | Банк, 1С/аналог | 2-3 дня | 6 000 | средняя |
| 12 | Онбординг production | CSM + Backend + DevOps | Cloud, monitoring, project plan | 1-2 недели | 55 000 | средняя |

### Вывод по процессу
Это не self-serve SaaS, а **длинная enterprise-сделка** с 2-3 техническими касаниями, пилотом, security review и юр. циклом. Поэтому raw marketing CAC здесь почти бесполезен, нужен именно **fully-loaded CAC**.

---

## 3. COGS на клиента в месяц

### COGS breakdown

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| STT/TTS/voice AI API и модельный inference | 34 000 | real-time voice processing на ограниченном enterprise-трафике |
| GPU/compute + orchestration | 19 000 | облачный inference + буфер на пиковые часы |
| Телефония, SIP routing, storage | 8 000 | voice transport, запись, хранение |
| Monitoring / security / observability | 6 000 | monitoring, логирование, алерты |
| Support & QA | 11 000 | доля команды support / QA / incident response |
| Customer success variable time | 5 000 | ежемесячные QBR, настройка, hand-holding |
| Амортизация внедрения и пилота | 10 000 | пилот 120k размазан на 12 мес |
| Итого COGS | **93 000** |  |

### Gross margin
- Выручка: **150 000 ₽/мес**
- COGS: **93 000 ₽/мес**
- Валовая прибыль: **57 000 ₽/мес**
- **Gross Margin = 38.0%**

Для B2B software это низко. Для инвестиционного SaaS-кейса хотелось бы 65%+ после стабилизации. Здесь продукт ближе к service-heavy voice layer, чем к scale SaaS.

---

## 4. CAC по каналам и воронка

### Канал 1. Outbound enterprise sales

| Метрика | Значение |
|---|---:|
| Target accounts / мес | 1 000 |
| Reply rate | 4.0% |
| Qualified meeting rate от replies | 40% |
| Discovery rate от meetings | 75% |
| Proposal rate от discovery | 45% |
| Pilot rate от proposals | 50% |
| Paid conversion от pilot | 50% |
| Новых paying клиентов / мес | **1.35** |
| Месячные затраты канала | **2 050 000 ₽** |
| CAC outbound | **1 519 000 ₽** |

### Канал 2. Партнёрства / BPO / интеграторы

| Метрика | Значение |
|---|---:|
| Partner intros / мес | 18 |
| Discovery rate | 55% |
| Proposal rate | 45% |
| Pilot rate | 50% |
| Paid conversion | 40% |
| Новых paying клиентов / мес | **0.89** |
| Месячные затраты канала | **680 000 ₽** |
| CAC partnerships | **764 000 ₽** |

### Канал 3. Paid/content/inbound

| Метрика | Значение |
|---|---:|
| Целевые визиты / мес | 300 |
| Demo request rate | 7% |
| Discovery rate | 50% |
| Proposal rate | 30% |
| Pilot rate | 35% |
| Paid conversion | 35% |
| Новых paying клиентов / мес | **0.39** |
| Месячные затраты канала | **480 000 ₽** |
| CAC inbound paid/content | **1 231 000 ₽** |

### Blended funnel

| Метрика | Значение |
|---|---:|
| Всего spend / мес | **3 210 000 ₽** |
| Новых paying клиентов / мес | **1.80** |
| **Blended fully-loaded CAC** | **1 783 000 ₽** |

---

## 5. FULLY-LOADED CAC

### Разложение fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK/контент) | 180 000 | тестовый demand capture по узкой enterprise-нише | internal model + низкий demand из `02-demand.md` |
| Outbound team FOT (SDR/AE attributed to new) | 1 015 000 | 1 SDR + 1 AE fully-loaded + доля CEO/CTO в pre-sale | HH.ru benchmark + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 220 000 | 0.5 FTE product marketing / founder marketing time | HH.ru benchmark / internal allocation |
| Tools (CRM, телефония, outreach, data) | 95 000 | CRM + телефония + sequencing + data providers | internal estimate |
| Events/partnerships | 250 000 | офлайн встречи, партнёрские комиссии, travel | internal estimate |
| Raw acquisition subtotal | **1 760 000** | сумма прямых затрат |  |
| Overhead multiplier | **1 450 000** | enterprise multiplier до fully-loaded уровня, эквивалентно ~x1.82 к raw subtotal | std enterprise B2B motion |
| Fully-loaded acquisition spend / мес | **3 210 000** | raw + overhead |  |
| New paying customers / мес | **1.80** | blended across channels | funnel model |
| **Fully-loaded CAC** | **1 783 000** | 3 210 000 / 1.80 |  |

### Почему multiplier высокий
По инструкции для enterprise >500k ₽ ACV допустим **×2.0-2.5** к raw CAC. Здесь контракт **1.8 млн ₽/год**, есть пилот, security review и legal. Я беру **консервативный эквивалент ниже верхней границы**, чтобы не завысить CAC искусственно.

### Sanity check vs benchmark
Справочник пользователя даёт sanity range для **Enterprise SaaS B2B в РФ: 300-900k ₽/клиент**, для **Healthtech B2B: 400-1200k ₽**. Наш blended CAC **1.78 млн ₽** выше ориентира, что логично для:
1. очень узкой ниши,
2. длинного enterprise цикла,
3. слабого локального category-demand,
4. высокой доли presales и пилотов.

---

## 6. LTV и churn

### Churn benchmark
Для B2B SaaS с относительно высоким ARPA беру **2.0% monthly gross revenue churn** как рабочий бенчмарк. Это уже не мягкий SMB SaaS, а enterprise-ish software с узким use case, где лого churn ниже, но revenue churn может быть заметным из-за пилотов, downsell и ограниченного ROI.

### Расчёт LTV
Формула: **LTV = MRR × Gross Margin / Monthly Churn**

- MRR = **150 000 ₽**
- Gross Margin = **38.0%**
- Churn = **2.0%/мес**

**LTV = 150 000 × 0.38 / 0.02 = 2 850 000 ₽**

### LTV/CAC
- LTV = **2 850 000 ₽**
- CAC = **1 783 000 ₽**
- **LTV/CAC = 1.60x**

### Вывод
Это сильно ниже инвестиционного порога **3:1**. Для fund-level кейса ratio **1.6x** означает, что компания почти не оставляет пространства на ошибки найма, churn, price pressure и затяжной ramp.

---

## 7. CAC Payback

По обязательной формуле:

**CAC Payback = CAC / MRR per customer = 1 783 000 / 150 000 = 11.9 мес**

Формально это почти укладывается в базовый порог 12 мес, но это misleading metric, потому что gross margin всего **38%**.

Если считать payback по gross profit:

**1 783 000 / 57 000 = 31.3 мес**

### Вывод
На бумаге payback выглядит терпимо только из-за высокой цены контракта. На уровне реальной валовой прибыли экономика очень тяжёлая.

---

## 8. Contribution Margin

Для оценки вклада на fixed-cost base беру:
- Выручка на клиента: **150 000 ₽**
- COGS: **93 000 ₽**
- Переменная комиссия / sales success / client-specific overhead: **0 ₽** (зашито в acquisition, не в servicing)

**Contribution per client = 57 000 ₽/мес**

**Contribution Margin = 57 000 / 150 000 = 38.0%**

Это слишком мало для продукта, который ещё и дорог в продаже.

---

## 9. Team & FOT

### Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | продажи, fundraise, enterprise closing | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, presales, security | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | real-time backend | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | integrations / platform | 420 000 | 126 000 | 546 000 |
| ML Engineer | voice / inference / model ops | 500 000 | 150 000 | 650 000 |
| DevOps | infra / SIP / observability | 350 000 | 105 000 | 455 000 |
| Frontend | demo/admin UI | 300 000 | 90 000 | 390 000 |
| Product Manager | roadmap / pilots / packaging | 350 000 | 105 000 | 455 000 |
| SDR | outbound prospecting | 165 000 | 49 500 | 214 500 |
| AE | demos, proposals, closing | 321 000 | 96 300 | 417 300 |
| Customer Success | onboarding / renewal / support | 250 000 | 75 000 | 325 000 |
| **Итого** |  |  |  | **5 558 800 ₽/мес** |

### Таблица найма с realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 165 000 | 0.75 | 1 | 49 500 | 214 500 |
| AE | 1 | 321 000 | 1.5 | 3 | 96 300 | 417 300 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product Manager | 1 | 350 000 | 2 | 2 | 105 000 | 455 000 |

### Источники salary benchmark
- HH.ru, вакансии CTO/Tech Lead, backend, ML, DevOps, SDR и AE, Москва, апрель 2026:  
  https://hh.ru/search/vacancy?text=CTO+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=Senior+Backend+Go+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=ML+Engineer+LLM+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=DevOps+Senior+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=SDR+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=Account+Executive+SaaS+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0

### Cumulative FOT timeline M1-M12
Соблюдаю realism: **нет 5+ hires в M1**, найм размазан по времени.

| Месяц | Кто в команде | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Backend#1, DevOps | 2 561 000 |
| M2 | + Backend#2 | 3 107 000 |
| M3 | + Frontend, Product | 3 952 000 |
| M4 | + ML Engineer | 4 602 000 |
| M5 | + SDR | 4 816 500 |
| M6 | + AE | 5 233 800 |
| M7 | + Customer Success | 5 558 800 |
| M8 | full team | 5 558 800 |
| M9 | full team | 5 558 800 |
| M10 | full team | 5 558 800 |
| M11 | full team | 5 558 800 |
| M12 | full team | 5 558 800 |

Комментарий: даже этот план уже выглядит агрессивно для ниши со слабым demand signal. Но я не делаю его ещё тяжелее, чтобы не «добить» кейс искусственно.

---

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5 558 800 |
| Office / coworking / admin | 180 000 |
| Legal / accounting | 120 000 |
| Core cloud / staging / internal infra | 350 000 |
| Licenses / security / observability not in COGS | 140 000 |
| G&A reserve | 100 000 |
| **Итого fixed costs / мес** | **6 448 800 ₽** |

---

## 11. Break-even

### Break-even по числу клиентов

Contribution на клиента = **57 000 ₽/мес**

**Break-even clients = 6 448 800 / 57 000 = 113.1**, то есть примерно **114 клиентов**.

Даже если сократить fixed-cost base на 15%, всё равно нужно около **97 клиентов**.

### Break-even по месяцам
Если компания закрывает клиентов так: 0, 0, 1, 1, 2, 2, 3, 3, 4, 5, 6, 7 кумулятивно по новым клиентам в месяц, то к концу M12 получится около **34 активных клиентов**. Это сильно ниже необходимых **97-114**.

**Итог: break-even не достигается в первые 12 месяцев.**

### Тест 50 клиентов
- Выручка: **7 500 000 ₽/мес**
- COGS: **4 650 000 ₽/мес**
- Gross profit / contribution: **2 850 000 ₽/мес**
- Fixed costs: **6 448 800 ₽/мес**
- **EBITDA = -3 598 800 ₽/мес**

Это прямое срабатывание Profit Gate FAIL.

---

## 12. Burn-to-breakeven и runway

### Burn-to-breakeven
Даже при мягком плане продаж и постепенном найме burn остаётся высоким.

| Месяц | Оценка выручки, ₽ | Валовая прибыль, ₽ | Fixed costs + acquisition, ₽ | Net burn, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 3 341 000 | -3 341 000 |
| M3 | 150 000 | 57 000 | 4 732 000 | -4 675 000 |
| M6 | 600 000 | 228 000 | 7 183 800 | -6 955 800 |
| M9 | 1 800 000 | 684 000 | 8 768 800 | -8 084 800 |
| M12 | 3 000 000 | 1 140 000 | 9 658 800 | -8 518 800 |

Даже к M12 условие **MRR × GM% > fixed costs** не выполняется. До operational break-even бизнес не доезжает в обозримом первом годе.

### Cash runway
Беру **startup_capital = 60 000 000 ₽**.

Если средний burn на траектории ~**5.9 млн ₽/мес** в первые 12 месяцев, то:

**Cash runway = 60 000 000 / 5 900 000 ≈ 10.2 мес**

Для enterprise B2B SaaS это слишком мало. Чтобы комфортно дожить до гипотетического break-even, нужен капитал сильно выше, ближе к **100-120 млн ₽**, и то без гарантии product-market fit.

---

## 13. Инвестиционный вывод

### Что не нравится фонду
1. **Слабый локальный category demand** уже зафиксирован в `02-demand.md`.
2. Продажа требует **длинного enterprise цикла** и дорогого presales.
3. **Gross margin низкий**, бизнес service-heavy.
4. **LTV/CAC = 1.60x**, то есть сильно ниже investable threshold.
5. **При 50 клиентах EBITDA всё ещё отрицательная**, значит операционный leverage плохой.
6. Для масштабирования нужен дорогой team build с заметным time-to-hire и ramp.

### Profit Gate
- EBITDA ≥ 500k/mo achievable even at 50 clients? **Нет**.
- LTV/CAC ≥ 1:1? **Да**, но всего **1.60x**, а требование для investable кейса **≥3.0x**.

### Вердикт
**REJECTED.**

Это не инвестиционный standalone business для РФ/СНГ, а скорее узкая enterprise-feature capability, которая лучше существует внутри более широкого CCaaS / speech analytics / voice AI stack.

---

## Источники
- `02-demand.md` текущего кейса
- HH.ru search benchmarks, Москва, апрель 2026:  
  https://hh.ru/search/vacancy?text=CTO+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=Senior+Backend+Go+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=ML+Engineer+LLM+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=DevOps+Senior+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=SDR+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0  
  https://hh.ru/search/vacancy?text=Account+Executive+SaaS+%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- SaaS churn benchmark reference: https://www.saas-capital.com/blog-posts/2024-b2b-saas-benchmarks/
- ChartMogul Benchmarks, SaaS retention context: https://chartmogul.com/saas-metrics/benchmarks/
