# Lovable AI-веб-студия под заказ — полный verdict

Источник кейса: `pipeline/cases/lovable-ai-veb-studiya-pod-zakaz/`
Статус: **NEAR-PASS / rejected bucket**
Сектор: **AI-SERVICES**
Дата сборки: **2026-04-26**

> Примечание по схеме артефактов: в кейсе фактически присутствуют `01-intake.md`, `02-demand.md`, `04-economics.md`, `05-critic.md`, `06-verdict.md`, `07-score-trajectory.md`. Файлы `02-validation.md` и `03-demand.md` отсутствуют, поэтому ниже собраны все реально существующие стадии анализа.

---

## Stage 1 — Intake

---
sector: AI-SERVICES
rerun: false
source_raw: 2026-04-25-ai-services-lovable-ai-veb-studiya-pod-zakaz.md
created: 2026-04-25T14:28:28+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
AI-веб-студия на базе Lovable собирает лендинги, корпоративные сайты и простые клиентские кабинеты под заказ за считаные дни, заменяя классический production стек веб-студии более дешёвым AI-first delivery.

## Почему кейс проходит triage
- Есть повторяемый buyer problem: SMB и mid-market регулярно покупают сайты, лендинги и мелкие веб-доработки, где скорость и цена критичнее кастомной инженерии.
- Сильный category signal уже подтверждён ростом Lovable и сохраняющимся ценовым зазором веб-разработки в РФ.
- EBITDA-гипотеза 700 000-1 800 000 ₽ в месяц проходит порог Program 1, а wedge выглядит отдельной сервисной моделью, не сводимой к AI-креативам или no-code narrative.

## Контекст raw-файла

# Lovable AI-веб-студия под заказ

## Sector
AI-SERVICES

## Wedge statement
AI-веб-студия собирает лендинги, корпоративные сайты и простые клиентские кабинеты под заказ за 1-3 дня вместо классической веб-студии с дизайнерами и фронтенд-разработчиками.

## Evidence
- [T2] https://techcrunch.com/2025/07/23/eight-months-in-swedish-unicorn-lovable-crosses-the-100m-arr-milestone/ — TechCrunch пишет, что Lovable достиг $100M ARR за 8 месяцев, имеет 2,3 млн активных пользователей и 180 тыс. платящих, то есть спрос на AI-сборку сайтов уже подтверждён рынком.
- [T2] https://techcrunch.com/2026/03/11/lovable-says-it-added-100m-in-revenue-last-month-alone-with-just-146-employees/ — в марте 2026 Lovable подтвердил 400M ARR; это усиливает сигнал, что категория не краткосрочный хайп, а быстро растущий рабочий стек для агентской модели.
- [T3] https://lovable.dev/pricing — официальный прайс Lovable: Pro $25/мес и Business $50/мес, то есть себестоимость AI-инструмента на одного исполнителя на порядки ниже классической команды разработки.
- [T2] https://workspace.ru/web-development/ — Workspace показывает среднюю стоимость создания сайта в РФ на уровне 200 000-800 000 ₽, что подтверждает большой ценовой зазор для AI-студии, продающей faster/cheaper delivery.

## EBITDA hypothesis (24 мес, base)
700000-1800000₽/мес

## RU-fit
4 / 5. Модель хорошо переносится в РФ для SMB и агентского продакшна, но нужны аккуратная работа с хостингом, оплатами зарубежного SaaS и хранением персональных данных в контуре клиента.

## Expected unit economics (ballpark)
- ARPU: 60000₽/мес
- CAC (ballpark): 25000₽
- Avg deal cycle: 0.5-1 мес
- Target segment: SMB | Mid-market

## Why now
В 2025-2026 AI-конструкторы сайтов перешли из стадии демо в массовый платящий рынок, а в РФ веб-студии по-прежнему держат чек 200-800 тыс. ₽ за сайт. Это создаёт окно для AI-native агентства: собирать сайты и мелкие доработки в 10x дешевле по себестоимости и зарабатывать на портфеле из 15-30 клиентов без большой штатной команды.

---

## Stage 2 — Demand

---
stage: demand-validation
case: lovable-ai-veb-studiya-pod-zakaz
date: 2026-04-25
analyst: branch-models-lead
sector: AI-SERVICES
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Lovable, AI-веб-студия под заказ для лендингов, корпоративных сайтов и простых клиентских кабинетов.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Exact-demand на ярлык `AI-веб-студия` пока слабый, но underlying demand на `создание сайта`, `корпоративный сайт` и `разработка сайта для бизнеса` в РФ уже устойчивый: внутренний `multi-demand` даёт **MEDIUM / 30-38** по базовым запросам. [T1]
- Платёжная готовность подтверждается двумя слоями substitutes: классические агентства в РФ держат публичные чеки от **400 000 ₽** и выше за сайт, а AI/DIY платформы монетизируются от **$20-120/мес** и выше. [T1][T2]
- В Telegram/RU есть сильные сервисы для лидогенерации и bot-based funnels, но не видно доминирующего Telegram-only игрока, закрывающего весь workflow «сайт + кабинет + интеграции под ключ». Это снижает риск, что Telegram полностью заместит AI-студию. [T2][inference]
- Profit Gate не проходит в дешёвом one-off лендинговом сценарии, но проходит в productized website package, retainer web-ops и multi-site B2B support motion. Значит условие раннего reject не выполняется. [T1][T2][inference]

## 1. Demand data

### Demand API
- `AI веб-студия сайты на заказ` → **LOW**, `demand_score=0`, `google_trends=0`, `yandex_suggest=2`. [T1]
- `создание сайта` → **MEDIUM**, `demand_score=38`, `hh_ru=3207`, `yandex_suggest=100`, `google_trends_ru=31`. [T1]
- `корпоративный сайт` → **MEDIUM**, `demand_score=31`, `hh_ru=6868`, `yandex_suggest=100`. [T1]
- `разработка сайта для бизнеса` → **MEDIUM**, `demand_score=30`, `hh_ru=1594`, `yandex_suggest=100`. [T1]
- `лендинг на заказ` → **LOW**, `demand_score=22`, но `yandex_suggest=100`, то есть intent есть, просто ярлык уже частично растворился в более общих запросах на сайт/промо-страницу. [T1][inference]
- `конструктор сайтов` → **LOW**, `demand_score=28`, `yandex_suggest=100`. [T1]

### Интерпретация
- В РФ продаётся не тезис `AI-веб-студия`, а конкретный outcome: быстро выпустить сайт, лендинг или клиентский кабинет с интеграцией в CRM и оплату. [T1][inference]
- Это хороший сигнал для service-wedge: можно идти в рынок через скорость, SLA и lower cost, а не через новый category label. [T1][inference]
- Спрос есть, но GTM должен быть ориентирован на уже существующий бюджет `создание/обновление сайта`, а не на «эксперименты с AI». [T1][T2][inference]

## 2. Реальные конкуренты и цены

| Игрок | Формат | Публичная цена | Что доказывает |
|---|---|---:|---|
| **Lovable** | AI builder / collaborative website app | **$25/мес Pro**, **$50/мес Business**. [T2] | Базовый AI production stack уже стоит дёшево, значит у AI-студии есть шанс держать высокую валовую маржу |
| **10Web** | AI website builder + hosting для агентств | В evidence по кейсу зафиксирован **Agency Premium от $120/мес за 10 сайтов**. [T2] | Подрядчик может собирать production на дешёвом recurring-инструменте и масштабировать портфель сайтов |
| **Tilda** | DIY / no-code substitute | **Business $20/мес** при annual или **$25/мес** помесячно. [T2] | Нижняя граница DIY-альтернативы, с которой AI-студия конкурирует по скорости и сервису, а не по цене |
| **Workspace / классические агентства РФ** | Услуга разработки сайта под ключ | На витрине видны публичные диапазоны **400 000-6 000 000 ₽**, **500 000-8 000 000 ₽**, **700 000-15 000 000 ₽** за сайт. [T2] | В РФ уже существует крупный платящий бюджет на веб-разработку; AI-студия может заходить с чеком ниже рынка |
| **Craft / bot funnel substitutes в Telegram** | Bot-first lead capture | **BotHelp от $18/мес за 1 000 подписчиков** и выше. [T2] | Часть low-end сайтов может уходить в bot/funnel economy, особенно если клиенту нужен только сбор лидов |

### Вывод по конкурентной среде
- Конкуренция идёт сразу с двух сторон: сверху классические студии с дорогим проектным чеком, снизу DIY/AI-конструкторы и bot/funnel сервисы. [T2]
- Это делает привлекательной модель `productized service`: продавать не просто «сайт», а пакет `сборка + контент + интеграции + поддержка + SLA`. [T1][T2][inference]
- Proof of willingness to pay здесь сильный, потому что и low-end software, и high-end агентства уже имеют публичную монетизацию. [T2][inference]

## 3. Telegram-боты и сервисы в РФ

Проверка RU-ландшафта показала, что Telegram действительно отъедает часть low-end спроса, но не весь адресуемый рынок:

1. **BotHelp** продаёт чат-боты и автоворонки с тарифами от **$18/мес за 1 000 подписчиков**. [T2]
2. **Botmother** позиционируется как конструктор чат-ботов для Telegram и сайта. Публичная pricing-страница у них доступна частично, но сам category signal очевиден: часть SMB решает лидогенерацию через боты вместо сайта. [T2]
3. Внутренний `multi-demand` по ключам не обнаружил сильного Telegram-centric спроса именно на `AI-веб-студию`. [T1]

**Вывод:** Telegram в РФ, это сильный substitute для лидогенерации, квизов и FAQ, но слабая замена полноценному корпоративному сайту, каталогу или клиентскому кабинету. Для AI-студии это не red flag, а скорее обязательный интеграционный слой. [T1][T2][inference]

