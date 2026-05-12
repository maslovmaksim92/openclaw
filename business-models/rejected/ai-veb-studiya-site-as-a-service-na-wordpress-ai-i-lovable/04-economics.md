# Unit Economics — AI-веб-студия Site-as-a-Service на WordPress AI и Lovable

Дата: 2026-05-12 23:20 MSK  
Стадия: Program 5 — Unit Economics  
Статус: REJECT

## 1) Executive summary

Кейс не проходит fund-level фильтр как investable SMB service business.

Почему:
- оффер выглядит как **managed service**, а не software-like SaaS, поэтому gross margin и scalability ниже, чем предполагалось на demand-этапе;
- **fully-loaded CAC** для SMB/Mid-market acquisition получается высоким из-за SDR/AE, CRM/tool stack, партнёрских затрат и длинной цепочки касаний;
- при реалистичном churn для SMB recurring-services **LTV/CAC = 2.31x**, это ниже инвестиционного порога `>=3.0x`;
- при штатной команде и реалистичном fixed cost base компания **не выходит на EBITDA 500k+/мес даже на 50 клиентах**.

Итог: **Profit Gate = FAIL**. Кейс переводится в `pipeline/rejected/`.

## 2) Модель и ключевые допущения

### ICP и пакет
- ICP: SMB и lower mid-market бизнесы, которым нужен сайт как канал лидогенерации.
- Продукт: запуск + ежемесячные обновления, контент, SEO/CRO-итерации, support.
- Базовый тариф для расчёта: **59 900 ₽/клиент/мес**.
- Разовые setup fees в расчёт LTV/CAC не включаю, чтобы не завышать экономику recurring-модели.

### Главные допущения
- MRR на клиента: **59 900 ₽/мес**.
- Logo churn benchmark для SMB ACV `<$10k`: **4.2% в месяц**. Это близко к нашему ACV `~719k ₽/год`, то есть ниже enterprise-порога и без сильных switching costs. [T3]
- Contribution margin на клиента после прямого delivery: **62.8%**.
- Segment CAC multiplier: **×1.6**, как для mid-market B2B с несколькими касаниями и sales-assisted closing.

## 3) Подробный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор целевого списка компаний | SDR | HH/2ГИС/Яндекс/ручной ресерч | 20 мин/лид | 233 | низкая |
| 2 | Обогащение контактов и сегментация | SDR | Google Sheets, Telegram, email lookup | 10 мин/лид | 116 | средняя |
| 3 | Персонализированный outbound | SDR | Instantly/Unisender/Telegram | 8 мин/лид | 102 | средняя |
| 4 | Первичный inbound capture | Marketing/Growth | Лендинг на WordPress, формы, CRM | 5 мин/лид | 61 | высокая |
| 5 | Qualification call | SDR | Telegram/Zoom/CRM | 30 мин/SQL | 350 | низкая |
| 6 | Discovery и pain mapping | AE/Founder | Zoom/Notion/CRM | 60 мин/opportunity | 1 120 | низкая |
| 7 | Mini-audit текущего сайта | Tech lead + Designer | WordPress audit, PageSpeed, AI tools | 90 мин/opportunity | 2 175 | средняя |
| 8 | Коммерческое предложение | AE | Notion/Google Docs/PandaDoc | 45 мин/proposal | 840 | средняя |
| 9 | Follow-up и дожим | AE | CRM, Telegram, email | 30 мин/proposal | 560 | средняя |
| 10 | Согласование договора/счёта | Founder/ops | Диадок/1С/банк | 40 мин/deal | 1 050 | низкая |
| 11 | Получение предоплаты | Finance/Founder | Банк, эквайринг | 15 мин/deal | 410 | высокая |
| 12 | Онбординг клиента | CSM/PM | Notion, TG, Forms | 90 мин/new client | 1 140 | средняя |

### Вывод по процессу
- Воронка не self-serve, а **sales-assisted service sale**.
- До первой оплаты требуется несколько ручных касаний SDR/AE/founder и мини-аудит delivery-команды.
- Это и поднимает fully-loaded CAC выше простого “реклама / оплаты”.

