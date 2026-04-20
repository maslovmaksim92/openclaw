## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **300 000 ₽/мес**.
- COGS на клиента: **65 000 ₽/мес**.
- Gross profit / contribution на клиента: **235 000 ₽/мес**.
- Fixed costs: **5 980 000 ₽/мес**, включая полный FOT; страховые взносы уже заложены в FOT.
- Churn: **base 1.8% / optimistic 1.2% / pessimistic 3.0% в месяц**.
- Стартовый капитал для расчёта cumulative cash: **90 000 000 ₽**.
- Сценарии отличаются в первую очередь скоростью новых продаж: enterprise sales-led ramp, без разовых внедрений и без кредитного плеча.
- НДС 20% в PnL не включён в выручку при УСН/IT-льготе; для ОСНО учитывается отдельно как транзитный налог и давит на cash conversion.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 3.95 | 5.88 | 8.77 | 11.61 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 300 000 | 594 600 | 1 183 897 | 1 762 587 | 2 630 860 | 3 483 505 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 65 000 | 128 830 | 256 511 | 381 894 | 570 020 | 754 759 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 235 000 | 465 770 | 927 386 | 1 380 693 | 2 060 841 | 2 728 746 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 |
| EBITDA, ₽ | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 745 000 | -5 514 230 | -5 052 614 | -4 599 307 | -3 919 159 | -3 251 254 |
| Cash burn, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 745 000 | 5 514 230 | 5 052 614 | 4 599 307 | 3 919 159 | 3 251 254 |
| Cumulative cash, ₽ | 84 020 000 | 78 040 000 | 72 060 000 | 66 080 000 | 60 100 000 | 54 120 000 | 48 375 000 | 42 860 770 | 37 808 156 | 33 208 849 | 29 289 690 | 26 038 436 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 3.00 | 4.00 | 5.00 | 6.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 3.96 | 6.92 | 10.83 | 15.70 | 21.52 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 300 000 | 596 400 | 1 189 243 | 2 074 972 | 3 250 073 | 4 711 072 | 6 454 539 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 65 000 | 129 220 | 257 669 | 449 577 | 704 182 | 1 020 732 | 1 398 483 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 235 000 | 467 180 | 931 574 | 1 625 395 | 2 545 890 | 3 690 340 | 5 056 055 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 |
| EBITDA, ₽ | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 745 000 | -5 512 820 | -5 048 426 | -4 354 605 | -3 434 110 | -2 289 660 | -923 945 |
| Cash burn, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 745 000 | 5 512 820 | 5 048 426 | 4 354 605 | 3 434 110 | 2 289 660 | 923 945 |
| Cumulative cash, ₽ | 84 020 000 | 78 040 000 | 72 060 000 | 66 080 000 | 60 100 000 | 54 355 000 | 48 842 180 | 43 793 754 | 39 439 149 | 36 005 039 | 33 715 379 | 32 791 434 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.97 | 2.91 | 4.82 | 6.68 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 300 000 | 591 000 | 873 270 | 1 447 072 | 2 003 660 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 65 000 | 128 050 | 189 208 | 313 532 | 434 126 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 235 000 | 462 950 | 684 062 | 1 133 540 | 1 569 533 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 |
| EBITDA, ₽ | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 980 000 | -5 745 000 | -5 517 050 | -5 295 938 | -4 846 460 | -4 410 467 |
| Cash burn, ₽ | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 980 000 | 5 745 000 | 5 517 050 | 5 295 938 | 4 846 460 | 4 410 467 |
| Cumulative cash, ₽ | 84 020 000 | 78 040 000 | 72 060 000 | 66 080 000 | 60 100 000 | 54 120 000 | 48 140 000 | 42 395 000 | 36 877 950 | 31 582 012 | 26 735 551 | 22 325 085 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Unit waterfall на 1 клиента / мес
- **ARPA:** 300 000 ₽
- **COGS:** 65 000 ₽
- **Gross profit:** 235 000 ₽
- **Contribution:** 235 000 ₽, потому что переменные non-COGS расходы в кейсе не выделены отдельно