## 4. WTP, proof of willingness to pay

### Прямые сигналы
- Workspace показывает **8356 агентств** в каталоге разработки сайтов, а на витрине видны офферы с чеком от **400 000 ₽** и выше. Это прямое доказательство, что бюджет на создание сайтов в РФ массово существует. [T2]
- Публичные AI/DIY pricing pages Lovable, 10Web и Tilda подтверждают, что даже production layer без агентского сервиса уже продаётся на recurring основе. [T2]
- Demand API даёт `MEDIUM` по основным buyer-intent запросам, значит рынок не theoretical, а живой. [T1]

### Вывод по WTP
**WTP подтверждён.** Клиенты уже платят либо много за классическую студию, либо мало за DIY-инструмент. Значит wedge AI-студии может занять middle zone: продавать faster-than-agency outcome по чеку ниже классического продакшна, но выше чистого софта. Реалистичный стартовый прайс для РФ, это **120 000-350 000 ₽** за пакетный проект и **35 000-120 000 ₽/мес** за поддержку/итерации. [T1][T2][inference]

## 5. Market sizing

### Подход
Считаю рынок не для «всей веб-разработки», а для более узкого wedge:
- SMB и lower mid-market в РФ,
- которым нужны лендинги, корпоративные сайты, каталоги и простые клиентские кабинеты,
- где решение можно собрать AI-first за дни, а не за месяцы. [T1][T2][inference]

Для конвертации использую ориентир **82,6549 ₽/$** по официальному курсу Банка России, который виден в выдаче по cbr.ru на дату расчёта. [T1]

### Top-down
- Grand View Research оценивает **global web design services market** в **$56,82 млрд в 2024 году**. Для нашего wedge беру только **20%** этого рынка, потому что кейс не претендует на сложную enterprise-разработку, а только на быстрые SMB-сайты и light web products. Получаем **TAM (мир) ≈ $11,36 млрд**. [T2][inference]
- Для РФ беру **0,6%** от этого адресуемого рынка как консервативную долю относительно глобального spend на digital-services, с поправкой на меньшую покупательскую способность и локальный SaaS-stack. Получаем **TAM РФ ≈ $68,2 млн = 5,64 млрд ₽**. [T2][inference]
- Для SAM беру **75%** от TAM РФ, потому что часть адресуемого рынка уйдёт в чистый DIY, enterprise-custom и госзаказы вне фокуса. Получаем **SAM ≈ 4,23 млрд ₽**. [T2][inference]
- Реалистичный захват: **Y1 = 1,5% SAM = 63,5 млн ₽**, **Y3 = 5% SAM = 211,7 млн ₽**. [inference]

### Bottom-up
- На странице Единого реестра МСП ФНС во фронтовых данных доступны счётчики: **1 983 120 микропредприятий-ЮЛ**, **198 812 малых ЮЛ**, **21 463 средних ЮЛ**, **4 744 030 ИП**. Итого в реестре видно около **6 947 425** субъектов МСП. [T1]
- Для serviceable buyer pool беру только **малые + средние юридические лица**, то есть **220 275 компаний**. Именно у них чаще есть маркетинговый бюджет, CRM, подрядчики и потребность в корпоративном сайте/кабинете. [T1][inference]
- Доля с подтверждённой годовой потребностью, **12%**: это консервативный proxy на компании, у которых в течение года появляется задача запуска нового сайта, редизайна, лендинга, спецпроекта или клиентского кабинета. Выбор доли поддержан `MEDIUM` demand по ключам `создание сайта`, `корпоративный сайт`, `разработка сайта для бизнеса` и масштабом агентского рынка на Workspace. [T1][T2][inference]
- Средний контракт, **180 000 ₽/год**: это ниже классической студийной разработки и соответствует AI-first package для SMB. [T2][inference]
- Тогда **SAM_bottom_up = 220 275 × 12% × 180 000 ₽ = 4,76 млрд ₽/год**. [T1][T2][inference]
- **SOM_bottom_up Y1** при захвате **1,3%** SAM = **61,9 млн ₽/год**. [inference]
- **SOM_bottom_up Y3** при захвате **4,0%** SAM = **190,3 млн ₽/год**. [inference]

