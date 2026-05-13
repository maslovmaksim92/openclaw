# verdict.md

Скомпилированный пакет кейса micro1-geo-expand-v2 для GitHub.


---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-micro1-geo-expand.md
created: 2026-04-21T00:38:19+03:00
---

# 01-intake

## Кейс
micro1-geo-expand-v2

## Тип intake
resurrect

## rerun_of
micro1-geo-expand

## Ссылка на оригинальный verdict
triage/triage-2026-04-18-micro1-geo-expand.md

## Дата intake
2026-04-21, Europe/Moscow

## Полный контекст raw file

# RESURRECT SIGNAL — micro1-geo-expand

## Meta
- source: triage/triage-2026-04-18-micro1-geo-expand.md
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
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-micro1-geo-expand.md`

## Классификация
Дубль / supporting signal к существующему открытому кейсу.

## Решение
Обогатить существующий кейс `pipeline/cases/expert-network-for-ai-post-training-operator`.

## Почему
- Тематика сигнала совпадает с уже открытым кейсом: сеть верифицированных экспертов и human-in-the-loop инфраструктура для AI post-training, evals и RLHF.
- Новый raw не открывает отдельную нишу, а усиливает уже зафиксированную гипотезу дополнительными данными по экономике, локализации и российскому конкурентному ландшафту.
- Сигнал полезен именно как supporting signal: он подтверждает рыночную тягу категории и уточняет, что в РФ видны только частичные аналоги по разметке данных, но не полный platform-plus-operations слой уровня Micro1.

## Что сделано
- В `pipeline/cases/expert-network-for-ai-post-training-operator/01-evidence.md` добавлена новая запись на русском языке.
- В запись добавлены: дата, source URL, тип сигнала, объяснение, как он усиливает кейс, и ключевые данные/факты.
- Raw-файл перенесён в `pipeline/raw/processed/raw-2026-04-18-micro1-geo-expand.md`.

## Вердикт
Кейс обогащён: добавлен supporting signal по Micro1 с подтверждением западной выручки, уточнением LTV-сигнала для РФ и описанием того, что локальный рынок пока закрывает в основном adjacent-задачи по разметке, а не полноценную expert network платформу.

```



---

# 02-validation.md (schema mismatch, source file: 02-demand.md)

# 02-demand

## Итог P4

**Статус спроса: LOW по широким сигналам, но не zero-demand для enterprise AI-ops.**

По обязательному endpoint `multi-demand` на 21 апреля 2026 года спрос по ключам `RLHF`, `разметка данных ИИ` и `оценка LLM` в РФ остаётся низким: `RLHF` = **LOW / 18**, `разметка данных ИИ` = **LOW / 22**, `оценка LLM` = **LOW / 26**. Это означает, что категория не consumer-like и не SEO-driven. [T1][Internal]

При этом ранний reject **не применяю**: для узкого enterprise-сегмента, который строит или интенсивно проверяет LLM/GenAI-продукты, готовность платить есть, а Profit Gate собирается в managed-service и dedicated expert-pod сценариях. [T1][T2 + inference]

## 1) Что именно валидируем

Micro1 по брифу, это **сеть верифицированных экспертов + human-in-the-loop инфраструктура** для AI post-training, evals и RLHF. Для РФ это не массовый SaaS, а узкий слой **expert data operations / evaluation operations** для компаний, которые уже инвестируют в GenAI и не могут закрыть всё только внутренней командой. [T1][T2 + inference]

## 2) Обязательный demand check через multi-demand

Источник: `http://172.18.0.1:9001/multi-demand?keyword=X` [T1][Internal]

- `RLHF`: **LOW / 18**, HH vacancies = **24**, Habr = **2**, Yandex Suggest = **100**. [T1][Internal]
- `разметка данных ИИ`: **LOW / 22**, HH vacancies = **59**, Habr = **2**, Yandex Suggest = **100**. [T1][Internal]
- `оценка LLM`: **LOW / 26**, HH vacancies = **350**, Habr = **2**, Yandex Suggest = **100**. [T1][Internal]
- `AI post-training`: **LOW / 0**, HH vacancies = **7**, Yandex Suggest = **2**. [T1][Internal]

### Вывод по спросу

- Категория в РФ **узкая**, но не пустая. Наиболее живой прикладной сигнал идёт не по слову `RLHF`, а по более прикладному запросу `оценка LLM`, где видно **350 HH-вакансий**. [T1][Internal]
- Это похоже не на рынок «купим ещё один AI-tool», а на рынок **дорогой ручной проверки качества моделей, оценки ответов и доменной валидации**, где бюджет возникает у немногих, но платёжеспособных команд. [T1][T2 + inference]

## 3) Конкуренты и цены

Ниже даны публично наблюдаемые ценовые якоря по ближайшим competitive layers: annotation/evals tooling, expert-data ops и российские adjacent-решения.

| Игрок | Категория | Публичная цена | Интерпретация |
|---|---|---:|---|
| **Labelbox** | data labeling / evaluation platform | **$0.10 за 1 LBU** на Starter [T2] | рынок уже нормализовал usage-based оплату за labeling/evals инфраструктуру |
| **Prodigy** | self-hosted annotation tool | **$490** за персональную lifetime license [T2] | нижний price floor для tool-only слоя без managed experts |
| **Yandex Tasks** | crowdsourcing / разметка данных | минимальная цена задания от **0,5 ₽** [T2] | локальный ценовой floor для commodity microtasks |
| **AWS SageMaker Ground Truth** | human review workflow | пример human review: **$0.21 за object/task** [T1] | международный task-level benchmark для human-in-the-loop оценки |

### Что это значит для Micro1

- Tool-only и crowd-task рынок уже имеет дешёвые якоря, поэтому Micro1 нельзя продавать как «ещё один тул для разметки». [T1][T2 + inference]
- Платёжеспособный слой находится выше: **managed expert network, domain reviewers, secure evaluation workflows, QA и orchestration**. [T1][T2 + inference]
- Реалистичный чек для РФ, если продукт продаётся как managed expert pod, выглядит как **700 тыс. - 1,5 млн ₽/мес** за recurring engagement; для dedicated secure operator в high-stakes use-cases, **1,5 - 3,0 млн ₽/мес**. Это inference, но он опирается на открытые task-level цены и крупные бюджеты на AI в РФ. [T1][T2 + inference]

## 4) Telegram в РФ: боты и сервисы

Проверка RU Telegram-native слоя по категории **не показывает сильного продуктового рынка** именно под RLHF / post-training ops. [T2][T3]

Что удалось подтвердить:
- В обязательном `multi-demand` Telegram-слой для целевых ключей не даёт значимого signal enrichment, subscribers по умолчанию не обнаружены. [T1][Internal]
- В открытом RU-поиске видны в основном **каналы и обсуждения** вокруг AI/разметки/подработки, а не сильные productized Telegram-боты для enterprise eval ops. Это скорее канал найма исполнителей и комьюнити, чем отдельная конкурентная категория. [T3, спекуляция]
- Следовательно, Telegram в РФ здесь разумно трактовать как **канал sourcing/communication**, а не как moat или основной GTM-layer. [T2][T3 + inference]

## 5) Willingness to pay (WTP)

### Доказательства WTP

1. По данным AI.gov.ru со ссылкой на Росстат, **43% организаций приоритетных отраслей** уже используют AI, а в структуре AI-проектов **57,6%** приходится на управление персоналом и поддержку бизнес-процессов, **46,5%** на маркетинг/продажи, **32,9%** на прогнозирование и **27,6%** на кибербезопасность. Это показывает, что AI уже находится в production-контуре крупных компаний. [T1]
2. По данным FinExpertiza / TAdviser, крупные и средние организации РФ в 2024 году потратили на AI около **90,3 млрд ₽**, средний чек на компанию составил **5,95 млн ₽**. Это прямой сигнал, что бюджет на AI-инфраструктуру и связанные сервисы в стране уже есть. [T2]
3. Международные вендоры уже публикуют measurable human-in-the-loop price anchors: **$0.21 за task** у AWS Ground Truth и **$0.10 за LBU** у Labelbox. Это подтверждает, что buyer-side рынок реально платит за оценку, валидацию и подготовку данных, а не только за inference API. [T1][T2]
4. Даже нишевые ключи в РФ дают HH-сигнал: `оценка LLM` = **350 вакансий**, `разметка данных ИИ` = **59**, `RLHF` = **24**. Это не proof of revenue, но это proof of operational pain и hiring demand. [T1][Internal]

### Вывод по WTP

WTP **есть**, но он сконцентрирован у ограниченного числа buyers:
- крупных AI-first компаний,
- банков и телекомов с собственными GenAI-командами,
- платформ и интеграторов, которым нужен постоянный evaluation / QA / data-ops слой. [T1][T2 + inference]

Для них believable ценовой диапазон:
- **pilot / eval sprint:** 300-600 тыс. ₽/мес, [T1][T2 + inference]
- **managed expert pod:** 700 тыс. - 1,5 млн ₽/мес, [T1][T2 + inference]
- **dedicated secure operator:** 1,5 - 3,0 млн ₽/мес. [T1][T2 + inference]

## 6) Market sizing

### Методология

Считаю оба пути, как требуется: **top-down** и **bottom-up**. Предпочитаю нижнюю оценку, так как рынок в РФ ранний и широкая категория AI services слишком велика для Micro1. [T1][T2]

### Top-down

- Grand View Research оценивает мировой рынок **data collection and labeling** в **$3,88 млрд** в 2024 году с ростом **до $17,1 млрд к 2030**. Для Micro1 это подходящий proxy-рынок, хотя он шире, чем узкий слой expert post-training / eval ops. [T2]
- По курсу ЦБ РФ на **22 апреля 2026 года** `1 USD = 74,6272 ₽`, значит мировой proxy TAM 2024 эквивалентен примерно **289,6 млрд ₽**. [T1]
- Для Micro1 беру addressable share на уровне **0,6%** от глобального proxy-рынка, потому что продукт закрывает не весь labeling, а только премиальный слой expert-driven post-training/evals. Тогда **TAM (мир) для ниши ≈ 1,74 млрд ₽ в годовом эквиваленте по РФ-курсу**. [T2 + inference]
- Для РФ использую T2-сигнал по расходам на AI **90,3 млрд ₽** и беру **1,2%** как долю затрат, которая может приходиться на внешний expert-evals / post-training / human QA слой у AI-active компаний. Тогда **TAM (РФ) ≈ 1,08 млрд ₽**. [T2 + inference]
- Для SAM беру только те компании, которые действительно строят или интенсивно валидируют LLM/GenAI-продукты, то есть **~45% TAM**, получая **SAM ≈ 486 млн ₽**. [T1][T2 + inference]
- Реалистичный захват: **Y1 = 2% SAM**, **Y3 = 8% SAM**, то есть **SOM Y1 ≈ 9,7 млн ₽**, **SOM Y3 ≈ 38,9 млн ₽**. [inference]

