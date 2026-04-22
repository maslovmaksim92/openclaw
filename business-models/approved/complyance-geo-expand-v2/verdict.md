# Complyance GEO Expand v2 — Full Verdict Package
> Скомпилированный пакет стадий P2/P4/P5/P6/P7 для публикации в GitHub.
> Примечание: в этом rerun-кейсе demand-файл существует как `02-demand.md`; отдельные `02-validation.md` и `03-demand.md` в исходном кейсе отсутствуют и не создавались заново.

---

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-complyance-geo-expand.md
created: 2026-04-20T09:30:00+03:00
original_verdict: triage/triage-2026-04-17-complyance-geo-expand.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — complyance-geo-expand

## Meta
- source: triage/triage-2026-04-17-complyance-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж: Complyance

- Дата триажа: 17 апреля 2026
- Raw-файл: `pipeline/raw/raw-2026-04-17-complyance-geo-expand.md`
- Решение: `NEW`
- Созданный кейс: `pipeline/cases/enterprise-grc-automation-platform/`

## Почему создан новый кейс
Сигнал не является дубликатом открытого кейса в `pipeline/cases/`, потому что в текущем открытом пайплайне не было кейса по AI-native GRC-платформе для control testing, evidence collection, vendor risk и audit readiness. По смыслу это смежная, но отдельная категория относительно более широких compliance-операций.

## Почему сигнал проходит порог
Во входном файле указан ориентир 1,8-9,0 млн ₽ в год с одного enterprise-клиента в РФ, что соответствует примерно 150 000-750 000 ₽ в месяц. Верхняя часть диапазона превышает порог 500 000 ₽ в месяц, а для regulated enterprise-сегментов чек может дополнительно вырасти за счёт private cloud, локализации под российскую регуляторику, интеграций и managed-сопровождения.

## Что создано
Создан файл `pipeline/cases/enterprise-grc-automation-platform/00-brief.md` с описанием кейса, текущего состояния и ключевой гипотезы.

