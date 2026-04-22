[GEO-EXPAND] Listen Labs GEO Expand v2 — APPROVED with notes: 70/100 | EBITDA base=698К₽/мес через 24 мес | LTV/CAC=10,7x | Ключевое преимущество: research OS для регулярных customer interviews | Главный риск: weak moat и price compression.

# 06-verdict — Listen Labs GEO Expand v2

sector: GEO-EXPAND
status: APPROVED
score: 70/100
normalized_from_raw: 105/150
case_slug: listen-labs-geo-expand-v2
updated_at: 2026-04-22 05:39 MSK

## Инвесткомитет: итоговый вердикт

Listen Labs проходит в APPROVED only with notes. Экономика в базе уже собирается в фондовый кейс: в `04-economics.md` зафиксированы `LTV/CAC = 10.7x`, `Gross Margin = 54.5%`, `contribution_margin_rub_month = 105 000 ₽/клиент/мес`, а в `05-critic.md` median Monte Carlo даёт `EBITDA @M24 = 698 068 ₽/мес`. Компания также проходит обязательный gate по масштабу: при 50 клиентах модель даёт `company_ebitda_potential_rub_month ≈ 2 188 000 ₽/мес`, а выход к `500k EBITDA` ожидается примерно за `18-22 месяца`, то есть внутри лимита `≤50 клиентов и ≤24 мес`.

Но approve здесь не “чистый”. Это не PLG SaaS и не широкий рынок. В `02-demand.md` прямой keyword-demand слабый, а рабочий wedge найден только в соседней budget line `исследование клиентов`; в `05-critic.md` p10 по Monte Carlo остаётся отрицательным (`-784 970 ₽/мес`), а moat слабый. Поэтому комитет одобряет кейс как узкий enterprise / upper-midmarket bet на research operating system, а не как массовый self-serve продукт.

## Delta vs previous

- В исходном triage от 2026-04-17 кейс был отклонён до пайплайна из-за предположения, что локальный LTV «не превышает порог 500 тыс. ₽ в месяц».
- Полный rerun P3→P7 показал обратное: threshold нужно проверять не по MRR на клиента, а по `company_ebitda_rub_month` и `company_ebitda_potential_rub_month`.
- После economics/finance выяснилось, что модель даёт `company_ebitda_potential_rub_month ≈ 2.19 млн ₽/мес` при 50 клиентах и median `698К ₽/мес` на M24.
- Итог: triage был слишком ранним и спутал ARPA с прибыльностью компании.

## Оценка

Source tier balance: T1=3, T2=6, T3=0, weighted=2.33. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | В 04-economics.md: «Base-case LTV/CAC = 10.7x», «Practical payback = ~8-10 месяцев», «Gross Margin = 54.5%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В 05-critic.md: «p50 EBITDA @M24 = 698 068 ₽/мес», а в 04-economics.md «к operating break-even можно выйти примерно в M18-M22». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | В 02-demand.md: «`исследование клиентов` ... MEDIUM / 30, HH vacancies = 5250», но по tier-balance применён штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | В 05-critic.md: «главный battlefront не против одного чемпиона, а против bundle из survey + agency + internal research team». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | В 05-critic.md: «русское AI-moderation даёт слабое качество инсайтов», «зависимость от LLM API», но это mitigatable через локализацию и fallback stack. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | В 04-economics.md blended CAC = «750 000 ₽», founder-led network даёт CAC «420 000 ₽», а buying ICP уже указан как Head of Research / CPO / CX lead. |

**Sum raw = 105/150**  
**Normalized score = round((105 × 100) / 150) = 70/100**

## Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | После настройки taxonomy, repository и governance возникает умеренная инерция перехода. |
| Scale economies | 1 | COGS частично падает на объёме, но сервисный research-ops слой остаётся заметным. |
| Proprietary data / model advantage | 1 | Repository интервью и сценариев полезен, но в материалах нет доказанного уникального датасета мирового масштаба. |
| Regulatory moat | 1 | Data residency и 152-ФЗ создают friction для новых игроков, но не формируют жёсткую лицензионную защиту. |
| Brand / distribution | 1 | В РФ бренда нет, продажи придётся строить аккаунтно. |
| Embedded workflow | 3 | Если продукт становится monthly insight cycle и research repository, он садится глубоко в product/research workflow. |

**Moat raw = 9/21, Moat score = round((9 × 25) / 21) = 11/25.** Это не weak moat по формальному порогу `<10`, но moat остаётся нижней границей approve.

## Investment one-liner

