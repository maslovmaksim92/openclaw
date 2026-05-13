# Unit economics

## Итог
**Вердикт: REJECT.**

Спрос есть, но на уровне инвестфонда кейс не проходит по экономике. При реалистичном ACV для РФ, fully-loaded CAC и команде, которая действительно может поддерживать продукт, продажи и качество, компания **не достигает EBITDA 500K ₽/мес даже на 50 активных клиентах**. Дополнительно LTV/CAC получается **2.8x**, то есть выше 1.0x, но ниже инвестиционного порога **3.0x**.

## 1) Базовая модель, которую считаю
- Модель: **hybrid B2C + SMB team packs**, но инвестиционный юнит считаю по **платящему SMB/agency account**.
- Основной пакет: **24 900 ₽/мес** за командный headshot/workflow pack.
- Допущение: B2C one-off покупки дают лиды и кэш, но не спасают фондовую экономику, потому что повторяемость низкая.
- Сегмент CAC multiplier: **Mid-market B2B**, использую **x1.5**.

## 2) Детальный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Привлечение трафика из VK/Telegram/affiliate | Growth | VK Ads, Telegram Ads, Rewardful/партнёры, Яндекс Метрика | 1-7 дней до конверсии | 4 200 / лид | Частично автоматизировано |
| 2 | Первый визит на лендинг | Клиент | Лендинг, Tilda/Webflow, аналитика | 3-5 мин | 120 | Полностью автоматизировано |
| 3 | Регистрация и загрузка 1-3 селфи | Клиент | Web app, S3/storage, auth | 10-15 мин | 180 | Полностью автоматизировано |
| 4 | Pre-check качества и модерация | AI + support ops | CV pipeline, moderation rules, admin panel | 3-8 мин | 95 | Частично автоматизировано |
| 5 | Генерация headshots | ML pipeline | GPU inference, queue, model orchestration | 8-20 мин | 1 650 | Полностью автоматизировано |
| 6 | Авторанжирование и отбор лучших кадров | AI | Ranking model, prompt presets | 2-3 мин | 140 | Полностью автоматизировано |
| 7 | Ручной QA и ретушь для team-pack клиента | Retoucher / CS | Photoshop, internal QA checklist | 12-18 мин | 1 050 | Низкая |
| 8 | Доставка превью и запрос правок | CS | Email, Telegram bot, web cabinet | 10-20 мин в течение 1 дня | 320 | Частично автоматизировано |
| 9 | Апсейл на team pack / white-label | AE / founder | CRM, demo deck, Telegram/Zoom | 1-3 дня | 2 800 | Низкая |
| 10 | Выставление счёта / онлайн-оплата | Клиент + ops | ЮKassa/Stripe, billing | 5-15 мин | 747 | Полностью автоматизировано |
| 11 | Онбординг аккаунта и бренд-настройка | CS | Notion, шаблоны, кабинет клиента | 1-2 часа | 1 100 | Частично автоматизировано |
| 12 | Повторные загрузки команды и поддержка | CS + AI | Support desk, pipeline, storage | ежемесячно 20-30 мин | 915 | Частично автоматизировано |

**Вывод:** delivery дешёвая, но не нулевая. Как только продаётся не один B2C чек, а recurring team account, появляется ручной QA, онбординг, поддержка, апсейл и sales-touch, из-за чего экономика уже не похожа на «чистый consumer app».

## 3) COGS на клиента в месяц

Считаю по **1 активному SMB/team account в месяц**.

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| GPU inference и model runtime | 1 900 | 2-3 генерации на сотрудника + батчи + retry |
| Хранение, CDN, мониторинг | 350 | storage + delivery allocation |
| Модерация и pre-check | 250 | support ops allocation |
| Ручной QA / ретушь | 1 150 | 12-18 мин ручного труда на аккаунт |
| Поддержка и правки | 600 | CS time allocation |
| Платёжный эквайринг | 747 | ~3% от 24 900 ₽ |
| Прочая переменная инфраструктура | 0 | включено выше |
| **Итого COGS** | **4 997** |  |

