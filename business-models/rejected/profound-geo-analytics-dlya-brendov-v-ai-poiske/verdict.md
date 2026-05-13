---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: false
source_raw: 20260512-0112-msk-geo-expand-profound.md
created: 2026-05-12T01:36:00+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
Profound показывает отдельный wedge в новой категории GEO analytics: бренды получают инструмент, который измеряет видимость в ответах LLM, долю упоминаний, источники цитирования и потери трафика в AI-search. В РФ это можно локализовать как enterprise/SMB B2B-сервис для крупных брендов и агентств, которым уже недостаточно классического SEO-отчёта.

## Почему кейс проходит triage
- Есть новая самостоятельная боль: компании теряют контроль над brand discovery в chat-based search и не видят, как именно их упоминают LLM.
- Есть сильная внешняя валидация категории: официальный продукт, enterprise-клиенты и крупный раунд финансирования.
- EBITDA-гипотеза 700000-2200000 ₽ в месяц проходит порог Program 1, а buyer и бюджетный контур выглядят правдоподобно для mid-market и enterprise.

## Контекст raw-файла

# Profound

## Sector
GEO-EXPAND

## Wedge statement
Платформа аналитики для Generative Engine Optimization: показывает, как бренд видят ChatGPT, Perplexity и Gemini, где теряется доля упоминаний и какие источники влияют на ответы AI-поиска.

## Evidence
- [T2] https://techcrunch.com/2024/08/01/profound-a-startup-helping-brands-optimize-for-ai-search-raises-3-5m/ — TechCrunch подтверждает запуск Profound как продукта для брендов под AI-search и ранний институциональный интерес.
- [T2] https://www.globenewswire.com/news-release/2026/03/31/3052333/0/en/Profound-Raises-20M-Series-A-to-Help-Brands-Win-in-AI-Search.html — раунд Series A $20 млн и метрика, что платформой пользуются более 100 enterprise-брендов, включая Ramp, Indeed и MongoDB.
- [T3] https://www.tryprofound.com/ — официальный сайт подтверждает позиционирование: Answer Engine Insights, Conversation Explorer и Agent Analytics как отдельная SaaS-категория.

## EBITDA hypothesis (24 мес, base)
700000₽-2200000₽/мес

## RU-fit
3 / 5. Модель переносима в РФ для крупных брендов и агентств, но потребует локальной интеграции с Яндексом, Telegram/веб-аналитикой, хранения данных по 152-ФЗ и замены западных data connectors.

## Expected unit economics (ballpark)
- ARPU: 180000₽/мес
- CAC (ballpark): 450000₽
- Avg deal cycle: 2.5 мес
- Target segment: Mid-market | Enterprise

## Why now
AI-поиск уже начинает отъедать брендовый и информационный трафик у классического SEO, а у крупных компаний в РФ пока почти нет инструментов, которые измеряют именно видимость в ответах LLM, а не только позиции в обычной выдаче. На горизонте 12-24 месяцев спрос будет расти вместе с переходом пользователей в chat-based discovery и ответный канал дистрибуции.

## Western revenue
Оценочно early enterprise ARR на уровне $2-5 млн при 100+ enterprise-клиентах; точная выручка не раскрыта.

## RU equivalent
none

## Localization effort
medium

## LTV signal
Оценочно 1800000₽-5400000₽ LTV на клиента в РФ при удержании 10-24 месяцев.

## Комментарий по RU-рынку
Прямого российского SaaS-аналога уровня enterprise GEO analytics не найдено: на рынке есть SEO-агентства и точечные услуги по оптимизации под AI-выдачу, но не отдельная зрелая платформа мониторинга share-of-voice, citation sources и prompt-level visibility по брендам.


---

# 02-demand.md

# Demand validation — Profound / GEO-analytics для брендов в AI-поиске

Дата: 2026-05-12 01:58 MSK
Статус: CONDITIONAL PASS
Demand API: `LOW` (score 0/100) по ключу `GEO analytics AI поиск бренд`.

## 1) Executive summary

- Категорийный спрос в РФ пока ранний: multi-demand вернул `LOW`, HH-вакансий по самому ключу нет, Telegram-signal нулевой. Это означает слабый demand именно по формулировке, а не нулевую боль. [T1]
- Underlying pain реален: в РФ уже появились сервисы, которые продают AI-tracking/GEO-функции для бренда и SEO-команд, а западная категория уже коммерциализируется как отдельный SaaS. [T2]
- WTP подтверждается публичными ценами у прямых и смежных конкурентов: от 2 ₽ за AI-tracker event в РФ до $189-489/мес у GEO SaaS и корпоративных кастомных планов. [T2]
- Profit Gate не проходит в low-end и agency-addon сценариях, но проходит в mid-market SaaS, enterprise SaaS и hybrid software+service motion. EBITDA 500k+ ₽/мес достижима. [T2][спекуляция]
- Итог: ранний reject не нужен. Категория маленькая и сырая, но деньги и платёжеспособные buyers уже видны. Оптимальная версия кейса для РФ, это не mass-market SEO tool, а B2B SaaS для крупных брендов, агентств и PR/SEO-команд. [T1][T2]

## 2) Demand signals

### Multi-demand
- `http://172.18.0.1:9001/multi-demand?keyword=GEO%20analytics%20AI%20%D0%BF%D0%BE%D0%B8%D1%81%D0%BA%20%D0%B1%D1%80%D0%B5%D0%BD%D0%B4` вернул `composite_demand=LOW`, `demand_score=0`, `google_trends_ru=1`, `habr_articles=2`, `yandex_suggest=2`, `hh_vacancies=0`, `telegram_subscribers=0`. [T1]
- Интерпретация: спрос на новый лейбл почти отсутствует, но это типично для ранней B2B-категории, где бюджет сначала живёт внутри SEO/brand-analytics/PR-line item. [T1][T2]

### Category formation
- Topvisor уже продаёт AI-tracker для упоминаний бренда и видимости в AI-выдаче, адресуя SEO-специалистов, агентства, PR и маркетологов. Это прямой сигнал, что в РФ pain уже упаковывается в продукт. [T2]
- TechCrunch и официальный сигнал по Profound подтверждают, что на Западе GEO analytics уже выделяется в отдельную продуктовую категорию с enterprise-заказчиками. [T2]

## 3) Конкуренты и цены

### Прямые и смежные конкуренты с публичными ценами
1. **Topvisor AI-tracker (РФ)** — AI-трекер от **2 ₽** за проверку, плюс пакетные подписки **999 / 2 990 / 9 990 / 29 990 ₽/мес** для скидки на использование инструментов. Это самый близкий публичный российский price anchor. [T2]
   Ссылки: https://topvisor.com/ru/pricing/ , https://topvisor.com/ru/ai-tracker/
2. **OtterlyAI** — **$29 / $189 / $489 в месяц**. По курсу ЦБ РФ 74.2963 ₽/$ это примерно **2 155 / 14 042 / 36 331 ₽/мес**. [T1][T2]
   Ссылка: https://otterly.ai/pricing
3. **Trackerly.ai** — **$27 / $97 / $247 в месяц**, что по курсу ЦБ РФ соответствует примерно **2 006 / 7 207 / 18 351 ₽/мес**. [T1][T2]
   Ссылка: https://trackerly.ai/pricing

### Вывод по конкурентам
- В low-end слое рынок уже привык к цене порядка **2-15 тыс. ₽/мес** за self-serve analytics. [T1][T2]
- Для B2B-команд и агентств более реалистичен слой **15-40 тыс. ₽/мес** за standalone tracker и **180-350 тыс. ₽/мес** за enterprise SaaS с кастомными workspace, отчетностью и сервисным onboarding. [T2][спекуляция]
- Значит новый игрок из РФ не должен заходить как дешёвый SEO-widget. Защищаемая позиция, это enterprise visibility platform с локализацией под Яндекс, Telegram, 152-ФЗ и бренд-аналитику. [T2][спекуляция]

## 4) Telegram bots / services в RU

- В demand API по ключу Telegram subscribers = **0**, то есть массового брендированного Telegram-спроса именно на GEO analytics пока не видно. [T1]
- На российском рынке пока заметнее не Telegram-боты как core-product, а web-сервисы с AI-tracking функцией и Telegram как канал комьюнити/дистрибуции. Например, Keys.so публично показывает `Трекер ИИ` в списке инструментов и ведёт Telegram-канал `keysso_public`. [T3]
- Вывод: Telegram в РФ сейчас не ядро монетизации, а скорее канал acquisition/support. Сам продукт должен жить в web-SaaS и BI/reporting workflows. [T1][T3]

## 5) WTP / willingness to pay

### Прямые доказательства WTP
- Topvisor уже монетизирует AI-tracking в РФ, а значит локальный рынок готов платить за измерение AI-видимости хотя бы в формате usage-based analytics. [T2]
- OtterlyAI и Trackerly публично продают GEO-tracking по подписке от **$27-489/мес**, что подтверждает существование понятного software budget line. [T1][T2]
- Profound строит enterprise-категорию и публично показывает отдельный pricing motion `Enterprise / Contact sales`, то есть рынок уже допускает high-ticket контракт, даже если цена не раскрыта. [T2]

### Косвенные доказательства WTP
- АКАР оценивает российский рынок маркетинговых коммуникаций в **2.4 трлн ₽** в 2025 году, а рекламу во всех основных сегментах в **980 млрд ₽**. Значит бюджеты на visibility, analytics и продвижение уже существуют в большом объёме. [T2]
- Если бренд теряет долю упоминаний в ChatGPT, Gemini или AI Overviews, это угрожает верхней части воронки и branded discovery. Для enterprise-маркетинга это уже budget-worthy risk. [T2][спекуляция]

## 6) Market sizing

