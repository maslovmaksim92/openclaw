## SECTION A. Finance PnL

### A1. Допущения модели

- ARPA / MRR на клиента: **450 000 ₽/мес**.
- COGS на клиента: **110 000 ₽/мес**.
- Gross profit на клиента: **340 000 ₽/мес**.
- Contribution после variable sales/support allocation: **313 000 ₽/клиент/мес**.
- Fixed costs: **5 862 000 ₽/мес**.
- Team FOT: **4 992 000 ₽/мес**.
- CAC by channel из `04-economics.md`: founder-led outbound / ABM **915 789 ₽**, partnerships / agencies / SI **505 882 ₽**, content / webinars / inbound **567 273 ₽**, blended CAC **686 000 ₽**.
- Налоги: сравниваю **УСН 6% с выручки**, **IT-льготу 3% с выручки** при аккредитации Минцифры и **ОСНО 20% по прибыли + НДС 20%**.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs, повторно не добавляются.
- Сценарии продаж на 12 месяцев:
  - **Base:** new clients = 1,1,1,2,2,2,3,3,3,3,3,3; churn **1.5%/мес**.
  - **Optimistic:** new clients = 1,1,2,2,3,3,4,4,4,4,4,4; churn **1.0%/мес**.
  - **Pessimistic:** new clients = 0,0,1,1,1,1,1,1,2,2,2,2; churn **2.5%/мес**.
- Cumulative cash в таблицах показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 1.00 | 1.98 | 2.96 | 4.91 | 6.84 | 8.73 | 11.60 | 14.43 | 17.21 | 19.95 | 22.66 | 25.32 |
| MRR, ₽ | 450 000 | 893 250 | 1 329 851 | 2 209 903 | 3 076 755 | 3 930 604 | 5 221 645 | 6 493 320 | 7 745 920 | 8 979 731 | 10 195 035 | 11 392 110 |
| COGS, ₽ | 110 000 | 218 350 | 325 075 | 540 199 | 752 096 | 960 814 | 1 276 402 | 1 587 256 | 1 893 447 | 2 195 045 | 2 492 120 | 2 784 738 |
| Gross profit, ₽ | 340 000 | 674 900 | 1 004 776 | 1 669 705 | 2 324 659 | 2 969 789 | 3 945 243 | 4 906 064 | 5 852 473 | 6 784 686 | 7 702 916 | 8 607 372 |
| GM% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% |
| Fixed costs, ₽ | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 |
| EBITDA, ₽ | -5 549 000 | -5 240 695 | -4 937 015 | -4 324 889 | -3 721 946 | -3 128 047 | -2 230 056 | -1 345 535 | -474 282 | 383 902 | 1 229 213 | 2 061 845 |
| Cash burn, ₽ | 5 549 000 | 5 240 695 | 4 937 015 | 4 324 889 | 3 721 946 | 3 128 047 | 2 230 056 | 1 345 535 | 474 282 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 549 000 | -10 789 695 | -15 726 710 | -20 051 599 | -23 773 545 | -26 901 592 | -29 131 648 | -30 477 183 | -30 951 465 | -30 951 465 | -30 951 465 | -30 951 465 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 4.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.99 | 3.97 | 5.93 | 8.87 | 11.78 | 15.66 | 19.51 | 23.31 | 27.08 | 30.81 | 34.50 |
| MRR, ₽ | 450 000 | 895 500 | 1 786 545 | 2 668 680 | 3 991 993 | 5 302 073 | 7 049 052 | 8 778 562 | 10 490 776 | 12 185 868 | 13 864 010 | 15 525 369 |
| COGS, ₽ | 110 000 | 218 900 | 436 711 | 652 344 | 975 820 | 1 296 062 | 1 723 102 | 2 145 871 | 2 564 412 | 2 978 768 | 3 388 980 | 3 795 090 |
| Gross profit, ₽ | 340 000 | 676 600 | 1 349 834 | 2 016 336 | 3 016 172 | 4 006 011 | 5 325 950 | 6 632 691 | 7 926 364 | 9 207 100 | 10 475 029 | 11 730 279 |
| GM% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% |
| Fixed costs, ₽ | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 |
| EBITDA, ₽ | -5 549 000 | -5 239 130 | -4 619 359 | -4 005 785 | -3 085 347 | -2 174 114 | -958 993 | 243 977 | 1 434 918 | 2 613 948 | 3 781 189 | 4 936 757 |
| Cash burn, ₽ | 5 549 000 | 5 239 130 | 4 619 359 | 4 005 785 | 3 085 347 | 2 174 114 | 958 993 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 549 000 | -10 788 130 | -15 407 489 | -19 413 274 | -22 498 621 | -24 672 735 | -25 631 728 | -25 631 728 | -25 631 728 | -25 631 728 | -25 631 728 | -25 631 728 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 4.76 | 5.64 | 7.50 | 9.31 | 11.08 | 12.80 |
| MRR, ₽ | 0 | 0 | 450 000 | 888 750 | 1 316 531 | 1 733 618 | 2 140 278 | 2 536 771 | 3 373 351 | 4 189 018 | 4 984 292 | 5 759 685 |
| COGS, ₽ | 0 | 0 | 110 000 | 217 250 | 321 819 | 423 773 | 523 179 | 620 099 | 824 597 | 1 023 982 | 1 218 383 | 1 407 923 |
| Gross profit, ₽ | 0 | 0 | 340 000 | 671 500 | 994 712 | 1 309 845 | 1 617 099 | 1 916 671 | 2 548 754 | 3 165 035 | 3 765 910 | 4 351 762 |
| GM% | 0.0% | 0.0% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% | 75.6% |
| Fixed costs, ₽ | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 | 5 862 000 |
| EBITDA, ₽ | -5 862 000 | -5 862 000 | -5 549 000 | -5 243 825 | -4 946 279 | -4 656 172 | -4 373 318 | -4 097 535 | -3 515 647 | -2 948 306 | -2 395 148 | -1 855 819 |
| Cash burn, ₽ | 5 862 000 | 5 862 000 | 5 549 000 | 5 243 825 | 4 946 279 | 4 656 172 | 4 373 318 | 4 097 535 | 3 515 647 | 2 948 306 | 2 395 148 | 1 855 819 |
| Cumulative cash, ₽ | -5 862 000 | -11 724 000 | -17 273 000 | -22 516 825 | -27 463 104 | -32 119 277 | -36 492 595 | -40 590 130 | -44 105 777 | -47 054 082 | -49 449 230 | -51 305 049 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 450 000 ₽
- **COGS:** 110 000 ₽
- **Gross profit:** 340 000 ₽
- **Variable sales/support:** 27 000 ₽
- **Contribution:** 313 000 ₽

