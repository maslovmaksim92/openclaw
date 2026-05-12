# verdict.md
case_slug: ai-native-claims-ops-dlya-strahovshchikov
status: rejected
result: NEAR-PASS
score: 65/100
sector: FINTECH
updated_at: 2026-05-12T17:00:00+03:00

---

# FILE: 01-intake.md

---
sector: FINTECH
rerun: false
source_raw: 20260511-1031-msk-fintech-reserv-ai-native-claims-ops.md
created: 2026-05-11T12:22:00+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
Reserv проходит triage как самостоятельный FINTECH-кейс: AI-native платформа и операционный слой для урегулирования страховых убытков, где объём ручного труда, стоимость ошибки и enterprise-LTV делают категорию привлекательной для отдельного запуска.

## Почему кейс проходит triage
- Это не общий AI для страхования, а узкий claims ops wedge с повторяющимся дорогим workflow и понятным buyer внутри страховщика или claims-оператора.
- Есть сильная рыночная валидация: у Reserv 100+ клиентов и масштаб порядка 100 млн $ ARR, что подтверждает зрелость категории и высокую готовность платить.
- Для РФ сценарий адаптируем через AI-first back-office для урегулирования, документооборота и маршрутизации кейсов без обязательной зависимости от тяжёлого enterprise-SI на старте.

## Контекст raw-файла

name: Reserv
source: https://fintech.global/2026/05/04/reserv-raises-125m-series-c-led-by-kkr/ (2026-05-04); https://www.finsmes.com/2025/06/reserv-raises-25m-in-series-b-funding.html (2025-06-04)
ltv_signal: консервативно 60 000 000+ ₽ в год на клиента. Оценка: при 100+ клиентах и 100 млн $ ARR средний годовой контракт порядка 1 млн $, то есть около 80 млн ₽; для сигнала беру дисконт до 60 млн ₽.
why it matters: Это не разовый аутсорс, а AI-native claims ops платформа с уже подтверждённым масштабом enterprise-выручки. Компания дошла до 100 млн $ ARR и работает с 100+ страховщиками, MGA и self-insured клиентами, значит модель проходит profit gate с огромным запасом: даже 10 клиентов такого уровня дают company EBITDA сильно выше 500 000 ₽ в месяц. Для РФ это сильный сигнал на запуск AI-first оператора урегулирования убытков и страхового бэк-офиса без зависимости от тяжёлого SI-внедрения.

---

# FILE: 02-demand.md

---
sector: FINTECH-INSURANCE
stage: demand-validation
updated: 2026-05-11T13:27:00+03:00
composite_demand: LOW
profit_gate: PASS
verdict: PROCEED
---

# 02-demand — Demand Validation

## 1. Что валидируем
Проверяем, есть ли в РФ платёжеспособный спрос на **AI-native claims ops для страховщиков**: не просто чат-бот или co-pilot, а внешний AI-оператор / software-enabled service для FNOL, triage, document intake, fraud pre-check, routing и части back-office урегулирования. [T1][T2]

## 2. Demand verdict в 1 строку
**Спрос как поисковая категория в РФ слабый, но бюджет как enterprise pain реален.** Multi-demand API дал `LOW` и 0 вакансий по точному phrasing, однако у рынка есть крупная база страховых премий и убытков, публичные бюджеты на автоматизацию клиентского сервиса, а также готовность платить за сокращение ручного claims headcount и SLA в урегулировании. Поэтому кейс **не уходит в early reject**, а проходит дальше как enterprise wedge с узким ICP. [T1][T2][API][inference]

## 3. Ключевые сигналы спроса
1. Российский страховой рынок в 2024 году вырос до **3,7 трлн ₽ премий**, выплаты составили **2,1 трлн ₽**. Это достаточно большой денежный поток, чтобы внутри него существовал отдельный бюджетный слой на автоматизацию урегулирования. Источник: обзор Банка России. [T1] https://www.cbr.ru/Collection/Collection/File/55129/review_insure_24.pdf
2. На глобальном рынке category proof уже есть: рынок claims management software оценивается примерно в **$4,25 млрд в 2024** с ростом к 2032. Это не доказывает локальный спрос само по себе, но показывает, что покупают именно отдельный software layer вокруг claims operations. [T2] https://www.fortunebusinessinsights.com/claims-management-software-market-112799
3. По данным Swiss Re sigma, **глобальные non-life premiums составили около $4,0 трлн в 2023 году**. Это даёт рабочий benchmark software-spend-to-premium ratio для top-down расчёта адресуемого слоя. [T2] https://www.swissre.com/institute/research/sigma-research/sigma-2024-04.html
4. Demand API по запросу `AI claims ops для страховщиков` вернул `LOW`, score 0, HH=0, Habr=2, Yandex suggest=2. Это означает, что **категория не формулируется рынком явно**, и вход через «AI claims ops» как message-market fit в РФ будет слабым. [API]
5. При этом сам pain уже бюджетирован. Страховщики массово тратят деньги на контакт-центры, обработку документов, речевую аналитику, OCR, антифрод и workflow automation, то есть продавать можно не «AI вообще», а reduction of claim handling cost / time-to-resolution / leakage. [T1][T2][inference]

## 4. Реальные конкуренты с ценами
Ниже не идеальные product twins, а **реальные ближайшие substitutes/competitors** в РФ-контуре, через которые заказчик уже сегодня решает куски claims ops.

1. **CraftTalk**, AI-боты и омниканальная поддержка. Публичный прайс: **от 59 000 ₽/мес** за Start, **159 000 ₽/мес** за Pro, Enterprise по запросу. Это сильный substitute для intake/status/support-части claims journey. [T2] https://crafttalk.ru/pricing
2. **Naumen Contact Center SaaS**. Публичный тариф на сайте начинается **от 2 000 ₽/мес** за базовый облачный контакт-центр, далее enterprise upsell и кастомный объём. Для страховщика это не full claims ops, но реальный baseline-конкурент за бюджет линии обращения/маршрутизации. [T2] https://www.naumen.ru/products/contact-center/services/cloud/contact-center/
3. **T-Bank VoiceKit / речевые API**. Публичные цены: примерно **0,72 ₽/мин** за streaming STT, **0,58 ₽/мин** за batch STT, **820 ₽ за 1 млн символов** синтеза. Это substitute на слой voice intake / transcription и снижает moat у простого voice-first решения. [T2] https://developer.tbank.ru/docs/products/voicekit/pricing

### Вывод по конкурентам
Уже существующие российские игроки показывают, что покупатель **привык платить** как минимум за три вещи: входящий омниканал, AI-боты, распознавание речи/документов. Значит, новый игрок должен продавать не «ещё один бот», а **claims outcome layer** поверх этих кирпичей. [T2][inference]

## 5. Telegram в РФ: есть ли канал / продуктовый слой
1. В РФ есть готовые платформы, которые поддерживают Telegram как канал обслуживания: CraftTalk и другие bot-platform игроки прямо заявляют интеграции с мессенджерами. Это означает, что Telegram можно использовать как дешёвый канал для inbound updates, FAQ и предзаполнения обращений. [T2]
2. Но с **1 июня 2025 года** для банков, некредитных финансовых организаций, операторов связи, маркетплейсов и ряда крупных сервисов введён запрет на использование иностранных мессенджеров для передачи персональных данных и уведомлений в части официального обслуживания. Для страховщиков это серьёзное ограничение на полноценное claims handling внутри Telegram. [T2] https://www.garant.ru/news/1804464/
3. Следовательно, **Telegram в RU годится как вспомогательный слой**, но не как основной контур урегулирования убытков. Реалистичный use case: lead intake, статусные уведомления без чувствительных данных, запись на осмотр, reminder, FAQ. Не реалистичный use case: полный документооборот по убытку и передача чувствительных материалов как основной канал. [T2][inference]

## 6. WTP, proof of willingness to pay
1. Публичные прайсы у CraftTalk, Naumen и T-Bank показывают, что рынок уже платит за automation building blocks десятки тысяч рублей в месяц и выше, а enterprise-слой почти всегда уходит в custom pricing. Это косвенное, но сильное доказательство willingness to pay за claims-adjacent automation. [T2]
2. В российских страховых группах стоимость даже небольшой команды урегулирования быстро уходит в сотни тысяч рублей в месяц на FTE, а у топ-10 страховщиков счёт идёт на десятки и сотни сотрудников across call center, front-line claims, document review и anti-fraud. Поэтому экономия 5-10 FTE или сокращение cycle time на массовых линиях уже создаёт бюджет на SaaS/managed-service чек **500 тыс. - 1,5 млн ₽/мес**. [T1][T2][inference]
3. Самый правдоподобный buyer budget owner: COO по урегулированию, директор по клиентскому сервису, операционный директор моторного блока, CIO / head of digital claims transformation. Бюджет берётся не из «инноваций», а из действующих строк cost-to-serve, подрядчиков и headcount. [T2][inference]

## 7. Profit Gate: проверка всех сценариев монетизации
### Сценарий A. SaaS / workflow layer
- Чек: **500-700 тыс. ₽/мес** на одного страховщика за FNOL + triage + routing + analytics. [T2][inference]
- Нужно для EBITDA > 500 тыс. ₽/мес: **5 клиентов × 600 тыс. ₽ = 3,0 млн ₽ MRR**.
- При валовой марже 65% и OPEX ~1,3 млн ₽/мес получается EBITDA около **650 тыс. ₽/мес**. [inference]
- **Вывод:** достижимо, но требует сильного продукта и интеграций.

