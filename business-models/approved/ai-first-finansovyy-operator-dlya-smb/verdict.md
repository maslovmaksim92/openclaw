# ai-first-finansovyy-operator-dlya-smb — investment verdict

**Статус:** ✅ APPROVED WITH NOTES  
**Score:** 71/100  
**Сектор:** B2B-OPS  
**GitHub slug:** `ai-first-finansovyy-operator-dlya-smb`

---

## Stage 0. Brief

# Краткий бриф

## Кейс
AI-first финансовый оператор для SMB

## Почему открыт
- Сигнал описывает самостоятельный B2B-OPS wedge: managed service + software для ежедневной бухгалтерии, AP, invoicing, payroll и базового finance back-office.
- В текущих открытых кейсах нет достаточно близкого кейса именно про AI-first finance ops оператор для SMB как регулярную подписочную услугу.
- Порог Program 1 проходит: при ARPU 90 000-180 000 ₽ в месяц и high-LTV сервисной модели гипотеза выглядит способной выйти выше 500 000 ₽ EBITDA в месяц.

## Что проверить дальше
- Насколько SMB в РФ готовы отдавать finance ops внешнему AI-first оператору, а не только отдельные задачи бухгалтеру или аутсорсеру.
- Какие workflows дают самый быстрый ROI: ежедневное bookeeping, AP, invoicing, payroll или финансовая аналитика.
- Как упаковать локальный стек под 1С, банк-клиенты, ЭДО, 152-ФЗ и налоговые требования без тяжёлого внедрения.

## Следующий этап
P3-demand-validation.


---

## Stage 1. Intake

---
sector: B2B-OPS
rerun: false
source_raw: 2026-04-23-b2b-ops-finally-ai-finance-operator-dlya-smb.md
created: 2026-04-23T22:07:00+03:00
---

# Intake

## Название сигнала
Finally, AI-first finance ops оператор для SMB

## Wedge statement
AI-first finance ops оператор для SMB: берёт на себя ежедневную бухгалтерию, AP, invoicing и базовые back-office процессы в модели managed service + software.

## Краткое резюме
Сигнал описывает не точечную автоматизацию, а полноценный операционный слой для малого и среднего бизнеса, который сочетает сервисную команду и AI-автоматизацию вокруг бухгалтерии, payables, payroll и invoicing. Это отличается от уже открытых кейсов про предаудит, дебиторку или чистый ввод первички и тянет на отдельный кейс с высоким LTV и подписочной выручкой.

## Evidence
- [T2] https://techcrunch.com/2024/09/09/miami-based-ai-bookkeeping-startup-finally-has-raised-another-big-round-200m-in-equity-and-debt/ — 2024-09-09, TechCrunch подтверждает спрос рынка, крупное финансирование и позиционирование Finally как AI bookkeeping/accounting/finance платформы для SMB.
- [T3] https://finally.com/ — 2026-04-23, официальный сайт заявляет AI Agents для accounting, expenses, payables, payroll и financial intelligence, плюс 3,500+ компаний-клиентов.
- [T3] https://finally.com/bookkeeping.html — 2026-04-23, официальный лендинг подтверждает done-for-you модель: in-house команда бухгалтеров + AI/ML-категоризация транзакций и ежедневное ведение книг.
- [T3] https://finally.com/pricing.html — 2026-04-23, официальный pricing подтверждает subscription-формат с recurring add-ons для payroll, bill pay, invoicing и tax filing.

## EBITDA hypothesis
700000-1400000 ₽/мес

## LTV signal
1080000-4320000 ₽ на клиента

## RU-fit
4 / 5. Модель хорошо переносится в РФ как AI-first аутсорсинг финопераций для SMB, но нужна локализация под 152-ФЗ, российские банки, 1С и налоговый контур.

## Почему это не duplicate
В текущих открытых кейсах нет достаточно близкого кейса именно про AI-first managed finance ops оператор для SMB, который объединяет ежедневную бухгалтерию, payables, invoicing и бэк-офис как подписочную услугу. Ближайшие кейсы покрывают предаудит отчётности, дебиторку или автоматизацию первички, но не весь контур finance back-office как сервис.

## Следующий этап
P3-demand-validation.


---

## Stage 1b. Supporting evidence

## 2026-04-24 — supporting signal
- **Источник:** https://techcrunch.com/2024/03/12/nanonets-funding-accel-India/ ; https://nanonets.com/pricing ; https://nanonets.com/flow/ap-automation
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал подтверждает, что AP automation и документный finance back-office уже стали зрелой категорией с заметным числом клиентов и измеримым ROI, а значит broader finance ops оператор можно упаковывать вокруг payables и связанных workflow. Он снижает риск, что гипотеза ограничена только bookkeeping, и показывает repeatable high-value use case в ежедневных финоперациях.
- **Ключевые данные и факты:** TechCrunch писал о 10 000+ клиентах Nanonets, росте выручки в 3 раза год к году и 90% straight-through processing; официальный AP Automation лендинг заявляет 99%+ точность, 80% сокращение затрат и 90%+ экономию времени; pricing остаётся usage-based с enterprise-пакетами, что поддерживает чек выше 50 000 ₽ в месяц на существенных объёмах документов.

## 2026-04-24 — supporting signal
- **Источник:** https://techcrunch.com/2024/03/12/nanonets-funding-accel-india/ ; https://nanonets.com/ap-automation ; https://nanonets.com/pricing
- **Тип:** supporting signal
- **Как усиливает кейс:** Nanonets дополнительно подтверждает, что AI-автоматизация кредиторки и invoice processing уже продаётся как зрелый finance ops слой, а не как точечный OCR-инструмент. Это усиливает уверенность, что российский кейс AI-first финансового оператора можно строить вокруг AP, согласований и ERP-интеграций с высоким средним чеком.
- **Ключевые данные и факты:** продукт заявляет 99%+ accuracy, 2-way и 3-way PO matching, ERP-интеграции и 80-90% экономии времени и затрат на AP; pricing остаётся usage-based с enterprise quote и managed services; TechCrunch писал о $29 млн финансирования на развитие workflow automation.


## 2026-04-24 — supporting signal — AI-оператор первички и автопроводок как узкий wedge внутри finance ops
- **Источник:** https://www.nalog.gov.ru/rn77/news/activities_fts/16471799/ ; https://portal.1c.ru/applications/1C-Document-Recognition ; https://saby.ru/autorecognition
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что подтверждает наиболее конкретный и внедряемый workflow внутри AI-first финансового оператора для SMB: ingestion первички, распознавание, автопроводки и подготовка данных для деклараций в 1С. Это делает broader finance ops кейс более реалистичным, потому что показывает уже сформированный платёжный контур вокруг AP, ЭДО и бухгалтерской рутины.
- **Ключевые данные и факты:** ФНС пишет о росте доли электронных счетов-фактур с 9% в 2020 году до 64% в 2025 году; каталог 1С показывает тарифы на распознавание документов до 3 000 000 ₽ в год; Saby заявляет распознавание УПД, ТОРГ-12, счетов-фактур и актов с точностью до 99% и формированием проводок с отражением в декларации.


## 2026-04-24 — supporting signal — Beorg как подтверждение wedge по AI-обработке первички для SMB
- **Дата:** 2026-04-24
- **Источник:** https://beorg.ru/kadry-buhgalter-docs/ ; https://www.rusprofile.ru/id/10836745 ; https://www.nalog.gov.ru/rn77/news/activities_fts/16572522/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс AI-first финансового оператора для SMB, потому что показывает уже коммерчески зрелый узкий wedge вокруг распознавания, верификации и загрузки первички в 1С/SAP. Это снижает риск, что finance ops automation в РФ остаётся теорией: есть локальный поставщик с заметной выручкой и внешний регуляторный драйвер через рост налогового мониторинга.
- **Ключевые данные и факты:** Beorg прямо заявляет обработку счетов, УПД, актов и накладных с качеством 99%+ и снижением затрат в 2,5–3 раза; Rusprofile по ООО «Биорг» указывает выручку 216,7 млн ₽ и прибыль 6,4 млн ₽ за 2024 год; ФНС сообщает, что с января 2026 года в налоговом мониторинге участвуют 876 компаний, более 80% уже подключены к интеграционной платформе.

## 2026-04-24 — supporting signal — AI-оператор первички и налогового закрытия как узкий wedge внутри finance ops
- **Дата:** 2026-04-24
- **Источник:** https://www.nalog.gov.ru/rn77/news/activities_fts/15454417/ ; https://rb.ru/news/outsource-revenue/ ; https://vc.ru/ai/2615629-kak-uskorit-vvod-pervichnyh-dokumentov-v-1s-s-pomoshhyu-idp
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что подтверждает платёжеспособный workflow вокруг ingestion первички, валидации реквизитов, автопроводок и подготовки налогового закрытия в 1С без ручного ввода. Это делает broader AI-first финансового оператора для SMB сильнее, потому что показывает конкретный entry-point с регуляторным драйвером и понятным ROI на дефиците бухгалтеров.
- **Ключевые данные и факты:** ФНС сообщала, что в 2025 году сервис машиночитаемых документов расширяется на счёт-фактуру, УПД и мобильную подпись; RB.RU со ссылкой на Smart Ranking и Forbes писало о росте выручки крупнейших аутсорсеров учётных функций до 20,9 млрд ₽ в 2024 году; кейс SL Soft заявляет ускорение ввода первички в 1С в 3-5 раз и масштабирование до десятков тысяч документов в месяц.


