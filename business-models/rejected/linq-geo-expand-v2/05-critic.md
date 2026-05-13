## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA: **600 000 ₽/клиент/мес**.
- CAC по каналам: founder-led outbound/SDR **987 000 ₽**, inbound/content **536 000 ₽**, partners/integrators/events **852 000 ₽**, blended **873 600 ₽**.
- LTV/mo: **439 800 ₽/клиент/мес** (21,99 млн ₽ LTV при churn 2,0%/мес, то есть около 50 месяцев implied lifetime).
- Contribution margin: **420 000 ₽/клиент/мес**.
- Fixed costs: **6 900 000 ₽/мес**, включая team FOT **6 162 000 ₽/мес**.
- COGS per client: **160 000 ₽/клиент/мес**.
- Сценарии заданы через new clients и monthly churn. Формула базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`.
- Cash burn = `max(0, -EBITDA)`. Cumulative cash показывает накопленную потребность в капитале, стартуя с 0 ₽.

### A2. Base scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 1,00 | 1,98 | 2,94 | 4,88 | 6,78 | 8,65 | 10,48 | 12,27 | 14,02 | 15,74 | 17,43 | 19,08 |
| MRR, ₽ | 600 000 | 1 188 000 | 1 764 240 | 2 928 955 | 4 070 376 | 5 188 969 | 6 285 189 | 7 359 485 | 8 412 296 | 9 444 050 | 10 455 169 | 11 446 065 |
| COGS, ₽ | 160 000 | 316 800 | 470 464 | 781 055 | 1 085 434 | 1 383 725 | 1 676 050 | 1 962 529 | 2 243 279 | 2 518 413 | 2 788 045 | 3 052 284 |
| Gross profit, ₽ | 440 000 | 871 200 | 1 293 776 | 2 147 900 | 2 984 942 | 3 805 244 | 4 609 139 | 5 396 956 | 6 169 017 | 6 925 637 | 7 667 124 | 8 393 781 |
| GM% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% |
| Fixed costs, ₽ | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 |
| EBITDA, ₽ | -6 460 000 | -6 028 800 | -5 606 224 | -4 752 100 | -3 915 058 | -3 094 756 | -2 290 861 | -1 503 044 | -730 983 | 25 637 | 767 124 | 1 493 781 |
| Cash burn, ₽ | 6 460 000 | 6 028 800 | 5 606 224 | 4 752 100 | 3 915 058 | 3 094 756 | 2 290 861 | 1 503 044 | 730 983 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 460 000 | -12 488 800 | -18 095 024 | -22 847 124 | -26 762 181 | -29 856 937 | -32 147 799 | -33 650 843 | -34 381 826 | -34 381 826 | -34 381 826 | -34 381 826 |

- Break-even по client count, contribution basis: **17 клиентов**.
- Break-even по client count, gross-profit basis: **16 клиентов**.
- Break-even month: **M11**.
- startup_capital_to_bep_rub: **34 381 826 ₽**.

### A2. Optimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 1,00 | 1,98 | 3,96 | 5,90 | 7,81 | 10,69 | 13,53 | 16,33 | 19,08 | 21,80 | 24,47 | 27,10 |
| MRR, ₽ | 600 000 | 1 191 000 | 2 373 135 | 3 537 538 | 4 684 475 | 6 414 208 | 8 117 995 | 9 796 225 | 11 449 281 | 13 077 542 | 14 681 379 | 16 261 158 |
| COGS, ₽ | 160 000 | 317 600 | 632 836 | 943 343 | 1 249 193 | 1 710 455 | 2 164 799 | 2 612 327 | 3 053 142 | 3 487 345 | 3 915 034 | 4 336 309 |
| Gross profit, ₽ | 440 000 | 873 400 | 1 740 299 | 2 594 195 | 3 435 282 | 4 703 752 | 5 953 196 | 7 183 898 | 8 396 140 | 9 590 198 | 10 766 345 | 11 924 849 |
| GM% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% |
| Fixed costs, ₽ | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 |
| EBITDA, ₽ | -6 460 000 | -6 026 600 | -5 159 701 | -4 305 805 | -3 464 718 | -2 196 248 | -946 804 | 283 898 | 1 496 140 | 2 690 198 | 3 866 345 | 5 024 849 |
| Cash burn, ₽ | 6 460 000 | 6 026 600 | 5 159 701 | 4 305 805 | 3 464 718 | 2 196 248 | 946 804 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 460 000 | -12 486 600 | -17 646 301 | -21 952 106 | -25 416 825 | -27 613 073 | -28 559 876 | -28 559 876 | -28 559 876 | -28 559 876 | -28 559 876 | -28 559 876 |

- Break-even по client count, contribution basis: **17 клиентов**.
- Break-even по client count, gross-profit basis: **16 клиентов**.
- Break-even month: **M9**.
- startup_capital_to_bep_rub: **28 559 876 ₽**.

### A2. Pessimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 2 | 2 |
| Total clients | 0,00 | 1,00 | 1,97 | 2,91 | 3,82 | 4,71 | 5,57 | 6,40 | 7,21 | 8,99 | 10,72 | 12,40 |
| MRR, ₽ | 0 | 600 000 | 1 182 000 | 1 746 540 | 2 294 144 | 2 825 319 | 3 340 560 | 3 840 343 | 4 325 133 | 5 395 379 | 6 433 517 | 7 440 512 |
| COGS, ₽ | 0 | 160 000 | 315 200 | 465 744 | 611 772 | 753 419 | 890 816 | 1 024 091 | 1 153 369 | 1 438 768 | 1 715 605 | 1 984 137 |
| Gross profit, ₽ | 0 | 440 000 | 866 800 | 1 280 796 | 1 682 372 | 2 071 901 | 2 449 744 | 2 816 252 | 3 171 764 | 3 956 611 | 4 717 913 | 5 456 375 |
| GM% | 0,0% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% | 73,3% |
| Fixed costs, ₽ | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 | 6 900 000 |
| EBITDA, ₽ | -6 900 000 | -6 460 000 | -6 033 200 | -5 619 204 | -5 217 628 | -4 828 099 | -4 450 256 | -4 083 748 | -3 728 236 | -2 943 389 | -2 182 087 | -1 443 625 |
| Cash burn, ₽ | 6 900 000 | 6 460 000 | 6 033 200 | 5 619 204 | 5 217 628 | 4 828 099 | 4 450 256 | 4 083 748 | 3 728 236 | 2 943 389 | 2 182 087 | 1 443 625 |
| Cumulative cash, ₽ | -6 900 000 | -13 360 000 | -19 393 200 | -25 012 404 | -30 230 032 | -35 058 131 | -39 508 387 | -43 592 135 | -47 320 371 | -50 263 760 | -52 445 847 | -53 889 472 |

- Break-even по client count, contribution basis: **17 клиентов**.
- Break-even по client count, gross-profit basis: **16 клиентов**.
- Break-even month: **не достигнут**.
- startup_capital_to_bep_rub: **53 889 472 ₽**.

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 600 000 | recurring выручка |
| Gross profit | 440 000 | ARPA - COGS |
| Contribution profit | 420 000 | gross profit - variable service reserve 20 000 ₽ |
| EBITDA contribution | 420 000 | до fixed costs; company break-even при 17 клиентах |
| Net after tax, УСН 6% | 384 000 | налог 6% с выручки |
| Net after tax, IT-льгота 3% | 402 000 | при аккредитации Минцифры и соблюдении доли профильной выручки |
| Net after tax, ОСНО 20% | 336 000 | приближённо 20% на прибыль до налога; НДС ниже отдельно |

### A6. Cash flow и startup_capital_to_bep_rub
- Base: **34 381 826 ₽** до выхода в положительный monthly EBITDA, break-even month **M10** по EBITDA и **M11** по client count contribution-basis.
- Optimistic: **28 559 876 ₽**, break-even month **M8** по EBITDA и **M9** по client count contribution-basis.
- Pessimistic: **53 889 472 ₽** в пределах горизонта M1-M12, но BEP за 12 месяцев **не достигается**; потребность уже выше стартового капитала **45 000 000 ₽**.

### A7. Налоговая модель РФ
- **УСН 6%**: налог берётся с выручки. Для текущей unit-модели это эквивалентно **36 000 ₽ налога на клиента в месяц** при ARPA 600 000 ₽.
- **IT-льгота 3%**: возможна при аккредитации Минцифры и выполнении критериев по профильной выручке. Налоговая нагрузка падает до **18 000 ₽ на клиента в месяц**, что даёт +18 000 ₽ к post-tax unit economics против УСН 6%.
- **Страховые взносы ~30% к ФОТ**: в модели считаю уже включёнными в FOT **6 162 000 ₽/мес** и fixed costs **6 900 000 ₽/мес**.
- **ОСНО / налог на прибыль 20%**: на уровне unit economics приближённо даёт post-tax contribution **336 000 ₽/клиент/мес**.
- **НДС 20%**: если компания на ОСНО и продаёт цену **сверху к тарифу**, EBITDA до налога почти не меняется, но ухудшается конверсия и cash collection. Если цена рынком воспринимается как **всё-включено**, то 600 000 ₽ нужно делить на 1,20, и тогда реальная net revenue падает до **500 000 ₽ без НДС**, что резко ухудшает маржу.

### A8. Break-even summary по сценариям
| Сценарий | New clients pattern | Churn / мес | Break-even clients | Break-even month | Clients at M12 | EBITDA at M12, ₽ |
|---|---|---:|---:|---|---:|---:|
| Base | 1,1,1,2,2,2,2,2,2,2,2,2 | 2,0% | 17 | M11 | 19,08 | 1 493 781 |
| Optimistic | 1,1,2,2,2,3,3,3,3,3,3,3 | 1,5% | 17 | M9 | 27,10 | 5 024 849 |
| Pessimistic | 0,1,1,1,1,1,1,1,1,2,2,2 | 3,0% | 17 | не достигнут | 12,40 | -1 443 625 |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База берёт M12 из SECTION A. Для чувствительности меняю по одному драйверу, остальные оставляю без изменений.

| Сценарий | Допущение | Клиенты @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | базовые допущения | 19.08 | 1 493 781 | проходит EBITDA gate |
| Sens1 | CAC x2 | 19.08 | -253 419 | при удвоении fully-loaded CAC добавочный acquisition burn ≈ 1.75 млн ₽/мес съедает прибыль |
| Sens2 | Churn x2 | 17.37 | 742 319 | бизнес остаётся живым, но запас прочности резко сужается |
| Sens3 | Price -30% | 19.08 | -1 940 038 | это главный single-point failure, значит pricing power критичен |

**Вывод:** для Linq опаснее всего не churn сам по себе, а потеря enterprise pricing. CAC-shock тоже переводит модель ниже нуля, если sales motion перестаёт быть дисциплинированным.

### B2. Monte Carlo Lite: confidence intervals

#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 536 000 | 873 600 | 1 200 000 | inbound CAC, blended CAC и stress-buffer поверх founder-led CAC [T5][T6] |
| Monthly churn, % | 1.5% | 2.0% | 4.0% | optimistic/base/stress from P6A + benchmark proxy [T4][T6] |
| ARPU, ₽/мес | 420 000 | 600 000 | 780 000 | price shock -30%, base, enterprise upsell +30% [T1][T6] |
| Conversion lead→paid, % | 0.8% | 1.14% | 2.08% | base blended funnel и нижняя/верхняя границы по каналам [T5] |
| Time-to-hire, мес | 1.0 | 1.6 | 2.5 | усреднение по team table и hiring realism [T5] |

#### Методика
Вместо полной 1000-run симуляции использую 9-комбинационный Monte Carlo Lite. Новые клиенты/мес масштабируются от базовых 2.0 через conversion, CAC и time-to-hire; retention через churn; EBITDA @M24 считается на полном fixed-cost run-rate 6.9 млн ₽/мес. Это приближённая оценка диапазона, а не бухгалтерский forecast.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -4 250 000 | 10 010 000 | 20 650 000 | 24 900 000 |
| CAC payback, мес | 4.6 | 2.0 | 1.2 | 3.4 |
| LTV/CAC | 5.4 | 25.2 | 41.0 | 35.6 |
| Cash runway, мес | 6.5 | 23.7 | 31.6 | 25.1 |

#### Интерпретация правил
- **Rule 1 triggered:** p10 EBITDA < 0, значит kill criterion #1 активируется, если плохая комбинация churn/CAC/pricing реализуется.
- **Rule 2 not triggered:** p50 EBITDA заметно выше 500 тыс. ₽/мес, то есть median-case инвестиционно ещё держится.
- **Rule 3 triggered де-факто:** при отрицательном p10 разброс хуже, чем формальный порог 10x, поэтому score нужно даунгрейдить за хрупкость распределения.
- **Rule 4 triggered:** range width по LTV/CAC = 35.6, это намного выше порога 8, значит модель очень чувствительна к pricing, churn и acquisition discipline.

**Итог Monte Carlo Lite:** median-case хороший, но левый хвост слишком тяжёлый. Для фонда это не “compounder”, а high-variance enterprise infra bet.

### B3. Competitor deep-dive

#### Западные конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Twilio | глобальная CPaaS-инфраструктура, сильный API-first стек, крупная customer base и channel breadth, сильный enterprise proof [T7][T8] | дорогой и сложный стек, слабая локальная пригодность под РФ-контур, санкционный и billing risk | **18-22% global CPaaS / omnichannel infra**; оценка-инференс по масштабу выручки и customer footprint [T7][T8] | Linq может продавать не сырой API, а готовый managed orchestration layer с локальными интеграциями и SLA |
| Infobip | сильный omnichannel, enterprise-grade routing, международное покрытие каналов и telecom-grade delivery [T9] | продукт тяжёлый для mid-market, меньше developer mindshare, чем у Twilio | **10-15% global tier-1 CPaaS / messaging orchestration**; inference по глобальному coverage и enterprise focus [T9] | Linq может быть быстрее в кастомизации под конкретные workflows и вертикали РФ/CIS |
| Intercom | сильный AI-first support UX, зрелый support workflow, хороший proof по AI automation [T10] | меньше глубины в raw messaging infra и voice stack, сильнее заточен под support frontend, чем под channel abstraction | **6-9% AI-first support messaging layer**; inference по customer-story scale и category position [T10] | Linq глубже в инфраструктуре каналов, webhooks, routing и enterprise-managed rollout |

#### Российские конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Chat2Desk | сильный local fit, реестр Минцифры, on-prem/enterprise варианты, 1 900+ клиентов, широкая сеть каналов [T11] | ближе к омниканальному helpdesk, чем к developer-grade infra; меньше product moat в orchestration | **12-18% российского омниканального customer-messaging SaaS**; inference от клиентской базы и заметности бренда [T11] | Linq может уйти выше по чеку за счёт AI-native routing, observability и complex integrations |
| Umnico | 5 000+ клиентов, сильный дистрибуционный охват в SMB/mid-market, хороший social-commerce fit, M&A signal от T2 [T12][T13][T14] | ниже enterprise-depth, слабее moat в сложном voice/SLA/integration контуре | **8-12% broad RU messaging aggregator layer**, но ниже в enterprise-инфраструктуре; inference [T12][T13] | Linq сильнее в enterprise reliability и в high-ACV use cases для банков, страховых и e-commerce |
| LiveTex | долгий бренд, реестр ПО РФ, зрелая чат-платформа, on-prem и CRM-интеграции [T15][T16] | legacy-perception, ниже developer extensibility, слабее AI-native positioning | **6-10% российского legacy omnichannel support stack**; inference [T15][T16] | Linq современнее как orchestration-core и лучше упаковывается в AI-agent stack |
| CraftTalk | AI/knowledge-base DNA, enterprise chatbot automation, Skolkovo signal, 350+ клиентов [T17][T18] | клиентская база меньше, чем у массовых агрегаторов; может проигрывать по breadth каналов и outbound distribution | **3-5% enterprise AI-contact-center niche**; inference [T17][T18] | Linq может выиграть как infra-layer под multiple channels, а не только как AI-contact-center overlay |

#### Вывод по конкурентам
- Внизу рынка Linq будет раздавлен по цене Chat2Desk, Umnico и LiveTex.
- На глобальном верхнем рынке Linq не перебьёт Twilio/Infobip breadth-ом каналов.
- Рабочая ниша только одна: **enterprise managed messaging orchestration для сложных multi-channel flows, где нужен AI-layer + локальные интеграции + SLA + ownership результата**.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder-led sales не масштабируется в repeatable pipeline | med | high | <1 новый paid logo в месяц 2 месяца подряд | раньше нанять AE/SE, стандартизировать discovery/pilot playbook |
| 2 | Operational | Интеграции по каналам и CRM ломаются при каждом кастомном rollout | med | high | рост backlog по incidents и SLA breaches | ограничить catalog интеграций, ввести certification и change-management |
| 3 | Operational | Зависимость от внешних LLM/API и routing vendors | high | high | рост latency/cost, ошибки у внешних API, деградация resolution rate | multi-vendor architecture, fallback models, локальные правила и кеши |
| 4 | Market | Спрос остаётся sales-led и не переходит в масштабируемый pipeline | med | high | низкий SQL volume, слабый inbound, длинные циклы >150 дней | фокус на 2-3 вертикалях и partner-led GTM |
| 5 | Market | Ценовая компрессия со стороны локальных helpdesk-игроков | high | high | скидки >20%, проигрыши deal'ов по цене | продавать outcome/SLA/интеграции, а не seat-based helpdesk |
| 6 | Market | Конкуренты добавляют AI-routing как фичу и стирают differentiator | med | high | релизы AI-bot/orchestration у Chat2Desk, CraftTalk, LiveTex | ускорить depth в analytics, observability и workflow ownership |
| 7 | Regulatory | 152-ФЗ и data residency ограничат хранение логов и message history | med | high | security/legal objections на pre-sale, требования on-prem | RU-hosting, selective retention, on-prem/private deployment |
| 8 | Regulatory | 115-ФЗ/комплаенс в finance требует audit trail и explainability | med | med | банки требуют дополнительные controls и протоколы | встроить audit logging, role model, traceability по ответам и routing |
| 9 | Regulatory | Санкции на SaaS/каналы/облачные компоненты рвут critical stack | high | high | отказ billing, ограничение API, блокировки provider accounts | vendor diversification, локальные аналоги, резервные каналы доставки |
| 10 | Financial | Cash runway сжимается из-за долгого пилота и delayed collections | med | high | DSO >75 дней, burn >4 млн ₽/мес | upfront setup fee, milestone invoicing, жёсткий cash control |
| 11 | Financial | Ослабление рубля поднимает стоимость импортных API и infra | high | med | USD/RUB скачок, рост cloud/telecom invoice | валютный буфер, пересмотр pricing, частичная рублёвая индексация |
| 12 | Financial | Инфляция зарплат в senior engineering и sales | med | med | offer decline rate, рост replacement cost | ESOP/bonus mix, selective outsourcing, tighter hiring plan |
| 13 | Black swan | Резкое ужесточение санкций или войны бьёт по enterprise IT-бюджетам | med | high | freeze новых ИТ-проектов у банков/retail | фокус на cost-saving ROI и mission-critical support flows |
| 14 | Black swan | Отключение ключевого LLM или messaging provider | med | very high | внезапная недоступность API, force-majeure notices | локальный fallback, provider redundancy, degraded-mode operations |

### B5. Kill conditions через 6 месяцев
1. **Median EBITDA path сломан:** если rolling forecast на M12 показывает EBITDA < 0 или p10 EBITDA@M24 остаётся ниже нуля после двух циклов коррекции.
2. **Pipeline не materializes:** если к концу M6 меньше **6 активных пилотов** или меньше **3 платящих enterprise-клиентов**.
3. **Unit economics деградировали:** если blended CAC > **1.3 млн ₽**, logo churn > **4%/мес** или фактический ARPU < **450 тыс. ₽/мес**.

### B6. Final critic verdict
Linq остаётся **проходимым**, но только как узкая ставка на enterprise orchestration. SECTION B ухудшает профиль кейса по risk-adjusted quality: median economics хорошие, однако downside слишком тяжёлый, а pricing power является ключевым условием выживания. Для IC это скорее **selective bet with strict kill-switches**, а не широкий scalable SaaS.

### Sources for SECTION B
- [T6] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/linq-geo-expand-v2/05-critic.md
- [T7] Twilio customer stories / scale proof: https://www.twilio.com/en-us/customers
- [T8] Twilio pricing: https://www.twilio.com/en-us/pricing/current-rates
- [T9] Infobip company / product footprint: https://www.infobip.com/company
- [T10] Intercom customer stories: https://www.intercom.com/customers
- [T11] Chat2Desk official site: https://chat2desk.com/
- [T12] Umnico official site: https://umnico.com/ru/
- [T13] vc.ru, T2 купил Umnico: https://vc.ru/id4994551/2673476-t2-kupil-platformu-umnico-dlya-obshcheniya-s-klientami
- [T14] Habr Career, Umnico: https://career.habr.com/companies/umnico
- [T15] LiveTex official site: https://livetex.ru/
- [T16] Habr, LiveTex profile: https://habr.com/ru/users/LiveTex/
- [T17] CraftTalk official site: https://crafttalk.ru/
- [T18] Skolkovo, CraftTalk + Авантелеком: https://sk.ru/news/rezident-skolkovo-crafttalk-i-avantelekom-zapustili-sovmestnuyu-omnikanalnuyu-ii-platformu/

<!-- P6B-DONE -->