### Сценарий B. Managed service / AI-оператор
- Чек: **1,0-1,5 млн ₽/мес** на клиента за обработку потока обращений с human-in-the-loop SLA. [T2][inference]
- Нужно для EBITDA > 500 тыс. ₽/мес: **3 клиента × 1,2 млн ₽ = 3,6 млн ₽ MRR**.
- При валовой марже 45% и OPEX ~1,0 млн ₽ EBITDA около **620 тыс. ₽/мес**. [inference]
- **Вывод:** самый реалистичный стартовый путь для РФ, потому что value проще привязать к SLA и headcount substitution.

### Сценарий C. Hybrid outcome-based
- Чек: **300-500 тыс. ₽/мес platform fee + success fee** за claim throughput / speed / leakage reduction. [T2][inference]
- Нужно для EBITDA > 500 тыс. ₽/мес: **4 клиента × 850 тыс. ₽ blended MRR ≈ 3,4 млн ₽/мес**.
- При валовой марже 50% и OPEX ~1,1 млн ₽ EBITDA около **600 тыс. ₽/мес**. [inference]
- **Вывод:** достижимо, если есть исторические данные и доверие клиента.

### Итог по Profit Gate
**Profit Gate = PASS.** Даже при слабом category-search спросе компания может превысить **500 тыс. ₽ EBITDA/мес** в нескольких сценариях, если заходит в верхний сегмент страховщиков и продаёт measurable claims outcomes, а не generic AI automation. [T2][inference]

## 8. Market sizing
### Методика
Считаю два пути: top-down и bottom-up, затем беру более консервативное значение.

#### Top-down
- Глобальный claims management software market: **$4,25 млрд** в 2024. [T2]
- Глобальные non-life premiums: **$4,0 трлн** в 2023. [T2]
- Benchmark spend ratio: **0,106%** от non-life premiums. [calc]
- РФ total premiums: **3,7 трлн ₽** в 2024. [T1]
- Для claims ops беру только non-life-like addressable part рынка, консервативно **45%** total premiums, то есть **1,665 трлн ₽**. Это рабочее приближение, потому что life-страхование гораздо хуже подходит под mass claims ops wedge. [T1][inference]
- **TAM РФ top-down = 1,665 трлн ₽ × 0,106% = 1,77 млрд ₽**. [calc]
- Для SAM беру только mid-market и top-tier carriers, где есть достаточный объём убытков, интеграционный бюджет и готовность к AI-оператору: **35% TAM = 620 млн ₽**. [inference]
- SOM Y1: **3% SAM = 18,6 млн ₽**. [calc]
- SOM Y3: **10% SAM = 62,0 млн ₽**. [calc]

#### Bottom-up
- Total buyers: **60** потенциальных покупателей в РФ-контуре, включая крупные и средние non-life insurers, специализированных health/property carriers и TPA/claims outsourcers. Реальность existence подтверждается единым реестром субъектов страхового дела Банка России. [T1] https://www.cbr.ru/insurance/registers/
- % with need: **70%**, потому что именно mass-claims линии и сервисные подразделения регулярно сталкиваются с document intake, routing, voice, fraud pre-check и SLA bottlenecks. [T2][inference]
- Avg ARR: **15 млн ₽/год** на одного покупателя, то есть около **1,25 млн ₽/мес**, что согласуется с managed-service и hybrid enterprise чеком. [T2][inference]
- **SAM bottom-up = 60 × 70% × 15 млн ₽ = 630 млн ₽**. [calc]
- SOM Y1 bottom-up при 3 клиентах: **45 млн ₽/год**. [calc]
- SOM Y3 bottom-up при 7 клиентах: **105 млн ₽/год**. [calc]

### 10 реальных buyers для GTM-базы
1. СОГАЗ [T1]
2. РЕСО-Гарантия [T1]
3. Ингосстрах [T1]
4. АльфаСтрахование [T1]
5. Росгосстрах [T1]
6. ВСК [T1]
7. Ренессанс Страхование [T1]
8. Согласие [T1]
9. МАКС [T1]
10. Т-Страхование [T1]

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $4,25 млрд [T2] | — | — | top-down |
| TAM (РФ) | 1,77 млрд ₽ [T1][T2] | — | bottom-up не считает весь рынок | top-down |
| SAM (РФ) | 620 млн ₽ [T1][T2] | 630 млн ₽ [T1][T2] | diff < 2%, оценка сошлась хорошо | **620 млн ₽** |
| SOM Y1 | 18,6 млн ₽ | 45 млн ₽ | top-down строже, safer | **18,6 млн ₽** |
| SOM Y3 | 62,0 млн ₽ | 105 млн ₽ | беру более консервативно | **62,0 млн ₽** |

### Sanity checks
- Расхождение top-down и bottom-up по SAM меньше 3x, пересборка не требуется. [calc]
- SOM Y1 = 18,6 млн ₽, это около 3% SAM, реалистично и не выглядит overclaim. [calc]
- Если средний sales cycle 6-9 месяцев, закрыть 3 enterprise клиента за первый год тяжело, но возможно при founder-led продажах и сильном design-partner motion. [T2][inference]

## 9. Главные риски спроса
1. **Category demand low.** Вход через формулировку «AI claims ops» в РФ почти никто не ищет. Продавать придётся через ROI, SLA, сокращение времени урегулирования и cost-to-serve. [API][inference]
2. **Long enterprise sales cycle.** Страховщики медленные, интеграции тяжёлые, нужен POC и безопасность. [T2]
3. **Telegram как канал ограничен регулированием.** Его нельзя считать core workflow moat. [T2]
4. **Горизонтальные платформы уже закрывают часть value chain.** Без глубокой вертикальной экспертизы новый игрок превратится в ещё одного vendor-а ботов/контакт-центра. [T2][inference]

## 10. Итоговое решение
**VERDICT: PROCEED.**

Почему не reject:
- demand API слабый, но **WTP подтверждается** существующими enterprise spend и публичными ценами substitutes; [T2]
- **Profit Gate проходит** в SaaS, managed service и hybrid-моделях; [inference]
- есть узкий, но понятный ICP: top-30/60 non-life insurers и claims-heavy линии; [T1][inference]
- правильный wedge для РФ, вероятно, не «полный AI claims brain», а **FNOL + triage + document orchestration + human-in-the-loop claims ops**. [T2][inference]

Следующий шаг на pipeline-уровне: проверить delivery feasibility, интеграции, регуляторику персональных данных и скорость пилота в 1-2 вертикалях, прежде всего motor и property. [T1][T2]

Sources: T1=4, T2=7, T3=0. Primary evidence basis: T2 with T1 market anchors.

> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче видны свежие публикации, обновления вендоров, вакансии и/или новая рыночная активность.

---

# FILE: 03-solution.md

---
stage: solution
case: ai-native-claims-ops-dlya-strahovshchikov
date: 2026-05-11
analyst: branch-models-lead
sector: FINTECH
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
AI-native claims ops для страховщиков: внешний AI-оператор / software-enabled service для FNOL, triage, document intake, routing, fraud pre-check и части back-office урегулирования убытков.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продуктовая боль реальна и дорогая: intake, маршрутизация, проверка документов, SLA и ручной труд в claims-операциях уже закрываются тяжелыми core claims systems и горизонтальными automation-вендорами, значит бюджет существует. [T1][T2][T3]
2. Но standalone wedge слабый, если продавать это как «ещё один AI-бот для урегулирования». Реалистичный вход только как outcome-layer поверх существующего claims stack, а не как замена ядра. [T1][T2][T3][inference]
3. Лучший локальный wedge, FNOL + triage + document orchestration + human-in-the-loop claims ops для top insurers и claims-heavy линий. [T1][T2][inference]
4. Главный риск, buyer уже имеет Guidewire / Duck Creek / Sapiens-подобную логику у global peers или локальные аналоги/самописные контуры, поэтому новый игрок легко превращается в подрядчика без platform power. [T2][T3][inference]

## 1. Какую проблему реально решает продукт

Покупают не «AI ради AI», а четыре очень конкретные вещи:
- ускорение **first notice of loss** и intake обращения;
- автоматическую сортировку и assignment по типу убытка, полноте пакета и срочности;
- снижение ручного document-review и повторных запросов клиенту;
- сокращение cycle time, leakage и cost-to-serve по массовым линиям урегулирования. [T1][T2][T3]

Если продукт не даёт measurable improvement по этим метрикам, он не нужен. Для страховщика claims operations это уже зона mission-critical workflow, а не nice-to-have productivity tool. [T1][inference]

## 2. Что уже есть у покупателя

У крупного страховщика обычно уже присутствуют substitutes:
- core claims management system;
- BPM / workflow / OCR / contact-center стек;
- антифрод и rules engines;
- подрядчики на BPO и ручную проверку;
- внутренние digital-команды для клиентского сервиса и урегулирования.

Глобальные category anchors это подтверждают:
- **Guidewire ClaimCenter** позиционируется как end-to-end claims management system от claim intake до closure, с automation и embedded insurance AI. [T2]
- **Duck Creek Claims** продаёт FNOL, triage, assignment, fraud detection и settlement в рамках единой claims platform. [T3]
- **Sapiens ClaimsPro** также продаёт rules-driven workflow, automated assignment и end-to-end P&C claims automation. [T3]

Следовательно, новый игрок не должен обещать «мы построим весь claims core заново». Реалистично продавать только верхний операционный слой, который ускоряет конкретный участок процесса и быстро подключается к уже существующему контуру. [T2][T3][inference]

## 3. Продуктовый wedge

### Core wedge
**Claims outcome layer поверх существующего страхового стека**:
- intake и предзаполнение кейса;
- document collection / completeness check;
- triage и routing;
- AI-first workbench для low-complexity claims;
- HITL-очередь для сложных кейсов;
- dashboard по SLA, throughput, handoff rate и leakage signals.

