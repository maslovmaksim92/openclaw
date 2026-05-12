---
stage: economics
case: getlivephoto-quick-ai-v2
date: 2026-05-12
analyst: branch-models-lead
sector: QUICK-AI
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
GetLivePhoto, consumer-first Telegram-сервис оживления фото в короткое MP4-видео.

## Executive summary

**Итог P5: REJECTED.**

Причина reject не в отсутствии спроса, а в том, что для low-ticket consumer Telegram-бота экономика не выдерживает fully-loaded acquisition.

Главные выводы:
1. Средний доход на 1 платящего клиента в активный месяц слишком низкий для paid-growth модели.
2. При realistic fully-loaded CAC модель даёт **LTV/CAC = 0.55x**, что ниже даже порога выживаемости 1.0x.
3. EBITDA **500k+ ₽/мес** не выглядит достижимой «уже на 50 клиентах» и вообще требует очень большого числа ежемесячно активных платящих клиентов.
4. Кейс может жить как маленький cashflow-бот на органике, но **не как investment-grade company**.

---

## 1. Ключевые модельные допущения

### Ценообразование и ARPPU
По публичным тарифам продукт продаёт пакеты **79 / 139 / 349 / 549 / 990 ₽**. Базовый модельный микс:
- 25% заказов: 79 ₽
- 20% заказов: 139 ₽
- 30% заказов: 349 ₽
- 15% заказов: 549 ₽
- 10% заказов: 990 ₽

Отсюда:
- средний чек заказа = **360 ₽**
- среднее число заказов на активного платящего клиента в месяц = **1.17**
- **Revenue per paying client/month = 421 ₽**

Это допущение выглядит реалистичным для impulse-product и уже лучше, чем считать всех клиентов на минимальном пакете. Источник цен, T1.

### Повторные покупки и churn
Для consumer quick-AI/Photo & Video приложений я беру консервативный benchmark churn на уровне **30% в месяц**.

Обоснование:
- RevenueCat показывает, что в категории subscription apps конверсия и удержание у **Photo & Video** ниже, чем у business/health apps; сама категория underperform по trial conversion, а monthly retention по рынку проседает год к году. [T2]
- Для разовой эмоциогенной покупки внутри Telegram churn обычно хуже, чем у полезного subscription utility. Поэтому **30% monthly churn** здесь не выглядит агрессивным, а скорее умеренно-оптимистичным.

Следствие:
- средняя жизнь платящего клиента = **1 / 0.30 = 3.33 месяца**

---

## 2. Подробный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Пользователь видит креатив/пример результата | Growth marketer / creator | Telegram Ads, VK Clips, посевы | 1-3 сек | 8 | Полуавто |
| 2 | Клик по ссылке в бот/лендинг | User | Telegram deep link | 3-5 сек | 4 | Авто |
| 3 | Запуск бота и welcome-flow | Bot | Telegram bot, CRM/event tracking | 10-20 сек | 3 | Авто |
| 4 | Загрузка фото | User | Telegram file upload | 20-40 сек | 2 | Авто |
| 5 | Выбор промпта/сценария | User + bot | Prompt templates | 15-30 сек | 2 | Авто |
| 6 | Превью / генерация результата | GPU/API pipeline | Media generation stack | 20-40 сек | 69 | Авто |
| 7 | Paywall и выбор пакета | Bot | Telegram paywall / mini-landing | 10-20 сек | 5 | Авто |
| 8 | Оплата | User + PSP | ЮKassa/CloudPayments/Telegram Payments | 30-60 сек | 21 | Авто |
| 9 | Выдача MP4 и upsell | Bot | storage/CDN + bot logic | 10-20 сек | 7 | Авто |
| 10 | Поддержка/refund edge-cases | Support ops | Telegram support, FAQ | 2-8 мин на кейс | 24 | Ручной слой |

**Итого variable cost на 1 платящего клиента в активный месяц: ~145 ₽**, без учёта acquisition.

---

## 3. COGS breakdown на клиента в месяц

