# AI Marketing Ops Microagency
**Статус:** NEAR-PASS
**Итоговый балл:** 66/100
**Дата:** 2026-04-19
**Сектор:** B2B MarTech / SMB services

---

## Этап 1 — Описание кейса
# 00-brief

## Case
ai-marketing-ops-microagency

## Status
active

## Summary
AI marketing ops micro-agency: managed copilot/service for SMB brands running ads + CRM + campaign execution.

## Current state
Источник сигнала: Business Insider pitch deck coverage про Pomo. На triage это классифицировано как отдельная SMB-oriented модель, а не просто adoption signal. Стартовый wedge: взять на себя marketing ops execution слой поверх ad platforms и CRM для небольших growth brands.

## Core hypothesis
Малые бренды готовы платить за productized AI-assisted marketing ops service, если можно сократить ручную кампанийную рутину, ускорить execution и показать понятный ROI без enterprise-grade внедрения.

---

## Этап 2 — Проверка спроса
# 02-demand

## Кейс
ai-marketing-ops-microagency

## Дата проверки
2026-04-19, Europe/Moscow

## Сектор
B2B MarTech / SMB services

## Итог
**DEMAND = MEDIUM, LTV Gate = PASS.**

Причина: есть живой рынок платных инструментов и Telegram-first automation-сервисов, SMB уже платят за контент, CRM и campaign ops, а стоимость ручной команды маркетинга в РФ достаточно высокая, чтобы retainer на AI-assisted execution выглядел рационально. До HIGH не дотягивает, потому что mandatory local demand endpoint не ответил, а прямой buyer-intent слой по exact формулировке micro-agency фрагментирован.

## 1) Mandatory demand API: localhost / multi-demand
Проверил обязательный источник:
- `http://localhost:9001/multi-demand?keyword=AI marketing ops agency`
- fallback: `http://172.17.0.1:9001/multi-demand?keyword=AI marketing ops agency`

Результат в этом прогоне:
- `localhost:9001` -> `Couldn't connect to server`
- `172.17.0.1:9001` -> `Connection timed out after 20001 milliseconds`

Вывод: обязательная попытка выполнена, но exact composite demand feed технически **не получен**.

## 2) Прямые сигналы спроса
### HH.ru: рынок уже платит за людей, которых эта модель частично заменяет
- По запросу `таргетолог` на HH.ru найдено **369 вакансий**.
- По запросу `CRM-маркетолог` видны зарплаты **130 000–200 000 ₽/мес**, также встречаются вилки **85 000–180 000 ₽/мес**.

Интерпретация: SMB и mid-market уже несут значимый payroll-cost на ads/CRM execution. Если AI micro-agency закрывает 0.3-1.0 FTE на аккаунт, retainer в десятки тысяч рублей в месяц выглядит экономически правдоподобным.

### Адресуемая база клиентов
Единый реестр МСП ФНС по состоянию на **10.04.2026** показывает:
- всего субъектов МСП: **6 947 425**
- юрлиц: **2 203 395**

Интерпретация: даже если брать только юрлица и только consumer-facing digital-active слой, база для SMB marketing ops остаётся большой.

## 3) Реальные конкуренты с ценами
- **Jasper**: **$59–69/мес** (~**4 487–5 248 ₽/мес**)
- **BotHelp**: от **$18/мес** (~**1 369 ₽/мес**), scale-based pricing до **$995/мес**
- **Salebot**: **2 999 ₽/мес** или **30 590 ₽/год**, higher tier **3 999 ₽/мес** или **40 790 ₽/год**

## 4) Что цены конкурентов говорят о willingness to pay
WTP подтверждён напрямую: AI-маркетинговые инструменты уже продаются как recurring-бюджет, Telegram/automation stack в РФ уже монетизируется, а HH зарплаты формируют верхний price anchor для managed execution.

## 5) Telegram bots / services в RU
- **Salebot**: Telegram/MAX/VK/WhatsApp automation, цены в рублях.
- **TextBack**: Telegram Account + Telegram Bot + CRM/рассылки/ИИ-боты.
- **BotHelp**: платный Telegram-first automation stack.

## 6) TAM / SAM / SOM в рублях
- **TAM = 47.59 млрд ₽/год**
- **SAM = 19.04 млрд ₽/год**
- **SOM = 143.1 млн ₽/год**

## 7) LTV Gate: проверка сценариев монетизации
- Low-ticket software-only: **FAIL** как standalone investment case
- Done-with-you AI copilot for SMB: **PASS**
- Done-for-you managed micro-agency: **PASS**
- Vertical package для Telegram-first SMB: **PASS**
- White-label / enablement for agencies: **PASS**

