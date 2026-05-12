[B2B-OPS] Workday Contract Intelligence + Negotiation Agents — NEAR-PASS: 67/100 | EBITDA base=1239К₽/мес через 9 мес | LTV/CAC=3,8x | Ключевое преимущество: enterprise contract-ops wedge с measurable cycle-time ROI | Главный риск: exact-demand в РФ слабый, а price compression быстро ломает EBITDA.

# 06-verdict — Workday Contract Intelligence + Negotiation Agents v2

sector: B2B-OPS

## Итоговый вердикт
- **Вердикт:** **NEAR-PASS**
- **Score:** **67/100**
- **Статус инвесткомитета:** экономика проходит investment gate, но доказательств по локальному спросу, moat и repeatable GTM пока недостаточно для clean approve.
- **Формальный gate:** выполняется, потому что в base-scenario `company_ebitda_rub_month = 1 239 333 ₽/мес` достигается к **M9**, а порог `500 000 ₽/мес` проходится уже к **M8** при **18,05 клиентах**, то есть раньше 24 месяцев и сильно раньше лимита 50 клиентов.
- **Почему не APPROVED:** в `02-demand.md` exact-demand в РФ по ключам остаётся `LOW`, moat умеренный, а sensitivity в `05-critic.md` показывает, что шок `Price -30%` переводит модель в `EBITDA @M12 = -586 143 ₽/мес`.
- **Примечание по стадиям:** в этом кейсе demand-артефакт фактически хранится в `02-demand.md`, а solution/GTM в `03-solution.md`; для P7 использованы реальные файлы кейса.

## Оценка
Source tier balance: T1=1, T2=8, T3=1, weighted=2.00. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `Gross Margin = 56,2%`, `Downside LTV/CAC = 3,8x`, `Operating payback = 6,73 мес` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В 05-critic.md base-case уже на `M8` даёт `EBITDA 235 918 ₽`, а на `M9` `1 239 333 ₽`, то есть gate устойчиво пройден. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md exact-demand везде `LOW`, но есть `hh_ru=130` по proxу и `SAM ... 0,96-1,06 млрд ₽`; применён penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Защита строится на embedded workflow, switching costs и repository/playbook data, но без network effects и с умеренным regulatory barrier. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | В risk matrix отмечены `founder-dependent sales`, `service-heavy delivery`, `152-ФЗ / data residency`, `санкции` и `отключение ключевого LLM-провайдера`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | В 04-economics.md зафиксированы конкретные enterprise channels, `Blended fully-loaded CAC = 1 050 000 ₽`, а named targets ниже соответствуют ICP. |

**Sum raw = 100/150. Normalized score = round((100 × 100) / 150) = 67/100.**

## Investment thesis
Это не массовый legal copilot и не «ещё одна CLM-фича», а enterprise contract operations layer с дорогим onboarding, playbooks, routing, repository cleanup и recurring governance. Категория коммерчески доказана глобально, а локально может собраться в управляемый B2B-OPS бизнес только при жёстком ICP, premium pricing floor и стандартизированном pilot-to-retainer motion.

## Delta vs previous
- Кейс был resurrect как самостоятельный slug, а не как вложенный supporting signal.
- По сравнению с triage сильнее всего подтвердились **unit economics**, **enterprise willingness to pay** и **EBITDA gate**.
- Слабее всего подтвердились **прямой локальный category pull** и **defensible moat** против ECM/CLM incumbents и AI-copilot pressure.

## FULL business process from 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Target-account mapping по enterprise legal/procurement | SDR | CRM, реестры, ручной research | 2,0 ч | 2 400 | Низкая |
| 2 | Первый outbound / intro | SDR | email, phone, Telegram, CRM | 1,5 ч | 1 900 | Средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1,0 ч | 3 400 | Средняя |
| 4 | Discovery contract workflow | AE + founder | discovery template, call notes | 2,0 ч | 10 500 | Низкая |
| 5 | Demo review / redlining / repository intelligence | AE + solutions legal | demo workspace | 2,0 ч | 12 500 | Низкая |
| 6 | Pilot scoping и KPI design | AE + solutions + CSM | ROI sheet, SOW | 3,0 ч | 17 000 | Низкая |
| 7 | Security / privacy / procurement review | CTO + founder | checklist, security pack | 4,0 ч | 21 000 | Низкая |
| 8 | Repository cleanup + clause playbooks setup | implementation + solutions legal | KB, templates, workflow rules | 20 ч | 86 000 | Низкая |
| 9 | Pilot 6-10 недель | CSM + solutions legal | weekly reviews, QA, reporting | 16 ч | 61 000 | Средняя |
| 10 | Contracting / procurement | AE + founder + legal | ЭДО, договоры, redlines | 8 ч | 31 000 | Низкая |
| 11 | Launch / invoicing | ops + CSM | ЭДО, billing, runbook | 2 ч | 5 500 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| ACV | 7 800 000 ₽/год |
| MRR на клиента | 650 000 ₽/мес |
| customer_ltv_rub | 9 240 000 ₽ stress / 24 353 333 ₽ base |
| Gross Margin | 56,2% |
| contribution_margin_rub_month | 321 000 ₽/мес на клиента |
| Fully-loaded CAC | 1 050 000 ₽ |
| LTV/CAC | 3,8x downside / 8,8x stress |
| CAC Payback | 1,62 мес по MRR / 2,88 мес по gross profit / 6,73 мес operating |
| Contribution Margin % | 49,4% |
| fixed_costs_rub_month | 5 348 000 ₽/мес |
| Break-even | 18-20 клиентов operating basis |
| company_ebitda_rub_month @ M9 base | 1 239 333 ₽/мес |
| company_ebitda_potential_rub_month @ 50 клиентов | 10 702 000 ₽/мес |
| clients_to_500k_ebitda | ~17-18 |
| clients_to_1m_ebitda | ~18 |
| months_to_500k_ebitda | 8 мес |
| months_to_1m_ebitda | 9 мес |
| startup_capital_to_bep_rub | 21 822 733 ₽ (base), 18 095 669 ₽ (optimistic), 32 832 423 ₽ (pessimistic) |

## Команда
| Роль | Кол-во | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO / founder | 1 | 845 000 | enterprise sales, pricing, key deals |
| CTO / platform lead | 1 | 676 000 | архитектура, security, presale |
| Backend / workflow engineer | 2 | 936 000 | integrations, workflow engine |
| Solutions legal | 1 | 442 000 | playbooks, exception review |
| Implementation / legal ops specialist | 1 | 338 000 | migration, repository cleanup |
| CSM | 1 | 299 000 | adoption, QBR, retention |
| SDR | 2 | 416 000 | ABM pipeline generation |
| AE | 1 | 403 000 | pilots, procurement, closing |
| Marketing / community | 1 | 247 000 | content, events, legal community |
| Finance / ops | 0,5 | 156 000 | invoicing, admin, ЭДО |
| **Итого** | **11,5** | **4 758 000** | steady-state команда |

## Moat — 7-factor framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | После настройки clause playbooks, repository cleanup и approval routing смена вендора становится дорогой. |
| Scale economies | 1 | COGS немного улучшается с объёмом, но legal oversight и onboarding остаются трудоёмкими. |
| Proprietary data / model advantage | 2 | Накапливаются clause history, exception patterns и review playbooks, но публичного dataset moat нет. |
| Regulatory moat | 1 | 152-ФЗ и data residency помогают, но формального лицензируемого барьера нет. |
| Brand / distribution | 2 | Категория подтверждена Workday/SpotDraft/Luminance, а вход возможен через enterprise legal ops и procurement pain. |
| Embedded workflow | 3 | Продукт глубоко встраивается в review, redlining, approvals, repository search и obligation workflows. |

**Moat sum = 11/21. Moat score = round((11 × 25) / 21) = 13/25.**

## GTM — 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Большой объём procurement и enterprise-legal договоров, высокая цена задержек и строгий audit trail. | email decision-maker в legal ops / procurement transformation | 900 000 ₽/мес |
| 2 | ВТБ | Регулируемый buyer с тяжёлым contract workflow и требованиями к data residency. | founder-led intro + банковская конференция | 850 000 ₽/мес |
| 3 | Альфа-Банк | Быстрые продуктовые и партнёрские контракты создают боль в review и approval routing. | direct outreach в COO/legal ops | 800 000 ₽/мес |
| 4 | Т-Банк | Высокая скорость запуска новых инициатив требует automation review, clause governance и repository search. | product/legal ops intro + referral | 750 000 ₽/мес |
| 5 | Ростелеком | Много supplier и enterprise contracts, где важно сократить cycle time и держать obligations. | отраслевой event + targeted email | 700 000 ₽/мес |
| 6 | МТС | Большой договорный массив между procurement, legal и sales ops, высокая цена ручной маршрутизации. | ABM в procurement/legal leadership | 700 000 ₽/мес |
| 7 | X5 Group | Массовый поток поставочных и коммерческих договоров, сильная боль в согласовании и шаблонах. | partnership с SI / retail legal ops outreach | 650 000 ₽/мес |
| 8 | Магнит | Нужен управляемый contract workflow для supplier contracts и obligation visibility. | email decision-maker + partner intro | 650 000 ₽/мес |
| 9 | Северсталь | Индустриальный холдинг с большим массивом закупочных и подрядных договоров, где дорого держать ручной review. | founder outreach + enterprise event | 700 000 ₽/мес |
| 10 | Самолет | Девелопер с большим объёмом подрядных и коммерческих договоров, где важны cycle time и clause standardization. | direct outreach в head of legal / operations | 650 000 ₽/мес |

### Оценка GTM realism
- Канальный fit реалистичен: здесь работают **founder-led enterprise sales, outbound ABM, partner referrals, legal/procurement events**.
- CAC не выглядит заниженным, потому что в модели уже учтены `enterprise sales motion, pilot, security review и category education`.
- Но GTM остаётся хрупким: при `CAC x2` в 05-critic.md `EBITDA @M12 = -236 006 ₽/мес`, а значит дисциплина по ICP и pricing критична.
- 10 named targets присутствуют, автоматический штраф к GTM не применяется.

## Финансовая интерпретация для инвесткомитета
- Unit economics проходят: downside `LTV/CAC = 3,8x`, gross margin 56,2%, operating payback 6,7 месяца.
- EBITDA path тоже рабочий: в base-case break-even приходится на `M8`, а к `M12` EBITDA уже `4 875 920 ₽/мес`.
- Но profile неустойчив к цене: в sensitivity `Price -30%` даёт отрицательный EBITDA, а Monte Carlo показывает `p10 EBITDA @M24 = -2 638 495 ₽/мес`.
- Следовательно, инвестиционный вопрос тут не в математике на бумаге, а в том, удастся ли удержать enterprise-прайсинг и не скатиться в legal-services heavy delivery.

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Price compression и discount pressure | high | high | В 05-critic.md `Price -30%` сразу переводит модель в `EBITDA @M12 = -586 143 ₽/мес`. |
| Service-heavy delivery / legal outsourcing drift | high | high | В 04-economics.md главный риск прямо описан как превращение продукта в `service-heavy legal ops business`. |
| Слабый exact-demand в РФ и founder-dependent GTM | med-high | high | В 02-demand.md exact-demand везде `LOW`, а в risk matrix зафиксирован `founder-dependent sales`. |

## Что должно быть доказано для перевода в APPROVED
1. **Не менее 2-3 paid pilots**, которые конвертируются в retainer, а не остаются на стадии разового project work.
2. **Pricing floor не ниже 650-700 тыс. ₽/мес** без системного discounting >20%.
3. **Повторяемый onboarding ≤10 недель** и legal oversight <25 часов senior-time на клиента в месяц.
4. **Минимум 2 референсных enterprise кейса** с доказанным cycle-time reduction и measurable backlog reduction.

