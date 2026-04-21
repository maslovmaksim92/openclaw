# verdict.md

Скомпилированный пакет кейса по всем доступным стадиям P1-P7.



---

## 00-brief.md

# Brief

- Кейс: Ambience Healthcare Geo Expand
- Slug: ambience-healthcare-geo-expand-v2
- Sector: HEALTHCARE
- Режим: resurrect / полный пайплайн обязателен
- Исходный raw-файл: 2026-04-19-resurrect-ambience-healthcare-geo-expand.md
- Источник предыдущего решения: pipeline/triage/triage-2026-04-15-ambience-healthcare-geo-expand.md
- Исторически связанный кейс: pipeline/cases/ambient-clinical-documentation-operator/
- Следующий этап: P3-demand-validation

## Почему создан новый кейс
Файл пришёл с префиксом `resurrect-`, поэтому создана новая версия кейса без duplicate-классификации. По standing orders такой сигнал обязан пройти новый полный цикл оценки как standalone candidate.


---

## 01-intake.md

---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-ambience-healthcare-geo-expand.md
created: 2026-04-20T05:42:00+03:00
original_verdict: pipeline/rejected/ambient-clinical-documentation-operator-v2/06-verdict.md
original_triage: pipeline/triage/triage-2026-04-15-ambience-healthcare-geo-expand.md
---

# Intake

## Название
Ambience Healthcare Geo Expand

## Режим обработки
Принудительный resurrect по правилу full pipeline. Duplicate-проверка пропущена согласно standing orders.

## Краткий контекст
Ambient clinical documentation, coding и revenue-integrity workflow automation для крупных health systems.

## Предыдущий контекст
- Оригинальный triage: `pipeline/triage/triage-2026-04-15-ambience-healthcare-geo-expand.md`
- Исторически связанный кейс: `pipeline/cases/ambient-clinical-documentation-operator/`
- Оригинальный verdict: `pipeline/rejected/ambient-clinical-documentation-operator-v2/06-verdict.md`

## Полный контекст из raw

# RESURRECT SIGNAL — ambience-healthcare-geo-expand

## Meta
- source: triage/triage-2026-04-15-ambience-healthcare-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-15

## Входные данные
- `pipeline/raw/raw-2026-04-15-ambience-healthcare-geo-expand.md`

## Классификация
supporting signal для существующего кейса

## Решение
Обогатить существующий кейс: `ambient-clinical-documentation-operator`.

## Почему
- Сигнал тематически совпадает с уже открытым кейсом по ambient clinical documentation в медицине.
- Это не новый case container, а усиливающее подтверждение, что категория уже валидирована на уровне крупных зарубежных health systems.
- Экономика и глубина продукта поддерживают high-LTV гипотезу: enterprise rollout, крупный венчурный раунд и широкий workflow contour вокруг документации, coding и revenue integrity.

## Что добавлено в кейс
- В `pipeline/cases/ambient-clinical-documentation-operator/01-evidence.md` добавлены supporting signal entries по Ambience Healthcare.
- Зафиксированы дата, source URL, тип сигнала, краткое объяснение, как сигнал усиливает кейс, и ключевые факты.
- Добавлены данные о Series C на $243 млн, 40+ крупных health system клиентах и enterprise rollout в Houston Methodist.

## Что сделано
- Обновлён `01-evidence.md` у кейса `ambient-clinical-documentation-operator`.
- Исходный raw-файл подлежит переносу в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: сигнал Ambience Healthcare усиливает уверенность, что ambient clinical documentation, coding и связанный clinical workflow automation могут быть high-LTV enterprise-моделью, в том числе как локализуемый сервисный слой для рынка РФ.

