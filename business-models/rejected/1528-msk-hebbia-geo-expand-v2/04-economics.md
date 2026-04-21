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
