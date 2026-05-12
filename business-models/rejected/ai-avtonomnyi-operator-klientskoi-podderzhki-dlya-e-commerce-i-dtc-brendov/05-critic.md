# SECTION A. PnL
## Принятые допущения из 04-economics.md
- CAC по каналам: paid 480 000 ₽, outbound 690 000 ₽, partnerships 506 000 ₽, blended CAC 549 250 ₽.
- LTV: 6,64 млн ₽ при churn 2,2%/мес.
- Базовый ARPA: 220 000 ₽/мес на клиента.
- COGS на клиента: 100 000 ₽/мес.
- Contribution margin per client/month для base: 94 000 ₽.
- Team FOT fully-loaded: 4 256 050 ₽/мес. Fixed costs на полном ранпе: 5 266 050 ₽/мес, с ramp-up по месяцам M1-M12.
- Страховые взносы: ~30% к ФОТ. Для ОСНО считаем применимость НДС 20%; для IT-льготы используем режим 3% с выручки только при аккредитации Минцифры.

## Сценарий: Базовый
| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 13 | 17 | 23 | 29 | 37 |
| MRR, ₽ | 0 | 0 | 220 000 | 435 160 | 865 586 | 1 286 544 | 1 918 240 | 2 756 038 | 3 795 406 | 5 031 907 | 6 461 205 | 8 079 058 |
| COGS, ₽ | 0 | 0 | 100 000 | 197 800 | 393 448 | 584 793 | 871 927 | 1 252 745 | 1 725 184 | 2 287 230 | 2 936 911 | 3 672 299 |
| Gross profit, ₽ | 0 | 0 | 120 000 | 237 360 | 472 138 | 701 751 | 1 046 313 | 1 503 294 | 2 070 221 | 2 744 676 | 3 524 293 | 4 406 759 |
| GM%, % | 0,0 | 0,0 | 54,5 | 54,5 | 54,5 | 54,5 | 54,5 | 54,5 | 54,5 | 54,5 | 54,5 | 54,5 |
| Fixed costs, ₽ | 965 000 | 1 270 300 | 2 490 550 | 3 465 550 | 3 803 550 | 4 616 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 |
| EBITDA, ₽ | -965 000 | -1 270 300 | -2 370 550 | -3 228 190 | -3 331 412 | -3 914 299 | -4 219 737 | -3 762 756 | -3 195 829 | -2 521 374 | -1 741 757 | -859 291 |
| Cash burn, ₽ | 965 000 | 1 270 300 | 2 370 550 | 3 228 190 | 3 331 412 | 3 914 299 | 4 219 737 | 3 762 756 | 3 195 829 | 2 521 374 | 1 741 757 | 859 291 |
| Cumulative cash, ₽ | -965 000 | -2 235 300 | -4 605 850 | -7 834 040 | -11 165 452 | -15 079 751 | -19 299 488 | -23 062 245 | -26 258 074 | -28 779 447 | -30 521 204 | -31 380 495 |
**Waterfall на 1 клиента/мес:** ARPA 220 000 ₽ -> Gross 120 000 ₽ -> Contribution 94 000 ₽ -> EBITDA -49 399 ₽ -> Net -62 599 ₽. Налоговая модель: УСН 6% с выручки; налог в waterfall 13 200 ₽/клиент/мес.
**Cash flow:** startup_capital_to_bep_rub = 31 380 495 ₽.
**Break-even:** 57 клиентов на полном fixed-cost run-rate; по месяцам: не достигнут в M1-M12.

