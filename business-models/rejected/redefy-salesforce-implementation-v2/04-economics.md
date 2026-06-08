---
stage: unit-economics
case: redefy-salesforce-implementation-v2
date: 2026-06-08
analyst: branch-models-lead
verdict: REJECT
confidence: medium
---

# 04-economics — Unit Economics

## Краткий вывод
**Итог: REJECT по Program 5.**

Даже если признать спрос на enterprise Salesforce/Agentforce implementation, сам unit economics ядра выглядит слабым как инвест-кейс:
- fully-loaded **blended CAC = 1,81 млн ₽** на нового платящего клиента;
- steady-state managed-services **MRR на клиента = 300 тыс. ₽/мес**;
- **COGS = 263 тыс. ₽/клиент/мес**;
- gross profit = **37 тыс. ₽/клиент/мес**;
- **LTV = 1,43 млн ₽** при annual churn benchmark **27%**;
- **LTV/CAC = 0,79x**, то есть ниже даже минимального порога 1:1;
- **CAC payback = 6,0 мес по валовой прибыли** и **60,5 мес по contribution margin**, что неприемлемо для project-heavy operator;
- при масштабировании до **50 клиентов EBITDA остаётся отрицательной**, потому что валовая маржа слишком тонкая, а штат и presale дорогие.

Ключевой вывод: это больше похоже на тяжёлый AI-native SI/implementation business с дорогим пресейлом и низкой стандартизацией delivery, чем на инвестиционно-качественный software-enabled operator.

## 1) Нормализованный unit of analysis
Чтобы не завышать экономику одноразовым внедренческим чеком, считаю юнитом **одного активного managed-services клиента после go-live**.

### Нормализованные допущения
- initial implementation чек: **4,8-6,0 млн ₽** единовременно, но проектная маржа нестабильна и сильно зависит от кастома;
- recurring support / optimization / governance retainer: **300 тыс. ₽/мес**;
- модель продаж: founder-led + partner referrals + enterprise outbound;
- sales cycle: **6-9 месяцев**;
- segment: **enterprise / regulated-adjacent B2B**, поэтому fully-loaded CAC считаю по enterprise-мультипликатору сложности, но не завышаю выше отдельной строки overhead.

## 2) Подробный бизнес-процесс от lead до оплаты
| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Поиск целевых enterprise-аккаунтов | SDR + founder | LinkedIn/Sales Navigator, CRM, spreadsheet | 3 ч | 4 500 | низкая |
| 2 | Исходящий outreach / partner intro | SDR / founder | email, LinkedIn, партнёрские интро | 5 ч | 8 000 | низкая |
| 3 | Qualification call | Founder/AE | Zoom, CRM | 1 ч | 6 000 | низкая |
| 4 | Discovery по текущему Salesforce-ландшафту | AE + solution consultant | Zoom, Miro, CRM | 4 ч | 18 000 | низкая |
| 5 | Security / integration scoping | solution architect + tech lead | diagramming, sandbox, docs | 10 ч | 55 000 | низкая |
| 6 | Подготовка demo / POV | architect + backend + AE | sandbox, demo env, AI tooling | 18 ч | 96 000 | средняя |
| 7 | Коммерческое предложение и SoW | AE + founder + legal | CRM, docs, e-sign | 6 ч | 34 000 | низкая |
| 8 | Procurement / legal / infosec review | founder + legal + architect | почта, DPA/MSA, security docs | 12 ч | 78 000 | низкая |
| 9 | Negotiation + close | founder + AE | CRM, calls | 5 ч | 31 000 | низкая |
| 10 | Invoice + payment collection | finance ops | accounting, bank, ЭДО | 2 ч | 7 500 | средняя |
| 11 | Onboarding и kickoff | CSM + architect + PM | PM tool, Slack/Teams, docs | 8 ч | 41 000 | средняя |

**Итого pre-sale + close cost на одну победу:** примерно **379 тыс. ₽** прямых человеко-часов без учёта маркетинга, SDR-пайплайна, событий и overhead. Это и объясняет, почему raw advertising CAC здесь не работает: основная стоимость съедается пресейлом и дорогими людьми.

## 3) COGS breakdown на клиента в месяц
Беру steady-state клиента на recurring retainer **300 тыс. ₽/мес**.

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| Salesforce / solution architect allocation | 85 000 | ~0,15 FTE senior architect | постоянные изменения, governance |
| Integration / backend engineer allocation | 70 000 | ~0,13 FTE senior backend | API, flows, data sync |
| Solution consultant / analyst | 45 000 | ~0,10 FTE | change requests, reporting |
| QA / PM allocation | 25 000 | частичная аллокация | regression + coordination |
| Cloud / sandbox / internal infra | 12 000 | sandbox, logging, support env | vendor-neutral estimate |
| AI tooling / copilots / evals | 8 000 | LLM/API/tooling на аккаунт | service enablement |
| Customer success / support allocation | 18 000 | ~0,06 FTE | SLA, weekly sync |
| **Итого COGS** | **263 000** |  |  |

