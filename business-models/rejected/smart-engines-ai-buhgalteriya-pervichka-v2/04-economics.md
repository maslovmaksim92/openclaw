---
stage: economics
case: smart-engines-ai-buhgalteriya-pervichka-v2
date: 2026-04-24
analyst: branch-models-lead
sector: FINTECH
verdict: REJECT
confidence: medium
---

# 04-economics

## Кейс
Smart Engines, AI-автоматизация бухгалтерской первички и учётного ввода.

## Короткий вывод
**Итог P5: REJECT на уровне фонда.**

Спрос и retention выглядят рабочими, но unit economics не проходят инвестиционный порог при реалистичном RU go-to-market и hiring plan. Главная проблема не в churn, а в слишком низком blended ARPA относительно необходимой product + enterprise sales команды.

Критический факт: **даже при 50 клиентах модель не выходит на EBITDA +500K ₽/мес**. При базовом сценарии получается около **-4.72M ₽/мес EBITDA**. Значит Profit Gate срабатывает и кейс должен быть отклонён.

## 1. Базовые допущения модели

### ICP и pricing
- ICP: бухгалтерские аутсорсеры, банки для МСБ, mid-market компании с большим потоком УПД/актов/счётов.
- Blended price: **55 000 ₽/клиент/мес**.
- Почему не выше:
  - 1С уже якорит рынок очень низкими OCR-only тарифами, вплоть до **40 000 ₽/год за 10 000 страниц** и **350 000 ₽/год за 100 000 страниц**.
  - Smart Engines продаёт enterprise-ready и on-prem value, но публичного high-ACV прайса нет, поэтому для фонда беру консервативный blended mid-market сценарий, а не оптимистичный bank-only сценарий.
  - Для бухгалтерских аутсорсеров платёжеспособность есть, но рынок остаётся price-sensitive и сравнивает новый продукт не только с payroll saving, но и с 1С / Saby / ручным вводом.

### Revenue assumption
- MRR на клиента: **55 000 ₽**
- ARR на клиента: **660 000 ₽**
- 50 клиентов = **2.75M ₽ MRR**

## 2. Детальный бизнес-процесс: от лида до оплаты

> Ниже процесс для одного выигранного клиента. Шаги 1-8 формируют sales CAC. Шаги 9-10 уже post-sale и не включаются в CAC, но нужны для cash conversion.

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка и enrichment | SDR | HH/реестры, CRM, таблицы | 3 ч | 18 000 | средняя |
| 2 | Холодный outreach, 6-8 касаний | SDR | CRM, почта, телефония | 10 ч | 55 000 | средняя |
| 3 | Qualification call | SDR + AE | VoIP, CRM | 2 ч | 22 000 | низкая |
| 4 | Discovery + demo | AE + PM | demo-стенд, CRM | 3 ч | 28 000 | низкая |
| 5 | Scoping пилота и ROI-калькуляция | AE + PM + CTO | Notion, калькулятор ROI | 4 ч | 35 000 | низкая |
| 6 | Пилот на реальных документах | Solutions/PM + Backend | sandbox/on-prem стенд | 20 ч | 110 000 | средняя |
| 7 | ИБ, legal, DPA, procurement review | CTO + CEO + юрист | docs, почта, ЭДО | 8 ч | 42 000 | низкая |
| 8 | Коммерческое согласование и закрытие | AE + CEO | CRM, договор, ЭДО | 5 ч | 30 000 | низкая |
| 9 | Onboarding и интеграция в 1С/ERP | Solutions + CS + Backend | API, 1С-коннектор | 12 ч | 68 000 | средняя |
| 10 | Выставление счёта и контроль оплаты | CS + finance | 1С, банк-клиент, ЭДО | 2 ч | 12 000 | высокая |

