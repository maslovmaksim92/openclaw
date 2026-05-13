# Unit Economics

## Статус
**Вердикт: REJECTED на этапе P5 Unit Economics.**

Причина отказа не в отсутствии спроса, а в том, что для фонда это **не investment-grade экономика на российском рынке** в выбранном wedge SMB/self-serve video ads. У продукта может быть хороший small business, но при реалистичном FOT, fully-loaded CAC и required build team модель **не даёт 500К+ EBITDA/мес даже близко на 50 клиентах**. Это прямой FAIL по Profit Gate из задания.

---

## 1) Ключевые допущения модели

### Сегмент, который считаю базовым
- Базовый сегмент: **SMB/self-serve sellers + small agencies**.
- Рабочий ARPU для РФ: **7 000 ₽/клиент/мес**.
- Логика цены: это выше low-end Telegram-ботов, но заметно ниже западных self-serve аналогов Topview/HeyGen/Creatify.
- Валовая маржа до sales & marketing: целевой диапазон **70-75%**, в модели беру **72.9%**.
- Churn benchmark: для SMB B2B SaaS беру **4.2% monthly logo churn** как benchmark для ACV < $10K. Источник: Optifai, 939 B2B SaaS companies, Q2 2025-Q1 2026.

### Источники, на которых стоит модель
- Topview pricing: https://www.topview.ai/pricing
- Topview RU pricing snapshot: https://www.topview.ai/ru/pricing?source=official_website
- amoCRM pricing: https://www.amocrm.ru/buy/tariff/
- ЮKassa fees: https://yookassa.ru/docs/support/payments/fees
- Unisender pricing: https://www.unisender.com/ru/prices/
- Yandex Direct CPC rules / budget logic: https://yandex.ru/support/direct/en/strategies/average-cpc
- Yandex Cloud Object Storage pricing: https://yandex.cloud/ru/docs/storage/pricing
- HH senior backend vacancy index: https://hh.ru/vacancies/senior-backend-developer
- HH senior backend example 350K gross: https://hh.ru/vacancy/129266637
- HH ML engineer search: https://hh.ru/vacancies/machine-learning-engineer
- HH DevOps search: https://hh.ru/vacancies/devops-engineer
- HH DevOps example 300-420K gross: https://hh.ru/vacancy/129135377
- HH SDR example: https://hh.ru/vacancy/128565026
- HH Account Executive search: https://hh.ru/vacancies/account_executive
- Churn benchmark: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/

> Примечание: часть операционных норм ниже является аналитическим inference на базе этих источников и типового RU SaaS GTM. Явно помечаю такие места как inference.

---

## 2) Детальная таблица бизнес-процесса: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Уровень автоматизации |
|---|---|---|---|---:|---:|---|
| 1 | Клик по объявлению / переход из SEO / TG | Performance marketer | Яндекс Директ, VK Ads, Telegram посевы | 1-3 мин user time | 120-450 за лид-клик | Высокая |
| 2 | Посадка на лендинг и signup | Growth/PMM | Tilda/Webflow, Метрика | 5-8 мин | 35 | Высокая |
| 3 | Email verification / welcome sequence | CRM marketer | Unisender, email automation | 1 день до первого касания | 12 | Высокая |
| 4 | Пользователь загружает URL/карточку товара | User + product | Web app onboarding | 10-20 мин | 60 | Высокая |
| 5 | AI генерирует первый ролик / avatar demo | Backend/ML stack | inference pipeline + storage | 3-7 мин compute | 310 | Высокая |
| 6 | User смотрит preview, получает watermark/free-limit | Product automation | in-app paywall | 3-10 мин | 18 | Высокая |
| 7 | Retargeting / nurture письма / TG follow-up | Marketing ops | Unisender, retargeting | 3-7 дней | 95 | Высокая |
| 8 | Для тёплых агентств, demo call | Founder/AE | amoCRM, Google Meet/Телемост | 45 мин | 2 800 | Средняя |
| 9 | Trial-to-paid offer / checkout | Product + payments | ЮKassa / cloud payments analog | 5-10 мин | 210 | Высокая |
| 10 | Оплата проходит, счёт/чек, доступ открыт | Billing ops | ЮKassa, CRM, bot/webhooks | 1-5 мин | 115 | Высокая |
| 11 | Onboarding 1-й недели | CS / product automation | email + in-app guides | 30-60 мин spread | 420 | Средняя |
| 12 | Повторное использование и upsell | CS / lifecycle marketing | CRM, product analytics | ongoing | 190 | Средняя |

