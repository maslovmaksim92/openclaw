# Unit Economics — Gamma, AI-презентации, КП, лендинги и деловые материалы

## Итог
**Решение: REJECTED на этапе P5 Unit Economics.**

Причина не в отсутствии спроса. Спрос и willingness-to-pay подтверждены в `02-demand.md`, а blended LTV/CAC в базовом сценарии получается приемлемым. Но по инвест-фильтру фонда кейс не проходит, потому что **при 50 клиентах бизнес не способен выйти на EBITDA 500 000 ₽/мес**. Для данного продукта нужен либо намного более высокий ACV, либо резкое упрощение команды, либо channel-first дистрибуция с меньшим burn.

---

## 1) Базовые допущения модели

### Сегмент
- Основной сегмент для модели: **SMB / small teams**, покупающие подписку на генерацию презентаций, КП и мини-лендингов.
- Это ближе к **mid-market B2B / prosumer team SaaS**, а не pure self-serve B2C: есть командные сценарии, бренд-гайды, workspace, экспорт, shared templates.

### Монетизация, принятая в модели
- Средний тариф: **12 900 ₽/клиент/мес**
- Под клиентом понимается **1 компания / 1 workspace**, а не 1 seat.
- Среднее число активных пользователей внутри workspace: **3-5**
- Средний gross margin target: **84%**

### Источники и опорные сигналы
- `02-demand.md`: рынок уже обучен платить за AI-презентации и team plans, ориентир по цене roughly 9 900-24 900 ₽/команду/мес. [T1]
- Gamma / comparable category: self-serve + team pricing и большой платящий рынок категории. [T2]
- SaaS churn benchmark: для ARPA около $100 monthly median gross revenue churn порядка **~4.1%/мес**; для low ARPA churn ещё выше. Для нашей модели беру **4.5%/мес** как консервативный benchmark для SMB/team SaaS. [T3]
- Зарплатные ориентиры по РФ 2026 для Москвы/СПб: диапазоны из HH/job-posting benchmarks, плюс рамки из инвестиционного промпта. [T4]

---

## 2) Подробный бизнес-процесс, от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Лид видит рекламу / контент / партнёрский пост | Marketing | Яндекс.Директ, VK Ads, Telegram ads | 1-7 дней до перехода | 1 800 на лид | Средняя |
| 2 | Переход на лендинг и регистрация trial | Growth / Product | Tilda/Webflow, analytics, signup flow | 10-15 мин | 220 | Высокая |
| 3 | Email onboarding + шаблоны первого use case | CRM marketer | email/CRM automation | 1 день | 90 | Высокая |
| 4 | Первый generated artifact: deck / КП / mini-site | Product + inference backend | LLM API, template engine, storage/CDN | 20-40 мин user time | 340 | Высокая |
| 5 | Product prompts to upgrade / limits reached | Product | paywall, in-app nudges | 3-7 дней | 60 | Высокая |
| 6 | Для team lead: demo request / sales qualification | SDR | CRM, Telegram, email, calendar | 20-30 мин | 1 450 | Средняя |
| 7 | Demo + use-case mapping | AE | CRM, Zoom/Meet, workspace demo | 45-60 мин | 3 200 | Низкая |
| 8 | Trial extension / template setup / brand kit | CSM | product admin, support desk | 1-3 дня | 620 | Средняя |
| 9 | Contract / invoice / online payment | Ops / AE | ЮKassa / cloudpayments / docs | 1 день | 310 | Средняя |
| 10 | Первое списание / monthly renewal | Billing system | payment gateway, CRM | ежемесячно | 464 | Высокая |

### Комментарий
- В self-serve хвосте шаги 6-8 отпадают, но тогда ниже ARPA и выше churn.
- В team-сценарии наоборот растут CAC и sales-touch, но удержание лучше.
- Для инвест-модели выбран **team-SMB base case**, потому что только он даёт шанс выйти на приемлемый LTV/CAC.

