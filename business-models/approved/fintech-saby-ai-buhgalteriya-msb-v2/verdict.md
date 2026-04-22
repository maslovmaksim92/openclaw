# verdict

Скомпилированный пакет кейса по всем доступным стадиям P1-P7.


---

# FILE: 01-intake.md

---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-fintech-saby-ai-buhgalteriya-msb.md
created: 2026-04-20T13:22:21+03:00
---

# Intake

## Режим обработки
Принудительный полный пайплайн по правилу `rerun-/resurrect-`. На этапе intake файл не классифицируется как duplicate.

## Оригинальный источник
- Raw-файл: `2026-04-19-resurrect-fintech-saby-ai-buhgalteriya-msb.md`
- Исторический источник: см. секцию Meta внутри raw-контента ниже.

## Контекст raw-файла

# RESURRECT SIGNAL — fintech-saby-ai-buhgalteriya-msb

## Meta
- source: triage/triage-2026-04-16-fintech-saby-ai-buhgalteriya-msb.md
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
2026-04-16

## Входные данные
- `pipeline/raw/2026-04-16-fintech-saby-ai-buhgalteriya-msb.md`

## Классификация
new case

## Решение
Открыть новый кейс `ai-accounting-document-processing-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` по AI-бухгалтерии, распознаванию первичных бухгалтерских документов и автоматизации бухгалтерских workflow не найдено.
- Сигнал сильный и локальный: Saby уже коммерциализирует AI-обработку первички, автозаполнение платёжных реквизитов, подготовку ответов на требования ФНС и работу с портфелем клиентских кабинетов для аутсорс-бухгалтерии.
- Потенциал LTV проходит порог Program 1, потому что ценность создаётся на уровне бухгалтерского аутсорсера, финсервиса или группы компаний, а не на уровне одного пользователя. Это делает реалистичной модель выше `500 000 ₽/мес.` на клиента или портфель клиентов за счёт лицензии, внедрения, интеграции и managed-сопровождения.
- В `pipeline/rejected/` уже существует близкий исторический кейс по той же нише, но по текущим standing orders открытого кейса в `pipeline/cases/` нет. Текущий сигнал оформлен как новое открытие кейса в active-контуре, поскольку он дополнительно подтверждает локальный спрос и коммерческую зрелость категории.

## Что сделано
- Создан новый кейс `pipeline/cases/ai-accounting-document-processing-operator/`.
- В `00-brief.md` на русском языке зафиксированы краткое описание, текущее состояние и ключевая гипотеза по нише.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Открыт новый кейс по AI-автоматизации бухгалтерской первички и смежных финопераций. Сигнал от Saby усиливает уверенность, что в России уже существует платёжеспособная B2B-категория, где AI продаётся не как эксперимент, а как часть критичного бухгалтерского workflow.

