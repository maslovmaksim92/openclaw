---
stage: unit-economics
case: ai-tranzaktsionnyi-skoring-dlya-mfo-i-bankov
date: 2026-05-09
analyst: branch-models-lead
sector: FINTECH
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P5: REJECTED.**

Кейс проходит проверку по эффективности привлечения, но **не проходит инвестиционный Profit Gate на уровне фонда**:

1. **Blended fully-loaded CAC = 1 049 000 ₽ на 1 нового платящего клиента**. Для regulated fintech это дорого, но ещё в допустимом диапазоне сложных B2B-продаж.
2. **LTV/CAC = 4,2x**, то есть сама воронка продаж не сломана.
3. **CAC Payback = 6,6 мес** по формуле CAC / MRR, что выглядит нормально.
4. Критический провал в другом месте: при реалистичном FOT, compliance-слое, интеграциях и enterprise support компания **не выходит на EBITDA > 500 000 ₽/мес даже на 50 клиентах**.
5. При текущей модели нужно **64 клиента для ежемесячного breakeven**, что слишком близко к верхней границе адресуемого рынка из `02-demand.md`.

**Решение: REJECTED и перенос в `pipeline/rejected/`.**

---

## 1. Базовые допущения модели

### ICP и коммерческая модель
- Сегмент: regulated fintech, digital-first МФО, mid-tier банки, embedded lenders.
- Motion: pilot + интеграция + recurring platform fee.
- Средний чек после скидок и пилотного периода: **160 000 ₽ MRR на клиента**.
- Разовый setup fee: **300 000 ₽**.
- Средний sales cycle: **4-6 месяцев**.
- Новые платящие клиенты в steady state: **3 в месяц**.

### Почему беру 160 000 ₽ MRR, а не 250 000-350 000 ₽
В `02-demand.md` было показано, что локальный реалистичный диапазон лежит между **80-150 тыс. ₽/мес** для SaaS/API и **250-500 тыс. ₽/мес** для white-label enterprise. Для модели фонда беру **консервативный blended-чек 160 тыс. ₽**, потому что:
- часть сделок придёт из МФО, а не только из крупных банков;
- первые 10-20 клиентов почти всегда подписываются с дисконтом за пилот, референс и кастомизацию;
- regulated buyer часто уводит часть стоимости в разовый проект внедрения, а не в чистый recurring.

### Churn benchmark
Для high-ARPA B2B SaaS churn обычно ниже массового SaaS. ChartMogul указывает, что типичный SaaS churn составляет **3-7% в месяц**, а у B2B с более высоким ARPA удержание заметно лучше; это позволяет взять **2,5% monthly logo churn** как умеренно-консервативный benchmark для early-stage regulated B2B. [T7][inference]

В модели использую:
- **Monthly churn = 2,5%**
- Средняя жизнь клиента = **40 месяцев**

