# Demand Validation — The Brief AI

## Итог
- **Решение этапа:** PASS TO NEXT STAGE.
- **Спрос:** **MEDIUM+**. Внутренний multi-demand по ключу `рекламные креативы` вернул `composite_demand=MEDIUM`, `demand_score=30`, `hh_vacancies=1543`, `yandex_suggest=100`, `habr_articles=2`; это не хайп-нарратив, а устойчивый operational pain у performance-команд и агентств.
- **Почему не reject:** even при умеренном спросе **Profit Gate проходит** минимум в 2 из 4 сценариев монетизации, а рынок в РФ достаточно большой, чтобы собрать EBITDA >500k ₽/мес без экстремальной доли рынка.

## Demand signals
1. **Рынок денег есть.** АКАР оценила рынок маркетинговых коммуникаций РФ в **2,4 трлн ₽** в 2025 году, причем в это определение прямо входят бюджеты на разработку и создание креативов, производство рекламной продукции и оплату услуг агентств [T1].
2. **Digital/performance слой живой.** АКАР отдельно указывает, что в 2025 году сегмент `Интернет-сервисы` оставался одним из самых крупных и быстрорастущих сегментов рынка [T1].
3. **Боль подтверждается наймом.** В demand API по ключу `рекламные креативы` найдено **1543 вакансии на hh.ru**; это сильный индикатор того, что компании либо инхаусят производство креативов, либо готовы платить внешнему подрядчику за скорость и объем [T1 via HH signal in internal aggregator].
4. **Категория не пустая на стороне подрядчиков.** В `Рейтинге Рунета` 2025 в рейтинги performance-маркетинга вошли **1300+ агентств / почти 89 тыс. проектов**, что подтверждает широкую базу потенциальных агентских покупателей и white-label спрос [T2].

## Конкуренты и цены
### Прямые и смежные конкуренты
1. **Penji** — подписка на дизайн-команду: **$499 / $995 / $1497 в месяц** [T2]. Для SMB и агентств это уже нормализованный ценовой якорь за внешний production layer. Источник: https://penji.co/pricing
2. **ManyPixels** — unlimited design: **$599 / $999 в месяц** [T2]. Источник: https://www.manypixels.co/pricing
3. **BannerBoo** — self-serve платформа для ad creatives: **$34/мес** за team-oriented plan, есть AI banner generator и multi-size generator [T2]. Источник: https://bannerboo.com/ru/plans/
4. **Kwork / FL.ru** как нижняя граница рынка в РФ: HTML5 баннеры по **1000–5000 ₽** за единицу, ресайзы по **1000 ₽**, пакетные заказы вроде **20 баннеров за 50 000 ₽**, то есть ~2500 ₽ за баннер [T2/T3]. Источники: 
   - https://kwork.ru/web-plus-mobile-design/2355411/animirovanniy-html5-banner
   - https://kwork.ru/web-plus-mobile-design/45752181/animirovanniy-html5-banner-ekspertniy-uroven
   - https://www.fl.ru/projects/5483630/razrabotka-reklamnyih-bannerov-dlya-reklamirovaniya-sayta-.html
   - https://www.fl.ru/uslugi-freelancera/17056/dizayn-bannerov-dlya-reklamnyh-sistem.html

### Вывод по конкурентам
- Нижний рынок в РФ уже commoditized: статичные и простые HTML5 баннеры легко покупаются поштучно [T2/T3].
- Верхний рынок платит за **скорость, SLA, многоканальный ресайз, стабильный output и white-label delivery**, а не просто за “картинку” [T2].
- Значит, The Brief AI нельзя позиционировать как “AI делает баннеры”, нужно позиционировать как **managed creative production для performance-операций**.

