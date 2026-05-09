# Unit Economics — Medsenger: AI-дистанционный мониторинг и телемедицина для клиник

## Итог
**Решение: FAIL инвестиционный фильтр.**

Почему:
- blended fully-loaded CAC для regulated healthtech B2B получается **~1.03 млн ₽ на 1 платящую клинику**;
- при базовом ACV **1.08 млн ₽/год** и MRR **90 000 ₽/клиент/мес** это даёт **LTV/CAC = 2.5x**, что ниже инвестиционного порога **3.0x**;
- даже при **50 клиентах** модель не выходит на **EBITDA 500K+ ₽/мес**: база даёт около **-2.26 млн ₽ EBITDA/мес**;
- break-even в базовой команде достигается только около **95 клиентов**, что слишком далеко для текущего GTM и длинного regulated sales cycle.

## 1) Ключевые допущения модели
| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Частные клиники и сети, chronic care / follow-up | regulated B2B healthtech |
| Средний recurring чек | **90 000 ₽/мес** | 10 активных врачей × 9 000 ₽/врач/мес, midpoint из 7–10K ₽ [T1] |
| Onboarding fee | **250 000 ₽** | интеграции, шаблоны, протоколы |
| ACV | **1 080 000 ₽/год** | recurring only, onboarding отдельно |
| Gross margin до sales commissions | **63.3%** | см. COGS ниже |
| Monthly logo churn | **2.2%/мес** | взят как enterprise/high-ARPA B2B SaaS benchmark [T6] |
| Deal cycle | **4–6 месяцев** | regulated клиники, ИБ/юристы/главврач |
| Startup capital в модели | **60 млн ₽** | stress-test на burn-to-breakeven |

## 2) Подробный бизнес-процесс: от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Поиск target-клиник и списка ЛПР | SDR | HH/2ГИС/сайты клиник/CRM | 2 ч на аккаунт | 1 400 | низкая |
| 2 | Первый outbound contact, письмо/звонок/мессенджер | SDR | amoCRM, почта, телефония | 30 мин | 350 | средняя |
| 3 | Квалификация боли и маршрута закупки | SDR + CEO | CRM, скрипт discovery | 45 мин | 1 600 | низкая |
| 4 | Intro-call с главврачом/операционным директором | CEO/AE | Zoom/Meet, презентация | 1 ч | 4 500 | низкая |
| 5 | Сбор требований по МИС, ПДн, телемедицине | CTO + CEO | Notion, чеклист ИБ | 2 ч | 5 200 | низкая |
| 6 | Подготовка demo и pilot scope | AE + CTO | Demo-стенд, Figma, docs | 4 ч | 10 400 | средняя |
| 7 | Пилот 4–8 недель | CSM + CTO + врач-куратор клиента | продукт, чат, аналитика | 30–40 ч | 52 000 | средняя |
| 8 | Согласование ИБ/юридических условий | CTO + CEO | DPA, договор, security pack | 10 ч | 26 000 | низкая |
| 9 | Коммерческое предложение и защита ROI | CEO/AE | финмодель, КП | 2 ч | 7 000 | низкая |
| 10 | Подписание договора | CEO + юрист аутсорс | ЭДО, Диадок | 1 неделя календарно | 8 000 | средняя |
| 11 | Технический онбординг и интеграция | CTO + backend + CSM | API/вебхуки/чат | 20–30 ч | 70 000 | средняя |
| 12 | Обучение врачей и запуск | CSM | вебинары, инструкции | 6 ч | 15 000 | средняя |
| 13 | Первый счёт и оплата | бухгалтерия клиента + CEO | банк, ЭДО | 7–15 дней | 2 000 | высокая |

**Вывод:** процесс дорогой и длинный. Это не self-serve SaaS, а regulated consultative sale с дорогим пилотом и интеграцией.

## 3) COGS на 1 клиента в месяц
| Компонент | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Облако и вычисления | 7 000 | защищённый контур, хранение ПДн, moderate AI-нагрузка | T1, аналитическая оценка |
| Хранение, бэкапы, логирование | 4 000 | резервирование и аудит | аналитическая оценка |
| SMS/уведомления/видеосвязь/коммуникации | 3 500 | средний usage на 10 врачей | аналитическая оценка |
| Имплементация и интеграции, амортизация | 6 500 | onboarding 250K, амортизация по 38 мес | аналитическая оценка |
| CSM/support allocation | 9 000 | 1 CSM на ~28 клиентов | T4 + модель команды |
| Security/compliance operations | 3 000 | ИБ, аудит доступов, инциденты | аналитическая оценка |
| **Итого COGS** | **33 000** |  |  |

**Gross profit на клиента/мес = 90 000 - 33 000 = 57 000 ₽**  
**Gross margin = 63.3%**