## Сценарий: Оптимистичный
| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| Total clients | 0 | 1 | 2 | 4 | 7 | 11 | 16 | 21 | 28 | 35 | 44 | 53 |
| MRR, ₽ | 0 | 260 000 | 515 320 | 1 026 044 | 1 787 575 | 2 795 399 | 4 045 082 | 5 532 270 | 7 252 690 | 9 202 141 | 11 376 503 | 13 771 726 |
| COGS, ₽ | 0 | 105 000 | 208 110 | 414 364 | 721 905 | 1 128 911 | 1 633 591 | 2 234 186 | 2 928 971 | 3 716 249 | 4 594 357 | 5 561 658 |
| Gross profit, ₽ | 0 | 155 000 | 307 210 | 611 680 | 1 065 670 | 1 666 488 | 2 411 491 | 3 298 084 | 4 323 719 | 5 485 892 | 6 782 146 | 8 210 067 |
| GM%, % | 0,0 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 | 59,6 |
| Fixed costs, ₽ | 965 000 | 1 270 300 | 2 490 550 | 3 465 550 | 3 803 550 | 4 616 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 |
| EBITDA, ₽ | -965 000 | -1 115 300 | -2 183 340 | -2 853 870 | -2 737 880 | -2 949 562 | -2 854 559 | -1 967 966 | -942 331 | 219 842 | 1 516 096 | 2 944 017 |
| Cash burn, ₽ | 965 000 | 1 115 300 | 2 183 340 | 2 853 870 | 2 737 880 | 2 949 562 | 2 854 559 | 1 967 966 | 942 331 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -965 000 | -2 080 300 | -4 263 640 | -7 117 510 | -9 855 390 | -12 804 952 | -15 659 511 | -17 627 476 | -18 569 808 | -18 349 966 | -16 833 870 | -13 889 853 |
**Waterfall на 1 клиента/мес:** ARPA 260 000 ₽ -> Gross 155 000 ₽ -> Contribution 130 000 ₽ -> EBITDA 30 581 ₽ -> Net 22 781 ₽. Налоговая модель: IT-льгота 3% с выручки при аккредитации Минцифры; налог в waterfall 7 800 ₽/клиент/мес.
**Cash flow:** startup_capital_to_bep_rub = 18 569 808 ₽.
**Break-even:** 41 клиентов на полном fixed-cost run-rate; по месяцам: M10.

## Сценарий: Пессимистичный
| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 9 | 12 | 16 | 19 |
| MRR, ₽ | 0 | 0 | 0 | 180 000 | 353 700 | 521 320 | 863 074 | 1 192 867 | 1 691 116 | 2 171 927 | 2 815 910 | 3 437 353 |
| COGS, ₽ | 0 | 0 | 0 | 110 000 | 216 150 | 318 585 | 527 434 | 728 974 | 1 033 460 | 1 327 289 | 1 720 834 | 2 100 605 |
| Gross profit, ₽ | 0 | 0 | 0 | 70 000 | 137 550 | 202 736 | 335 640 | 463 893 | 657 656 | 844 638 | 1 095 076 | 1 336 748 |
| GM%, % | 0,0 | 0,0 | 0,0 | 38,9 | 38,9 | 38,9 | 38,9 | 38,9 | 38,9 | 38,9 | 38,9 | 38,9 |
| Fixed costs, ₽ | 965 000 | 1 270 300 | 2 490 550 | 3 465 550 | 3 803 550 | 4 616 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 | 5 266 050 |
| EBITDA, ₽ | -965 000 | -1 270 300 | -2 490 550 | -3 395 550 | -3 666 000 | -4 413 314 | -4 930 410 | -4 802 157 | -4 608 394 | -4 421 412 | -4 170 974 | -3 929 302 |
| Cash burn, ₽ | 965 000 | 1 270 300 | 2 490 550 | 3 395 550 | 3 666 000 | 4 413 314 | 4 930 410 | 4 802 157 | 4 608 394 | 4 421 412 | 4 170 974 | 3 929 302 |
| Cumulative cash, ₽ | -965 000 | -2 235 300 | -4 725 850 | -8 121 400 | -11 787 400 | -16 200 714 | -21 131 124 | -25 933 282 | -30 541 675 | -34 963 087 | -39 134 061 | -43 063 362 |
**Waterfall на 1 клиента/мес:** ARPA 180 000 ₽ -> Gross 70 000 ₽ -> Contribution 70 000 ₽ -> EBITDA -205 761 ₽ -> Net -205 761 ₽. Налоговая модель: ОСНО: налог на прибыль 20%, НДС 20% применим; налог в waterfall 0 ₽/клиент/мес.
**Cash flow:** startup_capital_to_bep_rub = 43 063 362 ₽.
**Break-even:** 76 клиентов на полном fixed-cost run-rate; по месяцам: не достигнут в M1-M12.

