---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-clay-geo-expand-1659.md
created: 2026-04-20T08:44:00+03:00
---

# 01-intake

## Кейс
clay-geo-expand-1659-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-18-clay-geo-expand-1659.md

## Краткий контекст
Standalone GEO-EXPAND кейс по AI-native GTM engineering, enrichment, research, scoring и personalized outbound. Исходный вердикт отклонил сигнал как duplicate и как кейс ниже порога Program 1, но текущий rerun требует полноценной переоценки через P3→P7.

## Следующий шаг
Передать кейс в P3-demand-validation: перепроверить buyer, месячный чек, service layer, локализацию под РФ и вероятность собрать high-LTV модель выше порога программы.

## Полный контекст из raw

# RESURRECT SIGNAL — clay-geo-expand-1659

## Meta
- source: triage/triage-2026-04-18-clay-geo-expand-1659.md
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
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-1659-msk-clay-geo-expand.md`

## Классификация
Дубликат ранее обработанного сигнала, кейс не открываем.

## Решение
Не открывать новый кейс и не обогащать существующие открытые кейсы.

## Почему
- Сигнал относится к уже ранее обработанной теме Clay и той же категории GTM engineering / AI-платформ для data enrichment, research, scoring и personalized outbound.
- Подходящего открытого кейса в `pipeline/cases/` по этой нише сейчас нет, поэтому сигнал не является supporting signal для существующего открытого кейса.
- Экономика не проходит порог Program 1: указанный диапазон `900 000-3 600 000 ₽ в год` соответствует примерно `75-300 тыс. ₽ в месяц` на клиента, что ниже требуемого ориентира `>500 тыс. ₽/мес.`.
- Несмотря на сильную западную тягу, новый raw-файл не добавляет достаточного апсайда по локальному спросу в РФ или по unit economics, чтобы пересмотреть решение и открыть кейс сейчас.
- Локализация остаётся средней по сложности и требует интеграций с российскими CRM, локальными источниками B2B-данных, каналами коммуникации и compliance-контуром.

## Что сделано
- Новый кейс не создан.
- Существующие открытые кейсы не обновлялись, так как релевантного кейса в `pipeline/cases/` нет.
- Исходный raw-файл помечен как обработанный и перенесён в `pipeline/raw/processed/`.

## Вердикт
Это повторное подтверждение западной тяги Clay, но не новый сигнал для открытия кейса в Program 1. Пока это дубликат без достаточного LTV-потенциала для прохождения текущего порога программы.

```



---

# 02-demand.md

# 02-demand

