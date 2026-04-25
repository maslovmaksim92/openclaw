## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA / MRR на клиента: **160 000 ₽/мес**.
- COGS на клиента: **42 000 ₽/мес**.
- Gross profit на клиента: **118 000 ₽/мес**.
- Contribution profit на клиента: **118 000 ₽/мес**.
- Variable sales / support allocation: **0 ₽/клиент/мес**.
- Fixed costs: **5 298 000 ₽/мес**.
- Full team FOT: **5 668 000 ₽/мес**.
- CAC по каналам из 04-economics: outbound **210 000 ₽**, paid inbound **240 000 ₽**, partnerships/referrals **177 000 ₽**, blended raw **209 250 ₽**, fully-loaded рабочий CAC **243 100 ₽**.
- LTV: **4 720 000 ₽**, monthly churn benchmark: **2.5%**, LTV/CAC: **19.4x**.
- Налоговый контур для waterfall/net: **УСН 6%**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** по прибыли и **НДС 20%** если компания на ОСНО.
- Страховые взносы **~30% к ФОТ** уже учтены в FOT и fixed costs.
- Для PnL беру 3 сценария new clients / churn: **Base = 1,1,2,2,3,3,4,4,4,4,4,4 при churn 2.5%**, **Optimistic = 1,2,2,3,3,4,4,5,5,5,5,5 при churn 2.0%**, **Pessimistic = 0,1,1,2,2,2,3,3,3,3,3,3 при churn 3.5%**.
- Cash burn = `max(0; -EBITDA)`, cumulative cash считается от **0 ₽** как накопленный дефицит.

### A2. PnL 12 месяцев, Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 4.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.98 | 3.93 | 5.83 | 8.68 | 11.46 | 15.18 | 18.80 | 22.33 | 25.77 | 29.13 | 32.40 |
| MRR, ₽ | 160 000 | 316 000 | 628 100 | 932 398 | 1 389 088 | 1 834 360 | 2 428 501 | 3 007 789 | 3 572 594 | 4 123 279 | 4 660 197 | 5 183 692 |
| COGS, ₽ | 42 000 | 82 950 | 164 876 | 244 754 | 364 635 | 481 520 | 637 482 | 789 545 | 937 806 | 1 082 361 | 1 223 302 | 1 360 719 |
| Gross profit, ₽ | 118 000 | 233 050 | 463 224 | 687 643 | 1 024 452 | 1 352 841 | 1 791 020 | 2 218 244 | 2 634 788 | 3 040 918 | 3 436 895 | 3 822 973 |
| GM% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% |
| Fixed costs, ₽ | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 |
| EBITDA, ₽ | -5 180 000 | -5 064 950 | -4 834 776 | -4 610 357 | -4 273 548 | -3 945 159 | -3 506 980 | -3 079 756 | -2 663 212 | -2 257 082 | -1 861 105 | -1 475 027 |
| Cash burn, ₽ | 5 180 000 | 5 064 950 | 4 834 776 | 4 610 357 | 4 273 548 | 3 945 159 | 3 506 980 | 3 079 756 | 2 663 212 | 2 257 082 | 1 861 105 | 1 475 027 |
| Cumulative cash, ₽ | -5 180 000 | -10 244 950 | -15 079 726 | -19 690 083 | -23 963 631 | -27 908 790 | -31 415 770 | -34 495 526 | -37 158 738 | -39 415 820 | -41 276 924 | -42 751 951 |

