---
stage: unit-economics
case: kintsugi-geo-expand-v2
date: 2026-06-08
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: FAIL
confidence: medium
---

# 04-economics

## Executive summary
**Статус: FAIL.**

Локальный реалистичный сценарий для РФ не выглядит как premium tax automation SaaS. По данным demand-этапа buyer скорее покупает дешёвую бухгалтерию и аутсорсинг для маркетплейсов, а не отдельный high-ACV слой tax compliance. Поэтому для unit economics беру не американский enterprise dream-case, а более правдоподобный локальный сценарий: **productized tax ops / бухгалтерия+compliance для seller- и SMB-сегмента** с чеком **35 000 ₽/клиент/мес**. [T1][T2][T3][T4]

В этой модели:
- blended **fully-loaded CAC = 311 583 ₽**,
- **COGS = 15 700 ₽/клиент/мес**, contribution per client = **19 300 ₽/мес**,
- monthly churn принят **4%** для service-heavy SMB B2B, что даёт **LTV = 481 250 ₽**,
- **LTV/CAC = 1.54x**, что ниже investment-grade порога 3.0x,
- **CAC payback = 8.9 мес**, формально терпимо, но не спасает слабый LTV/CAC,
- fixed costs = **5 603 000 ₽/мес**,
- break-even = **291 клиента**,
- при **50 клиентах EBITDA = -4.64 млн ₽/мес**, то есть Profit Gate не проходит.

## 1. Рабочие допущения модели

### ICP для расчёта
Не считаю enterprise cross-border giant account, потому что demand-файл прямо показывает, что в РФ основной observable demand сидит в low-ticket bookkeeping bucket. Модель строится для локального платящего клиента типа:
- seller / merchant на маркетплейсах,
- небольшая e-commerce компания,
- SMB digital business с болью по НДС, учёту и filing.

### Ценообразование
| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний чек | 35 000 ₽/клиент/мес | выше массовой бухгалтерии, но ниже enterprise tax platform; попытка productized premium-слоя поверх локального рынка [T3][T4] |
| New paying customers / мес в base case | 6 | комбинация outbound + paid + partners |
| Startup capital | 30 000 000 ₽ | минимально правдоподобный стартовый капитал для B2B taxtech c командой и продажами |
| Сегмент CAC-multiplier | SMB / lower mid-market | для sanity-check применяю полный fully-loaded CAC и сверяю с бенчмарками [T5] |

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор intent-сигналов и базы лидов | SDR | hh/market maps, Excel, CRM | 20 мин/лид | 350 | низкая |
| 2 | Первичный outbound contact | SDR | почта, телефония, CRM | 15 мин/лид | 260 | средняя |
| 3 | Qualification call | SDR | телефония, CRM | 30 мин/лид | 520 | средняя |
| 4 | Discovery по налоговому контуру | AE + founder | видео, CRM, note taker | 60 мин/opportunity | 2 200 | низкая |
| 5 | Предварительный tax-fit / scope check | Tax ops lead | checklist, spreadsheet | 90 мин/opportunity | 2 000 | низкая |
| 6 | Demo продукта / кабинета | AE + product | demo env, CRM | 60 мин | 2 400 | средняя |
| 7 | Коммерческое предложение | AE | шаблон КП, e-sign | 45 мин | 1 650 | средняя |
| 8 | Security / legal / DPA ответы | founder + ops | docs, email | 120 мин на win | 5 000 | низкая |
| 9 | Contracting | AE + accountant | ЭДО, CRM | 60 мин на win | 2 100 | средняя |
| 10 | Invoice / payment link | accountant | банк, CRM, billing | 30 мин на win | 700 | высокая |
| 11 | Onboarding и настройка интеграций | CSM + backend | admin panel, API, support | 6 часов на клиента | 12 000 | средняя |
| 12 | Ежемесячный tax monitoring | Tax ops + backend | dashboard, rules engine | 2.5 ч/мес | 5 500 | средняя |
| 13 | Filing / reconciliation / client support | Tax ops + CSM | support desk, docs | 2.2 ч/мес | 6 500 | низкая |
| 14 | Повторный monthly billing | accountant / billing | billing, банк | 20 мин/мес | 1 000 | высокая |