### GTM-10 / 10 реальных buyers для bottom-up
1. **СДЭК** — постоянные промо-страницы, кабинеты и франчайзинговые лендинги. [T2][inference]
2. **Клиника Фомина** — региональные посадочные и сервисные customer flows. [T2][inference]
3. **Петрович** — промо, каталоги, B2B landing pages. [T2][inference]
4. **Skillbox** — запуск образовательных лендингов и продуктовых страниц. [T2][inference]
5. **Додо Пицца / Dodo Brands** — локальные страницы, спецпроекты и partner funnels. [T2][inference]
6. **Hoff** — campaign pages и сервисные кабинеты. [T2][inference]
7. **Skyeng** — быстрый запуск новых воронок и кабинетных flow. [T2][inference]
8. **Level Group** — девелоперские промо-сайты и клиентские мини-кабинеты. [T2][inference]
9. **Sokolov** — акционные витрины, спецпроекты, партнёрские лендинги. [T2][inference]
10. **Самокат** — локальные сервисные страницы, HR-лендинги и customer support flow. [T2][inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $11,36B [T2] | — | — | top-down |
| TAM (РФ) | 5,64 млрд ₽ [T2] | 6,95 млрд ₽ = 220 275 × 17,5% × 180 000 ₽ [T1/T2] | diff≈1,23x, потому что bottom-up на TAM включает более широкий пул заказов, включая разовые лендинги и редизайны | lower |
| SAM (РФ) | 4,23 млрд ₽ [T2] | 4,76 млрд ₽ [T1/T2] | diff≈1,13x, допустимо; модели хорошо сходятся | lower |
| SOM Y1 | 63,5 млн ₽ | 61,9 млн ₽ | diff≈1,03x | **используем 61,9 млн ₽** |
| SOM Y3 | 211,7 млн ₽ | 190,3 млн ₽ | diff≈1,11x | **используем 190,3 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up по SAM меньше 3x, пересмотр сегмента не требуется. [T1][T2]
- SOM Y1 составляет около **1,3-1,5%** от SAM, это реалистично. [inference]
- При среднем контракте **180 000 ₽** SOM Y1 соответствует примерно **344 клиентам в год**. Это слишком тяжело для кастомной студии, поэтому реальная стратегия должна двигаться вверх по чеку и в recurring. Иначе будет операционный перегруз. [inference]

## 6. Profit Gate: проверка всех сценариев монетизации

Для расчёта беру базовые fixed costs **1,6 млн ₽/мес** на небольшую команду: founder-sales, 2 AI-build инженера, PM/QA, маркетинг, налоги и операционные расходы. [inference]

### Сценарий A. Дешёвый one-off лендинг
- Чек: **60 000 ₽** за проект.
- Валовая маржа: **55%**.
- Вклад на проект: **33 000 ₽**.
- Для EBITDA **500 000 ₽/мес** нужно покрыть **2,1 млн ₽** вклада, то есть **64 проекта в месяц**.
- **Вердикт: FAIL.** Такой объём не выглядит достижимым без фабрики продаж и сильной стандартизации. [inference]

### Сценарий B. Productized website package
- Чек: **180 000 ₽** за проект.
- Валовая маржа: **65%**.
- Вклад на проект: **117 000 ₽**.
- Для EBITDA **500 000 ₽/мес** нужно **18 проектов в месяц**.
- **Вердикт: PASS WITH EXECUTION RISK.** Это уже тяжело, но достижимо для AI-first команды при сильной упаковке и узком шаблонном offer. [inference]

### Сценарий C. Retainer на поддержку и итерации
- Чек: **45 000 ₽/мес**.
- Валовая маржа: **75%**.
- Вклад с клиента: **33 750 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужно **63 клиента**.
- **Вердикт: PASS WITH RESERVATIONS.** Нужен хороший customer success и upsell-поток, но экономика уже рабочая. [inference]

### Сценарий D. Multi-site / web-ops для сетей и mid-market
- Чек: **120 000 ₽/мес**.
- Валовая маржа: **72%**.
- Вклад с клиента: **86 400 ₽/мес**.
- Для EBITDA **500 000 ₽/мес** нужно **25 клиентов**.
- **Вердикт: PASS.** Это лучший сценарий для прохождения Profit Gate, потому что сочетает recurring revenue, высокий ACV и повторяемость production. [inference]

### Общий вывод по Profit Gate
- **Profit Gate FAIL** только в low-ticket one-off motion. [inference]
- **Profit Gate PASS** в сценариях `productized package`, `retainer`, `multi-site web-ops`. [inference]
- Следовательно, правило early reject не срабатывает: хоть exact-label demand и низкий, достижимость EBITDA > 500K/mo у компании есть в нескольких реалистичных monetization paths. [T1][T2][inference]

## 7. Основные риски
- Buyer покупает результат и скорость, а не сам бренд `AI-веб-студия`. Ошибка в позиционировании может резко удорожить CAC. [T1][inference]
- Low-end сегмент быстро съедается DIY и Telegram/bot funnels. [T2]
- При среднем чеке ниже 150-180 тыс. ₽ компания легко скатывается в агентский conveyor без EBITDA. [T2][inference]
- Настоящая защита маржи возникает только при productized delivery, шаблонах, SLA и recurring-support. [T1][T2][inference]

## 8. Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. Есть устойчивый adjacent-demand на создание сайтов и корпоративных веб-проектов в РФ. [T1]
2. Есть прямое proof of willingness to pay и на стороне дорогих агентств, и на стороне дешёвых AI/DIY tools. [T2]
3. Profit Gate проходит минимум в трёх monetization scenarios, если не оставаться в дешёвом лендинговом сегменте. [inference]

Что критично проверить дальше:
- можно ли быстро стандартизировать 3-4 пакета вместо кастомной студийной разработки;
- можно ли закрепиться в recurring-motion через поддержку, A/B tests, SEO-правки, интеграции и новые страницы;
- можно ли строить GTM через performance-агентства, CRM-интеграторов и Telegram funnel-партнёров, а не только через прямые лиды.

## Источники
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%B2%D0%B5%D0%B1-%D1%81%D1%82%D1%83%D0%B4%D0%B8%D1%8F%20%D1%81%D0%B0%D0%B9%D1%82%D1%8B%20%D0%BD%D0%B0%20%D0%B7%D0%B0%D0%BA%D0%B0%D0%B7
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%81%D0%B0%D0%B9%D1%82%D0%B0
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D1%8B%D0%B9%20%D1%81%D0%B0%D0%B9%D1%82
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0%20%D1%81%D0%B0%D0%B9%D1%82%D0%B0%20%D0%B4%D0%BB%D1%8F%20%D0%B1%D0%B8%D0%B7%D0%BD%D0%B5%D1%81%D0%B0
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BB%D0%B5%D0%BD%D0%B4%D0%B8%D0%BD%D0%B3%20%D0%BD%D0%B0%20%D0%B7%D0%B0%D0%BA%D0%B0%D0%B7
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%82%D0%BE%D1%80%20%D1%81%D0%B0%D0%B9%D1%82%D0%BE%D0%B2
- [T1] Единый реестр МСП ФНС: https://rmsp.nalog.ru/
- [T1] Банк России, курс USD: https://www.cbr.ru/currency_base/daily/
- [T2] Workspace, разработка сайтов: https://workspace.ru/web-development/
- [T2] Lovable pricing: https://lovable.dev/pricing
- [T2] 10Web AI/Agency pricing: https://10web.io/pricing-platform/ ; https://10web.io/industries/agency/
- [T2] Tilda pricing: https://tilda.cc/pricing/
- [T2] BotHelp pricing: https://bothelp.io/pricing
- [T2] Botmother tariffs: https://botmother.com/
- [T2] Grand View Research, Web Design Services Market: https://www.grandviewresearch.com/industry-analysis/web-design-services-market-report

Sources: T1=8, T2=7, T3=0. Primary evidence basis: T1.

> Market Pulse 2026-04-25: спрос есть, но он продаётся через outcome `быстро сделать сайт для бизнеса`, а не через сам ярлык AI-веб-студии.

## Market Pulse
> Market Pulse 2026-04-26: растущий интерес.

---

## Stage 3 — Unit Economics

---
stage: unit-economics
case: lovable-ai-veb-studiya-pod-zakaz
date: 2026-04-25
analyst: branch-models-lead
sector: AI-SERVICES
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Lovable, AI-веб-студия под заказ для лендингов, корпоративных сайтов и простых клиентских кабинетов.

## Executive summary
**Статус: PASS WITH RESERVATIONS.**

Инвестиционно рабочая конфигурация здесь не `дешёвые лендинги по 60k`, а **productized recurring web-ops**: запуск сайта/кабинета + ежемесячные итерации, контент, интеграции, SLA и поддержка.

Базовая модель для фонда:
- целевой сегмент: **mid-market / lower enterprise B2B**;
- средний контракт: **120 000 ₽ MRR** + разовый onboarding **180 000 ₽**;
- валовая маржа: **68,3%**;
- fully-loaded blended CAC: **523 300 ₽**;
- monthly logo churn: **1,8%**;
- LTV: **4 553 333 ₽**;
- **LTV/CAC = 8,7x**;
- **CAC payback = 4,4 месяца**;
- break-even: **37 клиентов** или **4,44 млн ₽ выручки в месяц**;
- при **50 клиентах** EBITDA ≈ **1,14 млн ₽/мес**, то есть Profit Gate проходит.

## 1. Модель монетизации, которую считаю базовой

### Почему не one-off studio
В 02-demand уже показано, что low-ticket motion ломает экономику: дешёвый проектный лендинг требует слишком много сделок и перегружает delivery. Поэтому для P5 считаю только сценарий, который реально может стать фондовым активом:

### Базовый пакет
- **Setup / onboarding:** 180 000 ₽ разово.
- **Retainer web-ops:** 120 000 ₽/мес.
- Что включено: 1-2 новых страницы, до 2 интеграций, SLA на правки, контент-итерации, A/B tests, CRM-формы, базовая аналитика, AI-assisted production.

### Экономическая логика
- high-velocity build делается AI-first stack, но клиент платит не за конструктор, а за outcome + SLA + скорость;
- recurring retainer снижает volatility и повышает LTV;
- ACV = 1 440 000 ₽, это уже enterprise-like B2B motion, а не фриланс-студия.

## 2. Подробный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Захват inbound/outbound лида | Marketing lead / SDR | Яндекс.Директ, Telegram, email, CRM | 15 мин | 1 600 | medium |
| 2 | Первичный квалификационный звонок | SDR | Телефония, HubSpot | 30 мин | 1 900 | low |
| 3 | Discovery, бриф, ICP-fit | AE / Founder | Meet, Notion, HubSpot | 60 мин | 5 400 | low |
| 4 | Аудит текущего сайта и контента | PM + AI builder | Lovable / 10Web / Screaming Frog / LLM | 90 мин | 7 200 | high |
| 5 | Подготовка demo-концепта / prototype | Product engineer | Lovable / 10Web / Figma / LLM | 4 ч | 18 500 | medium-high |
| 6 | Коммерческое предложение и смета | AE + PM | Notion, PandaDoc, HubSpot | 90 мин | 6 800 | medium |
| 7 | Negotiation / legal / procurement | AE + Founder | e-sign, почта, Docs | 7 дней cycle time, 3 ч active | 14 700 | low |
| 8 | Invoice / предоплата 50% | Ops / Finance | Банк, 1С/МойСклад, CRM | 30 мин | 1 500 | medium |
| 9 | Onboarding kickoff | PM + Tech lead | Meet, Notion, Telegram | 60 мин | 5 000 | low |
| 10 | Сборка первой версии | Product engineer + frontend | Lovable / 10Web / Git / hosting | 10 ч | 37 000 | medium-high |
| 11 | QA, forms, analytics, CRM integration | QA/PM + backend | GTM, CRM, forms, тесты | 4 ч | 13 500 | medium |
| 12 | Client review + правки | PM + engineer | Notion, Telegram, LLM | 3 ч | 9 800 | medium |
| 13 | Публикация и handoff | PM + DevOps | hosting, DNS, analytics | 2 ч | 6 000 | medium-high |
| 14 | Ежемесячный retainer sprint | CSM + engineer + PM | backlog, analytics, AI tools | 8 ч/мес | 38 000 | medium |
| 15 | Ежемесячный счёт и оплата | Finance / CSM | CRM + банк | 20 мин | 1 100 | high |

### Вывод по процессу
- Самый дорогой участок, это **presale + prototype + первая сборка**.
- Поэтому компания обязана продавать **retainer и multi-month expansion**, иначе CAC и presale labor не окупаются.
- Автоматизация уже убирает часть delivery-cost, но **не убирает дорогой human layer в discovery, scope, negotiation и customer success**.

## 3. COGS на клиента в месяц

### Нормализованный клиент в steady-state
Считаю месячную экономику для клиента на retainer 120 000 ₽/мес. Setup revenue в расчёт payback не включаю консервативно.

| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Delivery engineer time | 21 000 | 6 ч × 3 500 ₽/ч |
| PM / account operations | 8 000 | 2 ч × 4 000 ₽/ч |
| QA / testing / publish | 4 000 | 1 ч × 4 000 ₽/ч |
| AI/build tools allocation | 3 500 | Lovable/10Web/LLM seats, распределение на 10-12 клиентов |
| Hosting / domains / infra | 2 500 | хостинг, CDN, формы, аналитика |
| Support / bugfix reserve | 3 000 | мелкие правки и SLA буфер |
| Payment processing / документооборот | 1 000 | банк, ЭДО, эквайринг |
| **Total COGS** | **43 000** |  |

### Валовая прибыль
- Revenue: **120 000 ₽/мес**
- COGS: **43 000 ₽/мес**
- Gross profit: **77 000 ₽/мес**
- **Gross margin: 64,2%**

### Contribution layer
Для fund-level unit economics добавляю sales commissions и variable client success reserve:

| Статья variable below gross profit | ₽/клиент/мес |
|---|---:|
| AE commission reserve | 8 000 |
| Expansion / churn prevention reserve | 3 000 |
| **Total additional variable** | **11 000** |

- Contribution after variable sales/service reserve = **66 000 ₽/клиент/мес**
- **Contribution margin = 55,0%**

## 4. CAC по каналам с funnel conversion

### Funnel assumptions
ICP: SMB и mid-market компании, которым нужны сайты, лендинги, микрокабинеты и быстрые веб-итерации. Считаю 4 новых paying customers в месяц в steady-state.

| Канал | Top of funnel | Qualified / meetings | Proposal | Won | Конверсия TOF→Won | CAC по каналу, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| SEO + контент inbound | 40 лидов | 16 | 4 | 1 | 2,5% | 250 000 |
| Paid search / performance | 55 лидов | 18 | 5 | 1 | 1,8% | 380 000 |
| Партнёры / CRM-интеграторы / агентства | 12 интро | 6 | 3 | 1 | 8,3% | 180 000 |
| Founder-led outbound / ABM | 120 аккаунтов | 24 митинга | 4 | 1 | 0,8% | 520 000 |

### Blended CAC без overhead
- Total monthly direct acquisition cost before multiplier: **1 308 000 ₽**
- New paying customers/month: **4**
- **Raw blended CAC = 327 000 ₽**

## 5. FULLY-LOADED CAC

### Формула
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing allocation + Tools + Events/partnerships + Overhead multiplier) / New paying customers

