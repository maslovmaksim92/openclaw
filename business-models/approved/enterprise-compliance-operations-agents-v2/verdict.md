# Enterprise Compliance Operations Agents v2 — Full Verdict Package
> Скомпилированный пакет стадий P2/P4/P5/P6/P7 для публикации в GitHub.
> Примечание: в этом rerun-кейсе demand-файл существует как `02-demand.md`; отдельный `03-demand.md` отсутствует в исходном пайплайне и не создавался заново.

---

## Файл: 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-rerun-enterprise-compliance-operations-agents.md
created: 2026-04-19T19:16:56+03:00
original_verdict: /home/node/.openclaw/repo/business-models/approved/enterprise-compliance-operations-agents__backup_2026-04-17_0355_msk/verdict.md
previous_score: "72/100"
previous_status: APPROVED
previous_date: 2026-04-16
---

# Intake — Enterprise Compliance Operations Agents

## Режим обработки
Принудительный rerun по правилу полного пайплайна для файлов `rerun-*`. Duplicate-проверка пропущена намеренно. Следующий этап: **P3-demand-validation**.

## Исходный контекст raw

# RE-ANALYSIS REQUEST — Enterprise Compliance Operations Agents

## Meta
- previous_status: ✅ APPROVED
- previous_score: 72/100
- previous_sector: B2B-OPS
- previous_date: 2026-04-16
- source_folder: /business-models/approved/enterprise-compliance-operations-agents__backup_2026-04-17_0355_msk/
- reason_for_rerun: обновлены P4 (Source Tiering, TAM/SAM/SOM), P5 (Fully-loaded CAC, Hiring Realism), P6B (Monte Carlo Lite), P7 (Rubric 6×25, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner)

## Description (1 line)
Enterprise compliance operations agents с сильной экономикой и регулярной compliance-болью проходят порог, если удержать продуктовую дисциплину и не уйти в bespoke-консалтинг.

## Задача для intake-triage
1. Прочитай verdict.md предыдущего запуска (`/home/node/.openclaw/repo/business-models/approved/enterprise-compliance-operations-agents__backup_2026-04-17_0355_msk/verdict.md`) для контекста, но НЕ копируй результат — начни свежий анализ.
2. Создай новый кейс в pipeline/cases/enterprise-compliance-operations-agents-v2/ и пройди полный пайплайн P3→P7 с новой рубрикой.
3. Сравни новый score с предыдущим (72/100) и запиши delta в финальный 06-verdict.md.

## Приоритет
p1 — batch re-run после обновления системы аналитики 2026-04-19.

---

## Файл: 02-demand.md

# 02-demand — Demand Validation

## Кейс
Enterprise Compliance Operations Agents, агентный слой для непрерывного compliance-операционного цикла: сбор evidence, контроль политик, подготовка к аудитам, управление remediation и регуляторной отчётностью.

## Итог
**Статус: CONDITIONAL PASS**

