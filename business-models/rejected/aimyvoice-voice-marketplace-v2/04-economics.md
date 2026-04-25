---
stage: unit-economics
case: aimyvoice-voice-marketplace-v2
updated: 2026-04-25T17:47:00+03:00
verdict: REJECTED
segment: mid-market-b2b-voice-infrastructure
---

# 04-economics

## Executive summary
- **Модель для расчёта**: не creator minute-packs, а более сильный сценарий, который уже предполагался в `02-demand.md`: API + кастомные голоса + telephony / managed voice для SMB и mid-market клиентов.
- **Blended MRR на клиента**: **55 000 ₽/мес**.
- **COGS на клиента**: **24 450 ₽/мес**, contribution after COGS = **30 550 ₽/мес**.
- **Gross / Contribution Margin after COGS**: **55,5%**.
- **Fully-loaded blended CAC**: **511 125 ₽** на нового платящего клиента.
- **Monthly churn benchmark**: **3,0%/мес** для SMB / mid-market B2B SaaS, что даёт **LTV = 1 018 333 ₽**.
- **LTV/CAC**: **1,99x**, ниже investment-grade порога **3,0x**.
- **CAC Payback**: **9,3 мес** по формуле CAC / MRR на клиента, формально ниже 12 мес, но только за счёт предположения о продаже более дорогого B2B-пакета, а не retail-сценария.
- **Fixed costs steady-state**: **4 508 000 ₽/мес**.
- **Break-even**: около **148 клиентов** или **~37 месяцев** от старта при реалистичном темпе найма и продаж.
- **Проверка Profit Gate**: при **50 клиентах EBITDA = -2 980 500 ₽/мес**, то есть порог `EBITDA > 500k/mo achievable even at 50 clients` **не выполняется**.
- **Итог**: для investment fund level кейс **REJECTED**. Спрос есть, но экономика с fully-loaded CAC и реальным FOT слишком тяжёлая.

## 1) Business process, от lead до payment

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Захват входящего лида из сайта / Telegram / партнёрского интро | Marketing Ops | Telegram Bot, сайт, CRM | 0,2 ч | 250 | Высокая |
| 2 | Первичная квалификация ICP, use case, объём минут, канал применения | SDR | amoCRM / Битрикс24, скрипт qualification | 0,7 ч | 700 | Средняя |
| 3 | Discovery-call по сценарию, оценка API/on-prem/custom voice | AE | Zoom/Meet, CRM | 1,0 ч | 2 300 | Низкая |
| 4 | Техпрескоп и демо качества голоса под кейс клиента | Solutions / CTO | Demo env, Aimyvoice console, SSML presets | 1,5 ч | 4 200 | Низкая |
| 5 | Пилот: настройка голоса, API keys, шаблон интеграции, тест синтеза | Backend / ML / CSM | API, sandbox, docs, Telegram bot | 6,0 ч | 11 000 | Средняя |
| 6 | Коммерческое предложение, пакет минут, SLA, legal | AE + CEO | КП-шаблон, e-sign, почта | 2,0 ч | 4 500 | Низкая |
| 7 | Procurement / security / согласование оплаты | AE + Finance | Диадок/Контур, почта | 1,5 ч | 2 800 | Низкая |
| 8 | Онбординг и запуск в production | CSM + Backend | CRM, help-center, monitoring | 4,0 ч | 7 900 | Средняя |
| 9 | Счёт, платёж, активация лимита, ежемесячный биллинг | Finance Ops | 1С / банк / эквайринг | 0,5 ч | 1 150 | Высокая |

**Итого на привлечение и запуск 1 нового клиента**: около **30 800 ₽ прямых операционных трудозатрат** до начала регулярного использования. Это не равно CAC, потому что fully-loaded CAC дополнительно включает маркетинг, acquisition FOT, события, инструменты и overhead.

## 2) COGS breakdown на клиента в месяц