### Gross margin
- Revenue per client/month: **300 000 ₽**
- COGS per client/month: **263 000 ₽**
- **Gross profit: 37 000 ₽/мес**
- **Gross margin: 12,3%**

Для investment-grade operator это слишком мало. Любой дополнительный кастом, перерасход часов или задержка интеграции легко съедает остаток маржи.

## 4) CAC по каналам с воронкой

### Канал A. Founder-led outbound
| Метрика | Значение |
|---|---:|
| Целевые аккаунты в работе / мес | 500 |
| Reply / intro rate | 6,0% |
| Intro calls | 30 |
| Discovery | 8 |
| Proposal / SoW | 3 |
| New paying customers | 1 |
| Конверсия account → paying | 0,2% |
| Monthly spend | 2 060 000 ₽ |
| **CAC** | **2 060 000 ₽** |

Состав spend: SDR FOT, founder/AE time, solutions pre-sale, CRM/tool stack, частично events.

### Канал B. Partner referrals / ecosystem
| Метрика | Значение |
|---|---:|
| Partner intros / мес | 20 |
| Discovery | 6 |
| Proposal | 3 |
| New paying customers | 1 |
| Конверсия intro → paying | 5,0% |
| Monthly spend | 870 000 ₽ |
| **CAC** | **870 000 ₽** |

Канал лучший по CAC, но его нельзя считать полностью контролируемым и масштабируемым: объём интро ограничен узким ecosystem pool.

### Канал C. Content / inbound / events
| Метрика | Значение |
|---|---:|
| MQL / мес | 50 |
| SQL | 10 |
| Proposal | 4 |
| New paying customers | 1 |
| Конверсия MQL → paying | 2,0% |
| Monthly spend | 1 120 000 ₽ |
| **CAC** | **1 120 000 ₽** |

### Blended CAC
Предполагаю mix новых клиентов: 50% outbound, 30% partner, 20% inbound.

**Blended raw CAC = 1 395 000 ₽.**

## 5) Fully-loaded CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT + Marketing FOT allocation + Tools/CRM + Events + Overhead multiplier) / New paying customers`

### Таблица fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads / paid distribution | 180 000 | тестовые paid touchpoints + retargeting на узкую enterprise-аудиторию | internal model + enterprise GTM assumption |
| Outbound team FOT (SDR + AE attributed to new) | 611 000 | SDR 150k gross + 30% = 195k; AE 320k gross + 30% = 416k; 100% атрибутировано acquisition | HH.ru vacancy search + model |
| Marketing team FOT allocation | 143 000 | 220k gross × 50% time × 1,3 | HH.ru benchmark range + model |
| Solutions / sales engineering allocation | 182 000 | 280k gross × 50% time × 1,3 | market benchmark + model |
| Tools / CRM / Sales Nav / outreach stack | 99 000 | CRM + prospecting + meeting + docs | market software estimate |
| Events / partnerships | 180 000 | ecosystem events, co-marketing, travel share | model |
| Overhead multiplier (x1.3) | 419 000 | 30% на subtotal 1 395 000 ₽ | standard overhead add-on для enterprise B2B |
| **Итого fully-loaded acquisition spend / мес** | **1 814 000** |  |  |
| **New paying customers / мес** | **1,0** | узкий enterprise throughput | model |
| **Fully-loaded CAC** | **1 814 000 ₽** |  |  |

### Sanity check vs benchmark
- Внутренний benchmark из standing orders для Enterprise SaaS B2B в РФ: **300-900 тыс. ₽/клиент**.
- Здесь CAC **выше** этой вилки, что допустимо только потому, что это не SaaS, а тяжёлый implementation motion с большим presale burden, founder involvement и procurement cycle.
- Иначе говоря, если считать честно fully-loaded, а не только paid ads, клиент очень дорогой.

## 6) LTV и churn
### Benchmark по churn
Для project-heavy B2B / professional services взял консервативный benchmark annual churn **27%** как ориентир для менее удерживаемых B2B-моделей; это заметно хуже классического enterprise SaaS и ближе к реальности, когда клиент после внедрения может сократить retainer, перевести поддержку in-house или к другому SI. Также использован sanity-check против IT-services benchmarks с lower churn **10-15% annual**.