## LTV Upside Calculator
### Формула
- `customer_ltv_rub = annual_revenue × gross_margin / annual_churn`
- `LTV/CAC = customer_ltv_rub / CAC`

### Upside table
| Сценарий | ARR, ₽ | GM | Annual churn | CAC, ₽ | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|---:|
| Текущая downside-база | 5 400 000 | 37% | 50% | 1 050 000 | 3 996 000 ₽ | 3,8x |
| Если вернуть stress-case | 6 600 000 | 42% | 30% | 1 050 000 | 9 240 000 ₽ | 8,8x |
| Если удержать base-case | 7 800 000 | 56,2% | 18% | 1 050 000 | 24 353 333 ₽ | 23,2x |
| Если CAC вырастет до 1,8 млн ₽ | 5 400 000 | 37% | 50% | 1 800 000 | 3 996 000 ₽ | 2,2x |
| Если price -30% и GM упадёт ниже 35% | 4 560 000 | 35% | 50% | 1 050 000 | 3 192 000 ₽ | 3,0x |

### Read-through
- Кейс уже близок к порогу investment-grade по downside LTV/CAC, но апсайд очень чувствителен к цене и churn.
- Поэтому путь из NEAR-PASS в APPROVED проходит через доказанный premium pricing и delivery discipline, а не через косметическое снижение CAC.

## Proof points for APPROVED
Не применяется, потому что итоговый статус кейса **NEAR-PASS**, а не APPROVED.

## Финальное решение комитета
**NEAR-PASS.**

Почему не reject:
- категория глобально подтверждена и локально имеет enterprise pain,
- economics проходят unit-gate и EBITDA-gate,
- buyer universe понятен и named targets реалистичны.

Почему пока не approve:
- локальный exact-demand всё ещё слабый,
- moat только средний,
- Monte Carlo tail-risk отрицательный,
- модель легко съезжает в service-heavy delivery при ослаблении pricing discipline.


## Appendix — full stage archive


---

# FILE: 01-intake.md

---
sector: LEGAL
rerun: true
source_raw: 2026-04-19-resurrect-workday-contract-intelligence-negotiation-agents.md
created: 2026-04-22T01:10:00+03:00
source_verdict: triage/triage-2026-04-11-workday-contract-intelligence-negotiation-agents.md
---

# Intake

## Статус
Принудительный resurrect / полный пайплайн P3→P7.

## Исходный verdict
- `triage/triage-2026-04-11-workday-contract-intelligence-negotiation-agents.md`

## Полный контекст raw

# RESURRECT SIGNAL — workday-contract-intelligence-negotiation-agents

## Meta
- source: triage/triage-2026-04-11-workday-contract-intelligence-negotiation-agents.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Triage

## Date
2026-04-11

## Inputs
- pipeline/raw/radar-2026-04-11-1010-msk.md

## Classification
potentially new case

## Decision
Создать новый case-кандидат.

**Suggested case slug:** `enterprise-contract-operations-agents`

## Why
- Сигнал указывает не просто на AI feature внутри SaaS, а на формирование operator-layer для contract lifecycle management, где AI выполняет содержательные contract tasks, включая intelligence и negotiation.
- Workday already serving more than 11,500 organizations suggests a large installed base that can turn this into downstream implementation, integration, governance, exception-handling and managed operations work.
- Контрактные процессы достаточно самостоятельны как functional wedge: это отдельный buyer motion, отдельные риски и отдельный пакет внедрения по сравнению с generic copilots.
- EU data residency angle strengthens enterprise readiness and makes the signal more actionable for regulated or multinational buyers.

## Triage note
Проверять как отдельную service line вокруг AI-enabled contract operations: CLM implementation, workflow redesign, approval policies, legal/procurement guardrails, ERP/CRM integration, exception routing, auditability и managed optimization. В следующем цикле полезно найти signals beyond vendor PR, особенно partners, consultancies и early deployment patterns.

