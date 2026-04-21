# 02-demand

## Demand validation summary
- **Продукт**: Langfuse, open-source платформа для LLM observability, tracing, prompt management и evals для production AI-стека. [T2: https://langfuse.com/pricing]
- **Итог по спросу в РФ**: **LOW**. Обязательный endpoint по ключу `Langfuse` вернул composite demand **LOW**, demand score **20**, `hh.ru vacancies = 27`, `google trends RU = 8`, `habr articles = 2`, `telegram subscribers = 0`, `yandex suggest = 100`. Это показывает инженерный интерес, но не сильный закупочный рынок. [T2: http://172.18.0.1:9001/multi-demand?keyword=Langfuse]
- **Итог по Profit Gate**: **FAIL**. При текущем размере ниши в РФ и ценовой вилке comparable-сервисов достижение **500 тыс. ₽ EBITDA в месяц** как standalone-компания выглядит ненадежным во всех базовых сценариях монетизации. [T1][T2]
- **Решение P4**: **EARLY REJECT**. Выполняются оба условия: demand = LOW и Profit Gate fail. [T2]

## Evidence of demand

### 1) Mandatory demand endpoint
- `Langfuse` → **LOW**, score **20**, `hh.ru vacancies = 27`, `google trends RU = 8`, `habr articles = 2`, `telegram subscribers = 0`, `yandex suggest = 100`. [T2: internal demand endpoint]
- Интерпретация: в РФ заметен след среди разработчиков и AI-инженеров, но доказательств устойчивого бюджетного спроса именно на отдельный слой LLM observability мало. [T2, inference]

### 2) Дополнительные рыночные сигналы
- Gartner ожидает, что мировой рынок **AI software** достигнет **$452,8 млрд** в 2026 году. Это подтверждает, что Langfuse находится внутри быстрорастущего глобального spend-потока, но сам продукт покрывает только узкий инфраструктурный слой этого пирога. [T1: https://www.gartner.com/en/newsroom/press-releases/2026-1-15-gartner-says-worldwide-ai-spending-will-total-2-point-5-trillion-dollars-in-2026]
- TAdviser со ссылкой на FinExpertiza пишет, что в 2024 году крупные и средние организации в РФ потратили на внедрение и использование ИИ **90,3 млрд ₽**, а ИИ используют лишь около **6% организаций**. Это подтверждает наличие AI-бюджетов в стране, но одновременно показывает раннюю стадию рынка. [T2: https://www.tadviser.ru/index.php/Статья:Искусственный_интеллект_(рынок_России)]
- По данным HH.ru в РФ есть вакансии по `LLM`, `GenAI`, `AI engineer`, то есть production-команды формируются. Однако это подтверждает спрос на talent и внедрение, а не обязательно на отдельный observability vendor. [T1: https://hh.ru/search/vacancy?text=LLM]
- Habr содержит отдельные инженерные публикации про Langfuse и observability LLM-приложений, то есть категория существует как практический dev tooling layer. Но Habr не доказывает willingness to pay сам по себе. [T3: https://habr.com/ru/companies/otus/articles/913018/]

## Real competitors with prices
1. **LangSmith**: Developer plan **$0**, Plus **$39/seat/month**, Enterprise custom. По курсу ЦБ РФ **75,2370 ₽/$** на **21.04.2026** это около **2 934 ₽ за seat в месяц**. [T2: https://www.langchain.com/langsmith ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
2. **Arize Phoenix**: Free **$0**, AX Pro **$50/user/month**, Enterprise custom. Это около **3 762 ₽ за пользователя в месяц** по курсу ЦБ РФ. [T2: https://arize.com/pricing/ ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
3. **Helicone**: Free **$0**, Pro **$79/month**, Team **$799/month**, Enterprise custom. Это около **5 944 ₽** и **60 114 ₽** в месяц по курсу ЦБ РФ. [T2: https://www.helicone.ai/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
4. **Langfuse как self-serve reference**: Core **$29/month**, Pro **$199/month**, Enterprise **$2,499/month**. Это около **2 182 ₽**, **14 972 ₽** и **188 017 ₽** в месяц по курсу ЦБ РФ. [T2: https://langfuse.com/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]

### Что означает ценовая вилка
- Публичная cloud-вилка прямых comparable находится примерно в диапазоне **2,9 тыс. ₽ - 60,1 тыс. ₽ в месяц** до enterprise custom. [T1][T2]
- Для российского рынка это означает, что standalone vendor должен либо продавать много дешевых аккаунтов, либо быстро собирать тяжелые enterprise-контракты. При LOW demand оба пути выглядят слабо. [T1][T2, inference]
- Дополнительно категорию ограничивает open-source природа Langfuse и Phoenix: часть buyer pool может self-hostить решение и не покупать дорогой managed layer. [T2, inference]

## Telegram bots / services in RU
- Специализированных российских Telegram-ботов с заметной дистрибуцией именно под **LLM observability / evals / tracing** я не нашел. Mandatory endpoint также вернул `telegram subscribers = 0`. [T2: internal demand endpoint]
- В РФ есть adjacent monitoring/alerting сервисы с Telegram-интеграциями, например **HiveTrace** у Raft, где Telegram используется как канал алертов, но это не Telegram-first продукт и не прямой конкурент Langfuse. Публичных цен на сайте нет. [T2: https://hivetrace.io/]
- Вывод: Telegram в РФ не выступает самостоятельным каналом спроса или дистрибуции для этой категории. [T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: несколько глобальных игроков берут деньги за LLM observability/evals, причем pricing опубликован публично. Значит, willingness to pay на мировом рынке есть. [T2]
- **Доказательство WTP №2**: в РФ уже есть общий AI spend на уровне **90,3 млрд ₽** среди крупных и средних организаций, то есть бюджет на AI-инструменты в принципе существует. [T2]
- **Ограничение локального WTP**: прямых подтверждений, что российские компании готовы массово выделять отдельную budget line именно под observability/evals, мало. Endpoint LOW, Telegram = 0, а HH и Habr показывают скорее build-side активность. Поэтому локальный WTP надо считать **слабым и косвенным**, а не доказанным. [T1][T2][T3]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/eng/currency_base/daily/]
- Global anchor: мировой рынок **AI software** в 2026 году = **$452,8 млрд** по Gartner. Для observability/evals/tracing беру **0,8%** этого spend как addressable proxy, потому что речь о нишевом инфраструктурном слое внутри AI stack. Это аналитическое допущение, не прямой market stat. [T1 + inference]
- Russia anchor: AI spend крупных и средних организаций в РФ = **90,3 млрд ₽** в 2024 году по TAdviser/FinExpertiza. Для observability/evals/tracing беру **0,9%** этого spend как proxy TAM РФ, потому что категория обычно сидит ниже моделей, интеграции, data/infra и часто частично закрывается open-source. [T2 + inference]
- Bottom-up total buyer base беру из крупного enterprise/upper-mid рынка РФ с production AI-командами. Для sanity check использую 10 реальных buyers ниже и экстраполирую до **700** потенциально релевантных компаний. Это оценка, а не официальный реестр. [T1][T2, inference]
- **% with need** = **18%**: доля компаний, где есть production LLM/agent workflow и отдельная потребность в tracing/evals, а не только в базовом monitoring. Консервативность поддерживается LOW demand endpoint. [T1][T2, inference]
- **Средний контракт**: **240 тыс. ₽ ARR** для mid-market/self-serve plus, либо 1,5-3 млн ₽ ARR для enterprise. Для base-case bottom-up использую **240 тыс. ₽ ARR**, поскольку рынок РФ для такой категории пока выглядит price-sensitive. [T1][T2, inference]

### Top-down
- **TAM (мир)** = $452,8 млрд × 0,8% = **$3,62 млрд**. [T1 + inference]
- **TAM (РФ)** = 90,3 млрд ₽ × 0,9% = **812,7 млн ₽**. [T2 + inference]
- **SAM (РФ)** = TAM РФ × 35% (только компании с production AI stack, где отдельный observability слой действительно нужен) = **284,4 млн ₽**. [T2 + inference]
- **SOM Y1** = SAM × 2% = **5,69 млн ₽**. [inference]
- **SOM Y3** = SAM × 7% = **19,91 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **700** компаний в РФ, где есть шанс на production AI/LLM use-case: банки, маркетплейсы, телекомы, крупный ритейл, интеграторы, bigtech, enterprise software vendors, крупные digital-first сервисы. [T1][T2, inference]
- **% with need** = **18%**. [T1][T2, inference]
- **SAM_bottom_up** = 700 × 18% × 240 000 ₽ = **30,24 млн ₽**. Эта оценка слишком низкая относительно top-down, поэтому проверяем enterprise overlay: 70 enterprise-аккаунтов × 2,5 млн ₽ ARR = **175,0 млн ₽**. Итоговый blended SAM_bottom_up = **175,0 млн ₽** как более реалистичный нижний bound для категории. [T1][T2, inference]
- **SOM_bottom_up Y1** = **10 клиентов** × 240 000 ₽ + **1 enterprise** × 2,5 млн ₽ = **4,9 млн ₽**. [inference]
- **SOM_bottom_up Y3** = **35 mid-market** × 240 000 ₽ + **4 enterprise** × 2,5 млн ₽ = **18,4 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $3,62 млрд [T1] | — | — | top-down |
| TAM (РФ) | 812,7 млн ₽ [T2] | 700,0 млн ₽ [T1][T2] | diff=16%, расхождение допустимо, bottom-up считает только вероятный buyer universe | lower |
| SAM (РФ) | 284,4 млн ₽ [T2] | 175,0 млн ₽ [T1][T2] | diff=1,63x, приемлемо с учетом консервативного RU adoption | lower |
| SOM Y1 | 5,69 млн ₽ | 4,9 млн ₽ | diff=16%, оценки сходятся | **используем 4,9 млн ₽** |
| SOM Y3 | 19,91 млн ₽ | 18,4 млн ₽ | diff=8%, оценки сходятся | **используем 18,4 млн ₽** |

### GTM: 10 реальных buyers для bottom-up
1. **Сбер**. [T2: https://www.sberbank.com/]
2. **Яндекс / Yandex Cloud**. [T2: https://yandex.cloud/ru]
3. **Т-Банк**. [T2: https://www.tbank.ru/]
4. **МТС AI**. [T2: https://mts.ai/]
5. **VK**. [T2: https://vk.company/ru/]
6. **Avito Tech**. [T2: https://avito.tech/]
7. **Ozon Tech**. [T2: https://job.ozon.ru/tech/]
8. **X5 Tech**. [T2: https://tech.x5.ru/]
9. **Альфа-Банк**. [T2: https://alfabank.ru/]
10. **Positive Technologies**. [T2: https://www.ptsecurity.com/ru-ru/]

Sanity check: при среднем цикле сделки **6-9 месяцев** команда без сильного локального бренда вряд ли успеет закрыть больше 1-2 enterprise-клиентов за первый год. Поэтому даже SOM Y1 около **4,9 млн ₽** выглядит как оптимистичный upper-mid case, а не базовый guaranteed outcome. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve cloud
- Реалистичный чек для РФ, если идти от comparable, находится в диапазоне **3-15 тыс. ₽ MRR** на команду или seat-bundle. [T1][T2]
- Чтобы получить **500 тыс. ₽ EBITDA/мес**, при gross margin около 80% и даже очень компактной команде нужно не меньше **1,5-1,8 млн ₽ MRR** выручки, то есть порядка **100-300** активных платящих аккаунтов в зависимости от ARPU. [T2, inference]
- Demand evidence это не поддерживает. **FAIL**. [T2]

### Сценарий B. Mid-market SaaS
- Реалистичный чек для российской продуктовой команды можно оценить в **20-40 тыс. ₽ MRR**. [T1][T2, inference]
- Для EBITDA 500 тыс. ₽/мес понадобятся примерно **40-70** живых mid-market аккаунтов. Для такой узкой категории в РФ это выглядит слишком тяжело. **FAIL**. [T2]

### Сценарий C. Enterprise private cloud / on-prem
- Теоретически возможен чек **1,5-3 млн ₽ ARR** на клиента. [T2, inference]
- Но даже при **3 млн ₽ ARR** и gross margin 70% нужно держать минимум **6-8** стабильных enterprise-клиентов, чтобы после presales, support, solutions engineering и compliance выйти на **500 тыс. ₽ EBITDA/мес**. Для LOW-demand категории это ненадежно. **FAIL**. [T2]

### Сценарий D. Services + implementation
- Можно брать деньги за внедрение, аудит prompt/trace pipeline и настройку evals. [T2, inference]
- Но тогда бизнес уходит в services-heavy модель с нестабильной маржой и слабой повторяемостью, что плохо соответствует fund-scale software thesis. По критерию company EBITDA >= 500K/mo как product company сценарий неубедителен. **FAIL**. [T2]

## Risks
- Категория в РФ пока слишком ранняя, а прямой demand signal = **LOW**. [T2]
- Open-source и self-hosted deployment снижают willingness to pay за managed vendor layer. [T2]
- Для покупки нужен зрелый production LLM-контур, а таких команд в РФ ограниченное число. [T1][T2]
- Telegram не работает как органический канал дистрибуции для этой ниши. [T2]

## Verdict for P4
- **P4 verdict**: **REJECTED (early)**.
- Обоснование: demand endpoint вернул **LOW**, а Profit Gate не проходит ни в self-serve, ни в mid-market, ни в enterprise, ни в services/integrator сценарии. [T2]
- Следствие: кейс не продолжаем в следующие стадии, оформляем reject на P4. [T2]

Sources: T1=4, T2=16, T3=1. Primary evidence basis: T2.