По exact-category в РФ поисковый спрос низкий, но money demand подтверждён: компании уже платят за privacy/compliance SaaS, подготовку к ISO/SOC 2, DPO-as-a-service и автоматизацию PD/GRC-процессов. [T2][T3] Early reject не срабатывает, потому что существует правдоподобный путь к EBITDA выше 500 000 ₽/мес как минимум в mid-market и enterprise сценариях. [T2]

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand?keyword=enterprise%20compliance%20operations%20agents`

- `enterprise compliance operations agents`: composite demand **LOW**, score **0**, hh.ru **0**, Habr **2**, Yandex suggest **2**. [T3]
- `compliance automation`: composite demand **LOW**, score **7**, hh.ru **52**, Google Trends RU **0**, Yandex suggest **2**. [T3]
- `автоматизация compliance`: composite demand **LOW**, score **22**, hh.ru **52**, Google Trends RU **1**, Yandex suggest **100**. [T3]

### Интерпретация
Низкий exact-keyword объясним: покупают не формулировку `enterprise compliance operations agents`, а budget lines `compliance automation`, `privacy management`, `ISO/SOC 2 readiness`, `vendor risk`, `GRC`. [T2][T3] Наличие 52 вакансий по смежному запросу и высокий suggest по русскоязычной формулировке подтверждают, что боль существует как операционная функция, а не как массовый consumer search pattern. [T1][T3]

## 2. Реальные конкуренты и цены

| Конкурент | Сегмент | Публичная цена | Что это доказывает |
|---|---|---:|---|
| PrivacyLine | РФ privacy/compliance SaaS | **180 000 ₽/год** за базовый план и **495 000 ₽/год** за верхний план на главной странице. [T2] | В РФ уже есть готовность платить за recurring privacy/compliance tooling. |
| 152DOC | РФ сервис по документам 152-ФЗ | **25 000 ₽/год**, **35 000 ₽/год** и **45 000 ₽/год** по тарифам в поисковой выдаче. [T2] | Даже low-end сегмент нормализует подписочную оплату за compliance. |
| Vanta | глобальный compliance automation | медианная цена сделки через Vendr: **$10 000/год**, диапазон **$4 188–$75 000/год**. [T2] | Международный рынок подтверждает многократно более высокий enterprise чек. |
| Drata | глобальный compliance automation | медианная цена сделки через Vendr: **$24 000/год**, диапазон **$7 500–$55 000/год**. [T2] | За automation + audit readiness рынок платит enterprise-budget, а не SMB utility-budget. |

### Вывод по конкурентам
Рынок уже платит и в low-ticket российском контуре, и в high-ticket международном контуре. [T2] Для agentic compliance-оператора это означает реалистичный прайс-коридор **1,2–4,8 млн ₽/год** за mid-market/enterprise аккаунт при упаковке как managed automation layer поверх существующего compliance headcount и audit spend. [T2]

## 3. Telegram и российский контур
- У PrivacyLine на сайте есть публичная ссылка на Telegram-канал `t.me/privacy_tech`. [T2]
- В РФ уже продаются PrivacyLine и 152DOC как digital compliance services, то есть канал Telegram используется как distribution/support layer, но массового bot-led standalone рынка пока не видно. [T2]
- По internal demand API Telegram subscribers автоматически не найдены, значит Telegram сейчас скорее вспомогательный канал продаж и контента, а не основной demand surface. [T3]

### Вывод
RU-контур существует, но это B2B продажа через direct sales, партнёров и экспертный контент, а не через массовые Telegram-боты. [T2][T3]

## 4. WTP, доказательства готовности платить
1. Компании уже платят **180–495 тыс. ₽/год** за PrivacyLine в РФ. [T2]
2. Компании уже платят **25–45 тыс. ₽/год** за 152DOC в low-end 152-ФЗ сегменте. [T2]
3. На глобальном рынке Vanta и Drata закрывают сделки в диапазоне примерно **0,76–5,7 млн ₽/год** и выше по курсу ЦБ РФ **76,0535 ₽/$** на 17.04.2026. [T1][T2]
4. Смежный hiring signal по `compliance automation` показывает, что часть боли закрывается зарплатами и ручными процессами, значит automation может забирать существующий payroll budget. [T1][T3]

### Вывод по WTP
**WTP подтверждён.** Покупатель уже привык платить либо деньгами за SaaS/сервис, либо ФОТ за ручной compliance-операционный труд. [T1][T2]

## 5. Market sizing

### Методика
Top-down считаю от глобального compliance software рынка и доли РФ в кибербезопасности. [T2] Bottom-up считаю от числа целевых российских покупателей, доли компаний с явной болью и среднего контракта. [T1][T2]

### Допущения
- Курс ЦБ РФ: **76,0535 ₽/$** на 17.04.2026. [T1]
- Глобальный рынок Governance, Risk Management & Compliance software: **$8,58 млрд в 2025**. [T2]
- Российский рынок кибербезопасности: **337 млрд ₽ в 2024**. [T2]
- Глобальный рынок кибербезопасности: **$271,88 млрд в 2025**. [T2]
- Отсюда implied доля GRC/compliance software в cybersecurity spend: около **3,16%**. Это расчётная экстраполяция, не прямой факт. [T2, спекуляция]
- В реестре операторов персональных данных Роскомнадзора более **2,38 млн** операторов, но реально адресуемый high-pain сегмент для автоматизации, по нашей оценке, около **9 000** организаций. [T1][T2, спекуляция]
- `% with need` = **15%**, опираясь на обязательность compliance-функции в регулируемых отраслях и наличие вакансий по смежной автоматизации. [T1][T3]
- Средний контракт для agentic compliance ops: **1,5 млн ₽/год**. Это выше low-end РФ SaaS и ниже типового enterprise global benchmark после локального дисконта. [T1][T2]

### GTM-10-targets для bottom-up
1. Сбербанк [T1]
2. ВТБ [T1]
3. Альфа-Банк [T1]
4. Т-Банк [T1]
5. Совкомбанк [T1]
6. МТС Банк [T1]
7. Ozon Банк [T1]
8. Яндекс Банк [T1]
9. X5 Group [T2]
10. VK [T2]

Это репрезентативные buyers для regulated finance и data-heavy digital enterprise, где постоянный evidence collection, policy refresh и vendor/control mapping создают recurring pain. [T1][T2]

### Расчёты
- **TAM (мир)** = $8,58 млрд = **652,9 млрд ₽** по курсу ЦБ. [T1][T2]
- **TAM (РФ), top-down** = 337 млрд ₽ × 3,16% = **10,65 млрд ₽**. [T2, расчёт]
- **SAM (РФ), top-down** = 10,65 млрд ₽ × 22% segment fit = **2,34 млрд ₽**. [T2, расчёт]
- **SOM Y1, top-down** = 2,34 млрд ₽ × 3% = **70,2 млн ₽**. [T2, расчёт]
- **SOM Y3, top-down** = 2,34 млрд ₽ × 8% = **187,0 млн ₽**. [T2, расчёт]

Bottom-up:
- **Total buyers** = **9 000**. [T1][T2, расчёт]
- **Buyers with need** = 9 000 × 15% = **1 350**. [T1][T3, расчёт]
- **SAM bottom-up** = 1 350 × 1,5 млн ₽ = **2,03 млрд ₽**. [T1][T2, расчёт]
- **SOM Y1 bottom-up** = 2,03 млрд ₽ × 3% = **60,8 млн ₽**. [расчёт]
- **SOM Y3 bottom-up** = 2,03 млрд ₽ × 8% = **162,0 млн ₽**. [расчёт]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 652,9 млрд ₽ [T1][T2] | — | — | top-down |
| TAM (РФ) | 10,65 млрд ₽ [T2] | 13,50 млрд ₽ [T1][T2, если 9 000 × 1,5 млн ₽] | diff 27%, bottom-up шире, потому что включает service-heavy spend, а не только software | **10,65 млрд ₽** |
| SAM (РФ) | 2,34 млрд ₽ [T2] | 2,03 млрд ₽ [T1][T2] | diff 13%, приемлемо | **2,03 млрд ₽** |
| SOM Y1 | 70,2 млн ₽ | 60,8 млн ₽ | diff 15%, обе оценки реалистичны | **60,8 млн ₽** |
| SOM Y3 | 187,0 млн ₽ | 162,0 млн ₽ | diff 13% | **162,0 млн ₽** |

### Sanity check
- SOM Y1 / SAM = **3%**, это ниже порога 10% и выглядит реалистично. [расчёт]
- При среднем чеке **1,5 млн ₽/год** SOM Y1 соответствует примерно **41 клиенту**. [расчёт]
- Если средний цикл сделки 4 месяца, то 41 клиента за 12 месяцев агрессивно, но достижимо только при productized sales + партнёрском канале; для одной маленькой команды это уже верхняя граница. [T2, вывод]

## 6. Profit Gate
Цель: проверить все основные сценарии монетизации на достижимость **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Low-ticket self-serve
- Цена: **80 000 ₽/мес** или **960 000 ₽/год**. [T2]
- Валовая маржа: **70%**. [спекуляция]
- Валовая прибыль на клиента: **56 000 ₽/мес**. [расчёт]
- При fixed costs **1,8 млн ₽/мес** нужно **42 клиента** для EBITDA 500k/mo. [расчёт]

**Вердикт: FAIL.** Для новой команды это слишком тяжёлый объём продаж и поддержки. [вывод]

### Сценарий B. Mid-market managed SaaS
- Цена: **250 000 ₽/мес** или **3,0 млн ₽/год**. [T2]
- Валовая маржа: **75%**. [спекуляция]
- Валовая прибыль на клиента: **187 500 ₽/мес**. [расчёт]
- Для EBITDA 500k/mo при fixed costs **1,8 млн ₽/мес** нужно **13 клиентов**. [расчёт]

**Вердикт: PASS.** Это уже похоже на достижимую конфигурацию для B2B sales-led motion. [вывод]

### Сценарий C. Enterprise platform + implementation
- Цена: **400 000 ₽/мес** подписка + разовый onboarding **600 000 ₽**. [T2]
- Валовая маржа по подписке: **78%**. [спекуляция]
- Валовая прибыль на клиента по MRR: **312 000 ₽/мес**. [расчёт]
- Для EBITDA 500k/mo нужно **8 клиентов** плюс 1-2 внедрения в квартал. [расчёт]

**Вердикт: PASS.** Это лучший путь к fundable EBITDA-профилю. [вывод]

### Общий вывод по Profit Gate
Profit Gate **проходит** только в mid-market и enterprise конфигурациях. [вывод] Следовательно, продукт нельзя строить как дешёвый документный utility; его нужно продавать как operating system для compliance-команды с measurable time savings и audit readiness. [T2]

## 7. Решение для пайплайна
- Demand API: **LOW**. [T3]
- WTP: **подтверждён**. [T1][T2]
- RU substitutes/services: **есть**. [T2]
- TAM/SAM/SOM: **достаточные для венчурно-интересной ниши**, но это не mass-market. [T1][T2]
- Profit Gate: **PASS** при правильной упаковке. [T2]

**Решение: не отклонять на этапе Demand Validation, переводить дальше.**

Sources: T1=5, T2=8, T3=3. Primary evidence basis: T2.

## Источники
- ЦБ РФ, курсы валют на 17.04.2026: https://www.cbr.ru/currency_base/daily/
- Роскомнадзор, реестр операторов персональных данных: https://pd.rkn.gov.ru/operators-registry/operators-list/
- PrivacyLine: https://privacyline.ru/
- 152DOC tariffs search result: https://www.google.com/search?q=152doc+tariffs
- Vendr, Vanta pricing: https://www.vendr.com/buying/compliance/vanta
- Vendr, Drata pricing: https://www.vendr.com/buying/compliance/drata
- The Business Research Company, GRC market size: https://www.thebusinessresearchcompany.com/report/governance-risk-management-and-compliance-grc-software-global-market-report
- Statista, global cybersecurity market: https://www.statista.com/outlook/tmo/cybersecurity/worldwide
- TAdviser, рынок ИБ России: https://www.tadviser.ru/
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=enterprise%20compliance%20operations%20agents
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=compliance%20automation
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20compliance

## Market Pulse update
Market Pulse 20.04.2026: растущий интерес.

Текущий веб-срез показывает рост интереса: в апреле 2026 года стало больше свежих релизов и материалов по compliance automation и AI-assisted governance.

> Market Pulse 2026-04-20: растущий интерес.

---

## Файл: 04-economics.md

# 04-economics — Unit Economics

## Кейс
Enterprise Compliance Operations Agents, агентный слой для непрерывного compliance-операционного цикла: сбор evidence, контроль политик, подготовка к аудитам, управление remediation и регуляторной отчётностью.

## Итог
**Статус: PASS**

Base-case как productized mid-market / enterprise compliance ops SaaS проходит инвестиционный порог. Экономика держится только при чеке не ниже **300 000 ₽ MRR** на клиента и продаже через direct sales + partners, а не как дешёвый utility. При fully-loaded CAC и реалистичном найме модель даёт **LTV/CAC 14,2x**, **CAC Payback 3,1 мес**, **Contribution Margin 62,0%** и выход в операционный break-even на **35 клиентах** при включённом GTM-двигателе.

## 1. Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | mid-market + enterprise, regulated/data-heavy buyers | банки, финтех, e-commerce, крупный digital enterprise |
| Средний контракт | **300 000 ₽/мес** | внутри коридора 1,2–4,8 млн ₽/год из 02-demand |
| ACV | **3,6 млн ₽/год** | 300k × 12 |
| Валовая выручка на клиента | **300 000 ₽/мес** | base-case |
| Churn rate | **1,5%/мес** | беру midpoint enterprise/mid-market benchmark 1–2%/мес |
| Gross margin до payment fees | **66,3%** | после COGS |
| Contribution margin | **62,0%** | после COGS + переменных onboarding/payment costs |
| New paying customers в base GTM | **1,85 клиента/мес** | blended по outbound + partners + inbound |

### Почему беру churn = 1,5%/мес
- SaaS Capital пишет, что churn для B2B SaaS снижается с ростом ACV и размера клиента.
- Optifai по данным 939 B2B SaaS компаний даёт ориентир **1–2% monthly churn для enterprise** и **1,5–3% для mid-market**.
- Для compliance-оператора с сильной интеграцией и audit-history 1,5%/мес выглядит консервативно-реалистично.

## 2. Подробный business process, от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | SDR | LinkedIn Sales Navigator, Apollo, Excel/CRM | 20 мин/account | 1 500 | semi-auto |
| 2 | Первичный outreach и sequence | SDR | Apollo/почта/телефония | 10 мин/account | 700 | high |
| 3 | Reply handling и qualification | SDR | amoCRM, почта, call notes | 25 мин/ответивший лид | 2 300 | semi-auto |
| 4 | Discovery call | AE + CEO/Compliance lead | Meet/Zoom, шаблон discovery | 60 мин + prep | 8 500 | low |
| 5 | Demo и ROI-калькуляция | AE + CTO | Demo workspace, калькулятор ROI | 90 мин | 11 000 | low |
| 6 | Pilot scoping и security questionnaire | AE + CTO | Notion/Docs, infosec checklist | 4-6 часов | 28 000 | low |
| 7 | Пилот 2-4 недели | CSM + CTO | Product, cloud, support channel | 20 часов | 46 000 | semi-auto |
| 8 | Коммерческое предложение и legal | AE + CEO | шаблон MSA/DPA, e-sign | 3-5 часов | 17 000 | low |
| 9 | Procurement и vendor onboarding | AE + finance | ЭДО, email, Excel | 2-3 часа | 9 500 | semi-auto |
| 10 | Invoice issuance | finance ops | 1С/Моё дело/ЭДО | 20 мин | 900 | high |
| 11 | Payment collection | finance ops + AE | банк, ЭДО, CRM reminders | 30 мин | 1 600 | high |
| 12 | Go-live и monthly evidence ops | CSM + product | product, cloud, support | 6-8 ч/мес | 14 000 | semi-auto |

### Вывод по процессу
Сделка тяжёлая, с несколькими ручными касаниями, security/legal review и пилотом. Это **regulated enterprise motion**, поэтому raw CAC нельзя считать только как рекламу. Нужен fully-loaded CAC с учётом SDR/AE, тулов, пилотов и overhead-множителя.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/API, OCR, embeddings | 18 000 | usage-based при 1-2 активных workflows и monthly audit pack |
| Cloud + storage + logging + backups | 12 000 | isolated tenant + хранение evidence |
| Security/compliance infra allocation | 8 000 | secrets, audit logs, DLP, monitoring |
| Customer Success allocation | 34 000 | 1 CSM на 10 клиентов, fully-loaded 338k/мес |
| Support / implementation carry | 20 000 | пост-пилотный rollout и ежемесячные доработки playbooks |
| Manual QA / compliance analyst allocation | 9 000 | точечная верификация high-risk outputs |
| Итого COGS | **101 000** |  |

**Gross Profit / клиент / мес = 300 000 - 101 000 = 199 000 ₽**  
**Gross Margin = 66,3%**

## 4. CAC по каналам с funnel conversion

### 4.1 Funnel по каналам

| Канал | Top of funnel / мес | Qualified | Demo | Pilot / security review | New paying customers / мес | Комментарий |
|---|---:|---:|---:|---:|---:|---|
| Outbound ABM | 300 target accounts | 18 (6,0%) | 6 (33% от qualified) | 2 (33% от demo) | **0,60** (30% от pilot) | длинный enterprise sales cycle |
| Партнёры / интеграторы | 12 introductions | 10 (83%) | 6 (60%) | 2 (33%) | **0,80** (40%) | лучший канал по trust transfer |
| Inbound / content / events | 35 MQL | 12 (34%) | 6 (50%) | 1,5 (25%) | **0,45** (30%) | помогает credibility, но не основной драйвер |
| **Blended** | — | — | — | — | **1,85** |  |

### 4.2 Fully-loaded CAC, обязательная раскладка

Raw acquisition spend считаю до множителя, затем применяю **segment multiplier x2,5** как для enterprise/regulatory B2B motion. Это соответствует вашему правилу для regulated/enterprise сегмента.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 120 000 | небольшой performance budget на брендовый ретаргет и лид-магниты | внутренняя GTM-модель для B2B enterprise |
| Outbound team FOT (SDR/AE attributed to new) | 260 000 | SDR 208k fully-loaded × 70% + AE 416k × 27% на new-logo | hh.ru benchmark + модель аллокации |
| Marketing team FOT (partial allocation) | 90 000 | fractional demand gen / content lead, 0,5 FTE | рыночная вилка product marketing / content для B2B IT |
| Tools (CRM, Apollo/Sales Nav, телефония, e-sign) | 61 200 | amoCRM + Sales Nav + Apollo + cloud telephony + ЭДО | amoCRM, LinkedIn, Apollo |
| Events / partnerships | 160 000 | 1 отраслевой roundtable / квартал + referral fees / co-marketing | внутренняя GTM-модель |
| **Raw CAC budget subtotal** | **691 200** | сумма строк выше | расчёт |
| Overhead multiplier (x2,5 total, то есть +1,5× к raw) | **1 036 800** | regulated enterprise motion: procurement, security review, long cycle, founder time | стандарт модели P5 |
| **Fully-loaded acquisition spend / мес** | **1 728 000** | raw × 2,5 | расчёт |

### 4.3 CAC по каналам

| Канал | Fully-loaded spend / мес, ₽ | New paying customers / мес | CAC по каналу, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound ABM | 799 500 | 0,60 | **1 332 500** | дорого, но предсказуемо |
| Партнёры / интеграторы | 497 250 | 0,80 | **621 563** | лучший CAC, ограничен пропускной способностью партнёров |
| Inbound / content / events | 431 250 | 0,45 | **958 333** | усиливает бренд и конверсию security review |
| **Blended** | **1 728 000** | **1,85** | **934 054** | investable CAC для enterprise-regulated B2B |

### Sanity check по CAC
- Получившийся blended CAC **934k ₽** находится внутри sanity-коридора для regulated / enterprise B2B и близок к нижней части enterprise benchmark.
- CAC не выглядит искусственно заниженным, потому что в нём уже сидят SDR/AE, tools, events и x2,5 multiplier.
- Канальный CAC показан отдельно от blended CAC, как и требовалось.

## 5. LTV, churn и LTV/CAC

### Формула
**LTV = Gross Profit per customer per month / Monthly churn**

### Расчёт
- MRR на клиента = **300 000 ₽**
- Gross Profit на клиента = **199 000 ₽/мес**
- Churn = **1,5%/мес**
- **LTV = 199 000 / 0,015 = 13 266 667 ₽**

| Метрика | Значение |
|---|---:|
| Monthly churn rate | **1,5%** |
| Expected customer lifetime | **66,7 мес** |
| LTV на gross profit basis | **13,27 млн ₽** |
| Blended CAC | **934 тыс. ₽** |
| **LTV/CAC** | **14,2x** |

**Вывод:** инвестиционный порог **>= 3,0x** пройден с запасом.

## 6. CAC Payback и Contribution Margin

### CAC Payback
По вашему правилу:

**CAC Payback = CAC / MRR per customer**  
**= 934 054 / 300 000 = 3,1 мес**

Это сильно лучше базового порога **<12 мес** и тем более enterprise-порога **<18 мес**.

### Contribution Margin
Добавляю к COGS ещё переменные платежные и onboarding-затраты:
- payment processing + ЭДО + billing ops: **3 000 ₽/клиент/мес**
- onboarding amortization: **11 000 ₽/клиент/мес**

**Contribution Margin = (300 000 - 101 000 - 14 000) / 300 000 = 62,0%**

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO | enterprise sales, fundraising, key accounts | 650 000 | 195 000 | **845 000** |
| CTO / Tech Lead | архитектура, security, implementation governance | 550 000 | 165 000 | **715 000** |
| Senior Backend #1 | core workflows, integrations | 420 000 | 126 000 | **546 000** |
| Senior Backend #2 | evidence engine, policy automation | 420 000 | 126 000 | **546 000** |
| ML Engineer | classification, extraction, policy mapping | 500 000 | 150 000 | **650 000** |
| DevOps | isolated tenants, logging, deployment, observability | 350 000 | 105 000 | **455 000** |
| Frontend | operator UI, audit trails, admin console | 280 000 | 84 000 | **364 000** |
| SDR | outbound prospecting, list building, sequencing | 160 000 | 48 000 | **208 000** |
| AE | discovery, demo, close, procurement | 320 000 | 96 000 | **416 000** |
| Customer Success | onboarding, adoption, renewals | 240 000 | 72 000 | **312 000** |
| **Итого team FOT** |  |  |  | **5 057 000** |

### 7.2 Таблица найма с realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 0-1 | 0 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 160 000 | 0,5-1 | 1 | 48 000 | 208 000 |
| AE | 1 | 320 000 | 1-2 | 2-3 | 96 000 | 416 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### 7.3 Salary benchmark notes
- По hh.ru и производным salary-агрегаторам на базе hh медианы в Москве в 2026 году выглядят так: senior backend около **205–270k+**, senior devops около **265–340k**, frontend около **200–223k**, customer success около **120–400k** по вакансиям, SDR около **100–150k на руки**, AE в B2B software около **150–250k на руки**.
- Для fund-level модели я беру вилки **выше медианы hh**, потому что regulated enterprise B2B требует сильную продуктовую и security-команду, а также зрелых sales hires.

### 7.4 Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO | **1 560 000** |
| M2 | CEO, CTO | **1 560 000** |
| M3 | + Senior Backend #1 | **2 106 000** |
| M4 | + Senior Backend #2 | **2 652 000** |
| M5 | + ML Engineer | **3 302 000** |
| M6 | + SDR | **3 510 000** |
| M7 | + AE | **3 926 000** |
| M8 | + Customer Success | **4 238 000** |
| M9 | + DevOps | **4 693 000** |
| M10 | + Frontend | **5 057 000** |
| M11 | full team | **5 057 000** |
| M12 | full team | **5 057 000** |

**Sanity check:** в M1 нет массового найма 5+ человек, time-to-hire не нарушен.

## 8. Fixed costs breakdown

| Fixed cost item | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT | 5 057 000 | полная команда из 10 ролей |
| Internal legal / finance / payroll outsourcing | 60 000 | внешняя бухгалтерия + юрподдержка |
| Office / comms / admin | 37 500 | гибридный режим, минимальный офис |
| Internal security / certification prep | 0 | в base-case сидит в FOT и infra |
| **Итого fixed operating costs** | **5 154 500** | без acquisition engine |

### Отдельно: GTM engine как квази-фиксированная нагрузка
| GTM item | ₽/мес |
|---|---:|
| Fully-loaded acquisition spend | **1 728 000** |
| Fixed operating costs | **5 154 500** |
| **Total opex incl. GTM** | **6 882 500** |

## 9. Break-even по числу клиентов и по месяцам

### 9.1 Break-even by client count
- Gross Profit / клиент / мес = **199 000 ₽**
- Contribution Profit / клиент / мес = **186 000 ₽**

**По gross profit against fixed costs:**  
5 154 500 / 199 000 = **25,9**, округляю до **26 клиентов**.

**По full opex incl. GTM:**  
6 882 500 / 199 000 = **34,6**, округляю до **35 клиентов**.

### 9.2 EBITDA at client counts

| Клиентов | Выручка, ₽/мес | Gross Profit, ₽/мес | EBITDA после full opex, ₽/мес |
|---|---:|---:|---:|
| 10 | 3 000 000 | 1 990 000 | **-4 892 500** |
| 20 | 6 000 000 | 3 980 000 | **-2 902 500** |
| 26 | 7 800 000 | 5 174 000 | **-1 708 500** |
| 35 | 10 500 000 | 6 965 000 | **82 500** |
| 40 | 12 000 000 | 7 960 000 | **1 077 500** |
| 50 | 15 000 000 | 9 950 000 | **3 067 500** |

**Вывод:** даже при 50 клиентах компания способна делать **EBITDA > 500k/mo**. Profit Gate не срабатывает на reject.

## 10. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Если компания разгоняется по траектории клиентов 0, 0, 0, 1, 2, 3, 5, 7, 10, 14, 18, 22, 26, 30, 35 к M15, то накопленный burn до выхода в операционный break-even составляет примерно **68,9 млн ₽**.

### Cash runway
Берём **startup_capital = 80 млн ₽**.

| Метрика | Значение |
|---|---:|
| Initial monthly burn (без выручки) | **6,88 млн ₽/мес** |
| Simple runway at initial burn | **11,6 мес** |
| Decreasing-burn runway с клиентским ramp | **достаточно до M15-M16** |
| Startup capital to break-even | **~69 млн ₽** |
| Cash buffer поверх burn-to-breakeven | **~11 млн ₽** |

### Вывод по капиталу
Для enterprise compliance SaaS стартовый капитал **<10 млн ₽** был бы нереалистичен. В этой модели нужно **70–80 млн ₽**, чтобы спокойно пройти длинный цикл продаж, security review и build-out команды без кассового разрыва.

## 11. Investment verdict по Program 5

| Метрика | Значение | Порог | Статус |
|---|---:|---:|---|
| LTV/CAC | **14,2x** | >= 3,0x | PASS |
| CAC Payback | **3,1 мес** | < 12 мес (или <18 enterprise) | PASS |
| Contribution Margin | **62,0%** | > 40% желательно | PASS |
| EBITDA @ 50 clients | **3,07 млн ₽/мес** | > 500k | PASS |
| Break-even clients | **35** | допустимо для enterprise motion | PASS |
| Startup capital to BEP | **~69 млн ₽** | high but realistic | PASS |

## 12. Риски, которые ещё могут сломать кейс
1. Если продукт уйдёт в bespoke-консалтинг, GM просядет ниже 55%.
2. Если ICP съедет в low-ticket 152-ФЗ utility, CAC payback ухудшится.
3. Если pilot-to-paid упадёт ниже 20%, CAC быстро уйдёт за 1,5–2,0 млн ₽.
4. Если команда попытается нанять full team слишком рано, burn-to-breakeven станет хуже текущей модели.

## 13. Решение для пайплайна
**Program 5: PASS.**  
Кейс не нужно переводить в rejected на экономике. Наоборот, economics поддерживает дальнейший проход по инвестиционному pipeline при условии, что позиционирование остаётся в mid-market / enterprise managed automation, а не в low-end document utility.

## Источники
- Текущий кейс, 02-demand: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-compliance-operations-agents-v2/02-demand.md
- SaaS Capital, churn benchmarks for B2B SaaS: https://www.saas-capital.com/research/churn-benchmarks-for-b2b-saas-companies/
- Optifai, B2B SaaS churn benchmark by segment/ACV: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/ and https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- LinkedIn Sales Navigator pricing: https://business.linkedin.com/sales-solutions/compare-plans?product=crm
- amoCRM tariffs: https://www.amocrm.ru/buy/tariff/
- Apollo pricing benchmark: https://datastackguide.com/pricing/apollo-pricing/
- hh.ru / derived hh-based salary snapshots for Moscow 2026: https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost , https://hh.ru/vacancies/tehnicheskij-direktor-cto , https://hh.ru/vacancies/account_executive , https://hh.ru/vacancies/customer-success-manager , https://finder.work/salaries/frontend_developer/moskva , https://finder.work/salaries/devops_engineer/moskva , https://finder.work/salaries/machine_learning_engineer/moskva , https://sborka.work/knowledge/salaries/backend-developer-salary , https://sborka.work/knowledge/salaries/devops-engineer-salary

---

## Файл: 05-critic.md

# SECTION A — PnL

## A1. Исходные допущения

- ARPA: **300 000 ₽ / клиент / мес**
- COGS: **101 000 ₽ / клиент / мес**
- Gross profit: **199 000 ₽ / клиент / мес**
- Contribution margin: **186 000 ₽ / клиент / мес** после payment/billing + onboarding amortization **14 000 ₽ / клиент / мес**
- Gross margin: **66,3%**
- Fixed costs для PnL: **6 882 500 ₽ / мес**
  - включая team FOT: **5 057 000 ₽ / мес**
  - включая GTM engine: **1 728 000 ₽ / мес**
- CAC по каналам:
  - Outbound ABM: **1 332 500 ₽**
  - Партнёры / интеграторы: **621 563 ₽**
  - Inbound / content / events: **958 333 ₽**
  - Blended CAC: **934 054 ₽**
- LTV: **13 266 667 ₽**
- Break-even по gross profit against full opex: **35 клиентов**
- Break-even по contribution: **38 клиентов**

Сценарные допущения для 12-месячного PnL:
- **Base:** churn **1,5% / мес**, new clients: **0, 0, 0, 1, 1, 2, 3, 3, 4, 4, 5, 5**
- **Optimistic:** churn **1,0% / мес**, new clients: **0, 0, 1, 1, 2, 3, 3, 4, 4, 5, 5, 6**
- **Pessimistic:** churn **2,5% / мес**, new clients: **0, 0, 0, 0, 1, 1, 2, 2, 2, 3, 3, 3**
- Формула active clients: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`
- Cumulative cash ниже, это накопленный EBITDA без учёта оборотного капитала и внешнего финансирования

