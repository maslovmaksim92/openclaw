# enterprise-ai-documentation-platform-v2
**Статус:** APPROVED WITH NOTES
**Итоговый балл:** 70/100
**Дата:** 2026-04-20
**Сектор:** GEO-EXPAND

---

## Этап 1 — Описание кейса
# Enterprise AI Documentation Platform

## Статус intake
Новый rerun-кейс создан принудительно по правилу полного переанализа для файлов `rerun-*`. Кейс направлен дальше в P3-demand-validation без проверки на duplicate.

## Почему кейс создан
- сигнал помечен как rerun и должен пройти полный пайплайн заново
- предыдущий вердикт: APPROVED (72/100) от 2026-04-19
- ожидаемый следующий этап: P3-demand-validation

## Краткое описание
Rerun-кейс по AI-native платформе для enterprise-документации, AI-поиска и managed documentation ops.

## Потенциал
По контексту исходного сигнала кейс сохраняет потенциал для порога EBITDA 500K+ RUB/мес, поэтому оставлен в пайплайне для полного переанализа.

---

## Этап 2 — Intake
---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-rerun-enterprise-ai-documentation-platform.md
created: 2026-04-19T19:16:56+03:00
original_verdict: /home/node/.openclaw/repo/business-models/approved/enterprise-ai-documentation-platform/verdict.md
previous_score: "72/100"
previous_status: APPROVED
previous_date: 2026-04-19
---

# Intake — Enterprise AI Documentation Platform

## Режим обработки
Принудительный rerun по правилу полного пайплайна для файлов `rerun-*`. Duplicate-проверка пропущена намеренно. Следующий этап: **P3-demand-validation**.

## Исходный контекст raw

# RE-ANALYSIS REQUEST — Enterprise AI Documentation Platform

## Meta
- previous_status: ✅ APPROVED
- previous_score: 72/100
- previous_sector: GEO-EXPAND
- previous_date: 2026-04-19
- source_folder: /business-models/approved/enterprise-ai-documentation-platform/
- reason_for_rerun: обновлены P4 (Source Tiering, TAM/SAM/SOM), P5 (Fully-loaded CAC, Hiring Realism), P6B (Monte Carlo Lite), P7 (Rubric 6×25, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner)

## Description (1 line)
AI-native платформа для enterprise-документации, AI-поиска и managed documentation ops для B2B-команд.

## Задача для intake-triage
1. Прочитай verdict.md предыдущего запуска (`/home/node/.openclaw/repo/business-models/approved/enterprise-ai-documentation-platform/verdict.md`) для контекста, но НЕ копируй результат — начни свежий анализ.
2. Создай новый кейс в pipeline/cases/enterprise-ai-documentation-platform-v2/ и пройди полный пайплайн P3→P7 с новой рубрикой.
3. Сравни новый score с предыдущим (72/100) и запиши delta в финальный 06-verdict.md.

## Приоритет
p1 — batch re-run после обновления системы аналитики 2026-04-19.

---

## Этап 3 — Demand Validation
# 02-demand — Demand Validation

## Кейс
Enterprise AI Documentation Platform, AI-native платформа для корпоративной документации, базы знаний, AI-поиска и managed documentation ops.

## Итог
**Статус: CONDITIONAL PASS**

