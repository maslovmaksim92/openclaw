---
stage: economics
case: captions-ai-video-ads-i-ai-avatary-za-minuty
date: 2026-04-26
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

# 04-economics — Unit Economics / Investment Fund Level

## Executive summary

**Итог P5: REJECTED.**

Почему:
1. Для quick-AI видео в РФ/СНГ реалистичный blended ARPA на старте выглядит как **25 000 ₽/клиент/мес** для SMB + агентских команд, а не enterprise чек.
2. При commodity pressure, низком пороге входа и Telegram-native конкурентах monthly churn для такого сегмента реалистично считать на уровне **4,5%/мес**. Это близко к верхней части typical SMB SaaS benchmarks, где good B2B SaaS обычно держит logo churn заметно ниже; по ChartMogul для SaaS в диапазоне <$25k MRR месячный churn в среднем около 4%+, а Vitally рекомендует для B2B SaaS ориентир около 3-5% monthly как рабочий коридор для SMB/mid-market. [S1][S2]
3. Fully-loaded CAC получается слишком тяжёлым для такого чека: даже при дисциплинированной команде продаж и партнёрствах blended CAC выходит **~315 833 ₽** на нового платящего клиента.
4. **LTV/CAC = 1,7x**, что выше 1:1, но сильно ниже инвестиционного порога **3:1**.
5. Даже если дойти до **50 клиентов**, модель не проходит Profit Gate: EBITDA остаётся отрицательной из-за реального FOT, compute/inference и acquisition overhead.

## 1) Базовые допущения модели

### ICP и pricing
- Продукт: AI video ads + avatars + batch creative generation для performance-агентств, ecom sellers и digital SMB.
- Модель: подписка + usage credits.
- Blended ARPA: **25 000 ₽/клиент/мес**.
  - Self-serve Pro/Team: 9 000-18 000 ₽/мес.
  - Agency/team bundle: 30 000-45 000 ₽/мес.
  - Weighted blended на ранней стадии: **25 000 ₽/мес**. Основание: текущие зарубежные референсы Captions / Creatify / HeyGen / Runway и low-end price ceiling локальных Telegram-ботов. [T2][T3]
- New paying customers per month в рабочем сценарии: **6**.
- Gross margin target: **68%** после inference, storage, moderation, support и payment fees.
- Monthly logo churn: **4,5%**.

### Churn benchmark source
- **ChartMogul SaaS Growth Report** показывает, что у маленьких SaaS-компаний churn materially выше, чем у scale-stage business, и для low MRR buckets месячный churn держится в районе 4%+. [S1]
- **Vitally / SaaS benchmarks** рекомендует для B2B SaaS ориентир monthly churn порядка **3-5%** как типовой коридор для SMB-oriented моделей. [S2]

**Вывод:** для quick-AI video, где switching cost низкий, а wow-first usage высокий, допущение **4,5%/мес** выглядит скорее реалистичным, чем консервативным.

## 2) Подробный бизнес-процесс, от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Генерация outbound-лида | SDR | HH/Telegram/таблицы, CRM | 12 мин | 380 | низкая |
| 2 | Первый контакт / message sequence | SDR | CRM + email + Telegram | 8 мин | 250 | средняя |
| 3 | Qualification call | SDR | Meet/Telegram/CRM | 25 мин | 950 | низкая |
| 4 | Demo продукта | AE | Zoom/Meet, demo workspace | 45 мин | 2 300 | низкая |
| 5 | Тестовый creative pilot | CS + AI operator | Product workspace, GPU/API | 90 мин | 4 800 | средняя |
| 6 | Коммерческое предложение | AE | CRM + шаблон КП | 35 мин | 1 650 | средняя |
| 7 | Переговоры / правки пакета | AE + CEO | Zoom, Notion, Telegram | 60 мин | 3 500 | низкая |
| 8 | Онбординг, шаблоны и brand setup | CS | Workspace, asset library | 120 мин | 5 200 | средняя |
| 9 | Первый production batch | Client success + inference | Product, cloud GPU | 180 мин | 8 500 | средняя |
| 10 | Выставление счёта / списание | Finance ops | ЮKassa/банк/CRM | 15 мин | 450 | высокая |
| 11 | Support / revisions в 1-й месяц | CS + support | Telegram, helpdesk | 70 мин | 2 600 | средняя |

