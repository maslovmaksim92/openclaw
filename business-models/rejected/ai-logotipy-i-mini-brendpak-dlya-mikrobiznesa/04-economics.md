# Unit economics — AI-логотипы и мини-бренд-пак для микробизнеса и селлеров

## Итог
**Статус: FAIL / неинвестируемо в текущем wedge self-serve SMB branding.**

Кейс не проходит investment-grade проверку по двум причинам:
1. **Profit Gate FAIL**: при 50 активных клиентах EBITDA не может приблизиться к 500 тыс. ₽/мес. Даже при ARPU 990 ₽ выручка составляет только 49,5 тыс. ₽/мес.
2. **LTV/CAC = 1,17x**, что выше 1:1, но заметно ниже порога **3:1** для investable unit economics.

Следствие: кейс можно было бы спасать только через радикальный репозиционинг в agency white-label / recurring design ops, но **текущий кейс как массовый self-serve logo/brand-pack для микробизнеса под фондовую инвестицию не годится**.

## 1) Модель и ключевые допущения
### Что считаю
Беру не pure one-off PNG, а наиболее благоприятную для кейса recurring-модель:
- подписка: **990 ₽/мес** за бренд-ассеты, хранение, редактирование, шаблоны, экспорт;
- target segment: **SMB self-serve**;
- CAC multiplier по сегменту: **×1.3**, как требуется для SMB SaaS;
- churn benchmark: **8%/мес** как верхняя часть нормального коридора для small business / self-serve subscription, где retention обычно хуже mid-market SaaS. [S8][S9]

### Почему эти допущения консервативно-реалистичны
- WTP по рынку подтверждён конкурентами в диапазоне **~2,6–9,6 тыс. ₽** за logo/brand-kit пакет, но это не означает высокий retention. Основа боли у клиента разовая: запуск бренда, а не ежедневная операционная задача. [S1]
- Поэтому recurring-ARPU в **990 ₽/мес** выглядит скорее верхней границей для массового SMB-продукта, а churn 8%/мес выглядит реалистичнее, чем «красивые» 3–4%/мес. [S8][S9]

## 2) Подробный бизнес-процесс от лида до оплаты
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Приводим холодный трафик | Growth marketer | Яндекс.Директ, VK Ads, Telegram ads | 1-7 дней до первого визита | 180-260 за визит в платных каналах | Средняя |
| 2 | SEO/контент собирает органику | Content/Growth | Tilda/Webflow, SEO tools, TG-контент | 2-8 недель | 40-90 за органический лид в пересчёте | Средняя |
| 3 | Пользователь попадает на лендинг | Product + analytics | Tilda/Webflow, Я.Метрика | 2-4 мин | 6 | Высокая |
| 4 | Вводит название, нишу, стиль | Клиент | Web app form | 3-5 мин | 8 | Высокая |
| 5 | Генерация 20-40 вариантов | Inference backend | LLM + image generation + vector pipeline | 30-90 сек | 55 | Высокая |
| 6 | Пользователь выбирает и донастраивает | Клиент | Editor/canvas | 8-12 мин | 25 | Высокая |
| 7 | Paywall: экспорт PNG/SVG + mini brand-pack | Product | App paywall + CRM | 1-2 мин | 5 | Высокая |
| 8 | Оплата | Клиент | YooKassa / cloudpayments class эквайринг | 2-3 мин | 35 | Высокая |
| 9 | Доставка ассетов | Backend | Storage/CDN/email | <1 мин | 12 | Высокая |
| 10 | Поддержка по вопросам/повторной генерации | Support/CS | Telegram, email, helpdesk | 6-10 мин на 1 платящего в среднем по месяцу | 70 | Низкая-средняя |
| 11 | Ретеншн-касания и upsell | CRM marketer | amoCRM, email/push bot | 10-20 дней после покупки | 24 | Высокая |

### Вывод по процессу
- Почти весь путь автоматизируем, но у бизнеса остаются реальные денежные затраты на acquisition, inference, эквайринг и support.
- Главная проблема не в COGS, а в том, что **разовая природа боли ломает retention**.