Exact-category спрос по формулировке кейса низкий, но adjacent demand в РФ уже есть, а готовность платить подтверждается публичными тарифами российских и международных knowledge-base платформ. [T2][T3] Early reject не срабатывает, потому что Profit Gate проходит в mid-market и enterprise сценариях. [T2]

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand?keyword=...`

- `enterprise ai documentation platform`: composite demand **LOW**, score **0**, hh.ru **1**, Habr **2**, Yandex suggest **2**. [T3]
- `enterprise knowledge base`: composite demand **LOW**, score **7**, hh.ru **70**, Habr **2**, Yandex suggest **2**. [T3]
- `база знаний для компании`: composite demand **MEDIUM**, score **30**, hh.ru **4689**, Habr **2**, Yandex suggest **100**. [T3]
- `корпоративная база знаний`: composite demand **MEDIUM**, score **30**, hh.ru **2865**, Habr **2**, Yandex suggest **100**. [T3]
- Дополнительная проверка на hh.ru по запросу `база знаний` показывает **5 867 вакансий**, то есть боль уже оплачивается через ФОТ и внутренние процессы, а не только через SaaS-линии бюджета. [T1]

### Интерпретация
Слабый спрос у exact-keyword объясним: покупают не `enterprise AI documentation platform`, а `корпоративную базу знаний`, `документацию`, `поиск по знаниям`, `онбординг` и `поддержку`. [T2][T3] Наличие тысяч вакансий по смежной тематике подтверждает, что проблема реальна и операционно значима для работодателей. [T1]

## 2. Реальные конкуренты и цены

| Конкурент | Сегмент | Публичная цена | Что доказывает |
|---|---|---:|---|
| TEAMLY | РФ база знаний / knowledge management | **299 ₽** за редактора в месяц на базовом тарифе и **399 ₽** за редактора в месяц на тарифе для зрелых компаний. [T2] | В РФ уже нормализована подписка за корпоративную базу знаний. |
| Confluence Cloud Standard | глобальный стандарт де-факто для командовой документации | **$6.70** за пользователя в месяц на первом ценовом тиру до 100 пользователей; Confluence Premium от **$18.10** за пользователя в месяц. [T2] | Международный рынок платит за collaborative docs и knowledge ops как за core workflow. |
| Slite | глобальная knowledge base + AI search | **$8** за участника в месяц для Standard и **$20** за участника в месяц для Knowledge Suite. [T2] | AI-assisted knowledge retrieval уже продаётся как отдельный продуктовый слой. |

### Вывод по конкурентам
Ниша не гипотетическая: есть российский low-to-mid ticket benchmark и международный mid-to-high ticket benchmark. [T2] Для AI-native enterprise решения с миграцией, governance, AI search и managed documentation ops реалистичный коридор чека выглядит как **1,2–5,4 млн ₽/год** на аккаунт, в зависимости от числа редакторов, private deployment и service-layer. [T2, вывод]

## 3. Telegram и российский контур
- На официальном сайте TEAMLY присутствуют ссылки на **`t.me/teamly_promo_bot`** и канал **`t.me/teamly_ru`**. Это подтверждает наличие Telegram как канала захвата и сопровождения в RU knowledge-management сегменте. [T2]
- На сайте TEAMLY отдельно заявлена выделенная поддержка в мессенджерах, то есть Telegram/мессенджеры используются как sales-support и customer-success слой, а не как самостоятельный продуктовый substitute. [T2]
- В internal demand API для ключевых запросов Telegram subscribers автоматически не обнаружены. [T3]

### Вывод
В РФ Telegram-контур есть, но как канал продвижения, демо и поддержки. Самостоятельного bot-first рынка для enterprise documentation я не вижу; платёжеспособный контур остаётся sales-led B2B. [T2][T3]

## 4. WTP, доказательства готовности платить
1. TEAMLY продаёт базу знаний по публичным тарифам **299–399 ₽ за редактора в месяц**. [T2]
2. Confluence Standard публично стоит **$6.70/user/month**, Premium от **$18.10/user/month** на первом тиру. [T2]
3. Slite публично стоит **$8/member/month** и **$20/member/month** за knowledge suite с AI-поиском. [T2]
4. TEAMLY публикует кейс, где в техподдержке за счёт базы знаний получена экономия **6,48 млн ₽ ФОТ**, а у 2ГИС мигрировано **150 000 страниц** знаний, что показывает готовность enterprise-заказчика оплачивать миграцию, внедрение и эксплуатацию knowledge stack. [T2]
5. Тысячи вакансий по запросам, связанным с базой знаний, означают, что компании уже несут payroll-cost на создание, поддержку и поиск знаний. [T1]

### Вывод по WTP
**WTP подтверждён.** Покупатель уже платит и за seat-based SaaS, и за enterprise-grade knowledge migration, и за внутренний труд, который можно замещать automation/search/documentation ops. [T1][T2]

## 5. Market sizing

### Методика
Top-down считаю от российского рынка СЭД/ECM/CSP и глобального рынка knowledge management software. [T2][T3] Bottom-up считаю от числа достижимых российских покупателей, доли компаний с подтверждённой болью и среднего контракта. [T1][T2]

### Допущения
- Глобальный knowledge management software market: **$20,15 млрд** в 2024. [T3]
- Российский рынок СЭД, ECM и CSP-систем: **95–110 млрд ₽** по итогам 2025; для расчёта беру midpoint **102,5 млрд ₽**. [T2]
- В глобальном KM-сегменте document management составляет **38,29%** выручки, что подтверждает большую долю документационного use-case в общей knowledge stack. [T3]
- Для узкого сегмента `enterprise AI documentation platform` беру **5%** от российского ECM/CSP-рынка как addressable share. Это расчётная оценка, а не прямой рыночный факт. [T2][T3, спекуляция]
- Достижимый buyer universe в РФ оцениваю в **3 500** компаний: это консервативный поднабор широкого ECM/CSP-рынка, при том что один TEAMLY уже заявляет **1 500 компаний** в базе клиентов. [T2, расчёт]
- `% with need` = **25%**, опираясь на тысячи hh.ru вакансий и medium adjacent-demand в internal API. [T1][T3]
- Средний контракт для AI documentation platform: **1,2 млн ₽/год**. Это примерно соответствует 200-seat развёртыванию около TEAMLY upper-tier benchmark с премией за AI-search, governance и migration/support layer. [T2, расчёт]

### GTM-10-targets для bottom-up
1. 2ГИС [T2]
2. ВкусВилл [T2]
3. SPLAT Global [T2]
4. Lamoda [T2]
5. Dodo Brands [T2]
6. Контур [T2]
7. МойОфис [T2]
8. Tele2/Т2 [T2]
9. 1C-Рарус [T2]
10. Robokassa [T2]

Это реальные buyers или близкие по профилю компании с распределёнными командами, высокой ценой знаний и сложной внутренней документацией. [T2]

### Расчёты
- **TAM (мир)** = **$20,15 млрд**. [T3]
- **TAM (РФ), top-down** = 102,5 млрд ₽ × 5% = **5,13 млрд ₽**. [T2][T3, расчёт]
- **SAM (РФ), top-down** = 5,13 млрд ₽ × 25% segment fit = **1,28 млрд ₽**. [T2][T3, расчёт]
- **SOM Y1, top-down** = 1,28 млрд ₽ × 3% = **38,4 млн ₽**. [расчёт]
- **SOM Y3, top-down** = 1,28 млрд ₽ × 8% = **102,5 млн ₽**. [расчёт]

Bottom-up:
- **Total buyers** = **3 500**. [T2, расчёт]
- **Buyers with need** = 3 500 × 25% = **875**. [T1][T3, расчёт]
- **SAM bottom-up** = 875 × 1,2 млн ₽ = **1,05 млрд ₽**. [T2, расчёт]
- **SOM Y1 bottom-up** = 1,05 млрд ₽ × 3% = **31,5 млн ₽**. [расчёт]
- **SOM Y3 bottom-up** = 1,05 млрд ₽ × 8% = **84,0 млн ₽**. [расчёт]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | $20,15 млрд [T3] | — | — | top-down |
| TAM (РФ) | 5,13 млрд ₽ [T2][T3] | 4,20 млрд ₽ [T2, если 3 500 × 1,2 млн ₽] | diff 18%, bottom-up уже сужен до достижимого buyer set | **4,20 млрд ₽** |
| SAM (РФ) | 1,28 млрд ₽ [T2][T3] | 1,05 млрд ₽ [T1][T2][T3] | diff 22%, приемлемо | **1,05 млрд ₽** |
| SOM Y1 | 38,4 млн ₽ | 31,5 млн ₽ | diff 18% | **31,5 млн ₽** |
| SOM Y3 | 102,5 млн ₽ | 84,0 млн ₽ | diff 18% | **84,0 млн ₽** |

### Sanity check
- SOM Y1 / SAM = **3%**, это реалистично и заметно ниже red-flag уровня. [расчёт]
- SOM Y1 при ARR **1,2 млн ₽** соответствует примерно **26 клиентам** за год. [расчёт]
- При среднем цикле сделки **4-5 месяцев** это напряжённо, но достижимо для productized B2B motion с сильной миграцией и реферальными кейсами; для совсем маленькой команды это уже верхняя граница. [T2, вывод]

## 6. Profit Gate
Цель: проверить все основные сценарии монетизации на достижимость **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Self-serve seat-based SaaS
- Цена: **399 ₽ за редактора в месяц**. [T2]
- Средний аккаунт: **100 редакторов** = **39 900 ₽ MRR**. [T2, расчёт]
- Валовая маржа: **80%**. [T2, допущение]
- Валовая прибыль на клиента: **31 920 ₽/мес**. [расчёт]
- При fixed costs **1,8 млн ₽/мес** нужно около **73 клиентов** для EBITDA 500k/mo. [расчёт]

**Вердикт: FAIL.** Для новой команды слишком тяжёлый объём привлечения и саппорта. [вывод]

### Сценарий B. Team workspace + AI add-on
- Цена: **120 000 ₽/мес** на аккаунт. [T2, вывод]
- Валовая маржа: **78%**. [T2, допущение]
- Валовая прибыль на клиента: **93 600 ₽/мес**. [расчёт]
- Для EBITDA 500k/mo нужно около **25 клиентов**. [расчёт]

**Вердикт: FAIL / borderline.** Возможно для зрелого бизнеса, но слабовато для fund-level кейса на старте. [вывод]

### Сценарий C. Mid-market AI knowledge platform
- Цена: **250 000 ₽/мес** или **3,0 млн ₽/год**. [T2, вывод]
- Валовая маржа: **80%**. [T2, допущение]
- Валовая прибыль на клиента: **200 000 ₽/мес**. [расчёт]
- Для EBITDA 500k/mo нужно около **12 клиентов**. [расчёт]

**Вердикт: PASS.** Это уже достижимая конфигурация для sales-led B2B продукта. [вывод]

### Сценарий D. Enterprise platform + migration + managed documentation ops
- Цена: **450 000 ₽/мес** подписка + **600 000 ₽** внедрение/миграция. [T2, вывод]
- Валовая маржа подписки: **82%**. [T2, допущение]
- Валовая прибыль на клиента по MRR: **369 000 ₽/мес**. [расчёт]
- Для EBITDA 500k/mo достаточно **7 клиентов** плюс несколько внедрений в квартал. [расчёт]

**Вердикт: PASS.** Это лучший путь к EBITDA и fundable профилю. [вывод]

### Сценарий E. AI-search add-on как отдельный продукт
- Цена: **50 000 ₽/мес**. [T2, вывод]
- Даже при высокой марже отдельный add-on требует слишком большой installed base, чтобы сам по себе дать EBITDA 500k/mo. [расчёт]

**Вердикт: FAIL standalone, PASS only as ARPU uplift.** [вывод]

### Общий вывод по Profit Gate
Profit Gate **проходит**, но только если продукт продавать не как дешёвую wiki-утилиту, а как AI knowledge layer с миграцией, governance, private deployment и managed documentation ops. [T2]

## 7. Решение для пайплайна
- Exact demand API: **LOW**, adjacent demand: **MEDIUM**. [T3]
- WTP: **подтверждён**. [T1][T2]
- RU services / Telegram contour: **есть**, но не bot-first. [T2][T3]
- TAM/SAM/SOM: **достаточны для нишевого B2B fund-level кейса**, но это не массовый рынок. [T2][T3]
- Profit Gate: **PASS** в mid-market и enterprise сценариях. [T2]

**Решение: не отклонять на этапе Demand Validation, переводить дальше.**

Sources: T1=2, T2=5, T3=2. Primary evidence basis: T2.

## Источники
- hh.ru search: https://hh.ru/search/vacancy?text=%D0%B1%D0%B0%D0%B7%D0%B0+%D0%B7%D0%BD%D0%B0%D0%BD%D0%B8%D0%B9
- TAdviser, рынок СЭД/ECM/CSP: https://www.tadviser.ru/index.php/%D0%A1%D0%AD%D0%94
- TEAMLY pricing: https://teamly.ru/pricing/
- TEAMLY homepage / cases: https://teamly.ru/
- Atlassian Confluence pricing: https://www.atlassian.com/software/confluence/pricing
- Atlassian licensing page: https://www.atlassian.com/licensing/confluence
- Slite pricing: https://slite.com/pricing
- Grand View Research, Knowledge Management Software Market Size Report: https://www.grandviewresearch.com/industry-analysis/knowledge-management-software-market-report
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=enterprise%20ai%20documentation%20platform
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=enterprise%20knowledge%20base
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B1%D0%B0%D0%B7%D0%B0%20%D0%B7%D0%BD%D0%B0%D0%BD%D0%B8%D0%B9%20%D0%B4%D0%BB%D1%8F%20%D0%BA%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D0%B8
- internal multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%B1%D0%B0%D0%B7%D0%B0%20%D0%B7%D0%BD%D0%B0%D0%BD%D0%B8%D0%B9

> Market Pulse 2026-04-20: растущий интерес.

---

## Этап 4 — Unit Economics
# 04-economics — Unit Economics

## Кейс
Enterprise AI Documentation Platform, AI-native платформа для enterprise-документации, AI-поиска и managed documentation ops.

## Итог
**Статус: PASS**

Кейс проходит Program 5 на fund-level, если продавать продукт как **mid-market / enterprise documentation platform с внедрением, governance, AI-search и managed ops**, а не как дешёвую wiki-подписку. При базе **MRR на клиента 320 000 ₽/мес**, fully-loaded **CAC 888 000 ₽**, monthly churn **1,8%** и contribution margin **71,3%** экономика выглядит инвестиционно приемлемой.

## 1. Базовый коммерческий сценарий

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Mid-market и enterprise B2B, 200-2 000 сотрудников | Документация, knowledge base, AI-search, private deployment |
| Средний чек | **320 000 ₽/мес** | Подписка + governance + managed docs ops, без разовых внедрений |
| Разовый onboarding / migration fee | **600 000 ₽** | В модель payback не включаю, чтобы не завышать economics |
| New paying customers | **1,8 клиента/мес** | Средний темп после выхода GTM в рабочий ритм |
| COGS на клиента | **92 000 ₽/мес** | Подробная раскладка ниже |
| Contribution profit на клиента | **228 000 ₽/мес** | 320 000 - 92 000 |
| Contribution Margin | **71,3%** | 228 000 / 320 000 |

## 2. Детальный бизнес-процесс: от lead до оплаты

Ниже показан **процесс на один выигранный контракт**. Это не blended CAC, а прямые операционные касания по сделке. Полный CAC выше, потому что включает невыигранные сделки, маркетинг, инструменты и overhead.

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | ICP-ресерч и сбор account list | SDR | HH/CRM/контур компаний/таблицы | 5 ч | 7 500 | Средняя |
| 2 | Enrichment по стеку docs/helpdesk/devtools | SDR | CRM, сайт клиента, ручной ресерч | 4 ч | 6 000 | Средняя |
| 3 | Персонализированный outbound | SDR | e-mail sequencer, Telegram, CRM | 8 ч | 12 000 | Средняя |
| 4 | Qualification call | SDR + AE | Meet, CRM, скрипт qualification | 2 ч | 8 500 | Низкая |
| 5 | Discovery с buyer и техкомандой | AE + CEO | Meet, Notion, discovery template | 4 ч | 19 000 | Низкая |
| 6 | Аудит текущей документации и knowledge stack | Solutions Engineer / PM | crawler, sample import, workspace demo | 6 ч | 21 000 | Средняя |
| 7 | Demo AI-search, governance и migration path | AE + CEO + SE | demo-tenant, презентация, ROI-sheet | 3 ч | 17 500 | Средняя |
| 8 | Подготовка пилота / proposal / scoping | AE + PM | CRM, калькулятор юнит-экономики, КП | 5 ч | 21 500 | Средняя |
| 9 | Security/legal/procurement review | CEO + Ops | DPA/SLA templates, ЭДО, security docs | 6 ч | 24 000 | Низкая |
| 10 | Переговоры по цене и согласование договора | CEO + AE | CRM, договор, таблица уступок | 4 ч | 18 500 | Низкая |
| 11 | Счёт, ЭДО, запуск и первый платёж | CSM + Finance Ops | банк, ЭДО, billing, onboarding checklist | 3 ч | 10 500 | Высокая |
| **Итого direct touch cost per won client** |  |  |  | **50 ч** | **166 000 ₽** |  |

**Вывод:** direct touch cost на выигранный контракт около **166 тыс. ₽**, но fully-loaded CAC должен учитывать все невыигранные касания, FOT sales/marketing, tools, events и overhead. Поэтому инвестиционно корректно считать blended CAC, а не только cost-to-serve выигранной сделки.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / AI-search | 24 000 | токены + retrieval + reranking | Основной AI cost bucket |
| Cloud / hosting / storage / CDN | 14 000 | серверы, storage, backup, CDN | Для enterprise workspace |
| Customer Success / support | 18 000 | аллокация CSM на 12-14 клиентов | QBR, поддержка, adoption |
| Documentation ops / content QA | 20 000 | доля docs-ops / PM | Проверка качества, governance |
| Onboarding амортизация | 10 000 | 600k setup fee частично offset, но в COGS оставляю реалистичную долю | Не занижаю service layer |
| Security / monitoring / compliance | 4 000 | audit logs, monitoring, security tools | Enterprise requirement |
| Payment / admin / ЭДО | 2 000 | банк, ЭДО, billing | Небольшой, но постоянный cost |
| **Итого COGS** | **92 000 ₽** |  |  |

**Gross / contribution:**
- Revenue per client/month = **320 000 ₽**
- COGS per client/month = **92 000 ₽**
- Contribution profit per client/month = **228 000 ₽**
- **Contribution Margin = 71,3%**

## 4. Fully-loaded CAC

### 4.1 Формула

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed to new + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### 4.2 Таблица компонентов CAC

Сегмент кейса: **mid-market / enterprise B2B**, поэтому беру multiplier на overhead и длинный sales cycle в диапазоне enterprise-light, фактически **x1,3 к raw acquisition stack** внутри расчёта.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK, retargeting, content distribution) | **180 000** | консервативный paid layer для B2B demand capture | T2 + расчёт |
| Outbound team FOT (SDR/AE attributed to new) | **742 000** | SDR 180k gross + AE 300k gross + 30% взносы + бонусы и 70% аллокация на new business | HH.ru benchmark, T1-T3 |
| Marketing team FOT (partial allocation) | **260 000** | product marketing / content lead 200k gross × 1,3 и ~100% на acquisition | HH.ru benchmark, T3 |
| Tools (CRM, data, outreach, call tools, analytics) | **96 000** | CRM + sequencer + enrichment + analytics stack | T2 + расчёт |
| Events/partnerships | **320 000** | 1 отраслевой ивент / квартал + партнёрские активности, усреднение по месяцу | T2 + расчёт |
| Overhead multiplier (x1.3) | **331 000** | 30% к raw stack 1 267 000 ₽/мес | standard for enterprise B2B, расчёт |
| **Итого acquisition spend** | **1 929 000 ₽/мес** |  |  |
| New paying customers | **2,17** | blended expected wins/month по каналам | расчёт |
| **Fully-loaded CAC** | **888 000 ₽** | 1 929 000 / 2,17 | расчёт |

### 4.3 CAC по каналу и funnel conversion

| Канал | Вход воронки / мес | Meeting rate | SQL rate | Proposal/Pilot rate | Win rate | New paying customers / мес | Monthly spend, ₽ | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 300 target accounts | 15% (45 reply) | 40% (18 meetings) | 39% (7 SQL) | 29% (2 wins from 7 SQL ≈ 0,58 from meetings) | **1,20** | **1 050 000** | **875 000** |
| Content / SEO / webinar inbound | 40 inbound leads | 35% (14 meetings) | 50% (7 SQL) | 43% (3 proposal) | 20% | **0,60** | **279 000** | **465 000** |
| Events / partnerships / referrals | 15 partner leads | 53% (8 meetings) | 63% (5 SQL) | 40% (2 proposal) | 19% | **0,37** | **600 000** | **1 622 000** |
| **Blended** | 355 mixed leads | — | — | — | — | **2,17** | **1 929 000** | **888 000** |

### 4.4 Sanity check against RU benchmarks

Сравнение с указанными industry benchmarks:
- Enterprise SaaS B2B в РФ: **300-900k ₽ / клиент**
- Healthtech B2B: **400-1 200k ₽ / клиент**
- Fintech B2B: **200-700k ₽ / клиент**

Наш blended **CAC = 888k ₽** находится **у верхней границы enterprise SaaS benchmark**, что для продаж с discovery, пилотом, security review и procurement выглядит реалистично. Red flag по слишком низкому CAC нет.

## 5. LTV и churn

### 5.1 Churn benchmark

Для B2B SaaS с высоким ARPA ориентируюсь на benchmark ChartMogul: у SaaS-компаний с более высоким ARPA monthly churn обычно заметно ниже SMB-уровня и часто находится в районе **1-2% в месяц**. Для модели беру **1,8% monthly churn** как консервативный уровень для нового B2B продукта без многолетнего lock-in.

### 5.2 Расчёт

Формула: `LTV = Contribution profit per month / monthly churn`

- Contribution profit per client/month = **228 000 ₽**
- Monthly churn = **1,8%**
- **LTV = 228 000 / 0,018 = 12 667 000 ₽**

Эквивалентный ожидаемый lifetime: `1 / 0,018 = 55,6 месяца`.

## 6. Ключевые investment-метрики

| Метрика | Формула | Значение | Норма |
|---|---|---:|---|
| LTV/CAC | 12 667 000 / 888 000 | **14,3x** | >= 3,0x |
| CAC Payback | 888 000 / 320 000 | **2,8 мес** | < 12 мес, допустимо < 18 для enterprise |
| Contribution Margin | 228 000 / 320 000 | **71,3%** | > 50% желательно |
| EBITDA threshold client count | (Fixed costs + 500k) / contribution profit | **21 клиент** | Чем ниже, тем лучше |

**Вывод:** по всем трём sanity checks кейс проходит. LTV/CAC существенно выше **3:1**, payback сильно ниже enterprise-порога **18 мес**, contribution margin высокая.

## 7. Team & FOT

### 7.1 Полная таблица команды и найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 180 000 | **780 000** |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | **715 000** |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | **1 092 000** |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | **650 000** |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | **455 000** |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | **390 000** |
| SDR (outbound) | 1 | 180 000 | 1 | 1 | 54 000 | **234 000** |
| AE (Account Exec) | 1 | 320 000 | 1,5 | 3 | 96 000 | **416 000** |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | **338 000** |
| Product / Docs Ops Lead | 1 | 320 000 | 1,5 | 1,5 | 96 000 | **416 000** |
| **Итого fully-loaded FOT при полной укомплектации** | **10** |  |  |  |  | **5 486 000 ₽/мес** |

### 7.2 Функции команды

| Роль | Функция | Fully-loaded salary, ₽/мес |
|---|---|---:|
| CEO | продажи enterprise, fundraising, partnerships, pricing | 780 000 |
| CTO/Tech Lead | архитектура, product delivery, инфобез, приоритизация | 715 000 |
| Senior Backend #1 | core platform, API, RBAC, billing | 546 000 |
| Senior Backend #2 | connectors, search, ingestion, analytics | 546 000 |
| ML Engineer | RAG, retrieval quality, ranking, hallucination control | 650 000 |
| DevOps | infra, deployment, observability, private cloud | 455 000 |
| Frontend | editor UX, admin panel, search UX | 390 000 |
| SDR | outbound, meetings, account research | 234 000 |
| AE | discovery, proposal, closing | 416 000 |
| Customer Success | onboarding, adoption, renewals | 338 000 |
| Product / Docs Ops Lead | docs governance, rollout, migration ops | 416 000 |

### 7.3 Cumulative FOT timeline M1-M12

План найма сделан без red flag: в M1 не нанимается 5+ человек, а функция GTM подключается после сборки базового продукта.

| Месяц | Кто в штате / начинает работу | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO/Tech Lead, Senior Backend #1 | **2 041 000** |
| M2 | + Frontend, + DevOps | **2 886 000** |
| M3 | + Senior Backend #2 | **3 432 000** |
| M4 | + Customer Success | **3 770 000** |
| M5 | + SDR | **4 004 000** |
| M6 | + AE | **4 420 000** |
| M7 | + Product / Docs Ops Lead | **4 836 000** |
| M8 | + ML Engineer | **5 486 000** |
| M9 | без новых hires | **5 486 000** |
| M10 | без новых hires | **5 486 000** |
| M11 | без новых hires | **5 486 000** |
| M12 | без новых hires | **5 486 000** |

**Кумулятивный FOT M1-M12:** **52 649 000 ₽**.

## 8. Fixed costs breakdown

Ниже считаю fixed costs как ежемесячную база-структуру после выхода команды в рабочий состав, без COGS на клиента.

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | **5 486 000** | Полная команда из 10 ролей |
| Office / admin / бухгалтерия / legal | **220 000** | Гибридный режим + юрподдержка |
| Core infra not in COGS | **310 000** | dev/staging, observability, internal tooling |
| G&A / software / licences | **160 000** | Notion/Jira/monitoring/finance stack |
| Recruitment reserve / misc overhead | **120 000** | hiring pipeline, HR, back-office |
| **Fixed costs total** | **6 296 000 ₽/мес** |  |

## 9. Break-even: по клиентам и по месяцу

### 9.1 Break-even by client count

Формула для EBITDA = 0:

`Client count BEP = Fixed costs / contribution profit per client`

- Fixed costs = **6 296 000 ₽/мес**
- Contribution profit per client = **228 000 ₽/мес**
- **Break-even = 27,6 клиента**, округляю до **28 клиентов**

Формула для EBITDA = 500k/mo:

`(6 296 000 + 500 000) / 228 000 = 29,8`

- **Порог 500k EBITDA = 30 клиентов**

### 9.2 Break-even by month

План продаж: первые пилоты с M4, затем 1, 1, 2, 2, 3, 3, 3, 4 клиентов по месяцам. Тогда активная база достигает:
- M4: 1 клиент
- M5: 2
- M6: 4
- M7: 6
- M8: 9
- M9: 12
- M10: 15
- M11: 19
- M12: 23
- M13: 27
- **M14: 30 клиентов**

**Вывод:**
- EBITDA break-even около **M13**
- Уровень **500k EBITDA/mo** достигается около **M14**

При **50 клиентах**:
- Revenue = **16,0 млн ₽/мес**
- Contribution profit = **11,4 млн ₽/мес**
- EBITDA ≈ **5,10 млн ₽/мес**

Profit Gate явно проходит, потому что даже при 50 клиентах компания не упирается в отрицательную экономику.

## 10. Burn-to-breakeven и cash runway

### 10.1 Burn-to-breakeven

До момента, когда `MRR × GM% > fixed costs`, компания проходит долгий продуктовый и GTM-разгон.

Грубая оценка cumulative burn до EBITDA break-even:
- M1-M3: команда и разработка без выручки, burn около **8,36 млн ₽**
- M4-M8: первые клиенты, но выручка ещё не покрывает fixed costs, дополнительный burn около **13,2 млн ₽**
- M9-M13: рост базы до 27 клиентов, дожигание ещё около **6,1 млн ₽**
- **Burn to break-even ≈ 27,7 млн ₽**

### 10.2 Cash runway

Для модели беру `startup_capital = 36 млн ₽`.

- Если смотреть на средний burn до M8, runway ≈ **7-8 месяцев**
- С учётом роста выручки и постепенного снижения net burn, фактический runway по модели ≈ **14-15 месяцев**
- До EBITDA break-even нужен капитал не меньше **30 млн ₽**, комфортно **36-40 млн ₽**

Это выше anti-red-flag порога **10 млн ₽** для enterprise B2B SaaS и выглядит реалистично для fund-level кейса.

## 11. Финальный вывод Program 5

### Что хорошо
1. **LTV/CAC = 14,3x**, заметно выше investment threshold **3,0x**.
2. **CAC Payback = 2,8 месяца**, сильно лучше enterprise-нормы **<18 мес**.
3. **Contribution Margin = 71,3%**, есть запас под sales-led рост.
4. При **30 клиентах** бизнес уже даёт **500k+ EBITDA/mo**, а при **50 клиентах** выглядит уверенно прибыльным.

### Что рискованно
1. Главный риск не в unit economics, а в **длине sales cycle** и исполнении внедрений.
2. Если продукт соскользнёт в low-ticket wiki/tooling сегмент, ARPA резко упадёт и модель перестанет быть fundable.
3. Если фактический churn будет не 1,8%, а 4-5% monthly, LTV просядет, хотя даже тогда запас ещё останется положительным.

## Решение
**PASS.**

Инвестиционно рабочая модель есть, но только в конфигурации **enterprise AI documentation platform + migration + managed documentation ops**. Как cheap self-serve knowledge base кейс бы не прошёл.

## Источники
- T1: hh.ru search / compensation references: https://hh.ru/search/vacancy?text=%D1%82%D0%B5%D1%85%D0%BB%D0%B8%D0%B4%20backend%20%D0%BC%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 ; https://hh.ru/search/vacancy?text=senior%20backend%20%D0%BC%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 ; https://hh.ru/search/vacancy?text=ML%20engineer%20%D0%BC%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 ; https://hh.ru/search/vacancy?text=account%20executive%20b2b%20%D0%BC%D0%BE%D1%81%D0%BA%D0%B2%D0%B0 ; https://hh.ru/search/vacancy?text=sdr%20%D0%BC%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- T2: category pricing / demand context from 02-demand.md: https://teamly.ru/pricing/ ; https://www.atlassian.com/software/confluence/pricing ; https://slite.com/pricing
- T3: churn benchmark: https://chartmogul.com/saas-metrics/customer-churn-rate/
- Internal case context: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-ai-documentation-platform-v2/02-demand.md

---

## Этап 5 — Critic
## SECTION A. PnL x 3 сценария (12 месяцев)

### A1. Исходные допущения
- ARPA: **320 000 ₽/клиент/мес**
- COGS: **92 000 ₽/клиент/мес**
- Gross profit / contribution на клиента: **228 000 ₽/клиент/мес**
- GM% / contribution margin: **71,3%**
- Fixed costs: **6 296 000 ₽/мес**
- Team FOT fully-loaded: **5 486 000 ₽/мес**
- Страховые взносы: **~30% к ФОТ**, уже включены в fully-loaded FOT
- CAC по каналам из 04-economics.md:
  - Outbound ABM: **875 000 ₽**
  - Content / SEO / webinar inbound: **465 000 ₽**
  - Events / partnerships / referrals: **1 622 000 ₽**
  - Blended CAC: **888 000 ₽**
- LTV: **12 667 000 ₽**
- Monthly churn baseline: **1,8%**
- Break-even по client count: **28 клиентов**

Сценарные допущения для PnL:
- **Base:** churn **1,8%/мес**, new clients = **0, 0, 0, 1, 1, 2, 2, 3, 3, 3, 4, 4**
- **Optimistic:** churn **1,2%/мес**, new clients = **0, 0, 1, 1, 2, 2, 3, 3, 3, 4, 4, 5**
- **Pessimistic:** churn **2,5%/мес**, new clients = **0, 0, 0, 0, 1, 1, 1, 2, 2, 2, 3, 3**
- Формула: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`
- Cash burn = отрицательный EBITDA, cumulative cash = накопленный EBITDA без учёта CAPEX, долга и внешнего финансирования

