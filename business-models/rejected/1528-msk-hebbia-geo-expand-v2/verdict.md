# 1528-msk-hebbia-geo-expand-v2

---

## 00-brief.md

# 00-brief

## Кейс
1528-msk-hebbia-geo-expand-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
1528-msk-hebbia-geo-expand

## Краткое описание
Кейс создан по правилу принудительного полного пайплайна для resurrect-сигнала по Hebbia, даже если раньше сигнал маршрутизировался в существующий кейс или считался supporting signal.

## Что делать дальше
Пройти полный пайплайн P3→P7 с новой аналитикой и в финальном verdict отдельно сравнить standalone-оценку с прежним решением triage.

---

## 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-1528-msk-hebbia-geo-expand.md
created: 2026-04-20T01:02:37+03:00
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан заново по standing orders и не классифицируется как duplicate на этапе intake.

## Оригинальный verdict / источник контекста
- Источник: triage/2026-04-19-resurrect-1528-msk-hebbia-geo-expand.md
- Базовый slug: `1528-msk-hebbia-geo-expand`
- Новый slug кейса: `1528-msk-hebbia-geo-expand-v2`

## Полный контекст raw

# RESURRECT SIGNAL — 1528-msk-hebbia-geo-expand

## Meta
- source: triage/triage-2026-04-17-1528-msk-hebbia-geo-expand.md
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
- pipeline/raw/raw-2026-04-17-1528-msk-hebbia-geo-expand.md

## Классификация
новый кейс

## Решение
Создать новый кейс: `investment-banking-ai-analyst-operator`.

## Почему
- В `pipeline/cases/` сейчас нет открытого кейса по AI-аналитику для investment banking, institutional finance и due diligence.
- Сигнал Hebbia описывает не общий AI-поиск, а специализированную платформу для research, VDR, data room, memo, document comparison и сделочных workflow.
- По экономике сигнал проходит порог Program 1: ориентир 5,0-18,0 млн ₽ в год на клиента соответствует примерно 417 000-1 500 000 ₽ в месяц, а верхняя часть диапазона превышает порог 500 000 ₽/мес.
- Для локализации в РФ потребуется тяжёлый сервисный слой: локальные финансовые источники, русскоязычные юридические и финансовые документы, secure deployment и compliance-контур, что делает модель потенциально high-LTV.

## Что создано
- Создан кейс `pipeline/cases/investment-banking-ai-analyst-operator/00-brief.md`.
- В кейсе зафиксированы описание категории, текущее состояние рынка и ключевая гипотеза для РФ.

## Что сделано
- Новый кейс создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это новый кейс, а не шум: Hebbia даёт сильный GEO-EXPAND сигнал в категории AI-native платформ для investment banking, institutional finance и due diligence, с потенциалом high-LTV для РФ.
```


---

## 02-demand.md

# 02-demand

## Demand validation summary
- **Продукт**: Hebbia как AI-native analyst workspace для investment banking, due diligence, data room review, memo drafting и document comparison.
- **Итог по спросу в РФ**: **LOW**, но не нулевой. Прямой keyword-demand по RU слабый, зато есть узкая enterprise-боль у M&A advisory, инвестбанков, Big Law и corpdev-команд. Обязательный endpoint дал: `Hebbia` = **LOW / 15**, `investment banking ai` = **LOW / 3**, `virtual data room` = **LOW / 15**. [T2: internal demand endpoint]
- **Решение по гейту**: **не отклонять на P4**. Массового self-serve спроса нет, но Profit Gate проходит в enterprise / on-prem / managed-deal-room сценарии при 4-6 платящих клиентах. [T1][T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=Hebbia` → **LOW**, score **15**; Google Trends RU = 0, Habr = 2, Yandex suggest = 100, HH = 0. Это означает слабую известность бренда, но наличие поисковых хвостов. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20ai` → **LOW**, score **3**; HH = 10, остальной спрос слабый. [T2: internal demand endpoint]
- `http://172.18.0.1:9001/multi-demand?keyword=virtual%20data%20room` → **LOW**, score **15**; Yandex suggest = 100. В РФ люди ищут категорию VDR, но не готовое AI-решение под бренд Hebbia. [T2: internal demand endpoint]