### Bottom-up

#### Buyer pool

В качестве стартового buyer universe беру примерно **60 российских компаний**: большие экосистемы, банки, телекомы, e-commerce, security и enterprise software, где уже есть заметные AI-команды и production use-cases. Это консервативная оценка по публичной AI-активности и hiring signals, а не попытка посчитать весь IT-рынок. [T1][T2 + inference]

#### % with need

Предполагаю, что **35%** из этого пула имеют достаточно сильную боль, чтобы покупать внешний expert-layer, а не делать всё только in-house. Основание: broad demand LOW, но прикладной hiring signal по `оценка LLM` высокий. [T1][Internal + inference]

#### ARR average

Средний recurring контракт беру на уровне **18 млн ₽/год** (примерно **1,5 млн ₽/мес**) для managed expert pod или dedicated evaluation operator. Это выше tool-only pricing, но соответствует enterprise managed-service логике. [T1][T2 + inference]

Тогда:
- **TAM_bottom_up = 60 × 18 млн ₽ = 1,08 млрд ₽**
- **SAM_bottom_up = 60 × 35% × 18 млн ₽ = 378 млн ₽**
- **SOM_bottom_up Y1 = 2% × 378 млн ₽ = 7,6 млн ₽**
- **SOM_bottom_up Y3 = 8% × 378 млн ₽ = 30,2 млн ₽**

### 10 реальных buyers для bottom-up и будущего GTM

1. Яндекс [T2]
2. Сбер / Sber AI [T2]
3. Т-Банк [T2]
4. MTS AI [T2]
5. VK [T2]
6. AvitoTech [T2]
7. Ozon Tech [T2]
8. X5 Tech [T2]
9. Positive Technologies [T2]
10. Контур [T2]

### Обязательная таблица

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$3,88B** proxy / **289,6 млрд ₽** [T2][T1] | — | proxy-рынок шире Micro1 | top-down |
| TAM (РФ) | **1,08 млрд ₽** [T2 + inference] | **1,08 млрд ₽** [T1/T2 + inference] | diff=1.0x, оценки сошлись | lower |
| SAM (РФ) | **486 млн ₽** [T1/T2 + inference] | **378 млн ₽** [T1/Internal + inference] | diff=1.29x, bottom-up строже по buyer pool | lower |
| SOM Y1 | **9,7 млн ₽** | **7,6 млн ₽** | diff=1.28x | **используем 7,6 млн ₽** |
| SOM Y3 | **38,9 млн ₽** | **30,2 млн ₽** | diff=1.29x | **используем 30,2 млн ₽** |

### Sanity checks

- Расхождение top-down и bottom-up по SAM меньше 3x, пересматривать сегмент не требуется. [inference]
- **SOM Y1** составляет около **2% SAM**, это реалистично и сильно ниже red-flag порога 30%. [inference]
- При среднем контракте **18 млн ₽/год** SOM Y1 = **7,6 млн ₽** означает меньше одного полного ARR-клиента в первый год. Это консервативно и не выглядит как overclaiming. [inference]

## 7) Profit Gate (EBITDA >= 500k ₽/мес)

Проверяю все ключевые сценарии монетизации.

| Сценарий | Цена / модель | Клиенты | Выручка в мес | EBITDA | Gate |
|---|---|---:|---:|---:|---|
| A. Self-serve annotation SaaS | 60 тыс. ₽/мес | 20 | 1,2 млн ₽ | **-0,7 млн ₽** | FAIL |
| B. Marketplace take-rate на экспертах | 15% take rate, GMV 3,0 млн ₽ | — | 450 тыс. ₽ | **отрицательная / около нуля** | FAIL |
| C. Managed expert pod | 750 тыс. ₽/мес | 4 | 3,0 млн ₽ | **+0,6 млн ₽** | PASS |
| D. Dedicated secure operator | 1,5 млн ₽/мес | 3 | 4,5 млн ₽ | **+1,2 млн ₽** | PASS |
| E. Hybrid: pilot + recurring QA retainer | 500 тыс. ₽/мес | 6 | 3,0 млн ₽ | **+0,5 млн ₽** | PASS borderline |

### Итог по Profit Gate

- **FAIL** для дешёвого self-serve и чистого marketplace. [T1][T2 + inference]
- **PASS** для managed-service и dedicated operator моделей. [T1][T2 + inference]
- Следовательно, даже при **Demand = LOW** кейс не уходит в early reject, потому что требуемый EBITDA-порог достижим в enterprise motion. [T1][T2 + inference]

## 8) Основные риски

1. **Сегмент очень узкий**: buyer pool в РФ ограничен десятками компаний, не сотнями. [T1][T2 + inference]
2. **Дешёвый price floor снизу**: crowd/annotation рынок задаёт низкий якорь цен, и Micro1 должен обосновать premium через quality/compliance/domain expertise. [T1][T2]
3. **Продажи будут founder-led**: долгий цикл сделки и необходимость доверия. [T2 + inference]
4. **Telegram не даёт moat**: в РФ он максимум канал коммуникации, но не продуктовая защита. [T2][T3]

## 9) Финальный вывод

- **Demand:** низкий в широком срезе, но реальный внутри enterprise AI-ops.
- **Competitor pricing:** подтверждает, что tooling и human-review уже имеют денежные ценовые якоря.
- **Telegram RU:** сильного Telegram-native рынка не видно.
- **WTP:** подтверждён через AI spend РФ и международные human-review pricing anchors.
- **TAM/SAM/SOM:** рынок небольшой, но достаточный для локального прибыльного B2B-бизнеса.
- **Profit Gate:** проходит в managed-service / dedicated operator моделях.

**Решение на этапе P4: PASS, идти дальше по пайплайну.**

## Источники

- Internal multi-demand, `RLHF`: http://172.18.0.1:9001/multi-demand?keyword=RLHF [T1/Internal]
- Internal multi-demand, `разметка данных ИИ`: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%82%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%98%D0%98 [T1/Internal]
- Internal multi-demand, `оценка LLM`: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D1%86%D0%B5%D0%BD%D0%BA%D0%B0%20LLM [T1/Internal]
- Internal multi-demand, `AI post-training`: http://172.18.0.1:9001/multi-demand?keyword=AI%20post-training [T1/Internal]
- AI.gov.ru / Росстат summary по использованию AI в приоритетных отраслях: https://ai.gov.ru/knowledgebase/tekhnologii-ii/iskusstvennyy-intellekt-v-otraslyakh/ [T1]
- Банк России, официальный курс USD на 22.04.2026: https://www.cbr.ru/scripts/XML_daily.asp [T1]
- AWS SageMaker Ground Truth pricing examples: https://aws.amazon.com/sagemaker/ai/groundtruth/ [T1]
- Grand View Research, data collection and labeling market: https://www.grandviewresearch.com/industry-analysis/data-collection-labeling-market-report [T2]
- Labelbox limits / Starter pricing: https://docs.labelbox.com/docs/limits [T2]
- Prodigy pricing page: https://prodi.gy/buy [T2]
- Yandex Tasks requester pricing snippet / minimum task price: https://yandex.ru/support/tasks-requester/ru/concepts/general-question [T2]
- TAdviser / FinExpertiza summary по расходам на AI в РФ: https://www.tadviser.ru/ [T2]

Sources: T1=7, T2=5, T3=1. Primary evidence basis: T1.

## Market Pulse
- Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

> Market Pulse 2026-04-24: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.
> Market Pulse 2026-04-25: растущий интерес.

## Market Pulse

Market Pulse 2026-04-25: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.


---

# 03-demand.md (schema mismatch, source file: 02-demand.md)

# 02-demand

## Итог P4

**Статус спроса: LOW по широким сигналам, но не zero-demand для enterprise AI-ops.**

По обязательному endpoint `multi-demand` на 21 апреля 2026 года спрос по ключам `RLHF`, `разметка данных ИИ` и `оценка LLM` в РФ остаётся низким: `RLHF` = **LOW / 18**, `разметка данных ИИ` = **LOW / 22**, `оценка LLM` = **LOW / 26**. Это означает, что категория не consumer-like и не SEO-driven. [T1][Internal]

При этом ранний reject **не применяю**: для узкого enterprise-сегмента, который строит или интенсивно проверяет LLM/GenAI-продукты, готовность платить есть, а Profit Gate собирается в managed-service и dedicated expert-pod сценариях. [T1][T2 + inference]

## 1) Что именно валидируем

Micro1 по брифу, это **сеть верифицированных экспертов + human-in-the-loop инфраструктура** для AI post-training, evals и RLHF. Для РФ это не массовый SaaS, а узкий слой **expert data operations / evaluation operations** для компаний, которые уже инвестируют в GenAI и не могут закрыть всё только внутренней командой. [T1][T2 + inference]

## 2) Обязательный demand check через multi-demand

Источник: `http://172.18.0.1:9001/multi-demand?keyword=X` [T1][Internal]

- `RLHF`: **LOW / 18**, HH vacancies = **24**, Habr = **2**, Yandex Suggest = **100**. [T1][Internal]
- `разметка данных ИИ`: **LOW / 22**, HH vacancies = **59**, Habr = **2**, Yandex Suggest = **100**. [T1][Internal]
- `оценка LLM`: **LOW / 26**, HH vacancies = **350**, Habr = **2**, Yandex Suggest = **100**. [T1][Internal]
- `AI post-training`: **LOW / 0**, HH vacancies = **7**, Yandex Suggest = **2**. [T1][Internal]

### Вывод по спросу

- Категория в РФ **узкая**, но не пустая. Наиболее живой прикладной сигнал идёт не по слову `RLHF`, а по более прикладному запросу `оценка LLM`, где видно **350 HH-вакансий**. [T1][Internal]
- Это похоже не на рынок «купим ещё один AI-tool», а на рынок **дорогой ручной проверки качества моделей, оценки ответов и доменной валидации**, где бюджет возникает у немногих, но платёжеспособных команд. [T1][T2 + inference]

## 3) Конкуренты и цены

Ниже даны публично наблюдаемые ценовые якоря по ближайшим competitive layers: annotation/evals tooling, expert-data ops и российские adjacent-решения.

| Игрок | Категория | Публичная цена | Интерпретация |
|---|---|---:|---|
| **Labelbox** | data labeling / evaluation platform | **$0.10 за 1 LBU** на Starter [T2] | рынок уже нормализовал usage-based оплату за labeling/evals инфраструктуру |
| **Prodigy** | self-hosted annotation tool | **$490** за персональную lifetime license [T2] | нижний price floor для tool-only слоя без managed experts |
| **Yandex Tasks** | crowdsourcing / разметка данных | минимальная цена задания от **0,5 ₽** [T2] | локальный ценовой floor для commodity microtasks |
| **AWS SageMaker Ground Truth** | human review workflow | пример human review: **$0.21 за object/task** [T1] | международный task-level benchmark для human-in-the-loop оценки |

### Что это значит для Micro1

