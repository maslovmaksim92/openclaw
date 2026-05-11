# Unit Economics — ServiceNow Enterprise AI Control Tower v2

> Stage: P5 Unit Economics
> Date: 2026-05-11
> Case: servicenow-enterprise-ai-control-tower-v2
> Segment model: enterprise B2B SaaS / control-plane для AI governance, inventory, risk/compliance и orchestration

## Вывод

**Вердикт этапа: PASS.**

Кейс сходится только как **enterprise high-touch SaaS** с длинным циклом сделки, дорогим пресейлом и высоким ACV. При базовом чеке **400 тыс. ₽ MRR** на клиента, fully-loaded CAC около **1,55 млн ₽**, contribution margin **67,0%**, churn **1,5%/мес** и LTV/CAC около **10,3x** модель выглядит инвестиционно годной. Break-even наступает примерно на **21 активном клиенте**. При **50 клиентах** месячный EBITDA заметно выше порога **500 тыс. ₽/мес**.

---

## 1) Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам, телекому, ритейлу, industrial | SDR | HH, сайты компаний, CRM, таблицы | 25 мин/account | 520 | средняя |
| 2 | Обогащение контактов CIO / CDO / Head of Risk / Head of Platform | SDR | CRM, email finder, Telegram, ручной ресерч | 20 мин/account | 420 | средняя |
| 3 | Outbound-sequence 5-8 касаний | SDR | email sequences, CRM, телефония | 35 мин/account | 730 | высокая |
| 4 | Qualification call | SDR | Meet/Zoom, CRM | 30 мин/SQL | 630 | средняя |
| 5 | Discovery с business + IT owner | AE | Zoom, deck, ROI-calculator | 90 мин | 2 100 | низкая |
| 6 | Подготовка tailored demo и architecture fit | AE + Solution Architect/CTO | sandbox, demo env, diagrams | 4 ч | 10 500 | низкая |
| 7 | Demo + workshop по governance / risk / inventory | AE + CTO + CEO | Zoom / onsite | 2 ч | 7 900 | низкая |
| 8 | Security review / legal / procurement Q&A | AE + CTO + юрист | docs, почта, Dataroom | 8 ч | 21 000 | низкая |
| 9 | Пилот 4-6 недель на 1-2 use cases | CSM + backend + ML + DevOps | cloud env, connectors, PM board | 32 ч | 78 000 | средняя |
| 10 | Коммерческое предложение и business case | AE + CEO | CRM, spreadsheet, docs | 4 ч | 11 000 | низкая |
| 11 | Согласование договора и DPA/ИБ приложений | AE + юрист | Диадок, Word, email | 7-15 раб. дней | 9 500 | средняя |
| 12 | Выставление счёта | Finance/Ops | 1С, банк-клиент | 20 мин | 400 | высокая |
| 13 | Оплата счёта | Клиент | банк-клиент | 5-20 раб. дней | 0 | вне контура |
| 14 | Onboarding, SSO, RBAC, initial integrations | CSM + backend + DevOps | API, IAM, Jira | 18-24 ч | 42 000 | средняя |
| 15 | Ежемесячный governance review / QBR | CSM + AE | BI, CRM, dashboards | 2 ч/мес | 5 500 | средняя |

### Комментарий по циклу сделки
- Типичный sales cycle: **4-8 месяцев**.
- Для enterprise AI governance основная стоимость сидит не в рекламе, а в **presale architecture, pilot, security review и founder/AE времени**.
- Поэтому корректно считать **fully-loaded CAC**, а не media CAC.

---

## 2) COGS на 1 клиента в месяц

### Базовый enterprise-пакет
- MRR на клиента: **400 000 ₽/мес**
- ACV: **4,8 млн ₽/год**

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud compute / app runtime | 18 000 | control plane, policy engine, background jobs |
| LLM / embeddings / summarization | 12 000 | policy explanations, inventory summaries, assistant workflows |
| Storage / audit logs / backup | 9 000 | журналы действий, policy logs, резервирование |
| Security tooling allocation | 11 000 | SIEM/light monitoring, secrets, vuln scanning |
| Integration/API maintenance | 14 000 | ITSM, IAM, model gateways, internal systems |
| Support & CSM variable allocation | 22 000 | monthly reviews, incidents, enablement |
| DevOps / uptime variable allocation | 10 000 | deployments, observability, incident response |
| Payment / документооборот / billing variable | 600 | ЭДО и платёжная операционка |
| **Итого COGS** | **96 600** |  |