**Вывод по процессу:** бизнес не self-serve. Это heavy-touch motion с заметной долей ручного tax ops и customer success. Поэтому CAC и COGS нельзя считать как у чистого SaaS.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Облако и хостинг | 2 000 | серверы, БД, мониторинг, LLM/automation reserve |
| Переменная доля backend / support engineering | 2 500 | 1 backend partially allocated на клиентскую поддержку |
| Tax ops analyst time | 6 000 | ~2 часа в месяц сложной проверки и filing |
| Customer Success / support | 3 000 | 1.2 часа сопровождения |
| Onboarding amortization | 1 500 | ~12 000 ₽ разовый onboarding, растянутый на 8 мес среднего retention |
| Платёжные и документооборот | 700 | банк, ЭДО, эквайринг |
| **Итого COGS** | **15 700** |  |

**Gross profit / client / month = 35 000 - 15 700 = 19 300 ₽**

## 4. CAC по каналам и funnel conversion

### Воронка по каналам
| Канал | Лиды/мес | Qualification | Demo | Proposal | New paying | Конверсия lead→paying | CAC raw, ₽ | CAC channel, fully-loaded, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound SDR | 320 | 48 | 12 | 6 | 2 | 0.63% | 345 000 | 450 000 |
| Paid search / performance | 55 | 18 | 10 | 4 | 1 | 1.82% | 200 000 | 260 000 |
| Partners / referrals | 12 | 6 | 4 | 2 | 1 | 8.33% | 107 700 | 140 000 |
| Founder-led inbound / network | 14 | 7 | 4 | 2 | 2 | 14.29% | 61 500 | 80 000 |

### Blended fully-loaded CAC

#### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 260 000 | рабочий бюджет performance для теста спроса | inference from launch budget |
| Outbound team FOT (SDR/AE attributed to new) | 868 000 | SDR 234k fully-loaded + AE 429k fully-loaded + 35% AE attributed + commissions | HH.ru benchmark + model [T6][T7] |
| Marketing team FOT (partial allocation) | 234 000 | part-time growth marketer 180k gross + 30% взносы | HH.ru benchmark range / model |
| Tools (CRM, Apollo, LinkedIn Sales Nav, телефония, ЭДО) | 111 500 | HubSpot 2 seats + Apollo 3 seats + Sales Navigator 2 seats + misc | [T8][T9][T10] |
| Events/partnerships | 180 000 | 1 локальный ивент/мес + referral payouts | inference |
| Overhead multiplier (x1.3) | 216 000 | applied to non-headcount acquisition overhead bucket | std for SMB B2B [T5] |
| **Итого acquisition cost / мес** | **1 869 500** |  |  |
| **New paying customers / мес** | **6** | blended across channels | model |
| **Fully-loaded CAC** | **311 583 ₽** | 1 869 500 / 6 |  |

### Sanity check vs benchmark
Для SMB self-serve в РФ ожидается 5-30k CAC, для mid-market SaaS 60-250k, для regulated / heavy-touch motion выше. У нас **311.6k ₽** выглядит слишком дорого для обычного SMB, но логично для tax-heavy продаж с длинным циклом и ручным onboarding. Это и есть ключевая проблема: локальный рынок покупает дешёвую бухгалтерию, а продаётся дорогой acquisition motion. [T5][T3][T4]

## 5. LTV и churn

### Churn assumption
Для service-heavy SMB B2B беру **monthly logo churn = 4%**. Это хуже best-in-class SaaS, потому что локальный buyer price-sensitive, легко уходит в бух-аутсорс или обратно в ручной режим. Бенчмарк по B2B SaaS обычно ниже: 3-8% monthly для SMB и заметно ниже для enterprise. [T11]

### Расчёт
- ARPA = **35 000 ₽/мес**
- Contribution margin per client = **19 300 ₽/мес**
- Monthly churn = **4%**
- **LTV = 19 300 / 0.04 = 482 500 ₽**

Округляю до **481 250-482 500 ₽**; в дальнейших коэффициентах использую **481 250 ₽** как консервативное значение.

## 6. LTV/CAC

| Метрика | Значение |
|---|---:|
| LTV | 481 250 ₽ |
| Fully-loaded CAC | 311 583 ₽ |
| **LTV/CAC** | **1.54x** |

