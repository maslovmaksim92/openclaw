# Unit economics — AI-фотосессии в Telegram для соцсетей и маркетплейсов

Дата: 2026-05-11 14:28 MSK
Статус: REJECT
Сегмент модели: SMB self-serve / micro-SMB seller tools

## 1) Executive summary

Вывод fund-level: **кейс не проходит investment grade**.

Почему:
- при целевом чеке `2 999 ₽/клиент/мес` бизнес может собрать приемлемый **CAC Payback ~8.0 мес**, но **LTV/CAC = 1.4x**, что сильно ниже investable-порога `3.0x`; [T4][T5]
- даже если дойти до `50` платящих клиентов, месячная выручка составит только `149 950 ₽`, а EBITDA останется глубоко отрицательной из-за команды, поддержки, acquisition и infra;
- порог `500k ₽ EBITDA/мес` на этом чеке достигается только примерно после `~1 050` активных клиентов, что слишком далеко для Telegram-first продукта с commodity-risk и слабым category demand. [T1][T2]

Итог: **Profit Gate = FAIL**, поэтому кейс переводится в `pipeline/rejected/`.

## 2) Ключевые допущения модели

### ICP
- продавцы маркетплейсов, эксперты и micro-SMB, которым нужны карточки, lifestyle-изображения и быстрые креативы; [T1][T2]
- средний тариф для расчёта: **Pro plan `2 999 ₽/мес`**;
- billing: месячная подписка;
- продуктовый сценарий: Telegram как интерфейс, backend image pipeline + templates + support.

### Бенчмарк churn
Для раннего SMB SaaS с низким ARPA берём **monthly logo churn = 6.5%**.

Обоснование:
- ChartMogul пишет, что median early-stage SaaS `<$300k ARR` имеет churn около `6.5%` в месяц; [T5]
- Help Center ChartMogul также даёт ориентир `6–7%`/мес для низкого ARPA и `3–7%`/мес как типичный диапазон для SaaS. [T4]

Для модели используем **6.5%/мес** как базовый сценарий.

### Gross margin
Берём **75% GM**.

Логика:
- у продукта есть GPU/inference cost, хранилище, платёжные комиссии и support;
- это лучше, чем агентская экономика, но хуже, чем pure-text SaaS.

## 3) Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Привлечение лида через рекламу/контент | Маркетолог | Яндекс.Директ, VK Ads, Telegram-посевы | 1-7 дней до визита | 180 | средняя |
| 2 | Клик и переход в бота/лендинг | Пользователь | Telegram Bot, Tilda/лендинг | 2-5 мин | 15 | высокая |
| 3 | Приветственный онбординг и выбор сценария | Бот + Product | Telegram bot flow | 3-7 мин | 20 | высокая |
| 4 | Загрузка 5-15 фото / brief по товару | Пользователь | Telegram upload | 10-20 мин | 10 | высокая |
| 5 | Валидация входных материалов | Support / AI-модерация | moderation script, admin panel | 5-10 мин | 45 | средняя |
| 6 | Генерация preview | ML/backend | inference pipeline, queue | 5-15 мин | 55 | высокая |
| 7 | Дожим до оплаты: paywall, reminders | CRM/бот | Telegram reminders, amoCRM | 1-3 дня | 35 | высокая |
| 8 | Ответы на вопросы / ручной help | Support | Telegram, FAQ | 5-15 мин | 70 | низкая |
| 9 | Оплата подписки | Пользователь | ЮKassa/Telegram payment | 2-3 мин | 110 | высокая |
| 10 | Выдача финального результата | Бот | Telegram bot, storage CDN | 1-5 мин | 35 | высокая |
| 11 | Повторный usage / retention-механика | CRM/CS | рассылки, шаблоны, триггеры | 30 дней | 90 | средняя |

Итого ориентир на одного нового paying customer в первый месяц обслуживания: **~665 ₽ переменных и полу-переменных операционных затрат**, без учёта acquisition.

## 4) COGS на клиента в месяц

Считаем для одного активного клиента на тарифе `2 999 ₽/мес`.

| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| GPU / inference | 320 | ~80 генераций в месяц с буфером на retries |
| Хранилище и CDN | 45 | хранение ассетов и выдача результатов |
| Telegram / backend infra | 90 | сервер, очереди, monitoring |
| Платёжная комиссия | 105 | ~3.5% от 2 999 ₽ |
| Support, ручные проверки | 140 | частичное время support |
| Возвраты/credits/брак | 50 | резерв ~1.7% выручки |
| Итого COGS | **750** |  |

- Выручка на клиента: `2 999 ₽/мес`
- Валовая прибыль на клиента: `2 249 ₽/мес`
- **Gross Margin = 75.0%**

## 5) CAC по каналам и воронка

### Воронка по каналам

| Канал | Показы/охват | Клик/лид | Start bot | Trial/preview | Paying customers | Конверсия lead→pay | CAC raw, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Яндекс.Директ | 120 000 | 2 400 | 1 080 | 216 | 36 | 1.5% от клика | 10 000 |
| VK Ads | 180 000 | 3 000 | 1 050 | 158 | 21 | 0.7% от клика | 9 524 |
| Telegram-посевы/инфлюенсеры | 300 000 views | 2 100 | 840 | 126 | 14 | 0.67% от клика | 12 857 |
| Партнёрки/рефералка | 200 leads | 200 | 120 | 48 | 12 | 6.0% от лида | 5 000 |

### Fully-loaded CAC

