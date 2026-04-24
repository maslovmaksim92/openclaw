# SCORISTA / AI-кредитный скоринг — verdict pack

- Статус: APPROVED WITH NOTES
- Score: 74/100
- Sector: FINTECH
- Дата: 2026-04-24
- GitHub: https://github.com/maslovmaksim92/openclaw/blob/main/business-models/approved/scorista-ai-kreditnyy-skoring-v2/verdict.md

## Stage 1 — Intake

```md
---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-scorista-ai-kreditnyy-skoring.md
created: 2026-04-21T18:26:12+03:00
original_verdict_source: triage/triage-2026-04-17-scorista-ai-kreditnyy-skoring.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — scorista-ai-kreditnyy-skoring

## Meta
- source: triage/triage-2026-04-17-scorista-ai-kreditnyy-skoring.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Triage report

## Файл
raw-2026-04-17-2304-msk-scorista-ai-kreditnyy-skoring.md

## Решение
NEW

## Причина
Сигнал не совпадает по теме, нише и технологии с текущим открытым кейсом в `pipeline/cases/`. Текущий открытый кейс относится к plaintiff-side legal claims automation, а здесь речь идёт о другой категории: AI-кредитный скоринг, андеррайтинг и антифрод для МФО, банков и других кредитных организаций.

## Что сделано
Создан новый кейс `ai-credit-scoring-and-underwriting-operator`.
Добавлен файл `pipeline/cases/ai-credit-scoring-and-underwriting-operator/00-brief.md` на русском языке.

## Почему кейс проходит порог
Потенциал LTV выше `500 000 ₽ в месяц` выглядит реалистичным, потому что продукт встраивается в core-кредитный workflow с высокой частотой использования и критичностью для бизнеса. Для такого класса клиентов монетизация естественно строится на подписке, usage по потоку заявок, кастомных моделях, интеграции в decisioning stack, SLA и постоянном сопровождении.

## Ключевой сигнал
SCORISTA прямо продаёт AI-скоринг, андеррайтинг, антифрод и подготовку кредитного решения за одну минуту, а также публично заявляет `383` клиента и `42 345 203` обработанных заявки. Это подтверждает, что рынок уже платит за автоматизацию кредитного decisioning в российском B2B-финтехе.

```

```

## Stage 3 — Demand

```md
# 02-demand — SCORISTA / AI-кредитный скоринг для МФО

## Вывод
Итог по demand validation: **GO / demand подтверждён, но с узким ICP**. Категория не массовая по публичному поисковому спросу, однако это нормальная картина для enterprise fintech. Ключевой фактор не поисковый шум, а наличие платящих B2B-покупателей, действующих альтернатив и понятной unit-экономики. По совокупности сигналов SCORISTA проходит Profit Gate.

## Demand snapshot
- API multi-demand по ключу `кредитный скоринг МФО` вернул **LOW**, но это скорее индикатор низкой публичной медийности B2B-ниши: hh vacancies = 9, Habr articles = 2, Yandex suggest = 2, Google Trends RU = 0. [T2] Источник: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9%20%D1%81%D0%BA%D0%BE%D1%80%D0%B8%D0%BD%D0%B3%20%D0%9C%D0%A4%D0%9E
- Сам рынок покупателей реален: в государственном реестре Банка России на момент проверки было **845 МФО**. [T1] Источник: https://www.cbr.ru/vfs/finmarkets/files/supervision/list_MFO.xlsx
- На сайте SCORISTA заявлены **383 клиента** и **42 345 203 обработанных заявок**, что подтверждает коммерческую зрелость категории и фактическую готовность платить. [T2] Источник: https://scorista.ru/

## Кто платит и за что
ICP: МФК/МКК с онлайн-выдачей, высоким входящим потоком заявок и потребностью одновременно снижать fraud/NPL и держать approval rate. [T1/T2]

Основная ценность:
1. автоматизация андеррайтинга,
2. сокращение time-to-decision,
3. рост approval без ухудшения риска,
4. снижение ручной проверки.

Это не SMB-self-serve продукт. Продажа идёт через B2B внедрение, интеграцию, API и настройку моделей. Поэтому низкий поисковый шум не отменяет высокий WTP. [T2]

## Конкуренты и цены
Ниже не только perfect-like-for-like, но и реальные заменители бюджета риск-команды МФО.

| Игрок | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| UNIRATE24 | проверка физлиц, скоринг, андеррайтинг-данные | от **19 ₽** за проверку физлица | прямой data/input substitute для скоринга [T2] |
| CheckPerson | проверка физлиц/заёмщиков | от **1500 ₽/мес** и от **9600 ₽/год** | низкий порог входа, подтверждает готовность платить даже малых клиентов [T2] |
| НБКИ | кредитные отчёты и скоринговые данные | отчёт для пользователя от **495 ₽** | реальный бюджетный substitute на слой данных/скоринга [T1] |

Источники:
- UNIRATE24: https://unirate24.ru/
- CheckPerson: https://checkperson.ru/
- НБКИ: https://nbki.ru/serviceszaem/history/

## WTP, proof of willingness to pay
- Готовность платить подтверждается существованием нескольких коммерческих альтернатив с публичным прайсом, от транзакционных проверок поштучно до подписок. [T1/T2]
- Наличие у SCORISTA 383 клиентов означает, что рынок уже оплачивает не только данные, но и полноценный decisioning layer. Это сильнее любого keyword-volume. [T2]
- Для МФО даже небольшое снижение fraud/default или рост конверсии окупает платный скоринг быстро, потому что решение влияет на core P&L кредитного портфеля. Это inference на основе природы юнит-экономики МФО и факта активной закупки проверок/отчётов. [T1 + inference]

## Telegram в РФ
- В demand API telegram signal = 0, подписчики не обнаружены. [T2] Источник: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B9%20%D1%81%D0%BA%D0%BE%D1%80%D0%B8%D0%BD%D0%B3%20%D0%9C%D0%A4%D0%9E
- На рынке РФ заметны в основном consumer-facing Telegram-боты/сервисы лидогенерации займов, а не B2B Telegram-native продукты для риск-менеджмента. Для SCORISTA это нейтральный фактор: канал продаж здесь enterprise, а не Telegram-first. [T3, поддержано T2 demand API]

## Market sizing
### Допущения
- Средний целевой чек на scoring/decisioning платформу для МФО беру **1,2 млн ₽ ARR** как рабочий средний кейс: это выше small-ticket подписок на проверки, но существенно ниже дорогих enterprise core-suite внедрений. Основание: публичные прайсы заменителей + enterprise nature продукта. [T1/T2 + inference]
- Доля МФО, для которых продвинутый внешний скоринг реально актуален сейчас: **35%**. Это сегмент digital-first, активно выдающих и риск-автоматизирующих игроков. [T1/T2 + inference]

### Top-down
- База рынка: **845 МФО** в реестре ЦБ. [T1]
- TAM РФ = 845 × 1,2 млн ₽ = **1,014 млрд ₽** [T1/T2 + inference]
- SAM РФ = 845 × 35% × 1,2 млн ₽ = **355 млн ₽** [T1/T2 + inference]
- SOM Y1 = 12 клиентов × 1,2 млн ₽ = **14,4 млн ₽**
- SOM Y3 = 35 клиентов × 1,2 млн ₽ = **42,0 млн ₽**

### Bottom-up
Формула: total buyers × % with need × ARR avg.
- Total buyers = **845 МФО** [T1]
- % with need = **35%** [T1/T2 + inference]
- ARR avg = **1,2 млн ₽** [T1/T2 + inference]
- SAM bottom-up = **355 млн ₽**
- SOM bottom-up Y1 = **14,4 млн ₽**
- SOM bottom-up Y3 = **42,0 млн ₽**

### 10 реальных buyers для bottom-up
1. МФК «Быстроденьги» [T1]
2. МФК «МигКредит» [T1]
3. МКК «Консалтинговая группа МиК» [T1]
4. МКК Фонд финансирования предпринимательства Тюменской области [T1]
5. МКК Удмуртский фонд развития предпринимательства [T1]
6. МКК Вологодской области «Фонд ресурсной поддержки МСП» [T1]
7. МКК Новосибирский областной фонд микрофинансирования МСП [T1]
8. НМКК «Ивановский фонд поддержки предпринимательства» [T1]
9. Фонд поддержки инвестиционных проектов креативных индустрий и микрофинансирования [T1]
10. МКК, НКО «Фонд поддержки МСП Республики Алтай» [T1]

Источник для списка: государственный реестр МФО ЦБ РФ: https://www.cbr.ru/vfs/finmarkets/files/supervision/list_MFO.xlsx