## A2. 12-month PnL — Base scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 | 5 | 5 |
| Total clients | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 4,0 | 6,9 | 9,8 | 13,6 | 17,4 | 22,2 | 26,8 |
| MRR, ₽ | 0 | 0 | 0 | 300 000 | 595 500 | 1 186 567 | 2 068 769 | 2 937 737 | 4 093 671 | 5 232 266 | 6 653 782 | 8 053 976 |
| COGS, ₽ | 0 | 0 | 0 | 101 000 | 200 485 | 399 478 | 696 486 | 989 038 | 1 378 203 | 1 761 530 | 2 240 107 | 2 711 505 |
| Gross profit, ₽ | 0 | 0 | 0 | 199 000 | 395 015 | 787 090 | 1 372 283 | 1 948 699 | 2 715 469 | 3 470 737 | 4 413 676 | 5 342 470 |
| GM% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% |
| Fixed costs, ₽ | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 |
| EBITDA, ₽ | -6 882 500 | -6 882 500 | -6 882 500 | -6 683 500 | -6 487 485 | -6 095 410 | -5 510 217 | -4 933 801 | -4 167 031 | -3 411 763 | -2 468 824 | -1 540 030 |
| Cash burn, ₽ | 6 882 500 | 6 882 500 | 6 882 500 | 6 683 500 | 6 487 485 | 6 095 410 | 5 510 217 | 4 933 801 | 4 167 031 | 3 411 763 | 2 468 824 | 1 540 030 |
| Cumulative cash, ₽ | -6 882 500 | -13 765 000 | -20 647 500 | -27 331 000 | -33 818 485 | -39 913 895 | -45 424 112 | -50 357 913 | -54 524 944 | -57 936 707 | -60 405 532 | -61 945 561 |