### Почему именно такой wedge выглядит правдоподобно
1. Он не требует заменить ядро страховщика, а встраивается в него. [T2][T3][inference]
2. Его можно привязать к понятным KPI: time-to-open, time-to-assign, time-to-close, % touchless/low-touch claims, cost per claim. [T2][T3][inference]
3. Он продаётся операционному buyer'у как снижение headcount pressure и backlog, а не как «инновация». [T1][inference]

### Что wedge не должен делать
- не позиционироваться как generic chatbot;
- не пытаться быть full-stack core claims platform с нуля;
- не делать ставку на Telegram как на основной moat;
- не продаваться в SMB-страхование или в broad market без явного claims volume.

## 4. Для кого solution-fit реален

### Primary ICP
- top-30/60 страховщиков в РФ с массовыми non-life линиями;
- motor, property, travel, DMS/health-like claims operations, где есть повторяемый поток кейсов;
- крупные страховые группы с call-center, документооборотом и backlog в урегулировании.

### Buyer'ы
- COO / директор по урегулированию;
- директор по клиентскому сервису;
- head of claims transformation / operations excellence;
- CIO / digital, если есть сильный бизнес-спонсор.

### ICP-фильтр
Клиент проходит, если одновременно есть:
1. большой поток типовых обращений;
2. заметная доля ручной проверки документов;
3. SLA pain и backlog;
4. готовность интегрироваться с core claims / CRM / contact center;
5. бюджет не на эксперимент, а на cost reduction и process improvement. [T1][T2][T3][inference]

### Нецелевой сегмент
- мелкие страховщики без объёма claims;
- линии с низкой частотой и высокой экспертной сложностью, где automation-touch ограничен;
- клиенты, которым нужен только бот для статуса обращения;
- команды без owner'а процесса урегулирования.

## 5. Delivery model

### Наиболее правдоподобная схема внедрения
1. выбрать один claims flow, например моторный FNOL или document intake;
2. подключить продукт к действующему каналу обращений и core/workflow-системе;
3. запустить AI triage и completeness check на ограниченном сегменте;
4. оставить human-in-the-loop на спорных и сложных кейсах;
5. доказать улучшение по KPI за 6-10 недель;
6. только потом масштабировать на другие линии и этапы claims journey. [T2][T3][inference]

### KPI пилота
- time-to-open claim;
- time-to-assignment;
- % claims без повторного запроса документов;
- touchless / low-touch share;
- cost per processed claim;
- handoff rate в human queue;
- NPS/CSAT по статусным коммуникациям.

## 6. Почему клиент купит это, а не текущий стек

Продукт может выиграть только если одновременно:
1. **быстрее запускается**, чем кастомная доработка core claims stack;
2. **лучше считает и показывает ROI**, чем набор OCR + BPM + contact-center tools;
3. **берёт на себя managed operations слой**, а не просто отдаёт API и исчезает;
4. **снижает ручной труд на measurable участке**, а не только улучшает UX клиента. [T1][T2][T3][inference]

Если этого нет, buyer выберет расширение текущего вендора, внутреннюю разработку или BPO-подрядчика.

## 7. Конкурентная позиция

### Против core claims platforms
Новый продукт не выигрывает как замена ClaimCenter/Duck Creek/Sapiens. Он может выиграть только как overlay, который внедряется быстрее и закрывает automation-gap без большой замены ядра. [T2][T3][inference]

### Против горизонтальных contact-center / OCR / bot vendors
Здесь шанс выше, если продукт собирает outcome на уровне whole claim intake/triage flow, а не продаёт один кирпич вроде распознавания речи или чат-бота. [T1][inference]

### Против BPO / ручного урегулирования
Сильный аргумент есть там, где страховщик уже чувствует дефицит людей, растущий backlog или дорогой пик нагрузки. Тогда hybrid AI-operator модель выглядит особенно правдоподобно. [T1][inference]

## 8. Основные риски solution-fit

1. **Core-system dependency risk.** Без интеграции в claims ядро продукт остаётся поверхностным add-on.
2. **Commodity risk.** Отдельные части value chain уже закрыты OCR, voice AI, workflow и anti-fraud вендорами.
3. **Long enterprise cycle risk.** Даже хороший пилот может идти медленно из-за безопасности, ИБ, архитектуры и согласований.
4. **Narrow-wedge risk.** Реальный fit есть в 1-2 потоках claims, а не во всём страховом ландшафте.
5. **Regulatory/process risk.** Telegram и другие внешние каналы не годятся как основной контур работы с чувствительными данными. [T1][inference]
6. **Services-overhang risk.** Без продуктовой стандартизации кейс скатится в кастомный проект и потеряет scalability.

## 9. Что обязательно проверить на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой enterprise ACV реально удерживается за pilot + managed operations;
- сколько presale и integration effort требует один страховщик;
- где проходит граница между software gross margin и project-heavy delivery;
- сколько клиентов нужно для EBITDA выше 500 000 ₽/мес;
- можно ли повторять шаблон на 2-3 массовых линиях без полной пересборки delivery;
- насколько buyer готов платить за outcome-layer, если уже платит за core claims platform.

## Итог для пайплайна

**P4 пройден условно.**

Кейс стоит двигать дальше только как узкий enterprise wedge: **FNOL + triage + document orchestration + HITL claims ops** поверх существующего страхового стека. Как broad AI claims platform для рынка РФ история пока выглядит слишком тяжёлой и слишком зависимой от интеграций.

## Источники
- [T1] `02-demand.md` в текущем кейсе: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-native-claims-ops-dlya-strahovshchikov/02-demand.md
- [T2] Guidewire ClaimCenter: https://www.guidewire.com/en/products/core-products/insurancesuite/claimcenter-claims-management-software
- [T3] Duck Creek Claims: https://www.duckcreek.com/product/claims-management-software/
- [T3] Sapiens ClaimsPro: https://sapiens.com/us/property-and-casualty/claimspro/

---

# FILE: 04-economics.md

---
stage: economics
case: ai-native-claims-ops-dlya-strahovshchikov
date: 2026-05-11
analyst: branch-models-lead
sector: FINTECH-INSURANCE
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P5: PASS.**

Кейс выглядит **инвестиционно допустимым**, но только как **enterprise regulated software-enabled service** для top insurers, а не как лёгкий SaaS.

Ключевые выводы:
- рабочая модель, **1,30 млн ₽ MRR на клиента**;
- **COGS = 0,53 млн ₽/клиент/мес**, contribution после COGS = **0,77 млн ₽**, contribution margin = **59,2%**;
- **fully-loaded blended CAC = 1,51 млн ₽**;
- benchmark churn для enterprise B2B SaaS беру **~12% годовых**, то есть **~1,0% monthly logo churn** как реалистичный локальный ориентир для длинных контрактов и тяжёлого внедрения; [E6][inference]
- **LTV = 77,0 млн ₽**, **LTV/CAC = 51,1x**, **CAC payback = 2,0 мес**;
- monthly break-even достигается примерно на **8 клиентах**;
- при аккуратном hire-плане **burn to breakeven ~39,8 млн ₽**, поэтому нужен стартовый капитал порядка **45 млн ₽**.

Вывод фонда: **экономика проходит порог 3:1 с большим запасом, EBITDA > 500 тыс. ₽/мес достижима задолго до 50 клиентов, значит Profit Gate = PASS**.

---

## 1. Модель монетизации

**Базовый контракт:** managed claims ops + AI workflow layer для одного страховщика.

| Компонент выручки | ₽/мес на клиента | Комментарий |
|---|---:|---|
| Platform fee | 750 000 | FNOL, triage, routing, dashboard |
| Managed ops / HITL слой | 350 000 | контроль сложных кейсов и SLA |
| Usage / success-fee слой | 200 000 | документы, voice, throughput |
| **Итого MRR на клиента** | **1 300 000** | базовая модель P5 |

Основание: в `02-demand.md` и `03-solution.md` уже подтверждён enterprise-check **0,5–1,5 млн ₽/мес**, а в `01-intake.md` есть сильный global category signal на high-ACV модель через Reserv. [T1][T2][T3]

---

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | ICP-лист и research страховщиков | SDR | HH/СПАРК/CRM/manual research | 2 ч | 2 000 | средняя |
| 2 | Первый outreach | SDR | email, phone, Telegram/мессенджер where allowed | 30 мин | 500 | средняя |
| 3 | Follow-up sequence 5-7 касаний | SDR | CRM + sequencing | 10 дней | 4 000 | высокая |
| 4 | Discovery call | AE + founder | Meet/Zoom | 1 ч | 12 000 | низкая |
| 5 | Qualification + ROI hypothesis | AE | CRM, ROI sheet | 1 день | 8 000 | средняя |
| 6 | Demo claims workflow | AE + solutions | demo env | 1,5 ч | 15 000 | средняя |
| 7 | Security / legal / architecture review | CTO + AE | docs, DPA, ИБ пакет | 2-4 недели | 80 000 | низкая |
| 8 | Pilot scoping | CTO + PM + buyer | workshop | 1 неделя | 60 000 | низкая |
| 9 | Pilot integration | backend + ML + DevOps | API, OCR, queues, storage | 4-6 недель | 220 000 | средняя |
| 10 | Pilot ops with HITL | CSM + claims ops analyst | internal console | 1 месяц | 140 000 | средняя |
| 11 | KPI review and business case | AE + founder | BI/report | 1 неделя | 20 000 | средняя |
| 12 | Procurement and contract signing | AE + founder + legal | CRM + docs | 2-6 недель | 45 000 | низкая |
| 13 | Go-live | CSM + CTO | production stack | 1 неделя | 35 000 | средняя |
| 14 | Monthly service delivery | CSM + ML + support | platform + ops queue | ongoing | 530 000 | средняя |
| 15 | Invoice and payment collection | finance ops | 1C/банк/ЭДО | 5 дней | 8 000 | высокая |

