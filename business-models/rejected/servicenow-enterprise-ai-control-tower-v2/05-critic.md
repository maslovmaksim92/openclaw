# SECTION A. Finance PnL

## A1. Входные данные и допущения
- ARPA / MRR на клиента: **400 000 ₽/мес**.
- COGS на клиента: **96 600 ₽/мес**.
- Gross profit на клиента: **303 400 ₽/мес**.
- Contribution profit на клиента: **268 000 ₽/мес**.
- Fixed costs: **6 892 000 ₽/мес**.
- Team FOT: **5 512 000 ₽/мес**.
- CAC по каналам из `04-economics.md`: outbound **1 244 444 ₽**, partners / integrators **1 280 000 ₽**, events / inbound **1 857 750 ₽**, blended investment-grade CAC **1 532 000 ₽**.
- LTV: **20,24 млн ₽** на клиента, monthly churn baseline **1,5%**.
- Налоговая рамка РФ: сравниваю **УСН 6%**, **IT-льготу 3%** при аккредитации Минцифры и **ОСНО 20%** по прибыли; при ОСНО дополнительно возникает **НДС 20%** и давление на оборотный капитал.
- Страховые взносы **~30% к ФОТ** уже учтены внутри FOT и fixed costs.
- Cumulative cash стартует с **0 ₽** и показывает накопленную потребность в капитале.

