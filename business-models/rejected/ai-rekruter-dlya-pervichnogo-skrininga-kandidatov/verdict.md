[B2B-OPS] AI-рекрутер для первичного скрининга кандидатов — NEAR-PASS: 69/100 | EBITDA base=560К₽/мес через 13 мес | LTV/CAC=17,3x | Ключевое преимущество: ROI-layer для массового найма с быстрым payback | Главный риск: weak moat и риск скатывания в service-heavy recruiting ops.

# 06-verdict

sector: B2B-OPS

## Investment committee verdict
- Название: AI-рекрутер для первичного скрининга кандидатов
- Slug: ai-rekruter-dlya-pervichnogo-skrininga-kandidatov
- Вердикт: NEAR-PASS
- Итоговый score: 69/100
- Raw score: 103/150
- Нормализация: round(103 × 100 / 150) = 69
- Committee note: кейс уверенно проходит unit economics и EBITDA gate, но не получает approve из-за слабого exact-demand сигнала в РФ, weak moat и высокого риска service creep в delivery.

## Этапы 1-5
### Этап 1 — Intake
Исходный тезис: AI-рекрутер, который сам назначает интервью, проводит voice/video pre-screening, пишет summary и scorecard, а затем передаёт shortlist рекрутеру или в ATS.

### Этап 2 — Validation / Evidence
В текущем кейсе отдельный файл `02-validation.md` отсутствует. Функцию подтверждения выполняют `01-evidence.md` и `02-demand.md`:
- Apriora заявляет 5 000 откликов в месяц и более 2 000 интервью через продукт.
- Skillaz и ConverzAI подтверждают, что buyer покупает ускорение screening и сокращение recruiter-hours, а не просто AI-фичу.
- Публичные тарифы Talantix, Workable, Manatal и Zoho Recruit подтверждают, что бюджет на recruiting stack уже существует.

### Этап 3 — Demand
Спрос в РФ есть, но он не investment-grade по чистоте сигнала:
- machine demand-check дал `composite_demand = LOW`;
- practical TAM/SAM сходится только в узком segment-first wedge;
- viable monetization начинается не в self-serve, а в managed screening / enterprise layer.

### Этап 4 — Economics
Base economics сильные:
- customer_ltv_rub = **5 440 000 ₽**
- CAC = **313 650 ₽**
- LTV/CAC = **17,3x**
- CAC payback = **2,3 мес**
- Gross Margin = **76,0%**
- contribution_margin_rub_month = **136 000 ₽/мес**
- fixed_costs_rub_month = **5 800 000 ₽/мес**
- startup_capital_to_bep_rub = **35 198 360 ₽**

### Этап 5 — Critic / Finance Risk
Finance critic подтверждает, что median-case сильный, но downside-tail неприятный:
- **p10 EBITDA @M24 = -780 000 ₽/мес**
- **p50 EBITDA @M24 = 8 540 000 ₽/мес**
- **p90 EBITDA @M24 = 14 930 000 ₽/мес**

Это не broken model, но distribution слишком широкий для чистого approve без дополнительных proof points по retention, pricing power и repeatable GTM.

## Оценка
Source tier balance: T1=2, T2=7, T3=1, weighted=2.10. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | "LTV/CAC: 17.3x", "CAC Payback = 2.3 мес", "Gross Margin = 76.0%" подтверждают investment-grade unit economics. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | "EBITDA при 50 клиентах: ~1.0 млн ₽/мес"; до 500k ₽/мес кейс доходит примерно при 47 клиентах и около M13. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | "composite_demand = LOW" ограничивает confidence, хотя "Profit Gate в принципе достижим" в managed и enterprise сценариях; применён tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Есть полезный workflow wedge, но нет сильных network effects и data moat, а в кейсе прямо зафиксирован риск, что продукт станет ATS-feature или service. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | "p10 EBITDA < 0", "рост стоимости или деградация LLM API" и длинный pilot-heavy sales motion повышают execution burden. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | Fully-loaded CAC **313 650 ₽** и payback **2,3 мес** сильны, а ICP по агентствам, массовому найму и enterprise подтверждён demand stage. |

## Moat: 7-factor framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных напрямую. |
| 2. Switching costs | 2 | Интеграции с ATS, шаблоны scorecards и обучение команды создают умеренную цену переключения. |
| 3. Scale economies | 2 | Shared infra и AI pipeline дешевеют с ростом, пока delivery остаётся productized. |
| 4. Proprietary data / model advantage | 1 | Свой защищённый датасет или уникальный model advantage в evidence не доказаны. |
| 5. Regulatory moat | 1 | 152-ФЗ и data residency важны, но это market requirement, а не уникальный moat компании. |
| 6. Brand / distribution | 1 | В РФ нет подтверждённого dominant brand, а лидогенерация остаётся largely founder/GTM-driven. |
| 7. Embedded workflow | 2 | Продукт встраивается в screening и scheduling, но пока не становится system-of-record. |