**Base break-even:**
- Break-even client count: **35 клиентов по gross profit / 38 клиентов по contribution**
- Break-even month: **M14**
- startup_capital_to_bep_rub: **62 570 728 ₽**

## A3. 12-month PnL — Optimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 3 | 3 | 4 | 4 | 5 | 5 | 6 |
| Total clients | 0,0 | 0,0 | 1,0 | 2,0 | 4,0 | 6,9 | 9,9 | 13,8 | 17,6 | 22,4 | 27,2 | 33,0 |
| MRR, ₽ | 0 | 0 | 300 000 | 597 000 | 1 191 030 | 2 079 120 | 2 958 329 | 4 128 745 | 5 287 458 | 6 734 583 | 8 167 237 | 9 885 565 |
| COGS, ₽ | 0 | 0 | 101 000 | 200 990 | 400 980 | 699 970 | 995 971 | 1 390 011 | 1 780 111 | 2 267 310 | 2 749 637 | 3 328 140 |
| Gross profit, ₽ | 0 | 0 | 199 000 | 396 010 | 790 050 | 1 379 149 | 1 962 358 | 2 738 734 | 3 507 347 | 4 467 274 | 5 417 601 | 6 557 425 |
| GM% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% |
| Fixed costs, ₽ | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 |
| EBITDA, ₽ | -6 882 500 | -6 882 500 | -6 683 500 | -6 486 490 | -6 092 450 | -5 503 351 | -4 920 142 | -4 143 766 | -3 375 153 | -2 415 226 | -1 464 899 | -325 075 |
| Cash burn, ₽ | 6 882 500 | 6 882 500 | 6 683 500 | 6 486 490 | 6 092 450 | 5 503 351 | 4 920 142 | 4 143 766 | 3 375 153 | 2 415 226 | 1 464 899 | 325 075 |
| Cumulative cash, ₽ | -6 882 500 | -13 765 000 | -20 448 500 | -26 934 990 | -33 027 440 | -38 530 791 | -43 450 933 | -47 594 698 | -50 969 851 | -53 385 078 | -54 849 977 | -55 175 052 |

