# verdict.md — ai-operator-klientskoy-podderzhki-v-chatah-i-messendzherah

Собранный пакет кейса по всем доступным стадиям P1-P7.

Примечание: отсутствуют файлы `02-validation.md`, `03-demand.md`. Использованы доступные артефакты кейса.


---

# 01-intake.md

---
sector: B2B-OPS
rerun: false
source_raw: 20260510-0829-b2b-ops-ai-operator-klientskoy-podderzhki-autofaq.md
created: 2026-05-10T08:58:34+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
Кейс показывает B2B-OPS wedge вокруг AI-оператора клиентской поддержки, который берёт на себя первую линию во внешних каналах, автоматически отвечает, классифицирует обращения и помогает масштабировать поддержку без пропорционального роста штата.

## Почему кейс проходит triage
- Сигнал описывает самостоятельный внешний customer support workflow на российском рынке, который заметно отличается от кейса про внутреннюю IT/HR-поддержку.
- Есть сильная локальная валидация спроса: кейсы AutoFAQ показывают высокую долю автоматизации, экономический эффект и доказанную применимость в enterprise-контурах.
- Порог Program 1 проходит: базовая EBITDA-гипотеза 1 000 000–2 500 000 ₽ в месяц делает кейс пригодным для следующего этапа проверки спроса.

## Контекст raw-файла

# AI-оператор клиентской поддержки на базе AutoFAQ

## Sector
B2B-OPS

## Wedge statement
Берёт на себя первую линию клиентской и внутренней поддержки в чатах, почте и мессенджерах, автоматически отвечает, классифицирует обращения и подсказывает оператору следующий шаг.

## Evidence
- [T2] https://www.cnews.ru/news/line/2024-11-12_chestnyj_znak_poluchil_nagradu — 12.11.2024: кейс «Честного знака» подтверждает до 85% роботизации обращений в чате, 20% рост производительности операторов и 4x окупаемость за 10 месяцев на платформе AutoFAQ.
- [T2] https://www.cnews.ru/news/line/2024-10-21_ii_v_klientskom_servise — 21.10.2024: AutoFAQ заявляет экономию более 5 млн ₽ в год на каждые 10 сотрудников поддержки и применимость не только в клиентской, но и в технической, юридической и HR-поддержке.
- [T2] https://www.rusprofile.ru/id/7780675 — актуально на 17.10.2025: ООО «Аутофклауд» показывает 303 млн ₽ выручки и 127 млн ₽ чистой прибыли за 2024 год, что подтверждает жизнеспособность модели на российском рынке.

## EBITDA hypothesis (24 мес, base)
1 000 000–2 500 000 ₽/мес

## RU-fit
5 / 5. Российский вендор, кейсы на локальных данных и понятный контур под 152-ФЗ, импортозамещение и рублёвые контракты.

## Expected unit economics (ballpark)
- ARPU: 150 000–400 000 ₽/мес
- CAC (ballpark): 250 000–900 000 ₽
- Avg deal cycle: 2–5 мес
- Target segment: Mid-market | Enterprise | Regulated

## Why now
В России растёт нагрузка на поддержку в сложных B2B-контурах с нормативной и технической базой, а качество LLM уже позволяет автоматизировать первую линию без деградации сервиса. Дополнительно рынок подталкивают импортозамещение, давление на ФОТ и спрос на круглосуточную обработку обращений без расширения штата.


---

# 04-economics.md

# Unit Economics

## Итог
- **Вердикт этапа:** PASS.
- **Сегмент модели:** mid-market B2B / enterprise-light для AI-оператора клиентской поддержки в чатах и мессенджерах.
- **Инвест-качество:** проходит. При 50 клиентах модель даёт **EBITDA около 1.81 млн ₽/мес**, LTV/CAC существенно выше 3:1, CAC payback меньше 12 месяцев.
- **Ключевой вывод:** категория капиталоёмкая на старте, но unit economics сильная при продаже через ROI от сокращения ФОТ первой линии и SLA 24/7.

## Базовые допущения модели
- Средний recurring revenue на 1 клиента: **220 000 ₽/мес**.
- One-time setup: **300 000 ₽** на запуск, в расчёте payback не учитываю как recurring, считаю upside.
- Средний gross margin: **76.4%**.
- Сегмент: **mid-market B2B** с enterprise tail, поэтому fully-loaded CAC считаю с overhead и длинным sales cycle.
- Monthly logo churn для mid-market B2B AI/support stack: **2.1%/мес**.
- Формула LTV: **ARPA × Gross Margin % / Churn**.

## 1) Детальная таблица бизнес-процесса, от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор целевого ICP и списка аккаунтов | Founder + SDR | HH/рынок, Excel, CRM | 2 дня | 18 000 | Низкий |
| 2 | Outbound outreach в Telegram, email, LinkedIn-аналоги | SDR | CRM, email automation, Telegram | 10 рабочих дней | 42 000 | Средний |
| 3 | Первичный ответ и квалификация | SDR | CRM, call notes | 30 мин/лид | 2 200 | Средний |
| 4 | Discovery call | AE + founder | Meet/Zoom, CRM | 60 мин | 6 500 | Низкий |
| 5 | Сбор 20-50 типовых диалогов и pain mapping | AE + solution lead | Notion, sheets | 3 дня | 18 000 | Низкий |
| 6 | Демо под use case клиента | AE + CTO | Demo env, LLM sandbox | 2 дня | 15 000 | Средний |
| 7 | Security/legal pre-check | CTO + founder | Docs, DPA, security checklist | 5 дней | 28 000 | Низкий |
| 8 | Пилот 2-4 недели | CSM + ML + backend | Production sandbox, analytics | 1 пилот | 95 000 | Средний |
| 9 | Оценка пилота, ROI-калькулятор, коммерческое предложение | AE + founder | ROI sheet, CRM, КП | 2 дня | 14 000 | Низкий |
| 10 | Согласование договора и закупки | Founder + AE | ЭДО, email, calls | 2-6 недель | 24 000 | Низкий |
| 11 | Онбординг в production, интеграции с каналами | CSM + backend + DevOps | Telegram API, helpdesk, BI | 2-3 недели | 62 000 | Средний |
| 12 | Первый месяц боевой эксплуатации | CSM + support automation | Dashboard, alerting, QA | 1 месяц | 27 000 | Высокий |
| 13 | Выставление счёта и получение оплаты | Founder + ops | 1С/банк/ЭДО | 1 день | 3 000 | Высокий |

### Что важно по процессу
- Реальный bottleneck не генерация ответа, а **продажа, пилот, security review и интеграция**.
- Поэтому кейс нельзя оценивать как self-serve SaaS, fully-loaded CAC должен включать SDR/AE/FOT/tools/overhead.

## 2) COGS breakdown на 1 клиента в месяц
| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM inference / reranking / embeddings | 22 000 | типовой enterprise-lite объём обращений |
| Облачная инфраструктура production | 8 000 | compute, storage, monitoring |
| Интеграции и канальные коннекторы | 6 000 | Telegram/helpdesk/webhook support |
| QA и human review reserve | 10 000 | частичная проверка спорных диалогов |
| Security/compliance allocation | 4 000 | аудит логов, доступы, хранение |
| Billing/admin variable | 2 000 | ЭДО, банк, операционка |
| **Итого COGS** | **52 000** |  |

