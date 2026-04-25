# Demand validation

## Итог
- Вердикт по спросу: **MEDIUM-LOW**, но не LOW-only blind spot. Прямой поисковый спрос по формулировке «сайт на подписке» слабый, зато есть подтверждённая готовность рынка платить за смежные managed/offline-to-online сервисы для SMB. [T2][T3]
- Рынок в РФ существует, но wedge не в «AI-сайт», а в **retainer на постоянные правки, контент, SEO и мелкую автоматизацию** для локальных SMB. [T2]
- Early reject **не срабатывает**: composite demand API вернул LOW, но Profit Gate в high-ARPU и white-label сценариях достижим. [T2][T3]

## Demand signal check
### API demand
- multi-demand по ключу `создание сайта на подписке для малого бизнеса` вернул `composite_demand=LOW`, `demand_score=0`, `habr_articles=2`, `yandex_suggest=2`, `hh_ru=0`, `google_trends_ru=0`. Источник: внутренний demand endpoint, 25.04.2026. [T2]
- Интерпретация: прямой category demand низкий, рынок ищет не «подписку», а более понятные JTBD: «сделать сайт», «поддержка сайта», «лендинг», «SEO/контент», «боты/оплаты/лиды». Это уже inference, а не прямое наблюдение. [T2]

### Наблюдаемый рыночный спрос
- В РФ уже есть офферы именно с логикой подписки: Siteling продаёт сайты по подписке от **2 000 / 5 000 / 8 000 ₽ в месяц**. Это прямое подтверждение того, что оффер тестируется на рынке. [T3]
- На hh.ru по запросу «контент-менеджер сайта» видны **135 вакансий** в Москве, а зарплаты в выдаче находятся примерно в диапазоне **80 000–150 000 ₽/мес**, что подтверждает наличие оплачиваемой проблемы вокруг постоянного ведения сайтов. [T1]
- Nethouse и Siteberry удерживают длинный хвост SMB в модели ежемесячной оплаты, что подтверждает устойчивую WTP за low-code/managed presence, даже если это не AI-first wedge. [T2][T3]

## Конкуренты и цены
| Игрок | Модель | Цена | Что это значит для кейса | Tier |
|---|---|---:|---|---|
| Siteling | сайт по подписке | 2 000 / 5 000 / 8 000 ₽ в мес | прямой локальный аналог, но низкий price umbrella | [T3] |
| Siteberry | поддержка сайтов/CMS | 3 000 / 9 000 ₽ в мес; продвижение от 20 000 ₽/мес | рынок платит не только за сборку, но и за ongoing support | [T3] |
| Nethouse | DIY-конструктор для SMB | от 600 ₽/мес | нижняя граница substitute pricing, сильный ценовой якорь вниз | [T2] |
| REG.RU | сайт/магазин под ключ | интернет-магазин под ключ 24 900 ₽ | разовый substitute, показывает WTP за быстрый запуск | [T2] |

## Telegram bots/services в РФ
- **BotHelp**: тарифы от **1 599 ₽/мес**, Telegram входит в поддерживаемые каналы; это substitute для SMB, которым не нужен полноценный сайт, а нужен лидоген/коммуникация в мессенджере. [T2]
- В РФ заметен класс Telegram-first automation tools, которые частично съедают бюджет сайта у микро-бизнеса, особенно в инфобизнесе, услугах и лидогенерации через мессенджеры. Это снижает шанс на массовый low-ticket website retainer. [T2][спекуляция]
- Вывод: Telegram не убивает рынок, но **сдвигает его вверх по ARPU**. Самый дешёвый сегмент может выбрать бот/лендинг/соцсеть вместо managed website. [T2]

