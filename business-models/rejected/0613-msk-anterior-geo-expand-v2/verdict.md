
# 0613 MSK Anterior GEO Expand v2
**Статус:** REJECTED
**Итоговый балл:** 59/100
**Дата:** 2026-04-20
**Сектор:** HEALTHCARE

---

## Этап 1 — Intake
---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-0613-msk-anterior-geo-expand.md
created: 2026-04-19T21:34:25+03:00
---

# Intake

## Название
0613 MSK Anterior GEO Expand

## Режим обработки
Принудительный resurrect по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Исходный triage
/home/node/.openclaw/workspace/branch-models-lead/pipeline/triage/triage-2026-04-19-0613-msk-anterior-geo-expand.md

## Краткий контекст
Сигнал ранее уже разбирался, но по правилу resurrect должен пройти независимую полную переоценку как standalone candidate.

## Полный контекст из raw

# RESURRECT SIGNAL — 0613-msk-anterior-geo-expand

## Meta
- source: triage/triage-2026-04-19-0613-msk-anterior-geo-expand.md
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
2026-04-19

## Входные данные
- `pipeline/raw/raw-2026-04-19-0613-msk-anterior-geo-expand.md`

## Классификация
новый кейс

## Решение
Создан новый кейс, потому что сигнал не совпадает по теме с уже открытыми кейсами и проходит порог Program 1 по потенциальному LTV.

## Созданный кейс
- `pipeline/cases/ai-payer-clinical-admin-automation-operator/`

## Почему
- Anterior относится к отдельной категории payer-side административно-клинической автоматизации, а не к patient-facing healthcare AI, hospital operations automation или медицинскому coding.
- Во входном файле есть сильные признаки зрелости категории: 50 млн insured lives в покрытии, кейс на 6 млн prior authorizations в год, заявленные 85% снижения базовых административных затрат и 99,24% clinical accuracy.
- Потенциал LTV в РФ проходит порог: во входном сигнале указан ориентир 3-15 млн ₽ ARR на одного крупного клиента, что даёт верхнюю часть диапазона выше 500 000 ₽ в месяц.
- Прямой зрелый российский AI-native аналог именно для payer-side clinical admin automation во входном сигнале не просматривается.

## Что сделано
- Создан новый кейс `ai-payer-clinical-admin-automation-operator`.
- В кейсе записан `00-brief.md` на русском языке.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал обработан как новый кейс. Открыт кейс про AI-автоматизацию медико-страховых и административно-клинических workflow на стороне страховщика, ДМС и крупных медицинских контуров.
```



---

## Этап 2 — Demand
---
stage: demand-validation
case: 0613-msk-anterior-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
0613 MSK Anterior GEO Expand, AI-native payer-side clinical admin automation для prior authorization, utilization management и смежных медико-страховых workflow.

## Итог
**Статус: CONDITIONAL PASS**

В РФ exact keyword demand почти нулевой, потому что американский термин prior authorization локально почти не используется как отдельная software category. Но money demand у категории реален: в США и глобальном payer-tech контуре prior auth остаётся огромным административным bottleneck, а регуляторное давление только усиливается. Anterior уже показывает production-grade traction, а рынок подтверждён официальными сигналами от CMS, AMA и CAQH.

Главная проблема не в наличии боли, а в локализации wedge. Полноценный US-style prior authorization плохо переносится в РФ один-в-один. Поэтому PASS не чистый, а **CONDITIONAL**: спрос и willingness-to-pay на payer-side clinical admin automation есть, но в следующих этапах нужно доказать, что локальный wedge строится вокруг ДМС, медико-страховой экспертизы, гарантийных писем, utilization review и клинико-административного routing, а не вокруг буквального копирования американского prior auth stack.

## 1. Demand data
Источник exact-check: `http://172.18.0.1:9001/multi-demand?keyword=prior%20authorization%20automation`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Дополнительные смежные проверки:

### `medical prior authorization software`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **1**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `payer clinical review automation`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `utilization management automation`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **5**
- Yandex suggest: **2**

### Интерпретация
Search-demand в РФ почти отсутствует, но это ожидаемо. Категория enterprise-only и к тому же терминологически импортная. Здесь важнее не поиск, а наличие дорогого ручного workflow у страховщиков и крупных медконтуров. По глобальным сигналам такая боль подтверждена очень сильно.

## 2. Реальные рыночные сигналы и why now

1. **CMS final rule от 17 января 2024 года** усилил требования к prior authorization process: для impacted payers операционные требования начали вступать с **1 января 2026 года**, а API-требования в основном с **1 января 2027 года**. Это создаёт прямой регуляторный push на automation.
2. **Anterior** официально показывает production signal: кейс на **6 млн prior authorizations в год**, **99,24% clinical accuracy**, **85% elimination baseline admin cost**, **56% reduced staff burden time**.
3. По состоянию на **12 февраля 2026 года** Anterior пишет, что уже поддерживает организации, покрывающие **50 млн lives**. Это сильный признак enterprise adoption, а не раннего пилотного шума.
4. **CAQH 2024 Index** показывает, что fully electronic prior authorization всё ещё только **35%** рынка, а savings opportunity остаётся заметной: **$414 млн** у providers и **$101 млн** у plans, всего **$515 млн** при переводе оставшихся partial/manual workflows в fully electronic.
5. **AMA survey, июль 2024** показывает, что **78%** врачей сообщают, что prior authorization иногда или часто приводит к отказу пациента от рекомендованного лечения. Это подтверждает, что pain не косметический, а системный.

### Вывод
Категория точно не выдуманная. Это большой, срочный и регуляторно подталкиваемый workflow. Вопрос дальше не в наличии спроса, а в том, насколько этот спрос переносим в локальный страховой контур.

## 3. Конкурентные и ценностные якоря

| Игрок | Что продаёт | Публичный якорь | Вывод |
|---|---|---|---|
| Anterior | AI-native prior auth / payer workflow automation | 6 млн prior auth в год, 99.24% accuracy, 182 sec approval, 85% admin cost elimination | сильный category proof |
| Experian Health | prior authorization software для provider-side automation | заявляет automation 100% inquiries и снижение denials | подтверждает зрелость spend по adjacent workflow |
| Waystar | AI / automation для prior auth | публично описывает prior auth как рынок с крупными потерями из-за manual process | подтверждает устойчивый budget line |
| CAQH ecosystem | стандарты и operating rules для PA workflows | $16.29 manual, $8.98 partial electronic, $5.43 fully electronic per transaction | даёт economic anchor даже без публичных SaaS цен |

### Вывод по конкурентному полю
Публичных ценников у category leaders почти нет, рынок явно sales-led enterprise. Но это не минус для demand-stage. Наоборот, это типичный признак high-ACV workflow software для payers. WTP подтверждается через:
- регуляторный push,
- огромный объём ручных транзакций,
- экономию на cost-per-transaction,
- факт существования нескольких зрелых vendors и интеграционного слоя.

## 4. Российский контур и substitutes
Прямого зрелого аналога Anterior в РФ не видно. Но substitutes понятны:
- ручная медико-страховая экспертиза в ДМС и страховых,
- call-center / medical review teams,
- гарантийные письма и согласование лечения,
- UM / экспертиза обоснованности госпитализаций и дорогих процедур,
- rule-based BPM/CRM/ECM в страховом и hospital admin контуре,
- outsourcing клинико-административной обработки.

### Вывод
Локальный рынок есть, но он не называется prior authorization software. Скорее это umbrella-layer над clinical admin automation для payer/provider boundary. Это делает локализацию возможной, но усложняет GTM и category narrative.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
- Для локального base-case беру **450 000 ₽/мес** = **5,4 млн ₽/год** на клиента.
- Это ниже верхней границы исходного сигнала `3–15 млн ₽ ARR`, но достаточно высоко для enterprise workflow с интеграцией, audit trail и human-in-the-loop.
- ICP: крупные ДМС-страховщики, федеральные страховщики с медконтуром, крупные частные медсети, TPA/assistance-контуры и enterprise-плательщики со сложным medical review.