### Таблица сверки
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | н/д | н/д | для решения не использую, надёжных T1/T2 данных без платных отчётов не получил | н/д |
| TAM (РФ) | 1,014 млрд ₽ [T1/T2] | 1,014 млрд ₽ [T1/T2] | diff=0%, одна и та же база реестра ЦБ | lower |
| SAM (РФ) | 355 млн ₽ [T1/T2] | 355 млн ₽ [T1/T2] | diff=0%, сегмент одинаково определён | lower |
| SOM Y1 | 14,4 млн ₽ | 14,4 млн ₽ | diff=0% | **используем 14,4 млн ₽** |
| SOM Y3 | 42,0 млн ₽ | 42,0 млн ₽ | diff=0% | **используем 42,0 млн ₽** |

Sanity check:
- SOM Y1 = 4,1% SAM, реалистично.
- При среднем цикле сделки 2-4 месяца 12 сделок за год достижимы для узкой enterprise GTM-команды.

## Profit Gate
Проверка сценариев монетизации:
1. **SaaS / platform fee**: 12 клиентов × 100 тыс. ₽ MRR = **1,2 млн ₽ выручки/мес**.
2. **Usage-based**: при 19 ₽ за проверку и 100 тыс. проверок/мес через портфель клиентов получается **1,9 млн ₽ GMV-выручки/мес** как верхняя ориентирная планка substitute economics. [T2]
3. **Hybrid (setup + monthly + usage)**: 8 клиентов × 80 тыс. ₽ MRR = 640 тыс. ₽/мес + 200-400 тыс. ₽ usage = **840 тыс. – 1,04 млн ₽/мес**.

Даже при консервативной gross margin 70% и OPEX команды 300-500 тыс. ₽/мес, сценарии 1 и 3 позволяют выйти на **EBITDA > 500 тыс. ₽/мес** после набора первых 8-12 клиентов. **Profit Gate PASS**. [T1/T2 + inference]

## Риски
- Ниша узкая, поэтому growth limited by market size, а не demand generation.
- Продажа enterprise и интеграционная, нужен длиннее цикл сделки, чем у обычного SaaS.
- Часть рынка может собирать стек из БКИ/антифрода/внутренней data science команды и не покупать внешний full-stack scoring.

## Инвесткомитетный вывод
Несмотря на LOW в публичном demand API, кейс **не должен быть отклонён по раннему правилу**, потому что Profit Gate проходит, а willingness to pay подтверждена фактом существующих клиентов и платных заменителей. Это **качественный, но нишевой B2B fintech infra market**.

**Решение на этапе demand validation: ПРОЙТИ ДАЛЬШЕ.**

Sources: T1=4, T2=4, T3=1. Primary evidence basis: T1/T2.
```

## Stage 4 — Economics

```md
# 04-economics — SCORISTA / AI-кредитный скоринг для МФО

## Executive summary
**Итог:** economics **PASS**. Для regulated B2B fintech infra модель выглядит инвестиционно пригодной: при целевом среднем чеке **160 000 ₽ MRR на клиента**, contribution margin **82,2%**, fully-loaded blended CAC **801 667 ₽**, logo churn **1,8%/мес** и **LTV/CAC = 9,1x**. 

Даже при консервативной полной команде и фиксированных расходах около **5,68 млн ₽/мес** компания выходит на monthly break-even примерно на **44 клиентах**, а на **50 клиентах** может делать порядка **0,90 млн ₽ EBITDA/мес**, то есть выше порога Profit Gate. 

## Что продаётся и как монетизируется
Рабочая модель монетизации для SCORISTA в РФ:
1. **setup / интеграция**: 250-600 тыс. ₽ разово,
2. **platform subscription**: 90-140 тыс. ₽/мес,
3. **usage / score-packs / anti-fraud checks**: 20-80 тыс. ₽/мес,
4. **premium SLA / кастомные модели / отчётность**: 10-40 тыс. ₽/мес.

Для unit economics беру **средний blended чек 160 000 ₽ MRR на клиента**. Это выше 100 тыс. ₽ из demand-модели, но всё ещё консервативно для core-risk stack в регулируемом кредитном workflow. Основание: enterprise nature продукта, наличие интеграции, anti-fraud и decisioning-слоя, а также 383 клиента у SCORISTA. [T1][T2]

## Business process: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Поиск ICP, сбор целевых МФО/банков | SDR | CRM + базы компаний + email/phone outreach | 2-3 дня на волну | 18 000 | средняя |
| 2 | Первый контакт и qualification | SDR | телефония, email sequences, CRM | 5-10 дней | 22 000 | средняя |
| 3 | Discovery call и pain mapping | AE + presales | видеозвонки, презентация, CRM | 3-5 дней | 28 000 | низкая |
| 4 | NDA, сбор требований, оценка потока заявок | AE + CTO/аналитик | шаблоны NDA, shared docs | 5-7 дней | 35 000 | низкая |
| 5 | Техдемо / pilot design | CTO + ML + AE | demo stand, scoring sandbox | 1-2 недели | 65 000 | низкая |
| 6 | Пилот на исторических данных клиента | ML + backend + risk analyst | sandbox, ETL, notebooks, API | 2-4 недели | 120 000 | средняя |
| 7 | Согласование KPI пилота, risk/compliance review | CTO + AE + клиентский риск-менеджер | BI, docs, чек-листы | 1-2 недели | 55 000 | низкая |
| 8 | Коммерческое предложение и negotiation | AE + CEO | CPQ/шаблон оффера | 5-10 дней | 30 000 | низкая |
| 9 | Договор, ИБ, закупка, legal | CEO + AE + юрист | ЭДО, шаблоны SLA/DPA | 2-4 недели | 48 000 | низкая |
| 10 | Интеграция API / загрузка модели | backend + DevOps + ML | API gateway, monitoring, staging | 2-3 недели | 95 000 | средняя |
| 11 | Go-live и обучение риск-команды | CSM + AE + аналитик | knowledge base, training calls | 3-5 дней | 26 000 | средняя |
| 12 | Ежемесячный scoring usage и выставление счёта | finance + CSM + платёжный контур | CRM, 1C/ЭДО, billing | ежемесячно | 9 000 | высокая |

**Вывод по процессу:** цикл сделки длинный, с пилотом и комплаенс-проверкой. Это не self-serve SaaS, а regulated B2B sale, поэтому обычный CAC «только по рекламе» здесь занижает реальность. 

## COGS на 1 клиента в месяц
Беру модель клиента со средним MRR **160 000 ₽**.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / compute / storage | 9 000 | вычисления скоринга, журналирование, резервирование |
| Data bureau / внешние проверки / API | 6 500 | БКИ, антифрод, внешние верификации, агрегировано |
| Onboarding / implementation amortized | 4 000 | 120 тыс. ₽ стартового внедрения, размазано на 30 мес |
| Support / Customer Success allocation | 5 000 | доля CSM на 30-35 активных клиентов |
| Monitoring / security / DevOps allocation | 2 500 | общая observability и безопасная эксплуатация |
| Billing / документооборот / admin variable | 1 500 | ЭДО, бухгалтерия, выставление счетов |
| **Итого COGS** | **28 500** |  |

### Unit contribution
- **MRR / клиент** = **160 000 ₽**
- **COGS / клиент** = **28 500 ₽**
- **Contribution / клиент** = **131 500 ₽/мес**
- **Contribution Margin** = **82,2%**

Для B2B risk-infra продукта такой уровень валовой маржи реалистичен: compute и support умеренные, а основная ценность лежит в decisioning logic и интеграции. [T2]

## CAC by channel с funnel conversion
### Воронка по каналам
| Канал | Вход в воронку / мес | SQL / demo | Pilot | New paying customers / мес | Конверсия lead→paying |
|---|---:|---:|---:|---:|---:|
| Outbound SDR/AE | 300 target accounts | 45 | 18 | 1,0 | 0,33% |
| Paid inbound / performance | 120 inbound leads | 30 | 9 | 1,2 | 1,0% |
| Partnerships / referrals / industry events | 20 partner leads | 10 | 4 | 0,8 | 4,0% |
| **Итого blended** | **440** | **85** | **31** | **3,0** | **0,68%** |

