---
stage: economics
case: 2216-msk-supio-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECT
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Supio GEO Expand: AI-платформа для plaintiff-side personal injury и mass tort law firms, разбор меддокументов, chronology, demand drafting и litigation workflow.

## Executive summary
**Итог: REJECT.**

Причина отказа не в отсутствии global category proof, а в слабой инвестиционной экономике для локального запуска. Для РФ/СНГ это enterprise legal-tech с длинным циклом продаж, дорогим presale, дорогим внедрением, слабым локальным спросом и узким ICP. В base-case модель даёт:

- **MRR на клиента:** 180 000 ₽/мес
- **COGS:** 86 400 ₽/клиент/мес
- **Contribution Margin:** 52.0%
- **Blended fully-loaded CAC:** 3 400 000 ₽
- **Churn:** 3.0% в месяц
- **LTV:** 3 120 000 ₽
- **LTV/CAC:** **0.92x**
- **CAC Payback:** **18.9 мес**
- **Break-even:** **50 клиентов** или **9.0 млн ₽ MRR/мес**
- **EBITDA при 50 клиентах:** около **+80 000 ₽/мес**, то есть Profit Gate не проходит даже на 50 клиентах

Следовательно, кейс неинвестируемый по двум обязательным условиям сразу:
1. **LTV/CAC < 1:1**
2. **Компания не достигает EBITDA 500 000 ₽/мес даже при 50 клиентах**

---

## 1. Базовые допущения модели

### ICP
- Крупные litigation boutiques, страховые споры, медико-правовые споры, отдельные крупные юрфирмы.
- Продажа идёт как **enterprise legal workflow**, а не self-serve SaaS.
- Сделка требует демо, security/legal review, пилот, ручную настройку workflow и customer success.

### Pricing assumption
Беру **180 000 ₽/мес** на клиента как реалистичный локальный чек после дисконта к американскому value capture.

Почему не 250 000-400 000 ₽/мес:
- спрос локально не доказан;
- category education ложится на вендора;
- buyer не привык к отдельному PI-legal AI stack;
- продажа идёт через пилот и скидку за раннее внедрение.

### Gross margin assumption
Беру **52% Contribution Margin** как base-case для early enterprise legal AI в локальном запуске.

Это ниже SaaS-нормы, потому что есть:
- ручной onboarding;
- project-like внедрение;
- частичная human QA;
- дорогая inference/storage/retrieval-инфраструктура;
- customer success с заметной долей кастомной поддержки.

---

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Поиск ICP и сбор аккаунт-листа | SDR | HH/2ГИС/СПАРК/ручной ресерч | 2.0 ч | 2 500 | низкая |
| 2 | Обогащение контактов партнёров/управляющих | SDR | CRM + ручной ресерч | 1.5 ч | 1 900 | низкая |
| 3 | Первый outbound/email/звонок | SDR | CRM, телефония, email | 1.0 ч | 1 300 | средняя |
| 4 | Follow-up 3-5 касаний | SDR | CRM sequences | 2.0 ч | 2 500 | средняя |
| 5 | Квалификация боли и ICP-fit | AE | Zoom/Meet + CRM | 1.0 ч | 3 300 | низкая |
| 6 | Discovery-call | AE + founder | Zoom, презентация | 1.5 ч | 7 000 | низкая |
| 7 | Сбор sample documents / use-case mapping | AE + solution lead | Notion/Drive | 3.0 ч | 10 500 | низкая |
| 8 | Демо на данных клиента | Solution engineer + AE | demo env, LLM stack | 4.0 ч | 14 000 | средняя |
| 9 | Security/legal review | Founder + tech lead | docs, DPA, checklists | 5.0 ч | 18 000 | низкая |
| 10 | Пилот 2-4 недели | CSM + solution engineer | sandbox, support, QA | 18.0 ч | 63 000 | средняя |
| 11 | Переговоры, закупка, договор | AE + founder | CRM, docs | 4.0 ч | 17 000 | низкая |
| 12 | Онбординг и настройка шаблонов | CSM + solution engineer | workspace, prompt/config | 8.0 ч | 28 000 | средняя |
| 13 | Первый production month | CSM + support | helpdesk, analytics | 6.0 ч | 17 500 | средняя |
| 14 | Выставление счёта и получение оплаты | Finance ops | банк, ЭДО | 0.5 ч | 1 000 | высокая |