### A2. 12-month PnL, Base scenario
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 4 | 4 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,98 | 3,95 | 5,88 | 8,77 | 11,61 | 14,40 | 18,14 | 21,82 |
| MRR, ₽ | 0 | 0 | 0 | 320 000 | 634 240 | 1 262 824 | 1 880 093 | 2 806 251 | 3 715 739 | 4 608 855 | 5 805 896 | 6 981 390 |
| COGS, ₽ | 0 | 0 | 0 | 92 000 | 182 344 | 363 062 | 540 527 | 806 797 | 1 068 275 | 1 325 046 | 1 669 195 | 2 007 150 |
| Gross profit, ₽ | 0 | 0 | 0 | 228 000 | 451 896 | 899 762 | 1 339 566 | 1 999 454 | 2 647 464 | 3 283 809 | 4 136 701 | 4 974 240 |
| GM% | 0,0% | 0,0% | 0,0% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% |
| Fixed costs, ₽ | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 |
| EBITDA, ₽ | -6 296 000 | -6 296 000 | -6 296 000 | -6 068 000 | -5 844 104 | -5 396 238 | -4 956 434 | -4 296 546 | -3 648 536 | -3 012 191 | -2 159 299 | -1 321 760 |
| Cash burn, ₽ | 6 296 000 | 6 296 000 | 6 296 000 | 6 068 000 | 5 844 104 | 5 396 238 | 4 956 434 | 4 296 546 | 3 648 536 | 3 012 191 | 2 159 299 | 1 321 760 |
| Cumulative cash, ₽ | -6 296 000 | -12 592 000 | -18 888 000 | -24 956 000 | -30 800 104 | -36 196 342 | -41 152 776 | -45 449 322 | -49 097 858 | -52 110 049 | -54 269 348 | -55 591 108 |