## WTP, proof of willingness to pay
- Прямое proof: Siteling и Siteberry уже продают ежемесячные пакеты, значит платежная привычка за recurring website service существует. [T3]
- Substitute proof: SMB уже платят Nethouse от 600 ₽/мес просто за инфраструктуру сайта, а REG.RU берёт 24 900 ₽ за быстрый запуск магазина. [T2]
- Stronger proof: компании на hh.ru платят 80 000–150 000 ₽/мес внутренним контент/site-ролям; для SMB это создаёт окно для аутсорса в диапазоне 10 000–30 000 ₽/мес как cheaper-than-hire offering. [T1]
- Итог по WTP: **за 2 000–9 000 ₽/мес рынок уже подтверждён; за 15 000–30 000 ₽/мес нужен вертикальный пакет с контентом, SEO, правками и автоматизацией, иначе оффер проигрывает DIY и фрилансу.** [T1][T2][T3]

## Market sizing
### Методика
- Top-down: взят глобальный рынок website builders около **$2,16 млрд в 2023** с CAGR 9,5% как software/infrastructure proxy. Для managed-service слоя в РФ использован консервативный addressable cut и discount к software TAM, потому что кейс продаёт не CMS, а сервис вокруг presence management. [T2]
- Bottom-up: база на числе субъектов МСП в РФ около **6,84 млн**. Из неё выделен узкий serviceable слой customer-facing SMB с регулярной потребностью в обновлениях сайта и lead-gen. [T1]
- Для перевода USD использован ориентир **~90 ₽/$** на апрель 2026 как рабочее допущение; точность conversion не является главным драйвером вывода. [T1][инференс]

### Допущения
- Всего субъектов МСП в РФ: **~6,84 млн**. [T1]
- Доля customer-facing SMB, которым сайт реально нужен как рабочий канал, а не «визитка для галочки»: **~12%**. Это консервативный сегмент услуг, локального ритейла, медицины, образования, B2B-distribution, HoReCa. [T1][T2][инференс]
- Доля сегмента, готового платить именно за managed retainer, а не за DIY/фриланс ad hoc: **~15%** от этого ядра. [T2][T3][инференс]
- Средний контракт: **120 000 ₽ ARR** для SAM-level оффера (≈10 000 ₽/мес), **180 000 ₽ ARR** для более сильного vertical package. Для модели взят консервативный 120 000 ₽. [T2][T3]

### 10 реальных buyers для bottom-up sanity check
1. FIX PRICE [T1]
2. KuchenLand [T1]
3. Торговый Дом Стройтерминал [T1]
4. Информационное агентство России ТАСС [T1]
5. ГК DIGIS [T1]
6. Моно-Стиль [T1]
7. Loft It [T1]
8. ИГРО [T1]
9. Proglib [T1]
10. ГК Терморос [T1]

Это не все SMB и не весь ICP, а публичные buyer examples из вакансий/рынка, которые явно тратят деньги на постоянное ведение сайта/контента. [T1]

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | ~$2,16 млрд [T2] | — | — | top-down |
| TAM (РФ) | ~11,7 млрд ₽ [T2] | ~9,8 млрд ₽ [T1][T2] | diff ~19%, top-down выше из-за включения более широкого software+service envelope | **9,8 млрд ₽** |
| SAM (РФ) | ~3,5 млрд ₽ [T2] | ~2,95 млрд ₽ [T1][T2] | diff ~19%, использую lower bound из bottom-up | **2,95 млрд ₽** |
| SOM Y1 | ~35 млн ₽ [T2] | ~29,5 млн ₽ [T1][T2] | diff ~19% | **29,5 млн ₽** |
| SOM Y3 | ~175 млн ₽ [T2] | ~147,5 млн ₽ [T1][T2] | diff ~19% | **147,5 млн ₽** |

### Как считалось
- **Top-down TAM РФ**: global website builder TAM $2,16 млрд × 0,6% РФ share для узкого SMB website-management slice × 90 ₽/$ ≈ 11,7 млрд ₽. [T2][инференс]
- **Top-down SAM РФ**: TAM РФ × 30% сегмент fit для managed subscription ≈ 3,5 млрд ₽. [T2][инференс]
- **Bottom-up TAM РФ**: 6,84 млн МСП × 12% customer-facing digital-heavy SMB × 10% готовых покупать managed website layer × 120 000 ₽ ARR ≈ 9,8 млрд ₽. [T1][T2][инференс]
- **Bottom-up SAM РФ**: TAM bottom-up × 30% сегмент с частыми правками/контентом/SEO ≈ 2,95 млрд ₽. [T1][T2][инференс]
- **SOM Y1/Y3**: 1% и 5% от SAM, что остаётся ниже red-flag порога и выглядит реалистично для вертикализированного сервиса. [T2][инференс]