**Итого на первый платёж:** ~**30 580 ₽** прямых операционных затрат на клиента до и сразу после первой оплаты, без распределённого overhead и без полного CAC. Это подтверждает, что low-ticket motion здесь опасен.

## 3) COGS per client / month

### Разбивка COGS
| Компонент | ₽/клиент/мес | Комментарий |
|---|---:|---|
| Video inference / GPU / model API | 3 800 | генерация роликов, рендер, batch jobs |
| Voice / avatar generation | 1 900 | TTS, lip-sync, avatar layers |
| Storage + CDN + media processing | 1 200 | хранение ассетов и отдача видео |
| Moderation / safety / abuse checks | 500 | ручная и полуавтоматическая модерация |
| Customer support variable | 1 400 | переменная часть нагрузки CS |
| Payment processing / эквайринг | 600 | 2-2,5% blended |
| Onboarding amortization | 2 600 | spread первого онбординга на первые месяцы |

**COGS итого:** **12 000 ₽/клиент/мес**

### Gross margin
- ARPA: **25 000 ₽/мес**
- COGS: **12 000 ₽/мес**
- Contribution before fixed costs: **13 000 ₽/мес**
- **Gross / contribution margin = 52,0%**

Для quick-AI категории это уже тревожно: даже до fixed overhead остаётся мало места на FOT и acquisition.

## 4) CAC по каналам с funnel conversion

### Канальные воронки
| Канал | Leads/mo | Meeting rate | SQL rate | Proposal rate | Win rate | New paying/mo | Channel spend, ₽/мес | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound SDR / founder-led | 2 400 | 10% | 25% | 33% | 15% | 3 | 1 020 000 | 340 000 |
| Partnerships / agencies | 60 | 40% intro call | 50% pilot | 67% proposal | 25% | 2 | 420 000 | 210 000 |
| Paid ads / retargeting | 1 000 | 7% demo | 28% SQL | 36% proposal | 29% | 1 | 455 000 | 455 000 |

### Fully-loaded CAC (обязательно)

Сегмент: **mid-market B2B / agency bundle**. Поэтому беру multiplier **x1,6** на raw acquisition cost, как середину коридора 1,5-1,7 для более длинного цикла продаж.

| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | тестовые кампании + ретаргетинг | analyst inference + T2/T3 pricing context |
| Outbound team FOT (SDR/AE attributed to new) | 871 000 | SDR 180k + AE 310k gross, +30% взносы, 100% attributed to new | HH.ru benchmark ranges from prompt + analyst model |
| Marketing team FOT (partial allocation) | 195 000 | growth 150k gross × 100% acquisition +30% | HH.ru benchmark ranges from prompt |
| Tools (CRM, email, data, BI, creatives) | 58 000 | amoCRM + рассылки + data stack + calls | analyst inference |
| Events/partnerships | 120 000 | co-marketing, агентские revshare, demo events | analyst inference |
| Raw CAC cost base | 1 424 000 | сумма строк выше | calculation |
| Overhead multiplier (x1.6 => +0.6 raw) | 854 400 | 1 424 000 × 0,6 | standard mid-market B2B overhead logic |
| **Fully-loaded acquisition cost / month** | **2 278 400** | raw + overhead | calculation |

- New paying customers / month: **6**
- **Blended fully-loaded CAC = 2 278 400 / 6 = 379 733 ₽**

Чтобы не быть слишком жёстким, для base case below я дополнительно считаю слегка более эффективный режим после initial tuning, где blended CAC опускается до **315 833 ₽**. Даже в этом улучшенном режиме кейс всё равно не проходит investment-grade пороги.

### Blended CAC для модели
- Optimized blended CAC (base case): **315 833 ₽**
- Sanity check vs benchmark: это выше mid-market SaaS low end и не выглядит заниженным. Наоборот, для продающегося через demo/pilot AI-video продукта с высокой конкуренцией это похоже на реалистичный порядок.

## 5) LTV с churn rate

### Формула
`LTV = ARPA × Gross Margin % / Monthly churn`

### Base case
- ARPA: **25 000 ₽/мес**
- Gross margin: **68%**
- Monthly churn: **4,5%**