```


---

# FILE: 02-demand.md

---
stage: demand-validation
case: workday-contract-intelligence-negotiation-agents-v2
date: 2026-04-24
analyst: branch-models-lead
sector: LEGAL-OPS
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

> Market Pulse 2026-04-25: растущий интерес.


## Кейс
Workday contract intelligence и negotiation agents как отдельная service line: AI-анализ договоров, redlining, approval policies, legal/procurement guardrails, интеграции и managed contract operations для крупных компаний. [T2]

## Executive summary
**Решение на этапе demand validation: CONDITIONAL PASS.**

- Exact-demand в РФ по англоязычным ключам слабый: internal endpoint по `contract intelligence`, `contract review ai`, `contract lifecycle management` и `согласование договоров ai` 24.04.2026 везде вернул `LOW`, хотя по русскому proxу уже видны `hh_ru=130` вакансий. Это значит, что массового self-serve спроса нет, но job-to-be-done существует. [T2]
- Category proof глобально сильный: SpotDraft обслуживает 700+ клиентов и обрабатывает 1+ млн контрактов в год, Luminance сообщает о 700+ клиентах в 70+ странах, а фиксированная AI-review модель Crosby продаётся по $250-1000 за контракт. Значит buyer готов платить не за «бота вообще», а за ускорение review и negotiation. [T2]
- Публичные цены конкурентов подтверждают WTP: Agiloft стартует от $25 000 в год, HyperStart от $79 за пользователя в месяц, AI-Юрист в РФ от 990 ₽ в месяц. На рынке уже виден платный диапазон от B2C/SMB до enterprise. [T1][T2]
- Profit Gate проходит не в low-ticket ботах, а в enterprise implementation + managed service модели. При 4-6 аккаунтах с чеком около 6 млн ₽ в год EBITDA >500 тыс. ₽ в месяц достижима; при модели только дешёвого бота или only-per-document review, как правило, нет. [T1][T2][inference]

## 1) Demand signals

### Internal demand check, 24.04.2026
- `contract intelligence` → `LOW`, `hh_ru=9`, `habr_articles=2`, `yandex_suggest=2`. [T2]
- `contract review ai` → `LOW`, `hh_ru=3`, `habr_articles=2`, `yandex_suggest=2`. [T2]
- `contract lifecycle management` → `LOW`, `hh_ru=10`, `habr_articles=2`, `yandex_suggest=100`. [T2]
- `согласование договоров ai` → `LOW`, `hh_ru=130`, `habr_articles=2`, `yandex_suggest=2`. [T2]

### Интерпретация
- Exact label почти не сформирован в массовом русскоязычном спросе. Это плохой сигнал для self-serve SaaS. [T2][inference]
- Но наличие 130 HH-вакансий по proxу `согласование договоров ai` и 100-балльного Yandex suggest по `contract lifecycle management` показывает, что контур pain живой: согласование, контроль, маршрутизация и review договоров уже являются реальной функцией в компаниях. [T1][T2][inference]
- Следовательно, спрос в РФ надо читать не как «люди ищут contract intelligence», а как «компании уже тратятся на договорный поток и готовы платить за ускорение и снижение риска». [T2][inference]

## 2) Category proof
1. SpotDraft, по данным TechCrunch, имеет 700+ клиентов, 1+ млн контрактов в год и растёт на 100% г/г. Это сильный признак того, что AI-first contract review уже коммерчески доказан как отдельный слой, а не только feature. [T2]
2. Luminance, по данным TechCrunch и продуктового позиционирования, работает с 700+ клиентами в 70+ странах и продаёт AI-review / redlining в enterprise legal workflows. [T2]
3. Crosby, по Forbes, продаёт AI-юрсервис по фиксированной цене $250-1000 за контракт. Это прямое proof of willingness to pay за единичный договорный workflow. [T2]

## 3) Real competitors with prices
По курсу ЦБ РФ на 24.04.2026: 1 USD = 74,8349 ₽, 1 EUR = 87,5261 ₽. [T1]

| Конкурент | Что продаёт | Публичная цена | Цена в ₽ | Вывод |
|---|---|---:|---:|---|
| Agiloft | CLM / contract operations platform | от $25 000 в год [T2] | ≈ 1,87 млн ₽/год [T1+T2] | Нижняя публичная планка enterprise CLM budget |
| HyperStart | AI contract lifecycle management | от $79 за пользователя в месяц [T2] | ≈ 5 912 ₽/польз./мес [T1+T2] | Подтверждает SaaS-seat модель для legal/procurement |
| AI-Юрист | РФ AI-юрист / проверка документов, web + Telegram | от 990 ₽/мес, 4 990 ₽/мес и 15 990 ₽/мес [T2] | 990-15 990 ₽/мес [T2] | Локальный low-ticket платный спрос существует |
| Crosby | AI-assisted contract review service | $250-1000 за контракт [T2] | ≈ 18,7-74,8 тыс. ₽ за контракт [T1+T2] | Buyer готов платить per-document за скорость и точность |

### Read-through по pricing stack
- Рынок уже показывает 3 рабочих модели монетизации: seat-based SaaS, annual enterprise platform и fixed-fee / per-contract service. [T2]
- Это важно для кейса, потому что отдельная service line может заходить через review-as-a-service, а потом расти в managed contract operations и policy automation. [T2][inference]

## 4) Telegram bots / services in RU
- Internal demand endpoint по всем ключам показывает `telegram subscribers=0`, то есть массового Telegram-native category лидера по contract intelligence в РФ не видно. [T2]
- При этом в РФ есть смежные AI-юрист сервисы с Telegram surface. AI-Юрист продаёт тарифы для проверки документов и позиционируется как AI-юрист / консультационный сервис, в том числе через мессенджерный entry-point. [T2]
- Вывод: Telegram в этом кейсе годится как acquisition / lightweight intake channel для SMB и частных кейсов, но не как core delivery surface для enterprise contract ops. Для enterprise value всё равно нужны Word, DMS, ERP, почта, approval flows и audit trail. [T2][inference]

## 5) WTP, proof of willingness to pay
- **Proof 1:** Agiloft публично показывает вход от $25 000 в год, то есть enterprise buyer уже принимает семизначный рублёвый annual spend на contract lifecycle tooling. [T1][T2]
- **Proof 2:** HyperStart показывает seat-pricing от $79/польз./мес, что подтверждает готовность платить за регулярный операционный доступ, а не только за проект внедрения. [T1][T2]
- **Proof 3:** Crosby продаёт AI-review по $250-1000 за контракт, значит даже unit-level workflow monetizable. [T1][T2]
- **Proof 4:** SpotDraft и Luminance имеют сотни клиентов, то есть willingness to pay подтверждён не только прайсом, но и масштабом коммерческого принятия. [T2]
- **Итог:** willingness to pay = **MEDIUM-HIGH** в enterprise и **LOW-MEDIUM** в массовом Telegram/B2C сегменте. [T2][inference]

## 6) Market sizing

### Методика
Считаю двумя путями и беру консервативное значение. Для top-down использую рынок СЭД/ECM/контент-сервисов в РФ как ближайший денежный контур, внутри которого contract intelligence является подкатегорией. [T2][inference]

### Top-down
- TAdviser оценивал рынок СЭД, ECM и CSP в РФ в 22,1 млрд ₽ по итогам 2024 года. [T2]
- По глобальным secondary estimates CLM как специализированный слой существенно уже общего document/ECM software; для консервативной модели беру адресуемую долю 12% от российского ECM-контура. Это даёт **TAM РФ = 2,65 млрд ₽**. [T2][T3][inference]
- Из TAM отсекаю SMB, госархивные use-cases и некритичные document-flow сценарии. Для новой команды реалистично адресуем only mid-market / large B2B / regulated buyers, то есть 40% TAM. Получаем **SAM top-down = 1,06 млрд ₽**. [T2][inference]
- **SOM Y1 top-down = 2% SAM = 21,2 млн ₽**. [inference]
- **SOM Y3 top-down = 7% SAM = 74,3 млн ₽**. [inference]

### Bottom-up
- **Total buyers = 800** компаний: крупные банки, страховые, ритейл, промышленные холдинги, телеком, фарма, IT и B2B-services компании, где договорный поток материален и есть центральные legal/procurement teams. Это консервативный ICP universe на основе крупнейших корпоративных покупателей и enterprise сегмента РФ. [T2][inference]
- **% with need = 20%**, то есть **160 компаний**. Обоснование: HH proxy по согласованию договоров, зрелость CLM-категории и импортозамещённый ECM-контур показывают, что не весь enterprise готов покупать AI-layer сразу, но часть рынка имеет явную боль. [T1][T2][inference]
- **ARR avg = 6 млн ₽/год**. Логика: базовый software/AI слой находится на уровне 1,9 млн ₽+ по публичному enterprise price floor, а вместе с настройкой playbooks, policy layer, integration и support годовой аккаунт выходит к 4-8 млн ₽; для модели беру 6 млн ₽. [T1][T2][inference]
- **SAM bottom-up = 160 × 6 млн ₽ = 960 млн ₽**. [T1][T2][inference]
- **SOM Y1 bottom-up = 4 клиента × 6 млн ₽ = 24 млн ₽**. [inference]
- **SOM Y3 bottom-up = 12 клиентов × 6 млн ₽ = 72 млн ₽**. [inference]

### 10 реальных buyers для GTM-base
1. Сбер [T2]
2. ВТБ [T2]
3. Альфа-Банк [T2]
4. Т-Банк [T2]
5. Ростелеком [T2]
6. МТС [T2]
7. X5 Group [T2]
8. Магнит [T2]
9. Северсталь [T2]
10. Самолет [T2]

### Reconciliation table
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | ~$1,62 млрд CLM market [T3] | — | — | top-down |
| TAM (РФ) | 2,65 млрд ₽ [T2+T3+inference] | 4,80 млрд ₽ = 800 × 6 млн ₽ [inference] | diff=1,8x, т.к. bottom-up считает весь buyer universe до фильтра боли | lower |
| SAM (РФ) | 1,06 млрд ₽ [T2+inference] | 0,96 млрд ₽ [T1+T2+inference] | diff≈10%, допустимо | lower |
| SOM Y1 | 21,2 млн ₽ | 24,0 млн ₽ | diff≈13% | **используем 21,2 млн ₽** |
| SOM Y3 | 74,3 млн ₽ | 72,0 млн ₽ | diff≈3% | **используем 72,0 млн ₽** |

### Sanity checks
- Расхождение top-down и bottom-up по SAM меньше 3x, модель допустима. [T2][inference]
- SOM Y1 меньше 10% SAM, overclaiming нет. [inference]
- При среднем цикле сделки 6-9 месяцев SOM Y1 на 4 клиента выглядит тяжёлым, но достижимым для founder-led enterprise motion; агрессивнее брать уже опасно. [T2][inference]

## 7) Profit Gate, EBITDA >= 500K ₽/mo
Проверяю все основные сценарии.

### Scenario A, Telegram / low-ticket AI-юрист
- Чек 1-16 тыс. ₽/мес по рынку локальных сервисов. [T2]
- Даже при сотнях пользователей экономика быстро упирается в support, acquisition и слабую дифференциацию. [T2][inference]
- **Profit Gate: FAIL.**

### Scenario B, per-contract review service
- Unit pricing подтверждён на уровне ~18,7-74,8 тыс. ₽ за контракт. [T1][T2]
- Модель может быть прибыльной как boutique service, но для устойчивых 500K+ EBITDA в месяц нужен постоянный большой поток review, а без software attach это операционно хрупко. [T2][inference]
- **Profit Gate: BORDERLINE / чаще FAIL как standalone.**

### Scenario C, enterprise implementation + managed contract ops
- Годовой чек около 4-8 млн ₽ на аккаунт выглядит правдоподобно на фоне публичного price floor и required delivery. [T1][T2][inference]
- При 4-6 активных клиентах годовая выручка 24-48 млн ₽. При валовой марже 40-50% и фиксированных расходах 0,8-1,2 млн ₽/мес EBITDA >500 тыс. ₽/мес достижима. [T1][T2][inference]
- **Profit Gate: PASS.**

### Scenario D, platform + legal/procurement policy layer
- Добавление clause playbooks, approval policies, redlining rules и exception routing повышает ACV и удержание. [T2][inference]
- При 6-10 аккаунтах это уже может быть сильнее обычного консалтинга и ближе к repeatable productized service. [T2][inference]
- **Profit Gate: PASS WITH RESERVATIONS.**

## 8) Risks
- В РФ нет сильного публичного category pull по exact label, поэтому education cost и sales cycle будут высокими. [T2]
- Telegram не решает core-enterprise delivery, а значит distribution придётся строить через direct sales, партнёров и Word/DMS/ERP интеграции. [T2][inference]
- Если продукт не переводит redlining и approvals в repeatable policy engine, кейс деградирует в кастомный legal outsourcing. [T2][inference]
- Global category валидна, но локальная адаптация упирается в языковые нюансы, доверие к AI-review и требования к auditability. [T2][inference]

## 9) Decision
**Статус: CONDITIONAL PASS.**

Почему не early reject:
1. Demand API даёт `LOW`, но не ноль по proxy-pain, особенно по русскому договорному workflow. [T2]
2. WTP подтверждён одновременно публичными enterprise ценами, per-contract ценой и локальными paid AI-юрист сервисами. [T1][T2]
3. Profit Gate проходит в сценариях enterprise implementation + managed contract operations. [T1][T2][inference]

Что делать дальше на следующих стадиях:
- проверить repeatability против «юристы вручную + шаблоны»;
- зафиксировать ICP, где договорный поток действительно стратегический, банки / enterprise procurement / девелоперы / телеком / промышленность;
- валидировать, насколько сильна интеграционная зависимость от Microsoft Word, DMS и ERP. [T2][inference]

## Источники
- [T1] Банк России, курсы валют на 24.04.2026: https://www.cbr.ru/scripts/XML_daily.asp
- [T2] Internal demand endpoint, 24.04.2026: http://172.18.0.1:9001/multi-demand?keyword=contract%20intelligence ; http://172.18.0.1:9001/multi-demand?keyword=contract%20review%20ai ; http://172.18.0.1:9001/multi-demand?keyword=contract%20lifecycle%20management ; http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%BE%D0%B2%20ai
- [T2] TechCrunch, SpotDraft signal, 2026-01-26: https://techcrunch.com/2026/01/26/qualcomm-backs-spotdraft-to-scale-on-device-contract-ai-with-valuation-doubling-toward-400m/
- [T2] TechCrunch, Luminance signal, 2025-02-18: https://techcrunch.com/2025/02/18/legal-ai-startup-luminance-Backed-by-the-late-mike-lynch-raises-75m/
- [T2] Forbes, Crosby pricing signal, 2026-03-31: https://www.forbes.com/sites/rashishrivastava/2026/03/31/why-this-ai-law-firm-is-ditching-the-billable-hour/
- [T2] Agiloft pricing: https://www.agiloft.com/pricing/
- [T2] HyperStart pricing: https://www.g2.com/products/hyperstart/reviews
- [T2] AI-Юрист тарифы: https://ai-urist.ru/blog/tag/nejroseti-v-yurisprudencii/
- [T2] TAdviser, рынок СЭД/ECM/CSP в РФ, 2024: https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F:%D0%A1%D0%AD%D0%94_(%D1%80%D1%8B%D0%BD%D0%BE%D0%BA_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8)
- [T3] Grand View Research, CLM market size: https://www.grandviewresearch.com/industry-analysis/contract-lifecycle-management-software-market-report

Sources: T1=1, T2=8, T3=1. Primary evidence basis: T2.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-05-10: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.


---

# FILE: 03-solution.md

---
stage: solution
case: workday-contract-intelligence-negotiation-agents-v2
date: 2026-05-10
analyst: branch-models-lead
sector: LEGAL
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Workday Contract Intelligence + Contract Negotiation Agent как service-led слой для enterprise contract operations: intake, review, redlining, approvals, clause governance, repository cleanup, obligation tracking и managed-оптимизация договорного контура.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Workday уже оформил категорию не как «ещё один AI-ассистент», а как полноценный CLM-контур с AI-driven drafting, negotiation, redlining, approvals, search и integrations. Это делает кейс самостоятельным operational wedge. [T1]
2. Для локального рынка правдоподобный продукт, не перепродажа Workday как софта, а дорогой service layer поверх contract workflow: внедрение playbooks, migration/normalization контрактов, policy setup, routing exception cases и ongoing governance. [T1][T2][inference]
3. Solution-fit есть прежде всего у enterprise-клиентов с большим договорным портфелем и cross-functional owner'ами между legal, procurement, finance и sales ops. [T1][T2][inference]
4. Главный риск, кейс легко деградирует в кастомный legal outsourcing или SI-проект, если не удержать 2-3 повторяемых workflow wedge и measurable KPI. [inference]

## 1. Какую проблему реально решает продукт

Клиент покупает не «AI для юристов вообще», а устранение конкретных дорогих потерь:
- долгий review и redlining договоров;
- хаос в clause library и шаблонах;
- ручную маршрутизацию согласований между legal, procurement, sales и finance;
- слабую видимость obligations, рисков и условий по историческому контрактному массиву;
- дорогую зависимость от senior legal team для first-pass анализа;
- отсутствие единого audit-friendly contract workflow.

У Workday это подтверждается на уровне продукта: CLM обещает end-to-end AI workflows, automated redlining, clause library, negotiation support, approvals и integrations с Box, SharePoint и Salesforce. [T1]

## 2. Продуктовый wedge

### Core wedge
**Contract operations operator для enterprise**
- аудит текущего договорного потока;
- очистка и структурирование contract repository;
- настройка clause playbooks и review policies;
- запуск intake-to-approval workflow;
- AI-assisted review / redlining / negotiation;
- obligation tracking и search across legacy contracts;
- managed optimization по cycle time, touch time и risk reduction.

### Почему это сильнее обычного CLM-внедрения
1. **Есть реальный workflow, а не только storage.** Workday прямо продаёт drafting, negotiation, approval и contract analysis как единую AI-native цепочку. [T1]
2. **Есть ценность на историческом массиве.** Workday Legal как customer zero заявляет 100 000 контрактов, 45 000 часов экономии в квартал и 3 500% ROI, то есть value появляется не только в новых договорах, но и в existing repository. [T1]
3. **Есть recurring слой.** После initial setup остаются playbook tuning, governance, exception handling, retraining rules, rollout на новые contract types и новые функции. [T1][T2][inference]
4. **Категория подтверждена вне Workday.** SpotDraft и Luminance показывают, что contract review и redlining уже живут как самостоятельный коммерческий слой, а не как уникальная аномалия одного вендора. [T2]

## 3. Для кого solution-fit реален в РФ

### Primary ICP
- крупные банки и страховые;
- enterprise procurement и shared services центры;
- девелоперы, телеком, industrial и retail группы с большим объёмом supplier/customer contracts;
- компании с сильным sales/legal handoff и большим объёмом MSA/SOW/NDA/закупочных договоров;
- холдинги, где уже есть DMS/SharePoint/Box-подобный архив, но слабая извлекаемость данных и медленный approval flow.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. крупный контрактный массив и заметный backlog на review/search/renewals;
2. owner на уровне CLO, head of legal ops, procurement director, CFO-1, COO или revenue operations leader;
3. готовность покупать не только разовую автоматизацию, но и governance + managed optimization;
4. несколько повторяемых contract types, где можно стандартизировать playbooks;
5. реальная цена задержек, ошибок и missed obligations.

### Нецелевой сегмент
- SMB с редким договорным потоком;
- компании, где договоры живут в email и Word без зрелого owner'а процесса;
- клиенты, которым нужен только «чат с документом»;
- команды, где дешевле нанять ещё одного юриста, чем менять operating model.

## 4. Как продукт должен выглядеть в локальном GTM

### Слабое позиционирование
- «внедрим AI для договоров»;
- продажа generic legal copilot;
- упор на западный бренд без локального workflow pain;
- попытка продавать только seat-based tool без ownership за процесс.

### Реалистичное позиционирование
- вход через один дорогой процесс: procurement contracts, sales contracting, renewals/obligations или repository intelligence;
- pilot на 6-10 недель;
- KPI pilot: turnaround time, touch time юристов, time-to-signature, % first-pass review, backlog reduction, % searchable contracts, obligation visibility;
- после pilot переход в retainer на policy tuning, workflow governance и rollout на новые contract types.

## 5. Delivery model

### Правдоподобная схема внедрения
1. discovery и baseline по contract workflow;
2. выбор одного wedge с понятным owner'ом;
3. импорт и нормализация исторических договоров;
4. настройка clause library, review rules, approval routing и negotiation guardrails;
5. pilot с human-in-the-loop;
6. KPI review через 6-10 недель;
7. rollout на соседние типы договоров и функции;
8. managed optimization на постоянной основе.

### Кто должен быть buyer'ом
- CLO / head of legal;
- head of legal operations;
- procurement director;
- CFO-1 / COO при сильном procurement или sales contract pain;
- CIO / head of enterprise applications при крупной трансформации документооборота.

### Кто редко будет настоящим buyer'ом
- отдельный юрист без бюджета и process ownership;
- IT без legal/procurement sponsor'а;
- SMB owner, которому нужен разовый review нескольких договоров.

## 6. Почему клиент купит это, а не альтернативы

У клиента уже есть substitutes:
- юристы вручную + шаблоны в Word;
- DMS/ЭДО без intelligence layer;
- разовые внешние review-сервисы;
- generic LLM tools без governance и audit trail;
- локальные low-ticket AI-юрист сервисы.

Кейс выигрывает только если предложение доказывает четыре вещи:
1. быстрее сокращает cycle time договора, чем ручной legal process;
2. даёт visibility по историческому портфелю, а не только помощь в создании новых договоров;
3. превращает review policies и clause standards в repeatable playbooks;
4. оставляет recurring managed layer после initial deployment.

Если этого нет, buyer рационально останется на сочетании Word, шаблонов, DMS и внешних юристов.

## 7. Конкурентная позиция

### Против low-ticket AI-юристов
Преимущество в том, что enterprise buyer покупает не «проверку документа», а управляемый contract operating system с approvals, repository intelligence и governance. [T1][T2][inference]

### Против обычных CLM-платформ
Шанс есть, если сервисный слой берёт на себя реальный rollout, playbook design, migration и ongoing optimization, а не просто внедряет коробку. [T1][inference]

### Против внешних юристов
Преимущество возникает, если first-pass review, поиск clauses и obligations становятся быстрее, дешевле и измеримее, при сохранении lawyer-in-the-loop для high-risk случаев. [T1][T2][inference]

## 8. Основные риски solution-fit

1. **SI-risk.** Каждый enterprise-клиент может требовать слишком много bespoke integration и cleanup legacy repository.
2. **Legal outsourcing risk.** Без productized playbooks кейс скатится в дорогой ручной review.
3. **Long-cycle risk.** Продажа legal/procurement transformation в enterprise идёт медленно.
4. **Trust / auditability risk.** Для high-risk contracts buyer потребует explainability, approval logs и контроль ошибок.
5. **Localization risk.** Англоязычная CLM-логика не всегда напрямую переносится на локальные contract templates и практики.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько стоит pilot и последующий retainer;
- какой delivery team нужен на 1 enterprise-клиента;
- можно ли удержать gross margin, если требуется много senior legal ops труда;
- сколько клиентов нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не превращается ли лучшая версия кейса в консалтинг/body shop без repeatable recurring revenue.

## Итог для пайплайна

**P4 пройден условно.**

Кейс жив как enterprise contract operations operator, а не как ещё один legal AI tool. Имеет смысл идти дальше только если на economics подтвердятся высокий ACV, шаблонный rollout и повторяемый managed layer поверх contract workflows.

## Источники
- [T1] Workday Contract Lifecycle Management: https://www.workday.com/en-us/products/contract-management/contract-lifecycle-management.html
- [T1] Workday Contract Intelligence: https://www.workday.com/en-in/products/contract-management/contract-intelligence.html
- [T1] Workday Legal customer story: https://www.workday.com/en-us/customer-stories/q-z/workday-legal-customer-zero-contract-intelligence.html
- [T1] Workday newsroom, EU data residency and Contract Intelligence Agent / Contract Negotiation Agent, 2026-02-26: https://newsroom.workday.com/2026-02-26-Workday-Brings-AI-Native-Contract-Lifecycle-Management-to-EU-Businesses-with-Frankfurt-Data-Residency
- [T2] SpotDraft VerifAI: https://www.spotdraft.com/verifai
- [T2] TechCrunch, SpotDraft signal: https://techcrunch.com/2026/01/26/qualcomm-backs-spotdraft-to-scale-on-device-contract-ai-with-valuation-doubling-toward-400m/
- [T2] TechCrunch, Luminance signal: https://techcrunch.com/2025/02/18/legal-ai-startup-luminance-Backed-by-the-late-mike-lynch-raises-75m/
- [T2] Forbes, Crosby signal: https://www.forbes.com/sites/rashishrivastava/2026/03/31/why-this-ai-law-firm-is-ditching-the-billable-hour/

> Market Pulse 2026-05-10: solution-fit выглядит правдоподобно как enterprise contract operations layer с AI-review, negotiation и governance, но не как массовый self-serve legal bot.


---

# FILE: 04-economics.md

---
stage: economics
case: workday-contract-intelligence-negotiation-agents-v2
date: 2026-05-11
analyst: branch-models-lead
sector: LEGAL
verdict: PASS_WITH_RESERVATIONS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## 1. Executive summary

**Итог P5: PASS WITH RESERVATIONS.**

Кейс собирается только как **enterprise contract operations layer** с pilot, repository cleanup, clause playbooks, approval-routing и ограниченным managed-оптимизационным слоем. Вариант cheap seat-SaaS или per-document review без platform-retainer экономику не держит.

Базовый operating-case:
- **MRR на клиента:** **650 000 ₽/мес**
- **Setup / onboarding fee:** **2 500 000 ₽**
- **COGS:** **285 000 ₽/клиент/мес**
- **Gross profit:** **365 000 ₽/клиент/мес**
- **Gross margin:** **56,2%**
- **Blended fully-loaded CAC:** **1 050 000 ₽**
- **Annual logo churn:** **18%**
- **Base LTV:** **24,4 млн ₽**
- **Stress LTV/CAC:** **3,8x**
- **CAC payback:** **1,6 мес по MRR** или **2,9 мес по gross profit**
- **Operating payback:** **6,7 мес**
- **Break-even:** **18-20 клиентов**
- **EBITDA при 50 клиентах:** **~5,5 млн ₽/мес**

Вывод: economics проходит program gate, но запас прочности средний. Модель держится на high-ticket ACV, стандартизированном rollout и контроле legal/service creep.

## 2. Ключевые допущения модели

### ICP
- крупные банки, страховые, телеком, industrial и retail-группы;
- enterprise legal / procurement teams с большим договорным портфелем;
- buyer уровня CLO, head of legal ops, procurement director, COO/CFO-1;
- компании, где цена медленного согласования и слабого repository visibility действительно материальна.

### Почему беру чек 650k ₽/мес
Опора на предыдущие стадии:
- в `02-demand.md` уже зафиксирован публичный enterprise floor у Agiloft около **1,87 млн ₽/год**, а также seat/pricing proof у HyperStart и per-contract monetization у Crosby;
- в `03-solution.md` кейс живёт не как solo legal tool, а как workflow layer с migration, playbooks, governance и recurring optimization.

Для локального base-case беру:
- **650 000 ₽/мес recurring** за software + workflow governance + managed optimization;
- **2,5 млн ₽ one-time setup** за pilot, migration/normalization, clause library и approval logic.

Это выше low-end legal AI, но заметно ниже тяжёлого multi-million CLM transformation. Для РФ такой чек выглядит правдоподобно только при продаже в cross-functional legal/procurement workflow, а не как «чат с договором».

## 3. Business process: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Target-account mapping по enterprise legal/procurement | SDR | CRM, реестры, ручной research | 2,0 ч | 2 400 | Низкая |
| 2 | Первый outbound / intro | SDR | email, phone, Telegram, CRM | 1,5 ч | 1 900 | Средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1,0 ч | 3 400 | Средняя |
| 4 | Discovery contract workflow | AE + founder | discovery template, call notes | 2,0 ч | 10 500 | Низкая |
| 5 | Demo review / redlining / repository intelligence | AE + solutions legal | demo workspace | 2,0 ч | 12 500 | Низкая |
| 6 | Pilot scoping и KPI design | AE + solutions + CSM | ROI sheet, SOW | 3,0 ч | 17 000 | Низкая |
| 7 | Security / privacy / procurement review | CTO + founder | checklist, security pack | 4,0 ч | 21 000 | Низкая |
| 8 | Repository cleanup + clause playbooks setup | implementation + solutions legal | KB, templates, workflow rules | 20 ч | 86 000 | Низкая |
| 9 | Pilot 6-10 недель | CSM + solutions legal | weekly reviews, QA, reporting | 16 ч | 61 000 | Средняя |
| 10 | Contracting / procurement | AE + founder + legal | ЭДО, договоры, redlines | 8 ч | 31 000 | Низкая |
| 11 | Launch / invoicing | ops + CSM | ЭДО, billing, runbook | 2 ч | 5 500 | Высокая |

**Direct pre-sale + onboarding cost на нового клиента: ~252 200 ₽.** Основной CAC создаётся не этим direct cost, а длинным enterprise sales motion, SDR/AE/FOT и partner/community overhead.

## 4. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / document inference / extraction / redlining | 42 000 | document-heavy legal workflow |
| Secure hosting / storage / logs | 33 000 | изоляция, хранение файлов, аудит |
| CSM / account operations | 28 000 | adoption, usage review, QBR |
| Solutions legal oversight | 74 000 | playbook tuning, exception review |
| Implementation amortization | 56 000 | часть setup spread на 12 мес |
| Support / ticketing / minor customization | 24 000 | run support и workflow tweaks |
| Security / compliance allocation | 16 000 | questionnaires, policy upkeep |
| Reporting / analytics | 12 000 | KPI-reporting и operational review |
| **Итого COGS** | **285 000** |  |

### Выручка и маржа
- MRR на клиента: **650 000 ₽**
- COGS на клиента: **285 000 ₽**
- Gross profit: **365 000 ₽**
- **Gross Margin = 56,2%**

Комментарий: маржа нормальная для software-plus-legal-ops слоя, но заметно ниже классического SaaS. Это допустимо, пока solutions legal не становится главным delivery-двигателем.

## 5. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 16 | 7 | 5 | 2 | 0,8 | 5,0% |
| Outbound ABM | 110 | 14 | 7 | 3 | 0,9 | 0,8% |
| Content / events / legal community | 26 | 7 | 4 | 1 | 0,4 | 1,5% |
| Partner / SI / legal referrals | 10 | 4 | 3 | 1 | 0,3 | 3,0% |
| **Итого blended** | **162** | **32** | **19** | **7** | **2,4** | **1,5%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid / category marketing | 180 000 | capture demand + retargeting |
| Outbound team FOT | 980 000 | 2 SDR + 1 AE + бонусы / налоги |
| Marketing allocation | 180 000 | content / legal community / webinars |
| Tools / CRM / enrichment / call stack | 110 000 | sales stack + ops tooling |
| Events / partner enablement | 190 000 | roundtables, referrals, enablement |
| Overhead multiplier (x1,4) | 880 000 | management / ops / enterprise friction |
| **Итого acquisition spend** | **2 520 000 ₽/мес** |  |

- New paying customers / мес: **2,4**
- **Blended fully-loaded CAC = 2 520 000 / 2,4 = 1 050 000 ₽**

### Sanity check
CAC выше обычного B2B SaaS, но это логично: здесь legal/procurement motion, pilot, security review и category education. Ниже 700k ₽ такой enterprise sale выглядел бы заниженным.

## 6. LTV и churn

### Допущения
- MRR: **650 000 ₽**
- ARR: **7 800 000 ₽**
- Gross Margin: **56,2%**
- Annual logo churn: **18%**

`LTV = ARR × GM / annual churn`

`LTV = 7 800 000 × 56,2% / 18% = 24 353 333 ₽`

### Operating/stress adjustment
Формальный base-case слишком красивый для новой локальной LEGAL категории. Для decision добавляю stress-layer:
- effective ARR = **6 600 000 ₽**,
- effective GM = **42%**,
- effective annual churn = **30%**.

`Stress LTV = 6 600 000 × 42% / 30% = 9 240 000 ₽`

### Вывод
- **Base LTV = 24,35 млн ₽**
- **Stress LTV = 9,24 млн ₽**

Для решения ориентируюсь именно на stress-case.

## 7. LTV/CAC

- Stress LTV: **9 240 000 ₽**
- CAC: **1 050 000 ₽**

`Stress LTV/CAC = 9 240 000 / 1 050 000 = 8,8x`

Чтобы не переоценить кейс, добавляю ещё более жёсткий downside-view, где:
- effective ARR = **5 400 000 ₽**,
- effective GM = **37%**,
- effective annual churn = **50%**.

`Downside LTV = 5 400 000 × 37% / 50% = 3 996 000 ₽`

`Downside LTV/CAC = 3 996 000 / 1 050 000 = 3,8x`

### Вердикт по метрике
Для decision-level realism беру **downside-view = 3,8x**. Это выше required `3,0x`, но без большого запаса.

## 8. CAC Payback

`CAC Payback = 1 050 000 / 650 000 = 1,62 мес`

По gross profit:

`Gross profit payback = 1 050 000 / 365 000 = 2,88 мес`

Operating payback, если effective contribution первого года ближе к **156 000 ₽/клиент/мес** после extra service load:

`Operating payback = 1 050 000 / 156 000 = 6,73 мес`

### Вывод
Для investment decision релевантно именно **~6,7 мес**. Это ещё приемлемо для enterprise legal/procurement motion.

## 9. Contribution Margin %

- Revenue per client / мес: **650 000 ₽**
- COGS: **285 000 ₽**
- Variable commissions + success support: **44 000 ₽**

`Contribution profit = 321 000 ₽`

`Contribution Margin = 321 000 / 650 000 = 49,4%`

Это достаточный уровень, если legal escalation-rate остаётся под контролем.

## 10. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire | Ramp до 80% | +30% взносы | FOT fully-loaded ₽/мес |
|---|---:|---:|---|---|---:|---:|
| CEO / founder | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / platform lead | 1 | 520 000 | 2 мес | 2 мес | 156 000 | 676 000 |
| Backend / workflow engineer | 2 | 360 000 | 1,5 мес | 1,5 мес | 108 000 | 936 000 |
| Solutions legal | 1 | 340 000 | 1,5 мес | 1 мес | 102 000 | 442 000 |
| Implementation / legal ops specialist | 1 | 260 000 | 1 мес | 1 мес | 78 000 | 338 000 |
| CSM | 1 | 230 000 | 1 мес | 1 мес | 69 000 | 299 000 |
| SDR | 2 | 160 000 + бонус | 1 мес | 1 мес | 48 000 | 416 000 |
| AE | 1 | 310 000 + комиссия | 1,5 мес | 2 мес | 93 000 | 403 000 |
| Marketing / community | 1 | 190 000 | 1 мес | 1 мес | 57 000 | 247 000 |
| Finance / ops | 0,5 | 120 000 | 0,5 мес | 0,5 мес | 36 000 | 156 000 |
| **Итого full team FOT** | **11,5** |  |  |  |  | **4 758 000 ₽/мес** |

Комментарий: команда остаётся умеренной. Если для каждого нового клиента нужен отдельный senior legal bench, модель быстро съедает margin.

## 11. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 4 758 000 |
| Core infra not in COGS | 240 000 |
| Security / legal / compliance retainers | 170 000 |
| G&A / admin / ЭДО / bank | 95 000 |
| Travel / enterprise meetings | 85 000 |
| **Итого fixed costs** | **5 348 000 ₽/мес** |

## 12. Break-even

### Break-even по числу клиентов
- Contribution profit per client / мес: **321 000 ₽**
- Fixed costs: **5 348 000 ₽/мес**

`Contribution break-even clients = 5 348 000 / 321 000 = 16,7`

С учётом резерва на discounts, custom work и longer pilot-to-rollout беру **operating break-even = 18-20 клиентов**.

## 13. EBITDA при 50 клиентах

| Метрика | Значение |
|---|---:|
| Клиентов | 50 |
| Выручка | 32 500 000 ₽/мес |
| COGS | 14 250 000 ₽/мес |
| Gross profit | 18 250 000 ₽/мес |
| Variable commissions / success support | 2 200 000 ₽/мес |
| Contribution profit | 16 050 000 ₽/мес |
| Fixed costs | 5 348 000 ₽/мес |
| **EBITDA** | **10 702 000 ₽/мес** |

### Консервативный operating view
С учётом price pressure, longer onboarding и extra legal ops runtime operating EBITDA может быть ближе к **5,5-6,5 млн ₽/мес**.

### Проверка правила
Требование программы, **EBITDA > 500k ₽/мес** в правдоподобной конфигурации, проходит уверенно.

## 14. Burn-to-breakeven и runway

- Fixed costs: **5,35 млн ₽/мес**
- Acquisition spend: **2,52 млн ₽/мес**
- Total burn до заметной выручки: **~7,87 млн ₽/мес**

Если стартовый капитал **95 млн ₽**, nominal runway около:

`95 / 7,87 ≈ 12,1 мес`

Это не лёгкая модель. Она терпима только при founder-led продажах, стандартизированном pilot и отсутствии глубокого SI-drift.

## 15. Итоговый вердикт P5

**PASS WITH RESERVATIONS.**

Почему:
1. Кейс проходит `Profit Gate`, потому что при реалистичном ACV и контролируемом service load выходит заметно выше `+500k ₽/мес`.
2. Даже downside-view даёт **LTV/CAC ~3,8x**, то есть выше порога `3,0x`, но запас не огромный.
3. **Operating payback ~6,7 мес** остаётся приемлемым для enterprise legal motion.
4. Главная угроза, repository cleanup, clause tuning и exception handling могут превратить продукт в service-heavy legal ops бизнес.

## 16. Что могло бы ухудшить решение до reject

Кейс стоило бы резать, если подтвердится хотя бы один из тезисов:
- реальный ACV застревает ближе к **350-450k ₽/мес**;
- effective GM уходит **ниже 35%**;
- buyer universe и conversion не позволяют дойти хотя бы до **18+ активных клиентов** без CAC-срыва;
- post-sale delivery требует слишком много senior legal времени на каждый аккаунт.

## Основание
- `02-demand.md`
- `03-solution.md`
- Workday CLM / Contract Intelligence pages [T1]
- SpotDraft / Luminance / Crosby category evidence [T2]
- Публичные price signals Agiloft / HyperStart / AI-Юрист из `02-demand.md`

<!-- P5-DONE -->


---

# FILE: 05-critic.md

# SECTION A. Finance PnL
## A1. Входные данные и допущения
- ARPA: **650 000 ₽/клиент/мес**.
- COGS на клиента: **285 000 ₽/клиент/мес**.
- Gross profit на клиента: **365 000 ₽/клиент/мес**.
- Contribution profit на клиента: **321 000 ₽/клиент/мес**.
- Fixed costs: **5 348 000 ₽/мес**, из них team FOT **4 758 000 ₽/мес**.
- CAC по каналам: founder-led **~1 050 000 ₽ blended fully-loaded**, каналовый funnel enterprise-heavy; в PnL CAC не вычитаю из EBITDA, а использую для sanity-check сценариев роста.
- LTV base: **24,35 млн ₽**, stress/downside LTV/CAC: **3,8x**.
- Страховые взносы **~30% к ФОТ** считаю уже включёнными в FOT и fixed costs.
- НДС **20%** учитываю как фактор cash flow при ОСНО, но PnL ниже построен в ценах **без НДС**, чтобы не искажать операционную маржу.

## A2. Сценарии
- **Base:** new clients = `1,1,2,2,2,2,3,3,3,3,4,4`, churn **1.64%/мес** (эквивалент annual churn 18%).
- **Optimistic:** new clients = `1,2,2,2,3,3,4,4,4,4,5,5`, churn **1,20%/мес**.
- **Pessimistic:** new clients = `0,1,1,1,1,2,2,2,2,2,2,3`, churn **2,50%/мес**.
- Формула активной базы: `Total clients_t = Total_(t-1) × (1 - churn) + New clients_t`.
- Cash burn = `max(0, -EBITDA)`. Cumulative cash стартует с **0 ₽** и показывает накопленную потребность в стартовом капитале до break-even.

## A3. PnL 12 месяцев, Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 1 | 2 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 4 | 4 |
| Total clients | 1.00 | 1.98 | 3.95 | 5.89 | 7.79 | 9.66 | 12.50 | 15.30 | 18.05 | 20.75 | 24.41 | 28.01 |
| MRR, ₽ | 650 000 | 1 289 339 | 2 568 192 | 3 826 069 | 5 063 316 | 6 280 269 | 8 127 263 | 9 943 963 | 11 730 866 | 13 488 462 | 15 867 229 | 18 206 982 |
| COGS, ₽ | 285 000 | 565 326 | 1 126 053 | 1 677 584 | 2 220 069 | 2 753 657 | 3 563 492 | 4 360 045 | 5 143 534 | 5 914 172 | 6 957 170 | 7 983 061 |
| Gross profit, ₽ | 365 000 | 724 013 | 1 442 138 | 2 148 485 | 2 843 247 | 3 526 613 | 4 563 771 | 5 583 918 | 6 587 333 | 7 574 290 | 8 910 060 | 10 223 920 |
| GM% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% |
| Fixed costs, ₽ | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 |
| EBITDA, ₽ | -4 983 000 | -4 623 987 | -3 905 862 | -3 199 515 | -2 504 753 | -1 821 387 | -784 229 | 235 918 | 1 239 333 | 2 226 290 | 3 562 060 | 4 875 920 |
| Cash burn, ₽ | 4 983 000 | 4 623 987 | 3 905 862 | 3 199 515 | 2 504 753 | 1 821 387 | 784 229 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -4 983 000 | -9 606 987 | -13 512 848 | -16 712 363 | -19 217 116 | -21 038 504 | -21 822 733 | -21 822 733 | -21 822 733 | -21 822 733 | -21 822 733 | -21 822 733 |

- Break-even по client count, EBITDA: **14.65 клиента**.
- Break-even по client count, post-tax: **18.96 клиента на УСН 6%**, **17.74 клиента на IT-льготе 3%**, **20.83 клиента на ОСНО 20%**.
- Break-even month: **M8**.
- startup_capital_to_bep_rub: **21 822 733 ₽**.

## A3. PnL 12 месяцев, Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 1 | 2 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 4 | 5 | 5 |
| Total clients | 1.00 | 2.99 | 4.95 | 6.89 | 9.81 | 12.69 | 16.54 | 20.34 | 24.10 | 27.81 | 32.47 | 37.08 |
| MRR, ₽ | 650 000 | 1 942 200 | 3 218 894 | 4 480 267 | 6 376 504 | 8 249 986 | 10 750 986 | 13 221 974 | 15 663 310 | 18 075 351 | 21 108 446 | 24 105 145 |
| COGS, ₽ | 285 000 | 851 580 | 1 411 361 | 1 964 425 | 2 795 852 | 3 617 301 | 4 713 894 | 5 797 327 | 6 867 759 | 7 925 346 | 9 255 242 | 10 569 179 |
| Gross profit, ₽ | 365 000 | 1 090 620 | 1 807 533 | 2 515 842 | 3 580 652 | 4 632 684 | 6 037 092 | 7 424 647 | 8 795 551 | 10 150 005 | 11 853 204 | 13 535 966 |
| GM% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% |
| Fixed costs, ₽ | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 |
| EBITDA, ₽ | -4 983 000 | -4 257 380 | -3 540 467 | -2 832 158 | -1 767 348 | -715 316 | 689 092 | 2 076 647 | 3 447 551 | 4 802 005 | 6 505 204 | 8 187 966 |
| Cash burn, ₽ | 4 983 000 | 4 257 380 | 3 540 467 | 2 832 158 | 1 767 348 | 715 316 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -4 983 000 | -9 240 380 | -12 780 847 | -15 613 005 | -17 380 353 | -18 095 669 | -18 095 669 | -18 095 669 | -18 095 669 | -18 095 669 | -18 095 669 | -18 095 669 |

- Break-even по client count, EBITDA: **14.65 клиента**.
- Break-even по client count, post-tax: **18.96 клиента на УСН 6%**, **17.74 клиента на IT-льготе 3%**, **20.83 клиента на ОСНО 20%**.
- Break-even month: **M7**.
- startup_capital_to_bep_rub: **18 095 669 ₽**.

## A3. PnL 12 месяцев, Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 3 |
| Total clients | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 5.76 | 7.61 | 9.42 | 11.19 | 12.91 | 14.58 | 17.22 |
| MRR, ₽ | 0 | 650 000 | 1 283 750 | 1 901 656 | 2 504 115 | 3 741 512 | 4 947 974 | 6 124 275 | 7 271 168 | 8 389 389 | 9 479 654 | 11 192 663 |
| COGS, ₽ | 0 | 285 000 | 562 875 | 833 803 | 1 097 958 | 1 640 509 | 2 169 496 | 2 685 259 | 3 188 127 | 3 678 424 | 4 156 464 | 4 907 552 |
| Gross profit, ₽ | 0 | 365 000 | 720 875 | 1 067 853 | 1 406 157 | 2 101 003 | 2 778 478 | 3 439 016 | 4 083 040 | 4 710 964 | 5 323 190 | 6 285 111 |
| GM% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% | 56.2% |
| Fixed costs, ₽ | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 | 5 348 000 |
| EBITDA, ₽ | -5 348 000 | -4 983 000 | -4 627 125 | -4 280 147 | -3 941 843 | -3 246 997 | -2 569 522 | -1 908 984 | -1 264 960 | -637 036 | -24 810 | 937 111 |
| Cash burn, ₽ | 5 348 000 | 4 983 000 | 4 627 125 | 4 280 147 | 3 941 843 | 3 246 997 | 2 569 522 | 1 908 984 | 1 264 960 | 637 036 | 24 810 | 0 |
| Cumulative cash, ₽ | -5 348 000 | -10 331 000 | -14 958 125 | -19 238 272 | -23 180 115 | -26 427 112 | -28 996 634 | -30 905 619 | -32 170 578 | -32 807 614 | -32 832 423 | -32 832 423 |

- Break-even по client count, EBITDA: **14.65 клиента**.
- Break-even по client count, post-tax: **18.96 клиента на УСН 6%**, **17.74 клиента на IT-льготе 3%**, **20.83 клиента на ОСНО 20%**.
- Break-even month: **M12**.
- startup_capital_to_bep_rub: **32 832 423 ₽**.

## A4. Waterfall на 1 клиента / месяц
| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 650 000 | Recurring выручка |
| Gross | 365 000 | ARPA - COGS (285 000 ₽) |
| Contribution | 321 000 | Gross - variable commissions/success (44 000 ₽) |
| EBITDA | 321 000 | EBITDA contribution до fixed costs; portfolio EBITDA break-even с 14.65 клиента по gross-модели |
| Net, УСН 6% | 282 000 | Налог с выручки 6% |
| Net, IT-льгота 3% | 301 500 | При аккредитации Минцифры и соблюдении criteria |
| Net, ОСНО 20% | 256 800 | Налог на прибыль 20%; НДС 20% сверх этого давит на оборотный капитал |

## A5. Cash flow
- **Base: startup_capital_to_bep_rub = 21 822 733 ₽**; EBITDA break-even month = **M8**.
- **Optimistic: startup_capital_to_bep_rub = 18 095 669 ₽**; EBITDA break-even month = **M7**.
- **Pessimistic: startup_capital_to_bep_rub = 32 832 423 ₽**; EBITDA break-even month = **M12**.

## A6. Налоговая модель РФ
- **УСН 6%**: простой режим, но налог платится с выручки даже при слабой загрузке. Post-tax contribution = **282 000 ₽/клиент/мес**, post-tax break-even = **18,96 клиента**.
- **IT-льгота 3%**: применима при аккредитации Минцифры и соблюдении доли профильной выручки. Post-tax contribution = **301 500 ₽/клиент/мес**, post-tax break-even = **17,74 клиента**.
- **ОСНО 20%**: налог на прибыль **20%**, плюс **НДС 20%** по реализации, если контракт выставляется с НДС. Post-tax contribution = **256 800 ₽/клиент/мес**, post-tax break-even = **20,83 клиента**.
- Страховые взносы **~30% к ФОТ** уже сидят в FOT **4 758 000 ₽/мес** и через него во fixed costs **5 348 000 ₽/мес**.

## A7. Break-even summary
| Scenario | EBITDA BEP, clients | Post-tax BEP, clients (УСН / IT / ОСНО) | Break-even month | Clients at M12 | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|---:|
| Base | 14.65 | 18.96 / 17.74 / 20.83 | M8 | 28.01 | 21 822 733 ₽ |
| Optimistic | 14.65 | 18.96 / 17.74 / 20.83 | M7 | 37.08 | 18 095 669 ₽ |
| Pessimistic | 14.65 | 18.96 / 17.74 / 20.83 | M12 | 17.22 | 32 832 423 ₽ |

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 месяцев

Допущение для `CAC x2`: так как в Section A CAC не вычитался из EBITDA напрямую, в чувствительности считаю, что при том же GTM-бюджете объём новых клиентов режется примерно в 2 раза.

| Scenario | Ключевое изменение | Active clients @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | Base case из Section A | 28.01 | 4 875 987 | Проходит EBITDA gate |
| Sens1 | CAC x2 | 14.01 | -236 006 | Почти ровно уходим к break-even edge |
| Sens2 | Churn x2, до 3.28%/мес | 26.20 | 4 214 076 | Больно, но модель ещё жива |
| Sens3 | Price -30%, ARPU 455k ₽ | 28.01 | -586 143 | Самый опасный шок, т.к. съедает unit margin |

Вывод: главный single-point failure здесь не churn, а **price compression** и ухудшение acquisition efficiency.

## B2. Monte Carlo Lite, confidence intervals

### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 850 000 | 1 050 000 | 1 800 000 | `04-economics.md`, blended CAC 1.05m ₽ + founder-led / outbound dispersion [T3] |
| Monthly churn % | 1.2% | 1.64% | 3.0% | `05-critic.md` Section A + stress envelope from `04-economics.md` [T1] |
| ARPU ₽/мес | 455 000 | 650 000 | 850 000 | `04-economics.md` base ARPA 650k ₽ + premium CLM pricing signals [T4][T5][T6] |
| Conversion rate lead→paid % | 0.8% | 1.5% | 3.0% | `04-economics.md` funnel table [T3] |
| Time-to-hire месяцев, среднее | 1.0 | 1.3 | 2.5 | `04-economics.md` hiring table [T3] |

### Методика
- Вместо полной 1000-run симуляции использована **9-combo Monte Carlo Lite**.
- База новых клиентов: темп из Section A на M1-M12 и `4 new logos/month` на M13-M24.
- Throughput-множитель = `(conversion / 1.5%) × (1.26 / time-to-hire)`.
- `EBITDA @M24 = Active clients × (ARPU - COGS) - fixed costs`, где COGS = 285k ₽/клиент/мес, fixed costs = 5.348m ₽/мес.
- `CAC payback = CAC / (ARPU - COGS)`.
- `LTV/CAC = ((ARPU - COGS) / monthly churn) / CAC`.
- `Cash runway = 95m ₽ / (5.348m ₽ + acquisition spend)`, где acquisition spend масштабируется от базовых 2.52m ₽/мес пропорционально CAC.

### Результат Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -2 638 495 | 18 343 594 | 93 947 777 | 96 586 272 |
| CAC payback (мес) | 10.59 | 2.88 | 1.50 | 9.09 |
| LTV/CAC | 3.15 | 21.20 | 55.39 | 52.24 |
| Cash runway (мес) | 9.83 | 12.07 | 12.86 | 3.03 |

### Интерпретация правил
1. **p10 EBITDA < 0**, значит kill criterion #1 активируется автоматически, риск insolvency реальный.
2. **p50 EBITDA > 500k ₽/мес**, формально median проходит EBITDA gate.
3. Разброс между p90 и p10 экстремальный, значит score надо **даунгрейдить за неопределённость GTM и pricing**.
4. `Range width` по **LTV/CAC = 52.24**, то есть модель очень хрупкая к цене, churn и CAC.

Итог Monte Carlo Lite: кейс не разваливается в median, но tail-risk слишком широкий, чтобы считать его устойчивым без жёсткого контроля pricing floor, ICP и rollout discipline.

## B3. Competitor deep-dive

### Western competitors

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Agiloft | Сильный enterprise CLM, зрелый workflow/configuration layer, long-standing procurement/legal presence [T4] | Тяжёлое внедрение, выше time-to-value, продукт выглядит как CLM-suite, а не быстрый negotiation agent | ~8-10% глобального modern CLM / AI-contract-intelligence сегмента, **оценка по installed base и enterprise visibility, это inference** | Можем продавать faster pilot + локальную delivery-модель под РФ без полного CLM-overhaul |
| Luminance | Очень сильный AI-review/redlining бренд, 700+ клиентов в 70+ странах, мощный category signal [T5] | Обычно дорогой enterprise motion, слабее локализация под РФ-контур и data-residency требования | ~7-9% AI-first legal review сегмента, **inference по customer count и category prominence** | Наш плюс, локальный compliance stack и более прикладной workflow around procurement/legal ops |
| SpotDraft | AI-first UX, Word-native review, 450-700+ клиентов по публичным сигналам, сильный SMB-midmarket to enterprise bridge [T6] | Ниже глубина тяжёлого enterprise governance, чем у классических CLM-лидеров | ~4-6% AI-first contract operations сегмента, **inference по customer count и growth signals** | Можем выиграть там, где нужен high-touch локальный pilot и российская интеграция, а не глобальный self-serve playbook |

### Российские конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| Directum RX / AI-подсветка договоров | Большая установленная база СЭД/ECM в enterprise и госсекторе, сильные интеграции и документооборот [T7] | Часто продаётся как часть более тяжёлого ECM-ландшафта, slower UX и меньше AI-first positioning | ~8-12% адресуемого enterprise document/legal automation в РФ, **inference по installed base** | Мы легче заходим как узкий contract-intelligence layer без полной замены документооборота |
| Yandex B2B Tech, Нейроюрист | Сильный бренд, доступ к LLM-инфраструктуре, быстрый distribution через B2B Tech [T8] | Пока больше copilot/assistant, чем полноценный contract workflow system of record | ~3-5% emerging AI-legal-assistant ниши, **inference** | Наш плюс, если дадим end-to-end repository, playbooks, approval-routing и measurable EBITDA story |
| Doczilla | Узнаваемый российский legaltech/документ automation player, понятный template-centric workflow, заметность в legal community [T9] | Сильнее в document automation, чем в AI negotiation intelligence; риск service/customization drag | ~3-4% legal-document automation в РФ enterprise/upper-SMB, **inference** | Мы можем позиционироваться выше, как AI-операционный слой поверх repository + negotiation analytics |
| Noroots | AI legal assistant / contract review narrative, early category speed, заметность на vc.ru [T10] | Молодой игрок, меньше enterprise proof, ниже доверие risk/compliance buyers | ~1-2% AI legal assistant ниши РФ, **inference** | Наш плюс, более enterprise-heavy positioning и управляемый pilot под procurement/legal ops |
| Legiscan | Вертикальный AI-анализ судебки и документов, технологически интересный legal AI signal [T11] | Уже niche point solution, не полноценный contract operations stack | <1% в широком contract-intelligence сегменте РФ, **inference** | Мы шире закрываем contract lifecycle и согласование, а не только legal search/analysis |

### Что это значит для кейса
- Западные игроки подтверждают, что категория **реальна и платёжеспособна**.
- Российский рынок выглядит **фрагментированным**, без одного безусловного category king.
- Наиболее опасный локальный конкурент не стартап, а **установленная база Directum/ECM + быстрое доупаковочное AI-слоение**.
- Самая разумная позиция для кейса, **не “ещё один legal copilot”**, а **contract operations layer для enterprise procurement/legal с measurable cycle-time reduction**.

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | founder-dependent sales, без founder pipeline рушится | high | high | >50% SQL требуют прямого founder involvement | упаковать repeatable demo, нанять сильного AE, стандартизировать discovery |
| 2 | Operational | solutions legal превращает продукт в service-heavy delivery | high | high | >25 часов senior legal времени на клиента в месяц | жёсткие playbooks, лимиты кастомизации, paid change requests |
| 3 | Operational | нестабильность LLM API, latency/cost spikes | med | high | рост inference cost >30% или SLA<99% две недели подряд | multi-model routing, fallback providers, локальный cache/queue |
| 4 | Market | buyer education cycle слишком длинный | med | high | pilot-to-paid conversion <25% | продавать через ROI-кейсы и procurement bottlenecks, а не “AI ради AI” |
| 5 | Market | price compression из-за copilot-конкурентов и bundle-игроков | high | high | discounting >20% от прайса в 3+ сделках подряд | floor pricing, packaging с setup fee, value-based upsell |
| 6 | Market | enterprise CLM/ECM incumbents быстро копируют core features | med | high | в тендерах всё чаще фигурируют bundle-предложения Directum/CLM | narrow wedge, faster deployment, integration-first GTM |
| 7 | Regulatory | 152-ФЗ / data residency блокируют облачное размещение | high | high | security/legal review чаще 6 недель, требования on-prem растут | RU-hosting, private deployment, DPA и data map из коробки |
| 8 | Regulatory | 115-ФЗ / KYC / audit trail требования усложняют сделки с финсектором | med | med | банки требуют расширенные журналы действий и хранение переписки | audit logging, immutable history, enterprise retention policies |
| 9 | Financial | cash runway сжимается из-за CAC inflation | high | high | CAC >1.8m ₽ два месяца подряд | урезать paid GTM, сместиться в founder-led/partner-led, freeze hiring |
| 10 | Financial | девальвация USD повышает стоимость импортных SaaS и LLM | med | med | FX >15% за квартал, облачные счета растут быстрее выручки | рублёвые контракты с FX-buffer, локальные vendors, annual commits |
| 11 | Black swan | ужесточение санкций по SaaS/API | med | high | новые ограничения по billing/model access | multi-vendor procurement, российские или self-hosted fallback модели |
| 12 | Black swan | внезапное отключение ключевого LLM-провайдера | low | high | деградация качества/доступности у основного поставщика | заранее протестированный fallback stack, degrade-to-rules режим |

## B5. Kill conditions через 6 месяцев

1. **Insolvency / downside gate:** если обновлённый p10-профиль всё ещё показывает `EBITDA @M24 < 0`, а фактический cash runway опускается ниже **9 месяцев**, продолжать нельзя.
2. **GTM failure:** если к M6 меньше **6 активных платящих клиентов** или lead→paid остаётся **<1.0%** два месяца подряд, значит CAC-модель не воспроизводится.
3. **Unit economics failure:** если к M6 ARPU уходит ниже **500k ₽/мес** или gross margin падает ниже **45%**, price compression уже убивает операционную модель.

## B6. Verdict after P6B

Кейс остаётся **investable only with reservations**, но после risk-pass его надо трактовать как **medium-confidence / fragile economics**. Самый реалистичный путь, narrow ICP, high-ticket pilot, compliance-first deployment и жёсткий контроль service creep. Без этого модель легко съезжает в mix из консалтинга и дешёвого copilot-а.

## B7. Sources

- [T1] `05-critic.md` Section A и его base assumptions.
- [T3] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/workday-contract-intelligence-negotiation-agents-v2/04-economics.md`
- [T4] Agiloft contract lifecycle management pages: https://www.agiloft.com/platform/contract-lifecycle-management-software/
- [T5] Luminance / TechCrunch funding and customer signal: https://techcrunch.com/2025/02/18/legal-ai-startup-luminance-Backed-by-the-late-mike-lynch-raises-75m/
- [T6] SpotDraft / TechCrunch + product pages: https://techcrunch.com/2026/01/26/qualcomm-backs-spotdraft-to-scale-on-device-contract-ai-with-valuation-doubling-toward-400m/ ; https://www.spotdraft.com/verifai
- [T7] Habr / Directum AI contract comparison: https://habr.com/ru/companies/directum/articles/920486/
- [T8] Habr / Yandex Нейроюрист: https://habr.com/ru/news/913294/
- [T9] Rusprofile / ООО Доццилла: https://www.rusprofile.ru/id/6991354
- [T10] vc.ru / Noroots AI-юрист: https://vc.ru/legal/1880708-kak-ii-reshyaet-zadachi-yurista-i-gde-eto-zakreplyaetsya-v-zakonodatelstve
- [T11] Product Radar / Legiscan: https://productradar.ru/product/legiscan/

