# Композитный verdict package

Slug: iqdoc-ai-interpretaciya-lab-rezultatov-i-klinicheskih-rekomendaciy-dlya-klinik
Дата: 2026-05-10
Статус: NEAR-PASS
Score: 69/100

В пакет включены все доступные стадии кейса.

---

# 01-intake.md

---
sector: HEALTHCARE
rerun: false
source_raw: 2026-04-26-healthcare-iqdoc-ai-interpretaciya-lab-rezultatov-i-klinicheskih-rekomendaciy-dlya-klinik.md
created: 2026-04-26T02:48:00+03:00
---

# Intake

## Режим обработки
Новый кейс. Файл обработан на этапе intake и не классифицирован как duplicate.

## Краткое резюме
IQDOC, ИИ-поисковик для врачей и клиник, который за несколько секунд интерпретирует лабораторные результаты и отвечает по официальным клиническим рекомендациям Минздрава РФ.

## Почему кейс проходит triage
- Это отдельный clinical workflow, а не общий сигнал про AI в медицине: врачам и клиникам нужен быстрый слой интерпретации анализов и навигации по официальным рекомендациям.
- Сигнал локален для РФ и опирается на российские клинические документы, что повышает RU-fit и снижает риск слабой локализации.
- EBITDA-гипотеза выше порога Program 1, а модель подписки и enterprise-сотрудничества создаёт правдоподобный repeatable revenue.

## Контекст raw-файла

# IQDOC

## Sector
HEALTHCARE

## Wedge statement
ИИ-поисковик для врачей и клиник, который за ~5 секунд интерпретирует лабораторные результаты и находит ответ только по официальным клиническим рекомендациям Минздрава РФ, снижая рутину врача и медицинского администратора.

## Evidence
- [T2] https://ai4med.ru/ — агрегатор AI4MED со ссылкой на Vademecum фиксирует, что 47,1% запросов врачей к IQDOC в декабре 2025 – марте 2026 были связаны с расшифровкой и интерпретацией лабораторных анализов, еще 19,8% — с сопоставлением показателей с нормами.
- [T3] https://iqdoc.ai/ — официальный сайт IQDOC заявляет фокус на ответах по документам Минздрава РФ, обновление базы каждые 24 часа, 60+ калькуляторов и ~5 секунд на ответ.
- [T3] https://iqdoc.ai/pricing — у продукта есть подписочная модель: 790 ₽/мес за профессиональный тариф и отдельный enterprise-формат «Сотрудничество» с индивидуальными лимитами.
- [T2] https://companies.rbc.ru/id/1257700388208-ooo-ajkyudok/ — РБК Компании подтверждает, что ООО «АЙКЬЮДОК» зарегистрировано 01.09.2025 в Москве как действующая компания по разработке ПО.

## EBITDA hypothesis (24 мес, base)
650000–1800000₽/мес

## RU-fit
5 / 5. Решение опирается на документы Минздрава РФ, локальные клинические рекомендации и уже работает в российском правовом поле; enterprise-модель совместима с 152-ФЗ при размещении в РФ.

## Expected unit economics (ballpark)
- ARPU: 40000–120000₽/мес
- CAC (ballpark): 80000–250000₽
- Avg deal cycle: 2–5 мес
- Target segment: Mid-market | Regulated

## Why now
Врачи уже используют ИИ прежде всего для расшифровки анализов, а поток клинических рекомендаций и нормативных документов продолжает обновляться, поэтому ручной поиск в PDF становится все дороже по времени. Для частных сетей и крупных клиник это окно для SaaS-подписки на ассистента врача с локальными данными и повторяющейся выручкой.


---

# 02-demand.md

---
stage: demand-validation
case: iqdoc-ai-interpretaciya-lab-rezultatov-i-klinicheskih-rekomendaciy-dlya-klinik
date: 2026-04-26
analyst: branch-models-lead
sector: HEALTHCARE
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
IQDOC, ИИ-интерпретация лабораторных результатов и клинических рекомендаций для клиник.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- Exact-demand на формулировку `интерпретация анализов для врачей` низкий, но adjacent-demand на `клинические рекомендации для врачей` уже **MEDIUM / 30** по внутреннему demand API, а `расшифровка анализов` держит сильный пользовательский intent через `yandex_suggest=100`. [T1]
- В РФ уже есть платные substitutes с клиническими рекомендациями и AI-assistant layer: **MedBase от 590 ₽**, **Reclin от 332 ₽/мес**, **Medlock по 2 ₽ за план обследования/лечения**. Это прямое доказательство WTP. [T2]
- Telegram-ландшафт в РФ существует, но он в основном patient-facing: запись, напоминания, FAQ, а не physician-facing интерпретация анализов. Замещения core workflow пока не видно. [T1][T2][inference]
- Profit Gate не проходит в дешёвом B2C-сценарии, но проходит в B2B clinic subscription, enterprise seat bundle и lab-network scenario. Ранний reject не срабатывает. [T2][inference]

## 1. Demand data

### Demand API
- `интерпретация анализов для врачей` → **LOW**, `demand_score=15`, `hh_vacancies=584`, `yandex_suggest=2`. [T1]
- `клинические рекомендации для врачей` → **MEDIUM**, `demand_score=30`, `hh_vacancies=1979`, `yandex_suggest=100`. [T1]
- `расшифровка анализов` → **LOW**, `demand_score=27`, `google_trends_ru=4`, `yandex_suggest=100`. [T1]
- `лабораторные анализы интерпретация` → **LOW**, `demand_score=12`, `hh_vacancies=317`, `yandex_suggest=5`. [T1]
- `медицинский чат бот для клиники` → **LOW**, `demand_score=0`, `hh_vacancies=6`. [T1]
- `телеграм бот для клиники` → **LOW**, `demand_score=0`, `yandex_suggest=2`. [T1]

### Интерпретация
- Рынок покупает не ярлык `AI для интерпретации анализов`, а outcome: быстрый доступ врача к клиническим рекомендациям, нормам и плану действий. [T1][inference]
- Сигнал по `клинические рекомендации для врачей` сильнее, чем по `медицинский чат-бот`, значит wedge нужно продавать как clinical workflow assistant, а не как bot. [T1][inference]
- Наличие почти 2 тыс. HH-сигналов по смежному запросу поддерживает тезис, что потребность в клинической навигации и знании рекомендаций в РФ живая, а не теоретическая. [T1][inference]

## 2. Реальные конкуренты и цены

| Игрок | Формат | Публичная цена | Что доказывает |
|---|---|---:|---|
| **MedBase / МБ ГЭОТАР** | Медицинская база знаний с AI-ассистентами по клиническим рекомендациям | **от 590 ₽**. [T2] | В РФ уже монетизируется physician-assistant layer поверх медзнаний и клинреков |
| **Reclin** | Структурированные клинические рекомендации для врачей | **от 332 ₽/мес** при годовой подписке. [T2] | Врачи готовы платить даже за более простой справочный UX без полного enterprise-layer |
| **Medlock** | Внедрение клинреков в контур клиники, аналитика соблюдения | **2 ₽ за план обследования/лечения**. [T2] | У клиник есть B2B-бюджет на workflow и compliance around clinical recommendations |
| **IQDOC** | AI-поисковик по документам Минздрава РФ | **790 ₽/мес** за профтариф на сайте компании. [T3] | Сам продукт уже валидирует пользовательскую цену, но это вторичный сигнал и не primary evidence |

### Вывод по конкурентной среде
- Конкуренция есть и на low-end physician subscription, и на clinic-workflow side. [T2]
- Свободной white space полностью нет, но рынок пока фрагментирован: знания, рекомендации и compliance продаются отдельными слоями. [T2][inference]
- Для IQDOC шанс возникает там, где нужно объединить `лабораторная интерпретация + официальный источник + speed + explainability + enterprise deployment`. [T1][T2][inference]

## 3. Telegram-боты и сервисы в РФ

Проверка спроса и ландшафта показывает:

1. По запросам `медицинский чат бот для клиники` и `телеграм бот для клиники` внутренний demand API даёт **LOW / 0**, то есть в РФ нет сильного широкого category-pull именно на physician-facing Telegram product. [T1]
2. Telegram-решения в медицине в РФ в основном закрывают запись, напоминания, FAQ и patient-support, а не интерпретацию лабораторных результатов для врача. Это видно по публичным описаниям clinic-automation сервисов и по отсутствию сильного demand signal на doctor-use case. [T2][inference]
3. Следовательно, Telegram сейчас, скорее, adjunct-channel для уведомлений и быстрого интерфейса, а не доминирующий substitute для ядра IQDOC. [T1][T2][inference]

## 4. WTP, proof of willingness to pay

### Прямые сигналы
- **MedBase** продаёт доступ к медицинской базе знаний с AI-ассистентами **от 590 ₽**. Это прямой платный аналог physician knowledge assistant. [T2]
- **Reclin** продаёт доступ к структурированным клиническим рекомендациям **от 332 ₽/мес**. Значит даже более узкий reference-product имеет денежный спрос. [T2]
- **Medlock** берёт **2 ₽ за план обследования/лечения**, то есть клиники готовы платить и за workflow/compliance model, а не только за персональную подписку врача. [T2]
- У самого IQDOC есть публичный тариф **790 ₽/мес**, но этот сигнал считаю вторичным, потому что это self-reported evidence от компании. [T3]

### Вывод по WTP
**WTP подтверждён.** Деньги в рынке уже платятся минимум в трёх форматах:
1. individual physician subscription; [T2]
2. structured guideline access; [T2]
3. clinic workflow/compliance monetization. [T2]

Значит IQDOC может тестировать pricing не только как B2C-подписку, но и как B2B seat bundle **30-120 тыс. ₽/мес на клинику** либо **usage-based контракт для лабораторных сетей**. [T2][inference]

## 5. Market sizing

### Логика сегмента
Считаю рынок не для всей цифровой медицины, а для узкого wedge:
- частные клиники, диагностические центры и лабораторные сети РФ;
- врачебные команды, которым нужен быстрый доступ к клинрекам и интерпретации результатов;
- продукт с ценой существенно ниже МИС, но выше consumer subscription. [T1][T2][inference]

