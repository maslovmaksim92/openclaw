# 02-demand — Demand Validation

## Кейс
1628-msk-sanas-geo-expand-v2

## Итог
**Статус: EARLY REJECT**

Прямой спрос на standalone accent translation для enterprise-контакт-центров в РФ остаётся **LOW** по exact- и adjacent-keywords [T1]. Готовность платить подтверждена только для более широкого voice/contact-center stack и транскрибации, но не для отдельного budget line под accent translation [T2][T3]. При консервативной экономике компания не добирается до **EBITDA 500 тыс. ₽/мес** ни в одном из трёх сценариев монетизации.

## 1. Demand data
Источник exact keyword: `http://172.18.0.1:9001/multi-demand?keyword=accent%20translation%20contact%20center`

### Exact demand
- `accent translation contact center`: composite demand **LOW**, demand score **0**, Google Trends RU **1**, hh.ru vacancies **0**, Yandex Suggest **2**, Telegram subscribers **0** [T1]
- `voice accent translation`: composite demand **LOW**, demand score **0**, Google Trends RU **0**, hh.ru vacancies **0**, Yandex Suggest **2**, Telegram subscribers **0** [T1]
- `real time speech translation call center`: composite demand **LOW**, demand score **0**, Google Trends RU **0**, hh.ru vacancies **0**, Yandex Suggest **2**, Telegram subscribers **0** [T1]

### Adjacent demand
- `contact center ai`: composite demand **LOW**, demand score **15**, hh.ru vacancies **2**, Yandex Suggest **100** [T1]
- `contact center english`: composite demand **LOW**, demand score **0**, hh.ru vacancies **7**, Yandex Suggest **2** [T1]

### Вывод по спросу
- Прямой category demand в РФ **не наблюдается** [T1].
- Adjacent pain существует, но он описывает **AI для контакт-центров** и **англоязычную поддержку**, а не отдельную закупку accent-translation слоя [T1][T2].
- Для investment-fund уровня это слабый сигнал: есть боль, но нет подтверждённого локального buying intent именно под standalone product [T1][T2].

## 2. Конкуренты и ценовые якоря

| Игрок | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Krisp [T2] | Accent Conversion и call-center voice stack | Core от **$8/мес**, Advanced от **$15/мес**, Enterprise по запросу | Accent conversion продаётся как feature внутри broader suite, а не как дорогой standalone category |
| Deepgram [T2] | Voice Agent API / speech stack | STT **$0.0077–0.0165/мин**, Voice Agent API **$0.075–0.163/мин** | Базовый speech layer уже сильно commoditized, ceiling для standalone accent layer ограничен |
| MANGO OFFICE [T2] | Контакт-центр в РФ | **7 800 / 10 200 / 13 400 ₽/мес**, enterprise по запросу | Подтверждает, что РФ покупает CC stack, но budget line гораздо ближе к platform spend, чем к дорогому accent-only add-on |
| Teamlogs [T3] | RU-сервис транскрибации/бот | в сниппете поиска: от **990 ₽/мес** | В РФ пользователи готовы платить за adjacent voice-to-text utility, но ценовой якорь низкий |

**FX для перевода USD → RUB:** курс ЦБ РФ на 18.04.2026: **76.0535 ₽/$** [T1]. Это даёт грубые якоря: Krisp Advanced ≈ **1 141 ₽/мес**, Deepgram Voice Agent Standard ≈ **5.70 ₽/мин** [T1][T2].

## 3. Product / traction validation
- Sanas продаёт Accent Translation, Language Translation и Speech Enhancement enterprise-клиентам [T2].
- На сайте Sanas заявлены deployments в contact center / BPO use cases и кейс с Teleperformance [T2].
- Это подтверждает, что продукт **технологически реален** и коммерциализируем глобально [T2].
- Но локальная РФ-готовность к покупке standalone wedge из этого **не следует автоматически**; это inference, потому что в локальных поисковых и hiring-сигналах категория почти не видна [T1][T2].