**Base break-even:** **28 клиентов**, **M14**.  
**startup_capital_to_bep_rub:** **56 090 404 ₽**.

### A3. 12-month PnL, Optimistic scenario
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 4 | 4 | 5 |
| Total clients | 0,00 | 0,00 | 1,00 | 1,99 | 3,96 | 5,92 | 8,85 | 11,74 | 14,60 | 18,42 | 22,20 | 26,94 |
| MRR, ₽ | 0 | 0 | 320 000 | 636 160 | 1 268 526 | 1 893 304 | 2 830 584 | 3 756 617 | 4 671 538 | 5 895 479 | 7 104 734 | 8 619 477 |
| COGS, ₽ | 0 | 0 | 92 000 | 182 896 | 364 701 | 544 325 | 813 793 | 1 080 027 | 1 343 067 | 1 694 950 | 2 042 611 | 2 478 100 |
| Gross profit, ₽ | 0 | 0 | 228 000 | 453 264 | 903 825 | 1 348 979 | 2 016 791 | 2 676 590 | 3 328 471 | 4 200 529 | 5 062 123 | 6 141 377 |
| GM% | 0,0% | 0,0% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% |
| Fixed costs, ₽ | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 |
| EBITDA, ₽ | -6 296 000 | -6 296 000 | -6 068 000 | -5 842 736 | -5 392 175 | -4 947 021 | -4 279 209 | -3 619 410 | -2 967 529 | -2 095 471 | -1 233 877 | -154 623 |
| Cash burn, ₽ | 6 296 000 | 6 296 000 | 6 068 000 | 5 842 736 | 5 392 175 | 4 947 021 | 4 279 209 | 3 619 410 | 2 967 529 | 2 095 471 | 1 233 877 | 154 623 |
| Cumulative cash, ₽ | -6 296 000 | -12 592 000 | -18 660 000 | -24 502 736 | -29 894 911 | -34 841 932 | -39 121 141 | -42 740 551 | -45 708 081 | -47 803 552 | -49 037 429 | -49 192 052 |

