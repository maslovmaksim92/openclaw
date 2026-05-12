# Demand validation — AI-перевод документов и локализация под заказ

## Итог
**Вердикт по спросу: LOW.** По обязательному demand endpoint запрос `AI перевод документов локализация` вернул `composite_demand=LOW`, `demand_score=0`, `google_trends_ru=0`, `hh_ru=0`, `habr_articles=2`, `yandex_suggest=2` [T2/T3]. На этом фоне кейс не показывает достаточной органики для fund-level входа.

## 1) Что реально покупают
- Рынок **не нулевой**, но он уже заполнен двумя типами игроков: платформы локализации и классические бюро/managed service [T1/T2].
- Платежеспособный use case есть у экспортеров, e-commerce и software-команд, которым нужны карточки товаров, техдокументация, legal docs и сайты на нескольких языках [T1/T2].
- Но публичные сигналы в РФ показывают скорее **фрагментированный нишевой спрос**, а не волну нового category demand [T1/T2].

## 2) Конкуренты с ценами
| Игрок | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Smartcat | AI localization platform + workflow | **от $1,200/год** за Basic [T1] | Низкий порог входа для SMB, давит на SaaS ARPU |
| Smartling | AI / MT / human translation | **MT от $0.0075/слово**, **AI translation от $0.06/слово**, **AI human translation от $0.12/слово**, **human translation от $0.20/слово** [T1] | Верхний enterprise benchmark, цена привязана к объёму и качеству |
| RushTranslate | Перевод документов | **от $24.95 за страницу** [T2] | Даёт понятный reference для per-page jobs |
| OnlyRead (RU, Telegram/MAX) | Документный AI-сервис рядом с translation workflow | **100 ₽/мес**, **950 ₽/мес**, **3 490 ₽/мес**, от **1.75 ₽/страница** [T2] | Показывает, что document-AI в РФ уже commoditized по цене |
| Voicee (RU, Telegram) | Adjacent AI service в Telegram | **от 300 ₽/час** или **от 990 ₽/мес** [T2] | Telegram как канал монетизации в RU работает, но по очень низкому чеку |

**Вывод:** конкурентное поле уже приучило рынок либо к дешёвому self-serve, либо к кастомному enterprise pricing. Для нового managed AI-localisation wedge место есть только при сильной вертикализации.

## 3) Telegram-боты и сервисы в РФ
Проверка RU Telegram/adjacent automation показала:
- **OnlyRead**: работа с PDF/JPG/PNG через Telegram и MAX, 35 362 пользователей, 188 284 страниц распознано, 151 253 файлов обработано [T2]. Это не прямой локализатор, но показывает привычку рынка покупать document AI через бот.
- **Voicee**: Telegram-бот для аудио/видео-to-text, тарифы от 300 ₽/час и от 990 ₽/мес [T2]. Это подтверждает, что Telegram годится как канал micro-SaaS/AI service delivery.
- Явного сильного mass-market RU Telegram-лидера именно в **локализации документов под заказ** не обнаружено; рынок выглядит скорее разрозненным и уходит либо в обычные бюро, либо в web SaaS [спекуляция, T2/T3].

## 4) WTP, proof of willingness to pay
- Smartcat монетизирует SMB вход **от $1,200/год** [T1]. Значит, бизнес уже платит минимум low-four-figure annual fee за localization workflow.
- Smartling публикует value-based pricing вплоть до **$0.20/слово** за human translation [T1]. Это прямое доказательство готовности enterprise-покупателя платить за качество, SLA и workflow.
- OnlyRead и Voicee показывают, что в РФ через Telegram проходят транзакции в диапазоне **100–3 490 ₽/мес** и **300 ₽/час** [T2], но это уровень utility tooling, а не premium managed localization.

**Вывод по WTP:** willingness to pay существует [T1/T2], но в РФ внизу рынка он смещён к дешёвому self-serve. Чтобы поднять чек, нужен enterprise-ready пакет: human review, SLA, локальный контур, 152-ФЗ, отраслевые глоссарии и интеграции [T1/T2].

## 5) Сигналы спроса в РФ
- Demand endpoint: `LOW` и score `0` [T2].
- hh.ru: по запросу **«локализация» найдено 1 624 вакансии**, **«переводчик английского» 640**, **«технический переводчик» 318**, **«менеджер локализации» 266**, **«локализация сайта» 37** [T1]. Это подтверждает наличие функции и бюджетов, но также показывает, что спрос размазан между HR, контентом, бюро и in-house ролями.
- На платформе **«Мой экспорт» уже 41.5 тыс. юрлиц и ИП**, из них **81% МСП** [T1]. Это реальная база компаний, которым потенциально нужны перевод и локализация для внешних рынков.
- По материалам Росстата, около **47.5% обследованных организаций имели веб-сайт в 2024 году** [T1]. Значит, только часть базы вообще готова к системной локализации сайта и цифровых материалов.

## 6) Market sizing
### Методика
Считал два пути.
1. **Top-down:** глобальный language industry market от Slator и затем дисконт до РФ по фактической доле адресуемых цифровых экспортно-ориентированных use cases [T2 + inference].
2. **Bottom-up:** база «Мой экспорт» × доля компаний с веб-сайтом × доля с регулярной multilingual-потребностью × средний ARR [T1/T2 + inference].

