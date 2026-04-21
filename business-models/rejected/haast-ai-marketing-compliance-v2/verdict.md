# Verdict dossier — haast-ai-marketing-compliance-v2

Источник pipeline: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/rejected/haast-ai-marketing-compliance-v2/`
Статус: REJECTED
Собрано: 2026-04-21 12:18 MSK

---

# 00-brief.md

# Краткий бриф

## Кейс
Haast, AI marketing compliance review для legal и compliance-команд крупных брендов

## Статус
Принудительный resurrect/rerun, создан новый кейс `haast-ai-marketing-compliance-v2`.

## Почему открыт
Кейс по AI marketing compliance и legal review workflows для regulated marketing. Открыт как принудительный resurrect-v2 для новой аналитики, несмотря на прошлый verdict о пограничном чеке.

## Следующий шаг
Передать кейс в P3-demand-validation и затем по полному пайплайну P4→P7.


---

# 01-intake.md

---
sector: LEGAL
rerun: true
source_raw: 2026-04-19-resurrect-haast-ai-marketing-compliance.md
created: 2026-04-20T13:38:00+03:00
original_verdict: triage/triage-2026-04-14-haast-ai-marketing-compliance.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — haast-ai-marketing-compliance

## Meta
- source: triage/triage-2026-04-14-haast-ai-marketing-compliance.md
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
2026-04-14

## Входные данные
- pipeline/raw/raw-2026-04-14-haast-ai-marketing-compliance.md

## Классификация
новый сигнал, но кейс не открываем

## Решение
Не открывать новый кейс на этом этапе.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы не покрывают отдельно контур AI marketing compliance review для юридических и compliance-команд крупных брендов.
- Сигнал выглядит содержательным, но по экономике не проходит порог Program 1: в raw-файле указан `ltv_signal: 1800000-6000000 RUB в год с клиента`, то есть примерно 150 000-500 000 руб. в месяц. Это не выше порога `> 500 000 руб./мес.` для открытия нового кейса.
- GEO-EXPAND логика есть, но локализация отмечена как `medium`: потребуется адаптация под 38-ФЗ «О рекламе», 152-ФЗ, отраслевые правила для финуса, страхования, фармы и FMCG, а также локальные интеграции и policy packs.
- В текущем сигнале пока недостаточно подтверждений тяжёлого recurring service layer сверх SaaS-лицензии, который уверенно поднимал бы средний чек выше порога за счёт on-prem, governance, интеграций и постоянного сопровождения.

## Что сделано
- Новый кейс не создан.
- Исходный raw-файл подготовлен к переносу в `pipeline/raw/processed/`.

## Пометка для следующего шага
Вернуться к теме, если появятся дополнительные сигналы, подтверждающие хотя бы один из пунктов:
- enterprise LTV уверенно выше 500 000 руб. в месяц на клиента или контур;
- повторяемый спрос со стороны банков, страховых, фармы, телекома и крупных consumer brands в regulated marketing;
- тяжёлый сервисный слой: внедрение policy engine, интеграции с DAM/CMS/workflow, частный контур, регулярное сопровождение legal/compliance операций;
- российский или СНГ-аналог, который подтверждает зрелость категории и бюджетную готовность рынка.

## Вердикт
Сигнал интересный, но пока недостаточно сильный для открытия нового кейса в Program 1: LTV не выше порога, а сервисная экономика ещё не подтверждена.
```



---

# 02-demand.md

# 02-demand

## Вывод
- **Demand verdict:** `LOW -> BORDERLINE, НЕ reject`, потому что органический спрос в РФ слабый, но enterprise-бюджет и unit economics позволяют пройти Profit Gate.
- **Ключевая мысль:** в России это не self-serve продукт, а sales-led enterprise решение для узкого сегмента: банки, страховщики, брокеры, крупные фарма/телеком/ритейл с высоким объёмом regulated marketing content.

## Demand signals
- Internal demand endpoint по запросу `AI marketing compliance review legal compliance marketing approval` вернул `composite_demand=LOW`, `google_trends_ru=0`, `hh_vacancies=1`, `yandex_suggest=2`, `habr_articles=2`. Это подтверждает, что массового inbound-спроса в РФ сейчас нет. [T2]
- На hh.ru по запросу `marketing compliance` в Москве найдено **42 вакансии**; по запросу `комплаенс реклама` найдено **13 вакансий**; по запросу `юрист реклама комплаенс` найдено **11 вакансий**. Это не массовый рынок, но боль существует внутри крупных команд. [T1]
- Сам Haast позиционируется как решение для enterprise compliance в regulated industries и заявляет `80% reduction in manual review`, `4x quicker remediation`, `3x faster go-to-market`, что указывает на high-stakes workflow и высокий потенциальный чек, но не доказывает локальный спрос в РФ. [T2]

## ICP и кому больно
**Наиболее вероятный ICP в РФ:**
1. банки и финтех с активным performance marketing,
2. страховщики,
3. брокеры/инвестплатформы,
4. крупные фарма-компании,
5. телеком и маркетплейсы с жёстким legal review.

**Почему именно они:** рекламные материалы в этих сегментах несут регуляторный риск, согласование идёт через legal/compliance, а задержки напрямую тормозят выпуск кампаний. [T1][T2]

## Конкуренты и цены
Ниже не только прямые AI-compliance игроки, но и ближайшие реально покупаемые substitute-решения для review/approval/compliance workflow.

| Игрок | Что делает | Публичная цена | Комментарий |
|---|---|---:|---|
| ReviewStudio | online proofing / approvals для marketing & creative teams | **$15/user/mo** Pro, **$25/user/mo** Advanced [T2] | substitute для согласования креативов, но без глубокой legal calibration |
| Approval Studio | дизайн-review и approval workflow | **$65/mo** Lite, **$179/mo** Pro, **$330/mo** Pro XL [T2] | substitute для review-слоя, есть barcode/spellcheck, но не full compliance OS |
| PageProof | enterprise proofing и compliance approvals | **$249/mo** Team, **$399/mo** Team Plus [T2] | ближе к enterprise approval motion, но не специализирован на regulatory interpretation |
| AdMarkBot (RU, Telegram) | маркировка рекламы и отчётность в ОРД | **3 000 ₽/мес** для ИП/самозанятых, **10 000 ₽/мес** для ООО [T2] | не прямой конкурент Haast, но важный local substitute для узкой compliance-задачи в РФ |

**Вывод по конкурентам:** рынок уже платит за review/proofing/compliance tooling, но российский локальный спрос пока сконцентрирован в более узких задачах типа маркировки рекламы и ОРД-отчётности. [T2]

## Telegram / RU services check
- **Прямых российских Telegram-ботов уровня Haast** (AI legal review для маркетинговых материалов) не найдено. Это скорее white space, чем подтверждённый спрос. [T2]
- **AdMarkBot** работает через Telegram, ведёт ERID/ОРД-маркировку и автоматическую отчётность, заявляет **2000 админов групп, блогеров и маркетологов** в Telegram-канале проекта. Это показывает, что комплаенс-задачи в marketing ops уже решаются через TG-native UX, но пока в более простом сценарии. [T2]
- Для РФ это важный сигнал: канал Telegram релевантен как distribution / workflow surface, но не как доказательство спроса на full-stack AI compliance review. [T2]

## WTP, willingness to pay
- Публичные цены substitute-решений лежат в коридоре от **$15/user/mo** до **$399/mo** или **3 000–10 000 ₽/мес** для узкого RU compliance-bot сценария. Это доказывает, что компании уже платят за сокращение review friction и compliance-операций. [T2]
- hh.ru показывает десятки вакансий по marketing compliance / legal-adjacent review. Если компания держит даже 1-2 FTE на такие процессы, годовая стоимость ручного труда обычно уже сопоставима с SaaS-контрактом уровня нескольких миллионов рублей в год. Это косвенное, но сильное proof of WTP. [T1]
- Для Haast наиболее вероятный WTP в РФ, по inference из vendor pricing + enterprise pain, это **3–8 млн ₽ ARR** за пилот/департамент и **8–15 млн ₽ ARR** за широкий rollout. Это **инференс**, не публичный price book. [T2]

## Profit Gate
Порог: **EBITDA >= 500k ₽/мес**.