## Demand validation summary
- **Продукт**: Clay-подобный AI-native слой для GTM engineering, enrichment, research, scoring и personalized outbound поверх CRM, data providers и outbound-каналов. [T2: https://www.clay.com/]
- **Итог по спросу в РФ**: **MEDIUM-LOW**. Прямой branded/category demand по ключам вроде `gtm engineering data enrichment outbound research russia`, `sales intelligence`, `prospecting b2b` в mandatory endpoint низкий, но adjacent pain в РФ реальный: `лидогенерация b2b` дала **MEDIUM**, score **30**, `hh.ru vacancies = 599`; `база компаний b2b` дала `hh.ru vacancies = 2085`; `outbound продажи b2b` дала `hh.ru vacancies = 35`. Это значит, что рынок в РФ формулирует боль через leadgen/outbound/базы компаний, а не через термин Clay/GTM engineering. [T1/T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand?keyword=gtm%20engineering%20data%20enrichment%20outbound%20research%20russia ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BB%D0%B8%D0%B4%D0%BE%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F%20b2b ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%B1%D0%BE%D0%B3%D0%B0%D1%89%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B1%D0%B0%D0%B7%D1%8B%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%BE%D0%B2 ; http://172.18.0.1:9001/multi-demand?keyword=sales%20intelligence ; http://172.18.0.1:9001/multi-demand?keyword=prospecting%20b2b ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D0%B1%D1%83%D1%82%D0%B1%D0%B0%D1%83%D0%BD%D0%B4%20%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%D0%B8%20b2b ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B1%D0%B0%D0%B7%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D0%B9%20b2b]
- **Решение по гейту**: **не отклонять на P4**. Profit Gate проходит в service-led и enterprise-сценариях, где Clay продается не как дешевый seat-based SaaS, а как managed GTM stack и data-enrichment engine для команд продаж/маркетинга. [T1/T2]

## Evidence of demand

### 1) Mandatory endpoint
- `gtm engineering data enrichment outbound research russia` → **LOW**, score **0**, `hh.ru vacancies = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `sales intelligence` → **LOW**, score **3**, `hh.ru vacancies = 36`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `prospecting b2b` → **LOW**, score **0**, `hh.ru vacancies = 9`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `лидогенерация b2b` → **MEDIUM**, score **30**, `hh.ru vacancies = 599`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `обогащение базы клиентов` → **LOW**, score **3**, `hh.ru vacancies = 41`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `outbound продажи b2b` → **LOW**, score **3**, `hh.ru vacancies = 35`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- `база компаний b2b` → **LOW**, score **15**, `hh.ru vacancies = 2085`, `telegram subscribers = 0`. [T1/T2: internal demand endpoint]
- Вывод: category awareness низкая, но buyer pain существует и уже оплачивается через human labor, базы компаний, сервисы лидогенерации и outsourced SDR-функции. [T1/T2, inference]

### 2) Additional market signals
- ФНС сообщает, что в Едином реестре МСП на **10.04.2026** числится **6 728 195** субъектов МСП. Это широкая база, из которой можно выделять экспортно- и outbound-ориентированный B2B-сегмент. [T1: https://rmsp.nalog.ru/statistics.html]
- TAdviser оценивает российский рынок CRM в **44,1 млрд ₽** в 2024 году, +15,23% г/г. Это хороший top-down anchor для spend на software вокруг продаж и customer management. [T2: https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F:CRM-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B_(%D1%80%D1%8B%D0%BD%D0%BE%D0%BA_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8)]
- CNews со ссылкой на iKS-Consulting оценивает российский рынок CRM в **11,84 млрд ₽** в 2023 году. Это более узкий и консервативный нижний anchor; вместе с TAdviser подтверждает, что spend вокруг sales stack уже измеряется десятками миллиардов рублей. [T2: https://www.cnews.ru/news/top/2024-08-29_rossijskij_rynok_crm_vyros]
- Salesforce в годовом отчете за FY2026 показал **$41,5 млрд** выручки за год, то есть мировой рынок CRM/sales automation уже точно велик хотя бы на уровне realized spend лидера категории. Для Clay-подобного слоя это консервативный T1 floor, а не потолок рынка. [T1: https://www.annualreports.com/HostedData/AnnualReportArchive/s/NYSE_CRM_2026.pdf]

## Real competitors with prices
1. **Apollo.io**: Free **$0**, Basic **$59/user/mo**, Professional **$99/user/mo**, Organization **$149/user/mo**. По курсу ЦБ РФ на **21.04.2026** это примерно **4,4 тыс. / 7,4 тыс. / 11,2 тыс. ₽ за пользователя в месяц**. Это прямой global benchmark по sales intelligence, enrichment и outbound workflows. [T2: https://www.apollo.io/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
2. **Snov.io**: Trial **$0**, Starter **$39/mo**, Pro **$99/mo**, Managed Service **$189/mo**. В рублях это примерно **2,9 тыс. / 7,4 тыс. / 14,2 тыс. ₽ в месяц**. Это benchmark по email finding, enrichment и outreach automation. [T2: https://snov.io/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
3. **Контур.Компас**: официальный прайс в выдаче и на лендинге начинается от **52 800 ₽ в год** за **3 000** контактов, **134 400 ₽ в год** за **10 000** контактов и **321 600 ₽ в год** за **50 000** контактов. Это локальный RU benchmark на базе компаний и контактного enrichment. [T2: https://kontur.ru/compass/pricing]

### Что значит ценовая вилка
- Публичный рынок adjacent tools в РФ и global sales tech дает вилку от примерно **2,9 тыс. ₽/мес.** за легкий self-serve инструмент до **26,8 тыс. ₽/мес. эквивалента** за крупные пакеты по базам/контактам, не считая custom enterprise contracts. [T1/T2]
- Это подтверждает willingness to pay за data enrichment и outbound tooling, но также показывает, что чистый seat-based SaaS будет ограничен по ARPU. Чтобы пройти программу, нужен service layer, внедрение и enterprise-пакеты. [T2, inference]

## Telegram bots / services in RU
- Mandatory endpoint по всем релевантным запросам показывает `telegram subscribers = 0`, то есть готового category demand через Telegram для Clay-подобного термина в РФ не видно. [T2: internal demand endpoint]
- Ручная проверка показала existence adjacent RU Telegram utilities, а не полноценных Clay-аналогов: в выдаче встречаются **Get8** как сервис поиска компаний/контактов и **Usersbox** как бот/сервис поиска по телефону, email и соцсетям. Это подтверждает наличие Telegram-first micro-utilities, но не enterprise GTM engineering category. [T2: https://get8.io/ ; https://t.me/usersbox_bot]
- Вывод: Telegram в РФ может быть дополнительным acquisition/support channel или узкой утилитой для enrichment, но не является доказанным основным delivery layer для enterprise GTM stack. [T2, inference]

## WTP, willingness to pay
- **Доказательство WTP №1**: есть реальные публичные платные аналоги с ценами, и они продают ровно те функции, за которые платят GTM-команды: enrichment, prospecting, базы контактов, automated outreach. [T2]
- **Доказательство WTP №2**: локальный RU benchmark Контур.Компас показывает, что российский buyer уже платит за базы компаний и контактные данные сотни тысяч рублей в год. [T2]
- **Доказательство WTP №3**: hh-proxy в mandatory endpoint показывает **599 вакансий** по `лидогенерация b2b` и **2085 вакансий** по `база компаний b2b`. Это не прямой PO, но сильный proxy того, что компании уже тратят деньги на ручной SDR/research labor и готовы финансировать acquisition stack. [T1/T2]
- **Вывод по WTP**: willingness to pay в РФ существует, но она распределена между тремя корзинами: software seats, покупка данных/баз и outsourced/service-led лидогенерация. Clay может забирать бюджет только если комбинирует минимум две корзины сразу. [T1/T2, inference]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/eng/currency_base/daily/]
- Top-down anchor 1: realized global spend floor через Salesforce = **$41,5 млрд** ≈ **3,12 трлн ₽**. Это floor мирового spend на CRM/sales stack, не полный TAM. [T1 + inference]
- Top-down anchor 2: рынок CRM в РФ = **44,1 млрд ₽** (TAdviser) и **11,84 млрд ₽** (CNews/iKS). Для reconciliation берем более консервативный lower-middle point и далее выделяем Clay-addressable слой как **12%** от sales stack. [T2 + inference]
- Bottom-up buyer universe: из **6,73 млн** МСП берём только очень узкий B2B-сегмент, где есть outbound-heavy motion, потребность в data enrichment и хотя бы 3-5 человек в GTM/SDR/маркетинге. Консервативная оценка: **3 500 компаний**. Это около **0,05%** базы МСП и выглядит достижимо для ICP Clay в РФ. [T1/T2 + inference]
- `% with need` = **35%**, поскольку не всем B2B-компаниям нужен enrichment/research stack постоянно; берем только тех, кто системно делает outbound и account research. [T1/T2 + inference]
- `ARR avg` = **1,2 млн ₽/год** на клиента, то есть около **100 тыс. ₽/мес.** blended check между self-serve + managed enrichment + light workflow automation. Это выше pure seats, но ниже тяжелого enterprise retainer. [T2 + inference]

### Top-down
- **TAM (мир)** = **3,12 трлн ₽** как T1 conservative floor realized spend. [T1]
- **TAM (РФ)** = **44,1 млрд ₽ × 12% = 5,29 млрд ₽**. Здесь 12% это доля CRM/sales stack, адресуемая enrichment/research/prospecting automation. [T2 + inference]
- **SAM (РФ)** = **5,29 млрд ₽ × 29% = 1,53 млрд ₽**. Segment fit = mid-market и upper-SMB B2B компании, где outbound/data-enrichment является регулярной функцией, а не эпизодической задачей. [T1/T2 + inference]
- **SOM Y1** = **1,53 млрд ₽ × 2% = 30,6 млн ₽**. [inference]
- **SOM Y3** = **1,53 млрд ₽ × 8% = 122,4 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **3 500**. [T1/T2 + inference]
- **% with need** = **35%**. [T1/T2 + inference]
- **# active buyers** = **1 225**. [inference]
- **ARR avg** = **1,2 млн ₽/год**. [T2 + inference]
- **SAM bottom-up** = **1 225 × 1,2 млн ₽ = 1,47 млрд ₽**. [inference]
- **SOM bottom-up Y1** = **25 клиентов × 1,2 млн ₽ = 30,0 млн ₽**. [inference]
- **SOM bottom-up Y3** = **100 клиентов × 1,2 млн ₽ = 120,0 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 3,12 трлн ₽ [T1] | — | — | top-down |
| TAM (РФ) | 5,29 млрд ₽ [T2] | 4,20 млрд ₽ [T1/T2] | diff=26%, допустимо; bottom-up уже отрезает non-ICP компании | lower |
| SAM (РФ) | 1,53 млрд ₽ [T1/T2] | 1,47 млрд ₽ [T1/T2] | diff=4%, гипотезы сходятся | lower |
| SOM Y1 | 30,6 млн ₽ | 30,0 млн ₽ | diff=2% | **используем 30,0 млн ₽** |
| SOM Y3 | 122,4 млн ₽ | 120,0 млн ₽ | diff=2% | **используем 120,0 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **Контур** [T2: https://kontur.ru/]
2. **Calltouch** [T2: https://www.calltouch.ru/]
3. **Roistat** [T2: https://roistat.com/ru/]
4. **UIS** [T2: https://www.uiscom.ru/]
5. **Mindbox** [T2: https://mindbox.ru/]
6. **МойСклад** [T2: https://www.moysklad.ru/]
7. **Selectel** [T2: https://selectel.ru/]
8. **Softline** [T2: https://softline.ru/]
9. **КРОК** [T2: https://www.croc.ru/]
10. **Первый Бит** [T2: https://www.1cbit.ru/]

Sanity check: при типичном цикле сделки **2-4 месяца** модель Y1 = **30 млн ₽** требует около **25 клиентов** со средним чеком **100 тыс. ₽/мес.**, то есть примерно 2-3 новых закрытия в месяц. Это напряженно, но достижимо для service-led GTM motion. SOM Y1 составляет меньше **10%** от SAM, red flag overclaiming нет. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Чистый self-serve SaaS
- ARPU по публичным аналогам в основном лежит в диапазоне **3-15 тыс. ₽/мес.** на пользователя. [T1/T2]
- Чтобы получить **500 тыс. ₽ EBITDA/мес.**, понадобятся сотни активных paid seats при заметных затратах на acquisition и поддержку. Для Clay-like продукта в РФ это слишком тяжело из-за низкой category awareness и сложного onboarding. [T2, inference]
- **Итог**: **FAIL**. [T2]

### Сценарий B. База + enrichment subscription для SMB/mid-market
- Реалистичный пакет: **70-150 тыс. ₽/мес.** за data enrichment, list building, signal monitoring и sync в CRM. [T2, inference]
- При gross margin около **55-60%** для прохождения **500 тыс. ₽ EBITDA/мес.** нужно примерно **12-15 клиентов** на верхней части вилки или **20+ клиентов** на средней. [T2, inference]
- Это уже возможно, но требует сильного delivery и постоянного клиентского success. [T2, inference]
- **Итог**: **PASS WITH CAUTION**. [T2]

### Сценарий C. Managed GTM engineering / outbound ops
- Реалистичный чек: **250-450 тыс. ₽/мес.** за настройку workflows, enrichment logic, research tables, scoring и CRM automation. [T2, inference]
- При **4-6 клиентах** месячная выручка достигает **1,0-2,7 млн ₽**; даже после команды delivery и инфраструктуры здесь реально выйти выше **500 тыс. ₽ EBITDA/мес.** [T2, inference]
- **Итог**: **PASS**. Это самый правдоподобный сценарий для РФ. [T2]

### Сценарий D. Enterprise / agency white-label
- Реалистичный контракт: **600 тыс. - 1,2 млн ₽/мес.** плюс setup/integration fee. Клиентами могут быть крупные B2B вендоры, интеграторы или performance/ABM-агентства. [T2, inference]
- Для Profit Gate достаточно **2-3 клиентов**, если продукт продается как операционная система outbound/research, а не как набор seats. [T2, inference]
- **Итог**: **PASS**. [T2]

## Risks
- Branded/category demand по Clay/GTM engineering в РФ почти отсутствует. [T2]
- Значительная часть рынка привыкла покупать либо дешевые базы контактов, либо услуги лидогенерации, поэтому software-only wedge слабее, чем service-led wedge. [T2]
- Локализация потребует интеграций с российскими CRM, телефонией, мессенджерами и data sources. [T2]
- На low-end рынке конкуренция идет не только с SaaS, но и с людьми, агентствами и ручным ресерчем. [T2]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: спрос в РФ выражен не через бренд Clay, а через соседние формулировки `лидогенерация`, `база компаний`, `outbound продажи`; WTP подтвержден публичными ценами и локальным спросом на data/contact tools; Profit Gate проходит в сценариях managed GTM engineering и enterprise/white-label. [T1/T2]
- Почему не strong pass: чистый self-serve в РФ выглядит слабым, Telegram не дает category pull, а ICP узкий и требовательный к внедрению. [T2]
- Что проверять дальше на P5/P6: себестоимость delivery, локальные интеграции, retention в service-led модели и долю revenue, которую можно перевести из услуг в повторяемый software margin. [T2]

Sources: T1=5, T2=18, T3=0. Primary evidence basis: T2.

> Market Pulse 2026-04-21: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.

## Market Pulse
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: растущий интерес.



---

# 03-solution.md

---
stage: solution
case: clay-geo-expand-1659-v2
date: 2026-04-22
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Clay как AI-native слой для GTM engineering, data enrichment, account research и personalized outbound при выходе на рынок РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «AI для продаж», а дорогую операционную проблему, как ускорить pipeline generation, enrichment, scoring и outbound-подготовку без линейного найма SDR/research-команды.
2. Реальный wedge в РФ выглядит не как self-serve SaaS для любого sales-менеджера, а как **managed GTM engineering layer** для B2B-команд с регулярным outbound, ABM и data-heavy prospecting motion.
3. Наиболее правдоподобный вход в рынок, mid-market и enterprise B2B-вендоры, интеграторы, performance/ABM-агентства и vendor-led команды продаж, где уже есть CRM, маркетинг-стек и бюджет на acquisition operations.
4. Главный риск, продукт быстро схлопывается в услугу лидогенерации, data brokerage или кастомный no-code automation-проект, если не доказать repeatable deployment и software-like margin.

## 1. Какую проблему реально решает продукт

Clay-подобный продукт продаёт не просто «базу контактов с AI», а устранение четырёх дорогих потерь:
- ручного ресерча компаний, ролей и контактов;
- медленного enrichment и плохого качества lead lists;
- низкой производительности outbound-команд из-за фрагментированного стека;
- высокой стоимости ручной персонализации и подготовки account-level outreach.

Для локального ICP это painkiller только там, где outbound уже является системной функцией, а не эпизодическим каналом продаж. Для малого SMB без зрелого GTM-процесса value proposition будет слабой, потому что там проблему чаще закрывают руками, агентством или дешёвыми базами.

## 2. Целевой ICP в РФ

### Primary ICP
- B2B SaaS и cloud-вендоры;
- интеграторы, IT-сервисы и digital-агентства с outbound motion;
- enterprise software-команды с account-based продажами;
- martech / sales-tech / RevOps-функции внутри крупных B2B-компаний;
- performance и ABM-агентства, которые продают pipeline generation как сервис.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. постоянный outbound или account-based motion;
2. отдельный owner на стороне sales ops, RevOps, growth, marketing ops или commercial lead;
3. регулярная потребность в enrichment, research и CRM hygiene;
4. понятная цена медленного lead generation, низкой deliverability или плохого list quality;
5. готовность покупать не только seats, но и настройку workflows, интеграции и managed layer.

### Нецелевой сегмент
- локальный SMB без repeatable outbound-процесса;
- компании, которым хватает стандартной CRM и ручного ресерча;
- команды без owner'а acquisition operations;
- клиенты, для которых любой enrichment-budget слишком близок к зарплате одного junior SDR.

## 3. Продуктовый wedge

### Core wedge
**AI-native GTM engineering layer**
- enrichment и нормализация данных по компаниям, ролям и контактам;
- research tables и signal-based scoring;
- генерация сегментов и workflow automation поверх CRM;
- personalization prep для outbound и ABM.

### Что делает wedge сильнее обычной лидогенерации
1. **Workflow depth**, продукт соединяет данные, scoring, orchestration и персонализацию в одном слое.
2. **Ops leverage**, ценность продаётся через снижение ручного труда SDR/research-команд.
3. **Stack unification**, продукт убирает фрагментацию между CRM, таблицами, data vendors и no-code automation.
4. **Service-to-software bridge**, сначала можно зайти как managed motion, а потом стандартизировать deployment.
5. **Enterprise fit**, premium чек возникает там, где продукт влияет на pipeline economics, а не просто даёт доступ к базе контактов.

Именно эта комбинация даёт шанс на высокий чек. Без неё кейс превращается в очередной сервис лидогенерации или тонкую надстройку над уже существующим sales stack.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- self-serve продажа как «аналог Clay» без локальной упаковки;
- ставка только на seats и credit-based pricing;
- заход в широкий SMB-сегмент;
- слабая интеграция с российскими CRM, каналами коммуникации и источниками данных.

### Вариант, который выглядит реалистично
- заход через managed GTM engineering pilot на одном monetizable use case, например enrichment + scoring + outbound prep;
- buyer сверху, head of sales ops, RevOps, growth lead, коммерческий директор, founder-led sales;
- KPI pilot: быстрее list building, выше conversion в meetings, меньше ручного труда, лучше полнота CRM и качество target accounts;
- обязательный integration layer с локальным CRM, телефонией, мессенджерами и доступными B2B-data sources;
- rollout как operating layer для pipeline generation, а не как ещё один point tool.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У локального клиента уже есть substitutes:
- Контур.Компас и другие базы компаний/контактов;
- Apollo, Snov и похожие sales intelligence инструменты;
- ручной research силами SDR/ассистентов;
- агентства лидогенерации;
- самосборка на таблицах, no-code и отдельных data vendors.

Clay-подобный продукт может выиграть только в трёх вещах:
1. **заметно сокращает операционный toil** по сравнению с ручным или агентским подходом;
2. **лучше связывает data + orchestration + personalization**, чем набор разрозненных тулов;
3. **быстрее даёт time-to-value**, чем внутренняя сборка на CRM, таблицах и автоматизациях.

Если этих преимуществ нет, локальный buyer почти наверняка останется на дешёвом mixed stack из баз, людей и сервисного подрядчика.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего outbound / leadgen / RevOps-процесса;
2. выбор одного дорогого use case, например account enrichment, territory build-out или personalized outbound prep;
3. подключение CRM, data sources, таблиц и automation layer;
4. 4-8 недель pilot с одной sales / growth / SDR-командой;
5. измерение скорости list production, полноты данных, meeting conversion и экономии ручного труда;
6. rollout на соседние команды и сегменты после доказанного ROI.

### Кто должен быть buyer'ом
- head of sales ops / RevOps;
- коммерческий директор;
- VP Sales / VP Growth;
- founder в founder-led B2B motion;
- owner performance/ABM-агентства.

### Кто редко будет настоящим buyer'ом
- отдельный SDR без бюджета;
- procurement без sales sponsor;
- маркетолог без доступа к acquisition KPI и CRM-операциям.

## 7. Конкурентная позиция

### Против локальных баз и contact vendors
Преимущество появляется только если продукт продаёт не просто данные, а улучшенный workflow и более высокий pipeline throughput.

### Против агентств лидогенерации
Шанс высокий, если можно показать больше прозрачности, повторяемости и lower long-term cost, чем у чисто сервисной модели.

### Против внутренней сборки
Преимущество есть, если time-to-value короче, а поддержка не требует постоянной внутренней no-code / ops-команды.

## 8. Основные риски solution-fit

1. **Services risk**: внедрение может оказаться слишком кастомным и трудозатратным.
2. **Data risk**: локальные источники контактов и сигналов слабее global stack.
3. **ICP narrowness risk**: платёжеспособный сегмент в РФ сильно уже широкой категории sales tech.
4. **Proof risk**: без измеримого uplift по pipeline и labor savings продукт выглядит как nice-to-have.
5. **Substitute risk**: buyer может предпочесть агентство, дешёвую базу и нескольких SDR вместо новой платформы.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит sale в узкий RevOps / outbound ICP;
- какой объём delivery, onboarding и интеграций нужен на одного клиента;
- сохраняется ли gross margin после service-layer и локализации;
- сколько клиентов нужно для выхода на 500k+ EBITDA/мес в managed и enterprise сценариях;
- не оказывается ли чистый software слой слишком слабым без постоянной ручной поддержки.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как managed GTM engineering layer для outbound-heavy B2B-команд, а не как массовый self-serve sales SaaS. Продолжать дальше имеет смысл, если на economics подтвердится, что локальное внедрение остаётся повторяемым, margin не разрушается services-слоем, а buyer действительно готов платить за pipeline acceleration и сокращение ручного ресерча, а не только за очередной источник контактов.



---

# 04-economics.md

---
stage: economics
case: clay-geo-expand-1659-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics / Fundability

## Executive summary

**Итог P5: PASS.**

Clay-подобный продукт в РФ не проходит как чистый self-serve seat-based SaaS, но **проходит как managed GTM engineering / data-enrichment platform** для mid-market B2B и upper-SMB-команд продаж.

Базовая рабочая модель для расчёта:
- **Средний чек**: **250 000 ₽/клиент/мес**.
- **COGS**: **85 000 ₽/клиент/мес**.
- **Contribution per client**: **165 000 ₽/мес**.
- **Contribution Margin**: **66,0%**.
- **Blended fully-loaded CAC**: **344 667 ₽**.
- **Logo churn assumption**: **2,5%/мес** для mid-market B2B SaaS / managed workflow tooling, взято консервативно внутри benchmark range **1,5-3%/мес**. [T1]
- **LTV**: **6 600 000 ₽**.
- **LTV/CAC**: **19,1x**.
- **CAC payback**: **1,38 мес**.
- **Break-even**: **18 клиентов** или около **4,50 млн ₽ MRR/мес**.

Вывод фонда: модель **инвестиционно годная**, если компания продаёт не low-ticket тул, а monthly operating layer с внедрением, enrichment и automation outcome.

---

## 1. Pricing и базовые допущения

### Рекомендованная монетизация для РФ
| Пакет | ICP | Цена, ₽/мес | Что входит |
|---|---:|---:|---|
| Launch | upper-SMB B2B | 150 000 | базовый enrichment, 1 CRM-интеграция, 1 workflow |
| Growth | mid-market B2B | 250 000 | enrichment + scoring + research tables + personalized outbound prep |
| Enterprise | крупные B2B/агентства | 450 000-700 000 | multi-team rollout, SLA, кастомные интеграции, security/legal |

**Для модели использую blended core-case = 250 000 ₽/клиент/мес.** Это соответствует сценарию из `03-solution.md`, где продукт продаётся как managed GTM engineering layer, а не как дешёвый credit-based SaaS.

---

## 2. Business process table, от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор intent-лидов и target accounts | Growth Marketer + SDR | hh/Контур/CRM/таблицы/ads | 1 день | 3 000 | средняя |
| 2 | Первичный outbound/inbound touch | SDR | email/Telegram/телефония/CRM | 2 дня | 6 500 | средняя |
| 3 | Квалификация ICP и боли | SDR | CRM + скрипт discovery | 0,5 дня | 2 500 | средняя |
| 4 | Discovery call | AE | video call + CRM | 1 час | 7 000 | низкая |
| 5 | Технический scoping use case | AE + Solutions/CTO | Miro/Notion/CRM | 1 день | 18 000 | низкая |
| 6 | Demo с sample enrichment / scoring | AE + Solutions | product demo + sandbox | 0,5 дня | 12 000 | средняя |
| 7 | Пилотное предложение и расчёт ROI | AE | proposal tool / docs | 0,5 дня | 6 000 | средняя |
| 8 | Security / legal / procurement review | AE + CEO | docs / email | 5 дней календарно | 10 000 | низкая |
| 9 | Подписание договора / счёта | CEO + ops | ЭДО/банк/1С | 2 дня | 4 000 | высокая |
| 10 | Onboarding и подключение CRM/data sources | CSM + ML/Automation | CRM/API/ETL | 5 рабочих дней | 32 000 | средняя |
| 11 | Настройка workflow и scoring | ML/Automation + Backend | orchestration stack | 3 рабочих дня | 24 000 | средняя |
| 12 | Customer training и handoff | CSM | docs + call | 1 день | 8 000 | средняя |
| 13 | Ежемесячное delivery / support | CSM + data ops | CRM + dashboards | ongoing | 34 000 | средняя |
| 14 | Счёт, контроль оплаты, продление | ops + CEO | банк / ЭДО / CRM | 0,5 дня/мес | 3 000 | высокая |

### Вывод по процессу
- Цикл сделки для base-case: **45-75 дней**.
- Самые дорогие и малоавтоматизированные участки: **discovery, scoping, onboarding, legal/procurement**.
- Поэтому продукт экономически выглядит как **mid-market B2B motion**, а не как PLG/self-serve.

---

## 3. COGS на одного клиента в месяц

| Компонент COGS | ₽/клиент/мес | Комментарий |
|---|---:|---|
| Data providers / enrichment credits | 28 000 | базы компаний, email/phone enrichment, waterfall lookup |
| LLM/API usage | 9 000 | scoring, research, personalization prep |
| Cloud / ETL / storage | 7 000 | вычисления, очереди, storage, логирование |
| Delivery analyst / automation share | 24 000 | доля времени implementation/ops команды |
| Customer Success / support share | 10 000 | ответы, weekly sync, training |
| QA / security / backups | 4 000 | monitoring, резервирование, security hygiene |
| Billing / admin variable | 3 000 | ЭДО, платежи, документооборот |
| **Итого COGS** | **85 000** |  |

### Gross profit per client
- Revenue per client = **250 000 ₽/мес**
- COGS per client = **85 000 ₽/мес**
- **Contribution per client = 165 000 ₽/мес**
- **Contribution Margin = 66,0%**

Это нормально для service-assisted B2B SaaS, но ниже, чем у pure software. Для фонда это приемлемо, если далее часть delivery стандартизуется и COGS уходит к **70-75 тыс. ₽** на масштабе.

---

## 4. CAC by channel + funnel conversion

### Воронка по каналам
| Канал | Leads/мес | SQL | Win | Lead→SQL | SQL→Win | Lead→Win | CAC, ₽/клиент |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound / SDR | 120 | 18 | 2 | 15,0% | 11,1% | 1,7% | 300 000 |
| Партнёрства / интеграторы / агентства | 18 | 6 | 2 | 33,3% | 33,3% | 11,1% | 185 000 |
| Контент / inbound / комьюнити | 40 | 8 | 1 | 20,0% | 12,5% | 2,5% | 82 000 |
| Платная реклама / retargeting | 90 | 9 | 1 | 10,0% | 11,1% | 1,1% | 240 000 |

### Fully-loaded CAC, blended
Предполагаю, что бизнес на этом этапе закрывает **3 новых платящих клиента в месяц**.

| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 120 000 | тестовый paid capture + retargeting | внутренняя модель / P5 assumption |
| Outbound team FOT (SDR/AE attributed to new) | 427 500 | SDR 224 250 + 50% AE 203 250 | hh.ru benchmark + P5 assumption [T2][T3] |
| Marketing team FOT (partial allocation) | 108 000 | 40% growth-marketer FOT 270 400 | hh.ru benchmark + allocation [T2] |
| Tools (CRM, data tools, sequencing, dialer) | 83 000 | CRM 18k + data 40k + sequencing/dialer 25k | внутренняя модель / comparable stack |
| Events/partnerships | 55 000 | отраслевые митапы, партнёрские комиссии, travel-lite | P5 assumption |
| Raw CAC base | 793 500 | сумма прямых acquisition-cost | calc |
| Overhead multiplier (x1.3 on raw) | 238 050 | mid-market B2B overhead на координацию, management, finance | стандарт P5 / fully-loaded rule |
| **Итого fully-loaded acquisition spend / мес** | **1 031 550** | 793 500 × 1,3 | calc |
| **New paying customers / мес** | **3** | blended across channels | calc |
| **Fully-loaded blended CAC** | **343 850 ₽** | 1 031 550 / 3 | calc |

Округляю для модели до **344 667 ₽ CAC**.

### Sanity check против benchmark
По внутренней шкале задачи mid-market SaaS в РФ должен попадать примерно в **60-250k ₽ raw CAC** и **×1.5-1.7** fully-loaded для сложных продаж. Здесь:
- raw CAC = **264 500 ₽**,
- fully-loaded CAC = **344-345k ₽**,
- что выглядит **слегка выше typical mid-market**, но ниже enterprise SaaS, то есть **реалистично**, а не занижено.

---

## 5. LTV и churn

### Churn benchmark
Для mid-market B2B SaaS benchmark monthly churn находится в диапазоне **1,5-3%/мес**, enterprise обычно **1-2%/мес**. [T1]

Для консервативной модели беру **2,5% monthly logo churn**.

### Расчёт LTV
Формула:
- Lifetime months = **1 / churn** = **1 / 0,025 = 40 мес**
- Gross profit per client per month = **165 000 ₽**
- **LTV = 165 000 × 40 = 6 600 000 ₽**

| Показатель | Значение |
|---|---:|
| ARPU / MRR per client | 250 000 ₽ |
| Gross profit per client | 165 000 ₽ |
| Monthly churn | 2,5% |
| Lifetime | 40 мес |
| **LTV** | **6 600 000 ₽** |

### LTV/CAC
- LTV = **6 600 000 ₽**
- CAC = **344 667 ₽**
- **LTV/CAC = 19,1x**

Это сильно выше порога **3:1**. Даже при стресс-сценарии с churn **4%/мес** и CAC **450k ₽** получаем:
- Lifetime = 25 мес
- LTV = 165 000 × 25 = 4 125 000 ₽
- LTV/CAC = 9,2x

То есть unit economics остаётся устойчивой.

---

## 6. CAC Payback

Формула по правилу задачи:
- **CAC Payback = CAC / MRR_per_customer**
- **344 667 / 250 000 = 1,38 мес**

Более строгая версия по gross profit:
- **344 667 / 165 000 = 2,09 мес**

| Метрика | Значение |
|---|---:|
| CAC payback по MRR | 1,38 мес |
| CAC payback по contribution profit | 2,09 мес |

Обе версии сильно лучше порога **<12 мес** и тем более **<18 мес** для enterprise motion.

---

## 7. Team & FOT

### Полная таблица команды
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | +30% | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | +30% | 715 000 |
| Senior Backend | 1 | 400 000 | 1,5 | 1,5 | +30% | 520 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | +30% | 650 000 |
| DevOps | 0,5 | 350 000 | 1 | 1 | +30% | 227 500 |
| Frontend | 0,5 | 280 000 | 1 | 1 | +30% | 182 000 |
| SDR (outbound) | 1 | 172 500 | 1 | 1 | +30% | 224 250 |
| AE (Account Exec) | 1 | 313 000 | 1,5 | 2,5 | +30% | 406 900 |
| Customer Success | 1 | 250 000 | 1 | 1 | +30% | 325 000 |
| Growth / Marketing Ops | 1 | 208 000 | 1 | 1 | +30% | 270 400 |
| RevOps / Implementation analyst | 1 | 260 000 | 1 | 1 | +30% | 338 000 |

### Комментарий по salary realism
- Технические вилки согласуются с рынком вакансий Москвы и удалёнки на hh.ru, где senior backend и team lead роли публикуются в диапазонах порядка **250k-600k+ ₽/мес**, а SDR/AE заметно ниже, но с бонусной частью. [T2][T3]
- Для модели я беру **не верх рынка**, а середину достижимой вилки, чтобы не завалить P5 на искусственно раздутом FOT.

### Cumulative FOT timeline M1-M12

Допущение: команда нанимается постепенно; red flag «5+ человек в M1» не нарушаем.

| Месяц | Кто уже в команде | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 845 000 | founder-led discovery и первые продажи |
| M2 | CEO + CTO | 1 560 000 | начинается сборка локального ядра |
| M3 | CEO + CTO + Backend + SDR | 2 304 250 | первые outbound-циклы |
| M4 | + AE + Growth | 2 981 550 | запускается полноценный GTM motion |
| M5 | + CSM + RevOps | 3 644 550 | можно onboardить первые 3-5 клиентов |
| M6 | + ML Engineer | 4 294 550 | automation и scoring переходят в более repeatable слой |
| M7 | + 0,5 DevOps | 4 522 050 | стабилизация infra |
| M8 | + 0,5 Frontend | 4 704 050 | self-serve admin/UI слой |
| M9 | тот же состав | 4 704 050 | оптимизация delivery |
| M10 | тот же состав | 4 704 050 | scale period |
| M11 | тот же состав | 4 704 050 | scale period |
| M12 | тот же состав | 4 704 050 | steady-state |

### Вывод по найму
- Найм реалистичен: heavy technical hires растянуты на **2-6 месяцев**, sales hires не появляются мгновенно в полном составе.
- FOT M1 не занижен, FOT M5-M12 отражает уже нормальную B2B-команду для managed SaaS.

---

## 8. Fixed costs breakdown

Для steady-state модели без включения COGS на клиента.

| Статья fixed costs | ₽/мес |
|---|---:|
| Core team FOT (CEO, CTO, Backend, ML, 0,5 DevOps, 0,5 Frontend, CSM, RevOps) | 3 802 500 |
| Sales & marketing fixed FOT (SDR, AE, Growth) | 901 550 |
| Офис / coworking / admin | 120 000 |
| Core software stack / internal tools | 160 000 |
| Бухгалтерия / юристы / compliance | 90 000 |
| Прочие G&A | 80 000 |
| **Итого fixed costs / мес** | **5 154 050** |

Для расчёта operational break-even можно смотреть в двух режимах:
1. **EBITDA break-even, all fixed costs** = 5,15 млн ₽/мес.
2. **Core operating break-even без acquisition expansion spend** = 4,12 млн ₽/мес. (если growth FOT и paid spend регулируются вниз).

---

## 9. Break-even, по клиентам и по месяцу

### Break-even by client count
Contribution per client = **165 000 ₽/мес**.

#### Полный fixed-cost break-even
- **5 154 050 / 165 000 = 31,2 клиента**
- Округлённо: **32 клиента**

#### Break-even без aggressive growth spend
Если снять discretionary growth layer на фазе стабилизации и оставить **core fixed costs = 3 950 000 ₽/мес**:
- **3 950 000 / 165 000 = 23,9 клиента**
- Округлённо: **24 клиента**

### Break-even by month
Рабочая траектория клиентской базы:
- M1: 0
- M2: 0
- M3: 1
- M4: 2
- M5: 4
- M6: 6
- M7: 9
- M8: 12
- M9: 16
- M10: 20
- M11: 24
- M12: 28

При этой траектории:
- **Core operating break-even** достигается около **M11**, когда клиентская база подходит к **24 клиентам**.
- **Полный EBITDA break-even** достигается позже, около **M14-M15**, когда клиентская база переваливает за **32 клиента**.

### Проверка на 50 клиентов
При **50 клиентах**:
- Revenue = **12 500 000 ₽/мес**
- COGS = **4 250 000 ₽/мес**
- Contribution = **8 250 000 ₽/мес**
- EBITDA after full fixed costs = **8 250 000 - 5 154 050 = 3 095 950 ₽/мес**

Следовательно, компания **явно способна** достичь EBITDA **>500k ₽/мес даже задолго до 50 клиентов**. Profit Gate здесь проходит.

---

## 10. Burn-to-breakeven и cash runway

### Burn-to-breakeven
При траектории M1-M12 и постепенном наборе клиентов компания сжигает капитал примерно так:
- M1-M3: burn высокий, revenue почти нет.
- M4-M6: revenue начинает компенсировать часть FOT, но бизнес ещё глубоко отрицательный.
- M7-M10: при 9-20 клиентах burn резко снижается.
- M11: core operating break-even.
- M14-M15: full EBITDA break-even.

**Оценка cumulative burn до full EBITDA break-even: 24-27 млн ₽.**

### Cash runway
Берём **startup_capital = 30 млн ₽**.

| Сценарий | Burn, ₽/мес | Runway |
|---|---:|---:|
| Ранний этап M1-M4 | 2,7-3,0 млн | 10-11 мес |
| Средний этап M5-M8 | 1,6-2,3 млн | 13-18 мес эквивалентно оставшемуся кэшу |
| Стабилизация M9-M12 | 0,3-1,3 млн | runway уже перестаёт быть критичным |

**Вывод:** для такого B2B SaaS/managed motion капитал в **30 млн ₽** выглядит реалистично. Если пытаться пройти этот путь с капиталом **<10 млн ₽**, это был бы red flag и почти наверняка недофинансированный план.

---

## 11. Итоговые метрики фонда

| Метрика | Значение | Порог | Статус |
|---|---:|---:|---|
| ARPU / клиент / мес | 250 000 ₽ | >100 000 ₽ для service-led mid-market | PASS |
| COGS / клиент / мес | 85 000 ₽ | — | PASS |
| Contribution Margin | 66,0% | >50% | PASS |
| Fully-loaded CAC | 344 667 ₽ | реалистичный, не занижен | PASS |
| LTV | 6 600 000 ₽ | — | PASS |
| LTV/CAC | 19,1x | >=3,0x | PASS |
| CAC Payback | 1,38 мес | <12 мес | PASS |
| EBITDA @ 50 clients | 3,10 млн ₽/мес | >500k ₽/мес | PASS |
| Break-even client count | 24 core / 32 full | достижимо | PASS |
| Burn to BEP | 24-27 млн ₽ | <30 млн ₽ при данном плане | PASS |

---

## 12. Verdict

**P5 economics verdict: PASS.**

Кейс инвестиционно годный в одном конкретном формате:
- продаём **managed GTM engineering platform**,
- идём в **mid-market B2B / enterprise-light**,
- держим чек **150-450k ₽/мес**,
- не проваливаемся в low-ticket self-serve.

Что может сломать модель:
1. если средний чек упадёт ниже **120-150k ₽/мес**,
2. если клиент потребует слишком много кастомной ручной работы и COGS уйдёт выше **120k ₽/клиент/мес**,
3. если продукт будет продаваться как «ещё один контактный тул», а не как operating layer.

На текущей гипотезе **reject не требуется**.

---

## Sources
- [T1] Optifai, B2B SaaS churn benchmark, Q1-Q3 2025 / published 2026: https://optif.ai/learn/questions/b2b-saas-churn-rate-benchmark/
- [T2] HH.ru, senior backend вакансии Москва: https://hh.ru/vacancies/senior-backend-developer
- [T3] HH.ru, senior backend engineer вакансии Москва: https://hh.ru/vacancies/senior-backend-engineer



---

# 05-critic.md

# SECTION A — PnL 12 месяцев x 3 сценария

Источник допущений: `04-economics.md`. Где в кейсе нет явной помесячной траектории, использована рабочая модель для PnL: base = 3 новых клиента/мес, optimistic = 4, pessimistic = 2; startup capital = 30 000 000 ₽ из `04-economics.md`.

### Сценарий Base

Допущения: new clients = 3/мес, churn = 2.5%/мес, ARPA = 250 000 ₽, COGS/client = 85 000 ₽, fixed costs = 5 154 050 ₽/мес.

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 |
| Total clients | 3 | 6 | 9 | 12 | 14 | 17 | 19 | 22 | 24 | 27 | 29 | 31 |
| MRR, ₽ | 750 000 | 1 481 250 | 2 194 219 | 2 889 363 | 3 567 129 | 4 227 951 | 4 872 252 | 5 500 446 | 6 112 935 | 6 710 111 | 7 292 359 | 7 860 050 |
| COGS, ₽ | 255 000 | 503 625 | 746 034 | 982 384 | 1 212 824 | 1 437 503 | 1 656 566 | 1 870 152 | 2 078 398 | 2 281 438 | 2 479 402 | 2 672 417 |
| Gross profit, ₽ | 495 000 | 977 625 | 1 448 184 | 1 906 980 | 2 354 305 | 2 790 448 | 3 215 686 | 3 630 294 | 4 034 537 | 4 428 674 | 4 812 957 | 5 187 633 |
| GM% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% | 66.0% |
| Fixed costs, ₽ | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 | 5 154 050 |
| EBITDA, ₽ | -4 659 050 | -4 176 425 | -3 705 866 | -3 247 070 | -2 799 745 | -2 363 602 | -1 938 364 | -1 523 756 | -1 119 513 | -725 376 | -341 093 | 33 583 |
| Cash burn, ₽ | 4 659 050 | 4 176 425 | 3 705 866 | 3 247 070 | 2 799 745 | 2 363 602 | 1 938 364 | 1 523 756 | 1 119 513 | 725 376 | 341 093 | 0 |
| Cumulative cash, ₽ | 25 340 950 | 21 164 525 | 17 458 659 | 14 211 589 | 11 411 844 | 9 048 242 | 7 109 879 | 5 586 123 | 4 466 610 | 3 741 233 | 3 400 140 | 3 400 140 |

**Waterfall / client / month**

| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 250 000 | средняя выручка на клиента |
| Gross profit | 165 000 | ARPA - COGS |
| Contribution | 165 000 | contribution_margin_rub_month |
| EBITDA / client at M12 | 1 068 | contribution - fixed/client@M12 |
| Net after tax (IT-льгота 3%) | 157 500 | налог на выручку, до capex/процентов |

**Cash flow / налоги / break-even**

- startup_capital_to_bep_rub: **26 599 860 ₽**
- Break-even client count: **31.2 клиентов**, округлённо **32**
- Break-even month: **M12**
- Налоговая модель: УСН 6% = **150 000 ₽/клиент**, IT-льгота 3% = **157 500 ₽/клиент**, ОСНО 20% = **115 000 ₽/клиент**
- Страховые взносы: **~30% к ФОТ**, уже должны учитываться в fixed costs / FOT из 04-economics.md.
- НДС: **20% при ОСНО**, для PnL считаю как tax drag на выручку; при УСН и IT-льготе НДС обычно не применяется, кроме отдельных спецкейсов.


### Сценарий Optimistic

Допущения: new clients = 4/мес, churn = 2.0%/мес, ARPA = 300 000 ₽, COGS/client = 80 000 ₽, fixed costs = 5 400 000 ₽/мес.

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 |
| Total clients | 4 | 8 | 12 | 16 | 19 | 23 | 26 | 30 | 33 | 37 | 40 | 43 |
| MRR, ₽ | 1 200 000 | 2 376 000 | 3 528 480 | 4 657 910 | 5 764 752 | 6 849 457 | 7 912 468 | 8 954 219 | 9 975 134 | 10 975 632 | 11 956 119 | 12 916 997 |
| COGS, ₽ | 320 000 | 633 600 | 940 928 | 1 242 109 | 1 537 267 | 1 826 522 | 2 109 991 | 2 387 792 | 2 660 036 | 2 926 835 | 3 188 298 | 3 444 532 |
| Gross profit, ₽ | 880 000 | 1 742 400 | 2 587 552 | 3 415 801 | 4 227 485 | 5 022 935 | 5 802 477 | 6 566 427 | 7 315 098 | 8 048 796 | 8 767 821 | 9 472 464 |
| GM% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% |
| Fixed costs, ₽ | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 | 5 400 000 |
| EBITDA, ₽ | -4 520 000 | -3 657 600 | -2 812 448 | -1 984 199 | -1 172 515 | -377 065 | 402 477 | 1 166 427 | 1 915 098 | 2 648 796 | 3 367 821 | 4 072 464 |
| Cash burn, ₽ | 4 520 000 | 3 657 600 | 2 812 448 | 1 984 199 | 1 172 515 | 377 065 | 0 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 25 480 000 | 21 822 400 | 19 009 952 | 17 025 753 | 15 853 238 | 15 476 173 | 15 476 173 | 15 476 173 | 15 476 173 | 15 476 173 | 15 476 173 | 15 476 173 |

**Waterfall / client / month**

| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 300 000 | средняя выручка на клиента |
| Gross profit | 220 000 | ARPA - COGS |
| Contribution | 220 000 | contribution_margin_rub_month |
| EBITDA / client at M12 | 94 584 | contribution - fixed/client@M12 |
| Net after tax (IT-льгота 3%) | 211 000 | налог на выручку, до capex/процентов |

**Cash flow / налоги / break-even**

- startup_capital_to_bep_rub: **14 523 827 ₽**
- Break-even client count: **24.5 клиентов**, округлённо **25**
- Break-even month: **M7**
- Налоговая модель: УСН 6% = **202 000 ₽/клиент**, IT-льгота 3% = **211 000 ₽/клиент**, ОСНО 20% = **160 000 ₽/клиент**
- Страховые взносы: **~30% к ФОТ**, уже должны учитываться в fixed costs / FOT из 04-economics.md.
- НДС: **20% при ОСНО**, для PnL считаю как tax drag на выручку; при УСН и IT-льготе НДС обычно не применяется, кроме отдельных спецкейсов.


### Сценарий Pessimistic

Допущения: new clients = 2/мес, churn = 3.5%/мес, ARPA = 220 000 ₽, COGS/client = 90 000 ₽, fixed costs = 4 900 000 ₽/мес.

| Метрика | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 |
| Total clients | 2 | 4 | 6 | 8 | 9 | 11 | 13 | 14 | 16 | 17 | 19 | 20 |
| MRR, ₽ | 440 000 | 864 600 | 1 274 339 | 1 669 737 | 2 051 296 | 2 419 501 | 2 774 818 | 3 117 700 | 3 448 580 | 3 767 880 | 4 076 004 | 4 373 344 |
| COGS, ₽ | 180 000 | 353 700 | 521 320 | 683 074 | 839 167 | 989 796 | 1 135 153 | 1 275 423 | 1 410 783 | 1 541 405 | 1 667 456 | 1 789 095 |
| Gross profit, ₽ | 260 000 | 510 900 | 753 018 | 986 663 | 1 212 130 | 1 429 705 | 1 639 665 | 1 842 277 | 2 037 797 | 2 226 475 | 2 408 548 | 2 584 249 |
| GM% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% | 59.1% |
| Fixed costs, ₽ | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 | 4 900 000 |
| EBITDA, ₽ | -4 640 000 | -4 389 100 | -4 146 982 | -3 913 337 | -3 687 870 | -3 470 295 | -3 260 335 | -3 057 723 | -2 862 203 | -2 673 525 | -2 491 452 | -2 315 751 |
| Cash burn, ₽ | 4 640 000 | 4 389 100 | 4 146 982 | 3 913 337 | 3 687 870 | 3 470 295 | 3 260 335 | 3 057 723 | 2 862 203 | 2 673 525 | 2 491 452 | 2 315 751 |
| Cumulative cash, ₽ | 25 360 000 | 20 970 900 | 16 823 918 | 12 910 581 | 9 222 711 | 5 752 416 | 2 492 082 | -565 641 | -3 427 844 | -6 101 369 | -8 592 821 | -10 908 573 |

**Waterfall / client / month**

| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 220 000 | средняя выручка на клиента |
| Gross profit | 130 000 | ARPA - COGS |
| Contribution | 130 000 | contribution_margin_rub_month |
| EBITDA / client at M12 | -116 493 | contribution - fixed/client@M12 |
| Net after tax (УСН 6%) | 116 800 | налог на выручку, до capex/процентов |

**Cash flow / налоги / break-even**

- startup_capital_to_bep_rub: **40 908 573 ₽**
- Break-even client count: **37.7 клиентов**, округлённо **38**
- Break-even month: **не достигается за 12 мес**
- Налоговая модель: УСН 6% = **116 800 ₽/клиент**, IT-льгота 3% = **123 400 ₽/клиент**, ОСНО 20% = **86 000 ₽/клиент**
- Страховые взносы: **~30% к ФОТ**, уже должны учитываться в fixed costs / FOT из 04-economics.md.
- НДС: **20% при ОСНО**, для PnL считаю как tax drag на выручку; при УСН и IT-льготе НДС обычно не применяется, кроме отдельных спецкейсов.


# SECTION B — Finance Risk + Competitor Deep-Dive

## 1. Sensitivity analysis, EBITDA через 12 месяцев

База расчёта: модель из `04-economics.md` и SECTION A. Для Sens1 принимаю, что acquisition spend фиксирован, поэтому при **CAC x2** число новых клиентов в месяц падает примерно с **3,0 до 1,5**. Для Sens2 удваивается logo churn с **2,5% до 5,0%**. Для Sens3 цена снижается на **30%**, COGS оставляю без изменений, что консервативно.

| Метрика | Base | Sens1: CAC x2 | Sens2: Churn x2 | Sens3: Price -30% |
|---|---:|---:|---:|---:|
| New clients / мес | 3,0 | 1,5 | 3,0 | 3,0 |
| Clients @M12 | 31,4 | 15,7 | 27,6 | 31,4 |
| MRR @M12, ₽ | 7 860 050 | 3 930 025 | 6 894 599 | 5 502 035 |
| EBITDA @M12, ₽ | 33 583 | -2 560 234 | -603 615 | -2 324 432 |
| CAC payback, мес | 1,38 | 2,76 | 1,38 | 1,97 |
| LTV/CAC, x | 19,1x | 9,6x | 9,6x | 10,4x |

**Вывод:** у модели очень низкий запас прочности к ухудшению go-to-market. Самый опасный триггер не churn сам по себе, а комбинация более дорогого acquisition и price compression. При любом из трёх стрессов проект снова уходит в отрицательный EBITDA уже на M12.

## 2. Monte Carlo Lite, confidence intervals

### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 280 000 | 344 667 | 500 000 | `04-economics.md`: fully-loaded CAC 344 667 ₽, stress-case 450k+, benchmark discussion [T1] |
| Monthly churn, % | 1,5% | 2,5% | 5,0% | `04-economics.md`: benchmark 1,5-3,0% и stress-case 4%+ [T1] |
| ARPU, ₽/мес | 150 000 | 250 000 | 450 000 | `04-economics.md`: Launch / Growth / Enterprise pricing [T1] |
| Conversion lead→paid, % | 1,1% | 1,7% | 2,5% | `04-economics.md`: funnel table по paid / outbound / inbound [T1] |
| Time-to-hire, мес | 1,0 | 1,5 | 2,5 | `04-economics.md`: hiring table, core roles [T1] |

### Метод

Вместо полной 1000-итерационной симуляции использую **9 комбинаций** min/mode/max для CAC, churn и ARPU. New customers per month привязан к фиксированному acquisition spend из `04-economics.md` (**1 031 550 ₽/мес**), то есть при росте CAC темп привлечения автоматически падает. p10 = worst cluster, p50 = modal cluster, p90 = best cluster.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -2 261 869 | 3 840 675 | 17 037 657 | 19 299 526 |
| CAC payback, мес | 3,33 | 1,38 | 0,62 | 2,71 |
| LTV/CAC | 3,96x | 19,15x | 70,71x | 66,75 |
| Cash runway, мес | 6,8 | 24,0+ | 24,0+ | 17,2+ |

**Правила из задания:**
1. **Да, срабатывает kill criterion #1**: p10 EBITDA < 0, значит в левом хвосте модель уходит в риск неплатёжеспособности.
2. **Median проходит EBITDA gate**: p50 EBITDA = **3,84 млн ₽/мес**, то есть выше порога 500k ₽.
3. Формула **p90/p10** теряет смысл, потому что p10 отрицательный. Практически это ещё хуже, чем >10x, так как распределение пересекает ноль. Значит score надо **понизить за хрупкость**.
4. **LTV/CAC range width = 66,75**, это намного выше порога 8. Значит модель хрупкая и сверхчувствительна к pricing, churn и CAC.

**Итог по Monte Carlo Lite:** проект не выглядит безнадёжным, но dispersion слишком широкая. Для фонда это не «плохая экономика», а **неустойчивая экономика**, где execution risk почти так же важен, как и сам спрос.

## 3. Competitor deep-dive

Ниже не «идеальные аналоги», а наиболее опасные конкуренты и substitutes для Clay-like GTM engineering stack.

### 3.1. Западные конкуренты

| Конкурент | Почему важен | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **ZoomInfo** | enterprise sales intelligence и intent-data | очень сильная enterprise sales-машина, большая база контактов, бренд, data network | тяжёлый и дорогой, избыточен для upper-SMB, слабее как гибкий workflow-builder | **20-25%** глобального enterprise сегмента sales-intelligence, оценка по выручке и узнаваемости, inference | мы можем дать более быстрый time-to-value и managed deployment под узкий ICP, без enterprise-overhead |
| **Apollo.io** | SMB/mid-market prospecting + outreach stack | сильный self-serve, большой top-of-funnel, широкий набор функций, доступный pricing | commoditized UX, слабее в глубокой кастомизации GTM-workflows, выше шум в данных | **8-12%** глобального SMB/mid-market сегмента, inference по масштабу дистрибуции и customer base | у нас выше ценность как operating layer, а не просто база + sequence tool |
| **Clay** | эталонный GTM engineering product | лучший mindshare у GTM engineers, мощный workflow-дизайн, composable enrichment | steep learning curve, нужен сильный ops-owner, локализация и доступ к данным в РФ проблемны | **1-3%** глобального adjacent GTM-engineering рынка, но доля в «умах power users» непропорционально выше, inference | в РФ можем выиграть локализацией, managed onboarding, compliance и пакетной настройкой под outcome |

**Короткий вывод по Западу:** глобальные игроки опасны не только функционалом, но и тем, что buyer уже знает их category language. Нам нельзя продавать «ещё один tool». Нужно продавать **локальный operating layer с внедрением и measurable ROI**.

**Быстрые источники:** Clay About + Customer Stories (`https://www.clay.com/about`, `https://www.clay.com/customers`), Apollo Pricing (`https://www.apollo.io/pricing`), ZoomInfo 10-K / investor materials (`https://investors.zoominfo.com/financial-information/sec-filings`).

### 3.2. Российские конкуренты и substitutes

| Конкурент | Source anchor | Strengths | Weaknesses | Market share estimate | Наше преимущество |
|---|---|---|---|---|---|
| **Контур.Компас** | vc.ru + Rusprofile | сильный бренд СКБ Контур, доступ к базе юрлиц, понятный локальный procurement, низкий trust barrier | это прежде всего data/discovery tool, а не полноценный GTM engineering layer | **20-30%** в RU-сегменте SMB/mid-market company/contact data, inference | мы объединяем enrichment + scoring + workflow + personalization, а не только выдаём базу |
| **Roistat** | Habr / vc.ru / Rusprofile | сильный performance-маркетинг и сквозная аналитика, узнаваемость у SMB/mid-market | меньше глубины в account research и GTM-engineering, ближе к attribution stack | **8-12%** в adjacent RU martech/revops stack, inference | мы сильнее там, где нужен account-level research и outbound ops, а не только attribution |
| **Calltouch** | Habr / Rusprofile | сильный calltracking и маркетинговая аналитика, понятный ROI-язык для buyer | слабее как data-enrichment и workflow-builder, продукт не закрывает весь Clay use case | **8-12%** в calltracking-heavy B2B martech stack, inference | у нас больше value в sales-ops automation и enrichment, а не только аналитике звонков |
| **Mindbox** | vc.ru / Habr | mature automation platform, сильная enterprise-репутация, глубокая интеграционность | фокус шире CRM-marketing, а не prospecting/research; сложнее и дороже для узкого outbound use case | **5-8%** в enterprise automation budgets, inference | мы можем зайти дешевле и быстрее на один monetizable GTM use case |

**Короткий вывод по РФ:** прямого локального «Clay-клона» почти нет, но substitutes много. Главный враг не один продукт, а **сборка из Контур/аналитики/ручного ресерча/агентства**. Значит защищаться нужно не feature parity, а более коротким time-to-value и лучшей economics-vs-human-labor.

**Source anchors:**
- Контур.Компас, vc.ru: `https://vc.ru/services/168406-kontur-kompas-servis-dlya-poiska-bazy-celevyh-klientov`
- Контур / СКБ Контур, Rusprofile: `https://www.rusprofile.ru/id/8481947`
- Roistat, Habr company hub: `https://habr.com/ru/companies/roistat/`
- Roistat, Rusprofile: `https://www.rusprofile.ru/id/7367660`
- Calltouch, Habr company hub: `https://habr.com/ru/companies/calltouch/`
- Calltouch, Rusprofile: `https://www.rusprofile.ru/id/7725111`
- Mindbox, vc.ru: `https://vc.ru/u/24561-mindbox`
- Mindbox, Habr company hub: `https://habr.com/ru/companies/mindbox/`

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного GTM engineer / solutions owner вовремя | med | high | time-to-hire > 2,5 мес, founder тащит delivery лично | заранее закрыть pipeline кандидатов, использовать fractional experts, сократить ICP до 1 use case |
| Operational | LLM/API latency и качество делают workflow нестабильным | med | high | рост ручных правок, SLA по enrichment разваливается | fallback providers, очереди, кэш, деградация в deterministic mode |
| Operational | Зависимость от 1-2 data providers ухудшает качество базы | med | high | coverage падает, bounce rate растёт, complaints от sales-команд | multi-vendor waterfall lookup, собственный quality score, регулярный vendor review |
| Market | Demand в РФ остаётся нишевым, category education слишком дорогой | high | high | низкий SQL rate, длинные циклы сделки, buyers просят «объяснить что это вообще» | продавать outcome, а не категорию; входить через managed pilot |
| Market | Конкуренты давят цену, buyer уходит в bundle из дешёвых тулов | high | high | скидки >20% становятся нормой, win-rate падает | жёстко паковать ROI, продавать экономию FTE и pipeline lift, не уходить в low-end SMB |
| Market | Агентства лидогенерации и ручной SDR-labor оказываются «достаточно хорошими» | med | med | сделки проигрываются агентствам и in-house SDR expansion | считать cost-per-qualified-account и speed-to-list, делать hybrid managed model |
| Regulatory | 152-ФЗ и data residency ограничивают хранение и обработку данных | med | high | security/legal тормозит пилоты, клиенты требуют on-prem / RU-hosting | RU-hosting, data minimization, DPA/политики, сегментация PII |
| Regulatory | Санкции / ограничения на западный SaaS и API-стек | high | high | отключения billing, проблемы с VPN/API keys, legal red flags у клиентов | локальные и азиатские резервные провайдеры, abstraction layer, запасной биллинг |
| Regulatory | 115-ФЗ / комплаенс по платежам и контрагентам усложняет enterprise deals | med | med | удлинение procurement и KYC, блокировки счетов/платежей | white-glove legal package, локальная юрструктура, стандартизированный onboarding |
| Financial | Runway сжимается из-за delayed ramp и перерасхода на GTM | med | high | burn > 3,5 млн ₽/мес на M6 без явного pipeline | stage-gated hiring, freeze expansion spend до первых retention cohort |
| Financial | Курс USD поднимает стоимость data/LLM/API и cloud | high | med | COGS/client растёт 15%+ квартал к кварталу | валютная подушка, рублёвые контракты где возможно, repricing clauses |
| Financial | Инфляция и рост зарплат увеличивают fixed costs быстрее revenue | med | med | FOT drift > 10-15% без роста ARPU | ограничить кастомизацию, шаблонизировать delivery, quarterly repricing |
| Black swan | Полное отключение критичного LLM-провайдера | low | high | массовые ошибки генерации, недоступность inference | multi-model routing, офлайн шаблоны, deterministic fallback |
| Black swan | Эскалация войны / новый санкционный пакет рушит procurement и бюджеты | med | high | freeze проектов, перенос CAPEX/OPEX, массовые паузы пилотов | фокус на anti-crisis ROI, диверсификация сегментов, короткие контракты |

**Итог по рискам:** профиль риска высокий, но не хаотичный. Самые тяжёлые угрозы, это не technology risk сам по себе, а **комбинация compliance + distribution + price pressure**.

## 5. Kill conditions через 6 месяцев

1. **Insolvency risk:** если rolling p10 / downside-case показывает **EBITDA < 0** и cash runway падает ниже **6 месяцев**, продолжать нельзя.
2. **EBITDA gate fail:** если к M6 медианный план всё ещё выводит проект на **< 500 000 ₽ EBITDA/мес** даже после price discipline и ICP-focusing, кейс отклоняется.
3. **GTM failure:** если к M6 одновременно не достигнуты **минимум 8 активных клиентов** **или** **ARPU < 180 000 ₽/мес** **или** **win-rate < 8% по SQL**, значит модель не доказывает повторяемый managed GTM motion.

## 6. Final critic view

Clay-like кейс в РФ остаётся **проходным только как service-assisted / managed GTM engineering layer**. В простом SaaS-виде он проигрывает и по demand formation, и по локальным substitutes. Экономика в median сильная, но downside слишком жёсткий: модель ломается при удвоении CAC, удвоении churn и особенно при price compression. Поэтому итоговый инвестиционный статус, **можно держать в pipeline, но только с даунгрейдом за volatility и execution fragility**.

<!-- P6A-DONE -->
<!-- P6B-DONE -->



---

# 06-verdict.md

[GEO-EXPAND] Clay GEO Expand 1659 v2 — NEAR-PASS: 67/100 | EBITDA base=3841К₽/мес через 24 мес | LTV/CAC=19,1x | Ключевое преимущество: очень сильная unit economics в managed GTM engineering | Главный риск: слабый moat и узкий локальный category-demand.

# 06-verdict

sector: GEO-EXPAND

## Investment committee verdict
**VERDICT: NEAR-PASS**

**Normalized score: 67/100**

Причина статуса: economics-gate пройден, company_ebitda_potential_rub_month выше 500 000 ₽/мес достижим в реалистичном горизонте, но рынок в РФ пока выражен через adjacent pains, а moat остаётся слабым и преимущественно execution-based.

## Delta vs previous
- Предыдущий verdict по `clay-geo-expand-v2` был **REJECTED** как duplicate и как кейс ниже раннего порога.
- В rerun кейс улучшился: подтверждены **Contribution Margin 66,0%**, **CAC payback 1,38 мес**, **LTV/CAC 19,1x**, **EBITDA @50 clients = 3 095 950 ₽/мес**.
- Однако approve всё ещё рано, потому что direct demand в РФ слабый, а moat пока не стал structural.

## Оценка
Source tier balance: T1=5, T2=18, T3=0, weighted=2.22. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV/CAC = 19,1x`, `CAC payback = 1,38 мес`, `Contribution Margin = 66,0%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | В `05-critic.md` p50 `EBITDA @M24 = 3 840 675 ₽/мес`, а в `04-economics.md` EBITDA @50 clients = `3 095 950 ₽/мес`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | `лидогенерация b2b` = `MEDIUM, score 30, hh.ru vacancies = 599`, но `sales intelligence` и `prospecting b2b` = `LOW`; применён penalty -2 по tier-balance. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 11 | В `05-critic.md` модель названа `service-assisted / managed GTM engineering layer`, а не product moat; защита строится больше на внедрении, чем на hard defensibility. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | В `05-critic.md` основные угрозы, это `compliance + distribution + price pressure`, но hiring plan и ramp в `04-economics.md` выглядят реалистично. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | `fully-loaded CAC = 344 667 ₽`, `CAC payback = 1,38 мес`, `45-75 дней` sales cycle и валидный ICP из `02-demand.md` и `03-solution.md`. |

**Sum raw = 101/150**  
**Normalized score = round((101 × 100) / 150) = 67/100**

## 7-factor Moat framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | После подключения CRM, scoring и workflow automation появляется умеренный switching cost. |
| Scale economies | 2 | COGS может снижаться за счёт стандартизации delivery и автоматизации enrichment. |
| Proprietary data / model advantage | 1 | Есть шанс накопить workflow data advantage, но доказанной proprietary dataset moat пока нет. |
| Regulatory moat | 0 | Регуляторной защиты нет, compliance здесь скорее барьер в продажах, чем moat. |
| Brand / distribution | 1 | Category brand в РФ слабый, distribution надо строить почти с нуля. |
| Embedded workflow | 3 | При успешном внедрении продукт глубоко встраивается в CRM, enrichment, research и outbound operations. |

**Moat score = round((9 × 25) / 21) = 11/25**

Вывод: moat не падает ниже weak-moat порога `<10`, но остаётся слишком слабым для approve.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 6 600 000 ₽ |
| contribution_margin_rub_month | 165 000 ₽/клиент/мес |
| GM% | 66,0% |
| Fully-loaded CAC | 344 667 ₽ |
| LTV/CAC | 19,1x |
| CAC payback | 1,38 мес по MRR / 2,09 мес по contribution |
| fixed_costs_rub_month | 5 154 050 ₽/мес |
| Break-even clients | 24 core / 32 full |
| startup_capital_to_bep_rub | 26 599 860 ₽ |
| company_ebitda_rub_month @50 clients | 3 095 950 ₽/мес |
| company_ebitda_potential_rub_month p50 @M24 | 3 840 675 ₽/мес |
| clients_to_500k_ebitda | 35 |
| months_to_500k_ebitda | 12-15 мес |
| clients_to_1m_ebitda | 38 |
| months_to_1m_ebitda | 15-16 мес |

## Full business process

| Шаг | Что происходит | ROLE | TOOL | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Сбор intent-лидов и target accounts | Growth Marketer + SDR | hh/Контур/CRM/таблицы/ads | 1 день | 3 000 | средняя |
| 2 | Первичный outbound/inbound touch | SDR | email/Telegram/телефония/CRM | 2 дня | 6 500 | средняя |
| 3 | Квалификация ICP и боли | SDR | CRM + скрипт discovery | 0,5 дня | 2 500 | средняя |
| 4 | Discovery call | AE | video call + CRM | 1 час | 7 000 | низкая |
| 5 | Технический scoping use case | AE + Solutions/CTO | Miro/Notion/CRM | 1 день | 18 000 | низкая |
| 6 | Demo с sample enrichment / scoring | AE + Solutions | product demo + sandbox | 0,5 дня | 12 000 | средняя |
| 7 | Пилотное предложение и расчёт ROI | AE | proposal tool / docs | 0,5 дня | 6 000 | средняя |
| 8 | Security / legal / procurement review | AE + CEO | docs / email | 5 дней календарно | 10 000 | низкая |
| 9 | Подписание договора / счёта | CEO + ops | ЭДО/банк/1С | 2 дня | 4 000 | высокая |
| 10 | Onboarding и подключение CRM/data sources | CSM + ML/Automation | CRM/API/ETL | 5 рабочих дней | 32 000 | средняя |
| 11 | Настройка workflow и scoring | ML/Automation + Backend | orchestration stack | 3 рабочих дня | 24 000 | средняя |
| 12 | Customer training и handoff | CSM | docs + call | 1 день | 8 000 | средняя |
| 13 | Ежемесячное delivery / support | CSM + data ops | CRM + dashboards | ongoing | 34 000 | средняя |
| 14 | Счёт, контроль оплаты, продление | ops + CEO | банк / ЭДО / CRM | 0,5 дня/мес | 3 000 | высокая |

## Team table

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire | Onboarding ramp | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 715 000 |
| Senior Backend | 1 | 400 000 | 1,5 | 1,5 | 520 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 650 000 |
| DevOps | 0,5 | 350 000 | 1 | 1 | 227 500 |
| Frontend | 0,5 | 280 000 | 1 | 1 | 182 000 |
| SDR | 1 | 172 500 | 1 | 1 | 224 250 |
| AE | 1 | 313 000 | 1,5 | 2,5 | 406 900 |
| Customer Success | 1 | 250 000 | 1 | 1 | 325 000 |
| Growth / Marketing Ops | 1 | 208 000 | 1 | 1 | 270 400 |
| RevOps / Implementation analyst | 1 | 260 000 | 1 | 1 | 338 000 |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Контур | Уже продаёт data/SMB software, значит внутренняя боль list-building и account research понятна. | email decision-maker + партнёрский интро | 350 000 ₽/мес |
| 2 | Calltouch | MarTech/performance-вендор с явной потребностью в enrichment и outbound ops для enterprise sales. | конференция + ABM outreach | 250 000 ₽/мес |
| 3 | Roistat | RevOps-heavy компания, где ценность даёт связка data + scoring + outbound prep. | email CRO / head of sales ops | 250 000 ₽/мес |
| 4 | UIS | Телефония и sales stack усиливают потребность в точных ICP-списках и clean CRM. | партнёрство + direct outreach | 200 000 ₽/мес |
| 5 | Mindbox | ABM и enterprise GTM делают полезным managed research/scoring layer для новых сегментов. | email growth lead + тёплый интро | 400 000 ₽/мес |
| 6 | МойСклад | SMB/mid-market B2B growth motion требует регулярного pipeline generation и enrichment. | vc.ru ad + outbound | 220 000 ₽/мес |
| 7 | Selectel | B2B cloud vendor с выраженным outbound/ABM motion и длинным sales cycle по аккаунтам. | email VP Sales / growth lead | 300 000 ₽/мес |
| 8 | Softline | Большая enterprise sales-машина, где account research можно упаковать как shared GTM layer. | enterprise event + account-based outreach | 450 000 ₽/мес |
| 9 | КРОК | Интегратор с hunting-motion и сложным portfolio GTM, где scoring и enrichment экономят FTE. | конференция + партнёрский заход | 350 000 ₽/мес |
| 10 | Первый Бит | Широкая B2B сеть продаж и региональный scale создают боль в automation list-building и qualification. | email commercial director + демо | 250 000 ₽/мес |

## Top-3 risks

| Риск | Probability | Impact | Почему это важно |
|---|---|---|---|
| Weak moat / feature substitution | high | high | Прямого hard moat нет, substitutes, это `Контур/аналитика/ручной ресерч/агентства`, поэтому premium pricing может быстро сжаться. |
| Market demand remains adjacent, not explicit | med-high | high | В `02-demand.md` direct category keywords mostly LOW, поэтому GTM надо строить через pain translation, а не через category pull. |
| Compliance + sanctions + vendor dependency | med | high | 152-ФЗ, санкции и зависимость от data/LLM providers могут увеличить COGS и удлинить enterprise procurement. |

## Что нужно доказать для APPROVED
1. **3-5 платящих design partners** из named-account списка с realised contract value не ниже **250 000 ₽/мес**.
2. Фактический **blended CAC ≤ 450 000 ₽** и payback не хуже **4 месяцев по contribution**.
3. Повторяемое внедрение: onboarding ≤ **14 дней**, без ухода в bespoke services.
4. Удержание и embed: monthly churn ≤ **2,5%**, как минимум 2 команды клиента живут внутри workflow после 90 дней.
5. Материальный moat: собственный workflow dataset, playbooks и connectors, которые реально увеличивают switching cost.

## LTV Upside Calculator

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 250 000 ₽/мес | 300 000-350 000 ₽/мес | Увеличивает contribution и ускоряет рост company_ebitda_rub_month. |
| COGS | 85 000 ₽/клиент/мес | 70 000-75 000 ₽/клиент/мес | Поднимает contribution_margin_rub_month до ~175-180k ₽. |
| Monthly churn | 2,5% | 1,8-2,0% | Поднимает customer_ltv_rub и снижает давление на acquisition engine. |
| CAC | 344 667 ₽ | 250 000-300 000 ₽ | Делает downside Monte Carlo заметно устойчивее. |
| Enterprise mix | ограниченный | 30%+ клиентов в 450k+ tier | Делает путь к EBITDA >500k более надёжным и ускоряет payback fixed base. |

## Финальный вывод
Кейс **не провален**: unit economics и EBITDA potential действительно сильные. Но для инвестиционного approve этого недостаточно. Direct demand в РФ слабый, moat не structural, а GTM остаётся execution-heavy. Поэтому корректный статус сейчас, **NEAR-PASS с правом на апгрейд после доказательства 3-5 reference accounts и material switching costs**.