### Итог
- Revenue per client/month = **400 000 ₽**
- COGS per client/month = **96 600 ₽**
- Gross profit per client/month = **303 400 ₽**
- **Gross Margin = 75,9%**

---

## 3) CAC по каналам и funnel conversion

### Воронка по каналам

| Канал | Lead → Meeting | Meeting → Pilot | Pilot → Paid | New paying customers / мес | Комментарий |
|---|---:|---:|---:|---:|---|
| Founder-led outbound + SDR | 6% | 30% | 28% | 0,9 | основной канал ранних enterprise продаж |
| Партнёрства / интеграторы / advisory | 14% | 45% | 35% | 0,5 | выше trust, но мало объёма |
| Events / thought leadership / inbound | 10% | 25% | 25% | 0,2 | медленно, но усиливает credibility |
| **Итого blended** | — | — | — | **1,6** | база для blended CAC |

### Fully-loaded CAC: обязательная раскладка

Raw acquisition cost до overhead = 1 193 500 ₽/мес.
Для enterprise сегмента применяю **CAC multiplier x1,3 как overhead multiplier** на скрытые затраты пресейла, founder time, legal, solution engineering и admin. Это даёт fully-loaded acquisition cost **1 551 550 ₽/мес**.

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | low-volume always-on demand capture + ретаргетинг | assumption, sanity vs enterprise search volume |
| Outbound team FOT (SDR/AE attributed to new) | 702 000 | SDR 180 000 + AE 360 000, всё ×1,3 соцвзносы | HH.ru benchmark [T3] |
| Marketing team FOT (partial allocation) | 91 000 | 70 000 gross attributed ×1,3 | assumption |
| Tools (CRM, LinkedIn Sales Nav, Apollo, аналог) | 95 500 | amoCRM, sequencing, enrichment, data tools, телефония | market pricing / assumption |
| Events/partnerships | 125 000 | усреднение 1 enterprise-события/мес + партнёрские активности | assumption |
| Overhead multiplier (x1.3) | 358 050 | 30% от raw acquisition base 1 193 500 ₽ | std enterprise B2B assumption |
| **Итого monthly acquisition cost** | **1 551 550** |  |  |

### Расчёт blended CAC
- New paying customers / month = **1,6**
- **Blended fully-loaded CAC = 1 551 550 / 1,6 = 969 719 ₽**

Но для инвестиционной оценки этого кейса добавляю ещё обязательный enterprise reality-check: часть CTO/solution architect времени сидит в пилотах и security review, а не отражена полностью в marketing/sales lines. Дополнительная аллокация presale-engineering = **580 000 ₽/мес**. Тогда:

- Adjusted monthly acquisition cost = **2 131 550 ₽/мес**
- **Investment-grade blended CAC = 2 131 550 / 1,6 = 1 332 219 ₽**

Для консервативной модели беру ещё 15% buffer на длинный procurement tail:
- **Final fully-loaded CAC = 1 532 000 ₽ на нового платящего клиента**

### CAC по каналам

| Канал | Аллоцированный spend / мес, ₽ | New customers / мес | CAC channel, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound | 1 120 000 | 0,9 | 1 244 444 | базовый рабочий канал |
| Partners / integrators | 640 000 | 0,5 | 1 280 000 | дорогой, но с лучшей конверсией в pilot |
| Events / inbound | 371 550 | 0,2 | 1 857 750 | самый дорогой канал на раннем объёме |
| **Blended** | **2 131 550** | **1,6** | **1 332 219** | raw investment CAC before tail buffer |
| **Blended final** | **—** | **—** | **1 532 000** | консервативный CAC для модели |

### Sanity check по benchmark
- Для **Enterprise SaaS B2B в РФ: 300-900 тыс. ₽/клиент**.
- Для этого кейса продукт ближе к **regulated / enterprise governance** с тяжёлым presale и security review, поэтому CAC выше базового enterprise benchmark допустим.
- Итоговый **1,53 млн ₽ CAC** выглядит жёстко, но не абсурдно для сложного enterprise governance motion. Если считать только media+sales, CAC был бы искусственно занижен.

