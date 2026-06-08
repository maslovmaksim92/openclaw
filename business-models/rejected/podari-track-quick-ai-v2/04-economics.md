---
stage: economics
case: podari-track-quick-ai-v2
date: 2026-06-08
analyst: branch-models-lead
sector: QUICK-AI
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Podari Track, QUICK-AI сервис персонализированных песен и поздравительных треков.

## Executive summary

**Итог P5: REJECTED по fund economics.**

Причина reject не в отсутствии спроса, а в плохой пригодности для фонда на уровне unit economics:
1. При базовом чеке **990 ₽** и даже при blended AOV **1 110 ₽** кейс **не проходит Profit Gate на 50 клиентах/мес**. Выручка на 50 платящих клиентах составляет лишь **55 500 ₽/мес**, что на порядок ниже даже минимально реалистичной fixed cost базы.
2. **Blended fully-loaded CAC = 1 050 ₽** на нового платящего клиента, почти равен выручке первого заказа и делает first-order economics почти нулевой. [T1][T4][T5][inference]
3. Даже при щедром допущении по repeat и gross margin получается **LTV/CAC = 1,28x**, что выше 1:1, но сильно ниже инвестиционного порога **3:1**. [T1][T3][T4][inference]
4. Формальный **CAC payback = 0,95 мес** по заданной формуле `CAC / MRR_per_customer`, но для one-off gifting это вводит в заблуждение, потому что у продукта нет настоящего подписочного MRR и нет гарантированного recurring cashflow. [inference]
5. По открытым данным Т-Бизнес у юрлица **ООО «ПОДАРИ ТРЕК ГЛОБАЛ» выручка 314,9 млн ₽ и прибыль 3,7 млн ₽ за 2024 год**, то есть даже на реальном масштабе прибыльность уже очень тонкая. Это усиливает вывод, что продукт может быть хорошим бизнесом-бутиком, но не investment-grade для фонда. [T2]

## 1. Ключевые допущения модели

### Доход на 1 клиента
- Базовая цена песни на сайте: **990 ₽**. [T1]
- Допущение по blended upsell: видео/слайдшоу и доп. опции дают ещё **120 ₽** на средний оплаченный заказ. Это консервативно, потому что апселл на сайте есть, но публичной конверсии нет. [T1][inference]
- **Blended AOV = 1 110 ₽**.

### Что считаю unit'ом
Для этого кейса unit = **1 платящий клиент / 1 оплаченный заказ**. Это важно, потому что продукт не является классической подпиской; repeat зависит от новых поводов и сезонности.

### Сценарий модели
Использую **base-case** для фонда:
- 1 200 новых платящих клиентов/мес,
- 20% заказов приходят от repeat/referral без платного привлечения в том же месяце,
- высокая автоматизация production, но маркетинг остаётся главным bottleneck.

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Пользователь видит пост/посев/рекламу | Growth marketer | Telegram, VK, Яндекс.Директ | 1-2 мин контакта | 210 | semi-auto |
| 2 | Переход на лендинг/бота | User + Web analytics | Сайт, Telegram bot, Метрика | 1 мин | 12 | auto |
| 3 | Выбор сценария и оффера | Product / UX | Лендинг, квиз | 2-3 мин | 8 | auto |
| 4 | Заполнение анкеты: имя, повод, детали | User | Web form / bot flow | 4-6 мин | 15 | auto |
| 5 | Предпросмотр и проверка полноты брифа | Support QA | CRM / internal admin | 2-4 мин | 38 | semi-auto |
| 6 | Генерация текста/структуры песни | LLM pipeline | LLM + templates | 30-60 сек | 42 | auto |
| 7 | Генерация музыки и вокала | AI production | music gen / voice stack | 2-4 мин | 96 | auto |
| 8 | Рендер, хранение, выдача preview | Infra | storage/CDN/render queue | 1-2 мин | 18 | auto |
| 9 | Оплата заказа | User + PSP | ЮKassa/CloudPayments class | 1-2 мин | 39 | auto |
| 10 | Контроль качества / ручная корректировка исключений | Content QA | CRM, audio editor | 3-5 мин | 55 | semi-auto |
| 11 | Доставка финального файла | Bot / email / site | Telegram, email, CDN | <1 мин | 7 | auto |
| 12 | Пост-продажный follow-up, upsell, referral | CRM marketer | CRM, Telegram, email | 1-3 дня лаг | 24 | semi-auto |