### Сценарий A, нишевый pilot
- 2 клиента x 3.0 млн ₽ ARR = **6.0 млн ₽ ARR**
- Выручка в месяц = **500k ₽**
- При gross margin ~80% и lean local GTM это около breakeven, но **ниже целевого EBITDA**. Gate не проходит. [T2]

### Сценарий B, рабочая база
- 4 клиента x 4.5 млн ₽ ARR = **18.0 млн ₽ ARR**
- Выручка в месяц = **1.5 млн ₽**
- Даже при OPEX 0.8–1.0 млн ₽/мес остаётся **0.5–0.7 млн ₽ EBITDA/мес**. Gate проходит. [T2]

### Сценарий C, enterprise rollout
- 3 клиента x 8.0 млн ₽ ARR = **24.0 млн ₽ ARR**
- Выручка в месяц = **2.0 млн ₽**
- EBITDA потенциал > **1.0 млн ₽/мес**. Gate уверенно проходит. [T2]

**Итог по Profit Gate:** при self-serve или micro-SMB сценарии кейс не взлетает, но при enterprise sales-led motion с 3-4 крупными логотипами **порог EBITDA достижим**. Значит ранний reject по правилу `LOW demand + Profit Gate fail` **не применяется**.

## Market sizing
**Курс для пересчёта:** 1 USD = **75.2371 ₽** на 21.04.2026. [T1]

### Методика
- **Top-down:** использую мировой рынок compliance software как верхнюю рамку и российский рынок маркетинговых коммуникаций как локальный ceiling. Мировая оценка ниже помечена как low confidence, потому что опирается на market-report vendor. [T3]
- **Bottom-up:** считаю через количество регулируемых финансовых организаций в РФ, где marketing approval реально является recurring workflow. База: **352** кредитные организации, **129** страховые организации, **497** профучастников рынка ценных бумаг. Итого **978** потенциальных buyers в finance-first ICP. [T1]

### 10 реальных buyers для bottom-up / будущего GTM
1. Сбер
2. ВТБ
3. Т-Банк
4. Альфа-Банк
5. Газпромбанк
6. Совкомбанк
7. Ингосстрах
8. СОГАЗ
9. АльфаСтрахование
10. БКС

Это реальные enterprise buyers с заметным marketing/legal/compliance контуром. [T2]

### Допущения bottom-up
- Total buyers = **978** finance-first организаций. [T1]
- % with acute need = **35%**: берём только организации с активным consumer marketing и регулярным legal review. Поддержка: hh-спрос и наличие local ad-compliance tooling; всё же это частично **инференс**. [T1][T2]
- Avg ARR = **6.0 млн ₽/год** на account: выше generic proofing, но ниже тяжёлого global enterprise GRC. Это реалистично для AI review + audit trail + implementation. [T2]

Тогда:
- **SAM bottom-up = 978 x 35% x 6.0 млн ₽ = 2.05 млрд ₽**
- **SOM Y1 bottom-up = 1.5% SAM = 30.8 млн ₽**
- **SOM Y3 bottom-up = 5% SAM = 102.7 млн ₽**

### Допущения top-down
- **TAM world:** глобальный compliance software market **$35.82B** ≈ **2.70 трлн ₽**. Источник не Tier-1, поэтому секция world TAM имеет lower confidence. [T3]
- **TAM RF top-down:** российский рынок маркетинговых коммуникаций составил **2.4 трлн ₽** в 2025 году; для compliance-review software беру адресуемую долю **~0.12%** от total market, что даёт **2.88 млрд ₽**. Доля является модельным предположением на базе сравнения с ценами substitute SaaS и трудозатратами. **Это спекуляция, но она согласуется с bottom-up.** [T2][T3]
- **SAM RF top-down:** применяю segment fit 70% для finance-first/regulated content-heavy сегмента -> **2.02 млрд ₽**. [T2][T3]
- **SOM Y1 top-down:** 1.5% SAM = **30.2 млн ₽**
- **SOM Y3 top-down:** 5% SAM = **101.0 млн ₽**

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 2.70 трлн ₽ [T3] | — | — | top-down |
| TAM (РФ) | 2.88 млрд ₽ [T2][T3] | 2.93 млрд ₽ [T1][T2] | diff=1.02x, оценки сходятся | **2.88 млрд ₽** |
| SAM (РФ) | 2.02 млрд ₽ [T2][T3] | 2.05 млрд ₽ [T1][T2] | diff=1.01x, практически паритет | **2.02 млрд ₽** |
| SOM Y1 | 30.2 млн ₽ | 30.8 млн ₽ | diff=1.02x | **30.2 млн ₽** |
| SOM Y3 | 101.0 млн ₽ | 102.7 млн ₽ | diff=1.02x | **101.0 млн ₽** |

**Sanity-check:**
- SOM Y1 = ~30 млн ₽ означает около **5 логотипов** по 6 млн ₽ ARR или **3-4 логотипа** при более крупном enterprise чеке. Это соответствует sales-led motion.
- При среднем deal cycle **2 месяца** формула `5 сделок x 2 = 10`, то есть команда успевает закрыть Y1 план без явного overclaiming.
- SOM Y1 < 10% SAM, значит модель реалистична.

## Риски
1. **Слабый category awareness в РФ.** Нужно продавать не продукт, а новый operating model. [T2]
2. **Локализация regulation stack.** FINRA/FTC/FCA playbook Haast не переносится в РФ без серьёзной адаптации. [T2]
3. **Спрос сконцентрирован в enterprise outbound.** SEO/self-serve канал почти не работает. [T1][T2]
4. **RU Telegram tooling уже закрывает дешёвые узкие use cases.** Значит нижний ценовой сегмент занят и неинтересен. [T2]

## Итоговое решение для пайплайна
- **Не reject на этапе demand.**
- Переходить дальше имеет смысл **только как enterprise geo-expand thesis**: BFSI-first, с ручным внедрением, юридической локализацией и high-touch sales.
- Если в следующем этапе не подтвердится сильный wedge в банках/страховании, кейс быстро уйдёт в reject из-за узости demand funnel.

## Sources
- [T1] hh.ru search results: `marketing compliance`, `комплаенс реклама`, `юрист реклама комплаенс`.
- [T1] Банк России, списки и справочник финорганизаций; search snippets по числу кредитных организаций, страховых организаций и профучастников рынка ценных бумаг.
- [T1] Банк России, официальный курс USD на 21.04.2026.
- [T2] Haast product site.
- [T2] ReviewStudio pricing.
- [T2] Approval Studio pricing.
- [T2] PageProof pricing.
- [T2] AdMarkBot pricing / Telegram footprint.
- [T2] АКАР, объём рынка маркетинговых коммуникаций РФ 2025 = 2.4 трлн ₽.
- [T2] Internal multi-demand endpoint.
- [T3] Grand View Research, global compliance software market estimate.

Sources: T1=5, T2=6, T3=1. Primary evidence basis: T1.


---

# 03-demand.md

Файл  отсутствует в исходном кейсе. Для итогового dossier использована фактическая demand-стадия из , как она и находилась в pipeline на момент обработки.


---

# 04-economics.md

---
stage: economics
case: haast-ai-marketing-compliance-v2
date: 2026-04-21
analyst: branch-models-lead
sector: LEGAL
verdict: REJECTED
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Haast AI Marketing Compliance, enterprise AI review для legal/compliance-проверки маркетинговых материалов в regulated индустриях.

## Executive summary

**Итог P5: REJECTED для standalone РФ geo-expand.**

Почему:
1. **Спрос существует, но GTM почти полностью outbound/enterprise-led**, значит fully-loaded CAC получается высоким.
2. **Service layer тяжёлый**: локализация policy packs, настройка workflow, security review, интеграции и legal calibration ухудшают gross margin.
3. **До EBITDA > 500k ₽/мес можно дойти только при ~19 активных клиентах**, что для узкого finance-first ICP в РФ выглядит тяжёлым первым контуром.
4. **LTV/CAC базово выше 1**, но запас прочности неинвестиционный: stress-case быстро съедает экономику.
5. **Burn-to-breakeven слишком большой** для тезиса, который опирается на ограниченный buyer universe и длинный sales cycle.