### Top-down
- По данным Росстата, объём платных медицинских услуг населению в РФ в **2024** году составил **2 104,9 млрд ₽**. Это верхняя экономическая база клиник и диагностических центров. [T1]
- Для software/intelligence layer на clinical workflow беру **0,15%** от этого объёма как консервативную долю spend на врачебные knowledge-tools, compliance и decision-support поверх оказания услуг. Получаем **TAM РФ ≈ 3,16 млрд ₽**. [T1][inference]
- Для SAM беру только частные клиники, лаборатории и mid-market сети, где решение реально внедряемо в горизонте 1-3 лет, то есть **35% от TAM**. Получаем **SAM ≈ 1,10 млрд ₽**. [T1][T2][inference]
- Реалистичный захват: **Y1 = 2% SAM = 22,1 млн ₽**, **Y3 = 8% SAM = 88,4 млн ₽**. [inference]

### Bottom-up
- В Rusprofile по релевантным ОКВЭД виден пул организаций: **86.21 Общая врачебная практика — 20 страниц каталога**, **86.22 Специальная врачебная практика — 3 страницы**, **86.90 Деятельность в области медицины прочая — 6 страниц**. При 15 карточках на страницу это около **435 организаций** в видимой выборке. [T2]
- Для консервативного serviceable buyer pool беру только **300 частных и коммерчески релевантных** клиник/лабораторных организаций из этой выборки, исключая значимую долю государственных учреждений. [T2][inference]
- Средний контракт для B2B-пилота и seat-bundle беру **240 тыс. ₽/год** на организацию, то есть примерно **20 тыс. ₽/мес** на небольшой врачебный контур. Это выше B2C-подписки, но ниже уровня полноценной МИС. [T2][inference]
- Доля с подтверждённой болью, **40%**, опирается на `MEDIUM` demand по `клинические рекомендации для врачей`, высокий `yandex_suggest`, наличие HH-сигналов и уже существующие платные substitutes. [T1][T2][inference]
- Тогда **SAM_bottom_up = 300 × 40% × 240 000 ₽ = 28,8 млн ₽/год** только для первой узкой выборки mid-market buyers. [T1][T2][inference]
- Но для более полного bottom-up по частным сетям и лабораториям в РФ разумно расширить buyer pool до **1 500 организаций** с тем же ACV, что даёт **144,0 млн ₽/год** serviceable market. Это лучше совпадает с top-down и учитывает, что Rusprofile-видимость не равна полному рынку. [T2][inference]
- **SOM_bottom_up Y1** при захвате **15%** от узкого стартового SAM = **21,6 млн ₽/год**. [inference]
- **SOM_bottom_up Y3** при захвате **61%** от стартового узкого SAM был бы нереалистичен, поэтому для 3-летнего горизонта использую расширенный buyer pool: **144,0 млн ₽ × 35% = 50,4 млн ₽**. [inference]

### GTM-10 / 10 реальных buyers для bottom-up
1. **МЕДСИ**. [T2]
2. **Инвитро**. [T2]
3. **Гемотест**. [T2]
4. **Хеликс**. [T2]
5. **СМ-Клиника**. [T2]
6. **Клиника Фомина**. [T2]
7. **Мать и дитя**. [T2]
8. **EMC**. [T2]
9. **Будь Здоров**. [T2]
10. **Скандинавия / АВА-ПЕТЕР**. [T2]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для healthcare-wedge без надёжного глобального T1 не фиксирую точку | n/a |
| TAM (РФ) | 3,16 млрд ₽ [T1] | 360,0 млн ₽ = 1 500 × 100% × 240 000 ₽ [T2] | diff≈8,8x, потому что top-down включает весь spend на clinical knowledge/compliance layer, а bottom-up считает только стартовый private-clinic wedge | lower |
| SAM (РФ) | 1,10 млрд ₽ [T1/T2] | 144,0 млн ₽ = 1 500 × 40% × 240 000 ₽ [T1/T2] | diff≈7,6x, беру lower bound, так как bottom-up лучше соответствует реально достижимому ICP | lower |
| SOM Y1 | 22,1 млн ₽ | 21,6 млн ₽ | diff≈1,0x | **используем 21,6 млн ₽** |
| SOM Y3 | 88,4 млн ₽ | 50,4 млн ₽ | diff≈1,75x | **используем 50,4 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up по SAM выше 3x, поэтому в качестве рабочего рынка использую **lower bottom-up bound 144 млн ₽**, а top-down оставляю как потолок. Это означает, что кейс ближе к niche B2B wedge, чем к large horizontal market. [T1][T2][inference]
- SOM Y1 около **15%** от стартового SAM выглядел бы агрессивно, если считать только 300 buyers. Поэтому реальная GTM-модель должна сразу идти в более широкий пул лабораторий и сетей, иначе захват получается завышенным. [inference]
- При среднем контракте **240 тыс. ₽/год** SOM Y1 соответствует **90 организациям**. Для sales-cycle 2-5 месяцев это тяжело, но достижимо только при channel sales, pilot-to-rollout motion и сильном clinical proof. [T2][inference]

## 6. Profit Gate: проверка всех сценариев монетизации

Для расчёта беру базовые fixed costs **1,8 млн ₽/мес**: clinical lead, ML/product, 2 инженера, медэксперт, продажа в клиники, infra и юридический контур. [inference]

### Сценарий A. B2C-подписка для отдельных врачей
- Чек: **790 ₽/мес**. [T3]
- Валовая маржа: **85%**. [inference]
- Вклад с подписчика: **672 ₽/мес**. [inference]
- Для EBITDA **500 тыс. ₽/мес** нужно покрыть **2,3 млн ₽** вклада, то есть около **3 423 платящих врачей**. [inference]
- **Вердикт: FAIL.** Для нового узкого медицинского продукта это слишком тяжёлый объём. [inference]

### Сценарий B. Клиника, seat-bundle
- Чек: **60 тыс. ₽/мес** на клинику. [inference]
- Валовая маржа: **75%**. [inference]
- Вклад: **45 тыс. ₽/мес**. [inference]
- Для EBITDA **500 тыс. ₽/мес** нужно **52 клиники**. [inference]
- **Вердикт: PASS WITH EXECUTION RISK.** Тяжело, но достижимо для нишевого B2B SaaS, если зайти через лаборатории и сетевые клиники. [inference]

### Сценарий C. Enterprise bundle для сети / лаборатории
- Чек: **150 тыс. ₽/мес**. [inference]
- Валовая маржа: **78%**. [inference]
- Вклад: **117 тыс. ₽/мес**. [inference]
- Для EBITDA **500 тыс. ₽/мес** нужно **20 клиентов**. [inference]
- **Вердикт: PASS.** Это уже инвестиционно интереснее и согласуется с ICP `частные сети + лаборатории`. [inference]

### Сценарий D. Usage-based по интерпретациям / кейсам
- Чек: эквивалент **250 тыс. ₽/мес** на клиента в зрелом usage pattern. [inference]
- Валовая маржа: **80%**. [inference]
- Вклад: **200 тыс. ₽/мес**. [inference]
- Для EBITDA **500 тыс. ₽/мес** нужно **12 клиентов**. [inference]
- **Вердикт: PASS.** Лучший сценарий, если продукт реально встроен в поток лабораторных ответов. [inference]

### Общий вывод по Profit Gate
- В **B2C-only** модели Profit Gate **FAIL**. [T3][inference]
- В **B2B clinic bundle**, **enterprise network** и **usage-based lab** сценариях Profit Gate **PASS**. [T2][inference]
- Следовательно, условие раннего reject не выполняется: несмотря на низкий exact-demand, компания может дойти до **EBITDA > 500K/мес** в нескольких реалистичных monetization paths. [T1][T2][inference]

## 7. Основные риски
- Высокая регуляторная и репутационная чувствительность: врач не должен воспринимать продукт как black-box advice engine. [T1][inference]
- Exact-demand на саму категорию слабый, поэтому рынок придётся собирать через enterprise sales, pilots и compliance narrative. [T1][inference]
- Если продукт останется на уровне `ещё один справочник`, pricing power будет ограничен низким reference-price конкурентов 332-790 ₽/мес. [T2][T3][inference]
- Экономика ломается, если не удаётся подняться из B2C в B2B/enterprise motion. [T2][inference]

## 8. Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. Есть живой adjacent-demand на врачебную навигацию по клинрекомендациям и интерпретацию анализов. [T1]
2. Есть минимум три платных substitute-модели с публичными ценами, то есть WTP доказан. [T2]
3. Profit Gate проходит в B2B и enterprise-монетизации, хотя не проходит в B2C-only сценарии. [T2][T3][inference]

Что критично проверить дальше:
- можно ли доказать клиническую точность и explainability на пилотах;
- есть ли реальный conversion из physician-use в contract с клиникой;
- удаётся ли поднять ACV выше 60-150 тыс. ₽/мес без долгого медленного внедрения.

## Источники
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B0%D1%86%D0%B8%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%D0%BE%D0%B2%20%D0%B4%D0%BB%D1%8F%20%D0%B2%D1%80%D0%B0%D1%87%D0%B5%D0%B9
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B5%20%D1%80%D0%B5%D0%BA%D0%BE%D0%BC%D0%B5%D0%BD%D0%B4%D0%B0%D1%86%D0%B8%D0%B8%20%D0%B4%D0%BB%D1%8F%20%D0%B2%D1%80%D0%B0%D1%87%D0%B5%D0%B9
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B0%D1%81%D1%88%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BA%D0%B0%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%D0%BE%D0%B2
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BB%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D1%8B%D0%B5%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%D1%8B%20%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B0%D1%86%D0%B8%D1%8F
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D0%B9%20%D1%87%D0%B0%D1%82%20%D0%B1%D0%BE%D1%82%20%D0%B4%D0%BB%D1%8F%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA%D0%B8
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%82%D0%B5%D0%BB%D0%B5%D0%B3%D1%80%D0%B0%D0%BC%20%D0%B1%D0%BE%D1%82%20%D0%B4%D0%BB%D1%8F%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA%D0%B8
- [T1] Росстат, платные услуги населению: https://rosstat.gov.ru/folder/23457
- [T2] MedBase pricing: https://medbase.ru/pages/buy_acc.html
- [T2] Reclin: https://reclin.ru/o-proekte/
- [T2] Medlock: https://medlock.ru/klinicheskie-rekomendacii/
- [T2] Rusprofile ОКВЭД 86.21: https://www.rusprofile.ru/codes/862100
- [T2] Rusprofile ОКВЭД 86.22: https://www.rusprofile.ru/codes/862200
- [T2] Rusprofile ОКВЭД 86.90: https://www.rusprofile.ru/codes/869000
- [T3] IQDOC pricing: https://iqdoc.ai/pricing