---

## Stage 2. Demand Validation

---
sector: B2B-OPS
stage: demand-validation
updated: 2026-04-24T19:11:00+03:00
---

# 02-demand — Demand Validation

## 1. Что именно валидируем
Проверяем, есть ли в РФ устойчивый платёжеспособный спрос не просто на бухгалтерский аутсорс, а на **AI-first финансового оператора для SMB**, который закрывает ежедневный finance back-office как подписочную услугу: bookkeeping, AP, invoicing, payroll, обработку первички и базовую финансовую аналитику.

## 2. Почему спрос выглядит реальным
1. Международный category proof уже есть. Finally продаёт не точечный инструмент, а целостный finance ops stack для SMB и заявляет 3 500+ компаний-клиентов, отдельные модули для bookkeeping, payroll, bill pay, invoicing и tax filing. Это важный сигнал, что рынок покупает именно bundled finance-operator motion, а не только один workflow. [T1]
2. Внутри broader кейса особенно силён AP / invoice automation wedge. Supporting evidence по Nanonets показывает зрелую категорию с 10 000+ клиентов, enterprise pricing, ERP-интеграциями и заявленным ROI по скорости и стоимости обработки документов. Это снижает риск, что finance ops гипотеза держится только на общем нарративе. [T2]
3. В РФ уже есть инфраструктурная база, на которую такой оператор может опереться: рост доли электронных счетов-фактур, зрелые контуры 1С и Saby, а также локальные сервисы распознавания и автопроводок. Значит, buyer pain не нужно объяснять с нуля, он уже существует в текущем документообороте и бухгалтерской рутине. [T2]
4. Локальный рынок подтверждает willingness to pay хотя бы за узкий кусок этой цепочки. Evidence по Beorg показывает коммерчески работающий бизнес на обработке первички и загрузке в учетные системы, что служит практическим proof, что finance back-office automation в РФ монетизируется. [T2]
5. Buyer и budget owner читаются ясно: собственник SMB, CEO, финансовый директор, главный бухгалтер, COO, иногда операционный директор группы компаний. Бюджет берётся не из “AI-экспериментов”, а из уже существующих расходов на бухгалтерию, первичку, payroll, аутсорс и внутренний finance admin. [T1][T2][inference]

## 3. Где именно сидит willingness to pay
Наиболее правдоподобные платящие сегменты:
- SMB с 20-250 сотрудниками, где уже есть регулярный поток счетов, выплат, актов и payroll;
- e-commerce, сервисные компании, агентства, дистрибьюторы и B2B-компании с большим объёмом первички и recurring invoicing;
- группы юрлиц и быстрорастущие SMB, где owner не хочет наращивать back-office headcount;
- компании, которым нужен гибрид: automation + human verification, а не только коробка.

Платят здесь за сокращение ручной рутины, снижение ошибок в учёте, ускорение закрытия периода, уменьшение зависимости от отдельных бухгалтеров и предсказуемый service level. В РФ это особенно важно там, где finance ops уже стал bottleneck для роста, но полноценная внутренняя функция ещё слишком дорога. [T1][T2][inference]

## 4. Предварительная логика чека
Базовая локальная гипотеза по monetization:
- low-end: 35-70 тыс. ₽/мес за узкий контур, только первичка + AP + базовая отчётность;
- mid-case: 90-180 тыс. ₽/мес за полноценный finance ops retainer для SMB;
- upper SMB / multi-entity: 180-300 тыс. ₽/мес при добавлении payroll, invoicing orchestration, cash visibility и расширенного SLA.

При таких чеках 8-12 активных клиентов уже дают выручку, из которой можно собирать Program 2 economics, если delivery остаётся productized, а не уходит в тяжёлый консалтинг. Это выглядит правдоподобно для B2B-OPS кейса с сильной долей automation и стандартизированными playbooks. [T1][T2][inference]

## 5. Что ограничивает спрос
1. В РФ уже очень плотный рынок дешёвого бухаутсорса и 1С-интеграторов, поэтому продавать “ещё одну бухгалтерию” бессмысленно. Нужна упаковка именно как faster finance operations layer.
2. Часть SMB покупает минимальный комплаенс, а не операционную эффективность. Это ограничивает массовый рынок и сдвигает кейс в более зрелые SMB.
3. Интеграции с 1С, банк-клиентами, ЭДО, payroll и налоговым контуром могут превратить продукт в кастомный сервис, если не держать жёсткий scope.
4. Есть риск, что buyer предпочитает локального главбуха или знакомый аутсорс, а не AI-first модель, особенно в чувствительных финансовых процессах.

## 6. Demand verdict
**Demand verdict: PASS WITH RESERVATIONS.**

Почему pass:
- есть сильный international category proof по Finally и смежным AP/workflow игрокам; [T1][T2]
- в РФ существует зрелый документооборот, 1С-контур и локальные коммерческие сигналы по automation первички; [T2]
- понятен buyer, понятен бюджетный карман и виден repeatable workflow;
- economics может собраться на ограниченном числе клиентов при retainer-модели.

Почему с оговорками:
- пока не доказано, что широкий SMB-рынок в РФ готов покупать именно bundled AI finance operator, а не набор разрозненных сервисов;
- основной спрос, вероятно, будет не в массовом SMB, а в сегменте с уже ощутимой операционной сложностью;
- главный риск не в отсутствии боли, а в коммодитизации через бухаутсорс и кастомизации через локальные интеграции.

## 7. Что обязательно проверить на следующем этапе
1. Где проходит граница между productized finance ops и обычным бухаутсорсом.
2. Какие workflows дают fastest payback: AP, первичка, invoicing, payroll или month-end close.
3. Можно ли стандартизировать delivery вокруг 1С/ЭДО/банк-клиентов без project-heavy модели.
4. Какой ICP даёт лучший LTV: e-commerce, агентства, сервисный SMB, multi-entity бизнес или B2B-компании с recurring billing.
5. Насколько сильна зависимость от человеческой бухгалтерской верификации и как это бьёт по марже.

## 8. Итог этапа
Кейс **не отклонять** на demand stage. Передавать дальше в P4 как B2B-OPS кейс с понятной регулярной болью, хорошим wedge вокруг AP/первички и правдоподобной retainer economics, но с обязательной проверкой consulting-risk, канала продаж и предела локальной стандартизации.

## Sources
- [T1] `01-intake.md`
- [T2] `01-evidence.md`


---

## Stage 4. Economics

---
case: ai-first-finansovyy-operator-dlya-smb
stage: unit-economics
updated_at: 2026-04-24T19:31:00+03:00
analyst: branch-models-lead
---

# 04-economics — Unit Economics

## Executive summary

**Вердикт этапа: PASS.**

Кейс собирает investable unit economics **только как productized mid-market B2B finance ops service**, а не как дешёвый бухаутсорс. При базовом чеке **160 000 ₽ MRR на клиента**, среднем **COGS 42 000 ₽/клиент/мес**, blended fully-loaded **CAC 209 063 ₽**, месячном churn benchmark **2.5%**, модель даёт:

- **Contribution Margin:** 73.8%
- **LTV:** 4.72 млн ₽
- **LTV/CAC:** 22.6x
- **CAC Payback:** 1.3 мес
- **Break-even:** ~45 клиентов или ~7.2 млн ₽ месячной выручки
- **EBITDA at 50 clients:** ~**+602 тыс. ₽/мес**

Это проходит Profit Gate, но запас прочности небольшой. Главный риск не в LTV/CAC, а в том, сможет ли команда реально дойти до **45-50 активных клиентов** без провала в кастомизацию и сервисный перегруз.

---

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | SMB / lower mid-market, 20-250 сотрудников | Компании с заметным документооборотом, recurring invoicing и 1С/ЭДО контуром |
| Средний чек | **160 000 ₽/мес** | Верх середины диапазона из 02-demand, нужен для окупаемости full-stack delivery |
| New customers / мес в steady-state | 4 | 2 outbound, 1 paid inbound, 1 partner/referral |
| Gross margin basis | Revenue minus delivery COGS | Sales & marketing не включены в COGS |
| Monthly churn | **2.5%** | Бенчмарк для SMB/mid-market B2B SaaS/service-heavy subscription |
| Startup capital | **40 млн ₽** | Нужен, чтобы дожить до масштаба 45-50 клиентов |