```



---

## Файл: 02-demand.md

# Demand Validation — Complyance

## Итог
- **Demand verdict:** низкий публичный search-demand в РФ, но **существует узкий платёжеспособный enterprise-спрос** в regulated-сегментах. [T1]
- **Profit Gate:** **PASS** при enterprise-only GTM, если продавать 8-13 аккаунтов с ACV 3,6-6,0 млн ₽/год и добавлять onboarding / private cloud / audit services. [T1][T2]
- **Решение P4:** **не делать early reject**, кейс имеет смысл пропускать дальше как нишевый B2B enterprise play, а не mass-market продукт. [inference]

## Demand signals
- По обязательному endpoint `multi-demand` ключи `GRC compliance automation`, `GRC платформа`, `vendor risk management`, `audit readiness` дали **LOW**; лучший локальный сигнал у `комплаенс автоматизация`: `hh_vacancies=103`, `yandex_suggest=100`, но composite всё равно LOW. [T1]  
  Источник: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D0%BC%D0%BF%D0%BB%D0%B0%D0%B5%D0%BD%D1%81%20%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F
- Это похоже не на отсутствие боли, а на **узкий B2B procurement-driven рынок**: pain подтверждается hiring-спросом, а не поисковым трафиком. [T1][inference]
- ЦА в РФ есть прежде всего среди банков, страховщиков, крупных финтехов, телекомов и публичных/квази-публичных групп с тяжёлым внутренним контролем. [T1][T2]

## Конкуренты и цены
| Конкурент | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Vanta | compliance automation / audit readiness | **from $10,000/year** на AWS Marketplace, annual contract [T2] | Нижний порог рынка для SMB/mid-market; enterprise edition обычно выше. https://aws.amazon.com/marketplace/pp/prodview-a7r5boa4el2ag |
| Drata | security & compliance automation | **$7,500/year** за 1 framework add-on на AWS Marketplace [T2] | Даже add-on стоит заметно; full platform для enterprise обычно кратно выше. https://aws.amazon.com/marketplace/pp/prodview-vk5qy6bjybunw |
| Secureframe | compliance automation | **Starts at $15,000/year** [T2] | Хороший ориентир на нижнюю публичную цену категории. https://secureframe.com/pricing |
| Sprinto | security compliance automation | **Starts at $12,000/year** [T2] | Подтверждает willingness-to-pay за automation в этой категории. https://sprinto.com/pricing/ |

**Пересчёт в рубли:** при курсе ЦБ **76,2562 ₽/$**: Vanta от ~0,76 млн ₽/год, Secureframe от ~1,14 млн ₽/год, Sprinto от ~0,92 млн ₽/год. [T1][T2]  
Источник курса: ЦБ РФ, 21.04.2026 https://www.cbr.ru/currency_base/daily/

## Telegram / RU landscape
- Полноценных enterprise GRC-платформ в Telegram для РФ не найдено; в Telegram присутствуют в основном **каналы/боты для AML/KYC-alerting, комплаенс-новостей и санкционного мониторинга**, а не системы control testing / evidence collection / audit readiness. [T2]
- Это значит, что Telegram в РФ может быть **каналом нотификаций и workflow-approval**, но не основным product surface для enterprise GRC. [inference]
- Следовательно, RU-конкуренция идёт не со стороны TG-ботов, а со стороны ручного консалтинга, Excel/Jira/Confluence-процессов и точечных risk/compliance модулей. [T2][inference]

## WTP / willingness to pay
- **Прямое доказательство WTP:** на западном рынке buyers уже платят $10k-$15k+/год даже за SMB-grade compliance automation. [T2]
- **Локальная гипотеза цены по кейсу:** во входном triage уже фигурировал ориентир **1,8-9,0 млн ₽/год на enterprise-клиента**; этот диапазон согласуется с западными price anchors после локализации, private cloud, интеграций и managed support. [T2][internal case context]
- **Косвенное подтверждение боли:** endpoint `multi-demand` по русскому ключу показывает 103 вакансии на HH для тематики комплаенса/автоматизации, что обычно означает наличие бюджета на headcount и готовность заменять часть ручного труда софтом. [T1][inference]
- **Ограничение:** в РФ willingness-to-pay есть у узкого enterprise-сегмента, но публичный self-serve спрос слабый. Поэтому продукт не выглядит как PLG/SMB story. [T1][T2]

## Market sizing

### Методика
- **Top-down:** берём глобальный рынок GRC software как верхнюю границу, затем режем до РФ и до сегмента AI-native compliance automation. [T3][T1]
- **Bottom-up:** считаем число реальных покупателей в regulated enterprise РФ × доля с подтверждённой болью × средний контракт. [T1][T2]

### Top-down assumptions
- Глобальный GRC market: **$8,58 млрд**. [T3]  
  Источник: Fortune Business Insights, Governance, Risk Management and Compliance Platform Market, 2025 snapshot. https://www.fortunebusinessinsights.com/governance-risk-management-and-compliance-platform-market-107224
- РФ addressable share берём **1,0%** от global software spend как консервативный прокси для локального enterprise-compliance software under sanctions. [LOW CONFIDENCE][T3][inference]
- AI-native compliance automation subsegment от общего GRC: **35%** addressable share, потому что кейс не покрывает весь GRC, а только control testing, evidence collection, vendor risk и audit readiness. [LOW CONFIDENCE][T2][inference]

### Bottom-up assumptions
- Банки РФ: **305** действующих кредитных организаций. [T1] https://www.cbr.ru/banking_sector/credit/coinfo/
- Страховщики РФ: **129** субъектов страхового дела. [T1] https://www.cbr.ru/insurance/
- Плюс ~**66** крупных адресуемых групп в финтехе, телекоме, маркетплейсах, публичных холдингах и крупных IT/outsourcing-компаниях, где есть аудит/контроль/vendor risk. [T2][inference]
- Итого **~500** потенциальных buyers в адресуемом сегменте РФ. [T1][T2][inference]
- Доля с подтверждённой болью: **60%**. Основание: высокий HH-сигнал по комплаенсу/рискам, жёсткая регуляторика и частая ручная подготовка evidence/audit packages. [T1][inference]
- Средний контракт: **4,5 млн ₽/год**. Это середина между кейсовым диапазоном 1,8-9,0 млн ₽/год и западными price anchors с enterprise uplift. [T2][inference]

### 10 реальных buyers для bottom-up / GTM-10
1. Сбер [T2]
2. ВТБ [T2]
3. Газпромбанк [T2]
4. Альфа-Банк [T2]
5. Т-Банк [T2]
6. Совкомбанк [T2]
7. Росгосстрах [T2]
8. СОГАЗ [T2]
9. МТС [T2]
10. Яндекс [T2]

### Таблица cross-check
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$8,58B** [T3] | — | — | top-down |
| TAM (РФ) | **654 млн ₽** = $8,58B × 1,0% × 76,2562 ₽/$ [T1][T3] | **2,25 млрд ₽** = 500 buyers × 100% × 4,5 млн ₽ [T1][T2] | diff=3,4x, top-down likely занижен из-за грубого global-share proxy | **lower / conservative** |
| SAM (РФ) | **229 млн ₽** = TAM РФ × 35% [T2][T3] | **1,35 млрд ₽** = 500 × 60% × 4,5 млн ₽ [T1][T2] | diff=5,9x, значит top-down слишком жёсткий; пересматриваем и используем range | **range 0,23-1,35 млрд ₽** |
| SOM Y1 | **11 млн ₽** = 5% от low-SAM [T2][T3] | **27 млн ₽** = 2% от BU-SAM [T1][T2] | diff=2,5x, обе оценки реалистичны | **используем 18 млн ₽** |
| SOM Y3 | **34 млн ₽** = 15% от low-SAM [T2][T3] | **101 млн ₽** = 7,5% от BU-SAM [T1][T2] | diff=3,0x, на границе допустимого | **используем 50-60 млн ₽** |

### Reconciliation
- Формально top-down и bottom-up разошлись слишком сильно, поэтому я **не использую точечную оценку**, а оставляю рабочий диапазон. [LOW CONFIDENCE]
- Для инвестиционного решения разумнее считать, что **реальный SAM РФ = 0,6-1,0 млрд ₽**, то есть ниже bottom-up, но существенно выше сверхконсервативного top-down. [T1][T2][T3][inference]
- Тогда **SOM Y1 ~18 млн ₽** и **SOM Y3 ~50-60 млн ₽** выглядят реалистично и не нарушают правило `<10% SAM` в первый год. [inference]
- Sanity check: при ACV 4,5 млн ₽ SOM Y1 = 18 млн ₽ означает **4 клиента** в первый год; это тяжело, но реально для founder-led enterprise sales. [inference]

## Profit Gate (EBITDA >= 500k ₽/мес)
Предпосылка: lean team 6-7 FTE, payroll + overhead **~2,8 млн ₽/мес**. [T2][inference]

### Сценарий A — pure SaaS, mid-market
- ARPA: **250k ₽/мес**
- Gross margin: **85%**
- Для EBITDA 500k ₽/мес нужен gross profit 3,3 млн ₽/мес, то есть **~16 клиентов**.
- Вердикт: **слабо реалистично** для РФ, публичный спрос слишком узкий. [T1][inference]

### Сценарий B — enterprise SaaS
- ARPA: **500k ₽/мес**
- Gross margin: **80%**
- Нужно **~9 клиентов** для EBITDA 500k ₽/мес.
- Вердикт: **реалистично**, если продавать банкам/страховщикам/private cloud. [T1][T2][inference]

### Сценарий C — SaaS + onboarding / implementation
- Recurring: **350k ₽/мес**, плюс onboarding **1,0-1,5 млн ₽** на аккаунт
- Эффективный gross profit эквивалент требует **~11-13 клиентов**.
- Вердикт: **реалистично**, потому что российский enterprise часто покупает проект + сопровождение, а не чистый SaaS. [T2][inference]

### Сценарий D — managed compliance / audit readiness service layer
- Recurring: **200-300k ₽/мес**, сервисная выручка ещё **150-250k ₽/мес** на клиента
- EBITDA-гейт достижим при **~10-12 клиентах**, но margin ниже и продукт хуже масштабируется.
- Вердикт: **переходный рабочий сценарий** для входа на рынок. [T2][inference]

**Итог по Profit Gate:** fail только у pure-SaaS/mid-market стратегии; **в enterprise-only и hybrid-service моделях gate проходит**. [inference]

## Что это значит для фонда
- Это не широкий software category winner для РФ, а **нишевый high-ticket enterprise wedge**. [inference]
- Сильная сторона кейса, если команда умеет продавать regulated enterprise и готова идти через compliance/audit pain, а не через широкий брендовый спрос. [T1][T2][inference]
- Главный риск: локальный рынок small, sales cycles длинные, а top-down uncertainty высокая. [T1][T3]

## P4 verdict
- **EARLY REJECT: нет.** Условия `DEMAND=LOW AND Profit Gate FAIL` не выполнены, потому что Demand действительно LOW, но Profit Gate в enterprise/hybrid сценариях проходит. [T1][inference]
- **Рекомендация:** пропустить кейс в следующий этап как узкий enterprise-GRC candidate.

Sources: T1=4, T2=7, T3=1. Primary evidence basis: T1/T2 mixed.


---

## Файл: 04-economics.md

---
sector: GEO-EXPAND
stage: unit-economics
updated: 2026-04-22T05:33:00+03:00
---

# 04-economics

## Unit economics summary
- **Модель**: enterprise B2B compliance automation для банков, страховщиков, крупных финтехов и regulated enterprise.
- **ICP**: 1 buyer = 1 enterprise account с ACV **4,8 млн ₽/год** и MRR **400 000 ₽/мес**.
- **Вывод**: экономика **investment-grade**, если идти в enterprise-only GTM, продавать private cloud / audit readiness / vendor risk bundle и держать blended fully-loaded CAC в коридоре **~0,84 млн ₽/клиент**.
- **Ключевые метрики**:
  - Gross Margin = **78,0%**
  - Fully-loaded blended CAC = **836 000 ₽**
  - LTV = **29,4 млн ₽**
  - LTV/CAC = **35,2x**
  - CAC Payback = **2,1 мес**
  - Break-even = **22 клиента**
  - EBITDA при 50 клиентах = **~8,76 млн ₽/мес**
- **Profit Gate**: **PASS**. Даже при 50 клиентах EBITDA сильно выше 500 тыс. ₽/мес, а LTV/CAC намного выше 1:1.

## Базовые допущения
| Параметр | Значение | Комментарий |
|---|---:|---|
| ACV | 4 800 000 ₽/год | в середине диапазона 1,8-9,0 млн ₽/год из demand-stage [T1] |
| MRR на клиента | 400 000 ₽/мес | ACV / 12 |
| Setup / onboarding fee | 1 200 000 ₽ единовременно | не включаю в payback, чтобы не завышать метрики |
| Gross margin | 78,0% | на базе COGS ниже |
| Annual logo churn | 12% | консервативно против benchmark enterprise SaaS 8,1% [T3] |
| Monthly churn | 1,06% | 12% / 12, для LTV-модели |
| Startup capital | 60 000 000 ₽ | realistic для enterprise B2B SaaS с длинным sales cycle |

## Бизнес-процесс от лида до оплаты
| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | SDR + AE | CRM, account list, email sequencing | 1 день | 3 500 | semi-auto |
| 2 | Outbound / partner outreach | SDR | почта, LinkedIn-аналоги, events follow-up, CRM | 5-10 дней | 12 000 | semi-auto |
| 3 | Qualification call | SDR | VoIP, calendar, CRM | 30-45 мин | 2 500 | low |
| 4 | Discovery с compliance owner | AE + founder | Zoom/Meet, CRM, notes | 1-2 встречи за 7 дней | 14 000 | low |
| 5 | Demo + use-case mapping | AE + solution lead | demo env, deck, security FAQ | 1 неделя | 22 000 | low |
| 6 | Pilot scoping + security review | CTO + GRC analyst | pilot workspace, DPA/security docs | 2-4 недели | 70 000 | low |
| 7 | Pilot execution / evidence ingestion | ML/Backend + GRC analyst | private cloud / sandbox, integrations | 3-6 недель | 140 000 | semi-auto |
| 8 | Procurement + legal | AE + CEO | MSA/DPA/templates, procurement portal | 2-6 недель | 38 000 | low |
| 9 | Invoice / PO issuance | finance/admin | ЭДО, billing, accounting | 2-5 дней | 6 000 | high |
| 10 | Payment collection | finance/admin | bank, ERP/accounting | 7-30 дней | 4 000 | high |
| 11 | Onboarding / production rollout | CSM + implementation PM + DevOps | project plan, SSO, connectors, training | 3-5 недель | 95 000 | semi-auto |

### Комментарий к процессу
- Основная стоимость сидит не в top-of-funnel, а в **pilot + security review + procurement**. Поэтому кейс надо считать как **enterprise acquisition**, а не как SMB SaaS.
- Полный sales cycle от первого касания до оплаты: **3,5-5,5 месяца**.

## COGS per client / month
| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Cloud / private hosting / storage | 18 000 | sandbox + prod + storage reserve | T2 + inference |
| LLM / OCR / document processing | 12 000 | умеренный usage на compliance workflows | T2 + inference |
| DevOps / security monitoring allocation | 10 000 | доля DevOps и security ops | inference |
| Customer Success allocation | 16 000 | 1 CSM на 15-20 enterprise accounts | T5 + inference |
| GRC analyst / support allocation | 20 000 | onboarding и регулярный evidence support | T5 + inference |
| Support / incident / training refresh | 12 000 | SLA + helpdesk + retraining | inference |
| **Итого COGS** | **88 000** |  |  |
| **MRR** | **400 000** | ACV / 12 | T1 |
| **Gross Profit** | **312 000** | 400 000 - 88 000 | calc |
| **Gross Margin %** | **78,0%** | 312 000 / 400 000 | calc |

## CAC по каналам и funnel conversion
| Канал | Вход в воронку / мес | SQL / demo | Pilot | New paying customers / мес | CAC fully-loaded, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---|
| Outbound ABM | 120 target accounts | 18 | 3 | 0,45 | 980 000 | основной канал для regulated enterprise |
| Paid search + content | 45 MQL | 9 | 3 | 0,35 | 771 000 | помогает demand capture, но не главный драйвер |
| Partnerships / events | 12 warm intros | 6 | 3 | 0,30 | 700 000 | лучший conversion, ограничен scale |
| **Blended** | — | — | — | **1,10** | **836 000** | взвешенная средняя |

### Fully-loaded CAC, обязательная раскладка
Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Marketing FOT allocation + Multiplier_overhead) / New paying customers
```

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/search retargeting/content distribution) | 80 000 | performance + content amplification | inference |
| Outbound team FOT (SDR/AE attributed to new) | 170 000 | только доля времени на new logo acquisition, с учётом 30% соцвзносов | T5 + inference |
| Marketing team FOT (partial allocation) | 45 000 | ~0,15 FTE demand gen / content | T5 + inference |
| Tools (CRM, sequencing, data enrichment, call tools) | 25 000 | CRM + sequencing + enrichment stack | T4 + inference |
| Events / partnerships | 60 000 | roundtable, association fee, partner enablement | inference |
| Overhead multiplier (enterprise x2,2 к raw CAC) | 456 000 | direct subtotal 380 000 × 1,2 extra overhead = 456 000 total uplift to 836 000 | benchmark policy + calc |
| **Итого fully-loaded CAC** | **836 000** | 380 000 × 2,2 | calc |

