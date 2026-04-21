# 06-verdict

[GEO-EXPAND] 1528 MSK Hebbia GEO Expand v2 — NEAR-PASS: 65/100 | EBITDA base=627К₽/мес через 14 мес | LTV/CAC=29,3x | Ключевое преимущество: сильная enterprise unit economics в secure deal-room wedge | Главный риск: узкий локальный спрос и слабый moat.

sector: GEO-EXPAND

## Вердикт
**NEAR-PASS**

## Investment committee summary
Кейс проходит экономический gate и показывает сильный путь к `company_ebitda_rub_month >= 500 000 ₽/мес` при `<=50` клиентах, но пока не дотягивает до approve по двум причинам. Во-первых, в РФ подтверждён не широкий продуктовый спрос, а только узкий enterprise wedge вокруг M&A, due diligence и secure data-room workflows. Во-вторых, moat остаётся средне-слабым: нет network effects, локальный proprietary data advantage не доказан, а substitutes в виде VDR + консультанты + внутренние аналитики уже встроены в workflow клиента.

## Delta vs previous
- Ближайший сопоставимый rerun `1755-msk-hebbia-geo-expand-v2` был отклонён на **22/100** как demand-light institutional intelligence кейс.
- Текущий кейс поднимается до **65/100**, потому что в новом проходе доказаны `customer_ltv_rub=24,47 млн ₽`, `CAC=836 тыс. ₽`, `LTV/CAC=29,3x`, `GM=73,4%` и путь к `company_ebitda_rub_month=626,8 тыс. ₽/мес` уже к **M14**.
- Но до approve всё ещё не хватает более сильного локального demand proof, повторяемого GTM и более защищённого moat.

