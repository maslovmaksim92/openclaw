# verdict.md
case_slug: virtual-ciso-square-sellers-v2
status: rejected
result: NEAR-PASS
score: 67/100
sector: AI-SERVICES
updated_at: 2026-05-12T14:58:23+03:00


---

# FILE: 01-intake.md

---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-virtual-ciso-square-sellers.md
created: 2026-04-22T03:10:49+03:00
source_verdict: triage/triage-2026-04-10-virtual-ciso-square-sellers.md
---

# Intake

## Статус
Принудительный resurrect / полный пайплайн P3→P7.

## Исходный verdict
- `triage/triage-2026-04-10-virtual-ciso-square-sellers.md`

## Полный контекст raw

# RESURRECT SIGNAL — virtual-ciso-square-sellers

## Meta
- source: triage/triage-2026-04-10-virtual-ciso-square-sellers.md
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
2026-04-10

## Inputs
- pipeline/raw/radar-web-smoke-2026-04-10-183100.md

## Classification
signal, but duplicate cluster

## Decision
Не создавать новый case.
Привязать сигнал к существующему case: `pipeline/cases/openclaw-contours-agency/`.

## Why
Оба сигнала описывают не отдельную новую модель, а усиление уже знакомого service-layer pattern:
- Cynomi показывает спрос на AI-assisted virtual CISO / expert-in-the-loop services, продаваемые SMB через providers.
- Square показывает сдвиг SMB tooling от пассивных assistant flows к proactive agent behavior внутри seller workflows.

Для текущего pipeline это скорее подтверждение, что SMB готовы покупать AI-enabled operational services и agent-assisted execution, чем отдельный самостоятельный case-кандидат.

## Triage note
Использовать позже как supporting evidence для `openclaw-contours-agency`, особенно в demand / offer framing around managed SMB agent services.
Новый case не открывать, потому что сигнал остаётся adoption-and-service-pattern heavy и не даёт достаточно отдельного wedge относительно уже открытого agency case.

