# 04-economics

## Unit Economics Summary
- **Кейс**: Norm AI, enterprise Legal/Compliance AI для банков, страховщиков и профучастников.
- **Модель**: только enterprise / regulated B2B, private-cloud или on-prem pilot-to-production.
- **Базовая цена**: **300 000 ₽ MRR** на клиента, то есть **3.6 млн ₽ ARR**.
- **COGS / клиент / месяц**: **110 000 ₽**.
- **Gross Margin / Contribution Margin**: **63.3%**.
- **Blended fully-loaded CAC**: **3.34 млн ₽**.
- **Monthly churn**: **1.5%**.
- **LTV (gross profit basis)**: **12.67 млн ₽**.
- **LTV/CAC**: **3.79x**.
- **CAC Payback**: **11.1 месяца**.
- **Break-even**: **35 клиентов** или около **M18-M20** при реалистичном темпе продаж.
- **Вывод**: economics **проходит** инвестиционный порог по unit economics, но только в узком enterprise-only сценарии. SMB/self-serve сценарий ломается.

## Ключевые допущения
1. Продаём не generic AI, а сокращение ручного compliance review, DDQ/RFP workload, contract review и disclosure approval.
2. Средний клиент в РФ, который стоит усилий, это крупный regulated buyer, а не SMB.
3. Цена **300 тыс. ₽/мес** консервативна относительно экономии 1.0-1.5 compliance FTE и международных enterprise benchmark floors.
4. Цикл сделки длинный, поэтому CAC считается как **fully-loaded**, а не как media-spend-only.
5. Churn взят консервативно выше типичного enterprise SaaS benchmark из-за локализации и длинного pilot-to-prod цикла в РФ.

## Источники и benchmark-база
- **Нормативно-нагруженный buyer universe РФ**: Банк России по банкам, страховщикам и профучастникам рынка ценных бумаг: https://cbr.ru/banking_sector/ ; https://www.cbr.ru/insurance/ ; https://www.cbr.ru/securities_market/
- **Найм и зарплатные вилки**: hh.ru поиск и вакансии по compliance / sales / engineering, плюс job-postings по Москве и СПб: https://hh.ru/ ; https://hh.ru/vacancies/compliance_officer ; https://hh.ru/search/vacancy?text=Senior+Backend ; https://hh.ru/search/vacancy?text=ML+Engineer ; https://hh.ru/search/vacancy?text=DevOps ; https://hh.ru/search/vacancy?text=SDR ; https://hh.ru/search/vacancy?text=Account+Executive
- **CRM / tools pricing**: Битрикс24 и amoCRM: https://www.bitrix24.ru/prices/ ; https://www.amocrm.ru/tariffs/
- **Cloud / infra pricing proxy**: Yandex Cloud pricing: https://yandex.cloud/ru/pricing
- **Enterprise churn benchmark**: SaaS Capital, 2025 SaaS benchmarks, у larger-ACV B2B churn materially ниже SMB: https://www.saas-capital.com/blog-posts/2025-saas-performance-metrics-benchmarks/ ; дополнительный sanity source по B2B SaaS churn bands: https://www.paddle.com/resources/reduce-b2b-saas-churn
- **Категорийные price floors**: VComply, ComplyCloud, Sengol, см. demand-stage sources в 02-demand.md.

## Business process table: от лида до платежа

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам/страховщикам | SDR | hh/СПАРК/ручной desk research/CRM | 2 ч | 2 700 | частично автоматизировано |
| 2 | Холодный outreach и первичная квалификация | SDR | email, Telegram, CRM, sequences | 3 ч | 4 100 | частично автоматизировано |
| 3 | Intro call и pain discovery | AE | видеозвонок, CRM | 1.5 ч | 4 100 | вручную |
| 4 | Compliance use-case scoping | AE + CEO | Zoom/Meet, Notion, CRM | 2 ч | 8 000 | вручную |
| 5 | Технический пресейл и security/QA ответы | CTO + ML Engineer | docs, security questionnaire | 5 ч | 18 800 | вручную |
| 6 | Пилотное ТЗ и proposal | AE + CTO + CEO | proposal doc, pricing sheet | 4 ч | 16 100 | частично автоматизировано |
| 7 | Пилот / sandbox / private-cloud setup | Backend + ML + DevOps | Yandex Cloud / private infra | 24 ч | 58 900 | частично автоматизировано |
| 8 | Юридическое согласование и procurement | CEO + AE | договор, redlines, email | 6 ч | 19 700 | вручную |
| 9 | Онбординг, policy ingestion, настройка workflow | CSM + ML + Backend | KB, workflow builder, support desk | 16 ч | 40 200 | частично автоматизировано |
| 10 | Выставление счёта и получение оплаты | Finance/CEO | банк-клиент, ЭДО, CRM | 1 ч | 2 000 | частично автоматизировано |