### Комментарий
- В self-serve SMB цепочка выглядит автоматизированной, но **экономика ломается не в COGS, а в fixed team cost + acquisition load**.
- Для agency сегмента касаний больше, поэтому channel CAC выше и multiplier должен быть уже **1.5**, а не 1.3.

---

## 3) COGS на 1 клиента в месяц

### Базовый SMB-клиент, ARPU 7 000 ₽/мес

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Inference / video generation | 1 050 | mix of short product videos + avatars, conservative inference | inference на базе Topview credit model + market analogs |
| Storage + CDN + выдача файлов | 120 | видеофайлы, превью, трафик | Yandex Cloud Object Storage |
| Support / moderation reserve | 260 | доля CS/time на аккаунт | inference |
| Payment processing | 210 | ~3% от ARPU | ЮKassa fees |
| Third-party SaaS variable share | 170 | e-mail / event / analytics variable apportionment | Unisender + inference |
| Chargeback / failed payment reserve | 90 | 1.3% reserve | inference |
| **Итого COGS** | **1 900** |  |  |

### Вывод по COGS
- **Gross profit на клиента = 7 000 - 1 900 = 5 100 ₽/мес**.
- **Contribution Margin = 5 100 / 7 000 = 72.9%**.
- Для AI video инструмента это нормально, но не спасает модель при маленьком чеке и тяжёлом build/FOT.

---

## 4) CAC по каналам и воронка

### Воронка по каналам

| Канал | Трафик / лиды в мес | Signup CVR | Trial->Paid | Новых paying / мес | Комментарий |
|---|---:|---:|---:|---:|---|
| Paid ads (Яндекс/VK) | 1 800 visits | 10% | 4.4% | 8 | короткий self-serve funnel |
| Content/SEO/community | 900 visits | 14% | 4.8% | 6 | дешевле, но медленнее разгон |
| Outbound/partners/agencies | 120 SQL | 35% demo | 14% close | 6 | выше чек, но длиннее цикл |
| **Итого / blended** | — | — | — | **20** | модель для раннего go-to-market |

### Fully-loaded CAC, обязательный разбор

Формула:

```
Fully-loaded CAC = (Direct marketing spend + Sales team FOT (attributed) + Tools/CRM + Events + Multiplier_overhead) / New paying customers
```

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | тестовый SMB budget | Yandex Direct docs + inference |
| Outbound team FOT (SDR/AE attributed to new) | 286 000 | SDR 170K gross + AE 300K gross, с 30% взносами и 50% attribution to new logo motion | HH.ru vacancy benchmarks + inference |
| Marketing team FOT (partial allocation) | 132 000 | growth marketer 220K gross × 60% × 1.3 | HH-like market norm + inference |
| Tools (CRM, email, analytics, call stack) | 41 000 | amoCRM + Unisender + call tools + attribution stack | amoCRM, Unisender + inference |
| Events/partnerships | 30 000 | small meetups / partner rev-share reserve | inference |
| Subtotal before multiplier | 669 000 | сумма выше | — |
| Overhead multiplier (×1.3) | 200 700 | SMB self-serve multiplier | стандарт из задания |
| **Итого fully-loaded acquisition cost pool** | **869 700** |  |  |
| **Новые paying customers / мес** | **20** | blended monthly acquisition | model |
| **Blended fully-loaded CAC** | **43 485 ₽** | 869 700 / 20 | calc |

### CAC по каналам

| Канал | Spend + allocated team/tool, ₽/мес | New paying / мес | Raw CAC, ₽ | Multiplier | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|
| Paid ads SMB | 250 000 | 8 | 31 250 | ×1.3 | **40 625** |
| Content/SEO/community | 119 000 | 6 | 19 833 | ×1.3 | **25 783** |
| Outbound/agency | 300 000 | 6 | 50 000 | ×1.5 | **75 000** |
| **Blended** | **669 000** | **20** | **33 450** | blended | **43 485** |

### Sanity check против benchmark
- Для SMB self-serve benchmark из задания: **5-30K ₽ raw CAC**.
- Здесь raw CAC blended = **33.45K ₽**, fully-loaded = **43.49K ₽**.
- Это **не заниженная** оценка, наоборот, ближе к реалистичной ранней фазе, где продукт ещё требует nurture, retargeting и ручной support для activation.
- Если считать «как в intake» CAC 3-8K ₽, это был бы явный red flag и недоучёт sales/FOT/tooling.

