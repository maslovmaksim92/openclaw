[GEO-EXPAND] Linq — NEAR-PASS: 68/100 | EBITDA base=1494К₽/мес через 12 мес | LTV/CAC=25,2x | Ключевое преимущество: enterprise orchestration layer поверх multi-channel support | Главный риск: weak moat и хрупкая pricing power.

# 06-verdict — Linq

sector: GEO-EXPAND

## Investment committee verdict
- **Название:** Linq
- **Slug:** `linq-geo-expand-v2`
- **Вердикт:** **NEAR-PASS**
- **Normalized score:** **68/100**
- **Raw score:** **102/150**
- **Статус по порогу:** score < 70, поэтому кейс уходит в `rejected/`, несмотря на прохождение EBITDA-gate.
- **Решение IC:** возвращать к approve-review только после доказательства repeatable premium GTM в 2-3 вертикалях РФ и улучшения moat.

## Executive summary
Linq собирает сильную клиентскую экономику только в узком enterprise-сценарии: **MRR 600 000 ₽/клиент/мес, customer_ltv_rub 21,99 млн ₽, LTV/CAC 25,2x, break-even 17 клиентов**. На уровне компании **company_ebitda_rub_month = 1 493 781 ₽/мес к M12 в base**, а порог **500 тыс. ₽/мес** проходится уже примерно на **18 клиентах**. Но investment committee не даёт approve из-за комбинации трёх факторов: **weak moat**, **sales-led demand с tier-penalty по evidence**, и **хрупкий premium pricing**, при котором даже price -30% переводит модель в отрицательный EBITDA-case.

## Delta vs previous
- Исторический triage отклонил сигнал на intake-этапе из-за предположительно недостаточного monthly LTV для локального кейса.
- Повторный rerun показал, что в enterprise-only конфигурации **customer_ltv_rub** уже не проблема: он доходит до **21,99 млн ₽**, а LTV/CAC = **25,2x**.
- Однако rerun всё равно не довёл кейс до approve, потому что новые этапы P6-P7 сильнее штрафуют **качество спроса, moat и downside-variance**.

## Оценка
Source tier balance: T1=4, T2=7, T3=1, weighted=2.25. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 25.2x», «CAC payback = 1.46 мес», «Gross margin: 73.3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «EBITDA @M12 = 1 493 781 ₽/мес», «500k EBITDA достигается уже примерно на 18 клиентах». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | «composite_demand=LOW», но есть «hh_vacancies=86» и «SAM ≈ 1.73-1.86 млрд ₽»; применён tier-penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | «Telegram сам по себе не является moat», рабочая защита только через orchestration, интеграции и SLA. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | В risk matrix сразу несколько high-risk пунктов: «санкции», «зависимость от внешних LLM/API», «data residency». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | Есть узкий, но реалистичный enterprise motion: «2 new paying customers / мес», пилот 4-6 недель, 10 named targets ниже. |

**Normalized score = round((102 × 100) / 150) = 68/100.**

## Moat — 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | После интеграции в CRM, routing и support stack стоимость переключения уже заметная. |
| Scale economies | 1 | Есть умеренный эффект масштаба по infra и support, но channel fees остаются значимыми. |
| Proprietary data / model advantage | 1 | Продукт работает на operational data, но в кейсе нет сильного доказанного dataset advantage. |
| Regulatory moat | 0 | Compliance важен, но собственный лицензируемый moat в РФ не доказан. |
| Brand / distribution | 1 | Глобальный сигнал сильный, но локального distribution moat в РФ нет. |
| Embedded workflow | 3 | При удачном rollout слой orchestration встраивается глубоко в customer-communication workflow. |

**Moat score = round((8 × 25) / 21) = 10/25.**

### Интерпретация moat
Moat остаётся **weak moat**. Кейс защищается не сетью и не regulatory capture, а только глубиной интеграции и сложностью замены после продакшн-rollout. Этого недостаточно для approve без дополнительных доказательств distribution и pricing power.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 21 990 000 ₽ |
| fully_loaded_cac_rub | 873 600 ₽ |
| LTV/CAC | 25.2x |
| CAC payback | 1.46 мес по MRR / 1.99 мес по gross profit |
| Gross Margin | 73.3% |
| contribution_margin_rub_month | 420 000 ₽/клиент/мес |
| Contribution Margin % | 70.0% |
| company_ebitda_rub_month (base M12) | 1 493 781 ₽/мес |
| EBITDA potential gate | >500 000 ₽/мес на ~18 клиентах |
| Break-even | 17 клиентов |
| startup_capital_to_bep_rub | 34 381 826 ₽ |
| Startup capital | 45 000 000 ₽ |
| clients_to_500k_ebitda | 18 |
| months_to_500k_ebitda | 10-12 мес |