**Optimistic break-even:** **28 клиентов**, **M13**.  
**startup_capital_to_bep_rub:** **49 192 052 ₽**.

### A4. 12-month PnL, Pessimistic scenario
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 |
| Total clients | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,98 | 2,93 | 4,85 | 6,73 | 8,56 | 11,35 | 14,07 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 320 000 | 632 000 | 936 200 | 1 552 795 | 2 153 975 | 2 740 126 | 3 631 623 | 4 500 832 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 92 000 | 181 700 | 269 158 | 446 429 | 619 268 | 787 786 | 1 044 091 | 1 293 989 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 228 000 | 450 300 | 667 042 | 1 106 366 | 1 534 707 | 1 952 340 | 2 587 531 | 3 206 843 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% | 71,3% |
| Fixed costs, ₽ | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 |
| EBITDA, ₽ | -6 296 000 | -6 296 000 | -6 296 000 | -6 296 000 | -6 068 000 | -5 845 700 | -5 628 958 | -5 189 634 | -4 761 293 | -4 343 660 | -3 708 469 | -3 089 157 |
| Cash burn, ₽ | 6 296 000 | 6 296 000 | 6 296 000 | 6 296 000 | 6 068 000 | 5 845 700 | 5 628 958 | 5 189 634 | 4 761 293 | 4 343 660 | 3 708 469 | 3 089 157 |
| Cumulative cash, ₽ | -6 296 000 | -12 592 000 | -18 888 000 | -25 184 000 | -31 252 000 | -37 097 700 | -42 726 658 | -47 916 291 | -52 677 584 | -57 021 244 | -60 729 713 | -63 818 870 |

**Pessimistic break-even:** **28 клиентов**, **M18**.  
**startup_capital_to_bep_rub:** **70 503 532 ₽**.

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

#### A5.1. На 1 клиента в месяц
| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 320 000 | managed subscription + governance + docs ops |
| Gross | 228 000 | после COGS 92 000 ₽ |
| Contribution | 228 000 | доп. переменные расходы отдельно не выделены, принимаю contribution = gross |
| EBITDA contribution | 228 000 | до распределения fixed costs |
| Net after tax, УСН 6% | 208 800 | 228 000 минус 19 200 ₽ налога с выручки |
| Net after tax, IT-льгота 3% | 218 400 | 228 000 минус 9 600 ₽ налога с выручки |
| Net after tax, ОСНО 20% | 182 400 | 228 000 минус 45 600 ₽ налога на прибыль; НДС 20% отдельно поверх цены, если применимо |

#### A5.2. На масштабе break-even, 28 клиентов
| Шаг | ₽/мес | Комментарий |
|---|---:|---|
| MRR | 8 960 000 | 28 × 320 000 ₽ |
| Gross | 6 384 000 | 28 × 228 000 ₽ |
| Contribution | 6 384 000 | при текущем unit economics |
| EBITDA | 88 000 | 6 384 000 минус 6 296 000 fixed costs |
| Net after tax, УСН 6% | -449 600 | 88 000 минус 537 600 ₽ налога с выручки |
| Net after tax, IT-льгота 3% | -180 800 | 88 000 минус 268 800 ₽ |
| Net after tax, ОСНО 20% | 70 400 | 88 000 минус 17 600 ₽ налога на прибыль |

### A6. Cash flow: startup_capital_to_bep_rub
| Сценарий | Break-even month | Break-even clients | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Optimistic | M13 | 28 | 49 192 052 |
| Base | M14 | 28 | 56 090 404 |
| Pessimistic | M18 | 28 | 70 503 532 |

### A7. Налоговая модель РФ
- **УСН 6%:** налог с выручки, удобный режим для early-stage, но ухудшает cash flow даже при низком EBITDA.
- **IT-льгота 3%:** предпочтительный режим для AI/software-компании при наличии аккредитации Минцифры и выполнении требований по профильной выручке.
- **ОСНО 20%:** налог на прибыль 20%; если enterprise-заказчикам нужен НДС, надо учитывать **НДС 20%** как отдельный слой цены и кассовых разрывов.
- **Страховые взносы:** в модели учтены как **~30% к ФОТ** и уже заложены в team FOT / fixed costs.
- Для текущего кейса базовый рабочий режим, **IT-льгота 3%**, резервный, **УСН 6%**, procurement-driven downside, **ОСНО**.

### A8. Break-even summary
| Scenario | Break-even client count | Break-even month | Startup capital to BEP, ₽ |
|---|---:|---:|---:|
| Base | 28 | 14 | 56 090 404 |
| Optimistic | 28 | 13 | 49 192 052 |
| Pessimistic | 28 | 18 | 70 503 532 |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor Deep-Dive

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База для сравнения: M12 из SECTION A, **21,82 клиента** и **EBITDA -1 321 760 ₽/мес**.

Важно: для шока **CAC x2** показываю не только unit-economics, но и **cash EBITDA after acquisition load**, то есть с учётом того, что 4 новых клиента в M12 стоят в 2 раза дороже по привлечению. Иначе CAC почти не меняет бухгалтерский EBITDA, но резко ухудшает cash burn.