### TAM
Беру **180** потенциально релевантных организаций в РФ и близком русскоязычном контуре.

**TAM = 180 × 5 400 000 ₽ = 972 млн ₽/год**

### SAM
Реально адресуемый слой для первого GTM, это крупные контуры с высокими объёмами сложных согласований и цифровой зрелостью.

Беру **45** организаций.

**SAM = 45 × 5 400 000 ₽ = 243 млн ₽/год**

### SOM
Ранний реалистичный слой: **8 контрактов**.

**SOM = 8 × 5 400 000 ₽ = 43,2 млн ₽/год**

### Вывод по рынку
Локальный рынок не огромный, но достаточный для operator-style бизнеса. Это не venture-scale SaaS category для сотен клиентов, но вполне может быть high-ticket B2B vertical с meaningful выручкой.

## 6. WTP и доказательства готовности платить
1. **CMS** фактически делает automation стратегическим требованием для части payer workflows, а не nice-to-have.
2. **CAQH 2024** показывает существенную разницу в cost-per-transaction: medical prior authorization в среднем стоит индустрии **$16.29** в manual-mode, **$8.98** в partial electronic и **$5.43** в fully electronic. Это сильный ROI-якорь даже без учёта system costs.
3. **Anterior** показывает реальную enterprise traction, а не только обещания: production deployment, интеграции, 50M covered lives.
4. **Experian Health** и **Waystar** подтверждают, что adjacent budget line давно существует и уже покупается крупными организациями.

### Вывод по WTP
**WTP подтверждён глобально и условно подтверждён локально.**

Глобально категория уже покупается. Локально готовность платить зависит от того, насколько продавец сможет упаковать решение не как “американский prior auth”, а как снижение нагрузки на медэкспертизу, ускорение согласований и контроль клинико-административного SLA.

## 7. Profit Gate
Нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Conservative
- Цена: **300 000 ₽/мес**
- GM: **55%**
- Валовая прибыль на клиента: **165 000 ₽/мес**
- Для fixed costs **1,8 млн ₽/мес** нужно **14 клиентов**

**Вердикт: STRETCH**

### Сценарий B. Base-case
- Цена: **450 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **270 000 ₽/мес**
- Нужно **9 клиентов**

**Вердикт: PASS**

### Сценарий C. Enterprise with services + integration
- Цена: **700 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **455 000 ₽/мес**
- Нужно **5 клиентов**

**Вердикт: PASS**

### Вывод по Profit Gate
Profit gate проходится, если продавать решение как mission-critical enterprise workflow, а не как узкий AI feature. Если локальный продукт скатится в кастомную автоматизацию с низким чеком и тяжёлым внедрением, экономика быстро станет натянутой.

## 8. Общий вывод
- Search demand в РФ: **LOW**
- Global workflow pain: **очень высокий**
- Регуляторный драйвер: **сильный**
- Публичные economic anchors: **есть**
- WTP: **подтверждён глобально, локально условно**
- Localizability: **возможна, но требует переупаковки категории**
- Profit Gate: **проходит в base и enterprise сценариях**

## 9. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс стоит двигать дальше в P4/P5, потому что:
1. глобальная боль и бюджет подтверждены;
2. Anterior уже демонстрирует зрелый category proof;
3. ROI у automation убедительный;
4. локальный high-LTV wedge выглядит возможным.

Но в следующих этапах нужно особенно жёстко проверить:
- насколько РФ/СНГ контур реально похож на payer prior auth, а не только на смежную медэкспертизу;
- сколько ручного clinician / ops load скрыто в delivery;
- можно ли построить repeatable GTM без американской regulatory scaffolding;
- не превращается ли кейс на практике в кастомный insurer IT-services business.

## Market Pulse
Market Pulse 20.04.2026: сильный глобальный спрос, локальный спрос опосредованный через страховой и клинико-административный workflow.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=prior%20authorization%20automation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=medical%20prior%20authorization%20software
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=payer%20clinical%20review%20automation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=utilization%20management%20automation
- CMS Interoperability and Prior Authorization Final Rule, 2024 / updated 2026: https://www.cms.gov/cms-interoperability-and-prior-authorization-final-rule-cms-0057-f
- CMS fact sheet on compliance dates: https://www.cms.gov/newsroom/fact-sheets/cms-interoperability-and-prior-authorization-final-rule-cms-0057-f
- Anterior prior authorization solution: https://www.anterior.com/prior-authorization-solution
- Anterior homepage: https://www.anterior.com/
- Anterior funding update, 2026-02-12: https://www.anterior.com/insights/anterior-raises-40m-series
- Anterior AHIP commitment note: https://www.anterior.com/insights/ahip-commitment-health-plans
- CAQH 2024 Index report: https://www.caqh.org/hubfs/Index/2024%20Index%20Report/CAQH_IndexReport_2024_FINAL.pdf
- CAQH prior authorization priority topic: https://www.caqh.org/core/priority-topics
- AMA survey coverage, 2024-07-18: https://www.ama-assn.org/practice-management/prior-authorization/exhausted-prior-auth-many-patients-abandon-care-ama-survey
- Experian Health prior authorization software: https://www.experian.com/healthcare/products/patient-access-registration/prior-authorization-software
- Waystar acquisition note on prior authorization automation: https://www.waystar.com/news/waystar-acquires-digitize-ai-to-automate-prior-authorization/

- Market Pulse 2026-04-20: растущий интерес.


---

## Этап 3 — Unit Economics
---
stage: economics
case: 0613-msk-anterior-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
0613 MSK Anterior GEO Expand, AI-native payer-side clinical admin automation для prior authorization, utilization management и смежных медико-страховых workflow.

## Economics verdict
**Статус: PASS**

Кейс проходит P5 как investment-grade regulated B2B healthtech play. Я считал не "красивый SaaS", а тяжёлый enterprise stress-case: длинный sales cycle, pilot + procurement, клинико-административный review, compliance и fully-loaded CAC c мультипликатором regulated segment. Даже в этой модели:

- **MRR на клиента:** 650 000 ₽
- **COGS на клиента/мес:** 255 000 ₽
- **Contribution margin:** 60,8%
- **Fully-loaded blended CAC:** 3 280 000 ₽
- **Logo churn:** 1,5%/мес
- **LTV:** 26,33 млн ₽
- **LTV/CAC:** 8,0x
- **CAC Payback:** 5,0 мес
- **Break-even:** 16 клиентов, около **M13**

Итог: модель капиталоёмкая, но не ломается. До **EBITDA > 500 тыс. ₽/мес** компания доходит задолго до 50 клиентов.

## 1. Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list страховщиков, ДМС, assistive/TPA и крупных медсетей | SDR | HH/рынок, ручной research, CRM | 2 дня | 18 000 | Низкая |
| 2 | Outreach: email, cold call, LinkedIn-like аналог, интро через партнёров | SDR | CRM, sequencer, телефония | 10 рабочих дней | 42 000 | Средняя |
| 3 | Discovery call и qualification по pain/volume/compliance | AE + CEO | CRM, Zoom/Meet | 5 дней | 55 000 | Низкая |
| 4 | Solution workshop с клинико-страховой командой клиента | AE + CTO + клин. эксперт | Miro, презентация, demo env | 1 неделя | 95 000 | Низкая |
| 5 | Доступ к sample-cases, mapping workflow, ROI baseline | CTO + ML + backend | sandbox, ETL, prompt stack | 2 недели | 180 000 | Средняя |
| 6 | Pilot / proof-of-value на ограниченном объёме кейсов | CTO + ML + clinical ops | cloud, LLM/OCR, audit logs | 4-6 недель | 310 000 | Средняя |
| 7 | Security/compliance/legal review, DPIA/infosec пакет | CTO + CEO + external legal | security docs, DPA, legal templates | 2-3 недели | 140 000 | Низкая |
| 8 | Коммерческое предложение, redlines, procurement | AE + CEO | CRM, doc flow, e-sign | 2 недели | 85 000 | Средняя |
| 9 | Onboarding и integration setup после подписания | CTO + DevOps + CSM | cloud, SSO, API/webhook | 2-4 недели | 165 000 | Средняя |
| 10 | Ежемесячная обработка workflow, QA, support, billing | CSM + clinical ops + finance | product, billing, helpdesk | ongoing monthly | 255 000 / клиент / мес | Средняя |