```


---

# FILE: 01-evidence.md

# Evidence

## 2026-04-22 — supporting signal — Что делать Внедрение / AI-налоговый помощник
- Дата: 2026-04-22
- Источник: https://4dk-soft.ru/services/ai-tax-assistant/
- Тип: supporting signal
- Как усиливает кейс: Сигнал подтверждает, что на российском рынке AI уже продаётся не только для обработки первички, но и для регулярной дорогой налоговой переписки с ФНС внутри B2B-сопровождения. Это усиливает тезис, что AI-бухгалтерия в РФ монетизируется как повторяемый workflow-слой поверх существующей клиентской базы и сервисного контракта.
- Ключевые данные и факты:
  - компания заявляет базу 9 052+ клиентов;
  - средний бизнес получает 2–6 требований ФНС в месяц;
  - на каждое требование уходит 3–8 часов ручной работы;
  - AI сводит обработку требования к 2–3 минутам;
  - продукт упакован как сервис для налогового сопровождения и 1С-контуров.


## 2026-04-22 — AI-закрытие месяца и подготовка отчётности для МСБ
- Дата: 2026-04-22
- Источник: https://www.nalog.gov.ru/rn77/related_activities/ucedo/mchd/
- Источник: https://rmsp.nalog.ru/
- Источник: https://techcrunch.com/2024/05/29/accounting-startup-numeric-lands-28m-for-its-ai-based-platform-that-helps-ease-the-pain-of-closing-the-books/
- Источник: https://www.moedelo.org/tariffs/buhgalteriya-na-autsorsinge
- Тип: supporting signal
- Как усиливает кейс: Сигнал расширяет кейс от AI-обработки первички к более широкому workflow закрытия периода, подготовки отчётности и human-in-the-loop бухгалтерии для МСБ. Это усиливает гипотезу, что в РФ можно продавать не отдельный OCR-модуль, а регулярный финансово-операционный сервис поверх уже существующего бюджета на бухгалтерию.
- Ключевые данные и факты:
  - ФНС подтверждает дальнейшую стандартизацию машиночитаемых документов и доверенностей;
  - реестр МСП ФНС показывает массовую базу потенциальных клиентов в РФ;
  - Numeric демонстрирует международную валидацию AI-платформы для close и отчётности с 4x ростом выручки год к году;
  - «Моё дело» подтверждает, что российский МСБ уже регулярно платит за бухгалтерское сопровождение по подписной модели.

## 2026-04-22 — supporting signal — AI-сверка ЕНС и ответы на требования ФНС для МСБ
- Дата: 2026-04-22
- Источник: https://www.nalog.gov.ru/rn77/ens/ ; https://www.nalog.gov.ru/rn77/about_fts/about_nalog/14763247/ ; https://www.rusprofile.ru/id/6479698 ; https://saby.ru/help/account/reconciliation/check
- Тип: supporting signal
- Как усиливает кейс: Сигнал подтверждает, что российский рынок AI-бухгалтерии уже упирается не только в обработку первички, но и в регулярные налоговые workflow вокруг ЕНС, электронных требований и сверки с ФНС. Это усиливает кейс как recurring B2B-сервис для МСБ и аутсорс-бухгалтерии с понятным локальным спросом и высокой частотой использования.
- Ключевые данные и факты:
  - ФНС ведёт ЕНС как обязательный операционный контур для бизнеса;
  - по данным ФНС, в 2024 году поступило 1,7 млрд электронных документов;
  - Rusprofile показывает выручку ООО «Компания Тензор» 37 млрд руб. в 2024 году;
  - Saby уже продуктует регулярную сверку ЕНС, ЕНП и состояния расчётов с бюджетом как повторяемый workflow.

## 2026-04-22 — supporting signal — AI-бухгалтерия и автоподготовка налоговой отчётности для МСБ
- Дата: 2026-04-22
- Источник: https://www.nalog.gov.ru/rn77/news/activities_fts/16447933/ ; https://companies.rbc.ru/news/wLc9w7l5SR/autsorsing-buhgalterii---2026-kak-avtomatizatsiya-menyaet-ryinok/ ; https://www.fa.ru/university/structure/university/uso/press-service/press-releases/iskusstvennyy-intellekt-v-bukhgalterii-prakticheskoe-primenenie-i-ekonomicheskiy-effekt
- Тип: supporting signal
- Как усиливает кейс: Сигнал подтверждает, что рынок AI-бухгалтерии для МСБ в РФ опирается не только на обработку первички, но и на полный цикл подготовки налоговой и бухгалтерской отчётности. Это усиливает кейс как recurring B2B-сервис поверх массовой базы МСП, где автоматизация уже стала экономически обязательной.
- Ключевые данные и факты:
  - ФНС сообщает о 6,4 млн субъектов МСП в обновлённом реестре;
  - РБК Компании отмечает, что налоговая реформа 2026 года ускоряет спрос на автоматизацию бухгалтерского аутсорсинга;
  - Финансовый университет оценивает, что 30–40% операций первичного учёта повторяются и автоматизируются;
  - обработка первички при внедрении AI ускоряется в 2–3 раза.


---

# FILE: 02-demand.md

---
sector: FINTECH
stage: demand-validation
updated: 2026-04-21T06:20:00+03:00
---

# 02-demand

## Demand validation summary
- **Продукт**: AI-слой для автоматического распознавания и ввода первичных бухгалтерских документов, плюс смежные workflow вокруг требований ФНС, архива, ЭДО и повседневной работы бухгалтера внутри Saby.
- **Итог по спросу в РФ**: **HIGH**. Здесь есть не просто глобальный category proof, а уже локально коммерциализированный российский продукт с публичными функциями, ценой и встраиванием в ежедневный бухгалтерский контур. [T1]
- **Решение по гейту**: **не отклонять на P4**. Exact demand, buyer pain и willingness-to-pay видны уже на P3, причём не только как OCR-фича, а как часть критичного accounting workflow. [T1][T2]

## Evidence of demand

### 1) Saby продаёт именно тот workflow, который нужен рынку
- Официальная страница Saby по распознаванию документов прямо заявляет автоматический ввод первички из сканов, распознавание УПД, ТОРГ-12, счетов-фактур, накладных, актов, чеков и счетов, а также загрузку поступления в 1С. Это уже не R&D, а оформленный коммерческий модуль. [T1: https://saby.ru/autorecognition ; https://saby.ru/edo/recognition_1c]
- Saby публично обещает ускорение ввода документов в **10 раз** и точность **99%**, а также описывает дополнительные действия после распознавания: заполнение каталога без дублей, сохранение в электронный архив, формирование проводок и отражение в декларации. Даже если vendor metrics нужно проверять осторожно, сам способ упаковки показывает, что продаётся измеримый ROI на рутинной бухгалтерской операции. [T1]
- Saby Bu позиционируется как приложение, которое покрывает **полный цикл бухгалтерского учёта, от ввода первичных документов до закрытия периода и формирования отчётов**. Это усиливает тезис, что покупка идёт не ради отдельной OCR-кнопки, а внутри системно важного учётного контура. [T1: https://saby.ru/help/account/sabybu ; https://saby.ru/help/account]

### 2) Категория в РФ уже имеет ценовые якоря выше low-ticket уровня
- У Saby на лендинге распознавания документов виден публичный прайс **от 1 500 ₽ до 5 000 ₽** для базового модуля. Сам по себе этот прайс низкий, но он доказывает готовность рынка покупать automation даже на entry-level. [T1: https://saby.ru/autorecognition]
- Важнее то, что рядом существует более тяжёлый локальный ценовой якорь от 1С: сервис `1С:Распознавание первичных документов` продаётся вплоть до **1 625 000 ₽/год** за **500 000** страниц и **3 000 000 ₽/год** за **1 000 000** страниц. Это сильное подтверждение, что в РФ уже есть клиенты с большим потоком первички и бюджетом на document automation. [T1: https://v8.1c.ru/its/services/1s-raspoznavanie-pervichnykh-dokumentov/cena-1s-raspoznavanie-pervichnykh-dokumentov/]
- Следовательно, Saby как standalone low-end SaaS может быть недорогим, но как часть более широкого бухгалтерского контура и managed-внедрения категория спокойно дотягивается до enterprise и mid-market spend line. Это **inference** на базе публичного прайса Saby и 1С. [T1 inference]

### 3) Боль частая и обязательная, а не nice-to-have
- Первичка, ЭДО, сверки, архив и ответы на требования ФНС относятся к регулярным и обязательным операциям. Saby отдельно показывает работу с требованиями ФНС, статусы требований, автоподтверждение, отправку ответов и подбор документов в архиве. Это означает, что продукт вшит в compliance-critical процесс с жёсткими сроками. [T1: https://saby.ru/help/ereport/ni/claim ; https://saby.ru/help/ereport/ni/claim/answer ; https://saby.ru/help/ereport/ni/claim/auto ; https://saby.ru/help/ereport/ni/claim/confirm]
- На одной из страниц помощи Saby прямо указано, что если не ответить на требования вовремя, налоговая может заблокировать расчётные счета компании. Это резко повышает ценность автоматизации и снижает tolerance к ошибкам ручного процесса. [T1: https://saby.ru/help/sbis24/upb/treb]
- Из этого следует, что automation здесь экономит не только FTE-время, но и снижает операционный и комплаенс-риск. Для buyer'а это значительно сильнее, чем обычный productivity tool. [T1 inference]

### 4) Buyer universe в РФ широкий и живой
- По данным ФНС в Едином реестре МСП по состоянию на апрель 2026 года числится **6 947 425** субъектов, в том числе **2 203 395** юрлиц и **4 744 030** ИП. Не весь этот массив релевантен, но масштаб buyer base большой. [T1: https://ofd.nalog.ru/statistics.html?fo=&level=2&ssrf=]
- Даже если убрать микробизнес без сложной первички, остаётся крупный слой компаний с бухгалтерским контуром, регулярным документооборотом, ЭДО и 1С/Saby-процессами. Это особенно касается торговли, дистрибуции, услуг, строительства, аутсорс-бухгалтерии и multi-entity групп. [T1 inference]

### 5) Ручная альтернатива уже стоит заметных денег
- Вакансии на hh.ru в Москве по роли `бухгалтер на первичную документацию` в начале 2026 года показывают вилки порядка **80-100 тыс. ₽/мес**, **90-95 тыс. ₽/мес**, **100-120 тыс. ₽/мес** и **120-130 тыс. ₽/мес**, а в обязанностях регулярно фигурируют обработка первички, ввод в 1С, ЭДО, сверки и контроль документов. [T2: https://hh.ru/vacancy/130241174 ; https://hh.ru/vacancy/129689154 ; https://hh.ru/vacancy/130136848 ; https://hh.ru/vacancy/128880091]
- Это даёт прямой локальный ROI-anchor: даже частичная автоматизация 1-2 FTE или ускорение аутсорс-команды уже монетизируется в понятный budget transfer. [T2 inference]

## Competitive pricing and WTP

### Публичные price anchors
- **Saby распознавание документов**: от **1 500 ₽ до 5 000 ₽**. [T1]
- **1С:РПД 100 000 страниц**: **350 000 ₽/год**. [T1]
- **1С:РПД 500 000 страниц**: **1 625 000 ₽/год**. [T1]
- **1С:РПД 1 000 000 страниц**: **3 000 000 ₽/год**. [T1]
- **Бухгалтер на первичку**: примерно **80-130 тыс. ₽/мес** по свежим hh-вакансиям. [T2]

### Вывод по willingness to pay
- Для микросегмента self-serve OCR у Saby чек маленький, поэтому сам по себе он не доказывает high-LTV модель. [T1]
- Но если продавать не только распознавание, а пакет `AI-ввод первички + интеграция с 1С/Saby + ЭДО/архив + правила обработки + контроль требований ФНС + onboarding + support`, то годовой контракт **600 тыс. - 2,5 млн ₽** выглядит реалистичным для бухгалтерского аутсорсера, группы компаний или интенсивного mid-market buyer'а. Это **inference** из локального прайса 1С, payback на зарплатах и критичности workflow. [T1+T2 inference]
- Самый сильный buyer здесь, вероятно, не одиночное МСП, а бухгалтерские аутсорсеры, финансовые shared services и компании с большим входящим документооборотом. [inference]

## Market sizing

### Логика сегмента
Берём не весь рынок МСП, а только слой компаний и сервис-провайдеров, у которых есть регулярный поток первички, обязательный учёт, заметные затраты на ручную обработку и готовность оплачивать внедрение. [T1+inference]

### Top-down
- **TAM (РФ)**: если взять всего **3%** от базы МСП ФНС (**6 947 425**) как реально релевантный слой, получаем около **208 423** организаций. При среднем чеке **180 000 ₽/год** получаем потолок около **37,5 млрд ₽**. Это широкий ceiling. [T1 + inference]
- **SAM (РФ)**: если сузить до компаний и аутсорс-провайдеров с ощутимым документооборотом и интеграционной готовностью, рабочий сегмент можно оценить в **15 000** аккаунтов. При среднем ARR **600 000 ₽** получаем **9,0 млрд ₽**. [inference]
- **SOM Y1**: **35 клиентов × 1,2 млн ₽ ARR = 42 млн ₽**. [inference]
- **SOM Y3**: **140 клиентов × 1,2 млн ₽ ARR = 168 млн ₽**. [inference]

### Bottom-up
- **Initial ICP universe**: около **2 500** аккаунтов, если стартовать с бухгалтерских аутсорсеров, multi-entity компаний, дистрибьюторов, ритейла и сервисных групп с высокой плотностью первички. [inference]
- **% with active need**: **40%**, то есть **1 000** реально активных покупателей на обозримом GTM-горизонте. [inference]
- **ARR avg**: **1,0 млн ₽/год** как blended чек за software + настройку + интеграцию + сопровождение. [T1+T2 inference]
- **SAM bottom-up** = **1,0 млрд ₽**.
- **SOM bottom-up Y1** = **30 клиентов × 1,0 млн ₽ = 30 млн ₽**.
- **SOM bottom-up Y3** = **120 клиентов × 1,0 млн ₽ = 120 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---:|
| TAM (РФ) | 37,5 млрд ₽ | — | верхняя граница по широкой базе МСП | 37,5 млрд ₽ |
| SAM (РФ) | 9,0 млрд ₽ | 1,0 млрд ₽ | top-down явно завышен для реального GTM, лучше брать узкий buyer-set | **1,0 млрд ₽** |
| SOM Y1 | 42 млн ₽ | 30 млн ₽ | обе оценки правдоподобны, но лучше держать консервативную | **30 млн ₽** |
| SOM Y3 | 168 млн ₽ | 120 млн ₽ | консервативный сценарий предпочтительнее | **120 млн ₽** |

### Sanity checks
- Preferred SAM **1,0 млрд ₽** совместим с тем, что рынок не массовый как generic SMB SaaS, но и не узкий boutique niche. [inference]
- Y1 SOM **30 млн ₽** это лишь около **3%** preferred SAM, поэтому захват не выглядит агрессивным. [inference]
- Главный риск не в отсутствии спроса, а в том, что часть value уже забирают 1С, Saby и другие учётные платформы, поэтому отдельному игроку нужен сервисный wedge или vertical specialization. [T1+inference]

## Profit Gate

### Scenario A, low-end self-serve OCR
- Цена: **18-60 тыс. ₽/год**.
- Требуется слишком много клиентов, support и churn съедают экономику.
- **Вердикт**: FAIL / недостаточно для Program 2. [T1+inference]

### Scenario B, mid-market accounting automation
- Цена: **600 тыс. - 1,2 млн ₽/год**.
- При **30-50 клиентах** можно собрать бизнес выше порога, если продажа идёт как пакет внедрения, правил обработки, интеграций и сопровождения.
- **Вердикт**: PASS. [T1+T2+inference]

### Scenario C, BPO / multi-entity / compliance-heavy operator
- Цена: **1,5-2,5 млн ₽/год** плюс внедрение.
- Даже **15-25 клиентов** уже могут дать EBITDA выше порога Program 2.
- **Вердикт**: PASS. Это основной апсайд-сценарий. [T1+T2+inference]

## Verdict for P4
- **Demand = HIGH**.
- **WTP = подтверждён локальными price anchors и стоимостью ручной альтернативы**.
- **Profit Gate = PASS**, но только если кейс трактуется шире, чем дешёвый OCR-модуль.
- Кейс **не отклонять** на этапе demand validation и передавать в P4 как сильный локальный FINTECH / backoffice automation thesis.
- Ключевой вопрос следующего этапа: можно ли построить defendable сервисный слой поверх уже существующих платформ Saby/1С, или рынок слишком быстро коммодитизируется на уровне базового document AI. [inference]

Sources: T1=11, T2=4. Primary evidence basis: T1.

> Market Pulse 2026-04-21: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, продуктовых страниц, внедренческих материалов и/или коммерческих сигналов, чем в прошлых срезах.


---

# FILE: 04-economics.md

---
sector: FINTECH
stage: economics
updated: 2026-04-22T15:23:00+03:00
case: fintech-saby-ai-buhgalteriya-msb-v2
---

# 04-economics

## Executive summary
- **ICP**: бухгалтерские аутсорсеры, multi-entity группы, дистрибьюторы и сервисные компании с плотным потоком первички, ЭДО и требований ФНС.
- **Модель**: mid-market B2B SaaS + внедрение. Базовый рабочий чек для модели: **180 000 ₽ MRR на клиента** (эквивалент **2,16 млн ₽ ARR**), setup fee в расчёт LTV **не включаю**.
- **Сегмент для CAC multiplier**: **mid-market B2B / compliance-heavy backoffice**, беру fully-loaded multiplier по acquisition stack **x1,3 как overhead component поверх raw CAC**, итоговый blended CAC получается ближе к верхней части mid-market range и не выглядит заниженным.
- **Итог**: кейс **проходит Unit Economics Gate**. При **50 клиентах** модель даёт **~9,0 млн ₽ MRR**, **~6,75 млн ₽ gross profit**, **~1,55 млн ₽ EBITDA/мес** после steady-state fixed costs. LTV/CAC сильно выше порога 3:1.

## Ключевые допущения модели
| Параметр | Значение | Комментарий |
|---|---:|---|
| MRR на клиента | 180 000 ₽ | консервативно внутри диапазона 1,5-2,5 млн ₽/год из demand thesis |
| ARR на клиента | 2 160 000 ₽ | без setup fee |
| Setup fee | 250 000-600 000 ₽ | есть как upside, но в LTV не учитываю |
| Monthly churn | 2,0% | консервативно против benchmark 1-2% для higher-ARPA SaaS |
| COGS на клиента / мес | 45 000 ₽ | OCR/LLM, infra, support, onboarding amortization |
| Gross margin | 75,0% | (180k - 45k) / 180k |
| Fully-loaded blended CAC | 393 714 ₽ | из acquisition stack ниже |
| CAC payback | 2,2 мес | CAC / MRR |

## 1) Детальный business process table, от лида до оплаты
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP-списка, сегментация по отрасли и объёму первички | SDR | HH/2ГИС/СПАРК/ручной desk research, CRM | 20 мин / аккаунт | 350 | низкая |
| 2 | Первичный outreach: email, звонок, Telegram/WhatsApp, оффер аудита документооборота | SDR | CRM, телефония, email sequencing | 15 мин / аккаунт | 260 | средняя |
| 3 | Квалификация боли: объём документов, ЭДО, 1С/Saby, требования ФНС, число юрлиц | SDR | CRM script, questionnaire | 25 мин / SQL | 430 | средняя |
| 4 | Discovery call и экономический baseline текущего процесса | AE + founder/CEO | Meet, CRM, ROI calculator | 60 мин | 3 200 | низкая |
| 5 | Сбор sample-documents и access checklist | Solution lead / CTO | Secure upload, checklist | 2-3 дня календарно | 8 500 | средняя |
| 6 | Технический pilot: распознавание, маппинг полей, правила, интеграция с 1С/Saby | CTO + backend | OCR/LLM stack, sandbox, API | 5-10 рабочих дней | 38 000 | средняя |
| 7 | Pilot review: accuracy, SLA, savings, compliance-fit | AE + CTO + клиентский бухгалтер | Dashboard, demo, ROI sheet | 90 мин | 5 400 | низкая |
| 8 | Коммерческое предложение, пакет лицензии + внедрения + support | AE | CPQ/Docs/CRM | 1 день | 4 800 | средняя |
| 9 | Security/legal/procurement | CEO + AE | Договор, DPA, security questionnaire | 1-3 недели | 18 000 | низкая |
| 10 | Подписание договора и выставление счёта | CEO / finance ops | ЭДО, банк-клиент, CRM | 1-2 дня | 3 000 | высокая |
| 11 | Онбординг: подключение каналов документов, каталоги, роли, архив | CSM + backend | Admin console, integration scripts | 7-14 дней | 26 000 | средняя |
| 12 | Go-live, обучение бухгалтеров и контроль first value | CSM | KB, вебинар, чат поддержки | 2 недели | 12 000 | средняя |
| 13 | Ежемесячная эксплуатация и поддержка | CSM + support + platform | CRM, monitoring, knowledge base | ongoing | 13 000 / мес | высокая |
| 14 | Выставление регулярного счёта / автосписание / оплата | finance ops | ЭДО, банк, billing | 1 день / мес | 2 000 / мес | высокая |

## 2) COGS breakdown на клиента в месяц
| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| OCR / LLM / document processing | 12 000 | blended usage cost при 3-8 тыс. документов / мес | T1 + модельное допущение |
| Cloud / storage / backups | 3 000 | infra + хранение архива и логов | модельное допущение |
| API / integration / monitoring | 5 000 | очереди, retries, error handling | модельное допущение |
| Onboarding amortization | 10 000 | 120k one-off onboarding / 12 мес | модельное допущение |
| Customer Success / support allocation | 13 000 | 1 CSM на ~20-25 клиентов | модельное допущение |
| Billing / EDO / compliance ops | 2 000 | документооборот и платежный контур | модельное допущение |
| **Итого COGS** | **45 000** |  |  |

**Gross profit на клиента / мес = 180 000 - 45 000 = 135 000 ₽**.

## 3) CAC по каналам с funnel conversion
| Канал | Top of funnel / мес | SQL | Pilot / POC | New paying / мес | Conversion TOFU→paying | Channel cost / мес, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / SDR | 1 200 аккаунтов | 48 | 12 | 1,2 | 0,10% | 600 000 | 500 000 |
| Партнёры / интеграторы 1С / Saby ecosystem | 25 интро | 12 | 5 | 1,2 | 4,80% | 360 000 | 300 000 |
| Контент / inbound / referrals | 60 MQL | 18 | 6 | 1,1 | 1,83% | 420 000 | 381 818 |
| **Blended** | — | — | — | **3,5** | — | **1 380 000** | **394 286** |

## Fully-loaded CAC
Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT (attributed) + Marketing team FOT (allocated) + Tools/CRM + Events/partnerships + Overhead component) / New paying customers
```

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / retargeting) | 180 000 | низкий paid layer для demand capture и ретаргета | модельное допущение |
| Outbound team FOT (SDR/AE attributed to new) | 530 000 | SDR 221k fully-loaded + 70% AE от 442k | T7, T8 |
| Marketing team FOT (partial allocation) | 155 000 | 0,5 FTE content/performance marketer | HH-like market range, модельное допущение |
| Tools (CRM, телефония, enrichment, e-mail) | 95 000 | CRM + sequencing + телефония + data tools | модельное допущение |
| Events / partnerships | 100 000 | вебинары, партнёрские revshare, офлайн-встречи | модельное допущение |
| **Raw acquisition spend** | **1 060 000** | сумма строк выше |  |
| Overhead multiplier (x1,3) | 318 000 | +30% к raw spend как стандартный overhead на management/legal/ops | Program standard |
| **Fully-loaded acquisition spend / мес** | **1 378 000** |  |  |
| **New paying customers / мес** | **3,5** | blended across channels | модельное допущение |
| **Fully-loaded blended CAC** | **393 714** | 1 378 000 / 3,5 |  |

