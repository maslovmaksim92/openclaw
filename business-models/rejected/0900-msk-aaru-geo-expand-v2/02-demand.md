---
stage: demand-validation
created: 2026-04-20T06:31:00+03:00
---

# 02-demand

## Demand validation verdict
- **Итог по спросу:** точечный глобальный спрос на synthetic customer research подтверждён, но в РФ это пока скорее adjacent-бюджет внутри классических маркетинговых исследований, innovation research и brand/perception work, а не самостоятельная high-LTV категория. **Статус: FAIL FOR PROGRAM 1.** [T1][T2]
- **Composite demand API:** `LOW` (`3/100`) по `синтетические исследования клиентов`, `LOW` (`18/100`) по `customer research`, `MEDIUM` (`30/100`) по `маркетинговые исследования`, `LOW` (`22/100`) по `опросы потребителей`. Это означает, что локальный buyer-language привязан к обычным исследованиям, а не к AI simulation layer. [T1]
- **Ключевой вывод:** Aaru доказывает, что категория существует у глобальных enterprise-клиентов через Accenture-style delivery motion, но для standalone запуска в РФ пока не хватает подтверждения чека `>500 000 ₽/мес` и repeatable локального ICP. [T1][T2, inference]

## Demand evidence
1. Aaru официально позиционирует Lumen как систему для `creative testing`, `product launches`, `price optimization`, `market segmentation`, `campaign strategy` и `brand perception tracking`. Это валидирует не лабораторный R&D, а коммерческий decision-support workflow. [T1]
   Source: https://aaru.com/products
2. Accenture 4 марта 2025 объявила об инвестиции в Aaru и плане интегрировать Lumen в продукты и сервисы Accenture Song для `new product development`, `marketing`, `customer strategy` и `customer service`. Это сильный сигнал enterprise willingness-to-pay, но через consulting/distribution layer, а не через self-serve SMB adoption. [T1]
   Source: https://newsroom.accenture.com/news/2025/accenture-invests-in-and-collaborates-with-ai-powered-agentic-prediction-engine-aaru
3. По данным TechCrunch от 5 декабря 2025, у Aaru ARR всё ещё ниже `$10 млн`, хотя раунд Series A был крупным. Для demand-stage это важно: hype высокий, но коммерческая зрелость категории ещё ранняя. [T2]
   Source: https://techcrunch.com/2025/12/05/ai-synthetic-research-startup-aaru-raised-a-series-a-at-a-1b-headline-valuation/
4. В РФ adjacent-category `маркетинговые исследования` показывает `MEDIUM / 30` и **2398 вакансий HH.ru**, а exact synthetic category почти отсутствует. Значит бюджетная строка существует, но buyer покупает исследование как service/project, а не как отдельную AI platform category. [T1]
   Source: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3%D0%BE%D0%B2%D1%8B%D0%B5%20%D0%B8%D1%81%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F

## Competitor set and pricing
| Игрок | Что закрывает | Публичная цена | Вывод |
|---|---|---:|---|
| Анкетолог | self-serve опросы, панель, DIY research | **2 990 / 6 690 / 9 890 ₽/мес** за тарифы self-serve [T2] | подтверждает низкий software price floor в РФ |
| Questionstar | конструктор опросов и отчётность | **2 999 / 29 995 / 73 500 ₽/мес** [T2] | локальный ceiling для DIY survey software всё ещё на порядок ниже Program 1 |
| Анкетолог panel | панель респондентов **332 500** человек [T2] | price on request | показывает, что рынок покупает доступ к людям и полевым данным, а не только к софту |
| Tiburon Research panel | online panel **670 000** респондентов [T2] | price on request | сильный substitute для custom research и concept testing |

Sources:
- Анкетолог тарифы: https://anketolog.ru/plans.html
- Questionstar тарифы: https://questionstar.ru/
- Анкетолог panel book: https://anketolog.ru/pages/panelbook.html
- Tiburon panel: https://tiburon-research.ru/panel

## WTP, willingness to pay
- Глобальный WTP подтверждён партнёрством с Accenture и использованием Aaru для product/marketing/customer strategy workflows. [T1]
- Но локальный observable WTP в РФ виден в основном у survey/research tooling и panel access. Публичный price band у self-serve substitute-решений находится примерно в диапазоне **2 990–73 500 ₽/мес**, что драматически ниже Program 1 target economics. [T2]
- Реалистичная интерпретация: если Aaru-подобный продукт и может продаваться в РФ дороже, то только как enterprise insight engine + managed services для крупных consumer brands, банков, телекомов и e-commerce. Тогда чек теоретически может подняться до **150 000–300 000 ₽/мес**. Это уже выше DIY research software, но всё ещё ниже требуемого порога `500 000 ₽/мес` на клиента. [T1][T2, inference]
- Следовательно, прямой WTP на standalone synthetic research platform в РФ пока **недостаточно подтверждён**. [T1][T2]

## Market sizing
### Assumptions
- Курс ЦБ РФ на **18 апреля 2026**: **76,0535 ₽/$**. [T1]
  Source: https://www.cbr.ru/eng/currency_base/dynamics/?UniDbQuery.FromDate=07.06.2025&UniDbQuery.Posted=True&UniDbQuery.ToDate=10.06.2025&UniDbQuery.VAL_NM_RQ=R01235&UniDbQuery.date_req1=&UniDbQuery.date_req2=&UniDbQuery.mode=1
- ESOMAR / Research World указывает размер global insights industry около **$153 млрд** в 2024, а сегмент **self-serve research platforms** около **$3,89 млрд**. Для Aaru ближе именно software/research-platform слой, а не весь insights market. [T2]
  Source: https://researchworld.com/articles/inside-the-153bn-insights-industry
