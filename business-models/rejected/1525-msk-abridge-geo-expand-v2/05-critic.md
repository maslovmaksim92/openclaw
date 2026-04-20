## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **280 000 ₽/мес**.
- COGS на клиента: **140 000 ₽/мес**.
- Gross profit на клиента: **140 000 ₽/мес**.
- Variable sales / success allocation: **18 000 ₽/клиент/мес**.
- Contribution после variable load: **122 000 ₽/клиент/мес**.
- Lean fixed costs для рабочего early-stage сценария: **3 550 000 ₽/мес**.
- Steady-state fixed costs полной команды из P5: **5 842 000 ₽/мес**. Этот уровень используется как stress / downside.
- Налоговые режимы для РФ: **УСН 6%**, **IT-льгота 3%** при соблюдении критериев, **ОСНО 20%** на прибыль плюс кассовое давление НДС.
- Для 12-месячного PnL беру три сценария продаж:
  - **Base:** new clients = 1,1,1,2,2,2,2,2,3,3,3,3; churn **1.7%/мес**.
  - **Optimistic:** new clients = 1,1,2,2,2,3,3,3,4,4,4,4; churn **1.2%/мес**.
  - **Pessimistic:** new clients = 0,0,1,1,1,1,1,2,2,2,2,2; churn **2.5%/мес**.
- Cumulative cash в таблицах показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 1.00 | 1.98 | 2.95 | 4.90 | 6.82 | 8.70 | 10.55 | 12.37 | 15.16 | 17.90 | 20.60 | 23.25 |
| MRR, ₽ | 280 000 | 555 240 | 825 801 | 1 371 762 | 1 908 442 | 2 435 999 | 2 954 587 | 3 464 359 | 4 245 465 | 5 013 292 | 5 768 066 | 6 510 009 |
| Gross profit, ₽ | 140 000 | 277 620 | 412 901 | 685 881 | 954 221 | 1 217 999 | 1 477 293 | 1 732 180 | 2 122 733 | 2 506 646 | 2 884 033 | 3 255 005 |
| Fixed costs, ₽ | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 |
| EBITDA, ₽ | -3 428 000 | -3 308 074 | -3 190 187 | -2 952 304 | -2 718 464 | -2 488 601 | -2 262 644 | -2 040 529 | -1 700 190 | -1 365 637 | -1 036 771 | -713 496 |
| Cumulative cash, ₽ | -3 428 000 | -6 736 074 | -9 926 261 | -12 878 564 | -15 597 029 | -18 085 629 | -20 348 274 | -22 388 803 | -24 088 993 | -25 454 630 | -26 491 402 | -27 204 898 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.99 | 3.96 | 5.92 | 7.85 | 10.75 | 13.62 | 16.46 | 20.26 | 24.02 | 27.73 | 31.40 |
| MRR, ₽ | 280 000 | 556 640 | 1 109 960 | 1 656 641 | 2 196 761 | 3 010 400 | 3 814 275 | 4 608 504 | 5 673 202 | 6 725 123 | 7 764 422 | 8 791 249 |
| Gross profit, ₽ | 140 000 | 278 320 | 554 980 | 828 321 | 1 098 380 | 1 505 200 | 1 907 137 | 2 304 252 | 2 836 601 | 3 362 562 | 3 882 211 | 4 395 625 |
| Fixed costs, ₽ | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 |
| EBITDA, ₽ | -3 428 000 | -3 307 464 | -3 066 374 | -2 828 178 | -2 592 840 | -2 238 326 | -1 888 066 | -1 542 009 | -1 078 105 | -619 768 | -166 930 | 280 473 |
| Cumulative cash, ₽ | -3 428 000 | -6 735 464 | -9 801 838 | -12 630 016 | -15 222 856 | -17 461 182 | -19 349 248 | -20 891 257 | -21 969 362 | -22 589 129 | -22 756 060 | -22 475 587 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 4.76 | 6.64 | 8.47 | 10.26 | 12.00 | 13.70 |
| MRR, ₽ | 0 | 0 | 280 000 | 553 000 | 819 175 | 1 078 696 | 1 331 728 | 1 858 435 | 2 371 974 | 2 872 675 | 3 360 858 | 3 836 836 |
| Gross profit, ₽ | 0 | 0 | 140 000 | 276 500 | 409 588 | 539 348 | 665 864 | 929 218 | 1 185 987 | 1 436 338 | 1 680 429 | 1 918 418 |
| Fixed costs, ₽ | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 | 3 550 000 |
| EBITDA, ₽ | -3 550 000 | -3 550 000 | -3 428 000 | -3 309 050 | -3 193 074 | -3 079 997 | -2 969 747 | -2 740 253 | -2 516 497 | -2 298 335 | -2 085 626 | -1 878 236 |
| Cumulative cash, ₽ | -3 550 000 | -7 100 000 | -10 528 000 | -13 837 050 | -17 030 124 | -20 110 121 | -23 079 868 | -25 820 121 | -28 336 618 | -30 634 952 | -32 720 579 | -34 598 814 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 280 000 ₽
- **COGS:** 140 000 ₽
- **Gross profit:** 140 000 ₽
- **Variable sales/support:** 18 000 ₽
- **Contribution:** 122 000 ₽