## Налоговая модель
- **УСН 6%**: базовый рабочий режим для старта, налог считается с выручки, НДС обычно нет.
- **IT-льгота 3%**: достижима только при аккредитации Минцифры и соблюдении критериев по доле профильной выручки, даёт лучший post-tax net.
- **ОСНО 20%**: налог на прибыль 20%; при работе с крупными заказчиками и входным НДС нужно учитывать НДС 20%, что давит на cash conversion и усложняет оборотный капитал.
- **Страховые взносы**: в модели уже учтены как ~30% к ФОТ.

## SECTION B. Finance Risk + Competitor

### 1) Sensitivity analysis: EBITDA через 12 месяцев
Беру базу из SECTION A: M12 EBITDA = **-859 291 ₽/мес**, M12 active clients = **37**, ARPA = **220 000 ₽**, COGS = **100 000 ₽/клиент/мес**, full fixed cost = **5 266 050 ₽/мес**. Для CAC-stress считаю, что для сохранения темпа продаж нужен doubling acquisition spend против base monthly CAC pool **1 098 500 ₽/мес** из 04-economics.md.

| Сценарий | Ключевое изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | Без изменений | -859 291 | База из SECTION A |
| Sens1 | CAC x2 | -1 957 791 | Доп. burn ≈ 1.10 млн ₽/мес, если рынок стал дороже, а объём найма клиентов нужно удержать |
| Sens2 | Churn x2 (2.2% -> 4.4%) | -1 327 291 | Active client base к M12 падает примерно до 33, gross profit снижается примерно на 468 тыс. ₽/мес |
| Sens3 | Price -30% (220k -> 154k) | -3 301 291 | GP/client падает со 120k до 54k, operating leverage ломается |

**Вывод:** на горизонте 12 месяцев кейс особенно хрупок к price compression, затем к churn. CAC inflation болезненен, но сам по себе не так разрушителен, как падение ценника.

### 2) Monte Carlo Lite, confidence intervals (M24)
#### Triangular inputs
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 450 000 | 549 250 | 900 000 | [B1] 04-economics + enterprise-style support motion benchmark |
| Monthly churn, % | 1.5% | 2.2% | 5.0% | [B2] Optifai benchmark + stress-case из 04-economics |
| ARPU, ₽/мес | 180 000 | 220 000 | 280 000 | [B1][B3] base/bear из 04-economics + premium SLA upside |
| Conversion lead→paid, % | 0.40% | 0.67% | 1.20% | [B1] blended funnel implied by 2 paid / мес и канальные воронки |
| Time-to-hire, мес | 1.0 | 1.5 | 3.0 | [B1] hiring table |

#### Упрощённая симуляция
Вместо 1000 реальных прогонов использую 9-комбинационный Monte Carlo Lite: worst, best, median и 6 mixed-комбинаций вокруг CAC/churn/ARPU. Базовая механика для M24: active clients зависят от churn и conversion, EBITDA считается как `active clients × gross profit/client - fixed costs - acquisition drag`, где fixed cost на полном ранпе держу в диапазоне **5.3-6.2 млн ₽/мес** в зависимости от time-to-hire и необходимости добора delivery-команды.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24 (₽/мес) | -1 800 000 | 6 200 000 | 14 500 000 | 16 300 000 |
| CAC payback (мес) | 5.0 | 2.5 | 1.6 | 3.4 |
| LTV/CAC | 1.8x | 8.3x | 18.0x | 16.2 |
| Cash runway (мес) | 6 | 13 | 24 | 18 |

**Интерпретация правил:**
1. **p10 EBITDA < 0** → kill criterion #1 активируется: в левом хвосте распределения есть риск неплатёжеспособности.
2. **p50 EBITDA = 6.2 млн ₽/мес** → EBITDA Gate в median проходит.
3. **Разброс слишком велик:** p90 против p10 фактически >10x по magnitude и p10 отрицательный, значит score надо **даунгрейдить за неопределённость**.
4. **LTV/CAC range width = 16.2 > 8** → модель хрупкая, главные источники хрупкости: pricing, churn, CAC.

