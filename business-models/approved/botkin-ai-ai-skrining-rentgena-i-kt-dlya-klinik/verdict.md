[HEALTHCARE] Botkin.AI — APPROVED WITH NOTES: 71/100 | EBITDA base=542К₽/мес через 17 мес | LTV/CAC=16,9x | Ключевое преимущество: глубокая интеграция в radiology workflow и регуляторный контур | Главный риск: price compression и project-heavy внедрения.

# Botkin.AI, AI-скрининг рентгена и КТ для клиник — 06-verdict
sector: HEALTHCARE
status: APPROVED WITH NOTES
score: 71/100
date: 2026-04-25
slug: botkin-ai-ai-skrining-rentgena-i-kt-dlya-klinik

## Итог
**Вердикт инвесткомитета: APPROVED WITH NOTES.**

Кейс проходит approval gate, потому что одновременно выполняются два условия:
1. **Normalized score = 71/100**, то есть выше порога 70.
2. **company_ebitda_potential_rub_month = 542 000 ₽/мес** достигается при **50 клиентах** и примерно **к 17 месяцу**, что укладывается в обязательный profitability gate: ≥500k ₽/мес, ≤50 клиентов, ≤24 месяцев.

Это не лёгкий SaaS, а тяжёлый regulated healthtech infrastructure play. Инвестиционный тезис держится на доказанной категории radiology AI в РФ, хорошей unit economics на уровне клиента и реальном regulatory/integration moat. Ограничение одно, но серьёзное: бизнес становится инвестиционно качественным только при дисциплине в pricing, платных пилотах и стандартизированных внедрениях.

## Этапы 1-5
### Этап 1 — Intake
Кейс пришёл как wedge вокруг AI-скрининга КТ, рентгена, маммографии и флюорографии для клиник и центров лучевой диагностики. Базовый тезис: продукт ускоряет triage, снижает ручную нагрузку рентгенологов и продаётся как B2B workflow-layer внутри PACS/МИС-контура.

### Этап 2 — Validation / Evidence
Evidence подтверждает, что Botkin.AI, это не лабораторный pilot-only продукт:
- официальный B2B-лендинг подтверждает фокус на клиниках и radiology workflow;
- Skolkovo и CNews подтверждают наличие регистрационных кейсов и международной коммерциализации;
- category proof по РФ есть через Минздрав, региональные внедрения ИИ и публичный рынок частной медицины.

### Этап 3 — Demand
Прямой exact-keyword спрос низкий, но для regulated B2B medtech это ожидаемо. Категория валидируется не поиском, а production-use, закупками, вакансиями и substitute-spend:
- Минздрав и регионы уже публикуют production-use AI в лучевой диагностике;
- hh.ru подтверждает организационный спрос на работу врача-рентгенолога в связке с ИИ;
- substitutes и конкуренты уже монетизируют second opinion и B2B-лицензии.

### Этап 4 — Economics
Base economics сильная:
- customer_ltv_rub = **7 542 857 ₽**
- CAC = **445 646 ₽**
- LTV/CAC = **16,9x**
- CAC payback = **2,8 мес по gross profit / 2,0 мес по MRR sanity-check**
- Gross Margin = **72,0%**
- contribution_margin_rub_month = **142 700 ₽/мес**
- fixed_costs_rub_month = **6 593 000 ₽/мес**
- startup_capital_to_bep_rub = **67 241 695 ₽** в базовом сценарии

### Этап 5 — Critic / Finance Risk
Monte Carlo Lite показывает не collapse, а широкий разброс:
- **p10 EBITDA @M24 = 623 881 ₽/мес**
- **p50 EBITDA @M24 = 4 864 739 ₽/мес**
- **p90 EBITDA @M24 = 8 431 414 ₽/мес**

То есть median-case проходит profitability gate уверенно, но dispersion высокий, а ключевой риск, это price compression плюс дорогой enterprise CAC. Поэтому кейс получает approve только с notes.

## Оценка
Source tier balance: T1=6, T2=12, T3=1, weighted=2.37. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 16.9x», «CAC Payback on gross profit = 2.8 мес», «Gross Margin: 72.0%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | «EBITDA achievable at 50 clients | ~542 000 ₽/мес», break-even примерно на M17. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | «Итог: ниша не mass-demand, а narrow B2B», но есть production-use Минздрава и hh-вакансия под AI-radiology. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 17 | Регуляторика, PACS/МИС-интеграции и embedded workflow дают защиту, но рынок уже занят сильными локальными игроками. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | «наиболее опасная связка, это операционная кастомизация + price compression + регуляторный on-prem pressure + длинный cash conversion». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | CAC 446k ₽ и payback 2,8 мес дают запас, а GTM реалистичен для private networks и imaging-heavy контуров. |

**Сумма raw:** 106/150  
**Normalized score = round((106 × 100) / 150) = 71/100**