### A3. PnL 12 месяцев, Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 5.00 | 5.00 | 5.00 | 5.00 | 5.00 |
| Total clients | 1.00 | 2.98 | 4.92 | 7.82 | 10.67 | 14.45 | 18.16 | 22.80 | 27.34 | 31.80 | 36.16 | 40.44 |
| MRR, ₽ | 160 000 | 476 800 | 787 264 | 1 251 519 | 1 706 488 | 2 312 359 | 2 906 111 | 3 647 989 | 4 375 029 | 5 087 529 | 5 785 778 | 6 470 063 |
| COGS, ₽ | 42 000 | 125 160 | 206 657 | 328 524 | 447 953 | 606 994 | 762 854 | 957 597 | 1 148 445 | 1 335 476 | 1 518 767 | 1 698 391 |
| Gross profit, ₽ | 118 000 | 351 640 | 580 607 | 922 995 | 1 258 535 | 1 705 364 | 2 143 257 | 2 690 392 | 3 226 584 | 3 752 052 | 4 267 011 | 4 771 671 |
| GM% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% |
| Fixed costs, ₽ | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 |
| EBITDA, ₽ | -5 180 000 | -4 946 360 | -4 717 393 | -4 375 005 | -4 039 465 | -3 592 636 | -3 154 743 | -2 607 608 | -2 071 416 | -1 545 948 | -1 030 989 | -526 329 |
| Cash burn, ₽ | 5 180 000 | 4 946 360 | 4 717 393 | 4 375 005 | 4 039 465 | 3 592 636 | 3 154 743 | 2 607 608 | 2 071 416 | 1 545 948 | 1 030 989 | 526 329 |
| Cumulative cash, ₽ | -5 180 000 | -10 126 360 | -14 843 753 | -19 218 758 | -23 258 223 | -26 850 858 | -30 005 601 | -32 613 209 | -34 684 625 | -36 230 572 | -37 261 561 | -37 787 890 |

### A4. PnL 12 месяцев, Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 1.00 | 1.96 | 3.90 | 5.76 | 7.56 | 10.29 | 12.93 | 15.48 | 17.94 | 20.31 | 22.60 |
| MRR, ₽ | 0 | 160 000 | 314 400 | 623 396 | 921 577 | 1 209 322 | 1 646 996 | 2 069 351 | 2 476 924 | 2 870 231 | 3 249 773 | 3 616 031 |
| COGS, ₽ | 0 | 42 000 | 82 530 | 163 641 | 241 914 | 317 447 | 432 336 | 543 205 | 650 192 | 753 436 | 853 065 | 949 208 |
| Gross profit, ₽ | 0 | 118 000 | 231 870 | 459 755 | 679 663 | 891 875 | 1 214 659 | 1 526 146 | 1 826 731 | 2 116 796 | 2 396 708 | 2 666 823 |
| GM% | 0.0% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% |
| Fixed costs, ₽ | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 |
| EBITDA, ₽ | -5 298 000 | -5 180 000 | -5 066 130 | -4 838 245 | -4 618 337 | -4 406 125 | -4 083 341 | -3 771 854 | -3 471 269 | -3 181 204 | -2 901 292 | -2 631 177 |
| Cash burn, ₽ | 5 298 000 | 5 180 000 | 5 066 130 | 4 838 245 | 4 618 337 | 4 406 125 | 4 083 341 | 3 771 854 | 3 471 269 | 3 181 204 | 2 901 292 | 2 631 177 |
| Cumulative cash, ₽ | -5 298 000 | -10 478 000 | -15 544 130 | -20 382 375 | -25 000 712 | -29 406 837 | -33 490 178 | -37 262 032 | -40 733 301 | -43 914 505 | -46 815 798 | -49 446 975 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### На 1 клиента / месяц
- **ARPA:** 160 000 ₽
- **COGS:** 42 000 ₽
- **Gross profit:** 118 000 ₽
- **Variable sales / support:** 0 ₽
- **Contribution:** 118 000 ₽

#### На уровне EBITDA break-even
- **EBITDA break-even clients по gross profit:** `5 298 000 / 118 000 = 44.9`, округлённо **45 клиентов**.
- Revenue: **7 200 000 ₽/мес**
- COGS: **1 890 000 ₽/мес**
- Gross profit: **5 310 000 ₽/мес**
- EBITDA: **12 000 ₽/мес**

#### На уровне contribution break-even
- **Contribution break-even clients:** `5 298 000 / 118 000 = 44.9`, округлённо **45 клиентов**.
- Revenue: **7 200 000 ₽/мес**
- COGS: **1 890 000 ₽/мес**
- Gross profit: **5 310 000 ₽/мес**
- Variable sales / support: **0 ₽/мес**
- Contribution: **5 310 000 ₽/мес**
- EBITDA: **12 000 ₽/мес**