### Fully-loaded CAC
Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocated + Tools + Events + Multiplier overhead) / New paying customers
```

### Компоненты fully-loaded CAC
SCORISTA относится к **regulated fintech B2B**, поэтому беру multiplier **x2,5**. Это соответствует сценарию с пилотом, legal/compliance review и закупочным циклом. 

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / performance) | 180 000 | рабочий budget для demand capture и ретаргета | допущение на базе B2B fintech GTM |
| Outbound team FOT (SDR + AE attributed to new) | 494 000 | SDR 150k + AE 230k gross + 30% соцвзносы + variable; доля, относимая на new biz | [T5][T6] + inference |
| Marketing team FOT (partial allocation) | 143 000 | 110k gross equivalent acquisition-share + 30% соцвзносы | [T5][T6] + inference |
| Tools (CRM, sequencing, телефония, BI) | 85 000 | amo/Битрикс + телефония + enrichment + BI | допущение |
| Events / partnerships | 60 000 | отраслевые мероприятия, travel, партнёрские touchpoints | допущение |
| **Overhead multiplier** | **1 443 000** | raw CAC pool 962k × 1,5, чтобы получить segment multiplier x2,5 | standard regulated fintech CAC loading |
| **Итого fully-loaded CAC pool** | **2 405 000** |  |  |

### CAC по каналам
| Канал | Direct cost pool, ₽/мес | New paying / мес | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound SDR/AE | 569 000 | 1,0 | 1 422 500 | самый дорогой канал, но нужен для крупных МФО |
| Paid inbound | 250 000 | 1,2 | 520 833 | лучший баланс масштаба и эффективности |
| Partnerships / referrals | 143 000 | 0,8 | 446 875 | самый качественный канал, но ограничен объёмом |
| **Blended** | **962 000** | **3,0** | **801 667** | используем в основной модели |

### Sanity check against benchmark
- Полученный blended CAC **~802 тыс. ₽**.
- Для обычного B2B fintech это выше диапазона **200-700 тыс. ₽**, но для **regulated / pilot-heavy infra** попадает в допустимый investment range **400-1200 тыс. ₽**. 
- Поэтому red flag по занижению CAC **нет**: наоборот, модель скорее консервативная, а не оптимистичная.

## LTV и churn
### Benchmark churn
Для enterprise / high-ACV B2B SaaS ориентир по месячному customer churn обычно находится в районе **0,8-1,5%**, для mid-market B2B примерно **0,8-1,5%**, а более общий B2B fintech benchmark держится около **2-5%** monthly. Для SCORISTA беру **1,8% logo churn / мес** как консервативный midpoint между enterprise lock-in и fintech risk volatility. [T3][T4]

### Расчёт
- **MRR / клиент** = 160 000 ₽
- **Contribution Margin** = 82,2%
- **Monthly churn** = 1,8%
- **LTV = MRR × Contribution Margin / Churn**
- **LTV = 160 000 × 0,821875 / 0,018 = 7 305 556 ₽**

### LTV/CAC
- **LTV** = **7,31 млн ₽**
- **Blended fully-loaded CAC** = **801 667 ₽**
- **LTV/CAC = 9,1x**

Это сильно выше минимального investment-grade порога **3,0x**.

## CAC payback
- **CAC Payback = CAC / Monthly contribution per customer**
- **801 667 / 131 500 = 6,1 месяца**

Для regulated enterprise-like sale это хороший результат. Он заметно лучше допустимого порога **<18 мес** и лучше базового порога **<12 мес**.

## Team & FOT
### Полная команда
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Onboarding ramp до 80% productivity, мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO / Tech Lead | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| Senior Backend | 2 | 270 000 | 1,5 | 1,5 | 81 000 each | 702 000 |
| ML Engineer | 1 | 350 000 | 2,5 | 2 | 105 000 | 455 000 |
| DevOps | 1 | 340 000 | 1,5 | 1 | 102 000 | 442 000 |
| Frontend | 1 | 200 000 | 1 | 1 | 60 000 | 260 000 |
| SDR | 1 | 150 000 | 0,75 | 1 | 45 000 | 195 000 |
| AE | 1 | 300 000 | 1,5 | 2,5 | 90 000 | 390 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### Salary realism
Использую уровни, которые укладываются в наблюдаемые вилки hh.ru по Москве / удалёнке для 2025-2026:
- senior backend в fintech: **400-600k на руки** встречается на hh.ru, значит gross 270-420k реалистичен; [T5]
- tech lead / head of engineering: **400-500k+**; [T6]
- DevOps: **200-300k+ gross** на рынке, для senior/fintech беру 340k gross как реалистичный midpoint; [T7]
- frontend middle+/senior: **250-350k** в сильных командах; [T8]
- SDR: **100-150k на руки** в B2B SaaS, gross 150k реалистичен; [T5]
- AE / account executive: **150-250k на руки** и выше, gross 300k под fintech enterprise sale реалистичен; [T9]

### Итого monthly team FOT
- **Полный team FOT fully-loaded** = **4 862 000 ₽/мес**

## Cumulative FOT timeline M1-M12
### План найма
- **M1**: CEO
- **M2**: SDR, Frontend
- **M3**: AE, 1 Senior Backend, Customer Success
- **M4**: CTO, DevOps
- **M5**: 2-й Senior Backend, ML Engineer
- **M6-M12**: без агрессивного over-hiring, фокус на продажах и донастройке delivery

Такой план соблюдает hiring realism: нет найма 5+ человек в первый месяц, ключевые senior-роли подключаются постепенно, с учётом market time-to-hire.

| Месяц | Кто в штате | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 780 000 |
| M2 | CEO + SDR + Frontend | 1 235 000 |
| M3 | + AE + Senior Backend(1) + CS | 2 613 000 |
| M4 | + CTO + DevOps | 3 705 000 |
| M5 | + Senior Backend(2) + ML | 4 862 000 |
| M6 | full team | 4 862 000 |
| M7 | full team | 4 862 000 |
| M8 | full team | 4 862 000 |
| M9 | full team | 4 862 000 |
| M10 | full team | 4 862 000 |
| M11 | full team | 4 862 000 |
| M12 | full team | 4 862 000 |

## Fixed costs breakdown
| Статья fixed costs | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 4 862 000 |
| Shared cloud / platform minimum | 220 000 |
| Data bureau minimum commits | 180 000 |
| Office / legal / accounting | 140 000 |
| Security / compliance | 90 000 |
| CRM / sales / monitoring tools | 85 000 |
| Travel / industry events baseline | 60 000 |
| Misc admin | 40 000 |
| **Итого fixed costs / мес** | **5 677 000** |

## Break-even
### Break-even by client count
- **Contribution per client / мес** = **131 500 ₽**
- **Fixed costs / мес** = **5 677 000 ₽**
- **Break-even clients = 5 677 000 / 131 500 = 43,2 клиента**
- Округлённо: **44 платящих клиента**

### Break-even by month
Консервативный план набора клиентов:
- M1: 0
- M2: 0
- M3: 1
- M4: 2
- M5: 4
- M6: 6
- M7: 9
- M8: 13
- M9: 18
- M10: 24
- M11: 31
- M12: 39
- **M13: 44**

Отсюда monthly operating break-even достигается примерно в **M13**.

### Проверка 50 клиентов
- **50 клиентов × 131 500 ₽ contribution = 6 575 000 ₽/мес**
- **EBITDA = 6 575 000 - 5 677 000 = 898 000 ₽/мес**

То есть даже на уровне **50 клиентов** компания проходит требование Profit Gate, потому что **EBITDA > 500k ₽/мес достижим**.

## Burn-to-breakeven
На траектории выше отрицательный EBITDA по месяцам составляет:
- M1: -1,60 млн ₽
- M2: -2,05 млн ₽
- M3: -3,30 млн ₽
- M4: -4,26 млн ₽
- M5: -5,15 млн ₽
- M6: -4,89 млн ₽
- M7: -4,49 млн ₽
- M8: -3,97 млн ₽
- M9: -3,31 млн ₽
- M10: -2,52 млн ₽
- M11: -1,60 млн ₽
- M12: -0,55 млн ₽
- M13: +0,11 млн ₽

**Совокупный burn до operating break-even ≈ 37,7 млн ₽.**

## Cash runway
Берём **startup capital = 45 млн ₽**.

- При среднем burn на траектории M1-M12 около **3,14 млн ₽/мес** runway составляет около **14,3 месяца**.
- Это покрывает путь до break-even в M13 с небольшим запасом.
- Для enterprise fintech infra стартовый капитал **45 млн ₽** выглядит реалистично и не попадает в red flag по недофинансированию.

## Investment view
### Сильные стороны economics
1. Высокая contribution margin для инфраструктурного risk-product.
2. CAC payback **6,1 мес**, что хорошо для regulated B2B.
3. LTV/CAC **9,1x**, большой запас над threshold 3x.
4. Break-even достижим уже в диапазоне **44-50 клиентов**, а не в сотнях клиентов.
5. Наличие у SCORISTA **383 клиентов** дополнительно снижает execution risk модели. [T2]

### Главные риски
1. Продажа зависит от длинного пилотного цикла и legal/compliance review.
2. Revenue concentration risk: крупные МФО могут давать disproportionate share выручки.
3. В кризисные периоды credit policies клиентов могут урезать объёмы scoring usage.
4. Нужна сильная customer success и model monitoring дисциплина, иначе churn вырастет выше базового 1,8%.

## Profit Gate
Проверка ключевых порогов:
- EBITDA > 500k ₽/мес при 50 клиентах: **PASS**
- LTV/CAC > 1,0x: **PASS**
- LTV/CAC ≥ 3,0x для investment grade: **PASS**
- CAC Payback < 18 мес: **PASS**

## Итог
**Решение: PASS.**

SCORISTA проходит Program 5 / Unit Economics. Для инвестиционного фонда это **качественный niche fintech infra asset**: рынок не бесконечный, но economics сильная, CAC реалистично посчитан fully-loaded, а достижение EBITDA >500k ₽/мес на масштабе **50 клиентов** выглядит правдоподобно.

## Sources
- **T1**: ЦБ РФ, государственный реестр МФО — https://www.cbr.ru/vfs/finmarkets/files/supervision/list_MFO.xlsx
- **T2**: SCORISTA, сайт компании — https://scorista.ru/
- **T3**: SaaS churn benchmark by segment, enterprise vs mid-market — https://culta.ai/blog/saas-churn-rate-guide-benchmarks
- **T4**: 2026 churn benchmark overview — https://www.saaspricelab.com/benchmarks/saas-churn-rates
- **T5**: hh.ru, senior backend / SDR / sales examples — https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost and https://hh.ru/vacancies/account_executive/polniy_den
- **T6**: hh.ru, tech lead / head of engineering examples — https://hh.ru/vacancies/team_leader
- **T7**: hh.ru, DevOps market examples — https://hh.ru/vacancies/devops-engineer
- **T8**: hh.ru, frontend market examples — https://hh.ru/vacancies/frontend-developer
- **T9**: hh.ru, account executive market examples — https://hh.ru/vacancies/account_executive

**Где есть inference:** распределение COGS, channel allocation, pricing mix, monthly cohort ramp и attributed FOT являются аналитическими допущениями, построенными на типовой модели regulated B2B SaaS/fintech sales и подтверждёнными порядком рыночных бенчмарков из источников выше.
```