### Принятое значение
- **Annual churn: 27%**
- **Monthly churn: 2,59%**
- Ожидаемая life в модели: **38,6 месяца**

### Формула LTV
`LTV = Monthly gross profit / Monthly churn`

- Monthly gross profit = **37 000 ₽**
- Monthly churn = **2,5885%**
- **LTV = 1 429 400 ₽**

### Интерпретация
Даже при сохранении клиента дольше 3 лет, слабая gross margin не даёт накопить достаточно валовой прибыли, чтобы окупить acquisition.

## 7) LTV/CAC ratio
- **LTV = 1 429 400 ₽**
- **Fully-loaded CAC = 1 814 000 ₽**
- **LTV/CAC = 0,79x**

### Вывод
- Порог investable quality: **≥3,0x**
- Минимальный порог выживания: **≥1,0x**
- Фактическое значение: **0,79x**

**Итог: бизнес не проходит даже базовый порог окупаемости.**

## 8) CAC payback
Показываю оба варианта, потому что для services-бизнеса payback по выручке вводит в заблуждение.

### Payback по MRR
`CAC / MRR per customer = 1 814 000 / 300 000 = 6,05 месяца`

Формально это выглядит терпимо, но это ложноположительный сигнал, потому что MRR почти полностью съедается delivery.

### Payback по gross profit
`CAC / Gross profit per customer = 1 814 000 / 37 000 = 49,0 месяца`

### Payback по contribution margin
Если учесть переменную комиссию/аккаунтинг на нового клиента ещё **7,5% выручки = 22 500 ₽/мес**, то:
- contribution per client = **14 500 ₽/мес**
- **CAC payback = 125,1 месяца**

### Вывод
Для фонда имеет смысл смотреть не на payback по выручке, а по gross profit / contribution. Там картина критическая.

## 9) Contribution Margin %
| Показатель | ₽/клиент/мес |
|---|---:|
| Revenue | 300 000 |
| COGS | 263 000 |
| Gross profit | 37 000 |
| Variable commissions / billing friction | 22 500 |
| **Contribution profit** | **14 500** |

**Contribution Margin = 14 500 / 300 000 = 4,8%**

Это слишком мало для тяжёлой enterprise-модели с длинным cash cycle.

## 10) Team & FOT

### Полная таблица команды
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес | Функция |
|---|---:|---:|---:|---:|---|---:|---|
| CEO | 1 | 650 000 | 0 | 0 | +30% | 845 000 | founder-led sales, key accounts |
| CTO / Tech Lead | 1 | 550 000 | 2,5 | 2 | +30% | 715 000 | enterprise architecture, quality gate |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | +30% | 1 092 000 | integrations, custom APIs |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | +30% | 650 000 | AI-native automation, evals |
| DevOps | 1 | 360 000 | 1,5 | 1 | +30% | 468 000 | env, infra, deployment |
| Frontend | 1 | 300 000 | 1 | 1 | +30% | 390 000 | internal tools / admin UI |
| SDR | 1 | 150 000 | 0,75 | 1 | +30% | 195 000 | outbound top-of-funnel |
| AE | 1 | 320 000 | 1,5 | 2,5 | +30% | 416 000 | enterprise close |
| Customer Success | 1 | 240 000 | 1 | 1 | +30% | 312 000 | retention, renewals |
| **Итого** | **10** |  |  |  |  | **5 083 000** |  |

### Комментарий по realism
- План найма не нарушает sanity rule 5+ hires в первый месяц: в M1 только founder.
- Но к steady state компания всё равно приходит к **5,08 млн ₽ FOT/мес** ещё до офиса, юррасходов и acquisition stack.
- Для узкого рынка это тяжёлая cost base.

## 11) Cumulative FOT timeline M1-M12
| Месяц | Кого реально успеваем подключить | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO/founder | 845 000 |
| M2 | + SDR, + Frontend | 1 430 000 |
| M3 | + Senior Backend #1, + Customer Success | 2 288 000 |
| M4 | + AE, + DevOps | 3 172 000 |
| M5 | + CTO/Tech Lead, + ML Engineer | 4 537 000 |
| M6 | + Senior Backend #2 | 5 083 000 |
| M7 | full team | 5 083 000 |
| M8 | full team | 5 083 000 |
| M9 | full team | 5 083 000 |
| M10 | full team | 5 083 000 |
| M11 | full team | 5 083 000 |
| M12 | full team | 5 083 000 |