#### Net после налогов РФ
- **УСН 6%:** `12 000 - 432 000 = -420 000 ₽/мес`
- **IT-льгота 3%:** `12 000 - 216 000 = -204 000 ₽/мес`
- **ОСНО 20%:** `12 000 × 0.8 = 9 600 ₽/мес` до кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub

| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Base | M17 | 44 980 738 ₽ | реалистичный путь требует полного seed-runway |
| Optimistic | M14 | 37 819 652 ₽ | лучший ramp, но первый год всё ещё ниже EBITDA 0 |
| Pessimistic | M25 | 63 084 173 ₽ | замедление продаж резко ухудшает capital need |

### A7. Налоговая модель РФ
- **УСН 6% с выручки** проще всего администрировать, но на масштабе около 45 клиентов почти полностью съедает ранний EBITDA.
- **IT-льгота 3%** materially лучше для этого кейса, если есть аккредитация Минцифры и выдержана доля профильной выручки.
- **ОСНО 20%** по прибыли выглядит мягче только после прохождения EBITDA break-even, но добавляет **НДС 20%** и ухудшает cash conversion.
- **Страховые взносы ~30% к ФОТ** уже учтены внутри FOT **5 668 000 ₽/мес** и fixed costs **5 298 000 ₽/мес**, повторно не начисляются.
- Для этого кейса рабочая база, это **УСН / IT-льгота**, а не ОСНО.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Base | 45 | 45 | M17 | вне 12 месяцев, но в разумном горизонте seed-scale |
| Optimistic | 45 | 45 | M14 | выполнимо быстрее за счёт 49+ клиентов уже к M14 |
| Pessimistic | 45 | 45 | M25 | при таком ramp модель становится тяжёлой operationally |

### A9. Вывод по PnL
- Во всех трёх сценариях **первый год остаётся EBITDA-отрицательным**, хотя optimistic почти выходит в ноль к M12.
- Экономика выглядит рабочей, потому что **gross profit на клиента 118 тыс. ₽** и break-even достигается не на сотнях, а примерно на **45 клиентах**.
- Главный риск модели, это не unit margin, а **способность дойти до 45-50 активных клиентов без service creep и ARPU compression**.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База берётся из SECTION A: **M12 EBITDA = -1 475 027 ₽/мес** при **32.4 клиента** на M12. Для sensitivity считаю, что объём клиентов и delivery-структура сохраняются, а меняется один драйвер за раз.

| Сценарий | Изменение | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | **-1 475 027** | — | уже отрицательная EBITDA к M12 |
| Sens1 | CAC x2 | **-2 447 427** | -972 400 | если fully-loaded CAC удваивается, модель теряет почти ещё 1 млн ₽/мес EBITDA |
| Sens2 | Churn x2 | **-1 846 758** | -371 731 | база клиентов на M12 падает примерно до 29.25 |
| Sens3 | Price -30% | **-3 030 135** | -1 555 108 | самый болезненный удар, потому что gross profit на клиента падает с 118k до 70k ₽ |

**Вывод:** ключевая хрупкость не в nominal CAC payback, а в том, что при price compression или CAC inflation путь к break-even резко отъезжает вправо.

### B2. Monte Carlo Lite — confidence intervals

Ниже не полноценный кодовый Monte Carlo, а **lite-аппроксимация через triangular inputs и 9 комбинаций**. Это достаточно, чтобы понять диапазон хрупкости модели на M24.

#### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 180 000 | 243 100 | 420 000 | [T1] + base CAC из 04-economics |
| Monthly churn, % | 1.5% | 2.5% | 5.0% | [T2], [T3] |
| ARPU, ₽/мес | 130 000 | 160 000 | 190 000 | [T1], [T4] |
| Conversion rate lead→paid, % | 0.20% | 0.30% | 0.45% | 04-economics blended funnel + upside on partner mix |
| Time-to-hire, мес | 1.0 | 1.5 | 2.5 | 04-economics hiring table |