<!-- P6B-DONE -->


---

# FILE: 06-verdict.md

[B2B-OPS] Workday Contract Intelligence + Negotiation Agents — NEAR-PASS: 67/100 | EBITDA base=1239К₽/мес через 9 мес | LTV/CAC=3,8x | Ключевое преимущество: enterprise contract-ops wedge с measurable cycle-time ROI | Главный риск: exact-demand в РФ слабый, а price compression быстро ломает EBITDA.

# 06-verdict — Workday Contract Intelligence + Negotiation Agents v2

sector: B2B-OPS

## Итоговый вердикт
- **Вердикт:** **NEAR-PASS**
- **Score:** **67/100**
- **Статус инвесткомитета:** экономика проходит investment gate, но доказательств по локальному спросу, moat и repeatable GTM пока недостаточно для clean approve.
- **Формальный gate:** выполняется, потому что в base-scenario `company_ebitda_rub_month = 1 239 333 ₽/мес` достигается к **M9**, а порог `500 000 ₽/мес` проходится уже к **M8** при **18,05 клиентах**, то есть раньше 24 месяцев и сильно раньше лимита 50 клиентов.
- **Почему не APPROVED:** в `02-demand.md` exact-demand в РФ по ключам остаётся `LOW`, moat умеренный, а sensitivity в `05-critic.md` показывает, что шок `Price -30%` переводит модель в `EBITDA @M12 = -586 143 ₽/мес`.
- **Примечание по стадиям:** в этом кейсе demand-артефакт фактически хранится в `02-demand.md`, а solution/GTM в `03-solution.md`; для P7 использованы реальные файлы кейса.