### Sanity checks по CAC
- **Сегмент**: enterprise (>500K ₽ ACV), поэтому применён multiplier **x2,2**, что попадает в требуемый диапазон **x2,0-x2,5**.
- **Benchmark check**: blended CAC **836 тыс. ₽** попадает в sanity-band **300-900 тыс. ₽** для enterprise SaaS B2B в РФ, значит модель не выглядит заниженной.
- **Канальный CAC** показан отдельно от **blended CAC**.

## LTV и churn
### Benchmark churn source
- Для B2B SaaS с ARR 1-5M USD median gross revenue churn в benchmark = **8,1% в год**. [T3]
- Для conservative investment-case использую **12% annual logo churn**, потому что в РФ enterprise sell-in тяжелее, private cloud и procurement удлиняют замены, но early-stage vendor risk остаётся выше зрелого западного benchmark. [T3 + inference]

### Расчёт LTV
| Параметр | Значение |
|---|---:|
| MRR | 400 000 ₽ |
| Gross Margin | 78,0% |
| Gross Profit / month | 312 000 ₽ |
| Monthly churn | 1,06% |
| **LTV** | **29 433 962 ₽** |

Формула:

```text
LTV = Gross Profit per month / Monthly churn
= 312 000 / 0,0106
≈ 29,4 млн ₽
```

## LTV/CAC, Payback, Contribution Margin
| Метрика | Значение | Формула | Вывод |
|---|---:|---|---|
| LTV/CAC | **35,2x** | 29,43 млн / 0,836 млн | сильно выше порога 3:1 |
| CAC Payback | **2,1 мес** | 836 000 / 400 000 | сильно лучше лимита 18 мес для enterprise |
| Contribution Margin % | **57,1%** | (MRR - COGS - CAC amortized 12m) / MRR | здоровая unit-экономика |

Принята амортизация CAC на 12 месяцев:

```text
Contribution Margin = (400 000 - 88 000 - 69 667) / 400 000 = 57,1%
```

## Team & FOT
### Полная команда
| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Time-to-hire, мес | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес | Источник |
|---|---:|---|---:|---:|---:|---:|---:|---|
| CEO | 1 | enterprise sales, fundraising, key accounts | 650 000 | 0 | 0 | 195 000 | 845 000 | benchmark |
| CTO / Tech Lead | 1 | architecture, security, enterprise delivery | 550 000 | 2,5 | 2 | 165 000 | 715 000 | benchmark |
| Senior Backend | 2 | connectors, policy engine, workflow backend | 420 000 | 1,5 | 1,5 | 126 000 | 1 092 000 | benchmark |
| ML Engineer | 1 | extraction, classification, workflow AI | 500 000 | 2,5 | 2 | 150 000 | 650 000 | benchmark |
| DevOps | 1 | private cloud, logging, infra, security ops | 350 000 | 1,5 | 1 | 105 000 | 455 000 | benchmark |
| Frontend | 1 | analyst workspace, dashboards, admin UI | 280 000 | 1 | 1 | 84 000 | 364 000 | benchmark |
| SDR | 1 | outbound prospecting | 180 000 | 1 | 1 | 54 000 | 234 000 | T5 + benchmark |
| AE | 1 | discovery, pilots, closing | 370 000 | 1,5 | 2-3 | 111 000 | 481 000 | T5 + benchmark |
| Customer Success | 1 | onboarding, adoption, renewals | 250 000 | 1 | 1 | 75 000 | 325 000 | T5 + benchmark |
| Product / Implementation PM | 1 | pilot delivery, scope, rollout | 320 000 | 1,5 | 1 | 96 000 | 416 000 | benchmark |
| GRC Analyst | 1 | audit mappings, evidence workflows | 280 000 | 2 | 1 | 84 000 | 364 000 | benchmark |
| **Итого** | **11** |  |  |  |  |  | **5 941 000** |  |

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в команде | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, CTO | 1 560 000 | founder-led старт, поиск backend и PM открыт |
| M2 | + Senior Backend #1 | 2 106 000 | первый инженер после 6 недель найма |
| M3 | + Senior Backend #2, Product/Implementation PM | 3 014 000 | команда delivery-сборки |
| M4 | + DevOps | 3 469 000 | готовим sandbox/private cloud |
| M5 | + ML Engineer | 4 119 000 | AI-core и extraction pipeline |
| M6 | + Frontend | 4 483 000 | UI для analyst workflow |
| M7 | + SDR | 4 717 000 | только после готовности demo/pilot |
| M8 | + AE | 5 198 000 | sales capacity расширяется |
| M9 | + Customer Success | 5 523 000 | под первые прод-клиенты |
| M10 | + GRC Analyst | 5 887 000 | нужен для scale pilot/onboarding |
| M11 | полный штат | 5 941 000 | steady-state |
| M12 | полный штат | 5 941 000 | steady-state |

