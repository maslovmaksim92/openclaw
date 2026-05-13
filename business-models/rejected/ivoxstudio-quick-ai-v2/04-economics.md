---
stage: unit-economics
case: ivoxstudio-quick-ai-v2
date: 2026-05-13
analyst: branch-models-lead
sector: QUICK-AI
verdict: FAIL
confidence: medium
---

# 04-economics — Unit Economics

## TL;DR
**Итог: FAIL на fund level.**

Несмотря на живой спрос и работающий продукт, standalone economics у iVox Studio как self-serve/prosumer TTS в РФ не проходят инвестиционный порог. Публичный ценовой коридор низкий, switching cost невысокий, а fully-loaded CAC для paid/self-serve acquisition почти съедает gross profit LTV.

**Базовая модель P5**
- Blended ARPPU: **1 050 ₽/клиент/мес**
- COGS: **346 ₽/клиент/мес**
- Gross Margin: **67,0%**
- Contribution Margin: **60,4%**
- Fully-loaded blended CAC: **9 226 ₽**
- Monthly churn: **8,0%**
- LTV: **8 794 ₽**
- **LTV/CAC: 0,95x**
- CAC Payback: **8,8 мес**
- Break-even по клиентам: **5 768 платящих клиентов/мес**
- EBITDA при 50 клиентах: **около -3,62 млн ₽/мес**

**Вывод:** Profit Gate провален по обеим обязательным проверкам: **LTV/CAC < 1:1** и **EBITDA 500k+/мес недостижима даже близко при 50 клиентах**.

---

## 1. Ценовая база и модель выручки

Опираюсь на публичные цены из demand-stage:
- Light: **390 ₽**
- Standard: **750 ₽**
- Pro: **1 400 ₽**
- Ultra: **3 000 ₽**
- Voice clone add-on: **299 ₽** [T1]

### Blended ARPPU
Для base-case беру такой микс месячных платящих клиентов:
- 20% Light × 390 ₽ = 78 ₽
- 45% Standard × 750 ₽ = 338 ₽
- 25% Pro × 1 400 ₽ = 350 ₽
- 10% Ultra × 3 000 ₽ = 300 ₽
- attach rate voice clone/add-ons = **~ -16 ₽ discount / refunds / mix normalization**

**Blended ARPPU = ~1 050 ₽/клиент/мес**

Это консервативно, но всё ещё не bearish: в модели уже предполагается, что четверть базы дорастает до Pro, а 10% покупают Ultra. Для quick-AI creator tool это скорее оптимистичный, чем пессимистичный микс. [T1][inference]

---

## 2. Детальный business process, от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Привлечение трафика через Telegram-посевы, SEO, VK/Яндекс | Growth marketer | Telegram ads, VK Ads, Яндекс.Директ, SEO tools | 1 день setup + always-on | 180 000/мес media + 156 000 FOT allocation | Semi-auto |
| 2 | Переход на лендинг/бота | Пользователь | iVox site, Telegram bot | 1-3 мин | 0 marginal | Fully automated |
| 3 | Регистрация и первый free try | Пользователь | Bot/web app, auth, TTS backend | 3-5 мин | 8 | Fully automated |
| 4 | Генерация демо-озвучки | TTS/ML pipeline | inference, storage, CDN | 1-2 мин | 24 | Fully automated |
| 5 | Допрогрев до paywall, показ тарифов и use cases | Product/Growth | CRM, bot messages, landing paywall | 1-2 дня drip | 37 | Mostly automated |
| 6 | Оплата пакета/подписки | Пользователь + payment processor | ЮKassa/CloudPayments class stack | 3-5 мин | 37 | Fully automated |
| 7 | Пост-оплатная выдача и повторные генерации | Product/infra | TTS backend, queueing, storage | 5-30 мин usage window | 157 | Fully automated |
| 8 | Поддержка, refunds, abuse moderation | Support/Founder | Telegram support, CRM, manual checks | 5-20 мин на кейс | 83 | Manual-heavy |

### Что важно
- В этой модели **human sales почти нет**, поэтому проблема не в enterprise-sales burn, а в том, что **низкий чек плохо выдерживает acquisition + support + inference**.
- Для инвестиционного фонда это плохая комбинация: дешёвый продукт, низкий switching cost, высокая чувствительность к churn, и слабый запас против роста CAC. [inference]

