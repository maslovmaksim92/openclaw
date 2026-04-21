# 02-demand

## Demand validation summary

**Краткий вывод:** в РФ для Norm Ai как enterprise AI-платформы для legal/compliance workflow спрос **низкий**, а юнит-экономика локального запуска не проходит Profit Gate. Поэтому кейс уходит в **REJECTED** уже на demand-stage.

**Почему:**
- по обязательному demand endpoint запросы `enterprise compliance automation`, `GRC software`, `регтех комплаенс автоматизация`, `AI compliance policy` дают `composite_demand=LOW`, `demand_score=0`; максимум зафиксировано только `hh_vacancies=7` по самому широкому англоязычному запросу, при этом Google Trends RU = 0-1 и Telegram subscribers = 0 [T1/T2 via internal multi-demand, 2026-04-22 MSK];
- Norm Ai позиционируется как high-touch enterprise продукт для крупнейших regulated institutions, а не как self-serve SaaS, то есть для РФ нужен дорогой legal/compliance enablement, локализация правил и длинный sales cycle [T2];
- в РФ есть соседний спрос на AML/KYC и контрагентский compliance, но почти нет явных Telegram-first или SMB-ready решений именно под policy execution / regulatory workflow automation для enterprise legal & compliance [T2/T3].

## Что именно продает Norm Ai
Norm Ai описывает себя как `Legal & Compliance AI`, которая превращает законы, регуляторные требования и внутренние policy в AI agents; на сайте заявлены use cases: regulated content review, disclosures, contract review, DDQ/RFP automation, supervisory AI, business & compliance workflows. Также компания пишет о клиентах с суммарным AUM $30T и 13.9M+ compliance determinations [T2: https://www.norm.ai/ ; https://www.norm.ai/regulated-content-review/].

**Следствие для РФ:** продукт ближе всего к продаже в банки, страховщиков, УК, НПФ и крупные публичные/финансовые группы с тяжелым disclosure/compliance контуром, а не к широкому mid-market.

## Demand signals
### 1) Обязательный multi-demand endpoint
Запросы к `http://172.18.0.1:9001/multi-demand?keyword=X`:
- `enterprise compliance automation` → `LOW`, score 0, `hh_vacancies=7`, `habr_articles=2`, `google_trends_ru=0`, `yandex_suggest=2`
- `GRC software` → `LOW`, score 0, `hh_vacancies=0`, `habr_articles=2`, `google_trends_ru=1`
- `регтех комплаенс автоматизация` → `LOW`, score 0, `hh_vacancies=0`, `google_trends_ru=0`
- `AI compliance policy` → `LOW`, score 0, `hh_vacancies=0`, `google_trends_ru=0`

**Интерпретация:** локальный верхневоронковый спрос слабый; категория в РФ пока не стала самостоятельным search-driven сегментом [T1/T2].

### 2) Регуляторная боль есть, но она не равна готовому бюджету на отдельный AI-layer
Deloitte пишет, что у retail и corporate banks операционные затраты на compliance выросли более чем на 60% относительно докризисных уровней [T1: https://www.deloitte.com/us/en/services/consulting/articles/cost-of-compliance-regulatory-productivity.html]. Это подтверждает боль, но не доказывает, что российские игроки готовы покупать отдельный импортный AI-layer вместо локальных процессов, ИБ-контуров и in-house/интеграторских решений.

## Конкуренты с ценами
Ниже не идеальные 1:1 аналоги Norm Ai, а ближайший коммерческий коридор по compliance/GRC automation, от которого можно оценивать willingness-to-pay.

| Конкурент | Что продает | Публичная цена | Вывод для коридора цен |
|---|---|---:|---|
| Dash ComplyOps | compliance automation / cloud compliance | старт от **$250/мес** за 0-5 protected units, далее $30/$10/$5 за unit [T2] | нижний SMB/DevSecOps floor |
| Secureframe via AWS Marketplace | compliance automation | **$15,000/год** annual subscription [T2] | mid-market baseline |
| Scrut via AWS Marketplace | security & compliance platform | **$15,000/год** contract price [T2] | mid-market baseline |
| Scytale via AWS Marketplace | compliance automation | **$7,500/год** subscription + **$2,100** onboarding [T2] | entry enterprise baseline |

Ссылки:
- Dash: https://dashsdk.com/pricing/
- Secureframe AWS Marketplace: https://aws.amazon.com/marketplace/pp/prodview-v3gp7lc4l5a6u
- Scrut AWS Marketplace: https://aws.amazon.com/marketplace/pp/prodview-zqmm6lmmk6l46
- Scytale AWS Marketplace: https://aws.amazon.com/marketplace/pp/prodview-6u7m2invjqzq4

**Рабочий вывод по цене для РФ:** для локального wedge реалистичный ACV скорее **1.0-2.0 млн ₽/год** за клиента, а не 3-6 млн ₽/год. Причина: низкий search demand в РФ, длинная интеграция, санкционный/ИБ барьер и наличие более дешевых adjacent решений [T2 + inference].

## Telegram и RU-services
### Telegram / боты в РФ
- BitOK продвигает Telegram AML bot для проверки крипторисков и AML reports [T2: https://bitok.org/ru/bot].
- Cerber продвигает AML-бот в Telegram, включая бесплатные проверки [T2: https://1.cerber.pro/aml-bot/].
- AML Telegram Bot предлагает проверку кошелька за **$1** и B2B API [T3: https://amlcheckbot.com/].

### Что это значит
В русскоязычном Telegram реально существует спрос на **AML/KYT/crypto-risk** проверки, но это другой бюджетный и продуктовый слой. Это не подтверждает спрос на enterprise policy execution platform уровня Norm Ai; наоборот, показывает, что в RU/TG монетизация смещена в дешевые per-check и crypto-compliance сценарии [T2/T3].

### RU services рядом с болью
- Контур Призма и похожие local tools закрывают KYC/AML/контрагентский compliance слой локально [T2/T3].
- ПравоТех/Case.one семейство и другие legal ops решения присутствуют как отечественный software context, но не видно сильного публичного product-market сигнала именно под AI-based regulatory workflow automation [T2/T3].

## WTP: willingness to pay
**Доказательства готовности платить есть, но они слабее, чем нужно для фонда:**
1. На мировом рынке compliance automation покупают подписки уровня **$7.5k-$15k/year**, иногда с onboarding fee [T2].
2. Deloitte фиксирует структурный рост cost of compliance, значит бюджетная боль реальна [T1].
3. Norm Ai already sells to very large institutions, то есть глобально WTP существует [T2].

**Но для РФ именно под этот продукт WTP не доказан:**
- поисковый спрос и вакансии в РФ слабые [T1/T2];
- enterprise buyers в РФ ожидают локальный data perimeter, русскую регуляторную модель и внедрение через доверенного вендора/интегратора [T2 inference];
- TG/RU evidence указывает скорее на AML/KYC adjacency, не на premium AI policy-execution category [T2/T3].

**Оценка WTP для РФ:** **низко-средняя**, с высокой вероятностью только через custom sale и heavy services. Для продукта как scalable software wedge это слабый сигнал.

## Market sizing
### Методика
- **Top-down:** от российского рынка ПО и узкой доли compliance/GRC workflow software.
- **Bottom-up:** от количества реально регулируемых финансовых организаций в РФ и реалистичного ACV.
- Если где-то есть inference, это явно отмечено.

### Top-down
1. Российский ИТ-рынок в 2024 году оценивался TAdviser в **3.5 трлн ₽** [T2: https://www.tadviser.ru/index.php/Статья:ИТ-рынок_России].
2. MWS/АК&M оценивали software vertical в РФ в **1.5 трлн ₽** в 2024 году [T2: https://www.akm.ru/eng/news/mws-the-volume-of-the-it-market-by-the-end-of-2024-will-reach-3-3-trillion-rubles/].
3. Глобальный eGRC market оценивался Grand View Research в **$72.42 млрд** на 2025 год [T3: https://www.grandviewresearch.com/industry-analysis/enterprise-governance-risk-compliance-egrc-market].
4. Для РФ берем addressable share **0.15%** от software market как very narrow slice под regulated compliance workflow AI. Это **инференс**, не прямой рынок [T2/T3 + inference].

**Top-down расчеты:**
- TAM (РФ) = 1.5 трлн ₽ × 0.15% = **2.25 млрд ₽**
- SAM (РФ) = 2.25 млрд ₽ × 25% (финансовый regulated wedge first) = **562.5 млн ₽**
- SOM Y1 = 562.5 млн ₽ × 1.0% = **5.6 млн ₽**
- SOM Y3 = 562.5 млн ₽ × 3.5% = **19.7 млн ₽**

### Bottom-up
**Total buyers (core wedge, РФ):**
- кредитные организации: **345** [T1: ЦБ РФ реестр финорганизаций, sheet `Кредитные организации`, по состоянию на 20.04.2026, https://cbr.ru/vfs/finmarkets/files/supervision/list_123_fz.xlsx]
- субъекты страхового дела: **200** unique registry numbers [T1: ЦБ РФ, https://cbr.ru/vfs/finmarkets/files/supervision/list_ssd.xlsx]
- НПФ: **32** [T1: ЦБ РФ, sheet `НПФ`, https://cbr.ru/vfs/finmarkets/files/supervision/list_123_fz.xlsx]
- лицензии на управление ценными бумагами: **169** [T1: ЦБ РФ, https://cbr.ru/vfs/finmarkets/files/supervision/list_trust.xlsx]
- специализированные депозитарии: **31** [T1: ЦБ РФ, https://cbr.ru/vfs/finmarkets/files/supervision/list_specdepositaries.xlsx]

**Итого core buyers = 777** [T1].

**10 реальных buyers для первичного GTM списка:**
1. Сбербанк [T1/T2]
2. Банк ВТБ [T1/T2]
3. Альфа-Банк [T1/T2]
4. Т-Банк [T1/T2]
5. Газпромбанк [T1/T2]
6. Совкомбанк [T1/T2]
7. СОГАЗ [T1/T2]
8. Ингосстрах [T1/T2]
9. АльфаСтрахование [T1/T2]
10. Ренессанс Жизнь [T1/T2]

**Допущения:**
- % with need = **35%**. Берем только организации с заметным объемом disclosure/marketing/client communication/compliance workflow, а не все из реестра [T1 + T2 inference].
- ARR avg = **1.5 млн ₽/год**. Это близко к международному lower-mid-market коридору после пересчета и discount for RU budget reality [T2 + inference].

**Bottom-up расчеты:**
- TAM (РФ) = 777 × 1.5 млн ₽ = **1.17 млрд ₽**
- SAM (РФ) = 777 × 35% × 1.5 млн ₽ = **408.0 млн ₽**
- SOM Y1 = 408.0 млн ₽ × 1.0% = **4.1 млн ₽**
- SOM Y3 = 408.0 млн ₽ × 3.5% = **14.3 млн ₽**

### Сверка top-down vs bottom-up
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------:|-----------:|----------------|-----------|
| TAM (мир) | $72.42B [T3] | — | — | top-down |
| TAM (РФ) | 2.25 млрд ₽ [T2/T3] | 1.17 млрд ₽ [T1/T2] | diff=1.9x, top-down шире, bottom-up уже по core regulated buyers | **lower** |
| SAM (РФ) | 562.5 млн ₽ [T2/T3] | 408.0 млн ₽ [T1/T2] | diff=1.38x, допустимо | **lower** |
| SOM Y1 | 5.6 млн ₽ | 4.1 млн ₽ | diff=1.36x | **используем 4.1 млн ₽** |
| SOM Y3 | 19.7 млн ₽ | 14.3 млн ₽ | diff=1.38x | **используем 14.3 млн ₽** |

**Вывод по sizing:** рынок в РФ существует, но для standalone foreign category это **узкий low-hundreds-millions ₽ SAM**, а не крупный венчурный geo-expand wedge.

## Profit Gate (company EBITDA >= 500K/mo)
Проверяю все разумные монетизационные сценарии для локального запуска.

### Сценарий A, software-only
- ACV: **1.2 млн ₽/год**
- MRR на клиента: 100k ₽
- Gross margin: 80%
- Локальная команда/overhead: ~1.3 млн ₽/мес
- EBITDA = 80k × N - 1.3 млн
- Для EBITDA 500k ₽/мес нужно **23 клиента**

**Вердикт:** нереалистично при LOW demand.

### Сценарий B, software + onboarding
- ACV: **1.8 млн ₽/год**
- MRR на клиента: 150k ₽
- Gross margin: 75%
- Team/overhead: ~1.6 млн ₽/мес
- EBITDA = 112.5k × N - 1.6 млн
- Для EBITDA 500k ₽/мес нужно **19 клиентов**

**Вердикт:** тоже не бьется; для такого числа нужен заметно более зрелый рынок и более короткий цикл сделки.

### Сценарий C, bespoke enterprise / managed compliance layer
- ACV: **4.0 млн ₽/год**
- MRR на клиента: 333k ₽
- Gross margin: 65%
- Team/overhead: ~2.0 млн ₽/мес
- EBITDA = 216k × N - 2.0 млн
- Для EBITDA 500k ₽/мес нужно **12 клиентов**

**Вердикт:** даже premium scenario требует 12 enterprise logos, а при current RU demand, локализации регуляторики и sales cycle 9-12+ месяцев это выглядит недостижимо в реалистичный горизонт.

**Итог по Profit Gate:** **FAIL**.

## Decision
- **Demand:** LOW
- **WTP:** есть глобально, но для РФ не доказан как repeatable software budget
- **Profit Gate:** FAIL
- **Решение:** **EARLY REJECT**

## Risks / why not now
1. Категория в РФ не сформирована как самостоятельный high-intent search market.
2. Нужен тяжелый regulatory localization и data/compliance trust layer.
3. Локальный бюджетный коридор слишком низок относительно требуемой команды внедрения.
4. Даже на узком финансовом wedge рынок не дает быстрой траектории к 500k ₽ EBITDA/мес.

Sources: T1=6, T2=10, T3=2. Primary evidence basis: T1.