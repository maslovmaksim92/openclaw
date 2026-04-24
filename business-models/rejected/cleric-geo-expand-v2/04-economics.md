---
stage: economics
case: cleric-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P5: REJECTED.**

Почему:
1. Для РФ это не SMB SaaS, а тяжёлый enterprise / regulated-like sale с пилотом, security review и solution engineering.
2. При реалистичном fully-loaded CAC модель даёт **LTV/CAC = 1.5x**, что ниже инвестиционного порога **3.0x**.
3. **CAC Payback = 16.5 мес**, это формально терпимо для enterprise, но слишком долго для раннего GEO-EXPAND motion при узком ICP и сильном incumbent pressure.
4. Break-even достигается только примерно на **37 платящих клиентах**, а burn до этого момента выглядит слишком тяжёлым для нового входа в РФ.

## 1. Базовые допущения модели

- ICP: крупные банки, маркетплейсы, телеком, travel-tech, large SaaS с постоянным on-call.
- Средний контракт: **350 000 ₽/мес на клиента**.
- Это ниже верхней границы из demand-stage и ближе к реалистичному входному чеку для первого локального пилота с последующим rollout.
- Gross Margin считаю после инфраструктуры, support, solution engineering и customer success.
- Churn беру **2.0% в месяц** как консервативный enterprise benchmark для узкого B2B SaaS / infrastructure software сегмента. Для зрелых enterprise SaaS возможен churn ниже, но для GEO-EXPAND в новой категории и при высокой замещаемости платформами это слишком оптимистично. [T4]

## 2. Unit economics per client / month

### COGS breakdown per client / month

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / orchestration | 55 000 | inference + agent orchestration для расследований | высокая нагрузка при разборе инцидентов |
| Cloud / storage / VPC isolation | 22 000 | выделенная облачная среда и хранение operational memory | enterprise buyer часто требует изоляцию |
| Integrations maintenance | 18 000 | поддержка Datadog / Prometheus / K8s / Slack коннекторов | не fully self-serve |
| Solution engineer allocation | 42 000 | доля pre/post-sales engineer на активного клиента | onboarding + tuning |
| Support / incident coverage | 18 000 | L2/L3 support и customer success allocation | high-touch модель |
| Security / compliance / DevOps allocation | 12 000 | hardening, audit trail, доступы | для enterprise deployment |
| **Итого COGS** | **167 000** |  |  |

- **Выручка на клиента в месяц:** 350 000 ₽
- **Валовая прибыль на клиента:** 183 000 ₽
- **Gross Margin:** **52.3%**
- **Contribution Margin:** **52.3%**

Вывод: для AI SRE в РФ это уже не software-like 75-85% GM, а тяжёлая high-touch инфраструктурная поставка.

## 3. Business process from lead to payment

### Детальная таблица процесса

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR | HH.ru, Rusprofile, LinkedIn/Sales Navigator analog, CRM | 2 ч | 3 500 | средняя |
| 2 | Обогащение контактов CTO / Head of Infra / SRE Lead | SDR | CRM, enrichment tools | 1.5 ч | 2 600 | средняя |
| 3 | Персонализированный outbound / intro outreach | SDR | email sequencing, Telegram, LinkedIn | 3 ч | 5 200 | средняя |
| 4 | Первичный ответ и qualification | SDR | CRM, календарь, email | 1 ч | 1 700 | средняя |
| 5 | Discovery call | AE + founder | Zoom / Meet, CRM | 1.5 ч | 9 500 | низкая |
| 6 | Demo с разбором инцидента | AE + Solutions Engineer | demo env, observability sandbox | 2 ч | 14 500 | низкая |
| 7 | Solution fit / security scoping | CTO + Solutions Engineer | архитектурные схемы, questionnaire | 4 ч | 29 000 | низкая |
| 8 | Pilot proposal / commercial offer | AE + founder | CRM, proposal tool | 2 ч | 11 500 | средняя |
| 9 | Пилот 6-8 недель | Solutions Engineer + CSM + buyer team | product, cloud, Slack, observability stack | 40 ч | 180 000 | низкая |
| 10 | Procurement + InfoSec + legal review | AE + founder + legal | договоры, security docs, DPA | 10 ч | 62 000 | низкая |
| 11 | Закрытие сделки и invoice | AE + finance | ЭДО, CRM, billing | 1 ч | 4 500 | высокая |
| 12 | Onboarding и первый платёж | CSM + DevOps | product, support desk, billing | 6 ч | 31 000 | средняя |