- Для локализации беру conservative proxy: РФ = **1,5%** глобального self-serve/platform TAM, чтобы не завышать размер рынка. [T2, inference]
- Bottom-up buyer universe: крупные consumer brands, банки, телекомы, маркетплейсы и исследовательские агентства, где research velocity реально влияет на GTM и pricing decisions. Для рабочей модели беру **120** потенциальных enterprise аккаунтов, из них fit only **20%**. [T1/T2-supported inference]

### 10 реальных buyers для GTM
1. Сбер
2. Т-Банк
3. ВТБ
4. МТС
5. МегаФон
6. Ozon
7. Wildberries
8. Яндекс Маркет
9. X5 Group
10. Магнит

### Top-down
- **TAM (platform layer, world):** `$3,89 млрд` = **295,6 млрд ₽**. [T2]
- **TAM (РФ proxy):** `1,5%` = **4,43 млрд ₽**. [T2, inference]
- **SAM (РФ):** беру **10%** TAM РФ, только крупные enterprise buyers с постоянным research cadence. Получаю **443 млн ₽**. [T2, inference]
- **SOM Y1:** **3%** от SAM = **13,3 млн ₽**. [T2, inference]
- **SOM Y3:** **10%** от SAM = **44,3 млн ₽**. [T2, inference]

### Bottom-up
- **Total buyers:** **120** enterprise accounts. [T2, inference]
- **% with need:** **20%** = **24** buyer-ов. [T1/T2-supported inference]
- **ARR avg:** **2,4 млн ₽/год** на клиента, то есть **200 000 ₽/мес**. [T2, inference]
- **SAM bottom-up:** 24 × 2,4 млн ₽ = **57,6 млн ₽**. [T2]
- **SOM Y1 bottom-up:** 5 клиентов = **12,0 млн ₽**. [T2]
- **SOM Y3 bottom-up:** 10 клиентов = **24,0 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---:|
| TAM РФ | 4,43 млрд ₽ | 288,0 млн ₽ как upper proxy при 120 buyer × 2,4 млн ₽ | большой разрыв, потому что top-down включает широкий insights software layer, а bottom-up только узкий enterprise ICP | top-down for ceiling |
| SAM РФ | 443,0 млн ₽ | 57,6 млн ₽ | разрыв ~7,7x, значит локальный serviceable wedge очень узкий | **57,6 млн ₽** |
| SOM Y1 | 13,3 млн ₽ | 12,0 млн ₽ | близко | **12,0 млн ₽** |
| SOM Y3 | 44,3 млн ₽ | 24,0 млн ₽ | bottom-up реалистичнее | **24,0 млн ₽** |

**Sanity check:** даже при хорошем execution Y1 выглядит как 5 enterprise клиентов по **200 000 ₽/мес**, а не как high-velocity category. Это уже само по себе сигнал, что кейс не тянет Program 1 threshold economics. [T2, inference]

## Profit Gate: EBITDA >= 500 000 ₽/мес
Проверил реалистичные сценарии:

1. **DIY research software**  
   30 клиентов × 30 000 ₽/мес = **900 000 ₽/мес выручки**. При EBITDA-марже 35% = **315 000 ₽/мес EBITDA**. **FAIL.** [T2]

2. **Enterprise insights subscription**  
   8 клиентов × 200 000 ₽/мес = **1 600 000 ₽/мес выручки**. При EBITDA-марже 35% = **560 000 ₽/мес EBITDA**. **PASS на уровне компании, но чек на клиента всё равно ниже Program 1.** [T2]

3. **Managed synthetic research studio**  
   5 клиентов × 300 000 ₽/мес = **1 500 000 ₽/мес выручки**. При EBITDA-марже 25% = **375 000 ₽/мес EBITDA**. **FAIL.** [T2]

4. **Premium enterprise package**  
   4 клиента × 500 000 ₽/мес = **2 000 000 ₽/мес выручки**. При EBITDA-марже 30% = **600 000 ₽/мес EBITDA**. **Теоретический PASS, но такой price point публично ничем не подтверждён в РФ.** [T1][T2, inference]

**Итог Profit Gate:** порог можно пройти только на агрессивном enterprise сценарии, который пока не подтверждён локальным willingness-to-pay. Для Program 1 это недостаточно. [T1][T2]

## Risks
- Exact category demand в РФ почти отсутствует, поэтому потребуется тяжёлое market education. [T1]
- Локальные substitutes дешёвые, а traditional research agencies уже закрывают job-to-be-done знакомым для buyer способом. [T2]
- Aaru сейчас сильнее выглядит как consulting-enabler / strategic research layer через партнёров уровня Accenture, чем как repeatable standalone software category для РФ. [T1]
- Высокий global hype пока не конвертирован в убедимый ARR scale: по TechCrunch ARR ниже `$10 млн` на декабрь 2025. Это повышает риск, что рынок ещё не устоялся. [T2]

## Final assessment
- **Demand:** глобально real, локально weak-to-niche. [T1][T2]
- **WTP:** в РФ подтверждён для adjacent research tooling, но не для standalone synthetic customer research platform на уровне `>500 000 ₽/мес` с клиента. [T2]
- **Profit Gate:** не проходит с достаточной уверенностью. [T1][T2]
- **Решение:** **Отклонить на этапе demand validation.** Кейс интересен стратегически как supporting signal для broader AI-enabled research / insights workflows, но в текущем виде не тянет standalone Program 1 case. [T1][T2]

## Market Pulse
> Market Pulse 2026-04-20: интерес к synthetic research globally растёт, но локальная monetization-ready категория в РФ пока не проявилась.

Sources: T1=4, T2=7, T3=0. Primary evidence basis: T1.