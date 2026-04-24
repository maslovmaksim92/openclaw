# 06-verdict

[GEO-EXPAND] Hilbert — NEAR-PASS: 69/100 | EBITDA base=2062К₽/мес через 12 мес | LTV/CAC=33.1x | Ключевое преимущество: strong unit economics на enterprise ICP | Главный риск: premium wedge против Mindbox/CDP substitutes пока не доказан.

## Вердикт
**NEAR-PASS**

sector: GEO-EXPAND

## Investment committee summary
Hilbert проходит финансовый gate и показывает редкую силу по unit economics, но пока не дотягивает до approve из-за двух факторов: слабый локальный moat и недостаточно доказанный repeatable GTM в РФ. Это не reject по экономике, а reject по margin of safety. Если команда подтвердит 2-3 design partners из приоритетного ICP и покажет, что product продаётся как uplift-layer поверх текущего стека, кейс может быстро перейти в approve.

## Delta vs previous
- Против раннего вердикта `0657-msk-hilbert-geo-expand-v2` score вырос с **0/100** до **69/100**: появился полный economics + P6A/P6B, подтверждён путь к EBITDA > 500k ₽/мес.
- Но итог всё ещё ниже approve, потому что новый разбор подтвердил старый core-risk: бюджет ownership в РФ уже сидит у Mindbox/CDP/CRM incumbents, а отдельный premium decisioning-layer пока не доказан.
- По качеству сопоставимых кейсов Hilbert попадает в тот же near-pass кластер, что и `warehouse-native-ai-decisioning-marketing-operator-v2` (**69/100**) и `1048-msk-hightouch-geo-expand-v2` (**66/100**).

## Оценка
Source tier balance: T1=6, T2=3, T3=1, weighted=2.50. Penalty applied: 0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 23 | `LTV/CAC = 33.1x`, `Gross Margin = 75.6%`, `Gross profit payback = 2.02 мес` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 22 | `M12 EBITDA = 2 061 845 ₽/мес`, `Base | M10 | 30 951 465` и `EBITDA break-even month M10` в 05-critic.md. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | `маркетинговая аналитика ... MEDIUM / 30 с 5008 вакансиями`, но `customer data platform ... LOW / 18 с 28 вакансиями` в 02-demand.md. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | `retention через data lock-in, custom connectors и workflow embedding` есть, но `главная угроза ... budget capture со стороны Mindbox/CDP/CEP incumbents` в 04/05. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 13 | `Founder-led sales не масштабируется`, `152-ФЗ / data residency`, `vendor lockout` и `services creep` помечены high/med-high в risk matrix. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | `lead→paid 1.5%`, `blended CAC 685 957 ₽`, но enterprise motion длинный и требует `paid pilot only` и founder-led ABM. |

**Сумма raw:** 103/150  
**Normalized score:** **69/100**

### Интерпретация шкалы
- 0-5 = отсутствует или катастрофа
- 6-10 = ниже investment-grade
- 11-15 = минимально приемлемо
- 16-20 = хорошо, investment-ready
- 21-25 = выдающееся

## 7-factor Moat framework

| Фактор | Балл (0-3) | Почему |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт автоматически для остальных; shared network effect не доказан. |
| Switching costs | 3 | Коннекторы, data workflows, weekly reviews и embedding в CRM/growth-процессы создают высокий switching cost. |
| Scale economies | 2 | COGS на клиента умеренный, а GTM и delivery улучшаются с объёмом, но не до winner-take-all. |
| Proprietary data / model advantage | 1 | Есть накопление account-specific data, но размер уникального датасета и model edge не подтверждены T1/T2-источником. |
| Regulatory moat | 1 | Есть security/compliance слой и 152-ФЗ friction, но это скорее bar-to-entry, чем сильный лицензионный moat. |
| Brand / distribution | 1 | Глобальный сигнал сильный, но локального бренда и распределения в РФ нет. |
| Embedded workflow | 3 | Продукт глубоко сидит в decision loops growth/CRM/analytics и weekly business review. |