### Вывод
Продажа и запуск здесь не похожи на дешёвый SaaS. Это **consultative sale + pilot-heavy deployment**, поэтому CAC должен считаться fully-loaded, а не только по рекламным расходам.

---

## 3. COGS на клиента в месяц

### COGS breakdown per client/month
| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / embeddings | 18 000 | usage-based estimate | анализ документов и RAG |
| Хранение, векторная БД, бэкапы | 7 000 | infra allocation | документы и индексы |
| Human QA / legal ops review | 22 000 | 0.12 FTE ops | ранняя стадия, высокий риск ошибок |
| Customer success / support | 16 000 | 0.08 FTE CSM | onboarding + регулярные вопросы |
| Solution engineering / template maintenance | 12 000 | shared allocation | настройка workflow |
| Инфра/security/compliance allocation | 11 400 | shared allocation | logging, access control, audit |
| **Итого COGS** | **86 400** |  |  |

### Unit contribution
- **Revenue / клиент / мес:** 180 000 ₽
- **COGS / клиент / мес:** 86 400 ₽
- **Contribution / клиент / мес:** 93 600 ₽
- **Contribution Margin:** **52.0%**

---

## 4. CAC по каналам и воронка

### Воронка по каналам
| Канал | Лидов/мес | SQL | Pilot | New paying | Lead→Paying | CAC raw, ₽ | CAC fully-loaded, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led network | 12 | 6 | 2 | 0.5 | 4.2% | 1 120 000 | 2 240 000 |
| Outbound ABM | 180 | 18 | 4 | 0.8 | 0.44% | 1 420 000 | 3 550 000 |
| Партнёрства / events | 25 | 5 | 1.5 | 0.3 | 1.2% | 1 600 000 | 4 000 000 |
| **Blended** | **217** | **29** | **7.5** | **1.6** | **0.74%** | **1 360 000** | **3 400 000** |

### Fully-loaded CAC, обязательный расчёт
Формула:

`Fully-loaded CAC = (Direct marketing + attributed sales FOT + attributed marketing FOT + tools + events + overhead multiplier) / new paying customers`

#### Таблица компонентов fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | узкий legal B2B demand gen, тестовый бюджет | допущение модели, T1-T3 sanity |
| Outbound team FOT (SDR/AE attributed to new) | 1 560 000 | SDR 180k + AE 350k + 30% взносы + бонус/комиссия + founder support allocation | HH.ru benchmark, T4-T6 |
| Marketing team FOT (partial allocation) | 260 000 | 0.5 FTE product marketing / content / events | модель, T4-T6 |
| Tools (CRM, телефония, enrichment, docs) | 210 000 | CRM + телефония + data tools + workspace | модель, enterprise B2B stack |
| Events / partnerships | 450 000 | 1 нишевое событие + поездки + партнёрские активности | модель, low-volume B2B |
| Subtotal raw CAC pool | 2 600 000 | сумма выше |  |
| Overhead multiplier | 1 300 000 | **x1.5** к raw, т.к. mid-market/enterprise B2B legal sale с длинным cycle | standing order sanity + enterprise B2B assumption |
| **Итого monthly CAC pool** | **3 900 000** | 2.6m + 1.3m |  |
| New paying customers / мес | **1.15** | консервативный blended close rate | воронка выше |
| **Blended fully-loaded CAC** | **3 400 000** | 3.9m / 1.15 | итог |

### Sanity check по industry benchmark
Для enterprise SaaS B2B в РФ ориентир из standing order: **300-900k ₽/клиент**, для сложных regulated/vertical workflows выше. Для legal AI с пилотом, document intelligence и длинным закупочным циклом **3.4 млн ₽** выглядит очень высоким, но не абсурдным, потому что category education почти полностью лежит на вендоре, а поток новых клиентов крайне мал.

---

## 5. LTV и churn

### Churn assumption
Беру **3.0% monthly logo churn**.

Почему так высоко для enterprise:
- локальный PMF не подтверждён;
- buyer может взять пилот и не масштабировать;
- продукт заточен под американский plaintiff workflow;
- для РФ велики риски замены на ручной труд + generic LLM + шаблоны.