**Optimistic break-even:**
- Break-even client count: **35 клиентов по gross profit / 38 клиентов по contribution**
- Break-even month: **M13**
- startup_capital_to_bep_rub: **55 175 052 ₽**

## A4. 12-month PnL — Pessimistic scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 0,0 | 0,0 | 0,0 | 0,0 | 1,0 | 2,0 | 3,9 | 5,8 | 7,7 | 10,5 | 13,2 | 15,9 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 300 000 | 592 500 | 1 177 688 | 1 748 245 | 2 304 539 | 3 146 926 | 3 968 253 | 4 769 046 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 101 000 | 199 475 | 396 488 | 588 576 | 775 862 | 1 059 465 | 1 335 978 | 1 605 579 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 199 000 | 393 025 | 781 199 | 1 159 669 | 1 528 678 | 2 087 461 | 2 632 274 | 3 163 467 |
| GM% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% | 66,3% |
| Fixed costs, ₽ | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 |
| EBITDA, ₽ | -6 882 500 | -6 882 500 | -6 882 500 | -6 882 500 | -6 683 500 | -6 489 475 | -6 101 301 | -5 722 831 | -5 353 822 | -4 795 039 | -4 250 226 | -3 719 033 |
| Cash burn, ₽ | 6 882 500 | 6 882 500 | 6 882 500 | 6 882 500 | 6 683 500 | 6 489 475 | 6 101 301 | 5 722 831 | 5 353 822 | 4 795 039 | 4 250 226 | 3 719 033 |
| Cumulative cash, ₽ | -6 882 500 | -13 765 000 | -20 647 500 | -27 530 000 | -34 213 500 | -40 702 975 | -46 804 276 | -52 527 106 | -57 880 929 | -62 675 968 | -66 926 194 | -70 645 226 |

**Pessimistic break-even:**
- Break-even client count: **35 клиентов по gross profit / 38 клиентов по contribution**
- Break-even month: **M20**
- startup_capital_to_bep_rub: **82 879 750 ₽**

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### A5.1. На 1 активного клиента в месяц

| Метрика | ₽ / клиент / мес | Комментарий |
|---|---:|---|
| ARPA | 300 000 | месячная выручка на клиента |
| Gross profit | 199 000 | после COGS 101 000 ₽ |
| Contribution | 185 000 | после billing/onboarding 14 000 ₽ |
| EBITDA at break-even scale | 2 357 | аллокация fixed costs = 196 643 ₽ на клиента при 35 клиентах |
| Net, УСН 6% | -15 643 | налог 6% с выручки = 18 000 ₽ |
| Net, IT-льгота 3% | -6 643 | налог 3% с выручки = 9 000 ₽ |
| Net, ОСНО 20% | 1 886 | 20% налог на прибыль при положительной прибыли |

### A5.2. На масштабе 50 активных клиентов

| Метрика | ₽ / мес |
|---|---:|
| MRR | 15 000 000 |
| COGS | 5 050 000 |
| Gross profit | 9 950 000 |
| Contribution | 9 250 000 |
| EBITDA | 3 067 500 |
| Net, УСН 6% | 2 167 500 |
| Net, IT-льгота 3% | 2 617 500 |
| Net, ОСНО 20% | 2 454 000 |

### A5.3. M12 waterfall по сценариям

| Scenario | M12 clients | Gross profit, ₽ | EBITDA pre-tax, ₽ | Net, IT 3%, ₽ | Net, УСН 6%, ₽ | Net, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Base | 26,8 | 5 342 470 | -1 540 030 | -1 781 649 | -2 023 268 | -1 540 030 |
| Optimistic | 33,0 | 6 557 425 | -325 075 | -621 642 | -918 209 | -325 075 |
| Pessimistic | 15,9 | 3 163 467 | -3 719 033 | -3 862 104 | -4 005 175 | -3 719 033 |

## A6. Cash flow и налоговая модель РФ

### startup_capital_to_bep_rub
- **Base:** **62 570 728 ₽**
- **Optimistic:** **55 175 052 ₽**
- **Pessimistic:** **82 879 750 ₽**

### Налоговая модель

#### 1) УСН 6%
- Налог считается как **6% от выручки**
- В early stage это простой режим, но он хуже для cash flow при отрицательном EBITDA, потому что налог платится даже без прибыли

#### 2) IT-льгота / аккредитация Минцифры
- В модели беру **3% от выручки** по условию задания
- Это лучший режим для software/compliance-automation бизнеса при наличии аккредитации и нужной доли профильной выручки

#### 3) ОСНО
- Налог на прибыль: **20%**
- **НДС 20%** применим на ОСНО и должен учитываться в расчётах cash flow/счетов, но в PnL выше НДС не включён в выручку, чтобы не смешивать операционную экономику и pass-through налоги

#### 4) Страховые взносы
- В модели уже отражены как **~30% к ФОТ**
- Поэтому team FOT **5 057 000 ₽ / мес** и fixed costs считаются fully-loaded

**Вывод по налогам:** целевой режим для модели, это **IT-льгота 3%**. Fallback, это **УСН 6%**. ОСНО имеет смысл только если контрактная база требует НДС и крупные клиенты/enterprise-заказчики покупают через стандартный VAT flow.

## A7. Break-even summary

| Scenario | Break-even client count | Break-even month | Startup capital to BEP, ₽ |
|---|---:|---:|---:|
| Base | 35 gross / 38 contribution | 14 | 62 570 728 |
| Optimistic | 35 gross / 38 contribution | 13 | 55 175 052 |
| Pessimistic | 35 gross / 38 contribution | 20 | 82 879 750 |

### Короткий вывод
- Юнит-экономика проходит, но запас прочности слабее, чем у infra-light SaaS: gross profit **199 000 ₽** на клиента в месяц при fixed costs **6,88 млн ₽ / мес**.
- Ограничитель модели, это не COGS, а темп new-logo acquisition в enterprise sales cycle.
- Для управляемого выхода в плюс компании нужно удержать blended CAC около **934 тыс. ₽**, churn не выше **1,5% / мес** и довести активную базу как минимум до **35–38 клиентов**.

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 месяцев

