# Program 5 — Unit Economics

## Итог этапа
- Решение: **FAIL**.
- Причина: при реалистичной team/FOT-модели, fully-loaded CAC и service-heavy delivery кейс **не выходит на EBITDA 500k+ ₽/мес даже на 50 активных клиентах**. LTV/CAC получается приемлемым, но fixed-cost base слишком тяжёлая для fund-level доходности.[T1][T2][T4][T5]
- Инвест-статус: **REJECTED**, перенос в `pipeline/rejected/`.

## 1) Operating model и ключевые допущения
- ICP: e-commerce бренды, performance-команды, маркетплейс-селлеры и агентства, которым нужен поток баннеров, ресайзов, локализаций и brand-safe asset production.[T1][T2]
- Модель монетизации: monthly retainer + SLA, не self-serve SaaS. Это важно, потому что delivery и account load остаются существенными даже при хорошей API-себестоимости.[T1][T2]
- Blended ARPU: **45 000 ₽/клиент/мес**. Это внутри intake-диапазона `45-90k ₽/мес`, но ближе к нижней половине, потому что рынок РФ давит на цену, а low-end альтернативы вроде Flyvi/SUPA задают anchor.[T1]
- Сегмент для CAC sanity: **mid-market B2B / agency-enabled service**. Значит, fully-loaded CAC должен быть выше «рекламного CAC» и попадать хотя бы в mid-market benchmark `60-250k ₽`, иначе модель занижена.[T4]
- Churn benchmark: для mid-market B2B ориентир **1.5-3.0% monthly churn**; для ранней стадии и слабого moat беру консервативно **2.8%/мес**.[T5]

## 2) Detailed business process table: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Захват лида из ads / outbound / партнёров | Performance marketer / SDR | Яндекс.Директ, VK Ads, Telegram, email, CRM | 10 мин | 1 400 | Средний |
| 2 | Первичный qualify: объём креативов, каналы, брендбук, SLA | SDR | amoCRM/Bitrix24, Telegram, почта | 20 мин | 700 | Средний |
| 3 | Discovery call | AE | Google Meet / Telegram / CRM | 45 мин | 2 200 | Низкий |
| 4 | Сбор brand-input: гайдлайны, референсы, SKU, tone | AE + Delivery lead | Notion, Google Drive, forms | 60 мин | 2 800 | Средний |
| 5 | Тестовый sample / concept pack | Designer-operator + AI pipeline | Recraft/API, Figma, prompt templates | 90 мин | 4 600 | Средний |
| 6 | Коммерческое предложение и пакет SLA | AE | CRM, template CP, e-sign | 45 мин | 2 100 | Средний |
| 7 | Legal / procurement / согласование оплаты | AE + founder | ЭДО, Диадок, CRM | 60 мин | 2 700 | Низкий |
| 8 | Onboarding клиента и постановка production workflow | Customer Success + Delivery lead | Notion, Telegram bot, task tracker | 120 мин | 4 900 | Средний |
| 9 | Ежемесячный production cycle: баннеры, ресайзы, локализация | Designer-operator + QA | Recraft/API, Figma, storage | 8.0 ч | 13 900 | Средний |
| 10 | Ревизии, сдача, invoice, контроль оплаты | CSM + бухгалтерия | CRM, 1С, банк, ЭДО | 60 мин | 2 100 | Средний |

### Вывод по процессу
- Самый дорогой блок не генерация, а **human-in-the-loop delivery и клиентский контекст**.
- Даже если API стоит дешево, бизнес остаётся похожим на productized agency, а не на software-margin SaaS.[T2][T3]

## 3) COGS breakdown per client/month
| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Designer/operator time | 8 400 | 4.0 ч на клиента × 2 100 ₽/ч fully-loaded | расчет от FOT |
| QA + delivery lead review | 3 000 | 1.2 ч × 2 500 ₽/ч | расчет от FOT |
| Customer success variable load | 2 200 | 0.8 ч × 2 750 ₽/ч | расчет от FOT |
| AI/API generation | 1 800 | mix raster/vector + iterations, запас к API-price | [T2] |
| Stock/fonts/storage/render | 1 200 | ассеты, хранилище, transfer, backup | [T2] + допущение |
| Overflow revisions / freelancers | 1 800 | ~0.6 ч внешнего буфера | допущение |
| Payment/acquiring | 900 | ~2% от ARPU | допущение |
| **Итого COGS** | **19 300** |  |  |

- Revenue per client/month: **45 000 ₽**.
- Gross profit per client/month: **25 700 ₽**.
- Gross margin: **57.1%**.

