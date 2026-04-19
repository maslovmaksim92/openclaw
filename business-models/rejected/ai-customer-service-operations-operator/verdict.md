# AI Customer Service Operations Operator
**Статус:** REJECTED
**Итоговый балл:** 64/100
**Дата:** 2026-04-18
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
- каналы: email, чат, Telegram, WhatsApp, helpdesk;
- buyer: Head of Support, COO, CX Director;
- оффер: внедрение AI-first support operations + постоянный managed optimization слой.
- ARPA: **180 000 ₽/мес**

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

### CAC, COGS, LTV и break-even
- CAC: **780 000 ₽**
- COGS: **112 000 ₽/клиент/мес**
- Маржа с клиента: **68 000 ₽/мес**
- Contribution Margin: **37,8%**
- Churn benchmark: **1,8%/мес**
- LTV: **3 780 000 ₽**
- LTV/CAC: **4,85x**
- CAC Payback: **11,5 месяца**
- Break-even: **28 активных клиентов, примерно М13**

### Команда и fixed costs
- ФОТ: **1 490 000 ₽/мес**
- Fixed costs: **1 850 000 ₽/мес**
- Формально economics проходят, но сервисная нагрузка остаётся высокой.

---

## Этап 4 — Финансовая модель и критика
# 05-critic

## Дата
2026-04-18 (Europe/Moscow)

## Вердикт Program 6
**FAIL**

### Базовый сценарий, 12 месяцев
- М12: **25 активных клиентов**
- MRR: **4 499 165 ₽**
- COGS: **2 799 481 ₽**
- Gross Profit: **1 699 684 ₽**
- Fixed Costs: **1 850 000 ₽**
- EBITDA: **-150 316 ₽**
- Operating BEP: примерно **М13** при **27,5-28 клиентах**

### Оптимистичный сценарий
- М12: **33,78 клиента**
- MRR: **6 587 293 ₽**
- EBITDA: **988 946 ₽**
- Break-even: **М9**

### Пессимистичный сценарий
- М12: **15,89 клиента**
- MRR: **2 621 937 ₽**
- EBITDA: **-1 053 145 ₽**

### Структура расходов на М12, базовый сценарий
- COGS: **2 799 481 ₽ (62,2% MRR)**
- Sales: **750 000 ₽ (16,7%)**
- Marketing: **220 000 ₽ (4,9%)**
- R&D: **430 000 ₽ (9,6%)**
- G&A: **450 000 ₽ (10,0%)**
- EBITDA margin: **-3,3%**

### Денежный поток и капитал
- Burn rate мес 1-3 fully-loaded: **2,43-2,56 млн ₽/мес**
- Operating capital до EBITDA break-even: **~12,9 млн ₽**
- Fully-loaded capital до BEP с CAC: **~36,3 млн ₽**

### Sensitivity analysis
- **CAC x2:** LTV/CAC = **2,42x**, payback = **22,9 месяца**
- **Churn x2:** LTV = **1 890 000 ₽**, M12 EBITDA = **-273 779 ₽**
- **Цена -30%:** contribution margin = **11,1%**, LTV/CAC = **1,00x**, break-even = **133 клиента**

### Глубокий critic-вывод
Главный стоп-фактор в том, что категория уже занята helpdesk incumbents и AI-native vendors. Модель может быть рабочей как бутик-оператор, но пока не выглядит как фондово-сильный compounder.

---

## Этап 5 — Финальный вердикт
# 06-verdict

## Финальный статус
**REJECTED**

## Итоговый балл
**64/100**

### Score breakdown
| Критерий | Балл | Макс | Почему |
|---|---:|---:|---|
| Реальный спрос | 13 | 20 | MEDIUM, без сильного exact спроса по категории в РФ. |
| Юнит-экономика | 19 | 25 | Экономика рабочая, но GM 37,8% слишком низкая для сильного compounding. |
| Масштабируемость | 11 | 20 | Delivery остаётся service-led. |
| Конкурентное позиционирование | 8 | 15 | Zendesk, Intercom и AI-native вендоры атакуют этот wedge. |
| Барьеры входа | 5 | 10 | Нет сильного moat. |
| Качество данных | 8 | 10 | Большинство ключевых цифр подтверждены, но спрос по exact-категории недожат. |

### Ключевые метрики
- CAC: **780 000 ₽**
- LTV: **3 780 000 ₽**
- LTV/CAC: **4,85x**
- CAC Payback: **11,5 месяца**
- GM: **37,8%**
- Break-even: **М13 / 28 активных клиентов**
- Стартовый капитал до BEP: **~36,3 млн ₽**

### Топ-3 риска
1. **CAC уходит выше плана**: вероятность 55%, impact 900 000 ₽/мес.
2. **Discounting платформами**: вероятность 45%, impact 1 350 000 ₽/мес.
3. **Платформенный риск Zendesk/Intercom**: вероятность 30%, impact 1 100 000 ₽/мес.

### LTV Upside Calculator
- Сейчас: **64/100**
- До порога 70: **+6 баллов**
- Усилить спрос exact-category в РФ: **+4**
- Снизить ручной delivery и поднять масштабируемость: **+3**
- Доказать вертикальный moat и lock-in: **+2-4**

---

## Этап 6 — История прохождения пайплайна
# 07-score-trajectory
## Кейс: ai-customer-service-operations-operator
## Перепрогон начат: 2026-04-18

### 2026-04-18 — Demand Validation
- Demand verdict: **MEDIUM**
- LTV gate: **PASS**
- Decision: **допущен в Program 5**

### 2026-04-18 — Unit Economics
- Economics verdict: **PASS**
- CAC: **780 000 ₽**
- LTV: **3 780 000 ₽**
- LTV/CAC: **4,85x**
- CAC Payback: **11,5 месяца**
- Break-even: **28 активных клиентов, примерно М13**

### 2026-04-18 — Financial Model + Critic
- Critic verdict: **FAIL**
- Base Month-12 MRR: **4 499 165 ₽**
- Base Month-12 EBITDA: **-150 316 ₽**
- Fully-loaded capital to BEP: **~36,3 млн ₽**

### 2026-04-18 — Программа 7 / Critic and verdict
- Статус: **REJECTED**
- Итоговый балл: **64/100**
- Разбивка: **13/20, 19/25, 11/20, 8/15, 5/10, 8/10**
- Причина: **экономика рабочая, но модель слишком капиталоёмкая и слабо защищена от платформ.**