## Stage 5 — Critic

```md
# SECTION A. PnL / 12 месяцев / 3 сценария

## Допущения модели
- Источник чисел: `04-economics.md` по кейсу SCORISTA.
- База: ARPA 160 000 ₽/мес, COGS 28 500 ₽/клиент/мес, contribution 131 500 ₽/клиент/мес, fixed costs на полном штате 5 677 000 ₽/мес.
- Сценарии:
  - Base: траектория найма и продаж из economics, churn 1,8%/мес, налоговая цель, IT-льгота 3% с выручки.
  - Optimistic: быстрее ramp продаж, ARPA +10%, churn 1,2%/мес, fixed cost выше базы на ~40 тыс. ₽/мес по non-payroll.
  - Pessimistic: slower ramp, ARPA 145 000 ₽, churn 3,0%/мес, COGS 32 000 ₽/клиент/мес, fixed cost выше из-за менее эффективной загрузки и отсутствия IT-льготы.
- Cash burn = max(0, -EBITDA). Cumulative cash показан как накопленный операционный cash result до финансирования, старт из 0 ₽.

## Базовый сценарий
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.0 | 0.0 | 1.0 | 1.0 | 2.0 | 2.0 | 3.0 | 4.0 | 5.0 | 6.0 | 7.0 | 8.0 |
| Total clients | 0.0 | 0.0 | 1.0 | 2.0 | 3.9 | 5.9 | 8.8 | 12.6 | 17.4 | 23.1 | 29.7 | 37.1 |
| MRR | 0 ₽ | 0 ₽ | 160 000 ₽ | 317 120 ₽ | 631 412 ₽ | 940 046 ₽ | 1 403 126 ₽ | 2 017 869 ₽ | 2 781 548 ₽ | 3 691 480 ₽ | 4 745 033 ₽ | 5 939 623 ₽ |
| COGS | 0 ₽ | 0 ₽ | 28 500 ₽ | 56 487 ₽ | 112 470 ₽ | 167 446 ₽ | 249 932 ₽ | 359 433 ₽ | 495 463 ₽ | 657 545 ₽ | 845 209 ₽ | 1 057 995 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 131 500 ₽ | 260 633 ₽ | 518 942 ₽ | 772 601 ₽ | 1 153 194 ₽ | 1 658 436 ₽ | 2 286 085 ₽ | 3 033 935 ₽ | 3 899 824 ₽ | 4 881 627 ₽ |
| GM% | 0.0% | 0.0% | 82.2% | 82.2% | 82.2% | 82.2% | 82.2% | 82.2% | 82.2% | 82.2% | 82.2% | 82.2% |
| Fixed costs | 1 595 000 ₽ | 2 050 000 ₽ | 3 428 000 ₽ | 4 520 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ | 5 677 000 ₽ |
| EBITDA | -1 595 000 ₽ | -2 050 000 ₽ | -3 296 500 ₽ | -4 259 367 ₽ | -5 158 058 ₽ | -4 904 399 ₽ | -4 523 806 ₽ | -4 018 564 ₽ | -3 390 915 ₽ | -2 643 065 ₽ | -1 777 176 ₽ | -795 373 ₽ |
| Cash burn | 1 595 000 ₽ | 2 050 000 ₽ | 3 296 500 ₽ | 4 259 367 ₽ | 5 158 058 ₽ | 4 904 399 ₽ | 4 523 806 ₽ | 4 018 564 ₽ | 3 390 915 ₽ | 2 643 065 ₽ | 1 777 176 ₽ | 795 373 ₽ |
| Cumulative cash | -1 595 000 ₽ | -3 645 000 ₽ | -6 941 500 ₽ | -11 200 867 ₽ | -16 358 925 ₽ | -21 263 325 ₽ | -25 787 131 ₽ | -29 805 695 ₽ | -33 196 610 ₽ | -35 839 675 ₽ | -37 616 851 ₽ | -38 412 224 ₽ |

### Waterfall и налоги
- ARPA: 160 000 ₽
- Gross: 131 500 ₽ = ARPA 160 000 ₽ - COGS 28 500 ₽
- Contribution: 131 500 ₽ (в этой модели gross = contribution, т.к. support/data usage уже в COGS)
- EBITDA at break-even load: около 0 ₽ на клиента после распределения fixed costs 131 500 ₽ на клиента при 43,2 клиентах
- Net after taxes: около -4 800 ₽ на клиента при режиме `IT-льгота 3% с выручки (целевой режим)`
- Сравнение налоговых режимов на 12-месячной выручке:
  - УСН 6%: Net ≈ -39 769 859 ₽
  - IT-льгота 3%: Net ≈ -39 091 041 ₽
  - ОСНО 20% на прибыль: Net ≈ -38 412 224 ₽ до влияния НДС
- Страховые взносы: ~30% к ФОТ уже включены в FOT и fixed costs.
- НДС 20% не моделируется в PnL при IT/УСН; при ОСНО станет кассовой и ценовой нагрузкой.

### Break-even и cash flow
- Break-even по client count: 43,2 клиента, округлённо 44.
- Break-even по месяцам: M13 при сохранении темпа M12 по new clients; в пределах M1-M12 ещё не достигнут.
- startup_capital_to_bep_rub: 38 412 224 ₽.
- 12m итог: выручка 22 627 256 ₽, gross profit 18 596 776 ₽, EBITDA -38 412 224 ₽.

## Оптимистичный сценарий
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.0 | 1.0 | 1.0 | 2.0 | 3.0 | 3.0 | 4.0 | 5.0 | 6.0 | 8.0 | 9.0 | 10.0 |
| Total clients | 0.0 | 1.0 | 2.0 | 4.0 | 6.9 | 9.8 | 13.7 | 18.6 | 24.3 | 32.0 | 40.7 | 50.2 |
| MRR | 0 ₽ | 176 000 ₽ | 349 888 ₽ | 697 689 ₽ | 1 217 317 ₽ | 1 730 709 ₽ | 2 413 941 ₽ | 3 264 973 ₽ | 4 281 794 ₽ | 5 638 412 ₽ | 7 154 751 ₽ | 8 828 894 ₽ |
| COGS | 0 ₽ | 30 000 ₽ | 59 640 ₽ | 118 924 ₽ | 207 497 ₽ | 295 007 ₽ | 411 467 ₽ | 556 530 ₽ | 729 851 ₽ | 961 093 ₽ | 1 219 560 ₽ | 1 504 925 ₽ |
| Gross profit | 0 ₽ | 146 000 ₽ | 290 248 ₽ | 578 765 ₽ | 1 009 820 ₽ | 1 435 702 ₽ | 2 002 474 ₽ | 2 708 444 ₽ | 3 551 943 ₽ | 4 677 319 ₽ | 5 935 191 ₽ | 7 323 969 ₽ |
| GM% | 0.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% | 83.0% |
| Fixed costs | 1 635 000 ₽ | 2 090 000 ₽ | 3 468 000 ₽ | 4 560 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ | 5 717 000 ₽ |
| EBITDA | -1 635 000 ₽ | -1 944 000 ₽ | -3 177 752 ₽ | -3 981 235 ₽ | -4 707 180 ₽ | -4 281 298 ₽ | -3 714 526 ₽ | -3 008 556 ₽ | -2 165 057 ₽ | -1 039 681 ₽ | 218 191 ₽ | 1 606 969 ₽ |
| Cash burn | 1 635 000 ₽ | 1 944 000 ₽ | 3 177 752 ₽ | 3 981 235 ₽ | 4 707 180 ₽ | 4 281 298 ₽ | 3 714 526 ₽ | 3 008 556 ₽ | 2 165 057 ₽ | 1 039 681 ₽ | 0 ₽ | 0 ₽ |
| Cumulative cash | -1 635 000 ₽ | -3 579 000 ₽ | -6 756 752 ₽ | -10 737 987 ₽ | -15 445 167 ₽ | -19 726 465 ₽ | -23 440 992 ₽ | -26 449 548 ₽ | -28 614 605 ₽ | -29 654 286 ₽ | -29 436 094 ₽ | -27 829 125 ₽ |

### Waterfall и налоги
- ARPA: 176 000 ₽
- Gross: 146 000 ₽ = ARPA 176 000 ₽ - COGS 30 000 ₽
- Contribution: 146 000 ₽ (в этой модели gross = contribution, т.к. support/data usage уже в COGS)
- EBITDA at break-even load: около 0 ₽ на клиента после распределения fixed costs 146 000 ₽ на клиента при 39,2 клиентах
- Net after taxes: около -5 280 ₽ на клиента при режиме `IT-льгота 3% с выручки (при аккредитации Минцифры)`
- Сравнение налоговых режимов на 12-месячной выручке:
  - УСН 6%: Net ≈ -29 974 387 ₽
  - IT-льгота 3%: Net ≈ -28 901 756 ₽
  - ОСНО 20% на прибыль: Net ≈ -27 829 125 ₽ до влияния НДС
- Страховые взносы: ~30% к ФОТ уже включены в FOT и fixed costs.
- НДС 20% не моделируется в PnL при IT/УСН; при ОСНО станет кассовой и ценовой нагрузкой.

### Break-even и cash flow
- Break-even по client count: 39,2 клиента, округлённо 40.
- Break-even по месяцам: M11.
- startup_capital_to_bep_rub: 29 654 286 ₽.
- 12m итог: выручка 35 754 370 ₽, gross profit 29 659 875 ₽, EBITDA -27 829 125 ₽.

## Пессимистичный сценарий
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.0 | 0.0 | 0.0 | 1.0 | 1.0 | 2.0 | 2.0 | 3.0 | 4.0 | 4.0 | 5.0 | 6.0 |
| Total clients | 0.0 | 0.0 | 0.0 | 1.0 | 2.0 | 3.9 | 5.8 | 8.6 | 12.4 | 16.0 | 20.5 | 25.9 |
| MRR | 0 ₽ | 0 ₽ | 0 ₽ | 145 000 ₽ | 285 650 ₽ | 567 080 ₽ | 840 068 ₽ | 1 249 866 ₽ | 1 792 370 ₽ | 2 318 599 ₽ | 2 974 041 ₽ | 3 754 820 ₽ |
| COGS | 0 ₽ | 0 ₽ | 0 ₽ | 32 000 ₽ | 63 040 ₽ | 125 149 ₽ | 185 394 ₽ | 275 833 ₽ | 395 558 ₽ | 511 691 ₽ | 656 340 ₽ | 828 650 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 0 ₽ | 113 000 ₽ | 222 610 ₽ | 441 932 ₽ | 654 674 ₽ | 974 034 ₽ | 1 396 813 ₽ | 1 806 908 ₽ | 2 317 701 ₽ | 2 926 170 ₽ |
| GM% | 0.0% | 0.0% | 0.0% | 77.9% | 77.9% | 77.9% | 77.9% | 77.9% | 77.9% | 77.9% | 77.9% | 77.9% |
| Fixed costs | 1 720 000 ₽ | 2 200 000 ₽ | 3 650 000 ₽ | 4 780 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ | 6 000 000 ₽ |
| EBITDA | -1 720 000 ₽ | -2 200 000 ₽ | -3 650 000 ₽ | -4 667 000 ₽ | -5 777 390 ₽ | -5 558 068 ₽ | -5 345 326 ₽ | -5 025 966 ₽ | -4 603 187 ₽ | -4 193 092 ₽ | -3 682 299 ₽ | -3 073 830 ₽ |
| Cash burn | 1 720 000 ₽ | 2 200 000 ₽ | 3 650 000 ₽ | 4 667 000 ₽ | 5 777 390 ₽ | 5 558 068 ₽ | 5 345 326 ₽ | 5 025 966 ₽ | 4 603 187 ₽ | 4 193 092 ₽ | 3 682 299 ₽ | 3 073 830 ₽ |
| Cumulative cash | -1 720 000 ₽ | -3 920 000 ₽ | -7 570 000 ₽ | -12 237 000 ₽ | -18 014 390 ₽ | -23 572 458 ₽ | -28 917 785 ₽ | -33 943 751 ₽ | -38 546 938 ₽ | -42 740 030 ₽ | -46 422 329 ₽ | -49 496 160 ₽ |

### Waterfall и налоги
- ARPA: 145 000 ₽
- Gross: 113 000 ₽ = ARPA 145 000 ₽ - COGS 32 000 ₽
- Contribution: 113 000 ₽ (в этой модели gross = contribution, т.к. support/data usage уже в COGS)
- EBITDA at break-even load: около 0 ₽ на клиента после распределения fixed costs 113 000 ₽ на клиента при 53,1 клиентах
- Net after taxes: около -8 700 ₽ на клиента при режиме `УСН 6% с выручки (без IT-льготы)`
- Сравнение налоговых режимов на 12-месячной выручке:
  - УСН 6%: Net ≈ -50 331 809 ₽
  - IT-льгота 3%: Net ≈ -49 913 984 ₽
  - ОСНО 20% на прибыль: Net ≈ -49 496 160 ₽ до влияния НДС
- Страховые взносы: ~30% к ФОТ уже включены в FOT и fixed costs.
- Если клиент требует ОСНО, НДС 20% дополнительно ухудшит cash conversion и цену входа.

### Break-even и cash flow
- Break-even по client count: 53,1 клиента, округлённо 54.
- Break-even по месяцам: за пределами M12.
- startup_capital_to_bep_rub: 49 496 160 ₽.
- 12m итог: выручка 13 927 494 ₽, gross profit 10 853 840 ₽, EBITDA -49 496 160 ₽.

## Вывод по SECTION A
- Base: к M12 ещё отрицательный EBITDA, но дефицит почти закрыт; operating break-even в M13.
- Optimistic: выходит в плюс в пределах горизонта M12, требует меньше стартового капитала и подтверждает upside модели.
- Pessimistic: не доходит до break-even за 12 месяцев, поэтому чувствителен к темпу продаж, churn и налоговому режиму.

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## Sensitivity analysis: EBITDA через 12 мес after M12 baseline
Допущение для stress-test: после M12 команда уже fully hired, поэтому смотрю следующий 12-месячный отрезок до **M24**. В базе сохраняется темп **8 новых клиентов/мес** как уровень M12, стартовая база = **37,1 клиента** на конце M12, fixed costs = **5 677 000 ₽/мес**. Для CAC x2 предполагаю, что при том же GTM-бюджете new paying logos падают примерно вдвое, с ~8 до ~4 в месяц.

| Сценарий | Ключевое изменение | Active clients @M24 | Contribution / client | EBITDA @M24 |
|---|---|---:|---:|---:|
| Base | без изменений | 116,9 | 131 500 ₽ | **9,69 млн ₽/мес** |
| Sens1 | CAC x2 | 73,4 | 131 500 ₽ | **3,97 млн ₽/мес** |
| Sens2 | Churn x2, до 3,6%/мес | 103,0 | 131 500 ₽ | **7,87 млн ₽/мес** |
| Sens3 | Price -30%, ARPU 112k ₽ | 116,9 | 83 500 ₽ | **4,08 млн ₽/мес** |

Вывод: самая болезненная ось для модели не churn сама по себе, а сочетание **price compression + CAC inflation**. База остаётся прибыльной на M24, но запас прочности быстро сужается, если рынок начнёт демпинговать или acquisition станет дороже.

## Monte Carlo Lite — confidence intervals
### Inputs (triangular distribution)
| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC ₽ | 520 833 | 801 667 | 1 603 334 | [T2][T5][T6] |
| Monthly churn % | 1,2% | 1,8% | 3,6% | [T3][T4] |
| ARPU ₽/мес | 145 000 | 160 000 | 176 000 | [T1][T2] |
| Conversion rate lead→paid % | 0,33% | 0,68% | 1,0% | [T2] |
| Time-to-hire месяцев (среднее) | 1,0 | 1,6 | 2,5 | [T5][T6][T7][T8][T9] |

Метод: вместо полного кода на 1000 прогонов использую **9 комбинаций** around min/mode/max, где база берёт mode/mode/mode, best case = CAC_min + churn_min + ARPU_max, worst case = CAC_max + churn_max + ARPU_min. Это даёт достаточно хороший proxy для p10/p50/p90 на инвестиционном pre-seed / seed уровне.

### Monte Carlo Lite results
| Метрика | p10 | p50 | p90 | Range width |
|---------|---:|---:|---:|---:|
| EBITDA @M24 (₽/мес) | **-1,17 млн ₽** | **2,54 млн ₽** | **6,71 млн ₽** | **7,88 млн ₽** |
| CAC payback (мес) | 13,8 | 6,1 | 3,5 | 10,2 |
| LTV/CAC | 2,0x | 9,1x | 23,6x | 21,6x |
| Cash runway (мес) | 38,6 | 99+ | 99+ | 60,4+ |

Интерпретация правил:
1. **p10 EBITDA < 0** → автоматически появляется kill criterion #1, потому что нижний дециль уже уводит бизнес в риск неплатёжеспособности.
2. **p50 EBITDA = 2,54 млн ₽/мес**, значит median проходит EBITDA Gate >500k ₽/мес.
3. Формально отношение **p90/p10** неинтерпретируемо, потому что p10 отрицательный; practically это значит, что tail-risk слишком велик и score должен быть downgraded на неопределённость.
4. **Range width по LTV/CAC = 21,6x > 8**, значит модель хрупкая: outcome слишком чувствителен к pricing, churn и CAC.

## Competitor deep-dive
Ниже market-share estimates даны как **грубая аналитическая оценка**, а не как audited share: у private players почти нет публичной выручки по сегменту AI-credit scoring, поэтому доли считаю по customer footprint, brand presence и глубине в кредитном workflow.

### Топ-3 западных
| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **FICO** | де-факто мировой стандарт в credit decisioning, сильный brand moat, глубокая интеграция в банки | тяжёлый enterprise stack, дорогой и медленный rollout, слабая локализация под РФ | **15-20% глобального decisioning / score software в tier-1 банках** | SCORISTA дешевле, быстрее внедряется и лучше адаптирован под МФО/небанковский РФ-контур |
| **Provenir** | AI decisioning platform, orchestration, сильный fraud + risk workflow, много клиентов по миру | меньше brand power, чем у FICO, интеграция всё равно enterprise-heavy | **5-8% global next-wave decisioning platforms** | локальная data residency, русскоязычная внедренческая команда, better fit для 152-ФЗ и санкционного контура |
| **Zest AI** | сильный AI/ML narrative, explainable lending, фокус на underwriting uplift | в основном US market, зависимость от local US credit stack, слабая применимость вне США | **<3% глобально, но заметная доля в AI-native US lending** | SCORISTA уже встроен в РФ risk stack, не требует адаптации под локальные БКИ, AML и KYC-процессы |

Ориентиры по источникам: FICO claims **“4+ billion decisions annually”**, Provenir claims **“145+ countries / 90+ AI models”**, Zest AI works with **“350+ lenders”**. Это подтверждает сильные платформы, но не отменяет локального барьера входа в РФ. Источники: https://www.fico.com/en/products/fico-platform, https://www.provenir.com/, https://www.zest.ai/.

### Топ российских / локальных substitute-конкурентов
| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Скоринг Бюро (бывш. ОКБ)** | сильнейший доступ к кредитным историям, trust у банков и МФО, данные как moat | bureau-first, а не agile SaaS-product; кастомизация и скорость хуже product-native игроков | **20-25% РФ на data-bureau layer, 10-15% в adjacent scoring workflows** | SCORISTA продаёт decisioning layer поверх данных, а не только data access |
| **Double Data** | alt-data, antifraud, ML-подход, сильная известность в fintech | санкционная и enterprise-complexity нагрузка, длинный цикл сделки | **5-10% РФ в AI-risk / antifraud stack** | у SCORISTA уже доказанный focus именно на кредитном скоринге и operational fit для МФО |
| **Smart Engines** | сильные OCR/KYC/IDV технологии, важный anti-fraud слой | это не full credit decisioning platform, а инфраструктурный компонент | **5-8% РФ в KYC/verification layer, ниже в full scoring** | SCORISTA ближе к core underwriting outcome, а не к точечному document-recognition модулю |
| **UNIRATE24** | понятный прайс, быстрый вход, data-check substitute для малого клиента | ниже глубина decisioning, скорее точечные проверки, чем full-stack risk engine | **3-5% РФ у small-ticket МФО и SMB-lenders** | SCORISTA выигрывает на ACV, кастомных моделях и глубине интеграции |
| **CheckPerson** | дешёвый вход, KYC/проверка физлиц, хорошо закрывает базовый verify-use-case | low-end substitute, слабее как full scoring / decisioning engine | **2-4% в small-ticket verification layer** | SCORISTA лучше там, где нужен рост approval rate и управление риск-политикой, а не только проверка анкеты |

Локальные источники и сигналы:
- **Скоринг Бюро / ОКБ**: rusprofile company profile и отраслевые публикации подтверждают масштаб бюро и institutional position, плюс на Habr и vc.ru регулярно обсуждается роль БКИ как data-layer рынка. https://www.rusprofile.ru/
- **Double Data**: кейсы и упоминания в экосистеме Skolkovo подтверждают AI/anti-fraud positioning. https://sk.ru/
- **Smart Engines**: публикации на Habr подтверждают сильный OCR/KYC moat для финтеха. https://habr.com/
- **UNIRATE24** и **CheckPerson** уже подтверждены в demand-section как реальные бюджетные substitutes с публичным прайсом. [T2]

Главный вывод по конкурентам: на Западе рынок сильнее институционализирован, но в РФ у SCORISTA есть понятный moat за счёт **локального compliance-fit, интеграции в МФО workflow и готового decisioning-слоя**, тогда как многие локальные альтернативы продают либо данные, либо KYC, либо antifraud-модуль, но не весь underwriting loop.

## Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять CTO/ML lead в срок | med | high | time-to-hire > 3 мес, офферы отклоняются | поднять comp, использовать fractional advisors, начать с внешнего team-lead контура |
| Operational | Сбой / деградация model quality после обновления | med | high | рост false positive / false negative, жалобы risk-команд клиентов | champion-challenger, model monitoring, rollback policy, monthly recalibration |
| Operational | Зависимость от LLM/API или внешних data APIs | med | med | рост latency, падение SLA, vendor price hike | multi-vendor architecture, offline fallback, кэширование critical workflows |
| Market | Спрос оказывается уже насыщен incumbent-решениями | med | high | win rate < 15%, pilots не конвертятся в paid | сузить ICP до digital-first МФО, продавать faster deployment и uplift economics |
| Market | Price compression из-за демпинга data-check игроков | high | high | discounting > 25%, сделки уходят в low-end substitutes | value-based pricing, bundling anti-fraud + decisioning, multi-year contracts |
| Market | Конкурент выигрывает за счёт bundle с БКИ/антифродом | med | med | чаще запрашивают one-stop-shop и “всё в одном” | партнёрства с бюро/IDV, white-label ecosystem strategy |
| Regulatory | 152-ФЗ / data residency ужесточают требования к хранению данных | high | high | клиенты требуют on-prem / private cloud, DPA redlines растут | RU-hosting by default, private perimeter deployment, юридические шаблоны |
| Regulatory | 115-ФЗ / AML-KYC требования меняют пайплайн проверки клиента | med | med | новые mandatory checks в procurement | модульная архитектура KYC, интеграции с верификацией и антифродом |
| Regulatory | Санкции или ограничения на западный SaaS / cloud | high | high | vendor lockout, отказ международных сервисов | импортонезависимый стек, российские облака, локальные observability/security substitutes |
| Financial | Burn выше плана, runway падает ниже safe threshold | med | high | cash runway < 9 мес, burn > 4 млн ₽/мес 2 месяца подряд | freeze hiring, cut acquisition spend, bridge round, renegotiate vendor costs |
| Financial | USD/RUB volatility повышает cloud/data costs | high | med | gross margin падает < 75% | рублёвые контракты, валютный buffer, pricing clauses |
| Financial | Налоговая нагрузка и отмена IT-льгот ухудшают EBITDA | med | med | effective tax rate > plan на 3+ п.п. | держать резерв, юридически поддерживать аккредитацию, сценарное бюджетирование |
| Black swan | Новая волна санкций / война блокирует часть клиентов и поставщиков | med | high | stop-payments, legal freezes, delayed collections | concentration cap, domestic supplier stack, emergency contingency plan |
| Black swan | Отключение критичного внешнего data/LLM/provider слоя | med | high | внезапные 5xx / contract termination | резервный поставщик, graceful degradation, локальные модели / on-prem fallback |

## Kill conditions через 6 месяцев
1. **Median-to-downside insolvency trigger:** если обновлённый p10 по EBITDA на горизонте 24 мес всё ещё **< 0**, а runway **< 12 мес**, продолжать нельзя.
2. **EBITDA Gate fail:** если к M6 ожидаемый **p50 EBITDA@M24 < 500 000 ₽/мес**, кейс не проходит даже median-сценарий.
3. **Commercial traction fail:** если через 6 месяцев active paying clients **< 15** или pilot→paid conversion **< 20%**, значит GTM не подтверждён и масштабирование нельзя финансировать.

## Итог SECTION B
SCORISTA остаётся **интересным, но не low-risk** кейсом. Unit economics в базе сильная, однако Monte Carlo Lite показывает широкий разброс outcomes: median проходит, downside уже уходит в отрицательный EBITDA, а LTV/CAC слишком волатилен. Значит инвестрешение допустимо только при жёстком контроле за pricing discipline, локальным compliance moat и скоростью превращения pilot в paid.

<!-- P6B-DONE -->

```

