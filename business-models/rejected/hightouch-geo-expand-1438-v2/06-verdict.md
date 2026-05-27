[GEO-EXPAND] Hightouch AI Decisioning — NEAR-PASS: 65/100 | EBITDA base=1261К₽/мес через 12 мес | LTV/CAC=23,8x | Ключевое преимущество: сильная unit economics в enterprise martech | Главный риск: weak moat и слабый прямой спрос в РФ.

# 06-verdict

sector: GEO-EXPAND

## Investment committee verdict
- Статус: **NEAR-PASS**
- Нормализованный score: **65/100**
- Raw total: **97/150**
- Routing: **pipeline/rejected/**
- Gate check: **company_ebitda_potential_rub_month > 500 000 ₽/мес проходит, но approve блокируют demand/moat margin of safety**.

## Delta vs previous
- Это rerun standalone-candidate для сигнала, который ранее схлопывался в соседний кейс `warehouse-native-ai-decisioning-marketing-operator`.
- По сравнению с прошлым rejection логика не изменилась: **экономика сильная, но локальный right-to-win слабый**.
- Отличие текущего rerun: enterprise PnL и CAC дисциплина описаны лучше, поэтому кейс доходит до **NEAR-PASS**, а не до жёсткого reject по economics.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV/CAC = 23,8x`, `CAC Payback = 1,31 месяца`, `Contribution Margin = 78%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `M12 EBITDA = +1 261 000 ₽`, `EBITDA при 50 клиентах = ~12,6 млн ₽/мес`, gate выполняется. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | `прямой спрос в РФ ... практически отсутствует`, а rule-default даёт `tier_balance = 1.00` и cap `10/25`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | `рынок быстро сведёт его к дорогой add-on аналитике`, moat есть в интеграциях, но не в category control. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | `любой sales slippage на 2-3 месяца легко съедает runway`, плюс enterprise onboarding и data residency риск. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | ICP ясен: `крупный e-commerce, fintech, telecom, retail media`, а blended CAC `656K ₽` остаётся в benchmark. |

**Normalized score = round((97 × 100) / 150) = 65/100.**

## 7-factor moat framework

| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Новый клиент почти не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | DWH-мэппинг, CRM-интеграции и обученные decision flows дают умеренный lock-in. |
| Scale economies | 1 | COGS снижается умеренно, но presales/integration остаются high-touch. |
| Proprietary data / model advantage | 1 | Есть potential на first-party decision data, но нет подтверждённого dataset moat. |
| Regulatory moat | 1 | 152-ФЗ и data residency важны, но это скорее hurdle, чем уникальная лицензируемая защита. |
| Brand / distribution | 1 | Локальный бренд отсутствует, distribution ещё founder-heavy. |
| Embedded workflow | 3 | После встраивания в CRM orchestration слой становится частью ежедневного retention workflow. |

**Moat sum = 9/21. Moat score = round((9 × 25) / 21) = 11/25.**

## Investment thesis summary
Кейс выглядит как **узкий enterprise decisioning-layer поверх уже существующих CDP/CRM бюджетов**, а не как массовая новая категория в РФ. Это означает, что продукт можно построить в прибыльный niche SaaS, но для комитета не хватает margin of safety по трём направлениям: прямой локальный спрос, defensibility против Mindbox/in-house stack и repeatable GTM без founder bottleneck.

## FULL business process from 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR + RevOps | CRM, Apollo/аналог, Excel | 6 ч | 12 000 | средняя |
| 2 | Обогащение контактов и сегментация | SDR | data provider, CRM | 8 ч | 16 000 | высокая |
| 3 | Outbound sequence и follow-ups | SDR | email automation, CRM | 20 ч | 40 000 | высокая |
| 4 | Первичный discovery call | SDR + AE | Zoom, CRM | 2 ч | 12 000 | низкая |
| 5 | Qualification / ICP-fit | AE | CRM, MEDDICC template | 3 ч | 18 000 | средняя |
| 6 | Demo с use-case mapping | AE + Solutions/CTO | demo env, slides | 4 ч | 35 000 | низкая |
| 7 | Data audit / feasibility assessment | CTO + Backend | DWH schema review, docs | 10 ч | 70 000 | низкая |
| 8 | Pilot scoping + ROI model | AE + CTO + Product | spreadsheet, proposal doc | 6 ч | 42 000 | низкая |
| 9 | Security / legal / procurement | AE + founder + legal | security questionnaire, MSA | 12 ч | 65 000 | низкая |
| 10 | Коммерческое предложение и negotiation | AE + CEO | CPQ, DocuSign/аналог | 5 ч | 38 000 | низкая |
| 11 | Pilot setup / onboarding kickoff | CSM + Backend + DevOps | cloud, connectors, PM tool | 14 ч | 82 000 | средняя |
| 12 | Invoice, procurement docs, payment collection | Finance/Ops + AE | 1C/банк/ЭДО | 4 ч | 18 000 | средняя |

**Прямые трудозатраты на выигранного клиента: ~448 000 ₽.**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 15 600 000 ₽ |
| CAC | 656 000 ₽ |
| LTV/CAC | 23,8x |
| CAC Payback | 1,31 мес |
| GM / Contribution Margin | 78% |
| contribution_margin_rub_month | 390 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 929 000 ₽/мес |
| Break-even clients | 18 |
| Break-even month | M11 |
| company_ebitda_rub_month base | 1 261 000 ₽/мес через 12 мес |
| company_ebitda_potential_rub_month | 12 571 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 20 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 21 |
| months_to_1m_ebitda | 12 |
| startup_capital_to_bep_rub | ~40 800 000 ₽ |

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraising, strategic deals | 780 000 |
| CTO / Tech Lead | архитектура, presales, security review | 715 000 |
| Senior Backend #1 | connectors, pipelines, orchestration | 585 000 |
| Senior Backend #2 | activation APIs, reliability | 585 000 |
| ML Engineer | scoring, experimentation, uplift models | 585 000 |
| DevOps | infra, CI/CD, observability | 455 000 |
| Frontend | marketer UI / workflow UX | 390 000 |
| Product Manager | roadmap, ICP prioritization, ROI cases | 520 000 |
| SDR | outbound pipeline generation | 234 000 |
| AE | new business closing, negotiations | 455 000 |
| Customer Success | onboarding, expansion, renewals | 325 000 |
| **Итого** |  | **5 629 000 ₽/мес** |

## PnL и risk summary

### SECTION A: PnL
- Base-case в `05-critic.md`: **M12 EBITDA = 5 332 677 ₽/мес** при 31 клиентах, если GTM идёт строго по модели P6A.
- Более консервативный ramp из `04-economics.md`: **M12 EBITDA = 1 261 000 ₽/мес** при 21 клиенте.
- Break-even count: **18 клиентов**.
- `startup_capital_to_bep_rub`: **~40,8 млн ₽** с буфером 15%.
- На 50 клиентах `company_ebitda_potential_rub_month = 12 571 000 ₽/мес`.

### SECTION B: Risk + Monte Carlo
- `p10 EBITDA @M24 = -2 888 000 ₽/мес`, `p50 = 16 011 000 ₽/мес`, `p90 = 57 732 000 ₽/мес`.
- `Range width по LTV/CAC = 62,4x`, то есть outcome слишком чувствителен к CAC, churn и pricing discipline.
- Single-point failure из critic: **CAC x2** уводит модель в отрицательный EBITDA на горизонте 12 месяцев.

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Ozon | Крупный marketplace с heavy CRM и персонализацией, где uplift на cross-sell и retention прямо монетизируется. | email decision-maker в CRM / loyalty + founder outbound | 500 000 ₽/мес |
| 2 | Wildberries | Огромная промо- и коммуникационная база, где decision layer может оптимизировать сегментацию и частоту касаний. | партнёрство с martech/SI + founder-led intro | 500 000 ₽/мес |
| 3 | Яндекс Маркет | Зрелый data stack и постоянные сценарии recommendations / lifecycle marketing. | конференция + email head of CRM/personalization | 450 000 ₽/мес |
| 4 | X5 Group | Loyalty и omnichannel promo orchestration создают понятную боль для next-best-action decisioning. | retail-конференция + интеграторский канал | 450 000 ₽/мес |
| 5 | Магнит | Большой first-party data контур и регулярные CRM-кампании, где важна promo efficiency. | email decision-maker + партнёрство с data-интегратором | 400 000 ₽/мес |
| 6 | МТС | Телеком с развитым CRM marketing и cross-sell сценариями по большой базе. | direct outbound в CVM/CRM lead | 450 000 ₽/мес |
| 7 | МегаФон | Сильный retention motion, upsell и тарифные предложения, где нужен decision engine поверх событийных данных. | отраслевое мероприятие + founder outbound | 400 000 ₽/мес |
| 8 | Т-Банк | Высокая культура экспериментов и lifecycle-коммуникаций, где measurable uplift легко защищается перед buyer. | warm intro в growth/CRM lead + email | 500 000 ₽/мес |
| 9 | Lamoda | Fashion e-commerce с высокой зависимостью от персонализации, сегментации и reactivation сценариев. | vc.ru ad + outbound в CRM/commercial analytics | 350 000 ₽/мес |
| 10 | Детский мир | Loyalty, промо и CRM-сценарии в ритейле создают понятный wedge для personalization uplift. | retail media / conference + email decision-maker | 350 000 ₽/мес |

**Вывод по GTM:** named targets реалистичны и совпадают с ICP, но motion остаётся enterprise-heavy и founder-dependent.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| weak moat / price compression | Высокая | Высокий | Buyer может закрыть заметную часть боли через Mindbox, Retail Rocket или in-house stack и продавить premium pricing вниз. |
| enterprise CAC shock | Средняя | Высокий | В critic прямо показано, что при `CAC x2` EBITDA уходит в отрицательную зону на M12. |
| evidence_quality_unverified | Высокая | Средний | В demand-файле отсутствует строка `Sources: T1=..., T2=..., T3=...`, поэтому tier-balance по дефолту penalized. |

## Что нужно доказать для APPROVED
1. **3-5 платящих enterprise клиентов** в РФ без дисконта ниже 400-500К ₽/мес.
2. **Pilot-to-production conversion** без расползания onboarding в кастомную интеграционную фабрику.
3. **Repeatable GTM**: часть pipeline должна приходить через partners/content, а не только founder-led deals.
4. **Локальный moat**: data residency + готовые коннекторы + ROI cases, которые Mindbox/in-house не повторяют быстро.
5. **Фактический source quality uplift**: demand-стадия должна быть пересобрана с явным T1/T2/T3 breakdown.

## LTV Upside Calculator
Так как итоговый статус **NEAR-PASS**, переход в approve можно считать от трёх рычагов:

| Рычаг | Текущее значение | Целевое значение | Влияние |
|---|---:|---:|---|
| ARPA | 500 000 ₽/мес | 550 000 ₽/мес | `customer_ltv_rub` вырастает примерно до **17,16 млн ₽** при тех же GM и churn. |
| CAC | 656 000 ₽ | 520 000 ₽ | `LTV/CAC` вырастает с **23,8x** до примерно **33,0x**. |
| Contribution margin | 78% | 80% | `contribution_margin_rub_month` растёт до **440 000 ₽/мес**, а clients_to_500k_ebitda снижается до **18**. |

**Практический апсайд-сценарий:** если кейс покажет 3-5 реальных локальных клиентов с чеком **500-550К ₽/мес**, CAC ниже **520К ₽** и временем внедрения до **60-90 дней**, он может перейти в диапазон **70-73/100**.

## Proof points, которых сейчас не хватает для APPROVED
- нет прямого локального evidence, что exact-category покупается как отдельная budget line в РФ;
- нет подтверждённого proprietary data moat или явного distribution moat;
- нет доказательства, что enterprise sales motion масштабируется без founder bottleneck;
- нет source-tier breakdown, чтобы снять penalty по Market+Demand.

## Final verdict
**Решение комитета: NEAR-PASS, маршрутизация в REJECTED bucket до новых proof points.**

Кейс не режется по экономике, наоборот, client-level и company-level PnL выглядят сильно. Но для approve не хватает именно инвестиционной защищённости: спрос в РФ остаётся косвенным, moat слабый, а enterprise GTM слишком чувствителен к CAC и price compression. Возвращаться к approve имеет смысл после первых локальных paid pilots и пересборки demand evidence.