## 4) CAC по каналам и воронка
| Канал | Лиды/касания в мес | Meetings | Qualified | Pilots | Wins | Monthly spend fully-loaded, ₽ | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| Outbound по клиникам | 120 | 24 (20%) | 8 (33%) | 3 (37.5%) | 0.55 (18%) | 520 000 | **945 455** | основной канал |
| Партнёры/МИС/интеграторы | 12 | 6 (50%) | 3 (50%) | 1 (33%) | 0.25 (25%) | 180 000 | **720 000** | лучший CAC, но мало объёма |
| Отраслевые мероприятия | 30 | 9 (30%) | 4 (44%) | 1 (25%) | 0.20 (20%) | 325 000 | **1 625 000** | дорогой канал |
| **Blended** | **162** | **39** | **15** | **5** | **1.00** | **1 025 000** | **1 025 000** | 1 новый платящий клиент/мес |

### FULLY-LOADED CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 40 000 | retargeting + branded search, низкая доля канала | аналитическая оценка |
| Outbound team FOT (SDR/AE attributed to new) | 220 000 | SDR 170K gross + AE 380K gross, атрибуция только acquisition, +30% соцвзносы | T4 |
| Marketing team FOT (partial allocation) | 55 000 | частичная загрузка founder-led GTM и контент/дизайн подрядчиков | аналитическая оценка |
| Tools (CRM, телефония, рассылки, аналитика) | 25 000 | amoCRM, телефония, почта, webinar stack | аналитическая оценка |
| Events/partnerships | 70 000 | усреднение конференций и co-marketing | аналитическая оценка |
| **Raw acquisition subtotal** | **410 000** | до overhead |  |
| Overhead multiplier (**regulated healthtech ×2.5**, additive uplift) | **615 000** | 410K × (2.5 - 1.0) | T7 |
| **Fully-loaded CAC** | **1 025 000** | 1 025 000 / 1 new customer |  |

### Sanity check по benchmark
Для **healthtech B2B** в РФ ориентир **400K–1.2M ₽ CAC**. Полученные **1.03M ₽** находятся у верхней границы, но не выглядят заниженными. [T7]

## 5) LTV и churn
| Метрика | Значение |
|---|---:|
| MRR на клиента | 90 000 ₽ |
| Gross margin | 63.3% |
| Monthly gross profit | 57 000 ₽ |
| Monthly logo churn | 2.2% |
| **LTV** | **2 590 909 ₽** |

Формула: `LTV = MRR × GM / churn = 90 000 × 0.633 / 0.022 = 2.59 млн ₽`

**Источник churn benchmark:** для high-ARPA B2B SaaS медианный monthly churn около 2%+; для enterprise он ниже SMB, но всё равно заметен и не должен моделироваться как «почти ноль». Для regulated клиник я беру **2.2%/мес** как консервативный benchmark. [T6]

## 6) LTV/CAC
**LTV/CAC = 2 590 909 / 1 025 000 = 2.53x**

Инвестиционный порог в задаче: **>= 3.0x**.  
**Вердикт: ниже investable quality.**

## 7) CAC Payback
Формула из задания: `CAC Payback = CAC / MRR per customer`

**CAC Payback = 1 025 000 / 90 000 = 11.4 месяца**

Формально это ещё укладывается в базовый порог **< 12 мес**, но запас маленький. Любое удлинение цикла продажи или рост пилотных затрат выбивает модель в 13–15 месяцев.

## 8) Contribution Margin
| Показатель | ₽ | % от выручки |
|---|---:|---:|
| Выручка на клиента/мес | 90 000 | 100.0% |
| COGS | 33 000 | 36.7% |
| Валовая прибыль | 57 000 | 63.3% |
| Sales commission / variable success pay | 6 300 | 7.0% |
| **Contribution profit** | **50 700** | **56.3%** |

**Contribution Margin = 56.3%**

## 9) Team & FOT
### Полная команда
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1.5 | 1.5 | 135 000 | 1 170 000 |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 | 1 | 1 | 51 000 | 221 000 |
| AE | 1 | 380 000 | 1.5 | 3 | 114 000 | 494 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product / Implementation Manager | 1 | 280 000 | 1.5 | 1.5 | 84 000 | 364 000 |
| Compliance / Medical Integration Specialist | 1 | 260 000 | 2 | 2 | 78 000 | 338 000 |
| **Итого** | **12** |  |  |  |  | **5 967 000 ₽/мес** |

### Функции команды
| Роль | Основная функция |
|---|---|
| CEO | founder-led sales, enterprise negotiations, fundraising |
| CTO | архитектура, security review, интеграции с МИС |
| Senior Backend | clinical workflows, API, billing, audit trail |
| ML Engineer | triage/напоминания/сводки/LLM safety |
| DevOps | защищённый контур, CI/CD, observability |
| Frontend | кабинет клиники, врачебный UI |
| SDR | первый контакт, pipeline creation |
| AE | демо, pilot to close |
| Customer Success | rollout, adoption, retention |
| Product/Implementation | onboarding, шаблоны care pathways |
| Compliance/Medical Integration | 152-ФЗ, договоры, clinical adaptation |

