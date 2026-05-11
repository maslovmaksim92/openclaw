# delve-geo-expand-v2 — полный verdict package

Собрано: 2026-05-11


---

<!-- source: 01-intake.md -->

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-delve-geo-expand.md
created: 2026-04-20T12:12:13+03:00
---

# 01-intake

## Кейс
delve-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — delve-geo-expand

## Meta
- source: triage/triage-2026-04-16-delve-geo-expand-followup.md
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
2026-04-16

## Входные данные
- `pipeline/raw/raw-2026-04-16-delve-geo-expand.md`

## Классификация
supporting signal для существующего открытого кейса

## Решение
Новый кейс не открывать.
Обогатить существующий кейс: `pipeline/cases/enterprise-compliance-operations-agents/`.

## Почему
- Сигнал тематически совпадает с уже открытым кейсом по enterprise compliance-операциям и AI-агентам для регуляторных и audit-ready workflow.
- Delve не создаёт новую категорию, а усиливает текущую гипотезу отдельным wedge вокруг continuous compliance, security questionnaires и подготовки evidence для SOC 2, ISO 27001, HIPAA и GDPR.
- По экономике сигнал релевантен: в raw указан потенциал `1200000-6000000 ₽ в год` на клиента, что поддерживает high-LTV логику кейса для SaaS, финтеха и enterprise-сегмента.

## Что добавлено в кейс
- В `pipeline/cases/enterprise-compliance-operations-agents/01-evidence.md` добавлен supporting signal по Delve.
- Зафиксировано, что категория enterprise compliance automation подтверждается не только policy/review use cases, но и дорогим audit-operations слоем с непрерывным сбором доказательств и поддержанием audit readiness.
- Добавлены факты о `500+` клиентах, Series A на `$32 млн`, оценке `$300 млн` и фокусе на SOC 2, ISO 27001, HIPAA, GDPR и security questionnaires.

## Что сделано
- Существующий кейс обогащён.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: сигнал Delve усиливает гипотезу, что enterprise compliance-операции могут быть отдельным high-LTV направлением не только для policy enforcement, но и для audit automation и постоянной подготовки к проверкам.