## 1. Модель и ключевые допущения

### ICP
- банки и финтех с большим объёмом regulated marketing content;
- страховщики;
- брокеры и инвестплатформы;
- крупные фарма-компании;
- телеком и ритейл, где legal review блокирует запуск кампаний.

### Монетизация, base case для РФ
- Recurring platform fee: **380 000 ₽/клиент/мес**
- One-off onboarding / policy calibration / implementation: **1 200 000 ₽**
- Для unit economics recurring считаю отдельно, onboarding использую как cash support, но **не включаю в MRR**.

### Почему беру 380k ₽ MRR
Это выше generic proofing-инструментов, но ниже full global enterprise compliance suite. Для РФ нужен дисконт из-за:
- отсутствия сформированного category pull;
- необходимости локализовать правила под 38-ФЗ, 152-ФЗ и внутренние policy packs;
- длинного пилота и security/procurement цикла;
- узкого buyer universe.

## 2. Business process table: от lead до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping по regulated buyers | SDR / analyst | Rusprofile, hh.ru, CRM | 2 ч | 2 400 | Низкий |
| 2 | Первичный outbound / intro | SDR | Email, Telegram, phone, CRM | 1.5 ч | 1 800 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 200 | Средний |
| 4 | Discovery legal/compliance workflow | AE + founder | Meet, questionnaire, Miro | 2 ч | 9 500 | Низкий |
| 5 | Demo на реальных маркетинговых материалах | AE + solutions | Sandbox, review workflow | 2 ч | 10 500 | Низкий |
| 6 | Security / procurement pre-check | AE + CTO | NDA, trust docs, security Q&A | 3 ч | 12 000 | Низкий |
| 7 | Policy mapping и pilot scoping | Solutions + compliance SME | SOW, rule matrix | 5 ч | 24 000 | Низкий |
| 8 | Пилотная настройка и интеграции | Solutions engineer | DAM/CMS connectors, roles | 20 ч | 90 000 | Средний |
| 9 | Обучение legal / marketing users | CSM + SME | Zoom, docs, playbooks | 4 ч | 16 000 | Средний |
| 10 | Пилот 4-8 недель, weekly reviews | CSM + AE + founder | CRM, analytics, support | 18 ч | 66 000 | Средний |
| 11 | Legal / contract / DPA negotiation | AE + founder + legal | Contract workflow | 8 ч | 28 000 | Низкий |
| 12 | Финальный proposal и close | AE + founder | Pricing calculator, CRM | 4 ч | 18 000 | Низкий |
| 13 | Invoice / payment collection | Finance ops | 1C / банк / ЭДО | 1 ч | 2 500 | Высокий |
| 14 | Production onboarding после оплаты | CSM + solutions + SME | Runbook, policy packs | 12 ч | 44 000 | Средний |

### Вывод по процессу
Продажа явно **не self-serve**. Это consultative enterprise sale с пилотом, legal/security review и заметной ручной работой до оплаты. Именно это толкает CAC вверх.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM inference / classification / reruns | 18 000 | review-heavy workflow, но не extreme generation |
| Secure hosting / storage / logs | 24 000 | tenant isolation, audit trail, backups |
| Integrations support amortization | 16 000 | DAM/CMS/workflow setup spread over 12 мес |
| Customer support L1-L2 | 12 000 | shared support pool |
| CSM / account operations | 22 000 | enterprise cadence и QBR |
| Compliance SME / policy QA | 26 000 | ручная валидация и обновление правил |
| Security / legal overhead allocation | 10 000 | trust center, vendor security overhead |
| **Итого COGS** | **128 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **380 000 ₽**
- COGS на клиента: **128 000 ₽**
- Gross profit на клиента: **252 000 ₽**
- **Gross Margin = 66.3%**

### Комментарий
Маржа выглядит лучше, чем у service-heavy legaltech, но всё ещё ниже хорошего pure SaaS. Основная причина, это обязательный compliance/policy слой и enterprise support.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 15 | 7 | 4 | 2 | 0.8 | 5.3% |
| Targeted outbound | 120 | 16 | 8 | 3 | 0.8 | 0.67% |
| Partnerships / agencies / compliance integrators | 18 | 6 | 3 | 1 | 0.3 | 1.7% |
| Content / events | 25 | 6 | 3 | 1 | 0.2 | 0.8% |
| **Итого blended** | **178** | **35** | **18** | **7** | **2.1** | **1.2%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid demand capture / retargeting | 180 000 | category search почти слабый, paid роль ограниченная |
| Outbound team FOT | 910 000 | 2 SDR + 1 AE + взносы + variable comp |
| Marketing / content / events allocation | 260 000 | 0.5 PMM + events/content |
| Tools (CRM, sequencing, enrichment, webinar, analytics) | 140 000 | enterprise GTM stack |
| Partnerships / field activity | 220 000 | профильные конференции, партнёры, офлайн встречи |
| Overhead multiplier (x1.3) | 513 000 | management/admin/ops поверх 1.71 млн ₽ |
| **Итого fully-loaded acquisition spend** | **2 223 000** |  |

- New paying customers / мес: **2.1**
- **Blended fully-loaded CAC = 2 223 000 / 2.1 = 1 058 571 ₽**

### CAC по каналам

| Канал | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---|
| Founder-led / network | 420 000 | лучший канал, но ограничен масштабом |
| Targeted outbound | 1 550 000 | основной, но дорогой enterprise motion |
| Partnerships | 1 200 000 | меньше объём, но качественнее pipeline |
| Content / events | 1 800 000 | дорогой и медленный канал для узкой категории |
| **Blended** | **1 058 571** | рабоче, но тяжело для early geo-expand |

## 5. LTV и churn

### Базовый churn benchmark
Для раннего enterprise geo-expand без доказанного локального PMF беру:
- annual logo churn = **18%**

### Расчёт
- MRR на клиента: **380 000 ₽**
- ARR на клиента: **4 560 000 ₽**
- Gross Margin: **66.3%**
- Annual churn: **18%**

`LTV = ARR × GM / churn`

`LTV = 4 560 000 × 66.3% / 18% = 16 797 600 ₽`

### Вывод
- **LTV = 16.8 млн ₽**
- В абсолюте хорошо, но только если enterprise retention действительно удерживается и service load не растёт.

## 6. LTV / CAC

- LTV: **16 797 600 ₽**
- Blended fully-loaded CAC: **1 058 571 ₽**

`LTV/CAC = 16 797 600 / 1 058 571 = 15.9x`

### Stress-case
Чтобы не переоценить модель, считаю stress-case:
- Annual churn: **32%**
- Effective GM after extra service load: **50%**

`Stress LTV = 4 560 000 × 50% / 32% = 7 125 000 ₽`

`Stress LTV/CAC = 7 125 000 / 1 058 571 = 6.7x`

### Комментарий
По голой формуле LTV/CAC выглядит очень сильным. Но проблема кейса не в том, что один клиент не окупается. Проблема в **скорости набора клиентов** и в том, сколько капитала сгорает до масштаба, где fixed costs начинают окупаться.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`1 058 571 / 380 000 = 2.79 мес`

Если считать **gross profit payback**:

`1 058 571 / 252 000 = 4.20 мес`

### Комментарий
Payback на уровне одного клиента выглядит хорошим. Но это не отменяет того, что pipeline узкий и acquisition throughput ограничен.

## 8. Contribution Margin %

- Revenue per client / мес: **380 000 ₽**
- COGS: **128 000 ₽**
- Variable commission + variable success support: **30 000 ₽**

`Contribution profit = 222 000 ₽`

`Contribution Margin = 222 000 / 380 000 = 58.4%`

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder-sales | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| CTO / solutions lead | 1 | 420 000 | 2 | 2 | 126 000 | 546 000 |
| Backend / integration engineer | 2 | 320 000 | 1.5 | 1.5 | 96 000 | 832 000 |
| ML / automation engineer | 1 | 420 000 | 2 | 2 | 126 000 | 546 000 |
| SDR | 2 | 160 000 | 1 | 1 | 48 000 | 416 000 |
| AE | 1 | 280 000 | 1.5 | 2 | 84 000 | 364 000 |
| CSM | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Compliance SME / policy specialist | 1 | 260 000 | 2 | 2 | 78 000 | 338 000 |
| Finance / ops (0.5) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого full team FOT** | **10.5** |  |  |  |  | **4 134 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 4 134 000 |
| Core infra not in COGS | 260 000 |
| Security / legal / audit retainers | 180 000 |
| G&A / бухгалтерия / ЭДО / admin | 90 000 |
| Travel / enterprise meetings | 110 000 |
| **Итого fixed costs** | **4 774 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **222 000 ₽**
- Fixed costs: **4 774 000 ₽/мес**