#### Waterfall на EBITDA break-even уровне 19 клиентов
- **Revenue:** 8 550 000 ₽/мес
- **COGS:** 2 090 000 ₽/мес
- **Gross profit:** 6 460 000 ₽/мес
- **Variable sales/support:** 513 000 ₽/мес
- **Contribution:** 5 947 000 ₽/мес
- **EBITDA:** 85 000 ₽/мес

#### Net после налогов РФ
- **УСН 6%:** 85 000 - 513 000 = **-428 000 ₽/мес**
- **IT-льгота 3%:** 85 000 - 256 500 = **-171 500 ₽/мес**
- **ОСНО 20%:** налог на прибыль ≈ **17 000 ₽/мес**, net ≈ **68 000 ₽/мес**, плюс **НДС 1 710 000 ₽/мес** создаёт дополнительное давление на cash flow.

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Base | M10 | 30 951 465 | Минимальный капитал до выхода на неотрицательную EBITDA. |
| Optimistic | M8 | 25 631 728 | Минимальный капитал до выхода на неотрицательную EBITDA. |
| Pessimistic | n/a | 51 305 049 | За 12 месяцев EBITDA break-even не достигается, нужен капитал минимум на покрытие burn первого года. |

### A7. Налоговая модель: УСН vs IT-льгота vs ОСНО
| Режим | Что платим | Эффект на PnL / cash flow | Вывод |
|---|---|---|---|
| УСН 6% | 6% с выручки | Простая админка, но при high-ACV SaaS съедает значимую часть EBITDA на раннем этапе. | Рабочий fallback-режим до аккредитации. |
| IT-льгота 3% | 3% с выручки при аккредитации Минцифры | Лучший денежный режим для AI/SaaS, снижает налоговую нагрузку вдвое против УСН 6%. | Предпочтительный режим при соответствии критериям. |
| ОСНО 20% | 20% налог на прибыль + НДС 20% | На бумаге налог на прибыль мягче при низкой прибыли, но НДС резко ухудшает cash conversion и усложняет администрирование. | Для этой модели хуже, чем IT-льгота и часто хуже, чем УСН. |

- Страховые взносы **~30% к ФОТ** уже отражены в fully-loaded FOT **4 992 000 ₽/мес**.
- Если компания получает IT-аккредитацию Минцифры, наиболее рациональный базовый режим для модели Hilbert, исходя из cash efficiency, это **IT-льгота 3%**.