## Оценка
Source tier balance: T1=1, T2=8, T3=1, weighted=2.00. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `Gross Margin = 56,2%`, `Downside LTV/CAC = 3,8x`, `Operating payback = 6,73 мес` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В 05-critic.md base-case уже на `M8` даёт `EBITDA 235 918 ₽`, а на `M9` `1 239 333 ₽`, то есть gate устойчиво пройден. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md exact-demand везде `LOW`, но есть `hh_ru=130` по proxу и `SAM ... 0,96-1,06 млрд ₽`; применён penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Защита строится на embedded workflow, switching costs и repository/playbook data, но без network effects и с умеренным regulatory barrier. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | В risk matrix отмечены `founder-dependent sales`, `service-heavy delivery`, `152-ФЗ / data residency`, `санкции` и `отключение ключевого LLM-провайдера`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | В 04-economics.md зафиксированы конкретные enterprise channels, `Blended fully-loaded CAC = 1 050 000 ₽`, а named targets ниже соответствуют ICP. |

**Sum raw = 100/150. Normalized score = round((100 × 100) / 150) = 67/100.**

## Investment thesis
Это не массовый legal copilot и не «ещё одна CLM-фича», а enterprise contract operations layer с дорогим onboarding, playbooks, routing, repository cleanup и recurring governance. Категория коммерчески доказана глобально, а локально может собраться в управляемый B2B-OPS бизнес только при жёстком ICP, premium pricing floor и стандартизированном pilot-to-retainer motion.