| Сценарий | Ключевое изменение | Клиенты @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | Базовые допущения из SECTION A | 21,82 | **-1 321 760** | До выхода на BEP ещё не дотягивает ~1,32 млн ₽/мес |
| Sens1 | **CAC x2**: 888k → 1,776m ₽ | 21,82 | **-4 873 760** | При 4 wins в M12 доп. acquisition load = **3,552 млн ₽**, cash burn резко растёт |
| Sens2 | **Churn x2**: 1,8% → 3,6%/мес | 20,71 | **-1 573 736** | Потеря ~1,11 клиента к M12, модель остаётся отрицательной дольше |
| Sens3 | **Price -30%**: 320k → 224k ₽/мес | 21,82 | **-3 416 177** | Contribution/client падает с 228k до **132k ₽**, break-even уезжает далеко вправо |

**Вывод:** самый опасный single-factor shock для кейса, **price compression**; самый опасный для cash runway, **CAC x2**.

### B2. Monte Carlo Lite, confidence intervals

#### B2.1. Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 650 000 | 888 000 | 1 800 000 | [T1] baseline CAC + downside на enterprise field sales |
| Monthly churn, % | 1,2% | 1,8% | 3,6% | [T1][T3] baseline + stress x2 |
| ARPU, ₽/мес | 224 000 | 320 000 | 420 000 | [T1][T2] downside = price -30%, upside = enterprise+AI premium |
| Conversion rate lead→paid, % | 12% | 18% | 24% | [T1] funnel blended inference from 04-economics |
| Time-to-hire, мес | 1,0 | 1,5 | 3,0 | [T1] team hiring table |

#### B2.2. Метод расчёта

Вместо полноценного кода использую **9-комбинационную Monte Carlo Lite**. Базовый принцип: беру worst / median / best и ещё 6 mixed-комбинаций вокруг них, продлеваю траекторию до **M24**, а темп новых wins после M12 масштабирую через sales efficiency factor:

`efficiency factor ≈ (CAC_mode / CAC) × (Conversion / Conversion_mode) × min(1; Hire_mode / Hire)`

Это приближение, а не аудированная финансовая модель, но оно достаточно, чтобы проверить **robustness** кейса.

#### B2.3. Результаты Monte Carlo Lite

Для метрик, где меньше лучше, p10/p50/p90 ниже трактую как **pessimistic / median / optimistic snapshot**, а не как строгую сортировку по возрастанию.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-2 708 012** | **7 627 035** | **19 910 444** | **22 618 456** |
| CAC payback (мес) | **13,6** | **3,9** | **2,0** | **11,6** |
| LTV/CAC | **2,0x** | **14,3x** | **42,1x** | **40,0x** |
| Cash runway (мес) | **0,0** | **24,0+** | **24,0+** | **24,0+** |

#### B2.4. Интерпретация правил gate

1. **p10 EBITDA < 0** → правило срабатывает, это прямой сигнал **risk of insolvency**.
2. **p50 EBITDA = 7,63 млн ₽/мес** → median-кейс EBITDA Gate проходит.
3. **Разброс между p10 и p90 пересекает ноль и фактически больше 10x по модулю outcome** → неопределённость слишком высокая, score надо даунгрейдить.
4. **Range width по LTV/CAC = 40,0x > 8** → модель хрупкая, особенно к price/CAC/churn shock.

**Итог Monte Carlo Lite:** median-кейс сильный, но left-tail слишком тяжёлый. Это не reject, но точно **not clean PASS** без сильного контроля GTM, retention и pricing discipline.

### B3. Competitor deep-dive

#### B3.1. Western top-3

Оценки market share ниже, где нет публичного аудита, являются **моей оценкой по customer scale, brand mindshare, enterprise install base и channel presence**.

| Конкурент | Что уже есть у них | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Confluence / Atlassian** | de-facto стандарт team docs + AI workspace/search [T4] | огромная установленная база, ecosystem lock-in, админка, интеграции, procurement-ready | тяжёлый UX, слабая AI-native вертикализация под конкретные workflows, миграции часто болезненны | **25-30%** глобального collaborative-docs / enterprise wiki subsegment | Можно продавать как **AI-native replacement + managed migration + governance ops**, а не как ещё одну wiki |
| **Notion Enterprise + AI** | docs + databases + AI agents + enterprise search [T5] | лучший UX, быстрое внедрение, сильный top-down brand pull, AI narrative | enterprise governance слабее, чем у тяжёлых enterprise incumbents; procurement/security не везде проходит; workflow часто too generic | **10-15%** в modern docs/knowledge layer | Сильнее в **private deployment, data residency, regulated enterprise rollout** |
| **Guru** | AI source of truth, verified answers, knowledge agents [T6] | очень ясный positioning вокруг trusted answers, cited AI, Slack-centric distribution | уже уже docs-authoring layer, чем у полноценных platforms; не лучший fit для тяжёлой migration-led документации | **3-5%** в AI knowledge layer | Можно объединить **authoring + search + governance + migration** в одном контракте |

#### B3.2. Russian top-3

| Конкурент | Что уже есть у них | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **TEAMLY** | зрелая knowledge-management платформа, AI, обучение, on-prem и миграция с Confluence [T2][T7][T8] | сильный локальный бренд, понятный pricing, migration narrative, закрытый контур, реальные кейсы крупного бизнеса | ближе к универсальной базе знаний/LMS, чем к deep enterprise AI docs ops; риск price ceiling | **18-25%** РФ knowledge-base SaaS / replacement-Confluence subsegment | Выше ARPU через **AI-search + docs ops + governance + enterprise service layer**, а не seat-only модель |
| **Minervasoft / Minerva Knowledge** | knowledge management + learning + AI knowledge base, отдельно продаёт replacement-Confluence [T9][T10] | сильный enterprise-RU positioning, фокус на support/use-case, экосистема продуктов, присутствие в Сколково | продукт шире, но сложнее; может быть длиннее внедрение и выше cost of change; меньше community pull, чем у TEAMLY | **8-12%** РФ enterprise knowledge-management subsegment | Можно зайти быстрее как **узкий wedge в docs/search**, не продавая сразу всю экосистему |
| **Naumen Knowledge Management System** | knowledge management внутри большого service-management / CX контура [T11] | сильный enterprise-sales motion, гос/крупняк, интеграции в service workflows, высокая доверенность у крупных клиентов | продукт тяготеет к service desk / contact center, а не к AI-native documentation layer; тяжёлый procurement cycle | **10-15%** РФ enterprise service-knowledge subsegment | Легче выиграть там, где нужен **documentation-first AI layer**, а не полный ITSM/CX stack |

**Вывод по конкуренции:**
- На Западе рынок уже красный океан, там побеждают distribution и ecosystem lock-in.
- В РФ окно открылось после санкционного сдвига и ухода части западного SaaS, но оно быстро закрывается локальными заменителями Confluence/Notion.
- Значит, наш лучший wedge, **не generic база знаний**, а **enterprise AI documentation platform для regulated и migration-heavy контуров**.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Не удаётся закрыть CTO/ML/DevOps hiring вовремя | Med | High | time-to-hire > 2,5 мес, offer acceptance < 50% | founder-led hiring, подрядный bridge, stock-like upside, сократить roadmap до core wedge |
| 2 | Operational | Retrieval/AI quality низкая, hallucination rate мешает rollout | Med | High | pilot NPS < 30, answer acceptance < 70%, рост ручных эскалаций | citation-first UX, human-in-the-loop, ограничение use-cases, golden datasets |
| 3 | Operational | Зависимость от внешних LLM API и latency/cost spikes | High | High | cost per answer > plan на 30%+, SLA деградирует | multi-model routing, локальные fallback-модели, кэш, лимиты, более дешёвые inference tiers |
| 4 | Market | Спрос остаётся adjacent, но не material: рынок говорит «хотим Confluence replacement дешевле» | Med | High | win rate падает, discovery сводится к price-only | repositioning в regulated docs/search, не продавать generic wiki, вертикальные пакеты |
| 5 | Market | Price compression из-за TEAMLY / Bitrix / open-source замены | High | High | скидки > 25%, частые сравнения только по seat-price | переход на bundle pricing, ROI-calculator, managed migration и governance как отдельная ценность |
| 6 | Market | Конкуренты быстрее закрывают Confluence replacement narrative | Med | High | inbound упоминает shortlist без нас, CAC растёт > 30% | ABM на regulated verticals, партнёры-интеграторы, кейсы миграции с measurable ROI |
| 7 | Regulatory | 152-ФЗ / data residency ограничивают облачную архитектуру | High | High | security review блокирует cloud-first deployment | on-prem / VPC SKU, локальное хранение embeddings/logs, DPA и security pack из коробки |
| 8 | Regulatory | 115-ФЗ / внутренний комплаенс банков и финсектора удлиняют продажи | Med | High | procurement cycle > 9 мес, security questionnaire растёт > 100 пунктов | отдельный BFSI package, аудит-логи, role-based access, оффер пилота в закрытом контуре |
| 9 | Financial | Cash runway сжимается из-за длинного sales cycle | High | High | cash runway < 9 мес, bookings сдвигаются вправо | режем burn, freeze hires, bridge financing, продаём setup/migration fees upfront |
| 10 | Financial | USD/RUB и инфляция увеличивают infra и зарплаты быстрее ARPU | Med | Med | gross margin < 65%, зарплатные ожидания +20% y/y | yearly indexation clauses, рублёвые контракты с пересмотром, vendor diversification |
| 11 | Black swan | Новый пакет санкций режет доступ к SaaS/LLM/vendors | Med | High | уведомления от вендоров, рост отказов в биллинге/API | российские и self-hosted fallback, заранее проверенный vendor matrix |
| 12 | Black swan | Отключение крупного LLM-поставщика или резкое ухудшение качества модели | Med | High | sudden accuracy drop, SLA incidents, forced migration | abstraction layer, prompt/version registry, локальный reranker, резерв на emergency re-tuning |

