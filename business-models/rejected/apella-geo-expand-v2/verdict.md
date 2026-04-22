# Verdict Dossier — apella-geo-expand-v2

## Stage 1 — Intake

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-apella-geo-expand.md
created: 2026-04-20T06:37:59+03:00
original_source: triage/triage-2026-04-19-apella-geo-expand-supporting.md
original_case: pipeline/cases/hospital-operations-automation-operator/
original_verdict: Существующий кейс обогащён, новый кейс не создавался.
---

# Intake

## Статус
Принудительный полный rerun/resurrect. Этот кейс создан заново и должен пройти P3→P7 с новой аналитикой.

## Краткое пояснение
Принудительный resurrect-rerun для повторной полной аналитики по сигналу Apella в теме hospital operations / perioperative coordination.

## Полный контекст raw-файла

# RESURRECT SIGNAL — apella-geo-expand

## Meta
- source: triage/triage-2026-04-19-apella-geo-expand-supporting.md
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
2026-04-19

## Входные данные
- `pipeline/raw/2026-04-19-0403-msk-apella-geo-expand.md`

## Классификация
поддерживающий сигнал для существующего открытого кейса

## Решение
Существующий кейс обогащён, новый кейс не создавался.

## Совпадающий кейс
- `pipeline/cases/hospital-operations-automation-operator/`

## Почему
- Сигнал совпадает по теме, нише и технологии с уже открытым кейсом про AI-автоматизацию госпитальных операций, особенно операционного блока и perioperative coordination.
- Во входном файле есть сильные подтверждающие данные о масштабе внедрений, инвестиционной поддержке и измеримой ценности для hospital-grade клиентов.
- Создание нового кейса не требуется, потому что сигнал логично усиливает уже существующий case wedge.

## Что добавлено в кейс
- В `pipeline/cases/hospital-operations-automation-operator/01-evidence.md` добавлена запись на русском языке.
- Зафиксированы дата, источники, тип сигнала, объяснение, как сигнал усиливает кейс, и ключевые факты.
- Добавлены данные: Series B на $80 млн, 500000+ поддержанных хирургических кейсов, внедрение в Houston Methodist с 200+ операционными в девяти больницах, а также кейс MUSC с эффектом по поиску возможностей повышения эффективности за 60 дней.

## Что сделано
- Кейс `hospital-operations-automation-operator` обогащён.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал обработан как supporting signal для открытого кейса. Кейс обогащён новыми подтверждающими данными.

```


## Stage 2 — Validation

Отсутствует обязательный файл `02-validation.md`. В исходном кейсе произошёл schema drift, это зафиксировано как quality-risk в финальном вердикте.

## Stage 3 — Demand

Отсутствует обязательный файл `03-demand.md`. Вместо него в кейсе присутствует `02-demand.md`, содержание приведено ниже как фактический demand-stage.

# 02-demand

## Demand validation summary
- **Продукт**: Apella AI, платформа для perioperative coordination и управления операционным блоком, с упором на hospital operations, OR utilization и orchestration для крупных hospital systems. [T2: https://www.apella.io/ ; https://www.fiercehealthcare.com/health-tech/apella-raises-80m-series-b-ai-powered-hospital-operations-platform]
- **Итог по спросу в РФ**: **LOW** по обязательному demand endpoint, но боль у крупных хирургических контуров реальна. По ключам `операционный блок больница`, `управление операционной больницы`, `perioperative coordination` endpoint вернул LOW, при этом по первому ключу есть **114 hh.ru вакансий** как proxy операционной нагрузки и staffing pain. [T1/T2: internal demand endpoint with HH proxy]
- **Решение по гейту**: **не отклонять на P4**. Массового PLG-спроса в РФ нет, но enterprise-сценарий для крупных многопрофильных больниц и частных сетей может пройти порог **500 тыс. ₽ EBITDA в месяц**. [T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%B1%D0%BB%D0%BE%D0%BA%20%D0%B1%D0%BE%D0%BB%D1%8C%D0%BD%D0%B8%D1%86%D0%B0` → **LOW**, score **22**, hh.ru vacancies = **114**, yandex suggest = **100**. [T1/T2: internal demand endpoint with HH proxy]
- `http://172.18.0.1:9001/multi-demand?keyword=%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%BE%D0%B9%20%D0%B1%D0%BE%D0%BB%D1%8C%D0%BD%D0%B8%D1%86%D1%8B` → **LOW**, score **7**, hh.ru vacancies = **57**. [T1/T2: internal demand endpoint with HH proxy]
- `http://172.18.0.1:9001/multi-demand?keyword=perioperative%20coordination` → **LOW**, score **0**. [T2: internal demand endpoint]
- Вывод: category demand в РФ есть как problem demand, но пока почти не проявлен как осознанный product demand. Это типичный enterprise-led рынок, а не self-serve категория. [T1/T2]