`[GEO-EXPAND] Listen Labs GEO Expand v2 — APPROVED with notes: 70/100 | EBITDA base=698К₽/мес через 24 мес | LTV/CAC=10,7x | Ключевое преимущество: research OS для регулярных customer interviews | Главный риск: weak moat и price compression.`

## Сводка по стадиям 01-05

### Stage 01 — Intake
- Кейс поднят как `resurrect`, потому что исходный triage не запускал полный пайплайн.
- Исходная гипотеза: западный category signal сильный, но локальный high-LTV порог под вопросом.

### Stage 02 — Validation / Demand
- Прямой keyword `пользовательские интервью` дал только `LOW / 15`.
- Более широкая budget line `исследование клиентов` дала `MEDIUM / 30`, `HH vacancies = 5250`, `Yandex Suggest = 100`.
- Итог: не массовый спрос, но есть enterprise budget на customer research / UX insights.

### Stage 03 — Demand / Market sizing
- Proxy-TAM РФ: `1.83 млрд ₽`, SAM: `640 млн ₽`, preferred SOM Y1: `16.1 млн ₽`, SOM Y3: `53.6 млн ₽`.
- Buyer universe около `620` потенциальных buyers, из них около `40%` выглядят адресуемыми.

### Stage 04 — Economics
- ARPA: `220 000 ₽/мес`, COGS: `100 000 ₽/мес`, gross profit: `120 000 ₽/мес`, contribution_margin_rub_month: `105 000 ₽/мес`.
- `customer_ltv_rub ≈ 7 993 333 ₽`, `LTV/CAC = 10.7x`, practical payback `~8-10 мес`.
- При `50 клиентах` модель даёт `company_ebitda_rub_month ≈ 2.188 млн ₽/мес`.

### Stage 05 — Critic / Finance risk
- Base PnL в 12 месяцев остаётся отрицательным, но M24 медиана выходит в плюс.
- Monte Carlo Lite: `p10 EBITDA @M24 = -784 970 ₽/мес`, `p50 = 698 068 ₽/мес`, `p90 = 4 012 177 ₽/мес`.
- Главные уязвимости: price compression, churn x2, LLM dependence, длинный sales cycle.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 7 993 333 ₽ |
| CAC blended fully-loaded | 750 000 ₽ |
| LTV/CAC | 10.7x |
| CAC Payback | 3.41 мес по MRR / 6.25 мес по gross profit / практический 8-10 мес |
| Gross Margin | 54.5% |
| contribution_margin_rub_month | 105 000 ₽/клиент/мес |
| fixed_costs_rub_month | 3 062 000 ₽/мес |
| company_ebitda_rub_month, M12 base | -1 304 947 ₽/мес |
| company_ebitda_potential_rub_month | 2 188 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 34 |
| months_to_500k_ebitda | 18-22 |
| clients_to_1m_ebitda | 39 |
| months_to_1m_ebitda | 20-24 |
| Break-even | 29.2 клиента по contribution; практический operating break-even около 18-22 клиентов в более дорогом mix |
| startup_capital_to_bep_rub | 45 000 000–60 000 000 ₽ |

## Полный business process из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping и список продуктовых команд | Founder + SDR | manual research, HH, сайт, LinkedIn-like sources | 2 ч | 3 500 | Низкий |
| 2 | Outreach / intro / first meeting | Founder + AE | почта, Telegram, созвоны | 3 ч | 8 000 | Низкий |
| 3 | Discovery по pain и current workflow | AE + solutions | call, audit checklist | 3 ч | 12 000 | Низкий |
| 4 | Demo + pilot design | AE + solutions + PM | demo workspace | 4 ч | 18 000 | Средний |
| 5 | Security / legal / procurement | founder + ops | договор, DPA, security FAQ | 5 ч | 20 000 | Низкий |
| 6 | Setup workspace + taxonomy | implementation | templates, prompts, permissions | 6 ч | 25 000 | Средний |
| 7 | Research ops onboarding | CSM | enablement sessions | 5 ч | 18 000 | Средний |
| 8 | First monthly insight cycle | CSM + analyst | QA, reporting | 6 ч | 22 000 | Средний |
| 9 | Billing / docs | ops | invoice, acts | 1 ч | 2 500 | Высокий |

## Финансовая траектория

| Scenario | EBITDA break-even month | EBITDA @M12 | EBITDA @M24 | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Optimistic | M14 | -446 368 ₽/мес | ~4 012 177 ₽/мес | ~22 849 114 ₽ |
| Base | M20 | -1 304 947 ₽/мес | 698 068 ₽/мес | ~31 105 813 ₽ по SECTION A cash-model, practical buffer 45-60 млн ₽ |
| Pessimistic | M25 | -1 915 209 ₽/мес | отрицательный | ~41 126 595 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-784 970 ₽/мес**
- p50 EBITDA @M24 = **698 068 ₽/мес**
- p90 EBITDA @M24 = **4 012 177 ₽/мес**
- Вывод: approve возможен только при discipline по pricing, retention и локализации delivery.