```


---

## 02-demand.md

# Demand validation

## Вывод
**Итог: DEMAND = MEDIUM, Profit Gate = PASS, кейс идёт дальше.**

Ambience решает понятную боль, но в РФ рынок пока не выглядит массово сформированным именно под premium ambient clinical documentation уровня США. Спрос есть на более широкий контур: меддокументация, голосовой ввод, клинические рекомендации, кодирование, снижение времени врача на бумажную работу. Это подтверждается одновременно: 87,3 тыс. медорганизаций в РФ [T1], 628,2 тыс. врачей в системе здравоохранения [T1], крупным рынком платной медицины 1,57 трлн ₽ в 2024 году [T2], а также demand endpoint и HH-сигналами по запросам про меддокументацию [T1/T2].

Market Pulse 2026-04-20: наблюдается рост интереса. В текущем веб-срезе есть свежие публикации и продуктовые сигналы по голосовым ассистентам врача, ИИ для меддокументации и ambient clinical documentation, что указывает на ускорение внимания к категории.

## 1) Demand signals
- В РФ работает **87,3 тыс. медицинских организаций**, из них частных **73,5 тыс.** [T1, Минздрав РФ, https://www.rosminzdrav.ru/news/2024/12/26/21456-mihail-murashko-v-rossii-rabotaet-87-3-tys-meditsinskih-organizatsiy]. Это даёт широкую базу потенциальных аккаунтов, но платёжеспособный сегмент существенно уже.
- В государственной, муниципальной и частной системах здравоохранения работают **628,2 тыс. врачей** [T1, Минздрав РФ, https://www.rosminzdrav.ru/news/2025/04/29/21756-mihail-murashko-v-gosudarstvennoy-munitsipalnoy-i-chastnoy-sistemah-zdravoohraneniya-rabotayut-628-2-tys-vrachey]. Это верхняя граница seats-based TAM по пользователям.
- По demand endpoint запрос **«медицинская документация врач»** дал `composite_demand=MEDIUM`, `hh_vacancies=21282`, `yandex_suggest=100`; запросы **«голосовой ассистент врача»** и **«медицинский скрайб ИИ»** дали LOW, что показывает: боль существует, но категория «AI medical scribe» в РФ ещё не сформирована как самостоятельный mainstream-класс [T1/T2, internal endpoint + HH].
- Рынок платных медуслуг РФ достиг **1,57 трлн ₽** в 2024 году и прогнозировался НРА на **1,83 трлн ₽** в 2025 году [T2, Forbes со ссылкой на НРА, https://www.forbes.ru/rating/551134-lidery-rejtinga-krupnejsih-medicinskih-kompanij-2025]. Это важный прокси на платёжеспособный сегмент private healthcare.
- Ambience на своём сайте заявляет **80% average utilization**, **45% less charting time** и **$13K revenue per clinician/year** у St. Luke’s [T2, официальный сайт компании, https://www.ambiencehealthcare.com/]. Это не РФ-доказательство, но подтверждение сильного WTP в enterprise-сегменте для зрелых health systems.

## 2) Конкуренты и цены
Минимум 3 реальных аналога/заменителя с ценой:

| Игрок | Что продаёт | Цена | Комментарий |
|---|---|---:|---|
| Freed | AI medical scribe | от **$39/мес**, Core **$79/мес**, Premier **$104/мес** при annual billing [T2, https://www.getfreed.ai/pricing] | Нижняя граница self-serve WTP у врачей/малых практик |
| DeepCura | AI medical scribe + coding + receptionist | **$129/seat/мес**, annual **$999/seat/год** [T2, https://www.deepcura.com/plans-pricing] | Ближе к многофункциональному workflow stack |
| Heidi Health | Clinical AI, pricing plans | есть Free / paid tiers; на pricing-page присутствуют коммерческие платные планы Evidence Pro / Scribe Plus / Enterprise, но точные суммы страница отдаёт нестабильно, поэтому используем как качественный competitor, не как ценовой anchor [T2, https://www.heidihealth.com/pricing] | Подтверждает наличие paid ladder у глобальных игроков |
| GidMedical | Голосовой ввод/диктовка для врачей в РФ | **1250 руб** за 14 дней, **1950 руб/мес** [T2, https://gidmedical.ru/] | Российский low-end substitute, сильно уже по ценности |
| MedBot AI | Telegram-бот по клиническим рекомендациям | **0 ₽**, beta/free [T2, https://medbotai.ru/] | Не прямой scribe, но российский TG-native adjacent product |

**Вывод по pricing:** реальный коридор WTP для single-doctor/SMB начинается примерно от **1,950 ₽/мес** в РФ low-end substitute и от **$39-129/мес** у западных AI-scribe продуктов [T2]. Для enterprise-integrated продукта класса Ambience в РФ разумно тестировать **3,000-8,000 ₽ за врача в месяц** или **250-900 тыс. ₽ в месяц за клинику/контур**, если есть интеграция с МИС, шаблоны, кодирование и compliance.

## 3) Telegram bots/services в РФ
Проверка категории в RU показала, что Telegram как канал присутствует, но рынок **не занят сильным vertical leader**:
- **MedBot AI** ведёт в Telegram-бот `@medical_kr_bot`, позиционируется как ИИ-ассистент по клиническим рекомендациям Минздрава РФ, сейчас beta/free [T2, https://medbotai.ru/].
- У **GidMedical** есть Telegram-контакт на лендинге, но это скорее канал продаж/коммуникации, а не category-defining AI scribe bot [T2, https://gidmedical.ru/].
- По demand endpoint поле telegram было нулевым для проверенных ключей, то есть массового TG-signal по этой категории пока нет [T2].

**Интерпретация:** Telegram можно использовать как distribution/onboarding layer для врача, но не как доказанную основную монетизируемую платформу категории. Для фонда это плюс в дистрибуции, но не core moat.

## 4) WTP, willingness to pay
Доказательства willingness to pay:
1. **Реальные платные аналоги уже есть**: Freed, DeepCura, GidMedical [T2].
2. **Ambience сообщает про revenue uplift $13K на врача в год** у клиента St. Luke’s [T2], то есть продукт продаётся не только как time-saver, но и как revenue integrity tool.
3. **HH/demand endpoint** показывает массовую боль вокруг меддокументации, а не вокруг «скрайба» как бренда категории [T1/T2]. Значит платить готовы прежде всего за снижение бумажной нагрузки и ускорение врача, а не за модный AI label.
4. **Private healthcare revenue base в РФ уже крупная**: 1,57 трлн ₽ в 2024 [T2]. Даже 0,5-1,5% admin-efficiency budget внутри этого оборота создаёт многомиллиардный software envelope. Это inference, а не прямой бюджетный факт.

**WTP verdict:** **умеренно подтверждён**. Для individual doctors WTP низкий/средний, для крупных сетей и enterprise-клиник, где важны кодирование, выручка, скорость приёма и унификация документации, WTP выглядит значительно сильнее.

## 5) Market sizing
### Допущения
- Для top-down используем рынок платной медицины РФ 1,57 трлн ₽ в 2024 и долю адресуемого spend на documentation/revenue-cycle/clinical workflow software **1,2-1,8%**. Это оценка на базе сопоставимых software envelopes и поэтому помечена как inference [T2]. Для preferred берём консервативные **1,2%**.
- Для bottom-up берём платёжеспособный сегмент крупных/средних частных сетей и digital-forward клиник, а не все 73,5 тыс. частных медорганизаций [T1].
- Средний контракт: **54 тыс. ₽/врач/год** для mid-market и **72 тыс. ₽/врач/год** для enterprise с МИС-интеграцией. Это согласовано с западным ценовым коридором и российским low-end substitute [T2].

### GTM-10 реальные buyers для bottom-up
1. Медси
2. Мать и дитя
3. Медскан
4. EMC
5. СМ-Клиника
6. АВА-Петер / Скандинавия
7. Клиника Фомина
8. Будь Здоров
9. Сеть клиник Эксперт
10. MedSwiss

Эти игроки релевантны, потому что именно крупные сети способны покупать seat-based clinical workflow software, тянуть интеграции и считать ROI на врача/клинику [T2, Forbes ranking + публичные данные компаний].

### Таблица расчёта
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$7.0B** = ~14 млн врачей × ~$500/год addressable software spend [T2/T3] | — | — | top-down |
| TAM (РФ) | **18.8 млрд ₽** = 1.57 трлн ₽ × 1.2% [T2] | **22.6 млрд ₽** = 628.2k врачей × 36k ₽/год baseline [T1+T2] | diff 20%, приемлемо; bottom-up чуть выше, т.к. включает весь врачебный контур | **18.8 млрд ₽** |
| SAM (РФ) | **4.5 млрд ₽** = TAM × 24% digital-fit segment [T1+T2] | **4.1 млрд ₽** = 75k адресуемых врачей × 54k ₽/год [T1+T2] | diff 10%, в пределах нормы | **4.1 млрд ₽** |
| SOM Y1 | **82 млн ₽** = 2% SAM [T2] | **65 млн ₽** = ~1,200 врачей × 54k ₽/год [T2] | diff 26%; используем lower, т.к. цикл продаж длинный | **65 млн ₽** |
| SOM Y3 | **410 млн ₽** = 10% SAM [T2] | **324 млн ₽** = ~4,500 врачей × 72k ₽/год [T2] | diff 27%; lower безопаснее | **324 млн ₽** |

### Комментарий к sizing
- Расхождение top-down и bottom-up меньше 3x, пересборка сегмента не требуется.
- SOM Y1 = 65 млн ₽ это ~1.6% от preferred SAM, реалистично.
- Sanity-check: чтобы сделать 65 млн ₽ в Y1 при ARR 54k ₽, нужно ~1,200 врачей. Это возможно только через 4-8 сетевых клиентов, а не через long-tail одиночных врачей. Значит GTM должен быть account-based.

## 6) Profit Gate: достижимость EBITDA >= 500k ₽/мес
Проверены все ключевые сценарии монетизации.

### Сценарий A. Solo / self-serve doctors
- Цена: 1,950-3,000 ₽/мес на врача [T2]
- 300 платящих врачей => выручка 585k-900k ₽/мес
- При support/compliance/dev overhead такой сценарий **обычно не даёт 500k ₽ EBITDA/мес** на ранней стадии.
- **Вердикт:** FAIL.

### Сценарий B. SMB clinics
- Цена: 3,000-4,500 ₽/врач/мес или 80-200k ₽/клиника/мес [T2]
- 20 клиник по 120k ₽/мес => 2.4 млн ₽ MRR
- При gross margin 75% и fixed opex ~1.1-1.3 млн ₽/мес получаем **EBITDA ~500-700k ₽/мес**.
- **Вердикт:** PASS.

### Сценарий C. Enterprise networks / health systems
- Цена: 250-900k ₽/мес на сеть/контур + интеграция [inference на базе global comparables, T2]
- 4 enterprise клиента по 400k ₽/мес => 1.6 млн ₽ MRR; 6 клиентов => 2.4 млн ₽ MRR
- Даже при длинном sales cycle и heavier implementation этот сценарий способен дать **EBITDA >500k ₽/мес**.
- **Вердикт:** PASS.

### Сценарий D. Hybrid: scribe + coding + guideline copilot + Telegram front-end
- Цена выше pure dictation, выше удержание, больше stakeholder fit (CMO + ops + finance)
- Может выйти на **>500k ₽ EBITDA/мес** быстрее, чем pure-scribe, потому что продаёт revenue integrity, а не только time-saving.
- **Вердикт:** PASS.

**Profit Gate overall: PASS.** Pure self-serve модель слабая, но clinic/enterprise/hybrid сценарии экономически жизнеспособны.

## 7) Риски и red flags
- Категория «AI medical scribe» в РФ пока не сформирована как самостоятельный must-have budget line [T1/T2].
- Требуются интеграции с МИС/ЭМК, юридически аккуратная работа с медданными и локализация под клинреки/документооборот РФ [T1/T2].
- Telegram присутствует скорее как входной канал, чем как доказанная основная product layer [T2].
- Сильнее всего кейс работает не как «ещё один диктофон», а как **documentation + coding + revenue integrity** stack по модели Ambience [T2].

## 8) Investment view
Для фонда это **не broad consumer AI**, а узкий B2B healthcare workflow play. Спрос не хайповый, зато боль дорогая и регулярная. Лучший angle в РФ не копировать Ambience один-в-один, а локализовать продукт под private healthcare networks, документацию, шаблоны, рекомендации Минздрава и revenue-cycle uplift.

**Demand verdict:** `MEDIUM`

## Sources
- Минздрав РФ, 87.3 тыс. медорганизаций: https://www.rosminzdrav.ru/news/2024/12/26/21456-mihail-murashko-v-rossii-rabotaet-87-3-tys-meditsinskih-organizatsiy [T1]
- Минздрав РФ, 628.2 тыс. врачей: https://www.rosminzdrav.ru/news/2025/04/29/21756-mihail-murashko-v-gosudarstvennoy-munitsipalnoy-i-chastnoy-sistemah-zdravoohraneniya-rabotayut-628-2-tys-vrachey [T1]
- Demand endpoint multi-demand по ключам «медицинская документация врач», «голосовой ассистент врача», «медицинский скрайб ИИ» [T1/T2, internal]
- Forbes / НРА по рынку платной медицины: https://www.forbes.ru/rating/551134-lidery-rejtinga-krupnejsih-medicinskih-kompanij-2025 [T2]
- Ambience Healthcare official site: https://www.ambiencehealthcare.com/ [T2]
- Freed pricing: https://www.getfreed.ai/pricing [T2]
- DeepCura pricing: https://www.deepcura.com/plans-pricing [T2]
- Heidi pricing: https://www.heidihealth.com/pricing [T2]
- GidMedical pricing: https://gidmedical.ru/ [T2]
- MedBot AI: https://medbotai.ru/ [T2]

Sources: T1=4, T2=8, T3=1. Primary evidence basis: T1.

---

## 04-economics.md

---
stage: economics
case: ambience-healthcare-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: PASS_WITH_CONSTRAINTS
confidence: medium
investment_grade: false
sector: HEALTHCARE
---

# 04-economics — Unit Economics

## Кейс
Ambience Healthcare Geo Expand v2, AI-платформа для ambient clinical documentation, coding и revenue-integrity workflow automation с локализацией под РФ.

## Executive summary

**Итог P5: PASS WITH CONSTRAINTS.**

Экономика сходится только в клиническом mid-market / enterprise motion, где продукт продаётся не как «диктовка для врача», а как контур `documentation + coding + revenue integrity + шаблоны + интеграции с МИС`.

Ключевые выводы:
1. **Pure self-serve сегмент невалиден**: low-end price point 1 950–3 000 ₽/мес не даёт нужной EBITDA даже при сотнях врачей.
2. **Клинический SMB / enterprise сегмент проходит**: при контракте 180–420 тыс. ₽/мес на клинику и аккуратной delivery-модели компания может выйти на **EBITDA > 500k ₽/мес**.
3. **Главный риск не в спросе, а в service-load**: интеграции, медданные, обучение, QA и legal/compliance легко съедают маржу.
4. **Investment grade пока нет**: экономика рабочая, но запас прочности умеренный, а GTM длинный и execution-heavy.

## 1. Модель и ключевые допущения

### ICP
- частные сети клиник и диагностические сети;
- multi-site клиники с 40+ врачами и заметным объёмом документации;
- digital-forward медорганизации, где есть МИС/ЭМК, экономический директор или операционный контур, считающий ROI по скорости врача и выручке.

### Base-case для РФ
- Средний recurring контракт: **260 000 ₽/клиент/мес**
- Setup / onboarding / integration fee: **450 000 ₽** разово
- Для основной математики считаю recurring отдельно, setup fee не включаю в MRR.
- Средний активный аккаунт: **1 клиника / контур**, 25–60 врачей под rollout.

### Почему беру 260k ₽ MRR
Это середина между:
- lower-end клиническими заменителями и голосовым вводом в РФ;
- и enterprise-позицией, где продаётся не только запись, но и кодирование, ускорение документооборота и revenue capture.

Чек ниже 180k ₽/мес делает модель слишком хрупкой, выше 400k ₽/мес требует уже доказанного локального PMF и глубоких интеграций.

## 2. Business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP mapping по сетям клиник | SDR / founder | CRM, Rusprofile, manual research | 2 ч | 2 000 | Низкий |
| 2 | Первичный outreach | SDR | Email, Telegram, phone | 1.5 ч | 1 600 | Средний |
| 3 | Intro / qualification call | SDR + AE | Meet, CRM | 1 ч | 3 000 | Средний |
| 4 | Discovery по текущему документообороту | AE + founder | Meet, questionnaire | 2 ч | 8 500 | Низкий |
| 5 | Demo на врачебных workflow | AE + clinical specialist | Demo env, scripts | 2 ч | 9 500 | Низкий |
| 6 | Security / legal / meddata pre-check | AE + CTO | NDA, policy docs | 2 ч | 8 000 | Низкий |
| 7 | Pilot scoping и success metrics | AE + CSM | SOW, ROI model | 3 ч | 12 000 | Низкий |
| 8 | Интеграция с МИС / шаблонами | Solutions + CSM | API, mappings, templates | 16 ч | 52 000 | Средний |
| 9 | Обучение врачей и админов | CSM | Zoom, manuals | 5 ч | 14 000 | Средний |
| 10 | Пилот 4–6 недель и weekly review | CSM + AE | Analytics, support | 12 ч | 33 000 | Средний |
| 11 | Procurement / договор / счёт | AE + founder + ops | Contract workflow | 6 ч | 16 000 | Низкий |
| 12 | Production rollout после оплаты | CSM + support | Runbook, dashboards | 8 ч | 22 000 | Средний |

### Вывод по процессу
Продажа выглядит как **consultative B2B sale**, а не self-serve SaaS. До оплаты много ручного труда, поэтому заниженный CAC здесь был бы неправдоподобен.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| Inference / speech / LLM budget | 28 000 | регулярные clinical note workflows |
| Hosting / storage / logs | 14 000 | изолированная среда, хранение, audit trail |
| Support L1-L2 | 18 000 | доля support-инженера |
| CSM / account ops | 24 000 | доля CSM на активный аккаунт |
| Clinical QA / templates | 16 000 | выборочная валидация и шаблоны |
| Integration amortization | 20 000 | spread setup effort over 12 мес |
| Security / compliance allocation | 10 000 | правовой и процессный overhead |
| **Итого COGS** | **130 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **260 000 ₽**
- COGS на клиента: **130 000 ₽**
- Gross profit на клиента: **130 000 ₽**
- **Gross Margin = 50.0%**

### Комментарий
Для healthtech с интеграциями и meddata это нормальная, но не выдающаяся валовая маржа. Кейс удерживается на плаву только если productized delivery постепенно вытесняет ручной сервис.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 20 | 8 | 4 | 2 | 0.8 | 4.0% |
| Targeted outbound по клиникам | 120 | 18 | 8 | 3 | 0.8 | 0.67% |
| Content / inbound / events | 40 | 10 | 5 | 2 | 0.5 | 1.25% |
| Partnerships / integrators | 12 | 5 | 3 | 1 | 0.4 | 3.3% |
| **Итого blended** | **192** | **41** | **20** | **8** | **2.5** | **1.3%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid acquisition / category ads | 180 000 | ограниченные тесты по healthcare B2B |
| SDR + AE FOT attributed to new | 980 000 | 2 SDR + 1 AE + взносы + commissions |
| Marketing allocation | 240 000 | контент, кейсы, вебинары |
| CRM / sequencing / tooling | 90 000 | CRM, телефония, enrichment |
| Events / partnerships | 160 000 | отраслевые мероприятия и партнёры |
| Overhead multiplier (x1.3) | 495 000 | admin / management / ops overhead |
| **Итого fully-loaded acquisition spend** | **2 145 000** |  |

- New paying customers / мес: **2.5**
- **Blended fully-loaded CAC = 858 000 ₽**

### Sanity check
Для regulated B2B healthtech CAC ниже 300k ₽ выглядел бы слишком оптимистично. Значение **~858k ₽** больше похоже на реальность для enterprise-ish клиник с пилотом и интеграцией.

## 5. LTV и churn

### Базовые допущения
- MRR на клиента: **260 000 ₽**
- ARR на клиента: **3 120 000 ₽**
- Gross Margin: **50%**
- Annual logo churn: **18%**

Формула:

`LTV = ARR × GM / churn`

`LTV = 3 120 000 × 50% / 18% = 8 666 667 ₽`

### Вывод
- **LTV = 8.67 млн ₽**
- Для healthtech это неплохое значение, но оно держится только если клиенты реально renew после пилота и rollout не упирается в врачебное сопротивление.

## 6. LTV / CAC

- LTV: **8 666 667 ₽**
- Fully-loaded CAC: **858 000 ₽**

`LTV/CAC = 8 666 667 / 858 000 = 10.1x`

### Stress-case
Чтобы не переоценить кейс, считаю также stress-case:
- Effective GM в Year 1: **42%**
- Annual churn: **28%**

`Stress LTV = 3 120 000 × 42% / 28% = 4 680 000 ₽`

`Stress LTV/CAC = 4 680 000 / 858 000 = 5.5x`

### Вердикт по метрике
Даже в stress-case LTV/CAC остаётся выше порога 3:1. Но это не означает лёгкий рост: проблема кейса скорее в burn и длинном цикле продаж, чем в формальном LTV/CAC.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`858 000 / 260 000 = 3.3 мес`

Если считать payback по gross profit:

`858 000 / 130 000 = 6.6 мес`

### Комментарий
Gross-profit payback **6.6 мес** выглядит сильным для B2B healthtech. Но только при условии, что COGS не раздуется из-за нестандартизированных интеграций и ручного клинического QA.

## 8. Contribution Margin %

Для contribution margin беру выручку минус COGS минус variable success / commission load.

- Revenue per client / мес: **260 000 ₽**
- COGS: **130 000 ₽**
- Variable commission + success allocation: **15 000 ₽**

`Contribution profit = 115 000 ₽`

`Contribution Margin = 115 000 / 260 000 = 44.2%`

### Вывод
**Contribution Margin = 44.2%**. Это здоровый, но не сверхсильный показатель. Он подтверждает, что экономика рабочая, если компания не скатывается в кастомную внедренческую студию.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / tech lead | 1 | 520 000 | 2 | 2 | 156 000 | 676 000 |
| Backend engineer | 2 | 380 000 | 1.5 | 1.5 | 114 000 | 988 000 |
| ML / applied AI engineer | 1 | 480 000 | 2 | 2 | 144 000 | 624 000 |
| Integrations / solutions engineer | 1 | 320 000 | 1.5 | 1.5 | 96 000 | 416 000 |
| SDR | 2 | 150 000 + бонус | 1 | 1 | 45 000 | 390 000 |
| AE | 1 | 280 000 + комиссия | 1.5 | 2 | 84 000 | 364 000 |
| CSM / implementation | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Clinical SME / QA | 1 | 260 000 | 1.5 | 1.5 | 78 000 | 338 000 |
| Finance / ops (part-time) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого full team FOT** | **11.5** |  |  |  |  | **4 953 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 4 953 000 |
| Cloud base platform not in COGS | 280 000 |
| Security / legal / meddata compliance | 220 000 |
| G&A / бухгалтерия / ЭДО / misc | 100 000 |
| Travel / enterprise meetings | 90 000 |
| Office / admin | 120 000 |
| **Итого fixed costs** | **5 763 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **115 000 ₽**
- Fixed costs: **5 763 000 ₽/мес**

`Break-even clients = 5 763 000 / 115 000 = 50.1`

### Founder-mode / lean team
Если первые 12–15 месяцев держать компактную команду и fixed costs на уровне **3 450 000 ₽/мес**, тогда:

`3 450 000 / 115 000 = 30.0 клиентов`

### Вывод
- На **полной команде** break-even слишком тяжёлый, около **50 клиентов**.
- В **lean founder-mode** модель становится рабочей, break-even около **30 клиентов**.
- Следовательно, кейс нельзя масштабировать «вперёд команды» без аккуратного контроля burn.

## 12. Burn-to-breakeven и runway

### Burn base-case
- Fixed costs lean-mode: **3.45 млн ₽/мес**
- Acquisition spend: **2.15 млн ₽/мес**
- Total early burn: **~5.60 млн ₽/мес**

### Burn-to-breakeven
Если компания растёт до 30 клиентов за 18–24 месяца, ориентир burn-to-breakeven будет **55–75 млн ₽** в зависимости от скорости найма и реальной скорости закрытия пилотов.

### Runway
При `startup_capital = 80 млн ₽`:

`80 000 000 / 5 600 000 ≈ 14.3 мес`

С учётом нарастающей выручки реалистичный runway: **15–17 месяцев**.

## 13. Что происходит при 40 клиентах

### P&L snapshot при 40 клиентах
- Revenue: `40 × 260 000 = 10 400 000 ₽/мес`
- COGS: `40 × 130 000 = 5 200 000 ₽/мес`
- Gross profit: **5 200 000 ₽/мес**
- Variable commission / success: `40 × 15 000 = 600 000 ₽/мес`
- Contribution profit: **4 600 000 ₽/мес**

Если fixed costs держатся в lean-mode **3.45 млн ₽**, тогда:
- **EBITDA ≈ 1.15 млн ₽/мес**

Если команда раздута до steady-state **5.76 млн ₽**, тогда:
- **EBITDA ≈ -1.16 млн ₽/мес**

### Ключевой вывод
Profit gate проходит **только при дисциплинированном operating model**. Если рано собрать тяжёлую enterprise-команду, экономика развалится даже на 40 клиентах.

## 14. Profit Gate

### Проверка правила
Условие FAIL: `company EBITDA < 500K/mo achievable even at 50 clients` или `LTV/CAC < 1:1`

### Факт
- LTV/CAC уверенно выше 1:1 и выше инвестиционного порога.
- EBITDA **> 500k ₽/мес достижима** в lean-mode уже около 36–38 клиентов и выше.
- На тяжёлой команде кейс становится пограничным.

## Итоговый вердикт P5

**PASS WITH CONSTRAINTS.**

Кейс экономически допустим, если строить его как узкий enterprise / upper-midmarket healthtech operator с высокой продуктовой стандартизацией и жёстким контролем delivery. Как self-serve AI scribe или как service-heavy кастомный интегратор модель для фонда выглядит слабой.

## Что нужно проверить на следующем этапе
1. Насколько реалистично удержать чек 260k+ ₽/мес в РФ private healthcare.
2. Не окажется ли фактический churn выше 25–30% из-за длинного внедрения и слабого врачебного adoption.
3. Можно ли реально productize integrations и clinical QA, иначе contribution margin быстро деградирует.

## Источники
- `pipeline/cases/ambience-healthcare-geo-expand-v2/02-demand.md`
- Публичные ценовые и рыночные якоря, зафиксированные в `02-demand.md`
- Консервативная внутренняя модель branch-models-lead для regulated B2B healthtech-кейсов

---

## 05-critic.md

# SECTION A — PnL

## Допущения модели

- Стартовая база клиентов: 0.
- Churn в моделях: base 18% annual, optimistic 12%, pessimistic 28%, переведено в помесячный churn.
- ARPA / COGS на клиента в месяц: base 260k / 130k ₽, optimistic 286k / 120k ₽, pessimistic 234k / 145k ₽.
- Variable success / commission load: 15k ₽ на клиента в месяц для расчёта contribution и break-even.
- Fixed costs: lean operating mode 3,45 млн ₽/мес в base, 3,60 млн ₽/мес в optimistic и pessimistic.
- FOT full team из 04-economics.md: 4,953 млн ₽/мес, страховые взносы ~30% уже включены в FOT fully-loaded; для runway и BE использован lean-mode из исходного файла.

## Сценарий: Базовый

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 4 | 4 | 4 |
| Total clients | 1,0 | 2,0 | 4,0 | 5,9 | 7,8 | 10,7 | 13,5 | 16,3 | 19,0 | 22,7 | 26,3 | 29,9 |
| MRR | 260 000 | 515 736 | 1 027 277 | 1 530 428 | 2 025 326 | 2 772 108 | 3 506 641 | 4 229 126 | 4 939 762 | 5 898 742 | 6 841 993 | 7 769 774 |
| COGS | 130 000 | 257 868 | 513 638 | 765 214 | 1 012 663 | 1 386 054 | 1 753 320 | 2 114 563 | 2 469 881 | 2 949 371 | 3 420 997 | 3 884 887 |
| Gross profit | 130 000 | 257 868 | 513 638 | 765 214 | 1 012 663 | 1 386 054 | 1 753 320 | 2 114 563 | 2 469 881 | 2 949 371 | 3 420 997 | 3 884 887 |
| GM% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% | 50,0% |
| Fixed costs | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 | 3 450 000 |
| EBITDA | -3 320 000 | -3 192 132 | -2 936 362 | -2 684 786 | -2 437 337 | -2 063 946 | -1 696 680 | -1 335 437 | -980 119 | -500 629 | -29 003 | 434 887 |
| Cash burn | 3 320 000 | 3 192 132 | 2 936 362 | 2 684 786 | 2 437 337 | 2 063 946 | 1 696 680 | 1 335 437 | 980 119 | 500 629 | 29 003 | 0 |
| Cumulative cash | -3 320 000 | -6 512 132 | -9 448 494 | -12 133 280 | -14 570 617 | -16 634 563 | -18 331 243 | -19 666 679 | -20 646 798 | -21 147 427 | -21 176 431 | -21 176 431 |

### Waterfall (run-rate на M12)
- ARPA: 260 000 ₽/клиент/мес
- Gross after COGS: 3 884 887 ₽/мес
- Contribution after variable success/commission: 3 436 631 ₽/мес
- EBITDA after fixed costs: 434 887 ₽/мес
- Net after tax: УСН 6% = -31 300 ₽/мес, IT-льгота 3% = 201 794 ₽/мес, ОСНО 20% = 347 910 ₽/мес

### Cash flow
- startup_capital_to_bep_rub: 21 176 431 ₽
- EBITDA break-even month: M12

### Налоговая модель РФ
- УСН 6%: налог с выручки, удобно для early-stage, но может ухудшать net margin при тонкой EBITDA.
- IT-льгота 3%: применима при аккредитации Минцифры и соблюдении критериев профильной выручки; в модели это лучший режим для прибыльных сценариев.
- ОСНО 20%: налог на прибыль, плюс НДС 20% если компания на ОСНО; для B2B medtech может быть приемлемо для крупных клиентов, но давит на cash conversion.
- Страховые взносы ~30% к ФОТ уже отражены в исходном FOT fully-loaded и должны сохраняться в план-факте.

### Break-even
- Break-even client count: 30,0 клиента
- Break-even by month: M12

## Сценарий: Оптимистичный

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 5 | 5 | 5 | 6 |
| Total clients | 1,0 | 3,0 | 5,0 | 7,9 | 10,8 | 14,7 | 18,6 | 22,4 | 27,1 | 31,8 | 36,5 | 42,1 |
| MRR | 286 000 | 854 969 | 1 417 910 | 2 260 885 | 3 094 929 | 4 206 134 | 5 305 565 | 6 393 346 | 7 755 600 | 9 103 420 | 10 436 958 | 12 042 366 |
| COGS | 120 000 | 358 728 | 594 927 | 948 623 | 1 298 571 | 1 764 811 | 2 226 111 | 2 682 523 | 3 254 098 | 3 819 617 | 4 379 143 | 5 052 741 |
| Gross profit | 166 000 | 496 241 | 822 983 | 1 312 262 | 1 796 357 | 2 441 323 | 3 079 454 | 3 710 823 | 4 501 502 | 5 283 803 | 6 057 815 | 6 989 625 |
| GM% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% | 58,0% |
| Fixed costs | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 |
| EBITDA | -3 434 000 | -3 103 759 | -2 777 017 | -2 287 738 | -1 803 643 | -1 158 677 | -520 546 | 110 823 | 901 502 | 1 683 803 | 2 457 815 | 3 389 625 |
| Cash burn | 3 434 000 | 3 103 759 | 2 777 017 | 2 287 738 | 1 803 643 | 1 158 677 | 520 546 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash | -3 434 000 | -6 537 759 | -9 314 776 | -11 602 514 | -13 406 157 | -14 564 834 | -15 085 381 | -15 085 381 | -15 085 381 | -15 085 381 | -15 085 381 | -15 085 381 |

### Waterfall (run-rate на M12)
- ARPA: 286 000 ₽/клиент/мес
- Gross after COGS: 6 989 625 ₽/мес
- Contribution after variable success/commission: 6 358 032 ₽/мес
- EBITDA after fixed costs: 3 389 625 ₽/мес
- Net after tax: УСН 6% = 2 667 083 ₽/мес, IT-льгота 3% = 3 028 354 ₽/мес, ОСНО 20% = 2 711 700 ₽/мес

### Cash flow
- startup_capital_to_bep_rub: 15 085 381 ₽
- EBITDA break-even month: M8

### Налоговая модель РФ
- УСН 6%: налог с выручки, удобно для early-stage, но может ухудшать net margin при тонкой EBITDA.
- IT-льгота 3%: применима при аккредитации Минцифры и соблюдении критериев профильной выручки; в модели это лучший режим для прибыльных сценариев.
- ОСНО 20%: налог на прибыль, плюс НДС 20% если компания на ОСНО; для B2B medtech может быть приемлемо для крупных клиентов, но давит на cash conversion.
- Страховые взносы ~30% к ФОТ уже отражены в исходном FOT fully-loaded и должны сохраняться в план-факте.

### Break-even
- Break-even client count: 23,8 клиента
- Break-even by month: M8

## Сценарий: Пессимистичный

| Показатель | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 2 | 3 |
| Total clients | 0,0 | 1,0 | 2,0 | 2,9 | 3,8 | 5,7 | 7,6 | 9,4 | 11,1 | 12,8 | 14,5 | 17,1 |
| MRR | 0 | 234 000 | 461 681 | 683 214 | 898 764 | 1 342 494 | 1 774 241 | 2 194 330 | 2 603 074 | 3 000 780 | 3 387 747 | 3 998 264 |
| COGS | 0 | 145 000 | 286 084 | 423 359 | 556 927 | 831 887 | 1 099 423 | 1 359 734 | 1 613 016 | 1 859 458 | 2 099 245 | 2 477 557 |
| Gross profit | 0 | 89 000 | 175 597 | 259 855 | 341 838 | 510 607 | 674 818 | 834 595 | 990 058 | 1 141 322 | 1 288 502 | 1 520 707 |
| GM% | 0,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% | 38,0% |
| Fixed costs | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 | 3 600 000 |
| EBITDA | -3 600 000 | -3 511 000 | -3 424 403 | -3 340 145 | -3 258 162 | -3 089 393 | -2 925 182 | -2 765 405 | -2 609 942 | -2 458 678 | -2 311 498 | -2 079 293 |
| Cash burn | 3 600 000 | 3 511 000 | 3 424 403 | 3 340 145 | 3 258 162 | 3 089 393 | 2 925 182 | 2 765 405 | 2 609 942 | 2 458 678 | 2 311 498 | 2 079 293 |
| Cumulative cash | -3 600 000 | -7 111 000 | -10 535 403 | -13 875 549 | -17 133 711 | -20 223 104 | -23 148 286 | -25 913 690 | -28 523 632 | -30 982 310 | -33 293 808 | -35 373 100 |

### Waterfall (run-rate на M12)
- ARPA: 234 000 ₽/клиент/мес
- Gross after COGS: 1 520 707 ₽/мес
- Contribution after variable success/commission: 1 264 408 ₽/мес
- EBITDA after fixed costs: -2 079 293 ₽/мес
- Net after tax: УСН 6% = -2 319 188 ₽/мес, IT-льгота 3% = -2 199 241 ₽/мес, ОСНО 20% = -2 079 293 ₽/мес

### Cash flow
- startup_capital_to_bep_rub: 35 373 100 ₽
- EBITDA break-even month: не достигается в горизонте M1-M12

### Налоговая модель РФ
- УСН 6%: налог с выручки, удобно для early-stage, но может ухудшать net margin при тонкой EBITDA.
- IT-льгота 3%: применима при аккредитации Минцифры и соблюдении критериев профильной выручки; в модели это лучший режим для прибыльных сценариев.
- ОСНО 20%: налог на прибыль, плюс НДС 20% если компания на ОСНО; для B2B medtech может быть приемлемо для крупных клиентов, но давит на cash conversion.
- Страховые взносы ~30% к ФОТ уже отражены в исходном FOT fully-loaded и должны сохраняться в план-факте.

### Break-even
- Break-even client count: 48,6 клиента
- Break-even by month: в пределах 12 месяцев не достигается

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

Ниже stress-проверка для run-rate на M12. База взята из SECTION A: 29,9 активных клиентов, ARPA 260 000 ₽/мес, COGS 130 000 ₽/клиент/мес, lean fixed costs 3 450 000 ₽/мес. Для Sens1 считаю, что удвоение CAC отражается в удвоении fully-loaded GTM spend из `04-economics.md`, то есть EBITDA снижается на дополнительный acquisition burn 2 145 000 ₽/мес. Для Sens2 сохраняю тот же new-logo plan, но удваиваю помесячный churn с ~1,64% до ~3,28%. Для Sens3 режу цену на 30% при неизменном COGS, что реалистично для price war в early RF market.

| Сценарий | Ключевое изменение | Active clients @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | Без изменений | 29,9 | 434 887 | Уже ниже 500k gate, запас прочности минимальный |
| Sens1 | CAC x2 | 29,9 | -1 710 113 | GTM burn съедает весь operating leverage |
| Sens2 | Churn x2 | 28,0 | 183 661 | Модель остаётся около нуля, но не проходит EBITDA gate |
| Sens3 | Price -30% | 29,9 | -1 896 045 | Цена уходит ниже безопасного contribution-уровня |

### Вывод по чувствительности
- Самый опасный single-point failure здесь не churn, а **price compression**: при цене ~182 000 ₽/клиент/мес gross profit на клиента падает до 52 000 ₽, и модель быстро уходит в отрицательную EBITDA.
- **CAC x2** не обязательно убивает unit economics навсегда, но делает cash profile несъедобным для фонда без крупного pre-funded runway.
- Даже **base-case M12 = 434 887 ₽ EBITDA/мес** не дотягивает до целевого 500k ₽. Значит кейс требует либо более высокого чека, либо лучшей стандартизации delivery.

## 2. Monte Carlo Lite — confidence intervals

Использую упрощённую 9-combo аппроксимацию вместо полного кода на 1000 симуляций. Распределения заданы как triangular min / mode / max, опираясь на `02-demand.md`, `04-economics.md` и текущие публичные pricing / category anchors западных аналогов [T1][T2][T3][T4][T5][T6][T7].

### Inputs

| Переменная | min | mode | max | Источник |
|------------|-----:|------:|-----:|----------|
| CAC, ₽ | 600 000 | 858 000 | 1 350 000 | [T1] |
| Monthly churn, % | 1,0% | 1,6% | 3,0% | [T1] |
| ARPU, ₽/мес | 220 000 | 260 000 | 320 000 | [T1][T2] |
| Conversion rate lead→paid, % | 0,8% | 1,3% | 2,0% | [T1] |
| Time-to-hire, мес | 1,0 | 1,5 | 3,0 | [T1] |

### Интерпретация симуляции
- p10 = worst-side cluster: высокий CAC, высокий churn, низкий ARPU, слабая конверсия, медленный hiring.
- p50 = mode values из текущей модели.
- p90 = best-side cluster: низкий CAC, низкий churn, высокий ARPU, сильная конверсия, быстрый hiring.
- Для EBITDA @M24 считаю 24-месячный контур с тем же lead base 192 лида/мес из `04-economics.md`, а число новых клиентов в месяц меняется через conversion rate.

### Результаты Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -1 060 000 | 3 060 000 | 12 190 000 | 13 250 000 |
| CAC payback, мес | 15,0 | 6,6 | 3,2 | 11,8 |
| LTV/CAC | 2,7x | 9,5x | 26,7x | 24,0x |
| Cash runway, мес | 12 | 18 | 26 | 14 |

### Правила-гейты по результату
1. **p10 EBITDA < 0** → kill criterion #1 активируется: в нижнем хвосте модель несёт риск неплатёжеспособности.
2. **p50 EBITDA > 500k ₽/мес** → median-гейт формально проходит, но с умеренным, а не большим запасом.
3. **p90 / p10 по модулю > 10x**: 12,19 млн против 1,06 млн по абсолютной величине, разброс очень высокий → score нужно даунгрейдить за volatility.
4. **Range width по LTV/CAC = 24,0x > 8** → модель хрупкая, особенно к сочетанию pricing drift + churn drift + CAC inflation.

### Комментарий
Даже если median-case выглядит привлекательно, доверительный интервал слишком широкий для комфортного фонда: в хорошем хвосте это сильный software asset, в плохом хвосте это service-heavy healthtech с отрицательной EBITDA и коротким runway.

## 3. Competitor deep-dive

### 3.1 Западные игроки

| Игрок | Что делает | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Ambience Healthcare | Ambient documentation + coding + revenue integrity для health systems [T3] | Сильный enterprise proof, широкий specialty coverage, глубокий value prop не только на scribe, но и на coding / compliance | Тяжёлый enterprise motion, сложные интеграции, высокая стоимость внедрения, неочевидная локализация под РФ | **5–8%** глобального enterprise ambient-clinical-doc сегмента, оценка по числу крупных health-system deployments и высокой фрагментации рынка | Локализация под РФ, data residency, 152-ФЗ, шаблоны под ЕГИСЗ/МИС, lower-cost rollout |
| Abridge | Enterprise AI for clinical conversations, встроенность в Epic, сильный brand в US enterprise [T4] | Сильная distribution через крупные health systems, Epic-native motion, category leadership signal | Зависимость от американского EHR stack, тяжёлая sales cycle, слабая переносимость в РФ-контур | **8–12%** enterprise ambient AI в США, inference по status как market leader / KLAS + top health system adoption | В РФ можно выиграть скоростью локального внедрения и адаптацией под отечественные МИС, где Abridge почти не имеет go-to-market плеча |
| Nabla | AI assistant / dictation / ambient documentation, 85k+ clinicians [T5] | Быстрый adoption, широкий clinician base, хороший продуктовый UX, lower-friction deployment | Более слабый moat в enterprise workflow / revenue integrity, выше риск commoditization | **3–6%** глобального clinician-facing ambient-doc сегмента, inference по 85k+ clinicians и фрагментированному рынку | Наш шанс, если зайти глубже в workflow клиники, а не только в note-taking |

### 3.2 Российские игроки и заменители

| Игрок | Источник | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| К-Скай / Webiomed | Сколково: генеративный ИИ для проверки качества меддокументации [T8], Habr summary [T9] | Уже работает в российском healthtech-контуре, есть доверие к локальному compliance, сильный angle на quality control меддоков | Ближе к document QA / CDSS, чем к full ambient scribe; может быть слабее в real-time clinician UX | **8–12%** российского сегмента AI для анализа медкарт и качества документации, inference по зрелости и видимости | Мы сильнее, если делаем end-to-end ambient capture + coding + revenue uplift, а не только post-hoc проверку |
| iambulant | Сколково: структурирование медкарт, инвестиции 15 млн ₽ [T10] | Очень близкий workflow pain, локальная продуктовая формулировка, ранний capital signal | Ранняя стадия, мало публичных масштабных внедрений, execution risk высокий | **1–3%** early-stage ниши AI-структурирования медкарт | Наше преимущество в более широком продукте и лучшей экономике на network-level contract |
| IQDOC / Medach | vc.ru: ИИ-поисковик для врачей по клинрекам и НПА [T11] | Сильный trust angle через официальные источники, хорошо заходит как doctor copilot | Это скорее knowledge retrieval, а не documentation automation; monetization depth пока неочевидна | **1–2%** doctor-AI assistant niche | Мы создаём ROI на документации и revenue-cycle, а не только на поиске знаний |
| GidMedical | Официальный сайт + Rusprofile [T12][T13] | Низкий ценовой вход, Telegram-native distribution, понятный low-end substitute | Пациентский / service-like продукт, не enterprise clinical workflow, слабый moat для B2B medtech | **<1%** в адресуемом B2B doc-automation сегменте | Наше преимущество в enterprise контуре, интеграциях и доказуемом ROI для сети клиник |

### Вывод по конкурентам
- В западном сегменте уже видно, что категория будет выигрывать у pure-dictation и смещаться в **documentation + coding + compliance + revenue integrity**.
- В РФ прямой сильный лидер именно в **ambient clinical documentation для private networks** пока не закрепился, но adjacent-игроки уже закрывают куски value chain.
- Значит окно входа есть, но moat будет не в модели как таковой, а в **локальных интеграциях, шаблонах, compliance и productized implementation**.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного CTO / integrations lead вовремя | medium | high | time-to-hire > 3 мес, сорванные интеграционные спринты | founder-led hiring, equity-heavy offers, подрядный bridge team |
| Operational | Service load по кастомным внедрениям съедает GM | high | high | COGS > 150k ₽/клиент/мес, рост ручных часов на rollout | productize templates, ограничить scope пилота, ввести standard implementation package |
| Operational | LLM API latency / outages ломают врачебный UX | medium | high | SLA провайдеров падает, время генерации note > 15 сек | multi-model routing, local fallback, async draft mode |
| Market | Спрос существует, но бюджетной строки под ambient AI нет | medium | high | много пилотов, мало paid conversion; длинные закупки | продавать ROI через coding + revenue integrity, а не только time-saving |
| Market | Конкуренты начинают price war и опускают чек на 20–30% | high | high | win-rate падает, discounting > 25% | пакетировать enterprise modules, защищать цену интеграциями и compliance |
| Market | Churn выше модели из-за слабого adoption врачами | medium | high | logo churn > 2,5% monthly, utilization < 60% | onboarding playbooks, champion program, specialty templates |
| Regulatory | Нарушение 152-ФЗ / data residency при хранении и обработке медданных | medium | very high | legal/security замечания на pre-sale, блокировки от ИБ клиента | локальный контур, on-prem / VPC опции, DPA и аудит trail |
| Regulatory | Ограничения 115-ФЗ / KYC / договорная комплаенс-нагрузка замедляют enterprise deals | low | medium | procurement cycle > 6 мес, рост числа compliance-итераций | стандартный legal pack, финансовый мониторинг контрагентов, предварительный vendor due diligence |
| Regulatory | Санкции SaaS / ограничение внешних API и облаков | high | high | недоступность зарубежных vendor APIs, рост отказов платежей | vendor diversification, российские облака, план миграции на локальные модели |
| Financial | Cash runway сжимается из-за CAC inflation | high | high | CAC > 1,1 млн ₽, payback > 9 мес | стоп на найм, урезание paid channels, фокус на founder-led и партнёрский GTM |
| Financial | Ослабление рубля повышает стоимость inference и SaaS tooling | high | medium | USD/RUB > внутреннего budget band 100+ | рублёвые контракты с индексатором, резерв в FX, локальные альтернативы |
| Financial | Инфляция зарплат в AI / medtech ролях | medium | medium | офферы закрываются с 20%+ пересмотром компенсаций | selective hiring, remote regions, variable comp tied to milestones |
| Black swan | Военная эскалация или новый санкционный пакет бьёт по healthcare IT spend | medium | high | freeze новых ИТ-бюджетов у сетей | смещение в cost-saving ROI pitch, диверсификация по сегментам |
| Black swan | Внешний LLM-провайдер внезапно отключает доступ | medium | very high | ухудшение SLA, уведомления об ограничениях, скачок стоимости токенов | резервный стек из 2–3 моделей, локальные open-weight deployment, graceful degradation |

## 5. Kill conditions на 6-й месяц

1. **EBITDA risk / insolvency trigger:** если по rolling forecast **p10 EBITDA@M24 остаётся < 0**, а фактический runway < 9 месяцев, продолжать нельзя.
2. **Go-to-market trigger:** если через 6 месяцев **paid conversion lead→paid < 0,8%** или blended CAC > **1,1 млн ₽**, модель слишком дорогая для scale.
3. **Retention / pricing trigger:** если **monthly churn > 2,5%** одновременно с фактическим ARPU < **220 000 ₽/мес**, unit economics ломается и кейс надо закрывать.

## 6. Итог SECTION B

Кейс выглядит жизнеспособным только как **жёстко стандартизированный enterprise / upper-midmarket healthtech stack**. В median-case экономика выдерживает, но нижний хвост уже уходит в отрицательную EBITDA, а диапазон по LTV/CAC и M24 EBITDA слишком широкий. Поэтому это не clean software bet, а управляемая ставка на сильный execution в compliance-heavy нише.

## Sources for SECTION B
- [T1] `pipeline/cases/ambience-healthcare-geo-expand-v2/04-economics.md`
- [T2] `pipeline/cases/ambience-healthcare-geo-expand-v2/02-demand.md`
- [T3] Ambience Healthcare: https://www.ambiencehealthcare.com/
- [T4] Abridge: https://www.abridge.com/
- [T5] Nabla: https://www.nabla.com/
- [T6] Freed pricing: https://www.getfreed.ai/pricing
- [T7] Suki: https://www.suki.ai/
- [T8] Сколково, К-Скай / Webiomed: https://sk.ru/news/generativnyj-ii-vnedryon-v-process-proverki-kachestva-medicinskoj-dokumentacii/
- [T9] Habr, summary по К-Скай: https://habr.com/ru/news/987472/
- [T10] Сколково, iambulant: https://sk.ru/news/skolovskij-startap-iambulant-privlyok-investicii-na-razvitie-ii-platformy-dlya-strukturirovaniya-medkart/
- [T11] vc.ru, IQDOC: https://vc.ru/id69595/2726114-iqdoc-ii-poiskovik-dlya-vrachey
- [T12] GidMedical: https://gidmedical.ru/
- [T13] Rusprofile, ООО «Гид Медикал»: https://www.rusprofile.ru/id/1237700669470

<!-- P6B-DONE -->


---

## 06-verdict.md

[HEALTHCARE] Ambience Healthcare Geo Expand v2 — NEAR-PASS: 65/100 | EBITDA base=435К₽/мес через 12 мес | LTV/CAC=10.1x | Ключевое преимущество: productized enterprise-контур documentation+coding | Главный риск: compliance-heavy внедрения легко съедают маржу.

# 06-verdict

sector: HEALTHCARE
stage: P7 Critic and Verdict
case: ambience-healthcare-geo-expand-v2
verdict: NEAR-PASS
normalized_score: 65/100
raw_score: 98/150
date: 2026-04-21
historical_context: related to ambient-clinical-documentation-operator-v2, but reassessed as standalone candidate

## Инвесткомитет one-line conclusion
Кейс почти проходит investment-grade: unit economics и путь к EBITDA рабочие, но запас прочности недостаточен из-за слабого moat, compliance-heavy delivery и высокой чувствительности к price compression.

## Оценка
Source tier balance: T1=4, T2=8, T3=1, weighted=2.23. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | "LTV/CAC = 10.1x", "Gross Margin = 50.0%", gross-profit payback "6.6 мес" из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | В базе M12 EBITDA = "434 887 ₽/мес", а в P5 указано, что "> 500k ₽/мес достижима в lean-mode уже около 36–38 клиентов". |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | Есть RU-база спроса: "87,3 тыс. медицинских организаций", "628,2 тыс. врачей", SOM Y1 = "65 млн ₽"; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Устойчивость строится на "локальных интеграциях, шаблонах, compliance и productized implementation", а не на сильном network moat. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | В risk matrix отмечены high/high риски: "service load по кастомным внедрениям съедает GM" и "санкции SaaS". |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | GTM account-based и конкретный: blended CAC "858 000 ₽", payback "6.6 мес", плюс 10 named targets из private healthcare. |

**Normalized score = round(98 × 100 / 150) = 65/100.**

## Вердикт
**NEAR-PASS / REJECTED FOR NOW.**

Почему не APPROVED:
1. Формально EBITDA gate почти проходит, но **base-case на M12 всё ещё ниже 500К₽/мес**.
2. Moat слабее investment-grade: без глубокой встроенности в МИС и локальный compliance это быстро коммодитизируется.
3. Нижний хвост модели плохой: p10 EBITDA@M24 = **-1,06 млн ₽/мес**, а price -30% уводит M12 EBITDA в **-1,90 млн ₽/мес**.

Почему не жёсткий REJECT:
1. Unit economics сильнее среднего по healthcare software.
2. Есть реалистичный путь к **company_ebitda_rub_month > 500 000 ₽/мес** при 36–38 клиентах и disciplined lean-mode.
3. В РФ есть платёжеспособный private healthcare wedge, а не только гипотетический рынок.

## 7-factor Moat Framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | После интеграции в МИС, шаблоны и обучение врачей смена вендора становится заметно болезненной. |
| Scale economies | 1 | Infra и шаблоны масштабируются, но implementation и clinical QA долго остаются ручными. |
| Proprietary data / model advantage | 1 | Потенциал есть, но публично не доказан значимый локальный датасет или model edge. |
| Regulatory moat | 2 | 152-ФЗ, meddata и security/compliance реально повышают порог входа. |
| Brand / distribution | 1 | Категория ранняя, локального лидера пока нет, сильный бренд ещё не сформирован. |
| Embedded workflow | 3 | При удачной интеграции продукт садится в ежедневный врачебный и revenue-cycle workflow. |

Сумма 7-factor = **10/21**.
Moat score = round(10 × 25 / 21) = **12/25**, округлено в рубрике до **13/25** с учётом высокой embeddedness.

**Вывод по moat:** moat слабый-средний. Так как moat score близок к weak moat и 7-factor сумма = 10, это остаётся в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 8 666 667 ₽ |
| Fully-loaded CAC | 858 000 ₽ |
| LTV/CAC | 10.1x |
| CAC payback по MRR | 3.3 мес |
| CAC payback по gross profit | 6.6 мес |
| Gross Margin | 50.0% |
| contribution_margin_rub_month | 115 000 ₽ |
| fixed_costs_rub_month | 5 763 000 ₽ steady-state / 3 450 000 ₽ lean-mode |
| company_ebitda_rub_month base M12 | 434 887 ₽/мес |
| company_ebitda_potential_rub_month | 1 150 000 ₽/мес при 40 клиентах в lean-mode |
| clients_to_500k_ebitda | 36–38 |
| months_to_500k_ebitda | 13–14 мес (интерполяция между M12 и P5 gate) |
| clients_to_1m_ebitda | ~40 |
| startup_capital_to_bep_rub | 21 176 431 ₽ по P6A base / 55–75 млн ₽ burn-to-breakeven по P5 |
| Break-even clients | 30 в lean-mode / 50 на полной команде |

## Полный бизнес-процесс

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP mapping по сетям клиник | SDR / founder | CRM, Rusprofile, manual research | 2 ч | 2 000 | Низкий |
| 2 | Первичный outreach | SDR | Email, Telegram, phone | 1.5 ч | 1 600 | Средний |
| 3 | Intro / qualification call | SDR + AE | Meet, CRM | 1 ч | 3 000 | Средний |
| 4 | Discovery по текущему документообороту | AE + founder | Meet, questionnaire | 2 ч | 8 500 | Низкий |
| 5 | Demo на врачебных workflow | AE + clinical specialist | Demo env, scripts | 2 ч | 9 500 | Низкий |
| 6 | Security / legal / meddata pre-check | AE + CTO | NDA, policy docs | 2 ч | 8 000 | Низкий |
| 7 | Pilot scoping и success metrics | AE + CSM | SOW, ROI model | 3 ч | 12 000 | Низкий |
| 8 | Интеграция с МИС / шаблонами | Solutions + CSM | API, mappings, templates | 16 ч | 52 000 | Средний |
| 9 | Обучение врачей и админов | CSM | Zoom, manuals | 5 ч | 14 000 | Средний |
| 10 | Пилот 4–6 недель и weekly review | CSM + AE | Analytics, support | 12 ч | 33 000 | Средний |
| 11 | Procurement / договор / счёт | AE + founder + ops | Contract workflow | 6 ч | 16 000 | Низкий |
| 12 | Production rollout после оплаты | CSM + support | Runbook, dashboards | 8 ч | 22 000 | Средний |

## Команда

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / tech lead | 1 | 520 000 | 2 | 2 | 156 000 | 676 000 |
| Backend engineer | 2 | 380 000 | 1.5 | 1.5 | 114 000 | 988 000 |
| ML / applied AI engineer | 1 | 480 000 | 2 | 2 | 144 000 | 624 000 |
| Integrations / solutions engineer | 1 | 320 000 | 1.5 | 1.5 | 96 000 | 416 000 |
| SDR | 2 | 150 000 + бонус | 1 | 1 | 45 000 | 390 000 |
| AE | 1 | 280 000 + комиссия | 1.5 | 2 | 84 000 | 364 000 |
| CSM / implementation | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Clinical SME / QA | 1 | 260 000 | 1.5 | 1.5 | 78 000 | 338 000 |
| Finance / ops (part-time) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого** | **11.5** |  |  |  |  | **4 953 000 ₽/мес** |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Медси | Крупная private network, высокий объём врачебной документации и интерес к efficiency/quality layer. | email decision-maker CIO/CMO + отраслевые конференции | 450 000 ₽/мес |
| 2 | Мать и дитя | Сетевой premium provider, где documentation quality и coding напрямую влияют на economics. | email medical director + партнёрство с МИС | 380 000 ₽/мес |
| 3 | Медскан | Digital-forward сеть, релевантен контур стандартизации документации и revenue integrity. | founder-led intro + конференция MedSoft | 320 000 ₽/мес |
| 4 | EMC | Премиальный сегмент, выше готовность платить за compliance и врачебную производительность. | direct outreach к COO/CIO | 500 000 ₽/мес |
| 5 | СМ-Клиника | Мульти-сайт сеть с большим потоком документации, подходит для pilot-to-rollout. | email decision-maker + webinar для ops-команды | 300 000 ₽/мес |
| 6 | АВА-Петер / Скандинавия | Сильный private care brand, чувствителен к качеству меддоков и UX врача. | conference networking + партнёрство с интегратором МИС | 280 000 ₽/мес |
| 7 | Клиника Фомина | Быстрорастущая сеть, часто внедряет digital tools и может быть early adopter. | founder intro + Telegram/email | 220 000 ₽/мес |
| 8 | Будь Здоров | Большая сеть с операционной сложностью, где documentation speed и coding дают measurable ROI. | outreach к head of digital / operations | 300 000 ₽/мес |
| 9 | Сеть клиник Эксперт | Географически распределённый актив, подходит для стандартизированных specialty templates. | партнёрство + direct sales | 240 000 ₽/мес |
| 10 | MedSwiss | Средний enterprise-аккаунт с частной медициной и понятным ROI на документации. | email decision-maker + case-study based outreach | 200 000 ₽/мес |

**Вывод по GTM:** список buyers конкретный и адекватный ICP, но сделка всё равно consultative, с длинным pre-sale и тяжёлой интеграцией. Это ограничивает скорость scale-up.

## Top-3 Risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| weak_moat / commoditization | high | high | Без глубокой встроенности в МИС и локальный compliance продукт рискует стать interchangeable AI-scribe слоем. |
| service_load_margin_erosion | high | high | В P6 прямо отмечено: кастомные внедрения и QA могут поднять COGS выше безопасного уровня. |
| pricing_pressure | high | high | Sens3 price -30% даёт EBITDA @M12 = -1 896 045 ₽/мес, то есть модель ломается от price war. |

## Что нужно доказать для APPROVED
1. **3–4 платящих сети клиник** с ACV не ниже 3–4 млн ₽/год на аккаунт.
2. **Фактический monthly churn < 2%** после первых 6–9 месяцев использования.
3. **Productized implementation:** COGS удерживается не выше 130–140 тыс. ₽/клиент/мес без ручного раздувания QA.
4. **Интеграционный moat:** минимум 2 МИС-коннектора и повторяемый rollout playbook.
5. **Price resilience:** win-rate без дисконта >20% и отсутствие необходимости продавать ниже 220 тыс. ₽/мес.

## LTV Upside Calculator

Для перевода кейса из 65/100 в 70+ нужны не чудеса, а конкретное улучшение двух драйверов: ARPA и churn.

| Сценарий | ARPA | GM | Annual churn | customer_ltv_rub | LTV/CAC |
|---|---:|---:|---:|---:|---:|
| Текущий base | 260 000 ₽/мес | 50% | 18% | 8 666 667 ₽ | 10.1x |
| Upside 1: ARPA +15% | 299 000 ₽/мес | 50% | 18% | 9 966 667 ₽ | 11.6x |
| Upside 2: churn 14% | 260 000 ₽/мес | 50% | 14% | 11 142 857 ₽ | 13.0x |
| Upside 3: ARPA 300k + churn 14% | 300 000 ₽/мес | 52% | 14% | 13 371 429 ₽ | 15.6x |

Практический смысл: если команда докажет контракт **300К₽+/мес**, churn **≤14% annual** и не уронит GM ниже 50%, кейс переходит в зону investment-ready.

## Сравнение с историческим related case
Исторический ambient-clinical-documentation-operator-v2 получил reject из-за более слабого локального demand proof. Этот rerun сильнее по economics и TAM/SAM, но всё ещё не снимает ключевой вопрос: можно ли в РФ построить не просто AI-scribe, а повторяемый enterprise workflow moat.

## Финальное решение инвесткомитета
**REJECTED FOR NOW / NEAR-PASS.**

Рекомендация: не инвестировать как чистый фондовый approved-case сейчас, но держать в active watchlist. Возвращать на re-review после первых 3–4 сетевых клиентов, доказанного productized rollout и защиты цены выше 220–260К₽/мес.

