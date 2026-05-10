# Контур.Фокус, AI-комплаенс и проверка контрагентов для KYC/AML, 115-ФЗ и risk-scoring

[FINTECH] Контур.Фокус AI-compliance Russia v2 — NEAR-PASS: 65/100 | EBITDA base=1213К₽/мес через 12 мес | LTV/CAC=25,6x | Ключевое преимущество: обязательный regulatory workflow и глубокая встройка в 1С/AML-контур | Главный риск: moat захватывает incumbent data-layer, а не новый AI-layer.

sector: FINTECH
slug: kontur-focus-ai-compliance-russia-v2
status: NEAR-PASS
score: 65/100
date: 2026-05-10

## Стадия 1. Intake
- Wedge: AI-assisted compliance layer поверх Контур.Фокуса / Фокус.Комплаенс для KYC/AML, 115-ФЗ, санкций, скоринга риска и case-handling внутри regulated компаний.
- Why now: российский рынок уже перешёл от разовой проверки контрагента к регулярному operational workflow с 1С-интеграциями, анкетами клиента, batch-checks и audit trail.
- Historical context: исходный сигнал раньше был учтён как supporting signal для другого кейса, но не проходил самостоятельный P4→P7 цикл.

## Стадия 2. Validation
- В папке кейса отдельный файл `02-validation.md` отсутствует.
- Validation-логика фактически встроена в `02-demand.md`, `04-economics.md` и `05-critic.md`.
- Это process-gap, но не блокер для verdict, потому что demand, unit economics и critic evidence присутствуют.

## Стадия 3. Demand
### Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

- Exact-demand по формулировкам категории в РФ в основном LOW, но adjacent-demand по `1с проверка контрагентов` уже MEDIUM с `hh_ru=2764`.
- Regulatory demand real: организации обязаны идентифицировать клиентов, оценивать риск и фиксировать результаты в анкете клиента.
- Local category proof сильный: Контур.Фокус публично заявляет `более 50 000 пользователей`, а контур для 1С закрывает 115-ФЗ, санкции, массовые проверки и скоринг по 70 критериям.
- Вывод: рынок реальный и budgeted, но category language остаётся workflow-first, а не AI-first.

## Стадия 4. Economics
### Ключевые метрики
- customer_ltv_rub: 24 656 667 ₽
- CAC fully-loaded: 962 000 ₽
- LTV/CAC: 25,6x
- CAC payback: 2,6 мес по contribution margin
- GM: 56,9%
- contribution_margin_rub_month: 370 000 ₽/клиент/мес
- break-even: 20 клиентов
- clients_to_500k_ebitda: 20-21
- months_to_500k_ebitda: 11-12
- clients_to_1m_ebitda: 23
- months_to_1m_ebitda: 12
- startup_capital_to_bep_rub: 22 200 000 ₽
- рекомендованный стартовый капитал с буфером: 50 000 000–60 000 000 ₽

### Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Target-account list и ICP enrichment | SDR | HH/СПАРК/Контур/таблицы | 20 мин/account | 1 200 | средняя |
| 2 | Первичный outbound-touch, email/call/Telegram | SDR | CRM + телефония + почта | 15 мин/account | 900 | средняя |
| 3 | Qualification, pain discovery | SDR | CRM, скрипт, AI-notes | 30 мин/lead | 1 800 | средняя |
| 4 | Discovery-call | SDR + compliance consultant | Meet, CRM, AI-transcript | 60 мин | 6 500 | средняя |
| 5 | Demo на данных клиента | AE + solutions engineer | demo stand, 1С sandbox | 90 мин | 11 000 | низкая |
| 6 | Предпроектный scoping / pilot design | Solutions engineer + compliance analyst | notion/jira/конфигуратор | 6 ч | 26 000 | низкая |
| 7 | Security / legal / procurement review | AE + founder + legal | docs, шаблоны, redlines | 8 ч | 35 000 | низкая |
| 8 | Коммерческое предложение и калькуляция | AE | CRM/CPQ/шаблон | 2 ч | 7 500 | средняя |
| 9 | Pilot / paid PoC | implementation lead + backend | staging + API + 1С | 20 ч | 78 000 | низкая |
| 10 | Закрытие сделки и счёт | AE + finance ops | CRM + 1С + ЭДО | 2 ч | 8 000 | высокая |
| 11 | Onboarding и интеграция | implementation lead + backend + analyst | API, 1С, ETL, docs | 40 ч | 155 000 | низкая |
| 12 | Training и rollout | CSM + analyst | webinar, KB, playbooks | 6 ч | 18 000 | средняя |
| 13 | Ежемесячный monitoring / QBR / support | CSM + analyst | helpdesk, BI, alerting | 4 ч/мес | 28 000 | средняя |
| 14 | Оплата и закрытие периода | finance ops | 1С, ЭДО, банк | 1 ч/мес | 3 000 | высокая |