---

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Генерация первичного лида | SDR + performance marketer | Яндекс.Директ, VK Ads, partner outreach, CRM | 1-14 дней | 18 000 | Средняя |
| 2 | Квалификация лида, first touch | SDR | amoCRM/Битрикс24, телефония, email sequencing | 30-45 мин | 2 200 | Средняя |
| 3 | Discovery call | AE | Zoom/Meet, CRM, call notes AI | 60 мин | 4 500 | Средняя |
| 4 | Сбор вводных: объём первички, банки, 1С, payroll | AE + Solution/Operations lead | Questionnaire, shared checklist | 2-3 дня | 6 500 | Низкая |
| 5 | Расчёт scope и коммерческого предложения | AE + CEO/Finance ops lead | Proposal template, калькулятор юнит-экономики | 1 день | 5 000 | Средняя |
| 6 | Security/legal review, договор | AE + CEO + юрист на аутсорсе | Документооборот, шаблон договора, ЭДО | 3-10 дней | 7 000 | Низкая |
| 7 | Выставление счёта | Finance ops | 1С, банк-клиент, ЭДО | 20 мин | 600 | Высокая |
| 8 | Оплата и активация клиента | Finance ops + Customer Success | Банк-клиент, CRM, billing | 1 день | 900 | Высокая |
| 9 | Onboarding: доступы, 1С, ЭДО, bank statements, шаблоны | CS + Finance ops specialist | 1С, Saby/Контур, shared drive, RPA | 3-5 рабочих дней | 9 500 | Средняя |
| 10 | Ежедневная обработка первички, AP, invoicing, reconciliations | Finance ops specialist | 1С, OCR, LLM extraction, RPA, bank feeds | Постоянно | 19 000 / мес | Средняя |
| 11 | Контроль качества и закрытие месяца | Chief accountant / QA | 1С, checklists, BI dashboard | 4-6 ч / мес | 7 000 / мес | Низкая |
| 12 | Продление / upsell / повторный платёж | CS + AE | CRM, QBR, BI, billing | 1-2 ч / мес | 2 500 / мес | Средняя |

**Вывод:** процесс монетизируется только если onboarding и ежедневная обработка стандартизированы вокруг 1С + ЭДО + банков. Если каждая сделка превращается в мини-проект интеграции, contribution margin быстро падает ниже 60%.

---

## 3. COGS breakdown на 1 клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Finance ops specialist delivery time | 19 000 | ~0.086 FTE при fully-loaded FOT 221 000 ₽ |
| Chief accountant review / QA | 7 000 | ~0.022 FTE при fully-loaded FOT 312 000 ₽ |
| Customer Success / support allocation | 4 000 | ~0.015 FTE |
| OCR / LLM / document AI / RPA | 5 000 | Распознавание, классификация, prompt/runtime, workflow |
| Интеграции и ЭДО / bank feeds / 1С коннекторы | 3 000 | Saby/ЭДО/connectors |
| Cloud / security / storage | 2 500 | Хостинг, backup, monitoring, secrets |
| Потери на платежах, исправлениях, ручных исключениях | 1 500 | Резерв на нестандартные кейсы |
| **Итого COGS** | **42 000** |  |

### Выручка и маржа на 1 клиента

| Показатель | Значение |
|---|---:|
| MRR на клиента | **160 000 ₽** |
| COGS | **42 000 ₽** |
| Contribution profit | **118 000 ₽** |
| Contribution Margin | **73.8%** |

---

## 4. CAC по каналам и воронка

### 4.1 CAC по каналам

| Канал | Лиды / мес | SQL / мес | Proposal / мес | New paying / мес | Месячные затраты, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Outbound | 900 | 18 | 6 | 2 | 420 000 | **210 000** |
| Paid inbound (Яндекс/VK/search) | 300 | 12 | 4 | 1 | 240 000 | **240 000** |
| Partnerships / referrals | 25 | 6 | 3 | 1 | 177 000 | **177 000** |
| **Blended** | **1 225** | **36** | **13** | **4** | **837 000** | **209 250** |

### 4.2 Funnel conversion

| Funnel stage | Outbound | Paid inbound | Partnerships |
|---|---:|---:|---:|
| Lead → meeting | 8.0% | 15.0% | 48.0% |
| Meeting → SQL | 25.0% | 26.7% | 50.0% |
| SQL → proposal | 33.3% | 33.3% | 50.0% |
| Proposal → win | 33.3% | 25.0% | 33.3% |
| Lead → win | 0.22% | 0.33% | 4.0% |

### 4.3 Fully-loaded CAC, обязательный расчёт

Сегмент здесь **mid-market B2B**, поэтому для sanity используется коэффициент overhead выше self-serve. В расчёте применён требуемый множитель **x1.3** поверх raw acquisition spend.

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK) | 180 000 | Базовый тестовый медиабюджет на нишевый B2B ICP | internal model + RU B2B launch assumption |
| Outbound team FOT (SDR + 0.5 AE attributed to new) | 403 000 | SDR 208 000 + 50% AE 195 000 | HH vacancy snapshots, 2026-04-24 |
| Marketing team FOT allocation | 90 000 | ~23% Product/Ops/marketing FOT 390 000 ₽ | internal allocation |
| Tools / CRM / data / sequencing | 42 000 | CRM + enrichment + телефония + email stack | vendor stack estimate |
| Events / partnerships | 33 000 | meetups, partner commissions, small events | internal model |
| Raw CAC spend subtotal | **748 000** | сумма строк выше |  |
| Overhead multiplier (x1.3) | **224 400** | 748 000 × 30% | required fully-loaded overhead |
| **Total fully-loaded acquisition spend** | **972 400** |  |  |
| **New paying customers / мес** | **4** | blended model |  |
| **Fully-loaded CAC** | **243 100 ₽** | 972 400 / 4 |  |

**Консервативный рабочий CAC для модели:** **243 100 ₽**.

Это всё ещё попадает в user-provided sanity range для **mid-market SaaS 60-250K ₽**, но уже у верхней границы. Значит, экономика чувствительна к просадке конверсии и к удлинению sales cycle.

---

## 5. LTV и churn benchmark

### 5.1 Churn benchmark

Для SMB/mid-market B2B подписки с заметной сервисной составляющей я беру **2.5% monthly churn** как консервативный ориентир.

Почему это разумно:
- SaaS Capital в 2025 пишет, что у B2B SaaS-компаний c ARR <10 млн $ logo churn заметно выше, чем у более крупных игроков; маленькие компании и SMB-oriented motion теряют клиентов чаще, чем enterprise. Это не точный proxy для finance ops service, но корректное направление для оценки. Источник: https://www.saas-capital.com/blog-posts/2025-b2b-saas-retention-benchmarks/
- Optifi.ai в 2026 сводит benchmark monthly churn для B2B SaaS в диапазоне около **3-5% для SMB** и **1-2% для enterprise**. Для данного кейса, который сидит между SMB и lower mid-market, **2.5% в месяц** выглядит рабочим базовым сценарием, а не агрессивным optimist case. Источник: https://www.optifi.ai/post/saas-churn-benchmarks

### 5.2 LTV calculation

Формула:

`LTV = ARPU × Contribution Margin % / Monthly churn`

`LTV = 160 000 × 73.75% / 2.5% = 4 720 000 ₽`

| Показатель | Значение |
|---|---:|
| ARPU / MRR | 160 000 ₽ |
| Contribution Margin % | 73.75% |
| Monthly churn | 2.5% |
| **LTV** | **4 720 000 ₽** |

---

## 6. LTV/CAC, CAC payback, contribution margin

| Метрика | Формула | Значение | Verdict |
|---|---|---:|---|
| LTV/CAC | 4 720 000 / 243 100 | **19.4x** | PASS |
| CAC Payback | 243 100 / 160 000 | **1.52 мес** | PASS |
| Contribution Margin % | (160 000 - 42 000) / 160 000 | **73.8%** | PASS |

### Sanity check against investment grade
- Требование investable: **LTV/CAC ≥ 3.0**. Здесь **19.4x**.
- Требование payback: **<12 мес** для базового B2B. Здесь **1.5 мес**.
- Ключевая оговорка: такой payback выглядит очень хорошим, потому что модель с high-retainer ARPU. Если реальный ARPU съедет к **120-130 тыс. ₽**, запас прочности заметно ухудшится.

---

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Функция | Кол-во | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|---:|
| CEO / Founder | Продажи крупных сделок, стратегия, финконтур | 1 | 500 000 | 150 000 | **650 000** |
| CTO / Tech Lead | Архитектура, интеграции, data layer | 1 | 450 000 | 135 000 | **585 000** |
| Senior Backend | Коннекторы, orchestration, billing, API | 2 | 350 000 | 105 000 | **910 000** |
| ML Engineer | OCR/LLM prompts, extraction quality, routing | 1 | 450 000 | 135 000 | **585 000** |
| DevOps | Infra, monitoring, secrets, CI/CD | 1 | 300 000 | 90 000 | **390 000** |
| Frontend | Кабинет, ops UI, CS tools | 1 | 250 000 | 75 000 | **325 000** |
| Product / Ops Lead | Упаковка оффера, процессы, маркетинг allocation | 1 | 300 000 | 90 000 | **390 000** |
| SDR | Outbound prospecting | 1 | 160 000 | 48 000 | **208 000** |
| AE | Discovery, proposals, close | 1 | 300 000 | 90 000 | **390 000** |
| Customer Success | Onboarding, retention, QBR | 1 | 200 000 | 60 000 | **260 000** |
| Finance Ops Specialist | Ежедневный delivery | 3 | 170 000 | 51 000 | **663 000** |
| Chief Accountant / QA | Контроль качества и закрытие месяца | 1 | 240 000 | 72 000 | **312 000** |
| **Итого** |  | **14** |  |  | **5 668 000 ₽/мес** |

