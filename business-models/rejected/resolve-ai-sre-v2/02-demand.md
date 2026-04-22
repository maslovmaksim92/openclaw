# 02-demand

## Demand validation summary
- **Продукт**: Resolve AI, AI-native incident response / SRE copilot для production engineering, triage, postmortems и on-call workflows. [T2: 00-brief.md; https://resolve.ai/]
- **Итог по спросу в РФ**: **LOW**. Обязательный endpoint по ключу `AI SRE incident response automation` вернул **LOW**, score **0**, `hh.ru vacancies = 1`, `google trends RU = 0`, `yandex suggest = 2`, `habr = 2`. Более широкий proxy `SRE incident management` тоже дал **LOW**, score **3**, хотя вакансий уже **11**. Это означает, что инженерная функция SRE в РФ есть, но отдельная закупочная категория AI incident response пока не сформирована. [T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand?keyword=AI%20SRE%20incident%20response%20automation ; http://172.18.0.1:9001/multi-demand?keyword=SRE%20incident%20management]
- **Итог по Profit Gate**: **FAIL**. Даже если enterprise-чек теоретически возможен, локальный buyer universe узкий, search demand низкий, а существующие зарубежные и российские аналоги задают либо низкую per-user цену, либо уже закрывают incident stack end-to-end. Надёжно выйти на **500 тыс. ₽ EBITDA в месяц** в РФ не получается ни в одном реалистичном сценарии. [T1][T2][T3]
- **Решение P4**: **EARLY REJECT**. Одновременно выполняются оба условия: direct demand = **LOW** и Profit Gate не проходит. [T2]

## Evidence of demand

### 1) Mandatory endpoint
- `AI SRE incident response automation` → **LOW**, score **0**, `hh.ru vacancies = 1`, `google trends RU = 0`, `habr = 2`, `yandex suggest = 2`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `SRE incident management` → **LOW**, score **3**, `hh.ru vacancies = 11`, `google trends RU = 0`, `habr = 2`, `yandex suggest = 2`. [T2: internal demand endpoint]
- Интерпретация: в РФ видна инженерная база вокруг SRE и incident handling, но не видно выраженного спроса именно на отдельный AI-native слой автоматизации incident response. [T2, inference]

### 2) Дополнительные сигналы рынка
- На hh.ru по запросу `SRE` в России найдено **116 вакансий**; среди работодателей на выдаче видны Сбер, Ozon, Wildberries & Russ, Альфа-Банк, Т-Банк, МТС, РТК-ЦОД, Cloud.ru, BI.ZONE и SberTech. Это подтверждает наличие реальной функции reliability/platform engineering у крупных российских digital-компаний. [T1: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
- Банк России фиксирует **305 действующих банков** и **53 НКО** на 1 апреля 2026 года, а также **129 страховых организаций** на 1 января 2026 года. Это важный proxy для regulated buyer universe, где простой и инциденты действительно стоят дорого. [T1: https://www.cbr.ru/banking_sector/ ; https://www.cbr.ru/insurance/]
- TAdviser со ссылками на рынок ИИ в РФ пишет, что российские компании тратят на внедрение ИИ **более 90 млрд ₽ в год**, но реально используют ИИ лишь около **6% организаций**. Это подтверждает наличие AI-бюджетов вообще, но не доказывает сформированную budget line под AI-SRE tooling. [T2: https://www.tadviser.ru/index.php/Статья:Искусственный_интеллект_(рынок_России)]

## Real competitors with prices
1. **PagerDuty Incident Management**: Free до 5 users, **Professional $21/user/month** при yearly billing, **Business $41/user/month**, Enterprise custom. По курсу ЦБ РФ на **22.04.2026** (`1 USD = 74,5897 ₽`) это примерно **1 566 ₽** и **3 058 ₽** за пользователя в месяц. [T2: https://www.pagerduty.com/pricing/incident-management/ ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=22/04/2026]
2. **incident.io**: Basic free, **Team $15/user/month** annual или **$19 monthly**, Pro **$25/user/month**, On-call add-on **+$10-20/user/month**. Это примерно **1 119 ₽**, **1 417 ₽**, **1 865 ₽** и ещё **746-1 492 ₽** за on-call на пользователя в месяц. [T2: https://incident.io/pricing ; T1 FX]
3. **FireHydrant Signals**: **$9 600/year** за plan Pro, то есть около **$800/month** или примерно **59 672 ₽/мес** за команду. [T2: https://firehydrant.com/pricing/ ; T1 FX]
4. **Status200 (РФ)**: **Базовый — бесплатно**, **Старт — 1 040 ₽/мес**, **Про — 1 600 ₽/мес**, **Корпоративный — по запросу**. Платформа уже закрывает мониторинг, инциденты, дежурства и статус-страницы в одном российском продукте. [T2: https://status200.ru/]

### Что означает ценовая вилка
- Публичный price anchor рынка находится примерно между **1 тыс. ₽ и 60 тыс. ₽ в месяц** для team/self-serve слоёв до enterprise custom. [T1][T2]
- Это плохой фон для Resolve AI как standalone vendor в РФ: чтобы пройти Profit Gate, продукту пришлось бы продаваться заметно выше рынка или превращаться в services-heavy enterprise motion. [T1][T2, inference]
- Наличие уже локального продукта Status200 усиливает pressure: российский buyer может закрыть базовые incident, on-call и notification workflows без дорогого AI-native слоя. [T2, inference]

## Telegram bots / services in RU
- **Status200** прямо поддерживает локальные уведомления через **Telegram**, звонки на российские номера, SMS, Max, Loop и Mattermost. [T2: https://status200.ru/]
- **readyz.io** обещает мониторинг доступности сайта/API с уведомлениями в **Telegram и на почту**, включая бесплатный тариф на 5 проверок. [T2: https://readyz.io/]
- **handy-site.ru / @checkmyservicebot** позиционируется как сервис мониторинга доступности сайта с мгновенными уведомлениями в **Telegram**, бесплатным планом `0 ₽` и Telegram-first UX. [T2: https://www.handy-site.ru/]
- Следовательно, Telegram в РФ уже является рабочим каналом доставки алертов и мониторинга, но найденные сервисы в основном закрывают **notification / uptime monitoring**, а не полноценный AI incident commander для SRE-команд. [T2, inference]

## WTP, willingness to pay
- **Доказательство WTP №1**: глобальные игроки PagerDuty, incident.io и FireHydrant продают incident stack по recurring-модели, а не как разовую услугу. Это подтверждает, что на зрелых рынках buyer готов платить за on-call и incident tooling. [T2]
- **Доказательство WTP №2**: в РФ уже есть локальный платящий слой вокруг мониторинга и incident management, например Status200 с платными тарифами **1 040-1 600 ₽/мес** и enterprise upsell. [T2]
- **Доказательство WTP №3**: hh.ru показывает фактический hiring спрос на SRE-функцию, значит проблема uptime/incident response для части крупных компаний реальна и budget-owning. [T1]
- **Но**: доказательство готовности платить именно за **AI-native automation layer** в РФ слабое. Mandatory endpoint остаётся LOW, специализированных Telegram-first AI incident продуктов не видно, а базовые workflow уже закрываются более дешёвыми продуктами. Поэтому локальный WTP для Resolve AI надо считать **слабым и косвенным**, а не подтверждённым. [T1][T2]

## Market sizing

### Методика и допущения
- Курс пересчёта: **1 USD = 74,5897 ₽** по курсу Банка России на **22.04.2026**. [T1: https://www.cbr.ru/scripts/XML_daily.asp?date_req=22/04/2026]
- Глобальный proxy: рынок **AIOps** в 2025 году оценён в **$2,23 млрд**, а в 2026 году прогнозируется **$2,67 млрд**. Это не чистый incident response market, а более широкий adjacent category, поэтому top-down ниже помечен как proxy. [T3: https://www.fortunebusinessinsights.com/aiops-market-109984]
- Российский proxy спроса: берём только крупные digital companies и regulated enterprises, где есть SRE/on-call функция. Для buyer universe опираемся на ЦБ РФ и фактический hh signal по SRE, а не на весь ИТ-рынок. [T1]
- Average ARR для bottom-up беру как **3,6 млн ₽/год** на одного enterprise-клиента, то есть около **300 тыс. ₽/мес**. Это уже aggressive price point относительно локальных и глобальных public anchors, но ниже heavy consulting motion. [T1][T2, inference]

### Top-down
**[LOW CONFIDENCE]** Категория Resolve AI находится на пересечении AIOps, incident management, on-call и automation, поэтому прямого чистого TAM нет, приходится использовать proxy.

- **TAM (мир)**: используем 2026 AIOps market **$2,67 млрд**, или примерно **199,2 млрд ₽**. [T3 + T1 FX]
- Для Resolve AI берём только incident-response / automation slice на уровне **15%** от broader AIOps proxy. Получаем адресуемый глобальный слой порядка **29,9 млрд ₽**. Это аналитическое допущение, а не прямой статистический факт. [T3, inference]
- **TAM (РФ)**: применяем грубую долю РФ **1,5%** от addressable global slice как proxy для большого enterprise IT-ландшафта и high-criticality отраслей. Получаем **448 млн ₽**. [T1/T3, inference]
- **SAM (РФ)**: берём **60%** от TAM РФ, потому что продукт подходит не всем enterprise-командам, а только тем, у кого есть круглосуточные дежурства, инцидентный процесс и достаточная зрелость. Получаем **268,8 млн ₽**. [T1/T3, inference]
- **SOM Y1**: **4%** SAM = **10,8 млн ₽**. [inference]
- **SOM Y3**: **12%** SAM = **32,3 млн ₽**. [inference]

### Bottom-up
- **Total buyers**: база из **603** regulated организаций по ЦБ РФ, то есть **305 банков + 129 страховщиков + 53 НКО + 116 SRE vacancies proxy на hh.ru** как дополнительный индикатор цифрово зрелых команд. Чтобы не считать дублей и не завышать рынок, консервативно округляю рабочий buyer pool до **220** крупных организаций с реальным шансом иметь зрелый incident/on-call процесс. [T1 + inference]
- **% with need**: **22%**. Это доля компаний, у которых одновременно есть 24/7 критичные сервисы, выделенная platform/SRE команда и готовность рассматривать новый automation layer поверх текущего monitoring stack. Низкий mandatory demand score заставляет брать консервативную долю. [T1][T2, inference]
- **SAM_bottom_up** = **220 × 22% × 3,6 млн ₽ = 174,24 млн ₽**. [T1][T2, inference]
- **SOM_bottom_up Y1** = **3 клиента × 3,6 млн ₽ = 10,8 млн ₽**. [inference]
- **SOM_bottom_up Y3** = **7 клиентов × 3,6 млн ₽ = 25,2 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 29,9 млрд ₽ [T3] | — | proxy через AIOps slice | top-down |
| TAM (РФ) | 448,0 млн ₽ [T1/T3] | 792,0 млн ₽ [T1] | diff=1,8x, bottom-up считает более широкий buyer pool, top-down жёстче режет category slice | lower |
| SAM (РФ) | 268,8 млн ₽ [T1/T3] | 174,2 млн ₽ [T1/T2] | diff=1,5x, приемлемо для proxy category | lower |
| SOM Y1 | 10,8 млн ₽ | 10,8 млн ₽ | diff=0%, оценки сошлись | **используем 10,8 млн ₽** |
| SOM Y3 | 32,3 млн ₽ | 25,2 млн ₽ | diff=1,3x, обе оценки остаются нишевыми | **используем 25,2 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **Сбер** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
2. **Ozon** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
3. **Wildberries & Russ** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
4. **Альфа-Банк** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
5. **Т-Банк** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
6. **МТС** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
7. **РТК-ЦОД** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
8. **Cloud.ru** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
9. **BI.ZONE** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]
10. **SberTech** [T1/T2: https://hh.ru/search/vacancy?text=SRE&search_field=name&area=113]

Sanity check: при среднем цикле сделки **6-9 месяцев** закрытие даже **3 клиентов** за первый год уже напряжённо для новой команды без локального бренда и без reference-клиентов. Это ещё один аргумент против агрессивного SOM. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve / team SaaS
- Ценовая вилка comparable-игроков: примерно **1,1-3,1 тыс. ₽ за пользователя в месяц** или low-thousands ₽ team-plan у локальных сервисов. [T1][T2]
- Даже если продавать по **50 тыс. ₽/мес** на команду, для EBITDA **500 тыс. ₽/мес** понадобятся десятки активных аккаунтов сверх локального demand evidence. [T1][T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий B. Mid-market platform plan
- Теоретический чек: **120-180 тыс. ₽/мес** на зрелую DevOps/SRE-команду. Это уже сильно выше локального public pricing и потребует доказанного AI value в triage/postmortems. [T2, inference]
- Чтобы пройти EBITDA gate при gross margin около 75%, пришлось бы удерживать **10-15** средних клиентов. Для категории с endpoint LOW это выглядит нереалистично. [T2, inference]
- Вывод: **FAIL**. [T2]

### Сценарий C. Enterprise SaaS / private deployment
- Теоретически возможен чек **300 тыс. ₽/мес** или **3,6 млн ₽ ARR** на крупный банк, маркетплейс или облачного провайдера. [T1][T2, inference]
- Но чтобы стабильно получить **500 тыс. ₽ EBITDA/мес**, нужно примерно **6-8** платящих enterprise-клиентов при локальной команде presales, solution engineer, support и security/compliance overhead. [T2, inference]
- С учётом buyer universe, длинного цикла сделки и слабого direct demand это не выглядит надёжно достижимым. [T1][T2]
- Вывод: **скорее FAIL**, как repeatable motion не проходит. [T2]

### Сценарий D. Hybrid SaaS + managed incident engineering
- Этот сценарий повышает чек до **400-600 тыс. ₽/мес**, но быстро сдвигает модель в сторону дорогого сервиса и кастомных внедрений. [T2, inference]
- Для фонда это ухудшает масштабируемость и не решает проблему узкого рынка; компания начинает конкурировать не с PagerDuty, а с локальными SRE/DevOps integrators. [T2, inference]
- Вывод: **FAIL**. [T2]

## Risks
- Категория в РФ слишком ранняя: mandatory demand endpoint даёт **LOW**. [T2]
- Уже существуют более простые и дешёвые substitutes: PagerDuty-class tools globally и локальные monitoring/incident platforms в РФ. [T2]
- Buyer может решить проблему не продуктом, а комбинацией текущего мониторинга, Telegram-алертов и внутреннего runbook-процесса. [T2, inference]
- Чтобы продавать AI layer, нужны reference wins и сильная локальная интеграционная история, которых пока не видно. [T2]

## Verdict for P4
- **P4 verdict**: **REJECTED (early)**.
- Обоснование: direct demand остаётся **LOW**, а Profit Gate не проходит ни в self-serve, ни в mid-market, ни в enterprise, ни в hybrid services сценарии. [T2]
- Следствие: кейс останавливается на этапе P4 Demand Validation и перемещается в rejected. [T2]

Sources: T1=5, T2=10, T3=1. Primary evidence basis: T2.