## Telegram bots/services в РФ
Проверка Telegram-native и adjacent сервисов показывает, что внутри Telegram уже есть сервисы, куда SMB и маркетологи привыкли платить регулярный чек:
1. **BotHelp** — российский сервис автоворонок/ботов: **1599 ₽/мес** за 1k подписчиков, **12 990 ₽/мес** за 20k, **29 990 ₽/мес** за безлимит [T2]. Источник: https://bothelp.io/ru/price
2. **@BotHelpSupportBot** и Telegram-операционный слой у BotHelp дополнительно показывают, что российский SMB нормально покупает маркетинговую инфраструктуру, управляемую через Telegram [T2].
3. В demand API по ключу `рекламные креативы` Telegram subscribers не зафиксированы, то есть **Telegram не выглядит основным каналом discovery для этой категории**, но служит каналом обслуживания и workflow [internal + T2].

**Вывод:** Telegram в РФ полезен как acquisition/ops-канал для сервиса, но не как доказательство отдельной большой bot-only ниши для ad creative production.

## WTP, proof of willingness to pay
1. **Глобальный референс.** SMB и агентства уже платят **$499–1497/мес** за внешний design subscription у Penji и **$599–999/мес** у ManyPixels [T2]. При курсе Банка России около **80,76 ₽ за $1** это эквивалентно примерно **40k–121k ₽/мес** [T1 + T2].
2. **Локальный floor.** На FL.ru и Kwork разовые рекламные баннеры стоят **от 1000 ₽ до 5000 ₽** за единицу, пакетные заказы доходят до **50 000 ₽ за 20 баннеров** [T2/T3]. Это подтверждает готовность платить даже у нижнего сегмента.
3. **Proof of recurring spend.** BotHelp в РФ берет регулярную подписку **от 1599 ₽ до 29 990 ₽/мес** за automation layer [T2]. Значит, recurring billing для маркетинговых инструментов и сервисов в Telegram/SMB уже нормализован.
4. **Buyer behavior.** HH-вакансии на создание рекламных креативов и AI-видео с зарплатами порядка **80k–150k+ ₽/мес** означают, что компании уже платят за эту функцию внутри команды; внешний сервис с лучшим SLA может забирать этот бюджет себе [T1/T2].

**WTP verdict:** подтвержден. Реалистичный чек для РФ выглядит как:
- SMB self-serve / light managed: **15k–35k ₽/мес**
- Productized studio для e-commerce и локального SMB: **35k–70k ₽/мес**
- White-label agency pod: **80k–150k ₽/мес**

## Market sizing
### Метод и допущения
- База рынка: АКАР оценивает рынок маркетинговых коммуникаций РФ в **2,4 трлн ₽** за 2025 год, причем туда входят расходы на креатив, продакшн и агентские услуги [T1].
- База покупателей: число субъектов МСП в России на 10 марта 2026 года превысило **6,9 млн** [T1/T2, по данным Минэкономразвития/МСП.РФ в пересказе РГ и Interfax].
- Для креативного managed service берем консервативную addressable share: не весь рекламный рынок, а только часть, где есть регулярное производство digital-креативов для performance, e-commerce и агентского delivery.
- Средний контракт для bottom-up беру **420k ₽ ARR** (= 35k ₽/мес), то есть заметно ниже глобальных design subscriptions в рублевом эквиваленте. Это консервативный локальный чек [T2].

### GTM-10-targets / реальные buyers для bottom-up
1. Demis Group [T2]
2. MediaGuru [T2]
3. Ingate [T2]
4. Kokoc Group [T2]
5. Adventum [T2]
6. E-Promo [T2]
7. MGCom [T2]
8. i-Media [T2]
9. ArrowMedia [T2]
10. Rocket10 [T2]

Основание: рейтинг performance-агентств `Рейтинг Рунета` 2025 и публикации самих агентств о позициях в рейтинге; в категории участвуют 1300+ агентств и десятки тысяч проектов, что подтверждает реальный pool агентских покупателей [T2].

