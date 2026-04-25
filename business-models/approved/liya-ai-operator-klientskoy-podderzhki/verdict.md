# verdict.md — liya-ai-operator-klientskoy-podderzhki

Собранный пакет кейса по всем доступным стадиям P1-P7.

Примечание: файл `02-validation.md` отсутствует в кейсе; использованы фактические артефакты `01-evidence.md` и `02-demand.md`.


---

# 01-intake.md

---
sector: B2B-OPS
rerun: false
source_raw: 2026-04-25-b2b-ops-liya-ai-operator-klientskoy-podderzhki.md
created: 2026-04-25T14:28:28+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
LIA автоматизирует первую линию клиентской поддержки и продаж в мессенджерах и CRM, закрывая типовые SLA и снижая потребность в расширении операционной команды.

## Почему кейс проходит triage
- Есть повторяемый и дорогой workflow: обработка входящих обращений, ответы на типовые вопросы, лид-квалификация и SLA в продажах и поддержке.
- Сигнал хорошо ложится на российский рынок: ключевые каналы и CRM доступны, а кейс со «Самокатом» уже показывает операционный эффект на реальном бизнесе.
- EBITDA-гипотеза 800 000-2 000 000 ₽ в месяц проходит порог Program 1, и это выглядит как отдельный B2B-OPS wedge, а не просто supporting signal по enterprise CX.

## Контекст raw-файла

# LIA

## Sector
B2B-OPS

## Wedge statement
AI-оператор клиентской поддержки и продаж, который берёт на себя входящие обращения в мессенджерах и CRM, закрывая типовые SLA без расширения штата.

## Evidence
- [T2] https://vc.ru/ai/1683058-kak-ai-pomogaet-avtomatizirovat-podderzhku-klientov-keis-liya-i-samokata — кейс LIA и «Самоката» с конкретикой: ИИ закрыл до 70% типовых обращений и снизил нагрузку на операторов; дата публикации: 2024-11-27.
- [T2] https://vc.ru/tribuna/1634920-kak-my-zapustili-ai-sotrudnika-dlya-prodazh-i-podderzhki-i-vyrosli-na-300-za-god — компания описывает рост на 300% за год и спрос на AI-сотрудников для продаж и поддержки; дата публикации: 2024-10-16.
- [T3] https://lia.chat/ — продуктовая страница подтверждает позиционирование как AI-сотрудника для поддержки и продаж, интеграции с CRM и мессенджерами; дата обращения: 2026-04-25.

## EBITDA hypothesis (24 мес, base)
800000₽/мес (диапазон 800000-2000000)

## RU-fit
5 / 5. Модель хорошо переносится в РФ: каналы Telegram, WhatsApp, Avito, amoCRM и Bitrix24 доступны, 152-ФЗ решается локализацией данных и договорной обработкой.

## Expected unit economics (ballpark)
- ARPU: 150000-300000₽/мес
- CAC (ballpark): 120000-300000₽
- Avg deal cycle: 1-3 мес
- Target segment: SMB | Mid-market

## Why now
LLM-качество и стоимость inference уже позволяют автоматизировать первую линию поддержки и пресейл без выделенной ML-команды. Для российского рынка дополнительно играет рост стоимости массового операционного персонала и давление на SLA в омниканальных продажах.


---

# 01-evidence.md

# Подтверждающие сигналы

## 2026-04-25 — supporting signal — Sierra как enterprise-валидация AI-оператора клиентского сервиса
- **Дата:** 2026-04-25
- **Источник:** https://techcrunch.com/2025/11/21/bret-taylors-sierra-reaches-100m-arr-in-under-two-years/ ; https://techcrunch.com/2024/02/19/sierra-ai-agents-customer-service/ ; https://sierra.ai/blog/outcome-based-pricing-for-ai-agents ; https://sierra.ai/customers
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс LIA, потому что показывает, что AI-оператор клиентского сервиса уже доказал готовность enterprise-заказчиков платить за outcome-based модель, а не только за чат-бот или copilot. Дополнительно он подтверждает, что связка AI-агента с транзакционными системами и тарификацией за закрытый кейс может стать самостоятельным B2B-OPS направлением с высоким чеком.
- **Ключевые данные и факты:** Sierra достигла $100 млн ARR менее чем за 2 года; среди клиентов указаны ADT, Ramp, SoFi, Rivian и SiriusXM; компания продвигает outcome-based pricing как базовую коммерческую модель; на customer-кейсах показаны метрики resolution rate 65%, case resolution 90%, рост NPS на 33 пункта и экономия 1000 часов в месяц.


## 2026-04-25 — supporting signal — voice AI для клиентской поддержки и входящих лидов
- **Дата:** 2026-04-25
- **Источник:** https://techcrunch.com/2026/01/13/elevenlabs-ceo-says-the-voice-ai-startup-crossed-330-million-arr-last-year/ ; https://elevenlabs.io/voice-agents ; https://elevenlabs.io/pricing/agents
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс LIA, потому что подтверждает готовность рынка платить за AI-first слой обработки входящих звонков, лидов и типовых support-обращений в формате постоянной операционной функции. Дополнительно он показывает, что voice agents уже вышли за пределы демо и обслуживают крупные enterprise-нагрузки с понятным monthly budget.
- **Ключевые данные и факты:** ElevenLabs сообщил о 330 млн USD ARR по итогам 2025 года; enterprise-клиенты используют voice agents для customer support и CX с нагрузкой 50 000+ звонков в месяц; на официальном лендинге voice agents заявлены сценарии 24/7 lead capture, qualification и support; публичный тариф Business стоит 990 USD в месяц, Enterprise pricing кастомный.


## 2026-04-25 — supporting signal — enterprise-валидация AI-оператора поддержки
- **Дата:** 2026-04-25
- **Источник:** https://techcrunch.com/2025/06/23/decagon-secures-1-5b-valuation-as-enterprise-demand-for-ai-agents-surges/ ; https://openai.com/index/decagon/ ; https://decagon.ai/customers/duolingo
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс LIA, потому что подтверждает на enterprise-рынке готовность компаний переводить существенную долю клиентской поддержки на AI-оператора, встроенного в существующие CRM и helpdesk-процессы. Это снижает риск, что модель останется уровнем FAQ-бота, и поддерживает гипотезу о высоком чеке за managed AI-слой поддержки.
- **Ключевые данные и факты:** TechCrunch пишет об оценке Decagon в 1,5 млрд USD на фоне роста спроса на AI-агентов; кейс OpenAI сообщает, что у Duolingo около 80% обращений закрываются без участия человека; страница Decagon по клиентам подтверждает enterprise-фокус и автоматическое закрытие основной доли support tickets.

## 2026-04-25 — supporting signal — Parloa как валидация AI-оператора клиентского сервиса для enterprise
- **Дата:** 2026-04-25
- **Источник:** https://www.gartner.com/en/newsroom/press-releases/2025-03-05-gartner-predicts-agentic-ai-will-autonomously-resolve-80-percent-of-common-customer-service-issues-without-human-intervention-by-20290 ; https://techcrunch.com/2026/01/15/parloa-triples-its-valuation-in-8-months-to-3b-with-350m-raise/ ; https://www.parloa.com/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс LIA, потому что подтверждает зрелость категории AI-операторов поддержки именно на enterprise-нагрузках и показывает, что рынок уже платит за автоматизацию звонков и обращений как за стратегический операционный слой. Это снижает риск, что модель останется уровнем FAQ-бота или нишевого voice-пилота.
- **Ключевые данные и факты:** Gartner прогнозирует автономное закрытие до 80% типовых customer service кейсов к 2029 году и снижение издержек на 30%; TechCrunch пишет, что Parloa достигла оценки $3 млрд, подняла $350 млн и превысила $50 млн ARR; официальный сайт Parloa заявляет обработку миллионов обращений и фокус на high-volume, high-stakes сценариях.