**Итого переменная стоимость процесса на 1 оплаченный заказ: ~564 ₽**, из которых прямой production COGS ниже, а остальное относится к acquisition/QA/follow-up. Для gross margin отдельно выделяю только COGS. [inference]

## 3. COGS breakdown на 1 клиента / месяц

Здесь считаю только прямую себестоимость исполнения заказа, без CAC.

| Компонент COGS | ₽/клиент | Как получено | Источник |
|---|---:|---|---|
| LLM генерация текста и структуры | 42 | inference + orchestration на 1 заказ | [inference] |
| Музыкальная генерация / вокал | 96 | 1-2 генерации + reroll reserve | [inference] |
| Render / storage / CDN | 18 | файл, хранение, выдача | [inference] |
| Платёжный эквайринг | 39 | ~3,5% от 1 110 ₽ | [inference] |
| Support / QA handling | 31 | аллокация ручных исключений | [inference] |
| Refund / remake reserve | 12 | 1% AOV + брак | [inference] |
| **Итого COGS** | **238 ₽** |  |  |

- **Revenue per client/month = 1 110 ₽**
- **COGS per client/month = 238 ₽**
- **Gross profit per client/month = 872 ₽**
- **Gross margin = 78,6%**

## 4. CAC по каналам с funnel conversion

### Канальная воронка

| Канал | Reach / Impressions | CTR в visit | Visits | Visit→brief | Briefs | Brief→checkout | Checkout | Checkout→paid | New paid | Channel spend, ₽/мес | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Telegram organic + referral content | 1 000 000 | 1,8% | 18 000 | 22% | 3 960 | 14% | 554 | 65% | 360 | 90 000 | 250 |
| Telegram посевы / блогеры | 900 000 | 1,3% | 11 700 | 24% | 2 808 | 14% | 393 | 61% | 240 | 240 000 | 1 000 |
| VK / Яндекс.Директ | 3 500 000 | 0,55% | 19 250 | 18% | 3 465 | 12% | 416 | 58% | 241 | 320 000 | 1 328 |
| Партнёрки / occasion placements | 400 000 | 1,0% | 4 000 | 20% | 800 | 15% | 120 | 58% | 70 | 70 000 | 1 000 |
| **Итого / blended channel** | **5 800 000** |  | **52 950** |  | **11 033** |  | **1 483** |  | **911** | **720 000** | **790** |

### Fully-loaded CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 320 000 | budget base-case | [inference] |
| Telegram посевы / блогеры | 240 000 | paid seeding budget | [inference] |
| Outbound team FOT (attributed to new) | 0 | для B2C gifting SDR/AE не являются core acquisition channel | [inference] |
| Marketing team FOT (partial allocation) | 140 000 | growth marketer 70% от 200k gross | [T4][inference] |
| Tools (CRM, аналитика, рассылки, bot stack) | 45 000 | amo/Bitrix class + analytics + bot tools | [inference] |
| Events / partnerships | 60 000 | партнёрские размещения, праздничные интеграции | [inference] |
| Subtotal raw acquisition cost | 805 000 | сумма выше |  |
| Overhead multiplier (x1.3 для SMB/self-serve) | 241 500 | 30% на management overhead и ops | [inference] |
| **Итого fully-loaded acquisition cost** | **1 046 500** |  |  |
| **New paying customers / мес** | **~1 000** | округление до realistic blended base |  |
| **Blended fully-loaded CAC** | **1 050 ₽** | 1 046 500 / ~1 000 |  |

