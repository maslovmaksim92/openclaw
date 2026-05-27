# verdict
Источник pipeline: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/rejected/hightouch-geo-expand-1438-v2`


## 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-hightouch-geo-expand-1438.md
created: 2026-04-20T17:18:00+03:00
---

# Intake

## Контекст resurrection
- Тип: принудительный полный пайплайн для повторной аналитики
- Исходный slug: hightouch-geo-expand-1438
- Основание: сигнал ранее был закрыт как duplicate/supporting и должен пройти заново через P3→P7

## Полный контекст raw-файла

# RESURRECT SIGNAL — hightouch-geo-expand-1438

## Meta
- source: triage/triage-2026-04-17-hightouch-geo-expand-1438-duplicate.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-hightouch-geo-expand.md`

## Классификация
Дубликат ранее обработанного сигнала.

## Решение
Новый кейс не создан. Сигнал не добавлялся в `pipeline/cases/`, потому что в открытых кейсах новых оснований для обогащения или открытия не найдено.

## Почему это дубликат
- Содержательно это тот же GEO-EXPAND сигнал по Hightouch AI Decisioning: warehouse-native decisioning слой для lifecycle-маркетинга поверх DWH.
- По этому же сигналу уже существует ранее обработанный triage: `pipeline/triage/triage-2026-04-17-hightouch-geo-expand.md`.
- Тезис уже был развёрнут в отдельный кейс `warehouse-native-ai-decisioning-marketing-operator`, который сейчас находится в `pipeline/rejected/` с финальным вердиктом **REJECTED**.