---

## 5) LTV и churn

### Churn benchmark
- Для ACV < $10K / SMB B2B SaaS Optifai даёт **4.2% monthly churn**.
- Это хорошо подходит к Topview-подобному продукту в сегменте селлеров/малых агентств, где switching cost невысокий, а альтернатив много.

### Расчёт LTV
- ARPU = **7 000 ₽/мес**
- Gross Margin = **72.9%**
- Monthly churn = **4.2%**
- Customer lifetime = **1 / 0.042 = 23.8 мес**
- **LTV = ARPU × GM% / churn = 7 000 × 0.729 / 0.042 = 121 500 ₽**

### Вывод
- **LTV = ~121.5K ₽**
- При честном fully-loaded CAC это не катастрофа, но и не premium-grade outcome для фонда при таком fixed cost и required ramp.

---

## 6) LTV/CAC ratio

- **LTV/CAC = 121 500 / 43 485 = 2.79x**

### Интерпретация
- Требование investment grade из задания: **>= 3:1**
- Фактический результат: **2.79:1**
- Это **ниже инвестиционного порога**.
- Формально это ещё не ниже 1:1, но уже **не fund-grade**.

---

## 7) CAC Payback

- Формула по заданию: **CAC Payback = CAC / MRR per customer**
- **43 485 / 7 000 = 6.21 мес**

### Интерпретация
- Для self-serve SMB это формально приемлемо, так как меньше 12 месяцев.
- Но payback сам по себе не компенсирует слабый LTV/CAC и очень высокий fixed burn.

---

## 8) Contribution Margin %

- Revenue per client = **7 000 ₽/мес**
- Variable cost per client = **1 900 ₽/мес**
- Contribution per client = **5 100 ₽/мес**
- **Contribution Margin = 72.9%**

Это нормальный software-like уровень. Проблема не в gross margin, а в том, что **чек слишком низкий для требуемой команды и acquisition stack**.

---

## 9) Team & FOT

### Полная таблица команды

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2.5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 170 000 | 0.75 | 1 | 51 000 | 221 000 |
| AE | 1 | 330 000 | 1.5 | 2.5 | 99 000 | 429 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Product Manager | 1 | 320 000 | 1.5 | 1.5 | 96 000 | 416 000 |
| Product Designer | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### Total steady-state full team FOT
- Полный steady-state FOT при такой конфигурации = **5 850 000 ₽/мес**.
- Даже если реально стартовать более lean-командой, **ниже ~3.0-3.5 млн ₽/мес быстро не опуститься**, если строить свой продукт, inference orchestration, billing, onboarding и acquisition.

### Hiring realism
- В первый месяц реалистично запустить только founder + 1 senior backend + 1 frontend/contract.
- Нанять 5-7 ключевых людей сразу нельзя без нарушения time-to-hire reality.
- Для ML/CTO/AE требуется ramp, и это удлиняет путь до revenue efficiency.

### Cumulative FOT timeline M1-M12

| Месяц | Кто реально в строю | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO + 1 Senior Backend | 1 391 000 | founder-driven start |
| M2 | + Frontend | 1 781 000 | MVP/web onboarding |
| M3 | + SDR | 2 002 000 | старт paid+outbound |
| M4 | + CTO/Tech Lead (partial productivity) | 2 717 000 | infra/process setup |
| M5 | + ML Engineer | 3 367 000 | quality uplift, avatars/workflows |
| M6 | + 2nd Senior Backend + AE | 4 342 000 | scale GTM + product velocity |
| M7 | + DevOps | 4 797 000 | reliability / cost control |
| M8 | + Customer Success | 5 122 000 | retention support |
| M9 | + Product Manager | 5 538 000 | roadmap discipline |
| M10 | + Designer | 5 850 000 | conversion/product polish |
| M11 | same team | 5 850 000 | full steady state |
| M12 | same team | 5 850 000 | full steady state |

### Вывод по FOT
Даже до полной команды burn становится слишком тяжёлым для ARPU ~7K. Это не значит, что сервис нельзя запустить как bootstrapped small business, но **для фонда это слабый capital efficiency profile**.

---

## 10) Fixed costs breakdown

