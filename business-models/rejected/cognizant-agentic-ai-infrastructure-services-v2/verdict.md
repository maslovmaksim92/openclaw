# Cognizant Agentic AI Infrastructure Services v2
**Статус:** NEAR-PASS
**Итоговый балл:** 66/100
**Дата:** 2026-04-20
**Сектор:** B2B-OPS
**Slug:** cognizant-agentic-ai-infrastructure-services-v2

---

## Этап 1 — Intake
Rerun старого кейса Cognizant после обновления P4-P7 рубрики. Исходный контекст: enterprise AI-managed IT operations, service desk, observability, incident management и managed infrastructure services для среднего и крупного бизнеса. Предыдущий вердикт, это 67/100 NEAR-PASS от 2026-04-19.

## Этап 2 — Demand Validation
Прямой локальный search-demand остаётся слабым: в demand-файле зафиксированы `Composite demand: LOW`, `Demand score: 3`, `hh.ru vacancies: 19`, `Yandex suggest: 2`, а по смежному запросу `AI service desk` есть более сильный suggest. TAM/SAM/SOM в файле оценены как 226,2 млрд ₽ / 23,4 млрд ₽ / 195 млн ₽ в год. Но обязательная числовая строка `Sources: T1=<N1>, T2=<N2>, T3=<N3>` отсутствует, поэтому evidence quality формально проседает.

## Этап 3 — Unit Economics
Экономика сильная. Базовые метрики: CAC 1 052 000 ₽, customer_ltv_rub 26 643 000 ₽, LTV/CAC 25,3x, CAC payback 1,62 месяца по MRR и 2,91 месяца по gross profit, gross margin 55,7%, contribution_margin_rub_month 315 500 ₽. Break-even достигается на 20 клиентах, startup_capital_to_bep_rub около 44,26 млн ₽. По чистой экономике кейс уверенно investment-grade.

## Этап 4 — Финансовая модель
В P6A/P6B median-case остаётся привлекательным: `EBITDA @M24 p50 = 9 660 000 ₽/мес`, а при 50 клиентах модель даёт около 9,775 млн ₽ company_ebitda_rub_month. Но downside остаётся жёстким: p10 EBITDA ниже нуля, sensitivity на `Price -30%` даёт отрицательный EBITDA, а Monte Carlo Lite показывает широкий разброс outcome distribution.

## Этап 5 — Critic
Главный вывод критики: кейс не проваливается по economics, а проваливается по margin of safety. Основные риски, это отсутствие корректной tier-разметки evidence, слабый moat против incumbent ITSM/MSP substitute-set, зависимость от внешних LLM/API vendors и чувствительность к price compression. Execution feasibility есть, но она enterprise-heavy и требует сильного trust/compliance contour.

## Этап 6 — Финальный вердикт инвесткомитета
**Итог: NEAR-PASS, 66/100.**

### Score breakdown
| Критерий | Балл |
|---|---:|
| Unit Economics | 21/25 |
| EBITDA Potential | 20/25 |
| Market + Demand | 10/25 |
| Moat | 10/25 |
| Execution Risk | 17/25 |
| GTM Realism | 21/25 |

### Почему не APPROVED
1. В demand-stage нет обязательной числовой source-tier строки, поэтому quality of evidence по рынку остаётся неполной.
2. Прямой локальный demand слабый, а market score capped penalty не даёт пройти investment-grade threshold.
3. Moat строится больше на delivery execution, чем на защищённых data/network/regulatory advantages.
4. Sensitivity показывает, что pricing power, это критическая точка хрупкости.

### Что нужно доказать для upgrade
1. Минимум 3 paid pilot в РФ и pilot-to-paid >= 33%.
2. Не менее 2 reference accounts с измеримым SLA/MTTR improvement.
3. Сохранение ARPA >= 650 000 ₽/мес без median discount >20%.
4. Один repeatable vertical с sales cycle <= 120 дней.
5. Vendor-risk mitigation: multi-model routing или локальный fallback.

### Ключевые метрики
- customer_ltv_rub: 26 643 000 ₽
- contribution_margin_rub_month: 315 500 ₽/клиент/мес
- company_ebitda_potential_rub_month: 9 660 000 ₽/мес через 24 мес
- clients_to_500k_ebitda: 21
- months_to_500k_ebitda: 13
- startup_capital_to_bep_rub: 44 260 472 ₽

### Итоговая рекомендация
Это хороший follow-up candidate, но пока не материал для approve. Возвращаться после доказательства repeatable RU-demand, source-tier discipline и de-risking moat/vendor stack.