### Вывод по процессу
- **Sales CAC = 340 000 ₽** по шагам 1-8 в процессной декомпозиции.
- Но для фонда этого мало: нужен **fully-loaded CAC**, включая маркетинг-команду, инструменты, и overhead.
- Поэтому в инвестиционной модели использую более жёсткий **blended fully-loaded CAC = 420 000 ₽**.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| OCR/инференс и CPU-обработка | 3 000 | on-prem / edge-friendly inference, но есть вычислительная стоимость пилотов и продовых задач |
| Хранение, логирование, бэкапы | 1 000 | S3-совместимое хранилище, логи, аудит |
| Поддержка интеграций с 1С/ERP | 2 500 | распределение труда backend/support по активной базе |
| Human exception review | 6 500 | ручная обработка сложных документов и исключений |
| Customer support / success variable | 2 000 | 1 линия, ответы по инцидентам |
| Амортизация внедрения | 2 000 | часть onboarding-стоимости размазывается на 12 мес |
| ИБ/мониторинг на клиента | 0 | включено в fixed infra |
| **Итого COGS** | **17 000** |  |

### Gross / contribution
- Revenue per client/month = **55 000 ₽**
- COGS per client/month = **17 000 ₽**
- Contribution per client/month = **38 000 ₽**
- **Contribution Margin = 69.1%**

## 4. CAC by channel с funnel conversion

| Канал | Monthly spend, ₽ | Воронка | New paying customers / мес | CAC, ₽ |
|---|---:|---|---:|---:|
| Outbound SDR/AE | 408 000 | 600 target accounts → 72 replies (12%) → 24 meetings (33%) → 8 pilots (33%) → 1.4 wins (17%) | 1.4 | 291 000 |
| Partners / 1С / банки | 182 000 | 18 partner intros → 10 qualified (56%) → 4 pilots (40%) → 1.0 win (25%) | 1.0 | 182 000 |
| Content + paid inbound | 187 000 | 110 leads → 20 SQL (18%) → 6 demos (30%) → 0.6 win (10%) | 0.6 | 312 000 |
| **Blended raw** | **777 000** | суммарно | **3.0** | **259 000** |