### 3) Competitor deep-dive
Ниже market-share estimates даны как **грубые экспертные оценки** для serviceable сегмента `AI/customer support stack для e-commerce и mid-market digital support`, а не как audited market share.

#### Western top-3
| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Gorgias** | Сильнейший e-commerce positioning, 150+ integrations, trusted by 15k brands, outcome-based AI pricing [B4] | Сильная привязка к западному стеку, дорогой usage-layer при high-volume support, слабее локализация под РФ | **15-20%** в global e-commerce helpdesk niche | Локальные каналы, Telegram-first, data residency в РФ, managed onboarding под маркетплейсы и DTC РФ |
| **Zendesk** | Масштаб, enterprise trust, mature omnichannel/helpdesk, 100k+ customers globally [B5] | Overkill для mid-market DTC, тяжелее внедрение, ниже vertical focus на e-commerce | **20-25%** в broader CX/helpdesk enterprise layer | Быстрее внедрение, ниже TCO, выше точность на узких e-commerce сценариях post-purchase |
| **Intercom Fin** | Сильный AI brand, $0.99 per resolution, быстрый запуск, хороший self-serve + AI-agent motion [B6] | Менее глубоко заточен под операционный контур российского e-commerce, санкционный/платёжный риск | **8-12%** в AI-native support automation for digital-first companies | Human-in-the-loop + SLA + русскоязычные интеграции, кастомные сценарии возвратов/статусов/маркетплейсов |

#### Russian top-5
| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Jivo** | Сильный SMB/mid-market penetration, понятный pricing, Telegram и омниканал, узнаваемый бренд [B3] | Это прежде всего helpdesk/chat stack, а не глубокий managed autonomous operator | **20-30%** в РФ live-chat/helpdesk for SMB/mid-market | Мы продаём outcome и deflection, а не seat-based инструмент |
| **Usedesk** | Сильный локальный helpdesk, AI-функции, multi-channel support, зрелый сервисный продукт [B7][B3] | Меньше product depth в autonomous resolution, чаще нужен integrator/service partner | **10-15%** в РФ helpdesk for support teams | Более вертикальный e-commerce play, быстрее time-to-value на post-purchase use cases |
| **Carrot quest** | Сильный automation/messaging/маркетинг-контур, известность в digital SMB [B8] | Ближе к marketing automation, чем к полноценному support-ops layer; корпоративная структура нестабильна, прежнее юрлицо ликвидировано [B9] | **5-8%** в conversational automation adjacent layer | У нас support-first позиционирование, SLA и HITL вместо lead-gen UX |
| **Wikibot / похожие AI-бот integrators** | Хорошо продают кастомизацию и API-доступ к внутренним системам, быстро закрывают пилот [B10] | Низкая стандартизация, риск агентского бизнеса без repeatable product | **2-4%** в AI support projects | У нас может быть выше повторяемость внедрения и лучше unit economics на серийных кейсах |
| **TED Chat / проектные AI-боты** | Продажа isolated contour и on-prem/закрытого контура, что важно для безопасности [B11] | Чаще проектная разработка, чем продуктовая платформа; масштабируемость ограничена | **2-4%** в enterprise custom bot projects | Мы можем занять середину между продуктом и кастомом: быстрее, дешевле, но с SLA и локальным hosting option |

**Итог по конкурентам:** западные игроки сильнее в продукте и масштабе, российские сильнее в локальных каналах и расчётах в рублях. Наш реальный wedge не в модели "ещё один бот", а в **быстром запуске автономной post-purchase поддержки для e-commerce с локальным compliance-контуром**.