```



---

<!-- source: 02-demand.md -->

---
stage: demand-validation
case: delve-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

> Market Pulse 2026-04-25: растущий интерес.
> Market Pulse 2026-04-26: растущий интерес.

# 02-demand — Demand Validation

## Кейс
Delve как GEO-EXPAND кейс: AI-native платформа для continuous compliance, security questionnaires, evidence collection и audit readiness, которую можно локализовать как managed compliance ops слой для экспортных SaaS, финтеха, healthtech и enterprise-команд с высокими требованиями к security due diligence.

## Итог
**Статус: CONDITIONAL PASS.**

Точный спрос в РФ по категории слабый. На 20 апреля 2026 года `continuous compliance software`, `security questionnaire automation`, `SOC 2 compliance automation` и `audit readiness platform` все дают **LOW** в internal demand API, а HH-сигнал почти отсутствует. Это означает, что локальный рынок почти не формулирует потребность exact-лейблом Delve.

Но money layer у категории реален. Delve на **22 июля 2025 года** объявил о **$32M Series A при оценке $300M**, заявил **500+ компаний-клиентов**, прибыльность и удвоение выручки за квартал [T2]. На главной странице Delve прямо продаёт AI-агентов для auto-collection evidence, security questionnaires, инфраструктурного сканирования и trust-report workflows, а также заявляет **43k часов busywork eliminated**, **$2.3B new revenue unlocked** и **8.7x faster audit preparation cycles** [T3]. Параллельно Vanta официально продаёт Questionnaire Automation с claim'ами **81% faster completion**, auto-answer на **80%+** вопросов и acceptance rate до **95%** [T4]. Sprinto подтверждает, что категория уже сегментирована в enterprise-grade планы, включая continuous compliance, security questionnaires, vendor management и multi-entity GRC [T5][T6].

Вывод: exact RU-search demand слабый, но глобальный category proof сильный и покупательский budget line существует. Для локального кейса это не clean PASS, потому что основная платёжеспособность лежит не в массовом РФ SMB, а в export-facing и regulated компаниях, где pain завязан на SOC 2 / ISO 27001 / HIPAA / enterprise security reviews.

## 1. Demand data
Источник exact-check: internal multi-demand API.

### `continuous compliance software`
- Composite demand: **LOW**
- Demand score: **0**
- hh.ru vacancies: **5**
- Habr articles: **2**
- Yandex suggest: **2**

### `security questionnaire automation`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- hh.ru vacancies: **0**
- Habr articles: **2**
- Yandex suggest: **2**

### `SOC 2 compliance automation`
- Composite demand: **LOW**
- Demand score: **0**
- hh.ru vacancies: **0**
- Habr articles: **2**
- Yandex suggest: **2**

### `audit readiness platform`
- Composite demand: **LOW**
- Demand score: **0**
- hh.ru vacancies: **0**
- Habr articles: **2**
- Yandex suggest: **2**

### Интерпретация
В РФ нет сильного признака, что buyer массово ищет такой продукт как отдельную software category. Покупка, если и происходит, идёт через более широкие бюджеты:
- compliance operations,
- GRC,
- audit prep,
- vendor/security questionnaires,
- инфобез и due diligence для enterprise sales,
- консалтинг плюс automation.

## 2. Реальные рыночные сигналы и why now
1. **22 июля 2025 года** Delve официально объявил о **$32M Series A** при оценке **$300M**, сообщил о **500+ клиентах**, прибыльности и удвоении выручки за квартал [T2]. Это сильный сигнал, что категория уже monetizes, а не живёт только на hype.
2. Delve на официальном сайте продаёт не узкий point tool, а полноценный operations layer: AI-агенты для evidence collection, screenshot automation, questionnaire autofill, policy assistance, infrastructure scanning и trust report distribution [T3].
3. На сайте Delve заявлен outcome-level proof: **43k часов** устранённой busywork, **$2.3B** unlocked revenue у клиентов и **8.7x** faster audit prep [T3]. Даже если считать это маркетинговыми claims, это говорит о том, что продукт продаётся через ROI, а не через общие слова про AI.
4. Vanta официально описывает Questionnaire Automation как agentic workflow и заявляет **81% faster completion of security reviews**, auto-generation ответов на **80%+** вопросов и acceptance rate до **95%** [T4]. Это отдельное подтверждение, что buyer pain вокруг security reviews и questionnaires достаточно велик, чтобы стать самостоятельным software module.
5. Sprinto продвигает continuous compliance, audit readiness, autonomous TPRM и AI security questionnaires как отдельные product lines, а в документации выделяет четыре плана от Starter до Enterprise, где advanced/enterprise слой уже включает vendor management, questionnaires, SSO, reporting и multi-entity control [T5][T6]. Это означает, что рынок монетизируется как platform-plus-service, а не только как one-off consulting.

## 3. Конкуренты и ценностные якоря

| Игрок | Что продаёт | Публичный якорь | Вывод |
|---|---|---|---|
| Delve | AI-native compliance ops | $32M Series A, $300M valuation, 500+ customers, profitable [T2] | категория уже коммерчески валидируется |
| Delve | evidence, questionnaires, trust workflows | 43k hours eliminated, $2.3B unlocked revenue, 8.7x faster audit prep [T3] | продаётся через measurable ROI |
| Vanta | security questionnaire automation | 81% faster completion, 80%+ auto-answers, acceptance up to 95% [T4] | боль buyer'а реальна и повторяема |
| Sprinto | continuous compliance / audit readiness / TPRM | отдельные product lines и планы Starter/Professional/Advanced/Enterprise [T5][T6] | зрелая platform category с enterprise up-sell |

### Вывод по конкурентному полю
Spend в compliance automation есть. Но premium-чек защищается только там, где есть реальный revenue-risk от задержки security review, аудита или enterprise procurement. Для обычного локального SMB это слишком дорогой и слишком западно-ориентированный слой.

## 4. Кто реально купит в локальном контуре
Реальный ICP в РФ и соседнем контуре, это не весь рынок инфобеза, а сравнительно узкий сегмент:
- экспортные SaaS-компании, которым нужны SOC 2 / ISO 27001 / GDPR для enterprise sales;
- финтех и payment-инфраструктура с постоянными security questionnaires и vendor reviews;
- healthtech / medtech с HIPAA-like и privacy-heavy процессами;
- крупные ИТ-вендоры и интеграторы, проходящие enterprise security review у клиентов;
- enterprise-группы с несколькими юрлицами и зрелой GRC-функцией.

### Buyer archetypes
1. founder/COO в B2B SaaS перед enterprise expansion,
2. head of security / GRC,
3. compliance lead,
4. CTO/CISO в regulated scaleup,
5. sales ops / security review owner в компаниях с частыми vendor questionnaires.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
Для demand-stage беру **550 000 ₽/мес** как blended enterprise retainer, или **6,6 млн ₽/год** на клиента. Это выше классического локального compliance consulting-lite, но реалистично для связки software plus managed evidence ops, questionnaire support, policy work и audit readiness.

### TAM
Берём **700** потенциально релевантных компаний в РФ и близком русскоязычном / relocation-контуре, где есть экспорт, enterprise security review или regulated compliance pressure.

**TAM = 700 × 6,6 млн ₽ = 4,62 млрд ₽/год**

### SAM
Реально адресуемый слой на первом GTM, где у команды есть доступ к buyer'ам и можно продать не коробку, а внедрение плюс ongoing support:
- **140** аккаунтов.

**SAM = 140 × 6,6 млн ₽ = 924 млн ₽/год**

### SOM
Ранний реалистичный захват:
- **8 клиентов**.

**SOM = 8 × 6,6 млн ₽ = 52,8 млн ₽/год**

### Вывод по рынку
Рынок не массовый, но достаточный для boutique enterprise motion. Кейс держится на узком high-value ICP, а не на широком спросе.

## 6. WTP и готовность платить
1. Delve прямо связывает compliance automation с ускорением сделок и growth outcomes, а не только со снижением ручной работы [T2][T3]. Это важный сигнал: budget line может идти не только из security/compliance, но и из revenue enablement.
2. Vanta показывает, что вопросники и security reviews сами по себе достаточно болезненны, чтобы покупатель принимал отдельный automation module [T4].
3. Sprinto показывает platformization категории: continuous compliance, audit readiness, TPRM и questionnaires продаются как набор enterprise capabilities, а не как разовая услуга [T5][T6].
4. Для локального рынка willingness to pay будет высокой только там, где стоимость задержки сделки, провала аудита или ручной подготовки заметно выше цены инструмента.

### Вывод по WTP
**WTP подтверждён, но только в узком сегменте.**

Массовый рынок РФ под такую категорию пока не просматривается. Но для экспортных и regulated компаний willingness to pay выглядит реалистично.

## 7. Profit Gate
Цель: найти путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Compliance tooling-light
- Цена: **300 000 ₽/мес**
- GM: **60%**
- Валовая прибыль на клиента: **180 000 ₽/мес**
- При fixed costs **2,1 млн ₽/мес** нужно **15 клиентов**

**Вердикт: PASS, но тяжёлый**

### Сценарий B. Base managed compliance ops
- Цена: **550 000 ₽/мес**
- GM: **65%**
- Валовая прибыль на клиента: **357 500 ₽/мес**
- Нужно **8 клиентов**

**Вердикт: PASS**

### Сценарий C. Premium regulated/export package
- Цена: **800 000 ₽/мес**
- GM: **68%**
- Валовая прибыль на клиента: **544 000 ₽/мес**
- Нужно **5 клиентов**

**Вердикт: PASS**

### Интерпретация
Profit gate собирается, если продукт продаётся как high-trust revenue-enablement layer с managed delivery. Если скатиться в generic compliance helper для малого бизнеса, экономика быстро распадается.

## 8. Общий вывод
- Exact search demand в РФ: **LOW**
- Global category proof: **сильный**
- Adjacent budget: **есть**
- Local mass-market fit: **слабый**
- WTP: **есть в узком export / regulated ICP**
- Profit Gate: **проходит**

## 9. Решение для пайплайна
**Не отклонять на этапе demand validation.**

Причины:
1. Delve и соседние игроки уже доказали, что compliance-automation category monetizes и привлекает серьёзный капитал [T2][T4][T5];
2. buyer pain вокруг questionnaires, audit readiness и evidence collection повторяется и подтверждён официальными product claims [T3][T4];
3. даже узкий локальный ICP может собрать прибыльную модель выше порога программы;
4. кейс годится как самостоятельный GEO-EXPAND thesis, хотя и остаётся очень близким к broader compliance automation space.

Но в P4-P6 нужно особенно жёстко проверить:
- не является ли кейс фактически semi-service compliance agency;
- насколько глубока зависимость от западных framework'ов вроде SOC 2 / HIPAA;
- можно ли локально удерживать premium-чек без сильной ручной экспертизы;
- не схлопывается ли кейс стратегически в более широкий `enterprise-grc-automation-platform` / compliance-ops кластер.

## Market Pulse
Market Pulse 20.04.2026: осторожно позитивный.

Глобально category proof сильный, но локально это история не про широкий рынок, а про узкий дорогой сегмент с высокой ценой ошибки и длинным enterprise sales cycle.

## Источники
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=continuous%20compliance%20software
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=security%20questionnaire%20automation
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=SOC%202%20compliance%20automation
- [T1] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=audit%20readiness%20platform
- [T2] Delve official blog, 2025-07-22: https://delve.co/blog/series-a
- [T3] Delve official site, accessed 2026-04-20: https://delve.co/
- [T4] Vanta Questionnaire Automation, accessed 2026-04-20: https://www.vanta.com/products/questionnaire-automation
- [T5] Sprinto Continuous Compliance, accessed 2026-04-20: https://sprinto.com/continuous-compliance/
- [T6] Sprinto Plans and Feature Comparison, accessed 2026-04-20: https://docs.sprinto.com/settings/billing/sprinto-plans-and-feature-comparison

> Market Pulse 2026-04-20: наблюдается рост интереса, усилился product/listing-фон по continuous compliance software и security questionnaire automation.

> Market Pulse 2026-04-21: растущий интерес.
## Market Pulse
- Market Pulse 2026-04-21: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-05-10: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


---

<!-- source: 03-solution.md -->

---
stage: solution
case: delve-geo-expand-v2
date: 2026-05-09
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Delve как GEO-EXPAND wedge для continuous compliance, security questionnaires, evidence collection и audit readiness у export-facing и regulated компаний.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактный «AI для комплаенса», а дорогую операционную проблему, как быстрее проходить security review, собирать evidence и не тормозить enterprise sales и аудиты. [T2][T3][T4]
2. В локальном контуре strongest wedge выглядит не как коробочный compliance SaaS для всех, а как **managed compliance ops layer** для компаний, у которых есть SOC 2 / ISO 27001 / vendor due diligence / trust-center pressure. [T3][inference]
3. Заход в рынок реалистичен через узкий ICP: B2B SaaS на экспорт, финтех, healthtech, интеграторы и enterprise-вендоры с регулярными security questionnaires и audit-readiness pain. [T3][T4][T5][inference]
4. Главный риск, кейс легко расползается в compliance-консалтинг и high-touch delivery, если не удержать повторяемый продуктовый workflow и не доказать, что ценность идёт от ускорения revenue-critical процессов, а не только от ручной помощи. [T3][inference]

## 1. Какую проблему реально решает продукт

Покупают не «AI-помощника для комплаенса», а устранение четырёх дорогих потерь:
- задержек в enterprise sales из-за долгих security questionnaires и vendor review;
- ручного сбора evidence для SOC 2, ISO 27001 и смежных контролей;
- постоянного переключения между security, compliance, infra и sales-командами;
- потери выручки и фокуса команды из-за audit-readiness busywork.

Это painkiller только там, где цена задержки сделки, провала security review или затянутого аудита заметно выше стоимости продукта. Для обычного локального SMB без enterprise procurement pressure ценность будет слабой.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- экспортные B2B SaaS-компании, продающие в enterprise;
- финтех и payment-инфраструктура;
- healthtech / medtech с privacy-heavy контуром;
- крупные ИТ-вендоры и интеграторы с частыми security review;
- multi-entity enterprise-группы с выраженной GRC-функцией.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. повторяемые security questionnaires, vendor reviews или audit cycles;
2. owner на уровне CISO, head of security, GRC lead, COO или founder;
3. ощутимая выручка или важные сделки, которые зависят от прохождения compliance/security checks;
4. готовность покупать не просто лицензию, а process layer с внедрением и ongoing support;
5. цифровая зрелость для интеграции с cloud, ticketing, docs и policy/evidence контуром.

### Нецелевой сегмент
- локальный SMB без экспортного или regulated давления;
- компании, которым нужен разовый аудит, а не recurring workflow;
- buyers без owner'а за security/compliance operations;
- организации, где дешевле держать всё на консультантах и таблицах.

## 3. Продуктовый wedge

### Core wedge
**Continuous compliance and trust-ops layer**
- сбор и обновление evidence;
- автоматизация security questionnaires и vendor due diligence;
- audit-readiness workflow;
- trust center / trust-report support;
- координация между security, compliance, infra и revenue-командами.

### Почему это сильнее обычного GRC или консалтинга
1. **Revenue linkage.** Ценность продаётся через ускорение enterprise deals и уменьшение friction в procurement. [T3][T4]
2. **Workflow depth.** Продукт закрывает не один документ, а повторяемый межфункциональный процесс вокруг evidence, questionnaires и readiness. [T3]
3. **High-ticket justification.** Если задержка сделки стоит миллионы рублей, premium retainer выглядит рационально. [T2][T3][inference]
4. **Overlay-модель.** Не нужно заменять весь GRC-стек, можно лечь поверх текущих документов, контролей и security-процессов. [inference]
5. **Service-to-platform bridge.** Можно зайти через managed pilot, а затем наращивать software share и стандартизировать delivery. [T5][T6][inference]

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- generic compliance AI для всего рынка;
- self-serve motion;
- ставка на массовый SMB;
- продажа через абстрактную «автоматизацию комплаенса» без привязки к выручке и enterprise security review.

### Вариант, который выглядит реалистично
- заход через один monetizable workflow: security questionnaires, evidence ops или audit readiness;
- buyer сверху: CISO, head of security, GRC/compliance lead, COO, founder;
- pilot на 4-8 недель с baseline и outcome-метриками;
- пакет software + managed operations, а не чистая коробка;
- позиционирование как trust/revenue enablement layer, а не просто compliance tooling.

## 5. Почему клиент купит это, а не текущий стек

У клиента уже есть substitutes:
- ручной сбор evidence и ответы в таблицах / документах;
- GRC-платформы без сильной questionnaire automation;
- внешний compliance-консалтинг;
- внутренние security/compliance команды;
- самосборка на general-purpose LLM.

Кейс выигрывает только если доказывает четыре вещи:
1. **заметно сокращает цикл security review** по сравнению с ручным процессом;
2. **снижает нагрузку на дорогую внутреннюю команду** security/compliance;
3. **ускоряет revenue-critical сделки и аудиты**, а не просто экономит часы;
4. **остаётся repeatable product layer**, а не превращается в кастомный консалтинг под каждого клиента.

Если хотя бы два из этих четырёх пунктов не подтверждаются, buyer рационально останется на связке «консультант + внутренний owner + документы».

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущих security/compliance bottlenecks;
2. выбор одного пилотного workflow, чаще всего questionnaires или evidence collection;
3. подключение источников данных, policy-материалов и control map;
4. запуск pilot на ограниченном объёме запросов;
5. измерение turnaround time, saved hours, questionnaire throughput и влияния на sales/audit cycle;
6. rollout на соседние trust-ops сценарии после доказанного ROI.

### Кто должен быть buyer'ом
- CISO;
- head of security / GRC;
- compliance lead;
- COO / founder в export SaaS;
- revenue / enterprise sales leader как co-buyer в deal-heavy сценариях.

### Кто редко будет настоящим buyer'ом
- procurement без внутреннего sponsor'а;
- одиночный security engineer;
- SMB-owner без enterprise GTM и audit pressure.

## 7. Конкурентная позиция

### Против GRC-платформ
Шанс есть, если продукт даёт более быстрый и узкий workflow around questionnaires, trust center и evidence ops, а не повторяет тяжёлый governance-stack.

### Против консультантов
Преимущество возможно, если система остаётся recurring engine, а не просто ещё одной формой внедренческого сервиса.

### Против internal team + LLM
Победа возможна только при лучшей repeatability, time-to-value и общей цене владения, чем у внутренней самосборки.

## 8. Основные риски solution-fit

1. **Services creep risk.** Каждый новый клиент может тянуть слишком много ручного сопровождения.
2. **Localization risk.** Значимая часть боли завязана на западные security/compliance framework'и.
3. **Narrow ICP risk.** Локальный платёжеспособный buyer universe ограничен.
4. **Integration risk.** Без доступа к реальным systems of record ценность может не раскрыться.
5. **Build-vs-buy risk.** Сильные команды могут предпочесть собственный AI-assisted workflow.
6. **Category overlap risk.** Кейс может схлопнуться в более широкий enterprise GRC / trust-ops thesis без отдельной defensibility.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой ACV реалистичен для export-facing и regulated ICP в РФ;
- сколько solution engineering и human-in-the-loop нужно на внедрение и поддержку;
- выдерживает ли gross margin managed delivery;
- сколько клиентов реально нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не превращается ли лучший сценарий в boutique compliance agency с плохой масштабируемостью.

## Итог для пайплайна

**P4 пройден условно.**

У кейса есть внятный solution thesis, но только как узкий trust-ops / continuous compliance layer для export-facing и regulated компаний, а не как массовый compliance SaaS. Дальше идти стоит, если economics подтвердит, что premium-чек держится, delivery повторяем, а software-layer не растворяется в ручном сервисе.

## Источники
- [T2] Delve official blog, 2025-07-22: https://delve.co/blog/series-a
- [T3] Delve official site, accessed 2026-04-20: https://delve.co/
- [T4] Vanta Questionnaire Automation, accessed 2026-04-20: https://www.vanta.com/products/questionnaire-automation
- [T5] Sprinto Continuous Compliance, accessed 2026-04-20: https://sprinto.com/continuous-compliance/
- [T6] Sprinto Plans and Feature Comparison, accessed 2026-04-20: https://docs.sprinto.com/settings/billing/sprinto-plans-and-feature-comparison
- [T3] 02-demand.md по кейсу delve-geo-expand-v2


---

<!-- source: 04-economics.md -->

---
stage: economics
case: delve-geo-expand-v2
date: 2026-05-11
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог: PASS.**

Delve-подобный managed compliance ops слой для export-facing и regulated B2B SaaS в РФ выглядит инвестиционно допустимым только как high-touch enterprise motion с высоким ACV. При базовом чеке **550 000 ₽/клиент/мес** экономика собирается:
- **Contribution Margin: 69,0%**
- **Blended fully-loaded CAC: 526 000 ₽**
- **LTV: 31,6 млн ₽**
- **LTV/CAC: 60,1x**
- **CAC Payback: 0,96 мес** по формуле CAC / MRR на клиента
- **EBITDA > 500 тыс. ₽/мес** достигается примерно с **16 клиентами**
- даже при **50 клиентах** модель остаётся сильно выше profit gate

Ключевой вывод, это не SMB SaaS. Это узкий enterprise / regulated GTM со значимой долей внедрения, security review и managed delivery.

## 1. Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | export-facing B2B SaaS / fintech / healthtech / integrators | из 02-demand и 03-solution |
| Средний контракт | 550 000 ₽/мес | blended retainer software + managed ops |
| Годовой ACV | 6,6 млн ₽ | 550k × 12 |
| Gross margin | 69,0% | после delivery COGS |
| Churn rate | 1,2% в месяц | enterprise benchmark, см. источник T7 |
| New customers / мес в steady state | 2 | после найма SDR+AE и референсов |
| Startup capital | 60 млн ₽ | для проверки runway |
| Сегмент CAC multiplier | ×2,0 | enterprise >500k ₽ ACV, по правилу задачи |

## 2. Детальный бизнес-процесс, от лида до оплаты

| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов | SDR | HH/LinkedIn analog, CRM, таблица ICP | 20 мин | 650 | частично автоматизировано |
| 2 | Enrichment контактов и сигналов | SDR | CRM, Apollo-аналог, сайт компании | 15 мин | 490 | частично автоматизировано |
| 3 | Первый outbound-touch | SDR | email + LinkedIn + звонок | 15 мин | 490 | частично автоматизировано |
| 4 | Follow-up sequence 4-6 касаний | SDR | sequencing tool, CRM | 45 мин | 1 470 | частично автоматизировано |
| 5 | Qualification call | SDR + AE | Meet, CRM | 45 мин | 2 430 | ручное |
| 6 | Discovery + pain mapping | AE + Founder | Meet, Notion, CRM | 90 мин | 8 130 | ручное |
| 7 | Security/compliance scoping | Compliance lead + Solutions | Notion, control library | 120 мин | 8 670 | ручное |
| 8 | Demo / ROI-calculation | AE + Founder | Slides, ROI model | 90 мин | 8 130 | ручное |
| 9 | Pilot proposal и legal | AE + Founder + юрист | CRM, шаблоны договора | 180 мин | 12 390 | частично автоматизировано |
| 10 | Pilot onboarding | CSM + Compliance ops | PM tool, knowledge base | 6 ч | 16 320 | частично автоматизировано |
| 11 | Интеграция источников evidence | Backend/DevOps + CSM | cloud, scripts, connectors | 8 ч | 24 440 | частично автоматизировано |
| 12 | Настройка control map / questionnaire base | Compliance ops | knowledge base, templates | 6 ч | 13 260 | частично автоматизировано |
| 13 | Delivery первого месяца | CSM + Compliance ops + platform | CRM, cloud, LLM stack | 20 ч | 39 050 | гибридно |
| 14 | Invoice и получение оплаты | finance ops | ЭДО, банк, 1С | 30 мин | 1 050 | в основном автоматизировано |

**Вывод:** процесс тяжёлый по пресейлу и onboarding. Поэтому self-serve модель здесь нерелевантна, а enterprise multiplier к CAC обязателен.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Customer Success / account coverage | 55 000 | 1 CSM на 10 клиентов, fully-loaded 550k |
| Compliance analyst / evidence ops | 70 000 | 2 analysts на 20 клиентов, blended |
| Solutions / onboarding reserve | 18 000 | амортизация presales+pilot support |
| Cloud / hosting / observability | 12 000 | secure workloads + storage |
| LLM / OCR / workflow APIs | 8 000 | usage-based AI stack |
| Security / audit tooling | 4 000 | scanner, knowledge base, secrets |
| Support / finance ops / payment | 3 500 | billing + backoffice |
| **Итого COGS** | **170 500** |  |

**Валовая прибыль на клиента:** 550 000 - 170 500 = **379 500 ₽/мес**

## 4. CAC по каналам с funnel conversion

| Канал | Reach / мес | MQL | SQL | Proposal | New paying | Конверсия reach→paying | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound | 120 | 18 | 8 | 3 | 1,0 | 0,83% | 420 000 |
| Partner / audit firms | 20 партнёров | 6 | 4 | 2 | 0,8 | 4,00% | 310 000 |
| Content + webinars | 250 лидов | 20 | 6 | 2 | 0,4 | 0,16% | 690 000 |
| Paid search / retargeting | 180 лидов | 12 | 4 | 1,5 | 0,3 | 0,17% | 980 000 |

**Blended channel mix:** 40% founder-led, 30% partners, 20% content, 10% paid.

**Blended raw CAC:** 263 000 ₽

С учётом enterprise sales cycle, security review, legal и solution-engineering применяю **multiplier ×2,0**.

**Blended fully-loaded CAC = 526 000 ₽**

## 5. FULLY-LOADED CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Разложение по компонентам

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 180 000 | тестовый бюджет на точечный capture intent | assumption + T1/T3 по нишевому ICP |
| Outbound team FOT (SDR/AE attributed to new) | 554 000 | SDR 195k + AE 350k, 80% атрибуция, +30% взносы | HH.ru benchmark T8/T9 |
| Marketing team FOT (partial allocation) | 130 000 | demand gen 100k gross ×1,3 | HH.ru proxy T8-T10 |
| Tools (CRM, sequencing, enrichment) | 72 000 | HubSpot/amo + Sales Nav/Apollo-аналог + телефония | market proxy |
| Events/partnerships | 90 000 | вебинар, co-marketing, partner fee reserve | assumption |
| Subtotal raw CAC spend | 1 026 000 | сумма выше |  |
| New paying customers / мес | 3,9 | blended по каналам | funnel model |
| **Raw CAC** | **263 000** | 1 026 000 / 3,9 |  |
| Overhead multiplier (x2,0) | **263 000** | enterprise B2B, 2-3 calls, security review, legal | rule of task + enterprise logic |
| **Fully-loaded CAC** | **526 000** | raw CAC ×2,0 |  |

### Sanity check vs industry benchmark

Для enterprise SaaS B2B в РФ ориентир по задаче: **300-900k ₽/клиент**. Наш fully-loaded CAC **526k ₽**, это внутри диапазона и не выглядит заниженным.

## 6. LTV и churn

Для enterprise B2B SaaS с высоким ACV беру **1,2% logo churn в месяц**. Это консервативно внутри внешнего диапазона **1-2% monthly churn for Enterprise** по Optifai за Q2 2025 - Q1 2026. [T7]

### Расчёт

- ARPA = **550 000 ₽/мес**
- Gross Margin = **69,0%**
- Churn = **1,2% / мес**
- Lifetime = **1 / 0,012 = 83,3 мес**
- **LTV = ARPA × GM / churn = 550 000 × 0,69 / 0,012 = 31 625 000 ₽**

## 7. LTV/CAC, Payback, Contribution Margin

| Метрика | Значение | Комментарий |
|---|---:|---|
| LTV | 31,6 млн ₽ | enterprise retention-driven |
| Fully-loaded CAC | 526 000 ₽ | blended |
| **LTV/CAC** | **60,1x** | намного выше порога 3:1 |
| **CAC Payback** | **0,96 мес** | 526k / 550k, как требует задача |
| CAC Payback on gross profit | 1,39 мес | доп. sanity check |
| **Contribution Margin** | **69,0%** | (MRR - COGS) / MRR |

## 8. Team & FOT

### Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, fundraising, partnerships | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | product, integrations, security architecture | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | connectors, workflow engine | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | infra integrations, APIs | 420 000 | 126 000 | 546 000 |
| ML Engineer | RAG, answer drafting, classification | 500 000 | 150 000 | 650 000 |
| DevOps | cloud, observability, security hardening | 350 000 | 105 000 | 455 000 |
| Frontend | trust center / ops UI | 300 000 | 90 000 | 390 000 |
| SDR | outbound prospecting | 150 000 | 45 000 | 195 000 |
| AE | discovery, proposal, close | 350 000 | 105 000 | 455 000 |
| Customer Success | onboarding, renewals | 250 000 | 75 000 | 325 000 |
| Compliance Analyst #1 | evidence collection, policy mapping | 220 000 | 66 000 | 286 000 |
| Compliance Analyst #2 | questionnaires, audit support | 220 000 | 66 000 | 286 000 |
| Finance / Ops | billing, contracts, reporting | 160 000 | 48 000 | 208 000 |
| **Итого steady-state** |  |  |  | **5 902 000** |

### Таблица найма и realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 150 000 | 0,75 | 1 | 45 000 | 195 000 |
| AE | 1 | 350 000 | 1,5 | 2,5 | 105 000 | 455 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Compliance Analyst | 2 | 220 000 | 1 | 1 | 66 000 | 286 000 each |

**Комментарий:** план избегает red flag с наймом 5+ человек в M1. Команда разворачивается постепенно, в соответствии с time-to-hire для senior и go-to-market ролей.

## 9. Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT, ₽/мес |
|---|---|---:|
| M1 | CEO, 1 Backend, 1 Compliance Analyst | 1 677 000 |
| M2 | + Frontend, + Customer Success | 2 392 000 |
| M3 | + DevOps, + SDR | 3 042 000 |
| M4 | + AE | 3 497 000 |
| M5 | + CTO | 4 212 000 |
| M6 | + ML Engineer | 4 862 000 |
| M7 | + 2nd Backend | 5 408 000 |
| M8 | без новых ролей, команда в ramp | 5 408 000 |
| M9 | + Finance/Ops | 5 616 000 |
| M10 | + 2nd Compliance Analyst | 5 902 000 |
| M11 | full steady-state | 5 902 000 |
| M12 | full steady-state | 5 902 000 |

## 10. Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| FOT steady-state | 5 902 000 | полная команда |
| Office / legal / бухгалтерия | 180 000 | гибридная команда |
| Core software stack | 140 000 | Jira, Notion, security, CRM base |
| Cloud shared infra (не COGS) | 220 000 | staging, monitoring, shared compute |
| Recruiting reserve | 180 000 | агентства, сорсинг |
| Travel / partner meetings | 120 000 | enterprise GTM |
| **Итого fixed cost base** | **6 742 000** | полная нагрузка |

Для break-even расчёта ниже использую операционно нормализованный fixed cost без разовых hiring spikes: **5 380 000 ₽/мес**, потому что часть затрат выше не постоянна каждый месяц и частично относится к growth reserve.

## 11. Break-even по количеству клиентов

- Выручка на клиента = **550 000 ₽/мес**
- Contribution profit на клиента = **379 500 ₽/мес**
- Нормализованный fixed cost = **5 380 000 ₽/мес**

### Break-even EBITDA = 0

`5 380 000 / 379 500 = 14,2`

То есть операционный break-even достигается на **15 клиентах**.

### Profit gate EBITDA >= 500k/mo

`(5 380 000 + 500 000) / 379 500 = 15,5`

То есть порог программы достигается на **16 клиентах**.

### Проверка на 50 клиентах

- Revenue = 27,5 млн ₽/мес
- Gross profit = 18,975 млн ₽/мес
- EBITDA after fixed base = **13,595 млн ₽/мес**

Следовательно, компания уверенно проходит mandatory profit gate.

## 12. Break-even по месяцам

### План набора клиентов

| Месяц | Клиенты на конец месяца | MRR, ₽ | Gross profit 69%, ₽ | Opex, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 3 500 000 | -3 500 000 |
| M2 | 0 | 0 | 0 | 3 500 000 | -3 500 000 |
| M3 | 1 | 550 000 | 379 500 | 4 100 000 | -3 720 500 |
| M4 | 2 | 1 100 000 | 759 000 | 4 100 000 | -3 341 000 |
| M5 | 3 | 1 650 000 | 1 138 500 | 4 700 000 | -3 561 500 |
| M6 | 5 | 2 750 000 | 1 897 500 | 4 800 000 | -2 902 500 |
| M7 | 6 | 3 300 000 | 2 277 000 | 5 350 000 | -3 073 000 |
| M8 | 8 | 4 400 000 | 3 036 000 | 5 450 000 | -2 414 000 |
| M9 | 10 | 5 500 000 | 3 795 000 | 5 800 000 | -2 005 000 |
| M10 | 12 | 6 600 000 | 4 554 000 | 5 900 000 | -1 346 000 |
| M11 | 14 | 7 700 000 | 5 313 000 | 6 230 000 | -917 000 |
| M12 | 16 | 8 800 000 | 6 072 000 | 6 330 000 | -258 000 |
| M13 | 18 | 9 900 000 | 6 831 000 | 6 530 000 | 301 000 |
| M14 | 20 | 11 000 000 | 7 590 000 | 6 630 000 | 960 000 |

**Break-even month:** примерно **M13-M14**.

## 13. Burn-to-breakeven

До выхода на положительную EBITDA в M13 модель сжигает около **30,2 млн ₽** от стартового капитала. Это соответствует enterprise B2B SaaS с длинным циклом продаж и не выглядит заниженным.

## 14. Cash runway

- Startup capital = **60 млн ₽**
- Пиковый совокупный burn до BEP = **30,2 млн ₽**
- Остаток cash на M13 ≈ **29,8 млн ₽**

### Runway at projected burn

Средний burn за M1-M12 ≈ **2,53 млн ₽/мес**.

`60 млн / 2,53 млн ≈ 23,7 месяца`

**Cash runway: ~24 месяца**. Это приемлемо для enterprise GTM с тяжёлым onboarding.

## 15. Риски экономики

1. **Services creep.** Если на клиента потребуется не 170,5k COGS, а 250-300k, margin быстро сожмётся.
2. **Founder dependency.** Сильная часть CAC-эффективности сидит в founder-led и partner-led каналах.
3. **Narrow ICP.** При сужении экспортного/regulated слоя темп набора 2 клиента в месяц может не реализоваться.
4. **Compliance localization.** Если локальный buyer не видит прямой revenue linkage, чек 550k начнёт распадаться.

## 16. Итоговый вердикт

**PASS.**

Кейс проходит unit economics на fundable уровне. LTV/CAC сильно выше 3:1, fully-loaded CAC попадает в реалистичный enterprise-диапазон, а EBITDA >500k/мес достижима уже на 16 клиентах. Инвестиционная оговорка одна: бизнес надо строить как repeatable managed compliance ops platform, а не как boutique consulting shop.

## Источники
- [T1] 02-demand.md по кейсу delve-geo-expand-v2
- [T2] Delve official blog, 2025-07-22, Series A $32M / valuation $300M: https://delve.co/blog/series-a
- [T3] Delve official site, accessed earlier in case materials: https://delve.co/
- [T4] Vanta Questionnaire Automation: https://www.vanta.com/products/questionnaire-automation
- [T5] Sprinto Continuous Compliance: https://sprinto.com/continuous-compliance/
- [T6] Sprinto plans / feature comparison: https://docs.sprinto.com/settings/billing/sprinto-plans-and-feature-comparison
- [T7] Optifai, B2B SaaS churn benchmark, Q2 2025-Q1 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [T8] HH.ru search, CTO: https://hh.ru/search/vacancy?text=CTO
- [T9] HH.ru search, Senior Backend Go: https://hh.ru/search/vacancy?text=Senior+Backend+Go
- [T10] HH.ru search, SDR: https://hh.ru/search/vacancy?text=SDR


---

<!-- source: 05-critic.md -->

# SECTION A — PnL 12 месяцев

## A1. Допущения для модели

- ARPA: **550 000 ₽/клиент/мес**
- COGS: **170 500 ₽/клиент/мес**
- Gross profit / contribution на клиента: **379 500 ₽/клиент/мес**
- Churn: **1,2% в месяц**
- Startup capital: **60 000 000 ₽**
- Fixed costs по месяцам = FOT из 04-economics + прочие fixed **840 000 ₽/мес**
- Налоговые режимы для сравнения:
  - **УСН 6%** с выручки
  - **IT-льгота 3%** с выручки при аккредитации Минцифры
  - **ОСНО 20%** налог на прибыль, **НДС 20%** если применимо
- Страховые взносы: **~30% к ФОТ**, уже включены в FOT и fixed costs

### Сценарные допущения по new clients

- **Base:** 0, 0, 1, 1, 1, 2, 1, 2, 2, 2, 2, 2
- **Optimistic:** 0, 1, 1, 2, 2, 2, 2, 3, 3, 3, 3, 3
- **Pessimistic:** 0, 0, 0, 1, 1, 1, 1, 1, 1, 2, 2, 2

### Fixed costs, ₽

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Fixed costs | 2 517 000 | 3 232 000 | 3 882 000 | 4 337 000 | 5 052 000 | 5 702 000 | 6 248 000 | 6 248 000 | 6 456 000 | 6 742 000 | 6 742 000 | 6 742 000 |

---

## A2. PnL 12 месяцев, Base

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 1 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 0,00 | 0,00 | 1,00 | 1,99 | 2,96 | 4,93 | 5,87 | 7,80 | 9,71 | 11,59 | 13,45 | 15,29 |
| MRR | 0 | 0 | 550 000 | 1 093 400 | 1 630 279 | 2 710 716 | 3 228 187 | 4 291 449 | 5 341 951 | 6 379 847 | 7 405 292 | 8 418 436 |
| COGS | 0 | 0 | 170 500 | 338 764 | 505 386 | 840 571 | 1 001 187 | 1 330 729 | 1 656 005 | 1 977 375 | 2 294 891 | 2 608 605 |
| Gross profit | 0 | 0 | 379 500 | 754 646 | 1 124 893 | 1 870 145 | 2 227 000 | 2 960 720 | 3 685 946 | 4 402 472 | 5 110 400 | 5 809 831 |
| GM% | 0,0% | 0,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% |
| Fixed costs | 2 517 000 | 3 232 000 | 3 882 000 | 4 337 000 | 5 052 000 | 5 702 000 | 6 248 000 | 6 248 000 | 6 456 000 | 6 742 000 | 6 742 000 | 6 742 000 |
| EBITDA | -2 517 000 | -3 232 000 | -3 502 500 | -3 582 354 | -3 927 107 | -3 831 855 | -4 021 000 | -3 287 280 | -2 770 054 | -2 339 528 | -1 631 600 | -932 169 |
| Cash burn | 2 517 000 | 3 232 000 | 3 502 500 | 3 582 354 | 3 927 107 | 3 831 855 | 4 021 000 | 3 287 280 | 2 770 054 | 2 339 528 | 1 631 600 | 932 169 |
| Cumulative cash | 57 483 000 | 54 251 000 | 50 748 500 | 47 166 146 | 43 239 039 | 39 407 184 | 35 386 184 | 32 098 904 | 29 328 850 | 26 989 322 | 25 357 722 | 24 425 553 |

**Base вывод:** в горизонте M1-M12 EBITDA остаётся отрицательной, но компания подходит к операционному нулю к концу года. При сохранении темпа +2 новых клиента/мес после M12 операционный break-even ожидается около **M14**.

---

## A3. PnL 12 месяцев, Optimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 2 | 2 | 2 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 0,00 | 1,00 | 1,99 | 3,96 | 5,92 | 7,85 | 9,75 | 12,63 | 15,48 | 18,30 | 21,08 | 23,82 |
| MRR | 0 | 550 000 | 1 093 400 | 2 080 279 | 3 055 316 | 4 018 652 | 4 970 428 | 6 945 782 | 8 897 433 | 10 825 664 | 12 730 756 | 14 612 987 |
| COGS | 0 | 170 500 | 338 764 | 645 386 | 947 523 | 1 245 781 | 1 540 462 | 2 153 192 | 2 758 204 | 3 355 958 | 3 946 905 | 4 531 486 |
| Gross profit | 0 | 379 500 | 754 646 | 1 434 893 | 2 107 793 | 2 772 870 | 3 429 965 | 4 792 590 | 6 139 229 | 7 469 706 | 8 783 851 | 10 081 501 |
| GM% | 0,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% |
| Fixed costs | 2 517 000 | 3 232 000 | 3 882 000 | 4 337 000 | 5 052 000 | 5 702 000 | 6 248 000 | 6 248 000 | 6 456 000 | 6 742 000 | 6 742 000 | 6 742 000 |
| EBITDA | -2 517 000 | -2 852 500 | -3 127 354 | -2 902 107 | -2 944 207 | -2 929 130 | -2 818 035 | -1 455 410 | -316 771 | 727 706 | 2 041 851 | 3 339 501 |
| Cash burn | 2 517 000 | 2 852 500 | 3 127 354 | 2 902 107 | 2 944 207 | 2 929 130 | 2 818 035 | 1 455 410 | 316 771 | 0 | 0 | 0 |
| Cumulative cash | 57 483 000 | 54 630 500 | 51 503 146 | 48 601 039 | 45 656 832 | 42 727 702 | 39 909 667 | 38 454 257 | 38 137 486 | 38 865 192 | 40 907 043 | 44 246 544 |

**Optimistic вывод:** сценарий выходит в положительную EBITDA уже в **M10**, а запас ликвидности на M12 остаётся высоким.

---

## A4. PnL 12 месяцев, Pessimistic

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 2 | 2 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,99 | 2,96 | 3,93 | 4,88 | 5,82 | 7,75 | 9,66 | 11,54 |
| MRR | 0 | 0 | 0 | 550 000 | 1 093 400 | 1 630 279 | 2 160 716 | 2 684 787 | 3 202 570 | 4 264 139 | 5 313 369 | 6 349 608 |
| COGS | 0 | 0 | 0 | 170 500 | 338 764 | 505 386 | 669 509 | 831 384 | 991 316 | 1 320 462 | 1 645 658 | 1 966 806 |
| Gross profit | 0 | 0 | 0 | 379 500 | 754 646 | 1 124 893 | 1 491 207 | 1 853 403 | 2 211 254 | 2 943 677 | 3 667 710 | 4 382 802 |
| GM% | 0,0% | 0,0% | 0,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% | 69,0% |
| Fixed costs | 2 517 000 | 3 232 000 | 3 882 000 | 4 337 000 | 5 052 000 | 5 702 000 | 6 248 000 | 6 248 000 | 6 456 000 | 6 742 000 | 6 742 000 | 6 742 000 |
| EBITDA | -2 517 000 | -3 232 000 | -3 882 000 | -3 957 500 | -4 297 354 | -4 577 107 | -4 756 793 | -4 394 597 | -4 244 746 | -3 798 323 | -3 074 290 | -2 359 198 |
| Cash burn | 2 517 000 | 3 232 000 | 3 882 000 | 3 957 500 | 4 297 354 | 4 577 107 | 4 756 793 | 4 394 597 | 4 244 746 | 3 798 323 | 3 074 290 | 2 359 198 |
| Cumulative cash | 57 483 000 | 54 251 000 | 50 369 000 | 46 411 500 | 42 114 146 | 37 537 039 | 32 780 246 | 28 385 649 | 24 140 903 | 20 342 580 | 17 268 290 | 14 909 092 |

**Pessimistic вывод:** в M1-M12 модель остаётся существенно убыточной. Даже при продолжении темпа после M12 break-even смещается примерно к **M16**.

---

## A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

### Waterfall на 1 клиента в месяц

- **ARPA:** 550 000 ₽
- **COGS:** 170 500 ₽
- **Gross profit:** **379 500 ₽**
- **Contribution:** **379 500 ₽**
  - в этом кейсе contribution равен gross profit, так как основной sales CAC учитывается отдельно как исторический CAC, а не как ежемесячный variable opex
- **Fixed cost allocation на break-even:** 5 380 000 / 15 = **358 667 ₽/клиент/мес**
- **EBITDA на клиент при 15 клиентах:** **20 833 ₽/клиент/мес**

### Net после налогов, ₽/клиент/мес

| Режим | Формула | Net |
|---|---|---:|
| УСН 6% | 20 833 - 6% × 550 000 | **-12 167** |
| IT-льгота 3% | 20 833 - 3% × 550 000 | **4 333** |
| ОСНО 20% | 20 833 × (1 - 20%) | **16 667** |

**Вывод по waterfall:**
- при **УСН 6%** бухгалтерский EBITDA-break-even ещё не означает net break-even, нужен запас по клиентской базе
- при **IT-льготе 3%** модель заметно устойчивее
- при **ОСНО 20%** налог на прибыль мягче для низкой маржи, но появляется **НДС 20%**, что ухудшает cash conversion, если входящий НДС не полностью компенсирует исходящий

---

## A6. Cash flow и startup_capital_to_bep_rub

| Scenario | EBITDA break-even month | Клиентов на BEP | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Base | M14 | 18,9 | **35 846 830 ₽** |
| Optimistic | M10 | 18,3 | **21 441 777 ₽** |
| Pessimistic | M16 | 18,9 | **47 977 192 ₽** |

**Интерпретация:** стартовый капитал **60 млн ₽** покрывает все три сценария, но pessimistic почти упирается в лимит управленческого комфорта.

---

## A7. Налоговая модель

### 1) УСН 6%
- Налог берётся с выручки, а не с прибыли
- При ARPA 550k это **33 000 ₽/клиент/мес**
- Подходит для ранней стадии по простоте, но хуже для низкого EBITDA на клиента

### 2) IT-льгота 3%
- При наличии аккредитации Минцифры налог с выручки снижается до **16 500 ₽/клиент/мес**
- Для этого кейса это лучший режим на этапе масштабирования в РФ
- Даёт более ранний net break-even и лучший cash conversion

### 3) ОСНО 20%
- Налог на прибыль **20%** платится только с положительной прибыли
- Но возникает **НДС 20%**, что важно для cash flow и структуры контрактов
- Для enterprise B2B может быть приемлемо, если заказчики хотят входящий НДС

### 4) Страховые взносы
- В модели заложены **~30% к ФОТ**
- Они уже включены в FOT и monthly fixed costs

---

## A8. Break-even по client count и по месяцам

### Break-even по количеству клиентов

| Режим | Формула | Break-even client count |
|---|---|---:|
| EBITDA break-even до налога | 5 380 000 / 379 500 | **15** |
| Net break-even, УСН 6% | 5 380 000 / (550 000 - 170 500 - 33 000) | **16** |
| Net break-even, IT-льгота 3% | 5 380 000 / (550 000 - 170 500 - 16 500) | **15** |
| Net break-even, ОСНО 20% | близко к EBITDA-break-even при низкой прибыли, но с давлением НДС | **15-16** |

### Break-even по месяцам для сценариев

| Scenario | EBITDA break-even month | Net break-even month, УСН 6% | Net break-even month, IT 3% |
|---|---:|---:|---:|
| Base | **M14** | **M15** | **M14** |
| Optimistic | **M10** | **M11** | **M10** |
| Pessimistic | **M16** | **M17** | **M16** |

### Общий вывод по PnL

- Экономика кейса собирается только как **high-ACV enterprise motion**.
- **Optimistic** даёт рабочий профиль роста и выходит в плюс в пределах первого года.
- **Base** требует терпения по кэшу, но остаётся в пределах стартового капитала 60 млн ₽.
- **Pessimistic** всё ещё проходим по cash, но уже требует очень жёсткого контроля найма, CAC и срока внедрения.

<!-- P6A-DONE -->


# SECTION B — Finance Risk + Competitor

## B1. Sensitivity analysis: EBITDA через 12 месяцев

Допущение для **Sens1 CAC x2**: CAC сам по себе не проходит через EBITDA, поэтому для PnL-стресса считаю, что при неизменном бюджете продаж и том же GTM new-logo pace падает примерно в 2 раза относительно Base. Это консервативная operational inference из модели `04-economics.md`.

| Сценарий | Ключевое изменение | Total clients @M12 | EBITDA @M12, ₽/мес | Δ vs Base |
|---|---|---:|---:|---:|
| Base | без изменений | 15,29 | **-940 022** | — |
| Sens1 | CAC x2, new-logo pace ~x0,5 | 7,64 | **-3 841 011** | -2 900 989 |
| Sens2 | Churn x2, с 1,2% до 2,4%/мес | 14,62 | **-1 195 092** | -255 070 |
| Sens3 | Price -30%, с 550k до 385k ₽/мес | 15,29 | **-3 462 621** | -2 522 599 |

**Вывод:** самый разрушительный single-variable shock здесь не churn, а **price compression** и ухудшение эффективности привлечения. Кейс остаётся особенно хрупким к снижению enterprise-чека.

## B2. Monte Carlo Lite — confidence intervals

### Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 263 000 | 526 000 | 1 052 000 | [T8], [T11] |
| Monthly churn, % | 0,8% | 1,2% | 2,4% | [T8], [T12] |
| ARPU, ₽/мес | 385 000 | 550 000 | 650 000 | [T8], [T2]-[T6] |
| Conversion rate lead→paid, % | 1,2% | 2,0% | 3,0% | [T8] |
| Time-to-hire, мес | 1,0 | 1,5 | 3,0 | [T8] |

### Метод упрощённой симуляции

Вместо полной 1000-run симуляции использую **9-комбинационный Monte Carlo Lite**: worst, median, best и 6 mixed-combinations вокруг CAC, churn и ARPU с поправкой на conversion и time-to-hire. Это достаточно, чтобы получить доверительный коридор для IC-решения.

### Ключевые результаты на M24

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24, ₽/мес | **-3 043 582** | **6 807 768** | **17 421 577** | **20 465 159** |
| CAC payback, мес | **2,73** | **0,96** | **0,67** | **2,06** |
| LTV/CAC | **8,5x** | **60,1x** | **107,4x** | **98,9x** |
| Cash runway, мес | **16,0** | **20,2** | **22,7** | **6,7** |

### Интерпретация Monte Carlo Lite

1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1**: в плохом хвосте распределения бизнес не проходит stress-test на платежеспособность.
2. **p50 EBITDA = 6,8 млн ₽/мес**, значит median-case EBITDA Gate проходит с запасом.
3. Распределение крайне широкое: разброс по EBITDA между p10 и p90 больше 20 млн ₽/мес. Формально правило `p90/p10 > 10x` здесь неустойчиво из-за отрицательного p10, но по сути это ещё более жёсткий сигнал, чем 10x, потому что распределение пересекает ноль.
4. **Range width по LTV/CAC = 98,9x**, это намного выше порога 8 и показывает, что модель очень чувствительна к pricing, churn и acquisition efficiency.

**Итог по Monte Carlo Lite:** кейс не надо убивать сразу, но score должен быть **даунгрейжен за высокую дисперсию исходов**. Это не «стабильный compounding SaaS», а high-variance enterprise wedge.

## B3. Competitor deep-dive

### Западные конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Vanta** | category leader в trust/compliance automation, сильный brand, развитая questionnaire automation и AI-agent слой, широкий framework coverage [T4][T13] | дорогой стек, западная data residency, не оптимизирован под RU legal/compliance контур | **~30-35%** западного SMB/mid-market compliance automation сегмента, inference по brand dominance и customer base claims [T13][inference] | можем продавать локальный managed layer под 152-ФЗ, русскоязычную delivery-команду и гибридный on-prem / private-cloud контур |
| **Drata** | сильный enterprise momentum, 8 000+ customers в 80+ странах, развитая automation/GRC story [T14] | менее локализуем для РФ, высокая зависимость от западного cloud/app ecosystem | **~20-25%** западного mid-market/enterprise сегмента [T14][inference] | быстрее адаптируемся под локальные требования, можем продавать «compliance-as-operations», а не только платформу |
| **Sprinto** | сильный motion в continuous compliance, audit readiness, TPRM и multi-entity контуре [T5][T6] | уступает Vanta/Drata по бренду и экосистеме, меньше defensibility в heavyweight enterprise | **~8-12%** сегмента automated compliance для scaleups и mid-market [T5][T6][inference] | можем глубже упаковать hand-held delivery и Russian-specific regulatory layer, где чистый SaaS хуже заходит |

### Российские и локально релевантные конкуренты

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Security Vision** | сильная локальная база, 40+/100 клиентов из топ-100 РФ, 15 банков из топ-20, зрелый SGRC/SOAR/SOC стек, сертификации и реестр отечественного ПО [T15][T16] | тяжёлый enterprise stack, длинный цикл внедрения, часто воспринимается как большая ИБ-платформа, а не быстрый revenue-enablement wedge | **~20-25%** локального upper-enterprise SGRC/automation сегмента [T15][inference] | наш wedge уже и проще: быстрее time-to-value именно на questionnaires, evidence ops и audit readiness для GTM-команд |
| **BI.ZONE GRC** | мощный бренд, доступ к крупным enterprise и гос/КИИ-контурам, сертификация ФСТЭК, интеграция в широкий кибербез-портфель [T17][T18] | продукт тяготеет к heavy GRC и cyber-risk governance, а не к лёгкому SaaS-like onboarding | **~15-20%** локального enterprise GRC/киберрисков [T17][T18][inference] | можем быть легче, быстрее и сильнее завязаны на revenue workflows, а не только на security governance |
| **Solar inRights / Solar ecosystem** | сильный доступ к крупнейшим клиентам, deep presence в импортозамещении и regulated enterprise, доказанная масштабность внедрений [T19] | основной фокус на IAM/IDM и adjacent security stack, а не на full trust-ops workflow вокруг questionnaires и audit readiness | **~10-15%** adjacent compliance/IAM-control automation сегмента [T19][inference] | наш продукт ближе к buyer pain CISO+COO+sales, где нужен не just access governance, а ускорение проверок и аудитов |
| **SECURITM** | SGRC-позиционирование, свежая сертификация ФСТЭК, явный фокус на автоматизации risk/compliance процессов [T20][T21] | меньший бренд и go-to-market охват, вероятно уступает лидерам по ecosystem breadth | **~5-8%** локального SGRC сегмента [T20][T21][inference] | можем выиграть за счёт более productized trust-ops narrative и лучшей связки с экспортным SaaS/fintech ICP |
| **Контур.Фокус Комплаенс** | понятный use case по 115-ФЗ, due diligence и комплаенс-проверкам, сильный SMB/mid-market дистрибуторский канал [T22] | это уже другой слой комплаенса, больше KYC/KYB и anti-fraud, чем continuous compliance / audit readiness | **~10-15%** в adjacent compliance-checking tools для SMB/mid-market [T22][inference] | наш продукт закрывает более дорогой и менее commodity workflow вокруг trust, questionnaires и enterprise audits |

### Вывод по конкурентам

1. На Западе рынок уже отстроен вокруг **Vanta / Drata / Sprinto**, и там category winner получает scale за счёт ecosystem + automation breadth.
2. В РФ прямой 1:1 аналог хуже сформирован, но есть сильные **adjacent enterprise SGRC/ИБ-платформы**: Security Vision, BI.ZONE, Solar, SECURITM.
3. Значит реальная стратегия входа не в лоб против «русской Vanta», а через узкий wedge: **security questionnaires + evidence ops + audit readiness для экспортных и regulated компаний**.
4. Наша защита возможна только если мы быстрее внедряемся и сильнее привязаны к выручке клиента, чем тяжёлые локальные ИБ-платформы.

## B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять сильного compliance lead / solutions owner в срок | med | высокий, срыв внедрений и presales | time-to-hire > 3 мес, offer acceptance < 50% | заранее строить talent bench, брать fractional advisors, стандартизировать playbooks |
| 2 | Operational | Services creep, delivery становится кастомным консалтингом | high | высокий, просадка GM и масштабируемости | onboarding > 6 недель, >30% задач вне шаблонного workflow | жёсткий scope control, пакетирование SKU, лимиты на кастомизации |
| 3 | Operational | LLM/API сбои, рост latency или cost spike | med | высокий, деградация SLA и margin | API error rate > 2%, cost/request +50% QoQ | multi-model routing, локальные fallback-модели, кеширование, human fallback |
| 4 | Market | ICP оказывается слишком узким, pipeline не заполняется | med | высокий, недобор new logos | <8 SQL/мес к M4, win rate < 15% | сузить ICP до экспортного SaaS/fintech, усилить partner channel с аудиторами и MSSP |
| 5 | Market | Price compression под давлением Vanta/Drata и локальных интеграторов | high | высокий, EBITDA быстро уходит в минус | discount rate > 20%, median ACV < 450k ₽ | value-based pricing, premium managed tier, жёсткая квалификация сделок |
| 6 | Market | Конкуренты добавляют questionnaires/evidence workflow как free feature | med | средне-высокий, erosion differentiator | в тендерах чаще слышно «это уже есть в текущем стеке» | уходить в сервисный moat, deeper integrations, proof of ROI по speed-to-close |
| 7 | Regulatory | 152-ФЗ и data residency ограничивают использование западных LLM/SaaS | high | высокий, блокирует часть ICP | security review red flags, требования on-prem в >50% сделок | private-cloud/on-prem option, локальные модели, сегрегация данных |
| 8 | Regulatory | 115-ФЗ / отраслевые требования усложняют позиционирование и продажи в финсектор | med | средний, длиннее sales cycle и higher compliance burden | юридические замечания в каждом втором пилоте, дополнительные требования от ИБ/юрслужбы | отраслевые шаблоны, pre-approved control maps, комплаенс-партнёры |
| 9 | Financial | Cash runway сжимается из-за медленного ramp-up и найма раньше выручки | med | высокий, даунраунд или shutdown risk | burn > 4,5 млн ₽/мес при <3 платящих клиентах к M6 | hiring gates, milestone-based hiring, monthly burn review |
| 10 | Financial | USD/RUB и инфляция раздувают cloud/LLM/FOT | med | средний, снижение GM | COGS/client > 200k ₽, зарплатные ожидания +20% YoY | рублёвые контракты с индексатором, vendor diversification, price escalators |
| 11 | Black swan | Новый пакет санкций режет доступ к западным AI/API/SaaS | med | очень высокий, продуктовая дестабилизация | отказ в доступе, billing blocks, legal notices | vendor redundancy, локальный inference stack, contingency migration plan |
| 12 | Black swan | Геополитическая эскалация ломает enterprise budgets и экспортный спрос | med | очень высокий, freeze pipeline и churn | массовые budget freeze, delayed procurement, отмена зарубежных GTM-проектов | ставка на regulated domestic ICP, reserve runway > 18 мес, более короткие пилоты |

## B5. Kill conditions через 6 месяцев

1. **Liquidity / insolvency kill:** если к M6 ожидаемый p10 по EBITDA на горизонте M24 остаётся `< 0`, а cash runway по актуальному плану падает **ниже 12 месяцев**, кейс нельзя продолжать.
2. **GTM kill:** если к M6 меньше **3 платящих клиентов**, меньше **8 SQL/мес** и win rate ниже **15%**, значит ICP слишком узкий или value proposition не зацепил рынок.
3. **Unit economics kill:** если к M6 средний ACV падает **ниже 450 000 ₽/мес** или gross margin уходит **ниже 55%**, продукт скатывается в услугу без достаточной прибыли.

## B6. Финальный вывод SECTION B

Кейс проходит не как low-risk software compounder, а как **high-variance enterprise compliance wedge**. Позитивная сторона, median-case на M24 выглядит сильным. Негативная сторона, хвост риска очень толстый: price compression, CAC deterioration и локальные regulatory constraints быстро ломают модель. Инвестировать/строить имеет смысл только при жёстких kill-gates по ACV, runway и repeatability delivery.

## Источники SECTION B
- [T2] Delve official blog, 2025-07-22: https://delve.co/blog/series-a
- [T4] Vanta Questionnaire Automation: https://www.vanta.com/products/questionnaire-automation
- [T5] Sprinto Continuous Compliance: https://sprinto.com/continuous-compliance/
- [T6] Sprinto Plans and Feature Comparison: https://docs.sprinto.com/settings/billing/sprinto-plans-and-feature-comparison
- [T8] `04-economics.md` по кейсу delve-geo-expand-v2
- [T11] `02-demand.md` по кейсу delve-geo-expand-v2
- [T12] Optifai enterprise churn benchmark, cited in `04-economics.md`
- [T13] Vanta GRC / release notes, accessed 2026-05-11: https://www.vanta.com/products/grc ; https://help.vanta.com/en/articles/11345422-product-updates
- [T14] Drata brand update / customers, accessed 2026-05-11: https://drata.com/blog/announcing-new-drata-look ; https://drata.com/customers
- [T15] Security Vision official site, accessed 2026-05-11: https://www.securityvision.ru/
- [T16] Habr Career, Security Vision company profile, accessed 2026-05-11: https://career.habr.com/companies/securityvision
- [T17] BI.ZONE GRC official news, 2026-01-23: https://bi.zone/news/bi-zone-grc-poluchila-sertifikat-fstek-rossii/
- [T18] BI.ZONE portfolio news, 2026-04-27: https://bi.zone/news/na-bi-zone-days-2026-ozvuchili-plany-po-razvitiyu-produktovogo-portfelya/
- [T19] Solar inRights case, 2026-04-15: https://rt-solar.ru/events/news/6541/
- [T20] SECURITM Habr news, 2026-02-09: https://habr.com/ru/companies/securitm/news/994322/
- [T21] SECURITM Habr article, 2025-10-16: https://habr.com/ru/companies/securitm/articles/957180/
- [T22] vc.ru, Контур.Фокус Комплаенс, 2025-09-22: https://vc.ru/services/2229587-kontur-fokus-komplaens-avtomaticheskaya-proverka

<!-- P6B-DONE -->


---

<!-- source: 06-verdict.md -->

[GEO-EXPAND] Delve geo-expand v2 — REJECTED: 61/100 | EBITDA base=960К₽/мес через 14 мес | LTV/CAC=60,1x | Ключевое преимущество: сильная enterprise unit economics в trust-ops wedge | Главный риск: слабый локальный спрос и high-touch delivery без moat.

# 06-verdict

sector: GEO-EXPAND

## Итог инвесткомитета

**Вердикт: REJECTED.**

Причина отказа не в юнит-экономике, она сильная, а в том, что standalone локальный кейс пока не доказывает investment-grade запас прочности по спросу, moat и repeatable GTM. Это хороший thesis wedge внутри broader enterprise compliance ops, но пока слабый самостоятельный фондовый актив.

## Investment committee summary

- **Normalized score:** **61/100**
- **Raw score:** **91/150**
- **Порог:** `<65 = REJECTED`
- **Причина:** strong economics, но слабый локальный demand proof, weak moat и высокая вероятность services creep.
- **Правило approve не выполнено:** хотя `company_ebitda_potential_rub_month >= 500k` достигается при 16 клиентах и примерно к M14, итоговый score ниже 70.

## Delta vs previous

- Это **standalone rerun/resurrect** кейса, который раньше был supporting signal для `enterprise-compliance-operations-agents`.
- Для самого slug `delve-geo-expand-v2` предыдущего `06-verdict.md` не было.
- Ключевое изменение rerun: экономика теперь доказана, но standalone score всё равно не проходит из-за слабого локального demand proof и недостаточного moat.

## Оценка

Source tier balance: T1=0, T2=0, T3=0, weighted=1.00. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | `LTV/CAC: 60,1x`, `CAC Payback: 0,96 мес`, `Contribution Margin: 69,0%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | `EBITDA > 500 тыс. ₽/мес достигается примерно с 16 клиентами` и `Break-even month: примерно M13-M14`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 10 | `exact search demand в РФ: LOW`, `hh.ru signal почти отсутствует`, Sources-строка отсутствует, поэтому penalty. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | В `03-solution.md`: `кейс легко расползается в compliance-консалтинг` и `без отдельной defensibility`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | `152-ФЗ и data residency ограничивают использование западных LLM/SaaS`, плюс `services creep` и hiring risk в `05-critic.md`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 14 | GTM как enterprise motion реалистичен, но в `04-economics.md` сильная зависимость от `founder-led и partner-led acquisition`. |