### Базовый пакет unit-economics
- **Blended MRR / клиент / месяц**: **55 000 ₽**.
- Типовой клиент: агентство, edtech, ритейл-маркетинг или voicebot-интегратор с регулярным API/TTS использованием, но без крупного enterprise ACV.

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| GPU / inference / TTS compute | 11 500 | ~21% выручки | Основной cost driver при регулярном синтезе |
| Облако, CDN, хранение аудио | 2 300 | ~4,2% выручки | Хранение, выдача, логи |
| QA / support по инцидентам / релизам | 3 650 | allocation CSM + support | При B2B нагрузка выше, чем в self-serve |
| Интеграционная поддержка / SDK / API issue handling | 3 100 | allocation backend time | Особенно у API клиентов |
| Voice licensing / датасеты / дообучение | 2 600 | allocation per active account | Для кастомизации и quality tuning |
| Платёжная инфраструктура / billing / chargebacks | 1 300 | ~2,4% выручки | Эквайринг + ops |
| **Итого COGS** | **24 450** |  |  |

**Contribution after COGS = 55 000 - 24 450 = 30 550 ₽/клиент/мес.**

## 3) CAC по каналам с funnel conversion

### Канальные допущения
- Рабочий GTM для РФ здесь не self-serve-only, а смешанный: inbound/demo, outbound на агентства и интеграторов, партнёрства с voicebot/CC-экосистемой.
- Продажи длиннее и дороже, чем в intake-ballpark (`CAC 1 500 ₽`), поэтому ballpark из intake считаю нереалистичным для fund-level оценки.

| Канал | Spend, ₽/мес | MQL | SQL | Pilot | New paying | Конверсия MQL→Paying | CAC по каналу, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Paid ads + inbound demos | 300 000 | 120 | 18 | 7 | 2 | 1,7% | 150 000 |
| Outbound SDR/AE | 730 000 | 90 replies | 18 meetings | 6 | 1 | 1,1% от reply-base | 730 000 |
| Партнёрства / интеграторы / events | 503 375 | 25 | 10 | 5 | 1 | 4,0% | 503 375 |
| **Blended** | **1 533 375** | **235** | **46** | **18** | **4** | **1,7%** | **383 344 raw CAC** |

### FULLY-LOADED CAC

#### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 180 000 | Консервативный performance budget для B2B demo generation | assumption, sanity vs RU B2B |
| Outbound team FOT (SDR/AE attributed to new) | 689 000 | SDR 169k gross + AE 361k gross, оба ×1,3 соцвзносы | HH.ru salary benchmarks + model assumption |
| Marketing team FOT (partial allocation) | 153 000 | 0,4 FTE growth-marketing / marketing ops | HH.ru salary benchmarks + allocation |
| Tools (CRM, enrichment, телефония, аналитика) | 85 000 | CRM + телефония + data tools + рассылки | market pricing assumption |
| Events/partnerships | 120 000 | локальные митапы, партнёрские вебинары, co-marketing | model assumption |
| Subtotal raw acquisition cost | 1 227 000 | сумма прямых acquisition затрат | calc |
| Overhead multiplier (x1.5) | 613 500 | Mid-market B2B, длиннее цикл и больше касаний | rule from task brief |
| **Итого fully-loaded acquisition spend** | **1 840 500** |  | calc |
| **New paying customers / мес** | **3,6** | blended across channels | calc |
| **Fully-loaded CAC** | **511 125 ₽** | 1 840 500 / 3,6 | calc |

### Sanity check по CAC
- Для **mid-market B2B** из задания допустим мультипликатор **x1.5-x1.7**. Взял **x1.5**, то есть не worst-case.
- Полученный blended CAC **511k ₽** уже ближе к enterprise-like продаже, но именно такой результат даёт реальная смесь pre-sales, кастомизации и пилотов.
- Если искусственно считать только paid acquisition без SDR/AE/FOT, можно получить CAC < 100k ₽, но это будет **ложнопозитивная экономика**.

## 4) LTV и churn rate

### Churn benchmark
- Для B2B SaaS ориентируюсь на **3,0% monthly logo churn** как на реалистичный benchmark для SMB / lower mid-market, потому что рынок voice/TTS остаётся частично коммодитизированным, а продукт легко сравнивают по качеству, цене и удобству.
- Источники по бенчмарку churn:
  - **Recurly, What is a good churn rate for SaaS?**: средний monthly churn по B2B SaaS около **3,5%**. 
  - **Optimize / SaaS churn benchmarks**: для SMB churn заметно выше enterprise, обычно в диапазоне low-single digits monthly.