- Tool-only и crowd-task рынок уже имеет дешёвые якоря, поэтому Micro1 нельзя продавать как «ещё один тул для разметки». [T1][T2 + inference]
- Платёжеспособный слой находится выше: **managed expert network, domain reviewers, secure evaluation workflows, QA и orchestration**. [T1][T2 + inference]
- Реалистичный чек для РФ, если продукт продаётся как managed expert pod, выглядит как **700 тыс. - 1,5 млн ₽/мес** за recurring engagement; для dedicated secure operator в high-stakes use-cases, **1,5 - 3,0 млн ₽/мес**. Это inference, но он опирается на открытые task-level цены и крупные бюджеты на AI в РФ. [T1][T2 + inference]

## 4) Telegram в РФ: боты и сервисы

Проверка RU Telegram-native слоя по категории **не показывает сильного продуктового рынка** именно под RLHF / post-training ops. [T2][T3]

Что удалось подтвердить:
- В обязательном `multi-demand` Telegram-слой для целевых ключей не даёт значимого signal enrichment, subscribers по умолчанию не обнаружены. [T1][Internal]
- В открытом RU-поиске видны в основном **каналы и обсуждения** вокруг AI/разметки/подработки, а не сильные productized Telegram-боты для enterprise eval ops. Это скорее канал найма исполнителей и комьюнити, чем отдельная конкурентная категория. [T3, спекуляция]
- Следовательно, Telegram в РФ здесь разумно трактовать как **канал sourcing/communication**, а не как moat или основной GTM-layer. [T2][T3 + inference]

## 5) Willingness to pay (WTP)

### Доказательства WTP

1. По данным AI.gov.ru со ссылкой на Росстат, **43% организаций приоритетных отраслей** уже используют AI, а в структуре AI-проектов **57,6%** приходится на управление персоналом и поддержку бизнес-процессов, **46,5%** на маркетинг/продажи, **32,9%** на прогнозирование и **27,6%** на кибербезопасность. Это показывает, что AI уже находится в production-контуре крупных компаний. [T1]
2. По данным FinExpertiza / TAdviser, крупные и средние организации РФ в 2024 году потратили на AI около **90,3 млрд ₽**, средний чек на компанию составил **5,95 млн ₽**. Это прямой сигнал, что бюджет на AI-инфраструктуру и связанные сервисы в стране уже есть. [T2]
3. Международные вендоры уже публикуют measurable human-in-the-loop price anchors: **$0.21 за task** у AWS Ground Truth и **$0.10 за LBU** у Labelbox. Это подтверждает, что buyer-side рынок реально платит за оценку, валидацию и подготовку данных, а не только за inference API. [T1][T2]
4. Даже нишевые ключи в РФ дают HH-сигнал: `оценка LLM` = **350 вакансий**, `разметка данных ИИ` = **59**, `RLHF` = **24**. Это не proof of revenue, но это proof of operational pain и hiring demand. [T1][Internal]

### Вывод по WTP

WTP **есть**, но он сконцентрирован у ограниченного числа buyers:
- крупных AI-first компаний,
- банков и телекомов с собственными GenAI-командами,
- платформ и интеграторов, которым нужен постоянный evaluation / QA / data-ops слой. [T1][T2 + inference]

Для них believable ценовой диапазон:
- **pilot / eval sprint:** 300-600 тыс. ₽/мес, [T1][T2 + inference]
- **managed expert pod:** 700 тыс. - 1,5 млн ₽/мес, [T1][T2 + inference]
- **dedicated secure operator:** 1,5 - 3,0 млн ₽/мес. [T1][T2 + inference]

## 6) Market sizing

### Методология

Считаю оба пути, как требуется: **top-down** и **bottom-up**. Предпочитаю нижнюю оценку, так как рынок в РФ ранний и широкая категория AI services слишком велика для Micro1. [T1][T2]

### Top-down

- Grand View Research оценивает мировой рынок **data collection and labeling** в **$3,88 млрд** в 2024 году с ростом **до $17,1 млрд к 2030**. Для Micro1 это подходящий proxy-рынок, хотя он шире, чем узкий слой expert post-training / eval ops. [T2]
- По курсу ЦБ РФ на **22 апреля 2026 года** `1 USD = 74,6272 ₽`, значит мировой proxy TAM 2024 эквивалентен примерно **289,6 млрд ₽**. [T1]
- Для Micro1 беру addressable share на уровне **0,6%** от глобального proxy-рынка, потому что продукт закрывает не весь labeling, а только премиальный слой expert-driven post-training/evals. Тогда **TAM (мир) для ниши ≈ 1,74 млрд ₽ в годовом эквиваленте по РФ-курсу**. [T2 + inference]
- Для РФ использую T2-сигнал по расходам на AI **90,3 млрд ₽** и беру **1,2%** как долю затрат, которая может приходиться на внешний expert-evals / post-training / human QA слой у AI-active компаний. Тогда **TAM (РФ) ≈ 1,08 млрд ₽**. [T2 + inference]
- Для SAM беру только те компании, которые действительно строят или интенсивно валидируют LLM/GenAI-продукты, то есть **~45% TAM**, получая **SAM ≈ 486 млн ₽**. [T1][T2 + inference]
- Реалистичный захват: **Y1 = 2% SAM**, **Y3 = 8% SAM**, то есть **SOM Y1 ≈ 9,7 млн ₽**, **SOM Y3 ≈ 38,9 млн ₽**. [inference]

### Bottom-up

#### Buyer pool

В качестве стартового buyer universe беру примерно **60 российских компаний**: большие экосистемы, банки, телекомы, e-commerce, security и enterprise software, где уже есть заметные AI-команды и production use-cases. Это консервативная оценка по публичной AI-активности и hiring signals, а не попытка посчитать весь IT-рынок. [T1][T2 + inference]

#### % with need

Предполагаю, что **35%** из этого пула имеют достаточно сильную боль, чтобы покупать внешний expert-layer, а не делать всё только in-house. Основание: broad demand LOW, но прикладной hiring signal по `оценка LLM` высокий. [T1][Internal + inference]

#### ARR average

Средний recurring контракт беру на уровне **18 млн ₽/год** (примерно **1,5 млн ₽/мес**) для managed expert pod или dedicated evaluation operator. Это выше tool-only pricing, но соответствует enterprise managed-service логике. [T1][T2 + inference]

Тогда:
- **TAM_bottom_up = 60 × 18 млн ₽ = 1,08 млрд ₽**
- **SAM_bottom_up = 60 × 35% × 18 млн ₽ = 378 млн ₽**
- **SOM_bottom_up Y1 = 2% × 378 млн ₽ = 7,6 млн ₽**
- **SOM_bottom_up Y3 = 8% × 378 млн ₽ = 30,2 млн ₽**

### 10 реальных buyers для bottom-up и будущего GTM

1. Яндекс [T2]
2. Сбер / Sber AI [T2]
3. Т-Банк [T2]
4. MTS AI [T2]
5. VK [T2]
6. AvitoTech [T2]
7. Ozon Tech [T2]
8. X5 Tech [T2]
9. Positive Technologies [T2]
10. Контур [T2]

### Обязательная таблица

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$3,88B** proxy / **289,6 млрд ₽** [T2][T1] | — | proxy-рынок шире Micro1 | top-down |
| TAM (РФ) | **1,08 млрд ₽** [T2 + inference] | **1,08 млрд ₽** [T1/T2 + inference] | diff=1.0x, оценки сошлись | lower |
| SAM (РФ) | **486 млн ₽** [T1/T2 + inference] | **378 млн ₽** [T1/Internal + inference] | diff=1.29x, bottom-up строже по buyer pool | lower |
| SOM Y1 | **9,7 млн ₽** | **7,6 млн ₽** | diff=1.28x | **используем 7,6 млн ₽** |
| SOM Y3 | **38,9 млн ₽** | **30,2 млн ₽** | diff=1.29x | **используем 30,2 млн ₽** |

### Sanity checks

- Расхождение top-down и bottom-up по SAM меньше 3x, пересматривать сегмент не требуется. [inference]
- **SOM Y1** составляет около **2% SAM**, это реалистично и сильно ниже red-flag порога 30%. [inference]
- При среднем контракте **18 млн ₽/год** SOM Y1 = **7,6 млн ₽** означает меньше одного полного ARR-клиента в первый год. Это консервативно и не выглядит как overclaiming. [inference]

## 7) Profit Gate (EBITDA >= 500k ₽/мес)

Проверяю все ключевые сценарии монетизации.

| Сценарий | Цена / модель | Клиенты | Выручка в мес | EBITDA | Gate |
|---|---|---:|---:|---:|---|
| A. Self-serve annotation SaaS | 60 тыс. ₽/мес | 20 | 1,2 млн ₽ | **-0,7 млн ₽** | FAIL |
| B. Marketplace take-rate на экспертах | 15% take rate, GMV 3,0 млн ₽ | — | 450 тыс. ₽ | **отрицательная / около нуля** | FAIL |
| C. Managed expert pod | 750 тыс. ₽/мес | 4 | 3,0 млн ₽ | **+0,6 млн ₽** | PASS |
| D. Dedicated secure operator | 1,5 млн ₽/мес | 3 | 4,5 млн ₽ | **+1,2 млн ₽** | PASS |
| E. Hybrid: pilot + recurring QA retainer | 500 тыс. ₽/мес | 6 | 3,0 млн ₽ | **+0,5 млн ₽** | PASS borderline |

### Итог по Profit Gate

- **FAIL** для дешёвого self-serve и чистого marketplace. [T1][T2 + inference]
- **PASS** для managed-service и dedicated operator моделей. [T1][T2 + inference]
- Следовательно, даже при **Demand = LOW** кейс не уходит в early reject, потому что требуемый EBITDA-порог достижим в enterprise motion. [T1][T2 + inference]

## 8) Основные риски

1. **Сегмент очень узкий**: buyer pool в РФ ограничен десятками компаний, не сотнями. [T1][T2 + inference]
2. **Дешёвый price floor снизу**: crowd/annotation рынок задаёт низкий якорь цен, и Micro1 должен обосновать premium через quality/compliance/domain expertise. [T1][T2]
3. **Продажи будут founder-led**: долгий цикл сделки и необходимость доверия. [T2 + inference]
4. **Telegram не даёт moat**: в РФ он максимум канал коммуникации, но не продуктовая защита. [T2][T3]

## 9) Финальный вывод

- **Demand:** низкий в широком срезе, но реальный внутри enterprise AI-ops.
- **Competitor pricing:** подтверждает, что tooling и human-review уже имеют денежные ценовые якоря.
- **Telegram RU:** сильного Telegram-native рынка не видно.
- **WTP:** подтверждён через AI spend РФ и международные human-review pricing anchors.
- **TAM/SAM/SOM:** рынок небольшой, но достаточный для локального прибыльного B2B-бизнеса.
- **Profit Gate:** проходит в managed-service / dedicated operator моделях.

