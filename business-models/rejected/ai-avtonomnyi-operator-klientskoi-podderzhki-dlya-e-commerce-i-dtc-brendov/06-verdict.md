[B2B-OPS] AI-автономный оператор клиентской поддержки для e-commerce и DTC-брендов — NEAR-PASS: 65/100 | EBITDA base=1240К₽/мес через 15 мес | LTV/CAC=12,1x | Ключевое преимущество: быстрый ROI через cost-to-serve | Главный риск: weak moat и price compression.

# 06-verdict — AI-автономный оператор клиентской поддержки для e-commerce и DTC-брендов

sector: B2B-OPS
status: NEAR-PASS
score: 65/100
case_slug: ai-avtonomnyi-operator-klientskoi-podderzhki-dlya-e-commerce-i-dtc-brendov
date: 2026-05-12

## Итог инвесткомитета
**Вердикт: NEAR-PASS.**

Кейс проходит по клиентской юнит-экономике, но не дотягивает до investment-grade на уровне компании. В плюсах, **customer_ltv_rub = 6,64 млн ₽**, **LTV/CAC = 12,1x**, **CAC payback = 2,5 месяца**, а operating view в `04-economics.md` допускает **company_ebitda_rub_month ≈ 1 240 000 ₽/мес при 50 клиентах**. В минусах, exact-demand в РФ остаётся слабым, moat слабый, а `05-critic.md` фиксирует отрицательный **p10 EBITDA @M24 = -1,8 млн ₽/мес**, что делает downside слишком тяжёлым для чистого approve.

## Investment one-liner
`[B2B-OPS] AI-автономный оператор клиентской поддержки для e-commerce и DTC-брендов — NEAR-PASS: 65/100 | EBITDA base=1240К₽/мес через 15 мес | LTV/CAC=12,1x | Ключевое преимущество: быстрый ROI через cost-to-serve | Главный риск: weak moat и price compression.`

## Оценка
Source tier balance: T1=5, T2=16, T3=1, weighted=2.18. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | В `04-economics.md`: «LTV/CAC = 12.1:1», «CAC Payback = 2.5 месяца», «Contribution Margin = 42.7%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | `04-economics.md` даёт «EBITDA = 1.24 млн ₽/мес» при 50 клиентах в operating view и break-even около M13-M15. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | В `02-demand.md`: «composite_demand=LOW, demand_score=0», но есть «HH ... 1 187 вакансий» и `SAM (РФ) = 1.08 млрд ₽`; учтён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 9 | В `02-demand.md` прямо зафиксировано: «Высокая коммодитизация, потому что Jivo, Usedesk, Gorgias и Tidio уже продают базовый automation layer». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | `05-critic.md` фиксирует high-risk по «LLM API quality/latency/cost», санкциям, 152-ФЗ и founder-led sales. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `04-economics.md` даёт fully-loaded CAC 549 250 ₽ и payback 2,5 мес, а ICP в `02-demand.md` узко задан как top/mid e-commerce с 10 buyer-targets. |

**Sum raw = 98 / 150. Normalized score = round((98 × 100) / 150) = 65 / 100.**

## 7-factor moat framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает модель для остальных без риска утечки доменных данных. |
| 2. Switching costs | 2 | После интеграции в helpdesk, Telegram, web-chat и QA-процессы смена поставщика уже болезненна. |
| 3. Scale economies | 1 | COGS частично падает с ростом, но HITL и onboarding сохраняют service-heavy профиль. |
| 4. Proprietary data / model advantage | 1 | В теории появится ticket/case data loop, но в материалах нет подтверждённого уникального датасета или model edge. |
| 5. Regulatory moat | 0 | 152-ФЗ создаёт friction, но не лицензируемый moat и не блокирует локальных конкурентов. |
| 6. Brand / distribution | 1 | Category proof есть, но локальный бренд и distribution в РФ не сформированы. |
| 7. Embedded workflow | 2 | Продукт глубоко встраивается в ежедневный post-purchase support workflow и escalation routing. |

**Moat score = round((7 × 25) / 21) = 8 / 25.**