### Fully-loaded CAC

Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocated + Tools/CRM + Events/partnerships + Overhead) / New paying customers
```

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый inbound budget для B2B category capture | допущение аналитика, sanity against RU SaaS GTM |
| Outbound team FOT (SDR/AE attributed to new) | 598 000 | SDR 180K gross + 30% = 234K; AE 400K gross + 30% = 520K; к new logo относим 70% AE = 364K; итого 598K | HH benchmark + модель загрузки |
| Marketing team FOT (partial allocation) | 117 000 | маркетинг 180K gross + 30% = 234K; 50% аллокация на acquisition | HH benchmark |
| Tools (CRM, enrichment, телефония, рассылки) | 65 000 | CRM + телефония + enrichment + demo stack | допущение аналитика |
| Events/partnerships | 180 000 | партнёрские мероприятия, совместные вебинары, roadshow | допущение аналитика |
| Overhead multiplier (x1.3) | 324 000 | 30% от raw acquisition stack 1 080 000 ₽ | стандартный overhead для B2B GTM |
| **Итого fully-loaded acquisition stack** | **1 404 000** |  |  |

- New paying customers / мес: **3.34** в оптимистичном плане, но для консервативной модели округляю до **3.3**.
- **Fully-loaded CAC = 1 404 000 / 3.34 = ~420 000 ₽**.

### Sanity check по CAC
- Бенчмарк из standing order для complex B2B / enterprise SaaS в РФ: **300K-900K ₽ CAC**.
- Наш **420K ₽** не выглядит заниженным.
- Значит проблема модели не в слишком оптимистичном CAC, а в недостаточном ARPA относительно burn.

## 5. LTV и churn

### Бенчмарк churn
- ChartMogul указывает, что для SaaS с ARPA **$500+** customer churn обычно составляет **1-2% в месяц**.
- Для Smart Engines беру консервативно **1.5% monthly logo churn**, потому что это workflow-heavy B2B продукт с интеграциями и относительно низкой частотой замены, но не mission-critical core ERP.

### LTV
Формула:

```text
LTV = Contribution per customer per month / monthly churn
```

- Contribution per client/month = **38 000 ₽**
- Monthly churn = **1.5%**
- **LTV = 38 000 / 0.015 = 2 533 333 ₽**

### LTV/CAC
- LTV = **2.53M ₽**
- Fully-loaded CAC = **420K ₽**
- **LTV/CAC = 6.0x**

Интерпретация:
- Формально retention хороший, модель не умирает от churn.
- Но **LTV/CAC > 3 сам по себе не спасает**, если компания не может дойти до EBITDA +500K при реалистичной базе в 50 клиентов.

## 6. CAC Payback

Формула по standing order:

```text
CAC Payback = CAC / MRR per customer
```

- CAC = **420 000 ₽**
- MRR per customer = **55 000 ₽**
- **CAC Payback = 7.6 мес**

Вывод:
- По payback модель выглядит терпимо.
- Но это не отменяет провал по burn и break-even.

## 7. Team & FOT

### Полная команда на go-to-market stage

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1.5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product Manager | 1 | 350 000 | 1-2 | 1.5 | 105 000 | 455 000 |
| SDR (outbound) | 1 | 180 000 | 0.5-1 | 1 | 54 000 | 234 000 |
| AE (Account Exec) | 1 | 400 000 | 1-2 | 2-3 | 120 000 | 520 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Solutions / Implementation Engineer | 1 | 300 000 | 1-2 | 1.5 | 90 000 | 390 000 |
| **Итого FOT fully-loaded** | **11** |  |  |  |  | **6 058 000 ₽/мес** |

### Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO, CTO | 1 560 000 |
| M2 | + Senior Backend #1, SDR | 2 340 000 |
| M3 | + DevOps | 2 795 000 |
| M4 | + Senior Backend #2, PM | 3 796 000 |
| M5 | + AE | 4 316 000 |
| M6 | + ML Engineer | 4 966 000 |
| M7 | + Frontend | 5 356 000 |
| M8 | + Customer Success | 5 668 000 |
| M9 | + Solutions / Implementation Engineer | 6 058 000 |
| M10 | full team | 6 058 000 |
| M11 | full team | 6 058 000 |
| M12 | full team | 6 058 000 |

### Комментарий по hiring realism
- План не нарушает sanity-check: нет найма 5+ человек в первый месяц.
- Но даже умеренный по темпу hiring plan быстро выводит FOT выше **6M ₽/мес**.
- Для продукта, который продаётся в blended сценарии по **55K ₽ MRR**, это слишком тяжёлая cost base.

## 8. Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 6 058 000 |
| Облако / сервера / тестовые контуры / мониторинг | 260 000 |
| Юристы, бухгалтерия, G&A | 180 000 |
| Офис / командировки / административные | 120 000 |
| **Итого fixed costs** | **6 618 000 ₽/мес** |

> Acquisition spend считаю отдельно в CAC-слое. Если смотреть EBITDA полностью, sales & marketing расходы всё равно давят сильнее, чем продуктовая маржа может компенсировать на базе 50 клиентов.

## 9. Break-even

### Break-even по числу клиентов
Формула:

```text
Break-even clients = Fixed costs / Contribution per client per month
```

- Fixed costs = **6 618 000 ₽/мес**
- Contribution per client/month = **38 000 ₽**
- **Break-even = 174 клиента**

### Клиенты для EBITDA +500K/мес

```text
Clients for EBITDA 500K = (Fixed costs + 500 000) / Contribution per client per month
```

- **(6 618 000 + 500 000) / 38 000 = 188 клиентов**

### Что происходит на 50 клиентах
- Revenue = **2 750 000 ₽/мес**
- COGS = **850 000 ₽/мес**
- Gross profit = **1 900 000 ₽/мес**
- Fixed costs = **6 618 000 ₽/мес**
- **EBITDA = -4 718 000 ₽/мес**

**Это прямое срабатывание Profit Gate FAIL.**

## 10. Break-even по времени

Если компания набирает в среднем по **3.3 новых клиента в месяц**, то:

- break-even по клиентам = **174 клиента**
- время до break-even = **174 / 3.3 ≈ 53 месяца**
- время до EBITDA +500K = **188 / 3.3 ≈ 57 месяцев**

Для pre-seed / seed / Series A фонда это слишком длинный и капиталоёмкий путь.

## 11. Burn-to-breakeven и runway

### Burn-to-breakeven
- Burn на полном составе без учёта COGS = **6.62M ₽/мес**.
- Если добавить acquisition stack для поддержания 3.3 new logos / мес, operating burn до самоокупаемости приближается к **8.0M ₽/мес**.
- Даже если часть GTM расходов уходит в variable CAC, суммарный cash burn до выхода на 174 клиента остаётся слишком высоким.

### Cash runway
При **startup_capital = 36M ₽**:

- runway на burn **~6.62M ₽/мес** = **5.4 месяца**;
- runway на более раннем burn **~4.0M-5.0M ₽/мес** = **7-9 месяцев**;
- для комфортного прохода до product-market fit и первых десятков клиентов нужен капитал заметно выше, порядка **60M-90M ₽**.

### Sanity check
- Для B2B enterprise-ish workflow startup capital до BEP **меньше 10M ₽** был бы нереалистичным. Здесь наоборот видно, что капитала нужно много, и именно это убивает инвестиционную привлекательность.

## 12. Инвестиционный вывод

### Что хорошо
- LTV/CAC = **6.0x**
- CAC payback = **7.6 мес**
- churn у workflow-heavy B2B продукта выглядит умеренным
- есть реальный спрос и понятный ROI на снижении ручного труда

### Что плохо и что критично
1. **Blended ARPA слишком низкий** для команды, которая нужна для enterprise-grade OCR + integrations + support.
2. **Break-even только на ~174 клиентах**, а EBITDA +500K лишь около **188 клиентов**.
3. На **50 клиентах** компания всё ещё глубоко убыточна.
4. Модель требует длинного финансирования и не выглядит fund-grade на текущем ценовом якоре рынка.

## 13. Profit Gate

### Проверка условий
- EBITDA +500K/мес achievable at 50 clients? **Нет.**
- LTV/CAC < 1:1? **Нет, LTV/CAC = 6.0x.**

### Итоговое правило
По standing order достаточно одного провала:
- компания **не может выйти на EBITDA +500K/мес даже при 50 клиентах**.

**Решение: REJECT и перенос в `pipeline/rejected/`.**

## Источники
- Smart Engines: AI-агент для бухгалтерской первички, 900 стр/мин, корпоративные заказчики и банки, https://smartengines.ru/news/buhgalterskiy-ai-agent/
- 1С: публичный прайс распознавания первичных документов, https://v8.1c.ru/its/services/1s-raspoznavanie-pervichnykh-dokumentov/cena-1s-raspoznavanie-pervichnykh-dokumentov/
- Saby автораспознавание первички, https://saby.ru/autorecognition
- Entera pricing, https://entera.pro/cost
- ChartMogul: SaaS churn benchmark, ARPA $500+ обычно 1-2% monthly churn, https://help.chartmogul.com/article/203-chart-customer-churn-rate
- HH salary market snapshots: senior backend / ML / SDR / AE pages and vacancy search on hh.ru, например https://hh.ru/vacancies/senior-backend-developer/polniy_den , https://hh.ru/vacancies/machine-learning-engineer , https://hh.ru/vacancy/128565026 , https://hh.ru/vacancies/account_executive/polniy_den
