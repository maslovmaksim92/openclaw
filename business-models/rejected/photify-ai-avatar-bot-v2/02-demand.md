---
sector: QUICK-AI
stage: demand-validation
updated: 2026-04-24T11:56:00+03:00
verdict: REJECTED
confidence: medium
---

# 02-demand

## Demand validation summary
- **Продукт**: Telegram/mobile-first сервис генерации AI-аватаров, headshots и стилизованных фото по 1-10 селфи. [T2]
- **Итог по спросу в РФ**: **LOW**. Прямой спрос по ключам `ai avatar`, `ai фотосессия`, `ai headshot`, `сгенерировать аватар` остаётся низким; единственный более живой JTBD-сигнал в РФ, это не `AI-аватар`, а обычное `фото для резюме`. [T1][T2][inference]
- **Решение по гейту**: **EARLY REJECT**. Для нового игрока в РФ demand не доказывает массовый повторяемый рынок, а ни один реалистичный сценарий монетизации не показывает уверенный путь к EBITDA 500 000 ₽/мес. [T1][T2][inference]

## 1. Demand signals по РФ

### 1.1. Прямой search-led спрос на AI-аватары слабый
- Demand API на **24 апреля 2026 года** даёт **LOW** по `ai avatar` с `demand_score=15`, по `ai фотосессия` с `demand_score=18`, по `ai headshot` с `demand_score=15`, по `сгенерировать аватар` с `demand_score=15`. Это плохая база для standalone consumer-category в РФ. [T2]
- Даже более прикладной запрос `аватар для резюме` показывает **LOW** и `demand_score=0`, то есть потребительская боль пока не формулируется как отдельная устойчивая покупка. [T2]
- Более сильный сигнал есть только у `фото для резюме` с **MEDIUM** и `demand_score=32`, но это подтверждает существование JTBD «нужно фото для профиля/резюме», а не готовность массово платить именно за AI-avatar bot. [T2][inference]

### 1.2. Категория существует глобально, но это не равно локальному PMF
- TechCrunch писал, что Remini выходил в топ App Store на волне AI headshots, а Sensor Tower через TechCrunch оценивал выручку GenAI-приложений в **$1,87 млрд за H1 2025**. Это подтверждает глобальный consumer spend в adjacent-category, но не даёт автоматического вывода о локальном RU-sustainability. [T2]
- HeadshotPro на официальном сайте заявляет **196 987 клиентов** и стартовую цену **$29**, значит buyer globally уже готов платить за AI headshots как finished outcome, а не просто за модель. [T2]
- Однако в РФ прямой поисковый сигнал слабее, чем в глобальном consumer app market, поэтому перенос международного спроса в локальную Telegram-first модель требует осторожности. [T1][T2][inference]

## 2. Реальные конкуренты и цены

| Конкурент | Модель | Цена | Цена в ₽* | Что доказывает |
|---|---|---:|---:|---|
| Fabula AI | Telegram/mobile AI photos, avatars, face swap | от **$2** за 40 фото, **$6** за 120 фото | ~**150 ₽** и **449 ₽** | В RU/Telegram-first сегменте рынок быстро скатывается к дешёвым пакетам. [T2] |
| HeadshotPro | AI headshots для профилей и резюме | от **$29** | ~**2 170 ₽** | Есть готовность платить за деловой результат, но оффер ближе к западному B2C/B2B headshots. [T2] |
| Aragon AI | AI professional headshots | от **$35** | ~**2 619 ₽** | Платёжный сегмент существует, но требует сильного brand trust и чёткого outcome. [T2] |
| BetterPic | AI headshots | от **$35** | ~**2 619 ₽** | Конкуренция в headshot-сегменте уже стандартизировала цены в районе $29-35. [T2] |
| StudioShot | AI headshots for teams | от **$29/seat** | ~**2 170 ₽/seat** | B2B-команды покупают не подписку, а пакетный результат для профилей сотрудников. [T2] |

\* Пересчёт по курсу Банка России **74,8349 ₽/$** на 24.04.2026. [T1]