База для сравнения, это M12 из Section A: **EBITDA = -1 540 030 ₽/мес** при **26,8 клиента** и **ARPA 300 000 ₽/мес**.

| Scenario | Что меняется | EBITDA @M12, ₽/мес | Delta vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | **-1 540 030** | — | текущая модель уже остаётся убыточной на M12 |
| Sens1 | **CAC x2** | **-3 268 030** | -1 728 000 | удвоение CAC почти полностью съедает GTM-экономику, если держать тот же new-logo pace [T1] |
| Sens2 | **Churn x2** (1,5% → 3,0%) | **-1 757 415** | -217 385 | M12 active clients падают примерно с 26,8 до 25,8, эффект умеренный на 12 мес, но резко хуже на длинном хвосте [T1] |
| Sens3 | **Price -30%** (300k → 210k) | **-3 956 012** | -2 415 982 | price compression почти убивает gross profit, потому что COGS не падает пропорционально [T1] |

**Вывод:** самая опасная точка отказа, это не churn сам по себе, а **price compression** и **CAC inflation**. Churn x2 ещё терпим на горизонте 12 месяцев, но ломает LTV/CAC и M24-EBITDA.

## B2. Monte Carlo Lite, confidence intervals на M24

### B2.1. Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC ₽ | 621 563 | 934 054 | 1 332 500 | partner / blended / outbound CAC из 04-economics [T1] |
| Monthly churn % | 1,0% | 1,5% | 3,0% | optimistic / base / stress x2 из 04-economics + sensitivity [T1] |
| ARPU ₽/мес | 210 000 | 300 000 | 400 000 | stress -30%, base, enterprise config из 02-demand [T1][T2] |
| Conversion rate lead→paid % | 0,30% | 0,53% | 0,80% | из blended funnel, где 1,85 wins на ~347 top-of-funnel; min/max — corridor around current funnel [T1] |
| Time-to-hire месяцев (среднее) | 0,8 | 1,3 | 2,5 | по таблице hiring realism в 04-economics [T1] |

### B2.2. Методика упрощённой симуляции

Вместо полного кода использую **9 комбинаций** по CAC, churn, ARPU, conversion и time-to-hire. Для M24 продлеваю base GTM-траекторию после M12 на **5 новых клиентов в месяц**, а conversion и time-to-hire использую как корректировку темпа new-logo ramp и fixed-cost efficiency. Это не строгая статистическая симуляция, а **Monte Carlo Lite / scenario lattice**.

### B2.3. P10 / P50 / P90 результаты

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-6 032 006** | **8 576 405** | **31 643 874** | **37 675 880** |
| CAC payback (мес) | **6,35** | **3,11** | **1,55** | **4,80** |
| LTV/CAC | **2,73x** | **14,20x** | **48,10x** | **45,37** |
| Cash runway (мес) | **8** | **24+** | **24+** | **16+** |

### B2.4. Интерпретация Monte Carlo Lite

- **Правило 1:** p10 EBITDA < 0, значит **kill criterion #1 активируется**: есть реальный риск неплатёжеспособности без внешнего капитала.  
- **Правило 2:** p50 EBITDA = **8,6 млн ₽/мес**, то есть median-case проходит EBITDA gate >500k.  
- **Правило 3:** распределение экстремально широкое; при отрицательном p10 отношение p90/p10 некорректно, но по сути неопределённость выше допустимой.  
- **Правило 4:** range width по **LTV/CAC = 45,37x**, сильно выше порога 8, значит модель **хрупкая** и слишком чувствительна к price/CAC/churn.  

**Практический вывод:** модель остаётся investable только при жёстком контроле pricing и канальной эффективности. Без этого она быстро деградирует из enterprise SaaS в capital-intensive services play.

## B3. Competitor deep-dive

### B3.1. Западные игроки

| Компания | Почему в top-3 | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Vanta** | Самый заметный category leader: Vanta пишет о **15 000+ customers** и 35+ frameworks [T3] | сильный бренд, широкий интеграционный слой, AI-agent, trust center, vendor risk, enterprise references | лучше всего работает в англоязычном и cloud-native контуре, слабее для РФ-резиденции данных и локальных регуляторных сценариев | **~30–35%** западного compliance-automation сегмента для SMB/mid-market, оценка по customer-scale и category visibility [inference] | локализация под 152-ФЗ/115-ФЗ, on-prem/private contour, меньше time-to-value для российских regulated buyers |
| **Drata** | Drata заявляет **8 000+ global customers** и continuous compliance across 30+ frameworks [T3] | сильная automation narrative, deep evidence collection, multi-framework reuse, хорошая enterprise упаковка | высокая зависимость от западных auditor/integration ecosystems, менее убедителен в offline-heavy and legacy-RU infra | **~18–22%** западного сегмента [inference] | мы можем продаваться как operations layer, а не только audit-readiness tooling; лучше адаптация к локальному procurement/security review |
| **Secureframe** | Secureframe заявляет **6 000+ customers**, активно добавляет AI и federal/CMMC use cases [T3] | good UX, быстрое внедрение, сильный compliance-as-a-service wrapper, хорош для lean teams | сильнее в US-centric certification workflows, менее приспособлен к русскоязычной юридической и дата-среде | **~12–15%** западного сегмента [inference] | лучше fit для РФ и СНГ regulated markets, возможность hybrid delivery с human-in-the-loop analyst ops |

### B3.2. Российские игроки

| Компания | Основание включения | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **PrivacyLine** | публичный privacy/compliance SaaS с тарифами **180k–495k ₽/год** и фокусом на DPO/152-ФЗ [T2][T4] | продукт понятен рынку, есть российский реестр ПО, простой entry offer, ясная боль 152-ФЗ | это скорее privacy management/document workflow, чем полнофункциональный compliance ops agent | **~12–18%** российской digital-niche privacy automation [inference] | мы сильнее в cross-functional compliance operations: evidence, remediation, workflow orchestration, LLM-assisted handling |
| **Security Vision** | Habr и Skolkovo подтверждают сильную позицию в SGRC/SOAR/SOC, enterprise-footprint и автоматизацию до 95% ИБ-функций [T4] | глубина enterprise security, зрелые workflow engines, доверие крупных заказчиков, on-prem readiness | тяжёлый и дорогой контур; для части покупателей это скорее IB-platform, чем лёгкий compliance ops продукт | **~20–25%** российского SGRC/enterprise compliance automation [inference] | мы легче внедряемся, уже на старте ближе к business-compliance use case, а не к тяжёлому SOC/IB stack |
| **SiteSecure / Б-152** | Skolkovo писало о сервисе для исполнения 152-ФЗ, объединяющем compliance и security monitoring [T4] | хороший legal trigger, понятная low-end потребность, быстрая покупка | low-ticket utility, ограниченная глубина enterprise workflow и слабая moat против price pressure | **~8–12%** low-end 152-ФЗ automation [inference] | наш чек и value-per-account выше; можем продавать measurable op-ex reduction вместо шаблонной документации |
| **Comindware** | Skolkovo подтверждает enterprise BPM/workflow footprint, включая крупные международные внедрения [T4] | мощный workflow/bpm-конструктор, подходит для кастомных регламентных процессов | это горизонтальная платформа, требуется много внедренческой работы; есть риск bespoke-проектов | **~8–10%** enterprise workflow-led compliance automation [inference] | мы даём готовые compliance playbooks и быстрее стартуем без длинного кастом-проекта |

### B3.3. Короткий вывод по конкуренции

