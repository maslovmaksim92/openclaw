---
stage: demand-validation
case: 2216-msk-supio-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: REJECT
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
2216 MSK Supio GEO Expand, AI-платформа для plaintiff-side personal injury и mass tort law firms: medical record review, chronology, demand drafting и litigation workflow.

## Итог
**Статус: REJECT**

Глобально категория реальна: у Supio есть сильный category proof, заметный рост и понятная ценность для plaintiff-side firms в США. Но для локального geo-expand кейса этого недостаточно. В РФ и близком контуре exact-demand практически отсутствует, а главное, не подтверждён сам экономический слой, на котором в США держится продукт: contingency-driven plaintiff PI / mass tort ecosystem с крупными settlement-driven бюджетами на case prep.

Иными словами, это не fake category, а **сильная американская vertical category со слабой локальной переносимостью**. Для P3 этого достаточно, чтобы кейс **не пропускать дальше**: evidence of demand есть в США, но для локального спроса и локального willingness-to-pay подтверждений пока нет.

## 1. Demand data
Источник exact-check: `http://172.18.0.1:9001/multi-demand?keyword=plaintiff%20legal%20AI`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Дополнительные смежные проверки:

### `medical record review software legal`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `personal injury case management AI`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `demand letter automation legal`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### Интерпретация
Search demand в РФ почти нулевой по всем разумным входам. Для enterprise/legal vertical это не автоматический стоп-фактор, но здесь нет даже косвенных локальных сигналов, что рынок уже формируется как software category.

## 2. Реальные рыночные сигналы и why now
1. **30 апреля 2025 года** Supio объявила о раунде **$60 млн Series B**, доведя суммарное финансирование до **$91 млн**. Компания заявила **4x ARR growth** с момента Series A и работу со многими top personal injury и mass tort firms в США.
2. На публичном сайте Supio указывает **$1B+ in settlements**, **100k+ cases processed** и **+28% higher settlements** как category-level outcome claims.
3. Supio позиционирует решение как полный workflow stack для PI: medical record review, chronology, demand drafting и litigation support, то есть продаёт не point tool, а operating layer поверх plaintiff-case preparation.
4. На продуктовой странице demand drafting компания заявляет **96.6% extraction accuracy** и human-verification option, что показывает готовность рынка платить за risk-controlled AI, а не только за cheap drafting.
5. Thomson Reuters в отчёте от **26 июня 2025 года** сообщил, что организации с видимой AI-стратегией в профессиональных сервисах вдвое чаще видят revenue growth от AI, а **88%** профессионалов предпочитают domain-specific AI assistants. Это усиливает общий why-now для legal AI.

### Вывод
В США спрос на такую категорию подтверждён: есть funding, рост, клиенты, case-study outcomes и общий AI tailwind в legal-tech. Проблема не в отсутствии global demand, а в переносимости этого спроса в локальный контур.

## 3. Конкурентные и ценностные якоря

| Якорь | Публичный сигнал | Что это доказывает |
|---|---|---|
| Supio homepage | $1B+ settlements, 100k+ cases processed, +28% settlements | продукт используется в реальных plaintiff workflows, а не только в демо-режиме |
| Supio Series B press release | $60M round, total funding $91M, 4x ARR growth | категория коммерчески растёт и видна инвесторам |
| Supio CaseAware AI | 112 case types, 96.6% extraction accuracy, 97% citation precision | есть technology wedge под сложные case records |
| Travis Legal Offices case study | кейсы, где офферы выросли с $700k до $3M, $400k до $800k, $100k до $740k | value capture завязан на больших settlement outcomes, а не просто на time saving |

### Вывод по конкурентному полю
Спрос в базовом американском рынке выглядит подтверждённым. Но все сильные proof-points привязаны к US plaintiff PI economics: высокий upside от settlement optimization, объёмные medical records, deposition-heavy workflows и готовность фирмы инвестировать в инструменты, которые реально двигают размер взыскания.

## 4. Российский контур и substitutes
Прямого локального аналога Supio в открытых сигналах не видно. Возможные substitutes в РФ:
- ручной разбор меддокументов и судебных материалов юристами/помощниками;
- general-purpose LLM + шаблоны документов;
- обычные case management / document management системы без vertical AI слоя;
- нишевые эксперты по медико-правовой подготовке и судебной экспертизе.

### Ключевая проблема локализации
Локальная переносимость выглядит слабой. Это **вывод-инференс**, а не прямой факт из источников: публичные proof-points Supio строятся вокруг экономики plaintiff-side personal injury и mass tort firms в США, тогда как в РФ не видно подтверждённого слоя сопоставимых law firms с таким же объёмом high-value claims, тем же процессом demand preparation и той же готовностью платить за ускорение settlement engine.

