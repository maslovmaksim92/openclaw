## SECTION A. PnL 12 месяцев, cash flow и break-even

### A1. Принятые допущения для 3 сценариев

- **Base:** ARPA 700 000 ₽, COGS 180 000 ₽/клиент/мес, contribution 520 000 ₽/клиент/мес, normalized CAC 1 790 000 ₽, core fixed costs 7 405 000 ₽/мес.
- **Optimistic:** ARPA 750 000 ₽, COGS 170 000 ₽/клиент/мес, contribution 580 000 ₽/клиент/мес, CAC 1 500 000 ₽, core fixed costs 7 000 000 ₽/мес.
- **Pessimistic:** ARPA 650 000 ₽, COGS 190 000 ₽/клиент/мес, contribution 460 000 ₽/клиент/мес, CAC 2 300 000 ₽, core fixed costs 7 800 000 ₽/мес.
- **Методика PnL:**
  - MRR = Total clients × ARPA.
  - COGS = Total clients × COGS per client.
  - Gross profit = MRR - COGS.
  - Fixed costs = core fixed costs + CAC × New clients.
  - EBITDA = Gross profit - Fixed costs.
  - Cash burn = max(0, -EBITDA).
  - Cumulative cash = накопленный burn от старта, без учёта привлечённого капитала.

### A2. PnL, Base scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 |
| MRR, ₽ | 0 | 0 | 0 | 700 000 | 1 400 000 | 2 800 000 | 4 200 000 | 5 600 000 | 7 000 000 | 8 400 000 | 9 800 000 | 11 200 000 |
| COGS, ₽ | 0 | 0 | 0 | 180 000 | 360 000 | 720 000 | 1 080 000 | 1 440 000 | 1 800 000 | 2 160 000 | 2 520 000 | 2 880 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 520 000 | 1 040 000 | 2 080 000 | 3 120 000 | 4 160 000 | 5 200 000 | 6 240 000 | 7 280 000 | 8 320 000 |
| GM% | 0% | 0% | 0% | 74,3% | 74,3% | 74,3% | 74,3% | 74,3% | 74,3% | 74,3% | 74,3% | 74,3% |
| Fixed costs, ₽ | 7 405 000 | 7 405 000 | 7 405 000 | 9 195 000 | 9 195 000 | 10 985 000 | 10 985 000 | 10 985 000 | 10 985 000 | 10 985 000 | 10 985 000 | 10 985 000 |
| EBITDA, ₽ | -7 405 000 | -7 405 000 | -7 405 000 | -8 675 000 | -8 155 000 | -8 905 000 | -7 865 000 | -6 825 000 | -5 785 000 | -4 745 000 | -3 705 000 | -2 665 000 |
| Cash burn, ₽ | 7 405 000 | 7 405 000 | 7 405 000 | 8 675 000 | 8 155 000 | 8 905 000 | 7 865 000 | 6 825 000 | 5 785 000 | 4 745 000 | 3 705 000 | 2 665 000 |
| Cumulative cash, ₽ | 7 405 000 | 14 810 000 | 22 215 000 | 30 890 000 | 39 045 000 | 47 950 000 | 55 815 000 | 62 640 000 | 68 425 000 | 73 170 000 | 76 875 000 | 79 540 000 |