## 7-factor moat framework
| Фактор | Балл (0-3) | Почему |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент даёт дополнительные данные и workflow-инсайты, но это слабый network effect, не marketplace. |
| Switching costs | 3 | Данные, интеграции PACS/МИС, обучение врачей и встраивание в маршрут чтения делают смену поставщика дорогой. |
| Scale economies | 2 | Compute, QA и compliance частично амортизируются на объёме, хотя внедрение остаётся partly custom. |
| Proprietary data / model advantage | 2 | Есть product and deployment advantage, но публичного T1/T2 подтверждения размера датасета внутри кейса нет, поэтому без максимума. |
| Regulatory moat | 3 | Категория и компания живут в медконтуре с регистрационными требованиями и высоким compliance-барьером. |
| Brand / distribution | 2 | Botkin.AI узнаваем в нише и имеет международные референсы, но в РФ против него уже стоят сильные incumbents. |
| Embedded workflow | 3 | Продукт встроен прямо в radiology workflow: triage, second reader, QA и приоритизация исследований. |

**Moat raw = 16/21**  
**Moat score = round((16 × 25) / 21) = 19/25**

Комментарий: moat выше среднего, но не монопольный. Это сильный workflow + regulatory moat, а не winner-takes-all moat. Поэтому в общей рубрике criterion #4 выставлен на **17/25**, а не на уровне top-tier platform.

## Investment committee view
### Почему кейс прошёл
1. **Категория уже доказана в РФ** через production-use radiology AI, гос- и частные контуры.
2. **Unit economics investment-grade**: LTV/CAC 16,9x, payback 2,8 месяца, GM 72%.
3. **EBITDA gate достигается** при 50 клиентах и в пределах 24 месяцев.
4. **Регуляторика и интеграции** создают реальный moat против generic AI-продуктов.

### Почему кейс не получил чистый APPROVED
1. Прямой keyword demand низкий и рынок продаётся только sales-led motion.
2. Base-case требует **67,2 млн ₽** до break-even против стартового капитала 60 млн ₽.
3. Модель очень чувствительна к скидкам, бесплатным пилотам и project-heavy внедрениям.

## Полный бизнес-процесс из 04-economics.md
| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-аккаунтов клиник/сетей | SDR | hh/2ГИС/СПАРК/CRM | 2 ч на 20 аккаунтов | 2 500 | низкая |
| 2 | Outbound outreach, email/call/Telegram/LinkedIn аналоги | SDR | CRM, телефония, почта | 10-14 дней | 9 000 | средняя |
| 3 | Первичный discovery-call | AE + founder | CRM, Meet | 1 ч + prep | 6 500 | низкая |
| 4 | Квалификация по объёму исследований, PACS/МИС, бюджету | AE + Solutions | CRM, questionnaire | 3-5 дней | 8 000 | средняя |
| 5 | Демо на реальных кейсах | AE + clinical specialist | Demo env, Meet | 1-2 ч | 10 000 | низкая |
| 6 | NDA и обмен sample studies | AE + legal + клиника | e-sign, secure storage | 5-10 дней | 12 000 | средняя |
| 7 | Технический scoping интеграции | Solutions engineer + CTO | PACS connector, API docs | 1-2 недели | 30 000 | низкая |
| 8 | Пилот на локальном потоке | ML/implementation + клиника | inference stack, QA dashboard | 4-8 недель | 95 000 | средняя |
| 9 | Медицинская/операционная валидация результатов | Clinical specialist | QA sheets, reporting | 1-2 недели | 24 000 | низкая |
| 10 | Коммерческое предложение и security/legal review | AE + legal + CTO | CRM, шаблоны договора | 2-4 недели | 28 000 | низкая |
| 11 | Procurement/тендер или direct approval | Buyer + AE | закупочный контур | 2-6 недель | 18 000 | низкая |
| 12 | Подписание договора и счёт | AE + finance | ЭДО, 1С | 3-7 дней | 7 500 | высокая |
| 13 | Onboarding production и обучение врачей | Implementation + CSM | LMS, docs, support desk | 2-3 недели | 42 000 | средняя |
| 14 | Monthly usage, support, retraining, account reviews | CSM + ML ops | helpdesk, monitoring | ежемесячно | 21 000 | средняя |
| 15 | Оплата и контроль дебиторки | Finance + AE | 1С, банк, CRM | 3-10 дней | 4 500 | высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 7 542 857 ₽ |
| CAC | 445 646 ₽ |
| LTV/CAC | 16,9x |
| CAC Payback | 2,8 мес gross / 2,0 мес simple |
| Gross Margin | 72,0% |
| contribution_margin_rub_month | 142 700 ₽/мес |
| fixed_costs_rub_month | 6 593 000 ₽/мес |
| Break-even clients | 47 |
| clients_to_500k_ebitda | 50 |
| clients_to_1m_ebitda | не достигнуто при 50 клиентах |
| months_to_500k_ebitda | 17 |
| months_to_1m_ebitda | >24 |
| company_ebitda_rub_month base | 542 000 ₽/мес при 50 клиентах |
| company_ebitda_potential_rub_month | 542 000 ₽/мес |
| startup_capital_to_bep_rub | 67 241 695 ₽ |

