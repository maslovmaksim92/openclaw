## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **500 000 ₽/мес**.
- COGS на клиента: **133 000 ₽/мес**.
- Gross profit на клиента: **367 000 ₽/мес**.
- Contribution после variable success/sales allocation: **342 000 ₽/клиент/мес**.
- Fixed costs: **5 979 200 ₽/мес**.
- Full team FOT: **5 309 200 ₽/мес**.
- Налоговые сценарии для net profit: **УСН 6%**, **IT-льгота 3%**, **ОСНО 20%** на прибыль; на ОСНО дополнительно есть кассовое давление НДС.
- Страховые взносы **~30% к ФОТ** уже включены в FOT / fixed costs.
- Для 12-месячного PnL беру три сценария продаж:
  - **Base:** new clients = 0,0,1,1,1,2,2,2,2,2,2,2; churn **1,5%/мес**.
  - **Optimistic:** new clients = 0,1,1,1,2,2,2,2,2,2,3,3; churn **1,0%/мес**.
  - **Pessimistic:** new clients = 0,0,0,1,1,1,1,1,1,1,1,1; churn **2,5%/мес**.
- Cumulative cash в таблицах показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.96 | 4.91 | 6.84 | 8.73 | 10.60 | 12.44 | 14.26 | 16.04 |
| MRR, ₽ | 0 | 0 | 500 000 | 992 500 | 1 477 612 | 2 455 448 | 3 418 617 | 4 367 337 | 5 301 827 | 6 222 300 | 7 128 965 | 8 022 031 |
| COGS, ₽ | 0 | 0 | 133 000 | 264 005 | 393 045 | 653 149 | 909 352 | 1 161 712 | 1 410 286 | 1 655 132 | 1 896 305 | 2 133 860 |
| Gross profit, ₽ | 0 | 0 | 367 000 | 728 495 | 1 084 568 | 1 802 299 | 2 509 265 | 3 205 626 | 3 891 541 | 4 567 168 | 5 232 661 | 5 888 171 |
| GM% | 0.0% | 0.0% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% |
| Fixed costs, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 |
| EBITDA, ₽ | -5 979 200 | -5 979 200 | -5 612 200 | -5 250 705 | -4 894 632 | -4 176 901 | -3 469 935 | -2 773 574 | -2 087 659 | -1 412 032 | -746 539 | -91 029 |
| Cash burn, ₽ | 5 979 200 | 5 979 200 | 5 612 200 | 5 250 705 | 4 894 632 | 4 176 901 | 3 469 935 | 2 773 574 | 2 087 659 | 1 412 032 | 746 539 | 91 029 |
| Cumulative cash, ₽ | -5 979 200 | -11 958 400 | -17 570 600 | -22 821 305 | -27 715 937 | -31 892 838 | -35 362 774 | -38 136 348 | -40 224 007 | -41 636 039 | -42 382 578 | -42 473 608 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 1.00 | 1.99 | 2.97 | 4.94 | 6.89 | 8.82 | 10.73 | 12.63 | 14.50 | 17.36 | 20.18 |
| MRR, ₽ | 0 | 500 000 | 995 000 | 1 485 050 | 2 470 199 | 3 445 498 | 4 411 043 | 5 366 932 | 6 313 263 | 7 250 130 | 8 677 629 | 10 090 853 |
| COGS, ₽ | 0 | 133 000 | 264 670 | 395 023 | 657 073 | 916 502 | 1 173 337 | 1 427 604 | 1 679 328 | 1 928 535 | 2 308 249 | 2 684 167 |
| Gross profit, ₽ | 0 | 367 000 | 730 330 | 1 090 027 | 1 813 126 | 2 528 995 | 3 237 705 | 3 939 328 | 4 633 935 | 5 321 596 | 6 369 380 | 7 406 686 |
| GM% | 0.0% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% |
| Fixed costs, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 |
| EBITDA, ₽ | -5 979 200 | -5 612 200 | -5 248 870 | -4 889 173 | -4 166 074 | -3 450 205 | -2 741 495 | -2 039 872 | -1 345 265 | -657 604 | 390 180 | 1 427 486 |
| Cash burn, ₽ | 5 979 200 | 5 612 200 | 5 248 870 | 4 889 173 | 4 166 074 | 3 450 205 | 2 741 495 | 2 039 872 | 1 345 265 | 657 604 | 0 | 0 |
| Cumulative cash, ₽ | -5 979 200 | -11 591 400 | -16 840 270 | -21 729 443 | -25 895 517 | -29 345 722 | -32 087 216 | -34 127 088 | -35 472 353 | -36 129 958 | -35 739 778 | -34 312 293 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 4.76 | 5.64 | 6.50 | 7.33 | 8.15 |
| MRR, ₽ | 0 | 0 | 0 | 500 000 | 987 500 | 1 462 812 | 1 926 242 | 2 378 086 | 2 818 634 | 3 248 168 | 3 666 964 | 4 075 290 |
| COGS, ₽ | 0 | 0 | 0 | 133 000 | 262 675 | 389 108 | 512 380 | 632 571 | 749 757 | 864 013 | 975 412 | 1 084 027 |
| Gross profit, ₽ | 0 | 0 | 0 | 367 000 | 724 825 | 1 073 704 | 1 413 862 | 1 745 515 | 2 068 877 | 2 384 155 | 2 691 552 | 2 991 263 |
| GM% | 0.0% | 0.0% | 0.0% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% |
| Fixed costs, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 |
| EBITDA, ₽ | -5 979 200 | -5 979 200 | -5 979 200 | -5 612 200 | -5 254 375 | -4 905 496 | -4 565 338 | -4 233 685 | -3 910 323 | -3 595 045 | -3 287 648 | -2 987 937 |
| Cash burn, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 612 200 | 5 254 375 | 4 905 496 | 4 565 338 | 4 233 685 | 3 910 323 | 3 595 045 | 3 287 648 | 2 987 937 |
| Cumulative cash, ₽ | -5 979 200 | -11 958 400 | -17 937 600 | -23 549 800 | -28 804 175 | -33 709 671 | -38 275 009 | -42 508 694 | -46 419 016 | -50 014 061 | -53 301 709 | -56 289 647 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 500 000 ₽
- **COGS:** 133 000 ₽
- **Gross profit:** 367 000 ₽
- **Variable sales/support:** 25 000 ₽
- **Contribution:** 342 000 ₽