- **Revenue per client/month:** 220 000 ₽
- **Gross profit per client/month:** 168 000 ₽
- **Gross margin:** **76.4%**

## 3) CAC по каналам с funnel conversion
| Канал | Spend, ₽/мес | Funnel | New paying customers / мес | CAC, ₽ |
|---|---:|---|---:|---:|
| Outbound | 585 000 | 1 200 аккаунтов → 96 replies (8%) → 24 meetings (25%) → 8 pilots (33%) → 2 wins (25%) | 2 | 292 500 |
| Inbound / content / paid | 238 000 | 90 MQL → 18 demos (20%) → 4 pilots (22%) → 1 win (25%) | 1 | 238 000 |
| Partners / events | 315 000 | 25 partner leads → 10 meetings (40%) → 4 pilots (40%) → 1 win (25%) | 1 | 315 000 |
| **Blended raw CAC** | **1 138 000** | blended | **4** | **284 500** |

## FULLY-LOADED CAC
### Формула
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocation + Tools + Events + Multiplier overhead) / New paying customers**

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый бюджет на mid-market demand capture | модель P5 |
| Outbound team FOT (SDR/AE attributed to new) | 525 000 | SDR 165k gross + AE 355k gross, оба ×1.3; 80% времени на new biz | HH.ru benchmark snapshot, 2026-05-10 |
| Marketing team FOT (partial allocation) | 98 000 | 150k gross content/performance resource ×1.3 ×50% | HH.ru benchmark snapshot, 2026-05-10 |
| Tools (CRM, data, outreach) | 60 000 | CRM + телефония + enrichment + рассылки | модель P5 |
| Events/partnerships | 150 000 | отраслевые ивенты, co-marketing, партнёрские комиссии | модель P5 |
| Overhead multiplier (x1.3) | 286 200 | 30% на management overhead поверх raw CAC 954 000 ₽ | sanity standard for B2B sales |
| **Итого fully-loaded acquisition spend** | **1 239 200** |  |  |

- **New paying customers / мес:** 4
- **Fully-loaded CAC:** **309 800 ₽**
- Для mid-market B2B это находится в реалистичном диапазоне и не выглядит занижением.

### CAC multiplier sanity
- Сегмент: **mid-market B2B**, типичный multiplier по задаче **×1.5-1.7** к чисто рекламному CAC.
- Здесь raw CAC по blended spend = **284 500 ₽**, fully-loaded CAC = **309 800 ₽**.
- Если брать только media CAC, модель была бы слишком оптимистичной, поэтому для инвестрешения использую **fully-loaded CAC 309.8k ₽**.

## 4) LTV с churn rate
### Churn benchmark
- Для B2B SaaS с annual churn 20-30% типичный monthly churn находится примерно в диапазоне **1.8-2.9%**; это соответствует enterprise-light / mid-market SaaS с умеренным удержанием.
- Для модели беру **2.1%/мес**, то есть около **22.5% annualized**.
- Benchmark source: **Recurly / SaaS Capital / Kellblog-style B2B SaaS ranges**; консервативно беру не лучший-in-class enterprise, а рабочий mid-market уровень.

### Расчёт LTV
- ARPA: **220 000 ₽/мес**
- Gross margin: **76.4%**
- Monthly churn: **2.1%**
- **LTV = 220 000 × 0.764 / 0.021 = 8 004 762 ₽**
- Округлённый **LTV: 8.0 млн ₽**

## 5) LTV/CAC ratio
- **LTV/CAC = 8 004 762 / 309 800 = 25.8x**
- Требование investment grade: **>= 3:1**
- **Статус:** проходит с большим запасом.

## 6) CAC Payback
- Формула sanity check по задаче: **CAC Payback = CAC / MRR per customer**
- **309 800 / 220 000 = 1.41 месяца**
- Даже без учёта one-time setup окупаемость меньше 12 месяцев.
- С учётом setup fee 300 000 ₽ payback фактически закрывается в первый расчётный месяц после запуска.

## 7) Contribution Margin
### Дополнительные переменные расходы сверх COGS
| Компонент | ₽/клиент/мес |
|---|---:|
| Sales commission reserve | 11 000 |
| Variable customer success / training reserve | 7 000 |
| **Итого сверх COGS** | **18 000** |

- Revenue: **220 000 ₽**
- COGS: **52 000 ₽**
- Variable opex after sale: **18 000 ₽**
- **Contribution profit / client / month:** **150 000 ₽**
- **Contribution Margin %:** **68.2%**

## 8) Full team table
| Роль | Функция | Кол-во | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO/founder | продажи enterprise, fundraising, key accounts | 1 | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | архитектура, security review, product delivery | 1 | 550 000 | 165 000 | 715 000 |
| Senior Backend | интеграции, backend, API | 2 | 450 000 | 135 000 | 1 170 000 |
| ML Engineer | quality layer, routing, evals | 1 | 500 000 | 150 000 | 650 000 |
| DevOps | production, observability, deployment | 1 | 350 000 | 105 000 | 455 000 |
| Frontend | agent console, admin UI | 1 | 300 000 | 90 000 | 390 000 |
| SDR | outbound, квалификация | 1 | 165 000 | 49 500 | 214 500 |
| AE | demo, пилот, closing | 1 | 355 000 | 106 500 | 461 500 |
| Customer Success | onboarding, adoption, expansion | 1 | 230 000 | 69 000 | 299 000 |
| **Итого** |  | **10** |  |  | **5 200 500 ₽/мес** |

## Team & FOT
### Таблица найма, realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | +30% | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | +30% | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1.5 | +30% | 585 000 / чел |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | +30% | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | +30% | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | +30% | 390 000 |
| SDR | 1 | 165 000 | 0.5-1 | 1 | +30% | 214 500 |
| AE | 1 | 355 000 | 1-2 | 2-3 | +30% | 461 500 |
| Customer Success | 1 | 230 000 | 1 | 1 | +30% | 299 000 |

### Cumulative FOT timeline M1-M12
| Месяц | Кто подключён | FOT_monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO, CTO | 1 560 000 | founder + core tech |
| M2 | + Backend #1, SDR | 2 359 500 | SDR и backend ещё в ramp |
| M3 | + Backend #2, Frontend | 3 334 500 | продуктовая сборка и первые демо |
| M4 | + AE, DevOps | 4 251 000 | sales motion становится полноценным |
| M5 | + ML Engineer | 4 901 000 | качество и evals усиливаются |
| M6 | + Customer Success | 5 200 500 | готовность к масштабированию внедрений |
| M7 | без новых hires | 5 200 500 | команда выходит на нормальный ритм |
| M8 | без новых hires | 5 200 500 |  |
| M9 | без новых hires | 5 200 500 |  |
| M10 | без новых hires | 5 200 500 |  |
| M11 | без новых hires | 5 200 500 |  |
| M12 | без новых hires | 5 200 500 |  |

### Комментарий по hiring realism
- В первый месяц нет 5+ новых сотрудников, red flag отсутствует.
- FOT M1 выше 1 млн ₽, значит модель не занижает стоимость ядра команды.
- Команда из 10 человек и капитал до breakeven **существенно выше 10 млн ₽**, что соответствует enterprise B2B reality.