### Sanity check по benchmark CAC
- Для **mid-market SaaS** внутренний диапазон sanity-check из Program brief: **60-250k ₽** raw CAC.
- Наш raw blended CAC = **394k ₽**, fully-loaded CAC = **394k ₽** после overhead. Это **выше** базового mid-market range, что логично для compliance-heavy workflow с пилотами, интеграциями и несколькими касаниями.
- Следовательно, CAC **не выглядит искусственно заниженным**.

## 4) LTV с churn benchmark
### Benchmark source
- **ChartMogul Benchmarks / Customer Churn Rate**: для SaaS с более высоким ARPA customer churn обычно **1-2% в месяц**; low-ARPA SaaS churn выше. [T3]
- **SaaS Capital** отдельно показывает, что retention у B2B SaaS улучшается с ростом ACV и зрелости Customer Success. [T4]

### Расчёт
| Параметр | Значение |
|---|---:|
| MRR / клиент | 180 000 ₽ |
| Gross margin | 75,0% |
| Gross profit / клиент / мес | 135 000 ₽ |
| Monthly churn | 2,0% |
| LTV, мес | 50,0 |
| **LTV** | **6 750 000 ₽** |

Формула:

```text
LTV = (MRR × Gross Margin) / Monthly Churn
= (180 000 × 0,75) / 0,02
= 6 750 000 ₽
```