**Вывод:** у сделки слишком много ручных касаний. Это не self-serve и даже не mid-market inside sales. Отсюда высокий CAC и длинный payback.

## 4. CAC by acquisition channel with funnel conversion

### Funnel assumptions

| Канал | Target accounts / contacts | Ответ / intro | Discovery | Pilot | New paying customers | Конверсия contact→paid |
|---|---:|---:|---:|---:|---:|---:|
| Founder network / warm intros | 12 | 8 | 6 | 3 | 0.30 | 2.5% |
| Outbound enterprise | 250 | 45 | 18 | 6 | 0.45 | 0.18% |
| Events / partners | 30 meetings | 18 | 10 | 4 | 0.15 | 0.50% |
| **Итого blended / мес** | 292 | 71 | 34 | 13 | **0.90** | **0.31%** |

### CAC по каналам

| Канал | Затраты, ₽/мес | New paying customers / мес | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Founder network / warm | 550 000 | 0.30 | 1 833 333 | самый дешёвый канал, но не масштабируется |
| Outbound enterprise | 1 450 000 | 0.45 | 3 222 222 | требует SDR + AE + SE |
| Events / partners | 660 000 | 0.15 | 4 400 000 | дорогой, волатильный канал |
| **Blended raw CAC** | **2 660 000** | **0.90** | **2 955 556** | без поправки на enterprise complexity |

### Fully-loaded CAC

#### Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 120 000 | ретаргет + brand defense + точечный ABM traffic | T2/T5 + model |
| Outbound team FOT (SDR + AE + SE attributed to new) | 1 183 000 | SDR 234k + AE 494k + 50% Solutions 455k | T5 + model |
| Marketing team FOT (partial allocation) | 160 000 | 40% founder/marketing time на acquisition | model |
| Tools (CRM, sequencing, enrichment, demo) | 95 000 | CRM + email stack + enrichment + call tools | model |
| Events / partnerships | 260 000 | 1 event / month + partner activities | model |
| Overhead multiplier (x1.3) | 545 400 | 30% на G&A / management / admin load | std enterprise B2B |
| **Raw fully-loaded acquisition spend / мес** | **2 363 400** |  |  |

- **Raw fully-loaded CAC = 2 363 400 / 0.90 = 2 625 999 ₽**
- Для данного сегмента применяю **enterprise multiplier x2.2**, потому что ACV высокий, есть 2-3 sales calls, пилот, security review, legal и procurement.
- **Enterprise-adjusted fully-loaded CAC = 2 625 999 × 2.2 = 5 777 198 ₽**

### Sanity check vs RU benchmarks

- Enterprise SaaS B2B в РФ: **300-900K ₽ / клиент** для complex sales.
- Healthtech / regulated B2B: **400-1200K ₽ / клиент**.
- Для Cleric-подобного AI SRE кейса фактический CAC выше benchmark, потому что buyer очень узкий, sale почти всегда идёт через пилот и solution engineering, а category education высокий.
- Это не ошибка вычислений, а сигнал, что локальный GTM слишком тяжёлый.

## 5. LTV with churn rate

### Churn benchmark

- Для B2B SaaS monthly revenue churn на enterprise сегменте обычно существенно ниже SMB, но для ранней GEO-EXPAND модели и категории с сильным platform substitution реалистично брать **1.5-2.5% monthly churn** как рабочий диапазон. [T4]
- В модели беру **2.0% monthly churn**.