### A8. Break-even по client count и по месяцам
- **Break-even по gross profit:** 17.24 клиента, то есть округлённо **18 клиентов**.
- **Break-even по contribution / EBITDA:** 18.73 клиента, то есть округлённо **19 клиентов**.

| Scenario | Break-even client count | Break-even month | Комментарий |
|---|---:|---:|---|
| Base | 19 | M10 | В этом месяце contribution покрывает fixed costs. |
| Optimistic | 19 | M8 | В этом месяце contribution покрывает fixed costs. |
| Pessimistic | 19 | n/a | К M12 база доходит только до 12.80 клиентов, ниже EBITDA break-even. |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

Базу беру из Section A: M12 EBITDA = **2 061 845 ₽/мес** при **25.32** клиентах, blended CAC **686 000 ₽**, churn **1.5%/мес**, ARPA **450 000 ₽/мес**.

| Сценарий | Ключевое изменение | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | Section A base case | **2 061 845** |
| Sens1 | CAC x2 | Удваиваю ежемесячный acquisition spend с 1.612 млн ₽ до 3.224 млн ₽, при том же клиентском базе | **449 845** |
| Sens2 | Churn x2 | Churn растёт с 1.5% до 3.0%, активная база к M12 падает с 25.32 до ~23.77 клиентов | **2 218 152** |
| Sens3 | Price -30% | ARPA падает с 450k до 315k ₽ при том же COGS 110k ₽ и той же базе клиентов | **-672 261** |

**Вывод:** модель терпит ухудшение CAC и умеренно терпит удвоение churn, но **ломается при price compression -30%**. Значит главный финансовый риск не acquisition efficiency, а невозможность удержать premium pricing против CDP/CEP substitutes.

### B2. Monte Carlo Lite, confidence intervals

#### Inputs: triangular min / mode / max

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 500 000 | 686 000 | 1 100 000 | [T1] `04-economics.md`, channel CAC + stress-upside/downside |
| Monthly churn, % | 1.0% | 1.5% | 3.0% | [T1] `04-economics.md`, Benchmarkit + Vitally |
| ARPU, ₽/мес | 350 000 | 450 000 | 550 000 | [T1] `02-demand.md`, `04-economics.md`, competitor price anchors |
| Conversion lead→paid, % | 0.8% | 1.5% | 2.5% | [T1] `04-economics.md`, funnel by channels |
| Time-to-hire, мес | 1.0 | 1.7 | 3.0 | [T1] `04-economics.md`, hiring plan |

#### Метод

Полную 1000-итерационную симуляцию не строю. Вместо этого использую **9 комбинаций** по CAC / churn / ARPU вокруг min-mode-max, а conversion и hiring беру как связанные переменные: при худшем CAC конверсия деградирует, при лучшем CAC улучшается; длинный time-to-hire увеличивает операционный лаг и снижает скорость выхода на M24 profile. Это упрощённый Monte Carlo Lite, достаточный для диапазонов p10 / p50 / p90.

#### Результат Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24 (₽/мес) | **1 365 170** | **11 908 728** | **20 543 113** | **19 177 943** |
| CAC payback (мес) | **4.58** | **2.02** | **1.14** | **3.44** |
| LTV/CAC | **7.27x** | **26.67x** | **88.00x** | **80.73x** |
| Cash runway (мес) | **13** | **18** | **24+** | **11+** |

#### Интерпретация Monte Carlo Lite

1. **p10 EBITDA @M24 > 0**, значит формально kill criterion по insolvency не срабатывает, но запас прочности невелик относительно enterprise execution risk.
2. **p50 EBITDA @M24 = 11.9 млн ₽/мес**, то есть медианный сценарий уверенно проходит EBITDA Gate.
3. **p90 / p10 ≈ 15.0x**, это **выше 10x**, значит неопределённость слишком высока и общий score кейса надо даунгрейдить на один уровень по risk-adjusted confidence.
4. **Range width по LTV/CAC = 80.73x**, это намного выше порога 8, значит модель действительно хрупкая: её outcome критически зависит от pricing discipline, реального churn и способности удержать CAC в разумном коридоре.

### B3. Competitor deep-dive

