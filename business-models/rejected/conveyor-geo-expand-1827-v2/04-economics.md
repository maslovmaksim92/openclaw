---
stage: economics
case: conveyor-geo-expand-1827-v2
date: 2026-05-09
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics / Fund View

## Executive summary

**Итог: REJECTED.**

Почему:
1. Для локального enterprise GTM модель требует дорогой product + presales + CS команды ещё до выхода на scale.
2. При реалистичной цене **210 тыс. ₽ MRR на клиента** и fully-loaded CAC **1,44 млн ₽** продукт даёт нормальный LTV/CAC, но **не проходит profit gate фонда**.
3. Даже при **50 активных клиентах** расчётный EBITDA остаётся **ниже 500 тыс. ₽/мес**: около **-220 тыс. ₽/мес** при полной fixed-cost базе и необходимом GTM-контуре.
4. Точка безубыточности получается около **52 клиентов**, что для узкого buyer universe в РФ слишком напряжённо.

## 1. Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Upper-mid / enterprise B2B | B2B SaaS, cloud, fintech, cyber vendors |
| Средний контракт | 2,52 млн ₽/год | 210 тыс. ₽ MRR, annual billing со скидкой уже учтён |
| Setup / onboarding fee | 450 тыс. ₽ разово | Не включён в MRR, помогает cash-in, но не спасает EBITDA |
| Активные клиенты в целевом steady state | 50 | Проверка profit gate |
| New paying customers / мес в steady state | 4 | 1 paid, 1 outbound, 1 partner/event, 1 mix |
| Churn rate | **2,0% в месяц** | Взят ближе к верхней границе enterprise SaaS benchmark 1-2% monthly |
| Gross margin | **73,3%** | После recurring COGS |
| Startup capital | **60 млн ₽** | Для расчёта burn и runway |

## 2. Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов | SDR | HH/рынок, LinkedIn-аналоги, Excel/CRM | 30 мин/аккаунт | 1 200 | Низкая |
| 2 | Первый outreach | SDR | Email, Telegram, CRM sequences | 15 мин | 600 | Средняя |
| 3 | Follow-up 3-5 касаний | SDR | CRM, почта, звонки | 45 мин | 1 800 | Средняя |
| 4 | Qualification call | SDR + AE | Meet/Zoom, CRM | 45 мин | 4 500 | Низкая |
| 5 | Discovery по questionnaire pain | AE + Sales Engineer | Meet, Notion/Docs | 90 мин | 10 500 | Низкая |
| 6 | Demo + ROI framing | AE + Solutions/Founder | Demo env, slides | 90 мин | 12 000 | Низкая |
| 7 | Security/process audit | Solutions + Security SME | Shared docs, checklist | 6 ч | 28 000 | Низкая |
| 8 | Pilot scoping | AE + CSM + Tech Lead | CRM, backlog | 3 ч | 16 000 | Низкая |
| 9 | Pilot setup (KB, answers, Trust Center) | CSM + Engineer | Product, cloud, docs | 20 ч | 78 000 | Средняя |
| 10 | Pilot support 4-8 недель | CSM + Engineer + AE | Slack/Telegram/email | 12 ч | 48 000 | Средняя |
| 11 | Procurement / InfoSec / legal | AE + Founder + Legal | Docs, email | 10 ч | 42 000 | Низкая |
| 12 | Коммерческое предложение | AE | CRM, template | 2 ч | 8 000 | Средняя |
| 13 | Переговоры и redlines | Founder + AE | Docs, calls | 6 ч | 34 000 | Низкая |
| 14 | Счёт и договор | Ops/Finance | 1C/банк/ЭДО | 2 ч | 5 000 | Средняя |
| 15 | Оплата и handoff в delivery | Finance + CSM | Банк, CRM, PM tool | 1 ч | 2 500 | Высокая |