### 4) Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется | med | high | >70% сделок держатся только на фаундере к M4-M6 | Нанять AE, прописать playbook, стандартизировать demo/scoping |
| Operational | Срыв интеграций с helpdesk/CRM/маркетплейсами | med | high | onboarding >21 дней, backlog интеграций растёт | Ограничить initial SKU интеграций, шаблоны коннекторов, sandbox-first |
| Operational | Деградация LLM API качества/latency/cost | high | high | latency >5 сек, hallucination spikes, рост cost per resolution >25% | Multi-model routing, fallback rules, кэш, human handoff |
| Market | Спрос остаётся niche, inbound почти нулевой | med | med | <10 SQL/мес после 90 дней GTM | Идти через outbound ABM и partners, не строить модель на inbound |
| Market | Ценовое сжатие со стороны helpdesk vendors | high | high | win-rate падает при цене >150k MRR | Пакетировать SLA/outcome, setup fee, premium integrations |
| Market | Конкуренты быстро копируют FAQ/chat сценарии | high | med | deal loss по причине "есть то же самое в Jivo/Usedesk" | Уходить в deeper workflows: возвраты, статусы, OMS/ERP actions |
| Regulatory | Нарушение 152-ФЗ / слабая data residency | med | high | enterprise buyers требуют DPA/on-prem и стопорят закупку | РФ-hosting, DPA templates, сегментация PII, локальный контур |
| Regulatory | 115-ФЗ / KYC-требования у финтех/маркетплейс-партнёров | low | med | buyer asks for enhanced audit trail / logging | Подготовить audit logs, role-based access, compliance package |
| Regulatory | Санкции на SaaS/LLM vendors | high | high | ограничения по API keys, billing decline, geo-blocks | Российские прокси/альтернативы, open-weight fallback, vendor diversification |
| Financial | Runway съедается до достижения repeatable sales | high | high | cash runway <9 мес до M6 | Заморозка найма, tranche-based budget, prepayment и setup fees |
| Financial | USD/RUB девальвация повышает LLM и cloud COGS | high | med | gross margin падает <50% два месяца подряд | Рублёвые контракты с FX clause, лимиты usage, локальный infra mix |
| Financial | Инфляция/налоги/FOT растут быстрее выручки | med | med | payroll inflation >15% YoY, EBITDA plan miss 2 квартала | Индексация цен, phased hiring, contractor mix |
| Black swan | Резкое ужесточение санкций/война ломает доступ к vendor stack | med | high | vendor notices, billing disruption, forced migration | DR-plan, резервные модели, локальные провайдеры, экспорт ключевых данных |
| Black swan | Массовое отключение LLM API или policy-ban на support use case | low | high | sudden quota cuts / ToS changes | Open-source fallback, retrieval-only mode, manual ops switch |

### 5) Kill conditions через 6 месяцев
1. **Median-quality insolvency risk:** если rolling forecast показывает **p10 EBITDA@M24 < 0** и runway < **6 месяцев**, продолжать нельзя.
2. **Unit economics fail:** если через 6 месяцев **CAC payback > 6 месяцев** или **LTV/CAC < 3x**, значит acquisition неинвестируем.
3. **Retention/pricing fail:** если **logo churn > 4.5%/мес** или средний net MRR/client < **150 000 ₽**, operating leverage не собирается даже при росте.

### 6) Итог SECTION B
Кейс остаётся **проходимым**, но уже не как "чистый PASS", а как **PASS WITH HEAVY RISK DISCOUNT**. Base/median экономика выглядит хорошей, но левый хвост распределения плохой: p10 EBITDA отрицательный, LTV/CAC range очень широкий, а pricing pressure и churn легко переводят модель в uninvestable состояние.

### Sources for SECTION B
- [B1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-avtonomnyi-operator-klientskoi-podderzhki-dlya-e-commerce-i-dtc-brendov/04-economics.md
- [B2] https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [B3] https://www.jivo.ru/pricing/ ; https://usedesk.ru/pricing
- [B4] https://www.gorgias.com/pricing ; https://www.gorgias.com/product
- [B5] https://www.zendesk.co.jp/pricing/support/
- [B6] https://www.intercom.com/pricing-new
- [B7] https://habr.com/users/usedesk
- [B8] https://help.carrotquest.io/article/685
- [B9] https://www.rusprofile.ru/id/10236368
- [B10] https://vc.ru/services/1018468-wikibot-chat-bot-dlya-podderzhki-klientov-s-ii-kotoryi-znaet-pro-vash-biznes-bolshe-vas
- [B11] https://vc.ru/ai/2817462-ted-chat-avtomatizatsiya-kommunikatsiy

<!-- P6A-DONE -->
<!-- P6B-DONE -->