## 3) COGS на клиента в месяц
Предполагаю **MRR на активного клиента = 990 ₽/мес**.

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Inference и генерация изображений | 110 | 2-3 генерации + 1-2 редактирования на клиента в мес, cross-check по cloud GPU economics | [S4] |
| Storage/CDN | 20 | хранение ассетов, превью, бренд-паков | [S4] + estimate |
| Платёжный эквайринг | 35 | ~3,5% от 990 ₽ | [S3] |
| Support / moderation | 70 | доля зарплаты support на 1 активного клиента | estimate |
| Шаблоны, шрифты, asset ops | 25 | лицензии и обслуживание библиотеки | estimate |
| CRM / retention messaging variable | 20 | рассылки и CRM-contact cost | [S2] + estimate |
| **Итого COGS** | **280** |  |  |

### Gross margin
- Выручка на клиента: **990 ₽/мес**
- COGS: **280 ₽/мес**
- **Gross profit: 710 ₽/мес**
- **Gross margin: 71,7%**

Для AI SMB-сервиса это неплохо. Значит проблема кейса не в валовой марже, а в acquisition + слабом LTV.

## 4) CAC по каналам и воронка
### Каналы acquisition
| Канал | Бюджет/мес, ₽ | Трафик/лиды | Signup | Paywall reach | New paying | Raw CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| SEO + контент | 120 000 | 18 000 визитов | 5,0% = 900 | 18% = 162 | 57 | 2 105 | Лучший канал, но медленно раскручивается |
| Telegram ads / посевы | 180 000 | 6 000 визитов | 12,0% = 720 | 14% = 101 | 20 | 9 000 | Дорогой трафик, слабая платежная конверсия |
| Партнёрства с агентствами/селлер-сервисами | 90 000 | 80 партнёрских лидов | 60% = 48 | 50% = 24 | 18 | 5 000 | Качественнее, но масштаб ограничен |
| Комьюнити селлеров / реферальный трафик | 50 000 | 1 500 визитов | 8,0% = 120 | 20% = 24 | 15 | 3 333 | Нестабильный объём |
| **Итого / blended raw** | **440 000** | 25 580 | 1 788 | 311 | **110** | **4 000** |  |

## 5) Fully-loaded CAC
### Формула
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocation + Tools + Events + Overhead multiplier) / New paying customers**

### Разложение fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/Telegram посевы) | 300 000 | 180 000 TG ads + 120 000 paid search/social | estimate |
| Outbound / partnerships FOT attributed to new | 117 000 | part-time partner manager equivalent 90 000 gross + 30% взносы | HH-style benchmark / estimate |
| Marketing team FOT (partial allocation) | 156 000 | growth marketer 120 000 gross × 1.3 | [S5][S6][estimate] |
| Tools (CRM, analytics, email) | 28 000 | amoCRM + email + analytics stack | [S2] |
| Events / partnerships | 40 000 | точечные интеграции, селлер-чаты, вебинары | estimate |
| Subtotal before overhead | 641 000 |  |  |
| Overhead multiplier (×1.3 for SMB SaaS) | 192 300 | 30% от subtotal | методика task |
| **Total fully-loaded acquisition cost / month** | **833 300** |  |  |
| **New paying customers / month** | **110** | blended funnel above |  |
| **Fully-loaded CAC** | **7 575 ₽** | 833 300 / 110 |  |

### Sanity-check против benchmark
- SMB self-serve benchmark в task: **5–30 тыс. ₽ CAC**.
- Наш fully-loaded CAC **7,6 тыс. ₽** находится внутри коридора и не выглядит искусственно заниженным.
- Если кто-то считал бы CAC только по рекламе, получил бы **4 000 ₽** и ошибочно решил бы, что модель очень хорошая. Реалистичная fully-loaded цифра почти **в 1,9 раза выше**.

## 6) LTV и churn
### Benchmark churn
- Для subscription-моделей важен именно churn, а не one-off margin.
- По отраслевым открытым бенчмаркам у SMB/self-serve subscription churn обычно существенно хуже, чем у mid-market B2B SaaS; в практическом коридоре **~5–8% monthly** считается нормой, а всё, что выше, быстро уничтожает LTV. [S8][S9]
- Для этого кейса беру **8% monthly churn**, потому что use case эпизодический: логотип и стартовый бренд-пак нужны в момент запуска, а не как ежедневный workflow.