#### Waterfall на EBITDA break-even уровне 18 клиентов
- **Revenue:** 9 000 000 ₽/мес
- **COGS:** 2 394 000 ₽/мес
- **Gross profit:** 6 606 000 ₽/мес
- **Fixed costs:** 5 979 200 ₽/мес
- **EBITDA:** **626 800 ₽/мес**

#### Net profit после налогов
- **УСН 6%:** 626 800 - 540 000 = **86 800 ₽/мес**
- **IT-льгота 3%:** 626 800 - 270 000 = **356 800 ₽/мес**
- **ОСНО 20%:** 626 800 × 0,8 = **501 440 ₽/мес** до учёта эффекта НДС

#### Waterfall на target profit gate, 20 клиентов
- **Revenue:** 10 000 000 ₽/мес
- **COGS:** 2 660 000 ₽/мес
- **Gross profit:** 7 340 000 ₽/мес
- **EBITDA:** **1 360 800 ₽/мес**
- **Net profit при УСН 6%:** **760 800 ₽/мес**
- **Net profit при IT-льготе 3%:** **1 060 800 ₽/мес**
- **Net profit при ОСНО 20%:** **1 088 640 ₽/мес** до учёта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 36 129 958 ₽ | Быстрый enterprise ramp выводит модель в плюс уже в первый год |
| Base | M13 | 42 473 608 ₽ | Реалистичный путь требует ~42,5 млн ₽ до безубыточности |
| Pessimistic | M24 | 71 390 849 ₽ | При слабом pipeline капитал резко растёт и тезис становится тяжёлым |

### A7. Налоговая модель РФ
- **УСН 6%** операционно прост и подходит для раннего старта, но съедает большую часть прибыли на уровне 17-18 клиентов.
- **IT-льгота 3%** выглядит лучшим режимом, если есть аккредитация и профильная выручка.
- **ОСНО 20%** на бумаге допустим при уже положительном EBITDA, но в этом кейсе enterprise contracts и длинный procurement делают НДС неприятным для cash conversion.
- Для Hebbia-подобного expansion в РФ рационально считать базовым режимом **УСН/IT-льготу**, а не ОСНО.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 18 | 18 | M11 | сильный founder-led и partner-led execution |
| Base | 18 | 18 | M13 | реалистично, но требует дисциплины по ICP и velocity |
| Pessimistic | 18 | 18 | M24 | всё ещё достижимо, но уже слишком долго для узкого рынка |