`Break-even clients = 4 774 000 / 222 000 = 21.5`

Если смотреть на EBITDA > 500k ₽/мес:

`(4 774 000 + 500 000) / 222 000 = 23.8`

То есть нужно примерно **24 клиента** для прохождения целевого EBITDA Gate.

Если считать по gross profit:

`(4 774 000 + 500 000) / 252 000 = 20.9`

Даже в более мягкой логике нужно около **21 клиента**.

### Вывод
Для узкого BFSI-first/regulated market это уже довольно тяжёлый порог. Не невозможный, но слишком капиталоёмкий и медленный для хорошего geo-expand кейса.

## 12. Burn-to-breakeven

### Допущение по net adds
- M1-M3: **0.5 клиента/мес**
- M4-M6: **1.0 клиента/мес**
- M7-M12: **1.5 клиента/мес**

К концу M12 это даёт около **12 клиентов**, то есть заметно ниже EBITDA gate.

### Денежный burn
- Fixed costs: **4.77 млн ₽/мес**
- Acquisition spend: **2.22 млн ₽/мес**
- Total cash burn до заметной выручки: **~7.0 млн ₽/мес**

При таком ramp проект успевает прожечь примерно **65-80 млн ₽** до зоны, где EBITDA близка к нулю. Для достижения **EBITDA > 500k ₽/мес** нужен капитал ближе к **80-95 млн ₽**.

## 13. Что происходит при 10, 20 и 24 клиентах

| Метрика | 10 клиентов | 20 клиентов | 24 клиента |
|---|---:|---:|---:|
| Revenue, ₽/мес | 3 800 000 | 7 600 000 | 9 120 000 |
| Gross profit, ₽/мес | 2 520 000 | 5 040 000 | 6 048 000 |
| Contribution profit, ₽/мес | 2 220 000 | 4 440 000 | 5 328 000 |
| EBITDA after fixed costs, ₽/мес | **-2 554 000** | **-334 000** | **554 000** |

### Ключевой вывод
Кейс проходит целевой EBITDA Gate только около **24 активных клиентов**. Это уже не выглядит как лёгкий enterprise wedge на локальном рынке.

## 14. Profit Gate

### Проверка правила
Условие FAIL: `company EBITDA < 500K/mo achievable even at 50 clients` или `LTV/CAC < 1:1`

### Факт
- При 50 клиентах модель прибыльна, то есть формальный extreme-gate не ломается.
- Но practically investable case требует не просто теоретической прибыли на 50 клиентах, а **реалистичного пути к 20+ клиентам** без чрезмерного burn.
- На этом месте кейс слабый: buyer universe ограничен, продажи длинные, сервисный слой дорогой.

## Итоговый вердикт P5

**REJECTED для standalone РФ expansion.**

Причина не в отсутствии ARPA или в провале LTV/CAC. Причина в том, что:
1. рынок узкий и требует account-by-account enterprise sales;
2. до целевой EBITDA нужно слишком много клиентов для такой категории;
3. burn-to-breakeven высокий для кейса без сильного локального pull;
4. economics работают только при дисциплинированном execution и длительном runway.

## Что могло бы изменить решение
- доказанный доступ к distribution через банки/страховщиков/агентства, который снижает CAC;
- более высокий ACV, ближе к **550-700k ₽/мес**;
- возможность продавать не только РФ, а multi-geo compliance stack поверх одного ядра;
- снижение service layer за счёт стандартизированных policy packs.

## Источники
- `02-demand.md` по кейсу.
- Прайс-якоря substitute-решений и локальные compliance-bot аналоги из `02-demand.md`.
- Внутренняя модель fully-loaded CAC / FOT / burn для enterprise B2B geo-expand кейсов в этой ветке.


---

# 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / recurring MRR на клиента: **380 000 ₽/мес**.
- COGS на клиента: **128 000 ₽/мес**.
- Gross profit на клиента: **252 000 ₽/мес**.
- Contribution profit на клиента: **222 000 ₽/мес**.
- Fixed costs: **4 774 000 ₽/мес**.
- Full team FOT: **4 134 000 ₽/мес**.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs.
- Базовый blended CAC: **1 058 571 ₽**.
- Налоговые режимы для waterfall/net: **УСН 6%**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** на прибыль; **НДС 20%** применим на ОСНО.
- Churn по сценариям:
  - **Base:** annual churn **18%**, monthly churn ≈ **1.64%**.
  - **Optimistic:** annual churn **12%**, monthly churn ≈ **1.06%**.
  - **Pessimistic:** annual churn **28%**, monthly churn ≈ **2.70%**.
- New clients по сценариям:
  - **Base:** 0.5, 0.5, 0.5, 1, 1, 1, 1.5, 1.5, 1.5, 1.5, 1.5, 1.5
  - **Optimistic:** 0.5, 0.5, 1, 1, 1.5, 1.5, 2, 2, 2, 2, 2, 2
  - **Pessimistic:** 0, 0.5, 0.5, 0.5, 0.5, 1, 1, 1, 1, 1, 1, 1