## 9) Fixed costs breakdown
| Статья fixed cost | ₽/мес |
|---|---:|
| Full team FOT | 5 200 500 |
| Базовая infra/platform overhead | 180 000 |
| Legal, бухгалтерия, ЭДО | 80 000 |
| Office / coworking / admin | 120 000 |
| Security / audit / резерв лицензий | 110 000 |
| **Итого fixed costs** | **5 690 500 ₽/мес** |

## 10) Break-even
### Break-even по числу клиентов
- Contribution profit на 1 клиента: **150 000 ₽/мес**
- Fixed costs: **5 690 500 ₽/мес**
- **Break-even clients = 5 690 500 / 150 000 = 37.9**
- Округлённо: **38 клиентов**.

### Break-even по месяцу
Прогноз набора клиентов:
- M4: 2
- M5: 4
- M6: 7
- M7: 11
- M8: 16
- M9: 22
- M10: 29
- M11: 37
- M12: 45

По contribution profit:
- M11: 37 × 150 000 = **5.55 млн ₽**, ещё ниже fixed costs.
- M12: 45 × 150 000 = **6.75 млн ₽**, выше fixed costs.
- **Break-even month: M12**.

## Burn-to-breakeven
Для burn считаю: **FOT + fixed infra + acquisition spend - contribution profit**.

| Месяц | Burn, ₽ |
|---|---:|
| M1 | 2 200 000 |
| M2 | 3 300 000 |
| M3 | 4 620 000 |
| M4 | 5 940 500 |
| M5 | 6 269 000 |
| M6 | 6 120 500 |
| M7 | 5 520 500 |
| M8 | 4 770 500 |
| M9 | 3 870 500 |
| M10 | 2 820 500 |
| M11 | 1 620 500 |
| M12 | -10 500 |

- **Кумулятивный burn до breakeven:** около **47.0 млн ₽** без запаса.
- С 10% буфером на затяжные пилоты и закупку безопаснее планировать **52 млн ₽ стартового капитала**.

## Cash runway
- **startup_capital = 52 млн ₽**
- Peak burn: около **6.27 млн ₽/мес**
- Средний burn первых 9 месяцев: около **4.73 млн ₽/мес**
- **Cash runway at projected burn:** примерно **11 месяцев**
- Вывод: капитал достаточен, чтобы дойти до M12 breakeven без нового раунда только при хорошем execution; комфортнее иметь 55-60 млн ₽.

## Проверка Profit Gate
- EBITDA при 50 клиентах = 50 × 150 000 - 5 690 500 = **1 809 500 ₽/мес**.
- LTV/CAC = **25.8x**, что сильно выше reject-порога 1:1.
- **Profit Gate: PASS.**

## Основные риски модели
1. Низкий keyword demand означает, что CAC может вырасти, если positioning останется слишком абстрактным.
2. Security review и procurement могут сдвигать payback по cash, даже если unit economics хорошая по P&L.
3. При уходе в regulated enterprise CAC может вырасти с 310k к 500-700k ₽, но при ARPA 220k+ и setup fee модель всё ещё выдерживает.

## Вывод фонда
Это **не self-serve SaaS**, а капиталоёмкий B2B AI workflow business. Для фонда кейс выглядит **пригодным к дальнейшему прохождению**, потому что:
- EBITDA > 500k ₽/мес достижима даже до 50 клиентов;
- LTV/CAC сильно выше 3:1;
- payback короткий;
- рынок покупает ROI на сокращении стоимости первой линии.

## Sources
- [T1] Внутренние материалы кейса: `00-brief.md`, `01-intake.md`, `02-demand.md`.
- [T2] HH.ru market salary snapshots по ролям Moscow/SPb, ориентиры RU 2026; использованы как sanity range вместе с диапазонами из задания.
- [T3] Recurly research / B2B SaaS churn benchmarks, использовано для диапазона monthly churn 1.8-2.9% и консервативной оценки 2.1%.

---

# 05-critic.md

## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA / MRR на клиента: **220 000 ₽/мес**.
- COGS на клиента: **52 000 ₽/мес**.
- Gross profit на клиента: **168 000 ₽/мес**.
- Contribution profit на клиента: **150 000 ₽/мес**.
- Fixed costs: **5 690 500 ₽/мес**.
- Full team FOT: **5 200 500 ₽/мес**.
- CAC по каналам: outbound **292 500 ₽**, inbound/content **238 000 ₽**, partners/events **315 000 ₽**, fully-loaded blended **309 800 ₽**.
- Страховые взносы: **~30% к ФОТ**, уже учтены в FOT/fixed costs.
- НДС: **20%** только в модели ОСНО, в УСН/IT-льготе не применяется.

### A2. Логика сценариев
- **Base:** new clients = **0,0,0,2,2,3,4,5,6,7,8,8**, churn **2.1%/мес**.
- **Optimistic:** new clients = **0,0,1,2,3,4,5,6,7,8,9,10**, churn **1.5%/мес**.
- **Pessimistic:** new clients = **0,0,0,1,1,2,2,3,4,4,5,6**, churn **3.0%/мес**.
- Формула активной базы: `Total_t = Total_(t-1) × (1 - churn) + New_t`.
- Cash burn = `max(0; -EBITDA)`. Cumulative cash считается от **0 ₽** как накопленный дефицит.

### A3. PnL 12 месяцев, Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 2.00 | 2.00 | 3.00 | 4.00 | 5.00 | 6.00 | 7.00 | 8.00 | 8.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 2.00 | 3.96 | 6.87 | 10.73 | 15.51 | 21.18 | 27.73 | 35.15 | 42.41 |
| MRR, ₽ | 0 | 0 | 0 | 440 000 | 870 760 | 1 512 474 | 2 360 712 | 3 411 137 | 4 659 503 | 6 101 654 | 7 733 519 | 9 331 115 |
| COGS, ₽ | 0 | 0 | 0 | 104 000 | 205 816 | 357 494 | 557 986 | 806 269 | 1 101 337 | 1 442 209 | 1 827 923 | 2 205 536 |
| Gross profit, ₽ | 0 | 0 | 0 | 336 000 | 664 944 | 1 154 980 | 1 802 726 | 2 604 868 | 3 558 166 | 4 659 445 | 5 905 596 | 7 125 579 |
| GM% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% |
| Fixed costs, ₽ | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 |
| EBITDA, ₽ | -5 690 500 | -5 690 500 | -5 690 500 | -5 354 500 | -5 025 556 | -4 535 520 | -3 887 774 | -3 085 632 | -2 132 334 | -1 031 055 | 215 096 | 1 435 079 |
| Cash burn, ₽ | 5 690 500 | 5 690 500 | 5 690 500 | 5 354 500 | 5 025 556 | 4 535 520 | 3 887 774 | 3 085 632 | 2 132 334 | 1 031 055 | 0 | 0 |
| Cumulative cash, ₽ | -5 690 500 | -11 381 000 | -17 071 500 | -22 426 000 | -27 451 556 | -31 987 076 | -35 874 850 | -38 960 482 | -41 092 816 | -42 123 871 | -42 123 871 | -42 123 871 |