**Итого variable + semi-variable deal execution cost на 1 нового клиента**: около **174 600 ₽** прямых часов команды плюс **~320-380 тыс. ₽** облака, инфобез-оверлей, пилотная поддержка и неуспешные касания. Но для инвестиционной модели этого недостаточно, поэтому основной CAC считается fully-loaded ниже.

## COGS breakdown на 1 клиента / месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| Inference / compute / private cloud | 28 000 | Yandex Cloud pricing proxy + enterprise reserve | inference и orchestration |
| Storage, logs, backup, security telemetry | 6 000 | cloud + SIEM/logging share | regulated workload |
| Customer Success / support allocation | 24 000 | 312 000 ₽ fully-loaded CSM / 13 клиентов | post-sale support |
| ML tuning / prompt-policy maintenance | 18 000 | 650 000 ₽ ML FOT × 0.33 FTE / 12 клиентов | domain adaptation |
| Backend / integration support allocation | 14 000 | 1 092 000 ₽ two backend FL / shared pool | APIs и fixes |
| Security/compliance review overhead | 8 000 | infosec/legal allocation | vendor reviews |
| Onboarding amortization | 12 000 | пилот/настройка размазаны на 12 мес | setup burden |
| Account infrastructure reserve | 0? | included above | чтобы не double count, отдельный reserve не добавляю |
| **Итого COGS** | **110 000** |  |  |

**Gross profit / клиент / месяц** = **300 000 - 110 000 = 190 000 ₽**.

## CAC by acquisition channel с funnel conversion

### Воронка 1: outbound ABM
| Метрика | Значение |
|---|---:|
| Target accounts / мес | 120 |
| Ответили / positive reply | 18 (15%) |
| Discovery calls | 6 (33% от replies) |
| Пилоты / sandbox | 2 (33% от discovery) |
| Win-rate из пилотов | 12% от пилотов? |
| Новые paying customers / мес | **0.24** |
| Channel spend / мес | **700 000 ₽** |
| CAC channel | **2.92 млн ₽** |

Расчёт spend: SDR fully-loaded 250k + AE attributed 280k + tools 70k + trips/events 100k = 700k. CAC = 700k / 0.24.

### Воронка 2: partnerships / SI / legal advisors
| Метрика | Значение |
|---|---:|
| Партнёрских интро / мес | 15 |
| Meetings | 6 (40%) |
| SQL | 3 (50%) |
| Пилоты | 1.2 (40%) |
| Новые paying customers / мес | **0.12** |
| Channel spend / мес | **297 000 ₽** |
| CAC channel | **2.48 млн ₽** |

Расчёт spend: partner manager / founder allocation 150k + co-marketing/legal events 90k + travel 57k.

### Воронка 3: content / inbound thought leadership
| Метрика | Значение |
|---|---:|
| MQL / мес | 20 |
| Meetings | 5 (25%) |
| SQL | 2 (40%) |
| Пилоты | 0.5 (25%) |
| Новые paying customers / мес | **0.04** |
| Channel spend / мес | **130 000 ₽** |
| CAC channel | **3.25 млн ₽** |

Расчёт spend: paid traffic 120k + content ops 10k. Канал полезен для trust-building, но для closed-won слабый.

## Fully-loaded CAC (обязательно)