## 4) COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| WordPress hosting + backup + CDN + плагины | 3 200 | инфраструктурный пакет на клиента |
| AI stack share (Lovable/LLM/copy/design) | 2 800 | аллокация лицензий и usage |
| Delivery: WordPress/no-code builder | 8 500 | ~2.0 ч/мес эквивалента |
| Delivery: design/CRO edits | 3 900 | ~1.0 ч/мес |
| Delivery: content/SEO updates | 2 900 | ~1.0 ч/мес |
| CSM / project communication | 2 600 | ~0.8 ч/мес |
| QA / release / bugfix reserve | 1 500 | буфер на внеплановые правки |
| Платёжные комиссии и мелкие сервисы | 900 | эквайринг + misc |
| **Итого COGS** | **22 300** |  |
| **Выручка на клиента** | **59 900** |  |
| **Contribution / gross profit на клиента** | **37 600** |  |
| **Contribution Margin** | **62.8%** | `37 600 / 59 900` |

## 5) CAC по каналам и воронка конверсии

### Воронка по каналам
| Канал | Верх воронки за мес | Discovery | Proposal | New paying customers | Конверсия lead→paying | Raw CAC, ₽ | Fully-loaded CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound email/Telegram | 600 лидов | 18 | 6 | 1.5 | 0.25% | 256 800 | 410 880 |
| Paid search / performance | 180 лидов | 12 | 4 | 0.6 | 0.33% | 300 000 | 480 000 |
| Партнёрства / referrals | 12 интро | 8 | 4 | 0.4 | 3.33% | 105 000 | 168 000 |
| **Blended** | **792** | **38** | **14** | **2.5** | **0.32%** | **242 880** | **388 608** |

### Fully-loaded CAC, обязательный расчёт

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый monthly budget для search + retargeting | T1/T2 + модель |
| Outbound team FOT (SDR attributed to new) | 182 000 | `140 000 gross × 1.3` | T4 |
| Sales team FOT (AE attributed to new) | 210 000 | `300 000 gross × 70% × 1.0` округлено + часть commission | T4 |
| Marketing team FOT (partial allocation) | 36 000 | `120 000 gross × 30%` | модель |
| Tools (CRM, outreach, domain/email, call stack) | 34 200 | amoCRM + рассылка + телефония + docs | модель |
| Events / partnerships | 25 000 | мини-ивенты, партнёрские бонусы, комьюнити | модель |
| **Raw acquisition spend / мес** | **607 200** | сумма выше |  |
| New paying customers / мес | **2.5** | blended funnel | модель |
| **Raw blended CAC** | **242 880** | `607 200 / 2.5` |  |
| Overhead multiplier | **×1.6** | mid-market B2B multiplier | user rule |
| **Fully-loaded blended CAC** | **388 608** | `242 880 × 1.6` |  |

### Sanity check против benchmark
- Наш blended CAC **~389k ₽**.
- Это выше mid-market SaaS benchmark `60–250k ₽`, но ниже enterprise `300–900k ₽`.
- Для сервиса с founder/AE-assisted продажей это **не выглядит заниженным**, наоборот близко к reality check.

## 6) LTV и churn

### Churn benchmark
- Для SMB ACV `<$10k` Optifai даёт **4.2% monthly churn**. [T3]
- Наш annual contract value: `59 900 × 12 = 718 800 ₽`, что примерно попадает в SMB ACV bucket, а не в enterprise. Поэтому беру **4.2%/мес** как benchmark, а не optimistic enterprise-like churn. [T3]

### LTV
- ARPA / MRR per customer = **59 900 ₽/мес**.
- Contribution margin = **62.8%**.
- Monthly churn = **4.2%**.
- **LTV (gross profit basis)** = `59 900 × 62.8% / 4.2% = 896 124 ₽`.
- Expected lifetime = `1 / 0.042 = 23.8 мес`.

## 7) LTV/CAC, CAC Payback, Contribution Margin

| Метрика | Значение | Формула |
|---|---:|---|
| LTV | 896 124 ₽ | `MRR × CM / churn` |
| Fully-loaded CAC | 388 608 ₽ | см. расчёт выше |
| **LTV/CAC** | **2.31x** | `896 124 / 388 608` |
| **CAC Payback** | **6.5 мес** | `388 608 / 59 900` |
| Contribution Margin | 62.8% | `37 600 / 59 900` |
| Gross-profit CAC Payback | 10.3 мес | `388 608 / 37 600` |

### Интерпретация
- По user rule **LTV/CAC должен быть >= 3.0x**. Здесь только **2.31x**.
- CAC payback по MRR выглядит терпимым, но **payback по gross profit уже 10.3 мес**, что тяжело для service-heavy SMB бизнеса.
- При churn 4.2% даже умеренно высокий CAC быстро ломает инвестиционный профиль.