| Компонент | ₽/клиент/мес | Как считалось | Источник |
|---|---:|---|---|
| Генерация / inference | 82 | 1.17 заказа × ~70 ₽ variable media cost | модельное допущение на базе T1 |
| Хранение и доставка MP4 | 11 | object storage + CDN + download traffic | модельное допущение |
| Платёжный эквайринг | 21 | 5% × 421 ₽ | модельное допущение |
| Антифрод / модерация / retry | 7 | небольшой variable слой на failed jobs | модельное допущение |
| Поддержка / refund reserve | 24 | low-ticket consumer support + возвраты | модельное допущение |
| **Итого COGS** | **145** |  |  |

Отсюда:
- Revenue/client/month = **421 ₽**
- COGS/client/month = **145 ₽**
- **Gross profit/client/month = 276 ₽**
- **Contribution margin = 65.6%**

---

## 4. CAC по каналам с funnel conversion

Модель считаю для месяца роста, где продукт активно льёт paid и creator-driven traffic.

| Канал | Reach / Impressions | CTR / click-to-start | Bot start rate | Start-to-pay | New paying customers | Direct spend, ₽ | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Telegram Ads / ads in channels | 3,200,000 | 1.1% | 42% | 3.8% | 562 | 700,000 | 1,246 |
| VK Clips / short-video paid | 1,800,000 | 0.9% | 38% | 3.5% | 216 | 250,000 | 1,157 |
| Посевы у creator-каналов | 900,000 | 1.4% | 45% | 4.9% | 278 | 180,000 | 647 |
| Referral / organic loop | 9,000 переходов | — | 55% | 7.0% | 347 | 60,000 | 173 |
| **Blended direct** | — | — | — | — | **1,403** | **1,190,000** | **848** |

Вывод:
- органика выглядит здоровой, но ограниченной по объёму;
- все масштабируемые paid-каналы дают CAC, который уже опасно близок к месячной выручке клиента;
- для investment-case важен не channel CAC сам по себе, а **fully-loaded CAC**.

---

## 5. FULLY-LOADED CAC

Сегмент здесь ближе к **SMB/self-serve consumer utility**, поэтому применяю mandatory multiplier **x1.3** на raw acquisition stack.

### Таблица fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Telegram/VK) | 950,000 | 700,000 + 250,000 | модель acquisition month |
| Outbound team FOT (SDR/AE attributed to new) | 0 | для consumer self-serve нет SDR/AE | n/a |
| Marketing team FOT (partial allocation) | 312,000 | Growth 240k gross +30%; Designer 180k gross +30%; аллокация 70% и 40% соответственно | HH benchmarks T3-T5 + модель |
| Tools / CRM / analytics / creatives | 95,000 | bot analytics, payments tooling, BI, creative SaaS | модель |
| Events / partnerships / creator fees | 240,000 | посевы и creator payouts | модель |
| Subtotal before overhead | **1,597,000** | сумма выше |  |
| Overhead multiplier (x1.3) | **479,100** | 1,597,000 × 0.30 | standard self-serve overhead |
| **Итого fully-loaded acquisition cost / month** | **2,076,100** |  |  |

При **1,403** новых платящих клиентах:

**Fully-loaded CAC = 2,076,100 / 1,403 = 1,480 ₽**

### Sanity check
Для consumer quick-AI с чеком ~421 ₽ fully-loaded CAC **1,480 ₽** выглядит болезненно, но правдоподобно: дешёвые показы не компенсируют слабую конверсию в оплату и высокую креативную текучку.

---

## 6. LTV, churn rate и LTV/CAC

### Churn benchmark
Берём **30% monthly churn**.

Почему это адекватно:
- RevenueCat 2024 показывает, что Photo & Video и Social/Lifestyle уступают более utilitarian категориям по монетизации и retention; category quality retention structurally ниже. [T2]
- У GetLivePhoto use case ещё более импульсный и event-driven, чем у стандартного monthly app subscription, поэтому 30% выглядит скорее мягким benchmark, а не жёстким.

### LTV расчёт
- Gross profit per client/month = **276 ₽**
- Monthly churn = **30%**
- **LTV = 276 / 0.30 = 920 ₽**