## Оценка
Source tier balance: T1=6, T2=12, T3=1, weighted=2.28. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | В 04-economics.md: `LTV/CAC = 29,3x`, `CAC Payback = 1,67 мес`, `Gross Margin = 73,4%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В 04-economics.md: `M14 ... EBITDA proxy +626 800`, а в 05-critic.md `p50 EBITDA @M24 = 820 000`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md: `Итог по спросу в РФ: LOW, но не нулевой`, при этом `SAM (РФ) ... 317 млн ₽` и endpoint остаётся `LOW`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | В 05-critic.md: основа защиты это `secure deployment + русскоязычный financial/legal corpus + deal workflow instrumentation`, но substitutes сильны. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В 05-critic.md отмечены `санкционные / vendor risks`, `клиенты требуют full on-prem`, `founder-led presales` и capital intensity 36-42 млн ₽. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | В 04-economics.md GTM опирается на `Founder-led outbound / ABM`, `партнёры` и blended CAC `836 000 ₽`, что реалистично для enterprise sales-led motion. |

**Сумма raw:** 98/150  
**Normalized score:** **65/100**

## 7-factor Moat framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не делает продукт заметно сильнее для остальных клиентов. |
| Switching costs | 2 | Интеграции, security review, импорт data room и обученность команды клиента создают умеренный lock-in. |
| Scale economies | 1 | Инфраструктура и playbooks улучшаются с объёмом, но enterprise presales остаётся тяжёлым. |
| Proprietary data / model advantage | 1 | Advantage есть только на приватных данных клиента; собственный датасет масштаба moat не доказан. |
| Regulatory moat | 1 | Compliance и private contour важны, но это скорее барьер входа, чем непроходимая крепость. |
| Brand / distribution | 1 | Локального brand pull нет, дистрибуция держится на founder-led продаже и партнёрах. |
| Embedded workflow | 3 | Продукт глубоко садится в due diligence, memo drafting и cross-doc review по data room. |

**Moat raw:** 9/21  
**Moat score:** **10/25**

## Почему это near-pass, а не approve
1. Экономика на клиента действительно сильная, но инвесткомитет покупает не только unit economics, а repeatable компанию. Здесь repeatability GTM ещё не доказана.
2. Спрос в РФ зафиксирован как `LOW`, а тезис держится на узком наборе high-value аккаунтов, а не на широком category pull.
3. Даже при хорошем EBITDA path модель зависит от founder-led продаж, partner intros и тяжёлого security/procurement цикла.
4. Moat лишь на нижней границе investment-grade: workflow embedding есть, но network effects, brand и proprietary data почти не работают.

## Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор таргет-аккаунтов: банки, Big Law, corpdev | CEO + SDR | CRM, Excel, hh/рынок, Telegram, сайты компаний | 2 дня | 18 000 | низкая |
| 2 | Первый outbound-touch: email, LinkedIn-аналоги, интро через партнёров | SDR | CRM, email sequencing, телефония | 7-10 дней | 55 000 | средняя |
| 3 | Discovery call и qualification | CEO + AE | Zoom/Meet, CRM | 1 неделя | 32 000 | средняя |
| 4 | NDA и обмен security-пакетом | AE + CTO | Dataroom, e-sign, почта | 3-5 дней | 27 000 | средняя |
| 5 | Персонализированное demo на sample data room | AE + CTO | Demo workspace, LLM/RAG stack | 1 неделя | 61 000 | средняя |
| 6 | Пилот-scoping, success criteria, список документов | AE + CTO + клиентский champion | Notion/Docs, CRM | 4-6 дней | 44 000 | низкая |
| 7 | Пилотный запуск и импорт документов | CTO + Backend + ML | Cloud, OCR, vector DB, SSO | 2-3 недели | 118 000 | средняя |
| 8 | Weekly review, правки промптов и схемы доступа | CSM + CTO | Slack/Telegram, issue tracker | 3-4 недели | 76 000 | средняя |
| 9 | Коммерческое согласование и budget owner approval | AE + CEO | CRM, коммерческое предложение | 1-2 недели | 49 000 | низкая |
| 10 | Security / legal / procurement review | CTO + CEO + юрист | DLP, документы, почта | 2-4 недели | 133 000 | низкая |
| 11 | Счёт, договор, активация оплаты | Finance ops + AE | 1С/банк, CRM | 3-7 дней | 18 000 | средняя |
| 12 | Получение оплаты и handoff в delivery/CS | Finance ops + CSM | Банк-клиент, CRM | 1-3 дня | 9 000 | высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 24 466 667 ₽ |
| CAC | 836 000 ₽ |
| LTV/CAC | 29,3x |
| CAC payback | 1,7 мес по revenue / 2,3 мес по gross profit |
| GM | 73,4% |
| contribution_margin_rub_month | 367 000 ₽ |
| company_ebitda_rub_month base @M14 | 626 800 ₽/мес |
| company_ebitda_potential_rub_month | 1 360 800 ₽/мес при 20 клиентах |
| clients_to_500k_ebitda | 18 |
| months_to_500k_ebitda | 14 |
| fixed_costs_rub_month | 5 979 200 ₽ |
| Break-even | 17 клиентов |
| startup_capital_to_bep_rub | 42 473 608 ₽ |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / founder | enterprise sales, fundraising, key accounts | 845 000 |
| CTO / Tech Lead | архитектура, security, enterprise presales | 715 000 |
| Senior Backend #1 | ingestion, APIs, RBAC, integrations | 585 000 |
| Senior Backend #2 | pipelines, performance, observability | 585 000 |
| ML Engineer | retrieval, evaluation, prompt optimization | 715 000 |
| DevOps | infra, deployment, backups, monitoring | 455 000 |
| Frontend | analyst workspace, admin UX | 390 000 |
| SDR | outbound prospecting, qualification | 239 200 |
| AE | demos, proposals, procurement close | 468 000 |
| Customer Success | onboarding, adoption, renewals | 312 000 |
| **Итого команда** |  | **5 309 200 ₽/мес** |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Слабый moat и price compression в enterprise wedge | high | high | Buyers уже умеют решать задачу через VDR + консультанты + internal analysts; при скидках >30% `EBITDA @M12 = -2 498 520 ₽`. |
| Security/on-prem complexity и регуляторика | high | high | В 05-critic.md: `клиенты требуют full on-prem / isolated contour`, что удлиняет цикл продажи и повышает COGS/CAC. |
| Зависимость от founder-led GTM и санкционных LLM-vendor deps | med-high | high | В 05-critic.md: `founder участвует в 100% сделок`, а `provider terms меняются, latency растёт`. |

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Газпромбанк | Активный M&A и проектное финансирование, document-heavy due diligence и IC memo workflows. | email decision-maker + отраслевые M&A конференции | 500 000 ₽/мес |
| Сбер CIB | Крупный контур investment banking и сложные data-room процессы, где важны speed + audit trail. | founder intro + email managing director | 600 000 ₽/мес |
| Альфа-Банк | Сильная corpfin и structured finance функция, высокая нагрузка на аналитиков и legal review. | ABM outreach + партнёрский интро через консультантов | 450 000 ₽/мес |
| Совкомбанк | Активный корпоративный блок и интеграционные сделки, где нужен быстрый cross-doc review. | email decision-maker + профильный форум | 400 000 ₽/мес |
| БКС КИБ | Узкий, но очень релевантный investment banking buyer с высокой ценностью экономии analyst-hours. | founder-led outbound + warm intro | 350 000 ₽/мес |
| Ренессанс Капитал | Classic institutional finance workflow, DD и memo drafting для сделок и размещений. | email decision-maker + конференция | 450 000 ₽/мес |
| АТОН | Бутик с high-value analyst time, где secure AI workspace может заменить часть ручного ресерча. | direct email partner/MD + referral | 300 000 ₽/мес |
| Kept | Transaction services и due diligence уже подтверждены в evidence, продукт может ускорить review больших room-пакетов. | партнёрство + demo для practice lead | 500 000 ₽/мес |
| Технологии Доверия | Большой объём DD, legal и M&A support, pain вокруг document comparison и synthesis. | email decision-maker + совместный roundtable | 500 000 ₽/мес |
| ДРТ | Transaction advisory и risk practices регулярно работают с data rooms и комплаенс-чувствительными документами. | partner outreach + конференция Big4-alumni | 450 000 ₽/мес |

## Proof points, которые нужны для approve
1. 3-5 платящих пилотов в РФ с price floor не ниже `400-500 тыс. ₽/мес` плюс setup fee.
2. Доказанный partner-led channel, который даёт не меньше 25% qualified pipeline без постоянного hero-sales фаундера.
3. Median pilot-to-paid conversion не ниже 30% и median security/procurement cycle не дольше 90 дней.
4. Повторяемый private deployment playbook, который не превращает каждый аккаунт в custom project.

## LTV Upside Calculator
Чтобы перевести кейс из **NEAR-PASS** в **APPROVED**, нужно улучшить не `customer_ltv_rub`, а repeatability и margin of safety. Ниже минимальные рычаги:

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| Paid clients к M12 | 16,0 | 18-20 | `company_ebitda_rub_month` становится устойчиво >500К₽/мес уже без optimistic assumptions. |
| ARPA / MRR | 500 000 ₽ | 550 000-600 000 ₽ | +50-100К₽ revenue на клиента даёт +0,9-1,8 млн ₽ EBITDA на 18 клиентах. |
| COGS на клиента | 133 000 ₽ | <=115 000 ₽ | Повышает `contribution_margin_rub_month` на 18 тыс. ₽ и усиливает запас по GM. |
| Fixed costs | 5 979 200 ₽ | <=5 300 000 ₽ | Снижает порог break-even на 2 клиента и уменьшает startup_capital. |
| Partner-sourced wins | <25% целевого | >=35% | Снижает CAC inflation и убирает часть founder dependence. |

## Финансовая интерпретация
Это не mass-SaaS и не search-led продукт. Правильная рамка, `secure enterprise deal-room copilot` для 15-30 российских аккаунтов верхнего сегмента. Если рынок подтверждает price floor и ускоряется partner channel, кейс может стать approve. Если же цена сползает в зону `150-300 тыс. ₽/мес`, тезис быстро превращается в service-heavy near-miss.

## Финальное решение
**NEAR-PASS.** Экономика уже сильнее многих GEO-EXPAND кейсов, но пока инвестиционный комитет не получает достаточно доказательств, что локальный спрос и GTM repeatability поддержат защитимую компанию, а не просто несколько дорогих внедрений.