## 8) Team & FOT

### Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / Founder-Seller | 1 | 650 000 | 0 | 0 | +30% | 845 000 |
| CTO / Tech Lead | 1 | 500 000 | 2 | 2 | +30% | 650 000 |
| Senior Backend / Automation | 1 | 350 000 | 1.5 | 1.5 | +30% | 455 000 |
| DevOps / Platform | 0.5 | 320 000 | 1.5 | 1 | +30% | 208 000 |
| Frontend / WordPress builder | 1 | 260 000 | 1 | 1 | +30% | 338 000 |
| SDR | 1 | 140 000 | 1 | 1 | +30% | 182 000 |
| AE | 1 | 300 000 | 1.5 | 2.5 | +30% | 390 000 |
| Customer Success / PM | 1 | 220 000 | 1 | 1 | +30% | 286 000 |
| **Итого steady-state FOT** | **7.0 FTE** |  |  |  |  | **3 354 000 ₽/мес** |

### Комментарий
- Для fund-level оценки учитываю **рыночную стоимость founder и core team**, а не “founder working for free”.
- Даже при AI-автоматизации сайтовый сервис остаётся людьмиёмким: discovery, edits, approvals, support, mini-audits, контентные итерации.

## 9) Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Frontend/WordPress | 1 183 000 |
| M3 | CEO + Frontend + SDR | 1 365 000 |
| M4 | CEO + Frontend + SDR + CSM | 1 651 000 |
| M5 | CEO + Frontend + SDR + CSM + AE | 2 041 000 |
| M6 | CEO + Frontend + SDR + CSM + AE + CTO | 2 691 000 |
| M7 | CEO + Frontend + SDR + CSM + AE + CTO + 0.5 DevOps | 2 899 000 |
| M8 | CEO + Frontend + SDR + CSM + AE + CTO + 0.5 DevOps + Backend | 3 354 000 |
| M9 | steady-state | 3 354 000 |
| M10 | steady-state | 3 354 000 |
| M11 | steady-state | 3 354 000 |
| M12 | steady-state | 3 354 000 |

### Sanity checks
- План не нанимает `5+` человек в M1, значит time-to-hire realism соблюдён.
- FOT после выхода на рабочий состав значительно выше `1 млн ₽/мес`, что подтверждает: прежние гипотезы были недоучтены.

## 10) Полная команда: роли, функции, зарплаты

| Роль | Функция | Gross salary, ₽ | Fully-loaded FOT, ₽ |
|---|---|---:|---:|
| CEO / Founder-Seller | продажи, ключевые переговоры, P&L | 650 000 | 845 000 |
| CTO / Tech Lead | шаблонизация delivery, автоматизация, quality bar | 500 000 | 650 000 |
| Senior Backend / Automation | интеграции, кастомные блоки, AI/ops | 350 000 | 455 000 |
| DevOps 0.5 FTE | хостинг, CI/CD, uptime, backup | 160 000 | 208 000 |
| Frontend / WordPress builder | сборка и релизы сайтов | 260 000 | 338 000 |
| SDR | генерация новых встреч | 140 000 | 182 000 |
| AE | discovery, proposal, close | 300 000 | 390 000 |
| Customer Success / PM | онбординг, коммуникация, renewals | 220 000 | 286 000 |

## 11) Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| CEO / Founder-Seller | 845 000 |
| CTO / Tech Lead | 650 000 |
| Senior Backend / Automation | 455 000 |
| DevOps 0.5 FTE | 208 000 |
| Frontend / WordPress builder | 338 000 |
| SDR | 182 000 |
| AE | 390 000 |
| Customer Success / PM | 286 000 |
| Офис / coworking / admin / бухгалтерия | 120 000 |
| Core software stack, not client-allocable | 95 000 |
| Юридические / misc reserve | 70 000 |
| **Итого fixed costs / мес** | **3 639 000 ₽** |

> Примечание: часть delivery-часов уже сидит в COGS. Здесь fixed base отражает минимальную штатную платформу, без которой сервис не держит качество и скорость. Это сознательно консервативная fund-level модель.

## 12) Break-even: по клиентам и по месяцам

### Break-even по клиентам
- Contribution на клиента = **37 600 ₽/мес**.
- Fixed costs = **3 639 000 ₽/мес**.
- **Break-even clients** = `3 639 000 / 37 600 = 96.8`, округлённо **97 клиентов**.