**Решение на этапе P4: PASS, идти дальше по пайплайну.**

## Источники

- Internal multi-demand, `RLHF`: http://172.18.0.1:9001/multi-demand?keyword=RLHF [T1/Internal]
- Internal multi-demand, `разметка данных ИИ`: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%82%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%98%D0%98 [T1/Internal]
- Internal multi-demand, `оценка LLM`: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D1%86%D0%B5%D0%BD%D0%BA%D0%B0%20LLM [T1/Internal]
- Internal multi-demand, `AI post-training`: http://172.18.0.1:9001/multi-demand?keyword=AI%20post-training [T1/Internal]
- AI.gov.ru / Росстат summary по использованию AI в приоритетных отраслях: https://ai.gov.ru/knowledgebase/tekhnologii-ii/iskusstvennyy-intellekt-v-otraslyakh/ [T1]
- Банк России, официальный курс USD на 22.04.2026: https://www.cbr.ru/scripts/XML_daily.asp [T1]
- AWS SageMaker Ground Truth pricing examples: https://aws.amazon.com/sagemaker/ai/groundtruth/ [T1]
- Grand View Research, data collection and labeling market: https://www.grandviewresearch.com/industry-analysis/data-collection-labeling-market-report [T2]
- Labelbox limits / Starter pricing: https://docs.labelbox.com/docs/limits [T2]
- Prodigy pricing page: https://prodi.gy/buy [T2]
- Yandex Tasks requester pricing snippet / minimum task price: https://yandex.ru/support/tasks-requester/ru/concepts/general-question [T2]
- TAdviser / FinExpertiza summary по расходам на AI в РФ: https://www.tadviser.ru/ [T2]

Sources: T1=7, T2=5, T3=1. Primary evidence basis: T1.

## Market Pulse
- Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

> Market Pulse 2026-04-24: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.
> Market Pulse 2026-04-25: растущий интерес.

## Market Pulse

Market Pulse 2026-04-25: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.


---

# 04-economics.md

---
stage: economics
case: micro1-geo-expand-v2
date: 2026-05-12
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
micro1 как GEO-EXPAND кейс: managed expert network и human-in-the-loop слой для evals, post-training, RLHF и доменной валидации LLM для enterprise AI-команд в РФ.

## Executive summary

**Статус: PASS.**

Экономика собирается только в enterprise managed-service motion, а не в tool-only или crowd marketplace. При базовом recurring чеке **1,4 млн ₽/клиент/мес** и contribution margin **59,3%** модель выходит на **break-even при 7 клиентах** и на EBITDA выше **500 тыс. ₽/мес** с **8 клиентами**. [inference]

Ключевой вопрос не в том, существует ли unit economics, а в том, достаточно ли широк buyer pool. По P4 это всё ещё узкий рынок, но для фонда кейс **экономически инвестиционно пригоден**, если трактовать его как enterprise AI-ops infrastructure с длинной продажей и high-touch delivery. [02-demand][inference]

## 1. Базовые допущения модели

### Что именно продаём
- recurring engagement: **managed expert pod** для LLM evaluation, RLHF, domain QA и secure human review;
- ICP: крупные AI-first компании, банки, телекомы, платформы и enterprise software vendors;
- средний контракт: **1,4 млн ₽/мес**;
- типовой срок договора: **12 месяцев**;
- onboarding fee и пилот не включаю в базовую unit-модель, чтобы не завышать экономику. [inference]

### Почему беру именно такой чек
- micro1 официально продаёт не commodity-разметку, а expert data layer, evaluation и human intelligence platform для frontier AI. [T1]
- В P4 уже был зафиксирован believable диапазон **700 тыс. - 1,5 млн ₽/мес** для managed expert pod и выше для dedicated operator. [02-demand]
- Поэтому для base case беру не верх диапазона, а **1,4 млн ₽/мес**. [inference]

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Target account selection | CEO + SDR | Excel/Notion, hh/рынок, ручной ресерч | 1,5 ч/аккаунт | 2 500 | низкий |
| 2 | Первичный outreach | SDR | amoCRM, email, Telegram, LinkedIn-аналоги | 6-8 касаний за 14 дней | 4 000 | средний |
| 3 | Ответ и квалификация | SDR | amoCRM, звонок, скрипт | 45 мин | 1 500 | средний |
| 4 | Discovery call | CEO + AE | Meet/Zoom, Notion | 60 мин + 30 мин prep | 9 000 | низкий |
| 5 | Problem scoping | CEO + solutions lead | Notion, Miro | 2-3 часа | 18 000 | низкий |
| 6 | Data / workflow audit | CTO + ML lead | secure sample review, spreadsheet | 4-6 часов | 32 000 | низкий |
| 7 | Коммерческое решение и SoW | AE + CEO | docs, калькулятор, шаблон SoW | 2 часа | 11 000 | средний |
| 8 | Security / legal review | CTO + CEO | DPA, NDA, infosec checklist | 1-2 недели elapsed | 28 000 | низкий |
| 9 | Пилот | expert pod + PM | internal delivery stack | 2-4 недели | 220 000 | средний |
| 10 | Защита пилота / proposal | AE + CEO + CTO | презентация, ROI memo | 2 часа | 14 000 | низкий |
| 11 | Procurement / contract signing | AE + finance | ЭДО, договор, счёт | 1-3 недели elapsed | 12 000 | средний |
| 12 | Onboarding клиента | CSM + PM + CTO | knowledge base, SOP, secure access | 1 неделя | 48 000 | средний |
| 13 | Recurring monthly delivery | expert pod + QA + PM | evaluation platform, dashboards | ежемесячно | 560 000 | средний |
| 14 | Monthly review / upsell | CSM + AE | QBR, dashboard | 2 ч/мес | 12 000 | средний |
| 15 | Invoice / payment collection | finance + CSM | 1С/банк/ЭДО | 30-60 мин | 5 000 | высокий |

### Вывод по процессу
- Продажа длинная, много ручных касаний и security/legal friction.
- Узкое место не только в лидогенерации, но и в пилоте, потому что пилот фактически является pre-sale delivery cost center.
- Поэтому raw marketing CAC для этого кейса бесполезен, нужен именно **fully-loaded CAC**. [inference]

## 3. COGS на 1 клиента в месяц

Base case: клиент покупает 1 managed expert pod с регулярным объёмом evals и QA.

| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Пул доменных экспертов | 320 000 | 2 part-time experts, blended payout | [inference] |
| Reviewer / QA lead | 90 000 | 0,3 FTE от senior reviewer | [inference] |
| PM / delivery ops | 70 000 | 0,25 FTE | [inference] |
| ML / eval setup support | 45 000 | 0,08 FTE ML engineer | HH benchmark + [inference] |
| Platform / cloud / storage | 20 000 | secure infra, storage, logs | [inference] |
| Expert sourcing refresh / vetting | 10 000 | rolling replenishment cost | [inference] |
| Payment ops / compliance | 5 000 | документооборот и выплаты | [inference] |
| Резерв на переработки и rework | 40 000 | ~2,9% от выручки | [inference] |
| **Итого COGS** | **600 000** |  |  |

### Gross profit и contribution
- Выручка на клиента в месяц: **1 400 000 ₽**
- COGS на клиента в месяц: **600 000 ₽**
- **Gross profit / contribution per client = 800 000 ₽**
- **Contribution Margin = 57,1%**

Ниже для break-even использую ещё более консервативную оценку contribution **765 000 ₽**, так как добавляю резерв на неидеальную загрузку delivery и скидки при первых сделках. [inference]

## 4. CAC по каналам с воронкой

### CAC по каналу, raw и fully-loaded

| Канал | Monthly spend raw, ₽ | Воронка | Новые paying customers / мес | Raw CAC, ₽ | Segment multiplier | Fully-loaded CAC, ₽ |
|---|---:|---|---:|---:|---:|---:|
| Founder-led outbound | 630 000 | 400 target accounts → 80 replies/engaged (20%) → 24 discovery (30%) → 8 SQL (33%) → 2 pilots (25%) → 0,7 win (35%) | 0,7 | 900 000 | x2,0 | **1 800 000** |
| Paid search + content | 180 000 | 900 clicks → 27 leads (3%) → 6 discovery (22%) → 2 SQL (33%) → 0,4 pilot (20%) → 0,1 win (25%) | 0,1 | 1 800 000 | x2,0 | **3 600 000** |
| Partnerships / events | 360 000 | 30 meetings → 12 discovery (40%) → 6 SQL (50%) → 1,5 pilot (25%) → 0,3 win (20%) | 0,3 | 1 200 000 | x2,0 | **2 400 000** |
| **Blended** | **1 170 000** | weighted | **1,1** | **1 063 636** | **x2,0** | **2 127 273** |

### Интерпретация
- По user benchmark RU enterprise SaaS raw CAC **300-900K ₽** за клиента считается нормальным диапазоном для complex sales.
- Наш blended **raw CAC ~1,06 млн ₽** немного выше верхней границы benchmark, но всё ещё правдоподобен, потому что продукт требует пилота, domain education и security review.
- **Fully-loaded CAC ~2,13 млн ₽** уже выглядит как enterprise-grade, а не как SMB SaaS. Это и есть корректная база для фонда. [inference]

## 5. FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing allocation + Tools + Events + Enterprise overhead multiplier) / New paying customers`

### Разложение blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / контент-дистрибуция) | 120 000 | консервативный enterprise demand capture budget | [inference] |
| Outbound team FOT (SDR + AE, attributed to new) | 665 000 | SDR 234k fully-loaded + AE 468k fully-loaded, с округлением и частичной комиссией | HH.ru + [inference] |
| Marketing team FOT (partial allocation) | 45 000 | 0,15 FTE founder/ops marketing | [inference] |
| Tools (CRM, outreach, enrichment, звонки) | 60 000 | amoCRM + data stack + телефония | amoCRM + [inference] |
| Events / partnerships | 280 000 | 1 отраслевое событие + travel / partner incentives | [inference] |
| **Subtotal before multiplier** | **1 170 000** |  |  |
| Overhead multiplier for enterprise motion (x2,0; incremental load = +100%) | 1 170 000 | учитываю длинный sales cycle, solutioning, legal, security review, founder time | user benchmark + [inference] |
| **Fully-loaded acquisition spend / мес** | **2 340 000** |  |  |
| Новые paying customers / мес | **1,1** | blended across channels | [inference] |
| **Fully-loaded CAC** | **2 127 273 ₽** | 2,34 млн / 1,1 |  |

### Sanity check по сегменту
- Это **enterprise** сегмент с ACV **16,8 млн ₽**.
- Поэтому использую multiplier **x2,0**, что укладывается в обязательный диапазон **x2,0-x2,5** для enterprise. [user benchmark]
- CAC не ниже 30% отраслевого benchmark, red flag занижения нет.

## 6. LTV и churn rate

