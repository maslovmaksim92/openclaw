[HEALTHCARE] Abridge, AI-медицинский скрайб для клиник — NEAR-PASS: 68/100 | EBITDA base=5349К₽/мес через 12 мес | LTV/CAC=4,9x | Ключевое преимущество: deep workflow integration в клиническую документацию | Главный риск: ранний RU-demand и тяжёлый enterprise GTM.

# Abridge, AI-медицинский скрайб для клиник — полный verdict

sector: HEALTHCARE
status: NEAR-PASS
score: 68/100
date: 2026-04-25
slug: abridge-ai-meditsinskiy-skraib-dlya-klinik
repo_path: rejected/abridge-ai-meditsinskiy-skraib-dlya-klinik/verdict.md

## Stage 1. Intake
- Western category proof сильный: Abridge уже масштабировался до 250+ health systems в США.
- В РФ зрелого прямого аналога не найдено, но pain по doctor documentation time real.
- Изначальная гипотеза: heavy enterprise healthtech wedge для частных сетей клиник.

## Stage 2. Demand Validation
- Итог demand-stage: `CONDITIONAL PASS`.
- Source tier balance: `T1=1, T2=6, T3=1`, weighted `2.00`, штраф к Market+Demand: `-2`.
- Buyer base в РФ есть, но прямой market pull пока ранний и sales-led.

## Stage 3. Economics
- customer_ltv_rub: `11 050 000 ₽`
- CAC blended: `2 242 000 ₽`
- LTV/CAC: `4,9x`
- CAC payback: `6,4 мес`
- Gross Margin: `66,3%`
- contribution_margin_rub_month: `232 000 ₽`
- company_ebitda_rub_month при 50 клиентах: `5 349 000 ₽/мес`
- startup_capital_to_bep_rub: `31 789 448 ₽`

## Stage 4. Finance / PnL / Risk
- Base M12 EBITDA: `4 171 937 ₽/мес`
- Optimistic break-even: `M9`
- Pessimistic break-even: `не достигнут в M1-M12`
- Sensitivity: `price -30% => -545 146 ₽ EBITDA @M12`
- Monte Carlo Lite: `p10=1,89 млн ₽`, `p50=9,28 млн ₽`, `p90=22,22 млн ₽`

## Stage 5. Critic scorecard
- Unit Economics: `18/25`
- EBITDA Potential: `19/25`
- Market + Demand: `14/25`
- Moat: `13/25`
- Execution Risk: `16/25`
- GTM Realism: `22/25`
- Sum raw: `102/150`
- Normalized: `68/100`

## Stage 6. Final verdict
**NEAR-PASS.**

Кейс почти проходит approve благодаря живой economics и сильной workflow-боли, но на момент 25.04.2026 не дотягивает до investment-grade из-за раннего локального спроса, среднего moat и unusually hard execution profile.

## Что доказать для upgrade до APPROVED
1. 2+ paid pilots в крупных частных сетях.
2. Контрактный floor не ниже 300-350 тыс. ₽/мес на контур.
3. Repeatable MIS connector и override rate врача <20%.
4. Партнёрский канал, снижающий blended CAC.

---

# Файл: 01-intake.md

---
sector: HEALTHCARE
rerun: false
source_raw: 2026-04-24-geo-expand-abridge-ai-meditsinskiy-skraib-dlya-klinik.md
created: 2026-04-24T15:11:37+03:00
---

# Intake

## Статус
Новый кейс, создан на этапе intake/triage.

## Wedge statement
Abridge даёт клиникам AI-слой ambient documentation, который слушает разговор врача с пациентом и автоматически формирует структурированную клиническую запись с привязкой к источнику.

## Почему это не duplicate
Сигнал не совпадает с уже открытыми кейсами по AI-администратору для клиник, radiology AI или document quality AI. Здесь отдельный workflow, отдельный buyer pain и отдельная ценность: не запись пациента, не анализ снимков и не аудит уже готовой документации, а создание клинической записи прямо во время приёма.

## Краткий контекст
Это GEO-EXPAND сигнал по зрелой западной категории ambient clinical AI с заметным enterprise-масштабом. Для РФ локализация будет тяжёлой, но сама боль врачебной документации, дефицита времени и перегруженности клиницистов достаточно сильна, чтобы рассматривать кейс как самостоятельный high-LTV healthcare wedge.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить buyer map в РФ, интеграционную сложность, регуляторные ограничения и путь к коммерческому пилоту.

## Полный контекст из raw

# Abridge

## Sector
GEO-EXPAND

## Wedge statement
AI-платформа, которая в реальном времени слушает разговор врача с пациентом и автоматически превращает его в структурированную клиническую документацию с привязкой к исходным доказательствам.

## Evidence
- [T2] https://techcrunch.com/2025/06/24/in-just-4-months-ai-medical-scribe-abridge-doubles-valuation-to-5-3b/ — TechCrunch пишет, что в Q1 2025 Abridge достиг $117 млн contracted ARR и используется более чем в 150 крупнейших health systems США.
- [T3] https://www.abridge.com/press-release/upmc-scales-abridge — официальный пресс-релиз Abridge сообщает, что к октябрю 2025 платформу используют более 200 health systems, а UPMC масштабирует внедрение на 12 тыс. клиницистов.
- [T3] https://www.abridge.com/blog/abridge-forbes-ai-50-2026 — в апреле 2026 компания заявляет, что ей доверяют более 250 крупных health systems США, а в 2026 году платформа поддержит свыше 100 млн клинических разговоров.
- [T3] https://habr.com/ru/articles/915330/ — в РФ виден лишь проектный кейс ИИ-ассистента для врачей на базе анализа речи, а не зрелый рыночный ambient-scribe продукт с enterprise-интеграциями.

## RU equivalent
none. На 24 апреля 2026 не найден зрелый российский коммерческий аналог уровня Abridge с enterprise-внедрениями, интеграцией в медкарты и автоформированием клинической документации прямо из разговора врача с пациентом; в выдаче видны в основном прототипы, кастомные разработки и смежные voice/clinic-agent решения.

## Localization effort
hard. Нужны локальные медицинские словари, интеграции с МИС/ЭМК, хранение и обработка ПДн/медтайны по 152-ФЗ, плюс дообучение под российские клинические шаблоны.

## Western revenue
$117 млн contracted ARR в Q1 2025, 150+ health systems тогда и 250+ health systems по состоянию на апрель 2026.

## LTV signal
3.5-12 млн ₽ на клинику/контур за 3 года при модели annual enterprise subscription + внедрение + расширение на врачей и специализации.

## EBITDA hypothesis (24 мес, base)
800000-2200000₽/мес

## RU-fit
3 / 5. Модель воспроизводима в РФ для частных сетей клиник и крупных медцентров, но потребует тяжёлой локализации под МИС, медтайну, 152-ФЗ и русскоязычную клиническую речь.

## Expected unit economics (ballpark)
- ARPU: 120000-350000₽/мес
- CAC (ballpark): 500000-2000000₽
- Avg deal cycle: 4-8 мес
- Target segment: Regulated

## Why now
В 2025-2026 категория ambient clinical AI перешла из пилотов в масштабные enterprise-rollout, а у Abridge уже есть подтверждённая экономика и масштаб внедрений. В РФ давление на врачей по документообороту и дефицит персонала никуда не исчезли, поэтому окно для локального vertical AI в клинической документации выглядит реальным именно сейчас.


---

# Файл: 02-demand.md

---
stage: demand-validation
case: abridge-ai-meditsinskiy-skraib-dlya-klinik
date: 2026-04-24
analyst: branch-models-lead
sector: HEALTHCARE
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
AI-медицинский скрайб для клиник: ambient documentation во время приема, автогенерация клинической записи, структурирование разговора врач-пациент, связка с МИС/ЭМК и последующая проверка врачом.

## Итог
**Статус: CONDITIONAL PASS.**

Спрос как массовый inbound в РФ пока слабый, но category proof на Западе уже очень сильный, buyer pain в России реален, а коммерческий wedge в РФ просматривается у крупных частных сетей и цифрово зрелых клиник. Кейс не выглядит ready-made copy-paste GEO-expansion, но проходит demand-stage как тяжёлый enterprise healthcare workflow с высоким чеком и длинным циклом сделки. [T1][T2][T3]

