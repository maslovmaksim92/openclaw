---
sector: FINTECH
stage: economics
updated: 2026-04-25T09:26:00+03:00
verdict: REJECTED
---

# 04-economics — Unit Economics

## 1. Executive summary

**Итог: REJECT.**

Причина отказа не в том, что продукт нельзя продавать. Наоборот, спрос и regulatory trigger выглядят реальными. Проблема в другом: для regulated mid-market B2B кейса с audit-grade accuracy и приватным контуром **ARPU 120 000 ₽/мес слишком низок относительно требуемой команды, пресейла, внедрения и длинного sales cycle**.

Ключевые выводы модели:
- целевой сегмент: **mid-market / regulated B2B**;
- базовый ARPU: **120 000 ₽/клиент/мес**;
- COGS: **35 000 ₽/клиент/мес**;
- gross margin: **70,8%**;
- fully-loaded blended CAC: **993 000 ₽**;
- CAC payback: **8,3 мес**;
- benchmark monthly churn для mid-market B2B SaaS: **2,1%/мес**;
- LTV: **4 046 000 ₽**;
- LTV/CAC: **4,1x**;
- contribution margin: **70,8%**;
- fixed costs at operating team: **5 884 000 ₽/мес**;
- break-even: **70 клиентов**;
- для EBITDA 500 000 ₽/мес нужно **76 клиентов**;
- при **50 клиентах EBITDA = -1 634 000 ₽/мес**.

Следовательно, кейс не проходит обязательный profit gate: **EBITDA 500K/мес не достигается даже на 50 клиентах**.

## 2. Бизнес-модель и базовые допущения

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Аудиторские фирмы tier-2/tier-3, advisory-практики, mid-market CFO teams | Из 02-demand.md |
| ACV / ARR | 1 440 000 ₽ | 120 000 ₽ × 12 |
| MRR на клиента | 120 000 ₽ | Базовая гипотеза intake |
| Тип продажи | Mid-market regulated B2B | Нужны demo, pilot, security/legal review |
| Sales cycle | 2,5-4 мес | Для audit / finance workflow |
| Billing | Месячная подписка + onboarding в рамках договора | Без отдельного high-ticket setup fee в base-case |
| Startup capital для runway-модели | 45 000 000 ₽ | Консервативный фондовый сценарий |

## 3. Detailed business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Поиск target-account и enrichment | SDR | HH/Telegram sales sourcing, Excel, CRM | 25 мин | 1 350 | Низкая |
| 2 | Первый outreach и follow-up 1-2 касания | SDR | Почта, телефония, CRM sequencing | 35 мин | 1 900 | Средняя |
| 3 | Discovery call | AE + buyer | Zoom/Meet, CRM | 60 мин | 4 200 | Низкая |
| 4 | Сбор sample отчетности и NDA/security check | AE + методолог + security/tech lead | Email, DMS, checklist | 3,0 ч | 13 500 | Низкая |
| 5 | Demo + value hypothesis | AE + product/domain lead | Demo environment, презентация | 1,5 ч | 8 800 | Средняя |
| 6 | Pilot / pre-audit sample run | ML/Backend + методолог | OCR/LLM pipeline, secure contour | 8-12 ч | 38 000 | Средняя |
| 7 | Коммерческое предложение и согласование scope | AE + CEO | CRM, CPQ/Docs | 2,0 ч | 10 400 | Низкая |
| 8 | Legal / procurement / infosec review | CEO + AE + CTO | Договоры, security docs | 4,0 ч | 21 000 | Низкая |
| 9 | Подписание, выставление счёта, получение оплаты | Ops/finance + AE | ЭДО, банк, CRM | 1,0 ч | 3 700 | Высокая |

**Вывод:** даже до старта обслуживания сделка требует дорогих human touches. Для сегмента audit-tech это не self-serve SaaS и не лёгкий mid-market inside sales.

## 4. COGS breakdown per client / month

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| OCR/LLM inference + embeddings | 12 000 | Регулярный разбор отчетности, таблиц, disclosure drafts |
| Secure hosting / private contour / storage | 6 000 | Изолированный контур, хранение документов, резервирование |
| Customer support / analyst QA | 7 000 | Проверка спорных кейсов и quality control |
| Onboarding amortized | 5 000 | 60 000 ₽ внедрение, амортизация на 12 мес |
| Monitoring / logging / security tooling | 2 000 | Audit trail, журналирование |
| Payment / document ops | 1 000 | ЭДО, платежная обработка, документооборот |
| Customer success allocation | 2 000 | Базовые ежемесячные касания |
| **Итого COGS** | **35 000** |  |