#### Waterfall на steady-state 33 клиентах
- **Revenue:** 9 900 000 ₽/мес
- **Gross profit / Contribution:** 7 755 000 ₽/мес
- **EBITDA:** 7 755 000 - 5 980 000 = **1 775 000 ₽/мес**
- **Net profit при УСН 6%:** 1 775 000 - 594 000 = **1 181 000 ₽/мес**
- **Net profit при IT-льготе 3%:** 1 775 000 - 297 000 = **1 478 000 ₽/мес**
- **Net profit при ОСНО 20%:** 1 775 000 - 355 000 = **1 420 000 ₽/мес**
- **Важно:** при ОСНО сверху возникает **НДС 20%**, который не равен прибыли и ухудшает cash flow, если входной НДС ограничен.

### A6. Cash flow и startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M13 | 57 208 566 ₽ | Быстрый ramp до ~27.3 клиентов при churn 1.2% |
| Base | M18 | 70 612 551 ₽ | Соответствует логике исходного economics, break-even после выхода за 27 клиентов |
| Pessimistic | M25 | 90 983 804 ₽ | 90 млн ₽ уже почти не хватает, нужен резерв > 91 млн ₽ |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** самая простая модель для ранней стадии, но при низкой EBITDA может давить сильнее, чем налог на прибыль.
- **IT-льгота 3% с выручки:** лучший режим для этого кейса, если есть аккредитация Минцифры и соблюдены критерии профильной выручки.
- **ОСНО 20% налог на прибыль:** экономически терпимо только после выхода на устойчивую прибыль; дополнительно появляется **НДС 20%** и более тяжёлый админ-контур.
- **Страховые взносы ~30% к ФОТ:** уже встроены в FOT и fixed costs, повторно не добавляются.
- Для cash planning я бы базово закладывал **УСН 6%**, а upside показывал через **IT-льготу 3%** как post-accreditation improvement.

### A8. Break-even по client count и по месяцам
| Scenario | Break-even clients | Break-even month | Комментарий |
|---|---:|---:|---|
| Optimistic | 26 | M13 | фактически модель пересекает EBITDA 0 около **27.3 клиента** |
| Base | 26 | M18 | фактически пересечение около **27.6 клиента** |
| Pessimistic | 26 | M25 | фактически пересечение около **26.3 клиента** |

## SECTION B. Finance risk + competitor deep-dive

### B1. Sensitivity analysis, EBITDA через 12 месяцев
Ниже стресс-тест на базе существующей PnL-модели из SECTION A. Для `CAC x2` я считаю **economic EBITDA after growth CAC**, потому что иначе рост CAC не отражается в PnL; для churn и price shock считаю операционный эффект на ту же клиентскую траекторию. [T1]

| Scenario | Ключевое изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | текущая модель | **-3 251 254** | 11.61 клиента к M12, модель ещё в фазе burn [T1] |
| Sens1 | CAC x2 | **-6 555 254** | при сохранении темпа продаж growth-spend почти удваивает burn; это главный риск cash runway [T1] |
| Sens2 | Churn x2 | **-3 338 984** | эффект к M12 пока умеренный, но к M18-M24 становится кумулятивно опасным [T1] |
| Sens3 | Price -30% | **-4 296 306** | падение ARPU сильнее бьёт по EBITDA, чем удвоение churn на первом году [T1] |

### B2. Monte Carlo Lite, confidence intervals
#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 100 000 | 1 418 000 | 2 836 000 | базовый CAC из 04-economics + stress `x2` [T1] |
| Monthly churn, % | 1.2% | 1.8% | 3.6% | optimistic/base из SECTION A + stress `x2` [T1] |
| ARPU, ₽/мес | 210 000 | 300 000 | 360 000 | base ARPU 300k, downside `-30%`, upside через enterprise upsell [T1][T2] |
| Conversion rate lead→paid, % | 1.0% | 1.5% | 2.5% | выведено из blended funnel sales-led motion [T1] |
| Time-to-hire, мес | 1.0 | 1.8 | 3.0 | диапазон по hiring realism table [T1] |