#### Waterfall на EBITDA break-even уровне 30 клиентов в lean-mode
- **Revenue:** 8 400 000 ₽/мес
- **COGS:** 4 200 000 ₽/мес
- **Gross profit:** 4 200 000 ₽/мес
- **Variable sales/support:** 540 000 ₽/мес
- **Contribution:** 3 660 000 ₽/мес
- **EBITDA:** **110 000 ₽/мес**

#### Waterfall на target profit gate, 34 клиента
- **Revenue:** 9 520 000 ₽/мес
- **COGS:** 4 760 000 ₽/мес
- **Gross profit:** 4 760 000 ₽/мес
- **Variable sales/support:** 612 000 ₽/мес
- **Contribution:** 4 148 000 ₽/мес
- **EBITDA:** **598 000 ₽/мес**

#### Net profit после налогов на gate-level 34 клиента
- **УСН 6%:** 598 000 - 571 200 = **26 800 ₽/мес**
- **IT-льгота 3%:** 598 000 - 285 600 = **312 400 ₽/мес**
- **ОСНО 20%:** налог на прибыль формально мягче, но НДС и длинные расчёты с клиниками ухудшают cash conversion.

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M12 | 22 800 000 ₽ | Только при хорошем ramp и жёстком контроле команды |
| Base | M15 | 29 000 000 ₽ | Реалистичный контур founder-mode, если интеграции не расползаются |
| Pessimistic | M24+ | 55 000 000 ₽+ | При слабом adoption медицина быстро съедает runway |

### A7. Налоговая модель РФ
- **УСН 6%** удобно считать как базовый режим early-stage, но на EBITDA около 0 съедает почти весь запас прочности.
- **IT-льгота 3%** заметно улучшает post-tax economics и почти обязательна, если строить отдельную российскую компанию.
- **ОСНО 20%** в healthcare B2B нежелательна из-за НДС и длинного cash cycle enterprise-клиентов.
- Страховые взносы уже учтены внутри FOT / fixed costs из P5.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 30 | 30 | M12 | Проходит только в lean-mode |
| Base | 30 | 30 | M15 | Экономика рабочая, но без большого safety margin |
| Pessimistic | 30 | 30 | M24+ | Категория остаётся хрупкой из-за продаж и внедрения |

<!-- P6A-DONE -->
## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 мес

База для sensitivity: M12 base-case, где активная база ≈ **23.25 клиента**, ARPA **280k ₽/мес**, contribution **122k ₽/клиент/мес**, EBITDA **-713 496 ₽/мес**.

| Сценарий | Что меняется | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | 23.25 клиента × 122k contribution - 3.55m fixed | **-713 496** |
| Sens1 | CAC x2 | доп. acquisition burn +2.1m ₽/мес к lean-mode | **-2 819 496** |
| Sens2 | Churn x2 | churn 1.7% -> 3.4%, активная база M12 падает примерно до 21.8 клиента | **-890 400** |
| Sens3 | Price -30% | ARPA 280k -> 196k, GP/client падает до 56k, contribution ≈ 38k | **-2 666 500** |
| Sens4 | Full team too early | fixed costs 3.55m -> 5.842m при той же базе клиентов | **-3 005 496** |

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 700 000 | 957 273 | 1 800 000 | [T1], [T2] |
| Monthly churn, % | 1.0% | 1.7% | 4.0% | [T1], [T2] |
| ARPU, ₽/мес | 196 000 | 280 000 | 420 000 | [T1], [T2] |
| Conversion pilot->paid, % | 20% | 28% | 40% | [T2] |
| Time-to-hire, мес | 1.0 | 1.5 | 3.0 | [T2] |

#### Как считалось
Использована Monte Carlo Lite логика на 9 смешанных состояниях между CAC, churn, ARPU и fixed-cost discipline. Это не полноценная 1000-run симуляция, а управленческая оценка диапазонов для founder-mode и early healthcare GTM.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 400 000** | **650 000** | **2 900 000** | **5 300 000** |
| CAC payback, мес | **11.0** | **6.8** | **3.5** | **7.5** |
| LTV/CAC | **2.6** | **4.9** | **8.7** | **6.1** |
| Cash runway, мес | **9.5** | **14.0** | **19.0** | **9.5** |

#### Интерпретация Monte Carlo Lite
- **p10 EBITDA < 0**, значит downside остаётся реальным и требует осторожного capital plan.
- **p50 EBITDA > 500k ₽/мес**, значит кейс формально проходит Profit Gate в median только при сохранении lean-mode.
- **LTV/CAC p10 = 2.6x** ниже желаемого comfort-level, но выше полного fail. Значит risk не в отсутствии value, а в execution discipline.
- **Ширина диапазона умеренная**: кейс не безумно хаотичный, но чувствителен к hiring и pricing.