**Инвестиционный вывод:** ниже порога **3.0x**, ниже даже комфортного минимума 2.0x. Для fund-level сделки это **reject**.

## 7. CAC Payback

Формула по mandate: **CAC Payback = CAC / MRR per customer**

- CAC = **311 583 ₽**
- MRR per customer = **35 000 ₽**
- **CAC Payback = 8.9 месяца**

Формально это < 12 месяцев и само по себе выглядело бы терпимо. Но payback не спасает, потому что удержание и contribution слишком слабые.

## 8. Contribution Margin %

- Revenue / client = **35 000 ₽**
- COGS / client = **15 700 ₽**
- Contribution / client = **19 300 ₽**
- **Contribution Margin = 55.1%**

Для настоящего investable SaaS хотелось бы существенно выше. Здесь маржа съедается ручным tax ops и поддержкой.

## 9. Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | продажи, fundraising, ключевые сделки | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | архитектура, roadmap, security | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | core product, integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | filing engine, data sync | 420 000 | 126 000 | 546 000 |
| Frontend | кабинет клиента, UX flows | 300 000 | 90 000 | 390 000 |
| DevOps | infra, monitoring, deploy | 350 000 | 105 000 | 455 000 |
| Tax Ops Analyst | tax operations, filing QA | 220 000 | 66 000 | 286 000 |
| Accountant / finance ops | billing, docs, reconciliation | 200 000 | 60 000 | 260 000 |
| SDR | outbound acquisition | 180 000 | 54 000 | 234 000 |
| AE | demos, proposals, closing | 330 000 | 99 000 | 429 000 |
| Customer Success | onboarding, renewals | 240 000 | 72 000 | 312 000 |
| Growth marketer (0.8 FTE modelled) | paid, content, events | 180 000 | 54 000 | 234 000 |
| **Итого** |  |  |  | **5 252 000 ₽/мес** |

### Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1.5 | 126 000 | 546 000 each |
| ML Engineer (если AI core) | 0 | 0 | - | - | - | 0 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 180 000 | 0.5-1 | 1 | 54 000 | 234 000 |
| AE (Account Exec) | 1 | 330 000 | 1-2 | 2-3 | 99 000 | 429 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Tax Ops Analyst | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Accountant / finance ops | 1 | 200 000 | 1 | 1 | 60 000 | 260 000 |
| Growth marketer | 0.8 | 180 000 | 1 | 1 | 54 000 | 234 000 |

**Комментарий по realism:** уже этот состав даёт >5.2 млн ₽ fully-loaded FOT. Это подтверждает, что локальный low-ticket рынок не выдерживает такую cost base.

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже работает | FOT / мес, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, Backend#1, Tax Ops | 1 677 000 | старт с 3 людьми, без перегруза найма |
| M2 | + Frontend, SDR | 2 301 000 | начинают сбор спроса и MVP client flows |
| M3 | + CTO, Accountant | 3 276 000 | tech governance и billing |
| M4 | + AE | 3 705 000 | sales motion только начинает раскручиваться |
| M5 | + DevOps | 4 160 000 | инфраструктура становится постоянной функцией |
| M6 | + Backend#2 | 4 706 000 | вторая backend-единица после первых клиентов |
| M7 | + Customer Success | 5 018 000 | onboarding и renewals начинают давить |
| M8 | + Growth marketer | 5 252 000 | полноценный acquisition stack |
| M9 | та же команда | 5 252 000 |  |
| M10 | та же команда | 5 252 000 |  |
| M11 | та же команда | 5 252 000 |  |
| M12 | та же команда | 5 252 000 |  |

Найм-план без red flag: нет 5+ наймов в первый месяц, но даже аккуратный график быстро разгоняет burn.

## 10. Fixed costs breakdown

| Компонент fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 252 000 |
| Office / legal / admin | 120 000 |
| Core software stack (non-acquisition) | 95 000 |
| Audit / security / accounting services reserve | 76 000 |
| Infra baseline not in COGS | 60 000 |
| **Итого fixed costs** | **5 603 000 ₽/мес** |

## 11. Break-even

### Break-even по числу клиентов
- Contribution per client = **19 300 ₽/мес**
- Fixed costs = **5 603 000 ₽/мес**
- **Break-even client count = 5 603 000 / 19 300 = 290.3**, округлённо **291 клиент**