### A3. PnL, Optimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 12 | 15 | 18 | 21 | 24 |
| MRR, ₽ | 0 | 0 | 750 000 | 1 500 000 | 3 000 000 | 4 500 000 | 6 750 000 | 9 000 000 | 11 250 000 | 13 500 000 | 15 750 000 | 18 000 000 |
| COGS, ₽ | 0 | 0 | 170 000 | 340 000 | 680 000 | 1 020 000 | 1 530 000 | 2 040 000 | 2 550 000 | 3 060 000 | 3 570 000 | 4 080 000 |
| Gross profit, ₽ | 0 | 0 | 580 000 | 1 160 000 | 2 320 000 | 3 480 000 | 5 220 000 | 6 960 000 | 8 700 000 | 10 440 000 | 12 180 000 | 13 920 000 |
| GM% | 0% | 0% | 77,3% | 77,3% | 77,3% | 77,3% | 77,3% | 77,3% | 77,3% | 77,3% | 77,3% | 77,3% |
| Fixed costs, ₽ | 7 000 000 | 7 000 000 | 8 500 000 | 8 500 000 | 10 000 000 | 10 000 000 | 11 500 000 | 11 500 000 | 11 500 000 | 11 500 000 | 11 500 000 | 11 500 000 |
| EBITDA, ₽ | -7 000 000 | -7 000 000 | -7 920 000 | -7 340 000 | -7 680 000 | -6 520 000 | -6 280 000 | -4 540 000 | -2 800 000 | -1 060 000 | 680 000 | 2 420 000 |
| Cash burn, ₽ | 7 000 000 | 7 000 000 | 7 920 000 | 7 340 000 | 7 680 000 | 6 520 000 | 6 280 000 | 4 540 000 | 2 800 000 | 1 060 000 | 0 | 0 |
| Cumulative cash, ₽ | 7 000 000 | 14 000 000 | 21 920 000 | 29 260 000 | 36 940 000 | 43 460 000 | 49 740 000 | 54 280 000 | 57 080 000 | 58 140 000 | 58 140 000 | 58 140 000 |

### A4. PnL, Pessimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 650 000 | 1 300 000 | 1 950 000 | 2 600 000 | 3 250 000 | 3 900 000 | 4 550 000 | 5 200 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 190 000 | 380 000 | 570 000 | 760 000 | 950 000 | 1 140 000 | 1 330 000 | 1 520 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 460 000 | 920 000 | 1 380 000 | 1 840 000 | 2 300 000 | 2 760 000 | 3 220 000 | 3 680 000 |
| GM% | 0% | 0% | 0% | 0% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% |
| Fixed costs, ₽ | 7 800 000 | 7 800 000 | 7 800 000 | 7 800 000 | 10 100 000 | 10 100 000 | 10 100 000 | 10 100 000 | 10 100 000 | 10 100 000 | 10 100 000 | 10 100 000 |
| EBITDA, ₽ | -7 800 000 | -7 800 000 | -7 800 000 | -7 800 000 | -9 640 000 | -9 180 000 | -8 720 000 | -8 260 000 | -7 800 000 | -7 340 000 | -6 880 000 | -6 420 000 |
| Cash burn, ₽ | 7 800 000 | 7 800 000 | 7 800 000 | 7 800 000 | 9 640 000 | 9 180 000 | 8 720 000 | 8 260 000 | 7 800 000 | 7 340 000 | 6 880 000 | 6 420 000 |
| Cumulative cash, ₽ | 7 800 000 | 15 600 000 | 23 400 000 | 31 200 000 | 40 840 000 | 50 020 000 | 58 740 000 | 67 000 000 | 74 800 000 | 82 140 000 | 89 020 000 | 95 440 000 |

### A5. Waterfall: ARPA → Gross → Contribution → EBITDA → Net

#### Base, на 1 клиента в steady-state
- ARPA: **700 000 ₽**
- Gross profit: **520 000 ₽** = 700 000 - 180 000
- Contribution: **520 000 ₽**
- EBITDA после core fixed на клиентах break-even: **≈ 26 333 ₽/клиент** при 15 клиентах
- Net after tax:
  - **УСН 6%:** 478 000 ₽ на клиента-месяц до аллокации fixed, формула 700 000 - 180 000 - 42 000
  - **IT-льгота 3%:** 499 000 ₽ на клиента-месяц до аллокации fixed
  - **ОСНО 20%:** 416 000 ₽ на клиента-месяц до аллокации fixed, без учёта эффекта вычета входного НДС

#### Optimistic, на 1 клиента в steady-state
- ARPA: **750 000 ₽**
- Gross profit: **580 000 ₽**
- Contribution: **580 000 ₽**
- EBITDA после core fixed на клиентах break-even: **≈ 41 538 ₽/клиент** при 13 клиентах
- Net after tax:
  - **IT-льгота 3%:** 557 500 ₽
  - **УСН 6%:** 535 000 ₽
  - **ОСНО 20%:** 430 000 ₽