#### Логика симуляции
- Взял 9 комбинаций вокруг min / mode / max для CAC, churn и ARPU.
- Lead→paid conversion и time-to-hire использовал как вторичные модификаторы скорости выхода на клиентскую базу к M24.
- p10/p50/p90 выбраны по ранжированию 9 результатов, а не по одной жёсткой pess/base/opt линии.

#### Результат: confidence intervals

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | **-2 462 979** | **2 470 107** | **9 634 510** | **12 097 489** |
| CAC payback, мес | **1.12** | **1.52** | **3.23** | **2.11** |
| LTV/CAC | **7.24x** | **19.42x** | **32.36x** | **25.12x** |
| Cash runway, мес | **16.2** | **>24** | **>24** | **>7.8** |

#### Интерпретация правил
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1**: риск неплатёжеспособности при плохой реализации.
2. **p50 EBITDA > 500k ₽/мес**, значит median-case формально проходит EBITDA Gate, но запас зависит от удержания price discipline.
3. **p90 / |p10| ≈ 3.9x**, то есть неопределённость большая, но ещё не экстремальная 10x.
4. **Range width по LTV/CAC = 25.12x > 8**, значит модель действительно хрупкая: достаточно просадки по pricing, churn или CAC, и «красивые» unit economics перестают быть опорой.

**Итог Monte Carlo Lite:** на бумаге upside сильный, но downside всё ещё уводит компанию в отрицательный EBITDA даже на M24. Это не reject автоматически, но требует более жёсткого risk discount, чем SECTION A могла показывать по точечной базе.

### B3. Competitor deep-dive

#### B3.1. Западные конкуренты

| Конкурент | Что делает | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Ramp** | spend/AP/finance automation platform | сильный product suite, 50k+ business customers, мощный workflow around AP and spend [T5] | US-first stack, слабая локальность под 1С/РФ-налоги, меньше managed-service handholding | **6-8%** в US SMB/mid-market AP/spend automation, оценка по customer base [inference] | локализация под 1С, ЭДО, payroll, банки РФ и возможность дать managed ops, а не только software |
| **Finally** | AI-native back-office platform: bookkeeping, payroll, AP, invoicing | closest category match, единая finance suite, 3 500+ клиентов [T1] | западный compliance stack, limited proof for Russia-like regulatory complexity | **<1% globally**, нишевой but category-defining player [inference] | можем быть глубже в российском compliance и в human-in-the-loop delivery для SMB |
| **Nanonets** | AP/document AI automation | сильный wedge в invoice/AP, 99%+ extraction claims, broad ERP integrations [T6][T7] | это скорее infra layer, а не полный finance operator; customer still needs ops orchestration | **1-2%** глобально в invoice/AP automation, оценка по category visibility [inference] | можем закрывать не только extraction, но и month-end close, payroll, invoicing, QA и SLA как сервис |

#### B3.2. Российские конкуренты

| Конкурент | Источник | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Моё дело** | vc.ru рейтинги и обзоры аутсорсинга [T8][T9] | сильный бренд в онлайн-бухгалтерии, широкий SMB reach, self-serve + аутсорс контур | ближе к классической онлайн-бухгалтерии, меньше AI-first positioning | **8-12%** российского digital accounting SMB сегмента [inference] | мы идём не в «бухгалтерию как сервис», а в AI-first finance operations layer с AP/invoicing/reconciliation |
| **Кнопка** | vc.ru обзоры и тарифные разборы [T10][T11] | сильный сервисный слой, живые бухгалтеры, all-in outsourced experience | низкая software defensibility, price-sensitive service model, меньше AI moat | **3-5%** в premium SMB аутсорсинге [inference] | выше automation density и шанс удержать gross margin лучше классического аутсорса |
| **Контур / Контур.Аутсорс** | vc.ru обзоры рынка [T12][T13] | крупнейшая экосистема, distribution, отчётность, интеграции, доверие рынка | продукт скорее horizontal accounting stack, чем AI-first operator | **12-18%** в digital accounting / отчетном ПО и adjacent outsourcing [inference] | можем атаковать узкий wedge: finance ops as outcome, а не как набор инструментов |
| **Биорг / Beorg Smart Vision** | Rusprofile + Skolkovo [T14][T15] | сильный документный AI, локальный residency, proof в обработке документов и банках | не full-stack finance operator, нужен партнёр/клиент для закрытия всей ops-цепочки | **1-2%** в российском document AI для финансовых документов [inference] | закрываем поверх OCR весь workflow, включая people/process/SLA |
| **1С / OCR-надстройки вокруг 1С (в т.ч. CORRECT, 1С-распознавание)** | Habr [T16] | natural fit в 1С-контур, низкий switching cost для бухгалтера, широкий installed base | это feature-level automation, а не end-to-end operator; качество зависит от manual verification | **20%+ installed-base share** как базовая платформа учета, но не как AI-operator [inference] | можно забрать outcome-layer над 1С: ingestion + AP + QA + close + customer success, а не просто OCR-модуль |