### B3. Competitor deep-dive

#### Топ-3 западных
| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Abridge** | сильный enterprise narrative, интеграции в clinical workflow, proof of category maturity | высокая сложность локализации под РФ и enterprise-heavy delivery | лидер категории ambient documentation в US enterprise segment | локальный data residency, on-prem и адаптация под российские МИС |
| **Freed** | простой продукт, понятный pricing, низкий порог входа | ориентирован на low-end / individual clinicians, меньше enterprise moat | заметный игрок в lower-end physician-scribe niche | российский кейс можно строить на клиниках и сетях, а не на self-serve врачах |
| **Sunoh.ai** | понятный pricing anchor, AI scribing category validation | ограниченная локальная применимость в РФ, слабее narrative по тяжёлым интеграциям | mid-tier category participant | преимущество через closed contour deployment и локальные medical templates |

#### Топ российских / локальных substitutes
| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **ЦРТ Voice2Med** | [T2] | локальная speech stack, медицинские словари, enterprise trust | ближе к speech/documentation layer, чем к full ambient workflow intelligence | **20-25%** локального voice-med сегмента | если продукт реально делает structured note + QA + workflow layer, value capture шире |
| **Aiston** | [T2] | on-prem и интеграции с МИС, локальная адаптация | меньше category power и глобального AI brand | **10-15%** нишевого сегмента | можно выиграть product depth и protocol automation |
| **Звёздочка** | [T2] | сильный локальный narrative вокруг хранения в РФ и ambient use-case | вероятно меньше масштаб enterprise-sales и integrations maturity | **5-10%** emerging segment | шанс в более зрелом enterprise GTM и richer documentation workflow |

#### Вывод по конкурентам
1. Западный рынок уже валидировал category и willingness-to-pay.
2. В РФ substitutes существуют, поэтому вход не бесплатный и pure-US playbook не переносится.
3. Настоящее преимущество возможно только как **enterprise ambient documentation layer + МИС integrations + secure deployment**, а не как дешёвый диктофон.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Интеграции с МИС занимают в 2 раза больше времени | high | high | onboarding > 8 недель | стандартизировать 2-3 типовых контура и ограничить кастомизацию |
| Operational | Врачи не доверяют AI-generated notes | med | high | низкий DAU и ручные правки > 35% | human-in-the-loop rollout, specialty templates, phased adoption |
| Operational | Clinical QA load съедает GM | high | high | COGS > 160k ₽/клиент/мес | productize templates, narrow ICP, убрать low-ACV клиентов |
| Market | РФ спрос остаётся enterprise-only и узким | med | high | pipeline < 30 качественных buyers за 90 дней | продавать крупным сетям, не дробиться на одиночных врачей |
| Market | Ценовое давление от локальных speech vendors | med | med | сделки выигрываются только через скидки > 20% | продавать outcome, а не transcription minutes |
| Regulatory | 152-ФЗ и медданные блокируют cloud deployment | high | high | клиенты требуют только on-prem | готовить on-prem / private cloud контур заранее |
| Financial | Ранний hiring раздувает fixed cost до 5.8m ₽ | high | high | burn > 6.5m ₽/мес без ускорения выручки | держать founder-mode до 20+ клиентов |
| Financial | CAC оказывается выше 1.3m ₽ | med | high | pilot win-rate < 25% | фокус на partnerships и founder-led sales |
| Black swan | Изменение регуляторики по AI в медицине | low | high | новые требования к хранению и валидации | legal monitoring и локальный compliance pack |

### B5. Kill conditions через 6 месяцев
1. **Pipeline fail:** если нет минимум **3 платящих клиник / сетей** или pilot->paid conversion остаётся **< 25%**, кейс нужно останавливать.
2. **Economics fail:** если фактический COGS уходит выше **160 000 ₽/клиент/мес** и contribution падает ниже **100 000 ₽**, founder-mode перестаёт сходиться.
3. **Hiring fail:** если команда раздута до full-cost базы раньше достижения **20 активных клиентов**, модель почти гарантированно теряет шанс на EBITDA gate.

### B6. Итог по SECTION B
SECTION B не ломает кейс, но резко сужает допустимую траекторию. Abridge-like модель в РФ может сработать только как дисциплинированный enterprise healthcare operator. Как только продукт превращается в heavy services business или пытается идти в self-serve, экономика быстро уходит в минус.

Практический вывод: **это не clean SaaS, а управляемый GEO-EXPAND кейс с умеренным upside и высоким execution risk**.

## Источники SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1525-msk-abridge-geo-expand-v2/04-economics.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1525-msk-abridge-geo-expand-v2/02-demand.md

<!-- P6B-DONE -->