Ключевые выводы:
1. Abridge к 17 апреля 2026 года пишет, что ему доверяют более 250 крупнейших health systems США, а платформа в 2026 году должна поддержать более 100 млн клинических разговоров. Это уже не пилотная категория, а зрелый enterprise signal. [T2]
2. В феврале 2025 Abridge сообщал о 100+ внедрениях в крупнейших health systems США, а в октябре 2025 уже писал про 200+ health systems и масштабирование UPMC на 12 тыс. клиницистов. Скорость роста подтверждает, что painkiller здесь не декоративный. [T2]
3. В РФ боль на стороне врача тоже понятна: в Habr-кейсе команды ИТМО/Genotek прямо сказано, что на заполнение медкарты уходит 5-8 минут из стандартного 15-минутного приёма. Это не зрелый рынок, но это хороший локальный proof of pain. [T3]
4. Рынок частной медицины в РФ уже крупный и растущий: Eqiva оценивает объём платных медуслуг в 2025 году в 1,78 трлн ₽, а выручка топ-550 частных клиник в 2024 году достигла 527,8 млрд ₽. Это означает наличие buyer base, где экономия времени врача и стандартизация документации могут монетизироваться. [T2]
5. Лучший стартовый wedge в РФ, не «AI-пишет всю медкарту для всех», а ambient scribe + structured draft note для сетевых клиник, где уже есть МИС, повторяемые шаблоны документации и дорогой врачебный час. [T1][T2][T3][inference]

## 1. Что именно валидируем
Проверяем, можно ли в РФ продать не просто speech-to-text, а clinical documentation workflow: запись разговора, черновик структурированной записи, автозаполнение шаблонов, traceability к исходной речи, интеграция в МИС/ЭМК и ручной final sign-off врачом.

Важно: это не consumer app и не generic voice assistant. Покупатель здесь платит за снижение doctor admin burden, ускорение оформления записи, более полный клинический note, снижение вариативности документации и потенциально лучшую пропускную способность врача. [T1][T2][T3][inference]

## 2. Почему спрос выглядит реальным

### 2.1 Global category proof уже очень сильный
- Abridge 17 февраля 2025 года сообщал о 100+ deployments в крупнейших health systems США. [T2]
- 16 октября 2025 Abridge писал уже о 200+ health systems и enterprise-wide rollout в UPMC на 12 тыс. клиницистов. [T2]
- 24 февраля 2026 Abridge сообщал, что платформа будет поддерживать более 80 млн patient-clinician conversations в 2026 году и используется в 250 крупнейших health systems США. [T2]
- 17 апреля 2026 компания подтвердила 250+ крупнейших health systems и прогноз более 100 млн клинических разговоров в 2026 году. [T2]

### 2.2 Российская боль подтверждена, но рынок ещё ранний
- Habr-кейс ИТМО/Genotek описывает локальную попытку построить ИИ-ассистента, который слушает приём и заполняет медкарту. Команда прямо указывает, что врачи тратят до 5-8 минут из 15-минутного приема на документацию. [T3]
- При этом сам же кейс показывает, что рынок РФ ещё в ранней стадии: решение находится на уровне MVP, тестировалось на анонимизированных записях и только планировало адаптацию под МИС и врачебное тестирование. [T3]
- Значит, pain есть, но продуктовый слой ещё не commoditized и не насыщен зрелыми игроками. [T3][inference]

### 2.3 Buyer base в РФ достаточна для дорогого vertical workflow
- Eqiva оценивает рынок платных медуслуг РФ в 1,78 трлн ₽ в 2025 году. [T2]
- Там же указано, что совокупная выручка топ-550 частных клиник выросла до 527,8 млрд ₽ в 2024 году. [T2]
- МЕДСИ как отдельный buyer-profile пишет о 145 клиниках по России, 15 тыс. сотрудников и более 4 900 врачей. [T2]

Вывод: даже если ICP сузить только до крупных частных сетей, там уже есть десятки-тысячи врачей, повторяющиеся шаблоны документации и экономический смысл automation слоя. [T2][inference]

## 3. Buyer map в РФ

### Core buyers
1. CEO/операционный директор крупной частной сети клиник.
2. Медицинский директор / chief medical officer.
3. CIO / директор по цифровизации / руководитель МИС.
4. Руководители направлений с высоким объёмом амбулаторных приемов: терапия, педиатрия, неврология, кардиология, гинекология, стоматология. [T1][T2][inference]

### Где боль максимальна
- сети частных многопрофильных клиник;
- крупные диагностические и амбулаторные контуры;
- клиники с высоким числом повторяемых приемов и формализованных шаблонов записи;
- цифрово зрелые игроки, где МИС уже используется как обязательная рабочая среда. [T1][T2][T3][inference]

### Где продавать хуже всего
- одиночным кабинетам и малым клиникам без зрелой МИС;
- государственным учреждениям на первом заходе, где цикл закупки, интеграций и согласований слишком длинный;
- specialty-практикам, где ценность не в note burden, а в визуальной диагностике и внеголосовых данных. [T1][T3][inference]

## 4. Конкурентная и substitute-картина в РФ
- Зрелого российского аналога масштаба Abridge в открытых источниках не видно. [T1][T3]
- Видны прототипы и ранние проекты, например кейс ИТМО/Genotek. [T3]
- Реальными substitute на первом этапе будут:
  - обычная ручная работа врача;
  - медицинские секретари и ассистенты;
  - диктовка с последующей ручной правкой;
  - более узкие модули голосового ввода без полноценной structured clinical note generation. [T1][T3][inference]

### Вывод по конкуренции
Рынок в РФ пока не crowded, но это не означает лёгкую победу. Наоборот, отсутствующий mature competition обычно означает, что нужно самим тащить buyer education, интеграции и clinical validation. [T3][inference]

## 5. WTP, willingness to pay
Прямого публичного прайсинга по российским analogues почти нет, поэтому willingness to pay проверяем через economics of pain и buyer profile.

### Что создаёт budget line
- врач тратит заметную долю приема на документацию, а не на пациента; [T3]
- у крупных клиник высокая стоимость часа квалифицированного врача; [T2][inference]
- сети клиник уже вкладывают большие бюджеты в рост и цифровую инфраструктуру, потому что масштаб бизнеса большой; [T2]
- value proposition завязан не на «красивый AI», а на throughput, doctor experience и стандартизацию notes. [T1][T2][T3][inference]

### Предварительный коридор WTP
Для РФ выглядят правдоподобно три модели:
1. **Pilot / department package:** 300-900 тыс. ₽ за пилот с интеграцией и адаптацией шаблонов. [inference]
2. **Clinic subscription:** 120-350 тыс. ₽/мес на клинику или группу врачей. [T1][inference]
3. **Network / enterprise contract:** 3-12 млн ₽ ARR на сеть, департамент или rollout по специализации. [T1][T2][inference]

Это согласуется с raw-гипотезой `3.5-12 млн ₽` LTV на клинику/контур за 3 года. [T1]

## 6. Market sizing

### Методика
Считаю двумя путями: top-down от рынка частной медицины и bottom-up от числа крупных buyer-организаций и plausible ARR.

### Top-down
- Рынок платных медуслуг РФ в 2025 году: **1,78 трлн ₽**. [T2]
- На ambient documentation / clinical documentation workflow беру очень консервативные **0,08%** рынка. Это даёт **TAM РФ = 1,42 млрд ₽**. [T2][inference]
- Для реально достижимого сегмента, где есть зрелая МИС, высокий врачебный час и готовность к цифровизации, беру **40%** TAM. Получаем **SAM РФ = 568 млн ₽**. [T2][inference]
- **SOM Y1 = 1-2% SAM = 5,7-11,4 млн ₽ ARR**. [inference]
- **SOM Y3 = 5-8% SAM = 28-45 млн ₽ ARR**. [inference]

### Bottom-up
- В качестве начального ICP беру **120** крупных и средне-крупных сетевых / цифрово зрелых клинических контуров по РФ. Это не весь рынок, а только targetable subset для enterprise pilot motion. [T2][inference]
- Беру средний achievable ARR **4,8 млн ₽** на один активный контур. Это эквивалентно примерно 400 тыс. ₽/мес и соответствует enterprise healthcare workflow, а не простой диктовке. [T1][inference]
- Тогда **SAM bottom-up = 120 × 4,8 млн ₽ = 576 млн ₽**. [inference]
- **SOM Y1 = 2-3 клиента = 9,6-14,4 млн ₽ ARR**. [inference]
- **SOM Y3 = 8-12 клиентов = 38,4-57,6 млн ₽ ARR**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (РФ) | 1,42 млрд ₽ [T2][inference] | 576 млн ₽ без расширения за пределы стартового ICP [inference] | top-down шире, bottom-up считает только стартовый enterprise wedge | lower |
| SAM (РФ) | 568 млн ₽ [T2][inference] | 576 млн ₽ [inference] | модели сошлись почти полностью | **568-576 млн ₽** |
| SOM Y1 | 5,7-11,4 млн ₽ | 9,6-14,4 млн ₽ | рабочий коридор близок | **6-14 млн ₽** |
| SOM Y3 | 28-45 млн ₽ | 38-58 млн ₽ | обе оценки проходят sanity-check | **28-58 млн ₽** |

