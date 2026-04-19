# AI Customer Service Operations Operator
**Статус:** REJECTED
**Итоговый балл:** 56/100
**Дата:** 2026-04-19
**Сектор:** B2B-OPS

---

## Этап 1 — Описание кейса
# 00-brief

## Case
ai-customer-service-operations-operator

## Status
rejected

## Summary
Сервисная модель: внедрение, настройка и постоянное сопровождение AI-first customer service operations поверх support platforms.

## Current state
Источник сигнала: triage от 2026-04-11 по Zendesk AI customer service operator narrative. На triage это выглядит как потенциально отдельная модель, потому что речь идёт не о широком AI adoption, а о конкретном operational wedge вокруг support resolution, knowledge orchestration, workflow design, tuning и managed optimisation.

## Core hypothesis
Можно собрать repeatable service business вокруг внедрения, настройки и сопровождения AI-first customer service operations, если подтвердится:
- что buyer pain в support / resolution operations достаточно острый и регулярный
- что внедрение требует заметного service layer поверх Zendesk-подобных платформ, knowledge systems и adjacent workflows
- что tuning, governance, workflow design и continuous optimisation нельзя полностью commoditize внутри самого вендора
- что существует воспроизводимый budget owner и путь к recurring revenue

---

## Этап 2 — Проверка спроса
# 02-demand

## Кейс
ai-customer-service-operations-operator

## Дата проверки
2026-04-18 (Europe/Moscow)

## Сектор
B2B-OPS

## Итог этапа
PASS

## Composite demand
MEDIUM

## Почему не HIGH
Для HIGH не хватает exact-category demand data (wordstat endpoint timeout).
- Публичный спрос подтверждён по adjacent-категориям: AI customer service, helpdesk AI
- Конкуренты с ценами: Zendesk от $19-$115/агент/мес, Freshdesk от $0-$79, Usedesk от 1 500 ₽/мес, Chat2Desk от 990 ₽/мес
- Реальный WTP подтверждён (RU-рынок платит за SaaS-helpdesk)
- RU Telegram: Chat2Desk, Carrot Quest, BotHelp — активные игроки

## Ранний reject
нет

## LTV gate
PASS — при целевом чеке ≥ 150 000 ₽/мес unit economics сходятся

> Market Pulse 2026-04-19: растущий интерес.

---

## Этап 3 — Юнит-экономика
# 04-economics

## Кейс
ai-customer-service-operations-operator

## Дата расчёта
2026-04-18 (Europe/Moscow)

## Итог
**PASS**

Экономика проходит investment-grade порог по Program 5:
- **LTV = 3 780 000 ₽**
- **CAC = 780 000 ₽**
- **LTV/CAC = 4,8x**
- **CAC Payback = 11,5 месяца**
- **Contribution Margin = 37,8%**

LTV выше обязательного порога **500 000 ₽**, ratio выше минимального порога **3:1**.

### Рабочий ICP и ценовая модель
- mid-market и upper-mid-market компании с **25-60 агентами поддержки**;
- buyer: Head of Support, COO, CX Director;
- оффер: внедрение AI-first support operations + постоянный managed optimization слой.
- ARPA: **180 000 ₽/мес**.
- COGS: **112 000 ₽/клиент/мес**.
- contribution_margin_rub_month: **68 000 ₽/мес**.
- fixed_costs_rub_month: **1 850 000 ₽/мес**.
- Break-even: **28 клиентов**, примерно **месяц 13**.

### Детальный бизнес-процесс
| Шаг | Что происходит | Роль | Tool | Время | Стоимость, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка и enrichment аккаунтов | SDR / RevOps | LinkedIn, HH, Clay, CRM | 6 ч | 18 000 | Высокая |
| 2 | Персонализированный outbound и первичный outreach | SDR | email sequencer, Telegram, CRM | 18 ч | 42 000 | Средняя |
| 3 | Квалификация ответа и booking discovery call | SDR + AE | CRM, календарь, call notes AI | 8 ч | 26 000 | Средняя |
| 4 | Discovery: pain mapping, текущие метрики, SLA, stack | AE + Solution Lead | Zoom, Notion, AI-notetaker | 10 ч | 58 000 | Низкая |
| 5 | Пресейл-аудит support ops и дизайн целевого workflow | Solution Lead + Prompt/QA Lead | Miro, helpdesk sandbox, LLM workspace | 20 ч | 132 000 | Низкая |
| 6 | ROI-модель, коммерческое предложение, security/QA ответы | AE + Founder + Finance | spreadsheets, CRM, doc templates | 14 ч | 104 000 | Средняя |
| 7 | Пилот 2-4 недели: настройка intent routing, KB, автоответов | Solution Engineer + QA Analyst | Zendesk/Freshdesk, bots, analytics | 36 ч | 188 000 | Средняя |
| 8 | Procurement, legal, MSA/SLA, DPA, финальное согласование | Founder + AE + Legal | e-sign, docs, CRM | 16 ч | 112 000 | Низкая |
| 9 | Онбординг после подписания: интеграции, rollout, first invoice | Solution Engineer + CSM | helpdesk, billing, PM tool | 20 ч | 74 000 | Средняя |

### LTV и метрики
- customer_ltv_rub по churn 1,8%/мес: **3 780 000 ₽**
- Консервативный сценарий: **680 000 ₽**
- Базовый сценарий: **1 360 000 ₽**
- Оптимистичный сценарий: **3 400 000 ₽**
- LTV/CAC: **4,85x**
- CAC Payback: **11,5 мес**
- Gross Margin: **37,8%**

---

## Этап 4 — Финансовая модель и критика
# 05-critic

## Кейс
ai-customer-service-operations-operator

