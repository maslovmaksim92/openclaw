# Celsus, AI-скрининг и ранняя диагностика для клиник и диагностических сетей
**Статус:** APPROVED WITH NOTES
**Итоговый балл:** 73/100
**Дата:** 2026-04-19
**Сектор:** HEALTHCARE
**Slug:** celsus-radiology-ai-screening

---

## Этап 1 — Описание кейса
Celsus — AI-layer для лучевой диагностики, встроенный в регулярный поток исследований клиник и диагностических сетей. Кейс покрывает triage, приоритизацию и раннее выявление патологий по рентгену, КТ, маммографии и флюорографии. Базовая инвестиционная гипотеза: частные клиники и диагностические группы готовы платить recurring-чек за ускорение потока исследований, разгрузку врачей и повышение качества первичного screening.

## Этап 2 — Evidence
Открытые сигналы подтверждают зрелость категории: 11+ млн обработанных исследований, 44 региона присутствия, 29 клинических признаков и публичные кейсы внедрения в сети «Будь Здоров». Это важнее, чем просто технология: продукт уже встроен в реальный radiology workflow и используется как commercial-grade software.

## Этап 3 — Demand Validation
По автоматическому demand API ниша получила composite demand LOW, но это не ломает кейс: healthcare enterprise-сделки редко выглядят как search-driven category. WTP подтверждён конкурентами и substitute-услугами: Third Opinion, WillyAI и ручное экспертное описание исследований. TAM / SAM / SOM по модели составили 4,14 млрд ₽ / 966 млн ₽ / 34,5 млн ₽ в год. Stage result: CONDITIONAL PASS.

## Этап 4 — Unit Economics
Ключевые метрики инвестиционной модели:
- CAC: 296 000 ₽
- customer_ltv_rub: 7 168 000 ₽
- LTV/CAC: 24,2x
- CAC Payback: 3,3 месяца
- GM: 77,9%
- contribution_margin_rub_month: 89 600 ₽/клиент/мес
- fixed_costs_rub_month: 2 556 700 ₽/мес
- Break-even: 29 клиентов
- startup_capital_to_bep_rub: 13 534 869 ₽

Бизнес-процесс длинный, но понятный: outbound по клиникам, discovery, demo, ROI-калькуляция, NDA и пилот, security review, интеграция с МИС/РИС/PACS, онбординг врачей, затем recurring support. Economics stage: PASS.

## Этап 5 — Финансовая модель и критика
Base scenario показывает 33,9 клиента и 484 538 ₽ EBITDA в M12, optimistic — 53,4 клиента и 2 423 940 ₽ EBITDA, pessimistic — 23,8 клиента и -980 377 ₽ EBITDA. Основные точки уязвимости: price compression, удорожание acquisition и длинные интеграции. При этом `company_ebitda_potential_rub_month` достигает 1 923 300 ₽/мес на 50 клиентах, а порог 500K EBITDA достигается примерно при 35 клиентах и около 13-го месяца.

## Этап 6 — Финальный вердикт инвесткомитета
**Итог: APPROVED WITH NOTES, 73/100.**

Score breakdown:
- Реальный спрос: 11/20
- Прибыль компании / Unit economics: 21/25
- Масштабируемость: 14/20
- Конкурентное позиционирование: 11/15
- Барьеры входа: 9/10
- Качество данных: 7/10

Почему одобрено:
1. Категория уже коммерциализирована и имеет подтверждённый enterprise WTP.
2. Fundable unit economics с большим запасом по LTV/CAC и payback.
3. Порог `company_ebitda_potential_rub_month >= 500 000 ₽` достигается в пределах 50 клиентов и 24 месяцев.

Топ-3 риска:
1. Price compression и скидки >25%.
2. Долгие и дорогие интеграции с МИС/РИС/PACS.
3. Founder bottleneck в sales и medical presale.

Что доказать дальше:
1. Pilot-to-paid conversion не ниже 40% на первых 10 пилотах.
2. Go-live cycle не длиннее 60 дней.
3. ARPA не ниже 110 000 ₽/мес без системных скидок >20%.

## История прохождения пайплайна
- 2026-04-19, Program 4: CONDITIONAL PASS по спросу, несмотря на LOW search-demand.
- 2026-04-19, Program 5: PASS по юнит-экономике, `customer_ltv_rub = 7 168 000 ₽`, `LTV/CAC = 24,2x`.
- 2026-04-19, Program 6: critic PASS WITH RESERVATIONS, execution-risk выше среднего.
- 2026-04-19, Program 7: APPROVED WITH NOTES, 73/100.