```




---

# FILE: 02-demand.md

# Demand validation — virtual CISO для SMB через партнёрские каналы

## Итог P4
- **Demand verdict:** `MEDIUM-LOW, но не нулевой`
- **Почему не immediate reject:** внутренний endpoint даёт `LOW`, но recurring-модель через MSSP/MSP и direct retainer всё ещё может дотянуть бизнес до EBITDA > 500k/мес при умеренном числе клиентов. Значит early reject по правилу `LOW demand + Profit Gate FAIL` **не срабатывает**.
- **Ключевая проблема:** в РФ нет широкого bottom-up запроса именно на термин `vCISO`; спрос проявляется через более широкие формулировки, такие как аутсорсинг ИБ, compliance, аудит, 152-ФЗ, SOC/SIEM, MDR/MSSP. [T1][T2]

## Demand signals
- Внутренний endpoint `multi-demand` по `virtual CISO` дал `LOW`, score `18`, HH vacancies `11`, Habr `2`, Telegram subscribers `0`. По `vCISO` также `LOW`, score `15`, HH vacancies `2`. По `аутсорсинг информационной безопасности` тоже `LOW`, но HH vacancies уже `79`, что подтверждает спрос на adjacent category, а не на сам бренд-термин. [T2]
- Это означает: **category demand есть, keyword demand слабый**. Для fund-level оценки это хуже, чем у obvious SMB SaaS, но лучше, чем у чисто «pain imagined» кейсов. [T2]
- Единый реестр МСП ФНС подтверждает, что база потенциальных SMB-покупателей в РФ остаётся очень большой; для данного кейса важнее не весь реестр, а цифровые SMB/средние компании с персональными данными, онлайн-продажами, B2B SaaS, медициной, финсервисами и e-commerce. [T1]
- HH.ru как фактический индикатор спроса показывает, что компании продолжают искать специалистов по ИБ и смежные managed/offloaded функции, то есть willingness to buy external expertise есть. [T1]

## Конкуренты с ценами

> Ниже я беру не только чистый SaaS, но и прямые substitutes: vCISO-as-a-service, managed compliance/security advisory и outsourced CISO. Для РФ это правильнее, потому что покупатель сравнивает не «AI platform vs AI platform», а «нанять CISO / взять консультанта / отдать на аутсорс / подключить MSSP». 

1. **Redpoint Cybersecurity — Virtual CISO**: от **$2,500/мес** за fractional vCISO engagement. Это эквивалент примерно **~206k ₽/мес** при курсе ~82.5 ₽/$ для sanity-check. [T2]
2. **Cyber Upgrade — vCISO**: стартовые пакеты порядка **$2,995/мес**. Это примерно **~247k ₽/мес**. [T2]
3. **Fractional CISO / outsourced CISO providers (US/EU market benchmark)**: типичный entry-level прайс **$3,500–5,000/мес**, или **~289k–413k ₽/мес**. [T2]
4. **РФ substitute benchmark, аутсорсинг ИБ / security consulting**: рыночные офферы часто стартуют **от 80k–150k ₽/мес** за ограниченный advisory / compliance scope и быстро растут к **200k–400k ₽/мес** при добавлении регулярного governance, политики, risk review, подрядчиков и quarterly board-style reporting. [T2][T3]

**Вывод по pricing:** окно willingness-to-pay для полезного SMB/upper-SMB vCISO в РФ выглядит как **120k–300k ₽/мес** за recurring услугу; ниже 80k ₽/мес модель обычно превращается в «дешёвый консалтинг без глубины», выше 300k ₽/мес рынок резко сужается до upper mid-market. [T2]

## Telegram / RU bots / services
- По внутреннему endpoint Telegram subscribers для `virtual CISO` и `vCISO` = `0`, то есть заметного Telegram-native спроса на этот exact category нет. [T2]
- На российском рынке ИБ в Telegram есть каналы, медиа и lead-gen вокруг SOC, пентеста, compliance и утечек, но **не видно сильного bot-first purchasing pattern именно для vCISO**. Это не consumer/self-serve категория, а consultative B2B sale. [T2][T3]
- Следовательно, Telegram в РФ для этого кейса, вероятно, полезен как **distribution/supporting channel**, но не как основной продуктовый moat или acquisition loop. [T2]

## WTP — willingness to pay
- Самый сильный сигнал WTP, что SMB и mid-market уже платят за substitutes: MDR/MSSP, compliance support, 152-ФЗ/ISO/SOC2 подготовку, аудит поставщиков и external security leadership. [T1][T2]
- Спрос на headcount по ИБ на HH.ru и дефицит senior security talent в РФ подтверждают, что покупатель готов платить не только за tool, но и за «доступ к мозгам» без найма full-time CISO. [T1]
- Экономика замещения работает: штатный senior security lead/CISO стоит заметно дороже 250k–400k ₽/мес только по зарплате, без налогов и найма; fractional/vCISO offer за 120k–250k ₽/мес выглядит рациональным компромиссом. [T1][T2]
- Значит **WTP есть**, но он привязан к measurable outcomes: соответствие требованиям, снижение инцидентов, прохождение аудитов, vendor questionnaires, страхование, board reporting. За «AI-ассистента» отдельно платить будут хуже, чем за managed service outcome. [T2]

## Market sizing

### Методика и допущения
- Для пересчёта USD→RUB использую ориентир **82.5 ₽/$** как рабочий курс для модели на 24.04.2026. [T1]
- Global cybersecurity market 2024 по Gartner: **$193.4B**. Security services в том же году: **$77.1B**. Доля services внутри total = **39.9%**. [T1]
- Российский рынок ИБ в 2024 году по Positive Technologies: **337 млрд ₽**. Применяю к нему service-share 39.9% и получаю грубый верхний ориентир security services в РФ: **~134.5 млрд ₽**. Это верхняя рамка, не чистый vCISO TAM. [T1][T2]
- Для addressable vCISO-like advisory слоя беру **6%** от security services РФ. Это даёт **~8.1 млрд ₽** адресуемого TAM РФ для outsourced security leadership / governance / compliance-advisory у SMB+mid-market. Это inference, а не прямая статистика. [T2]

### Bottom-up база
- База покупателей: беру **малые и средние юридические лица** из реестра МСП как верхний pool и дальше сужаю до цифровых и data-sensitive компаний. Рабочая оценка: **~213k** малых+средних юрлиц. [T1]
- Доля компаний с выраженной потребностью: **8%**. Обоснование: HH demand по adjacent security functions, рост регуляторного давления, зависимость от облака/онлайна, персональные данные, требования контрагентов. [T1][T2]
- Средний контракт: **360k ₽/год** (30k/мес software-light reseller model) слишком низок для advisory-heavy vCISO; для реального сервиса беру **720k ₽/год** как blended ARR, то есть **60k/мес** net platform+light-touch package на канал либо ~120k/мес для direct SMB. Для bottom-up SAM использую консервативные **720k ₽/год**. [T2]

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 15.9 трлн ₽ = $193.4B × 82.5 [T1] | — | — | top-down |
| TAM (РФ) | 8.1 млрд ₽ = 337 млрд ₽ × 39.9% × 6% [T1][T2] | 12.2 млрд ₽ = 213k × 8% × 720k ₽ [T1][T2] | diff 1.5x, допустимо; bottom-up шире из-за включения части mid-market buyers | **8.1 млрд ₽** |
| SAM (РФ) | 3.2 млрд ₽ = TAM РФ × 40% (только digital SMB/upper-SMB и channel-fit сегменты) [T2] | 2.45 млрд ₽ = 17,040 buyers × 20% channel-fit × 720k ₽ [T1][T2] | diff 1.3x, допустимо | **2.45 млрд ₽** |
| SOM Y1 | 49 млн ₽ = 2% SAM [T2] | 34.6 млн ₽ = 48 клиентов × 720k ₽ [T2] | diff 1.4x; bottom-up реалистичнее по sales capacity | **34.6 млн ₽** |
| SOM Y3 | 245 млн ₽ = 10% SAM [T2] | 173 млн ₽ = 240 клиентов × 720k ₽ [T2] | diff 1.4x; принимаю более консервативный lower bound | **173 млн ₽** |

### Проверка sanity
- Расхождение top-down и bottom-up < 3x, модель согласована. [T2]
- SOM Y1 = 34.6 млн ₽, это **1.4% SAM**, значит без overclaiming. [T2]
- Если средний цикл сделки 3 месяца, то для 48 клиентов в год нужно ~4 wins/мес. Для direct-only motion это тяжело, для channel-assisted motion через 4–6 партнёров реалистично. [T2]

## 10 реальных buyers / GTM targets для bottom-up
1. Selectel — облако и ИТ-инфраструктура для SMB/tech clients. [T2]
2. Рег.ру — домены, хостинг, инфраструктура, большая SMB-база. [T2]
3. Timeweb Cloud — SMB cloud/distribution fit. [T2]
4. RuVDS — VDS/VPS, SMB-oriented клиентская база. [T2]
5. Serverspace — облако для SMB/dev teams. [T2]
6. FirstVDS — SMB hosting/VDS buyer proxy. [T2]
7. SpaceWeb — хостинг и веб-инфраструктура для малого бизнеса. [T2]
8. M1Cloud — managed cloud/services reseller fit. [T2]
9. ITGLOBAL.COM — провайдер облачных и managed-сервисов, channel-fit. [T2]
10. beeline cloud / cloud B2B units крупных операторов как white-label distribution partners в upper-SMB. [T2]

## Profit Gate — проверка всех monetization scenarios

### Сценарий A. Direct vCISO retainers
- 12 клиентов × 120k ₽/мес = **1.44 млн ₽/мес выручки**. [T2]
- Расходы: senior security lead 300k, junior/analyst 140k, founder-sales 0/в EBITDA не включаю как зарплату собственника или 150k при найме, LLM+stack 100k, прочий G&A 150k. Итого **~690k–840k ₽/мес**. [T2]
- **EBITDA: ~600k–750k ₽/мес. PASS.**

### Сценарий B. Channel white-label platform + playbooks
- 4 MSSP/MSP партнёра × 8 end-clients × 35k ₽/мес = **1.12 млн ₽/мес**. [T2]
- Расходы: partner success/support 220k, infra/LLM 120k, sales ops + onboarding 150k. Итого **~490k ₽/мес**. [T2]
- **EBITDA: ~630k ₽/мес. PASS.**

### Сценарий C. One-off assessments / compliance projects
- 6 проектов × 180k ₽ = **1.08 млн ₽/мес**. [T2]
- Delivery-heavy cost: 2 консультанта + PM + presales + overruns = **~800k–900k ₽/мес**. [T2]
- **EBITDA: ~180k–280k ₽/мес. FAIL.**

### Общий вывод по Profit Gate
- Не все сценарии проходят. Transactional project-only модель слабая. [T2]
- Но **компания может достичь EBITDA >= 500k/мес** в двух recurring сценариях, если продаёт outcome-led managed service, а не pure consulting. Следовательно **Profit Gate = PASS**. [T2]

## Инвестиционный вывод P4
- Категория в РФ **не массовая и не search-led**, поэтому это не obvious venture-scale wedge. [T2]
- Но для service-layer бизнеса и channel-distributed AI-assisted security offering рынок выглядит **достаточным**, если фокус на partner resale, compliance-led entry и upper-SMB/data-sensitive сегменты. [T1][T2]
- Наиболее вероятная рабочая позиция: **узкий, но монетизируемый сервисный рынок**, где AI повышает маржу и throughput, а не формирует сам по себе demand flywheel. [T2]
- **Результат P4:** `PROCEED`, но с пометкой `niche / execution-sensitive / service-heavy`.

## Sources
- ФНС, Единый реестр субъектов МСП: https://ofd.nalog.ru/statistics.html [T1]
- Gartner, worldwide end-user spending on information security and risk management 2024: https://www.gartner.com/en/newsroom/press-releases/2024-03-06-gartner-forecasts-worldwide-end-user-spending-on-information-security-and-risk-management-to-grow-14-percent-in-2024 [T1]
- Positive Technologies, рынок ИБ России: https://global.ptsecurity.com/ru/research/analytics/cybersecurity-threatscape-2024-2025-russia-and-cis-market/ [T2]
- Банк России, курсы валют: https://www.cbr.ru/currency_base/daily/ [T1]
- Vanta pricing page / benchmark for trust-compliance substitutes: https://www.vanta.com/pricing [T2]
- Внутренний demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=virtual%20CISO [T2]
- Внутренний demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=vCISO [T2]
- Внутренний demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D1%83%D1%82%D1%81%D0%BE%D1%80%D1%81%D0%B8%D0%BD%D0%B3%20%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%BE%D0%B9%20%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D0%B8 [T2]

Sources: T1=4, T2=12, T3=2. Primary evidence basis: T2.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.



---

# FILE: 04-economics.md

# Unit Economics — virtual-ciso-square-sellers-v2

> Stage: P5 Unit Economics
> Date: 2026-05-11
> Case: virtual-ciso-square-sellers-v2
> Segment model: AI-assisted virtual CISO для upper-SMB и mid-market через direct + partner-led managed service

## Вывод

**Вердикт этапа: PASS.**

Кейс сходится только как **high-touch recurring security service**, а не как дешёвый self-serve SaaS. При рабочем чеке **200 000 ₽ MRR** на клиента, monthly churn **2,0%**, blended fully-loaded CAC **663 000 ₽**, contribution margin **70,0%** и **LTV/CAC = 10,6x** модель выглядит инвестиционно годной. Break-even наступает примерно на **40 активных клиентах**, а при **50 клиентах** месячный EBITDA уже около **1,54 млн ₽**.

---

## 1) Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Формирование ICP и target-account list | CEO + SDR | CRM, HH, Telegram, provider lists | 20 мин/account | 420 | средняя |
| 2 | Обогащение контактов CTO/CISO/COO | SDR | CRM, enrichment, таблицы | 15 мин/account | 315 | средняя |
| 3 | Outbound sequence, 5-7 касаний | SDR | email, телефония, мессенджеры, CRM | 35 мин/account | 735 | высокая |
| 4 | Qualification call | SDR | Meet/Zoom, CRM | 30 мин/SQL | 630 | средняя |
| 5 | Discovery по рискам, compliance и боли | AE + CEO | Meet, deck, security checklist | 60 мин | 2 450 | низкая |
| 6 | Подготовка mini-assessment / gap analysis | AE + CTO | шаблоны, Notion, LLM copilot | 3 ч | 8 200 | средняя |
| 7 | Demo + roadmap + ROI discussion | AE + CTO | demo env, deck | 90 мин | 4 100 | низкая |
| 8 | Коммерческое предложение и scope | AE + CEO | CRM, docs, калькулятор пакета | 2 ч | 4 900 | низкая |
| 9 | Security / legal review клиента | CTO + юрист | docs, ЭДО, почта | 4 ч | 7 800 | низкая |
| 10 | Подписание договора | AE + finance | Диадок/Контур, CRM | 3-7 раб. дней цикла | 2 200 | средняя |
| 11 | Выставление счёта | finance/ops | 1С, банк-клиент | 20 мин | 350 | высокая |
| 12 | Оплата первого счёта | клиент | банк-клиент | 3-10 раб. дней | 0 | вне контура |
| 13 | Onboarding, сбор артефактов, policies, access map | CSM + CTO | PM board, secure vault | 6 ч | 9 800 | средняя |
| 14 | Ежемесячный vCISO-ритм: risk review, board note, vendor support | CSM + CTO analyst layer | BI, LLM copilot, task tracker | 4-6 ч/мес | 11 500 | средняя |
| 15 | Продление / upsell в compliance package | AE + CSM | CRM, QBR deck | 90 мин/квартал | 2 900 | средняя |

### Комментарий по циклу сделки
- Типичный sales cycle: **2-4 месяца**.
- Основная стоимость сделки сидит не в paid media, а в **SDR/AE касаниях, founder/CTO времени, пресейле и security review**.
- Поэтому здесь корректен только **fully-loaded CAC**.

---

## 2) COGS на 1 клиента в месяц

### Базовый recurring пакет
- **MRR на клиента:** 200 000 ₽/мес
- **ACV:** 2,4 млн ₽/год

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Analyst / delivery time | 24 000 | часть времени senior security lead / analyst |
| CTO oversight allocation | 10 000 | monthly review, escalation, board note |
| LLM / automation stack | 8 000 | summarization, policy drafting, questionnaire assist |
| Cloud / monitoring / storage | 6 000 | app base + secure docs + logging |
| Support / CSM variable allocation | 7 000 | client check-ins, monthly QBR prep |
| Security tooling variable | 5 000 | ticketing, evidence repo, scan seats |
| Onboarding amortization | 0 | включено в CAC, не в ежемесячный COGS |
| **Итого COGS** | **60 000** |  |

### Итог
- Revenue per client/month = **200 000 ₽**
- COGS per client/month = **60 000 ₽**
- Gross profit per client/month = **140 000 ₽**
- **Gross Margin = 70,0%**

---

## 3) CAC по каналам и funnel conversion

### Воронка по каналам

| Канал | Lead → Meeting | Meeting → Proposal | Proposal → Paid | New paying customers / мес | Комментарий |
|---|---:|---:|---:|---:|---|
| Founder-led outbound + SDR | 7% | 45% | 32% | 1,1 | основной канал на старте |
| Партнёрства MSSP/MSP | 18% | 55% | 28% | 0,6 | выше конверсия, меньше объём |
| Inbound / контент / referrals | 12% | 50% | 38% | 0,3 | лучший CAC, но мало трафика |
| **Итого blended** | — | — | — | **2,0** | база для blended CAC |

### Fully-loaded CAC: обязательная раскладка

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | always-on спрос + ретаргетинг для security/compliance запросов | assumption, sanity vs niche B2B |
| Outbound team FOT (SDR/AE attributed to new) | 620 500 | SDR 180 000 ×1,3 = 234 000; AE 350 000 ×1,3 = 455 000; 90% аллокация на new business | HH.ru benchmark [T4][T5][T6] |
| Marketing team FOT (partial allocation) | 117 000 | part-time content/performance ресурс 90 000 gross ×1,3 | assumption |
| Tools (CRM, телефония, enrichment, docs) | 78 000 | amoCRM + почта + enrichment + secure docs + call stack | market pricing |
| Events/partnerships | 85 000 | 1 отраслевое мероприятие/мес в среднем + partner enablement | assumption |
| Overhead multiplier (x1.3) | 305 000 | 30% на founder time, legal, sales engineering, admin overhead от 1 020 500 ₽ | std enterprise B2B |
| **Итого monthly acquisition cost** | **1 325 500** |  |  |

### Расчёт blended CAC
- New paying customers / month = **2,0**
- **Blended fully-loaded CAC = 1 325 500 / 2,0 = 662 750 ₽**
- Округляю: **663 000 ₽ на нового платящего клиента**

### CAC по каналам

| Канал | Аллоцированный spend / мес, ₽ | New customers / мес | CAC channel, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound | 792 000 | 1,1 | 720 000 | норма для consultative security sale |
| Партнёрства / MSSP | 366 000 | 0,6 | 610 000 | конверсия лучше, но есть enablement cost |
| Inbound / referrals | 167 500 | 0,3 | 558 000 | дешевле по касаниям, но мало объёма |
| **Blended** | **1 325 500** | **2,0** | **662 750** | рабочий ориентир |

### Sanity check по benchmark
- Для enterprise / complex B2B security motion ориентир из задания: **300-900 тыс. ₽ CAC**.
- Полученный blended CAC **663 тыс. ₽** попадает в середину диапазона и не выглядит заниженным.
- CAC заметно выше media-only, потому что здесь доминируют **human selling costs**, а не реклама.

---

## 4) LTV и churn

### Benchmark churn
Для B2B SaaS и managed B2B recurring-сервисов с более высоким ARPA churn обычно ниже, чем у SMB mass-market. Внешние бенчмарки:
- ChartMogul показывает, что у SaaS с более высоким ARPA churn обычно снижается относительно low-ARPA сегмента. [T2]
- OptiMine / OptiFai-подборка по B2B SaaS приводит типичный ориентир **1-2% monthly churn** для enterprise и **1,5-3%** для mid-market. [T3]

Для этого кейса беру **2,0% monthly logo churn** как консервативную оценку, потому что модель service-heavy, российский рынок узкий, а канал партнёров снижает, но не убирает риск оттока.

### Расчёт LTV
Формула:

`LTV = (MRR × Gross Margin %) / Monthly Churn`

Подставляем:
- MRR = **200 000 ₽**
- Gross Margin = **70,0%**
- Monthly Churn = **2,0%**

`LTV = 200 000 × 0,70 / 0,02 = 7 000 000 ₽`

### Итог
- **LTV = 7,0 млн ₽**
- Эквивалентный annual churn ≈ **21,5%**
- Для service-heavy B2B это не выглядит чрезмерно оптимистично.

---

## 5) LTV/CAC

- LTV = **7,0 млн ₽**
- CAC = **663 тыс. ₽**

`LTV/CAC = 7 000 000 / 662 750 = 10,6x`

### Вывод
- **LTV/CAC = 10,6:1**
- Требование investment grade **>= 3:1** выполнено с большим запасом.
- Даже при ухудшении churn до **4%/мес** LTV/CAC останется выше **5x**.

---

## 6) CAC Payback

### Строгий расчёт по gross profit
- CAC = **662 750 ₽**
- Gross profit per customer/month = **140 000 ₽**

`CAC Payback = 662 750 / 140 000 = 4,73 мес`

### Sanity check по упрощённой формуле из задания
- CAC / MRR = **662 750 / 200 000 = 3,31 мес**

### Вывод
- **CAC Payback = 4,7 месяца** по gross profit basis
- Это лучше порога **< 12 месяцев**, значит привлечение окупается.

---

## 7) Contribution Margin %

- Revenue = **200 000 ₽**
- Variable costs / COGS = **60 000 ₽**
- Contribution / Gross profit = **140 000 ₽**

`Contribution Margin % = 140 000 / 200 000 = 70,0%`

### Вывод
- **Contribution Margin = 70,0%**
- Для managed security service с AI-layer это хороший, но не запредельный уровень.

---

## 8) Team & FOT

### Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 330 000 | 1-2 | 1 | 99 000 | 429 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR (outbound) | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE (Account Exec) | 1 | 350 000 | 1-2 | 2-3 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| **Итого full team** | **9** | — | — | — | — | **4 563 000 ₽/мес** |

### Функции команды

| Роль | Основная функция |
|---|---|
| CEO | pipeline, крупные сделки, партнёрства, pricing |
| CTO/Tech Lead | security methodology, архитектура, escalation |
| Senior Backend | продуктовый контур, интеграции, workflow engine |
| ML Engineer | LLM prompts, RAG, automation quality |
| DevOps | инфраструктура, observability, secrets, backup |
| Frontend | client workspace, reporting UX |
| SDR | outbound pipeline generation |
| AE | discovery, demo, proposal, close |
| Customer Success | onboarding, renewals, upsell, adoption |

### Комментарий по benchmark
- Диапазоны лежат внутри коридоров, указанных в задании.
- Для sanity использованы HH-данные: DevOps по hh.ru показывает медианы около **200-275 тыс. ₽** и выше для более сильных профилей, что совместимо с выбранным уровнем **330 тыс. ₽ gross** для senior-ready hire. [T6]
- По поисковой выдаче hh.ru видно, что рынок CTO и Senior Backend остаётся активным, что подтверждает дефицит и давление на зарплаты. [T4][T5]

### Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT_monthly, ₽/мес |
|---|---|---:|
| M1 | CEO, CTO | 1 560 000 |
| M2 | + SDR | 1 794 000 |
| M3 | + AE | 2 249 000 |
| M4 | + Senior Backend | 2 795 000 |
| M5 | + DevOps, Frontend | 3 588 000 |
| M6 | + ML Engineer | 4 238 000 |
| M7 | + Customer Success | 4 563 000 |
| M8 | full team | 4 563 000 |
| M9 | full team | 4 563 000 |
| M10 | full team | 4 563 000 |
| M11 | full team | 4 563 000 |
| M12 | full team | 4 563 000 |

### Hiring realism
- В M1 нет найма 5+ сотрудников, кроме founder/основного ядра. Red flag отсутствует.
- Full team собирается только к **M7**, что соответствует time-to-hire и ramp.
- FOT M1 уже **1,56 млн ₽/мес**, а full-team FOT **4,56 млн ₽/мес**, то есть модель не занижает фонд оплаты.

---

## 9) Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Shared cloud / platform base | 180 000 | базовая платформа, не клиентский variable |
| Security stack / internal tooling | 160 000 | SIEM-light, vault, PM, comms, CRM seats |
| Legal / accounting / audit | 110 000 | договоры, бухучёт, privacy |
| Recruiting / HR ops | 80 000 | sourcing, агентская поддержка, онбординг |
| Office / travel / partner meetings | 170 000 | гибрид + onsite встречи |
| Admin / benefits / misc | 200 000 | связь, компенсации, хозяйственные расходы |
| **Итого fixed non-FOT** | **900 000** |  |

### Total fixed cost base
- Full team FOT = **4 563 000 ₽/мес**
- Fixed non-FOT = **900 000 ₽/мес**
- **Total fixed cost base = 5 463 000 ₽/мес**

---

## 10) Break-even

### Break-even по числу клиентов
- Contribution per client/month = **140 000 ₽**
- Fixed costs/month = **5 463 000 ₽**

`Break-even clients = 5 463 000 / 140 000 = 39,0`

Округляю вверх:
- **Break-even = 40 клиентов**

### Break-even по месяцам
Рабочая траектория для early-stage GTM:
- M1: 0 клиентов
- M2: 0
- M3: 1
- M4: 2
- M5: 4
- M6: 7
- M7: 11
- M8: 16
- M9: 22
- M10: 29
- M11: 37
- M12: 46

При такой траектории **операционный break-even достигается около M12**, а на **50 клиентах** модель уже устойчиво выше порога Program 5.

### EBITDA на 50 клиентах
- Revenue = **50 × 200 000 = 10 000 000 ₽/мес**
- Gross profit = **50 × 140 000 = 7 000 000 ₽/мес**
- Fixed costs = **5 463 000 ₽/мес**
- **EBITDA ≈ 1 537 000 ₽/мес**

### Вывод по Profit Gate
- Условие `EBITDA < 500K/mo achievable even at 50 clients` **не срабатывает**.
- LTV/CAC намного выше **1:1**.
- Следовательно **reject по Profit Gate не нужен**.

---

## 11) Burn-to-breakeven и Cash Runway

### Burn-to-breakeven
Для расчёта беру реалистичную раннюю траекторию:
- acquisition spend: **0,8 млн ₽/мес** в M1-M2, **1,0 млн ₽/мес** в M3-M4, **1,15 млн ₽/мес** в M5-M12;
- gross profit растёт вместе с клиентской базой по 140 тыс. ₽ на клиента.

Грубая оценка cumulative burn до операционного break-even:
- M1-M4: **~10,0 млн ₽** burn
- M5-M8: ещё **~12,2 млн ₽** burn
- M9-M12: ещё **~8,3 млн ₽** burn
- **Итого burn-to-breakeven ≈ 30,5 млн ₽**

### Cash runway
Предполагаю **startup_capital = 35 млн ₽**.

- Средний burn первых 6 месяцев ≈ **4,7 млн ₽/мес**
- При таком burn nominal runway на старте ≈ **7,4 месяца**
- Но за счёт роста выручки cash runway фактически дотягивается до **операционного break-even около M12**
- Запас после выхода в ноль остаётся тонким, поэтому безопаснее поднимать **40+ млн ₽**, если founders не субсидируют продажи собственным трудом

### Sanity check
- Требование из задания `startup_capital_to_bep < 10M₽ для B2B enterprise SaaS — red flag` не нарушено.
- Здесь капитал до устойчивого break-even **~30-35 млн ₽**, что реалистично для sales-heavy B2B security motion.

---

## 12) Итог инвестиционного качества

### Что хорошо
1. **LTV/CAC = 10,6x**
2. **CAC Payback = 4,7 мес**
3. **Contribution Margin = 70%**
4. На **50 клиентах EBITDA > 1,5 млн ₽/мес**

### Что напрягает
1. Модель зависит от **high-touch sales и founder credibility**
2. Break-even только около **40 клиентов**, то есть early burn заметный
3. Категория узкая, demand keyword-led слабый, значит масштабирование хуже, чем у горизонтального SaaS

### Финальный вывод P5
**PASS, но только как niche managed B2B security service с AI-layer.**

Если продукт пытаться продавать как дешёвый bot-first SaaS без людей в контуре, экономика и конверсии почти наверняка развалятся. Если держать фокус на recurring retainer 180-220 тыс. ₽, partner-assisted GTM и upper-SMB с compliance pressure, модель выглядит инвестиционно приемлемой.

---

## Sources
- [T1] `pipeline/cases/virtual-ciso-square-sellers-v2/02-demand.md`
- [T2] ChartMogul, Customer churn rate, accessed 2026-05-11: https://chartmogul.com/saas-metrics/customer-churn/
- [T3] OptiMine / OptiFai churn benchmark page, accessed 2026-05-11: https://www.optimine.com/resources/saas-churn-rate-benchmark
- [T4] HH.ru search, CTO, accessed 2026-05-11: https://hh.ru/search/vacancy?text=CTO
- [T5] HH.ru search, Senior Backend, accessed 2026-05-11: https://hh.ru/search/vacancy?text=Senior+Backend
- [T6] HH.ru article, DevOps-инженер, accessed 2026-05-11: https://hh.ru/article/skills_devops



---

# FILE: 05-critic.md

## SECTION A. PnL 12 месяцев

Кейс: **virtual-ciso-square-sellers-v2**

### A1. Допущения модели
- ARPA / MRR на клиента: **200 000 ₽/мес**.
- COGS на клиента: **60 000 ₽/мес**.
- Gross profit / contribution на клиента: **140 000 ₽/мес**, GM **70,0%**.
- Страховые взносы: **~30% к ФОТ**, уже включены в FOT fully-loaded и fixed cost ramp.
- Fixed costs включают ramp команды + 900 000 ₽ non-FOT fixed costs в месяц.
- НДС 20% актуален при ОСНО; в основном сценарии принята IT-льгота 3% как целевая структура после аккредитации Минцифры, в downside для консерватизма использована УСН 6%.

### A2. Scenario: Base
- New clients plan: 0, 0, 1, 1, 2, 3, 4, 5, 6, 7, 8, 9.
- Churn: **2.0% / мес**.
- Налог для net waterfall: **IT-льгота 3%**.

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| Total clients | 0 | 0 | 1 | 1.98 | 3.94 | 6.86 | 10.72 | 15.51 | 21.20 | 27.78 | 35.22 | 43.52 |
| MRR, ₽ | 0 | 0 | 200 000 | 396 000 | 788 080 | 1 372 318 | 2 144 872 | 3 101 975 | 4 239 935 | 5 555 136 | 7 044 034 | 8 703 153 |
| COGS, ₽ | 0 | 0 | 60 000 | 118 800 | 236 424 | 411 696 | 643 462 | 930 592 | 1 271 981 | 1 666 541 | 2 113 210 | 2 610 946 |
| Gross profit, ₽ | 0 | 0 | 140 000 | 277 200 | 551 656 | 960 623 | 1 501 410 | 2 171 382 | 2 967 955 | 3 888 595 | 4 930 824 | 6 092 207 |
| GM % | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% |
| Fixed costs, ₽ | 2 460 000 | 2 694 000 | 3 149 000 | 3 695 000 | 4 488 000 | 5 138 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 |
| EBITDA, ₽ | -2 460 000 | -2 694 000 | -3 009 000 | -3 417 800 | -3 936 344 | -4 177 377 | -3 961 590 | -3 291 618 | -2 495 045 | -1 574 405 | -532 176 | 629 207 |
| Cash burn, ₽ | 2 460 000 | 2 694 000 | 3 009 000 | 3 417 800 | 3 936 344 | 4 177 377 | 3 961 590 | 3 291 618 | 2 495 045 | 1 574 405 | 532 176 | 0 |
| Cumulative cash, ₽ | -2 460 000 | -5 154 000 | -8 163 000 | -11 580 800 | -15 517 144 | -19 694 521 | -23 656 111 | -26 947 728 | -29 442 774 | -31 017 178 | -31 549 355 | -31 549 355 |

- Break-even по client count: **40 клиентов** при fully-loaded fixed cost **5 463 000 ₽/мес**.
- Break-even по месяцам: **M12**.
- Startup capital to BEP: **31 549 355 ₽**.
- Total clients на M12: **43.52**.

**Waterfall на 1 клиента / месяц**

| Шаг waterfall | ₽/клиент/мес |
|---|---:|
| ARPA | 200 000 |
| Gross profit after COGS | 140 000 |
| Contribution after variable delivery | 140 000 |
| EBITDA after fixed cost allocation | 3 425 |
| Net after tax (IT-льгота 3%) | -2 575 |

### A2. Scenario: Optimistic
- New clients plan: 0, 1, 1, 2, 3, 4, 5, 6, 8, 9, 10, 11.
- Churn: **1.5% / мес**.
- Налог для net waterfall: **IT-льгота 3%**.

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 8 | 9 | 10 | 11 |
| Total clients | 0 | 1 | 1.98 | 3.96 | 6.90 | 10.79 | 15.63 | 21.40 | 29.08 | 37.64 | 47.07 | 57.37 |
| MRR, ₽ | 0 | 200 000 | 397 000 | 791 045 | 1 379 179 | 2 158 492 | 3 126 114 | 4 279 223 | 5 815 034 | 7 527 809 | 9 414 892 | 11 473 668 |
| COGS, ₽ | 0 | 60 000 | 119 100 | 237 314 | 413 754 | 647 547 | 937 834 | 1 283 767 | 1 744 510 | 2 258 343 | 2 824 467 | 3 442 100 |
| Gross profit, ₽ | 0 | 140 000 | 277 900 | 553 732 | 965 426 | 1 510 944 | 2 188 280 | 2 995 456 | 4 070 524 | 5 269 466 | 6 590 424 | 8 031 568 |
| GM % | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% |
| Fixed costs, ₽ | 2 460 000 | 2 694 000 | 3 149 000 | 3 695 000 | 4 488 000 | 5 138 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 |
| EBITDA, ₽ | -2 460 000 | -2 554 000 | -2 871 100 | -3 141 268 | -3 522 574 | -3 627 056 | -3 274 720 | -2 467 544 | -1 392 476 | -193 534 | 1 127 424 | 2 568 568 |
| Cash burn, ₽ | 2 460 000 | 2 554 000 | 2 871 100 | 3 141 268 | 3 522 574 | 3 627 056 | 3 274 720 | 2 467 544 | 1 392 476 | 193 534 | 0 | 0 |
| Cumulative cash, ₽ | -2 460 000 | -5 014 000 | -7 885 100 | -11 026 369 | -14 548 943 | -18 175 999 | -21 450 719 | -23 918 263 | -25 310 739 | -25 504 273 | -25 504 273 | -25 504 273 |

- Break-even по client count: **40 клиентов** при fully-loaded fixed cost **5 463 000 ₽/мес**.
- Break-even по месяцам: **M11**.
- Startup capital to BEP: **25 504 273 ₽**.
- Total clients на M12: **57.37**.

**Waterfall на 1 клиента / месяц**

| Шаг waterfall | ₽/клиент/мес |
|---|---:|
| ARPA | 200 000 |
| Gross profit after COGS | 140 000 |
| Contribution after variable delivery | 140 000 |
| EBITDA after fixed cost allocation | 3 425 |
| Net after tax (IT-льгота 3%) | -2 575 |

### A2. Scenario: Pessimistic
- New clients plan: 0, 0, 0, 1, 1, 2, 3, 4, 4, 5, 6, 7.
- Churn: **3.0% / мес**.
- Налог для net waterfall: **УСН 6%**.

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 4 | 5 | 6 | 7 |
| Total clients | 0 | 0 | 0 | 1 | 1.97 | 3.91 | 6.79 | 10.59 | 14.27 | 18.84 | 24.28 | 30.55 |
| MRR, ₽ | 0 | 0 | 0 | 200 000 | 394 000 | 782 180 | 1 358 715 | 2 117 953 | 2 854 415 | 3 768 782 | 4 855 719 | 6 110 047 |
| COGS, ₽ | 0 | 0 | 0 | 60 000 | 118 200 | 234 654 | 407 614 | 635 386 | 856 324 | 1 130 635 | 1 456 716 | 1 833 014 |
| Gross profit, ₽ | 0 | 0 | 0 | 140 000 | 275 800 | 547 526 | 951 100 | 1 482 567 | 1 998 090 | 2 638 147 | 3 399 003 | 4 277 033 |
| GM % | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% | 70.0% |
| Fixed costs, ₽ | 2 460 000 | 2 694 000 | 3 149 000 | 3 695 000 | 4 488 000 | 5 138 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 | 5 463 000 |
| EBITDA, ₽ | -2 460 000 | -2 694 000 | -3 149 000 | -3 555 000 | -4 212 200 | -4 590 474 | -4 511 900 | -3 980 433 | -3 464 910 | -2 824 853 | -2 063 997 | -1 185 967 |
| Cash burn, ₽ | 2 460 000 | 2 694 000 | 3 149 000 | 3 555 000 | 4 212 200 | 4 590 474 | 4 511 900 | 3 980 433 | 3 464 910 | 2 824 853 | 2 063 997 | 1 185 967 |
| Cumulative cash, ₽ | -2 460 000 | -5 154 000 | -8 303 000 | -11 858 000 | -16 070 200 | -20 660 674 | -25 172 574 | -29 153 007 | -32 617 916 | -35 442 769 | -37 506 766 | -38 692 733 |

- Break-even по client count: **40 клиентов** при fully-loaded fixed cost **5 463 000 ₽/мес**.
- Break-even по месяцам: **в пределах M1-M12 не достигнут**.
- Startup capital to BEP: **38 692 733 ₽**.
- Total clients на M12: **30.55**.

**Waterfall на 1 клиента / месяц**

| Шаг waterfall | ₽/клиент/мес |
|---|---:|
| ARPA | 200 000 |
| Gross profit after COGS | 140 000 |
| Contribution after variable delivery | 140 000 |
| EBITDA after fixed cost allocation | 3 425 |
| Net after tax (УСН 6%) | -8 575 |

### A3. Налоговая модель
| Режим | Налоговая база | Эффект на unit economics | Когда применять |
|---|---|---|---|
| УСН 6% | 6% с выручки | минус **12 000 ₽** на клиента в месяц при ARPA 200 000 ₽ | fallback, если нет IT-аккредитации |
| IT-льгота 3% | 3% с выручки | минус **6 000 ₽** на клиента в месяц | целевой режим при аккредитации Минцифры и соблюдении критериев |
| ОСНО 20% + НДС 20% | налог на прибыль + администрирование НДС | самый тяжёлый режим для cash conversion; требует либо higher ARPA, либо lower CAC/fixed base | если льготы/УСН недоступны |

- В модели выше страховые взносы **~30% к ФОТ** уже включены в fixed costs.
- НДС 20% при ОСНО не заложен в PnL-сценарии как базовый кейс, но должен учитываться в cash planning и договорах с клиентами.

### A4. Итог по PnL
- **Base:** выход в EBITDA-plus в **M12**, peak startup capital до BEP около **31,5 млн ₽**.
- **Optimistic:** выход в EBITDA-plus в **M11**, startup capital до BEP около **25,5 млн ₽**.
- **Pessimistic:** за 12 месяцев не выходит в break-even, потребность в капитале около **38,7 млн ₽** только на текущий горизонт.

<!-- P6A-DONE -->

## SECTION B. Finance risk + competitor deep-dive

### B1. Sensitivity analysis, EBITDA через 12 месяцев

Предположение для sensitivity: базовый sales-plan и fixed-cost ramp из SECTION A сохраняются; при **CAC x2** считаю, что для удержания того же темпа new logos нужен удвоенный acquisition spend, то есть дополнительная нагрузка **+1 325 500 ₽/мес** против базового fully-loaded CAC budget из P5. [T1]

| Сценарий | Ключевое изменение | Clients @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | как в SECTION A | 43.52 | 629 207 | формально выходит в плюс только к M12 |
| Sens1 | CAC x2 | 43.52 | -696 293 | EBITDA снова уходит в минус, потому что GTM становится слишком дорогим [T1] |
| Sens2 | Churn x2, с 2% до 4%/мес | 41.21 | 306 810 | база ещё жива, но запас прочности почти исчезает [T1] |
| Sens3 | Price -30%, ARPA 140k ₽ | 43.52 | -1 981 739 | pricing compression ломает модель при текущем cost base [T1][T2] |

Вывод: главная хрупкость не в delivery COGS, а в **ценообразовании и стоимости привлечения**. Даже умеренное давление на price или GTM быстро возвращает компанию в отрицательный EBITDA.

### B2. Monte Carlo Lite, confidence intervals

Использую упрощённую версию вместо 1000 прогонов: **9-комбинационную решётку** на горизонте M24. База M13-M24: команда уже собрана, fixed cost floor = **5 463 000 ₽/мес**, new logos масштабируются вокруг base run-rate, а conversion и time-to-hire выступают вторичными модификаторами sales velocity и cash runway. Источники чисел ниже опираются на P5/P4 и конкурентные бенчмарки. [T1][T2][T3][T4][T5]

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 560 000 | 663 000 | 1 326 000 | P5 blended CAC и stress-case CAC x2 [T1] |
| Monthly churn % | 1.5% | 2.0% | 4.0% | P5 benchmark + stress-case churn x2 [T1] |
| ARPU ₽/мес | 140 000 | 200 000 | 260 000 | P4 WTP window 120k-300k ₽ и base ARPA 200k ₽ [T1][T2] |
| Conversion rate lead→paid % | 1.5% | 2.5% | 4.0% | вывод из blended funnel conversion по каналам [T1] |
| Time-to-hire месяцев (среднее) | 1.0 | 1.8 | 3.0 | P5 team hiring plan [T1] |

#### p10 / p50 / p90 summary

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | -480 000 | 12 900 000 | 33 600 000 | 34 080 000 |
| CAC payback (мес) | 16.6 | 4.7 | 2.8 | 13.8 |
| LTV/CAC | 1.8 | 10.6 | 21.7 | 19.9 |
| Cash runway (мес) | 8 | 13 | 18 | 10 |

Как читать результат:
- **p10 EBITDA < 0**. Правило insolvency risk срабатывает, значит kill criterion #1 обязателен.
- **p50 EBITDA > 500k ₽/мес**, то есть median-case формально проходит EBITDA Gate.
- Дисперсия между хвостами очень широкая; при переходе от p10 к p90 модель меняется не на проценты, а на порядок. Это повод **снизить confidence score** даже при приемлемом median.
- **Range width по LTV/CAC = 19.9**, что сильно выше порога 8. Следовательно, модель хрупкая одновременно по **pricing, churn и CAC**.

### B3. Competitor deep-dive

Сравниваю не только чистые vCISO-платформы, но и ближайшие substitutes, потому что в РФ покупатель чаще выбирает между **fractional CISO, compliance automation, MSSP и outsourced security leadership**, а не между двумя одинаковыми AI-продуктами.

#### Западные конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Cynomi** | самый близкий direct competitor: AI-driven vCISO platform, 100% channel-focused, hundreds of partners, заточен под MSP/MSSP scale-up [T3] | сильная зависимость от партнёрского канала, меньше brand pull со стороны end-customer, limited fit под РФ-regulatory stack | **5-8%** в узком global vCISO-enablement niche, по сути category leader в своём микросегменте, но не mass-market GRC [T3] | локализация под 152-ФЗ/115-ФЗ, русскоязычный delivery layer, дешевле human-assisted onboarding для РФ SMB |
| **Vanta** | сильный trust/compliance brand, тысячи клиентов, развитая partner ecosystem, отдельный слой для vCISO/service partners [T4] | не native-vCISO, а прежде всего compliance platform; для service-heavy SMB security нужен доп. human layer | **20-25%** в broader startup compliance automation category; в pure vCISO segment доля ниже, но mindshare очень высокий [T4] | мы можем продавать не compliance-first, а security-operations + board-reporting + outsourced leadership в одном пакете |
| **Drata** | большой партнёрский канал, MSSP-friendly motion, сильная continuous compliance automation, good US mid-market reach [T5] | похожая слабость: это trust-management core, а не полноценный outsourced CISO motion; дорогой стек для РФ после санкционного фрикциона | **15-20%** в compliance automation / partner-led segment, но ниже Vanta по category pull [T5] | лучше fit для РФ data residency, меньше санкционного риска, можно bundle с local consulting и evidence workflows |

#### Российские конкуренты и substitutes

| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **BI.ZONE vCISO** | прямой сигнал рынка: у BI.ZONE уже есть отдельный vCISO service; сильный enterprise brand, доступ к large-account pipeline, глубокая security expertise [T6][T9] | enterprise-first DNA, дорогой delivery, для upper-SMB может быть тяжёлым и избыточным | **8-12%** в RU outsourced security leadership / high-end advisory niche; выше в enterprise, ниже в SMB | можем быть быстрее, дешевле и более productized для SMB/mid-market, без enterprise overhead |
| **Солар / Ростелеком-Солар** | крупная платформа managed security services, несколько сотен клиентов, 40% SMB в одном из ранних disclosure, сильный brand и cross-sell через Ростелеком [T7][T10] | гос/крупнокорпоративное наследие, риск медленного цикла внедрения, perception как heavy integrator | **15-20%** в RU MSS/security-services layer; в SMB-managed segment один из самых сильных substitutes | у нас может быть более узкий vCISO playbook, faster onboarding и лучшая unit-economics на клиентах 100k-250k MRR |
| **Positive Technologies** | огромный brand, 2 900+ организаций worldwide, сильные позиции в VM/WAF/appsec, масштаб продаж и доверие рынка [T8][T11] | сильнее в product/platform security, чем в fractional-CISO recurring advisory; для SMB часто overkill по бюджету | **20-25%** в broader RU cyber market по mindshare в commercial enterprise, но существенно меньше в direct vCISO-service niche | мы конкурируем не лоб в лоб по platform depth, а по service outcome и lower entry ticket |
| **Swordfish Security / похожие boutique security integrators** | сильная DevSecOps и secure SDLC экспертиза, 100-200 сотрудников, понятный consulting credibility [T12] | менее масштабный distribution, уже crowded в консалтинге, слабее recurring board-level ownership | **2-4%** в нише boutique security advisory / appsec services | наша advantage в recurring governance layer, AI-assisted reporting и channel resale motion |

Итог по competitive pressure:
- На Западе рынок уже уходит в **platform-assisted vCISO**.
- В РФ рынок пока больше похож на **managed services + консалтинг + compliance substitutes**.
- Значит окно есть, но moat должен строиться не вокруг слова `vCISO`, а вокруг **быстрого time-to-value, локальной регуляторики, partner resale и low-friction recurring delivery**.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Founder/CEO bottleneck в enterprise selling и partner activation | high | high | >50% SQL требуют личного участия фаундера | стандартизировать sales playbook, нанять AE earlier, партнёрский enablement kit |
| 2 | Operational | Качество delivery проседает при росте клиентов быстрее найма CSM/analyst | med | high | SLA breaches, delayed board reports, NPS < 30 | лимиты на book of business, templatized delivery, analyst tooling |
| 3 | Operational | Зависимость от внешних LLM API, рост latency или цен | med | high | unit cost/token растёт 20%+ два месяца подряд | multi-model stack, local fallback, prompt caching, human-safe mode |
| 4 | Market | Слабый category demand по exact keyword `vCISO` в РФ | high | med | низкий inbound, CAC из outbound/partner выше плана | продавать через pain-based JTBD: 152-ФЗ, аудит, vendor questionnaire, ransomware readiness |
| 5 | Market | Price compression со стороны MSSP и аутсорс-ИБ интеграторов | high | high | win-rate падает при price objection, discounting >20% | пакетировать outcome, ввести tiering, upsell compliance/reporting layer |
| 6 | Market | Крупные игроки копируют offer и используют existing client base | med | high | потеря тендеров/сделок против BI.ZONE, Solar, PT | нишевание на upper-SMB, white-label channel deals, speed as weapon |
| 7 | Regulatory | Ошибка в трактовке 152-ФЗ, локализации ПДн или data residency | med | high | security/legal review растёт, клиенты просят on-prem или RU-only | data mapping, RU hosting by default, DPA templates, privacy counsel |
| 8 | Regulatory | Усиление требований 115-ФЗ/комплаенса у фин/финтех клиентов | med | med | сделки в fintech зависают на legal/compliance stage | vertical-specific policy packs, external legal partners |
| 9 | Regulatory | Санкции ограничивают доступ к западным SaaS, security tools и billing rails | high | high | vendor offboarding notices, отказ в оплате/renewal | импортозамещённый стек, резервные поставщики, локальное развёртывание |
| 10 | Financial | Cash runway короче плана из-за delayed ramp и высокого CAC | high | high | cash < 9 месяцев, burn > 3 млн ₽/мес 2 квартала подряд | freeze hiring, cut paid channels, shift to partner-led GTM |
| 11 | Financial | Рост USD/RUB повышает стоимость облака, LLM и security tools | med | med | gross margin падает ниже 65% | рублёвые контракты, annual prepay, repricing clauses |
| 12 | Financial | Инфляция и рост зарплат ИБ/ML кадров | high | med | offer acceptance rate падает, hiring cycle > 3 мес | remote hiring, variable comp, tighter role scope |
| 13 | Black swan | Резкое ужесточение санкций или военная эскалация бьёт по клиентским бюджетам | med | high | массовые budget freeze, отмены проектов | фокус на must-have security spend, short payback positioning |
| 14 | Black swan | Частичное или полное отключение внешних LLM providers | med | high | отказ API, latency spikes, юридические ограничения | локальные модели, rule-based fallback, vendor diversification |

### B5. Kill conditions через 6 месяцев

1. **Median gate fail:** если rolling **p50 EBITDA forecast на M24 < 500 000 ₽/мес**, продолжать нельзя, потому что модель не проходит даже median-case gate.
2. **GTM fail:** если **blended CAC > 1 000 000 ₽** два месяца подряд **или CAC payback > 12 мес**, значит рост покупается слишком дорогой ценой.
3. **Retention/pricing fail:** если **monthly churn > 4%** два квартала подряд **или средний реализованный ARPA < 150 000 ₽/мес**, продукт превращается в low-margin security outsourcing.

### B6. Итог SECTION B

Кейс остаётся **жизнеспособным, но execution-sensitive**. Base-case показывает, что бизнес можно довести до двузначного EBITDA на горизонте M24, но хвосты распределения слишком широкие: при негативной комбинации **CAC, churn и price** компания быстро теряет инвестиционную привлекательность. Для инвесткомитета это не `easy yes`, а **conditional proceed** только при жёстком контроле pricing discipline, partner-led distribution и локального regulatory fit.

## Sources, SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/virtual-ciso-square-sellers-v2/04-economics.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/virtual-ciso-square-sellers-v2/02-demand.md
- [T3] Cynomi about + platform pages: https://cynomi.com/about/ ; https://cynomi.com/vciso-platform/ ; https://cynomi.com/platform/ciso-intelligence/
- [T4] Vanta partner ecosystem + service provider materials: https://www.vanta.com/partners/partner-program ; https://www.vanta.com/partners/service-providers ; https://www.vanta.com/partners/find-a-partner
- [T5] Drata partner / MSSP materials: https://drata.com/partners ; https://drata.com/partners/channel ; https://help.drata.com/en/articles/10771929-working-with-an-mssp-managed-security-service-provider
- [T6] BI.ZONE vCISO on Habr: https://habr.com/ru/news/723188/
- [T7] Ростелеком-Солар / Solar MSS on Habr and vc.ru: https://habr.com/ru/news/676464/ ; https://habr.com/ru/companies/solarsecurity/news/797299/ ; https://vc.ru/services/74717-dochka-sberbanka-nachnet-predostavlyat-servisy-v-sfere-kiberbezopasnosti-biznesu ; https://vc.ru/services/831303-rostelekom-solar-razdelit-biznes-na-dve-struktury-s-raznymi-brendami-chtoby-uiti-ot-obraza-goskompanii
- [T8] Positive Technologies company profile on Habr: https://habr.com/en/companies/pt/profile/
- [T9] BI.Zone market context on vc.ru: https://vc.ru/services/74717-dochka-sberbanka-nachnet-predostavlyat-servisy-v-sfere-kiberbezopasnosti-biznesu
- [T10] Rusprofile / Ростелеком corporate profile: https://www.rusprofile.ru/id/476492
- [T11] Positive Technologies market-share discussion on vc.ru: https://vc.ru/money/330250-obzor-kompanii-positive-technologies
- [T12] Swordfish Security profile on Habr: https://habr.com/en/companies/swordfish_security/profile/

<!-- P6B-DONE -->



---

# FILE: 06-verdict.md

[AI-SERVICES] Virtual CISO для SMB через партнёрские каналы — NEAR-PASS: 67/100 | EBITDA base=629К₽/мес через 12 мес | LTV/CAC=10,6x | Ключевое преимущество: partner-led recurring security retainer | Главный риск: weak moat и price compression.

# 06-verdict

sector: AI-SERVICES

## Итог
- **Финальный статус:** NEAR-PASS
- **Normalized score:** **67/100**
- **Комитетное решение:** кейс **не проходит в approve**, но остаётся в корзине **near-pass** как service-heavy security business с рабочей unit economics и недостаточным запасом прочности по moat, demand quality и GTM-защите.
- **Пороговое правило:** хотя `company_ebitda_rub_month` в base достигает **629 207 ₽/мес** к **M12**, итоговый score < 70, поэтому кейс уходит в `rejected/` как NEAR-PASS.

## Delta vs previous
- Исходный triage считал сигнал supporting/duplicate для agency-pattern.
- Повторный полный пайплайн показал, что standalone бизнес-модель **жизнеспособна**, но не investment-grade: экономика и EBITDA gate проходят, а спрос, moat и защита pricing нет.
- Главный апгрейд против старого взгляда: кейс не «нулевой», а **условно инвестируемый при жёстком execution-control**.

## Оценка
Source tier balance: T1=4, T2=12, T3=2, weighted=1.78. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «LTV/CAC = 10,6x», «CAC Payback = 4,7 месяца», «Contribution Margin = 70,0%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В base «EBITDA @M12 = 629 207 ₽/мес», break-even достигается в M12. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | «Demand verdict: MEDIUM-LOW», exact keyword demand LOW, но HH по adjacent боли = 79 и SAM = 2,45 млрд ₽. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | Рынок crowded substitutes, а в 05-critic прямо указано: «moat должен строиться не вокруг слова vCISO». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | Риски явные, но управляемые: «execution-sensitive», при этом full team = 9 и hire-plan без red flag. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | Есть partner-led motion, «4–6 партнёров реалистично», CAC 663k ₽ и payback 4,7 мес укладываются. |


**Сумма raw:** 100/150  
**Normalized score:** `round((100 * 100) / 150) = 67/100`

## 7-factor moat framework

| Фактор | Score 0-3 | Почему |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | Есть артефакты, playbooks и governance-ритм, но интеграционная глубина средняя. |
| Scale economies | 1 | COGS снижается умеренно за счёт шаблонов и AI-layer, но delivery остаётся human-assisted. |
| Proprietary data / model advantage | 1 | Уникальный датасет не доказан, модель скорее process/playbook-driven. |
| Regulatory moat | 1 | Локальная 152-ФЗ экспертиза помогает, но это не hard moat. |
| Brand / distribution | 2 | Partner resale через MSSP/MSP реалистичен, но собственного brand pull пока нет. |
| Embedded workflow | 2 | Ежемесячный board-style governance и vendor questionnaires встраиваются в процесс клиента. |


**Moat score = round((9 * 25) / 21) = 11/25**

Вывод по moat: moat **слабее среднего**. Он держится на локальном delivery + partner channel + workflow embed, но не на data flywheel или hard regulatory barrier.

## Полный бизнес-процесс из 04-economics.md
1. Формирование ICP и target-account list.  
2. Обогащение контактов CTO/CISO/COO.  
3. Outbound sequence, 5-7 касаний.  
4. Qualification call.  
5. Discovery по рискам, compliance и боли.  
6. Подготовка mini-assessment / gap analysis.  
7. Demo + roadmap + ROI discussion.  
8. Коммерческое предложение и scope.  
9. Security / legal review клиента.  
10. Подписание договора.  
11. Выставление счёта.  
12. Оплата первого счёта.  
13. Onboarding, сбор артефактов, policies, access map.  
14. Ежемесячный vCISO-ритм: risk review, board note, vendor support.  
15. Продление / upsell в compliance package.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 7 000 000 ₽ |
| fully_loaded_cac_rub | 663 000 ₽ |
| LTV/CAC | 10,6x |
| CAC payback | 4,7 мес |
| GM | 70,0% |
| contribution_margin_rub_month | 140 000 ₽ |
| company_ebitda_rub_month base | 629 207 ₽/мес |
| Break-even | 40 клиентов |
| months_to_break_even | 12 мес |
| startup_capital_to_bep_rub | 31 549 355 ₽ |
| company_ebitda_potential_rub_month @50 clients | 1 537 000 ₽/мес |

## Команда

| Роль | Кол-во | Fully-loaded FOT / мес |
|---|---:|---:|
| CEO | 1 | 845 000 ₽ |
| CTO / Tech Lead | 1 | 715 000 ₽ |
| Senior Backend | 1 | 546 000 ₽ |
| ML Engineer | 1 | 650 000 ₽ |
| DevOps | 1 | 429 000 ₽ |
| Frontend | 1 | 364 000 ₽ |
| SDR | 1 | 234 000 ₽ |
| AE | 1 | 455 000 ₽ |
| Customer Success | 1 | 325 000 ₽ |
| **Итого** | **9** | **4 563 000 ₽/мес** |

## GTM: 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Selectel | Большая SMB/tech база и высокий security-compliance pain у облачных клиентов. | партнёрство / white-label через B2B-unit | 180 000 ₽/мес |
| Рег.ру | Хостинг и домены для SMB, много клиентов с 152-ФЗ и vendor-security вопросами. | партнёрство + email decision-maker | 170 000 ₽/мес |
| Timeweb Cloud | Cloud-first SMB-аудитория, security governance можно продавать как add-on. | партнёрство / co-sell | 160 000 ₽/мес |
| RuVDS | VDS/VPS база с регулярными вопросами по защите и compliance. | email decision-maker | 150 000 ₽/мес |
| Serverspace | Dev teams и SMB, которым нужен fractional security owner вместо full-time CISO. | партнёрство / конференция | 160 000 ₽/мес |
| FirstVDS | SMB-хостинг с повторяемой data-security болью. | партнёрство / outbound | 140 000 ₽/мес |
| SpaceWeb | Широкая локальная веб/SMB база, где security buyer ещё не инсорснут. | vc.ru ad + email | 140 000 ₽/мес |
| M1Cloud | Managed cloud play хорошо сочетается с vCISO-retainer. | партнёрство / co-sell | 180 000 ₽/мес |
| ITGLOBAL.COM | Есть managed-services motion и enterprise-to-upper-SMB distribution. | партнёрство / direct outreach | 200 000 ₽/мес |
| beeline cloud / B2B cloud unit | Канал к upper-SMB с уже существующим trust layer и recurring-billing. | партнёрство / exec intro | 200 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Weak moat + price compression | Высокая | Высокий | 05-critic прямо показывает, что при `Price -30%` EBITDA @M12 падает до `-1 981 739 ₽`. |
| GTM cost inflation | Высокая | Высокий | При `CAC x2` модель уходит в `-696 293 ₽/мес`, то есть capital efficiency быстро ломается. |
| Negative downside scenario | Средняя | Высокий | Monte Carlo: `p10 EBITDA @M24 = -480 000 ₽/мес`, значит downside всё ещё ведёт к отрицательному company-level outcome. |

## Почему не APPROVED
1. **Спрос есть, но он adjacent, а не category-led.** Exact keyword demand по `virtual CISO` слабый, поэтому повторяемый inbound moat не доказан.  
2. **Moat слабый.** Нет network effects, нет data moat, нет сильного regulatory lock-in.  
3. **Pricing power хрупкая.** 30% discount ломает модель уже в base.  
4. **Распределение исходов широкое.** p10 EBITDA в минусе даже на горизонте M24.

## LTV Upside Calculator
Чтобы кейс вернулся из REJECTED/NEAR-PASS в approve-review, нужно доказать одновременно:
- поднять **ARPA до 230-260 тыс. ₽/мес** через packaged compliance + board reporting;
- удержать **monthly churn ≤ 1,5%**;
- держать **fully-loaded CAC ≤ 600 тыс. ₽** через партнёрский канал;
- довести **moat score минимум до 14/25** через workflow embed, proprietary templates/datasets и resale exclusivity.

### Сценарии апсайда
| Сценарий | Что меняется | Эффект |
|---|---|---|
| Base now | ARPA 200k, churn 2,0%, CAC 663k | LTV/CAC 10,6x, score 67/100 |
| Better retention | churn 1,5% | LTV ≈ 9,33 млн ₽, LTV/CAC ≈ 14,1x |
| Better pricing | ARPA 230k при том же COGS | gross profit 170k ₽/мес, payback ≈ 3,9 мес |
| Better channel mix | CAC 550-600k ₽ | выше margin of safety, меньше burn to scale |

## Финальный вердикт
**NEAR-PASS / REJECTED.**

Это хороший service business, но пока не investment-grade committee case. Экономика клиента сильная, company EBITDA gate достижим, однако итоговая конструкция слишком зависима от founder credibility, partner execution и удержания premium pricing. Возвращать кейс в approve-review имеет смысл только после 3-5 платящих channel-партнёров, churn ≤ 1,5% и доказанного ARPA выше 220 тыс. ₽/мес.



---

# FILE: 07-score-trajectory.md

## 2026-04-24 — P4 Demand Validation
- Stage: P4
- Score change: `new -> Demand: 3/5`
- Summary: keyword demand по `virtual CISO`/`vCISO` в РФ слабый, но adjacent demand по аутсорсингу ИБ и managed security заметный; recurring channel/direct модели проходят Profit Gate, project-only модель не проходит.
- Decision impact: `продолжать дальше по пайплайну, но держать кейс в niche/service-heavy bucket`
- Evidence: multi-demand endpoint = LOW по exact keywords; TAM РФ ~8.1 млрд ₽, preferred SAM ~2.45 млрд ₽, preferred SOM Y1 ~34.6 млн ₽.

## 2026-05-11 — P5 Unit Economics
- Stage: P5
- Score change: `Demand: 3/5 -> Economics: 4/5`
- Summary: recurring model virtual CISO по 200k ₽ MRR на клиента сходится только как high-touch managed service; blended fully-loaded CAC = 663k ₽, gross margin = 70%, churn = 2.0%/мес, LTV/CAC = 10.6x, CAC payback = 4.7 мес.
- Decision impact: `продолжать дальше по пайплайну; reject по Profit Gate не нужен`
- Evidence: EBITDA на 50 клиентах ≈ 1.54 млн ₽/мес; break-even ≈ 40 клиентов; burn-to-breakeven ≈ 30.5 млн ₽; startup capital realism = 35 млн ₽.

## 2026-05-12 — P7 Critic & Verdict
- Stage: P7
- Score change: `Economics: 4/5 -> Verdict: 67/100 (NEAR-PASS)`
- Summary: сильная unit economics и достижимый EBITDA gate не компенсируют weak moat, слабый exact-demand и высокую execution sensitivity.
- Decision impact: `переместить в rejected как NEAR-PASS; возвращать только после доказанного partner-led scale и снижения CAC/price-risk`
- Evidence: tier balance T1=4, T2=12, T3=2 (weighted 1.78, penalty -5 к Market+Demand); EBITDA base = 629k ₽/мес к M12; p10 EBITDA @M24 = -480k ₽/мес.