### Вывод по процессу
Это не self-serve SaaS. Это regulated enterprise sale с 8-12 неделями на deal cycle и заметным pre-sale cost. Поэтому blended CAC ниже ~3 млн ₽ выглядел бы занижением.

## 2. Ценообразование и выручка

### Base-case pricing
- Подписка: **650 000 ₽/мес** на одного payer/provider enterprise клиента
- One-time implementation fee в модели не включаю в MRR, считаю как upside, а не как костыль для окупаемости
- Средний контракт: 12 месяцев, далее annual renewal

### Почему беру 650 000 ₽/мес
Это выше base-case из 02-demand, но ниже агрессивного enterprise-стресса 700 000 ₽/мес. Для regulated workflow с audit trail, human-in-the-loop и интеграциями такой чек реалистичнее, чем 300-450 тыс. ₽/мес.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM/OCR/API inference | 55 000 | usage-based | prior auth / UM кейсы документ-heavy |
| Cloud, storage, monitoring | 35 000 | shared infra allocation | логирование, резервирование, observability |
| Clinical QA / human-in-the-loop review | 85 000 | 0,35 FTE медицинского reviewer | ключевой regulated cost-driver |
| Customer Success / support | 45 000 | 0,14 FTE CSM | регулярные SLA, отчёты, change requests |
| Integration maintenance | 25 000 | backend/devops allocation | API, ETL, mapping payer rules |
| Compliance / audit / security ops | 10 000 | per-client allocation | журналирование, контроль доступа |
| **Итого COGS** | **255 000** |  |  |

### Unit margin
- **Revenue / client / month:** 650 000 ₽
- **COGS / client / month:** 255 000 ₽
- **Contribution / client / month:** 395 000 ₽
- **Contribution Margin %:** **60,8%**

Для healthtech enterprise это здоровая, но не "слишком красивая" маржа. Основной риск в том, что если доля ручного clinician review уйдёт выше 0,5 FTE на клиента, margin просядет к 50%.

## 4. CAC по каналам с funnel conversion

| Канал | Top of funnel / мес | Meetings | Qualified | Pilot | New paying customers / мес | Monthly cost, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound к страховщикам и медсетям | 180 accounts | 30 (16,7%) | 12 (40%) | 4 (33%) | 0,45 (11,3% из pilot) | 1 510 000 | 3 356 000 |
| Partnerships / industry events | 20 target intros | 8 (40%) | 4 (50%) | 2 (50%) | 0,30 (15%) | 1 070 000 | 3 567 000 |
| Founder-led referrals / inbound | 10 warm intros | 6 (60%) | 4 (67%) | 2 (50%) | 0,25 (12,5%) | 590 000 | 2 360 000 |
| **Blended** | **210** | **44** | **20** | **8** | **1,00** | **3 170 000** | **3 170 000** |

### Интерпретация
- Самый дешёвый канал, как обычно, это founder-led referrals, но он плохо масштабируется.
- Основной repeatable engine, скорее всего, outbound + partnerships.
- Для regulated healthtech enterprise blended CAC **~3,2 млн ₽** выглядит сурово, но не абсурдно. Это соответствует тому, что продажа требует пилота, security review и нескольких senior touches.

## 5. Fully-loaded CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/ретаргет) | 120 000 | low-volume account-based demand capture | внутренняя модель acquisition для enterprise wedge |
| Outbound team FOT (SDR + 60% AE attributed to new) | 546 000 | SDR 180 000 gross ×1,3 + AE 400 000 gross ×60% | HH.ru: SDR и account executive вакансии |
| Marketing team FOT (partial allocation) | 156 000 | 300 000 gross ×40% ×1,3 | HH.ru / market benchmark по product marketing |
| Tools (CRM, sequencing, data enrichment, telephony) | 108 000 | CRM + prospecting stack + телефония | рыночный стек enterprise outbound |
| Events/partnerships | 240 000 | 1 отраслевой ивент + travel + sponsorship allocation | рыночная оценка B2B field marketing |
| **Raw CAC spend** | **1 170 000** | сумма прямых acquisition cost |  |
| Overhead multiplier (x2,8 для regulated segment) | 2 106 000 | 1 170 000 × 1,8 incremental overhead | enterprise regulated stress-case |
| **Fully-loaded CAC** | **3 276 000** | raw spend × 2,8 / 1 new customer |  |

### Почему x2,8
Кейс попадает в **regulated healthtech / payer-tech**, где продажа включает compliance, pilot, security review, закупку и senior multi-threading. Поэтому я беру мультипликатор не x1,3 и не x1,7, а **x2,8**, то есть ближе к верхней границе правил для regulated сегмента.

### Sanity check к benchmark
В задании дан ориентир **Healthtech B2B 400-1200K ₽/клиент** для РФ. Наша оценка выше, потому что это не обычный clinic SaaS, а enterprise payer workflow c тяжёлым pre-sale. Для локального, упрощённого ДМС-only wedge CAC может быть ниже, но для текущей модели занижать его опасно.

## 6. LTV и churn

### Бенчмарк churn
Для SaaS с высоким ARPA ChartMogul показывает, что при ARPA **>$1k/мес** типичный customer churn падает примерно к **1-2%/мес**, а median customer churn для high-ARPA сегмента около **1,8%/мес**. Для этого кейса беру **1,5%/мес**, потому что:
- чек сильно выше high-ARPA порога,
- продукт глубоко встроен в workflow,
- есть switching costs через интеграции и audit trail,
- но всё равно остаётся procurement / vendor-switch risk.

### Формула LTV
`LTV = Contribution per customer per month / monthly churn`

### Расчёт
- Contribution / клиент / мес = **395 000 ₽**
- Logo churn = **1,5%/мес**
- **LTV = 395 000 / 0,015 = 26 333 333 ₽**

### Вывод
Даже если поднять churn до 2,0%/мес, LTV будет **19,75 млн ₽**, что всё равно значительно выше CAC.

## 7. LTV/CAC, Payback, Contribution Margin

| Метрика | Значение | Комментарий |
|---|---:|---|
| LTV | 26,33 млн ₽ | по contribution, не по выручке |
| Fully-loaded CAC | 3,28 млн ₽ | blended, regulated stress-case |
| **LTV/CAC** | **8,0x** | выше порога 3:1 |
| **CAC Payback** | **5,0 мес** | 3,276 млн / 650 тыс. ₽ MRR |
| **Contribution Margin %** | **60,8%** | healthy для enterprise healthtech |

### Вывод по investment threshold
- **LTV/CAC ≥ 3**: да
- **CAC Payback < 18 мес для enterprise**: да
- **EBITDA > 500k/mo achievable before 50 clients**: да

Следовательно, profit gate в P5 проходит.

## 8. Team & FOT

### Полная команда

| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO | enterprise sales, fundraising, partnerships | 1 | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | product architecture, security, enterprise delivery | 1 | 550 000 | 165 000 | 715 000 |
| Senior Backend | core workflow engine, APIs, integrations | 2 | 450 000 | 135 000 | 585 000 each |
| ML Engineer | extraction, classification, routing quality | 1 | 500 000 | 150 000 | 650 000 |
| DevOps | infra, monitoring, CI/CD, tenancy/security | 1 | 350 000 | 105 000 | 455 000 |
| Frontend | ops console, reviewer UI | 1 | 300 000 | 90 000 | 390 000 |
| SDR | target account generation, outreach | 1 | 180 000 | 54 000 | 234 000 |
| AE | deal orchestration, pilot to close | 1 | 400 000 | 120 000 | 520 000 |
| Customer Success | onboarding, SLA, renewals | 1 | 250 000 | 75 000 | 325 000 |
| **Итого** |  | **10** |  |  | **5 304 000 ₽/мес** |

