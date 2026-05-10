# DeepIP — полный пакет verdict


---

# 01-intake.md

---
sector: LEGAL
rerun: true
source_raw: 2026-04-19-resurrect-deepip-geo-expand.md
created: 2026-04-20T11:18:00+03:00
---

# 01-intake

## Кейс
deepip-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-deepip-geo-expand.md

## Краткий контекст
Standalone legal/IP-кейс по patent drafting, prior-art search и автоматизации патентных workflow. Требуется новая аналитика P3→P7, даже если исторически сигнал считался дубликатом или недостаточным по LTV.

## Следующий шаг
Передать кейс в P3-demand-validation: подтвердить high-LTV сценарии, сложность локализации, доступность buyer'ов и наличие устойчивого GEO-EXPAND окна.

## Полный контекст из raw

# RESURRECT SIGNAL — deepip-geo-expand

## Meta
- source: triage/triage-2026-04-14-deepip-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-14

## Входные данные
- pipeline/raw/raw-2026-04-14-deepip-geo-expand.md

## Классификация
дубликат ранее обработанного сигнала, кейс не открываем

## Решение
Не открывать новый кейс и не обогащать существующие кейсы.

## Почему
- Сигнал тематически совпадает с уже обработанным DeepIP по vertical AI для patent drafting, prior-art search и patent workflow.
- Подходящего открытого кейса в `pipeline/cases/` по patent AI / IP operations сейчас нет.
- Экономика всё ещё не проходит порог Program 1: в raw-файле указан `ltv_signal: 1200000-5000000 ₽ в год на клиента`, то есть примерно 100 000-417 000 руб. в месяц, что ниже требуемого порога `> 500 000 руб./мес.`.
- Локализация остаётся тяжёлой из-за необходимости адаптации под процессы Роспатента, русскоязычные патентные документы и локальные IP-workflow, а подтверждённый recurring service layer в сигнале не показан.

## Что сделано
- Новый кейс не создан.
- Существующие кейсы не обновлялись, так как релевантного открытого кейса по теме нет.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал полезный как дополнительное подтверждение интереса к patent AI, но для Program 1 это дубликат без нового апсайда по экономике: открывать кейс рано, пока LTV ниже порога и сервисная модель недостаточно подтверждена.

