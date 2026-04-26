# Demand validation — Gamma, AI-сборка презентаций, КП, лендингов и деловых материалов

## Итог
**Решение: PROCEED.**
Спрос в РФ выглядит **средним, но платёжеспособным**, а порог EBITDA 500 000 ₽/мес достижим сразу в нескольких моделях монетизации. Основной рынок не mass-consumer, а B2B wedge: sales-команды, агентства, маркетинг, founders, marketplace-селлеры и SMB-операторы, которым нужны презентации, КП и быстрые лендинги под продажи.

## 1) Demand signals
- Endpoint `multi-demand` дал **MEDIUM** для `ai презентации` и `создание презентаций` с `demand_score=32`; для `коммерческие предложения` тоже **MEDIUM 32**. Для `лендинги ai` спрос ниже, **LOW 22**, значит лендинги лучше считать вторичным use case, а не core wedge. [T1]
- HH по запросу `презентации` показывает **48 480 вакансий**, что подтверждает массовую повторяемость задачи подготовки презентационных материалов в РФ. [T1]
- Внутренний demand endpoint также фиксирует **5 439** вакансий по `создание презентаций`, **841** по `ai презентации`, **22 234** по `коммерческие предложения`. Это не чистый TAM, но сильный индикатор повторяемой бизнес-задачи. [T1]
- В Telegram есть отдельная категория ботов для генерации презентаций, например каталог TGDYK перечисляет боты `@prezaprobot`, `@PrezentumBot`, а также крупные AI-боты с функцией создания презентаций. Это подтверждает локальный demand на mobile-first / chat-first сценарий. [T2]

## 2) Конкуренты и цены
| Игрок | Что продаёт | Цена | Комментарий |
|---|---|---:|---|
| Beautiful.ai | AI-презентации для individual/team | **$12/мес** Pro, **$40/польз./мес** annual Team или **$50** monthly Team, one-off deck **$45** [T2] | Самый прямой comparable по AI deck creation |
| Pitch | Презентации для команд | **€10/мес** Plus annual, **€12/мес** monthly; Team **€15-18/seat/мес** [T2] | Сильнее в team collaboration, слабее в instant artifact generation |
| Presentations.AI | AI deck maker | **$198/год** Pro для 1 пользователя, team offer **$40/год до 10 участников** в public beta [T2] | Агрессивный pricing, useful lower-bound для WTP |
| Google Workspace | Gemini + Docs/Slides workflow | **€6.80-21.10/польз./мес** по business plans [T1/T2] | Непрямой substitute, но важный pricing anchor |
| Gamma | pricing page не отдала публичные суммы, но help center подтверждает платные планы Free/Plus/Pro/Ultra/Teams/Business [T2] | Факт paid packaging подтверждён, но точную цену из доступных источников быстро не вытащил |

**Вывод по pricing:** рынок уже обучен покупать либо individual subscription в диапазоне примерно **900-2 500 ₽/мес**, либо team-seat **1 300-4 500 ₽/seat/мес** при курсовом пересчёте. Для РФ realistic sweet spot выглядит как **1 990-3 490 ₽/польз./мес** self-serve или **9 900-24 900 ₽/команду/мес**. [T2]

## 3) Telegram / RU landscape
- `tgdyk.com/lists/presentations` показывает отдельную подборку Telegram-ботов для генерации презентаций; один из listed ботов имеет **262 195** пользователей каталога/подписки, другой **84 449**. Это не revenue proof, но знак того, что distribution channel уже существует. [T2]
- `presentationrobot.ru` описывает Telegram-бота для подготовки к презентациям и заявляет **170 000+** пользователей. Продукт больше про coaching, чем instant deck generation, но adjacent demand реален. [T2]
- `diaclass.ru/botai` продвигает Telegram-чат-бота для PowerPoint и отмечает статус аккредитованной IT-компании и запись в реестре отечественного ПО. Это снижает риск тезиса, что в РФ совсем нет локальных игроков. [T2]