### Break-even по месяцам
Если команда привлекает **6 новых платящих клиентов в месяц** и churn = **4%/мес**, то клиентская база через 12 месяцев:
- M1: 6
- M2: 12
- M3: 18
- M4: 23
- M5: 28
- M6: 33
- M7: 38
- M8: 42
- M9: 46
- M10: 50
- M11: 54
- M12: 58

Даже в конце года это **в 5 раз ниже** break-even уровня 291 клиента. Реалистично break-even в base case **не достигается в горизонте 12 месяцев**.

## 12. Burn-to-breakeven

Для burn беру FOT + fixed + acquisition spend, минус contribution margin от клиентской базы.

| Месяц | Клиенты на конец месяца | Contribution margin, ₽ | Total burn before margin, ₽ | Net burn, ₽ |
|---|---:|---:|---:|---:|
| M1 | 6 | 115 800 | 3 546 500 | 3 430 700 |
| M3 | 18 | 347 400 | 5 145 500 | 4 798 100 |
| M6 | 33 | 636 900 | 6 575 500 | 5 938 600 |
| M9 | 46 | 887 800 | 7 121 500 | 6 233 700 |
| M12 | 58 | 1 119 400 | 7 121 500 | 6 002 100 |

Даже при росте выручки месячный burn почти не закрывается, потому что acquisition + team base слишком тяжёлые.

## 13. Cash runway

- Startup capital = **30 000 000 ₽**
- Средний net burn в M1-M12 ≈ **4.9 млн ₽/мес**
- **Cash runway ≈ 6.1 месяца**

Даже если урезать часть найма, до устойчивого break-even всё равно очень далеко. Для enterprise SaaS / taxtech такой стартовый капитал уже не выглядит absurdly low, но для данной локальной экономики он сгорает слишком быстро.

## 14. Profit Gate check

### Проверка 1: EBITDA at 50 clients
- Revenue = 50 × 35 000 = **1 750 000 ₽/мес**
- COGS = 50 × 15 700 = **785 000 ₽/мес**
- Gross contribution = **965 000 ₽/мес**
- Fixed costs = **5 603 000 ₽/мес**
- **EBITDA = -4 638 000 ₽/мес**

### Проверка 2: LTV/CAC
- **1.54x**, ниже минимально допустимого 3.0x и ниже safe-zone 2.0x.

## 15. Итоговый вывод
**FAIL / REJECTED.**

Почему:
1. локальный рынок показывает цену и ожидания ближе к бухгалтерскому сервису, чем к premium SaaS [T3][T4],
2. heavy-touch sales + onboarding делают blended CAC слишком высоким,
3. ручной tax ops удерживает contribution margin на уровне около 55%,
4. **LTV/CAC = 1.54x** не проходит investment-grade порог,
5. при 50 клиентах бизнес глубоко убыточен, а break-even требует **291 клиента**, что противоречит observed demand.

Следовательно, кейс нужно **отклонять на economics-этапе** и переносить в rejected.

## Источники
- [T1] pipeline/cases/kintsugi-geo-expand-v2/02-demand.md
- [T2] Kintsugi Product Overview: https://www.trykintsugi.com/product/overview
- [T3] Моё дело, бухгалтерия для маркетплейсов: https://www.moedelo.org/tovarouchet/marketplace
- [T4] Saby, тарифы «Бухгалтерия»: https://saby.ru/accounting/tariffs
- [T5] User mandate, industry CAC sanity ranges for RU 2024-2026, used as benchmark guardrail in this cycle
- [T6] HH.ru search, Senior backend salary market: https://hh.ru/search/vacancy?text=senior+backend+developer
- [T7] HH.ru search, Account executive salary market: https://hh.ru/search/vacancy?text=account+executive
- [T8] HubSpot Sales Hub pricing: https://www.hubspot.com/pricing/sales
- [T9] Apollo pricing: https://www.apollo.io/pricing
- [T10] LinkedIn Sales Navigator pricing: https://business.linkedin.com/sales-solutions/compare-plans
- [T11] Vitally, acceptable SaaS churn benchmarks: https://www.vitally.io/post/acceptable-churn-rate-saas