### Ключевые допущения
- Global language industry market: **$31.7B в 2025** [T2, Slator].
- Для перевода в рубли использован рабочий курс **90 ₽/$** [inference].
- Средний ARR для managed AI localization desk по SME/mid-market: **420 000 ₽/год** = 35 000 ₽/мес [inference from competitor pricing and SMB affordability, T1/T2].
- Доля экспортёров с регулярной multilingual-задачей: **18%**. Это консервативно ниже, чем доля компаний с веб-сайтами, и согласуется с умеренным количеством hh-вакансий по локализации [T1 + inference].

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------:|----------:|----------------|-----------|
| TAM (мир) | **$31.7B** [T2] | — | — | top-down |
| TAM (РФ) | **20.0 млрд ₽** [T2+T1, inference] | **8.3 млрд ₽** [T1+inference] | diff 2.4x, top-down включает более широкий enterprise spend, bottom-up только web-active export base | **8.3 млрд ₽** |
| SAM (РФ) | **1.8 млрд ₽** [T2+inference] | **1.49 млрд ₽** [T1+inference] | diff 1.2x, оценки близки | **1.49 млрд ₽** |
| SOM Y1 | **7.2 млн ₽** | **5.0 млн ₽** | diff 1.4x | **5.0 млн ₽** |
| SOM Y3 | **21.6 млн ₽** | **16.8 млн ₽** | diff 1.3x | **16.8 млн ₽** |

### Bottom-up расчёт
- Total buyers base: **41 500** компаний на платформе «Мой экспорт» [T1].
- Web-ready base: **41 500 × 47.5% = 19 713** [T1].
- Buyers with recurring need: **19 713 × 18% = 3 548** [T1+inference].
- ARR avg: **420 000 ₽/год** [T1/T2+inference].
- **SAM_bottom_up = 3 548 × 420 000 ₽ = 1.49 млрд ₽.**
- **SOM Y1 = 12 клиентов × 420 000 ₽ = 5.04 млн ₽.**
- **SOM Y3 = 40 клиентов × 420 000 ₽ = 16.8 млн ₽.**

### 10 реальных buyers / GTM targets
1. Kaspersky
2. 1C
3. Splat Global
4. Askona
5. Geoscan
6. BIOCAD
7. Ozon Global
8. Wildberries
9. FESCO
10. Р-Фарм

Это не оценка закрываемости, а список реальных компаний с международным контентом, техдокументацией, карточками товаров или multilingual sales motion [T2].

## 7) Profit Gate: EBITDA >= 500K/mo
Проверил все базовые сценарии монетизации.

### Сценарий A. B2C/B2B2C перевод документов поштучно
- Средний чек: **1 500 ₽** [inference from per-page market references, T1/T2]
- Объём: **400 заказов/мес** => **600 000 ₽ выручки/мес**
- Валовая маржа после human review / PM / correction: ~**35%**
- EBITDA после фиксированных расходов: **150–180 тыс. ₽/мес**
- **Gate FAIL**

### Сценарий B. SME export retainer
- Средний retainer: **35 000 ₽/мес**
- 20 клиентов => **700 000 ₽/мес выручки**
- Валовая маржа: ~**45%**
- EBITDA после sales + PM + reviewer: **220–320 тыс. ₽/мес**
- **Gate FAIL**

### Сценарий C. Mid-market localization desk
- Средний retainer: **150 000 ₽/мес**
- 10 клиентов => **1.5 млн ₽/мес выручки**
- Валовая маржа: ~**55%**
- EBITDA после 1 senior PM, reviewer pool, sales overhead, security/compliance overhead: **350–480 тыс. ₽/мес**
- Чтобы пройти gate, нужно скорее **12–14 клиентов** такого класса, что при LOW demand и длинном sales cycle выглядит нереалистично в обозримом горизонте [T1/T2+inference].
- **Gate FAIL**

**Итог по Profit Gate:** во всех трёх типовых моделях компания **не показывает надёжного пути к EBITDA 500K+/мес** без enterprise sales machine или сильной отраслевой специализации.

## 8) Основные риски
- Слабый верхневоронковый спрос по keyword-demand [T2].
- Коммодитизация document AI и translation tooling по цене [T1/T2].
- Большая часть выручки уходит в services delivery, QA и reviewer layer, что ограничивает EBITDA [T1/T2].
- Сегмент может жить как boutique agency, но слабо похож на venture-scale wedge [вывод].

## 9) Решение
**REJECTED.**

Причина: сработало правило early reject.
1. **DEMAND = LOW** по обязательному endpoint.
2. **Profit Gate FAIL**: ни один реалистичный monetization scenario не даёт устойчивого EBITDA >= 500K/мес без натяжки.

## Sources
- Smartcat pricing: https://www.smartcat.com/pricing/ [T1]
- Smartling plans/pricing: https://www.smartling.com/plans/ [T1]
- RushTranslate pricing: https://rushtranslate.com/pricing [T2]
- OnlyRead: https://www.onlyread.ru/ [T2]
- Voicee Telegram: https://voicee.ru/telegram [T2]
- hh.ru vacancies pages and searches [T1]
- РЭЦ / «Мой экспорт»: https://www.exportcenter.ru/press_center/bolee-3500-kompaniy-zaregistrirovalis-na-platforme-moy-eksport-za-pervoe-polugodie-2025-goda/ [T1]
- Rosstat regional 2024 ICT statistics with org web-site penetration: https://62.rosstat.gov.ru/storage/mediabank/%D0%A2%D0%BE%D0%BC%202-2024.pdf [T1]
- Slator 2025 Language Industry Market Report: https://slator.com/slator-2025-language-industry-market-report/ [T2]

Sources: T1=5, T2=4, T3=0. Primary evidence basis: T1.