- **Выручка на клиента/мес:** 24 900 ₽
- **Валовая прибыль на клиента/мес:** 19 903 ₽
- **Gross Margin / Contribution Margin:** **79.9%**

## 4) CAC по каналам и воронка

### 4.1 CAC по каналам

| Канал | Показ клика/лида | SQL / demo | New paying customers / мес | Расходы канала, ₽/мес | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|
| Paid social (VK/Telegram) | 1 200 лидов | 48 SQL | 3 | 300 000 | 100 000 |
| Affiliates / career creators | 220 лидов | 30 SQL | 3 | 180 000 | 60 000 |
| Outbound to SMB agencies / HR boutiques | 180 аккаунтов | 18 встреч | 2 | 210 000 | 105 000 |
| Inbound / SEO / referrals | 90 лидов | 12 SQL | 2 | 70 000 | 35 000 |
| **Blended** | **1 690** | **108 SQL** | **10** | **760 000** | **76 000 raw CAC** |

### 4.2 Funnel conversion

| Этап | Paid social | Affiliate | Outbound | Inbound |
|---|---:|---:|---:|---:|
| Visit / target accounts | 24 000 кликов | 220 лидов | 180 аккаунтов | 90 лидов |
| Lead | 1 200 | 220 | 36 replies | 90 |
| SQL / demo | 48 | 30 | 18 | 12 |
| Paying customer | 3 | 3 | 2 | 2 |
| Lead -> paying | 0.25% от клика | 1.36% | 1.11% от target accounts | 2.22% |

## 5) Fully-loaded CAC

### 5.1 Обязательная таблица fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (VK/Telegram/Яндекс.Директ) | 160 000 | базовый performance budget | внутренняя модель по каналу |
| Outbound team FOT (SDR/AE attributed to new) | 286 000 | SDR 150K gross + 30% = 195K; 25% AE 280K gross + 30% = 91K | HH.ru benchmark, вакансии sales / SDR / AE |
| Marketing team FOT (partial allocation) | 156 000 | Growth marketer 120K gross + 30% = 156K; 100% времени на acquisition | HH.ru benchmark |
| Tools (CRM, TG tools, analytics, creative stack) | 45 000 | amoCRM + аналитика + рассылки + creative tools | рыночные SaaS-подписки, внутренняя модель |
| Events / partnerships | 40 000 | партнерские выплаты, карьерные каналы, интеграции | внутренняя модель |
| **Raw CAC stack** | **687 000** | сумма прямых расходов |  |
| Overhead multiplier (x1.5) | 343 500 | mid-market B2B, длиннее цикл и больше касаний | стандарт для mid-market B2B |
| **Fully-loaded acquisition spend** | **1 030 500** | raw × 1.5 |  |

- **New paying customers / мес:** 8-10, в base-case беру **8** для консервативности.
- **Fully-loaded CAC:** **1 030 500 / 8 = 128 813 ₽**
- **Blended raw CAC:** **76 000 ₽**
- **Blended fully-loaded CAC:** **128 813 ₽**

### 5.2 Sanity check по benchmark
- Бенчмарк из задания для **Mid-market SaaS в РФ: 60-250K ₽/клиент**.
- Наш fully-loaded CAC **128.8K ₽** лежит внутри диапазона, то есть модель не занижает acquisition cost.
- Raw CAC 76K без sales/FOT выглядит «красивым», но неполным. Именно поэтому для решения использую **fully-loaded CAC**.

## 6) LTV и churn

### Выбранный benchmark churn
Для SMB/mid-market B2B SaaS по свежему benchmark Optifai, сегмент ACV $10K-$50K показывает **около 2.1% monthly churn**, а SMB ниже этого ACV ближе к **4.2% monthly churn**. Для данного кейса российский пакет дешевле, switching costs низкие, moat слабый, поэтому беру **консервативный churn 5.5% в месяц** как penalty за low-lock-in и visual commodity risk.

### Расчёт
- **ARPA / MRR на клиента:** 24 900 ₽
- **Gross Margin:** 79.9%
- **Churn rate:** 5.5% / мес
- **Lifetime:** 1 / 0.055 = **18.2 мес**
- **LTV:** 24 900 × 79.9% × 18.2 = **362 235 ₽**