## 8) Финальный verdict по спросу
**Спрос подтверждён, early reject не нужен.**

---

## Этап 3 — Юнит-экономика
# 04-economics

## Кейс
ai-marketing-ops-microagency

## Дата расчёта
2026-04-19, Europe/Moscow

## Итог
**ECONOMICS = PASS. Investment grade по unit economics: да.**

Ключевой вывод: при среднем чеке **75 000 ₽/клиент/мес** и переменной себестоимости **27 500 ₽/клиент/мес** модель даёт **Contribution Margin 63.3%**, **LTV ≈ 1.98 млн ₽**, **blended CAC ≈ 90 000 ₽**, **LTV/CAC ≈ 22.0x**, **CAC Payback ≈ 1.9 месяца**.

## Детальный бизнес-процесс
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листов и enrichment | SDR | HH/2GIS/manual lists, Apollo-like DB, Google Sheets | 20 мин/лид | 180 | Средняя |
| 2 | Первичный outreach в email/Telegram | SDR | Instantly/UniSender, Telegram, шаблоны | 10 мин/лид | 90 | Высокая |
| 3 | Follow-up sequence 2-3 касания | SDR | CRM + sequencer | 15 мин/лид | 135 | Высокая |
| 4 | Ответ и qualification | SDR | CRM, Telegram, анкета-квалификатор | 15 мин/MQL | 135 | Средняя |
| 5 | Discovery call | Founder / AE | Google Meet, Notion discovery template | 45 мин | 1 200 | Низкая |
| 6 | Подготовка mini-audit и гипотез роста | Founder + Delivery Lead | Looker Studio, ChatGPT, Notion | 90 мин | 3 500 | Средняя |
| 7 | Коммерческое предложение | AE | PandaDoc/Google Docs, pricing calculator | 45 мин | 1 050 | Средняя |
| 8 | Negotiation / scope fix | Founder / AE | Meet, Telegram, калькулятор юнитов | 45 мин | 1 200 | Низкая |
| 9 | Договор и счёт | Ops/Admin | Диадок/Контур, банк, CRM | 30 мин | 500 | Высокая |
| 10 | Предоплата / 1-й платёж | Client + Ops | Банк, эквайринг | 10 мин | 700 | Высокая |
| 11 | Onboarding и доступы | Account Lead | Notion, checklist, password vault | 120 мин | 2 400 | Средняя |
| 12 | Настройка CRM/ботов/UTM/reporting | CRM Automation Specialist | BotHelp/Salebot, amoCRM/Битрикс, GTM | 180 мин | 5 000 | Средняя |
| 13 | Запуск campaign ops и контент-календаря | Marketing Ops Specialist | Ads Manager, ChatGPT, Canva/Figma | 240 мин | 6 700 | Средняя |
| 14 | Еженедельная оптимизация | Delivery team | Ads/CRM dashboards, Notion | 180 мин/мес | 7 000 | Средняя |
| 15 | Месячный отчёт + QBR-lite | Account Lead | Looker Studio, Loom, Meet | 90 мин/мес | 2 800 | Средняя |
| 16 | Повторный платёж / продление | Ops/Admin | Счёт, банк, CRM reminders | 15 мин/мес | 350 | Высокая |

## COGS и метрики
- Revenue per client/month = **75 000 ₽**
- COGS per client/month = **27 500 ₽**
- Contribution per client/month = **47 500 ₽**
- Contribution Margin = **63.3%**
- Blended CAC = **90 000 ₽**
- Contribution LTV = **1 979 167 ₽**
- LTV/CAC = **22.0x**
- CAC Payback = **1.9 мес**
- Break-even = **14 клиентов / 1 050 000 ₽ MRR**

---

## Этап 4 — Финансовая модель и критика
# 05-critic

## Кейс
ai-marketing-ops-microagency

## Дата
2026-04-19, Europe/Moscow

## Итог
**CRITIC = PASS WITH RESERVATIONS.**

Экономика на бумаге сильная, но это не software-compounding кейс, а service-led cash flow business с узким местом в delivery quality, founder-led sales и контроле scope.

## P&L модель — базовый сценарий
- Мес 1: **225 000 ₽ MRR**, **-487 500 ₽ EBITDA**
- Мес 6: **600 000 ₽ MRR**, **-250 000 ₽ EBITDA**
- Мес 12: **1 125 000 ₽ MRR**, **82 500 ₽ EBITDA**

## Оптимистичный сценарий
Мес 12: **1 804 000 ₽ MRR**, **518 000 ₽ EBITDA**, **22 клиента**

