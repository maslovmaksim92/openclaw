---
stage: P4
created: 2026-05-13T02:13:00+03:00
case: ai-logotipy-svg-ikonki-i-brand-assets-za-minuty
verdict: REJECTED
segment_focus: mid-market B2B white-label/API для агентств, конструкторов сайтов и SMB-платформ
---

# Unit economics

## Итог
**Вердикт: REJECTED.**

Спрос подтверждён, CAC и LTV сами по себе выглядят рабочими, но **profit gate не проходит**: при реалистичной команде и fully-loaded FOT компания **не достигает EBITDA 500 тыс. ₽/мес даже на 50 клиентах**. Для безубыточности нужно около **128 платящих клиентов**, что слишком далеко от порога программы для фонда на этой стадии.

## Модель, сегмент и базовые допущения
- Основной сегмент: **mid-market B2B** white-label/API, а не дешёвый B2C one-off.
- Продукт: генерация логотипов, SVG-иконок, brand-kit и production-ready assets для агентств, SMB-конструкторов и маркетинговых платформ.
- Средний контракт: **55 000 ₽ MRR на клиента**.
- Sales cycle: **~1.5 месяца**.
- Gross churn: **3.0% в месяц** как консервативный benchmark для SMB/mid-market SaaS. Это внутри диапазона **2.5–3.0% monthly** для B2B SaaS у OptiMine/Optifi benchmark 2025 и соответствует тезису SaaS Capital о более низком churn у большего ACV и более высоком у малого сегмента [T6, T7].
- Startup capital для модели runway: **36 млн ₽**.

## 1) Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листов агентств и конструкторов | SDR | HH/2GIS/сайт-листы, Google Sheets | 20 мин/лид | 180 | Низкая |
| 2 | Enrichment контактов | SDR | CRM + почтовый enrichment | 10 мин/лид | 90 | Средняя |
| 3 | Первый outbound/email/Telegram outreach | SDR | CRM, email sequencing | 15 мин/лид | 140 | Средняя |
| 4 | Follow-up 2-3 касания | SDR | CRM, шаблоны сообщений | 20 мин/лид | 190 | Средняя |
| 5 | Qualification call | SDR + AE | Meet/Zoom, CRM | 30 мин | 420 | Низкая |
| 6 | Demo с кейсами и sandbox | AE | Meet, live demo, Figma/landing | 45 мин | 620 | Низкая |
| 7 | Технический scoping и estimation | CTO/Backend | Notion, API docs | 60 мин | 1 200 | Низкая |
| 8 | Пилот 7-14 дней | AE + CTO + ML | sandbox, API keys, support chat | 10 дней | 6 500 | Средняя |
| 9 | Коммерческое предложение и договор | AE + CEO | шаблон оффера, e-sign | 2 дня | 1 100 | Средняя |
| 10 | Счёт и оплата | AE + accountant | банк, ЭДО | 3 дня | 450 | Высокая |
| 11 | Onboarding клиента | CSM + Frontend/Backend | help center, templates, API docs | 5 рабочих дней | 8 000 | Средняя |
| 12 | Ежемесячный usage review и upsell | CSM | CRM, BI dashboard | 60 мин/мес | 1 200 | Средняя |

**Вывод:** процесс длиннее, чем казалось в intake. Это не self-serve SMB CAC, а фактически **mid-market B2B sale с пилотом**, поэтому нужен SDR/AE/CSM слой, а не только перформанс-маркетинг.

## 2) COGS на клиента в месяц

База: **MRR 55 000 ₽ на клиента**.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Inference / генерация brand-assets | 4 200 | blended cost: open-source pipeline + часть premium API вызовов, ограниченный пакет usage |
| Хранение, CDN, delivery | 350 | облако + object storage |
| Support / CSM variable load | 1 400 | ~0.4 часа CSM на клиента в месяц |
| Onboarding amortized | 900 | 8 000 ₽ единовременно, амортизация на 9 мес |
| Платёжный эквайринг и billing | 1 650 | ~3% от MRR |
| Резерв на retry/quality/manual fixes | 1 100 | ручные правки, повторные рендеры |
| **Итого COGS** | **9 600** |  |

- **Gross profit / клиент / мес = 55 000 - 9 600 = 45 400 ₽**
- **Gross Margin = 82.5%**

## 3) CAC по каналам с funnel conversion

### Канальные воронки

| Канал | Верх воронки | MQL / meeting | SQL / demo | Win | Конверсия в платящего | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Paid ads + content | 1 200 визитов | 60 лидов | 12 demo | 4 клиента | 0.33% от визита / 6.7% от лида | 97 500 |
| Outbound | 1 500 аккаунтов | 90 ответов | 30 встреч | 3 клиента | 0.20% от аккаунта / 3.3% от ответа | 132 300 |
| Partnerships / events | 40 интро | 20 встреч | 8 proposals | 2 клиента | 5.0% от интро / 10% от встречи | 162 500 |