## 12) Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5 083 000 |
| Internal infra / shared cloud / security / sandboxes | 240 000 |
| G&A / legal / бухучёт / ЭДО | 210 000 |
| Travel / partner meetings / field enablement | 280 000 |
| Office / coworking / hardware reserve | 170 000 |
| Management software / PM / collaboration | 105 000 |
| **Итого fixed costs** | **6 088 000 ₽/мес** |

## 13) Break-even
### По количеству клиентов
Использую contribution profit **14 500 ₽/клиент/мес**.

`Break-even clients = 6 088 000 / 14 500 = 420 клиентов`

Даже если считать по gross profit, а не contribution:

`6 088 000 / 37 000 = 165 клиентов`

Обе цифры существенно выше реалистичной capacity boutique enterprise operator.

### По месяцам
Даже при оптимистичном росте active retainers:
- M6: 2 клиента → contribution ~29 тыс. ₽
- M9: 5 клиентов → contribution ~72,5 тыс. ₽
- M12: 9 клиентов → contribution ~130,5 тыс. ₽

При fixed cost 4,5-6,1 млн ₽/мес компания **не выходит на break-even в горизонте 12 месяцев**.

## 14) Burn-to-breakeven
Даже в optimistic hiring+sales сценарии burn выглядит так:
- ранние месяцы: **2,0-4,5 млн ₽/мес** burn;
- после полной сборки команды: **~6,0 млн ₽/мес** fixed burn до маркетинга-сверху;
- клиентская contribution-экономика слишком тонкая, чтобы компенсировать burn.

**Burn-to-breakeven** при текущей модели фактически неограничен: для достижения операционного нуля нужен либо резкий рост retainer pricing, либо снижение delivery headcount per account, либо перевод продукта в software-like model.

## 15) Cash runway
Допущение: **startup capital = 25 млн ₽**.

### Runway estimate
- burn на старте (M1-M3 средний): ~**2,2 млн ₽/мес**
- burn на M4-M6: ~**4,3 млн ₽/мес**
- burn после выхода на full team: ~**5,9-6,1 млн ₽/мес**

Если считать blended burn по первому году около **4,0 млн ₽/мес**, то:

`Cash runway = 25 000 000 / 4 000 000 = 6,25 месяца`

Для enterprise B2B SaaS-like истории это red flag: до продаж и до стабильного продления runway слишком короткий.

## 16) EBITDA check при 50 клиентах
Это обязательная проверка на фондовом уровне.

### Сценарий 50 active retainers
- Revenue: **50 × 300 000 = 15,0 млн ₽/мес**
- COGS: **50 × 263 000 = 13,15 млн ₽/мес**
- Gross profit: **1,85 млн ₽/мес**
- Fixed costs: **6,09 млн ₽/мес**
- EBITDA до налогов и без экстраординарного project revenue: **-4,24 млн ₽/мес**

**Следовательно, компания не достигает EBITDA 500 тыс. ₽/мес даже при 50 клиентах. Profit Gate FAIL.**

## 17) Что должно измениться, чтобы экономика стала investable
Минимум один из трёх сдвигов:
1. поднять recurring retainer хотя бы до **600-800 тыс. ₽/мес** без пропорционального роста COGS;
2. сократить delivery COGS на клиента минимум на **35-40%** через реальную продуктовую стандартизацию;
3. убрать founder-heavy/solution-heavy presale и опустить fully-loaded CAC ближе к **700-900 тыс. ₽**.

Пока этого в кейсе не видно.

## Итоговый вердикт по economics
**REJECT.**

Это жизнеспособный boutique services business только в режиме project cashflow, но не инвестиционно-качественный operator:
- нет доказанной software-like repeatability;
- маржа слишком тонкая;
- CAC слишком дорогой для такого GP profile;
- break-even требует unrealistically high client count;
- LTV/CAC < 1,0x.

## Источники
- [T1] `02-demand.md` кейса ReDEFY, внутренний анализ спроса и ценового якоря Salesforce Agentforce.
- [T2] Salesforce Agentforce Pricing: https://www.salesforce.com/agentforce/pricing/
- [T3] ReDEFY homepage / positioning: https://redefy.com/
- [T4] HH.ru vacancy search, CTO: https://hh.ru/search/vacancy?text=CTO
- [T5] HH.ru vacancy search, Senior Backend Developer: https://hh.ru/search/vacancy?text=Senior+Backend+Developer
- [T6] CustomerGauge / churn benchmarks search result context, checked 2026-06-08.
- [T7] Benchmarkit churn benchmark search result context, checked 2026-06-08.

Примечание: T6-T7 использованы только как benchmark sanity для диапазона churn; итоговая модель консервативно выбирает высокий churn, потому что здесь project-heavy enterprise services, а не чистый SaaS.