| Показатель | Значение |
|---|---:|
| MRR / клиент | 24 900 ₽ |
| Gross Margin | 79.9% |
| Monthly churn | 5.5% |
| Lifetime | 18.2 мес |
| **LTV** | **362 235 ₽** |

## 7) LTV/CAC ratio

- **LTV/CAC = 362 235 / 128 813 = 2.81x**

Интерпретация:
- **>= 3.0x**: investable
- **2.0x-3.0x**: погранично
- **< 2.0x**: слабая экономика

**Итог:** кейс **не инвестиционного качества**, потому что **2.81x < 3.0x**.

## 8) CAC Payback

По правилу из задания считаю так:
- **CAC Payback = CAC / MRR per customer**
- **128 813 / 24 900 = 5.17 мес**

**Итог:** формально payback нормальный, **< 12 мес**, но он не компенсирует две проблемы: низкий ARPA и слишком тяжёлую команду для 50-клиентной базы.

## 9) Contribution Margin %

Для operating unit:
- Revenue: 24 900 ₽
- Variable COGS: 4 997 ₽

**Contribution Margin = (24 900 - 4 997) / 24 900 = 79.9%**

Это сильный показатель на уровне delivery, но недостаточный для инвестиционного кейса, если acquisition и fixed team съедают почти всю маржу.

## 10) Team & FOT

### 10.1 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| CTO / Tech Lead | 1 | 450 000 | 2 | 2 | 135 000 | 585 000 |
| Senior Backend | 1 | 320 000 | 1.5 | 1.5 | 96 000 | 416 000 |
| ML Engineer | 1 | 400 000 | 2.5 | 2 | 120 000 | 520 000 |
| DevOps | 0.5 | 300 000 | 1.5 | 1 | 90 000 | 195 000 |
| Frontend | 0.5 | 250 000 | 1 | 1 | 75 000 | 162 500 |
| SDR | 1 | 150 000 | 1 | 1 | 45 000 | 195 000 |
| AE | 1 | 280 000 | 1.5 | 2.5 | 84 000 | 364 000 |
| Customer Success | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |

**Комментарий:** для малого visual-AI продукта такая команда выглядит уже тяжёлой, но именно она нужна, если бизнес хочет не просто продавать one-off фотки, а удерживать recurring SMB accounts, quality SLA, white-label и вменяемый acquisition engine.

### 10.2 Полная команда, роли, функции, оклады

| Роль | Функция | Cash comp / мес | Fully-loaded / мес |
|---|---|---:|---:|
| Founder / CEO | pricing, partnerships, product decisions, enterprise support | 180 000 | 180 000 |
| CTO / Full-stack lead | core product, infra, release management | 450 000 gross | 585 000 |
| Backend engineer | pipeline, storage, billing, integrations | 320 000 gross | 416 000 |
| Growth marketer | paid acquisition, landing tests, analytics | 130 000 gross | 169 000 |
| Customer success / ops | onboarding, revisions, support, retention | 180 000 gross | 234 000 |
| Designer / retouch contractor | QA templates, promo creatives, edge-case edits | 60 000 | 60 000 |
| Bookkeeping / legal / admin | G&A | 70 000 | 70 000 |
| **Итого cash fixed team** |  |  | **1 714 000 ₽/мес** |

## 11) Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Team FOT cash fixed | 1 714 000 |
| Core software / CRM / analytics / support stack | 61 000 |
| Юр / бухгалтерия / документы / оферта / 152-ФЗ support | 45 000 |
| Office / admin / связь / misc | 20 000 |
| Base brand/content production | 35 000 |
| **Итого fixed costs / мес** | **1 875 000 ₽** |

## 12) Break-even по количеству клиентов и по месяцу

### 12.1 Break-even по client count
- Валовая прибыль с 1 клиента: **19 903 ₽/мес**
- Fixed costs: **1 875 000 ₽/мес**

**Break-even client count = 1 875 000 / 19 903 = 94.2 клиента**