### Fully-loaded CAC

Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | тестовый paid budget | внутренняя модель |
| Outbound team FOT (SDR/AE attributed to new) | 455 000 | SDR 234k + 50% AE 221k | HH.ru benchmark + модель [T2, T5] |
| Marketing team FOT (partial allocation) | 120 000 | 0.4 FTE growth/generalist | рынок RU 2026, внутренняя модель |
| Tools (CRM, sequencer, аналитика, domain/email) | 57 000 | amo/HubSpot-lite + почтовые инструменты | внутренняя модель |
| Events/partnerships | 120 000 | 1 отраслевой митап + партнёрские комиссии | внутренняя модель |
| Overhead multiplier (x1.6 для mid-market B2B) | 372 000 | на базу 932k, long sales cycle | стандарт mid-market B2B из задания |
| **Итого fully-loaded acquisition cost / мес** | **1 304 000** |  |  |
| **Новых платящих клиентов / мес** | **9** | 4 paid + 3 outbound + 2 partnerships | модель |
| **Blended fully-loaded CAC** | **144 900** | 1 304 000 / 9 |  |

### Sanity check по benchmark
- Для **mid-market SaaS** из задания ориентир **60-250k ₽ CAC**.
- Полученный **blended CAC 144.9k ₽** выглядит **реалистично** и не занижен.
- Канальный CAC у партнёрств выше, но допустим за счёт большего чека и ниже churn.

## 4) LTV с churn benchmark

### Churn benchmark
- Для SMB/mid-market B2B SaaS разумно брать **3.0% monthly gross churn** как консервативную оценку для early-stage продукта [T6, T7].
- Это даёт lifetime около **33.3 месяца**.

### Расчёт LTV
- MRR = **55 000 ₽**
- Gross profit / мес = **45 400 ₽**
- Monthly churn = **3.0%**
- Lifetime = **1 / 0.03 = 33.3 мес**
- **LTV = 45 400 × 33.3 = 1 513 820 ₽**

## 5) LTV/CAC ratio

- **LTV/CAC = 1 513 820 / 144 900 = 10.45x**

Формально метрика **выше 3:1** и сама по себе инвестиционно хорошая. Но это **не спасает кейс**, потому что структура fixed costs слишком тяжёлая для 50-клиентной базы.

## 6) CAC Payback

По правилу задания:
- **CAC Payback = CAC / MRR per customer = 144 900 / 55 000 = 2.64 месяца**

Дополнительно по gross profit:
- **Payback on gross profit = 144 900 / 45 400 = 3.19 месяца**

Это хороший показатель, но profit gate всё равно не проходит из-за heavy team load.

## 7) Contribution Margin %

Для вклада на покрытие фиксированных расходов считаю commission/discount reserve как variable SG&A:

| Элемент | ₽/клиент/мес |
|---|---:|
| Выручка | 55 000 |
| COGS | -9 600 |
| AE commission reserve | -1 650 |
| Promo/discount reserve | -1 250 |
| **Contribution profit** | **42 500** |

- **Contribution Margin = 42 500 / 55 000 = 77.3%**

## 8) Полная команда: роли, функции, зарплаты

### Базовая operating team

| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO/founder | продажи enterprise-lite, fundraising, strategy | 1 | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | архитектура, data/integration | 1 | 550 000 | 165 000 | 715 000 |
| Senior Backend | API, billing, integrations | 2 | 400 000 | 120 000 | 1 040 000 |
| ML Engineer | генерация, prompt/evals, routing | 1 | 500 000 | 150 000 | 650 000 |
| DevOps | infra, CI/CD, observability | 1 | 320 000 | 96 000 | 416 000 |
| Frontend | кабинеты, onboarding UI | 1 | 280 000 | 84 000 | 364 000 |
| SDR | outbound prospecting | 1 | 180 000 | 54 000 | 234 000 |
| AE | demo, pilot, close | 1 | 350 000 | 105 000 | 455 000 |
| Customer Success | onboarding, retention, expansion | 1 | 230 000 | 69 000 | 299 000 |
| **Итого FOT fully-loaded** |  | **10** |  |  | **5 018 000** |

### Hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2.0 | 2.0 | 165 000 | 715 000 |
| Senior Backend | 2 | 400 000 | 1.5 | 1.5 | 120 000 | 520 000 / чел |
| ML Engineer | 1 | 500 000 | 2.5 | 2.0 | 150 000 | 650 000 |
| DevOps | 1 | 320 000 | 1.5 | 1.0 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1.0 | 1.0 | 84 000 | 364 000 |
| SDR | 1 | 180 000 | 0.75 | 1.0 | 54 000 | 234 000 |
| AE | 1 | 350 000 | 1.5 | 2.5 | 105 000 | 455 000 |
| Customer Success | 1 | 230 000 | 1.0 | 1.0 | 69 000 | 299 000 |

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend | 1 209 000 |
| M3 | CEO + Frontend + CTO + Backend #1 | 2 444 000 |
| M4 | M3 + ML + SDR | 3 328 000 |
| M5 | M4 + Backend #2 + DevOps | 4 264 000 |
| M6 | M5 + AE | 4 719 000 |
| M7 | M6 + CSM | 5 018 000 |
| M8 | steady state | 5 018 000 |
| M9 | steady state | 5 018 000 |
| M10 | steady state | 5 018 000 |
| M11 | steady state | 5 018 000 |
| M12 | steady state | 5 018 000 |