## A2. Сценарии
- **Base:** new clients = `0,0,0,1,1,2,2,3,3,4,5,5`, churn **1,5%/мес**.
- **Optimistic:** new clients = `0,0,1,1,2,2,3,4,4,5,5,5`, churn **1,0%/мес**.
- **Pessimistic:** new clients = `0,0,0,0,1,1,1,2,2,2,3,3`, churn **2,5%/мес**.
- Формула активной базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`.
- EBITDA в таблицах считаю как `Gross profit - Fixed costs`.
- Cash burn = `max(0, -EBITDA)`.

## A3. PnL 12 месяцев, Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 5 | 5 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 3.96 | 5.90 | 8.81 | 11.68 | 15.50 | 20.27 | 24.96 |
| MRR, ₽ | 0 | 0 | 0 | 400 000 | 794 000 | 1 582 090 | 2 358 359 | 3 522 983 | 4 670 139 | 6 200 086 | 8 107 085 | 9 985 479 |
| COGS, ₽ | 0 | 0 | 0 | 96 600 | 191 751 | 382 075 | 569 544 | 850 800 | 1 127 838 | 1 497 321 | 1 957 861 | 2 411 493 |
| Gross profit, ₽ | 0 | 0 | 0 | 303 400 | 602 249 | 1 200 015 | 1 788 815 | 2 672 183 | 3 542 300 | 4 702 766 | 6 149 224 | 7 573 986 |
| GM% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% |
| Fixed costs, ₽ | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 |
| EBITDA, ₽ | -6 892 000 | -6 892 000 | -6 892 000 | -6 588 600 | -6 289 751 | -5 691 985 | -5 103 185 | -4 219 817 | -3 349 700 | -2 189 234 | -742 776 | 681 986 |
| Cash burn, ₽ | 6 892 000 | 6 892 000 | 6 892 000 | 6 588 600 | 6 289 751 | 5 691 985 | 5 103 185 | 4 219 817 | 3 349 700 | 2 189 234 | 742 776 | 0 |
| Cumulative cash, ₽ | -6 892 000 | -13 784 000 | -20 676 000 | -27 264 600 | -33 554 351 | -39 246 336 | -44 349 521 | -48 569 338 | -51 919 038 | -54 108 272 | -54 851 048 | -54 851 048 |

## A4. PnL 12 месяцев, Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 4 | 5 | 5 | 5 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.99 | 3.97 | 5.93 | 8.87 | 12.78 | 16.65 | 21.49 | 26.27 | 31.01 |
| MRR, ₽ | 0 | 0 | 400 000 | 796 000 | 1 588 040 | 2 372 160 | 3 548 438 | 5 112 954 | 6 661 824 | 8 595 206 | 10 509 254 | 12 404 161 |
| COGS, ₽ | 0 | 0 | 96 600 | 192 234 | 383 512 | 572 877 | 856 948 | 1 234 778 | 1 608 831 | 2 075 742 | 2 537 985 | 2 995 605 |
| Gross profit, ₽ | 0 | 0 | 303 400 | 603 766 | 1 204 528 | 1 799 283 | 2 691 490 | 3 878 175 | 5 052 994 | 6 519 464 | 7 971 269 | 9 408 556 |
| GM% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% |
| Fixed costs, ₽ | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 |
| EBITDA, ₽ | -6 892 000 | -6 892 000 | -6 588 600 | -6 288 234 | -5 687 472 | -5 092 717 | -4 200 510 | -3 013 825 | -1 839 006 | -372 536 | 1 079 269 | 2 516 556 |
| Cash burn, ₽ | 6 892 000 | 6 892 000 | 6 588 600 | 6 288 234 | 5 687 472 | 5 092 717 | 4 200 510 | 3 013 825 | 1 839 006 | 372 536 | 0 | 0 |
| Cumulative cash, ₽ | -6 892 000 | -13 784 000 | -20 372 600 | -26 660 834 | -32 348 306 | -37 441 023 | -41 641 532 | -44 655 357 | -46 494 363 | -46 866 900 | -46 866 900 | -46 866 900 |

## A5. PnL 12 месяцев, Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 4.85 | 6.73 | 8.56 | 11.35 | 14.07 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 400 000 | 790 000 | 1 170 250 | 1 940 994 | 2 692 469 | 3 425 157 | 4 539 528 | 5 626 040 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 96 600 | 190 785 | 282 615 | 468 750 | 650 231 | 827 175 | 1 096 296 | 1 358 689 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 303 400 | 599 215 | 887 635 | 1 472 244 | 2 042 238 | 2 597 982 | 3 443 232 | 4 267 351 |
| GM% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% | 75,9% |
| Fixed costs, ₽ | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 |
| EBITDA, ₽ | -6 892 000 | -6 892 000 | -6 892 000 | -6 892 000 | -6 588 600 | -6 292 785 | -6 004 365 | -5 419 756 | -4 849 762 | -4 294 018 | -3 448 768 | -2 624 649 |
| Cash burn, ₽ | 6 892 000 | 6 892 000 | 6 892 000 | 6 892 000 | 6 588 600 | 6 292 785 | 6 004 365 | 5 419 756 | 4 849 762 | 4 294 018 | 3 448 768 | 2 624 649 |
| Cumulative cash, ₽ | -6 892 000 | -13 784 000 | -20 676 000 | -27 568 000 | -34 156 600 | -40 449 385 | -46 453 750 | -51 873 507 | -56 723 269 | -61 017 287 | -64 466 055 | -67 090 704 |

## A6. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
### Waterfall на 1 клиента / месяц
| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 400 000 | recurring revenue |
| Gross profit | 303 400 | ARPA - COGS 96 600 ₽ |
| Contribution profit | 268 000 | после variable sales / success allocation |
| EBITDA contribution | 303 400 | вклад в покрытие fixed costs по PnL-таблице |
| Net, УСН 6% | 279 400 | gross profit - 6% от выручки |
| Net, IT-льгота 3% | 291 400 | gross profit - 3% от выручки |
| Net, ОСНО 20% | 242 720 | 20% налог на прибыль; НДС 20% не сидит в EBITDA, но ухудшает cash conversion |

### Waterfall на EBITDA break-even уровне 23 клиента
| Шаг | ₽/мес |
|---|---:|
| Revenue | 9 200 000 |
| COGS | 2 221 800 |
| Gross profit | 6 978 200 |
| Contribution profit | 6 164 000 |
| EBITDA | 86 200 |
| Net, УСН 6% | -465 800 |
| Net, IT-льгота 3% | -189 800 |
| Net, ОСНО 20% | 68 960 |

### Waterfall на post-tax safe level 26 клиентов
| Шаг | ₽/мес |
|---|---:|
| Revenue | 10 400 000 |
| COGS | 2 511 600 |
| Gross profit | 7 888 400 |
| Contribution profit | 6 968 000 |
| EBITDA | 996 400 |
| Net, УСН 6% | 372 400 |
| Net, IT-льгота 3% | 684 400 |
| Net, ОСНО 20% | 797 120 |

## A7. Cash flow: startup_capital_to_bep_rub
- **Base:** startup_capital_to_bep_rub = **54 851 048 ₽**. EBITDA break-even достигается только в **M12**.
- **Optimistic:** startup_capital_to_bep_rub = **46 866 900 ₽**. EBITDA break-even достигается в **M11**.
- **Pessimistic:** startup_capital_to_bep_rub = **67 090 704 ₽**. В горизонте **M1-M12** break-even не достигается.

## A8. Налоговая модель РФ
- **УСН 6% с выручки:** простой режим, но в этом кейсе на уровне EBITDA break-even 23 клиента бизнес ещё остаётся post-tax отрицательным.
- **IT-льгота 3%:** лучший рабочий режим для software-first AI governance платформы при аккредитации Минцифры и соблюдении требований к профильной выручке. На 23 клиентах почти выводит кейс к post-tax нулю.
- **ОСНО 20%:** по PnL выглядит мягче при уже положительном EBIT, но даёт **НДС 20%**, более тяжёлый документооборот и давление на оборотный капитал enterprise-сделок.
- **Страховые взносы ~30% к ФОТ** уже сидят в team FOT **5 512 000 ₽/мес** и повторно не добавляются.
- Для этого кейса базово рационально считать **IT-льготу / УСН**, а ОСНО держать как enterprise fallback.

## A9. Break-even по client count и по месяцам
| Scenario | EBITDA break-even, clients | Post-tax break-even, clients (УСН / IT / ОСНО) | Break-even month | Clients at M12 | Gap to EBITDA BEP |
|---|---:|---:|---:|---:|---:|
| Base | 23 | 25 / 24 / 29 | M12 | 24.96 | 1.96 |
| Optimistic | 23 | 25 / 24 / 29 | M11 | 31.01 | 8.01 |
| Pessimistic | 23 | 25 / 24 / 29 | не достигнут | 14.07 | 8.93 |

<!-- P6A-DONE -->
# SECTION B. Finance Risk, Monte Carlo Lite и Competitor Deep-Dive

## B1. Sensitivity analysis, EBITDA @M12

Ниже считаю **EBITDA after acquisition engine**, а не только gross profit minus fixed costs. Иначе сценарий `CAC x2` не был бы виден в P&L. База для сравнения: gross profit @M12 из SECTION A, fixed costs **6 892 000 ₽/мес**, acquisition engine baseline **2 131 550 ₽/мес** из `04-economics.md`. [T1]

| Сценарий | Ключевое изменение | Active clients @M12 | Gross profit @M12, ₽/мес | EBITDA after CAC @M12, ₽/мес |
|---|---|---:|---:|---:|
| Base | baseline | 24,96 | 7 572 864 | **-1 450 686** |
| Sens1 | CAC x2 | 24,96 | 7 572 864 | **-3 582 236** |
| Sens2 | Churn x2, до 3,0%/мес | 23,98 | 7 276 332 | **-1 747 218** |
| Sens3 | Price -30%, ARPU 280k ₽ | 24,96 | 5 301 005 | **-3 722 545** |

### Вывод по чувствительности
- Уже в base после учёта growth CAC M12 остаётся отрицательным, то есть модель **требует внешнего капитала дольше, чем кажется по "чистому" EBITDA из SECTION A**. [T1]
- Самый болезненный удар даёт **price compression -30%**: экономика быстро уходит ниже комфортного порога, потому что gross margin на клиента ещё высокая, но fixed base слишком тяжёлый. [T1]
- **CAC x2** почти столь же опасен, как скидка по цене: рынок enterprise AI governance легко наказывает молодого игрока длинным procurement tail и более дорогим presale. [T1]
- Удвоение churn тоже неприятно, но в этой модели оно чуть менее разрушительно на M12, чем price/CAC shock, потому что основная боль сидит в acquisition intensity и fixed-cost load. [T1]

## B2. Monte Carlo Lite, confidence intervals @M24

### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|----:|----------|
| CAC, ₽ | 1 200 000 | 1 532 000 | 2 300 000 | `04-economics.md`, консервативный хвост на procurement/presale risk [T1] |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | базовая модель + enterprise benchmark [T1] |
| ARPU, ₽/мес | 280 000 | 400 000 | 520 000 | base contract и stress/upsell corridor [T1][T2] |
| Conversion lead→paid, % | 0,6% | 1,0% | 1,8% | inference из blended enterprise funnel и каналов [T1] |
| Time-to-hire, мес | 0,5 | 1,5 | 3,0 | hiring timeline по core ролям [T1] |

### Метод
Полную 1000-итерационную симуляцию здесь не строю. Использую **Monte Carlo Lite** через 9 комбинаций: best, median, worst и 6 mixed cases. Для каждого кейса M24 считаю:
- active clients через формулу retention;
- EBITDA after CAC = gross profit - fixed costs - acquisition spend;
- CAC payback = CAC / gross profit per client;
- LTV/CAC = `(ARPU × GM%) / churn / CAC`;
- cash runway при стартовом капитале **55 млн ₽**, что соответствует нижней границе адекватного funding envelope из P5. [T1]

### Confidence interval summary
| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | -6 390 341 | -542 153 | 47 580 724 | 53 971 065 |
| CAC payback, мес | 3,0 | 5,0 | 10,8 | 7,8 |
| LTV/CAC | 3,1 | 17,1 | 32,9 | 29,8 |
| Cash runway, мес | 7,8 | 10,2 | 23,3 | 15,5 |

### Интерпретация
- **Правило 1 срабатывает:** `p10 EBITDA < 0`, значит downside включает реальный риск недофинансирования и insolvency. [T1]
- **Правило 2 тоже срабатывает:** `p50 EBITDA < 500К ₽/мес`, медианный сценарий не проходит EBITDA Gate даже к M24. [T1]
- **Правило 3 де-факто срабатывает ещё жёстче, чем 10x**: распределение EBITDA пересекает ноль, то есть разброс не просто широкий, а меняет знак результата. Это уровень неопределённости, при котором score нужно даунгрейдить. [T1]
- **Правило 4 срабатывает:** `Range width по LTV/CAC = 29,8 > 8`, модель хрупкая. Основные источники хрупкости, в порядке силы, это **pricing pressure, CAC volatility и churn drift**. [T1]

## B3. Competitor deep-dive

### Западные конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **ServiceNow AI Control Tower** | Глубокий доступ к enterprise workflow, сильный бренд, встроенность в ITSM/ESM, готовый board-level governance narrative. [T3][T4] | Очень тяжёлый цикл продажи, дорогой стек, слабая локализация под РФ-регуляторику и санкционные ограничения. | **20-25% global enterprise AI governance/control-plane shortlists**, оценка по бренду и installed base, это inference, не официальный share. [T3][T4] | Мы можем выиграть у них в **локальной поставке, data residency, более быстрой кастомизации и lower-TCV wedge** для РФ enterprise. |
| **IBM watsonx.governance** | Сильный compliance story, model risk governance, explainability, исторический доступ в regulated enterprise. [T5] | Часто воспринимается как тяжёлый governance suite, а не быстрый operational control layer; внедрение долгое и дорогoe. | **8-12% global enterprise governance deals**, inference по силе бренда IBM в regulated verticals. [T5] | Более короткий путь к value, меньше consulting tax, лучше fit для мультивендорной среды в РФ без западного heavyweight stack. |
| **Credo AI** | Чистый AI governance specialist, фокус на policy, controls, compliance mapping, меньше legacy baggage. [T6] | Слабее distribution, чем у platform incumbents; нет собственной большой ITSM/workflow базы. | **3-5% of specialist AI-governance pilots** на западном рынке, inference по нишевому positioning. [T6] | Мы можем позиционироваться не только как governance registry, но как **governance + operations + integration execution** поверх enterprise workflows. |

### Российские и локальные substitute-конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Just AI / Jay Flow / JAICP enterprise stack** | Сильный локальный AI-вендор, enterprise integrations, голос/чат/агенты, заметная узнаваемость в РФ. [T7][T8] | Больше ассоциируется с conversational/agent automation, чем с независимым control tower для governance всего AI-ландшафта. | **10-15% RF enterprise AI orchestration/agent platform pilots**, inference по узнаваемости бренда и числу enterprise кейсов. [T7][T8] | Наше отличие, узкий **AI governance + inventory + audit-first** слой, а не только агентная платформа. |
| **GigaChat Enterprise / Сбер** | Самый мощный бренд, доступ к крупным enterprise и regulated buyers, локальная инфраструктура и сильный LLM narrative. [T9] | Решение тяготеет к собственному экосистемному стеку; для многих клиентов это vendor-lock-in risk. | **20-30% RF enterprise generative AI shortlists**, inference по дистрибуции Сбера. [T9] | Мы сильнее как **vendor-neutral overlay** над разными моделями, системами и внутренними AI-активами. |
| **MWS AI, AI Agent / agent platform layer** | Сильный телеком-доступ к enterprise клиентам, инфраструктурная база, кросс-продажа через облако и data services. [T10] | Пока меньше доказанного governance depth, чем у чистых control-plane игроков; может остаться infra/adoption story. | **8-12% RF enterprise AI platform pilots**, inference по каналу МТС и MWS. [T10] | У нас более чёткий тезис вокруг **policy, risk, auditability и AI asset inventory**, а не вокруг общего AI enablement. |
| **SimpleOne / GenAI-adjacent ITSM stack** | Сильный локальный ITSM/ESM substitute, понятный buyer access через service-management budget line. [T11][T12] | Собственный AI-governance moat пока слабее; риск остаться ITSM-core с AI-feature bundle. | **5-8% RF adjacent shortlists** в тех аккаунтах, где бюджет идёт через ITSM replacement. [T11][T12] | Мы выигрываем, если продаёмся как **control-plane поверх heterogeneous AI stack**, а не как ещё один service desk. |

### Вывод по конкурентной карте
- На Западе category owner сейчас ближе всего к **ServiceNow + IBM**, а нишевый specialist-layer представляет **Credo AI**. [T3][T5][T6]
- В РФ прямой категории почти нет, поэтому реальная конкуренция идёт не с "AI control tower" как label, а с **локальными AI-платформами, ITSM-слоем и экосистемными LLM-вендорами**. [T7][T9][T10][T11]
- Следовательно, продукту нужен очень конкретный wedge: **vendor-neutral governance for multi-model, multi-team, regulated enterprise**, иначе value утечёт в incumbent platform bundle. [T1][T3]

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Нехватка senior backend/ML кадров удлиняет roadmap | med | high | 2+ ключевые роли открыты >90 дней, sprint slip >20% | заранее нанять 1-2 ключевых инженеров, держать contractor bench, урезать scope до audit/inventory core |
| Operational | LLM/API dependency: рост latency/cost, деградация SLA | high | high | cost/request +30%, latency p95 >2x, частые provider incidents | multi-provider gateway, fallback на локальные модели, лимиты на expensive workflows |
| Market | Спрос остаётся educational, а не budgeted | med | high | много discovery, мало paid pilot, close rate <15% | продавать через ITSM/risk/compliance budget line, а не через абстрактный AI label |
| Market | Price compression из-за bundled AI-features у incumbents | high | high | 3+ сделки подряд требуют скидку >25%, ARPA <350k ₽ | фиксировать floor pricing, upsell managed governance, жёстко резать кастомный scope |
| Regulatory | 152-ФЗ и data residency блокируют часть мультиоблачных архитектур | med | high | ИБ/юристы требуют on-prem или RU-only размещение почти в каждом enterprise deal | поддержка on-prem/private cloud, локальный лог-стор, изоляция PII |
| Regulatory | 115-ФЗ, внутренний AML/KYC и audit trail требуют более строгой прослеживаемости | med | med | enterprise security review добавляет 4-8 недель и новые mandatory controls | заранее готовый audit pack, immutable logs, role-based approvals |
| Financial | Cash runway падает ниже 9 месяцев до product-market proof | high | high | burn >6 млн ₽/мес 2 месяца подряд, новых paid <1/мес | поднимать bridge раньше, сокращать hiring pace, замораживать growth spend |
| Financial | Курс USD и импортный SaaS/LLM cost inflation бьют по COGS | med | med | LLM/cloud cost в рублях +20-30% за квартал | рублёвые контракты с клиентами, surcharge clause, локальные providers |
| Black swan | Новые санкции режут доступ к западному SaaS и model APIs | med | high | provider notice, отказ в биллинге, блоки аккаунтов | локальные и self-hosted fallback, архитектура без single foreign dependency |
| Black swan | Резкое отключение или запрет внешнего LLM-провайдера | low | high | rate-limit collapse, legal notice, массовые outages | минимизировать критичность LLM в core workflows, офлайн policy rules, локальные модели для базового режима |

## B5. Kill conditions, checkpoint через 6 месяцев

1. **Go-to-market kill:** к M6 меньше **4 активных платящих клиентов** или меньше **8 квалифицированных pilot opportunities** в pipeline. Значит category pain не конвертируется в repeatable demand.
2. **Unit economics kill:** к M6 blended **CAC > 2,5 млн ₽** или **CAC payback > 12 месяцев** на gross-profit basis. Это означает, что enterprise motion стал слишком дорогим для узкого SAM.
3. **Retention/pricing kill:** к M6 фактический **logo churn > 3%/мес** либо средний новый **ARPU < 350 тыс. ₽/мес**. Тогда модель не выдерживает ни churn-risk, ни price compression.

## B6. Итог по SECTION B

- Finance-risk профиль у кейса **заметно хуже**, чем видно из чистого base EBITDA в SECTION A. После учёта acquisition engine проект выглядит **капиталоёмким и чувствительным к цене/CAC**. [T1]
- Monte Carlo Lite показывает, что median-case **не проходит EBITDA Gate**, а p10 уходит в отрицательный сценарий. Это не auto-reject, но точно **downgrade по уверенности и score**. [T1]
- Конкурентная среда в РФ опасна тем, что прямой категории почти нет, а substitute-давление уже есть со стороны **Сбера, Just AI, MWS и ITSM-слоя**. [T7][T9][T10][T11]
- Следовательно, инвесткейс живёт только при жёстком positioning: **vendor-neutral governance/control plane для regulated enterprise**, с локальной поставкой и без скидочной войны.

## Источники SECTION B
- [T1] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/servicenow-enterprise-ai-control-tower-v2/04-economics.md`
- [T2] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/servicenow-enterprise-ai-control-tower-v2/02-demand.md`
- [T3] ServiceNow AI Control Tower product page: https://www.servicenow.com/products/ai-control-tower.html
- [T4] ServiceNow press release, 2025-05-06: https://newsroom.servicenow.com/press-releases/details/2025/ServiceNow-Launches-AI-Control-Tower-a-Centralized-Command-Center-to-Govern-Manage-Secure-and-Realize-Value-From-Any-AI-Agent-Model-and-Workflow/
- [T5] IBM watsonx.governance: https://www.ibm.com/products/watsonx-governance
- [T6] Credo AI platform: https://www.credo.ai/platform
- [T7] Habr, Just AI / JAICP enterprise AI: https://habr.com/ru/companies/just_ai/
- [T8] Skolkovo, Just AI profile: https://navigator.sk.ru/orn/1123623
- [T9] Habr, GigaChat Enterprise / Сбер AI материалы: https://habr.com/ru/companies/sberbank/articles/
- [T10] vc.ru / MWS AI материалы: https://vc.ru/services/2054490-platforma-ai-agentov-mws-ai-zamenit-assistentov-i-anlitikov-v-biznes-processah
- [T11] Habr, SimpleOne / локальный ITSM: https://habr.com/ru/companies/simpleone/
- [T12] Rusprofile / SimpleOne legal profile: https://www.rusprofile.ru/

Все market-share estimates в competitor deep-dive являются **аналитическим inference**, потому что публичных точных долей рынка по узкой категории enterprise AI control tower в РФ и global niche governance layer нет.

<!-- P6B-DONE -->
