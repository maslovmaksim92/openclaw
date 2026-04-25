# 06-verdict

[B2B-OPS] AI-first финансовый оператор для SMB — APPROVED WITH NOTES: 71/100 | EBITDA base=602К₽/мес через 17 мес | LTV/CAC=19,4x | Ключевое преимущество: высокий retainer и productized finance ops поверх 1С/ЭДО | Главный риск: слабая доказанность demand-tier и price compression до уровня аутсорса.

sector: B2B-OPS

## Вердикт
**APPROVED WITH NOTES**

## Investment committee summary
Кейс проходит комитет только как **productized mid-market finance ops layer**, а не как массовый бухгалтерский аутсорс. Базовая экономика сильная: `customer_ltv_rub = 4 720 000 ₽`, `CAC = 243 100 ₽`, `LTV/CAC = 19.4x`, `CAC payback = 1.52 мес`, `GM = 73.8%`, `company_ebitda_rub_month = 602 000 ₽/мес` на 50 клиентах и выход выше **500К ₽/мес** через **17 месяцев** в base-case. Но approve даётся с оговорками, потому что evidence-quality по спросу не investment-grade, moat умеренный, а execution хрупок к `ARPU` ниже 130-160 тыс. ₽/мес и к service creep.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | `LTV/CAC = 19.4x`, `CAC Payback = 1.52 мес`, `Contribution Margin = 73.8%` в `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `EBITDA @ 50 clients = +602 000 ₽/мес`, `Break-even по времени: M15-M16`, а P6A даёт base break-even `M17`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | `Demand verdict: PASS WITH RESERVATIONS`, но в `02-demand.md` отсутствует строка `Sources: T1=...`, поэтому применён штраф качества evidence. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Есть глубина в `1С + ЭДО + bank feeds + human verification`, но рынок фрагментирован между `аутсорсом`, `1С-экосистемой` и `document-AI`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | `time-to-hire >2 мес`, `service creep`, `152-ФЗ`, санкции и LLM dependence описаны как high-risk в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | `Blended CAC = 243 100 ₽`, `CAC payback = 1.52 мес`, а ICP и каналы sales motion в `04-economics.md` выглядят повторяемыми. |

**Sum raw = 106 / 150. Normalized score = round((106 * 100) / 150) = 71/100.**

## Почему это APPROVED WITH NOTES
1. Кейс проходит обязательный gate: `company_ebitda_potential_rub_month = 602 000 ₽/мес` в base/near-base логике при `50` клиентах и в горизонте `17 мес`, то есть **≤50 клиентов и ≤24 месяцев**.
2. У клиента сильная unit economics на один аккаунт, поэтому бизнесу не нужен сотенный клиентский портфель, чтобы стать EBITDA-positive.
3. Платёжный контур уже существует в бюджете клиента, потому что покупка идёт из расходов на бухгалтерию, AP, первичку, payroll и finance admin, а не из экспериментального AI-бюджета.
4. Главный риск, это не отсутствие боли, а недоказанность масштабируемого локального GTM и защита от коммодитизации под классический аутсорс.

## FULL business process из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Генерация первичного лида | SDR + performance marketer | Яндекс.Директ, VK Ads, partner outreach, CRM | 1-14 дней | 18 000 | Средняя |
| 2 | Квалификация лида, first touch | SDR | amoCRM/Битрикс24, телефония, email sequencing | 30-45 мин | 2 200 | Средняя |
| 3 | Discovery call | AE | Zoom/Meet, CRM, call notes AI | 60 мин | 4 500 | Средняя |
| 4 | Сбор вводных: объём первички, банки, 1С, payroll | AE + Solution/Operations lead | Questionnaire, shared checklist | 2-3 дня | 6 500 | Низкая |
| 5 | Расчёт scope и коммерческого предложения | AE + CEO/Finance ops lead | Proposal template, калькулятор юнит-экономики | 1 день | 5 000 | Средняя |
| 6 | Security/legal review, договор | AE + CEO + юрист на аутсорсе | Документооборот, шаблон договора, ЭДО | 3-10 дней | 7 000 | Низкая |
| 7 | Выставление счёта | Finance ops | 1С, банк-клиент, ЭДО | 20 мин | 600 | Высокая |
| 8 | Оплата и активация клиента | Finance ops + Customer Success | Банк-клиент, CRM, billing | 1 день | 900 | Высокая |
| 9 | Onboarding: доступы, 1С, ЭДО, bank statements, шаблоны | CS + Finance ops specialist | 1С, Saby/Контур, shared drive, RPA | 3-5 рабочих дней | 9 500 | Средняя |
| 10 | Ежедневная обработка первички, AP, invoicing, reconciliations | Finance ops specialist | 1С, OCR, LLM extraction, RPA, bank feeds | Постоянно | 19 000 / мес | Средняя |
| 11 | Контроль качества и закрытие месяца | Chief accountant / QA | 1С, checklists, BI dashboard | 4-6 ч / мес | 7 000 / мес | Низкая |
| 12 | Продление / upsell / повторный платёж | CS + AE | CRM, QBR, BI, billing | 1-2 ч / мес | 2 500 / мес | Средняя |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | **4 720 000 ₽** |
| CAC fully-loaded | **243 100 ₽** |
| LTV/CAC | **19.4x** |
| CAC Payback | **1.52 мес** |
| GM / Contribution Margin | **73.8%** |
| Break-even clients | **45** |
| Break-even revenue | **7 200 000 ₽/мес** |
| Break-even month | **M17** в P6A base-case |
| contribution_margin_rub_month на клиента | **118 000 ₽/клиент/мес** |
| company_ebitda_rub_month @ 50 клиентов | **602 000 ₽/мес** |
| startup_capital_to_bep_rub | **44 980 738 ₽** |
| Startup capital working minimum | **40 000 000 ₽** |

## Team table
| Роль | Кол-во | Fully-loaded FOT ₽/мес | Time-to-hire | Комментарий |
|---|---:|---:|---:|---|
| CEO / Founder | 1 | 650 000 | 0 | founder-led sales и стратегия |
| CTO / Tech Lead | 1 | 585 000 | 2.0 мес | критичен для архитектуры и интеграций |
| Senior Backend | 2 | 910 000 | 1.5 мес | коннекторы, orchestration, API |
| ML Engineer | 1 | 585 000 | 2.5 мес | OCR/LLM prompts, extraction quality |
| DevOps | 1 | 390 000 | 1.5 мес | infra, monitoring, secrets |
| Frontend | 1 | 325 000 | 1.0 мес | кабинет и ops UI |
| Product / Ops Lead | 1 | 390 000 | н/д | упаковка оффера и процессы |
| SDR | 1 | 208 000 | 0.75 мес | outbound prospecting |
| AE | 1 | 390 000 | 1.5 мес | discovery, proposals, close |
| Customer Success | 1 | 260 000 | 1.0 мес | onboarding, retention, QBR |
| Finance Ops Specialist | 3 | 663 000 | н/д | ежедневный delivery |
| Chief Accountant / QA | 1 | 312 000 | н/д | контроль качества и закрытие месяца |
| **Итого** | **14** | **5 668 000 ₽/мес** |  | full operating team |

## Moat: 7-factor framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не делает продукт сильно лучше для остальных. |
| 2. Switching costs | 2 | Данные, процессы, 1С-коннекторы, ЭДО и monthly close создают умеренный lock-in. |
| 3. Scale economies | 2 | При стандартизации onboarding и QA COGS на клиента падает с объёмом. |
| 4. Proprietary data / model advantage | 1 | Может накопиться workflow-data по первичке и reconciliations, но пока нет доказанной базы данных. |
| 5. Regulatory moat | 1 | 152-ФЗ и локальный compliance больше как threshold, чем как настоящий moat. |
| 6. Brand / distribution | 1 | Пока нет сильного бренда или доминирующего канала дистрибуции. |
| 7. Embedded workflow | 3 | Продукт сидит в ежедневном finance back-office клиента и deeply embedded в month-end close. |

**Moat sum = 10 / 21. Moat score = round((10 * 25) / 21) = 12/25.**

## GTM: 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | 12 STOREEZ | fashion-retail с multi-entity учётом, большим объёмом AP, payroll и контуром поставщиков | партнёрство через 1С/финтех-интегратора + email CFO | 220 000 ₽/мес |
| 2 | DDX Fitness | сеть с recurring billing, payroll и большим операционным back-office | outbound на CFO/COO + профильная конференция fitness/retail ops | 180 000 ₽/мес |
| 3 | Skyeng | сервисный бизнес с высокой интенсивностью invoicing, payroll и reconciliations | email decision-maker + warm intro через CFO community | 240 000 ₽/мес |
| 4 | Нетология | edtech с recurring invoices, payroll для large ops-team и document-heavy back-office | outbound на finance director + vc.ru thought-leadership | 180 000 ₽/мес |
| 5 | FitStars | subscription/e-commerce модель, частые платежи и growing finance ops нагрузка | rb.ru / vc.ru channel targeting + founder/CFO outreach | 150 000 ₽/мес |
| 6 | Qummy | foodtech с закупками, B2B поставщиками и распределённым AP контуром | партнёрство с bank/ERP интегратором | 160 000 ₽/мес |
| 7 | SOKOLOV | retail + e-commerce + региональная сеть, высокие объёмы документооборота | enterprise outbound + отраслевой event | 250 000 ₽/мес |
| 8 | CDEK.Shopping / related e-com unit | cross-border/e-commerce operations увеличивают сложность finance back-office | email CFO + кейс через логистического партнёра | 170 000 ₽/мес |
| 9 | Авиасейлс | digital business с vendor invoices, payroll и потребностью в faster month-end close | direct outreach finance leader + Habr/vc.ru content | 190 000 ₽/мес |
| 10 | Flowwow | маркетплейс с большим AP/invoicing потоком и pain по quality finance operations | партнёрство с payment/ERP vendor + ABM outreach | 200 000 ₽/мес |

**Итог по GTM:** named-account ABM лучше mass-SMB. Наиболее реалистичный заход, это `1С/ЭДО/банк/интегратор-партнёр + CFO outreach + ROI-калькулятор по скорости закрытия и снижению manual FTE`.

## Top-3 risks
| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| ARPU / price compression до 90-120 тыс. ₽/мес | High | High | `05-critic.md` показывает, что `Price -30%` ухудшает `EBITDA @M12` до `-3 030 135 ₽/мес`. |
| Service creep и кастомные интеграции | High | High | Если onboarding превращается в project-heavy delivery, `GM` и путь к 45 клиентам ломаются. |
| evidence_quality_unverified | High | Medium | В `02-demand.md` нет строки `Sources: T1=..., T2=..., T3=...`, значит source-tier balance не подтверждён. |

## Proof points, которые оправдывают APPROVED
1. **Высокий unit margin:** `contribution_margin_rub_month = 118 000 ₽/клиент/мес` даёт быстрый payback и запас для sales motion.
2. **EBITDA gate проходит:** `company_ebitda_rub_month = 602 000 ₽/мес` на 50 клиентах в горизонте `17 мес`.
3. **Repeatable workflow существует:** `1С + ЭДО + bank feeds + AP + month-end close` образуют понятный recurring pain.
4. **Category proof есть:** Finally и Nanonets подтверждают, что bundled finance ops и AP automation продаются как отдельная категория.

## Что обязательно доказать после approve
1. Реальный `ARPU ≥ 140 000 ₽/мес` на первых 8-10 клиентах без deep discounting.
2. `Logo churn ≤ 3%/мес` и manual correction rate ниже 20%.
3. Что onboarding можно удержать в `3-5 рабочих дней`, а не в custom project cycle.
4. Что минимум 30-40% pipeline можно получать не только founder-led продажами, а через repeatable partner / outbound motion.

## Финальный вывод IC
Это **не clean SaaS**, а **SaaS-enabled managed finance ops business**. Для фонда это допустимо только потому, что чек высокий, payback быстрый, а путь к EBITDA ≥500К ₽/мес достигается без экстремального клиентского объёма. Но margin of safety средний, поэтому решение, это **APPROVED WITH NOTES**, а не unconditional approve.