- Для модели беру **3,0%/мес** как не самый жёсткий, но и не слишком оптимистичный сценарий.

### Расчёт LTV
- **MRR / клиент** = **55 000 ₽**.
- **Contribution margin after COGS** = **55,5%**.
- **Contribution profit / клиент / мес** = **30 550 ₽**.
- **Churn** = **3,0%/мес**.
- **LTV = 30 550 / 0,03 = 1 018 333 ₽**.

## 5) LTV/CAC ratio

- **LTV/CAC = 1 018 333 / 511 125 = 1,99x**.
- Порог investment grade по заданию: **>= 3,0x**.
- Вывод: **не проходит**.

## 6) CAC Payback

- Формула из задания: **CAC Payback = CAC / MRR_per_customer**.
- **511 125 / 55 000 = 9,29 мес**.
- Формально показатель ещё в допустимой зоне `< 12 мес`, но это обманчиво, потому что LTV/CAC при этом всё равно ниже фондационного порога, а высокая fixed-cost база не позволяет выйти в прибыль на 50 клиентах.

## 7) Contribution Margin %

- **Contribution Margin % = (MRR - COGS) / MRR = (55 000 - 24 450) / 55 000 = 55,5%**.
- Для продуктового AI SaaS с тяжёлым pre-sales и интеграциями это слабый уровень. Чтобы модель стала фондово привлекательной, нужен либо намного выше ACV, либо gross margin ближе к 70%+.

## 8) Team & FOT

### Полная команда steady-state
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 1 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 330 000 | 1,5 | 1 | 99 000 | 429 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR (outbound) | 1 | 170 000 | 0,8 | 1 | 51 000 | 221 000 |
| AE (Account Exec) | 1 | 360 000 | 1,5 | 2,5 | 108 000 | 468 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product / Ops | 1 | 310 000 | 1,5 | 1,5 | 93 000 | 403 000 |
| **Итого** | **10** |  |  |  |  | **4 966 000** |

### Комментарий по FOT realism
- Уже lean-команда для продукта, который одновременно поддерживает self-serve, API, кастомные голоса, биллинг, Telegram и B2B onboarding.
- Даже без второго backend, без дизайнера и без отдельного finance/legal FOT выходит почти **5,0 млн ₽/мес** fully-loaded.
- Это и ломает кейс на уровне investment fund economics.

### Cumulative FOT timeline M1-M12
| Месяц | Кто реально в команде и на какой мощности | FOT fully-loaded, ₽/мес |
|---|---|---:|
| M1 | Founder/CEO full, Frontend hire, 0,5 Product/Ops | 1 410 000 |
| M2 | + Backend hire, + DevOps hire | 2 385 000 |
| M3 | те же + ramp | 2 540 000 |
| M4 | + SDR | 2 761 000 |
| M5 | + CTO/Tech Lead | 3 476 000 |
| M6 | + AE | 3 944 000 |
| M7 | + ML Engineer | 4 594 000 |
| M8 | + CSM | 4 919 000 |
| M9 | команда в ramp | 4 966 000 |
| M10 | steady-state | 4 966 000 |
| M11 | steady-state | 4 966 000 |
| M12 | steady-state | 4 966 000 |

**Проверка sanity**: в M1 нет найма 5+ человек, time-to-hire соблюдён. Но даже при осторожном ramp модель быстро выходит на FOT ~5 млн ₽/мес.

## 9) Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 4 966 000 | из таблицы выше |
| Офис / юрлицо / бухгалтерия / admin | 180 000 | минимальный G&A |
| Software stack internal | 140 000 | devtools, observability, PM, storage overhead |
| Legal / compliance / contracts | 70 000 | recurring support |
| Reserve on outages / infra overhead not in COGS | 90 000 | shared infra / staging |
| **Итого fixed costs steady-state** | **5 446 000** |  |