### 2) Operating pain and buyer reality
- Apella публично указывает, что ее система уже поддержала более **500 000** хирургических кейсов; Houston Methodist развернул Apella на контуре с **200+ операционными** в девяти больницах, а MUSC использовал платформу для поиска возможностей повышения эффективности в течение **60 дней**. Это сильное доказательство того, что боль вокруг OR orchestration budget-worthy для крупных health systems. [T2: https://www.fiercehealthcare.com/health-tech/apella-raises-80m-series-b-ai-powered-hospital-operations-platform]
- В РФ на 2024 год насчитывалось **5 044 больничных организации**, что задает широкий buyer universe, но реально адресуем только верхний слой крупных хирургических контуров. [T2, citing Rosstat: https://vademec.ru/news/2025/05/07/rosstat-v-rossii-v-2024-godu-rabotali-5-044-bolnichnykh-organizatsii/]
- HH-сигналы из обязательного endpoint показывают устойчивый спрос на staffing вокруг операционных и hospital operations, но не на сам software category. Следовательно, боль подтверждена, а software budget нужно продавать через экономику OR utilization и throughput. [T1/T2]

## Real competitors with prices

### Международные и смежные comparable с публичными ценами
1. **Surgimate**, surgical coordination / scheduling software: от **$249 в месяц**. Это closest public comparable для цифровизации perioperative workflow на уровне scheduling/coordination. [T2: https://www.softwareadvice.com/medical/surgimate-profile/]
2. **Shift Admin**, hospital/medical staff scheduling: от **$1 200 в год**. Это нижняя граница бюджета на workflow software в healthcare operations. [T2: https://www.capterra.com/p/169447/Shift-Admin/]
3. **eSchedule** (hospital staff scheduling): единоразово от **$300**. Это low-end benchmark и скорее админ-инструмент, а не AI-платформа, но он показывает, что даже простой scheduling budget already exists. [T2: https://www.capterra.com/p/181523/eSchedule/]

### Более прямые enterprise-конкуренты без публичных прайсов
- **LeanTaaS iQueue for Operating Rooms**: OR block utilization и scheduling optimization, enterprise pricing не раскрыта. [T2: https://leantaas.com/software/operating-room/]
- **Qventus Perioperative Solution**: AI orchestration для perioperative growth и OR efficiency, enterprise pricing не раскрыта. [T2: https://www.qventus.com/perioperative-solution/]
- **Apella** сама продается как hospital-grade enterprise platform, что дополнительно подтверждает buying motion через крупные B2B сделки, а не через seat-based PLG. [T2: https://www.apella.io/]

### Что это значит по конкуренции
- Публичная вилка по смежным workflow tools начинается примерно от **$100-249 в месяц** или **$1 200 в год**, но у прямых enterprise AI-решений цена скрыта. [T2]
- Это означает, что российский вход для Apella логично считать не как легкий SaaS по seat, а как enterprise deployment с higher ACV, интеграциями и длинным sales cycle. [T2, inference]

## Telegram bots / services in RU
- Специализированных российских Telegram-ботов для управления операционным блоком, perioperative coordination или OR utilization с заметной дистрибуцией я не нашел. Обязательный endpoint тоже вернул `telegram.subscribers = 0` по целевым ключам. [T2: internal demand endpoint]
- В российском medtech Telegram чаще встречаются patient-facing сценарии, например запись, reminders и коммуникации. Пример: Medesk публично продвигает Telegram-бота для записи пациентов, но это другой слой продукта, не OR operations. [T2: https://www.medesk.net/ru/blog/telegram-bot-for-clinic/]
- Вывод: в РФ Telegram не является существующим каналом рынка для этого класса продукта. Максимум это вспомогательный notification layer, но не GTM wedge. [T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: Apella привлекла **$80 млн Series B**, а ее внедрения идут в крупных hospital systems, где решение применяется на сотнях операционных. Это не ценник, но сильное подтверждение того, что клиенты готовы выделять enterprise budget под OR orchestration. [T2: https://www.fiercehealthcare.com/health-tech/apella-raises-80m-series-b-ai-powered-hospital-operations-platform]
- **Доказательство WTP №2**: на смежном рынке surgical/workforce scheduling уже есть публичные прайсы от **$249/мес** и **$1 200/год**. Значит, бюджетная строка на workflow software существует даже до AI-апсайда. [T2]
- **Доказательство WTP №3**: по обязательному endpoint есть **114** и **57** hh-сигналов по операционным ключам. Это не purchase order, но T1-proxy того, что hospital operators уже платят за ручное решение той же проблемы через персонал. [T1]
- **Ограничение**: в РФ willingness to pay выглядит только как budget-owner motion на уровне COO/главврача/директора по хирургии/ИТ-директора крупной больницы. Для малого сегмента и для Telegram-first формата доказательств WTP нет. [T2]

## Market sizing

### Методика и допущения
- Курс перевода: **1 USD = 90 ₽** для грубого сопоставления международных comparable. Это операционное допущение для модели, а не primary market source. [спекуляция]
- Из-за отсутствия качественного прямого отчета по рынку perioperative operations software в РФ section ниже считается как **proxy-based estimate**, но с cross-check top-down и bottom-up. [T2]
- Средний целевой контракт для РФ берем в базе как **4,8 млн ₽ ARR** на hospital group/крупную больницу, то есть **400 тыс. ₽ в месяц**. Это на порядок выше low-end scheduling SaaS и отражает enterprise premium за AI, интеграции и hospital-grade deployment. [T2 + inference]

### Top-down
- **TAM (мир)**: глобальный рынок operating room management оценивается примерно в **$3,25 млрд** в 2024 году. В рублях это около **292,5 млрд ₽**. [T2: https://www.grandviewresearch.com/industry-analysis/operating-room-management-market-report]
- **TAM (РФ)**: берем консервативный proxy, что РФ может адресовать около **0,35%** глобального TAM в этой нише через крупные хирургические контуры. Получаем около **1,02 млрд ₽**. Доля маленькая, потому что сегмент узкий, enterprise-only и привязан к limited set крупных buyers. [T2 + спекуляция]
- **SAM (РФ)**: берем **45%** от TAM РФ как реально достижимый в 1-3 года слой крупных федеральных, региональных и частных хирургических контуров. Получаем **459 млн ₽**. [T2 + inference]
- **SOM Y1**: **3%** от SAM = **13,8 млн ₽**. [inference]
- **SOM Y3**: **12%** от SAM = **55,1 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **120** крупных buyers: федеральные центры, большие многопрофильные госбольницы, private hospital groups и сети с заметной хирургией. Это уже не все 5 044 больницы, а только верхний слой цифрово зрелых хирургических контуров. [T2 + inference]
- **% with need** = **70%**. Pain подтверждается staffing proxies, хирургической нагрузкой и международными внедрениями comparable решений. [T1/T2]
- **Активные buyers** = **84**. [расчет]
- **ARR avg** = **4,8 млн ₽/год**. [T2 + inference]
- **SAM bottom-up** = **84 × 4,8 млн ₽ = 403,2 млн ₽**. [расчет]
- **SOM bottom-up Y1** = **4%** от SAM = **16,1 млн ₽**. [inference]
- **SOM bottom-up Y3** = **15%** от SAM = **60,5 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 292,5 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 1,02 млрд ₽ [T2] | 576,0 млн ₽ [T2] | diff=1,8x; bottom-up ниже, потому что считает только 120 явных крупных buyers | lower |
| SAM (РФ) | 459,0 млн ₽ [T2] | 403,2 млн ₽ [T2] | diff=14%; расхождение приемлемое | lower |
| SOM Y1 | 13,8 млн ₽ | 16,1 млн ₽ | diff=17% | **используем 13,8 млн ₽** |
| SOM Y3 | 55,1 млн ₽ | 60,5 млн ₽ | diff=10% | **используем 55,1 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **НМИЦ хирургии им. А. В. Вишневского**. [T2: https://www.vishnevskogo.ru/]
2. **НМИЦ им. В. А. Алмазова**. [T2: https://www.almazovcentre.ru/]
3. **НМИЦ онкологии им. Н. Н. Блохина**. [T2: https://www.ronc.ru/]
4. **НМИЦ трансплантологии и искусственных органов им. В. И. Шумакова**. [T2: https://transpl.ru/]
5. **ГКБ им. С. П. Боткина, Москва**. [T2: https://botkinmoscow.ru/]
6. **НИИ скорой помощи им. Н. В. Склифосовского**. [T2: https://sklif.mos.ru/]
7. **European Medical Center (EMC)**. [T2: https://www.emcmos.ru/]
8. **МЕДСИ**. [T2: https://medsi.ru/]
9. **MD Medical Group / Мать и дитя**. [T2: https://www.mcclinics.ru/]
10. **АО «Медицина»**. [T2: https://www.medicina.ru/]

Sanity check: SOM Y1 в **13,8 млн ₽** при среднем цикле сделки **9-12 месяцев** означает примерно **3 enterprise-контракта** по 4,8 млн ₽ ARR в первый год. Это реалистично для узкого enterprise GTM. SOM Y1 составляет сильно меньше 10% SAM, значит overclaim нет. [T2 + inference]

## Profit Gate: может ли компания выйти на EBITDA > 500 тыс. ₽/мес?

### Сценарий A: low-touch SaaS для одной больницы
- Цена: **150 тыс. ₽/мес** за контур без тяжелых интеграций. [T2 + inference]
- Даже при **10 клиентах** выручка составит **1,5 млн ₽/мес**. При gross margin 70% это **1,05 млн ₽** валовой прибыли, что не покрывает sales + implementation + support + product локализацию. [inference]
- **Вердикт**: **FAIL**. EBITDA 500 тыс. ₽/мес недостижима. [inference]

### Сценарий B: enterprise software для крупной больницы
- Цена: **400 тыс. ₽/мес** или **4,8 млн ₽ ARR**. [T2 + inference]
- При **8 клиентах** выручка = **3,2 млн ₽/мес**. При gross margin 75% валовая прибыль = **2,4 млн ₽/мес**. При операционных расходах около **1,8 млн ₽/мес** остается **0,6 млн ₽ EBITDA**. [inference]
- **Вердикт**: **PASS**. Это минимально рабочая экономика. [inference]

### Сценарий C: network / federal center / внедрение + подписка
- Цена: **700 тыс. ₽/мес blended** за крупную сеть или федеральный хирургический центр, включая интеграцию и расширенный support. [T2 + inference]
- При **5 клиентах** выручка = **3,5 млн ₽/мес**. Даже при gross margin 70% остается **2,45 млн ₽**, что позволяет пройти порог EBITDA > 500 тыс. ₽/мес при разумном штате. [inference]
- **Вердикт**: **PASS**. Самый правдоподобный сценарий для РФ. [inference]

## Risks
- **Рынок узкий и небрендовый**: обязательный demand endpoint стабильно LOW. [T1/T2]
- **Нужен тяжелый enterprise sale**: само наличие прямых конкурентов с закрытыми прайсами указывает на сложную закупку и длинный цикл. [T2]
- **Локализация и контур данных**: hospital-grade deployment в РФ почти наверняка потребует local hosting, интеграций и compliance-by-design. [T2]
- **Telegram не помогает как wedge**: в РФ нет подтвержденного Telegram-native рынка для этого класса продукта. [T2]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: direct demand низкий, но Profit Gate проходит в двух enterprise-сценариях; SAM по двум методикам сходится в диапазоне **403-459 млн ₽**; WTP подтверждается международными внедрениями и существующим бюджетом на workflow software. [T1/T2]
- Почему не strong pass: в РФ это очень узкий рынок, зависимый от few-large-accounts, локального внедрения и длительного enterprise cycle. [T2]
- Что проверять дальше на P5/P6: реальный cost of implementation в РФ, наличие локального интеграционного партнера, требования по data residency и готовность 10 целевых buyers покупать не просто scheduling, а именно OR orchestration AI. [T2]

Sources: T1=3, T2=17, T3=0. Primary evidence basis: T2.


## Stage 4 — Economics

---
stage: economics
case: apella-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
sector: HEALTHCARE
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Apella AI как enterprise-платформа для perioperative coordination, OR utilization и hospital operations orchestration в крупных хирургических контурах РФ.

## Executive summary

**Итог P4/P5: CONDITIONAL PASS.**

Почему:
1. **Путь к EBITDA > 500 тыс. ₽/мес реалистичен** уже примерно на **13-15 активных hospital-клиентах** в base-case модели.
2. **LTV/CAC в стресс-сценарии ≈ 4.4x**, то есть выше минимального порога 3.0x, но без большого запаса для длинного enterprise-sale.
3. Экономика держится только в **high-ACV deployment motion** с локальной интеграцией, внедрением и ongoing optimisation, а не в low-touch SaaS для отдельной клиники.
4. Главные риски: **длинный цикл закупки, data residency / compliance, тяжёлый пресейл и ограниченный пул реально адресуемых buyers**.

## 1. Модель и ключевые допущения

### ICP
- крупные многопрофильные больницы и hospital groups;
- федеральные центры и private networks с высокой хирургической нагрузкой;
- buyer level: COO, главный врач, директор по хирургии, директор по цифровизации / ИТ;
- внедрение в контур OR scheduling, staffing, block utilization и perioperative command.

### Почему это не low-touch SaaS
Из `02-demand.md` видно, что рынок в РФ problem-led, а не category-led: search demand низкий, но операционная боль реальна. При этом сами международные игроки продают через enterprise motion с интеграцией в EHR/операционные процессы, а не как seat-based self-serve продукт. [T1][T2][T3][inference]

### Base-case для РФ
- Recurring subscription + support: **550 000 ₽/клиент/мес**
- One-off implementation / integration fee: **1 800 000 ₽**
- Onboarding считаю отдельно от recurring, как дополнительный cash-support.
- Sales ramp: **1 новый клиент в месяц** после первых 2-3 пилотных месяцев, затем 1-2 enterprise wins в квартал. [inference]

### Почему беру именно 550k ₽ MRR
Это выше обычного scheduling software и ближе к hospital-grade operations platform. Такой чек возможен только если продаётся не «софтина для расписания», а пакет:
- OR utilization analytics,
- case duration prediction,
- block release / scheduling optimisation,
- operational dashboards,
- внедрение и интеграция,
- ежемесячный optimisation layer.

## 2. Business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping hospital systems | Founder + analyst | manual research, registry, site review | 3 ч | 6 000 | Низкий |
| 2 | Intro через сеть / партнёров / конференции | Founder | warm outreach, calls | 4 ч | 16 000 | Низкий |
| 3 | Discovery с хирургическим и ops-контуром | Founder + solutions | Meet, audit checklist | 4 ч | 22 000 | Низкий |
| 4 | Оценка IT / данных / интеграций | Solutions + architect | integration scoping | 6 ч | 39 000 | Низкий |
| 5 | ROI model и pilot design | Founder + finance + solutions | business case | 5 ч | 31 000 | Низкий |
| 6 | Procurement / legal / infosec | founder + legal | договор, DPA, security pack | 10 ч | 55 000 | Низкий |
| 7 | Внедрение и интеграция | implementation lead | EHR / analytics / data mapping | 40 ч | 180 000 | Средний |
| 8 | Обучение OR-команды | CSM + implementation | workshops, SOPs | 10 ч | 35 000 | Средний |
| 9 | Первый 60-дневный optimisation cycle | CSM + analyst | dashboards, weekly ops reviews | 16 ч | 62 000 | Средний |
| 10 | Billing / collection | finance ops | invoice, acts | 2 ч | 5 000 | Высокий |

### Вывод по процессу
Продажа и delivery здесь очевидно **enterprise consultative**, с дорогим пресейлом и длинным implementation cycle. Это ухудшает CAC, но позволяет держать высокий ACV.

## 3. COGS per client / month

### Разбивка COGS на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| CSM / hospital ops support | 45 000 | еженедельные sync и сопровождение |
| Solutions / workflow optimisation | 52 000 | аналитика и рекомендации |
| Integration support / data engineering | 28 000 | поддержка контура и коннекторов |
| Clinical implementation QA | 18 000 | контроль качества rollout |
| Infra / hosting / monitoring | 17 000 | вычисления, storage, monitoring |
| Local compliance / security overhead | 10 000 | документация и security upkeep |
| Implementation amortization | 20 000 | spread тяжёлого onboarding на 12 мес |
| **Итого COGS** | **190 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **550 000 ₽**
- COGS на клиента: **190 000 ₽**
- Gross profit на клиента: **360 000 ₽**
- **Gross Margin = 65.5%**

### Комментарий
Для healthcare enterprise software с заметным services layer это хороший, но не выдающийся показатель. Если проект уйдёт в тяжёлый кастом или on-prem, GM может быстро опуститься к 50-55%.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/год | First meetings | Qualified pilots | Procurement-ready deals | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder / network | 24 | 12 | 7 | 4 | 2.0 | 8.3% |
| Integration / medtech partners | 20 | 10 | 6 | 3 | 1.5 | 7.5% |
| Conferences / industry events | 36 | 10 | 4 | 2 | 1.0 | 2.8% |
| Direct enterprise outbound | 60 | 12 | 4 | 1 | 0.5 | 0.8% |
| **Итого blended** | **140** | **44** | **21** | **10** | **5.0** | **3.6%** |

### Fully-loaded CAC

| Компонент | ₽/год | Как получено |
|---|---:|---|
| Founder-led enterprise sales allocation | 4 200 000 | 1 founder + travel + key meetings |
| Solutions presales / pilot design | 2 000 000 | solution architect и discovery cost |
| Industry events / networking / travel | 2 400 000 | конференции, визиты, demo-days |
| Marketing / content / credibility assets | 1 000 000 | кейсы, ROI materials, локализация |
| Legal / procurement / security support | 1 400 000 | DPA, infosec, tender overhead |
| Tools / CRM / data room / webinar | 500 000 | GTM stack |
| Overhead multiplier (x1.25) | 2 875 000 | management / admin overhead |
| **Итого acquisition spend** | **14 375 000** |  |

- New paying customers / год: **5.0**
- **Blended fully-loaded CAC = 14 375 000 / 5.0 = 2 875 000 ₽**

### CAC по каналам

| Канал | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---|
| Founder / network | 1 700 000 | лучший early channel |
| Integration / medtech partners | 2 300 000 | сильный channel, но ограничен |
| Conferences / industry events | 3 200 000 | нужен для trust-building |
| Direct enterprise outbound | 5 500 000 | дорогой и слабо предсказуемый |
| **Blended** | **2 875 000** | реалистичный base-case |

## 5. LTV и churn

### Допущение по churn
Для hospital operations платформы churn должен быть ниже, чем у обычного B2B SaaS, если продукт встроился в ежедневный workflow. Но локальный рынок маленький, а внедрение тяжёлое, поэтому беру **annual logo churn = 15%**. [inference]

### Расчёт
- MRR на клиента: **550 000 ₽**
- ARR на клиента: **6 600 000 ₽**
- Gross Margin: **65.5%**
- Annual churn: **15%**

`LTV = ARR × GM / churn`

`LTV = 6 600 000 × 65.5% / 15% = 28 820 000 ₽`

### Вывод
- **LTV = 28.82 млн ₽**
- Абсолютно это выглядит сильно, но только если hospital-клиенты реально живут 5+ лет и deployment становится sticky.

## 6. LTV / CAC

- LTV: **28 820 000 ₽**
- Blended fully-loaded CAC: **2 875 000 ₽**

`LTV/CAC = 28 820 000 / 2 875 000 = 10.0x`

### Stress-case
Чтобы не переоценить кейс, считаю стресс-сценарий:
- Effective GM year 1 = **48%**
- Annual churn = **24%**
- Effective CAC = **3 000 000 ₽**

`Stress LTV = 6 600 000 × 48% / 24% = 13 200 000 ₽`

`Stress LTV/CAC = 13 200 000 / 3 000 000 = 4.4x`

### Вердикт по метрике
- **Base-case LTV/CAC = 10.0x**
- **Stress-case LTV/CAC = 4.4x**
- Итог: метрика проходит, но запас прочности зависит от того, получится ли удерживать high-ACV и низкий churn.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`2 875 000 / 550 000 = 5.23 мес`

Это слишком оптимистично для enterprise healthcare, поэтому считаю **gross profit payback**:

`2 875 000 / 360 000 = 7.99 мес`

И затем добавляю procurement + pilot drag:
- **Practical payback = ~11-13 месяцев**

### Комментарий
Для hospital enterprise motion это ещё допустимо, но уже на грани. Если цикл оплаты уйдёт сильно дальше года, модель станет заметно тяжелее.

## 8. Contribution Margin %

- Revenue per client / мес: **550 000 ₽**
- COGS: **190 000 ₽**
- Variable account / field support / travel: **30 000 ₽**

`Contribution profit = 330 000 ₽`

`Contribution Margin = 330 000 / 550 000 = 60.0%`

### Вывод
**Contribution Margin = 60.0%**. Это позволяет строить прибыльную модель, если продукт не требует постоянного тяжёлого onsite-delivery.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| GM / founder | 1 | 450 000 | 0 | 0 | 135 000 | 585 000 |
| Enterprise AE / founder-assist | 1 | 260 000 | 1.5 | 2 | 78 000 | 338 000 |
| Solutions architect | 1 | 320 000 | 2 | 1.5 | 96 000 | 416 000 |
| Implementation manager | 1 | 260 000 | 1.5 | 1.5 | 78 000 | 338 000 |
| Clinical ops / perioperative SME | 1 | 300 000 | 2 | 2 | 90 000 | 390 000 |
| Data / integration engineer | 2 | 240 000 | 1.5 | 1.5 | 72 000 | 624 000 |
| CSM | 2 | 210 000 | 1 | 1 | 63 000 | 546 000 |
| Product / analytics | 1 | 260 000 | 1.5 | 1 | 78 000 | 338 000 |
| Legal / procurement / admin | 0.5 | 140 000 | 1 | 0.5 | 42 000 | 91 000 |
| Finance / ops | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 78 000 |
| **Итого full team FOT** | **11.0** |  |  |  |  | **3 744 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 3 744 000 |
| Office / legal / admin | 110 000 |
| Core infra not in COGS | 90 000 |
| G&A / бухгалтерия / bank / ЭДО | 70 000 |
| Travel / field visits / workshops | 170 000 |
| **Итого fixed costs** | **4 184 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **330 000 ₽**
- Fixed costs: **4 184 000 ₽/мес**

`Break-even clients = 4 184 000 / 330 000 = 12.7`

С operational buffer округляю до **13-15 активных клиентов**.

### Break-even by month
Если стартовать с темпа:
- M1-M3: pilot + 0.5-1 контракт в месяц,
- M4-M9: 1 контракт в месяц,
- M10-M18: 1-2 контракта в квартал сверху через network / partners,

то к operational break-even можно выйти примерно в **M16-M18**. [inference]

### Вывод
Для standalone healthcare motion break-even не быстрый, но достижимый. Это уже не «маленький SaaS», а узкий enterprise build.

## 12. Burn-to-breakeven и runway

### Burn в early stage
- Fixed costs: **4.18 млн ₽/мес**
- Acquisition spend run-rate: **~1.20 млн ₽/мес**
- Total pre-scale burn: **~5.38 млн ₽/мес**

### Burn-to-breakeven
При выходе к B/E около M16-M18 ориентир cumulative burn:
- **65-80 млн ₽** до уверенного operating break-even.

### Runway
При `startup_capital = 85 млн ₽`:
- runway ≈ **15-16 месяцев**,
- при нормальном росте выручки с M5-M6 effective runway может растянуться до **17-18 месяцев**.

## 13. Что происходит при 50 клиентах

### P&L snapshot при 50 клиентах
- Revenue: `50 × 550 000 = 27 500 000 ₽/мес`
- COGS: `50 × 190 000 = 9 500 000 ₽/мес`
- Gross profit: **18 000 000 ₽/мес**
- Variable account support: `50 × 30 000 = 1 500 000 ₽/мес`
- Contribution profit: **16 500 000 ₽/мес**
- Fixed costs: **4 184 000 ₽/мес**
- **EBITDA ≈ 12 316 000 ₽/мес**

### Вывод
Правило Program 2 выполняется уверенно: при **50 клиентах** модель сильно выше порога **EBITDA > 500 000 ₽/мес**.

## 14. Profit gate

### Проверка правила
FAIL только если:
- `company EBITDA < 500k/mo achievable even at 50 clients`, или
- `LTV/CAC < 1:1`

### Факт
- EBITDA при 50 клиентах: **~12.32 млн ₽/мес**
- Stress LTV/CAC: **4.4x**

## Итоговый вердикт P4/P5

**CONDITIONAL PASS.**

Кейс проходит economics-gate только как **узкий enterprise healthcare operations motion** с высоким ACV, долгим sales cycle и умеренно тяжёлым delivery.

### Что обязательно проверить дальше в P6/P7
1. Реалистичность локальных hospital procurement cycles и data residency требований.
2. Насколько повторяем deployment между больницами, без полного кастома каждый раз.
3. Есть ли сильный partner-led route-to-market через интеграторов и hospital IT.
4. Не съедают ли onsite-внедрения и clinical change management валовую маржу после 5-7 клиентов.
5. Насколько российские buyers готовы платить за OR optimisation layer, если уже живут на EHR + ручных процессах.

## Источники
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/apella-geo-expand-v2/02-demand.md
- [T2] Apella, Series B announcement, 2026-01-08: https://apella.io/blog/apella-raises-80-million-in-series-b-to-transform-the-hospital-with-ambient-ai-and-computer-vision
- [T3] Apella homepage / product positioning, accessed 2026-04-21: https://www.apella.io/
- [T4] LeanTaaS iQueue for Operating Rooms, results and OR metrics, accessed 2026-04-21: https://iqueue.com/products/operating-rooms/
- [T5] Qventus Surgical Growth, 11x ROI and utilization claims, accessed 2026-04-21: https://www.qventus.com/solutions/operating-room-utilization/
- [T6] Fierce Healthcare, Apella raise and customer expansion, 2026-01-08: https://www.fiercehealthcare.com/health-tech/or-optimization-platform-apella-raises-80m-fuel-health-system-expansion
- [T7] LeanTaaS / Baptist Health case signal, 16% increase in prime time utilization, 2022-10-06: https://leantaas.com/press-releases/baptist-health-and-leantaas-collaboration-in-improving-operating-room-utilization-included-in-2022-gartner-case-study/

<!-- P4-P5-DONE -->


## Stage 5 — Critic

# SECTION A — PnL (12 месяцев, 3 сценария)
## 1. Входные допущения для модели
- ARPA / MRR на клиента: **550 000 ₽/мес**
- COGS на клиента: **190 000 ₽/мес**
- Gross profit на клиента: **360 000 ₽/мес**
- Contribution margin на клиента: **330 000 ₽/мес**
- Fixed costs: **4 184 000 ₽/мес**, из них team FOT: **3 744 000 ₽/мес**
- Страховые взносы: **~30% к ФОТ** (уже включены в fully-loaded FOT)
- Annual churn: **15%**, эквивалентный monthly churn: **1,3%**
- CAC blended: **2 875 000 ₽** на нового клиента
- CAC по каналам: Founder/network **1 700 000 ₽**, partners **2 300 000 ₽**, conferences **3 200 000 ₽**, outbound **5 500 000 ₽**
- Для cash burn учтён cash CAC на новых клиентов, даже если PnL-строки ниже показывают EBITDA до налогов.

## 2. Сценарий Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 0 | 1 | 2 | 3 | 3,9 | 4,9 | 5,8 | 6,7 | 7,6 | 8,5 | 9,4 |
| MRR, ₽ | 0 | 0 | 550 000 | 1 092 601 | 1 627 904 | 2 156 005 | 2 677 003 | 3 190 992 | 3 698 067 | 4 198 321 | 4 691 845 | 5 178 731 |
| COGS, ₽ | 0 | 0 | 190 000 | 377 444 | 562 367 | 744 802 | 924 783 | 1 102 343 | 1 277 514 | 1 450 329 | 1 620 819 | 1 789 016 |
| Gross profit, ₽ | 0 | 0 | 360 000 | 715 157 | 1 065 537 | 1 411 203 | 1 752 220 | 2 088 649 | 2 420 553 | 2 747 992 | 3 071 026 | 3 389 715 |
| GM% | 0,0% | 0,0% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% |
| Fixed costs, ₽ | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 |
| EBITDA, ₽ | -4 184 000 | -4 184 000 | -3 824 000 | -3 468 843 | -3 118 463 | -2 772 797 | -2 431 780 | -2 095 351 | -1 763 447 | -1 436 008 | -1 112 974 | -794 285 |
| Cash burn, ₽ | 4 184 000 | 4 184 000 | 6 699 000 | 6 343 843 | 5 993 463 | 5 647 797 | 5 306 780 | 4 970 351 | 4 638 447 | 4 311 008 | 3 987 974 | 3 669 285 |
| Cumulative cash, ₽ | -4 184 000 | -8 368 000 | -15 067 000 | -21 410 843 | -27 404 306 | -33 052 102 | -38 358 882 | -43 329 233 | -47 967 680 | -52 278 688 | -56 266 662 | -59 935 948 |

- Break-even по client count: **13 клиентов** (математически), рабочий диапазон: **13-15 клиентов**.
- Break-even по месяцам: **не достигается в горизонте M1-M12**.
- Startup capital to BEP: **60 000 000 ₽**.

## 2. Сценарий Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 1 | 1 | 1 | 1 |
| Total clients | 0 | 1 | 2 | 3 | 3,9 | 4,9 | 5,8 | 7,7 | 8,6 | 9,5 | 10,4 | 11,2 |
| MRR, ₽ | 0 | 550 000 | 1 092 601 | 1 627 904 | 2 156 005 | 2 677 003 | 3 190 992 | 4 248 067 | 4 740 922 | 5 227 148 | 5 706 832 | 6 180 064 |
| COGS, ₽ | 0 | 190 000 | 377 444 | 562 367 | 744 802 | 924 783 | 1 102 343 | 1 467 514 | 1 637 773 | 1 805 742 | 1 971 451 | 2 134 931 |
| Gross profit, ₽ | 0 | 360 000 | 715 157 | 1 065 537 | 1 411 203 | 1 752 220 | 2 088 649 | 2 780 553 | 3 103 149 | 3 421 406 | 3 735 381 | 4 045 133 |
| GM% | 0,0% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% |
| Fixed costs, ₽ | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 |
| EBITDA, ₽ | -4 184 000 | -3 824 000 | -3 468 843 | -3 118 463 | -2 772 797 | -2 431 780 | -2 095 351 | -1 403 447 | -1 080 851 | -762 594 | -448 619 | -138 867 |
| Cash burn, ₽ | 4 184 000 | 6 699 000 | 6 343 843 | 5 993 463 | 5 647 797 | 5 306 780 | 4 970 351 | 7 153 447 | 3 955 851 | 3 637 594 | 3 323 619 | 3 013 867 |
| Cumulative cash, ₽ | -4 184 000 | -10 883 000 | -17 226 843 | -23 220 306 | -28 868 102 | -34 174 882 | -39 145 233 | -46 298 680 | -50 254 531 | -53 892 125 | -57 215 744 | -60 229 611 |

- Break-even по client count: **13 клиентов** (математически), рабочий диапазон: **13-15 клиентов**.
- Break-even по месяцам: **не достигается в горизонте M1-M12**.
- Startup capital to BEP: **61 000 000 ₽**.

## 2. Сценарий Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 1 | 0 | 1 | 0 |
| Total clients | 0 | 0 | 0 | 1 | 1 | 2 | 2,9 | 2,9 | 3,9 | 3,8 | 4,8 | 4,7 |
| MRR, ₽ | 0 | 0 | 0 | 550 000 | 542 601 | 1 085 302 | 1 620 703 | 1 598 901 | 2 127 393 | 2 098 775 | 2 620 543 | 2 585 291 |
| COGS, ₽ | 0 | 0 | 0 | 190 000 | 187 444 | 374 923 | 559 879 | 552 348 | 734 918 | 725 032 | 905 278 | 893 101 |
| Gross profit, ₽ | 0 | 0 | 0 | 360 000 | 355 157 | 710 380 | 1 060 824 | 1 046 554 | 1 392 475 | 1 373 744 | 1 715 264 | 1 692 191 |
| GM% | 0,0% | 0,0% | 0,0% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% | 65,5% |
| Fixed costs, ₽ | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 | 4 184 000 |
| EBITDA, ₽ | -4 184 000 | -4 184 000 | -4 184 000 | -3 824 000 | -3 828 843 | -3 473 620 | -3 123 176 | -3 137 446 | -2 791 525 | -2 810 256 | -2 468 736 | -2 491 809 |
| Cash burn, ₽ | 4 184 000 | 4 184 000 | 4 184 000 | 6 699 000 | 3 828 843 | 6 348 620 | 5 998 176 | 3 137 446 | 5 666 525 | 2 810 256 | 5 343 736 | 2 491 809 |
| Cumulative cash, ₽ | -4 184 000 | -8 368 000 | -12 552 000 | -19 251 000 | -23 079 843 | -29 428 463 | -35 426 639 | -38 564 086 | -44 230 610 | -47 040 866 | -52 384 602 | -54 876 411 |

- Break-even по client count: **13 клиентов** (математически), рабочий диапазон: **13-15 клиентов**.
- Break-even по месяцам: **не достигается в горизонте M1-M12**.
- Startup capital to BEP: **55 000 000 ₽**.

## 3. Waterfall на 1 клиента в месяц
| Метрика | ₽ | % от выручки |
|---|---:|---:|
| ARPA | 550 000 | 100,0% |
| Gross profit | 360 000 | 65,5% |
| Contribution profit | 330 000 | 60,0% |
| EBITDA after fixed-cost allocation at BEP (13 clients) | 8 154 | 1,5% |
| Net after tax, УСН 6% | -24 846 | -4,5% |
| Net after tax, IT-льгота 3% | -8 346 | -1,5% |
| Net after tax, ОСНО 20%* | -101 846 | n/a |

*ОСНО здесь показан консервативно: НДС 20% на выручку плюс 20% налог на прибыль на положительную прибыль после НДС. Для мед/IT-поставщика это worst-case cash-tax view, без детализации вычетов входящего НДС.*

## 4. Налоговая модель РФ
- **УСН 6%**: налог = 6% от выручки, без НДС. Для early-stage SaaS это самый понятный базовый режим.
- **IT-льгота 3%**: при аккредитации Минцифры и соблюдении критериев допустимо моделировать налоговую нагрузку как **3% от выручки**; это materially улучшает net margin и ускоряет выход в cash BEP.
- **ОСНО 20%**: для stress-view учитываю **НДС 20%** и **налог на прибыль 20%**. Если входящий НДС значим, реальная cash-нагрузка может быть мягче, но в консервативной модели ОСНО худший режим.
- **Страховые взносы ~30% к ФОТ** уже зашиты в fully-loaded payroll, отдельно повторно в EBITDA не начисляются.

## 5. Сводка по break-even
| Сценарий | New clients за 12 мес | Клиентов на M12 | EBITDA break-even month | Break-even client count | Startup capital to BEP, ₽ |
|---|---:|---:|---|---:|---:|
| Base | 10 | 9,4 | не достигнут | 13 | 60 000 000 |
| Optimistic | 12 | 11,2 | не достигнут | 13 | 61 000 000 |
| Pessimistic | 5 | 4,7 | не достигнут | 13 | 55 000 000 |

## 6. Вывод по PnL
- **Base**: к M12 компания остаётся ниже EBITDA break-even, но подходит к нему; нужен капитал порядка **60 млн ₽**.
- **Optimistic**: к M12 компания почти закрывает fixed-cost base, но полный break-even всё ещё скорее лежит сразу за горизонтом 12 месяцев; нужен капитал порядка **61 млн ₽**.
- **Pessimistic**: без ускорения продаж модель остаётся burn-heavy; нужен капитал порядка **55 млн ₽**.
- Главный финансовый рычаг здесь не ARPA, а **скорость набора hospital-клиентов при сохранении COGS discipline и налогового режима IT-льготы**.

<!-- P6A-DONE -->


## Stage 6 — Verdict

[HEALTHCARE] Apella AI — REJECTED: 59/100 | EBITDA base=766К₽/мес через 16-18 мес | LTV/CAC=10,0x | Ключевое преимущество: высокий ACV и measurable OR-efficiency wedge | Главный риск: РФ-спрос узкий, а p50 EBITDA @M24 ниже gate.

# 06-verdict

sector: HEALTHCARE
case: apella-geo-expand-v2
date: 2026-04-22
verdict: REJECTED
normalized_score: 59/100
committee: Program 7

## Investment committee verdict

**Вердикт: REJECTED.**

Кейс проходит economics-gate только как узкий hospital-enterprise продукт, но не дотягивает до investment grade из-за слабой ширины локального спроса, среднего moat, высокой execution-зависимости и schema drift в самом кейсе: вместо обязательных `02-validation.md` и `03-demand.md` присутствует только `02-demand.md`.

## Оценка

Source tier balance: T1=3, T2=17, T3=0, weighted=2.15. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «Gross Margin = 65.5%», «Base-case LTV/CAC = 10.0x», но «Practical payback = ~11-13 месяцев». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 16 | «Путь к EBITDA > 500 тыс. ₽/мес реалистичен уже примерно на 13-15 активных hospital-клиентах», но «p50 EBITDA @M24 = 450 000». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «Итог по спросу в РФ: LOW», при этом «hh.ru vacancies = 114» и «SAM... 403-459 млн ₽»; применён tier penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Продукт может встроиться в OR-workflow, но нет network effects и локальный moat в РФ пока не доказан. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | «Главные риски: длинный цикл закупки, data residency / compliance, тяжёлый пресейл и ограниченный пул реально адресуемых buyers». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 16 | «Founder/network 1.7 млн ₽», «partners 2.3 млн ₽», но GTM реалистичен только через named-account enterprise motion. |

**Сумма raw = 89/150. Normalized score = round((89 × 100) / 150) = 59/100.**

## Moat — 7-factor framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый hospital-клиент не улучшает продукт для остальных напрямую. |
| 2. Switching costs | 2 | После внедрения в OR-процессы и dashboards смена поставщика болезненна. |
| 3. Scale economies | 1 | Часть COGS падает с объёмом, но services-layer остаётся тяжёлым. |
| 4. Proprietary data / model advantage | 1 | Есть потенциальный data flywheel, но локальный объём данных и dataset advantage не доказаны T1/T2 по РФ. |
| 5. Regulatory moat | 1 | Compliance важен, но подтверждённого лицензируемого или аккредитационного moat нет. |
| 6. Brand / distribution | 1 | Международный бренд есть, но локальной hospital-distribution в РФ нет. |
| 7. Embedded workflow | 3 | При успешном rollout решение глубоко встраивается в perioperative coordination. |

**Sum_7factor = 9/21. Moat score = round((9 × 25) / 21) = 11/25.**

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account mapping hospital systems | Founder + analyst | manual research, registry, site review | 3 ч | 6 000 | Низкий |
| 2 | Intro через сеть / партнёров / конференции | Founder | warm outreach, calls | 4 ч | 16 000 | Низкий |
| 3 | Discovery с хирургическим и ops-контуром | Founder + solutions | Meet, audit checklist | 4 ч | 22 000 | Низкий |
| 4 | Оценка IT / данных / интеграций | Solutions + architect | integration scoping | 6 ч | 39 000 | Низкий |
| 5 | ROI model и pilot design | Founder + finance + solutions | business case | 5 ч | 31 000 | Низкий |
| 6 | Procurement / legal / infosec | founder + legal | договор, DPA, security pack | 10 ч | 55 000 | Низкий |
| 7 | Внедрение и интеграция | implementation lead | EHR / analytics / data mapping | 40 ч | 180 000 | Средний |
| 8 | Обучение OR-команды | CSM + implementation | workshops, SOPs | 10 ч | 35 000 | Средний |
| 9 | Первый 60-дневный optimisation cycle | CSM + analyst | dashboards, weekly ops reviews | 16 ч | 62 000 | Средний |
| 10 | Billing / collection | finance ops | invoice, acts | 2 ч | 5 000 | Высокий |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 28 820 000 ₽ |
| CAC blended | 2 875 000 ₽ |
| LTV/CAC | 10.0x |
| CAC payback | 5.23 мес |
| Gross profit payback | 7.99 мес |
| practical CAC payback | ~11-13 мес |
| Gross Margin | 65.5% |
| contribution_margin_rub_month | 330 000 ₽/клиент/мес |
| company_ebitda_rub_month base @M12 | -794 285 ₽/мес |
| company_ebitda_potential_rub_month | 766 000 ₽/мес |
| clients_to_500k_ebitda | 15 |
| months_to_500k_ebitda | 16-18 |
| Break-even clients | 13 |
| startup_capital_to_bep_rub | 60 000 000 ₽ |

## Команда

| Роль | Нужно чел. | FOT fully-loaded ₽/мес |
|---|---:|---:|
| GM / founder | 1 | 585 000 |
| Enterprise AE / founder-assist | 1 | 338 000 |
| Solutions architect | 1 | 416 000 |
| Implementation manager | 1 | 338 000 |
| Clinical ops / perioperative SME | 1 | 390 000 |
| Data / integration engineer | 2 | 624 000 |
| CSM | 2 | 546 000 |
| Product / analytics | 1 | 338 000 |
| Legal / procurement / admin | 0.5 | 91 000 |
| Finance / ops | 0.5 | 78 000 |
| **Итого** | **11.0** | **3 744 000** |

## Top-3 risks

| Риск | Probability | Impact | Почему важно |
|---|---|---|---|
| Узкий локальный спрос и evidence_quality_unverified | High | High | В кейсе отсутствуют обязательные `02-validation.md` и `03-demand.md`, а прямой спрос в РФ отмечен как LOW. |
| Weak moat | Medium | High | Moat score = 11/25, локальный distribution moat и proprietary data advantage не доказаны. |
| Procurement / compliance / data residency | High | High | Hospital sales cycle длинный, а security, DPA и локальный контур могут растянуть внедрение за пределы payback. |

## GTM — 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | НМИЦ хирургии им. А. В. Вишневского | Большой хирургический контур, высокая цена простоя операционных | email decision-maker + профильные медконференции | 550 000 ₽/мес |
| 2 | НМИЦ им. В. А. Алмазова | Сложные хирургические маршруты и федеральный масштаб | партнёрство через интегратора / digital health vendor | 600 000 ₽/мес |
| 3 | НМИЦ онкологии им. Н. Н. Блохина | Высокая нагрузка на OR и значимый throughput pain | email директору по хирургии / ИТ | 650 000 ₽/мес |
| 4 | НМИЦ трансплантологии им. В. И. Шумакова | Дорогие и критичные операционные слоты, нужен orchestration layer | конференция + warm intro через medtech-партнёра | 700 000 ₽/мес |
| 5 | ГКБ им. С. П. Боткина | Большой городской хирургический контур, pain по загрузке и координации | tender/integrator route + личные встречи | 500 000 ₽/мес |
| 6 | НИИ СП им. Н. В. Склифосовского | Высокая интенсивность и операционная сложность | email decision-maker + pilot proposal | 600 000 ₽/мес |
| 7 | European Medical Center (EMC) | Частный premium hospital, быстрее enterprise purchase и выше willingness to pay | founder-led outreach / private healthcare events | 700 000 ₽/мес |
| 8 | МЕДСИ | Сетевая частная медицина, можно продавать network-level rollout | партнёрство + conference follow-up | 750 000 ₽/мес |
| 9 | MD Medical Group / Мать и дитя | Сетевой оператор с хирургическим объёмом и digital maturity | email COO / директорам клиник | 550 000 ₽/мес |
| 10 | АО «Медицина» | Premium private hospital, понятный buyer и KPI по utilisation | founder network + case-based pitch | 500 000 ₽/мес |

## Что нужно доказать для пересмотра

1. Не менее 3 платных пилотов или LOI от крупных hospital systems в РФ.
2. Реальный blended CAC ≤ 2.3 млн ₽ и payback ≤ 12 месяцев с учётом procurement.
3. Повторяемый rollout без bespoke-разработки, где COGS/client удерживается ≤ 190 тыс. ₽/мес.
4. Подтверждение, что company_ebitda_rub_month > 500 тыс. ₽ достигается не только в optimistic, но и в median-case.

## LTV Upside Calculator

Так как кейс **REJECTED**, ниже что должно улучшиться, чтобы score мог выйти в near-pass/approve:

| Рычаг | Текущее | Целевое | Эффект |
|---|---:|---:|---|
| ARPA | 550 000 ₽/мес | 650 000-700 000 ₽/мес | Улучшает EBITDA и снижает требуемое число клиентов до 500k EBITDA. |
| CAC blended | 2 875 000 ₽ | ≤2 300 000 ₽ | Даёт больше запаса по GTM и Monte Carlo median. |
| Annual churn | 15% | ≤12% | Повышает customer_ltv_rub и усиливает switching-cost story. |
| COGS/client | 190 000 ₽/мес | ≤160 000 ₽/мес | Расширяет GM и делает rollout менее service-heavy. |
| Signed targets | 0 | ≥3 пилота / LOI | Снимает основной demand-risk и повышает критерии #3 и #6. |

## Proof points, которых не хватило до approve

- Нет подтверждения, что в РФ category demand уже превратился в устойчивый software budget, а не только в staffing pain.
- Нет локально доказанного moat по данным, интеграциям или distribution.
- Median-case из Monte Carlo не проходит gate: p50 EBITDA @M24 = 450 000 ₽/мес.

## Итог комитета

Apella AI выглядит сильнее большинства healthcare workflow идей по unit economics, но пока это скорее качественный enterprise hypothesis, чем investment-ready кейс для РФ. На текущих данных фондовый апсайд слишком зависит от нескольких крупных госпитальных сделок, а запас прочности по спросу и moat недостаточен.