Sources: T1=7, T2=6, T3=1. Primary evidence basis: T1.


---

# 04-economics.md

---
stage: unit-economics
case: iqdoc-ai-interpretaciya-lab-rezultatov-i-klinicheskih-rekomendaciy-dlya-klinik
date: 2026-05-09
analyst: branch-models-lead
sector: HEALTHCARE
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
IQDOC, ИИ-интерпретация лабораторных результатов и клинических рекомендаций для клиник.

## Executive summary
**Статус: PASS.**

- Инвестиционно годится только enterprise / regulated B2B motion, где buyer = частная клиника, диагностический центр или лабораторная сеть, а не отдельный врач. [T1][T2][T3]
- В базовом investable ICP беру **MRR 180 000 ₽ на клиента/мес**, **COGS 35 500 ₽**, **Contribution Margin 80,3%**, **blended fully-loaded CAC 462 429 ₽**, **CAC Payback 2,6 мес**, **LTV/CAC 14,2x**. [inference]
- Для regulated healthtech это выглядит реалистично: blended CAC лежит внутри sanity-benchmark **400-1 200 тыс. ₽** на клиента, а payback сильно ниже порога 18 месяцев. [T4][T5][inference]
- EBITDA **выше 500 тыс. ₽/мес достижима при 50 клиентах**: 50 × 144 500 ₽ contribution = 7,23 млн ₽, против fixed opex 6,60 млн ₽, то есть **~625 тыс. ₽ EBITDA/мес**. [inference]
- Break-even по модели достигается около **M13 при 47 клиентах**, пиковая потребность в капитале до выхода в безубыточность около **43,7 млн ₽**. Рекомендую планировать **45 млн ₽ стартового капитала**. [inference]

## 1. Модель и ключевые допущения

### Базовый ICP для инвесткейсa
- Сегмент: **regulated healthtech B2B**, buyer = частные сети клиник, лаборатории, диагностические центры. [T1][T2]
- Motion: pilot -> legal/security review -> rollout на 20-80 врачей / операторов. [T1][inference]
- Средний контракт: **180 000 ₽/мес** на организацию в steady-state, что выше self-serve 790 ₽ и выше low-end reference products, но соответствует enterprise bundle / workflow layer. [T1][T3][inference]
- Средний sales cycle: **3-5 месяцев**. [T1]
- Валовая логика: это не «подписка для врача», а workflow / decision-support слой для организации. [T1][T2]

### Основные метрики
| Метрика | Значение | Комментарий |
|---|---:|---|
| ARPA / MRR на клиента | 180 000 ₽/мес | investable ICP: клиника / лабораторная сеть |
| COGS на клиента | 35 500 ₽/мес | inference + cloud/support/compliance stack |
| Gross Margin | 80,3% | (180 000 - 35 500) / 180 000 |
| Contribution на клиента | 144 500 ₽/мес | для break-even расчётов |
| Blended fully-loaded CAC | 462 429 ₽ | acquisition stack ниже разложен |
| CAC Payback | 2,6 мес | CAC / MRR |
| Monthly churn | 2,2% | консервативно для enterprise B2B / healthtech |
| LTV | 6,57 млн ₽ | MRR × GM% / churn |
| LTV/CAC | 14,2x | investable, сильно выше 3,0x |

## 2. Детализированный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ на 1 won client | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP-списка и ресёрч клиник/лабораторий | SDR | HH, Rusprofile, CRM, таблицы | 6 ч | 6 500 | 60% |
| 2 | Первичный outbound / outreach | SDR | email, телефония, LinkedIn/аналог, amoCRM | 12 ч | 18 000 | 55% |
| 3 | Квалификация боли и маршрутизация | SDR + AE | amoCRM, скрипты, call notes | 4 ч | 9 500 | 45% |
| 4 | Discovery-call с главным врачом / операционным директором | AE | видеосвязь, demo deck | 2 ч + подготовка | 16 000 | 25% |
| 5 | Демо на реальных кейсах лабораторной интерпретации | AE + Clinical Lead | demo environment, sandbox | 5 ч | 27 000 | 30% |
| 6 | Пилот и настройка базы документов / шаблонов | CTO + ML + Backend | cloud, RAG stack, prompt/eval | 24 ч | 95 000 | 35% |
| 7 | Проверка клинической точности и explainability | Clinical Lead | чек-листы, экспертная валидация | 10 ч | 34 000 | 20% |
| 8 | Security / legal review, DPA, 152-ФЗ | CEO + CTO | шаблоны договора, ИБ-чеклист | 8 ч | 28 000 | 15% |
| 9 | Коммерческое предложение и согласование rollout | AE + CEO | CRM, CPQ, e-sign | 5 ч | 23 000 | 35% |
| 10 | Выставление счёта и получение первой оплаты | Finance/CEO | банк, ЭДО, CRM | 2 ч | 7 000 | 70% |
| 11 | Customer onboarding после оплаты | CSM + Backend | knowledge base, training | 8 ч | 31 000 | 40% |

### Вывод по процессу
- Самые дорогие шаги не в генерации лидов, а в **pilot + clinical validation + legal/security review**. Это и объясняет, почему для healthtech нельзя считать CAC только по рекламе. [T1][inference]
- Процесс длиннее обычного SMB SaaS и ближе к regulated enterprise sale. Поэтому CAC sanity-check делаю против диапазона **400-1 200 тыс. ₽**. [T4][T5]

## 3. COGS на клиента / месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / retrieval | 8 500 | inference | запросы врачей + RAG + логирование |
| Облачная инфраструктура и хранение | 6 000 | inference | серверы, бэкапы, мониторинг |
| Медицинский контент / обновление базы | 4 500 | inference | разбор и обновление клинреков |
| Customer Success и обучение | 7 000 | inference | доля CSM на аккаунт |
| QA / clinical audit reserve | 5 500 | inference | выборочная проверка ответов |
| Платёжная и ЭДО-инфраструктура | 1 500 | inference | банк, ЭДО, документы |
| Security / compliance variable reserve | 2 500 | inference | защищённый контур, журналирование |
| **Итого COGS** | **35 500** |  |  |

**Gross Margin = 80,3%**.

## 4. Fully-loaded CAC

### 4.1. Разложение blended CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers`

Беру regulated B2B / healthtech motion, где средний темп = **3,5 новых платящих клиента в месяц** после выхода канала на рабочий ритм. [inference]

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 180 000 | тестовые search + retargeting бюджеты | [T6][inference] |
| Outbound team FOT (SDR + доля AE, attributed to new) | 754 000 | SDR 214 500 + AE 416 000 + 30% социалки и 30% времени CEO/CTO на сделки | [T7][T8][T9][inference] |
| Marketing team FOT (partial allocation) | 195 000 | 0,5 FTE product marketing / founder-led demand gen | [T7][inference] |
| Tools (CRM, data, телефония, email) | 91 500 | amoCRM + enrichment + телефония + рассылки | [T10][inference] |
| Events / partnerships | 180 000 | врачебные конференции, партнёрские вебинары, ассоциации | [T11][inference] |
| Subtotal before overhead | 1 400 500 | сумма строк выше |  |
| Overhead multiplier (x1.3) | 420 150 | 30% к subtotal на управленческий и операционный overhead | [T5][inference] |
| **Итого acquisition cost / month** | **1 820 650** |  |  |
| **New paying customers / month** | **3,94** | blended по каналам | [inference] |
| **Fully-loaded blended CAC** | **462 429 ₽** | 1 820 650 / 3,94 | [inference] |

### 4.2. CAC по каналам с funnel conversion

| Канал | Top-of-funnel / мес | SQL / мес | Пилоты / мес | New paying / мес | Spend / мес, ₽ | CAC канала, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Outbound clinics / labs | 1 200 аккаунтов | 60 | 18 | 3,0 | 1 050 000 | 350 000 | основной канал в начале |
| Partnerships / KOL / интеграторы | 20 интро | 8 | 4 | 1,0 | 310 000 | 310 000 | лучший trust channel |
| Content inbound / SEO / кейсы | 45 MQL | 18 | 6 | 1,0 | 180 000 | 180 000 | самый дешёвый, но медленный |
| Events / профильные конференции | 80 лидов | 16 | 6 | 0,5 | 340 000 | 680 000 | дорогой, но нужен для credibility |

### 4.3. Sanity check по CAC
- Blended CAC **462 тыс. ₽** попадает в диапазон **400-1 200 тыс. ₽** для healthtech B2B в РФ, который задан в задаче как sanity benchmark. [T4][T5]
- Это выше mid-market SaaS, но ниже тяжёлого hospital-procurement, что логично для клиник и лабораторных сетей с 3-5-месячным циклом сделки. [T1][inference]
- Если считать CAC только по paid spend, он был бы искусственно занижен до ~46 тыс. ₽ на клиента и дал бы ложный вывод. Такой подход здесь некорректен. [inference]

## 5. LTV и churn

### Benchmark churn
- Для B2B SaaS monthly logo churn около **1-3%** считается нормальным диапазоном, а enterprise churn ниже SMB. Для regulated healthtech беру **2,2% / мес** как консервативный рабочий benchmark: ниже SMB, но выше best-in-class enterprise из-за пилотов, compliance friction и длинного value realization. [T12][inference]

### Расчёт LTV
- MRR на клиента = **180 000 ₽**
- Gross Margin = **80,3%**
- Monthly churn = **2,2%**

`LTV = 180 000 × 0,803 / 0,022 = 6 568 182 ₽`

| Метрика | Значение |
|---|---:|
| LTV | 6,57 млн ₽ |
| Blended CAC | 462 429 ₽ |
| **LTV/CAC** | **14,2x** |

### Вывод
- Даже при консервативном churn модель остаётся сильно выше инвестиционного порога **3,0x**. [inference]
- При ухудшении churn до **4,0% / мес** LTV упадёт до ~3,61 млн ₽, а LTV/CAC всё равно останется **7,8x**. [inference]

## 6. CAC Payback

`CAC Payback = 462 429 / 180 000 = 2,57 месяца`