#### Pessimistic, на 1 клиента в steady-state
- ARPA: **650 000 ₽**
- Gross profit: **460 000 ₽**
- Contribution: **460 000 ₽**
- EBITDA после core fixed на клиентах break-even: **≈ 1 176 ₽/клиент** при 17 клиентах
- Net after tax:
  - **ОСНО 20%:** 330 000 ₽
  - **УСН 6%:** 421 000 ₽
  - **IT-льгота 3%:** 440 500 ₽

### A6. Cash flow и startup_capital_to_bep_rub

| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | **58 140 000 ₽** | запас капитала нужен до выхода в плюс на 21 клиенте |
| Base | > M12 | **79 540 000 ₽** | в горизонте 12 месяцев EBITDA ещё отрицательная, нужен капитал на 13-14 месяцев |
| Pessimistic | > M12 | **95 440 000 ₽** | без корректировки cost base или роста ARPA модель остаётся burn-heavy |

### A7. Налоговая модель РФ

- **УСН 6%:** простой режим для ранней стадии, налог считается с выручки. Для base-case это **42 000 ₽ налога на клиента в месяц**.
- **IT-льгота / аккредитация Минцифры:** целевой режим для software/AI-компании, в модели закладываю **3% с выручки** как лучший сценарий по cash efficiency.
- **ОСНО 20%:** консервативный стресс-сценарий. При применимости появляется **НДС 20%**, что ухудшает cash conversion и усложняет продажи, если клиент не нейтрален к входному НДС.
- **Страховые взносы:** в модели учтены как **~30% к ФОТ** и уже сидят в fixed cost base из 04-economics.
- Практический вывод: для RapidClaims критично как можно раньше идти в **IT-аккредитацию**, иначе tax drag и VAT friction заметно давят на burn.

### A8. Break-even по client count и по месяцам

| Scenario | Contribution per client/month, ₽ | Core fixed costs, ₽/мес | Break-even client count | Break-even month |
|---|---:|---:|---:|---:|
| Optimistic | 580 000 | 7 000 000 | **13** | **M11** |
| Base | 520 000 | 7 405 000 | **15** | **за пределами M12**, ориентир M13-M14 |
| Pessimistic | 460 000 | 7 800 000 | **17** | **за пределами M12** |

**Вывод по SECTION A:** кейс экономически живой только при enterprise ARPA, tight control CAC и предпочтительно налоговом режиме IT-льготы. Base-case требует почти 80 млн ₽ капитала до операционного break-even, optimistic-case делает модель фондируемой, pessimistic-case требует пересборки go-to-market или цены.

<!-- P6A-DONE -->

## SECTION B. Finance Risk, Monte Carlo Lite и competitor deep-dive

### B1. Sensitivity analysis, EBITDA через 12 месяцев

База для расчёта: M12 из SECTION A, base-case = 16 клиентов, contribution = 520 000 ₽/клиент/мес, fixed core = 7 405 000 ₽/мес, new clients в M12 = 2.

| Сценарий | Что меняется | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | **-2 665 000** | — | даже базовый план ещё burn-heavy на 12-м месяце |
| Sens1 | CAC ×2 | **-6 245 000** | -3 580 000 | GTM становится почти нефондируемым без снижения fixed base |
| Sens2 | Churn ×2, до 5%/мес | **-4 002 302** | -1 337 302 | erosion активной базы заметно ухудшает M12 EBITDA |
| Sens3 | Price -30% | **-6 025 000** | -3 360 000 | pricing compression почти так же опасен, как удвоение CAC |

**Вывод:** главный downside не один, а двойной, pricing pressure и дорогой CAC ломают экономику быстрее, чем churn alone. Для кейса это означает, что без узкого enterprise ICP и жёсткого ROI-sales motion модель быстро уходит в глубокий burn.

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 1 500 000 | 1 790 000 | 2 300 000 | [T4] |
| Monthly churn, % | 1,1% | 2,5% | 5,0% | [T1][T4] |
| ARPU, ₽/мес | 650 000 | 700 000 | 750 000 | [T3][T4] |
| Conversion rate lead→paid, % | 8% | 10% | 14% | [T4] |
| Time-to-hire, мес | 0,8 | 1,5 | 2,8 | [T4] |