### Lean operating month (после выхода из MVP, но до полной команды)

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT active team (реалистичный M6-M7 уровень) | 4 342 000 | CEO, CTO, 2 BE, ML, FE, SDR, AE |
| Infra reserve beyond per-client COGS | 180 000 | QA/staging/logging/monitoring |
| CRM / email / analytics / call stack | 41 000 | amoCRM + Unisender + misc |
| Legal / accounting / admin | 85 000 | external back office |
| Content production / brand / site ops | 120 000 | non-performance marketing base |
| Misc reserve | 75 000 | платежи, домены, small tooling |
| **Итого fixed cost / мес** | **4 843 000** |  |

### Строгий минимум для выживания
Если ещё сильнее ужаться и отложить PM/Designer/CS, всё равно рабочий минимум выходит около **4.0-4.8 млн ₽/мес**, если делать продукт самостоятельно и не жить только на founder labor.

---

## 11) Break-even: по клиентам и по месяцам

### Break-even по количеству клиентов
- Contribution per client = **5 100 ₽/мес**
- Fixed cost = **4 843 000 ₽/мес**
- **Break-even clients = 4 843 000 / 5 100 = 950 клиентов**

### Sanity check на 50 клиентов
- Revenue at 50 clients = **350 000 ₽/мес**
- Variable COGS = **95 000 ₽/мес**
- Gross profit = **255 000 ₽/мес**
- EBITDA before fixed cost = **255 000 ₽/мес**
- EBITDA after fixed cost = **-4 588 000 ₽/мес**

Это прямой **FAIL** по Profit Gate. Даже близко нет 500K EBITDA/мес на 50 клиентах.

### Break-even по месяцам
Если предположить рост активной базы:
- M3: 20 клиентов
- M6: 70 клиентов
- M9: 140 клиентов
- M12: 220 клиентов
- M18: 500 клиентов
- M24: 900+ клиентов

То **операционный break-even наступает не раньше M24-M25**, и то при хорошем execution. Для фонда это слишком длинный и рискованный путь при commodity-risk рынка.

---

## 12) Burn-to-breakeven и runway

### Burn-to-breakeven
Грубый cumulative burn по M1-M12 при ramp FOT + infra + acquisition:

| Период | Средний burn / мес, ₽ | Месяцев | Burn, ₽ |
|---|---:|---:|---:|
| M1-M3 | 2 300 000 | 3 | 6 900 000 |
| M4-M6 | 4 100 000 | 3 | 12 300 000 |
| M7-M9 | 5 000 000 | 3 | 15 000 000 |
| M10-M12 | 5 400 000 | 3 | 16 200 000 |
| **Итого M1-M12** | — | — | **50 400 000** |

Даже если часть team build растянуть и часть ролей закрыть founder effort, путь до масштабного break-even всё равно требует **десятки миллионов рублей**.

### Cash runway
- Допущение: **startup_capital = 25 000 000 ₽**
- Средний burn в первый год: **~4 200 000 ₽/мес**
- **Runway = 25 000 000 / 4 200 000 = 5.95 месяца**

Даже при более жёстком lean-mode и burn ~2.2-2.5 млн ₽/мес runway был бы лишь **10-11 месяцев**. Для такой длинной дороги до break-even это плохо.

### Sanity check
- Для B2B/SMB AI SaaS с video generation **startup_capital_to_bep < 10M ₽ нереалистично**.
- Здесь, наоборот, realistic capital need выглядит как **30-50M+ ₽**, если строить не микро-сервис, а repeatable venture case.

---

## 13) Итоговая инвестиционная оценка

### Что хорошо
- Есть подтверждённый спрос на video creative automation.
- Gross margin по сервисной части не ужасная.
- CAC payback не проваливается.
- Small business / agency tool здесь может существовать.

### Что плохо
1. **LTV/CAC = 2.79x**, ниже порога 3:1 для investable case.
2. **На 50 клиентах экономика глубоко отрицательная**, FAIL по Profit Gate.
3. Нужен тяжёлый team/FOT для продукта, где конкуренция уже commodity-like.
4. Выход на break-even требует слишком большой клиентской базы, порядка **~950 активных клиентов** при ARPU 7K.
5. Для fund-return profile кейс слабый: много execution risk, большой burn, неочевидный moat.

## Финальный вердикт
**REJECTED.**

Кейс можно было бы реанимировать только при одном из трёх условий:
1. поднять ARPU в 2-3 раза через agency/team workflow,
2. резко снизить product scope и идти как very lean cashflow business,
3. иметь distribution unfair advantage, который режет blended CAC ниже 25K fully-loaded.

В текущем виде для pipeline фонда кейс **не проходит**.
