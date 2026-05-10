---
sector: QUICK-AI
stage: demand-validation
updated: 2026-05-10T20:33:00+03:00
verdict: REJECTED
confidence: medium
---

# 02-demand

## Demand validation summary
- **Продукт**: быстрый AI-сервис генерации headshots и портретов из селфи для резюме, соцсетей, маркетплейсов и личного бренда. [T2][T3]
- **Итог по спросу в РФ**: **LOW**. Категория узнаваема глобально, но в РФ пока слабо выражена как самостоятельный платёжный спрос. Demand API по ключу `ai headshots` вернул `composite_demand=LOW`, `hh_vacancies=2`, `habr_articles=2`, `yandex_suggest=100`, что больше похоже на ранний curiosity-signal, чем на зрелую локальную категорию. [T2]
- **Решение по гейту**: **EARLY REJECT**. При текущем уровне локального спроса и ценовых якорях по рынку РФ путь к EBITDA компании **500 000 ₽/мес** не выглядит достижимым ни в B2C self-serve, ни в Telegram, ни в micro-B2B пакетах без чрезмерных объёмов продаж. [T2][T3][inference]

## 1. Сигналы спроса

### 1.1. Global category proof есть, но это не равно зрелому локальному спросу
- TechCrunch писал, что после запуска AI headshots у Remini приложение резко выросло в загрузках и consumer spend. Это сильный глобальный сигнал WTP для impulse-покупки. [T2]
- Aragon AI, BetterPic и HeadshotPro продолжают продавать standalone headshot-продукты по фиксированным пакетам, значит сама категория существует как отдельная платная вертикаль. [T3]
- Но в РФ на стороне observable demand сигналов категория пока слабая: внутренний demand API не показывает высокой глубины рынка именно по headshots как самостоятельному JTBD. [T2][inference]

### 1.2. Локальный спрос в РФ ранний и фрагментированный
- Внутренний demand API на **10 мая 2026 года** по ключу `ai headshots` показал: `LOW`, `score=15`, `hh_vacancies=2`, `habr_articles=2`, `yandex_suggest=100`. Это означает, что интерес к формулировке есть, но коммерческая плотность низкая. [T2]
- Проверка RU Telegram / web-игроков показывает наличие предложения, но не наличие крупной категории: локальные сервисы продают разовые пакеты генераций, а не очевидно повторяющуюся подписку. [T3][inference]
- Для consumer-кейса это критично: impulse purchase возможна, но repeat revenue и поисковый pull пока не доказаны. [T2][T3][inference]

## 2. Конкуренты и цены

### Международные конкуренты
| Игрок | Цена | Что продаёт | Вывод |
|---|---:|---|---|
| Aragon AI | от **$29** до **$69** | пакеты AI headshots | сильный глобальный ценовой якорь, но не RU proof [T3] |
| BetterPic | от **$35** | AI headshots | подтверждает отдельную категорию и готовность платить $30+ [T3] |
| HeadshotPro | от **$29** | AI headshots для профиля/LinkedIn | подтверждает demand в западном self-serve сегменте [T3] |

### РФ / RU-friendly конкуренты
| Игрок | Цена | Канал | Вывод |
|---|---:|---|---|
| OpenLora | **490 ₽**, **690 ₽**, **990 ₽** | web + Telegram | локальный self-serve ценовой якорь ниже западных аналогов [T3] |
| NEiVA | **500 ₽ / неделя**, **850 ₽ / месяц**, **4 490 ₽ / год** | Telegram bot / AI assistant | показывает, что Telegram-аудитория в РФ привыкла к подписке до ~850 ₽/мес [T3] |
| Remini | freemium / in-app subscription | mobile app | глобально сильный продукт, но не локальный B2B market proof [T2][T3] |

### Вывод по конкурентам
- Конкуренция **реальна**, но она в основном про дешёвую impulse-покупку и маркетинговую упаковку, а не про высокий ACV. [T3][inference]
- В РФ наблюдается ценовой коридор примерно **490-990 ₽** за пакет / месяц для mass-market AI photo tooling. Это низкий средний чек для прохождения Profit Gate без очень большого объёма заказов. [T3][inference]