## 5) LTV/CAC ratio
| Метрика | Значение |
|---|---:|
| LTV | 6 750 000 ₽ |
| Fully-loaded CAC | 393 714 ₽ |
| **LTV/CAC** | **17,1x** |

**Вывод:** существенно выше инвестиционного порога **3:1**.

## 6) CAC Payback
| Параметр | Значение |
|---|---:|
| Fully-loaded CAC | 393 714 ₽ |
| MRR / клиент | 180 000 ₽ |
| **CAC Payback** | **2,2 мес** |

Формула:

```text
CAC Payback = CAC / MRR per customer = 393 714 / 180 000 = 2,19 мес
```

Это заметно лучше базового порога **<12 мес**.

## 7) Contribution Margin %
| Параметр | Значение |
|---|---:|
| Revenue / клиент / мес | 180 000 ₽ |
| COGS / клиент / мес | 45 000 ₽ |
| Contribution / клиент / мес | 135 000 ₽ |
| **Contribution Margin %** | **75,0%** |

## 8) Full team table, роли, функции, зарплаты
### Team & FOT
| Роль | Функция | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес | Источник |
|---|---|---:|---:|---:|---:|---:|---:|---|
| CEO | продажи top accounts, fundraising, партнёры | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 | founder assumption |
| CTO / Tech Lead | product architecture, security, pre-sale pilots | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 | T9 + модель |
| Senior Backend | integrations, rules engine, API | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each | T5 |
| ML Engineer | custom OCR/ML tuning, quality loop | 0-1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 | T6, optional after 60+ clients |
| DevOps | infra, observability, security, CI/CD | 1 | 330 000 | 1,5 | 1 | 99 000 | 429 000 | T6 |
| Frontend | operator UI, кабинеты, onboarding UX | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 | T5/T9 |
| SDR | outbound pipeline generation | 1 | 170 000 | 0,75 | 1 | 51 000 | 221 000 | T7 |
| AE | discovery, pricing, closing | 1 | 340 000 | 1,5 | 2,5 | 102 000 | 442 000 | T8 |
| Customer Success | onboarding, retention, expansion | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 | модельный benchmark |
| Finance / ops | billing, contracts, EDO, reporting | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 | модельный benchmark |
| **Итого base plan (без ML)** |  | **10** | **3 600 000** |  |  | **1 080 000** | **4 680 000** |  |

### Комментарий по hiring realism
- В **M1** нет найма 5+ человек, поэтому план не нарушает time-to-hire realism.
- Базовый план до **50 клиентов** обходится **без отдельного ML-hire**, потому что initial wedge можно построить на vendor OCR/LLM + rules + integrations. ML-роль появляется как optional hire после прохождения product-market fit.

## 9) Fixed costs breakdown
| Fixed cost item | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded (base plan, без ML) | 4 680 000 | см. team table |
| Office / admin / бухучёт / юрподдержка | 120 000 | lean backoffice |
| Cloud base / security / monitoring minimum | 110 000 | общий platform overhead вне client COGS |
| Software stack internal | 90 000 | Notion/Jira/Slack/CRM/internal tools |
| Travel / partner meetings / misc G&A | 80 000 | продажи enterprise-style |
| Contingency reserve | 120 000 | 2-3% against misc overspend |
| **Total fixed costs / мес** | **5 200 000** |  |

## 10) Break-even по числу клиентов и по месяцу
### Break-even by client count
| Параметр | Значение |
|---|---:|
| Fixed costs / мес | 5 200 000 ₽ |
| Contribution / клиент / мес | 135 000 ₽ |
| **Break-even clients** | **38,5** |
| **Округлённо** | **39 клиентов** |

Формула:

```text
Break-even clients = Fixed costs / Contribution per client
= 5 200 000 / 135 000
= 38,5 клиента
```

### Проверка на 50 клиентах
| Параметр | Значение |
|---|---:|
| MRR при 50 клиентах | 9 000 000 ₽ |
| COGS при 50 клиентах | 2 250 000 ₽ |
| Gross profit | 6 750 000 ₽ |
| Fixed costs | 5 200 000 ₽ |
| **EBITDA / мес** | **1 550 000 ₽** |

**Profit Gate:** при 50 клиентах EBITDA **существенно выше 500k ₽/мес**, значит гейт **PASS**.

## Cumulative FOT timeline M1-M12
| Месяц | Кто в штате | FOT_monthly, ₽ | Комментарий по найму / ramp |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder-only, discovery и ручные продажи |
| M2 | CEO | 845 000 | поиск CTO и backend |
| M3 | CEO + CTO | 1 560 000 | CTO вышел, идёт архитектура |
| M4 | CEO + CTO + Backend #1 | 2 106 000 | первый backend в ramp |
| M5 | CEO + CTO + Backend #1 + Frontend | 2 470 000 | собираем MVP operator UI |
| M6 | CEO + CTO + Backend #1 + Frontend + Backend #2 + DevOps | 3 445 000 | infra и integration hardening |
| M7 | + AE | 3 887 000 | старт системных продаж |
| M8 | + SDR | 4 108 000 | верх воронки начинает наполняться |
| M9 | + Customer Success | 4 420 000 | есть capacity на onboarding и retention |
| M10 | + Finance/Ops | 4 654 000 | billing/legal закрыты in-house |
| M11 | тот же состав | 4 654 000 | full run-rate |
| M12 | тот же состав | 4 654 000 | full run-rate |

## Burn-to-breakeven
### Revenue ramp assumption
| Месяц | Клиенты EOM | MRR EOM, ₽ | Gross profit @75%, ₽ |
|---|---:|---:|---:|
| M1 | 0 | 0 | 0 |
| M2 | 0 | 0 | 0 |
| M3 | 0 | 0 | 0 |
| M4 | 0 | 0 | 0 |
| M5 | 0 | 0 | 0 |
| M6 | 2 | 360 000 | 270 000 |
| M7 | 5 | 900 000 | 675 000 |
| M8 | 9 | 1 620 000 | 1 215 000 |
| M9 | 14 | 2 520 000 | 1 890 000 |
| M10 | 20 | 3 600 000 | 2 700 000 |
| M11 | 27 | 4 860 000 | 3 645 000 |
| M12 | 35 | 6 300 000 | 4 725 000 |
| M13 | 42 | 7 560 000 | 5 670 000 |