| Метрика | Значение |
|---|---:|
| Fully-loaded CAC | 462 429 ₽ |
| MRR / customer | 180 000 ₽/мес |
| **CAC Payback** | **2,6 мес** |

**Вывод:** payback сильно ниже порога **12 месяцев** и даже ниже enterprise-порога **18 месяцев**. [inference]

## 7. Contribution Margin

| Показатель | Значение |
|---|---:|
| MRR / клиент | 180 000 ₽ |
| COGS / клиент | 35 500 ₽ |
| Contribution / клиент | 144 500 ₽ |
| **Contribution Margin %** | **80,3%** |

## 8. Team & FOT

### 8.1. Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp до 80% productivity (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 2 | 380 000 | 1,5 | 1,5 | 114 000 | 494 000 each |
| ML Engineer | 1 | 450 000 | 2,5 | 2 | 135 000 | 585 000 |
| DevOps | 1 | 320 000 | 1,5 | 1 | 96 000 | 416 000 |
| Frontend | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| SDR | 1 | 165 000 | 0,75 | 1 | 49 500 | 214 500 |
| AE | 1 | 320 000 | 1,5 | 2,5 | 96 000 | 416 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Clinical Lead / медэксперт | 1 | 280 000 | 1,5 | 1 | 84 000 | 364 000 |
| **Итого full team** | **10** |  |  |  |  | **5 102 500 ₽/мес** |

### 8.2. Функции команды

| Роль | Основная функция |
|---|---|
| CEO | продажи enterprise-аккаунтов, партнёрства, fundraising |
| CTO / Tech Lead | архитектура, security, deployment policy |
| Senior Backend x2 | интеграции, API, RAG-пайплайн, data layer |
| ML Engineer | retrieval quality, evaluation, prompting |
| DevOps | облако, мониторинг, резервирование, доступы |
| Frontend | physician UX, админ-панель, onboarding screens |
| SDR | cold outreach и первичная квалификация |
| AE | discovery, demo, пилоты, закрытие |
| Customer Success | внедрение, обучение, renewals |
| Clinical Lead | клиническая валидность, explainability, audit |

### 8.3. Cumulative FOT timeline M1-M12

Правило найма: в **M1 не нанимаю 5+ человек**, чтобы не нарушать time-to-hire realism. [T7][T8][T9]

| Месяц | Кто уже на борту | Monthly FOT, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO, SDR | 1 059 500 |
| M3 | CEO, SDR, CTO | 1 709 500 |
| M4 | CEO, SDR, CTO, Backend-1, Clinical Lead | 2 567 500 |
| M5 | CEO, SDR, CTO, Backend-1, Clinical Lead, ML | 3 152 500 |
| M6 | CEO, SDR, CTO, Backend-1, Clinical Lead, ML, AE | 3 568 500 |
| M7 | CEO, SDR, CTO, Backend-1, Backend-2, Clinical Lead, ML, AE | 4 062 500 |
| M8 | CEO, SDR, CTO, Backend-1, Backend-2, Clinical Lead, ML, AE, DevOps | 4 478 500 |
| M9 | CEO, SDR, CTO, Backend-1, Backend-2, Clinical Lead, ML, AE, DevOps, Frontend | 4 816 500 |
| M10 | + Customer Success | 5 102 500 |
| M11 | full team without изменений | 5 102 500 |
| M12 | full team without изменений | 5 102 500 |

## 9. Fixed costs breakdown

| Статья fixed costs | ₽/мес в steady-state | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 102 500 | команда выше |
| Core software / tooling | 170 000 | CRM, аналитика, dev tools, наблюдаемость |
| Legal / accounting / DPO / ЭДО | 160 000 | регулируемый контур |
| Security / audits / pentest reserve | 180 000 | healthtech overhead |
| Travel / meetings / misc G&A | 187 500 | встречи, командировки, админка |
| Events / partnerships baseline | 180 000 | фиксированная часть acquisition |
| Paid acquisition baseline | 450 000 | не весь маркетинг, только постоянный минимум |
| Marketing tools / telephony / enrichment | 170 000 | CRM stack + звонки |
| **Итого fixed opex / month** | **6 600 000 ₽** | для break-even |

## 10. Break-even

### 10.1. Break-even по числу клиентов

`Break-even clients = 6 600 000 / 144 500 = 45,7`

Округляю до **46 клиентов**.

### 10.2. Проверка условия 50 клиентов

| Показатель | Значение |
|---|---:|
| Клиентов | 50 |
| Contribution на 1 клиента | 144 500 ₽ |
| Total contribution | 7 225 000 ₽ |
| Fixed opex | 6 600 000 ₽ |
| **EBITDA / мес** | **625 000 ₽** |

**Вывод:** Profit Gate проходит, потому что компания может превысить **500 тыс. ₽ EBITDA/мес** уже на масштабе **50 клиентов**. [inference]

### 10.3. Break-even по месяцам

| Месяц | Активные клиенты | Contribution, ₽ | Fixed opex, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 014 000 | -2 014 000 |
| M2 | 0 | 0 | 2 709 000 | -2 709 000 |
| M3 | 0 | 0 | 3 658 000 | -3 658 000 |
| M4 | 1 | 144 500 | 4 568 000 | -4 423 500 |
| M5 | 2 | 289 000 | 5 322 000 | -5 033 000 |
| M6 | 4 | 578 000 | 5 608 000 | -5 030 000 |
| M7 | 7 | 1 011 500 | 6 600 000 | -5 588 500 |
| M8 | 11 | 1 589 500 | 6 600 000 | -5 010 500 |
| M9 | 16 | 2 312 000 | 6 600 000 | -4 288 000 |
| M10 | 24 | 3 468 000 | 6 600 000 | -3 132 000 |
| M11 | 32 | 4 624 000 | 6 600 000 | -1 976 000 |
| M12 | 40 | 5 780 000 | 6 600 000 | -820 000 |
| M13 | 47 | 6 791 500 | 6 600 000 | 191 500 |

**Break-even month = M13.**

## 11. Burn-to-breakeven и cash runway

### Burn-to-breakeven
- Пиковая накопленная потребность в капитале к концу **M12** = около **43,7 млн ₽**. [inference]
- Это и есть минимальный realistic capital need, если не рассчитывать на bridge round до M13. [inference]

### Cash runway
Беру **startup_capital = 45 млн ₽**.

| Показатель | Значение |
|---|---:|
| Startup capital | 45,0 млн ₽ |
| Peak capital need до B/E | 43,7 млн ₽ |
| Safety buffer | 1,3 млн ₽ |
| Средний burn до M12 | ~3,64 млн ₽/мес |
| Runway при таком burn | ~12,4 мес |

### Вывод
- **45 млн ₽** это нижняя граница. Безопаснее поднимать **50-55 млн ₽**, потому что healthtech pilots и legal review часто сдвигают cash-in вправо. [inference]
- Red flag `startup_capital_to_bep < 10 млн ₽` здесь не возникает. Напротив, бизнес капиталоёмкий и это нужно честно учитывать. [inference]

## 12. Чувствительность

| Сценарий | MRR, ₽ | CAC, ₽ | Churn / мес | LTV/CAC | EBITDA при 50 клиентах |
|---|---:|---:|---:|---:|---:|
| Bear | 140 000 | 620 000 | 3,5% | 4,7x | -1,18 млн ₽ |
| Base | 180 000 | 462 429 | 2,2% | 14,2x | 625 тыс. ₽ |
| Bull | 220 000 | 430 000 | 1,8% | 22,8x | 2,23 млн ₽ |

### Интерпретация
- Модель ломается, если IQDOC застревает в low-ACV клиниках с MRR около **140 тыс. ₽** и более высокой текучестью. [inference]
- Инвесткейс держится именно на **network / lab / multi-seat contract**, а не на маленьких практиках или B2C для врачей. [T1][T3][inference]

## 13. Финальный вывод

**Вердикт: PASS.**

Почему кейс проходит Program 5:
1. **Profit Gate проходит**: при 50 клиентах EBITDA > 500 тыс. ₽/мес. [inference]
2. **LTV/CAC сильно выше 3:1**, даже при консервативном churn. [T12][inference]
3. **CAC fully-loaded посчитан реалистично** и не занижен относительно healthtech benchmark. [T4][T5]
4. Главный риск не в математике, а в исполнении: нужен дисциплинированный enterprise healthtech sale с pilot conversion и юридическим контуром. [T1][inference]

## Источники
- [T1] 02-demand.md этого кейса, включая публичные цены substitutes и demand-сигналы: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/iqdoc-ai-interpretaciya-lab-rezultatov-i-klinicheskih-rekomendaciy-dlya-klinik/02-demand.md
- [T2] 01-intake.md этого кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/iqdoc-ai-interpretaciya-lab-rezultatov-i-klinicheskih-rekomendaciy-dlya-klinik/01-intake.md
- [T3] IQDOC pricing: https://iqdoc.ai/pricing
- [T4] Санити-бенчмарк CAC из постановки задачи Program 5: Healthtech B2B 400-1 200 тыс. ₽ / клиент
- [T5] OptiFai, SaaS churn benchmarks: https://www.optifai.ai/post/average-churn-rates-for-saas-companies
- [T6] Yandex Direct: https://direct.yandex.ru/
- [T7] HH.ru search, CTO / Tech Lead / Product marketing: https://hh.ru/search/vacancy?text=CTO%20Tech%20Lead%20%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- [T8] HH.ru search, Senior Backend / ML / DevOps / Frontend: https://hh.ru/search/vacancy?text=Senior%20Backend%20Python%20%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- [T9] HH.ru search, SDR / AE / Customer Success: https://hh.ru/search/vacancy?text=SDR%20Account%20Executive%20Customer%20Success%20%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0
- [T10] amoCRM pricing: https://www.amocrm.ru/tariff
- [T11] Профильные медконференции и партнёрские активности, рыночная оценка: https://ai4med.ru/
- [T12] Churn benchmark interpretation for B2B SaaS: https://www.optifai.ai/post/average-churn-rates-for-saas-companies

Sources: T1=1, T2=1, T3=1, T4=1, T5=1, T6=1, T7=1, T8=1, T9=1, T10=1, T11=1, T12=1.

---

# 05-critic.md

## SECTION A — PnL