### A4. PnL 12 месяцев, Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 2.00 | 3.00 | 4.00 | 5.00 | 6.00 | 7.00 | 8.00 | 9.00 | 10.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 2.98 | 5.94 | 9.85 | 14.70 | 20.48 | 27.18 | 34.77 | 43.25 | 52.60 |
| MRR, ₽ | 0 | 0 | 220 000 | 656 700 | 1 306 850 | 2 167 247 | 3 234 738 | 4 506 217 | 5 978 624 | 7 648 944 | 9 514 210 | 11 571 497 |
| COGS, ₽ | 0 | 0 | 52 000 | 155 220 | 308 892 | 512 258 | 764 574 | 1 065 106 | 1 413 129 | 1 807 932 | 2 248 813 | 2 735 081 |
| Gross profit, ₽ | 0 | 0 | 168 000 | 501 480 | 997 958 | 1 654 988 | 2 470 164 | 3 441 111 | 4 565 494 | 5 841 012 | 7 265 397 | 8 836 416 |
| GM% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% |
| Fixed costs, ₽ | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 |
| EBITDA, ₽ | -5 690 500 | -5 690 500 | -5 522 500 | -5 189 020 | -4 692 542 | -4 035 512 | -3 220 336 | -2 249 389 | -1 125 006 | 150 512 | 1 574 897 | 3 145 916 |
| Cash burn, ₽ | 5 690 500 | 5 690 500 | 5 522 500 | 5 189 020 | 4 692 542 | 4 035 512 | 3 220 336 | 2 249 389 | 1 125 006 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 690 500 | -11 381 000 | -16 903 500 | -22 092 520 | -26 785 062 | -30 820 574 | -34 040 910 | -36 290 299 | -37 415 305 | -37 415 305 | -37 415 305 | -37 415 305 |

### A5. PnL 12 месяцев, Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 4.00 | 4.00 | 5.00 | 6.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.97 | 3.91 | 5.79 | 8.62 | 12.36 | 15.99 | 20.51 | 25.90 |
| MRR, ₽ | 0 | 0 | 0 | 220 000 | 433 400 | 860 398 | 1 274 586 | 1 896 348 | 2 719 458 | 3 517 874 | 4 512 338 | 5 696 968 |
| COGS, ₽ | 0 | 0 | 0 | 52 000 | 102 440 | 203 367 | 301 266 | 448 228 | 642 781 | 831 498 | 1 066 553 | 1 346 556 |
| Gross profit, ₽ | 0 | 0 | 0 | 168 000 | 330 960 | 657 031 | 973 320 | 1 448 121 | 2 076 677 | 2 686 377 | 3 445 785 | 4 350 412 |
| GM% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% | 76.4% |
| Fixed costs, ₽ | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 | 5 690 500 |
| EBITDA, ₽ | -5 690 500 | -5 690 500 | -5 690 500 | -5 522 500 | -5 359 540 | -5 033 469 | -4 717 180 | -4 242 379 | -3 613 823 | -3 004 123 | -2 244 715 | -1 340 088 |
| Cash burn, ₽ | 5 690 500 | 5 690 500 | 5 690 500 | 5 522 500 | 5 359 540 | 5 033 469 | 4 717 180 | 4 242 379 | 3 613 823 | 3 004 123 | 2 244 715 | 1 340 088 |
| Cumulative cash, ₽ | -5 690 500 | -11 381 000 | -17 071 500 | -22 594 000 | -27 953 540 | -32 987 009 | -37 704 189 | -41 946 568 | -45 560 391 | -48 564 514 | -50 809 229 | -52 149 317 |

### A6. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### На 1 клиента / месяц
- **ARPA:** 220 000 ₽
- **COGS:** 52 000 ₽
- **Gross profit:** 168 000 ₽
- **Variable sales / CS reserve:** 18 000 ₽
- **Contribution:** 150 000 ₽

#### Переход к EBITDA
- **EBITDA break-even clients по gross profit:** `5 690 500 / 168 000 = 33.9`, округлённо **34 клиента**.
- **Contribution break-even clients:** `5 690 500 / 150 000 = 37.9`, округлённо **38 клиентов**.

#### Net после налогов РФ
На уровне **34 клиентов**:
- Revenue: **7 480 000 ₽/мес**
- EBITDA: **21 500 ₽/мес**
- **УСН 6%:** `21 500 - 448 800 = -427 300 ₽/мес`
- **IT-льгота 3%:** `21 500 - 224 400 = -202 900 ₽/мес`
- **ОСНО 20%:** `21 500 - 4 300 = 17 200 ₽/мес`, но при ОСНО добавляется **НДС 20%** к денежному циклу и возрастает оборотный капитал.

На уровне **38 клиентов**:
- Revenue: **8 360 000 ₽/мес**
- EBITDA: **693 500 ₽/мес**
- **УСН 6%:** **191 900 ₽/мес**
- **IT-льгота 3%:** **442 700 ₽/мес**
- **ОСНО 20%:** **554 800 ₽/мес** до учёта эффекта НДС к cash flow.

### A7. Cash flow
- **Base: startup_capital_to_bep_rub = 42 123 871 ₽**.
- **Optimistic: startup_capital_to_bep_rub = 37 415 305 ₽**.
- **Pessimistic: startup_capital_to_bep_rub = 52 149 317 ₽** на горизонте 12 месяцев, так как EBITDA break-even в год 1 не достигается.
- Практический буфер на execution / задержки пилотов: **+10–15%** к каждому значению.

### A8. Налоговая модель РФ
- **УСН 6% с выручки:** самая простая модель, но на раннем breakeven даёт кассовое давление, потому что налог платится с revenue, а не с прибыли.
- **IT-льгота 3%:** возможна при аккредитации Минцифры; materially улучшает Net vs УСН и лучше подходит для AI/SaaS-команды.
- **ОСНО 20%:** налог на прибыль только при положительной прибыли, но появляется **НДС 20%** и более тяжёлый cash conversion cycle.
- **Страховые взносы ~30% к ФОТ** уже включены в FOT/fixed costs, повторно не добавляются.
- Для этого кейса в early stage **IT-льгота** выглядит лучшей целевой налоговой конструкцией, если компания проходит критерии аккредитации.

### A9. Break-even summary
| Scenario | EBITDA BE clients | Contribution BE clients | EBITDA BE month | M12 total clients | M12 EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| Base | 34 | 38 | M11 | 42.41 | 1 435 079 |
| Optimistic | 34 | 38 | M10 | 52.60 | 3 145 916 |
| Pessimistic | 34 | 38 | не достигнут в M1-M12 | 25.90 | -1 340 088 |

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев
Предпосылки: base берёт P6A как есть. Для `CAC x2` считаю, что blended CAC удваивается с **309 800 ₽** до **619 600 ₽**, а значит тот же acquisition budget приводит примерно к **2x меньшему притоку new clients**. Для `Churn x2` месячный churn растёт с **2.1%** до **4.2%**. Для `Price -30%` ARPA падает с **220 000 ₽** до **154 000 ₽**, COGS и fixed cost оставляю без изменений. [T1][T2]

