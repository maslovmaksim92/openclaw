# SECTION A. PnL

## A1. Исходные допущения

- ARPA: **300 000 ₽ / клиент / мес**.
- COGS per client: **110 000 ₽ / клиент / мес**.
- Gross profit per client: **190 000 ₽ / клиент / мес**.
- Contribution margin: **63,3%**.
- Blended CAC: **3 341 000 ₽**.
- LTV (gross profit basis): **12 673 000 ₽**.
- Fixed costs run-rate: **5 964 600 ₽ / мес**.
- Team FOT fully-loaded: **5 176 600 ₽ / мес**.
- Страховые взносы: **~30% к ФОТ**, уже включены в fully-loaded FOT.
- НДС **20%** учитывается только при ОСНО и не включён в MRR ниже.
- Формула активной базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`.
- EBITDA в таблицах = `Gross profit - Fixed costs`.

Сценарии:
- **Base**: churn **1,5% / мес**, траектория active clients к M12 = **0, 0, 0, 1, 2, 3, 5, 7, 10, 14, 18, 22**.
- **Optimistic**: churn **1,0% / мес**, траектория active clients к M12 = **0, 0, 1, 2, 4, 6, 9, 13, 18, 24, 30, 37**.
- **Pessimistic**: churn **2,5% / мес**, траектория active clients к M12 = **0, 0, 0, 1, 1, 2, 3, 5, 7, 10, 13, 16**.

## A2. 12-month PnL, Base scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,02 | 1,03 | 2,04 | 2,08 | 3,11 | 4,15 | 4,21 | 4,27 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 2,00 | 3,00 | 5,00 | 7,00 | 10,00 | 14,00 | 18,00 | 22,00 |
| MRR, ₽ | 0 | 0 | 0 | 300 000 | 600 000 | 900 000 | 1 500 000 | 2 100 000 | 3 000 000 | 4 200 000 | 5 400 000 | 6 600 000 |
| COGS, ₽ | 0 | 0 | 0 | 110 000 | 220 000 | 330 000 | 550 000 | 770 000 | 1 100 000 | 1 540 000 | 1 980 000 | 2 420 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 190 000 | 380 000 | 570 000 | 950 000 | 1 330 000 | 1 900 000 | 2 660 000 | 3 420 000 | 4 180 000 |
| GM% | 0,0% | 0,0% | 0,0% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% |
| Fixed costs, ₽ | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 |
| EBITDA, ₽ | -5 964 600 | -5 964 600 | -5 964 600 | -5 774 600 | -5 584 600 | -5 394 600 | -5 014 600 | -4 634 600 | -4 064 600 | -3 304 600 | -2 544 600 | -1 784 600 |
| Cash burn, ₽ | 5 964 600 | 5 964 600 | 5 964 600 | 5 774 600 | 5 584 600 | 5 394 600 | 5 014 600 | 4 634 600 | 4 064 600 | 3 304 600 | 2 544 600 | 1 784 600 |
| Cumulative cash, ₽ | -5 964 600 | -11 929 200 | -17 893 800 | -23 668 400 | -29 253 000 | -34 647 600 | -39 662 200 | -44 296 800 | -48 361 400 | -51 666 000 | -54 210 600 | -55 995 200 |

**Base break-even:**
- Break-even client count: **32 клиента по EBITDA**, **35 клиентов с запасом**.
- Break-even month: **вне M1-M12**, ориентир **M15** при сохранении late-year темпа.
- startup_capital_to_bep_rub: **57 312 814 ₽**.

## A3. 12-month PnL, Optimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0,00 | 0,00 | 1,00 | 1,01 | 2,02 | 2,04 | 3,06 | 4,09 | 5,13 | 6,18 | 6,24 | 7,30 |
| Total clients | 0,00 | 0,00 | 1,00 | 2,00 | 4,00 | 6,00 | 9,00 | 13,00 | 18,00 | 24,00 | 30,00 | 37,00 |
| MRR, ₽ | 0 | 0 | 300 000 | 600 000 | 1 200 000 | 1 800 000 | 2 700 000 | 3 900 000 | 5 400 000 | 7 200 000 | 9 000 000 | 11 100 000 |
| COGS, ₽ | 0 | 0 | 110 000 | 220 000 | 440 000 | 660 000 | 990 000 | 1 430 000 | 1 980 000 | 2 640 000 | 3 300 000 | 4 070 000 |
| Gross profit, ₽ | 0 | 0 | 190 000 | 380 000 | 760 000 | 1 140 000 | 1 710 000 | 2 470 000 | 3 420 000 | 4 560 000 | 5 700 000 | 7 030 000 |
| GM% | 0,0% | 0,0% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% |
| Fixed costs, ₽ | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 |
| EBITDA, ₽ | -5 964 600 | -5 964 600 | -5 774 600 | -5 584 600 | -5 204 600 | -4 824 600 | -4 254 600 | -3 494 600 | -2 544 600 | -1 404 600 | -264 600 | 1 065 400 |
| Cash burn, ₽ | 5 964 600 | 5 964 600 | 5 774 600 | 5 584 600 | 5 204 600 | 4 824 600 | 4 254 600 | 3 494 600 | 2 544 600 | 1 404 600 | 264 600 | 0 |
| Cumulative cash, ₽ | -5 964 600 | -11 929 200 | -17 703 800 | -23 288 400 | -28 493 000 | -33 317 600 | -37 572 200 | -41 066 800 | -43 611 400 | -45 016 000 | -45 280 600 | -44 215 200 |

**Optimistic break-even:**
- Break-even client count: **32 клиента по EBITDA**, **35 клиентов с запасом**.
- Break-even month: **M12**.
- startup_capital_to_bep_rub: **45 280 600 ₽**.

## A4. 12-month PnL, Pessimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0,00 | 0,00 | 0,00 | 1,00 | 0,03 | 1,02 | 1,05 | 2,08 | 2,12 | 3,17 | 3,25 | 3,33 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,00 | 2,00 | 3,00 | 5,00 | 7,00 | 10,00 | 13,00 | 16,00 |
| MRR, ₽ | 0 | 0 | 0 | 300 000 | 300 000 | 600 000 | 900 000 | 1 500 000 | 2 100 000 | 3 000 000 | 3 900 000 | 4 800 000 |
| COGS, ₽ | 0 | 0 | 0 | 110 000 | 110 000 | 220 000 | 330 000 | 550 000 | 770 000 | 1 100 000 | 1 430 000 | 1 760 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 190 000 | 190 000 | 380 000 | 570 000 | 950 000 | 1 330 000 | 1 900 000 | 2 470 000 | 3 040 000 |
| GM% | 0,0% | 0,0% | 0,0% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% |
| Fixed costs, ₽ | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 | 5 964 600 |
| EBITDA, ₽ | -5 964 600 | -5 964 600 | -5 964 600 | -5 774 600 | -5 774 600 | -5 584 600 | -5 394 600 | -5 014 600 | -4 634 600 | -4 064 600 | -3 494 600 | -2 924 600 |
| Cash burn, ₽ | 5 964 600 | 5 964 600 | 5 964 600 | 5 774 600 | 5 774 600 | 5 584 600 | 5 394 600 | 5 014 600 | 4 634 600 | 4 064 600 | 3 494 600 | 2 924 600 |
| Cumulative cash, ₽ | -5 964 600 | -11 929 200 | -17 893 800 | -23 668 400 | -29 443 000 | -35 027 600 | -40 422 200 | -45 436 800 | -50 071 400 | -54 136 000 | -57 630 600 | -60 555 200 |

**Pessimistic break-even:**
- Break-even client count: **32 клиента по EBITDA**, **35 клиентов с запасом**.
- Break-even month: **вне M1-M12**, ориентир **M18** при сохранении late-year темпа.
- startup_capital_to_bep_rub: **67 183 586 ₽**.

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### A5.1. На 1 активного клиента в месяц

| Метрика | ₽ / клиент / мес | Комментарий |
|---|---:|---|
| ARPA | 300 000 | месячная выручка без НДС |
| Gross profit | 190 000 | 300 000 - 110 000 COGS |
| Contribution | 190 000 | доп. variable SG&A поверх COGS в модели не выделяю |
| EBITDA at BE scale | 3 606 | при 32 клиентах EBITDA около нуля |
| Net, УСН 6% | -14 394 | налог 18 000 ₽ с выручки |
| Net, IT-льгота 3% | -5 394 | налог 9 000 ₽ с выручки |
| Net, ОСНО 20% | 2 885 | 20% на прибыль при положительном EBITDA |

### A5.2. Waterfall на M12 по сценариям

| Scenario | M12 clients | Gross profit, ₽ | EBITDA pre-tax, ₽ | Net, IT 3%, ₽ | Net, УСН 6%, ₽ | Net, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Base | 22 | 4 180 000 | -1 784 600 | -1 982 600 | -2 180 600 | -1 784 600 |
| Optimistic | 37 | 7 030 000 | 1 065 400 | 732 400 | 399 400 | 852 320 |
| Pessimistic | 16 | 3 040 000 | -2 924 600 | -3 068 600 | -3 212 600 | -2 924 600 |

## A6. Cash flow: startup_capital_to_bep_rub

- **Base:** **57 312 814 ₽**.
- **Optimistic:** **45 280 600 ₽**.
- **Pessimistic:** **67 183 586 ₽**.

## A7. Налоговая модель РФ

1. **УСН 6%**: налог = **6% от выручки**, даже если EBITDA низкая или отрицательная.
2. **IT-льгота / аккредитация Минцифры**: в модели использован режим **3% от выручки** как целевой льготный контур.
3. **ОСНО**: налог на прибыль **20%**, плюс **НДС 20%** в cash flow, если компания работает с VAT-контуром.
4. **Страховые взносы ~30% к ФОТ** уже зашиты в fully-loaded FOT и fixed costs, повторно не добавляются.

## A8. Break-even summary

| Scenario | Break-even client count | Break-even month | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Base | 32 EBITDA / 35 with buffer | 15 | 57 312 814 |
| Optimistic | 32 EBITDA / 35 with buffer | 12 | 45 280 600 |
| Pessimistic | 32 EBITDA / 35 with buffer | 18 | 67 183 586 |

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

База берётся из SECTION A: ARPA **300 000 ₽/мес**, COGS **110 000 ₽/мес**, fixed costs **5 964 600 ₽/мес**, M12 active clients ≈ **22**.

| Scenario | Что меняем | M12 clients | Gross profit, ₽/мес | EBITDA, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без изменений | 22.0 | 4 180 000 | **-1 784 600** | уже ниже EBITDA gate на M12 |
| Sens1 | **CAC x2** | 22.0 | 4 180 000 | **-3 121 000** | считаю, что fully-loaded acquisition spend растёт с 1.336 млн ₽ до 2.673 млн ₽/мес, EBITDA ухудшается на 1.336 млн ₽ |
| Sens2 | **Churn x2** (1.5% → 3.0%) | 21.2 | 4 019 625 | **-1 944 975** | при той же new-logo траектории база клиентов к M12 проседает с ~22.0 до ~21.2 |
| Sens3 | **Price -30%** (300k → 210k) | 22.0 | 2 200 000 | **-3 764 600** | strongest downside, т.к. gross profit на клиента падает с 190k до 100k |

**Вывод:** самая хрупкая переменная здесь не churn, а **pricing power**. Даже умеренный price compression ломает модель сильнее, чем удвоение churn. CAC inflation тоже опасен, потому что кейс и так держится на дорогом enterprise-sale.

## B2. Monte Carlo Lite, confidence intervals на M24

### B2.1. Inputs, triangular assumptions

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 2 500 000 | 3 341 000 | 6 000 000 | [T1][T2] + текущая модель CAC из 04-economics |
| Monthly churn, % | 1.0% | 1.5% | 3.0% | [T3] + stress-case из текущей модели |
| ARPU, ₽/мес | 250 000 | 300 000 | 350 000 | [T4][T5][T6] + enterprise WTP logic из 02-demand |
| Conversion lead→paid, % | 0.25% | 0.33% | 0.45% | mode = 0.40 wins / 120 target accounts из 04-economics; min/max = stress/uplift assumption |
| Time-to-hire, мес (среднее) | 1.0 | 1.6 | 2.5 | 04-economics hiring table |

### B2.2. Метод упрощённой симуляции

Вместо полного кода считаю **9 комбинаций** вокруг min/mode/max. M24 median anchor = **50 active clients**, потому что именно на этом уровне в 04-economics модель впервые даёт EBITDA около **3.54 млн ₽/мес**. Далее я двигаю M24 client base вверх/вниз по трём главным драйверам: conversion, churn и time-to-hire. Market-share и EBITDA значения ниже являются **оценкой-инференсом**, а не аудированной статистикой.

Ключевые реперные точки:
- **Worst** = CAC_max + Churn_max + ARPU_min + Conv_min + Hire_max → EBITDA@M24 ≈ **-4.27 млн ₽/мес**.
- **Median** = CAC_mode + Churn_mode + ARPU_mode + Conv_mode + Hire_mode → EBITDA@M24 ≈ **3.54 млн ₽/мес**.
- **Best** = CAC_min + Churn_min + ARPU_max + Conv_max + Hire_min → EBITDA@M24 ≈ **13.24 млн ₽/мес**.

### B2.3. Confidence interval table

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | **-4 270 000** | **3 540 000** | **13 240 000** | **17 510 000** |
| CAC payback, мес | **24.0** | **11.1** | **7.1** | **16.9** |
| LTV/CAC | **0.8x** | **3.8x** | **9.6x** | **8.8x** |
| Cash runway, мес | **13** | **20** | **30+** | **17+** |

### B2.4. Decision rules from Monte Carlo Lite

1. **p10 EBITDA < 0**: правило срабатывает, значит уже на downside-хвосте есть реальный риск неплатёжеспособности.
2. **p50 EBITDA > 500k ₽/мес**: формально median проходит gate, но запас не огромный, потому что это достигается только около **50 активных клиентов**.
3. **p90/p10 dispersion**: формально ratio бессмысленно интерпретировать из-за отрицательного p10, но сам факт перехода от **-4.27 млн** к **+13.24 млн** говорит о слишком широкой вилке исходов.
4. **LTV/CAC range width = 8.8x > 8**: правило хрупкости срабатывает. Модель чувствительна к pricing, churn и CAC одновременно.

**Итог Monte Carlo Lite:** кейс не фейлится автоматически по median, но выглядит **хрупким**. Для инвестрешения это скорее thesis на аккуратный staged rollout, а не на агрессивное масштабирование сразу.

## B3. Competitor deep-dive

### B3.1. Западные конкуренты

| Конкурент | Что умеет | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Harvey** | AI platform for legal and professional services | сильный бренд у top-tier law firms, enterprise security, широкая инсталляционная база (**100k+ professionals**, **1,000+ organizations**, **60+ AmLaw 100**) [T7] | ориентирован прежде всего на англоязычный legal workflow, слабая локализация под РФ, тяжёлый enterprise ticket | **15-20%** глобального AI-native legal/copilot сегмента, **<1% в РФ**. Это **инференс**, не публичная отчётность | Norm AI-подход лучше для **policy-as-code**, supervisory workflow и локальной regulatory adaptation |
| **Luminance** | contract intelligence, agentic legal workflows | сильная contract lifecycle automation, context-aware review, хорошая fit для enterprise CLM [T8] | более контрактный, чем compliance-native; слабее там, где нужен explicit regulatory rule layer | **8-12%** global legal AI / CLM-adjacent segment, **~0% в РФ**. **Инференс** | у Norm AI лучше позиционирование именно в **compliance determinations**, а не только в договорном контуре |
| **vLex Vincent AI** | legal research + workflow AI поверх глобальной базы права | мощная база правовых источников, cited answers, сильная research-side credibility [T9] | менее сфокусирован на internal policy workflows и supervisory review; санкционный и data residency барьер для РФ | **8-10%** AI legal research segment globally, **~0% в РФ**. **Инференс** | у Norm AI выше шанс продать value через **операционное соответствие**, а не через research-only use case |

### B3.2. Российские конкуренты

| Конкурент | Источник | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Yandex B2B Tech «Нейроюрист»** | vc.ru: продукт на базе Alice AI LLM, 20 free запросов, платные тарифы от **2 000 ₽/мес**, ~**50 пилотных партнёров**, 10k+ внутренних ответов [T10] | сильнейшая дистрибуция, собственный LLM-stack, нативная работа с российским правом | сейчас ближе к general legal assistant, чем к deep compliance workflow для банка/страховщика | **10-15%** раннего RU AI-legal assistant сегмента. **Инференс** | Norm AI сильнее там, где нужны **traceable determinations**, policy governance и approval workflow для regulated marketing/comms |
| **Doczilla / Doczilla Pro** | официальный сайт и отраслевые публикации: document automation + AI module, enterprise customers [T11][T12] | зрелый документный workflow, интеграции, узнаваемость в LegalTech РФ | core DNA всё ещё document automation, а не supervisory AI / compliance engine | **10-15%** broader RU legaltech automation, но лишь **5-8%** в узком AI-compliance сегменте. **Инференс** | Norm AI выигрывает, если buyer платит не за шаблоны документов, а за **снижение regulatory review load** |
| **Noroots** | vc.ru LegalTech обзор: проверка договоров прямо в Word, подсветка рисков и рекомендаций [T13] | простой и понятный wedge, быстрый ROI на contract review | продукт уже по описанию уже, чем enterprise compliance platform; риск быть feature, а не system-of-record | **3-5%** RU AI contract review microsegment. **Инференс** | Norm AI шире по use cases: disclosures, supervisory checks, DDQ/RFP, internal policy alignment |
| **Legiscan** | Habr Product Radar: AI для анализа и проверки договоров на риски [T14] | AI-native product, сфокусирован на понятной боли, low-friction trial potential | ранняя стадия, ограниченный brand trust для крупных regulated buyers | **1-3%** RU AI contract review segment. **Инференс** | у Norm AI лучше шанс зайти в enterprise, если будет private-cloud и explainability layer |
| **Комбинатор** | vc.ru LegalTech обзор: нейро-шаблоны, генерация типовых документов, интеграции с 1С / Bitrix24 / amoCRM [T13] | силён в документообороте и шаблонном drafting, понятен SMB/mid-market | слабый fit для сложного regulated approval workflow и supervisory oversight | **3-6%** RU document automation niche. **Инференс** | Norm AI сильнее в high-stakes compliance, а не в template generation |

### B3.3. Вывод по конкурентному полю

- **На Западе** рынок уже занят сильными legal-AI брендами, поэтому международная экспансия без выраженного regulatory wedge будет дорогой.
- **В РФ** конкуренты есть, но большинство закрывает либо **document automation**, либо **general legal assistant**. Меньше игроков, которые доказали enterprise-grade **compliance decisioning** в банках/страховании.
- Значит реальный шанс Norm AI в РФ, не mass-market legal copilot, а **дорогой compliance workflow layer для regulated enterprise**.

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | founder-heavy sales, зависимость от CEO в enterprise deals | high | high | >70% SQL держатся только на founder-led calls | нанять сильного AE, стандартизировать пресейл-материалы и security Q&A |
| 2 | Operational | качество rule-engine / LLM output недостаточно для compliance-grade workflow | med | high | pilot accuracy <90%, много ручных override | human-in-the-loop, evals на реальных кейсах, ограничить use cases до low-regret zones |
| 3 | Operational | зависимость от внешних LLM/API и latency/quality drift | high | high | рост ошибок, latency spikes, внезапные изменения цен/лимитов | multi-model routing, локальный fallback, private deployment option |
| 4 | Market | в РФ спрос остаётся education-led, а не budget-led | med | high | много встреч, мало paid pilots, цикл сделки >9 мес | продавать через конкретные KPI: TAT, FTE savings, approval SLA |
| 5 | Market | price compression из-за generalist AI и дешёвых legal copilots | high | high | клиенты сравнивают с 2-10 тыс. ₽/мес legal assistants | упаковать продукт как regulated workflow platform, а не чат-бот |
| 6 | Market | enterprise buyer выбирает локального incumbent с интеграциями | med | med | проигрыши на procurement stage из-за vendor trust/integration checklist | partnerships с SI/интеграторами, готовые коннекторы, on-prem/private cloud |
| 7 | Regulatory | 152-ФЗ и data residency ограничивают использование внешнего SaaS | high | high | security/compliance stop на этапе пилота | локальный контур, private-cloud, DPA и data-processing architecture под РФ |
| 8 | Regulatory | 115-ФЗ / отраслевые требования усложняют модель explainability и audit trail | med | high | комплаенс-клиент требует детальный traceability log, которого нет | decision logs, versioning policy, explainability-by-design |
| 9 | Financial | runway сжимается из-за медленного закрытия enterprise deals | high | high | cash <12 months runway до выхода на 15+ клиентов | staging of hiring, жёсткий burn control, raise раньше M9-M10 |
| 10 | Financial | курс USD и инфляция повышают cloud/API/FOT быстрее выручки | med | med | рост COGS >15% и pressure на зарплаты | рублёвое ценообразование с indexation, vendor diversification |
| 11 | Black swan | новый пакет санкций режет доступ к западным SaaS / моделям | med | high | поставщик ограничивает billing, API или регион | заранее подготовить Russian-hosted stack и alternate vendors |
| 12 | Black swan | резкое отключение ключевого LLM-провайдера или запрет модели | low/med | high | официальный notice от vendor, падение SLA | abstraction layer, open-source fallback, critical workflows без single-model dependency |

## B5. Kill conditions через 6 месяцев

1. **EBITDA downside kill:** если обновлённый p10 по EBITDA на горизонте 24 месяцев всё ещё **< 0**, а runway при этом **< 12 мес**, продолжать нельзя.
2. **Median economics kill:** если через 6 месяцев модель показывает **p50 EBITDA < 500 000 ₽/мес** на M24 или **LTV/CAC < 3.0x**, кейс не проходит economic gate.
3. **GTM reality kill:** если через 6 месяцев меньше **3 paid clients** или меньше **8 активных enterprise pilots**, а blended CAC уже ушёл выше **4.5 млн ₽**, значит рынок не конвертируется в оплачиваемый спрос.

## B6. Final critic view

Norm AI в РФ выглядит не как broad legaltech ставка, а как **узкая enterprise compliance infrastructure bet**. Upside есть, если продукт продаётся в private-cloud формате и доказывает measurable reduction of compliance workload. Но SECTION B показывает, что модель **очень чувствительна** к pricing, CAC и execution. Это не "плохой" кейс, а **хрупкий**.

### Sources for SECTION B
- [T1] 04-economics.md, fully-loaded CAC model inside this case.
- [T2] 04-economics.md, hiring and burn assumptions inside this case.
- [T3] SaaS Capital churn benchmarks: https://www.saas-capital.com/blog-posts/2025-saas-performance-metrics-benchmarks/
- [T4] VComply pricing: https://www.v-comply.com/pricing/
- [T5] ComplyCloud pricing: https://www.complycloud.com/pricing/
- [T6] Sengol pricing: https://www.sengol.ai/products/compliance/pricing
- [T7] Harvey official site: https://www.harvey.ai/
- [T8] Luminance official site: https://www.luminance.com/contract-intelligence/
- [T9] vLex Vincent AI official site: https://vlex.com/vincent-ai
- [T10] vc.ru about Yandex B2B Tech legal AI assistant: https://vc.ru/ai/2608476-yandex-b2b-tech-neuroyurist
- [T11] Doczilla official site: https://doczilla.ru/
- [T12] Doczilla company / industry coverage: https://dsmedia.pro/company/doczilla
- [T13] vc.ru overview of Russian LegalTech tools: https://vc.ru/legal/2169379-legaltech-v-rossii-avtomatizatsiya-yuristov
- [T14] Habr Product Radar, Legiscan: https://habr.com/ru/companies/productradar/articles/986632/

<!-- P6B-DONE -->
