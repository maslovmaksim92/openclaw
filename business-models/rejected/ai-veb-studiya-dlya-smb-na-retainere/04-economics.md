# Unit Economics

## Executive summary
- Кейс: **AI-веб-студия для SMB на retainere**.
- Модель для расчёта: verticalized managed website retainer для SMB, ARPA **20 000 ₽/клиент/мес**.
- Переменная себестоимость: **8 400 ₽/клиент/мес**.
- Contribution / gross profit на клиента: **11 600 ₽/мес**.
- Blended fully-loaded CAC: **161 100 ₽**.
- Monthly churn benchmark для SMB subscription/service: **4%/мес**.
- LTV: **290 000 ₽**.
- LTV/CAC: **1,8x**.
- CAC Payback: **13,9 мес**.
- Contribution Margin: **58%**.
- Break-even: **382 клиента** или около **77 месяцев** при темпе net +5 новых платящих клиентов/мес.
- EBITDA при 50 клиентах: **-3,85 млн ₽/мес**.
- Вывод: **Profit Gate FAIL**, модель не инвестиционного качества на fund level.

## 1. Модель и ключевые допущения

### ICP и pricing
- ICP: SMB в РФ, которым нужен сайт + постоянные правки + базовое SEO + контент + мелкая автоматизация.
- Пакет: managed retainer.
- Средний чек: **20 000 ₽/мес**.
- Сегмент: **mid-market SMB service** с sales-assisted продажей, поэтому для sanity принят CAC multiplier **x1.5**.

### Почему взят churn = 4%/мес
- Для SMB subscription-бизнесов ChartMogul показывает monthly churn около **3,5–4,5%** у малых чеков, что даёт коридор для SMB-retainer модели. Использую **4%/мес** как базовый benchmark, потому что здесь нет сильного технологического lock-in, а замена агентства/подрядчика для SMB относительно проста.
- Источник benchmark: https://chartmogul.com/saas-metrics/reduced-churn-benchmarks/ 

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Захват лида из рекламы/сайта/Telegram | Marketing + SDR | Tilda/форма, Telegram, CRM | 10 мин | 350 | Высокая |
| 2 | Первичная квалификация | SDR | CRM, скрипт, телефония | 20 мин | 450 | Средняя |
| 3 | Discovery call | AE / founder-led sales | Meet, CRM, ICP checklist | 45 мин | 1 700 | Низкая |
| 4 | Сбор брифа и материалов | AE + PM | Notion, CRM, Google Drive | 40 мин | 1 200 | Средняя |
| 5 | Коммерческое предложение и пакет | AE | шаблон КП, e-sign | 60 мин | 2 000 | Средняя |
| 6 | Технический scoping | CTO/Tech Lead | checklist, estimator | 45 мин | 3 300 | Низкая |
| 7 | AI-генерация структуры/текстов/референсов | Designer/Content Ops | GPT/Claude, Midjourney, Framer/Tilda | 90 мин | 1 800 | Высокая |
| 8 | Сборка сайта / no-code / интеграции | Frontend/No-code | Tilda/Framer, forms, analytics | 180 мин | 4 400 | Средняя |
| 9 | QA, правки, SEO-base | Designer + PM | чеклисты, analytics, page-speed | 90 мин | 2 200 | Средняя |
| 10 | Запуск, домен, аналитика, CRM forms | Frontend + PM | домен, метрика, CRM | 60 мин | 1 500 | Средняя |
| 11 | Онбординг на retainer и SLA | CSM/PM | CRM, Telegram, billing | 45 мин | 950 | Средняя |
| 12 | Выставление счёта и оплата | Finance/Admin | банк, ЭДО, CRM | 20 мин | 300 | Высокая |

### Итог по процессу
- One-off implementation / onboarding cost на нового клиента: **~20 150 ₽** до первой оплаты.
- Это не входит в monthly COGS напрямую, но объясняет, почему payback длиннее, чем у self-serve SaaS.
- Узкое место процесса: discovery + scoping + ручной QA, а не генерация контента.

## 3. COGS breakdown на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| AI/LLM и генерация | 1 200 | GPT/Claude + occasional image generation, усреднённое потребление |
| Хостинг/CDN/формы/аналитика | 800 | Tilda/Framer/hosting stack + plug-ins |
| Аккаунт-менеджмент и support labor | 2 800 | ~1,5 ч PM/CSM на клиента в месяц |
| Контент/дизайн QA labor | 1 800 | ~1,0 ч content/design support |
| Dev/no-code maintenance labor | 1 500 | ~0,7 ч мелких правок / интеграций |
| Платежи и прочие переменные | 300 | эквайринг, сервисные хвосты |
| **Итого COGS** | **8 400** |  |

### На клиента
- MRR на клиента: **20 000 ₽**.
- Gross profit / contribution на клиента: **11 600 ₽**.
- Contribution Margin: **58%**.

## 4. CAC по каналам с funnel conversion

### Funnel assumptions