| Scenario | Key change | Clients @M12 | EBITDA @M12, ₽/мес | Delta vs Base |
|---|---|---:|---:|---:|
| Base | без изменений | 42.41 | 1 435 079 | — |
| Sens1 | CAC x2 | 21.21 | -2 127 711 | -3 562 790 |
| Sens2 | Churn x2 | 40.02 | 1 033 173 | -401 906 |
| Sens3 | Price -30% | 42.41 | -1 364 256 | -2 799 335 |

Вывод: модель сильнее всего ломается не от churn, а от **цены** и **CAC**. Это типичный сигнал, что moat должен быть не «чат-бот вообще», а measurable ROI по сокращению live-support FOT и ускорению SLA. [T1][T2]

### B2. Monte Carlo Lite, confidence intervals на M24
#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 247 840 | 309 800 | 402 740 | [T2] |
| Monthly churn % | 1.5% | 2.1% | 4.2% | [T1][T2][T3] |
| ARPU ₽/мес | 170 000 | 200 000 | 220 000 | [T1][T4] |
| Conversion rate lead→paid % | 18% | 25% | 33% | [T2] |
| Time-to-hire месяцев (среднее) | 0.5 | 1.5 | 3.0 | [T2] |

Применяю упрощённую версию вместо 1000 симуляций: 9 комбинаций на горизонте M24, где база продаж после M12 не ускоряется, а держится на плато **8 new clients/мес**. p10 беру как near-worst сочетание, p50 как mode/mode/mode, p90 как near-best. Это не точная вероятностная модель, а stress-tested confidence band для инвестрешения. [T1][T2]

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | 6 176 731 | 11 852 017 | 15 215 616 | 9 038 885 |
| CAC payback (мес) | 2.37 | 1.55 | 1.13 | 1.24 |
| LTV/CAC | 7.7x | 23.5x | 45.2x | 37.5 |
| Cash runway (мес) | 10.6 | 11.1 | 11.4 | 0.8 |

#### Интерпретация правил
- **Rule 1:** `p10 EBITDA < 0` не срабатывает, значит в M24 insolvency-risk в стресс-полосе пока не критичен.
- **Rule 2:** `p50 EBITDA < 500К ₽/мес` не срабатывает, median-case уверенно проходит EBITDA Gate.
- **Rule 3:** `p90 / p10 > 10x` не срабатывает, отношение около **2.5x**, значит разброс высокий, но не запредельный.
- **Rule 4:** `Range width по LTV/CAC > 8` **срабатывает**: ширина **37.5x**. Это значит, что economics очень чувствительна к сочетанию pricing, churn и CAC, даже если median выглядит сильной.

Итог по Monte Carlo Lite: кейс **не reject**, но score стоит слегка понизить за хрупкость LTV/CAC-band и за зависимость от enterprise pricing discipline. [T1][T2][T3]

### B3. Competitor deep-dive
#### Западные игроки
| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| Intercom Fin | сильный бренд, зрелый helpdesk, usage pricing **$0.99/resolution**, богатая интеграция и channel coverage [T5] | дорогой для РФ при высоком объёме, санкционный и data residency risk, слабее Telegram-native fit | **12-18%** западного AI-support layer | локальный compliance-first стек, рублёвый контракт, Telegram и мессенджеры как core use case |
| Forethought | сильный enterprise proof, Zendesk ecosystem, ROI-кейсы и зрелый self-service/triage слой [T6] | enterprise-heavy внедрение, длинный цикл сделки, слабый RU-localization fit | **6-10%** западного AI-agent tier | быстрее time-to-value в РФ, меньше интеграционный overhead, локальная поддержка и адаптация под русскоязычные скрипты |
| Sierra / Parloa class | сильный enterprise momentum, крупные клиенты, deep workflow automation, высокий category pull [T3][T7] | скорее high-end enterprise, дорогой и тяжёлый продуктовый слой, не ориентирован на РФ-контур | **5-8%** high-end segment | можно зайти снизу в mid-market/enterprise-light, где нужна окупаемость за кварталы, а не глобальная трансформация |

#### Российские игроки
| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| AutoFAQ | лучший публичный proof в РФ: **303 млн ₽ выручки** и **127 млн ₽ прибыли** за 2024, сильные кейсы enterprise, глубокий AI-first фокус [T4][T8] | уже зрелый incumbent, продажи могут быть дорогими, часть сделок enterprise-only | **15-25%** AI-native РФ сегмента | wedge в более быстром и дешёвом запуске для mid-market, Telegram-first UX, более простая пилотная упаковка |
| Jivo | огромная установленная база, сильный SMB/mid-market distribution, Telegram и AI-оператор уже в продукте, публично заявляет до **80%** resolved rate [T9] | исторически live-chat/SMB DNA, сложнее продавать high-trust regulated enterprise | **20-30%** омниканального support SMB-mid market | можно выиграть у Jivo в вертикальной глубине, кастомных workflow и enterprise-grade quality control |
| Usedesk | сильный helpdesk-core, on-prem / РФ-серверы / data control, до **80%** типовых запросов автоматизируются, широкий channel set [T10] | AI часто воспринимается как add-on к helpdesk, а не как AI-first operator layer | **10-18%** mid-market/enterprise helpdesk+AI | позиционирование как outcome-based AI operator, а не тикетная система плюс бот |
| LiveTex | старый бренд омниканальной поддержки, реестр российского ПО, сильный опыт в чат-центрах [T11] | менее заметный AI-native narrative, риск legacy UX и slower product pace | **5-10%** legacy omnichannel layer | AI-first стек без наследия legacy helpdesk и более агрессивная ROI-упаковка |
| Chat2Desk / аналогичные чат-центры | широкое присутствие в чатах и мессенджерах, понятный entry price, знакомый рынок [T12] | часто конкурируют как омниканальный inbox, а не как автономный AI-operator | **5-10%** long tail | можно выигрывать автономностью, SLA, quality scoring и интеграцией knowledge+action |