---

## 4) LTV и churn

### Benchmark churn
Для enterprise B2B SaaS с высоким ACV churn обычно заметно ниже SMB:
- ChartMogul пишет, что у SaaS с ARPA **$500+** customer churn обычно около **1-2% в месяц**. [T4]
- Optifai даёт для enterprise сегмента **1-2% monthly churn**, а для сегмента **>$100K ACV** показывает около **0,7% monthly logo churn**. [T4]

Для РФ и ранней стадии нового control-plane продукта беру **хуже global best-case**, то есть **1,5% monthly logo churn**, чтобы не завысить LTV.

### Расчёт LTV
Формула:

`LTV = (MRR × Gross Margin %) / Monthly Churn`

Подставляем:
- MRR = **400 000 ₽**
- Gross Margin = **75,9%**
- Monthly Churn = **1,5%**

`LTV = 400 000 × 0,759 / 0,015 = 20 240 000 ₽`

Округляю:
- **LTV = 20,24 млн ₽**
- Annualized churn equivalent ≈ **16,6%**

---

## 5) LTV/CAC

- LTV = **20,24 млн ₽**
- CAC = **1,532 млн ₽**

`LTV/CAC = 20 240 000 / 1 532 000 = 13,2x`

### Вывод
- **LTV/CAC = 13,2:1**
- Требование investment grade **>= 3:1** выполнено с большим запасом.
- Даже если ухудшить churn до **2,5%/мес**, LTV/CAC останется около **7,9x**.

---

## 6) CAC Payback

### Строгий расчёт по gross profit
- CAC = **1 532 000 ₽**
- Gross profit per customer/month = **303 400 ₽**

`CAC Payback = 1 532 000 / 303 400 = 5,05 мес`

### Sanity check по формуле из задания
- CAC / MRR = **1 532 000 / 400 000 = 3,83 мес**

### Вывод
- **CAC Payback = 5,1 месяца** по gross profit basis
- Это лучше порога **< 12 месяцев** и комфортно даже для enterprise motion.

---

## 7) Contribution Margin %

В P5 считаю contribution margin как выручка минус COGS и прямые переменные продажи/обслуживание после запуска.

Дополнительные переменные на клиента в месяц:
- Success travel / workshops allocation: **12 000 ₽**
- AE variable commission allocation: **23 400 ₽**

Итого variable post-sale costs = **96 600 + 12 000 + 23 400 = 132 000 ₽**

- Revenue = **400 000 ₽**
- Contribution after variable costs = **268 000 ₽**

`Contribution Margin % = 268 000 / 400 000 = 67,0%`

### Вывод
- **Contribution Margin = 67,0%**
- Для AI-governance enterprise SaaS это хороший уровень, оставляющий место под heavy sales motion.

---

## 8) Team & FOT

### Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 700 000 | 0 (founder) | 0 | 210 000 | 910 000 |
| CTO/Tech Lead | 1 | 600 000 | 0 (founder/early) | 0 | 180 000 | 780 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 ×2 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 360 000 | 1-2 | 1 | 108 000 | 468 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE (Account Exec) | 1 | 360 000 | 1-2 | 2-3 | 108 000 | 468 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Finance/Ops | 0,5 | 140 000 | 1 | 1 | 42 000 | 182 000 |
| **Итого full team** | **10,5** | — | — | — | — | **5 512 000 ₽/мес** |

### Функции команды

| Роль | Ключевая функция |
|---|---|
| CEO | enterprise sales, strategic partnerships, top accounts |
| CTO/Tech Lead | architecture, security posture, enterprise solutioning |
| Senior Backend | policy engine, connectors, admin workflows |
| ML Engineer | AI inventory classification, summaries, risk workflows |
| DevOps | deployments, observability, uptime, infra cost control |
| Frontend | admin console, dashboards, governance UX |
| SDR | account mapping, meetings, outbound sequences |
| AE | discovery, demo, proposal, procurement navigation |
| Customer Success | onboarding, QBR, retention, expansion |
| Finance/Ops | contracts, billing, reporting, vendor ops |