### Cumulative FOT timeline M1-M12
| Месяц | Кто подключён | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, 1 Senior Backend | 1 430 000 |
| M2 | + CTO, Frontend | 2 535 000 |
| M3 | + 2nd Senior Backend, DevOps | 3 575 000 |
| M4 | + Product/Implementation, SDR | 4 160 000 |
| M5 | + ML Engineer | 4 810 000 |
| M6 | + AE | 5 304 000 |
| M7 | + Customer Success | 5 629 000 |
| M8 | + Compliance / Medical Integration | 5 967 000 |
| M9 | full team | 5 967 000 |
| M10 | full team | 5 967 000 |
| M11 | full team | 5 967 000 |
| M12 | full team | 5 967 000 |

**Sanity checks:**
- Найм не нарушает realism, потому что 5+ человек не нанимаются в M1.
- FOT команды 5–7+ человек с M3 уже выше 3.5M ₽/мес, значит модель не занижает burn.

## 10) Fixed costs breakdown
| Компонент | ₽/мес |
|---|---:|
| FOT full team | 5 967 000 |
| Офис / remote stipends / HR / бухгалтерия | 220 000 |
| Юридическая поддержка и compliance | 120 000 |
| Инфраструктура platform-level, не в COGS | 180 000 |
| Software stack internal | 90 000 |
| Прочие G&A | 85 000 |
| **Итого fixed costs** | **6 662 000 ₽/мес** |

Для break-even беру contribution после variable costs, но acquisition spend считаю отдельной строкой роста. Чтобы не смешивать COGS и CAC, operational fixed-cost base для поддержки 50 клиентов нормализую до **4 795 000 ₽/мес** без масштабного growth spend и без части founder BD. Это всё равно выше того, что может выдержать база в 50 клиентов.

## 11) Break-even
### По количеству клиентов
`Break-even clients = Fixed costs / contribution profit per client`

`4 795 000 / 50 700 = 94.6`

**Break-even = 95 клиентов**

### По месяцу
Базовый реалистичный сценарий: 0 клиентов в M1-M3, 1 клиент в M4, затем +1, +1, +2, +2, +3, +3, +4, +4, +5 новых клиентов в месяц при churn 2.2%.

По такой траектории:
- к **M12** база около **23 клиентов**;
- к **M24** база около **58 клиентов**;
- operational break-even достигается только около **M31-M33**.

**Следствие:** в горизонте первых 24 месяцев кейс остаётся below break-even.

## 12) Burn-to-breakeven и runway
### Burn-to-breakeven
Усреднённый burn на M1-M12 с учётом FOT, platform opex и acquisition: **~5.1 млн ₽/мес**.  
Для достижения 95 клиентов в базовом сценарии потребуется суммарно **~112–118 млн ₽** cash burn до полноценного break-even.

### Cash runway
При `startup_capital = 60 млн ₽`:

`Runway = 60 / 5.1 = ~11.8 месяца`

Даже если burn во втором полугодии частично компенсируется выручкой, капитал 60 млн ₽ не даёт комфортного запаса до M31-M33 break-even. Нужен либо более крупный раунд, либо более лёгкий GTM/implementation model.

## 13) Stress-test: что происходит при 50 клиентах
| Показатель | Значение |
|---|---:|
| Клиенты | 50 |
| MRR | 4 500 000 ₽ |
| COGS | 1 650 000 ₽ |
| Gross profit | 2 850 000 ₽ |
| Variable sales comp | 315 000 ₽ |
| Contribution profit | 2 535 000 ₽ |
| Normalized fixed costs | 4 795 000 ₽ |
| **EBITDA** | **-2 260 000 ₽/мес** |

**Profit Gate FAIL:** даже при 50 клиентах модель не показывает **EBITDA 500K+ ₽/мес**.

## 14) Общий вывод
Кейс выглядит коммерчески реальным, но **не инвестиционно-качественным** на текущей стадии:
- CAC высокий и близок к верхней границе рынка;
- LTV/CAC ниже порога фонда;
- break-even слишком далеко;
- 50 клиентов не хватает, чтобы выйти даже в умеренно положительную EBITDA.

Следовательно, кейс должен быть переведён в **REJECTED** по Program 5.

## Sources
- [T1] Medsenger official / pricing context: https://about.medsenger.ru/
- [T4] HH.ru salary benchmark pages and role searches, Moscow/SPb medians: https://hh.ru/
- [T6] ChartMogul, SaaS churn by ARPA and segment benchmarks: https://chartmogul.com/saas-metrics/reducing-churn/
- [T7] Внутренний benchmark задачи для RU CAC sanity: Healthtech B2B 400K–1.2M ₽ CAC, regulated segment multiplier 2.5–3.0.