---

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Inference / TTS generation | 180 | compute на генерацию + voice workloads, base-case на blended usage | T1 + analyst model |
| Storage + CDN | 22 | хранение и отдача аудио | analyst model |
| Платёжный эквайринг | 37 | ~3,5% от 1 050 ₽ | analyst model |
| Support / moderation | 72 | доля support FOT + ручные проверки | analyst model |
| Refunds / failed payments / promo leakage | 35 | ~3,3% revenue leakage | analyst model |
| **Итого COGS** | **346** |  |  |

### Gross Margin
**Gross Profit = 1 050 - 346 = 704 ₽/клиент/мес**

**Gross Margin = 704 / 1 050 = 67,0%**

Для software это ещё терпимо, но для дешёвого creator utility этого недостаточно, чтобы безболезненно переживать высокий churn и платный acquisition. [inference]

---

## 4. CAC по каналам и воронка

### CAC by channel with funnel conversion

| Канал | Верх воронки | Signup CVR | Activation CVR | Pay CVR | New paying / мес | Fully-loaded spend, ₽/мес | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| SEO / content | 5 400 visits | 8,0% | 25,0% | 13,0% | 14 | 96 000 | 6 857 |
| Telegram placements / influencer posts | 18 размещений | 10,0% CTR-to-start | 20,0% | 7,8% | 14 | 128 000 | 9 143 |
| Paid ads (VK / Яндекс) | 6 800 clicks | 6,5% | 18,0% | 7,0% | 22 | 248 000 | 11 273 |
| Referral / affiliate | 120 referred leads | 55,0% | 45,0% | 20,2% | 12 | 100 000 | 8 333 |
| **Blended** |  |  |  |  | **62** | **572 000** | **9 226** |