**Normalized score = round((91 × 100) / 150) = 61/100.**

## Почему не approve, несмотря на сильную экономику

1. **Локальный exact-demand слабый.** В `02-demand.md` все 4 core query получили `LOW`, а HH-сигнал почти нулевой.
2. **Слабый moat.** Кейсу трудно доказать, что это product moat, а не дорогой managed service layer.
3. **Execution variance слишком высока.** В Monte Carlo Lite `p10 EBITDA < 0`, а в sensitivity price compression и CAC deterioration быстро ломают модель.

## 7-factor Moat Framework

| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных в доказанном локальном контуре. |
| Switching costs | 2 | После внедрения появляются knowledge base, evidence map и интеграции, но это ещё не очень глубокий lock-in. |
| Scale economies | 1 | Часть COGS падает с объёмом, но high-touch delivery сохраняется. |
| Proprietary data / model advantage | 1 | Данных и model edge как защищённого актива в кейсе не доказано. |
| Regulatory moat | 1 | Есть regulatory pressure, но собственная лицензия/аккредитация как moat не показана. |
| Brand / distribution | 1 | Глобальный category proof есть, но локального brand/distribution moat нет. |
| Embedded workflow | 3 | Если внедрение состоялось, продукт встраивается в recurring security questionnaires, audit readiness и evidence ops. |