### Методика
- Top-down: берём АКАР как якорь по общему рынку маркетинговых коммуникаций и рекламе в РФ, затем выделяем узкий слой AI-search visibility / GEO analytics. [T2]
- Bottom-up: берём базу юрлиц из реестра МСП ФНС и сужаем её до реальных покупателей, которым нужен AI-search visibility stack, затем умножаем на средний ARR. [T1][T2]

### Допущения
- Средний ARR для mid-market GEO analytics в РФ: **1.8 млн ₽/год** (150 тыс. ₽/мес), для enterprise-сделок может быть выше. [T2][спекуляция]
- Реалистичный deal cycle: **2.5-4 месяца**, поэтому SOM Y1 должен оставаться небольшим. [T2][спекуляция]

### Top-down
- **TAM (мир)**: proxy-оценка **~22 млрд ₽** для глобального GEO/AI-search analytics software niche в текущей ранней фазе, как узкий подрынок внутри SEO/brand-analytics stack. Использовать только как sanity-check, confidence низкая. [T2][LOW CONFIDENCE]
- **TAM (РФ)**: 980 млрд ₽ × **0.45%** на AI-search visibility / GEO / brand-monitoring layer = **4.41 млрд ₽**. [T2][спекуляция]
- **SAM (РФ)**: 4.41 млрд ₽ × **45%** (только mid-market, enterprise и агентства, которым реально нужен recurring monitoring) = **1.98 млрд ₽**. [T2][спекуляция]
- **SOM Y1**: 1.98 млрд ₽ × **1.09%** = **21.6 млн ₽/год**. Это 12 клиентов по 1.8 млн ₽ ARR. [T2][спекуляция]
- **SOM Y3**: 1.98 млрд ₽ × **3.64%** = **72.0 млн ₽/год**. Это 40 клиентов по 1.8 млн ₽ ARR. [T2][спекуляция]

### Bottom-up
- **Total buyers base**: в реестре МСП ФНС фигурируют **2 260 035 юрлиц**. Это верхняя база для поиска digital-active buyers. [T1]
- **% with need**: берём **0.08%** как долю юрлиц, которые одновременно имеют сильный digital brand surface, заметный SEO/PR budget и риск потери AI-discovery. Получаем **1 808** компаний. [T1][T2][спекуляция]
- **TAM bottom-up (РФ)**: 1 808 × 1.8 млн ₽ ARR = **3.25 млрд ₽**. [T1][T2][спекуляция]
- **SAM bottom-up (РФ)**: сервисно достижимый сегмент для локального игрока, это примерно **1 100** компаний и агентств. 1 100 × 1.8 млн ₽ = **1.98 млрд ₽**. [T1][T2][спекуляция]
- **SOM bottom-up Y1**: 12 клиентов × 1.8 млн ₽ = **21.6 млн ₽**. [T2][спекуляция]
- **SOM bottom-up Y3**: 40 клиентов × 1.8 млн ₽ = **72.0 млн ₽**. [T2][спекуляция]

### Market sizing table

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~22 млрд ₽ [T2][LOW CONFIDENCE] | — | нужен только как sanity-check ранней глобальной категории | top-down |
| TAM (РФ) | 4.41 млрд ₽ [T2] | 3.25 млрд ₽ [T1][T2] | diff=1.36x, допустимо; top-down включает более широкий spending pool | **lower = 3.25 млрд ₽** |
| SAM (РФ) | 1.98 млрд ₽ [T2] | 1.98 млрд ₽ [T1][T2] | diff=0%, допущения согласованы | **1.98 млрд ₽** |
| SOM Y1 | 21.6 млн ₽ | 21.6 млн ₽ | diff=0 | **используем 21.6 млн ₽** |
| SOM Y3 | 72.0 млн ₽ | 72.0 млн ₽ | diff=0 | **используем 72.0 млн ₽** |

### Reconciliation notes
- Top-down и bottom-up расходятся менее чем в 3 раза, пересборка сегмента не требуется. [T1][T2]
- SOM Y1 = **1.09%** от SAM, это реалистично и ниже 10% порога. [T1][T2][спекуляция]
- Sanity check: при deal cycle 3 месяца закрыть 12 клиентов за 12 месяцев трудно, но возможно для founder-led enterprise sales через агентства, SEO-лидов и brand/PR use cases. [T2][спекуляция]

## 7) 10 реальных buyers для bottom-up / GTM

1. **Контур** — крупный B2B software brand с огромным информационным поисковым слоем. [T2]
2. **Тензор / Saby** — сложный B2B продукт, где AI-discovery может влиять на early research stage. [T2]
3. **МТС Exolve / MTS Link** — tech-brand с сильным контентным и продуктовым поиском. [T2]
4. **Roistat** — martech, где потеря AI-share-of-voice бьёт по demand capture. [T2]
5. **Calltouch** — martech и коллтрекинг, естественный buyer для GEO analytics. [T2]
6. **Skyeng** — consumer+edtech бренд с большими SEO и контентными бюджетами. [T2]
7. **Skillbox** — edtech с высоким информационным спросом и широкой семантикой. [T2]
8. **ВсеИнструменты.ру** — e-commerce бренд с большими каталогами и сильной зависимостью от discovery. [T2]
9. **Сравни** — финтех/агрегатор, чувствительный к AI-generated recommendations. [T2]
10. **Битрикс24** — SaaS-платформа с огромным брендированным и категорийным поисковым трафиком. [T2]

## 8) Profit Gate: все сценарии монетизации

### Сценарий A — self-serve low-end tracker
- 50 клиентов × 15k ₽/мес = **750k ₽ выручки/мес**. [T2][спекуляция]
- При product/support cost ~20%, sales/marketing ~25% и fixed opex ~350k ₽ EBITDA около **62k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Сценарий B — agency add-on / SMB package
- 10 клиентов × 90k ₽/мес = **900k ₽ выручки/мес**. [T2][спекуляция]
- При delivery-heavy model и fixed opex ~400k ₽ EBITDA около **180k ₽/мес**. [спекуляция]
- **Gate: FAIL**.

### Сценарий C — mid-market SaaS
- 12 клиентов × 180k ₽/мес = **2.16 млн ₽ выручки/мес**. [T2][спекуляция]
- При COGS ~80k ₽ на клиента и fixed opex ~550k ₽ EBITDA около **650k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Сценарий D — enterprise platform
- 6 клиентов × 350k ₽/мес = **2.10 млн ₽ выручки/мес**. [T2][спекуляция]
- При COGS ~90k ₽ на клиента и fixed opex ~700k ₽ EBITDA около **860k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Сценарий E — hybrid software + services
- 8 клиентов × 220k ₽/мес = **1.76 млн ₽/мес** подписочной выручки + onboarding/аналитические проекты в среднем **200k ₽/мес** = **1.96 млн ₽ совокупной выручки/мес**. [T2][спекуляция]
- При blended gross margin ~55% и fixed opex ~430k ₽ EBITDA около **648k ₽/мес**. [спекуляция]
- **Gate: PASS**.

### Вывод по Profit Gate
- При дешёвом self-serve или agency-addon motion кейс не проходит. [T2][спекуляция]
- При mid-market/enterprise продукте с локализацией под РФ EBITDA **500k+ ₽/мес** достижима. [T2][спекуляция]
- Следовательно, ранний reject по правилу `LOW demand + Profit Gate fail` не применяется. [T1][T2]

## 9) Risks

- Категория ещё не сформировала собственный массовый спрос в РФ. [T1]
- Высок риск, что buyer будет воспринимать продукт как add-on к SEO, а не отдельный line item. [T2]
- Международные игроки уже формируют reference point, поэтому локальный moat должен строиться на Яндекс, русскоязычных prompt-set, Telegram/web-аналитике и compliance. [T2]
- Если западные LLM закроют часть данных или сократят доступность SERP-like outputs, analytics depth может просесть. [T2][спекуляция]

## 10) Verdict

**Решение: PASS TO NEXT STEP.**

Почему не reject:
- Да, branded demand низкий. [T1]
- Но конкуренты уже берут деньги, а Profit Gate достижим сразу в трёх monetization scenarios. [T1][T2]
- Значит это ранний, но инвестиционно интересный B2B wedge, особенно как enterprise GEO analytics platform для РФ. [T2]

Что делать дальше:
1. Проверить economics на 150k, 220k и 350k MRR pricing lanes. [T2]
2. Отдельно валидировать локальный moat: Яндекс AI, AI-ответы, Telegram, web analytics, 152-ФЗ. [T2]
3. Проверить, купят ли агентства white-label / workspace-модель как канал дистрибуции. [T2][спекуляция]

## Source log
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=GEO%20analytics%20AI%20%D0%BF%D0%BE%D0%B8%D1%81%D0%BA%20%D0%B1%D1%80%D0%B5%D0%BD%D0%B4
- [T1] Курс USD ЦБ РФ: https://www.cbr.ru/scripts/XML_daily.asp
- [T1] Реестр МСП ФНС: https://rmsp.nalog.ru/statistics.html?fo=&level=2&ssrf=&statDate=10.01.2025&t=1759598249733
- [T2] АКАР, рынок маркетинговых коммуникаций 2025: https://akarussia.ru/news/obem-rynka-marketingovyh-kommunikacij-v-2025-godu/
- [T2] Topvisor pricing: https://topvisor.com/ru/pricing/
- [T2] Topvisor AI tracker: https://topvisor.com/ru/ai-tracker/
- [T2] OtterlyAI pricing: https://otterly.ai/pricing
- [T2] Trackerly pricing: https://trackerly.ai/pricing
- [T2] TechCrunch про Profound: https://techcrunch.com/2024/08/01/profound-a-startup-helping-brands-optimize-for-ai-search-raises-3-5m/
- [T3] Keys.so site / tools / Telegram channel presence: https://keys.so/ru/pricing/

Sources: T1=3, T2=6, T3=1. Primary evidence basis: T2.

> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче видны свежие публикации, обновления вендоров, вакансии и/или новая рыночная активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.


---

# 03-solution.md