### Что важно для фонда
- Самые дорогие места не в лидах, а в **presale + pilot + integration**.
- Поэтому эта история не self-serve и не SMB SaaS, а **regulated enterprise acquisition motion**.
- До первой оплаты цикл реалистично занимает **6-9 месяцев**. [T2][T4][T6][inference]

---

## 3. COGS breakdown на 1 клиента в месяц

| Статья COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM / OCR / speech inference | 120 000 | вызовы моделей, OCR, STT/TTS под claims flow | T1 + market inference |
| Cloud compute + storage + backups | 75 000 | prod env, защищённое хранение документов | T2 + inference |
| HITL claims ops analysts | 160 000 | 0,8 FTE операционного специалиста | HH benchmark / inference |
| CSM allocation | 85 000 | 0,25 FTE CSM на клиента | HH benchmark / inference |
| Support + QA + monitoring | 55 000 | shared support pool allocation | inference |
| Security / compliance allocation | 35 000 | журналирование, аудит, DLP/ИБ сервисы | inference |
| **Итого COGS** | **530 000** |  |  |

**Gross profit на клиента = 1 300 000 - 530 000 = 770 000 ₽/мес.**

---

## 4. CAC по каналам с funnel conversion

### Канал 1. Founder-led outbound

| Этап | Conversion |
|---|---:|
| 300 target accounts | 100% |
| 75 replies | 25% |
| 24 discovery calls | 32% |
| 10 qualified opportunities | 42% |
| 4 pilots | 40% |
| 1 paid customer | 25% |

| Метрика | Значение |
|---|---:|
| Monthly spend | 900 000 ₽ |
| New paying customers / мес | 0,75 |
| **CAC channel** | **1 200 000 ₽** |

### Канал 2. Partnerships / SI / insurtech ecosystem

| Этап | Conversion |
|---|---:|
| 20 active partners | 100% |
| 8 intros | 40% |
| 5 qualified meetings | 62% |
| 3 pilots | 60% |
| 1 paid customer | 33% |

| Метрика | Значение |
|---|---:|
| Monthly spend | 650 000 ₽ |
| New paying customers / мес | 0,60 |
| **CAC channel** | **1 083 000 ₽** |

### Канал 3. Content + events + inbound

| Этап | Conversion |
|---|---:|
| 120 leads / мес | 100% |
| 18 meetings | 15% |
| 7 SQL | 39% |
| 2 pilots | 29% |
| 0,5 paid customers | 25% |

| Метрика | Значение |
|---|---:|
| Monthly spend | 700 000 ₽ |
| New paying customers / мес | 0,50 |
| **CAC channel** | **1 400 000 ₽** |

### Blended CAC

Предполагаю steady-state mix: 45% outbound, 35% partnerships, 20% inbound.

**Blended CAC = 1,20m × 45% + 1,083m × 35% + 1,40m × 20% = 1,199m ₽.**

Но для фонда использую **fully-loaded CAC**, а не channel-only.

---

## 5. FULLY-LOADED CAC

### Таблица компонентов

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | search + retargeting на узкий B2B ICP | inference |
| Outbound team FOT (SDR/AE attributed to new) | 663 000 | SDR 160k + AE 350k, всё ×1,3 | E1 E2 E3 E4 |
| Marketing team FOT (partial allocation) | 156 000 | marketer 240k × 50% ×1,3 | E2/E3 inference |
| Tools (CRM, data, sequencing, call stack) | 95 000 | CRM + prospecting + call/meeting stack | inference |
| Events/partnerships | 125 000 | средний месячный аллокейт на офлайн и партнёров | inference |
| Overhead multiplier (x1.3) | 347 100 | 30% overhead на acquisition stack | standard enterprise B2B |
| **Итого fully-loaded spend** | **1 506 100** |  |  |

### Расчёт
- Raw acquisition stack = **1 159 000 ₽/мес**
- Overhead = **347 100 ₽/мес**
- Fully-loaded spend = **1 506 100 ₽/мес**
- New paying customers = **1,0 / мес**
- **Fully-loaded CAC = 1 506 100 ₽**

### Sanity check по сегменту
- Это **regulated enterprise** кейс, поэтому CAC выше mid-market и заметно выше простого SaaS.
- Полученный CAC **вписывается в верхнюю часть** диапазона для enterprise / regulated B2B motion из задания и не выглядит подозрительно низким.
- CAC не ниже 30% от benchmark, red flag нет.

---

## 6. LTV с churn rate

### Benchmark churn
- Bessemer для лучших private cloud companies показывает, что у enterprise-направления annual gross logo churn обычно **ниже 10%**, а для weaker cohorts может быть выше. [E6]
- Для консервативной модели РФ беру **12% annual logo churn**, то есть примерно **1,0% monthly churn**. Это чуть хуже best-in-class, что разумно для молодого продукта с пилотами и тяжёлым внедрением. [E6][inference]

### Расчёт LTV
Формула: **LTV = Gross Profit per customer per month / Monthly churn**

- Gross Profit per customer per month = **770 000 ₽**
- Monthly churn = **1,0% = 0,01**
- **LTV = 770 000 / 0,01 = 77 000 000 ₽**

### Вывод
Даже при более жёстком churn **1,5% monthly** LTV остаётся **51,3 млн ₽**, поэтому запас к CAC очень большой.

---

## 7. LTV/CAC ratio

- **LTV = 77 000 000 ₽**
- **Fully-loaded CAC = 1 506 100 ₽**
- **LTV/CAC = 51,1x**

**Investment grade threshold 3:1 пройден с огромным запасом.**

Комментарий: столь высокий ratio типичен для high-ACV enterprise моделей с низким churn, но он не отменяет тяжёлую проблему upfront burn и длинного sales cycle.

---

## 8. CAC Payback

Формула из задания: **CAC Payback = CAC / MRR per customer**

- CAC = **1 506 100 ₽**
- MRR per customer = **1 300 000 ₽**
- **CAC Payback = 1,16 мес**

Более строгий вариант через gross profit:
- 1 506 100 / 770 000 = **1,96 мес**

**Вывод:** даже по gross margin payback < 12 месяцев, значит тест пройден.

---

## 9. Contribution Margin %

Формула: **(Revenue - COGS) / Revenue**

- Revenue = **1 300 000 ₽**
- COGS = **530 000 ₽**
- Contribution = **770 000 ₽**
- **Contribution Margin = 59,2%**

Для software-enabled service это хороший, но не exceptional уровень. Улучшение возможно после стандартизации внедрений и снижения HITL-нагрузки.

---

## 10. Team & FOT

### Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 700 000 | 0 | 0 | 210 000 | 910 000 |
| CTO / Tech Lead | 1 | 600 000 | 2,0 | 2,0 | 180 000 | 780 000 |
| Senior Backend | 2 | 400 000 | 1,5 | 1,5 | 120 000 | 1 040 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2,0 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1,0 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1,0 | 1,0 | 90 000 | 390 000 |
| SDR | 1 | 160 000 | 0,75 | 1,0 | 48 000 | 208 000 |
| AE | 1 | 350 000 | 1,5 | 2,5 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1,0 | 1,0 | 75 000 | 325 000 |
| **Итого** | **10** |  |  |  |  | **5 213 000** |

### Функции команды

| Роль | Ключевая функция |
|---|---|
| CEO | founder-led sales, enterprise trust, fundraising |
| CTO | архитектура, security review, integration design |
| Senior Backend | claims workflow, API, queues, document orchestration |
| ML Engineer | extraction, routing models, quality loop |
| DevOps | infra, observability, compliance basics |
| Frontend | operator workbench, dashboard |
| SDR | первичный outbound и meeting generation |
| AE | discovery, ROI, closing, procurement navigation |
| Customer Success | onboarding, renewals, usage expansion |

### Salary basis
- Tech salary anchors: HH median API показывает типичные вилки по backend, frontend и DevOps в Москве. [E1]
- Прямые вакансии на hh.ru подтверждают уровни для senior backend, frontend, DevOps, AE и SDR. [E2][E3][E4][E5]
- Для CEO и CTO беру midpoint из диапазонов задания и рынка Москвы как консервативный hiring benchmark. [inference]

---

## 11. Cumulative FOT timeline M1-M12

Правило realism соблюдено: в M1 не нанимаю 5+ человек, команда раскладывается по hire-lag.

| Месяц | Кто уже в команде | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 910 000 | founder-led discovery |
| M2 | CEO + CTO | 1 690 000 | старт архитектуры |
| M3 | CEO + CTO + Backend1 + SDR | 2 418 000 | первая сборка и outbound |
| M4 | + Frontend + CSM | 3 133 000 | demo и pilot readiness |
| M5 | + DevOps + AE | 4 043 000 | полноценный presale |
| M6 | + Backend2 | 4 563 000 | integration capacity grows |
| M7 | + ML Engineer | 5 213 000 | production ML loop |
| M8 | полный состав | 5 213 000 | steady state |
| M9 | полный состав | 5 213 000 | steady state |
| M10 | полный состав | 5 213 000 | steady state |
| M11 | полный состав | 5 213 000 | steady state |
| M12 | полный состав | 5 213 000 | steady state |

Ramp влияет не на FOT, а на продуктивность, поэтому выручка смещается вправо и входит в burn model ниже.

---

## 12. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT steady-state | 5 213 000 | из таблицы выше |
| Office / admin / бухгалтерия | 180 000 | lean office + back-office |
| Legal / compliance / DPA / procurement | 120 000 | договоры, ИБ, регуляторка |
| Core internal software | 95 000 | Jira, docs, monitoring, mail |
| Finance / banking / ЭДО | 35 000 | операционный контур |
| Recruiting / HR buffer | 90 000 | ongoing search |
| **Итого fixed costs / мес** | **5 733 000** |  |