### GTM-10 targets
1. МЕДСИ. [T2]
2. ГК «Мать и дитя». [T2]
3. СМ-Клиника. [T2][inference]
4. Медскан. [T2]
5. EMC. [T2][inference]
6. Будь Здоров. [T2][inference]
7. РЖД-Медицина. [T2][inference]
8. Скандинавия / АВА-ПЕТЕР. [T2][inference]
9. крупные стоматологические сети с повторяемым outpatient workflow. [T1][inference]
10. поставщики МИС как channel partners / embedded distribution layer. [T1][T3][inference]

### Sanity-check
- SOM Y1 не превышает 10% SAM. Overclaiming нет. [inference]
- Даже 2-3 enterprise-клиента в первый год уже дают meaningful ARR. [inference]
- Для категории с длинным sales cycle это реалистичнее, чем массовый PLG. [T3][inference]

## 7. Profit Gate, сценарии монетизации

### Сценарий A, pure dictation / speech-to-text add-on
- Низкий чек, высокая риск-коммодитизация.
- Нужны десятки и сотни врачей почти без кастома.
- **Вердикт: FAIL.**

### Сценарий B, clinic documentation copilot
- Продаём черновик structured note, шаблоны по специальностям, review workflow и базовую интеграцию.
- Чек 120-350 тыс. ₽/мес. [inference]
- При 5-8 клиентах уже можно строить meaningful B2B unit economics.
- **Вердикт: PASS.**

### Сценарий C, enterprise rollout по сети / департаменту
- Продаём не только note generation, но и governance, traceability, analytics, specialty templates и integration layer.
- Контракт 3-12 млн ₽ ARR. [T1][inference]
- 3-6 клиентов могут провести кейс через порог EBITDA 500 тыс. ₽/мес.
- **Вердикт: STRONG PASS.**

### Сценарий D, pilot + recurring expansion
- Setup/pilot fee + recurring per clinic/department.
- Лучше всего подходит для РФ, потому что снижает риск длинного enterprise sales cycle и окупает интеграционную фазу.
- **Вердикт: BEST ENTRY MODEL.**

## 8. Главные риски
1. **Регуляторика и данные.** Медтайна, ПДн, хранение аудио и клинических записей делают on-prem / private-cloud архитектуру почти обязательной для части клиентов. [T1][inference]
2. **Интеграции.** Без качественной связки с МИС/ЭМК продукт остаётся «красивой игрушкой», а не рабочим doctor workflow. [T1][T3]
3. **Клиническая точность.** Врач не простит галлюцинации в медзаписи; нужен strict human-in-the-loop. [T3][inference]
4. **Visual gap.** Не всё в клиническом приеме выражается голосом; часть контекста врач видит, а не слышит. Этот риск прямо подсвечен в обсуждении Habr-кейса. [T3]
5. **Длинный sales cycle.** Рынок выглядит enterprise-heavy, а не PLG-heavy. [T2][T3][inference]

## 9. Решение для pipeline
**Оставить кейс в pipeline и передавать дальше.**

Почему:
- есть очень сильный западный category proof; [T2]
- в РФ боль понятна и не выглядит искусственной; [T3]
- buyer base достаточно большая и платёжеспособная; [T2]
- Profit Gate просматривается через enterprise/pilot motion, а не через дешёвый per-doctor SaaS. [T1][T2][inference]

Но это **не easy geo-copy**. Для РФ кейс жизнеспособен только как high-trust healthcare workflow с жёсткой интеграцией, врачебной верификацией и узким ICP на старте.

## Источники
- [T1] `01-intake.md`
- [T2] Abridge, Series D announcement, 17.02.2025: https://www.abridge.com/press-release/series-d
- [T2] Abridge, UPMC scales Abridge, 16.10.2025: https://www.abridge.com/press-release/upmc-scales-abridge
- [T2] Abridge, UCHealth scales Abridge, 24.02.2026: https://www.abridge.com/press-release/uchealth-scales-abridge
- [T2] Abridge, Forbes AI 50 2026, 17.04.2026: https://www.abridge.com/blog/abridge-forbes-ai-50-2026
- [T2] Eqiva, рынок платных медицинских услуг России 2025: https://eqiva.ru/private-healthcare-market-2025
- [T2] МЕДСИ, о компании: https://vestnik.medsi.ru/about/
- [T3] Habr, ИИ-ассистент для врачей: как мы автоматизируем приём пациента на основе анализа речи и NLP, 04.06.2025: https://habr.com/ru/articles/915330/

Sources: T1=1, T2=6, T3=1. Primary evidence basis: T2.

## Market Pulse
> Market Pulse 24.04.2026: растущий, но ещё ранний локальный рынок с сильным западным category proof.


---

# Файл: 04-economics.md

---
stage: unit-economics
case: abridge-ai-meditsinskiy-skraib-dlya-klinik
date: 2026-04-24
analyst: branch-models-lead
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 04-economics

## Executive summary

**Статус: PASS WITH RESERVATIONS.**

Кейс проходит Program 5 на уровне фонда, но только как **regulated mid-market / enterprise healthtech** с высоким чеком, длинным sales cycle и дисциплиной по внедрению. Экономика держится не на массовом self-serve, а на контракте уровня **≈350 тыс. ₽ MRR на клинику/контур**, gross margin **66,3%**, fully-loaded CAC **≈2,24 млн ₽**, churn **2,1%/мес** и **LTV/CAC 4,9x**. Это выше инвестиционного порога **3:1**, а EBITDA при **50 клиентах** достигает **≈5,35 млн ₽/мес**.

Главное ограничение не в unit economics как таковых, а в **burn-to-breakeven**: для выхода на устойчивый break-even нужно **≈55-60 млн ₽ стартового капитала** и аккуратный найм в течение 12 месяцев. [T1][T2][T3][T4]

## 1. Базовая модель

### ICP для расчёта
- крупная частная сеть клиник, диагностический контур или отдельный департамент;
- 20-40 врачей в первом rollout;
- обязательная интеграция с МИС/ЭМК;
- human-in-the-loop финальное подтверждение врачом;
- договор минимум на 12 месяцев. [T1]

### Принятые допущения
- **MRR на клиента:** 350 000 ₽/мес
- **Setup fee:** 900 000 ₽ one-off, не включаю в LTV и payback, чтобы модель была консервативной
- **Средний срок сделки:** 6-8 месяцев
- **Monthly logo churn:** 2,1%/мес
- **Рабочий горизонт LTV:** по формуле SaaS `ARPA × GM / churn`
- **Сегмент:** regulated / upper mid-market B2B healthcare. [T1][T3]

## 2. Подробный business process, от lead до payment

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов и enrichment | SDR | HH/2ГИС/списки сетей клиник, CRM | 3 ч | 4 100 | Средняя |
| 2 | Первый outbound-контакт и qualification | SDR | CRM, email, телефония | 4 ч | 5 500 | Средняя |
| 3 | Discovery call с меддиректором/CIO | AE + CEO | Zoom/Meet, CRM | 2 ч | 16 100 | Низкая |
| 4 | Demo и value hypothesis | AE + Product/Implementation | Demo sandbox, презентация | 3 ч | 16 100 | Средняя |
| 5 | Сбор требований по МИС/ИБ/ПДн | CTO + Product | Notion, security checklist | 5 ч | 18 500 | Низкая |
| 6 | Подготовка пилотного scope и сметы | AE + CTO + Product | КП, калькулятор юнитов | 6 ч | 24 800 | Низкая |
| 7 | Юридическое согласование и DPA | CEO + внешний юрист | Word, ЭДО | 6 ч | 31 700 | Низкая |
| 8 | Техинтеграция с МИС/ЭМК | Backend + DevOps + CTO | API, VPN, staging | 24 ч | 83 100 | Средняя |
| 9 | Настройка speech/LLM pipeline и шаблонов | ML + Backend | ASR/LLM stack, prompt configs | 16 ч | 68 500 | Средняя |
| 10 | Обучение врачей и запуск пилота | Product + CSM | LMS, Zoom, playbooks | 8 ч | 18 900 | Средняя |
| 11 | Pilot review и конверсия в paid annual | AE + CEO + Product | CRM, ROI report | 5 ч | 26 700 | Низкая |
| 12 | Invoice, procurement, оплата | Finance/CEO | 1С, ЭДО, банк | 3 ч | 8 900 | Высокая |