### Вывод по конкурентам
- Нижний ценовой якорь уже очень низкий, **150-449 ₽** у Fabula AI, поэтому простая Telegram-обёртка без moat быстро попадает в price pressure. [T1][T2][inference]
- Верхний ценовой якорь **$29-35** существует, но он привязан к узкому JTBD, «деловой headshot для LinkedIn/резюме/команды», где важны качество, доверие и post-processing. [T2][inference]
- Для нового RU-игрока это означает неприятную вилку: consumer-фан сегмент дешёвый и шумный, а premium headshot сегмент требует бренда и результата, а не просто Telegram-бота. [T2][inference]

## 3. Telegram bots / services в РФ
- **Fabula AI** является самым явным локальным ориентиром: RB.ru пишет о **1,7 млн пользователей менее чем за год**, а сам продукт продаёт AI-фото и face-swap через mobile/Telegram-first механику. Это подтверждает, что канал Telegram в РФ для quick-AI работает, но одновременно усиливает конкуренцию лидера категории. [T2]
- В demand API для Telegram-источника по ключам выше на **24.04.2026** подписчики не подтягиваются (`subscribers=0`), то есть автоматического evidence обширного слоя независимых RU-ботов с заметной аудиторией не видно. [T2]
- Вывод: канал Telegram в РФ существует, но market structure больше похожа на winner-takes-most вокруг нескольких вирусных приложений, чем на широкую экосистему платёжеспособных нишевых ботов. [T2][inference]

## 4. Willingness to pay

### 4.1. WTP есть, но он неровный и в основном outcome-driven
- HeadshotPro, Aragon AI и BetterPic публично держат стартовые цены **$29-35**, что является прямым proof of willingness to pay за деловой digital-portrait. [T2]
- Fabula AI держит существенно более низкий чек, **$2-6**, что показывает: в mass-market entertainment/photo-editing buyer готов платить, но только мало и часто импульсно. [T2]
- Российские офлайн-фотостудии продают деловые фотосессии существенно дороже AI-пакетов, что подтверждает наличие JTBD «нужен хороший портрет», но не гарантирует, что пользователь выберет AI вместо человека без сильного quality delta. [T2][inference]

### 4.2. Вывод по WTP
- **WTP подтверждён частично**: платить готовы либо за дешёвое развлечение, либо за чёткий профессиональный outcome. [T2]
- **WTP не подтверждён** для тезиса о стабильной recurring-подписке на AI-аватары в РФ, потому что прямой локальный search-demand низкий, а потребление больше похоже на разовый wow-effect. [T1][T2][inference]

## 5. Market sizing

### Методика
Считаю два пути и беру консервативно меньшую оценку.

#### Top-down
- В России в 2024 году было **74,6 млн занятых**. [T1]
- Доля занятых с высшим образованием, **35,7%**. Это грубый proxy для knowledge-worker / white-collar pool, которому чаще нужен цифровой профайл. [T1]
- Адресуемая доля для AI-headshots/avatars берётся как **1,5%** от этого пула в год, потому что продукт не является обязательной покупкой и подходит не всем. [T1][inference]
- Средний annual spend принимаю **1 000 ₽** на пользователя, это ниже западного premium headshot и выше ultra-cheap entertainment pack, то есть консервативный blended anchor. [T1][T2][inference]

**Top-down расчёт:**
- TAM РФ = 74,6 млн × 35,7% × 1,5% × 1 000 ₽ = **399,4 млн ₽/год**. [T1][T2][inference]
- SAM РФ = TAM × 40% segment fit (реально достижимый сегмент: job seekers, эксперты, sales, founders, агентские команды) = **159,8 млн ₽/год**. [T1][T2][inference]
- SOM Y1 = SAM × 1% = **1,6 млн ₽/год**. [inference]
- SOM Y3 = SAM × 5% = **8,0 млн ₽/год**. [inference]