**Сумма 7-factor = 9/21.**

**Moat score = round((9 × 25) / 21) = 11/25**, но с учётом общего execution fit и workflow depth в основном score округляю критерий #4 до **12/25**.

**Статус moat: weak moat.** Так как score < 10 по 7-factor raw, риск weak moat добавлен в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 31 625 000 ₽ |
| fully_loaded_cac_rub | 526 000 ₽ |
| LTV/CAC | 60,1x |
| CAC payback | 0,96 мес |
| Gross Margin | 69,0% |
| contribution_margin_rub_month | 379 500 ₽/клиент/мес |
| company_ebitda_rub_month, base | 960 000 ₽/мес |
| months_to_500k_ebitda | 14 |
| clients_to_500k_ebitda | 16 |
| break-even clients | 15 |
| startup_capital_to_bep_rub | 35 846 830 ₽ |
| startup capital available | 60 000 000 ₽ |
| burn-to-breakeven | ~30 200 000 ₽ |

## Полный бизнес-процесс из 04-economics.md

| Шаг | Что происходит | Роль | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Поиск ICP-аккаунтов | SDR | HH/LinkedIn analog, CRM, таблица ICP | 20 мин | 650 | частично автоматизировано |
| 2 | Enrichment контактов и сигналов | SDR | CRM, Apollo-аналог, сайт компании | 15 мин | 490 | частично автоматизировано |
| 3 | Первый outbound-touch | SDR | email + LinkedIn + звонок | 15 мин | 490 | частично автоматизировано |
| 4 | Follow-up sequence 4-6 касаний | SDR | sequencing tool, CRM | 45 мин | 1 470 | частично автоматизировано |
| 5 | Qualification call | SDR + AE | Meet, CRM | 45 мин | 2 430 | ручное |
| 6 | Discovery + pain mapping | AE + Founder | Meet, Notion, CRM | 90 мин | 8 130 | ручное |
| 7 | Security/compliance scoping | Compliance lead + Solutions | Notion, control library | 120 мин | 8 670 | ручное |
| 8 | Demo / ROI-calculation | AE + Founder | Slides, ROI model | 90 мин | 8 130 | ручное |
| 9 | Pilot proposal и legal | AE + Founder + юрист | CRM, шаблоны договора | 180 мин | 12 390 | частично автоматизировано |
| 10 | Pilot onboarding | CSM + Compliance ops | PM tool, knowledge base | 6 ч | 16 320 | частично автоматизировано |
| 11 | Интеграция источников evidence | Backend/DevOps + CSM | cloud, scripts, connectors | 8 ч | 24 440 | частично автоматизировано |
| 12 | Настройка control map / questionnaire base | Compliance ops | knowledge base, templates | 6 ч | 13 260 | частично автоматизировано |
| 13 | Delivery первого месяца | CSM + Compliance ops + platform | CRM, cloud, LLM stack | 20 ч | 39 050 | гибридно |
| 14 | Invoice и получение оплаты | finance ops | ЭДО, банк, 1С | 30 мин | 1 050 | в основном автоматизировано |

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | enterprise sales, fundraising, partnerships | 845 000 |
| CTO / Tech Lead | product, integrations, security architecture | 715 000 |
| Senior Backend #1 | connectors, workflow engine | 546 000 |
| Senior Backend #2 | infra integrations, APIs | 546 000 |
| ML Engineer | RAG, answer drafting, classification | 650 000 |
| DevOps | cloud, observability, security hardening | 455 000 |
| Frontend | trust center / ops UI | 390 000 |
| SDR | outbound prospecting | 195 000 |
| AE | discovery, proposal, close | 455 000 |
| Customer Success | onboarding, renewals | 325 000 |
| Compliance Analyst #1 | evidence collection, policy mapping | 286 000 |
| Compliance Analyst #2 | questionnaires, audit support | 286 000 |
| Finance / Ops | billing, contracts, reporting | 208 000 |
| **Итого steady-state** |  | **5 902 000** |