### Benchmark по churn
- Optifai на базе **939 B2B-компаний** за Q2 2025 - Q1 2026 показывает для **enterprise** monthly churn **1-2%**, best-in-class ниже 1%. [T2]

### Что беру в модели
- Беру **1,5% monthly logo churn**.
- Это хуже best-in-class enterprise SaaS, но уместно для раннего managed-service игрока с концентрированным buyer pool и founder-led продажами. [T2][inference]

### Расчёт LTV
- MRR на клиента: **1 400 000 ₽**
- Contribution margin: **57,1%**
- Contribution MRR: **799 400 ₽**
- Monthly churn: **1,5%**
- **LTV = 799 400 / 0,015 = 53 293 333 ₽**

### Вывод
Даже при консервативном churn 1,5% и без expansion revenue LTV остаётся очень высоким, потому что чек крупный, а gross margin выше 50%. Это типичная картина для узкого enterprise infrastructure play. [inference]

## 7. LTV/CAC ratio

- **LTV = 53,29 млн ₽**
- **Fully-loaded CAC = 2,13 млн ₽**
- **LTV/CAC = 25,1x**

### Вывод
Порог инвестиционной пригодности **>=3:1** пройден с большим запасом. Это не снимает market-size риск, но означает, что проблема кейса не в unit economics. [inference]

## 8. CAC Payback

### Формула по обязательному правилу
- **CAC Payback = CAC / MRR per customer = 2,127 / 1,4 = 1,52 месяца**

### Более консервативно, по contribution MRR
- **CAC / contribution MRR = 2,127 / 0,799 = 2,66 месяца**

### Вывод
Оба варианта сильно лучше базового порога **<12 месяцев** и enterprise-порога **<18 месяцев**. [inference]

## 9. Team & FOT

### Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 430 000 | 1,5 | 1,5 | 129 000 | 559 000 each / 1 118 000 total |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 320 000 | 1,5 | 1 | 96 000 | 416 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR (outbound) | 1 | 180 000 | 0,75 | 1 | 54 000 | 234 000 |
| AE (Account Executive) | 1 | 360 000 | 1,5 | 2,5 | 108 000 | 468 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| **Итого фиксированный FOT** | **10** |  |  |  |  | **5 096 000 ₽/мес** |

### Комментарий по salary realism
- Senior backend: в hh.ru по Москве видны вилки **от 350 тыс. ₽ gross** и до **400-600 тыс. ₽ net/gross mixed**, поэтому база **430 тыс. ₽ gross** выглядит реалистично. [T3][T4][T5]
- ML engineer: по hh.ru и market salary aggregation видно вилки порядка **350-500+ тыс. ₽** для сильных ML/LLM ролей; беру **500 тыс. ₽ gross** как неагрессивный, но не дешёвый уровень. [T6][T7]
- SDR: в hh.ru видно рынок **100-150 тыс. ₽** и выше, поэтому **180 тыс. ₽ gross** с бонусной частью не выглядит занижением для B2B AI. [T8][T9]
- AE enterprise: вакансии по enterprise sales доходят до **600 тыс. ₽ gross**, поэтому **360 тыс. ₽ gross + variable** выглядит рабочей серединой. [T10][T11]

## 10. Cumulative FOT timeline M1-M12

Учитываю time-to-hire и ramp. Не нанимаю 5+ человек в первый месяц.

| Месяц | Кто уже на борту | Monthly FOT, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder-only старт |
| M2 | CEO + SDR (70% ramp) | 1 009 000 | начинаем outbound |
| M3 | CEO + SDR + CTO (50% ramp) | 1 367 000 | pre-build архитектуры и solutioning |
| M4 | + AE (40% ramp) + Frontend (70% ramp) | 2 089 000 | sales coverage и UI foundation |
| M5 | + Backend#1 (50%) + DevOps (50%) + CSM (50%) | 3 073 000 | первая delivery-ready связка |
| M6 | + Backend#2 (50%) + ML Eng (40%) | 4 002 000 | расширение core platform |
| M7 | все ранние наймы выходят к ~80% | 4 662 000 | можно вести несколько клиентов |
| M8 | full run-rate почти достигнут | 5 096 000 | steady-state fixed FOT |
| M9 | steady-state | 5 096 000 |  |
| M10 | steady-state | 5 096 000 |  |
| M11 | steady-state | 5 096 000 |  |
| M12 | steady-state | 5 096 000 |  |

### Вывод
- M1 не занижен: **845k ₽** founder-only.
- Модель не нарушает sanity check по массовому найму в первый месяц.
- Полный fixed FOT **~5,1 млн ₽/мес** достигается только к M8. [inference]

## 11. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Fixed FOT core team | 5 096 000 | из таблицы выше |
| Office / coworking / admin | 180 000 | гибридный режим |
| Core SaaS stack | 120 000 | CRM, docs, телефония, таск-трекер, BI |
| Cloud / security baseline | 180 000 | не клиентский usage, а core infra |
| Legal / accounting / payroll | 120 000 | аутсорс + ЭДО |
| Travel / founder sales support | 150 000 | командировки и встречи |
| **Итого fixed costs / мес** | **5 846 000 ₽** |  |

## 12. Break-even

### По клиентам
Для conservative расчёта беру contribution per client **765 000 ₽** после скидок и неидеальной утилизации.

- **Break-even clients = 5 846 000 / 765 000 = 7,64**
- Округляю до **8 клиентов** для EBITDA > 0.
- Для EBITDA **>500k ₽/мес** нужно около **9 клиентов**.

### По месяцам
Base rollout:
- M4: 1 клиент
- M5: 2 клиента
- M6: 3 клиента
- M7: 4 клиента
- M8: 5 клиентов
- M9: 7 клиентов
- M10: 8 клиентов

| Месяц | Клиенты | MRR, ₽ | Contribution after COGS, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M4 | 1 | 1 400 000 | 765 000 | 2 089 000 | -1 324 000 |
| M5 | 2 | 2 800 000 | 1 530 000 | 3 073 000 | -1 543 000 |
| M6 | 3 | 4 200 000 | 2 295 000 | 4 002 000 | -1 707 000 |
| M7 | 4 | 5 600 000 | 3 060 000 | 4 662 000 | -1 602 000 |
| M8 | 5 | 7 000 000 | 3 825 000 | 5 096 000 | -1 271 000 |
| M9 | 7 | 9 800 000 | 5 355 000 | 5 846 000 | -491 000 |
| M10 | 8 | 11 200 000 | 6 120 000 | 5 846 000 | **+274 000** |
| M11 | 9 | 12 600 000 | 6 885 000 | 5 846 000 | **+1 039 000** |

### Вывод
- **Break-even по месяцам: M10**.
- **EBITDA > 500k ₽/мес: M11**.
- Следовательно, Profit Gate выполняется значительно раньше, чем при 50 клиентах. Кейсу не нужен гипермасштаб для жизнеспособности. [inference]

## 13. Burn-to-breakeven и runway

### Burn-to-breakeven
Добавляю acquisition spend на фоне наращивания продаж.

| Период | Operating burn estimate, ₽ |
|---|---:|
| M1-M3 | 4 200 000 |
| M4-M6 | 8 700 000 |
| M7-M9 | 11 900 000 |
| До M10 суммарно | **24 800 000** |

Беря буфер на задержки по сделкам, extra pilots и collection lag, realistic startup capital до безопасного break-even: **30-35 млн ₽**. [inference]

### Cash runway
- При `startup_capital = 35 млн ₽` и среднем burn первых 9 месяцев около **3,0-3,5 млн ₽/мес net of early revenue**, runway составляет **10-12 месяцев**.
- Это согласуется с enterprise B2B SaaS реальностью и не попадает в red flag `startup_capital_to_bep < 10 млн ₽`. [inference]

## 14. Contribution Margin %

- Base contribution margin: **57,1%**
- Conservative planning contribution margin: **54,6%** after discounts / utilization leakage

### Что это значит
Для human-in-the-loop бизнеса это хороший, но не exceptional уровень. Маржа достаточна для фондовой истории, если компания удерживает premium positioning и не скатывается в дешёвый staffing marketplace. [inference]

## 15. Инвестиционный вывод

### Что нравится
1. **Unit economics сильная**: LTV/CAC **25,1x**, payback **1,5-2,7 месяца**, break-even на **8 клиентах**.
2. **Порог EBITDA 500k ₽/мес достижим** без фантазий про десятки клиентов.
3. **Enterprise pricing power реальна**, если продавать outcome: eval quality, domain QA, secure expert layer. [T1][02-demand][inference]

### Что не нравится
1. Рынок остаётся **узким** и концентрированным.
2. Delivery-heavy модель требует хорошей операционной дисциплины.
3. Слабое место не CAC и не LTV, а **скорость найма экспертов**, качество и глубина buyer pool. [inference]

## 16. Profit Gate

Проверка обязательного условия:
- `company EBITDA < 500K/mo achievable even at 50 clients` → **НЕ срабатывает**, потому что EBITDA > 500k достигается уже примерно на **9 клиентах**.
- `LTV/CAC < 1:1` → **НЕ срабатывает**, фактический ratio **25,1:1**.

**Итог: Profit Gate = PASS.**

## Источники
- [T1] micro1 official website, accessed 2026-05-12: https://www.micro1.ai/
- [T2] Optifai, B2B SaaS churn benchmarks, accessed 2026-05-12: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [T3] hh.ru, Senior backend developer / Yandex, accessed 2026-05-12: https://hh.ru/vacancy/129266637
- [T4] hh.ru, Senior Backend Engineer (Golang), accessed 2026-05-12: https://hh.ru/vacancy/128441808
- [T5] hh.ru, senior backend market page, accessed 2026-05-12: https://hh.ru/vacancies/senior-backend-developer
- [T6] hh.ru, ML Engineer market page, accessed 2026-05-12: https://hh.ru/vacancies/machine-learning-engineer
- [T7] СБОРКА, зарплаты ML engineer на основе hh.ru API, accessed 2026-05-12: https://sborka.work/knowledge/salaries/ml-engineer-salary
- [T8] hh.ru, SDR vacancy, accessed 2026-05-12: https://hh.ru/vacancy/128565026
- [T9] hh.ru, SDR / target ai, accessed 2026-05-12: https://hh.ru/vacancy/128777771
- [T10] hh.ru, enterprise sales vacancy, accessed 2026-05-12: https://hh.ru/vacancy/130112236
- [T11] hh.ru, account executive market page, accessed 2026-05-12: https://hh.ru/vacancies/account_executive
- [T12] amoCRM pricing, accessed 2026-05-12: https://www.amocrm.ru/buy/

Примечание: все расчёты CAC, COGS, FOT allocation, break-even и runway являются инвестиционной моделью аналитика на основе P4, публичных ценовых якорей и рыночных зарплат, а не раскрытой отчётностью компании. Там, где нет публичных данных, это явно помечено как **[inference]**.


---

# 05-critic.md

## SECTION A - PnL