---

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор целевых аккаунтов банков/МФО | SDR | HH/рынок, сайты компаний, CRM | 2 ч на аккаунт | 1 500 | Низкая |
| 2 | Обогащение контактов decision makers | SDR | CRM, e-mail finder, ручной ресерч | 1 ч | 700 | Низкая |
| 3 | Первый outbound-touch | SDR | почта, телефония, мессенджеры | 20 мин | 250 | Средняя |
| 4 | Follow-up 1-3 касания | SDR | CRM sequences, телефония | 45 мин | 550 | Средняя |
| 5 | Discovery call | AE + founder | VC/телефон, презентация | 1 ч | 6 000 | Низкая |
| 6 | Сбор pain points и data-map | AE + CTO | Notion, Miro, чек-лист интеграции | 3 ч | 18 000 | Низкая |
| 7 | Предварительный ROI-калькулятор | AE + risk analyst | spreadsheet/model | 2 ч | 8 000 | Средняя |
| 8 | Security/compliance pre-check | CTO + compliance | чек-листы, политика ИБ | 4 ч | 20 000 | Низкая |
| 9 | Пилотное предложение и SoW | AE + CEO | шаблон договора, коммерческое предложение | 3 ч | 12 000 | Средняя |
| 10 | Юрсогласование и закупка | CEO + юрист | договор, ЭДО | 3-6 недель | 35 000 | Низкая |
| 11 | Data onboarding | CTO + Backend + ML | API, SFTP, sandbox | 2-3 недели | 110 000 | Низкая |
| 12 | Настройка модели и rules layer | ML engineer | ML pipeline, feature store | 1-2 недели | 85 000 | Средняя |
| 13 | Champion/challenger backtest | ML + risk analyst | notebooks, BI | 1 неделя | 45 000 | Средняя |
| 14 | Pilot go-live | CTO + AE + CSM | мониторинг, алерты | 3 дня | 30 000 | Средняя |
| 15 | Еженедельный review пилота | AE + ML + client risk owner | BI, dashboard | 1 ч/нед | 18 000/мес | Средняя |
| 16 | Конверсия в paid annual/rolling contract | AE + CEO | CPQ, договор | 1-2 недели | 20 000 | Низкая |
| 17 | Invoice / ЭДО / оплата | Finance/CEO | банк, ЭДО, CRM | 30 мин | 2 000 | Высокая |
| 18 | Пост-продажная поддержка | CSM + ML support | helpdesk, monitoring | 4-6 ч/мес | 18 000/мес | Средняя |

### Вывод по процессу
- Продажа **не self-serve** и не inside-sales-only.
- Большая часть стоимости сидит не в рекламном клике, а в **ручных enterprise-касаниях, пилоте, интеграции и compliance**.
- Это автоматически тянет CAC вверх и ограничивает скорость масштабирования.

---

## 3. COGS на 1 клиента в месяц

### COGS breakdown

| Статья | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| Облачная инфраструктура inference/storage | 16 000 | compute + storage + резерв | базовая модель scoring/feature serving |
| Data/API fees (БКИ, транзакционные провайдеры, enrichment) | 17 000 | blended estimate на активного клиента | критичная переменная статья |
| ML monitoring / logging / retraining reserve | 5 000 | логирование, drift-monitoring | нужен audit trail |
| Support & customer success | 7 000 | доля FOT CSM на клиента | при 35-40 активных клиентах |
| Compliance / security support reserve | 3 000 | политика ИБ, аудит, ответы на security questionnaire | regulated overhead |
| Амортизация внедрения и доработок | 2 000 | setup effort spread over 12 мес | консервативно |
| **Итого COGS** | **50 000** |  |  |

### Gross profit на клиента
- MRR = **160 000 ₽**
- COGS = **50 000 ₽**
- **Contribution / Gross Profit = 110 000 ₽**
- **Contribution Margin = 68,75%**

Это неплохая валовая маржа для fintech infrastructure, но она **слишком низкая**, чтобы нести heavy enterprise team при ограниченном TAM.

---

## 4. CAC по каналам с воронкой

| Канал | Monthly spend, ₽ | Воронка | New paid customers / мес | CAC, ₽ |
|---|---:|---|---:|---:|
| Outbound enterprise | 1 650 000 | 300 accounts → 42 meetings (14%) → 18 SQL (43%) → 6 pilots (33%) → 1,5 paid (25%) | 1,5 | 1 100 000 |
| Партнёрства / интеграторы | 450 000 | 10 referrals → 7 discovery (70%) → 4 SQL (57%) → 1,5 pilots (38%) → 0,75 paid (50%) | 0,75 | 600 000 |
| Inbound / контент / performance | 300 000 | 25 MQL → 6 discovery (24%) → 3 SQL (50%) → 1 pilot (33%) → 0,5 paid (50%) | 0,5 | 600 000 |
| Личные связи founder / industry network | 746 000 | 12 warm intros → 8 meetings (67%) → 5 SQL (63%) → 2 pilots (40%) → 0,25 paid (13%) | 0,25 | 2 984 000 |
| **Blended** | **3 146 000** |  | **3,0** | **1 049 000** |