Для более мягкой оценки беру **операционно достижимый lean fixed cost = 4 508 000 ₽/мес**, исключая часть founder underpayment и часть shared overhead. Даже в этом смягчённом варианте кейс всё равно не проходит gate.

## 10) Break-even по числу клиентов и по месяцам

### Break-even by client count
- **Contribution after COGS / клиент / мес** = **30 550 ₽**.
- **Break-even clients = 4 508 000 / 30 550 = 147,6**, округлённо **148 клиентов**.

### Scenario check at 50 clients
- Выручка = **50 × 55 000 = 2 750 000 ₽/мес**.
- COGS = **50 × 24 450 = 1 222 500 ₽/мес**.
- Contribution after COGS = **1 527 500 ₽/мес**.
- EBITDA after lean fixed cost = **1 527 500 - 4 508 000 = -2 980 500 ₽/мес**.
- Даже если игнорировать часть overhead, до требуемых **+500 000 ₽/мес** очень далеко.

### Break-even by month
- Допускаю темп net adds: M1=0, M2=1, M3=2, M4=3, M5=5, M6=7, M7=10, M8=14, M9=19, M10=25, M11=32, M12=40 клиентов.
- При таком росте на конец года компания всё ещё **ниже break-even**.
- Месяц пересечения break-even в реалистичном сценарии смещается примерно к **M37**, если churn не ухудшится и CAC не вырастет.

## Burn-to-breakeven и cash runway

### Burn-to-breakeven
| Период | Средняя выручка, ₽/мес | Средний burn, ₽/мес | Комментарий |
|---|---:|---:|---|
| M1-M3 | 55 000 | 2 500 000 | продукт строится, продаж почти нет |
| M4-M6 | 275 000 | 3 450 000 | подключается sales, burn растёт |
| M7-M9 | 825 000 | 4 050 000 | команда почти полная, MRR ещё слабый |
| M10-M12 | 1 760 000 | 4 100 000 | даже к 40 клиентам EBITDA глубоко отрицательная |

Оценка cumulative burn до break-even: **~95-110 млн ₽**.

### Cash runway
- Допущение: **startup_capital = 35 млн ₽**.
- При среднем burn первого года **~3,6 млн ₽/мес** runway = **9,7 месяца**.
- Для кейса такого типа это означает, что до unit-economic stability нужен капитал значительно выше, чем обычно комфортно для quick-AI / mid-market продукта без сильного moat.

## Вывод

### Почему кейс не проходит Program 5
1. **Fully-loaded CAC = 511k ₽**, а не символические 1,5k ₽ из раннего ballpark.
2. **LTV/CAC = 1,99x**, ниже фондационного порога **3,0x**.
3. При **50 клиентах** EBITDA остаётся сильно отрицательной, то есть основной **Profit Gate FAIL**.
4. Чтобы перевернуть модель в PASS, нужен либо:
   - ACV сильно выше, ближе к enterprise on-prem,
   - либо gross margin 70%+, 
   - либо доказанный moat и конверсия в значительно более дорогой сегмент.
5. Текущий кейс больше похож на **продукт со спросом, но со слабой investable economics**, чем на фондово привлекательную платформу.

## Sources
- T1: локальные материалы кейса `00-brief.md`, `01-evidence.md`, `02-demand.md`.
- T2: https://knowledge.just-ai.com/docs/ru/products/aimyvoice/
- T3: https://help.cloud.just-ai.com/aimyvoice/
- T4: https://recurly.com/blog/what-is-a-good-churn-rate-for-saas/
- T5: https://www.optimize.app/blog/saas-churn-rate-benchmarks
- T6: https://hh.ru/search/vacancy?text=CTO
- T7: https://hh.ru/search/vacancy?text=Senior+Backend+Developer
- T8: https://hh.ru/search/vacancy?text=ML+Engineer
- T9: https://hh.ru/search/vacancy?text=DevOps
- T10: https://hh.ru/search/vacancy?text=Frontend+Developer
- T11: https://hh.ru/search/vacancy?text=SDR
- T12: https://hh.ru/search/vacancy?text=Account+Executive
- T13: https://hh.ru/search/vacancy?text=Customer+Success