Округляю вверх:
- **Операционный break-even:** **95 активных клиентов**
- **Для EBITDA 500K / мес:** (1 875 000 + 500 000) / 19 903 = **119.3**, то есть **120 клиентов**

### 12.2 Проверка на 50 клиентах
- Revenue: 50 × 24 900 = **1 245 000 ₽**
- Gross profit: 50 × 19 903 = **995 150 ₽**
- EBITDA before growth experiments: **995 150 - 1 875 000 = -879 850 ₽/мес**

**Это прямой FAIL по правилу задания.** Даже на **50 активных клиентах** компания не просто не делает 500K EBITDA, а остаётся в минусе почти **0.88 млн ₽/мес**.

## 13) Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT / мес, ₽ |
|---|---|---:|
| M1 | Founder/CEO, CTO | 765 000 |
| M2 | + Growth marketer | 934 000 |
| M3 | + Backend engineer | 1 350 000 |
| M4 | без новых hires, ramp | 1 350 000 |
| M5 | + Customer success | 1 584 000 |
| M6 | + Designer/retouch contractor | 1 644 000 |
| M7 | + SDR | 1 839 000 |
| M8 | без новых hires | 1 839 000 |
| M9 | + ML engineer | 2 359 000 |
| M10 | без новых hires | 2 359 000 |
| M11 | + AE | 2 723 000 |
| M12 | без новых hires | 2 723 000 |

**Sanity check:** нет 5+ hires в первый месяц, но уже к M7-M12 FOT становится слишком тяжёлым для такого ARPA.

## 14) Burn-to-breakeven и runway

### 14.1 Burn-to-breakeven
Base-case: компания растёт до 50 активных клиентов к M12, но всё ещё убыточна.

| Период | Средний burn / мес, ₽ | Комментарий |
|---|---:|---|
| M1-M3 | 1.4-1.8 млн | build + первые тесты acquisition |
| M4-M6 | 1.8-2.1 млн | запуск growth и support |
| M7-M9 | 2.2-2.6 млн | SDR + платный acquisition + ML hire |
| M10-M12 | 2.5-2.9 млн | попытка ускорить продажи, AE подключён |

При движении к **95 клиентам** суммарный накопленный burn до break-even оцениваю примерно в **24-27 млн ₽**.

### 14.2 Cash runway
- **startup_capital = 18 000 000 ₽**
- При среднем burn **~2.1 млн ₽/мес** runway = **8.6 мес**

**Вывод:** при стартовом капитале 18 млн ₽ компания, скорее всего, заканчивает деньги **до выхода на break-even**. Для такого кейса нужен либо гораздо более высокий ARPA, либо почти полностью self-serve PLG без тяжёлой команды, либо сильный white-label distribution partner.

## 15) Почему demand PASS, а economics REJECT
1. Пользовательская боль реальна, и платить за headshots готовы.
2. Но recurring lock-in слабый, товар частично коммодитизирован.
3. При попытке строить фондовый кейс приходится добавлять sales, support, QA, retention и бренд, а значит fixed cost резко растёт.
4. ARPA в российском SMB слишком мал, чтобы комфортно нести эту команду.
5. На 50 клиентах EBITDA не просто ниже 500K, а отрицательная.

## 16) Финальное решение
**Решение: REJECT.**

Причины:
- **Profit Gate FAIL:** EBITDA **< 500K ₽/мес даже на 50 клиентах**.
- **LTV/CAC = 2.81x**, что **ниже investable threshold 3.0x**.
- Для выхода в нормальную экономику нужно либо:
  - поднять ARPA минимум к 40-50K ₽/мес,
  - либо продавать enterprise/agency white-label,
  - либо возвращаться к почти чистому self-serve без sales-heavy operating model.

## Sources
- T1: Optifai B2B SaaS churn benchmark, Q2 2025-Q1 2026, https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- T2: HeadshotPro official pricing / product positioning, https://www.headshotpro.com/
- T3: Rewardful case study on HeadshotPro affiliate revenue, https://www.rewardful.com/case-studies/headshotpro
- T4: HH.ru vacancy market snapshots for senior backend / sales roles, https://hh.ru/vacancies/senior-backend-developer and related vacancy pages