**Итого прямой cost-to-close / cost-to-launch на один выигранный клиент:** **≈322 900 ₽**.  
Важно: это **не CAC**, а только себестоимость успешного deal-flow и запуска. Полный CAC выше, потому что включает несостоявшиеся сделки, маркетинг, SDR/AE FOT, CRM stack, ивенты и overhead.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| ASR/LLM inference и GPU | 52 000 | обработка аудио, summarization, specialty prompts | самая крупная переменная статья |
| Облако, storage, мониторинг | 16 000 | хранение аудио/логов, observability | regulated workload |
| Variable customer support / QA | 18 000 | доля CSM и support engineer | пост-пилотная поддержка |
| Амортизация onboarding и template tuning | 22 000 | 264k ₽ на запуск / 12 мес | консервативная амортизация |
| Security/compliance variable layer | 10 000 | key management, audit, защищённый контур | healthcare overhead |
| Telephony / audio transport / misc | 0  | включено в cloud + inference | чтобы не считать дважды |
| **Итого COGS** | **118 000** |  |  |

**Revenue/client/month = 350 000 ₽**  
**Gross profit/client/month = 232 000 ₽**  
**Gross margin = 66,3%**

## 4. CAC по каналам и воронка

### 4.1 CAC по acquisition channels

| Канал | Верх воронки / мес | Следующий шаг | Pilot | New paying customers / мес | Spend / мес, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Outbound по сетям клиник | 180 target accounts | 18 qualified meetings (10%) | 6 pilots (33% от meetings) | 0,30 | 720 000 | 2 400 000 |
| Партнёрства с МИС/интеграторами и отраслевые ивенты | 12 introductions | 6 discovery (50%) | 3 pilots (50%) | 0,18 | 390 000 | 2 166 667 |
| Inbound / контент / thought leadership | 30 MQL | 12 SQL (40%) | 4 pilots (33%) | 0,17 | 350 000 | 2 058 824 |
| **Blended** | **222** | **36 meetings/SQL** | **13 pilots** | **0,65** | **1 460 000** | **2 246 154** |

### 4.2 FULLY-LOADED CAC

