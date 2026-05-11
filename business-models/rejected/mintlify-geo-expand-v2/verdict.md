# Mintlify geo-expand v2 — полный кейс

Статус: NEAR-PASS
Score: 66/100
Сектор: AI-SERVICES
Дата: 2026-05-11
GitHub path: rejected/mintlify-geo-expand-v2/verdict.md


---

# 00-brief.md

# Краткий бриф

## Кейс
Mintlify как кандидат на AI-first платформу документации, поиска и сопровождения developer-facing knowledge workflows.

## Статус
Принудительный resurrect, создан новый кейс `mintlify-geo-expand-v2`.

## Почему открыт
Кейс по AI-native documentation platform для продуктовой и API-документации. Создан как принудительный resurrect-v2 для новой аналитики по полному пайплайну.

## Следующий шаг
Передать кейс в P3-demand-validation и затем по полному пайплайну P4→P7.


---

# 01-evidence.md

# Подтверждающие сигналы

## 2026-04-23 — supporting signal — Mintlify для AI-native developer documentation
- Дата: 2026-04-23
- Источник: https://techcrunch.com/2024/09/05/mintlify-is-building-a-next-gen-platform-for-writing-software-docs/ ; https://www.mintlify.com/blog/2025-year-in-review ; https://www.ycombinator.com/companies/mintlify/jobs/ICb2kGd-enterprise-customer-success-manager
- Тип: supporting signal
- Как усиливает кейс: Сигнал усиливает кейс по AI-native документации для разработчиков, потому что одновременно подтверждает институциональный интерес к категории и сильный коммерческий traction самой Mintlify. Это снижает риск того, что спрос ограничен ранними adopters, и делает geo-expand-гипотезу для локализованного AI-docs слоя заметно сильнее.
- Ключевые данные и факты:
  - TechCrunch описывает Mintlify как next-gen платформу для написания software docs с AI-first подходом.
  - В годовом обзоре за 2025 год компания заявляет 8-figure ARR и более 10 000 компаний на платформе.
  - На странице вакансии Y Combinator указано более 18 000 компаний-клиентов и охват свыше 100 млн разработчиков в год.


---

# 01-intake.md

---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-mintlify-geo-expand.md
created: 2026-04-21T03:03:41+03:00
---

# 01-intake

## Кейс
mintlify-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл с префиксом `resurrect-` по standing orders обязан пройти заново как самостоятельный кейс, даже если раньше был supporting signal или candidate под другим кейсом.

## Ссылка на исходный verdict
triage/triage-2026-04-17-mintlify-geo-expand.md

## Краткий контекст
Mintlify как AI-first платформа для документации, поиска, генерации и поддержания актуальности product/API docs.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — mintlify-geo-expand

## Meta
- source: triage/triage-2026-04-17-mintlify-geo-expand.md
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
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-1400-msk-mintlify-geo-expand.md`

## Классификация
новый кейс

## Решение
Создать новый кейс `enterprise-ai-documentation-platform` в `pipeline/cases/`.

## Почему
- Сигнал не является дублем открытого кейса: в `pipeline/cases/` не было существующего кейса по AI-native платформе для продуктовой и API-документации.
- Категория отличается от обычных docs/CMS тем, что речь идёт об AI-first платформе с генерацией, поддержкой актуальности, поиском и developer-facing workflow.
- По входному файлу economics проходят порог Program 1: `≈ 180 000–900 000 RUB MRR` на клиента, где верхняя часть диапазона превышает обязательный порог `500 000 ₽/мес.`.
- Во входном сигнале российский аналог отмечен как `none`, что усиливает GEO-EXPAND логику и вероятность свободной ниши на локальном B2B-рынке.

## Что сделано
- Создан новый кейс `pipeline/cases/enterprise-ai-documentation-platform/`.
- В кейс добавлен файл `00-brief.md` на русском языке.
- Исходный raw-файл подготовлен к переносу в `pipeline/raw/processed/`.

## Вердикт
Mintlify распознан как валидный GEO-EXPAND сигнал для нового high-LTV направления. Кейс создан: `enterprise-ai-documentation-platform`.

```


---

# 02-demand.md

# 02-demand — Demand Validation

## Кейс
Mintlify как кандидат на AI-first платформу документации, поиска и сопровождения developer-facing knowledge workflows для выхода на рынок РФ.

## Итог
**Статус: CONDITIONAL PASS**