## Delta vs previous
- Кейс был resurrect как самостоятельный slug, а не как вложенный supporting signal.
- По сравнению с triage сильнее всего подтвердились **unit economics**, **enterprise willingness to pay** и **EBITDA gate**.
- Слабее всего подтвердились **прямой локальный category pull** и **defensible moat** против ECM/CLM incumbents и AI-copilot pressure.

## FULL business process from 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Target-account mapping по enterprise legal/procurement | SDR | CRM, реестры, ручной research | 2,0 ч | 2 400 | Низкая |
| 2 | Первый outbound / intro | SDR | email, phone, Telegram, CRM | 1,5 ч | 1 900 | Средняя |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1,0 ч | 3 400 | Средняя |
| 4 | Discovery contract workflow | AE + founder | discovery template, call notes | 2,0 ч | 10 500 | Низкая |
| 5 | Demo review / redlining / repository intelligence | AE + solutions legal | demo workspace | 2,0 ч | 12 500 | Низкая |
| 6 | Pilot scoping и KPI design | AE + solutions + CSM | ROI sheet, SOW | 3,0 ч | 17 000 | Низкая |
| 7 | Security / privacy / procurement review | CTO + founder | checklist, security pack | 4,0 ч | 21 000 | Низкая |
| 8 | Repository cleanup + clause playbooks setup | implementation + solutions legal | KB, templates, workflow rules | 20 ч | 86 000 | Низкая |
| 9 | Pilot 6-10 недель | CSM + solutions legal | weekly reviews, QA, reporting | 16 ч | 61 000 | Средняя |
| 10 | Contracting / procurement | AE + founder + legal | ЭДО, договоры, redlines | 8 ч | 31 000 | Низкая |
| 11 | Launch / invoicing | ops + CSM | ЭДО, billing, runbook | 2 ч | 5 500 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| ACV | 7 800 000 ₽/год |
| MRR на клиента | 650 000 ₽/мес |
| customer_ltv_rub | 9 240 000 ₽ stress / 24 353 333 ₽ base |
| Gross Margin | 56,2% |
| contribution_margin_rub_month | 321 000 ₽/мес на клиента |
| Fully-loaded CAC | 1 050 000 ₽ |
| LTV/CAC | 3,8x downside / 8,8x stress |
| CAC Payback | 1,62 мес по MRR / 2,88 мес по gross profit / 6,73 мес operating |
| Contribution Margin % | 49,4% |
| fixed_costs_rub_month | 5 348 000 ₽/мес |
| Break-even | 18-20 клиентов operating basis |
| company_ebitda_rub_month @ M9 base | 1 239 333 ₽/мес |
| company_ebitda_potential_rub_month @ 50 клиентов | 10 702 000 ₽/мес |
| clients_to_500k_ebitda | ~17-18 |
| clients_to_1m_ebitda | ~18 |
| months_to_500k_ebitda | 8 мес |
| months_to_1m_ebitda | 9 мес |
| startup_capital_to_bep_rub | 21 822 733 ₽ (base), 18 095 669 ₽ (optimistic), 32 832 423 ₽ (pessimistic) |