### Команда
| Роль | Кол-во | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO / Founder | 1 | 780 000 | enterprise selling и стратегические партнёрства |
| CTO / Tech Lead | 1 | 715 000 | архитектура и security review |
| Senior Backend | 2 | 1 092 000 | интеграции и delivery |
| ML Engineer | 1 | 650 000 | AI/risk-scoring слой |
| DevOps | 1 | 455 000 | infra и reliability |
| Frontend | 1 | 390 000 | UI и adoption layer |
| Product / Compliance lead | 1 | 455 000 | compliance logic и roadmap |
| SDR | 2 | 390 000 | acquisition и account mapping |
| AE | 1 | 416 000 | demo, proposal, close |
| Customer Success | 1 | 325 000 | onboarding и retention |
| Compliance analyst | 1 | 338 000 | analyst-in-the-loop delivery |
| Finance / ops | 0,5 | 195 000 | billing и admin |
| **Итого** | **12,5** | **6 201 000** | senior-heavy regulated delivery team |

## Стадия 5. Critic
- Base-case силён: EBITDA становится положительной на M11 и достигает `1 213 085 ₽/мес` к M12.
- Downside остаётся жёстким: Monte Carlo Lite даёт `p10 EBITDA @M24 = -1 493 851 ₽/мес`, `p50 = 10 040 539 ₽/мес`, `p90 = 32 011 815 ₽/мес`.
- Sensitivity показывает, что главные поломки сидят в `CAC x2` и `Price -30%`, а не только в churn.
- Bottom line: economics проходит, но risk-adjusted moat и GTM запас прочности пока недостаточны для approve.

## Стадия 6. Verdict
### Оценка
| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV / CAC = 25,6x`, `Payback on gross profit = 2,60 мес`, `Gross margin = 56,9%`, но delivery остаётся service-heavy. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `Break-even по MRR contribution достигается на M11`, `EBITDA M12 = 1 213 085 ₽`, при 50 клиентах `EBITDA ≈ 11,3 млн ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 12 | `1с проверка контрагентов` = `MEDIUM`, `hh_ru=2764`, но строка `Sources:` отсутствует, поэтому применён штраф evidence-quality и exact-demand mostly LOW. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 15 | Регуляторный workflow real, но value-capture может остаться у `Контур.Фокус / Фокус.Комплаенс` и 1С-интеграторов, а не у нового AI-layer. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | Есть `152-ФЗ / data residency`, vendor overlap, long enterprise cycle и риск превращения в кастомный SI-проект. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | Лучшая экономика у `1С / integrator partners`, `CAC = 962 000 ₽` и 10 named targets реалистичны, но sales motion дорогой и procurement-heavy. |

**Итого raw:** 98/150  
**Normalized score:** 65/100

### 7-factor moat framework
| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не усиливает продукт для остальных клиентов. |
| Switching costs | 2 | 1С-интеграции, правила и настроенные анкеты создают friction, но migration возможен. |
| Scale economies | 1 | Upstream data и delivery постепенно улучшаются с объёмом, но не радикально. |
| Proprietary data / model advantage | 1 | Собственный dataset не доказан, data moat в основном у incumbent-источника. |
| Regulatory moat | 3 | 115-ФЗ, санкции, ПОД/ФТ и audit requirements формируют сильный workflow barrier. |
| Brand / distribution | 3 | Локальный distribution и доверие в этой категории уже доказаны у Контур-экосистемы. |
| Embedded workflow | 3 | При хорошем внедрении решение глубоко встраивается в onboarding, treasury, procurement и AML operations. |