Метод: вместо полноценной 1000-итерационной симуляции использую упрощённый Monte Carlo Lite из 9 комбинаций. Якоря p10/p50/p90 задаю как worst / median(mode-mode-mode) / best, а 6 mixed-case использую для sanity-check диапазона. Conversion и time-to-hire folded в темп новых платящих клиентов и штраф к runway через более длинный период burn.

#### 9 комбинаций для sanity-check

| Комбинация | CAC | Churn | ARPU | Conversion | Time-to-hire | EBITDA @M24, ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Worst | 2 300 000 | 5,0% | 650 000 | 8% | 2,8 | -4 112 509 |
| Mixed 1 | 2 300 000 | 2,5% | 650 000 | 10% | 2,0 | -484 514 |
| Mixed 2 | 1 790 000 | 5,0% | 650 000 | 8% | 2,0 | -3 326 709 |
| Mixed 3 | 2 300 000 | 5,0% | 700 000 | 8% | 2,8 | -3 432 818 |
| Median | 1 790 000 | 2,5% | 700 000 | 10% | 1,5 | 1 442 497 |
| Mixed 4 | 1 500 000 | 5,0% | 700 000 | 10% | 1,2 | -591 173 |
| Mixed 5 | 1 790 000 | 2,5% | 750 000 | 10% | 1,5 | 2 535 357 |
| Mixed 6 | 1 500 000 | 1,1% | 700 000 | 14% | 0,8 | 8 591 268 |
| Best | 1 500 000 | 1,1% | 750 000 | 14% | 0,8 | 10 371 679 |

#### Confidence intervals

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | **-4 112 509** | **1 442 497** | **10 371 679** | **14 484 188** |
| CAC payback, мес | **4,9** | **3,4** | **2,6** | **2,3** |
| LTV/CAC | **4,1** | **11,6** | **34,5** | **30,4** |
| Cash runway, мес | **11,5** | **20,9** | **37,3** | **25,8** |

#### Правила-интерпретации

1. **p10 EBITDA < 0, правило срабатывает.** В downside-контуре кейс может уйти в риск неплатёжеспособности до выхода на устойчивую положительную EBITDA.
2. **p50 EBITDA > 500 тыс. ₽/мес, median-gate проходит.** Median-case инвестиционно живой, но не комфортный.
3. **Диапазон неопределённости экстремальный.** Формально отношение p90/p10 некорректно из-за отрицательного p10, но знак flip сам по себе хуже порога 10x и означает необходимость даунгрейда score за volatility.
4. **Range width по LTV/CAC = 30,4 > 8.** Модель хрупкая, в первую очередь к нестабильности pricing, churn и CAC.

**Итог Monte Carlo Lite:** кейс не разваливается в median-case, но downside-ветка слишком тяжёлая, чтобы считать его low-risk enterprise expansion. Для инвесткомитета это скорее conditional pass only при наличии подтверждённого pilot ROI, а не paper thesis.

### B3. Competitor deep-dive

Сразу важно: в РФ почти нет чистых analogues autonomous medical coding по американскому образцу. Поэтому ниже и прямые конкуренты, и ближайшие substitutes. Оценки долей рынка, это мои inference по узкому сегменту AI-слоя над medical coding / clinical documentation / RCM, а не по всему medtech рынку.

#### Top-3 западных