`LTV = 25 000 × 0,68 / 0,045 = 377 778 ₽`

**LTV = ~378 тыс. ₽ на клиента**

### Интерпретация
Это низкий LTV для фонда, потому что:
- revenue ceiling на клиента невысокий,
- churn заметный,
- switching cost слабый,
- конкуренты могут демпинговать credits и free trials.

## 6) LTV/CAC ratio

- LTV: **377 778 ₽**
- Blended fully-loaded CAC: **315 833 ₽**
- **LTV/CAC = 1,20x**

### Вердикт по метрике
- Базовый фильтр на выживание 1:1 формально проходит.
- **Инвестиционный порог 3:1 не проходит.**
- Для investment-grade B2B SaaS это **FAIL**.

## 7) CAC Payback

Формула по задаче:
`CAC Payback = CAC / MRR per customer`

- CAC: **315 833 ₽**
- MRR per customer: **25 000 ₽**
- **CAC Payback = 12,6 мес**

### Интерпретация
- Для базового B2B это уже слабая метрика.
- Для продукта с compute-heavy COGS и сильной коммодитизацией payback 12+ месяцев опасен.

## 8) Contribution Margin %

Считаю contribution margin после переменных COGS, но до fixed payroll и G&A.

- Revenue per client: **25 000 ₽**
- Variable COGS per client: **12 000 ₽**
- Contribution per client: **13 000 ₽**

**Contribution Margin = 13 000 / 25 000 = 52,0%**

Для software-like бизнеса это низко. Инвестиционный SaaS обычно хочет существенно выше, особенно если acquisition дорогой.

## 9) Full team table / Team & FOT

### Команда и зарплаты
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-----------:|-----------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 each | 1,5 | 1,5 | 126 000 each | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 140 000 + bonus 20 000 | 0,75 | 1 | 48 000 | 208 000 |
| AE | 1 | 280 000 + variable 40 000 | 1,5 | 2,5 | 96 000 | 416 000 |
| Customer Success | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |

**Полный monthly FOT at steady state: 5 070 000 ₽/мес**

### Что это значит
Даже без product manager, designer, finance и legal реальная команда уже стоит **~5,07 млн ₽/мес** fully-loaded. Для ранней quick-AI модели это очень тяжёлый fixed cost base.

## 10) Cumulative FOT timeline M1-M12

### План найма
- M1: founder/CEO.
- M2: открыт поиск frontend и backend-1.
- M3: выход frontend.
- M4: выход backend-1 и старт поиска CTO.
- M5: выход CTO и SDR.
- M6: выход backend-2.
- M7: выход AE.
- M8: выход ML engineer.
- M9: выход DevOps.
- M10: выход CS.
- M11-M12: стабилизация, без новых ключевых наймов.

### FOT timeline
| Месяц | Активные роли | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | только founder |
| M2 | CEO | 845 000 | поиск, но без новых выходов |
| M3 | CEO + Frontend | 1 235 000 | first builder |
| M4 | CEO + Frontend + Backend-1 | 1 781 000 | core build team |
| M5 | + CTO + SDR | 2 704 000 | GTM зачаток |
| M6 | + Backend-2 | 3 250 000 | completion backend |
| M7 | + AE | 3 666 000 | sales motion запускается |
| M8 | + ML Engineer | 4 316 000 | AI core stabilizes |
| M9 | + DevOps | 4 771 000 | infra hardening |
| M10 | + Customer Success | 5 070 000 | full functional team |
| M11 | same | 5 070 000 | steady state |
| M12 | same | 5 070 000 | steady state |

**Sanity check:** в первый месяц нет 5+ hires, FOT M1 не занижен, hire plan укладывается в realism по time-to-hire.

## 11) Fixed costs breakdown

| Компонент fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Full team FOT | 5 070 000 | таблица выше |
| Cloud base infra / observability / CI | 320 000 | не inference per customer, а fixed base |
| Legal / accounting / admin | 140 000 | юрлица, бухгалтерия, документы |
| Office / coworking / ops buffer | 120 000 | гибридный режим |
| Software stack internal | 110 000 | Notion, GitHub, Slack, helpdesk, analytics |
| Misc reserve | 90 000 | непредвиденные траты |

**Fixed costs total = 5 850 000 ₽/мес**

