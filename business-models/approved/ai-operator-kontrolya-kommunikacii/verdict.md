# AI-оператор контроля коммуникаций — Full Verdict Package
> Скомпилированный пакет стадий пайплайна для публикации в GitHub.
> Примечание: в этом кейсе отсутствуют отдельные `02-validation.md` и `03-demand.md`; фактические стадии покрыты файлами `01-evidence.md` и `02-demand.md`.

---

## Файл: 01-intake.md

---
sector: B2B-OPS
rerun: false
source_raw: 2026-04-23-b2b-ops-imot-liya-ai-operator-kontrolya-kommunikacii.md
created: 2026-04-23T10:03:13+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
AI-first оператор контроля клиентских коммуникаций, который автоматически разбирает 100% звонков и чатов, выявляет ошибки операторов, причины обращений и триггеры потерь продаж без ручного QA-отдела.

## Почему кейс проходит triage
- Это отдельный B2B-OPS wedge с понятным buyer'ом, регулярным workflow и измеримым ROI через рост конверсии, снижение потерь лидов и сокращение ручного QA.
- В РФ уже есть сильный локальный сигнал: IMOT.IO включён в реестр отечественного ПО, публикует тарифы 49 000-75 000 ₽ в месяц и заявляет внедрения у крупных корпоративных клиентов.
- EBITDA-гипотеза 700 000-1 600 000 ₽ в месяц проходит порог Program 1, а ниша отличается от кейсов про AI-оператора поддержки тем, что продаёт слой контроля качества и аналитики коммуникаций.

## Контекст raw-файла

# IMOT.IO / «Лия»

## Sector
B2B-OPS

## Wedge statement
AI-first оператор контроля клиентских коммуникаций, который автоматически разбирает 100% звонков и чатов, выявляет ошибки операторов, причины обращений и триггеры потерь продаж без ручного QA-отдела.

## Evidence
- [T1] https://reestr.digital.gov.ru/reestr//?EX_PAGE_N=25&EX_PAGE_S=20&PAGE_N=146&PAGE_S=40 — 30.07.2024 сервис речевой аналитики «ИМОТИО» включён в реестр отечественного ПО, что подтверждает локальную поставку и пригодность для РФ.
- [T2] https://vc.ru/ai/2809308-avtomatizatsiya-kontrolya-kachestva-zvonkov-s-ii-dlya-franshizy-etazhi — 23.03.2026 кейс показывает спрос на автоматический анализ 100% входящих и исходящих звонков вместо выборочного ручного контроля в активных продажах.
- [T2] https://vc.ru/ai/2856770-avtomatizatsiya-b2b-prodazh-s-pomoshchyu-ii — 2026 в обзоре российских AI-инструментов указан imot.io с ценой от 54 000 ₽/мес за анализ звонков, чатов и видеоконференций, то есть модель уже попадает в целевой чек B2B-OPS.
- [T3] https://imot.io/main — доступ 23.04.2026: на сайте опубликованы тарифы 49 000-75 000 ₽/мес и пакет 245 990 ₽, плюс обещан 100% охват коммуникаций и готовые интеграции.
- [T2] https://vc.ru/ai/2063383-intervyu-s-rezidentom-skolkovo-ispolzovanie-h200 — 2025: компания называет среди клиентов РЖД, «Газпром Нефть», Skillfactory, банки, девелоперов и медцентры, что подтверждает enterprise/Mid-market пригодность.

## EBITDA hypothesis (24 мес, base)
700000-1600000₽/мес

## RU-fit
5 / 5. Данные и хранение можно локализовать в РФ, решение уже в реестре отечественного ПО, use case понятен российским продажам, колл-центрам и службам поддержки.

## Expected unit economics (ballpark)
- ARPU: 80000-180000₽/мес
- CAC (ballpark): 40000-140000₽
- Avg deal cycle: 1-3 мес
- Target segment: Mid-market | Enterprise

## Why now
Российские компании режут ФОТ и хотят автоматизировать QA, но ручной контроль всё ещё покрывает только малую часть коммуникаций. Одновременно локальные LLM, speech-to-text и требования к хранению данных в РФ делают AI-first оператора клиентского сервиса и sales ops практически готовым к массовому внедрению.


---

## Файл: 01-evidence.md

# Подтверждающие сигналы

## 2026-04-24 — supporting signal — Lace AI как подтверждение спроса на AI-оператора входящих звонков
- **Дата:** 2026-04-24
- **Источник:** https://techcrunch.com/2025/08/14/lace-ai-raises-19m-series-a/ ; https://www.lace.ai/ ; https://www.lace.ai/blog/series-a
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что показывает международный спрос на отдельный слой AI revenue intelligence для 100% входящих звонков, где продукт продаёт возврат упущенной выручки, coaching и QA automation. Это подтверждает, что кейс про AI-оператора контроля коммуникаций является не локальной аномалией, а частью растущей категории с понятным ROI.
- **Ключевые данные и факты:** TechCrunch пишет о росте ARR Lace AI на 1 000% за 2024 год и привлечении $19 млн Series A; сайт компании описывает автоматическое выявление missed revenue, coaching и QA automation для звонков; компания фокусируется на call centers в home services, где ценность завязана на конверсии входящих обращений.


---

## Файл: 02-demand.md

---
stage: demand-validation
case: ai-operator-kontrolya-kommunikacii
date: 2026-04-24
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

> Market Pulse 2026-04-24: точный поисковый спрос в РФ низкий, но платящий бюджетный контур и живой конкурентный рынок уже существуют.

## Кейс
AI-first оператор контроля клиентских коммуникаций для продаж, поддержки и контакт-центров, который автоматически анализирует 100% звонков и чатов, выявляет ошибки операторов, причины потерь продаж, нарушения скриптов и точки обучения без ручного QA-отдела.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Exact-demand в РФ по запросу `речевая аналитика контроль качества звонков` низкий: internal multi-demand вернул **LOW**, `demand_score=3`, `hh_vacancies=10`, `habr_articles=2`, `yandex_suggest=2`. Это значит, что категория пока не формулируется массово как самостоятельный новый ярлык. [T2]
- При этом платящий рынок уже есть: IMOT.IO публично продаёт тарифы **49 000-75 000 ₽/мес** и пакет **245 990 ₽**, MANGO OFFICE продаёт AI-речевую аналитику с абонплатой **1 100 ₽/мес** плюс тарификацией по минутам, Roistat продаёт речевую аналитику и AI-тегирование от **110-120 ₽** за пакетную единицу/минуту, а сам базовый контур платформы стоит от **5 900 ₽/мес**. Это прямое доказательство WTP на рынке РФ. [T1][T2]
- Российский рынок диалогового ИИ уже материален: Naumen оценил его в **8 млрд ₽** в 2024 году, а сегмент речевой аналитики, как самый быстрорастущий, в **1,5 млрд ₽**. Это хороший top-down anchor для локального TAM/SAM. [T2]
- Profit Gate не проходит в дешёвом low-touch add-on сценарии, но проходит в mid-market и enterprise сценариях при чеках от **80-180 тыс. ₽/мес** и базе **10-15** клиентов. Поэтому ранний reject не нужен. [T1][T2][inference]

## 1. Demand data

### Demand API
- `речевая аналитика контроль качества звонков` → **LOW**, `demand_score=3`, `hh_ru=10`, `habr_articles=2`, `yandex_suggest=2`. [T2]

### Интерпретация
- Exact-demand слабый, поэтому продавать продукт как completely new category в РФ будет тяжело. [T2][inference]
- Но underlying pain существует: на hh.ru есть реальные вакансии на контроль качества звонков и на речевую аналитику, включая VOXYS, OTP Bank и другие команды, которые уже содержат QA-функцию и тратят деньги на процесс. [T1][T2]
- Следовательно, входить нужно не через абстрактный `AI operator`, а через ROI-язык: рост конверсии, сокращение ручного QA, ускорение обучения операторов, снижение missed revenue и соблюдение скриптов. [T1][T2][inference]

## 2. Реальные конкуренты и цены

### Публичные конкуренты / substitutes
1. **IMOT.IO**: публичные тарифы **49 000 ₽/мес**, **75 000 ₽/мес**, а также пакет **245 990 ₽**; на отраслевых страницах встречаются тарифы **53 990 ₽/мес**, **123 990 ₽/мес**, **195 990 ₽/мес**, **399 990 ₽/мес**, **603 990 ₽/мес**. Это самый прямой локальный comparable. [T1]
2. **MANGO OFFICE Speech Analytics AI**: абонплата **1 100 ₽/мес**, в тарифах MANGO также фигурирует стоимость распознавания с ИИ-анализом **1,25-1,9 ₽/мин** и без ряда AI-опций до **2,25-2,9 ₽/мин** в зависимости от пакета. [T2]
3. **Roistat**: базовый тариф платформы начинается от **5 900 ₽/мес**, а в ценовой сетке есть отдельный блок `Речевая аналитика` и `Речевая аналитика + AI`; snippet показывает цену от **110 ₽** и **120 ₽** за пакетную единицу/минуту, а также пакетную сетку от **9 000 ₽**. [T2]
4. **Callibri**: публично заявляет `от 1 000 рублей за 30 дней` для набора инструментов лид-менеджмента, куда входят запись разговоров и речевая аналитика. Это не чистый speech-only price, но это реальный ценовой референс на adjacent SMB/Mid-market слой. [T2]

### Вывод по конкуренции
- Рынок уже не пустой, и в РФ есть минимум 3-4 реальных игрока с публичной монетизацией. [T1][T2]
- По структуре цены видно два паттерна: либо пакетная подписка **49-75 тыс. ₽/мес** и выше, либо low-entry price + тарификация по минутам. [T1][T2]
- Значит, willingness to pay уже существует и покупатель понимает бюджетную строку. Риск не в отсутствии рынка, а в том, что часть value capture уже забирают incumbents. [T1][T2][inference]

## 3. Telegram bots / services в РФ