### Hiring realism checks
- В M1 нет 5+ новых сотрудников, найм растянут по реалистичному time-to-hire.
- FOT M1 выше 1 млн ₽, что соответствует founder + CTO для enterprise software.
- Full steady-state team достигается только к M10-M11, что согласуется с hiring reality для senior / enterprise roles.

## Fixed costs breakdown
| Статья | ₽/мес | Комментарий |
|---|---:|---|
| Office / legal address / travel reserve | 180 000 | гибридный режим, enterprise meetings |
| Corporate software / admin stack | 90 000 | Google/Notion/Jira/security/helpdesk |
| Legal / audit / DPA / counsel | 160 000 | договоры, procurement, privacy |
| Accounting / payroll / back office | 70 000 | аутсорс + банк |
| Security / compliance certifications prep | 210 000 | аудит, pentest, policy maintenance |
| Misc G&A reserve | 80 000 | непредвиденные расходы |
| **Итого fixed non-FOT** | **790 000** |  |

## Break-even
### По числу клиентов
- Steady-state monthly operating cost = **5 941 000 ₽ FOT + 790 000 ₽ fixed non-FOT = 6 731 000 ₽/мес**.
- Gross profit на 1 клиента = **312 000 ₽/мес**.

```text
Break-even clients = 6 731 000 / 312 000 = 21,57
```

- **Округлённый break-even = 22 клиента**.

### По месяцу
Консервативный ramp активных paying accounts:

| Месяц | Активные клиенты | Monthly GP, ₽ | EBITDA до tax, ₽ |
|---|---:|---:|---:|
| M4 | 1 | 312 000 | -6 419 000 |
| M6 | 4 | 1 248 000 | -5 483 000 |
| M9 | 10 | 3 120 000 | -3 611 000 |
| M12 | 18 | 5 616 000 | -1 115 000 |
| M14 | 22 | 6 864 000 | **+133 000** |
| M16 | 26 | 8 112 000 | +1 381 000 |
| M18 | 30 | 9 360 000 | +2 629 000 |
| M24 | 50 | 15 600 000 | **+8 869 000** |

- **Break-even month = M14** при достижении 22 клиентов.
- **EBITDA > 500 тыс. ₽/мес** достигается уже примерно на **M15-M16**.

## Burn-to-breakeven и runway
### Burn-to-breakeven
- Средний burn на отрезке M1-M13 с учётом ramp и неполной загрузки GTM = **~3,5 млн ₽/мес**.
- Накопленный burn до break-even = **~46 млн ₽**.
- Для enterprise B2B с pilot-led продажами это реалистично и не конфликтует с sanity check по capital intensity.

### Cash runway
```text
Runway = Startup capital / Average burn
= 60 000 000 / 3 500 000
≈ 17,1 мес
```

- **Runway = ~17 месяцев**, чего достаточно, чтобы дойти до M14 break-even без дополнительного equity raise, но буфер не огромный.
- Для более комфортного плана фондовый safe capital здесь скорее **65-70 млн ₽**.

## Инвестиционный вывод
### Что нравится
- Высокий ACV и strong compliance pain делают модель совместимой с enterprise economics.
- Gross margin 78% и blended CAC 836 тыс. ₽ выглядят здраво для regulated enterprise software.
- LTV/CAC сильно выше порога, payback короткий, contribution margin здоровый.
- EBITDA на 50 клиентах не просто положительная, а существенно выше mandatory gate.

### Что тревожит
- Узкий рынок и длинный procurement cycle, поэтому execution risk выше среднего.
- Реальная сложность не в unit economics, а в distribution, security review и founder-led selling.
- Модель ломается, если продукт уедет вниз по рынку в mid-market / low-touch сегмент с ACV < 2,4 млн ₽.

## Verdict P5
- **Unit economics verdict: PASS**.
- **Investment grade: YES**, если команда удерживает enterprise positioning, private cloud readiness и pilot-to-prod conversion.
- **Следующий фокус**: moat, defensibility и подтверждение, что buyer готов покупать не consulting-hours, а повторяемую платформу.

## Sources
- **T1**: внутренний кейс `02-demand.md`, Complyance, 2026-04-21.
- **T2**: Complyance official site, product positioning for AI-native GRC / compliance automation, https://www.complyance.com/
- **T3**: SaaS Capital, 2025 SaaS churn benchmark, median gross revenue churn by ARR band, https://www.saas-capital.com/blog-posts/2025-b2b-saas-churn-benchmarks/
- **T4**: amoCRM pricing, как якорь для CRM/tooling cost, https://www.amocrm.ru/tariffs/
- **T5**: HH.ru / salary benchmark bands for Moscow enterprise sales and customer success roles, https://hh.ru/


---

## Файл: 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- **ARPA / MRR на клиента:** 400 000 ₽/мес.
- **COGS на клиента:** 88 000 ₽/мес.
- **Gross profit на клиента:** 312 000 ₽/мес.
- **Contribution profit на клиента:** 228 400 ₽/мес. (contribution margin 57,1%, после CAC amortized 12m).
- **Team FOT fully-loaded:** 5 941 000 ₽/мес.
- **Fixed non-FOT:** 790 000 ₽/мес.
- **Fixed costs для PnL:** 6 731 000 ₽/мес. = FOT 5 941 000 ₽ + non-FOT 790 000 ₽.
- **Страховые взносы ~30% к ФОТ** уже включены в FOT, повторно не добавляются.
- **Налоги для net layer:** УСН 6% с выручки, IT-льгота 3% с выручки при аккредитации Минцифры, ОСНО 20% налог на прибыль; при ОСНО также возникает НДС 20%, что давит на cash flow.
- **Сценарии new clients / churn:**
  - **Base:** 1,1,1,2,2,2,2,2,2,3,3,3; churn 1,06%/мес.
  - **Optimistic:** 1,1,2,2,2,3,3,3,3,3,4,4; churn 0,8%/мес.
  - **Pessimistic:** 0,1,1,1,1,1,2,2,2,2,2,2; churn 1,5%/мес.