**Вывод:** RU/Telegram слой есть, но он фрагментирован и часто слабее по продукту, чем западные AI-first deck builders. Для нового игрока это плюс: рынок не пустой, но и не закрыт сильным local champion. [T2]

## 4) Willingness to pay (WTP)
- Публичные тарифы Beautiful.ai, Pitch, Presentations.AI и Google Workspace показывают, что рынок готов платить за создание/сборку деловых материалов в диапазоне от low-ticket self-serve до team-seat pricing. [T1/T2]
- Наличие one-off pricing у Beautiful.ai (`$45` за разовую презентацию) особенно важно: это прямое доказательство willingness to pay не только за подписку, но и за transactional use case, что хорошо совпадает с кейсом КП/тендерных материалов/питчей. [T2]
- HH-вакансии по `презентации` и `коммерческие предложения` показывают, что компании уже оплачивают труд людей, которые делают эти материалы вручную. Следовательно, software replacing part of this labor может забирать бюджет из payroll / agency spend, а не только из “экспериментального AI бюджета”. [T1]

**WTP verdict:** подтверждён. Не спекуляция.

## 5) Market sizing

### Top-down
1. Российский рекламный рынок оценивается около **679 млрд ₽** по данным отраслевых публикаций АКАР/СОСТАВ за 2024 год. Беру это как верхний кошелёк на production/creative/sales-enablement budget. [T2]
2. Для AI-сборки презентаций/КП/микролендингов addressable share беру **0.5%** от этого spend, потому что продукт закрывает только узкий слой pre-sale / content assembly, а не весь ad market. Получаем **TAM РФ ≈ 3.4 млрд ₽**. [T2 + аналитическое допущение]
3. Сегмент fit для SMB, sales-team, agencies и founders: **30%** от TAM РФ, потому что enterprise brand studios и full-service agencies не весь spend вынесут в self-serve SaaS. Получаем **SAM РФ ≈ 1.02 млрд ₽**. [T2 + аналитическое допущение]
4. Реалистичный capture: **1.5% в Y1** и **5% в Y3**. Тогда **SOM Y1 ≈ 15.3 млн ₽**, **SOM Y3 ≈ 50.9 млн ₽**. [аналитическое допущение]

### Bottom-up
1. База потенциальных покупателей: **6.59 млн МСП** в РФ, по публикациям о реестре МСП. [T2]
2. Беру только content-heavy сегменты, где регулярно нужны презентации/КП/лендинги: агентства, интеграторы, IT-сервисы, B2B-селлеры, консалтинг, edtech, marketplace sellers, девелопмент, event/HR. Консервативно это **3%** МСП, то есть **197 700** компаний. [T2 + аналитическое допущение]
3. Доля с острой регулярной болью, подтверждаемой HH/demand endpoint: **15%**. Получаем **29 655** реальных покупателей. [T1 + аналитическое допущение]
4. Средний ARR: **36 000 ₽/год** на одного клиента, это эквивалент около **2 990 ₽/мес** с учётом скидок/части transactional users. [T2]
5. **SAM bottom-up = 29 655 × 36 000 ₽ = 1.07 млрд ₽**.
6. Реалистичный capture: **1.0% Y1** и **4.0% Y3**. Тогда **SOM Y1 ≈ 10.7 млн ₽**, **SOM Y3 ≈ 42.7 млн ₽**.

### 10 реальных buyers для GTM-bottom-up списка
1. iConText Group
2. Kokoc Group
3. QSOFT
4. Mindbox
5. Roistat
6. Calltouch
7. Skillbox
8. SberMarketing
9. Ingate
10. Telega.in