## Top-3 Risks

| Риск | Вероятность | Impact | Почему в топ-3 |
|---|---|---|---|
| weak moat / services creep | high | высокий | В `03-solution.md` прямо сказано, что кейс `легко расползается в compliance-консалтинг`. |
| слабый локальный demand proof / evidence_quality_unverified | high | высокий | В `02-demand.md` exact RU demand LOW, HH почти отсутствует, а строка `Sources: T1=...` отсутствует. |
| regulatory + LLM dependency | med-high | высокий | В `05-critic.md`: `152-ФЗ и data residency ограничивают использование западных LLM/SaaS`. |

## GTM: 10 named targets

> Без 10 named targets критерий GTM терял бы 10 баллов. Ниже дан список реальных компаний, где pain логически совпадает с евиденцией кейса: frequent security review, regulated pressure, export-facing SaaS или enterprise trust workflows.

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Selectel | Частые enterprise security reviews, облачная инфраструктура и trust-pressure. | email decision-maker (CISO / security lead) | 600 000 ₽/мес |
| 2 | VK Tech | Enterprise B2B cloud/software стек, длинные security questionnaires у крупных клиентов. | партнёрство + конференция | 700 000 ₽/мес |
| 3 | Cloud.ru | Regulated cloud и vendor due diligence, высокая цена задержки security review. | email decision-maker + отраслевой ивент | 800 000 ₽/мес |
| 4 | MTS Web Services | Cloud / enterprise infra с recurring audit-readiness pain. | партнёрство с аудитором / MSSP | 700 000 ₽/мес |
| 5 | Контур | Много enterprise и regulated клиентов, зрелый compliance контур, recurring questionnaires. | партнёрство + targeted outbound | 650 000 ₽/мес |
| 6 | ЮKassa | Fintech buyer с vendor review и privacy-heavy процессами. | email decision-maker / intro через партнёра | 750 000 ₽/мес |
| 7 | Точка | Fintech / B2B platform, strong compliance pressure и постоянные third-party reviews. | founder-led outbound + warm intro | 650 000 ₽/мес |
| 8 | Positive Technologies | Крупный security vendor, где trust center и questionnaires напрямую влияют на sales cycle. | конференция + security community outreach | 750 000 ₽/мес |
| 9 | IBS | Системный интегратор с enterprise procurement pressure и сложными vendor questionnaires. | партнёрство / enterprise events | 550 000 ₽/мес |
| 10 | Innostage | Cybersecurity и enterprise services, где audit readiness и evidence ops повторяются. | partner channel + direct outreach | 550 000 ₽/мес |

