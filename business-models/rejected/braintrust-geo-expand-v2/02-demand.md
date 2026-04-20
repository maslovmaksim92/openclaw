# 02-demand

## Demand validation summary
- **Продукт**: Braintrust, платформа для LLM observability, evals, tracing и quality control production AI-систем. [T2: https://www.braintrust.dev/pricing]
- **Итог по спросу в РФ**: **LOW**. Обязательный endpoint по ключу `AI observability LLM evals tracing` вернул composite demand **LOW**, score **0**, `hh.ru vacancies = 0`, `google trends RU = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand?keyword=AI%20observability%20LLM%20evals%20tracing]
- **Итог по Profit Gate**: **FAIL**. Даже в лучшем enterprise/on-prem сценарии достижение **500 тыс. ₽ EBITDA в месяц** в РФ выглядит малореалистичным из-за узкой категории, длинного presale, низкой публичной ценовой вилки у глобальных аналогов и наличия open-source/self-hosted substitutes. [T1][T2][T3]
- **Решение P4**: **EARLY REJECT**. Одновременно выполняются оба условия: direct demand = LOW и Profit Gate не проходит. [T2]

## Evidence of demand

### 1) Mandatory endpoint
- `AI observability LLM evals tracing` → **LOW**, score **0**, `hh.ru vacancies = 0`, `google trends RU = 0`, `habr articles = 2`, `yandex suggest = 2`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- Интерпретация: в РФ есть слабый контентный след среди инженеров, но почти нет признаков закупочного спроса или зрелой категории. [T2, inference]

### 2) Дополнительные сигналы рынка
- TAdviser со ссылкой на FinExpertiza пишет, что в 2024 году крупные и средние российские организации потратили на внедрение и использование ИИ **90,3 млрд ₽**, средний чек на компанию составил **5,95 млн ₽**. Это подтверждает наличие базового AI-бюджета, но не отдельной budget line под observability/evals. [T2: https://www.tadviser.ru/index.php/Статья:Искусственный_интеллект_(рынок_России)]
- В той же публикации TAdviser приводится оценка, что ИИ реально используют лишь около **6% организаций**, а доля неудачных ИИ-проектов в РФ находится около **80-90%**. Это усиливает саму боль around measurement/evaluation, но также показывает раннюю зрелость рынка и слабую способность покупать отдельный best-of-breed tool. [T2: https://www.tadviser.ru/index.php/Статья:Искусственный_интеллект_(рынок_России)]
- На Habr есть только точечные инженерные публикации про Langfuse и observability для AI-агентов, то есть ниша существует скорее как dev-практика, чем как массово закупаемый софт-слой. [T3, supported by T2: https://habr.com/ru/articles/987230/ ; internal demand endpoint]

## Real competitors with prices
1. **Braintrust**: free plan **$0/мес**, paid plan **$249/мес**, далее custom enterprise; включено 5 GB processed data, overage **+$3/GB**, 50k scores included, далее **$1.50 за 1,000**. По курсу ЦБ РФ на **21.04.2026** это примерно **18,7 тыс. ₽/мес** за paid tier. [T2: https://www.braintrust.dev/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
2. **Langfuse**: Core **$29/мес**, Pro **$199/мес**, Enterprise **$2,499/мес**, additional usage **$8/100k units**. Это примерно **2,2 тыс. ₽ / 15,0 тыс. ₽ / 188 тыс. ₽** в месяц по курсу ЦБ РФ. [T2: https://langfuse.com/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
3. **Helicone**: Pro **$79/мес**, Team **$799/мес**, enterprise custom. Это примерно **5,9 тыс. ₽** и **60,1 тыс. ₽** в месяц по курсу ЦБ РФ. [T2: https://www.helicone.ai/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
4. **Portkey**: Production **$49/мес**, overage **$9 за каждые 100k requests**, enterprise custom. Это примерно **3,7 тыс. ₽/мес** по курсу ЦБ РФ. [T2: https://portkey.ai/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]

### Что означает ценовая вилка
- Публичная cloud-вилка direct competitors находится примерно в диапазоне **2,2 тыс. ₽ - 60,1 тыс. ₽ в месяц** до enterprise custom. [T1][T2]
- Это слишком низкая отправная точка для уверенного прохождения Profit Gate на российском рынке, если продавать как standalone observability SaaS. [T1][T2, inference]
- Одновременно категории сильно помогают open-source/self-hosted alternatives, поэтому российский buyer часто может начать с Langfuse/Phoenix/Grafana stack без тяжелой годовой подписки. Это снижает willingness to pay именно за отдельный vendor layer. [T2][T3]

## Telegram bots / services in RU
- Специализированных российских Telegram-ботов с заметной дистрибуцией именно под **LLM observability / evals / tracing** я не нашел; mandatory endpoint также вернул `telegram subscribers = 0`. [T2: internal demand endpoint]
- В РФ есть скорее инженерные и cloud-сервисы общего observability/monitoring класса, а не Telegram-first продукты для AI evals. [T2, inference]
- Вывод: Telegram не является существующим каналом рыночной дистрибуции для этой категории в РФ. [T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: глобальные игроки действительно продают продукт, причем не только enterprise custom, но и по публичным тарифам от **$29** до **$799** в месяц. Значит, willingness to pay у мирового рынка существует. [T2]
- **Доказательство WTP №2**: TAdviser фиксирует общие AI-бюджеты в РФ на уровне **90,3 млрд ₽** в 2024 году, то есть деньги на AI-инструменты в стране уже есть. [T2]
- **Но ключевое ограничение**: в РФ не видно прямых признаков, что buyer готов платить именно за отдельный слой AI observability. Endpoint дает **LOW**, hh proxy = **0**, Telegram = **0**, а локальный контентный след почти целиком инженерный. Поэтому локальный WTP надо считать **слабым и косвенным**, а не доказанным. [T2][T3]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/eng/currency_base/daily/]
- Global anchor: Gartner прогнозирует мировой **AI Software** рынок в **$452,458 млрд** в 2026 году. Для observability/evals/tracing берем лишь **1%** этого слоя как addressable proxy, так как продукт покрывает узкую инфраструктурную подкатегорию, а не весь AI software. Это именно аналитическое допущение, а не прямой market statistic. [T1: https://www.gartner.com/en/newsroom/press-releases/2026-1-15-gartner-says-worldwide-ai-spending-will-total-2-point-5-trillion-dollars-in-2026 ; inference]
- Russia anchor: в РФ расходы крупных и средних организаций на ИИ составили **90,3 млрд ₽** в 2024 году. Для AI observability/evals берем **1,5%** этого пирога как proxy TAM РФ, потому что category spend обычно заметно ниже spend на модели, интеграцию и инфраструктуру. Это оценка с умеренной неопределенностью. [T2: TAdviser/FinExpertiza ; inference]
- Bottom-up avg ARR для РФ принимаю как **9 млн ₽/год** на одного enterprise-клиента. Это соответствует тяжелому on-prem / private deployment / compliance sale, а не self-serve тарифу. [T1][T2, inference]

### Top-down
- **TAM (мир)** = $452,458 млрд × 1% = **$4,525 млрд** ≈ **340,5 млрд ₽**. [T1 + inference]
- **TAM (РФ)** = 90,3 млрд ₽ × 1,5% = **1,35 млрд ₽**. [T2 + inference]
- **SAM (РФ)** = TAM РФ × 20% (только крупные enterprise buyers с production LLM, security/compliance и отдельной платформенной командой) = **270,9 млн ₽**. [T2 + inference]
- **SOM Y1** = SAM × 4% = **10,8 млн ₽**. [inference]
- **SOM Y3** = SAM × 12% = **32,5 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **100** крупных российских организаций с собственными AI/LLM-командами и production-контуром. Это оценка по крупным банкам, маркетплейсам, телекомам, bigtech, интеграторам и большим industrial groups, а не статистически точный реестр. [T2/T3, спекуляция]
- **% with need** = **28%**. То есть только часть таких компаний дошла до стадии, где отдельный слой tracing/evals реально нужен и budget-izable. Низкий endpoint score поддерживает консервативность, но сама доля остается экспертной оценкой. [T2, inference]
- **SAM_bottom_up** = 100 × 28% × 9 млн ₽ = **252,0 млн ₽**. [T2 + inference]
- **SOM_bottom_up Y1** = **3 клиента** × 9 млн ₽ = **27,0 млн ₽** выручки в год. [inference]
- **SOM_bottom_up Y3** = **8 клиентов** × 9 млн ₽ = **72,0 млн ₽** выручки в год. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 340,5 млрд ₽ [T1] | — | — | top-down |
| TAM (РФ) | 1,35 млрд ₽ [T2] | 900,0 млн ₽ [T2/T3] | diff=1,5x, допустимо: bottom-up ограничен только крупным enterprise buyer pool | lower |
| SAM (РФ) | 270,9 млн ₽ [T2] | 252,0 млн ₽ [T2] | diff=7%, гипотезы сходятся | lower |
| SOM Y1 | 10,8 млн ₽ | 27,0 млн ₽ | diff=2,5x, но обе оценки малы для fund-scale outcome | **используем 10,8 млн ₽** |
| SOM Y3 | 32,5 млн ₽ | 72,0 млн ₽ | diff=2,2x, обе оценки ограничены узким buyer universe | **используем 32,5 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **Сбер** [T2: https://www.sberbank.com/]
2. **Яндекс / Yandex Cloud** [T2: https://yandex.ru/company/]
3. **Т-Банк** [T2: https://www.tbank.ru/]
4. **МТС / MTS AI** [T2: https://mts.ai/]
5. **VK** [T2: https://vk.company/]
6. **Avito Tech** [T2: https://avito.tech/]
7. **Ozon Tech** [T2: https://job.ozon.ru/tech/]
8. **X5 Tech** [T2: https://tech.x5.ru/]
9. **Альфа-Банк** [T2: https://alfabank.ru/]
10. **Positive Technologies** [T2: https://www.ptsecurity.com/ru-ru/]

Sanity check: при среднем цикле сделки **9-12 месяцев** даже закрытие 3 контрактов в Y1 уже напряженно для новой команды без локального brand equity. Поэтому bottom-up SOM Y1 = 27 млн ₽ выглядит скорее верхней границей, а не base case. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve cloud
- Ценовой ориентир категории: **2,2-18,7 тыс. ₽/мес** за аккаунт/проектный тариф по глобальным comparable. [T1][T2]
- Чтобы получить **500 тыс. ₽ EBITDA/мес**, нужна многократно большая выручка, а в РФ прямой спрос по категории пока почти отсутствует. [T2]
- Вывод: **FAIL**. [T2]

### Сценарий B. Mid-market SaaS для команд разработчиков
- Реалистичный чек в РФ выглядел бы как **30-80 тыс. ₽ MRR** на команду, иначе buyer почти наверняка уходит в open source/self-hosted. [T2][T3, inference]
- Для EBITDA 500 тыс. ₽/мес при gross margin 75% и минимальной локальной команде продаж/solutions/support пришлось бы держать десятки платящих аккаунтов, чего demand evidence не поддерживает. [T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий C. Enterprise on-prem / private cloud
- Теоретически чек **9 млн ₽ ARR** на крупного клиента возможен. [T2, inference]
- Но для **500 тыс. ₽ EBITDA/мес** понадобятся как минимум **4-5** активных enterprise-клиентов при локальной команде presales, solution architect, customer success и legal/compliance overhead. При текущем buyer universe и demand LOW это выглядит слишком тяжело. [T2, inference]
- Вывод: **скорее FAIL**, не проходит как надежно достижимый сценарий. [T2]

### Сценарий D. Интеграторский / reseller channel
- Этот путь может ускорить первые пилоты, но обычно съедает маржу и делает vendor зависимым от кастомных внедрений. [T2, inference]
- При и без того небольшом SAM он не решает Profit Gate, а чаще переводит компанию в services-heavy модель. [T2]
- Вывод: **FAIL**. [T2]

## Risks
- Категория в РФ слишком ранняя, direct demand по endpoint = **LOW**. [T2]
- У buyer есть бесплатные и open-source substitutes, поэтому ценовая власть vendor ограничена. [T2][T3]
- Нужен долгий enterprise presale с compliance/data residency, что ухудшает unit economics. [T2]
- Российский рынок production LLM команд заметно уже, чем мировой шум вокруг категории. [T2]

## Verdict for P4
- **P4 verdict**: **REJECTED (early)**.
- Обоснование: demand endpoint вернул **LOW**, а Profit Gate не проходит ни в self-serve, ни в mid-market, ни в enterprise, ни в reseller сценарии. [T2]
- Следствие: кейс не продолжаем в P5-P7, оформляем reject на P4. [T2]

Sources: T1=2, T2=12, T3=2. Primary evidence basis: T2.