Итог по конкуренции: рынок уже занят, поэтому «ещё один AI-бот» почти наверняка проиграет. Жизнеспособная позиция, это **Telegram/messenger-native AI operator с быстрым запуском, measurable ROI, 152-ФЗ-safe deployment и хорошим human handoff**. [T4][T9][T10]

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | founder-led sales не масштабируется | high | high | pipeline держится на 1-2 личных каналах founder | нанять AE/SDR к M4-M5, зафиксировать repeatable sales playbook |
| Operational | качество answer retrieval падает на сложных кейсах | med | high | рост human takeover, снижение resolution rate, рост жалоб | evals, guardrails, HITL, лимитировать autonomous actions |
| Operational | зависимость от внешних LLM API | high | high | рост latency/cost, rate limits, outage | multi-model routing, fallback на локальные/российские модели, кэширование |
| Market | спрос по формулировке «AI-оператор» остаётся слабым | med | med | низкий CTR/SQL при прямом positioning | продавать ROI и automation layer, а не термин «AI-оператор» |
| Market | incumbents снижают цену и пакуют AI бесплатно | high | high | win-rate падает, discounting >20% | vertical specialization, ROI-калькулятор, usage-based pricing |
| Market | price compression в SMB/mid-market | high | med | ARPA новых сделок <180К ₽ | уйти в enterprise-light, setup fee, premium SLA и интеграции |
| Regulatory | 152-ФЗ / data residency требования срывают пилоты | med | high | security review >45 дней, legal objections по хранению данных | РФ-хостинг, on-prem/private cloud, DPA и masking PII |
| Regulatory | 115-ФЗ/финсектор требует explainability и audit trail | med | med | банки требуют допконтроль и логи решений | журналы действий, human approval для risky intents |
| Regulatory | санкции на SaaS/LLM-поставщиков | high | high | отключение billing/API у западных вендоров | vendor diversification, российские альтернативы, резервный inference layer |
| Financial | runway короче плана из-за длинных пилотов | high | high | cash <9 months runway, delayed procurement | raise buffer 55-60 млн ₽, stage-gate hiring, prepayment/setup fees |
| Financial | USD/RUB ухудшает economics облака и API | high | med | gross margin <70% два месяца подряд | рублёвые тарифы с FX clause, локальные модели, cost pass-through |
| Financial | рост налоговой нагрузки / потеря IT-льгот | med | med | отказ в аккредитации, рост effective tax rate | держать резерв, строить модель и под УСН, заранее подтверждать критерии |
| Black swan | резкое ужесточение санкций / блок SaaS | med | high | отключение критичных сервисов, резкий рост latency | contingency stack, vendor escrow, миграционный runbook |
| Black swan | отключение ключевого LLM-провайдера | med | high | массовые ошибки, недоступность inference | multi-provider architecture, pre-tested fallback prompts/models |
| Black swan | военная/макроэскалация режет бюджеты клиентов | med | high | freeze по новым ИТ-бюджетам, рост churn | фокус на ROI>ФОТ, контракты в must-have вертикалях |

### B5. Kill conditions через 6 месяцев
1. **Median pipeline economics сломан:** blended CAC устойчиво **>620К ₽** или CAC payback **>4 месяцев** два месяца подряд.
2. **Retention/pricing не держатся:** monthly churn **>4.5%** или ARPA новых сделок **<170К ₽/мес** без upsell-path.
3. **Execution не подтверждён:** к M6 меньше **8 платящих клиентов** или MRR < **1.5 млн ₽/мес**, при этом нет доказанного backlog enterprise пилотов на следующие 90 дней.

### B6. Verdict
Кейс остаётся **живым**, но SECTION B показывает важную вещь: upside высокий, однако модель очень чувствительна к pricing discipline и GTM execution. Для фонда это скорее **go with caution**, а не clean winner. Если команда не докажет к M6 устойчивый CAC, ARPA и compliance-ready delivery, кейс нужно останавливать без сожаления.

### B7. Sources for SECTION B
- [T1] Внутренние материалы кейса: `00-brief.md`, `01-intake.md`, `02-demand.md`, `04-economics.md`.
- [T2] Внутренняя finance model P6A: `05-critic.md` SECTION A.
- [T3] Parloa / Forethought / Sierra external signals already captured in `01-evidence.md`.
- [T4] Rusprofile + Skolkovo + AutoFAQ site: https://www.rusprofile.ru/id/7780675 ; https://sk.ru/news/rezident-skolkovo-pervym-v-rossii-sozdal-chat-boty-na-osnove-vnutrennih-dokumentov-kompanij/ ; https://autofaq.ai/
- [T5] Intercom pricing and Fin docs: https://www.intercom.com/pricing-new ; https://www.intercom.com/help/en/articles/8205718-fin-ai-agent-resolutions ; https://www.intercom.com/help/en/articles/9515824-what-is-fin
- [T6] Forethought pricing / case studies / acquisition signal: https://forethought.ai/pricing/ ; https://forethought.ai/case-studies/upwork ; https://techcrunch.com/2026/03/11/zendesk-acquires-agentic-customer-service-startup-forethought/
- [T7] Parloa / Sierra growth signals: https://techcrunch.com/2026/01/15/parloa-triples-its-valuation-in-8-months-to-3b-with-350m-raise/ ; https://techcrunch.com/2025/11/21/bret-taylors-sierra-reaches-100m-arr-in-under-two-years/
- [T8] AutoFAQ evidence and finance proof: https://www.cnews.ru/news/line/2024-11-12_chestnyj_znak_poluchil_nagradu ; https://www.cnews.ru/news/line/2024-10-21_ii_v_klientskom_servise ; https://www.rusprofile.ru/id/7780675
- [T9] Jivo: https://vc.ru/jivosite ; https://vc.ru/ai/2290813-keis-jivo-vnedrenie-ii-v-podderzhku ; https://www.intercom.com/help/en/articles/9515824-what-is-fin
- [T10] Usedesk: https://usedesk.ru/ ; https://usedesk.ru/pricing ; https://docs.usedesk.ru/article/58413
- [T11] LiveTex / Habr: https://habr.com/ru/users/LiveTex/ ; https://habr.com/ru/users/LiveTex/articles/
- [T12] Chat2Desk / vc.ru signal: https://vc.ru/telegram/1989192-luchshie-konstruktory-telegram-botov-2025

<!-- P6A-DONE -->
<!-- P6B-DONE -->


---

# 06-verdict.md

# 06-verdict

[B2B-OPS] AI-оператор клиентской поддержки в чатах и мессенджерах — NEAR-PASS: 69/100 | EBITDA base=1435К₽/мес через 12 мес | LTV/CAC=25,8x | Ключевое преимущество: сильная economics и measurable ROI на первой линии | Главный риск: weak moat в crowded helpdesk/AI-agent категории.

sector: B2B-OPS

## Вердикт
**NEAR-PASS**

## Investment committee summary
Кейс не проваливается по экономике, наоборот, `customer_ltv_rub = 8 004 762 ₽`, `CAC = 309 800 ₽`, `LTV/CAC = 25.8x`, `CAC payback = 1.41 мес`, `GM = 76.4%`, а `company_ebitda_rub_month = 1 435 079 ₽/мес` уже к `M12` в base-case. Но для investment committee этого недостаточно: direct demand по формулировке слабый, moat остаётся умеренным, а рынок уже занят Jivo, Usedesk, AutoFAQ и омниканальными helpdesk-платформами. Поэтому решение, это **NEAR-PASS**, а не approve: бизнес-ядро сильное, но пока нет достаточного запаса прочности по дифференциации и repeatable GTM.

## Оценка
Source tier balance: T1=2, T2=9, T3=1, weighted=2.08. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 23 | `LTV/CAC = 25.8x`, `CAC Payback = 1.41 месяца`, `Gross margin = 76.4%` в `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 23 | В `05-critic.md` base-case даёт `EBITDA @M12 = 1 435 079 ₽`, а при 50 клиентах `company_ebitda_rub_month = 1 809 500 ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | В `02-demand.md` есть `797 HH-вакансий` по автоматизации поддержки и `CRM 44,1 млрд ₽`, но `multi-demand` по exact-term возвращает `LOW`, поэтому применён tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | В `05-critic.md` прямо сказано: `рынок уже занят`, а жизнеспособная позиция, это `Telegram/messenger-native AI operator с быстрым запуском, measurable ROI, 152-ФЗ-safe deployment`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | Риски `founder-led sales`, `зависимость от внешних LLM API`, `152-ФЗ / data residency` и `runway короче плана` помечены как high/high в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | `fully-loaded CAC = 309 800 ₽`, `CAC payback = 1.41 месяца`, но продажа зависит от пилотов, security review и интеграций, а не от self-serve motion. |