---

## 13. Break-even по числу клиентов

### На contribution basis
- Contribution per client = **770 000 ₽/мес**
- Fixed costs = **5 733 000 ₽/мес**
- Break-even client count = **5 733 000 / 770 000 = 7,45**
- Округляю вверх: **8 клиентов**

### Проверка EBITDA
| Клиентов | Revenue, ₽/мес | Gross profit, ₽/мес | EBITDA before tax, ₽/мес |
|---|---:|---:|---:|
| 5 | 6 500 000 | 3 850 000 | -1 883 000 |
| 8 | 10 400 000 | 6 160 000 | **427 000** |
| 9 | 11 700 000 | 6 930 000 | **1 197 000** |
| 10 | 13 000 000 | 7 700 000 | **1 967 000** |
| 50 | 65 000 000 | 38 500 000 | **32 767 000** |

**Profit Gate test проходит:** даже не на 50, а уже на **9 клиентах** EBITDA уверенно выше **500 000 ₽/мес**.

---

## 14. Break-even по месяцам

### План по клиентам M1-M12

| Месяц | Платящих клиентов | Revenue, ₽ | Gross profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 370 000 | -1 370 000 |
| M2 | 0 | 0 | 0 | 2 060 000 | -2 060 000 |
| M3 | 0 | 0 | 0 | 2 908 000 | -2 908 000 |
| M4 | 0 | 0 | 0 | 3 623 000 | -3 623 000 |
| M5 | 0 | 0 | 0 | 4 533 000 | -4 533 000 |
| M6 | 1 | 1 300 000 | 770 000 | 5 053 000 | -4 283 000 |
| M7 | 2 | 2 600 000 | 1 540 000 | 5 703 000 | -4 163 000 |
| M8 | 3 | 3 900 000 | 2 310 000 | 5 733 000 | -3 423 000 |
| M9 | 5 | 6 500 000 | 3 850 000 | 5 733 000 | -1 883 000 |
| M10 | 6 | 7 800 000 | 4 620 000 | 5 733 000 | -1 113 000 |
| M11 | 7 | 9 100 000 | 5 390 000 | 5 733 000 | -343 000 |
| M12 | 8 | 10 400 000 | 6 160 000 | 5 733 000 | **427 000** |

### Вывод
- **Monthly break-even наступает в M12**.
- Для выхода выше **500k EBITDA/mo** нужен **M13 или 9 клиентов**.

---

## 15. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Суммарный отрицательный EBITDA до конца M11:

**39 702 000 ₽**

Добавляю safety buffer на задержки оплат, extra legal, доработки пилотов и hiring slippage **~5,3 млн ₽**.

**Startup capital to breakeven = ~45 млн ₽.**

### Cash runway
При стартовом капитале **45 млн ₽**:
- средний burn M1-M8 ≈ **3,30 млн ₽/мес**;
- runway до cash-zero без роста продаж ≈ **13,6 мес**;
- при базовом плане компания добирается до monthly break-even примерно к концу **12-го месяца**.

### Sanity checks
- Для enterprise B2B SaaS / service-heavy модели капитал <10 млн ₽ был бы нереалистичен.
- В этой модели нужно **не менее 45 млн ₽**, и это выглядит правдоподобно.

---

## 16. Риски экономики

1. **Pilot-heavy delivery risk.** Если pilot требует >400k кастомных работ на клиента, gross margin быстро уедет вниз.
2. **Compliance drag.** Любая ИБ/регуляторная надстройка увеличивает presale CAC и time-to-cash.
3. **Logo concentration.** Рынок узкий, поэтому пара срывов procurement цикла сдвигает break-even на квартал.
4. **Services creep.** Если HITL не стандартизирован, contribution margin падает ниже 50%.

---

## 17. Финальный вывод

**VERDICT: PASS.**

Почему кейс проходит P5:
- **LTV/CAC = 51,1x**, сильно выше порога **3:1**;
- **CAC payback 1,16 мес по MRR** и **1,96 мес по gross profit**;
- **contribution margin 59,2%** достаточен для enterprise software-enabled service;
- **EBITDA > 500k/mo** достижима уже на **9 клиентах**, а не только на 50;
- нужный капитал высокий, но реалистичный для regulated enterprise motion.

Для фонда это **не low-burn SaaS**, а **капиталоёмкий, но потенциально качественный vertical enterprise business**, если команда удержит стандартизацию внедрений и churn не уйдёт выше 2% monthly.

---

## Sources
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-native-claims-ops-dlya-strahovshchikov/02-demand.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-native-claims-ops-dlya-strahovshchikov/03-solution.md
- [T3] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-native-claims-ops-dlya-strahovshchikov/01-intake.md
- [E1] HH Salary API, медианы по backend/frontend/devops: https://api.hh.ru/salary_statistics
- [E2] HH.ru, senior backend salary examples: https://hh.ru/search/vacancy?text=senior+backend+developer
- [E3] HH.ru, DevOps / Tech Lead / marketing salary examples: https://hh.ru/search/vacancy?text=devops
- [E4] HH.ru, AE / SDR salary examples: https://hh.ru/search/vacancy?text=account+executive
- [E5] HH.ru, customer success salary examples: https://hh.ru/search/vacancy?text=customer+success+manager
- [E6] Bessemer Venture Partners, State of the Cloud / churn benchmarks: https://www.bvp.com/atlas/state-of-the-cloud-2024

---

# FILE: 05-critic.md

# SECTION A — PnL

## 1) PnL 12 месяцев x 3 сценария

Исходные допущения из `04-economics.md`: ARPA 1,30 млн ₽/клиент/мес, COGS 0,53 млн ₽/клиент/мес, gross profit 0,77 млн ₽/клиент/мес, gross margin 59,2%, fully-loaded CAC 1,506 млн ₽, steady-state fixed costs 5,733 млн ₽/мес, monthly churn: base 1,0%, optimistic 0,5%, pessimistic 2,0%.

### Базовый scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 1 | 1.99 | 2.97 | 4.94 | 5.89 | 6.83 | 7.76 |
| MRR, млн ₽ | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.30 | 2.59 | 3.86 | 6.42 | 7.66 | 8.88 | 10.09 |
| COGS, млн ₽ | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.53 | 1.05 | 1.57 | 2.62 | 3.12 | 3.62 | 4.11 |
| Gross profit, млн ₽ | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.77 | 1.53 | 2.29 | 3.80 | 4.54 | 5.26 | 5.98 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% |
| Fixed costs, млн ₽ | 1.37 | 2.06 | 2.91 | 3.62 | 4.53 | 5.05 | 5.70 | 5.73 | 5.73 | 5.73 | 5.73 | 5.73 |
| EBITDA, млн ₽ | -1.37 | -2.06 | -2.91 | -3.62 | -4.53 | -4.28 | -4.17 | -3.45 | -1.93 | -1.20 | -0.47 | 0.25 |
| Cash burn, млн ₽ | -1.37 | -2.06 | -2.91 | -3.62 | -4.53 | -4.28 | -4.17 | -3.45 | -1.93 | -1.20 | -0.47 | 0.00 |
| Cumulative cash, млн ₽ | -1.37 | -3.43 | -6.34 | -9.96 | -14.49 | -18.78 | -22.95 | -26.39 | -28.32 | -29.52 | -29.99 | -29.75 |

Break-even: 8 клиентов, месяц EBITDA>0: M12. Startup capital to BE: 34.5 млн ₽.


### Оптимистичный scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 2.99 | 4.97 | 6.95 | 8.91 | 10.87 | 12.81 | 14.75 |
| MRR, млн ₽ | 0.00 | 0.00 | 0.00 | 1.30 | 2.59 | 3.88 | 6.46 | 9.03 | 11.58 | 14.13 | 16.66 | 19.17 |
| COGS, млн ₽ | 0.00 | 0.00 | 0.00 | 0.53 | 1.06 | 1.58 | 2.63 | 3.68 | 4.72 | 5.76 | 6.79 | 7.82 |
| Gross profit, млн ₽ | 0.00 | 0.00 | 0.00 | 0.77 | 1.54 | 2.30 | 3.83 | 5.35 | 6.86 | 8.37 | 9.86 | 11.36 |
| GM% | 0.0% | 0.0% | 0.0% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% |
| Fixed costs, млн ₽ | 1.37 | 2.06 | 2.91 | 3.62 | 4.53 | 5.30 | 6.10 | 6.40 | 6.40 | 6.40 | 6.40 | 6.40 |
| EBITDA, млн ₽ | -1.37 | -2.06 | -2.91 | -2.85 | -3.00 | -3.00 | -2.27 | -1.05 | 0.46 | 1.97 | 3.46 | 4.96 |
| Cash burn, млн ₽ | -1.37 | -2.06 | -2.91 | -2.85 | -3.00 | -3.00 | -2.27 | -1.05 | 0.00 | 0.00 | 0.00 | 0.00 |
| Cumulative cash, млн ₽ | -1.37 | -3.43 | -6.34 | -9.19 | -12.19 | -15.19 | -17.46 | -18.51 | -18.05 | -16.09 | -12.62 | -7.67 |

Break-even: 9 клиентов, месяц EBITDA>0: M9. Startup capital to BE: 21.3 млн ₽.