### Почему founder-network такой дорогой
На ранней стадии он полезен для first doors open, но плохо масштабируется. Когда разложить на стоимость времени CEO и высокий процент неуспешных кастомных обсуждений, канал оказывается не бесплатным.

---

## 5. Fully-loaded CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools + Events/partnerships + Overhead multiplier) / New paying customers`

### Таблица компонентов

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 220 000 | тестовый demand capture + retargeting + брендовый трафик | T6 + model |
| Outbound team FOT (SDR + AE, attributed to new) | 1 050 000 | SDR 180k gross + AE 360k gross + 30% взносы + founder assist allocation | T4 + model |
| Marketing team FOT (partial allocation) | 180 000 | 0,5 FTE content/marketing manager с 30% взносами | T4 + model |
| Tools (CRM, телефония, data tools, sequencing) | 140 000 | amoCRM, телефония, e-mail tools, аналитика | T5 + model |
| Events / partnerships | 830 000 | спонсорство, поездки, отраслевые встречи, партнёрские rev-share advances | model |
| Overhead multiplier (x1.3) | 726 000 | 30% на management overhead и non-billable presales на subtotal 2 420 000 ₽ | enterprise B2B standard |
| **Итого** | **3 146 000** |  |  |

### Sanity-check по сегменту
- Raw CAC до overhead = **806 667 ₽**.
- Fully-loaded CAC = **1 049 000 ₽**.
- Для regulated fintech user дал sanity-band **200-700k ₽** для B2B fintech и **2,5-3,0x multiplier** для regulated motion. Наш результат находится **выше mid-market benchmark, но логичен для pilot-heavy regulated sale**.
- CAC не выглядит заниженным, наоборот, это реалистичный расчёт.

---

## 6. LTV, churn, LTV/CAC

### Параметры
- MRR per customer = **160 000 ₽**
- Gross profit per customer = **110 000 ₽**
- Monthly churn = **2,5%**
- Lifetime = **1 / 0,025 = 40 месяцев**

### LTV
Использую gross-profit LTV:

`LTV = Gross Profit per month / Churn`

`LTV = 110 000 / 0,025 = 4 400 000 ₽`

### LTV/CAC
`LTV/CAC = 4 400 000 / 1 049 000 = 4,2x`

### Вывод
- По чистой эффективности привлечения модель **формально investable**.
- Но фондовый уровень оценки не может смотреть только на LTV/CAC, потому что дальше упираемся в **market size и fixed-cost floor**.

---

## 7. CAC Payback

### Базовая формула пользователя
`CAC Payback = CAC / MRR_per_customer`

`1 049 000 / 160 000 = 6,6 месяца`

### Дополнительный GM-adjusted взгляд
`1 049 000 / 110 000 = 9,5 месяца`

### Вывод
- Формальный payback < 12 месяцев, то есть GTM не сломан.
- Но payback сам по себе не спасает кейс, если fixed-cost база слишком тяжёлая.

---

## 8. Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 700 000 | 0 | 0 | 210 000 | 910 000 |
| CTO / Tech Lead | 1 | 600 000 | 2-3 | 2 | 180 000 | 780 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 585 000 ×2 = 1 170 000 |
| ML Engineer | 1 | 600 000 | 2-3 | 2 | 180 000 | 780 000 |
| DevOps | 1 | 380 000 | 1-2 | 1 | 114 000 | 494 000 |
| Frontend | 1 | 320 000 | 1 | 1 | 96 000 | 416 000 |
| SDR | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 360 000 | 1-2 | 2-3 | 108 000 | 468 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Risk / Compliance analyst | 1 | 300 000 | 2-4 | 2 | 90 000 | 390 000 |
| **Итого steady-state FOT** | **10** |  |  |  |  | **5 980 000 ₽/мес** |