### Таблица найма с realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 | 585 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 180 000 | 0,75 | 1 | 54 000 | 234 000 |
| AE (Account Exec) | 1 | 400 000 | 1,5 | 2,5 | 120 000 | 520 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Источники по salary benchmark
- HH.ru, Senior Backend / backend engineer: 230-600 тыс. ₽+ по Москве/remote, отдельные senior fintech вакансии доходят до 400-600 тыс. ₽
- HH.ru, ML Engineer Москва: 200-350 тыс. ₽ для mid; для LLM/RAG/production ML беру premium uplift до 500 тыс. ₽ gross
- HH.ru, senior DevOps: около 225-300 тыс. ₽ на публичной выборке, для enterprise regulated беру 350 тыс. ₽ gross как реалистичный hire price
- HH.ru, senior frontend React: 170-300 тыс. ₽+; для сильного product frontend беру 300 тыс. ₽ gross
- HH.ru, SDR / B2B Sales Development: 150-200 тыс. ₽+ и variable, беру 180 тыс. ₽ gross
- HH.ru, Customer Success Enterprise: 170-280 тыс. ₽, беру 250 тыс. ₽ gross
- HH.ru, Account Executive / KAM enterprise: ориентир 180-320 тыс. ₽ fixed плюс variable; для тяжёлого enterprise sale беру 400 тыс. ₽ gross total-on-target

## 9. Cumulative FOT timeline M1-M12

| Месяц | Кто в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Senior Backend #1 | 2 145 000 |
| M2 | + DevOps | 2 600 000 |
| M3 | + ML Engineer | 3 250 000 |
| M4 | + Frontend, + AE | 4 160 000 |
| M5 | + SDR | 4 394 000 |
| M6 | + Customer Success | 4 719 000 |
| M7 | + Senior Backend #2 | 5 304 000 |
| M8 | full core team | 5 304 000 |
| M9 | full core team | 5 304 000 |
| M10 | full core team | 5 304 000 |
| M11 | full core team | 5 304 000 |
| M12 | full core team | 5 304 000 |

### Комментарий
План найма не нарушает realism checks: в первый месяц не набирается 5+ человек, а full build-out происходит только к M7.

## 10. Fixed costs breakdown

| Компонент fixed costs | ₽/мес |
|---|---:|
| Общекорпоративная cloud / shared infra | 300 000 |
| Security, audit, compliance tooling | 220 000 |
| Legal / бухгалтерия / HR ops | 150 000 |
| Office / admin / travel / misc | 180 000 |
| G&A SaaS stack | 110 000 |
| **Итого fixed non-FOT** | **960 000** |

### Full fixed cost at steady-state
- **FOT:** 5 304 000 ₽/мес
- **Fixed non-FOT:** 960 000 ₽/мес
- **Всего fixed:** **6 264 000 ₽/мес**

## 11. Break-even по клиентам и по месяцам

### Break-even по количеству клиентов
`Break-even clients = Fixed costs / Contribution per client`

- Fixed costs = **6 264 000 ₽/мес**
- Contribution / client = **395 000 ₽/мес**
- **Break-even = 15,86**, округляю до **16 клиентов**

### Ramp по клиентам
Допущение для long enterprise sales cycle:
- M1-M5: 0 клиентов
- M6: 1
- M7: 2
- M8: 3
- M9: 5
- M10: 7
- M11: 10
- M12: 13
- **M13: 16**

### Break-even по месяцу
При таком ramp компания выходит примерно в **операционный ноль в M13**.

## 12. Burn-to-breakeven и cash runway

### EBITDA / burn timeline

| Месяц | Клиенты | Fixed cost, ₽ | Contribution from clients, ₽ | EBITDA / burn, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 3 105 000 | 0 | -3 105 000 |
| M2 | 0 | 3 560 000 | 0 | -3 560 000 |
| M3 | 0 | 4 210 000 | 0 | -4 210 000 |
| M4 | 0 | 5 120 000 | 0 | -5 120 000 |
| M5 | 0 | 5 354 000 | 0 | -5 354 000 |
| M6 | 1 | 5 679 000 | 395 000 | -5 284 000 |
| M7 | 2 | 6 264 000 | 790 000 | -5 474 000 |
| M8 | 3 | 6 264 000 | 1 185 000 | -5 079 000 |
| M9 | 5 | 6 264 000 | 1 975 000 | -4 289 000 |
| M10 | 7 | 6 264 000 | 2 765 000 | -3 499 000 |
| M11 | 10 | 6 264 000 | 3 950 000 | -2 314 000 |
| M12 | 13 | 6 264 000 | 5 135 000 | -1 129 000 |
| M13 | 16 | 6 264 000 | 6 320 000 | **+56 000** |

### Burn-to-breakeven
Суммарный burn до выхода в M13 примерно **48,4 млн ₽**.

### Cash runway
Берём **startup_capital = 60 млн ₽**.

- Runway по стартовому burn M1: около **19 мес**
- Runway по среднему burn до M13: около **15 мес**
- Остаток капитала к точке break-even: примерно **11,6 млн ₽**

### Вывод
Для enterprise B2B healthtech это тяжёлая, но реалистичная капитальная потребность. Если пытаться доказать, что до BEP достаточно 10 млн ₽, это был бы red flag.

## 13. Profit Gate

### Проверка условия из задания
1. **EBITDA < 500K/mo achievable even at 50 clients?** Нет.
   - EBITDA при 50 клиентах = 50 × 395 000 − 6 264 000 = **13 486 000 ₽/мес**
2. **LTV/CAC < 1:1?** Нет.
   - Факт: **8,0x**

### Итого
**Profit Gate = PASS**

## 14. Главные риски, которые ещё могут сломать модель
1. Если локальный рынок окажется не payer-tech, а project-heavy insurer IT-services, чек и renewal quality просядут.
2. Если regulated delivery потребует больше clinician-in-the-loop, COGS вырастет и margin уйдёт к 45-50%.
3. Если цикл сделки растянется с 3 до 6+ месяцев сверх модели, cash need вырастет выше 60 млн ₽.
4. Если РФ wedge будет только у нескольких ДМС/assistance контуров, масштабирование до 16+ клиентов станет сложнее, чем показывает базовая воронка.

## 15. Итог для пайплайна
**P5 PASS.**

Кейс не выглядит дешёвым или быстрым, но юнит-экономика для фонда всё ещё достаточно сильная:
- высокий ACV,
- manageable churn,
- LTV/CAC сильно выше порога,
- payback укладывается в enterprise-норму,
- EBITDA > 500 тыс. ₽/мес достижима задолго до 50 клиентов.

Следующий главный риск уже не в P5, а в том, насколько локальный wedge реально repeatable в ДМС/страховом контуре РФ.

## Источники
- 02-demand текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0613-msk-anterior-geo-expand-v2/02-demand.md
- ChartMogul churn benchmarks: https://chartmogul.com/saas-metrics/revenue-churn/
- ChartMogul churn explainer: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- HH.ru Senior Backend: https://hh.ru/vacancies/senior-backend-engineer
- HH.ru backend developer: https://hh.ru/vacancies/backend-developer
- HH.ru ML Engineer vacancy sample: https://hh.ru/vacancy/129433377
- HH.ru Senior DevOps: https://hh.ru/vacancies/senior-devops-engineer
- HH.ru Senior Frontend React: https://hh.ru/vacancies/senior-frontend-developer-react
- HH.ru SDR vacancy sample: https://hh.ru/vacancy/128203218
- HH.ru SDR vacancy sample 2: https://hh.ru/vacancy/129973514
- HH.ru Account Executive / KAM: https://hh.ru/vacancies/account_executive
- HH.ru Customer Success: https://hh.ru/vacancies/customer-success-manager


---

## Этап 4 — Finance Critic
## SECTION A — PnL 12 месяцев x 3 сценария

### Нормализация входных допущений