## Команда
| Роль | Кол-во | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO / founder | 1 | 845 000 | enterprise sales, pricing, key deals |
| CTO / platform lead | 1 | 676 000 | архитектура, security, presale |
| Backend / workflow engineer | 2 | 936 000 | integrations, workflow engine |
| Solutions legal | 1 | 442 000 | playbooks, exception review |
| Implementation / legal ops specialist | 1 | 338 000 | migration, repository cleanup |
| CSM | 1 | 299 000 | adoption, QBR, retention |
| SDR | 2 | 416 000 | ABM pipeline generation |
| AE | 1 | 403 000 | pilots, procurement, closing |
| Marketing / community | 1 | 247 000 | content, events, legal community |
| Finance / ops | 0,5 | 156 000 | invoicing, admin, ЭДО |
| **Итого** | **11,5** | **4 758 000** | steady-state команда |

## Moat — 7-factor framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | После настройки clause playbooks, repository cleanup и approval routing смена вендора становится дорогой. |
| Scale economies | 1 | COGS немного улучшается с объёмом, но legal oversight и onboarding остаются трудоёмкими. |
| Proprietary data / model advantage | 2 | Накапливаются clause history, exception patterns и review playbooks, но публичного dataset moat нет. |
| Regulatory moat | 1 | 152-ФЗ и data residency помогают, но формального лицензируемого барьера нет. |
| Brand / distribution | 2 | Категория подтверждена Workday/SpotDraft/Luminance, а вход возможен через enterprise legal ops и procurement pain. |
| Embedded workflow | 3 | Продукт глубоко встраивается в review, redlining, approvals, repository search и obligation workflows. |