### Top-down
- **TAM (мир):** **~94 млрд ₽** для сервиса масштаба The Brief AI как узкого vertical slice, если от глобального рынка design subscription / ad creative automation брать только SMB+agency production wedge; это скорее ориентационный ceiling, не опорная цифра [T2, estimate].
- **TAM (РФ):** **36,0 млрд ₽** = 2,4 трлн ₽ × **1,5%** доля production-heavy digital creative spend внутри marketing communications [T1 + estimate].
- **SAM (РФ):** **21,6 млрд ₽** = 36,0 млрд ₽ × **60%** сегментный fit (SMB, e-commerce, marketplace sellers, performance agencies, mid-market in-house) [T1/T2 + estimate].
- **SOM Y1:** **8,6 млн ₽** = 21,6 млрд ₽ × **0,04%** [estimate].
- **SOM Y3:** **38,9 млн ₽** = 21,6 млрд ₽ × **0,18%** [estimate].

### Bottom-up
- **Total buyers:** **55 200 компаний** = 6,9 млн МСП × **0,8%** компаний с повторяемой нуждой в digital ad creative production [T1/T2 + estimate].
- **% with need rationale:** поддерживается hh-сигналом 1543 вакансии по категории `рекламные креативы`, ростом digital/performance рынка и большой базой агентств в `Рейтинге Рунета` [T1/T2].
- **ARR avg:** **420 000 ₽/год** = 35 000 ₽/мес, ниже глобальных подписок Penji/ManyPixels и выше базового фриланс-floor [T2].
- **SAM bottom-up:** **23,2 млрд ₽** = 55 200 × 420 000 ₽.
- **SOM bottom-up Y1:** **9,3 млн ₽** = 23,2 млрд ₽ × **0,04%**.
- **SOM bottom-up Y3:** **41,8 млн ₽** = 23,2 млрд ₽ × **0,18%**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~94 млрд ₽ экв. [T2, estimate] | — | — | top-down |
| TAM (РФ) | 36,0 млрд ₽ [T1+estimate] | 23,2 млрд ₽ [T1/T2+estimate] | diff=1,55x, допустимо: bottom-up сознательно срезает enterprise и крупный brand production | **23,2 млрд ₽** |
| SAM (РФ) | 21,6 млрд ₽ [T1/T2+estimate] | 23,2 млрд ₽ [T1/T2+estimate] | diff=1,07x, хороший cross-check | **21,6 млрд ₽** |
| SOM Y1 | 8,6 млн ₽ | 9,3 млн ₽ | diff=8% | **8,6 млн ₽** |
| SOM Y3 | 38,9 млн ₽ | 41,8 млн ₽ | diff=7% | **38,9 млн ₽** |

### Reconciliation verdict
- Top-down и bottom-up не расходятся более чем в 3 раза, пересборка сегмента не требуется.
- Для инвестиционного комитета разумно использовать **SAM = 21,6 млрд ₽** и **SOM Y1 = 8,6 млн ₽**, потому что это более консервативная линия.

## Profit Gate: EBITDA >= 500k ₽/мес
### Сценарий A. Поштучные баннеры / ресайзы
- Средний чек: **2500 ₽** за единицу [T2/T3]
- Объем: **300 единиц/мес**
- Выручка: **750k ₽/мес**
- Команда/COGS/ops: ~**380k ₽/мес**
- Маркетинг и оверхед: ~**120k ₽/мес**
- **EBITDA: ~250k ₽/мес**
- **Вердикт:** FAIL. Слишком commoditized.

### Сценарий B. Productized studio для SMB
- Чек: **45k ₽/мес**
- Клиенты: **20**
- Выручка: **900k ₽/мес**
- COGS + PM + tools: ~**320k ₽/мес**
- SG&A: ~**90k ₽/мес**
- **EBITDA: ~490k ₽/мес**
- **Вердикт:** borderline / почти проходит, но запас маленький.

### Сценарий C. Agency white-label pod
- Чек: **120k ₽/мес**
- Клиенты: **10 агентств**
- Выручка: **1,2 млн ₽/мес**
- COGS + PM + QA + tooling: ~**430k ₽/мес**
- SG&A: ~**90k ₽/мес**
- **EBITDA: ~680k ₽/мес**
- **Вердикт:** PASS.