**Moat sum:** 11/21  
**Moat score:** **13/25**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 22 680 000 ₽ |
| CAC blended | 686 000 ₽ |
| LTV/CAC | 33.1x |
| CAC payback (gross profit) | 2.02 мес |
| Gross Margin | 75.6% |
| contribution_margin_rub_month | 313 000 ₽/клиент/мес |
| fixed_costs_rub_month | 5 862 000 ₽/мес |
| company_ebitda_rub_month (base M12) | 2 061 845 ₽/мес |
| company_ebitda_potential_rub_month (p50 M24) | 11 908 728 ₽/мес |
| clients_to_500k_ebitda | 21 |
| clients_to_1m_ebitda | 22 |
| months_to_500k_ebitda | 11 |
| months_to_1m_ebitda | 11 |
| EBITDA break-even clients | 19 |
| startup_capital_to_bep_rub | 30 951 465 ₽ |
| EBITDA @ 50 clients | 11 138 000 ₽/мес |

## Полный бизнес-процесс

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по top B2C buyers | SDR | HH, Rusprofile, CRM, ручной ресерч | 2.0 ч | 1 900 | Низкий |
| 2 | Обогащение контактов и гипотезы use case | SDR | CRM, enrichment tools, LinkedIn/аналог | 1.5 ч | 1 450 | Средний |
| 3 | Персонализированный outreach | SDR | Email sequencing, Telegram, phone | 2.0 ч | 1 900 | Средний |
| 4 | Qualification / first call | SDR + AE | Meet, CRM | 1.0 ч | 3 250 | Средний |
| 5 | Discovery по data stack и growth pain | AE + founder | Meet, questionnaire, ROI sheet | 2.0 ч | 8 900 | Низкий |
| 6 | Demo поверх реального warehouse / mock data | AE + solution lead | Product demo, BI, SQL notebooks | 2.5 ч | 11 800 | Низкий |
| 7 | Пилотный scope и KPI | AE + CSM + CTO | SOW, roadmap, security checklist | 3.0 ч | 15 200 | Низкий |
| 8 | Data / security review | CTO + solution lead | Docs, DPA, architecture review | 4.0 ч | 18 700 | Низкий |
| 9 | Настройка коннекторов и decisioning rules | Backend + ML + CSM | Product, cloud, warehouse | 18.0 ч | 66 000 | Средний |
| 10 | Pilot 4-6 недель с weekly business review | CSM + AE + analyst | Dashboards, alerts, playbooks | 16.0 ч | 43 500 | Средний |
| 11 | Procurement / legal / budget approval | AE + founder + finance | ЭДО, контракт, invoice workflow | 8.0 ч | 28 400 | Низкий |
| 12 | Invoice, старт платного контура, handoff в CSM | Finance ops + CSM | Bank, CRM, runbook | 1.5 ч | 4 900 | Высокий |

## Команда

| Роль | Функция | Нужно чел. | FOT fully-loaded ₽/мес | Time-to-hire | Ramp |
|---|---|---:|---:|---:|---:|
| CEO | founder-led sales, fundraising, enterprise deals | 1 | 780 000 | 0 | 0 |
| CTO / Tech Lead | архитектура, security review, enterprise deployment | 1 | 715 000 | 2.5 мес | 2 мес |
| Senior Backend | connectors, decisioning layer, data workflows | 2 | 1 092 000 | 1.5 мес | 1.5 мес |
| ML Engineer | uplift models, segmentation, experimentation logic | 1 | 650 000 | 2.5 мес | 2 мес |
| DevOps | cloud, observability, private deployment | 1 | 455 000 | 1.5 мес | 1 мес |
| Frontend | operator UI / dashboards | 1 | 390 000 | 1 мес | 1 мес |
| SDR | targeted outbound | 1 | 195 000 | 1 мес | 1 мес |
| AE | discovery, demo, close | 1 | 390 000 | 1.5 мес | 2.5 мес |
| Customer Success | onboarding, adoption, renewal | 1 | 325 000 | 1 мес | 1 мес |
| **Итого** |  | **9** | **4 992 000 ₽/мес** |  |  |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | X5 Digital | Высокий CRM/performance spend и сложная promo/lifecycle-механика в grocery; прямо указан в ICP-list кейса. | email decision-maker CDO/Head of CRM + отраслевые retail-конференции | 450 000 ₽/мес |
| 2 | ВкусВилл | Сильная подписка, retention и персонализация ассортимента, где uplift-layer может влиять на частоту заказов. | founder-led intro + партнёрство с data/SI-интегратором | 450 000 ₽/мес |
| 3 | Самокат | Быстрый e-grocery и высокая цена ошибки в offer/channel timing, сильный fit под decisioning. | email VP Growth / Head of CRM | 500 000 ₽/мес |
| 4 | Lamoda | Fashion e-commerce с heavy CRM, рекомендациями и промо-календарём; нужен cross-channel decisioning. | ABM outreach + demo через retail media/data use case | 500 000 ₽/мес |
| 5 | Hoff | Большой каталог, длинный цикл покупки и потребность в персонализированном nurture. | email CMO/Director of Analytics | 400 000 ₽/мес |
| 6 | Sunlight | Высокая частота акций и loyalty-коммуникаций, где ROI от next-best-action прозрачен. | vc.ru ad + direct outreach в CRM/marketing leadership | 400 000 ₽/мес |
| 7 | SOKOLOV | D2C retail с повторными покупками и активным промо-движком; подходит под premium uplift-layer. | партнёрство с martech-интегратором + email Head of Retention | 400 000 ₽/мес |
| 8 | Dodo Brands / Додо Пицца | Сильная digital-заказная база и регулярные lifecycle-триггеры; нужен decisioning на стыке CRM и промо. | founder network / конференция по retail-tech | 450 000 ₽/мес |
| 9 | Okko | Подписка и медиасервис, где churn/promo optimization напрямую бьёт в LTV. | email VP Product Marketing / Growth | 500 000 ₽/мес |
| 10 | Kassir.ru / МТС Live | Ticketing и event-retention сценарии, высокая чувствительность к timing и audience segmentation. | партнёрство + targeted email CMO/Head of CRM | 350 000 ₽/мес |