## 3. Telegram в РФ
- **OpenLora** явно ведёт в Telegram и продаёт AI-фото/аватары пакетами **490-990 ₽**. Это прямой локальный аналог distribution-модели через Telegram. [T3]
- **NEiVA** продаёт AI-подписку через Telegram по **500 ₽/неделя**, **850 ₽/месяц** и **4 490 ₽/год**. Это не чистый headshots-only продукт, но важный маркер готовности аудитории платить в Telegram. [T3]
- Проверка подтверждает: Telegram-канал дистрибуции в РФ **доступен**, однако пока не видно убедительного evidence, что именно `AI headshots` в Telegram формируют крупный и устойчивый repeat market. [T3][inference]

## 4. Willingness to pay

### Доказательства WTP
- Глобально WTP подтверждён: category leaders удерживают прайс **$29-69** за пакет. [T3]
- В РФ WTP подтверждён только на уровне **низкого чека**: порядка **490-990 ₽** за пакет или до **850 ₽/мес** за AI-подписку в Telegram. [T3]
- TechCrunch-сигнал по Remini показывает, что при вирусном продукте аудитория действительно покупает AI headshots, но этот факт плохо переносится на локальный RU-only сервис без сильного бренда и mobile-distribution engine. [T2][inference]

### Вывод по WTP
- **WTP есть, но он низкий и эпизодический.** Для инвестиционного кейса это недостаточно, если бизнес опирается на дешёвый B2C-тикет без мощной органики или app-scale performance-маркетинга. [T2][T3][inference]

## 5. Market sizing

### Методика
Ниже две оценки: top-down и bottom-up. Обе даны как рабочие ranges, потому что по нише AI headshots в РФ мало T1-статистики. Секция помечается как **[LOW CONFIDENCE]** там, где используются T2/T3 и inference.

### Top-down
- Росстат сообщал, что число занятых в РФ в марте 2025 года составляло около **74,1 млн человек**. [T1]
- Для headshots addressable audience разумно взять только white-collar / self-employed / публично-профильные роли. Консервативно берём **4%** занятых как потенциальных покупателей за год, то есть около **3,0 млн человек**. [T1][inference]
- При среднем annual spend **900 ₽** на 1 покупателя TAM РФ получается около **2,7 млрд ₽**. [T1][T3][inference]
- Для SAM берём только сегмент, который реально покупает online self-serve без фотостудии, **35%** от TAM, то есть около **945 млн ₽**. [inference]
- Реалистичный capture: **2% в год 1** и **6% за 3 года** от SAM. Тогда SOM Y1 ≈ **18,9 млн ₽**, SOM Y3 ≈ **56,7 млн ₽**. [inference]

### Bottom-up
- По данным реестра МСП, в России было около **6,59 млн** субъектов МСП на начало 2025 года. [T2]
- Для headshots / team portraits берём только digital-heavy и public-facing сегменты, консервативно **2%** МСП, то есть около **131,8 тыс. компаний**. [T2][inference]
- Средний годовой чек для micro-B2B пакета берём **7 200 ₽/год** на компанию, это соответствует 1-2 пакетам по текущим локальным ценам. [T3][inference]
- Тогда SAM_bottom_up ≈ **949 млн ₽**. [T2][T3][inference]
- Реалистичный capture: **1,5% в год 1** и **5% за 3 года**. Тогда SOM_bottom_up Y1 ≈ **14,2 млн ₽**, SOM_bottom_up Y3 ≈ **47,5 млн ₽**. [inference]

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$0,4-0,6 млрд** [T3] | — | — | top-down |
| TAM (РФ) | **2,7 млрд ₽** [T1][T3] | **3,0 млрд ₽** экв. до фильтра сегмента [T2][T3][inference] | diff ~11%, порядок совпадает | lower |
| SAM (РФ) | **945 млн ₽** [inference] | **949 млн ₽** [inference] | diff <1%, модели сходятся | lower |
| SOM Y1 | **18,9 млн ₽** | **14,2 млн ₽** | diff ~33%, берём консервативно lower | **14,2 млн ₽** |
| SOM Y3 | **56,7 млн ₽** | **47,5 млн ₽** | diff ~19%, берём консервативно lower | **47,5 млн ₽** |

### 10 реальных buyers / GTM-10-targets
1. Skyeng  
2. Яндекс Практикум  
3. Самолет Плюс  
4. Этажи  
5. Demis Group  
6. Kokoc Group  
7. Ozon Seller  
8. MPSTATS  
9. Profi.ru  
10. Skillbox  

Это не доказанные клиенты, а **реальные named targets**, где у команд продаж, преподавателей, рекрутеров, экспертов и marketplace-консультантов есть правдоподобный спрос на быстрые профили/аватары/портреты. [T2][inference]