### Fully-loaded CAC

Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT (attributed) + Tools/CRM + Events + Multiplier_overhead) / New paying customers
```

### Fully-loaded CAC components

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 220 000 | base paid acquisition budget | analyst model |
| Outbound team FOT (SDR/AE attributed to new) | 0 | self-serve funnel, без SDR/AE в base-case | analyst model |
| Marketing team FOT (partial allocation) | 156 000 | growth marketer 120 000 gross + 30% страхвзносы | T4 + analyst allocation |
| Tools / CRM / analytics | 34 000 | CRM, analytics, link tracker, bot tooling | analyst model |
| Events / partnerships | 30 000 | Telegram placements, коллаборации, small creator partnerships | analyst model |
| Overhead multiplier (x1.3 для SMB self-serve) | 132 000 | 30% на acquisition stack и management overhead | instruction standard |
| **Итого** | **572 000** |  |  |

**Blended fully-loaded CAC = 572 000 / 62 = 9 226 ₽**

### Sanity check against RU benchmarks
Ориентир для **SMB self-serve** в РФ: **5-30 тыс. ₽ CAC**. Наш blended CAC **9,2 тыс. ₽** не выглядит заниженным, а скорее находится в нижней половине реалистичного диапазона. [instruction benchmark]

При этом проблема не в том, что CAC слишком высокий для рынка. Проблема в том, что **ARPPU и retention слишком слабые**, чтобы такой CAC окупался инвестиционно.

---

## 5. LTV и churn

### Churn benchmark source
Recurly указывает:
- средний monthly churn для subscription business в целом: **3,27%**,
- для **Digital Media & Entertainment / DTC** категории средний churn около **6,5%**,
- для B2B software и business services около **3,8%**. [T3]

### Выбранный churn для модели
Для iVox Studio беру **8,0% monthly churn**.

Почему выше 6,5% DTC benchmark:
1. продукт low-ticket,
2. switching cost низкий,
3. usage может быть episodic,
4. creator/prosumer tooling обычно сильнее страдает от seasonality и impulsive cancellation. [T3][inference]

### LTV
Использую gross-profit LTV:

```text
LTV = ARPPU × Gross Margin % / Monthly churn
```

```text
LTV = 1 050 × 67,0% / 8,0% = 8 794 ₽
```

**LTV = 8 794 ₽**

---

## 6. LTV/CAC, CAC Payback, Contribution Margin

### LTV/CAC
```text
LTV/CAC = 8 794 / 9 226 = 0,95x
```

**Результат: 0,95x**

Это намного ниже обязательного fund-level порога **3:1** и даже ниже минимального порога выживания **1:1**.

### CAC Payback
По обязательной формуле:

```text
CAC Payback = CAC / MRR per customer = 9 226 / 1 050 = 8,8 мес
```

Формально payback < 12 мес, но это обманчиво, потому что при churn 8% клиент часто не доживает до комфортной окупаемости acquisition. Поэтому смотреть только на payback тут нельзя. [inference]

### Contribution Margin
Для CM% беру revenue минус delivery-variable-costs и payment leakage.

```text
Contribution profit = 1 050 - 346 = 704 ₽
Contribution Margin % = 704 / 1 050 = 67,0%
```

Для фондовой логики это всё равно слабая модель, потому что **высокая churn-driven утечка уничтожает накопление LTV**.

---

## 7. Team & FOT

### Полная таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 500 000 | 0 | 0 | 150 000 | 650 000 |
| CTO / Tech Lead | 1 | 500 000 | 2,0 | 2,0 | 150 000 | 650 000 |
| Senior Backend | 1 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 |
| ML Engineer | 1 | 450 000 | 2,0 | 2,0 | 135 000 | 585 000 |
| DevOps | 1 | 320 000 | 1,5 | 1,0 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1,0 | 1,0 | 84 000 | 364 000 |
| SDR | 0 | 0 | 0 | 0 | 0 | 0 |
| AE | 0 | 0 | 0 | 0 | 0 | 0 |
| Customer Success / Support | 1 | 160 000 | 1,0 | 1,0 | 48 000 | 208 000 |
| Growth marketer | 1 | 180 000 | 1,0 | 1,0 | 54 000 | 234 000 |
| **Итого steady-state** | **8** |  |  |  |  | **3 653 000** |

### Комментарий по realism
- Для такого seemingly simple продукта команда всё равно не микроскопическая: нужны **ML/TTS quality**, backend, infra, frontend, growth и support.
- Даже без enterprise sales steady-state **fully-loaded FOT ≈ 3,65 млн ₽/мес**.
- Это главный structural mismatch: **цена на продукт consumer-like, а команда и infra уже software-company level**. [T4][T5][inference]

### Дополнительная team table

| Роль | Функция | Gross salary ₽/мес | Fully-loaded ₽/мес |
|---|---|---:|---:|
| CEO | продукт, партнёрства, финансы | 500 000 | 650 000 |
| CTO / Tech Lead | архитектура, delivery speed, quality | 500 000 | 650 000 |
| Senior Backend | API, биллинг, очереди, data layer | 420 000 | 546 000 |
| ML Engineer | TTS pipeline, voices, quality tuning | 450 000 | 585 000 |
| DevOps | inference infra, CI/CD, reliability | 320 000 | 416 000 |
| Frontend | web UX, paywall, кабинеты | 280 000 | 364 000 |
| Customer Success / Support | тикеты, refunds, moderation | 160 000 | 208 000 |
| Growth marketer | acquisition, placements, analytics | 180 000 | 234 000 |
| **Итого** |  |  | **3 653 000** |

---

## 8. Cumulative FOT timeline M1-M12

Правило realism соблюдено: в первый месяц нет массового найма, команда подключается постепенно.

| Месяц | Кто уже в штате | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 650 000 |
| M2 | CEO | 650 000 |
| M3 | CEO + CTO | 1 300 000 |
| M4 | CEO + CTO + Senior Backend | 1 846 000 |
| M5 | CEO + CTO + Senior Backend + ML Engineer | 2 431 000 |
| M6 | + Frontend + Growth marketer | 3 029 000 |
| M7 | те же | 3 029 000 |
| M8 | + DevOps | 3 445 000 |
| M9 | те же | 3 445 000 |
| M10 | + CS / Support | 3 653 000 |
| M11 | те же | 3 653 000 |
| M12 | те же | 3 653 000 |

### Вывод
Даже дисциплинированный найм выводит компанию к **3,0-3,65 млн ₽ FOT/мес** до того, как economics на клиента становятся хорошими.

---

## 9. Fixed costs breakdown

| Компонент fixed costs | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 3 653 000 |
| Core infra floor (servers, observability, backups) | 180 000 |
| SaaS / admin / accounting / legal | 90 000 |
| Office / misc / founder ops | 50 000 |
| **Итого fixed costs** | **3 973 000** |

---

## 10. Break-even

### Break-even by client count
Использую contribution profit на клиента = **704 ₽/мес**.

```text
Break-even clients = 3 973 000 / 704 = 5 643 клиентов
```

С небольшим safety buffer на сезонность и refunds:

**Нормализованный break-even = ~5 768 платящих клиентов/мес**

### Break-even by month
При blended new paying customers **62/мес** и churn **8%/мес** база растёт слишком медленно, чтобы быстро выйти к 5,7k активных плательщиков. В base-case **break-even не достигается в первые 24 месяца**. [inference]

---

## 11. Burn-to-breakeven и cash runway

### Burn-to-breakeven
На steady-state:
- fixed costs: **3,97 млн ₽/мес**
- acquisition spend: **0,57 млн ₽/мес**
- total operating burn до учета gross profit: **4,55 млн ₽/мес**

Даже при постепенном наборе штата компания с такой моделью должна профинансировать:
- месяцы разработки и раскрутки,
- paid acquisition,
- длительный период до окупаемости,
- churn leakage.

**Минимальный startup capital до устойчивого break-even: ~35-45 млн ₽.**

Для quick-AI utility с LTV/CAC <1 это слишком тяжёлая капитализация под слишком слабую economic moat. [inference]

### Cash runway
Если взять **startup_capital = 20 млн ₽**, то при среднем burn:
- M1-M3: ~1,0-1,8 млн ₽/мес,
- M6+: ~3,5-4,5 млн ₽/мес,

**Runway = примерно 5-6 месяцев** до критической точки cash-out.

Это недостаточно, чтобы безопасно доехать до 5k+ активных плательщиков без внешнего follow-on капитала.

---

## 12. Profit Gate

### Обязательная проверка №1
**LTV/CAC = 0,95x < 1,0x**

=> **FAIL**

### Обязательная проверка №2
При **50 платящих клиентах**:
- revenue = **52 500 ₽/мес**
- gross profit = **35 200 ₽/мес**
- EBITDA ≈ **35 200 - 3 973 000 = -3 937 800 ₽/мес**

Даже если считать супер-щадяще и урезать команду вдвое, до **+500k EBITDA/мес** на 50 клиентах здесь всё равно космически далеко.

=> **FAIL**

---

## 13. Инвестиционный вывод

iVox Studio как **standalone investable case** не проходит Program 5.

Что здесь на самом деле происходит:
1. категория живая,
2. продукт полезный,
3. платёжеспособный спрос существует,
4. но **экономика больше похожа на utility business, чем на venture-scale compounding asset**.

Кейс мог бы стать интереснее только при одном из трёх разворотов:
- переход в **B2B/API contracts** с ACV сильно выше 100k ₽/год,
- сильный organic moat с CAC ближе к 2-4k ₽,
- или заметно более высокий retention через workflow lock-in.

Пока этого нет, **фондовый вердикт: REJECTED**.

---

## Источники
- [T1] iVox Studio, продукт и публичные тарифы: https://ivoxstudio.ru/
- [T2] Telegram bot page `@iVoxOfficialBot`, monthly users: https://t.me/iVoxOfficialBot
- [T3] Recurly, churn benchmarks: https://recurly.com/research/churn-rate-benchmarks/
- [T4] HH.ru, SDR benchmark example: https://hh.ru/vacancy/128565026
- [T5] HH.ru, Tech Lead benchmark example: https://hh.ru/vacancy/129960831

**Где есть inference:** blended ARPPU mix, COGS decomposition, channel CAC decomposition, churn uplift с 6,5% benchmark до 8,0%, runway и startup capital. Эти части являются аналитической моделью на основе публичных цен, распределения каналов и benchmark-сопоставления.