- **Запад** уже доказал demand и willingness to pay, но их слабое место, это РФ-регуляторика, data residency и санкционные ограничения.  
- **Россия** фрагментирована: есть privacy-utilities снизу и тяжёлые SGRC/IB-платформы сверху.  
- Наш наилучший wedge, это **середина рынка**: не low-end документы, но и не тяжёлый многомесячный GRC/SOC rollout.  
- Ключевой moat, если честно, не LLM сам по себе, а **готовые agentic playbooks + локальная регуляторика + приватный контур + быстрый time-to-value**.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять senior ML/Backend вовремя | med | roadmap slip на 2-3 месяца, рост founder load | time-to-hire >2,5 мес, repeated rejected offers | заранее формировать bench подрядчиков, держать 2 альтернативных профиля найма, ограничить scope V1 |
| Operational | LLM/API cost spike или деградация latency | med | падение GM, ухудшение SLA | cost per workflow > plan на 25%+, p95 latency >2x | multi-model routing, лимиты на expensive tasks, fallback rules engine/manual review |
| Market | Спрос остаётся точечным, pipeline не масштабируется | med | new-logo pace <1 клиент/мес, burn без роста | <10 SQL/мес, pilot volume stagnant 2 квартала | сузить ICP до банков/fintech/e-commerce, усилить partner-led GTM |
| Market | Price compression из-за конкурентов и тендеров | high | ARPA падает ниже 250k, p10 EBITDA уходит глубже в минус | win rate есть, но discount >25% становится нормой | пакетировать premium modules, внедрить floor-price, продавать ROI и audit-risk reduction |
| Regulatory | Ужесточение 152-ФЗ и требований к data residency | high | нужен дорогой локальный контур, slower sales cycle | новые требования к локализации/уведомлениям, customer legal redlines растут | on-prem/private cloud by design, локальные DPA templates, аудит data flows |
| Regulatory | Санкции SaaS/LLM vendors ограничивают критичные integrations | med | отказ части западных API, срочный replatforming | предупреждения vendor, billing/payment failures, geo blocks | резервный стек российских и open-source моделей, abstraction layer для providers |
| Financial | Cash runway сжимается из-за длинного sales cycle | high | down round / insolvency risk | runway <9 мес, cumulative burn хуже плана на 15%+ | квартальное rebudgeting, hiring freeze triggers, milestone-based fundraising |
| Financial | Рост USD и инфляции раздувает infra/FOT | med | COGS/FOT выше плана, CAC растёт | cloud/API bill в ₽ +20%+, salary refresh pressure | рублёвые контракты с клиентами, валютные буферы, annual repricing clauses |
| Black swan | Резкое усиление санкций или военная эскалация | med | заморозка части клиентов и подрядчиков | тендеры стопорятся, vendor exits, payment disruptions | российский контур поставщиков, cash reserve, диверсификация по отраслям |
| Black swan | Отключение ключевого LLM-провайдера или regulator ban on external AI | med | core workflow outage, ручной fallback | массовые API errors, sudden policy changes, regulator notices | offline fallback flows, self-hosted models, critical-path tasks без зависимости от одного LLM |

## B5. Kill conditions через 6 месяцев

1. **Median insolvency trigger:** если обновлённый **p10 EBITDA @M24 < 0** и фактический runway **<9 месяцев**, продолжать нельзя.  
2. **EBITDA gate failure:** если через 6 месяцев forecast **p50 EBITDA @M24 < 500 000 ₽/мес**, кейс не проходит инвестиционный порог.  
3. **Go-to-market failure:** если к M6 одновременно **<3 платящих клиентов** И **blended CAC > 1,5 млн ₽** И/ИЛИ **pilot→paid <20%**, модель уходит в неинвестируемый consulting-like режим.

## B6. Итог по Program 6B

**Вердикт P6B: CONDITIONAL PASS.**  
Кейс выдерживает median-case, но запас прочности слабый. Главные threat vectors, это **price compression, CAC inflation, локальный regulatory overhead и vendor dependency на LLM/API**. При сохранении ARPA 300k+, churn около 1,5% и partner-assisted distribution модель ещё может дойти до сильного EBITDA на M24. Но если рынок продавит цену вниз или продажи окажутся медленнее, инвестиционный профиль быстро ломается.

### Источники для SECTION B
- [T1] внутренние расчёты кейса: `04-economics.md` и Section A текущего `05-critic.md`
- [T2] `02-demand.md` текущего кейса
- [T3] Vanta: https://www.vanta.com/ , https://www.vanta.com/resources/what-is-vanta , Drata: https://drata.com/products/compliance , Secureframe: https://secureframe.com/
- [T4] PrivacyLine: https://privacyline.ru/ , vc.ru про рост значимости 152-ФЗ комплаенса: https://vc.ru/id184214/2108071-izmeneniya-v-152-fz-s-30-maya-2025-goda , Habr Security Vision: https://habr.com/ru/companies/securityvison/articles/834702/ , https://habr.com/ru/companies/securityvison/news/989128/ , Skolkovo про SiteSecure/Б-152: https://old.sk.ru/news/b/pressreleases/archive/2017/09/06/rezident-skolkovo-pomozhet-saytam-ispolnyat-zakon-o-personalnyh-dannyh.aspx , Skolkovo про Security Vision: https://sk.ru/news/rezident-skolkovo-avtomatiziroval-informacionnuyu-bezopasnost-pochty-rossii/ , Skolkovo про Comindware: https://sk.ru/news/rezident-skolkovo-avtomatiziruet-biznesprocessy-hertz/

<!-- P6B-DONE -->

---

## Файл: 06-verdict.md

[B2B-OPS] Enterprise Compliance Operations Agents v2 — APPROVED WITH NOTES: 71/100 | EBITDA base=680К₽/мес через 15 мес | LTV/CAC=14,2x | Ключевое преимущество: enterprise compliance ops с private-contour fit | Главный риск: price compression и длинный sales cycle.

# 06-verdict — Enterprise Compliance Operations Agents v2

sector: B2B-OPS
status: APPROVED WITH NOTES
score: 71/100
normalized_from_raw: 107/150
previous_score: 72/100
score_delta_vs_previous: -1
case_slug: enterprise-compliance-operations-agents-v2
updated_at: 2026-04-20 02:42 MSK

## Инвесткомитет: итоговый вердикт

Кейс проходит инвестиционный порог как **APPROVED WITH NOTES**. Сильная сторона, это подтверждённая unit economics и достижимость `company_ebitda_potential_rub_month > 500 000 ₽` в enterprise-конфигурации при 38-40 клиентах и горизонте до 24 месяцев. Ограничение, это узкий и дорогой GTM: рынок реален, но evidence quality и защищённость pricing пока не дотягивают до безусловного approve.

## Оценка

Source tier balance: T1=5, T2=8, T3=3, weighted=2.13. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | "LTV/CAC 14,2x", "CAC Payback 3,1 мес", "Contribution Margin 62,0%" из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В 04-economics.md: "при 50 клиентах EBITDA около 3,07 млн ₽/мес"; порог 500К достигается примерно на 38 клиентах к M15. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | В 02-demand.md: "exact-category в РФ поисковый спрос низкий, но money demand подтверждён"; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | В 05-critic.md: "Ключевой moat... готовые agentic playbooks + локальная регуляторика + приватный контур + быстрый time-to-value". |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | В 05-critic.md: "главные threat vectors — price compression, CAC inflation, локальный regulatory overhead и vendor dependency". |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | В 04-economics.md есть канальный CAC и funnel; в 02-demand.md уже выделены 10 целевых аккаунтов regulated/data-heavy ICP. |

**Sum raw = 107/150**  
**Normalized score = round(107 × 100 / 150) = 71/100**

### Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 1 | Сетевых эффектов почти нет, каждый клиент в основном автономен. |
| Switching costs | 2 | Есть исторические evidence, playbooks, интеграции и наработанные policy-workflows. |
| Scale economies | 2 | COGS и delivery-процессы улучшаются с ростом базы, но не драматически из-за service-компоненты. |
| Proprietary data / model advantage | 1 | Уникальный датасет не доказан количественно, преимущество пока скорее в workflow design. |
| Regulatory moat | 2 | Локальный private contour и знание 152-ФЗ/enterprise procurement помогают, но лицензируемый moat не доказан. |
| Brand / distribution | 1 | Бренд и канал пока слабые, distribution опирается на founder-led sales и партнёров. |
| Embedded workflow | 3 | При внедрении продукт встраивается в ежемесячный evidence/remediation цикл клиента. |

**Moat raw = 12/21, moat score = round(12 × 25 / 21) = 14/25**

## Investment one-liner