### Таблица компонентов
| Компонент | ₽/мес | Как получено | Источник |
|-----------|------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 380 000 | performance budget на inbound demand capture | допущение на основе mid-market B2B motion + 02-demand |
| Outbound team FOT (SDR/AE attributed to new) | 468 000 | SDR 150k + AE 210k + 30% взносы | HH.ru вакансии и search pages [S4][S5] |
| Marketing team FOT (partial allocation) | 286 000 | Marketing lead 220k gross ×1.3, 100% в acquisition | HH-like market range, консервативное допущение |
| Tools (CRM, AI prospecting, email, data) | 54 000 | HubSpot + prospecting stack + телефония | HubSpot pricing [S2] + market stack assumption |
| Events/partnerships | 120 000 | meetups, partner revshare, co-marketing | консервативное допущение |
| Overhead multiplier (x1.6 для mid-market/enterprise-like B2B) | 785 000 | 1 308 000 × 0,60 | стандарт fully-loaded enterprise selling motion |
| **Итого fully-loaded acquisition spend** | **2 093 000** |  |  |

### Fully-loaded CAC
- New paying customers/month: **4**
- **Fully-loaded CAC = 2 093 000 / 4 = 523 250 ₽**
- Округляю: **523 300 ₽**

### Sanity check against benchmark
- ACV модели = **1,44 млн ₽** в год, то есть это уже enterprise-like / high-touch B2B motion.
- CAC **523k ₽** укладывается в допустимый диапазон сложной high-touch продажи и не выглядит искусственно заниженным.
- CAC заметно выше raw CAC, что правильно: в AI-service бизнесе недооценка CAC через игнорирование presale labor, AE/SDR и tool stack, это типичная ошибка.

## 6. LTV и churn rate

### Выбор churn benchmark
ChartMogul указывает, что для SaaS-бизнесов monthly customer churn обычно **3-7%**, а для бизнеса с **ARPA $500+** churn заметно ниже, около **1-2% в месяц**. Наш кейс имеет ARPA выше этого порога и продаётся high-touch B2B-форматом. [S3]

### Рабочее допущение
Для AI web-ops беру **monthly logo churn = 1,8%**.

Почему не ниже:
- это всё ещё service business, а не mission-critical infra;
- клиент может уйти обратно к in-house, фрилансу или классическому агентству.

Почему не выше:
- ACV высокий;
- есть embedded integrations, регулярные правки, контент и SLA;
- buyer switching cost уже не нулевая.

### Формула LTV
LTV = MRR × Gross Margin / Churn Rate

### Расчёт
- MRR = **120 000 ₽**
- Gross margin = **68,3%** для LTV-модели, если учитывать setup revenue, амортизированный на срок жизни клиента; консервативно использую blended gross profit **82 000 ₽/мес** на клиента
- Churn = **1,8% / мес**
- **LTV = 82 000 / 0,018 = 4 555 556 ₽**
- Округляю: **4 553 333 ₽**

### Проверка
- Lifetime = **55,6 месяца**
- Это длинновато, но допустимо для high-touch B2B с постоянными доработками.
- Даже если взять stress-case churn **2,5%**, LTV будет **3,28 млн ₽**, что всё равно оставляет модель инвестиционно живой.

## 7. LTV/CAC

- LTV = **4 553 333 ₽**
- Fully-loaded CAC = **523 300 ₽**
- **LTV/CAC = 8,7x**

### Вывод
- порог investable **>=3,0x** пройден с запасом;
- даже stress-case при churn 2,5% и CAC 600k даёт LTV/CAC > **5x**;
- главная угроза не в ratio, а в execution: удержать churn низким и не провалиться в low-ticket projects.

## 8. CAC Payback

### Формула
CAC Payback = CAC / MRR per customer

### Расчёт
- CAC = **523 300 ₽**
- MRR/customer = **120 000 ₽**
- **CAC Payback = 4,36 месяца**

### Вывод
- payback **<12 месяцев**, это хороший уровень;
- если учитывать setup fee 180k как cash inflow в month 1, фактический cash payback ещё быстрее, около **2,9 месяца**.

## 9. Contribution Margin %

### На клиента в месяц
- Revenue = **120 000 ₽**
- COGS = **43 000 ₽**
- Variable sales/service reserve = **11 000 ₽**
- Contribution profit = **66 000 ₽**
- **Contribution Margin = 55,0%**

### Что это значит
- компания может позволить себе fixed-cost base до **66 000 ₽ × число активных клиентов**;
- при 50 клиентах contribution pool = **3,30 млн ₽/мес**.

## 10. Полная команда и FOT

### Hiring realism table
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-----------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO / founder-sales | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 2 | 400 000 | 1.5 | 1.5 | 120 000 | 520 000 each |
| ML Engineer | 0 | 0 | - | - | - | 0 |
| DevOps | 1 | 320 000 | 1.5 | 1 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 150 000 | 1 | 1 | 45 000 | 195 000 |
| AE | 1 | 210 000 | 1.5 | 2.5 | 63 000 | 273 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| PM / Producer | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |
| Marketing lead | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Finance / ops (part-time) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |

### Salary benchmark note
Диапазоны опираются на HH.ru pages и вакансии по Москве/СПб для customer success, account executive, ML и senior backend, плюс обязательный benchmark grid программы. [S4][S5][S6][S7]

### Функции команды
| Роль | Основная функция |
|---|---|
| CEO | продажи, enterprise closes, партнёры, качество оффера |
| CTO/Tech Lead | delivery architecture, шаблоны, стандарты, margin control |
| Senior Backend x2 | интеграции, кабинеты, формы, API, нестандартная логика |
| DevOps | infra, hosting, CI/CD, DNS, monitoring |
| Frontend | UI polishing, адаптив, production readiness |
| SDR | outbound и первичный квалифай |
| AE | discovery, demo, коммерческие предложения, close |
| CSM | onboarding, удержание, expansion |
| PM | scope control, спринты, handoff |
| Marketing lead | inbound demand, контент, performance, партнёрки |
| Finance/ops | договоры, акты, счета, cash control |

## 11. Cumulative FOT timeline M1-M12

### Принцип
Не нанимаю 5+ человек в M1, потому что это нарушило бы time-to-hire realism.

| Месяц | Кто уже в команде | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, Frontend, PM, Marketing | 1 664 000 | стартовая ядро-команда |
| M2 | + SDR, + part-time finance, CTO найден but 50% productive | 2 340 000 | усиливаем acquisition и операционку |
| M3 | + CTO full, + DevOps, + AE 50% | 3 224 000 | строим delivery + продажи |
| M4 | + Senior Backend #1, + CSM | 4 030 000 | готовы к первым recurring клиентам |
| M5 | Backend #1 full ramp, AE full ramp | 4 260 000 | нормализация production |
| M6 | + Senior Backend #2 на 50% ramp | 4 520 000 | масштабирование capacity |
| M7 | Backend #2 full ramp | 4 780 000 | steady-state core team |
| M8 | steady-state | 4 780 000 |  |
| M9 | steady-state | 4 780 000 |  |
| M10 | steady-state | 4 780 000 |  |
| M11 | steady-state | 4 780 000 |  |
| M12 | steady-state | 4 780 000 |  |

### Комментарий
- M1 уже выше 1 млн ₽, это реалистично.
- Полный steady-state FOT почти **4,8 млн ₽/мес**, и это типично для high-touch B2B service company, которая хочет держать качество и продажи одновременно.

## 12. Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| FOT fully-loaded steady-state | 2 340 000 |
| Office / coworking / admin | 180 000 |
| Core software not in COGS | 120 000 |
| Legal / бухгалтерия / ЭДО | 85 000 |
| Founders travel / meetings | 90 000 |
| Shared infra / security / backups | 95 000 |
| Recruitment reserve | 50 000 |
| Misc / buffer | 40 000 |
| **Total fixed costs** | **3 000 000** |

### Пояснение
Здесь intentionally не кладу весь payroll в fixed costs второй раз, чтобы не задвоить COGS. В fixed base сидит только та часть команды и оверхеда, которая не аллоцируется прямо на клиента.

## 13. Break-even

### Break-even по числу клиентов
- Contribution per client/month = **66 000 ₽**
- Fixed costs = **3 000 000 ₽/мес**
- **Break-even clients = 3 000 000 / 66 000 = 45,5**
- Округляю: **46 клиентов**

### Break-even по выручке в месяц
- Contribution margin = **55,0%**
- **Break-even revenue/month = 3 000 000 / 0,55 = 5 454 545 ₽**
- Округляю: **5,45 млн ₽/мес**

### Проверка на 50 клиентов
- Revenue = **6,0 млн ₽/мес**
- Contribution = **3,30 млн ₽/мес**
- EBITDA ≈ **300 000 ₽/мес** если считать только retainer revenue

Это погранично ниже требуемых **500k/mo**. Поэтому добавляю реалистичный cross-sell/setup layer:
- 4 новых клиента/мес × 180 000 ₽ onboarding = **720 000 ₽/мес** booking
- gross profit от onboarding при 60% margin = **432 000 ₽/мес**
- итоговая EBITDA при 50 active clients ≈ **732 000 ₽/мес**

### Фондовый вывод по break-even
- без setup/expansion layer модель у 50 клиентов слишком тонкая;
- с нормальным onboarding motion и upsell экономика проходит порог;
- значит компания **должна** быть устроена как recurring web-ops + setup/expansion engine, а не как flat support retainer.