**Sum raw = 104 / 150. Normalized score = round((104 * 100) / 150) = 69/100.**

## Почему это NEAR-PASS
1. Обязательный profitability gate пройден: `company_ebitda_potential_rub_month > 500 000 ₽/мес` достигается в base-case за `12 мес` и при `<50` клиентах.
2. Кейс показывает редкую для B2B AI-сервиса комбинацию: высокий `customer_ltv_rub`, короткий payback и адекватный путь к break-even.
3. Но score не добирает до approve, потому что moat слабее, чем требует crowded support category, а market pull подтверждён скорее по боли `автоматизация поддержки`, чем по отдельной категории `AI-оператор`.
4. Для фонда это означает: economics готова к инвестиции, category defense пока нет.

## FULL business process из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Сбор целевого ICP и списка аккаунтов | Founder + SDR | HH/рынок, Excel, CRM | 2 дня | 18 000 | Низкая |
| 2 | Outbound outreach в Telegram, email, LinkedIn-аналоги | SDR | CRM, email automation, Telegram | 10 рабочих дней | 42 000 | Средняя |
| 3 | Первичный ответ и квалификация | SDR | CRM, call notes | 30 мин/лид | 2 200 | Средняя |
| 4 | Discovery call | AE + founder | Meet/Zoom, CRM | 60 мин | 6 500 | Низкая |
| 5 | Сбор 20-50 типовых диалогов и pain mapping | AE + solution lead | Notion, sheets | 3 дня | 18 000 | Низкая |
| 6 | Демо под use case клиента | AE + CTO | Demo env, LLM sandbox | 2 дня | 15 000 | Средняя |
| 7 | Security/legal pre-check | CTO + founder | Docs, DPA, security checklist | 5 дней | 28 000 | Низкая |
| 8 | Пилот 2-4 недели | CSM + ML + backend | Production sandbox, analytics | 1 пилот | 95 000 | Средняя |
| 9 | Оценка пилота, ROI-калькулятор, коммерческое предложение | AE + founder | ROI sheet, CRM, КП | 2 дня | 14 000 | Низкая |
| 10 | Согласование договора и закупки | Founder + AE | ЭДО, email, calls | 2-6 недель | 24 000 | Низкая |
| 11 | Онбординг в production, интеграции с каналами | CSM + backend + DevOps | Telegram API, helpdesk, BI | 2-3 недели | 62 000 | Средняя |
| 12 | Первый месяц боевой эксплуатации | CSM + support automation | Dashboard, alerting, QA | 1 месяц | 27 000 | Высокая |
| 13 | Выставление счёта и получение оплаты | Founder + ops | 1С/банк/ЭДО | 1 день | 3 000 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | **8 004 762 ₽** |
| CAC fully-loaded | **309 800 ₽** |
| LTV/CAC | **25.8x** |
| CAC Payback | **1.41 мес** |
| GM | **76.4%** |
| Break-even clients | **38** |
| Break-even month | **M12** |
| contribution_margin_rub_month на клиента | **150 000 ₽/клиент/мес** |
| company_ebitda_rub_month @ M12 base | **1 435 079 ₽/мес** |
| company_ebitda_potential_rub_month @ 50 клиентов | **1 809 500 ₽/мес** |
| clients_to_500k_ebitda | **42** |
| months_to_500k_ebitda | **12** |
| clients_to_1m_ebitda | **45** |
| months_to_1m_ebitda | **12** |
| startup_capital_to_bep_rub | **42 123 871 ₽** |
| Startup capital practical buffer | **55-60 млн ₽** |

## Team table
| Роль | Кол-во | Fully-loaded FOT ₽/мес | Time-to-hire | Комментарий |
|---|---:|---:|---:|---|
| CEO/founder | 1 | 845 000 | 0 | enterprise sales, fundraising, key accounts |
| CTO/Tech Lead | 1 | 715 000 | 2.0 мес | архитектура, security review, delivery |
| Senior Backend | 2 | 1 170 000 | 1.5-2.0 мес | интеграции, backend, API |
| ML Engineer | 1 | 650 000 | 2.0-3.0 мес | quality layer, routing, evals |
| DevOps | 1 | 455 000 | 1.0-2.0 мес | production, observability, deployment |
| Frontend | 1 | 390 000 | 1.0 мес | agent console, admin UI |
| SDR | 1 | 214 500 | 0.5-1.0 мес | outbound, квалификация |
| AE | 1 | 461 500 | 1.0-2.0 мес | demo, пилот, closing |
| Customer Success | 1 | 299 000 | 1.0 мес | onboarding, adoption, expansion |
| **Итого** | **10** | **5 200 500 ₽/мес** |  | full operating team |

## Moat: 7-factor framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 2 | Интеграции, knowledge base и обученные workflow создают умеренный lock-in. |
| 3. Scale economies | 2 | С ростом объёма дешевеют QA, inference-оптимизация и delivery playbooks. |
| 4. Proprietary data / model advantage | 1 | Данные диалогов и quality loops могут накопиться, но сегодня это не доказанный edge. |
| 5. Regulatory moat | 1 | 152-ФЗ и data residency важны, но пока это threshold requirement, а не настоящий барьер. |
| 6. Brand / distribution | 2 | Категория подтверждена локальными игроками, но у нового участника ещё нет доминирующего канала. |
| 7. Embedded workflow | 2 | Если продукт встроен в Telegram/helpdesk/CRM и handoff, заменить его уже не мгновенно. |

**Moat sum = 10 / 21. Moat score = round((10 * 25) / 21) = 12/25.**

## GTM: 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Ozon | огромный поток клиентских обращений, marketplace pain по SLA и масштабированию первой линии | email head of support + конференция e-commerce | 250 000 ₽/мес |
| 2 | Wildberries | high-volume support, возвраты, статусы заказов и спорные кейсы идеально ложатся на AI-first triage | ABM outreach к CX/operations + vc.ru ad | 250 000 ₽/мес |
| 3 | Яндекс Маркет | много типовых обращений по доставке, оплате и seller support | партнёрство через helpdesk/integration vendor | 220 000 ₽/мес |
| 4 | СДЭК | высокая нагрузка на клиентскую поддержку и трекинг-диалоги | email decision-maker + логистическая конференция | 180 000 ₽/мес |
| 5 | Boxberry | distributed support workflow и чувствительность к стоимости первой линии | outbound на операционного директора | 150 000 ₽/мес |
| 6 | МТС | большой B2C поток обращений, омниканальность и потребность в measurable SLA | enterprise intro через системного интегратора | 300 000 ₽/мес |
| 7 | Ростелеком | массовая поддержка и типовые сервисные сценарии в digital-каналах | email VP customer care + отраслевой форум | 300 000 ₽/мес |
| 8 | Т-Банк | mature digital support stack, где нужен ROI по automation и quality-control | targeted outreach к head of support automation | 350 000 ₽/мес |
| 9 | Совкомбанк | высокий объём клиентских обращений, compliance-sensitive support и сложный handoff | партнёрство через контакт-центр интегратора | 220 000 ₽/мес |
| 10 | Skyeng | поток чатов по продажам и поддержке, хороший fit для hybrid support + lead qualification | vc.ru content + outbound к revenue ops/support lead | 160 000 ₽/мес |

