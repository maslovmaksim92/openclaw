---
sector: FINTECH
stage: unit-economics
updated: 2026-04-24T21:46:00+03:00
verdict: REJECTED
---

# 04-economics — Unit Economics

## 1. Executive summary

**Итог: FAIL по profit gate.**

Почему:
1. При реалистичном mid-market B2B go-to-market в РФ fully-loaded CAC получается **~323 917 ₽ на нового платящего клиента**, что выше ранней intake-гипотезы 40–150 тыс. ₽ и ближе к lower bound enterprise-style sales.
2. При базовом чеке **65 000 ₽ MRR на клиента** и валовой марже **71,5%** клиент дает contribution after COGS **46 450 ₽/мес**, а payback по blended CAC составляет **~7,0 мес по revenue** или **~9,5 мес по gross profit**.
3. Даже при **50 клиентах** monthly revenue = **3,25 млн ₽**, gross profit = **2,3225 млн ₽**, но фиксированные расходы зрелой operating-команды составляют **~4,797 млн ₽/мес**, поэтому EBITDA остается около **-2,475 млн ₽/мес**.
4. Даже в lean-конфигурации без части найма EBITDA при 50 клиентах не достигает **+500 тыс. ₽/мес**, а значит кейс не проходит обязательный порог программы.

## 2. ICP и модель монетизации

**ICP:** B2B SMB и mid-market компании с регулярной отсрочкой платежа, счетами из 1С, ЭДО и банковских выписок.

**Продукт:** AI-слой над дебиторкой, который:
- собирает данные из 1С, ЭДО, банк-клиента,
- приоритизирует просрочку,
- предлагает следующий шаг,
- генерирует reminders, сверки и эскалации,
- ведет workflow collection для CFO / финменеджера / бухгалтерии.

**Базовый pricing для модели:**
- Setup: 0–80 тыс. ₽, в базовой модели не учитываю как core revenue.
- Подписка: **65 000 ₽/клиент/мес**.
- Сегмент: **mid-market B2B**, не self-serve и не настоящий enterprise.

## 3. Подробный business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Генерация таргет-листа | SDR | HH/контактные базы, Excel, CRM | 20 мин/лид | 220 | 40% |
| 2 | Первый outbound outreach | SDR | Почта, телефония, CRM | 15 мин/лид | 165 | 50% |
| 3 | Follow-up 1–3 касания | SDR | CRM sequences, email, Telegram, телефония | 30 мин/лид | 330 | 55% |
| 4 | Квалификация боли и ICP fit | SDR | Скрипт, CRM | 20 мин/MQL | 220 | 35% |
| 5 | Discovery call | AE + иногда founder | Meet/Zoom, CRM | 60 мин | 1 650 | 20% |
| 6 | Расчет демо-сценария на данных клиента | Sales engineer / PM / founder | Sheets, SQL, demo env | 3 ч | 6 000 | 25% |
| 7 | Demo + ROI discussion | AE + founder | Meet/Zoom, deck | 90 мин | 2 400 | 15% |
| 8 | Security / IT / data access согласование | AE + CTO | Почта, docs, NDA | 4 ч | 10 000 | 10% |
| 9 | Pilot scoping и коммерческое предложение | AE + PM | Docs, CRM, КП | 3 ч | 6 900 | 20% |
| 10 | Переговоры / procurement / правки договора | AE + founder + legal template | Почта, docs | 4 ч | 9 200 | 15% |
| 11 | Выставление счета | Ops / finance | 1С, банк-клиент | 20 мин | 500 | 70% |
| 12 | Оплата первого месяца | Клиент | Банк-клиент | 5 раб. дней cycle time | 0 прямых | 100% |
| 13 | Onboarding: доступы к 1С/ЭДО/банку | CSM + implementation | TeamViewer/VPN, docs | 6 ч | 11 700 | 20% |
| 14 | Настройка правил collection | PM / CSM | Admin panel | 3 ч | 4 500 | 35% |
| 15 | Запуск рабочего контура | CSM | CRM, dashboard | 2 ч | 2 600 | 50% |
| 16 | Ежемесячное сопровождение | CSM + support + infra | CRM, helpdesk, monitoring | 3,5 ч/мес | 8 600 | 45% |

### Вывод по процессу
- Продажа не self-serve, а **human-assisted mid-market B2B**.
- Есть несколько дорогих ручных шагов: demo customization, доступы, согласование security и договора.
- Значит для blended CAC надо использовать **mid-market multiplier**, а не SMB self-serve.

## 4. COGS breakdown per client / month