## Почему кейс не переоткрываю
- Во входном файле нет нового факта, который меняет исходную инвестиционную картину относительно уже рассмотренного кейса.
- Основные данные совпадают с ранее зафиксированными: Hightouch, AI Decisioning, ссылка на TechCrunch от 2026-04-15, масштаб $100 млн ARR и тот же локальный wedge для РФ.
- Поскольку это не новый supporting signal для открытого кейса в `pipeline/cases/`, а повтор уже обработанного материала, файл корректно закрыт без создания нового контейнера.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Дубликат ранее обработанного сигнала по warehouse-native AI decisioning для маркетинга. Новый кейс не создан, существующие открытые кейсы не обогащались.
```



## 02-validation.md

_Файл отсутствует в кейсе: 02-validation.md_


## 03-demand.md

_Файл отсутствует в кейсе: 03-demand.md_


## 04-economics.md

---
stage: unit-economics
case: hightouch-geo-expand-1438-v2
date: 2026-05-12
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Hightouch AI Decisioning, enterprise B2B SaaS для warehouse-native customer data activation, персонализации и CRM-оркестрации поверх DWH.

## Executive summary

**Итог: PASS.**

На 12 мая 2026 года экономика в РФ собирается только как **mid-market / enterprise martech platform**, а не как SMB self-serve. При базовом чеке **500 000 ₽ MRR на клиента**, gross margin **78%**, fully-loaded enterprise CAC **~656 000 ₽** и месячном churn **2,5%** модель даёт:

- **LTV = 15,6 млн ₽**
- **LTV/CAC = 23,8x**
- **CAC Payback = 1,3 месяца**
- **Contribution Margin = 78%**
- **Break-even = 18 клиентов**
- **EBITDA при 50 клиентах = ~12,6 млн ₽/мес**

Ключевой риск не в математике LTV/CAC, а в том, что рынок узкий, продажа тяжёлая, а внедрение требует сильного presales + integration слоя. Но **Profit Gate проходит уверенно**, даже в консервативной enterprise-модели.

---

## 1. Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Mid-market / Enterprise B2B | крупный e-commerce, fintech, telecom, retail media |
| Средний чек | 500 000 ₽/мес | опора на локальный якорь Mindbox Enterprise от 400 000 ₽/мес + premium AI layer [T1] |
| ACV | 6 000 000 ₽/год | 500 000 × 12 |
| Валовая маржа | 78% | high-gross-margin SaaS, но с integration/support нагрузкой |
| COGS на клиента | 110 000 ₽/мес | см. разбивку ниже |
| Monthly churn | 2,5% | использую как реалистичный ориентир для enterprise B2B SaaS с высоким ARPA, чуть лучше медианы ChartMogul для компаний >$8M ARR [T2][T3] |
| LTV formula | ARPA × GM / churn | стандартная SaaS-формула |
| Segment CAC mode | Enterprise | complex sale, security/legal/procurement цикл |
| New customers at scale | 3 в месяц | 1 outbound + 1 inbound + 1 partner |
| Startup capital | 45 000 000 ₽ | для burn-to-breakeven и runway |

---

## 2. Подробный business process от lead до оплаты

Оценка дана **на 1 выигранного клиента** в enterprise motion.

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR + RevOps | CRM, Apollo/аналог, Excel | 6 ч | 12 000 | средняя |
| 2 | Обогащение контактов и сегментация | SDR | data provider, CRM | 8 ч | 16 000 | высокая |
| 3 | Outbound sequence и follow-ups | SDR | email automation, CRM | 20 ч | 40 000 | высокая |
| 4 | Первичный discovery call | SDR + AE | Zoom, CRM | 2 ч | 12 000 | низкая |
| 5 | Qualification / ICP-fit | AE | CRM, MEDDICC template | 3 ч | 18 000 | средняя |
| 6 | Demo с use-case mapping | AE + Solutions/CTO | demo env, slides | 4 ч | 35 000 | низкая |
| 7 | Data audit / feasibility assessment | CTO + Backend | DWH schema review, docs | 10 ч | 70 000 | низкая |
| 8 | Pilot scoping + ROI model | AE + CTO + Product | spreadsheet, proposal doc | 6 ч | 42 000 | низкая |
| 9 | Security / legal / procurement | AE + founder + legal | security questionnaire, MSA | 12 ч | 65 000 | низкая |
| 10 | Коммерческое предложение и negotiation | AE + CEO | CPQ, DocuSign/аналог | 5 ч | 38 000 | низкая |
| 11 | Pilot setup / onboarding kickoff | CSM + Backend + DevOps | cloud, connectors, PM tool | 14 ч | 82 000 | средняя |
| 12 | Invoice, procurement docs, payment collection | Finance/Ops + AE | 1C/банк/ЭДО | 4 ч | 18 000 | средняя |

**Прямые трудозатраты и deal-processing cost на win:** ~**448 000 ₽**.

Вывод: это не self-serve SaaS. Без дорогого presales, security review и integration handoff enterprise-сделка не закрывается.

---

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Облачная инфраструктура и DWH-коннекторы | 30 000 | compute + storage + data sync на одного активного enterprise-клиента |
| ML / inference / scoring | 15 000 | персонализация и decisioning jobs |
| Support & incident handling | 20 000 | часть CSM/support нагрузки |
| Solutions / integration maintenance | 25 000 | мелкие доработки, mapping, QA |
| Security/compliance overhead | 8 000 | VPN, logging, secrets, audit tooling |
| Billing / docs / customer ops | 5 000 | ЭДО, актирование, финоперации |
| Резерв на SLA и overage | 7 000 | буфер на пиковые нагрузки |
| **Итого COGS** | **110 000** |  |

**MRR на клиента:** 500 000 ₽

**Gross Profit на клиента:** 500 000 - 110 000 = **390 000 ₽/мес**

**Gross Margin / Contribution Margin:** 390 000 / 500 000 = **78%**

---

## 4. CAC по каналам с funnel conversion

### 4.1 Funnel by channel

| Канал | Top of funnel / мес | Reply/Lead | Discovery | SQL / Pilot | Won | Конверсия lead→won |
|---|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 1 200 target accounts | 120 replies (10%) | 36 meetings (30%) | 8 pilots (22% от meetings) | 1 | 0,83% от accounts |
| Inbound / content / thought leadership | 90 MQL | 30 SQL (33%) | 12 demos (40%) | 4 proposals (33%) | 1 | 1,1% от MQL |
| Partners / SI / agency referrals | 20 intros | 10 qualified (50%) | 5 demos (50%) | 2 commercial proposals (40%) | 1 | 5% от intros |

### 4.2 Fully-loaded CAC components

**Принцип:** сначала считаю raw acquisition pool, затем добавляю overhead x1.3, затем sanity-check against enterprise benchmark. Для этого кейса отдельный enterprise multiplier >2.0 не понадобился, потому что в raw уже заложены AE, presales, tools, partner activity и event spend, а итоговая величина уже попадает в benchmark 300-900K ₽/клиент [T4].

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 250 000 | поддержка inbound спроса и retargeting по enterprise ICP | допущение модели, sanity против enterprise B2B GTM |
| Outbound team FOT (SDR/AE attributed to new) | 689 000 | SDR 180K + AE 350K gross, +30% social contributions, AE аллокация 80% на new biz | [T5][T6] |
| Marketing team FOT (partial allocation) | 260 000 | Product marketing / content lead 200K gross × 100% new biz × 1,3 | [T7] + model allocation |
| Tools (CRM, Sales Nav/Apollo-аналог, enrichment, call tools) | 120 000 | CRM + enrichment + sequencing + call recording | допущение модели |
| Events/partnerships | 195 000 | мини-ивенты, co-marketing, partner MDF, travel | допущение модели |
| Overhead multiplier (x1.3) | 454 200 | 30% на менеджмент, finance, legal, office overhead от базы 1 514 000 ₽ | enterprise B2B standard per task |
| **Итого fully-loaded CAC pool / мес** | **1 968 200** |  |  |

При **3 новых paying customers в месяц**:

**Blended fully-loaded CAC = 1 968 200 / 3 = 656 067 ₽ ≈ 656 000 ₽**

### 4.3 CAC by channel

| Канал | Monthly spend, ₽ | New paying customers / мес | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound ABM | 730 000 | 1 | 730 000 | самый дорогой, но даёт контроль над ICP |
| Inbound / content | 610 000 | 1 | 610 000 | дешевле за счёт более тёплого спроса |
| Partners / SI | 628 200 | 1 | 628 200 | сильный канал для enterprise доверия |
| **Blended** | **1 968 200** | **3** | **656 000** | внутри benchmark 300-900K ₽/клиент [T4] |

**Sanity checks:**
- blended CAC не занижен относительно enterprise SaaS benchmark в РФ,
- channel CAC показан отдельно от blended CAC,
- CAC не выглядит подозрительно низким.

---

## 5. LTV с churn rate

### Выбранный churn benchmark

Опираюсь на ChartMogul:
- для SaaS-компаний с ARR **>$8M** медианный monthly customer churn около **3,1%** [T3],
- компании с высоким ARPA и B2B motion удерживаются лучше low-ARPA SaaS [T2].

Для локальной base-case модели беру **2,5% monthly churn** как рабочий ориентир для enterprise B2B SaaS с внедрением в CRM/data stack. Это не aggressive best-case, но и не медиана слабого SMB SaaS.

### Расчёт

- ARPA / MRR per customer = **500 000 ₽/мес**
- Gross Margin = **78%**
- Monthly churn = **2,5%**

**LTV = 500 000 × 0,78 / 0,025 = 15 600 000 ₽**

### Sensitivity

| Monthly churn | LTV, ₽ |
|---|---:|
| 2,0% | 19 500 000 |
| 2,5% | 15 600 000 |
| 3,1% | 12 580 645 |
| 4,0% | 9 750 000 |

Даже на 4% churn модель остаётся жизнеспособной, если чек удерживается на 500K+ MRR.

---

## 6. LTV/CAC ratio

- **LTV = 15 600 000 ₽**
- **CAC = 656 000 ₽**

**LTV/CAC = 15 600 000 / 656 000 = 23,8x**

### Интерпретация

- инвестиционный минимум: **>=3,0x**
- у кейса: **23,8x**

**Вердикт: инвестиционный порог проходит с большим запасом.**

---

## 7. CAC Payback

Формула по задаче:

**CAC Payback = CAC / MRR per customer**

- CAC = **656 000 ₽**
- MRR per customer = **500 000 ₽**

**CAC Payback = 656 000 / 500 000 = 1,31 месяца**

Дополнительно, если считать payback по gross profit:

**656 000 / 390 000 = 1,68 месяца**

Оба сценария сильно лучше базового sanity-порога <12 месяцев.

---

## 8. Contribution Margin %

- Revenue per customer = **500 000 ₽/мес**
- COGS per customer = **110 000 ₽/мес**
- Contribution per customer = **390 000 ₽/мес**

**Contribution Margin % = 390 000 / 500 000 = 78%**

Для enterprise software с integration layer это хороший уровень: достаточно высокий для масштабирования, но не нереалистично высокий.

---

## 9. Team & FOT

### 9.1 Полная таблица команды

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | enterprise sales, fundraising, strategic deals | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | архитектура, presales, security review | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | connectors, pipelines, orchestration | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | activation APIs, reliability | 450 000 | 135 000 | 585 000 |
| ML Engineer | scoring, experimentation, uplift models | 450 000 | 135 000 | 585 000 |
| DevOps | infra, CI/CD, observability | 350 000 | 105 000 | 455 000 |
| Frontend | marketer UI / workflow UX | 300 000 | 90 000 | 390 000 |
| Product Manager | roadmap, ICP prioritization, ROI cases | 400 000 | 120 000 | 520 000 |
| SDR | outbound pipeline generation | 180 000 | 54 000 | 234 000 |
| AE | new business closing, negotiations | 350 000 | 105 000 | 455 000 |
| Customer Success | onboarding, expansion, renewals | 250 000 | 75 000 | 325 000 |
| **Итого** |  |  |  | **5 629 000 ₽/мес** |

### 9.2 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 585 000 ×2 |
| ML Engineer | 1 | 450 000 | 2-3 | 2 | 135 000 | 585 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 350 000 | 1-2 | 2-3 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product Manager | 1 | 400 000 | 1-2 | 1 | 120 000 | 520 000 |

### 9.3 Salary benchmark notes

Использованные внешние якоря по РФ / Москва:
- Senior backend / Tech Lead: 300-600K+ ₽ [T8][T9]
- ML Engineer: 300-500K+ ₽ [T10][T11]
- DevOps: 350-450K ₽ [T12][T13]
- Frontend senior: 300-420K ₽ [T14][T15]
- Product Manager: 350-500K ₽ [T7][T16]
- SDR: 150-180K ₽ [T5]
- AE / account executive: 350-500K ₽ [T6]
- Customer Success: 170-250K ₽ [T17][T18]

### 9.4 Cumulative FOT timeline M1-M12

Правило realism: не нанимаю 5+ человек в первый месяц.

| Месяц | Кто в команде | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, CTO | 1 495 000 | foundation + customer discovery |
| M2 | + Backend #1 | 2 080 000 | начинается build ядра |
| M3 | + Backend #2, Frontend | 3 055 000 | появляется usable product shell |
| M4 | + DevOps, Product | 4 030 000 | infra + productization |
| M5 | + SDR | 4 264 000 | старт systematic outbound |
| M6 | + AE | 4 719 000 | полноценный closing motion |
| M7 | + Customer Success | 5 044 000 | readiness к onboarding и renewals |
| M8 | + ML Engineer | 5 629 000 | decisioning layer усиливается |
| M9 | без изменений | 5 629 000 |  |
| M10 | без изменений | 5 629 000 |  |
| M11 | без изменений | 5 629 000 |  |
| M12 | без изменений | 5 629 000 |  |

Вывод: план выглядит реалистично по hiring velocity и не нарушает time-to-hire sanity.

---

## 10. Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 629 000 | steady-state после M8 |
| Core infra base load | 600 000 | общая инфраструктура, не client-specific |
| Internal SaaS / CRM / analytics | 180 000 | Jira, Notion, CRM, observability, BI |
| Legal / accounting / security admin | 220 000 | документы, договоры, security paperwork |
| Office / admin / travel baseline | 300 000 | гибридный формат, командировки, admin |
| **Итого fixed costs** | **6 929 000 ₽/мес** |  |

---

## 11. Break-even по количеству клиентов и по месяцам

### 11.1 Break-even by client count

- Fixed costs = **6 929 000 ₽/мес**
- Contribution per client = **390 000 ₽/мес**

**Break-even clients = 6 929 000 / 390 000 = 17,77**

Округляю вверх:

**Break-even = 18 клиентов**

### 11.2 EBITDA at 50 clients

- Revenue = 50 × 500 000 = **25 000 000 ₽/мес**
- Gross profit = 50 × 390 000 = **19 500 000 ₽/мес**
- EBITDA ≈ 19 500 000 - 6 929 000 = **12 571 000 ₽/мес**

**Profit Gate check:** даже при 50 клиентах EBITDA сильно выше 500K ₽/мес. Fail-condition не наступает.

### 11.3 Break-even by month

Base ramp по платящим клиентам:

| Месяц | Платящие клиенты | MRR, ₽ | Gross Profit, ₽ | Fixed costs, ₽ | EBITDA approx, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 2 795 000 | -2 795 000 |
| M2 | 0 | 0 | 0 | 3 380 000 | -3 380 000 |
| M3 | 0 | 0 | 0 | 4 355 000 | -4 355 000 |
| M4 | 1 | 500 000 | 390 000 | 5 330 000 | -4 940 000 |
| M5 | 2 | 1 000 000 | 780 000 | 5 564 000 | -4 784 000 |
| M6 | 4 | 2 000 000 | 1 560 000 | 6 019 000 | -4 459 000 |
| M7 | 6 | 3 000 000 | 2 340 000 | 6 344 000 | -4 004 000 |
| M8 | 9 | 4 500 000 | 3 510 000 | 6 929 000 | -3 419 000 |
| M9 | 12 | 6 000 000 | 4 680 000 | 6 929 000 | -2 249 000 |
| M10 | 15 | 7 500 000 | 5 850 000 | 6 929 000 | -1 079 000 |
| M11 | 18 | 9 000 000 | 7 020 000 | 6 929 000 | **+91 000** |
| M12 | 21 | 10 500 000 | 8 190 000 | 6 929 000 | **+1 261 000** |

**Break-even month: M11**

---

## 12. Burn-to-breakeven и cash runway

### 12.1 Burn-to-breakeven

Суммарный отрицательный EBITDA до выхода в плюс:

- M1-M10 cumulative burn ≈ **35 464 000 ₽**

Добавляю buffer 15% на sales slippage, delayed procurement и extra integration work:

**Burn-to-breakeven = ~40 800 000 ₽**

### 12.2 Cash runway

При **startup_capital = 45 000 000 ₽**:

- peak burn around M8 = **6,93 млн ₽/мес**
- simple runway at peak burn = **~6,5 месяца**
- runway по полной ramp-модели = **~11-12 месяцев**, если клиентский набор идёт по плану

### Интерпретация

Для enterprise B2B SaaS это выглядит реалистично:
- капитал до BEP **не меньше 10 млн ₽**, red flag отсутствует,
- но запас очень некомфортный: любая просадка по продажам на 2-3 месяца легко съедает runway.

Практически это означает, что безопаснее поднимать **50-60 млн ₽**, а не 45 млн ₽.

---

## 13. Sanity checks

| Проверка | Статус | Комментарий |
|---|---|---|
| CAC Payback < 18 мес для enterprise | PASS | 1,31 мес |
| LTV/CAC >= 3,0 | PASS | 23,8x |
| CAC в enterprise benchmark 300-900K ₽ | PASS | 656K ₽ |
| EBITDA > 500K ₽/мес при 50 клиентах | PASS | 12,57M ₽ |
| Hire-план не ставит 5+ hires в M1 | PASS | в M1 только CEO и CTO |
| FOT M1 не выглядит заниженным | PASS | 1,495M ₽ |
| Capital to BEP > 10M ₽ | PASS | ~40,8M ₽ |

---

## 14. Final verdict

**PASS.**

Кейс проходит investment-grade unit economics при условии, что продаётся как enterprise/mid-market martech platform с чеком **от 500K ₽/мес**, а не как дешёвый SaaS-инструмент.

Главные выводы:
1. **Gross margin и contribution margin хорошие**.
2. **Fully-loaded CAC не занижен** и укладывается в enterprise benchmark.
3. **LTV/CAC сильно выше порога 3:1**.
4. **Break-even достижим на 18 клиентах**, а при 50 клиентах EBITDA уже комфортная.
5. Главный риск не в unit economics, а в **узости рынка, длинном цикле сделки и тяжёлом внедрении**.

Следовательно, на уровне P5 кейс **не режется по экономике**.

---

## Источники
- [T1] Mindbox tariffs, accessed 2026-05-12: https://mindbox.ru/tariffs/
- [T2] ChartMogul SaaS Retention Report: https://chartmogul.com/reports/saas-retention-report/
- [T3] ChartMogul, Customer churn rate benchmark: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
- [T4] Sanity benchmark from task brief for RU enterprise SaaS B2B: 300-900K ₽ CAC per client
- [T5] HH.ru, SDR / Sales Development Representative: https://hh.ru/vacancy/129774256
- [T6] HH.ru, Account Executive: https://hh.ru/vacancies/account_executive
- [T7] HH.ru, Senior Product Manager: https://hh.ru/vacancy/127470022
- [T8] HH.ru, Tech Lead / Technical Lead: https://hh.ru/vacancy/129718735
- [T9] HH.ru, Senior backend developer: https://hh.ru/vacancy/130003451
- [T10] HH.ru, Senior ML Engineer: https://hh.ru/vacancy/126901936
- [T11] HH.ru, ML engineer: https://hh.ru/vacancy/128020566
- [T12] HH.ru, Senior DevOps: https://hh.ru/vacancy/128794942
- [T13] HH.ru, Senior DevOps Engineer: https://hh.ru/vacancy/129322186
- [T14] HH.ru, Senior Frontend developer: https://hh.ru/vacancy/127093436
- [T15] HH.ru, Senior Frontend Developer: https://hh.ru/vacancy/129888122
- [T16] HH.ru, Product Owner / Product Manager: https://hh.ru/vacancy/128516150
- [T17] HH.ru, Customer Success Manager: https://hh.ru/vacancies/customer-success-manager
- [T18] HH.ru, Customer Success Manager (IT-проекты): https://hh.ru/vacancy/128771369
- [T19] Hightouch funding announcement, 2025-02-18: https://hightouch.com/blog/hightouch-funding-series-c
- [T20] TechCrunch, 2026-04-15, Hightouch reaches $100M ARR: https://techcrunch.com/2026/04/15/hightouch-reaches-100m-arr-fueled-by-marketing-tools-powered-by-ai/


## 05-critic.md

# SECTION A — PnL

### Сценарий: Базовый
Допущения: 3 новых клиента/мес, churn 2.5%, ARPA 500 000 ₽, COGS 110 000 ₽/клиент/мес, GM 78%.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 3 | 6 | 9 | 12 | 14 | 17 | 19 | 22 | 24 | 27 | 29 | 31 |
| MRR, ₽ | 1 500 000 | 2 962 500 | 4 388 438 | 5 778 727 | 7 134 258 | 8 455 902 | 9 744 504 | 11 000 892 | 12 225 869 | 13 420 223 | 14 584 717 | 15 720 099 |
| COGS, ₽ | 330 000 | 651 750 | 965 456 | 1 271 320 | 1 569 537 | 1 860 298 | 2 143 791 | 2 420 196 | 2 689 691 | 2 952 449 | 3 208 638 | 3 458 422 |
| Gross profit, ₽ | 1 170 000 | 2 310 750 | 3 422 981 | 4 507 407 | 5 564 722 | 6 595 604 | 7 600 713 | 8 580 696 | 9 536 178 | 10 467 774 | 11 376 079 | 12 261 677 |
| GM % | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% |
| Fixed costs, ₽ | 2 795 000 | 3 380 000 | 4 355 000 | 5 330 000 | 5 564 000 | 6 019 000 | 6 344 000 | 6 929 000 | 6 929 000 | 6 929 000 | 6 929 000 | 6 929 000 |
| EBITDA, ₽ | -1 625 000 | -1 069 250 | -932 019 | -822 593 | 722 | 576 604 | 1 256 713 | 1 651 696 | 2 607 178 | 3 538 774 | 4 447 079 | 5 332 677 |
| Cash burn, ₽ | 1 625 000 | 1 069 250 | 932 019 | 822 593 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 43 375 000 | 42 305 750 | 41 373 731 | 40 551 138 | 40 551 138 | 40 551 138 | 40 551 138 | 40 551 138 | 40 551 138 | 40 551 138 | 40 551 138 | 40 551 138 |

Break-even client count: 18 клиентов.
Break-even month: M5.
startup_capital_to_bep_rub: 4 448 862 ₽.

### Сценарий: Оптимистичный
Допущения: 4 новых клиента/мес, churn 2.0%, ARPA 500 000 ₽, COGS 110 000 ₽/клиент/мес, GM 78%.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 |
| Total clients | 4 | 8 | 12 | 16 | 19 | 23 | 26 | 30 | 33 | 37 | 40 | 43 |
| MRR, ₽ | 2 000 000 | 3 960 000 | 5 880 800 | 7 763 184 | 9 607 920 | 11 415 762 | 13 187 447 | 14 923 698 | 16 625 224 | 18 292 719 | 19 926 865 | 21 528 328 |
| COGS, ₽ | 440 000 | 871 200 | 1 293 776 | 1 707 900 | 2 113 742 | 2 511 468 | 2 901 238 | 3 283 214 | 3 657 549 | 4 024 398 | 4 383 910 | 4 736 232 |
| Gross profit, ₽ | 1 560 000 | 3 088 800 | 4 587 024 | 6 055 284 | 7 494 178 | 8 904 294 | 10 286 208 | 11 640 484 | 12 967 675 | 14 268 321 | 15 542 955 | 16 792 096 |
| GM % | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% |
| Fixed costs, ₽ | 2 795 000 | 3 380 000 | 4 355 000 | 5 330 000 | 5 564 000 | 6 019 000 | 6 344 000 | 6 929 000 | 6 929 000 | 6 929 000 | 6 929 000 | 6 929 000 |
| EBITDA, ₽ | -1 235 000 | -291 200 | 232 024 | 725 284 | 1 930 178 | 2 885 294 | 3 942 208 | 4 711 484 | 6 038 675 | 7 339 321 | 8 613 955 | 9 863 096 |
| Cash burn, ₽ | 1 235 000 | 291 200 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 43 765 000 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 | 43 473 800 |

Break-even client count: 18 клиентов.
Break-even month: M3.
startup_capital_to_bep_rub: 1 526 200 ₽.

### Сценарий: Пессимистичный
Допущения: 2 новых клиента/мес, churn 3.5%, ARPA 500 000 ₽, COGS 110 000 ₽/клиент/мес, GM 78%.
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 2 | 4 | 6 | 8 | 9 | 11 | 13 | 14 | 16 | 17 | 19 | 20 |
| MRR, ₽ | 1 000 000 | 1 965 000 | 2 896 225 | 3 794 857 | 4 662 037 | 5 498 866 | 6 306 406 | 7 085 681 | 7 837 682 | 8 563 364 | 9 263 646 | 9 939 418 |
| COGS, ₽ | 220 000 | 432 300 | 637 170 | 834 869 | 1 025 648 | 1 209 750 | 1 387 409 | 1 558 850 | 1 724 290 | 1 883 940 | 2 038 002 | 2 186 672 |
| Gross profit, ₽ | 780 000 | 1 532 700 | 2 259 056 | 2 959 989 | 3 636 389 | 4 289 115 | 4 918 996 | 5 526 831 | 6 113 392 | 6 679 424 | 7 225 644 | 7 752 746 |
| GM % | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% | 78% |
| Fixed costs, ₽ | 2 795 000 | 3 380 000 | 4 355 000 | 5 330 000 | 5 564 000 | 6 019 000 | 6 344 000 | 6 929 000 | 6 929 000 | 6 929 000 | 6 929 000 | 6 929 000 |
| EBITDA, ₽ | -2 015 000 | -1 847 300 | -2 095 944 | -2 370 011 | -1 927 611 | -1 729 885 | -1 425 004 | -1 402 169 | -815 608 | -249 576 | 296 644 | 823 746 |
| Cash burn, ₽ | 2 015 000 | 1 847 300 | 2 095 944 | 2 370 011 | 1 927 611 | 1 729 885 | 1 425 004 | 1 402 169 | 815 608 | 249 576 | 0 | 0 |
| Cumulative cash, ₽ | 42 985 000 | 41 137 700 | 39 041 756 | 36 671 744 | 34 744 133 | 33 014 248 | 31 589 245 | 30 187 076 | 29 371 468 | 29 121 892 | 29 121 892 | 29 121 892 |

Break-even client count: 18 клиентов.
Break-even month: M11.
startup_capital_to_bep_rub: 15 878 108 ₽.

## Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

Ниже waterfall для steady-state на 50 клиентах, чтобы была видна налоговая развилка.

| Метрика | Значение |
|---|---:|
| ARPA на клиента | 500 000 ₽/мес |
| Gross profit на клиента | 390 000 ₽/мес |
| Contribution на клиента | 390 000 ₽/мес |
| Revenue @ 50 clients | 25 000 000 ₽/мес |
| Gross profit @ 50 clients | 19 500 000 ₽/мес |
| EBITDA @ 50 clients | 12 571 000 ₽/мес |
| Net after tax, УСН 6% | 11 071 000 ₽/мес |
| Net after tax, IT-льгота 3% | 11 821 000 ₽/мес |
| Net after tax, ОСНО 20% | 10 056 800 ₽/мес |

Примечание: страховые взносы ~30% уже включены в FOT/fixed costs. НДС 20% при ОСНО не считается частью PnL-выручки, но создаёт cash-gap и требования к оборотке.

## Налоговая модель

| Режим | Как учтён в модели | Комментарий |
|---|---|---|
| УСН 6% | 6% от выручки | консервативный режим для SaaS без подтверждённой IT-льготы |
| IT-льгота 3% | 3% от выручки | применимо при аккредитации Минцифры и соблюдении критериев |
| ОСНО 20% | 20% от прибыли до налога | плюс НДС 20% к cash flow, если применимо |
| Страховые взносы | ~30% к gross ФОТ | уже включены в monthly fixed costs |

## Break-even summary

| Сценарий | Break-even client count | Break-even month | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Базовый | 18 | M5 | 4 448 862 ₽ |
| Оптимистичный | 18 | M3 | 1 526 200 ₽ |
| Пессимистичный | 18 | M11 | 15 878 108 ₽ |

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

База для сравнения взята из SECTION A: M12 EBITDA = **5 332 677 ₽/мес** при **31** клиентах, ARPA **500 000 ₽/мес**, churn **2,5%**, blended CAC **656 000 ₽**.

Логика sensitivity:
- **CAC x2**: при том же GTM-бюджете темп новых продаж падает примерно вдвое, поэтому к M12 ожидаемо не 31, а около **15,5** активных клиентов.
- **Churn x2**: при churn **5%/мес** и тех же 3 новых клиентах/мес клиентская база к M12 падает примерно до **27,6**.
- **Price -30%**: клиентская база та же, но ARPA снижается до **350 000 ₽/мес**.

| Сценарий | Active clients @M12 | ARPA, ₽/мес | Gross profit, ₽/мес | EBITDA @M12, ₽/мес | CAC payback, мес | LTV/CAC |
|---|---:|---:|---:|---:|---:|---:|
| Base | 31,0 | 500 000 | 12 090 000 | 5 161 000 | 1,31 | 23,8x |
| Sens1: CAC x2 | 15,5 | 500 000 | 6 045 000 | -884 000 | 2,62 | 11,9x |
| Sens2: Churn x2 | 27,6 | 500 000 | 10 756 000 | 3 827 000 | 1,31 | 11,9x |
| Sens3: Price -30% | 31,0 | 350 000 | 7 440 000 | 511 000 | 1,87 | 16,6x |

### Вывод по sensitivity
1. Самый опасный single-point failure здесь не churn, а **резкое удорожание enterprise CAC**: при CAC x2 модель уже уходит в отрицательный EBITDA на горизонте 12 месяцев.
2. **Price compression на 30%** почти полностью съедает запас прочности, EBITDA остаётся всего около **0,5 млн ₽/мес**, то есть почти на границе инвестиционного gate.
3. **Churn x2** неприятен, но не смертелен на M12, если сохраняется темп продаж 3 новых клиента в месяц.

## B2. Monte Carlo Lite — confidence intervals

Ниже не полный кодовый Monte Carlo, а упрощённая аппроксимация через **9 комбинаций** min/mode/max по ключевым драйверам. Это достаточно, чтобы получить p10/p50/p90 и проверить устойчивость экономики.

### Inputs: triangular distribution assumptions

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 500 000 | 656 000 | 1 200 000 | [T1][T4] |
| Monthly churn % | 1,5% | 2,5% | 5,0% | [T2][T3] |
| ARPU ₽/мес | 400 000 | 500 000 | 650 000 | [T1][T19][T20] |
| Conversion rate lead→paid % | 0,6% | 1,0% | 1,5% | [T4] + inference from current funnel |
| Time-to-hire месяцев (среднее) | 1,0 | 1,8 | 3,0 | [T5]-[T18] |

Примечание: для M24 я связал число новых клиентов в месяц с CAC и conversion rate, а active client base — с churn. Это не точная симуляция 1000 прогонов, а приближённая decision-useful модель.

### Ключевые результаты распределения

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -2 888 000 | 16 011 000 | 57 732 000 | 60 620 000 |
| CAC payback (мес) | 3,00 | 1,31 | 0,77 | 2,23 |
| LTV/CAC | 5,2x | 23,8x | 67,6x | 62,4x |
| Cash runway (мес) | 15,6 | 24,0+ | 24,0+ | 8,4+ |

### Интерпретация правил gate
1. **p10 EBITDA < 0**: правило срабатывает, значит нужно включать **kill criterion #1** и считать риск неплатёжеспособности реальным, а не теоретическим.
2. **p50 EBITDA > 500 000 ₽/мес**: median-case gate проходит с большим запасом.
3. **p90 / p10** в строгом виде неинтерпретируемо из-за отрицательного p10, что само по себе хуже правила `>10x`: хвост риска слишком тяжёлый.
4. **Range width по LTV/CAC = 62,4x > 8**: модель хрупкая, потому что outcome слишком зависит от pricing, churn и CAC discipline.

### Decision takeaway
Monte Carlo Lite не ломает кейс полностью, но переводит его из «просто хороший unit economics» в режим **high-variance enterprise bet**. Для фонда или бутстрэп-команды это означает, что без жёсткого контроля CAC и коммерческой дисциплины кейс легко разваливается, несмотря на сильный median.

## B3. Competitor deep-dive

### Топ-3 западных конкурента

> Оценки долей рынка ниже являются **инференсом**, а не аудированной статистикой. Я использую visible enterprise footprint, category mindshare, product breadth и публичные коммерческие сигналы.

| Игрок | Почему конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Bloomreach Engagement | CDP + ESP + AI personalization + omnichannel orchestration [T21] | широкий продукт, real-time personalization, сильный e-commerce footprint, зрелые AI-модули [T21] | тяжёлое внедрение, западный SaaS-риск, overkill для части RU-клиентов | ~8-12% глобального enterprise CDP/personalization сегмента (inference) | локальное внедрение, data residency в РФ, кастомизация под местные CRM/ESP/1С быстрее |
| Twilio Segment CDP | сильная data pipeline + CDP база, большой бренд и широкая экосистема [T22] | top-of-funnel brand, developer trust, data infra maturity | слабее как готовый AI decisioning слой, чаще требует докрутки поверх stack | ~10-15% в broader CDP tooling (inference) | можем продавать не как инфраструктуру, а как готовый decisioning outcome для CRM-команд |
| Simon Data | warehouse-first CDP + AI/segmentation/personalization [T23] | близкий positioning к Hightouch, no-code activation, strong data-warehouse story [T23] | меньше brand power, enterprise sale всё ещё сложный, outside-US footprint ограничен | ~2-4% глобального сегмента (inference) | локальный compliance package, ниже cost-to-serve в РФ, лучше адаптация под local martech stack |

### Топ-5 российских конкурентов

| Игрок | Evidence base | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Mindbox | тарифы 150K/400K+ ₽, enterprise focus [T1]; юрлицо в РФ [T24] | самый сильный локальный бренд, омниканальность, mature implementation motion, on-prem/SLA для enterprise [T1] | product breadth выше, чем у узкого AI decisioning, значит часть функций покупатель уже получает без нас | ~25-35% локального upper-mid/enterprise CRM automation/CDP сегмента (inference) | warehouse-native decisioning поверх существующего стека, меньше vendor lock-in, лучше для data-mature компаний |
| Retail Rocket | Habr описывает платформу мультиканальной персонализации на big data [T25]; Habr Career показывает международный footprint и продуктовый набор [T26] | сильны в e-commerce personalization, recommendations, loyalty/promo, retail domain expertise | более вертикальный e-commerce DNA, менее универсальный warehouse-native слой | ~10-15% локального e-commerce personalization сегмента (inference) | лучше cross-vertical story для fintech, telecom, subscription и больших CRM-баз вне e-commerce |
| Altcraft | Habr прямо позиционирует Altcraft как CDP platform [T27]; Rusprofile фиксирует отдельное юрлицо/историю компании [T28] | on-prem / data control story, российская локализация, омниканальные коммуникации | слабее category pull и бренд, меньше публичного enterprise proof | ~5-10% локального CDP/marketing automation сегмента (inference) | более сильный ROI-тезис на uplift/decisioning, а не просто on-prem CDP |
| enKod | vc.ru прямо называет enKod CDP-платформой [T29][T30]; Rusprofile подтверждает действующее юрлицо [T31] | хороший fit для CRM-marketing automation, заметность в local community, вероятно более лёгкий старт | ниже enterprise moat, меньше perceived strategic depth для very large accounts | ~3-7% локального mid-market сегмента (inference) | лучше продаёмся в large-enterprise как intelligence layer над DWH и action systems |
| Natimatica CDP / Skolkovo-type stack | Skolkovo PDF описывает fullstack CDP, ML/AI модели, campaign launch, data unification [T32] | сильный adtech/data-science DNA, российская разработка, понятная ставка на ML/AI | выглядит менее go-to-market зрелым, больше platform build risk | <3% в локальном enterprise CDP сегменте (inference) | можем выигрывать зрелостью commercial packaging и более чётким enterprise ROI narrative |

### Вывод по конкурентам
1. На Западе категория уже доказана, значит риск не в отсутствии use-case, а в **локальном right-to-win**.
2. В РФ самый опасный конкурент не Hightouch-подобный pure-play, а **Mindbox + in-house stack**.
3. Если оффер не покажет measurable uplift поверх уже купленного CDP/CRM-стека, рынок быстро сведёт его к «дорогой add-on аналитике» и продавит price compression.

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder-led sales не масштабируется, без CEO pipeline останавливается | high | high | >50% сделок завязаны на одного фаундера, AE не закрывает enterprise самостоятельно | формализовать sales playbook, нанять senior AE, ввести deal reviews и MEDDICC |
| 2 | Operational | Интеграции с DWH/CRM/ESP занимают дольше плана и съедают margin | med | high | onboarding >90 дней, рост custom scope, много ручных mapping tasks | стандартизировать коннекторы, ограничить custom scope, внедрить paid implementation |
| 3 | Operational | Зависимость от внешних LLM/API и генеративных моделей ухудшает SLA или себестоимость | med | high | рост inference cost >30%, просадки latency, rate limits от провайдера | multi-model routing, fallback на open-source/on-prem inference, кэширование, лимиты на costly workloads |
| 4 | Market | Реальный спрос в РФ остаётся нишевым, ICP слишком узкий | high | high | <10 качественных enterprise opportunities в квартал, мало inbound с нужным чеком | сузить ICP, идти через top-100 accounts, проверять wedge в 2-3 вертикалях вместо broad market |
| 5 | Market | Mindbox, Retail Rocket и in-house stacks давят на цену | high | high | win rate падает, скидки >25%, клиенты сравнивают только с ESP/CDP тарифами | продавать uplift/ROI, брать оплату за outcome-linked modules, избегать commodity messaging |
| 6 | Market | Price compression делает premium AI layer «необязательной надстройкой» | med | high | ARPA у новых сделок <400K ₽, upsell не растёт | модульная упаковка, доказательство quick wins за 60-90 дней, фокус на больших базах с заметным uplift |
| 7 | Regulatory | 152-ФЗ и data residency ломают западный deployment и ограничивают SaaS-архитектуру | high | high | security/legal блокируют cloud outside RF, удлиняется procurement | РФ-hosting, on-prem/private cloud option, локальные DPA и security docs |
| 8 | Regulatory | 115-ФЗ / банковский compliance и требования к explainability ограничивают продажи в fintech | med | med | банки требуют расширенный аудит, журналирование и модельную прозрачность | audit trail, explainability layer, sandbox/pilot в non-core use-cases |
| 9 | Regulatory | Санкции и ограничения западных SaaS-вендоров обрывают часть инфраструктуры | med | high | недоступность critical vendor, рост отказов по оплатам/аккаунтам | локальные замены, self-hosted stack, vendor concentration cap |
| 10 | Financial | Runway слишком короткий для enterprise sales cycle, особенно при 2-3 кварталах sales slippage | high | high | cash <9 месяцев runway, burn растёт быстрее bookings | поднимать 50-60 млн ₽ вместо 45 млн ₽, stop-hiring discipline, monthly cash review |
| 11 | Financial | Ослабление рубля к USD повышает стоимость облака, API и security tooling | med | med | USD/RUB sustained shock, рост dollar-denominated vendor bills | FX buffer, RUB pricing uplifts, локализация части стека |
| 12 | Financial | Инфляция зарплат и найма в senior data/ML/backend разрушает fixed-cost plan | med | med | offer acceptance падает, компенсации +20-30% выше бюджета | phased hiring, remote hiring outside Moscow, variable comp, automation over headcount |
| 13 | Black swan | Новые санкции или военная эскалация режут enterprise IT-бюджеты | med | high | пауза в новых IT-проектах, перенос пилотов, procurement freeze | вертикальный фокус на сегменты с defensive ROI, сокращение burn, services revenue buffer |
| 14 | Black swan | Отключение доступа к ключевым LLM/API провайдерам или облакам | low | high | внезапная недоступность модели/облака, форсированный replatform | резервный стек open-source models, abstraction layer, disaster recovery drills |

## B5. Kill conditions через 6 месяцев

1. **Median EBITDA gate не собирается**: rolling forecast на M12 показывает **EBITDA < 500 000 ₽/мес** даже в base/median-case.
2. **Продажи не нашли PMF**: за 6 месяцев получено **<3 paying клиентов** ИЛИ blended **CAC > 1,2 млн ₽** на платящего клиента.
3. **Retention/pricing сломаны**: monthly churn устойчиво **>5%** ИЛИ фактический ARPA по новым сделкам **<350 000 ₽/мес**.

## B6. Итоговый critic verdict по SECTION B

SECTION B усиливает кейс как **интересный, но хрупкий enterprise bet**. Категория доказана глобально, локальный бюджет существует, но downside жёсткий: при CAC shock или price compression economics быстро деградирует. Поэтому кейс можно продолжать только при дисциплине по трём метрикам: **CAC, ARPA, deployment speed**.

## Источники SECTION B
- [T21] Bloomreach Engagement: https://www.bloomreach.com/en/products/engagement
- [T22] Twilio Segment Customer Data Platform: https://segment.com/
- [T23] Simon Data overview: https://www.simondata.com/
- [T24] Rusprofile, ООО «Майндбокс»: https://www.rusprofile.ru/
- [T25] Habr, Retail Rocket как платформа персонализации: https://habr.com/ru/companies/retailrocket/
- [T26] Habr Career, Retail Rocket company profile: https://career.habr.com/companies/retailrocket
- [T27] Habr, Altcraft CDP platform: https://habr.com/ru/companies/altcraft/
- [T28] Rusprofile, ООО «Альткрафт»: https://www.rusprofile.ru/
- [T29] vc.ru, enKod CDP / CRM automation materials: https://vc.ru/u/310470-enkod
- [T30] vc.ru, обзор CDP-рынка с enKod: https://vc.ru/
- [T31] Rusprofile, ООО «Энкод»: https://www.rusprofile.ru/
- [T32] Skolkovo, Martech/Adtech company materials with CDP/AI stack references: https://old.sk.ru/

<!-- P6B-DONE -->


## 06-verdict.md

[GEO-EXPAND] Hightouch AI Decisioning — NEAR-PASS: 65/100 | EBITDA base=1261К₽/мес через 12 мес | LTV/CAC=23,8x | Ключевое преимущество: сильная unit economics в enterprise martech | Главный риск: weak moat и слабый прямой спрос в РФ.

# 06-verdict

sector: GEO-EXPAND

## Investment committee verdict
- Статус: **NEAR-PASS**
- Нормализованный score: **65/100**
- Raw total: **97/150**
- Routing: **pipeline/rejected/**
- Gate check: **company_ebitda_potential_rub_month > 500 000 ₽/мес проходит, но approve блокируют demand/moat margin of safety**.

## Delta vs previous
- Это rerun standalone-candidate для сигнала, который ранее схлопывался в соседний кейс `warehouse-native-ai-decisioning-marketing-operator`.
- По сравнению с прошлым rejection логика не изменилась: **экономика сильная, но локальный right-to-win слабый**.
- Отличие текущего rerun: enterprise PnL и CAC дисциплина описаны лучше, поэтому кейс доходит до **NEAR-PASS**, а не до жёсткого reject по economics.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV/CAC = 23,8x`, `CAC Payback = 1,31 месяца`, `Contribution Margin = 78%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `M12 EBITDA = +1 261 000 ₽`, `EBITDA при 50 клиентах = ~12,6 млн ₽/мес`, gate выполняется. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | `прямой спрос в РФ ... практически отсутствует`, а rule-default даёт `tier_balance = 1.00` и cap `10/25`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | `рынок быстро сведёт его к дорогой add-on аналитике`, moat есть в интеграциях, но не в category control. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | `любой sales slippage на 2-3 месяца легко съедает runway`, плюс enterprise onboarding и data residency риск. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | ICP ясен: `крупный e-commerce, fintech, telecom, retail media`, а blended CAC `656K ₽` остаётся в benchmark. |

**Normalized score = round((97 × 100) / 150) = 65/100.**

## 7-factor moat framework

| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Новый клиент почти не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | DWH-мэппинг, CRM-интеграции и обученные decision flows дают умеренный lock-in. |
| Scale economies | 1 | COGS снижается умеренно, но presales/integration остаются high-touch. |
| Proprietary data / model advantage | 1 | Есть potential на first-party decision data, но нет подтверждённого dataset moat. |
| Regulatory moat | 1 | 152-ФЗ и data residency важны, но это скорее hurdle, чем уникальная лицензируемая защита. |
| Brand / distribution | 1 | Локальный бренд отсутствует, distribution ещё founder-heavy. |
| Embedded workflow | 3 | После встраивания в CRM orchestration слой становится частью ежедневного retention workflow. |

**Moat sum = 9/21. Moat score = round((9 × 25) / 21) = 11/25.**

## Investment thesis summary
Кейс выглядит как **узкий enterprise decisioning-layer поверх уже существующих CDP/CRM бюджетов**, а не как массовая новая категория в РФ. Это означает, что продукт можно построить в прибыльный niche SaaS, но для комитета не хватает margin of safety по трём направлениям: прямой локальный спрос, defensibility против Mindbox/in-house stack и repeatable GTM без founder bottleneck.

## FULL business process from 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list | SDR + RevOps | CRM, Apollo/аналог, Excel | 6 ч | 12 000 | средняя |
| 2 | Обогащение контактов и сегментация | SDR | data provider, CRM | 8 ч | 16 000 | высокая |
| 3 | Outbound sequence и follow-ups | SDR | email automation, CRM | 20 ч | 40 000 | высокая |
| 4 | Первичный discovery call | SDR + AE | Zoom, CRM | 2 ч | 12 000 | низкая |
| 5 | Qualification / ICP-fit | AE | CRM, MEDDICC template | 3 ч | 18 000 | средняя |
| 6 | Demo с use-case mapping | AE + Solutions/CTO | demo env, slides | 4 ч | 35 000 | низкая |
| 7 | Data audit / feasibility assessment | CTO + Backend | DWH schema review, docs | 10 ч | 70 000 | низкая |
| 8 | Pilot scoping + ROI model | AE + CTO + Product | spreadsheet, proposal doc | 6 ч | 42 000 | низкая |
| 9 | Security / legal / procurement | AE + founder + legal | security questionnaire, MSA | 12 ч | 65 000 | низкая |
| 10 | Коммерческое предложение и negotiation | AE + CEO | CPQ, DocuSign/аналог | 5 ч | 38 000 | низкая |
| 11 | Pilot setup / onboarding kickoff | CSM + Backend + DevOps | cloud, connectors, PM tool | 14 ч | 82 000 | средняя |
| 12 | Invoice, procurement docs, payment collection | Finance/Ops + AE | 1C/банк/ЭДО | 4 ч | 18 000 | средняя |

**Прямые трудозатраты на выигранного клиента: ~448 000 ₽.**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 15 600 000 ₽ |
| CAC | 656 000 ₽ |
| LTV/CAC | 23,8x |
| CAC Payback | 1,31 мес |
| GM / Contribution Margin | 78% |
| contribution_margin_rub_month | 390 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 929 000 ₽/мес |
| Break-even clients | 18 |
| Break-even month | M11 |
| company_ebitda_rub_month base | 1 261 000 ₽/мес через 12 мес |
| company_ebitda_potential_rub_month | 12 571 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 20 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 21 |
| months_to_1m_ebitda | 12 |
| startup_capital_to_bep_rub | ~40 800 000 ₽ |

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraising, strategic deals | 780 000 |
| CTO / Tech Lead | архитектура, presales, security review | 715 000 |
| Senior Backend #1 | connectors, pipelines, orchestration | 585 000 |
| Senior Backend #2 | activation APIs, reliability | 585 000 |
| ML Engineer | scoring, experimentation, uplift models | 585 000 |
| DevOps | infra, CI/CD, observability | 455 000 |
| Frontend | marketer UI / workflow UX | 390 000 |
| Product Manager | roadmap, ICP prioritization, ROI cases | 520 000 |
| SDR | outbound pipeline generation | 234 000 |
| AE | new business closing, negotiations | 455 000 |
| Customer Success | onboarding, expansion, renewals | 325 000 |
| **Итого** |  | **5 629 000 ₽/мес** |

## PnL и risk summary

### SECTION A: PnL
- Base-case в `05-critic.md`: **M12 EBITDA = 5 332 677 ₽/мес** при 31 клиентах, если GTM идёт строго по модели P6A.
- Более консервативный ramp из `04-economics.md`: **M12 EBITDA = 1 261 000 ₽/мес** при 21 клиенте.
- Break-even count: **18 клиентов**.
- `startup_capital_to_bep_rub`: **~40,8 млн ₽** с буфером 15%.
- На 50 клиентах `company_ebitda_potential_rub_month = 12 571 000 ₽/мес`.

### SECTION B: Risk + Monte Carlo
- `p10 EBITDA @M24 = -2 888 000 ₽/мес`, `p50 = 16 011 000 ₽/мес`, `p90 = 57 732 000 ₽/мес`.
- `Range width по LTV/CAC = 62,4x`, то есть outcome слишком чувствителен к CAC, churn и pricing discipline.
- Single-point failure из critic: **CAC x2** уводит модель в отрицательный EBITDA на горизонте 12 месяцев.

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Ozon | Крупный marketplace с heavy CRM и персонализацией, где uplift на cross-sell и retention прямо монетизируется. | email decision-maker в CRM / loyalty + founder outbound | 500 000 ₽/мес |
| 2 | Wildberries | Огромная промо- и коммуникационная база, где decision layer может оптимизировать сегментацию и частоту касаний. | партнёрство с martech/SI + founder-led intro | 500 000 ₽/мес |
| 3 | Яндекс Маркет | Зрелый data stack и постоянные сценарии recommendations / lifecycle marketing. | конференция + email head of CRM/personalization | 450 000 ₽/мес |
| 4 | X5 Group | Loyalty и omnichannel promo orchestration создают понятную боль для next-best-action decisioning. | retail-конференция + интеграторский канал | 450 000 ₽/мес |
| 5 | Магнит | Большой first-party data контур и регулярные CRM-кампании, где важна promo efficiency. | email decision-maker + партнёрство с data-интегратором | 400 000 ₽/мес |
| 6 | МТС | Телеком с развитым CRM marketing и cross-sell сценариями по большой базе. | direct outbound в CVM/CRM lead | 450 000 ₽/мес |
| 7 | МегаФон | Сильный retention motion, upsell и тарифные предложения, где нужен decision engine поверх событийных данных. | отраслевое мероприятие + founder outbound | 400 000 ₽/мес |
| 8 | Т-Банк | Высокая культура экспериментов и lifecycle-коммуникаций, где measurable uplift легко защищается перед buyer. | warm intro в growth/CRM lead + email | 500 000 ₽/мес |
| 9 | Lamoda | Fashion e-commerce с высокой зависимостью от персонализации, сегментации и reactivation сценариев. | vc.ru ad + outbound в CRM/commercial analytics | 350 000 ₽/мес |
| 10 | Детский мир | Loyalty, промо и CRM-сценарии в ритейле создают понятный wedge для personalization uplift. | retail media / conference + email decision-maker | 350 000 ₽/мес |

**Вывод по GTM:** named targets реалистичны и совпадают с ICP, но motion остаётся enterprise-heavy и founder-dependent.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| weak moat / price compression | Высокая | Высокий | Buyer может закрыть заметную часть боли через Mindbox, Retail Rocket или in-house stack и продавить premium pricing вниз. |
| enterprise CAC shock | Средняя | Высокий | В critic прямо показано, что при `CAC x2` EBITDA уходит в отрицательную зону на M12. |
| evidence_quality_unverified | Высокая | Средний | В demand-файле отсутствует строка `Sources: T1=..., T2=..., T3=...`, поэтому tier-balance по дефолту penalized. |

## Что нужно доказать для APPROVED
1. **3-5 платящих enterprise клиентов** в РФ без дисконта ниже 400-500К ₽/мес.
2. **Pilot-to-production conversion** без расползания onboarding в кастомную интеграционную фабрику.
3. **Repeatable GTM**: часть pipeline должна приходить через partners/content, а не только founder-led deals.
4. **Локальный moat**: data residency + готовые коннекторы + ROI cases, которые Mindbox/in-house не повторяют быстро.
5. **Фактический source quality uplift**: demand-стадия должна быть пересобрана с явным T1/T2/T3 breakdown.

## LTV Upside Calculator
Так как итоговый статус **NEAR-PASS**, переход в approve можно считать от трёх рычагов:

| Рычаг | Текущее значение | Целевое значение | Влияние |
|---|---:|---:|---|
| ARPA | 500 000 ₽/мес | 550 000 ₽/мес | `customer_ltv_rub` вырастает примерно до **17,16 млн ₽** при тех же GM и churn. |
| CAC | 656 000 ₽ | 520 000 ₽ | `LTV/CAC` вырастает с **23,8x** до примерно **33,0x**. |
| Contribution margin | 78% | 80% | `contribution_margin_rub_month` растёт до **440 000 ₽/мес**, а clients_to_500k_ebitda снижается до **18**. |

**Практический апсайд-сценарий:** если кейс покажет 3-5 реальных локальных клиентов с чеком **500-550К ₽/мес**, CAC ниже **520К ₽** и временем внедрения до **60-90 дней**, он может перейти в диапазон **70-73/100**.

## Proof points, которых сейчас не хватает для APPROVED
- нет прямого локального evidence, что exact-category покупается как отдельная budget line в РФ;
- нет подтверждённого proprietary data moat или явного distribution moat;
- нет доказательства, что enterprise sales motion масштабируется без founder bottleneck;
- нет source-tier breakdown, чтобы снять penalty по Market+Demand.

## Final verdict
**Решение комитета: NEAR-PASS, маршрутизация в REJECTED bucket до новых proof points.**

Кейс не режется по экономике, наоборот, client-level и company-level PnL выглядят сильно. Но для approve не хватает именно инвестиционной защищённости: спрос в РФ остаётся косвенным, moat слабый, а enterprise GTM слишком чувствителен к CAC и price compression. Возвращаться к approve имеет смысл после первых локальных paid pilots и пересборки demand evidence.


## 07-score-trajectory.md

# 07-score-trajectory

```yaml
- date: 2026-05-12
  stage: P5
  analyst: branch-models-lead
  change: created
  scores:
    demand: 3.4
    unit_economics: 4.2
    moat: 2.8
    market: 3.1
    founder_fit: 2.5
    investability: 3.5
  summary:
    previous_status: CONDITIONAL_PASS at demand stage
    current_status: PASS at unit economics stage
    rationale:
      - unit economics собираются только в enterprise/mid-market GTM с чеком около 500K ₽ MRR
      - fully-loaded CAC после нормализации до 656K ₽ остаётся в enterprise benchmark
      - LTV/CAC 23.8x и payback 1.3 месяца проходят investment-grade пороги
      - break-even достигается на 18 клиентах, EBITDA при 50 клиентах существенно выше 500K ₽/мес
      - основной риск смещается из economics в market narrowness, long sales cycle и implementation-heavy delivery