Именно поэтому даже хороший global proof не конвертируется автоматически в local demand proof.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
- Для локального case беру **250 000 ₽/мес** = **3 млн ₽/год** на клиента как optimistic enterprise/legal workflow чек.
- Это ниже американской implied value capture и уже предполагает, что продукт урезан до более общего litigation-support workflow.
- ICP в локальном контуре: крупные litigation boutiques, юридические фирмы со страховыми и медико-правовыми спорами, редкие контуры mass-claims / consumer disputes.

### TAM
Беру **60** потенциально релевантных организаций.

**TAM = 60 × 3 000 000 ₽ = 180 млн ₽/год**

### SAM
Реально достижимый digital-mature слой, где вообще возможна покупка специализированного AI-инструмента.

Беру **15** организаций.

**SAM = 15 × 3 000 000 ₽ = 45 млн ₽/год**

### SOM
Ранний реалистичный слой: **3 контракта**.

**SOM = 3 × 3 000 000 ₽ = 9 млн ₽/год**

### Вывод по рынку
Даже при оптимистичных допущениях локальный рынок выглядит узким и хрупким. К тому же сам ICP пока скорее гипотетический, чем подтверждённый реальными публичными сигналами покупки.

## 6. WTP и доказательства готовности платить
1. В США WTP подтверждён косвенно через funding, рост ARR, customer stories и outcome-linked ROI.
2. Travis Legal Offices показывает, что value proposition может быть огромным, если инструмент materially повышает settlement outcomes.
3. Но локально такого же подтверждения нет: нет публичных сигналов о зрелой категории plaintiff-legal AI, нет visible local buyers, нет якорей по ценам и нет признаков, что firms в РФ уже покупают подобный vertical stack.

### Вывод по WTP
**Глобально WTP подтверждён, локально не подтверждён.**

Для geo-expand кейса этого недостаточно, потому что standing logic здесь требует доказать не просто существование категории где-то в мире, а реалистичность локального спроса и монетизации.

## 7. Profit Gate
Нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Conservative
- Цена: **150 000 ₽/мес**
- GM: **55%**
- Валовая прибыль на клиента: **82 500 ₽/мес**
- Для fixed costs **1,5 млн ₽/мес** нужно **19 клиентов**

**Вердикт: FAIL**

### Сценарий B. Base-case
- Цена: **250 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **150 000 ₽/мес**
- Нужно **14 клиентов**

**Вердикт: FAIL**

### Сценарий C. Premium litigation workflow
- Цена: **400 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **260 000 ₽/мес**
- Нужно **8 клиентов**

**Вердикт: STRETCH**

### Вывод по Profit Gate
Profit gate не выглядит убедительным. Чтобы пройти его, нужен либо существенно больший локальный рынок, либо намного более высокий чек, но публичных подтверждений для любого из этих условий пока нет.

## 8. Общий вывод
- Search demand в РФ: **LOW**
- Global category proof: **сильный**
- Local category proof: **слабый / отсутствует**
- WTP: **подтверждён в США, не подтверждён локально**
- Localizability: **слабая**
- Profit Gate: **не проходит убедительно**

## 9. Решение для пайплайна
**Отклонить на этапе demand validation.**

Причины:
1. глобальный спрос есть, но локальный спрос не подтверждён;
2. economics Supio опирается на US plaintiff PI / mass tort structure, для которого локальный аналог не доказан;
3. even optimistic TAM/SAM/SOM остаются узкими;
4. profit gate не собирается без слишком смелых допущений.

## Market Pulse
Market Pulse 20.04.2026: сильный product-market fit в США, но слабая доказательная база для локального geo-expand.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=plaintiff%20legal%20AI
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=medical%20record%20review%20software%20legal
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=personal%20injury%20case%20management%20AI
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=demand%20letter%20automation%20legal
- Supio Series B press release, 2025-04-30: https://www.supio.com/press/supio-announces-60m-series-b-to-accelerate-adoption-of-legal-ai-in-plaintiff-law
- Supio homepage: https://www.supio.com/
- Supio CaseAware AI: https://www.supio.com/case-aware-ai
- Supio AI Demand Letter Drafting: https://www.supio.com/products/ai-demand-letter
- Supio customer story, Travis Legal Offices: https://www.supio.com/customers/travis-law-offices
- Thomson Reuters press release on 2025 Future of Professionals report, 2025-06-26: https://www.thomsonreuters.com/en/press-releases/2025/june/the-ai-adoption-reality-check-firms-with-ai-strategies-are-twice-as-likely-to-see-ai-driven-revenue-growth-those-without-risk-falling-behind

## Market Pulse
> Market Pulse 2026-04-20: растущий интерес.
## Market Pulse
- Market Pulse 2026-04-21: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.