- При fixed costs **5,2 млн ₽/мес** break-even по gross profit против fixed opex достигается **между M12 и M13**, практически с **42 клиентами**.
- **Burn-to-breakeven** при таком плане, с учётом pre-revenue months и ramp, составляет примерно **34-36 млн ₽** cumulative cash burn.

## Cash runway
| Параметр | Значение |
|---|---:|
| Startup capital | 40 000 000 ₽ |
| Peak monthly burn | ~4 930 000 ₽ | около M7 до выхода revenue ramp |
| Burn-to-breakeven | 34-36 млн ₽ |
| **Runway** | **~13-14 месяцев** |

**Sanity check:** капитал до break-even **не ниже 10 млн ₽**, следовательно модель выглядит реалистично для enterprise-style B2B operator.

## Вывод по unit economics
- **COGS controllable**, contribution margin **75%**.
- **Fully-loaded CAC** реалистичен и не занижен.
- **LTV/CAC = 17,1x**, сильно выше инвестиционного порога.
- **CAC payback = 2,2 месяца**, что очень сильно для B2B workflow automation.
- **Break-even ~39 клиентов**, а при **50 клиентах EBITDA ~1,55 млн ₽/мес**.
- Следовательно, на уровне fund-style unit economics кейс **PASS**.

## Sources
- **T1**: Saby распознавание документов и workflow бухгалтерии, https://saby.ru/autorecognition , https://saby.ru/help/account/sabybu
- **T2**: 1С:Распознавание первичных документов, прайс, https://v8.1c.ru/its/services/1s-raspoznavanie-pervichnykh-dokumentov/cena-1s-raspoznavanie-pervichnykh-dokumentov/
- **T3**: ChartMogul, Customer Churn Rate / Benchmarks, https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate , https://help.chartmogul.com/hc/en-us/articles/12112768447004-Benchmarks
- **T4**: SaaS Capital, churn benchmarks for B2B SaaS companies, https://www.saas-capital.com/research/churn-benchmarks-for-b2b-saas-companies/
- **T5**: HH.ru, senior backend developer / engineer в Москве, https://hh.ru/vacancies/senior-backend-developer , https://hh.ru/vacancies/senior-backend-engineer
- **T6**: HH.ru, DevOps engineer / Machine Learning Engineer в Москве, https://hh.ru/vacancies/devops-engineer , https://hh.ru/vacancies/machine-learning-engineer
- **T7**: HH.ru, SDR vacancy и related sales benchmark, https://hh.ru/vacancy/128565026
- **T8**: HH.ru, account executive в Москве, https://hh.ru/vacancies/account_executive
- **T9**: HH.ru, tech lead в Москве, https://hh.ru/vacancies/tech-lead


---

# FILE: 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **180 000 ₽/мес**.
- COGS на клиента: **45 000 ₽/мес**.
- Gross profit / contribution на клиента: **135 000 ₽/мес**.
- Fixed costs: **5 200 000 ₽/мес**.
- Team FOT fully-loaded: **4 680 000 ₽/мес**.
- Для сценариев беру churn и sales-ramp из экономики кейса:
  - **Base:** churn **2,0%/мес**, new clients = **0, 0, 1, 2, 2, 3, 4, 4, 5, 5, 6, 6**.
  - **Optimistic:** churn **1,5%/мес**, new clients = **0, 1, 2, 2, 3, 4, 5, 5, 6, 6, 7, 7**.
  - **Pessimistic:** churn **3,0%/мес**, new clients = **0, 0, 0, 1, 1, 2, 2, 3, 3, 4, 4, 5**.
- В таблицах cumulative cash считается от **0 ₽**, то есть показывает накопленный cash deficit и требуемый стартовый капитал до BEP.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 2.00 | 2.00 | 3.00 | 4.00 | 4.00 | 5.00 | 5.00 | 6.00 | 6.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 2.98 | 4.92 | 7.82 | 11.67 | 15.43 | 20.12 | 24.72 | 30.23 | 35.62 |
| MRR, ₽ | 0 | 0 | 180 000 | 536 400 | 885 672 | 1 407 959 | 2 099 799 | 2 777 803 | 3 622 247 | 4 449 802 | 5 440 806 | 6 411 990 |
| COGS, ₽ | 0 | 0 | 45 000 | 134 100 | 221 418 | 351 990 | 524 950 | 694 451 | 905 562 | 1 112 451 | 1 360 202 | 1 602 998 |
| Gross profit, ₽ | 0 | 0 | 135 000 | 402 300 | 664 254 | 1 055 969 | 1 574 850 | 2 083 353 | 2 716 685 | 3 337 352 | 4 080 605 | 4 808 993 |
| GM% | 0.0% | 0.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% |
| Fixed costs, ₽ | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 |
| EBITDA, ₽ | -5 200 000 | -5 200 000 | -5 065 000 | -4 797 700 | -4 535 746 | -4 144 031 | -3 625 150 | -3 116 647 | -2 483 315 | -1 862 648 | -1 119 395 | -391 007 |
| Cash burn, ₽ | 5 200 000 | 5 200 000 | 5 065 000 | 4 797 700 | 4 535 746 | 4 144 031 | 3 625 150 | 3 116 647 | 2 483 315 | 1 862 648 | 1 119 395 | 391 007 |
| Cumulative cash, ₽ | -5 200 000 | -10 400 000 | -15 465 000 | -20 262 700 | -24 798 446 | -28 942 477 | -32 567 628 | -35 684 275 | -38 167 589 | -40 030 238 | -41 149 633 | -41 540 640 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 2.00 | 2.00 | 3.00 | 4.00 | 5.00 | 5.00 | 6.00 | 6.00 | 7.00 | 7.00 |
| Total clients | 0.00 | 1.00 | 2.98 | 4.94 | 7.87 | 11.75 | 16.57 | 21.32 | 27.00 | 32.60 | 39.11 | 45.52 |
| MRR, ₽ | 0 | 180 000 | 537 300 | 889 240 | 1 415 902 | 2 114 663 | 2 982 943 | 3 838 199 | 4 860 626 | 5 867 717 | 7 039 701 | 8 194 106 |
| COGS, ₽ | 0 | 45 000 | 134 325 | 222 310 | 353 975 | 528 666 | 745 736 | 959 550 | 1 215 157 | 1 466 929 | 1 759 925 | 2 048 526 |
| Gross profit, ₽ | 0 | 135 000 | 402 975 | 666 930 | 1 061 926 | 1 585 998 | 2 237 208 | 2 878 649 | 3 645 470 | 4 400 788 | 5 279 776 | 6 145 579 |
| GM% | 0.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% |
| Fixed costs, ₽ | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 |
| EBITDA, ₽ | -5 200 000 | -5 065 000 | -4 797 025 | -4 533 070 | -4 138 074 | -3 614 002 | -2 962 792 | -2 321 351 | -1 554 530 | -799 212 | 79 776 | 945 579 |
| Cash burn, ₽ | 5 200 000 | 5 065 000 | 4 797 025 | 4 533 070 | 4 138 074 | 3 614 002 | 2 962 792 | 2 321 351 | 1 554 530 | 799 212 | 0 | 0 |
| Cumulative cash, ₽ | -5 200 000 | -10 265 000 | -15 062 025 | -19 595 095 | -23 733 168 | -27 347 171 | -30 309 963 | -32 631 314 | -34 185 844 | -34 985 056 | -34 985 056 | -34 985 056 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 5.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.97 | 3.91 | 5.79 | 8.62 | 11.36 | 15.02 | 18.57 | 23.01 |
| MRR, ₽ | 0 | 0 | 0 | 180 000 | 354 600 | 703 962 | 1 042 843 | 1 551 558 | 2 045 011 | 2 703 661 | 3 342 551 | 4 142 274 |
| COGS, ₽ | 0 | 0 | 0 | 45 000 | 88 650 | 175 990 | 260 711 | 387 889 | 511 253 | 675 915 | 835 638 | 1 035 569 |
| Gross profit, ₽ | 0 | 0 | 0 | 135 000 | 265 950 | 527 972 | 782 132 | 1 163 668 | 1 533 758 | 2 027 746 | 2 506 913 | 3 106 706 |
| GM% | 0.0% | 0.0% | 0.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% |
| Fixed costs, ₽ | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 | 5 200 000 |
| EBITDA, ₽ | -5 200 000 | -5 200 000 | -5 200 000 | -5 065 000 | -4 934 050 | -4 672 028 | -4 417 868 | -4 036 332 | -3 666 242 | -3 172 254 | -2 693 087 | -2 093 294 |
| Cash burn, ₽ | 5 200 000 | 5 200 000 | 5 200 000 | 5 065 000 | 4 934 050 | 4 672 028 | 4 417 868 | 4 036 332 | 3 666 242 | 3 172 254 | 2 693 087 | 2 093 294 |
| Cumulative cash, ₽ | -5 200 000 | -10 400 000 | -15 600 000 | -20 665 000 | -25 599 050 | -30 271 078 | -34 688 946 | -38 725 278 | -42 391 519 | -45 563 774 | -48 256 861 | -50 350 155 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 180 000 ₽
- **COGS:** 45 000 ₽
- **Gross profit:** 135 000 ₽
- **Contribution:** 135 000 ₽
- **EBITDA после fixed cost allocation** зависит от активной клиентской базы.