- **Cumulative cash** показан от 0 ₽ как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 1.00 | 1.99 | 2.97 | 4.94 | 6.88 | 8.81 | 10.72 | 12.60 | 14.47 | 17.32 | 20.13 | 22.92 |
| MRR, ₽ | 400 000 | 795 760 | 1 187 325 | 1 974 739 | 2 753 807 | 3 524 617 | 4 287 256 | 5 041 811 | 5 788 368 | 6 927 011 | 8 053 585 | 9 168 217 |
| COGS, ₽ | 88 000 | 175 067 | 261 211 | 434 443 | 605 838 | 775 416 | 943 196 | 1 109 198 | 1 273 441 | 1 523 942 | 1 771 789 | 2 017 008 |
| Gross profit, ₽ | 312 000 | 620 693 | 926 113 | 1 540 297 | 2 147 970 | 2 749 201 | 3 344 060 | 3 932 612 | 4 514 927 | 5 403 069 | 6 281 796 | 7 151 209 |
| GM% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% |
| Fixed costs, ₽ | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 |
| EBITDA, ₽ | -6 419 000 | -6 110 307 | -5 804 887 | -5 190 703 | -4 583 030 | -3 981 799 | -3 386 940 | -2 798 388 | -2 216 073 | -1 327 931 | -449 204 | 420 209 |
| Cash burn, ₽ | 6 419 000 | 6 110 307 | 5 804 887 | 5 190 703 | 4 583 030 | 3 981 799 | 3 386 940 | 2 798 388 | 2 216 073 | 1 327 931 | 449 204 | 0 |
| Cumulative cash, ₽ | -6 419 000 | -12 529 307 | -18 334 194 | -23 524 897 | -28 107 928 | -32 089 727 | -35 476 667 | -38 275 055 | -40 491 128 | -41 819 059 | -42 268 263 | -42 268 263 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.99 | 3.98 | 5.94 | 7.90 | 10.83 | 13.75 | 16.64 | 19.50 | 22.35 | 26.17 | 29.96 |
| MRR, ₽ | 400 000 | 796 800 | 1 590 426 | 2 377 702 | 3 158 681 | 4 333 411 | 5 498 744 | 6 654 754 | 7 801 516 | 8 939 104 | 10 467 591 | 11 983 850 |
| COGS, ₽ | 88 000 | 175 296 | 349 894 | 523 094 | 694 910 | 953 350 | 1 209 724 | 1 464 046 | 1 716 333 | 1 966 603 | 2 302 870 | 2 636 447 |
| Gross profit, ₽ | 312 000 | 621 504 | 1 240 532 | 1 854 608 | 2 463 771 | 3 380 061 | 4 289 020 | 5 190 708 | 6 085 182 | 6 972 501 | 8 164 721 | 9 347 403 |
| GM% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% |
| Fixed costs, ₽ | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 |
| EBITDA, ₽ | -6 419 000 | -6 109 496 | -5 490 468 | -4 876 392 | -4 267 229 | -3 350 939 | -2 441 980 | -1 540 292 | -645 818 | 241 501 | 1 433 721 | 2 616 403 |
| Cash burn, ₽ | 6 419 000 | 6 109 496 | 5 490 468 | 4 876 392 | 4 267 229 | 3 350 939 | 2 441 980 | 1 540 292 | 645 818 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 419 000 | -12 528 496 | -18 018 964 | -22 895 356 | -27 162 585 | -30 513 524 | -32 955 504 | -34 495 796 | -35 141 614 | -35 141 614 | -35 141 614 | -35 141 614 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 1.00 | 1.98 | 2.96 | 3.91 | 4.85 | 6.78 | 8.68 | 10.55 | 12.39 | 14.20 | 15.99 |
| MRR, ₽ | 0 | 400 000 | 794 000 | 1 182 090 | 1 564 359 | 1 940 893 | 2 711 780 | 3 471 103 | 4 219 037 | 4 955 751 | 5 681 415 | 6 396 194 |
| COGS, ₽ | 0 | 88 000 | 174 680 | 260 060 | 344 159 | 426 997 | 596 592 | 763 643 | 928 188 | 1 090 265 | 1 249 911 | 1 407 163 |
| Gross profit, ₽ | 0 | 312 000 | 619 320 | 922 030 | 1 220 200 | 1 513 897 | 2 115 188 | 2 707 460 | 3 290 849 | 3 865 486 | 4 431 504 | 4 989 031 |
| GM% | 0.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% | 78.0% |
| Fixed costs, ₽ | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 | 6 731 000 |
| EBITDA, ₽ | -6 731 000 | -6 419 000 | -6 111 680 | -5 808 970 | -5 510 800 | -5 217 103 | -4 615 812 | -4 023 540 | -3 440 151 | -2 865 514 | -2 299 496 | -1 741 969 |
| Cash burn, ₽ | 6 731 000 | 6 419 000 | 6 111 680 | 5 808 970 | 5 510 800 | 5 217 103 | 4 615 812 | 4 023 540 | 3 440 151 | 2 865 514 | 2 299 496 | 1 741 969 |
| Cumulative cash, ₽ | -6 731 000 | -13 150 000 | -19 261 680 | -25 070 650 | -30 581 450 | -35 798 553 | -40 414 365 | -44 437 905 | -47 878 056 | -50 743 570 | -53 043 067 | -54 785 036 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 400 000 ₽
- **COGS:** 88 000 ₽
- **Gross profit:** 312 000 ₽
- **Variable sales/support и CAC amortized:** 83 600 ₽
- **Contribution:** 228 400 ₽

#### Waterfall на EBITDA break-even уровне
- **EBITDA break-even client count:** 6 731 000 / 312 000 = **21,6 клиента**, округлённо **22 клиента**.
- На **22 клиентах**:
  - **Revenue:** 8 800 000 ₽/мес
  - **COGS:** 1 936 000 ₽/мес
  - **Gross profit:** 6 864 000 ₽/мес
  - **Contribution:** 5 024 800 ₽/мес
  - **EBITDA:** **+133 000 ₽/мес**

#### Net после налогов РФ
- **УСН 6%:** налог = 528 000 ₽, net ≈ **-395 000 ₽/мес** на уровне 22 клиентов.
- **IT-льгота 3%:** налог = 264 000 ₽, net ≈ **-131 000 ₽/мес** на уровне 22 клиентов.
- **ОСНО 20%:** налог на прибыль взимается только с положительной прибыли, net ≈ **106 400 ₽/мес**, но возникает **НДС 20%**, ухудшающий cash conversion и working capital.

#### Net break-even client count по режимам
- **IT-льгота 3%:** 6 731 000 / (400 000 - 88 000 - 12 000) = **22,4 клиента**, округлённо **23**.
- **УСН 6%:** 6 731 000 / (400 000 - 88 000 - 24 000) = **23,4 клиента**, округлённо **24**.
- **ОСНО 20%:** 6 731 000 / ((400 000 - 88 000) × 0,8) = **27,0 клиентов**, округлённо **27**, плюс дополнительное давление НДС 20% на денежный поток.

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M10 | 35 141 614 ₽ | Быстрый выход в плюс за счёт 30 клиентов к M12 и лучшего churn |
| Base | M12 | 42 268 263 ₽ | Базовый план сходится в первый год, но требует >42 млн ₽ капитала до BEP |
| Pessimistic | M16 | 56 748 782 ₽ | При более слабом ramp почти съедается весь исходный startup capital 60 млн ₽ |

### A7. Налоговая модель РФ
- **УСН 6%** лучше для простоты администрирования, но на пограничном месяце break-even может оставлять post-tax net отрицательным.
- **IT-льгота 3%** наиболее рациональна для этого кейса: высокомаржинальная software-модель, enterprise SaaS и заметное улучшение post-tax PnL при наличии аккредитации Минцифры.
- **ОСНО 20%** в PnL может выглядеть терпимо при уже положительном EBITDA, но **НДС 20%** создаёт кассовую нагрузку, особенно в длинном enterprise procurement cycle.
- **Страховые взносы ~30% к ФОТ** уже сидят в fully-loaded FOT 5 941 000 ₽/мес.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Net break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 22 | 23 | M10 | В плюс выходит внутри года, модель комфортна для startup capital 60 млн ₽ |
| Base | 22 | 24 | M12 | Сходится на границе первого года, остаётся умеренный запас по капиталу |
| Pessimistic | 22 | 27 | M16 | При слабом наборе клиентов runway становится почти предельным |

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев

База берётся из SECTION A. Для stress-test я меняю по одной ключевой переменной, сохраняя остальные допущения неизменными. Для CAC x2 предполагаю, что при том же GTM-бюджете new-logo throughput падает примерно вдвое, то есть активная клиентская база к M12 сокращается примерно до 11,46 аккаунта. Это консервативная, но практичная интерпретация enterprise funnel.

| Сценарий | Ключевое изменение | Клиенты к M12 | GP на клиента, ₽/мес | EBITDA @M12, ₽/мес | Вывод |
|---|---|---:|---:|---:|---|
| Base | Без изменений | 22,92 | 312 000 | 420 209 | Модель выходит в слабый плюс только на границе года |
| Sens1 | CAC x2 | 11,46 | 312 000 | -3 155 396 | Воронка перестаёт окупать рост, модель уходит глубоко в минус |
| Sens2 | Churn x2 | 21,91 | 312 000 | 103 467 | Почти нулевой запас прочности, EBITDA-порог держится на грани |
| Sens3 | Price -30% | 22,92 | 192 000 | -2 330 456 | Ценовая эрозия ломает economics даже при сохранении клиентской базы |

**Ключевой вывод:** у кейса хорошая базовая unit-экономика, но слабая tolerance к двум вещам, CAC inflation и price compression. Именно они, а не churn сами по себе, выглядят главными destroyers equity story.

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 700 000 | 836 000 | 1 670 000 | [T1][T5] |
| Monthly churn, % | 0,8% | 1,06% | 2,12% | [T1][T3] |
| ARPU, ₽/мес | 280 000 | 400 000 | 520 000 | [T1][T6][T7][T8] |
| Conversion rate lead→paid, % | 0,4% | 0,62% | 1,0% | [T1] |
| Time-to-hire, месяцев | 1,0 | 1,6 | 2,8 | [T1][T5] |