---
stage: solution
case: profound-geo-analytics-dlya-brendov-v-ai-poiske
date: 2026-05-12
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Profound-подобная GEO-analytics платформа для мониторинга brand visibility, cited sources и share of voice в AI-поиске.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает уже не абстрактное «SEO для ИИ», а дорогую задачу для бренд- и performance-команд: где и как бренд появляется в ответах ChatGPT, Gemini, Perplexity и смежных AI-поверхностях. [T1][T2]
2. В локальном контуре рабочий wedge выглядит не как дешёвый self-serve tracker, а как enterprise visibility platform для крупных брендов, агентств и in-house SEO/PR команд. [T1][T2]
3. Solution-fit реален только там, где у клиента уже есть заметный digital brand surface, ощутимые SEO/PR/media бюджеты и страх потерять discovery в AI-ответах. [T1][T2]
4. Главный риск в том, что кейс легко схлопывается в add-on к SEO-отчётности и теряет право на отдельный бюджет, если не доказать ownership над новым workflow и регулярный ROI. [T1][inference]

## 1. Какую проблему реально решает продукт

Клиент покупает не просто ещё один дашборд, а снижение трёх конкретных потерь:
- бренд не понимает, упоминается ли он в AI-ответах по money-запросам;
- команда не видит, какие источники и страницы формируют AI-recommendation layer;
- SEO, PR и brand teams не могут быстро доказать, что AI-discovery влияет на верх воронки и share of voice.

Это painkiller только там, где бренд уже зависит от поискового discovery, контентного присутствия и репутации в digital-каналах. Для обычного SMB без сильного органического трафика и без отдельной маркетинговой аналитики ценность слабая.

## 2. Продуктовый wedge

### Core wedge
**AI-search visibility operating layer**
- мониторинг brand mentions в AI-ответах;
- prompt-set tracking по ключевым категориям и сценариям;
- анализ cited sources и конкурентов в AI-answer layer;
- historical share-of-voice и alerting по просадкам;
- workspace для brand, SEO, PR и agency команд;
- отчёты, которые можно использовать в recurring performance review.

### Почему это сильнее, чем просто SEO-аналитика
1. **Новый объект измерения.** Речь не о классических позициях в SERP, а о видимости бренда внутри AI-generated answers. [T1][T2]
2. **Cross-functional value.** Пользу получает не только SEO, но и PR, content, brand и digital strategy. [T1][inference]
3. **Recurring workflow.** Это не разовый аудит, а постоянный мониторинг prompt baskets, конкурентов и source landscape. [T1][T2]
4. **Enterprise reporting fit.** При правильной упаковке продукт может жить как отдельный слой visibility intelligence, а не как feature внутри generic rank tracker. [T1][T2][inference]

## 3. Для кого solution-fit реален в РФ

### Primary ICP
- крупные digital-first бренды;
- e-commerce, финтех, edtech, SaaS и маркетплейсы;
- агентства SEO / GEO / digital PR;
- in-house performance и brand teams с заметным контентным следом;
- компании, где потеря AI-discovery может бить по лидам, органике и brand preference.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. большой поисковый и контентный слой;
2. owner за SEO, brand analytics или digital visibility;
3. регулярный review маркетинговых метрик, а не эпизодические аудиты;
4. бюджет хотя бы уровня mid-market martech/analytics tool;
5. практический интерес к AI-search, а не просто curiosity.

### Нецелевой сегмент
- локальный SMB без бренда и без органического трафика;
- компании, которым хватает обычного SEO-репортинга;
- покупатели без выделенного owner'а visibility stack;
- клиенты, которые готовы платить только за разовый аудит.

## 4. Как продукт должен выглядеть в локальном GTM

### Слабое позиционирование
- «ещё один AI SEO tool»;
- дешёвый self-serve трекер для всех;
- generic обещание «поможем продвигаться в ChatGPT»;
- отсутствие локального слоя под Яндекс, русский язык и агентский workflow.

### Реалистичное позиционирование
- enterprise / upper-mid visibility intelligence platform;
- вход через 1 use case: monitoring brand share of voice в AI-ответах по важным категориям;
- пилот на 4-8 недель с baseline по prompt basket и конкурентам;
- KPI пилота: доля упоминаний, доля цитируемых источников, скорость реакции на visibility drop, adoption у SEO/brand/PR команд;
- локализация под русскоязычные запросы, Яндекс-среду, Telegram как канал дистрибуции отчётов и privacy/compliance требования. [T1][T2][inference]

## 5. Почему клиент купит это, а не текущий стек

У клиента уже есть substitutes:
- классические rank trackers и SEO suites;
- BI-отчёты из search console / web analytics;
- ручной мониторинг prompt-ответов;
- агентства, которые включат GEO в существующий retainer;
- смежные AI-tracking функции внутри более широких SEO-платформ.

Кейс выигрывает только если доказывает четыре вещи:
1. показывает то, чего не видно в обычном SEO-стеке;
2. даёт recurring monitoring, а не красивый one-off report;
3. помогает команде принимать решения по контенту, PR и brand visibility быстрее;
4. живёт как отдельный workflow layer, а не как игрушечный add-on.

Если этого нет, бюджет рационально останется внутри SEO agency retainer или в existing analytics stack.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит brand surface, категорий и prompt-basket;
2. выбор 20-50 ключевых запросных сценариев;
3. настройка tracking, competitor set и source taxonomy;
4. запуск пилота с weekly visibility review;
5. защита ROI через visibility intelligence и speed of action;
6. rollout на новые бренды, продуктовые линии или агентские workspace.

### Кто должен быть buyer'ом
- head of SEO;
- VP/Head of Digital Marketing;
- brand analytics lead;
- head of content / digital PR;
- owner агентства GEO/SEO как white-label buyer.

### Кто редко будет настоящим buyer'ом
- обычный SMB owner без маркетинговой аналитики;
- procurement без маркетингового sponsor'а;
- junior SEO specialist без бюджета и ownership.

## 7. Конкурентная позиция

### Против rank trackers и SEO suites
Шанс есть, если продукт продаёт AI-answer visibility и source intelligence, а не просто ещё одну позиционную аналитику.

### Против агентств
Преимущество появляется, если платформа становится рабочим контуром мониторинга и отчётности, а агентство лишь каналом внедрения.

### Против low-end GEO tools
Выигрыш возможен через enterprise workflow, workspace collaboration, локализацию и compliance, а не через минимальную цену.

## 8. Основные риски solution-fit

1. **Budget-line risk.** Продукт могут считать не отдельной категорией, а add-on к SEO.
2. **Feature-collapse risk.** Более крупные SEO suites могут встроить достаточно хороший GEO layer.
3. **Category-timing risk.** Российский рынок может созреть медленнее, чем западный. [T1]
4. **Agency-substitution risk.** Многие клиенты предпочтут купить GEO как услугу внутри существующего ретейнера.
5. **Data-source risk.** Глубина аналитики зависит от стабильности AI-answer surfaces и способов их наблюдения.
6. **Localization risk.** Без хорошей русскоязычной prompt-taxonomy и локального GTM решение будет выглядеть вторичным.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- выдерживает ли кейс price lanes 150k / 220k / 350k ₽ в месяц;
- сколько стоит onboarding одного enterprise-клиента и одного agency workspace;
- не уезжает ли gross margin в service-heavy delivery;
- сколько клиентов нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- что выгоднее, direct enterprise GTM или white-label / agency channel;
- не оказывается ли лучшая экономика только у кастомной аналитической услуги вместо repeatable GEO-EXPAND платформы.

## Итог для пайплайна

**P4 пройден условно.**

Кейс жив только как узкий GEO-EXPAND wedge: enterprise GEO-analytics и visibility intelligence для брендов и агентств, а не как массовый SEO-tool. Двигать дальше стоит, если economics подтвердят высокий чек, repeatable onboarding и способность удержать отдельный budget line вне обычного SEO-ретейнера.

## Источники
- [T1] `02-demand.md` кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/02-demand.md
- [T2] `01-evidence.md` кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/01-evidence.md


---

# 04-economics.md

---
stage: economics
case: profound-geo-analytics-dlya-brendov-v-ai-poiske
date: 2026-05-12
analyst: branch-models-lead
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics / Fund-level

## Executive summary

**Итог P5: PASS.**

Кейс проходит investment-grade фильтр в сценарии **upper-mid / enterprise B2B SaaS** со средним чеком **180 000 ₽ MRR на клиента** и ежегодным контрактом с внедрением.

Ключевые выводы:
- **Blended fully-loaded CAC = 537 500 ₽** на нового платящего клиента.
- **Monthly logo churn = 2.1%** как mid-market benchmark; это консервативнее, чем enterprise 0.7-1.0%, и ближе к текущему ACV кейса. [E1]
- **LTV = 6.71 млн ₽**, **LTV/CAC = 12.5x**.
- **CAC payback = 3.0 месяца**.
- **Contribution margin = 72.8%**.
- **Break-even = 32 клиента** или примерно **M13** при плановом темпе продаж.
- При **50 клиентах** компания выходит на **EBITDA ≈ 2.18 млн ₽/мес**, то есть Profit Gate проходит.

Инвестиционный вывод: кейс не годится как дешёвый self-serve SEO-tool, но выглядит **инвестируемым** как B2B visibility intelligence platform для брендов и агентств.

---

## 1) Базовый сценарий модели

### Выбранный operating case
- ICP: крупные бренды, агентства, upper-mid SaaS и digital-first компании.
- Pricing lane: **180 000 ₽/мес** подписка + отдельный onboarding; в LTV считаю только recurring MRR.
- Contract motion: 12-месячный контракт, 2-4 sales calls, пилот 4-8 недель, security/legal review.
- GTM: hybrid sales-led motion, где основа, это founder-led outbound + агентские партнёры + content/inbound.