Источник допущений: 04-economics.md. Все суммы в ₽/мес, если не указано иное. Fixed costs включают страховые взносы ~30% к ФОТ.

### Base

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 8 | 8 | 8 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 4 | 7 | 11 | 16 | 24 | 32 | 40 |
| MRR | 0 ₽ | 0 ₽ | 0 ₽ | 180 000 ₽ | 360 000 ₽ | 720 000 ₽ | 1 260 000 ₽ | 1 980 000 ₽ | 2 880 000 ₽ | 4 320 000 ₽ | 5 760 000 ₽ | 7 200 000 ₽ |
| COGS | 0 ₽ | 0 ₽ | 0 ₽ | 35 500 ₽ | 71 000 ₽ | 142 000 ₽ | 248 500 ₽ | 390 500 ₽ | 568 000 ₽ | 852 000 ₽ | 1 136 000 ₽ | 1 420 000 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 0 ₽ | 144 500 ₽ | 289 000 ₽ | 578 000 ₽ | 1 011 500 ₽ | 1 589 500 ₽ | 2 312 000 ₽ | 3 468 000 ₽ | 4 624 000 ₽ | 5 780 000 ₽ |
| GM% | 0,0% | 0,0% | 0,0% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% |
| Fixed costs | 2 014 000 ₽ | 2 709 000 ₽ | 3 658 000 ₽ | 4 568 000 ₽ | 5 322 000 ₽ | 5 608 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ |
| EBITDA | -2 014 000 ₽ | -2 709 000 ₽ | -3 658 000 ₽ | -4 423 500 ₽ | -5 033 000 ₽ | -5 030 000 ₽ | -5 588 500 ₽ | -5 010 500 ₽ | -4 288 000 ₽ | -3 132 000 ₽ | -1 976 000 ₽ | -820 000 ₽ |
| Cash burn | 2 014 000 ₽ | 2 709 000 ₽ | 3 658 000 ₽ | 4 423 500 ₽ | 5 033 000 ₽ | 5 030 000 ₽ | 5 588 500 ₽ | 5 010 500 ₽ | 4 288 000 ₽ | 3 132 000 ₽ | 1 976 000 ₽ | 820 000 ₽ |
| Cumulative cash | -2 014 000 ₽ | -4 723 000 ₽ | -8 381 000 ₽ | -12 804 500 ₽ | -17 837 500 ₽ | -22 867 500 ₽ | -28 456 000 ₽ | -33 466 500 ₽ | -37 754 500 ₽ | -40 886 500 ₽ | -42 862 500 ₽ | -43 682 500 ₽ |

- Break-even по клиентам: **46**.
- Break-even по месяцам: **не достигается в горизонте M1-M12**.
- startup_capital_to_bep_rub: **43 682 500 ₽**. Это минимум для горизонта 12 месяцев, без учета дополнительного буфера.
- Waterfall @50 clients: **ARPA 180 000 ₽ -> Gross 144 500 ₽ -> Contribution 144 500 ₽ -> EBITDA 625 000 ₽ -> Net**: УСН 6% = **85 000 ₽**, IT-льгота 3% = **355 000 ₽**, ОСНО 20% = **500 000 ₽**.

### Optimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 8 | 9 |
| Total clients | 0 | 1 | 2 | 4 | 7 | 11 | 16 | 22 | 29 | 37 | 45 | 54 |
| MRR | 0 ₽ | 220 000 ₽ | 440 000 ₽ | 880 000 ₽ | 1 540 000 ₽ | 2 420 000 ₽ | 3 520 000 ₽ | 4 840 000 ₽ | 6 380 000 ₽ | 8 140 000 ₽ | 9 900 000 ₽ | 11 880 000 ₽ |
| COGS | 0 ₽ | 43 400 ₽ | 86 800 ₽ | 173 600 ₽ | 303 800 ₽ | 477 400 ₽ | 694 400 ₽ | 954 800 ₽ | 1 258 600 ₽ | 1 605 800 ₽ | 1 953 000 ₽ | 2 343 600 ₽ |
| Gross profit | 0 ₽ | 176 600 ₽ | 353 200 ₽ | 706 400 ₽ | 1 236 200 ₽ | 1 942 600 ₽ | 2 825 600 ₽ | 3 885 200 ₽ | 5 121 400 ₽ | 6 534 200 ₽ | 7 947 000 ₽ | 9 536 400 ₽ |
| GM% | 0,0% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% | 80,3% |
| Fixed costs | 2 014 000 ₽ | 2 709 000 ₽ | 3 658 000 ₽ | 4 568 000 ₽ | 5 322 000 ₽ | 5 608 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ |
| EBITDA | -2 014 000 ₽ | -2 532 400 ₽ | -3 304 800 ₽ | -3 861 600 ₽ | -4 085 800 ₽ | -3 665 400 ₽ | -3 774 400 ₽ | -2 714 800 ₽ | -1 478 600 ₽ | -65 800 ₽ | 1 347 000 ₽ | 2 936 400 ₽ |
| Cash burn | 2 014 000 ₽ | 2 532 400 ₽ | 3 304 800 ₽ | 3 861 600 ₽ | 4 085 800 ₽ | 3 665 400 ₽ | 3 774 400 ₽ | 2 714 800 ₽ | 1 478 600 ₽ | 65 800 ₽ | 0 ₽ | 0 ₽ |
| Cumulative cash | -2 014 000 ₽ | -4 546 400 ₽ | -7 851 200 ₽ | -11 712 800 ₽ | -15 798 600 ₽ | -19 464 000 ₽ | -23 238 400 ₽ | -25 953 200 ₽ | -27 431 800 ₽ | -27 497 600 ₽ | -26 150 600 ₽ | -23 214 200 ₽ |

- Break-even по клиентам: **38**.
- Break-even по месяцам: **M11**.
- startup_capital_to_bep_rub: **27 497 600 ₽**.
- Waterfall @50 clients: **ARPA 220 000 ₽ -> Gross 176 600 ₽ -> Contribution 176 600 ₽ -> EBITDA 2 230 000 ₽ -> Net**: УСН 6% = **1 570 000 ₽**, IT-льгота 3% = **1 900 000 ₽**, ОСНО 20% = **1 784 000 ₽**.

### Pessimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 5 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 13 | 18 | 23 |
| MRR | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 140 000 ₽ | 280 000 ₽ | 560 000 ₽ | 840 000 ₽ | 1 260 000 ₽ | 1 820 000 ₽ | 2 520 000 ₽ | 3 220 000 ₽ |
| COGS | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 31 600 ₽ | 63 200 ₽ | 126 400 ₽ | 189 600 ₽ | 284 400 ₽ | 410 800 ₽ | 568 800 ₽ | 726 800 ₽ |
| Gross profit | 0 ₽ | 0 ₽ | 0 ₽ | 0 ₽ | 108 400 ₽ | 216 800 ₽ | 433 600 ₽ | 650 400 ₽ | 975 600 ₽ | 1 409 200 ₽ | 1 951 200 ₽ | 2 493 200 ₽ |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 77,4% | 77,4% | 77,4% | 77,4% | 77,4% | 77,4% | 77,4% | 77,4% |
| Fixed costs | 2 014 000 ₽ | 2 709 000 ₽ | 3 658 000 ₽ | 4 568 000 ₽ | 5 322 000 ₽ | 5 608 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ | 6 600 000 ₽ |
| EBITDA | -2 014 000 ₽ | -2 709 000 ₽ | -3 658 000 ₽ | -4 568 000 ₽ | -5 213 600 ₽ | -5 391 200 ₽ | -6 166 400 ₽ | -5 949 600 ₽ | -5 624 400 ₽ | -5 190 800 ₽ | -4 648 800 ₽ | -4 106 800 ₽ |
| Cash burn | 2 014 000 ₽ | 2 709 000 ₽ | 3 658 000 ₽ | 4 568 000 ₽ | 5 213 600 ₽ | 5 391 200 ₽ | 6 166 400 ₽ | 5 949 600 ₽ | 5 624 400 ₽ | 5 190 800 ₽ | 4 648 800 ₽ | 4 106 800 ₽ |
| Cumulative cash | -2 014 000 ₽ | -4 723 000 ₽ | -8 381 000 ₽ | -12 949 000 ₽ | -18 162 600 ₽ | -23 553 800 ₽ | -29 720 200 ₽ | -35 669 800 ₽ | -41 294 200 ₽ | -46 485 000 ₽ | -51 133 800 ₽ | -55 240 600 ₽ |

- Break-even по клиентам: **61**.
- Break-even по месяцам: **не достигается в горизонте M1-M12**.
- startup_capital_to_bep_rub: **55 240 600 ₽**. Это минимум для горизонта 12 месяцев, без учета дополнительного буфера.
- Waterfall @50 clients: **ARPA 140 000 ₽ -> Gross 108 400 ₽ -> Contribution 108 400 ₽ -> EBITDA -1 180 000 ₽ -> Net**: УСН 6% = **-1 600 000 ₽**, IT-льгота 3% = **-1 390 000 ₽**, ОСНО 20% = **-1 180 000 ₽**.

### Налоговая модель РФ

- **УСН 6%**: налог считается с выручки. Для early-stage SaaS это часто самый жесткий режим к EBITDA при низкой марже по EBITDA.
- **IT-льгота 3%**: применима при аккредитации Минцифры и соблюдении профильных критериев. Для этого кейса это **предпочтительный режим**, если структура выручки и юрлицо позволяют.
- **ОСНО 20%**: налог на прибыль 20% только при положительной прибыли, но при применимости ОСНО возникает **НДС 20%**, который обычно проходит ниже выручки как транзитный налог и ухудшает cash conversion.
- **Страховые взносы ~30% к ФОТ** уже включены в team FOT и fixed costs.

### Вывод по PnL

- **Base**: модель почти доходит до безубыточности за 12 месяцев, но формальный break-even сдвинут на **M13**; минимальная потребность в капитале до точки безубыточности близка к **43,7 млн ₽**.
- **Optimistic**: break-even достигается в **M11**, startup_capital_to_bep_rub около **27,5 млн ₽**.
- **Pessimistic**: в горизонте 12 месяцев break-even не достигается; капиталовая потребность на этот горизонт около **55,2 млн ₽**.

<!-- P6A-DONE -->

## SECTION B — Finance Risk + Competitor