## Команда
| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO/founder | продажи, fundraising, partnerships | 845 000 |
| CTO/Tech Lead | архитектура, PACS/МИС integration, security | 715 000 |
| Senior Backend x2 | API, data pipelines, integrations | 1 170 000 |
| ML Engineer | inference, quality, retraining | 715 000 |
| DevOps/SRE | infra, observability, deployment | 455 000 |
| Frontend/Product engineer | кабинет, reporting | 390 000 |
| SDR | outbound generation | 195 000 |
| AE | deals, pilots, procurement | 416 000 |
| Customer Success/Implementation | onboarding, training, renewals | 312 000 |
| Clinical specialist/radiology advisor | validation, medical workflows | 364 000 |
| Finance/admin (0.5 FTE) | счета, закрытие, legal ops | 156 000 |
| **Итого** |  | **5 733 000 ₽/мес** |

## GTM — 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | крупнейшая частная сеть, высокий объём imaging и доказанный интерес к clinical AI в private-care контуре | email decision-maker + warm intro через digital health ecosystem | 1 200 000 ₽/мес |
| 2 | Мать и дитя / MD Medical | сеть с маммографией, женским здоровьем и высоким спросом на QA/second reader | founder-led intro к medical director + профильная конференция | 900 000 ₽/мес |
| 3 | EMC | premium сеть, где скорость описания и снижение diagnostic risk имеют прямую монетизацию | direct email CIO/CMO | 800 000 ₽/мес |
| 4 | СМ-Клиника | крупная многопрофильная сеть, где дефицит рентгенологов и поток КТ/рентгена дают явную боль | outbound через медицинского директора + отраслевой форум | 700 000 ₽/мес |
| 5 | Поликлиника.ру | большая амбулаторная сеть, которой нужен throughput и стандартизация описаний | email decision-maker + партнёрский интро через МИС/ПАКС-вендора | 500 000 ₽/мес |
| 6 | Медскан | сеть с диагностическими активами и фокусом на цифровые сервисы, хороший fit под multi-site rollout | conference + founder outreach | 850 000 ₽/мес |
| 7 | РЖД-Медицина | распределённая сеть и централизованный контур закупки, где ценен multi-site radiology workflow | партнёрство с интегратором + procurement intro | 900 000 ₽/мес |
| 8 | МИБС | imaging-heavy сеть центров, у которой core pain лежит прямо в лучевой диагностике и throughput | email руководителю лучевой службы | 1 000 000 ₽/мес |
| 9 | К+31 | premium private healthcare с высокими требованиями к SLA и качеству диагностики | direct outreach к CIO / chief medical officer | 450 000 ₽/мес |
| 10 | Клиника Фомина | быстрорастущая сеть с сильным digital DNA и понятным channel fit для pilot-to-paid motion | founder outreach + отраслевые медиа / конференции | 400 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Price compression и скидочный enterprise motion | high | high | Stress price -30% уводит EBITDA @M12 до -4 233 960 ₽/мес и ломает запас прочности. |
| Integration drag и project-heavy delivery | high | high | Кастомные PACS/МИС-интеграции способны съесть roadmap, GM и темп rollout. |
| Cash gap до break-even | medium-high | high | startup_capital_to_bep_rub 67,2 млн ₽ выше исходного капитала 60 млн ₽, значит без дисциплины возможна докапитализация. |

## Proof points для APPROVED
1. **Есть category proof в РФ:** production-use ИИ в лучевой диагностике подтверждён Минздравом и регионами.
2. **Есть enterprise-grade economics:** risk-adjusted LTV/CAC 6,8x и gross-basis LTV/CAC 16,9x.
3. **Есть достижимый EBITDA gate:** 50 клиентов дают около 542 000 ₽/мес в base-case.
4. **Есть regulatory / integration moat:** продукт встроен в PACS/МИС и продаётся в высокобарьерный medical workflow.

## Что доказать в ближайшие 6 месяцев
1. **Платный pilot-to-paid conversion ≥ 30%** без системных бесплатных пилотов.
2. **ARPA floor не ниже 180-200 тыс. ₽/мес** на новых контрактах.
3. Не менее **2-3 референсных частных сетей** с go-live < 90 дней.
4. Доля кастомной разработки во внедрении не выше **20-25% capacity** продуктовой команды.

## Delta vs previous
Предыдущего полноценного P7 verdict для кейса не было. Относительно стадий P4-P6 картина усилилась за счёт formal rubric scoring, 7-factor moat framework и Monte Carlo Lite. Главный вывод не изменился: кейс investable, но только как disciplined enterprise healthtech play, а не как mass-market AI-product.

## Финальный комитетский вывод
**APPROVED WITH NOTES.**

Botkin.AI подходит для фонда, который умеет инвестировать в regulated B2B healthtech и принимает длинный sales cycle. Кейс не для вирусного AI-growth, а для системного workflow-инфраструктурного бизнеса с высоким ACV, глубокой интеграцией и понятным путём к EBITDA при сохранении pricing discipline.