### Benchmark source
По SaaS Capital lower churn характерен для более крупных/enterprise SaaS, а более маленькие и ранние компании показывают заметно более высокий churn. Для этого кейса уместен не best-in-class benchmark, а penalized benchmark из-за слабого local fit.

### LTV calculation
Формула:

`LTV = MRR × Contribution Margin / Monthly Churn`

Подставляем:
- MRR = 180 000 ₽
- CM = 52%
- Churn = 3.0%

**LTV = 180 000 × 0.52 / 0.03 = 3 120 000 ₽**

---

## 6. LTV/CAC, CAC Payback, Contribution Margin

| Метрика | Формула | Значение |
|---|---|---:|
| LTV | 180 000 × 0.52 / 0.03 | 3 120 000 ₽ |
| Blended fully-loaded CAC | см. расчёт выше | 3 400 000 ₽ |
| **LTV/CAC** | 3 120 000 / 3 400 000 | **0.92x** |
| **CAC Payback** | 3 400 000 / 180 000 | **18.9 мес** |
| **Contribution Margin** | (180 000 - 86 400) / 180 000 | **52.0%** |

### Вывод по investability
- **LTV/CAC 0.92x < 1.0x** → жёсткий FAIL
- **Payback 18.9 мес** → хуже базового порога 12 мес и на грани даже для тяжёлого enterprise
- **CM 52%** → недостаточно высок для компенсации длинного CAC cycle

---

## 7. Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи, fundraising, key accounts | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | архитектура, delivery, security | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion, API, integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | workflow engine, data layer | 420 000 | 126 000 | 546 000 |
| ML Engineer | extraction / RAG / evals | 500 000 | 150 000 | 650 000 |
| DevOps | infra, observability, security | 350 000 | 105 000 | 455 000 |
| Frontend | user workspace | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | demos, pilot, closing | 350 000 | 105 000 | 455 000 |
| Customer Success | onboarding, retention | 260 000 | 78 000 | 338 000 |
| Finance / Ops (0.5 FTE) | docs, billing, vendor ops | 120 000 | 36 000 | 156 000 |
| **Итого** |  |  |  | **5 265 000 ₽/мес** |

### Таблица найма с hiring realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 + бонус | 1 | 1 | 54 000 | 234 000 |
| AE | 1 | 350 000 + комиссия | 1.5 | 3 | 105 000 | 455 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |

### Salary benchmark note
Диапазоны выше согласованы с московскими/СПб HH benchmark-диапазонами для Team Lead, Senior SWE, ML, DevOps, SDR и AE; для legal AI берётся верхняя половина диапазона из-за niche premium.

---

## 8. Cumulative FOT timeline M1-M12

С учётом realistic time-to-hire нельзя посадить всю команду в M1. План ниже deliberately conservative.

| Месяц | Кто уже в команде | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 780 000 |
| M2 | CEO + Frontend + Backend#1 | 1 716 000 |
| M3 | M2 + SDR + DevOps | 2 405 000 |
| M4 | M3 + CTO + AE | 3 575 000 |
| M5 | M4 + Backend#2 + CSM | 4 459 000 |
| M6 | M5 + ML Engineer | 5 109 000 |
| M7 | полная core team + 0.5 Finance/Ops | 5 265 000 |
| M8 | без изменений | 5 265 000 |
| M9 | без изменений | 5 265 000 |
| M10 | без изменений | 5 265 000 |
| M11 | без изменений | 5 265 000 |
| M12 | без изменений | 5 265 000 |

### Комментарий
Даже этот план уже тяжёлый. Если пытаться нанять 5+ человек в первый месяц, это будет red flag против hiring realism.

---

## 9. Fixed costs breakdown

Для break-even считаю не полный FOT 5.265m, а operating fixed costs после частичной оптимизации и founder-underpay в стартовой фазе.

| Статья fixed cost | ₽/мес |
|---|---:|
| Team FOT cash-paid | 3 650 000 |
| Office / legal / accounting | 180 000 |
| Core infra not in COGS | 220 000 |
| Security / audit / compliance | 160 000 |
| G&A / travel / misc | 140 000 |
| Product / content / brand | 250 000 |
| **Итого fixed costs** | **4 600 000 ₽/мес** |

---

## 10. Break-even

### Break-even by client count
Формула:

`Break-even clients = Fixed costs / Contribution per client`