## Profit Gate (EBITDA >= 500K/мес)
### Сценарий 1, low-ticket template retainer
- ARPA: 5 000 ₽/мес
- Gross margin: ~60%
- Contribution: ~3 000 ₽/клиент/мес
- Fixed OPEX: ~450 000 ₽/мес
- Для EBITDA 500 000 ₽ нужно примерно **317 клиентов**.
- Вывод: **FAIL**. Для ранней команды это слишком тяжёлый объём аккаунтинга и саппорта. [инференс]

### Сценарий 2, mid-tier managed website
- ARPA: 15 000 ₽/мес
- Gross margin: ~60%
- Contribution: ~9 000 ₽/клиент/мес
- Fixed OPEX: ~550 000 ₽/мес
- Для EBITDA 500 000 ₽ нужно примерно **117 клиентов**.
- Вывод: borderline, возможно только при сильной шаблонизации и узком вертикальном ICP. [инференс]

### Сценарий 3, high-ARPU vertical retainer / white-label
- ARPA: 30 000 ₽/мес
- Gross margin: ~60%
- Contribution: ~18 000 ₽/клиент/мес
- Fixed OPEX: ~650 000 ₽/мес
- Для EBITDA 500 000 ₽ нужно примерно **64 клиента**.
- Вывод: **PASS**. Уже похоже на fundable service wedge, если продавать не «сайт», а «growth + updates + SEO + bot/payment automations». [инференс]

### Profit gate verdict
- Так как хотя бы один внятный monetization scenario проходит порог **500 000 ₽ EBITDA/мес**, кейс **не уходит в early reject**, несмотря на LOW по прямому category-search demand. [T1][T2][инференс]

## Риски
- Самый дешёвый сегмент уходит в DIY-конструкторы и Telegram-first сценарии. [T2]
- Формулировка «AI-веб-студия» слабо резонирует с рынком; нужно продавать outcome, а не production layer. [T2][инференс]
- Без вертикализации оффер быстро коммодитизируется и скатывается в low-margin agency work. [T2][T3]

## Что нужно для следующего этапа
- Тестировать не broad SMB, а 1-2 вертикали с частыми обновлениями сайта: клиники, интерьер/ремонт, B2B-distribution, школы/курсы, мебель/свет. [T1][T2][инференс]
- Проверить white-label канал через маркетинговые агентства и performance-студии, где сайт-support можно продавать как fulfillment layer. [T2][инференс]
- Поднять минимальный стартовый пакет в сторону **15–30 тыс. ₽/мес**, иначе unit economics разваливаются. [T1][T2][инференс]

## Источники
- ФНС, Единый реестр субъектов МСП: https://rmsp.nalog.ru/ [T1]
- HeadHunter, выдача вакансий «контент-менеджер сайта»: https://hh.ru/vacancies/kontent-menedzher-sajta/polnaya_zanyatost [T1]
- Nethouse: https://nethouse.ru/ [T2]
- REG.RU: https://www.reg.ru/solutions/catalog/group/site-making [T2]
- BotHelp pricing: https://bothelp.io/ru/pricing [T2]
- Siteling: https://www.siteling.ru/ [T3]
- Siteberry tariffs: https://www.siteberry.ru/ru/price/tarifs/ [T3]
- Grand View Research, website builders market report: https://www.grandviewresearch.com/industry-analysis/website-builders-market-report [T2]
- Internal multi-demand endpoint, keyword `создание сайта на подписке для малого бизнеса`, 25.04.2026. [T2]

Sources: T1=2, T2=5, T3=2. Primary evidence basis: T2.