### LTV calculation
Формула: **LTV = ARPU × Gross Margin / Monthly Churn**

- ARPU = **990 ₽/мес**
- Gross margin = **71,7%**
- Monthly churn = **8%**

**LTV = 990 × 0.717 / 0.08 = 8 874 ₽**

### Интерпретация
- Это очень низкий LTV для продукта, который всё равно вынужден покупать трафик.
- Даже небольшое ухудшение churn до 10% уронит LTV до **~7,1 тыс. ₽**, то есть почти к уровню CAC.

## 7) LTV/CAC ratio
- LTV = **8 874 ₽**
- Fully-loaded CAC = **7 575 ₽**
- **LTV/CAC = 1,17x**

### Вердикт по инвесткачеству
- Требование investment-grade: **≥ 3,0x**
- Reject threshold по task: **<1,0x**
- Фактический результат: **1,17x**, то есть чуть выше полного экономического коллапса, но далеко ниже уровня, в который стоит вкладывать фондовые деньги.

## 8) CAC payback
Формула по task: **CAC Payback = CAC / MRR per customer**

- CAC = **7 575 ₽**
- MRR/customer = **990 ₽**
- **CAC Payback = 7,65 месяца**

### Интерпретация
- Формально payback < 12 месяцев, что само по себе ещё допустимо.
- Но payback здесь обманчиво «нормальный», потому что churn высокий и клиент может не дожить до хорошего вклада в валовую прибыль.

## 9) Contribution Margin %
Использую contribution margin как доход после прямого COGS, но до fixed opex.

- Revenue/client/month = **990 ₽**
- COGS/client/month = **280 ₽**
- Contribution/client/month = **710 ₽**
- **Contribution Margin = 71,7%**

Высокая contribution margin не спасает кейс, потому что абсолютный рублёвый вклад на клиента слишком мал.

## 10) Team & FOT
### Таблица команды
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire, мес | Onboarding ramp до 80% | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO/founder | 1 | 600 000 | 0 | 0 | 180 000 | 780 000 |
| CTO / Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 1 | 400 000 | 1.5 | 1.5 | 120 000 | 520 000 |
| ML Engineer | 1 | 450 000 | 2.5 | 2 | 135 000 | 585 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| Growth Marketer | 1 | 120 000 | 1 | 1 | 36 000 | 156 000 |
| Customer Success / Support | 1 | 130 000 | 1 | 1 | 39 000 | 169 000 |
| **Итого полная команда** | **7** |  |  |  |  | **3 224 000** |

### Комментарий по реалистичности найма
- План не нарушает sanity-check: **нет 5+ наймов в первый месяц**.
- Даже очень lean-команда для такого продукта уже стоит **~3,2 млн ₽/мес** только по FOT fully-loaded.
- Для фонда это плохой сигнал: product complexity есть, а ARPU слишком маленький.

## 11) Cumulative FOT timeline M1-M12
Предполагаю поэтапный найм без фантазий про мгновенное комплектование команды.

| Месяц | Кто в штате | FOT/month, ₽ |
|---|---|---:|
| M1 | CEO | 780 000 |
| M2 | CEO + Frontend | 1 144 000 |
| M3 | CEO + Frontend + Growth | 1 300 000 |
| M4 | CEO + Frontend + Growth + Senior Backend | 1 820 000 |
| M5 | CEO + Frontend + Growth + Senior Backend + CTO | 2 470 000 |
| M6 | CEO + Frontend + Growth + Senior Backend + CTO + ML | 3 055 000 |
| M7 | + Customer Success | 3 224 000 |
| M8 | полная команда | 3 224 000 |
| M9 | полная команда | 3 224 000 |
| M10 | полная команда | 3 224 000 |
| M11 | полная команда | 3 224 000 |
| M12 | полная команда | 3 224 000 |

### Вывод
Даже при аккуратном найме burn быстро приходит к **3,2+ млн ₽/мес FOT**, а с acquisition и infra переваливает за **3,8–4,2 млн ₽/мес**.