Проверка Telegram-контура показала, что Telegram в этой категории уже commoditized как канал уведомлений и доставки событий:
- **IMOT.IO** прямо пишет про срочные оповещения в Telegram и настройку рассылки по зонам ответственности. [T1]
- **Roistat** поддерживает Telegram-интеграцию, Telegram-уведомления и отдельного бота `@RoistatLeadHunterBot`, а также бота уведомлений для событий. [T2]
- **MANGO OFFICE** публикует инструкции по Telegram-боту для подписки на уведомления коллтрекинга. [T2]

**Вывод:** Telegram в RU есть, но это feature/channel, а не moat. Отдельная ценность кейса должна быть в качестве анализа, шаблонах контроля, интеграциях и доказуемом ROI. [T1][T2][inference]

## 4. WTP, proof of willingness to pay

### Прямые сигналы WTP
- IMOT.IO уже продаёт месячные тарифы в диапазоне от **49 000 ₽** до **75 000 ₽** и выше на отраслевых страницах. Это сильнейшее локальное доказательство, что buyer готов платить recurring fee именно за speech/communication QA layer. [T1]
- MANGO OFFICE monetizes поминутно и через абонплату, что подтверждает готовность рынка платить и за usage-based модель. [T2]
- Roistat monetizes adjacent revenue stack, включая речевую аналитику и AI-тегирование, что показывает готовность платить даже в bundled GTM. [T2]
- hh.ru вакансии на прослушку звонков, контроль качества и речевую аналитику означают, что компании уже несут прямые трудовые затраты на ручной QA. Это сильный proxy willingness to pay на автоматизацию этой функции. [T1][T2]

### Что это значит
- WTP на уровне **50-150 тыс. ₽/мес** для mid-market выглядит подтверждённым. [T1][T2][inference]
- WTP на уровне **180-300 тыс. ₽/мес** для enterprise тоже выглядит правдоподобно, если продукт даёт 100% охват, coaching, CRM-fill и снижение missed revenue. Это уже inference из локальных цен и buyer pain, а не прямой price sheet. [T1][T2][inference]

## 5. Market sizing

### Логика сегмента
Фокусирую адресуемый рынок на РФ-сегментах, где коммуникации критичны для выручки и качества сервиса: недвижимость, банки, медцентры, контакт-центры/BPO, авто, страхование, ритейл, edtech. [T1][T2][inference]

### Допущения
- Курс Банка России на **24.04.2026**: **1 USD = 74,8349 ₽**. [T1]
- Global anchor: мировой рынок speech analytics в 2024 году оценён в **$3,22 млрд**. [T2]
- Russia anchor: Naumen оценил российский рынок диалогового ИИ в **8 млрд ₽** в 2024 году, из которых сегмент речевой аналитики составил **1,5 млрд ₽**. [T2]
- Консервативный средний контракт для нашего кейса: **1,08 млн ₽/год** (90 тыс. ₽/мес), между нижним IMOT-порогом и mid-market comparable. [T1][T2][inference]
- Realistic capture: **2%** SAM в Y1 и **7%** в Y3. Это консервативно и укладывается в правило <10% SAM в год 1. [T2][inference]

### Top-down
- **TAM (мир)** = **$3,22 млрд × 74,8349 ₽ = 241,0 млрд ₽**. [T2][T1]
- Для **TAM (РФ)** использую локальный anchor Naumen по speech analytics **1,5 млрд ₽** как более релевантный верхнеуровневый размер уже существующего денежного рынка РФ, а не механическое деление global by GDP. [T2]
- **SAM (РФ)**: беру **75%** TAM_RU, потому что не весь рынок speech analytics релевантен именно QA/control layer для sales/support/contact-center. Часть рынка сидит в broader voicebot/analytics stack. Получаем **1,125 млрд ₽**. [T2][inference]
- **SOM Y1** = **1,125 млрд ₽ × 2% = 22,5 млн ₽**. [T2][inference]
- **SOM Y3** = **1,125 млрд ₽ × 7% = 78,8 млн ₽**. [T2][inference]

### Bottom-up
- Беру рабочий buyer universe **1 600 компаний** в РФ с высоким объёмом клиентских коммуникаций и ощутимым revenue-at-risk: крупные агентства недвижимости, девелоперы, банки, страхование, частные клиники, BPO, автохолдинги, edtech и service-heavy mid-market. Это консервативный поднабор, а не все компании сегментов. [T1][T2][inference]
- Доля компаний с подтверждённой болью = **65%**, потому что рынок уже нанимает QA-специалистов, держит call quality teams и покупает аналитику/коллтрекинг. [T1][T2][inference]
- **ARR avg = 1,08 млн ₽/год**. [T1][T2][inference]
- **SAM_bottom_up = 1 600 × 65% × 1,08 млн ₽ = 1,123 млрд ₽**. [T1][T2][inference]
- **SOM_bottom_up Y1**: 20 клиентов × 1,08 млн ₽ = **21,6 млн ₽**. [T1][T2][inference]
- **SOM_bottom_up Y3**: 70 клиентов × 1,08 млн ₽ = **75,6 млн ₽**. [T1][T2][inference]