Moat score = round((9 × 25) / 21) = 11/25.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 5 440 000 ₽ |
| CAC | 313 650 ₽ |
| LTV/CAC | 17,3x |
| CAC payback | 2,3 мес |
| Gross Margin | 76,0% |
| contribution_margin_rub_month | 136 000 ₽/клиент/мес |
| company_ebitda_rub_month base M12 | 114 859 ₽/мес |
| company_ebitda_potential_rub_month | 1 000 000 ₽/мес |
| break-even clients | 43 |
| clients_to_500k_ebitda | 47 |
| clients_to_1m_ebitda | 50 |
| months_to_500k_ebitda | 13 |
| months_to_1m_ebitda | 13 |
| fixed_costs_rub_month | 5 800 000 ₽/мес |
| startup_capital_to_bep_rub | 35 198 360 ₽ |
| Практический капитал с буферами | 40 000 000 ₽ |

## Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов | SDR | HH.ru, сайты компаний, CRM | 20 мин/акк | 300 | Полуручной |
| 2 | Enrichment контактов | SDR | Snov/аналог, email finder, CRM | 10 мин/акк | 120 | Полуавто |
| 3 | Первый outbound-touch | SDR | CRM + email + Telegram/телефония | 5 мин | 80 | Частично автоматизировано |
| 4 | Follow-up 1-3 | SDR | CRM sequences | 15 мин суммарно | 240 | Авто + ручной контроль |
| 5 | Квалификация боли | SDR | Скрипт discovery, CRM | 30 мин | 450 | Ручной |
| 6 | Discovery call | AE | Video call + CRM | 45 мин | 1 200 | Ручной |
| 7 | Demo продукта | AE + sales engineer/CTO | Meet, demo env | 60 мин | 2 200 | Ручной |
| 8 | Сбор требований и security/ATS-fit | AE + CTO | Notion/CRM/почта | 90 мин | 3 500 | Ручной |
| 9 | Pilot proposal и расчёт ROI | AE | Шаблон калькулятора ROI | 60 мин | 1 600 | Полуручной |
| 10 | Запуск пилота | CSM + CTO | Product admin, ATS integration | 4-6 ч | 9 000 | Полуручной |
| 11 | Скрининг кандидатов в пилоте | AI + recruiter reviewer | LLM, voice stack, dashboard | 1-2 недели | 12 000 | Высокая автоматизация |
| 12 | Итоговый review пилота | AE + CSM | Dashboard + ROI report | 60 мин | 1 800 | Полуручной |
| 13 | Procurement / договор | AE + CEO | ЭДО, юрист, почта | 5-10 раб. дней | 4 500 | Ручной |
| 14 | Invoice / счёт | Finance ops | 1C/банк/ЭДО | 20 мин | 400 | Полуавто |
| 15 | Оплата и активация monthly service | Finance ops + CSM | Банк, CRM, product admin | 15 мин | 300 | Полуавто |

## Команда
| Роль | Функция | Fully-loaded ₽/мес |
|---|---|---:|
| CEO / founder | продажи крупных аккаунтов, fundraising, key accounts | 650 000 |
| CTO / Tech Lead | продукт, архитектура, security, integration oversight | 715 000 |
| Senior Backend #1 | core backend, ATS integrations | 520 000 |
| Senior Backend #2 | workflow engine, billing, data pipelines | 520 000 |
| ML Engineer | scoring, prompts, evaluation, AI quality | 585 000 |
| DevOps | infra, observability, deployment | 390 000 |
| SDR | outbound prospecting | 195 000 |
| AE | demo, pilot, close | 390 000 |
| Customer Success | onboarding, retention, upsell | 286 000 |
| **Итого FOT** |  | **4 251 000** |