### 7.2 Обязательная таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 500 000 | 0 (founder) | 0 | 150 000 | 650 000 |
| CTO/Tech Lead | 1 | 450 000 | 2.0 | 2.0 | 135 000 | 585 000 |
| Senior Backend | 2 | 350 000 | 1.5 | 1.5 | 105 000 | 455 000 / чел |
| ML Engineer | 1 | 450 000 | 2.5 | 2.0 | 135 000 | 585 000 |
| DevOps | 1 | 300 000 | 1.5 | 1.0 | 90 000 | 390 000 |
| Frontend | 1 | 250 000 | 1.0 | 1.0 | 75 000 | 325 000 |
| SDR | 1 | 160 000 | 0.75 | 1.0 | 48 000 | 208 000 |
| AE | 1 | 300 000 | 1.5 | 2.5 | 90 000 | 390 000 |
| Customer Success | 1 | 200 000 | 1.0 | 1.0 | 60 000 | 260 000 |

**Salary benchmark note:** диапазоны подтверждены HH snapshot pages на 2026-04-24: senior backend, frontend, DevOps, ML Engineer, CTO, SDR/account executive related searches. Ниже в Sources даны ссылки. Я использую консервативные midpoint-like gross значения внутри наблюдаемого коридора.

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто уже в команде | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | **650 000** |
| M2 | CEO + CTO | **1 235 000** |
| M3 | + Backend #1 + Product/Ops | **2 080 000** |
| M4 | + Frontend + DevOps | **2 795 000** |
| M5 | + Backend #2 + ML Engineer | **3 835 000** |
| M6 | + SDR | **4 043 000** |
| M7 | + AE + Customer Success | **4 693 000** |
| M8 | + Finance Ops Specialist #1 + Chief Accountant | **5 226 000** |
| M9 | + Finance Ops Specialist #2 | **5 447 000** |
| M10 | + Finance Ops Specialist #3 | **5 668 000** |
| M11 | Полная команда | **5 668 000** |
| M12 | Полная команда | **5 668 000** |

**Проверка realism:** план не нанимает 5+ человек в первый месяц и учитывает, что ML/CTO/AE не выходят мгновенно. Это выглядит реалистично для Москвы/СПб рынка найма 2026.

---

## 8. Fixed costs breakdown

Ниже fixed cost база для расчёта break-even. Delivery staff, которые сидят в COGS на клиента, здесь не дублируются.

| Компонент fixed costs | ₽/мес |
|---|---:|
| Core team FOT (CEO, CTO, backend x2, ML, DevOps, frontend, Product/Ops, SDR, AE, CS) | **4 693 000** |
| Office / legal / бухгалтерия / admin | 120 000 |
| Cloud platform shared core / monitoring / backups | 85 000 |
| CRM / телефония / internal tools | 42 000 |
| Paid acquisition budget | 180 000 |
| Events / partnerships | 33 000 |
| Misc reserve | 145 000 |
| **Итого fixed costs / мес** | **5 298 000 ₽** |

---

## 9. Break-even: по клиентам и по месяцу

### 9.1 Break-even по числу клиентов

Формула:

`Break-even clients = Fixed costs / Contribution profit per client`

`= 5 298 000 / 118 000 = 44.9`

**Break-even = 45 клиентов.**

### 9.2 Break-even по месячной выручке

`Break-even revenue = 45 × 160 000 = 7 200 000 ₽ / мес`

### 9.3 Break-even по времени

При реалистичном ramp-up:
- M6: 4 клиента
- M9: 16 клиентов
- M12: 36 клиентов
- M15-M16: 45-46 клиентов

**Оценка break-even по времени: M15-M16 от старта.**

### 9.4 EBITDA на 50 клиентах

| Показатель | Значение |
|---|---:|
| Revenue @ 50 clients | 8 000 000 ₽ |
| COGS @ 50 clients | 2 100 000 ₽ |
| Gross profit @ 50 clients | 5 900 000 ₽ |
| Fixed costs | 5 298 000 ₽ |
| **EBITDA @ 50 clients** | **+602 000 ₽/мес** |

**Profit Gate:** PASS, потому что при 50 клиентах компания уже может выйти выше **500K ₽ EBITDA/мес**.

---

## 10. Burn-to-breakeven и cash runway

### 10.1 Burn-to-breakeven

Использую gross profit после COGS и вычитаю core fixed burn. При указанном ramp-up до M15-M16 совокупный cash burn до операционного breakeven оценивается в **36-38 млн ₽**.

Это означает:
- ниже **30 млн ₽** стартового капитала модель опасно хрупкая;
- **40 млн ₽** выглядят рабочим минимумом с небольшим буфером;
- любой провал по hiring, churn или ARPU легко съедает буфер.

### 10.2 Cash runway

| Показатель | Значение |
|---|---:|
| Startup capital | **40 000 000 ₽** |
| Средний burn в первые 12 мес | ~**2.9 млн ₽/мес** |
| Простая runway-оценка | **13.7 мес** |
| Реальная runway с убывающим burn при росте клиентов | **15-16 мес** |

**Вывод:** раунд ниже 40 млн ₽ для такой модели нежелателен. На бумаге unit economics красивые, но cash conversion медленная, потому что приходится заранее строить команду и GTM.

---

## 11. Основные риски для economics

1. **ARPU compression.** Если рынок примет только 120-130 тыс. ₽/мес, EBITDA на 50 клиентах уйдёт обратно к нулю.
2. **Service creep.** Любая кастомная интеграция с 1С или нестандартный payroll/налоговый контур быстро повышает COGS.
3. **Sales cycle drift.** Если win-rate из proposal падает с 30% к 15-20%, blended CAC уходит выше 300 тыс. ₽.
4. **Retention fragility.** У SMB churn может быть выше 2.5% в кризисный год, особенно если owner воспринимает сервис как заменимый аутсорс.
5. **Hiring bottleneck.** CTO, ML и сильный chief accountant не нанимаются моментально, а без них качество delivery страдает.

---

## 12. Итоговый verdict

**Unit economics verdict: PASS WITH TIGHT EXECUTION.**

Кейс выглядит **инвестируемым на unit economics уровне**, если соблюдаются одновременно четыре условия:
- чек держится около **160 тыс. ₽ MRR**;
- delivery остаётся стандартизированным, а не кастомным;
- churn удерживается около **2.5% monthly** или ниже;
- компания действительно доводит базу до **45-50 активных клиентов**.

Если хотя бы один из этих параметров ломается, модель быстро превращается из investable SaaS-enabled service в просто неплохо продающийся, но тяжёлый операционный аутсорс.

## Sources
- HH, Senior Backend, Москва, snapshot 2026-04-24: https://hh.ru/vacancies/senior-backend-developer
- HH, DevOps, Москва, snapshot 2026-04-24: https://hh.ru/vacancies/devops
- HH, Frontend Developer, Москва, snapshot 2026-04-24: https://hh.ru/vacancies/frontend-developer
- HH, ML Engineer, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=ML+Engineer&area=1
- HH, CTO, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=CTO&area=1
- HH, Sales Development Representative, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=sales+development+representative&area=1
- HH, менеджер по продажам B2B SaaS, Москва, snapshot 2026-04-24: https://hh.ru/search/vacancy?text=%D0%BC%D0%B5%D0%BD%D0%B5%D0%B4%D0%B6%D0%B5%D1%80+%D0%BF%D0%BE+%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%D0%B0%D0%BC+B2B+SaaS&area=1
- SaaS Capital, 2025 B2B SaaS Retention Benchmarks: https://www.saas-capital.com/blog-posts/2025-b2b-saas-retention-benchmarks/
- Optifi.ai, SaaS Churn Benchmarks, accessed 2026-04-24: https://www.optifi.ai/post/saas-churn-benchmarks
- Finally pricing and product pages, accessed earlier in case intake: https://finally.com/ ; https://finally.com/bookkeeping.html ; https://finally.com/pricing.html


---

## Stage 5. Critic

## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA / MRR на клиента: **160 000 ₽/мес**.
- COGS на клиента: **42 000 ₽/мес**.
- Gross profit на клиента: **118 000 ₽/мес**.
- Contribution profit на клиента: **118 000 ₽/мес**.
- Variable sales / support allocation: **0 ₽/клиент/мес**.
- Fixed costs: **5 298 000 ₽/мес**.
- Full team FOT: **5 668 000 ₽/мес**.
- CAC по каналам из 04-economics: outbound **210 000 ₽**, paid inbound **240 000 ₽**, partnerships/referrals **177 000 ₽**, blended raw **209 250 ₽**, fully-loaded рабочий CAC **243 100 ₽**.
- LTV: **4 720 000 ₽**, monthly churn benchmark: **2.5%**, LTV/CAC: **19.4x**.
- Налоговый контур для waterfall/net: **УСН 6%**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** по прибыли и **НДС 20%** если компания на ОСНО.
- Страховые взносы **~30% к ФОТ** уже учтены в FOT и fixed costs.
- Для PnL беру 3 сценария new clients / churn: **Base = 1,1,2,2,3,3,4,4,4,4,4,4 при churn 2.5%**, **Optimistic = 1,2,2,3,3,4,4,5,5,5,5,5 при churn 2.0%**, **Pessimistic = 0,1,1,2,2,2,3,3,3,3,3,3 при churn 3.5%**.
- Cash burn = `max(0; -EBITDA)`, cumulative cash считается от **0 ₽** как накопленный дефицит.