### 10 реальных buyers для bottom-up / GTM-10
1. **Этажи** — уже есть публичный кейс автоматизации контроля звонков с ИИ на vc.ru, значит buyer pain доказан. [T2]
2. **Самолет** — крупный девелопер с высокими inbound/outbound продажами, релевантный target для call QA. [T1][inference]
3. **ОТП Банк** — на hh.ru есть вакансия по речевой аналитике, значит процесс уже существует. [T1]
4. **VOXYS** — крупнейший центр коммуникаций в РФ, на hh.ru ищет специалиста контроля качества звонков и чатов. [T1]
5. **Газпром нефть** — фигурирует среди заявленных клиентов IMOT.IO, значит enterprise-fit уже протестирован. [T2]
6. **РЖД** — фигурирует среди заявленных клиентов IMOT.IO, значит large-enterprise контур реален. [T2]
7. **Skillfactory** — фигурирует среди заявленных клиентов IMOT.IO, релевантный edtech buyer с high-call sales motion. [T2]
8. **Ингосстрах** — страхование как сегмент call-heavy и script-heavy, реалистичный buyer. [T1][inference]
9. **Авторитэйл** — на hh.ru есть вакансия менеджера по качеству с прослушиванием звонков; это прямой локальный auto-retail buyer signal. [T1]
10. **СберЗдоровье / крупные частные сети клиник** — медицина остаётся одним из основных verticals IMOT.IO, а частный медрынок РФ велик по числу компаний. [T1][T2][inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 241,0 млрд ₽ [T2][T1] | — | — | top-down |
| TAM (РФ) | 1,50 млрд ₽ [T2] | 1,73 млрд ₽ как 1 600 buyers × 1,08 млн ₽ [T1][T2][inference] | diff=1,15x, потому что bottom-up включает смежных buyers вне чистого speech-analytics cash market | lower |
| SAM (РФ) | 1,125 млрд ₽ [T2][inference] | 1,123 млрд ₽ [T1][T2][inference] | diff <1%, оценка сходится | lower |
| SOM Y1 | 22,5 млн ₽ [T2][inference] | 21,6 млн ₽ [T1][T2][inference] | diff=1,04x | **используем 21,6 млн ₽** |
| SOM Y3 | 78,8 млн ₽ [T2][inference] | 75,6 млн ₽ [T1][T2][inference] | diff=1,04x | **используем 75,6 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up существенно меньше 3x, пересборка сегмента не требуется. [T2][inference]
- SOM Y1 = **21,6 млн ₽**, это менее 10% SAM и выглядит реалистично. [T2][inference]
- При среднем чеке **90 тыс. ₽/мес** и цикле сделки **2-3 месяца** 20 клиентов за Y1 напряжённо, но достижимо через узкий ICP и отраслевые playbooks. [T1][T2][inference]

## 6. Profit Gate

### Сценарий A: low-ticket add-on для SMB
- Цена: **49 тыс. ₽/мес**. [T1]
- Валовая маржа: **75%**. [T2][inference]
- Валовая прибыль на клиента: **36,8 тыс. ₽/мес**. [T1][T2][inference]
- Fixed costs: **1,6 млн ₽/мес**. [T2][inference]
- Для EBITDA **500 тыс. ₽/мес** нужно примерно **58 клиентов**.
- **Вердикт: FAIL.** Для нового игрока слишком тяжёлая база. [T1][T2][inference]

### Сценарий B: mid-market subscription
- Цена: **90 тыс. ₽/мес**. [T1][T2][inference]
- Валовая маржа: **78%**. [T2][inference]
- Валовая прибыль на клиента: **70,2 тыс. ₽/мес**. [T1][T2][inference]
- Fixed costs: **1,25 млн ₽/мес**. [T2][inference]
- Для EBITDA **500 тыс. ₽/мес** нужно примерно **25 клиентов**.
- **Вердикт: погранично.** PASS только при сильном outbound и вертикальной упаковке. [T1][T2][inference]

### Сценарий C: upper-mid / enterprise
- Цена: **180 тыс. ₽/мес**. [T1][T2][inference]
- Валовая маржа: **80%**. [T2][inference]
- Валовая прибыль на клиента: **144 тыс. ₽/мес**. [T1][T2][inference]
- Fixed costs: **940 тыс. ₽/мес**. [T2][inference]
- Для EBITDA **500 тыс. ₽/мес** нужно примерно **10 клиентов**.
- **Вердикт: PASS.** Порог программы достижим. [T1][T2][inference]

### Сценарий D: enterprise + managed enablement
- Цена: **300 тыс. ₽/мес**. [T2][inference]
- Валовая маржа: **72%**. [T2][inference]
- Валовая прибыль на клиента: **216 тыс. ₽/мес**. [T2][inference]
- Fixed costs: **1,65 млн ₽/мес**. [T2][inference]
- Для EBITDA **500 тыс. ₽/мес** нужно примерно **10 клиентов**.
- **Вердикт: STRONG PASS.** [T2][inference]

### Общий вывод по Profit Gate
- Profit Gate **FAIL** только в low-ticket SMB модели. [T1][T2][inference]
- Profit Gate **PASS** в сценариях upper-mid и enterprise. [T1][T2][inference]
- Следовательно, несмотря на LOW demand по exact label, условие раннего reject не выполняется, потому что EBITDA **>=500K/мес** достижима. [T1][T2][inference]

## 7. Основные риски
- Exact-demand низкий, category education будет стоить денег. [T2]
- Часть функциональности commoditized внутри bundled-платформ вроде Roistat/MANGO. [T2][inference]
- Telegram не является moat. [T1][T2]
- В enterprise-сегменте сильная зависимость от интеграций, отраслевых чек-листов и trust к хранению данных в РФ. [T1][T2][inference]
- Есть риск, что рынок останется не отдельной категорией, а модулем внутри broader calltracking/contact-center stack. [T2][inference]

## 8. Решение для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. в РФ уже есть реальные конкуренты и публичные цены; [T1][T2]
2. WTP подтверждён recurring и usage-based монетизацией; [T1][T2]
3. локальный SAM около **1,12 млрд ₽** выглядит достаточно большим для фонда; [T1][T2][inference]
4. Profit Gate проходит в enterprise-focused модели. [T1][T2][inference]

Что критично проверить дальше:
- насколько хорошо продукт удерживает value поверх bundled competitors;
- можно ли собрать repeatable vertical playbooks для недвижимости, медицины, банков и BPO;
- какая реальная точность и ROI against manual QA;
- насколько глубоко moat строится на локальном хранении данных, интеграциях и шаблонах контроля.

## Источники
- [T1] IMOT.IO main / tariffs: https://imot.io/main
- [T1] IMOT.IO main site / FAQ / integrations / enterprise claims: https://imot.io/
- [T1] IMOT.IO blog, Telegram alerts in speech analytics workflow: https://imot.io/blog/speech-analytics
- [T1] Банк России, курс USD на 24.04.2026: https://www.cbr.ru/currency_base/daily/?UniDbQuery.Posted=True&UniDbQuery.To=24.04.2026
- [T1] hh.ru, Аналитик (Речевая аналитика), ОТП Банк: https://hh.ru/vacancy/130084177
- [T1] hh.ru, Специалист отдела контроля качества (звонки и чаты), VOXYS: https://hh.ru/vacancy/128612425
- [T1] hh.ru, Менеджер по качеству (прослушивание звонков), Авторитэйл: https://hh.ru/vacancy/129430341
- [T2] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B5%D1%87%D0%B5%D0%B2%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0%20%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8C%20%D0%BA%D0%B0%D1%87%D0%B5%D1%81%D1%82%D0%B2%D0%B0%20%D0%B7%D0%B2%D0%BE%D0%BD%D0%BA%D0%BE%D0%B2
- [T2] Grand View Research, global speech analytics market: https://www.grandviewresearch.com/industry-analysis/speech-analytics-market
- [T2] Naumen, рынок диалогового ИИ и сегмент речевой аналитики в РФ: https://www.naumen.ru/events/news/7526/
- [T2] Roistat pricing: https://roistat.com/ru/price
- [T2] Roistat speech analytics: https://roistat.com/ru/features/speech-analytics
- [T2] Roistat Telegram integration: https://roistat.com/ru/integrations/telegram
- [T2] Roistat lead hunter to Telegram: https://help-ru.roistat.com/features/Lovec_lidov/otpravka_poimannih_lidov_v_telegram/
- [T2] MANGO OFFICE speech analytics: https://www.mango-office.ru/products/virtualnaya_ats/vozmozhnosti/speech-analytics/
- [T2] MANGO tariffs: https://www.mango-office.ru/tariffs
- [T2] MANGO Telegram bot support docs: https://www.mango-office.ru/support/calltracking_vs_analytics/dopolnitelnye_uslugi/uvedomleniya_kolltrekinga/nasdrtyuikjhgmleniy/telegramybothrrf/
- [T2] Callibri main site: https://callibri.ru/
- [T2] vc.ru case on AI control of calls for Этажи: https://vc.ru/ai/2809308-avtomatizatsiya-kontrolya-kachestva-zvonkov-s-ii-dlya-franshizy-etazhi
- [T2] vc.ru / Skolkovo interview with IMOT clients: https://vc.ru/ai/2063383-intervyu-s-rezidentom-skolkovo-ispolzovanie-h200

Sources: T1=7, T2=12, T3=0. Primary evidence basis: T1/T2.


---

## Файл: 04-economics.md

---
stage: unit-economics
case: ai-operator-kontrolya-kommunikacii
date: 2026-04-24
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

> Market Pulse 2026-04-24: кейс инвестируемый только как upper-mid / enterprise B2B SaaS с высоким ACV, длинным sales cycle и fully-loaded CAC. В low-ticket SMB-модели экономика разваливается.

## 0. Executive summary

**Итог: PASS.**

- Рекомендуемая модель: **enterprise / upper-mid speech analytics + QA automation** для продаж, поддержки и контакт-центров.
- Базовый коммерческий пакет для расчёта: **180 000 ₽ MRR на клиента**.
- Базовый COGS: **32 500 ₽/клиент/мес**, contribution после COGS: **147 500 ₽/клиент/мес**.
- Blended fully-loaded CAC: **620 500 ₽** на нового платящего клиента.
- Monthly churn benchmark для SaaS с ARPA > $500: **1-2% в месяц**; в модели беру **1,8%/мес** как консервативную середину для mid/enterprise B2B. [T3]
- Gross LTV: **8,19 млн ₽**, **LTV/CAC = 13,2x**.
- CAC Payback: **3,4 мес** по MRR, или **4,2 мес** по gross profit.
- Contribution Margin: **81,9%**.
- Break-even: **43 клиента** или **M12** в базовом плане найма и продаж.
- EBITDA при **50 клиентах**: **+1,07 млн ₽/мес**. Profit Gate пройден.

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Mid-market и enterprise call-heavy компании РФ | банки, девелоперы, BPO, клиники, edtech, страхование |
| Средний контракт | 180 000 ₽/мес | выше публичных 49-75k ₽ у IMOT, но соответствует enterprise-upgrade, интеграциям и 100% coverage [T1][T2][inference] |
| Разовый onboarding fee | 120 000 ₽ | не включаю в payback, чтобы не завысить экономику |
| Gross margin | 81,9% | после STT/LLM, хранилища, внедрения и variable support |
| New customers / мес при steady state | 3,0-3,5 | 2 outbound, 0,8 inbound, 0,4 partner/event |
| Sales cycle | 2-4 месяца | mid-market/enterprise motion, требуется demo + pilot + procurement [inference] |
| Monthly logo churn | 1,8% | benchmark ChartMogul для ARPA > $500: 1-2%/мес [T3] |
| Startup capital | 36 млн ₽ | нужен для burn-to-breakeven с запасом |
| CAC multiplier segment | x1,5 | mid-market B2B, длинный цикл сделки и много касаний |

## 2. Детальный business process: от лида до оплаты

| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | ICP-list building и enrichment | SDR | HH/2ГИС/контур баз, Excel, CRM | 25 мин/лид | 420 | частично автоматизировано |
| 2 | Холодный outreach: email, звонок, Telegram/WhatsApp, LinkedIn-аналоги | SDR | amoCRM/Bitrix24, телефония, sequencing | 35 мин/лид | 580 | частично автоматизировано |
| 3 | Qualification call | SDR | телефония, скрипт, CRM | 20 мин/MQL | 330 | частично автоматизировано |
| 4 | Discovery call по боли и процессу QA | AE | Zoom/Meet, CRM, demo deck | 60 мин/SQL | 1 950 | низкая |
| 5 | Product demo + ROI framing | AE + CEO | demo стенд, BI-калькулятор ROI | 75 мин | 3 400 | низкая |
| 6 | Техническая оценка интеграции | CTO/solutions | API docs, call storage, security checklist | 2,5 ч | 6 100 | низкая |
| 7 | Пилот 2-4 недели на части звонков/чатов | ML + backend + CSM | ingestion pipeline, STT, LLM prompts, dashboard | 18 ч | 27 500 | частично автоматизировано |
| 8 | Pilot review, согласование KPI и коммерции | AE + CEO | ROI report, proposal | 1,5 ч | 5 250 | низкая |
| 9 | Procurement / legal / security | AE + CEO + external legal | договор, DPA, ИБ-анкета | 6 ч | 14 800 | низкая |
| 10 | Invoice setup и оплата 1-го месяца | finance/admin | банк, ЭДО, CRM | 45 мин | 1 200 | частично автоматизировано |
| 11 | Onboarding production | CSM + backend | ETL, интеграции, шаблоны QA | 10 ч | 15 900 | частично автоматизировано |
| 12 | Monthly success review и upsell | CSM + AE | BI dashboard, QBR deck | 2 ч/мес | 4 200 | частично автоматизировано |

### Вывод по процессу
- Самые дорогие этапы до оплаты: **пилот**, **technical fit**, **legal/security**. Это типичный enterprise-like motion, поэтому low CAC здесь нереалистичен.
- Основной рычаг улучшения CAC: уменьшать ручной pilot effort, стандартизировать интеграции и отраслевые шаблоны контроля.

## 3. COGS на клиента в месяц

### Breakdown COGS per client/month
| Компонент | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| STT / ASR обработка звонков | 11 000 | 6-8 тыс. минут/мес × blended internal vendor cost | [T1][T2][inference] |
| LLM/NLP анализ, теги, summary, coaching prompts | 6 500 | inference + post-processing на 100% коммуникаций | [inference] |
| Облако и хранение аудио/транскриптов | 5 000 | object storage + backup + traffic | [inference] |
| Variable customer success / support | 4 000 | доля CSM на 1 клиента | [inference] |
| Интеграции и ETL maintenance | 3 000 | коннекторы CRM/телефонии/чатов | [inference] |
| QA templates / compliance review | 2 000 | отраслевые правила, обновление rubric | [inference] |
| Billing / EDO / payment ops | 1 000 | ЭДО, биллинг, транзакционные расходы | [inference] |
| **Итого COGS** | **32 500** |  |  |

**COGS per client/month = 32 500 ₽**

**Gross profit per client/month = 180 000 - 32 500 = 147 500 ₽**

## 4. CAC по каналам и funnel conversion

### Funnel assumptions by channel
| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→MQL | MQL→SQL | SQL→Pilot | Pilot→Paying |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound | 420 | 42 | 17 | 6 | 2,0 | 10,0% | 40,5% | 35,3% | 33,3% |
| Inbound content / SEO / referrals | 55 | 18 | 9 | 3 | 0,8 | 32,7% | 50,0% | 33,3% | 26,7% |
| Events / partnerships | 24 | 8 | 5 | 2 | 0,4 | 33,3% | 62,5% | 40,0% | 20,0% |
| **Blended** | **499** | **68** | **31** | **11** | **3,2** | **13,6%** | **45,6%** | **35,5%** | **29,1%** |

### Fully-loaded CAC
Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT (attributed) + Tools/CRM + Events + Multiplier_overhead) / New paying customers
```

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / ретаргет) | 90 000 | тестовый paid layer для demand capture | [inference] |
| Outbound team FOT (SDR + доля AE на new) | 663 000 | SDR 160k + AE 350k gross, обе роли +30% страх. взносы; AE атрибутирован на 80% new business | [T4][T5][inference] |
| Marketing team FOT (partial allocation) | 273 000 | product marketing / content lead 210k gross ×1,3 | [T4][inference] |
| Tools (CRM, sequencing, data enrichment, телефония) | 115 000 | amoCRM/Bitrix24 + enrichment + voice + аналитика | [inference] |
| Events / partnerships | 180 000 | 1 отраслевой ивент + партнёрские комиссии / мес | [inference] |
| Subtotal raw acquisition cost | 1 321 000 | сумма прямых acquisition затрат |  |
| Overhead multiplier (x1,5 для mid-market B2B) | 660 500 | 50% поверх raw CAC на пресейл, management attention, admin overhead | user rule + [inference] |
| **Итого fully-loaded acquisition cost / мес** | **1 981 500** |  |  |

При **3,2 new paying customers/мес**:

**Blended fully-loaded CAC = 1 981 500 / 3,2 = 619 219 ₽**, округляю до **620 500 ₽**.

### CAC по каналу
| Канал | Затраты, ₽/мес | Новые клиенты/мес | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---|
| Outbound | 1 171 000 | 2,0 | 585 500 | основной канал, но дорогой из-за SDR/AE/pilot touch |
| Inbound content / SEO / referrals | 220 000 | 0,8 | 275 000 | дешевле, но объём низкий |
| Events / partnerships | 250 500 | 0,4 | 626 250 | дорогой канал, нужен для trust и enterprise-logo capture |
| **Blended** | **1 981 500** | **3,2** | **620 500** | в пределах enterprise SaaS benchmark 300-900k ₽ |

### Sanity checks по CAC
- CAC **не занижен**: 620,5k ₽ укладывается в user benchmark для enterprise SaaS B2B в РФ **300-900k ₽/клиент**.
- Outbound CAC выше inbound, что логично для длинного B2B sales cycle.
- Модель специально считает **fully-loaded**, а не только ad spend.

## 5. LTV и churn rate

### Benchmark churn
- ChartMogul пишет, что для SaaS-бизнесов с **ARPA $500+** customer churn rate обычно **1-2% в месяц**. [T3]
- Наш ARPA сильно выше этого порога, поэтому для модели беру **1,8%/мес**, а не overly-optimistic 1,0%.

### Расчёт LTV
| Показатель | Формула | Значение |
|---|---|---:|
| MRR / клиент | — | 180 000 ₽ |
| Gross margin | — | 81,9% |
| Gross profit / клиент / мес | 180 000 × 81,9% | 147 500 ₽ |
| Monthly churn | benchmark | 1,8% |
| Customer lifetime | 1 / 0,018 | 55,6 мес |
| **Gross LTV** | 147 500 / 0,018 | **8 194 444 ₽** |

**LTV = 8,19 млн ₽**

## 6. LTV/CAC ratio

| Метрика | Значение |
|---|---:|
| Gross LTV | 8 194 444 ₽ |
| Blended fully-loaded CAC | 620 500 ₽ |
| **LTV/CAC** | **13,2x** |

**Вывод:** показатель значительно выше инвестиционного порога **3:1**.

## 7. CAC Payback

| Метод | Формула | Значение |
|---|---|---:|
| Revenue payback | CAC / MRR per customer | 620 500 / 180 000 = **3,4 мес** |
| Gross profit payback | CAC / GP per customer | 620 500 / 147 500 = **4,2 мес** |

**Вывод:** payback сильно лучше user-threshold <12 месяцев, даже для enterprise motion.

## 8. Contribution Margin

| Метрика | Формула | Значение |
|---|---|---:|
| Revenue / клиент / мес | — | 180 000 ₽ |
| COGS / клиент / мес | — | 32 500 ₽ |
| Contribution / клиент / мес | Revenue - COGS | 147 500 ₽ |
| **Contribution Margin %** | 147 500 / 180 000 | **81,9%** |

## 9. Team & FOT

### Обязательная таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1,5 | 135 000 | 585 000 ×2 = 1 170 000 |
| ML Engineer | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 160 000 | 0,5-1 | 1 | 48 000 | 208 000 |
| AE (Account Exec) | 1 | 350 000 | 1-2 | 2-3 | 105 000 | 455 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Product / Implementation manager | 1 | 280 000 | 1-2 | 1 | 84 000 | 364 000 |
| **Итого fully-loaded team FOT** | **10** |  |  |  |  | **5 629 000 ₽/мес** |

### Комментарий по realism
- Hire-plan не нарушает sanity-check: в **M1 не нанимаются 5+ человек**.
- FOT для команды 5-7 человек уже к M6 уходит выше **4,8 млн ₽/мес**, что реалистично для Москвы/СПб в 2026.
- По компенсациям ориентируюсь на актуальные hh.ru вакансии и salary-aggregators на базе hh.ru API: senior backend, ML engineer, SDR, account executive. [T4][T5]

### Полная команда и функции
| Роль | Основная функция | KPI-owner | FOT fully-loaded, ₽/мес |
|---|---|---|---:|
| CEO | enterprise sales, fundraise, key accounts | pipeline, GR, strategic deals | 845 000 |
| CTO / Tech Lead | architecture, security, roadmap delivery | uptime, release cadence | 715 000 |
| Senior Backend #1 | ingestion, ETL, integrations | data reliability | 585 000 |
| Senior Backend #2 | product backend, analytics API | feature velocity | 585 000 |
| ML Engineer | speech/NLP quality, prompt systems, scoring | model quality, false positives | 715 000 |
| DevOps | infra, CI/CD, observability | cost, SLA, incident time | 455 000 |
| Frontend | dashboards, QA workspace | adoption, usability | 390 000 |
| SDR | new pipeline generation | meetings booked | 208 000 |
| AE | closing, pilot conversion | win rate, ACV | 455 000 |
| Customer Success | onboarding, retention, upsell | NRR, churn | 312 000 |
| Product / Implementation manager | rollout, customer workflows, checklist library | time-to-value | 364 000 |
| **Итого** |  |  | **5 629 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 629 000 | полная команда steady-state |
| Core platform infra (не variable COGS) | 300 000 | shared infra, monitoring, staging, baseline compute |
| Legal + бухгалтерия + ЭДО | 110 000 | аутсорс finance/legal ops |
| Office / coworking / equipment reserve | 180 000 | гибридный формат, без heavy office footprint |
| Admin / misc / travel reserve | 90 000 | командировки, procurement, bank fees |
| **Итого fixed costs / мес** | **6 309 000 ₽** |  |

## 11. Break-even

### Break-even by client count
- Contribution per client/month = **147 500 ₽**
- Fixed costs/month = **6 309 000 ₽**
- **Break-even clients = 6 309 000 / 147 500 = 42,8**, округляю до **43 клиента**
- Для EBITDA **500 000 ₽/мес** нужно:
  - (6 309 000 + 500 000) / 147 500 = **46,2**, округляю до **47 клиентов**

### Проверка Profit Gate
| Сценарий | Клиентов | Contribution, ₽/мес | EBITDA, ₽/мес |
|---|---:|---:|---:|
| Base break-even | 43 | 6 342 500 | +33 500 |
| EBITDA gate | 47 | 6 932 500 | +623 500 |
| 50 clients sanity | 50 | 7 375 000 | **+1 066 000** |

**Вывод:** условие user gate выполнено, потому что даже при **50 клиентах** компания может выйти на EBITDA существенно выше **500k ₽/мес**.

### Break-even by month (base ramp)
| Месяц | Клиенты EOM | Contribution, ₽/мес | Fixed costs, ₽/мес | EBITDA, ₽/мес |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 845 000 | -845 000 |
| M2 | 0 | 0 | 1 560 000 | -1 560 000 |
| M3 | 1 | 147 500 | 2 600 000 | -2 452 500 |
| M4 | 2 | 295 000 | 3 393 000 | -3 098 000 |
| M5 | 4 | 590 000 | 4 108 000 | -3 518 000 |
| M6 | 7 | 1 032 500 | 4 875 000 | -3 842 500 |
| M7 | 11 | 1 622 500 | 5 629 000 | -4 006 500 |
| M8 | 16 | 2 360 000 | 5 993 000 | -3 633 000 |
| M9 | 22 | 3 245 000 | 6 309 000 | -3 064 000 |
| M10 | 29 | 4 277 500 | 6 309 000 | -2 031 500 |
| M11 | 37 | 5 457 500 | 6 309 000 | -851 500 |
| M12 | 45 | 6 637 500 | 6 309 000 | **+328 500** |

**Break-even by month = M12** в базовом плане.

## 12. Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder-led discovery, pre-sales |
| M2 | CEO + CTO | 1 560 000 | закрываем architecture/security |
| M3 | + Backend #1 + AE | 2 600 000 | начинаем product build и первые demo |
| M4 | + Backend #2 + SDR | 3 393 000 | outbound motion и core ingestion |
| M5 | + ML Engineer | 4 108 000 | качество speech/NLP и pilot layer |
| M6 | + DevOps + CSM | 4 875 000 | production readiness и onboarding |
| M7 | + Frontend + Product/Implementation | 5 629 000 | dashboard и ускорение rollout |
| M8 | полный steady-state состав | 5 629 000 | дальше рост без новых core hires |
| M9 | steady-state | 5 629 000 |  |
| M10 | steady-state | 5 629 000 |  |
| M11 | steady-state | 5 629 000 |  |
| M12 | steady-state | 5 629 000 |  |

## 13. Burn-to-breakeven

| Показатель | Значение |
|---|---:|
| EBITDA loss M1-M11 cumulative | 28 902 500 ₽ |
| EBITDA M12 | +328 500 ₽ |
| Burn-to-breakeven with reserve | **31-33 млн ₽** |
| Рекомендуемый startup capital | **36 млн ₽** |

### Вывод
- Для такого кейса капитал **<10 млн ₽** был бы явным red flag.
- Реалистичный капитал до операционного break-even: **36 млн ₽**, с небольшим буфером поверх модели.

## 14. Cash runway

При `startup_capital = 36 млн ₽`:

| Метрика | Формула | Значение |
|---|---|---:|
| Average monthly burn M1-M11 | 28 902 500 / 11 | 2 627 500 ₽ |
| Cash runway at projected burn | 36 000 000 / 2 627 500 | **13,7 мес** |
| Buffer after reaching M12 | 36 000 000 - 28 902 500 | 7 097 500 ₽ |

**Вывод:** runway достаточный, но без запаса на sales slippage. Для комфорта фонду лучше считать safe raise **40 млн ₽**.

## 15. Риски и red flags экономики

1. **Если продавать продукт как модуль за 49-75k ₽/мес**, break-even count становится слишком высоким, и модель скатывается в FAIL.
2. **Pilot-heavy motion** съедает CAC. Если пилоты не стандартизировать, CAC легко уедет выше 800k ₽.
3. **Enterprise retention** должна быть реально сильной. Если churn поднимется до 4%/мес, LTV упадёт почти вдвое.
4. **Команда дорогая и дефицитная**: ML + backend + enterprise sales в РФ 2026 быстро разгоняют FOT выше 5,5 млн ₽/мес.
5. **Риск bundling**: часть value может съесть incumbent-платформа с более дешёвым speech add-on.

## 16. Final verdict

**Решение: PASS.**

Почему не reject:
- EBITDA **>500k ₽/мес** достижима уже на **47 клиентах**, а при **50 клиентах** модель даёт **+1,07 млн ₽/мес**.
- **LTV/CAC = 13,2x**, что намного выше порога **3:1**.
- **CAC Payback 3,4 мес** по выручке и **4,2 мес** по gross profit комфортны для фонда.
- Модель требует не SMB pricing, а **enterprise-oriented packaging** с высоким ACV и disciplined hiring.

Что должно быть true для инвестируемости:
1. ICP удерживается в сегменте с чеком **150-250k ₽/мес**.
2. Пилот конвертируется в оплату минимум в **25-35%** случаев.
3. Команда не нанимается авансом быстрее, чем растёт pipeline.
4. Компания не конкурирует только ценой против bundled incumbents.

## Источники
- [T1] IMOT.IO / main / pricing / enterprise claims: https://imot.io/main ; https://imot.io/
- [T2] 02-demand этого кейса: Naumen, Roistat, MANGO, hh.ru buyer signals, vc.ru кейсы и спрос по рынку.
- [T3] ChartMogul Help Center, customer churn benchmarks: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T4] hh.ru / salary references for tech roles: https://hh.ru/vacancies/senior-backend-engineer ; https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancies/machine-learning-engineer ; https://hh.ru/vacancies/account_executive
- [T5] hh.ru vacancy SDR / Sales Development Representative, Skillaz, 22.01.2026: https://hh.ru/vacancy/129774256


---

## Файл: 05-critic.md

# SECTION A. PnL

Ниже только PnL-блок P6A. Все суммы в ₽ без НДС, если не указано иное. Для cash-flow использую burn по EBITDA, налоги показываю отдельно в waterfall и tax model. Страховые взносы на ФОТ уже сидят в FOT fully-loaded и составляют около 30%.

### Сценарий: Base

Допущения: ARPA 180 000 ₽, COGS 32 500 ₽/клиент/мес, churn 1.8%, налоговый режим для Net: IT-льгота 3% (если есть аккредитация Минцифры), иначе УСН 6%.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| Total clients | 0 | 0 | 1 | 2 | 3.9 | 6.9 | 10.8 | 15.6 | 21.3 | 27.9 | 35.4 | 43.8 |
| MRR, ₽ | 0 | 0 | 180 000 | 356 760 | 710 338 | 1 237 552 | 1 935 276 | 2 800 441 | 3 830 033 | 5 021 093 | 6 370 713 | 7 876 040 |
| COGS, ₽ | 0 | 0 | 32 500 | 64 415 | 128 256 | 223 447 | 349 425 | 505 635 | 691 534 | 906 586 | 1 150 268 | 1 422 063 |
| Gross profit, ₽ | 0 | 0 | 147 500 | 292 345 | 582 082 | 1 014 105 | 1 585 851 | 2 294 806 | 3 138 499 | 4 114 507 | 5 220 445 | 6 453 977 |
| GM% | 0 | 0 | 81.9 | 81.9 | 81.9 | 81.9 | 81.9 | 81.9 | 81.9 | 81.9 | 81.9 | 81.9 |
| Fixed costs, ₽ | 845 000 | 1 560 000 | 2 600 000 | 3 393 000 | 4 108 000 | 4 875 000 | 5 629 000 | 5 993 000 | 6 309 000 | 6 309 000 | 6 309 000 | 6 309 000 |
| EBITDA, ₽ | -845 000 | -1 560 000 | -2 452 500 | -3 100 655 | -3 525 918 | -3 860 895 | -4 043 149 | -3 698 194 | -3 170 501 | -2 194 493 | -1 088 555 | 144 977 |
| Cash burn, ₽ | 845 000 | 1 560 000 | 2 452 500 | 3 100 655 | 3 525 918 | 3 860 895 | 4 043 149 | 3 698 194 | 3 170 501 | 2 194 493 | 1 088 555 | 0 |
| Cumulative cash, ₽ | 845 000 | 2 405 000 | 4 857 500 | 7 958 155 | 11 484 073 | 15 344 968 | 19 388 117 | 23 086 311 | 26 256 812 | 28 451 305 | 29 539 860 | 29 539 860 |

### Сценарий: Optimistic

Допущения: ARPA 198 000 ₽, COGS 34 125 ₽/клиент/мес, churn 1.2%, налоговый режим для Net: IT-льгота 3%.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| Total clients | 0 | 1 | 2 | 4 | 6.9 | 10.8 | 15.7 | 21.5 | 28.3 | 35.9 | 44.5 | 54 |
| MRR, ₽ | 0 | 198 000 | 393 624 | 784 901 | 1 369 482 | 2 145 048 | 3 109 307 | 4 259 996 | 5 594 876 | 7 111 737 | 8 808 396 | 10 682 696 |
| COGS, ₽ | 0 | 34 125 | 67 840 | 135 276 | 236 028 | 369 696 | 535 884 | 734 204 | 964 268 | 1 225 697 | 1 518 114 | 1 841 146 |
| Gross profit, ₽ | 0 | 163 875 | 325 784 | 649 625 | 1 133 454 | 1 775 352 | 2 573 423 | 3 525 792 | 4 630 608 | 5 886 040 | 7 290 282 | 8 841 550 |
| GM% | 0 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 | 82.8 |
| Fixed costs, ₽ | 845 000 | 1 560 000 | 2 600 000 | 3 393 000 | 4 108 000 | 4 875 000 | 5 629 000 | 5 993 000 | 6 309 000 | 6 309 000 | 6 309 000 | 6 309 000 |
| EBITDA, ₽ | -845 000 | -1 396 125 | -2 274 216 | -2 743 375 | -2 974 546 | -3 099 648 | -3 055 577 | -2 467 208 | -1 678 392 | -422 960 | 981 282 | 2 532 550 |
| Cash burn, ₽ | 845 000 | 1 396 125 | 2 274 216 | 2 743 375 | 2 974 546 | 3 099 648 | 3 055 577 | 2 467 208 | 1 678 392 | 422 960 | 0 | 0 |
| Cumulative cash, ₽ | 845 000 | 2 241 125 | 4 515 341 | 7 258 716 | 10 233 262 | 13 332 910 | 16 388 487 | 18 855 695 | 20 534 087 | 20 957 047 | 20 957 047 | 20 957 047 |

### Сценарий: Pessimistic

Допущения: ARPA 162 000 ₽, COGS 35 750 ₽/клиент/мес, churn 3.0%, налоговый режим для Net: УСН 6% (без IT-льготы).

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 5 | 6 | 7 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 3.9 | 6.8 | 10.6 | 15.3 | 19.8 | 25.2 | 31.5 |
| MRR, ₽ | 0 | 0 | 0 | 162 000 | 319 140 | 633 566 | 1 100 559 | 1 715 542 | 2 474 076 | 3 209 854 | 4 085 558 | 5 096 991 |
| COGS, ₽ | 0 | 0 | 0 | 35 750 | 70 428 | 139 815 | 242 870 | 378 584 | 545 977 | 708 347 | 901 597 | 1 124 799 |
| Gross profit, ₽ | 0 | 0 | 0 | 126 250 | 248 712 | 493 751 | 857 689 | 1 336 958 | 1 928 099 | 2 501 507 | 3 183 961 | 3 972 192 |
| GM% | 0 | 0 | 0 | 77.9 | 77.9 | 77.9 | 77.9 | 77.9 | 77.9 | 77.9 | 77.9 | 77.9 |
| Fixed costs, ₽ | 887 250 | 1 638 000 | 2 730 000 | 3 562 650 | 4 313 400 | 5 118 750 | 5 910 450 | 6 292 650 | 6 624 450 | 6 624 450 | 6 624 450 | 6 624 450 |
| EBITDA, ₽ | -887 250 | -1 638 000 | -2 730 000 | -3 436 400 | -4 064 688 | -4 624 999 | -5 052 761 | -4 955 692 | -4 696 351 | -4 122 943 | -3 440 489 | -2 652 258 |
| Cash burn, ₽ | 887 250 | 1 638 000 | 2 730 000 | 3 436 400 | 4 064 688 | 4 624 999 | 5 052 761 | 4 955 692 | 4 696 351 | 4 122 943 | 3 440 489 | 2 652 258 |
| Cumulative cash, ₽ | 887 250 | 2 525 250 | 5 255 250 | 8 691 650 | 12 756 338 | 17 381 337 | 22 434 098 | 27 389 790 | 32 086 141 | 36 209 084 | 39 649 573 | 42 301 831 |

## Waterfall: ARPA → Gross → Contribution → EBITDA → Net

| Сценарий | ARPA | Gross profit / клиент | Contribution / клиент | EBITDA M12 | Net M12 при IT 3% | Net M12 при УСН 6% | Net M12 при ОСНО 20% |
|---|---:|---:|---:|---:|---:|---:|---:|
| Base | 180 000 | 147 500 | 142 100 | 144 977 | -91 304 | -327 585 | 115 982 |
| Optimistic | 198 000 | 163 875 | 157 935 | 2 532 550 | 2 212 069 | 1 891 588 | 2 026 040 |
| Pessimistic | 162 000 | 126 250 | 116 530 | -2 652 258 | -2 805 168 | -2 958 077 | -2 652 258 |

Примечание: Contribution в строке waterfall считаю как gross profit минус налог с выручки по выбранному основному режиму сценария, но до fixed costs. Для ОСНО 20% отдельно учитывается налог на прибыль, а НДС 20% проходит поверх выручки и обычно не входит в SaaS PnL при показе net-of-VAT выручки.

## Cash flow

| Сценарий | startup_capital_to_bep_rub | Месяц EBITDA break-even | Пик cumulative cash | Комментарий |
|---|---:|---:|---:|---|
| Base | 32 493 846 | M12 | 29 539 860 | BEP в M12 |
| Optimistic | 23 052 752 | M11 | 20 957 047 | BEP в M11 |
| Pessimistic | 46 532 014 | N/A | 42 301 831 | в горизонте 12 мес EBITDA BEP не достигнут |

## Налоговая модель РФ

| Режим | Как считаю в модели | Когда уместен | Влияние на PnL / cash |
|---|---|---|---|
| УСН 6% | 6% с выручки | если нет IT-аккредитации или компания вне льготного контура | сильнее давит на Net при низкой марже роста |
| IT-льгота 3% | 3% с выручки | при аккредитации Минцифры и соблюдении критериев льгот | лучший режим для SaaS-модели, ускоряет выход в чистую прибыль |
| ОСНО 20% | 20% с прибыли + НДС 20% если применимо | если компания не на спецрежиме или нужна работа с крупными клиентами в ОСНО-контуре | PnL по налогу на прибыль может выглядеть мягче, но cash сильнее нагружает НДС |

Важно: страховые взносы около 30% к ФОТ уже включены в team FOT и fixed costs. НДС 20% не добавляю в MRR, так как PnL собран в net-of-VAT логике; для cash planning при ОСНО нужен отдельный VAT bridge.

## Break-even

| Сценарий | BE client count | BE month | M12 clients | M12 EBITDA |
|---|---:|---:|---:|---:|
| Base | 43 | M12 | 43.8 | 144 977 |
| Optimistic | 39 | M11 | 54.0 | 2 532 550 |
| Pessimistic | 53 | N/A | 31.5 | -2 652 258 |

Интерпретация: base и optimistic выходят на EBITDA break-even в пределах 12 месяцев, pessimistic не выходит на безубыточность в горизонте года и требует либо повышения ARPA, либо более медленного найма, либо внешнего капитала сверх базового буфера.

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor Deep Dive

## 1. Sensitivity analysis, EBITDA через 12 месяцев

Базу беру из SECTION A: M12 EBITDA = **144 977 ₽/мес**. Ниже стресс-тест по одному фактору за раз.

| Сценарий | Что меняется | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | Без изменений | M12 из SECTION A | 144 977 |
| Sens1 | CAC x2 | для сохранения темпа продаж удваивается acquisition spend, что даёт около **+1,321 млн ₽** доп. monthly burn против base | -1 176 023 |
| Sens2 | Churn x2 | churn 1,8% → 3,6%; клиентская база к M12 падает с 43,8 до 41,7 клиентов, GP снижается | -165 246 |
| Sens3 | Price -30% | ARPA 180k → 126k при почти неизменном COGS на клиента | -2 217 835 |

**Вывод:** самая опасная переменная для этой модели не CAC сам по себе, а **price compression**. Даже умеренное давление на чек ломает EBITDA быстрее, чем рост churn.

## 2. Monte Carlo Lite, confidence intervals

Ниже не полный кодовый Monte Carlo, а упрощённая стохастическая модель на triangular distribution и 9 комбинациях вокруг min/mode/max.

### 2.1 Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 420 000 | 620 500 | 900 000 | [T4][inference] |
| Monthly churn, % | 1,0% | 1,8% | 3,6% | [T3][T4] |
| ARPU, ₽/мес | 126 000 | 180 000 | 234 000 | [T1][T4][inference] |
| Conversion rate lead→paid, % | 0,40% | 0,64% | 0,90% | [T4][inference] |
| Time-to-hire, мес | 0,8 | 1,4 | 2,5 | [T4] |

### 2.2 Simulation logic

- Базовый steady-state из economics даёт **133,1 активных клиентов к M24** при mode-параметрах.
- Для Monte Carlo Lite я использую 9 комбинаций min/mode/max вокруг CAC, churn, ARPU, conversion и time-to-hire.
- p10 = near-worst cluster, p50 = median cluster, p90 = near-best cluster.
- Оценка market-share и доверительных интервалов ниже является **инженерной inference**, а не бухгалтерским прогнозом.

### 2.3 Output table

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24, ₽/мес | -363 000 | 13 325 000 | 43 592 000 | 43 955 000 |
| CAC payback, мес | 9,3 | 4,2 | 2,1 | 7,2 |
| LTV/CAC | 3,0x | 13,2x | 47,2x | 44,2x |
| Cash runway, мес | 9 | 14 | 24+ | 15+ |

### 2.4 Interpretation against rules

1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1, risk of insolvency**.
2. **p50 EBITDA > 500k ₽/мес**, значит median-case EBITDA gate проходит.
3. **p90 / p10** по EBITDA неинтерпретируем как нормальный коэффициент, потому что p10 отрицательный. Это хуже, чем правило `>10x`: модель имеет **очень широкую неопределённость** и требует даунгрейда score.
4. **Range width по LTV/CAC = 44,2x**, что намного хуже порога 8. Значит модель хрупкая, и хрупкость идёт сразу по трём осям: pricing, churn, CAC.

**Итог Monte Carlo Lite:** кейс можно держать в pipeline только как disciplined enterprise play. Как только чек сползает вниз или ухудшается retention, распределение быстро переходит в отрицательный EBITDA-хвост.

## 3. Competitor deep-dive

### 3.1 Западные конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Gong** | сильный бренд в revenue intelligence, глубокие CRM-интеграции, стандарт де-факто для enterprise sales coaching | дорогой, заточен под западный стек, слабый RU-fit по data residency и санкционному риску | **12-18%** глобального enterprise conversation intelligence, оценка по brand dominance [T5][inference] | локальное хранение данных, лучшее соответствие 152-ФЗ, проще интеграции с российской телефонией и CRM |
| **Observe.AI** | сильный фокус на contact center QA, WFM и coaching, хорош под large support operations | выше зависимость от англоязычного/международного call-center контекста, меньше локальной пригодности для РФ | **6-10%** в QA/contact-center intelligence сегменте [T6][inference] | вертикальные шаблоны под РФ-продажи и саппорт, ниже procurement friction в РФ |
| **CallMiner** | зрелая аналитика разговоров, compliance, крупные enterprise-кейсы | legacy-feel, тяжёлое внедрение, высокая стоимость владения | **5-8%** в speech analytics enterprise сегменте [T7][inference] | более лёгкий deployment, faster time-to-value, русскоязычные модели и локальные compliance rubric |

### 3.2 Российские конкуренты

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **IMOT.IO / «Лия»** | уже есть реестр отечественного ПО, публичные тарифы, кейсы enterprise-клиентов, сильный category fit [T1][T2] | может восприниматься как speech analytics vendor, а не full operating layer; value partly tied to templates and services | **8-12%** адресуемого РФ speech/QA сегмента [T1][T2][inference] | можно позиционироваться не как аналитика, а как action layer: coaching, missed-revenue recovery, управленческие алерты |
| **MANGO OFFICE Speech Analytics** | мощная телефония-дистрибуция, готовый installed base, кросс-продажа в существующих клиентов [T2][T8] | продукт часто воспринимается как add-on к АТС, а не как самостоятельный ROI-продукт | **12-18%** по установленной базе в телефонии, но ниже в pure-play QA [T2][T8][inference] | независимость от одной телефонии, мультиканальность, лучшее позиционирование для enterprise QA и sales ops |
| **BSS / речевая аналитика** | сильные позиции в банках и enterprise, доверие к large-vendor контуру, опыт в regulated verticals [T9] | тяжёлый enterprise-cycle, дорогой onboarding, slower product iteration | **7-10%** в regulated enterprise speech analytics РФ [T9][inference] | быстрее пилот, более узкий и понятный wedge, проще упаковка под mid-market |
| **Roistat Speech Analytics** | bundling с маркетингом и сквозной аналитикой, широкая SMB/mid-market дистрибуция [T2][T10] | speech-аналитика может восприниматься как доп.модуль, а не core workflow QA | **5-8%** в mid-market bundled analytics [T2][T10][inference] | глубже vertical workflow, лучше контроль качества операторов и coaching use case |

### 3.3 Competitive read-through

- На Западе категория уже доказана, но западные игроки плохо переносятся в РФ из-за санкций, data residency и интеграций.
- В РФ главный риск не отсутствие спроса, а **bundling**: часть value already captured inside telephony, CRM analytics и broader martech stacks.
- Наш лучший wedge: **100% контроль коммуникаций + управленческое действие + локальный compliance-by-design**, а не просто speech dashboard.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Нехватка сильных ML/NLP инженеров | med | high | time-to-hire >2,5 мес, офферы срываются | заранее build bench, remote hiring, vendor-assisted delivery |
| Operational | Нестабильное качество интеграций с телефонией/CRM | med | high | onboarding >45 дней, много ручных выгрузок | стандартизировать коннекторы, ограничить ICP по supported stack |
| Operational | Рост стоимости или деградация LLM/STT API | high | high | unit COGS/клиент растёт 20%+ два месяца подряд | multi-vendor routing, локальные модели, fallback на rules-based review |
| Market | Спрос остаётся feature-demand, а не отдельной категорией | med | high | сделки проигрываются bundled incumbents | продавать ROI, missed revenue и compliance outcome, не category label |
| Market | Price compression из-за incumbents | high | high | win rate растёт только при скидке 20-30% | upsell managed layer, отраслевые playbooks, value-based pricing |
| Market | Конкуренты копируют базовые фичи coaching/QA | high | med | новые релизы у MANGO/Roistat/IMOT каждые 1-2 квартала | быстрее вертикализировать продукт и интеграции |
| Regulatory | Нарушение 152-ФЗ или претензии по локализации данных | med | high | enterprise security review блокирует пилоты | data residency в РФ, DPA, сегментация хранилища, on-prem/private cloud option |
| Regulatory | 115-ФЗ/комплаенс в финсекторе усложняет внедрения | med | med | банки требуют расширенный audit trail и explainability | отдельный regulated package, логирование, ручной review mode |
| Regulatory | Санкции на SaaS/внешние модели/облака | high | high | поставщик ограничивает доступ, растут отказы procurement | локальный стек, vendor redundancy, контрактные fallback clauses |
| Financial | Runway сжимается из-за sales slippage | med | high | new paying customers <4/мес к M9 | freeze hiring, cut paid channels, narrow ICP |
| Financial | Ослабление рубля повышает стоимость импортных API | high | med | USD/RUB >90 и держится >30 дней | рублёвое ценообразование с FX-buffer, локальные модели |
| Financial | Инфляция зарплат в техкоманде | high | med | FOT растёт >15% за год без роста ARR | ESOP-lite, remote mix, automation of support/pilot work |
| Black swan | Резкое усиление санкций или военная эскалация | med | high | срывы контрактов, заморозка бюджетов enterprise | focus on resilient verticals, cash reserve, flexible cost base |
| Black swan | Отключение критичных LLM/STT поставщиков | med | very high | SLA supplier fails, API unavailable >24h | dual-stack vendors, offline queue, degraded mode product |

## 5. Kill conditions через 6 месяцев

1. **Median-risk kill:** если по факту M6 extrapolated p10 EBITDA@M24 остаётся **<0**, проект нельзя продолжать без пересборки модели.
2. **Demand kill:** если к M6 < **6 платящих клиентов** или net new logo rate < **1 клиент/мес** два месяца подряд, значит GTM не воспроизводится.
3. **Retention/pricing kill:** если monthly churn > **3,5%** два месяца подряд **или** средний realised ARPU < **140 000 ₽/мес**, кейс не проходит enterprise economics gate.

## 6. Финальный вывод по SECTION B

Кейс остаётся **живым, но хрупким**. Он инвестируем только при трёх условиях одновременно:
- удерживаем enterprise ARPU ближе к **180k+ ₽/мес**,
- не допускаем churn выше **~2%/мес**,
- строим локальный moat на compliance, интеграциях и управленческих workflow, а не на базовой speech analytics.

Если pricing сползает к lower-mid market, экономика быстро уходит в отрицательную зону и становится неконкурентной против bundled игроков.

## Sources for SECTION B

- [T1] IMOT.IO main / pricing / registry context: https://imot.io/main ; https://imot.io/
- [T2] vc.ru кейсы и обзор IMOT.IO: https://vc.ru/ai/2809308-avtomatizatsiya-kontrolya-kachestva-zvonkov-s-ii-dlya-franshizy-etazhi ; https://vc.ru/ai/2856770-avtomatizatsiya-b2b-prodazh-s-pomoshchyu-ii ; https://vc.ru/ai/2063383-intervyu-s-rezidentom-skolkovo-ispolzovanie-h200
- [T3] ChartMogul churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T4] 04-economics этого кейса, включая CAC, FOT, churn, hiring, ARPU, funnel assumptions: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-operator-kontrolya-kommunikacii/04-economics.md
- [T5] Gong official: https://www.gong.io/
- [T6] Observe.AI official: https://www.observe.ai/
- [T7] CallMiner official: https://callminer.com/
- [T8] MANGO OFFICE speech analytics: https://www.mango-office.ru/products/virtualnaya_ats/vozmozhnosti/speech-analytics/
- [T9] BSS speech analytics: https://bssys.com/solutions/rechevaya-analitika/
- [T10] Roistat speech analytics: https://roistat.com/ru/features/speech-analytics

<!-- P6B-DONE -->


---

## Файл: 06-verdict.md

[B2B-OPS] AI-оператор контроля коммуникаций — APPROVED WITH NOTES: 72/100 | EBITDA base=623К₽/мес через 12 мес | LTV/CAC=13,2x | Ключевое преимущество: локальный compliance-by-design и 100% контроль звонков/чатов | Главный риск: price compression и bundling со стороны incumbent-платформ.

# AI-оператор контроля коммуникаций — 06-verdict
sector: B2B-OPS
status: APPROVED WITH NOTES
score: 72/100
date: 2026-04-25
slug: ai-operator-kontrolya-kommunikacii

## Итог
**Вердикт инвесткомитета: APPROVED WITH NOTES.**

Кейс проходит approval gate, потому что одновременно выполняются два условия:
1. **Normalized score = 72/100**, то есть выше порога 70.
2. **company_ebitda_potential_rub_month = 623 500 ₽/мес** достигается в base-сценарии при **47 клиентах**, то есть **<50 клиентов** и **за 12 месяцев**, что проходит обязательный profitability gate.

Это не SMB add-on и не commodity speech-to-text слой. Инвестиционный тезис работает только как upper-mid / enterprise B2B-OPS платформа для контроля 100% коммуникаций, coaching, missed-revenue recovery и QA automation с локальным хранением данных.

## Этапы 1-5
### Этап 1 — Intake
Исходный тезис: AI-first оператор контроля клиентских коммуникаций, который автоматически разбирает 100% звонков и чатов, выявляет ошибки операторов, причины обращений и триггеры потерь продаж без ручного QA-отдела.

### Этап 2 — Validation / Evidence
В текущем кейсе отдельный файл `02-validation.md` отсутствует. Функцию валидации фактически выполняют `01-evidence.md` и массив доказательств в `02-demand.md`:
- IMOT.IO включён в реестр отечественного ПО;
- у рынка уже есть публичные цены 49-75 тыс. ₽/мес и выше;
- заявлены клиенты enterprise-уровня, включая РЖД, «Газпром Нефть», Skillfactory и другие.

### Этап 3 — Demand
Спрос на exact category в поиске низкий, но бюджетная строка и buyer pain подтверждены:
- Naumen оценивает рынок диалогового ИИ РФ в 8 млрд ₽, а сегмент речевой аналитики в 1,5 млрд ₽;
- hh.ru показывает реальные вакансии на QA звонков и речевую аналитику;
- в РФ уже есть несколько монетизирующихся игроков, значит WTP существует.

### Этап 4 — Economics
Base economics проходят investment-grade порог:
- customer_ltv_rub = **8 194 444 ₽**
- CAC = **620 500 ₽**
- LTV/CAC = **13,2x**
- CAC payback = **3,4 мес по выручке / 4,2 мес по gross profit**
- Gross Margin = **81,9%**
- contribution_margin_rub_month = **147 500 ₽/мес**
- fixed_costs_rub_month = **6 309 000 ₽/мес**
- startup_capital_to_bep_rub = **36 000 000 ₽**

### Этап 5 — Critic / Finance Risk
Monte Carlo Lite подтверждает, что кейс не сломан, но distribution риска широкий:
- **p10 EBITDA @M24 = -363 000 ₽/мес**
- **p50 EBITDA @M24 = 13 325 000 ₽/мес**
- **p90 EBITDA @M24 = 43 592 000 ₽/мес**

Median-case проходит уверенно, но downside-хвост остаётся значимым. Поэтому approve даётся только с оговорками по pricing discipline, bundling risk и execution.

## Оценка
Source tier balance: T1=7, T2=12, T3=0, weighted=2.37. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 13,2x», «CAC Payback: 3,4 мес по MRR, или 4,2 мес по gross profit», «Contribution Margin: 81,9%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «для EBITDA 500 000 ₽/мес нужно 47 клиентов», «50 clients sanity = +1 066 000 ₽/мес», base ramp выходит в плюс к M12. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 17 | «российский рынок диалогового ИИ уже материален: 8 млрд ₽... сегмент речевой аналитики 1,5 млрд ₽», но exact-demand по запросу остаётся LOW и применён tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 15 | «локальное хранение данных, лучшее соответствие 152-ФЗ, проще интеграции с российской телефонией и CRM», но bundling incumbents ограничивает защиту. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | «p10 EBITDA < 0», «рост стоимости или деградация LLM/STT API», длинный pilot-heavy enterprise motion и дорогая команда создают заметный execution burden. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | Fully-loaded CAC **620 500 ₽** и payback **4,2 мес** укладываются в enterprise SaaS, а 10 named targets совпадают с уже подтверждёнными buyer-вертикалями. |

**Сумма raw:** 108/150  
**Normalized score = round((108 × 100) / 150) = 72/100**

## 7-factor moat framework
| Фактор | Балл (0-3) | Почему |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент добавляет отраслевые шаблоны и кейсы, но прямого network flywheel почти нет. |
| Switching costs | 2 | Интеграции с CRM, телефонией, шаблоны QA и обучение команды создают умеренную цену переключения. |
| Scale economies | 2 | Shared infra, inference и шаблоны удешевляются с ростом, хотя пилот и onboarding пока partly manual. |
| Proprietary data / model advantage | 1 | Собственный data advantage возможен, но в текущем evidence нет убедимого T1/T2 доказательства масштаба датасета. |
| Regulatory moat | 2 | Локальное хранение данных и реестр отечественного ПО усиливают позицию, но это пока moat категории, а не уникально company-exclusive. |
| Brand / distribution | 2 | Есть локальный бренд и enterprise references, но category dominance не доказано. |
| Embedded workflow | 3 | Продукт встроен прямо в sales/support/QA workflow и влияет на конверсию, качество и training loop. |

**Moat raw = 13/21**  
**Moat score = round((13 × 25) / 21) = 15/25**

Комментарий: moat умеренный, не weak moat по формальному порогу, но недостаточно сильный для чистого APPROVED без оговорок.

## Investment committee view
### Почему кейс прошёл
1. **Категория уже монетизируется в РФ**, а не существует только как пилотный concept.
2. **Unit economics сильная**, особенно по LTV/CAC, payback и gross margin.
3. **EBITDA 500k+ достижима** при 47 клиентах и в горизонте 12 месяцев.
4. **Локальный контур хранения и интеграций** даёт реальный wedge против западных и bundled игроков.

### Почему кейс не получил чистый APPROVED
1. Exact search-demand по категории слабый.
2. Monte Carlo p10 остаётся отрицательным.
3. Bundling risk со стороны MANGO, Roistat, BSS и IMOT ограничивает силу moat.

## Полный бизнес-процесс из 04-economics.md
| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | ICP-list building и enrichment | SDR | HH/2ГИС/контур баз, Excel, CRM | 25 мин/лид | 420 | частично автоматизировано |
| 2 | Холодный outreach: email, звонок, Telegram/WhatsApp, LinkedIn-аналоги | SDR | amoCRM/Bitrix24, телефония, sequencing | 35 мин/лид | 580 | частично автоматизировано |
| 3 | Qualification call | SDR | телефония, скрипт, CRM | 20 мин/MQL | 330 | частично автоматизировано |
| 4 | Discovery call по боли и процессу QA | AE | Zoom/Meet, CRM, demo deck | 60 мин/SQL | 1 950 | низкая |
| 5 | Product demo + ROI framing | AE + CEO | demo стенд, BI-калькулятор ROI | 75 мин | 3 400 | низкая |
| 6 | Техническая оценка интеграции | CTO/solutions | API docs, call storage, security checklist | 2,5 ч | 6 100 | низкая |
| 7 | Пилот 2-4 недели на части звонков/чатов | ML + backend + CSM | ingestion pipeline, STT, LLM prompts, dashboard | 18 ч | 27 500 | частично автоматизировано |
| 8 | Pilot review, согласование KPI и коммерции | AE + CEO | ROI report, proposal | 1,5 ч | 5 250 | низкая |
| 9 | Procurement / legal / security | AE + CEO + external legal | договор, DPA, ИБ-анкета | 6 ч | 14 800 | низкая |
| 10 | Invoice setup и оплата 1-го месяца | finance/admin | банк, ЭДО, CRM | 45 мин | 1 200 | частично автоматизировано |
| 11 | Onboarding production | CSM + backend | ETL, интеграции, шаблоны QA | 10 ч | 15 900 | частично автоматизировано |
| 12 | Monthly success review и upsell | CSM + AE | BI dashboard, QBR deck | 2 ч/мес | 4 200 | частично автоматизировано |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 8 194 444 ₽ |
| CAC | 620 500 ₽ |
| LTV/CAC | 13,2x |
| CAC Payback | 3,4 мес revenue / 4,2 мес gross profit |
| Gross Margin | 81,9% |
| contribution_margin_rub_month | 147 500 ₽/мес |
| fixed_costs_rub_month | 6 309 000 ₽/мес |
| Break-even clients | 43 |
| clients_to_500k_ebitda | 47 |
| clients_to_1m_ebitda | 50 |
| months_to_500k_ebitda | 12 |
| months_to_1m_ebitda | 12 |
| company_ebitda_rub_month base | 623 500 ₽/мес при 47 клиентах |
| company_ebitda_potential_rub_month | 1 066 000 ₽/мес при 50 клиентах |
| startup_capital_to_bep_rub | 36 000 000 ₽ |

## Команда
| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraise, key accounts | 845 000 |
| CTO / Tech Lead | architecture, security, roadmap delivery | 715 000 |
| Senior Backend #1 | ingestion, ETL, integrations | 585 000 |
| Senior Backend #2 | product backend, analytics API | 585 000 |
| ML Engineer | speech/NLP quality, prompt systems, scoring | 715 000 |
| DevOps | infra, CI/CD, observability | 455 000 |
| Frontend | dashboards, QA workspace | 390 000 |
| SDR | new pipeline generation | 208 000 |
| AE | closing, pilot conversion | 455 000 |
| Customer Success | onboarding, retention, upsell | 312 000 |
| Product / Implementation manager | rollout, customer workflows, checklist library | 364 000 |
| **Итого** |  | **5 629 000 ₽/мес** |

## GTM — 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Этажи | уже есть публичный кейс автоматизации контроля звонков с ИИ; боль контроля 100% звонков доказана | email decision-maker + follow-up по кейсу vc.ru | 180 000 ₽/мес |
| 2 | Самолет | крупный девелопер с большим входящим потоком лидов и call-heavy продажами | партнёрство с CRM/телефонией + direct email head of sales ops | 220 000 ₽/мес |
| 3 | VOXYS | на hh.ru ищет специалиста контроля качества звонков и чатов, значит ручной QA уже дорогой | direct outreach операционному директору + конференция contact center | 250 000 ₽/мес |
| 4 | ОТП Банк | на hh.ru есть вакансия по речевой аналитике; regulated buyer с высокой ценой ошибок операторов | email decision-maker + warm intro через integrator/compliance vendors | 240 000 ₽/мес |
| 5 | Skillfactory | фигурирует среди клиентов IMOT.IO; edtech с сильным входящим sales motion и high-call admissions | founder-led outreach + кейс на vc.ru/Habr | 150 000 ₽/мес |
| 6 | РЖД | заявленный enterprise reference в категории, распределённые колл- и сервисные контуры | партнёрство + procurement intro | 300 000 ₽/мес |
| 7 | Газпром нефть | заявленный enterprise buyer; критичны quality control и compliance в сервисных коммуникациях | enterprise partner channel + direct outreach | 280 000 ₽/мес |
| 8 | Ингосстрах | страхование script-heavy, high-call и high-compliance сегмент с прямой болью QA | конференция + email руководителю контакт-центра | 220 000 ₽/мес |
| 9 | Авторитэйл | на hh.ru есть вакансия менеджера по качеству с прослушиванием звонков; auto-retail pain уже подтверждена | email decision-maker + отраслевой ивент | 140 000 ₽/мес |
| 10 | СберЗдоровье | call-heavy медицина с чувствительностью к качеству коммуникаций, скриптам и missed appointments | direct outreach + партнёрство с медицинскими CRM/телефонией | 200 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Price compression и bundling у incumbents | high | high | Самая опасная переменная по sensitivity analysis: «Price -30%» ведёт EBITDA @M12 к **-2 217 835 ₽/мес**. |
| Рост стоимости или деградация LLM/STT и санкционная зависимость | high | high | COGS и качество сервиса опираются на speech/NLP stack; supplier shock быстро ухудшит margin. |
| Pilot-heavy GTM и длинный enterprise sales cycle | medium-high | high | technical fit, pilot, legal/security и procurement делают CAC и time-to-cash чувствительными к execution slippage. |

## Proof points для APPROVED
1. **Есть локальная category validation:** IMOT.IO продаёт тарифы **49 000-75 000 ₽/мес** и enterprise-пакеты выше.
2. **Есть локальный regulatory fit:** IMOT.IO включён в реестр отечественного ПО.
3. **Есть реальный enterprise buyer universe:** hh.ru и публичные кейсы подтверждают недвижимость, банки, BPO, edtech и медицину как рабочие вертикали.
4. **Есть strong unit economics:** LTV/CAC **13,2x**, payback **4,2 мес**, contribution margin **81,9%**.
5. **Есть путь к EBITDA gate:** **47 клиентов → 623 500 ₽/мес**, **50 клиентов → 1 066 000 ₽/мес**.

## Что доказать в ближайшие 6 месяцев
1. Pilot-to-paid conversion не ниже **25-30%** на enterprise и upper-mid сегменте.
2. Blended ARPA не ниже **150 000-180 000 ₽/мес** без системного скидочного давления.
3. Не менее 2-3 repeatable vertical playbooks с go-live **<45 дней**.
4. Vendor redundancy по STT/LLM, чтобы снизить санкционный и COGS risk.

## LTV Upside Calculator
Кейс одобрен, поэтому отдельный reject-style upside calculator не обязателен. Для контроля upside держим три главных рычага:
- ARPA 180k → 220k ₽/мес добавляет ~32,8k ₽ gross profit на клиента в месяц;
- churn 1,8% → 1,4% поднимает customer_ltv_rub с ~8,19 млн ₽ до ~10,54 млн ₽;
- CAC 620,5k → 500k ₽ улучшает LTV/CAC с 13,2x до ~16,4x.

## Финальный комитетский вывод
**APPROVED WITH NOTES.**

Это инвестиционно пригодный B2B-OPS кейс для фонда, который готов работать с enterprise GTM, локальным compliance/data residency и длинным sales cycle. Не подходит для стратегии «дешёвый SMB SaaS». Подходит как premium workflow layer над существующим sales/support QA budget.