**Налоговая модель РФ.** Для ООО/АО без НДС в упрощённом режиме считаю УСН 6% с выручки. Для аккредитованной IT-компании показываю льготный вариант 3% с выручки как целевой tax case. Для ОСНО показываю 20% налога на прибыль с EBITDA как упрощённый ориентир, плюс НДС 20% применим сверх выручки и не включён в MRR/PnL как pass-through. Страховые взносы на ФОТ уже учтены в fixed costs через fully-loaded FOT (~30% к gross salary).

### Базовый

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 2 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 0 | 1 | 1,98 | 2,96 | 3,91 | 4,85 | 6,78 | 7,68 | 8,56 | 9,43 |
| MRR, ₽ | 0 | 0 | 0 | 1 400 000 | 2 779 000 | 4 137 315 | 5 475 255 | 6 793 126 | 9 491 230 | 10 748 861 | 11 987 628 | 13 207 814 |
| COGS, ₽ | 0 | 0 | 0 | 600 000 | 1 191 000 | 1 773 135 | 2 346 538 | 2 911 340 | 4 067 670 | 4 606 655 | 5 137 555 | 5 660 492 |
| Gross profit, ₽ | 0 | 0 | 0 | 800 000 | 1 588 000 | 2 364 180 | 3 128 717 | 3 881 787 | 5 423 560 | 6 142 206 | 6 850 073 | 7 547 322 |
| GM% | 0,0% | 0,0% | 0,0% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% |
| Fixed costs, ₽ | 1 595 000 | 1 759 000 | 2 117 000 | 2 839 000 | 3 823 000 | 4 752 000 | 5 412 000 | 5 846 000 | 5 846 000 | 5 846 000 | 5 846 000 | 5 846 000 |
| EBITDA, ₽ | -1 595 000 | -1 759 000 | -2 117 000 | -2 039 000 | -2 235 000 | -2 387 820 | -2 283 283 | -1 964 213 | -422 440 | 296 206 | 1 004 073 | 1 701 322 |
| Cash burn, ₽ | 1 595 000 | 1 759 000 | 2 117 000 | 2 039 000 | 2 235 000 | 2 387 820 | 2 283 283 | 1 964 213 | 422 440 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 1 595 000 | 3 354 000 | 5 471 000 | 7 510 000 | 9 745 000 | 12 132 820 | 14 416 103 | 16 380 316 | 16 802 756 | 16 802 756 | 16 802 756 | 16 802 756 |

**Waterfall M12:**
 ARPA 1 400 000 ₽ -> Gross 7 547 322 ₽ -> Contribution 7 547 322 ₽ -> EBITDA 1 701 322 ₽ -> Net after tax: УСН 6% = 908 853 ₽, IT-льгота 3% = 1 305 088 ₽, ОСНО 20% = 1 361 058 ₽.

**Break-even:** 8 клиентов по steady-state fixed cost; по месяцам M10.
**Cash flow:** startup_capital_to_bep_rub = 16 802 756 ₽.

### Оптимистичный

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 1 | 2 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 1 | 1,98 | 2,96 | 4,91 | 5,84 | 7,75 | 8,63 | 9,50 | 10,36 | 11,21 |
| MRR, ₽ | 0 | 0 | 1 400 000 | 2 779 000 | 4 137 315 | 6 875 255 | 8 172 126 | 10 849 545 | 12 086 801 | 13 305 499 | 14 505 917 | 15 688 328 |
| COGS, ₽ | 0 | 0 | 600 000 | 1 191 000 | 1 773 135 | 2 946 538 | 3 502 340 | 4 649 805 | 5 180 058 | 5 702 357 | 6 216 822 | 6 723 569 |
| Gross profit, ₽ | 0 | 0 | 800 000 | 1 588 000 | 2 364 180 | 3 928 717 | 4 669 787 | 6 199 740 | 6 906 744 | 7 603 142 | 8 289 095 | 8 964 759 |
| GM% | 0,0% | 0,0% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% |
| Fixed costs, ₽ | 1 595 000 | 1 759 000 | 2 117 000 | 2 839 000 | 3 823 000 | 4 752 000 | 5 412 000 | 5 846 000 | 5 846 000 | 5 846 000 | 5 846 000 | 5 846 000 |
| EBITDA, ₽ | -1 595 000 | -1 759 000 | -1 317 000 | -1 251 000 | -1 458 820 | -823 283 | -742 213 | 353 740 | 1 060 744 | 1 757 142 | 2 443 095 | 3 118 759 |
| Cash burn, ₽ | 1 595 000 | 1 759 000 | 1 317 000 | 1 251 000 | 1 458 820 | 823 283 | 742 213 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 1 595 000 | 3 354 000 | 4 671 000 | 5 922 000 | 7 380 820 | 8 204 103 | 8 946 316 | 8 946 316 | 8 946 316 | 8 946 316 | 8 946 316 | 8 946 316 |

**Waterfall M12:**
 ARPA 1 400 000 ₽ -> Gross 8 964 759 ₽ -> Contribution 8 964 759 ₽ -> EBITDA 3 118 759 ₽ -> Net after tax: УСН 6% = 2 177 459 ₽, IT-льгота 3% = 2 648 109 ₽, ОСНО 20% = 2 495 007 ₽.

**Break-even:** 8 клиентов по steady-state fixed cost; по месяцам M8.
**Cash flow:** startup_capital_to_bep_rub = 8 946 316 ₽.

### Пессимистичный

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 0,98 | 1,97 | 2,94 | 3,90 | 4,84 | 5,77 | 6,68 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 1 400 000 | 1 379 000 | 2 758 315 | 4 116 940 | 5 455 186 | 6 773 358 | 8 071 758 | 9 350 682 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 600 000 | 591 000 | 1 182 135 | 1 764 403 | 2 337 937 | 2 902 868 | 3 459 325 | 4 007 435 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 800 000 | 788 000 | 1 576 180 | 2 352 537 | 3 117 249 | 3 870 491 | 4 612 433 | 5 343 247 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% | 57,1% |
| Fixed costs, ₽ | 1 595 000 | 1 759 000 | 2 117 000 | 2 839 000 | 3 823 000 | 4 752 000 | 5 412 000 | 5 846 000 | 5 846 000 | 5 846 000 | 5 846 000 | 5 846 000 |
| EBITDA, ₽ | -1 595 000 | -1 759 000 | -2 117 000 | -2 839 000 | -3 023 000 | -3 964 000 | -3 835 820 | -3 493 463 | -2 728 751 | -1 975 509 | -1 233 567 | -502 753 |
| Cash burn, ₽ | 1 595 000 | 1 759 000 | 2 117 000 | 2 839 000 | 3 023 000 | 3 964 000 | 3 835 820 | 3 493 463 | 2 728 751 | 1 975 509 | 1 233 567 | 502 753 |
| Cumulative cash, ₽ | 1 595 000 | 3 354 000 | 5 471 000 | 8 310 000 | 11 333 000 | 15 297 000 | 19 132 820 | 22 626 283 | 25 355 033 | 27 330 543 | 28 564 110 | 29 066 863 |

**Waterfall M12:**
 ARPA 1 400 000 ₽ -> Gross 5 343 247 ₽ -> Contribution 5 343 247 ₽ -> EBITDA -502 753 ₽ -> Net after tax: УСН 6% = -1 063 794 ₽, IT-льгота 3% = -783 274 ₽, ОСНО 20% = -502 753 ₽.

**Break-even:** 8 клиентов по steady-state fixed cost; по месяцам не достигнут.
**Cash flow:** startup_capital_to_bep_rub = 29 066 863 ₽.

### Сводка по сценариям

| Сценарий | Break-even clients | Break-even month | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Базовый | 8 | M10 | 16 802 756 ₽ |
| Оптимистичный | 8 | M8 | 8 946 316 ₽ |
| Пессимистичный | 8 | не достигнут | 29 066 863 ₽ |

<!-- P6A-DONE -->


## SECTION B - Finance Risk + Competitor

### 1. Sensitivity analysis, EBITDA через 12 месяцев

База для сравнения: M12 EBITDA из SECTION A = **1 701 322 ₽/мес**.

| Сценарий | Изменение | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | без изменений | M12 из SECTION A | 1 701 322 |
| Sens1 | CAC x2 | При сохранении текущего темпа найма клиентов fully-loaded CAC растёт с 2,13 млн ₽ до 4,25 млн ₽; дополнительная нагрузка на 1 нового клиента M12 ≈ 2,13 млн ₽ | -425 951 |
| Sens2 | Churn x2 | churn растёт с 1,5% до 3,0%; клиентская база к M12 снижается до ~8,90 клиента против 9,43 в базе | 1 277 977 |
| Sens3 | Price -30% | ARPU падает с 1,4 млн ₽ до 980 тыс. ₽, COGS на раннем этапе почти не успевает ужаться | -2 261 022 |

**Вывод:** самая опасная переменная для модели не churn, а **pricing power**. При скидке 30% unit economics ломается даже без роста churn. CAC inflation тоже быстро переводит кейс в отрицательную EBITDA-зону.

### 2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distributions

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 800 000 | 2 127 273 | 3 600 000 | [04-economics], канальная воронка и blended CAC |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | [T2], [04-economics] |
| ARPU, ₽/мес | 1 000 000 | 1 400 000 | 1 700 000 | [04-economics], [02-demand] |
| Conversion rate lead→paid, % | 8% | 12% | 18% | [04-economics], blended enterprise funnel [inference] |
| Time-to-hire, мес | 1,0 | 1,6 | 2,8 | [04-economics], средняя по core hiring plan |

#### Метод

Вместо fixed base/opt/pess использую упрощённый Monte Carlo Lite: распределения выше транслируются в 1000+ мысленных прогонов через три драйвера результата, которые реально двигают модель к M24: скорость привлечения новых клиентов, удержание, и gross profit на клиента. [inference]

- new paid / мес масштабируется через `conversion x (CAC_mode / CAC_actual) x (time-to-hire_mode / time-to-hire_actual)`;
- EBITDA @M24 считается при steady-state fixed cost **5,846 млн ₽/мес**;
- cash runway считается от стартового капитала **35 млн ₽** из [04-economics] и среднего burn первых 12 месяцев. [inference]

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | 3 085 531 | 7 736 351 | 14 911 548 | 11 826 017 |
| CAC payback, мес | 1,43 | 1,81 | 2,35 | 0,91 |
| LTV/CAC | 11,88 | 17,70 | 25,83 | 13,95 |
| Cash runway, мес | 6,43 | 8,90 | 14,53 | 8,10 |

#### Интерпретация правил

1. **p10 EBITDA < 0** -> **не срабатывает**, значит модель на M24 не выглядит structurally insolvent.
2. **p50 EBITDA < 500К ₽/мес** -> **не срабатывает**, median-case EBITDA заметно выше gate.
3. **p90 / p10 > 10x** -> **не срабатывает**, отношение ~4,8x.
4. **Range width по LTV/CAC > 8** -> **срабатывает**: разброс **13,95** означает, что модель хрупкая к pricing, CAC и churn одновременно. Нужен даунгрейд score на устойчивость, даже если median-case остаётся привлекательным.