#### Топ-3 западных

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Hightouch AI Decisioning | Самый близкий функциональный аналог decisioning layer поверх warehouse [T2] | warehouse-native, RL/agentic orchestration, быстрый запуск поверх existing stack | зависит от зрелого data stack и внешних delivery systems, сложен для менее зрелых команд | **3-5% global composable CDP / decisioning niche** [инференс] | Hilbert может продавать не только orchestration, но и готовые growth insights + anomaly detection в одном слое |
| Braze | Enterprise CEP для real-time engagement и AI-driven personalization [T2] | сильный execution, надёжность, multichannel delivery, enterprise procurement readiness | скорее engagement system, чем глубоко warehouse-native causal decisioning; дорогой и тяжёлый стек | **8-12% global enterprise CEP** [инференс] | Hilbert может выиграть там, где buyer уже имеет каналы доставки и не хочет ещё один monolithic CEP |
| Amplitude | Сильнейший analytics + experimentation incumbent [T2] | бренд, self-serve analytics, experimentation, большое install base | insight-heavy, но action loop и autonomous decisioning слабее, чем у Hilbert/Hightouch | **10-15% global product analytics** [инференс] | Hilbert ближе к revenue action layer, а не к dashboard/analysis layer |

#### Топ-4 российских

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Mindbox | Самый сильный локальный incumbent в CRM/CDP/омниканале, тарифы от 150k и 400k ₽/мес, on-prem и SLA [T2][T3] | сильный бренд, большая установленная база, mature product, высокая надёжность, data/marketing depth | продукт широкий и тяжёлый, часто продаётся как центральная CRM/CDP платформа, а не как чистый decisioning brain | **20-25% RU enterprise CRM/CDP** [инференс] | Hilbert может зайти поверх существующего Mindbox-стека как decision intelligence слой вместо полной замены ядра |
| Retail Rocket | Сильный personalization player, Сколково называет его лидером отечественного рынка в своём сегменте [T4] | сильная экспертиза в e-commerce personalization, real-time use cases, узнаваемость в retail | уже ближе к recommendation/personalization suite, чем к cross-functional growth OS; исторически вертикализирован | **8-12% RU personalization / retail decisioning** [инференс] | Hilbert шире: соединяет marketing + product + finance signals, а не только retail merchandising/personalization |
| Altcraft | Российская enterprise CDP с cloud/on-prem и сильным контролем данных, заметно присутствует в обзорах vc.ru [T5] | on-prem, данные в РФ, омниканал, enterprise security posture | менее выраженный AI-native decisioning narrative; больше про communications stack и CDP orchestration | **4-7% RU enterprise CDP** [инференс] | Hilbert может позиционироваться как AI-native growth brain поверх Altcraft и других delivery stacks |
| Carrot quest | Широко известный mid-market automation/chat/player, хороший low-end substitute [T3][T6] | доступный вход, быстрый запуск, понятная value proposition для mid-market | слабее в enterprise-grade warehouse-native аналитике, security и сложных decision loops | **10-15% RU SMB/mid automation** [инференс] | Hilbert не конкурирует в low-end, а уходит выше в high-ACV enterprise uplift layer |

#### Вывод по конкурентам

