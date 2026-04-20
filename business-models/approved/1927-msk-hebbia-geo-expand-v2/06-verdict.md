# 06-verdict

[GEO-EXPAND] 1927 MSK Hebbia GEO Expand v2 — APPROVED: 72/100 | EBITDA base=5770К₽/мес через 24 мес | LTV/CAC=9.2x | Ключевое преимущество: strong secure enterprise workflow economics для закрытого контура | Главный риск: price compression и длинный regulated sales cycle.

sector: GEO-EXPAND

## Вердикт
**APPROVED WITH NOTES**

## Investment committee summary
Кейс проходит порог инвесткомитета за счёт сильной unit economics, достижимого пути к `company_ebitda_rub_month ≥ 500 000 ₽/мес` при `<=50` клиентах и понятного enterprise ICP. Но это approve без большого запаса прочности: локальный moat средний, outcome dispersion высокая, а спрос подтверждён скорее category-level evidence, чем прямым brand pull.

## Delta vs previous
- Предыдущий близкий Hebbia-rerun `1755-msk-hebbia-geo-expand-v2` был отклонён на **22/100** как demand-light standalone category.
- Текущий кейс переходит в **72/100**, потому что в новом проходе доказаны `LTV/CAC=9.2x`, `CAC payback=4.7 мес`, путь к **5.77 млн ₽/мес EBITDA** при 50 клиентах и рабочий RF enterprise ICP.
- Главный сдвиг в оценке: не «бренд Hebbia в РФ», а `secure enterprise knowledge copilot` как локализуемый product wedge для банков, телекома и промышленности.

## Оценка
Source tier balance: T1=3, T2=6, T3=0, weighted=2.33. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `LTV/CAC: 9.2x`, `CAC Payback: 4.7 мес`, `Contribution Margin: 78.3%` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `M19: 33 клиента -> EBITDA break-even`, а при `50 клиентах ... ~5.77 млн ₽` и gate проходит уверенно. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | В 02-demand.md: `рынок GenAI-решений в РФ ... 58 млрд ₽`, `hh_vacancies=179`, но `брендовый спрос ... почти отсутствует`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Moat держится на `on-prem/private contour, русскоязычные corpora` и embedded workflow, но brand/network effects слабые. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | В 05-critic.md зафиксированы `LLM API / inference instability`, `152-ФЗ / data residency`, `cash runway сжимается из-за CAC inflation`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 23 | `sales cycle: 8-14 недель`, `Fully-loaded CAC = 1.418 млн ₽`, ICP уже сужен до 10 named enterprise targets. |

**Сумма raw:** 108/150  
**Normalized score:** **72/100**

## 7-factor Moat framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных клиентов. |
| Switching costs | 2 | Глубокие интеграции, ACL, security review и обученность аналитиков создают умеренный lock-in. |
| Scale economies | 1 | Инфра и GTM улучшаются с объёмом, но enterprise presale остаётся тяжёлым. |
| Proprietary data / model advantage | 1 | Есть advantage на private corpora клиента, но публично не доказан крупный собственный датасет. |
| Regulatory moat | 2 | Требования по 152-ФЗ, audit trail и private contour создают барьер входа, но не непроходимый moat. |
| Brand / distribution | 1 | Категория известна, но локальный brand pull слабый и основа дистрибуции sales-led. |
| Embedded workflow | 3 | Продукт встраивается в due diligence, legal review, procurement и internal research workflows. |

**Moat raw:** 10/21  
**Moat score:** **12/25**

## Почему approve, а не near-pass
1. `customer_ltv_rub = 13.05 млн ₽` при `CAC = 1.418 млн ₽` даёт инвестиционно пригодный запас по unit economics.
2. `company_ebitda_rub_month` в базовом зрелом состоянии проходит порог не только формально, а с запасом: `~1.775 млн ₽/мес` на 33 клиентах и `~5.77 млн ₽/мес` на 50 клиентах.
3. GTM не опирается на wishful thinking по search demand, а на enterprise outbound, referrals и partners, что соответствует сегменту.
4. Downside серьёзный, но не смертельный: даже Monte Carlo Lite показывает `p50 EBITDA @M24 = 3.89 млн ₽/мес`.

## Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Формирование target account list | CEO + SDR | CRM, Excel, ручной research | 3 ч на аккаунт | 3,500 | Низкая |
| 2 | Обогащение контактов ЛПР | SDR | CRM, email finder, Telegram/manual | 1.5 ч | 1,300 | Средняя |
| 3 | Первый outbound outreach, 5-7 касаний | SDR | CRM sequences, почта, звонки | 2 недели | 7,500 | Средняя |
| 4 | Qualification call | SDR + AE | Meet/Zoom, CRM | 45 мин | 2,700 | Низкая |
| 5 | Discovery по workflow и security constraints | AE + CEO | Meet/Zoom, CRM | 1.5 ч | 8,000 | Низкая |
| 6 | Подготовка demo environment / pilot scope | CTO + ML + Backend | Cloud/GPU, demo tenant | 3-5 дней | 28,000 | Средняя |
| 7 | Product demo + ROI framing | AE + CEO | Meet/Zoom, deck, demo | 1.5 ч | 9,500 | Низкая |
| 8 | Security / legal / IT review | CTO + CEO | Docs, security checklist, DPA/SLA | 2-4 недели | 42,000 | Низкая |
| 9 | Pilot setup / sandbox integration | Backend + ML + DevOps | API, connectors, on-prem deploy | 2-3 недели | 95,000 | Средняя |
| 10 | Pilot support и weekly QBR | CSM + AE + ML | Slack/Telegram, CRM, dashboards | 4 недели | 36,000 | Средняя |
| 11 | Коммерческое предложение и redlines | AE + CEO | CRM, docs, e-sign | 1 неделя | 15,000 | Низкая |
| 12 | Procurement / PO / invoice | Finance ops + AE | ЭДО, 1С/аналог, CRM | 1 неделя | 8,000 | Высокая |
| 13 | Оплата и handoff в customer success | Finance + CSM | Банк-клиент, CRM, billing | 2 дня | 4,000 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 13 050 000 ₽ |
| CAC | 1 418 000 ₽ |
| LTV/CAC | 9.2x |
| CAC payback | 4.7 мес |
| GM / contribution margin | 78.3% |
| Break-even clients | 26 operational / 33 с активным GTM-spend |
| Break-even month | M17 operational / M19 EBITDA |
| contribution_margin_rub_month | 235 000 ₽/клиент/мес |
| company_ebitda_rub_month base @33 clients | 1 775 000 ₽/мес |
| company_ebitda_potential_rub_month @50 clients | 5 770 000 ₽/мес |
| clients_to_500k_ebitda | 28 |
| months_to_500k_ebitda | 18 |
| fixed_costs_rub_month | 5 980 000 ₽ |
| startup_capital_to_bep_rub | 70 612 551 ₽ |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | enterprise sales, fundraising, partnerships | 845,000 |
| CTO / Tech Lead | архитектура, security, внедрения | 715,000 |
| Senior Backend x2 | ingestion, API, integrations | 1,092,000 |
| ML Engineer | RAG quality, retrieval, evaluation | 650,000 |
| DevOps | infra, k8s, private contour | 455,000 |
| Frontend | analyst UI, permissions UX | 390,000 |
| SDR | outbound prospecting | 234,000 |
| AE | demos, negotiation, close | 507,000 |
| Customer Success | onboarding, adoption, expansion | 312,000 |
| **Итого команда** |  | **5,200,000 ₽/мес** |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Price compression и скидки >25% | high | high | В 05-critic.md: `Price -30%` уводит `EBITDA @M12` до `-4.30 млн ₽`, а конкуренты и интеграторы давят на pricing. |
| Регуляторика, data residency, private deployment complexity | high | high | `152-ФЗ / data residency блокирует cloud deployment`, а security/legal friction удлиняет продажу и COGS. |
| CAC inflation и execution volatility | high | high | `CAC x2` ведёт к `-6.56 млн ₽ EBITDA @M12`, Monte Carlo даёт отрицательный `p10 EBITDA @M24`. |