---

## 3) COGS на 1 клиента в месяц

### COGS breakdown
| Компонент | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM / inference | 980 | генерация 25-35 артефактов, mix text+layout+rewrite | аналитическая модель по AI workload, на базе category usage [T2] |
| Storage + CDN + export | 210 | файлы, previews, экспорт PDF/PPT | аналитическая оценка |
| Variable support / success | 360 | ~20 мин саппорта на клиента в мес | аналитическая оценка |
| Payment processing | 464 | 3.6% от 12 900 ₽ | типичный эквайринг RU |
| QA / moderation / retries | 50 | re-run и ручные эскалации | аналитическая оценка |
| **Итого COGS** | **2 064** |  |  |

### Валовая маржа
- Revenue per client/month = **12 900 ₽**
- COGS per client/month = **2 064 ₽**
- Contribution per client before fixed costs = **10 836 ₽**
- **Gross Margin = 84.0%**

---

## 4) Fully-loaded CAC, обязательно не только ad spend

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocated + Tools + Events + Overhead multiplier) / New paying customers`

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/Telegram) | 600 000 | тестовый acquisition budget на SMB/team funnel | аналитическая модель, sanity vs RU SaaS [T1] |
| Outbound team FOT (SDR + AE attributed to new) | 702 000 | SDR 234K + AE 468K fully-loaded | T4 |
| Marketing team FOT (partial allocation) | 240 000 | 40% времени growth/marketing owner | T4 + аналитическое допущение |
| Tools (CRM, analytics, outreach, support) | 120 000 | CRM + email + call tracking + support + analytics | аналитическая оценка |
| Events / partnerships | 150 000 | webinars, partner revshare, niche events | аналитическая оценка |
| Raw CAC cost pool | 1 812 000 | сумма строк выше |  |
| Overhead multiplier (x1.3) | 543 600 | 30% overlay на management/admin overhead | стандарт fully-loaded uplift |
| **Итого fully-loaded CAC pool** | **2 355 600** |  |  |

### Funnel и CAC по каналам
| Канал | Spend, ₽/мес | Лиды | Trial | Платящие | Конверсия lead->pay | CAC по каналу, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Paid search / paid social | 600 000 | 1 500 | 240 | 24 | 1.6% | 25 000 |
| Outbound / SDR | 702 000 | 220 | 44 | 8 | 3.6% | 87 750 |
| Partnerships / events | 270 000 | 90 | 27 | 6 | 6.7% | 45 000 |
| **Итого channel spend only** | **1 572 000** | **1 810** | **311** | **38** | **2.1%** | **41 368 blended raw** |

### Blended fully-loaded CAC
- New paying customers / month: **38**
- Raw CAC = **1 812 000 / 38 = 47 684 ₽**
- Fully-loaded CAC = **2 355 600 / 38 = 61 989 ₽**
- Округляю до **62 000 ₽**

### Sanity check vs benchmark
- Для mid-market SaaS benchmark в промпте: **60-250K ₽/клиент**
- Наш **62K ₽** находится на нижней границе, но **не ниже 30%** benchmark, то есть формально проходит sanity-check.
- Это не enterprise sales. Для enterprise-сценария CAC был бы заметно выше, 150K+.

---

## 5) LTV с churn rate

### Churn benchmark
ChartMogul показывает, что у SaaS-компаний с ARPA около **$100** monthly gross revenue churn median составляет примерно **4.1%/мес**, а у более дешёвых SMB-продуктов churn обычно хуже. Для модели беру **4.5%/мес**. [T3]

### Расчёт LTV
Формула: `LTV = ARPA × Gross Margin / Monthly Churn`

- ARPA = **12 900 ₽/мес**
- Gross Margin = **84%**
- Monthly churn = **4.5%**

`LTV = 12 900 × 0.84 / 0.045 = 240 800 ₽`

### Вывод
- **LTV = ~241 000 ₽**
- Для более дешёвого self-serve тарифа churn был бы выше, а LTV ниже.
- Для team-плана с template lock-in и brand-kit churn может быть лучше, но это ещё не доказано.

---

## 6) LTV/CAC ratio

- LTV = **240 800 ₽**
- Fully-loaded CAC = **61 989 ₽**

`LTV/CAC = 240 800 / 61 989 = 3.88x`

### Вывод
- **LTV/CAC = 3.9x**
- Формально это **investment-grade** по этому одному показателю.
- Но фондовый гейт всё равно **FAIL**, потому что показатель EBITDA при 50 клиентах провален.

---

## 7) CAC Payback

Формула по заданию: `CAC Payback = CAC / MRR per customer`

- Fully-loaded CAC = **61 989 ₽**
- MRR per customer = **12 900 ₽**

`CAC Payback = 61 989 / 12 900 = 4.8 мес`

### Вывод
- **CAC Payback = 4.8 месяца**
- Формально хорошо, ниже 12 месяцев.

---

## 8) Contribution Margin %

- Revenue = **12 900 ₽**
- COGS = **2 064 ₽**
- Contribution after COGS = **10 836 ₽**

`Contribution Margin % = 10 836 / 12 900 = 84.0%`

### Вывод
- **Contribution Margin = 84.0%**
- На уровне валовой маржи продукт выглядит нормально.
- Проблема не в gross margin, а в том, что fixed cost base для нормального продукта и go-to-market слишком велика относительно achievable MRR на первых десятках клиентов.

---

## 9) Team & FOT

### Полная команда
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1.5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 0.5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 360 000 | 1-2 | 2-3 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

### Функции команды
| Роль | Функция | Fully-loaded FOT, ₽/мес |
|---|---|---:|
| CEO | стратегия, fundraising, partnerships | 845 000 |
| CTO | архитектура, roadmap, качество продукта | 715 000 |
| Backend x2 | generation pipeline, billing, integrations | 1 170 000 |
| ML Engineer | prompt systems, evals, optimization | 650 000 |
| DevOps | infra, CI/CD, reliability | 455 000 |
| Frontend | editor, workspace UX, onboarding | 390 000 |
| SDR | outbound qualification | 234 000 |
| AE | demo, close, expansion | 468 000 |
| CSM | onboarding, adoption, retention | 325 000 |
| **Итого steady-state FOT** |  | **5 252 000 ₽/мес** |

### Cumulative FOT timeline M1-M12
Реалистичный план с учётом найма и ramp. Специально **нет 5+ людей в M1**, чтобы не нарушать sanity check.

| Месяц | Кто уже в штате | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + CTO + Frontend | 1 950 000 |
| M3 | + Backend #1 + DevOps | 2 990 000 |
| M4 | + Backend #2 + ML | 4 225 000 |
| M5 | + SDR | 4 459 000 |
| M6 | + AE | 4 927 000 |
| M7 | + CSM | 5 252 000 |
| M8 | steady-state | 5 252 000 |
| M9 | steady-state | 5 252 000 |
| M10 | steady-state | 5 252 000 |
| M11 | steady-state | 5 252 000 |
| M12 | steady-state | 5 252 000 |

### Вывод по найму
- Команда меньше этого состава резко повышает product risk и снижает velocity.
- Для AI-продукта с editor/workspace + billing + onboarding + GTM это уже **не игрушечный** состав.
- Именно FOT объясняет, почему кейс не дотягивает до фонда на масштабе 50 клиентов.

---

## 10) Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 252 000 |
| Office / distributed ops / equipment reserve | 180 000 |
| Core SaaS tools / CRM / support / analytics | 120 000 |
| Legal / accounting / data / admin | 130 000 |
| Base infra not included in client COGS | 220 000 |
| Brand/content baseline | 180 000 |
| **Итого fixed costs / month** | **6 082 000 ₽** |

---

## 11) Break-even по клиентам и по месяцу

### Break-even by client count
Формула: `Fixed costs / contribution per client`

- Fixed costs = **6 082 000 ₽/мес**
- Contribution per client = **10 836 ₽/мес**

`Break-even clients = 6 082 000 / 10 836 = 561.3`

Итого:
- **Операционный break-even = 562 клиентов**
- **Для EBITDA 500K/мес нужно:** `(6 082 000 + 500 000) / 10 836 = 607.5`, то есть **608 клиентов**

### Break-even by month
Если net new paying customers = **38/мес**, а churn = **4.5%/мес**, то к break-even компания приходит сильно позже первого года. Даже грубая модель даёт:
- M6: ~190 клиентов кумулятивно брутто, заметно ниже break-even
- M12: ~350-380 активных клиентов при хорошем исполнении, всё ещё ниже 562
- Реалистичный break-even: **после 14-18 месяца**, и это при аккуратном исполнении funnel

### Главный Profit Gate check
При **50 клиентах**:
- Revenue = `50 × 12 900 = 645 000 ₽/мес`
- COGS = `50 × 2 064 = 103 200 ₽/мес`
- Contribution after COGS = **541 800 ₽/мес**
- EBITDA = `541 800 - 6 082 000 = -5 540 200 ₽/мес`

**Итог: при 50 клиентах EBITDA не просто ниже 500K, а глубоко отрицательная. Profit Gate = FAIL.**

---

## 12) Burn-to-breakeven и runway

### Burn-to-breakeven
Даже если допустить рост до 38 новых платящих в месяц, компания в первый год продолжает жечь значительный кэш.

Грубая оценка burn:
- M1 burn: ~1.2M ₽
- M3 burn: ~3.5M ₽
- M6 burn: ~5.0-5.5M ₽
- M7-M12 steady-state burn до выхода на 300+ клиентов: ~3.0-5.0M ₽/мес в зависимости от MRR

**Кумулятивный burn до break-even: 45-60M ₽**.

### Cash runway
При `startup_capital = 30M ₽`:
- На ранних месяцах runway выглядит как **6-8 месяцев**
- До реального break-even такого капитала **не хватает**

### Sanity check
- Для B2B/team AI SaaS здесь нужен капитал заметно выше **10M ₽**, иначе модель нереалистична.
- Наш расчёт это подтверждает, а не опровергает.

---

## 13) Инвест-вывод

### Что хорошо
- Спрос подтверждён. [T1]
- Рынок умеет платить за category outcome. [T1][T2]
- LTV/CAC и payback сами по себе не выглядят катастрофически плохими.

### Что ломает кейс для фонда
1. **50 клиентов не дают даже близко EBITDA 500K/мес**.
2. Чтобы собрать инвестиционно приемлемую команду и продукт, нужен высокий fixed burn.
3. Экономика начинает работать только при **500+ активных клиентах**, что для такого продукта уже требует почти полноценного scale-up GTM.
4. Значит это не хороший fund-return case на ранней стадии, а скорее **bootstrap / studio / channel-led** бизнес, если делать очень lean.

## Финальный verdict
**REJECTED.**

Не потому что рынок плохой, а потому что **unit economics на investment-fund уровне не сходится при заданном profit gate**.

---

## Sources
- **T1** — `02-demand.md` данного кейса: ценовые якоря, сегменты спроса, рыночные use cases.
- **T2** — `01-evidence.md` и первичные источники категории: TechCrunch про Gamma, gamma.app/pricing, Accel note.
- **T3** — ChartMogul Benchmarks, SaaS churn by ARPA band: https://chartmogul.com/reports/saas-benchmarks/ ; https://chartmogul.com/saas-metrics/churn-rate/
- **T4** — HH.ru / RU hiring benchmarks, использованные как salary sanity ranges; также рамки из системного hiring realism блока задачи.