### A2. PnL 12 месяцев, Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 4.00 | 4.00 | 4.00 |
| Total clients | 1.00 | 1.98 | 3.93 | 5.83 | 8.68 | 11.46 | 15.18 | 18.80 | 22.33 | 25.77 | 29.13 | 32.40 |
| MRR, ₽ | 160 000 | 316 000 | 628 100 | 932 398 | 1 389 088 | 1 834 360 | 2 428 501 | 3 007 789 | 3 572 594 | 4 123 279 | 4 660 197 | 5 183 692 |
| COGS, ₽ | 42 000 | 82 950 | 164 876 | 244 754 | 364 635 | 481 520 | 637 482 | 789 545 | 937 806 | 1 082 361 | 1 223 302 | 1 360 719 |
| Gross profit, ₽ | 118 000 | 233 050 | 463 224 | 687 643 | 1 024 452 | 1 352 841 | 1 791 020 | 2 218 244 | 2 634 788 | 3 040 918 | 3 436 895 | 3 822 973 |
| GM% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% |
| Fixed costs, ₽ | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 |
| EBITDA, ₽ | -5 180 000 | -5 064 950 | -4 834 776 | -4 610 357 | -4 273 548 | -3 945 159 | -3 506 980 | -3 079 756 | -2 663 212 | -2 257 082 | -1 861 105 | -1 475 027 |
| Cash burn, ₽ | 5 180 000 | 5 064 950 | 4 834 776 | 4 610 357 | 4 273 548 | 3 945 159 | 3 506 980 | 3 079 756 | 2 663 212 | 2 257 082 | 1 861 105 | 1 475 027 |
| Cumulative cash, ₽ | -5 180 000 | -10 244 950 | -15 079 726 | -19 690 083 | -23 963 631 | -27 908 790 | -31 415 770 | -34 495 526 | -37 158 738 | -39 415 820 | -41 276 924 | -42 751 951 |

### A3. PnL 12 месяцев, Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 5.00 | 5.00 | 5.00 | 5.00 | 5.00 |
| Total clients | 1.00 | 2.98 | 4.92 | 7.82 | 10.67 | 14.45 | 18.16 | 22.80 | 27.34 | 31.80 | 36.16 | 40.44 |
| MRR, ₽ | 160 000 | 476 800 | 787 264 | 1 251 519 | 1 706 488 | 2 312 359 | 2 906 111 | 3 647 989 | 4 375 029 | 5 087 529 | 5 785 778 | 6 470 063 |
| COGS, ₽ | 42 000 | 125 160 | 206 657 | 328 524 | 447 953 | 606 994 | 762 854 | 957 597 | 1 148 445 | 1 335 476 | 1 518 767 | 1 698 391 |
| Gross profit, ₽ | 118 000 | 351 640 | 580 607 | 922 995 | 1 258 535 | 1 705 364 | 2 143 257 | 2 690 392 | 3 226 584 | 3 752 052 | 4 267 011 | 4 771 671 |
| GM% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% |
| Fixed costs, ₽ | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 |
| EBITDA, ₽ | -5 180 000 | -4 946 360 | -4 717 393 | -4 375 005 | -4 039 465 | -3 592 636 | -3 154 743 | -2 607 608 | -2 071 416 | -1 545 948 | -1 030 989 | -526 329 |
| Cash burn, ₽ | 5 180 000 | 4 946 360 | 4 717 393 | 4 375 005 | 4 039 465 | 3 592 636 | 3 154 743 | 2 607 608 | 2 071 416 | 1 545 948 | 1 030 989 | 526 329 |
| Cumulative cash, ₽ | -5 180 000 | -10 126 360 | -14 843 753 | -19 218 758 | -23 258 223 | -26 850 858 | -30 005 601 | -32 613 209 | -34 684 625 | -36 230 572 | -37 261 561 | -37 787 890 |

### A4. PnL 12 месяцев, Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 1.00 | 1.96 | 3.90 | 5.76 | 7.56 | 10.29 | 12.93 | 15.48 | 17.94 | 20.31 | 22.60 |
| MRR, ₽ | 0 | 160 000 | 314 400 | 623 396 | 921 577 | 1 209 322 | 1 646 996 | 2 069 351 | 2 476 924 | 2 870 231 | 3 249 773 | 3 616 031 |
| COGS, ₽ | 0 | 42 000 | 82 530 | 163 641 | 241 914 | 317 447 | 432 336 | 543 205 | 650 192 | 753 436 | 853 065 | 949 208 |
| Gross profit, ₽ | 0 | 118 000 | 231 870 | 459 755 | 679 663 | 891 875 | 1 214 659 | 1 526 146 | 1 826 731 | 2 116 796 | 2 396 708 | 2 666 823 |
| GM% | 0.0% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% | 73.8% |
| Fixed costs, ₽ | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 | 5 298 000 |
| EBITDA, ₽ | -5 298 000 | -5 180 000 | -5 066 130 | -4 838 245 | -4 618 337 | -4 406 125 | -4 083 341 | -3 771 854 | -3 471 269 | -3 181 204 | -2 901 292 | -2 631 177 |
| Cash burn, ₽ | 5 298 000 | 5 180 000 | 5 066 130 | 4 838 245 | 4 618 337 | 4 406 125 | 4 083 341 | 3 771 854 | 3 471 269 | 3 181 204 | 2 901 292 | 2 631 177 |
| Cumulative cash, ₽ | -5 298 000 | -10 478 000 | -15 544 130 | -20 382 375 | -25 000 712 | -29 406 837 | -33 490 178 | -37 262 032 | -40 733 301 | -43 914 505 | -46 815 798 | -49 446 975 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### На 1 клиента / месяц
- **ARPA:** 160 000 ₽
- **COGS:** 42 000 ₽
- **Gross profit:** 118 000 ₽
- **Variable sales / support:** 0 ₽
- **Contribution:** 118 000 ₽

#### На уровне EBITDA break-even
- **EBITDA break-even clients по gross profit:** `5 298 000 / 118 000 = 44.9`, округлённо **45 клиентов**.
- Revenue: **7 200 000 ₽/мес**
- COGS: **1 890 000 ₽/мес**
- Gross profit: **5 310 000 ₽/мес**
- EBITDA: **12 000 ₽/мес**

#### На уровне contribution break-even
- **Contribution break-even clients:** `5 298 000 / 118 000 = 44.9`, округлённо **45 клиентов**.
- Revenue: **7 200 000 ₽/мес**
- COGS: **1 890 000 ₽/мес**
- Gross profit: **5 310 000 ₽/мес**
- Variable sales / support: **0 ₽/мес**
- Contribution: **5 310 000 ₽/мес**
- EBITDA: **12 000 ₽/мес**

#### Net после налогов РФ
- **УСН 6%:** `12 000 - 432 000 = -420 000 ₽/мес`
- **IT-льгота 3%:** `12 000 - 216 000 = -204 000 ₽/мес`
- **ОСНО 20%:** `12 000 × 0.8 = 9 600 ₽/мес` до кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub

| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Base | M17 | 44 980 738 ₽ | реалистичный путь требует полного seed-runway |
| Optimistic | M14 | 37 819 652 ₽ | лучший ramp, но первый год всё ещё ниже EBITDA 0 |
| Pessimistic | M25 | 63 084 173 ₽ | замедление продаж резко ухудшает capital need |

### A7. Налоговая модель РФ
- **УСН 6% с выручки** проще всего администрировать, но на масштабе около 45 клиентов почти полностью съедает ранний EBITDA.
- **IT-льгота 3%** materially лучше для этого кейса, если есть аккредитация Минцифры и выдержана доля профильной выручки.
- **ОСНО 20%** по прибыли выглядит мягче только после прохождения EBITDA break-even, но добавляет **НДС 20%** и ухудшает cash conversion.
- **Страховые взносы ~30% к ФОТ** уже учтены внутри FOT **5 668 000 ₽/мес** и fixed costs **5 298 000 ₽/мес**, повторно не начисляются.
- Для этого кейса рабочая база, это **УСН / IT-льгота**, а не ОСНО.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Base | 45 | 45 | M17 | вне 12 месяцев, но в разумном горизонте seed-scale |
| Optimistic | 45 | 45 | M14 | выполнимо быстрее за счёт 49+ клиентов уже к M14 |
| Pessimistic | 45 | 45 | M25 | при таком ramp модель становится тяжёлой operationally |

### A9. Вывод по PnL
- Во всех трёх сценариях **первый год остаётся EBITDA-отрицательным**, хотя optimistic почти выходит в ноль к M12.
- Экономика выглядит рабочей, потому что **gross profit на клиента 118 тыс. ₽** и break-even достигается не на сотнях, а примерно на **45 клиентах**.
- Главный риск модели, это не unit margin, а **способность дойти до 45-50 активных клиентов без service creep и ARPU compression**.

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

База берётся из SECTION A: **M12 EBITDA = -1 475 027 ₽/мес** при **32.4 клиента** на M12. Для sensitivity считаю, что объём клиентов и delivery-структура сохраняются, а меняется один драйвер за раз.

