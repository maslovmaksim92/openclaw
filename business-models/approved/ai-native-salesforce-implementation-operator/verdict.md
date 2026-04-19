# AI-native Salesforce Implementation Operator
**Статус:** APPROVED
**Итоговый балл:** 70/100
**Дата:** 2026-04-19
**Сектор:** GEO-EXPAND

---

## Этап 1 — Описание кейса

### Источник и суть идеи
Сервисная модель: AI-native оператор внедрения Salesforce Agentforce и Industry Cloud, который продаёт более быстрое и результативное enterprise implementation за счёт собственного agentic delivery engine.

### Текущее состояние гипотезы
На входе был ранний сигнал: ReDEFY позиционирует себя как applied AI Salesforce partner с упором на Agentforce, Industry Cloud и собственный implementation engine. Гипотеза состояла в том, что внутри установленной Salesforce-базы можно собрать repeatable service business, если подтвердятся спрос на ускоренное внедрение, стандартизируемый workflow и экономика лучше классического SI.

---

## Этап 2 — Проверка спроса

Спрос оценён как **MEDIUM+**, Profit Gate как **PASS**. Mandatory multi-demand endpoint был недоступен по технической причине, но глобальный спрос подтвердили независимые сигналы.

### Основные подтверждения спроса
- Salesforce публично сообщала о **1 000+ paid deals Agentforce** на Dreamforce 2024 и о **5 000+ paid deals** и **8 200+ total deals** по итогам FY25 Q4.
- Salesforce указывает на базу **150 000+ компаний**.
- Партнёрская экосистема Salesforce для Agentforce и Industry Cloud подтверждает, что implementation budget встроен в категорию с самого начала.

### Конкуренты и willingness to pay
- **Simplus**: 12 383-16 427 ₽/час, minimum project size от 825 500 ₽.
- **MagicFuse**: 4 128-8 172 ₽/час, minimum project size от 2,06 млн ₽.
- **Peeklogic**: 4 128-8 172 ₽/час, minimum project size от 825 500 ₽.

WTP подтверждён: enterprise buyer уже платит 4-16 тыс. ₽ за час Salesforce implementation, а минимальные проекты начинаются от 825 500 ₽.

### TAM / SAM / SOM
- **TAM:** 180 млрд ₽/год.
- **SAM:** 30 млрд ₽/год.
- **SOM:** 270 млн ₽/год.

### Ключевой вывод demand-этапа
Кейс не тянет на HIGH из-за слабого локального рынка РФ и недоступности mandatory API, но глобальный спрос и willingness to pay достаточны для продолжения анализа.

---

## Этап 3 — Юнит-экономика

### Бизнес-процесс
| № | Шаг | Кто | Инструмент | Время | Стоимость |
|---|---|---|---|---|---:|
| 1 | Сбор ICP-аккаунтов и enrichment | SDR / Growth | LinkedIn Sales Navigator, Apollo-подобный стек, CRM | 3 ч | 7 500 ₽ |
| 2 | Первичный outbound | SDR | E-mail sequencer, LinkedIn, CRM | 5 ч | 14 000 ₽ |
| 3 | Qualification call | AE / Founder | Zoom/Meet, CRM, AI call notes | 1,5 ч | 9 000 ₽ |
| 4 | Discovery | AE + Solutions Architect | Discovery template, Notion, CRM | 3 ч | 24 000 ₽ |
| 5 | Solution design | Solutions Architect | Miro, solution template, Salesforce sandbox docs | 6 ч | 42 000 ₽ |
| 6 | Pilot scoping | Architect + Salesforce Engineer | Demo org, backlog template, ROI calculator | 8 ч | 56 000 ₽ |
| 7 | SoW и pricing | AE + Founder + Finance | CPQ, spreadsheet, deck | 4 ч | 28 000 ₽ |
| 8 | Security / procurement / legal review | Founder + Architect + Legal Ops | NDA/SOW/MSA templates, ЭДО | 6 ч | 41 000 ₽ |
| 9 | Контрактинг и billing | Finance Ops + AE | 1С, ЭДО, CRM, billing | 3 ч | 19 000 ₽ |
| 10 | Kickoff и первый платёж | Delivery Lead + Finance Ops | Jira, Slack/Teams, billing, checklist | 4 ч | 27 000 ₽ |

Direct deal-process cost на 1 выигранного клиента: **267 500 ₽**.

### Unit economics
- **ARPA:** 1 200 000 ₽/мес.
- **COGS:** 465 000 ₽/мес.
- **Gross Margin:** 61,3%.
- **contribution_margin_rub_month:** 636 000 ₽/мес.
- **CAC:** 1 320 000 ₽.
- **customer_ltv_rub:** 35 333 333 ₽.
- **LTV/CAC:** 26,8x.
- **CAC Payback:** 2,1 месяца.
- **Break-even:** 4 клиента / 4-й месяц.
- **startup_capital_to_bep_rub:** 2 550 000 ₽.