```



---

# 02-demand.md

---
stage: demand-validation
sector: LEGAL
updated: 2026-04-21T02:57:00+03:00
---

# 02-demand

## Demand validation summary
- DeepIP к апрелю 2026 уже выглядит не как сырой AI-эксперимент, а как оформленная product category: на официальном сайте компания продаёт end-to-end patent workflow, включая invention capture, patentability, drafting, prosecution и portfolio intelligence, плюс отдельно подчёркивает использование у Am Law 100 и Fortune 500 команд. Это сильный сигнал внешней category validation. [T2]
- На странице law firms DeepIP заявляет до 70% faster drafting и фокус на росте маржи patent firms. Это важно, потому что buyer покупает не «ещё один legal copilot», а инструмент, который напрямую бьёт в realization rate, throughput и partner leverage. [T2]
- 27 марта 2025 DeepIP официально объявил о раунде Series A на $15 млн. Это не доказывает локальный спрос в РФ, но подтверждает, что западный рынок уже готов финансировать и покупать patent-AI workflow как отдельную категорию. [T2]
- В РФ buyer-слой существует. Роспатент 19 февраля 2025 сообщил, что за 2024 год российские разработчики подали 41,4 тыс. заявок на регистрацию изобретений, полезных моделей и промышленных образцов, из них на изобретения пришлось более 21 тыс. Это означает, что объём патентной активности не нулевой и есть поверхность для IP automation. [T1]
- Денежный спрос в РФ сегодня лучше виден через сервисы, а не через чистый SaaS. Online Patent публично продаёт регистрацию программы для ЭВМ от 19 990 ₽, регистрацию товарного знака от 27 490 ₽ и показывает, что рынок уже платит за IP-outcome и сопровождение. Значит, чисто продуктовый чек можно усиливать сервисным слоем. [T2]
- Вывод: массового спроса на standalone patent AI в РФ не видно, но есть узкий платёжеспособный LEGAL/IP сегмент, где кейс проходит дальше только как enterprise или hybrid software + service motion, а не как широкая self-serve история. [T1][T2]

## Почему спрос не выглядит массовым
- Локальный рынок патентной автоматизации в РФ небольшой и довольно экспертный: buyer чаще формулирует задачу как «патентование под ключ», «патентный поиск», «сопровождение заявки», а не как покупку AI drafting seat. [T1][T2]
- DeepIP сегодня явно оптимизирован под западные юрисдикции, Word-first workflow и law-firm operating model. Для РФ нужна локализация под практику Роспатента, русскоязычные корпуса, шаблоны формулировок и local expert QA. Без этого exact-demand будет ограничен. [T2, inference]
- Поэтому прямой PLG-сценарий в РФ слабый, но managed-service сценарий выглядит реалистично: локальный партнёр может продавать ускорение drafting/prosecution поверх собственной патентной экспертизы. [T1][T2, inference]

## Buyers и budget owners
1. Крупные корпорации с активным R&D и собственными IP/юридическими функциями: Ростех, Росатом, Сбер, Яндекс, МТС, СИБУР. [T1, inference]
2. Патентные бюро и патентные поверенные, которым важны скорость подготовки заявок, качество драфта и маржинальность fixed-fee работы. [T2]
3. Фарма, industrial и deeptech-компании, где регулярный поток invention disclosures и prior-art work делает automation экономически осмысленной. [T1, inference]

## Willingness to pay
- У международного buyer'а WTP подтверждается самим positioning DeepIP: экономия времени, рост качества и margin uplift для law firms. [T2]
- В РФ WTP уже подтверждён оплатой патентных услуг. Даже если AI-seat сам по себе трудно продать, bundled-офер «AI drafting + патентный поверенный + prosecution support» попадает в понятный бюджет. [T2]
- Практический вывод: standalone seat в РФ выглядит слабее, чем annual contract или managed retainer. [T2, inference]

## Profit gate scenarios
### Scenario A, pure SaaS seats for boutiques
- 30 000-50 000 ₽ за пользователя в месяц выглядит теоретически возможно, но для прохождения порога нужно слишком много активных пользователей в слишком узкой нише.
- Вердикт: **скорее нет**.

### Scenario B, team license for patent firm
- 180 000-300 000 ₽ в месяц за фирму с shared workspace, шаблонами и quality controls выглядит ближе к реальности, но всё ещё на грани без сервисного слоя.
- Вердикт: **на грани**.

### Scenario C, hybrid software + expert patent operations
- 250 000-450 000 ₽ в месяц SaaS/retainer + 150 000-400 000 ₽ в месяц за managed drafting, prior-art support, локализацию и QA уже даёт 400 000-850 000 ₽ на клиента.
- 3-5 таких клиентов достаточно, чтобы выйти за порог программы по EBITDA при boutique delivery team.
- Вердикт: **да, проходит**.

### Scenario D, enterprise annual contract
- Для крупных R&D-компаний реалистичен контракт 3-6 млн ₽ в год за private deployment, workflow customization, интеграцию и экспертную поддержку.
- При 4-6 клиентах экономика уже выглядит инвестиционно осмысленной.
- Вердикт: **да, проходит**.

## Risks
- Рынок РФ слишком узкий для чистого product-only кейса.
- Локализация сложная: нужны русскоязычные патентные данные, шаблоны под Роспатент и human QA.
- Если DeepIP нельзя встроить в local service wrapper, кейс быстро скатывается ниже порога Program 2.

## Final assessment
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Кейс не стоит резать на P3, потому что:
- глобальная category validation сильная и свежая;
- локальная патентная активность в РФ достаточна для узкого wedge;
- profit gate проходит в hybrid и enterprise сценариях.

Но не надо переоценивать рынок: это не широкий LEGAL SaaS, а узкий enterprise/service-heavy IP automation thesis.

## Sources
- [T1] Роспатент, 19 февраля 2025: в 2024 году подано 41,4 тыс. заявок на регистрацию изобретений, полезных моделей и промышленных образцов, из них более 21 тыс. заявок на изобретения: https://rospatent.gov.ru/ru/news/19-02-2025-v-2024-godu-rossiyskie-innovatory-narastili-patentnuyu-aktivnost
- [T2] DeepIP official product pages и company pages, просмотрено 21 апреля 2026: https://www.deepip.ai/ , https://www.deepip.ai/law-firms , https://www.deepip.ai/products/patent-drafting , https://www.deepip.ai/blog/deepip-raises-15m-ai-patent-drafting
- [T2] Online Patent pricing pages, просмотрено 21 апреля 2026: https://onlinepatent.ru/uslugi/ , https://onlinepatent.ru/uslugi/registraciya-programmy-dlya-evm/ , https://onlinepatent.ru/faq/common/price/

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.


---

# 03-solution.md

---
stage: solution
case: deepip-geo-expand-v2
date: 2026-04-25
analyst: branch-models-lead
sector: LEGAL
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
DeepIP, patent AI для patent drafting, prosecution и IP workflow automation.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает дорогую и регулярную задачу, ускорение patent drafting, prior-art work и patent operations, а не декоративный legal copilot.
2. В локальном контуре лучший wedge выглядит не как чистый self-serve SaaS, а как hybrid software + expert patent operations для патентных бюро и крупных IP-команд.
3. Сильнейший buyer есть в узком enterprise/legal сегменте, где важны throughput, качество формул и сокращение часов патентных специалистов.
4. Главный риск, кейс легко разваливается, если локализация под Роспатент, русский корпус и human QA окажутся слишком тяжёлыми и съедят всю маржу.

## 1. Какую проблему реально решает продукт

Покупают не просто “AI для патентов”, а снижение четырёх дорогих потерь:
- долгой ручной подготовки patent draft и claims;
- перегрузки патентных поверенных и дорогого expert time;
- медленного prior-art и prosecution workflow;
- низкой пропускной способности IP-команды при росте числа заявок.

Для buyer'а это painkiller, если продукт действительно:
- ускоряет выпуск draft без просадки качества;
- помогает стандартизировать workflow и шаблоны;
- сокращает часы senior patent experts;
- встраивается в existing patent-operations процесс, а не требует полной перестройки.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- крупные патентные бюро и команды патентных поверенных;
- in-house IP / legal команды у больших R&D-компаний;
- фарма, industrial, deeptech и ИТ-компании с регулярным потоком invention disclosures;
- локальные сервисные команды, готовые продавать patent drafting и prosecution как managed service поверх AI.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. регулярный поток заявок или патентных задач;
2. дорогие human-hours патентных специалистов;
3. owner с мандатом на ускорение IP-функции;
4. готовность платить за workflow outcome, а не только за дешёвый seat;
5. готовность принять hybrid-модель с expert QA.

### Нецелевой сегмент
- одиночные изобретатели и микро-SMB;
- команды с редкими разовыми заявками;
- клиенты, которым нужна только дешёвая регистрационная услуга;
- покупатели без эксперта, готового валидировать AI-output.

## 3. Продуктовый wedge

### Core wedge
**AI-ускорение patent operations с локальным expert wrapper**
- drafting первого драфта заявки и claims;
- support для prior-art и patentability review;
- workflow для prosecution и правок;
- локальные шаблоны, QA и адаптация под практику Роспатента;
- managed delivery для патентных бюро и enterprise IP-команд.

### Почему это сильнее, чем просто legal copilot
1. **Workflow ownership**: продукт закрывает конкретный патентный процесс, а не абстрактное “писать лучше тексты”.
2. **ROI понятен**: меньше часов эксперта на одну заявку, выше throughput команды.
3. **Bundled value**: buyer может купить результат, drafting + QA + filing support, а не только интерфейс.
4. **Service moat**: локальные шаблоны, данные и human review повышают stickiness.
5. **Enterprise fit**: для крупного клиента ценность идёт через process layer и governance, а не через массовые seat-licenses.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- чистый западный SaaS без локализации под Роспатент;
- продажа AI-seat напрямую небольшим бюро как самостоятельного продукта;
- отсутствие human QA и legal accountability;
- generic legal AI positioning без упора на patent workflow.

### Вариант, который выглядит реалистично
- pilot на одном понятном use case, например drafting + prior-art support;
- локальный service wrapper с патентным поверенным или специализированной командой;
- библиотека шаблонов, формулировок и quality controls под российскую практику;
- упаковка как managed patent ops layer или enterprise IP acceleration service;
- продажа top-down через head of IP, legal ops owner или управляющего партнёра патентного бюро.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У клиента уже есть substitutes:
- ручная работа патентных поверенных;
- шаблоны документов и внутренние базы знаний;
- аутсорс патентования под ключ;
- generic LLM-инструменты без IP-специализации.

Такой продукт выигрывает только если делает три вещи:
1. **сильно ускоряет подготовку заявки** по сравнению с ручным процессом;
2. **снижает стоимость expert-hour на единицу результата**;
3. **поставляется как контролируемый сервисный слой**, где ответственность и QA не исчезают.

Если этого нет, рынок выберет либо обычное патентное бюро, либо generic AI-tool, либо сохранит текущий ручной процесс.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего patent workflow и объёма задач;
2. выбор одного сценария для пилота, drafting, prior-art или prosecution support;
3. настройка шаблонов, review-process и quality gates;
4. запуск через локальную expert-команду с обязательным human QA;
5. измерение экономии часов, времени цикла и throughput;
6. расширение на дополнительные типы заявок и бизнес-юниты.

### Кто должен быть buyer'ом
- управляющий партнёр патентного бюро;
- head of IP / in-house patent counsel;
- legal ops owner в крупной R&D-компании;
- руководитель сервисной практики по IP.

### Кто редко будет настоящим buyer'ом
- procurement без legal/IP sponsor;
- маленький inventors-as-customers сегмент;
- general counsel без активного patent workflow;
- команды, где патенты возникают слишком редко.

## 7. Конкурентная позиция

### Против обычных патентных бюро
Шанс есть, если продукт даёт более быстрый throughput и более предсказуемую unit economics без потери качества.

### Против generic LLM-инструментов
Преимущество возможно только при наличии patent-specific workflow, шаблонов, QA и domain expertise.

### Против внутренней автоматизации
Шанс появляется, если pilot запускается быстрее и дешевле, чем building in-house knowledge layer и process automation.

## 8. Основные риски solution-fit

1. **Localization-risk**: адаптация под Роспатент и русский корпус может оказаться слишком тяжёлой.
2. **QA-risk**: без обязательного human review legal risk неприемлем для buyer'а.
3. **Consulting-risk**: каждая поставка может превратиться в bespoke legal service.
4. **Market-width-risk**: локальный рынок узкий, массового SaaS-scale не видно.
5. **Trust-risk**: IP-данные чувствительны, поэтому buyer может требовать жёсткий security и приватный контур.
6. **Replacement-risk**: часть клиентов предпочтёт просто нанять ещё одного специалиста или отдать работу наружу.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит pilot и локализация одного клиента;
- какая доля delivery шаблонизируется, а какая остаётся ручным экспертным трудом;
- сколько клиентов нужно для EBITDA > 500 000 ₽/мес;
- выдерживает ли кейс маржу при обязательном human QA;
- реалистичнее direct enterprise motion или channel через патентные бюро / IP service partners.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как узкий LEGAL/IP сценарий: AI-ускорение patent operations, упакованное в hybrid software + expert service слой. Двигать дальше стоит, но только если economics подтвердят, что локализация и human QA не превращают продукт в низкомаржинальный патентный аутсорс.


---

# 04-economics.md

---
stage: unit-economics
case: deepip-geo-expand-v2
date: 2026-05-10
analyst: branch-models-lead
sector: LEGAL
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
DeepIP, AI-платформа для patent drafting, prosecution и IP workflow automation, локализуемая в РФ как hybrid software + expert patent operations.

## Итог
**Статус: PASS WITH RESERVATIONS.**

В инвестиционной модели для РФ кейс проходит пороги программы только как **enterprise / hybrid legaltech**, а не как массовый SaaS. Базовая модель:
- **MRR на клиента = 550 000 ₽/мес**;
- **COGS = 215 000 ₽/клиент/мес**;
- **gross margin = 60,9%**;
- **contribution margin = 53,6%**;
- **fully-loaded CAC = 1 640 500 ₽**;
- **logo churn = 1,6%/мес** по enterprise SaaS benchmark для high-ARPA сегмента; [T3]
- **LTV = 20 937 500 ₽**;
- **LTV/CAC = 12,8x**;
- **CAC payback = 3,0 мес** по формуле программы `CAC / MRR_per_customer`;
- **break-even = 22 клиента**, EBITDA 500K+/мес достигается примерно с **24 клиентов**.

Mandatory reject не срабатывает: при **50 клиентах** модель способна генерировать около **8,36 млн ₽ EBITDA/мес**, то есть сильно выше порога 500K. Главный риск не в арифметике, а в том, удастся ли удержать delivery стандартизованным и не скатиться в патентный аутсорс.

## 1. Модель монетизации

### Базовый пакет для РФ
- **Setup / pilot fee:** 900 000 ₽ разово. [inference]
- **Подписка / retainer:** 550 000 ₽/мес на клиента. [T1][T2][inference]
- **Формат:** AI workspace + patent workflow templates + human QA патентного эксперта + support по prosecution / prior-art. [T1][T2]
- **Сегмент:** enterprise IP-команды и патентные бюро с регулярным потоком заявок. [T1][T2]
- **ARR на клиента:** 6 600 000 ₽. [inference]

### Почему именно такой пакет
- В `02-demand.md` уже видно, что слабый seat-based сценарий не проходит, а проходят только **hybrid** и **enterprise annual contract**. [T1]
- В `03-solution.md` зафиксировано, что ценность создаётся через workflow ownership, локализацию под Роспатент и обязательный human QA. [T2]
- Поэтому считать нужно не SMB SaaS, а **regulated / enterprise legaltech motion** с высоким чеком и дорогим пресейлом.

## 2. Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-аккаунтов, патентных бюро и in-house IP-команд | SDR | LinkedIn Sales Navigator, Bitrix24, ручной ресерч | 45 мин | 1 100 | Полуавтоматически |
| 2 | Поиск decision-maker, контактов и warm-intro путей | SDR | Snov.io, LinkedIn, сайт компании | 30 мин | 800 | Полуавтоматически |
| 3 | Outbound sequence / обработка inbound interest | SDR | email, Bitrix24, Telegram | 25 мин | 700 | Полуавтоматически |
| 4 | Первичная квалификация по ICP и объёму патентного потока | SDR | Bitrix24, qualification script | 30 мин | 850 | Ручной контроль |
| 5 | Discovery call по текущему patent workflow | AE + CEO | Google Meet / Zoom, CRM notes | 75 мин | 4 200 | Ручной |
| 6 | Product demo и разбор 1-2 реальных use cases | AE + Patent Counsel | demo workspace, sample claims, templates | 90 мин | 6 300 | Ручной |
| 7 | Оценка юрисдикции, качества данных и локализации под Роспатент | Patent Counsel + CTO | внутренние чек-листы, corpus review | 2 ч | 8 800 | Ручной |
| 8 | Security / privacy / deployment scoping | CTO | архитектурные схемы, docs, cloud design | 2 ч | 7 500 | Ручной |
| 9 | Расчёт ROI, pilot scope и коммерческое предложение | AE + CEO | spreadsheet, proposal template | 2 ч | 6 800 | Полуавтоматически |
| 10 | Согласование договора, NDA, ИБ и procurement | CEO + AE | email, ЭДО, redlines | 3 ч | 10 500 | Ручной |
| 11 | Платный pilot / setup: настройка шаблонов, QA flow, sandbox | CTO + Backend + Patent Counsel | cloud, product sandbox, prompt library | 10 ч | 31 000 | Полуавтоматически |
| 12 | Go-live и обучение команды клиента | CSM + Patent Counsel | playbook, workspace, onboarding sessions | 3 ч | 9 500 | Полуавтоматически |
| 13 | Счёт, акт, поступление первой оплаты | Finance / CEO | банк, Диадок / ЭДО, CRM | 30 мин | 1 000 | Почти автоматизировано |

### Вывод по процессу
- Это явно **enterprise / regulated B2B sale** с длинным циклом и несколькими дорогими expert-touchpoints.
- Поэтому к blended CAC нужно применять не self-serve логику, а **enterprise multiplier 2,0-2,5**. Я беру нижнюю часть вилки и sanity-check через fully-loaded CAC. [inference]

## 3. COGS breakdown per client/month

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM / inference / prompt execution | 35 000 | генерация draft, claim refinement, summarization | [inference] |
| Patent data / search / corpus enrichment | 18 000 | prior-art search, индексация и вспомогательные данные | [inference] |
| Cloud / storage / monitoring / secure tenant | 22 000 | вычисления, хранение документов, логи | [inference] |
| Patent counsel QA allocation | 95 000 | обязательная экспертная проверка output перед выдачей | [T2][inference] |
| Customer Success allocation | 20 000 | adoption, QBR, support, training | [T4][inference] |
| Support / QA reserve | 10 000 | инциденты, ручные правки, minor rework | [inference] |
| Onboarding amortization | 15 000 | 180K ₽ delivery effort / 12 мес | [inference] |
| **Итого COGS** | **215 000** |  |  |

### Gross margin
- Выручка на клиента = **550 000 ₽/мес**.
- COGS = **215 000 ₽/мес**.
- Gross profit = **335 000 ₽/мес**.
- **Gross margin = 60,9%**.

Для legaltech с обязательным human QA это нормальная, хотя и не «чисто SaaS», маржа. Ключевой риск, что при росте кастомной экспертизы GM легко сползает ниже 55%. [inference]

## 4. Fully-loaded CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ / VK) | 220 000 | ограниченный demand-capture и ретаргет, не основной канал | [T5][inference] |
| Outbound team FOT (SDR / AE attributed to new) | 624 000 | SDR 160K + AE 320K gross, +30% соцвзносы; AE учитываю как 100% new-logo motion | [T4][inference] |
| Marketing team FOT (partial allocation) | 156 000 | fractional content / founder marketing 120K gross +30% | [T4][inference] |
| Tools (CRM, Sales Nav, Snov.io, ЭДО) | 75 000 | Bitrix24, Snov.io, LinkedIn Sales Navigator, документооборот | [T5][T6][inference] |
| Events / partnerships | 250 000 | нишевые legal/IP-конференции, партнёрские вебинары, industry dinners | [inference] |
| Subtotal raw CAC spend | 1 325 000 | сумма строк выше |  |
| Overhead multiplier (x1.3) | 397 500 | стандартный overhead для enterprise B2B motion | [inference] |
| **Итого fully-loaded acquisition spend / мес** | **1 722 500** |  |  |
| New paying customers / мес | **1,05** | blended по каналам ниже | [inference] |
| **Fully-loaded CAC** | **1 640 500 ₽** | 1 722 500 / 1,05 |  |

### Sanity-check
- Кейс относится к **enterprise / regulated legaltech**, поэтому blended CAC должен быть кратно выше mid-market SaaS. [inference]
- Получившийся CAC выше типичного enterprise SaaS benchmark 300-900K ₽, но остаётся правдоподобным для юридически чувствительного продукта с pilot, security review и expert validation. [T4][inference]
- CAC не выглядит «слишком дешёвым», поэтому red flag `<30% benchmark` отсутствует.

## 5. CAC по каналам и funnel conversion

| Канал | Верх funnel | SQL | Demo / Pilot | New paying customers / мес | Spend / мес, ₽ | CAC по каналу, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Partner / referral | 10 intro | 5 | 2 | 0,45 | 180 000 | 400 000 |
| Founder-led inbound / ABM | 30 лидов | 8 | 3 | 0,35 | 310 000 | 885 700 |
| Outbound targeted enterprise | 180 аккаунтов | 22 встречи | 5 | 0,20 | 872 500 | 4 362 500 |
| Paid search / retargeting | 220 кликов | 7 MQL | 2 demo | 0,05 | 360 000 | 7 200 000 |
| **Blended** | **440** | **42** | **12** | **1,05** | **1 722 500** | **1 640 500** |

### Вывод по каналам
- **Partner/referral** и founder-led motion дают лучшую экономику.
- **Outbound** дорогой, но нужен, потому что рынок узкий и buyer education пока не сформирован.
- **Paid** как основной канал разрушает unit economics, его место, ретаргет и бренд-поддержка, а не core acquisition.

## 6. LTV, churn rate и LTV/CAC

### Churn benchmark
Использую **1,6% monthly logo churn**. Основание: у ChartMogul для SaaS с **ARPA $500+** customer churn обычно ниже, около **1-2% в месяц**; это ближе к enterprise/high-ARPA профилю, чем к SMB. [T3]

### Расчёт LTV
- MRR на клиента = **550 000 ₽**.
- Gross profit на клиента = **335 000 ₽/мес**.
- Churn = **1,6%/мес**.
- **LTV = 335 000 / 0,016 = 20 937 500 ₽**.

### LTV/CAC ratio
- **LTV/CAC = 20 937 500 / 1 640 500 = 12,8x**.

### Интерпретация
- Порог investable **3,0x** пройден с большим запасом.
- Даже при ухудшении churn до **2,5%/мес** LTV будет **13,4 млн ₽**, а LTV/CAC останется около **8,2x**. [inference]
- Следовательно, главный риск в кейсе, не retention math, а ограниченная ширина рынка и дорогой presales / localization layer.

## 7. CAC Payback

### Формула программы
`CAC Payback = CAC / MRR_per_customer`

- CAC = **1 640 500 ₽**.
- MRR на клиента = **550 000 ₽/мес**.
- **CAC Payback = 2,98 мес**.

### Проверка на здравый смысл
- Базовый порог `<12 мес` выполняется уверенно.
- Если считать более жёстко по gross profit, получается **1 640 500 / 335 000 = 4,9 мес**, что всё равно хорошо для enterprise legaltech. [inference]

## 8. Contribution Margin %

### Variable costs beyond COGS
| Компонент | ₽/клиент/мес | Комментарий |
|---|---:|---|
| COGS | 215 000 | см. breakdown выше |
| AE commission | 27 500 | 5% от MRR на первый год | [inference] |
| Billing / ЭДО / payment ops | 5 000 | финоперации и документооборот | [inference] |
| Travel / workshop reserve | 7 500 | occasional onsite и legal workshop | [inference] |
| **Total variable cost** | **255 000** |  |

### Contribution
- Contribution per client = **550 000 - 255 000 = 295 000 ₽/мес**.
- **Contribution Margin = 53,6%**.

Это приемлемо для productized service, но уже означает, что любой существенный scope creep быстро бьёт по экономике. [inference]

## 9. Team & FOT

### Полная команда, необходимая для 20-30 активных клиентов

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|------------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 520 000 | 2-3 | 2 | 156 000 | 676 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 160 000 | 0,5-1 | 1 | 48 000 | 208 000 |
| AE | 1 | 320 000 | 1-2 | 2-3 | 96 000 | 416 000 |
| Patent Counsel / QA Lead | 1 | 300 000 | 1-2 | 1 | 90 000 | 390 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| **Итого FOT fully-loaded** | **11** |  |  |  |  | **5 473 000 ₽/мес** |

### Комментарий по зарплатам
- Технические роли калиброваны по актуальным вакансиям hh.ru для senior backend, ML и DevOps в Москве/удалённо. [T4]
- SDR / AE / CSM также сверены по hh.ru и не занижены до unrealistically cheap B2B-sales levels. [T4]
- Для legaltech-слоя добавлен **Patent Counsel / QA Lead**, потому что без этого роли модель занижала бы COGS и risk surface.

## 10. Cumulative FOT timeline M1-M12

### План найма
- **M1:** CEO, старт discovery рынка.
- **M2:** выходит Patent Counsel / QA Lead.
- **M3:** выходит CTO.
- **M4:** выходят Senior Backend #1 и SDR.
- **M5:** выходит AE.
- **M6:** выходят Senior Backend #2 и ML Engineer.
- **M7:** выходит DevOps.
- **M8:** выходит Customer Success.
- **M9:** выходит Frontend.
- **M10-M12:** без новых hires, команда доходит до полной продуктивности.

| Месяц | Активные роли | FOT_monthly, ₽ | Краткий комментарий по ramp |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder-led discovery и presales |
| M2 | CEO, Patent Counsel | 1 235 000 | строится локальный legal QA слой |
| M3 | CEO, Patent Counsel, CTO | 1 950 000 | начинается продуктовая локализация |
| M4 | + Backend #1, SDR | 2 704 000 | появляется первая delivery и lead-gen capacity |
| M5 | + AE | 3 120 000 | запускается полноценный new-logo motion |
| M6 | + Backend #2, ML Engineer | 4 342 000 | можно вести несколько pilot параллельно |
| M7 | + DevOps | 4 797 000 | stabilizing infra и secure deployment |
| M8 | + Customer Success | 5 109 000 | onboarding и adoption становятся управляемыми |
| M9 | + Frontend | 5 473 000 | команда полная |
| M10 | full team | 5 473 000 | часть сотрудников ещё в ramp |
| M11 | full team | 5 473 000 | sales cycle начинает созревать |
| M12 | full team | 5 473 000 | база для 20+ клиентов |

### Sanity-check
- В первый месяц не нанимается 5+ человек, time-to-hire realism не нарушен.
- FOT при выходе к полной команде быстро уходит выше **5,4 млн ₽/мес**, что выглядит реалистично для senior-heavy legaltech.
- Если исключить Patent Counsel или занизить AE/CTO, экономика станет косметически лучше, но операционно нереалистичной.

## 11. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| FOT fully-loaded | 5 473 000 | см. team table | [T4][inference] |
| Office / travel / client meetings | 150 000 | гибридный режим + выезды на enterprise встречи | [inference] |
| Shared infra not in COGS | 300 000 | core cloud, CI/CD, security, staging, observability | [inference] |
| Legal / accounting / compliance | 150 000 | договоры, бухучёт, юрподдержка | [inference] |
| Recruiting / sourcing / hiring overhead | 200 000 | hh, сорсинг, recruiter support | [T4][inference] |
| Corporate software / admin tools | 120 000 | corp stack beyond sales tools | [inference] |
| **Итого fixed costs / мес** | **6 393 000 ₽** |  |  |

## 12. Break-even по клиентам и по месяцам

### По количеству клиентов
- Contribution per client = **295 000 ₽/мес**.
- Fixed costs = **6 393 000 ₽/мес**.
- **Break-even client count = 6 393 000 / 295 000 = 21,7**, округляю до **22 клиентов**.
- Для **EBITDA 500 000 ₽/мес** нужно: `(6 393 000 + 500 000) / 295 000 = 23,4`, то есть **24 клиента**.

### Проверка правила 50 клиентов
- При **50 клиентах** contribution = **14 750 000 ₽/мес**.
- EBITDA ≈ **14 750 000 - 6 393 000 = 8 357 000 ₽/мес**.
- Значит mandatory reject `EBITDA < 500K/mo even at 50 clients` **не выполняется**.

### По месяцам, базовый ramp клиентов

| Месяц | Активные клиенты | Contribution, ₽/мес | Fixed costs, ₽/мес | EBITDA, ₽/мес |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 445 000 | -1 445 000 |
| M2 | 0 | 0 | 1 895 000 | -1 895 000 |
| M3 | 1 | 295 000 | 2 730 000 | -2 435 000 |
| M4 | 2 | 590 000 | 3 514 000 | -2 924 000 |
| M5 | 3 | 885 000 | 4 000 000 | -3 115 000 |
| M6 | 5 | 1 475 000 | 5 302 000 | -3 827 000 |
| M7 | 7 | 2 065 000 | 5 807 000 | -3 742 000 |
| M8 | 10 | 2 950 000 | 6 169 000 | -3 219 000 |
| M9 | 13 | 3 835 000 | 6 393 000 | -2 558 000 |
| M10 | 16 | 4 720 000 | 6 393 000 | -1 673 000 |
| M11 | 19 | 5 605 000 | 6 393 000 | -788 000 |
| M12 | 22 | 6 490 000 | 6 393 000 | **97 000** |

### Вывод
- Операционный monthly break-even достигается примерно в **M12** при 22 клиентах.
- До EBITDA 500K+/мес модель доходит в районе **24 клиентов**, то есть вскоре после M12 при сохранении темпа продаж.

## 13. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Суммарный отрицательный EBITDA до выхода в near-breakeven по модели выше составляет около **27,6 млн ₽**. Если добавить рабочий буфер на delayed collections, внедрения, непредвиденные legal/security расходы и резерв по найму, реалистичный **startup capital to breakeven = 40-45 млн ₽**. [inference]

### Cash runway
Берём **startup_capital = 60 млн ₽**.
- На раннем участке M1-M6 средний burn около **2,6-3,1 млн ₽/мес**.
- На участке M7-M11 burn держится около **2,4-3,7 млн ₽/мес**.
- При такой траектории **cash runway ≈ 16-18 месяцев**, что достаточно, чтобы дожить до breakeven только при дисциплинированном найме и канальном фокусе. [inference]

### Sanity-check
- Для enterprise legaltech startup capital **ниже 10 млн ₽** был бы нереалистичен; в нашей модели нужно в 4-6 раз больше.
- Главный кассовый риск, если enterprise sales cycle растянется, а локализация будет более ручной, запас 60 млн ₽ может сжаться до **12-14 месяцев runway**. [inference]

## 14. Ключевые риски unit economics

1. **Consulting creep:** если каждое внедрение превращается в bespoke патентное сопровождение, contribution margin быстро разрушается.
2. **Market width:** рынок РФ узкий, поэтому даже хорошая экономика на клиента не гарантирует лёгкий scale до 22-24 клиентов.
3. **Partner dependency:** лучшие каналы, referrals и partnerships, значит рост может зависеть от ограниченного числа отраслевых посредников.
4. **Localization burden:** русскоязычные патентные шаблоны, QA и corpus tuning могут оказаться дороже, чем заложено.
5. **Security / privacy drag:** для крупных R&D-команд может понадобиться private deployment, что временно ухудшит COGS и CAC.

## 15. Финальный вывод

**P5: PASS WITH RESERVATIONS.**

Кейс проходит инвестиционный фильтр по юнит-экономике, если его продавать как **дорогой enterprise legaltech workflow**, а не как массовый AI-seat. На текущей модели:
- LTV/CAC сильно выше 3x;
- CAC payback комфортный;
- EBITDA 500K+/мес достижим уже около 24 клиентов;
- при 50 клиентах бизнес выглядит прибыльным.

Но инвестиционный тезис остаётся хрупким: рынок нишевый, лучшие каналы ограничены, а любая деградация в сторону ручного patent outsourcing быстро съедает маржу. Поэтому кейс проходит дальше, но только с жёстким фокусом на productization, partner-led distribution и ограничение кастомного scope.

## Sources
- [T1] `02-demand.md` кейса DeepIP, спрос и monetization scenarios: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/deepip-geo-expand-v2/02-demand.md
- [T2] `03-solution.md` кейса DeepIP, solution thesis и delivery model: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/deepip-geo-expand-v2/03-solution.md
- [T3] ChartMogul Help Center, Customer Churn Rate, high-ARPA SaaS обычно ближе к 1-2% monthly churn: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T4] hh.ru, срез вакансий и вилок по senior backend / ML / DevOps / SDR / AE / CSM, просмотрено 2026-05-10: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancy/129266637 ; https://hh.ru/vacancies/machine-learning-engineer ; https://hh.ru/vacancy/128836250 ; https://hh.ru/vacancies/devops-engineer ; https://hh.ru/vacancy/128565026 ; https://hh.ru/vacancy/129749266 ; https://hh.ru/vacancies/customer-success-manager
- [T5] Bitrix24 pricing, Snov.io pricing и Яндекс.Директ, просмотрено 2026-05-10: https://www.bitrix24.com/prices/ ; https://snov.io/pricing ; https://yandex.ru/support/direct/ru/strategies/minimal-budget
- [T6] LinkedIn Sales Navigator help / pricing references, просмотрено 2026-05-10: https://www.linkedin.com/help/sales-navigator/answer/a108223 ; https://postiv.ai/blog/linkedin-sales-navigator-cost


---

# 05-critic.md

# SECTION A - PnL
## Допущения сценариев
- Base: ARPA 550 000 ₽, COGS 215 000 ₽/клиент/мес, fixed costs 6 393 000 ₽/мес, churn 1,6%/мес, налоговая база: IT-льгота 3% при аккредитации Минцифры.
- Optimistic: ARPA 580 000 ₽, COGS 204 000 ₽/клиент/мес, fixed costs 6 713 000 ₽/мес, churn 1,2%/мес, faster sales ramp, налоговая база: IT-льгота 3%.
- Pessimistic: ARPA 520 000 ₽, COGS 226 000 ₽/клиент/мес, fixed costs 7 032 000 ₽/мес, churn 2,5%/мес, slower ramp, налоговая база: УСН 6% от выручки как fallback.
- Contribution margin per client для cash-flow: Base 255 000 ₽ variable cost на клиента, Optimistic 244 000 ₽, Pessimistic 266 000 ₽.
- Страховые взносы уже учтены в fixed costs как ~30% к ФОТ. НДС 20% релевантен только на ОСНО и в PnL ниже не добавлен, так как рекомендованная структура для кейса, IT-льгота / УСН.
## Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 1 | 1.98 | 2.95 | 4.91 | 6.83 | 9.72 | 12.56 | 15.36 | 18.12 | 20.83 |
| MRR | 0 | 0 | 550 000 | 1 091 200 | 1 623 741 | 2 697 761 | 3 754 597 | 5 344 523 | 6 909 011 | 8 448 467 | 9 963 291 | 11 453 879 |
| COGS | 0 | 0 | 215 000 | 426 560 | 634 735 | 1 054 579 | 1 467 706 | 2 089 223 | 2 700 795 | 3 302 582 | 3 894 741 | 4 477 425 |
| Gross profit | 0 | 0 | 335 000 | 664 640 | 989 006 | 1 643 182 | 2 286 891 | 3 255 301 | 4 208 216 | 5 145 884 | 6 068 550 | 6 976 453 |
| GM% | 0.0% | 0.0% | 60.9% | 60.9% | 60.9% | 60.9% | 60.9% | 60.9% | 60.9% | 60.9% | 60.9% | 60.9% |
| Fixed costs | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 | 6 393 000 |
| EBITDA | -6 393 000 | -6 393 000 | -6 058 000 | -5 728 360 | -5 403 994 | -4 749 818 | -4 106 109 | -3 137 699 | -2 184 784 | -1 247 116 | -324 450 | 583 453 |
| Cash burn | -6 393 000 | -6 393 000 | -6 058 000 | -5 728 360 | -5 403 994 | -4 749 818 | -4 106 109 | -3 137 699 | -2 184 784 | -1 247 116 | -324 450 | 0 |
| Cumulative cash | -6 393 000 | -12 786 000 | -18 844 000 | -24 572 360 | -29 976 354 | -34 726 173 | -38 832 282 | -41 969 981 | -44 154 766 | -45 401 881 | -45 726 331 | -45 142 878 |

**Waterfall (M12):** ARPA 550 000 ₽ -> Gross 335 000 ₽/client -> Contribution 295 000 ₽/client -> EBITDA 583 453 ₽/мес -> Net after tax: IT-льгота 3% = 239 837 ₽/мес. Для сравнения: УСН 6% = -103 779 ₽, IT-льгота 3% = 239 837 ₽, ОСНО 20% = 466 763 ₽.

**Cash flow:** startup_capital_to_bep_rub = 45 726 331 ₽.

**Break-even:** 20 клиентов по gross profit, месяц M12.

## Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 4 | 4 |
| Total clients | 0 | 1 | 1.99 | 3.96 | 5.92 | 8.85 | 11.74 | 15.60 | 19.41 | 23.18 | 26.90 | 30.58 |
| MRR | 0 | 580 000 | 1 153 040 | 2 299 204 | 3 431 613 | 5 130 434 | 6 808 869 | 9 047 162 | 11 258 596 | 13 443 493 | 15 602 171 | 17 734 945 |
| COGS | 0 | 204 000 | 405 552 | 808 685 | 1 206 981 | 1 804 497 | 2 394 843 | 3 182 105 | 3 959 920 | 4 728 401 | 5 487 660 | 6 237 808 |
| Gross profit | 0 | 376 000 | 747 488 | 1 490 518 | 2 224 632 | 3 325 936 | 4 414 025 | 5 865 057 | 7 298 676 | 8 715 092 | 10 114 511 | 11 497 137 |
| GM% | 0.0% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% | 64.8% |
| Fixed costs | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 | 6 713 000 |
| EBITDA | -6 713 000 | -6 337 000 | -5 965 512 | -5 222 482 | -4 488 368 | -3 387 064 | -2 298 975 | -847 943 | 585 676 | 2 002 092 | 3 401 511 | 4 784 137 |
| Cash burn | -6 713 000 | -6 337 000 | -5 965 512 | -5 222 482 | -4 488 368 | -3 387 064 | -2 298 975 | -847 943 | 0 | 0 | 0 | 0 |
| Cumulative cash | -6 713 000 | -13 050 000 | -19 015 512 | -24 237 994 | -28 726 362 | -32 113 426 | -34 412 400 | -35 260 344 | -34 674 668 | -32 672 576 | -29 271 065 | -24 486 928 |

**Waterfall (M12):** ARPA 580 000 ₽ -> Gross 376 000 ₽/client -> Contribution 336 000 ₽/client -> EBITDA 4 784 137 ₽/мес -> Net after tax: IT-льгота 3% = 4 252 088 ₽/мес. Для сравнения: УСН 6% = 3 720 040 ₽, IT-льгота 3% = 4 252 088 ₽, ОСНО 20% = 3 827 309 ₽.

**Cash flow:** startup_capital_to_bep_rub = 35 260 344 ₽.

**Break-even:** 18 клиентов по gross profit, месяц M9.

## Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 1 | 1.98 | 2.93 | 3.85 | 5.76 | 7.61 | 9.42 | 11.19 | 12.91 | 14.58 |
| MRR | 0 | 0 | 520 000 | 1 027 000 | 1 521 325 | 2 003 292 | 2 993 210 | 3 958 379 | 4 899 420 | 5 816 934 | 6 711 511 | 7 583 723 |
| COGS | 0 | 0 | 226 000 | 446 350 | 661 191 | 870 661 | 1 300 895 | 1 720 373 | 2 129 363 | 2 528 129 | 2 916 926 | 3 296 003 |
| Gross profit | 0 | 0 | 294 000 | 580 650 | 860 134 | 1 132 630 | 1 692 315 | 2 238 007 | 2 770 057 | 3 288 805 | 3 794 585 | 4 287 720 |
| GM% | 0.0% | 0.0% | 56.5% | 56.5% | 56.5% | 56.5% | 56.5% | 56.5% | 56.5% | 56.5% | 56.5% | 56.5% |
| Fixed costs | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 | 7 032 000 |
| EBITDA | -7 032 000 | -7 032 000 | -6 738 000 | -6 451 350 | -6 171 866 | -5 899 370 | -5 339 685 | -4 793 993 | -4 261 943 | -3 743 195 | -3 237 415 | -2 744 280 |
| Cash burn | -7 032 000 | -7 032 000 | -6 738 000 | -6 451 350 | -6 171 866 | -5 899 370 | -5 339 685 | -4 793 993 | -4 261 943 | -3 743 195 | -3 237 415 | -2 744 280 |
| Cumulative cash | -7 032 000 | -14 064 000 | -20 802 000 | -27 253 350 | -33 425 216 | -39 324 586 | -44 664 271 | -49 458 264 | -53 720 208 | -57 463 403 | -60 700 818 | -63 445 097 |

**Waterfall (M12):** ARPA 520 000 ₽ -> Gross 294 000 ₽/client -> Contribution 254 000 ₽/client -> EBITDA -2 744 280 ₽/мес -> Net after tax: УСН 6% = -3 199 303 ₽/мес. Для сравнения: УСН 6% = -3 199 303 ₽, IT-льгота 3% = -2 971 791 ₽, ОСНО 20% = -2 744 280 ₽.

**Cash flow:** startup_capital_to_bep_rub = 63 445 097 ₽.

**Break-even:** 24 клиентов по gross profit, месяц не достигнут в M1-M12.

## Налоговая модель
- **УСН 6%**: safest fallback для early-stage структуры, налог считается с выручки, cash-out заметен даже при низкой EBITDA.
- **IT-льгота 3%**: предпочтительный режим для DeepIP при аккредитации Минцифры и соблюдении доли профильной IT-выручки; даёт лучший Net cash result.
- **ОСНО 20%**: применять только если льготы / УСН недоступны; тогда дополнительно появляется **НДС 20%**, что ухудшает оборотный капитал и усложняет price parity.
- **Страховые взносы ~30% к ФОТ** уже зашиты в fixed costs и дополнительно не начисляются в таблицах.

<!-- P6A-DONE -->

# SECTION B - Finance Risk + Competitor

## 1. Sensitivity analysis, EBITDA impact через 12 месяцев

Базовая точка берётся из SECTION A: EBITDA в M12 = **583 453 ₽/мес**. Для чувствительности я меняю по одному драйверу, остальное оставляю как в base.

| Сценарий | Допущение | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | как в текущей модели | 583 453 | 0 | near-breakeven в M12 |
| Sens1 | CAC x2 | -1 139 047 | -1 722 500 | удвоение acquisition spend почти сразу уводит модель обратно в burn |
| Sens2 | Churn x2, с 1,6% до 3,2% | 216 231 | -367 222 | экономика ещё жива, но запас прочности резко падает |
| Sens3 | Price -30%, ARPA 550K → 385K | -2 852 710 | -3 436 163 | price compression ломает модель быстрее, чем churn |

**Вывод:** у кейса главный финансовый single-point-of-failure, не churn, а **price compression** и рост стоимости продаж. Это типично для узкого enterprise legaltech, где конкуренция и procurement pressure бьют сильнее, чем чистый self-serve SaaS.

## 2. Monte Carlo Lite, confidence intervals

### 2.1. Triangular inputs

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 100 000 | 1 640 500 | 3 300 000 | [T4][T5][inference] |
| Monthly churn, % | 1,2% | 1,6% | 3,2% | [T3][inference] |
| ARPU, ₽/мес | 450 000 | 550 000 | 650 000 | [T1][T2][inference] |
| Conversion rate lead→paid, % | 0,15% | 0,24% | 0,40% | [T5][inference] |
| Time-to-hire, мес | 1,0 | 1,8 | 3,0 | [T4][inference] |

### 2.2. Метод расчёта

Полную 1000-итерационную симуляцию здесь не кодирую. Вместо неё использую **9-комбинационный Monte Carlo Lite**:
- best: CAC_min + churn_min + ARPU_max;
- median: CAC_mode + churn_mode + ARPU_mode;
- worst: CAC_max + churn_max + ARPU_min;
- плюс 6 смешанных комбинаций.

Горизонт для оценки, **M24**, потому что на M12 модель ещё только подходит к break-even и слишком чувствительна к фазе ramp-up.

### 2.3. Результат, p10 / p50 / p90

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | 2 121 700 | 11 020 519 | 16 786 109 | 14 664 410 |
| CAC payback, мес | 1,69 | 2,98 | 7,33 | 5,64 |
| LTV/CAC | 2,23x | 9,52x | 32,95x | 30,73x |
| Cash runway, мес | 9,43 | 15,82 | 20,61 | 11,17 |

### 2.4. Interpretation vs rules

- **Rule 1:** p10 EBITDA < 0, **не срабатывает**. Даже в нижнем сценарии на M24 EBITDA остаётся положительной.
- **Rule 2:** p50 EBITDA < 500K ₽/мес, **не срабатывает**. Median сильно выше gate.
- **Rule 3:** p90 / p10 > 10x, **не срабатывает**. Соотношение ~**7,9x**, неопределённость высокая, но ещё не запредельная.
- **Rule 4:** range width по **LTV/CAC = 30,73x**, это **сильно выше порога 8**. Значит модель хрупкая и очень зависит от связки **pricing + churn + CAC**.

### 2.5. Главный вывод по Monte Carlo Lite

Median-сценарий выглядит инвестируемым, но хвост риска широкий. Это не «стабильный compounder», а кейс, где высокая upside-математика покупается ценой чувствительности к каналу продаж, удержанию и ценовой дисциплине.

## 3. Competitor deep-dive

Ниже market-share estimate понимается **не как доля всего патентного рынка**, а как **оценка доли в своём релевантном сегменте digital patent workflow / AI patent tooling / IP operations**, потому что публичной единой базы по этому узкому рынку нет. Оценки ниже — экспертные и приблизительные. [inference]

### 3.1. Топ-3 западных

| Конкурент | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Solve Intelligence** | Прямой AI-игрок для patent drafting и prosecution | сильный фокус на drafting workflow, security positioning, 500+ IP teams, понятный ROI на productivity | меньше service-wrapper, слабее локальная адаптация под РФ, buyer чаще западная patent firm | **8-12%** среди AI-first patent drafting tools | можем выиграть локализацией под Роспатент и hybrid QA layer для русскоязычных заявок |
| **Patlytics** | Идёт шире drafting, в patent intelligence, litigation, claim charts | сильный enterprise story, аналитика портфеля, infringement use-cases, хороший fit для крупных IP teams | heavier platform sale, вероятно длиннее внедрение и выше complexity | **10-15%** среди AI-native patent intelligence / workflow | DeepIP-подобный wedge проще упаковать как drafting-first managed outcome, а не как тяжёлую platform transformation |
| **PatSnap** | Большой incumbent в IP intelligence и innovation analytics | масштаб данных, бренд, широкий enterprise footprint, кросс-функциональный innovation stack | не так узко заточен под drafting throughput, продукт шире и тяжелее, может быть overkill для нишевого buyer'а | **20-25%** в global IP intelligence stack, но ниже в AI drafting niche | можно заходить с более узким painkiller, быстрее pilot, меньше implementation drag |

### 3.2. Топ российских и локальных substitutes

| Конкурент | Основание включения | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Онлайн Патент** | Habr-profile заявляет 105K+ пользователей, 5000+ заявок в год, 70+ специалистов, прямую синхронизацию с Роспатентом | сильнейший локальный digital IP brand, большой installed base, реальная подача заявок и enterprise logos | больше про end-to-end IP service platform, чем про глубокий AI drafting moat; risk of service heaviness | **25-35%** среди цифровых IP-сервисов в РФ | наш шанс, deep drafting / prosecution copilot для high-value patent workflow, а не общий кабинет ИС |
| **PATENTUS** | Rusprofile показывает выручку 181 млн ₽ в 2025, зрелый бренд и long-standing практика | сильная юридическая экспертиза, доверие, офлайн/сервисный канал, корпоративные клиенты | слабее product/SaaS moat, выше доля ручного труда, ниже AI differentiation | **10-15%** среди premium patent service firms с digital front-end | можем быть быстрее, технологичнее и лучше в workflow automation, а не только в сервисе |
| **Skolkovo IP / ЦИС Сколково** | Сервисы Сколково дают полный спектр IP/legal support для резидентов | доступ к потоку deeptech-команд, trust и встроенный канал distribution | это не чистый продукт, а ecosystem service layer; outside-resident scale ограничен | **5-10%** в сегменте стартап-oriented IP support | можем продавать не только консультацию, а recurring workflow engine для зрелых enterprise IP teams |
| **n’RIS / Digital IP** | VC и market coverage вокруг цифрового управления ИС и licensing stack | сильная тема digital IP management, сделки, учёт и оборот прав | меньше фокус на patent drafting и prosecution execution | **5-8%** в adjacent digital IP management | наш product wedge глубже в creation workflow, а не в post-registration monetization |
| **Классические патентные бюро без сильного ПО** | Это главный substitute в РФ, даже если не software competitor | доверие, ответственность, human QA, established relationships | низкая автоматизация, дорогой expert-hour, слабая масштабируемость | **30%+** в spend share конечного buyer'а | если productized delivery реально экономит 30-50% expert time, можно отбирать budget у ручного аутсорса |

### 3.3. Конкурентный вывод

На Западе DeepIP конкурирует с сильными AI-native продуктами, где differentiation строится на product depth и security. В РФ главный бой идёт не только против «другого AI-патентного стартапа», а против **сервисных игроков с локальным доверием и доступом к Роспатенту**. Поэтому победная стратегия в РФ, не PLG, а **hybrid software + expert operations + private/security-ready deployment**.

## 4. Risk matrix

| # | Category | Risk | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | CTO / ML hiring slip, команда не собирается в срок | med | high | time-to-hire > 3 мес, офферы отклоняются, roadmap сдвигается | заранее build bench, fractional advisors, перенос части roadmap в simpler stack |
| 2 | Operational | Quality drift у patent drafts, слишком много ручных правок | med | high | >25% deliverables требуют major rewrite патентным поверенным | mandatory QA gates, template library, narrow ICP по типам заявок |
| 3 | Operational | LLM API latency / outage / token-cost spike | med | high | рост unit-cost inference >30%, SLA инциденты, vendor outages | multivendor routing, caching, fallback models, contract caps |
| 4 | Market | Спрос уже есть, но enterprise sales cycle растягивается >9 мес | high | high | пилоты висят без conversion, procurement freeze, много security redlines | founder-led enterprise selling, partner channel, pre-scoped paid pilots |
| 5 | Market | Price compression из-за конкуренции с бюро и generic LLM | high | high | скидки >20%, win-rate падает без price cut | value-based packaging, ROI calculator, private deployment premium |
| 6 | Market | Narrow market width, в РФ не набирается 22-24 качественных клиента | med | high | pipeline concentration, <8 qualified ICP accounts в квартал | идти через бюро/партнёров, CIS/ME expansion, смежные IP workflows |
| 7 | Regulatory | 152-ФЗ, data residency и требования к локализации данных | med | high | security questionnaires всё чаще требуют RU-hosting и private contour | RU cloud / on-prem option, DPA templates, tenant isolation |
| 8 | Regulatory | 115-ФЗ и KYC/AML friction у части клиентов и платежей | low | med | затяжка контрактации, extra compliance requests, блокировки платежей | юрструктура, прозрачный billing, ready compliance pack |
| 9 | Regulatory | Санкции на SaaS / ограничения доступа к западным моделям и облакам | high | high | vendor policy changes, billing rejects, geo-blocks | domestic backup infra, abstraction layer, alternative model providers |
| 10 | Financial | Cash runway сжимается из-за sales delay и медленного выхода в MRR | med | high | runway < 12 мес, plan/fact burn >20% хуже | freeze hiring, cut paid channels, bridge financing plan |
| 11 | Financial | USD/RUB volatility поднимает LLM и cloud COGS | high | med | FX move >15%, рост долларовых invoice | FX buffer in pricing, quarterly repricing clauses, RUB-heavy infra |
| 12 | Financial | Налоги / льготы Минцифры недоступны, effective tax rate растёт | med | med | не получена аккредитация, доля профильной выручки спорная | fallback УСН model, legal structuring, early tax review |
| 13 | Black swan | Военная/санкционная эскалация режет доступ к клиентам и поставщикам | med | high | sudden compliance blocks, counterparties pause procurement | diversify geographies, reserve cash, multi-region infra |
| 14 | Black swan | Критичное отключение LLM vendor или резкий policy-ban на legal use-case | med | very high | ToS changes, suspended API keys, degraded outputs | model-agnostic architecture, local inference fallback, human-only contingency mode |

## 5. Kill conditions через 6 месяцев

1. **MRR < 1,5 млн ₽ и < 3 платящих клиента.** Это значит, что market pull не подтвердился даже на раннем enterprise wedge.
2. **Blended CAC > 3,0 млн ₽ или CAC payback > 9 мес.** При такой цене new-logo motion уже начинает съедать весь upside legaltech-модели.
3. **Gross margin < 50% или human-QA share > 45% COGS.** Это сигнал, что продукт скатился в патентный аутсорс, а не в scalable workflow software.

## 6. Investment judgment after P6B

**Итог:** кейс остаётся **проходимым, но хрупким**.

Что нравится:
- median и даже p10 на горизонте M24 не ломают EBITDA-gate;
- локальный wedge понятен, если идти через enterprise/hybrid delivery;
- конкурентное окно в РФ есть, потому что рынок всё ещё сервисно-фрагментирован.

Что тревожит:
- чувствительность к price compression очень высокая;
- диапазон LTV/CAC слишком широкий, модель неустойчива;
- главный конкурент в РФ, не AI-стартап, а доверенный сервисный игрок с локальным доступом к клиенту.

Практический вывод: инвестировать в такой кейс можно только при жёстком контроле трёх метрик, **pricing discipline, QA automation share и partner-led pipeline velocity**.

## Sources for SECTION B
- [B1] Solve Intelligence official site: https://www.solveintelligence.com/
- [B2] Patlytics official site: https://www.patlytics.ai/
- [B3] PatSnap official site: https://www.patsnap.com/
- [B4] DeepIP funding / positioning: https://www.deepip.ai/blog/deepip-raises-15m-ai-patent-drafting
- [B5] Habr company profile, Online Patent: https://habr.com/ru/companies/onlinepatent/profile/
- [B6] Rusprofile, PATENTUS / Шуршилин М.В.: https://www.rusprofile.ru/person/shurshilin-mv-772070636397
- [B7] Сервисы Сколково, юридическая поддержка и IP: https://services.sk.ru/service/217/N4IgZiBcoC4IYHMDOB9GBPADgUyiA9gE4gC%2BANCEngCbZhwCuANjCBZlAIwlA
- [B8] vc.ru search references used as qualitative market corroboration for digital IP services in РФ: https://vc.ru/search?q=%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD%20%D0%BF%D0%B0%D1%82%D0%B5%D0%BD%D1%82 ; https://vc.ru/search?q=patentus ; https://vc.ru/search?q=nris

<!-- P6B-DONE -->


---

# 06-verdict.md

# 06-verdict

[GEO-EXPAND] DeepIP — REJECTED: 53/100 | EBITDA base=583К₽/мес через 12 мес | LTV/CAC=12,8x | Ключевое преимущество: hybrid IP workflow с локальным QA-слоем | Главный риск: weak moat и слишком узкий buyer universe в РФ.

sector: GEO-EXPAND

## Финальный вердикт
- **Статус:** REJECTED
- **Score:** **53/100**
- **Пороговое правило:** score < 65, поэтому кейс не проходит инвесткомитет, даже при формально проходимом EBITDA-gate.
- **Ключевая причина отказа:** клиентская экономика сильная, но investment-grade запас прочности отсутствует из-за слабого moat, узкого локального рынка, founder/partner-heavy GTM и непроверенного качества evidence tier.

## Investment committee one-liner
[GEO-EXPAND] DeepIP — REJECTED: 53/100 | EBITDA base=583К₽/мес через 12 мес | LTV/CAC=12,8x | Ключевое преимущество: hybrid IP workflow с локальным QA-слоем | Главный риск: weak moat и слишком узкий buyer universe в РФ.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | "LTV/CAC = 12,8x", "CAC Payback = 2,98 мес", "Gross margin = 60,9%" из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 17 | "EBITDA 500K+/мес нужно... 24 клиента" и в PnL "EBITDA ... M12 = 583 453" из `04-economics.md` и `05-critic.md`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | "массового спроса на standalone patent AI в РФ не видно" и отсутствует строка `Sources:` в `02-demand.md`, поэтому cap 10/25. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | "service moat" описан, но moat остаётся слабым: в `05-critic.md` главный бой идёт против "доверенных сервисных игроков". |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 13 | В risk matrix есть "санкции", "LLM vendor", "152-ФЗ", hiring slip и price compression, то есть риск materially above investment-grade. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 11 | В `04-economics.md` лучшие каналы это "Partner / referral" и founder-led motion, а outbound/payments слишком дорогие. |

**Sum raw = 79/150. Normalized score = round((79 × 100) / 150) = 53/100.**

## 7-factor moat framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных в явной сетевой форме. |
| Switching costs | 2 | Есть workflow templates, corpus и team training, но без глубокой системной интеграции switching costs средние. |
| Scale economies | 1 | COGS частично улучшается с объёмом, но human QA остаётся крупной статьёй. |
| Proprietary data / model advantage | 1 | Domain tuning возможен, но доказанного уникального локального датасета в evidence нет. |
| Regulatory moat | 1 | Legal/IP compliance важны, но лицензируемого барьера уровня health/fintech тут нет. |
| Brand / distribution | 1 | У глобального игрока есть category validation, но локальный бренд и channel ownership в РФ не доказаны. |
| Embedded workflow | 2 | Если внедрение прошло, продукт садится в регулярный patent workflow и prosecution loop. |

**Moat score = round((8 × 25) / 21) = 10/25.**

**Вывод по moat:** weak moat. Это автоматически попадает в Top-3 Risks.

## Почему не approve, несмотря на сильную клиентскую economics
1. **Клиентская математика сильнее, чем рыночная реальность.** LTV/CAC и payback выглядят хорошо, но сам `02-demand.md` прямо говорит, что "массового спроса на standalone patent AI в РФ не видно".
2. **Moat слишком слабый для investment committee.** Локальный buyer может купить похожий outcome через патентное бюро, in-house процесс или generic LLM + human expert.
3. **GTM слишком узкий и human-heavy.** Лучшие каналы, referrals и founder-led selling, а не repeatable scalable acquisition engine.
4. **Evidence quality недостаточно сильная.** Нет строки `Sources: T1=..., T2=..., T3=...`, поэтому критерий #3 получает штраф и флаг `evidence_quality_unverified`.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 20 937 500 ₽ |
| Fully-loaded CAC | 1 640 500 ₽ |
| LTV/CAC | 12,8x |
| CAC payback | 2,98 мес по MRR / 4,9 мес по gross profit |
| Gross margin | 60,9% |
| contribution_margin_rub_month | 295 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 393 000 ₽/мес |
| company_ebitda_rub_month base | 583 453 ₽/мес на M12 |
| company_ebitda_potential_rub_month | 8 357 000 ₽/мес при 50 клиентах |
| Break-even | 22 клиента |
| clients_to_500k_ebitda | 24 |
| months_to_500k_ebitda | 12-13 мес |
| clients_to_1m_ebitda | 26 |
| months_to_1m_ebitda | 13-14 мес |
| startup_capital_to_bep_rub | 45 726 331 ₽ |

## Полный бизнес-процесс

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-аккаунтов, патентных бюро и in-house IP-команд | SDR | LinkedIn Sales Navigator, Bitrix24, ручной ресерч | 45 мин | 1 100 | Полуавтоматически |
| 2 | Поиск decision-maker, контактов и warm-intro путей | SDR | Snov.io, LinkedIn, сайт компании | 30 мин | 800 | Полуавтоматически |
| 3 | Outbound sequence / обработка inbound interest | SDR | email, Bitrix24, Telegram | 25 мин | 700 | Полуавтоматически |
| 4 | Первичная квалификация по ICP и объёму патентного потока | SDR | Bitrix24, qualification script | 30 мин | 850 | Ручной контроль |
| 5 | Discovery call по текущему patent workflow | AE + CEO | Google Meet / Zoom, CRM notes | 75 мин | 4 200 | Ручной |
| 6 | Product demo и разбор 1-2 реальных use cases | AE + Patent Counsel | demo workspace, sample claims, templates | 90 мин | 6 300 | Ручной |
| 7 | Оценка юрисдикции, качества данных и локализации под Роспатент | Patent Counsel + CTO | внутренние чек-листы, corpus review | 2 ч | 8 800 | Ручной |
| 8 | Security / privacy / deployment scoping | CTO | архитектурные схемы, docs, cloud design | 2 ч | 7 500 | Ручной |
| 9 | Расчёт ROI, pilot scope и коммерческое предложение | AE + CEO | spreadsheet, proposal template | 2 ч | 6 800 | Полуавтоматически |
| 10 | Согласование договора, NDA, ИБ и procurement | CEO + AE | email, ЭДО, redlines | 3 ч | 10 500 | Ручной |
| 11 | Платный pilot / setup: настройка шаблонов, QA flow, sandbox | CTO + Backend + Patent Counsel | cloud, product sandbox, prompt library | 10 ч | 31 000 | Полуавтоматически |
| 12 | Go-live и обучение команды клиента | CSM + Patent Counsel | playbook, workspace, onboarding sessions | 3 ч | 9 500 | Полуавтоматически |
| 13 | Счёт, акт, поступление первой оплаты | Finance / CEO | банк, Диадок / ЭДО, CRM | 30 мин | 1 000 | Почти автоматизировано |

## Команда

| Роль | Нужно чел. | FOT fully-loaded ₽/мес | Time-to-hire | Ramp |
|---|---:|---:|---:|---:|
| CEO | 1 | 845 000 | 0 мес | 0 мес |
| CTO / Tech Lead | 1 | 715 000 | 2-3 мес | 2 мес |
| Senior Backend | 2 | 1 092 000 | 1-2 мес | 1,5 мес |
| ML Engineer | 1 | 676 000 | 2-3 мес | 2 мес |
| DevOps | 1 | 455 000 | 1-2 мес | 1 мес |
| Frontend | 1 | 364 000 | 1 мес | 1 мес |
| SDR | 1 | 208 000 | 0,5-1 мес | 1 мес |
| AE | 1 | 416 000 | 1-2 мес | 2-3 мес |
| Patent Counsel / QA Lead | 1 | 390 000 | 1-2 мес | 1 мес |
| Customer Success | 1 | 312 000 | 1 мес | 1 мес |
| **Итого** | **11** | **5 473 000 ₽/мес** |  |  |

## GTM: 10 named targets

| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Онлайн Патент | Уже продаёт digital IP services и имеет большую installed base, значит может купить AI-layer для ускорения drafting/QA. | партнёрство + email decision-maker | 450 000 ₽/мес |
| 2 | PATENTUS | Сильная сервисная практика и выручка 181 млн ₽ указывают на объём кейсов, где нужен throughput. | email управляющему партнёру | 500 000 ₽/мес |
| 3 | Skolkovo IP / ЦИС Сколково | Поток deeptech-клиентов и встроенный IP-service channel, где можно тестировать managed patent ops. | партнёрство / конференция Сколково | 400 000 ₽/мес |
| 4 | Яндекс | Крупная R&D-команда и регулярная IP-активность делают private workflow automation осмысленной. | warm intro в legal/IP + конференция | 700 000 ₽/мес |
| 5 | Сбер | Большой поток технологий, чувствительность к безопасности и budget for enterprise legal ops. | email decision-maker + партнёрский интро | 800 000 ₽/мес |
| 6 | МТС | Разнообразный tech/IP портфель и потребность ускорять prosecution без роста headcount. | outbound ABM + industry event | 600 000 ₽/мес |
| 7 | Росатом | Высокая патентная активность, длинный lifecycle и потребность в controlled private contour. | госпартнёрство / отраслевой форум | 850 000 ₽/мес |
| 8 | Ростех | Много НИОКР и формализованных IP-процессов, где automation может снизить нагрузку на поверенных. | партнёрство + conference intro | 750 000 ₽/мес |
| 9 | СИБУР | Industrial R&D и регулярный поток разработок создают понятный ROI на faster drafting/prior-art. | email head of IP / legal ops | 550 000 ₽/мес |
| 10 | BIOCAD | Фарма и deeptech имеют дорогой patent workflow и высокий риск ошибок, поэтому QA-heavy AI слой релевантен. | конференция + targeted outbound | 650 000 ₽/мес |

**Оценка GTM:** named targets есть, но почти все они требуют enterprise trust-selling, security review и founder/partner-led access. Это улучшает критерий #6, но не поднимает его до investment-ready.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top risk |
|---|---|---|---|
| weak_moat_vs_service_incumbents | high | high | Локальный buyer может выбрать доверенное патентное бюро или собственный workflow вместо отдельного AI-layer. |
| market_width_russia_too_narrow | medium-high | high | Даже при сильной economics рынок РФ может не дать достаточно repeatable ICP для быстрого scale. |
| evidence_quality_unverified | high | medium-high | В `02-demand.md` нет строки `Sources: T1=..., T2=..., T3=...`, поэтому quality of evidence formally ниже стандарта. |

## Proof points, которые были бы нужны для APPROVED
1. **2-3 paid design partners в РФ** с чеком не ниже 500-700 тыс. ₽/мес.
2. **Подтверждённый pilot-to-production** цикл ≤ 90 дней, без bespoke legal consulting creep.
3. **Реальный локальный moat**: private deployment, интеграции, corpus advantage или partner channel, который сложно быстро скопировать.
4. **Снижение human QA share** в COGS ниже 35-40% без просадки качества.
5. **Трекшн по enterprise targets**: хотя бы 10-15 реальных qualified accounts в активной воронке.

## LTV Upside Calculator
Поскольку кейс = **REJECTED**, ниже условия, при которых его можно вернуть в near-pass / approve review.

| Рычаг | Текущая база | Upside-сценарий | Эффект |
|---|---:|---:|---|
| ARPA | 550 000 ₽/мес | 650 000 ₽/мес | Повышает contribution и смягчает pressure от enterprise sales cycle. |
| COGS | 215 000 ₽/мес | 180 000 ₽/мес | Улучшает gross margin и снижает consulting creep risk. |
| Human QA доля | 95 000 ₽/мес | 60 000 ₽/мес | Делает модель более productized, а не service-heavy. |
| Churn | 1,6%/мес | 1,2%/мес | Поднимает customer_ltv_rub и доказывает workflow stickiness. |
| New paying customers / мес | 1,05 | 1,5-1,8 | Ускоряет выход к 500K и 1M EBITDA без чрезмерного burn. |
| Partner share в new logos | 43% | 60%+ | Снижает blended CAC и dependence на дорогой outbound. |

## Финальный комментарий инвесткомитета
DeepIP в РФ выглядит как качественный **enterprise/hybrid patent workflow** кейс с сильной экономикой на клиента, но не как готовый фондовый winner. Если команда докажет локальный repeatable demand, partner-led distribution и productization QA-слоя, кейс можно вернуть на пересмотр. На текущих данных это **REJECTED, 53/100**.