### LTV calculation

Формула:

`LTV = MRR per customer × Gross Margin / Monthly Churn`

Подстановка:

- MRR per customer = **350 000 ₽**
- Gross Margin = **52.3%**
- Monthly churn = **2.0%**

`LTV = 350 000 × 0.523 / 0.02 = 9 152 500 ₽`

**LTV ≈ 9.15 млн ₽**

## 6. LTV / CAC ratio

- **LTV = 9.15 млн ₽**
- **Fully-loaded CAC = 5.78 млн ₽**

`LTV/CAC = 9.15 / 5.78 = 1.58x`

### Интерпретация

- Инвестиционный порог: **>= 3.0x**
- Нейтральная зона: **2.0-3.0x**
- Reject zone: **< 2.0x**

**Факт: 1.58x, это reject.**

## 7. CAC payback

Формула:

`CAC Payback = CAC / MRR per customer`

`5 777 198 / 350 000 = 16.5 мес`

- **CAC Payback = 16.5 месяцев**
- Для enterprise это ещё не катастрофа, но для нового GEO-EXPAND входа в РФ при узком ICP и слабом category demand это слишком долго.

## 8. Team & FOT

### Полная таблица команды

| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|---:|---:|
| CEO / Founder | продажи, fundraising, enterprise closing | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, roadmap | 1 | 600 000 | 2.5 | 2 | 180 000 | 780 000 |
| Senior Backend | connectors, orchestration, backend | 2 | 450 000 | 1.5 | 1.5 | 135 000 | 585 000 each |
| ML Engineer | agents, inference quality, evals | 1 | 550 000 | 2.5 | 2 | 165 000 | 715 000 |
| DevOps | deployment, infra, observability | 1 | 380 000 | 1.5 | 1 | 114 000 | 494 000 |
| SDR | outbound prospecting | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| Account Executive | enterprise sales + closing | 1 | 380 000 | 1.5 | 2.5 | 114 000 | 494 000 |
| Customer Success | onboarding, adoption, renewal | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product / Solutions Engineer | pilot setup, demo, technical fit | 1 | 350 000 | 2 | 1.5 | 105 000 | 455 000 |
| Finance / Ops | invoicing, документооборот, admin | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| **Итого steady-state team** |  | **10** |  |  |  |  | **5 746 000 ₽/мес** |

### Salary realism

- Senior / Lead engineering compensation находится внутри коридора HH benchmark для Москвы/СПб. [T5]
- SDR/AE compensation тоже внутри типового диапазона. [T5]
- Для enterprise AI infra кейса план менее 5 млн ₽ loaded FOT в steady-state был бы занижением.

### Cumulative FOT timeline M1-M12

| Месяц | Подключение команды | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO | 845 000 |
| M3 | CEO + CTO | 1 625 000 |
| M4 | + Backend #1 | 2 210 000 |
| M5 | + Backend #2 + DevOps | 3 289 000 |
| M6 | + ML Engineer | 4 004 000 |
| M7 | + Product / Solutions Engineer | 4 459 000 |
| M8 | + SDR | 4 693 000 |
| M9 | + AE | 5 187 000 |
| M10 | + Customer Success | 5 512 000 |
| M11 | + Finance / Ops | 5 746 000 |
| M12 | steady-state | 5 746 000 |

Вывод: быстрый старт командой 5-7 человек в первый месяц был бы нереалистичен. Нормальный hire plan сам по себе съедает темп выхода в рынок.

## 9. Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT steady-state | 5 746 000 | из таблицы выше |
| Core cloud / internal infra | 420 000 | dev / staging / monitoring / security tooling |
| Legal, accounting, admin | 180 000 | договоры, бухгалтерия, юрподдержка |
| Travel / events baseline | 250 000 | поездки, встречи, small events |
| Rent / coworking / workplace | 120 000 | гибридная команда |
| G&A software / licenses | 160 000 | Notion, GitHub, CRM, security, finance stack |
| **Итого fixed costs / мес** | **6 876 000 ₽** |  |