| Канал | Top of funnel | SQL / discovery | Proposal | New paying | Конверсия TOFU→Paying |
|---|---:|---:|---:|---:|---:|
| Paid search / performance | 60 лидов | 15 | 6 | 2 | 3,3% |
| Outbound | 2 000 аккаунтов | 20 discovery | 8 | 2 | 0,1% |
| Partnerships / agencies | 12 интро | 8 | 5 | 1 | 8,3% |
| **Итого / blended** | **2 072** | **43** | **19** | **5** | **0,24%** |

### CAC по каналу

| Канал | Расход, ₽/мес | Что входит | New paying | CAC, ₽ |
|---|---:|---|---:|---:|
| Paid search / performance | 144 000 | 120k ads + 24k ops allocation | 2 | 72 000 |
| Outbound | 390 000 | SDR FOT + AE allocation + tools | 2 | 195 000 |
| Partnerships / agencies | 156 000 | partner spend + AE allocation | 1 | 156 000 |
| **Blended** | **805 500** | fully-loaded acquisition | **5** | **161 100** |

## 5. FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Разложение blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый бюджет на performance acquisition | допущение фонда, sanity against SMB leadgen budgets |
| Outbound team FOT (SDR/AE attributed to new) | 195 000 | SDR 150k gross ×1.3 = 195k | HH.ru salary benchmark + 30% страхвзносы |
| Marketing team FOT (partial allocation) | 117 000 | 90k gross ×1.3, 100% на acquisition | HH.ru benchmark + allocation |
| Tools (CRM, телефония, prospecting, analytics) | 45 000 | CRM + телефония + prospecting stack | amoCRM pricing + market stack estimate |
| Events/partnerships | 60 000 | усреднение небольших партнёрских активаций | допущение фонда |
| Subtotal raw CAC pool | 537 000 | сумма выше | расчёт |
| Overhead multiplier (x1.5 для sales-assisted SMB) | 268 500 | 537 000 × 0.5 | правило из методики для mid-market B2B |
| **Итого fully-loaded CAC pool** | **805 500** | 537 000 × 1.5 | расчёт |
| **New paying customers / мес** | **5** | blended across 3 channels | funnel model |
| **Blended fully-loaded CAC** | **161 100 ₽** | 805 500 / 5 | расчёт |

### Sanity check against benchmarks
- Для mid-market SMB / sales-assisted digital service полученный CAC **161k ₽** попадает в коридор **60–250k ₽** и выглядит реалистично.
- Если считать только ads spend, CAC был бы искусственно занижен, поэтому использован **fully-loaded** подход.

## 6. LTV, churn, LTV/CAC и payback

| Метрика | Формула | Значение |
|---|---|---:|
| Churn rate | benchmark | 4%/мес |
| Customer lifetime | 1 / churn | 25 мес |
| Gross profit на клиента | ARPA - COGS | 11 600 ₽/мес |
| LTV | 11 600 / 0.04 | 290 000 ₽ |
| Blended CAC | fully-loaded | 161 100 ₽ |
| **LTV/CAC** | 290 000 / 161 100 | **1,8x** |
| **CAC Payback** | 161 100 / 11 600 | **13,9 мес** |

### Интерпретация
- **LTV/CAC 1,8x** ниже инвестиционного порога **3,0x**.
- **Payback 13,9 мес** находится выше комфортного уровня для non-enterprise модели.
- Даже при нормальном churn бизнес упирается в дорогой sales-assisted acquisition и ручной delivery.

## 7. Team & FOT

### Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend / integrations | 1 | 420 000 | 2 | 1.5 | 126 000 | 546 000 |
| Frontend / No-code builder | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Designer / Content Ops | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| SDR | 1 | 150 000 | 1 | 1 | 45 000 | 195 000 |
| AE | 1 | 280 000 | 2 | 3 | 84 000 | 364 000 |
| Customer Success / PM | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |
| Finance/Admin | 0.5 | 45 000 | 1 | 1 | 13 500 | 58 500 |
| **Итого** | **8.5** |  |  |  |  | **3 698 500 ₽/мес** |

### Salary benchmark note
- Диапазоны согласованы с медианами HH.ru по Москве/СПб и с sanity-band из задания: Senior/Lead SWE 350–550k, Tech Lead 450–700k, SDR 100–180k + bonus, AE 300–500k OTE.

## 8. Cumulative FOT timeline M1-M12

> Важно: модель найма не нарушает realism, нет 5+ hires в первый месяц. Зарплата платится после выхода, ramp влияет на продуктивность, но не на cash cost.

| Месяц | Кто уже в штате | FOT/month, ₽ |
|---|---|---:|
| M1 | CEO, Finance/Admin 0.5 | 903 500 |
| M2 | + CTO, SDR | 1 813 500 |
| M3 | + Senior Backend | 2 359 500 |
| M4 | + Frontend/No-code, AE | 3 113 500 |
| M5 | + Designer/Content Ops | 3 399 500 |
| M6 | + Customer Success/PM | 3 698 500 |
| M7 | full team | 3 698 500 |
| M8 | full team | 3 698 500 |
| M9 | full team | 3 698 500 |
| M10 | full team | 3 698 500 |
| M11 | full team | 3 698 500 |
| M12 | full team | 3 698 500 |