## GTM: 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | ANCOR | Крупное кадровое агентство, pain в масштабировании первичного screening без роста рекрутеров подтверждён рынком staffing. | email decision-maker + ABM outreach | 180 000 ₽/мес |
| 2 | Ventra | Staffing и аутсорсинг персонала, где скорость pre-screening напрямую влияет на placements и EBITDA. | email managing director + отраслевой ивент | 180 000 ₽/мес |
| 3 | Coleman Group | Recruitment services и регулярный поток вакансий создают repeatable use-case для AI-screening. | direct email head of recruitment | 170 000 ₽/мес |
| 4 | Ozon | Массовый hiring в логистике, операционке и call-center функциях, где screening-объём большой и цикличный. | партнёрство + direct outreach TA lead | 220 000 ₽/мес |
| 5 | X5 Group | Массовый подбор в retail и логистике, важен time-to-screen и сокращение recruiter-hours. | конференция HR Tech + email decision-maker | 230 000 ₽/мес |
| 6 | Самокат | Высокая текучесть и distributed hiring в дарксторах, нужен быстрый screening frontline-кандидатов. | direct email + продуктовый pilot | 190 000 ₽/мес |
| 7 | СДЭК | Постоянный подбор в филиалах и логистике, pain в стандартизации первичного отбора. | партнёрство с ATS/integrator | 170 000 ₽/мес |
| 8 | Додо Пицца | Сетевой массовый hiring по ресторанам, где screening и scheduling можно автоматизировать end-to-end. | vc.ru ad + founder outreach | 160 000 ₽/мес |
| 9 | ВкусВилл | Retail hiring и высокая повторяемость screening делают managed layer экономически оправданным. | email head of talent acquisition | 180 000 ₽/мес |
| 10 | Rostic’s | Frontline mass hiring с понятным ROI на скорости и снижении ручной нагрузки рекрутеров. | direct outreach + HR event | 160 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Комментарий |
|---|---|---|---|
| weak_moat_and_feature_bundling | high | high | Если ATS-инкамбенты или HR-suite игроки добавят comparable AI-screening как фичу, premium pricing быстро сожмётся. |
| service_creep_destroying_margin | high | high | Кейс прямо зависит от того, что managed screening не превратится в кастомный recruiting service с ростом human review. |
| evidence_quality_unverified | medium | medium-high | Exact category demand в РФ пока слабый, а weighted tier balance = 2,10, поэтому conviction ниже approve-grade. |

## Что должно быть доказано для APPROVED
1. Не менее 3-5 платных пилотов в РФ с ARPA не ниже **150 000-180 000 ₽/мес**.
2. Pilot-to-paid conversion не ниже **25%** и monthly churn не выше **2,5-3,0%**.
3. Human review и COGS удерживаются в коридоре **≤50-55 тыс. ₽/клиент/мес**.
4. Не менее 2 repeatable vertical playbooks для staffing или mass hiring с go-live **<45 дней**.
5. Подтверждение, что buyers покупают именно screening layer, а не только более дешёвый ATS-seat.

## Proof points, которые уже сильны
- Публичные price anchors Talantix, Workable, Manatal и Zoho Recruit подтверждают реальный бюджет на recruiting software.
- Skillaz, Apriora и ConverzAI подтверждают полезность AI-screening и interview automation как ROI-driven wedge.
- Unit economics уже инвестиционно сильна: customer_ltv_rub **5,44 млн ₽**, CAC **313 650 ₽**, payback **2,3 мес**.
- EBITDA gate достижим: **47 клиентов → ~560 тыс. ₽/мес**, **50 клиентов → ~1,0 млн ₽/мес**.

## LTV Upside Calculator
Так как кейс = NEAR-PASS, для апгрейда до approve нужен следующий upside:

| Рычаг | Текущее | Target | Эффект |
|---|---:|---:|---|
| ARPU | 179 000 ₽ | 195 000 ₽ | Ускоряет путь к EBITDA >500k и повышает gross profit на клиента. |
| COGS | 43 000 ₽ | 38 000 ₽ | Поднимает contribution_margin_rub_month до ~157 000 ₽. |
| CAC | 313 650 ₽ | 280 000 ₽ | Улучшает payback и снижает burn-to-breakeven. |
| Churn | 2,5% | 2,0% | Увеличивает customer_ltv_rub с ~5,44 млн ₽ до ~7,41 млн ₽. |
| GTM | mixed outbound | partner-led + staffing focus | Снижает acquisition friction и даёт более repeatable ICP. |

Пример upside-сценария: при ARPU 195k, COGS 38k и CAC 280k получаем contribution_margin_rub_month около 157k ₽, payback около 1,8 месяца и LTV/CAC существенно выше 20x, что уже даёт запас для APPROVED при подтверждённом retention.

## Финальный вывод
Кейс уже достоин watchlist: economics сильная, EBITDA gate достижим и buyer pain реальна. Но инвестиционный комитет пока не даёт APPROVED, потому что рынок в РФ выглядит узким и плохо стандартизованным, а moat слабее, чем хотелось бы для fund-level conviction. Решение: **NEAR-PASS / rerun после платных пилотов и подтверждения repeatable GTM**.