**Вывод:** цикл сделки длинный и дорогой. Для regulated / enterprise trust workflow это не self-serve SaaS, а тяжёлый consultative sale с существенным presales effort.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/API inference | 15 000 | Генерация draft answers, RAG, re-checks |
| Cloud / hosting / compute | 8 000 | База знаний, retrieval, background jobs |
| Storage / monitoring / logging | 4 000 | Объектное хранилище, observability |
| Customer support share | 11 000 | 1 CSM на ~20-25 клиентов |
| Solutions / success engineering share | 12 000 | Пост-внедренческие доработки и сложные кейсы |
| Security / compliance maintenance share | 6 000 | Policy updates, access review |
| Billing / payment / docs | 500 | ЭДО, банк, админка |
| **Итого COGS** | **56 500** |  |

**MRR на клиента:** 210 000 ₽  
**Gross profit на клиента:** 153 500 ₽  
**Gross margin:** **73,1%-73,3%**

## 4. CAC по каналам и воронка

### 4.1 Воронка по каналам

| Канал | Leads/мес | Discovery | Pilot | Won | Конверсия lead→won | Комментарий |
|---|---:|---:|---:|---:|---:|---|
| Paid ads / intent capture | 55 | 11 | 4 | 2 | 3,6% | Высокоинтентные inbound лиды ограничены |
| Outbound ABM | 140 | 14 | 3 | 1 | 0,7% | Длинный цикл, тяжёлый доступ к buyer'у |
| Events / partners | 35 | 8 | 3 | 1 | 2,9% | Самый качественный pipeline, но дорогой |
| **Итого blended** | **230** | **33** | **10** | **4** | **1,7%** | 4 новых paying customers / мес |