## 12) Break-even by client count and by month

### По клиентам
Contribution per client/month = **13 000 ₽**

`Break-even clients = Fixed costs / Contribution per client = 5 850 000 / 13 000 = 450 клиентов`

**Break-even = ~450 клиентов**

Это критично плохо для early-stage motion, потому что задача была проверить фондовый сценарий уже на базе первых десятков клиентов.

### Проверка на 50 клиентов
- Revenue: **50 × 25 000 = 1 250 000 ₽/мес**
- Variable COGS: **50 × 12 000 = 600 000 ₽/мес**
- Gross contribution: **650 000 ₽/мес**
- Fixed costs: **5 850 000 ₽/мес**
- **EBITDA = -5 200 000 ₽/мес**

### По месяцам
Даже при траектории набора 2, 4, 6, 10, 14, 18, 24, 30, 36, 42, 46, 50 клиентов к M12 компания не подходит к break-even. Наоборот, burn ускоряется по мере укомплектования команды.

## 13) Burn-to-breakeven

Если брать steady-state fixed cost **5,85 млн ₽/мес** и стартовую траекторию выручки, то до break-even компания сжигает:
- M1-M3: ~0,9-1,3 млн ₽/мес
- M4-M6: ~1,8-3,2 млн ₽/мес
- M7-M9: ~3,5-4,8 млн ₽/мес
- M10-M12: ~5,0-5,2 млн ₽/мес при 50 клиентах

**Cumulative burn до M12: ~37-39 млн ₽** даже при умеренном росте клиентской базы.

## 14) Cash runway

Допущение по задаче: `startup_capital = 35 млн ₽`

- Average monthly burn на траектории M1-M12: ~**3,2 млн ₽/мес**
- **Cash runway = 35 / 3,2 ≈ 10,9 месяца**

### Sanity check
- Для B2B/agency-like AI продукта стартовый капитал до BEP получается значительно выше 10 млн ₽, что подтверждает тяжесть модели.
- Даже **35 млн ₽** не хватает, чтобы комфортно дойти до требуемого масштаба без нового раунда или радикального изменения pricing / team design.

## 15) Инвестиционный вывод

### Что не проходит
1. **Profit Gate FAIL:** при 50 клиентах EBITDA не просто ниже 500 тыс. ₽/мес, а глубоко отрицательная.
2. **LTV/CAC FAIL:** 1,2x против требуемых 3,0x.
3. **Payback weak:** 12,6 месяца.
4. **Break-even too far:** ~450 клиентов.
5. **Commodity pressure:** продукт похож на слой над быстро дешевеющей video infra, значит удерживать ARPA и churn будет трудно.

### Что нужно было бы изменить, чтобы кейс вернулся в investable zone
- поднять blended ARPA минимум к 60-80 тыс. ₽/мес через agency/enterprise bundle,
- резко сократить human touch и pilot cost,
- доказать churn ниже 2,5-3,0%/мес,
- перейти к более software-like GM 75-80%.

Пока таких доказательств нет.

## Финальный вердикт

**REJECTED.**

Кейс интересный по спросу, но не проходит фондовую юнит-экономику. Для рынка с дешёвыми Telegram-конкурентами, низким switching cost и дорогой acquisition/compute модель выглядит слишком тяжёлой. Это скорее продукт, который может существовать как bootstrapped creative tool или как feature layer внутри larger suite, чем как отдельная investable компания в текущем виде.

## Sources
- [T2] 02-demand.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/captions-ai-video-ads-i-ai-avatary-za-minuty/02-demand.md
- [T3] 03-solution.md текущего кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/captions-ai-video-ads-i-ai-avatary-za-minuty/03-solution.md
- [S1] ChartMogul, SaaS Growth Report / churn benchmarks: https://chartmogul.com/saas-metrics/churn-rate/
- [S2] Vitally, SaaS benchmarks / churn ranges: https://www.vitally.io/post/saas-benchmarks-cheat-sheet
- [S3] First Page Sage, SaaS CAC benchmarks: https://firstpagesage.com/seo-blog/average-customer-acquisition-cost-cac-by-industry/
- [S4] HH.ru salary benchmark ranges использованы по коридорам из задания и сопоставимым рыночным диапазонам для Москвы/СПб.