### Источник зарплат
Диапазоны собраны по актуальным вакансиям hh.ru в Москве и близким FinTech/Backend/SDR ролям, затем округлены до медианы для найма уровня, достаточного под regulated B2B stack. [T4][inference]

### Полная команда: роли и функции

| Роль | Функция | Fully-loaded salary, ₽/мес |
|---|---|---:|
| CEO | fundraising, enterprise sales, ключевые партнёрства | 910 000 |
| CTO | архитектура, security, data integration | 780 000 |
| Senior Backend #1 | API, scoring service, integrations | 585 000 |
| Senior Backend #2 | platform, data pipelines, client-specific connectors | 585 000 |
| ML Engineer | feature engineering, scorecards, monitoring | 780 000 |
| DevOps | infra, CI/CD, observability, security baseline | 494 000 |
| Frontend | internal dashboard, pilot UI, client кабинеты | 416 000 |
| SDR | outbound sourcing и first-touch | 234 000 |
| AE | discovery, pilots, closing | 468 000 |
| Customer Success | onboarding, QBR, support coordination | 338 000 |
| Risk / Compliance analyst | model governance, explainability, questionnaires | 390 000 |
| **Итого** |  | **5 980 000** |

### Cumulative FOT timeline M1-M12

| Месяц | Кто в команде | FOT_monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO | 910 000 | founder-only, discovery |
| M2 | CEO | 910 000 | найм CTO ещё идёт |
| M3 | CEO + CTO | 1 690 000 | CTO в ramp |
| M4 | + Backend #1 | 2 275 000 | старт платформы |
| M5 | + ML Engineer | 3 055 000 | модель ещё не на полной продуктивности |
| M6 | + AE | 3 523 000 | sales ramp только стартует |
| M7 | + Backend #2 + SDR | 4 342 000 | ещё нет полной выработки |
| M8 | + Customer Success | 4 680 000 | первые пилоты |
| M9 | + DevOps | 5 174 000 | подготовка к production-scale |
| M10 | + Frontend | 5 590 000 | client-facing dashboard |
| M11 | + Risk/Compliance | 5 980 000 | governance layer закрыт |
| M12 | та же команда | 5 980 000 | steady-state FOT |

### Sanity checks
- В M1 нет найма 5+ человек, значит time-to-hire не нарушен.
- Даже при аккуратном наборе команда быстро выходит к **≈6,0 млн ₽ FOT/мес**.
- Это и есть главная причина, почему ранняя оценка из intake была слишком оптимистичной.

---

## 9. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 980 000 |
| Юридическое сопровождение, аудит, ЭДО | 140 000 |
| Security/compliance baseline, pentest reserve | 160 000 |
| Base cloud / shared infra | 150 000 |
| Общие software / internal tools | 110 000 |
| Операционные расходы / офис / admin | 120 000 |
| Страхование, бухгалтерия, misc G&A | 140 000 |
| **Итого fixed costs / мес** | **6 800 000 ₽** |

> Важно: acquisition spend в CAC-таблице считаю отдельно, а не внутри fixed costs, чтобы не смешивать cost to serve и cost to acquire.

---

## 10. Break-even

### Break-even по количеству клиентов
- Contribution per client = **110 000 ₽/мес**
- Fixed costs = **6 800 000 ₽/мес**

`Break-even clients = 6 800 000 / 110 000 = 61,8`

Округляю вверх:

**Break-even = 62 клиента** без учёта acquisition burn.

Если включить ongoing acquisition machine хотя бы на уровне 300-500k net/month, фактический operating break-even сдвигается к **64 клиентам**.

### Break-even по выручке в месяц
- 62 клиента × 160 000 ₽ MRR = **9 920 000 ₽ MRR**
- 64 клиента × 160 000 ₽ MRR = **10 240 000 ₽ MRR**

