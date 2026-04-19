# 02-demand — Demand Validation

## Кейс
Ambient Clinical Documentation Operator, AI-ассистент для ambient clinical documentation, автогенерации медзаписей и post-visit summary для клиник и hospital-grade контуров.

## Итог
**Статус: REJECTED**

Рынок в США уже валидирован платящими продуктами, но именно **в РФ на 19 апреля 2026 года** открытые сигналы спроса слабые: multi-demand по базовым запросам даёт **LOW**, hh.ru по релевантным запросам даёт **0**, заметного Telegram-first сегмента в России не видно. При этом путь к **EBITDA ≥ 500 000 ₽/мес** требует слишком большого числа платящих врачей или клиник для категории с длинным циклом внедрения, медицинскими рисками и интеграцией в МИС/ЭМК.

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand`

- `ambient clinical documentation` → **LOW**, demand score **0**, Google Trends RU **0**, Habr **2**, hh.ru **0**, Yandex suggest **2**
- `AI medical scribe` → **LOW**, demand score **0**, Google Trends RU **0**, Habr **2**, hh.ru **0**, Yandex suggest **2**
- `clinical documentation AI` → **LOW**, demand score **0**, Google Trends RU **0**, Habr **2**, hh.ru **0**, Yandex suggest **2**
- `voice to medical note` → **LOW**, demand score **0**, Google Trends RU **1**, Habr **2**, hh.ru **0**, Yandex suggest **2**

### Интерпретация
- Для российского контура это пока не search-led категория, а очень узкий enterprise workflow. [T1]
- В отличие от США, в РФ нет видимого слоя вакансий, поискового спроса и Telegram-native дистрибуции именно под medical scribe / ambient documentation. [T1][T2]
- Следовательно, продукту пришлось бы одновременно создавать категорию, проходить ИБ/медкомплаенс и интегрироваться в клинический контур. Это резко повышает go-to-market cost. [T2]

## 2. Реальные конкуренты и цены

| Конкурент | Что продаёт | Публичная цена | Источник | Вывод |
|---|---|---:|---|---|
| Freed | AI medical scribe для clinician workflow | **от $39/мес** ≈ **2 966 ₽/мес** по курсу ЦБ 76,0535 ₽/$ | getfreed.ai pricing [T2], ЦБ РФ [T1] | Есть нижняя ценовая точка self-serve, но это не hospital-grade внедрение |
| Scribeberry | AI medical scribe / notes / enterprise | **$99/мес** Pro, enterprise **от $79/user/мес** ≈ **7 529 ₽/мес** и **6 008 ₽/user/мес** | scribeberry.com pricing [T2], ЦБ РФ [T1] | Подтверждает готовность платить за physician-seat модель |
| Sunoh.ai | AI medical scribe | **$149/user/мес** ≈ **11 333 ₽/user/мес** | sunoh.ai pricing [T2], ЦБ РФ [T1] | Верхняя часть референсного диапазона для платного scribe |
| Heidi Health | Freemium ambient scribe + paid evidence/scribe plans | Бесплатный entry + платные clinician/team tiers, цена публично не раскрыта в extract | heidihealth.com pricing [T2] | Видно давление freemium-модели на ARPU |

### Вывод по конкурентному полю
- Конкуренты реальны, продуктовая категория глобально существует, а значит **WTP как класс подтверждён**, но прежде всего на англоязычном рынке. [T2]
- Публичные цены лежат примерно в диапазоне **3–11 тыс. ₽ за врача в месяц** по self-serve моделям. [T1][T2]
- Для РФ это плохая новость для экономики hospital-grade продукта: локальная команда должна поддерживать speech, медшаблоны, МИС-интеграции и комплаенс, а мировой price anchor при этом довольно низкий. [T2]

## 3. Telegram-боты и сервисы в РФ

### Что проверено
- Поиск по RU-вебу и Telegram-упоминаниям не показывает заметного **специализированного** Telegram-first продукта именно для ambient clinical documentation в российском healthcare-контуре. [T2]
- В РФ есть generic speech-to-text и voice-note инструменты, но не видно открытого лидера, который уже продаёт врачам потоковую клиническую документацию через Telegram как отдельную категорию. [T2][T3]

### Вывод по Telegram
- Telegram в РФ не подтверждает самостоятельный канал спроса для этого кейса. [T2]
- Отсутствие сильного Telegram-конкурента здесь не плюс, а скорее индикатор того, что сама категория ещё не сформирована локально. [T2]

## 4. WTP, доказательства готовности платить

### Что подтверждено
1. **Freed, Scribeberry, Sunoh.ai** продают подписку на medical scribe публично, значит врачи и клиники в развитых рынках уже платят за ускорение документации. [T2]
2. В России сама боль документационной нагрузки реальна: Росстат фиксирует **758,8 тыс. врачей** в РФ, то есть база пользователей большая, а административная нагрузка в медицине структурно существует. [T1]
3. Но именно **готовность российского рынка платить за ambient-scribe как отдельный software layer** в открытых источниках подтверждена слабо. [T2]

### Оценка WTP
**WTP = частично подтверждён, но в основном на зарубежных comparables.** Для РФ это пока не сильное локальное доказательство, а перенос международного паттерна. [T2]

## 5. Market sizing

### Метод и допущения
Курс для пересчёта: **1 USD = 76,0535 ₽** по XML_daily Банка России на дату проверки. [T1]

Средний референсный чек по международным comparable:
- Freed $39/мес,
- Scribeberry Pro $99/мес,
- Sunoh $149/user/мес.

Консервативный blended reference = **$96/мес** или **≈ 87 610 ₽/год за врача**. [T1][T2]

Для top-down беру только узкий адресуемый слой: врачи в амбулаторном и частно-клиническом контуре, где есть повторяющиеся консультации и экономический смысл автогенерации note. Для bottom-up беру крупные и средние частные сети/многопрофильные клиники как первые реалистичные покупатели. [T2][T3]

### 10 реальных buyers для bottom-up / GTM
1. МЕДСИ [T2]
2. Мать и дитя / MD Medical Group [T1]
3. EMC [T1]
4. СМ-Клиника [T2]
5. Медскан [T2]
6. Будь Здоров [T2]
7. Поликлиника.ру [T2]
8. АВА-Петер / Скандинавия [T2]
9. Медси Premium / SmartMed-контур МТС Медиацина substitute [T2]
10. МедСвисс [T2]

### Top-down
- База врачей в РФ: **758 800** человек. [T1]
- Addressable share для узкого initial use-case: **35%** врачей, в первую очередь амбулаторный и частный контур с высокой долей текстовой документации. Это **265 580** seat-equivalent. [T1][T2]
- **TAM РФ = 265 580 × 87 610 ₽ ≈ 23,27 млрд ₽/год**. [T1][T2]
- Для более узкого коммерчески достижимого сегмента беру **25% от TAM РФ** как клиники и сети, где реально возможна закупка отдельного digital workflow в горизонте 3 лет. **SAM top-down ≈ 5,82 млрд ₽/год**. [T2][T3]
- **SOM Y1 = 2% SAM ≈ 116,3 млн ₽/год**. [T2][T3]
- **SOM Y3 = 8% SAM ≈ 465,4 млн ₽/год**. [T2][T3]

### Bottom-up
- Целевой buyer universe для первых продаж: **250** частных сетей/крупных клиник и диагностических групп по РФ. [T2][T3]
- % with need: **60%**, так как в амбулаторной медицине documentation pain universal, но не везде можно внедрить voice AI. [T2]
- Средний контракт: **40 seat × 87 610 ₽/год = 3,50 млн ₽/год** на одну клинику/группу. [T1][T2]
- **SAM bottom-up = 250 × 60% × 3,50 млн ₽ ≈ 525,7 млн ₽/год**. [T2][T3]
- **SOM Y1 bottom-up = 5% ≈ 26,3 млн ₽/год**. [T2][T3]
- **SOM Y3 bottom-up = 15% ≈ 78,9 млн ₽/год**. [T2][T3]

### Reconciliation
Top-down сильно выше bottom-up, потому что seat-based верхняя оценка захватывает весь адресуемый клинический контур, а bottom-up считает только реально доступные для продаж частные сети в РФ. Для fund-level решения беру **lower bound**, то есть bottom-up, потому что он лучше отражает фактический GTM-радиус. Расхождение по SAM около **11,1x**, это red flag и означает, что реальный доступный рынок существенно уже теоретического. [LOW CONFIDENCE]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$4,0–6,0 млрд** global ambient/documentation AI market proxy [T2][T3] | — | Использую только как внешний ориентир, не для инвестиционного решения по РФ | top-down range |
| TAM (РФ) | **23,27 млрд ₽** [T1][T2] | **0,88 млрд ₽** proxy при 250 buyers × 100% need [T2][T3] | diff ≈ 26x, потому что seat-TAM сильно шире реального buyer universe | **lower** |
| SAM (РФ) | **5,82 млрд ₽** [T2][T3] | **0,53 млрд ₽** [T2][T3] | diff ≈ 11,1x, фактически достижимый рынок гораздо уже | **lower** |
| SOM Y1 | **116,3 млн ₽** | **26,3 млн ₽** | diff ≈ 4,4x | **используем 26,3 млн ₽** |
| SOM Y3 | **465,4 млн ₽** | **78,9 млн ₽** | diff ≈ 5,9x | **используем 78,9 млн ₽** |

## 6. Profit Gate, проверка сценариев монетизации
Правило: нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

Для hospital-grade продукта в РФ беру консервативную структуру расходов:
- команда, внедрение, QA, медэкспертиза, sales, support, infra и комплаенс: **2,4 млн ₽/мес** fixed cost,
- целевая EBITDA: **500 000 ₽/мес**,
- значит нужен gross profit **2,9 млн ₽/мес**.

### Сценарий A. Self-serve physician seat
- Цена: **8 000 ₽/врач/мес**
- Gross margin: **72%**
- Валовая прибыль на seat: **5 760 ₽/мес**
- Нужно: **2 900 000 / 5 760 = 504 врача**

**Вердикт: FAIL**. Для локального рынка с LOW demand и нулевыми hh-сигналами 500+ платящих seat выглядит слишком тяжело. [T1][T2]

### Сценарий B. Clinic package
- Цена: **120 000 ₽/клиника/мес**
- Gross margin: **70%**
- Валовая прибыль на клиента: **84 000 ₽/мес**
- Нужно: **35 клиник**

**Вердикт: FAIL**. Для sales-cycle 6–9 месяцев и узкого buyer universe закрыть 35 клиник раньше, чем сгорит runway, малореалистично. [T2][T3]

### Сценарий C. Enterprise hospital / network
- Цена: **250 000 ₽/мес**
- Gross margin: **65%**
- Валовая прибыль на клиента: **162 500 ₽/мес**
- Нужно: **18 enterprise-клиентов**

**Вердикт: FAIL**. 18 hospital-grade внедрений в РФ для новой категории без локально доказанного спроса, с ИБ и интеграциями, выглядит не как стартовый SaaS, а как длинный consultative business. [T2]

### Sanity-check
Если использовать preferred SOM Y1 **26,3 млн ₽/год**, это всего **2,19 млн ₽ выручки в месяц** на весь первый год. Даже до gross profit этого недостаточно для достижения **500 000 ₽ EBITDA/мес** при зафиксированном cost base. Значит Profit Gate ломается на уровне market capacity уже в год 1. [T2][T3]

## 7. Общий вывод
- Search demand в РФ: **низкий** [T1]
- Локальные признаки category pull: **слабые** [T1][T2]
- Глобальные конкуренты и цены: **есть** [T1][T2]
- Telegram-first рынок в РФ: **не подтверждён** [T2]
- WTP: **подтверждён глобально, слабо подтверждён локально** [T2]
- Profit Gate: **FAIL** [T2][T3]

## 8. Решение для пайплайна
Так как выполняется правило **DEMAND = LOW** и одновременно **Profit Gate FAIL**, кейс нужно **отклонить немедленно**, записать verdict и перенести в `pipeline/rejected/`.

## Market Pulse
Market Pulse 19.04.2026: локальный рынок РФ для ambient clinical documentation находится на слишком ранней стадии, чтобы оправдать fund-level вход.

## Источники
- Банк России, XML_daily: https://www.cbr.ru/scripts/XML_daily.asp
- Rosstat, Russia and countries of the world 2024: https://rosstat.gov.ru/folder/210/document/13206
- Freed pricing: https://www.getfreed.ai/pricing
- Scribeberry pricing: https://scribeberry.com/pricing
- Sunoh pricing: https://sunoh.ai/pricing
- Heidi pricing: https://www.heidihealth.com/pricing
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=ambient%20clinical%20documentation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20medical%20scribe
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=clinical%20documentation%20AI
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=voice%20to%20medical%20note

Sources: T1=4, T2=8, T3=3. Primary evidence basis: T2.