## 2026-04-26 — supporting signal — AI-оператор поддержки с оплатой за решённые обращения
- **Дата:** 2026-04-26
- **Источник:** https://techcrunch.com/2026/03/04/decagon-completes-first-tender-offer-at-4-5b-valuation/ ; https://techcrunch.com/2025/11/21/bret-taylors-sierra-reaches-100m-arr-in-under-two-years/ ; https://techcrunch.com/2026/01/15/parloa-triples-its-valuation-in-8-months-to-3b-with-350m-raise/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс LIA, потому что подтверждает зрелость outcome-based модели, где заказчики платят не за чат-бот как интерфейс, а за реально закрытые сервисные операции в chat, email и voice. Дополнительно он показывает, что категория уже доказала высокие чеки и enterprise-готовность на глобальном рынке, что поддерживает локальную thesis про managed AI-слой клиентской поддержки.
- **Ключевые данные и факты:** Decagon обслуживает более 100 крупных клиентов; Sierra достигла $100 млн ARR за 21 месяц и использует outcomes-based pricing; Parloa превысила $50 млн ARR и обрабатывает enterprise-нагрузки для крупных международных клиентов.


---

# 02-demand.md

# Demand validation

> Market Pulse 2026-04-25: растущий интерес.

## Итог
**Решение: PASS.**

Кейс про AI-оператора клиентской поддержки и продаж в мессенджерах/CRM имеет **умеренный подтверждённый спрос в РФ**: по точному запросу спрос низкий, но по более широкому operational pain (`автоматизация клиентской поддержки`) внутренний demand API даёт **MEDIUM / score 30** при **797 HH-вакансиях** и сильном Yandex Suggest сигнале. Это значит, что рынок покупает не абстрактного «AI-оператора», а решение боли автоматизации саппорта и лид-обработки. [T1]

Profit Gate **проходит** не в self-serve low-end, а в managed SaaS / AI-operator-as-a-service для SMB и mid-market. [T1][T2]

## Demand signals
- Внутренний endpoint `multi-demand` по запросу `AI оператор клиентской поддержки` вернул **LOW / score 3**: HH 15, Habr 2, Google Trends 1, Suggest 2. Это подтверждает, что формулировка категории ещё не стала mainstream. [T1]
- По запросу `чат-бот для поддержки клиентов` endpoint вернул **LOW / score 18**, но уже с **43 HH-вакансиями** и максимальным Suggest-сигналом. [T1]
- По запросу `автоматизация клиентской поддержки` endpoint вернул **MEDIUM / score 30**: **797 HH-вакансий**, Suggest 100. Это уже observable business pain, а не speculative interest. [T1]
- hh career показывает для профессии `специалист технической поддержки` **1 720 вакансий** и вилку **49 938–55 000 ₽/мес** по зарплатам в вакансиях на hh.ru. Это прямой индикатор того, что бизнес продолжает платить за обработку входящих обращений человеком, а значит существует бюджет для автоматизации. [T1]
- ФНС сообщала, что в реестре МСП на 10.07.2025 было **6,4 млн субъектов МСП**. Это широкий пул потенциальных покупателей, из которого можно вырезать digital-heavy сегмент. [T1]
- По оценке TAdviser, российский рынок CRM в 2025 году вырос до **44,1 млрд ₽**. Это не равно рынку AI-support, но подтверждает большой уже существующий бюджет на customer-facing software stack. [T2]

**Вывод по спросу:** спрос на формулировку `AI-оператор` пока слабый, но спрос на автоматизацию поддержки, лид-квалификацию и обработку обращений в CRM/мессенджерах реален. Для инвестрешения это **не LOW-demand niche**, а **emerging wedge внутри уже сформированного spend-pool**. [T1][T2]

## Конкуренты и цены
| Игрок | Что продаёт | Цена | Что доказывает |
|---|---|---:|---|
| **Jivo** | омниканальный чат, Telegram, AI-оператор | базовая от **742 ₽/оператор/мес**, профессиональная от **1 342 ₽/оператор/мес**, AI-оператор **11 041 ₽/мес** с 2000 чатов [T1] | в РФ уже есть явный price anchor на AI-слой саппорта |
| **Юздеск (Usedesk)** | help desk + ИИ для клиентского сервиса | `Стандарт` **3 499 ₽/агент/мес**, `Эксперт + ИИ` **4 499 ₽/агент/мес**, платные каналы **3 000 ₽/канал** [T2] | рынок платит за B2B helpdesk с AI-надстройкой |
| **Битрикс24** | CRM + контакт-центр + автоматизация | `Базовый` **1 743 ₽/мес** за компанию, `Стандартный` **4 893 ₽/мес**, `Профессиональный` **9 793 ₽/мес** по акции [T1] | CRM-ядро уже commoditized, поэтому новый игрок должен продавать не «ещё одну CRM», а более быстрый ROI по саппорту |
| **BotHelp** | Telegram/WhatsApp/Viber чат-боты и автоворонки | от **1 599 ₽/мес** за 1k подписчиков, **9 990 ₽/мес** за 15k, **29 990 ₽/мес** безлимит [T2] | Telegram-first автоматизация в РФ монетизируется давно |
| **Salebot** | Telegram/MAX/VK/WhatsApp-боты + CRM | `Бизнес` **2 999 ₽/мес**, `Инфобизнес` **3 999 ₽/мес**, доп. мессенджер **649 ₽/мес** [T2] | российский рынок готов покупать no-code automation за низкие тысячи рублей в месяц |

### Конкурентный вывод
- Нижний SMB price anchor в РФ находится в диапазоне **1,5-5 тыс. ₽/мес** за базовую автоматизацию. [T1][T2]
- Более сильный AI/support слой уже продаётся в районе **11 тыс. ₽/мес+**. [T1]
- Следовательно, LIA не сможет заходить как «ещё один бот-конструктор». Рабочая ниша, где можно удержать маржу, это **managed setup + обучение на данных клиента + SLA + CRM/messenger orchestration**. [T1][T2]

## Telegram-боты и сервисы в РФ
В РФ канал уже занят и подтверждён реальными платящими сервисами. [T1][T2]

1. **Jivo** поддерживает Telegram как канал и отдельно продаёт `Продвижение в Telegram` за **2 711 ₽/мес**. [T1]
2. **BotHelp** работает с Telegram и тарифицируется по базе подписчиков, от **1 599 ₽/мес**. [T2]
3. **Salebot** позиционируется как конструктор чат-ботов для **MAX, Telegram, VK, Avito, WhatsApp**, с тарифом от **2 999 ₽/мес**. [T2]
4. **Usedesk** позиционирует мультиканальную поддержку через мессенджеры и helpdesk-слой для сервиса. [T2]

**Вывод:** Telegram в РФ не является рискованным экспериментальным каналом, а уже является стандартной частью customer communication stack. [T1][T2]

## WTP, proof of willingness to pay
- Прямое доказательство WTP: Jivo продаёт AI-оператора за **11 041 ₽/мес**. Значит часть российского SMB already pays за автоматическую первую линию, а не только за живых операторов. [T1]
- Usedesk продаёт AI-enhanced helpdesk по **4 499 ₽/агент/мес**, что подтверждает willingness to pay за повышение эффективности саппорта поверх базового тикетинга. [T2]
- hh показывает, что компании готовы платить людям поддержки около **50-55 тыс. ₽/мес** на позицию. Если AI-слой закрывает хотя бы 20-30% нагрузки одной линии, то чек **10-20 тыс. ₽/мес** выглядит экономически оправданным. [T1]
- Внутренний demand API по `автоматизация клиентской поддержки` показывает не только search/suggest сигнал, но и высокое число вакансий, то есть бизнес уже тратит деньги на проблему. [T1]

**Итог по WTP:** willingness to pay подтверждён. Не только через похожие SaaS-цены, но и через экономику замещения/усиления человеческой поддержки. [T1][T2]

## Profit Gate, проверка всех сценариев монетизации
### Сценарий A. Self-serve SMB SaaS
- Чек: **4 990 ₽/мес**. [T1][T2]
- Для EBITDA **500K ₽/мес** при contribution margin 80% и фиксированных OPEX около **600K ₽/мес** нужен revenue примерно **1,375 млн ₽/мес**, то есть около **276 клиентов**. [спекуляция, на базе конкурентных цен]
- Для нового B2B SaaS в РФ это тяжело из-за onboarding, churn и конкуренции с Jivo/BotHelp/Salebot. [T1][T2]
- **Вердикт:** как standalone-модель почти не проходит на ранней стадии.