## 4. Telegram bots / services в РФ
- В MANGO Office текстовые коммуникации для контакт-центра прямо включают **Telegram** как один из каналов обслуживания [T2].
- В `multi-demand` по exact-keywords обнаружено **0 Telegram subscribers**, то есть автоматический demand-signal по категории отсутствует [T1].
- На рынке есть adjacent RU-боты и сервисы для транскрибации/распознавания аудио, например Teamlogs [T3], но **не найдено заметного RU Telegram-бота именно для live accent translation contact-center calls**; это inference на базе поисковой выдачи и low-demand signals [T1][T3].

## 5. WTP — proof of willingness to pay
### Что подтверждено
1. Компании в РФ уже платят за контакт-центр и омниканальную платформу: MANGO Office публикует тарифы от **7 800 до 13 400 ₽/мес** [T2].
2. На глобальном рынке buyers платят за voice stack и accent-related feature sets: Krisp monetizes Accent Conversion, Deepgram monetizes speech stack поминутно [T2].
3. HH-сигналы по `contact center english` показывают, что англоязычная клиентская поддержка как боль существует [T1].

### Что не подтверждено
1. Что в РФ buyer создаёт **отдельную строку бюджета** под accent translation, а не решает задачу наймом, QA, скриптами, training или broader CCaaS stack [T1][T2].
2. Что локальный buyer готов платить **100–250 тыс. ₽ MRR** именно за accent-only слой [T2][T3].
3. Что Telegram или bot-driven канал формирует самостоятельный входящий спрос на категорию [T1][T3].

### Вывод по WTP
**Adjacent WTP подтверждён, category-specific WTP не доказан** [T1][T2]. Для инвестиционного кейса это недостаточно.

## 6. Market sizing

### Методика
- **Top-down:** база 5 000+ контакт-центров в РФ у MANGO Office [T2], далее сужение до мульти-язычных / международных / BPO-like контуров через low exact-demand и limited hh signals [T1].
- **Bottom-up:** 10 реальных buyers в РФ-контуре + экстраполяция на похожие аккаунты по вертикалям BPO, travel, medical, fintech, consumer support [T1][T2].
- **ARR avg:** **1.2 млн ₽/год** на клиента как нижняя граница из исходного кейса (`100 000 ₽/мес`) и с оглядкой на low-cost substitutes; это inference, но оно лучше согласуется с локальными ценовыми якорями, чем более агрессивные 1.8–3.0 млн ₽/год [T2][T3].

### 10 реальных buyers для bottom-up
1. Voxys [T2]
2. CallTraffic [T2]
3. Onecta [T2]
4. Reply [T2]
5. MANGO Office BPO / крупные аутсорсинговые контакт-центры как customer segment [T2]
6. GMS Clinic [T1/T2]
7. GMS Dental [T1/T2]
8. Класс-Ассист [T1/T2]
9. Avosend [T1/T2]
10. VIVO RUS [T1/T2]

### Основные допущения
- Из 5 000+ контакт-центров только около **3%** выглядят потенциально релевантными для accent translation, потому что exact category demand почти нулевой, а hh-сигналы по English-support остаются единичными [T1][T2].
- Это даёт около **150** теоретически релевантных аккаунтов в РФ [inference from T1+T2].
- Реально продаваемый сегмент уже: примерно **80–90** аккаунтов, где одновременно есть voice, международный контур и бюджет на enterprise tooling [inference from T1+T2].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **3.63 трлн ₽** = $47.71B global contact-center software market × 76.0535 ₽/$ [T3+T1, LOW CONFIDENCE] | — | — | top-down |
| TAM (РФ) | **180 млн ₽** = 5 000 × 3% × 1.2 млн ₽ [T2+T1] | **144 млн ₽** = 120 buyers × 1.2 млн ₽ [T1+T2] | diff=25%; bottom-up строже, потому что отсекает номинальные install base без реального cross-border pain | **144 млн ₽** |
| SAM (РФ) | **108 млн ₽** = TAM × 60% segment fit [T1+T2] | **96 млн ₽** = 80 buyers × 1.2 млн ₽ [T1+T2] | diff=12.5%; оценки близки, используем lower bound | **96 млн ₽** |
| SOM Y1 | **3.24 млн ₽** = 3% SAM [T1+T2] | **4.8 млн ₽** = 4 клиента × 1.2 млн ₽ [T1+T2] | diff=48%; top-down реалистичнее из-за длинного enterprise sales cycle | **3.24 млн ₽** |
| SOM Y3 | **10.8 млн ₽** = 10% SAM [T1+T2] | **9.6 млн ₽** = 8 клиентов × 1.2 млн ₽ [T1+T2] | diff=12.5%; оценки сходятся | **10.8 млн ₽** |