## Команда

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / GM | 1 | 350 000 | 0 | 0 | 105 000 | 455 000 |
| AE / sales | 1 | 220 000 | 1.5 | 2 | 66 000 | 286 000 |
| PM / product owner | 1 | 260 000 | 1.5 | 1 | 78 000 | 338 000 |
| ML / applied AI | 1 | 320 000 | 2 | 1.5 | 96 000 | 416 000 |
| Full-stack engineer | 1 | 250 000 | 1.5 | 1.5 | 75 000 | 325 000 |
| Research ops / implementation | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| CSM / analyst | 2 | 170 000 | 1 | 1 | 51 000 | 442 000 |
| Marketing / content | 0.5 | 120 000 | 1 | 1 | 36 000 | 78 000 |
| Finance / ops / legal admin | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 78 000 |
| **Итого** | **9.0** |  |  |  |  | **2 652 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Большая product/research функция, регулярные customer interviews и CX backlog подтверждаются масштабом digital-команд | email decision-maker / warm intro в CPO/CX | 320 000 ₽/мес |
| Альфа-Банк | В 02-demand.md банк фигурирует как buyer-class с живой research-функцией и высокой ценой product-insight ошибок | founder-led outreach + конференция | 280 000 ₽/мес |
| Банк Уралсиб | Упомянут в HH/job-signal блоке как рынок с реальной research-компетенцией | direct email Head of Research / UX | 220 000 ₽/мес |
| МТС | Большой B2C digital footprint, регулярные исследования клиентского опыта и тарифных сценариев | партнёрство с research agency + enterprise outreach | 300 000 ₽/мес |
| Ozon | Высокий volume product-discovery и UX research в e-commerce, где time-to-insight критичен | ABM outreach в CX/product research | 300 000 ₽/мес |
| Avito | Product-led marketplace с постоянной потребностью в качественных customer interviews и repository инсайтов | founder intro + event networking | 260 000 ₽/мес |
| VK | Широкий набор digital-продуктов и рекламных/социальных сценариев требует регулярного user research | direct outreach в product excellence / research ops | 250 000 ₽/мес |
| Яндекс / Яндекс Еда | Большой поток product-гипотез, где AI synthesis может уменьшить cycle-time исследований | email decision-maker + профильная конференция | 320 000 ₽/мес |
| Magnit Tech | В 02-demand.md фигурирует в HH signal, что подтверждает внутреннюю product/research maturity | партнёрский заход через CX/retail tech integrator | 220 000 ₽/мес |
| MANGO OFFICE | Упомянут как работодатель с research-функцией, mid-market enterprise ICP с более коротким procurement path | email Head of Product / CX | 180 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Weak moat и замена bundle-ом survey + agency + internal team | high | high | В 05-critic.md прямо сказано, что главный battlefront идёт против связки заменителей, а не против одного игрока. |
| Price compression / discounting | high | high | В sensitivity analysis «Price -30%» ухудшает EBITDA @M12 до `-2 408 227 ₽/мес`, это самый болезненный shock. |
| Качество русского AI-moderation и зависимость от LLM stack | high | high | В risk matrix отмечено: «клиенты просят ручную перепроверку >50% интервью» и возможны outages / рост cost per interview. |

## Что нужно доказать для сохранения APPROVED-статуса

1. Минимум **3-5 платящих design partners** в ICP с чеком **≥220К ₽/мес** и monthly insight cadence, а не разовыми исследованиями.
2. Подтверждение, что **pilot-to-paid ≥ 30%**, а blended CAC удерживается **≤750К ₽**.
3. Реальные кейсы, где AI moderation на русском снижает cycle-time исследований без массовой ручной перепроверки.
4. Contract evidence, что к **18-22 месяцам** путь к `500К EBITDA` не требует раздувания COGS выше модели.

## Финальное решение инвесткомитета

**APPROVED with notes.**

Approve основан на том, что company-level economics проходит fund threshold, а median risk-case всё же выводит компанию к `>500К EBITDA/мес` в пределах 24 месяцев. Но это approve нижней границы. Если pricing просядет, churn вырастет или RU moderation окажется слишком ручным, кейс быстро скатится в near-pass. Значит инвестировать можно только при жёсткой дисциплине: enterprise ICP, data-residency story, hybrid human-in-the-loop QA и фокус на repeatable research cadence, а не на ad-hoc projects.