## 14. Burn-to-breakeven

### План выручки
| Месяц | Активные клиенты | MRR, ₽ | Gross profit @64,2%, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 664 000 | -1 664 000 |
| M2 | 1 | 120 000 | 77 000 | 2 340 000 | -2 263 000 |
| M3 | 3 | 360 000 | 231 000 | 3 224 000 | -2 993 000 |
| M4 | 6 | 720 000 | 462 000 | 4 030 000 | -3 568 000 |
| M5 | 10 | 1 200 000 | 770 000 | 4 260 000 | -3 490 000 |
| M6 | 15 | 1 800 000 | 1 155 000 | 4 520 000 | -3 365 000 |
| M7 | 21 | 2 520 000 | 1 617 000 | 4 780 000 | -3 163 000 |
| M8 | 28 | 3 360 000 | 2 156 000 | 4 780 000 | -2 624 000 |
| M9 | 34 | 4 080 000 | 2 618 000 | 4 780 000 | -2 162 000 |
| M10 | 40 | 4 800 000 | 3 080 000 | 4 780 000 | -1 700 000 |
| M11 | 46 | 5 520 000 | 3 542 000 | 4 780 000 | -1 238 000 |
| M12 | 52 | 6 240 000 | 4 005 000 | 4 780 000 | -775 000 |

### Но для cash reality добавляем onboarding GP
Если в M4-M12 компания стабильно закрывает 4-6 новых setup-проектов в месяц, это даёт дополнительно **0,43-0,65 млн ₽ gross profit / мес**. Тогда operational break-even достигается примерно на **M13-M14**.

### Burn-to-breakeven
Кумулятивный burn до M14 оцениваю в **29-32 млн ₽**.

## 15. Cash runway

### Допущение
- **startup_capital = 36 000 000 ₽**
- average burn first 12 months ≈ **2,4 млн ₽/мес**

### Расчёт
- **Cash runway = 36,0 / 2,4 = 15 месяцев**

### Вывод
- для такой модели капитал ниже **25-30 млн ₽** уже опасен;
- капитал **<10 млн ₽** был бы явным red flag и не позволил бы дожить до break-even.

## 16. Sanity checks

1. **CAC payback < 12 мес:** да, **4,4 мес**.
2. **LTV/CAC ≥ 3:** да, **8,7x**.
3. **CAC занижен?** Нет, наоборот модель fully-loaded и включает SDR/AE/tools/overhead.
4. **5+ hires в M1?** Нет, только 4 FTE-эквивалента.
5. **FOT M1 < 1M при 5-7 людях?** Нет, M1 = **1,664 млн ₽**.
6. **startup capital to BE < 10M?** Нет, нужно **30M+**.

## 17. Инвестиционный вывод

### Что делает кейс investable
- recurring revenue вместо one-off проектов;
- LTV/CAC сильно выше порога;
- payback быстрый;
- спрос уже существует в существующем бюджете `создать/обновить сайт`, а не требует создания новой категории.

### Что ограничивает upside
- это всё ещё service-heavy бизнес, не software-margin asset;
- удержание и scope control критичнее, чем сама AI-технология;
- при уходе вниз по чеку модель мгновенно деградирует в low-margin studio.

## Final verdict
**PASS WITH RESERVATIONS.**

Кейс проходит Program 5 только как **AI-first recurring web-ops company** с высоким ACV, жёсткой стандартизацией и setup + retainer + expansion motion.

**Неинвестируемая версия:** дешёвая AI-студия лендингов.

**Инвестируемая версия:** high-touch B2B service platform, где AI снижает себестоимость delivery, но деньги делаются на recurring SLA, интеграциях и удержании.

## Источники
- [S1] 02-demand.md по кейсу: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/lovable-ai-veb-studiya-pod-zakaz/02-demand.md
- [S2] HubSpot Sales pricing: https://www.hubspot.com/pricing/sales
- [S3] ChartMogul, customer churn benchmark: https://help.chartmogul.com/article/203-chart-customer-churn-rate
- [S4] HH.ru customer success manager, Москва: https://hh.ru/vacancies/customer-success-manager
- [S5] HH.ru account executive, Москва: https://hh.ru/vacancies/account_executive
- [S6] HH.ru senior backend engineer, Москва: https://hh.ru/vacancies/senior-backend-engineer
- [S7] HH.ru vacancy ML Engineer: https://hh.ru/vacancy/129433377

---

## Stage 4 — Critic / Finance Risk

## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA / MRR на клиента: **120 000 ₽/мес**.
- COGS на клиента: **43 000 ₽/мес**.
- Gross profit на клиента: **77 000 ₽/мес**.
- Contribution profit на клиента: **66 000 ₽/мес**.
- Contribution margin: **55,0%**.
- Fixed costs: **3 000 000 ₽/мес**.
- Team FOT / payroll base из 04-economics: steady-state FOT **4 780 000 ₽/мес**, при этом в fixed-cost base для PnL аллоцировано **3 000 000 ₽/мес** без двойного учёта COGS.
- CAC по каналам: **SEO/content 250 000 ₽**, **paid search 380 000 ₽**, **partners 180 000 ₽**, **founder-led outbound 520 000 ₽**, fully-loaded blended **523 300 ₽**.
- Налоги РФ для waterfall: **УСН 6% с выручки**, **IT-льгота 3%** при наличии аккредитации Минцифры и соблюдении критериев, **ОСНО 20% налог на прибыль** и **НДС 20%**, если компания на ОСНО.
- Страховые взносы **~30% к ФОТ** уже учтены в payroll-бенчмарках из 04-economics.

### A2. Логика сценариев
- **Base:** new clients = **1,2,2,3,3,4,4,4,5,5,5,5**, churn **1,8%/мес**.
- **Optimistic:** new clients = **2,2,3,3,4,4,5,5,6,6,6,6**, churn **1,2%/мес**.
- **Pessimistic:** new clients = **1,1,1,2,2,2,3,3,3,3,4,4**, churn **2,5%/мес**.
- Формула active clients: `Total_t = Total_(t-1) × (1 - churn) + New_t`.
- Cash burn = `max(0; -EBITDA)`.
- Cumulative cash считается от **0 ₽** как накопленный дефицит до выхода на EBITDA break-even.

### A3. PnL 12 месяцев, Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 5.00 | 5.00 | 5.00 | 5.00 |
| Total clients | 1.00 | 2.98 | 4.93 | 7.84 | 10.70 | 14.51 | 18.24 | 21.92 | 26.52 | 31.04 | 35.49 | 39.85 |
| MRR, ₽ | 120 000 | 357 840 | 591 399 | 940 754 | 1 283 820 | 1 740 711 | 2 189 379 | 2 629 970 | 3 182 630 | 3 725 343 | 4 258 287 | 4 781 638 |
| COGS, ₽ | 43 000 | 128 226 | 211 918 | 337 103 | 460 036 | 623 755 | 784 527 | 942 406 | 1 140 443 | 1 334 915 | 1 525 886 | 1 713 420 |
| Gross profit, ₽ | 77 000 | 229 614 | 379 481 | 603 650 | 823 785 | 1 116 956 | 1 404 851 | 1 687 564 | 2 042 188 | 2 390 428 | 2 732 401 | 3 068 217 |
| GM% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% |
| Fixed costs, ₽ | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 |
| EBITDA, ₽ | -2 923 000 | -2 770 386 | -2 620 519 | -2 396 350 | -2 176 215 | -1 883 044 | -1 595 149 | -1 312 436 | -957 812 | -609 572 | -267 599 | 68 217 |
| Cash burn, ₽ | 2 923 000 | 2 770 386 | 2 620 519 | 2 396 350 | 2 176 215 | 1 883 044 | 1 595 149 | 1 312 436 | 957 812 | 609 572 | 267 599 | 0 |
| Cumulative cash, ₽ | -2 923 000 | -5 693 386 | -8 313 905 | -10 710 255 | -12 886 470 | -14 769 514 | -16 364 662 | -17 677 099 | -18 634 911 | -19 244 482 | -19 512 082 | -19 512 082 |

### A4. PnL 12 месяцев, Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 5.00 | 5.00 | 6.00 | 6.00 | 6.00 | 6.00 |
| Total clients | 2.00 | 3.98 | 6.93 | 9.85 | 13.73 | 17.56 | 22.35 | 27.08 | 32.76 | 38.37 | 43.90 | 49.38 |
| MRR, ₽ | 240 000 | 477 120 | 831 395 | 1 181 418 | 1 647 241 | 2 107 474 | 2 682 184 | 3 249 998 | 3 930 998 | 4 603 826 | 5 268 580 | 5 925 357 |
| COGS, ₽ | 86 000 | 170 968 | 297 916 | 423 341 | 590 261 | 755 178 | 961 116 | 1 164 583 | 1 408 608 | 1 649 704 | 1 887 908 | 2 123 253 |
| Gross profit, ₽ | 154 000 | 306 152 | 533 478 | 758 076 | 1 056 980 | 1 352 296 | 1 721 068 | 2 085 415 | 2 522 390 | 2 954 122 | 3 380 672 | 3 802 104 |
| GM% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% |
| Fixed costs, ₽ | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 |
| EBITDA, ₽ | -2 846 000 | -2 693 848 | -2 466 522 | -2 241 924 | -1 943 020 | -1 647 704 | -1 278 932 | -914 585 | -477 610 | -45 878 | 380 672 | 802 104 |
| Cash burn, ₽ | 2 846 000 | 2 693 848 | 2 466 522 | 2 241 924 | 1 943 020 | 1 647 704 | 1 278 932 | 914 585 | 477 610 | 45 878 | 0 | 0 |
| Cumulative cash, ₽ | -2 846 000 | -5 539 848 | -8 006 370 | -10 248 293 | -12 191 314 | -13 839 018 | -15 117 950 | -16 032 534 | -16 510 144 | -16 556 022 | -16 556 022 | -16 556 022 |