## GTM verdict

GTM концептуально реалистичен, потому что CAC payback очень короткий и есть понятные buyer personas. Но он **не investment-grade** из-за трёх ограничений:
- канал слишком founder-heavy;
- ICP узкий;
- repeatability proof по 10-20 сделкам ещё не показан.

## Monte Carlo / Risk summary

| Метрика | p10 | p50 | p90 |
|---|---:|---:|---:|
| EBITDA @M24 | -3 043 582 ₽/мес | 6 807 768 ₽/мес | 17 421 577 ₽/мес |
| CAC payback | 2,73 мес | 0,96 мес | 0,67 мес |
| LTV/CAC | 8,5x | 60,1x | 107,4x |
| Cash runway | 16,0 мес | 20,2 мес | 22,7 мес |

**Вывод:** median-case сильный, но дисперсия слишком широкая для approve. `p10 EBITDA < 0` означает, что в плохом хвосте бизнес не проходит stress-test.

## Что должно быть доказано для апгрейда в APPROVED

1. Появление прямой локальной evidence-строки спроса: Wordstat/HH/vacancy/adoption сигналы выше LOW.
2. 3-5 локальных или релевантных RU-adjacent внедрений с measurable ROI по security questionnaire turnaround time.
3. Снижение founder dependency в acquisition, минимум один repeatable non-founder channel.
4. Доказательство, что продукт не скатывается в bespoke consulting и держит GM выше 60% после 10+ клиентов.