### Переменные прямые затраты на 1 клиента в месяц
| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / AI inference | 2 500 | ~80–120k AI операций/мес на клиента, mix локальных и внешних моделей | для reminders, summary, next-best-action |
| OCR / parsing / ETL | 1 000 | разбор закрывающих, актов, выписок | часть клиентов почти не использует |
| Облако / БД / storage / monitoring | 2 000 | share infra cost | multi-tenant |
| Интеграции с 1С / ЭДО / bank connectors amortized | 3 000 | поддержка и обновления коннекторов | высоко для RU-fit продукта |
| Support / customer success variable | 6 000 | ~1,5 часа CSM + 0,8 часа support | early-stage high-touch |
| Payment / документооборот / billing ops | 500 | 1С, ЭДО, банк, операционные мелкие расходы | |
| Резерв на инциденты / ручные сверки | 3 500 | buffer 5,4% revenue | потому что workflow чувствителен к данным |
| **Итого COGS** | **18 500** |  |  |

**Gross profit per client/month = 65 000 - 18 500 = 46 500 ₽**  
**Contribution margin after COGS = 71,5%**

## 5. CAC by acquisition channel with funnel conversion

### Воронка по каналам
| Канал | Lead → MQL | MQL → SQL/demo | SQL → Paid | Lead → Paid | New paid / мес | Канальный spend, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound SDR | 18% | 35% | 18% | 1,13% | 3,0 | 780 000 | 260 000 |
| Paid ads (Яндекс.Директ / VK lead gen) | 8% | 22% | 12% | 0,21% | 1,2 | 420 000 | 350 000 |
| Партнеры 1С / аутсорсеры / интеграторы | 25% | 45% | 20% | 2,25% | 0,8 | 120 000 | 150 000 |
| Контент / inbound / вебинары | 12% | 28% | 15% | 0,50% | 0,6 | 90 000 | 150 000 |
| **Blended** | — | — | — | — | **5,6** | **1 410 000** | **251 786** |

## 6. FULLY-LOADED CAC

Сегмент здесь **mid-market B2B**, поэтому к raw acquisition cost применяю realistic overhead, tool stack и sales-support load. Вместо чистого маркетинга использую full formula.

### Формула
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Marketing team FOT allocated + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers**

### Разложение blended CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 420 000 | тестовый lead-gen бюджет для mid-market B2B | Yandex Direct pricing docs T5 + model assumption |
| Outbound team FOT (SDR/AE attributed to new) | 850 000 | 1 SDR 160k + 1 AE 320k + бонусы, затем +30% взносы ≈ 624k; 80% attributed to new = 499k, плюс founder-presales and sales engineer allocation до 850k | HH.ru вакансии T6-T10 + model assumption |
| Marketing team FOT (partial allocation) | 210 000 | product marketing / demand gen 162k fully-loaded × ~1,3 FTE allocation | HH / market benchmark + model assumption |
| Tools (CRM, телефония, sequences, enrichment) | 95 000 | amoCRM, телефония, почта, enrichment, BI | amoCRM pricing T11 + model assumption |
| Events/partnerships | 65 000 | 1–2 отраслевых вебинара/партнерских активации в мес averaged | model assumption |
| Subtotal raw CAC pool | **1 640 000** |  |  |
| Overhead multiplier (x1.3) | **492 000** | standard для mid-market B2B acquisition support | sanity benchmark from task policy |
| **Total fully-loaded acquisition pool** | **2 132 000** |  |  |
| New paying customers / мес | **6,58** | blended plan after partner assist | model assumption |
| **Fully-loaded CAC** | **323 917 ₽** | 2 132 000 / 6,58 | computed |

### Sanity check against benchmarks
- Для **mid-market SaaS** user guideline в задаче дает бенчмарк **60–250 тыс. ₽ CAC**.
- Наша оценка **324 тыс. ₽** выше typical mid-market range и уже подползает к enterprise-motion.
- Это красный флаг: либо продажи слишком кастомные, либо продукт недоупакован как software.

## 7. LTV with churn rate

Для mid-market B2B SaaS беру **monthly logo churn = 2,1%** как рабочий benchmark. Это соответствует сегменту ACV $10K–$50K в свежем benchmark Optifai за 2026 год.

### Расчет
- ARPU / MRR per client = **65 000 ₽/мес**
- Gross margin = **71,5%**
- Monthly churn = **2,1%**
- Lifetime in months = **1 / 0,021 = 47,6 мес**
- **Revenue LTV = 65 000 × 47,6 = 3 094 000 ₽**
- **Gross profit LTV = 46 500 × 47,6 = 2 213 400 ₽**

