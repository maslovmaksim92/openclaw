---
stage: unit-economics
case: enterprise-agent-adoption-signals-v2
date: 2026-05-11
analyst: branch-models-lead
sector: AI-SERVICES
verdict: REJECT
confidence: medium
---

# 04-economics — Unit Economics

## Краткий вывод
Standalone-модель для `enterprise agent adoption signals / managed-agent services` как отдельного repeatable бизнеса **неинвестиционного качества**.

- **MRR на клиента:** 350 000 ₽/мес
- **COGS на клиента:** 220 000 ₽/мес
- **Gross Profit на клиента:** 130 000 ₽/мес
- **Gross Margin:** 37,1%
- **Contribution Margin:** 32,1%
- **Blended fully-loaded CAC:** 2 536 000 ₽
- **Churn rate:** 4,0% в месяц
- **LTV:** 3 250 000 ₽
- **LTV/CAC:** **1,28x**
- **CAC Payback:** 7,2 мес по обязательной формуле `CAC / MRR`; 19,5 мес по более жёсткой формуле `CAC / Gross Profit`
- **Break-even:** 59 клиентов
- **EBITDA при 50 клиентах:** **-1,0 млн ₽/мес**

Итог: **Profit Gate FAIL**. Даже при 50 клиентах компания не достигает EBITDA 500k+/мес, а LTV/CAC сильно ниже порога 3:1 для investment grade.

---

## 1. Рабочая модель и допущения

Считаю не «чистый SaaS», а наиболее реалистичную для этого кейса модель: enterprise managed service вокруг внедрения и сопровождения агентных систем.

Почему беру именно её:
1. В `02-demand.md` уже видно, что standalone wedge слабый и рынок скорее service-led.
2. Для продажи нужен длинный presale: discovery, security review, pilot, legal, procurement.
3. После продажи остаётся тяжёлая delivery-нагрузка: кастомные интеграции, governance, поддержка, change management.

### Основные допущения
- **Средний контракт:** 350 000 ₽ MRR на клиента после пилота.
- **Средний срок жизни клиента:** 25 месяцев при churn 4,0%/мес как консервативный early-stage benchmark для дорогого B2B-offering.
- **Сегмент:** enterprise / upper mid-market B2B, значит fully-loaded CAC считаю по enterprise логике, а не как «реклама / сделки».
- **Команда:** строится медленно, без нереалистичного найма 5+ человек в первый месяц.

---

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account списка | SDR | HH/LinkedIn-аналоги, таблицы, CRM | 40 мин | 1 200 | низкая |
| 2 | Исследование ICP и pain points | SDR + founder | CRM, сайты компаний, manual research | 50 мин | 2 100 | низкая |
| 3 | Персонализированный outreach | SDR | почта, мессенджеры, sequencing tool | 25 мин | 900 | средняя |
| 4 | Follow-up 1–3 касания | SDR | sequencing tool, CRM | 35 мин | 1 200 | средняя |
| 5 | Qualification call | AE | Zoom/Meet, CRM | 45 мин | 3 000 | низкая |
| 6 | Discovery + mapping use cases | AE + CEO/solutions | Zoom, Miro, CRM | 90 мин | 8 500 | низкая |
| 7 | Security/compliance pre-check | CTO/solutions | Notion, questionnaires, docs | 120 мин | 6 500 | низкая |
| 8 | Demo / architecture workshop | CTO + AE | Demo env, slides, Meet | 120 мин | 9 000 | низкая |
| 9 | Пилот scoping и proposal | AE + CTO + CEO | Docs, calculator, CRM | 180 мин | 16 000 | низкая |
| 10 | Legal / procurement loop | CEO + AE | договоры, e-sign, email | 14 дней цикл | 18 000 | низкая |
| 11 | Платный pilot onboarding | CTO + backend + ML | cloud, repo, PM tools | 2-3 недели | 75 000 | средняя |
| 12 | Pilot review и расширение до retainer | CEO + AE + client sponsor | slides, KPI dashboard | 60 мин | 5 500 | низкая |
| 13 | Выставление счёта | Ops/finance | ЭДО, банк, 1С | 20 мин | 700 | высокая |
| 14 | Получение оплаты | Finance | банк, ЭДО | 3-10 дней DSO | 300 | высокая |