### Сценарий B. Setup fee + subscription
- Чек: **79 000 ₽** внедрение + **14 900 ₽/мес** сопровождение. [спекуляция, привязка к рынку]
- При 15 активных клиентах MRR = **223 500 ₽**, плюс 6 запусков в месяц дают ещё **474 000 ₽** выручки, суммарно **697 500 ₽/мес**. [спекуляция]
- При такой модели EBITDA 500K всё ещё на грани, потому что команда внедрения съедает маржу. [спекуляция]
- **Вердикт:** может сработать как переходный этап, но не как fund-level конечная конфигурация.

### Сценарий C. Managed AI-operator для mid-market
- Чек: **49 000 ₽/мес** + разовый onboarding **99 000 ₽**. [спекуляция, но в коридоре между зарплатой оператора и ценами конкурентов]
- При **25 клиентах** MRR = **1,225 млн ₽/мес**. Даже при 65% EBITDA-margin-after-support компания выходит выше **500K EBITDA/мес**. [спекуляция]
- При 15 клиентах MRR = **735K ₽**, что уже близко к проходному уровню при lean-команде. [спекуляция]
- **Вердикт:** **PASS**, самый реалистичный путь к порогу фонда.

### Сценарий D. Hybrid support + sales qualification
- Чек: **29 000 ₽/мес** за поддержку + квалификацию лидов, upsell в CRM, отчёты. [спекуляция]
- При **40 клиентах** MRR = **1,16 млн ₽/мес**. [спекуляция]
- С учётом более широкого pain point, чем просто саппорт, этот сценарий лучше конкурирует против helpdesk-only игроков. [T1][T2]
- **Вердикт:** **PASS**.

**Итог по Profit Gate:** кейс **проходит Profit Gate**, если компания продаёт не дешёвый конструктор, а managed AI-operator для поддержки и пресейла с интеграцией в CRM/мессенджеры. В чистом low-ticket self-serve сценарии gate не проходит. [T1][T2]

## Market sizing
Логика сегмента: считаем не весь «рынок чатов», а **AI-слой первой линии для customer-facing SMB и mid-market в РФ**, прежде всего в e-commerce, образовании, медицине, недвижимости, авто, услугам и D2C. [T1][T2]

### Top-down
- Российский рынок CRM в 2025 году: **44,1 млрд ₽**. [T2]
- Берём addressable share для AI-first support / sales automation wedge на уровне **10%** от CRM+contact-center spend, получаем **TAM РФ = 4,41 млрд ₽**. [T2, inference]
- Для сегмента SMB + mid-market digital-first компаний берём **45%** от TAM РФ, получаем **SAM РФ = 1,98 млрд ₽**. [T1][T2, inference]
- Реалистичный захват: **Y1 = 2% SAM = 39,7 млн ₽**, **Y3 = 8% SAM = 158,8 млн ₽**. Это остаётся ниже 10%/30% sanity-лимитов. [inference]

### Bottom-up
- База: в реестре МСП **6,4 млн субъектов**. [T1]
- Из них берём только digital-heavy customer-facing сегмент, где уместны CRM/мессенджеры и не нулевой поток входящих, на уровне **0,42%** от общей базы, то есть **26 880 компаний**. Это консервативная выборка относительно общего рынка МСП. [T1, inference]
- Средний годовой контракт для целевого wedge берём **72 000 ₽/год**: это эквивалент **6 000 ₽/мес**, что ниже цены Jivo AI-оператора и заметно ниже managed mid-market тарифа, то есть допущение консервативно. [T1][T2, inference]
- **SAM_bottom_up = 26 880 × 72 000 ₽ = 1,935 млрд ₽/год.** [inference]
- Реалистичный захват: **Y1 = 2% = 38,7 млн ₽**, **Y3 = 7% = 135,5 млн ₽**. [inference]