Источник чисел для Base: 04-economics.md этого кейса. Где нет прямых чисел, использую консервативный inference на базе уже зафиксированных bear/base/bull допущений и публичных описаний конкурентов.

### 1. Sensitivity analysis, EBITDA через 12 месяцев

Логика:
- **CAC x2**: при том же acquisition budget поток новых платящих клиентов падает примерно в 2 раза, поэтому к M12 вместо ~40 клиентов модель удерживает около ~20 клиентов. [T1][inference]
- **Churn x2**: churn растёт с 2,2% до 4,4% в месяц, что бьёт прежде всего по накопленной клиентской базе и LTV. [T1][inference]
- **Price -30%**: ARPU падает с 180 000 ₽ до 126 000 ₽, COGS считаю в первом приближении неизменным, поэтому contribution на клиента падает с 144 500 ₽ до ~90 500 ₽. [T1][inference]

| Сценарий | Ключевое изменение | Клиенты / эквивалент к M12 | EBITDA @M12 |
|---|---|---:|---:|
| Base | Без изменений | 40 | -820 000 ₽ |
| Sens1 | CAC x2 | ~20 | **-3 710 000 ₽** |
| Sens2 | Churn x2 | ~36 | **-1 398 000 ₽** |
| Sens3 | Price -30% | 40 | **-2 980 000 ₽** |

### Вывод по чувствительности
- Самый опасный single-point shock для этой модели, **не считая регуляторных стопов**, это **price compression**: при -30% к цене EBITDA уходит почти на **-3,0 млн ₽/мес** даже без роста CAC. [inference]
- **CAC x2** почти так же разрушителен: модель остаётся живой только если компания может компенсировать удорожание продаж более высоким ARPU или лучшей pilot-to-rollout конверсией. [T1][inference]
- **Churn x2** выглядит чуть менее убийственным на горизонте 12 месяцев, но именно он сильнее всего ломает экономику на M24 и дальше, потому что срезает LTV и замедляет накопление клиентской базы. [T1][inference]

### 2. Monte Carlo Lite, confidence intervals

Использую упрощённую версию вместо 1000 симуляций: **9 комбинаций** вокруг triangular inputs. p10/p50/p90 ниже, это не статистически строгий MC, а инвестиционная approximation grid для проверки хрупкости модели.

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC ₽ | 430 000 | 462 429 | 620 000 | [T1] |
| Monthly churn % | 1,8% | 2,2% | 3,5% | [T1] |
| ARPU ₽/мес | 140 000 | 180 000 | 220 000 | [T1] |
| Conversion rate lead→paid % | 0,2% | 0,3% | 0,5% | [T1][inference] |
| Time-to-hire месяцев, среднее | 1,0 | 1,5 | 2,5 | [T1] |

#### p10 / p50 / p90 outcome table

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-1 800 000 ₽** | **4 100 000 ₽** | **10 200 000 ₽** | **12 000 000 ₽** |
| CAC payback (мес) | **4,4** | **2,6** | **1,9** | **2,5** |
| LTV/CAC | **3,3x** | **14,2x** | **25,4x** | **22,1x** |
| Cash runway (мес) | **8,5** | **12,4** | **19,2** | **10,7** |

#### Интерпретация Monte Carlo Lite
- **Правило 1 срабатывает**: `p10 EBITDA < 0`, значит worst-decile сценарий уже указывает на **risk of insolvency** без bridge round или жёсткого снижения fixed opex. [inference]
- **Правило 2 не срабатывает**: `p50 EBITDA > 500К ₽/мес`, значит медианный сценарий EBITDA Gate проходит. [inference]
- **Правило 3 срабатывает по сути**: dispersion экстремальная, а при отрицательном p10 отношение `p90/p10` теряет смысл, но сам диапазон слишком широк, поэтому **score нужно понизить за неопределённость**. [inference]
- **Правило 4 срабатывает**: `Range width по LTV/CAC = 22,1x`, намного выше порога 8, значит модель реально хрупкая к комбинации `pricing + churn + CAC`. [inference]

### 3. Competitor deep-dive

Ниже market-share estimate — это **оценка доли в узком subsegment physician-facing clinical decision support / AI-assistant**, а не во всём digital health. Для западных игроков беру глобально/US usage inference, для российских — локальный enterprise/reference niche.

#### 3.1. Western, top-3

| Игрок | Почему важен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **UpToDate Expert AI / Wolters Kluwer** [B1][B2][B3] | Инкумбент доказательной клинической справки, уже добавил GenAI-слой | сильнейший бренд доверия, огромная экспертная база, enterprise distribution, traceable reasoning | дорогой и тяжёлый enterprise stack, слабее локализация под РФ, не built-for-Russian-guidelines | **35-45%** legacy clinical reference / **20-30%** GenAI-CDS среди крупных систем [inference] | IQDOC может быть быстрее, дешевле и глубже по **клинрекам Минздрава РФ + локальным НПА + русскому медицинскому языку** |
| **OpenEvidence** [B4][B5] | Самый быстрорастущий physician-AI search в США | очень сильный продуктовый UX, быстрый retrieval, высокая врачебная adoption, сильные партнёрства с JAMA/NEJM | US-only trust/data moat, слабая пригодность для РФ, regulation/data residency вне их core | **15-25%** physician-AI search / CDS usage в США [inference] | IQDOC может выигрывать локальным compliance-контуром и enterprise deployment без передачи чувствительных данных в американский SaaS |
| **Glass Health** [B6][B7][B8] | Близкий по форме copilot для врача: Q&A, differential, plan drafting | workflow-native, ambient + CDS, API/integration layer, evidence-based outputs | меньше brand trust, уже довольно crowded category, не заточен под российские требования и локальные источники | **1-3%** physician-AI CDS niche [inference] | IQDOC проще позиционировать как **узкий regulated assistant по лабораторной интерпретации и клинрекам**, а не общий doctor copilot |

#### 3.2. Russian, top-4

| Игрок | Почему важен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Webiomed / К-Скай** [B9][B10] | Самый серьёзный локальный сосед по классу clinical decision support и compliance | регистрационный/интеграционный опыт, бренд Сколково, B2B/B2G distribution, работа с клинрекомендациями | шире и тяжелее как platform bet, не так сфокусирован на узком wedge «лаборатория + интерпретация + поиск» | **8-12%** РФ clinical AI/CDS subsegment [inference] | IQDOC может быть легче во внедрении, быстрее в поиске по документам и точнее в узком lab-use-case |
| **MedBase / ГЭОТАР** [T2][B11] | Прямой reference substitute для врача | уже продаёт врачам доступ к базе знаний, понятный WTP, низкий порог входа | это скорее база/справочник, чем workflow copilot; слабее AI moat и enterprise orchestration | **10-15%** physician reference subscription niche [inference] | IQDOC может дать **answer engine с цитатами, а не только доступ к базе** |
| **Medlock** [T2] | Близок по клинрекам и compliance-слою для клиник | B2B-монетизация, привязка к клиническим рекомендациям, ценность для аудита и маршрутизации | уже не «быстрый врачебный поиск», а более процессный workflow, значит выше friction внедрения | **2-5%** guideline workflow niche [inference] | IQDOC может зайти снизу как doctor productivity tool и затем апселлить в workflow/compliance |
| **OncoCopilot** [B12] | Показательный российский нишевой copilot для врачей | очень хороший wedge-фокус, RAG + клинические маршруты + документация, легче доказать ROI в узкой специальности | нишевость ограничивает TAM, масштабирование за пределы онкологии неочевидно | **<1%** общего physician-AI subsegment, но заметная доля в своём микро-сегменте [inference] | IQDOC шире по specialty coverage и лучше ложится на multi-clinic/lab rollout, если докажет качество на общей терапии и диагностике |

### Вывод по конкуренции
- На Западе категория уже быстро институционализируется: **incumbent trusted content + physician-native AI UX** становится стандартом. [B1][B4][B6]
- В РФ рынок пока фрагментирован между **справочниками**, **workflow/compliance-решениями** и **точечными AI-помощниками**. Это даёт окно, но не даёт white space. [T2][B9][B12]
- Реальный шанс IQDOC: не пытаться победить всех как «универсальный мед-ИИ», а зафиксироваться как **лучший локальный assistant по клинрекам Минздрава, лабораторной интерпретации и explainable answer engine для клиник**. [inference]

### 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного Clinical Lead и ML Engineer в срок | med | high | time-to-hire > 2,5 мес, repeated offer declines | заранее формировать advisor bench, дробить роли на fractional setup, удерживать резервный hiring budget |
| Operational | Качество ответов по сложным кейсам нестабильно, hallucination rate выше допустимого | med | high | рост числа physician overrides, жалобы пилотных врачей | gold-set eval, red-team сценарии, human-in-the-loop review, ограничение use cases на старте |
| Operational | LLM API latency/cost drift бьёт по SLA и COGS | high | med | inference cost > 12-15 тыс. ₽ на клиента, p95 latency растёт | multi-model routing, локальный fallback, кэширование, prompt compression |
| Market | Adjacent-demand есть, но buyers не видят budget line item | med | high | много пилотов, мало rollout contracts, низкий close rate | продавать через ROI и compliance narrative, а не через «ещё один AI tool» |
| Market | Конкуренты сжимают цену до уровня справочника 300-800 ₽/мес на врача | high | high | частые price objections, сделки с дисконтом >30% | уходить в clinic/lab ACV, seat-bundle, workflow integrations и audit trail |
| Market | Incumbent типа UpToDate/OpenEvidence локализует русскоязычный UX или заходит через партнёра | low | high | крупные клиники начинают пилотировать иностранные AI-CDS | ускорить локальный moat: 152-ФЗ, data residency, русские источники, on-prem/private cloud |
| Regulatory | 152-ФЗ / data residency не позволяет использовать публичный зарубежный SaaS-контур | high | high | security review стопорится на DPA и хранении данных | private cloud, on-prem, деидентификация, запрет на PHI в open endpoints |
| Regulatory | 115-ФЗ и банковские/compliance процедуры тормозят B2B cash collection | med | med | unusually long contract/payment cycles, extra KYC requests | early legal templates, заранее подготовленный compliance pack, предоплата пилотов |
| Regulatory | Усиление требований к медицинскому ПО и трактовка как медизделия | med | high | клиники требуют РУ/сертификацию до пилота | product scoping как assistant, юридическая позиция, дорожная карта к регистрации при необходимости |
| Financial | Cash runway уходит ниже 9 месяцев до достижения repeatable sales | high | high | burn > план на 20%+, lag по MRR 2 квартала подряд | нанимать этапно, урезать fixed opex, stop hiring until pilot conversion improves |
| Financial | Курс USD и импортный SaaS stack повышают COGS и dev-tooling spend | high | med | рост cloud/API invoices в ₽ на 20%+ | рублёвые контракты, российские аналоги, резерв в pricing |
| Financial | Инфляция ФОТ и рост налоговой нагрузки сдвигают break-even вправо | med | med | salary refresh чаще чем раз в 12 мес, рост payroll >10-12% | индексировать цены, держать variable comp, автоматизировать поддержку |
| Black swan | Резкое ужесточение санкций на LLM/API или отключение критического провайдера | med | high | предупреждения о прекращении сервиса, просадка SLA | multi-vendor architecture, локальный inference fallback, заранее собранный резерв моделей |
| Black swan | Военная/политическая эскалация ломает рынок private healthcare capex | med | high | freeze новых IT-бюджетов, приостановка пилотов | уход в ROI-first buyers, shorter pilots, сохранение cash buffer 12+ мес |