### Проверка на 50 клиентах
- Revenue = `50 × 59 900 = 2 995 000 ₽/мес`.
- Contribution = `50 × 37 600 = 1 880 000 ₽/мес`.
- EBITDA = `1 880 000 - 3 639 000 = -1 759 000 ₽/мес`.
- **Даже на 50 клиентах EBITDA не просто < 500k, а отрицательная. Profit Gate FAIL.**

### Break-even по месяцам (модель ramp)
| Месяц | Клиенты на конец месяца | Contribution, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 060 000 | -1 060 000 |
| M2 | 2 | 75 200 | 1 360 000 | -1 284 800 |
| M3 | 5 | 188 000 | 1 560 000 | -1 372 000 |
| M4 | 8 | 300 800 | 1 900 000 | -1 599 200 |
| M5 | 12 | 451 200 | 2 280 000 | -1 828 800 |
| M6 | 16 | 601 600 | 2 980 000 | -2 378 400 |
| M7 | 20 | 752 000 | 3 170 000 | -2 418 000 |
| M8 | 26 | 977 600 | 3 639 000 | -2 661 400 |
| M9 | 32 | 1 203 200 | 3 639 000 | -2 435 800 |
| M10 | 38 | 1 428 800 | 3 639 000 | -2 210 200 |
| M11 | 45 | 1 692 000 | 3 639 000 | -1 947 000 |
| M12 | 52 | 1 955 200 | 3 639 000 | -1 683 800 |

Вывод: в горизонте 12 месяцев break-even **не достигается**.

## 13) Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Суммарный отрицательный EBITDA по M1-M12: **~22.88 млн ₽**.
- Это только operating burn до выхода к масштабу, без дополнительных one-off затрат на запуск, юрструктуру и неудачные наймы.
- Для сервиса такого типа **startup capital <10 млн ₽** был бы явным red flag; даже **18 млн ₽** здесь недостаточно, чтобы спокойно дожить до break-even.

### Cash runway
- Если стартовый капитал = **18 млн ₽**, а средний burn в M1-M12 = **~1.91 млн ₽/мес**, runway = `18 / 1.91 = 9.4 мес`.
- Значит деньги заканчиваются **до достижения даже 52 клиентов**, не говоря уже о 97 клиентах, нужных для break-even.

## 14) Final investment verdict

### Что хорошего
- Спрос на underlying услугу есть.
- Клиенты готовы платить за запуск и поддержку сайтов.
- AI действительно снижает tooling cost и часть production time.

### Что ломает кейс
1. **Это service business, а не SaaS.** AI уменьшает труд, но не убирает ручные шаги в продажах, онбординге и ongoing delivery.
2. **Fully-loaded CAC высокий.** Founder/AE-assisted продажа в SMB плохо масштабируется.
3. **Retention слабее, чем нужно инвестфонду.** При churn `4.2%/мес` lifetime недостаточен, чтобы окупить такой CAC с запасом.
4. **Break-even слишком поздний.** На реалистичном штате компания не проходит порог ни по EBITDA, ни по capital efficiency.

## Verdict

**REJECTED.**

Формальное основание:
- **LTV/CAC = 2.31x < 3.0x**;
- **EBITDA 500k+/мес недостижима даже на 50 клиентах**;
- следовательно кейс не проходит investment-grade filter Program 5.

## Sources
- [T1] WordPress pricing: https://wordpress.com/ru/pricing/
- [T2] Lovable pricing / context: https://lovable.dev/pricing ; https://techcrunch.com/2025/07/02/lovable-on-track-to-raise-150m-at-2b-valuation/
- [T3] Optifai, B2B SaaS churn by ACV, 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [T4] HH.ru salary benchmarks / live vacancies and search pages:
  - SDR: https://hh.ru/vacancy/128565026
  - AE / Account Executive listings: https://hh.ru/vacancies/account_executive
  - Frontend: https://hh.ru/vacancies/senior-frontend-developer
  - DevOps: https://hh.ru/vacancies/devops-engineer
  - WordPress developer: https://hh.ru/vacancies/wordpress-developer
- [T5] Public RU price anchors used ранее в demand-stage:
  - Подписайт: https://podpisite.ru/
  - СайтЭксперт: https://saitexpert.ru/
  - IZE support: https://ize.ru/support/
  - Taptop pricing: https://taptop.pro/pricing