## 4) CAC by acquisition channel with funnel conversion
| Канал | Spend, ₽/мес | Top of funnel | MQL | SQL/meeting | Proposal | New paying customers | Conv lead→pay | Raw CAC, ₽ | Channel comment |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| Paid ads (Яндекс.Директ + VK) | 180 000 | 1 500 visits | 90 | 18 | 9 | 3 | 0.20% от visits / 3.3% от MQL | 60 000 | Работает на широком ICP, но лиды шумные |
| Outbound | 265 000 | 3 000 contacts | 150 replies | 30 meetings | 9 | 2 | 0.07% от contacts / 1.3% от replies | 132 500 | Дорогой канал, но даёт agency ICP |
| Partnerships / events | 220 000 | 40 partner leads | 24 | 12 | 6 | 2 | 5.0% от leads | 110 000 | Хорошее качество, маленький объём |
| **Blended** | **665 000** | — | — | — | — | **7** | — | **95 000** | Это только direct spend, без команды и overhead |

## 5) FULLY-LOADED CAC
Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools + Events + Overhead multiplier) / New paying customers`

### Разложение blended CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | рабочий бюджет на paid acquisition | модель GTM |
| Outbound team FOT (SDR/AE attributed to new) | 377 000 | SDR 160k gross + 30% = 208k; 0.5 AE allocation = 169k | [T4] |
| Marketing team FOT (partial allocation) | 117 000 | 0.5 performance marketer: 180k gross × 1.3 | [T4] + допущение |
| Tools (CRM, prospecting, телефония, email, аналитика) | 45 000 | amoCRM/Bitrix24 + sequencing + workspace | допущение |
| Events/partnerships | 120 000 | meetups, partner fee, co-marketing | допущение |
| Subtotal before overhead | 839 000 | сумма выше |  |
| Overhead multiplier (x1.3) | 251 700 | 30% от subtotal как офис/финансы/management overhead | standard for B2B service |
| **Total fully-loaded acquisition cost / month** | **1 090 700** |  |  |
| **New paying customers / month** | **7** | из blended funnel |  |
| **Fully-loaded blended CAC** | **155 814 ₽** | 1 090 700 / 7 |  |

### CAC по каналу vs blended CAC
| Метрика | Paid ads | Outbound | Partnerships | Blended |
|---|---:|---:|---:|---:|
| Raw CAC, ₽ | 60 000 | 132 500 | 110 000 | 95 000 |
| Fully-loaded CAC, ₽ | 126 000 | 238 000 | 187 000 | **155 814** |
| Sanity vs RU benchmark | ок | верх mid-market | ок | ок |

### Sanity checks по CAC
- Fully-loaded blended CAC **155.8k ₽** попадает в диапазон mid-market SaaS/B2B service для РФ `60-250k ₽`, значит модель не выглядит искусственно заниженной.[T4]
- CAC заметно выше raw CAC, что нормально для сервиса с длинной pre-sale фазой и human touch.
- Если бы считать только ads-spend, экономика выглядела бы слишком красивой и была бы misleading.

## 6) LTV with churn rate
- Monthly contribution per client = **25 700 ₽**.
- Benchmark churn для mid-market B2B: **1.5-3.0%/мес**.[T5]
- Для раннего сервиса без сильного product lock-in беру **2.8% monthly churn**.

Формула:
`LTV = monthly contribution / monthly churn`

`LTV = 25 700 / 0.028 = 917 857 ₽`

| Показатель | Значение |
|---|---:|
| Monthly churn | 2.8% |
| Avg customer lifetime | 35.7 мес |
| Monthly contribution | 25 700 ₽ |
| **LTV** | **917 857 ₽** |

## 7) LTV/CAC ratio
`917 857 / 155 814 = 5.89x`

- **LTV/CAC = 5.9x**.
- Формально это выше порога `3:1`, то есть retention и монетизация сами по себе не убивают кейс.
- Но для фонда важно не только отношение LTV/CAC, а способность быстро конвертировать gross profit в EBITDA при реалистичном fixed-cost base.

## 8) CAC Payback in months
Формула по заданию:
`CAC Payback = CAC / MRR per customer`

`155 814 / 45 000 = 3.46 месяца`

- **CAC Payback = 3.5 месяца**.
- Это лучше базового порога `<12 мес`, значит проблема кейса не в payback, а в delivery leverage и fixed costs.

## 9) Contribution Margin %
Формула:
`Contribution Margin % = (Revenue - variable costs) / Revenue`

`(45 000 - 19 300) / 45 000 = 57.1%`

- **Contribution Margin = 57.1%**.
- Для service-first AI business это прилично, но **недостаточно для venture-scale**, если почти весь gross profit съедается людьми и клиентским контекстом.

## 10) Team & FOT

### Full team table
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| CEO/founder | продажи top accounts, партнёры, финансы | 650 000 | 195 000 | 845 000 | market-equivalent founder salary |
| CTO / Tech Lead | automation stack, QA systems, integrations | 500 000 | 150 000 | 650 000 | [T4] |
| Senior Backend | генерация пайплайнов, CRM/workflow интеграции | 400 000 | 120 000 | 520 000 | [T4] |
| Frontend / internal tools | клиентский кабинет, формы, production UI | 280 000 | 84 000 | 364 000 | [T4] |
| DevOps | infra, storage, secrets, CI/CD | 320 000 | 96 000 | 416 000 | [T4] |
| ML / prompt systems engineer | prompt optimization, routing, QC | 450 000 | 135 000 | 585 000 | [T4] |
| Delivery lead / creative ops | production standards, QA, throughput | 250 000 | 75 000 | 325 000 | market proxy |
| SDR | outbound pipeline | 160 000 | 48 000 | 208 000 | [T4] |
| AE | discovery, proposals, close | 330 000 | 99 000 | 429 000 | [T4] |
| Customer Success | onboarding, retention, revisions control | 230 000 | 69 000 | 299 000 | [T4] |
| **Итого mature monthly FOT** |  |  |  | **4 641 000** |  |

### Таблица найма по realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 1 | 400 000 | 2 | 1.5 | 120 000 | 520 000 |
| ML Engineer | 1 | 450 000 | 3 | 2 | 135 000 | 585 000 |
| DevOps | 1 | 320 000 | 1.5 | 1 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 160 000 | 1 | 1 | 48 000 | 208 000 |
| AE | 1 | 330 000 | 1.5 | 2.5 | 99 000 | 429 000 |
| Customer Success | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |
| Delivery lead / creative ops | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Salary benchmark notes
- Senior backend: вакансии hh.ru показывают диапазон около `300-450k+ ₽` gross/net-equivalent.[T4]
- Tech lead: hh.ru tech lead / backend lead объявления дают ориентир порядка `350-400k+ ₽`, для стартапа беру `500k gross` с premium за ownership.[T4]
- DevOps: hh.ru senior DevOps даёт `300-450k ₽` net-equivalent.[T4]
- ML engineer: hh.ru machine learning engineer listings доходят до `512-768k ₽ gross`, поэтому `450k gross` консервативно.[T4]
- SDR/AE/CS: hh.ru даёт коридоры около `100-200k` для SDR, `250-500k` для AE/KAE и `170-250k` для CS.[T4]

## 11) Cumulative FOT timeline M1-M12
Допущение: найм идёт реалистично, без нарушения time-to-hire. Полная продуктивность включается после ramp.

| Месяц | Кто в команде | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | старт, founder-led sales |
| M2 | CEO + Delivery lead | 1 170 000 | начинаем руками собирать delivery |
| M3 | + CTO/Tech Lead | 1 820 000 | строим automation backbone |
| M4 | + Senior Backend + SDR | 2 548 000 | появляется outbound |
| M5 | + AE | 2 977 000 | усиливаем pipeline и close |
| M6 | + Customer Success + Frontend | 3 640 000 | onboarding и client ops растут |
| M7 | + DevOps | 4 056 000 | стабилизация production stack |
| M8 | + ML Engineer | 4 641 000 | internal AI tooling |
| M9 | те же | 4 641 000 | full run-rate |
| M10 | те же | 4 641 000 | full run-rate |
| M11 | те же | 4 641 000 | full run-rate |
| M12 | те же | 4 641 000 | full run-rate |

### Проверка realism
- В M1 нет «5+ человек сразу», значит time-to-hire не нарушен.
- Но уже к M6-M8 возникает слишком тяжёлая FOT-база для бизнеса с ARPU `45k ₽`.

## 12) Fixed costs breakdown
| Компонент fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT at steady state | 4 641 000 | см. таблицу выше |
| Core software/tools not in COGS | 140 000 | CRM, PM, analytics, design ops |
| Cloud/platform/security | 120 000 | storage, backups, monitoring |
| Finance/legal/admin | 180 000 | бухгалтерия, юрподдержка, ЭДО |
| Office / coworking / misc | 120 000 | гибридный режим |
| **Total fixed costs / month** | **5 201 000** |  |

## 13) Break-even by client count and by month
### Break-even by client count
- Contribution per client/month = **25 700 ₽**.
- Fixed costs/month = **5 201 000 ₽**.

`Break-even clients = 5 201 000 / 25 700 = 202.4`

- **Break-even = 203 активных клиента**.
- На 50 клиентах:
  - Revenue = `2 250 000 ₽/мес`
  - Contribution = `1 285 000 ₽/мес`
  - EBITDA ≈ `-3 916 000 ₽/мес`
- Значит Profit Gate **провален жёстко**: даже на `50` клиентах компания не подходит близко к `500k ₽ EBITDA/мес`.

### Break-even by month
Допущение по набору клиентов: 2, 4, 7, 10, 14, 18, 23, 28, 33, 38, 44, 50 клиентов к концу M12.

| Месяц | Активные клиенты | Revenue, ₽ | Contribution, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 2 | 90 000 | 51 400 | 1 405 000 | -1 353 600 |
| M2 | 4 | 180 000 | 102 800 | 1 730 000 | -1 627 200 |
| M3 | 7 | 315 000 | 179 900 | 2 380 000 | -2 200 100 |
| M4 | 10 | 450 000 | 257 000 | 3 108 000 | -2 851 000 |
| M5 | 14 | 630 000 | 359 800 | 3 537 000 | -3 177 200 |
| M6 | 18 | 810 000 | 462 600 | 4 200 000 | -3 737 400 |
| M7 | 23 | 1 035 000 | 591 100 | 4 616 000 | -4 024 900 |
| M8 | 28 | 1 260 000 | 719 600 | 5 201 000 | -4 481 400 |
| M9 | 33 | 1 485 000 | 848 100 | 5 201 000 | -4 352 900 |
| M10 | 38 | 1 710 000 | 976 600 | 5 201 000 | -4 224 400 |
| M11 | 44 | 1 980 000 | 1 130 800 | 5 201 000 | -4 070 200 |
| M12 | 50 | 2 250 000 | 1 285 000 | 5 201 000 | -3 916 000 |

- В горизонте 12 месяцев **break-even не достигается**.
- Даже если заморозить часть продуктового найма, разрыв слишком большой, чтобы считать это «fund-level investable» без радикальной смены модели.

## 14) Burn-to-breakeven и Cash runway
### Burn-to-breakeven
- При траектории выше cumulative EBITDA burn за M1-M12 ≈ **39.0 млн ₽**.
- Даже если вырезать часть discretionary spend, до operating break-even потребуется **30M+ ₽** капитала.
- Для B2B enterprise-style service это не фантастика, но при ARPU `45k ₽` и отсутствии software leverage такой burn плохо сочетается с венчурной доходностью.

### Cash runway
Допущение по startup_capital: **18 млн ₽**.

- Average monthly burn M1-M12 ≈ `3.25 млн ₽`.
- Точный расчёт: `18 000 000 / 3 253 350 ≈ 5.5 месяца`.
- **Cash runway ≈ 5.5 месяца**.
- Чтобы комфортно дожить до точки, где gross profit перекрывает fixed costs, нужен капитал существенно выше `18 млн ₽`, ближе к `35-40 млн ₽`.

## 15) Почему кейс не проходит fund-level filter
1. **Это service-heavy business**, а не software-margin engine. Дешёвый API не компенсирует высокую долю людей в delivery.[T2][T3]
2. **ARPU слишком низок** для команды, которая должна одновременно держать sales, delivery, QA, client success и automation.
3. **Break-even требует ~203 клиентов**, что плохо сочетается с обещанием quality/SLA и с enterprise-style GTM.
4. Формально **LTV/CAC и CAC payback хорошие**, но это ловушка: метрики acquisition выглядят красиво, потому что gross profit на клиента положительный. Однако fixed-cost machine съедает всю экономику.

## 16) Final verdict
- **Profit Gate: FAIL**.
- Основание: `company EBITDA < 500K/mo achievable even at 50 clients`.
- Дополнительный вывод: даже при LTV/CAC `5.9x` кейс остаётся **неинвестируемым на уровне фонда**, потому что unit economics не масштабируются в EBITDA без тяжёлого роста headcount.

## Источники
- [T1] Intake и demand-артефакты кейса: `00-brief.md`, `01-intake.md`, `02-demand.md`, `07-score-trajectory.md`
- [T2] Recraft enterprise + API pricing: https://www.recraft.ai/enterprise ; https://www.recraft.ai/docs/api-reference/pricing
- [T3] TechCrunch о Recraft growth / category validation: https://techcrunch.com/2025/05/05/a-stealth-ai-model-beat-dall-e-and-midjourney-on-a-popular-benchmark-its-creator-just-landed-30m/
- [T4] HH.ru compensation benchmarks, проверено 2026-05-13: https://hh.ru/vacancy/128441808 ; https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancy/129581822 ; https://hh.ru/vacancy/128565026 ; https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancy/128771369 ; https://hh.ru/vacancies/machine-learning-engineer ; https://hh.ru/vacancy/128841806 ; https://hh.ru/vacancy/128318995
- [T5] Optifai churn benchmark, проверено 2026-05-13: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ ; https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