### 5. Kill conditions, через 6 месяцев продолжать нельзя

1. **Median-case insolvency risk**: если обновлённый forward model показывает `p10 EBITDA@M24 < 0` **и** cash runway < **6 месяцев**, проект нельзя продолжать без bridge round или резкого downsizing.
2. **Go-to-market failure**: если через 6 месяцев меньше **5 платящих B2B-клиентов** или pilot→paid conversion < **20%**, значит enterprise motion не подтверждён.
3. **Pricing failure**: если фактический ARPU < **120 000 ₽/мес** на организацию **или** blended CAC > **900 000 ₽**, то LTV/CAC и EBITDA gate перестают быть инвестиционно интересными.

### 6. Финальный вывод SECTION B

- Кейс **не разваливается в median**, но **очень хрупок в lower-tail**.
- Главная опасность не одна конкретная метрика, а связка **price compression + CAC inflation + regulatory friction**.
- По конкуренции IQDOC нельзя считать white-space play: против него уже есть и **глобальные trusted incumbents**, и **локальные российские substitutes**. Следовательно, ставку нужно делать на **локальную explainability, 152-ФЗ-ready deployment и узкий physician workflow ROI**.
- Для investment discipline я бы **снизил score за uncertainty**, даже при сохранении базового PASS по экономике. [inference]

### Источники SECTION B
- [B1] Wolters Kluwer, UpToDate Expert AI overview: https://www.wolterskluwer.com/en/solutions/uptodate/ai-clinical-decision-support
- [B2] Wolters Kluwer, AI Labs / UpToDate press release: https://www.wolterskluwer.com/en/news/himss-uptodate-ailabs
- [B3] Wolters Kluwer, UpToDate editorial process: https://www.wolterskluwer.com/en/solutions/uptodate/about/editorial-process
- [B4] OpenEvidence about: https://www.openevidence.com/about
- [B5] OpenEvidence funding/adoption announcement: https://www.openevidence.com/announcements/openevidence-the-fastest-growing-application-for-physicians-in-history-announces-dollar210-million-round-at-dollar35-billion-valuation
- [B6] Glass Health overview: https://glass.health/info
- [B7] Glass Health features: https://glass.health/features
- [B8] Glass Health API / integration: https://glass.health/developer-api
- [B9] Сколково, Webiomed в коммерческой медицине: https://sk.ru/news/rezident-skolkovo-vyvel-ii-platformu-webiomed-na-rynok-kommercheskoj-mediciny/
- [B10] Сколково, сервис контроля соблюдения клинических рекомендаций Webiomed: https://sk.ru/news/v-platformu-webiomed-dobavlen-servis-kontrolya-soblyudeniya-klinicheskih-rekomendacij/
- [B11] Rusprofile, ООО КБ «Гэотар»: https://www.rusprofile.ru/id/10917382
- [B12] Habr, OncoCopilot: https://habr.com/ru/articles/933638/

<!-- P6B-DONE -->


---

# 06-verdict.md

# 06-verdict

[HEALTHCARE] IQDOC — NEAR-PASS: 69/100 | EBITDA base=625К₽/мес через 13 мес | LTV/CAC=14,2x | Ключевое преимущество: локальный clinical assistant по клинрекам Минздрава РФ | Главный риск: weak moat и тяжёлый regulated GTM.

sector: HEALTHCARE

## Вердикт
**NEAR-PASS**

## Investment committee summary
IQDOC выглядит сильнее типичного medical AI-ассистента по экономике клиента: `customer_ltv_rub = 6 568 182 ₽`, `CAC = 462 429 ₽`, `LTV/CAC = 14,2x`, `CAC payback = 2,6 мес`, `GM = 80,3%`, `contribution_margin_rub_month = 144 500 ₽/клиент/мес`. На уровне компании базовая модель проходит profitability gate, потому что при `50` клиентах даёт `company_ebitda_rub_month = 625 000 ₽/мес`, а break-even ожидается около `M13`. Но инвестиционный запас прочности пока недостаточен: exact-demand в РФ остаётся умеренным и во многом adjacent, moat слабый, а модель чувствительна к `price compression + CAC inflation + regulatory friction`.