| Игрок | Почему в топе | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **CodaMetrix** [T5] | AI-native autonomous coding для крупных provider-сетей | сильный category fit, глубокий focus на coding automation, enterprise workflow, заметный бренд в US provider market | тяжёлый enterprise deployment, длинный цикл сделки, американская reimbursement-логика плохо переносится в РФ | **2-4%** мирового узкого AI-native coding сегмента | RapidClaims шире по RCM narrative, не только coding, но и denial prevention / scrub / CDI |
| **Fathom** [T6] | ambient clinical documentation и physician workflow automation | сильный product velocity, хороший user love, lower-friction wedge через documentation | меньше прямого фокуса на reimbursement / denials / enterprise billing economics | **1-3%** adjacent ambient documentation сегмента в enterprise/mid-market healthcare | RapidClaims продаёт CFO-grade ROI, а не только physician productivity |
| **Solventum / 3M HIS** [T7] | incumbent с огромной installed base в coding / CDI / clinical documentation | доверие больших hospital systems, distribution, compliance maturity, доступ к existing workflows | legacy baggage, slower product cycles, выше риск дорогого и тяжёлого stack'а | **8-12%** broad enterprise coding/CDI stack в развитых рынках | RapidClaims может выиграть speed, AI-first automation rate и более ясный ROI-story для greenfield deployment |

#### Топ российских и локальных substitutes

| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Webiomed / К-Скай** [T8] | Skolkovo | сильная локальная регуляторная адаптация, доступ к клиническим данным, узнаваемость в AI для медицины РФ | core focus больше на clinical decision support и risk analytics, чем на revenue cycle и coding | **12-18%** в узком сегменте AI-over-clinical-workflow у крупных ЛПУ РФ | RapidClaims ближе к деньгам клиента, продаёт сокращение denial / coding cost / A/R days, а не только clinical insight |
| **iAmbulance / iVan** [T9] | Skolkovo | сильный wedge в voice capture, ambient documentation и меддоках, локальный язык и on-prem contour | documentation-first, а не full RCM/coding stack; сложнее доказать CFO-ROI | **4-7%** в сегменте AI-меддокументации и ambient capture | RapidClaims сильнее в back-office monetization и billing outcomes |
| **Medico Mind** [T10] | vc.ru | понятная упаковка AI-ассистента для клиник, близость к частным клиникам и customer support workflows | ближе к front-office/операционному AI, слабее moat в enterprise billing / coding | **2-4%** в частных клиниках по AI-automation tooling | RapidClaims заходит сверху через revenue leakage и unit economics, а не через service assistant layer |
| **K2 NeuroTech / K2Тех** [T11] | Habr | сильная enterprise-интеграция, доступ к крупным заказчикам, доверие по безопасному внедрению AI | чаще выступает как интегратор/проектный слой, а не как repeatable product company | **3-6%** AI-интеграционных проектов в мед и adjacent regulated verticals | RapidClaims может быть productized layer с лучшей валовой маржой и repeatability, если удержит стандартный rollout |

#### Вывод по конкуренции

1. **На Западе конкуренция сильная и category-aware.** Против CodaMetrix и 3M невозможно выигрывать «ещё одной моделью», нужно выигрывать workflow-level ROI.
2. **В РФ прямой pure-play competition слабее, но substitutes сильны.** Главные враги, это МИС + ручной процесс + интегратор + локальный AI-документооборот.
3. **Наш moat возможен только при связи с cash metrics.** Если продукт в РФ скатится в «AI для меддоков», он потеряет differentiation и уйдёт в low-multiple integrator zone.

### B4. Risk matrix