### Sanity check по CAC
- Для self-serve digital продукта **raw CAC 790 ₽** и **fully-loaded CAC 1 050 ₽** означают, что acquisition почти съедает весь первый чек.
- Это не нарушает внешний enterprise benchmark из задания, потому что кейс не enterprise SaaS. Но для low-ticket gifting это всё равно **красный флаг**, так как CAC почти равен AOV.
- **CAC по каналу ≠ blended CAC**: лучший канал здесь organic/referral, а blended портится из-за платных посевов и paid social.

## 5. LTV и churn rate

### Бенчмарк churn
В качестве верхней границы использую подписочный B2C benchmark Recurly: **B2C churn 6,77%**, а для Digital Media / Entertainment / Consumer Goods около **7,1%**. [T3]

### Почему этот benchmark слишком оптимистичен для кейса
Podari Track продаёт не подписку, а **occasion-driven one-off gift**. Поэтому реальная «эффективная churn/не-возвратность» должна быть значительно хуже, чем у подписочного B2C entertainment. Для инвестиционной модели применяю **effective monthly churn = 68%** как рабочее допущение для событийного подарочного спроса. Это inference, но оно лучше отражает реальность use case. [T1][T3][inference]

### Расчёт LTV
- Gross profit per client/month = **872 ₽**
- Effective monthly churn = **68%**
- Expected lifetime months = **1 / 0,68 = 1,47 мес**
- **LTV = 872 × 1,47 = 1 282 ₽**

### Интерпретация
- Если взять слишком мягкий subscription benchmark 6,8%, LTV получается искусственно огромным и вводит в заблуждение.
- Для фонда корректнее считать короткую life с редким repeat, потому что это подарок под событие, а не регулярный utility.

## 6. LTV/CAC ratio

- **LTV = 1 282 ₽**
- **Blended fully-loaded CAC = 1 050 ₽**
- **LTV/CAC = 1,22x**

### Вывод
- Формально выше 1:1, значит модель не полностью сломана.
- Но до инвестиционного порога **3:1** очень далеко.
- Для фонда это **FAIL**.

## 7. CAC payback

По обязательной формуле:
- `CAC Payback = CAC / MRR_per_customer`
- `1 050 / 1 110 = 0,95 мес`

### Почему метрика misleading
Для one-off gifting здесь нет настоящего MRR. Поэтому **0,95 месяца** выглядит красиво только формально. Экономически важнее то, что **first-order contribution после COGS и CAC = 1 110 - 238 - 1 050 = -178 ₽**. То есть новый клиент в среднем убыточен на первом заказе, и окупаемость зависит исключительно от repeat/referral.

## 8. Contribution Margin %

### CM1, без CAC
- Revenue = **1 110 ₽**
- COGS = **238 ₽**
- Contribution = **872 ₽**
- **Contribution Margin = 78,6%**

### CM2, после fully-loaded CAC на первом заказе
- Revenue = **1 110 ₽**
- COGS = **238 ₽**
- CAC = **1 050 ₽**
- Contribution after CAC = **-178 ₽**
- **Acquisition-adjusted Contribution Margin = -16,0%**

Для инвестиционного фонда важнее именно второй взгляд, потому что компания должна покупать рост, а не только считать gross margin на исполнении.

## 9. Team & FOT

### Полная таблица команды

| Роль | Функция | Нужно чел. | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO / Founder | стратегия, партнёрства, бренд | 1 | 520 000 | 156 000 | 676 000 |
| CTO / Tech Lead | архитектура, пайплайн генерации | 1 | 450 000 | 135 000 | 585 000 |
| Senior Backend | backend, интеграции, billing | 2 | 350 000 | 105 000 | 910 000 |
| ML Engineer | prompt/data/audio quality | 1 | 400 000 | 120 000 | 520 000 |
| DevOps | infra, очереди, деплой | 1 | 300 000 | 90 000 | 390 000 |
| Frontend | лендинг, квиз, checkout | 1 | 250 000 | 75 000 | 325 000 |
| Growth marketer | performance + creatives | 1 | 200 000 | 60 000 | 260 000 |
| Customer Support | саппорт и возвраты | 1 | 120 000 | 36 000 | 156 000 |
| Content QA / producer | ручные корректировки и QA | 1 | 140 000 | 42 000 | 182 000 |
| Finance / Ops (outsource) | бухгалтерия, юрка, отчётность | 0,5 | 90 000 | 27 000 | 117 000 |
| **Итого** |  | **9,5 FTE** |  |  | **4 121 000 ₽/мес** |