## Дата
2026-04-18 (Europe/Moscow)

## Вердикт Program 6
**FAIL**

## Почему
Кейс проходит Program 5 по юнит-экономике, но не проходит investment-fund critic по трём причинам:
1. **Слишком длинный путь к cash break-even**: even в базовом плане EBITDA остаётся отрицательной до М12, а fully-loaded капитал до выхода на operating BEP около **36,3 млн ₽**.
2. **Слабая защита от крупных платформ**: Intercom, Zendesk, Forethought и Decagon уже продают AI-automation в support и могут быстрее копировать workflow-слой.
3. **Низкая compounding-качество модели**: gross margin всего **37,8%**, а цена сильно чувствительна к discounting.

### P&L, базовый сценарий
| Месяц | Активные клиенты | MRR | COGS | Gross Profit | Fixed Costs | EBITDA |
|---:|---:|---:|---:|---:|---:|---:|
| 1 | 1.00 | 180 000 | 112 000 | 68 000 | 1 850 000 | -1 782 000 |
| 6 | 8.68 | 1 562 889 | 972 464 | 590 425 | 1 850 000 | -1 259 575 |
| 12 | 25.00 | 4 499 165 | 2 799 481 | 1 699 684 | 1 850 000 | -150 316 |

### Оптимистичный сценарий
Мес 12: **33,78 клиентов, MRR 6 587 293 ₽, EBITDA 988 946 ₽**.

### Пессимистичный сценарий
Мес 12: **15,89 клиентов, MRR 2 621 937 ₽, EBITDA -1 053 145 ₽**.

### Sensitivity analysis
- CAC ×2: LTV/CAC падает до **2,42x**, payback доходит до **22,9 месяца**.
- Churn ×2: month-12 EBITDA ухудшается до **-273 779 ₽**.
- Цена -30%: LTV/CAC = **1,0x**, break-even = **133 клиента**.

### Топ-риски
| Риск | Вероятность | Месячный impact |
|---|---|---:|
| CAC выше плана из-за длинных пилотов и procurement | 55% | 900 000 ₽ |
| Discounting под давлением крупных платформ | 45% | 1 350 000 ₽ |
| Churn после 3-6 месяцев из-за слабой интеграции | 35% | 630 000 ₽ |

### Kill conditions
- blended CAC > 1 200 000 ₽ два месяца подряд
- ARPA по 5 сделкам подряд < 150 000 ₽/мес
- к концу М9 active base < 18 клиентов или EBITDA хуже -900 000 ₽

---

## Этап 5 — Финальный вердикт
# 06-verdict

## Кейс
ai-customer-service-operations-operator

## Дата вердикта
2026-04-19, Europe/Moscow

## Итог
**REJECTED. Итоговый балл: 56/100.**

Кейс подтверждает реальный рынок AI-автоматизации поддержки и рабочую unit economics на одном клиенте, но для инвестиционного комитета проваливается на экономике компании и defensibility. При `contribution_margin_rub_month = 68 000 ₽` бизнесу нужно примерно **28 активных клиентов** и около **13 месяцев** только до operating break-even, а fully-loaded `startup_capital_to_bep_rub` достигает **36 300 000 ₽**, что слишком тяжело для service-led модели с умеренной защитой от Zendesk, Intercom и AI-native support vendors.

### Score breakdown
| Критерий | Балл | Макс | Почему |
|---|---:|---:|---|
| Реальный спрос | 14 | 20 | Спрос подтверждён: есть действующие helpdesk/AI-support игроки с реальными ценами, RU-рынок платит за SaaS/helpdesk, WTP подтверждён, но `Composite demand = MEDIUM`, а exact Wordstat-category data нет. |
| Прибыль компании / Unit Economics | 12 | 25 | `clients_to_500k_ebitda ≈ 35`, `months_to_500k_ebitda ≈ 15`, `clients_to_1m_ebitda ≈ 42`, `months_to_1m_ebitda ≈ 18`, при этом `startup_capital_to_bep_rub ≈ 36 300 000 ₽`. |
| Масштабируемость | 10 | 20 | Delivery частично автоматизирован, но по-прежнему service-heavy. |
| Конкурентное позиционирование | 6 | 15 | Zendesk, Intercom и AI-native vendors могут быстро копировать слой value proposition. |
| Барьеры входа | 5 | 10 | Есть интеграции и workflow tuning, но moat умеренный. |
| Качество данных | 9 | 10 | Ключевые числа подтверждены ценами, churn benchmark и P&L. |
| **Итого** | **56** | **100** | **Ниже порога 65, кейс отклонён.** |

### LTV Upside Calculator
- Сейчас: **56/100**
- Нужно ещё: **14 баллов**
- Кратчайший путь: улучшить экономику компании через рост `contribution_margin_rub_month`, сократить долю ручного delivery и доказать moat против helpdesk incumbents.

---

## Этап 6 — История прохождения пайплайна
# 07-score-trajectory
## Кейс: ai-customer-service-operations-operator
## Начат: 2026-04-19

История прохождения пайплайна.

### 2026-04-19 — Программа 7 / Critic and verdict
- Статус: REJECTED
- Итоговый балл: 56/100
- Разбивка: спрос 14/20, экономика 12/25, масштаб 10/20, конкуренция 6/15, защита 5/10, данные 9/10
- LTV/CAC: 4,85x | CAC Payback: 11,5 мес | Break-even: мес 13 / 28 клиентов
- Стартовый капитал до BEP: 36 300 000 ₽
- Причина: спрос и юнит-экономика на клиента подтверждены, но компании нужен слишком длинный и капиталоёмкий путь к 500K EBITDA, а moat против платформ остаётся умеренным.