| Риск | Категория | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Невозможность быстро закрыть senior compliance + medical coding lead | Operational | med | high | >90 дней открыта ключевая вакансия, пилоты идут без доменной экспертизы | founder-led hiring, advisor bench, pre-signed contractor pool |
| LLM/OCR качество падает на русских меддоках и hand-written scans | Operational | med | high | доля manual override >25%, QA backlog растёт 2+ месяца | narrow specialty rollout, human-in-the-loop, benchmark set на локальных датасетах |
| Зависимость от внешнего LLM API или OCR-поставщика | Operational | high | high | рост latency/cost, ухудшение SLA, изменения в лицензии API | multi-vendor stack, fallback models, on-prem inference path |
| Спрос в РФ ограничится 10-20 реально платёжеспособными buyer'ами | Market | med | high | pipeline не конвертируется в 3+ пилота за 2 квартала | ужесточить ICP, идти через private chains и integrator channels |
| Конкуренты и substitutes запускают price compression | Market | high | high | win-rate падает, скидки >25% становятся нормой | pricing by ROI, modular packaging, outcome-based pilot economics |
| Buyer выбирает доработку МИС или аутсорс вместо нового AI-слоя | Market | med | med/high | воронка застревает на security/procurement, no-decision >40% | pilot with measured baseline, reference cases, lower-friction land-and-expand |
| Требования 152-ФЗ и data residency делают SaaS-модель непродаваемой | Regulatory | high | high | каждый второй enterprise требует on-prem/VPN-only контур | on-prem deployment, российские облака, segregated data architecture |
| 115-ФЗ / внутренний комплаенс клиента блокируют AI в документообороте и billing | Regulatory | med | med/high | compliance review >120 дней, юристы режут scope пилота | готовый compliance pack, DPA templates, audit logs, explainability layer |
| Санкции режут доступ к западному SaaS/LLM стеку | Regulatory | high | high | поставщик прекращает поддержку RU entities или billing | local hosting, OSS fallback, vendor redundancy, contract ring-fencing |
| Burn выше плана и runway падает ниже 9 месяцев | Financial | med | high | ежемесячный burn >7 млн ₽ 2 квартала подряд | freeze hiring, cut event spend, paid pilots before full rollout |
| Ослабление рубля удорожает LLM, GPU и secure infra | Financial | high | med/high | USD/RUB >100 и infra cost +20%+ | RUB-indexed contracts, price escalators, local compute mix |
| Налоговая и страховая нагрузка выше модели | Financial | med | med | не получена IT-аккредитация, effective tax rate >6% | early tax structuring, Минцифры accreditation roadmap |
| Новый санкционный виток или военная эскалация срывают закупки | Black swan | med | high | enterprise customers freeze capex/IT projects | focus on ROI-critical buyers, preserve 12+ month liquidity buffer |
| Отключение ключевого LLM/облачного провайдера на 2-6 недель | Black swan | med/high | high | провайдер вводит geoblock или SLA outage | offline queue, local model fallback, critical workflow degradation mode |

### B5. Kill conditions через 6 месяцев

1. **Runway-risk kill:** p10 EBITDA@M24 остаётся < 0 и фактический cash runway падает **ниже 9 месяцев** при burn >7 млн ₽/мес два месяца подряд.
2. **GTM kill:** после 6 месяцев нет минимум **2 оплаченных пилотов** или хотя бы **1 paid design partner** с доказанным ROI baseline, а blended CAC по первым сделкам уходит **выше 2,5 млн ₽**.
3. **Economics kill:** подтверждённый churn у ранних аккаунтов идёт **>5%/мес**, либо фактический ARPU опускается **ниже 550 тыс. ₽/мес**, либо median-case LTV/CAC падает **ниже 3x**.

### B6. Bottom line по SECTION B

RapidClaims остаётся интересным только как **high-ticket enterprise RCM play**. Median-case ещё проходит, но чувствительность к CAC и pricing слишком высокая, а Monte Carlo Lite показывает отрицательный p10 и слишком широкий разброс LTV/CAC. Это не reject по бумаге, но это кейс, где без жёсткой дисциплины по ICP, on-prem deployment и pilot ROI инвестиционный риск быстро становится непропорциональным.

## Sources, SECTION B
- [T5] CodaMetrix official website / autonomous coding positioning: https://www.codametrix.com/
- [T6] Fathom official website / ambient AI for healthcare: https://www.fathomhealth.com/
- [T7] Solventum official page / 3M health information systems and coding workflow positioning: https://www.solventum.com/en-us/health-information-technology/
- [T8] Skolkovo / Webiomed (К-Скай): https://navigator.sk.ru/orn/1123782
- [T9] Skolkovo / iAmbulance, iVan: https://navigator.sk.ru/orn/1129203
- [T10] vc.ru / Medico Mind: https://vc.ru/tribuna/1638576-medico-mind-i-novaya-era-obsluzhivaniya-v-chastnyh-klinikah
- [T11] Habr / K2 NeuroTech, AI в медицине и enterprise внедрениях: https://habr.com/ru/companies/k2tech/articles/845086/

<!-- P6B-DONE -->
