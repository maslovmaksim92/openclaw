# Enterprise AI Knowledge Search Operator v2
**Статус:** NEAR-PASS
**Итоговый балл:** 65/100
**Дата:** 2026-04-20
**Сектор:** B2B-OPS

---

## Этап 1 — Intake
Это rerun кейса `enterprise-ai-knowledge-search-operator`, который ранее был одобрен с результатом 72/100. Повторный прогон потребовался после обновления системы оценки: добавлены rubric 6×25, 7-factor moat, tier-awareness penalty и более строгая проверка EBITDA-потенциала и GTM. Базовая гипотеза кейса не изменилась: service-led внедрение enterprise AI-поиска по корпоративным данным, wiki, документам, чатам и SaaS-системам с private deployment, ACL и managed knowledge ops.

---

## Этап 2 — Demand Validation
Demand-stage завершился статусом PASS, но с оговоркой по качеству evidence. В файле demand зафиксировано: «По exact-category спрос в открытом RU-поиске низкий, но money demand подтверждён». Категория валидируется через substitute spend и соседние budget lines, а не через широкий keyword pull. В качестве WTP-сигналов использованы Confluence, Яндекс 360 для бизнеса и глобальный сигнал Glean.

Ключевые выводы этапа:
- TAM: около 370,3 млрд ₽ глобально.
- SAM РФ: около 1,44 млрд ₽.
- SOM Y1: около 28,8 млн ₽.
- Публичный substitute-коридор даёт правдоподобный чек 3,6–9,6 млн ₽/год.

Слабое место, в demand-файле отсутствует строка `Sources: T1=..., T2=..., T3=...`, поэтому на этапе P7 автоматически сработал tier-penalty и критерий Market + Demand был ограничен сверху.

---

## Этап 3 — Unit Economics
P5 прошёл уверенно. Модель работает только в premium enterprise-сегменте, зато там даёт очень сильные метрики:

- customer_ltv_rub: 34 200 000 ₽
- CAC: 1 684 000 ₽
- LTV/CAC: 20,3x
- CAC payback: 2,1 мес по MRR
- contribution_margin_rub_month: 410 000 ₽/клиент/мес
- Gross Margin: 51,3%
- fixed_costs_rub_month: 8 078 000 ₽/мес
- Break-even: 20 клиентов, около M13

Иными словами, экономика клиента фондового уровня есть. Основная уязвимость не в LTV/CAC, а в том, сможет ли команда repeatably довозить enterprise deals без взрывного роста CAC и scope creep.

---

## Этап 4 — Finance / Critic
В base scenario на M12 компания ещё убыточна, `company_ebitda_rub_month = -698 000 ₽/мес`, но к M14 модель пересекает 500K EBITDA примерно на 21 клиенте. При 50 клиентах `company_ebitda_potential_rub_month = 12 422 000 ₽/мес`, то есть сам EBITDA Gate проходит с большим запасом.

Monte Carlo Lite:
- p10 EBITDA @M24: -2 878 000 ₽/мес
- p50 EBITDA @M24: 5 042 000 ₽/мес
- p90 EBITDA @M24: 17 682 000 ₽/мес

Главная критика: downside остаётся неприятно глубоким. Цена и CAC чувствительнее churn, а значит у кейса не хватает margin of safety для автоматического approve.

---

## Этап 5 — Committee Scoring
Итог по новой рубрике: **98/150 raw**, что даёт **65/100 normalized**.

Score breakdown:
- Unit Economics: 23/25
- EBITDA Potential: 20/25
- Market + Demand: 10/25
- Moat: 13/25
- Execution Risk: 15/25
- GTM Realism: 17/25

7-factor moat показал умеренную защищённость: switching costs и embedded workflow есть, но сильного proprietary data moat, network effects или category brand в РФ пока нет.

---

## Этап 6 — Финальный вердикт
Финальный статус: **NEAR-PASS**.

Почему не APPROVED:
1. Новая система справедливо штрафует кейс за неполную tiered evidence-базу спроса.
2. Moat в основном сервисный, а не платформенный.
3. GTM enterprise-heavy, founder-dependent и чувствителен к price compression и CAC inflation.

Почему не REJECTED:
1. Unit economics действительно сильная.
2. EBITDA >500K достижим в пределах 24 месяцев и до 50 клиентов.
3. Есть defendable ниша в private deployment + ACL-heavy enterprise knowledge search.

Что нужно доказать для следующего rerun:
- 3 платящих design partners по 700К+ ₽/мес.
- pilot-to-paid ≥35%.
- CAC <1,3 млн ₽.
- 2 reference accounts с private deployment.
- tier balance ≥2.0 с корректной строкой Sources.

---

## Короткий вывод
Это не слабый кейс, а кейс с сильной экономикой и пока недостаточно надёжной доказательной базой. При подтверждении GTM и evidence quality он может быстро вернуться в approve-коридор.