## 12) Fixed costs breakdown
| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 3 224 000 | полная команда |
| Cloud / infra base | 180 000 | prod, dev, storage, observability |
| SaaS tools / CRM / support desk | 45 000 | amoCRM, аналитика, helpdesk |
| Бухгалтерия / юр / комплаенс | 35 000 | аутсорс + сервисы |
| Прочий G&A | 70 000 | домены, сервисы, связь, misc |
| **Итого fixed costs / month** | **3 554 000** | без paid acquisition |

Если добавить поддерживаемый acquisition budget 300-440 тыс. ₽/мес, operating burn становится **3,85–3,99 млн ₽/мес**.

## 13) Break-even по клиентам и по времени
### Break-even by client count
Формула: **Fixed costs / contribution per active client**

- Fixed costs = **3 554 000 ₽/мес**
- Contribution per active client = **710 ₽/мес**

**Break-even = 3 554 000 / 710 = 5 006 активных клиентов**

### Break-even sanity at 50 clients
- 50 клиентов × 990 ₽ = **49 500 ₽ MRR**
- Contribution = 50 × 710 = **35 500 ₽/мес**
- Это **в 100 раз ниже** нужного уровня fixed cost coverage.

### Break-even by month
Если брать 110 новых платящих в месяц и churn 8%, активная база к концу года растёт примерно так:
- M3: ~304 активных
- M6: ~581 активных
- M9: ~815 активных
- M12: ~1 011 активных

Даже к M12:
- Revenue = **~1,00 млн ₽/мес**
- Contribution = **~718 тыс. ₽/мес**
- Fixed costs = **3,55 млн ₽/мес**

**Break-even не достигается в пределах первых 12 месяцев.**

## 14) Burn-to-breakeven и runway
### Burn-to-breakeven
При operating burn **~3,9 млн ₽/мес** и отсутствии breakeven в M12 продукт сжжёт:
- **~18,5 млн ₽ за первые 6 месяцев**
- **~41–44 млн ₽ за 12 месяцев**

Это без учёта существенных ошибок по конверсии или необходимости наращивать paid acquisition.

### Cash runway
Берём startup_capital = **12 млн ₽**.

- Burn early stage M1-M3: **~1,3–2,1 млн ₽/мес**
- Burn после комплектования команды: **~3,8–4,0 млн ₽/мес**
- **Runway = примерно 4 месяца** до кассы 0 при realistic ramp

### Вывод
Для такой модели нужно либо:
1. кратно выше ARPU,
2. сильно лучше retention,
3. или другой сегмент, где 1 клиент стоит десятки тысяч рублей в месяц.

В текущем wedge ничего из этого не видно.

## 15) Инвестиционный вывод
### Что хорошо
- Валовая маржа нормальная.
- Автоматизация высокая.
- Time-to-value короткий.

### Что плохо
- Боль клиента в основном разовая.
- Fully-loaded CAC нельзя честно удержать низким без сильной органики.
- LTV/CAC = **1,17x**, то есть модель почти не оставляет запаса на ошибки.
- Для достижения breakeven нужно **~5 тыс. активных клиентов**, что несоразмерно команде и retention.
- **При 50 клиентах EBITDA 500 тыс. ₽/мес недостижима в принципе.**

## Финальный вердикт
**REJECTED для инвестиционного pipeline.**

Не потому что продукт никому не нужен, а потому что **self-serve logo/mini brand-pack для микробизнеса выглядит как хороший bootstrapped side-business, но слабый фондовый кейс**.

## Sources
- [S1] Внутренний кейс: `02-demand.md` по этому же кейсу, 2026-05-10.
- [S2] amoCRM, тарифы: https://www.amocrm.ru/tariffs/
- [S3] YooKassa, комиссия за платежи: https://yookassa.ru/developers/payments/basics/tariffs
- [S4] Cloud.ru, GPU/облако и инфраструктурные прайсы: https://cloud.ru/pricing
- [S5] hh.ru, рыночные вакансии backend/team lead/маркетинг: https://hh.ru/search/vacancy
- [S6] Habr Career salaries / market context: https://career.habr.com/salaries
- [S7] hh.ru, вакансии SDR/AE/Customer Success в Москве и СПб: https://hh.ru/search/vacancy
- [S8] RetentionCheck, SaaS churn benchmarks: https://www.retentioncheck.com/benchmarks/saas-churn-rate
- [S9] Baremetrics Open Benchmarks: https://baremetrics.com/open-benchmarks