**Moat score:** round((13 × 25) / 21) = **15/25**  
**Вывод:** moat средний, но большая часть силы принадлежит incumbent infrastructure.

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Банк Россия | В evidence уже есть кейс автоматизации AML-процессов, значит бюджет и pain подтверждены. | email decision-maker в комплаенсе + отраслевые AML-конференции | 900 000 ₽/мес |
| Сбербанк | Публично сообщил о применении AI-агента для комплаенс-расследований, значит buyer education уже начат. | партнёрский заход через интеграторов + конференции CNews | 1 200 000 ₽/мес |
| Совкомбанк | Большой объём SME/KYC-процессов и высокая нагрузка на anti-fraud/AML команды. | email head of compliance / procurement | 850 000 ₽/мес |
| Т-Банк | Digital-first risk stack и большой поток onboarding/monitoring кейсов. | warm intro через fintech ecosystem + targeted outreach | 1 000 000 ₽/мес |
| МТС Банк | Комбинация fintech growth и regulated onboarding создаёт регулярную потребность в AML case-handling. | email decision-maker + профильные fintech events | 800 000 ₽/мес |
| CarMoney | МФО/consumer lending требует потоковой risk-check и работы по 115-ФЗ. | direct outreach CFO/compliance lead | 600 000 ₽/мес |
| Займер | High-volume lender, где ручной AML/KYC контур особенно дорог. | outbound + webinar для risk/compliance | 650 000 ₽/мес |
| СберРешения | Бухгалтерский аутсорсинг прямо подпадает под 115-ФЗ pain из evidence по аутсорсерам. | партнёрство + email операционному директору | 500 000 ₽/мес |
| 1С-Рарус | Сильный канал внедрения в 1С-контур, где pain подтверждён запросом `1с проверка контрагентов`. | партнёрство с practice lead по compliance | 450 000 ₽/мес |
| Softline | Крупный корпоративный интегратор с enterprise-клиентами, которым можно продавать AI-layer как add-on к GRC и 1С. | partnership / совместный вебинар / account mapping | 700 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Комментарий |
|---|---|---|---|
| Incumbent capture risk | Высокая | Высокий | Value-capture и trust already sit у Контур.Фокуса, а AI-layer рискует остаться add-on без самостоятельного pricing power. |
| evidence_quality_unverified | Средняя | Средний | В `02-demand.md` нет строки `Sources: T1=..., T2=..., T3=...`, поэтому quality penalty обязателен и market score ограничен. |
| Service-heavy GTM и delivery | Высокая | Высокий | Если внедрение уйдёт в bespoke SI, margin и repeatability быстро деградируют. |

## Что должно быть доказано для APPROVED
1. 3-5 платящих российских reference-клиентов в банках/МФО/бухгалтерских аутсорсерах с чеком не ниже 600-900К ₽/мес.
2. Partner-led pipeline через 1С и интеграторов ≥40% новых сделок и blended CAC ≤900К ₽.
3. Стандартизованный onboarding ≤6 недель без ухода gross margin ниже 50%.
4. Независимый AI-layer, который сохраняет pricing power даже поверх incumbent data-source.

## LTV Upside Calculator
Чтобы перевести кейс из NEAR-PASS в APPROVED WITH NOTES, нужен один из апсайд-сценариев:

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 650 000 ₽/мес | 800 000 ₽/мес | Повышает contribution и снижает чувствительность к price compression. |
| CAC | 962 000 ₽ | ≤800 000 ₽ | Улучшает capital efficiency и сужает downside Monte Carlo. |
| Gross margin | 56,9% | ≥60% | Даёт больший запас против service-heaviness. |
| p10 EBITDA @M24 | -1 493 851 ₽ | ≥0 ₽ | Снимает главный risk-adjusted стоп-фактор. |
| Channel mix | partner-led ~0,9 wins/мес | partner-led ≥60% wins | Снижает CAC volatility и dependence on founder/AE motion. |

## Delta vs previous
- Раньше сигнал был лишь supporting input для `enterprise-compliance-operations-agents` и не имел standalone score.
- Текущий rerun впервые даёт самостоятельный инвестиционный verdict: **65/100, NEAR-PASS**.
- Апгрейд по сравнению с простым supporting signal в том, что теперь подтверждены unit economics, EBITDA path и конкретные GTM-условия, но moat и evidence-discipline пока не дотягивают до approve.

### Финальное решение инвесткомитета
**NEAR-PASS.**

Кейс интересен, потому что сочетает обязательный regulatory workflow, сильную client-level economics и достижимую EBITDA уже на первом году. Но approve пока рано: moat в основном принадлежит incumbent data/distribution layer, а не новому AI-слою, а evidence discipline и repeatable GTM ещё не дотягивают до investment-grade уровня.

## Артефакты
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/00-brief.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/01-intake.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/01-evidence.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/02-demand.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/04-economics.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/05-critic.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/06-verdict.md`
- `pipeline/rejected/kontur-focus-ai-compliance-russia-v2/07-score-trajectory.md`