### Таблица найма с realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 520 000 | 0 | 0 | 156 000 | 676 000 |
| CTO/Tech Lead | 1 | 450 000 | 2 | 2 | 135 000 | 585 000 |
| Senior Backend | 2 | 350 000 | 1,5 | 1,5 | 105 000 | 455 000 / чел |
| ML Engineer | 1 | 400 000 | 2,5 | 2 | 120 000 | 520 000 |
| DevOps | 1 | 300 000 | 1,5 | 1 | 90 000 | 390 000 |
| Frontend | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| SDR | 0 | 0 | н/п | н/п | 0 | 0 |
| AE | 0 | 0 | н/п | н/п | 0 | 0 |
| Customer Success / Support | 1 | 120 000 | 1 | 1 | 36 000 | 156 000 |

### Salary benchmark notes
- HH.ru по Москве показывает для senior backend / senior python диапазон примерно **200–400k net**, что соответствует gross около **280–500k**. [T4]
- HH.ru по tech lead в Москве показывает офферы от **350k+ net**. [T4]
- HH.ru по ML Engineer в Москве встречается диапазон **200–300k gross** уже для middle+/senior, что подтверждает минимум рынка, а сильные LLM/audio специалисты обычно стоят выше. [T4][inference]
- HH.ru по B2B sales показывает широкий диапазон **120–300k** для продажников, но для этого кейса полноценные SDR/AE не являются core-motion. [T4]

## 10. Cumulative FOT timeline M1-M12

Соблюдаю hiring realism: нет 5+ полноценных hires в первый месяц.

| Месяц | Кто в штате | FOT month, ₽ |
|---|---|---:|
| M1 | CEO | 676 000 |
| M2 | CEO + Frontend | 1 001 000 |
| M3 | CEO + Frontend + CTO + Backend #1 | 2 041 000 |
| M4 | M3 + Backend #2 + Support | 2 652 000 |
| M5 | M4 + Growth marketer + Content QA | 3 094 000 |
| M6 | M5 + DevOps | 3 484 000 |
| M7 | M6 + ML Engineer | 4 004 000 |
| M8 | зрелая команда | 4 121 000 |
| M9 | зрелая команда | 4 121 000 |
| M10 | зрелая команда | 4 121 000 |
| M11 | зрелая команда | 4 121 000 |
| M12 | зрелая команда | 4 121 000 |

## 11. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT | 4 121 000 | см. таблицу выше |
| Infra reserve / cloud / monitoring | 220 000 | очереди, storage, observability |
| SaaS tools / CRM / analytics | 80 000 | неacquisition часть |
| Legal / accounting / compliance | 90 000 | юрка и бухгалтерия |
| Office / admin / misc | 120 000 | минимальный overhead |
| **Итого fixed costs** | **4 631 000 ₽/мес** |  |

## 12. Break-even: по числу клиентов и по месяцу

### Break-even по числу клиентов

**Вариант 1. Без учёта CAC, только по gross profit**
- Fixed costs = **4 631 000 ₽/мес**
- Gross profit per paid client = **872 ₽**
- Нужно клиентов в месяц: `4 631 000 / 872 = 5 311`

**Break-even = ~5 311 платящих клиентов/мес** только чтобы закрыть fixed cost базу, если игнорировать acquisition burden.

**Вариант 2. После fully-loaded CAC на first order**
- Unit contribution after CAC = **-178 ₽**
- При текущем channel mix **break-even на новых клиентах не достигается вообще**.