**Moat sum = 11/21. Moat score = round((11 × 25) / 21) = 13/25.**

## GTM — 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Большой объём procurement и enterprise-legal договоров, высокая цена задержек и строгий audit trail. | email decision-maker в legal ops / procurement transformation | 900 000 ₽/мес |
| 2 | ВТБ | Регулируемый buyer с тяжёлым contract workflow и требованиями к data residency. | founder-led intro + банковская конференция | 850 000 ₽/мес |
| 3 | Альфа-Банк | Быстрые продуктовые и партнёрские контракты создают боль в review и approval routing. | direct outreach в COO/legal ops | 800 000 ₽/мес |
| 4 | Т-Банк | Высокая скорость запуска новых инициатив требует automation review, clause governance и repository search. | product/legal ops intro + referral | 750 000 ₽/мес |
| 5 | Ростелеком | Много supplier и enterprise contracts, где важно сократить cycle time и держать obligations. | отраслевой event + targeted email | 700 000 ₽/мес |
| 6 | МТС | Большой договорный массив между procurement, legal и sales ops, высокая цена ручной маршрутизации. | ABM в procurement/legal leadership | 700 000 ₽/мес |
| 7 | X5 Group | Массовый поток поставочных и коммерческих договоров, сильная боль в согласовании и шаблонах. | partnership с SI / retail legal ops outreach | 650 000 ₽/мес |
| 8 | Магнит | Нужен управляемый contract workflow для supplier contracts и obligation visibility. | email decision-maker + partner intro | 650 000 ₽/мес |
| 9 | Северсталь | Индустриальный холдинг с большим массивом закупочных и подрядных договоров, где дорого держать ручной review. | founder outreach + enterprise event | 700 000 ₽/мес |
| 10 | Самолет | Девелопер с большим объёмом подрядных и коммерческих договоров, где важны cycle time и clause standardization. | direct outreach в head of legal / operations | 650 000 ₽/мес |

### Оценка GTM realism
- Канальный fit реалистичен: здесь работают **founder-led enterprise sales, outbound ABM, partner referrals, legal/procurement events**.
- CAC не выглядит заниженным, потому что в модели уже учтены `enterprise sales motion, pilot, security review и category education`.
- Но GTM остаётся хрупким: при `CAC x2` в 05-critic.md `EBITDA @M12 = -236 006 ₽/мес`, а значит дисциплина по ICP и pricing критична.
- 10 named targets присутствуют, автоматический штраф к GTM не применяется.

## Финансовая интерпретация для инвесткомитета
- Unit economics проходят: downside `LTV/CAC = 3,8x`, gross margin 56,2%, operating payback 6,7 месяца.
- EBITDA path тоже рабочий: в base-case break-even приходится на `M8`, а к `M12` EBITDA уже `4 875 920 ₽/мес`.
- Но profile неустойчив к цене: в sensitivity `Price -30%` даёт отрицательный EBITDA, а Monte Carlo показывает `p10 EBITDA @M24 = -2 638 495 ₽/мес`.
- Следовательно, инвестиционный вопрос тут не в математике на бумаге, а в том, удастся ли удержать enterprise-прайсинг и не скатиться в legal-services heavy delivery.

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Price compression и discount pressure | high | high | В 05-critic.md `Price -30%` сразу переводит модель в `EBITDA @M12 = -586 143 ₽/мес`. |
| Service-heavy delivery / legal outsourcing drift | high | high | В 04-economics.md главный риск прямо описан как превращение продукта в `service-heavy legal ops business`. |
| Слабый exact-demand в РФ и founder-dependent GTM | med-high | high | В 02-demand.md exact-demand везде `LOW`, а в risk matrix зафиксирован `founder-dependent sales`. |

## Что должно быть доказано для перевода в APPROVED
1. **Не менее 2-3 paid pilots**, которые конвертируются в retainer, а не остаются на стадии разового project work.
2. **Pricing floor не ниже 650-700 тыс. ₽/мес** без системного discounting >20%.
3. **Повторяемый onboarding ≤10 недель** и legal oversight <25 часов senior-time на клиента в месяц.
4. **Минимум 2 референсных enterprise кейса** с доказанным cycle-time reduction и measurable backlog reduction.

## LTV Upside Calculator
### Формула
- `customer_ltv_rub = annual_revenue × gross_margin / annual_churn`
- `LTV/CAC = customer_ltv_rub / CAC`

### Upside table
| Сценарий | ARR, ₽ | GM | Annual churn | CAC, ₽ | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|---:|
| Текущая downside-база | 5 400 000 | 37% | 50% | 1 050 000 | 3 996 000 ₽ | 3,8x |
| Если вернуть stress-case | 6 600 000 | 42% | 30% | 1 050 000 | 9 240 000 ₽ | 8,8x |
| Если удержать base-case | 7 800 000 | 56,2% | 18% | 1 050 000 | 24 353 333 ₽ | 23,2x |
| Если CAC вырастет до 1,8 млн ₽ | 5 400 000 | 37% | 50% | 1 800 000 | 3 996 000 ₽ | 2,2x |
| Если price -30% и GM упадёт ниже 35% | 4 560 000 | 35% | 50% | 1 050 000 | 3 192 000 ₽ | 3,0x |

### Read-through
- Кейс уже близок к порогу investment-grade по downside LTV/CAC, но апсайд очень чувствителен к цене и churn.
- Поэтому путь из NEAR-PASS в APPROVED проходит через доказанный premium pricing и delivery discipline, а не через косметическое снижение CAC.

## Proof points for APPROVED
Не применяется, потому что итоговый статус кейса **NEAR-PASS**, а не APPROVED.

## Финальное решение комитета
**NEAR-PASS.**

Почему не reject:
- категория глобально подтверждена и локально имеет enterprise pain,
- economics проходят unit-gate и EBITDA-gate,
- buyer universe понятен и named targets реалистичны.

Почему пока не approve:
- локальный exact-demand всё ещё слабый,
- moat только средний,
- Monte Carlo tail-risk отрицательный,
- модель легко съезжает в service-heavy delivery при ослаблении pricing discipline.


---

# FILE: 07-score-trajectory.md

# Score trajectory

## 2026-04-24 06:55 MSK — P4 Demand Validation
- case: `workday-contract-intelligence-negotiation-agents-v2`
- stage: `P4-demand-validation`
- demand: `LOW exact-demand / MEDIUM adjacent enterprise pain`
- profit_gate: `PASS via enterprise implementation + managed contract ops; FAIL in low-ticket bot and usually FAIL in pure per-contract mode`
- market_view: `узкая, но монетизируемая LEGAL-OPS категория`
- score_impact:
  - demand_quality: `+1`
  - willingness_to_pay: `+2`
  - market_size: `+1`
  - go_to_market_complexity: `-1`
  - overall_delta: `+3`
- rationale:
  - internal multi-demand показал LOW по exact label, но сильный proxy-signal по русскому договорному workflow;
  - публичные цены Agiloft, HyperStart, Crosby и AI-Юрист подтверждают реальную willingness to pay;
  - SAM в РФ выглядит на уровне ~0,96-1,06 млрд ₽;
  - EBITDA > 500K ₽/мес достижима только в enterprise implementation / managed service модели.
- artifact: `pipeline/cases/workday-contract-intelligence-negotiation-agents-v2/02-demand.md`

## 2026-05-12 10:16 MSK — P7 Critic and Verdict
- case: `workday-contract-intelligence-negotiation-agents-v2`
- stage: `P7-critic-verdict`
- verdict: `NEAR-PASS`
- normalized_score: `67/100`
- raw_score: `100/150`
- status_gate: `EBITDA gate проходит, но APPROVED threshold не достигнут`
- score_impact:
  - unit_economics: `+4`
  - ebitda_path: `+4`
  - market_demand: `-2`
  - moat: `-2`
  - execution_risk: `-2`
  - gtm_realism: `+1`
  - overall_delta: `+3`
- rationale:
  - downside LTV/CAC = 3,8x и operating payback = 6,73 мес подтверждают рабочую математику;
  - base PnL проходит 500k EBITDA уже к M8 и 1,24 млн ₽/мес к M9;
  - exact-demand в РФ по ключам остаётся LOW, хотя prox-demand и глобальная категория валидны;
  - sensitivity показывает, что шок price -30% ломает EBITDA, а Monte Carlo p10 остаётся отрицательным.
- artifact: `pipeline/cases/workday-contract-intelligence-negotiation-agents-v2/06-verdict.md`