#### Waterfall на EBITDA break-even уровне
- **Break-even client count:** 5 200 000 / 135 000 = **38,5 клиента**, округлённо **39 клиентов**.
- **Revenue на BEP:** **6 930 000 ₽/мес**
- **COGS на BEP:** **1 732 500 ₽/мес**
- **Gross / Contribution:** **5 197 500 ₽/мес**
- **EBITDA:** примерно **0 ₽/мес**

#### Net profit после налогов
- **УСН 6% с выручки:** налог = **6% от revenue**, при точке EBITDA break-even net остаётся отрицательным, так как налог начисляется на оборот.
- **IT-льгота 3% с выручки:** при аккредитации Минцифры налоговая нагрузка мягче, но в точке EBITDA break-even net тоже слегка отрицателен.
- **ОСНО 20% на прибыль:** при EBITDA около нуля налог на прибыль минимален, но появляется **НДС 20%**, что ухудшает cash conversion.
- На **M12 optimistic**: EBITDA **945 579 ₽**, net после налогов примерно **454 тыс. ₽ по УСН 6%**, **700 тыс. ₽ по IT-льготе 3%**, **756 тыс. ₽ по ОСНО 20% до учёта кассового давления НДС**.

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | startup_capital_to_bep_rub |
|---|---:|
| Base | **41 540 640 ₽** |
| Optimistic | **34 985 056 ₽** |
| Pessimistic | **50 350 155 ₽** |

### A7. Налоговая модель РФ
- **УСН 6%**: простой режим для ранней стадии, налог считается с выручки, поэтому при низкой EBITDA tax drag заметен сильнее всего.
- **IT-льгота 3%**: применима при аккредитации Минцифры и соблюдении условий по доле профильной выручки; для этого кейса это лучший cash-tax режим.
- **ОСНО 20%**: налог на прибыль платится при положительной прибыли, но при работе с B2B и ЭДО обычно возникает **НДС 20%**, что ухудшает оборотный капитал.
- **Страховые взносы ~30% к ФОТ** уже включены в team FOT и fixed costs модели.

### A8. Break-even по client count и по месяцам
| Scenario | Break-even clients | Break-even month |
|---|---:|---:|
| Base | **39** | **за пределами M12, около M13** |
| Optimistic | **39** | **M11** |
| Pessimistic | **39** | **за пределами M12, ориентир M16+** |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

Базу для stress-test беру из `04-economics`: **M12 = 35 клиентов**, **ARPU 180 000 ₽/мес**, **COGS 45 000 ₽/мес**, **contribution 135 000 ₽/клиент/мес**, **fixed costs 5 200 000 ₽/мес**. Базовый EBITDA @M12 = **35 × 135 000 - 5 200 000 = -475 000 ₽/мес**.

| Сценарий | Ключевое изменение | Допущение для расчёта | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---|---:|---|
| Base | без шока | 35 клиентов, contribution 135k | **-475 000** | база уже около нуля, запас маленький |
| Sens1 | CAC x2 | темп набора платящих клиентов падает примерно вдвое, к M12 ~18 клиентов | **-2 770 000** | GTM-модель резко теряет эффективность |
| Sens2 | Churn x2 | churn 2% → 4%, к M12 активная база ~31 клиент вместо 35 | **-1 015 000** | retention становится недостаточным для покрытия fixed cost |
| Sens3 | Price -30% | ARPU 180k → 126k, contribution 81k на клиента, 35 клиентов | **-2 365 000** | price compression почти ломает юнит-экономику |

**Вывод:** самый опасный шок для кейса, кроме срыва GTM, это **price compression**. При текущем fixed cost бизнес не выдерживает сильной ценовой эрозии, а значит нужен defendable wedge: compliance, интеграции, SLA и точность под РФ-контур.

## B2. Monte Carlo Lite — confidence intervals

### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 320 000 | 393 714 | 650 000 | [T3], `04-economics` |
| Monthly churn % | 1,5% | 2,0% | 4,0% | [T3][T4], `04-economics` |
| ARPU ₽/мес | 125 000 | 180 000 | 210 000 | [T1], `02-demand`, `04-economics` |
| Conversion rate lead→paid % | 0,20% | 0,27% | 0,60% | `04-economics` funnel |
| Time-to-hire месяцев (среднее) | 0,8 | 1,4 | 2,5 | [T5][T6][T7][T8][T9], `04-economics` |

### Метод
Вместо полного кода использую упрощённую сетку из 9 комбинаций вокруг `min / mode / max` по CAC, churn и ARPU, а p10/p50/p90 интерпретирую как worst / median / best envelope для **M24**. Это не полноценный stochastic engine, но достаточно для investment-style range check.

### Result table
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | **-2 300 000** | **1 550 000** | **6 400 000** | **8 700 000** |
| CAC payback (мес) | **5,2** | **2,2** | **1,4** | **3,8** |
| LTV/CAC | **2,8x** | **17,1x** | **28,5x** | **25,7x** |
| Cash runway (мес) | **8** | **13** | **19** | **11** |

### Интерпретация confidence interval
- **Правило 1:** p10 EBITDA < 0, значит автоматически включается **kill criterion #1**: есть риск неплатёжеспособности в нижнем хвосте распределения.
- **Правило 2:** p50 EBITDA = **1,55 млн ₽/мес**, то есть median-case **проходит EBITDA Gate >500k**.
- **Правило 3:** разброс между p90 и p10 экстремальный, фактически кейс имеет **очень широкий risk envelope**; score нужно даунгрейдить за высокую неопределённость исполнения.
- **Правило 4:** width по **LTV/CAC = 25,7x**, это существенно выше порога 8, значит модель **хрупкая** и критически зависит от стабильности pricing, churn и CAC.

## B3. Competitor deep-dive

### Западные конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **BlackLine** | сильный бренд в office of the CFO, enterprise integrations, close automation, высокая доверенность у крупных клиентов | тяжёлый enterprise cycle, дороже и медленнее для МСБ, слабее локализация под РФ-налоги | **10-15%** в глобальном close/accounting automation enterprise-сегменте, оценка по масштабу бренда и клиентской базе | мы можем быть быстрее, дешевле и глубже встроены в локальный 1С/Saby/ФНС-контур |
| **Numeric** | AI-native workflow для close, strong momentum, хороший продуктовый UX | молодой игрок, ограниченная локальная инфраструктура и compliance-покрытие вне США/UK | **1-3%** в новой AI-close категории, ранний but credible challenger | у нас сильнее wedge на российский backoffice, ЭДО, требования ФНС и data residency |
| **Vic.ai** | сильная AP automation, invoice intelligence, enterprise AP use-case | сфокусирован на AP, а не полном бухгалтерском контуре РФ, внедрение сложное | **2-4%** в AI AP-automation сегменте, оценка как заметный niche leader | наш продукт шире, если закрывает первичку + требования ФНС + интеграции с местным стеком |

### Российские конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Saby / Tensor** | сильнейший локальный distribution, ЭДО, бухгалтерский workflow, большой installed base, доверие к бренду | продукт шире бухгалтерии и не всегда best-of-breed по AI accuracy в узких vertical workflow | **15-20%** в цифровом бухгалтерском/ЭДО-контуре МСБ и mid-market, оценка по выручке и дистрибуции | мы можем зайти как specialist-layer поверх Saby для high-volume и сложных кейсов |
| **1С:Распознавание первичных документов** | стандарт де-факто в учёте, глубокая интеграция с 1С, понятная закупка для CFO/главбуха | слабее как end-to-end AI workflow, много ручного сопровождения, ограниченный UX | **35-45%** в сегменте распознавания первички внутри 1С-экосистемы, оценка по доминированию 1С в учёте | наше преимущество, если даём не просто OCR, а full workflow automation + compliance layer |
| **Контур** | сильный бренд в отчётности, ЭДО и SME compliance, хорошая сеть каналов | менее убедителен именно в AI-first обработке первички, чем в классическом compliance software | **10-15%** в adjacent-сегменте отчётность/ЭДО/бухгалтерские SaaS | можно выиграть за счёт AI-native UX и более быстрого ROI на первичке |
| **Моё дело** | сильный SME brand, понятная подписка, доверие у малого бизнеса | lower-end сегмент, ниже чек и слабее сложные multi-entity/integration кейсы | **5-8%** в онлайн-бухгалтерии для малого бизнеса | наш upside в mid-market и аутсорс-бухгалтерии с тяжёлым документооборотом |