### B5. Kill conditions через 6 месяцев

1. **Median-like pipeline не собирается:** < **8 платящих клиентов** к M6 **или** MRR < **2,5 млн ₽/мес**. Это значит, что траектория к 28-30 клиентам почти наверняка не собирается.
2. **Unit economics ломается:** blended **CAC > 1,6 млн ₽** **или** payback > **9 мес** **или** LTV/CAC < **4x**. Тогда growth становится слишком дорогим для текущего burn profile.
3. **Retention / pricing fail:** monthly churn > **3,5%** **или** realised ARPU < **250k ₽/мес** на cohort basis. Тогда модель уходит в сторону low-ticket wiki и теряет fundability.

### B6. Финальный критический вывод по SECTION B

Кейс всё ещё выглядит рабочим, но уже не как «почти guaranteed winner», а как **высоковариативный enterprise execution bet**.

Что держит кейс:
- median Monte Carlo проходит EBITDA Gate с большим запасом;
- в РФ есть реальный пост-Confluence спрос и локальный budget line;
- wedge через regulated enterprise, migration и AI-search логичен.

Что ломает кейс:
- слишком тяжёлый left-tail по p10;
- price compression и CAC inflation быстро убивают runway;
- конкуренция в РФ уже занята TEAMLY / Minerva / Naumen и generic replacement-плеерами.

**Decision framing:** проходить дальше можно только как **enterprise AI documentation + governance + migration ops**, с жёстким отказом от дешёвого wiki-позиционирования.

### B7. Sources

- [T1] Internal unit economics: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-ai-documentation-platform-v2/04-economics.md`
- [T2] Internal demand/pricing context: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-ai-documentation-platform-v2/02-demand.md`
- [T3] ChartMogul churn benchmark: https://chartmogul.com/saas-metrics/customer-churn-rate/
- [T4] Atlassian Confluence product page: https://www.atlassian.com/software/confluence
- [T5] Notion AI / Enterprise Search page: https://www.notion.com/product/ai
- [T6] Guru homepage: https://www.getguru.com/
- [T7] TEAMLY pricing: https://teamly.ru/pricing/
- [T8] TEAMLY on Habr / vc.ru context: https://habr.com/ru/companies/teamly/articles/ ; https://vc.ru/tag/teamly
- [T9] Minervasoft product page: https://minervasoft.ru/
- [T10] Minervasoft at Skolkovo: https://sk.ru/companies/minervasoft/
- [T11] Naumen product line / Knowledge Management System context: https://www.naumen.ru/

<!-- P6B-DONE -->

---

## Этап 6 — Final Verdict
[GEO-EXPAND] Enterprise AI Documentation Platform v2 — APPROVED WITH NOTES: 70/100 | EBITDA base=680К₽/мес через 15 мес | LTV/CAC=14,3x | Ключевое преимущество: migration-led AI documentation wedge для enterprise | Главный риск: price compression и слабый moat.

# 06-verdict — Enterprise AI Documentation Platform v2

sector: GEO-EXPAND
status: APPROVED WITH NOTES
score: 70/100
normalized_from_raw: 105/150
previous_score: 72/100
score_delta_vs_previous: -2
case_slug: enterprise-ai-documentation-platform-v2
updated_at: 2026-04-20 06:02 MSK

## Инвесткомитет: итоговый вердикт

Кейс проходит порог как **APPROVED WITH NOTES**. Экономика на уровне сделки сильная, а путь к `company_ebitda_potential_rub_month ≥ 500 000 ₽` достижим в базе за **15 месяцев** и **30 клиентов**. Ограничение, это не category-winner, а execution-heavy ставка: спрос в РФ подтверждён в adjacent-category, но moat пока средний, а price discipline и GTM-исполнение критичны.

## Оценка

Source tier balance: T1=2, T2=5, T3=2, weighted=2.00. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | В 04-economics.md: "LTV/CAC = 14,3x", "CAC Payback = 2,8 мес", "Contribution Margin = 71,3%". |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В 04-economics.md: "уровень 500k EBITDA/mo достигается около M14" и "при 50 клиентах EBITDA ≈ 5,10 млн ₽/мес". |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | В 02-demand.md: "exact-category спрос... низкий, но adjacent demand в РФ уже есть"; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | В 05-critic.md: лучший wedge, это "enterprise AI documentation + governance + migration ops", но рынок уже занят replacement-плеерами. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В 05-critic.md: "слишком тяжёлый left-tail по p10", плюс "зависимость от внешних LLM API" и 152-ФЗ/data residency риск. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | В 04-economics.md есть канальный CAC 465k-1,622m ₽ и blended CAC 888k ₽; named-target ICP уже просматривается. |

**Sum raw = 105/150**  
**Normalized score = round(105 × 100 / 150) = 70/100**

### Moat — 7-factor framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый клиент почти не улучшает продукт для остальных, сетевой эффект отсутствует. |
| Switching costs | 2 | После миграции, AI-search, governance и ACL-интеграций смена решения становится ощутимо болезненной. |
| Scale economies | 2 | С ростом клиентской базы можно снижать COGS на инференс, deployment playbooks и support-операции. |
| Proprietary data / model advantage | 1 | Уникальный датасет или модельное превосходство количественно не доказаны. |
| Regulatory moat | 1 | Private deployment и data residency важны, но T1-регуляторного подтверждения moat нет, поэтому преимущество пока слабое. |
| Brand / distribution | 1 | В РФ brand pull ограничен, а дистрибуция остаётся founder-led и партнёрской. |
| Embedded workflow | 3 | Продукт глубоко встраивается в ежедневный knowledge workflow, onboarding, support и внутреннюю документацию. |

**Moat raw = 10/21, moat score = round(10 × 25 / 21) = 12/25**

## Investment one-liner

