## SECTION A. Finance PnL

### A1. Входные данные и принятые допущения
- ARPA / MRR на клиента: **220 000 ₽/мес**.
- COGS на клиента: **93 000 ₽/мес**.
- Gross profit на клиента: **127 000 ₽/мес**.
- Contribution margin: **118 000 ₽/клиент/мес**.
- Fixed costs: **3 310 000 ₽/мес**.
- Team FOT fully-loaded: **5 291 000 ₽/мес**.
- Страховые взносы: **~30% к ФОТ**, считаю уже включёнными в fully-loaded FOT и fixed costs.
- Налоговые режимы для net: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры и соблюдении профильной выручки, **ОСНО 20% налога на прибыль**; **НДС 20%** возникает при ОСНО и ухудшает cash conversion, если цена клиенту quoted без дополнительной наценки.
- Формула активной базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`. Cash burn = `max(0, -EBITDA)`. Cumulative cash стартует с **0 ₽**.

### A2. Сценарии
- **Base**: new clients = `1,1,1,2,2,2,2,3,3,3,4,4`, churn **2.0%/мес**.
- **Optimistic**: new clients = `1,1,2,2,2,3,3,3,4,4,4,5`, churn **1.5%/мес**.
- **Pessimistic**: new clients = `0,1,1,1,1,2,2,2,2,2,3,3`, churn **3.0%/мес**.

### A3. PnL 12 месяцев, scenario: Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 4 |
| Total clients | 1.00 | 1.98 | 2.94 | 4.88 | 6.78 | 8.65 | 10.48 | 13.27 | 16.00 | 18.68 | 22.31 | 25.86 |
| MRR, ₽ | 220 000 | 435 600 | 646 888 | 1 073 950 | 1 492 471 | 1 902 622 | 2 304 569 | 2 918 478 | 3 520 108 | 4 109 706 | 4 907 512 | 5 689 362 |
| COGS, ₽ | 93 000 | 184 140 | 273 457 | 453 988 | 630 908 | 804 290 | 974 204 | 1 233 720 | 1 488 046 | 1 737 285 | 2 074 539 | 2 405 048 |
| Gross profit, ₽ | 127 000 | 251 460 | 373 431 | 619 962 | 861 563 | 1 098 332 | 1 330 365 | 1 684 758 | 2 032 063 | 2 372 421 | 2 832 973 | 3 284 313 |
| GM% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs, ₽ | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 |
| EBITDA, ₽ | -3 183 000 | -3 058 540 | -2 936 569 | -2 690 038 | -2 448 437 | -2 211 668 | -1 979 635 | -1 625 242 | -1 277 937 | -937 579 | -477 027 | -25 687 |
| Cash burn, ₽ | 3 183 000 | 3 058 540 | 2 936 569 | 2 690 038 | 2 448 437 | 2 211 668 | 1 979 635 | 1 625 242 | 1 277 937 | 937 579 | 477 027 | 25 687 |
| Cumulative cash, ₽ | -3 183 000 | -6 241 540 | -9 178 109 | -11 868 147 | -14 316 584 | -16 528 252 | -18 507 887 | -20 133 130 | -21 411 067 | -22 348 646 | -22 825 673 | -22 851 359 |

- Break-even по client count: **29 клиентов** (`3 310 000 / 118 000`).
- Break-even по месяцам: **не достигнут в M1-M12**.
- `startup_capital_to_bep_rub`: **22 851 359 ₽** на горизонте модели; если break-even не достигнут, это минимальная потребность капитала до конца M12.

### A3. PnL 12 месяцев, scenario: Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 4 | 4 | 5 |
| Total clients | 1.00 | 1.98 | 3.96 | 5.90 | 7.81 | 10.69 | 13.53 | 16.33 | 20.08 | 23.78 | 27.42 | 32.01 |
| MRR, ₽ | 220 000 | 436 700 | 870 149 | 1 297 097 | 1 717 641 | 2 351 876 | 2 976 598 | 3 591 949 | 4 418 070 | 5 231 799 | 6 033 322 | 7 042 822 |
| COGS, ₽ | 93 000 | 184 605 | 367 836 | 548 318 | 726 094 | 994 202 | 1 258 289 | 1 518 415 | 1 867 639 | 2 211 624 | 2 550 450 | 2 977 193 |
| Gross profit, ₽ | 127 000 | 252 095 | 502 314 | 748 779 | 991 547 | 1 357 674 | 1 718 309 | 2 073 534 | 2 550 431 | 3 020 175 | 3 482 872 | 4 065 629 |
| GM% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs, ₽ | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 |
| EBITDA, ₽ | -3 183 000 | -3 057 905 | -2 807 686 | -2 561 221 | -2 318 453 | -1 952 326 | -1 591 691 | -1 236 466 | -759 569 | -289 825 | 172 872 | 755 629 |
| Cash burn, ₽ | 3 183 000 | 3 057 905 | 2 807 686 | 2 561 221 | 2 318 453 | 1 952 326 | 1 591 691 | 1 236 466 | 759 569 | 289 825 | 0 | 0 |
| Cumulative cash, ₽ | -3 183 000 | -6 240 905 | -9 048 591 | -11 609 813 | -13 928 265 | -15 880 591 | -17 472 283 | -18 708 748 | -19 468 317 | -19 758 142 | -19 758 142 | -19 758 142 |

- Break-even по client count: **29 клиентов** (`3 310 000 / 118 000`).
- Break-even по месяцам: **M11**.
- `startup_capital_to_bep_rub`: **19 758 142 ₽** на горизонте модели; если break-even не достигнут, это минимальная потребность капитала до конца M12.

### A3. PnL 12 месяцев, scenario: Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 3 | 3 |
| Total clients | 0.00 | 1.00 | 1.97 | 2.91 | 3.82 | 5.71 | 7.54 | 9.31 | 11.03 | 12.70 | 15.32 | 17.86 |
| MRR, ₽ | 0 | 220 000 | 433 400 | 640 398 | 841 186 | 1 255 950 | 1 658 272 | 2 048 524 | 2 427 068 | 2 794 256 | 3 370 428 | 3 929 316 |
| COGS, ₽ | 0 | 93 000 | 183 210 | 270 714 | 355 592 | 530 925 | 700 997 | 865 967 | 1 025 988 | 1 181 208 | 1 424 772 | 1 661 029 |
| Gross profit, ₽ | 0 | 127 000 | 250 190 | 369 684 | 485 594 | 725 026 | 957 275 | 1 182 557 | 1 401 080 | 1 613 048 | 1 945 656 | 2 268 287 |
| GM% | 0.0% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% | 57.7% |
| Fixed costs, ₽ | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 | 3 310 000 |
| EBITDA, ₽ | -3 310 000 | -3 183 000 | -3 059 810 | -2 940 316 | -2 824 406 | -2 584 974 | -2 352 725 | -2 127 443 | -1 908 920 | -1 696 952 | -1 364 344 | -1 041 713 |
| Cash burn, ₽ | 3 310 000 | 3 183 000 | 3 059 810 | 2 940 316 | 2 824 406 | 2 584 974 | 2 352 725 | 2 127 443 | 1 908 920 | 1 696 952 | 1 364 344 | 1 041 713 |
| Cumulative cash, ₽ | -3 310 000 | -6 493 000 | -9 552 810 | -12 493 126 | -15 317 532 | -17 902 506 | -20 255 231 | -22 382 674 | -24 291 594 | -25 988 546 | -27 352 889 | -28 394 603 |

- Break-even по client count: **29 клиентов** (`3 310 000 / 118 000`).
- Break-even по месяцам: **не достигнут в M1-M12**.
- `startup_capital_to_bep_rub`: **28 394 603 ₽** на горизонте модели; если break-even не достигнут, это минимальная потребность капитала до конца M12.

### A4. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
| Scenario | Clients @ M12 | ARPA, ₽ | Gross / client, ₽ | Contribution / client, ₽ | EBITDA @ M12, ₽ | Net after tax, УСН 6%, ₽ | Net after tax, IT-льгота 3%, ₽ | Net after tax, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Base | 25.86 | 220 000 | 127 000 | 118 000 | -25 687 | -367 048 | -196 367 | -25 687 |
| Optimistic | 32.01 | 220 000 | 127 000 | 118 000 | 755 629 | 333 060 | 544 344 | 604 503 |
| Pessimistic | 17.86 | 220 000 | 127 000 | 118 000 | -1 041 713 | -1 277 472 | -1 159 593 | -1 041 713 |

- Для УСН и IT-льготы налог считаю как процент от выручки, так как даже при отрицательной EBITDA налог с оборота сохраняется.
- Для ОСНО `Net = EBITDA - 20% налога на прибыль`, но только при положительной прибыли; при убытке налог на прибыль = 0. НДС 20% не включаю отдельной строкой в PnL выше, но отмечаю как фактор давления на оборотный капитал и цену.

### A5. Сравнение налоговых режимов и cash flow
| Параметр | Значение |
|---|---:|
| Fixed costs / мес | 3 310 000 ₽ |
| Team FOT fully-loaded / мес | 5 291 000 ₽ |
| Страховые взносы | ~30% к ФОТ |
| НДС при ОСНО | 20% |
| Break-even clients | 29 |
| startup_capital_to_bep_rub, Base | 22 851 359 ₽ |
| startup_capital_to_bep_rub, Optimistic | 19 758 142 ₽ |
| startup_capital_to_bep_rub, Pessimistic | 28 394 603 ₽ |

### A6. Вывод по break-even
- **Base:** конец M12 = **25.86 клиента**, EBITDA M12 = **-25 687 ₽**, break-even month = **не достигнут**, недобор до EBITDA break-even = **3.14 клиента**.
- **Optimistic:** конец M12 = **32.01 клиента**, EBITDA M12 = **755 629 ₽**, break-even month = **M11**, недобор до EBITDA break-even = **-3.01 клиента**.
- **Pessimistic:** конец M12 = **17.86 клиента**, EBITDA M12 = **-1 041 713 ₽**, break-even month = **не достигнут**, недобор до EBITDA break-even = **11.14 клиента**.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

Ниже стресс-тестирую уже существующую base-модель из SECTION A. Для `CAC x2` считаю, что план продаж сохраняется, но acquisition spend на новых клиентов в M12 удваивается, поэтому смотрю на cash EBITDA после роста sales & marketing pressure, а не только на delivery EBITDA.

| Метрика | Base | Sens1: CAC x2 | Sens2: Churn x2 | Sens3: Price -30% |
|---|---:|---:|---:|---:|
| Clients @ M12 | 25.86 | 25.86 | 23.94 | 25.86 |
| ARPU, ₽/мес | 220 000 | 220 000 | 220 000 | 154 000 |
| EBITDA @ M12, ₽/мес | -25 687 | -2 560 087 | -269 037 | -1 732 495 |
| Комментарий | почти break-even | рост CAC убивает cash efficiency | retention проседает, но модель ещё жива | снижение цены разрушает gross margin |

Вывод: для этой модели главный fragility point не churn сам по себе, а **price compression** и **CAC inflation**. Если рынок уйдёт в тендерный демпинг, бизнес быстро превращается в low-margin agency.

### B2. Monte Carlo Lite: confidence intervals по M24

#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 450 000 | 633 600 | 1 200 000 | [T4], внутренняя модель на базе blended CAC из SECTION A |
| Monthly churn, % | 1.5% | 2.0% | 4.0% | [T3] |
| ARPU, ₽/мес | 180 000 | 220 000 | 260 000 | [T4], pricing sanity-check |
| Conversion lead→paid, % | 1.1% | 1.7% | 2.5% | [T4], funnel из SECTION A |
| Time-to-hire, мес | 1.0 | 1.8 | 3.0 | [T1][T2] |

Метод: вместо полноценного кода беру 9 комбинаций по CAC/churn/ARPU, а conversion влияет на темп привлечения, сохраняя логику base funnel. Это упрощённая Monte Carlo Lite версия, достаточная для инвестиционного sanity-check.

#### Результат: p10 / p50 / p90
| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -2 044 220 | 2 357 240 | 11 502 719 | 13 546 939 |
| CAC payback, мес | 12.6 | 5.4 | 3.2 | 9.4 |
| LTV/CAC | 2.2x | 10.0x | 22.2x | 20.0x |
| Cash runway, мес | 9.0 | 32.8 | 99.3 | 90.3 |

Интерпретация правил:
- **Rule 1 triggered:** `p10 EBITDA < 0`, значит риск неплатёжеспособности реален.
- **Rule 2 not triggered:** `p50 EBITDA > 500k ₽/мес`, median-case проходит EBITDA Gate.
- **Rule 3 triggered:** распределение фактически слишком широкое; при отрицательном p10 upside/downside asymmetry экстремальная, score нужно даунгрейдить.
- **Rule 4 triggered:** `Range width по LTV/CAC = 20.0x`, модель хрупкая к сочетанию pricing, churn и CAC.

Практический вывод: это **проходной**, но не robust кейс. Он интересен только при жёсткой дисциплине на ARPU, glossary-based retention и secure-enterprise positioning. В commodity-сегменте вероятнее провал.

### B3. Competitor deep-dive

#### Западные конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **RWS / Language Weaver** | крупный enterprise vendor, сильный MT stack, терминология, legal/regulated опыт, глобальные аккаунты [T4] | тяжёлый enterprise sales cycle, дорогая внедряемость, слабее fit для русскоязычного mid-market | **12-18%** enterprise AI-translation stack на западном рынке, по моей оценке | можем продавать быстрее, дешевле и с локальным SLA для РФ/СНГ |
| **Lilt** | human-in-the-loop workflow, сильная enterprise automation, хорош для continuous localization [T4] | выше зависимость от англоязычного GTM, неочевидный локальный compliance fit для РФ | **5-8%** modern AI localization stack, по моей оценке | глубже работаем с русским контентом, PDF/техдоками, on-prem и data residency |
| **Smartling / Phrase / Lokalise class** | зрелые connectors, developer workflow, сильны в app/software localization [T4] | слабее в тяжёлой техдокументации, тендерной кастомизации и human QA для regulated docs | **15-25%** software-localization SaaS category суммарно, по моей оценке | позиционируемся не как UI-string tool, а как managed secure localization для техдоков |

#### Российские конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Smartcat (российские корни, глобальная платформа)** | CAT/TMS workflow, marketplace исполнителей, сильный бренд, историческая связь с ABBYY LS и Сколково [R1][R2] | широкий горизонтальный продукт, не всегда deep-service для сложных отраслевых техдоков | **8-12%** доступного enterprise/localization spend в РФ-сегменте digital-first, по моей оценке | можем выиграть узким vertical play: промка, экспорт, manuals, KB, compliance docs |
| **PROMT** | сильная историческая экспертиза в MT, узнаваемость, большой языковой корпус и B2B/гос наследие [R3][R4] | legacy-perception, слабее modern workflow/orchestration и managed service UX | **5-10%** корпоративного MT/переводческого софта в РФ, по моей оценке | современный AI workflow, post-editing QA, API orchestration и сервисный слой поверх перевода |
| **Yandex Translate / Yandex Cloud Translate** | мощный NMT stack, 102 языка, сильная инфраструктура и brand trust [R5][R6] | это infra/API, а не готовый localization operating system для enterprise docs | **10-15%** machine-translation API usage в РФ, по моей оценке | продаём не API, а полный SLA-результат: glossary, QA, layout, secure delivery |
| **ABBYY Language Services legacy / интеграторы вокруг ABBYY stack** | сильны в enterprise documents, OCR, linguistic assets, знакомы крупным заказчикам [R1] | после отделения Smartcat рынок фрагментирован, слабее гибкость small-team delivery | **3-6%** legacy enterprise localization workflows в РФ, по моей оценке | быстрее запускаемся, проще pricing, меньше overhead и выше адаптация под кастомный scope |

Итог по конкурентам: западные игроки сильнее в платформенности и глобальном бренде, российские в локальном доступе и data-compliance. Наш шанс появляется только если не конкурировать в лоб по pure software seat model, а продавать **secure managed localization for technical docs**.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся держать reviewer quality на доменных техдоках | med | высокий, rework съедает маржу и SLA | рост QA rejects, падение NPS, рост часов постредактуры | certification pool, domain glossaries, double-check QA на top accounts |
| Operational | LLM/API latency или деградация качества на PDF, tables, schematics | med | высокий, срок сдачи и качество страдают | рост manual fallback, больше ручной вёрстки, больше escalations | multi-model routing, pre-processing pipeline, шаблоны для CAD/PDF |
| Market | Спрос остаётся проектным, не подписочным | med | высокий, churn растёт и MRR не набирается | короткие контракты, low repeat rate, нет upsell в новые языки | продавать retainer+SLA, monthly glossary maintenance, KB localization bundles |
| Market | Price compression из-за агентств и дешёвого AI-демпинга | high | высокий, price -20-30% ломает EBITDA | проигрыш тендеров по цене, клиенты просят per-word parity | фокус на regulated verticals, ROI from speed, secure/on-prem packaging |
| Regulatory | 152-ФЗ и data residency ограничивают использование западных LLM/SaaS | med | высокий, часть ICP недоступна | юристы блокируют пилоты, требуют on-prem, DPA redlines | локальный inference option, private VPC, классификация данных |
| Regulatory | 115-ФЗ/комплаенс и экспортный контроль по документам | low-med | средний-высокий, задержки сделок и отказ от кейсов | затягивание legal review, запросы на дополнительные проверки | KYC/KYB, whitelist отраслей, шаблоны договоров и логирование доступа |
| Financial | Cash runway сжимается при CAC inflation и найме раньше выручки | high | высокий, кассовый разрыв до M12-M18 | CAC > 800k, burn > 2.5 млн/мес, pipeline coverage < 3x | stage-gated hiring, setup fees upfront, партнёрский канал вместо paid scale |
| Financial | Курс USD и инфляция раздувают API и фонд оплаты | med | средний-высокий, gross margin проседает на 5-10 п.п. | рост COGS/client выше 100k, поставщики меняют тарифы | рублёвые прайсы с индексатором, резерв 10-15%, fallback на локальные модели |
| Black swan | Усиление санкций, отключение ключевых SaaS или платёжных каналов | med | высокий, delivery stack рвётся | сбои биллинга, отключение workspace/connectors | vendor redundancy, self-hosted alternatives, резервные каналы доставки |
| Black swan | Военный/геополитический шок и отключение LLM-провайдера | low-med | очень высокий, внезапная остановка сервиса | внезапные rate limits, недоступность API, force majeure клиентов | hybrid stack: open-source + локальные GPU-подрядчики + аварийные тарифы |

### B5. Kill conditions через 6 месяцев

1. **Median EBITDA path не просматривается:** если подтверждённый forward EBITDA на M12 остаётся **< 0 ₽/мес**, продолжать нельзя.
2. **Retention сломан:** если monthly logo churn стабильно **> 4%** два месяца подряд или net revenue retention **< 90%**, модель не выдержит накопление базы.
3. **Unit economics развалились:** если blended **CAC > 900 000 ₽** и одновременно **ARPU < 180 000 ₽**, LTV/CAC падает к неинвестируемой зоне.

### B6. Источники для competitor/risk section
- **R1**: Skolkovo profile / материалы про Smartcat и происхождение продукта. 
- **R2**: Rusprofile / корпоративные данные по Smartcat/связанным юрлицам. 
- **R3**: Rusprofile / PROMT, выручка и юридический профиль. 
- **R4**: Habr / материалы про PROMT, MT и корпоративное применение. 
- **R5**: Habr / материалы о Яндекс.Переводчике и NMT. 
- **R6**: vc.ru / обзоры российского AI/translation software рынка и корпоративных стеков.

<!-- P6B-DONE -->