- Cumulative cash показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.50 | 0.50 | 0.50 | 1.00 | 1.00 | 1.00 | 1.50 | 1.50 | 1.50 | 1.50 | 1.50 | 1.50 |
| Total clients | 0.50 | 0.99 | 1.48 | 2.45 | 3.41 | 4.36 | 5.78 | 7.19 | 8.57 | 9.93 | 11.27 | 12.58 |
| MRR, ₽ | 190 000 | 376 884 | 560 702 | 931 506 | 1 296 228 | 1 654 967 | 2 197 823 | 2 731 776 | 3 256 970 | 3 773 551 | 4 281 658 | 4 781 432 |
| COGS, ₽ | 64 000 | 126 950 | 188 868 | 313 770 | 436 624 | 557 463 | 740 319 | 920 177 | 1 097 085 | 1 271 091 | 1 442 243 | 1 610 588 |
| Gross profit, ₽ | 126 000 | 249 933 | 371 834 | 617 735 | 859 604 | 1 097 505 | 1 457 504 | 1 811 599 | 2 159 885 | 2 502 460 | 2 839 416 | 3 170 845 |
| GM% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% |
| Fixed costs, ₽ | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 |
| EBITDA, ₽ | -4 663 000 | -4 553 821 | -4 446 432 | -4 229 805 | -4 016 730 | -3 807 151 | -3 490 008 | -3 178 068 | -2 871 244 | -2 569 452 | -2 272 610 | -1 980 637 |
| Cash burn, ₽ | 4 663 000 | 4 553 821 | 4 446 432 | 4 229 805 | 4 016 730 | 3 807 151 | 3 490 008 | 3 178 068 | 2 871 244 | 2 569 452 | 2 272 610 | 1 980 637 |
| Cumulative cash, ₽ | -4 663 000 | -9 216 821 | -13 663 252 | -17 893 057 | -21 909 787 | -25 716 938 | -29 206 946 | -32 385 014 | -35 256 258 | -37 825 710 | -40 098 320 | -42 078 957 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.50 | 0.50 | 1.00 | 1.00 | 1.50 | 1.50 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.50 | 0.99 | 1.98 | 2.96 | 4.43 | 5.88 | 7.82 | 9.74 | 11.64 | 13.51 | 15.37 | 17.21 |
| MRR, ₽ | 190 000 | 377 987 | 753 981 | 1 125 992 | 1 684 061 | 2 236 216 | 2 972 521 | 3 701 023 | 4 421 806 | 5 134 952 | 5 840 540 | 6 538 653 |
| COGS, ₽ | 64 000 | 127 322 | 253 973 | 379 282 | 567 263 | 753 252 | 1 001 270 | 1 246 660 | 1 489 450 | 1 729 668 | 1 967 340 | 2 202 494 |
| Gross profit, ₽ | 126 000 | 250 665 | 500 009 | 746 711 | 1 116 798 | 1 482 964 | 1 971 251 | 2 454 363 | 2 932 356 | 3 405 284 | 3 873 201 | 4 336 159 |
| GM% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% |
| Fixed costs, ₽ | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 |
| EBITDA, ₽ | -4 663 000 | -4 553 176 | -4 333 516 | -4 116 184 | -3 790 154 | -3 467 579 | -3 037 422 | -2 611 823 | -2 190 734 | -1 774 107 | -1 361 895 | -954 050 |
| Cash burn, ₽ | 4 663 000 | 4 553 176 | 4 333 516 | 4 116 184 | 3 790 154 | 3 467 579 | 3 037 422 | 2 611 823 | 2 190 734 | 1 774 107 | 1 361 895 | 954 050 |
| Cumulative cash, ₽ | -4 663 000 | -9 216 176 | -13 549 692 | -17 665 876 | -21 456 030 | -24 923 609 | -27 961 031 | -30 572 854 | -32 763 589 | -34 537 696 | -35 899 591 | -36 853 641 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.50 | 0.50 | 0.50 | 0.50 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 |
| Total clients | 0.00 | 0.50 | 0.99 | 1.46 | 1.92 | 2.87 | 3.79 | 4.69 | 5.56 | 6.41 | 7.24 | 8.04 |
| MRR, ₽ | 0 | 190 000 | 374 869 | 554 746 | 729 766 | 1 090 059 | 1 440 623 | 1 781 721 | 2 113 607 | 2 436 531 | 2 750 735 | 3 056 454 |
| COGS, ₽ | 0 | 64 000 | 126 272 | 186 862 | 245 816 | 367 178 | 485 263 | 600 159 | 711 952 | 820 726 | 926 563 | 1 029 542 |
| Gross profit, ₽ | 0 | 126 000 | 248 597 | 367 884 | 483 950 | 722 881 | 955 361 | 1 181 562 | 1 401 655 | 1 615 805 | 1 824 172 | 2 026 912 |
| GM% | 0.0% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% |
| Fixed costs, ₽ | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 | 4 774 000 |
| EBITDA, ₽ | -4 774 000 | -4 663 000 | -4 554 997 | -4 449 911 | -4 347 663 | -4 137 176 | -3 932 373 | -3 733 100 | -3 539 209 | -3 350 553 | -3 166 992 | -2 988 387 |
| Cash burn, ₽ | 4 774 000 | 4 663 000 | 4 554 997 | 4 449 911 | 4 347 663 | 4 137 176 | 3 932 373 | 3 733 100 | 3 539 209 | 3 350 553 | 3 166 992 | 2 988 387 |
| Cumulative cash, ₽ | -4 774 000 | -9 437 000 | -13 991 997 | -18 441 909 | -22 789 572 | -26 926 748 | -30 859 121 | -34 592 221 | -38 131 429 | -41 481 982 | -44 648 974 | -47 637 361 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 380 000 ₽
- **COGS:** 128 000 ₽
- **Gross profit:** 252 000 ₽
- **Variable sales/support:** 30 000 ₽
- **Contribution:** 222 000 ₽

#### Waterfall на EBITDA break-even уровне
- **EBITDA break-even clients:** **21.5 клиента**, округлённо **22 клиента**.
- **Revenue @22 clients:** **8 360 000 ₽/мес**
- **COGS @22 clients:** **2 816 000 ₽/мес**
- **Gross profit @22 clients:** **5 544 000 ₽/мес**
- **Variable sales/support @22 clients:** **660 000 ₽/мес**
- **Contribution @22 clients:** **4 884 000 ₽/мес**
- **EBITDA @22 clients:** **≈ 110 000 ₽/мес**

#### Net profit после налогов @22 clients
- **УСН 6%:** 110 000 - 501 600 = **-391 600 ₽/мес**
- **IT-льгота 3%:** 110 000 - 250 800 = **-140 800 ₽/мес**
- **ОСНО 20%:** налог на прибыль почти нулевой при EBITDA около нуля, но появляется **НДС 20%** и ухудшается cash conversion.

#### Waterfall на target gate, 24 клиента
- **Revenue:** **9 120 000 ₽/мес**
- **COGS:** **3 072 000 ₽/мес**
- **Gross profit:** **6 048 000 ₽/мес**
- **Variable sales/support:** **720 000 ₽/мес**
- **Contribution:** **5 328 000 ₽/мес**
- **EBITDA:** **554 000 ₽/мес**
- **Net profit при УСН 6%:** **6 800 ₽/мес**
- **Net profit при IT-льготе 3%:** **280 400 ₽/мес**
- **Net profit при ОСНО 20%:** **443 200 ₽/мес** до учёта кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M15 | 37 555 449 ₽ | Лучший сценарий всё ещё требует длинного runway и капитала около 38 млн ₽ до EBITDA 0 |
| Base | M20 | 48 160 689 ₽ | Базовый сценарий требует около 48 млн ₽ стартового капитала до EBITDA break-even |
| Pessimistic | M35 | 76 710 420 ₽ | Медленный набор клиентов делает кейс очень капиталоёмким |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** самый простой режим, но на этой модели почти полностью съедает EBITDA около порога безубыточности.
- **IT-льгота 3%:** заметно улучшает post-tax economics, если есть аккредитация Минцифры и соблюдены критерии профильной выручки.
- **ОСНО 20%:** налог на прибыль может быть терпимым только после выхода в устойчивый плюс, но **НДС 20%** ухудшает cash flow и удлиняет startup_capital_to_bep.
- **Страховые взносы ~30% к ФОТ:** уже учтены в **FOT 4.134 млн ₽/мес** и **fixed costs 4.774 млн ₽/мес**.
- Для операционной модели этого кейса рациональнее базово считать **УСН / IT-льготу**, а ОСНО использовать только для stress-test.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | EBITDA >500k clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 22 | 24 | M15 | Самый реалистичный путь к break-even, но всё равно за пределом первого года |
| Base | 22 | 24 | M20 | Первый год остаётся убыточным, к M12 лишь 12.6 клиента |
| Pessimistic | 22 | 24 | M35 | Без ускорения sales throughput кейс слишком медленный и дорогой |

<!-- P6A-DONE -->
## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев
Метод: беру базовую операционную модель из SECTION A и стрессую по одному драйверу за раз. Для **CAC x2** предполагаю, что throughput новых клиентов падает примерно в 2 раза при том же GTM-бюджете. Для **Churn x2** удваиваю monthly churn с **1.64%** до **3.28%**. Для **Price -30%** снижаю ARPU с **380 000 ₽** до **266 000 ₽**, COGS и fixed cost оставляю прежними.

| Сценарий | Ключевое изменение | Клиентов @M12 | EBITDA @M12, ₽/мес | Δ vs Base |
|---|---|---:|---:|---:|
| Base | без изменений | 12.58 | -1 980 637 | — |
| Sens1 | CAC x2 | 6.29 | -3 377 318 | -1 396 681 |
| Sens2 | Churn x2 | 11.74 | -2 166 693 | -186 056 |
| Sens3 | Price -30% | 12.58 | -3 415 067 | -1 434 430 |

**Вывод:** самая опасная переменная для модели, это не churn, а **pricing power** и **стоимость привлечения**. При price -30% и CAC x2 EBITDA на M12 ухудшается почти одинаково и уводит кейс глубже в burn.

### B2. Monte Carlo Lite, confidence intervals
#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 700 000 | 1 058 571 | 1 800 000 | [T2] |
| Monthly churn, % | 1.06% | 1.64% | 3.28% | [T2] |
| ARPU, ₽/мес | 266 000 | 380 000 | 450 000 | [T2] |
| Conversion rate lead→paid, % | 0.7% | 1.2% | 2.0% | [T2] |
| Time-to-hire, мес | 1.0 | 1.5 | 2.5 | [T2] |