### Таблица компонентов
| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 120 000 | минимальный ABM + retargeting budget | Yandex/VK benchmark, internal assumption |
| Outbound team FOT (SDR/AE attributed to new) | 530 000 | SDR 250k fully-loaded + AE 468k × 60% attributed | hh.ru benchmark + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 120 000 | founder/marketing ops allocation на acquisition | internal allocation |
| Tools (CRM, enrichment, телефония, e-sign) | 78 000 | Bitrix24/amoCRM + телефония + data tools | Bitrix24, amoCRM |
| Events/partnerships | 180 000 | отраслевые мероприятия, бизнес-завтраки, travel | internal assumption |
| Overhead multiplier (x1.3) | 308 400 | (120k+530k+120k+78k+180k) × 0.3 | стандарт для enterprise B2B |
| **Итого fully-loaded acquisition spend / мес** | **1 336 400** |  |  |
| **New paying customers / мес** | **0.40** | 0.24 outbound + 0.12 partnerships + 0.04 inbound | funnel model |
| **Blended fully-loaded CAC** | **3 341 000 ₽** | 1 336 400 / 0.40 | calculation |

### Sanity по сегменту
- Это **regulated enterprise** motion, поэтому SMB CAC здесь неприменим.
- Полученный blended CAC **3.34 млн ₽** выше типичного RU enterprise SaaS benchmark 300-900k ₽/клиент, но это оправдано тем, что у кейса длинный pilot, security review, procurement и локализация policy engine.
- CAC не выглядит заниженным: он **не ниже** industry floor и включает FOT, tools, events и overhead.

## LTV и churn rate

### Benchmark churn source
- SaaS Capital показывает, что у B2B SaaS с большим ACV churn materially ниже SMB, часто около **8-12% annual gross revenue churn** для более зрелого enterprise сегмента.
- Для локального expansion-кейса беру **консервативный monthly logo churn = 1.5%**, то есть около **16.6% annualized**, хуже benchmark, потому что в РФ будут потери на пилотах, долгом внедрении и политике закупок.

### Расчёт LTV
- **Average lifetime** = 1 / 0.015 = **66.7 месяца**.
- **Gross profit / мес / клиент** = **190 000 ₽**.
- **LTV (gross profit basis)** = 190 000 × 66.7 = **12 673 000 ₽**.

## LTV/CAC ratio
- **LTV/CAC = 12.673 млн / 3.341 млн = 3.79x**.
- Это **выше порога 3:1**, значит кейс можно считать investable по unit economics, но только при сохранении цены 300k MRR и churn не хуже 1.5% monthly.

## CAC Payback
- Формула по требованию: **CAC Payback = CAC / MRR per customer**.
- **3.341 млн / 300 тыс. = 11.1 месяца**.
- Для enterprise/regulatory motion это допустимо, так как укладывается в порог **<18 месяцев**.

## Contribution Margin %
- Contribution Margin = (MRR - COGS) / MRR.
- **(300 000 - 110 000) / 300 000 = 63.3%**.
- Для AI-heavy enterprise SaaS это приемлемо, но запас по марже не огромный, потому что есть cloud + human-in-the-loop.

## Team & FOT

### Полная таблица команды
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи, enterprise deals, fundraising | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, пресейл | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | API, integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | workflow engine, infra code | 420 000 | 126 000 | 546 000 |
| ML Engineer | policy modeling, evals, RAG | 500 000 | 150 000 | 650 000 |
| DevOps | private cloud, CI/CD, observability | 350 000 | 105 000 | 455 000 |
| Frontend | admin/workbench UI | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting | 192 000 | 57 600 | 249 600 |
| AE | discovery, pilots, close | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, retention | 240 000 | 72 000 | 312 000 |
| **Итого** |  |  |  | **5 176 600 ₽/мес** |

### Таблица найма (обязательно)
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1.5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 192 000 | 0.5-1 | 1 | 57 600 | 249 600 |
| AE (Account Exec) | 1 | 360 000 | 1-2 | 3 | 108 000 | 468 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### Cumulative FOT timeline M1-M12