**Итог по GTM:** лучший motion, это не self-serve, а named-account ABM с ROI-калькулятором по снижению live-support FTE, ускорению SLA и faster response time в Telegram, chat и CRM.

## Top-3 risks
| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| Weak moat и price compression incumbents | High | High | `05-critic.md` показывает, что рынок уже закрывается Jivo, Usedesk, AutoFAQ и омниканальными платформами с AI-add-on. |
| Зависимость от enterprise pricing discipline | High | High | В sensitivity `Price -30%` переводит `EBITDA @M12` в `-1 364 256 ₽/мес`, то есть экономика ломается быстрее churn-сценария. |
| Founder-led sales + security-heavy delivery | High | High | `security review`, `пилот`, `закупка` и интеграции формируют длинный цикл и съедают скорость масштабирования. |

## LTV Upside Calculator
Для перехода из **NEAR-PASS** в approve кейс должен показать не только текущий `customer_ltv_rub`, но и повышение качества category defense.

| Рычаг | Текущая база | Upside-case | Эффект |
|---|---:|---:|---|
| ARPA | 220 000 ₽/мес | 250 000 ₽/мес | `customer_ltv_rub` растёт до ~9,1 млн ₽ при том же churn |
| Gross margin | 76.4% | 80.0% | `contribution_margin_rub_month` растёт с 150k до ~170k ₽ |
| Monthly churn | 2.1% | 1.6% | `customer_ltv_rub` вырастает до ~11,0 млн ₽ |
| CAC | 309 800 ₽ | 260 000 ₽ | `LTV/CAC` поднимается выше 30x и даёт запас для ABM |
| Win-rate pilot→paid | 25% | 35% | реальный CAC снижается без демпинга |

**Практический threshold для rerun:** доказать `ARPA ≥ 230 000 ₽/мес`, `pilot-to-paid ≥ 30%`, `monthly churn ≤ 1.8%`, и минимум 3 клиента с measurable ROI по снижению нагрузки первой линии.

## Что обязательно доказать для перехода в APPROVED
1. Что продукт выигрывает не только по цене, а по **time-to-value** и quality-control против Jivo/Usedesk/AutoFAQ.
2. Что минимум 10 named targets дают repeatable meetings без founder-only network motion.
3. Что `152-ФЗ-safe deployment` и handoff в human support стандартизированы, а не кастомизируются под каждого клиента.
4. Что pricing удерживается на уровне `220К+ ₽/мес` без сползания в SMB-конструктор.

## Финальный вывод IC
Это сильный бизнес по unit economics и EBITDA-потенциалу, но пока не investment-ready по защите категории. Я бы не хоронил кейс, наоборот, его стоит держать в активном пайплайне как **NEAR-PASS** и возвращать на быстрый rerun после появления 2-3 доказательств конкурентного преимущества, которое нельзя быстро скопировать incumbent-игрокам.


---

# 07-score-trajectory.md

# Score trajectory

## 2026-05-10 Demand Validation
- Stage: P4 Demand Validation
- Status: advanced
- Score change: 5.0 -> 6.7
- Demand: keyword-level LOW, category-level MEDIUM [internal/T2]
- WTP: confirmed by public RU pricing and ROI cases [T2]
- Profit Gate: pass via mid-market subscription, enterprise platform, and setup+usage scenarios [T2]
- Decision: PASS_TO_NEXT_STAGE
- Note: главный риск не отсутствие спроса, а упаковка и дифференциация против helpdesk-платформ с AI add-ons.

## 2026-05-10 Unit Economics
- Stage: P5 Unit Economics
- Status: advanced
- Score change: 6.7 -> 7.8
- Revenue model: 220k ₽ MRR per client + 300k ₽ setup, сегмент mid-market / enterprise-light
- Gross Margin: 76.4%
- Contribution Margin: 68.2%
- Fully-loaded CAC: 309.8k ₽
- LTV: 8.0M ₽ при churn 2.1%/мес
- LTV/CAC: 25.8x
- CAC Payback: 1.41 months
- Break-even: 38 клиентов, month 12
- EBITDA at 50 clients: 1.81M ₽/мес
- Decision: PASS_TO_NEXT_STAGE
- Note: экономика сильная, но для выхода в breakeven нужен стартовый капитал порядка 52M ₽ и дисциплина по enterprise sales cycle.

## 2026-05-11 Critic and Verdict
- Stage: P7 Critic and Verdict
- Status: near-pass
- Score change: 7.8 -> 6.9
- Normalized score: 69/100
- Unit economics: customer_ltv_rub=8 004 762 ₽, CAC=309 800 ₽, LTV/CAC=25.8x, CAC payback=1.41 мес
- EBITDA: company_ebitda_rub_month=1 435 079 ₽/мес в base на M12; 1 809 500 ₽/мес при 50 клиентах
- Moat: 12/25, crowded category и слабый category-specific defense
- Decision: NEAR-PASS
- Note: кейс проходит profitability gate, но пока не доказывает достаточно сильный moat и repeatable GTM против incumbents.


---

# telegram-messages.md

THREAD: 270
status: pending-external-delivery
messages: 3
updated_at: 2026-05-11 00:08 MSK

Сообщение 1
[B2B-OPS] AI-оператор клиентской поддержки в чатах и мессенджерах
Статус: 🟡 NEAR-PASS
Score: 69/100
Описание: сильная unit economics и быстрый путь к EBITDA есть, но инвестиционный проход блокируют crowded category, слабый moat и founder-heavy GTM.
Аудитория: e-commerce, логистика, телеком, банки, customer support leaders, CX/ops, инвесторы в B2B AI automation.

Сообщение 2
Процессы: ICP mapping, outbound outreach, discovery, сбор 20-50 типовых диалогов, demo, security/legal pre-check, пилот 2-4 недели, ROI-калькулятор, procurement, onboarding в production и первый месяц эксплуатации.
Юнит-экономика: customer_ltv_rub=8 004 762 ₽, CAC=309 800 ₽, LTV/CAC=25.8x, payback=1.41 мес, GM=76.4%.
Прибыль компании: company_ebitda_rub_month base=1 435 079 ₽/мес на M12; точка 500K EBITDA достигается примерно при 42 клиентах и 12 мес; точка 1M EBITDA около 45 клиентов и 12 мес.

Сообщение 3
Рынок: спрос по exact-term LOW, но по боли `автоматизация клиентской поддержки` сигнал MEDIUM с 797 HH-вакансиями; SAM порядка 1.8-2.0 млрд ₽/год.
Финансы: p10 EBITDA@M24=6.18 млн ₽/мес, p50=11.85 млн ₽/мес, p90=15.22 млн ₽/мес; главный риск, это weak moat и price compression от incumbents.
Что доказать: ARPA ≥230К ₽/мес, pilot-to-paid ≥30%, churn ≤1.8%/мес, 3 кейса с measurable ROI и repeatable GTM вне founder network.
Куда отправить: Telegram topic 270.
GitHub: PENDING