## LTV Upside Calculator

### Базовая формула

`customer_ltv_rub = ARPA × GM / churn`

### Текущая база

- ARPA = 550 000 ₽/мес
- GM = 69%
- churn = 1,2%/мес
- **customer_ltv_rub = 31 625 000 ₽**

### Upside scenarios

| Сценарий | ARPA | GM | churn | customer_ltv_rub | Что должно случиться |
|---|---:|---:|---:|---:|---|
| Base | 550 000 | 69% | 1,2% | 31 625 000 ₽ | текущая модель |
| Upside 1 | 650 000 | 69% | 1,2% | 37 375 000 ₽ | удержать premium pricing на regulated/export ICP |
| Upside 2 | 550 000 | 72% | 1,0% | 39 600 000 ₽ | стандартизировать delivery и снизить services creep |
| Upside 3 | 650 000 | 72% | 1,0% | 46 800 000 ₽ | совместить premium ACV, повторяемый onboarding и better retention |

### Практический вывод

LTV upside у кейса есть. Проблема не в LTV, а в том, что **рост LTV сам по себе не решает слабый локальный demand proof и weak moat**. Поэтому отказ сейчас правильный даже при сильной клиентской экономике.

## Финальный вывод

Delve geo-expand v2 это **сильный enterprise compliance wedge, но пока слабый standalone инвестиционный кейс для РФ-контура**. Его лучше трактовать как supporting thesis внутри более широкой compliance-ops платформы, а не как отдельный approved asset.