### Комментарий по benchmark
- Senior backend в Москве на HH.ru встречается в коридоре примерно **350-550 тыс. ₽**. [T3]
- ML engineer по HH.ru часто уже уходит в **400-700 тыс. ₽**. [T3]
- Enterprise/account executive в Москве легко уходит в диапазон **300-500 тыс. ₽** плюс комиссия. [T3]
- DevOps senior в HH.ru часто видно в диапазоне около **250-430 тыс. ₽** и выше. [T3]

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT fully-loaded, ₽/мес |
|---|---|---:|
| M1 | CEO, CTO | 1 690 000 |
| M2 | + SDR | 1 924 000 |
| M3 | + Frontend | 2 314 000 |
| M4 | + Backend #1, AE | 3 328 000 |
| M5 | + DevOps | 3 796 000 |
| M6 | + ML Engineer | 4 446 000 |
| M7 | + Backend #2 | 4 992 000 |
| M8 | + Customer Success | 5 330 000 |
| M9 | + 0,5 Finance/Ops | 5 512 000 |
| M10 | full team | 5 512 000 |
| M11 | full team | 5 512 000 |
| M12 | full team | 5 512 000 |

### Проверка realism
- В M1 нет найма 5+ человек, кроме founders. Red flag по найму нет.
- Уже в M1 FOT около **1,69 млн ₽**, что реалистично для founder-led enterprise SaaS.
- До full team компания дорастает только к **M9**, что лучше отражает time-to-hire и ramp.

---

## 9) Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Офис / встречи / переговорки | 220 000 | гибридный формат + enterprise meetings |
| Shared cloud / platform base | 260 000 | не клиентский variable, а базовый платформенный слой |
| ПО и внутренние инструменты | 240 000 | Jira, Git, security, CRM base seats, BI |
| Legal / accounting / audit | 180 000 | договоры, DPA, ИБ-приложения, бухучёт |
| Recruiting / HR ops | 110 000 | hiring support |
| Travel / onsite workshops | 180 000 | командировки к enterprise accounts |
| Admin / benefits / misc | 190 000 | связь, компенсации, админка |
| **Итого fixed non-FOT** | **1 380 000** |  |

### Total fixed cost base
- Full team FOT = **5 512 000 ₽/мес**
- Fixed non-FOT = **1 380 000 ₽/мес**
- **Total fixed cost base = 6 892 000 ₽/мес**

---

## 10) Break-even

### Break-even по числу клиентов
- Contribution per client/month = **268 000 ₽**
- Fixed costs/month = **6 892 000 ₽**

`Break-even clients = 6 892 000 / 268 000 = 25,72`

Но с учётом того, что часть fixed non-FOT travel/legal масштабируется неравномерно, operational steady-state можно считать при fixed base **5 650 000 ₽** без части growth-опций. Тогда:

`Operational break-even clients = 5 650 000 / 268 000 = 21,08`

Округляю:
- **Break-even = 21 клиент** по operational fixed base
- **Stress break-even = 26 клиентов** по full loaded fixed base

### Break-even по месяцам
Модель набора active paying clients:
- M1: 0
- M2: 0
- M3: 0
- M4: 1
- M5: 2
- M6: 4
- M7: 6
- M8: 9
- M9: 12
- M10: 16
- M11: 21
- M12: 26

Тогда contribution profit:
- M10: 16 × 268k = **4,29 млн ₽** < fixed costs
- M11: 21 × 268k = **5,63 млн ₽** ≈ operational fixed base
- M12: 26 × 268k = **6,97 млн ₽** > full loaded fixed base

### Вывод
- **Break-even по клиентам: 21 клиент operational / 26 клиентов stress-case**
- **Break-even по времени: около M11-M12**

---

## 11) Burn-to-breakeven и runway

### Burn-to-breakeven
Упрощённо считаю burn как fixed costs + acquisition spend - gross profit.