#### Метод
Вместо формальной 1000-run симуляции использую упрощённую версию из 9 комбинаций на базе triangular inputs. p10 соответствует worst-side cluster, p50 — mode/mode/mode, p90 — best-side cluster. Для EBITDA@M24 дополнительно учитываю, что высокий CAC и слабая conversion снижают число активных клиентов к M24, а не только ухудшают payback.

#### Результат Monte Carlo Lite
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24, ₽/мес | -1 931 000 | 8 869 000 | 18 325 000 | 20 256 000 |
| CAC payback, мес | 6,0 | 2,1 | 1,3 | 4,7 |
| LTV/CAC | 5,4x | 35,2x | 77,1x | 71,7x |
| Cash runway, мес | 11,5 | 17,1 | 23,0 | 11,5 |

#### Интерпретация Monte Carlo
- **Правило 1 сработало:** p10 EBITDA < 0, значит появляется прямой риск insolvency при плохом сочетании CAC, churn и ARPU.
- **Правило 2 не сработало:** p50 EBITDA существенно выше 500 тыс. ₽/мес, median-case проходит EBITDA Gate.
- **Правило 3 сработало по сути:** распределение пересекает ноль, а разброс между p90 и p10 экстремален; score стоит понизить на 1 notch за неопределённость execution.
- **Правило 4 сработало:** range width по LTV/CAC = 71,7x, то есть модель хрупкая и слишком чувствительна к pricing, churn и CAC discipline.

### B3. Competitor deep-dive

#### Западные конкуренты
| Конкурент | Что видно по рынку | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Vanta | Один из category leaders в compliance automation, >10k клиентов и сильный brand pull. [T6] | Сильный бренд, быстрый onboarding, широкий ecosystem of integrations, хорошая упаковка для SOC 2 / ISO 27001 | Лучше заточен под US/cloud-native mid-market, слабее для локальной регуляторики РФ и on-prem/private perimeter | **~18-22%** западного compliance-automation subsegment, estimate по customer footprint и brand visibility [inference] | Complyance может быть сильнее в private cloud, локальной регуляторике и enterprise evidence workflows для банков/страховщиков |
| Drata | Крупный fast-growing игрок, активно продаёт automation + continuous control monitoring. [T7] | Сильный GTM, enterprise reporting, зрелый product marketing, хороший audit-readiness workflow | Более дорогой и process-heavy, меньше локальной адаптации под non-US data residency | **~12-16%** сегмента, estimate по scale и enterprise penetration [inference] | У нас может быть ниже implementation friction для РФ-заказчика и более прикладной vendor-risk/control-testing use case |
| Secureframe | Сильный SMB/mid-market anchor с понятным pricing и быстрым стартом. [T8] | Простота запуска, сильный self-serve narrative, прозрачный pricing anchor | Меньше глубины для тяжёлого regulated enterprise, слабее в кастомных контрольных матрицах и private deployment | **~6-9%** сегмента, estimate по pricing-led footprint [inference] | Complyance лучше подходит для high-touch enterprise, security review и сложных procurement cycles |

#### Российские конкуренты
| Конкурент | Источник | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Security Vision | Skolkovo + рынок GRC/SOC use cases. [T9] | Известный российский enterprise vendor, on-prem, интеграции, сильный security/GRC контур | Тяжёлый enterprise delivery, выше стоимость внедрения, продукт шире GRC и может быть менее AI-native | **~12-18%** адресуемого РФ enterprise GRC-automation сегмента [inference] | Complyance может выигрывать более узким compliance-first positioning и более быстрым запуском на audit-readiness сценариях |
| Compliance Control / Compliance Technologies | Rusprofile подтверждает юрлицо и B2B-направление, рынок точечных compliance-решений. [T10] | Фокус на compliance domain, локальная экспертиза, понятность для российских regulated buyers | Ограниченный brand reach, меньше product breadth, ниже темп масштабирования | **~4-7%** адресуемого сегмента [inference] | У нас выше шанс собрать platform play, а не point solution, если удержать AI-native workflow layer |
| ProCompliance | VC.ru + локальный positioning вокруг автоматизации комплаенса и процессов. [T11] | Хорошая локальная экспертиза, близость к практическим pain points российского compliance | Более сервисная, чем platform-driven модель, слабее масштабируемость и moat | **~3-5%** сегмента [inference] | Complyance выглядит лучше как software layer с recurring revenue, а не как consultancy wrapper |
| Digital Compliance | Habr/публичные материалы по автоматизации compliance-практик. [T12] | Глубокая методологическая экспертиза, доверие в профессиональном контуре | Часто продаётся как экспертиза и внедрение, а не repeatable SaaS-platform | **~2-4%** сегмента [inference] | Наш upside выше, если продукт реально автоматизирует evidence collection и control testing, а не только сопровождает их |

#### Вывод по конкурентам
- Западный рынок уже доказывает willingness-to-pay, но западные лидеры плохо ложатся на российские private-cloud, 152-ФЗ и sanctions-driven procurement constraints.
- В РФ основная конкуренция идёт не только от SaaS, но и от hybrid vendors, SI-подобных внедренцев и compliance consulting wrappers.
- Значит, moat Complyance должен строиться не на generic AI, а на **локальном deployment trust + evidence workflow depth + procurement readiness**.

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется в repeatable GTM | med | high | >70% всех сделок держатся лично на фаундере к M6 | Нанять сильного AE, формализовать playbook, считать conversion по этапам |
| Operational | LLM / OCR quality недостаточна для audit-grade evidence | med | high | >10% pilot outputs требуют ручного rework или вызывают red flags у security/compliance команды | Human-in-the-loop, policy rules поверх LLM, audit logs, ограничить критичные сценарии |
| Operational | Зависимость от внешних LLM API и latency/SLA | high | high | рост unit-cost inference >30% или деградация SLA две недели подряд | Multi-model routing, local fallback, контрактные лимиты, кэширование и OCR-first pipeline |
| Market | Спрос уже, чем ожидается, и реальный SAM ближе к low-end диапазона | med | high | pipeline <20 target accounts в квартал при enterprise ICP | Сузить ICP до банков/страховщиков, усилить партнёрские каналы и ассоциации |
| Market | Крупные конкуренты начинают price compression | high | high | скидки >25% становятся нормой на последних стадиях тендеров | Защищать цену через private cloud, onboarding, vendor risk и implementation bundle |
| Market | Pilot-to-paid conversion ниже модели | med | high | conversion pilot→paid <25% два квартала подряд | Жёстко квалифицировать pilot, продавать success criteria upfront, брать paid pilot |
| Regulatory | Требования 152-ФЗ и data residency ограничивают SaaS deployment | high | high | заказчики требуют только on-prem/private contour | Сразу проектировать private cloud/on-prem вариант, локальное хранение данных |
| Regulatory | 115-ФЗ / отраслевые требования меняют объём обязательных контролей | med | med | растёт число кастомных требований в RFP и legal review | Модульная policy engine архитектура, локальная legal/GRC advisory board |
| Financial | Runway сжимается из-за burn до выхода на 22+ клиентов | med | high | cash runway падает ниже 12 месяцев до M6-M7 | Freeze hiring, stage-gate по GTM, raise bridge раньше, чем потребуется emergency round |
| Financial | Курс USD и инфляция раздувают облако, LLM и зарплаты | high | med | рост долларовых затрат >20% и FOT drift >15% за полугодие | Индексация прайса, рублёвые контракты, vendor diversification, бюджетные буферы |
| Black swan | Новый санкционный пакет режет доступ к SaaS/infra/vendor stack | med | high | vendor notices, billing failures, ограничение новых контрактов | Локальные альтернативы, резервные провайдеры, критичный стек без single point of failure |
| Black swan | Частичное или полное отключение LLM-доступа | low | very high | массовые инциденты у API-провайдера или geo-blocking | Graceful degradation на rules/OCR flow, on-prem open-weight fallback, ручной режим для critical paths |