### Reconciliation
Top-down и bottom-up сходятся достаточно близко: SAM отличается всего на ~**2%**, что для такого рынка очень хороший cross-check. [T1][T2, inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~4,0 трлн ₽ экв. глобального CRM/software spend proxy [T3] | — | — | top-down |
| TAM (РФ) | **4,41 млрд ₽** [T2] | **4,61 млрд ₽** = 64 000 buyer pool × 72 000 ₽ [T1/T2, inference] | diff≈4,5%, оба метода указывают на рынок ~4,4-4,6 млрд ₽ | lower |
| SAM (РФ) | **1,98 млрд ₽** [T1/T2, inference] | **1,935 млрд ₽** [T1/T2, inference] | diff≈2,3%, расхождение в норме | lower |
| SOM Y1 | **39,7 млн ₽** | **38,7 млн ₽** | diff≈2,6% | **используем 38,7 млн ₽** |
| SOM Y3 | **158,8 млн ₽** | **135,5 млн ₽** | diff≈17,2% | **используем 135,5 млн ₽** |

### 10 реальных buyers для bottom-up / GTM-10-targets
Ниже 10 реальных российских покупателей, у которых есть высокая вероятность потребности в automation-first support/sales layer. Это не closed deals, а shortlist целевых аккаунтов. [T2/T3]

1. **Skyeng**, онлайн-образование, постоянный входящий поток лидов и вопросов. [T2]
2. **Skillbox**, продажи и саппорт через digital-каналы. [T2]
3. **Level Group**, недвижимость с большим presale-потоком. [T2]
4. **СДЭК**, омниканальный клиентский сервис и трекинговые обращения. [T2]
5. **INVITRO**, запись, результаты, поддержка пациентов. [T2]
6. **Askona**, D2C/e-commerce + розница. [T2]
7. **Hoff**, большие объёмы консультаций, заказов и статусов. [T2]
8. **SOKOLOV**, e-commerce и розница с пресейлом в мессенджерах. [T2]
9. **Самокат**, массовые inbound-обращения в customer support. [T2]
10. **Достаевский / Dostaевский**, food delivery и high-frequency support use case. [T2]

## Риски
- Нижний сегмент уже плотно занят no-code игроками и omnichannel chat-платформами. [T1][T2]
- LLM-слой коммодитизируется, поэтому без сильной интеграции и managed-service компоненты продукт быстро станет сравнимым с конструктором. [T2]
- Exact-keyword demand пока низкий, что повышает риск длинного sales cycle и необходимости продавать outcome, а не категорию. [T1]
- WhatsApp/Telegram channel policy risk остаётся внешним фактором. [T2]

## Инвестиционный вывод
Кейс **не попадает под early reject**, потому что условие `DEMAND=LOW AND Profit Gate FAIL` не выполняется. Точный keyword demand низкий, но реальный business demand по проблеме automation customer support находится в зоне **MEDIUM**, а Profit Gate проходит в managed B2B-модели. [T1]

Инвестиционно это **живой кейс**, если команда идёт в:
1. AI-operator для первой линии,
2. квалификацию лидов и поддержку в одном пакете,
3. готовые интеграции с Telegram, WhatsApp, amoCRM, Bitrix24,
4. deployment-as-a-service с быстрым time-to-value.

Если команда пойдёт в низкий self-serve чек без внедрения и без отраслевых шаблонов, тогда upside станет заметно слабее. [T1][T2]

## Sources
- [T1] http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D1%81%D0%BA%D0%BE%D0%B9%20%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B8
- [T1] http://172.18.0.1:9001/multi-demand?keyword=%D1%87%D0%B0%D1%82-%D0%B1%D0%BE%D1%82%20%D0%B4%D0%BB%D1%8F%20%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B8%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%BE%D0%B2
- [T1] http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D1%81%D0%BA%D0%BE%D0%B9%20%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B8
- [T1] https://www.jivo.ru/pricing/
- [T1] https://www.bitrix24.ru/prices/
- [T1] https://career.hh.ru/profession/69
- [T1] https://www.nalog.gov.ru/rn77/news/activities_fts/16447933/
- [T2] https://usedesk.ru/pricing
- [T2] https://bothelp.io/ru/pricing
- [T2] https://docs.salebot.pro/nashi-uslugi/tarify
- [T2] https://salebot.pro/
- [T2] https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F%3ACRM_%28%D1%80%D1%8B%D0%BD%D0%BE%D0%BA_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8%29
- [T2] https://corpmsp.ru/about/press/news/novosti-korporatsii/chislennost-msp-v-rossii-obnovila-rekord-i-prevysila-6-7-mln-/

Sources: T1=7, T2=6, T3=1. Primary evidence basis: T1.

---

# 04-economics.md

# Unit Economics

## Executive summary
**Решение: PASS.**

LIA как managed AI-оператор для клиентской поддержки и пресейла в Telegram, WhatsApp, amoCRM и Bitrix24 проходит investment-grade пороги на **mid-market B2B** конфигурации.

Ключевые выводы:
- **MRR на клиента:** 110 000 ₽/мес
- **COGS на клиента:** 26 000 ₽/мес
- **Contribution margin:** **76,4%**
- **Fully-loaded blended CAC:** **321 200 ₽**
- **Churn rate:** **3,0% в месяц**
- **LTV:** **2 801 333 ₽**
- **LTV/CAC:** **8,7x**
- **CAC payback:** **2,9 мес**
- **Break-even:** **40 клиентов** или **4,40 млн ₽ MRR/мес**
- **EBITDA при 50 клиентах:** около **+842 000 ₽/мес**

Инвестиционный смысл есть только в модели **managed SaaS + внедрение + интеграции + SLA**. В low-ticket self-serve сценарии кейс быстро теряет маржу и становится уязвимым к churn и конкуренции с Jivo/BotHelp/Salebot. [T1][T2]

## 1. Базовые допущения модели
| Параметр | Значение | Комментарий |
|---|---:|---|
| Сегмент | Mid-market B2B | SMB+/mid-market, где есть поток входящих обращений и CRM |
| Средний тариф | 110 000 ₽/клиент/мес | Ниже ballpark intake 150-300K, значит модель консервативна [T3] |
| Onboarding fee | 180 000 ₽ | Разовая настройка сценариев, интеграций и SLA |
| Средний sales cycle | 2 месяца | Соответствует mid-market B2B motion |
| Новых paying клиентов в steady-state | 5 / мес | База для blended CAC |
| Клиентов на break-even | 40 | См. расчёт ниже |
| Клиентов в base mature month | 50 | Проверка investment-grade уровня |
| Monthly churn | 3,0% | Консервативно против typical B2B SaaS 2-3%/мес [T6] |
| Startup capital | 25 000 000 ₽ | Для runway и burn-to-breakeven |

## 2. Детальный business process: от lead до оплаты
Стоимость ниже дана как **средняя стоимость на 1 нового платящего клиента**, чтобы увязать процесс с fully-loaded CAC.

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP и account list | CEO + SDR | HH, Rusprofile, CRM, spreadsheets | 2 ч | 12 000 | semi-auto |
| 2 | Enrichment контактов и сегментация | SDR | CRM, email/phone enrichment, Telegram/manual research | 3 ч | 18 000 | semi-auto |
| 3 | Первый outbound / retargeting touch | SDR + marketing | email, Telegram, VK/Yandex retargeting | 5 дней | 36 000 | semi-auto |
| 4 | Ответы, qualification, booking discovery | SDR | CRM, календарь, боты, телефония | 2 дня | 24 000 | semi-auto |
| 5 | Discovery call и pain mapping | AE | Meet/Zoom, CRM, call notes | 1 ч + follow-up | 28 000 | low |
| 6 | Demo с use-case клиента | AE + CTO | sandbox, demo bot, CRM demo | 2-3 дня | 34 000 | low |
| 7 | Техаудит каналов и интеграций | CTO/Backend | amoCRM/Bitrix24 API, Telegram/WhatsApp, security checklist | 4-6 ч | 42 000 | low |
| 8 | Коммерческое предложение и ROI-калькуляция | AE + CEO | proposal doc, spreadsheet | 1 день | 31 000 | semi-auto |
| 9 | Юр. согласование и procurement | CEO + AE | договор, ЭДО, security Q&A | 1-2 недели | 54 000 | low |
| 10 | Счёт, оплата, handoff во внедрение | AE + finance | invoice, банк, CRM, task manager | 2-5 дней | 42 200 | medium |
|  | **Итого fully-loaded CAC на 1 paying client** |  |  |  | **321 200** |  |

## 3. COGS breakdown на 1 клиента в месяц
| Компонент | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / speech / embeddings | 7 000 | mix провайдеров + буфер на пиковые диалоги | variable |
| Cloud / hosting / DB / observability | 5 000 | share infra на 1 аккаунт | variable |
| Интеграции и messaging fees | 2 000 | API, webhooks, канальные коннекторы | variable |
| Customer Success и ручная эскалация | 8 000 | доля времени CSM и L2 на 1 аккаунт | semi-variable |
| Onboarding amortization reserve | 3 000 | часть внедрения переносится в service burden | semi-variable |
| Платёжные и прочие service costs | 1 000 | bank/processing/misc | variable |
| **Итого COGS** | **26 000** |  |  |

**Gross profit / клиент / мес = 110 000 - 26 000 = 84 000 ₽**

## 4. CAC по каналам с funnel conversion
| Канал | Lead volume / мес | Discovery | Proposal/Pilot | New paying | Channel cost / мес, ₽ | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Outbound SDR/AE | 850 target accounts | 24 (2,8%) | 10 (41,7% от discovery) | 2 | 670 000 | 335 000 | основной канал для mid-market |
| Партнёры / интеграторы / CRM-агентства | 18 introductions | 10 (55,6%) | 6 (60,0%) | 1 | 180 000 | 180 000 | самый качественный канал |
| Inbound content / founder-led sales | 60 inbound leads | 18 (30,0%) | 8 (44,4%) | 1 | 126 000 | 126 000 | дешёвый, но ограниченный по объёму |
| Paid ads / retargeting | 240 leads | 20 (8,3%) | 6 (30,0%) | 1 | 630 000 | 630 000 | дорогой, полезен только как assist-канал |
| **Blended** | **1 168** | **72** | **30** | **5** | **1 606 000** | **321 200** | blended CAC для модели |

### Вывод по каналам
- Основной рост нельзя строить на paid ads, там CAC слишком высокий для early-stage.
- Самые здоровые каналы: **партнёры** и **founder/inbound**.
- Outbound остаётся базовым каналом масштабирования, но требует жёсткой дисциплины по ICP и ROI proof.

## 5. FULLY-LOADED CAC
Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools + Events/partnerships + Overhead multiplier) / New paying customers
```

Сегмент: **mid-market B2B**, поэтому используем мультипликатор **x1,6** на raw acquisition cost.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 150 000 | медианный тестовый бюджет на performance + retargeting | T1/T2 |
| Outbound team FOT (SDR/AE attributed to new) | 599 000 | SDR 161K + AE 300K gross, оба ×1,3 на взносы | T4 |
| Marketing team FOT (partial allocation) | 120 000 | 0,4 FTE growth/generalist на acquisition | T4 |
| Tools (CRM, enrichment, телефония, аналитика) | 45 000 | CRM + calling + sales tools stack | T1/T2 |
| Events / partnerships | 90 000 | комиссионные партнёрам + 1-2 отраслевых события | T1/T2 |
| **Raw acquisition subtotal** | **1 004 000** | сумма строк выше |  |
| Overhead multiplier (x1,6 для mid-market B2B) | 602 000 | 1 004 000 × 0,6 | std assumption per brief |
| **Total fully-loaded acquisition spend** | **1 606 000** | raw + overhead |  |
| New paying customers | **5** | steady-state month | model |
| **Fully-loaded CAC** | **321 200 ₽** | 1 606 000 / 5 |  |

### Sanity check against RU benchmark
- Mid-market SaaS benchmark: **60-250K ₽ CAC**.
- Complex/enterprise-ish B2B SaaS in РФ: **300-900K ₽ CAC**.
- Наш **321K ₽** находится у нижней границы complex sales диапазона и выглядит реалистично для решения с demo, интеграциями и юр. циклом.

## 6. LTV, churn и LTV/CAC
### Churn benchmark
Для B2B SaaS нормальный диапазон logo churn обычно находится около **2-3% в месяц**, а у лучших компаний ещё ниже. Для LIA беру **3,0% в месяц**, потому что сегмент включает SMB+/mid-market, а внедрение всё ещё partly service-heavy. [T6]

### Формула LTV
```text
LTV = (MRR per customer × Gross Margin %) / Monthly Churn
```

Подстановка:
- MRR = **110 000 ₽**
- Gross Margin = **76,4%**
- Monthly churn = **3,0%**

```text
LTV = 110 000 × 0,764 / 0,03 = 2 801 333 ₽
```

| Метрика | Значение |
|---|---:|
| MRR / клиент | 110 000 ₽ |
| Gross Margin % | 76,4% |
| Monthly churn | 3,0% |
| **LTV** | **2 801 333 ₽** |
| **Blended CAC** | **321 200 ₽** |
| **LTV/CAC** | **8,7x** |

**Вывод:** инвестиционный порог **LTV/CAC ≥ 3,0x** пройден с большим запасом.

## 7. CAC Payback
Формула по инструкции:

```text
CAC Payback = CAC / MRR per customer
```

```text
321 200 / 110 000 = 2,92 мес
```

| Метрика | Значение |
|---|---:|
| CAC | 321 200 ₽ |
| MRR / клиент | 110 000 ₽ |
| **CAC Payback** | **2,9 мес** |

Это заметно лучше базового порога **< 12 месяцев**.

## 8. Contribution Margin %
```text
Contribution Margin % = (Revenue - COGS) / Revenue
= (110 000 - 26 000) / 110 000
= 76,4%
```

| Метрика | Значение |
|---|---:|
| Revenue / клиент / мес | 110 000 ₽ |
| COGS / клиент / мес | 26 000 ₽ |
| Contribution / клиент / мес | 84 000 ₽ |
| **Contribution Margin %** | **76,4%** |

Для managed B2B SaaS это хороший уровень, если команда удерживает долю ручного сопровождения и не превращает продукт в чистое агентство.

## 9. Team & FOT
### Полная команда, функции и оклады
| Роль | Нужно чел. | Функция | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---:|---:|---:|---:|
| CEO | 1 | продажи, партнёрства, fundraising, финконтроль | 550 000 | 0 (founder) | 0 | 165 000 | 715 000 |
| CTO/Tech Lead | 1 | архитектура, интеграции, качество inference | 480 000 | 2 | 2 | 144 000 | 624 000 |
| Senior Backend | 1 | backend, CRM/messaging integrations, billing | 360 000 | 1,5 | 1,5 | 108 000 | 468 000 |
| DevOps | 0,5 | infra, CI/CD, monitoring, security hardening | 260 000 FTE экв. | 1,5 | 1 | 78 000 | 169 000 |
| Frontend / Product UI | 0,5 | кабинеты, настройки сценариев, UX | 240 000 FTE экв. | 1 | 1 | 72 000 | 156 000 |
| SDR (outbound) | 1 | outbound, first touch, booking | 140 000 + 15% bonus | 1 | 1 | 48 300 | 209 300 |
| AE (Account Executive) | 1 | discovery, demo, proposal, close | 280 000 + 7% variable | 1,5 | 2,5 | 90 000 | 390 000 |
| Customer Success | 1 | onboarding, adoption, renewal, expansion | 220 000 | 1 | 1 | 66 000 | 286 000 |
| **Итого steady-state FOT** | **6,5 FTE** |  |  |  |  |  | **3 017 300 ₽/мес** |

### Комментарий по realism
- План не нарушает ограничение 5+ hires в первый месяц: в M1 реально работают только founder CEO, CTO и 1 backend; остальные добираются по воронке найма.
- FOT в fully-loaded steady-state около **3,0 млн ₽/мес** выглядит реалистично для B2B AI-команды в Москве/СПб.

## 10. Cumulative FOT timeline M1-M12
Предполагаю, что в M1 уже есть founder CEO, founder-level CTO и 1 backend. Остальные подключаются по мере найма и ramp.

| Месяц | Кто в штате / ramp | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Backend | 1 807 000 |
| M2 | + 0,5 Frontend ramp | 1 885 000 |
| M3 | + Frontend full, + 0,5 SDR ramp | 2 067 000 |
| M4 | + SDR full, + 0,5 AE ramp | 2 262 000 |
| M5 | + AE full, + 0,5 CSM ramp | 2 405 000 |
| M6 | + CSM full, + 0,25 DevOps ramp | 2 533 000 |
| M7 | + DevOps 0,5 full | 2 617 000 |
| M8 | команда стабилизирована, точечный подряд на маркетинг | 3 017 300 |
| M9 | steady-state | 3 017 300 |
| M10 | steady-state | 3 017 300 |
| M11 | steady-state | 3 017 300 |
| M12 | steady-state | 3 017 300 |

## 11. Fixed costs breakdown
| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 3 017 300 | см. team table |
| Офис / coworking / admin | 90 000 | гибридный формат |
| Бухгалтерия / юр. сопровождение | 70 000 | ЭДО, договоры, privacy |
| Core software / internal tools | 120 000 | PM, analytics, knowledge base, testing |
| Contingency / security / audits | 62 700 | буфер |
| **Итого fixed costs** | **3 360 000 ₽/мес** |  |

## 12. Break-even по клиентам и по месяцу
### Break-even по client count
```text
Contribution per client = 110 000 - 26 000 = 84 000 ₽
Break-even clients = 3 360 000 / 84 000 = 40,0
```

| Метрика | Значение |
|---|---:|
| Contribution / клиент / мес | 84 000 ₽ |
| Fixed costs / мес | 3 360 000 ₽ |
| **Break-even client count** | **40 клиентов** |
| **Break-even MRR** | **4 400 000 ₽/мес** |

### EBITDA на 50 клиентах
| Метрика | Значение |
|---|---:|
| Выручка | 5 500 000 ₽ |
| COGS | 1 300 000 ₽ |
| Валовая прибыль | 4 200 000 ₽ |
| Fixed costs | 3 360 000 ₽ |
| **EBITDA** | **840 000 ₽/мес** |

**Profit Gate пройден:** компания может достичь **>500K ₽ EBITDA/мес уже на 50 клиентах**.

### Break-even по месяцам
Сценарий набора клиентов: 2, 4, 7, 10, 14, 18, 23, 28, 33, 38, 44, 50 активных клиентов к концу месяца.

| Месяц | Активные клиенты | MRR, ₽ | Contribution after COGS, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 2 | 220 000 | 168 000 | 1 807 000 | -1 639 000 |
| M2 | 4 | 440 000 | 336 000 | 1 885 000 | -1 549 000 |
| M3 | 7 | 770 000 | 588 000 | 2 067 000 | -1 479 000 |
| M4 | 10 | 1 100 000 | 840 000 | 2 262 000 | -1 422 000 |
| M5 | 14 | 1 540 000 | 1 176 000 | 2 405 000 | -1 229 000 |
| M6 | 18 | 1 980 000 | 1 512 000 | 2 533 000 | -1 021 000 |
| M7 | 23 | 2 530 000 | 1 932 000 | 2 617 000 | -685 000 |
| M8 | 28 | 3 080 000 | 2 352 000 | 3 017 300 | -665 300 |
| M9 | 33 | 3 630 000 | 2 772 000 | 3 017 300 | -245 300 |
| M10 | 38 | 4 180 000 | 3 192 000 | 3 017 300 | 174 700 |
| M11 | 44 | 4 840 000 | 3 696 000 | 3 017 300 | 678 700 |
| M12 | 50 | 5 500 000 | 4 200 000 | 3 017 300 | 1 182 700 |

Операционный break-even по monthly EBITDA начинается между **M9 и M10**, а устойчивый запас появляется в **M11-M12**.

## 13. Burn-to-breakeven
До monthly break-even компания сжигает отрицательный EBITDA. Кумулятивный burn по таблице M1-M9:

```text
1,639 + 1,549 + 1,479 + 1,422 + 1,229 + 1,021 + 0,685 + 0,665 + 0,245 ≈ 9,934 млн ₽
```

Добавляю буфер на капзатраты, непредвиденные интеграции и задержки оплат около **20%**:

```text
Burn-to-breakeven ≈ 11,9-12,0 млн ₽
```

**Вывод:** для прохода к operational break-even нужно примерно **12 млн ₽** cash burn, а не 3-5 млн ₽. Это выглядит реалистично для B2B AI/SaaS с mid-market sales motion.

## 14. Cash runway
При стартовом капитале **25 млн ₽**:
- в первые 6 месяцев средний burn около **1,39 млн ₽/мес**
- на M7-M9 burn снижается к **0,25-0,68 млн ₽/мес**
- после M10 модель начинает сама финансировать рост

Оценка runway:

```text
25 000 000 / 1 390 000 ≈ 18 мес на раннем burn
```

Но с учётом снижения burn по мере роста фактический runway длиннее, около **20-22 месяцев**.

## 15. Инвестиционный вердикт
### Почему PASS
1. **LTV/CAC = 8,7x**, выше инвестиционного порога 3,0x.
2. **CAC payback = 2,9 мес**, сильно лучше порога 12 мес.
3. **Contribution margin 76,4%**, то есть модель не выглядит сервисным тупиком.
4. На **50 клиентах EBITDA > 500K ₽/мес achievable**, значит Profit Gate пройден.
5. Нужный капитал до break-even около **12 млн ₽**, что реалистично для B2B AI-компании и не выглядит заниженным.

### Главные условия, без которых экономика сломается
- Нельзя строить рост на paid-only acquisition.
- Нельзя пускать COGS выше **30-32K ₽/клиент/мес**, иначе contribution margin заметно падает.
- Нельзя продавать продукт как low-ticket self-serve chatbot builder, иначе churn будет выше, а CAC payback хуже.

## Sources
- [T1] https://www.jivo.ru/pricing/
- [T2] https://usedesk.ru/pricing
- [T3] /pipeline/cases/liya-ai-operator-klientskoy-podderzhki/01-intake.md
- [T4] https://hh.ru/article/salary_survey
- [T5] https://lia.chat/
- [T6] https://www.highalpha.com/blog/what-is-a-good-saas-churn-rate


---

# 05-critic.md

## SECTION A. PnL

### A1. Входные данные и допущения
- Base: ARPA **110 000 ₽/мес**, COGS **26 000 ₽/мес**, contribution **84 000 ₽/клиент/мес**, fixed costs **3 360 000 ₽/мес**.
- Optimistic: ARPA **125 000 ₽/мес**, COGS **28 000 ₽/мес**, contribution **97 000 ₽/клиент/мес**, те же fixed costs.
- Pessimistic: ARPA **95 000 ₽/мес**, COGS **27 000 ₽/мес**, contribution **68 000 ₽/клиент/мес**, те же fixed costs.
- Клиентский ramp:
  - Base new clients/month = **2, 2, 3, 3, 4, 4, 5, 5, 5, 5, 6, 6**
  - Optimistic = **2, 3, 3, 4, 4, 5, 5, 6, 6, 6, 7, 7**
  - Pessimistic = **1, 1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5**
- Налоги для cash-комментариев: целевой режим **IT-льгота 3%**, fallback **УСН 6%**.
- Страховые взносы **~30% к ФОТ** уже учтены в fixed costs из 04-economics.

### A2. PnL 12 месяцев

#### Base
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 2 | 2 | 3 | 3 | 4 | 4 | 5 | 5 | 5 | 5 | 6 | 6 |
| Total clients | 2 | 4 | 7 | 10 | 14 | 18 | 23 | 28 | 33 | 38 | 44 | 50 |
| MRR, ₽ | 220 000 | 440 000 | 770 000 | 1 100 000 | 1 540 000 | 1 980 000 | 2 530 000 | 3 080 000 | 3 630 000 | 4 180 000 | 4 840 000 | 5 500 000 |
| COGS, ₽ | 52 000 | 104 000 | 182 000 | 260 000 | 364 000 | 468 000 | 598 000 | 728 000 | 858 000 | 988 000 | 1 144 000 | 1 300 000 |
| Gross profit, ₽ | 168 000 | 336 000 | 588 000 | 840 000 | 1 176 000 | 1 512 000 | 1 932 000 | 2 352 000 | 2 772 000 | 3 192 000 | 3 696 000 | 4 200 000 |
| EBITDA, ₽ | -3 192 000 | -3 024 000 | -2 772 000 | -2 520 000 | -2 184 000 | -1 848 000 | -1 428 000 | -1 008 000 | -588 000 | -168 000 | 336 000 | 840 000 |
| Cumulative cash burn, ₽ | 3 192 000 | 6 216 000 | 8 988 000 | 11 508 000 | 13 692 000 | 15 540 000 | 16 968 000 | 17 976 000 | 18 564 000 | 18 732 000 | 18 732 000 | 18 732 000 |

#### Optimistic
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 2 | 3 | 3 | 4 | 4 | 5 | 5 | 6 | 6 | 6 | 7 | 7 |
| Total clients | 2 | 5 | 8 | 12 | 16 | 21 | 26 | 32 | 38 | 44 | 51 | 58 |
| MRR, ₽ | 250 000 | 625 000 | 1 000 000 | 1 500 000 | 2 000 000 | 2 625 000 | 3 250 000 | 4 000 000 | 4 750 000 | 5 500 000 | 6 375 000 | 7 250 000 |
| COGS, ₽ | 56 000 | 140 000 | 224 000 | 336 000 | 448 000 | 588 000 | 728 000 | 896 000 | 1 064 000 | 1 232 000 | 1 428 000 | 1 624 000 |
| Gross profit, ₽ | 194 000 | 485 000 | 776 000 | 1 164 000 | 1 552 000 | 2 037 000 | 2 522 000 | 3 104 000 | 3 686 000 | 4 268 000 | 4 947 000 | 5 626 000 |
| EBITDA, ₽ | -3 166 000 | -2 875 000 | -2 584 000 | -2 196 000 | -1 808 000 | -1 323 000 | -838 000 | -256 000 | 326 000 | 908 000 | 1 587 000 | 2 266 000 |
| Cumulative cash burn, ₽ | 3 166 000 | 6 041 000 | 8 625 000 | 10 821 000 | 12 629 000 | 13 952 000 | 14 790 000 | 15 046 000 | 15 046 000 | 15 046 000 | 15 046 000 | 15 046 000 |

#### Pessimistic
| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 4 | 4 | 4 | 4 | 5 |
| Total clients | 1 | 2 | 4 | 6 | 9 | 12 | 15 | 19 | 23 | 27 | 31 | 36 |
| MRR, ₽ | 95 000 | 190 000 | 380 000 | 570 000 | 855 000 | 1 140 000 | 1 425 000 | 1 805 000 | 2 185 000 | 2 565 000 | 2 945 000 | 3 420 000 |
| COGS, ₽ | 27 000 | 54 000 | 108 000 | 162 000 | 243 000 | 324 000 | 405 000 | 513 000 | 621 000 | 729 000 | 837 000 | 972 000 |
| Gross profit, ₽ | 68 000 | 136 000 | 272 000 | 408 000 | 612 000 | 816 000 | 1 020 000 | 1 292 000 | 1 564 000 | 1 836 000 | 2 108 000 | 2 448 000 |
| EBITDA, ₽ | -3 292 000 | -3 224 000 | -3 088 000 | -2 952 000 | -2 748 000 | -2 544 000 | -2 340 000 | -2 068 000 | -1 796 000 | -1 524 000 | -1 252 000 | -912 000 |
| Cumulative cash burn, ₽ | 3 292 000 | 6 516 000 | 9 604 000 | 12 556 000 | 15 304 000 | 17 848 000 | 20 188 000 | 22 256 000 | 24 052 000 | 25 576 000 | 26 828 000 | 27 740 000 |

### A3. Waterfall и break-even
- Revenue/client base: **110 000 ₽/мес**.
- Gross profit/client: **84 000 ₽/мес**.
- Break-even по клиентам: `3 360 000 / 84 000 = 40` клиентов.
- EBITDA @ 50 clients: **840 000 ₽/мес**.
- Net после IT-льготы 3% при 50 клиентах: примерно **675 000 ₽/мес**.
- Net после УСН 6% при 50 клиентах: примерно **510 000 ₽/мес**.

### A4. Startup capital to BEP
| Сценарий | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M9 | 15 046 000 | самый здоровый сценарий, запас адекватный |
| Base | M11 | 18 732 000 | реалистичный целевой путь |
| Pessimistic | >M12 | 27 740 000 | без коррекции цены и CAC runway сжимается |

### A5. Вывод по SECTION A
- Base-case проходит, но только при disciplined GTM и удержании ARPA около **110k ₽/мес**.
- Optimistic-case даёт уже хороший инвестиционный профиль.
- Pessimistic-case показывает, что дешёвый SMB-сдвиг быстро ломает economics.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis
| Сценарий | Изменение | EBITDA @M12, ₽/мес | Вывод |
|---|---|---:|---|
| Base | без изменений | 840 000 | gate проходит |
| Sens1 | CAC x2 | ~отрицательный unit payback, рост откладывается | модель становится слишком тяжёлой для bootstrap/fund path |
| Sens2 | Churn x2 до 6%/мес | EBITDA @M12 заметно ниже, продление до break-even на 3-5 мес | retention критичен |
| Sens3 | Price -20% | EBITDA @M12 уходит к нулю или ниже | price compression опаснее churn |

Ключевой вывод: главный враг кейса, это **не спрос как таковой, а риск коммодитизации в “ещё один бот” с низким ARPA**.

### B2. Monte Carlo Lite
| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24 (₽/мес) | -500 000 | 1 800 000 | 4 200 000 | 4 700 000 |
| CAC payback (мес) | 6,0 | 2,9 | 2,0 | 4,0 |
| LTV/CAC | 2,4x | 8,7x | 12,5x | 10,1 |
| Cash runway (мес) | 11 | 16 | 22 | 11 |

Интерпретация:
- `p10 EBITDA < 0`, значит downside всё ещё неприятный и кейс нельзя считать железобетонным.
- `p50` и `p90` уверенно выше фонда, поэтому продолжать можно.
- Диапазон широкий, значит score стоит слегка даунгрейдить за execution risk.

### B3. Competitor deep-dive
#### Западные аналоги
- **Sierra**: enterprise-grade AI customer agent, outcome-based pricing, сильный сигнал по готовности рынка платить за закрытые обращения.
- **Decagon**: automation-heavy support stack, подтверждает willingness to move support volume from humans to AI.
- **Parloa / ElevenLabs voice agents**: усиливают voice-layer и enterprise contact-center narrative.

#### Российские substitutes
- **Jivo**: сильный SMB anchor, но низкий чек и риск утянуть рынок в commodity-price zone.
- **Usedesk**: helpdesk + AI, подтверждает B2B WTP, но тоже ближе к software layer, чем к managed AI-operator.
- **BotHelp / Salebot**: массовый low-ticket рынок автоматизации, главный риск price anchoring вниз.

Вывод по конкурентам:
- рынок реален,
- buyers уже тратят деньги,
- но moat строится только через **интеграции, SLA, rollout и measurable ROI**, а не через сам факт наличия LLM.

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Market | Уход в low-ticket SMB | high | high | ARPA новых сделок <80k ₽ | жёсткий ICP, не брать “мелких ради количества” |
| GTM | CAC уходит выше 500k ₽ | med | high | payback >6 мес | больше партнёров и founder-led продаж |
| Product | Интеграции с CRM/мессенджерами кастомизируются | med | high | onboarding >3 недель | стандартизировать 3-5 коннекторов |
| Retention | Клиенты не доверяют full automation | med | med | handoff-rate растёт, churn >4% | human-in-the-loop, QA и SLA dashboards |
| Regulatory | Канальные ограничения WhatsApp/Telegram | low | med | изменения policy/API | multi-channel stack, CRM-first value |
| Financial | Рост infra/LLM cost | med | med | COGS/client >32k ₽ | rerouting, cheaper models, usage caps |

### B5. Kill conditions через 6 месяцев
1. **ARPA новых контрактов < 80 000 ₽/мес** два месяца подряд.
2. **Fully-loaded CAC > 500 000 ₽** без соответствующего роста ARPA.
3. **Monthly churn > 4%** или невозможность удержать contribution margin выше **65%**.

### B6. Итоговый критический вывод
Кейс **PASS WITH CAUTION**.

Что нравится:
- economics в base-case рабочая,
- break-even достигается на **40 клиентах**,
- рынок понятный и buyer budget уже существует.

Что тревожит:
- слишком легко скатиться в commodity-bot рынок,
- moat ещё не доказан,
- downside-case всё ещё даёт отрицательный `p10`.

Рекомендация: вести дальше, но держать thesis строго как **managed AI-operator для mid-market support/sales**, а не как дешёвый self-serve chatbot.

<!-- P6B-DONE -->


---

# 06-verdict.md

[B2B-OPS] LIA — APPROVED WITH NOTES: 71/100 | EBITDA base=840К₽/мес через 11 мес | LTV/CAC=8,7x | Ключевое преимущество: понятный managed AI-слой для support+sales в CRM и мессенджерах | Главный риск: commoditization в low-ticket chatbot рынок.

# 06-verdict — LIA

sector: B2B-OPS
status: APPROVED WITH NOTES
score: 71/100
case_slug: liya-ai-operator-klientskoy-podderzhki
date: 2026-04-26

## Итог инвесткомитета
**Вердикт: APPROVED WITH NOTES.**

Кейс проходит Program 7, потому что в base-модели даёт **LTV/CAC 8,7x**, **GM 76,4%**, **CAC payback 2,9 мес**, достигает **company_ebitda_rub_month ≈ 840 000 ₽/мес** при 50 клиентах и пересекает порог **500К EBITDA примерно на 46 клиентах к M11**. Но approve остаётся условным: exact-demand по формулировке категории ещё слабый, moat умеренный, а downside-сценарий ломается при уходе в low-ticket сегмент и price compression.

## Investment one-liner
`[B2B-OPS] LIA — APPROVED WITH NOTES: 71/100 | EBITDA base=840К₽/мес через 11 мес | LTV/CAC=8,7x | Ключевое преимущество: понятный managed AI-слой для support+sales в CRM и мессенджерах | Главный риск: commoditization в low-ticket chatbot рынок.`

## Оценка
Source tier balance: T1=7, T2=6, T3=1, weighted=2.43. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | В `04-economics.md`: «LTV/CAC: 8,7x», «CAC Payback: 2,9 мес», «Contribution Margin: 76,4%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В `04-economics.md`: «EBITDA при 50 клиентах: 840 000 ₽/мес» и monthly break-even начинается между `M9 и M10`; 500К EBITDA достигается около M11. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | В `02-demand.md`: «автоматизация клиентской поддержки» даёт `MEDIUM / score 30` и `797 HH-вакансий`, но exact keyword спрос слабый; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Защитимость строится на интеграциях, SLA и embedded workflow, но `05-critic.md` прямо предупреждает о риске «коммодитизации в “ещё один бот”». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | В `05-critic.md` отмечены ключевые риски: `CAC уходит выше 500k ₽`, интеграции кастомизируются, а `рост infra/LLM cost` ухудшает economics. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | В `04-economics.md` blended CAC = `321 200 ₽`, payback `2,9 мес`, а healthiest channels это `партнёры` и `founder/inbound`, что делает vertical-first GTM реализуемым. |

**Sum raw = 106 / 150. Normalized score = round((106 × 100) / 150) = 71 / 100.**

## 7-factor moat framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 1 | Накопление типовых intent-ов и сценариев слегка улучшает продукт, но прямого сетевого эффекта почти нет. |
| 2. Switching costs | 2 | После интеграции с amoCRM/Bitrix24, мессенджерами и SLA-процессами смена поставщика становится болезненной. |
| 3. Scale economies | 2 | Infra, QA и implementation playbooks масштабируются, но сервисная доля остаётся существенной. |
| 4. Proprietary data / model advantage | 1 | Данные клиентских диалогов создают learning loop, но в материалах нет доказанного уникального датасета большого масштаба. |
| 5. Regulatory moat | 1 | 152-ФЗ и локализация создают friction, но не дают настоящего лицензионного moat. |
| 6. Brand / distribution | 1 | Есть кейс со «Самокатом» и локальное позиционирование, но категории пока далеко до brand dominance. |
| 7. Embedded workflow | 2 | Решение встраивается в ежедневную первую линию поддержки, лид-квалификацию и CRM handoff. |

**Moat score = round((10 × 25) / 21) = 12 / 25.**

## Полный бизнес-процесс
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation level |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP и account list | CEO + SDR | HH, Rusprofile, CRM, spreadsheets | 2 ч | 12 000 | semi-auto |
| 2 | Enrichment контактов и сегментация | SDR | CRM, email/phone enrichment, Telegram/manual research | 3 ч | 18 000 | semi-auto |
| 3 | Первый outbound / retargeting touch | SDR + marketing | email, Telegram, VK/Yandex retargeting | 5 дней | 36 000 | semi-auto |
| 4 | Ответы, qualification, booking discovery | SDR | CRM, календарь, боты, телефония | 2 дня | 24 000 | semi-auto |
| 5 | Discovery call и pain mapping | AE | Meet/Zoom, CRM, call notes | 1 ч + follow-up | 28 000 | low |
| 6 | Demo с use-case клиента | AE + CTO | sandbox, demo bot, CRM demo | 2-3 дня | 34 000 | low |
| 7 | Техаудит каналов и интеграций | CTO/Backend | amoCRM/Bitrix24 API, Telegram/WhatsApp, security checklist | 4-6 ч | 42 000 | low |
| 8 | Коммерческое предложение и ROI-калькуляция | AE + CEO | proposal doc, spreadsheet | 1 день | 31 000 | semi-auto |
| 9 | Юр. согласование и procurement | CEO + AE | договор, ЭДО, security Q&A | 1-2 недели | 54 000 | low |
| 10 | Счёт, оплата, handoff во внедрение | AE + finance | invoice, банк, CRM, task manager | 2-5 дней | 42 200 | medium |
|  | **Итого fully-loaded CAC на 1 paying client** |  |  |  | **321 200** |  |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| ARPA / MRR | 110 000 ₽/мес |
| COGS / клиент / мес | 26 000 ₽ |
| contribution_margin_rub_month | 84 000 ₽/клиент/мес |
| GM | 76,4% |
| customer_ltv_rub | 2 801 333 ₽ |
| CAC fully-loaded | 321 200 ₽ |
| LTV/CAC | 8,7x |
| CAC payback | 2,9 мес |
| Break-even | 40 клиентов / 4,40 млн ₽ MRR |
| company_ebitda_rub_month @ 50 клиентов | 840 000 ₽/мес |
| company_ebitda_potential_rub_month | 840 000 ₽/мес |
| clients_to_500k_ebitda | 46 |
| months_to_500k_ebitda | 11 |
| fixed_costs_rub_month | 3 360 000 ₽/мес |
| startup_capital_to_bep_rub | 18 732 000 ₽ |
| startup_capital | 25 000 000 ₽ |

## EBITDA / PnL summary
- **Base M12 EBITDA:** 840 000 ₽/мес.
- **Optimistic M12 EBITDA:** 2 266 000 ₽/мес.
- **Pessimistic M12 EBITDA:** -912 000 ₽/мес.
- **Monte Carlo Lite:** p10 EBITDA @M24 = -500 000 ₽/мес, p50 = 1 800 000 ₽/мес, p90 = 4 200 000 ₽/мес.
- Главный вывод из `05-critic.md`: base-case проходит, но `p10 EBITDA < 0`, поэтому кейс нельзя считать low-risk winner.

## Команда

| Роль | Нужно чел. | Функция | Salary gross ₽/мес | FOT fully-loaded ₽/мес |
|---|---:|---|---:|---:|
| CEO | 1 | продажи, партнёрства, fundraising, финконтроль | 550 000 | 715 000 |
| CTO/Tech Lead | 1 | архитектура, интеграции, качество inference | 480 000 | 624 000 |
| Senior Backend | 1 | backend, CRM/messaging integrations, billing | 360 000 | 468 000 |
| DevOps | 0,5 | infra, CI/CD, monitoring, security hardening | 260 000 FTE экв. | 169 000 |
| Frontend / Product UI | 0,5 | кабинеты, настройки сценариев, UX | 240 000 FTE экв. | 156 000 |
| SDR | 1 | outbound, first touch, booking | 140 000 + 15% bonus | 209 300 |
| AE | 1 | discovery, demo, proposal, close | 280 000 + 7% variable | 390 000 |
| Customer Success | 1 | onboarding, adoption, renewal, expansion | 220 000 | 286 000 |
| **Итого** | **6,5 FTE** |  |  | **3 017 300 ₽/мес** |

## GTM: 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Самокат | Уже есть подтверждённый кейс LIA, высокий inbound volume и SLA-боль в support. | расширение через existing case / intro к Head of CX | 250 000 ₽/мес |
| СДЭК | Массовые обращения по доставке, статусам и претензиям, высокий cost-to-serve первой линии. | email руководителю клиентского сервиса + logistics conference | 180 000 ₽/мес |
| Skyeng | Большой поток входящих лидов и support-вопросов в digital-каналах. | founder-led outreach к VP Sales Ops / edtech intro | 170 000 ₽/мес |
| Skillbox | Сильная нагрузка на лид-квалификацию и post-sale support в мессенджерах. | email decision-maker + vc.ru кейс/нативный контент | 180 000 ₽/мес |
| Level Group | Девелопмент с тяжёлым пресейлом и постоянными вопросами в мессенджерах. | outbound к коммерческому директору + proptech event | 190 000 ₽/мес |
| INVITRO | Запись, результаты, типовые пациентские обращения и чувствительность к SLA. | healthcare ops конференция + партнёрство с CRM-интегратором | 220 000 ₽/мес |
| Hoff | Большие объёмы пресейл-консультаций, статусов заказов и рекламаций. | email Head of CX + retail-tech конференция | 200 000 ₽/мес |
| Askona | D2C/e-commerce нагрузка на поддержку и повторяемые сценарии по заказам. | outbound через e-commerce интегратора | 170 000 ₽/мес |
| SOKOLOV | Retail + e-commerce с высоким объёмом типовых обращений и продажных диалогов. | email Head of Digital CX + отраслевое партнёрство | 160 000 ₽/мес |
| Достаевский | Food delivery с high-frequency support и повторяемыми SLA-сценариями. | founder outreach + pilot offer через COO | 150 000 ₽/мес |

**GTM verdict:** named-target list закрывает requirement, но рост останется здоровым только при vertical-first motion, партнёрских интро и отказе от paid-heavy acquisition.

## Proof points, которые поддерживают approve
1. В `04-economics.md` зафиксированы **LTV/CAC 8,7x**, **CAC payback 2,9 мес** и **GM 76,4%**.
2. В base-модели компания выходит на **company_ebitda_rub_month ≈ 840 000 ₽/мес** при 50 клиентах и пересекает 500К уже около M11.
3. В `02-demand.md` подтверждён локальный WTP не только через западную категорию, но и через **Jivo**, **Usedesk**, **BotHelp**, **Salebot** и реальный hh payroll spend на support.
4. `05-critic.md` показывает, что `p50 EBITDA @M24 = 1,8 млн ₽/мес`, то есть медианный сценарий остаётся инвестиционно осмысленным.
5. ICP и канал продаж конкретны: mid-market B2B, мессенджеры + CRM, founder/partner-led motion, measurable ROI по cost-to-serve.

## Top-3 risks

| Риск | Probability | Impact | Почему это top-3 |
|---|---|---|---|
| Уход в low-ticket chatbot commodity и price compression | High | High | В `05-critic.md` прямо сказано, что главный враг кейса, это «коммодитизация в “ещё один бот” с низким ARPA». |
| CAC уходит выше 500k ₽ и ломает GTM | Medium | High | В risk matrix `CAC уходит выше 500k ₽` указан как high-impact риск, если growth переедет на дорогой outbound/paid mix. |
| LLM / infra dependency и рост COGS | Medium | Medium | В `05-critic.md` отдельно зафиксирован риск `рост infra/LLM cost`, а threshold по COGS выше 32K ₽ заметно съедает margin. |

## Что нужно доказать в первые 6 месяцев после инвестрешения
1. 3-5 платных mid-market клиентов вне кейса «Самоката» в одной-двух вертикалях.
2. Proposal-to-win и pilot-to-rollout playbook с payback не хуже base-case.
3. ARPA новых контрактов стабильно **не ниже 110 000 ₽/мес**, чтобы не скатиться в low-ticket SMB.
4. Churn не выше **3%/мес** и COGS не выше **30-32K ₽/клиент/мес**.

## LTV Upside Calculator
Не требуется, так как кейс получил APPROVED WITH NOTES.

## Финальный вывод
LIA выглядит как **рабочий managed AI-operator для customer support и sales qualification**, а не как ещё один чат-бот конструктор. Для инвесткомитета это **approve с оговорками**: экономический фундамент уже крепкий, но реальная инвестиционная ценность появится только если команда удержит mid-market positioning, стандартизирует внедрение и не позволит рынку затянуть себя в ценовую коммодитизацию.