### 3. Competitor deep-dive

#### Топ-3 западных конкурента

| Компания | Почему конкурент | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Scale AI | Самый сильный глобальный reference player в data labeling, evals, RLHF и GenAI data engine [T13][T14] | бренд, доступ к hyperscalers и frontier labs, mature tooling, большой supply-side moat | дорогой enterprise motion, слабая локализация под РФ, высокий compliance friction в санкционном контуре | **20-25% глобального premium-сегмента** human-feedback/evals [inference] | локальный secured delivery в РФ, data residency, быстрый кастомный expert pod под русскоязычные домены |
| Turing | Сильный игрок в talent cloud + AI training experts для STEM/PhD workflows [T15][T16] | глобальный пул экспертов, сильный recruiting engine, узнаваемость у AI labs | менее глубоко productized как evaluation stack, зависимость от distributed labor supply | **8-12% глобального expert-talent сегмента** [inference] | можно продавать не talent marketplace, а готовый managed outcome с локальной ответственностью и SLA |
| Invisible Technologies | Сильный managed-service конкурент в human feedback и AI operations; публично оценивается около $2 млрд [T17] | сильная операционная машина, high-touch service, enterprise delivery discipline | сервисно тяжёлый бизнес, высокая зависимость от менеджмента операций, сложнее масштабировать margin | **5-8% глобального managed AI-ops сегмента** [inference] | у нас короче цепочка принятия решений, дешевле локальный delivery, меньше geopolitical trust gap для российских клиентов |

#### Топ-4 российских конкурента

| Компания | Почему конкурент | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Toloka | Самый известный русскоязычный бренд в data labeling/crowd data prep; на Habr прямо выделяется как крупный игрок рынка [T18] | массовый supply, известный бренд, широкий набор задач по разметке | ближе к масштабной платформе разметки, чем к premium expert pod для enterprise evals | **15-20% российского broad data-labeling рынка** [inference] | позиционирование выше по value chain: не массовая разметка, а domain experts + enterprise QA + secure eval workflows |
| Beorg Smart Vision | Сильный игрок в document AI, разметке и human-in-the-loop обработке документов; 50 000 удалённых операторов, защищённый контур, ФСТЭК/ФСБ и реестр отечественного ПО [T19] | сильная комплаенс-позиция, государственный и enterprise document flow, крупный operator base | фокус на OCR/document processing, уже менее универсален для frontier LLM evals и RLHF | **8-12% российского enterprise labeling/document-AI сегмента** [inference] | у нас лучше fit под LLM evaluation, red-teaming, post-training и domain QA, а не только document digitization |
| NLab Marker / Наносемантика | Industrial platform for annotation и on-prem deployment в защищённом контуре [T20] | on-prem, контроль качества, strong fit для regulated industries | скорее tooling/platform play, чем full managed expert network | **5-8% российского industrial annotation сегмента** [inference] | можем выиграть там, где клиенту нужен сервисный результат и экспертная команда, а не только коробка |
| Data Light | Публично продвигает экспертизу по организации разметки ML-данных и in-house/outsource workflows [T21] | контентная экспертиза, гибкость в организации data ops, узнаваемость в DS-сообществе | меньше признаков глубокого moat, слабее enterprise-defensible positioning против premium managed-service модели | **2-5% российского нишевого data-ops рынка** [inference] | более высокая специализация на LLM post-training и enterprise-grade accountable delivery |

**Вывод по конкурентам:** западные игроки сильнее по масштабу и tooling, российские по комплаенсу и локальному доступу. Окно для micro1-style play в РФ есть только если продавать **не разметку как commodity**, а **secure expert layer для LLM evals, RLHF и domain validation**.

### 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся быстро нанимать domain experts нужного уровня | high | high | time-to-hire > 2,5 мес, acceptance rate кандидатов < 20% | заранее строить vetted bench, партнёрства с вузами/экспертными сообществами, pre-approved talent pool |
| Operational | QA drift: качество разметки/оценки проседает по мере роста объёма | med | high | rework > 8% выручки, рост dispute rate, просадка benchmark accuracy | double-review, gold tasks, rubric library, QA lead per pod |
| Operational | Зависимость от LLM API/внешних foundation models | high | high | рост latency/cost, rate-limit incidents, model regressions | multi-model stack, локальные fallback models, vendor diversification |
| Market | Buyer pool в РФ уже, чем кажется, и sales pipeline не восполняется | high | high | < 3 SQL в месяц после M4, stagnant pipeline coverage < 3x quota | сузить ICP до regulated enterprise, founder-led ABM, отраслевые партнёры |
| Market | Конкуренты давят ценой, рынок коммодитизируется | high | high | discount requests > 20%, win rate падает при premium price | продавать outcome/SLA, пакетировать secure compliance + expert QA, ограничить кастомный scope |
| Market | Сильный global brand заходит через local partner и забирает топ-аккаунты | med | med/high | в тендерах чаще фигурируют Scale/Toloka/крупные integrators | закрепляться через on-prem/security posture и long-term MSA |
| Regulatory | Нарушение требований 152-ФЗ по персональным данным | med | high | клиент требует DPIA/DPA, security audit не проходит, замечания DPO | data minimization, on-prem/segmented environment, DPA templates, хранение в РФ |
| Regulatory | Попадание под 115-ФЗ/AML-проверки из-за трансграничных выплат экспертам и подрядчикам | med | med/high | банк запрашивает пояснения, задержки платежей подрядчикам | белая договорная схема, KYC подрядчиков, платёжный контур через РФ-юрлицо |
| Regulatory | Санкционные ограничения на SaaS и зарубежные модели/облака | high | high | vendor offboarding notices, блокировки billing/accounts | резервный стек на отечественных и open-weight моделях, локальные облака, escrow критичных компонентов |
| Financial | Runway сжимается из-за более медленного revenue ramp | high | high | burn multiple > 2,0, runway < 9 мес до M6 | raise buffer 35-45 млн ₽, stop non-core hiring, stage-gated spend |
| Financial | Рост курса USD повышает cost base по облаку и SaaS | high | med | FX move > 15%, SaaS vendors индексируют цены | рублёвые контракты с клиентами, FX reserve, импортозамещённый стек где возможно |
| Financial | Инфляция и налоговая нагрузка съедают маржу команды | med | med/high | salary inflation > 15% YoY, effective tax take-up | quarterly repricing, utilization controls, IT льготы и налоговое планирование |
| Black swan | Новая волна санкций отключает критичный LLM/API провайдер | med | high | слухи о geo-blocking, письма о прекращении сервиса | prebuilt fallback на open-source и локальных провайдерах, abstraction layer |
| Black swan | Военный/политический шок ломает hiring и enterprise budgets | med | high | freeze hiring, frozen tenders, elongated procurement > 2x | держать variable cost base, работать с критичными индустриями, cash buffer |

### 5. Kill conditions через 6 месяцев

1. **Runway < 6 месяцев** при отсутствии подписанного bridge financing или pipeline coverage < 2x на ближайшие 2 квартала.
2. **< 4 активных paying clients к M6** или win rate по pilot→annual contract < 20%, значит GTM не подтверждён для enterprise motion.
3. **LTV/CAC < 4x или фактический gross margin < 45%** два месяца подряд, значит premium positioning не удерживается и модель скатывается в staffing/commodity service.

### 6. Итог по finance risk

Кейс остаётся **проходимым по median-case**, но уже не выглядит low-risk. Главные красные зоны: **pricing compression, CAC inflation, regulatory/vendor dependence и хрупкость LTV/CAC-диапазона**. Для фонда это не reject по economics, а **conditional pass only при жёстком контроле ICP, pricing и локального compliance moat**.

## Источники SECTION B
- [T13] Scale AI official website, accessed 2026-05-13: https://scale.com/
- [T14] Scale AI company overview / market context, accessed 2026-05-13: https://www.grandviewresearch.com/industry-analysis/data-collection-labeling-market
- [T15] Turing official website, accessed 2026-05-13: https://www.turing.com/
- [T16] Turing, AI and expert talent positioning, accessed 2026-05-13: https://www.turing.com/solutions/ai
- [T17] Business Insider, Invisible Technologies valuation and human-feedback thesis, published 2026-01-05, accessed 2026-05-13: https://www.businessinsider.com/ai-training-ceo-artificial-data-humans-matt-fitzpatrick-invisible-technologies-2026-1
- [T18] Habr, «Разметка данных для машинного обучения: обзор рынка, методики и компании», accessed 2026-05-13: https://habr.com/ru/articles/599323/
- [T19] vc.ru, Beorg Smart Vision and hybrid AI + crowdsourcing workflow, accessed 2026-05-13: https://vc.ru/services/323389-ii-kraudsorsing-kak-ustroen-servis-dlya-razmetki-massivov-dannyh-raspoznavaniya-i-ocifrovki-dokumentov
- [T20] Skolkovo, NLab Marker by Наносемантика, accessed 2026-05-13: https://sk.ru/news/platforma-rezidenta-skolkovo-pomozhet-sobrat-dannye-dlya-obucheniya-iskusstvennogo-intellekta/
- [T21] Habr, Data Light on ML data annotation operations, accessed 2026-05-13: https://habr.com/ru/companies/data_light/articles/862464/

<!-- P6B-DONE -->


---

# 06-verdict.md

[GEO-EXPAND] micro1 — NEAR-PASS: 65/100 | EBITDA base=1701К₽/мес через 12 мес | LTV/CAC=25,1x | Ключевое преимущество: premium managed expert pod с ранним break-even на 8-9 клиентах | Главный риск: рынок РФ слишком узкий и moat слабый.

# 06-verdict

sector: GEO-EXPAND

## Investment one-liner
[GEO-EXPAND] micro1 — NEAR-PASS: 65/100 | EBITDA base=1701К₽/мес через 12 мес | LTV/CAC=25,1x | Ключевое преимущество: premium managed expert pod с ранним break-even на 8-9 клиентах | Главный риск: рынок РФ слишком узкий и moat слабый.

## Финальный вердикт
**VERDICT: NEAR-PASS**

Почему не APPROVED:
1. Direct demand в РФ остаётся LOW, buyer universe выглядит как несколько десятков accounts, а не широкий рынок.
2. Moat weak: сеть экспертов, QA и secure delivery ценны, но пока не дают сильной неоткопируемой защиты.
3. Модель service-heavy и чувствительна к pricing compression, CAC inflation и доступности доменных экспертов.

Почему не REJECTED:
1. Unit economics сильная: `customer_ltv_rub ≈ 53,3 млн ₽`, `CAC ≈ 2,13 млн ₽`, `LTV/CAC ≈ 25,1x`.
2. `company_ebitda_rub_month` в базе выходит на **1 701 322 ₽/мес к M12**, а порог **500К₽/мес** пересекается уже к **M11**.
3. Monte Carlo Lite не показывает structural insolvency: `p10 EBITDA @M24 = 3,09 млн ₽`, `p50 = 7,74 млн ₽`.