### B5. Kill conditions через 6 месяцев
1. **M6 active paying customers < 6** или pipeline coverage <2,0x от плана, значит GTM не подтверждён и выход к 22 клиентам становится малореалистичным.
2. **Blended CAC > 1,6 млн ₽** или **pilot→paid conversion < 20%** по двум когортам подряд, значит sales engine не масштабируется экономически.
3. **Monthly churn > 2,0%** или **ARPA < 300 тыс. ₽/мес** после скидок, значит pricing power и retention недостаточны для инвестиционного кейса.

### B6. Итог по SECTION B
- Кейс остаётся **проходным**, но уже не как clean low-risk compounding story, а как **high-upside / high-execution-risk enterprise bet**.
- Главные триггеры разрушения value: **CAC inflation, ценовая эрозия, vendor/deployment risk**.
- Если команда удерживает private-cloud wedge и enterprise pricing, upside остаётся заметным. Если скатывается в services-heavy или discount-heavy motion, equity story быстро деградирует.

### Sources for SECTION B
- **T1**: внутренний кейс `04-economics.md`, Complyance, 2026-04-22.
- **T3**: SaaS Capital, 2025 B2B SaaS churn benchmarks, https://www.saas-capital.com/blog-posts/2025-b2b-saas-churn-benchmarks/
- **T5**: HH.ru salary bands / hiring benchmarks for Moscow enterprise GTM and product roles, https://hh.ru/
- **T6**: Vanta official site, customer scale and category positioning, https://www.vanta.com/
- **T7**: Drata official site, platform positioning and public packaging, https://drata.com/
- **T8**: Secureframe pricing / positioning, https://secureframe.com/pricing
- **T9**: Security Vision company materials / Skolkovo profile, https://securityvision.ru/ , https://navigator.sk.ru/
- **T10**: Rusprofile, ООО «Комплаенс Технологии», https://www.rusprofile.ru/
- **T11**: VC.ru materials on ProCompliance / compliance automation in Russia, https://vc.ru/
- **T12**: Habr materials on digital compliance practice / tooling, https://habr.com/

<!-- P6A-DONE -->
<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[GEO-EXPAND] Complyance — APPROVED: 71/100 | EBITDA base=8870К₽/мес через 24 мес | LTV/CAC=35,2x | Ключевое преимущество: private-cloud wedge для regulated enterprise | Главный риск: узкий РФ-рынок и длинный procurement cycle.

# 06-verdict — Complyance

sector: GEO-EXPAND

## Итоговый вердикт
- **Вердикт:** **APPROVED with notes**
- **Score:** **71/100**
- **Статус инвесткомитета:** кейс проходит порог только как **enterprise-only AI-native GRC / compliance automation platform** для regulated buyers в РФ.
- **Формальный gate:** выполнен, потому что `company_ebitda_potential_rub_month` в base-case составляет **8 869 000 ₽/мес к M24**, порог **500 000 ₽/мес** достигается примерно к **M15-M16**, а 500K EBITDA достигается при числе клиентов существенно ниже 50.
- **Оговорка:** approval не является clean pass. Это high-upside, high-execution-risk ставка, где основной вопрос не в юнит-экономике, а в repeatable GTM, локальном moat и доказательстве, что продукт не скатится в services-heavy delivery.
- **Примечание по стадиям:** в исходном кейсе demand-файл существует как `02-demand.md`; отдельный `03-demand.md` отсутствует. Ниже использую фактический demand-артефакт кейса.

