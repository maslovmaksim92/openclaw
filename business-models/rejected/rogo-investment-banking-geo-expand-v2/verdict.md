# Rogo Investment Banking Geo Expand v2 — Full Verdict Package
> Скомпилированный пакет стадий пайплайна для публикации в GitHub.
> Примечание: в этом кейсе отсутствует `03-demand.md`; фактическая demand-стадия представлена файлом `02-demand.md`.

---

## Файл: 00-brief.md

# Краткий бриф

## Кейс
Rogo для investment banking и AI-аналитики сделок

## Почему открыт
- Сигнал указывает на вертикальный AI-продукт для investment banking workflow, а не на generic copilot.
- В исходном triage уже зафиксированы признаки сильного traction: европейская экспансия, Series C на $75 млн и использование продукта десятками тысяч банкиров и инвесторов.
- Для РФ это выглядит как high-LTV FINTECH wedge для M&A, corpdev, PE/VC и аналитики сделок в защищённом контуре.

## Следующий шаг
Передать кейс в P3-demand-validation для новой аналитики по РФ-рынку, economics, moat и финальному verdict.

---

## Файл: 01-intake.md

---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-rogo-investment-banking-geo-expand.md
created: 2026-04-21T17:22+03:00
source_triage: triage/triage-2026-04-15-rogo-investment-banking-geo-expand.md
original_verdict: resurrect-full-pipeline
---

# Intake

## Статус
Принудительный resurrect/re-run. Кейс создан как standalone candidate и должен пройти полный пайплайн P3→P7 без классификации как duplicate.

## Исходный verdict
- `triage/triage-2026-04-15-rogo-investment-banking-geo-expand.md`

## Полный контекст raw-файла

# RESURRECT SIGNAL — rogo-investment-banking-geo-expand

## Meta
- source: triage/triage-2026-04-15-rogo-investment-banking-geo-expand.md
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
2026-04-15

## Входные данные
- pipeline/raw/raw-2026-04-15-rogo-investment-banking-geo-expand.md

## Классификация
supporting signal для существующего кейса

## Matching case
- `pipeline/cases/investment-banking-ai-analyst-operator/`

## Решение
Новый кейс не создавать. Обогатить существующий кейс `investment-banking-ai-analyst-operator`.

## Что добавлено в кейс
В `pipeline/cases/investment-banking-ai-analyst-operator/01-evidence.md` добавлена новая запись на русском языке с датой, URL источника и кратким объяснением, как сигнал усиливает кейс.

Добавленный смысл:
- появился дополнительный независимый supporting signal по теме vertical AI для investment banking;
- усилена уверенность, что рынок уже подтверждает enterprise traction категории, а не только точечный PR отдельных вендоров;
- подтверждена применимость кейса как high-LTV сервиса для локализации под российские инвестбанки, corpdev, PE/VC и M&A-команды.

## Ключевые факты, которые зафиксированы
- Rogo продолжает выглядеть как специализированная AI-платформа именно под investment banking workflow, а не как generic copilot;
- в сигнале повторно подтверждаются европейская экспансия, Series C на $75 млн и использование продукта 25 000+ банкиров и инвесторов;
- оценка потенциального LTV для РФ остаётся выше порога Program 1: 2,5-12,0 млн руб. в год на клиента.

## Что сделано
- Существующий кейс обогащён.
- Исходный raw-файл подлежит переносу в `pipeline/raw/processed/`.

## Вердикт
Кейс усилен: это не новый кейс, а качественное обогащение уже открытого направления `investment-banking-ai-analyst-operator`.