## FULL business process from 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам, страховым, e-commerce | SDR | HH, Data Insight, CRM, таблицы | 25 мин/account | 520 | средняя |
| 2 | Enrichment контактов owner'ов CX / Support / Product / CTO | SDR | CRM, enrichment, Telegram/email search | 20 мин/account | 420 | средняя |
| 3 | Холодный outreach, 5-7 касаний | SDR | sequencer, телефония, email, CRM | 35 мин/account | 730 | высокая |
| 4 | Qualification call | SDR | Meet, CRM, notes AI | 30 мин/SQL | 630 | средняя |
| 5 | Discovery по текущему communication stack | AE | Meet, deck, ROI template | 60 мин | 1 900 | низкая |
| 6 | Solution scoping и channel map | AE + Solutions Engineer | Notion, API docs, architecture board | 3 ч | 7 600 | низкая |
| 7 | Demo и walkthrough orchestration layer | AE + CTO | sandbox, docs, demo tenant | 90 мин | 4 800 | низкая |
| 8 | Security / legal / compliance review | CTO + CEO + юрист | docs, ЭДО, security answers | 6 ч | 15 500 | низкая |
| 9 | Пилот на 4-6 недель с 1-2 use cases | CSM + Backend + DevOps | API, monitoring, staging | 18 ч | 38 000 | средняя |
| 10 | Коммерческое предложение, SLA, pricing commit | AE + CEO | CRM, pricing sheet, docs | 2 ч | 5 100 | низкая |
| 11 | Подписание договора и procurement | AE + finance/ops | Диадок, банк, 1С | 5-10 раб. дней цикла | 3 500 | средняя |
| 12 | Выставление счёта и первая оплата | finance/ops | банк-клиент, ЭДО | 20 мин | 350 | высокая |
| 13 | Production onboarding и rollout | CSM + Backend + DevOps | API keys, routing, monitoring | 10-14 ч | 24 000 | средняя |
| 14 | Ежемесячный review, usage true-up, upsell | CSM + AE | BI, CRM, usage dashboard | 90 мин/мес | 4 000 | средняя |

### Вывод по процессу
Это не PLG и не self-serve SaaS. Полноценная продажа Linq в РФ выглядит как **pilot-heavy enterprise motion** с обязательными security review, интеграциями и managed onboarding. Именно поэтому fully-loaded CAC здесь важнее media CAC.

## Team table

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO / Founder | enterprise sales, fundraising, key accounts | 910 000 |
| CTO / Tech Lead | архитектура, security, channel reliability | 715 000 |
| Senior Backend #1 | core API, routing, webhooks | 585 000 |
| Senior Backend #2 | billing, connectors, retries | 585 000 |
| ML Engineer | agent routing, summarization, evals | 650 000 |
| DevOps | infra, monitoring, CI/CD, SRE | 455 000 |
| Frontend | operator console, admin, analytics UI | 390 000 |
| SDR | outbound prospecting | 234 000 |
| AE | discovery, demos, closing | 455 000 |
| Customer Success | onboarding, retention, QBR | 338 000 |
| Solutions Engineer | pilots, integration scoping | 416 000 |
| Product Marketing Manager | category education, inbound, cases | 247 000 |
| Finance / Ops | invoicing, contracts, reporting | 182 000 |
| **Итого full team FOT** |  | **6 162 000 ₽/мес** |

## Top-3 risks

| Риск | Probability | Impact | Почему в top-3 |
|---|---|---|---|
| weak_moat_and_price_compression | high | high | В P6B «Price -30%» даёт **EBITDA @M12 = -1 940 038 ₽**, то есть pricing power критична для выживания. |
| sanctions_and_vendor_dependency | high | high | В risk matrix прямо указаны «санкции», «ограничение API» и «зависимость от внешних LLM/API и routing vendors». |
| evidence_quality_unverified | medium | high | Tier balance = 2.25, primary basis T2, direct demand в РФ остаётся LOW и penalized. |

## GTM — 10 named targets

| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Огромный multi-channel support и notifications, высокая цена ошибки в routing и uptime. | intro через интегратора / email decision-maker в CX или digital support | 900 000 ₽/мес |
| 2 | ВТБ | Банковский volume, compliance-heavy support и потребность в audit trail. | конференция + партнёрство с contact-center интегратором | 800 000 ₽/мес |
| 3 | Альфа-Банк | Сильный digital banking, много клиентских сценариев в push/chat/voice. | founder-led outbound к head of CX / product owner messaging | 850 000 ₽/мес |
| 4 | Т-Банк | Высокий message volume и AI-friendly продуктовая культура. | тёплое интро через fintech ecosystem / email decision-maker | 900 000 ₽/мес |
| 5 | Совкомбанк | Много операций поддержки и уведомлений, нужен стабильный orchestration layer. | партнёрство с SI и security-led workshop | 700 000 ₽/мес |
| 6 | Ингосстрах | Страховые customer journeys длинные, много статусов и документных касаний. | email head of service + отраслевой ивент по страхованию | 650 000 ₽/мес |
| 7 | АльфаСтрахование | Высокая ценность SLA и омниканального routing для claims/support. | партнёрство с CX-консультантом / точечный ABM | 650 000 ₽/мес |
| 8 | Ozon | Массовые клиентские обращения, post-purchase коммуникации и продавеческая поддержка. | outbound к VP customer experience / marketplace ops | 1 000 000 ₽/мес |
| 9 | Wildberries | Очень большой inbound support volume, высокая боль в асинхронных каналах. | через integrator partner / конференция e-commerce ops | 1 000 000 ₽/мес |
| 10 | Яндекс Маркет | Сложный marketplace workflow, много каналов и internal tooling. | founder-led outbound + product/demo workshop | 850 000 ₽/мес |

### GTM-комментарий
Список таргетов узкий, но реалистичный. Все 10 компаний совпадают с buyer universe из demand-stage и действительно могут платить **600k+ ₽/мес** за orchestration layer, если Linq продаёт не API-ключ, а outcome + SLA + managed rollout.

## Proof points, которые нужны для approve
1. **3-5 paid pilots** в РФ/CIS с чеком не ниже **600 000 ₽/мес** и переходом pilot → production.
2. Подтверждение, что **logo churn ≤ 2%/мес** удерживается не только в base-модели, но и на реальных локальных клиентах.
3. Доказательство, что **price discount >20%** не требуется для закрытия банка, страховщика или top e-commerce.
4. Наличие хотя бы **1-2 partner channels** с repeatable pipeline, а не только founder-led closing.
5. Реальный локальный security/compliance package, снимающий возражения по **152-ФЗ, residency и санкционным зависимостям**.

## Monte Carlo / downside readout
- **p10 EBITDA @M24 = -4,25 млн ₽/мес**
- **p50 EBITDA @M24 = 10,01 млн ₽/мес**
- **p90 EBITDA @M24 = 20,65 млн ₽/мес**
- **Range width по LTV/CAC = 35,6**

Вывод: median-case хороший, но левый хвост слишком тяжёлый для approve. Это и есть основная причина, почему кейс остаётся **NEAR-PASS**, а не переходит в approve-with-notes.

## LTV Upside Calculator

| Рычаг | Текущее значение | Upside-case | Эффект |
|---|---:|---:|---|
| ARPA / MRR | 600 000 ₽ | 750 000 ₽ | Повышает customer_ltv_rub и снижает риск price-shock. |
| Monthly churn | 2.0% | 1.5% | Даёт LTV ≈ 36.65 млн ₽ при той же GM. |
| Gross Margin | 73.3% | 76% | Увеличивает contribution и ускоряет company EBITDA. |
| Fully-loaded CAC | 873 600 ₽ | 700 000 ₽ | Повышает LTV/CAC с 25.2x до 31.4x при базе. |
| Clients @M12 | 19.1 | 22+ | Сдвигает запас EBITDA вверх и уменьшает downside. |

### Условный upside-вывод
Если Linq докажет **MRR 700-750 тыс. ₽**, **CAC ≤ 700 тыс. ₽** и **churn ≤ 1.5%**, этот же кейс может перейти из **68/100** в диапазон **72-75/100**. То есть NEAR-PASS здесь обратим, но только при строгом подтверждении premium GTM.

## Final verdict
**Linq = NEAR-PASS (68/100).**

Кейс уже проходит unit economics и company EBITDA-gate, но пока не проходит investment committee по качеству рынка и защищённости модели. В текущем виде это **selective enterprise bet with strict kill-switches**, а не approve-case. Формально кейс уходит в `rejected/`, но по содержанию это кандидат на возврат после локальных pilot proofs.