## 9. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 3 698 500 |
| Офис / coworking / admin buffer | 350 000 |
| Software stack / internal tools | 120 000 |
| Finance / legal / ЭДО / бухгалтерия | 70 000 |
| Cloud / staging / observability | 80 000 |
| Founder travel / meetings / misc | 60 000 |
| Recruiting / hiring overhead | 50 000 |
| **Итого fixed costs / мес** | **4 428 500 ₽** |

## 10. Break-even: по клиентам и по месяцам

### По клиентам
- Contribution на клиента: **11 600 ₽/мес**.
- Fixed costs: **4 428 500 ₽/мес**.
- Break-even clients = 4 428 500 / 11 600 = **382 клиента**.

### По месяцам
Базовый сценарий роста: 2, 4, 6, 10, 14, 18, 24, 30, 36, 42, 48, 55 клиентов к концу M1-M12.

| Месяц | Клиентов | Валовая прибыль, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 2 | 23 200 | 1 633 500 | -1 610 300 |
| M2 | 4 | 46 400 | 2 543 500 | -2 497 100 |
| M3 | 6 | 69 600 | 3 089 500 | -3 019 900 |
| M4 | 10 | 116 000 | 3 843 500 | -3 727 500 |
| M5 | 14 | 162 400 | 4 129 500 | -3 967 100 |
| M6 | 18 | 208 800 | 4 428 500 | -4 219 700 |
| M7 | 24 | 278 400 | 4 428 500 | -4 150 100 |
| M8 | 30 | 348 000 | 4 428 500 | -4 080 500 |
| M9 | 36 | 417 600 | 4 428 500 | -4 010 900 |
| M10 | 42 | 487 200 | 4 428 500 | -3 941 300 |
| M11 | 48 | 556 800 | 4 428 500 | -3 871 700 |
| M12 | 55 | 638 000 | 4 428 500 | -3 790 500 |

### Проверка порога 50 клиентов
- Валовая прибыль при 50 клиентах: **580 000 ₽/мес**.
- EBITDA при 50 клиентах: **580 000 - 4 428 500 = -3 848 500 ₽/мес**.
- Следовательно, кейс **не может показать 500k EBITDA/mo даже близко на 50 клиентах**.

## 11. Burn-to-breakeven и runway

### Burn-to-breakeven
- Пик ежемесячного burn в модели: около **4,22 млн ₽/мес** в M6.
- После выхода на full team burn остаётся **~3,8–4,1 млн ₽/мес**, если рост клиентов не ускоряется кратно.
- До break-even нужно либо **382 клиента**, либо радикально уменьшить команду и sales motion.

### Cash runway
- Допущение: `startup_capital = 60 млн ₽`.
- Runway при steady-state burn **~4,1 млн ₽/мес**: около **14,5 месяца**.
- Но так как break-even в текущей модели далеко за пределами 12-18 месяцев, даже 60 млн ₽ не решают базовую проблему экономики.
- Для B2B service-heavy модели это означает: капитал нужен большой, а predictability низкая.

## 12. Почему модель ломается
- AI удешевляет production, но **не убирает discovery, scoping, sales, QA и account work**.
- SMB-сегмент чувствителен к цене, поэтому ARPA недостаточно высок, чтобы покрыть sales-assisted acquisition.
- Fully-loaded CAC близок к **161k ₽**, а gross-profit lifetime only **290k ₽**. Это слишком тонкий запас для фонда.
- Для инвестиционного качества здесь нужен либо self-serve motion, либо гораздо более высокий ACV, либо white-label delivery без собственного тяжёлого sales floor.

## 13. Final economics verdict
- **Profit Gate: FAIL**.
- Основание 1: **LTV/CAC = 1,8x < 3,0x**.
- Основание 2: при **50 клиентах EBITDA = -3,85 млн ₽/мес**, то есть порог 500k EBITDA/mo недостижим.
- Основание 3: break-even требует **382 клиента**, что несовместимо с текущей team/FOT моделью.

## Sources
- ChartMogul churn benchmarks: https://chartmogul.com/saas-metrics/reduced-churn-benchmarks/
- HH.ru vacancies: content manager / site roles: https://hh.ru/vacancies/kontent-menedzher-sajta/polnaya_zanyatost
- HH.ru vacancies: SDR / sales development: https://hh.ru/search/vacancy?text=SDR
- HH.ru vacancies: account executive / b2b sales: https://hh.ru/search/vacancy?text=account%20executive
- amoCRM pricing: https://www.amocrm.ru/tariffs/
- Demand stage sources already validated in 02-demand.md: Nethouse, REG.RU, BotHelp, Siteling, Siteberry, ФНС реестр МСП.