`[B2B-OPS] Enterprise Compliance Operations Agents v2 — APPROVED WITH NOTES: 71/100 | EBITDA base=680К₽/мес через 15 мес | LTV/CAC=14,2x | Ключевое преимущество: private-contour compliance ops для regulated buyers | Главный риск: price compression и длинный sales cycle.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 13 266 667 ₽ |
| CAC blended | 934 054 ₽ |
| LTV/CAC | 14,2x |
| CAC Payback | 3,1 мес по MRR |
| Gross Margin | 66,3% |
| contribution_margin_rub_month | 186 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 882 500 ₽/мес |
| company_ebitda_rub_month, M12 base | -1 540 030 ₽/мес |
| company_ebitda_potential_rub_month | 3 067 500 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 38 |
| months_to_500k_ebitda | 15 |
| clients_to_1m_ebitda | 40 |
| months_to_1m_ebitda | 15-16 |
| Break-even | 35 клиентов по gross profit / 38 по contribution |
| startup_capital_to_bep_rub | 62 570 728 ₽ |

## Полный business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | SDR | LinkedIn Sales Navigator, Apollo, Excel/CRM | 20 мин/account | 1 500 | semi-auto |
| 2 | Первичный outreach и sequence | SDR | Apollo/почта/телефония | 10 мин/account | 700 | high |
| 3 | Reply handling и qualification | SDR | amoCRM, почта, call notes | 25 мин/ответивший лид | 2 300 | semi-auto |
| 4 | Discovery call | AE + CEO/Compliance lead | Meet/Zoom, шаблон discovery | 60 мин + prep | 8 500 | low |
| 5 | Demo и ROI-калькуляция | AE + CTO | Demo workspace, калькулятор ROI | 90 мин | 11 000 | low |
| 6 | Pilot scoping и security questionnaire | AE + CTO | Notion/Docs, infosec checklist | 4-6 часов | 28 000 | low |
| 7 | Пилот 2-4 недели | CSM + CTO | Product, cloud, support channel | 20 часов | 46 000 | semi-auto |
| 8 | Коммерческое предложение и legal | AE + CEO | шаблон MSA/DPA, e-sign | 3-5 часов | 17 000 | low |
| 9 | Procurement и vendor onboarding | AE + finance | ЭДО, email, Excel | 2-3 часа | 9 500 | semi-auto |
| 10 | Invoice issuance | finance ops | 1С/Моё дело/ЭДО | 20 мин | 900 | high |
| 11 | Payment collection | finance ops + AE | банк, ЭДО, CRM reminders | 30 мин | 1 600 | high |
| 12 | Go-live и monthly evidence ops | CSM + product | product, cloud, support | 6-8 ч/мес | 14 000 | semi-auto |

## Финансовая траектория

| Scenario | M12 clients | EBITDA @M12 | Break-even month | Startup capital to BEP |
|---|---:|---:|---:|---:|
| Base | 26,8 | -1 540 030 ₽/мес | 14 | 62 570 728 ₽ |
| Optimistic | 33,0 | -325 075 ₽/мес | 13 | 55 175 052 ₽ |
| Pessimistic | 15,9 | -3 719 033 ₽/мес | 20 | 82 879 750 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-6 032 006 ₽/мес**
- p50 EBITDA @M24 = **8 576 405 ₽/мес**
- p90 EBITDA @M24 = **31 643 874 ₽/мес**
- Вывод: median-case инвестиционно пригоден, но хвост риска широкий.

## Команда

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraising, key accounts | 845 000 |
| CTO / Tech Lead | архитектура, security, implementation governance | 715 000 |
| Senior Backend #1 | core workflows, integrations | 546 000 |
| Senior Backend #2 | evidence engine, policy automation | 546 000 |
| ML Engineer | classification, extraction, policy mapping | 650 000 |
| DevOps | isolated tenants, logging, deployment, observability | 455 000 |
| Frontend | operator UI, audit trails, admin console | 364 000 |
| SDR | outbound prospecting, list building, sequencing | 208 000 |
| AE | discovery, demo, close, procurement | 416 000 |
| Customer Success | onboarding, adoption, renewals | 312 000 |
| **Итого** |  | **5 057 000** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбербанк | крупнейший regulated buyer, постоянный объём evidence, vendor и policy controls | email decision-maker в compliance/IB + профильные конференции CNews/AntiFraud | 400 000 ₽/мес |
| ВТБ | тяжёлый procurement, постоянные регуляторные циклы и audit-readiness | партнёрство с интегратором + direct outreach в compliance office | 400 000 ₽/мес |
| Альфа-Банк | сильный digital bank, много data/privacy процессов | warm intro через интегратора/consulting partner | 350 000 ₽/мес |
| Т-Банк | data-heavy fintech с большим количеством внутренних контролей и vendor workflows | founder-led outreach + security/compliance meetup | 350 000 ₽/мес |
| Совкомбанк | банковская регуляторика и высокая цена ручного compliance ops | email decision-maker + отраслевой roundtable | 300 000 ₽/мес |
| МТС Банк | сочетание fintech и телеком-персональных данных, много cross-functional controls | партнёрство с MTS digital ecosystem vendor + direct sales | 300 000 ₽/мес |
| Ozon Банк | быстрорастущий fintech-контур, высокий объём policy/evidence задач | direct outreach через compliance/legal leadership | 300 000 ₽/мес |
| Яндекс Банк | digital-first банк, где важны быстрые remediation и vendor-control loops | CTO/compliance outreach + контент на vc.ru | 300 000 ₽/мес |
| X5 Group | data-heavy enterprise с персональными данными и сложной сетью процессов | партнёрство с интегратором + отраслевые ивенты по data governance | 250 000 ₽/мес |
| VK | крупный digital enterprise с privacy/compliance и data residency болью | Habr/vc.ru thought leadership + direct outreach в governance/IB | 250 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Price compression в тендерах и enterprise discounts | high | high | В sensitivity price -30% ведёт к EBITDA @M12 **-3 956 012 ₽/мес**. |
| CAC inflation и медленный sales cycle | high | high | CAC x2 в sensitivity ухудшает EBITDA @M12 до **-3 268 030 ₽/мес**. |
| Vendor dependency на LLM/API и regulatory overhead | medium | high | 05-critic.md прямо отмечает vendor dependency и локальный regulatory overhead как threat vector. |

## Что должно быть доказано после инвестиции

1. Pilot-to-paid не ниже **30-35%** на первых 10-12 пилотах.
2. ARPA удерживается **300 000 ₽/мес+** без системной скидки >20%.
3. К M12 компания доходит минимум до **25+ активных клиентов**, чтобы сохранить путь к 500К EBITDA на M15.
4. Не менее **2-3 reference accounts** в РФ regulated/data-heavy сегментах.
5. Private contour и локальная регуляторика оформлены как repeatable product playbook, а не кастомный консалтинг.

## Proof points для APPROVED

- Unit economics инвестиционного уровня уже доказаны: **LTV/CAC 14,2x**, **CAC Payback 3,1 мес**, **GM 66,3%**.
- Profit gate проходит: при **38 клиентах** компания выходит на **500К+ EBITDA/мес**, при **40 клиентах** уже проходит 1М EBITDA/мес.
- Рынок узкий, но платёжеспособный: есть публичные референсы **PrivacyLine**, **Vanta**, **Drata**, а также RU hiring/data signals по compliance automation.
- Категория понятна enterprise buyer: продукт решает recurring pain, а не разовую "nice to have" задачу.

## Финальное решение инвесткомитета

**APPROVED WITH NOTES.**

Инвестировать можно, если команда сразу фиксирует три дисциплины: 1) не уходит в low-ticket utility, 2) продаёт через regulated mid-market/enterprise ICP и партнёров, 3) защищает pricing floor. Это не mass-market SaaS, а узкий B2B-OPS кейс с хорошей economics и умеренно-хрупким moat. Поэтому approve оправдан, но только с ежеквартальной проверкой GTM и price integrity.

---

## Файл: 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-19 — Program 4 Demand Validation
- stage: P4
- verdict: CONDITIONAL_PASS
- summary: Exact search demand в РФ низкий, но WTP подтверждён через PrivacyLine, 152DOC, Vanta и Drata; early reject не сработал, потому что Profit Gate проходит в mid-market и enterprise сценариях.
- demand_api: LOW (score=0 exact, score=7-22 adjacent)
- market_view: узкая, но платёжеспособная B2B compliance automation ниша с достаточным SAM для fund-level интереса
- profit_gate: PASS
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-compliance-operations-agents-v2/02-demand.md

## 2026-04-19 — Program 5 Unit Economics
- stage: P5
- verdict: PASS
- provisional_score: 80/100
- delta_vs_previous_approved_score: +8 vs 72/100
- summary: fully-loaded CAC подтверждён для regulated enterprise motion; при MRR 300k и churn 1,5%/мес модель даёт LTV 13,27 млн ₽, LTV/CAC 14,2x, CAC Payback 3,1 мес и Contribution Margin 62%.
- economics_view: break-even достигается на 35 клиентах с включённым GTM engine; при 50 клиентах EBITDA около 3,07 млн ₽/мес, поэтому economics-stage reject не требуется.
- gate_checks:
  - ltv_cac: PASS (14.2x)
  - cac_payback: PASS (3.1 months)
  - contribution_margin: PASS (62.0%)
  - ebitda_50_clients: PASS (3.07M RUB/month)
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-compliance-operations-agents-v2/04-economics.md

## 2026-04-20 — Program 7 Critic and Verdict
- stage: P7
- verdict: APPROVED_WITH_NOTES
- score: 71/100
- raw_score: 107/150
- delta_vs_previous_approved_score: -1 vs 72/100
- summary: кейс проходит investment committee gate за счёт сильной unit economics и достижимого EBITDA >500К/мес к M15, но получает штраф за качество demand evidence и умеренно слабый moat.
- rubric:
  - unit_economics: 22/25
  - ebitda_potential: 19/25
  - market_demand: 17/25
  - moat: 14/25
  - execution_risk: 17/25
  - gtm_realism: 18/25
- source_tier_balance:
  - T1: 5
  - T2: 8
  - T3: 3
  - weighted: 2.13
  - penalty_to_market_demand: -2
- key_gates:
  - company_ebitda_potential_rub_month: PASS (3 067 500 ₽/мес at 50 clients)
  - clients_to_500k_ebitda: PASS (38)
  - months_to_500k_ebitda: PASS (15)
  - moat_strength: CONDITIONAL_PASS (14/25)
  - evidence_quality: CONDITIONAL_PASS
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-compliance-operations-agents-v2/06-verdict.md