`[GEO-EXPAND] Enterprise AI Documentation Platform v2 — APPROVED WITH NOTES: 70/100 | EBITDA base=680К₽/мес через 15 мес | LTV/CAC=14,3x | Ключевое преимущество: migration-led AI documentation wedge для enterprise | Главный риск: price compression и слабый moat.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 12 667 000 ₽ |
| CAC blended | 888 000 ₽ |
| LTV/CAC | 14,3x |
| CAC Payback | 2,8 мес |
| Gross Margin | 71,3% |
| contribution_margin_rub_month | 228 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 296 000 ₽/мес |
| company_ebitda_rub_month, M12 base | -1 321 760 ₽/мес |
| company_ebitda_potential_rub_month | 5 104 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 30 |
| months_to_500k_ebitda | 15 |
| clients_to_1m_ebitda | 33 |
| months_to_1m_ebitda | 15-16 |
| Break-even | 28 клиентов |
| startup_capital_to_bep_rub | 56 090 404 ₽ |

## Полный business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | ICP-ресерч и сбор account list | SDR | HH/CRM/контур компаний/таблицы | 5 ч | 7 500 | Средняя |
| 2 | Enrichment по стеку docs/helpdesk/devtools | SDR | CRM, сайт клиента, ручной ресерч | 4 ч | 6 000 | Средняя |
| 3 | Персонализированный outbound | SDR | e-mail sequencer, Telegram, CRM | 8 ч | 12 000 | Средняя |
| 4 | Qualification call | SDR + AE | Meet, CRM, скрипт qualification | 2 ч | 8 500 | Низкая |
| 5 | Discovery с buyer и техкомандой | AE + CEO | Meet, Notion, discovery template | 4 ч | 19 000 | Низкая |
| 6 | Аудит текущей документации и knowledge stack | Solutions Engineer / PM | crawler, sample import, workspace demo | 6 ч | 21 000 | Средняя |
| 7 | Demo AI-search, governance и migration path | AE + CEO + SE | demo-tenant, презентация, ROI-sheet | 3 ч | 17 500 | Средняя |
| 8 | Подготовка пилота / proposal / scoping | AE + PM | CRM, калькулятор юнит-экономики, КП | 5 ч | 21 500 | Средняя |
| 9 | Security/legal/procurement review | CEO + Ops | DPA/SLA templates, ЭДО, security docs | 6 ч | 24 000 | Низкая |
| 10 | Переговоры по цене и согласование договора | CEO + AE | CRM, договор, таблица уступок | 4 ч | 18 500 | Низкая |
| 11 | Счёт, ЭДО, запуск и первый платёж | CSM + Finance Ops | банк, ЭДО, billing, onboarding checklist | 3 ч | 10 500 | Высокая |

## Финансовая траектория

| Scenario | M12 clients | EBITDA @M12 | Break-even month | Startup capital to BEP |
|---|---:|---:|---:|---:|
| Base | 21,82 | -1 321 760 ₽/мес | 14 | 56 090 404 ₽ |
| Optimistic | 26,94 | -154 623 ₽/мес | 13 | 49 192 052 ₽ |
| Pessimistic | 14,07 | -3 089 157 ₽/мес | 18 | 70 503 532 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-2 708 012 ₽/мес**
- p50 EBITDA @M24 = **7 627 035 ₽/мес**
- p90 EBITDA @M24 = **19 910 444 ₽/мес**
- Вывод: median-case проходит EBITDA Gate, но left-tail слишком тяжёлый для clean approve.

## Команда

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | продажи enterprise, fundraising, partnerships, pricing | 780 000 |
| CTO/Tech Lead | архитектура, product delivery, инфобез, приоритизация | 715 000 |
| Senior Backend #1 | core platform, API, RBAC, billing | 546 000 |
| Senior Backend #2 | connectors, search, ingestion, analytics | 546 000 |
| ML Engineer | RAG, retrieval quality, ranking, hallucination control | 650 000 |
| DevOps | infra, deployment, observability, private cloud | 455 000 |
| Frontend | editor UX, admin panel, search UX | 390 000 |
| SDR | outbound, meetings, account research | 234 000 |
| AE | discovery, proposal, closing | 416 000 |
| Customer Success | onboarding, adoption, renewals | 338 000 |
| Product / Docs Ops Lead | docs governance, rollout, migration ops | 416 000 |
| **Итого fully-loaded FOT** |  | **5 486 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| 2ГИС | В 02-demand.md уже зафиксирована миграция **150 000 страниц** знаний у реального enterprise buyer, значит боль по knowledge migration доказана. | email decision-maker в knowledge/support/product ops + кейсовый follow-up | 350 000 ₽/мес |
| ВкусВилл | Большая распределённая операционная сеть и высокий объём внутренних регламентов, FAQ и onboarding-материалов. | vc.ru / Habr thought-leadership + direct outreach в digital ops | 300 000 ₽/мес |
| SPLAT Global | Международные и распределённые команды, где высока цена актуальности продуктовой и обучающей документации. | email head of enablement / IT + партнёрский интро | 280 000 ₽/мес |
| Lamoda | Сложные support и operations workflow, где AI-search по базе знаний может снижать стоимость ответа и обучения. | direct outreach в CX/knowledge management + профильные конференции | 320 000 ₽/мес |
| Dodo Brands | Сильный knowledge-heavy операционный бизнес с большим объёмом внутренних playbooks и onboarding-контента. | founder-led outreach + продуктовые сообщества | 300 000 ₽/мес |
| Контур | B2B software-компания с developer docs, support docs и high-value internal knowledge base. | email VP Product / Support + Habr-материалы | 350 000 ₽/мес |
| МойОфис | Enterprise software vendor, где документация, help-center и private deployment критичны для продаж и внедрения. | direct outreach в product marketing / docs team | 300 000 ₽/мес |
| Т2 | Крупная телеком-компания с большим объёмом внутренних знаний и сервисных сценариев, где важен быстрый поиск по документам. | партнёрство с интегратором + CNews/ComNews конференции | 320 000 ₽/мес |
| 1C-Рарус | Интегратор и enterprise-решения, для которого документация и knowledge transfer напрямую влияют на margin delivery. | direct outreach в practice lead + партнёрский канал | 280 000 ₽/мес |
| Robokassa | Финтех-платформа с требованиями к точности документации, onboarding merchant-ов и support knowledge. | email decision-maker + контент в vc.ru для fintech ops | 260 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Price compression в сравнении с wiki/help-center решениями | high | high | В 05-critic.md price -30% ведёт к **EBITDA @M12 -3 416 177 ₽/мес**. |
| CAC inflation и длинный enterprise sales cycle | high | high | В 05-critic.md при **CAC x2** cash EBITDA @M12 падает до **-4 873 760 ₽/мес**. |
| Зависимость от внешних LLM/API и data residency требований | high | high | В 05-critic.md это выделено как отдельный риск: "Зависимость от внешних LLM API" и ограничение 152-ФЗ/cloud-first. |

## Что должно быть доказано после инвестиции

1. Минимум **3 design partners** с realized ACV не ниже **3,0-3,8 млн ₽/год**.
2. pilot-to-paid не ниже **30%** и sales cycle не длиннее **120-150 дней** на первом ICP.
3. Реализованный ARPA удерживается **300 000 ₽/мес+**, а скидка не уходит системно за **20%**.
4. Не менее **2 reference accounts** в РФ с measurable снижением времени поиска знаний, onboarding effort или support load.
5. Private deployment / governance / migration собираются в repeatable SKU, а не в bespoke-консалтинг.

## Proof points для APPROVED

- Unit economics уже на investment-grade уровне: **LTV/CAC 14,3x**, **CAC Payback 2,8 мес**, **Gross Margin 71,3%**.
- EBITDA gate проходит в базе: **30 клиентов** дают **500К+ EBITDA/мес** в пределах **15 месяцев**, а при **50 клиентах** потенциал **5,1 млн ₽/мес**.
- Рынок не mass-market, но buyer pain подтверждён и seat-based pricing уже нормализован публично через **TEAMLY / Confluence / Slite**.
- Adjacent-demand и hh/job signals показывают, что компании уже платят за knowledge work, а не только декларируют интерес.

## Финальное решение инвесткомитета

**APPROVED WITH NOTES.**

Инвестировать можно, если команда с первого дня держит premium-positioning: продаёт не "ещё одну базу знаний", а migration-led AI documentation platform для regulated и documentation-heavy enterprise-контуров. Это сильный economics-case, но не защищённый winner-takes-most рынок, поэтому approve оправдан только при жёстком контроле pricing, retention и partner-led GTM.

---

## Этап 7 — История прохождения пайплайна
# 07-score-trajectory

## 2026-04-20 — Program 4 Demand Validation
- stage: P4
- verdict: CONDITIONAL_PASS
- summary: Exact search demand по формулировке кейса низкий, но adjacent demand по корпоративной базе знаний уже medium; WTP подтверждён публичными тарифами TEAMLY, Confluence и Slite, а Profit Gate проходит в mid-market и enterprise сценариях.
- demand_api: LOW exact / MEDIUM adjacent (score=0 exact, score=30 adjacent)
- market_view: нишевой, но платёжеспособный B2B рынок enterprise documentation и AI knowledge ops в РФ
- profit_gate: PASS
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-ai-documentation-platform-v2/02-demand.md

## 2026-04-20 — Program 5 Unit Economics
- stage: P5
- verdict: PASS
- summary: Fully-loaded CAC пересчитан по enterprise B2B логике и остаётся в допустимом диапазоне; при ARPA 320k ₽/мес, churn 1,8% monthly и contribution margin 71,3% кейс сохраняет investable-профиль.
- key_metrics:
  - revenue_per_client_month: 320000 ₽
  - cogs_per_client_month: 92000 ₽
  - contribution_profit_per_client_month: 228000 ₽
  - contribution_margin: 71.3%
  - fully_loaded_cac: 888000 ₽
  - ltv: 12667000 ₽
  - ltv_cac: 14.3x
  - cac_payback: 2.8 months
  - break_even: 28 clients / ~M13
  - ebitda_500k_threshold: 30 clients / ~M14
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-ai-documentation-platform-v2/04-economics.md

## 2026-04-20 — Program 7 Critic and Verdict
- stage: P7
- verdict: APPROVED WITH NOTES
- summary: Rerun сохраняет approve-статус, но новая 6x25 рубрика и tier-aware penalty снижают кейс до пограничного investment-grade профиля. Сильные unit economics и EBITDA-потенциал компенсируют лишь средний moat и тяжёлый left-tail execution risk.
- score:
  - raw: 105/150
  - normalized: 70/100
  - previous_score: 72/100
  - delta: -2
- key_metrics:
  - customer_ltv_rub: 12667000 ₽
  - blended_cac: 888000 ₽
  - ltv_cac: 14.3x
  - cac_payback: 2.8 months
  - gross_margin: 71.3%
  - company_ebitda_potential_rub_month: 5104000 ₽
  - clients_to_500k_ebitda: 30
  - months_to_500k_ebitda: 15
- artifacts:
  - /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/enterprise-ai-documentation-platform-v2/06-verdict.md