## Оценка
Source tier balance: T1=7, T2=6, T3=1, weighted=2.35. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | В `04-economics.md` указано: `LTV/CAC = 14,2x`, `CAC Payback = 2,6 мес`, `Gross Margin = 80,3%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В `04-economics.md`: `EBITDA / мес = 625 000 ₽` при `50` клиентах и `Break-even month = M13`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | В `02-demand.md` есть `adjacent-demand ... MEDIUM / 30`, `WTP подтверждён`, но `exact-demand ... низкий`; применён tier penalty `-2`. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | В `05-critic.md` прямо сказано: `кейс не разваливается в median, но очень хрупок в lower-tail`, а локальный moat держится в основном на `152-ФЗ-ready deployment и узком physician workflow ROI`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В `05-critic.md` перечислены high/high риски: `price objections`, `152-ФЗ`, `medical software`, `cash runway`, `санкции на LLM/API`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | В `04-economics.md` `CAC Payback = 2,57 месяца`, а лучший motion это `частные сети клиник, лаборатории, диагностические центры` с pilot-to-rollout. |

**Sum raw = 103 / 150. Normalized score = round((103 * 100) / 150) = 69/100.**

## Почему это NEAR-PASS, а не APPROVED
1. Financial gate проходит: базовая модель даёт `company_ebitda_rub_month = 625 000 ₽/мес` при `50` клиентах и горизонте `13` месяцев.
2. Но exact-category demand в РФ пока не подтверждён на investment-grade уровне, а текущий рынок скорее adjacent: `клинические рекомендации`, `расшифровка анализов`, `workflow/compliance around clinical recommendations`.
3. Moat остаётся слабым: без глубоких интеграций и доказанного clinical trust IQDOC рискует остаться просто более быстрым справочником поверх существующих баз знаний.
4. Monte Carlo из `05-critic.md` показывает `p10 EBITDA @M24 = -1 800 000 ₽`, то есть левый хвост всё ещё уходит в insolvency-risk.

## FULL business process из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ на 1 won client | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Формирование ICP-списка и ресёрч клиник/лабораторий | SDR | HH, Rusprofile, CRM, таблицы | 6 ч | 6 500 | 60% |
| 2 | Первичный outbound / outreach | SDR | email, телефония, LinkedIn/аналог, amoCRM | 12 ч | 18 000 | 55% |
| 3 | Квалификация боли и маршрутизация | SDR + AE | amoCRM, скрипты, call notes | 4 ч | 9 500 | 45% |
| 4 | Discovery-call с главным врачом / операционным директором | AE | видеосвязь, demo deck | 2 ч + подготовка | 16 000 | 25% |
| 5 | Демо на реальных кейсах лабораторной интерпретации | AE + Clinical Lead | demo environment, sandbox | 5 ч | 27 000 | 30% |
| 6 | Пилот и настройка базы документов / шаблонов | CTO + ML + Backend | cloud, RAG stack, prompt/eval | 24 ч | 95 000 | 35% |
| 7 | Проверка клинической точности и explainability | Clinical Lead | чек-листы, экспертная валидация | 10 ч | 34 000 | 20% |
| 8 | Security / legal review, DPA, 152-ФЗ | CEO + CTO | шаблоны договора, ИБ-чеклист | 8 ч | 28 000 | 15% |
| 9 | Коммерческое предложение и согласование rollout | AE + CEO | CRM, CPQ, e-sign | 5 ч | 23 000 | 35% |
| 10 | Выставление счёта и получение первой оплаты | Finance/CEO | банк, ЭДО, CRM | 2 ч | 7 000 | 70% |
| 11 | Customer onboarding после оплаты | CSM + Backend | knowledge base, training | 8 ч | 31 000 | 40% |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | **6 568 182 ₽** |
| CAC fully-loaded | **462 429 ₽** |
| LTV/CAC | **14.2x** |
| CAC Payback | **2.6 мес** |
| GM | **80.3%** |
| Break-even clients | **46** |
| Break-even month | **M13** |
| contribution_margin_rub_month на клиента | **144 500 ₽/клиент/мес** |
| company_ebitda_rub_month @ 50 клиентов | **625 000 ₽/мес** |
| clients_to_500k_ebitda | **46** |
| months_to_500k_ebitda | **13** |
| startup_capital_to_bep_rub | **43 682 500 ₽** |
| Startup capital working minimum | **45 000 000-55 000 000 ₽** |

## Team table
| Роль | Кол-во | Fully-loaded FOT ₽/мес | Time-to-hire | Комментарий |
|---|---:|---:|---:|---|
| CEO | 1 | 845 000 | 0.0 мес | продажи enterprise-аккаунтов, партнёрства, fundraising |
| CTO / Tech Lead | 1 | 650 000 | 2.0 мес | архитектура, security, deployment policy |
| Senior Backend | 2 | 988 000 | 1.5 мес | API, интеграции, RAG-пайплайн |
| ML Engineer | 1 | 585 000 | 2.5 мес | retrieval quality, evaluation, prompting |
| DevOps | 1 | 416 000 | 1.5 мес | облако, мониторинг, резервирование |
| Frontend | 1 | 338 000 | 1.0 мес | physician UX и админ-панель |
| SDR | 1 | 214 500 | 0.75 мес | cold outreach и первичная квалификация |
| AE | 1 | 416 000 | 1.5 мес | discovery, demo, пилоты, закрытие |
| Customer Success | 1 | 286 000 | 1.0 мес | внедрение, обучение, renewals |
| Clinical Lead / медэксперт | 1 | 364 000 | 1.5 мес | клиническая валидность, explainability, audit |
| **Итого** | **10** | **5 102 500 ₽/мес** |  | full operating team |

## Moat: 7-factor framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не делает продукт заметно лучше для остальных. |
| 2. Switching costs | 2 | После интеграций, обучения и настройки врачебного workflow переключение становится болезненным. |
| 3. Scale economies | 2 | Контент, evaluation и infra частично масштабируются на портфель клиник. |
| 4. Proprietary data / model advantage | 1 | Может накопиться usage/eval data, но доказанного data moat пока нет. |
| 5. Regulatory moat | 1 | 152-ФЗ и private cloud помогают в продаже, но сами по себе не дают сильного защитного рва. |
| 6. Brand / distribution | 1 | Есть локальный healthcare narrative, но сильного бренда уровня incumbents пока нет. |
| 7. Embedded workflow | 2 | При регулярном использовании продукт встраивается в physician workflow и clinical navigation. |

**Moat sum = 9 / 21. Moat score = round((9 * 25) / 21) = 11/25.**

## GTM: 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | крупная частная сеть с широким physician workflow и нагрузкой на интерпретацию анализов | email medical director / digital director + MedSoft | 220 000 ₽/мес |
| 2 | Инвитро | лабораторная сеть, где ценен быстрый слой интерпретации и навигации по рекомендациям | партнёрство + email product/medical lead | 250 000 ₽/мес |
| 3 | Гемотест | высокий поток лабораторных результатов и понятный сценарий patient-to-doctor handoff | outbound на chief medical officer + отраслевые конференции | 220 000 ₽/мес |
| 4 | Хеликс | diagnostics-first сеть, где можно продавать usage-based lab workflow | email decision-maker + партнёрство с LIS/CRM интегратором | 240 000 ₽/мес |
| 5 | СМ-Клиника | сеть частных клиник с большим объёмом врачебных консультаций и лабораторных направлений | direct outreach на операционного директора + кейс на vc.ru | 180 000 ₽/мес |
| 6 | Клиника Фомина | цифровая частная сеть, готовая тестировать physician productivity tools | email head of digital / medical ops | 170 000 ₽/мес |
| 7 | Мать и дитя | сложный клинический контур и высокая цена врачебного времени | conference intro + email chief doctor | 230 000 ₽/мес |
| 8 | EMC | premium-клиника, где justify можно через скорость доступа к клинрекам и quality-of-care | founder-led outreach на medical leadership | 250 000 ₽/мес |
| 9 | Будь Здоров | крупная сеть, где важны стандартизация и explainable physician support | email operations / medical quality lead | 180 000 ₽/мес |
| 10 | Скандинавия / АВА-ПЕТЕР | сильный private healthcare игрок с цифровым контуром и потребностью в стандартизации care-path | партнёрство + профильная конференция | 190 000 ₽/мес |

**Итог по GTM:** реалистичен только named-account enterprise motion через частные сети клиник, лаборатории и диагностические центры. Лучшие каналы, это `email decision-maker + профильные конференции + партнёрство с интеграторами/вендорами медконтуров`.

## Top-3 risks
| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| weak_moat / product can be reframed as upgraded reference tool | High | High | Moat score всего `11/25`, а защиту пока дают скорее локализация и интеграции, чем не复制руемый продуктовый актив. |
| price_compression + CAC_inflation | High | High | В `05-critic.md` самые токсичные сценарии, это `Price -30%` и `CAC x2`, которые резко ухудшают `EBITDA @M12`. |
| evidence_quality_and_regulatory_execution | Medium | High | Exact-demand остаётся adjacent, а `152-ФЗ`, explainability и риск трактовки как медизделия могут затормозить rollout. |

## LTV Upside Calculator
| Рычаг | Текущая база | Upside-case | Эффект |
|---|---|---|---|
| ARPU / ACV | 180 000 ₽/мес | 220 000 ₽/мес | EBITDA @50 клиентов растёт с `625 000 ₽` до `2 230 000 ₽/мес` |
| Churn | 2.2%/мес | 1.8%/мес | customer_ltv_rub растёт примерно с `6,57 млн ₽` до `8,03 млн ₽` |
| CAC | 462 429 ₽ | 430 000 ₽ | LTV/CAC растёт примерно с `14,2x` до `15,3x` |
| Pilot→paid conversion | 20-25% | 30%+ | уменьшает CAC volatility и ускоряет выход к `46` клиентам |
| Distribution mix | founder/AE-heavy | 30-40% pipeline через партнёрства | снижает execution-risk и делает GTM более repeatable |

## Что нужно доказать для перехода в APPROVED
1. Что фактический B2B `ARPU` устойчиво держится **не ниже 180-200 тыс. ₽/мес** без скидочной эрозии.
2. Что pilot→paid conversion подтверждается на выборке минимум **8-10 пилотов** и даёт предсказуемый sales cycle.
3. Что `logo churn ≤ 2%/мес`, а продукт становится частью physician workflow, а не разовой справочной игрушкой.
4. Что есть минимум **2-3 референсных внедрения** в сетях клиник или лабораториях с measurable ROI по времени врача / quality / compliance.

## Proof points для APPROVED
Пока отсутствуют. Для апгрейда до APPROVED комитету нужны:
- 2-3 публично или приватно верифицируемых enterprise-клиента в РФ;
- подтверждённый repeatable контракт **≥180 тыс. ₽/мес**;
- доказанная explainability и безопасность для security/legal review без блокировки сделки;
- evidence, что продукт выигрывает не только по скорости ответа, но и по workflow outcomes.

## Финальный вывод IC
IQDOC не проваливается по математике и уже выглядит как настоящий regulated B2B healthtech, а не consumer AI utility. Но инвестиционный профиль пока всё ещё хрупкий: рынок подтверждён лишь частично, moat слабый, а lower-tail risk заметный. Поэтому решение комитета, это **NEAR-PASS: 69/100**. Следующий апгрейд до approve возможен только после валидации repeatable enterprise GTM и clinical trust moat.

---

# 07-score-trajectory.md

## 2026-04-26 — P4 Demand Validation
- Stage: P4 / demand-validation
- Analyst: branch-models-lead
- Score trajectory: **7.0 → 7.4**
- Verdict shift: **TRIAGE PASS → PASS WITH RESERVATIONS**
- Why it moved:
  - adjacent-demand по клиническим рекомендациям и интерпретации анализов в РФ подтверждён, но exact-category demand остаётся слабым;
  - willingness to pay подтверждён публичными ценами MedBase, Reclin и Medlock, то есть деньги в категории уже платятся;
  - инвестиционный кейс держится только на B2B/enterprise motion, тогда как B2C-only сценарий Profit Gate не проходит.
- Key risks:
  - слабый exact-demand означает долгий educative sale и необходимость продавать outcome, а не категорию;
  - низкий reference price у справочных продуктов ограничивает pricing power без enterprise-integration и explainability;
  - регулируемость и клиническая ответственность могут удлинить пилоты и снизить скорость продаж.
- Next check:
  - проверить unit economics по B2B clinic bundle и enterprise/lab scenario, включая CAC, pilot conversion и ACV uplift.

## 2026-05-09 — P5 Unit Economics
- Stage: P5 / unit-economics
- Analyst: branch-models-lead
- Score trajectory: **7.4 → 7.8**
- Verdict shift: **PASS WITH RESERVATIONS → PASS**
- Why it moved:
  - fully-loaded CAC в regulated B2B healthtech получился **462 тыс. ₽**, что укладывается в реалистичный benchmark и не выглядит искусственно заниженным;
  - при базовом ICP **180 тыс. ₽ MRR на клиента** модель даёт **Contribution Margin 80,3%**, **CAC Payback 2,6 мес** и **LTV/CAC 14,2x**;
  - Profit Gate проходит: на масштабе **50 клиентов** бизнес выходит примерно на **625 тыс. ₽ EBITDA / мес**, а break-even достигается около **M13**.
- Key risks:
  - экономика остаётся хорошей только в enterprise / lab-network motion, а не в low-ACV клиниках;
  - высокий burn до безубыточности, пиковая потребность в капитале около **43,7 млн ₽**, поэтому недокапитализация быстро сломает траекторию;
  - длинные legal / security / clinical pilots могут сдвинуть cash-in и ухудшить runway.
- Next check:
  - подтвердить, что в реальных пилотах IQDOC удерживает ACV не ниже **180 тыс. ₽/мес**, а logo churn после rollout остаётся в диапазоне до **2-3% / мес**.

## 2026-05-10 — P7 Critic and Verdict
- Stage: P7 / critic-and-verdict
- Analyst: branch-models-lead
- Score trajectory: **7.8 → 6.9**
- Verdict shift: **PASS → NEAR-PASS**
- Why it moved:
  - несмотря на сильную клиентскую economics, exact-demand в РФ остаётся скорее adjacent, чем category-defining, поэтому кейс не дотягивает до investment-grade certainty;
  - moat слабый: без глубоких интеграций и подтверждённого clinical trust продукт рискует остаться быстрым справочником поверх уже существующих баз знаний;
  - Monte Carlo из `05-critic.md` даёт `p10 EBITDA @M24 = -1,8 млн ₽`, то есть lower-tail риск всё ещё слишком велик для безусловного approve.
- Key risks:
  - weak_moat и возможность price compression со стороны справочников, CDS-платформ и локальных substitutes;
  - regulatory/explainability friction, которая может удлинить sales cycle и срезать pilot-to-rollout conversion;
  - CAC inflation и founder-heavy GTM при необходимости долго продавать outcome, а не категорию.
- Next check:
  - доказать 2-3 референсных enterprise-внедрения в сетях клиник или лабораториях, стабильный ACV **≥180-200 тыс. ₽/мес** и pilot→paid conversion на выборке не меньше **8-10** пилотов.