### LTV/CAC
- LTV = **920 ₽**
- Fully-loaded CAC = **1,480 ₽**
- **LTV/CAC = 0.62x**

### Вердикт по метрике
- Требование investment grade: **≥ 3.0x**
- Hard reject line: **< 1.0x**
- Факт: **0.62x**

**Итог: FAIL.**

---

## 7. CAC payback

По обязательной формуле:

**CAC Payback = CAC / MRR per customer = 1,480 / 421 = 3.5 месяца**

Формально payback < 12 месяцев. Но это здесь обманчиво:
1. churn высокий;
2. клиент часто живёт только 3.33 месяца;
3. большая часть когорты выгорает до того, как создаст достаточный gross profit.

Поэтому хороший payback по формуле **не спасает** плохой LTV/CAC.

---

## 8. Contribution Margin %

- Revenue/client/month = **421 ₽**
- COGS/client/month = **145 ₽**
- Contribution/client/month = **276 ₽**
- **Contribution Margin = 65.6%**

На уровне продукта margin неплохая. Проблема не в gross margin, а в том, что acquisition stack съедает value.

---

## 9. Full team table

### Операционная команда для запуска и поддержки

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder | продукт, партнёрства, финконтроль | 600,000 | 180,000 | 780,000 |
| CTO / Tech Lead | архитектура, интеграции, релизы | 500,000 | 150,000 | 650,000 |
| Senior Backend | bot logic, payments, media pipeline | 380,000 | 114,000 | 494,000 |
| Frontend / mini-app | paywall, web-flow, promo pages | 260,000 | 78,000 | 338,000 |
| Growth marketer | acquisition, creative testing, funnel | 240,000 | 72,000 | 312,000 |
| Support / community ops | support, refunds, moderation | 180,000 | 54,000 | 234,000 |
| Designer / motion creative | ad creatives, pack visuals | 180,000 | 54,000 | 234,000 |
| DevOps / infra | reliability, cost control, deploys | 350,000 | 105,000 | 455,000 |
| **Итого** |  | **2,690,000** | **807,000** | **3,497,000** |

### Hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600,000 | 0 | 0 | 180,000 | 780,000 |
| CTO/Tech Lead | 1 | 500,000 | 0 | 0 | 150,000 | 650,000 |
| Senior Backend | 1 | 380,000 | 1.5 | 1.5 | 114,000 | 494,000 |
| ML Engineer | 0 | 0 | 0 | 0 | 0 | 0 |
| DevOps | 1 | 350,000 | 1.5 | 1 | 105,000 | 455,000 |
| Frontend | 1 | 260,000 | 1 | 1 | 78,000 | 338,000 |
| SDR (outbound) | 0 | 0 | 0 | 0 | 0 | 0 |
| AE (Account Exec) | 0 | 0 | 0 | 0 | 0 | 0 |
| Customer Success | 1 | 180,000 | 1 | 1 | 54,000 | 234,000 |
| Growth marketer | 1 | 240,000 | 1 | 1 | 72,000 | 312,000 |
| Designer / creative | 1 | 180,000 | 1 | 1 | 54,000 | 234,000 |

### Комментарий по benchmark зарплат
- Senior backend в hh.ru по Москве виден в коридоре примерно **200k–400k net**, что поддерживает gross-диапазон **350k–550k** для сильного senior. [T3]
- Account executive в Москве на hh.ru виден от **300k+ ₽** с переменной частью, что поддерживает enterprise sales benchmark из standing order, хотя для этого кейса AE не нужен. [T4]
- По hh.ru также видны позиции technical director от **400k ₽** и выше, что поддерживает выбранный CTO-коридор. [T5]

---

## 10. Cumulative FOT timeline M1-M12

Принципиально не нанимаю 5+ человек в первый месяц, чтобы не сломать hiring realism.