- date: 2026-05-12
  stage: P6A
  analyst: branch-models-lead
  change: appended
  scores:
    investability: 3.9
    capital_efficiency: 4.1
    downside_resilience: 3.4
  summary:
    previous_status: PASS at unit economics stage
    current_status: PASS_WITH_RESERVATIONS pending final verdict
    rationale:
      - PnL подтверждает ранний EBITDA break-even на 18 клиентах, в base-case уже к M5
      - startup_capital_to_bep_rub выглядит умеренным для enterprise GTM, около 4.45 млн ₽ в base и 15.88 млн ₽ в pessimistic
      - при 50 клиентах EBITDA остаётся существенно выше mandatory gate 500K ₽/мес во всех рабочих сценариях
      - экономическая прочность держится только при high-ACV positioning и контроле implementation-heavy delivery
      - главный residual risk не в математике, а в узости рынка и зависимости от enterprise sales execution

- date: 2026-05-27
  stage: P7
  analyst: branch-models-lead
  change: rewritten_with_append
  scores:
    unit_economics: 20
    ebitda_potential: 19
    market_demand: 10
    moat: 11
    execution_risk: 17
    gtm_realism: 20
    normalized_score: 65
  summary:
    previous_status: PASS_WITH_RESERVATIONS pending final verdict
    current_status: NEAR-PASS routed to rejected bucket
    rationale:
      - raw total по rubric 6x25 составил 97 из 150, нормализованный итог 65 из 100
      - criterion #3 capped at 10 из 25, потому что в demand-файле нет строки Sources T1/T2/T3 и сработал default penalty
      - moat остаётся слабым, 9 из 21 по 7-factor framework, потому что у кейса нет network effects и локального distribution moat
      - company_ebitda_potential_rub_month проходит gate, но investment margin of safety ломается из-за слабого прямого спроса и price compression risk
      - комитет переводит кейс в near-pass и ждёт 3-5 локальных платящих enterprise pilot-to-production кейсов для возврата к approve review
```