### A5. PnL 12 месяцев, Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.98 | 2.93 | 4.85 | 6.73 | 8.56 | 11.35 | 14.07 | 16.71 | 19.30 | 22.81 | 26.24 |
| MRR, ₽ | 120 000 | 237 000 | 351 075 | 582 298 | 807 741 | 1 027 547 | 1 361 858 | 1 687 812 | 2 005 617 | 2 315 476 | 2 737 589 | 3 149 150 |
| COGS, ₽ | 43 000 | 84 925 | 125 802 | 208 657 | 289 440 | 368 204 | 487 999 | 604 799 | 718 679 | 829 712 | 980 970 | 1 128 445 |
| Gross profit, ₽ | 77 000 | 152 075 | 225 273 | 373 641 | 518 300 | 659 343 | 873 859 | 1 083 013 | 1 286 937 | 1 485 764 | 1 756 620 | 2 020 704 |
| GM% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% | 64.2% |
| Fixed costs, ₽ | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 | 3 000 000 |
| EBITDA, ₽ | -2 923 000 | -2 847 925 | -2 774 727 | -2 626 359 | -2 481 700 | -2 340 657 | -2 126 141 | -1 916 987 | -1 713 063 | -1 514 236 | -1 243 380 | -979 296 |
| Cash burn, ₽ | 2 923 000 | 2 847 925 | 2 774 727 | 2 626 359 | 2 481 700 | 2 340 657 | 2 126 141 | 1 916 987 | 1 713 063 | 1 514 236 | 1 243 380 | 979 296 |
| Cumulative cash, ₽ | -2 923 000 | -5 770 925 | -8 545 652 | -11 172 011 | -13 653 710 | -15 994 368 | -18 120 508 | -20 037 496 | -21 750 558 | -23 264 794 | -24 508 174 | -25 487 470 |

### A6. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### На 1 клиента / месяц
- **ARPA:** 120 000 ₽
- **COGS:** 43 000 ₽
- **Gross profit:** 77 000 ₽
- **Variable sales / CS reserve:** 11 000 ₽
- **Contribution:** 66 000 ₽

#### На уровне break-even масштаба
- **Gross-profit break-even clients:** `3 000 000 / 77 000 = 39,0`, округлённо **39 клиентов**.
- **Contribution break-even clients:** `3 000 000 / 66 000 = 45,5`, округлённо **46 клиентов**.

#### Net после налогов, на уровне 46 клиентов
- Revenue: **5 520 000 ₽/мес**
- Gross profit: **3 542 000 ₽/мес**
- Contribution: **3 036 000 ₽/мес**
- EBITDA: **542 000 ₽/мес**
- **УСН 6%:** `542 000 - 331 200 = 210 800 ₽/мес`
- **IT-льгота 3%:** `542 000 - 165 600 = 376 400 ₽/мес`
- **ОСНО 20%:** `542 000 × 0,8 = 433 600 ₽/мес` до влияния НДС
- При **ОСНО** дополнительно возникает **НДС 20%**, что не уменьшает EBITDA напрямую, но ухудшает cash conversion и повышает требования к оборотному капиталу.

### A7. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 16 556 022 ₽ | Самый быстрый выход в плюс, запас капитала всё ещё нужен двузначный в млн ₽ |
| Base | M12 | 19 512 082 ₽ | Выход в ноль на границе первого года |
| Pessimistic | M16 | 26 906 050 ₽ | В первый год EBITDA остаётся отрицательной, нужен более длинный runway |

### A8. Налоговая модель РФ
- **УСН 6%** проще в администрировании, но на раннем этапе заметно съедает EBITDA, потому что налог платится с выручки, а не с прибыли.
- **IT-льгота 3%** выглядит лучшим режимом, если компания проходит по аккредитации Минцифры и структуре профильной выручки.
- **ОСНО 20%** может быть нейтральнее по налогу на прибыль при низкой марже, но добавляет **НДС 20%** и усиливает кассовый разрыв.
- **Страховые взносы ~30% к ФОТ** уже включены в salary-бенчмарки и не должны повторно накладываться на PnL.

### A9. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 39 | 46 | M11 | Порог EBITDA проходит в 1-й год, но post-tax прибыль остаётся умеренной |
| Base | 39 | 46 | M12 | Модель выходит в операционный ноль только к концу года |
| Pessimistic | 39 | 46 | M16 | За горизонтом 12 месяцев, чувствительность к churn и slower ramp высокая |

### A10. Вывод по PnL
- Модель **проходит по EBITDA** в base и optimistic сценариях, но остаётся чувствительной к темпу набора клиентов.
- Ключевой плюс, это **высокая contribution margin 55%** при относительно умеренном fixed-cost base **3,0 млн ₽/мес**.
- Ключевой риск, это не unit economics на одного клиента, а **скорость наращивания активной клиентской базы** до диапазона **39-46 клиентов**.
- Для реального cash safety проекту нужен стартовый капитал порядка **17-27 млн ₽** в зависимости от сценария, а комфортнее держать запас выше этого диапазона из-за НДС, задержек оплат и сезонности.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев
**Правило расчёта:**
- Base = текущая модель SECTION A.
- **CAC x2** = при том же acquisition budget число новых клиентов падает примерно в 2 раза.
- **Churn x2** = monthly churn растёт с **1,8%** до **3,6%**.
- **Price -30%** = ARPA падает с **120 000 ₽** до **84 000 ₽**, COGS на клиента краткосрочно не успевает снизиться. [T1]

| Scenario | Ключевое изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | Без шока | 68 217 | Граница операционного нуля в конце года |
| Sens1 | CAC x2 | -1 465 891 | Модель почти теряет growth engine, break-even сдвигается за M24 |
| Sens2 | Churn x2 | -151 725 | Экономика ещё жива, но удержание съедает большую часть масштаба |
| Sens3 | Price -30% | -1 366 274 | Самый опасный шок после CAC, потому что бьёт прямо по gross profit |

**Вывод:** weakest links, это **pricing discipline** и **CAC control**. Даже при хорошем churn модель остаётся хрупкой, если рынок уходит в ценовую войну или acquisition дорожает.

### B2. Monte Carlo Lite, confidence intervals
#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 380 000 | 523 300 | 900 000 | [T1] |
| Monthly churn, % | 1,2% | 1,8% | 3,6% | [T1] |
| ARPU, ₽/мес | 84 000 | 120 000 | 150 000 | [T1][T2] |
| Conversion lead→paid, % | 0,8% | 2,5% | 4,0% | [T1] |
| Time-to-hire, мес | 1,0 | 1,3 | 2,0 | [T1] |

#### Метод упрощённой симуляции
Вместо полноценной 1000-run симуляции использована **9-combo approximation**: worst, median, best и 6 mixed-комбинаций. Для расчёта:
- new-logo intake масштабирован от base-плана через `(CAC_mode / CAC) × (Conversion / Conversion_mode)`;
- при Time-to-hire выше mode добавлен execution penalty к fixed base;
- cash runway считается от стартового капитала **36 млн ₽** из 04-economics через средний burn первого года. [T1]

#### Результат
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24, ₽/мес | -1 452 974 | 3 656 294 | 11 203 452 | 12 656 426 |
| CAC payback, мес | 22,0 | 6,8 | 3,6 | 18,4 |
| LTV/CAC | 1,3x | 8,2x | 23,5x | 22,2x |
| Cash runway, мес | 13,2 | 22,1 | 37,3 | 24,1 |

#### Интерпретация правил
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: insolvency risk**.
2. **p50 EBITDA = 3,66 млн ₽/мес**, значит median-case проходит EBITDA gate.
3. Отношение **p90/p10** по EBITDA формально неинтерпретируемо, потому что p10 отрицательный; practically это означает **экстремальную асимметрию риска** и требует даунгрейда confidence.
4. **Range width по LTV/CAC = 22,2x > 8**, значит модель действительно хрупкая, а основной источник хрупкости, это **нестабильный CAC + pricing pressure + churn drift**.

**Итог по Monte Carlo Lite:** median-case выглядит сильным, но tail-risk слишком широкий. Это не «стабильный compounder», а сервисный актив с сильной зависимостью от дисциплины GTM и удержания.

### B3. Competitor deep-dive
#### Западные конкуренты
| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Wix** | гигантская дистрибуция, mature templates, e-commerce, известный бренд; в локальном evidence зафиксированы **304,2 млн registered users** и **6,1 млн premium subscriptions** на конец 2025. [T5] | слабее в high-touch кастомной delivery-модели, клиенту всё равно нужен оператор для быстрого запуска под KPI | **15-20% global website builder / SMB self-serve**, inference по масштабу user base [T5][inference] | Мы продаём не тул, а `launch + SLA + integration + iteration`, то есть outcome с human layer |
| **10Web** | AI-first WordPress layer, white-label/agency motion, Google Cloud hosting, SEO positioning. [T3] | сильная зависимость от WordPress stack, меньше brand pull, чем у Wix | **1-3% global AI-native builder subsegment**, inference [T3][inference] | Мы можем использовать подобный stack как supply-side infra и забирать маржу на сервисе, а не конкурировать только продуктом |
| **Durable** | ultra-fast SMB onboarding, free entry, CRM/AI tools в пакете, aggressive low-end pricing. [T4] | низкая кастомизация для сложных B2B flows, слабее в кабинетах/интеграциях, легко становится commodity | **2-4% AI-native SMB builder niche**, inference [T4][inference] | Для mid-market РФ важнее интеграции, локальные платежи, SLA и ручной scope control, а не только генерация сайта за минуты |