## Полный бизнес-процесс

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов и intent-list | SDR | HH/Data Insight/ручной research/CRM | 30 мин | 1 350 | Низкая |
| 2 | Первый outbound/inbound touch | SDR | email, Telegram, CRM sequences | 15 мин | 675 | Средняя |
| 3 | Qualification call | SDR | Meet, CRM, скрипт квалификации | 30 мин | 1 350 | Средняя |
| 4 | Discovery с buyer | AE + founder | Meet, Miro, CRM | 60 мин | 6 250 | Низкая |
| 5 | Solution demo и ROI framing | AE + CTO | Demo workspace, dashboard, CRM | 90 мин | 10 875 | Низкая |
| 6 | Технический scoping и оценка интеграций | CTO + backend | Notion, API docs, helpdesk sandbox | 4 ч | 16 000 | Низкая |
| 7 | Pilot proposal / commercial offer | AE + founder | CPQ, Docs, e-sign | 2 ч | 9 250 | Средняя |
| 8 | Security/legal review | CTO + founder | DPA, SLA, security checklist | 3 ч | 15 000 | Низкая |
| 9 | Contract signing | Founder/AE | Диадок/Контур, e-sign | 1 ч | 4 625 | Высокая |
| 10 | Channel onboarding (Telegram, web-chat, helpdesk) | CSM + backend | Jivo/Usedesk/API/webhooks | 6 ч | 15 900 | Средняя |
| 11 | Knowledge ingestion и настройка AI-оператора | ML engineer + CSM | RAG/KB pipeline, prompt stack | 8 ч | 22 800 | Средняя |
| 12 | QA, escalation routing, HITL policy | ML engineer + CSM | QA dashboard, eval set | 6 ч | 17 100 | Средняя |
| 13 | Go-live и первые 2 недели hypercare | CSM + founder | Slack/Telegram, CRM, analytics | 10 ч | 25 550 | Низкая |
| 14 | Ежемесячный success review / upsell | CSM + AE | BI, CRM, CS deck | 2 ч/мес | 5 940 | Средняя |
| 15 | Invoice / акт / collection | Finance ops | 1С/МойСклад/банк/ЭДО | 45 мин/мес | 900 | Высокая |
| 16 | Оплата клиентом | Buyer | банк-клиент / счёт | 3-10 дней DSO | 0 | Полная со стороны вендора нет |

**Direct win-cost по процессу:** 147 565 ₽ до acquisition overhead; реальный fully-loaded CAC остаётся 549 250 ₽.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| ARPA / MRR | 220 000 ₽/мес |
| COGS / клиент / мес | 100 000 ₽ |
| contribution_margin_rub_month | 94 000 ₽/клиент/мес |
| GM | 54,5% |
| service-adjusted contribution margin | 42,7% |
| customer_ltv_rub | 6 643 636 ₽ |
| CAC fully-loaded | 549 250 ₽ |
| LTV/CAC | 12,1x |
| CAC payback | 2,5 мес |
| Break-even | 51 клиент |
| company_ebitda_rub_month @ 50 клиентов | 1 240 000 ₽/мес |
| clients_to_500k_ebitda | ~45 |
| months_to_500k_ebitda | ~15 |
| startup_capital_to_bep_rub | 31 380 495 ₽ |
| startup_capital | 35 000 000 ₽ |

## EBITDA / PnL summary
- **Base M12 EBITDA:** -859 291 ₽/мес.
- **Optimistic M12 EBITDA:** +2 944 017 ₽/мес.
- **Pessimistic M12 EBITDA:** -3 929 302 ₽/мес.
- **Monte Carlo Lite:** p10 EBITDA@M24 = -1 800 000 ₽/мес, p50 = 6 200 000 ₽/мес, p90 = 14 500 000 ₽/мес.
- Главный вывод из `05-critic.md`: медиана проходит gate, но левый хвост распределения остаётся отрицательным, поэтому риск капитала выше допустимого для clean approve.

## Команда

| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO / founder | 1 | 845 000 | Продажи, fundraising, ключевые аккаунты |
| CTO / Tech Lead | 1 | 715 000 | Архитектура, security, delivery supervision |
| Senior Backend | 1 | 585 000 | Интеграции, API, routing, billing |
| ML Engineer | 1 | 650 000 | RAG, evals, prompt quality |
| DevOps | 0.5 | 227 500 | Infra, observability, CI/CD |
| Frontend | 0.5 | 195 000 | Dashboards и клиентский интерфейс |
| SDR | 1 | 255 300 | Prospecting и meetings |
| AE | 1 | 445 250 | Discovery, proposal, close |
| Customer Success | 1 | 338 000 | Onboarding, retention, QBR |
| **Итого** | **8.0 FTE** | **4 256 050 ₽/мес** | Полная базовая команда |