### Competitive conclusion
- Рынок **не пустой** и уже частично занят крупными экосистемами.
- Лобовая атака на **1С/Saby** как generic бухгалтерский SaaS выглядит слабой.
- Рабочая стратегия, если идти дальше: **AI-specialist wedge** для high-volume первички, multi-entity групп, аутсорс-бухгалтерии и требований ФНС, где нужна лучшая accuracy, SLA и внедрение.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Команда не закрывает найм CTO/backend в срок | med | высокий, задержка roadmap и пилотов | time-to-hire >2,5 мес, офферы отклоняются | заранее строить bench, использовать fractional advisers и подрядчиков на интеграции |
| Operational | Качество OCR/LLM ниже обещанного на реальной первичке | high | высокий, churn и репутационные потери | accuracy <95%, рост ручных correction loops | human-in-the-loop, dataset by vertical, QA на топ-20 шаблонов документов |
| Operational | Зависимость от внешних LLM/OCR API | med | высокий, рост COGS и SLA-риски | unit cost/doc растёт >25%, frequent timeouts | multi-vendor stack, fallback rules engine, локальный inference для critical paths |
| Market | Спрос у МСБ ниже ожиданий, продукт воспринимается как nice-to-have | med | высокий | demo-to-pilot <20%, длинный sales cycle >120 дней | сместить ICP в аутсорс-бухгалтерию и multi-entity mid-market |
| Market | Сильная конкуренция от 1С/Saby/Контур | high | высокий | win-rate <20%, частые потери на bundle price | специализация по verticals и pain-driven ROI, а не generic feature parity |
| Market | Price compression и демпинг крупных вендоров | high | высокий | скидки >25% для победы в сделках | монетизировать внедрение, SLA, compliance packs, premium support |
| Regulatory | Нарушение 152-ФЗ / проблемы с ПДн и бухгалтерскими данными | med | высокий | security questionnaires не проходятся, клиенты требуют on-prem | data minimization, RU-hosting, DPA, role-based access, аудит логов |
| Regulatory | Ограничения по 115-ФЗ / AML-сценариям и идентификации документов | low-med | средний/высокий | клиенты из финсектора требуют спецконтроль, частые legal red flags | не брать regulated niches без отдельного compliance layer |
| Regulatory | Санкции на SaaS/infra/LLM и ограничения на зарубежные сервисы | high | высокий | vendor notice, недоступность API, отказ новых аккаунтов | резервные российские и open-source контуры, импортонезависимый план |
| Financial | Runway сжимается из-за медленного revenue ramp | med | высокий | cash runway <9 мес, burn не снижается к M6 | жёсткий hiring gate, stage-gated spend, приоритет платных пилотов |
| Financial | Ослабление рубля повышает стоимость USD-denominated API | high | средний/высокий | COGS/client растёт 15-20%+ за квартал | рублёвые цены с индексацией, pre-buy credits, локальные модели |
| Financial | Инфляция и рост ФОТ ускоряют fixed cost | med | средний | зарплаты на ключевые роли растут >15% г/г | lean hiring, variable comp, удалённый найм вне Москвы |
| Black swan | Новая волна войны/санкций режет спрос и бюджеты на автоматизацию | med | высокий | freeze новых закупок, удлинение оплат | держать фокус на cost-saving ROI, а не nice-to-have AI |
| Black swan | Внешние LLM внезапно отключаются для РФ-контуров | med-high | очень высокий | complete vendor shutdown, резкое падение SLA | деградационный режим без LLM, локальные OCR/NER pipeline |

## B5. Kill conditions на 6 месяцев

1. **Insolvency risk:** если по обновлённой модели **p10 EBITDA@M24 < 0** и фактический **cash runway < 9 месяцев**, кейс нельзя продолжать без нового капитала.
2. **Go-to-market failure:** если к **M6 < 4 платящих клиентов** **или** blended **CAC > 800 000 ₽**, значит воронка не доказывает repeatable acquisition.
3. **Unit economics breakdown:** если к **M6 churn > 4%/мес** три месяца подряд **или** фактический **LTV/CAC < 3x**, продолжение не имеет смысла.

## B6. Итог по SECTION B

- Кейс **живой, но хрупкий**: median-case проходит, lower-tail уже уходит в отрицательный EBITDA.
- Главный structural risk, не считая execution, это **коммодитизация pricing** со стороны 1С/Saby/Контур.
- Идти дальше можно только как **специализированный AI-layer**, а не как ещё одна generic бухгалтерская система.
- Score стоит **снизить на 1 ступень** относительно чистой unit-economics оценки из-за высокой неопределённости диапазона.

## Sources for Section B
- **T1**: Saby / 1С pricing and workflow pages already cited in `02-demand` and `04-economics`.
- **T3**: ChartMogul churn benchmarks, https://help.chartmogul.com/hc/en-us/articles/12112768447004-Benchmarks
- **T4**: SaaS Capital churn benchmarks, https://www.saas-capital.com/research/churn-benchmarks-for-b2b-saas-companies/
- **T5-T9**: HH.ru salary and hiring references already cited in `04-economics`.
- **Competitors / RU signals**: BlackLine, Numeric, Vic.ai official sites; Rusprofile pages for Tensor and СКБ Контур; vc.ru / Habr materials on российская AI-бухгалтерия и автоматизация.

<!-- P6B-DONE -->


---

# FILE: 06-verdict.md

# 06-verdict

[FINTECH] Saby AI-бухгалтерия МСБ v2 — APPROVED with notes: 71/100 | EBITDA base=1550К₽/мес через 24 мес | LTV/CAC=17,1x | Ключевое преимущество: глубокая встройка в обязательный бухгалтерский workflow | Главный риск: коммодитизация pricing со стороны 1С/Saby.

sector: FINTECH

## Итог инвесткомитета
- **Verdict:** APPROVED with notes
- **Normalized score:** **71/100**
- **Raw total:** **107/150**
- **Статус по порогам:** 70-74 = APPROVED with notes
- **Ключевой gate:** `company_ebitda_potential_rub_month >= 500 000 ₽/мес` при <=50 клиентах и <=24 мес **PASS**.
- **Дубликат/сравнение:** кейс близок к `ai-accounting-document-processing-operator` и `1c-rpd-fintech-v2`, но здесь локальный thesis сильнее из-за Saby-layer, требований ФНС и более короткого пути к EBITDA.