### Вывод по процессу
Это **дорогой и медленный sales motion**. Большая часть CAC сидит не в рекламе, а в людях, пилотах, legal/procurement и пресейле.

---

## 3. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM/API и облако | 70 000 | inference + storage + monitoring | при кастомных enterprise workloads |
| Delivery / solutions engineering | 95 000 | доля backend/ML/CTO времени | кастомизация и поддержка use cases |
| QA / observability / on-call | 18 000 | доля DevOps + monitoring | прод-нагрузка и инциденты |
| Customer Success / support | 14 000 | доля CSM времени | weekly sync, helpdesk, adoption |
| Security / reporting / governance | 8 000 | аудит-логи, отчёты, review | enterprise-требования |
| Travel / workshops amortized | 15 000 | редкие onsite и workshop costs | для enterprise сделок |
| **Итого COGS** | **220 000** |  |  |

### Gross Margin
- Выручка: **350 000 ₽/мес**
- COGS: **220 000 ₽/мес**
- **Gross Profit:** 130 000 ₽/мес
- **Gross Margin:** 37,1%

Для investment-grade software-компании это слишком низко. Это больше похоже на тяжёлый services business с тонкой валовой маржой.

---

## 4. Fully-loaded CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Overhead multiplier) / New paying customers`

### CAC components

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс/таргет/ретаргет) | 90 000 | тестовый demand-capture бюджет | внутренняя модель для enterprise ABM |
| Outbound team FOT (SDR attributed to new) | 234 000 | 180 000 gross × 1,3 | HH benchmark: SDR в Москве [T6][T7] |
| Marketing team FOT (partial allocation) | 117 000 | 300 000 gross × 30% взносы × 30% времени | HH/рыночный диапазон product marketing для B2B tech, консервативная аллокация |
| AE attributed to new | 291 000 | 320 000 gross × 1,3 × 70% времени | HH benchmark: account executive / enterprise sales [T8] |
| Tools (CRM, enrichment, sequencing, data room) | 63 000 | HubSpot/Pipedrive + enrichment + call stack | рыночная сборка enterprise sales stack |
| Events / partnerships | 180 000 | 1 event + 2 partner activities в мес, усреднено | event-led enterprise GTM |
| Overhead multiplier (x1.3) | 293 000 | 30% на management / admin / finance поверх raw CAC | стандартный enterprise B2B uplift |
| **Итого acquire spend / мес** | **1 268 000** |  |  |

### Новые платящие клиенты
- Реалистично для ранней стадии: **0,5 нового платящего клиента в месяц**.
- Это эквивалентно **1 новому клиенту каждые 2 месяца** после фильтра discovery → pilot → procurement.

### Blended CAC
- **CAC = 1 268 000 / 0,5 = 2 536 000 ₽ на клиента**

### Sanity check
Это **выше** ориентиров 300-900k ₽ для enterprise SaaS, и это само по себе red flag. Но для данного кейса это объяснимо: здесь не software-led motion, а service-heavy motion с пилотом, кастомизацией и длинным legal loop. Именно поэтому standalone-модель плохо масштабируется.

---

## 5. CAC по каналам и воронка конверсии

| Канал | Вход в воронку | SQL | Proposal/Pilot | Paid win | Конверсия lead→paid | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Founder-led outbound ABM | 800 target accounts | 24 | 8 | 1 | 0,125% | 3 050 000 | самый дорогой, но даёт control |
| Партнёры / SI / интеграторы | 20 партнёров | 6 активных | 3 пилота | 1 | 5,0% | 1 750 000 | лучший канал, но медленно строится |
| Inbound content / webinars | 40 MQL | 10 | 4 | 1 | 2,5% | 900 000 | лучше по CAC, но объём ограничен |
| **Blended** | — | — | — | — | — | **2 536 000** | weighted average |

### Вывод по CAC
- CAC по каналам и blended CAC **существенно отличаются**, как и требуется.
- Самый реалистичный рост идёт через partners, но он плохо контролируется и долго разворачивается.
- Outbound как основной канал делает модель слишком тяжёлой.

---

## 6. LTV и churn rate

### Benchmark source
Для дорогих B2B/SaaS компаний с высоким ARPA ChartMogul указывает, что customer churn у mature-компаний обычно ниже, а для ранних стадий медианный churn заметно выше. По данным ChartMogul:
- для компаний с **ARPA > $1k/мес** median customer churn около **1,8%/мес** [T2]
- для early-stage компаний с ARR $1-3M monthly customer churn около **3,7%/мес** [T4]