## GTM: 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Lamoda | Fashion e-commerce с высоким объёмом post-purchase вопросов, возвратов и статусов доставки, что идеально совпадает с ICP из `02-demand.md`. | email Head of CX / партнёрский intro через helpdesk-интегратора | 300 000 ₽/мес |
| ВсеИнструменты | Большой SKU-ассортимент и длинный хвост customer inquiries по наличию, доставке и возвратам. | outbound ABM на Director of Customer Support | 280 000 ₽/мес |
| DNS | Массовая consumer electronics-поддержка и нагрузка на статусы заказов, гарантию и exchange/return flow. | email decision-maker + retail-tech конференция | 320 000 ₽/мес |
| Ситилинк | Омниканальный support и много повторяемых вопросов по доставке, сборке и возвратам. | партнёрство с омниканальным contact-center интегратором | 280 000 ₽/мес |
| М.Видео-Эльдорадо | Высокий объём логистических и сервисных обращений, где measurable ROI строится от AHT и deflection rate. | direct outreach Head of Contact Center | 350 000 ₽/мес |
| Лэтуаль | Beauty retail с частыми вопросами по статусу, наличию, лояльности и возвратам. | email e-commerce operations lead / vc.ru ad remarketing | 220 000 ₽/мес |
| Золотое Яблоко | DTC и app-first поддержка, высокая чувствительность к SLA в пиковые сезоны. | outreach через e-commerce conference + referral intro | 240 000 ₽/мес |
| Hoff | Мебель и home сегмент, где много обращений по срокам доставки, сборке и рекламациям. | outbound на customer service director | 260 000 ₽/мес |
| Askona | DTC/home-коммерция с дорогими заказами и высоким cost-to-serve по post-purchase сценарию. | email decision-maker + партнёрство с CRM/helpdesk интегратором | 230 000 ₽/мес |
| Flowwow | Высокочастотный marketplace-like support и Telegram-friendly customer communication. | founder-led intro / Telegram-first demo | 200 000 ₽/мес |

**GTM verdict:** target list выглядит реалистично, но для approve не хватает доказанного design-partner pipeline и подтверждённой pilot-to-rollout конверсии на 2-3 клиентах.

## Top-3 risks

| Риск | Probability | Impact | Почему это top-3 |
|---|---|---|---|
| Weak moat и коммодитизация AI-support слоя | High | High | `02-demand.md` прямо говорит о «высокой коммодитизации», а moat score всего 8/25. |
| Price compression / discounting | High | High | В `05-critic.md` сценарий `Price -30%` даёт EBITDA @M12 = -3 301 291 ₽/мес. |
| LLM/API dependence + 152-ФЗ + санкции | High | High | `05-critic.md` отдельно отмечает зависимость от внешних LLM, geo-blocking risk и enterprise friction по data residency. |

## Что нужно доказать для перехода из NEAR-PASS в APPROVED
1. 2-3 платных design partners из top-1000 e-commerce с contract value не ниже 220-250 тыс. ₽/мес.
2. Pilot-to-rollout conversion не ниже 40% и onboarding < 14 дней на типовом helpdesk stack.
3. Доказанный churn ≤ 2,5%/мес при deflection rate и CSAT без просадки.
4. Частный deployment или локальный LLM fallback без падения GM ниже 50%.
5. Реальный operating path к `company_ebitda_rub_month ≥ 500 000 ₽/мес` не позже M15 без price dumping.

## LTV Upside Calculator
Цель блока, показать, что кейс можно дотянуть до approve, если улучшить 3 рычага, ARPA, churn и CAC.

| Сценарий | ARPA, ₽/мес | Gross margin | Churn / мес | CAC, ₽ | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|---:|
| Текущий base | 220 000 | 66,4% | 2,2% | 549 250 | 6 643 636 | 12,1x |
| Upside 1, pricing discipline | 250 000 | 66,4% | 2,2% | 549 250 | 7 549 545 | 13,7x |
| Upside 2, retention improvement | 220 000 | 66,4% | 1,8% | 549 250 | 8 120 000 | 14,8x |
| Upside 3, CAC discipline | 220 000 | 66,4% | 2,2% | 450 000 | 6 643 636 | 14,8x |
| Combined upside | 250 000 | 68,0% | 1,8% | 450 000 | 9 444 444 | 21,0x |

**Интерпретация:** чисто на клиентской экономике запас уже есть. Для перехода в approve нужен не столько выше LTV/CAC, сколько доказанный company-level operating leverage и снижение downside variance.

## Verdict rationale
Это качественный **service-led B2B-OPS wedge**, но пока не фондовый compounder. Если смотреть только на client economics, кейс тянет на approve. Если смотреть на инвестиционный риск на уровне компании, то отсутствие moat, слабый локальный category pull и отрицательный p10 на M24 переводят его в **NEAR-PASS**.