**Вывод по конкурентам:**
- На Западе category proof уже есть, но почти все сильные игроки заточены под US stack.
- В РФ рынок фрагментирован между **классическим аутсорсом**, **1С-экосистемой** и **точечным document AI**.
- Это даёт окно для позиционирования: **не очередная бухгалтерия и не просто OCR, а managed AI finance operator для SMB**.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | не удаётся нанять CTO / ML / chief accountant вовремя | med | high | time-to-hire >2 мес по ключевым ролям | заранее формировать bench, внешние advisors, stage-gated hiring |
| 2 | Operational | service creep, каждая сделка превращается в кастомный проект | high | high | onboarding >10 рабочих дней, нестандартные интеграции >30% новых клиентов | жёсткий ICP, blacklist сложных кейсов, productized onboarding |
| 3 | Operational | деградация качества LLM/OCR на длинном хвосте документов | med | high | доля manual correction >20%, рост QA-ошибок | fallback rules engine, human-in-the-loop QA, versioned prompts/models |
| 4 | Operational | зависимость от внешних LLM/API-поставщиков | med | high | рост latency/cost, frequent outages, rate limits | multi-model routing, локальные fallback-модели, кэш и batch-processing |
| 5 | Market | SMB не готов платить 160k ₽/мес, рынок тянет к 90-120k ₽ | high | high | win-rate падает при quote >120k ₽ | перепаковать в tiered offer, выделить wedge SKU, upsell later |
| 6 | Market | price compression из-за классического бухаутсорса | high | high | в переговорах доминирует сравнение с бухаутсорсом 20-60k ₽ | продавать SLA/скорость/visibility, а не «ведение бухгалтерии» |
| 7 | Market | крупные игроки типа Контур/1С/Saby копируют feature-set | med | high | релизы AP/OCR/workflow automation у incumbents | строить moat в delivery-data-process layer и customer integration depth |
| 8 | Market | churn оказывается ближе к 5%/мес, а не к 2.5% | med | high | logo churn >3% три месяца подряд | усилить CS, QBR, embedded workflows, annual contracts |
| 9 | Regulatory | несоответствие 152-ФЗ / data residency | med | high | юристы клиентов блокируют доступы, security review >30 дней | RU-hosting, DPA, data maps, on-prem / private cloud option |
| 10 | Regulatory | кейсы попадают под 115-ФЗ и вызывают блокировки/ручные проверки | med | med/high | больше запросов банка по suspicious ops | ограничить high-risk verticals, AML playbooks, escalation path |
| 11 | Regulatory | санкции режут доступ к зарубежным SaaS и LLM | high | high | vendor notices, billing/payment failures | импортонезависимый стек, резервные российские провайдеры |
| 12 | Regulatory | налоговые/кадровые изменения ломают шаблоны автоматизации | med | med | frequent exceptions after law updates | методологический контур, rule updates, legal watch |
| 13 | Financial | runway съедается до выхода на 45 клиентов | high | high | cash <9 мес runway, burn выше плана на 20%+ | stage hiring, weekly burn review, early bridge planning |
| 14 | Financial | рост USD ухудшает себестоимость LLM/infra | med | med/high | FX >110 RUB/USD или рост vendor invoices >25% | рублёвые контракты где возможно, price indexation, local models |
| 15 | Financial | инфляция зарплат и налоговая нагрузка раздувают fixed costs | med | med | FOT plan +15% vs budget | quarterly repricing, comp bands, automation of backoffice |
| 16 | Financial | просадка collection / отсрочки платежа ухудшают cash conversion | med | med/high | DSO >30 дней, просрочка >10% MRR | предоплата, stricter billing terms, autopay |
| 17 | Black swan | резкое ужесточение санкций на SaaS / cloud / payments | med | high | новые ограничения по расчётам и cloud accounts | sovereign stack, резервные провайдеры, минимизация single points of failure |
| 18 | Black swan | отключение ключевого LLM-провайдера на недели | med | high | repeated incidents / policy bans | модельный abstraction layer, prompt portability, резервный inference |
| 19 | Black swan | военная/макроэскалация бьёт по SMB спросу | med | high | freeze новых договоров, рост churn у клиентов crisis-sensitive сегментов | focus на resilient verticals, flexible pricing, burn containment |
| 20 | Black swan | крупная data/security авария разрушает доверие | low/med | very high | security incidents, failed audits, anomalous access logs | zero-trust, audit trail, encryption, incident response drills |