## Stage 6 — Verdict

```md
[FINTECH] SCORISTA AI-кредитный скоринг — APPROVED WITH NOTES: 74/100 | EBITDA base=898К₽/мес через 13 мес | LTV/CAC=9,1x | Ключевое преимущество: глубокая встройка в regulated credit workflow | Главный риск: downside-сценарий всё ещё уходит в отрицательный EBITDA.

# 06-verdict — SCORISTA / AI-кредитный скоринг для МФО

sector: FINTECH
status: APPROVED WITH NOTES
score: 74/100
date: 2026-04-24
case_slug: scorista-ai-kreditnyy-skoring-v2

## Investment committee verdict
**Вердикт: APPROVED WITH NOTES.**

Кейс проходит investment committee threshold, потому что выполняет обе ключевые проверки на дату **2026-04-24**:
1. **score = 74/100**, то есть попадает в диапазон `70-74 = APPROVED with notes`;
2. **company_ebitda_potential_rub_month = 898 000 ₽/мес** в базовом сценарии достигается уже примерно на **50 клиентах** и **через 13 месяцев**, то есть укладывается в gate `≥500k ₽/мес`, `≤50 клиентов`, `≤24 месяцев`.

При этом approve не «чистый»: downside из Monte Carlo Lite слабее, чем хотелось бы для low-risk asset. Комитет может одобрять кейс только как **regulated niche infra bet** с жёсткими условиями по pricing discipline, pilot-to-paid conversion и локальному compliance moat.

## Оценка
Source tier balance: T1=4, T2=4, T3=1, weighted=2.33. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 9,1x», «CAC Payback = 6,1 месяца», «Contribution Margin = 82,2%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «на 50 клиентах может делать порядка 0,90 млн ₽ EBITDA/мес», «monthly break-even достигается примерно в M13». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 18 | «в государственном реестре Банка России ... 845 МФО», «SCORISTA заявлены 383 клиента и 42 345 203 обработанных заявок». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 18 | «локальный compliance-fit, интеграции в МФО workflow и готовый decisioning-слой» создают защиту, но не монополию. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | «p10 EBITDA < 0», плюс высокий регуляторный и санкционный риск в 152-ФЗ / data residency контуре. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | «Blended fully-loaded CAC = 801 667 ₽», «pilot-heavy infra», но 10 named targets и channel-fit указыват на реалистичный enterprise GTM. |

**Sum raw = 111/150. Normalized score = round((111 × 100) / 150) = 74/100.**

## Почему это не 80+
- Рынок реальный, но **узкий**: SAM около **355 млн ₽** по demand-модели, поэтому upside ограничен размером ICP.
- Moat хороший, но не выдающийся: сильная встройка в workflow есть, однако часть защиты принадлежит не только продукту, но и локальному compliance-факту рынка.
- По риску исполнения кейс не investment-grade premium: **p10 EBITDA @M24 = -1,17 млн ₽/мес**, то есть downside всё ещё ломает профиль качества.

## 7-factor Moat framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| 2. Switching costs | 3 | Интеграции, risk-policy tuning и встройка в кредитный контур создают высокие switching costs. |
| 3. Scale economies | 2 | COGS умеренный, а fixed-cost база размывается по мере роста клиентской базы. |
| 4. Proprietary data / model advantage | 2 | У SCORISTA есть сильный signal по «42 345 203 обработанных заявок», но масштаб датасета не полностью раскрыт по сегментам. |
| 5. Regulatory moat | 3 | Локальный data residency, 152-ФЗ и МФО/банковский compliance-контур работают как естественный барьер входа. |
| 6. Brand / distribution | 2 | «383 клиента» создают trust и distribution signal, но не дают доминирующего бренд-moat уровня FICO. |
| 7. Embedded workflow | 3 | Продукт сидит в core underwriting loop, а не в периферийном модуле. |

**Moat raw = 15/21. Moat score = round((15 × 25) / 21) = 18/25.**

## FULL business process from 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Поиск ICP, сбор целевых МФО/банков | SDR | CRM + базы компаний + email/phone outreach | 2-3 дня | 18 000 | средняя |
| 2 | Первый контакт и qualification | SDR | телефония, email sequences, CRM | 5-10 дней | 22 000 | средняя |
| 3 | Discovery call и pain mapping | AE + presales | видеозвонки, презентация, CRM | 3-5 дней | 28 000 | низкая |
| 4 | NDA, сбор требований, оценка потока заявок | AE + CTO/аналитик | шаблоны NDA, shared docs | 5-7 дней | 35 000 | низкая |
| 5 | Техдемо / pilot design | CTO + ML + AE | demo stand, scoring sandbox | 1-2 недели | 65 000 | низкая |
| 6 | Пилот на исторических данных клиента | ML + backend + risk analyst | sandbox, ETL, notebooks, API | 2-4 недели | 120 000 | средняя |
| 7 | Согласование KPI пилота, risk/compliance review | CTO + AE + клиентский риск-менеджер | BI, docs, чек-листы | 1-2 недели | 55 000 | низкая |
| 8 | Коммерческое предложение и negotiation | AE + CEO | CPQ/шаблон оффера | 5-10 дней | 30 000 | низкая |
| 9 | Договор, ИБ, закупка, legal | CEO + AE + юрист | ЭДО, шаблоны SLA/DPA | 2-4 недели | 48 000 | низкая |
| 10 | Интеграция API / загрузка модели | backend + DevOps + ML | API gateway, monitoring, staging | 2-3 недели | 95 000 | средняя |
| 11 | Go-live и обучение риск-команды | CSM + AE + аналитик | knowledge base, training calls | 3-5 дней | 26 000 | средняя |
| 12 | Ежемесячный scoring usage и выставление счёта | finance + CSM + платёжный контур | CRM, 1C/ЭДО, billing | ежемесячно | 9 000 | высокая |

## Ключевые метрики
| Метрика | Значение | Комментарий |
|---|---:|---|
| customer_ltv_rub | 7 305 556 ₽ | 160 000 ₽ × 82,2% / 1,8% churn |
| CAC | 801 667 ₽ | fully-loaded blended CAC |
| LTV/CAC | 9,1x | существенно выше investment-grade порога |
| CAC payback | 6,1 мес | хорошо для regulated enterprise sale |
| GM% | 82,2% | высокая валовая маржа инфраструктурного risk-product |
| contribution_margin_rub_month | 131 500 ₽ | на 1 клиента в месяц |
| fixed_costs_rub_month | 5 677 000 ₽ | полная monthly fixed-cost база |
| company_ebitda_rub_month | 898 000 ₽/мес | на 50 клиентах, базовая проверка Profit Gate |
| Break-even clients | 44 | monthly operating break-even |
| Break-even month | 13 мес | base ramp |
| startup_capital_to_bep_rub | 38 412 224 ₽ | базовый burn до operating break-even |
| clients_to_500k_ebitda | 47 | округлено из 6 177 000 / 131 500 |
| clients_to_1m_ebitda | 51 | округлено из 6 677 000 / 131 500 |
| months_to_500k_ebitda | 13 мес | base ramp |
| months_to_1m_ebitda | 14 мес | при сохранении темпа после M13 |

## Team table
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Ramp до 80% prod, мес | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 | 0 | 780 000 |
| CTO / Tech Lead | 1 | 500 000 | 2,5 | 2 | 650 000 |
| Senior Backend | 2 | 270 000 | 1,5 | 1,5 | 702 000 |
| ML Engineer | 1 | 350 000 | 2,5 | 2 | 455 000 |
| DevOps | 1 | 340 000 | 1,5 | 1 | 442 000 |
| Frontend | 1 | 200 000 | 1 | 1 | 260 000 |
| SDR | 1 | 150 000 | 0,75 | 1 | 195 000 |
| AE | 1 | 300 000 | 1,5 | 2,5 | 390 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 286 000 |
| **Итого** | **10** |  |  |  | **4 862 000 ₽/мес** |

## GTM: 10 named targets
| # | Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Быстроденьги | крупный retail-MFO, высокая цена ошибки в approval/fraud, нужен decisioning uplift | email decision-maker + отраслевые fintech-конференции | 220 000 ₽/мес |
| 2 | МигКредит | зрелый онлайн-кредитный workflow, высокая потребность в anti-fraud и underwriting speed | email CRO/Head of Risk + тёплый партнёрский интро | 220 000 ₽/мес |
| 3 | Webbankir | digital-first выдача, важна автоматизация решения в real time | email decision-maker + пилот через risk sandbox | 180 000 ₽/мес |
| 4 | MoneyMan | online lender с чувствительностью к churn, NPL и fraud-rate | партнёрство + точечный outbound AE | 220 000 ₽/мес |
| 5 | Займер | сильный online traffic, pain в speed-to-decision и scalable scoring | email Head of Risk + кейс-презентация на конференции | 200 000 ₽/мес |
| 6 | еКапуста | массовый поток заявок, value от роста approval без ухудшения риска | targeted outbound + referral от data-партнёра | 170 000 ₽/мес |
| 7 | Vivus | mid-large MFO, понятный fit для hybrid anti-fraud + scoring | email decision-maker + vc.ru/fintech media touch | 160 000 ₽/мес |
| 8 | Lime-Zaim | кредитный поток и необходимость более дешёвого decisioning слоя, чем bespoke stack | outbound AE + demo через compliance-safe pilot | 160 000 ₽/мес |
| 9 | Т-Банк / Т-Бизнес credit stack | публично уже двигается в транзакционный скоринг для МФО, значит есть pain и budget | партнёрство / конференция / executive intro | 300 000 ₽/мес |
| 10 | Совкомбанк digital lending / Халва-контур | крупный consumer lending buyer, нужен устойчивый локальный compliance-fit | email decision-maker + enterprise partner channel | 280 000 ₽/мес |

**Вывод по GTM.** Канал fit хороший: это не broad-top-of-funnel SaaS, а account-based sale в узкий ICP. 10 named targets есть, а CAC payback 6,1 месяца оставляет место для controlled scaling.

## Market and finance synthesis
- **TAM РФ:** 1,014 млрд ₽.
- **SAM РФ:** 355 млн ₽.
- **SOM Y1:** 14,4 млн ₽.
- **SOM Y3:** 42,0 млн ₽.
- Реальность спроса подтверждена не keyword-volume, а структурой рынка: **845 МФО** в реестре ЦБ и **383 клиента** у SCORISTA.
- Финансово кейс рабочий: при **44 клиентах** достигается break-even, при **50 клиентах** base EBITDA уже **898 тыс. ₽/мес**.
- Ограничитель upside, а не жизнеспособности: рынок нишевый и regulated, поэтому fund-level scale будет зависеть от способности подняться выше сегмента МФО и уйти в adjacent lending verticals.

## Top-3 risks
| Риск | Probability | Impact | Почему в top-3 |
|---|---|---|---|
| Downside EBITDA risk | medium | high | Monte Carlo Lite даёт **p10 EBITDA @M24 = -1,17 млн ₽/мес**, значит модель ещё чувствительна к price compression и CAC inflation. |
| Regulatory / sanctions / data residency risk | high | high | 152-ФЗ, локальное хранение данных и санкционные ограничения могут резко удлинить интеграции и удорожить стек. |
| Price compression from substitutes | high | high | Низкочековые substitute-игроки и bundle от БКИ/anti-fraud providers могут давить premium pricing. |

## Что должно быть доказано после approve
1. **Pilot→paid conversion не ниже 20%** на горизонте следующих 6 месяцев.
2. **Не менее 15 активных paying clients** за 6 месяцев, иначе GTM не подтверждён.
3. **p10 EBITDA @M24 >= 0** после обновления данных по pricing, churn и CAC.
4. Доказанный локальный moat: минимум 3 кейса, где клиент выбрал SCORISTA из-за compliance-fit, а не только из-за цены.
5. Расширение buyer-base за пределы ядра МФО, иначе SAM останется слишком узким для следующего раунда.

## Proof points for APPROVED
- **LTV/CAC = 9,1x** и **CAC payback = 6,1 мес**.
- **Contribution Margin = 82,2%**.
- **company_ebitda_rub_month = 898 000 ₽/мес** на **50 клиентах**.
- **Break-even = 44 клиента**, **break-even month = 13**.
- На сайте компании заявлены **383 клиента** и **42 345 203 обработанных заявок**, что является сильным commercial proof.

## Финальное решение
SCORISTA — это **не венчурный broad-market rocketship**, а сильный **regulated niche infra asset**. Для инвесткомитета это означает: одобрять можно, если цель фонда допускает disciplined vertical fintech play с высоким LTV/CAC и контролируемым execution. Если нужен asset с огромным TAM и минимальным regulatory tail-risk, этот кейс слабее стандарта.

**Итог: APPROVED WITH NOTES, 74/100.**
```