#### Метод
Вместо полного кода использован `Monte Carlo Lite`: 9 комбинаций min/mode/max по CAC, churn, ARPU, conversion и time-to-hire. p10 взят как нижний хвост, p50 как median-case, p90 как верхний хвост. EBITDA считается на M24 по той же клиентской динамике, что и в SECTION A, но с корректировкой на conversion и hiring drag после M12. Это приближение, не полноценная стохастическая симуляция. [T1]

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 674 925** | **3 885 059** | **15 107 823** | **17 782 748** |
| CAC payback, мес | **17.2** | **6.0** | **3.9** | **13.3** |
| LTV/CAC | **1.6x** | **9.2x** | **21.4x** | **19.8x** |
| Cash runway, мес | **16.3** | **16.9** | **17.3** | **1.0** |

#### Вывод по Monte Carlo Lite
1. **Rule #1 triggered:** p10 EBITDA @M24 **ниже нуля**, значит downside уже указывает на риск экономической несостоятельности.
2. **Rule #2 not triggered:** p50 EBITDA @M24 = **3.89 млн ₽/мес**, то есть median-case проходит EBITDA Gate.
3. **Rule #3 triggered по сути:** распределение слишком широкое, потому что нижний хвост отрицательный, а верхний хвост >15 млн ₽/мес; это значит, что score надо даунгрейдить за высокую дисперсию execution outcomes.
4. **Rule #4 triggered:** width по LTV/CAC = **19.8x**, модель хрупкая, и хрупкость почти целиком сидит в pricing discipline, CAC и churn. [T1]

### B3. Competitor deep-dive
Оценки market share ниже, это **инференс по видимости категории, числу enterprise deployments, публичным кейсам и ценовой/дистрибуционной силе**, а не аудированная доля рынка. Я оцениваю долю в **adjacent enterprise knowledge search / AI assistant segment**, а не во всём software market. [Inference][T2][T3]

#### Top-3 западных
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Glean** | сильный enterprise search UX, коннекторы, хороший brand pull у крупных knowledge teams | слабая локализация под РФ, санкционный и data residency риск, cloud-first DNA | **8-12% global adjacent segment** [Inference] | on-prem/private contour, русскоязычные corpora, кастомизация под банки/телеком РФ |
| **Coveo** | зрелая search relevance платформа, e-commerce + enterprise search опыт, аналитика | более «platform-heavy», чем workflow-heavy analyst copilot; сложнее продавать как turnkey knowledge copilot | **6-9%** [Inference] | можем продавать не search layer, а end-to-end secure analyst workflow |
| **Sinequa** | глубокий enterprise search, security, сложные regulated deployments | тяжёлое внедрение, высокая стоимость и длительный presale | **4-7%** [Inference] | ниже TCO, быстрее pilot-to-value, проще адаптировать под локальные data-perimeter требования |

#### Top-4 российских
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Yandex Search API / AI Search** | крупнейшая инфраструктурная дистрибуция, узнаваемость, сильная search-технология | это building block, а не полнофункциональный analyst copilot; enterprise workflow и permissions layer надо достраивать | **20-25% RF adjacent infra layer** [Inference] | мы выше по стеку: citations, workflow orchestration, document reasoning, private contour |
| **TEAMLY** | локальная база знаний с AI-слоем, доступный прайс, быстрое внедрение | ближе к wiki/knowledge base, чем к тяжёлому документному анализу enterprise-класса | **5-8% RF knowledge-assistant segment** [Inference] | лучше fit для банков/телекома с большими массивами неструктурированных документов |
| **Just AI JAICP** | сильный conversational AI, омниканальность, on-prem, mature enterprise sales | ядро ценности всё же в bot/dialog layer, а не в analyst-grade deep research по документам | **8-12% RF enterprise conversational AI / RAG** [Inference] | мы лучше закрываем non-chat use case: аналитик, юрист, procurement, due diligence |
| **SL Soft AI Search / knowledge stack** | хороший локальный корпоративный контур, интеграционный fit для крупных компаний | меньше brand gravity и product mindshare, часто выигрывает через интеграторский канал, а не product pull | **4-6% RF adjacent segment** [Inference] | можем быть быстрее, продуктово чище и сильнее в UX cited answers + multi-step reasoning |