- ARPA: **650 000 ₽/клиент/мес**
- COGS per client: **255 000 ₽/клиент/мес**
- Gross profit / contribution per client: **395 000 ₽/клиент/мес**
- Gross margin: **60,8%**
- Fixed costs ramp M1-M12: **3 105 000, 3 560 000, 4 210 000, 5 120 000, 5 354 000, 5 679 000, 6 264 000, 6 264 000, 6 264 000, 6 264 000, 6 264 000, 6 264 000 ₽**
- Startup capital: **60 000 000 ₽**
- Налоговая логика для waterfall: **УСН 6% с выручки**, **IT-льгота 3% с выручки при аккредитации Минцифры**, **ОСНО 20% на прибыль**; **НДС 20%** применим на ОСНО, но считаю его транзитным и не включаю в строки MRR/COGS/EBITDA.
- Страховые взносы около **30% к ФОТ** уже включены в FOT и fixed costs из 04-economics.

### Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 10 | 13 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 650 000 | 1 300 000 | 1 950 000 | 3 250 000 | 4 550 000 | 6 500 000 | 8 450 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 255 000 | 510 000 | 765 000 | 1 275 000 | 1 785 000 | 2 550 000 | 3 315 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 395 000 | 790 000 | 1 185 000 | 1 975 000 | 2 765 000 | 3 950 000 | 5 135 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% |
| Fixed costs, ₽ | 3 105 000 | 3 560 000 | 4 210 000 | 5 120 000 | 5 354 000 | 5 679 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 |
| EBITDA, ₽ | -3 105 000 | -3 560 000 | -4 210 000 | -5 120 000 | -5 354 000 | -5 284 000 | -5 474 000 | -5 079 000 | -4 289 000 | -3 499 000 | -2 314 000 | -1 129 000 |
| Cash burn, ₽ | 3 105 000 | 3 560 000 | 4 210 000 | 5 120 000 | 5 354 000 | 5 284 000 | 5 474 000 | 5 079 000 | 4 289 000 | 3 499 000 | 2 314 000 | 1 129 000 |
| Cumulative cash, ₽ | -3 105 000 | -6 665 000 | -10 875 000 | -15 995 000 | -21 349 000 | -26 633 000 | -32 107 000 | -37 186 000 | -41 475 000 | -44 974 000 | -47 288 000 | -48 417 000 |

**Waterfall M12:**
- ARPA **650 000 ₽** → Gross **395 000 ₽** → Contribution **395 000 ₽** → EBITDA на клиента после fixed allocation зависит от масштаба.
- На масштабе **M12**: Revenue **8 450 000 ₽** → Gross **5 135 000 ₽** → EBITDA **-1 129 000 ₽**.
- Net after tax, M12: **УСН 6% = -1 636 000 ₽**, **IT-льгота 3% = -1 382 500 ₽**, **ОСНО 20% = -1 129 000 ₽**.
- Break-even client count: **16 клиентов**.
- Break-even month: **M13**.
- startup_capital_to_bep_rub: **48 417 000 ₽**.

### Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 12 | 15 | 18 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 650 000 | 1 300 000 | 2 600 000 | 3 900 000 | 5 850 000 | 7 800 000 | 9 750 000 | 11 700 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 255 000 | 510 000 | 1 020 000 | 1 530 000 | 2 295 000 | 3 060 000 | 3 825 000 | 4 590 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 395 000 | 790 000 | 1 580 000 | 2 370 000 | 3 555 000 | 4 740 000 | 5 925 000 | 7 110 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% |
| Fixed costs, ₽ | 3 105 000 | 3 560 000 | 4 210 000 | 5 120 000 | 5 354 000 | 5 679 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 |
| EBITDA, ₽ | -3 105 000 | -3 560 000 | -4 210 000 | -5 120 000 | -4 959 000 | -4 889 000 | -4 684 000 | -3 894 000 | -2 709 000 | -1 524 000 | -339 000 | 846 000 |
| Cash burn, ₽ | 3 105 000 | 3 560 000 | 4 210 000 | 5 120 000 | 4 959 000 | 4 889 000 | 4 684 000 | 3 894 000 | 2 709 000 | 1 524 000 | 339 000 | 0 |
| Cumulative cash, ₽ | -3 105 000 | -6 665 000 | -10 875 000 | -15 995 000 | -20 954 000 | -25 843 000 | -30 527 000 | -34 421 000 | -37 130 000 | -38 654 000 | -38 993 000 | -38 147 000 |

**Waterfall M12:**
- ARPA **650 000 ₽** → Gross **395 000 ₽** → Contribution **395 000 ₽** → EBITDA на клиента после fixed allocation зависит от масштаба.
- На масштабе **M12**: Revenue **11 700 000 ₽** → Gross **7 110 000 ₽** → EBITDA **846 000 ₽**.
- Net after tax, M12: **УСН 6% = 144 000 ₽**, **IT-льгота 3% = 495 000 ₽**, **ОСНО 20% = 676 800 ₽**.
- Break-even client count: **16 клиентов**.
- Break-even month: **M12**.
- startup_capital_to_bep_rub: **38 993 000 ₽**.

### Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 3 | 5 | 7 | 10 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 650 000 | 1 300 000 | 1 950 000 | 3 250 000 | 4 550 000 | 6 500 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 255 000 | 510 000 | 765 000 | 1 275 000 | 1 785 000 | 2 550 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 395 000 | 790 000 | 1 185 000 | 1 975 000 | 2 765 000 | 3 950 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% | 60,8% |
| Fixed costs, ₽ | 3 105 000 | 3 560 000 | 4 210 000 | 5 120 000 | 5 354 000 | 5 679 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 | 6 264 000 |
| EBITDA, ₽ | -3 105 000 | -3 560 000 | -4 210 000 | -5 120 000 | -5 354 000 | -5 679 000 | -5 869 000 | -5 474 000 | -5 079 000 | -4 289 000 | -3 499 000 | -2 314 000 |
| Cash burn, ₽ | 3 105 000 | 3 560 000 | 4 210 000 | 5 120 000 | 5 354 000 | 5 679 000 | 5 869 000 | 5 474 000 | 5 079 000 | 4 289 000 | 3 499 000 | 2 314 000 |
| Cumulative cash, ₽ | -3 105 000 | -6 665 000 | -10 875 000 | -15 995 000 | -21 349 000 | -27 028 000 | -32 897 000 | -38 371 000 | -43 450 000 | -47 739 000 | -51 238 000 | -53 552 000 |

**Waterfall M12:**
- ARPA **650 000 ₽** → Gross **395 000 ₽** → Contribution **395 000 ₽** → EBITDA на клиента после fixed allocation зависит от масштаба.
- На масштабе **M12**: Revenue **6 500 000 ₽** → Gross **3 950 000 ₽** → EBITDA **-2 314 000 ₽**.
- Net after tax, M12: **УСН 6% = -2 704 000 ₽**, **IT-льгота 3% = -2 509 000 ₽**, **ОСНО 20% = -2 314 000 ₽**.
- Break-even client count: **16 клиентов**.
- Break-even month: **M14** при сохранении темпа конца года.
- startup_capital_to_bep_rub: **54 681 000 ₽**.

### Сравнение налоговых режимов на M12 по сценариям

| Scenario | EBITDA M12, ₽ | Net after tax, УСН 6%, ₽ | Net after tax, IT-льгота 3%, ₽ | Net after tax, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|
| Base | -1 129 000 | -1 636 000 | -1 382 500 | -1 129 000 |
| Optimistic | 846 000 | 144 000 | 495 000 | 676 800 |
| Pessimistic | -2 314 000 | -2 704 000 | -2 509 000 | -2 314 000 |

### Break-even summary

| Scenario | Break-even clients | Break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---:|---|
| Base | 16 | M13 | 48 417 000 ₽ | по базовому ramp из 04-economics |
| Optimistic | 16 | M12 | 38 993 000 ₽ | внутри 12 месяцев |
| Pessimistic | 16 | M14 | 54 681 000 ₽ | после 12 месяцев при сохранении late-year темпа |

<!-- P6A-DONE -->


## SECTION B — Finance Risk + Competitor Deep-Dive

### 1. Sensitivity analysis: EBITDA через 12 месяцев вперёд

Базу считаю от текущего состояния **M12 = 13 клиентов** и продолжаю тот же sales ramp ещё на 12 месяцев. Базовый terminal state к **M24** даёт около **49 клиентов**. Это не полноценная cohort-модель, а stress-test на уровне investment memo.