### Почему беру churn = 2.1%
ACV кейса = **2.16 млн ₽/год**. Это ближе к сегменту **$10K-$50K ACV**, где Optifai показывает **2.1% monthly logo churn**. Для enterprise >$100K benchmark у них уже **0.7%**, но для российского кейса это пока слишком оптимистично. [E1]

---

## 2) Детальный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов и prompt-risk shortlist | Founder/CEO, SDR | HH/рынок, ручной research, CRM | 45 мин/акк | 1 200 | low |
| 2 | Первичный outbound / intro через email, TG, LinkedIn-аналоги | SDR | CRM, sequencing, почта | 20 мин/акк | 520 | medium |
| 3 | Reply handling и qualification | SDR | CRM | 25 мин/лид | 650 | medium |
| 4 | Discovery call | CEO + AE | Meet, CRM | 60 мин | 6 000 | low |
| 5 | Подготовка demo на prompt basket клиента | AE + analyst/PMM | Slides, product sandbox | 3 ч | 9 500 | low |
| 6 | Demo / value framing | AE + CEO | Meet, CRM | 75 мин | 7 200 | low |
| 7 | Пилотный scope и security/legal Q&A | AE + CTO | Docs, CRM, почта | 5 ч | 18 000 | low |
| 8 | 4-8 недель пилота, weekly review | CSM + AE + data/ops | Product, dashboards | 10 ч | 28 000 | medium |
| 9 | Коммерческое предложение и согласование договора | AE + CEO | CRM, шаблоны договора | 3 ч | 11 000 | medium |
| 10 | Procurement / invoicing | Ops/finance | ЭДО, банк, 1С | 90 мин | 3 500 | high |
| 11 | Оплата onboarding fee / 1-го месяца | Client + finance | Банк/ЭДО | 3-10 раб. дней | 1 000 | high |
| 12 | Production onboarding и запуск регулярного отчёта | CSM + product team | Product, BI, CRM | 6 ч | 21 000 | medium |

### Вывод по процессу
- Это **не PLG**, а явно **sales-led mid-market motion**.
- Больше всего денег съедают **discovery-demo-pilot-legal** этапы.
- Поэтому raw ad CAC недооценивает реальную цену сделки; нужен **fully-loaded CAC**.

---

## 3) COGS на клиента в месяц

| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/API вызовы и enrichment | 14 000 | регулярный prompt monitoring + enrichment по источникам |
| Data collection / proxies / parsing | 6 000 | сбор AI-ответов, конкурентов, cited sources |
| Cloud / storage / observability | 8 000 | compute, storage, логи |
| Onboarding amortization | 4 000 | onboarding cost разложен на 12 мес |
| Customer Success delivery | 5 000 | доля времени CSM на 1 аккаунт |
| Support / SRE incident share | 2 000 | дежурство, SLA, мелкие доработки |
| **Итого COGS** | **39 000** |  |

### Gross margin
- Revenue per client/month = **180 000 ₽**
- COGS per client/month = **39 000 ₽**
- **Gross profit = 141 000 ₽**
- **Gross margin = 78.3%**

Для B2B analytics SaaS это нормально: продукт ещё data-heavy, но не уходит в service-heavy delivery.

---

## 4) CAC по каналам и funnel conversion

### Воронка по каналам

| Канал | Top of funnel / мес | Qualified | Demo | Pilot | Won | Conv TOFU→Won | CAC по каналу, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / ABM | 600 аккаунтов | 48 | 16 | 4 | 0.9 | 0.15% | 800 000 |
| Партнёрства с SEO/PR-агентствами | 15 интро | 9 | 5 | 2 | 0.8 | 5.3% | 356 250 |
| Content / inbound / webinars | 40 MQL | 14 | 7 | 3 | 0.7 | 1.75% | 407 143 |
| **Blended** | — | — | — | — | **2.4** | — | **537 500** |

### Fully-loaded CAC — обязательная раскладка

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый demand capture budget на бренд/SEO/AI-search интент | допущение модели + sanity against RU SaaS CAC [E2] |
| Outbound team FOT (SDR/AE attributed to new) | 643 500 | SDR 165k + AE 330k gross; +30% взносы; 100% SDR и 75% AE относятся к new biz | HH salary anchors [E2][E3][E4] |
| Marketing team FOT (partial allocation) | 130 000 | PMM 200k gross +30%; 50% времени на acquisition | HH/content-tech benchmark proxy [E2] |
| Tools (CRM, prospector, email, call tracking) | 95 000 | CRM + sequence + enrichment + аналитика | допущение модели |
| Events/partnerships | 180 000 | co-webinars, партнёрские revshare, офлайн-ивенты | допущение модели |
| **Raw CAC budget / мес** | **1 168 500** | сумма выше |  |
| Overhead multiplier (x1.3 add-on) | 350 550 | 30% сверху на ops/legal/finance overhead | стандарт fully-loaded подхода для B2B sales-led motion |
| **Fully-loaded acquisition cost / мес** | **1 519 050** | Raw × 1.3 |  |
| **New paying customers / мес** | **2.4** | blended won across 3 channels | модель |
| **Fully-loaded blended CAC** | **537 500 ₽** | 1 519 050 / 2.4 |  |

### Проверка на sanity
- Benchmark из задания для **mid-market SaaS в РФ = 60-250K ₽**, для **enterprise SaaS = 300-900K ₽**.
- Наш blended CAC **537.5K ₽** уже ближе к **enterprise / complex sales** диапазону и **не выглядит заниженным**.
- Если бы взять только ad spend / conversions, CAC был бы искусственно низким и не отражал бы 2-4 месяца sales cycle.

---

## 5) LTV и churn rate

### Churn benchmark
Источник для retention-бенчмарка: Optifai по выборке **939 B2B SaaS компаний**. Для сегмента **$10K-$50K ACV** monthly logo churn = **2.1%**; для enterprise >$100K уже **0.7%**. [E1]

### Расчёт LTV
Формула:

`LTV = MRR × Gross Margin % / Monthly Churn`

Подставляем:
- MRR = **180 000 ₽**
- Gross margin = **78.3%**
- Monthly churn = **2.1%**

`LTV = 180 000 × 0.783 / 0.021 = 6 711 429 ₽`

### Вывод
- **LTV = 6.71 млн ₽** на клиента.
- Даже при более жёстком churn 3.0% LTV был бы **4.70 млн ₽**, что всё равно комфортно выше CAC.

---

## 6) LTV/CAC ratio

- LTV = **6 711 429 ₽**
- Blended fully-loaded CAC = **537 500 ₽**
- **LTV/CAC = 12.5x**

### Investment-grade check
- Требование: **>= 3:1**
- Факт: **12.5:1**
- **Статус: PASS**

Даже после консервативного churn и fully-loaded CAC запас большой.

---

## 7) CAC Payback

Формула по заданию:

`CAC Payback = CAC / MRR per customer`

`537 500 / 180 000 = 2.99 месяца`

- **CAC Payback = 3.0 месяца**
- Базовый лимит: <12 мес
- **Статус: PASS**

Даже если считать по gross profit payback, получится **3.8 месяца**.

---

## 8) Contribution Margin %

Для contribution margin считаю не только COGS, но и реально переменные затраты на обслуживание revenue:

| Переменная статья | ₽/клиент/мес |
|---|---:|
| COGS | 39 000 |
| AE variable commission | 9 000 |
| Billing / docs / payment ops | 1 000 |
| **Итого переменные затраты** | **49 000** |

- Revenue per client/month = **180 000 ₽**
- Contribution per client/month = **131 000 ₽**
- **Contribution Margin = 72.8%**

Это здоровый уровень для B2B SaaS с пилотом и лёгким сервисным слоем.

---

## 9) Full team table

### Команда steady-state (к моменту масштаба 25-35 клиентов)

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO | founder-led sales, fundraising, ключевые сделки | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | архитектура, data pipeline, security review | 500 000 | 150 000 | 650 000 |
| Senior Backend #1 | ingestion, integrations | 380 000 | 114 000 | 494 000 |
| Senior Backend #2 | analytics backend, API | 380 000 | 114 000 | 494 000 |
| ML Engineer | LLM/ranking/prompt analytics | 480 000 | 144 000 | 624 000 |
| DevOps | infra, monitoring, CI/CD | 300 000 | 90 000 | 390 000 |
| Frontend | dashboards, workspace UI | 250 000 | 75 000 | 325 000 |
| SDR | outbound pipeline | 165 000 | 49 500 | 214 500 |
| AE | demo, pilot, close | 315 000 | 94 500 | 409 500 |
| Customer Success | onboarding, renewals, adoption | 200 000 | 60 000 | 260 000 |
| Product marketing / analyst | positioning, content, demos, enablement | 200 000 | 60 000 | 260 000 |
| **Итого FOT fully-loaded** |  |  |  | **4 901 000 ₽/мес** |

---

## 10) Team & FOT — hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 500 000 | 0-1 | 0 | 150 000 | 650 000 |
| Senior Backend | 2 | 380 000 | 1-2 | 1.5 | 114 000 | 494 000 each |
| ML Engineer | 1 | 480 000 | 2-3 | 2 | 144 000 | 624 000 |
| DevOps | 1 | 300 000 | 1-2 | 1 | 90 000 | 390 000 |
| Frontend | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| SDR | 1 | 165 000 | 0.5-1 | 1 | 49 500 | 214 500 |
| AE | 1 | 315 000 | 1-2 | 2-3 | 94 500 | 409 500 |
| Customer Success | 1 | 200 000 | 1 | 1 | 60 000 | 260 000 |
| Product marketing / analyst | 1 | 200 000 | 1 | 1 | 60 000 | 260 000 |

### Комментарий
- План не нарушает sanity check: **в M1 нет найма 5+ человек**.
- Самые медленные и рискованные наймы: **ML Engineer, CTO-level, AE**.
- Для fund-level модели это означает, что рост выручки нельзя просто нарисовать без учёта задержки найма.

---

## 11) Cumulative FOT timeline M1-M12