#### Короткий вывод по конкурентам
- На Западе рынок уже подтверждён, но для РФ почти все top players упираются в **санкции, hosting, data residency и procurement friction**.
- В РФ уже есть локальные substitutes, но большинство из них либо **ниже по стеку** как search/API, либо **сбоку** как knowledge base/chatbot.
- Значит, окно для кейса реально существует, но только если продукт удержит позиционирование **secure enterprise knowledge copilot**, а не съедет в generic bot platform. [T2][T3]

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Нехватка сильного ML/RAG-лида | med | high | >90 дней без закрытия ML-вакансии, деградация retrieval quality | заранее нанимать principal-level ML, держать advisor bench, упростить MVP scope [T1] |
| Operational | LLM API / inference instability | high | high | рост latency, рост стоимости токенов, падение SLA | multi-model routing, fallback на open-weight/on-prem модели, лимиты usage [T1][T3] |
| Market | Спрос остаётся category-curious, но не budget-backed | med | high | много пилотов, мало paid conversion, длинный procurement >120 дней | ICP only enterprise, продавать ROI/use-case, не распыляться на SMB [T2] |
| Market | Price compression из-за локальных аналогов и интеграторов | high | high | скидки >25%, сделки уходят в RFP с lowest bid | держать vertical workflows, security moat и citations, не конкурировать чисто ценой [T2][T3] |
| Regulatory | 152-ФЗ / data residency блокирует cloud deployment | high | high | security/legal red flags уже на pre-sale, требование on-prem с первой встречи | private contour по умолчанию, локальное хранение embeddings/logs, DPA + threat model [T2][T3] |
| Regulatory | 115-ФЗ / compliance и audit trail недостаточны для банков | med | high | банк требует explainability, audit logs, role-based access, а продукт даёт только chat UX | audit trail, immutable logs, citations, role-based permissions, red-team с клиентом [T2] |
| Financial | Cash runway сжимается из-за CAC inflation | high | high | CAC payback >9 мес, pipeline coverage <3x quota | урезать burn, сместиться в founder-led sales, партнёры вместо paid acquisition [T1] |
| Financial | USD/RUB и инфляция раздувают infra/FOT | med | med | рост COGS >20% QoQ, salary reset market-wide | рублёвые контракты с индексацией, open-source fallback, quarterly repricing [T1] |
| Black swan | Новые санкции режут доступ к западным SaaS/моделям | high | high | vendor notices, отключение billing или API keys | vendor diversification, локальные substitutes, резервный стек open-source [T3] |
| Black swan | Внешний шок, война/кибератака/полное отключение модели | med | high | длительный outage, запрет каналов/облаков, forced infra migration | disaster recovery plan, self-hosted inference, офлайн ingestion queue, резервный контур [T3] |

### B5. Kill conditions, если смотреть на метрики через 6 месяцев
1. **Kill #1, insolvency risk:** если к M6 обновлённый `p10 EBITDA @M24 < 0` **и** cash runway упал ниже **12 месяцев**, продолжать нельзя.
2. **Kill #2, economics gate:** если к M6 `p50 EBITDA @M24 < 500 000 ₽/мес` **или** CAC payback устойчиво выше **12 месяцев**, кейс надо закрывать.
3. **Kill #3, GTM/product fit:** если к M6 `LTV/CAC < 3x` **или** monthly logo churn > **3.5%** два месяца подряд **или** меньше **2 платящих enterprise клиентов**, продолжать нельзя. [T1][T2]

### B6. Bottom line
- Кейс остаётся **живым**, но только в median/upside исходе.
- Главный risk cluster здесь не в demand as such, а в **execution volatility**: CAC, price discipline, regulated deployment complexity.
- Я бы **даунгрейдил confidence**, но не закрывал кейс автоматически: median-case всё ещё сильный, а RF-local moat против западных игроков выглядит правдоподобно.

### Sources for SECTION B
- **T1**: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1927-msk-hebbia-geo-expand-v2/04-economics.md`
- **T2**: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1927-msk-hebbia-geo-expand-v2/02-demand.md`
- **T3**: Glean https://www.glean.com/ , Coveo https://www.coveo.com/ , Sinequa https://www.sinequa.com/ , Yandex Search API pricing https://yandex.cloud/ru/docs/search-api/pricing , TEAMLY https://teamly.ru/ and Habr article https://habr.com/ru/companies/qsoft/articles/829478/ , Just AI JAICP https://just-ai.com/platforma-jaicp and Skolkovo profile https://sk.ru/technopark/residents/just-ai/ , SL Soft AI Search / enterprise stack https://slsoft.ru/

<!-- P6A-DONE -->
<!-- P6B-DONE -->