| Месяц | Кто уже в штате | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | discovery, customer interviews |
| M2 | CEO + Backend #1 | 1 391 000 | начинаем prototype |
| M3 | + CTO | 2 106 000 | security architecture |
| M4 | + ML Engineer | 2 756 000 | core policy logic |
| M5 | + Backend #2 + Frontend | 3 692 000 | build-out admin/workbench |
| M6 | + DevOps | 4 147 000 | private-cloud readiness |
| M7 | + SDR | 4 396 000 | outbound starts |
| M8 | + AE | 4 864 000 | pipeline coverage |
| M9 | без новых | 4 864 000 | AE ramp still incomplete |
| M10 | + Customer Success | 5 176 000 | onboarding capacity |
| M11 | без новых | 5 176 000 | stable team |
| M12 | без новых | 5 176 000 | full run-rate |

Sanity: нет найма 5+ человек в M1, FOT в M1-M3 не занижен, масштабирование соответствует time-to-hire.

## Fixed costs breakdown / месяц

| Статья | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5 176 600 |
| Base cloud / staging / shared infra | 250 000 |
| CRM, телефония, tooling | 78 000 |
| Legal, accounting, audit | 120 000 |
| Office/admin/G&A | 160 000 |
| Travel / industry events base | 180 000 |
| **Итого fixed costs / мес** | **5 964 600 ₽** |

## Break-even
- **Contribution / клиент / мес** = **190 000 ₽**.
- **Break-even by client count** = 5 964 600 / 190 000 = **31.4**, округляю до **32 клиентов**.
- С запасом на просадки и ramp продаж инвестиционно разумнее считать **35 клиентов** как operational break-even.
- **Break-even by month**: при траектории 0, 0, 0, 1, 2, 3, 5, 7, 10, 14, 18, 22, 26, 30, 34, 37 клиентов компания проходит cash operating break-even около **M18-M20**.

## Burn-to-breakeven
- На run-rate до выхода в 30+ клиентов бизнес жжёт примерно **5.9-6.3 млн ₽/мес** fixed burn плюс variable onboarding.
- За первые 12 месяцев cumulative burn до существенного revenue coverage составит около **46-52 млн ₽**.
- До operational break-even требуется примерно **70-80 млн ₽** совокупного финансирования, если идти без резкого урезания команды.

## Cash runway
- Беру **startup_capital = 90 млн ₽** как реалистичный запас для enterprise B2B SaaS.
- При среднем burn первых 12 месяцев **~4.9 млн ₽/мес**, затем **~3.5-4.0 млн ₽/мес** после появления revenue, runway составляет около **19-21 месяцев**.
- Это даёт шанс дожить до M18-M20 break-even, но запаса мало. Раунд меньше **60 млн ₽** выглядел бы рискованно.

## Проверка Profit Gate
- При **50 клиентах**: MRR = **15.0 млн ₽**, gross profit = **9.5 млн ₽/мес**.
- EBITDA approximation = 9.5 млн - 5.96 млн fixed = **~3.54 млн ₽/мес** до экстра-найма.
- Следовательно, критерий **EBITDA > 500k/mo achievable even at 50 clients** выполняется уверенно.
- **LTV/CAC > 1** и даже **>3**. Значит формальный reject по Profit Gate не требуется.

## Риски для экономики
1. Если MRR упадёт ниже **250k**, LTV/CAC быстро соскальзывает к **3.0x** и ниже.
2. Если churn ухудшится до **2.5% monthly**, LTV упадёт до **7.6 млн ₽**, а LTV/CAC станет **2.3x**.
3. Если придётся держать более тяжёлую implementation team, contribution margin уйдёт ниже **55%**.
4. Самая уязвимая часть модели, не COGS, а **скорость закрытия regulated deals**.

## Итог
- **Economics verdict**: **PASS, но узко**.
- Investable только как **high-ticket enterprise compliance AI** с private-cloud delivery, слабой зависимостью от paid acquisition и очень дисциплинированным GTM.
- Для фонда это не mass-scale SaaS, а thesis на дорогие сделки, долгий цикл и умеренное число клиентов.