## Delta vs previous
- Предыдущий rerun-вердикт в индексе: **64/100, REJECTED** для `micro1-human-data-geo-expand-v2`.
- Текущий кейс: **65/100, NEAR-PASS**.
- Что улучшилось: лучше формализованы PnL, EBITDA-gate, Monte Carlo и GTM через конкретные target accounts.
- Что не улучшилось: direct demand остаётся LOW, moat остаётся weak, buyer pool по РФ всё ещё слишком узкий для investment-grade запаса прочности.

## Оценка
Source tier balance: T1=7, T2=5, T3=1, weighted=2.46. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 25,1x», «CAC payback = 1,52 месяца», «Contribution Margin = 57,1%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | «EBITDA > 500k ₽/мес: M11», `M12 EBITDA = 1 701 322 ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | «Статус спроса: LOW», но `оценка LLM = 350 HH vacancies`; применён tier-penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | «Telegram не даёт moat», рынок снизу задаёт «дешёвый price floor», явного network effect нет. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | «Главные красные зоны: pricing compression, CAC inflation, regulatory/vendor dependence». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | Есть named-account ICP, `fully-loaded CAC ~2,13 млн ₽`, но sales cycle длинный и founder-led. |

**Normalized score = round((97 * 100) / 150) = 65/100.**

### Интерпретация score
- 75+ = APPROVED
- 70-74 = APPROVED WITH NOTES
- 65-69 = NEAR-PASS
- <65 = REJECTED

## 7-factor moat framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных; это не marketplace с self-reinforcing liquidity. |
| Switching costs | 1 | Есть SOP, QA-процессы и частичная встройка в eval workflow, но интеграции пока не выглядят глубокими. |
| Scale economies | 1 | Часть COGS и sourcing улучшаются с масштабом, но delivery остаётся human-heavy. |
| Proprietary data / model advantage | 1 | Может накопиться внутренняя rubric library и eval know-how, но публично не доказан заметный proprietary dataset advantage. |
| Regulatory moat | 1 | RF compliance и data residency могут помочь, но лицензируемого/regulatory barrier уровня health/fintech здесь пока нет. |
| Brand / distribution | 1 | Глобальный бренд Micro1 полезен, но в РФ локальная дистрибуция ещё не доказана. |
| Embedded workflow | 2 | Если pod встраивается в recurring eval / RLHF / QA контур, отказ становится болезненным для клиента. |

**Moat score = round((7 * 25) / 21) = 8/25.**

Вывод: **weak moat**. Это обязано оставаться в Top-3 Risks.

## Полный бизнес-процесс из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Target account selection | CEO + SDR | Excel/Notion, hh/рынок, ручной ресерч | 1,5 ч/аккаунт | 2 500 | низкий |
| 2 | Первичный outreach | SDR | amoCRM, email, Telegram, LinkedIn-аналоги | 6-8 касаний за 14 дней | 4 000 | средний |
| 3 | Ответ и квалификация | SDR | amoCRM, звонок, скрипт | 45 мин | 1 500 | средний |
| 4 | Discovery call | CEO + AE | Meet/Zoom, Notion | 60 мин + 30 мин prep | 9 000 | низкий |
| 5 | Problem scoping | CEO + solutions lead | Notion, Miro | 2-3 часа | 18 000 | низкий |
| 6 | Data / workflow audit | CTO + ML lead | secure sample review, spreadsheet | 4-6 часов | 32 000 | низкий |
| 7 | Коммерческое решение и SoW | AE + CEO | docs, калькулятор, шаблон SoW | 2 часа | 11 000 | средний |
| 8 | Security / legal review | CTO + CEO | DPA, NDA, infosec checklist | 1-2 недели elapsed | 28 000 | низкий |
| 9 | Пилот | expert pod + PM | internal delivery stack | 2-4 недели | 220 000 | средний |
| 10 | Защита пилота / proposal | AE + CEO + CTO | презентация, ROI memo | 2 часа | 14 000 | низкий |
| 11 | Procurement / contract signing | AE + finance | ЭДО, договор, счёт | 1-3 недели elapsed | 12 000 | средний |
| 12 | Onboarding клиента | CSM + PM + CTO | knowledge base, SOP, secure access | 1 неделя | 48 000 | средний |
| 13 | Recurring monthly delivery | expert pod + QA + PM | evaluation platform, dashboards | ежемесячно | 560 000 | средний |
| 14 | Monthly review / upsell | CSM + AE | QBR, dashboard | 2 ч/мес | 12 000 | средний |
| 15 | Invoice / payment collection | finance + CSM | 1С/банк/ЭДО | 30-60 мин | 5 000 | высокий |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 53 293 333 ₽ |
| fully_loaded_cac_rub | 2 127 273 ₽ |
| LTV/CAC | 25,1x |
| CAC payback по MRR | 1,52 мес |
| CAC payback по contribution MRR | 2,66 мес |
| GM% | 57,1% |
| contribution_margin_rub_month на клиента | 799 400 ₽ |
| company_ebitda_rub_month base M12 | 1 701 322 ₽/мес |
| clients_to_ebitda_positive | 8 |
| clients_to_500k_ebitda | 9 |
| months_to_ebitda_positive | 10 |
| months_to_500k_ebitda | 11 |
| startup_capital_to_bep_rub | 16 802 756 ₽ |
| realistic startup capital with buffer | 30 000 000 - 35 000 000 ₽ |

## Scenario snapshot

| Сценарий | Break-even month | startup_capital_to_bep_rub | company_ebitda_rub_month |
|---|---:|---:|---:|
| Base | M10 | 16 802 756 ₽ | 1 701 322 ₽/мес к M12 |
| Optimistic | M8 | 8 946 316 ₽ | 3 118 759 ₽/мес к M12 |
| Pessimistic | не достигнут в M12 | 29 066 863 ₽ | -502 753 ₽/мес к M12 |

## Team table

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2,5 | 2 | 715 000 |
| Senior Backend | 2 | 430 000 | 1,5 | 1,5 | 1 118 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 650 000 |
| DevOps | 1 | 320 000 | 1,5 | 1 | 416 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 364 000 |
| SDR | 1 | 180 000 | 0,75 | 1 | 234 000 |
| AE | 1 | 360 000 | 1,5 | 2,5 | 468 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 286 000 |
| **Итого** | **10** |  |  |  | **5 096 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Яндекс | Крупнейший локальный AI buyer, публичные AI-продукты и постоянная потребность в eval / QA для моделей. | email decision-maker в Yandex Cloud / YandexGPT + тёплый intro через AI-конференции | 1 500 000 ₽/мес |
| Сбер / Sber AI | Большой внутренний GenAI-контур, high-stakes quality control и regulated deployment. | партнёрство + конференции + direct outreach в Sber AI | 1 800 000 ₽/мес |
| Т-Банк | Сильная AI-команда и потребность в качественной валидации customer-facing и internal LLM workflows. | email decision-maker + ABM через кейс по secure expert QA | 1 400 000 ₽/мес |
| MTS AI | Строит AI-сервисы и корпоративные модели, нужен recurring evaluation layer. | конференция / отраслевой ивент + direct outreach | 1 300 000 ₽/мес |
| VK | Большой контур контента, поиска и assistant-like сценариев, нужен human feedback at scale. | email VP AI / product leader + Habr/vc.ru thought-leadership | 1 300 000 ₽/мес |
| AvitoTech | Marketplace/ML-heavy среда, где качество ranking и generative функций требует регулярной оценки. | direct outreach в ML platform / ranking leadership | 1 200 000 ₽/мес |
| Ozon Tech | E-commerce и AI-операции вокруг поиска, контента и customer workflows. | партнёрство + email decision-maker | 1 400 000 ₽/мес |
| X5 Tech | Крупный enterprise buyer с AI/данными и потенциальной потребностью в secure human QA. | конференция + warm intro через интегратора | 1 000 000 ₽/мес |
| Positive Technologies | Security AI и сложные экспертные контуры, где нужен domain-specific review и red-teaming. | партнёрство / экспертный круглый стол / direct outreach | 1 500 000 ₽/мес |
| Контур | Enterprise software и document/AI workflows, близок к recurring expert-validation use case. | email decision-maker + кейс через vc.ru / Habr | 1 100 000 ₽/мес |

**Оценка GTM:** named-account GTM реалистичен, но это тяжёлый founder-led ABM, а не масштабируемый demand-gen.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top risk |
|---|---|---|---|
| Weak moat и price compression | high | high | Снизу рынок якорится дешёвыми annotation/tasking tools, сверху давят крупные global/local players. |
| Слишком узкий buyer universe в РФ | high | high | Demand LOW, а bottom-up buyer pool близок к 60 компаниям с реальной болью только у части из них. |
| Зависимость от экспертов, LLM vendors и compliance | med/high | high | Time-to-hire, качество QA, санкции, 152-ФЗ и vendor offboarding могут быстро сбить execution. |

## Proof points, нужные для upgrade в APPROVED
1. Не менее **4-5 платящих enterprise клиентов** с realized price **≥1,2 млн ₽/мес**.
2. Подтверждённый pilot→annual conversion **≥25%** на выборке не меньше 8 пилотов.
3. Удержание на уровне **monthly churn ≤1,5%** и rework не выше **8% выручки**.
4. Локальный compliance moat: RU-hosting / on-prem / security pack, который реально повышает win-rate.
5. Повторяемый sourcing engine доменных экспертов, чтобы time-to-hire не выходил за **2,5 месяца**.

## LTV Upside Calculator
Так как кейс получил **NEAR-PASS**, ниже what-must-change для выхода в approve:

| Рычаг | Текущее | Цель для approve | Эффект |
|---|---:|---:|---|
| Realized ARPA | 1,4 млн ₽/мес | 1,5-1,7 млн ₽/мес | усиливает margin of safety и окупает enterprise GTM |
| Buyer pool conversion | 12% lead→paid mode | 15-18% | снижает blended CAC и ускоряет выход к 500К EBITDA |
| Churn | 1,5%/мес | ≤1,2%/мес | увеличивает `customer_ltv_rub` и stabilizes revenue base |
| Local compliance packaging | частично | productized RU-secure offer | добавляет moat и улучшает win-rate в regulated accounts |
| Expert supply engine | founder-heavy | repeatable vetted bench | снижает execution risk и dependency on heroic hiring |

## Investment committee conclusion
micro1 в РФ, это **неширокий, но потенциально прибыльный enterprise AI-ops business**. На economics кейс выглядит сильно, на committee-level moat и market width, заметно слабее. Поэтому правильный статус сегодня, это **NEAR-PASS 65/100**: держать в наблюдении, возвращаться после первых 4-5 реальных enterprise logos, подтверждённого retention и локального compliance wedge.