## Proof points для APPROVED
1. `company_ebitda_potential_rub_month` выше `500 000 ₽/мес` задолго до 50 клиентов и в пределах 24 месяцев.
2. 10 конкретных enterprise targets уже видны и совпадают с pain profile: document-heavy, regulated, budget-backed.
3. Category demand подтверждён не только поиском, но и `179` HH-сигналами, локальными платными аналогами и TAM/SAM в миллиардах рублей.
4. Кейс не требует consumer-scale adoption; достаточно 20-35 крупных аккаунтов с `ACV 3.6 млн ₽/год`.

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Огромный массив внутренних документов, legal/compliance/research workflows, высокий бюджет на AI. | email decision-maker + отраслевые конференции + партнёрство с интегратором | 500,000 ₽/мес |
| Т-Банк | Data-heavy knowledge teams и быстрый rollout AI-инструментов для аналитики и ops. | founder-led intro + email decision-maker | 450,000 ₽/мес |
| ВТБ | Сильная документная и регуляторная нагрузка, потребность в audit trail и private contour. | тендерный вход + партнёрство с SI | 450,000 ₽/мес |
| Альфа-Банк | Активная digital-функция, большой объём policy/legal/procurement documents. | email decision-maker + профильная конференция | 400,000 ₽/мес |
| МТС | Крупный enterprise knowledge perimeter и множество внутренних сервисных процессов. | партнёрство + ABM outreach | 350,000 ₽/мес |
| билайн | Сложные внутренние документы, IT/security требования и большой procurement contour. | email decision-maker + кейс через интегратора | 350,000 ₽/мес |
| Северсталь | Промышленный enterprise с технической документацией и закупочными/юридическими workflow. | отраслевые мероприятия + партнёрство | 300,000 ₽/мес |
| Норникель | Много регламентов, договоров и внутренней базы знаний, высокий эффект от secure retrieval. | email decision-maker + enterprise referral | 300,000 ₽/мес |
| СИБУР | Сложные техпроцессы и большая база документов, где нужен controlled access и citations. | партнёрский канал + конференция | 300,000 ₽/мес |
| X5 Group | Масштабный corporate knowledge stack, procurement/legal/support pain, быстрая экономия времени аналитиков. | ABM outbound + referral | 250,000 ₽/мес |

## Финансовая интерпретация
- Бизнес выглядит как `enterprise sales-led AI workflow platform`, а не как классический SMB SaaS.
- Главный драйвер доходности, удержание `ARPA = 300 000 ₽/мес` и дисциплины по COGS `65 000 ₽/мес`.
- При `33` клиентах бизнес уже проходит устойчивый EBITDA gate, а при `50` клиентах превращается в сильный cash-generating asset.

## Что нужно доказать в ближайшие 6 месяцев
1. 2-3 paid pilots в банках, телекоме или промышленности без скидочного демпинга.
2. Median pilot-to-paid conversion не ниже 30% и CAC payback не выше 8 месяцев.
3. Private contour / on-prem deployment playbook, который не превращает каждый проект в custom integration shop.
4. Стабильный channel mix: founder-led inbound + ABM + integrator referrals, а не только hero-sales фаундера.

## Финальное решение
**APPROVED** при условии строгой product discipline: продавать `secure enterprise knowledge copilot`, а не generic chatbot или кастомную интеграторскую разработку. Если pricing discipline нарушится или private deployment раздует COGS, кейс быстро деградирует до near-pass.