<!-- P6A-DONE -->
## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 мес
База для sensitivity: M12 из SECTION A, active base ≈ **16,0 клиента**, ARPA **500k ₽/мес**, gross profit на клиента **367k ₽/мес**, EBITDA **-91k ₽/мес**.

| Сценарий | Что меняется | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | 16,04 клиента × 367k GP/client - 5,979m fixed | **-91 029** |
| Sens1 | CAC x2 | GTM spend и скорость закрытия хуже, фактически на M12 база падает к ~12 клиентам | **-1 575 200** |
| Sens2 | Churn x2 | churn 1,5% -> 3,0%, активная база M12 падает к ~14,7 клиента | **-585 100** |
| Sens3 | Price -30% | ARPA 500k -> 350k; при COGS 133k GP/client падает до 217k | **-2 498 520** |

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 700 000 | 836 000 | 1 500 000 | [T1], [T2] |
| Monthly churn, % | 1,0% | 1,5% | 4,0% | [T1], [T2] |
| ARPU, ₽/мес | 350 000 | 500 000 | 800 000 | [T1], [T2] |
| Conversion target-account -> paid, % | 2,0% | 4,5% | 8,0% | [T2] |
| Time-to-hire, мес | 0,75 | 1,5 | 3,0 | [T2] |

#### Как считалось
Вместо полноценной 1000-run симуляции использована упрощённая 9-point simulation: worst, median, best и 6 mixed-комбинаций между CAC, churn и ARPU. p10/p50/p90 ниже, это ручная интерполяция поверх P5-экономики и трёх PnL-сценариев.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 900 000** | **820 000** | **4 400 000** | **7 300 000** |
| CAC payback, мес | **4,3** | **1,7** | **1,0** | **3,3** |
| LTV/CAC | **5,8** | **29,3** | **52,0** | **46,2** |
| Cash runway, мес | **9,8** | **14,0** | **20,0** | **10,2** |

#### Интерпретация Monte Carlo Lite
- **Правило 1:** p10 EBITDA < 0, значит downside есть и он реальный.
- **Правило 2:** p50 EBITDA > 500k ₽/мес, значит median-case уже проходит фондовый EBITDA Gate.
- **Правило 3:** разброс высокий, но не катастрофический для enterprise-case; главный driver риска здесь не churn, а price realization и скорость первых 10 wins.
- **Правило 4:** модель не похожа на wide-SaaS, но для narrow enterprise wedge уже выглядит рабочей.

### B3. Competitor deep-dive

#### Топ-3 западных
| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Hebbia** | глубоко finance-native продукт, Matrix для сложных multi-step workflow, сильные integrations и enterprise security | pricing opaque, тяжёлый enterprise motion, не локализован под РФ-контур | **5-10%** узкой ниши AI research workspace для buy-side / IB / advisory | локальный secure deployment, русскоязычные документы, локальные источники и более узкий ICP |
| **AlphaSense** | мощная контентная база, цитируемый GenAI, сильный бренд в due diligence и market intelligence | меньше заточен под data-room execution и внутренние клиентские документы | **15-20%** broader market-intelligence / research platform | можно продавать не data subscription, а workflow execution внутри закрытого deal-room |
| **Datasite Diligence / iDeals VDR-class** | сильная security, audit trail, mature VDR workflows, привычны для M&A | это скорее VDR + workflow, а не AI analyst workspace уровня Hebbia | **20-30%** VDR / diligence room слоя | AI-first сравнение документов, memo drafting и вопрос-ответ поверх data room, а не просто room infrastructure |

#### Топ российских / локальных substitutes
| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **LegalScan** | официальный сайт [T6] | локальный AI review для договоров и комплаенса, рублёвый pricing anchor | legal-first, а не M&A / IB analyst workspace | **5-10%** локального AI document review | finance-specific workflows, DD memo, cross-doc reasoning по room |
| **Kept Risk RADAR / due diligence practice** | [T7], [T8] | доверие крупных клиентов, готовые due diligence процессы, экспертиза в high-stakes проверках | service-heavy и consulting-led, а не software scale | **10-15%** слоя managed due diligence / substitutes | software gross margin, постоянный workspace, ускорение analyst-hours вместо ручного проекта |
| **Большие банки / Big Law с внутренними VDR и аналитиками** | внутренняя замена, не единый vendor | уже встроены в сделки, высокое доверие, доступ к данным | ручной труд, низкая скорость, трудно масштабировать knowledge reuse | **40%+** фактического execution в РФ | automation + traceability + institutional memory в одном продукте |