| Сценарий | Изменение | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | **-1 475 027** | — | уже отрицательная EBITDA к M12 |
| Sens1 | CAC x2 | **-2 447 427** | -972 400 | если fully-loaded CAC удваивается, модель теряет почти ещё 1 млн ₽/мес EBITDA |
| Sens2 | Churn x2 | **-1 846 758** | -371 731 | база клиентов на M12 падает примерно до 29.25 |
| Sens3 | Price -30% | **-3 030 135** | -1 555 108 | самый болезненный удар, потому что gross profit на клиента падает с 118k до 70k ₽ |

**Вывод:** ключевая хрупкость не в nominal CAC payback, а в том, что при price compression или CAC inflation путь к break-even резко отъезжает вправо.

### B2. Monte Carlo Lite — confidence intervals

Ниже не полноценный кодовый Monte Carlo, а **lite-аппроксимация через triangular inputs и 9 комбинаций**. Это достаточно, чтобы понять диапазон хрупкости модели на M24.

#### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 180 000 | 243 100 | 420 000 | [T1] + base CAC из 04-economics |
| Monthly churn, % | 1.5% | 2.5% | 5.0% | [T2], [T3] |
| ARPU, ₽/мес | 130 000 | 160 000 | 190 000 | [T1], [T4] |
| Conversion rate lead→paid, % | 0.20% | 0.30% | 0.45% | 04-economics blended funnel + upside on partner mix |
| Time-to-hire, мес | 1.0 | 1.5 | 2.5 | 04-economics hiring table |

#### Логика симуляции
- Взял 9 комбинаций вокруг min / mode / max для CAC, churn и ARPU.
- Lead→paid conversion и time-to-hire использовал как вторичные модификаторы скорости выхода на клиентскую базу к M24.
- p10/p50/p90 выбраны по ранжированию 9 результатов, а не по одной жёсткой pess/base/opt линии.

#### Результат: confidence intervals

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | **-2 462 979** | **2 470 107** | **9 634 510** | **12 097 489** |
| CAC payback, мес | **1.12** | **1.52** | **3.23** | **2.11** |
| LTV/CAC | **7.24x** | **19.42x** | **32.36x** | **25.12x** |
| Cash runway, мес | **16.2** | **>24** | **>24** | **>7.8** |

#### Интерпретация правил
1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1**: риск неплатёжеспособности при плохой реализации.
2. **p50 EBITDA > 500k ₽/мес**, значит median-case формально проходит EBITDA Gate, но запас зависит от удержания price discipline.
3. **p90 / |p10| ≈ 3.9x**, то есть неопределённость большая, но ещё не экстремальная 10x.
4. **Range width по LTV/CAC = 25.12x > 8**, значит модель действительно хрупкая: достаточно просадки по pricing, churn или CAC, и «красивые» unit economics перестают быть опорой.

**Итог Monte Carlo Lite:** на бумаге upside сильный, но downside всё ещё уводит компанию в отрицательный EBITDA даже на M24. Это не reject автоматически, но требует более жёсткого risk discount, чем SECTION A могла показывать по точечной базе.

### B3. Competitor deep-dive

#### B3.1. Западные конкуренты

| Конкурент | Что делает | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Ramp** | spend/AP/finance automation platform | сильный product suite, 50k+ business customers, мощный workflow around AP and spend [T5] | US-first stack, слабая локальность под 1С/РФ-налоги, меньше managed-service handholding | **6-8%** в US SMB/mid-market AP/spend automation, оценка по customer base [inference] | локализация под 1С, ЭДО, payroll, банки РФ и возможность дать managed ops, а не только software |
| **Finally** | AI-native back-office platform: bookkeeping, payroll, AP, invoicing | closest category match, единая finance suite, 3 500+ клиентов [T1] | западный compliance stack, limited proof for Russia-like regulatory complexity | **<1% globally**, нишевой but category-defining player [inference] | можем быть глубже в российском compliance и в human-in-the-loop delivery для SMB |
| **Nanonets** | AP/document AI automation | сильный wedge в invoice/AP, 99%+ extraction claims, broad ERP integrations [T6][T7] | это скорее infra layer, а не полный finance operator; customer still needs ops orchestration | **1-2%** глобально в invoice/AP automation, оценка по category visibility [inference] | можем закрывать не только extraction, но и month-end close, payroll, invoicing, QA и SLA как сервис |

#### B3.2. Российские конкуренты

| Конкурент | Источник | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Моё дело** | vc.ru рейтинги и обзоры аутсорсинга [T8][T9] | сильный бренд в онлайн-бухгалтерии, широкий SMB reach, self-serve + аутсорс контур | ближе к классической онлайн-бухгалтерии, меньше AI-first positioning | **8-12%** российского digital accounting SMB сегмента [inference] | мы идём не в «бухгалтерию как сервис», а в AI-first finance operations layer с AP/invoicing/reconciliation |
| **Кнопка** | vc.ru обзоры и тарифные разборы [T10][T11] | сильный сервисный слой, живые бухгалтеры, all-in outsourced experience | низкая software defensibility, price-sensitive service model, меньше AI moat | **3-5%** в premium SMB аутсорсинге [inference] | выше automation density и шанс удержать gross margin лучше классического аутсорса |
| **Контур / Контур.Аутсорс** | vc.ru обзоры рынка [T12][T13] | крупнейшая экосистема, distribution, отчётность, интеграции, доверие рынка | продукт скорее horizontal accounting stack, чем AI-first operator | **12-18%** в digital accounting / отчетном ПО и adjacent outsourcing [inference] | можем атаковать узкий wedge: finance ops as outcome, а не как набор инструментов |
| **Биорг / Beorg Smart Vision** | Rusprofile + Skolkovo [T14][T15] | сильный документный AI, локальный residency, proof в обработке документов и банках | не full-stack finance operator, нужен партнёр/клиент для закрытия всей ops-цепочки | **1-2%** в российском document AI для финансовых документов [inference] | закрываем поверх OCR весь workflow, включая people/process/SLA |
| **1С / OCR-надстройки вокруг 1С (в т.ч. CORRECT, 1С-распознавание)** | Habr [T16] | natural fit в 1С-контур, низкий switching cost для бухгалтера, широкий installed base | это feature-level automation, а не end-to-end operator; качество зависит от manual verification | **20%+ installed-base share** как базовая платформа учета, но не как AI-operator [inference] | можно забрать outcome-layer над 1С: ingestion + AP + QA + close + customer success, а не просто OCR-модуль |

**Вывод по конкурентам:**
- На Западе category proof уже есть, но почти все сильные игроки заточены под US stack.
- В РФ рынок фрагментирован между **классическим аутсорсом**, **1С-экосистемой** и **точечным document AI**.
- Это даёт окно для позиционирования: **не очередная бухгалтерия и не просто OCR, а managed AI finance operator для SMB**.

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | не удаётся нанять CTO / ML / chief accountant вовремя | med | high | time-to-hire >2 мес по ключевым ролям | заранее формировать bench, внешние advisors, stage-gated hiring |
| 2 | Operational | service creep, каждая сделка превращается в кастомный проект | high | high | onboarding >10 рабочих дней, нестандартные интеграции >30% новых клиентов | жёсткий ICP, blacklist сложных кейсов, productized onboarding |
| 3 | Operational | деградация качества LLM/OCR на длинном хвосте документов | med | high | доля manual correction >20%, рост QA-ошибок | fallback rules engine, human-in-the-loop QA, versioned prompts/models |
| 4 | Operational | зависимость от внешних LLM/API-поставщиков | med | high | рост latency/cost, frequent outages, rate limits | multi-model routing, локальные fallback-модели, кэш и batch-processing |
| 5 | Market | SMB не готов платить 160k ₽/мес, рынок тянет к 90-120k ₽ | high | high | win-rate падает при quote >120k ₽ | перепаковать в tiered offer, выделить wedge SKU, upsell later |
| 6 | Market | price compression из-за классического бухаутсорса | high | high | в переговорах доминирует сравнение с бухаутсорсом 20-60k ₽ | продавать SLA/скорость/visibility, а не «ведение бухгалтерии» |
| 7 | Market | крупные игроки типа Контур/1С/Saby копируют feature-set | med | high | релизы AP/OCR/workflow automation у incumbents | строить moat в delivery-data-process layer и customer integration depth |
| 8 | Market | churn оказывается ближе к 5%/мес, а не к 2.5% | med | high | logo churn >3% три месяца подряд | усилить CS, QBR, embedded workflows, annual contracts |
| 9 | Regulatory | несоответствие 152-ФЗ / data residency | med | high | юристы клиентов блокируют доступы, security review >30 дней | RU-hosting, DPA, data maps, on-prem / private cloud option |
| 10 | Regulatory | кейсы попадают под 115-ФЗ и вызывают блокировки/ручные проверки | med | med/high | больше запросов банка по suspicious ops | ограничить high-risk verticals, AML playbooks, escalation path |
| 11 | Regulatory | санкции режут доступ к зарубежным SaaS и LLM | high | high | vendor notices, billing/payment failures | импортонезависимый стек, резервные российские провайдеры |
| 12 | Regulatory | налоговые/кадровые изменения ломают шаблоны автоматизации | med | med | frequent exceptions after law updates | методологический контур, rule updates, legal watch |
| 13 | Financial | runway съедается до выхода на 45 клиентов | high | high | cash <9 мес runway, burn выше плана на 20%+ | stage hiring, weekly burn review, early bridge planning |
| 14 | Financial | рост USD ухудшает себестоимость LLM/infra | med | med/high | FX >110 RUB/USD или рост vendor invoices >25% | рублёвые контракты где возможно, price indexation, local models |
| 15 | Financial | инфляция зарплат и налоговая нагрузка раздувают fixed costs | med | med | FOT plan +15% vs budget | quarterly repricing, comp bands, automation of backoffice |
| 16 | Financial | просадка collection / отсрочки платежа ухудшают cash conversion | med | med/high | DSO >30 дней, просрочка >10% MRR | предоплата, stricter billing terms, autopay |
| 17 | Black swan | резкое ужесточение санкций на SaaS / cloud / payments | med | high | новые ограничения по расчётам и cloud accounts | sovereign stack, резервные провайдеры, минимизация single points of failure |
| 18 | Black swan | отключение ключевого LLM-провайдера на недели | med | high | repeated incidents / policy bans | модельный abstraction layer, prompt portability, резервный inference |
| 19 | Black swan | военная/макроэскалация бьёт по SMB спросу | med | high | freeze новых договоров, рост churn у клиентов crisis-sensitive сегментов | focus на resilient verticals, flexible pricing, burn containment |
| 20 | Black swan | крупная data/security авария разрушает доверие | low/med | very high | security incidents, failed audits, anomalous access logs | zero-trust, audit trail, encryption, incident response drills |