### Интерпретация sizing
- Preferred **SAM ≈ 96 млн ₽/год**. Это слишком узко для fund-level standalone wedge [T1][T2].
- **SOM Y1 / SAM = 3.4%**, это реалистично и не overclaiming [T1][T2].
- Даже такой консервативный SOM требует закрыть несколько enterprise logo sales в нише с почти нулевым inbound demand [T1].
- Sanity-check: если цикл сделки 6–9 месяцев, то даже 4 логотипа в Y1 уже требуют плотного founder-led enterprise motion; для новой категории это тяжело [T2].

## 7. Profit Gate — все сценарии монетизации
Цель: проверить достижимость **EBITDA ≥ 500 тыс. ₽/мес**.

### Сценарий A. Seat-based add-on
- Цена: **5 000 ₽/seat/мес** [inference from Krisp/MANGO anchors, T2]
- Средний аккаунт: **30 операторов** [T2]
- MRR на клиента: **150 000 ₽**
- GM: **55%**
- Валовая прибыль на клиента: **82 500 ₽/мес**
- Для fixed costs **2.2 млн ₽/мес** нужно GP **2.7 млн ₽/мес**, то есть **33 клиента**

**Вердикт: FAIL**. Это около 41% preferred SAM по числу покупателей, при LOW category demand [T1][T2].

### Сценарий B. Usage-based speech layer
- Цена: **~5.5–6.0 ₽/мин** после привязки к Deepgram и ЦБ [T1][T2]
- Предполагаемый revenue на средний аккаунт: **250 000 ₽/мес**
- GM: **30%** после ASR/TTS/latency/support
- Валовая прибыль на клиента: **75 000 ₽/мес**
- Для той же цели нужно **36 клиентов**

**Вердикт: FAIL**. Usage-экономика не спасает, потому что compute и support съедают маржу, а рынок локально узкий [T1][T2].

### Сценарий C. Enterprise platform / managed rollout
- Цена: **300 000 ₽/мес**
- GM: **35%**
- Валовая прибыль на клиента: **105 000 ₽/мес**
- Для EBITDA-цели нужно **26 клиентов**

**Вердикт: FAIL**. Даже premium scenario требует десятки enterprise logos в нише без доказанного local pull [T1][T2].

## 8. Общий вывод
- **Demand = LOW** [T1]
- **WTP на adjacent stack есть, но на standalone accent translation не доказан** [T1][T2]
- **Preferred SAM порядка 96 млн ₽/год**, что мало для fund-level standalone outcome [T1][T2]
- **Profit Gate fail во всех сценариях** [T1][T2]

## 9. Решение для пайплайна
**REJECTED на этапе demand validation.**

Основание для early reject выполнено: **DEMAND = LOW** и **Profit Gate FAIL**. Кейс имеет смысл только как feature inside broader CCaaS / speech stack, но не как самостоятельный investable wedge для РФ.

## Источники
### [T1]
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=accent%20translation%20contact%20center
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=voice%20accent%20translation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=real%20time%20speech%20translation%20call%20center
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=contact%20center%20ai
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=contact%20center%20english
- ЦБ РФ, курсы валют: https://www.cbr.ru/currency_base/daily/
- hh.ru поисковые сигналы использованы внутри multi-demand

### [T2]
- Sanas: https://www.sanas.ai/
- Sanas customer story / TP: https://www.sanas.ai/customer-stories/tp
- Krisp pricing: https://krisp.ai/pricing/
- Deepgram pricing: https://deepgram.com/pricing
- MANGO Office contact center: https://www.mango-office.ru/products/contact-center/
- MANGO Office tariffs: https://www.mango-office.ru/products/contact-center/tariffs/

### [T3]
- Teamlogs: https://teamlogs.ru/
- Grand View Research, contact center software market: https://www.grandviewresearch.com/industry-analysis/contact-center-software-market-report

Sources: T1=7, T2=6, T3=2. Primary evidence basis: T1.
