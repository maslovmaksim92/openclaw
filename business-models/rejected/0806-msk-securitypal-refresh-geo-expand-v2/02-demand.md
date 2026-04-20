---
stage: demand-validation
case: 0806-msk-securitypal-refresh-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
0806 MSK SecurityPal Refresh GEO Expand, AI-native customer assurance слой для автоматизации security questionnaires, trust center и vendor security review у B2B software и enterprise-tech компаний.

## Итог
**Статус: CONDITIONAL PASS**

По exact-keyword search-demand в РФ спрос почти отсутствует, но money demand подтверждён: компании уже тратят деньги на trust center, questionnaire automation и response tooling, потому что security review реально тормозит enterprise sales. SecurityPal добавляет к этому не только software, но и human-in-the-loop execution, что делает кейс чуть шире, чем просто trust portal.

При этом overlap с Conveyor и другими trust workflow платформами высокий. Поэтому это не clean PASS, а **CONDITIONAL PASS**: standalone wedge выглядит коммерчески валидным, но в следующих этапах нужно проверить, достаточно ли он отдельный от общего customer trust workflow.

## 1. Demand data
Источник exact-check: `http://172.18.0.1:9001/multi-demand?keyword=security%20questionnaire%20automation`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Дополнительные смежные проверки:

### `trust center software`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `vendor security review automation`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **1**
- Habr articles: **2**
- hh.ru vacancies: **1**
- Yandex suggest: **2**

### `security review automation`
- Composite demand: **LOW**
- Demand score: **7**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **102**
- Yandex suggest: **2**

### Интерпретация
В РФ категория почти не существует как массовый поисковый запрос. Но это не consumer-style рынок. Pain возникает внутри enterprise sales, infosec и GRC, когда security review задерживает закрытие сделки. Сильный сигнал здесь не search volume, а наличие repeatable workflow и готовности компаний платить за ускорение due diligence.

## 2. Реальные конкуренты и ценовые якоря

| Конкурент | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| SecurityPal | Trust Center + Questionnaire Concierge + CAx platform | **Trust Center free**, premium tiers через sales-led motion | Есть самостоятельный wedge: trust layer + managed AI/human execution |
| Conveyor | Trust center + questionnaire automation + RFP automation | **Professional от $9,600 в год** | Прямой ценовой якорь для trust workflow категории |
| SafeBase | Trust Center + AI Questionnaire Assistance | **Foundation free**, Advanced/Enterprise custom | Категория trust center уже стала отдельным software budget |
| Loopio | RFP / security questionnaire response automation | **от $20,000 в год** | Смежный response workflow уже покупается как дорогой B2B stack |

### Вывод по конкурентному полю
- Клиенты уже платят за ускорение security review и response workflows.
- SecurityPal отличается от чистого portal-SaaS тем, что продаёт **AI + analyst execution**, а не только витрину документов.
- Это усиливает тезис о standalone wedge, но одновременно показывает сильное пересечение с уже открытым кейсом customer trust workflow.

## 3. Российский контур и substitutes
Прямого локального category leader в РФ по trust center / customer assurance почти не видно, но substitutes понятны:
- ручная работа security и compliance команд,
- Excel/Docs-анкеты и data room,
- sales engineering / presales команды,
- внешние консалтинг и compliance-подрядчики,
- глобальные trust/compliance платформы.

### Вывод
Для demand-stage это означает, что покупка вероятнее всего идёт не из новой budget line, а как ROI-layer поверх уже существующих расходов на enterprise sales, infosec и GRC. Это валидирует спрос, но ослабляет аргумент, что кейс полностью отдельный от Conveyor-like customer trust workflow.

## 4. TAM / SAM / SOM в рублях

### Базовые допущения
- Беру midpoint чека: **250 000 ₽/мес** = **3 000 000 ₽/год** на клиента.
- Это ниже агрессивной enterprise-гипотезы по Conveyor, потому что у SecurityPal trust center имеет бесплатный вход и часть value может съедаться services-heavy delivery.
- ICP, это B2B software, fintech, AI vendors, cloud/platform companies и enterprise suppliers, которые регулярно проходят security questionnaires в сделках.

### TAM
Беру **4 000** потенциально релевантных аккаунтов в РФ и русскоязычном контуре.

**TAM = 4 000 × 3 000 000 ₽ = 12 млрд ₽/год**

### SAM
Реально адресуемый слой для первого GTM, это компании с enterprise deal motion, англоязычными/международными клиентами и регулярным потоком security reviews.

Беру **700** компаний.