### Комментарий
Для early fintech workflow в РФ это **оптимистичный**, но не экстремальный retention case, потому что интеграции с 1С/ЭДО и включенность в cash collection действительно повышают switching cost. Но если churn поднимется к 3% monthly, экономика заметно слабеет.

## 8. LTV/CAC ratio

- **Revenue LTV / CAC = 3 094 000 / 323 917 = 9,6x**
- **Gross profit LTV / CAC = 2 213 400 / 323 917 = 6,8x**

### Интерпретация
Формально по LTV/CAC кейс **проходит investable threshold >3:1**.  
Но это **не спасает кейс**, потому что burn и fixed-cost base слишком тяжелые относительно возможной клиентской базы на раннем этапе.

## 9. CAC Payback

- **Payback on revenue basis = 323 917 / 65 000 = 5,0 мес**
- **Payback on gross profit basis = 323 917 / 46 500 = 7,0 мес**

**Итог:** по payback модель еще приемлема для mid-market B2B, но не выглядит exceptional.

## 10. Contribution Margin %

- Revenue per client/month = **65 000 ₽**
- COGS per client/month = **18 500 ₽**
- **Contribution Margin = 46 500 ₽ = 71,5%**

Для software-layer это нормально, но не outstanding, потому что продукт остается high-touch и содержит заметную долю implementation/support labor.

## 11. Team & FOT

### Полная команда: роли, функции, зарплаты
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | продажи, fundraising, key accounts | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | архитектура, security, roadmap | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | core backend, connectors | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | integrations, billing logic | 420 000 | 126 000 | 546 000 |
| Frontend | operator UI / dashboard | 300 000 | 90 000 | 390 000 |
| DevOps | infra, observability, releases | 350 000 | 105 000 | 455 000 |
| Product / Implementation manager | rollout, pilot, process mapping | 280 000 | 84 000 | 364 000 |
| SDR | outbound pipeline | 160 000 | 48 000 | 208 000 |
| AE | demos, closing | 320 000 | 96 000 | 416 000 |
| Customer Success | onboarding, renewals | 240 000 | 72 000 | 312 000 |
| Support / QA hybrid | issue triage, regressions | 180 000 | 54 000 | 234 000 |
| **Итого** |  |  |  | **4 966 000** |

### Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each |
| ML Engineer (если AI core) | 0 | 0 | — | — | — | 0 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 160 000 | 0,75 | 1 | 48 000 | 208 000 |
| AE (Account Exec) | 1 | 320 000 | 1,5 | 2,5 | 96 000 | 416 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### Hiring realism verdict
- Не нанимаю 5+ человек в M1, чтобы не нарушать time-to-hire realism.
- Но даже аккуратный hire plan все равно приводит к heavy FOT к M6–M8.
- Для такого продукта team requirement слишком велик относительно допустимого ARPU.

## 12. Cumulative FOT timeline M1-M12

### План подключения команды
- **M1:** founder only + 1 backend contractor equivalent.
- **M2:** Frontend joins.
- **M3:** Senior Backend #1, SDR.
- **M4:** DevOps, CSM.
- **M5:** AE.
- **M6:** CTO/Tech Lead.
- **M7:** Product/Implementation manager.
- **M8:** Senior Backend #2.
- **M9-M12:** support/QA hybrid.

### FOT monthly timeline
| Месяц | Кто в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO + contractor backend equivalent | 1 120 000 |
| M2 | + Frontend | 1 510 000 |
| M3 | + Backend #1 + SDR | 2 264 000 |
| M4 | + DevOps + CSM | 3 031 000 |
| M5 | + AE | 3 447 000 |
| M6 | + CTO | 4 162 000 |
| M7 | + Product/Implementation | 4 526 000 |
| M8 | + Backend #2 | 5 072 000 |
| M9 | + Support/QA | 5 306 000 |
| M10 | same | 5 306 000 |
| M11 | same | 5 306 000 |
| M12 | same | 5 306 000 |

## 13. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded operating team | 4 966 000 |
| Офис / коворкинг / admin reserve | 120 000 |
| Общее ПО / GSuite / Notion / dev tools | 85 000 |
| Legal / accounting / audit / compliance | 110 000 |
| Base cloud not in client COGS | 140 000 |
| Recruiting / employer brand averaged | 90 000 |
| Прочее G&A | 80 000 |
| **Итого fixed costs** | **5 591 000** |

Для расчетов break-even ниже беру более щадящую operating baseline **4 797 000 ₽/мес**, исключая часть founder comp и discretionary hiring. Это уже благоприятная для кейса трактовка.

## 14. Break-even by client count and by month

### Break-even by client count
Формула:
**Break-even clients = Fixed costs / Gross profit per client**

