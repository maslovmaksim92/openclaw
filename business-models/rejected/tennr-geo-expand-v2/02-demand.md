# Demand validation — Tennr geo expand (RU)

## Итог
**Решение: EARLY REJECT.** Сигнал спроса по РФ низкий по обязательному demand API, а прохождение Profit Gate требует enterprise-only сценария с длинным циклом внедрения и локальной интеграцией в МИС/ЕГИСЗ. Для расширения Tennr в РФ это делает юнит-экономику и скорость набора выручки непривлекательными.

## 1) Demand snapshot
- Обязательный API `multi-demand` по ключу `автоматизация записи пациентов в клинику` вернул **LOW**, score **3/10**, сигналы: Google Trends RU = 0, Habr = 2, HH = 13, Yandex Suggest = 2. [T1: internal demand endpoint]
- На hh.ru по запросу `медицинский регистратор клиника` найдено **189 вакансий**, типичные зарплаты в выдаче **40–60 тыс. ₽/мес**, что подтверждает наличие ручного фронт-офисного труда и экономического бенчмарка замещения. [T1: https://hh.ru/search/vacancy?text=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D0%B9+%D1%80%D0%B5%D0%B3%D0%B8%D1%81%D1%82%D1%80%D0%B0%D1%82%D0%BE%D1%80+%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA%D0%B0&area=113]
- Вывод: боль существует, но в РФ она чаще закрывается MIS/CRM/контакт-центром, а не отдельным intake/referral AI-слоем. Это **нишевый, а не широкий high-velocity demand**. [T1/T2, inference]

## 2) Конкуренты и цены
Ниже не только прямые AI-аналоги, но и реальные substitute-решения, за которые уже платят клиники в РФ.

| Игрок | Что закрывает | Цена | Вывод |
|---|---|---:|---|
| YCLIENTS | онлайн-запись, CRM, напоминания, запись через каналы | **от 9 525 ₽/мес** по official pricing snippet [T1: https://www.yclients.com/prices] | нижняя граница WTP у SMB/clinic admin layer |
| MEDODS | МИС/расписание/учет клиники | **от 6 900 ₽/мес** [T1: https://medods.ru/] | сильный ценовой якорь для небольших клиник |
| Medesk | облачная МИС, patient portal, online booking, integrations | **от 4 000 ₽/мес** по official snippet [T1: https://www.medesk.ru/prices/] | рынок уже приучен покупать bundled workflow, а не отдельный AI intake |
| ZoeAgent | AI-агент для записи и коммуникации | **Basic $125, Pro $250, Advanced $299 / мес** [T1: https://zoeagent.com/ru/pricing] | closest AI-style comparable, но ценник ближе к SMB automation |

### Вывод по конкурентам
- В РФ и adjacent-рынке уже есть рабочие substitute-платформы с ценой **4–10 тыс. ₽/мес** на нижнем уровне и около **10–25 тыс. ₽/мес** для AI-style automation. [T1]
- Чтобы Tennr продавался отдельно, ему нужно доказывать не просто удобство записи, а measurable uplift по referral conversion, SLA intake и загрузке врачей. Без этого buyer будет сравнивать продукт с MIS/CRM, а не с enterprise care-orchestration. [T1/T2, inference]

## 3) Telegram в РФ
- В РФ есть горизонтальные bot/platform слои для продаж и поддержки, например SaleBot и BotHelp, но они не выглядят как доминирующий **медицинский intake stack** для крупных сетей. [T2: https://salebot.pro/, https://bothelp.io/]
- Значимых Telegram-first решений именно под referral orchestration/private clinic intake в масштабе enterprise я не нашёл; скорее Telegram используется как дополнительный канал напоминаний и lead capture. [T2, inference]
- Для healthcare enterprise в РФ основной стек по-прежнему смещён в МИС, телефонию, сайт-виджеты и контакт-центр, а Telegram служит вторичным каналом. [T1/T2]

## 4) WTP, willingness to pay
- Факт WTP уже подтверждается тем, что клиники платят за YCLIENTS, MEDODS, Medesk и похожие workflow-системы. [T1]
- Зарплата регистратора **40–60 тыс. ₽/мес** на hh.ru означает, что продукт, экономящий хотя бы 0.5–1 FTE или повышающий конверсию записи, теоретически может окупаться при цене **20–60 тыс. ₽/мес**. [T1, inference]
- Но публичные рыночные прайсы показывают, что базовый рынок привык к **низкому ARPU**, а high-ticket enterprise слой покупается только при доказуемой интеграционной и операционной ценности. [T1/T2]
- Следовательно, **WTP есть, но она сегментирована**: SMB платит мало, а enterprise готов платить больше только после тяжёлого пилота и интеграции. [T1/T2]

## 5) Market sizing
### Подход и допущения
- Для top-down беру коммерческий рынок частной медицины РФ как верхнюю экономическую базу и выделяю адресуемую долю front-office/intake automation. [T2]
- Для bottom-up считаю только клиники и сети, где есть online-booking, регистратура, call-center или распределение patient flow, то есть реальная боль для intake/orchestration. [T1/T2]
- Все суммы в рублях, курс для global conversion принят **95 ₽/$** как рабочее допущение на 2026-04-24. [T2, inference]

### Top-down
- Global patient engagement / intake-adjacent software market беру как **$24.4 млрд**. [T2: Grand View Research, https://www.grandviewresearch.com/industry-analysis/patient-engagement-solutions-market]
- Addressable share для intake/referral/workflow automation внутри этого пирога принимаю **6%**, отсюда **TAM (мир) ≈ $1.46 млрд = 138.7 млрд ₽**. [T2, inference]
- Для РФ в качестве economic base беру частную медицину/платные услуги как рынок порядка **1.5 трлн ₽**; долю spend на intake/admin automation принимаю **0.35%**, что даёт **TAM (РФ) ≈ 5.25 млрд ₽**. [T2 + inference]
- Для сегмента Tennr fit (сети, multi-site clinics, сложный intake) беру **35%** TAM, итого **SAM (РФ) ≈ 1.84 млрд ₽**. [T2, inference]
- Реалистичный capture: **2% Y1** и **8% Y3** от SAM, значит **SOM Y1 ≈ 36.8 млн ₽**, **SOM Y3 ≈ 147.0 млн ₽**. [inference]

### Bottom-up
Формула: total buyers × % with need × ARR avg.
- Total buyers = **6 000** частных клиник/медцентров и сетевых площадок, где есть заметный поток записи и front-desk operations. Это консервативная подвыборка от общего частного рынка, а не все медорганизации. [T2, inference]
- % with need = **30%**, потому что не всем нужен отдельный orchestration слой, но у части клиник боль подтверждается ручными регистраторами, online-booking и call-center нагрузкой. [T1/T2]
- ARR avg = **720 000 ₽/год** (60 тыс. ₽/мес) как mid-case между low-end SaaS и enterprise-lite AI automation. [T1 + inference]
- **SAM_bottom_up = 6 000 × 30% × 720 000 ₽ = 1.296 млрд ₽**.
- При capture **2% Y1** и **8% Y3** получаем **SOM Y1 = 25.9 млн ₽**, **SOM Y3 = 103.7 млн ₽**.

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 138.7 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 5.25 млрд ₽ [T2+inf] | 4.32 млрд ₽ [T2+T1+inf, SAM/0.30] | diff 1.2x, допустимо | lower |
| SAM (РФ) | 1.84 млрд ₽ [T2+inf] | 1.296 млрд ₽ [T1/T2+inf] | diff 1.42x, в допустимом диапазоне | **1.296 млрд ₽** |
| SOM Y1 | 36.8 млн ₽ | 25.9 млн ₽ | diff 1.42x | **25.9 млн ₽** |
| SOM Y3 | 147.0 млн ₽ | 103.7 млн ₽ | diff 1.42x | **103.7 млн ₽** |

### GTM-10 targets для bottom-up
1. МЕДСИ [T1: https://medsi.ru/]
2. ГК «Мать и дитя» / MD Medical [T1: https://mamadeti.ru/]
3. СМ-Клиника [T1: https://www.smclinic.ru/]
4. Будь Здоров [T1: https://klinikabudzdorov.ru/]
5. Поликлиника.ру [T1: https://polyclinika.ru/]
6. Скандинавия / АВА-ПЕТЕР [T1: https://www.avaclinic.ru/]
7. Медскан [T1: https://medscangroup.ru/]
8. Ниармедик [T1: https://www.nrmed.ru/]
9. Инвитро [T1: https://www.invitro.ru/]
10. KDL [T1: https://kdl.ru/]

Sanity check: при среднем enterprise deal cycle 9–12 месяцев закрыть SOM Y1 через 3–5 крупных сетей уже трудно; это ухудшает реальную достижимость даже консервативного Y1. [T1/T2, inference]

## 6) Profit Gate: все сценарии монетизации
Цель: понять, достижима ли **EBITDA ≥ 500 тыс. ₽/мес** для локальной компании.

### Сценарий A. SMB SaaS
- Цена: **20 тыс. ₽/мес**.
- Валовая маржа: **80%**.
- Постоянные расходы: минимум **1.2 млн ₽/мес** (продакт + внедрение + продажи + support + локализация). [inference]
- Нужно клиентов для EBITDA 500 тыс. ₽/мес: `(1.2 млн + 0.5 млн) / (20k × 0.8) ≈ 107`.
- **Вердикт:** нереалистично. Рынок сравнивает с Medods/Medesk/Yclients. [T1]

### Сценарий B. Mid-market vertical SaaS
- Цена: **60 тыс. ₽/мес**.
- Валовая маржа: **80%**.
- Нужно `(1.7 млн) / (60k × 0.8) ≈ 36` клиентов.
- **Вердикт:** тоже слабо реалистично, потому что это уже десятки клиник при low demand и длинном sale cycle. [T1/T2]

### Сценарий C. Enterprise SaaS + onboarding
- Цена: **180 тыс. ₽/мес** + **300 тыс. ₽** setup, амортизировано на 12 мес = +25 тыс. ₽/мес.
- Contribution на клиента: `180k × 0.75 + 25k ≈ 160k ₽/мес`.
- Нужно `(1.7 млн) / 160k ≈ 11` крупных клиентов.
- **Вердикт:** теоретически единственный рабочий путь, но для РФ он требует интеграций с МИС, compliance, локализации процессов и 9–12+ месяцев цикла. Для geo-expand без локального distribution edge сценарий выглядит слабым. [T1/T2]

### Сценарий D. Service-heavy implementation
- Цена выше, но валовая маржа **40–50%**.
- Для EBITDA 500 тыс. ₽/мес нужен постоянный поток дорогих внедрений, что делает бизнес консалтингом, а не scalable SaaS. [inference]
- **Вердикт:** fail.

### Profit Gate verdict
**FAIL.** Формально только enterprise-only сценарий даёт шанс, но он не выглядит достаточно достижимым на российском рынке для этого кейса. Значит условие `company EBITDA >= 500K/mo achievable` не проходит. [T1/T2, inference]

## 7) Почему reject сейчас
- DEMAND по обязательному API = **LOW**. [T1]
- Profit Gate = **FAIL** во всех реалистичных сценариях, кроме натянутого enterprise-only пути с длинным циклом и высокой интеграционной стоимостью. [T1/T2]
- Российский рынок уже закрывает большую часть боли bundled MIS/CRM/booking systems с низким price anchor. [T1]
- Для Tennr нужен слишком узкий buyer profile и слишком сложная локализация под РФ ради сравнительно небольшого SOM. [T1/T2]

## Sources
- T1: internal demand endpoint `http://172.18.0.1:9001/multi-demand?keyword=...`
- T1: hh.ru search results
- T1: https://www.yclients.com/prices
- T1: https://medods.ru/
- T1: https://www.medesk.ru/prices/
- T1: https://zoeagent.com/ru/pricing
- T1: official buyer sites (medsi.ru, mamadeti.ru, smclinic.ru, klinikabudzdorov.ru, polyclinika.ru, avaclinic.ru, medscangroup.ru, nrmed.ru, invitro.ru, kdl.ru)
- T2: https://www.grandviewresearch.com/industry-analysis/patient-engagement-solutions-market
- T2: https://salebot.pro/
- T2: https://bothelp.io/

Sources: T1=7, T2=3, T3=0. Primary evidence basis: T1.