## Top-3 risks

| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Price compression и budget capture со стороны Mindbox/CDP/CEP incumbents | High | Very high | Модель ломается при `Price -30%`, EBITDA @M12 уходит в `-672 261 ₽/мес`. |
| Services creep и founder-led enterprise sale | High | High | `onboarding >8 недель` и зависимость от founder ухудшают repeatability, CAC и margin discipline. |
| Regulatory + vendor dependency risk (152-ФЗ, sanctions, LLM/API lockout) | Medium-High | High | RU-hosted/private cloud обязателен, а `vendor lockout` может нарушить SLA и COGS. |

## Что нужно доказать для APPROVED
1. **2-3 design partners** из named targets с готовностью идти в paid pilot по цене не ниже **400-450k ₽/мес**.
2. **Proof of uplift**: кейсы, где decisioning-layer даёт измеримый прирост выручки/ROMI/retention, а не просто ещё один dashboard.
3. **Productized deployment**: onboarding <= 6 недель, не более 20-25 часов solution engineering на логотип после стандартизации.
4. **Суверенный контур**: private cloud / on-prem SKU и multi-model architecture без критической зависимости от одного зарубежного API.

## LTV Upside Calculator
Так как статус **NEAR-PASS**, апсайд надо считать от already-good unit economics, а не от price fantasy.

### Базовая формула
`customer_ltv_rub = (MRR × GM) / churn`

### Базовый кейс
- MRR = 450 000 ₽
- GM = 75.6%
- churn = 1.5%/мес
- `customer_ltv_rub = 22 680 000 ₽`
- `LTV/CAC = 33.1x`

### Upside case
- MRR = 500 000 ₽
- GM = 78%
- churn = 1.2%/мес
- `customer_ltv_rub ≈ 32 500 000 ₽`
- при CAC 750 000 ₽ получаем `LTV/CAC ≈ 43.3x`

### Downside case
- MRR = 350 000 ₽
- GM = 68%
- churn = 3.0%/мес
- `customer_ltv_rub ≈ 7 933 333 ₽`
- при CAC 1 100 000 ₽ получаем `LTV/CAC ≈ 7.2x`

### Инвестиционный смысл
Upside не в том, чтобы ещё поднять LTV, он уже выдающийся. Реальный upside в том, чтобы подтвердить **repeatable premium GTM** и снизить execution variance, иначе рынок не даст этой математике конвертироваться в defendable company outcome.

## Proof points, которых не хватает
- Нет публично подтверждённых RU design partners.
- Нет данных, что local buyer готов платить premium поверх уже установленного Mindbox/CDP стека.
- Нет доказательства, что weekly business review и solution engineering не превращают rollout в квазиконсалтинг.

## Финальный вывод инвесткомитета
Hilbert близок к approve, но пока это **не investment-grade approve**, а **NEAR-PASS 69/100**. Причина простая: экономика отличная, рынок существует, но moat и GTM в РФ ещё не дают достаточного запаса прочности. Следующий апдейт должен быть не про ещё одну красивую категорию, а про конкретные локальные design partners, pricing floor и measured uplift.