**SAM = 700 × 3 000 000 ₽ = 2,1 млрд ₽/год**

### SOM
Ранний реалистичный слой: **15 контрактов**.

**SOM = 15 × 3 000 000 ₽ = 45 млн ₽/год**

### Вывод по рынку
Рынок узкий, но не микроскопический. При нормальном GTM и сильной delivery-модели кейс может дойти до meaningful выручки, хотя масштаб сильно зависит от того, продаётся ли продукт как software-first или как managed assurance service.

## 5. WTP, доказательства готовности платить
1. **SecurityPal Trust Center** официально продвигается как отдельный продукт с бесплатным входом и обещанием сократить входящий поток security questionnaires на **60%** и сэкономить **1-2 недели** на review cycle.
2. **SecurityPal Questionnaire Concierge** заявляет **менее 12 часов turnaround**, около **2 млн отвеченных вопросов** и **150+ certified analysts**. Это важный сигнал, что покупают не только софт, но и outcome.
3. В анонсе **20 сентября 2022 года** SecurityPal сообщил о **$21 млн Series A** и назвал себя partner for hundreds of enterprises. Это подтверждает инвестиционную и коммерческую валидность категории.
4. **Conveyor** публично продаёт category-adjacent продукт от **$9,600 в год**.
5. **Loopio** продаёт response automation от **$20,000 в год**, включая security questionnaires.
6. **SafeBase** подтверждает, что trust center и AI questionnaire assistance уже покупаются как отдельный stack, начиная с free entry и дальше через sales-led expansion.

### Вывод по WTP
**WTP подтверждён условно.**

Покупатели готовы платить за ускорение security review и снижение presales-friction. Но есть и обратный сигнал: free tiers у SecurityPal и SafeBase означают, что trust center сам по себе может коммодитизироваться. Значит premium economics нужно защищать либо concierge execution, либо аналитикой, либо глубокой интеграцией в revenue workflow.

## 6. Profit Gate
Нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Lean managed layer
- Цена: **150 000 ₽/мес**
- GM: **55%**
- Валовая прибыль на клиента: **82 500 ₽/мес**
- Для fixed costs **1,8 млн ₽/мес** нужно **28 клиентов**

**Вердикт: STRETCH**

### Сценарий B. Base-case customer assurance retainer
- Цена: **250 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **150 000 ₽/мес**
- Нужно **16 клиентов**

**Вердикт: PASS**

### Сценарий C. Enterprise premium concierge
- Цена: **400 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **260 000 ₽/мес**
- Нужно **9 клиентов**

**Вердикт: PASS**

### Вывод по Profit Gate
Кейс проходит profit gate только если удаётся продавать не бесплатный trust center, а premium concierge / managed assurance motion. Если delivery слишком services-heavy и чек опускается к нижней границе, экономика быстро становится натянутой.

## 7. Общий вывод
- Search demand: **LOW**
- Adjacent enterprise workflow demand: **есть**
- Публичные ценовые якоря: **есть**
- WTP: **подтверждён условно**
- Standalone wedge: **есть, но с высоким overlap к Conveyor-like category**
- Profit Gate: **проходит в base и premium сценариях**

## 8. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс стоит двигать дальше в economics, потому что:
1. pain коммерчески реален;
2. глобальный category spend подтверждён;
3. SecurityPal показывает отдельный managed wedge поверх trust center;
4. путь к EBITDA выше 500 000 ₽/мес существует.

Но в P5/P6/P7 нужно особенно жёстко проверить:
- не является ли это просто вариантом уже существующего кейса Conveyor;
- сколько ручного analyst load скрыто в модели;
- можно ли удерживать premium pricing после free-entry trust center.

## Market Pulse
Market Pulse 20.04.2026: нишевый, но коммерчески валидированный интерес.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=security%20questionnaire%20automation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=trust%20center%20software
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=vendor%20security%20review%20automation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=security%20review%20automation
- SecurityPal Trust Center: https://www.securitypalhq.com/products/trust-center
- SecurityPal Free Trust Center: https://www.securitypalhq.com/free-trust-center
- SecurityPal Questionnaire Concierge: https://www.securitypalhq.com/solutions/questionnaire-concierge
- SecurityPal Series A announcement, 2022-09-20: https://www.prnewswire.com/news-releases/securitypal-emerges-from-stealth-with-21m-to-end-the-dreaded-security-review-301627541.html
- Conveyor pricing: https://www.conveyor.com/pricing
- SafeBase pricing: https://safebase.io/pricing
- Loopio pricing: https://loopio.com/pricing/

- Market Pulse 2026-04-20: растущий интерес.