- Fixed costs for scaled but still lean team = **4 797 000 ₽/мес**
- Gross profit per client = **46 500 ₽/мес**
- **Break-even client count = 4 797 000 / 46 500 = 103,2 клиента**

Округляя вверх, нужно **104 платящих клиента**.

### Stress-test at 50 clients
- Revenue = **3 250 000 ₽/мес**
- COGS = **925 000 ₽/мес**
- Gross profit = **2 325 000 ₽/мес**
- EBITDA after lean fixed costs = **-2 472 000 ₽/мес**

### Profit gate check
Чтобы пройти внутренний порог, нужно показать достижимость **EBITDA > 500 000 ₽/мес хотя бы при 50 клиентах**.  
Фактически при 50 клиентах модель глубоко отрицательная. **Profit Gate = FAIL.**

### Break-even by month
Если предположить траекторию новых клиентов: 1 / 2 / 3 / 4 / 5 / 6 / 7 / 8 / 9 / 10 / 11 / 12 net adds per month, то к концу M12 будет лишь **78 клиентов** без существенного churn drag. Это **ниже точки безубыточности 104 клиента**.

Следовательно, **в первый год проект не выходит на break-even** даже по благоприятной траектории.

## 15. Burn-to-breakeven и Cash runway

### Burn-to-breakeven
Возьмем консервативно средний burn до BEP:
- Средний FOT M1-M12 = **3,92 млн ₽/мес**
- Infra/G&A/acquisition extra = **1,55 млн ₽/мес**
- Средний gross profit recognition from early clients during first year = **~0,95 млн ₽/мес**
- **Net burn ≈ 4,52 млн ₽/мес** в среднем по году

Если break-even достигается только после ~104 клиентов, капитал до BEP нужен порядка:
- **~45–60 млн ₽** в зависимости от скорости найма и маркетинга.

### Cash runway
При **startup capital = 30 млн ₽** и среднем burn **4,52 млн ₽/мес**:
- **Cash runway = 30 / 4,52 ≈ 6,6 месяца**

Даже при 40 млн ₽ runway около **8,8 месяца**, что мало для B2B product с интеграциями и длинным sales cycle.

## 16. Почему экономика ломается

1. **Слишком тяжелый implementation motion.** Это не plug-and-play SaaS, а полу-сервисная поставка.
2. **Низкий ceiling по чеку.** При ARPU 65 тыс. ₽ и даже 90 тыс. ₽ продукт не тянет команду, нужную для безопасной fintech-интеграции.
3. **Слабый operating leverage в ранней фазе.** Каждому клиенту нужны доступы, mapping, исключения, ручные сверки.
4. **Продажи сложнее, чем intake-предполагал.** Fully-loaded CAC уходит выше 300 тыс. ₽.
5. **Break-even > 100 клиентов** слишком высок для такого узкого workflow на ранней стадии.

## 17. Verdict

**Экономический verdict: REJECTED.**

Хотя demand-stage выглядел убедительно, unit economics для фонда слабые:
- LTV/CAC формально хороший,
- payback терпимый,
- но **операционная база не масштабируется в +500 тыс. ₽ EBITDA при 50 клиентах**,
- а значит кейс не дотягивает до инвестиционного стандарта pipeline.

## Sources
- **T1** `00-brief.md`
- **T2** `01-intake.md`
- **T3** `02-demand.md`
- **T4** Optifai, B2B SaaS churn by ACV, 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- **T5** Яндекс Директ, про стоимость и аукционную механику, 2026: https://direct.yandex.ru/base/articles/stoimost-kontekstnoy-reklamy-v-yandeks-direkte ; https://yandex.ru/support/direct/ru/payments/faq ; https://yandex.ru/support/direct/strategies/average-cpc.html
- **T6** HH.ru, вакансия Menеджер по B2B-продажам/SDR, Mindbox, 2026: https://hh.ru/vacancy/129617556
- **T7** HH.ru, вакансия SDR / Sales Development Representative (IT / SaaS), Skillaz, 2026: https://hh.ru/vacancy/129774256
- **T8** HH.ru, подборка senior backend developer в Москве: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancies/backend-developer
- **T9** HH.ru, подборка frontend developer и customer success manager в Москве: https://hh.ru/vacancies/frontend-developer ; https://hh.ru/vacancies/customer-success-manager
- **T10** HH.ru, подборка account executive и DevOps в Москве: https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancies/devops
- **T11** amoCRM pricing: https://www.amocrm.ru/buy/tariff/

> Все денежные оценки, которых нет в публичных источниках, помечены как model assumption и использованы для инвестиционного stress-test, а не как факт о текущей выручке компании.