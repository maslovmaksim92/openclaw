# Rogo Finance AI Analyst v2 — Full Verdict Package
> Скомпилированный пакет стадий пайплайна для публикации в GitHub.
> Примечание: в этом кейсе отсутствуют `02-validation.md` и `03-demand.md`; demand-стадия представлена файлом `02-demand.md` из фактического пайплайна.


---

## Файл: 01-intake.md

---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-rogo-finance-ai-analyst.md
created: 2026-04-21T14:16:00+03:00
---

# Intake

## Контекст resurrection
- Тип: принудительный полный пайплайн для повторной аналитики
- Исходный slug: rogo-finance-ai-analyst
- Основание: сигнал ранее не прошёл полный цикл или был маршрутизирован как duplicate/supporting, поэтому должен пройти заново через P3→P7
- Оригинальный triage/verdict: см. блок `Meta.source` внутри полного контекста ниже

## Полный контекст raw-файла

# RESURRECT SIGNAL — rogo-finance-ai-analyst

## Meta
- source: triage/triage-2026-04-14-rogo-finance-ai-analyst.md
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
- pipeline/raw/raw-2026-04-14-rogo-finance-ai-analyst.md

## Классификация
новый сигнал, отклонён на этапе triage

## Решение
Не создавать новый кейс.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: сигнал относится к вертикали investment banking / private equity / corporate finance, а текущие активные кейсы покрывают другие ниши.
- По самому raw-файлу первичная экономика ниже обязательного порога: указан `ltv_signal: 1200000-5000000 RUB в год с клиента`, то есть примерно 100 000-416 000 руб/мес, что ниже LTV Gate `> 500 000 руб/мес`.
- Сигнал выглядит содержательным и интересным как GEO-EXPAND идея, но на текущих данных не подтверждает достаточно высокий чек для запуска кейса в этом пайплайне.
- Без подтверждения более дорогого enterprise-контракта, on-prem контура или повторяемого multi-team deployment создание кейса будет преждевременным.