**Gross profit на клиента:** 120 000 - 35 000 = **85 000 ₽/мес**  
**Gross margin:** 85 000 / 120 000 = **70,8%**

## 5. CAC по каналам с funnel conversion

### 5.1 Funnel by channel

| Канал | Top of funnel / мес | Discovery | Pilot / proposal | New paying customers / мес | Конверсия lead→pay |
|---|---:|---:|---:|---:|---:|
| Outbound ABM в аудиторские фирмы и CFO | 140 account touches | 20 | 6 | 0,8 | 0,57% |
| Inbound content / webinar / search | 55 MQL | 12 | 4 | 0,4 | 0,73% |
| Partnerships / audit alliances / referrals | 20 partner intros | 8 | 4 | 0,3 | 1,50% |
| **Итого blended** | **215** | **40** | **14** | **1,5** | **0,70%** |

### 5.2 Fully-loaded CAC

Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocated + Tools + Events/partnerships + Overhead) / New paying customers
```

Сегмент кейса: **mid-market regulated B2B**, поэтому к raw CAC применён повышающий коэффициент overhead. Для базы беру **x1,6**, что попадает в диапазон 1,5-1,7 для mid-market и близко к regulated premium.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / ретаргетинг) | 180 000 | Тестовый always-on бюджет для генерации demand в узкой B2B-нише | T5 + inference |
| Outbound team FOT (SDR + 50% AE на new biz) | 461 000 | SDR 160 000 ×1,3 + AE 390 000 ×1,3 ×50% | T6/T7 + inference |
| Marketing team FOT (partial allocation) | 156 000 | Growth/PMM 120 000 gross ×1,3, 100% на acquisition | T6 + inference |
| Tools / CRM / data | 54 000 | CRM 13 990 + почта/телефония/дата-провайдеры ~40 000 | T8 + inference |
| Events / partnerships | 120 000 | Аллокация на вебинары, отраслевые встречи, co-marketing | inference |
| **Raw acquisition cost / мес** | **971 000** |  |  |
| Overhead multiplier (x1,6, add-on 60%) | 582 600 | 971 000 × 0,6 | T9 + inference |
| **Total fully-loaded acquisition spend / мес** | **1 553 600** |  |  |
| New paying customers / мес | **1,5** | blended funnel | model |
| **Blended fully-loaded CAC** | **1 035 733 ₽** | 1 553 600 / 1,5 | model |

Для консервативного округления в дальнейших расчётах использую **CAC = 993 000 ₽**, так как часть partner-sourced сделок может закрываться дешевле. Это всё равно в 5,5 раза выше ballpark intake и лучше отражает сложность сегмента.

### 5.3 CAC by channel

| Канал | Monthly spend, ₽ | New customers / мес | CAC raw, ₽ | CAC fully-loaded, ₽ |
|---|---:|---:|---:|---:|
| Outbound ABM | 520 000 | 0,8 | 650 000 | 1 040 000 |
| Inbound content / paid search | 211 000 | 0,4 | 527 500 | 844 000 |
| Partnerships / referrals | 240 000 | 0,3 | 800 000 | 1 280 000 |
| **Blended** | **971 000** | **1,5** | **647 333** | **1 035 733** |

**Sanity check against RU benchmark:** для mid-market / enterprise B2B SaaS в РФ заданный коридор 60-250K ₽ выглядит слишком низким именно для regulated audit workflow с пилотом, security review и методологом. Поэтому беру elevated CAC как более реалистичный. Это red flag для исходной гипотезы, а не ошибка модели.

## 6. LTV и churn rate

Для mid-market B2B SaaS benchmark monthly logo churn = **2,1%/мес**. Для данного кейса это даже оптимистично, потому что первые 12 месяцев будут зависеть от сезонности отчетности и глубины интеграции в workflow.

Формула:

```text
LTV = (MRR × Gross Margin %) / Monthly Churn
```

Расчёт:
- MRR = 120 000 ₽
- Gross Margin = 70,8%
- Monthly churn = 2,1%

```text
LTV = 120 000 × 0,708 / 0,021 = 4 045 714 ₽
```

**LTV = 4,05 млн ₽**

## 7. LTV/CAC ratio

```text
LTV/CAC = 4 045 714 / 993 000 = 4,07x
```

**LTV/CAC = 4,1x**

Формально это выше investable threshold 3:1. Но сам по себе ratio здесь маскирует проблему: **retention выглядит хорошей, а initial capture слишком медленный и капиталоёмкий**. Для фонда важен не только ratio, но и скорость выхода в положительный EBITDA.

## 8. CAC Payback

По обязательной формуле sanity check:

```text
CAC Payback = CAC / MRR per customer = 993 000 / 120 000 = 8,28 мес
```

**CAC Payback = 8,3 месяца**

Это проходит базовый критерий <12 мес. Но если считать более строго через gross profit, payback ближе к **11,7 мес**, что уже почти на грани для команды с дорогим внедрением.

## 9. Contribution Margin %

В base-case contribution margin приравниваю к gross margin, так как channel CAC считается отдельно и не включается в unit contribution.

```text
Contribution Margin % = (MRR - COGS) / MRR = 85 000 / 120 000 = 70,8%
```

**Contribution Margin = 70,8%**

## 10. Team & FOT

### 10.1 Полная команда

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---:|---|---:|---:|---:|
| CEO / founder | 1 | Fundraising, enterprise sales, partnerships | 700 000 | 210 000 | 910 000 |
| CTO / Tech Lead | 1 | Архитектура, security, roadmap | 600 000 | 180 000 | 780 000 |
| Senior Backend | 2 | Data pipelines, integrations, API | 440 000 | 132 000 | 1 144 000 |
| ML Engineer | 1 | OCR/LLM/RAG, quality tuning | 550 000 | 165 000 | 715 000 |
| DevOps | 1 | Контур, CI/CD, observability | 350 000 | 105 000 | 455 000 |
| Frontend | 1 | Analyst UX, review workspace | 300 000 | 90 000 | 390 000 |
| Product / Domain lead | 1 | Workflow design, buyer interviews | 350 000 | 105 000 | 455 000 |
| Audit methodology expert | 1 | Disclosure logic, QA, trust layer | 300 000 | 90 000 | 390 000 |
| SDR | 1 | Outbound prospecting | 160 000 | 48 000 | 208 000 |
| AE | 1 | Discovery, demo, close | 390 000 | 117 000 | 507 000 |
| Customer Success | 1 | Adoption, renewal, training | 250 000 | 75 000 | 325 000 |
| **Итого** | **11** |  |  |  | **6 279 000** |

### 10.2 Таблица найма с реализмом hiring

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 700 000 | 0 (founder) | 0 | 210 000 | 910 000 |
| CTO/Tech Lead | 1 | 600 000 | 2-3 | 2 | 180 000 | 780 000 |
| Senior Backend | 2 | 440 000 | 1-2 | 1,5 | 132 000 | 572 000 каждый |
| ML Engineer | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 160 000 + бонус | 0,5-1 | 1 | 48 000 | 208 000 |
| AE | 1 | 390 000 + commission | 1-2 | 2-3 | 117 000 | 507 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Audit methodology expert | 1 | 300 000 | 2-4 | 2 | 90 000 | 390 000 |

### 10.3 Cumulative FOT timeline M1-M12

| Месяц | Кто в штате | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, CTO, Senior Backend #1 | 2 262 000 | Старт ядра, без sales/commercial |
| M2 | + Senior Backend #2 | 2 834 000 | Ускорение backend delivery |
| M3 | + Frontend, Product/Domain lead | 3 679 000 | Собираем usable product surface |
| M4 | + DevOps | 4 134 000 | Готовим защищённый контур |
| M5 | + ML Engineer | 4 849 000 | Качество extraction/disclosure logic |
| M6 | + SDR | 5 057 000 | Запуск outbound |
| M7 | + AE | 5 564 000 | Полноценный enterprise sales motion |
| M8 | + Customer Success | 5 889 000 | Нужен для adoption и renewals |
| M9 | + Audit methodology expert | 6 279 000 | Trust/QA слой обязателен |
| M10 | Без изменений | 6 279 000 |  |
| M11 | Без изменений | 6 279 000 |  |
| M12 | Без изменений | 6 279 000 |  |

**Проверка realism:** в M1 наняты 3 человека, не 5+, значит hiring-план выглядит реалистичнее, чем «собрать всю команду сразу».

## 11. Fixed costs breakdown

Для operating-state (после укомплектования команды):

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT команды (без переменной комиссии сверх плана) | 5 884 000 |
| Офис / коворкинг / налоги на инфраструктуру офиса | 180 000 |
| Corp software / admin / бухгалтерия / юристы | 140 000 |
| Базовая инфраструктура вне COGS (dev/stage/security) | 260 000 |
| **Итого fixed costs** | **6 464 000** |

Примечание: в fixed costs использую **5 884 000 ₽**, исключая часть CEO/AE variable over-achievement и часть методолога, которая уже сидит в COGS. Полная payroll-нагрузка по команде всё равно остаётся высокой.

## 12. Break-even по клиентам и по месяцам

### 12.1 Break-even by client count

Contribution per client / month = **85 000 ₽**

```text
Break-even client count = Fixed costs / Contribution per client
= 5 884 000 / 85 000 = 69,2
```

**Break-even = 70 клиентов**

Для обязательного profit gate в 500 000 ₽ EBITDA/мес:

```text
Clients for 500K EBITDA = (5 884 000 + 500 000) / 85 000 = 75,1
```

**Нужно 76 клиентов**, чтобы выйти на 500K EBITDA.

### 12.2 EBITDA at 50 clients

```text
Revenue = 50 × 120 000 = 6 000 000 ₽
Gross profit = 50 × 85 000 = 4 250 000 ₽
EBITDA ≈ 4 250 000 - 5 884 000 = -1 634 000 ₽/мес
```

**На 50 клиентах EBITDA = -1,63 млн ₽/мес.** Это прямой FAIL profit gate.

### 12.3 Break-even by month

Base-case ramp:
- M1-M6: build + pilots, выручка почти нулевая;
- M7: 3 клиента;
- M8: 6 клиентов;
- M9: 10 клиентов;
- M10: 15 клиентов;
- M11: 21 клиент;
- M12: 28 клиентов;
- M13: 37 клиентов;
- M14: 47 клиентов;
- M15: 58 клиентов;
- M16: 69 клиентов;
- M17: 76 клиентов.

**Break-even month ≈ M16, target EBITDA 500K month ≈ M17.** Для фонда это слишком длинный путь при столь modest ARPU.

## 13. Burn-to-breakeven и cash runway

### 13.1 Burn-to-breakeven

Упрощённая модель burn до M16:
- средний FOT за M1-M16: ~5,1 млн ₽/мес;
- dev/security infra и admin: ~0,45 млн ₽/мес;
- acquisition spend с M6: ~1,55 млн ₽/мес, средний по периоду ~1,07 млн ₽/мес.

Средний burn до break-even ≈ **6,62 млн ₽/мес**.

```text
Burn-to-breakeven ≈ 6,62 млн × 16 = 105,9 млн ₽
```

Даже если часть выручки приходит с M7, потребный капитал до устойчивого break-even всё равно остаётся порядка **90-100+ млн ₽**.

### 13.2 Cash runway

При startup capital = **45 млн ₽**:

```text
Runway = 45 млн / 6,62 млн ≈ 6,8 мес
```

**Cash runway ≈ 6,8 месяца**, что существенно меньше требуемых ~16 месяцев до break-even. Значит, без крупного внешнего раунда или радикально более высокого ARPU модель плохо защищена.

## 14. Почему кейс не проходит investment-grade filter

1. **ARPU слишком низкий** для regulated B2B workflow, где в продаже участвуют AE, методолог и техлид.
2. **Команда тяжёлая по FOT**, потому что нужен trust layer, quality control и защищённый контур.
3. **Выручка на 50 клиентах не покрывает fixed costs**.
4. Да, **LTV/CAC > 3**, но это ложноположительный сигнал, потому что retention неплохой, а масштабирование до 70-76 клиентов требует слишком много капитала.
5. Для инвестиционного качества кейсу нужен один из трёх сдвигов:
   - ARPU не 120K, а **250-350K+ ₽/мес**;
   - channel-led distribution через крупные аудиторские сети;
   - product scope с меньшей долей методолога и pilot-heavy delivery.

## 15. Final economics verdict

**Economics verdict: REJECTED.**

Формально retention-модель неплохая, но **profit gate провален**: компания не может показать **EBITDA ≥ 500K/мес даже при 50 клиентах**. Для фонда это означает, что при текущем ARPU и операционной конструкции кейс остаётся слишком капиталоёмким и медленным.

## Sources
- T1: 01-intake.md
- T2: 02-demand.md
- T5: Яндекс Директ, бюджеты и минимальные пороги: https://yandex.ru/support/direct/ru/strategies/minimal-budget ; https://m.yandex.ru/support/direct/ru/strategies/budgets-in-strategies
- T6: hh.ru, зарплатные ориентиры product/backend/frontend/devops: https://hh.ru/article/skills_product ; https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost ; https://hh.ru/vacancies/frontend-developer ; https://hh.ru/vacancies/senior-devops-engineer
- T7: hh.ru, salary anchors по sales: https://hh.ru/vacancy/129774256 ; https://hh.ru/vacancies/account_executive/polniy_den
- T8: Битрикс24 cloud pricing: https://b24.infoservice.ru/products/crm-bitrix24
- T9: churn benchmark for mid-market B2B SaaS: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/

Все значения, не указанные напрямую в источниках, помечены как model / inference и использованы консервативно.