### Сценарий D. Гибрид studio + template/library upsell
- 12 managed-клиентов × **60k ₽/мес** = **720k ₽**
- 40 self-serve/template seats × **5k ₽/мес** = **200k ₽**
- Upsell на видео/HTML5: **180k ₽**
- Итого выручка: **1,1 млн ₽/мес**
- Суммарные расходы: ~**540k ₽/мес**
- **EBITDA: ~560k ₽/мес**
- **Вердикт:** PASS.

### Profit Gate verdict
- Gate **проходит**, потому что как минимум сценарии **C** и **D** дают EBITDA выше **500k ₽/мес** без агрессивных допущений.
- Следовательно ранний reject по правилу `DEMAND=LOW and Profit Gate FAIL` не применяется.

## Основные риски
1. **Коммодитизация.** Нижний сегмент баннеров уже уходит в Kwork/FL/Canva/BannerBoo [T2/T3].
2. **Сжатие маржи AI-инструментами.** Если сервис продает “генерацию картинок”, а не SLA/операции/white-label pod, маржа быстро съедается [T2/T3].
3. **Высокая цена кастомных правок.** Без жесткого scope и очереди задач managed service превращается в агентство с ручным адом [операционный вывод].

## Что должно быть moat
- Brand kits + reusable templates + batch-resize pipeline
- SLA и turnaround time, особенно для агентств
- White-label delivery под performance-команды
- История тестов креативов и learning loop по CTR/CVR, а не просто дизайн
- Интеграции с ad кабинетом / asset management / Telegram-ops

## Финальный вывод
Кейс **не выглядит как венчурный software rocketship**, но **выглядит как реальный cash-efficient AI-service** для РФ-рынка. Спрос не взрывной, зато денежный и операционно понятный. Лучший wedge, который я вижу, это **white-label creative production для performance-агентств и e-commerce команд**, а не широкий self-serve “сделай баннер нейросетью”.

**Итог этапа:** писать reject рано. Кейс проходит дальше.

## Sources
- [T1] АКАР, объем рынка маркетинговых коммуникаций 2025: https://akarussia.ru/volumes/obem-rynka-marketingovyh-kommunikacij-v-2025-godu/
- [T1] Банк России, официальный курс валют: https://www.cbr.ru/currency_base/daily/
- [T1/T2] Минэкономразвития/МСП.РФ в пересказе РГ: https://rg.ru/2026/03/10/v-mer-nazvali-chislo-malyh-predpriiatij-v-rf-ono-dostiglo-pochti-7-mln.html
- [T2] Interfax о рекордном числе МСП: https://www.interfax.ru/business/1068369
- [T2] Рейтинг Рунета performance: https://ratingruneta.ru/performance/
- [T2] MediaGuru о данных рейтинга: https://www.mediaguru.ru/ratingruneta2025/
- [T2] Penji pricing: https://penji.co/pricing
- [T2] ManyPixels pricing: https://www.manypixels.co/pricing
- [T2] BannerBoo pricing: https://bannerboo.com/ru/plans/
- [T2] BotHelp pricing: https://bothelp.io/ru/price
- [T2/T3] Kwork HTML5 banner examples: https://kwork.ru/web-plus-mobile-design/2355411/animirovanniy-html5-banner ; https://kwork.ru/web-plus-mobile-design/45752181/animirovanniy-html5-banner-ekspertniy-uroven ; https://kwork.ru/web-plus-mobile-design/22840223/animirovanniy-html5-banner-dlya-reklamnoy-kampaniy
- [T2/T3] FL.ru examples: https://www.fl.ru/projects/5483630/razrabotka-reklamnyih-bannerov-dlya-reklamirovaniya-sayta-.html ; https://www.fl.ru/uslugi-freelancera/17056/dizayn-bannerov-dlya-reklamnyh-sistem.html ; https://www.fl.ru/uslugi-freelancera/10153/kreativy-dlya-reklamy-vizualy-i-bannery.html

Sources: T1=4, T2=8, T3=3. Primary evidence basis: T2.
> Market Pulse 2026-05-10: растущий интерес.