### 4.2 Fully-loaded CAC

Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT (attributed) + Tools/CRM + Events + Multiplier_overhead) / New paying customers
```

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 450 000 | Поисковый спрос + ретаргетинг на узкий enterprise ICP | T4 |
| Outbound team FOT (SDR/AE attributed to new) | 1 170 000 | SDR 180k + AE 420k + 30% взносы + бонус/комиссия, 100% в new acquisition | T2, T4 |
| Marketing team FOT (partial allocation) | 260 000 | 0,5 demand gen FTE + 30% взносы | T2 |
| Tools (CRM, data, enrichment, mailing) | 140 000 | CRM + prospecting stack + call tracking | T4 |
| Events/partnerships | 420 000 | 1 отраслевое мероприятие/мес + co-marketing | T4 |
| Overhead multiplier (x1.3) | 732 000 | 30% к прямым acquisition-costs как enterprise B2B overhead | T4 |
| **Итого fully-loaded acquisition cost / мес** | **3 172 000** |  |  |
| **New paying customers / мес** | **4** | blended won deals |  |
| **Blended fully-loaded CAC** | **793 000 ₽** | 3 172 000 / 4 |  |

### 4.3 CAC по каналам

| Канал | Канальные затраты/мес, ₽ | Won/мес | CAC raw, ₽ | Мультипликатор сегмента | CAC fully-loaded, ₽ |
|---|---:|---:|---:|---:|---:|
| Paid ads / inbound enterprise | 1 012 000 | 2 | 506 000 | ×2,5 | **1 265 000** |
| Outbound ABM | 900 000 | 1 | 900 000 | ×2,0 | **1 800 000** |
| Events / partners | 720 000 | 1 | 720 000 | ×2,0 | **1 440 000** |
| **Blended** | **2 632 000** | **4** | **658 000** | учтён выше | **793 000** |

**Sanity check:** blended CAC попадает в нижнюю часть диапазона **enterprise SaaS B2B РФ 300-900k ₽** только если смотреть raw. Fully-loaded CAC ближе к **0,8 млн ₽**, что реалистичнее для сложной enterprise продажи.

## 5. LTV и churn

### Churn benchmark
- Для B2B SaaS enterprise/large accounts разумный ориентир monthly logo churn около **1-2%**. В модели взято **2,0%**, то есть консервативный конец диапазона, потому что локальный рынок узкий, а renewals зависят от доказанного ROI и качества внедрения. Источник benchmark: T1.

### Расчёт LTV

```text
LTV = (MRR × Gross Margin) / Monthly Churn
```

- MRR = 210 000 ₽
- Gross Margin = 73,3%
- Monthly Churn = 2,0%

**LTV = 7,70 млн ₽**

## 6. LTV/CAC

- **LTV = 7,70 млн ₽**
- **Blended fully-loaded CAC = 793 тыс. ₽**
- **LTV/CAC = 9,7x**

На бумаге ratio высокий. Но это не делает проект investable автоматически, потому что узкий buyer universe и тяжёлая fixed-cost база съедают прибыльность на уровне компании.

## 7. CAC payback

```text
CAC Payback = CAC / MRR per customer
```

- CAC = 793 000 ₽
- MRR per customer = 210 000 ₽

**CAC Payback = 3,8 месяца**

Это выглядит хорошо, но только если новый клиент быстро стартует и не требует сверхнормативного custom setup. На практике pilot-heavy motion легко растягивает реальный payback до 6-9 месяцев cash-wise.

## 8. Contribution Margin

| Показатель | ₽/клиент/мес | % выручки |
|---|---:|---:|
| Revenue | 210 000 | 100,0% |
| COGS | 56 500 | 26,9% |
| **Contribution after COGS** | **153 500** | **73,1%** |

Для проверки breakeven я использую именно **153,5 тыс. ₽ вклада на клиента в месяц**.

## 9. Team & FOT

### 9.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | Продажи, fundraising, ключевые сделки | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | Архитектура, delivery, security | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | Core product / integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | Data / workflow engine | 420 000 | 126 000 | 546 000 |
| ML Engineer | RAG / answer quality / evals | 500 000 | 150 000 | 650 000 |
| DevOps | Infra, observability, CI/CD | 350 000 | 105 000 | 455 000 |
| Frontend | Trust Center / admin UX | 300 000 | 90 000 | 390 000 |
| Product Manager | Roadmap / pilot feedback | 350 000 | 105 000 | 455 000 |
| SDR | Outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | Discovery, demo, negotiation | 420 000 | 126 000 | 546 000 |
| Customer Success | Onboarding / adoption / renewals | 260 000 | 78 000 | 338 000 |
| Finance / Ops | Docs, billing, procurement | 180 000 | 54 000 | 234 000 |
| **Итого команда** |  |  |  | **5 954 000 ₽/мес** |

### 9.2 Таблица найма и реализм

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 каждый |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 + бонус | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 420 000 + комиссия | 1-2 | 2-3 | 126 000 | 546 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |

### 9.3 Cumulative FOT timeline M1-M12

| Месяц | Кто в команде реально активен | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO, Backend #1, Frontend, Finance/Ops | 2 015 000 |
| M2 | + SDR, + DevOps | 2 704 000 |
| M3 | + Backend #2 | 3 250 000 |
| M4 | + CSM | 3 588 000 |
| M5 | + CTO (после найма) | 4 303 000 |
| M6 | + AE | 4 849 000 |
| M7 | + Product Manager | 5 304 000 |
| M8 | тот же состав, ramp | 5 304 000 |
| M9 | + ML Engineer | 5 954 000 |
| M10 | тот же состав | 5 954 000 |
| M11 | бонусы/комиссии и полная загрузка GTM | 6 404 000 |
| M12 | тот же состав | 6 404 000 |

**Sanity checks:**
- В первый месяц нет найма 5+ человек сверхреалистичного плана.
- FOT M1 уже выше 1 млн ₽, что соответствует реальности.
- Чтобы добежать до breakeven, проекту нужно больше 10 млн ₽, на деле сильно больше.

## 10. Fixed costs

| Статья fixed costs | ₽/мес |
|---|---:|
| Team FOT steady-state | 5 954 000 |
| Office / legal / accounting / admin | 320 000 |
| Core infra not allocated to COGS | 380 000 |
| Security / compliance / pentest reserve | 220 000 |
| General software stack | 260 000 |
| Travel / founder sales / misc | 180 000 |
| **Итого fixed costs / мес** | **7 314 000** |

## 11. Break-even

### По числу клиентов

```text
Break-even clients = Fixed costs / Contribution per client
= 7 314 000 / 153 500 ≈ 47,6 клиента
```

Но для **EBITDA > 500 тыс. ₽/мес** нужно:

```text
(7 314 000 + 500 000) / 153 500 ≈ 50,9 клиента
```

То есть нужен **51 клиент** минимум.

### По месяцу
По реалистичному плану найма и продаж в первые 12 месяцев компания **не выходит на breakeven**. К концу M12 модель показывает около **22 активных клиентов**, что даёт лишь **3,38 млн ₽ gross profit / мес** против fixed cost базы более **7,3 млн ₽/мес**.

## 12. Burn-to-breakeven

| Месяц | Активные клиенты | Gross profit, ₽ | Fixed + acquisition burn, ₽ | Чистый burn, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 950 000 | 2 950 000 |
| M2 | 0 | 0 | 2 950 000 | 2 950 000 |
| M3 | 1 | 153 500 | 3 880 000 | 3 726 500 |
| M4 | 2 | 307 000 | 4 550 000 | 4 243 000 |
| M5 | 3 | 460 500 | 5 140 000 | 4 679 500 |
| M6 | 4 | 614 000 | 5 820 000 | 5 206 000 |
| M7 | 6 | 921 000 | 6 520 000 | 5 599 000 |
| M8 | 8 | 1 228 000 | 6 520 000 | 5 292 000 |
| M9 | 11 | 1 688 500 | 7 040 000 | 5 351 500 |
| M10 | 14 | 2 149 000 | 7 040 000 | 4 891 000 |
| M11 | 18 | 2 763 000 | 7 604 000 | 4 841 000 |
| M12 | 22 | 3 377 000 | 7 604 000 | 4 227 000 |

**Вывод:** burn остаётся высоким даже к концу первого года. До безубыточности компании нужно дотянуться минимум до 51 активного клиента, а это при узком рынке и длинном цикле сделки выглядит тяжело.

## 13. Cash runway

- Startup capital: **60 млн ₽**
- Совокупный burn за M1-M12: примерно **59,96 млн ₽**
- Остаток cash к концу M12: около **0,04 млн ₽**

**Runway ≈ 12 месяцев по плану**, но практически без запаса. Для комфортного прохода к breakeven проекту нужен капитал скорее **80-90 млн ₽+**, иначе риск кассового разрыва слишком высок.

## 14. Проверка profit gate фонда

### Проверка at 50 clients
- Revenue: **10,5 млн ₽/мес**
- Gross profit: **7,68 млн ₽/мес**
- Fixed costs: **7,31 млн ₽/мес**
- EBITDA: около **+0,36 млн ₽/мес** до дополнительных нестабильных расходов, и **ниже 500 тыс. ₽/мес** на нормализованной базе.

### Итог
**Profit Gate = FAIL.** Причина не в слабом LTV/CAC, а в том, что **при 50 клиентах компания всё ещё не создаёт требуемую EBITDA-подушку фонда**. Для столь узкой категории это плохой риск/доходность профиль.

## 15. Инвестиционный вывод

Conveyor-подобный продукт в РФ может продаваться как нишевой enterprise tool и даже давать достойный LTV/CAC на единичной сделке. Но на уровне фонда это **слишком узкая и капиталоёмкая история**:
- buyer universe ограничен;
- цикл продажи длинный и дорогой;
- нужен сильный solutions-heavy delivery;
- fixed cost база высокая;
- требуемая прибыльность достигается слишком поздно.

**Решение P5: REJECTED.**

## Sources
- **T1. OptiMine / SaaS churn benchmark summary**: https://www.optiminemodern.com/post/average-churn-rates-for-saas-companies
- **T2. Dream Job / hh.ru salary benchmark pages**: https://dreamjob.ru/salaries/programmist?experience=moreThan6Years , https://dreamjob.ru/salaries/devops-inzhener?experience=moreThan6Years , https://dreamjob.ru/salaries/menedzher-po-prodazham?experience=moreThan6Years
- **T3. Conveyor official site / pricing / docs**: https://www.conveyor.com/pricing , https://docs.conveyor.com/docs/what-is-questionnaire-automation
- **T4. Analyst inference based on RU enterprise SaaS GTM cost structure and ranges given in mandate**