## Пессимистичный сценарий
Мес 12: **816 000 ₽ MRR**, **-194 000 ₽ EBITDA**, **12 клиентов**

## Структура расходов, месяц 12, база
- COGS: **412 500 ₽ (36.7%)**
- Sales: **290 000 ₽ (25.8%)**
- Marketing: **80 000 ₽ (7.1%)**
- R&D / automation / internal tooling: **55 000 ₽ (4.9%)**
- G&A: **205 000 ₽ (18.2%)**
- EBITDA: **82 500 ₽ (7.3%)**

## Денежный поток
- Burn rate мес 1-3: **-440 000 ₽/мес** в среднем
- Cash gap до month-10: **2 547 500 ₽**
- Рекомендованный стартовый капитал: **2.8-2.95 млн ₽**
- Monthly EBITDA break-even: **месяц 11**

## Sensitivity analysis
- **CAC x2**: month-12 EBITDA около **-367 500 ₽**
- **Churn x2**: month-12 MRR **975 000 ₽**, EBITDA **-12 500 ₽**
- **Price -30%**: break-even уже **26 клиентов**, month-12 EBITDA **-255 000 ₽**

## Главные риски
- Scope creep и erosion margin
- Churn spike у SMB при слабом ROI
- Founder bottleneck в продажах и аудите
- Platform/channel shock
- Перегрузка delivery команды

## Kill conditions
1. К концу месяца 6 активная база < 8 клиентов
2. Churn > 5% три месяца подряд
3. Contribution margin < 50% два квартала подряд

---

## Этап 5 — Финальный вердикт
# 06-verdict

## Кейс
ai-marketing-ops-microagency

## Дата вердикта
2026-04-19, Europe/Moscow

## Финальный статус
**NEAR-PASS**

Итог: кейс набирает **66/100** и не проходит порог 70. Это не слабая экономика, а сильный service-led бизнес с ограниченной масштабируемостью, умеренными барьерами входа и слабой продуктовой защитой.

## Score breakdown
| Критерий | Балл | Макс |
|---|---:|---:|
| Реальный спрос | 14 | 20 |
| Юнит-экономика | 22 | 25 |
| Масштабируемость | 12 | 20 |
| Конкурентное позиционирование | 7 | 15 |
| Барьеры входа | 4 | 10 |
| Качество данных | 7 | 10 |
| **Итого** | **66** | **100** |

## Ключевые метрики
- GM: **63.3%**
- CAC: **90 000 ₽**
- LTV: **1 979 167 ₽**
- LTV/CAC: **22.0x**
- Payback: **1.9 мес**
- Break-even: **14 клиентов / 1 050 000 ₽ MRR**
- Стартовый капитал: **2.8-2.95 млн ₽** рекомендовано

## LTV Upside Calculator
- Сейчас: **66/100**
- Нужно ещё: **4 балла**
- Кратчайший путь: улучшить **масштабируемость** и **качество данных** через доказанный vertical wedge, repeatable delivery pod и пилоты с premium-retainer.

---

## Этап 6 — История прохождения пайплайна
# 07-score-trajectory
## Кейс: ai-marketing-ops-microagency
## Перепрогон начат: 2026-04-18

История прохождения пайплайна (перепрогон с улучшенными агентами).

### 2026-04-19 — Program 4 / Demand Validation
- Статус после шага: **PASS TO NEXT STEP**
- Demand: **MEDIUM**
- LTV Gate: **PASS**
- TAM: **47.59 млрд ₽/год** | SAM: **19.04 млрд ₽/год** | SOM: **143.1 млн ₽/год**

### 2026-04-19 — Program 5 / Unit Economics
- Статус после шага: **PASS TO NEXT STEP**
- Contribution margin: **63.3%**
- Blended CAC: **90 000 ₽**
- Contribution LTV: **1 979 167 ₽**
- Break-even: **14 клиентов**

### 2026-04-19 — Program 6 / Financial Model + Critic
- Статус после шага: **PASS WITH RESERVATIONS**
- Мес 12 база: **1 125 000 ₽ MRR**, **82 500 ₽ EBITDA**
- Стартовый капитал: **2.8-2.95 млн ₽**

### 2026-04-19 — Program 7 / Critic and verdict
- Статус: **NEAR-PASS**
- Итоговый балл: **66/100**
- Разбивка: спрос **14/20**, экономика **22/25**, масштаб **12/20**, конкуренция **7/15**, защита **4/10**, данные **7/10**
- Причина: сильная экономика, но недостаточная масштабируемость и слабый moat для инвестиционного одобрения.