| Месяц | Кто в штате | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO | 1,430,000 |
| M2 | + Senior Backend | 1,924,000 |
| M3 | + Frontend, Growth | 2,574,000 |
| M4 | + Support / community | 2,808,000 |
| M5 | + Designer / creative | 3,042,000 |
| M6 | + DevOps | 3,497,000 |
| M7 | тот же состав | 3,497,000 |
| M8 | тот же состав | 3,497,000 |
| M9 | тот же состав | 3,497,000 |
| M10 | тот же состав | 3,497,000 |
| M11 | тот же состав | 3,497,000 |
| M12 | тот же состав | 3,497,000 |

Это уже очень тяжёлый FOT для продукта с ARPPU около 421 ₽. Даже lean-команда создаёт слишком высокую fixed-cost базу относительно unit economics.

---

## 11. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| FOT fully-loaded | 3,497,000 |
| Базовая infra/hosting/platform ops | 120,000 |
| Tools / BI / analytics / creative stack | 140,000 |
| Юрка, бухгалтерия, комплаенс, admin | 95,000 |
| Refund buffer / chargeback reserve / misc ops | 80,000 |
| **Итого fixed costs** | **3,932,000** |

---

## 12. Break-even по клиентам и по месяцу

### Break-even по числу активных платящих клиентов
Contribution на 1 клиента в месяц = **276 ₽**.

**Break-even clients = 3,932,000 / 276 = 14,246 клиентов/мес**

### Break-even для EBITDA 500k/мес
Нужно покрыть fixed costs и ещё принести 500k EBITDA:

**Required clients for 500k EBITDA = (3,932,000 + 500,000) / 276 = 16,058 клиентов/мес**

### Проверка на 50 клиентов
- Revenue = 50 × 421 = **21,050 ₽/мес**
- Contribution = 50 × 276 = **13,800 ₽/мес**
- EBITDA после fixed costs ≈ **-3.92 млн ₽/мес**

**Следовательно, profit gate не проходит с огромным запасом.**

---

## 13. Burn-to-breakeven

Если компания строит growth-модель, месячный burn выглядит так:
- fixed costs = **3.93 млн ₽**
- acquisition month spend fully-loaded = **2.08 млн ₽**
- total burn в фазе активного роста = **~6.01 млн ₽/мес**

Даже если продукт наращивает клиентскую базу, break-even достигается только при объёме **14k+ активных платящих клиентов/мес**, что требует либо очень сильной органики, либо больших рекламных бюджетов, которые дополнительно ухудшают CAC.

**Итог:** burn-to-breakeven для такого low-ticket бота выглядит непропорционально тяжёлым.

---

## 14. Cash runway

Допущение для sanity: **startup_capital = 20 млн ₽**.

- При burn **6.01 млн ₽/мес** runway = **3.3 месяца**
- Даже без активного paid-growth, при одном fixed burn **3.93 млн ₽/мес** runway = **5.1 месяца**

Для consumer bot без сильного moat это слишком короткая полоса для безопасной инвестиционной ставки.

---

## 15. Финальный вывод

### Что хорошо
- Понятный low-friction продукт.
- Неплохой gross margin на единицу.
- Есть шанс на маленький органический cashflow-business.

### Что плохо
- Fully-loaded CAC разрушает экономику.
- LTV/CAC сильно ниже 1.0x.
- Требуемый масштаб клиентской базы для break-even непропорционален moat и ticket size.
- EBITDA 500k+/мес не выглядит инвестируемо достижимой без слишком большого маркетингового риска.

## Вердикт P5

**REJECTED.**

Этот кейс может быть нормальным lifestyle/micro-bootstrapped продуктом, но **не проходит investment fund level unit economics**.

## Источники
- [T1] GetLivePhoto, официальный сайт и тарифы: https://getlivebot.ru/
- [T2] RevenueCat, State of Subscription Apps 2024: https://www.revenuecat.com/state-of-subscription-apps-2024/
- [T3] hh.ru, senior backend developer Москва: https://hh.ru/vacancies/senior-backend-developer
- [T4] hh.ru, account executive Москва: https://hh.ru/vacancies/account_executive/polnaya_zanyatost
- [T5] hh.ru, cto / technical director Москва: https://hh.ru/vacancies/cto