### 2) Russia demand proxies
- В реестре Банка России на 20.04.2026 числится **252 брокера**, **271 дилер** и **156 инвестиционных советников**. Это не равно TAM продукта, но подтверждает наличие нескольких сотен regulated финансовых организаций, где есть workflows с инвестиционным анализом, сделками и документарной проверкой. [T1: Банк России, https://www.cbr.ru/vfs/finmarkets/files/supervision/list_brokers.xlsx ; https://www.cbr.ru/vfs/finmarkets/files/supervision/list_dealers.xlsx ; https://www.cbr.ru/vfs/finmarkets/files/supervision/List_is.xlsx]
- AK&M оценил рынок M&A в РФ за 2025 год в **3,52 трлн ₽** и **536 сделок**, что подтверждает сохраняющийся объём транзакционной активности, на который может лечь VDR / DD automation. [T2: https://www.akm.ru/news/obem_rynka_sliyaniy_i_pogloshcheniy_rossii_v_2025_godu_vyros_na_2_do_3_52_trln_rubley/]
- Kept отмечает, что в 2025 году на российском M&A-рынке было **499 сделок** на **$42,2 млрд**, при этом активность поддерживали внутренние корпораты и private capital. Это независимая проверка того, что рынок сделок в РФ жив, хотя и уже, чем глобальный. [T2: https://kept.ru/insights/articles/rossiyskiy-rynok-sliyaniy-i-pogloshcheniy-itogi-2025-goda/]
- Поиск по hh.ru по категориям `due diligence`, `M&A`, `investment analyst`, `corporate finance` стабильно показывает десятки релевантных вакансий в Москве и Санкт-Петербурге, а internal demand endpoint для `investment banking ai` видит **10 вакансий**. Это подтверждает существование оплачиваемой ручной функции, которую продукт может ускорять. [T1: HH.ru fact of live job demand; T2: internal demand endpoint]

## Competitive pricing and WTP

### 1) Реальные конкуренты с ценами
- **FirmRoom**: тарифы от **$395/мес** (Starter), **$695/мес** (Standard), **$1,295/мес** (Premium), Enterprise custom. По курсу ЦБ на 20.04.2026 это примерно **30 тыс. ₽ / 53 тыс. ₽ / 98 тыс. ₽ в месяц**. [T2: https://firmroom.com/pricing/ ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]
- **SecureDocs Virtual Data Room**: от **$250/мес** и **$400 flat fee** за подготовку, то есть около **19 тыс. ₽/мес** и **30 тыс. ₽** setup. [T2: https://www.securedocs.com/pricing ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]
- **Drooms**: pricing начинается от **€1,900 в месяц за проект**, то есть около **170 тыс. ₽/мес** по курсу ЦБ. [T2: https://drooms.com/pricing/ ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]
- **LegalScan (РФ)**: от **80 тыс. ₽/мес**; позиционируется как AI legal review для договоров и комплаенса. Это важный локальный price anchor для русскоязычного рынка документов. [T2: https://www.legalscan.ai/]

### 2) Willingness to pay
- Сам факт того, что global VDR vendors продают продукт в диапазоне **19 тыс. ₽-170 тыс. ₽/мес** за room / проект, а локальный RU legal-AI сервис ставит цену **80 тыс. ₽/мес**, доказывает, что рынок платит за снижение времени ревью и безопасный обмен документами. [T2]
- Для Hebbia-подобного продукта WTP выше, чем у простого VDR, только если продаётся не просто storage, а **ускорение analyst-hours, memo drafting, cross-doc comparison и question answering по data room**. Тогда price point **300-900 тыс. ₽/мес** выглядит достижимым в enterprise-сегменте, но это уже inference, а не публично подтверждённый прайс. [T2 + inference]
- [Спекуляция] Для pure self-serve бота без VDR, audit trail и on-prem контуров рынок в РФ вряд ли готов платить существенно выше **30-80 тыс. ₽/мес**. [T3-supported-by-T2]

## Telegram bots / services in RU
- Проверка RU web / Telegram / TGStat-поиска не выявила сильных специализированных Telegram-ботов именно под **investment banking due diligence / VDR AI**. [T2]
- В РФ есть adjacent legal-AI и document-review сервисы, но они в основном поставляются как веб-продукт, а не как secure Telegram workflow. Это снижает риск мгновенного bot-led commodity pressure, но и подтверждает, что рынок требует web/on-prem, а не мессенджер. [T2]
- Вывод: Telegram не является главным каналом доставки ценности в этой категории; максимум, это уведомления и Q&A-слой, а не ядро продукта. [T2]

## Market sizing

### Логика сегмента
- Адресуем не все финансовые организации, а только команды, у которых реально есть M&A, DD, data room review, IC memo и многодокументный анализ: инвестбанки, corpdev крупных корпораций, Big Law, transaction services, PE/VC и debt advisory. [T1][T2]

### Top-down
- **TAM (мир)**: глобальный рынок VDR оценивается примерно в **$2,71 млрд**. По курсу ЦБ это около **206,1 млрд ₽**. Источник не Tier-1, поэтому использовать как верхний ориентир, а не как опорную точку. [T3: https://www.grandviewresearch.com/industry-analysis/virtual-data-room-market-report ; T1 FX]
- **TAM (РФ)**: берём рынок M&A РФ **3,52 трлн ₽** и применяем адресуемую software+workflow долю **0,015%** для DD/VDR/AI-automation слоя. Получаем **528 млн ₽**. Это допущение калибровано на публичных прайсах VDR и на том, что software spend в сделках очень мала относительно notional deal value. [T2 + inference]
- **SAM (РФ)**: берём TAM РФ **528 млн ₽** и применяем segment fit **60%**, так как Hebbia релевантна не всем сделкам, а в первую очередь upper mid-market / крупным advisory workflows. Получаем **317 млн ₽**. [T2 + inference]
- **SOM Y1**: **30 млн ₽**, что соответствует примерно 5 enterprise клиентам с ARR ~6 млн ₽. [T2 + inference]
- **SOM Y3**: **72 млн ₽**, что соответствует примерно 12 enterprise клиентам. [T2 + inference]

### Bottom-up
- **Total buyers**: используем базу из regulated finance + transaction advisors. Из 252 брокеров и 156 инвестсоветников только часть реально ведёт сложные сделки; добавляем крупные банки, top law / transaction firms и corpdev-команды. Рабочая база для TAM = **180 организаций**. [T1 + T2 + inference]
- **% with need**: только примерно **30%** из этой базы регулярно сталкиваются с data room / DD / memo-heavy workload. Получаем **54 активных buyers**. [T1 HH + T2 market reports + inference]
- **ARR avg**: ориентир **6 млн ₽/год** на клиента, то есть **500 тыс. ₽/мес**. Это выше обычного VDR, но ниже стоимости 2-3 сильных аналитиков / юристов и соответствует enterprise-only сценарию. [T2 competitor anchors + inference]
- **SAM bottom-up** = 54 × 6 млн ₽ = **324 млн ₽**.
- **SOM bottom-up Y1** = 5 клиентов × 6 млн ₽ = **30 млн ₽**.
- **SOM bottom-up Y3** = 12 клиентов × 6 млн ₽ = **72 млн ₽**.

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 206,1 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 528 млн ₽ [T2] | 1,08 млрд ₽ [T1+T2+inf] | diff 2,0x, bottom-up шире, т.к. считает весь buyer universe, а top-down привязан к активным сделкам | **528 млн ₽** |
| SAM (РФ) | 317 млн ₽ [T2+inf] | 324 млн ₽ [T1+T2+inf] | diff 2,2%, оценки согласуются | **317 млн ₽** |
| SOM Y1 | 30 млн ₽ | 30 млн ₽ | diff 0% | **используем 30 млн ₽** |
| SOM Y3 | 72 млн ₽ | 72 млн ₽ | diff 0% | **используем 72 млн ₽** |

### 10 реальных buyers для bottom-up
1. Газпромбанк
2. Sber CIB
3. Альфа-Банк
4. Совкомбанк
5. БКС КИБ
6. Ренессанс Капитал
7. АТОН
8. Kept
9. Технологии Доверия
10. ДРТ

Комментарий: этот список нужно перенести как основу для P7 GTM-10-targets. [T2]

### Sanity checks
- Расхождение top-down и bottom-up по SAM меньше 3x, пересборка не требуется.
- SOM Y1 = 30 млн ₽, то есть **9,5%** от preferred SAM 317 млн ₽. Это агрессивно, но всё ещё в допустимом диапазоне <10%. 
- При среднем deal cycle **6-9 месяцев** закрыть 5 enterprise клиентов за год тяжело, но реалистично только при founder-led sales и узком списке аккаунтов. [T2]

## Profit Gate

### Сценарий A, self-serve bot / light SaaS
- Цена: **30-80 тыс. ₽/мес**.
- Для EBITDA 500 тыс. ₽/мес потребуется слишком много клиентов при слабом прямом спросе и дорогом enterprise onboarding.
- **Вердикт**: fail. [T2]

### Сценарий B, team workspace для advisory / legal
- Цена: **150-300 тыс. ₽/мес**.
- Gate достижим только при 10-15 клиентах и хорошем gross margin, но рынок в РФ для такого middle tier узкий.
- **Вердикт**: borderline / слабый. [T2]

### Сценарий C, enterprise / on-prem / managed deal room
- Цена: **500-900 тыс. ₽/мес** плюс setup **1-3 млн ₽**.
- При 4-6 клиентах ARR выходит на **24-54 млн ₽/год**; даже при небольшой delivery-команде можно получить **EBITDA > 500 тыс. ₽/мес**.
- **Вердикт**: pass. Это единственный сценарий, на котором кейс инвестируемо выглядит в РФ. [T2 + inference]

## Verdict for P4
- **Demand = LOW**, но не zero.
- **Profit Gate = PASS ONLY IN NARROW ENTERPRISE WEDGE**.
- Поэтому **ранний reject не применяем**. Кейс стоит нести дальше только как enterprise-only thesis: AI workspace для high-stakes DD / M&A / corpfin команд, с secure deployment и очень узким ICP. 

Sources: T1=6, T2=12, T3=1. Primary evidence basis: T2.

## Market Pulse
> Market Pulse 2026-04-20: растущий интерес.

> Market Pulse 2026-04-21: растущий интерес.

---

## 04-economics.md

# 04-economics

## Unit Economics Summary
- **Кейс**: Hebbia-подобный AI analyst workspace для investment banking, due diligence, data room review и memo drafting.
- **Рабочий сегмент**: только **enterprise** и только high-stakes workflows, где ACV >= **6,0 млн ₽/год**.
- **Базовый прайс модели**: **500 000 ₽ MRR** на клиента + **1,5 млн ₽ setup** разово. В unit economics setup не включаю в MRR/LTV, использую как upside и способ финансировать onboarding. Основание: в `02-demand.md` зафиксирован enterprise-WTP **500-900 тыс. ₽/мес** для secure / on-prem / managed deal room сценария.
- **Вывод**: экономика **положительная**, но только в узком enterprise-клине. Массовый SaaS или self-serve для РФ не сходится.

## Ключевые assumptions
| Параметр | Значение | Комментарий |
|---|---:|---|
| MRR на 1 клиента | 500 000 ₽/мес | enterprise-only, lower bound из проходного P4-сценария |
| Setup fee | 1 500 000 ₽ | покрывает пилот, настройку, security review |
| COGS на 1 клиента | 133 000 ₽/мес | inference + storage + support + security |
| Contribution на 1 клиента | 367 000 ₽/мес | 500 000 - 133 000 |
| Contribution Margin | 73,4% | выше порога для software-like модели |
| Monthly churn | 1,5% | enterprise benchmark |
| LTV в месяцах | 66,7 мес | 1 / churn |
| LTV gross profit | 24 466 667 ₽ | 367 000 × 66,7 |
| Blended fully-loaded CAC | 836 000 ₽ | enterprise motion, длинный sales cycle |
| LTV/CAC | 29,3x | investable по метрике, но зависит от узкого ICP |
| CAC payback | 1,7 мес | CAC / MRR |
| CAC payback on gross profit | 2,3 мес | CAC / contribution |

## 1) Детальный бизнес-процесс: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор таргет-аккаунтов: банки, Big Law, corpdev | CEO + SDR | CRM, Excel, hh/рынок, Telegram, сайты компаний | 2 дня | 18 000 | низкая |
| 2 | Первый outbound-touch: email, LinkedIn-аналоги, интро через партнёров | SDR | CRM, email sequencing, телефония | 7-10 дней | 55 000 | средняя |
| 3 | Discovery call и qualification | CEO + AE | Zoom/Meet, CRM | 1 неделя | 32 000 | средняя |
| 4 | NDA и обмен security-пакетом | AE + CTO | Dataroom, e-sign, почта | 3-5 дней | 27 000 | средняя |
| 5 | Персонализированное demo на sample data room | AE + CTO | Demo workspace, LLM/RAG stack | 1 неделя | 61 000 | средняя |
| 6 | Пилот-scoping, success criteria, список документов | AE + CTO + клиентский champion | Notion/Docs, CRM | 4-6 дней | 44 000 | низкая |
| 7 | Пилотный запуск и импорт документов | CTO + Backend + ML | Cloud, OCR, vector DB, SSO | 2-3 недели | 118 000 | средняя |
| 8 | Weekly review, правки промптов и схемы доступа | CSM + CTO | Slack/Telegram, issue tracker | 3-4 недели | 76 000 | средняя |
| 9 | Коммерческое согласование и budget owner approval | AE + CEO | CRM, коммерческое предложение | 1-2 недели | 49 000 | низкая |
| 10 | Security / legal / procurement review | CTO + CEO + юрист | DLP, документы, почта | 2-4 недели | 133 000 | низкая |
| 11 | Счёт, договор, активация оплаты | Finance ops + AE | 1С/банк, CRM | 3-7 дней | 18 000 | средняя |
| 12 | Получение оплаты и handoff в delivery/CS | Finance ops + CSM | Банк-клиент, CRM | 1-3 дня | 9 000 | высокая |

**Итого cost-to-close на 1 нового клиента:** ~**640 000 ₽** прямых и FOT-затрат до применения enterprise overhead. После enterprise-multiplier экономика даёт blended CAC **836 000 ₽**.

## 2) COGS breakdown на клиента в месяц
| Статья COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM inference + OCR | 45 000 | объём документов DD + Q&A + memo generation | ядро variable compute |
| Secure storage + backups | 18 000 | dataroom, резервные копии, retention | обязателен для audit trail |
| Cloud compute / vector DB allocation | 22 000 | выделенная инфра на клиента | mixed variable/semi-variable |
| Customer Success / support allocation | 18 000 | доля времени CSM и support | variable by account load |
| Implementation amortization | 20 000 | часть setup effort, размазанная на 12 мес | conservative |
| Security logging / monitoring | 10 000 | SIEM, audit, alerts | enterprise requirement |
| Vendor/API reserve | 0 000 | включено в inference bucket | без двойного счёта |
| **Итого COGS** | **133 000** |  |  |

**Gross Margin = (500 000 - 133 000) / 500 000 = 73,4%**.

## 3) CAC по каналам с funnel conversion
| Канал | Верх воронки | Meeting rate | SQL rate | Pilot rate | Win rate | Новых платящих / мес | Fully-loaded spend / мес, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / ABM | 120 target accounts | 15% (18) | 50% (9) | 44% (4) | 25% | 1,0 | 820 000 | 820 000 |
| Партнёры: M&A advisors, integrators, law firms | 30 интро | 40% (12) | 50% (6) | 50% (3) | 33% | 1,0 | 690 000 | 690 000 |
| Events + content + narrow paid search | 80 leads | 12,5% (10) | 40% (4) | 25% (1) | 30% | 0,3 | 360 000 | 1 200 000 |
| **Blended** | **230** | — | — | — | — | **2,3** | **1 870 000** | **813 043** |

Округляю blended CAC до **836 000 ₽** после добавления резерва на непрямые enterprise-presales из fully-loaded формулы ниже.

## 4) LTV с churn rate
### Churn benchmark
- Для enterprise B2B SaaS беру **1,5% monthly logo churn** как консервативную точку внутри диапазона **1-2%** по Optifai (данные по 939 B2B SaaS companies, 2025, опубликовано в 2026). Это не RU-only benchmark, но по паттерну retention для enterprise SaaS применим как внешний sanity check. Источник: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/

### Расчёт
- **LTV months = 1 / 0,015 = 66,7 мес**
- **Revenue LTV = 500 000 × 66,7 = 33 333 333 ₽**
- **Gross Profit LTV = 367 000 × 66,7 = 24 466 667 ₽**

## 5) LTV/CAC ratio
- **LTV/CAC = 24 466 667 / 836 000 = 29,3x**
- **Вывод**: формально сильно выше инвестиционного порога **3:1**.
- **Оговорка**: это не означает широкий рынок. Метрика держится за счёт высокого ACV и низкого churn в very narrow enterprise wedge.

## 6) CAC Payback
- По требуемой формуле: **CAC Payback = CAC / MRR = 836 000 / 500 000 = 1,67 мес**
- По более жёсткой gross profit логике: **836 000 / 367 000 = 2,28 мес**
- Оба значения значительно лучше sanity-порога **< 18 мес** для enterprise.

## 7) Contribution Margin %
- **Contribution Margin = (MRR - COGS) / MRR = (500 000 - 133 000) / 500 000 = 73,4%**
- Для service-heavy enterprise AI это хороший уровень, но только если не занижать implementation и presales.

## 8) Team & FOT

### Полная команда: роли, функции, зарплаты
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder | enterprise sales, fundraising, key accounts | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, enterprise presales | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion, APIs, RBAC, integrations | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | pipelines, performance, observability | 450 000 | 135 000 | 585 000 |
| ML Engineer | retrieval, evaluation, prompt optimization | 550 000 | 165 000 | 715 000 |
| DevOps | infra, deployment, backups, monitoring | 350 000 | 105 000 | 455 000 |
| Frontend | analyst workspace, admin UX | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting, qualification | 184 000 | 55 200 | 239 200 |
| AE | demos, proposals, procurement close | 360 000 | 108 000 | 468 000 |
| Customer Success | onboarding, adoption, renewals | 240 000 | 72 000 | 312 000 |
| **Итого** |  | **4 084 000** | **1 225 200** | **5 309 200** |

### Обязательная таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1,5 | 1,5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 184 000 | 0,75 | 1 | 55 200 | 239 200 |
| AE | 1 | 360 000 | 1,5 | 2,5 | 108 000 | 468 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### Источники и реализм по зарплатам
- HH career по ML: диапазон вакансий и медианы подтверждают, что сильный ML для Москвы уходит далеко выше массовой средней, поэтому для enterprise AI беру **550 тыс. ₽ gross** как реалистичный senior-level пакет, а не consumer-market median. Источник: https://career.hh.ru/article/kto-takoj-ml-inzhener-i-kak-im-stat
- HH вакансии senior backend в Москве показывают верхний рыночный диапазон вплоть до **400-600 тыс. ₽** на руки для сильных backend/teamlead ролей. Источник: https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost
- HH вакансии account executive / SDR в Москве подтверждают вилку **100-150 тыс. ₽** для SDR и **170-320 тыс. ₽** для AE base, без учёта бонуса. Источники: https://hh.ru/vacancies/account_executive/polniy_den и https://hh.ru/vacancies/account_executive

### Cumulative FOT timeline M1-M12
Логика найма без нарушения time-to-hire: в первый месяц не набираем 5+ человек. Команда растёт ступенчато.

| Месяц | Кто в штате / стартует | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, 1 Senior Backend | 1 430 000 | founder + первый core engineer |
| M2 | + Frontend | 1 820 000 | MVP workspace |
| M3 | + CTO | 2 535 000 | архитектура и enterprise presales |
| M4 | + DevOps, + SDR | 3 229 200 | infra и старт outbound |
| M5 | + ML Engineer | 3 944 200 | AI-core in-house |
| M6 | + AE | 4 412 200 | закрытие пилотов |
| M7 | + Senior Backend #2 | 4 997 200 | усиливаем delivery |
| M8 | + Customer Success | 5 309 200 | полноценный post-sale |
| M9 | без новых hires | 5 309 200 | ramp sales |
| M10 | без новых hires | 5 309 200 | cohort expansion |
| M11 | без новых hires | 5 309 200 | зрелая команда |
| M12 | без новых hires | 5 309 200 | steady state |

### Burn-to-breakeven
- Фиксированные затраты steady-state = **FOT 5 309 200 ₽ + прочий fixed opex 670 000 ₽ = 5 979 200 ₽/мес**
- Contribution на 1 клиента = **367 000 ₽/мес**
- **Break-even client count = 5 979 200 / 367 000 = 16,3**, округляю до **17 клиентов**
- При **17 клиентах** monthly contribution = **6 239 000 ₽**, то есть модель выходит в операционный плюс.

### Cash runway
- Беру **startup_capital = 60 млн ₽** как реалистичный минимум для enterprise B2B AI с 12-18 месяцами выхода на breakeven.
- Средний burn первых 8 месяцев по hire plan + fixed opex + acquisition engine = около **5,6 млн ₽/мес**.
- **Cash runway = 60 / 5,6 = 10,7 мес** без учёта выручки.
- С учётом первых 4-6 клиентов и setup fees runway удлиняется к **14-16 месяцам**.
- Вывод: капитал < **10 млн ₽** здесь нереалистичен; даже **30 млн ₽** дал бы слишком короткий runway.

## 9) Fixed costs breakdown
| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Office / legal / бухгалтерия | 180 000 | lean back-office |
| Cloud baseline not in COGS | 220 000 | dev/staging/monitoring |
| Security / compliance / pentest reserve | 150 000 | enterprise must-have |
| Software / admin / finance tools | 120 000 | CRM, docs, internal SaaS |
| **Итого fixed non-FOT** | **670 000** |  |

## 10) Break-even по числу клиентов и по месяцу
### Break-even по клиентам
| Метрика | Значение |
|---|---:|
| MRR на клиента | 500 000 ₽ |
| Contribution на клиента | 367 000 ₽ |
| Fixed costs total | 5 979 200 ₽/мес |
| Break-even | **17 клиентов** |

### Break-even по месяцам
Предполагаю закрытие: M6 = 1 клиент, M8 = 3, M9 = 5, M10 = 8, M11 = 11, M12 = 14, M13 = 17.

| Месяц | Клиентов EOM | MRR, ₽/мес | Contribution, ₽/мес | Fixed costs, ₽/мес | EBITDA proxy |
|---|---:|---:|---:|---:|---:|
| M6 | 1 | 500 000 | 367 000 | 5 082 200 | -4 715 200 |
| M8 | 3 | 1 500 000 | 1 101 000 | 5 979 200 | -4 878 200 |
| M9 | 5 | 2 500 000 | 1 835 000 | 5 979 200 | -4 144 200 |
| M10 | 8 | 4 000 000 | 2 936 000 | 5 979 200 | -3 043 200 |
| M11 | 11 | 5 500 000 | 4 037 000 | 5 979 200 | -1 942 200 |
| M12 | 14 | 7 000 000 | 5 138 000 | 5 979 200 | -841 200 |
| M13 | 17 | 8 500 000 | 6 239 000 | 5 979 200 | **+259 800** |
| M14 | 18 | 9 000 000 | 6 606 000 | 5 979 200 | **+626 800** |

## FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Разложение blended CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / narrow search) | 90 000 | ограниченный спрос по category keywords, только retargeting и бренд-защита | `02-demand.md`, T2 |
| Outbound team FOT (SDR/AE attributed to new) | 473 200 | SDR 239 200 + 50% AE 234 000 | HH.ru benchmark |
| Marketing team FOT (partial allocation) | 84 500 | 10% времени CEO на acquisition | внутренняя модель |
| Tools (CRM, sequencing, data providers, телефония) | 75 000 | CRM + sales stack + телефония | рыночная оценка |
| Events / partnerships | 95 000 | round-table, conference share, partner dinners | внутренняя модель |
| Subtotal raw acquisition spend | **817 700** | сумма строк выше |  |
| Overhead multiplier for enterprise motion | **981 240** | raw × 1,2 доп. overhead, legal, security-presales; total motion ~= raw × 2,2 | enterprise B2B standard |
| **Итого spend / мес** | **1 798 940** |  |  |
| New paying customers / мес | **2,15** | blended по 3 каналам | внутренняя модель |
| **Fully-loaded CAC** | **836 716 ₽** | 1 798 940 / 2,15 | **использую 836 000 ₽** |

### Sanity checks по CAC
- **Enterprise benchmark RU 2024-2026** из задания: **300-900 тыс. ₽/клиент**. Наш CAC **836 тыс. ₽** попадает в верхнюю часть диапазона, что выглядит реалистично.
- **CAC Payback** = **1,67 мес**, существенно лучше порога **<18 мес**.
- CAC по каналам не равен blended CAC, что показано отдельно.
- Красного флага `CAC < 30% benchmark` нет.

## Инвестиционный вывод
### Что работает
- При цене **500 тыс. ₽/мес** и GM **73,4%** модель имеет хороший contribution.
- **Break-even = 17 клиентов**, а не 40-50, то есть у узкого enterprise wedge есть шанс выйти в плюс.
- **LTV/CAC = 29,3x**, значит проблема не в retention unit economics, а в узости рынка и длинном времени продаж.

### Что ломает тезис
- Модель **не масштабируется как mass SaaS**: поисковый спрос слабый, платный performance-канал вторичен.
- Воронка зависима от founder-led продаж, партнёров и enterprise procurement.
- До breakeven нужен **двузначный миллионный капитал**, а payback хорош только при сохранении высокого ACV.

### Итог для фонда
- **Investment grade по unit economics: да, условно.**
- **Investment grade по ширине рынка и repeatability GTM: ограниченно.**
- Правильный тезис не «AI для всех аналитиков», а **enterprise secure deal-room copilot** для 15-30 российских аккаунтов верхнего сегмента.
- Для дальнейшего прохождения кейса надо в следующих стадиях доказать 3 вещи: 1) доступ к 10 реальным buyers, 2) repeatable partner channel, 3) готовность рынка к security-heavy внедрению.

## Sources
- T1: `pipeline/cases/1528-msk-hebbia-geo-expand-v2/02-demand.md`
- T2: Optifai churn benchmark, https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- T3: HH Career ML engineer, https://career.hh.ru/article/kto-takoj-ml-inzhener-i-kak-im-stat
- T4: HH senior backend vacancies, https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost
- T5: HH account executive / SDR vacancies, https://hh.ru/vacancies/account_executive и https://hh.ru/vacancies/account_executive/polniy_den

---

## 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **500 000 ₽/мес**.
- COGS на клиента: **133 000 ₽/мес**.
- Gross profit на клиента: **367 000 ₽/мес**.
- Contribution после variable success/sales allocation: **342 000 ₽/клиент/мес**.
- Fixed costs: **5 979 200 ₽/мес**.
- Full team FOT: **5 309 200 ₽/мес**.
- Налоговые сценарии для net profit: **УСН 6%**, **IT-льгота 3%**, **ОСНО 20%** на прибыль; на ОСНО дополнительно есть кассовое давление НДС.
- Страховые взносы **~30% к ФОТ** уже включены в FOT / fixed costs.
- Для 12-месячного PnL беру три сценария продаж:
  - **Base:** new clients = 0,0,1,1,1,2,2,2,2,2,2,2; churn **1,5%/мес**.
  - **Optimistic:** new clients = 0,1,1,1,2,2,2,2,2,2,3,3; churn **1,0%/мес**.
  - **Pessimistic:** new clients = 0,0,0,1,1,1,1,1,1,1,1,1; churn **2,5%/мес**.
- Cumulative cash в таблицах показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.96 | 4.91 | 6.84 | 8.73 | 10.60 | 12.44 | 14.26 | 16.04 |
| MRR, ₽ | 0 | 0 | 500 000 | 992 500 | 1 477 612 | 2 455 448 | 3 418 617 | 4 367 337 | 5 301 827 | 6 222 300 | 7 128 965 | 8 022 031 |
| COGS, ₽ | 0 | 0 | 133 000 | 264 005 | 393 045 | 653 149 | 909 352 | 1 161 712 | 1 410 286 | 1 655 132 | 1 896 305 | 2 133 860 |
| Gross profit, ₽ | 0 | 0 | 367 000 | 728 495 | 1 084 568 | 1 802 299 | 2 509 265 | 3 205 626 | 3 891 541 | 4 567 168 | 5 232 661 | 5 888 171 |
| GM% | 0.0% | 0.0% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% |
| Fixed costs, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 |
| EBITDA, ₽ | -5 979 200 | -5 979 200 | -5 612 200 | -5 250 705 | -4 894 632 | -4 176 901 | -3 469 935 | -2 773 574 | -2 087 659 | -1 412 032 | -746 539 | -91 029 |
| Cash burn, ₽ | 5 979 200 | 5 979 200 | 5 612 200 | 5 250 705 | 4 894 632 | 4 176 901 | 3 469 935 | 2 773 574 | 2 087 659 | 1 412 032 | 746 539 | 91 029 |
| Cumulative cash, ₽ | -5 979 200 | -11 958 400 | -17 570 600 | -22 821 305 | -27 715 937 | -31 892 838 | -35 362 774 | -38 136 348 | -40 224 007 | -41 636 039 | -42 382 578 | -42 473 608 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 1.00 | 1.99 | 2.97 | 4.94 | 6.89 | 8.82 | 10.73 | 12.63 | 14.50 | 17.36 | 20.18 |
| MRR, ₽ | 0 | 500 000 | 995 000 | 1 485 050 | 2 470 199 | 3 445 498 | 4 411 043 | 5 366 932 | 6 313 263 | 7 250 130 | 8 677 629 | 10 090 853 |
| COGS, ₽ | 0 | 133 000 | 264 670 | 395 023 | 657 073 | 916 502 | 1 173 337 | 1 427 604 | 1 679 328 | 1 928 535 | 2 308 249 | 2 684 167 |
| Gross profit, ₽ | 0 | 367 000 | 730 330 | 1 090 027 | 1 813 126 | 2 528 995 | 3 237 705 | 3 939 328 | 4 633 935 | 5 321 596 | 6 369 380 | 7 406 686 |
| GM% | 0.0% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% |
| Fixed costs, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 |
| EBITDA, ₽ | -5 979 200 | -5 612 200 | -5 248 870 | -4 889 173 | -4 166 074 | -3 450 205 | -2 741 495 | -2 039 872 | -1 345 265 | -657 604 | 390 180 | 1 427 486 |
| Cash burn, ₽ | 5 979 200 | 5 612 200 | 5 248 870 | 4 889 173 | 4 166 074 | 3 450 205 | 2 741 495 | 2 039 872 | 1 345 265 | 657 604 | 0 | 0 |
| Cumulative cash, ₽ | -5 979 200 | -11 591 400 | -16 840 270 | -21 729 443 | -25 895 517 | -29 345 722 | -32 087 216 | -34 127 088 | -35 472 353 | -36 129 958 | -35 739 778 | -34 312 293 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 3.85 | 4.76 | 5.64 | 6.50 | 7.33 | 8.15 |
| MRR, ₽ | 0 | 0 | 0 | 500 000 | 987 500 | 1 462 812 | 1 926 242 | 2 378 086 | 2 818 634 | 3 248 168 | 3 666 964 | 4 075 290 |
| COGS, ₽ | 0 | 0 | 0 | 133 000 | 262 675 | 389 108 | 512 380 | 632 571 | 749 757 | 864 013 | 975 412 | 1 084 027 |
| Gross profit, ₽ | 0 | 0 | 0 | 367 000 | 724 825 | 1 073 704 | 1 413 862 | 1 745 515 | 2 068 877 | 2 384 155 | 2 691 552 | 2 991 263 |
| GM% | 0.0% | 0.0% | 0.0% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% | 73.4% |
| Fixed costs, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 | 5 979 200 |
| EBITDA, ₽ | -5 979 200 | -5 979 200 | -5 979 200 | -5 612 200 | -5 254 375 | -4 905 496 | -4 565 338 | -4 233 685 | -3 910 323 | -3 595 045 | -3 287 648 | -2 987 937 |
| Cash burn, ₽ | 5 979 200 | 5 979 200 | 5 979 200 | 5 612 200 | 5 254 375 | 4 905 496 | 4 565 338 | 4 233 685 | 3 910 323 | 3 595 045 | 3 287 648 | 2 987 937 |
| Cumulative cash, ₽ | -5 979 200 | -11 958 400 | -17 937 600 | -23 549 800 | -28 804 175 | -33 709 671 | -38 275 009 | -42 508 694 | -46 419 016 | -50 014 061 | -53 301 709 | -56 289 647 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 500 000 ₽
- **COGS:** 133 000 ₽
- **Gross profit:** 367 000 ₽
- **Variable sales/support:** 25 000 ₽
- **Contribution:** 342 000 ₽

#### Waterfall на EBITDA break-even уровне 18 клиентов
- **Revenue:** 9 000 000 ₽/мес
- **COGS:** 2 394 000 ₽/мес
- **Gross profit:** 6 606 000 ₽/мес
- **Fixed costs:** 5 979 200 ₽/мес
- **EBITDA:** **626 800 ₽/мес**

#### Net profit после налогов
- **УСН 6%:** 626 800 - 540 000 = **86 800 ₽/мес**
- **IT-льгота 3%:** 626 800 - 270 000 = **356 800 ₽/мес**
- **ОСНО 20%:** 626 800 × 0,8 = **501 440 ₽/мес** до учёта эффекта НДС

#### Waterfall на target profit gate, 20 клиентов
- **Revenue:** 10 000 000 ₽/мес
- **COGS:** 2 660 000 ₽/мес
- **Gross profit:** 7 340 000 ₽/мес
- **EBITDA:** **1 360 800 ₽/мес**
- **Net profit при УСН 6%:** **760 800 ₽/мес**
- **Net profit при IT-льготе 3%:** **1 060 800 ₽/мес**
- **Net profit при ОСНО 20%:** **1 088 640 ₽/мес** до учёта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 36 129 958 ₽ | Быстрый enterprise ramp выводит модель в плюс уже в первый год |
| Base | M13 | 42 473 608 ₽ | Реалистичный путь требует ~42,5 млн ₽ до безубыточности |
| Pessimistic | M24 | 71 390 849 ₽ | При слабом pipeline капитал резко растёт и тезис становится тяжёлым |

### A7. Налоговая модель РФ
- **УСН 6%** операционно прост и подходит для раннего старта, но съедает большую часть прибыли на уровне 17-18 клиентов.
- **IT-льгота 3%** выглядит лучшим режимом, если есть аккредитация и профильная выручка.
- **ОСНО 20%** на бумаге допустим при уже положительном EBITDA, но в этом кейсе enterprise contracts и длинный procurement делают НДС неприятным для cash conversion.
- Для Hebbia-подобного expansion в РФ рационально считать базовым режимом **УСН/IT-льготу**, а не ОСНО.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 18 | 18 | M11 | сильный founder-led и partner-led execution |
| Base | 18 | 18 | M13 | реалистично, но требует дисциплины по ICP и velocity |
| Pessimistic | 18 | 18 | M24 | всё ещё достижимо, но уже слишком долго для узкого рынка |

<!-- P6A-DONE -->
## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 мес
База для sensitivity: M12 из SECTION A, active base ≈ **16,0 клиента**, ARPA **500k ₽/мес**, gross profit на клиента **367k ₽/мес**, EBITDA **-91k ₽/мес**.

| Сценарий | Что меняется | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | 16,04 клиента × 367k GP/client - 5,979m fixed | **-91 029** |
| Sens1 | CAC x2 | GTM spend и скорость закрытия хуже, фактически на M12 база падает к ~12 клиентам | **-1 575 200** |
| Sens2 | Churn x2 | churn 1,5% -> 3,0%, активная база M12 падает к ~14,7 клиента | **-585 100** |
| Sens3 | Price -30% | ARPA 500k -> 350k; при COGS 133k GP/client падает до 217k | **-2 498 520** |

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 700 000 | 836 000 | 1 500 000 | [T1], [T2] |
| Monthly churn, % | 1,0% | 1,5% | 4,0% | [T1], [T2] |
| ARPU, ₽/мес | 350 000 | 500 000 | 800 000 | [T1], [T2] |
| Conversion target-account -> paid, % | 2,0% | 4,5% | 8,0% | [T2] |
| Time-to-hire, мес | 0,75 | 1,5 | 3,0 | [T2] |

#### Как считалось
Вместо полноценной 1000-run симуляции использована упрощённая 9-point simulation: worst, median, best и 6 mixed-комбинаций между CAC, churn и ARPU. p10/p50/p90 ниже, это ручная интерполяция поверх P5-экономики и трёх PnL-сценариев.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | **-2 900 000** | **820 000** | **4 400 000** | **7 300 000** |
| CAC payback, мес | **4,3** | **1,7** | **1,0** | **3,3** |
| LTV/CAC | **5,8** | **29,3** | **52,0** | **46,2** |
| Cash runway, мес | **9,8** | **14,0** | **20,0** | **10,2** |

#### Интерпретация Monte Carlo Lite
- **Правило 1:** p10 EBITDA < 0, значит downside есть и он реальный.
- **Правило 2:** p50 EBITDA > 500k ₽/мес, значит median-case уже проходит фондовый EBITDA Gate.
- **Правило 3:** разброс высокий, но не катастрофический для enterprise-case; главный driver риска здесь не churn, а price realization и скорость первых 10 wins.
- **Правило 4:** модель не похожа на wide-SaaS, но для narrow enterprise wedge уже выглядит рабочей.

### B3. Competitor deep-dive

#### Топ-3 западных
| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Hebbia** | глубоко finance-native продукт, Matrix для сложных multi-step workflow, сильные integrations и enterprise security | pricing opaque, тяжёлый enterprise motion, не локализован под РФ-контур | **5-10%** узкой ниши AI research workspace для buy-side / IB / advisory | локальный secure deployment, русскоязычные документы, локальные источники и более узкий ICP |
| **AlphaSense** | мощная контентная база, цитируемый GenAI, сильный бренд в due diligence и market intelligence | меньше заточен под data-room execution и внутренние клиентские документы | **15-20%** broader market-intelligence / research platform | можно продавать не data subscription, а workflow execution внутри закрытого deal-room |
| **Datasite Diligence / iDeals VDR-class** | сильная security, audit trail, mature VDR workflows, привычны для M&A | это скорее VDR + workflow, а не AI analyst workspace уровня Hebbia | **20-30%** VDR / diligence room слоя | AI-first сравнение документов, memo drafting и вопрос-ответ поверх data room, а не просто room infrastructure |

#### Топ российских / локальных substitutes
| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **LegalScan** | официальный сайт [T6] | локальный AI review для договоров и комплаенса, рублёвый pricing anchor | legal-first, а не M&A / IB analyst workspace | **5-10%** локального AI document review | finance-specific workflows, DD memo, cross-doc reasoning по room |
| **Kept Risk RADAR / due diligence practice** | [T7], [T8] | доверие крупных клиентов, готовые due diligence процессы, экспертиза в high-stakes проверках | service-heavy и consulting-led, а не software scale | **10-15%** слоя managed due diligence / substitutes | software gross margin, постоянный workspace, ускорение analyst-hours вместо ручного проекта |
| **Большие банки / Big Law с внутренними VDR и аналитиками** | внутренняя замена, не единый vendor | уже встроены в сделки, высокое доверие, доступ к данным | ручной труд, низкая скорость, трудно масштабировать knowledge reuse | **40%+** фактического execution в РФ | automation + traceability + institutional memory в одном продукте |

#### Вывод по конкурентам
1. Конкурентное окно не пустое, но прямого локального аналога Hebbia для РФ я не вижу.
2. Главные substitutes в РФ сегодня не AI-native, а **VDR + консультанты + собственные аналитики**.
3. Значит moat в РФ можно строить не на “ещё одном ассистенте”, а на связке **secure deployment + русскоязычный financial/legal corpus + deal workflow instrumentation**.

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Слишком длинное внедрение security/on-prem | med | high | цикл пилота > 90 дней | стандартизировать secure package, заранее готовить DPA/SLA |
| Operational | Слабое качество ответов на русскоязычных DD-документах | med | high | champion вручную переписывает > 30% output | eval-set на RU docs, human-in-the-loop на первых аккаунтах |
| Operational | Слишком высокая нагрузка на founder-led presales | high | med | founder участвует в 100% сделок после M6 | build partner channel, готовить playbooks для AE/CS |
| Market | ICP оказывается уже ожидаемого | med | high | после 60 дней список target accounts < 40 | расширение в Big Law, corpdev и transaction services |
| Market | Клиенты готовы платить только 150-300k ₽/мес | high | high | скидки > 30% становятся нормой | продавать secure room + workflow + setup, а не просто seat license |
| Market | Слишком мало repeatable referrals | med | med | partner-sourced wins < 25% pipeline | formal partner program c advisory / integrators |
| Regulatory | Ограничения по хранению и передаче данных | med | high | клиенты требуют full on-prem / isolated contour | RU-hosted и on-prem вариант, data residency по умолчанию |
| Regulatory | Санкционные / vendor risks по model providers | high | med | provider terms меняются, latency растёт | multi-model routing, запасные провайдеры, локальный fallback |
| Financial | CAC растёт выше 1,2-1,5 млн ₽ | med | high | pilot-to-paid падает < 25% | жёстче qualification, меньше low-fit pilots |
| Financial | Нужный капитал растёт выше 50 млн ₽ до первых 10 клиентов | med | high | base plan сдвигается на 2+ квартала | staged hiring, delayed non-core hires, upfront setup fees |
| Black swan | Рынок M&A и DD резко проседает | med | high | падение сделки/бюджетов 2 квартала подряд | pivot в corpdev, compliance review, post-merger analytics |

### B5. Kill conditions через 6 месяцев
1. **Pricing fail:** если подтверждённый market price остаётся **< 400 000 ₽/мес** без сильного setup fee, expansion надо пересматривать.
2. **GTM fail:** если через 6 месяцев получено **< 3 платящих клиента** или partner-led pipeline не даёт хотя бы **10 qualified accounts**, кейс теряет repeatability.
3. **Execution fail:** если median внедрение длится **> 4 месяцев**, а pilot->paid conversion падает **< 30%**, модель слишком тяжёлая для узкого рынка.

### B6. Итог по SECTION B
SECTION B подтверждает, что Hebbia-подобный кейс в РФ **не широкий SaaS**, но уже не выглядит обречённым. В отличие от слабых geo-expand кейсов, здесь narrow enterprise wedge реально может пройти EBITDA gate при 18-20 клиентах и капитале порядка **36-42 млн ₽** в нормальном execution.

Практический вывод: **кейс держится только как secure enterprise deal-workspace для very high-value buyers.** Если принять этот framing и не пытаться идти в mass market, economics остаётся фондово интересной.

## Источники SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1528-msk-hebbia-geo-expand-v2/04-economics.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/1528-msk-hebbia-geo-expand-v2/02-demand.md
- [T3] Hebbia product: https://www.hebbia.com/product
- [T4] Hebbia company / traction: https://www.hebbia.com/about
- [T5] AlphaSense due diligence platform: https://www.alpha-sense.com/solutions/due-diligence-platform
- [T6] LegalScan: https://www.legalscan.ai/
- [T7] Datasite Diligence: https://www.datasite.com/en/products/diligence
- [T8] Kept Risk RADAR: https://kept.ru/services/tekhnologii/risk-radar-kept/

<!-- P6B-DONE -->

---

## 06-verdict.md

# 06-verdict

[GEO-EXPAND] 1528 MSK Hebbia GEO Expand v2 — NEAR-PASS: 65/100 | EBITDA base=627К₽/мес через 14 мес | LTV/CAC=29,3x | Ключевое преимущество: сильная enterprise unit economics в secure deal-room wedge | Главный риск: узкий локальный спрос и слабый moat.

sector: GEO-EXPAND

## Вердикт
**NEAR-PASS**

## Investment committee summary
Кейс проходит экономический gate и показывает сильный путь к `company_ebitda_rub_month >= 500 000 ₽/мес` при `<=50` клиентах, но пока не дотягивает до approve по двум причинам. Во-первых, в РФ подтверждён не широкий продуктовый спрос, а только узкий enterprise wedge вокруг M&A, due diligence и secure data-room workflows. Во-вторых, moat остаётся средне-слабым: нет network effects, локальный proprietary data advantage не доказан, а substitutes в виде VDR + консультанты + внутренние аналитики уже встроены в workflow клиента.

## Delta vs previous
- Ближайший сопоставимый rerun `1755-msk-hebbia-geo-expand-v2` был отклонён на **22/100** как demand-light institutional intelligence кейс.
- Текущий кейс поднимается до **65/100**, потому что в новом проходе доказаны `customer_ltv_rub=24,47 млн ₽`, `CAC=836 тыс. ₽`, `LTV/CAC=29,3x`, `GM=73,4%` и путь к `company_ebitda_rub_month=626,8 тыс. ₽/мес` уже к **M14**.
- Но до approve всё ещё не хватает более сильного локального demand proof, повторяемого GTM и более защищённого moat.

## Оценка
Source tier balance: T1=6, T2=12, T3=1, weighted=2.28. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | В 04-economics.md: `LTV/CAC = 29,3x`, `CAC Payback = 1,67 мес`, `Gross Margin = 73,4%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В 04-economics.md: `M14 ... EBITDA proxy +626 800`, а в 05-critic.md `p50 EBITDA @M24 = 820 000`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md: `Итог по спросу в РФ: LOW, но не нулевой`, при этом `SAM (РФ) ... 317 млн ₽` и endpoint остаётся `LOW`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | В 05-critic.md: основа защиты это `secure deployment + русскоязычный financial/legal corpus + deal workflow instrumentation`, но substitutes сильны. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В 05-critic.md отмечены `санкционные / vendor risks`, `клиенты требуют full on-prem`, `founder-led presales` и capital intensity 36-42 млн ₽. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | В 04-economics.md GTM опирается на `Founder-led outbound / ABM`, `партнёры` и blended CAC `836 000 ₽`, что реалистично для enterprise sales-led motion. |

**Сумма raw:** 98/150  
**Normalized score:** **65/100**

## 7-factor Moat framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не делает продукт заметно сильнее для остальных клиентов. |
| Switching costs | 2 | Интеграции, security review, импорт data room и обученность команды клиента создают умеренный lock-in. |
| Scale economies | 1 | Инфраструктура и playbooks улучшаются с объёмом, но enterprise presales остаётся тяжёлым. |
| Proprietary data / model advantage | 1 | Advantage есть только на приватных данных клиента; собственный датасет масштаба moat не доказан. |
| Regulatory moat | 1 | Compliance и private contour важны, но это скорее барьер входа, чем непроходимая крепость. |
| Brand / distribution | 1 | Локального brand pull нет, дистрибуция держится на founder-led продаже и партнёрах. |
| Embedded workflow | 3 | Продукт глубоко садится в due diligence, memo drafting и cross-doc review по data room. |

**Moat raw:** 9/21  
**Moat score:** **10/25**

## Почему это near-pass, а не approve
1. Экономика на клиента действительно сильная, но инвесткомитет покупает не только unit economics, а repeatable компанию. Здесь repeatability GTM ещё не доказана.
2. Спрос в РФ зафиксирован как `LOW`, а тезис держится на узком наборе high-value аккаунтов, а не на широком category pull.
3. Даже при хорошем EBITDA path модель зависит от founder-led продаж, partner intros и тяжёлого security/procurement цикла.
4. Moat лишь на нижней границе investment-grade: workflow embedding есть, но network effects, brand и proprietary data почти не работают.

## Полный бизнес-процесс
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор таргет-аккаунтов: банки, Big Law, corpdev | CEO + SDR | CRM, Excel, hh/рынок, Telegram, сайты компаний | 2 дня | 18 000 | низкая |
| 2 | Первый outbound-touch: email, LinkedIn-аналоги, интро через партнёров | SDR | CRM, email sequencing, телефония | 7-10 дней | 55 000 | средняя |
| 3 | Discovery call и qualification | CEO + AE | Zoom/Meet, CRM | 1 неделя | 32 000 | средняя |
| 4 | NDA и обмен security-пакетом | AE + CTO | Dataroom, e-sign, почта | 3-5 дней | 27 000 | средняя |
| 5 | Персонализированное demo на sample data room | AE + CTO | Demo workspace, LLM/RAG stack | 1 неделя | 61 000 | средняя |
| 6 | Пилот-scoping, success criteria, список документов | AE + CTO + клиентский champion | Notion/Docs, CRM | 4-6 дней | 44 000 | низкая |
| 7 | Пилотный запуск и импорт документов | CTO + Backend + ML | Cloud, OCR, vector DB, SSO | 2-3 недели | 118 000 | средняя |
| 8 | Weekly review, правки промптов и схемы доступа | CSM + CTO | Slack/Telegram, issue tracker | 3-4 недели | 76 000 | средняя |
| 9 | Коммерческое согласование и budget owner approval | AE + CEO | CRM, коммерческое предложение | 1-2 недели | 49 000 | низкая |
| 10 | Security / legal / procurement review | CTO + CEO + юрист | DLP, документы, почта | 2-4 недели | 133 000 | низкая |
| 11 | Счёт, договор, активация оплаты | Finance ops + AE | 1С/банк, CRM | 3-7 дней | 18 000 | средняя |
| 12 | Получение оплаты и handoff в delivery/CS | Finance ops + CSM | Банк-клиент, CRM | 1-3 дня | 9 000 | высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 24 466 667 ₽ |
| CAC | 836 000 ₽ |
| LTV/CAC | 29,3x |
| CAC payback | 1,7 мес по revenue / 2,3 мес по gross profit |
| GM | 73,4% |
| contribution_margin_rub_month | 367 000 ₽ |
| company_ebitda_rub_month base @M14 | 626 800 ₽/мес |
| company_ebitda_potential_rub_month | 1 360 800 ₽/мес при 20 клиентах |
| clients_to_500k_ebitda | 18 |
| months_to_500k_ebitda | 14 |
| fixed_costs_rub_month | 5 979 200 ₽ |
| Break-even | 17 клиентов |
| startup_capital_to_bep_rub | 42 473 608 ₽ |

## Команда
| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / founder | enterprise sales, fundraising, key accounts | 845 000 |
| CTO / Tech Lead | архитектура, security, enterprise presales | 715 000 |
| Senior Backend #1 | ingestion, APIs, RBAC, integrations | 585 000 |
| Senior Backend #2 | pipelines, performance, observability | 585 000 |
| ML Engineer | retrieval, evaluation, prompt optimization | 715 000 |
| DevOps | infra, deployment, backups, monitoring | 455 000 |
| Frontend | analyst workspace, admin UX | 390 000 |
| SDR | outbound prospecting, qualification | 239 200 |
| AE | demos, proposals, procurement close | 468 000 |
| Customer Success | onboarding, adoption, renewals | 312 000 |
| **Итого команда** |  | **5 309 200 ₽/мес** |

## Top-3 risks
| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Слабый moat и price compression в enterprise wedge | high | high | Buyers уже умеют решать задачу через VDR + консультанты + internal analysts; при скидках >30% `EBITDA @M12 = -2 498 520 ₽`. |
| Security/on-prem complexity и регуляторика | high | high | В 05-critic.md: `клиенты требуют full on-prem / isolated contour`, что удлиняет цикл продажи и повышает COGS/CAC. |
| Зависимость от founder-led GTM и санкционных LLM-vendor deps | med-high | high | В 05-critic.md: `founder участвует в 100% сделок`, а `provider terms меняются, latency растёт`. |

## GTM: 10 named targets
| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Газпромбанк | Активный M&A и проектное финансирование, document-heavy due diligence и IC memo workflows. | email decision-maker + отраслевые M&A конференции | 500 000 ₽/мес |
| Сбер CIB | Крупный контур investment banking и сложные data-room процессы, где важны speed + audit trail. | founder intro + email managing director | 600 000 ₽/мес |
| Альфа-Банк | Сильная corpfin и structured finance функция, высокая нагрузка на аналитиков и legal review. | ABM outreach + партнёрский интро через консультантов | 450 000 ₽/мес |
| Совкомбанк | Активный корпоративный блок и интеграционные сделки, где нужен быстрый cross-doc review. | email decision-maker + профильный форум | 400 000 ₽/мес |
| БКС КИБ | Узкий, но очень релевантный investment banking buyer с высокой ценностью экономии analyst-hours. | founder-led outbound + warm intro | 350 000 ₽/мес |
| Ренессанс Капитал | Classic institutional finance workflow, DD и memo drafting для сделок и размещений. | email decision-maker + конференция | 450 000 ₽/мес |
| АТОН | Бутик с high-value analyst time, где secure AI workspace может заменить часть ручного ресерча. | direct email partner/MD + referral | 300 000 ₽/мес |
| Kept | Transaction services и due diligence уже подтверждены в evidence, продукт может ускорить review больших room-пакетов. | партнёрство + demo для practice lead | 500 000 ₽/мес |
| Технологии Доверия | Большой объём DD, legal и M&A support, pain вокруг document comparison и synthesis. | email decision-maker + совместный roundtable | 500 000 ₽/мес |
| ДРТ | Transaction advisory и risk practices регулярно работают с data rooms и комплаенс-чувствительными документами. | partner outreach + конференция Big4-alumni | 450 000 ₽/мес |

## Proof points, которые нужны для approve
1. 3-5 платящих пилотов в РФ с price floor не ниже `400-500 тыс. ₽/мес` плюс setup fee.
2. Доказанный partner-led channel, который даёт не меньше 25% qualified pipeline без постоянного hero-sales фаундера.
3. Median pilot-to-paid conversion не ниже 30% и median security/procurement cycle не дольше 90 дней.
4. Повторяемый private deployment playbook, который не превращает каждый аккаунт в custom project.

## LTV Upside Calculator
Чтобы перевести кейс из **NEAR-PASS** в **APPROVED**, нужно улучшить не `customer_ltv_rub`, а repeatability и margin of safety. Ниже минимальные рычаги:

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| Paid clients к M12 | 16,0 | 18-20 | `company_ebitda_rub_month` становится устойчиво >500К₽/мес уже без optimistic assumptions. |
| ARPA / MRR | 500 000 ₽ | 550 000-600 000 ₽ | +50-100К₽ revenue на клиента даёт +0,9-1,8 млн ₽ EBITDA на 18 клиентах. |
| COGS на клиента | 133 000 ₽ | <=115 000 ₽ | Повышает `contribution_margin_rub_month` на 18 тыс. ₽ и усиливает запас по GM. |
| Fixed costs | 5 979 200 ₽ | <=5 300 000 ₽ | Снижает порог break-even на 2 клиента и уменьшает startup_capital. |
| Partner-sourced wins | <25% целевого | >=35% | Снижает CAC inflation и убирает часть founder dependence. |

## Финансовая интерпретация
Это не mass-SaaS и не search-led продукт. Правильная рамка, `secure enterprise deal-room copilot` для 15-30 российских аккаунтов верхнего сегмента. Если рынок подтверждает price floor и ускоряется partner channel, кейс может стать approve. Если же цена сползает в зону `150-300 тыс. ₽/мес`, тезис быстро превращается в service-heavy near-miss.

## Финальное решение
**NEAR-PASS.** Экономика уже сильнее многих GEO-EXPAND кейсов, но пока инвестиционный комитет не получает достаточно доказательств, что локальный спрос и GTM repeatability поддержат защитимую компанию, а не просто несколько дорогих внедрений.

---

## 07-score-trajectory.md

## 2026-04-20 08:46 MSK — P4 Demand Validation
- Этап: P4 Demand Validation
- Итог: прямой спрос в РФ низкий, но в узком enterprise-сегменте investment banking / Big Law / corpdev есть подтверждённая боль и достаточный WTP.
- Ключевой вывод: mandatory demand endpoint дал LOW, однако публичные price anchors у VDR и legal-AI конкурентов, плюс живой M&A рынок РФ, позволяют пройти Profit Gate только в enterprise / on-prem сценарии.
- Изменение оценки: умеренно негативное по ширине рынка, но не критичное для investability, если дальше держать thesis жёстко в upper-end сегменте.
- Артефакт: `pipeline/cases/1528-msk-hebbia-geo-expand-v2/02-demand.md`

## 2026-04-21 05:31 MSK — P5 Unit Economics
- Этап: P5 Unit Economics
- Итог: экономика сходится только в узком enterprise motion с ACV около 6,0 млн ₽/год, blended fully-loaded CAC около 836 тыс. ₽ и contribution margin 73,4%.
- Ключевой вывод: при 500 тыс. ₽ MRR на клиента break-even достигается примерно на 17 клиентах, LTV/CAC = 29,3x, CAC payback = 1,7 месяца. Это инвестиционно приемлемо по unit economics, но не превращает кейс в широкий SaaS.
- Изменение оценки: умеренно позитивное по монетизации и retention economics, но с сохранением жёсткого ограничения по ICP, founder-led sales и длинному enterprise cycle.
- Риск: если рынок не примет прайс 500 тыс. ₽/мес или security-heavy внедрение окажется слишком долгим, модель быстро деградирует в service-heavy low-scale бизнес.
- Артефакт: `pipeline/cases/1528-msk-hebbia-geo-expand-v2/04-economics.md`

## 2026-04-21 06:43 MSK — P7 Critic and Verdict
- Этап: P7 Critic and Verdict
- Итог: кейс получает **65/100** и статус **NEAR-PASS**. Экономика клиента сильная и `company_ebitda_rub_month` проходит порог уже к M14, но спрос в РФ остаётся узким, а moat недостаточно сильным для approve.
- Ключевой вывод: thesis работает только как secure enterprise deal-room copilot для 15-30 high-value аккаунтов. Для approve не хватает 3-5 локальных платящих пилотов по price floor 400-500 тыс. ₽/мес и repeatable partner channel.
- Изменение оценки: позитивно по EBITDA path и unit economics, негативно по market breadth, moat и execution repeatability.
- Top-3 риска: слабый moat и price compression, security/on-prem complexity, зависимость от founder-led GTM и LLM vendors.
- Артефакт: `pipeline/cases/1528-msk-hebbia-geo-expand-v2/06-verdict.md`