### Что беру в модель
Беру **4,0% logo churn в месяц** как консервативный benchmark-proxy, потому что:
1. offering ещё не productized,
2. часть клиентов будет заходить через pilot и не расширяться в долгий retainer,
3. value proposition слишком широкий и risk of budget reallocation высокий.

### LTV calculation
- Gross Profit на клиента = **130 000 ₽/мес**
- Churn rate = **4,0%/мес**
- **LTV = 130 000 / 0,04 = 3 250 000 ₽**

### LTV/CAC
- **LTV/CAC = 3 250 000 / 2 536 000 = 1,28x**

### Интерпретация
- **< 2,0x**: слабая модель
- **< 3,0x**: не investment grade
- **1,28x**: почти весь lifetime gross profit съедается привлечением

---

## 7. CAC Payback

### Обязательная формула
- **CAC Payback = CAC / MRR = 2 536 000 / 350 000 = 7,2 месяца**

### Более строгая проверка по gross profit
- **CAC / Gross Profit = 2 536 000 / 130 000 = 19,5 месяца**

### Вывод
По формальной enterprise-границе `<18 мес` кейс выглядит терпимо только на упрощённой формуле. Но по фактическому валовому возврату денег payback уже почти **20 месяцев**, что для фонда выглядит слабо.

---

## 8. Contribution Margin

| Метрика | ₽/клиент/мес |
|---|---:|
| Revenue | 350 000 |
| COGS | 220 000 |
| Gross Profit | 130 000 |
| Sales commission / success fee | 17 500 |
| **Contribution Profit** | **112 500** |
| **Contribution Margin** | **32,1%** |

32,1% contribution margin недостаточна, чтобы комфортно нести длинный cycle, дорогой support и ошибочную найм-политику.

---

## 9. Team & FOT

### Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO | enterprise sales, fundraising, strategy | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | architecture, security, delivery control | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | integrations, orchestration | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | custom connectors, infra features | 420 000 | 126 000 | 546 000 |
| ML Engineer | agent logic, evals, prompt workflows | 500 000 | 150 000 | 650 000 |
| DevOps | deployments, observability, security hardening | 350 000 | 105 000 | 455 000 |
| Frontend | admin console / dashboards | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | qualification, deals, procurement | 320 000 | 96 000 | 416 000 |
| Customer Success | adoption, retention, upsell | 250 000 | 75 000 | 325 000 |
| Product / Marketing manager | positioning, webinars, collateral | 280 000 | 84 000 | 364 000 |
| **Итого full team FOT** |  |  |  | **5 486 000** |

### Hiring realism table

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 + бонус | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 320 000 + комиссия | 1-2 | 2-3 | 96 000 | 416 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product / Marketing manager | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |

### Источники по зарплатам
- CTO в Москве: вакансии hh.ru показывают вилки порядка **500-650k ₽** и выше [T5]
- SDR в Москве: публичные вакансии hh.ru дают рынок около **100-180k ₽** для base [T6][T7]
- AE / account executive в Москве: рынок порядка **350-500k ₽** для сильных B2B sales ролей [T8]
- ML Engineer и DevOps: hh.ru показывает рынок от нескольких сотен тысяч рублей, что подтверждает выбранные вилки [T9][T10]

---

## 10. Cumulative FOT timeline M1-M12

Логика: без нереалистичного массового найма в M1. Команда разворачивается ступенчато.

| Месяц | Кто подключается | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO | 1 560 000 |
| M2 | + Product/Marketing | 1 924 000 |
| M3 | + Senior Backend #1 | 2 470 000 |
| M4 | + ML Engineer | 3 120 000 |
| M5 | + AE | 3 536 000 |
| M6 | + DevOps, Frontend | 4 381 000 |
| M7 | + SDR | 4 615 000 |
| M8 | + Customer Success | 4 940 000 |
| M9 | + Senior Backend #2 | 5 486 000 |
| M10 | без изменений | 5 486 000 |
| M11 | без изменений | 5 486 000 |
| M12 | без изменений | 5 486 000 |

### Проверка реалистичности
- В первый месяц нет 5+ hires, значит базовый sanity check соблюдён.
- Даже так к M9 FOT выходит на **5,49 млн ₽/мес**, что типично для enterprise AI-services команды.