**Sanity checks:**
- В первый месяц не нанимается 5+ человек, значит time-to-hire не нарушен.
- FOT для команды 5-7+ человек быстро выходит выше **4 млн ₽/мес**, что подтверждает: cheap-SMB интуиция из intake была слишком оптимистичной для B2B/API модели.

## 9) Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 018 000 |
| Базовая инфраструктура и observability | 160 000 |
| G&A, бухгалтерия, юристы, ЭДО | 130 000 |
| SaaS/tools non-acquisition | 90 000 |
| Офис/коворкинг/админ-расходы | 130 000 |
| **Итого fixed costs / мес** | **5 528 000** |

## 10) Break-even по числу клиентов и по месяцам

### Break-even by client count
- Contribution profit на клиента = **42 500 ₽/мес**
- Fixed costs = **5 528 000 ₽/мес**
- **Break-even clients = 5 528 000 / 42 500 = 130.1**, округляю до **131 клиента**

### Check на 50 клиентах
- Выручка = **50 × 55 000 = 2 750 000 ₽/мес**
- Contribution profit = **50 × 42 500 = 2 125 000 ₽/мес**
- EBITDA до прочих = **2 125 000 - 5 528 000 = -3 403 000 ₽/мес**

**Profit Gate FAIL:** при **50 клиентах EBITDA не только не >= 500k ₽/мес, а глубоко отрицательная**.

### Month-by-month ramp

| Месяц | Клиенты EOM | MRR, ₽ | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 355 000 | -1 355 000 |
| M2 | 1 | 55 000 | 42 500 | 1 719 000 | -1 676 500 |
| M3 | 3 | 165 000 | 127 500 | 2 954 000 | -2 826 500 |
| M4 | 6 | 330 000 | 255 000 | 3 838 000 | -3 583 000 |
| M5 | 10 | 550 000 | 425 000 | 4 774 000 | -4 349 000 |
| M6 | 15 | 825 000 | 637 500 | 5 229 000 | -4 591 500 |
| M7 | 21 | 1 155 000 | 892 500 | 5 528 000 | -4 635 500 |
| M8 | 28 | 1 540 000 | 1 190 000 | 5 528 000 | -4 338 000 |
| M9 | 35 | 1 925 000 | 1 487 500 | 5 528 000 | -4 040 500 |
| M10 | 43 | 2 365 000 | 1 827 500 | 5 528 000 | -3 700 500 |
| M11 | 51 | 2 805 000 | 2 167 500 | 5 528 000 | -3 360 500 |
| M12 | 60 | 3 300 000 | 2 550 000 | 5 528 000 | -2 978 000 |

### Burn-to-breakeven
- До выхода на **131 клиента** компания сжигает капитал весь первый год.
- Кумулятивный burn за M1-M12 по таблице выше: **40.4 млн ₽**.
- Это больше выбранного startup capital **36 млн ₽**, то есть без допфинансирования компания не доживает до break-even.

### Cash runway
- Startup capital = **36 млн ₽**
- Средний burn M1-M12 = **~3.37 млн ₽/мес**
- **Cash runway = 36 / 3.37 = 10.7 месяца**

## Вывод для фонда

Экономика парадоксальная:
- **LTV/CAC хороший**,
- **CAC payback хороший**,
- но **фиксированная база команды для B2B/API слишком тяжёлая**.

Это означает, что кейс мог бы работать как:
1. lifestyle/self-serve продукт,
2. bootstrap studio-tool,
3. фича внутри существующего конструктора,

но **как отдельная fundable компания на этой стадии он не проходит**. Чтобы пройти gate, нужно радикально менять модель:
- либо уходить в pure self-serve с маленькой командой,
- либо поднимать ARPA сильно выше **100-120k ₽ MRR**, что уже превращает кейс в другой продукт.

## Sources
- **T1**: Recraft API pricing, официальный сайт, проверка 2026-05-13, https://www.recraft.ai/pricing?tab=api
- **T2**: HH.ru, вакансии SDR/BDR Москва, проверка 2026-05-13, https://hh.ru/search/vacancy?text=SDR
- **T3**: HH.ru, вакансии Senior Backend, проверка 2026-05-13, https://hh.ru/search/vacancy?text=senior%20backend
- **T4**: HH.ru, вакансии ML Engineer, проверка 2026-05-13, https://hh.ru/search/vacancy?text=ML%20Engineer
- **T5**: HH.ru, вакансии Account Executive / sales manager B2B, проверка 2026-05-13, https://hh.ru/search/vacancy?text=account%20executive
- **T6**: OptiMine / Optifi benchmark 2025, churn benchmarks for SaaS, проверка 2026-05-13, https://www.optifi.ai/post/saas-churn-rate-benchmarks
- **T7**: SaaS Capital, churn by ACV benchmark, проверка 2026-05-13, https://www.saas-capital.com/blog-posts/what-is-a-good-saas-churn-rate/