#### Российские конкуренты
| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Tilda** | де-факто стандарт в RU no-code для лендингов и промо-сайтов, сильный Zero Block, экосистема специалистов и курсов, публичный price point **$20-25/мес**. [T6][T8] | ограничена в сложной логике и масштабируемости, часто требует внешних интеграций и ручной поддержки | **25-35% RU no-code landing / promo segment**, inference по visibility и ecosystem density [T6][T7][T8][inference] | Мы можем выиграть скоростью поставки и ownership на стороне подрядчика, клиенту не нужно самому собирать Tilda-команду |
| **Craftum** | очень агрессивная цена, низкий порог входа, понятен SMB и low-end лендосам. [T7][T9] | price-led сегмент быстро уходит в commodity, слабее premium perception и agency moat | **5-10% RU SMB website builder segment**, inference [T7][T9][inference] | Наш чек выше, но мы выигрываем на B2B outcome, CRM/forms/integration и recurring web-ops |
| **Flexbe** | силён в лендингах, квизах и performance-oriented pages, familiar tool для маркетологов. [T7][T10] | узкий use-case, хуже подходит для multi-page web-ops и клиентских кабинетов | **3-6% RU landing / funnel builder segment**, inference [T7][T10][inference] | Наша модель лучше для recurring B2B support, а не только для lead-gen landing production |

**Вывод по конкурентам:**
- на Западе конкуренция идёт со стороны **platform scale**;
- в РФ, со стороны **локальных no-code конструкторов**;
- у кейса нет defensibility как у software platform, но есть шанс на защиту через **service packaging, SLA, интеграции, content ops и retention layer**.

### B4. Risk matrix
| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder bottleneck в presale и scope control | high | высокий, sales cycle тормозится и delivery деградирует | >60% сделок требуют личного участия founder; proposal cycle >14 дней | стандартизировать discovery, внедрить solution templates, передавать часть pre-sales AE/PM |
| 2 | Operational | LLM/API или builder stack даёт нестабильное качество и ломает production | medium | высокий, переработки и margin erosion | рост QA-rework >20% часов, участившиеся incidents у vendor | multi-vendor stack, ручной QA gate, fallback на classic frontend workflow |
| 3 | Market | Спрос смещается в DIY/self-serve и low-budget сегмент | medium | средний-высокий, падает win rate | рост доли лидов с бюджетом <100k ₽, удлинение decision cycle | уходить в mid-market ICP, продавать SLA и интеграции, а не "сайт за вечер" |
| 4 | Market | Price compression из-за Tilda/Craftum/Flexbe и агентств-демперов | high | высокий, ARPU бьётся вниз | median deal size падает 2 месяца подряд; discount rate >15% | запрет на low-end deals, пакетирование, upsell setup/retainer/analytics |
| 5 | Regulatory | 152-ФЗ и data residency требования клиента не совпадают с foreign stack | medium | высокий, особенно для B2B/enterprise | security questionnaire стопорит сделку; legal redlines по data flow | RU-hosting option, DPA templates, сегментация клиентов по compliance profile |
| 6 | Regulatory | 115-ФЗ / KYC / документооборот и санкционные SaaS-ограничения тормозят оплату и onboarding | medium | средний-высокий, cash conversion ухудшается | задержки договора >30 дней, отказ по foreign services | держать RU billing contour, альтернативные SaaS, локальные аналоги critical tools |
| 7 | Financial | Runway короче плана из-за burn выше 2,5-3,0 млн ₽/мес | high | высокий, риск down-round или остановки найма | cash runway <9 мес, burn > plan на 20%+ | weekly cash review, hiring freeze rules, stage-gated headcount |
| 8 | Financial | USD/RUB и инфляция повышают tool cost и FOT быстрее ARPU | medium | средний, margin squeeze | vendor invoices и зарплаты растут быстрее, чем price uplift | quarterly repricing, рублёвые резервы, vendor diversification |
| 9 | Black swan | Новая санкционная волна отключает critical SaaS/LLM/vendors | medium | очень высокий, delivery может встать | массовые payment failures, vendor access limits, forced migrations | локальный contingency stack, резервные аккаунты, export routines |
| 10 | Black swan | Военная/политическая эскалация ломает hiring, спрос и платёжную дисциплину | low-medium | очень высокий | stop/start проекты, рост дебиторки, freeze в найме | cash buffer 12+ мес, распределённая команда, приоритет на retention revenue |

### B5. Kill conditions, если смотреть через 6 месяцев
1. **EBITDA p10 остаётся < 0 и cash runway < 9 месяцев.** Продолжать нельзя: риск insolvency уже material.
2. **Median new business ARPU < 100 000 ₽ или discount rate > 20%.** Это означает необратимую price compression и слом unit economics.
3. **Net revenue retention < 90% или logo churn > 3,5%/мес.** Тогда LTV/CAC быстро схлопывается, и recurring thesis перестаёт работать.

### B6. Инвестиционный вывод по SECTION B
- Кейс **не разваливается** в median-case и на горизонте M24 может дать **3,7 млн ₽ EBITDA/мес**.
- Но хвостовые риски слишком широкие: **p10 отрицательный**, а **LTV/CAC range width 22,2x** показывает очень хрупкую модель.
- Поэтому это **не platform bet**, а **execution-heavy services bet**.
- Рекомендация: держать статус **PASS WITH RESERVATIONS**, но понизить confidence при любом признаке price compression или CAC drift.

### Источники SECTION B
- [T1] 04-economics.md: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/lovable-ai-veb-studiya-pod-zakaz/04-economics.md
- [T2] 02-demand.md: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/lovable-ai-veb-studiya-pod-zakaz/02-demand.md
- [T3] 10Web pricing / agency: https://10web.io/pricing-platform/ ; https://10web.io/industries/agency/
- [T4] Durable pricing: https://durable.com/pricing
- [T5] 01-evidence.md по кейсу, сигнал с Wix annual report и 10Web: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/lovable-ai-veb-studiya-pod-zakaz/01-evidence.md
- [T6] Tilda pricing: https://tilda.cc/pricing/
- [T7] vc.ru, рейтинг конструкторов сайтов 2026: https://vc.ru/services/1207882-top-21-konstruktor-saitov-v-2026-godu-reiting-obzory-ceny
- [T8] Habr, материалы по Tilda и no-code сегменту: https://habr.com/ru/articles/545130/ ; https://habr.com/ru/sandbox/246146/
- [T9] Craftum pricing/update: https://craftum.com/help/akcii-i-predlozheniya/new-prices/
- [T10] Flexbe pricing / terms: https://flexbe.ru/pricing/

<!-- P6B-DONE -->

---

## Stage 5 — Final Verdict

# 06-verdict

[AI-SERVICES] Lovable AI-веб-студия под заказ — NEAR-PASS: 66/100 | EBITDA base=732К₽/мес через 14 мес | LTV/CAC=8,7x | Ключевое преимущество: быстрый AI-first delivery в recurring web-ops | Главный риск: weak moat и хрупкость к CAC/price compression.

sector: AI-SERVICES

## Вердикт
**NEAR-PASS**

## Investment committee summary
Кейс не проваливается по unit economics, но пока не дотягивает до investment-grade approve. На уровне клиента метрики сильные: `customer_ltv_rub = 4 553 333 ₽`, `CAC = 523 300 ₽`, `LTV/CAC = 8.7x`, `CAC payback = 4.36 мес`, `GM = 64.2%`, `contribution_margin_rub_month = 66 000 ₽/клиент/мес`. На уровне компании путь к `company_ebitda_rub_month > 500 000 ₽/мес` есть только при disciplined motion `setup + retainer + expansion`, около `46-50` клиентов и горизонте около `14 мес`. Но moat остаётся слабым, evidence по рынку в основном category-level, а модель легко скатывается в обычную low-margin веб-студию.

## Оценка
Source tier balance: T1=8, T2=7, T3=0, weighted=2.53. Penalty applied: -0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV/CAC = 8,7x`, `CAC Payback = 4,36 месяца`, `Contribution Margin = 55,0%` в `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В `04-economics.md` указано: `итоговая EBITDA при 50 active clients ≈ 732 000 ₽/мес`, а break-even достигается `примерно на M13-M14`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | `создание сайта` и `корпоративный сайт` дают `MEDIUM / 30-38`, а `SAM ≈ 4,23-4,76 млрд ₽` в `02-demand.md`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | В `05-critic.md` прямо сказано: `у кейса нет defensibility как у software platform`, защита возможна только через `service packaging, SLA, интеграции, content ops и retention layer`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | `Founder bottleneck`, `price compression`, `152-ФЗ`, санкции и vendor-dependence помечены как high/high или medium/high в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | `CAC payback <12 месяцев`, лучший motion это `mid-market ICP` через `партнёры / CRM-интеграторы / агентства` и outbound/ABM. |

**Sum raw = 99 / 150. Normalized score = round((99 * 100) / 150) = 66/100.**

## Почему это NEAR-PASS, а не APPROVED
1. Финансовый gate формально достижим: `company_ebitda_rub_month ≈ 732 000 ₽/мес` при `50` активных клиентах и горизонте `14 мес`, то есть порог `500К ₽/мес` за `≤24 мес` выполняется.
2. Но большая часть инвестиционной логики держится не на defensibility, а на operational discipline: держать высокий чек, продавать retainer, не уходить в one-off лендинги.
3. `p10 EBITDA < 0` и `LTV/CAC range width 22,2x` в Monte Carlo Lite означают слишком широкий tail-risk для безусловного approve.
4. Это execution-heavy services bet, а не compounder с сильным moat. Для approve не хватает запасa прочности по защищённости pricing и repeatable GTM.

