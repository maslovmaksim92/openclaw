# RankAI, AI-first SEO/GEO white-label fulfillment
**Статус:** REJECTED
**Итоговый балл:** 53/100
**Дата:** 2026-04-19
**Сектор:** AI-SERVICES

---

## Этап 1 — Описание кейса

Исходный `00-brief.md` в кейсе отсутствовал. По совокупности `01-evidence.md`, `02-demand.md` и `04-economics.md` кейс описывается как AI-first SEO/GEO white-label fulfillment для агентств и SMB с фокусом на recurring B2B delivery.

## Этап 2 — Проверка спроса

Из `02-demand.md`:
- Статус: **CONDITIONAL PASS**.
- Search-demand: **LOW**.
- TAM / SAM / SOM: **36 млрд ₽ / 4,32 млрд ₽ / 50,4 млн ₽**.
- Позитив: есть WTP и подтверждённые substitute-рынки white-label SEO.
- Негатив: отсутствует строка `Sources: T1/T2/T3`, нет жёсткой tier-верификации, локальный спрос в РФ подтверждён косвенно.

## Этап 3 — Evidence

Из `01-evidence.md`:
- RankAI Agency и Y Combinator подтверждают white-label модель для агентств.
- RankAI декларирует resale economics в диапазоне **$2 000–6 000/мес** в США и более дешёвую autonomous-модель.
- Value proposition основан на радикальном снижении стоимости SEO/GEO-операций.

## Этап 4 — Unit Economics

Из `04-economics.md`:
- customer_ltv_rub: **4 187 616 ₽**
- Fully-loaded CAC: **284 160 ₽**
- LTV/CAC: **14,7x**
- CAC payback: **2,37 мес**
- contribution_margin_rub_month: **88 000 ₽/клиент/мес**
- fixed_costs_rub_month: **6 557 000 ₽/мес**
- Break-even: **38 клиентов в lean-mode / 75 клиентов steady-state**
- company_ebitda_potential_rub_month @ 50 клиентов в lean-mode: **1 056 000 ₽/мес**

## Этап 5 — Critic / Finance

Из `05-critic.md`:
- company_ebitda_rub_month base M12: **-1 846 102 ₽/мес**
- startup_capital_to_bep_rub base: **31 474 202 ₽**
- Monte Carlo Lite: **p50 EBITDA @M24 = 384 805 ₽/мес**, что ниже инвестиционного порога **500К₽/мес**.
- Главные риски: founder dependency, price compression, LLM/API dependency, санкционные и vendor risks.

## Этап 6 — Финальный вердикт

### Investment one-liner
[AI-SERVICES] RankAI — REJECTED: 53/100 | EBITDA base=-1846К₽/мес через 12 мес | LTV/CAC=14,7x | Ключевое преимущество: сильная unit economics на агентском white-label чеке | Главный риск: weak moat и недоказанная repeatable прибыль компании.

### Scorecard

| # | Критерий | Вес | Raw (0-25) | Обоснование |
|---|----------|-----|------------|-------------|
| 1 | Unit Economics | 25 | 20 | Сильные LTV/CAC, payback и margin по данным `04-economics.md`. |
| 2 | EBITDA Potential | 25 | 13 | Base-case и median-case не подтверждают устойчивый проход порога 500К₽/мес. |
| 3 | Market + Demand | 25 | 10 | Спрос коммерчески есть, но локальная evidence-база в РФ слабая и без tier-строки. |
| 4 | Moat | 25 | 9 | Moat в основном операционный, а не структурный. |
| 5 | Execution Risk | 25 | 14 | Много high/high рисков по delivery, санкциям, зависимости от LLM и founder-led GTM. |
| 6 | GTM Realism | 25 | 14 | ICP реалистичный, но sales motion тяжёлый и масштабирование пока не repeatable. |

**Raw total:** 80/150  
**Normalized:** 53/100

### Почему REJECTED
1. Экономика одного клиента сильная, но компания не показывает достаточно надёжный путь к EBITDA 500К₽/мес в base/median-case.
2. Moat слабый, а narrative GEO/SEO легко копируется конкурентами и агентствами in-house.
3. Качество demand-evidence для РФ недостаточно сильное для investment committee уровня.

### Что должно быть доказано для relaunch
- 3-5 платящих агентств в РФ с контрактами **120-180К₽/мес**.
- churn не выше **2,5%/мес**.
- company_ebitda_rub_month **>= 500К₽/мес** в lean-mode при **<= 50 клиентах**.
- стандартизированный white-label dashboard и delivery playbook как доказательство moat.

### GitHub verdict
Этот кейс сохранён как rejected из-за расхождения между сильной unit economics клиента и недоказанной устойчивостью экономики компании.
