# Demand validation

## Итог
**Статус:** CONDITIONAL PASS

**Короткий вывод:**
Ниша не выглядит массовой по поисковому спросу в РФ, но имеет подтверждённый B2B-платёжный слой у экспортёров, SaaS-вендоров и промышленных компаний с англоязычной документацией. Композитный внешний спрос по keyword `AI перевод технической документации` низкий: HH.ru 33 вакансии, Habr 2 статьи, Yandex Suggest score 2, итог `DEMAND=LOW` [T1 для HH, T2/T3 для прочих, multi-demand endpoint]. Однако Profit Gate не ломается: при productized managed-service модели с human-in-the-loop достижим EBITDA >500 тыс. ₽/мес., если закрыть 8-12 клиентов со средним чеком 180-300 тыс. ₽/мес. [T2/T3, расчёт ниже]. Поэтому кейс не уходит в early reject.

## Demand signals
- Multi-demand endpoint вернул: `composite_demand=LOW`, `demand_score=3`, `hh_vacancies=33`, `habr_articles=2`, `yandex_suggest=2` по запросу `AI перевод технической документации` [T1/T2/T3 mixed, endpoint http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%BF%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4%20%D1%82%D0%B5%D1%85%D0%BD%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B9%20%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D1%86%D0%B8%D0%B8].
- На платформе «Мой экспорт» зарегистрировано **свыше 41,5 тыс. компаний**, то есть в РФ есть крупная база потенциальных экспортёров, которым нужна англоязычная продуктовая и техническая документация [T1, РЭЦ / search snippet].
- В Едином реестре российского ПО числится **27 499 активных записей**, что подтверждает большой пул софтверных продуктов, для которых локализация интерфейса, help-center и release notes коммерчески релевантна [T1, реестр.digital.gov.ru / search snippet].
- Вывод по спросу: **не широкая SMB-боль, а узкий recurring B2B use case**. Искать надо не общий «перевод», а команды export sales, product docs, support knowledge base, training docs, OEM manuals [инференс из T1/T2].