### Проверка условия 50 клиентов
- 50 клиентов × 160 000 ₽ = **8 000 000 ₽ MRR**
- 50 клиентов × 110 000 ₽ contribution = **5 500 000 ₽ contribution**
- EBITDA до учёта роста = **5 500 000 - 6 800 000 = -1 300 000 ₽/мес**

**Следовательно, EBITDA > 500 000 ₽/мес не достижима даже при 50 клиентах. Profit Gate = FAIL.**

---

## 11. Burn-to-breakeven и runway

### Revenue ramp assumption
Консервативная траектория:
- M1-M8: 0-1 платящих клиента, в основном пилоты
- M9: 2 клиента
- M10: 4 клиента
- M11: 6 клиентов
- M12: 8 клиентов
- после M12: +3 клиента/мес в steady state

При такой скорости компания выходит к **64 клиентам только примерно к M31-M32** от старта, если продажи не ломаются и churn не ухудшается.

### Burn-to-breakeven
Даже если взять средний net burn:
- первые 12 месяцев: **≈4,8-5,2 млн ₽/мес**
- месяцы 13-24: **≈3,0-4,0 млн ₽/мес** до плотного заполнения клиентской базы

Суммарный капитал до operating breakeven получается порядка:

**≈95-110 млн ₽**

### Cash runway
Если взять `startup_capital = 80 000 000 ₽`:

`80 000 000 / 5 100 000 ≈ 15,7 месяца`

Даже с плавным снижением burn runway получается **около 16-18 месяцев**, а breakeven приходит существенно позже.

### Вывод
- Для данной бизнес-модели нужно слишком много капитала до breakeven.
- При этом рынок из `02-demand.md` ограничен: SAM порядка **181-188 млн ₽/год**, а компании нужно выйти почти к **120+ млн ₽ ARR run-rate**, чтобы стать устойчивой.
- Это слишком узкий коридор между market cap и cost base.

---

## 12. Почему кейс отклоняется на уровне фонда

### Что хорошо
- Реальная боль у клиента есть.
- WTP есть.
- LTV/CAC хороший.
- CAC payback не катастрофический.

### Что ломает инвесткейс
1. **Слишком высокий fixed-cost floor** для regulated delivery.
2. **Слишком длинный путь до 60+ активных клиентов**.
3. **Даже 50 клиентов не дают EBITDA > 500k/mo**.
4. Чтобы окупить такую платформу, нужно занять слишком большую долю уже и так неширокого SAM.
5. Модель легко уходит в consulting-heavy onboarding, где каждый новый клиент удлиняет срок до breakeven.

---

## Итог

**Вердикт: REJECTED.**

Не потому что рынок совсем плохой, а потому что **на уровне фонда этот кейс не даёт достаточно широкого пространства между реалистичным чеком, CAC, FOT и размером адресуемого рынка**. В regulated fintech такая компания может существовать как boutique infra-vendor или как feature внутри более крупного risk stack, но как standalone venture-scale актив в текущем виде кейс слабый.

## Источники
- [T4] HH.ru, выборка актуальных вакансий senior backend / SDR / enterprise sales в Москве: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancy/129522775 ; https://hh.ru/vacancy/128565026
- [T5] amoCRM тарифы: https://www.amocrm.ru/buy/tariff/
- [T6] Яндекс.Директ, минимальные бюджеты и дневной лимит: https://yandex.ru/support/direct/ru/strategies/minimal-budget ; https://yandex.ru/support/direct/en/strategies/day-budget
- [T7] ChartMogul, churn benchmark и retention context: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate ; https://chartmogul.com/reports/saas-benchmarks-report/ ; https://chartmogul.com/reports/saas-retention-the-new-normal/
- [T1] Банк России и demand-источники из `02-demand.md`
- [T2] Pricing / market sources из `02-demand.md`

[inference] означает аналитическое допущение на основе публичных benchmark-источников и логики enterprise fintech GTM.