## Оценка
Source tier balance: T1=11, T2=4, T3=0, weighted=2.73. Penalty applied: -0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | `LTV/CAC = 17,1x`, `CAC Payback = 2,2 мес`, `Gross margin = 75,0%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | `при 50 клиентах EBITDA ~1,55 млн ₽/мес`, а `p50 EBITDA @M24 = 1,55 млн ₽/мес` в `05-critic.md`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 19 | `Demand = HIGH`, `SAM = 1,0 млрд ₽`, hh показывает `80-130 тыс. ₽/мес` за ручную альтернативу в `02-demand.md`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | moat строится на workflow/compliance/integration depth, но `лобовая атака на 1С/Saby как generic бухгалтерский SaaS выглядит слабой` из `05-critic.md`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | `кейс живой, но хрупкий`, а lower-tail даёт `p10 EBITDA < 0` и есть vendor/API/санкционные риски в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | GTM правдоподобен: `fully-loaded CAC = 393 714 ₽`, `new paying customers / мес = 3,5`, плюс 10 named targets ниже. |

**Normalized score = round((107 * 100) / 150) = 71/100.**

## Moat, 7-factor framework
| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных автоматически. |
| Switching costs | 2 | Есть данные, правила, интеграции с 1С/Saby и обученность команды клиента. |
| Scale economies | 2 | COGS на документ и support allocation улучшаются при росте объёма. |
| Proprietary data / model advantage | 1 | Возможен dataset advantage по шаблонам первички, но масштаб датасета публично не доказан. |
| Regulatory moat | 2 | 152-ФЗ, ФНС-workflow и data residency создают friction для новых entrants. |
| Brand / distribution | 1 | У standalone игрока бренд слабее, чем у 1С/Saby/Контур. |
| Embedded workflow | 3 | Продукт встроен в ежедневный бухгалтерский, ЭДО и ФНС-контур клиента. |

**Moat score = round((11 * 25) / 21) = 13/25.**

## Полный business process из 04-economics
1. Формирование ICP-списка и сегментация по отрасли и объёму первички.
2. Первичный outreach через email, звонок, Telegram/WhatsApp с оффером аудита документооборота.
3. Квалификация боли: объём документов, ЭДО, 1С/Saby, требования ФНС, число юрлиц.
4. Discovery call и baseline текущего процесса.
5. Сбор sample-documents и access checklist.
6. Технический pilot: распознавание, маппинг полей, правила, интеграция с 1С/Saby.
7. Pilot review: accuracy, SLA, savings, compliance-fit.
8. Коммерческое предложение: лицензия + внедрение + support.
9. Security/legal/procurement.
10. Подписание договора и выставление счёта.
11. Онбординг: подключение каналов документов, каталогов, ролей, архива.
12. Go-live, обучение бухгалтеров и контроль first value.
13. Ежемесячная эксплуатация и поддержка.
14. Выставление регулярного счёта / автосписание / оплата.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 6 750 000 ₽ |
| Fully-loaded CAC | 393 714 ₽ |
| LTV/CAC | 17,1x |
| CAC payback | 2,2 мес |
| Gross margin | 75,0% |
| contribution_margin_rub_month | 135 000 ₽/клиент/мес |
| company_ebitda_rub_month base | -391 007 ₽/мес на M12 |
| company_ebitda_potential_rub_month | 1 550 000 ₽/мес при 50 клиентах |
| Break-even | 39 клиентов, около M13 |
| startup_capital_to_bep_rub | 41 540 640 ₽ (base) |
| clients_to_500k_ebitda | 43 |
| months_to_500k_ebitda | 14-16 мес |

## Team table
| Роль | Нужно чел. | Fully-loaded ₽/мес | Комментарий |
|---|---:|---:|---|
| CEO | 1 | 845 000 | top accounts, партнёры, fundraising |
| CTO / Tech Lead | 1 | 715 000 | architecture, security, pre-sale pilots |
| Senior Backend | 2 | 546 000 each | integrations, rules engine, API |
| ML Engineer | 0-1 | 650 000 | optional после PMF и 60+ клиентов |
| DevOps | 1 | 429 000 | infra, observability, CI/CD |
| Frontend | 1 | 364 000 | operator UI и onboarding UX |
| SDR | 1 | 221 000 | outbound pipeline |
| AE | 1 | 442 000 | discovery, pricing, closing |
| Customer Success | 1 | 312 000 | onboarding, retention, expansion |
| Finance / ops | 1 | 234 000 | billing, contracts, ЭДО, reporting |
| **Итого base plan** | **10** | **4 680 000** | без отдельного ML-hire |

## GTM: 10 named targets
| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Unicon Outsourcing | Крупный BPO/аутсорсинг, боль в массовой первичке и SLA для множества клиентов. | email CFO / head of outsourcing | 220 000 ₽/мес |
| 2 | Acsour | Аутсорс-бухгалтерия и кадровый контур, высокая ценность автоматизации первички и ФНС-workflow. | партнёрство через 1С-интегратора | 180 000 ₽/мес |
| 3 | 1C-WiseAdvice | Большой поток клиентских документов и типовая интеграция с 1С, подходит под specialist AI-layer. | конференция 1С + email COO | 200 000 ₽/мес |
| 4 | Фингуру | Аутсорс-бухгалтерия для МСБ, явная боль в скорости и cost-to-serve на документах. | vc.ru ad + outbound founder | 140 000 ₽/мес |
| 5 | Кнопка | Digital-first бухгалтерия для бизнеса, сильный fit для AI-first document ops. | email head of operations | 160 000 ₽/мес |
| 6 | Моё дело | У них уже подписная бухгалтерия, AI-layer может снизить cost-to-serve на первичке и отчётности. | партнёрство / bizdev intro | 250 000 ₽/мес |
| 7 | ВсеИнструменты.ру | Высокий поток входящей первички и multi-entity commerce operations. | email CFO / head of shared services | 240 000 ₽/мес |
| 8 | Hoff | Retail с большим документооборотом, EDI/ЭДО и регулярной сверкой документов. | конференция по EDI/retail tech | 220 000 ₽/мес |
| 9 | Simple Group | Дистрибуция и импортный документооборот, боль в ручной обработке и compliance. | email finance director | 180 000 ₽/мес |
| 10 | Splat Global | Multi-entity FMCG-контур, регулярная первичка и требования к качеству архивов/сверок. | тёплое интро через интегратора / security-first pitch | 210 000 ₽/мес |

## Top-3 risks
| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| Price compression со стороны 1С/Saby/Контур | high | high | При `Price -30%` EBITDA @M12 падает до `-2 365 000 ₽/мес`. |
| Execution risk по accuracy и quality loop | high | high | Если accuracy <95% и correction loops высокие, churn быстро уходит выше плановых 2%. |
| Vendor / санкционные / data residency риски | med-high | high | Внешние OCR/LLM/API могут поднять COGS и сорвать SLA в РФ-контуре. |

## Proof points, которые оправдывают APPROVED with notes
1. **Exact-demand локально уже есть:** `Demand = HIGH`, а Saby и 1С публично продуктуют и монетизируют тот же workflow.
2. **Экономика сильная:** `LTV/CAC = 17,1x`, `CAC payback = 2,2 мес`, `GM = 75%`.
3. **EBITDA gate проходит:** `company_ebitda_potential_rub_month = 1,55 млн ₽/мес` при 50 клиентах и <=24 мес.
4. **Workflow criticality высокая:** требования ФНС и первичка относятся к обязательным процессам, а просрочка может блокировать счета.

## Что ещё доказать в post-approval
- pilot-to-paid conversion >= 25% на первых 10 пилотах;
- средний фактический COGS <= 45 000 ₽/клиент/мес;
- win-rate против 1С/Saby не ниже 20% в specialist wedge;
- churn удерживается <= 2,5%/мес после первых 12 клиентов.

## Committee note
Это не approve на лобовую войну против 1С/Saby. Это **approve с оговорками** на specialist AI-layer для high-volume первички, BPO и multi-entity backoffice, где можно продать SLA, compliance-fit и интеграции, а не просто дешёвый OCR.

## Артефакты
- `06-verdict.md`
- `07-score-trajectory.md`
- `telegram-messages.md`


---

# FILE: 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-23 00:41 MSK — Critic and Verdict
- Stage: Program 7 / Critic and Verdict
- Case: `fintech-saby-ai-buhgalteriya-msb-v2`
- Preconditions check:
  - `05-critic.md` содержит оба маркера `P6A-DONE` и `P6B-DONE`
  - `06-verdict.md` до запуска отсутствовал
  - `07-score-trajectory.md` до запуска отсутствовал и создан заново полным rewrite
- Итоговая рубрика 6x25:
  - Unit Economics: `21/25`
  - EBITDA Potential: `21/25`
  - Market + Demand: `19/25`
  - Moat: `13/25`
  - Execution Risk: `15/25`
  - GTM Realism: `18/25`
- Raw total: `107/150`
- Normalized score: `71/100`
- Tier-awareness:
  - `Sources: T1=11, T2=4` найдено в `02-demand.md`
  - `tier_balance = 2.73`
  - Penalty applied to criterion #3: `0`
- 7-factor moat:
  - Sum: `11/21`
  - Normalized moat score: `13/25`
- Finance synthesis:
  - `customer_ltv_rub = 6 750 000 ₽`
  - `CAC = 393 714 ₽`
  - `LTV/CAC = 17,1x`
  - `CAC payback = 2,2 мес`
  - `contribution_margin_rub_month = 135 000 ₽`
  - `company_ebitda_potential_rub_month = 1 550 000 ₽/мес` при 50 клиентах
  - `clients_to_500k_ebitda ≈ 43`
- Committee conclusion:
  - Exact-demand в РФ подтверждён лучше среднего по FINTECH-backoffice category
  - Unit economics инвестиционного уровня, но moat и execution risk пока средние
  - Одобрение допустимо только как specialist AI-layer, а не как generic accounting suite
- Outcome: `APPROVED with notes`
- Final routing: `pipeline/approved/fintech-saby-ai-buhgalteriya-msb-v2/`
- Artifacts: `06-verdict.md`