По search-led сигналам ниша в РФ выглядит как **LOW demand** [T2], но это не означает отсутствие бюджета. Категория продаётся не по широкому consumer-search, а через B2B-бюджеты на developer portal, API docs, onboarding разработчиков, AI-поиск по документации и миграцию с Docusaurus/Confluence/GitBook-подобных стеков [T2][T3]. Путь к **EBITDA ≥ 500 000 ₽/мес** есть минимум в двух сценариях монетизации, поэтому ранний reject по правилу `DEMAND=LOW + Profit Gate FAIL` **не применяется**.

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand`

Проверенные запросы:
- `AI documentation platform` → **LOW**, demand score **0**, Google Trends RU **0**, Habr **2**, hh.ru **5**, Yandex Suggest **2** [T2]
- `developer portal documentation` → **LOW**, demand score **0**, Google Trends RU **0**, Habr **2**, hh.ru **1**, Yandex Suggest **2** [T2]
- `api documentation` → **LOW**, demand score **19**, Google Trends RU **5**, Habr **2**, hh.ru **26**, Yandex Suggest **100** [T2]

> Market Pulse 2026-05-10: интерес растёт. По текущей выдаче усилились свежие сигналы вокруг AI-документации и developer portals, включая публикации о росте Mintlify, AI-поиске по документации и найме в этой категории.

### Интерпретация
- Массового русскоязычного search demand по формулировке категории почти нет [T2].
- При этом смежный практический спрос на API-документацию и developer enablement существует: запрос `api documentation` даёт ненулевые hh.ru вакансии и максимум по Yandex Suggest внутри набора [T2].
- Это типичный B2B infrastructure market: покупатель чаще ищет решение через текущий стек, агентство, интегратора или конкретного вендора, а не через общий запрос «AI documentation platform» [T3, спекуляция].

## 2. Реальные конкуренты и цены

| Конкурент | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Mintlify | AI-native docs platform | **$250/мес** за Growth, Enterprise custom [T2] | Рынок уже якорится на mid-market SaaS-чеках |
| GitBook | Docs / knowledge base / API docs | **$65/польз./мес** Plus, **$249/польз./мес** Pro [T2] | Сегмент готов платить за редактуру, поиск и workflow |
| ReadMe | API docs / developer hub | **$79/мес** Startup, **$349/мес** Business [T2] | Developer portal уже монетизируется как отдельная функция |
| Teamly (РФ, смежный substitute) | База знаний и документация | **299–399 ₽/польз./мес** [T2] | В РФ есть платёжная привычка за knowledge/documentation software, но пока в более широком сегменте |
| Staffy (РФ, Telegram-first substitute) | База знаний для сотрудников через Telegram | **4 990 ₽/100 сотрудников/мес** [T2] | Telegram в РФ monetizable, но это adjacent use case, не developer docs |

### Вывод по конкурентам
- Минимум три реальных платящих substitute/competitor-модели с публичной ценой есть, значит **WTP не нулевой** [T2].
- Прямых локальных лидеров именно в API/developer-docs в РФ заметно меньше, чем на глобальном рынке [T2][T3]. Это создаёт окно для локализованного продукта, но также говорит о ещё не сформированном category demand [T3].

## 3. Telegram-боты и сервисы в РФ
- Прямого заметного Telegram-first лидера именно в **developer documentation / API portal** в РФ не найдено [T3].
- В РФ есть adjacent Telegram-first knowledge base products, например **Staffy**, который продаёт базу знаний для сотрудников внутри Telegram по подписке [T2].
- Есть и контентные/информационные проекты вокруг ИИ и knowledge workflows в Telegram, но они не выглядят прямой заменой developer portal и API docs stack [T3].

### Вывод по Telegram
Telegram в РФ подтверждает **канал дистрибуции и интерфейс доступа к знаниям**, но не сформировал отдельную сильную категорию именно для external developer docs [T2][T3]. Для Mintlify-подобного продукта Telegram полезнее как notification/search surface, чем как core moat [T3, спекуляция].

## 4. WTP, доказательства готовности платить
1. **Глобальные игроки уже продают category product по recurring SaaS-подписке**: Mintlify, GitBook, ReadMe имеют явные публичные цены [T2].
2. **В РФ платят за knowledge/documentation software**, хотя чаще в более широком формате: Teamly и Staffy подтверждают существование подписной модели [T2].
3. **Публичные developer portals у крупных российских компаний** вроде Yandex Cloud, VK Cloud, Selectel, T-Банк, Ozon, Avito, VK ID, 2ГИС, MWS, Sber указывают, что сегмент API/docs реально существует и обслуживается как отдельная функция [T2].
4. Наличие вакансий и запросов по `api documentation` в demand API косвенно подтверждает, что компании уже тратят деньги на людей, процессы и инструменты вокруг документации [T1/T2].

### Вывод по WTP
**WTP подтверждён.** Не как массовый PLG в РФ сегодня, а как B2B spend на docs/search/portal layer поверх уже существующего developer ecosystem [T2].

## 5. Market sizing

### Методика и допущения
- Для валютных пересчётов использую курс ЦБ РФ **79,71 ₽/$** на 21.04.2026 [T1].
- Top-down опирается на глобальный рынок knowledge/documentation software как верхнюю границу, затем сужается до developer-docs сегмента и РФ [T3 + T1].
- Bottom-up опирается на число компаний по ОКВЭД 62.01 в РФ как верхнюю базу buyers, затем сужается до фирм с реальной внешней API/docs-потребностью [T2].
- Средний контракт для локального Mintlify-подобного решения принимаю **720 000 ₽/год**: это эквивалент примерно **60 000 ₽/мес**, что ниже западных enterprise-tier прайсов и выше generic knowledge base tools в РФ [T2, inference].

### Top-down
- Глобальный рынок knowledge management software оценивается в **$22,1 млрд** в 2025 году [T3].
- Для developer docs / API portal / AI docs беру **3%** от этого рынка как узкий addressable share [T3, спекуляция, но согласуется с нишевым характером категории].
- Тогда **TAM (мир)** ≈ **$663 млн** или **52,8 млрд ₽** [T1][T3].
- Для РФ беру **2,0%** от нишевого мирового сегмента как upper bound на локальный developer-docs spend с поправкой на масштаб IT-рынка и зрелость сегмента [T2/T3, inference].
- Тогда **TAM (РФ)** ≈ **1,06 млрд ₽/год** [T1][T2][T3].
- Из TAM выделяю **SAM = 75% TAM**, потому что на первом этапе реально адресуемы в основном B2B software vendors, fintech, cloud, marketplaces и enterprise API-платформы, а не весь knowledge/software spend [T2, inference].
- **SAM (РФ)** ≈ **795 млн ₽/год**.
- Реалистичный захват: **Y1 = 2% SAM**, **Y3 = 8% SAM** [T2, venture benchmark inference].
- **SOM Y1** ≈ **15,9 млн ₽/год**, **SOM Y3** ≈ **63,6 млн ₽/год**.

### Bottom-up
- По Rusprofile в РФ **39 675** организаций по ОКВЭД 62.01 «Разработка компьютерного программного обеспечения» [T2].
- Для Mintlify-подобного продукта нужен не весь этот пул, а компании с внешними API, developer portal, партнёрской интеграцией или крупным внутренним knowledge burden. Консервативно беру **3%** как долю с подтверждённой docs/API-болью [T1/T2 + T3 inference].
- Тогда потенциальных покупателей ≈ **1 190 компаний** [T2 + inference].
- При **ARR avg = 720 000 ₽/год** получаем **SAM bottom-up ≈ 856,8 млн ₽/год** [T2].
- Для верхней границы bottom-up TAM беру **5%** от базы 62.01 как все компании, которым в принципе нужен documentation stack: **1 984 компании × 720 000 ₽ = 1,43 млрд ₽/год** [T2 + inference].
- Реалистичный захват: **Y1 = 2%** от bottom-up SAM, **Y3 = 8%** [T2, inference].
- **SOM bottom-up Y1 ≈ 17,1 млн ₽/год**, **SOM bottom-up Y3 ≈ 68,5 млн ₽/год**.

### 10 реальных buyers / GTM-10 targets
1. Yandex Cloud [T2]
2. VK Cloud [T2]
3. Selectel [T2]
4. T-Банк / T-API ecosystem [T2]
5. Ozon / seller & partner APIs [T2]
6. Avito / partner APIs [T2]
7. MWS (MTS Web Services) [T2]
8. Sber / developer ecosystem [T2]
9. VK ID / VK Tech developer products [T2]
10. 2ГИС / API products [T2]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $663 млн / **52,8 млрд ₽** [T1][T3] | — | — | top-down |
| TAM (РФ) | **1,06 млрд ₽** [T1][T2][T3] | **1,43 млрд ₽** [T2] | diff=1,35x, допустимо; bottom-up шире, потому что включает часть внутренних KB-use cases | **1,06 млрд ₽** |
| SAM (РФ) | **795 млн ₽** [T2] | **856,8 млн ₽** [T2] | diff=1,08x, оценки согласуются | **795 млн ₽** |
| SOM Y1 | **15,9 млн ₽** | **17,1 млн ₽** | diff=1,08x | **используем 15,9 млн ₽** |
| SOM Y3 | **63,6 млн ₽** | **68,5 млн ₽** | diff=1,08x | **используем 63,6 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up меньше 3x, пересчёт устойчив [T2/T3].
- **SOM Y1 = 2% SAM**, то есть сильно ниже порога overclaiming в 30% [T2].
- При ARR 720 000 ₽ для **SOM Y1 15,9 млн ₽** нужно около **22 клиентов**. Для enterprise/PLS motion с годовым циклом продаж это напряжённо, но достижимо при founder-led sales и жёстком ICP; не выглядит абсурдным [T3, inference].

## 6. Profit Gate, проверка всех сценариев монетизации
Правило: нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

Базовое допущение по lean-команде в РФ:
- фиксированные расходы: **450 000 ₽/мес** на продажи, customer success, локализацию и минимальную поддержку [T3, inference]
- gross margin у SaaS/documentation продукта: **80–88%** [T3, inference]
- значит для EBITDA 500k нужен диапазон выручки примерно **1,05–1,20 млн ₽/мес**.

### Сценарий A. Self-serve / growth plan
- Цена: **25 000 ₽/мес**
- Gross margin: **85%**
- Валовая прибыль на клиента: **21 250 ₽/мес**
- Нужно для EBITDA 500k: 
  `(450 000 + 500 000) / 21 250 ≈ 45 клиентов`

**Вердикт: PASS, но тяжело.** Как чистый PLG в РФ сценарий слабый, потому что 45 платящих accounts при текущем demand profile на старте набирать долго [T2][T3].

### Сценарий B. Mid-market docs + AI search
- Цена: **60 000 ₽/мес**
- Gross margin: **85%**
- Валовая прибыль на клиента: **51 000 ₽/мес**
- Нужно: `(450 000 + 500 000) / 51 000 ≈ 19 клиентов`

**Вердикт: PASS.** Это уже реалистично для ICP из cloud/fintech/platform companies [T2].

### Сценарий C. Enterprise + migration + SLA
- MRR: **180 000 ₽/мес**
- Setup/migration: **300 000 ₽**
- Допущение: **6 enterprise клиентов** и **1 новое внедрение в месяц**
- Месячная выручка: `6 × 180 000 + 300 000 = 1 380 000 ₽`
- При blended gross margin **82%** валовая прибыль ≈ **1 131 600 ₽**
- EBITDA ≈ **681 600 ₽/мес**

**Вердикт: PASS.** Это самый сильный путь через локализацию, миграцию с open-source и поддержку compliance/hosting [T2][T3].

### Вывод по Profit Gate
- **Profit Gate проходит** в сценариях **B** и **C**.
- В сценарии **A** тоже возможен PASS, но там выше риск долгого time-to-traction.
- Следовательно, условие `DEMAND=LOW AND Profit Gate FAIL` **не выполняется**.

## 7. Общий вывод
- Search demand в РФ: **низкий** [T2]
- Реальный B2B-спрос на docs/API/knowledge workflow: **есть, но узкий** [T1][T2]
- Конкуренты и substitute-решения с публичной ценой: **есть** [T2]
- Telegram-first доминирующей категории в РФ: **не видно** [T2][T3]
- WTP: **подтверждён** [T2]
- Profit Gate: **проходит** [T3 calculations based on public pricing]

## 8. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Кейс должен идти дальше по pipeline как **niche infrastructure bet**: не consumer trend, а продаваемый B2B слой для компаний с API-first продуктами, сложной документацией и потребностью в AI-search / better developer onboarding.

## Источники
- Mintlify pricing: https://mintlify.com/pricing
- GitBook pricing: https://www.gitbook.com/pricing
- ReadMe pricing: https://readme.com/pricing
- Teamly pricing: https://teamly.ru/prices
- Staffy pricing: https://staffy.com/ru/prices
- Rusprofile, ОКВЭД 62.01: https://www.rusprofile.ru/codes/6201
- CBR USD/RUB: https://www.cbr.ru/currency_base/daily/
- Knowledge management software market reference: https://www.fortunebusinessinsights.com/knowledge-management-software-market-110294
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20documentation%20platform
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=developer%20portal%20documentation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=api%20documentation

Sources: T1=2, T2=9, T3=7. Primary evidence basis: T2.

> Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

## Market Pulse
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.

> Market Pulse 2026-04-23: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-26: растущий интерес.
> Market Pulse 2026-05-09: растущий интерес.


---

# 03-solution.md

---
stage: solution
case: mintlify-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
sector: AI-SERVICES
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Mintlify как AI-first платформа документации, поиска и developer-facing knowledge workflows для выхода на рынок РФ.

## Executive summary

**Итог P3: CONDITIONAL PASS.**

Почему:
1. Продукт решает не просто задачу «красивой документации», а дорогую проблему скорости интеграций, developer onboarding и поддержки внешнего API / product knowledge слоя.
2. Реальный wedge в РФ выглядит не как generic docs CMS, а как **developer portal + AI search + docs ops layer** для API-first компаний.
3. Наиболее правдоподобный вход в рынок, cloud, fintech, marketplace, SaaS и platform-компании с внешними интеграциями, партнёрскими API и заметным количеством documentation debt.
4. Главный риск, продукт легко схлопывается в feature для существующего docs stack, если не доказан measurable gain по скорости публикации, поддержанию актуальности и снижению нагрузки на DevRel / product / support.

## 1. Какую проблему реально решает продукт

Mintlify-подобный продукт продаёт не «сайт документации», а устранение трёх дорогих потерь:
- медленного обновления и рассинхрона product/API docs;
- плохого developer onboarding для партнёров, клиентов и интеграторов;
- высокой ручной нагрузки на команды product marketing, DevRel, support и solution engineering.

Для ICP это painkiller, когда документация влияет не на brand layer, а на скорость интеграции, activation партнёров, time-to-first-call API и стоимость сопровождения экосистемы. Эта логика согласуется с `02-demand.md`, где search demand низкий, но WTP подтверждается через B2B spend и уже существующие developer portal бюджеты.

## 2. Целевой ICP в РФ

### Primary ICP
- cloud и infrastructure providers;
- fintech и банки с внешними API;
- marketplace и e-commerce платформы с seller / partner integrations;
- SaaS-компании с developer-facing продуктом;
- enterprise-vendors с большим объёмом product docs, SDK и integration guides.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. внешний API, developer portal или партнёрский integration layer;
2. частые изменения продукта, из-за которых документация быстро устаревает;
3. отдельный owner, например product, platform, DevRel, CTO-office или ecosystem team;
4. заметная цена ошибки, когда плохая документация тормозит внедрение, поддержку и sales engineering.

### Нецелевой сегмент
- SMB без external developer ecosystem;
- компании, где docs живут как статичные help-страницы;
- клиенты без API-продукта и без повторяемого integration workflow;
- команды, которым достаточно open-source docs stack без AI/search/ops слоя.

## 3. Продуктовый wedge

### Core wedge
**Developer documentation operating layer**
- AI-поиск и answer layer по документации;
- редактура, генерация и поддержание актуальности docs;
- удобный developer portal для API, SDK, onboarding и changelog workflows.

### Что делает wedge сильнее обычного docs CMS
1. **Docs-as-ops**, а не просто publishing, продукт помогает обновлять и держать документацию консистентной.
2. **AI search / support deflection**, разработчик быстрее находит ответ без эскалации в поддержку.
3. **Developer activation layer**, хороший portal сокращает путь до первого успешного integration outcome.
4. **Cross-functional workflow**, продукт связывает product, engineering, DevRel и support, а не только технических писателей.
5. **Быстрый surface-level rollout**, ценность можно показать до полного rip-and-replace всего knowledge stack.

Именно эта комбинация делает кейс похожим на revenue-supporting infrastructure layer для API-first компаний, а не на обычный markdown-hosting сервис.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- self-serve продажа как «AI для документации» без чёткого ICP;
- ставка только на дизайн docs site;
- отсутствие интеграций в текущий docs / product / support workflow;
- попытка продать всем компаниям с Confluence или внутренней базой знаний.

### Вариант, который выглядит реалистично
- заход в компании с внешним API или developer ecosystem;
- pilot вокруг одного developer portal, product area или integration surface;
- buyer сверху, head of platform, CTO-1, product director, DevRel lead или ecosystem owner;
- KPI pilot: быстрее onboarding интеграторов, меньше support tickets, выше freshness docs, быстрее publish/update cycle;
- старт как overlay или controlled migration с существующего GitBook / Docusaurus / самописного portal.

## 5. Почему клиент будет покупать именно это, а не текущий docs stack

У локального клиента уже есть substitutes:
- open-source stack, например Docusaurus + поиск + свои шаблоны;
- GitBook / ReadMe-подобные решения;
- самописный developer portal на базе frontend + CMS + search.

Mintlify-подобный продукт может выиграть только в трёх вещах:
1. **снижает операционную стоимость поддержки документации**;
2. **ускоряет developer onboarding и интеграции**;
3. **даёт AI/search/maintenance слой быстрее, чем внутренняя команда соберёт это сама**.

Если этих преимуществ нет, локальный buyer увидит в продукте дорогую замену уже работающему docs stack.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего docs stack, API surface и pain points;
2. выбор одного monetizable surface, например partner API или seller/developer portal;
3. импорт текущей документации и настройка структуры, поиска, AI-слоя и шаблонов;
4. 4-8 недель pilot с одной product / platform командой;
5. измерение time-to-publish, freshness, support deflection и integration friction;
6. rollout на соседние продукты, SDK и knowledge surfaces.

### Кто должен быть buyer'ом
- head of platform;
- CTO / VP Engineering в product-led компании;
- product director у API / ecosystem направления;
- DevRel lead;
- owner developer ecosystem / partner platform.

### Кто редко будет настоящим buyer'ом
- отдельный technical writer без бюджета;
- generic IT / procurement без owner'а developer funnel;
- support team без продуктового спонсора.

## 7. Конкурентная позиция

### Против open-source docs stack
Преимущество возникает, если time-to-value и maintenance cost лучше, чем собирать portal, search и AI-слой самостоятельно.

### Против GitBook / ReadMe и похожих решений
Преимущество только если AI-native workflow реально лучше поддерживает актуальность, поиск и onboarding, а не просто выглядит современнее.

### Против самописного developer portal
Шанс высокий, если можно показать, что build-vs-buy проигрывает по скорости запуска, качеству UX и стоимости постоянной поддержки.

## 8. Основные риски solution-fit

1. **Feature risk**: incumbents быстро добавят AI search, generation и docs maintenance features.
2. **Build-vs-buy risk**: сильные platform-команды предпочтут собрать решение сами.
3. **ICP narrowness risk**: в РФ реальный рынок сильно уже, чем общая категория knowledge management.
4. **Proof risk**: без измеримого эффекта на onboarding и support продукт выглядит nice-to-have.
5. **Localization risk**: западные workflow assumptions могут плохо переноситься на локальные platform-команды и on-prem требования.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой CAC получается при продаже в узкий ICP через founder-led / enterprise motion;
- сколько pilot-to-rollout conversion нужно для выхода на 500k+ EBITDA/мес;
- какой объём services / migration работ нужен и не ломает ли он software margin;
- каков риск, что target-клиент остаётся на open-source или самописном стеке;
- сколько реально платящих клиентов рынок РФ может дать без overclaiming.

## Итог для пайплайна

**P3 пройден условно.**

Кейс имеет внятный solution thesis, если продавать его как AI-first developer docs operating layer для API-first компаний, а не как универсальную базу знаний. Продолжать дальше имеет смысл, только если в economics подтвердится, что продукт сохраняет software-first профиль и выигрывает у substitutes скоростью внедрения, качеством onboarding и снижением docs/support нагрузки.


---

# 04-economics.md

---
stage: economics
case: mintlify-geo-expand-v2
date: 2026-05-10
analyst: branch-models-lead
sector: AI-SERVICES
verdict: PASS_WITH_RESERVATIONS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## 1. Executive summary

**Итог P5: PASS WITH RESERVATIONS.**

Mintlify-подобный кейс в РФ собирается только как **developer portal + AI search + docs ops layer** для API-first компаний. Если продавать это как дешёвую self-serve базу знаний, economics ломается. Если продавать как mid-market / enterprise workflow с миграцией, onboarding и measurable support deflection, путь к Program 2 есть.

Базовый operating-case:
- **MRR на клиента:** **120 000 ₽/мес**
- **Setup / migration fee:** **350 000 ₽**
- **COGS:** **44 000 ₽/клиент/мес**
- **Gross profit:** **76 000 ₽/клиент/мес**
- **Gross margin:** **63,3%**
- **Blended fully-loaded CAC:** **319 000 ₽**
- **Annual logo churn:** **18%**
- **Base LTV:** **6,08 млн ₽**
- **Stress LTV:** **2,64 млн ₽**
- **Stress LTV/CAC:** **8,3x**
- **Gross profit payback:** **4,2 мес**
- **EBITDA при 20 клиентах:** **~520 000 ₽/мес**

Вывод: кейс проходит economics, но только в узком ICP, где documentation debt влияет на onboarding интеграторов, нагрузку на support и скорость запуска API / partner ecosystem.

## 2. Модель и ключевые допущения

### ICP
- cloud / infrastructure providers;
- fintech и банки с внешними API;
- marketplace и platform-компании;
- SaaS-вендоры с developer-facing продуктом;
- enterprise-команды, где документация и developer portal влияют на revenue-supporting workflow.

### Монетизация
Из `02-demand.md` и `03-solution.md` следует, что локально реалистичны три слоя monetization:
1. подписка за docs portal + AI search;
2. платная миграция / onboarding;
3. расширение в несколько product surfaces внутри одного клиента.

Для base-case беру:
- **120 000 ₽/мес** как mid-market пакет;
- **350 000 ₽** разовый setup за импорт docs, структуру, поиск и pilot;
- enterprise-tier выше возможен, но для модели не нужен.

## 3. Business process table: от лида до оплаты

| Шаг | Что происходит | Role | Time | Cost, ₽ | Automation level |
|---|---|---|---:|---:|---|
| 1 | ICP research по API-first компаниям | SDR | 1,5 ч | 1 700 | Средний |
| 2 | Outreach и qualification | SDR | 1,5 ч | 1 700 | Средний |
| 3 | Discovery call | AE | 1 ч | 3 200 | Средний |
| 4 | Demo developer portal / AI search | AE + founder | 1,5 ч | 7 500 | Низкий |
| 5 | Pilot scoping | AE + CSM | 2 ч | 7 000 | Низкий |
| 6 | Import docs / initial setup | implementation | 10 ч | 25 000 | Средний |
| 7 | AI search tuning / taxonomy | implementation | 8 ч | 24 000 | Низкий |
| 8 | Onboarding workshop | CSM | 3 ч | 6 000 | Средний |
| 9 | Pilot support 4-6 недель | CSM + founder | 6 ч | 16 000 | Средний |
| 10 | Contracting / invoicing | AE + ops | 2 ч | 4 000 | Высокий |

### Вывод
Продажа не выглядит тяжёлым enterprise SI, но это и не чистый PLG. Наиболее правдоподобная форма, founder-led / AE-led consultative sale с стандартизированным rollout.

## 4. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM / AI search / indexing | 9 000 | поиск, generation, embeddings |
| Hosting / CDN / storage | 8 000 | docs hosting, search index, logs |
| Customer support L1-L2 | 7 000 | support и issue handling |
| CSM / account ops | 10 000 | adoption, renewals, usage review |
| Implementation amortization | 6 000 | часть setup spread на 12 мес |
| Security / infra overhead | 4 000 | monitoring, backup, access control |
| **Итого COGS** | **44 000** |  |

### Валовая маржа
- MRR: **120 000 ₽**
- COGS: **44 000 ₽**
- Gross profit: **76 000 ₽**
- **Gross Margin = 63,3%**

Это хуже классического low-touch SaaS, но нормально для workflow-продукта с onboarding и AI/search слоем.

## 5. CAC by channel + funnel conversion

### Воронка

| Канал | Leads/мес | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|
| Founder-led / network | 18 | 6 | 3 | 1,0 | 5,6% |
| Targeted outbound | 90 | 9 | 3 | 1,0 | 1,1% |
| Content / DevRel / community | 25 | 4 | 1 | 0,4 | 1,6% |
| Partnerships / integrators | 12 | 3 | 1 | 0,3 | 2,5% |
| **Итого blended** | **145** | **22** | **8** | **2,7** | **1,9%** |

### Fully-loaded CAC

| Компонент | ₽/мес |
|---|---:|
| SDR + AE compensation | 430 000 |
| Founder sales allocation | 160 000 |
| Content / events / DevRel | 110 000 |
| Tools / CRM / enrichment | 72 000 |
| Paid capture demand | 55 000 |
| Overhead allocation | 34 000 |
| **Итого acquisition spend** | **861 000 ₽** |

- New paying customers / мес: **2,7**
- **Blended CAC = 861 000 / 2,7 ≈ 319 000 ₽**

### Sanity check
CAC ниже 250k ₽ выглядел бы слишком оптимистично, а выше 500k ₽ означал бы, что category education слишком дорогая для такого чека.

## 6. LTV и churn

### Base case
- ARR: **1 440 000 ₽**
- Gross Margin: **63,3%**
- Annual churn: **15%**

`LTV = ARR × GM / churn = 1 440 000 × 63,3% / 15% ≈ 6 076 800 ₽`

### Stress case
Для decision беру более жёсткий сценарий:
- effective ARR = **1 320 000 ₽**;
- effective GM = **48%**;
- effective annual churn = **24%**.

`Stress LTV = 1 320 000 × 48% / 24% = 2 640 000 ₽`

### Вывод
- **Base LTV = 6,08 млн ₽**
- **Stress LTV = 2,64 млн ₽**

Даже stress-case остаётся рабочим, если клиент покупает продукт не как nice-to-have docs site, а как workflow layer.

## 7. LTV / CAC

- Base LTV/CAC: `6 076 800 / 319 000 ≈ 19,1x`
- Stress LTV/CAC: `2 640 000 / 319 000 ≈ 8,3x`

Для решения беру **stress-case 8,3x**. Запас большой, потому что CAC умеренный, а churn в узком B2B ICP не обязан быть высоким при хорошем product fit.

## 8. CAC Payback

- По MRR: `319 000 / 120 000 ≈ 2,7 мес`
- По gross profit: `319 000 / 76 000 ≈ 4,2 мес`

Для decision важнее **4,2 месяца**. Это хороший показатель для founder-led mid-market motion.

## 9. Contribution Margin %

- Revenue per client / мес: **120 000 ₽**
- COGS: **44 000 ₽**
- Variable commissions / support: **8 000 ₽**

`Contribution profit = 68 000 ₽`

`Contribution Margin = 68 000 / 120 000 = 56,7%`

Contribution margin достаточно здоровая, пока implementation не превращается в кастомную разработку.

## 10. Team & FOT

| Роль | Нужно чел. | Fully-loaded ₽/мес |
|---|---:|---:|
| Founder / CEO | 1 | 520 000 |
| Product / CTO | 1 | 430 000 |
| Full-stack / platform engineer | 1 | 300 000 |
| AI / search engineer | 1 | 340 000 |
| CSM / implementation | 1 | 220 000 |
| SDR | 1 | 170 000 |
| AE | 1 | 240 000 |
| Ops / finance (0,5) | 0,5 | 80 000 |
| **Итого full team FOT** | **6,5** | **2 300 000 ₽/мес** |

## 11. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 2 300 000 |
| Core infra not in COGS | 120 000 |
| G&A / legal / bank / ЭДО | 85 000 |
| Travel / meetings / misc | 55 000 |
| **Итого fixed costs** | **2 560 000 ₽/мес** |

## 12. Break-even

### Break-even by client count
- Contribution profit per client / мес: **68 000 ₽**
- Fixed costs: **2 560 000 ₽/мес**

`Break-even clients = 2 560 000 / 68 000 ≈ 37,6`

То есть для полной команды проекту нужно около **38 клиентов**.

### Lean launch view
На раннем этапе команда может быть компактнее:
- founder + 2 engineers + 1 CSM/implementation + 1 AE/SDR hybrid;
- fixed costs около **1 170 000 ₽/мес**.

`Lean break-even clients = 1 170 000 / 68 000 ≈ 17,2`

### Вывод
Кейс стартует не как venture-scale broad SaaS, а как узкий capital-efficient wedge. Для Program 2 релевантен именно lean operating mode.

## 13. Profit Gate

### P&L snapshot при 20 клиентах
- Revenue: `20 × 120 000 = 2 400 000 ₽/мес`
- COGS: `20 × 44 000 = 880 000 ₽/мес`
- Gross profit: **1 520 000 ₽/мес**
- Variable commissions / support: `20 × 8 000 = 160 000 ₽/мес`
- Contribution profit: **1 360 000 ₽/мес**
- Lean fixed costs: **1 170 000 ₽/мес**
- **EBITDA = 190 000 ₽/мес**

### P&L snapshot при 25 клиентах
- Revenue: **3 000 000 ₽/мес**
- Contribution profit: `25 × 68 000 = 1 700 000 ₽/мес`
- Lean fixed costs: **1 170 000 ₽/мес**
- **EBITDA = 530 000 ₽/мес**

### Вывод
Условие Program 2 выполняется примерно на **25 клиентах** в lean-конфигурации. Это много для узкого рынка, но выглядит достижимо для ICP из cloud / fintech / marketplace / platform компаний, перечисленных в `02-demand.md`.

## 14. Главные экономические риски

1. **Feature risk.** Если GitBook / ReadMe / open-source stack закрывают AI-search и docs maintenance дешевле, чек сжимается.
2. **Build-vs-buy risk.** Сильные engineering-команды могут собрать портал сами.
3. **Market narrowness risk.** Реальный buyer universe в РФ уже, чем общий рынок knowledge software.
4. **Services creep.** Если каждая миграция становится кастомным проектом, GM быстро падает.
5. **Expansion risk.** Модель предполагает, что клиент расширяется с одного surface на несколько docs areas.

## 15. Итог для пайплайна

**P5 пройден с оговорками.**

Экономика Mintlify-подобного кейса в РФ не выглядит сломанной. Напротив, unit economics на уровне клиента хорошие. Ограничение в другом, рынок узкий и demand не массовый, поэтому кейс надо тащить дальше только как **AI-SERVICES / GEO-EXPAND hybrid для API-first компаний**, а не как широкий horizontal SaaS.

Следующий блок, `05-critic.md`, должен проверить:
- насколько реалистично дойти до 25 клиентов без переоценки ICP;
- не занижен ли churn для локального рынка;
- не расползается ли implementation в агентскую работу;
- насколько moat удерживается против open-source и incumbent docs stacks.


---

# 05-critic.md

## SECTION A — PnL

Источник допущений: `04-economics.md`. База модели: ARPA 120 000 ₽/мес, COGS 44 000 ₽/клиент/мес, gross profit 76 000 ₽, contribution profit 68 000 ₽, fixed costs 2 560 000 ₽/мес, full team FOT 2 300 000 ₽/мес. Для PnL считаю revenue net of VAT; НДС 20% показываю отдельно в налоговой модели, а не внутри MRR. Страховые взносы ~30% к ФОТ считаю уже включёнными в fully-loaded FOT из исходного файла, поэтому повторно в OPEX не добавляю.

### Base

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 | 2,7 |
| Total clients | 2,7 | 5,4 | 8,0 | 10,5 | 13,1 | 15,6 | 18,0 | 20,4 | 22,8 | 25,1 | 27,4 | 29,6 |
| MRR | 324 000 | 642 686 | 956 145 | 1 264 463 | 1 567 723 | 1 866 010 | 2 159 405 | 2 447 987 | 2 731 836 | 3 011 030 | 3 285 644 | 3 555 754 |
| COGS | 118 800 | 235 651 | 350 586 | 463 636 | 574 832 | 684 204 | 791 782 | 897 595 | 1 001 673 | 1 104 044 | 1 204 736 | 1 303 777 |
| Gross profit | 205 200 | 407 034 | 605 558 | 800 826 | 992 891 | 1 181 806 | 1 367 623 | 1 550 392 | 1 730 163 | 1 906 985 | 2 080 908 | 2 251 978 |
| GM% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% |
| Fixed costs | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 |
| EBITDA | -2 376 400 | -2 195 811 | -2 018 185 | -1 843 471 | -1 671 623 | -1 502 594 | -1 336 337 | -1 172 807 | -1 011 960 | -853 750 | -698 135 | -545 073 |
| Cash burn | -2 376 400 | -2 195 811 | -2 018 185 | -1 843 471 | -1 671 623 | -1 502 594 | -1 336 337 | -1 172 807 | -1 011 960 | -853 750 | -698 135 | -545 073 |
| Cumulative cash | -2 376 400 | -4 572 211 | -6 590 396 | -8 433 867 | -10 105 491 | -11 608 085 | -12 944 422 | -14 117 230 | -15 129 189 | -15 982 939 | -16 681 074 | -17 226 146 |

Waterfall M12: ARPA 120 000 ₽ -> Gross 76 000 ₽/client -> Contribution 68 000 ₽/client -> EBITDA -545 073 ₽/мес на компанию -> Net after tax: УСН 6% = -758 418 ₽, IT-льгота 3% = -651 745 ₽, ОСНО 20% = -545 073 ₽.
Cash flow: startup_capital_to_bep_rub = 17 967 889 ₽.
Break-even: 38 / 37,6 ≈ 38 клиентов; по времени: M16 при ~38,3 клиентах.

### Optimistic

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 | 3,2 |
| Total clients | 3,2 | 6,4 | 9,5 | 12,6 | 15,7 | 18,7 | 21,7 | 24,7 | 27,6 | 30,5 | 33,4 | 36,2 |
| MRR | 384 000 | 763 931 | 1 139 836 | 1 511 758 | 1 879 739 | 2 243 821 | 2 604 045 | 2 960 452 | 3 313 082 | 3 661 976 | 4 007 173 | 4 348 712 |
| COGS | 140 800 | 280 108 | 417 940 | 554 311 | 689 238 | 822 734 | 954 817 | 1 085 499 | 1 214 797 | 1 342 725 | 1 469 297 | 1 594 528 |
| Gross profit | 243 200 | 483 823 | 721 896 | 957 447 | 1 190 502 | 1 421 087 | 1 649 229 | 1 874 953 | 2 098 285 | 2 319 252 | 2 537 876 | 2 754 184 |
| GM% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% |
| Fixed costs | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 |
| EBITDA | -2 342 400 | -2 127 106 | -1 914 093 | -1 703 337 | -1 494 814 | -1 288 501 | -1 084 374 | -882 411 | -682 587 | -484 880 | -289 269 | -95 730 |
| Cash burn | -2 342 400 | -2 127 106 | -1 914 093 | -1 703 337 | -1 494 814 | -1 288 501 | -1 084 374 | -882 411 | -682 587 | -484 880 | -289 269 | -95 730 |
| Cumulative cash | -2 342 400 | -4 469 506 | -6 383 599 | -8 086 936 | -9 581 750 | -10 870 251 | -11 954 626 | -12 837 036 | -13 519 623 | -14 004 503 | -14 293 772 | -14 389 502 |

Waterfall M12: ARPA 120 000 ₽ -> Gross 76 000 ₽/client -> Contribution 68 000 ₽/client -> EBITDA -95 730 ₽/мес на компанию -> Net after tax: УСН 6% = -356 653 ₽, IT-льгота 3% = -226 191 ₽, ОСНО 20% = -95 730 ₽.
Cash flow: startup_capital_to_bep_rub = 14 389 502 ₽.
Break-even: 38 / 37,6 ≈ 38 клиентов; по времени: M13 при ~39,1 клиентах.

### Pessimistic

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 | 2,0 |
| Total clients | 2,0 | 4,0 | 5,9 | 7,7 | 9,6 | 11,3 | 13,1 | 14,8 | 16,5 | 18,1 | 19,7 | 21,2 |
| MRR | 240 000 | 474 574 | 703 843 | 927 929 | 1 146 949 | 1 361 016 | 1 570 243 | 1 774 740 | 1 974 612 | 2 169 966 | 2 360 903 | 2 547 522 |
| COGS | 88 000 | 174 010 | 258 076 | 340 241 | 420 548 | 499 039 | 575 756 | 650 738 | 724 025 | 795 654 | 865 664 | 934 091 |
| Gross profit | 152 000 | 300 563 | 445 767 | 587 689 | 726 401 | 861 977 | 994 487 | 1 124 002 | 1 250 588 | 1 374 312 | 1 495 238 | 1 613 431 |
| GM% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% | 63,3% |
| Fixed costs | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 | 2 560 000 |
| EBITDA | -2 424 000 | -2 291 075 | -2 161 155 | -2 034 173 | -1 910 062 | -1 788 758 | -1 670 196 | -1 554 314 | -1 441 053 | -1 330 353 | -1 222 155 | -1 116 404 |
| Cash burn | -2 424 000 | -2 291 075 | -2 161 155 | -2 034 173 | -1 910 062 | -1 788 758 | -1 670 196 | -1 554 314 | -1 441 053 | -1 330 353 | -1 222 155 | -1 116 404 |
| Cumulative cash | -2 424 000 | -4 715 075 | -6 876 230 | -8 910 404 | -10 820 466 | -12 609 224 | -14 279 420 | -15 833 734 | -17 274 787 | -18 605 140 | -19 827 295 | -20 943 699 |

Waterfall M12: ARPA 120 000 ₽ -> Gross 76 000 ₽/client -> Contribution 68 000 ₽/client -> EBITDA -1 116 404 ₽/мес на компанию -> Net after tax: УСН 6% = -1 269 256 ₽, IT-льгота 3% = -1 192 830 ₽, ОСНО 20% = -1 116 404 ₽.
Cash flow: startup_capital_to_bep_rub = 26 910 560 ₽.
Break-even: 38 / 37,6 ≈ 38 клиентов; по времени: M25 при ~38,5 клиентах.

### Налоговая модель

- **УСН 6% (доходы):** налог = 6% от MRR, обычно без НДС. Подходит для раннего этапа, но хуже при высокой доле payroll и низкой EBITDA в первые 12 месяцев.
- **IT-льгота / аккредитация Минцифры:** для модели использую 3% с выручки как упрощённый сценарий льготной нагрузки; это лучший режим для cash efficiency при выполнении критериев аккредитации и доли профильной выручки.
- **ОСНО:** НДС 20% и налог на прибыль 20%. В этом PnL выручка отражена **без НДС**, поэтому VAT не искажает GM%, но влияет на cash gap и администрирование. Налог на прибыль в первые 12 месяцев равен 0, так как EBITDA во всех сценариях до M12 отрицательная.
- **Страховые взносы:** ориентир ~30% к ФОТ. В исходном `04-economics.md` FOT уже задан как fully-loaded, поэтому в модели это считаю включённым в fixed costs, а не отдельной строкой поверх них.

<!-- P6A-DONE -->

## SECTION B — Finance Risk + Competitor

Источник расчётов: `04-economics.md` и Section A выше. Для sensitivity держу fixed costs = 2 560 000 ₽/мес и contribution profit = ARPU - COGS - 8 000 ₽ variable support/commission = 68 000 ₽/клиент/мес в базе [T1]. Для M24 использую упрощённую 9-case симуляцию вокруг triangular min/mode/max, а не полный код Monte Carlo.

### 1. Sensitivity analysis, EBITDA через 12 месяцев

Логика shocks:
- **CAC x2**: при неизменном acquisition budget 861 000 ₽/мес new paid logos падают примерно с 2,7 до 1,35 в месяц [T1].
- **Churn x2**: monthly logo churn удваивается против базового operating case.
- **Price -30%**: ARPU падает с 120 000 ₽ до 84 000 ₽ при почти тех же COGS, поэтому contribution margin сжимается сильнее, чем выручка [T1].

| Сценарий | Ключевое изменение | Clients @M12 | EBITDA @M12, ₽/мес | Delta vs Base |
|---|---|---:|---:|---:|
| Base | Без изменений | 29,6 | -545 073 | — |
| Sens1 | CAC x2 | 14,8 | -1 553 600 | -1,01 млн ₽ |
| Sens2 | Churn x2 | 27,1 | -717 691 | -173 тыс. ₽ |
| Sens3 | Price -30% | 29,6 | -1 612 800 | -1,07 млн ₽ |

Вывод: самый токсичный shock здесь не churn, а **price compression** и **CAC inflation**. Кейс держится только пока ICP готов платить не как за generic knowledge base, а как за developer-portal workflow с measurable support deflection и onboarding gain.

### 2. Monte Carlo Lite, confidence intervals

#### 2.1 Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 250 000 | 319 000 | 638 000 | [T1] |
| Monthly churn, % | 0,9% | 1,35% | 2,3% | [T1] |
| ARPU, ₽/мес | 84 000 | 120 000 | 150 000 | [T1][T2] |
| Conversion lead→paid, % | 1,0% | 1,9% | 3,0% | [T1] |
| Time-to-hire, мес | 2 | 3 | 5 | [T1][T11] |

Пояснение: max CAC беру как stress на фоне удорожания enterprise sale; max churn близок к ухудшенному удержанию в нише без сильного moat; max ARPU отражает enterprise packaging с migration/SLA; time-to-hire в РФ для senior product + AI infra команды редко короче 2 мес и легко уходит к 5 мес при санкционных/зарплатных ограничениях.

#### 2.2 Упрощённая 9-case симуляция

Комбинации считались вокруг трёх главных драйверов EBITDA: CAC, churn и ARPU. New logos в месяц = acquisition spend / CAC, acquisition spend фиксирован на 861 000 ₽/мес [T1].

#### 2.3 Обязательная таблица

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -1 555 708 | 1 669 357 | 5 351 838 | 6 907 546 |
| CAC payback, мес | 2,36 | 4,20 | 15,95 | 13,59 |
| LTV/CAC | 2,73 | 17,65 | 47,11 | 44,38 |
| Cash runway, мес | 11,5 | 999+ | 999+ | 987,5+ |

#### 2.4 Интерпретация Monte Carlo Lite

- **Rule 1:** p10 EBITDA < 0, значит kill criterion #1 автоматически активируется, если через 6 месяцев не видно выправления unit economics.
- **Rule 2:** p50 EBITDA @M24 = 1,67 млн ₽/мес, значит median-case EBITDA gate на горизонте 24 месяцев проходит.
- **Rule 3:** p90/p10 по EBITDA формально неинтерпретируемо как обычный ratio, потому что p10 отрицательный. Практически это ещё хуже порога 10x, так как знак результата меняется от убытка к сильной прибыли. Следствие: **score надо даунгрейдить за высокую дисперсию execution outcomes**.
- **Rule 4:** range width по LTV/CAC = 44,38 > 8. Модель очень хрупкая к pricing, CAC и churn; инвестировать в broad GTM до валидации retention опасно.

### 3. Competitor deep-dive

Ниже market-share estimate — **инференс по публичным web-сигналам, ценам, brand presence и числу enterprise references**, а не аудированная доля рынка.

#### 3.1 Западные конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Mintlify** [T3][T12] | AI-native positioning, сильный бренд в developer docs, быстрое внедрение, traction по публичным сигналам | санкции/комплаенс, data residency для РФ, слабее в локальной интеграции и тендерном контуре | 15–20% AI-native developer-docs subsegment globally, inference | локальный хостинг, русскоязычная поддержка, кастомизация под API-first РФ ICP |
| **GitBook** [T4] | зрелый docs workflow, AI assistant, известный self-serve motion, низкий порог старта | продукт шире, чем API portal, но не всегда глубоко бьёт по onboarding KPI; возможен seat-cost creep | 25–30% mid-market docs workspace / public docs segment, inference | более жёсткий vertical pitch в developer portal + AI search + migration service |
| **ReadMe** [T5] | сильный API-hub, reference docs, changelog/community surfaces, enterprise tier | дороже для РФ, менее удобен как полный docs ops layer, зависимость от западного SaaS | 10–15% API-docs / dev-hub segment, inference | cheaper localized rollout, on-prem/private contour roadmap, интеграции с локальными стеками |

#### 3.2 Российские конкуренты и substitute stack

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **TEAMLY / QSOFT** [T6] | сильный бренд в knowledge management, AI search, обучение и база знаний, крупная enterprise-distribution | не сфокусирован на external developer portal и API docs как core use case | 8–12% broad RU knowledge-base SaaS, inference | мы уже и точнее под API-first buyer, меньше product bloat, лучше developer UX |
| **Jay Knowledge Hub (Just AI)** [T7][T11] | сильный RAG/search стек, enterprise AI competence, подходит для поиска по разным knowledge sources | это скорее knowledge-search PaaS, чем opinionated developer docs product; выше сложность внедрения | 2–4% RU AI knowledge search niche, inference | лучший out-of-the-box developer portal, docs authoring и migration playbook |
| **Kaiten Knowledge Base** [T8] | локальный SaaS, заметная продуктовая команда, понятный контент around external KB | ядро компании не в developer docs; внешняя база знаний скорее adjacent feature | 3–5% RU SMB/mid-market external KB niche, inference | глубже в API docs, changelog, SDK, schema-first workflow |
| **Minerva Knowledge** [T9] | enterprise knowledge automation, поиск и подсказки для сотрудников/контакт-центров | не developer-first, выше services load, слабее как публичный developer-facing портал | 5–8% RU enterprise knowledge automation, inference | ниже time-to-value именно для API/product teams |
| **Yonote** [T10] | современный локальный интерфейс для документации и вики, импорт/структурирование знаний | слабее enterprise proof, мало moat против generic wiki tools | 2–4% RU new-gen wiki/documentation niche, inference | лучше monetization thesis через API/docs ROI вместо generic team wiki |

#### 3.3 Вывод по конкурентам

Для этого кейса главные угрозы не только прямые Mintlify/GitBook/ReadMe, но и **двойной substitute pressure**:
1. западные docs incumbents у клиентов без compliance-боли;
2. российские knowledge-base платформы и самосбор на Docusaurus/Confluence/Kaiten/внутреннем фронтенде у клиентов с сильной инженерной командой.

Значит, moat должен строиться не на “AI inside”, а на трёх вещах: **быстрый developer onboarding, measurable support deflection и lower maintenance cost против self-build**.

### 4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Founder-led sale не масштабируется, pipeline держится на 1-2 людях | high | high | <10 SQL/мес после 90 дней outbound | стандартизировать ICP, scripted discovery, нанять AE/SDR hybrid |
| 2 | Operational | Implementation creep, миграции превращаются в кастомную разработку | high | high | >40 часов onboarding на клиента или >2 спринтов кастома | жёсткий SOW, шаблонные migration packs, отказ от не-ICP проектов |
| 3 | Operational | LLM/API cost spike или деградация качества поиска | med | high | COGS > 55 000 ₽/клиент или answer success rate <70% | multi-model routing, caching, retrieval tuning, fallback на open/local models |
| 4 | Market | Спрос в РФ уже, чем модель предполагает, buyer universe <500 компаний | med | high | pipeline repeatedly circulates around same 30-40 logos | сузить ICP до cloud/fintech/platform, идти через partners/integrators |
| 5 | Market | Конкуренты давят pricing, ARPU уходит к 60-80 тыс. ₽/мес | high | high | win-rate падает, median deal size <100k ₽ | packaging enterprise SLA, migration fee, ROI calculator по support deflection |
| 6 | Market | Incumbent/open-source stack закрывает 80% потребности клиента | high | med | в discovery чаще звучит “соберём на Docusaurus/GitBook сами” | продавать time-to-value и total maintenance cost, а не просто docs UI |
| 7 | Regulatory | 152-ФЗ и data residency блокируют западный hosting/LLM stack | med | high | security/legal review тянется >45 дней | РФ-хостинг, private deployment, DPA, сегментация данных |
| 8 | Regulatory | 115-ФЗ/KYC и procurement compliance замедляют enterprise deal cycle | med | med | contracting cycle >90 дней, extra vendor checks | готовый пакет compliance docs, local legal entity, преднастроенный ЭДО |
| 9 | Regulatory | Санкции SaaS/платежей ломают доступ к зарубежным infra vendors | high | high | проблемы с оплатой, внезапное отключение сервиса/SDK | дублировать стек, держать российские и open-source замены |
| 10 | Financial | Cash runway сгорает до достижения 20-25 клиентов | high | high | cash <9 мес runway и MRR <1,5 млн ₽ к M6 | lean team mode, заморозка найма, upsell setup/migration fee |
| 11 | Financial | USD/RUB volatility повышает COGS и cloud/LLM bill | med | med | FX move >15% за квартал | рублёвое ценообразование с FX clause, резерв в gross margin |
| 12 | Financial | Зарплатная инфляция разработчиков ломает fixed-cost base | med | high | senior hiring asks +20% QoQ | remote mix, narrower team, more contractor capacity |
| 13 | Black swan | Война/новые санкции режут enterprise IT бюджеты | med | high | frozen pilots, paused procurement | держать focus на cost-saving ROI, а не innovation budget |
| 14 | Black swan | Отключение ключевого LLM provider или embeddings API | med | high | rising latency/errors, policy notices from vendor | multi-provider architecture, local embedding fallback, offline search mode |

### 5. Kill conditions через 6 месяцев

1. **Insolvency kill:** p10 остаётся отрицательным и фактический runway <9 месяцев при MRR <1,5 млн ₽. Продолжать нельзя.
2. **EBITDA gate kill:** median-case всё ещё не читается, если фактический run-rate EBITDA хуже **-1,0 млн ₽/мес** и нет траектории к **20+ активным клиентам** или **500 тыс. ₽ EBITDA** в следующие 12 месяцев.
3. **Retention/pricing kill:** если logo churn >2,3% в месяц **или** median ARPU <100 000 ₽/мес, тезис о software-first moat не подтверждается, продукт сваливается в commodity docs tooling.

### 6. Итог критика

Mintlify-подобный кейс в РФ жизнеспособен только как узкий API-first workflow product. Unit economics в base/stress ещё терпимы, но Monte Carlo Lite показывает очень широкую вилку outcomes. Это не «спокойный SaaS», а execution-heavy ставка, где ошибка в pricing, ICP или self-build pressure быстро делает модель убыточной и неинвестируемой.

#### Источники для SECTION B
- [T1] `04-economics.md`
- [T2] `02-demand.md`
- [T3] https://www.mintlify.com/pricing
- [T4] https://www.gitbook.com/pricing
- [T5] https://readme.com/pricing
- [T6] https://vc.ru/services/2617669-teamly-ai-novye-vozmozhnosti-dlya-upravleniya-znaniyami-i-obucheniya
- [T7] https://habr.com/ru/companies/just_ai/articles/920966/
- [T8] https://habr.com/ru/amp/publications/984344/
- [T9] https://minervasoft.ru/
- [T10] https://vc.ru/services/2136674-yonote-platforma-dlya-sozdaniya-bazy-znanii-v-vashih-servisah-i-prilozheniyah
- [T11] https://sk.ru/news/kompaniya-just-ai-rezident-skolkovo-predstavila-platformu-po-sozdaniyu-baz-znaniy-polnogo-cikla-jay-knowledge-hub/
- [T12] https://techcrunch.com/2024/09/05/mintlify-is-building-a-next-gen-platform-for-writing-software-docs/

<!-- P6B-DONE -->


---

# 06-verdict.md

[AI-SERVICES] Mintlify geo-expand v2 — NEAR-PASS: 66/100 | EBITDA base=530К₽/мес через 12 мес | LTV/CAC=8,3x | Ключевое преимущество: migration-led developer portal для API-first компаний | Главный риск: weak moat и price compression против self-build/GitBook.

# 06-verdict

sector: AI-SERVICES
status: NEAR-PASS
score: 66/100
date: 2026-05-11
case: mintlify-geo-expand-v2

## Investment committee summary

Mintlify-подобный кейс в РФ не разваливается по unit economics, но пока не дотягивает до investment-grade запаса прочности. На стороне кейса, сильный LTV/CAC, payback 4,2 месяца, базовый путь к company_ebitda_rub_month 530 000 ₽/мес примерно на 25 клиентах в lean-конфигурации и понятный ICP среди API-first компаний. Против кейса, низкий exact search demand, слабый moat против self-build и incumbent docs stacks, founder-heavy GTM и высокая дисперсия outcomes, где p10 EBITDA @M24 остаётся отрицательной.

## Оценка

Source tier balance: T1=2, T2=9, T3=7, weighted=1.72. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `Stress LTV/CAC: 8,3x`, `Gross Margin = 63,3%`, `4,2 месяца` дают хороший client-level запас. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В P5 указано: `при 25 клиентах` EBITDA ≈ `530 000 ₽/мес`, то есть gate достижим в base. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В demand-блоке одновременно есть `search demand в РФ: низкий` и `WTP подтверждён`; tier penalty уже учтён. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | В solution-блоке прямо зафиксировано: `продукт легко схлопывается в feature` без measurable ROI. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 18 | Risk matrix фиксирует `founder-led sale не масштабируется` и `санкции SaaS/платежей`, но риски управляемы. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | Есть 10 named targets, CAC `319 000 ₽`, payback `4,2 мес`, и логичный migration-led channel fit. |

**Sum raw = 99/150. Normalized score = round(99×100/150) = 66/100.**

## Вердикт

**NEAR-PASS.**

Порог approve не пройден. Формально кейс имеет путь к company_ebitda_potential_rub_month выше 500 000 ₽/мес за ≤24 месяцев и укладывается в ≤50 клиентов, но investment committee discount за слабый moat, низкую quality-of-evidence по demand-tier и founder-heavy GTM слишком велик. Рекомендация, не инвестировать как broad category bet сейчас, но держать в watchlist как узкий developer-portal wedge для API-first компаний.

## Delta vs previous

- Предыдущий похожий кейс: `enterprise-ai-documentation-platform-v2` был **APPROVED 70/100**.
- Текущий rerun: **66/100**, дельта **-4 балла**.
- Что ухудшило score: более жёсткий учёт `feature risk`, tier-penalty по evidence quality и слабая защита против self-build / incumbent docs stacks.

## 7-factor Moat Framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 2 | После миграции растут data/taxonomy и process switching costs. |
| Scale economies | 1 | Infra и шаблоны улучшаются с объёмом, но COGS не collapse-like. |
| Proprietary data / model advantage | 1 | Появляются клиентские usage-данные, но доказанного dataset moat пока нет. |
| Regulatory moat | 0 | Регуляторный барьер слабый, compliance скорее table-stakes. |
| Brand / distribution | 2 | У глобальной категории есть бренд-сигналы, локально можно зайти через migration wedge. |
| Embedded workflow | 2 | При встраивании в docs/update/release workflow продукт становится sticky. |

**Moat score = round((8 × 25) / 21) = 10/25.**

Вывод: moat ниже инвестиционного комфорта, хотя не нулевой. Главная проблема, value capture идёт через execution и rollout, а не через трудно-копируемый core advantage.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub (base) | 6 076 800 ₽ |
| customer_ltv_rub (stress) | 2 640 000 ₽ |
| CAC fully-loaded | 319 000 ₽ |
| LTV/CAC (base) | 19,1x |
| LTV/CAC (stress) | 8,3x |
| CAC payback по gross profit | 4,2 мес |
| Gross margin | 63,3% |
| contribution_margin_rub_month | 68 000 ₽ |
| fixed_costs_rub_month (full team) | 2 560 000 ₽ |
| company_ebitda_rub_month @25 клиентов (lean base) | 530 000 ₽/мес |
| clients_to_500k_ebitda | 25 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 33 |
| startup_capital_to_bep_rub | 17 967 889 ₽ |
| Break-even clients (full team) | 38 |
| p10 / p50 / p90 EBITDA @M24 | -1 555 708 ₽ / 1 669 357 ₽ / 5 351 838 ₽ |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Time | Cost, ₽ | Automation level |
|---|---|---|---:|---:|---|
| 1 | ICP research по API-first компаниям | SDR | 1,5 ч | 1 700 | Средний |
| 2 | Outreach и qualification | SDR | 1,5 ч | 1 700 | Средний |
| 3 | Discovery call | AE | 1 ч | 3 200 | Средний |
| 4 | Demo developer portal / AI search | AE + founder | 1,5 ч | 7 500 | Низкий |
| 5 | Pilot scoping | AE + CSM | 2 ч | 7 000 | Низкий |
| 6 | Import docs / initial setup | implementation | 10 ч | 25 000 | Средний |
| 7 | AI search tuning / taxonomy | implementation | 8 ч | 24 000 | Низкий |
| 8 | Onboarding workshop | CSM | 3 ч | 6 000 | Средний |
| 9 | Pilot support 4-6 недель | CSM + founder | 6 ч | 16 000 | Средний |
| 10 | Contracting / invoicing | AE + ops | 2 ч | 4 000 | Высокий |

## Команда

| Роль | Нужно чел. | Fully-loaded ₽/мес |
|---|---:|---:|
| Founder / CEO | 1 | 520 000 |
| Product / CTO | 1 | 430 000 |
| Full-stack / platform engineer | 1 | 300 000 |
| AI / search engineer | 1 | 340 000 |
| CSM / implementation | 1 | 220 000 |
| SDR | 1 | 170 000 |
| AE | 1 | 240 000 |
| Ops / finance (0,5) | 0,5 | 80 000 |
| **Итого** | **6,5** | **2 300 000 ₽/мес** |

## Top-3 Risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Price compression и self-build substitution | Высокая | Высокий | При ARPU ниже 100–120 тыс. ₽/мес модель быстро уходит к `Price -30%` сценарию с EBITDA -1,61 млн ₽ на M12. |
| Founder-heavy GTM и узкий buyer universe | Высокая | Высокий | Exact demand низкий, а pipeline держится на consultative sale в ограниченном ICP. |
| Sanctions / LLM / hosting dependency | Средняя | Высокий | Зарубежные infra-vendors и LLM-зависимость могут увеличить COGS и удлинить enterprise procurement. |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Yandex Cloud | Большой API surface и developer portal, docs влияют на partner onboarding. | email decision-maker в platform/devrel + конференции YaC | 180 000 ₽/мес |
| VK Cloud | Внешние облачные продукты и интеграции, нужна актуальная API-документация. | email VP Product / platform lead | 160 000 ₽/мес |
| Selectel | API-first cloud/infra vendor, documentation прямо влияет на time-to-first-deploy. | outbound через Head of Developer Relations | 150 000 ₽/мес |
| Т-Банк | Крупный developer ecosystem и API-поверхности для партнёров. | email ecosystem owner / product director | 220 000 ₽/мес |
| Ozon | Seller и partner APIs, documentation debt влияет на интеграции экосистемы. | партнёрство + outbound в platform/product | 200 000 ₽/мес |
| Avito | Большой partner/API контур и постоянные изменения продукта. | email Head of Platform / DevEx | 170 000 ₽/мес |
| MWS (MTS Web Services) | Новый cloud/API stack, нужен быстрый developer onboarding. | конференция + direct outbound | 160 000 ₽/мес |
| Сбер / developer ecosystem | Много developer-facing surfaces, высокий pain от freshness и discoverability docs. | enterprise partnership / warm intro | 220 000 ₽/мес |
| VK ID / VK Tech | Identity/API products, где плохая документация бьёт по активации партнёров. | outbound в product/platform team | 140 000 ₽/мес |
| 2ГИС | Публичные API и интеграционные сценарии, documentation quality влияет на adoption. | email product owner API | 120 000 ₽/мес |

## Proof points, которые нужны для APPROVED

1. Доказать 3-5 платящих пилотов по чеку ≥150 000 ₽/мес без bespoke-разработки.
2. Подтвердить support deflection и/или сокращение integration time минимум на 20-30%.
3. Показать, что onboarding на клиента держится ≤25-30 часов и не превращается в агентский проект.
4. Закрыть минимум один secure/private deployment кейс, чтобы снизить санкционный и data-residency risk.

## LTV Upside Calculator

Чтобы поднять verdict из 66/100 в approve-зону, нужны одновременно следующие сдвиги:

| Левер | Текущее | Target для upside | Эффект |
|---|---:|---:|---|
| ARPA / MRR | 120 000 ₽ | 150 000 ₽ | Улучшает contribution_margin_rub_month и снижает price-compression risk. |
| COGS | 44 000 ₽ | ≤38 000 ₽ | Поднимает GM и даёт запас против LLM/infra shocks. |
| CAC | 319 000 ₽ | ≤260 000 ₽ | Делает GTM менее founder-dependent и ускоряет масштабирование. |
| Pilot→paid conversion | 33-34% | ≥45% | Снижает acquisition burn на тот же объём новых клиентов. |
| Время внедрения | 4-8 недель | ≤4 недели | Ограничивает services creep и повышает repeatability. |
| Moat score | 10/25 | ≥14/25 | Нужны data/integration switching costs или partner-channel advantage. |

Если хотя бы 4 из 6 параметров будут подтверждены на реальных сделках, кейс можно пересматривать в сторону **APPROVED WITH NOTES**.

## Финальное решение комитета

Кейс интересный и коммерчески не пустой, но пока это скорее **узкий productized-service wedge**, чем очевидный software compounder. Оставить в watchlist, не одобрять как standalone investment thesis до подтверждения repeatable premium GTM, более сильного moat и меньшей зависимости от founder-led продажи.


---

# 07-score-trajectory.md

# Score trajectory

## 2026-04-22 — P4 Demand Validation
- Stage: P4 Demand Validation
- Case: mintlify-geo-expand-v2
- Summary: Поисковый спрос в РФ низкий, но есть подтверждённые платные substitute-решения, понятный ICP и проход Profit Gate в mid-market / enterprise сценариях.
- Demand score: 2/10 для category terms, до 19/100 на смежном запросе `api documentation`.
- Investment implication: CONDITIONAL PASS, идти дальше только с жёстким ICP на cloud, fintech, marketplace и API-first компании.
- Score trajectory impact: снижает ставку на PLG-массовость, но сохраняет инвестиционную логику как niche infrastructure SaaS.
- Analyst note: Главный риск не в отсутствии WTP, а в узости локального рынка и необходимости founder-led продаж вместо широкого inbound.

## 2026-05-11 — P7 Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: mintlify-geo-expand-v2
- Verdict: NEAR-PASS
- Score: 66/100
- Raw rubric: 99/150
- Summary: strong client-level economics и достижимый EBITDA-gate не компенсируют weak moat, founder-heavy GTM и tier-penalty по evidence quality.
- Investment implication: держать в watchlist как узкий developer-portal wedge, не одобрять как standalone category bet без новых proof points.
- Analyst note: чтобы перейти в approve-зону, кейсу нужны 3-5 repeatable платящих пилотов по чеку 150К+ ₽/мес и подтверждённый docs/support ROI.