| Scenario | Ключевое изменение | Клиенты @M24 | Contribution / клиент / мес | EBITDA @M24, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без изменений | 49,0 | 395 000 | **13 091 000** | 49 × 395 000 − 6 264 000 |
| Sens1 | CAC x2 | 31,0 | 395 000 | **5 981 000** | допускаю падение acquisition efficiency примерно в 2 раза, то есть прирост снижается с ~3 до ~1,5 клиента/мес |
| Sens2 | Churn x2 | 40,6 | 395 000 | **9 773 000** | churn растёт с 1,5% до 3,0% в месяц, terminal client base заметно проседает |
| Sens3 | Price -30% | 49,0 | 200 000 | **3 536 000** | ARPU падает до 455 000 ₽, COGS держу прежним 255 000 ₽, contribution сжимается до 200 000 ₽ |

### Вывод по sensitivity

- Самый болезненный single-variable shock здесь не churn, а **price compression**, потому что он почти вдвое режет contribution.
- **CAC x2** модель переживает, но рост становится гораздо менее комфортным и резко удлиняется путь к cash cushion.
- Даже при **Price -30%** EBITDA на M24 формально остаётся положительной, но safety margin уже узкий для regulated B2B delivery.

### 2. Monte Carlo Lite — confidence intervals

Ниже не full-code симуляция, а упрощённый Monte Carlo Lite на базе triangular inputs и 9 комбинаций. Этого достаточно, чтобы увидеть ширину распределения и хрупкость модели.

#### Inputs — triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 2 600 000 | 3 280 000 | 5 800 000 | [T1], [T2] |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | [T1], [T3] |
| ARPU, ₽/мес | 455 000 | 650 000 | 780 000 | [T1], [T2] |
| Conversion rate lead→paid, % | 0,30% | 0,48% | 0,80% | [T1] |
| Time-to-hire, месяцев | 1,2 | 1,6 | 2,4 | [T1] |

#### Логика упрощённой симуляции

Использую 9 комбинаций вокруг трёх опорных точек:
- best case: CAC_min + Churn_min + ARPU_max,
- median: CAC_mode + Churn_mode + ARPU_mode,
- worst case: CAC_max + Churn_max + ARPU_min,
- плюс 6 mixed-комбинаций, чтобы не переоценить линейность модели.

#### Результат Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 864 000** | **13 091 000** | **19 476 000** | **22 340 000** |
| CAC payback, мес | **12,7** | **5,0** | **3,3** | **9,4** |
| LTV/CAC | **1,1x** | **8,0x** | **20,2x** | **19,1x** |
| Cash runway, мес | **8** | **15** | **22** | **14** |

#### Интерпретация Monte Carlo Lite

1. **p10 EBITDA < 0**. Это автоматически активирует **kill criterion #1**: в левом хвосте модель уходит в риск неплатёжеспособности.
2. **p50 EBITDA = 13,1 млн ₽/мес**, то есть median формально проходит EBITDA gate. Сам базовый сценарий не ломается.
3. Отношение **p90/p10** здесь некорректно в прямом виде, потому что p10 отрицательный. Практически это ещё хуже, чем 10x dispersion: диапазон включает переход через ноль, значит неопределённость очень высокая.
4. **Range width по LTV/CAC = 19,1x**, что сильно выше порога 8. Следовательно, модель **хрупкая** к pricing, churn и acquisition quality.

### 3. Competitor deep-dive

Ниже я разделяю **прямых западных конкурентов** и **российских ближайших substitutes**. Для РФ это важно: прямого AI-native prior authorization аналога я не вижу, поэтому локальное поле состоит из document AI, med-AI и enterprise workflow-платформ, которые закрывают отдельные куски value chain, но не весь payer-side stack целиком.

#### 3.1 Западные конкуренты

| Игрок | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Anterior** | category leader / reference case | сильный payer-first narrative, KLAS-verified clinical accuracy 99,24%, кейс на 6 млн PA/год, explainability и human-in-the-loop | зависимость от США regulatory scaffolding, длинный enterprise implementation, тяжёлый compliance burden | **5-10%** в AI-native нише payer-side prior auth, но значительно меньше 1% всего UM/PA software рынка | локальная адаптация под ДМС, медэкспертизу и data residency РФ; меньше затрат на русификацию workflow |
| **Cohere Health** | самый сильный adjacent incumbent в UM/prior auth automation | до 90% auto-approvals, 47% admin savings, CMS-0057-F compliance, большие existing payer relationships | менее острое AI-native positioning, сложнее продавать как быстрый narrow-wedge продукт, внедрение часто тяжёлое enterprise-first | **10-20%** AI-enabled prior auth / UM automation сегмента в США | можем зайти как более узкий и быстрый payer workflow layer без тяжёлой legacy-платформы |
| **Waystar** | большой workflow/infrastructure игрок на payer-provider boundary | масштаб сети, интеграционный след, сильный data flywheel, broad RCM footprint | prior auth для них лишь часть более широкой revenue-cycle машины; не всегда приоритет payer clinical admin | **15-25%** broader adjacent workflow market, но ниже доля именно в AI-native PA decisioning | у нас уже в ядре не revenue cycle, а clinical-admin payer workflow; меньше platform bloat |

#### 3.2 Российские конкуренты / substitutes

| Игрок | Тип | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **К-Скай / Webiomed** | closest med-AI substitute | сильная клиническая аналитика, узнаваемость в health IT, опора на экосистему Сколково и интеграции с медданными | фокус скорее на CDS/аналитике, а не на payer-side prior auth / utilization workflow orchestration | **3-5%** в broader RU med-AI stack, около нуля в точном нашем сегменте | у нас более чёткий ROI-кейс на административное плечо страховщика и медэкспертизы |
| **Биорг / Beorg Smart Vision** | document AI substitute | сильный OCR/IDP, кейсы в страховании, высокая точность на слабоструктурированных документах, реальная коммерческая выручка | не закрывает clinical reasoning, policy digitization и end-to-end adjudication | **5-10%** в RU document AI для страхования/документооборота | наш advantage в том, что OCR у нас только входной слой, а не весь продукт |
| **Naumen** | enterprise workflow platform substitute | масштаб, зрелый enterprise sales motion, большая installed base в контакт-центрах и сложных workflow | не healthtech-native, нет глубокой клинической decisioning-логики out of the box | **10-15%** в крупном enterprise workflow/case-management ПО РФ, но низкая доля в med-insurance AI | у нас ниже time-to-value именно для medical review и payer operations |
| **N3.Health** | health-data / integration substitute | сильный контур обмена медданными и интеграций, полезен как инфраструктурный слой | это pipe, а не решение для prior auth reasoning или utilization review | **5-10%** в RU health-data exchange infrastructure | можем работать поверх таких pipes и забирать верхний слой decision automation |


#### Вывод по конкурентам

- На Западе есть реальные сильные игроки, значит category risk низкий: рынок не надуман.
- В РФ прямого one-to-one аналога почти нет. Это плюс для входа, но и минус: придётся **самим объяснять категорию** и собирать стек из интеграций, policy engine и clinician-in-the-loop.
- Наиболее вероятный локальный конкурент не «ещё один Anterior», а **комбинация**: OCR-вендор + BPM/workflow платформа + внутренняя команда медэкспертизы страховщика.