#### Bottom-up
- В едином реестре МСП на 10.04.2026, **6,4 млн субъектов МСП**. [T1]
- Беру только **0,3%** компаний как реально нуждающихся в профессиональных digital-headshots для продаж/экспертизы/профилей команды. Это **19 200 потенциальных buyers**. [T1][inference]
- Средний годовой контракт беру **12 000 ₽/год**: один-два team-refresh пакета или несколько профилей в течение года. [T2][inference]

**Bottom-up расчёт:**
- SAM_bottom_up = 19 200 × 12 000 ₽ = **230,4 млн ₽/год**. [T1][T2][inference]
- SOM_bottom_up Y1 = 1% = **2,3 млн ₽/год**. [inference]
- SOM_bottom_up Y3 = 5% = **11,5 млн ₽/год**. [inference]

### 10 реальных buyers для bottom-up sanity check
1. Самолет Плюс, сеть агентов и брокеров. [T2]
2. Этажи, федеральное агентство недвижимости. [T2]
3. Skyeng, публичные профили преподавателей и экспертов. [T2]
4. Нетология, карточки преподавателей и экспертов. [T2]
5. Skillbox, marketing/expert pages и преподаватели. [T2]
6. СберЗдоровье, профили врачей и экспертов. [T2]
7. DocDeti, профили врачей на сайте и в соцсетях. [T2]
8. YCLIENTS, экспертный контент и PR-профили команды. [T2]
9. Calltouch, sales/marketing speakers и профильные страницы. [T2]
10. Самолет Банк / финтех-партнёры с публичными экспертами и sales-профилями. [T2]

### Reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **≈14,0 млрд ₽/год** как 5% от annualized GenAI app spend $3,74 млрд [T2][speculative] | — | Adjacent market, не чистый AI-avatar TAM | top-down |
| TAM (РФ) | **399,4 млн ₽** [T1][T2][inference] | — | Bottom-up даёт SAM, не полный TAM | top-down |
| SAM (РФ) | **159,8 млн ₽** [T1][T2][inference] | **230,4 млн ₽** [T1][T2][inference] | diff=44%, допустимо; bottom-up шире за счёт B2B team packs | **159,8 млн ₽** |
| SOM Y1 | **1,6 млн ₽** | **2,3 млн ₽** | diff=44% | **1,6 млн ₽** |
| SOM Y3 | **8,0 млн ₽** | **11,5 млн ₽** | diff=44% | **8,0 млн ₽** |

### Вывод по рынку
- Даже после reconciliation годовой **SOM Y3 около 8,0 млн ₽** слишком мал, чтобы уверенно поддержать компанию с EBITDA **500 000 ₽/мес** без выхода в другие гео или в другой продуктовый слой. [T1][T2][inference]
- Это означает, что локальный RU-рынок для standalone AI-avatar bot выглядит скорее как фича, ad-on или acquisition wedge, а не как самостоятельный большой бизнес. [T2][inference]

## 6. Profit gate, проверка всех сценариев

### Сценарий A. Разовые consumer-пакеты
- При среднем платеже **449 ₽** (Fabula mid-pack anchor) и contribution margin около 60% нужно примерно **1 856 оплаченных пакетов в месяц**, чтобы получить 500 000 ₽ contribution до fixed costs. Для нового продукта при LOW direct demand это выглядит слабореалистично. [T1][T2][inference]
- **Вердикт: FAIL.**

### Сценарий B. Consumer subscription
- Подписка для AI-аватаров конфликтует с характером потребления: портреты и стилизованные фото делаются эпизодически, а не как ежедневный utility. [T2][inference]
- Даже при **799 ₽/мес** и 60% margin нужен пул свыше **1 040 активных платящих подписчиков** только для 500k contribution, без запаса на churn и acquisition. [inference]
- **Вердикт: FAIL.**

### Сценарий C. B2B team headshots
- У B2B-сценария чек выше, но покупка чаще пакетная и нерегулярная, а не месячная recurring-выручка. [T2][inference]
- Чтобы держать **500 000 ₽ EBITDA/мес**, нужен либо постоянный поток новых batch-сделок, либо превращение продукта в более широкий media/profile workflow, чего в текущем кейсе не доказано. [T2][inference]
- **Вердикт: FAIL.**