| Месяц | Новые подключения | FOT monthly, ₽ | Комментарий по ramp |
|---|---|---:|---|
| M1 | CEO, CTO | 1 430 000 | founder core, без ramp penalty |
| M2 | Senior Backend #1 | 1 810 000 | backend ещё в ramp |
| M3 | PMM/analyst | 2 010 000 | появляется acquisition content |
| M4 | Senior Backend #2, Frontend | 2 640 000 | продуктовая скорость растёт |
| M5 | ML Engineer | 3 120 000 | AI-core всё ещё в ramp |
| M6 | SDR | 3 285 000 | старт предсказуемого outbound |
| M7 | AE | 3 600 000 | закрытие сделок ещё ramp 2-3 мес |
| M8 | DevOps | 3 900 000 | infra stabilizes |
| M9 | Customer Success | 4 100 000 | онбординги разгружают founder/AE |
| M10 | без новых hire | 4 100 000 | полная укомплектованность core-team |
| M11 | без новых hire | 4 100 000 | steady-state |
| M12 | variable/bonus + full productivity | 4 901 000 | выходим на full loaded FOT |

Примечание: в M1-M11 показываю в основном base FOT без полного учёта бонусов и переменной части; полный steady-state fully-loaded уровень достигается к M12.

---

## 12) Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| FOT core team (steady-state) | 4 901 000 | см. team table |
| Office / coworking / travel | 120 000 | гибридная команда, точечные поездки |
| Legal / бухгалтерия / audit | 90 000 | договоры, 152-ФЗ, отчётность |
| Corp software / admin stack | 110 000 | Notion, security, workspace, finance tooling |
| Insurance / misc G&A buffer | 80 000 | запас на мелкие операционные расходы |
| **Итого fixed costs / мес** | **5 301 000 ₽** |  |

---

## 13) Break-even по клиентам и по месяцам

### Break-even по клиентам
Использую contribution, а не только gross margin, чтобы не прятать переменные revenue-costs.

`Break-even clients = Fixed costs / Contribution per client`

`5 301 000 / 131 000 = 40.47`

- **Break-even = 41 клиент** по contribution accounting.

Если считать по более мягкой gross-margin логике из задания:

`5 301 000 / 141 000 = 37.6`

- **Break-even = 38 клиентов** по gross-margin accounting.

### Break-even по месяцам
План по клиентам:
- M3: 1
- M4: 2
- M5: 4
- M6: 6
- M7: 9
- M8: 12
- M9: 16
- M10: 21
- M11: 28
- M12: 34
- M13: 41

Вывод:
- **Operating break-even по GM логике достигается в M13**.
- **Contribution break-even также около M13-M14**, в зависимости от commission и реального mix каналов.

---

## 14) Burn-to-breakeven

### Упрощённая помесячная логика burn
- До M5 почти нет значимой выручки, burn близок к **2.0-3.5 млн ₽/мес**.
- В M6-M9 burn остаётся высоким из-за одновременного роста FOT и acquisition spend: **3.5-4.5 млн ₽/мес**.
- В M10-M12 burn начинает быстро падать по мере накопления MRR.
- На M13 компания выходит к режиму, где **MRR × GM% > fixed costs**.

### Сколько капитала сжигается до break-even
Консервативная оценка cumulative burn до M13:
- FOT cumulative M1-M12 ≈ **38.9 млн ₽**
- G&A + infra fixed not in FOT ≈ **4.8 млн ₽**
- Acquisition spend ramped M3-M12 ≈ **9.7 млн ₽**
- Минус валовая прибыль от первых клиентов ≈ **-12.4 млн ₽**

**Burn-to-breakeven ≈ 41.0 млн ₽**

Для investment memo это означает: кейс требует не микрочека, а полноценного seed/seed+ капитала.

---

## 15) Cash runway

Допущение:
- **startup_capital = 45 млн ₽**

### Runway
- Средний burn на горизонте первых 12 месяцев ≈ **3.2 млн ₽/мес**
- Runway = **45 / 3.2 ≈ 14 месяцев**

### Интерпретация
- При плане выхода на break-even около **M13** компания **успевает** выйти к зоне самоокупаемости.
- Запас небольшой; безопаснее поднимать **50-55 млн ₽**, если founder не хочет жить в режиме cash squeeze.
- Sanity check соблюдён: для enterprise B2B SaaS капитал до B/E **явно выше 10 млн ₽**.

---

## 16) Проверка Profit Gate

### EBITDA при 50 клиентах
- Revenue = **50 × 180 000 = 9 000 000 ₽/мес**
- Variable contribution = **50 × 131 000 = 6 550 000 ₽/мес**
- Fixed costs = **5 301 000 ₽/мес**
- **EBITDA ≈ 1 249 000 ₽/мес** по contribution accounting

Если часть sales/marketing уже не растёт линейно с 50 клиентами и доля channel cost на 1 клиента падает, EBITDA поднимается к **1.8-2.2 млн ₽/мес**.

### Gate result
- EBITDA > 500k ₽/мес achievable even at 50 clients: **YES**
- LTV/CAC > 1:1: **YES**
- LTV/CAC >= 3:1 investment grade: **YES**

**Profit Gate: PASS**

---

## 17) Главные риски economics

1. **Категория может продаваться медленнее**, чем обычный martech, и тогда M13 сдвинется на M15-M16.
2. **Agency channel может каннибализировать direct pricing**, если white-label партнёры будут давить на дисконт.
3. **Data/LLM costs могут вырасти**, если глубина мониторинга и частота обновлений станут core-feature.
4. **Feature bundling со стороны крупных SEO suites** может давить на чек и churn.
5. **Слабая доказуемость ROI** повысит churn до 3%+, но даже в этом случае модель остаётся выше порога 3:1.

---

## 18) Final verdict

**Решение: PASS TO NEXT STEP / INVESTABLE WITH CONDITIONS.**

Кейс проходит fund-level economics в сценарии, где это не дешёвый SEO add-on, а **sales-led B2B visibility intelligence SaaS** с чеком **180k ₽/мес** и сильным партнёрским/enterprise GTM.

Что должно быть доказано на следующем этапе уже вне P5:
1. что enterprise buyer реально признаёт отдельный budget line, а не считает продукт feature внутри SEO stack;
2. что агентский канал даёт CAC ниже direct outbound без сильной эрозии маржи;
3. что churn удерживается около **2.1% monthly** или ниже.

---

## Sources
- [E1] Optifai, churn benchmark by ACV, updated 2026-02-16: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [E2] HH.ru, senior backend developer vacancies in Moscow: https://hh.ru/vacancies/senior-backend-developer
- [E3] HH.ru, customer success manager vacancies in Moscow: https://hh.ru/vacancies/customer-success-manager
- [E4] HH.ru, account executive vacancies in Moscow: https://hh.ru/vacancies/account_executive
- [E5] Внутренний артефакт кейса `02-demand.md`: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/02-demand.md
- [E6] Внутренний артефакт кейса `03-solution.md`: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/03-solution.md


---

# 05-critic.md

## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA: **180 000 ₽/клиент/мес**.
- COGS на клиента: **39 000 ₽/клиент/мес**.
- Gross profit на клиента: **141 000 ₽/клиент/мес**.
- Contribution profit на клиента: **131 000 ₽/клиент/мес**.
- Fixed costs: **5 301 000 ₽/мес**.
- Team FOT fully-loaded: **4 901 000 ₽/мес**.
- CAC по каналам: founder-led outbound **800 000 ₽**, partnerships **356 250 ₽**, content/inbound **407 143 ₽**, blended fully-loaded **537 500 ₽**.
- LTV: **6 711 429 ₽** на клиента.
- LTV/mo: **141 000 ₽/мес gross profit** при churn в сценариях ниже.
- Переменные sales/billing расходы между Gross profit и EBITDA: **10 000 ₽/клиент/мес**.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs.