### Пессимистичный scenario

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0.98 | 1.96 | 2.92 | 3.86 | 4.79 |
| MRR, млн ₽ | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.30 | 1.27 | 2.55 | 3.80 | 5.02 | 6.22 |
| COGS, млн ₽ | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.53 | 0.52 | 1.04 | 1.55 | 2.05 | 2.54 |
| Gross profit, млн ₽ | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.77 | 0.75 | 1.51 | 2.25 | 2.97 | 3.68 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% | 59.2% |
| Fixed costs, млн ₽ | 1.37 | 2.06 | 2.91 | 3.62 | 4.53 | 4.80 | 5.20 | 5.40 | 5.40 | 5.40 | 5.40 | 5.40 |
| EBITDA, млн ₽ | -1.37 | -2.06 | -2.91 | -3.62 | -4.53 | -4.80 | -4.43 | -4.65 | -3.89 | -3.15 | -2.43 | -1.72 |
| Cash burn, млн ₽ | -1.37 | -2.06 | -2.91 | -3.62 | -4.53 | -4.80 | -4.43 | -4.65 | -3.89 | -3.15 | -2.43 | -1.72 |
| Cumulative cash, млн ₽ | -1.37 | -3.43 | -6.34 | -9.96 | -14.49 | -19.29 | -23.72 | -28.37 | -32.26 | -35.41 | -37.84 | -39.55 |

Break-even: 8 клиентов, месяц EBITDA>0: не достигнут за M1-M12. Startup capital to BE: 45.5 млн ₽.


## 2) Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### Unit waterfall на 1 клиента в месяц

| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 1 300 000 | контрактовая выручка |
| COGS | 530 000 | inference, cloud, HITL, CSM, support, security |
| Gross profit | 770 000 | gross margin 59,2% |
| CAC amortization / мес | 125 508 | 1 506 100 / 12 |
| Contribution after CAC | 644 492 | gross profit после нормализованного acquisition load |
| Fixed cost load / client at BE | 716 625 | 5 733 000 / 8 клиентов |
| EBITDA / client at BE | -72 133 | на ровном пороге 8 клиентов до налогов почти в ноль |
| EBITDA / client at 9 clients | 133 000 | 6 930 000 - 5 733 000 = 1 197 000 / 9 |

### Net after tax на уровне компании при steady-state 9 клиентах

| Налоговый режим | Выручка, млн ₽/мес | EBITDA, млн ₽/мес | Налоговая логика | Net, млн ₽/мес |
|---|---:|---:|---|---:|
| УСН 6% | 11,70 | 1,197 | 6% с выручки | 0,495 |
| IT-льгота 3% | 11,70 | 1,197 | 3% с выручки при аккредитации Минцифры | 0,846 |
| ОСНО 20% | 11,70 | 1,197 | 20% налог на прибыль; НДС 20% учитывать отдельно по cash flow | 0,958 |

Вывод: для этого кейса операционно оптимален режим **IT-льготы 3%**, если компания проходит аккредитацию и профиль выручки; fallback для раннего этапа, если льгота недоступна, это **УСН 6%** до упора в лимиты режима.

## 3) Cash flow: startup_capital_to_bep_rub

| Scenario | Минимум cumulative cash, млн ₽ | Buffer 15%, млн ₽ | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Base | 29,99 | 4,50 | 34 490 621 |
| Optimistic | 18,51 | 2,78 | 21 291 746 |
| Pessimistic | 39,55 | 5,93 | 45 484 107 |

Практический ориентир на raise: **35-45 млн ₽**, чтобы пережить procurement lag, задержки оплат и донабор команды.

## 4) Налоговая модель

- **Страховые взносы:** заложены как ~30% к ФОТ и уже входят в FOT/fixed costs из `04-economics.md`.
- **УСН 6%:** самый простой режим для раннего этапа, но налог берётся с выручки, поэтому при просадке margin сильнее давит на cash burn.
- **IT-льгота / 3%:** применима при аккредитации Минцифры и соблюдении профильной доли IT-выручки; в модели это лучший баланс для PnL и cash.
- **ОСНО / 20% прибыль + НДС 20%:** в PnL налог на прибыль считаю от EBIT/EBT, а **НДС 20%** трактую как cash-flow фактор, если компания не может полностью зачесть input VAT по подрядчикам и cloud.
- Для фонда базовый underwriting имеет смысл вести в двух срезах: **УСН 6% как downside**, **IT-льгота 3% как target case**.

## 5) Break-even по client count и по месяцам

| Scenario | Churn / мес | Fixed cost run-rate, млн ₽/мес | Break-even client count | Break-even month |
|---|---:|---:|---:|---|
| Base | 1,0% | 5,733 | 8 | M12 |
| Optimistic | 0,5% | 6,400 | 9 | M9 |
| Pessimistic | 2,0% | 5,400 | 8 | не достигнут за M1-M12 |

Интерпретация:
- **Base:** компания доходит до operating break-even к концу первого года.
- **Optimistic:** ускоренный pipeline и более низкий churn сдвигают break-even в **M9**.
- **Pessimistic:** при более медленном наборе и churn 2% нужен либо второй год runway, либо сокращение fixed-cost base.

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## 1) Sensitivity analysis: EBITDA через 12 мес

База для сравнения: `M12 EBITDA = 0,25 млн ₽` из SECTION A. Для sensitivity беру те же fixed costs и клиентскую базу к M12, а изменяю один драйвер за раз.

| Сценарий | Ключевое изменение | EBITDA @M12, млн ₽/мес | Комментарий |
|---|---|---:|---|
| Base | Без изменений | 0,25 | На грани положительной EBITDA |
| Sens1 | CAC x2 | -1,26 | Доп. acquisition burn ~1,51 млн ₽/мес съедает весь operating profit |
| Sens2 | Churn x2 | 0,06 | База почти обнуляется, т.к. клиентская масса к M12 проседает |
| Sens3 | Price -30% | -2,79 | ARPU падает до 0,91 млн ₽, gross profit на клиента сжимается до ~0,38 млн ₽ |

Вывод: модель **гораздо более чувствительна к price compression и CAC inflation**, чем к умеренному ухудшению churn в первый год. Это значит, что главный moat должен быть в outcome-based ROI и в дешёвом доступе к distribution, а не только в модели/продукте.

## 2) Monte Carlo Lite — Confidence Intervals

### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 083 000 | 1 506 100 | 2 400 000 | [T4], stress-case inference |
| Monthly churn, % | 0,5% | 1,0% | 2,0% | [T4], [E6] |
| ARPU, ₽/мес | 910 000 | 1 300 000 | 1 500 000 | [T2], [T4] |
| Conversion rate lead→paid, % | 0,3% | 0,8% | 1,5% | [T4], funnel inference |
| Time-to-hire, мес | 1,0 | 1,5 | 3,0 | [T4] |

### Метод упрощённой симуляции

Вместо полного кода использую **9 комбинаций** на базе min/mode/max для CAC, churn и ARPU, а conversion + time-to-hire применяю как поправку к скорости набора клиентов. Это даёт рабочие приближения для p10/p50/p90 на M24.

Ключевые допущения:
- fixed costs steady-state: **5,733 млн ₽/мес**; [T4]
- gross profit / клиент / мес: `ARPU - 530 000 ₽ COGS`; [T4]
- p50 соответствует текущему base motion: примерно **1 новый платящий клиент/мес** после ramp-up; [T4]
- p10 закладывает slower hiring + weaker conversion, поэтому эффективный net-add ниже;
- p90 закладывает faster hiring + better conversion, поэтому net-add выше.

### Результат: confidence intervals

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -3 000 000 | 7 600 000 | 20 700 000 | 23 700 000 |
| CAC payback, мес | 6,3 | 2,0 | 1,1 | 5,2 |
| LTV/CAC | 7,9x | 51,1x | 149,2x | 141,3 |
| Cash runway, мес | 11 | 16 | 25 | 14 |

Интерпретация правил:
1. **p10 EBITDA < 0** → да, модель имеет downside до отрицательной EBITDA, значит автоматически срабатывает **kill criterion #1**.
2. **p50 EBITDA < 500К ₽/мес** → нет, медиана сильно выше порога, значит median-case gate проходит.
3. **p90 / p10 > 10x** → из-за отрицательного p10 ratio теряет смысл, но practically dispersion экстремальная: диапазон от отрицательной EBITDA до >20 млн ₽/мес. Это требует **downside haircut к score**.
4. **Range width по LTV/CAC > 8** → да, **141,3**. Модель хрупкая, ключевая нестабильность сидит в pricing, churn и acquisition efficiency.

### Что означает p10/p50/p90 для фонда
- **p10**: кейс превращается в services-heavy insurer vendor с тяжёлым burn, без права на ошибку в цене и go-live.
- **p50**: компания выглядит инвестиционно допустимой, но только при сохранении enterprise pricing и низкого churn.
- **p90**: upside сильный, если команда быстро стандартизирует внедрения и превращает pilots в повторяемый workflow layer.

## 3) Competitor deep-dive

### 3.1. Топ-3 западных

> Оценки долей ниже — **inference**, не публичный аудит. Я оцениваю их по установленной базе, brand power, breadth platform и роли в claims-core / claims-automation stack.

| Компания | Почему это competitor | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Guidewire ClaimCenter | Де-факто reference core claims platform для P&C | очень сильный enterprise brand, end-to-end claims lifecycle, глубокая installed base, AI inside workflow [W1] | тяжёлые внедрения, дорогой TCO, слабый fit для быстрого overlay-пилота | 25-35% западного enterprise claims-core сегмента | можно зайти как overlay/HITL outcome layer быстрее и дешевле, не требуя rip-and-replace |
| Duck Creek Claims | Современный cloud claims stack с сильным FNOL/triage | cloud-native motion, configurable workflows, AI-enabled decision support, прозрачная claims analytics [W2] | тоже platform-first, нужен длинный enterprise цикл, слабее как managed ops vendor | 10-15% | можно продавать не core, а managed claims throughput + локальную интеграцию |
| Sapiens ClaimsPro | Сильный rules-driven claims automation для P&C | auditable workflow, automated assignment, cloud claims automation [W3] | меньше ecosystem power, чем у Guidewire, и тоже ориентирован на core/workflow replacement | 5-10% | у нас лучше wedge для «узкого painful процесса» и сильнее human-in-the-loop локально |