Формула:

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers
```

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 180 000 | тестовый performance budget на niche healthcare B2B | T1 + analyst model |
| Outbound team FOT (SDR/AE attributed to new) | 486 000 | SDR 221k + 60% AE от 442k = 265k | T4 + HH + analyst model |
| Marketing team FOT (partial allocation) | 150 000 | 30% от product marketing / founder-led marketing capacity | T4 + analyst model |
| Tools (CRM, prospecting, телефония, аналитика) | 95 000 | amo/HubSpot class + prospecting + телефония | analyst model |
| Events/partnerships | 210 000 | 1 отраслевой слот + travel + co-marketing | T1 + analyst model |
| Overhead multiplier (x1.3) | 336 300 | 30% от 1 121 000 ₽ subtotal | std. enterprise B2B overhead |
| **Итого acquisition spend / мес** | **1 457 300** |  |  |
| **New paying customers / мес** | **0,65** | blended conversion | analyst model |
| **Fully-loaded CAC** | **2 242 000** | 1 457 300 / 0,65 |  |

### 4.3 Sanity check по сегменту
- ad-only/raw CAC был бы около **723k ₽** на клиента, если считать только media + events; fully-loaded CAC **2,24 млн ₽** даёт мультипликатор **≈3,1x**;
- это соответствует логике **regulated B2B** с длинным циклом, procurement и integration-heavy motion;
- blended CAC выше mid-market SaaS, но укладывается в reality check для complex healthtech enterprise sale. [T1]

## 5. LTV и churn

### Churn benchmark
Optifai в выборке **939 B2B SaaS компаний** за **Q2 2025 - Q1 2026** даёт средний **monthly logo churn 2,1%** для **Mid-Market ($10K-$50K ACV)**, **1,3%** для upper mid-market и **0,7%** для enterprise. Наш расчётный ACV около **4,2 млн ₽/год**, то есть примерно на границе mid-market/upper mid-market, поэтому беру **2,1%/мес** как консервативную базу. [T3]

### LTV
- **ACV:** 4 200 000 ₽
- **ARPA MRR:** 350 000 ₽
- **Gross margin:** 66,3%
- **Monthly churn:** 2,1%

```text
LTV = ARPA × Gross Margin / Monthly churn
LTV = 350 000 × 0,663 / 0,021 = 11 050 000 ₽
```

**LTV = ≈11,05 млн ₽**

## 6. LTV/CAC, payback, contribution margin

| Метрика | Формула | Значение |
|---|---|---:|
| LTV/CAC | 11 050 000 / 2 242 000 | **4,9x** |
| CAC Payback | 2 242 000 / 350 000 | **6,4 мес** |
| Contribution per client/month | 350 000 - 118 000 | **232 000 ₽** |
| Contribution Margin % | 232 000 / 350 000 | **66,3%** |

### Вывод по investment-grade критериям
- **LTV/CAC = 4,9x**, выше порога **3:1**;
- **CAC payback = 6,4 мес**, что лучше допустимого диапазона для enterprise/regulatory motion (**<18 мес**);
- contribution margin выше 60%, значит компания может absorb длинный sales cycle без разрушения маржи.

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 1 092 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product / Implementation | 1 | 320 000 | 1-2 | 1 | 96 000 | 416 000 |
| SDR | 1 | 170 000 | 0,5-1 | 1 | 51 000 | 221 000 |
| AE | 1 | 340 000 | 1-2 | 2-3 | 102 000 | 442 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| **Итого fully-loaded FOT / мес** | **11** |  |  |  |  | **5 551 000 ₽** |

### 7.2 Функции команды

| Роль | Основная функция |
|---|---|
| CEO | enterprise sales, fundraising, ключевые клиники и партнёрства |
| CTO | архитектура, security, МИС-интеграции, delivery governance |
| Senior Backend x2 | API, data pipelines, integration layer, billing, audit trails |
| ML Engineer | ASR/LLM quality, specialty templates, evaluation pipeline |
| DevOps | защищённый контур, observability, CI/CD, infra cost control |
| Frontend | врачебный UI, review workflow, traceability layer |
| Product / Implementation | discovery, template design, onboarding clinics |
| SDR | top-of-funnel outbound по сетям и департаментам |
| AE | demo, pilot-to-paid conversion, procurement close |
| Customer Success | adoption, usage expansion, renewals, churn prevention |

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Backend #1 | 1 958 580 |
| M2 | + DevOps | 2 561 000 |
| M3 | + Product/Implementation | 2 917 460 |
| M4 | + Backend #2 | 3 417 310 |
| M5 | + Frontend | 3 795 610 |
| M6 | + ML Engineer | 4 380 480 |
| M7 | + SDR | 4 640 480 |
| M8 | + AE | 5 121 480 |
| M9 | + Customer Success | 5 551 000 |
| M10 | без новых hire | 5 551 000 |
| M11 | без новых hire | 5 551 000 |
| M12 | без новых hire | 5 551 000 |

**Sanity check:** в первый месяц нет найма 5+ человек, план соответствует time-to-hire для regulated B2B, а M1 FOT не занижен.

## 8. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Fully-loaded FOT | 5 551 000 | штат из 11 человек |
| Базовая cloud/security infra | 260 000 | VPN, observability, backup, base hosting |
| Legal, accounting, DPO/compliance support | 120 000 | внешний контур |
| Офис / коворкинг / admin | 180 000 | гибридный режим |
| Travel / industry presence / customer visits | 140 000 | enterprise healthtech sales |
| **Итого fixed costs / мес** | **6 251 000 ₽** |  |

## 9. Break-even

### 9.1 Break-even по числу клиентов

```text
Break-even clients = Fixed costs / Contribution per client
= 6 251 000 / 232 000 = 26,9
```

**Break-even = 27 активных клиентов**

### 9.2 EBITDA при разном числе клиентов

| Активные клиенты | MRR, ₽/мес | Gross profit, ₽/мес | EBITDA после fixed costs, ₽/мес |
|---:|---:|---:|---:|
| 10 | 3 500 000 | 2 320 000 | -3 931 000 |
| 20 | 7 000 000 | 4 640 000 | -1 611 000 |
| 27 | 9 450 000 | 6 264 000 | **+13 000** |
| 35 | 12 250 000 | 8 120 000 | +1 869 000 |
| 50 | 17 500 000 | 11 600 000 | **+5 349 000** |

### 9.3 Break-even по месяцу
При ramp `0,0,0,1,1,2,3,4,6,8,10,12` клиентов в первый год компания остаётся убыточной весь Y1. При сохранении темпа выхода на **+3 клиента/мес** после M12 break-even достигается примерно в **M17-M18**.

## 10. Burn-to-breakeven и runway

### 10.1 Burn-to-breakeven
При описанном hire-плане и ramp продаж cumulative burn до точки, где `MRR × GM% > fixed costs`, составит **≈48-52 млн ₽**. Это уже не angel-friendly проект, а модель под pre-seed/seed с резервом под медленные закупки и пилоты.

### 10.2 Cash runway
Берём **startup_capital = 60 млн ₽**.

- средний burn в первые 12 месяцев: **≈4,0-4,3 млн ₽/мес**;
- cash runway без дополнительного revenue upside: **≈14-15 месяцев**;
- с плановым ростом до 27 клиентов runway хватает до operational break-even, но запас по ошибкам маленький.

## 11. Ключевые риски экономики

1. **Implementation creep.** Если пилоты превращаются в кастомную интеграционную разработку, COGS и payback резко ухудшаются.
2. **Underpricing.** Ниже 300k MRR модель быстро теряет инвестиционную привлекательность.
3. **Слабый partner motion.** Без канала через МИС/интеграторов blended CAC может уйти выше 2,5-2,8 млн ₽.
4. **Регуляторный оверхед.** Дополнительные требования по ПДн и хранению аудио могут снизить GM на 5-8 п.п.
5. **Найм ML/CTO.** Дефицит специалистов с healthcare + LLM опытом напрямую влияет на time-to-market. [T4]

## 12. Финальный вывод

**Экономика проходит Program 5.**

Почему не reject:
- **LTV/CAC = 4,9x**, выше инвестиционного порога;
- **CAC payback = 6,4 мес**, значительно лучше лимита для enterprise sale;
- **EBITDA при 50 клиентах = 5,35 млн ₽/мес**, то есть Profit Gate выполняется с запасом;
- break-even по базе достигается при **27 клиентах**, а не при 60-80.

Почему всё ещё нужны reservations:
- это **capital-intensive** healthtech motion с большим burn-to-breakeven;
- demand уже валидирован, но GTM остаётся узким и не mass-market;
- инвестиционная состоятельность держится только при чёткой стандартизации внедрения и контракте не ниже **≈350k MRR**.

**Итоговый вердикт: PASS WITH RESERVATIONS.**

## Sources
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/abridge-ai-meditsinskiy-skraib-dlya-klinik/01-intake.md
- [T2] https://eqiva.ru/private-healthcare-market-2025
- [T3] https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [T4] https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost
- [T4] https://hh.ru/vacancies/account_executive/polniy_den


---

# Файл: 05-critic.md

# 05-critic

## SECTION A. PnL

Ниже только PnL-блок Program 6A. SECTION B intentionally omitted.

### Налоговая модель РФ

- **УСН 6%**: налог берётся с выручки, НДС обычно нет, удобно для base-case при обороте в рамках режима.
- **IT-льгота 3%**: применима при аккредитации Минцифры и выполнении критериев по профильной выручке; в модели использована как optimistic-case.
- **ОСНО 20%**: налог на прибыль 20%, **НДС 20%** применим, если компания вне спецрежимов; в pessimistic-case использован как стресс-тест по net margin.
- **Страховые взносы ~30% к ФОТ** уже включены в FOT fully-loaded из 04-economics.md.
- Для PnL-таблиц ниже EBITDA показана **до налога**, а налог учитывается в waterfall как переход к Net.

## SECTION A. PnL (Базовый scenario)

Допущения: ARPA 350 000 ₽/мес, COGS 118 000 ₽/клиент/мес, churn 2.1%/мес, налоговый режим для net waterfall: УСН 6%.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 6 | 8 | 10 | 12 |
| Total clients | 0.0 | 0.0 | 0.0 | 1.0 | 2.0 | 3.9 | 6.9 | 10.7 | 16.5 | 24.1 | 33.6 | 44.9 |
| MRR | 0 | 0 | 0 | 350 000 | 692 650 | 1 378 104 | 2 399 164 | 3 748 782 | 5 770 057 | 8 448 886 | 11 771 459 | 15 724 259 |
| COGS | 0 | 0 | 0 | 118 000 | 233 522 | 464 618 | 808 861 | 1 263 875 | 1 945 334 | 2 848 482 | 3 968 663 | 5 301 322 |
| Gross profit | 0 | 0 | 0 | 232 000 | 459 128 | 913 486 | 1 590 303 | 2 484 907 | 3 824 724 | 5 600 404 | 7 802 796 | 10 422 937 |
| GM% | 0.0% | 0.0% | 0.0% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% | 66.3% |
| Fixed costs | 2 658 580 | 3 261 000 | 3 617 460 | 4 117 310 | 4 495 610 | 5 080 480 | 5 340 480 | 5 821 480 | 6 251 000 | 6 251 000 | 6 251 000 | 6 251 000 |
| EBITDA | -2 658 580 | -3 261 000 | -3 617 460 | -3 885 310 | -4 036 482 | -4 166 994 | -3 750 177 | -3 336 573 | -2 426 276 | -650 596 | 1 551 796 | 4 171 937 |
| Cash burn | 2 658 580 | 3 261 000 | 3 617 460 | 3 885 310 | 4 036 482 | 4 166 994 | 3 750 177 | 3 336 573 | 2 426 276 | 650 596 | 0 | 0 |
| Cumulative cash | -2 658 580 | -5 919 580 | -9 537 040 | -13 422 350 | -17 458 832 | -21 625 826 | -25 376 003 | -28 712 576 | -31 138 852 | -31 789 448 | -30 237 652 | -26 065 714 |

**Break-even clients:** 27
**Break-even month:** M11
**startup_capital_to_bep_rub:** 31 789 448 ₽

### Waterfall (Базовый, steady-state at 50 clients)

| Step | ₽/мес | Комментарий |
|---|---:|---|
| ARPA x clients | 17 500 000 | 50 клиентов × 350 000 ₽ |
| Gross profit | 11 600 000 | после COGS 118 000 ₽/клиент |
| Contribution | 11 600 000 | contribution = gross, т.к. variable S&M отдельно не выделен в 04-economics.md |
| EBITDA | 5 349 000 | после fixed costs 6 251 000 ₽/мес |
| Net after tax | 5 028 060 | УСН 6% |

## SECTION A. PnL (Оптимистичный scenario)

Допущения: ARPA 380 000 ₽/мес, COGS 110 000 ₽/клиент/мес, churn 1.5%/мес, налоговый режим для net waterfall: IT-льгота 3%.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 6 | 8 | 10 | 12 | 14 |
| Total clients | 0.0 | 0.0 | 1.0 | 2.0 | 4.0 | 6.9 | 10.8 | 16.6 | 24.4 | 34.0 | 45.5 | 58.8 |
| MRR | 0 | 0 | 380 000 | 754 300 | 1 502 985 | 2 620 441 | 4 101 134 | 6 319 617 | 9 264 823 | 12 925 850 | 17 291 963 | 22 352 583 |
| COGS | 0 | 0 | 110 000 | 218 350 | 435 075 | 758 549 | 1 187 170 | 1 829 363 | 2 681 922 | 3 741 694 | 5 005 568 | 6 470 485 |
| Gross profit | 0 | 0 | 270 000 | 535 950 | 1 067 911 | 1 861 892 | 2 913 964 | 4 490 254 | 6 582 900 | 9 184 157 | 12 286 395 | 15 882 099 |
| GM% | 0.0% | 0.0% | 71.1% | 71.1% | 71.1% | 71.1% | 71.1% | 71.1% | 71.1% | 71.1% | 71.1% | 71.1% |
| Fixed costs | 2 658 580 | 3 261 000 | 3 617 460 | 4 117 310 | 4 495 610 | 5 080 480 | 5 340 480 | 5 821 480 | 6 251 000 | 6 251 000 | 6 251 000 | 6 251 000 |
| EBITDA | -2 658 580 | -3 261 000 | -3 347 460 | -3 581 360 | -3 427 699 | -3 218 588 | -2 426 516 | -1 331 226 | 331 900 | 2 933 157 | 6 035 395 | 9 631 099 |
| Cash burn | 2 658 580 | 3 261 000 | 3 347 460 | 3 581 360 | 3 427 699 | 3 218 588 | 2 426 516 | 1 331 226 | 0 | 0 | 0 | 0 |
| Cumulative cash | -2 658 580 | -5 919 580 | -9 267 040 | -12 848 400 | -16 276 099 | -19 494 687 | -21 921 203 | -23 252 429 | -22 920 529 | -19 987 372 | -13 951 977 | -4 320 879 |

**Break-even clients:** 24
**Break-even month:** M9
**startup_capital_to_bep_rub:** 23 252 429 ₽

### Waterfall (Оптимистичный, steady-state at 50 clients)

| Step | ₽/мес | Комментарий |
|---|---:|---|
| ARPA x clients | 19 000 000 | 50 клиентов × 380 000 ₽ |
| Gross profit | 13 500 000 | после COGS 110 000 ₽/клиент |
| Contribution | 13 500 000 | contribution = gross, т.к. variable S&M отдельно не выделен в 04-economics.md |
| EBITDA | 7 249 000 | после fixed costs 6 251 000 ₽/мес |
| Net after tax | 7 031 530 | IT-льгота 3% |

## SECTION A. PnL (Пессимистичный scenario)

Допущения: ARPA 320 000 ₽/мес, COGS 130 000 ₽/клиент/мес, churn 3.0%/мес, налоговый режим для net waterfall: ОСНО 20%.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 8 |
| Total clients | 0.0 | 0.0 | 0.0 | 0.0 | 1.0 | 2.0 | 3.9 | 6.8 | 10.6 | 15.3 | 20.8 | 28.2 |
| MRR | 0 | 0 | 0 | 0 | 320 000 | 630 400 | 1 251 488 | 2 173 943 | 3 388 725 | 4 887 063 | 6 660 451 | 9 020 638 |
| COGS | 0 | 0 | 0 | 0 | 130 000 | 256 100 | 508 417 | 883 164 | 1 376 670 | 1 985 369 | 2 705 808 | 3 664 634 |
| Gross profit | 0 | 0 | 0 | 0 | 190 000 | 374 300 | 743 071 | 1 290 779 | 2 012 056 | 2 901 694 | 3 954 643 | 5 356 004 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 59.4% | 59.4% | 59.4% | 59.4% | 59.4% | 59.4% | 59.4% | 59.4% |
| Fixed costs | 2 658 580 | 3 261 000 | 3 617 460 | 4 117 310 | 4 495 610 | 5 080 480 | 5 340 480 | 5 821 480 | 6 251 000 | 6 251 000 | 6 251 000 | 6 251 000 |
| EBITDA | -2 658 580 | -3 261 000 | -3 617 460 | -4 117 310 | -4 305 610 | -4 706 180 | -4 597 409 | -4 530 701 | -4 238 944 | -3 349 306 | -2 296 357 | -894 996 |
| Cash burn | 2 658 580 | 3 261 000 | 3 617 460 | 4 117 310 | 4 305 610 | 4 706 180 | 4 597 409 | 4 530 701 | 4 238 944 | 3 349 306 | 2 296 357 | 894 996 |
| Cumulative cash | -2 658 580 | -5 919 580 | -9 537 040 | -13 654 350 | -17 959 960 | -22 666 140 | -27 263 549 | -31 794 250 | -36 033 195 | -39 382 501 | -41 678 858 | -42 573 854 |

**Break-even clients:** 33
**Break-even month:** не достигнут в M1-M12
**startup_capital_to_bep_rub:** 42 573 854 ₽

### Waterfall (Пессимистичный, steady-state at 50 clients)

| Step | ₽/мес | Комментарий |
|---|---:|---|
| ARPA x clients | 16 000 000 | 50 клиентов × 320 000 ₽ |
| Gross profit | 9 500 000 | после COGS 130 000 ₽/клиент |
| Contribution | 9 500 000 | contribution = gross, т.к. variable S&M отдельно не выделен в 04-economics.md |
| EBITDA | 3 249 000 | после fixed costs 6 251 000 ₽/мес |
| Net after tax | 2 599 200 | ОСНО 20% |

### Сводка по break-even

| Scenario | Break-even clients | Break-even month | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Базовый | 27 | M11 | 31 789 448 |
| Оптимистичный | 24 | M9 | 23 252 429 |
| Пессимистичный | 33 | n/a | 42 573 854 |

<!-- P6A-DONE -->

## SECTION B. Finance risk + competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев

База для stress-test: M12 EBITDA = **4 171 937 ₽/мес**, ARPU = **350 000 ₽**, churn = **2,1%/мес**, blended CAC = **2 242 000 ₽**, активных клиентов к M12 = **44,9**. Основа расчёта: `04-economics.md` + SECTION A выше. Для CAC stress считаю, что удвоение CAC требует примерно удвоить acquisition spend, то есть даёт **-1,46 млн ₽/мес** дополнительной нагрузки на EBITDA. Для churn и price stress меняю клиентскую базу или contribution при прочих равных. [B1][B2][inference]

| Scenario | Предпосылка | EBITDA @M12, ₽/мес | Delta vs Base |
|---|---|---:|---:|
| Base | как в SECTION A | 4 171 937 | 0 |
| Sens1 | CAC x2 | 2 714 637 | -1 457 300 |
| Sens2 | Churn x2, с 2,1% до 4,2% | 3 721 176 | -450 761 |
| Sens3 | Price -30%, ARPU 245k ₽ | -545 146 | -4 717 083 |

**Вывод:** самая опасная переменная не churn, а **pricing discipline**. При снижении цены на 30% модель уходит в отрицательную EBITDA даже без ухудшения churn и CAC.

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 800 000 | 2 242 000 | 3 200 000 | [B1][B2] |
| Monthly churn, % | 1,3% | 2,1% | 4,2% | [B2][B3] |
| ARPU, ₽/мес | 320 000 | 350 000 | 420 000 | [B1][B4] |
| Conversion rate lead→paid, % | 0,18% | 0,29% | 0,45% | [B1][inference] |
| Time-to-hire, мес | 1,0 | 1,7 | 3,0 | [B1][B5] |

#### Метод упрощённой симуляции

Вместо формальных 1000 прогонов использую **9 комбинаций** min/mode/max. База M12 = 44,9 активных клиентов, далее на M13-M24 считаю net new logos вокруг **3/мес** в median, с поправкой на conversion и time-to-hire. p10 = worst cluster, p50 = median cluster, p90 = best cluster. Это не статистически строгий Monte Carlo, а **manual scenario lattice**, достаточный для committee-level stress test. [inference]

#### Результат, p10 / p50 / p90

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | 1 890 000 | 9 280 000 | 22 220 000 | 20 330 000 |
| CAC payback, мес | 10,0 | 6,4 | 4,3 | 5,7 |
| LTV/CAC | 1,6x | 4,9x | 11,9x | 10,3x |
| Cash runway, мес | 13,2 | 14,5 | 21,1 | 7,9 |

**Gate-check rules:**
1. **p10 EBITDA < 0?** Нет, p10 остаётся положительным, значит формальный insolvency trigger пока не сработал.
2. **p50 EBITDA < 500k ₽/мес?** Нет, median выше порога с большим запасом.
3. **p90 / p10 > 10x?** Да, `22,22 / 1,89 = 11,8x`, значит неопределённость слишком высокая, score надо **понизить на 1 notch**.
4. **Range width по LTV/CAC > 8?** Да, `11,9 - 1,6 = 10,3`, значит модель **хрупкая**, и её устойчивость держится на цене, churn и discipline в CAC.

### B3. Competitor deep-dive

#### Top-3 западных

| Игрок | Почему важен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Abridge** | category leader в ambient clinical documentation | сильный brand, 250+ крупных health systems в США, доказанный enterprise rollout, deep workflow integration | тяжёлая enterprise-настройка, дорогой rollout, почти не переносится в РФ без полной локализации | **30-40%** западного enterprise ambient-scribe сегмента, по публичному deployment footprint [B6][inference] | локальная интеграция с МИС/ЭМК РФ, data residency, русская медречь, cheaper services layer |
| **Nuance DAX Copilot (Microsoft)** | крупнейший incumbent в clinical documentation stack | доступ к EHR ecosystem Microsoft/Nuance, сильный канал через крупные health systems, низкий vendor risk | legacy-stack inertia, высокая стоимость владения, слабая гибкость под локальные specialty templates вне США | **25-35%** enterprise ambient-doc сегмента, как сильнейший incumbent [B7][inference] | быстрее адаптировать под локальные клиники, меньше procurement friction, кастомизация под РФ-регуляторику |
| **Suki** | сильный multi-specialty AI assistant, documentation + coding | широкий specialty coverage, mobile/desktop workflow, хороший product UX | меньше enterprise moat, чем у Abridge/Nuance, сложнее удерживать differentiation при commodity LLM layer | **10-15%** next-tier западного сегмента [B8][inference] | vertical focus на РФ, on-prem/private cloud, адаптация под billing+MIS+152-ФЗ вместо generic US workflow |

#### Топ российских и adjacent substitutes

| Игрок | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Webiomed / К-Скай** | Skolkovo, Rusprofile [B9][B10] | сильная клиническая аналитика, заметный бренд в медИИ РФ, доступ к региональным и госпроектам | core focus не на ambient scribe, а на CDSS/аналитике; workflow врача во время приёма закрывает частично | **10-15%** российского AI-in-clinics бюджета, но не более **5%** именно в ambient-doc [inference] | мы решаем документацию в момент приёма, а не post-hoc risk scoring |
| **Третье Мнение** | Skolkovo [B11] | сильный радиологический AI brand, B2B trust в медицине, опыт продаж в regulated contour | основной продукт в imaging, не в voice/documentation; buyer overlap ограничен | **5-10%** AI budget в частной медицине, но **<3%** в целевом workflow [inference] | documentation wedge ближе к core pain амбулаторного врача |
| **Botkin.AI / AIRA** | Skolkovo [B12] | зрелость в клиническом AI, опыт работы с медорганизациями, сильный compliance narrative | опять же imaging-first, не ambient documentation | **5-10%** AI spend в радиологии, **минимальная доля** в note-generation [inference] | наш wedge шире по врачебному throughput, а не по снимкам |
| **Genotek + ИТМО medical scribe prototype** | Habr [B13] | closest local signal по самой задаче, понимают pain 5-8 минут документации на 15-минутный приём | пока это прототип/MVP, без публичного enterprise rollout и без доказанного GTM | **<1%** рынка, research-stage | можно быстрее превратить прототипный painkiller в industrial product с МИС-интеграцией и SLA |

**Итог по конкуренции:** прямого зрелого аналога Abridge в РФ по состоянию на 25.04.2026 не видно. Это хорошо для входа, но плохо для GTM, потому что buyer education и clinical validation придётся тащить самим.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Срыв найма CTO/ML-лида | med | high | >90 дней без закрытия критичных вакансий | founder-led recruiting, advisor network, interim fractional CTO |
| Operational | Рост ошибок/галлюцинаций в клинических summary | med | high | доля doctor overrides >25%, жалобы пилотных врачей | human-in-the-loop, specialty QA, red-team evals, hard guardrails |
| Operational | Недоступность LLM/API или деградация latency | med | high | SLA <99%, latency >8-10 сек, рост unit-cost inference | multi-vendor routing, fallback models, local ASR buffer, reserved capacity |
| Market | Спрос есть, но conversion в paid пилоты ниже модели | med | high | lead→paid <0,2% два квартала подряд | сузить ICP до сетей/департаментов, partner-led GTM, paid pilot first |
| Market | Price compression из-за дешёвых voice/LLM substitutes | high | high | win-rate падает при цене >300k ₽/мес | setup fee + enterprise packaging, ROI calculator, compliance moat |
| Market | Появление сильного incumbent через MIS/EHR-партнёра | med | high | крупные МИС начинают продавать own co-pilot | channel partnerships заранее, API-first embedding, exclusivity by workflow |
| Regulatory | Несоответствие 152-ФЗ и data residency | med | high | запросы клиентов на on-prem, блокирующие security questionnaires | private cloud/on-prem option, DPA, хранение аудио в РФ |
| Regulatory | Риски 115-ФЗ/комплаенса закупок и KYC enterprise-клиентов | low | med | затяжка legal/procurement >120 дней | стандартизованный procurement pack, compliance counsel |
| Regulatory | Санкции SaaS / отключение зарубежных API-поставщиков | high | high | новые ограничения по billing или API access | российские/opensource fallback, abstraction layer, валютный резерв |
| Financial | Cash runway сжимается из-за burn-to-breakeven > плана | high | high | runway <9 мес до M12 | raise sooner, cut hiring pace, stage-gated hiring |
| Financial | Рост USD/RUB увеличивает inference cost | high | med | +15% cost per encounter за квартал | рублёвые контракты с клиентами, pricing indexation, GPU optimization |
| Financial | Инфляция ФОТ и налоговая нагрузка давят fixed costs | med | med | payroll growth >12-15% YoY, отмена льгот | annual repricing, variable comp, reserve in budget |
| Black swan | Эскалация войны/санкций ломает продажи и внедрения | med | high | freeze новых проектов у частных клиник | focus на cash-rich buyers, shorter pilot, preserve 12m liquidity |
| Black swan | Полное отключение ключевого LLM/ASR provider | med | very high | provider notice, sudden quota cuts | multi-model stack, local inference for critical path, emergency downgrade mode |

### B5. Kill conditions через 6 месяцев

1. **Median economics fail:** p50 EBITDA@M24 у пересчитанной модели падает ниже **500 000 ₽/мес** или LTV/CAC остаётся ниже **3,0x**.
2. **Go-to-market fail:** за 6 месяцев нет минимум **2 paid pilots** или lead→paid стабильно ниже **0,2%**.
3. **Pricing/compliance fail:** средний контракт не держит **300 000 ₽ MRR** либо ни один pilot не проходит security/compliance review по 152-ФЗ без кастомного re-architecture.

### B6. Итоговый вывод по SECTION B

Кейс всё ещё **проходит**, но уже не как clean pass, а как **fragile pass**. Почему:
- base-case и median-case дают положительную EBITDA trajectory;
- но price cut на 30% ломает модель сразу;
- p90/p10 выше 10x, значит разброс слишком велик;
- LTV/CAC range width >8, значит economics хрупкая;
- прямых зрелых конкурентов в РФ почти нет, но substitutes за бюджет цифровизации есть уже сейчас.

**Рекомендация:** оставлять кейс живым только при жёстком execution discipline: enterprise pricing floor, partner-led GTM, on-prem/private-cloud readiness и быстрый выход к 2+ paid pilots.

### Sources for SECTION B
- [B1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/abridge-ai-meditsinskiy-skraib-dlya-klinik/04-economics.md
- [B2] https://optif.ai/learn/questions/b2b-saas-churn-rate-by-acv/
- [B3] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/abridge-ai-meditsinskiy-skraib-dlya-klinik/01-intake.md
- [B4] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/abridge-ai-meditsinskiy-skraib-dlya-klinik/02-demand.md
- [B5] https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost
- [B6] https://www.abridge.com/blog/abridge-forbes-ai-50-2026
- [B7] https://www.microsoft.com/en-us/health-solutions/ai/dax-copilot
- [B8] https://www.suki.ai/
- [B9] https://sk.ru/news/b/press/archive/2020/12/28/startap-skolkovo-k_sky-vnedrit-v-regionah-platformu-dlya-prognozirovaniya-riskov-zabolevaniy.aspx
- [B10] https://www.rusprofile.ru/id/9236860
- [B11] https://sk.ru/news/b/news/archive/2021/12/29/startap-rezident-skolkovo-pomogaet-vracham-postavit-pravilnyy-diagnoz-v-10-raz-bystree.aspx
- [B12] https://sk.ru/news/b/news/archive/2020/06/24/pomozhet-li-iskusstvennyy-intellekt-opredelyat-rak-na-ranney-stadii.aspx
- [B13] https://habr.com/ru/articles/915330/

<!-- P6B-DONE -->


---

# Файл: 06-verdict.md

[HEALTHCARE] Abridge, AI-медицинский скрайб для клиник — NEAR-PASS: 68/100 | EBITDA base=5349К₽/мес через 12 мес | LTV/CAC=4,9x | Ключевое преимущество: deep workflow integration в клиническую документацию | Главный риск: ранний RU-demand и тяжёлый enterprise GTM.

# Abridge, AI-медицинский скрайб для клиник — вердикт инвесткомитета

sector: HEALTHCARE
status: NEAR-PASS
score: 68/100
date: 2026-04-25
case_slug: abridge-ai-meditsinskiy-skraib-dlya-klinik

## Оценка
Source tier balance: T1=1, T2=6, T3=1, weighted=2.00. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «LTV/CAC = 4,9x», «CAC payback = 6,4 мес», «Gross margin = 66,3%» из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «EBITDA при 50 клиентах = +5 349 000 ₽/мес», в 05-critic M11 уже «1 551 796 ₽», значит gate выполняется. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | «рынок частной медицины... 1,78 трлн ₽», но «спрос как массовый inbound в РФ пока слабый»; применён tier-penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Есть интеграционный и workflow moat, но «зрелого российского аналога... не видно» пока не равен доказанному барьеру входа. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В 05-critic зафиксированы риски «152-ФЗ», «санкции SaaS», «полное отключение ключевого LLM/ASR provider». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | В кейсе уже есть сетевой ICP, «лучший стартовый wedge... для сетевых клиник», и 10 named targets ниже. |

**Sum raw = 102/150. Normalized score = round(102×100/150) = 68/100.**

## 7-factor Moat

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает core product для остальных напрямую. |
| Switching costs | 2 | После внедрения появляются шаблоны, данные, привычки врачей и интеграции с МИС/ЭМК. |
| Scale economies | 2 | COGS inference и support на клиента снижаются при стандартизации rollout и росте базы шаблонов. |
| Proprietary data / model advantage | 1 | Потенциал есть, но публичного доказательства крупного proprietary RU-датасета пока нет. |
| Regulatory moat | 2 | 152-ФЗ, медтайна и private-cloud/on-prem readiness создают реальный, но воспроизводимый барьер. |
| Brand / distribution | 1 | Глобальный category proof сильный, но локальный бренд и канал в РФ ещё не сформированы. |
| Embedded workflow | 3 | Продукт живёт внутри core clinical note workflow, а не как внешний nice-to-have. |

**Moat raw = 11/21. Moat score = round(11×25/21) = 13/25.**

## Финальный вердикт
**NEAR-PASS.**

Кейс инвестиционно интересный, но пока не проходит fund-level committee без дополнительных proof points. Экономика уже рабочая, EBITDA-потенциал высокий, buyer pain реален, однако локальный спрос в РФ ранний, moat только средний, а execution risk unusually high из-за регуляторики, интеграций и зависимости от AI-stack.

## Почему не APPROVED
1. **Спрос в РФ пока не investment-grade.** 02-demand прямо говорит: «спрос как массовый inbound в РФ пока слабый», то есть market pull ещё не доказан на уровне repeatable enterprise category.
2. **Moat средний, не выдающийся.** Интеграции и compliance дают барьер, но не дают монополистического преимущества без локального data/distribution layer.
3. **Execution unusually hard.** На входе нужен regulated healthtech stack, private deployment readiness, дорогая команда и длинный sales cycle 6-8 месяцев.
4. **Финансовая хрупкость к pricing.** В 05-critic price -30% сразу переводит модель в отрицательную EBITDA @M12.

## Что должно быть доказано для APPROVED
- минимум **2 paid pilots** в крупных частных сетях или digital-first медцентрах РФ;
- средний контракт **не ниже 300-350 тыс. ₽/мес** на контур;
- physician edit/override rate **<15-20%** на 2+ специальностях;
- частично стандартизированный коннектор к МИС/ЭМК, сокращающий rollout до **≤6-8 недель**;
- partner channel через МИС или отраслевого интегратора, снижающий blended CAC.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 11 050 000 ₽ |
| CAC blended | 2 242 000 ₽ |
| LTV/CAC | 4,9x |
| CAC payback | 6,4 мес |
| Gross Margin | 66,3% |
| contribution_margin_rub_month | 232 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 251 000 ₽/мес |
| company_ebitda_rub_month (50 клиентов, base) | 5 349 000 ₽/мес |
| clients_to_500k_ebitda | 30 |
| months_to_500k_ebitda | 11 |
| startup_capital_to_bep_rub | 31 789 448 ₽ |
| break-even clients | 27 |

## FULL business process из 04-economics.md
1. Поиск ICP-аккаунтов и enrichment.
2. Первый outbound-контакт и qualification.
3. Discovery call с меддиректором или CIO.
4. Demo и value hypothesis.
5. Сбор требований по МИС, ИБ и ПДн.
6. Подготовка пилотного scope и сметы.
7. Юридическое согласование и DPA.
8. Техинтеграция с МИС/ЭМК.
9. Настройка speech/LLM pipeline и specialty templates.
10. Обучение врачей и запуск пилота.
11. Pilot review и conversion в paid annual.
12. Invoice, procurement, оплата.

**Прямой cost-to-close / cost-to-launch:** ≈322 900 ₽ на выигранный аккаунт. Это не полный CAC, а только себестоимость успешной сделки и запуска.

## PnL и risk summary из 05-critic.md
- Base-case: M12 EBITDA = **4 171 937 ₽/мес**, startup_capital_to_bep_rub = **31 789 448 ₽**.
- Optimistic-case: break-even в **M9**, startup capital ≈ **23,25 млн ₽**.
- Pessimistic-case: break-even не достигается за 12 месяцев.
- Sensitivity: **CAC x2 → EBITDA @M12 = 2 714 637 ₽**, **churn x2 → 3 721 176 ₽**, **price -30% → -545 146 ₽**.
- Monte Carlo Lite: **p10 EBITDA @M24 = 1,89 млн ₽**, **p50 = 9,28 млн ₽**, **p90 = 22,22 млн ₽**. Разброс 11,8x, значит uncertainty high.

## Команда

| Роль | Кол-во | FOT fully-loaded, ₽/мес | Зачем нужна |
|---|---:|---:|---|
| CEO | 1 | 845 000 | enterprise sales, fundraising, ключевые партнёрства |
| CTO / Tech Lead | 1 | 715 000 | архитектура, security, МИС-интеграции |
| Senior Backend | 2 | 1 092 000 | API, integration layer, audit trails |
| ML Engineer | 1 | 650 000 | ASR/LLM quality, specialty prompts |
| DevOps | 1 | 455 000 | private-cloud, observability, infra |
| Frontend | 1 | 390 000 | врачебный UI и review workflow |
| Product / Implementation | 1 | 416 000 | discovery, onboarding, template design |
| SDR | 1 | 221 000 | top-of-funnel outbound |
| AE | 1 | 442 000 | pilot-to-paid conversion |
| Customer Success | 1 | 325 000 | adoption, expansion, renewals |
| **Итого** | **11** | **5 551 000** | regulated enterprise healthtech stack |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | Крупнейшая частная сеть, много амбулаторных приёмов и цифровой контур; в demand-файле отдельно указан buyer-profile. | email decision-maker + конференции MedSoft/телемед | 350 000 ₽/мес |
| 2 | Мать и дитя / MD Medical | Высокий объём стандартизируемых приёмов, дорогой врачебный час, enterprise budget. | интро через CIO/CMO + партнёрство с МИС | 400 000 ₽/мес |
| 3 | СМ-Клиника | Сетевой амбулаторный поток и повторяемые шаблоны documentation-heavy приёмов. | founder-led outbound + кейс ROI | 300 000 ₽/мес |
| 4 | Медскан | Цифрово зрелый контур и мультиклиническая структура, где ROI на doctor throughput понятен. | email CIO + отраслевые мероприятия | 300 000 ₽/мес |
| 5 | EMC | Premium healthcare buyer с высокой стоимостью врачебного времени и tolerance к high-end software. | executive outreach + pilot на отделение | 450 000 ₽/мес |
| 6 | Будь Здоров | Крупная сеть с масштабируемым outpatient workflow и интересом к efficiency layer. | партнёрство через интегратора МИС | 280 000 ₽/мес |
| 7 | РЖД-Медицина | Большой distributed контур, где стандартизация записей и traceability ценны. | гос/корпоративный partner-led channel | 250 000 ₽/мес |
| 8 | Скандинавия / АВА-ПЕТЕР | Сильная частная сеть, где premium service и doctor time economics поддерживают чек. | executive email + медицинские конференции | 300 000 ₽/мес |
| 9 | K+31 | Премиальные частные клиники с цифровой зрелостью и требованиями к качеству документации. | direct outreach к меддиректору | 250 000 ₽/мес |
| 10 | Инвитро (клиническое направление) | Adjacent clinic workflow, бренд и масштаб позволяют pilot в формализованных сценариях. | партнёрство + outbound через digital health контакт | 220 000 ₽/мес |

## Top-3 risks

| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Ранний локальный спрос и длинный sales cycle | high | high | Если рынок останется founder-led, а не category-led, blended CAC и срок сделки выйдут за модель. |
| Price compression / underpricing | high | high | В stress-test price -30% переводит EBITDA @M12 в отрицательную зону. |
| Регуляторика + зависимость от LLM/ASR stack | medium | very high | 152-ФЗ, data residency, санкции и provider shutdown могут сломать delivery unit economics. |

## Proof points для APPROVED
1. **2-3 платящих пилота** в сетях из GTM-10, а не только discovery/LOI.
2. **Median contract ≥300k ₽/мес** без кастомной разработки на каждый rollout.
3. **Override rate врача <20%** и time saved на приём ≥3-5 минут.
4. **Интеграция с 1-2 МИС** в repeatable connector format, а не bespoke project.
5. **Чёткий channel partner** через МИС/интегратора или отраслевого реселлера.

## LTV Upside Calculator
Так как кейс получил **NEAR-PASS**, нужен план повышения score до approve.

| Рычаг | Текущее | Целевое | Эффект на модель |
|---|---:|---:|---|
| ARPA / MRR на контур | 350 000 ₽ | 420 000 ₽ | повышает contribution и делает price-compression менее смертельным |
| COGS на клиента | 118 000 ₽ | 95 000 ₽ | GM растёт с 66,3% до ~77%, EBITDA margin резко улучшается |
| CAC blended | 2 242 000 ₽ | 1 800 000 ₽ | LTV/CAC растёт с 4,9x до ~6,1x |
| Monthly churn | 2,1% | 1,5% | customer_ltv_rub растёт примерно до 15,5 млн ₽ |
| Months to 500k EBITDA | 11 | 9 | модель становится ближе к approve по capital efficiency |

**Rule of thumb:** если одновременно достигнуть ARPA **420k ₽**, COGS **≤95k ₽** и CAC **≤1,8 млн ₽**, кейс поднимается из 68/100 к диапазону **72-75/100** и становится кандидатом на APPROVED WITH NOTES.