## 10. Break-even

### Break-even by client count

Формула:

`Break-even clients = Fixed costs / Contribution profit per client`

`6 876 000 / 183 000 = 37.57`

**Нужно 38 клиентов для месячного break-even.**

### Break-even by month

При рабочем ramp-сценарии:
- M6: 1 клиент
- M7: 2
- M8: 4
- M9: 6
- M10: 9
- M11: 12
- M12: 15
- далее +3 клиента/мес

38 клиентов достигаются только примерно к **M20**.

### Break-even revenue

- **MRR на break-even:** `38 × 350 000 = 13.3 млн ₽/мес`
- **Contribution profit на break-even:** `38 × 183 000 = 6.95 млн ₽/мес`

## 11. Burn-to-breakeven and runway

### Burn-to-breakeven

Упрощённо:
- Средний burn в M1-M6: около **3.4 млн ₽/мес**
- Средний burn в M7-M12: около **5.3 млн ₽/мес** после учёта первых клиентов
- К моменту вероятного break-even в M20 суммарный cash burn получается порядка **75-85 млн ₽**

### Cash runway

Если взять **startup capital = 40 млн ₽**:

- при burn **~4.8 млн ₽/мес** средняя runway = **8.3 месяца**

Если взять **startup capital = 60 млн ₽**:

- runway = **12.5 месяца**

Вывод: чтобы дожить до break-even, реалистично нужен капитал ближе к **80+ млн ₽**, что для локального GEO-EXPAND wedge выглядит слишком тяжёлым.

## 12. Profit gate

### Проверка инвестиционной состоятельности

- EBITDA > 500K ₽/мес при 50 клиентах: **да, достижимо**
- LTV/CAC >= 3.0x: **нет**
- CAC Payback < 18 мес для enterprise: **формально да**
- Повторяемость канала привлечения: **нет, слабая**

### Итоговый вывод

Кейс **не инвестиционного качества** на уровне фонда, потому что:
1. юнит-экономика держится только на длинном и дорогом enterprise sale;
2. gross margin слишком низкий для AI infra software;
3. blended fully-loaded CAC слишком высокий относительно LTV;
4. break-even наступает слишком поздно и требует непропорционально большого капитала.

## Verdict

**P5 verdict: REJECTED.**

Причина reject, **LTV/CAC = 1.58x**, что заметно ниже инвестиционного порога **3.0x**. Даже при том, что теоретически EBITDA > 500K ₽/мес достижима на масштабе, для фонда это слишком тяжёлый и капиталоёмкий GEO-EXPAND motion.

## Sources

- Cleric launch / product positioning: https://cleric.ai/ [T1]
- Cleric product page: https://cleric.ai/product [T1]
- Datadog Bits AI SRE: https://www.datadoghq.com/product/ai/bits-ai-sre/ [T2]
- Datadog press release, 2025-12-02: https://www.datadoghq.com/about/latest-news/press-releases/datadog-launches-bits-ai-sre-agent-to-resolve-incidents-faster/ [T2]
- OptiMine / Optifai B2B SaaS churn benchmarks: https://www.optiminemetrics.com/blog/saas-churn-benchmarks [T4]
- HH.ru salary trends / job market / vacancies: https://hh.ru/article/301127 [T5]
- HH.ru salary service: https://salary.hh.ru/ [T5]
- HH.ru vacancies search: https://hh.ru/search/vacancy [T5]

Где использованы model assumptions:
- локальный ACV 350K ₽/мес;
- COGS allocation по enterprise deployment;
- channel mix и funnel conversions;
- event/tool spend;
- enterprise complexity multiplier x2.2.