### Сценарий D. API / white-label
- Fabula AI показывает, что API/enterprise слой в категории вообще возможен, но это уже другой бизнес: infra, sales-led GTM, SLA, white-label интеграции. [T2]
- Для нового игрока без сильного distribution moat и без подтверждённого enterprise demand в РФ это не выглядит реалистичным коротким путём именно для данного кейса. [T2][inference]
- **Вердикт: FAIL для текущего кейса.**

## 7. Основные риски спроса
1. **Repeat usage слабый**: после первого wow-эффекта пользователь может не возвращаться месяцами. [T2][inference]
2. **Price compression**: локальный лидер уже продаёт дешёвые пакеты, поэтому вход без moat быстро упирается в дисконт. [T2]
3. **Нечёткий ICP**: entertainment, резюме, команды, creators и white-label, это разные рынки с разной экономикой; текущий кейс их смешивает. [T1][T2][inference]

## 8. Решение для pipeline
**EARLY REJECT.**

Почему:
1. Прямой demand в РФ по ключевой формулировке категории остаётся **LOW**. [T2]
2. WTP есть, но он либо низкий и импульсный, либо привязан к более premium outcome с сильным брендом и качеством. [T2]
3. Даже консервативный reconciled **SAM ≈ 159,8 млн ₽**, а **SOM Y3 ≈ 8,0 млн ₽/год**, что слабо соотносится с целью **500 000 ₽ EBITDA/мес**. [T1][T2][inference]
4. Profit Gate не проходит ни в consumer packs, ни в subscription, ни в B2B batch, ни в API/white-label для нового RU-игрока в рамках текущего кейса. [T1][T2][inference]

## Источники
- [T1] Банк России, курсы валют на 24.04.2026: https://www.cbr.ru/currency_base/daily/
- [T1] Росстат, занятое население в возрасте 15 лет и старше по уровню образования, 2024: https://rosstat.gov.ru/labor_market_employment_salaries
- [T1] Единый реестр субъектов МСП / ФНС России, 10.04.2026: https://rmsp.nalog.ru/
- [T2] Demand API, просмотрено 24.04.2026:
  - http://172.18.0.1:9001/multi-demand?keyword=ai%20avatar
  - http://172.18.0.1:9001/multi-demand?keyword=ai%20%D1%84%D0%BE%D1%82%D0%BE%D1%81%D0%B5%D1%81%D1%81%D0%B8%D1%8F
  - http://172.18.0.1:9001/multi-demand?keyword=ai%20headshot
  - http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%20%D0%B0%D0%B2%D0%B0%D1%82%D0%B0%D1%80
  - http://172.18.0.1:9001/multi-demand?keyword=%D1%84%D0%BE%D1%82%D0%BE%20%D0%B4%D0%BB%D1%8F%20%D1%80%D0%B5%D0%B7%D1%8E%D0%BC%D0%B5
- [T2] RB.ru / Fabula AI: https://rb.ru/data/fabula-ai-54913/
- [T2] Fabula AI pricing / business site: https://business.fabula-ai.com/
- [T2] HeadshotPro pricing: https://www.headshotpro.com/
- [T2] Aragon AI pricing: https://www.aragon.ai/pricing
- [T2] BetterPic pricing: https://www.betterpic.io/pricing
- [T2] StudioShot pricing: https://www.studioshot.ai/pricing
- [T2] TechCrunch / Remini: https://techcrunch.com/2023/07/20/remini-tops-the-app-store-for-its-viral-ai-headshots-but-its-body-edits-go-too-far-some-say/
- [T2] TechCrunch / Sensor Tower H1 2025 GenAI spend: https://techcrunch.com/2025/07/30/gen-ai-apps-doubled-their-revenue-grew-to-1-7b-downloads-in-first-half-of-2025/

Sources: T1=3, T2=10, T3=0. Primary evidence basis: T2.