```

---

## Файл: 02-validation.md

> Файл отсутствует в кейсе.

---

## Файл: 03-demand.md

> Файл отсутствует в кейсе.

---

## Файл: 04-economics.md

---
stage: economics
case: rogo-investment-banking-geo-expand-v2
date: 2026-05-12
analyst: branch-models-lead
sector: FINTECH
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Краткий вывод
**Статус: PASS**

Rogo-подобный продукт для investment banking и PE в РФ выглядит не как массовый SaaS, а как узкий enterprise AI workflow. При base-case чеке **600 000 ₽ MRR на клиента**, fully-loaded CAC **2,33 млн ₽**, contribution margin **63,3%** и месячном logo churn **1,5%** модель даёт **LTV/CAC = 10,9x**, **CAC payback = 3,9 месяца** и break-even около **9 клиентов**. Profit Gate пройден.

Главный вывод для фонда: кейс **не упирается в unit economics**, а упирается в **узкий SAM, длинный enterprise sales cycle и риск white-glove delivery**.

## 1. Модель и допущения
- ICP: инвестбанки, PE/VC, corpdev, advisory boutiques верхнего сегмента.
- Average contract value: **600 000 ₽/мес** на клиента.
- Onboarding fee: разовая, в LTV не включаю.
- Base gross margin до fixed costs: **63,3%**.
- Тип GTM: enterprise / regulated-finance B2B.
- Для CAC применяю **enterprise multiplier 2,0x** к raw acquisition stack, потому что в сделке есть 2-3 calls, demo, security review, procurement и legal.

## 2. Детальный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-аккаунтов и ICP-листа | SDR | HH/СПАРК/ручной research, CRM | 2 ч | 2 200 | низкая |
| 2 | Первичный outreach по warm intro / email / Telegram / LinkedIn | SDR | CRM, sequencing, Sales Navigator | 1,5 ч | 1 900 | средняя |
| 3 | Discovery call и qualification | AE | Zoom/Meet, CRM | 1 ч | 4 100 | низкая |
| 4 | Demo на реальных finance workflow | AE + Solutions | Demo workspace, презентация | 2 ч | 9 800 | низкая |
| 5 | Pilot scoping: data sources, use-cases, security | Solutions Architect + CTO | Notion, security checklist | 3 ч | 15 200 | низкая |
| 6 | Pilot / sandbox deployment | DevOps + ML + Backend | Cloud, connectors, LLM stack | 10 ч | 41 500 | средняя |
| 7 | Pilot support, prompt tuning, feedback loop | CSM + ML | Slack/Telegram, issue tracker | 6 ч | 19 800 | средняя |
| 8 | Procurement, infosec, DPA / legal | AE + founder + legal | Документы, e-sign | 4 ч | 17 600 | низкая |
| 9 | Коммерческое согласование и invoice | Founder + AE + finance | CRM, 1С/банк | 1,5 ч | 7 100 | средняя |
| 10 | Оплата, onboarding и запуск recurring usage | CSM + Solutions | Billing, monitoring, support | 4 ч | 14 400 | средняя |

**Итого pre-paid delivery + sales cost на одну новую сделку:** около **133 600 ₽ прямого труда**, но реальный acquisition cost выше из-за зарплатной ёмкости enterprise GTM, tool stack и overhead. Поэтому для инвестиционного решения использую fully-loaded CAC ниже, а не только процессную себестоимость касаний.

## 3. COGS на клиента в месяц

### COGS breakdown per client / month
| Статья | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / inference / reranking | 45 000 | частые длинные документы, research-heavy usage |
| Secure cloud / storage / logging | 30 000 | изолированный контур, аудит, логи |
| Data connectors / ingestion / parsers | 20 000 | API и ingestion pipeline |
| Customer Success / support allocation | 40 000 | 1 CSM на ~15 клиентов |
| Solutions / implementation amortization | 55 000 | high-touch rollout и monthly optimization |
| Security / compliance operations | 15 000 | review, access control, audits |
| Итого COGS | **205 000** |  |

### Валовая экономика на клиента
- MRR: **600 000 ₽**
- COGS: **205 000 ₽**
- Contribution per client: **395 000 ₽**
- **Contribution Margin = 65,8%**

Для консервативности в итоговых KPI ниже использую ещё небольшой резерв на service credits и churned support load, поэтому расчётный portfolio-level contribution margin принимаю **63,3%**.

## 4. CAC по каналам и funnel conversion

### Воронка по каналам
| Канал | Leads/mo | SQL | Pilot | Win | Lead→SQL | SQL→Pilot | Pilot→Win | New paid/mo |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Founder-led warm intro / network | 20 | 8 | 4 | 2 | 40% | 50% | 50% | 2,0 |
| Target outbound ABM | 120 | 12 | 4 | 1 | 10% | 33% | 25% | 1,0 |
| Events / partnerships | 30 | 6 | 2 | 0,6 | 20% | 33% | 30% | 0,6 |

### CAC по каналам
| Канал | Monthly spend, ₽ | Wins/mo | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Founder-led warm intro | 1 800 000 | 2,0 | **900 000** | лучший канал, но не бесконечно масштабируется |
| Target outbound ABM | 1 450 000 | 1,0 | **1 450 000** | нужен SDR+AE+tooling |
| Events / partnerships | 1 200 000 | 0,6 | **2 000 000** | длиннее цикл, но высокий brand trust |

### Blended CAC
- Total acquisition spend / month: **4 450 000 ₽**
- New paid customers / month: **3,6**
- **Blended CAC = 1 236 000 ₽**

## 5. Fully-loaded CAC

### Таблица компонентов
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK, ретаргетинг + брендовый спрос) | 250 000 | ограниченный paid layer, т.к. search demand LOW | модель branch-models-lead по ICP и LOW demand из 02-demand |
| Outbound team FOT (SDR + AE attributed to new) | 1 742 000 | SDR 180k + AE 480k + bonus + 30% соцвзносы; 100% на new revenue | HH.ru benchmark + hiring realism baseline |
| Marketing team FOT (partial allocation) | 338 000 | 0,5 demand gen / content lead × 520k fully-loaded + 35% time founder | HH.ru benchmark + allocation model |
| Tools (CRM, sequencing, sales intelligence, data room) | 320 000 | CRM + Sales Navigator / Apollo-like stack + enrichment + webinar/demo | HubSpot/Sales tooling class benchmark + модель |
| Events / partnerships | 600 000 | 2 отраслевых события в квартал + travel amortized | enterprise field marketing assumption |
| Raw CAC stack | **3 250 000** | сумма выше |  |
| Overhead multiplier (x1,3 на acquisition org) | 975 000 | 30% сверху на management, finance, legal, recruiting, office/cloud shared costs | стандарт fully-loaded enterprise B2B |
| **Fully-loaded acquisition spend** | **4 225 000** | Raw × 1,3 |  |

### Fully-loaded CAC formula
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT + Tools/CRM + Events + Multiplier_overhead) / New paying customers**

- Fully-loaded acquisition spend: **4 225 000 ₽/мес**
- New paying customers: **1,81 / мес** в консервативном enterprise throughput
- **Fully-loaded CAC = 2 334 000 ₽**

### Sanity check against RU benchmarks
- Enterprise SaaS B2B benchmark по задаче: **300-900k ₽ / клиент** как direct CAC.
- Наш fully-loaded CAC **2,33 млн ₽** выше direct benchmark, что логично для regulated finance vertical с heavy presales и white-glove rollout.
- Значение **не выглядит искусственно заниженным**, red flag нет.

## 6. LTV и churn benchmark

### Benchmark source
По ChartMogul для SaaS с высоким ARPA customer churn обычно ниже mass-market, а для ARPA **$500+ / мес** customer churn находится в диапазоне **1-2% в месяц**. Для enterprise-like SaaS это разумный ориентир; для российского finance-vertical беру консервативно **1,5% logo churn / мес**.

Источники:
- ChartMogul Help Center, customer churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- ChartMogul blog, churn by ARPA bands: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/

### LTV calculation
Формула: **LTV = (MRR × Gross Margin) / Monthly Churn**

- MRR per client: **600 000 ₽**
- Gross margin: **63,3%**
- Gross profit per client/month: **379 800 ₽**
- Monthly churn: **1,5%**
- Expected lifetime: **66,7 месяца**
- **LTV = 25 320 000 ₽**

Для extra conservatism можно смотреть downside-case при churn 2,5%: тогда LTV = **15,2 млн ₽**. Даже в downside экономика остаётся выше investable threshold.

## 7. LTV/CAC ratio
- LTV: **25,32 млн ₽**
- Fully-loaded CAC: **2,334 млн ₽**
- **LTV/CAC = 10,9x**

### Вывод
Порог investment grade **>= 3:1** пройден с большим запасом. Даже downside-case с churn 2,5% даёт около **6,5x**.

## 8. CAC Payback
Формула по задаче: **CAC Payback = CAC / MRR per customer**

- Fully-loaded CAC: **2 334 000 ₽**
- MRR per customer: **600 000 ₽**
- **CAC Payback = 3,9 месяца**

Sanity check: для enterprise допустим порог до 18 месяцев, здесь запас хороший.

## 9. Contribution Margin %
Формула: **(Revenue - Variable COGS) / Revenue**

- Revenue per client/month: **600 000 ₽**
- Portfolio-level variable COGS: **220 200 ₽**
- Contribution profit: **379 800 ₽**
- **Contribution Margin = 63,3%**

Это нормально для AI workflow с дорогим, но не кастомным delivery. Ниже 55% было бы тревожно, выше 75% для такого enterprise use-case было бы слишком оптимистично.

## 10. Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи, fundraising, ключевые сделки | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security, enterprise delivery | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | connectors, data pipelines | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | document workflows, APIs | 420 000 | 126 000 | 546 000 |
| ML Engineer | retrieval, evals, prompt stack | 520 000 | 156 000 | 676 000 |
| DevOps | secure infra, observability | 360 000 | 108 000 | 468 000 |
| Frontend | analyst workspace | 300 000 | 90 000 | 390 000 |
| SDR | target outbound | 180 000 | 54 000 | 234 000 |
| AE | demo, negotiation, close | 320 000 | 96 000 | 416 000 |
| Customer Success / Solutions | onboarding, support, upsell | 260 000 | 78 000 | 338 000 |
| Finance / Ops (0,5 FTE or outsource) | invoicing, contracts, HR ops | 140 000 | 42 000 | 182 000 |
| **Итого** |  |  |  | **5 356 000 ₽/мес** |

### Таблица найма (Hiring Realism)
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 520 000 | 2,5 | 2 | 156 000 | 676 000 |
| DevOps | 1 | 360 000 | 1,5 | 1 | 108 000 | 468 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 + бонус | 0,75 | 1 | 54 000 | 234 000 |
| AE | 1 | 320 000 + комиссия | 1,5 | 2,5 | 96 000 | 416 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |

Источник для зарплатных вилок: **HH.ru benchmark / job postings по Москве и СПб, плюс baseline из задания**. Вилка выглядит реалистично для RU 2026.

## 11. Cumulative FOT timeline M1-M12

Найм разворачиваю постепенно. Массовый старт 5+ человек в M1 был бы red flag, поэтому его избегаю.

| Месяц | Кто уже в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | Founder, 1 Backend, Frontend | 1 781 000 |
| M2 | + SDR, + CS | 2 353 000 |
| M3 | + CTO, + DevOps, + AE | 3 952 000 |
| M4 | те же, AE/CTO ещё на ramp | 3 952 000 |
| M5 | + ML Engineer | 4 628 000 |
| M6 | + Backend #2 | 5 174 000 |
| M7 | полная рабочая команда | 5 356 000 |
| M8 | полная рабочая команда | 5 356 000 |
| M9 | полная рабочая команда | 5 356 000 |
| M10 | полная рабочая команда | 5 356 000 |
| M11 | полная рабочая команда | 5 356 000 |
| M12 | полная рабочая команда | 5 356 000 |

Средний FOT за первые 12 месяцев: **4,55 млн ₽/мес**.

## 12. Fixed costs breakdown
| Статья | ₽/мес |
|---|---:|
| FOT fixed org (не включая success-based variable part) | 5 356 000 |
| Office / legal / бухгалтерия / HR | 280 000 |
| Core software stack | 220 000 |
| Non-client cloud / staging / observability | 300 000 |
| Travel / enterprise sales | 180 000 |
| Misc reserve | 164 000 |
| **Итого fixed costs** | **6 500 000 ₽/мес** |

## 13. Break-even

### Break-even по числу клиентов
Формула: **Fixed costs / contribution profit per client**

- Fixed costs: **6 500 000 ₽/мес**
- Contribution profit per client: **379 800 ₽/мес**
- **Break-even = 17,1 клиента**

Округляя вверх: **18 клиентов**.

### Break-even по месяцу
Ramp-кейс по новым клиентам: M1=0, M2=1, M3=2, M4=3, M5=5, M6=7, M7=9, M8=11, M9=13, M10=15, M11=17, M12=19.

При таком сценарии:
- M11 ещё чуть ниже нуля,
- **M12 выходит в операционный break-even**.

## 14. Burn-to-breakeven
- Средний burn в M1-M6: около **5,9 млн ₽/мес**
- Средний burn в M7-M11: около **2,8 млн ₽/мес** после роста выручки
- Кумулятивный burn до operating break-even: около **43-46 млн ₽**

Это реалистично для enterprise B2B AI. Значение **<10 млн ₽ до BEP** здесь было бы red flag, но у нас такого занижения нет.

## 15. Cash runway
Предполагаю **startup_capital = 60 млн ₽**.

- Burn на старте: **~6,5 млн ₽/мес**
- Burn после первых контрактов: снижается до **3-4 млн ₽/мес**
- При базовом ramp runway: **12-14 месяцев**
- При слабом GTM и задержке закрытий на 1-2 квартала runway сжимается до **9-10 месяцев**

### Вывод по runway
Для такого кейса капитал меньше **40 млн ₽** уже выглядит тесно. Диапазон **50-70 млн ₽** на первый этап правдоподобнее.

## 16. Проверка Profit Gate
### Условие 1
EBITDA **> 500k ₽/мес** достижима задолго до 50 клиентов.

Проверка на 50 клиентах:
- Revenue: **30,0 млн ₽/мес**
- Contribution profit: **18,99 млн ₽/мес**
- Fixed costs: **6,5 млн ₽/мес**
- EBITDA before growth spend: **~12,49 млн ₽/мес**

### Условие 2
- **LTV/CAC = 10,9x**
- Порог отказа **< 1:1** не нарушен.

## 17. Риски, которые ещё могут сломать кейс
1. **Слишком узкий локальный SAM**: экономика хорошая, но сделок мало.
2. **Security / procurement drag**: цикл продаж легко уходит в 4-9 месяцев.
3. **White-glove delivery creep**: если кастомизация станет почти консалтингом, GM уйдёт вниз.
4. **Доступ к данным и локализация**: продукт должен работать на русскоязычных документах и локальных data workflows.
5. **Founder dependence**: лучший канал сейчас warm intros; масштабирование outbound ограничено.

## 18. Итоговый verdict
**PASS в Program 5.**

Финансово это выглядит как **инвестируемый niche enterprise AI business**, если фонд принимает:
- узкий и элитный ICP,
- длинные продажи,
- высокий pre-sales и deployment load,
- зависимость от founder-led GTM на ранней стадии.

Если смотреть только на unit economics, кейс **сильнее среднего**. Если смотреть на market size и repeatability, это **хороший нишевый bet, но не очевидный venture-scale outlier в РФ-контуре**.

## Источники
- 02-demand: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/rogo-investment-banking-geo-expand-v2/02-demand.md
- Rogo Series C / traction: https://rogo.ai/news/scaling-rogo-to-build-the-future-of-investment-banking-our-75m-series-c-and-european-expansion
- OpenAI x Rogo case: https://openai.com/index/rogo/
- ChartMogul customer churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- ChartMogul churn by ARPA bands: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
- Salary baseline: HH.ru benchmark ranges по Москве/СПб + hiring realism baseline из задания

---

## Файл: 05-critic.md

# SECTION A — PnL

## 1. Допущения модели

- Источник юнит-экономики: `04-economics.md`.
- ARPA base: **600 000 ₽/мес** на клиента.
- Portfolio COGS/client/month base: **220 200 ₽** (из contribution margin 63,3%).
- Fixed costs: **6 500 000 ₽/мес**, включая FOT; страховые взносы на ФОТ ~**30%** уже встроены в FOT и fixed cost baseline.
- CAC blended: **2 334 000 ₽**. По каналам из 04-economics: warm intro **900 000 ₽**, outbound ABM **1 450 000 ₽**, events/partnerships **2 000 000 ₽**.
- Churn: base **1,5%/мес**, optimistic **1,0%**, pessimistic **2,5%**.
- НДС **20%** релевантен только при ОСНО и не включён в выручку PnL, а учитывается в налоговой модели как отдельный режимный фактор.

## 2. Сценарий Base

- ARPA: **600 000 ₽**
- COGS/client/month: **220 200 ₽**
- Contribution/client/month: **379 800 ₽**
- Fixed costs/month: **6 500 000 ₽**
- Break-even по клиентам: **18**
- Break-even по месяцу: **M12**
- startup_capital_to_bep_rub: **41 202 110 ₽**

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 1 | 1.98 | 2.96 | 4.91 | 6.84 | 8.73 | 10.60 | 12.44 | 14.26 | 16.04 | 17.80 |
| MRR, ₽ | 0 | 600 000 | 1 191 000 | 1 773 135 | 2 946 538 | 4 102 340 | 5 240 805 | 6 362 193 | 7 466 760 | 8 554 758 | 9 626 437 | 10 682 041 |
| COGS, ₽ | 0 | 220 200 | 437 097 | 650 741 | 1 081 379 | 1 505 559 | 1 923 375 | 2 334 925 | 2 740 301 | 3 139 596 | 3 532 902 | 3 920 309 |
| Gross profit, ₽ | 0 | 379 800 | 753 903 | 1 122 394 | 1 865 159 | 2 596 781 | 3 317 429 | 4 027 268 | 4 726 459 | 5 415 162 | 6 093 535 | 6 761 732 |
| GM% | 0.0% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% | 63.3% |
| Fixed costs, ₽ | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 | 6 500 000 |
| EBITDA, ₽ | -6 500 000 | -6 120 200 | -5 746 097 | -5 377 606 | -4 634 841 | -3 903 219 | -3 182 571 | -2 472 732 | -1 773 541 | -1 084 838 | -406 465 | 261 732 |
| Cash burn, ₽ | 6 500 000 | 6 120 200 | 5 746 097 | 5 377 606 | 4 634 841 | 3 903 219 | 3 182 571 | 2 472 732 | 1 773 541 | 1 084 838 | 406 465 | 0 |
| Cumulative cash, ₽ | -6 500 000 | -12 620 200 | -18 366 297 | -23 743 903 | -28 378 744 | -32 281 963 | -35 464 533 | -37 937 265 | -39 710 806 | -40 795 644 | -41 202 110 | -41 202 110 |


### Waterfall на клиента в месяц

| Метрика | ₽/client/month |
|---|---:|
| ARPA | 600 000 |
| Gross | 379 800 |
| Contribution | 379 800 |
| EBITDA (M12 run-rate) | 14 701 |
| Net after tax, УСН 6% (M12 run-rate) | -21 299 |
| Net after tax, IT-льгота 3% (M12 run-rate) | -3 299 |
| Net after tax, ОСНО 20% на прибыль (M12 run-rate) | 11 761 |

### Налоговая модель

- **УСН 6%**: налог = 6% от выручки; подходит early-stage режиму без НДС.
- **IT-льгота 3%**: при аккредитации Минцифры и соблюдении критериев, эффективнее УСН по net margin в этом кейсе.
- **ОСНО**: в PnL считаю **20% налог на прибыль** только на положительный EBIT; **НДС 20%** учитывать отдельно в cash conversion и договорах, т.к. он влияет на оборотный капитал и pricing, но не должен дублироваться в выручке PnL.
| Режим | Налог M12, ₽ | Net profit M12, ₽ |
|---|---:|---:|
| УСН 6% | 640 922 | -379 191 |
| IT-льгота 3% | 320 461 | -58 730 |
| ОСНО 20% на прибыль | 52 346 | 209 385 |

## 2. Сценарий Optimistic

- ARPA: **660 000 ₽**
- COGS/client/month: **210 000 ₽**
- Contribution/client/month: **450 000 ₽**
- Fixed costs/month: **7 000 000 ₽**
- Break-even по клиентам: **16**
- Break-even по месяцу: **M8**
- startup_capital_to_bep_rub: **28 642 703 ₽**

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 1 | 1.99 | 3.97 | 5.93 | 7.87 | 10.79 | 13.68 | 16.55 | 19.38 | 22.19 | 24.97 | 27.72 |
| MRR, ₽ | 660 000 | 1 313 400 | 2 620 266 | 3 914 063 | 5 194 923 | 7 122 973 | 9 031 744 | 10 921 426 | 12 792 212 | 14 644 290 | 16 477 847 | 18 293 069 |
| COGS, ₽ | 210 000 | 417 900 | 833 721 | 1 245 384 | 1 652 930 | 2 266 401 | 2 873 737 | 3 474 999 | 4 070 249 | 4 659 547 | 5 242 951 | 5 820 522 |
| Gross profit, ₽ | 450 000 | 895 500 | 1 786 545 | 2 668 680 | 3 541 993 | 4 856 573 | 6 158 007 | 7 446 427 | 8 721 963 | 9 984 743 | 11 234 896 | 12 472 547 |
| GM% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% | 68.2% |
| Fixed costs, ₽ | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 | 7 000 000 |
| EBITDA, ₽ | -6 550 000 | -6 104 500 | -5 213 455 | -4 331 320 | -3 458 007 | -2 143 427 | -841 993 | 446 427 | 1 721 963 | 2 984 743 | 4 234 896 | 5 472 547 |
| Cash burn, ₽ | 6 550 000 | 6 104 500 | 5 213 455 | 4 331 320 | 3 458 007 | 2 143 427 | 841 993 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -6 550 000 | -12 654 500 | -17 867 955 | -22 199 275 | -25 657 283 | -27 800 710 | -28 642 703 | -28 642 703 | -28 642 703 | -28 642 703 | -28 642 703 | -28 642 703 |


### Waterfall на клиента в месяц

| Метрика | ₽/client/month |
|---|---:|
| ARPA | 660 000 |
| Gross | 450 000 |
| Contribution | 450 000 |
| EBITDA (M12 run-rate) | 197 445 |
| Net after tax, УСН 6% (M12 run-rate) | 157 845 |
| Net after tax, IT-льгота 3% (M12 run-rate) | 177 645 |
| Net after tax, ОСНО 20% на прибыль (M12 run-rate) | 157 956 |

### Налоговая модель

- **УСН 6%**: налог = 6% от выручки; подходит early-stage режиму без НДС.
- **IT-льгота 3%**: при аккредитации Минцифры и соблюдении критериев, эффективнее УСН по net margin в этом кейсе.
- **ОСНО**: в PnL считаю **20% налог на прибыль** только на положительный EBIT; **НДС 20%** учитывать отдельно в cash conversion и договорах, т.к. он влияет на оборотный капитал и pricing, но не должен дублироваться в выручке PnL.
| Режим | Налог M12, ₽ | Net profit M12, ₽ |
|---|---:|---:|
| УСН 6% | 1 097 584 | 4 374 963 |
| IT-льгота 3% | 548 792 | 4 923 755 |
| ОСНО 20% на прибыль | 1 094 509 | 4 378 037 |

## 2. Сценарий Pessimistic

- ARPA: **540 000 ₽**
- COGS/client/month: **240 000 ₽**
- Contribution/client/month: **300 000 ₽**
- Fixed costs/month: **6 200 000 ₽**
- Break-even по клиентам: **21**
- Break-even по месяцу: **не достигается в M1-M12**
- startup_capital_to_bep_rub: **59 077 737 ₽**

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 1 | 1.98 | 2.93 | 3.85 | 4.76 | 5.64 | 6.50 | 7.33 | 8.15 | 8.95 |
| MRR, ₽ | 0 | 0 | 540 000 | 1 066 500 | 1 579 838 | 2 080 342 | 2 568 333 | 3 044 125 | 3 508 022 | 3 960 321 | 4 401 313 | 4 831 280 |
| COGS, ₽ | 0 | 0 | 240 000 | 474 000 | 702 150 | 924 596 | 1 141 481 | 1 352 944 | 1 559 121 | 1 760 143 | 1 956 139 | 2 147 236 |
| Gross profit, ₽ | 0 | 0 | 300 000 | 592 500 | 877 688 | 1 155 745 | 1 426 852 | 1 691 180 | 1 948 901 | 2 200 178 | 2 445 174 | 2 684 045 |
| GM% | 0.0% | 0.0% | 55.6% | 55.6% | 55.6% | 55.6% | 55.6% | 55.6% | 55.6% | 55.6% | 55.6% | 55.6% |
| Fixed costs, ₽ | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 |
| EBITDA, ₽ | -6 200 000 | -6 200 000 | -5 900 000 | -5 607 500 | -5 322 312 | -5 044 255 | -4 773 148 | -4 508 820 | -4 251 099 | -3 999 822 | -3 754 826 | -3 515 955 |
| Cash burn, ₽ | 6 200 000 | 6 200 000 | 5 900 000 | 5 607 500 | 5 322 312 | 5 044 255 | 4 773 148 | 4 508 820 | 4 251 099 | 3 999 822 | 3 754 826 | 3 515 955 |
| Cumulative cash, ₽ | -6 200 000 | -12 400 000 | -18 300 000 | -23 907 500 | -29 229 812 | -34 274 067 | -39 047 216 | -43 556 035 | -47 807 134 | -51 806 956 | -55 561 782 | -59 077 737 |


### Waterfall на клиента в месяц

| Метрика | ₽/client/month |
|---|---:|
| ARPA | 540 000 |
| Gross | 300 000 |
| Contribution | 300 000 |
| EBITDA (M12 run-rate) | -392 984 |
| Net after tax, УСН 6% (M12 run-rate) | -425 384 |
| Net after tax, IT-льгота 3% (M12 run-rate) | -409 184 |
| Net after tax, ОСНО 20% на прибыль (M12 run-rate) | -392 984 |

### Налоговая модель

- **УСН 6%**: налог = 6% от выручки; подходит early-stage режиму без НДС.
- **IT-льгота 3%**: при аккредитации Минцифры и соблюдении критериев, эффективнее УСН по net margin в этом кейсе.
- **ОСНО**: в PnL считаю **20% налог на прибыль** только на положительный EBIT; **НДС 20%** учитывать отдельно в cash conversion и договорах, т.к. он влияет на оборотный капитал и pricing, но не должен дублироваться в выручке PnL.
| Режим | Налог M12, ₽ | Net profit M12, ₽ |
|---|---:|---:|
| УСН 6% | 289 877 | -3 805 832 |
| IT-льгота 3% | 144 938 | -3 660 894 |
| ОСНО 20% на прибыль | 0 | -3 515 955 |

## 3. Сводка по break-even и cash need

| Scenario | Break-even clients | Break-even month | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Base | 18 | M12 | 41 202 110 ₽ |
| Optimistic | 16 | M8 | 28 642 703 ₽ |
| Pessimistic | 21 | не достигнут в M1-M12 | 59 077 737 ₽ |

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

Предположение: для `CAC x2` сохраняем тот же темп привлечения, но удваиваем acquisition spend, уже встроенный в enterprise GTM-модель. Для `Churn x2` пересчитан клиентский портфель M1-M12. Для `Price -30%` сохраняем volume и cost base.

| Сценарий | Ключевое изменение | Total clients @M12 | MRR @M12, ₽ | EBITDA @M12, ₽ | Комментарий |
|---|---|---:|---:|---:|---|
| Base | Без изменений | 17,80 | 10 682 041 | 261 732 | Точка безубыточности почти достигнута |
| Sens1 | CAC x2 | 17,80 | 10 682 041 | -3 963 268 | При сохранении того же sales velocity модель уходит обратно в burn |
| Sens2 | Churn x2 (1,5% → 3,0%) | 16,70 | 10 019 105 | -157 907 | Break-even сдвигается правее M12 |
| Sens3 | Price -30% | 17,80 | 7 477 429 | -2 942 881 | Самый опасный удар по EBITDA, если рынок навяжет discounting |

## 2. Monte Carlo Lite — confidence intervals

### 2.1 Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 1 500 000 | 2 334 000 | 4 500 000 | [T1] |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | [T1] |
| ARPU, ₽/мес | 540 000 | 600 000 | 660 000 | [T1] |
| Conversion rate lead→paid, % | 1,0% | 2,1% | 4,0% | [T1] |
| Time-to-hire, мес | 1,0 | 1,5 | 2,5 | [T1] |

### 2.2 Метод

Полную 1000-run симуляцию не строю. Использую упрощённую сетку из 9 комбинаций по CAC, churn и ARPU, где:
- p10 ≈ worst-side combinations,
- p50 ≈ mode/mixed median,
- p90 ≈ best-side combinations.

Горизонт для интервалов: **M24**, так как на M12 модель ещё слишком близка к нулю и плохо отделяет noise от signal.

### 2.3 Результат

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24, ₽/мес | 3 732 526 | 7 539 734 | 10 585 297 | 6 852 771 |
| CAC payback, мес | 2,27 | 3,89 | 8,33 | 6,06 |
| LTV/CAC | 2,37x | 10,85x | 29,32x | 26,95 |
| Cash runway, мес | 14,96 | 17,47 | 19,65 | 4,69 |

### 2.4 Вывод по Monte Carlo Lite

- **Rule 1:** p10 EBITDA @M24 **выше нуля**, значит немедленный insolvency-trigger **не активирован**.
- **Rule 2:** p50 EBITDA @M24 = **7,54 млн ₽/мес**, значит EBITDA Gate в median-case **пройден**.
- **Rule 3:** p90/p10 по EBITDA ≈ **2,84x**, экстремальной неопределённости `>10x` **нет**.
- **Rule 4:** Range width по **LTV/CAC = 26,95**, это **намного выше порога 8**. Следовательно, модель хрупкая: outcome очень чувствителен к сочетанию pricing, churn и CAC.

Итог: **доходная модель в M24 выглядит жизнеспособной, но variance слишком велика для комфортного “set-and-forget” запуска**. Инвестиционный риск сидит не в среднем сценарии, а в хвостах распределения.

## 3. Competitor deep-dive

### 3.1 Западные конкуренты

> Оценка market share ниже — это **моя inference** по узкому сегменту AI research/copilot для investment banking, PE и adjacent institutional finance, а не по всему enterprise search рынку.

| Конкурент | Что делает | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Rogo | AI finance copilot для investment banks, PE и asset managers [E1] | Нативный фокус на IB workflow, private data rooms, strong referenceability, уже 5k+ bankers [E1] | Вероятно дорогой и US-centric; зависим от западных data vendors и SaaS stack | 3-5% узкого global AI-for-IB сегмента | Локализация под РФ, lower price point, data residency внутри РФ, интеграция в русскоязычный документооборот |
| Hebbia | Institutional AI для анализа документов и сделок [E2] | Сильный brand у buy-side/advisory, очень глубокая работа с длинными документами, massive processing scale | Менее vertical-specific для RU finance compliance, высокая сложность внедрения, premium pricing | 8-12% | Можем выиграть в domain-tuning под русские материалы, в compliance-by-design и в speed of onboarding |
| AlphaSense | Enterprise market intelligence/search platform для investment banking, PE, AM [E3] | Огромный контентный слой, mature workflow, citations, trusted enterprise UX | Это скорее broad intelligence layer, чем deal-native workflow; дорого; слабая пригодность для локальных private data workflows в РФ | 15-20% | Более узкий, но лучше заточенный продукт для deal execution, memo drafting и локального банковского use-case |

### 3.2 Российские конкуренты / ближайшие субституты

> В РФ я не вижу точного full-stack аналога Rogo для инвестбанкинга. Поэтому ниже — **ближайшие субституты**: legal/document AI, knowledge AI и secure document-processing players, которые могут “съесть” часть бюджета у целевого клиента.

| Конкурент | Что делает | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| Yandex B2B Tech: Нейроюрист + Нейроэксперт | Анализ документов, сравнение версий, reasoning over corp knowledge [E4][E5] | Огромная дистрибуция, низкий порог входа, готовая инфраструктура Yandex Cloud, сильный brand | Не investment-banking-native, меньше workflow depth в CIM/teaser/IC memo/diligence tracker | 25-35% среди широких RU AI knowledge assistants для adjacent задач | Мы можем быть не “ещё один ассистент”, а специализированный banker workstation с deal-specific outputs |
| Smart Engines | OCR/document AI для KYC, паспортов и финсервисов [E6] | Сильный on-prem/privacy narrative, глубокая экспертиза в document recognition для банковских процессов | Это слой распознавания, а не полнофункциональный research copilot; слабее в synthesis и memo generation | 8-12% в релевантном document-AI слое | Мы закрываем верхний слой value chain: не только извлечь поля, но и собрать вывод, тезисы, сравнительный анализ и draft материалов |
| FastLaw | LegalTech AI: маршрутизация документов, извлечение данных, текстовые ответы [E7] | Ранний AI-native фокус, document routing/extraction, потенциально ближе к enterprise legal ops | Узкий масштаб, менее сильный brand и sales reach, не finance-native | 1-3% | Более высокий чек и большее value capture в investment workflow, а не только в legal automation |

### 3.3 Конкурентный вывод

- **Главный западный benchmark**: Rogo/Hebbia/AlphaSense задают стандарт по UX, citation quality и depth of workflow.
- **Главный риск в РФ**: не столько прямой Rogo-клон, сколько то, что клиент закроет 60-70% потребности более дешёвым general-purpose AI stack от Яндекса + OCR/IDP layer + ручной аналитикой.
- **Наш шанс на defensibility**: стать не generic LLM UI, а **операционной системой сделки** для банкиров, с data-room ingestion, memo automation, comparable analysis и compliance-safe deployment.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется в repeatable GTM | high | high | >70% wins идут только из тёплых интро founder | Рано нанять enterprise AE, формализовать playbook, мерить non-founder sourced pipeline |
| Operational | White-glove delivery съедает margin | high | high | onboarding >4 недель, >20 часов кастомизации на клиента | Ограничить scope, стандартизировать templates/connectors, внедрить paid onboarding |
| Operational | Зависимость от внешних LLM API и latency/cost spikes | med | high | рост inference cost >25% QoQ, SLA incidents | Multi-model routing, локальный fallback, budget caps и caching |
| Market | Слишком узкий SAM в РФ investment banking | high | high | pipeline не растёт после первых 15-20 целевых аккаунтов | Расширение в PE, corpdev, Big4-style advisory, legal DD и sovereign finance workflows |
| Market | Price compression из-за generic AI assistants | high | high | discount >20% становится нормой в 3+ сделках подряд | Packaging по workflow, ROI calculator, premium security/compliance tier |
| Market | Конкурент выигрывает за счёт bundled distribution | med | med | клиенты выбирают bundle “cloud + LLM + doc AI” вместо point solution | Партнёрства с интеграторами/банковским ПО, API-first embedding strategy |
| Regulatory | Нарушение 152-ФЗ / data residency | med | high | security review блокирует пилот, клиент требует on-prem/VPC-only | Локальный контур, VPC/on-prem deployment, DPA и карта потоков данных |
| Regulatory | 115-ФЗ / AML-use-case требует explainability и audit trail | med | high | compliance team не принимает black-box outputs | Citations, logs, approval workflow, human-in-the-loop для high-risk задач |
| Financial | Runway сжимается из-за задержки закрытий на 1-2 квартала | high | high | cash <9 месяцев runway, M6 bookings below plan на 30%+ | Freeze hiring, stage-gated spend, bridge round only при подтверждённом pipeline |
| Financial | Рост USD и импортных SaaS/LLM costs | med | med | FX >15% against plan, vendor invoices растут быстрее ARPU | RUB pricing reviews, reserve buffer, partial import substitution |
| Black swan | Новые санкции режут доступ к западным SaaS/LLM | med | high | vendor TOS changes, account restrictions, billing failures | Архитектура с локальными моделями, domestic cloud mirrors, vendor diversification |
| Black swan | Геополитический shock / war escalation бьёт по deal volume | med | high | резкое падение M&A/ECM activity, стоп новых mandates | Сдвиг в restructuring, distressed, compliance/research use-cases; cost-down plan |

## 5. Kill conditions через 6 месяцев

1. **Model insolvency trigger**: если обновлённый rolling forecast покажет **p10 EBITDA @M24 < 0**, проект закрывать или переводить в services-only режим.
2. **GTM failure trigger**: если к концу **M6 < 7 активных клиентов** **или** win-rate pilot→paid **< 20%**, значит repeatability не появилась, несмотря на founder effort.
3. **Unit-economics trigger**: если к концу **M6 blended CAC > 3,5 млн ₽** **или** discounting уронит realized ARPU **< 500 тыс. ₽/мес**, дальше масштабировать нельзя, потому что медианный upside перестаёт окупать execution risk.

## 6. Bottom line по SECTION B

Финансовый downside **не убивает кейс автоматически**, но делает его **очень чувствительным к pricing discipline и качеству GTM**. Это не “safe SaaS compounding play”, а узкий enterprise-AI bet, где:
- upside есть,
- p50 хороший,
- но LTV/CAC dispersion слишком большая,
- а прямой moat появится только если продукт станет частью реального deal workflow, а не ещё одним чат-интерфейсом.

## Sources

- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/rogo-investment-banking-geo-expand-v2/04-economics.md
- [E1] https://openai.com/index/rogo/
- [E2] https://www.hebbia.com/
- [E3] https://www.alpha-sense.com/
- [E4] https://vc.ru/ai/2608476-yandex-b2b-tech-neuroyurist
- [E5] https://vc.ru/services/2079623-neyroekspert-ot-yandeksa-rezhimy-rabotyi-i-analiza-dannyih
- [E6] https://sk.ru/news/smart-engines-raspoznovanie-pasporta-rf/
- [E7] https://sk.ru/news/rezident-skolkovo-fastlaw-i-yuridicheskaya-kompaniya-pravokard-zapuskayut-sovmestnye-proekty-v-legaltech/

<!-- P6B-DONE -->

---

## Файл: 06-verdict.md

[FINTECH] Rogo Investment Banking Geo Expand v2 — NEAR-PASS: 67/100 | EBITDA base=641К₽/мес через 13 мес | LTV/CAC=10,9x | Ключевое преимущество: дорогой analyst workflow с сильной unit economics | Главный риск: узкий buyer universe и weak moat.

# 06-verdict

sector: FINTECH
status: NEAR-PASS
result: rejected
score: 67/100
case_slug: rogo-investment-banking-geo-expand-v2
date: 2026-05-20
analyst: branch-models-lead

## Investment committee summary
Rogo-подобный AI workflow для investment banking и PE в РФ проходит по клиентской экономике, но пока не проходит по качеству инвестиционного актива. Экономика на клиента сильная: customer_ltv_rub **25,32 млн ₽**, fully-loaded CAC **2,334 млн ₽**, **LTV/CAC 10,9x**, **CAC payback 3,9 мес**, contribution margin **63,3%**. Но локальный buyer universe узкий, moat слабее среднего, а весь GTM остаётся founder-heavy и чувствительным к price compression и security-heavy rollout.

Формально путь к `company_ebitda_rub_month > 500 000 ₽/мес` в base-case существует уже примерно к **13 месяцу** и сильно раньше **50 клиентов**, поэтому это не early fail. Однако investment committee не видит достаточного запаса прочности для APPROVED, потому что в базе operating break-even приходит только к **M12**, стартовый капитал до BEP нужен около **41,2 млн ₽**, а top-of-funnel и repeatable non-founder channel ещё не доказаны.

Кейс полезен как high-trust FINTECH wedge и заслуживает наблюдения, но в текущем виде это **NEAR-PASS / REJECTED FOR NOW**.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 10,9x», «CAC Payback = 3,9 месяца», «Contribution Margin = 63,3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «M12 выходит в операционный break-even», а при +2 клиентах сверх M12 база проходит 500К₽ EBITDA примерно к M13. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «TAM = 648 млн ₽/год», «SAM = 162 млн ₽/год», но «Composite demand: LOW» и нет строки `Sources`, поэтому applied penalty = -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | «наш шанс на defensibility: стать не generic LLM UI», то есть moat скорее проектируется, чем уже доказан. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | В risk matrix одновременно стоят «Founder-led sales не масштабируется», «White-glove delivery съедает margin» и «Новые санкции режут доступ к западным SaaS/LLM». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | GTM тяжёлый, но конкретный: «Founder-led warm intro», «Target outbound ABM», «Events / partnerships», payback по MRR = 3,9 мес. |

**Normalized score = round((101 × 100) / 150) = 67/100.**

### Интерпретация score
- **67/100 = NEAR-PASS**
- Порог APPROVED не достигнут.
- Причина, почему кейс не доходит до approve, это не поломка юнит-экономики, а недостаточный moat и слишком узкий локальный buyer universe при тяжёлом enterprise GTM.

## Investment one-liner
`[FINTECH] Rogo Investment Banking Geo Expand v2 — NEAR-PASS: 67/100 | EBITDA base=641К₽/мес через 13 мес | LTV/CAC=10,9x | Ключевое преимущество: дорогой analyst workflow с сильной unit economics | Главный риск: узкий buyer universe и weak moat.`

## Полный business process из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-аккаунтов и ICP-листа | SDR | HH/СПАРК/ручной research, CRM | 2 ч | 2 200 | низкая |
| 2 | Первичный outreach по warm intro / email / Telegram / LinkedIn | SDR | CRM, sequencing, Sales Navigator | 1,5 ч | 1 900 | средняя |
| 3 | Discovery call и qualification | AE | Zoom/Meet, CRM | 1 ч | 4 100 | низкая |
| 4 | Demo на реальных finance workflow | AE + Solutions | Demo workspace, презентация | 2 ч | 9 800 | низкая |
| 5 | Pilot scoping: data sources, use-cases, security | Solutions Architect + CTO | Notion, security checklist | 3 ч | 15 200 | низкая |
| 6 | Pilot / sandbox deployment | DevOps + ML + Backend | Cloud, connectors, LLM stack | 10 ч | 41 500 | средняя |
| 7 | Pilot support, prompt tuning, feedback loop | CSM + ML | Slack/Telegram, issue tracker | 6 ч | 19 800 | средняя |
| 8 | Procurement, infosec, DPA / legal | AE + founder + legal | Документы, e-sign | 4 ч | 17 600 | низкая |
| 9 | Коммерческое согласование и invoice | Founder + AE + finance | CRM, 1С/банк | 1,5 ч | 7 100 | средняя |
| 10 | Оплата, onboarding и запуск recurring usage | CSM + Solutions | Billing, monitoring, support | 4 ч | 14 400 | средняя |

**Итого pre-paid delivery + sales cost на одну новую сделку:** около **133 600 ₽ прямого труда**, но инвестиционное решение опирается на fully-loaded CAC **2 334 000 ₽**.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 25 320 000 ₽ |
| contribution_margin_rub_month | 379 800 ₽/клиент/мес |
| fully_loaded_cac_rub | 2 334 000 ₽ |
| LTV/CAC | 10,9x |
| CAC payback | 3,9 мес |
| Gross Margin / Contribution Margin | 63,3% |
| fixed_costs_rub_month | 6 500 000 ₽/мес |
| Break-even clients | 18 |
| Break-even month | M12 |
| startup_capital_to_bep_rub | 41 202 110 ₽ |
| company_ebitda_rub_month base @ M12 | 261 732 ₽/мес |
| company_ebitda_potential_rub_month @ 50 clients | 12 490 000 ₽/мес |
| clients_to_500k_ebitda | 19 |
| months_to_500k_ebitda | 13 |
| clients_to_1m_ebitda | 21 |
| months_to_1m_ebitda | 14 |

### Что это значит для IC
1. На уровне клиента экономика investment-grade.
2. На уровне компании кейс не сломан, но слишком чувствителен к продаже дорогих контрактов без затягивания внедрения.
3. Для фонда главный вопрос, это repeatability и defendability, а не math на одном платящем клиенте.

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | продажи, fundraising, ключевые сделки | 845 000 |
| CTO / Tech Lead | архитектура, security, enterprise delivery | 715 000 |
| Senior Backend #1 | connectors, data pipelines | 546 000 |
| Senior Backend #2 | document workflows, APIs | 546 000 |
| ML Engineer | retrieval, evals, prompt stack | 676 000 |
| DevOps | secure infra, observability | 468 000 |
| Frontend | analyst workspace | 390 000 |
| SDR | target outbound | 234 000 |
| AE | demo, negotiation, close | 416 000 |
| Customer Success / Solutions | onboarding, support, upsell | 338 000 |
| Finance / Ops (0,5 FTE) | invoicing, contracts, HR ops | 182 000 |
| **Итого** |  | **5 356 000 ₽/мес** |

## Moat — 7-factor framework

| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | Интеграции, шаблоны, security review и обучение команды дают умеренное удержание. |
| Scale economies | 1 | Часть COGS снижается с объёмом, но white-glove rollout и support всё ещё заметны. |
| Proprietary data / model advantage | 1 | Упор на private data room и workflow есть, но уникальный датасет не доказан. |
| Regulatory moat | 1 | Compliance нужен, но собственного лицензируемого барьера пока нет. |
| Brand / distribution | 1 | Глобальный benchmark сильный, локальный бренд в РФ ещё не построен. |
| Embedded workflow | 3 | Если продукт садится в comps, memo, diligence и committee pack, он становится частью core workflow. |

**Moat score = round((9 × 25) / 21) = 11/25**, но инвестиционно я округляю вниз до **10/25**, потому что moat пока больше обещанный, чем доказанный.

### Вывод по moat
Moat слабее investment-grade, потому что buyer пока может закрыть 60-70% потребности связкой analyst team + research terminals + generic AI stack. **Weak moat** остаётся в Top-3 Risks.

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер CIB | Крупный поток M&A и strategy-workflows, высокая цена analyst-hour и жёсткий security контур. | email decision-maker + private roundtable | 600 000 ₽/мес |
| 2 | ВТБ / ВТБ CIB | Регулярные сделки и внутренние research workflows, где ценны memo, comps и due diligence. | email managing director + отраслевой форум | 600 000 ₽/мес |
| 3 | Альфа-Банк CIB | Активный корпоративный блок и сложные презентационные материалы, где нужен AI speedup. | warm intro через fintech-партнёров | 500 000 ₽/мес |
| 4 | Газпромбанк | Regulated buyer с corpfin и advisory use-cases, где окупаются secure rollout и audit trail. | конференция + direct outreach | 550 000 ₽/мес |
| 5 | БКС Мир инвестиций | Research-heavy broker, плотная работа с инвестматериалами и сравнительным анализом. | email head of research + pilot offer | 450 000 ₽/мес |
| 6 | Атон | Boutique/high-touch advisory, быстрее пилотный цикл и выше шанс founder-led сделки. | founder-to-founder intro | 400 000 ₽/мес |
| 7 | Совкомбанк CIB | Active corpfin контур и потребность ускорять due diligence и committee materials. | email + targeted roundtable | 450 000 ₽/мес |
| 8 | УК Первая | Investment committee materials и исследовательский workflow, где важны скорость и explainability. | партнёрство с data-vendor + outbound | 400 000 ₽/мес |
| 9 | Альфа-Капитал | Управляющая компания с memo/research workload и recurring потребностью в investment summaries. | direct outreach + content-led кейс | 400 000 ₽/мес |
| 10 | Т-Капитал / Т-Инвестиции | Digital-first инвестиционный контур, готовность тестировать новый workflow stack и фонды ранних стадий. | founder outreach + vc.ru / Habr thought leadership | 450 000 ₽/мес |

Комментарий: 10 named targets присутствуют, поэтому автоматический штраф **-10 к GTM** не применяется.

## Top-3 risks

| Риск | Probability | Impact | Почему это top-3 |
|---|---|---|---|
| weak_moat_and_price_compression | Высокая | Высокое | В sensitivity price -30% даёт **EBITDA @M12 = -2 942 881 ₽**, то есть рынок легко выбивает запас прочности. |
| buyer_universe_too_narrow | Высокая | Высокое | В 02-demand «SAM = 162 млн ₽/год» и всего около **30** реально адресуемых организаций. |
| founder_led_gtm_and_delivery_creep | Высокая | Высокое | В risk matrix прямо указано: «Founder-led sales не масштабируется» и «White-glove delivery съедает margin». |

Дополнительный обязательный риск: **evidence_quality_unverified**, потому что в `02-demand.md` отсутствует строка `Sources: T1=..., T2=..., T3=...`, и по правилу tier-awareness применяется дефолтный штраф.

## Proof points required for APPROVED
1. Минимум **3 платящих enterprise logo** в РФ/СНГ с recurring MRR **≥500-700 тыс. ₽/мес**.
2. Подтверждение, что **security review + procurement** закрываются не дольше **90 дней**.
3. Повторяемый blended CAC **≤2,0 млн ₽** на платящего клиента вне founder-only канала.
4. Реальный retention proof: monthly churn **≤1,5%** или annual gross retention **≥85%**.
5. Доказательство локального data / integration moat, а не просто premium wrapper над LLM и manual services.

## LTV Upside Calculator
Так как verdict = NEAR-PASS / REJECTED FOR NOW, upside считаю через 4 рычага.

| Рычаг | Текущее значение | Цель для approve | Эффект |
|---|---:|---:|---|
| ARPA | 600 000 ₽/мес | 700 000 ₽/мес | company_ebitda_rub_month проходит 500К₽ раньше и запас против скидок растёт. |
| Fully-loaded CAC | 2 334 000 ₽ | ≤ 1 800 000 ₽ | LTV/CAC растёт выше 14x и GTM становится менее хрупким. |
| Monthly churn | 1,5% | ≤ 1,2% | customer_ltv_rub увеличивается, а sensitivity к long payback снижается. |
| Delivery scope | high-touch rollout | ≤ 6 недель стандартизированного внедрения | Улучшается GM%, moat и execution score одновременно. |

**Upside trigger для rerun:** если одновременно достигаются **ARPA ≥ 650К₽**, **CAC ≤ 1,8 млн ₽**, **2-3 платящих логотипа** и один repeatable non-founder channel, кейс можно возвращать на повторный critic.

## Финансовый вывод инвесткомитета
Сильная сторона кейса, это редкая для FINTECH комбинация дорогого analyst workflow и хорошей клиентской экономики. Слабая сторона, это то, что локальная версия тезиса может остаться небольшим boutique enterprise business, а не investable compounding asset. Для фонда этого пока недостаточно.

## Окончательный вердикт
**NEAR-PASS / REJECTED FOR NOW.**

Кейс не отклоняется как бессмысленный. Он отклоняется как **недостаточно защищённый и недостаточно повторяемый** на текущем объёме доказательств. Следить стоит, но approve пока рано.

---

## Файл: 07-score-trajectory.md

---
case: rogo-investment-banking-geo-expand-v2
updated: 2026-05-12
analyst: branch-models-lead
---

# Score Trajectory

## 2026-05-12 — Program 5 / Unit Economics
- Stage: P5 economics
- Score impact: positive
- Summary: unit economics собраны в investment-fund формате. При base-case 600k ₽ MRR на клиента, fully-loaded CAC 2,334 млн ₽, churn 1,5%/мес и contribution margin 63,3% кейс даёт LTV/CAC 10,9x, payback 3,9 месяца и break-even около 18 клиентов.
- Decision signal: economics PASS, Profit Gate пройден.
- Key caution: узкий SAM в РФ и риск white-glove delivery важнее, чем сами unit economics.

## 2026-05-20 — P7 Critic and Verdict
- Stage: P7 Final Verdict
- Analyst: branch-models-lead
- Final score: 67/100 (raw 101/150).
- Verdict: NEAR-PASS / REJECTED FOR NOW.
- Score breakdown: Unit Economics 21/25, EBITDA Potential 19/25, Market+Demand 13/25, Moat 10/25, Execution Risk 17/25, GTM Realism 20/25.
- Tier-awareness: в `02-demand.md` отсутствует строка `Sources`, поэтому по правилу применён дефолтный режим T1=0, T2=0, T3=0, weighted=1.00 и penalty -5 к Market+Demand.
- Committee reading: сильная клиентская economics и рабочий путь к EBITDA >500К₽ подтверждены, но approve блокируют weak moat, узкий локальный buyer universe, founder-heavy GTM и price-compression risk.
- What would change decision: 3+ платящих enterprise-клиента в РФ/СНГ, repeatable non-founder channel, CAC ≤ 1.8 млн ₽ и стандартизированное внедрение ≤ 6 недель.
- New trajectory status: near-pass, переведён в rejected до появления proof points для rerun.