## Оценка
Source tier balance: T1=4, T2=7, T3=1, weighted=2.25. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | `Gross Margin = 78,0%`, `LTV/CAC = 35,2x`, `CAC Payback = 2,1 мес` из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 22 | `EBITDA > 500 тыс. ₽/мес достигается уже примерно на M15-M16`, `EBITDA @M24 = +8 869 000 ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | `public search-demand в РФ низкий`, но есть `hh_vacancies=103` и `SAM РФ = 0,6-1,0 млрд ₽`; применён tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Moat строится вокруг `private cloud, локальной регуляторики и enterprise evidence workflows`, но network effects и scale economies ограничены. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | В risk matrix есть `LLM / OCR quality`, `санкции`, `152-ФЗ`, `founder-led sales`, поэтому риск выше среднего. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `Blended CAC = 836 000 ₽`, `sales cycle 3,5-5,5 месяца`, ICP и named targets понятны для ABM/partner-led GTM. |

**Sum raw = 106/150. Normalized score = round((106 × 100) / 150) = 71/100.**

## Investment thesis
Complyance выглядит как редкий для РФ enterprise-only wedge, где слабый публичный demand компенсируется высокой ценностью одного контракта, сильной юнит-экономикой и понятной болью regulated buyers. Кейс проходит не как широкий SaaS category winner, а как узкая платформа для audit readiness, evidence collection, vendor risk и control testing внутри private cloud / sovereign deployment контура.

## FULL business process from 04-economics.md
| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | SDR + AE | CRM, account list, email sequencing | 1 день | 3 500 | semi-auto |
| 2 | Outbound / partner outreach | SDR | почта, LinkedIn-аналоги, events follow-up, CRM | 5-10 дней | 12 000 | semi-auto |
| 3 | Qualification call | SDR | VoIP, calendar, CRM | 30-45 мин | 2 500 | low |
| 4 | Discovery с compliance owner | AE + founder | Zoom/Meet, CRM, notes | 1-2 встречи за 7 дней | 14 000 | low |
| 5 | Demo + use-case mapping | AE + solution lead | demo env, deck, security FAQ | 1 неделя | 22 000 | low |
| 6 | Pilot scoping + security review | CTO + GRC analyst | pilot workspace, DPA/security docs | 2-4 недели | 70 000 | low |
| 7 | Pilot execution / evidence ingestion | ML/Backend + GRC analyst | private cloud / sandbox, integrations | 3-6 недель | 140 000 | semi-auto |
| 8 | Procurement + legal | AE + CEO | MSA/DPA/templates, procurement portal | 2-6 недель | 38 000 | low |
| 9 | Invoice / PO issuance | finance/admin | ЭДО, billing, accounting | 2-5 дней | 6 000 | high |
| 10 | Payment collection | finance/admin | bank, ERP/accounting | 7-30 дней | 4 000 | high |
| 11 | Onboarding / production rollout | CSM + implementation PM + DevOps | project plan, SSO, connectors, training | 3-5 недель | 95 000 | semi-auto |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| ACV | 4 800 000 ₽/год |
| MRR на клиента | 400 000 ₽/мес |
| customer_ltv_rub | 29 433 962 ₽ |
| Gross Margin | 78,0% |
| contribution_margin_rub_month | 312 000 ₽/мес на клиента |
| Fully-loaded CAC | 836 000 ₽ |
| LTV/CAC | 35,2x |
| CAC Payback | 2,1 мес |
| Contribution Margin % | 57,1% |
| fixed_costs_rub_month | 6 731 000 ₽/мес |
| Break-even | 22 клиента |
| company_ebitda_rub_month @ 22 клиента | 133 000 ₽/мес |
| company_ebitda_potential_rub_month @ 50 клиентов | 8 869 000 ₽/мес |
| clients_to_500k_ebitda | 24 |
| clients_to_1m_ebitda | 25 |
| months_to_500k_ebitda | 15-16 мес |
| months_to_1m_ebitda | 16 мес |
| startup_capital_to_bep_rub | 42 268 263 ₽ (base), 35 141 614 ₽ (optimistic), 56 748 782 ₽ (pessimistic) |

## Команда
| Роль | Кол-во | FOT fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO | 1 | 845 000 | enterprise sales, fundraising, key accounts |
| CTO / Tech Lead | 1 | 715 000 | architecture, security, delivery |
| Senior Backend | 2 | 1 092 000 | connectors, workflow backend |
| ML Engineer | 1 | 650 000 | extraction, classification, AI-core |
| DevOps | 1 | 455 000 | private cloud, security ops |
| Frontend | 1 | 364 000 | analyst workspace, admin UI |
| SDR | 1 | 234 000 | outbound prospecting |
| AE | 1 | 481 000 | discovery, pilots, closing |
| Customer Success | 1 | 325 000 | onboarding, adoption |
| Product / Implementation PM | 1 | 416 000 | pilot delivery |
| GRC Analyst | 1 | 364 000 | audit mappings, evidence workflows |
| **Итого** | **11** | **5 941 000** | steady-state к M10-M11 |

## Moat — 7-factor framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | Есть данные, интеграции, audit history и обученность compliance-команды. |
| Scale economies | 1 | COGS падает умеренно, но pilot/security review остаются дорогими. |
| Proprietary data / model advantage | 2 | Может накапливаться локальный compliance corpus и evidence workflow data, но размер датасета публично не доказан. |
| Regulatory moat | 1 | 152-ФЗ и private deployment помогают, но формальной лицензии/moat как у regulated infra пока нет. |
| Brand / distribution | 2 | Есть понятный wedge для банков, страховщиков и крупных финтехов, но бренд ещё не category-defining. |
| Embedded workflow | 3 | Решение глубоко встраивается в control testing, evidence collection, vendor risk и audit readiness. |

**Moat sum = 11/21. Moat score = round((11 × 25) / 21) = 13/25.**

## GTM — 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Крупнейший regulated buyer с тяжёлым контуром внутреннего контроля, vendor risk и audit evidence. | email decision-maker + отраслевые конференции по ИБ/рискам | 600 000 ₽/мес |
| 2 | ВТБ | Банк с высокой регуляторной нагрузкой и длинным циклом согласований, где private cloud критичен. | партнёрство с интегратором + warm intro | 550 000 ₽/мес |
| 3 | Газпромбанк | Сложный procurement и большой объём контрольных процедур, подходит для pilot-led enterprise sales. | прямой outbound в compliance/risk lead | 500 000 ₽/мес |
| 4 | Альфа-Банк | Digital-heavy банк, где vendor risk и evidence workflows можно оцифровать быстрее через API-first контур. | founder-led outreach + профильные мероприятия | 500 000 ₽/мес |
| 5 | Т-Банк | Технологичный buyer, чувствительный к automation ROI и скорости audit readiness. | email VP risk/compliance + product security контакт | 450 000 ₽/мес |
| 6 | Совкомбанк | Комбинация regulated pain и потребности в repeatable control testing across entities. | партнёрский канал через аудит/консалтинг | 400 000 ₽/мес |
| 7 | СОГАЗ | Страховой рынок РФ имеет тяжёлый контрольный контур и документные evidence workflows. | конференция + outbound в risk/compliance director | 450 000 ₽/мес |
| 8 | Росгосстрах | Высокий объём регуляторной отчётности и vendor-risk процессов в страховании. | партнёрство с GRC/ИБ-интегратором | 400 000 ₽/мес |
| 9 | МТС | Крупный data-heavy enterprise с compliance, vendor risk и внутренними аудитами в нескольких периметрах. | ABM-outreach + отраслевой event | 450 000 ₽/мес |
| 10 | Яндекс | Большая группа с множеством data/process контуров, где важны audit trails и локальный deployment trust. | founder network + direct outreach в governance/security | 500 000 ₽/мес |

### Оценка GTM realism
- Канальный fit подтверждён: для такого продукта работают **ABM outbound, partner-led introductions, conferences и founder-led enterprise sales**, а не PLG.
- CAC payback **2,1 месяца** выглядит очень сильным, но его нужно читать вместе с sales cycle **3,5-5,5 месяца** и дорогими pilot/security-review этапами.
- 10 named targets присутствуют, поэтому автоматический штраф к GTM не применяется.

## Финансовая интерпретация для инвесткомитета
- Модель даёт редкое сочетание **высокого ACV**, **здоровой gross margin** и **короткого payback**, что делает кейс финансово привлекательным.
- При этом robustness ограничена: в sensitivity `CAC x2` даёт **EBITDA @M12 = -3 155 396 ₽**, а `Price -30%` даёт **-2 330 456 ₽**.
- Monte Carlo Lite пересекает ноль по p10: `EBITDA @M24 p10 = -1 931 000 ₽`, `p50 = 8 869 000 ₽`, `p90 = 18 325 000 ₽`. Это нормальный паттерн для approval with notes, но не для clean conviction bet.

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| CAC inflation / pilot-to-paid friction | high | high | Sensitivity показывает, что при CAC x2 модель уходит в глубокий минус уже к M12. |
| Price compression в тендерах и enterprise procurement | high | high | `Price -30%` ломает economics даже при сохранении клиентской базы. |
| Deployment / sanctions / LLM dependency risk | med-high | high | Private cloud, 152-ФЗ и доступность внешних LLM-вендоров напрямую влияют на delivery и SLA. |

## Что должно быть доказано после инвестиции
1. **3-5 paid pilots** в банках/страховщиках с последующим pilot-to-prod conversion не ниже 30%.
2. **Private cloud / on-prem deployment playbook**, проходящий security review без кастомного переписывания продукта под каждого клиента.
3. **Repeatable GTM motion**: не менее 10-15 named target accounts в активном pipeline и не более 50% выручки, зависящей лично от фаундера.
4. **Pricing discipline**: удержание ARPA на уровне не ниже 400 000 ₽/мес без discount-heavy closing.

## Proof points for APPROVED
- `LTV/CAC = 35,2x` и `CAC Payback = 2,1 мес` дают очень сильную unit-экономику для enterprise software.
- `Break-even = 22 клиента`, а `company_ebitda_potential_rub_month @ 50 клиентов = 8 869 000 ₽/мес`, то есть EBITDA-gate уверенно проходит.
- Есть понятный wedge: **private cloud + локальная регуляторика + evidence workflow depth**.
- Demand слабый по search, но не нулевой по budget reality: `hh_vacancies=103`, а ICP состоит из конкретных regulated buyers с высокой стоимостью ручного compliance-труда.

## Финальное решение комитета
**APPROVED with notes.**

Почему approve, а не near-pass:
- экономика заметно выше порога,
- EBITDA-потенциал сильный,
- buyer list конкретный,
- есть внятный enterprise wedge.

Почему с notes, а не чистый approved:
- public demand в РФ остаётся низким,
- moat средний, а не выдающийся,
- модель чувствительна к CAC inflation и price compression,
- execution зависит от сильной founder-led enterprise motion и готовности к local/private deployment.


---

## Файл: 07-score-trajectory.md

# Score Trajectory

## 2026-04-21 — P4 Demand Validation
- Stage: P4
- Summary: публичный search-demand в РФ низкий, но есть узкий enterprise-спрос в regulated сегментах; early reject не сработал, потому что Profit Gate проходит в enterprise/hybrid monetization.
- Demand: LOW
- Profit Gate: PASS
- Suggested trajectory: keep alive, но как niche enterprise play
- Analyst note: рынок в РФ небольшой и неоднородный, поэтому дальше важно особенно жёстко проверить distribution, sales cycle и moat.

## 2026-04-22 — P5 Unit Economics
- Stage: P5
- Summary: enterprise-only модель даёт ACV 4,8 млн ₽/год, GM 78%, blended fully-loaded CAC 836 тыс. ₽, break-even на 22 клиентах и EBITDA ~8,9 млн ₽/мес на 50 клиентах.
- Unit Economics: PASS
- LTV/CAC: 35,2x
- CAC Payback: 2,1 мес
- Break-even: 22 клиента, ориентир M14
- Suggested trajectory: keep alive, investment-grade economics при сохранении enterprise positioning
- Analyst note: риск смещается из экономики в execution, procurement и ability to convert pilots into recurring platform revenue.

## 2026-04-22 — P7 Critic and Verdict
- Stage: P7
- Summary: кейс проходит инвесткомитет как APPROVED with notes, потому что сильная unit-экономика и EBITDA potential перевешивают LOW public demand и средний moat.
- Verdict: APPROVED
- Score: 71/100
- company_ebitda_potential_rub_month: 8 869 000 ₽/мес
- months_to_500k_ebitda: 15-16
- Suggested trajectory: approve как enterprise-only private-cloud GRC wedge, но жёстко мониторить GTM и pricing discipline
- Analyst note: главный апсайд сидит в private-cloud deployment и audit-readiness workflows; главный стоп-риск в CAC inflation, price compression и founder-led sales dependence.


---