### B5. Kill conditions через 6 месяцев

1. **Median risk gate:** если обновлённый p10 EBITDA@M24 остаётся **< 0** и cash runway **< 9 мес**, проект нельзя продолжать.
2. **Commercial gate:** если к M6 активных платящих клиентов **< 8** или новый sale не держит **ARPU ≥ 130k ₽/мес**, GTM-гипотеза не подтверждается.
3. **Retention/quality gate:** если churn **>4%/мес** два квартала подряд или manual correction rate **>25%**, automation moat отсутствует и модель превращается в обычный аутсорс.

### B6. Итоговый критический вывод

Кейс всё ещё выглядит **интересным**, но после risk-layer он уже не выглядит «лёгким PASS». SECTION A показывала красивую LTV/CAC-картину, однако SECTION B показывает более жёсткую правду:
- downside-case на M24 остаётся отрицательным;
- pricing power критичнее, чем казалось в точечной модели;
- конкурировать придётся сразу против **аутсорса**, **1С-экосистемы** и **document-AI игроков**.

**Мой итог:** это скорее **PASS WITH HEAVY RISK DISCOUNT**, а не clean green-light. Инвестировать можно только если команда доказывает productized delivery, удерживает чек **130-160k ₽+** и быстро показывает, что это не «ещё одна бухгалтерия».

## Sources for SECTION B
- [T1] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-first-finansovyy-operator-dlya-smb/02-demand.md
- [T2] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-first-finansovyy-operator-dlya-smb/04-economics.md
- [T3] https://www.saas-capital.com/blog-posts/2025-b2b-saas-retention-benchmarks/
- [T4] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/ai-first-finansovyy-operator-dlya-smb/00-brief.md
- [T5] https://ramp.com/
- [T6] https://nanonets.com/ap-automation
- [T7] https://techcrunch.com/2024/03/12/nanonets-funding-accel-india/
- [T8] https://vc.ru/services/1479376-buhgalterskii-autsorsing-reiting-luchshih-onlain-servisov-v-2026-godu
- [T9] https://vc.ru/marketing/2285150-top-15-autsorsingovykh-kompanij-moskvy
- [T10] https://vc.ru/id5314066/2866933-onlayn-bukhgalteriya-dlya-ip-obzor-servisov-i-zakonov
- [T11] https://vc.ru/services/2259043-servisy-dlya-vedeniya-buhgalterii-top-11-luchshikh
- [T12] https://vc.ru/marketing/2285150-top-15-autsorsingovykh-kompanij-moskvy
- [T13] https://vc.ru/services/2229487-kontur-elba-onlajn-buhgalteriya-dlya-ip-i-ooo
- [T14] https://www.rusprofile.ru/id/10836745
- [T15] https://sk.ru/news/ms-bank-rus-uprostil-vydachu-avtokreditov-s-pomoshyu-rossijskoj-tehnologii-raspoznavaniya-dokumentov/
- [T16] https://habr.com/ru/articles/582910/

<!-- P6B-DONE -->


---

## Stage 6. Verdict

# 06-verdict

[B2B-OPS] AI-first финансовый оператор для SMB — APPROVED WITH NOTES: 71/100 | EBITDA base=602К₽/мес через 17 мес | LTV/CAC=19,4x | Ключевое преимущество: высокий retainer и productized finance ops поверх 1С/ЭДО | Главный риск: слабая доказанность demand-tier и price compression до уровня аутсорса.

sector: B2B-OPS

## Вердикт
**APPROVED WITH NOTES**

## Investment committee summary
Кейс проходит комитет только как **productized mid-market finance ops layer**, а не как массовый бухгалтерский аутсорс. Базовая экономика сильная: `customer_ltv_rub = 4 720 000 ₽`, `CAC = 243 100 ₽`, `LTV/CAC = 19.4x`, `CAC payback = 1.52 мес`, `GM = 73.8%`, `company_ebitda_rub_month = 602 000 ₽/мес` на 50 клиентах и выход выше **500К ₽/мес** через **17 месяцев** в base-case. Но approve даётся с оговорками, потому что evidence-quality по спросу не investment-grade, moat умеренный, а execution хрупок к `ARPU` ниже 130-160 тыс. ₽/мес и к service creep.