---

## 11. Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Core software / SaaS stack | 180 000 |
| Security / compliance / legal | 210 000 |
| Finance / accounting / admin | 140 000 |
| Travel / client workshops / events base | 220 000 |
| Office / equipment / misc G&A | 190 000 |
| Recruiting / agencies / employer brand | 200 000 |
| **Итого fixed costs без FOT** | **1 140 000** |

### Fixed cost base total
- Full team FOT: **5 486 000 ₽/мес**
- Non-FOT fixed: **1 140 000 ₽/мес**
- **Всего fixed cost base: 6 626 000 ₽/мес**

---

## 12. Break-even

### По количеству клиентов
- Contribution profit на клиента: **112 500 ₽/мес**
- Fixed cost base: **6 626 000 ₽/мес**
- **Break-even clients = 6 626 000 / 112 500 = 58,9**, округляю до **59 клиентов**

### Проверка на 50 клиентах
- Contribution profit at 50 clients = **5 625 000 ₽/мес**
- EBITDA = **5 625 000 - 6 626 000 = -1 001 000 ₽/мес**

**Следствие:** даже на 50 клиентах компания не достигает обязательного EBITDA 500k+/мес.

### По времени
Реалистичный набор клиентов для такого motion:
- M6: 1
- M7: 2
- M8: 4
- M9: 6
- M10: 9
- M11: 12
- M12: 16

При такой траектории **break-even не достигается в первые 12 месяцев**. При сохранении конверсий и найм-плана выход к BEP смещается примерно на **M16-M18**, что слишком долго для такого слабого LTV/CAC.

---

## 13. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Грубая проверка по формуле пользователя: когда `MRR × GM% > fixed costs`.
- Revenue/client = 350 000 ₽
- GM% = 37,1%
- Gross profit/client = 130 000 ₽
- Fixed costs = 6 626 000 ₽
- Нужно **51+ клиента только для покрытия fixed costs по gross profit**

То есть бизнес жжёт деньги почти весь первый год. С учётом acquisition spend и ramp delivery cumulative burn до точки безубыточности получается порядка **55-60 млн ₽**.

### Cash runway
Беру **startup_capital = 40 млн ₽**.
- При burn 3,5-5,5 млн ₽/мес на отрезке M4-M12 runway составляет примерно **8-10 месяцев**.
- До break-even этой подушки **не хватает**.

### Вывод по капиталу
Для такого кейса нужно скорее **55-65 млн ₽** до уверенного BEP. Это уже плохой профиль риска для бизнеса, где LTV/CAC лишь 1,28x.

---

## 14. Итоговый инвестиционный вывод

### Что не сходится
1. **Слабая валовая маржа**: 37,1% больше похожа на services firm, чем на software company.
2. **Очень дорогой fully-loaded CAC**: 2,54 млн ₽ из-за длинного enterprise цикла и кастомного пресейла.
3. **LTV/CAC = 1,28x**: ниже и базового quality bar, и тем более ниже 3:1 для investment grade.
4. **Break-even только на 59 клиентах**.
5. **EBITDA при 50 клиентах отрицательная**, значит mandatory Profit Gate не выполняется.

### Verdict
**REJECT.**

Этот кейс можно использовать как supporting market signal для других service-кейсов, но как отдельный фондовый объект он не проходит по unit economics.

---

## Sources
- [T1] OpenAI + Accenture enterprise AI partnership, 2025-12-01: https://newsroom.accenture.com/news/2025/openai-and-accenture-accelerate-enterprise-reinvention-with-advanced-ai
- [T2] ChartMogul, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T3] ChartMogul, Revenue churn benchmarks: https://chartmogul.com/saas-metrics/revenue-churn/
- [T4] ChartMogul, Customer churn by ARR stage: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
- [T5] HH.ru CTO vacancy example: https://hh.ru/vacancy/129284953
- [T6] HH.ru SDR vacancy example: https://hh.ru/vacancy/128565026
- [T7] HH.ru SDR search Moscow: https://hh.ru/vacancy/129428700
- [T8] HH.ru account executive Moscow: https://hh.ru/vacancies/account_executive
- [T9] HH.ru machine learning engineer Moscow: https://hh.ru/vacancies/machine-learning-engineer
- [T10] HH.ru DevOps Moscow: https://hh.ru/vacancies/devops