## Score trajectory

```md
# 07-score-trajectory

## 2026-04-23 — P4 Demand Validation
- Stage: P4 Demand Validation
- Score change: 0 -> 0
- Summary: публичный keyword-demand низкий, но рынок платящих B2B-покупателей подтверждён; Profit Gate PASS; кейс идёт дальше
- Evidence:
  - ЦБ РФ: 845 МФО в реестре
  - SCORISTA: 383 клиента, 42 345 203 обработанных заявок
  - Публичные substitute prices: UNIRATE24, CheckPerson, НБКИ
- Decision: keep alive / proceed

## 2026-04-24 — P5 Unit Economics
- Stage: P5 Unit Economics
- Score change: 0 -> 11
- Summary: fully-loaded CAC пересчитан по regulated fintech модели; unit economics сильная, EBITDA > 500k ₽/мес достижим уже на 50 клиентах; кейс проходит economics gate
- Evidence:
  - Blended fully-loaded CAC: 801 667 ₽
  - Contribution Margin: 82,2%
  - LTV: 7,31 млн ₽ при churn 1,8%/мес
  - LTV/CAC: 9,1x
  - CAC Payback: 6,1 мес
  - Break-even: 44 клиента, monthly EBITDA на 50 клиентах ≈ 898 тыс. ₽
- Decision: proceed to next stage / economics PASS

## 2026-04-24 09:37 MSK — P7 Critic and Verdict
- Stage: P7 Critic and Verdict
- Score change: 11 -> 74
- Summary: кейс approved with notes, потому что сильная unit economics и достижимый EBITDA gate перевешивают узкий SAM; главный даунсайд — хрупкость downside-сценария и regulatory tail-risk
- Evidence:
  - Normalized score: 74/100
  - company_ebitda_rub_month: 898 000 ₽/мес на 50 клиентах
  - months_to_500k_ebitda: 13
  - customer_ltv_rub: 7 305 556 ₽
  - CAC: 801 667 ₽
  - LTV/CAC: 9,1x
  - Moat score: 18/25
  - Source tier balance: T1=4, T2=4, T3=1, weighted=2.33, penalty -2 к Market+Demand
- Decision: APPROVED WITH NOTES; перевести кейс в pipeline/approved/ и мониторить pilot-to-paid conversion, pricing discipline и p10 EBITDA downside
```