## 6. Profit Gate, все сценарии

### Допущения
- Нужный порог: **EBITDA компании ≥ 500 000 ₽/мес**.
- Даже в lean-режиме нужен фиксированный OPEX не ниже **300 000 ₽/мес** на founder, поддержку, GPU/tooling, платёжку и трафик-эксперименты. [inference]
- Значит, monthly contribution должен быть хотя бы **800 000 ₽**. [inference]

### Сценарий A. B2C разовая покупка через web
- Средний чек: **690 ₽**. [T3]
- Переменные затраты + оплата + refund/support + acquisition берём на уровне **420 ₽** на заказ. [T3][inference]
- Contribution ≈ **270 ₽** с заказа. [inference]
- Для EBITDA 500k нужно около **2 963 заказов/мес**. [inference]
- При `LOW` спросе и ранней категории в РФ такой объём выглядит не поддержанным observable demand. **FAIL**. [T2][inference]

### Сценарий B. Telegram-подписка
- Средний чек: **850 ₽/мес**. [T3]
- После комиссий, GPU и поддержки contribution реалистично около **300 ₽/подписчик/мес**. [inference]
- Для EBITDA 500k нужно около **2 667 активных платящих подписчиков**. [inference]
- Для нишевого photo-use-case без сильного retention это слишком много. **FAIL**. [T2][T3][inference]

### Сценарий C. Micro-B2B team packs
- Средний чек: **7 900 ₽** за командный пакет. [inference]
- Contribution после sales/support/GPU около **1 700 ₽** на пакет. [inference]
- Для EBITDA 500k нужно около **471 пакета/мес**. [inference]
- Для ранней категории без сильного outbound-proof и при низком ticket size это нереалистично. **FAIL**. [T2][T3][inference]

### Сценарий D. White-label для агентств / фотостудий
- Теоретически повышает чек, но требует longer sales cycle, QA и кастомного сервиса. [inference]
- На demand-stage нет evidence, что в РФ есть достаточное число партнёров, готовых регулярно покупать такой поток. **CONDITIONAL FAIL**, недостаточно данных. [T3][inference]

## 7. Почему early reject
1. **Demand API = LOW**, и это совпадает с ощущением ранней, не устоявшейся локальной категории. [T2]
2. **WTP в РФ низкий**: подтверждён в диапазоне примерно **490-990 ₽**, что слабо совместимо с быстрым достижением EBITDA 500k/mo без большого paid volume. [T3]
3. **Repeat revenue не доказан**: headshots ближе к разовой покупке, чем к strong recurring utility. [T2][T3][inference]
4. **Profit Gate не проходит ни один базовый сценарий** без слишком больших объёмов или невалидированных B2B допущений. [inference]

## 8. Решение для pipeline
**Кейс отклоняется на стадии Demand Validation и переводится в `pipeline/rejected/`.**

Потенциальный rerun имеет смысл только если появится хотя бы одно из трёх:
1. доказанный вирусный канал с CAC сильно ниже **200 ₽**,
2. подтверждённый B2B/white-label чек **20k+ ₽** с повторяемым спросом,
3. удержание подписки в Telegram / mobile лучше, чем у типичной impulse-photo категории.

## Источники
- [T1] Росстат, занятость населения, 28.04.2025: https://rosstat.gov.ru/folder/313/document/232205
- [T2] TechCrunch о росте Remini AI Headshots: https://techcrunch.com/2023/07/11/reminis-ai-headshots-have-spurred-the-app-to-the-top-of-the-charts/
- [T2] TACC о числе субъектов МСП по данным реестра ФНС: https://tass.ru/ekonomika/22820363
- [T2] Demand API, просмотрено 10.05.2026: http://172.18.0.1:9001/multi-demand?keyword=ai%20headshots
- [T3] Aragon AI pricing: https://www.aragon.ai/pricing
- [T3] BetterPic pricing: https://www.betterpic.io/pricing
- [T3] HeadshotPro pricing: https://www.headshotpro.com/pricing
- [T3] OpenLora pricing: https://openlora.ru/
- [T3] NEiVA pricing: https://neiva.ai/
- [T3] Global AI headshots market summary: https://www.reanin.com/reports/global-ai-headshot-generator-market

Sources: T1=1, T2=4, T3=6. Primary evidence basis: T2.

> Market Pulse 2026-05-10: локальный спрос ранний, WTP есть, но слишком низкий для investment-grade headshots-only бизнеса.