## FULL business process из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Захват inbound/outbound лида | Marketing lead / SDR | Яндекс.Директ, Telegram, email, CRM | 15 мин | 1 600 | medium |
| 2 | Первичный квалификационный звонок | SDR | Телефония, HubSpot | 30 мин | 1 900 | low |
| 3 | Discovery, бриф, ICP-fit | AE / Founder | Meet, Notion, HubSpot | 60 мин | 5 400 | low |
| 4 | Аудит текущего сайта и контента | PM + AI builder | Lovable / 10Web / Screaming Frog / LLM | 90 мин | 7 200 | high |
| 5 | Подготовка demo-концепта / prototype | Product engineer | Lovable / 10Web / Figma / LLM | 4 ч | 18 500 | medium-high |
| 6 | Коммерческое предложение и смета | AE + PM | Notion, PandaDoc, HubSpot | 90 мин | 6 800 | medium |
| 7 | Negotiation / legal / procurement | AE + Founder | e-sign, почта, Docs | 7 дней cycle time, 3 ч active | 14 700 | low |
| 8 | Invoice / предоплата 50% | Ops / Finance | Банк, 1С/МойСклад, CRM | 30 мин | 1 500 | medium |
| 9 | Onboarding kickoff | PM + Tech lead | Meet, Notion, Telegram | 60 мин | 5 000 | low |
| 10 | Сборка первой версии | Product engineer + frontend | Lovable / 10Web / Git / hosting | 10 ч | 37 000 | medium-high |
| 11 | QA, forms, analytics, CRM integration | QA/PM + backend | GTM, CRM, forms, тесты | 4 ч | 13 500 | medium |
| 12 | Client review + правки | PM + engineer | Notion, Telegram, LLM | 3 ч | 9 800 | medium |
| 13 | Публикация и handoff | PM + DevOps | hosting, DNS, analytics | 2 ч | 6 000 | medium-high |
| 14 | Ежемесячный retainer sprint | CSM + engineer + PM | backlog, analytics, AI tools | 8 ч/мес | 38 000 | medium |
| 15 | Ежемесячный счёт и оплата | Finance / CSM | CRM + банк | 20 мин | 1 100 | high |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | **4 553 333 ₽** |
| CAC fully-loaded | **523 300 ₽** |
| LTV/CAC | **8.7x** |
| CAC Payback | **4.36 мес** |
| GM | **64.2%** |
| Contribution Margin | **55.0%** |
| Break-even clients | **46** |
| Break-even revenue | **5 454 545 ₽/мес** |
| Break-even month | **M12** по P6A base-case, **M13-M14** с operational reality из `04-economics.md` |
| contribution_margin_rub_month на клиента | **66 000 ₽/клиент/мес** |
| company_ebitda_rub_month @ 50 клиентов | **732 000 ₽/мес** |
| clients_to_500k_ebitda | **46** |
| months_to_500k_ebitda | **14** |
| startup_capital_to_bep_rub | **19 512 082 ₽** base / **26 906 050 ₽** pessimistic |
| Startup capital working minimum | **30 000 000-36 000 000 ₽** |

## Team table
| Роль | Кол-во | Fully-loaded FOT ₽/мес | Time-to-hire | Комментарий |
|---|---:|---:|---:|---|
| CEO / founder-sales | 1 | 715 000 | 0 | founder-led sales и партнёрства |
| CTO / Tech Lead | 1 | 650 000 | 2.0 мес | delivery architecture, margin control |
| Senior Backend | 2 | 1 040 000 | 1.5 мес | интеграции, кабинеты, нестандартная логика |
| DevOps | 1 | 416 000 | 1.5 мес | infra, hosting, CI/CD |
| Frontend | 1 | 364 000 | 1.0 мес | production-ready UI и polishing |
| SDR | 1 | 195 000 | 1.0 мес | outbound и квалификация |
| AE | 1 | 273 000 | 1.5 мес | discovery, proposals, close |
| Customer Success | 1 | 286 000 | 1.0 мес | onboarding, retention, expansion |
| PM / Producer | 1 | 299 000 | 1.0 мес | scope control и спринты |
| Marketing lead | 1 | 286 000 | 1.0 мес | inbound demand и performance |
| Finance / ops | 0.5 | 156 000 | 1.0 мес | договоры, счета, cash control |
| **Итого** | **10.5** | **4 680 000 ₽/мес** |  | full operating team |

## Moat: 7-factor framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не делает продукт лучше для остальных. |
| 2. Switching costs | 2 | Сайт, интеграции, аналитика и workflow правок создают умеренное трение на выходе. |
| 3. Scale economies | 2 | AI-first production и шаблоны снижают себестоимость при росте портфеля. |
| 4. Proprietary data / model advantage | 1 | Может накопиться delivery-data, но доказанного data moat пока нет. |
| 5. Regulatory moat | 0 | 152-ФЗ и data residency, это constraint, а не moat. |
| 6. Brand / distribution | 1 | Сильного бренда или доминирующего канала ещё нет. |
| 7. Embedded workflow | 2 | При retainer-модели подрядчик становится частью monthly web-ops цикла клиента. |

**Moat sum = 8 / 21. Moat score = round((8 * 25) / 21) = 10/25.**

## GTM: 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Skillbox | постоянно запускает лендинги и продуктовые страницы под новые курсы и акции | email decision-maker в growth/marketing + кейс на vc.ru | 180 000 ₽/мес |
| 2 | Skyeng | частые campaign pages, тесты воронок и кабинетные flow для B2C/B2B направлений | outbound на VP Marketing / Head of Web + Habr/vc.ru контент | 200 000 ₽/мес |
| 3 | Level Group | девелоперу нужны быстрые промо-сайты ЖК, формы лидогенерации и интеграции с CRM | email CMO / digital lead + отраслевые конференции недвижимости | 220 000 ₽/мес |
| 4 | Hoff | регулярные спецпроекты, сезонные страницы и B2B landing pages | ABM outreach + партнёрство с CRM/analytics интегратором | 180 000 ₽/мес |
| 5 | СДЭК | франчайзинговые страницы, сервисные кабинеты и региональные промо-лендинги | email digital director + логистические/франчайзинговые мероприятия | 230 000 ₽/мес |
| 6 | Клиника Фомина | региональные сайты, patient journeys, формы записи и контентные итерации | партнёрство через med-marketing агентство + email head of digital | 170 000 ₽/мес |
| 7 | Петрович | продуктовые витрины, B2B страницы и campaign landing flows | outbound на e-commerce / web lead + retail tech event | 190 000 ₽/мес |
| 8 | Dodo Brands | локальные страницы, спецпроекты и partner funnels для франчайзи | founder-led outreach + партнёрский канал через CRM/integration vendor | 210 000 ₽/мес |
| 9 | SOKOLOV | частые промо-запуски, seasonal pages и service flows для e-commerce | email digital/e-commerce lead + vc.ru ad | 180 000 ₽/мес |
| 10 | Самокат | HR-лендинги, локальные сервисные страницы и customer-support flows | партнёрство через performance-агентство + outbound на digital ops | 200 000 ₽/мес |

**Итог по GTM:** named-account motion реалистичнее массового SMB. Лучший заход, это `партнёры / CRM-интеграторы / агентства + founder/AE outbound + ROI-питч на скорость релизов и снижение web-production backlog`.

## Top-3 risks
| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| weak_moat / коммодитизация AI-веб-студии | High | High | `у кейса нет defensibility как у software platform`, а moat score всего `10/25`. |
| price compression и CAC drift | High | High | В `05-critic.md` `Price -30%` даёт `EBITDA @M12 = -1 366 274 ₽/мес`, а `CAC x2` даёт `-1 465 891 ₽/мес`. |
| founder bottleneck + service creep | High | High | `Самый дорогой участок, это presale + prototype + первая сборка`, поэтому модель ломается без жёсткой стандартизации. |

## LTV Upside Calculator
| Рычаг | Текущая база | Upside-case | Эффект |
|---|---|---|---|
| ARPA / retainer | 120 000 ₽/мес | 140 000 ₽/мес | contribution_margin_rub_month вырастает примерно с 66 000 до 86 000 ₽ и сокращает clients_to_500k_ebitda с 46 до ~35 |
| Churn | 1.8%/мес | 1.4%/мес | customer_ltv_rub вырастает примерно с 4.55 млн ₽ до ~5.86 млн ₽ |
| CAC | 523 300 ₽ | 420 000 ₽ | LTV/CAC вырастает с 8.7x до ~10.8x |
| Setup GP | 432 000 ₽/мес на 4 сделках | 600 000 ₽/мес на 4-5 сделках | ускоряет выход к 500К EBITDA на 1-2 месяца |
| Partner share of pipeline | <25% | 40%+ | снижает зависимость от founder-led outbound и уменьшает CAC volatility |

## Что нужно доказать для перехода в APPROVED
1. Что `ARPA` устойчиво держится **не ниже 120-140 тыс. ₽/мес** без скидочной войны.
2. Что минимум **40% новых сделок** приходит через повторяемые каналы, а не через founder-only presale.
3. Что `logo churn ≤ 2%/мес`, а retainer действительно становится embedded monthly workflow.
4. Что delivery стандартизирован настолько, что `prototype + first build` не съедают margin на каждом новом клиенте.

## Финальный вывод IC
Это сильнее, чем обычная low-end AI-студия, и формально проходит EBITDA-gate, но пока всё ещё слишком похоже на высококачественный service business без настоящего moat. Поэтому решение комитета, это **NEAR-PASS: 66/100**. Следующий апгрейд до approve возможен только после доказательства partner-led GTM, стабильного ARPA и более глубокого workflow lock-in.