### 3.2. Топ-5 российских / локальных substitutes

> Здесь конкурируют не только прямые twins, но и **adjacent substitutes**, через которые страховщик уже сегодня закрывает бюджет intake, OCR, routing, contact-center и digital claims.

| Компания | Источник | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| MAINS Lab | Skolkovo пишет про ИИ-автоматизацию урегулирования и продукт «Секунда»; также кейс с Ингосстрахом [W4][W5] | самый близкий локальный category fit, уже работает в страховании, понимает photo appraisal и settlement flow | уже заметно привязан к конкретным use-cases, риск project-heavy delivery | 5-10% локального insurtech-automation слоя | мы можем быть шире, чем damage-assessment, и идти в полный FNOL + triage + routing + HITL ops |
| Naumen | Habr/Naumen подтверждает крупный enterprise contact-center stack и сложные внедрения [W6][W7] | сильная installed base в enterprise CX, зрелый workflow, омниканал, доверие крупных корпораций | claims outcome не core-DNA, больше horizontal platform, чем vertical claims engine | 15-20% adjacent automation budget у крупных enterprise-команд | наш плюс, вертикальный ROI по claims, а не generic contact-center automation |
| CraftTalk | Habr Career: platform with AI bots, KMS, омниканал; среди клиентов указан Ингосстрах [W8] | быстро закрывает intake/support/chat-слой, low-friction старт, enterprise references | слабее в core claims orchestration, fraud, triage depth и SLA-управлении процессом | 5-10% digital intake/chat budget | наш плюс, продаём whole-claim outcome, а не бот/чат-слой |
| Smart Engines | Habr: позиционируется как лидер российского OCR-рынка документов [W9] | сильный document OCR, verification, on-prem / импортозамещение-friendly stack | это компонент, а не claims-ops платформа | 5-10% document-recognition budget | можем использовать OCR как commodity-кирпич и забирать более высокую value-layer маржу |
| Content AI | Habr: сильный портфель OCR/NLP/document automation [W10] | сильная документная экспертиза, enterprise-ready automation | опять же, это horizontal document layer, а не end-to-end claims operator | 5-10% document automation budget | наш плюс, orchestration, decisioning и measurable KPI по урегулированию |

### Конкурентный вывод

Западные игроки сильнее в **core platform**. Российские игроки сильнее в **отдельных кирпичах**: OCR, contact-center, чат, point automation. Значит, лучшая позиция для нового кейса, это не «заменить Guidewire», а стать **claims outcome overlay** над legacy/core + локальными AI-компонентами.

## 4) Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного CTO/ML вовремя | med | высокий | time-to-hire > 3 мес, офферы отклоняются | founder-led recruiting, advisor bench, interim fractional CTO |
| Operational | LLM/OCR quality не держит production SLA | med | высокий | handoff rate > 40%, QA error rate растёт | fallback rules, human review queue, vendor redundancy |
| Operational | Зависимость от внешних LLM API и latency | high | высокий | latency spikes, cost/token растёт, rate limits | multi-model routing, локальные модели для PII, кеширование |
| Market | Страховщики не покупают category, только point tools | high | высокий | discovery → pilot conversion < 20% | продавать через ROI-кейсы, не через «AI claims ops» messaging |
| Market | Price compression из-за горизонтальных vendors | high | высокий | скидки > 25%, pushback на platform fee | outcome-based pricing, narrow wedge, reference cases |
| Market | Incumbent core vendor закрывает тот же use-case roadmap'ом | med | высокий | buyer просит «подождать релиз текущего вендора» | идти в faster deployment, managed ops, low-risk pilot |
| Regulatory | 152-ФЗ / data residency не позволяют облачную обработку | high | высокий | security review > 60 дней, требование on-prem | hybrid/on-prem deployment, segregated storage, DPA by default |
| Regulatory | 115-ФЗ / AML-процедуры усложняют обработку документов и проверок | med | средний | legal/compliance блокируют scope | compliance-by-design, audit logs, explainability |
| Regulatory | Ограничения на иностранные SaaS/мессенджеры | high | средний | запрет Telegram/foreign tools в pilot scope | делать core workflow вне мессенджеров, локальный стек коммуникаций |
| Financial | Runway съедается длинным pilot-to-cash циклом | high | высокий | DSO > 75 дней, paid go-live сдвигается > 2 мес | milestone billing, upfront pilot fee, reserve cash buffer |
| Financial | Ослабление рубля повышает cost base по LLM/cloud | high | средний | USD/RUB скачет, gross margin падает | RUB-pricing clauses, pre-buy capacity, local substitutes |
| Financial | Инфляция ФОТ и рост налоговой нагрузки | med | средний | зарплатные ожидания +15-20% г/г | lean hiring, more automation, variable comp mix |
| Black swan | Резкое ужесточение санкций на AI/cloud vendors | med | высокий | vendor notices, отключение API, billing failures | multi-vendor stack, self-hosted fallback, sovereign infra |
| Black swan | Отключение ключевого LLM-провайдера | med | высокий | деградация inference / no access | резервная модельная матрица, open-source fallback |
| Black swan | Военный/макро-шок, freeze IT-бюджетов страховщиков | med | высокий | заморозка пилотов, procurement freeze | focus on hard-ROI use-cases, shorten payback, preserve cash |

## 5) Kill conditions через 6 месяцев

1. **Median-case economics fail:** если обновлённый p50 EBITDA forecast на M24 падает **ниже 500 тыс. ₽/мес**, продолжать нельзя.
2. **Insolvency risk visible:** если p10 EBITDA forecast остаётся **< 0** и фактический runway падает **ниже 9 месяцев**, продолжать нельзя.
3. **Go-to-market не повторяется:** если за 6 месяцев нет хотя бы **2 paid pilots или 1 полноценного annual contract**, а discovery→pilot conversion остаётся **< 20%**, история подтверждает отсутствие repeatable wedge.

## 6) Итоговый вывод SECTION B

Кейс остаётся **интересным, но хрупким**. P5/P6A выглядел очень сильным на точечной unit-экономике, однако P6B показывает, что downside концентрируется в трёх местах:
- enterprise pricing must hold;
- CAC не должен уходить в x2 без пропорционального роста win rate;
- архитектура должна переживать требования локального compliance и возможное отключение внешних AI vendors.

Для фонда это не «безопасный SaaS compounder», а **high-variance vertical AI bet**. Продолжать стоит только при дисциплине: on-prem/hybrid readiness, узкий claims wedge, платные пилоты, и жёсткий контроль CAC/payback.

### Sources
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-native-claims-ops-dlya-strahovshchikov/02-demand.md
- [T4] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-native-claims-ops-dlya-strahovshchikov/04-economics.md
- [E6] Bessemer Venture Partners, churn benchmarks: https://www.bvp.com/atlas/state-of-the-cloud-2024
- [W1] https://www.guidewire.com/en/products/core-products/insurancesuite/claimcenter-claims-management-software
- [W2] https://www.duckcreek.com/product/claims-management-software/
- [W3] https://sapiens.com/us/property-and-casualty/claimspro/
- [W4] https://sk.ru/news/mains-lab-poluchila-grant-v-razmere-20-mln-rubley-ot-fsi/
- [W5] https://sk.ru/news/ingosstrah-sovmestno-c-mains-lab-vnedrili-ii-v-process-soglasovaniya-uslug-po-dms/
- [W6] https://career.habr.com/companies/naumen
- [W7] https://habr.com/ru/companies/naumen/articles/473710/
- [W8] https://career.habr.com/companies/crafttalk
- [W9] https://habr.com/ru/companies/smartengines/news/762606/
- [W10] https://habr.com/ru/companies/contentai/profile/

<!-- P6B-DONE -->

---

# FILE: 06-verdict.md

[FINTECH] AI-native claims ops для страховщиков — NEAR-PASS: 65/100 | EBITDA base=1197К₽/мес через 13 мес | LTV/CAC=51,1x | Ключевое преимущество: дорогой claims-workflow с measurable ROI | Главный риск: спрос в РФ не формулируется как самостоятельная категория.

# 06-verdict

sector: FINTECH

## Investment committee verdict
- **Вердикт:** NEAR-PASS
- **Score:** 65/100
- **Raw score:** 98/150
- **Пороговое решение:** score ниже 70, поэтому кейс уходит в `rejected/`, несмотря на прохождение EBITDA-gate.
- **Почему не approve:** экономика и EBITDA-потенциал сильные, но investment-grade запас прочности съедают LOW category demand в РФ, weak moat и enterprise-heavy GTM.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 77 000 000 ₽ |
| fully_loaded_cac_rub | 1 506 100 ₽ |
| LTV/CAC | 51,1x |
| CAC payback | 1,16 мес по MRR / 1,96 мес по gross profit |
| GM% | 59,2% |
| contribution_margin_rub_month | 770 000 ₽ на клиента |
| company_ebitda_rub_month (base, 9 клиентов) | 1 197 000 ₽/мес |
| company_ebitda_potential_rub_month (50 клиентов) | 32 767 000 ₽/мес |
| clients_to_500k_ebitda | 9 |
| months_to_500k_ebitda | 13 |
| break-even clients | 8 |
| startup_capital_to_bep_rub | 45 000 000 ₽ |
| SAM РФ | 620 000 000 ₽ |
| SOM Y1 | 18 600 000 ₽ |
| SOM Y3 | 62 000 000 ₽ |