### Profit Gate
Компания проходит порог фонда: EBITDA >500K ₽/мес достигается при 4 клиентах, а при 50 клиентах теоретическая EBITDA значительно выше порога.

---

## Этап 4 — Финансовая модель и критика

### P&L, базовый сценарий
- Месяц 1: MRR 1 200 000 ₽, EBITDA -1 585 000 ₽.
- Месяц 4: MRR 4 800 000 ₽, EBITDA 620 000 ₽.
- Месяц 12: MRR 9 600 000 ₽, EBITDA 3 560 000 ₽.

### Оптимистичный сценарий
Месяц 12: **13 клиентов, MRR 16 380 000 ₽, EBITDA 7 965 000 ₽**.

### Пессимистичный сценарий
Месяц 12: **5 клиентов, MRR 5 400 000 ₽, EBITDA 650 000 ₽**. Break-even сдвигается к 8-му месяцу.

### Денежный поток
- Минимальный стартовый капитал до break-even: **2,55 млн ₽**.
- Рекомендованный капитал с 20% резервом: **3,06 млн ₽**.

### Stress-тесты
- **CAC x2:** LTV/CAC падает до 13,4x, payback до 4,15 месяца.
- **Churn x2:** customer_ltv_rub падает до 17,7 млн ₽.
- **Price -30%:** contribution_margin_rub_month падает до 276 000 ₽/мес, break-even ухудшается до 9 клиентов, EBITDA месяца 12 снижается до 680 000 ₽.

### Главные риски
1. Delivery уходит в кастомный SI, COGS растёт выше плана.
2. Price compression разрушает premium ARPA.
3. Partner/referral channel Salesforce не открывается в нужном масштабе.

---

## Этап 5 — Финальный вердикт

### Score breakdown
| Критерий | Балл | Макс |
|---|---:|---:|
| Реальный спрос | 14 | 20 |
| Прибыль компании / Unit Economics | 22 | 25 |
| Масштабируемость | 12 | 20 |
| Конкурентное позиционирование | 8 | 15 |
| Барьеры входа | 6 | 10 |
| Качество данных | 8 | 10 |
| **Итого** | **70** | **100** |

### Ключевые метрики для инвесткомитета
- **CAC:** 1 320 000 ₽
- **customer_ltv_rub:** 35 333 333 ₽
- **LTV/CAC:** 26,8x
- **Payback:** 2,1 месяца
- **GM:** 61,3%
- **Break-even:** 4 клиента / 4-й месяц
- **company_ebitda_potential_rub_month:** 3 560 000 ₽/мес в базовом сценарии на месяце 12
- **500K EBITDA:** 4 клиента / месяц 4
- **1M EBITDA:** 5 клиентов / месяц 5

### Почему кейс approved
1. Порог фонда по EBITDA выполняется очень рано и с небольшим стартовым капиталом.
2. Unit economics кратно выше минимального investment-grade уровня.
3. Глобальный enterprise WTP подтверждён vendor traction и реальными конкурентными ценами.

### Что доказать до запуска
1. Минимум 3 partner/referral agreements и 30% SQL из канала.
2. COGS на клиента не выше 550 000 ₽/мес при 5+ клиентах.
3. Не менее 40% implementation-клиентов переходят в recurring managed retainer за 6 месяцев.

---

## Этап 6 — История прохождения пайплайна

### 2026-04-19 — Program 4: Demand Validation
- Статус: completed
- Demand score: MEDIUM+
- Profit Gate: PASS
- Вывод: глобальный спрос подтверждён, рынок РФ слабый.

### 2026-04-19 — Program 5: Unit Economics
- Статус: completed
- Economics score: 23/25
- Вывод: сильная экономика service-enabled operator при стандартизированном delivery.

### 2026-04-19 — Program 6: Financial Model + Critic
- Статус: completed
- Critic score: 17/25
- Вывод: кейс интересный, но чувствительный к pricing power, partner access и service creep.

### 2026-04-19 — Program 7 / Critic and verdict
- Статус: APPROVED
- Итоговый балл: 70/100
- Разбивка: спрос 14/20, экономика 22/25, масштаб 12/20, конкуренция 8/15, защита 6/10, данные 8/10
- LTV/CAC: 26,8x | CAC Payback: 2,1 месяца | Break-even: месяц 4 / 4 клиента
- Стартовый капитал до BEP: 2 550 000 ₽
- Причина: экономика проходит порог фонда с запасом, но защита бизнеса средняя и требует доказательства на практике.