## Итог
Сигнал обработан и отклонён на этапе triage по причине недостаточного подтверждённого LTV. Raw-файл должен быть перемещён в `pipeline/raw/processed/`, новый кейс не создан.
```



---

## Файл: 02-demand.md

---
stage: demand-validation
case: rogo-finance-ai-analyst-v2
date: 2026-04-22
analyst: branch-models-lead
sector: FINTECH
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Rogo, AI-аналитик для investment banking, private equity и корпоративных финансов.

## Итог
**Статус: CONDITIONAL PASS.**

Прямой поисковый спрос в РФ по формулировкам категории остаётся низким, но для такого продукта это не критичный минус: покупка идёт не через массовый SEO-спрос, а через enterprise GTM, доверие, secure deployment и экономию дорогих analyst-hours. Глобальные сигналы у Rogo уже сильные: по состоянию на **28 января 2026 года** компания официально объявила о **$75 млн Series C**, суммарном финансировании **свыше $165 млн**, **25 000+ финансовых профессионалов, использующих Rogo ежедневно**, и запуске первого международного офиса в Лондоне. OpenAI отдельно пишет, что после выхода из stealth в 2024 году Rogo уже обслуживала **5 000+ банкиров**, экономила **10+ часов в неделю** и выросла по ARR в **27 раз**.

Это не доказывает большой массовый рынок в РФ, но хорошо подтверждает, что категория реально продаётся в дорогой finance workflow. Для локального контура кейс выглядит как узкий high-ticket FINTECH thesis, а не как широкая SaaS-категория.

## 1. Demand data
Источник exact-check: `http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20ai`

- `investment banking ai` → **LOW**, score **3**, Google Trends RU **1**, HH vacancies **11**, Yandex suggest **2**.
- `finance ai analyst` → **LOW**, score **0**, Google Trends RU **0**, HH vacancies **7**, Yandex suggest **2**.
- `AI for investment banking` → **LOW**, score **0**, Google Trends RU **0**, HH vacancies **0**, Yandex suggest **2**.
- `financial research platform` → **LOW**, score **0**, Google Trends RU **0**, HH vacancies **2**, Yandex suggest **2**.

### Интерпретация
- Exact-demand в РФ слабый.
- Но это ожидаемо для enterprise-продукта, который продаётся в десятки дорогих команд, а не в широкий self-serve рынок.
- Значит, low search demand сам по себе не даёт early reject, если есть сильный global category proof и правдоподобный путь к high-LTV контракту.

## 2. Реальные рыночные сигналы и why now
1. **Rogo** на официальной странице **Series C** и в анонсе от **28 января 2026 года** сообщает о **$75 млн Series C** и total funding **$165M+**. Это сильный сигнал доверия к категории со стороны Tier-1 инвесторов. [T1]
2. В том же анонсе Rogo пишет о **25 000+ финансовых профессионалов, использующих платформу ежедневно**, и о клиентах уровня **Rothschild & Co, Jefferies, Lazard**. Это уже не ранний пилот, а подтверждённый enterprise adoption signal. [T1]
3. Rogo также объявила открытие офиса в **Лондоне** для ускорения европейской экспансии. Это важно именно для GEO-EXPAND / finance workflow логики: продукт мыслит себя как международную инфраструктуру, а не локальный point solution. [T1]
4. **OpenAI** в кейсе про Rogo пишет, что компания после выхода из stealth в 2024 году уже работала с **5 000+ bankers**, экономила **10+ часов в неделю** и увеличила **ARR в 27 раз**. Это не независимый аудит, но всё же сильный первичный operating signal. [T1]
5. На официальном сайте Rogo прямо описывает outputs, за которые finance buyer реально платит: **auditable Excel models, investment memos, diligence materials, slide decks**. Это хороший indicator, что продукт встроен в core workflow, а не в факультативный AI-эксперимент. [T1]
6. По данным **AK&M**, рынок M&A с российскими активами за **2025 год** составил **399 сделок** на **$41,12 млрд**. Это ниже 2024 года, но сам рынок сделок остаётся достаточно крупным, чтобы поддерживать спрос на инструменты ускорения анализа, diligence и подготовки материалов в верхнем сегменте. [T1]

## 3. Что именно здесь покупают
Покупают не "AI-аналитика" как красивый ярлык, а конкретные результаты:
- быстрее разобрать data room и материалы по сделке;
- быстрее собрать market map и comparable companies;
- подготовить memo, deck и Excel-модель под стандарт институционального клиента;
- сократить время дорогих аналитиков и ассоциатов;
- уменьшить риск ручных ошибок и ускорить turnaround по сделкам.

Именно поэтому реальный substitute здесь не поиск в Яндексе, а сочетание:
- analyst team,
- Excel + PowerPoint,
- Bloomberg / FactSet / S&P / локальные базы,
- внутренние шаблоны,
- внешние advisory и research команды.

## 4. TAM / SAM / SOM в РФ

### Базовые допущения
- Беру **450 000 ₽/мес** или **5,4 млн ₽/год** как base-case контракт на одну команду с high-touch onboarding, безопасным развёртыванием и поддержкой.
- ICP: крупные investment banking и advisory команды, PE/VC / growth equity, corpdev крупных групп, special situations, research-heavy finance teams.
- Это не массовый продукт, а узкий enterprise workflow layer.

### TAM
Беру **120** релевантных организаций в РФ и русскоязычном контуре, где вообще может существовать такой pain.

**TAM = 120 × 5 400 000 ₽ = 648 млн ₽/год**

### SAM
Реально адресуемый слой, где есть бюджеты, data maturity и интенсивный сделочный / research workflow.

Беру **30** организаций.

**SAM = 30 × 5 400 000 ₽ = 162 млн ₽/год**

### SOM
Ранний реалистичный слой: **5 контрактов**.

**SOM = 5 × 5 400 000 ₽ = 27 млн ₽/год**

### Вывод по рынку
Рынок узкий, но не нулевой. Для standalone large-scale SaaS это слабая история, но для нишевого high-ticket FINTECH / AI-services motion рынок выглядит достаточным, если удаётся держать enterprise pricing.

## 5. WTP и доказательства готовности платить
1. Цена часа аналитика и associate в IB / PE / corpfin workflows высока, особенно в контексте сделок и клиентских материалов.
2. OpenAI указывает на экономию **10+ часов в неделю**, что делает premium pricing правдоподобным. [T1]
3. Rogo продаёт outputs, которые напрямую встроены в revenue-generating finance workflows, а не в периферийную productivity-категорию. [T1]
4. Официальный messaging у Rogo явно enterprise-first: bespoke deployment, security, white-glove partnership. Это хороший косвенный сигнал, что продукт уже продаётся не по низкому seat price. [T1]

### Вывод по WTP
**WTP глобально подтверждён.**

Для РФ willingness-to-pay вероятен у ограниченного числа top-tier покупателей, если продукт даёт measurable speedup и не ломается на локальных источниках, форматах документов и security-требованиях.

## 6. Profit Gate
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

**Вердикт: BORDERLINE PASS**

### Сценарий C. Enterprise secure deployment
- Цена: **700 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **455 000 ₽/мес**
- Нужно **6 клиентов**

**Вердикт: PASS**

### Вывод по Profit Gate
Кейс проходит profit gate только в дорогом enterprise-сценарии. Если чек сползает к обычному copilot-level SaaS, локальный рынок становится слишком узким.

## 7. Основные риски
1. **Слишком маленький локальный SAM**: покупателей мало, и ошибка по ICP дорого стоит.
2. **Deployment burden**: secure rollout, интеграции и white-glove support могут съесть маржу.
3. **Substitute risk**: часть value уже покрывается analyst team + терминалы + research stack.
4. **Localization risk**: продукту может понадобиться заметная адаптация под локальные data sources и процессные требования.

## 8. Решение для pipeline
**Не отклонять на этапе demand validation.**

Кейс стоит двигать дальше в P4/P5, потому что:
1. глобальный спрос на категорию уже подтверждён;
2. продукт встроен в дорогой и частотный workflow;
3. есть правдоподобный путь к high-LTV контрактам;
4. главный вопрос дальше уже не "есть ли боль", а "можно ли собрать economics и moat в локальном контуре".

На следующих этапах нужно жёстко проверить:
- реально ли держать recurring-чек хотя бы **450–700 тыс. ₽/мес**;
- насколько тяжёлые security и data integrations;
- не превращается ли модель в дорогой аналитический консалтинг;
- можно ли расширить ICP за пределы чистого investment banking в corpdev, PE, strategy и buyside research.

## Источники
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20ai [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=finance%20ai%20analyst [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20for%20investment%20banking [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=financial%20research%20platform [T2]
- Rogo Series C: https://rogo.ai/series-c [T1]
- Rogo, Series C and European expansion, 2026-01-28: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion [T1]
- OpenAI, Rogo scales AI-driven financial research with OpenAI o1: https://openai.com/index/rogo/ [T1]
- AK&M, итоги рынка M&A с российскими активами за 2025 год, 2026-02-12: https://www.akm.ru/news/ak_m_vypustilo_itogi_rynka_m_a_s_rossiyskimi_aktivami_za_2025_god/?sphrase_id=455401 [T1]

Sources: T1=4, T2=4, T3=0. Primary evidence basis: T1.

## Market Pulse
Market Pulse 2026-04-22: глобальный спрос на AI для high-finance workflow уже подтверждён, а в РФ это выглядит как узкий премиальный сегмент, а не массовая категория.

> Market Pulse 2026-04-22: растущий интерес.
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-10: растущий интерес.

> Market Pulse 2026-05-11: зафиксирован рост интереса, по текущему веб-поиску и публикациям динамика выглядит растущей.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


---

## Файл: 04-economics.md

---
stage: economics
case: rogo-finance-ai-analyst-v2
date: 2026-05-11
analyst: branch-models-lead
sector: FINTECH
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Rogo, AI-аналитик для investment banking, private equity и корпоративных финансов.

## Итог
**Статус: PASS.**

Base-case экономика для investment-grade фонда складывается только как **enterprise AI workflow** с чеком **700 000 ₽/клиент/мес**, gross margin около **61,4%**, monthly churn **1,5%** и fully-loaded blended CAC около **1,75 млн ₽**. При этих вводных:

- **LTV = 28,65 млн ₽**
- **LTV/CAC = 16,4x**
- **CAC Payback = 2,5 мес** по формуле CAC / MRR
- **Contribution Margin = 58,6%**
- **Break-even = 15 клиентов**

Кейс инвестиционно приемлем **только** в дорогом enterprise-сегменте с secure deployment, длинным sales cycle и white-glove onboarding. Если средний чек сползает к 300-450 тыс. ₽/мес, экономика резко слабеет.

## 1. Модель и ключевые допущения

### Base-case pricing
- MRR на клиента: **700 000 ₽/мес**
- Годовой контракт: **8,4 млн ₽/год**
- Тип сделки: enterprise / regulated finance workflow
- Sales cycle: **4-6 месяцев**
- Валюта модели: **₽**

### Почему беру именно этот сценарий
Из demand-этапа уже видно, что кейс проходит только как дорогой enterprise workflow для небольшого числа команд. OpenAI указывает, что Rogo экономит **10+ часов в неделю** на пользователя, а сама компания уже используется **25 000+ финансовых профессионалов ежедневно** и продаётся в топовые finance teams. Это поддерживает high-ticket deployment model, а не self-serve SaaS. [S1][S2]

## 2. Business process table, от лида до оплаты

### Воронка и операционный процесс на 1 выигранного клиента
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Target account selection | Founder + SDR | CRM, ручной account mapping | 6 ч | 12 000 | Низкая |
| 2 | Холодный outreach / warm intro | SDR | CRM, email, мессенджеры | 18 ч | 36 000 | Средняя |
| 3 | Discovery call | Founder/AE | Zoom/Meet, CRM | 2 ч | 18 000 | Низкая |
| 4 | Demo на finance use-case | AE + Solutions/CTO | Demo env, shared deck | 4 ч | 42 000 | Низкая |
| 5 | Security / IT review | CTO + DevOps | VPC docs, security docs | 10 ч | 78 000 | Низкая |
| 6 | Pilot scoping | AE + CTO + PM/founder | SOW, pilot plan | 6 ч | 54 000 | Низкая |
| 7 | Pilot setup | Backend + ML + DevOps | Private cloud, connectors | 28 ч | 168 000 | Средняя |
| 8 | Pilot support and iteration | ML + CS + AE | Slack/Telegram, issue tracker | 30 ч | 165 000 | Средняя |
| 9 | Procurement / legal / info-sec | Founder + AE + legal | MSA/DPA, procurement docs | 12 ч | 96 000 | Низкая |
| 10 | Commercial negotiation | Founder + AE | Pricing model, ROI memo | 4 ч | 42 000 | Низкая |
| 11 | Contract signing | Founder + legal | E-sign / paperflow | 3 ч | 24 000 | Средняя |
| 12 | Invoice + payment collection | Finance ops | 1C/банк/ЭДО | 2 ч | 9 000 | Высокая |

### Вывод по процессу
- Продажа неавтоматизируемая, с большим количеством ручных касаний.
- Узкое место экономики не в рекламе, а в **pre-sales / pilot / security review**.
- Поэтому сегмент должен считаться как **regulated enterprise** и CAC надо считать с multiplier **выше self-serve**.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/API inference | 90 000 | большой объём research, summarization, document drafting |
| Cloud/VPC/compute/storage | 45 000 | выделенный secure контур, storage, monitoring |
| Data ingestion и коннекторы | 35 000 | ETL, parsing data room, connectors |
| Onboarding / implementation amortized | 55 000 | стартовые работы 330 000 ₽, амортизация на 6 мес |
| Customer Success / support | 25 000 | high-touch support на портфель клиентов |
| Security/compliance support | 20 000 | поддержка infosec, audit trail, access control |
| **Итого COGS** | **270 000** |  |

### Gross Margin
- Revenue per client/month = **700 000 ₽**
- COGS per client/month = **270 000 ₽**
- Gross Profit = **430 000 ₽**
- **Gross Margin = 61,4%**

Для enterprise AI в regulated finance это адекватно: выше, чем у сервиса, но ниже классического pure-play SaaS из-за пилотов, secure deployment и integration burden.

## 4. CAC by acquisition channel с funnel conversion

### Канальные воронки
| Канал | Lead -> Meeting | Meeting -> Pilot | Pilot -> Paid | Итоговая конверсия lead -> paid | Новых клиентов/мес | Комментарий |
|---|---:|---:|---:|---:|---:|---|
| Founder-led outbound / warm intros | 12% | 35% | 30% | 1,26% | 1,0 | Основной канал для дорогих finance deals |
| Partnerships / advisory / SI | 20% | 40% | 35% | 2,80% | 0,5 | Меньше объём, выше trust |
| Paid ABM / events | 4% | 20% | 20% | 0,16% | 0,2 | Поддерживающий канал, не основной |

### Fully-loaded CAC, по обязательной формуле
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier overhead) / New paying customers**

#### Разложение blended CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / ABM) | 180 000 | тестовый account-based demand capture | internal model |
| Outbound team FOT (SDR + AE attributed to new) | 877 500 | SDR 180 000 + AE 495 000 fully-loaded; 130% attribution в acquisition нельзя, беру 100%: (180 000×1,3)+(380 000×1,3) | HH.ru benchmark [S4][S5] |
| Marketing team FOT (partial allocation) | 195 000 | founder/PMM equivalent 300 000 gross × 50% × 1,3 | HH.ru benchmark [S6] |
| Tools (CRM, prospecting, enrichment, calling) | 95 000 | CRM + enrichment + email infra + call tooling | vendor benchmark / internal model |
| Events / partnerships | 250 000 | small roundtables, partner commissions, private events | internal model |
| Overhead multiplier (x1,3) | 478 650 | 30% на базу 1 597 500 ₽ | enterprise B2B standard |
| **Итого месячный acquisition spend** | **2 076 150** |  |  |

### Blended CAC
- New paying customers/month: **1,19**
- **Blended fully-loaded CAC = 2 076 150 / 1,19 = 1 744 664 ₽**, округляю до **1,75 млн ₽**

### CAC по каналам
| Канал | CAC, ₽ | Как считалось |
|---|---:|---|
| Founder-led outbound / warm intros | 1 100 000 | меньше media, но дорогой founder/AE time и pilot burden |
| Partnerships / advisory / SI | 1 450 000 | выше revenue share / partner cost, зато выше conversion |
| Paid ABM / events | 3 200 000 | низкая конверсия на узком enterprise ICP |
| **Blended CAC** | **1 750 000** | weighted average |

### Sanity check против бенчмарка
Для regulated / high-finance enterprise user задал sanity-band **200-700K ₽** для fintech B2B и **400-1200K ₽** для healthtech B2B, но для этого кейса есть дополнительная enterprise complexity: security review, pilot, procurement и legal. Поэтому blended CAC **1,75 млн ₽** выглядит выше общего fintech SaaS band, но логичен для very narrow high-ticket workflow и не является подозрительно заниженным.

## 5. LTV с churn rate

### Churn benchmark
Optifi показывает, что для **enterprise SaaS** типичный monthly logo churn находится около **1-2% в месяц**. Для base-case беру **1,5% monthly churn** как середину диапазона. [S3]

### Расчёт
- MRR = **700 000 ₽**
- Gross Margin = **61,4%**
- Monthly churn = **1,5%**
- Gross profit per client/month = **430 000 ₽**

**LTV = Gross Profit / Monthly Churn = 430 000 / 0,015 = 28 666 667 ₽**

Округляю до **28,65 млн ₽**.

## 6. LTV/CAC ratio
- LTV = **28,65 млн ₽**
- Blended CAC = **1,75 млн ₽**
- **LTV/CAC = 16,4x**

### Вывод
Порог investment grade **>= 3:1** уверенно выполняется. Но это справедливо только если:
1. удерживается enterprise-чек около **700 тыс. ₽/мес**,
2. churn действительно не уходит выше **3%/мес**,
3. модель не расползается в тяжелый кастомный консалтинг.

## 7. CAC Payback
По обязательной sanity-формуле:

**CAC Payback = CAC / MRR = 1 750 000 / 700 000 = 2,5 месяца**

Даже если считать через gross profit, payback будет **4,1 месяца**. Оба значения лучше предельных **12 мес** и **18 мес** для enterprise.

## 8. Contribution Margin %
Для вклада в покрытие fixed costs считаю так:

- Revenue = **700 000 ₽**
- COGS = **270 000 ₽**
- Variable payment/admin costs = **20 000 ₽**
- Contribution per client/month = **410 000 ₽**

**Contribution Margin % = 410 000 / 700 000 = 58,6%**

## 9. Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, fundraising, partnerships | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security review, product delivery | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | ingestion, backend, integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | workflow engine, infra integration | 420 000 | 126 000 | 546 000 |
| ML Engineer | retrieval, evals, model orchestration | 500 000 | 150 000 | 650 000 |
| DevOps | VPC, observability, deployment | 350 000 | 105 000 | 455 000 |
| Frontend | analyst workspace UI | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting | 180 000 | 54 000 | 234 000 |
| AE | demos, pilot conversion, procurement | 380 000 | 114 000 | 494 000 |
| Customer Success | onboarding, adoption, renewals | 260 000 | 78 000 | 338 000 |
| **Итого** |  |  |  | **5 213 000** |

### Таблица найма, как требовалось
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 + бонус | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 380 000 + комиссия | 1-2 | 2-3 | 114 000 | 494 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |

### Hiring realism
- В **M1** нет нереалистичного набора 5+ человек.
- Самые дефицитные роли, которые удлиняют план: **CTO/Tech Lead, ML Engineer, AE enterprise**.
- Полноценная enterprise GTM и secure delivery реально раскрываются только к **M6-M8**.

## 10. Cumulative FOT timeline M1-M12

### План подключения людей
- M1: Founder
- M2: SDR, Frontend
- M3: Backend #1
- M4: CTO, DevOps
- M5: Backend #2, AE
- M6: ML Engineer
- M8: Customer Success

### FOT timeline
| Месяц | Кто в штате | Monthly FOT, ₽ |
|---|---|---:|
| M1 | Founder | 845 000 |
| M2 | Founder, SDR, Frontend | 1 469 000 |
| M3 | + Backend #1 | 2 015 000 |
| M4 | + CTO, DevOps | 3 185 000 |
| M5 | + Backend #2, AE | 4 225 000 |
| M6 | + ML Engineer | 4 875 000 |
| M7 | тот же состав | 4 875 000 |
| M8 | + Customer Success | 5 213 000 |
| M9 | тот же состав | 5 213 000 |
| M10 | тот же состав | 5 213 000 |
| M11 | тот же состав | 5 213 000 |
| M12 | тот же состав | 5 213 000 |

## 11. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 213 000 | по таблице выше |
| Office / coworking / admin | 180 000 | гибридный формат |
| Legal / бухгалтерия / audit readiness | 120 000 | договоры, privacy, procurement |
| Core software stack | 140 000 | Jira, Slack, Notion, Git, monitoring |
| Founder travel / meetings | 100 000 | enterprise sales motion |
| Misc reserve | 80 000 | непредвиденные расходы |
| **Итого fixed costs** | **5 833 000** |  |

## 12. Break-even, по клиентам и по месяцам

### Break-even по количеству клиентов
- Contribution per client/month = **410 000 ₽**
- Fixed costs/month = **5 833 000 ₽**

**Break-even clients = 5 833 000 / 410 000 = 14,2**

Округляю до **15 клиентов**.

### Break-even по месяцам
Планирую ramp новых клиентов так:
- M3: 1
- M5: 2
- M6: 3
- M7: 4
- M8: 6
- M9: 8
- M10: 10
- M11: 13
- M12: 15

| Месяц | Клиентов активных | Contribution, ₽ | Fixed costs, ₽ | EBITDA before tax, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 465 000 | -1 465 000 |
| M2 | 0 | 0 | 2 089 000 | -2 089 000 |
| M3 | 1 | 410 000 | 2 635 000 | -2 225 000 |
| M4 | 1 | 410 000 | 3 805 000 | -3 395 000 |
| M5 | 2 | 820 000 | 4 845 000 | -4 025 000 |
| M6 | 3 | 1 230 000 | 5 495 000 | -4 265 000 |
| M7 | 4 | 1 640 000 | 5 495 000 | -3 855 000 |
| M8 | 6 | 2 460 000 | 5 833 000 | -3 373 000 |
| M9 | 8 | 3 280 000 | 5 833 000 | -2 553 000 |
| M10 | 10 | 4 100 000 | 5 833 000 | -1 733 000 |
| M11 | 13 | 5 330 000 | 5 833 000 | -503 000 |
| M12 | 15 | 6 150 000 | 5 833 000 | **317 000** |

### Вывод
Операционный break-even достигается примерно на **M12** и требует **15 активных enterprise-клиентов**.

## 13. Burn-to-breakeven
Кумулятивный burn до операционного break-even:

- M1-M11 cumulative EBITDA = **-29 481 000 ₽**
- Для safety reserve на collection lag, delayed procurements и более длинные пилоты нужен запас минимум **+25%**

**Burn-to-breakeven ≈ 36,9 млн ₽**

Это уже выглядит как реальный масштаб для узкого enterprise B2B AI, а не как «дёшево соберём на коленке».

## 14. Cash runway
Берём **startup_capital = 60 млн ₽**.

- Burn-to-breakeven = **36,9 млн ₽**
- Остаток после выхода на break-even ≈ **23,1 млн ₽**
- Средний burn на участке M1-M11 ≈ **2,68 млн ₽/мес**
- Peak burn ≈ **4,27 млн ₽/мес**

### Вывод по runway
- При капитале **60 млн ₽** runway выглядит как **14-18 месяцев**, в зависимости от скорости пилотов и collection cycle.
- При капитале **< 40 млн ₽** проект становится напряжённым.
- Для enterprise B2B AI это не red flag, а скорее ожидаемая капиталоёмкость.

## 15. Profit Gate
### Проверка обязательных порогов
1. **EBITDA >= 500K/mo achievable even at 50 clients?** Да. При 50 клиентах contribution = **20,5 млн ₽/мес**, что многократно перекрывает fixed cost base.
2. **LTV/CAC >= 1:1?** Да. **16,4x**.
3. **Investment-grade threshold LTV/CAC >= 3:1?** Да.

### Итог по gate
**Profit Gate: PASS.**

Но pass держится на трёх жёстких условиях:
- средний чек **не ниже 700 тыс. ₽/мес**,
- churn **не выше 1,5-2,0%/мес**,
- delivery не превращается в полу-консалтинг с распухшим implementation COGS.

## 16. Sensitivity

| Сценарий | MRR, ₽ | GM | Churn / мес | LTV, ₽ | CAC, ₽ | LTV/CAC | Вывод |
|---|---:|---:|---:|---:|---:|---:|---|
| Bear | 450 000 | 55% | 3,0% | 8 250 000 | 1 900 000 | 4,3x | ещё живо, но запас тоньше |
| Base | 700 000 | 61,4% | 1,5% | 28 650 000 | 1 750 000 | 16,4x | PASS |
| Bull | 900 000 | 65% | 1,0% | 58 500 000 | 1 800 000 | 32,5x | сильный enterprise outcome |

## 17. Главные риски экономики
1. **Слишком узкий ICP**. Клиентов немного, ошибка в positioning дорого стоит.
2. **Security/procurement drag**. Enterprise win-rate может оказаться ниже модели.
3. **Custom work creep**. Если каждый пилот уникален, COGS и pre-sales time вырастут.
4. **Data-source localization**. Нужны локальные и закрытые источники данных, иначе retention просядет.
5. **Founder dependency**. Ранняя выручка почти наверняка завязана на founder-led selling.

## 18. Вывод
Rogo-like кейс в РФ и русскоязычном контуре не выглядит массовым SaaS, но как **дорогой enterprise AI layer для finance teams** unit economics могут работать. Для фонда это **не объёмная категория**, а **узкий high-ticket thesis**: инвестировать можно только если команда реально подтверждает secure deployment motion, pilot-to-paid discipline и чек не ниже **700 тыс. ₽/мес**.

## Источники
- [S1] Rogo Series C and European expansion: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion
- [S2] OpenAI x Rogo case study: https://openai.com/index/rogo/
- [S3] Optifi, SaaS churn benchmarks: https://www.optifi.ai/post/saas-churn-benchmarks
- [S4] HH.ru, SDR вакансии Москва: https://hh.ru/search/vacancy?text=SDR
- [S5] HH.ru, Account Executive вакансии Москва: https://hh.ru/search/vacancy?text=account%20executive
- [S6] HH.ru, Product Marketing / Product Manager вакансии Москва: https://hh.ru/search/vacancy?text=product%20marketing%20manager
- [S7] HH.ru, CTO / Tech Lead вакансии Москва: https://hh.ru/search/vacancy?text=cto
- [S8] HH.ru, Senior Backend вакансии Москва: https://hh.ru/search/vacancy?text=senior%20backend
- [S9] HH.ru, ML Engineer вакансии Москва: https://hh.ru/search/vacancy?text=ml%20engineer
- [S10] HH.ru, DevOps вакансии Москва: https://hh.ru/search/vacancy?text=devops
- [S11] HH.ru, Frontend вакансии Москва: https://hh.ru/search/vacancy?text=frontend
- [S12] HH.ru, Customer Success вакансии Москва: https://hh.ru/search/vacancy?text=customer%20success


---

## Файл: 05-critic.md

# SECTION A — PnL

Допущения взяты из 04-economics.md. Fixed costs приняты на полном плато 5 833 000 ₽/мес для сравнимости сценариев. Налог для base/optimistic: IT-льгота 3% по выручке при аккредитации Минцифры; fallback: УСН 6%; для ОСНО учитывать налог на прибыль 20% и НДС 20% если применимо.

## Пессимистичный сценарий

Параметры: ARPA 450 000 ₽/мес, COGS/client 202 500 ₽/мес, contribution_margin_rub_month 227 500 ₽/клиент/мес, churn 3.0%, CAC 1 900 000 ₽.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 1 |
| Total clients | 0.0 | 0.0 | 1.0 | 1.0 | 1.9 | 2.9 | 3.8 | 4.7 | 5.5 | 6.4 | 8.2 | 8.9 |
| MRR, ₽ | 0 | 0 | 450 000 | 436 500 | 873 405 | 1 297 203 | 1 708 287 | 2 107 038 | 2 493 827 | 2 869 012 | 3 682 942 | 4 022 454 |
| COGS, ₽ | 0 | 0 | 202 500 | 196 425 | 393 032 | 583 741 | 768 729 | 948 167 | 1 122 222 | 1 291 055 | 1 657 324 | 1 810 104 |
| Gross profit, ₽ | 0 | 0 | 247 500 | 240 075 | 480 373 | 713 462 | 939 558 | 1 158 871 | 1 371 605 | 1 577 957 | 2 025 618 | 2 212 349 |
| GM%, % | 0.0% | 0.0% | 55.0% | 55.0% | 55.0% | 55.0% | 55.0% | 55.0% | 55.0% | 55.0% | 55.0% | 55.0% |
| Fixed costs, ₽ | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 |
| EBITDA, ₽ | -5 833 000 | -5 833 000 | -5 585 500 | -5 592 925 | -5 352 627 | -5 119 538 | -4 893 442 | -4 674 129 | -4 461 395 | -4 255 043 | -3 807 382 | -3 620 651 |
| Cash burn, ₽ | 5 833 000 | 5 833 000 | 5 585 500 | 5 592 925 | 5 352 627 | 5 119 538 | 4 893 442 | 4 674 129 | 4 461 395 | 4 255 043 | 3 807 382 | 3 620 651 |
| Cumulative cash, ₽ | -5 833 000 | -11 666 000 | -17 251 500 | -22 844 425 | -28 197 052 | -33 316 591 | -38 210 033 | -42 884 162 | -47 345 557 | -51 600 600 | -55 407 982 | -59 028 633 |

**Waterfall на 1 клиента / месяц**

| Шаг | ₽ |
|---|---:|
| ARPA | 450 000 |
| Gross profit | 247 500 |
| Contribution | 227 500 |
| EBITDA before tax | 227 500 |
| Net after УСН 6% | 200 500 |
| Net after IT-льгота 3% | 214 000 |
| Net after ОСНО 20%* | 182 000 |

* Для ОСНО показан только налог на прибыль 20% от EBITDA; НДС 20% считать отдельно, если price card quoted gross-of-VAT.

**Cash flow**: startup_capital_to_bep_rub = 59 028 633 ₽.

**Налоговая модель**

- База для расчёта: выручка на клиента 450 000 ₽/мес.
- УСН: 6% от выручки = 27 000 ₽/клиент/мес.
- IT-льгота: 3% от выручки = 13 500 ₽/клиент/мес при аккредитации Минцифры.
- Страховые взносы: ~30% к ФОТ уже заложены в team FOT/fixed costs.
- НДС 20%: применять только при ОСНО; в модели PnL выше выручка показана net для операционной сопоставимости.

**Break-even**: 26 клиентов; по месяцам: в пределах M1-M12 не достигнут.

## Базовый сценарий

Параметры: ARPA 700 000 ₽/мес, COGS/client 270 000 ₽/мес, contribution_margin_rub_month 410 000 ₽/клиент/мес, churn 1.5%, CAC 1 750 000 ₽.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 2 |
| Total clients | 0.0 | 0.0 | 1.0 | 1.0 | 2.0 | 2.9 | 3.9 | 5.8 | 7.8 | 9.6 | 12.5 | 14.3 |
| MRR, ₽ | 0 | 0 | 700 000 | 689 500 | 1 379 158 | 2 058 470 | 2 727 593 | 4 086 679 | 5 425 379 | 6 743 998 | 8 742 838 | 10 011 696 |
| COGS, ₽ | 0 | 0 | 270 000 | 265 950 | 531 961 | 793 981 | 1 052 072 | 1 576 291 | 2 092 646 | 2 601 256 | 3 372 238 | 3 861 654 |
| Gross profit, ₽ | 0 | 0 | 430 000 | 423 550 | 847 197 | 1 264 489 | 1 675 521 | 2 510 389 | 3 332 733 | 4 142 742 | 5 370 601 | 6 150 042 |
| GM%, % | 0.0% | 0.0% | 61.4% | 61.4% | 61.4% | 61.4% | 61.4% | 61.4% | 61.4% | 61.4% | 61.4% | 61.4% |
| Fixed costs, ₽ | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 |
| EBITDA, ₽ | -5 833 000 | -5 833 000 | -5 403 000 | -5 409 450 | -4 985 803 | -4 568 511 | -4 157 479 | -3 322 611 | -2 500 267 | -1 690 258 | -462 399 | 317 042 |
| Cash burn, ₽ | 5 833 000 | 5 833 000 | 5 403 000 | 5 409 450 | 4 985 803 | 4 568 511 | 4 157 479 | 3 322 611 | 2 500 267 | 1 690 258 | 462 399 | 0 |
| Cumulative cash, ₽ | -5 833 000 | -11 666 000 | -17 069 000 | -22 478 450 | -27 464 253 | -32 032 764 | -36 190 243 | -39 512 854 | -42 013 122 | -43 703 380 | -44 165 779 | -44 165 779 |

**Waterfall на 1 клиента / месяц**

| Шаг | ₽ |
|---|---:|
| ARPA | 700 000 |
| Gross profit | 430 000 |
| Contribution | 410 000 |
| EBITDA before tax | 410 000 |
| Net after УСН 6% | 368 000 |
| Net after IT-льгота 3% | 389 000 |
| Net after ОСНО 20%* | 328 000 |

* Для ОСНО показан только налог на прибыль 20% от EBITDA; НДС 20% считать отдельно, если price card quoted gross-of-VAT.

**Cash flow**: startup_capital_to_bep_rub = 44 165 779 ₽.

**Налоговая модель**

- База для расчёта: выручка на клиента 700 000 ₽/мес.
- УСН: 6% от выручки = 42 000 ₽/клиент/мес.
- IT-льгота: 3% от выручки = 21 000 ₽/клиент/мес при аккредитации Минцифры.
- Страховые взносы: ~30% к ФОТ уже заложены в team FOT/fixed costs.
- НДС 20%: применять только при ОСНО; в модели PnL выше выручка показана net для операционной сопоставимости.

**Break-even**: 15 клиентов; по месяцам: M12.

## Оптимистичный сценарий

Параметры: ARPA 900 000 ₽/мес, COGS/client 315 000 ₽/мес, contribution_margin_rub_month 565 000 ₽/клиент/мес, churn 1.0%, CAC 1 800 000 ₽.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 3 |
| Total clients | 0.0 | 1.0 | 2.0 | 3.0 | 4.9 | 6.9 | 8.8 | 11.7 | 14.6 | 17.5 | 21.3 | 24.1 |
| MRR, ₽ | 0 | 900 000 | 1 791 000 | 2 673 090 | 4 446 359 | 6 201 896 | 7 939 877 | 10 560 478 | 13 154 873 | 15 723 324 | 19 166 091 | 21 674 430 |
| COGS, ₽ | 0 | 315 000 | 626 850 | 935 582 | 1 556 226 | 2 170 663 | 2 778 957 | 3 696 167 | 4 604 206 | 5 503 163 | 6 708 132 | 7 586 051 |
| Gross profit, ₽ | 0 | 585 000 | 1 164 150 | 1 737 508 | 2 890 133 | 4 031 232 | 5 160 920 | 6 864 311 | 8 550 667 | 10 220 161 | 12 457 959 | 14 088 380 |
| GM%, % | 0.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% | 65.0% |
| Fixed costs, ₽ | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 | 5 833 000 |
| EBITDA, ₽ | -5 833 000 | -5 248 000 | -4 668 850 | -4 095 492 | -2 942 867 | -1 801 768 | -672 080 | 1 031 311 | 2 717 667 | 4 387 161 | 6 624 959 | 8 255 380 |
| Cash burn, ₽ | 5 833 000 | 5 248 000 | 4 668 850 | 4 095 492 | 2 942 867 | 1 801 768 | 672 080 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 833 000 | -11 081 000 | -15 749 850 | -19 845 342 | -22 788 208 | -24 589 976 | -25 262 056 | -25 262 056 | -25 262 056 | -25 262 056 | -25 262 056 | -25 262 056 |

**Waterfall на 1 клиента / месяц**

| Шаг | ₽ |
|---|---:|
| ARPA | 900 000 |
| Gross profit | 585 000 |
| Contribution | 565 000 |
| EBITDA before tax | 565 000 |
| Net after УСН 6% | 511 000 |
| Net after IT-льгота 3% | 538 000 |
| Net after ОСНО 20%* | 452 000 |

* Для ОСНО показан только налог на прибыль 20% от EBITDA; НДС 20% считать отдельно, если price card quoted gross-of-VAT.

**Cash flow**: startup_capital_to_bep_rub = 25 262 056 ₽.

**Налоговая модель**

- База для расчёта: выручка на клиента 900 000 ₽/мес.
- УСН: 6% от выручки = 54 000 ₽/клиент/мес.
- IT-льгота: 3% от выручки = 27 000 ₽/клиент/мес при аккредитации Минцифры.
- Страховые взносы: ~30% к ФОТ уже заложены в team FOT/fixed costs.
- НДС 20%: применять только при ОСНО; в модели PnL выше выручка показана net для операционной сопоставимости.

**Break-even**: 11 клиентов; по месяцам: M8.

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## 1. Sensitivity analysis, EBITDA через 12 месяцев

База берётся из SECTION A: base-case M12 EBITDA = **317 042 ₽/мес** при **14,3** активных клиентах, ARPA **700 000 ₽/мес**, gross profit на клиента **430 000 ₽/мес**, churn **1,5%/мес**, CAC **1,75 млн ₽**.

Для чувствительности использую один и тот же fixed cost base **5 833 000 ₽/мес** и следующие правила:
- **Sens1, CAC x2**: acquisition budget тот же, значит новых клиентов удаётся закрыть примерно вдвое меньше.
- **Sens2, Churn x2**: new bookings те же, но churn растёт с **1,5%** до **3,0%**.
- **Sens3, Price -30%**: ARPA падает до **490 000 ₽/мес**, COGS на раннем горизонте считаю липкими и оставляю **270 000 ₽/клиент/мес**.

| Сценарий | ARPA, ₽/мес | CAC, ₽ | Churn / мес | Активных клиентов к M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---:|---:|---:|---:|---:|---|
| Base | 700 000 | 1 750 000 | 1,5% | 14,3 | 317 042 | Едва выходит в плюс |
| Sens1: CAC x2 | 700 000 | 3 500 000 | 1,5% | 7,2 | -2 757 979 | GTM ломается, scale почти вдвое медленнее |
| Sens2: Churn x2 | 700 000 | 1 750 000 | 3,0% | 13,6 | 35 490 | Формально около нуля, но запаса нет |
| Sens3: Price -30% | 490 000 | 1 750 000 | 1,5% | 14,3 | -2 686 467 | Самый опасный single-variable shock |

### Вывод по чувствительности
- Самая токсичная переменная здесь, **price compression**: минус 30% по цене почти полностью убивает EBITDA.
- **CAC inflation** тоже критична: проект остаётся живым как продукт, но перестаёт быть scale-friendly как венчурный актив.
- **Churn x2** не убивает модель мгновенно, но оставляет компанию у нулевой черты и делает любой следующий shock фатальным.

## 2. Monte Carlo Lite, confidence intervals

Вместо одной тройки base/opt/pess задаю треугольные распределения для ключевых драйверов. Min/mode/max выбраны из уже использованных economics assumptions и соседних допустимых band'ов для enterprise AI в finance. [T1][T2][T3][T4][T5]

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 1 200 000 | 1 750 000 | 2 600 000 | [T1] |
| Monthly churn % | 1,0% | 1,5% | 3,0% | [T1][T3] |
| ARPU ₽/мес | 490 000 | 700 000 | 910 000 | [T1][T2] |
| Conversion rate lead→paid % | 0,8% | 1,26% | 2,8% | [T1] |
| Time-to-hire месяцев | 0,5 | 1,5 | 3,0 | [T1][T5] |

### Методика
Полные 1000 итераций не считаю кодом, а делаю **Monte Carlo Lite** через 9 комбинаций вокруг min/mode/max:
- best: CAC_min + churn_min + ARPU_max
- median: CAC_mode + churn_mode + ARPU_mode
- worst: CAC_max + churn_max + ARPU_min
- плюс 6 смешанных комбинаций между ними

Предпосылка для M24: после M12 компания продолжает продавать примерно **2 новых клиента/мес** в base-режиме; при росте CAC поток новых клиентов уменьшается пропорционально при том же acquisition spend.

### Результаты доверительных интервалов

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|-------------:|
| EBITDA @M24 (₽/мес) | -627 477 | 8 806 714 | 23 488 726 | 24 116 203 |
| CAC payback (мес) | 5,3 | 2,5 | 1,3 | 4,0 |
| LTV/CAC | 2,8x | 16,4x | 53,3x | 50,5x |
| Cash runway (мес) | 39,8 | >60 | >60 | >20 |

### Интерпретация Monte Carlo Lite
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1**: риск неплатёжеспособности и дофинансирования остаётся реальным даже после прохождения base-case.
2. **p50 EBITDA > 500К ₽/мес**, значит median-case EBITDA Gate проходит. Это плюс.
3. Формально коэффициент **p90/p10** неинтерпретируем из-за отрицательного p10, но по сути это ещё хуже правила **10x dispersion**: хвост слева уходит ниже нуля, значит неопределённость очень высокая и score нужно даунгрейдить.
4. **Range width по LTV/CAC = 50,5x**, намного выше порога **8**, значит модель очень хрупкая к сочетанию pricing, CAC и churn.

### Что это значит для инвестрешения
Base-case у Rogo-подобного актива выглядит сильным, но распределение outcomes очень широкое. Это не «стабильный compounder», а **узкий high-ticket bet**, где даже хороший median скрывает тяжёлый downside при price compression или CAC blow-up.

## 3. Competitor deep-dive

### 3.1 Западные конкуренты

#### 1) Hebbia
- **Что делает**: AI knowledge work / due diligence copilot для фондов, банков и legal-heavy команд. [T6]
- **Strengths**:
  - сильный бренд в buy-side и deal workflows,
  - хорошо ложится на large document sets и data room analysis,
  - premium enterprise positioning.
- **Weaknesses**:
  - высокая стоимость внедрения и длинный enterprise cycle,
  - риск стать «horizontal research layer» без жёсткого workflow lock-in,
  - сложнее локализовать под российские закрытые источники и контуры.
- **Market-share estimate**: **1-3%** в глобальном AI-native сегменте research/diligence для upper-end finance teams, но share of mind существенно выше доли выручки.
- **Our advantage**:
  - локальная data residency,
  - faster deployment для РФ/CIS finance teams,
  - возможность продавать как compliance-friendly private deployment, а не только как западный SaaS.

#### 2) AlphaSense
- **Что делает**: market intelligence и search platform для research, corpdev, consulting и capital markets. [T7]
- **Strengths**:
  - мощная библиотека контента и market intelligence moat,
  - зрелый enterprise sales motion,
  - сильный incumbent status у research-heavy организаций.
- **Weaknesses**:
  - больше intelligence terminal, чем action-oriented workflow system,
  - высокая зависимость от западных data subscriptions,
  - в локальном русском контуре часть преимущества теряется.
- **Market-share estimate**: **10-15%** глобального enterprise market-intelligence слоя для крупных research teams, особенно как replacement/adjacent to legacy research stacks.
- **Our advantage**:
  - не competing-on-content breadth, а competing-on-workflow для сделки, memo и investment committee deliverables,
  - ниже total cost для регионального клиента,
  - проще встроить закрытые локальные источники и клиентские данные.

#### 3) Daloopa
- **Что делает**: AI/data extraction для financial models, filings и investment research automation. [T8]
- **Strengths**:
  - силён в extracted structured data,
  - понятный ROI на analyst productivity,
  - ближе к ядру financial modeling, чем generic chatbot.
- **Weaknesses**:
  - narrower wedge, чем у полноценного workflow copilot,
  - может упираться в coverage и ручную валидацию edge-cases,
  - сложнее защитить premium multiple без end-to-end workflow control.
- **Market-share estimate**: **2-4%** в AI financial-data-extraction нише, в основном как specialist vendor.
- **Our advantage**:
  - более широкий use-case: research + memo drafting + Q&A + internal knowledge,
  - возможность адаптировать продукт под русскоязычные документы, неструктурированные data rooms и локальный регконтур.

### 3.2 Российские конкуренты и substitute-set

Прямых российских копий Rogo почти нет, поэтому ниже не только прямые конкуренты, но и **наиболее близкие substitutes** в document AI, KYC/IDP и enterprise knowledge automation для финансового контура.

#### 1) Smart Engines
- **Что делает**: OCR, IDP, распознавание документов, strong presence в финсекторе и KYC/AML use-cases. [T9][T10]
- **Strengths**:
  - сильная локальная технология в документах и on-prem deployment,
  - доверие со стороны банков и regulated clients,
  - понятная импортонезависимая ценность.
- **Weaknesses**:
  - это не полноценный IB/PE research copilot,
  - фокус на document layer, а не на memo/investment workflow,
  - меньше product surface для аналитической генерации.
- **Market-share estimate**: **8-12%** российского OCR/IDP enterprise-сегмента; в finance-specific analyst layer доля минимальна.
- **Our advantage**:
  - Rogo-подобный продукт может сидеть выше по стеку, превращая распознанные документы в выводы, memo и analyst workflow.

#### 2) Content AI
- **Что делает**: OCR, capture, document processing для enterprise и госсектора. [T11][T12]
- **Strengths**:
  - большая installed base в document workflows,
  - enterprise-grade продажи и интеграции,
  - понятный бренд на рынке capture/processing.
- **Weaknesses**:
  - слабее AI-native positioning именно как аналитик для корпоративных финансов,
  - высокая зависимость от интеграторской модели,
  - может давать «трубу документов», но не финальный investment insight.
- **Market-share estimate**: **10-15%** российского OCR/capture слоя, особенно среди крупных enterprise внедрений.
- **Our advantage**:
  - быстрее показать board-level output, а не только extraction,
  - выше perceived ROI для M&A, PE и corpdev команд.

#### 3) Dbrain
- **Что делает**: document AI / OCR / KYC automation, участник Skolkovo и enterprise AI layer для документов. [T13][T14]
- **Strengths**:
  - сильная tech-first репутация,
  - хороший fit для KYC, back-office automation и document ingestion,
  - близость к финсектору через документы и проверки.
- **Weaknesses**:
  - продукт ближе к infrastructure layer, чем к banker workflow,
  - меньше доказанной traction именно в IB/PE knowledge work,
  - выше риск commoditization на документном слое.
- **Market-share estimate**: **2-5%** российского intelligent document processing сегмента.
- **Our advantage**:
  - можно занять более дорогой application layer поверх Dbrain-подобных capabilities.

#### 4) Just AI
- **Что делает**: корпоративные AI-ассистенты, knowledge bots и автоматизация коммуникаций. [T15][T16]
- **Strengths**:
  - сильный enterprise go-to-market,
  - опыт продакшн-внедрений в крупные организации,
  - хорошая экспертиза в conversational orchestration.
- **Weaknesses**:
  - слабее специализация именно на finance research и modeling,
  - customer perception может быть как «chatbot vendor», а не mission-critical analyst stack,
  - меньше moat на financial datasets и deal workflows.
- **Market-share estimate**: **5-8%** российского enterprise conversational AI, но **<2%** в узком finance-analyst use-case.
- **Our advantage**:
  - vertical focus на investment memo, committee prep и research QA, а не на generic bot layer.

### 3.3 Общий вывод по конкурентам
- На Западе конкуренция уже сильная, и moat строится через **workflow + proprietary data access + trust**.
- В России ниша прямого finance-AI-аналитика пока почти пустая, но substitutes на document AI и enterprise assistant layer уже есть.
- Поэтому главная ставка не на «лучший чат с документами», а на **закрытый enterprise workflow для finance decision-making**: data room → diligence → memo → IC prep → Q&A trail.

## 4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder-led sales не масштабируется, pipeline держится на 1-2 личных каналах | high | high | >70% qualified pipeline приходит от founder intros | нанять AE с finance domain expertise, формализовать ICP/playbook, развить partner channel |
| 2 | Operational | Delivery превращается в полу-консалтинг, onboarding и кастомизация раздувают COGS | high | high | implementation >8 недель, >25% roadmap уходит в one-off requests | productize templates, ограничить custom scope, жёсткий SOW и платные change requests |
| 3 | Operational | LLM API latency/cost volatility ухудшает UX и gross margin | med | high | inference cost/client >120K ₽ или median response time >20 сек | multi-model routing, caching, fallback vendors, ограничение дорогих deep-research flows |
| 4 | Market | Реальный спрос слишком узок, ICP ограничивается несколькими десятками команд | med | high | <15 target accounts доходят до пилота за 2 квартала | расширить wedge в corpdev/strategy, продавать team package, а не single-seat |
| 5 | Market | Конкуренты price-compress рынок, и ARPA сползает ниже 500K ₽/мес | high | high | win-rate растёт только при discount >25% | value-based packaging, private deployment surcharge, paid onboarding |
| 6 | Market | Инкумбенты типа AlphaSense/Hebbia закрывают core use-cases у premium-клиентов | med | high | в enterprise deal review клиент уже использует 1-2 западных incumbent tools | фокус на local data, Russian-language workflow, secure contour и post-pilot speed |
| 7 | Regulatory | 152-ФЗ и data residency мешают использовать внешний SaaS/облако для чувствительных документов | high | high | infosec review требует on-prem/VPC в >50% сделок | изначально проектировать private cloud/on-prem SKU, логирование и DPA-пакет |
| 8 | Regulatory | 115-ФЗ / AML / audit trail требования делают explainability и traceability обязательными | med | high | compliance требует сохранить источники каждого вывода и chain-of-evidence | citation layer, immutable audit logs, human-in-the-loop approval |
| 9 | Regulatory | Санкции и блокировки SaaS-поставщиков ломают часть стека и procurement | med | high | vendor legal/security questionnaire начинает стопорить закупку >60 дней | vendor redundancy, локальные аналоги, self-hosted critical components |
| 10 | Financial | Cash runway сжимается из-за длинного sales cycle и delayed collections | med | high | DSO >75 дней, pilot-to-paid >6 месяцев | upfront pilot fees, milestone billing, raise buffer 25-30% сверх burn-to-BE |
| 11 | Financial | Ослабление рубля поднимает стоимость USD-привязанных моделей и cloud | high | med | USD/RUB скачок >20% за квартал | рублёвый pricing с FX-clause, pre-purchase credits, локальные модели для части трафика |
| 12 | Financial | Инфляция зарплат senior ML/backend/AE съедает operating leverage | med | med | FOT растёт >15% год к году без соразмерного роста MRR | remote hiring outside Moscow, stock-heavy packages, automation внутренних процессов |
| 13 | Black swan | Война/новые санкции резко сужают клиентскую базу или блокируют западные API | med | very high | несколько клиентов одновременно замораживают закупки, API/legal notices от поставщиков | sovereign stack plan, локальные inference fallback, сегментация клиентов по risk profile |
| 14 | Black swan | Ключевой LLM vendor отключает доступ или меняет policy для finance use-cases | low | very high | рост error rate, policy refusals, sudden contract changes | abstraction layer, резервные модели, хранение prompt/eval suite для быстрого re-platforming |

### Итог по risk matrix
Рисковый профиль у кейса выше среднего даже по меркам enterprise AI. Большая часть downside сконцентрирована не в технологии как таковой, а в сочетании **узкого ICP + price compression + регуляторного контура + зависимости от внешних моделей**.

## 5. Kill conditions через 6 месяцев

1. **EBITDA downside kill**: если обновлённый p10 для **EBITDA @M24 < 0**, проект нельзя продолжать без резкого пересмотра pricing/GTM, потому что downside остаётся insolvent even after learning cycle.
2. **Median profitability kill**: если через 6 месяцев пересчитанный **p50 EBITDA @M24 < 500 000 ₽/мес**, кейс не проходит EBITDA Gate даже в median и не тянет венчурный риск.
3. **Commercial traction kill**: если к M6 нет хотя бы **3 платящих клиентов** или хотя бы **1 клиента с ARPA ≥700K ₽/мес**, значит рынок не подтвердил high-ticket thesis и модель сползает в non-investable custom work.

## 6. Итог SECTION B

Rogo-like кейс остаётся **проходимым, но хрупким**. У него сильный upside в median и p90, однако downside всё ещё уходит ниже нуля, а диапазон LTV/CAC слишком широк. Значит это не универсальный category winner, а **selective investment candidate**, который можно брать только при жёсткой дисциплине по pricing, secure deployment и enterprise sales execution.

## Источники SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/rogo-finance-ai-analyst-v2/04-economics.md
- [T2] OpenAI x Rogo case study: https://openai.com/index/rogo/
- [T3] Optifi, SaaS churn benchmarks: https://www.optifi.ai/post/saas-churn-benchmarks
- [T4] Rogo funding / expansion note: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion
- [T5] HH.ru role benchmarks already referenced in 04-economics.md
- [T6] Hebbia official site: https://www.hebbia.com/
- [T7] AlphaSense official site: https://www.alpha-sense.com/
- [T8] Daloopa official site: https://daloopa.com/
- [T9] Smart Engines company page: https://smartengines.ru/
- [T10] Habr, Smart Engines / OCR in finance: https://habr.com/ru/companies/smartengines/
- [T11] Content AI official site: https://contentai.ru/
- [T12] Rusprofile, Content AI legal entity: https://www.rusprofile.ru/
- [T13] Dbrain official site: https://dbrain.io/
- [T14] Skolkovo company page / profile references for Dbrain: https://navigator.sk.ru/
- [T15] Just AI official site: https://just-ai.com/
- [T16] VC.ru / Habr materials on Russian enterprise AI assistants: https://vc.ru/ and https://habr.com/

<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[FINTECH] Rogo Finance AI Analyst v2 — NEAR-PASS: 67/100 | EBITDA base=317К₽/мес через 12 мес | LTV/CAC=16,4x | Ключевое преимущество: finance-native workflow для memo и diligence | Главный риск: слишком узкий buyer universe и price compression.

# 06-verdict

sector: FINTECH

## Investment Committee Verdict
- Название: Rogo Finance AI Analyst v2
- Финальный статус: NEAR-PASS
- Normalized score: 67/100
- Raw score: 100/150
- Решение по пайплайну: REJECTED (<70), но близко к проходу при доказательстве repeatable GTM и 3+ платящих enterprise-клиентов.
- Delta vs previous: у исходного raw-сигнала не было полноценного P7-вердикта; ближайший аналог в базе, `investment-banking-ai-analyst-operator-v2`, был на 69/100, текущий кейс слабее на 2 балла из-за более узкого локального buyer universe.

## Оценка
Source tier balance: T1=4, T2=4, T3=0, weighted=2.50. Penalty applied: 0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | "LTV = 28,65 млн ₽", "LTV/CAC = 16,4x", "Gross Margin = 61,4%" и "CAC Payback = 2,5 месяца" из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 16 | Base-case даёт только "317 042 ₽/мес" на M12, но p50 в M24 = "8 806 714 ₽/мес" и 500К₽ достижимы примерно с 16 клиентами. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | В 02-demand указано: "exact-demand в РФ слабый", но есть "25 000+ финансовых профессионалов" у Rogo и TAM "648 млн ₽/год" в локальном контуре. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | Продукт встроен в workflow, но substitutes сильны: в 05-critic прямо сказано, что в РФ ниша почти пуста, однако substitutes на document AI и enterprise assistant layer уже есть. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | Риск высокий, но управляемый: "p10 EBITDA < 0", есть 14 рисков, однако команда и on-prem/private deployment motion выглядят реалистично. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | GTM тяжёлый, но конкретный: founder-led outbound, partnerships, ABM; blended CAC 1,75 млн ₽ окупается за 2,5 мес по MRR и ICP концентрирован. |

**Normalized score = round((100 × 100) / 150) = 67/100.**

## 7-factor Moat Framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных из-за закрытых контуров и приватных данных. |
| Switching costs | 2 | После интеграции data room, шаблонов memo и audit trail переключение станет болезненным. |
| Scale economies | 1 | COGS на inference и support падает ограниченно, secure deployment остаётся дорогим. |
| Proprietary data / model advantage | 1 | Пока нет доказанного локального proprietary dataset moat, только гипотеза вокруг закрытых клиентских данных. |
| Regulatory moat | 2 | 152-ФЗ, data residency и audit trail создают барьер, но это compliance tax, а не уникальная лицензия. |
| Brand / distribution | 1 | Глобальный proof сильный, локального бренда и канала в РФ пока нет. |
| Embedded workflow | 2 | Value сидит внутри data room → diligence → memo → IC prep, что даёт хороший workflow stickiness. |

Сумма 7-factor = 9/21.
**Moat score = round((9 × 25) / 21) = 11/25.**

Вывод по moat: moat слабее среднего. Он не попал ниже 10, но находится опасно близко к weak moat зоне и остаётся одной из причин near-pass.

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Target account selection | Founder + SDR | CRM, ручной account mapping | 6 ч | 12 000 | Низкая |
| 2 | Холодный outreach / warm intro | SDR | CRM, email, мессенджеры | 18 ч | 36 000 | Средняя |
| 3 | Discovery call | Founder/AE | Zoom/Meet, CRM | 2 ч | 18 000 | Низкая |
| 4 | Demo на finance use-case | AE + Solutions/CTO | Demo env, shared deck | 4 ч | 42 000 | Низкая |
| 5 | Security / IT review | CTO + DevOps | VPC docs, security docs | 10 ч | 78 000 | Низкая |
| 6 | Pilot scoping | AE + CTO + PM/founder | SOW, pilot plan | 6 ч | 54 000 | Низкая |
| 7 | Pilot setup | Backend + ML + DevOps | Private cloud, connectors | 28 ч | 168 000 | Средняя |
| 8 | Pilot support and iteration | ML + CS + AE | Slack/Telegram, issue tracker | 30 ч | 165 000 | Средняя |
| 9 | Procurement / legal / info-sec | Founder + AE + legal | MSA/DPA, procurement docs | 12 ч | 96 000 | Низкая |
| 10 | Commercial negotiation | Founder + AE | Pricing model, ROI memo | 4 ч | 42 000 | Низкая |
| 11 | Contract signing | Founder + legal | E-sign / paperflow | 3 ч | 24 000 | Средняя |
| 12 | Invoice + payment collection | Finance ops | 1C/банк/ЭДО | 2 ч | 9 000 | Высокая |

## Ключевые метрики
- customer_ltv_rub: 28 650 000 ₽
- blended CAC: 1 750 000 ₽
- LTV/CAC: 16,4x
- CAC payback: 2,5 мес
- Gross Margin: 61,4%
- contribution_margin_rub_month: 410 000 ₽
- fixed_costs_rub_month: 5 833 000 ₽
- company_ebitda_rub_month base @M12: 317 042 ₽
- company_ebitda_potential_rub_month @50 клиентов: 14 667 000 ₽
- clients_to_500k_ebitda: 16
- months_to_500k_ebitda: 13
- clients_to_1m_ebitda: 18
- months_to_1m_ebitda: 14-15
- break-even: 15 клиентов / M12
- startup_capital_to_bep_rub: 44 165 779 ₽

## Team table

| Роль | Функция | FOT fully-loaded ₽/мес | Hiring realism |
|---|---|---:|---|
| CEO / Founder | enterprise sales, fundraising, partnerships | 845 000 | Критичен для первых сделок, founder dependency высокая |
| CTO / Tech Lead | архитектура, security review, delivery | 715 000 | Нанять сложно, time-to-hire 2 мес |
| Senior Backend #1 | ingestion, backend, integrations | 546 000 | Реалистично |
| Senior Backend #2 | workflow engine, infra integration | 546 000 | Реалистично |
| ML Engineer | retrieval, evals, model orchestration | 650 000 | Дефицитная роль |
| DevOps | VPC, observability, deployment | 455 000 | Критичен для secure deployment |
| Frontend | analyst workspace UI | 390 000 | Реалистично |
| SDR | outbound prospecting | 234 000 | Нанимается быстро |
| AE | demos, pilot conversion, procurement | 494 000 | Одна из самых трудных GTM-ролей |
| Customer Success | onboarding, adoption, renewals | 338 000 | Подключается позже |
| **Итого** |  | **5 213 000** | Полный штат раскрывается только к M8 |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Крупнейший buyer закрытых finance-workflows, сильный M&A/strategy и высокий demand на audit trail. | intro через decision-maker + private roundtable | 900 000 ₽/мес |
| 2 | ВТБ | Большой поток корпоративного анализа и due diligence, чувствительность к secure deployment. | email decision-maker + отраслевой форум | 800 000 ₽/мес |
| 3 | Альфа-Банк | Сильный corpfin и CIB-контур, готовность платить за ускорение analyst output. | warm intro через fintech-партнёров | 750 000 ₽/мес |
| 4 | Газпромбанк | Частые проектные и структурные сделки, важны memo и committee materials. | конференция + follow-up email | 750 000 ₽/мес |
| 5 | МТС | Активный corpdev и strategy motion, нужен ускоренный market map и investment memo workflow. | email VP Strategy / CorpDev | 650 000 ₽/мес |
| 6 | АФК Система | Постоянная инвестиционная активность и portfolio-review burden. | партнёрство с advisory-бутиком | 700 000 ₽/мес |
| 7 | Северсталь | Регулярный capex/M&A screening, много внутренних материалов и сравнительного анализа. | конференция + targeted ABM | 600 000 ₽/мес |
| 8 | СИБУР | Corpdev и инвестиционный комитет по крупным проектам, нужен secure документный контур. | enterprise email + referral from SI | 650 000 ₽/мес |
| 9 | X5 Group | Strategy/corpdev функция и частый анализ рынков/активов. | vc.ru sponsored content + email | 550 000 ₽/мес |
| 10 | Яндекс | Большой объём strategic finance work и M&A evaluation, высокая ценность time-to-memo. | warm intro через AI/community network | 700 000 ₽/мес |

Комментарий: 10 named targets присутствуют, поэтому штраф -10 к GTM не применяется.

## Top-3 risks

| Риск | Вероятность | Влияние | Почему это top-3 |
|---|---|---|---|
| price_compression_below_500k | Высокая | Высокое | В 05-critic цена -30% даёт EBITDA @M12 = -2 686 467 ₽ и почти ломает кейс. |
| buyer_universe_too_narrow | Средняя | Высокое | В 02-demand локальный SAM всего 30 организаций, ошибка по ICP критична. |
| founder-led enterprise GTM | Высокая | Среднее/Высокое | В 04-economics early revenue почти целиком завязана на founder-led selling и trust motion. |

## Proof points required for APPROVED
1. Три платящих enterprise-клиента в РФ/СНГ с ARPA не ниже 700 000 ₽/мес.
2. Один кейс secure deployment или private cloud без кастомного консалтинга > 8 недель.
3. Pilot-to-paid conversion не ниже 30% на выборке хотя бы из 6 пилотов.
4. Подтверждение, что company_ebitda_rub_month проходит 500К₽ не позже 13-14 месяца без резкого расширения штата.
5. Повторяемый канал кроме founder intros, например 2+ сделки через advisory/SI partners.

## LTV Upside Calculator
Поскольку вердикт NEAR-PASS, ниже минимальные рычаги для перевода кейса в approve-диапазон:

| Рычаг | Текущее значение | Цель для approve | Эффект |
|---|---:|---:|---|
| ARPA | 700 000 ₽/мес | 800 000–900 000 ₽/мес | Даёт больше запаса против price compression |
| Pilot-to-paid | 30% | 35%+ | Снижает blended CAC и повышает GTM score |
| Churn | 1,5%/мес | ≤1,2%/мес | Укрепляет LTV и делает удержание investment-grade |
| New clients by M12 | 14,3 активных | 16+ активных | Переводит base EBITDA выше 500К₽/мес |
| Custom implementation | 8+ недель риск | ≤6 недель | Укрепляет moat и execution score |

## Финансовый вывод инвесткомитета
Сильная сторона кейса, это редкая для FINTECH комбинация хорошего customer_ltv_rub и короткого CAC payback даже при дорогом enterprise CAC. Слабая сторона, это хрупкость всей модели к одному shock-фактору: уменьшению price realization. При локальном buyer universe в десятки команд и founder-heavy GTM у фонда пока нет достаточного запаса прочности для approve.

## Окончательный вердикт
**NEAR-PASS / REJECTED FOR NOW.**

Кейс достоин повторного входа в инвесткомитет после подтверждения 3-5 локальных платящих команд, устойчивого чека 700К₽+ и одного доказанного non-founder канала продаж. Пока это хороший enterprise-finance thesis, но ещё не investment-grade asset для безусловного approve.


---

## Файл: 07-score-trajectory.md

# Score Trajectory

## 2026-05-11 — P5 Economics
- Stage: P5 Unit Economics
- Analyst: branch-models-lead
- Previous state: после P3 кейс был CONDITIONAL_PASS по demand, но с открытым риском недостаточного LTV и спорной локальной экономики.
- Economics update: собрана enterprise-модель для regulated finance workflow с MRR 700 000 ₽, blended fully-loaded CAC 1,75 млн ₽, Gross Margin 61,4%, Contribution Margin 58,6%, monthly churn 1,5%, LTV 28,65 млн ₽, LTV/CAC 16,4x, CAC Payback 2,5 мес.
- Break-even: 15 клиентов, ориентир по сроку выхода на операционный break-even около M12.
- Gate result: PASS.
- Score direction: повышаю оценку по качеству монетизации и предсказуемости unit economics, но оставляю дисконт за узкий ICP, founder dependency и риск heavy implementation.
- Investment reading: это не массовый SaaS, а нишевый high-ticket enterprise AI asset. Для фонда кейс годится только при подтверждении secure deployment motion и чека не ниже 700 тыс. ₽/мес.
- New trajectory status: P5 пройден, кейс можно двигать дальше в moat / final verdict.

## 2026-05-12 — P7 Critic and Verdict
- Stage: P7 Final Verdict
- Analyst: branch-models-lead
- Final score: 67/100 (raw 100/150).
- Verdict: NEAR-PASS / REJECTED FOR NOW.
- Score breakdown: Unit Economics 20/25, EBITDA Potential 16/25, Market+Demand 15/25, Moat 10/25, Execution Risk 17/25, GTM Realism 22/25.
- Tier-awareness: T1=4, T2=4, T3=0, weighted=2.50, penalty to Market+Demand = 0.
- Committee reading: сильная клиентская economics и реалистичный enterprise workflow подтверждены, но локальный buyer universe слишком узкий, moat слабее среднего, а downside к price compression слишком тяжёлый.
- What would change decision: 3+ платящих enterprise-клиента по 700К₽+/мес, repeatable partner channel и доказанный выход company_ebitda_rub_month выше 500К₽/мес к M13-M14 без распухания кастомной delivery.
- New trajectory status: near-pass, переведён в rejected до появления proof points для rerun.