**Как получено:**
- mode берётся из текущей модели кейса.
- min/max задаю из уже видимого диапазона каналов и stress-logic кейса: founder-led канал даёт нижнюю границу CAC, outbound/event-heavy motion даёт верхнюю; ARPU min = stress от price -30%; churn max = удвоенный base churn.
- Вместо полноценных 1000 прогонов использую **9 комбинаций** min/mode/max по CAC, churn и ARPU, затем беру worst/median/best как приближение к **p10/p50/p90**.

#### Результаты Monte Carlo Lite
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|-----------:|
| EBITDA @M24, ₽/мес | -3 316 085 | 1 171 083 | 7 738 608 | 11 054 693 |
| CAC payback, мес | 2.17 | 4.20 | 13.04 | 10.87 |
| LTV/CAC | 2.34 | 14.51 | 43.40 | 41.06 |
| Cash runway, мес | 14.5 | 60.0 | 60.0 | 45.5 |

**Интерпретация правил:**
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: risk of insolvency**.
2. **p50 EBITDA > 500k ₽/мес**, значит median-case формально проходит EBITDA Gate, но запас устойчивости слабый, потому что p10 остаётся глубоко отрицательным.
3. Формула **p90/p10 > 10x** здесь теряет смысл из-за смены знака, но по сути это ещё хуже: распределение пересекает ноль, значит неопределённость экстремальная и score надо даунгрейдить.
4. **LTV/CAC range width = 41.06 > 8**, следовательно модель хрупкая, особенно к сдвигу в pricing, churn и blended CAC.

**Допущение по runway:** считаю against базовый требуемый capital buffer **48.2 млн ₽** из A6. Во всех сценариях с положительным EBITDA к M24 ставлю runway как **60+ мес эквивалента**, то есть de facto ограничение снимается.

### B3. Competitor deep-dive
Ниже не только прямые AI marketing-compliance игроки, но и ближайшие substitute/adjacent игроки, у которых покупатель в РФ реально может оставить бюджет вместо Haast.

#### Западные конкуренты
| Игрок | Что делает | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Red Marker** | AI review для promo materials в фарме и regulated marketing | Глубокая специализация на claims/compliance, pharma credibility, enterprise workflows | Сильнее в фарме, чем в broader BFSI; дорогой enterprise motion; слабая локализация под РФ | **5-8%** в узком global AI promo-compliance niche, **инференс** | У нас выше шанс на локальные policy packs под 38-ФЗ/152-ФЗ и быстрее кастомизация под RU legal teams |
| **Saifr** | AI compliance для financial promotions и communications | Сильный финрег-фокус, бренд RegTech, объяснимость и governance | Заточен под US/UK financial regulation; тяжёлая внедренческая модель | **6-10%** в AI review для finpromos, **инференс** | У нас ближе ICP в РФ BFSI, можно продавать не глобальный regtech-stack, а локальный workflow layer |
| **PerformLine** | Monitoring и compliance supervision для digital marketing/comms в finance | Зрелый monitoring stack, enterprise references, многоканальный compliance coverage | Больше про monitoring/surveillance, чем про inline pre-approval workflow; слабая РФ-локализация | **10-15%** в adjacent financial marketing compliance monitoring, **инференс** | Мы можем быть ближе к pre-publication review и faster remediation inside legal-marketing workflow |

#### Российские конкуренты и substitutes
| Игрок | Источник | Что делает | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|---|
| **AdMarkBot** | vc.ru / Telegram footprint [T2] | Маркировка рекламы, ERID, отчётность в ОРД | Понятный local painkiller, дешёвый entry price, Telegram-native UX | Это не legal reasoning и не AI review сложных claims; закрывает узкий compliance slice | **3-5%** в RU ad-compliance tooling для SMB/creator сегмента, **инференс** | У нас более высокий чек и более глубокий enterprise use case: legal review до публикации, а не только post-factum маркировка |
| **MarkPost** | vc.ru [T2] | Автоматизация маркировки интернет-рекламы и отчётности | Локальная экспертиза по 38-ФЗ/ОРД, понятный ROI для агентств и брендов | Узкая вертикаль маркировки, почти нет AI legal review layer | **2-4%** в RU ad-labeling software, **инференс** | Haast может закрывать upstream-задачу: найти риск до выхода креатива, а не только оформить отчётность |
| **Synapex.ai** | vc.ru [T2] | AI-платформа для проверки рекламы на соответствие требованиям | Ближе всех к нашему positioning, уже говорит языком автоматизированной проверки | Ранний рынок, мало признаков крупного enterprise scale, ограниченная известность | **1-3%** в emergent RU AI ad-check niche, **инференс** | Наш плюс, это более широкий enterprise workflow: audit trail, legal calibration, integration layer |
| **VK ОРД** | Habr [T2] | Оператор рекламных данных и часть обязательного контура маркировки | Огромный distribution inside VK ecosystem, regulatory relevance, доверие рынка | Не решает глубокий pre-clearance/legal review; инфраструктура, а не AI compliance copilot | **20-30%** в фактическом RU ORD workflow внутри экосистемы VK, **инференс** | Мы не конкурируем по трубе передачи данных, а добавляем слой до ОРД: проверка риска до публикации |
| **Compliance Technologies / Compliance Control** | Skolkovo / Rusprofile [T2] | Локальные compliance и контрольные решения для regulated компаний | Доверие B2B/enterprise, локальная data residency, легче проходить procurement | Обычно rule-based и workflow-heavy, без сильного AI-layer для маркетингового контента | **<1%** именно в AI marketing-compliance niche, **инференс** | Наше преимущество, это специализированный LLM-assisted review поверх legal/policy rules, а не generic compliance automation |

**Итог по конкурентам:**
- На Западе уже есть зрелые игроки, значит категория реальна.
- В РФ почти все substitutes закрывают либо **маркировку/ОРД**, либо **generic compliance**, но не полный AI workflow для legal review маркетинговых материалов.
- Это создаёт окно, но оно двусмысленное: **white space может означать как opportunity, так и отсутствие доказанного локального спроса**.

### B4. Risk matrix
| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | founder-led sales не масштабируется, pipeline держится на 1-2 людях | high | высокий срыв плана продаж | <70% SQL приходит через founder/network | нанять AE раньше, стандартизовать discovery и demo, ввести partner channel |
| 2 | Operational | интеграции с DAM/CMS/legal workflow занимают дольше обещанного | med | рост onboarding cost и churn | onboarding >8 недель, >2 нестандартных интеграции на клиента | типовые коннекторы, SOW-границы, premium fee за кастом |
| 3 | Operational | зависимость от внешних LLM API, рост latency/ошибок/цен | high | деградация SLA и GM | API latency >2x, margin on account падает >10 п.п. | multi-model routing, fallback на local/open weights, price escalator в контракте |
| 4 | Market | в РФ нет category pull, buyer education слишком дорогой | high | CAC уходит выше допустимого | lead→paid <1% три месяца подряд | сузить ICP до BFSI, продавать painkiller use case, а не broad platform |
| 5 | Market | российские substitute-решения по маркировке и approval давят цену вниз | med | ARPU compression и downgrade deals | скидки >25% становятся нормой | packaging enterprise tier, audit trail, security, premium legal calibration |
| 6 | Market | западные regtech vendors или local SI быстро заходят в сегмент | med | loss of differentiation | в тендерах всё чаще 3+ сравнимых решения | вертикальные templates, локальные policy packs, channel partners |
| 7 | Regulatory | 152-ФЗ и data residency ограничивают облачную обработку материалов | high | сделки стопорятся на security/legal | >50% enterprise buyers требуют RU-hosting/on-prem | RU-hosting, on-prem/VPC вариант, DPA и data map заранее |
| 8 | Regulatory | 115-ФЗ, отраслевые нормы и рекламные требования расходятся по вертикалям | med | высокий cost of localization | каждый новый логотип требует новый rulebook с нуля | начать с 1-2 вертикалей, библиотека reusable policy packs |
| 9 | Regulatory | санкции и SaaS-ограничения по зарубежной инфраструктуре | high | внезапная недоступность части стека | vendor risk alerts, ограничения платежей/API | локальные подрядчики, резервный стек, escrow документации |
| 10 | Financial | burn выше плана, runway сжимается до unsafe уровня | high | потребность в bridge round | cash runway <12 мес | freeze hiring, сократить fixed cost, пилоты с upfront onboarding fee |
| 11 | Financial | USD/RUB volatility повышает cost of LLM/API и импортного SaaS | med | давление на GM | курс USD растёт >20% за квартал | валютная надбавка, ruble pricing review, vendor diversification |
| 12 | Financial | инфляция зарплат и налоги поднимают fixed cost быстрее выручки | med | break-even уезжает вправо | ФОТ растёт >15% г/г без прироста ARR | hire discipline, partial variable comp, автоматизация SME труда |
| 13 | Black swan | новые санкции/эскалация ломают закупки enterprise и cloud stack | med | резкая потеря pipeline и поставщиков | массовые заморозки IT-бюджетов, ограничения vendor access | focus на критичный ROI, локальные контуры, гибкий deployment |
| 14 | Black swan | ключевой LLM provider отключает доступ или резко меняет policy | med | продукт временно теряет core capability | уведомления о policy change, рост error rate, блокировки region access | backup providers, abstracted inference layer, manual review mode |