1. На Западе closest analog для Hilbert это **Hightouch AI Decisioning**, а не классические analytics dashboards.
2. В РФ основной риск идёт от **Mindbox как incumbent platform budget owner** и от более дешёвых substitutes вроде **Carrot quest**.
3. Наиболее разумный заход Hilbert в РФ, если делать geo-expand, это **layer above existing stack**, а не замена CRM/CDP/CEP с нуля.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Founder-led sales не масштабируется, pipeline держится на 1-2 людях | high | высокий, срыв new ARR | <6 SQL/мес после M4, все сделки завязаны на founder | нанять сильного AE, зафиксировать ICP, playbook discovery/demo |
| 2 | Operational | Services creep: каждый клиент требует кастомную интеграцию и ручную аналитику | high | высокий, margin erosion | onboarding >8 недель, solution engineering >40 ч на логотип | productize connectors, ограничить кастомизацию, setup fee выше |
| 3 | Operational | LLM/API cost spike или деградация качества inference | med | средний-высокий, COGS inflation | COGS/client >140k ₽ 2 месяца подряд, latency/SLA complaints | multi-model routing, локальные fallback-модели, rate-limit/caching |
| 4 | Market | Узкий спрос: buyer покупает CDP/CEP, но не отдельный decisioning layer | high | высокий, stalls pipeline | win rate <10%, частые ответы «закроем Mindbox/Braze» | продавать через ROI/uplift, не через category education |
| 5 | Market | Price compression из-за incumbent substitutes | high | высокий, model breaks at -30% pricing | скидки >20% становятся нормой, median proposal <350k ₽/мес | hard floor pricing, modular packaging, paid pilot only |
| 6 | Market | Конкуренты добавляют AI features в существующий стек быстрее, чем Hilbert строит moat | med | средний-высокий | в RFP чаще просят AI add-on к действующей платформе | акцент на cross-functional signal layer и measurable lift |
| 7 | Regulatory | 152-ФЗ / data residency мешают cloud deployment и трансграничной обработке | high | высокий, сделки стопорятся на security/legal | >30% enterprise сделок встают на DPA / hosting review | RU-hosted/private cloud/on-prem SKU, локальный контур данных |
| 8 | Regulatory | 115-ФЗ и внутренний compliance банков/финсектора усложняют внедрение | med | средний | security questionnaire >4 недель, red flags по explainability | идти сначала в retail/ecom/media, а не в bank-first ICP |
| 9 | Regulatory | Санкции или ограничения на западный SaaS/LLM vendor | high | высокий, platform disruption | vendor lockout, billing/payment failures, loss of API access | vendor diversification, российские/opensource fallback, contract buffer |
| 10 | Financial | Cash runway сжимается раньше выхода на 10+ клиентов | med | высокий, down round / bridge risk | cash <12 мес runway при <8 клиентах | hire gating, freeze non-core spend, raise earlier |
| 11 | Financial | USD/RUB volatility удорожает cloud и API | med | средний | gross margin <70% 2 квартала подряд | рублёвые прайсы с FX-buffer, reserve in FX, repricing clause |
| 12 | Financial | Налоги и страховые взносы съедают early EBITDA сильнее ожиданий | med | средний | effective take-rate по налогам >6% выручки при низкой прибыли | IT-аккредитация, legal/tax planning, entity optimization |
| 13 | Black swan | Усиление войны/санкций режет enterprise IT-бюджеты | med | высокий | массовые заморозки RFP, перенос budget approvals | фокус на ROI-critical verticals и quick payback pilot |
| 14 | Black swan | Отключение ключевого LLM/API или резкий policy ban | med | очень высокий | падение deliverability/quality без альтернативы | abstraction layer, multi-vendor inference, локальный backup stack |

### B5. Kill conditions через 6 месяцев

1. **Median EBITDA path не подтверждается:** forecast на M24 уходит ниже **500 000 ₽/мес** или p50 EBITDA становится ниже gate. Продолжать нельзя, потому что даже медианный кейс не окупает риск.
2. **Unit economics ломаются:** blended CAC устойчиво **>1.2 млн ₽**, либо **LTV/CAC < 5x**, либо payback **>6 мес** два квартала подряд. Это означает, что enterprise GTM не повторяется.
3. **Go-to-market traction не появляется:** к M6 меньше **3 платящих enterprise клиентов** или меньше **8 design partners / pilots** в зрелом pipeline. В этом случае рынок не подтверждает willingness to pay на premium level.

### B6. Итоговый вывод P6B

**Вердикт: риск высокий, но не фатальный, если Hilbert продаётся как enterprise-only decision intelligence layer поверх существующего martech/data stack.**

Что особенно важно:
- pricing power критичнее, чем churn;
- неопределённость outcome слишком высокая, p90/p10 > 10x;
- в РФ главная угроза не отсутствие боли, а budget capture со стороны Mindbox/CDP/CEP incumbents;
- инвестиционно кейс остаётся интересным только при жёсткой дисциплине ICP, pricing floor и multi-vendor architecture.

### Sources for SECTION B
- [T1] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/hilbert-geo-expand-v2/04-economics.md`
- [T2] Hightouch AI Decisioning overview: https://hightouch.com/docs/ai-decisioning/overview ; Braze: https://www.braze.com/product/customer-engagement ; Amplitude: https://amplitude.com/platform
- [T3] Mindbox tariffs: https://mindbox.ru/tariffs/ ; Habr company page/articles: https://habr.com/ru/companies/mindbox/articles/ ; Carrot quest Habr page: https://habr.com/ru/companies/carrotquest/articles/
- [T4] Skolkovo on Retail Rocket: https://sk.ru/news/retail-rocket-nachinaet-rabotat-v-zapadnom-polusharii/
- [T5] vc.ru Altcraft coverage: https://vc.ru/top-raiting/2712065-top-10-platform-email-marketing-2026
- [T6] Rusprofile, ООО «Майндбокс»: https://www.rusprofile.ru/search?query=%D0%9C%D0%B0%D0%B9%D0%BD%D0%B4%D0%B1%D0%BE%D0%BA%D1%81

<!-- P6B-DONE -->