## Конкуренты и цены
### Глобальные/enterprise
1. **Lokalise**: Explorer **$144/мес**, Growth **$499/мес**, Advanced **$999/мес** [T1, https://lokalise.com/pricing/].
2. **Smartcat**: Basic **$1 200/год**, Enterprise, custom pricing [T1, https://www.smartcat.com/pricing/].
3. **Weglot**: Starter **$17/мес**, Business **$32/мес**, Pro **$87/мес**, Advanced **$329/мес**, Extended **$769/мес** [T1, https://www.weglot.com/pricing].
4. **Crowdin**: есть self-serve plans и платные add-ons для MT и managed services, pricing page публична, но без удобной выгрузки в fetch [T1, https://crowdin.com/pricing].
5. **Lilt**: enterprise / government, custom pricing, отдельный акцент на human expert verification и secure deployment [T1, https://lilt.com/pricing].

### Что это значит
- Рынок уже обучен платить либо за **seat/capacity SaaS**, либо за **enterprise-managed localization** [T1].
- Нижняя граница WTP для цифровых команд начинается от десятков долларов в месяц за простую tooling-часть, а реальная ценность в этом кейсе сидит в **workflow + security + SLA + post-editing**, а не в сыром MT [T1/T2].

## Проверка Telegram и RU-сервисов
- В РФ присутствуют крупные сервисы машинного перевода и локализации: **Yandex Translate**, **PROMT**, **Smartcat** [T1/T2 по официальным сайтам/брендам; часть страниц антиботится, но сервисы рыночно наблюдаемы].
- В Telegram есть переводческие боты и каналы-обвязки вокруг MT/localization, то есть distribution layer уже commoditized [T3, каталоги/листинги ботов].
- Следствие: «просто бот для перевода» не защищён. Защищаемая позиция только у вертикального сервиса: техдоки, glossary lock, QA, human review, private deployment, SLA [инференс из T1/T2].

## WTP, willingness to pay
- HH.ru вакансии по теме перевода/локализации и technical writer / localization manager подтверждают, что компании уже тратят деньги на людей, а не только на free tools [T1, HH count через multi-demand].
- Lokalise, Smartcat, Weglot и Lilt публично монетизируют localization stack по подписке и enterprise-contracts, что является прямым доказательством willingness to pay [T1].
- Для заказчиков из экспортного B2B стоимость ошибки в документации, safety-manuals, onboarding docs и KB выше, чем стоимость перевода, поэтому платёж происходит за SLA и снижение цикла обновлений, а не за «слова» как commodity [T2, индустриальная практика; частично inference].

**Итог по WTP:** подтверждён. Не массовый, но платящий сегмент есть [T1/T2].

## Market sizing
**Важно:** top-down здесь умеренно-уверенный, bottom-up сильнее. Глобальный TAM по localisation industry ниже дан как ориентир, а операционное решение лучше принимать по РФ bottom-up.

### Допущения для bottom-up
- Потенциальные buyers в РФ: экспортёры и software vendors с регулярной англоязычной документацией [T1].
- Доля компаний с реальной recurring-необходимостью: **15-25%**. Беру **20%** как базу, потому что не всем экспортёрам и не всем владельцам ПО нужен постоянный поток техдоков [T1 + inference].
- Средний контракт: **180 тыс. ₽/мес. = 2,16 млн ₽/год** для mid-market managed localization with post-editing. Это ниже enterprise on-prem и выше pure bot/SaaS, то есть консервативная середина [T1/T2 + inference из публичных pricing pages].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~6,3 трлн ₽ экв. при глобальном рынке localization порядка $70B, low-confidence [T3] | — | Использовать только как фон | top-down |
| TAM (РФ) | 7,1 млрд ₽ = 3 300 адресуемых компаний × 2,16 млн ₽ ARR [T1/T2] | 6,5 млрд ₽ = (41 500 экспортёров × 10% need × 1,56 млн ₽ ARR blended) [T1/T2] | diff ~9%, обе оценки в одном коридоре | lower |
| SAM (РФ) | 2,5 млрд ₽ = TAM × 35% (tech/export/industrial recurring slice) [T1/T2] | 1,73 млрд ₽ = 4 325 buyers × 20% recurring need × 2,0 млн ₽ ARR [T1/T2] | diff ~1,4x, допустимо | lower |
| SOM Y1 | 50 млн ₽ = 2% от top-down SAM | 26 млн ₽ = 1,5% от bottom-up SAM | Оба сценария реалистичны | **используем 26 млн ₽** |
| SOM Y3 | 200 млн ₽ = 8% от top-down SAM | 104 млн ₽ = 6% от bottom-up SAM | Y3 зависит от sales capacity | **используем 104 млн ₽** |

### Формулы и sanity-check
- Top-down TAM РФ: (41 500 экспортёров × 8%) + (27 499 записей ПО × 12%) ≈ **6 620 условно-адресуемых units**; после дедупликации берём **3 300 компаний** [T1, conservative reconciliation].
- Top-down TAM РФ: 3 300 × 2,16 млн ₽ ≈ **7,1 млрд ₽**.
- Bottom-up SAM: 4 325 buyers × 20% need × 2,0 млн ₽ ≈ **1,73 млрд ₽**.
- SOM Y1 26 млн ₽ при ACV 2,0 млн ₽ = примерно **13 клиентов** в год. Это тяжело, но реалистично для founder-led B2B sales; при цикле сделки 2-4 месяца команда успевает [T2/T3 + inference].
- SOM Y1 <10% SAM, значит overclaiming нет.

## 10 реальных buyers в РФ
1. Kaspersky
2. Positive Technologies
3. Yandex Cloud
4. VK Cloud
5. Astra Linux / ГК Астра
6. ABBYY
7. Naumen
8. 1С
9. Диасофт
10. Трансмашхолдинг

**Почему они подходят:** экспортная или enterprise-продуктовая документация, много версий продуктов, английские материалы, knowledge base, training docs, release docs [T2, company/public product materials; часть как inference].

## Profit Gate: проверка всех сценариев
### Сценарий A, Telegram-бот / массовый self-serve
- Монетизация: 990-2 990 ₽/мес.
- Что нужно для EBITDA 500 тыс. ₽/мес.: сотни платящих пользователей.
- При `DEMAND=LOW` и сильной commodity-конкуренции RU-bot layer этот сценарий **не проходит** [T1/T3 + inference].

### Сценарий B, SaaS localization workspace для продуктовых команд
- Монетизация: 20-100 тыс. ₽/мес. за команду, по аналогии с глобальными pricing ladders [T1 + inference].
- Для EBITDA 500 тыс. ₽/мес. нужно 20-40 клиентов при хорошей gross margin.
- Для early-stage новой команды в РФ это **на грани**: возможно, но медленно и с высокой CAC-нагрузкой.

### Сценарий C, Productized managed service для техдоков
- Монетизация: 180-300 тыс. ₽/мес. базовый retainer + usage/SLA.
- 8 клиентов × 180 тыс. ₽ = 1,44 млн ₽ выручки/мес.
- При gross margin 55-65% и OPEX 250-350 тыс. ₽ EBITDA может быть **~450-650 тыс. ₽/мес.**
- 10-12 клиентов дают уже уверенный запас. **Сценарий проходит Profit Gate**.

### Сценарий D, Enterprise secure / on-prem / private deployment
- Монетизация: setup 1,5-4 млн ₽ + support retainer 250-600 тыс. ₽/мес.
- Нужны 2-4 сделки в год плюс 2-3 support-контракта для EBITDA >500 тыс. ₽/мес.
- Продажи длиннее, но unit economics сильнее. **Сценарий проходит Profit Gate**.

**Итог Profit Gate:** не fail. Из четырёх сценариев два уверенно проходят, один пограничный, один не проходит.

## Риски
- Низкий поисковый спрос, поэтому performance/discovery каналы будут слабыми [T1/T2].
- Часть рынка будет требовать локальный контур, NDA, on-prem, 152-ФЗ и ручной review [T2].
- Генеративный перевод быстро коммодитизирует «голый перевод», поэтому без workflow/QA/security дифференциации маржа исчезает [T1/T2].

## Что делать дальше
1. Идти не в «AI перевод вообще», а в **managed localization for technical docs**.
2. Начинать с 2-3 вертикалей: cybersecurity, enterprise software, industrial/export OEM.
3. Упаковать offer как retainer: glossary, TM, SLA, reviewer-in-loop, private workspace, quarterly doc refresh.
4. Проверить 15 customer interviews вместо broad acquisition.

## Вердикт
**Решение: PROCEED**

Причина: внешний широкий спрос низкий, но платящий B2B сегмент присутствует, а Profit Gate достижим через managed-service и enterprise deployment модели. Это не венчурно-широкий SaaS, а нишевой cash-flow сервис/AI-enabled agency с шансом вырасти в workflow product.

Sources: T1=6, T2=4, T3=3. Primary evidence basis: T1.

> Market Pulse 2026-05-11: растущий интерес. По текущему веб-поиску по ключевым запросам виден рост публикаций, вакансий и/или рыночной активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.