#### Вывод по конкурентам
1. Конкурентное окно не пустое, но прямого локального аналога Hebbia для РФ я не вижу.
2. Главные substitutes в РФ сегодня не AI-native, а **VDR + консультанты + собственные аналитики**.
3. Значит moat в РФ можно строить не на “ещё одном ассистенте”, а на связке **secure deployment + русскоязычный financial/legal corpus + deal workflow instrumentation**.

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Слишком длинное внедрение security/on-prem | med | high | цикл пилота > 90 дней | стандартизировать secure package, заранее готовить DPA/SLA |
| Operational | Слабое качество ответов на русскоязычных DD-документах | med | high | champion вручную переписывает > 30% output | eval-set на RU docs, human-in-the-loop на первых аккаунтах |
| Operational | Слишком высокая нагрузка на founder-led presales | high | med | founder участвует в 100% сделок после M6 | build partner channel, готовить playbooks для AE/CS |
| Market | ICP оказывается уже ожидаемого | med | high | после 60 дней список target accounts < 40 | расширение в Big Law, corpdev и transaction services |
| Market | Клиенты готовы платить только 150-300k ₽/мес | high | high | скидки > 30% становятся нормой | продавать secure room + workflow + setup, а не просто seat license |
| Market | Слишком мало repeatable referrals | med | med | partner-sourced wins < 25% pipeline | formal partner program c advisory / integrators |
| Regulatory | Ограничения по хранению и передаче данных | med | high | клиенты требуют full on-prem / isolated contour | RU-hosted и on-prem вариант, data residency по умолчанию |
| Regulatory | Санкционные / vendor risks по model providers | high | med | provider terms меняются, latency растёт | multi-model routing, запасные провайдеры, локальный fallback |
| Financial | CAC растёт выше 1,2-1,5 млн ₽ | med | high | pilot-to-paid падает < 25% | жёстче qualification, меньше low-fit pilots |
| Financial | Нужный капитал растёт выше 50 млн ₽ до первых 10 клиентов | med | high | base plan сдвигается на 2+ квартала | staged hiring, delayed non-core hires, upfront setup fees |
| Black swan | Рынок M&A и DD резко проседает | med | high | падение сделки/бюджетов 2 квартала подряд | pivot в corpdev, compliance review, post-merger analytics |

### B5. Kill conditions через 6 месяцев
1. **Pricing fail:** если подтверждённый market price остаётся **< 400 000 ₽/мес** без сильного setup fee, expansion надо пересматривать.
2. **GTM fail:** если через 6 месяцев получено **< 3 платящих клиента** или partner-led pipeline не даёт хотя бы **10 qualified accounts**, кейс теряет repeatability.
3. **Execution fail:** если median внедрение длится **> 4 месяцев**, а pilot->paid conversion падает **< 30%**, модель слишком тяжёлая для узкого рынка.

### B6. Итог по SECTION B
SECTION B подтверждает, что Hebbia-подобный кейс в РФ **не широкий SaaS**, но уже не выглядит обречённым. В отличие от слабых geo-expand кейсов, здесь narrow enterprise wedge реально может пройти EBITDA gate при 18-20 клиентах и капитале порядка **36-42 млн ₽** в нормальном execution.

Практический вывод: **кейс держится только как secure enterprise deal-workspace для very high-value buyers.** Если принять этот framing и не пытаться идти в mass market, economics остаётся фондово интересной.

## Источники SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1528-msk-hebbia-geo-expand-v2/04-economics.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1528-msk-hebbia-geo-expand-v2/02-demand.md
- [T3] Hebbia product: https://www.hebbia.com/product
- [T4] Hebbia company / traction: https://www.hebbia.com/about
- [T5] AlphaSense due diligence platform: https://www.alpha-sense.com/solutions/due-diligence-platform
- [T6] LegalScan: https://www.legalscan.ai/
- [T7] Datasite Diligence: https://www.datasite.com/en/products/diligence
- [T8] Kept Risk RADAR: https://kept.ru/services/tekhnologii/risk-radar-kept/

<!-- P6B-DONE -->