Подставляем:
- Fixed costs = 4 600 000 ₽
- Contribution per client = 93 600 ₽/мес

**Break-even = 4 600 000 / 93 600 = 49.15 → 50 клиентов**

### Break-even by month
Формула MRR at BE:

`MRR_break-even = Fixed costs / Contribution Margin`

**MRR_break-even = 4 600 000 / 0.52 = 8 846 154 ₽/мес**

Округляю до **9.0 млн ₽ MRR/мес**.

### Profit Gate check at 50 clients
- Revenue at 50 clients = 50 × 180 000 = **9 000 000 ₽/мес**
- Contribution = 9 000 000 × 52% = **4 680 000 ₽/мес**
- EBITDA = 4 680 000 - 4 600 000 = **+80 000 ₽/мес**

**До требуемых 500 000 ₽/мес EBITDA не дотягивает. Profit Gate FAIL.**

---

## 11. Burn-to-breakeven и cash runway

### План выручки для base-case
Из-за длинного enterprise cycle предполагаю медленный ramp:
- M1-M6: 0 клиентов
- M7: 1 клиент
- M8: 2
- M9: 4
- M10: 6
- M11: 8
- M12: 10

Даже к M12:
- Revenue = 10 × 180 000 = **1 800 000 ₽/мес**
- Contribution = **936 000 ₽/мес**
- Это сильно ниже fixed costs 4.6m ₽/мес.

### Burn-to-breakeven
Если суммировать FOT + infra + acquisition до выхода на 50 клиентов, потребуется примерно **65-75 млн ₽** cumulative burn, причём сам break-even уходит далеко за пределы первого года.

### Cash runway
Беру **startup_capital = 36 млн ₽**.

При среднем burn первых 12 месяцев около **4.8-5.2 млн ₽/мес**, runway составляет:

`36 000 000 / 5 000 000 ≈ 7.2 месяца`

**Cash runway: около 7 месяцев**, то есть компания заканчивает деньги существенно раньше реалистичного break-even.

### Sanity checks
- startup_capital_to_bep заметно выше 10 млн ₽ → да, и это реалистично для enterprise B2B AI
- FOT для 5-7 человек >1 млн ₽/мес → да, underestimation нет
- пайплайн найма не нарушает time-to-hire → да

---

## 12. Why economics fail

1. **Узкий ICP**, почти нет входящего спроса.
2. **Длинный sales cycle**: demo, pilot, legal/security review.
3. **Дорогой пресейл** на каждый логотип.
4. **Высокий churn risk** из-за слабой локальной переносимости американского plaintiff workflow.
5. **Низкий объём рынка** делает масштабирование до 50 клиентов малореалистичным.
6. **COGS не SaaS-like**: много human QA и solution engineering.

---

## 13. Финальный вывод

### Investment decision
**REJECT**

### Обязательные метрики
- **LTV/CAC = 0.92x** → ниже даже 1:1
- **CAC Payback = 18.9 мес** → слишком долго
- **Contribution Margin = 52.0%** → посредственно для такого CAC
- **EBITDA при 50 клиентах = +80k ₽/мес** → ниже порога 500k ₽/мес

### Итог
Кейс не проходит investment-grade unit economics. Для фонда это не просто weak case, а **структурно плохая локальная экономика**.

---

## Источники
- T1. Supio Series B press release, 2025-04-30: https://www.supio.com/press/supio-announces-60m-series-b-to-accelerate-adoption-of-legal-ai-in-plaintiff-law
- T2. Supio homepage: https://www.supio.com/
- T3. Supio AI Demand Letter: https://www.supio.com/products/ai-demand-letter
- T4. HeadHunter, зарплата Team Lead в Москве, 2026: https://stats.hh.ru/moscow/salary/it_specialist/Teamlead
- T5. HeadHunter, зарплата программиста в Москве, 2026: https://stats.hh.ru/moscow/salary/it_specialist/programmista
- T6. HeadHunter, зарплата менеджера по продажам в Москве, 2026: https://stats.hh.ru/moscow/salary/menedzher_po_prodazham
- T7. SaaS Capital, What is a Good Annual Churn Rate for SaaS?: https://www.saascapital.com/blog-posts/what-is-a-good-annual-churn-rate-for-saas/
- T8. 02-demand.md кейса, локальный спрос и TAM/SAM/SOM допущения