### B5. Kill conditions через 6 месяцев

1. **Median risk gate:** если обновлённый p10 EBITDA@M24 остаётся **< 0** и cash runway **< 9 мес**, проект нельзя продолжать.
2. **Commercial gate:** если к M6 активных платящих клиентов **< 8** или новый sale не держит **ARPU ≥ 130k ₽/мес**, GTM-гипотеза не подтверждается.
3. **Retention/quality gate:** если churn **>4%/мес** два квартала подряд или manual correction rate **>25%**, automation moat отсутствует и модель превращается в обычный аутсорс.

### B6. Итоговый критический вывод

Кейс всё ещё выглядит **интересным**, но после risk-layer он уже не выглядит «лёгким PASS». SECTION A показывала красивую LTV/CAC-картину, однако SECTION B показывает более жёсткую правду:
- downside-case на M24 остаётся отрицательным;
- pricing power критичнее, чем казалось в точечной модели;
- конкурировать придётся сразу против **аутсорса**, **1С-экосистемы** и **document-AI игроков**.

**Мой итог:** это скорее **PASS WITH HEAVY RISK DISCOUNT**, а не clean green-light. Инвестировать можно только если команда доказывает productized delivery, удерживает чек **130-160k ₽+** и быстро показывает, что это не «ещё одна бухгалтерия».

## Sources for SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-first-finansovyy-operator-dlya-smb/02-demand.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-first-finansovyy-operator-dlya-smb/04-economics.md
- [T3] https://www.saas-capital.com/blog-posts/2025-b2b-saas-retention-benchmarks/
- [T4] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-first-finansovyy-operator-dlya-smb/00-brief.md
- [T5] https://ramp.com/
- [T6] https://nanonets.com/ap-automation
- [T7] https://techcrunch.com/2024/03/12/nanonets-funding-accel-india/
- [T8] https://vc.ru/services/1479376-buhgalterskii-autsorsing-reiting-luchshih-onlain-servisov-v-2026-godu
- [T9] https://vc.ru/marketing/2285150-top-15-autsorsingovykh-kompanij-moskvy
- [T10] https://vc.ru/id5314066/2866933-onlayn-bukhgalteriya-dlya-ip-obzor-servisov-i-zakonov
- [T11] https://vc.ru/services/2259043-servisy-dlya-vedeniya-buhgalterii-top-11-luchshikh
- [T12] https://vc.ru/marketing/2285150-top-15-autsorsingovykh-kompanij-moskvy
- [T13] https://vc.ru/services/2229487-kontur-elba-onlajn-buhgalteriya-dlya-ip-i-ooo
- [T14] https://www.rusprofile.ru/id/10836745
- [T15] https://sk.ru/news/ms-bank-rus-uprostil-vydachu-avtokreditov-s-pomoshyu-rossijskoj-tehnologii-raspoznavaniya-dokumentov/
- [T16] https://habr.com/ru/articles/582910/

<!-- P6B-DONE -->