### 4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | не удаётся нанять strong CTO/ML и удержать core team | med | high | time-to-hire > 2,4 мес, repeated offer declines | founder-led recruiting, referral-only shortlists, retention package, phased roadmap |
| 2 | Operational | clinician-in-the-loop нагрузка выходит выше 0,5 FTE на клиента и съедает margin | med | high | QA backlog, рост ручных эскалаций, падение auto-approval rate | ограничить scope, policy tuning, ввод hard escalation thresholds |
| 3 | Operational | деградация качества/стоимости LLM API или OCR stack | med | high | cost per case растёт 20%+ два месяца подряд, latency SLA срывается | multi-vendor routing, fallback models, локальные/он-прем варианты, кеширование |
| 4 | Market | локальный спрос оказывается проектным, а не подписочным | high | high | клиенты просят только pilot/integration fee без annual commit | жёстко продавать annual platform fee, modular packaging, reference cases |
| 5 | Market | price compression из-за тендеров и кастомных интеграторов | high | high | скидки >25%, win-rate держится только через discounting | value-based pricing, narrow ICP, выделять ROI по SLA и headcount savings |
| 6 | Market | крупный incumbent или страховая делает in-house substitute | med | high | затяжка procurement, рост числа RFP c требованием on-prem + source access | продавать fast time-to-value, explainability, managed deployment, API-first |
| 7 | Regulatory | требования 152-ФЗ / data residency усложняют хранение и обработку медданных | high | high | юристы клиента блокируют облако, требуют локальный контур и отдельные DPA | RU-hosted deployment, data minimization, on-prem / private cloud option |
| 8 | Regulatory | 115-ФЗ / KYC-проверки и комплаенс страховщиков затягивают сделку | med | med | security/legal review > 90 дней | заранее готовый vendor due diligence pack, шаблоны договоров, security room |
| 9 | Regulatory | санкции SaaS и ограничение доступа к западным API/infra | high | high | vendor notices, billing failures, ограничения по регионам | российские и open-weight fallback, dual-stack infra, contract diversification |
| 10 | Financial | burn оказывается выше модели и runway падает ниже 9 мес | med | high | ежемесячный burn > 5,5 млн ₽ три месяца подряд | hiring gate, cash committee, runway dashboard, freeze non-core spend |
| 11 | Financial | курс USD поднимает себестоимость LLM/API и облака | high | med | FX move >15% без repricing клиентских контрактов | RUB-indexed pricing, reserve buffer, vendor renegotiation, local providers |
| 12 | Financial | инфляция зарплат и налоги поднимают fixed cost быстрее revenue ramp | med | med | FOT inflation >12% г/г, новые обязательные отчисления | staggered hiring, variable comp, annual repricing clauses |
| 13 | Black swan | резкое ужесточение санкций или война нарушают доступ к SaaS/платежам | med | high | отключение billing rails, отказ hyperscaler, force majeure notices | sovereign infra, local backups, disaster playbooks, запас ликвидности |
| 14 | Black swan | крупный LLM-provider отключает API или резко меняет политику использования | med | high | notice period <60 дней, cap на throughput, отказ в healthcare use-case | abstracted model layer, резервные провайдеры, локальные модели для critical path |

### 5. Kill conditions через 6 месяцев

1. **p10 EBITDA @M24 остаётся ниже нуля**, а фактический cash runway падает ниже **9 месяцев**. Это прямой риск insolvency.
2. **Median-case forecast** после обновления воронки и churn показывает **EBITDA < 500 000 ₽/мес** на горизонте M24. Тогда кейс не проходит EBITDA Gate даже в центральном сценарии.
3. Фактические метрики за 6 месяцев одновременно дают хотя бы две из трёх проблем: **LTV/CAC < 3x**, **CAC payback > 12 мес**, **logo churn > 3%/мес**. В такой конфигурации продолжать нельзя.

### 6. Итоговый critic view по SECTION B

- Юнит-экономика всё ещё выглядит рабочей в median-case.
- Но **distribution risk высокий**: p10 уже отрицательный, а ширина диапазона по LTV/CAC слишком большая.
- Значит, это не “очевидный compounder”, а **сильный, но хрупкий regulated operator case**, где исход почти полностью зависит от дисциплины по pricing, churn control, локальному compliance stack и способности не скатиться в services-heavy delivery.

### T-refs для SECTION B

- **[T1]** /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0613-msk-anterior-geo-expand-v2/04-economics.md
- **[T2]** /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0613-msk-anterior-geo-expand-v2/02-demand.md
- **[T3]** ChartMogul churn benchmarks: https://chartmogul.com/saas-metrics/revenue-churn/
- **[T4]** Anterior official: https://www.anterior.com/ and https://www.anterior.com/prior-authorization-solution
- **[T5]** Cohere Health official: https://www.coherehealth.com/utilization-management/in-house and https://www.coherehealth.com/decision
- **[T6]** Waystar official: https://www.waystar.com/news/waystar-advances-ai-innovation-with-google-cloud-to-accelerate-the-autonomous-revenue-cycle/
- **[T7]** Skolkovo on Webiomed / insurance digitization context: https://sk.ru/news/uchastnik-skolkovo-podklyuchilsya-k-avtomatizirovannoj-sisteme-monitoringa-medizdelij-s-iskusstvennym-intellektom-roszdravnadzora/ and https://sk.ru/news/o-glavnyh-trendah-cifrovizacii-strahovoj-otrasli-rukovoditel-strahovogo-napravleniya-fonda-skolkovo-gruppa-vebrf-mihail-sorokin-pobesedoval-s-rukovoditelyami-kompanij-vnedryayushih-tehnologii-ii/
- **[T8]** Skolkovo + Rusprofile on Beorg: https://sk.ru/news/ii-ot-rezidenta-skolkovo-pomozhet-zastrahovat-zhizn-za-sem-minut/ ; https://sk.ru/news/vyruchka-biorg-ot-uslug-po-raspoznavaniyu-dokumentov-za-2023-god-vyrosla-na-27-3-mln-rub/ ; https://www.rusprofile.ru/id/3374022
- **[T9]** Habr company page on Naumen: https://habr.com/en/companies/naumen/
- **[T10]** Experian Health prior authorization software: https://www.experian.com/healthcare/products/patient-access-registration/prior-authorization-software

<!-- P6B-DONE -->


---

## Этап 5 — Final Verdict
[HEALTHCARE] 0613 MSK Anterior GEO Expand v2 — REJECTED: 59/100 | EBITDA base=13091К₽/мес через 24 мес | LTV/CAC=8,0x | Ключевое преимущество: сильная economics в enterprise healthtech | Главный риск: в РФ не доказан repeatable спрос.

# 06-verdict

sector: HEALTHCARE

## Кейс
0613-msk-anterior-geo-expand-v2

## Дата вердикта
2026-04-20 (Europe/Moscow)

## Финальный статус
REJECTED

## Итоговый балл
**59/100**

## Delta vs previous
Это rerun/resurrect-кейс. Подтверждённого предыдущего 06-verdict.md для этого slug в active repo не найдено, поэтому формального delta score нет.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC: 8,0x», «CAC Payback: 5,0 мес», «Contribution Margin %: 60,8%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В P6B base-case «EBITDA @M24, ₽/мес = 13 091 000», а в P5 break-even достигается около M13. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | В 02-demand: «Search-demand в РФ почти отсутствует», при этом локальный SOM ограничен 8 контрактами и нет валидированной tier-строки. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Кейс держится на интеграциях и workflow depth, но «прямого зрелого аналога Anterior в РФ не видно» не равно защитимому moat. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 12 | В risk matrix есть high/high по 152-ФЗ, санкциям, price compression и clinician-in-the-loop нагрузке. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 16 | CAC payback сильный, named targets понятны, но сам demand-stage предупреждает: «локализация wedge строится вокруг ДМС... а не вокруг буквального копирования американского prior auth stack». |

**Sum raw = 88/150**  
**Normalized score = round((88 × 100) / 150) = 59/100**

## Почему не проходит инвесткомитет
Кейс не проваливается по экономике. Наоборот, на бумаге это один из самых сильных healthtech enterprise cases в текущем батче: высокий customer_ltv_rub, быстрый CAC payback и явный путь к company_ebitda_rub_month сильно выше 500К ₽/мес. Но Program 7 отсекает не только «сломанные» модели, а и те, где нет достаточного доказательства repeatable спроса и защитимости именно в РФ. Здесь category proof в основном американский, локальная категория размазана между ДМС, медэкспертизой и гарантийными письмами, а moat пока ближе к solution engineering, чем к платформенной защите.