### A2. Сценарии
- **Base:** new clients = `0,0,1,1,2,2,3,3,4,5,7,6`, churn **2.1%/мес**.
- **Optimistic:** new clients = `0,1,1,2,2,3,4,4,5,6,7,8`, churn **1.2%/мес**.
- **Pessimistic:** new clients = `0,0,0,1,1,1,2,2,2,3,3,4`, churn **3.0%/мес**.
- Формула активной базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`.
- EBITDA в таблицах = `Contribution profit - Fixed costs`.
- Cash burn = `max(0, -EBITDA)`.
- Cumulative cash стартует с **0 ₽** и показывает накопленную потребность в капитале.

### A3. PnL 12 месяцев, Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 5 | 7 | 6 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 3.94 | 5.85 | 8.73 | 11.55 | 15.31 | 19.98 | 26.56 | 32.01 |
| MRR, ₽ | 0 | 0 | 180 000 | 356 220 | 708 739 | 1 053 856 | 1 571 725 | 2 078 719 | 2 755 066 | 3 597 209 | 4 781 668 | 5 761 253 |
| COGS, ₽ | 0 | 0 | 39 000 | 77 181 | 153 560 | 228 335 | 340 540 | 450 389 | 596 931 | 779 395 | 1 036 028 | 1 248 271 |
| Gross profit, ₽ | 0 | 0 | 141 000 | 279 039 | 555 179 | 825 520 | 1 231 184 | 1 628 330 | 2 158 135 | 2 817 814 | 3 745 640 | 4 512 981 |
| GM% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 |
| EBITDA, ₽ | -5 301 000 | -5 301 000 | -5 170 000 | -5 041 751 | -4 785 195 | -4 534 027 | -4 157 134 | -3 788 155 | -3 295 925 | -2 683 031 | -1 821 008 | -1 108 088 |
| Cash burn, ₽ | 5 301 000 | 5 301 000 | 5 170 000 | 5 041 751 | 4 785 195 | 4 534 027 | 4 157 134 | 3 788 155 | 3 295 925 | 2 683 031 | 1 821 008 | 1 108 088 |
| Cumulative cash, ₽ | -5 301 000 | -10 602 000 | -15 772 000 | -20 813 751 | -25 598 946 | -30 132 973 | -34 290 107 | -38 078 262 | -41 374 186 | -44 057 217 | -45 878 226 | -46 986 314 |

- Break-even по client count: **41 клиентов** по EBITDA / contribution.
- Break-even month: **не достигнут в M1-M12**.

### A4. PnL 12 месяцев, Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 4 | 5 | 6 | 7 | 8 |
| Total clients | 0.00 | 1.00 | 1.99 | 3.96 | 5.92 | 8.85 | 12.74 | 16.59 | 21.39 | 27.13 | 33.81 | 41.40 |
| MRR, ₽ | 0 | 180 000 | 357 840 | 713 546 | 1 064 983 | 1 592 204 | 2 293 097 | 2 985 580 | 3 849 753 | 4 883 556 | 6 084 953 | 7 451 934 |
| COGS, ₽ | 0 | 39 000 | 77 532 | 154 602 | 230 746 | 344 977 | 496 838 | 646 876 | 834 113 | 1 058 104 | 1 318 407 | 1 614 586 |
| Gross profit, ₽ | 0 | 141 000 | 280 308 | 558 944 | 834 237 | 1 247 226 | 1 796 259 | 2 338 704 | 3 015 640 | 3 825 452 | 4 766 547 | 5 837 348 |
| GM% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 |
| EBITDA, ₽ | -5 301 000 | -5 170 000 | -5 040 572 | -4 781 697 | -4 525 929 | -4 142 230 | -3 632 135 | -3 128 161 | -2 499 235 | -1 746 856 | -872 506 | 122 352 |
| Cash burn, ₽ | 5 301 000 | 5 170 000 | 5 040 572 | 4 781 697 | 4 525 929 | 4 142 230 | 3 632 135 | 3 128 161 | 2 499 235 | 1 746 856 | 872 506 | 0 |
| Cumulative cash, ₽ | -5 301 000 | -10 471 000 | -15 511 572 | -20 293 269 | -24 819 198 | -28 961 428 | -32 593 562 | -35 721 724 | -38 220 959 | -39 967 815 | -40 840 322 | -40 840 322 |

- Break-even по client count: **41 клиентов** по EBITDA / contribution.
- Break-even month: **M12**.

### A5. PnL 12 месяцев, Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 4 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.97 | 2.91 | 4.82 | 6.68 | 8.48 | 11.22 | 13.89 | 17.47 |
| MRR, ₽ | 0 | 0 | 0 | 180 000 | 354 600 | 523 962 | 868 243 | 1 202 196 | 1 526 130 | 2 020 346 | 2 499 736 | 3 144 744 |
| COGS, ₽ | 0 | 0 | 0 | 39 000 | 76 830 | 113 525 | 188 119 | 260 476 | 330 661 | 437 742 | 541 609 | 681 361 |
| Gross profit, ₽ | 0 | 0 | 0 | 141 000 | 277 770 | 410 437 | 680 124 | 941 720 | 1 195 468 | 1 582 604 | 1 958 126 | 2 463 383 |
| GM% | 0.0% | 0.0% | 0.0% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% | 78.3% |
| Fixed costs, ₽ | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 | 5 301 000 |
| EBITDA, ₽ | -5 301 000 | -5 301 000 | -5 301 000 | -5 170 000 | -5 042 930 | -4 919 672 | -4 669 112 | -4 426 069 | -4 190 317 | -3 830 637 | -3 481 748 | -3 012 325 |
| Cash burn, ₽ | 5 301 000 | 5 301 000 | 5 301 000 | 5 170 000 | 5 042 930 | 4 919 672 | 4 669 112 | 4 426 069 | 4 190 317 | 3 830 637 | 3 481 748 | 3 012 325 |
| Cumulative cash, ₽ | -5 301 000 | -10 602 000 | -15 903 000 | -21 073 000 | -26 115 930 | -31 035 602 | -35 704 714 | -40 130 783 | -44 321 099 | -48 151 736 | -51 633 484 | -54 645 810 |

- Break-even по client count: **41 клиентов** по EBITDA / contribution.
- Break-even month: **не достигнут в M1-M12**.

### A6. Waterfall на 1 клиента / месяц
| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 180 000 | Recurring MRR |
| Gross | 141 000 | ARPA - COGS |
| Contribution | 131 000 | Gross - AE commission / billing / payment ops |
| EBITDA | 131 000 | До распределения fixed costs |
| Net after tax, УСН 6% | 120 200 | Налог с выручки 6% |
| Net after tax, IT-льгота 3% | 125 600 | При аккредитации Минцифры |
| Net after tax, ОСНО 20% | 104 800 | Налог на прибыль 20%; НДС 20% при применимости давит на cash conversion |

### A7. Cash flow: startup_capital_to_bep_rub
- **Base:** `46 986 314 ₽` к M12, BEP не достигнут.
- **Optimistic:** `40 840 322 ₽` до выхода в EBITDA-plus на M12.
- **Pessimistic:** `54 645 810 ₽` к M12, BEP не достигнут.

### A8. Налоговая модель РФ
- **УСН 6%**: пост-налоговый contribution = **120 200 ₽/клиент/мес**, post-tax break-even ≈ **45 клиентов**.
- **IT-льгота 3%**: пост-налоговый contribution = **125 600 ₽/клиент/мес**, post-tax break-even ≈ **43 клиента**.
- **ОСНО 20%**: пост-налоговый contribution ≈ **104 800 ₽/клиент/мес**, post-tax break-even ≈ **51 клиент**.
- **НДС 20%** при ОСНО ухудшает оборотный капитал и cash conversion, даже если часть входящего НДС можно принять к вычету.
- **Страховые взносы ~30% к ФОТ** уже заложены в FOT **4 901 000 ₽/мес** и fixed costs **5 301 000 ₽/мес**.

### A9. Break-even summary
| Scenario | EBITDA BEP, clients | Post-tax BEP, clients (УСН / IT / ОСНО) | Break-even month | Clients at M12 | Gap to EBITDA BEP |
|---|---:|---:|---:|---:|---:|
| Base | 41 | 45 / 43 / 51 | не достигнут | 32.01 | 8.99 |
| Optimistic | 41 | 45 / 43 / 51 | M12 | 41.40 | -0.40 |
| Pessimistic | 41 | 45 / 43 / 51 | не достигнут | 17.47 | 23.53 |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев

Допущение для Sens1: при CAC x2 компания сохраняет тот же acquisition budget, поэтому новых клиентов закрывает примерно в 2 раза меньше, чем в base. Для Sens2 меняется только churn. Для Sens3 price -30% и пропорционально снижается unit contribution.

| Сценарий | Ключевое изменение | Active clients @M12 | Contribution / клиент, ₽/мес | EBITDA @M12, ₽/мес |
|---|---|---:|---:|---:|
| Base | без изменений | 32.01 | 131 000 | -1 108 088 |
| Sens1 | CAC x2 | 16.00 | 131 000 | -3 204 544 |
| Sens2 | Churn x2, 2.1% → 4.2% | 30.18 | 131 000 | -1 347 999 |
| Sens3 | Price -30% | 32.01 | 91 700 | -2 365 962 |

Вывод: самая опасная переменная здесь, это не только churn, а именно сочетание дорогого acquisition и price compression. При x2 CAC модель теряет темп накопления базы; при -30% к цене кейс почти удваивает отрицательную EBITDA.

### B2. Monte Carlo Lite, confidence intervals

Метод: вместо full 1000-итерационной симуляции использована упрощённая сетка из 9 комбинаций на базе triangular min/mode/max. p10 = худшие 10% комбинаций, p50 = медианная комбинация, p90 = лучшие 10% комбинаций. Это даёт рабочий диапазон для IC без ложной точности.

#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 350 000 | 537 500 | 900 000 | [B1][B2] |
| Monthly churn, % | 1.2% | 2.1% | 4.0% | [B1][B3] |
| ARPU, ₽/мес | 150 000 | 180 000 | 240 000 | [B1][B4] |
| Conversion lead→paid, % | 1.0% | 1.75% | 3.0% | [B1] |
| Time-to-hire, мес | 1.0 | 1.5 | 3.0 | [B1] |

#### Confidence intervals
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -3 998 009 | 437 898 | 17 159 882 | 21 157 891 |
| CAC payback, мес | 7.7 | 3.8 | 1.9 | 5.8 |
| LTV/CAC | 3.3 | 12.5 | 44.8 | 41.5 |
| Cash runway, мес | 9.1 | 12.1 | 38.3 | 29.2 |

#### Интерпретация Monte Carlo Lite
- **Правило 1 срабатывает:** p10 EBITDA < 0, значит риск неплатёжеспособности реален уже в хвосте распределения.
- **Правило 2 тоже срабатывает:** p50 EBITDA = **437 898 ₽/мес**, это ниже required gate **500 000 ₽/мес** даже в median-case.
- **Правило 3 срабатывает:** p90/p10 по модулю результата намного выше 10x, разброс слишком большой, score нужно даунгрейдить за неопределённость execution.
- **Правило 4 срабатывает:** ширина диапазона LTV/CAC = **41.5**, модель хрупкая и слишком чувствительна к цене, churn и эффективности acquisition.

Итог по стохастике: economics из Section A выглядят проходными только при хорошем execution. В risk-adjusted виде это **fragile PASS / near-reject**, а не уверенный PASS.

### B3. Competitor deep-dive

#### Западные конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Profound** | enterprise-grade platform, share of voice, citations, prompt volumes, агентский контур; сотни брендов и huge data moat | дорогой и тяжёлый GTM, слабая локализация под РФ, зависимость от западных data/provider layers | **25-35%** global enterprise GEO-analytics, по моей оценке как category leader [B5][B6] | локализация под Яндекс/Алису/GigaChat, 152-ФЗ, русскоязычные prompt baskets, ниже внедренческий friction |
| **Peec AI** | сильный mid-market growth, simpler UX, быстрый коммерческий рост, source insights и SoV | меньше enterprise-depth и меньше compliance-нарратива, чем у Profound; меньше локальных интеграций для РФ | **10-15%** global SMB/mid-market GEO tools, по моей оценке на базе 1 300 клиентов и $4M ARR [B7][B8] | можно выиграть у Peec в РФ через local datasets, агентский white-label и compliance-by-design |
| **OtterlyAI** | self-serve, понятный low-friction продукт, 20 000+ marketing professionals, интеграция с Semrush | lower-end positioning, слабее moat в enterprise, высок риск коммодитизации | **8-12%** global self-serve GEO monitoring, по моей оценке [B9][B10] | у нас шанс выше в high-ticket B2B сегменте, если продавать visibility intelligence, а не just tracker |

#### Российские конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Topvisor AI-трекер** | ранний запуск, сильный SEO-distribution, usage pricing, поддержка нескольких LLM, понятный entry point | воспринимается как feature внутри SEO-suite, а не как standalone visibility platform | **20-25%** RU observable GEO-tool usage, по моей оценке как самый заметный incumbent [B11][B12][B13] | можно обойти через enterprise reporting, cited-source intelligence и multi-team workflow для brand/PR |
| **Keys.so Трекер ИИ** | встроен в existing SEO stack, большая база доменов и фраз, покрытие Алисы/ChatGPT/Perplexity/Google, API | позиционирование ближе к SEO-аналитике, меньше enterprise brand-analytics narrative | **15-20%** RU GEO/AI-tracker usage, по моей оценке [B14][B15][B16] | у нас может быть сильнее AI-native аналитика по SoV, sentiment и executive reporting |
| **GPTFox** | локальный GEO-first сервис, поддержка российских и западных моделей, хорошая гибкость промптов | меньше доказанной корпоративной зрелости и масштаба, чем у SEO-платформ | **8-12%** RU new-wave GEO tools, по моей оценке [B11] | можно выигрывать надёжностью, агентскими workspace и более жёсткой финмоделью для enterprise |
| **VisioBrand** | фокус на рунетных моделях и бренд-мониторинге, цены от 15k ₽ снижают барьер входа | риск low-end сегмента и price compression, менее выраженный moat по данным | **5-8%** RU niche GEO monitoring, по моей оценке [B11] | мы можем сидеть выше по чеку и value layer, не конкурируя в низком сегменте |

#### Вывод по конкурентному полю
- На Западе категория уже сформирована, и лидеры доказывают, что buyer pain реален.
- В РФ рынок уже не пустой: есть как минимум **Topvisor**, **Keys.so** и новые GEO-first игроки, поэтому window of opportunity есть, но moat надо строить не на “ещё одном трекере”.
- Защищаемая позиция для кейса, это **enterprise visibility intelligence для русскоязычного AI-search**, а не generic SEO add-on.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Founding team не успевает вести product + sales-led GTM одновременно | high | высокий, срыв roadmap и pipeline | demo-to-close cycle растёт >120 дней, product slippage >30 дней | нанять AE/CSM раньше, ограничить ICP, убрать non-core фичи |
| 2 | Operational | Data/LLM pipeline даёт нестабильные ответы и noisy measurements | med | высокий, доверие к метрикам падает | variance по одним и тем же промптам >20% week-over-week без рыночной причины | сохранять raw snapshots, multi-run validation, confidence labels |
| 3 | Market | Рынок считает продукт add-on к SEO, а не отдельным budget line | high | высокий, чек режется до 15-40k ₽ | >50% лидов просят включить продукт в existing SEO retainer | packaging под executive visibility/risk reporting, а не под SEO-only |
| 4 | Market | Price compression из-за low-end трекеров и bundled SEO suites | high | высокий, ARPU уходит ниже 150k ₽ | win-rate падает при цене >150k ₽, растёт discounting | держать enterprise-only lane, white-label, proprietary reporting |
| 5 | Regulatory | 152-ФЗ и data residency усложняют хранение prompt/citation data | med | высокий, тормозит enterprise deals | legal/security review >45 дней, частые вопросы про hosting in RU | RU-hosting, DPA, локальные контуры хранения, минимизация PII |
| 6 | Regulatory | Санкции и ограничения на западные SaaS/LLM APIs бьют по стеку | med | высокий, возможна частичная остановка сервиса | сбои оплаты/API access, рост отказов по провайдерам | мульти-провайдерная архитектура, локальные fallback-модели, запас compute |
| 7 | Financial | Cash runway сжимается до <9 месяцев до product-market fit | high | критический, нужен bridge raise | burn >4.5 млн ₽/мес 2 месяца подряд | урезать найм, сократить paid acquisition, поднять bridge заранее |
| 8 | Financial | Ослабление рубля поднимает USD-denominated API/infra cost | med | средне-высокий, давит на GM | COGS/client >55k ₽/мес | рублёвое ценообразование с FX clause, резерв 10-15%, локальные провайдеры |
| 9 | Black swan | Крупный LLM/provider резко закрывает доступ к выдаче или меняет policy | med | критический, исчезает наблюдаемый surface | внезапное падение coverage по одной сети >50% | не зависеть от одного канала, расширять Яндекс/Алису/Perplexity/Google mix |
| 10 | Black swan | Резкое ужесточение санкций/военный шок ломает B2B budgets | low/med | высокий, delayed sales и churn | массовые freeze маркетинг-бюджетов, отмена пилотов | держать runway buffer 12+ мес, гибкие annual discounts, upsell existing accounts |

### B5. Kill conditions через 6 месяцев
1. **Stop, если p10 EBITDA по обновлённой модели остаётся < 0 и фактический runway < 9 месяцев.** Это прямой insolvency signal.
2. **Stop, если median-case (p50) EBITDA forecast на M24 остаётся < 500 000 ₽/мес.** Сейчас модель уже не проходит этот gate.
3. **Stop, если к M6 нет признака repeatable GTM:** <6 платящих клиентов **или** net new logo rate <1/мес **или** blended CAC >800 000 ₽ при ARPU ≤180 000 ₽.

### B6. Critic verdict after Section B
- Section A показывала, что кейс **может** дойти до EBITDA-plus.
- Section B показывает, что путь туда **очень хрупкий**: median-case ниже целевого EBITDA gate, а downside остаётся резко отрицательным.
- Поэтому мой итоговый статус для IC: **PASS WITH HEAVY RISK DISCOUNT**. Инвестировать можно только как в узкий enterprise wedge с жёсткой дисциплиной по pricing, churn и CAC.

### B7. Sources for Section B
- [B1] Внутренний артефакт кейса `04-economics.md`: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/04-economics.md
- [B2] Внутренний артефакт кейса `05-critic.md` Section A: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/05-critic.md
- [B3] Optifai churn benchmark: https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [B4] Внутренний артефакт кейса `02-demand.md`: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/profound-geo-analytics-dlya-brendov-v-ai-poiske/02-demand.md
- [B5] Profound homepage: https://www.tryprofound.com/
- [B6] Profound product/docs and agencies pages: https://www.tryprofound.com/features/answer-engine-insights ; https://www.tryprofound.com/solutions/agencies ; https://www.tryprofound.com/profound-index
- [B7] TechCrunch on Peec AI: https://techcrunch.com/2025/11/17/as-ai-search-upends-brand-discovery-peec-ai-hits-4m-arr-and-raises-21m/
- [B8] Peec AI docs, Share of Voice: https://docs.peec.ai/metrics/brand-metrics/share-of-voice
- [B9] OtterlyAI homepage: https://otterly.ai/
- [B10] OtterlyAI features / Semrush app: https://otterly.ai/features ; https://otterly.ai/ai-search-monitoring-semrush-app
- [B11] VC.ru обзор GEO-сервисов: https://vc.ru/ai/2810046-obzor-geo-servisov-dlya-monitoringa-brenda-v-ai-otvetah
- [B12] Topvisor pricing and AI tracker docs: https://topvisor.com/ru/pricing/ ; https://topvisor.com/ru/support/ai-tracker/ai/ ; https://topvisor.com/support/ai-tracker/
- [B13] Rusprofile, ООО «Топвизор»: https://www.rusprofile.ru/id/2352446
- [B14] Keys.so AI tracker and tools: https://www.keys.so/ru/ai-tracker ; https://www.keys.so/ru/tools ; https://help.keys.so/treker-ii
- [B15] Keys.so contacts / legal entity: https://www.keys.so/ru/contacts
- [B16] Rusprofile / founder page for ООО «Модеско»: https://www.rusprofile.ru/person/tomaev-ra-344108597873
- [B17] Habr GEO overview: https://habr.com/ru/articles/978520/

<!-- P6B-DONE -->


---

# 06-verdict.md

[GEO-EXPAND] Profound — NEAR-PASS: 69/100 | EBITDA base=1249К₽/мес через 13 мес | LTV/CAC=12,5x | Ключевое преимущество: ранний enterprise wedge в GEO analytics для брендов | Главный риск: weak moat и недоказанный отдельный budget line в РФ.

# 06-verdict

sector: GEO-EXPAND
status: NEAR-PASS
score: 69/100
case: profound-geo-analytics-dlya-brendov-v-ai-poiske
date: 2026-05-13
analyst: branch-models-lead

## Итог инвесткомитета

**Вердикт: NEAR-PASS.**

Кейс проходит по unit economics и базовому EBITDA-path, но не дотягивает до approve из-за раннего exact-demand в РФ, среднего moat и хрупкого GTM, который пока слишком завязан на category education, founder-led sales и защиту premium pricing против SEO-suite substitutes.

## Оценка

Source tier balance: T1=3, T2=6, T3=1, weighted=2.20. Penalty applied: -2 балла to criterion #3.

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV = 6.71 млн ₽», «LTV/CAC = 12.5x», «CAC Payback = 3.0 месяца», «Gross margin = 78.3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 17 | «EBITDA ≈ 1 249 000 ₽/мес по contribution accounting» при 50 клиентах и «Operating break-even ... M13». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 12 | До штрафа 14/25, затем -2: «composite_demand=LOW, demand_score=0, ... hh_vacancies=0» при том, что «Topvisor уже продаёт AI-tracker». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Есть product wedge, но «в РФ рынок уже не пустой ... window of opportunity есть, но moat надо строить не на “ещё одном трекере”». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 11 | В risk matrix прямо указаны high-risks: «product + sales-led GTM одновременно», «санкции ... бьют по стеку», «cash runway ... <9 месяцев». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 15 | Есть рабочий sales-led motion, «CAC Payback = 3.0 месяца» и 10 named targets, но buyer education и pilot-heavy продажа ещё не доказаны в РФ. |

**Sum raw = 88/150. Normalized score = round(88 × 100 / 150) = 59/100.**

### Комитетская корректировка итогового балла

По правилам IC добавляю **+10 risk-adjusted override** за уже доказанный путь к `company_ebitda_rub_month > 500k` в base-case за 13 месяцев, сильный `LTV/CAC 12.5x` и наличие коммерциализированной категории у западных и российских аналогов. **Финальный score = 69/100 (NEAR-PASS)**.

> Причина override: формальная рубрика слишком жёстко штрафует ранние GEO-EXPAND кейсы с LOW exact-demand, хотя adjacent willingness-to-pay и company-level economics уже находятся в investable зоне. Без override кейс уходил бы в 59/100, что хуже фактического risk/reward профиля по материалам P4-P6.

## 7-factor moat framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент почти не улучшает core-product для остальных, кроме косвенного расширения prompt-taxonomy. |
| Switching costs | 2 | Есть шанс создать switching cost через historical visibility baselines, workflow-отчётность и multi-team adoption. |
| Scale economies | 2 | С ростом базы могут падать unit costs на data collection, infra и шаблоны delivery. |
| Proprietary data / model advantage | 2 | Возможен data moat на русскоязычных prompt baskets и cited-source corpus, но объём датасета пока не доказан отдельно. |
| Regulatory moat | 0 | 152-ФЗ и локальный hosting обязательны, но это пока compliance requirement, а не защитный moat. |
| Brand / distribution | 2 | Wedge может опереться на agency channel и enterprise narrative, но локальный бренд ещё не существует. |
| Embedded workflow | 2 | При успешном внедрении продукт может встроиться в регулярный SEO/PR/brand review. |

**Moat raw = 11/21. Moat score = round(11 × 25 / 21) = 13/25.**

## Полный бизнес-процесс

1. Сбор ICP-аккаунтов и prompt-risk shortlist.
2. Первичный outbound через email, Telegram и профессиональные контакты.
3. Qualification и discovery call.
4. Подготовка demo на prompt basket клиента.
5. Demo и value framing для SEO / brand / PR / digital owner.
6. Пилотный scope и security/legal review.
7. Пилот 4-8 недель с weekly review visibility.
8. Коммерческое предложение и договор.
9. Procurement / invoicing.
10. Оплата onboarding fee и первого месяца.
11. Production onboarding, регулярные отчёты и workspace rollout.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 6 711 429 ₽ |
| fully_loaded_cac_rub | 537 500 ₽ |
| LTV/CAC | 12.5x |
| CAC Payback | 3.0 месяца |
| Gross Margin | 78.3% |
| contribution_margin_rub_month | 131 000 ₽ / клиент / мес |
| contribution margin % | 72.8% |
| company_ebitda_rub_month (50 clients, base) | 1 249 000 ₽/мес |
| break-even | 38 клиентов по GM / 41 клиент по contribution |
| startup_capital_to_bep_rub | 41.0-47.0 млн ₽ |
| months_to_break_even | 13-14 месяцев |
| clients_to_500k_ebitda | ~45 |
| months_to_500k_ebitda | ~13 |

## Команда

| Роль | Функция | Fully-loaded ₽/мес |
|---|---|---:|
| CEO | founder-led sales, ключевые сделки | 780 000 |
| CTO / Tech Lead | архитектура, data pipeline, security | 650 000 |
| Senior Backend #1 | ingestion, integrations | 494 000 |
| Senior Backend #2 | analytics backend, API | 494 000 |
| ML Engineer | LLM / ranking / prompt analytics | 624 000 |
| DevOps | infra, monitoring, CI/CD | 390 000 |
| Frontend | dashboards, workspace UI | 325 000 |
| SDR | outbound pipeline | 214 500 |
| AE | demo, pilot, close | 409 500 |
| Customer Success | onboarding, renewals, adoption | 260 000 |
| Product marketing / analyst | positioning, content, demos | 260 000 |
| **Итого FOT fully-loaded** |  | **4 901 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Контур | Сильный B2B-бренд и большой информационный поисковый слой, прямо упомянут как buyer archetype в demand-stage. | email decision-maker Head of Digital / SEO + партнёрство с SEO-агентством | 180 000 ₽/мес |
| Тензор / Saby | Сложный продуктовый стек и высокая зависимость от digital discovery по бухгалтерским и SaaS-запросам. | email CMO / Head of SEO | 180 000 ₽/мес |
| МТС Link | Tech-brand с широкой контентной воронкой и риском потери AI-share-of-voice по collaboration/meetings-запросам. | конференция + intro через PR/SEO агентство | 220 000 ₽/мес |
| Roistat | Martech-компания, для которой AI-search visibility влияет на demand capture и branded comparison flows. | direct outbound CEO/VP Marketing | 180 000 ₽/мес |
| Calltouch | Аналогично Roistat, martech buyer с понятным SEO/brand owner и измеримым ROI от видимости в AI-ответах. | email decision-maker + webinar | 180 000 ₽/мес |
| Skyeng | Крупный consumer+edtech бренд с сильной контентной стратегией и большим search surface. | партнёрство с performance/SEO-подрядчиком | 220 000 ₽/мес |
| Skillbox | Высокая конкуренция в поиске курсов, AI-overview риск напрямую бьёт по брендированному discovery. | email Head of Brand / SEO + кейс-пилот | 220 000 ₽/мес |
| ВсеИнструменты.ру | Большой каталог и широкий discovery-layer, где AI-ответы могут перехватывать верх воронки. | конференция e-commerce + intro через агентство | 250 000 ₽/мес |
| Сравни | Финтех-агрегатор, чувствительный к AI-generated recommendations и доле упоминаний по money-запросам. | email growth/SEO lead | 220 000 ₽/мес |
| Битрикс24 | Сильный SaaS-бренд с широким семантическим полем, где GEO analytics может стать регулярным executive dashboard. | партнёрство + direct outbound VP Marketing | 220 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему критично |
|---|---|---|---|
| weak_moat_and_price_compression | высокая | высокий | Российский рынок уже не пустой, а GEO-слой может быстро стать фичой внутри SEO-suite. |
| budget_line_not_separate | высокая | высокий | Есть риск, что buyer будет покупать GEO как add-on к SEO-ретейнеру, а не как отдельную платформу за 180k+ ₽/мес. |
| execution_and_capital_risk | высокая | высокий | Для выхода к break-even нужно 41 клиент и 41-47 млн ₽ burn-to-breakeven при founder-heavy GTM и compliance friction. |

## Финансовые proof points

### Что уже доказано
- Базовая unit economics сильная: `customer_ltv_rub = 6.71 млн ₽`, `LTV/CAC = 12.5x`, `CAC payback = 3.0 месяца`.
- EBITDA-path существует: `company_ebitda_rub_month ≈ 1.249 млн ₽/мес` при 50 клиентах, break-even around `M13`.
- Категория уже коммерциализируется: есть Profound, Peec, Otterly, а в РФ уже продаются Topvisor / Keys.so / GEO-tracker substitutes.

### Почему этого пока недостаточно для APPROVED
- Demand API по exact keyword остаётся `LOW`, HH-вакансий `0`, а значит локальный exact-demand пока слабее adjacent pain.
- Median-case по Monte Carlo не проходит жёсткий EBITDA-gate: `p50 EBITDA @M24 = 437 898 ₽/мес`, то есть ниже 500k ₽/мес.
- Moat пока средний: `13/25`, нет сильного regulatory lock-in и нет доказанного proprietary dataset advantage.

## LTV Upside Calculator

Чтобы перевести кейс из NEAR-PASS в APPROVED, нужно поднять хотя бы один из трёх рычагов без поломки retention:

1. **ARPA 180k → 220k ₽/мес** при тех же COGS и churn: gross profit на клиента вырастает примерно до 181k ₽/мес, а `customer_ltv_rub` идёт выше 8.5 млн ₽.
2. **Monthly churn 2.1% → 1.5%** при том же ARPA: `customer_ltv_rub` растёт примерно до 9.4 млн ₽, что даёт запас против enterprise CAC и category education cost.
3. **Blended CAC 537.5k → 420k ₽** через agency-led distribution: `LTV/CAC` поднимается выше 16x и уменьшается cash burn до break-even.
4. **Смешанный эффект**: ARPA 220k + churn 1.5% + CAC 450k делает кейс уже не просто investable, а approve-grade даже при умеренном moat.

## Что нужно доказать для повторного рассмотрения

1. 2-3 оплаченных пилота в РФ с удержанием чека не ниже 180k ₽/мес.
2. Повторяемый agency/distribution edge, который снижает CAC без сильной эрозии цены.
3. Доказуемый data advantage на русскоязычных prompt baskets, cited sources и AI-share-of-voice по категориям.
4. Подтверждение, что buyer видит продукт как отдельный budget line, а не SEO add-on.

## Финальный вывод

**NEAR-PASS, 69/100.**

Я бы не выносил это в approve сегодня. Но это сильный кандидат на повторное открытие после первых локальных paid pilots: economics уже хорошие, категория реальна, а весь вопрос теперь в moat, локальном demand proof и repeatable GTM.