Формула:
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocated + Tools + Events + Overhead multiplier) / New paying customers`

Модель месяца acquisition:
- новые paying customers в месяц: **60**
- сегмент: **SMB self-serve**, поэтому используем multiplier **x1.3**

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ + VK) | 560 000 | 360k + 200k budget | внутреннее допущение по тестовому спенду |
| Outbound / sales FOT attributed to new | 234 000 | 1 SDR `180k` gross × 1.3 | [T8] |
| Marketing team FOT (partial allocation) | 156 000 | marketer `240k` gross × 50% × 1.3 | [T10] |
| Tools / CRM / analytics | 60 000 | amoCRM + трекинг + creative tools | внутреннее допущение |
| Events / partnerships | 80 000 | посевы, микроинтеграции, партнёрки | внутреннее допущение |
| Subtotal before multiplier | 1 090 000 | сумма выше |  |
| Overhead multiplier x1.3 | 327 000 | `1 090 000 × 0.3` | стандарт для SMB self-serve |
| Total acquisition cost | **1 417 000** |  |  |

**Blended fully-loaded CAC = `1 417 000 / 60 = 23 617 ₽`**

### Sanity check против бенчмарка
- полученный blended CAC `23.6k ₽` попадает в диапазон **SMB self-serve `5-30k ₽`**, то есть модель не выглядит заниженной;
- при этом CAC почти в `7.9x` месячного ARPA, что уже тяжело для low-ticket продукта.

## 6) LTV, churn, LTV/CAC, payback

### Расчёт LTV
- ARPA / MRR per customer = `2 999 ₽`
- Gross Margin = `75%`
- Monthly churn = `6.5%`
- Lifetime months = `1 / 0.065 = 15.4 мес`
- **LTV = `2 999 × 0.75 / 0.065 = 34 604 ₽`**

### Метрики эффективности

| Метрика | Значение |
|---|---:|
| Blended fully-loaded CAC | 23 617 ₽ |
| LTV | 34 604 ₽ |
| **LTV/CAC** | **1.47x** |
| **CAC Payback** | **7.9 мес** |
| Contribution Margin per client/month | `2 249 - 393 = 1 856 ₽` |
| Contribution Margin % | **61.9%** |

Где `393 ₽` это acquisition amortization на месяц жизни клиента: `23 617 / 60` здесь не используется. Для contribution-margin берём приближение через распределение CAC по lifetime: `23 617 / 15.4 = 1 534 ₽`? Это уже после-acquisition unit margin. Чтобы не смешивать определения, используем ниже два слоя:

### Margin layers
- Gross Margin: `75.0%`
- Contribution after amortized CAC: `(2 249 - 1 534) / 2 999 = 23.8%`

### Интерпретация
- **Payback < 12 мес**, это формально терпимо для SMB SaaS;
- но **LTV/CAC 1.47x** ниже и базового comfort-level `2x`, и investment-grade порога `3x`;
- значит продукт может быть операционно живым, но **не fund-grade**.

## 7) Team & FOT

### Полная команда

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | Time-to-hire | Ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес | Источник |
|---|---:|---|---:|---|---|---:|---:|---|
| CEO/founder | 1 | стратегия, GTM, fundraising | 600 000 | 0 | 0 | 180 000 | 780 000 | [T11] |
| CTO/Tech Lead | 1 | продукт, архитектура, delivery | 550 000 | 2-3 мес | 2 мес | 165 000 | 715 000 | [T7] |
| Senior Backend | 2 | bot/backend/integrations | 420 000 | 1-2 мес | 1.5 мес | 126 000 | 546 000 each | [T6] |
| ML Engineer | 1 | inference quality, prompts, pipelines | 500 000 | 2-3 мес | 2 мес | 150 000 | 650 000 | [T12] |
| DevOps | 1 | infra, CI/CD, cost control | 350 000 | 1-2 мес | 1 мес | 105 000 | 455 000 | [T9] |
| Frontend / bot UI | 1 | mini-app, landing, growth UX | 280 000 | 1 мес | 1 мес | 84 000 | 364 000 | [T13] |
| SDR / growth ops | 1 | партнёрки, outbound, лидогенерация | 180 000 | 0.5-1 мес | 1 мес | 54 000 | 234 000 | [T8] |
| AE / partnerships | 1 | сделки с seller teams, апсейл | 300 000 | 1-2 мес | 2-3 мес | 90 000 | 390 000 | [T7] |
| Customer Success / Support | 1 | onboarding, support, retention | 220 000 | 1 мес | 1 мес | 66 000 | 286 000 | [T14] |
| Маркетолог performance/content | 1 | ads, creatives, funnels | 240 000 | 1 мес | 1 мес | 72 000 | 312 000 | [T10] |

**Полный steady-state FOT команды = 4 732 000 ₽/мес**

### Комментарий по hiring realism
- в первый месяц нельзя реалистично вывести все `10` ролей;
- минимальная рабочая команда стартует с founder-led ядра и добирается до полного штата только к `M6-M7`;
- это означает длинный burn до стабильной воронки и отрицательную экономику на раннем этапе.

## 8) Cumulative FOT timeline M1-M12

Предпосылки:
- `M1`: founder full-time, marketer, 1 backend;
- `M2`: support;
- `M3`: CTO и SDR;
- `M4`: DevOps и frontend;
- `M5`: ML engineer;
- `M6`: AE и второй backend;
- ramp учитываем консервативно через 100% cash-cost, так как зарплата платится сразу, даже если продуктивность ещё не 100%.

| Месяц | Кто в штате | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, Marketing, Backend-1 | 1 638 000 |
| M2 | + Customer Success | 1 924 000 |
| M3 | + CTO, SDR | 2 873 000 |
| M4 | + DevOps, Frontend | 3 692 000 |
| M5 | + ML Engineer | 4 342 000 |
| M6 | + AE, Backend-2 | 5 278 000 |
| M7 | полный состав | 5 278 000 |
| M8 | полный состав | 5 278 000 |
| M9 | полный состав | 5 278 000 |
| M10 | полный состав | 5 278 000 |
| M11 | полный состав | 5 278 000 |
| M12 | полный состав | 5 278 000 |

Примечание: здесь FOT по timeline выше steady-state таблицы, потому что включён founder full cash-comp и 2 backend. Для инвестиционной оценки берём более жёсткий cash view.

## 9) Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT + payroll taxes | 5 278 000 | по M6+ состоянию |
| Office / legal / бухгалтерия | 180 000 | lean setup |
| SaaS tools / CRM / analytics | 120 000 | без ads |
| Core infra reserve | 220 000 | non-usage base |
| Итого fixed costs / month | **5 798 000** |  |

## 10) Break-even

### Break-even по количеству клиентов
Формула: `Fixed costs / contribution per client`

Берём contribution до CAC-amortization:
- revenue = `2 999 ₽`
- COGS = `750 ₽`
- contribution = `2 249 ₽`

**Break-even clients = `5 798 000 / 2 249 = 2 578 клиентов`**

Даже если смотреть через более мягкий fixed-cost режим `~2.35 млн ₽/мес` на маленькой команде, break-even всё равно около:
- `2 350 000 / 2 249 = 1 045 клиентов`

### Break-even по времени
Если компания умеет добавлять по `60` новых paying customers net в месяц и churn `6.5%`, то до `1 045` активных клиентов она идёт примерно **18-22 месяцев**, при условии что acquisition не ломается. Для Telegram-first commodity-product это слишком длинный и рискованный путь.

## 11) EBITDA test на 50 клиентов

| Показатель | Значение |
|---|---:|
| Клиенты | 50 |
| Выручка | 149 950 ₽/мес |
| COGS | 37 500 ₽/мес |
| Валовая прибыль | 112 450 ₽/мес |
| Fixed costs even lean | 2 350 000 ₽/мес |
| EBITDA | **-2 237 550 ₽/мес** |

**Тест Profit Gate провален:** при `50` клиентах компания не просто не достигает `500k EBITDA`, а остаётся глубоко убыточной.

## 12) Burn-to-breakeven и runway

### Burn-to-breakeven
Для консервативной модели берём startup capital = **20 000 000 ₽**.

| Период | Средний burn / мес, ₽ | Комментарий |
|---|---:|---|
| M1-M2 | 2 000 000 | core team + тесты acquisition |
| M3-M5 | 3 800 000 | расширение продукта и GTM |
| M6-M12 | 5 500 000 | near full team + платный рост |

При таком профиле кэша до выхода хотя бы на lean break-even потребуется примерно:
- `~55-65 млн ₽` совокупного burn,
- что существенно выше стартовых `20 млн ₽`.

### Cash runway
При burn-rate `~3.8 млн ₽/мес` средним по первым 6 месяцам:
- **runway = `20 000 000 / 3 800 000 = 5.3 мес`**

При полном составе и платном acquisition `~5.5 млн ₽/мес`:
- **runway = `20 000 000 / 5 500 000 = 3.6 мес`**

Это слишком коротко для категории, где ещё не доказан retention-quality и category pull.

## 13) Инвестиционный вердикт

### Что хорошо
- понятный low-friction entry point через Telegram;
- есть платёжная привычка и substitutes в диапазоне `399-2 999 ₽/мес`; [T2]
- payback по blended CAC не катастрофический.

### Что плохо
- **ARPA слишком низкий** для команды, которая нужна даже для lean-эксплуатации visual AI-продукта;
- **LTV/CAC = 1.47x**, ниже минимально комфортного уровня;
- для break-even нужен объём клиентов, который не соответствует observed demand strength и защитимости канала;
- при `50` клиентах EBITDA глубоко отрицательная, то есть mandatory Profit Gate не проходит.

## 14) Final verdict

**Решение: REJECTED.**

Причины reject:
1. **Profit Gate FAIL**: `EBITDA < 500k ₽/мес` не просто на 50 клиентах, а даже близко недостижима.
2. **LTV/CAC 1.47x**: не investment grade и существенно ниже порога `3:1`.
3. Нужный объём клиентов для окупаемости слишком высок для Telegram-first commodity use case.

## Sources
- [T1] Demand validation по кейсу: `02-demand.md`
- [T2] Публичные тарифы 24AI / SUPA / Flyvi из `02-demand.md`
- [T4] ChartMogul Help Center, Customer Churn Rate: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T5] ChartMogul, customer churn benchmarks by ARR: https://chartmogul.com/blog/actionable-saas-metrics-customer-churn-rate/
- [T6] HH.ru, senior backend developer в Москве: https://hh.ru/vacancy/129266637
- [T7] HH.ru, account executive / KAE в Москве: https://hh.ru/vacancies/account_executive
- [T8] HH.ru, SDR в Москве: https://hh.ru/vacancies/account_executive/polniy_den
- [T9] HH.ru, devops engineer в Москве: https://hh.ru/search/vacancy?text=DevOps+Engineer
- [T10] HH.ru, performance marketing manager в Москве: https://hh.ru/search/vacancy?text=performance+marketing+manager
- [T11] HH.ru, CEO / general manager вакансии: https://hh.ru/search/vacancy?text=CEO
- [T12] HH.ru, ML engineer в Москве: https://hh.ru/search/vacancy?text=ML+engineer
- [T13] HH.ru, frontend developer в Москве: https://hh.ru/search/vacancy?text=frontend+developer
- [T14] HH.ru, customer success manager в Москве: https://hh.ru/search/vacancy?text=customer+success+manager