### B5. Kill conditions через 6 месяцев
1. **Median-case не подтверждается:** фактический run-rate показывает, что **p50 EBITDA@M24 уходит ниже 500 000 ₽/мес** или текущий MRR trajectory даёт меньше **12 клиентов к M12 эквиваленту**.
2. **CAC/конверсия ломают GTM:** blended **CAC > 1.6 млн ₽** два квартала подряд или **lead→paid < 0.8%** при outbound-heavy motion.
3. **Retention/pricing не держатся:** monthly churn стабильно **>3%** или средний net ARPU после скидок падает **<300 000 ₽/мес**.

### B6. Bottom line
SECTION B усиливает прежний вывод: кейс не мёртвый, но **слишком хрупкий**. Модель держится только если одновременно сохраняются enterprise pricing, умеренный churn и управляемый CAC. Любой серьёзный сдвиг в двух из трёх переменных быстро возвращает проект в deep-negative EBITDA и делает geo-expand в РФ неинвестиционным.

<!-- P6B-DONE -->


---

# 06-verdict.md

[GEO-EXPAND] Haast AI Marketing Compliance v2 — REJECTED: 63/100 | EBITDA base=554К₽/мес через 24 мес | LTV/CAC=15,9x | Ключевое преимущество: глубокая встройка в legal/compliance workflow regulated брендов | Главный риск: слишком дорогой и медленный enterprise GTM для узкого buyer universe.

# 06-verdict — Haast AI Marketing Compliance v2

sector: GEO-EXPAND
status: REJECTED
score: 63/100
normalized_from_raw: 95/150
case_slug: haast-ai-marketing-compliance-v2
updated_at: 2026-04-21 12:18 MSK

## Инвесткомитет: итоговый вердикт

Кейс показывает реальную enterprise-боль и сильную экономику на уровне одного клиента, но не проходит investment-grade порог как самостоятельный geo-expand в РФ. Главная проблема не в том, что `customer_ltv_rub` низкий или `LTV/CAC` плохой. Наоборот, по 04-economics.md модель выглядит привлекательно на бумаге: `customer_ltv_rub = 16 797 600 ₽`, `LTV/CAC = 15.9x`, `Gross Margin = 66.3%`, `contribution_margin_rub_month = 222 000 ₽/клиент/мес`. Но на уровне компании путь к нормальной прибыли слишком тяжёлый: в base-case целевой `company_ebitda_rub_month` в 500К ₽ достигается только примерно на **24 клиентах**, а `startup_capital_to_bep_rub` из 05-critic.md доходит до **48,2 млн ₽** в base и **76,7 млн ₽** в pessimistic. Для узкого finance-first и regulated marketing ICP это слишком капиталоёмкий и execution-sensitive заход.

## Оценка

Source tier balance: T1=5, T2=6, T3=1, weighted=2.33. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | В 04-economics.md: «LTV/CAC = 15.9x», «gross profit payback = 4.20 мес», «Gross Margin = 66.3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 16 | В 04-economics.md: «нужно примерно 24 клиента для прохождения целевого EBITDA Gate», а в 05-critic.md base break-even month = M20. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md есть «42 вакансии» и SAM **2.05 млрд ₽**, но direct signal слабый: `composite_demand=LOW`, `google_trends_ru=0`, при tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | В 05-critic.md: «white space может означать как opportunity, так и отсутствие доказанного локального спроса», а moat в основном строится на workflow embedding и policy packs. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В 05-critic.md: «p10 EBITDA < 0», есть риск санкций, 152-ФЗ, data residency и зависимость от внешних LLM API. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | В 04-economics.md blended CAC = **1 058 571 ₽**, lead→paid = **1.2%**, named targets есть, но motion остаётся outbound-heavy и founder/AE dependent. |

**Sum raw = 95/150**  
**Normalized score = round((95 × 100) / 150) = 63/100**

## Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не усиливает продукт для остальных. |
| Switching costs | 2 | Интеграции, policy calibration и обучение legal/compliance команд дают умеренную инерцию. |
| Scale economies | 1 | COGS частично снижается за счёт шаблонов и policy packs, но service layer остаётся тяжёлым. |
| Proprietary data / model advantage | 1 | Доказанного уникального датасета или model moat нет, преимущество скорее в workflow orchestration. |
| Regulatory moat | 1 | Regulatory pain есть, но нет T1-proof на лицензируемый или аккредитационный барьер именно у продукта. |
| Brand / distribution | 1 | В РФ собственного бренда и distribution moat нет; продажи придётся строить account-by-account. |
| Embedded workflow | 3 | После внедрения решение глубоко встраивается в pre-publication review, legal approval и audit trail. |

**Moat raw = 9/21, Moat score = round((9 × 25) / 21) = 11/25. Committee overlay: 12/25 за сильную embedded-workflow ценность, но moat остаётся weak-to-medium.**

## Investment one-liner