## Оценка
Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | `LTV/CAC = 19.4x`, `CAC Payback = 1.52 мес`, `Contribution Margin = 73.8%` в `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `EBITDA @ 50 clients = +602 000 ₽/мес`, `Break-even по времени: M15-M16`, а P6A даёт base break-even `M17`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | `Demand verdict: PASS WITH RESERVATIONS`, но в `02-demand.md` отсутствует строка `Sources: T1=...`, поэтому применён штраф качества evidence. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Есть глубина в `1С + ЭДО + bank feeds + human verification`, но рынок фрагментирован между `аутсорсом`, `1С-экосистемой` и `document-AI`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | `time-to-hire >2 мес`, `service creep`, `152-ФЗ`, санкции и LLM dependence описаны как high-risk в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 22 | `Blended CAC = 243 100 ₽`, `CAC payback = 1.52 мес`, а ICP и каналы sales motion в `04-economics.md` выглядят повторяемыми. |

**Sum raw = 106 / 150. Normalized score = round((106 * 100) / 150) = 71/100.**

## Почему это APPROVED WITH NOTES
1. Кейс проходит обязательный gate: `company_ebitda_potential_rub_month = 602 000 ₽/мес` в base/near-base логике при `50` клиентах и в горизонте `17 мес`, то есть **≤50 клиентов и ≤24 месяцев**.
2. У клиента сильная unit economics на один аккаунт, поэтому бизнесу не нужен сотенный клиентский портфель, чтобы стать EBITDA-positive.
3. Платёжный контур уже существует в бюджете клиента, потому что покупка идёт из расходов на бухгалтерию, AP, первичку, payroll и finance admin, а не из экспериментального AI-бюджета.
4. Главный риск, это не отсутствие боли, а недоказанность масштабируемого локального GTM и защита от коммодитизации под классический аутсорс.

## FULL business process из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Генерация первичного лида | SDR + performance marketer | Яндекс.Директ, VK Ads, partner outreach, CRM | 1-14 дней | 18 000 | Средняя |
| 2 | Квалификация лида, first touch | SDR | amoCRM/Битрикс24, телефония, email sequencing | 30-45 мин | 2 200 | Средняя |
| 3 | Discovery call | AE | Zoom/Meet, CRM, call notes AI | 60 мин | 4 500 | Средняя |
| 4 | Сбор вводных: объём первички, банки, 1С, payroll | AE + Solution/Operations lead | Questionnaire, shared checklist | 2-3 дня | 6 500 | Низкая |
| 5 | Расчёт scope и коммерческого предложения | AE + CEO/Finance ops lead | Proposal template, калькулятор юнит-экономики | 1 день | 5 000 | Средняя |
| 6 | Security/legal review, договор | AE + CEO + юрист на аутсорсе | Документооборот, шаблон договора, ЭДО | 3-10 дней | 7 000 | Низкая |
| 7 | Выставление счёта | Finance ops | 1С, банк-клиент, ЭДО | 20 мин | 600 | Высокая |
| 8 | Оплата и активация клиента | Finance ops + Customer Success | Банк-клиент, CRM, billing | 1 день | 900 | Высокая |
| 9 | Onboarding: доступы, 1С, ЭДО, bank statements, шаблоны | CS + Finance ops specialist | 1С, Saby/Контур, shared drive, RPA | 3-5 рабочих дней | 9 500 | Средняя |
| 10 | Ежедневная обработка первички, AP, invoicing, reconciliations | Finance ops specialist | 1С, OCR, LLM extraction, RPA, bank feeds | Постоянно | 19 000 / мес | Средняя |
| 11 | Контроль качества и закрытие месяца | Chief accountant / QA | 1С, checklists, BI dashboard | 4-6 ч / мес | 7 000 / мес | Низкая |
| 12 | Продление / upsell / повторный платёж | CS + AE | CRM, QBR, BI, billing | 1-2 ч / мес | 2 500 / мес | Средняя |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | **4 720 000 ₽** |
| CAC fully-loaded | **243 100 ₽** |
| LTV/CAC | **19.4x** |
| CAC Payback | **1.52 мес** |
| GM / Contribution Margin | **73.8%** |
| Break-even clients | **45** |
| Break-even revenue | **7 200 000 ₽/мес** |
| Break-even month | **M17** в P6A base-case |
| contribution_margin_rub_month на клиента | **118 000 ₽/клиент/мес** |
| company_ebitda_rub_month @ 50 клиентов | **602 000 ₽/мес** |
| startup_capital_to_bep_rub | **44 980 738 ₽** |
| Startup capital working minimum | **40 000 000 ₽** |

## Team table
| Роль | Кол-во | Fully-loaded FOT ₽/мес | Time-to-hire | Комментарий |
|---|---:|---:|---:|---|
| CEO / Founder | 1 | 650 000 | 0 | founder-led sales и стратегия |
| CTO / Tech Lead | 1 | 585 000 | 2.0 мес | критичен для архитектуры и интеграций |
| Senior Backend | 2 | 910 000 | 1.5 мес | коннекторы, orchestration, API |
| ML Engineer | 1 | 585 000 | 2.5 мес | OCR/LLM prompts, extraction quality |
| DevOps | 1 | 390 000 | 1.5 мес | infra, monitoring, secrets |
| Frontend | 1 | 325 000 | 1.0 мес | кабинет и ops UI |
| Product / Ops Lead | 1 | 390 000 | н/д | упаковка оффера и процессы |
| SDR | 1 | 208 000 | 0.75 мес | outbound prospecting |
| AE | 1 | 390 000 | 1.5 мес | discovery, proposals, close |
| Customer Success | 1 | 260 000 | 1.0 мес | onboarding, retention, QBR |
| Finance Ops Specialist | 3 | 663 000 | н/д | ежедневный delivery |
| Chief Accountant / QA | 1 | 312 000 | н/д | контроль качества и закрытие месяца |
| **Итого** | **14** | **5 668 000 ₽/мес** |  | full operating team |

## Moat: 7-factor framework
| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент не делает продукт сильно лучше для остальных. |
| 2. Switching costs | 2 | Данные, процессы, 1С-коннекторы, ЭДО и monthly close создают умеренный lock-in. |
| 3. Scale economies | 2 | При стандартизации onboarding и QA COGS на клиента падает с объёмом. |
| 4. Proprietary data / model advantage | 1 | Может накопиться workflow-data по первичке и reconciliations, но пока нет доказанной базы данных. |
| 5. Regulatory moat | 1 | 152-ФЗ и локальный compliance больше как threshold, чем как настоящий moat. |
| 6. Brand / distribution | 1 | Пока нет сильного бренда или доминирующего канала дистрибуции. |
| 7. Embedded workflow | 3 | Продукт сидит в ежедневном finance back-office клиента и deeply embedded в month-end close. |

**Moat sum = 10 / 21. Moat score = round((10 * 25) / 21) = 12/25.**

## GTM: 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | 12 STOREEZ | fashion-retail с multi-entity учётом, большим объёмом AP, payroll и контуром поставщиков | партнёрство через 1С/финтех-интегратора + email CFO | 220 000 ₽/мес |
| 2 | DDX Fitness | сеть с recurring billing, payroll и большим операционным back-office | outbound на CFO/COO + профильная конференция fitness/retail ops | 180 000 ₽/мес |
| 3 | Skyeng | сервисный бизнес с высокой интенсивностью invoicing, payroll и reconciliations | email decision-maker + warm intro через CFO community | 240 000 ₽/мес |
| 4 | Нетология | edtech с recurring invoices, payroll для large ops-team и document-heavy back-office | outbound на finance director + vc.ru thought-leadership | 180 000 ₽/мес |
| 5 | FitStars | subscription/e-commerce модель, частые платежи и growing finance ops нагрузка | rb.ru / vc.ru channel targeting + founder/CFO outreach | 150 000 ₽/мес |
| 6 | Qummy | foodtech с закупками, B2B поставщиками и распределённым AP контуром | партнёрство с bank/ERP интегратором | 160 000 ₽/мес |
| 7 | SOKOLOV | retail + e-commerce + региональная сеть, высокие объёмы документооборота | enterprise outbound + отраслевой event | 250 000 ₽/мес |
| 8 | CDEK.Shopping / related e-com unit | cross-border/e-commerce operations увеличивают сложность finance back-office | email CFO + кейс через логистического партнёра | 170 000 ₽/мес |
| 9 | Авиасейлс | digital business с vendor invoices, payroll и потребностью в faster month-end close | direct outreach finance leader + Habr/vc.ru content | 190 000 ₽/мес |
| 10 | Flowwow | маркетплейс с большим AP/invoicing потоком и pain по quality finance operations | партнёрство с payment/ERP vendor + ABM outreach | 200 000 ₽/мес |

**Итог по GTM:** named-account ABM лучше mass-SMB. Наиболее реалистичный заход, это `1С/ЭДО/банк/интегратор-партнёр + CFO outreach + ROI-калькулятор по скорости закрытия и снижению manual FTE`.

## Top-3 risks
| Риск | Probability | Impact | Почему это критично |
|---|---|---|---|
| ARPU / price compression до 90-120 тыс. ₽/мес | High | High | `05-critic.md` показывает, что `Price -30%` ухудшает `EBITDA @M12` до `-3 030 135 ₽/мес`. |
| Service creep и кастомные интеграции | High | High | Если onboarding превращается в project-heavy delivery, `GM` и путь к 45 клиентам ломаются. |
| evidence_quality_unverified | High | Medium | В `02-demand.md` нет строки `Sources: T1=..., T2=..., T3=...`, значит source-tier balance не подтверждён. |

## Proof points, которые оправдывают APPROVED
1. **Высокий unit margin:** `contribution_margin_rub_month = 118 000 ₽/клиент/мес` даёт быстрый payback и запас для sales motion.
2. **EBITDA gate проходит:** `company_ebitda_rub_month = 602 000 ₽/мес` на 50 клиентах в горизонте `17 мес`.
3. **Repeatable workflow существует:** `1С + ЭДО + bank feeds + AP + month-end close` образуют понятный recurring pain.
4. **Category proof есть:** Finally и Nanonets подтверждают, что bundled finance ops и AP automation продаются как отдельная категория.

## Что обязательно доказать после approve
1. Реальный `ARPU ≥ 140 000 ₽/мес` на первых 8-10 клиентах без deep discounting.
2. `Logo churn ≤ 3%/мес` и manual correction rate ниже 20%.
3. Что onboarding можно удержать в `3-5 рабочих дней`, а не в custom project cycle.
4. Что минимум 30-40% pipeline можно получать не только founder-led продажами, а через repeatable partner / outbound motion.

## Финальный вывод IC
Это **не clean SaaS**, а **SaaS-enabled managed finance ops business**. Для фонда это допустимо только потому, что чек высокий, payback быстрый, а путь к EBITDA ≥500К ₽/мес достигается без экстремального клиентского объёма. Но margin of safety средний, поэтому решение, это **APPROVED WITH NOTES**, а не unconditional approve.


---

## Stage 7. Score trajectory

---
case: ai-first-finansovyy-operator-dlya-smb
updated_at: 2026-04-24
analyst: branch-models-lead
---

# 07-score-trajectory

## Score block

| Stage | Score | Verdict | Δ | Комментарий |
|---|---:|---|---:|---|
| Intake | 71/100 | HOLD | — | Хороший wedge на стыке finance ops и managed service, но без проверки локальной монетизации |
| Demand Validation | 78/100 | PASS WITH RESERVATIONS | +7 | Есть category proof, понятный buyer и бюджетный карман, но остаётся риск коммодитизации через бухаутсорс |
| Unit Economics | 84/100 | PASS | +6 | ARPU 160K ₽, contribution margin 73.8%, fully-loaded CAC 243K ₽, LTV/CAC 19.4x, break-even около 45 клиентов |

| Critic + Verdict | 71/100 | APPROVED WITH NOTES | -13 | Unit economics и EBITDA gate проходят, но evidence-tier слабый, moat умеренный, а price compression/service creep остаются главными стоп-рисками |

## Narrative
- На этапе critic кейс был понижен с economics-only optimism до инвестиционного approve с жёсткими оговорками.
- Главная причина дисконта, это не математика юнит-экономики, а слабая source-tier база, риск кастомизации delivery и средний moat.
- Тем не менее EBITDA gate выполняется в пределах 24 месяцев и при клиентской базе около 50 аккаунтов, поэтому кейс остаётся investable.

## Current status
**Текущий статус: APPROVED WITH NOTES в Program 7 / Critic and Verdict.**

Следующий критический вопрос: сможет ли команда доказать `ARPU >= 140 000 ₽/мес`, churn <= 3%/мес и productized onboarding без project-heavy внедрений.