### Break-even по месяцу
Если стартовать с найма по плану и раскруткой каналов, то в base-case break-even по месяцам **не достигается в горизонте M1-M12**, потому что acquisition-adjusted margin на новой продаже отрицательная, а repeat недостаточен.

## 13. Burn-to-breakeven

### Base-case burn
- Fixed costs: **4,63 млн ₽/мес**
- Acquisition spend: **1,05 млн ₽/мес** fully-loaded
- Base burn before repeat margin: **~5,68 млн ₽/мес**

Даже если получить 1 000 новых клиентов/мес:
- Gross profit = **872k ₽/мес**
- EBITDA до fixed cost остаётся глубоко отрицательной.

### Burn needed until breakeven
При старте с капиталом и попытке разогнать paid + seeding, до честного operating breakeven потребуется **существенно больше 30 млн ₽**, а реалистично ближе к **45–60 млн ₽**, если вообще удастся стабилизировать repeat. [inference]

## 14. Cash runway

Допущение: **startup_capital = 25 млн ₽**.

- Average burn на зрелой фазе M7+ ≈ **5,68 млн ₽/мес**
- Cash runway = `25 / 5,68 ≈ 4,4 мес`

Даже если burn в первые месяцы ниже из-за неполного штата, runway остаётся порядка **5–6 месяцев**, что слишком мало для consumer product, зависимого от сезонности и креативов.

## 15. Profit Gate

### Проверка gate
1. **EBITDA ≥ 500k/mo achievable at 50 clients?** — **Нет.**
   - 50 клиентов × 1 110 ₽ = **55 500 ₽ выручки/мес**.
   - Даже gross profit на этом объёме лишь **43 600 ₽**, что несопоставимо с fixed cost базой **4,63 млн ₽/мес**.
2. **LTV/CAC < 1:1?** — нет, но почти у границы; **1,22x**.
3. **Investment grade threshold LTV/CAC ≥ 3:1?** — **Нет**.

### Итог gate
По правилам фонда кейс получает **REJECTED**, потому что **не может математически показать путь к EBITDA 500k+/мес на 50 клиентах**, а также не дотягивает до инвестиционного порога по LTV/CAC.

## 16. Финальный вывод

Podari Track может быть реальным выручным consumer-бизнесом, и открытые данные по юрлицу подтверждают, что категория в РФ коммерчески существует. Но на уровне фонда это **не investment-grade asset**:
- слишком низкий чек,
- слишком высокий acquisition burden,
- слишком слабый repeat для надёжного LTV,
- слишком большая зависимость от сезонных gifting-поводов,
- отсутствует путь к фондовой unit economics при малом клиентском объёме.

## Источники
- [T1] Podari Track, официальный сайт: https://podari-track.ru/
- [T2] Т-Бизнес, карточка юрлица ООО «ПОДАРИ ТРЕК ГЛОБАЛ»: https://www.tbank.ru/business/contractor/legal/1197746132902/
- [T3] Recurly, churn benchmarks: https://recurly.com/research/churn-rate-benchmarks/
- [T4] HH.ru search, Москва: senior backend / tech lead / ML engineer / sales benchmarks: https://hh.ru/search/vacancy?text=Senior+Backend+Python&area=1 ; https://hh.ru/search/vacancy?text=Tech+Lead&area=1 ; https://hh.ru/search/vacancy?text=ML+Engineer&area=1 ; https://hh.ru/search/vacancy?text=%D0%BC%D0%B5%D0%BD%D0%B5%D0%B4%D0%B6%D0%B5%D1%80+%D0%BF%D0%BE+%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%D0%B0%D0%BC+B2B&area=1
- [T5] Внутренние материалы кейса: `02-demand.md`, `03-solution.md`, `01-evidence.md`

> Investment note 2026-06-08: коммерческий спрос подтверждён, но для фонда экономика слабая, because first-order margin съедается acquisition, а repeat не спасает кейс до 3:1.