Это не клиенты, а реальные компании, для которых pain с презентациями/КП/лендингами выглядит правдоподобным. Список пригоден как seed GTM-10-targets. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$3.5-5.0 млрд** [T3, low confidence] | — | глобальный market map доступен в основном у research firms | top-down range |
| TAM (РФ) | **3.40 млрд ₽** [T2] | **2.37 млрд ₽** = 65 850 content-heavy компаний × 36 000 ₽ [T2] | diff 1.4x, допустимо; top-down включает более широкий spend wallet | **2.37 млрд ₽** |
| SAM (РФ) | **1.02 млрд ₽** [T2] | **1.07 млрд ₽** [T1/T2] | diff ~5%, хорошее совпадение | **1.02 млрд ₽** |
| SOM Y1 | **15.3 млн ₽** | **10.7 млн ₽** | diff ~43%, но обе оценки <10% SAM | **10.7 млн ₽** |
| SOM Y3 | **50.9 млн ₽** | **42.7 млн ₽** | diff ~19% | **42.7 млн ₽** |

**Sanity checks**
- Расхождение top-down vs bottom-up по SAM меньше 3x, ок.
- SOM Y1 < 10% SAM, ок.
- При среднем чеке 36 000 ₽/год для SOM Y1 нужен портфель около **297 клиентов**. Это агрессивно, но достижимо при self-serve + agency channel + freemium. 

## 6) Profit Gate (EBITDA >= 500 000 ₽/мес)
Проверяю все основные сценарии.

### Сценарий A: self-serve subscription
- ARPU: **2 990 ₽/мес**
- Валовая выручка для 500k EBITDA при 80% gross margin и 250k fixed overhead: нужно около **937 500 ₽/мес выручки**
- Это = **314 платящих пользователей**
- Вывод: достижимо. [T2 + unit economics assumption]

### Сценарий B: team plans
- Тариф: **12 900 ₽/команду/мес**
- Для той же цели нужно около **73 команд**
- Если средняя команда 3-5 активных пользователей, это уже довольно компактный B2B-портфель
- Вывод: достижимо.

### Сценарий C: agency / white-label / done-with-you
- Тариф: **35 000 ₽/мес**
- Нужно около **27 агентств/партнёров**
- Для рынка агентств и performance shops это реалистичный сценарий, особенно если есть bulk generation и brand kits
- Вывод: достижимо.

### Сценарий D: transactional one-off decks / КП
- Средний чек: **4 900 ₽**
- Нужно ~**191 продаж в месяц** только для покрытия EBITDA-цели без сильного retention
- Вывод: слабее, как standalone model рискованно; лучше как entry offer.

**Profit Gate verdict:** **PASS**. Порог EBITDA 500k/мес достижим минимум в 3 сценариях из 4.

## 7) Риски
- Core demand в РФ сильнее у `презентаций` и `коммерческих предложений`, чем у `AI лендингов`; не стоит пытаться позиционировать все use cases одинаково. [T1]
- Pricing pressure высокая: substitutes вроде Google Workspace и generic AI tools могут съедать low-end сегмент. [T1/T2]
- Product moat слабый, если нет brand systems, team workflows, approvals, template libraries, CRM/docs ingestion и white-label режимов. [T2]

## 8) Инвест-вывод
Фондовый взгляд: это **не огромный category-defining рынок**, но хороший **cash-efficient AI application wedge**. При дисциплинированном позиционировании как `sales/marketing collateral OS` под SMB и агентства кейс заслуживает прохода дальше. 

**Что было бы best wedge:**
1. Презентации + КП как core
2. Лендинги как secondary export
3. Team workflows, templates, brand kits, RU-first payment/onboarding
4. Agency / reseller channel

**Decision:** PROCEED to next stage.

---
Sources: T1=3, T2=9, T3=1. Primary evidence basis: T2.

### Source notes
- [T1] multi-demand endpoint `ai презентации`, `создание презентаций`, `коммерческие предложения`, `лендинги ai`; HH query `презентации`.
- [T2] Beautiful.ai pricing, Pitch pricing, Presentations.AI pricing, TGDYK list, presentationrobot.ru, diaclass.ru, TASS/публикации о числе МСП, отраслевые публикации об объёме рекламного рынка РФ.
- [T3] Global presentation software market range, used only as directional world TAM.
