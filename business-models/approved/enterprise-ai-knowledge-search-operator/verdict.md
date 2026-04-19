# Enterprise AI Knowledge Search Operator
**Статус:** APPROVED
**Итоговый балл:** 72/100
**Дата:** 2026-04-19
**Сектор:** GEO-EXPAND

---

## Этап 1 — Описание кейса
Сервисная модель внедрения и сопровождения enterprise AI-поиска по корпоративным данным, knowledge graph и агентного слоя поверх внутренних документов, SaaS-систем и permission-aware контента. Исходный сигнал пришёл из GEO-EXPAND категории через Glean, который к 8 декабря 2025 года публично сообщил о ARR более $200 млн. Гипотеза кейса в том, что в РФ можно занять окно implementation-led substitute: private deployment, локальные коннекторы, аудит прав доступа, governance и managed operations вокруг enterprise knowledge stack.

Ключевая гипотеза: крупные компании готовы покупать не просто поиск, а единый AI-интерфейс к документам, wiki, CRM, тикетам, чатам и коду, если решение закрывает безопасность, ACL, качество retrieval и последующее сопровождение.

---

## Этап 2 — Проверка спроса
Проверка спроса завершилась со статусом PASS и composite demand MEDIUM-HIGH. Mandatory demand API был технически недоступен, поэтому exact keyword volume получить не удалось. Вместо этого спрос подтверждён через рыночные и коммерческие сигналы:

- Glean публично раскрыл ARR > $200 млн, что подтверждает зрелость категории.
- В РФ есть локальный product signal через запуск Яндекс Нейроэксперта.
- Найдены substitute-конкуренты с публичными ценами: Slab ($8/user/month), Tettra ($8/user/month), Confluence ($5.16/user/month), Algolia usage-based.
- WTP подтверждён recurring pricing у игроков категории и крупным коммерческим масштабом Glean.

TAM / SAM / SOM:
- TAM: 43,2 млрд ₽/год
- SAM: 9,6 млрд ₽/год
- SOM: 288 млн ₽/год

LTV Gate по спросу проходит в нескольких сценариях: внедрение, recurring support, private cloud / on-prem, integration packs и retainers. Категория оценена как GROWING / EARLY SCALE.

---

## Этап 3 — Юнит-экономика
Бизнес-процесс расписан от лида до первой оплаты: target-account enrichment, outreach, qualification, discovery, audit коннекторов и ACL, pilot/PoC, security/legal/procurement, предложение и запуск.

Ключевые метрики:
- CAC: 940 000 ₽
- Revenue / client / month: 620 000 ₽
- COGS / client / month: 238 000 ₽
- contribution_margin_rub_month: 382 000 ₽/мес
- Gross Margin: 61,6%
- customer_ltv_rub: 21 222 222 ₽
- LTV/CAC: 22,6x
- CAC Payback: 2,46 месяца
- fixed_costs_rub_month: 2 290 000 ₽
- Break-even: 6 клиентов / 6-й месяц ramp

Команда запуска: 11 человек, payroll 2 470 000 ₽/мес. Критические риски этапа: presale-heavy CAC, service creep при кастомных коннекторах и founder-led sales dependency.

---

## Этап 4 — Финансовая модель и критика
Base scenario на 12 месяцев:
- M12: 11 клиентов, MRR 6 820 000 ₽, EBITDA 1 552 000 ₽
- Year 1 EBITDA: -1 536 000 ₽

Optimistic scenario:
- M12: 13 клиентов, EBITDA 2 116 000 ₽
- Year 1 EBITDA: +3 456 000 ₽

Pessimistic scenario:
- M12: 6 клиентов, EBITDA -358 000 ₽
- Year 1 EBITDA: -15 288 000 ₽

Пик потребности в капитале в base scenario достигается в M7 на уровне около 5,876 млн ₽. Безопасный стартовый капитал оценён в 6,5-7,0 млн ₽.

Критические стресс-тесты:
- CAC x2: payback растёт до 4,92 месяца, дополнительная потребность в капитале +10,34 млн ₽.
- Churn x2: customer_ltv_rub падает до 10,61 млн ₽, пространство для ошибок сильно сужается.
- Цена -30%: contribution margin падает до 45,2%, break-even уходит на 12 клиентов, M12 EBITDA становится -494 тыс. ₽.

Главные риски: CAC drift, service creep, price compression, payment delays и procurement stretch.

---

## Этап 5 — Финальный вердикт
Финальный балл: 72/100. Статус: APPROVED с замечаниями.

Score breakdown:
- Реальный спрос: 14/20
- Прибыль компании / Unit economics: 19/25
- Масштабируемость: 14/20
- Конкурентное позиционирование: 10/15
- Барьеры входа: 7/10
- Качество данных: 8/10

Компания выходит на 500K EBITDA при 8 клиентах и на 1M EBITDA при 10 клиентах. По base scenario 500K достигается на 9-м месяце, 1M на 11-м. company_ebitda_potential_rub_month в M12 составляет 1 552 000 ₽.

Почему одобрено:
1. Сильная мировая валидация категории и подтверждённый WTP.
2. Fundable юнит-экономика: LTV/CAC 22,6x, payback 2,46 месяца.
3. Прибыль компании достигает порогов при реалистичном масштабе до 50 клиентов и в пределах 24 месяцев.

Что доказать до запуска:
1. Pilot-to-paid conversion не ниже 50% на первых 6 пилотах.
2. ARPA не ниже 550 000 ₽/мес без системного дисконтирования.
3. Стандартизация топ-10 коннекторов, чтобы COGS не выходил выше 250 000 ₽/клиент/мес.

---

## Этап 6 — История прохождения пайплайна
2026-04-19, Program 4: спрос PASS, composite demand MEDIUM-HIGH, TAM/SAM/SOM = 43,2 млрд / 9,6 млрд / 288 млн ₽, ранний reject не требуется.

2026-04-19, Program 5: юнит-экономика PASS, CAC 940 тыс. ₽, customer_ltv_rub 21,2 млн ₽, contribution_margin_rub_month 382 тыс. ₽/мес, LTV/CAC 22,6x, break-even 6 клиентов.

2026-04-19, Program 6: critic PASS WITH RESERVATIONS, base M12 EBITDA 1,55 млн ₽, year-1 EBITDA -1,54 млн ₽, безопасный стартовый капитал 6,5-6,8 млн ₽.

2026-04-19, Program 7: итог APPROVED, 72/100, ключевой риск в price compression и service creep, а не в самом наличии спроса.