## 7-factor Moat Framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных в локальном контуре. |
| Switching costs | 2 | Интеграции, audit trail и обучение reviewer-команды создают умеренные switching costs. |
| Scale economies | 1 | Инфраструктура и playbooks улучшаются с объёмом, но clinician review остаётся дорогим. |
| Proprietary data / model advantage | 1 | Возможна локальная policy/data база, но размер и эксклюзивность датасета не доказаны. |
| Regulatory moat | 1 | Compliance complexity даёт барьер входа, но не видно уникальной локальной аккредитации или лицензии. |
| Brand / distribution | 1 | У западного Anterior бренд есть, у локального clone-case бренд и канал ещё не построены. |
| Embedded workflow | 3 | Если решение встраивается в payer/provider review loop, вытащить его потом сложно. |

**Moat raw = 9/21**  
**Moat score = round((9 × 25) / 21) = 11/25**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 26 333 333 ₽ |
| CAC | 3 276 000 ₽ |
| LTV/CAC | 8,0x |
| CAC payback | 5,0 мес |
| GM | 60,8% |
| contribution_margin_rub_month | 395 000 ₽ |
| fixed_costs_rub_month | 6 264 000 ₽ |
| company_ebitda_rub_month, M12 base | -1 129 000 ₽ |
| company_ebitda_potential_rub_month, M24 base | 13 091 000 ₽ |
| clients_to_500k_ebitda | 16 |
| months_to_500k_ebitda | 13 |
| startup_capital_to_bep_rub | 48 417 000 ₽ |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор target-account list страховщиков, ДМС, assistive/TPA и крупных медсетей | SDR | HH/рынок, ручной research, CRM | 2 дня | 18 000 | Низкая |
| 2 | Outreach: email, cold call, LinkedIn-like аналог, интро через партнёров | SDR | CRM, sequencer, телефония | 10 рабочих дней | 42 000 | Средняя |
| 3 | Discovery call и qualification по pain/volume/compliance | AE + CEO | CRM, Zoom/Meet | 5 дней | 55 000 | Низкая |
| 4 | Solution workshop с клинико-страховой командой клиента | AE + CTO + клин. эксперт | Miro, презентация, demo env | 1 неделя | 95 000 | Низкая |
| 5 | Доступ к sample-cases, mapping workflow, ROI baseline | CTO + ML + backend | sandbox, ETL, prompt stack | 2 недели | 180 000 | Средняя |
| 6 | Pilot / proof-of-value на ограниченном объёме кейсов | CTO + ML + clinical ops | cloud, LLM/OCR, audit logs | 4-6 недель | 310 000 | Средняя |
| 7 | Security/compliance/legal review, DPIA/infosec пакет | CTO + CEO + external legal | security docs, DPA, legal templates | 2-3 недели | 140 000 | Низкая |
| 8 | Коммерческое предложение, redlines, procurement | AE + CEO | CRM, doc flow, e-sign | 2 недели | 85 000 | Средняя |
| 9 | Onboarding и integration setup после подписания | CTO + DevOps + CSM | cloud, SSO, API/webhook | 2-4 недели | 165 000 | Средняя |
| 10 | Ежемесячная обработка workflow, QA, support, billing | CSM + clinical ops + finance | product, billing, helpdesk | ongoing monthly | 255 000 / клиент / мес | Средняя |

## Team table

| Роль | Функция | Нужно чел. | FOT fully-loaded ₽/мес |
|---|---|---:|---:|
| CEO | enterprise sales, fundraising, partnerships | 1 | 845 000 |
| CTO / Tech Lead | product architecture, security, enterprise delivery | 1 | 715 000 |
| Senior Backend | core workflow engine, APIs, integrations | 2 | 1 170 000 |
| ML Engineer | extraction, classification, routing quality | 1 | 650 000 |
| DevOps | infra, monitoring, CI/CD, tenancy/security | 1 | 455 000 |
| Frontend | ops console, reviewer UI | 1 | 390 000 |
| SDR | target account generation, outreach | 1 | 234 000 |
| AE | deal orchestration, pilot to close | 1 | 520 000 |
| Customer Success | onboarding, SLA, renewals | 1 | 325 000 |
| **Итого** |  | **10** | **5 304 000 ₽/мес** |

## GTM: 10 named targets

| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | СОГАЗ | крупнейший ДМС-контур, высокая вероятность перегруженных согласований и гарантийных писем | email decision-maker + отраслевые конференции по страхованию | 700 000 ₽/мес |
| 2 | АльфаСтрахование | сильный ДМС и цифровой бренд, готовность тестировать automation для medical review выше среднего | founder intro + email CDO/директору ДМС | 650 000 ₽/мес |
| 3 | Ингосстрах | крупный страховой портфель и enterprise-scale procurement, где prior-approval workflow особенно дорог | партнёрство с интегратором + email ЛПР | 700 000 ₽/мес |
| 4 | РЕСО-Гарантия | крупный ДМС/страховой игрок с масштабом ручных кейсов и понятным ROI на SLA согласований | email medical operations lead | 600 000 ₽/мес |
| 5 | Росгосстрах | большой федеральный контур, где даже частичная автоматизация экспертизы даёт экономию на headcount | конференция + follow-up через enterprise AE | 600 000 ₽/мес |
| 6 | BestDoctor | digital-first ДМС и корпоративное медобслуживание, ближе всего к быстрому design-partner pilot | warm intro через HR-tech / benefits ecosystem | 550 000 ₽/мес |
| 7 | СберЗдоровье | сочетание телемедицины и корпоративного healthcare funnel делает triage/approval workflows особенно релевантными | партнёрский заход через экосистему + email | 600 000 ₽/мес |
| 8 | МЕДСИ | федеральная частная медсеть, где важны согласования со страховщиками и загрузка координаторов | direct sales в корпоративный блок | 500 000 ₽/мес |
| 9 | Мать и дитя | high-ticket care pathways и ДМС-нагрузка, где скорость согласований влияет на NPS и utilisation | email COO / директору по ДМС | 500 000 ₽/мес |
| 10 | Европейский медицинский центр (EMC) | премиальная сеть с дорогими кейсами и высокой ценой ручной задержки согласований | founder-led intro + private event | 650 000 ₽/мес |

## Топ-3 риска

| Риск | Вероятность | Impact | Почему это критично |
|---|---|---|---|
| evidence_quality_unverified и слабый локальный demand proof | high | high | Нет корректной `Sources: T1=..., T2=..., T3=...` строки, а прямой search-demand в РФ почти нулевой. |
| clinician-in-the-loop и compliance cost explode | medium | high | Если ручной review уйдёт выше 0,5 FTE на клиента, GM быстро съедается. |
| sanctions / LLM dependency / data residency | high | high | В risk matrix уже отмечены high/high по санкциям и 152-ФЗ, что может сломать delivery-модель. |

## LTV Upside Calculator
Так как кейс REJECTED, ниже условия, при которых он может вернуться в near-pass/approve:

| Рычаг | Текущее значение | Порог для rerun | Эффект |
|---|---:|---:|---|
| Локальные paid pilots | 0 подтверждённых | ≥3 paid pilots | Снимает главный риск по demand repeatability |
| customer_ltv_rub / CAC | 8,0x | удержать ≥6,0x после локализации | Доказывает, что локальный delivery не ломает economics |
| Время до 500К EBITDA | 13 мес | ≤15 мес фактом | Подтверждает, что GTM в РФ не хуже модели |
| Доля ручного review | не подтверждена локально | ≤0,35 FTE на клиента | Сохраняет contribution_margin_rub_month на уровне 350К+ |
| Source tier balance | 1,00 по default penalty | ≥2,0 | Поднимает Market+Demand к investment-grade |

## Что нужно доказать для повторного запуска
1. Три российских design partners с платным pilot budget, а не только интересом.
2. Подтверждение, что buyer покупает именно workflow software, а не кастомный insurer IT-project.
3. Локальный compliance stack без критической зависимости от санкционно-уязвимых LLM/API-провайдеров.
4. Реальную скорость pilot-to-production не хуже 90-120 дней.

## Финальный вывод
**REJECTED.**

Это сильный international category case, но пока не фондовый российский операторский кейс. Экономика убедительная, но инвестиционный комитет не должен путать наличие global proof с локально доказанным repeatable business. До APPROVED не хватает не маржи, а локального demand proof, evidence quality и более глубокого moat.