## Оценка
Source tier balance: T1=4, T2=7, T3=0, weighted=2.36. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC = 51,1x», «CAC payback = 1,16 мес», «Contribution Margin = 59,2%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «EBITDA > 500k/mo достижима уже на 9 клиентах», «M13 или 9 клиентов». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «Demand API ... LOW, score 0, HH=0», при этом «SAM ... 620 млн ₽»; применён штраф за tier-balance. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | Есть workflow wedge, но «новый игрок легко превращается в подрядчика без platform power». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | «high» по 152-ФЗ/data residency, price compression и LLM/cloud dependence делают кейс high-variance. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | Есть 10 named targets и channel-fit, но «до первой оплаты цикл реалистично занимает 6-9 месяцев». |

**Normalized score = round((98 × 100) / 150) = 65/100.**

## Почему итог именно такой
Кейс проходит по клиентской экономике и company EBITDA, но это не достаточно для approve. Инвесткомитету нужен повторяемый локальный спрос и защищаемый moat. Здесь спрос в РФ подтверждён как pain/budget, но не как отдельная категория. Вдобавок moat остаётся средним: core claims systems, OCR, contact-center и bot vendors уже закрывают куски value chain. Поэтому фондово это near-pass, а не approve.

## FULL business process из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | ICP-лист и research страховщиков | SDR | HH/СПАРК/CRM/manual research | 2 ч | 2 000 | средняя |
| 2 | Первый outreach | SDR | email, phone, Telegram/мессенджер where allowed | 30 мин | 500 | средняя |
| 3 | Follow-up sequence 5-7 касаний | SDR | CRM + sequencing | 10 дней | 4 000 | высокая |
| 4 | Discovery call | AE + founder | Meet/Zoom | 1 ч | 12 000 | низкая |
| 5 | Qualification + ROI hypothesis | AE | CRM, ROI sheet | 1 день | 8 000 | средняя |
| 6 | Demo claims workflow | AE + solutions | demo env | 1,5 ч | 15 000 | средняя |
| 7 | Security / legal / architecture review | CTO + AE | docs, DPA, ИБ пакет | 2-4 недели | 80 000 | низкая |
| 8 | Pilot scoping | CTO + PM + buyer | workshop | 1 неделя | 60 000 | низкая |
| 9 | Pilot integration | backend + ML + DevOps | API, OCR, queues, storage | 4-6 недель | 220 000 | средняя |
| 10 | Pilot ops with HITL | CSM + claims ops analyst | internal console | 1 месяц | 140 000 | средняя |
| 11 | KPI review and business case | AE + founder | BI/report | 1 неделя | 20 000 | средняя |
| 12 | Procurement and contract signing | AE + founder + legal | CRM + docs | 2-6 недель | 45 000 | низкая |
| 13 | Go-live | CSM + CTO | production stack | 1 неделя | 35 000 | средняя |
| 14 | Monthly service delivery | CSM + ML + support | platform + ops queue | ongoing | 530 000 | средняя |
| 15 | Invoice and payment collection | finance ops | 1C/банк/ЭДО | 5 дней | 8 000 | высокая |

## Team table
| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|
| CEO | 1 | 700 000 | 0 | 0 | 910 000 |
| CTO / Tech Lead | 1 | 600 000 | 2,0 | 2,0 | 780 000 |
| Senior Backend | 2 | 400 000 | 1,5 | 1,5 | 1 040 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2,0 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1,0 | 455 000 |
| Frontend | 1 | 300 000 | 1,0 | 1,0 | 390 000 |
| SDR | 1 | 160 000 | 0,75 | 1,0 | 208 000 |
| AE | 1 | 350 000 | 1,5 | 2,5 | 455 000 |
| Customer Success | 1 | 250 000 | 1,0 | 1,0 | 325 000 |
| **Итого** | **10** |  |  |  | **5 213 000** |

## Moat
### 7-factor moat framework
| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент почти не улучшает продукт для остальных, кроме косвенного playbook learning. |
| Switching costs | 2 | Интеграции, workflow и обученная claims-команда создают средние switching costs. |
| Scale economies | 2 | COGS и HITL можно ужимать с ростом объёма, но не до pure software уровня. |
| Proprietary data / model advantage | 1 | Возможен learning loop, но в кейсе нет доказанного локального датасета или размера corpus. |
| Regulatory moat | 2 | On-prem/hybrid и compliance-by-design полезны, но это скорее hurdle, чем уникальная лицензия. |
| Brand / distribution | 1 | Новый игрок стартует без сильного enterprise insurance brand. |
| Embedded workflow | 3 | Если продукт входит в FNOL/triage/document orchestration, он глубоко сидит в ежедневном процессе клиента. |

**Moat score = round((12 × 25) / 21) = 14/25.**

Вывод: moat средний, не weak-moat по формальному порогу, но недостаточно сильный для premium multiple. Главный дефицит, отсутствие network effects, слабая brand/distribution база и недоказанное proprietary data advantage.

## GTM: 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | СОГАЗ | Крупный non-life поток и высокий cost-to-serve в claims, значит FNOL/triage ROI максимален. | email decision-maker + отраслевые конференции по страхованию | 1 500 000 ₽/мес |
| 2 | РЕСО-Гарантия | Массовое автострахование и документы создают боль в intake и routing. | founder-led outreach директору по урегулированию | 1 300 000 ₽/мес |
| 3 | Ингосстрах | Уже внедрял AI в adjacent insurance workflows, значит восприимчив к claims automation. | партнёрство + warm intro через insurtech ecosystem | 1 500 000 ₽/мес |
| 4 | АльфаСтрахование | Сильный digital и большой объём клиентских обращений, что повышает ценность throughput layer. | email decision-maker / digital transformation lead | 1 300 000 ₽/мес |
| 5 | Росгосстрах | Большой legacy claims volume и вероятный backlog в документах и сервисе. | конференция + account-based outreach | 1 200 000 ₽/мес |
| 6 | ВСК | Claims-heavy non-life lines, где можно продать SLA и снижение ручной обработки. | partnership с интегратором / страховым консультантом | 1 100 000 ₽/мес |
| 7 | Ренессанс Страхование | Digital-first позиционирование упрощает pilot wedge в FNOL/document orchestration. | email decision-maker + LinkedIn/мероприятия | 1 200 000 ₽/мес |
| 8 | Согласие | Средне-крупный insurer, где проще зайти через один mass-claims flow как design partner. | founder outreach + pilot offer | 900 000 ₽/мес |
| 9 | МАКС | Подходит для более узкого pilot motion по motor/property claims. | отраслевые контакты + direct email | 850 000 ₽/мес |
| 10 | Т-Страхование | Высокая digital-культура и потенциальная готовность тестировать outcome-layer быстрее incumbents. | warm intro + product/ops pitch | 1 000 000 ₽/мес |

### GTM realism verdict
Плюс: LTV/CAC и payback очень сильные, 10 named targets есть, buyer list конкретный. Минус: «до первой оплаты цикл реалистично занимает 6-9 месяцев», а security/legal review и pilot integration тяжелы. Следовательно, GTM выглядит реалистичным только как founder-led enterprise motion с design partners и узким wedge, не как масштабируемый быстрый sales machine.

## Top-3 risks
| Риск | Вероятность | Impact | Почему в top-3 |
|---|---|---|---|
| Category demand low / message-market fit слабый | high | высокий | Demand API = LOW, HH=0, поэтому продавать придётся через ROI боли, а не готовую категорию. |
| Price compression и commodity risk | high | высокий | Горизонтальные OCR/contact-center/voice vendors уже закрывают часть value chain и давят на pricing. |
| Regulatory + LLM dependency | high | высокий | 152-ФЗ/data residency, запрет иностранных мессенджеров и зависимость от external LLM/cloud сужают deployment options. |

## Proof points required for APPROVED
1. 2 paid pilots или 1 полноценный annual contract в течение 6 месяцев.
2. Discovery→pilot conversion не ниже 20% на ICP top insurers.
3. Pilot доказывает сокращение time-to-assignment или cost-per-claim минимум на 20%.
4. Hybrid/on-prem deployment проходит security review без критического re-architecture.
5. Повторяемый ACV не ниже 1,0 млн ₽/мес без глубокой кастомной команды под каждого клиента.

## LTV Upside Calculator
Так как кейс получает **NEAR-PASS**, нужен путь в approve через улучшение доказательств, а не через ухудшение economics.

### Какие рычаги переводят 65/100 в 70+
| Рычаг | Текущее значение | Цель для approve | Эффект на score |
|---|---:|---:|---|
| Market evidence | LOW category demand, HH=0 | 2-3 paid pilots + публичные локальные кейсы | +3-4 балла к критерию #3 |
| Moat | 14/25 | доказанный proprietary claims dataset + 2 интеграционных шаблона | +2-3 балла к критерию #4 |
| GTM | 17/25 | 10 таргетов конвертируются в 2 LOI/paid pilots | +2 балла к критерию #6 |
| Execution risk | high | on-prem package и резервный local model stack | +1-2 балла к критерию #5 |

### Минимальный путь к approve
Если за 6 месяцев компания докажет 2 paid pilots, сохранит ACV 1,0-1,3 млн ₽/мес и закроет compliance gap, то score может подняться примерно с 65 до 71-73 без пересборки экономики.

## Финальный комитетский вывод
Это сильный candidate для watchlist и partner-backed pilot strategy, но пока не для approve. Фундаментальная причина отказа не в цифрах P&L, а в том, что локальный спрос и moat не дотягивают до investment-grade certainty. Кейс надо дорабатывать через доказанный design-partner motion в top insurers, а не через broad-market launch.

---