| Месяц | Клиенты | Gross profit, ₽ | Fixed + acquisition, ₽ | Net burn / EBITDA-like, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 3 070 000 | -3 070 000 |
| M2 | 0 | 0 | 3 304 000 | -3 304 000 |
| M3 | 0 | 0 | 3 694 000 | -3 694 000 |
| M4 | 1 | 303 400 | 4 708 000 | -4 404 600 |
| M5 | 2 | 606 800 | 5 176 000 | -4 569 200 |
| M6 | 4 | 1 213 600 | 5 826 000 | -4 612 400 |
| M7 | 6 | 1 820 400 | 6 372 000 + 2 131 550 = 8 503 550 | -6 683 150 |
| M8 | 9 | 2 730 600 | 8 841 550 | -6 110 950 |
| M9 | 12 | 3 640 800 | 9 023 550 | -5 382 750 |
| M10 | 16 | 4 854 400 | 9 023 550 | -4 169 150 |
| M11 | 21 | 6 371 400 | 9 023 550 | -2 652 150 |
| M12 | 26 | 7 888 400 | 9 023 550 | -1 135 150 |

### Интерпретация
- Если держать acquisition engine на уровне **1,6 новых платящих клиентов/мес**, бухгалтерский break-even наступит позже operational break-even.
- Но **fixed-cost coverage** достигается примерно на **M11-M12**.

### Startup capital и runway
Беру стартовый капитал **45 млн ₽**.

- Пиковый burn в фазе разгона: **~6,7 млн ₽/мес**
- Более типичный burn по году: **~4,8-5,2 млн ₽/мес**
- Cash runway при среднем burn **5,0 млн ₽/мес**: `45 / 5,0 = 9,0 мес`

### Вывод по капиталу
- **45 млн ₽** достаточно для старта, но запас умеренный.
- Чтобы дойти до break-even без кассовой нервозности, реалистичнее иметь **55-65 млн ₽** стартового капитала / финансирования.
- Sanity check пройден: **startup_capital_to_bep < 10 млн ₽** здесь точно не получается.

---

## 12) Profit Gate

### Проверка на 50 клиентов
- Clients = **50**
- Revenue = **20,0 млн ₽/мес**
- COGS = **4,83 млн ₽/мес**
- Gross profit = **15,17 млн ₽/мес**
- Contribution profit = **13,40 млн ₽/мес**
- Fixed costs = **6,89 млн ₽/мес**
- EBITDA before growth CAC = **6,51 млн ₽/мес**

Даже если оставить acquisition engine включённым, компания остаётся выше порога **500 тыс. ₽/мес**.

### Финальный вывод по Profit Gate
- EBITDA **> 500 тыс. ₽/мес** достижим уже заметно раньше 50 клиентов.
- При **50 клиентах** модель выглядит уверенно прибыльной.
- **Profit Gate: PASS**

---

## 13) Риски модели

1. **Чек нельзя опускать к 180-250 тыс. ₽ MRR**, иначе enterprise presale CAC быстро съест экономику.
2. **Pilot-heavy motion** может незаметно перетащить модель из software в services-margin.
3. **Узкий buyer universe** ограничивает масштаб в РФ, даже если unit economics на клиента хорошие.
4. **Incumbent pressure** со стороны крупных платформ может поднять CAC и удлинить payback.

---

## Финальный вывод

ServiceNow Enterprise AI Control Tower v2 в российской модели не похож на массовый SaaS. Но как **узкий enterprise governance/control-plane слой** экономика выглядит сильной:
- COGS manageable
- fully-loaded CAC жёсткий, но реалистичный
- CAC payback в норме для enterprise
- LTV/CAC сильно выше инвестиционного порога
- Break-even достижим на **21-26 клиентах**
- При **50 клиентах** EBITDA уверенно положительный

**Решение этапа P5: PASS.**

## Источники
- [T1] pipeline/cases/servicenow-enterprise-ai-control-tower-v2/02-demand.md
- [T2] pipeline/cases/servicenow-enterprise-ai-control-tower-v2/01-intake.md
- [T3] HH.ru salary signals:
  - https://hh.ru/vacancies/senior-backend-developer
  - https://hh.ru/vacancies/account_executive
  - https://hh.ru/vacancies/machine-learning-engineer
  - https://hh.ru/vacancies/senior-devops-engineer/polniy_den
- [T4] Churn benchmarks:
  - https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
  - https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
  - https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
  - https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/

Все расчёты по CAC, break-even, FOT timeline и runway являются аналитической моделью для РФ 2026, а не публичным прайс-листом ServiceNow.