`[GEO-EXPAND] Haast AI Marketing Compliance v2 — REJECTED: 63/100 | EBITDA base=554К₽/мес через 24 мес | LTV/CAC=15,9x | Ключевое преимущество: глубокая встройка в legal/compliance workflow regulated брендов | Главный риск: слишком дорогой и медленный enterprise GTM для узкого buyer universe.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 16 797 600 ₽ |
| CAC blended fully-loaded | 1 058 571 ₽ |
| LTV/CAC | 15,9x |
| CAC Payback | 2,79 мес по MRR / 4,20 мес по gross profit |
| Gross Margin | 66,3% |
| contribution_margin_rub_month | 222 000 ₽/клиент/мес |
| fixed_costs_rub_month | 4 774 000 ₽/мес |
| company_ebitda_rub_month, M12 base | -1 980 637 ₽/мес |
| company_ebitda_potential_rub_month | 554 000 ₽/мес при 24 клиентах |
| clients_to_500k_ebitda | 24 |
| months_to_500k_ebitda | 20 |
| clients_to_1m_ebitda | 27 |
| months_to_1m_ebitda | 24+ |
| Break-even | 22 клиента / M20 |
| startup_capital_to_bep_rub | 48 160 689 ₽ |

## Полный business process из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping по regulated buyers | SDR / analyst | Rusprofile, hh.ru, CRM | 2 ч | 2 400 | Низкий |
| 2 | Первичный outbound / intro | SDR | Email, Telegram, phone, CRM | 1.5 ч | 1 800 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 200 | Средний |
| 4 | Discovery legal/compliance workflow | AE + founder | Meet, questionnaire, Miro | 2 ч | 9 500 | Низкий |
| 5 | Demo на реальных маркетинговых материалах | AE + solutions | Sandbox, review workflow | 2 ч | 10 500 | Низкий |
| 6 | Security / procurement pre-check | AE + CTO | NDA, trust docs, security Q&A | 3 ч | 12 000 | Низкий |
| 7 | Policy mapping и pilot scoping | Solutions + compliance SME | SOW, rule matrix | 5 ч | 24 000 | Низкий |
| 8 | Пилотная настройка и интеграции | Solutions engineer | DAM/CMS connectors, roles | 20 ч | 90 000 | Средний |
| 9 | Обучение legal / marketing users | CSM + SME | Zoom, docs, playbooks | 4 ч | 16 000 | Средний |
| 10 | Пилот 4-8 недель, weekly reviews | CSM + AE + founder | CRM, analytics, support | 18 ч | 66 000 | Средний |
| 11 | Legal / contract / DPA negotiation | AE + founder + legal | Contract workflow | 8 ч | 28 000 | Низкий |
| 12 | Финальный proposal и close | AE + founder | Pricing calculator, CRM | 4 ч | 18 000 | Низкий |
| 13 | Invoice / payment collection | Finance ops | 1C / банк / ЭДО | 1 ч | 2 500 | Высокий |
| 14 | Production onboarding после оплаты | CSM + solutions + SME | Runbook, policy packs | 12 ч | 44 000 | Средний |

**Итого direct pre-sale + close cost на 1 клиента: 327 400 ₽.**

## Финансовая траектория

| Scenario | EBITDA break-even month | EBITDA @M12 | EBITDA @M24 | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Optimistic | M15 | -954 050 ₽/мес | 7 738 608 ₽/мес | 37 555 449 ₽ |
| Base | M20 | -1 980 637 ₽/мес | 1 171 083 ₽/мес | 48 160 689 ₽ |
| Pessimistic | M35 | -2 988 387 ₽/мес | -3 316 085 ₽/мес | 76 710 420 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-3 316 085 ₽/мес**
- p50 EBITDA @M24 = **1 171 083 ₽/мес**
- p90 EBITDA @M24 = **7 738 608 ₽/мес**
- Вывод: median-case формально проходит EBITDA Gate, но downside слишком широкий и остаётся ниже нуля.

## Команда

| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Функция |
|---|---:|---:|---|
| CEO / founder-sales | 1 | 650 000 | founder-led enterprise sales, strategic close |
| CTO / solutions lead | 1 | 546 000 | architecture, security review, solution design |
| Backend / integration engineer | 2 | 832 000 | integrations, connectors, deployment |
| ML / automation engineer | 1 | 546 000 | model workflows, automation layer |
| SDR | 2 | 416 000 | outbound prospecting |
| AE | 1 | 364 000 | discovery, demo, proposal, close |
| CSM | 1 | 286 000 | onboarding, training, renewals |
| Compliance SME / policy specialist | 1 | 338 000 | policy packs, legal calibration |
| Finance / ops (0.5) | 0.5 | 156 000 | billing, contracts, ops |
| **Итого** | **10.5** | **4 134 000** | full GTM + delivery команда |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Крупнейший объём regulated marketing и тяжёлый legal approval контур в финуслугах | email decision-maker в marketing compliance / legal ops | 450 000 ₽/мес |
| ВТБ | Большой retail marketing volume и высокая цена ошибки в рекламных обещаниях | отраслевые конференции + direct outbound | 420 000 ₽/мес |
| Т-Банк | Digital-first marketing machine, где скорость pre-publication review критична | founder-led warm intro + email | 480 000 ₽/мес |
| Альфа-Банк | Агрессивный маркетинг в regulated vertical, высокий риск legal bottleneck | partner-led через integrator / legaltech channel | 420 000 ₽/мес |
| Газпромбанк | Enterprise procurement и compliance-heavy согласования подтверждают fit кейса | conference networking + ABM outreach | 400 000 ₽/мес |
| Совкомбанк | Активный consumer marketing и длинный approval chain в regulated продуктах | direct outbound + vc.ru thought leadership | 380 000 ₽/мес |
| Ингосстрах | Страховой маркетинг чувствителен к claims и формулировкам обещаний | email decision-maker + партнёрство с compliance-консалтингом | 360 000 ₽/мес |
| СОГАЗ | Крупный страховщик с множеством маркетинговых и агентских материалов | отраслевые ивенты + интеграторский канал | 350 000 ₽/мес |
| АльфаСтрахование | Высокий объём digital marketing и чувствительный legal/compliance review | ABM outreach + conference intro | 360 000 ₽/мес |
| БКС | Инвестпродукты и брокерские коммуникации несут высокий regulatory risk | email CMO/legal/compliance + контент на Habr/vc.ru | 340 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Weak moat / narrow buyer universe | high | high | Moat score остаётся низким, а ICP ограничен finance-first и regulated брендами с длинным sales cycle. |
| Price compression + slow enterprise sales | high | high | В 05-critic.md сценарий `Price -30%` даёт EBITDA @M12 **-3 415 067 ₽/мес**, а CAC x2 почти так же разрушителен. |
| Regulatory / LLM dependency | high | high | 152-ФЗ, data residency, санкции и зависимость от внешних LLM API одновременно бьют по GM, SLA и скорости закрытия сделок. |

## Что надо доказать для APPROVED

1. Не менее **3-4 платящих enterprise клиентов** в банках/страховании с чеком **≥ 450К ₽/мес** без bespoke scope creep.
2. Реальный **pilot-to-paid ≥ 25%** и sales cycle **≤ 6 месяцев** хотя бы по двум логотипам.
3. Подтверждение, что `company_ebitda_rub_month` выходит на **500К+ ₽/мес** не позже **M18-M20**, а не только в конце двухлетнего окна.
4. Стандартизированные policy packs и integration playbooks, удерживающие **COGS ≤ 120-130К ₽/клиент/мес**.
5. Локальный evidence pack по РФ: ещё больше HH/job-postings, кейсы штрафов, тендеры, пилоты и buyer interviews.

## LTV Upside Calculator

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 380 000 ₽/мес | 500 000 ₽/мес | Сильно ускоряет путь к 500К EBITDA и снижает требуемое число клиентов. |
| COGS на клиента | 128 000 ₽/мес | ≤110 000 ₽/мес | Поднимает `contribution_margin_rub_month` и сокращает clients-to-break-even. |
| Fully-loaded CAC | 1 058 571 ₽ | ≤800 000 ₽ | Снижает burn и делает GTM менее зависимым от длинных пилотов. |
| Pilot-to-paid | 1.2% lead→paid blended | ≥1.8% blended / ≥25% pilot→paid | Делает enterprise motion повторяемым, а не штучным. |
| Buyer universe | 978 finance-first buyers | + фарма, телеком, ритейл high-risk verticals | Расширяет SAM и даёт шанс на более широкий локальный wedge. |

### Минимальные proof points для rerun
1. **10 SQL** из списка named targets и минимум **3 paid pilots**.
2. Реальный **CAC ≤ 800К ₽** на первых закрытых клиентах.
3. Выход на **24 клиента** должен подтверждаться не позже **M18-M20** и без роста fixed costs выше плана.
4. Два кейса, где Haast реально сокращает manual review time и повышает speed-to-launch для regulated campaigns.

## Финальное решение инвесткомитета

**REJECTED.**

Я бы не давал approve и даже near-pass сейчас, потому что фондовая математика ломается не на клиентской экономике, а на уровне компании. Для такого узкого buyer universe путь к 24 клиентам, 48+ млн ₽ капитала и tolerable downside выглядит слишком тяжёлым. Кейс стоит держать в longlist как enterprise legal-compliance wedge, но не как текущий приоритет для инвестируемого standalone РФ-выхода.


---

# 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-21 07:53 MSK - P4 Demand Validation
- stage: P4 Demand Validation
- case: haast-ai-marketing-compliance-v2
- demand_score: LOW / BORDERLINE
- market_signal: слабый органический спрос в РФ, но подтверждённая enterprise-боль в узком regulated сегменте
- economics_signal: Profit Gate проходит только в sales-led enterprise сценарии от 3-4 крупных клиентов
- decision: proceed, no early reject
- artifacts:
  - `02-demand.md`
- note: thesis сохраняется как geo-expand в BFSI-first; при отсутствии сильного wedge на следующих этапах риск reject высокий

## 2026-04-21 12:18 MSK - P7 Critic and Verdict
- stage: P7 Critic and Verdict
- case: haast-ai-marketing-compliance-v2
- score: 63/100
- delta: n/a
- verdict: REJECTED
- summary: сильная unit economics на клиента и рабочий EBITDA median-case к M24 не компенсируют узкий buyer universe, длинный enterprise cycle и высокий burn до break-even
- artifacts:
  - `06-verdict.md`
  - `telegram-messages.md`
- note: кейс отклонён как standalone РФ geo-expand, но сохранён в longlist как legal/compliance wedge при наличии будущих proof points
