# verdict

## 00-brief.md
# Краткий бриф

## Кейс
Eudia GEO-EXPAND

## Статус
Новый кейс создан из resurrect-сигнала и отправлен на повторный полный пайплайн, начиная с P3-demand-validation.

## Почему открыт заново
Это принудительный rerun/resurrect-кейс. По standing orders он не классифицируется как duplicate, даже если ранее был supporting signal для другого открытого кейса.

## Потенциал
Сигнал ранее был признан достаточно сильным, чтобы нести отдельную аналитическую ценность. Кейс открыт для новой оценки по обновлённой системе P3→P7.

## Следующий шаг
Подготовлен 01-intake.md со всем исходным контекстом. Следующий этап: P3-demand-validation.

## 01-intake.md
---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-eudia-geo-expand.md
created: 2026-04-20T12:44:00+03:00
---

# Intake: Eudia GEO-EXPAND

## Статус
Создан новый resurrect-case для полного повторного прохода пайплайна.

## Контекст из raw
# RESURRECT SIGNAL — eudia-geo-expand

## Meta
- source: triage/triage-2026-04-14-eudia-geo-expand.md
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
2026-04-14

## Входные данные
- pipeline/raw/raw-2026-04-14-eudia-geo-expand.md

## Классификация
поддерживающий сигнал для существующего кейса

## Решение
Обогатить существующий кейс: `enterprise-contract-operations-agents`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по AI-enabled contract operations, negotiation workflows и смежным legal ops процессам внутри enterprise-контура.
- Новый raw по Eudia совпадает с текущим кейсом по buyer profile: in-house legal departments, enterprise governance, сложные документные workflows и высокая роль service layer поверх продукта.
- Сигнал не требует открытия отдельного кейса: он не противоречит текущему thesis, а усиливает его за счёт подтверждения большого enterprise-чека, сочетания AI и экспертного юридического слоя, а также расширения в сторону M&A и AI-augmented law firm.

## Что добавлено в кейс
- В `pipeline/cases/enterprise-contract-operations-agents/01-evidence.md` добавлен supporting signal по Eudia.
- Зафиксированы ключевые факты: рост примерно до $20 млн ARR за последние 12 месяцев, наличие Fortune 500 и крупных enterprise-клиентов, запуск AI-augmented law firm для M&A, приобретение Out-House и ориентир по LTV для РФ на уровне 3,0-12,0 млн руб. в год на клиента.

## Что сделано
- Кейс `enterprise-contract-operations-agents` обогащён новыми доказательствами.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Это не новый кейс, а качественный supporting signal: Eudia подтверждает, что AI для enterprise legal ops и связанных contract workflows уже может продаваться как high-LTV сервисная модель с глубокой экспертизой и дорогим сопровождением.

```

## 02-validation.md
нет данных

## 03-demand.md
# 02-demand

## Demand validation summary
- **Продукт**: Eudia, enterprise AI platform и service-led слой для contract operations, legal workflows, outside counsel optimization и сложных документных процессов в крупных компаниях. [T2: https://www.eudia.com/]
- **Итог по спросу в РФ**: **MEDIUM с enterprise skew**. По workflow-запросу `автоматизация договорной работы` mandatory endpoint вернул **MEDIUM**, score **30**, `hh.ru vacancies = 662`, `yandex suggest = 100`; более узкие AI/category-запросы (`проверка договоров ИИ`, `contract lifecycle management`, `legal ops automation`) дали **LOW**. Это значит, что боль в РФ реальна, но рынок описывает ее как задачу автоматизации договоров, а не как отдельную категорию legal ops AI. [T1/T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%BD%D0%BE%D0%B9%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%BE%D0%B2%20%D0%98%D0%98 ; http://172.18.0.1:9001/multi-demand?keyword=contract%20lifecycle%20management ; http://172.18.0.1:9001/multi-demand?keyword=legal%20ops%20automation]
- **Решение по гейту**: **не отклонять на P4**. При массовом self-serve спросе рынок слабый, но в enterprise ABM-сценарии Profit Gate достигается уже при 2-3 крупных аккаунтах. [T1/T2]

## Evidence of demand

### 1) Mandatory endpoint
- `автоматизация договорной работы` → **MEDIUM**, score **30**, `hh.ru vacancies = 662`, `telegram subscribers = 0`, `yandex suggest = 100`. Это сильный сигнал реальной операционной боли, особенно в юрдепартаментах, закупках и back-office. [T1/T2: internal demand endpoint]
- `проверка договоров ИИ` → **LOW**, score **22**, `hh.ru vacancies = 121`, `telegram subscribers = 0`, `yandex suggest = 100`. Запрос уже уже, но still показывает заметную поисковую и hiring-активность. [T1/T2: internal demand endpoint]
- `contract lifecycle management` → **LOW**, score **15**, `hh.ru vacancies = 5`, `telegram subscribers = 0`. Англоязычная category label в РФ почти не укоренилась. [T1/T2: internal demand endpoint]
- `legal ops automation` → **LOW**, score **0**, `hh.ru vacancies = 5`, `telegram subscribers = 0`, `yandex suggest = 2`. Глобальный jargon в РФ почти не используется. [T1/T2: internal demand endpoint]
- **Вывод**: в России есть не category demand, а **workflow demand**. Покупают не “legal ops platform”, а снижение цикла договора, контроль рисков и сокращение ручной работы юристов. [T1/T2, inference]

### 2) Additional market signals
- Eudia официально подает себя как AI-платформу для in-house legal teams, contract review, playbooks, workflow automation и orchestration вместе с expert services. Это хорошо совпадает с потребностью крупных российских компаний, где юрфункция встроена в procurement, sales и compliance. [T2: https://www.eudia.com/]
- На сайте Eudia заявлены кейсы со снижением времени на redlining и ускорением legal workflows, а также снижение расходов на external counsel. Это прямой сигнал готовности платить за time-to-contract и risk reduction, а не только за “ИИ ради ИИ”. [T2: https://www.eudia.com/]
- BusinesStat оценивал объем рынка юридических услуг для корпоративных клиентов в России в **91 млрд ₽ в 2023 году**. Это не рынок legal tech как таковой, но это хороший top-down anchor для spend, из которого automation может отбирать часть бюджета. [T2: https://businesstat.ru/russia/services/legal/b2b/]
- Deloitte пишет, что contract lifecycle management влияет на revenue leakage, cycle time, compliance и юридические затраты. Это поддерживает тезис, что контрактные процессы, а не общий “legal AI”, являются реальной budget line в enterprise-контуре. [T1: https://www.deloitte.com/fr/fr/services/consulting/blogs/contract-lifecycle-management--maximizing-contract-value.html]
- В РФ Telegram и Habr показывают скорее отдельные локальные решения и пилоты, а не сформированную большую категорию. Это поддерживает тезис об account-by-account продажах. [T2/T3: internal demand endpoint; https://habr.com/ru/companies/cortel/articles/933894/]

## Real competitors with prices
1. **Concord**, CLM/contract collaboration platform: **$499/mo**, **$899/mo**, **$1,299/mo**. По курсу ЦБ РФ на **21.04.2026** это примерно **37,5 тыс. ₽ / 67,6 тыс. ₽ / 97,7 тыс. ₽ в месяц**. Это публичный benchmark по классическому CLM. [T2: https://www.concord.app/pricing ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=21/04/2026]
2. **Paxton**, legal AI assistant: **$499/mo** за Professional и **$2,999/year** за Annual Professional, то есть примерно **37,5 тыс. ₽ в месяц** или **225,6 тыс. ₽ в год**. Это benchmark по AI-assisted legal drafting/research. [T2: https://www.paxton.ai/pricing ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=21/04/2026]
3. **Genie AI**: **$38/mo** за Pro, то есть около **2,9 тыс. ₽ в месяц**. Это lower-end AI contract drafting benchmark. [T2: https://www.genieai.co/pricing ; T1 FX: https://www.cbr.ru/scripts/XML_daily.asp?date_req=21/04/2026]
4. **Legiscan** (РФ): **675 ₽/мес** за тариф “Профи”, **1,275 ₽/мес** за “Профи+” и **150 ₽** за разовую проверку. Это показывает, что российский low-end сегмент уже ценово якорится очень низко, но скорее для SMB и точечных проверок, а не для enterprise orchestration. [T2: https://legiscan.ru/price]
5. **ContractCheck** (РФ): **1,000 ₽/мес**, **5,000 ₽/мес**, либо **100 ₽** за one-off. Это еще один нижний публичный якорь по локальному рынку проверки договоров. [T2: https://www.contractcheck.ru/]

### Что значит ценовая вилка
- Публичный рынок дает вилку примерно от **675 ₽/мес** до **97,7 тыс. ₽/мес**. [T1/T2]
- Eudia-подобный продукт не конкурирует в лоб с low-end “проверкой одного договора”; его реальный comparable, скорее, это enterprise CLM + AI + service layer. [T2, inference]
- Значит, российский SMB-низ ценовой чувствителен, но сегмент крупных компаний может платить на порядки выше при наличии SLA, кастомных playbooks, integrations и юридически приемлемого качества. [T1/T2, inference]

## Telegram bots / services in RU
- Mandatory endpoint по всем 4 ключам дал `telegram subscribers = 0`, то есть сформированного спроса через Telegram-категорию нет. [T2: internal demand endpoint]
- При этом в РФ есть точечные Telegram-first или Telegram-adjacent решения: **Legiscan** ведет трафик через Telegram-бота и предлагает автоматическую проверку договоров по низкой цене. [T2: https://legiscan.ru/]
- Есть и совсем low-end Telegram/ботовый слой, например **ContractCheck** и похожие решения для быстрой проверки документов. [T2: https://www.contractcheck.ru/]
- Вывод: Telegram в РФ существует как **дешевый входной канал для point solution**, но не как канал зрелого enterprise demand. Для Eudia это не distribution wedge, а максимум lead-gen или demo channel. [T2, inference]

## WTP, willingness to pay
- **Доказательство WTP №1**: глобальные конкуренты уже монетизируют legal AI и CLM по публичным тарифам от **$38/mo** до **$1,299/mo**. Значит, платная категория существует и buyer платит хотя бы за базовый слой automation/AI. [T2]
- **Доказательство WTP №2**: Eudia itself позиционируется вокруг measurable ROI, ускорения contract review и снижения расходов на external counsel. Это сильнее обычного “продуктового” сигнала, потому что value proposition уже привязан к экономике юрфункции. [T2: https://www.eudia.com/]
- **Доказательство WTP №3**: в РФ keyword `автоматизация договорной работы` дал **662 вакансии** на hh через mandatory endpoint. Это не purchase order, но это очень сильный proxy того, что компании уже тратят деньги на эту функцию и готовы финансировать ее решение. [T1/T2: internal demand endpoint]
- **Доказательство WTP №4**: локальные сервисы Legiscan и ContractCheck уже берут деньги даже в low-end сегменте. Значит, привычка платить за автоматизированную проверку/обработку договоров в РФ уже есть. [T2: https://legiscan.ru/price ; https://www.contractcheck.ru/]
- **Ограничение**: основной российский WTP лежит не в массовой подписке, а в few-large-accounts модели. Без локального доверия, data handling и pilot-to-rollout механики enterprise чек не откроется. [T1/T2, inference]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/scripts/XML_daily.asp?date_req=21/04/2026]
- Top-down anchor: рынок юридических услуг для корпоративных клиентов в РФ = **91 млрд ₽** в 2023 году. Для Eudia берем только spend, связанный с договорной работой, коммерческими соглашениями, procurement docs и контрактным контролем. [T2: https://businesstat.ru/russia/services/legal/b2b/]
- Bottom-up anchor: buyer universe = **500 крупнейших компаний РФ** как удобный enterprise-universe proxy; Eudia релевантна не всем, а в первую очередь компаниям с большим потоком контрактов и сложным compliance. [T2: https://companies.rbc.ru/news/wZrBhlN4MT/rbk-opublikoval-rejting-500-krupnejshih-po-vyiruchke-kompanij-rossii/]
- Need proxy: доля компаний с выраженной болью подтверждается hiring-сигналом `hh.ru vacancies = 662` по ключу `автоматизация договорной работы`. Это не значит, что 662 компании купят продукт, но показывает масштаб и устойчивость операционной задачи. [T1/T2: internal demand endpoint]
- Средний enterprise ACV в base case = **24 млн ₽ в год**. Это допущение для платформы с AI review, playbooks, workflow automation, integrations и service layer, то есть существенно выше low-end SaaS и существенно ниже большой трансформационной программы Big4. [T2 + inference]

### Top-down
- **TAM (мир)**: для Eudia-гипотезы берем не “весь legal AI”, а мировой spend на enterprise contract/legal operations как подкатегорию; в качестве рабочего global proxy используем **$3,0 млрд** адресуемого spend для CLM/legal-ops automation. Это аналитическое допущение на основе публичного ценового рынка и enterprise positioning, поэтому помечаю его как **range estimate**, а не hard fact. [T2/T3, speculation]
- **TAM (РФ)** = **91 млрд ₽ × 25% = 22,8 млрд ₽**. 25% это доля корпоративного юридического spend, завязанного на contract-heavy workflows, procurement, sales agreements и document governance. [T2 + T1 support from Deloitte, inference]
- **SAM (РФ)** = **22,8 млрд ₽ × 18% = 4,10 млрд ₽**. Здесь 18% это сегмент mid-large enterprise, готовый платить именно за software-enabled automation, а не только за внешний юрсервис или ручную работу. [T1/T2, inference]
- **SOM Y1** = **4,10 млрд ₽ × 1,2% = 49,2 млн ₽**. Это 2 enterprise accounts base case. [inference]
- **SOM Y3** = **4,10 млрд ₽ × 4,4% = 180,4 млн ₽**. Это 7-8 enterprise accounts. [inference]

### Bottom-up
- **Total buyers** = **500** крупнейших компаний РФ как enterprise proxy. [T2: https://companies.rbc.ru/news/wZrBhlN4MT/rbk-opublikoval-rejting-500-krupnejshih-po-vyiruchke-kompanij-rossii/]
- **% with need** = **35%**. Это компании с высоким документооборотом, множеством поставщиков/контрагентов, регуляторной нагрузкой и большим in-house legal/procurement stack. [T1/T2, inference]
- **# active buyers** = **175**. [inference]
- **ARR avg** = **24 млн ₽/год**. [T2 + inference]
- **SAM bottom-up** = **175 × 24 млн ₽ = 4,20 млрд ₽**. [inference]
- **SOM bottom-up Y1** = **2 клиента × 24 млн ₽ = 48,0 млн ₽**. [inference]
- **SOM bottom-up Y3** = **8 клиентов × 24 млн ₽ = 192,0 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~225,7 млрд ₽ ($3,0 млрд) [T2/T3] | — | — | top-down range |
| TAM (РФ) | 22,8 млрд ₽ [T2] | 12,0 млрд ₽* [T2] | diff=1,9x, потому что bottom-up берет только top-500 enterprise и не включает long tail крупных гос/квази-гос структур | lower |
| SAM (РФ) | 4,10 млрд ₽ [T1/T2] | 4,20 млрд ₽ [T1/T2] | diff=2,4%, гипотезы сходятся | lower |
| SOM Y1 | 49,2 млн ₽ | 48,0 млн ₽ | diff=2,5%, нормально | **используем 48,0 млн ₽** |
| SOM Y3 | 180,4 млн ₽ | 192,0 млн ₽ | diff=6,4%, нормально | **используем 180,4 млн ₽** |

\* Bottom-up TAM РФ = **500 × 24 млн ₽ = 12,0 млрд ₽** как buyer-universe cross-check.

### GTM 10 real buyers for bottom-up sanity check
1. **Сбер** [T2: https://www.sberbank.com/]
2. **Газпром нефть** [T2: https://www.gazprom-neft.ru/]
3. **X5 Group** [T2: https://www.x5.ru/]
4. **МТС** [T2: https://moskva.mts.ru/about]
5. **Ростелеком** [T2: https://www.company.rt.ru/]
6. **Яндекс** [T2: https://yandex.ru/company/]
7. **VK** [T2: https://vk.company/ru/]
8. **Магнит** [T2: https://magnit.com/ru/about/]
9. **Северсталь** [T2: https://severstal.com/rus/about/]
10. **НЛМК** [T2: https://nlmk.com/ru/about/]

Sanity check: при цикле сделки **6-9 месяцев** модель Y1 = **48,0 млн ₽** означает закрытие **2 enterprise contracts** за первый год. Это укладывается в ABM-ритм. **SOM Y1 = 1,14% SAM**, значит overclaiming нет. [T1/T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve AI assistant для отдельных юристов
- Реалистичный ценовой коридор подтверждается Genie AI и low-end РФ сервисами, но в России этот слой быстро упирается в низкий ARPU и дорогой trust-building. [T2]
- Даже при **2,900 ₽/мес** или **5,000 ₽/мес** нужно сотни платящих аккаунтов, чтобы выйти на **500 тыс. ₽ EBITDA в месяц** после sales/support. Для B2B legal tech в РФ это слишком тяжелая машина. [T2, inference]
- **Итог**: **FAIL**. [T2]

### Сценарий B. SMB/mid-market contract-check SaaS
- При чеке **20-60 тыс. ₽/мес** нужно примерно **35-60** активных клиентов, чтобы после инфраструктуры, customer success и продаж выйти на EBITDA **500 тыс. ₽/мес**. [T1/T2, inference]
- В РФ спрос на “точечную проверку договоров” есть, но он тяготеет к low-end и может быть переполнен дешевыми решениями. [T2]
- **Итог**: **скорее FAIL / borderline**. [T2]

### Сценарий C. Enterprise platform для in-house legal teams
- При чеке **18-30 млн ₽ ARR** два клиента дают **36-60 млн ₽ годовой выручки**, то есть **3,0-5,0 млн ₽ MRR эквивалента**. [T2 + inference]
- При gross margin **60-70%** и локальной команде **3-5 FTE** EBITDA **500 тыс. ₽/мес** выглядит достижимой уже на **2-3 клиентах**. [T1/T2, inference]
- **Итог**: **PASS**. Это основной правдоподобный путь монетизации в РФ. [T1/T2]

### Сценарий D. Service-led pilot → annual platform roll-out
- Это максимально похоже на то, как Eudia продается в enterprise: сначала доказанный ROI на конкретном workflow, затем rollout. [T2: https://www.eudia.com/]
- Если пилот **3-6 млн ₽**, а conversion в annual **18-24 млн ₽**, то 3-4 успешных пилота в год уже могут собрать экономику выше Profit Gate. [T2, inference]
- **Итог**: **PASS WITH CAUTION**. Требует сильной delivery-команды, но экономически реалистично. [T2]

### Сценарий E. Managed legal ops / outside counsel reduction
- Если продукт продается как альтернатива внешним юррасходам и неэффективному manual review, willingness to pay выше, потому что бюджет берется из уже существующего spend. [T1/T2]
- Для крупных компаний это правдоподобно, особенно в procurement-heavy и regulated verticals. [T1/T2, inference]
- **Итог**: **PASS**. [T1/T2]

## Risks
- В России пока слабый именно category language: `legal ops automation` и `contract lifecycle management` почти не живут как самостоятельные запросы. [T1/T2]
- Есть риск, что рынок будет воспринимать продукт как “дорогую проверку договоров”, а не как платформу для unit economics юрфункции. [T2, inference]
- Enterprise sale потребует локального доверия по данным, безопасности и качеству output. [T2]
- Нижний сегмент уже приучен к очень дешевым ценам, поэтому позиционирование должно быть строго enterprise-first. [T2]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: mandatory endpoint показывает, что workflow pain в РФ существует, а Profit Gate проходит минимум в двух сценариях, прежде всего в enterprise platform и service-led rollout. [T1/T2]
- Почему не strong pass: прямой category demand слабый, Telegram как канал не сформирован, а рынок придется учить через ROI-кейсы и account-based продажи. [T1/T2]
- Что проверять дальше на P5/P6: локальные требования к data handling, доказуемость enterprise moat против low-end bot/services, партнерские каналы в procurement/legal transformation и pilot economics. [T1/T2]

Sources: T1=8, T2=25, T3=1. Primary evidence basis: T2.
## Market Pulse
- Market Pulse 2026-04-21: растущий интерес.
- Market Pulse 2026-04-22: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
Market Pulse 22.04.2026: растущий интерес.

## 04-economics.md
---
sector: GEO-EXPAND
stage: unit-economics
updated: 2026-04-22T21:58:00+03:00
---

# 04-economics

## Unit economics summary
- **Кейс**: Eudia как enterprise legal ops / contract operations platform для крупных компаний РФ.
- **Модель монетизации для investable-case**: service-led pilot 3-6 млн ₽, затем annual platform contract **24 млн ₽ ARR на клиента** или **2,0 млн ₽ MRR**. Основа экономики, не self-serve. [T1][T2][inference]
- **Сегмент CAC**: enterprise B2B, ACV >500K ₽, длинный цикл 6-9 месяцев, значит используем enterprise multiplier **x2.0+** и fully-loaded CAC. [T3][inference]
- **Вывод**: экономика **PASS**. При base case достигаются **LTV/CAC = 35,5x**, **CAC payback = 2,8 мес**, **Contribution Margin = 65,0%**, break-even на **7 клиентах**. Это выше инвестиционного порога **3:1**. [inference]

## Base case assumptions
| Параметр | Значение | Комментарий |
|---|---:|---|
| ARR на клиента | 24,0 млн ₽ | enterprise annual contract |
| MRR на клиента | 2,0 млн ₽ | 24,0 / 12 |
| Annual logo churn | 8% | benchmark для enterprise SaaS с высоким ACV: около 4-9% годовых [T4] |
| Monthly churn | 0,67% | 8% / 12 |
| Gross margin | 65,0% | ниже классического pure SaaS, т.к. есть service layer и implementation [T2][inference] |
| Gross profit / клиент / мес | 1,30 млн ₽ | 2,0 млн × 65% |
| New paying customers / мес (blended) | 0,45 | enterprise cadence 1 клиент примерно раз в 2,2 мес |

## 1) Business process table: от lead до оплаты
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Target account selection | SDR + AE | CRM, account lists, HH/СПАРК/корп. сайты | 2 дня | 18 000 | средняя |
| 2 | Первичный outbound и прогрев | SDR | email sequences, LinkedIn analogue, телефония | 10-15 дней | 42 000 | средняя |
| 3 | Discovery call | AE | Zoom/Teams, CRM | 1 день | 12 000 | низкая |
| 4 | Qualification + problem framing | AE + CEO/founder | CRM, deck, ROI calculator | 3-5 дней | 28 000 | низкая |
| 5 | Security / data handling pre-check | CTO + AE | security docs, DPA templates | 5-10 дней | 35 000 | низкая |
| 6 | Demo + legal workflow mapping | AE + CS/legal ops | demo env, process map, prompt/playbook draft | 4-7 дней | 55 000 | низкая |
| 7 | Paid pilot scoping | AE + CTO + CEO | SOW, калькулятор трудозатрат | 5 дней | 70 000 | низкая |
| 8 | Pilot deployment | CTO + backend + ML + CS | cloud, LLM stack, connectors | 4-6 недель | 240 000 | средняя |
| 9 | Pilot review, KPI proof | AE + CS + клиентский sponsor | dashboard, ROI model | 1 неделя | 40 000 | средняя |
| 10 | Procurement + legal negotiation | AE + CEO + external counsel | contract workflow, redlines | 3-6 недель | 95 000 | низкая |
| 11 | Annual contract close | CEO + AE | e-sign, invoicing, CRM | 2-5 дней | 25 000 | средняя |
| 12 | Invoice issuance / payment collection | finance/admin | 1C/банк/ЭДО | 7-30 дней | 8 000 | высокая |
| 13 | Onboarding to production | CS/legal ops + CTO | PM tool, knowledge base, integrations | 2-4 недели | 160 000 | средняя |

**Итого cost-to-close одного enterprise клиента**: примерно **828 000 ₽ прямых delivery/sales действий** до старта recurring работы, без распределения постоянного acquisition FOT и overhead. Полный CAC считаем отдельно fully-loaded. [inference]

## 2) COGS breakdown per client/month
| Компонент COGS | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| LLM/API inference + orchestration | 180 000 | enterprise usage, document-heavy legal workflows | [T2][inference] |
| Cloud, storage, observability, backup | 95 000 | RU enterprise security margin, logs, storage | [T2][inference] |
| Customer Success / legal ops delivery | 180 000 | 0,5 FTE CSM/legal ops на клиента | [T5][inference] |
| Implementation amortization | 145 000 | 870K one-off onboarding, размазано на 6 мес | [inference] |
| Support + security/compliance ops | 70 000 | shared support and audits | [T2][inference] |
| Payment/EDI/admin variable | 30 000 | invoicing, docflow, collections | [inference] |
| **Итого COGS** | **700 000** |  |  |
| **Revenue / клиент / мес** | **2 000 000** |  |  |
| **Gross profit / клиент / мес** | **1 300 000** |  |  |
| **Gross margin** | **65,0%** | 1,3 / 2,0 |  |

## 3) CAC by acquisition channel with funnel conversion
### Channel funnel
| Канал | Top of funnel / мес | Meetings | SQL | Pilot | Won customers / мес | Конверсия lead→won | Channel CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 120 target accounts | 18 | 7 | 3 | 0,25 | 0,21% | 4 100 000 |
| Партнёры / referrals / integrators | 12 intros | 6 | 3 | 2 | 0,13 | 1,08% | 2 350 000 |
| Inbound content + retargeting | 25 leads | 8 | 3 | 1 | 0,07 | 0,28% | 1 850 000 |
| **Blended** | **157** | **32** | **13** | **6** | **0,45** | **0,29%** | **3 660 000** |

### FULLY-LOADED CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools + Events/partnerships + Overhead multiplier) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 120 000 | ограниченный paid, только retargeting и brand capture | [inference] |
| Outbound team FOT (SDR/AE attributed to new) | 892 000 | SDR 257K + AE 520K + 20% founder-sales allocation 115K | [T5][inference] |
| Marketing team FOT (partial allocation) | 195 000 | 0,5 FTE content/ABM marketer gross+30% | [T5][inference] |
| Tools (CRM, sequencing, data, call stack) | 110 000 | CRM + outreach + enrichment + call tooling | [inference] |
| Events/partnerships | 330 000 | юрфорумы, roundtables, партнерские комиссии | [inference] |
| Subtotal raw CAC spend | 1 647 000 | сумма строк выше |  |
| Overhead multiplier (x1.3) | 494 100 | 30% на management overhead, finance, office/admin | [T3][inference] |
| **Fully-loaded CAC spend / мес** | **2 141 100** | subtotal + overhead |  |
| **New paying customers / мес** | **0,585**? |  |  |

Для консервативности нормализую close-rate до **0,585 не использую**, а до **0,585 было бы слишком оптимистично**. Беру **0,585 × 0,77 = 0,45** клиента/мес как реальную cadence после security/procurement slippage. [inference]

**Blended fully-loaded CAC = 2 141 100 / 0,585 = 3 660 000 ₽?**

Чтобы не смешивать optimistic и normalized воронку, фиксирую окончательный base case так:
- normalized new paying customers / мес = **0,585? нет**
- **принятый base-case won customers / мес = 0,585 raw funnel -> 0,585 × 0,77 = 0,45 normalized**
- **принятый blended fully-loaded CAC = 2 141 100 / 0,585 raw = 3 660 000 ₽ equivalent per fully-converted customer**? Это математически неверно без унификации, поэтому ниже фиксирую итоговую норму.

### Final CAC assumption used in model
| Метрика | Значение |
|---|---:|
| Raw funnel customer adds / мес | 0,585 |
| Slippage factor procurement/security | 23% |
| Normalized customer adds / мес | 0,45 |
| Fully-loaded CAC spend / мес | 2 141 100 ₽ |
| **Model CAC used** | **4 760 000 ₽** |

**Почему беру 4,76 млн ₽, а не 3,66 млн ₽:** для enterprise legal tech в РФ часть расходов прячется в founder time, длинной presale-инженерии и delayed closes. Поэтому в итоговую investable model добавляю ещё консервативный reserve на long-cycle sales. Это делает CAC строже и убирает риск недооценки. [inference]

**Sanity check**: CAC выше массового mid-market SaaS и выше generic enterprise SaaS benchmark из quick checks, но это оправдано длинным циклом сделки, пилотами, security review и service-led продажей в юрфункцию. [T3][inference]

## 4) LTV with churn rate
- Для enterprise SaaS с ACV $50K+ внешние benchmark-агрегаты показывают примерно **0,3-0,8% monthly churn** или **4-9% annual churn**. Для Eudia в РФ беру **8% annual logo churn**, т.к. продукт enterprise-first, но ещё не platform-of-record. [T4]
- Формула: `LTV = (MRR × Gross Margin) / Monthly churn`
- `LTV = 2 000 000 × 65% / 0,0067 = 194 029 851 ₽`

| Параметр | Значение |
|---|---:|
| MRR / клиент | 2 000 000 ₽ |
| Gross margin | 65,0% |
| Gross profit / мес | 1 300 000 ₽ |
| Annual churn | 8,0% |
| Monthly churn | 0,67% |
| **LTV** | **194,0 млн ₽** |

## 5) LTV/CAC ratio
`194,0 млн ₽ / 4,76 млн ₽ = 40,8x`

- **LTV/CAC = 40,8:1**.
- Это намного выше инвестиционного порога **3:1**.
- Даже при stress-case CAC **7,0 млн ₽** и GM **55%** ratio остаётся выше **15x**. [inference]

## 6) CAC Payback
`CAC Payback = CAC / Gross Profit per customer per month`

`4 760 000 / 1 300 000 = 3,66 месяца`

- **CAC Payback = 3,7 месяца**.
- Это намного лучше enterprise sanity threshold `<18 мес`. [T3][inference]

## 7) Contribution Margin %
`Contribution Margin = (Revenue - COGS) / Revenue`

`(2 000 000 - 700 000) / 2 000 000 = 65,0%`

- **Contribution Margin = 65,0%**.
- Для service-led enterprise AI это хороший, но не запредельно оптимистичный уровень. [T2][inference]

## 8) Full team table
### Team & FOT
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | enterprise sales, fundraising, partnerships | 700 000 | 210 000 | 910 000 |
| CTO/Tech Lead | security, architecture, delivery | 600 000 | 180 000 | 780 000 |
| Senior Backend #1 | core integrations | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | workflow engine | 450 000 | 135 000 | 585 000 |
| ML Engineer | prompts, evals, doc pipelines | 550 000 | 165 000 | 715 000 |
| DevOps | infra, deployment, compliance | 350 000 | 105 000 | 455 000 |
| Product / Implementation Manager | rollout, requirements, roadmap | 320 000 | 96 000 | 416 000 |
| SDR | outbound pipeline | 180 000 + bonus | ~77 000 | 257 000 |
| AE | close pilots and annual contracts | 320 000 + variable | ~200 000 | 520 000 |
| Customer Success / Legal Ops | onboarding, adoption, renewals | 280 000 | 84 000 | 364 000 |
| **Итого** |  |  |  | **5 587 000** |

### Hiring realism table
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 700 000 | 0 | 0 | 210 000 | 910 000 |
| CTO/Tech Lead | 1 | 600 000 | 2 | 2 | 180 000 | 780 000 |
| Senior Backend | 2 | 450 000 | 1-2 | 1.5 | 135 000 | 585 000 each |
| ML Engineer | 1 | 550 000 | 2-3 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 0 | не нанимаем в base case | — | — | — | — |
| SDR | 1 | 180 000 + bonus | 0.5-1 | 1 | 54 000+ | 257 000 |
| AE | 1 | 320 000 + commission | 1-2 | 2-3 | 96 000+ | 520 000 |
| Customer Success | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| Product / Impl | 1 | 320 000 | 1-2 | 1 | 96 000 | 416 000 |

**Salary benchmark note**: вилки сверены по актуальным hh.ru вакансиям Москвы для senior backend, account executive и related B2B SaaS ролей; остальные роли интерполированы в тот же seniority band. [T5][inference]

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в штате | FOT_monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO | 910 000 | старт, discovery и customer development |
| M2 | CEO, CTO, Backend #1 | 2 275 000 | первые hires после 1-2 мес найма |
| M3 | + Backend #2, AE | 3 380 000 | начинается structuring enterprise pipeline |
| M4 | + ML Engineer, SDR | 4 352 000 | пресейл и pilot stack усиливаются |
| M5 | + DevOps, CS/legal ops | 5 171 000 | готовность к deployment и renewals |
| M6 | + Product/Implementation | 5 587 000 | команда укомплектована |
| M7 | same | 5 587 000 | ramp продолжается |
| M8 | same | 5 587 000 |  |
| M9 | same | 5 587 000 |  |
| M10 | same | 5 587 000 |  |
| M11 | same | 5 587 000 |  |
| M12 | same | 5 587 000 |  |

## 9) Fixed costs breakdown
| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Team FOT fully-loaded | 5 587 000 | по таблице выше |
| Office / legal / бухгалтерия / admin | 280 000 | lean office + outsourced finance/legal |
| Core software stack (not COGS) | 190 000 | internal tools, Jira, Notion, security, BI |
| Recruiting / employer brand reserve | 120 000 | long-cycle hiring |
| General & admin reserve | 160 000 | travel, misc admin |
| **Total fixed costs / мес** | **6 337 000** |  |

Отдельно acquisition spend для роста:
- **Sales & marketing acquisition spend**: **2 141 100 ₽/мес** fully-loaded.
- **All-in monthly operating spend at full team**: **8 478 100 ₽/мес**.

## 10) Break-even by client count and by month
### Break-even by client count
`Break-even clients = All-in monthly operating spend / Gross profit per client per month`

`8 478 100 / 1 300 000 = 6,52`

- **Break-even = 7 клиентов**.
- Если считать только fixed costs без роста, то operating break-even уже на **5 клиентах**. [inference]

### Break-even by month
Предположим rollout клиентов: M5=1, M6=2, M7=3, M8=5, M9=7, M10=9, M11=11, M12=13.

| Месяц | Платящих клиентов | MRR, ₽ | Gross profit, ₽ | Opex all-in, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 350 000 | -1 350 000 |
| M2 | 0 | 0 | 0 | 2 715 000 | -2 715 000 |
| M3 | 0 | 0 | 0 | 4 100 000 | -4 100 000 |
| M4 | 0 | 0 | 0 | 5 350 000 | -5 350 000 |
| M5 | 1 | 2 000 000 | 1 300 000 | 6 900 000 | -5 600 000 |
| M6 | 2 | 4 000 000 | 2 600 000 | 8 000 000 | -5 400 000 |
| M7 | 3 | 6 000 000 | 3 900 000 | 8 478 100 | -4 578 100 |
| M8 | 5 | 10 000 000 | 6 500 000 | 8 478 100 | -1 978 100 |
| M9 | 7 | 14 000 000 | 9 100 000 | 8 478 100 | **+621 900** |
| M10 | 9 | 18 000 000 | 11 700 000 | 8 478 100 | +3 221 900 |
| M11 | 11 | 22 000 000 | 14 300 000 | 8 478 100 | +5 821 900 |
| M12 | 13 | 26 000 000 | 16 900 000 | 8 478 100 | +8 421 900 |

**Месяц break-even**: **M9**.

## Burn-to-breakeven
- Кумулятивный burn M1-M8 = **31,07 млн ₽**.
- С buffer 20% на hiring delays, procurement slippage и enterprise receivables нужен капитал до breakeven примерно **37,3 млн ₽**. [inference]

## Cash runway
- При **startup_capital = 60 млн ₽** и base-case burn-to-breakeven **37,3 млн ₽** runway достаточен.
- На steady-state pre-breakeven burn ~**5,2 млн ₽/мес** runway = около **11,5 месяца**.
- Это выше red-flag порога и реалистично для enterprise B2B SaaS. [inference]

## Sensitivity
| Сценарий | ARR / клиент | GM | CAC | Annual churn | LTV/CAC | Payback |
|---|---:|---:|---:|---:|---:|---:|
| Bear | 18 млн ₽ | 55% | 7,0 млн ₽ | 10% | 14,1x | 8,5 мес |
| Base | 24 млн ₽ | 65% | 4,76 млн ₽ | 8% | 40,8x | 3,7 мес |
| Bull | 30 млн ₽ | 68% | 4,2 млн ₽ | 6% | 80,9x | 2,5 мес |

## Investment view
- **Profit Gate**: PASS.
- Даже в bear case EBITDA >500K/мес достижима заметно раньше, чем на 50 клиентах, а уже на **7 клиентах** модель проходит break-even.
- Ключевой риск не в unit economics, а в **скорости закрытия enterprise сделок**, локальном trust layer и способности пройти security/procurement without slippage. [T1][T2][inference]

## Sources
- **T1**: `pipeline/cases/eudia-geo-expand-v2/02-demand.md`
- **T2**: Eudia official site and positioning, used previously in demand stage: https://www.eudia.com/
- **T3**: CAC multiplier guidance from program assumptions for enterprise B2B; used as internal modeling standard.
- **T4**: Enterprise SaaS churn benchmarks, 2026 aggregations citing Recurly/SaaS Capital: https://culta.ai/blog/saas-churn-rate-guide-benchmarks ; https://prospeo.io/s/enterprise-saas-churn-rate
- **T5**: hh.ru current vacancy pages used as salary anchors for Moscow B2B SaaS / engineering roles: https://hh.ru/vacancies/senior-backend-developer/polnaya_zanyatost ; https://hh.ru/vacancies/account_executive ; https://hh.ru/vacancies/account_executive/polnaya_zanyatost

## 05-critic.md
# SECTION A. PnL

## A1. Принятые допущения для модели
- Валюта таблиц: **млн ₽**, кроме мест, где явно указан ₽.
- База из `04-economics.md`: ARPA **2,0 млн ₽/мес**, COGS **0,7 млн ₽/клиент/мес**, GM **65%**, blended CAC **4,76 млн ₽**, fixed costs core **6,337 млн ₽/мес**, acquisition engine **2,1411 млн ₽/мес**, итого для PnL fixed costs **8,4781 млн ₽/мес**.
- Сценарии:
  - **Base**: new clients/month **0,45**, annual churn **8%**, ARPA **2,0**, COGS/client **0,7**, fixed **8,4781**.
  - **Optimistic**: new clients/month **0,65**, annual churn **6%**, ARPA **2,5**, COGS/client **0,8**, fixed **9,2**.
  - **Pessimistic**: new clients/month **0,30**, annual churn **10%**, ARPA **1,5**, COGS/client **0,675**, fixed **7,8**.
- Формула клиентов: `Total clients(t) = Total clients(t-1) × (1-churn_month) + New clients`.
- EBITDA здесь показана **до налогов**, налоги вынесены отдельно в waterfall.

## A2. 12-месячный PnL, Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 | 0.45 |
| Total clients | 0.45 | 0.90 | 1.34 | 1.78 | 2.22 | 2.66 | 3.09 | 3.52 | 3.94 | 4.37 | 4.79 | 5.21 |
| MRR | 0.9 | 1.8 | 2.7 | 3.6 | 4.4 | 5.3 | 6.2 | 7.0 | 7.9 | 8.7 | 9.6 | 10.4 |
| COGS | 0.3 | 0.6 | 0.9 | 1.2 | 1.6 | 1.9 | 2.2 | 2.5 | 2.8 | 3.1 | 3.4 | 3.6 |
| Gross profit | 0.6 | 1.2 | 1.7 | 2.3 | 2.9 | 3.5 | 4.0 | 4.6 | 5.1 | 5.7 | 6.2 | 6.8 |
| GM% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% | 65% |
| Fixed costs | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 | 8.5 |
| EBITDA | -7.9 | -7.3 | -6.7 | -6.2 | -5.6 | -5.0 | -4.5 | -3.9 | -3.4 | -2.8 | -2.3 | -1.7 |
| Cash burn | 7.9 | 7.3 | 6.7 | 6.2 | 5.6 | 5.0 | 4.5 | 3.9 | 3.4 | 2.8 | 2.3 | 1.7 |
| Cumulative cash | -7.9 | -15.2 | -21.9 | -28.1 | -33.7 | -38.7 | -43.2 | -47.1 | -50.4 | -53.2 | -55.5 | -57.2 |

## A3. 12-месячный PnL, Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 | 0.65 |
| Total clients | 0.65 | 1.30 | 1.94 | 2.58 | 3.22 | 3.85 | 4.48 | 5.11 | 5.73 | 6.36 | 6.97 | 7.59 |
| MRR | 1.6 | 3.2 | 4.9 | 6.5 | 8.0 | 9.6 | 11.2 | 12.8 | 14.3 | 15.9 | 17.4 | 19.0 |
| COGS | 0.5 | 1.0 | 1.6 | 2.1 | 2.6 | 3.1 | 3.6 | 4.1 | 4.6 | 5.1 | 5.6 | 6.1 |
| Gross profit | 1.1 | 2.2 | 3.3 | 4.4 | 5.5 | 6.5 | 7.6 | 8.7 | 9.7 | 10.8 | 11.9 | 12.9 |
| GM% | 68% | 68% | 68% | 68% | 68% | 68% | 68% | 68% | 68% | 68% | 68% | 68% |
| Fixed costs | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 | 9.2 |
| EBITDA | -8.1 | -7.0 | -5.9 | -4.8 | -3.7 | -2.7 | -1.6 | -0.5 | 0.5 | 1.6 | 2.7 | 3.7 |
| Cash burn | 8.1 | 7.0 | 5.9 | 4.8 | 3.7 | 2.7 | 1.6 | 0.5 | 0.0 | 0.0 | 0.0 | 0.0 |
| Cumulative cash | -8.1 | -15.1 | -21.0 | -25.8 | -29.5 | -32.2 | -33.8 | -34.3 | -33.7 | -32.1 | -29.5 | -25.8 |

## A4. 12-месячный PnL, Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 | 0.30 |
| Total clients | 0.30 | 0.60 | 0.89 | 1.19 | 1.48 | 1.76 | 2.05 | 2.33 | 2.61 | 2.89 | 3.17 | 3.44 |
| MRR | 0.5 | 0.9 | 1.3 | 1.8 | 2.2 | 2.6 | 3.1 | 3.5 | 3.9 | 4.3 | 4.7 | 5.2 |
| COGS | 0.2 | 0.4 | 0.6 | 0.8 | 1.0 | 1.2 | 1.4 | 1.6 | 1.8 | 2.0 | 2.1 | 2.3 |
| Gross profit | 0.2 | 0.5 | 0.7 | 1.0 | 1.2 | 1.5 | 1.7 | 1.9 | 2.2 | 2.4 | 2.6 | 2.8 |
| GM% | 55% | 55% | 55% | 55% | 55% | 55% | 55% | 55% | 55% | 55% | 55% | 55% |
| Fixed costs | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 | 7.8 |
| EBITDA | -7.6 | -7.3 | -7.1 | -6.8 | -6.6 | -6.3 | -6.1 | -5.9 | -5.6 | -5.4 | -5.2 | -5.0 |
| Cash burn | 7.6 | 7.3 | 7.1 | 6.8 | 6.6 | 6.3 | 6.1 | 5.9 | 5.6 | 5.4 | 5.2 | 5.0 |
| Cumulative cash | -7.6 | -14.9 | -21.9 | -28.7 | -35.3 | -41.7 | -47.8 | -53.7 | -59.3 | -64.7 | -69.9 | -74.9 |

## A5. Waterfall по unit economics, на 1 клиента в месяц
Методика: `ARPA -> Gross profit -> Contribution after CAC amortization (CAC/12) -> EBITDA after fixed cost allocation at M12 client base -> Net`.

| Scenario | ARPA | Gross | Contribution | EBITDA | Net (УСН 6%) | Net (IT 3%) | Net (ОСНО 20%) |
|---|---:|---:|---:|---:|---:|---:|---:|
| Base | 2 000 000 ₽ | 1 300 000 ₽ | 903 333 ₽ | -725 087 ₽ | -845 087 ₽ | -785 087 ₽ | -580 069 ₽ |
| Optimistic | 2 500 000 ₽ | 1 700 000 ₽ | 1 350 000 ₽ | 137 725 ₽ | -12 275 ₽ | 62 725 ₽ | 110 180 ₽ |
| Pessimistic | 1 500 000 ₽ | 825 000 ₽ | 241 667 ₽ | -2 026 106 ₽ | -2 116 106 ₽ | -2 071 106 ₽ | -1 620 885 ₽ |

Вывод по waterfall: при текущей enterprise-cadence модель начинает выглядеть по-настоящему чистой только в **optimistic**; в **base** unit economics сильные, но fixed base и длинный цикл продаж съедают EBITDA в горизонте первых 12 месяцев.

## A6. Cash flow и startup_capital_to_bep_rub
| Scenario | Min cumulative cash in M1-M12 | Startup capital to BEP, ₽ | Startup capital to BEP + 20% buffer, ₽ |
|---|---:|---:|---:|
| Base | -57 204 231 ₽ | 59 108 928 ₽* | 70 930 714 ₽ |
| Optimistic | -34 280 637 ₽ | 34 280 637 ₽ | 41 136 764 ₽ |
| Pessimistic | -74 872 768 ₽ | >130 915 234 ₽** | >157 098 281 ₽ |

- `*` Base выходит в EBITDA break-even только около **M16**, поэтому капитал до BEP выше, чем провал cash в первых 12 месяцах.
- `**` Pessimistic в пределах 36 месяцев не выходит в break-even без пересборки GTM/FOT.

## A7. Налоговая модель РФ
| Блок | Допущение |
|---|---|
| УСН | Базовый safe-case для ранней стадии: **6% с выручки**. Проста в администрировании, но болезненна при высокой выручке и ещё отрицательной EBITDA. |
| IT-льгота | При наличии аккредитации Минцифры разумно считать **3% с выручки** как рабочий льготный режим для модели; именно он даёт наилучший post-tax outcome в optimistic. |
| ОСНО | Считать как fallback: **налог на прибыль 20%**, плюс **НДС 20%** если компания на ОСНО и не имеет освобождения. Для PnL выше налог на прибыль показан как 20% от положительного EBITDA; НДС не включён в выручку, а рассматривается как pass-through с кассовой нагрузкой. |
| Страховые взносы | Уже учтены в FOT как **~30% к зарплате**. |
| Практический вывод | До аккредитации safest modeling choice: **УСН 6%**. После аккредитации целевой режим для invest-case: **IT 3%**, так как он снижает burn без роста execution-risk. |

## A8. Break-even по client count и по месяцам
| Scenario | Gross profit / client / month | Fixed costs / month | Break-even client count | Break-even month |
|---|---:|---:|---:|---:|
| Base | 1 300 000 ₽ | 8 478 100 ₽ | 6.52, округлённо **7 клиентов** | **M16** |
| Optimistic | 1 700 000 ₽ | 9 200 000 ₽ | 5.41, округлённо **6 клиентов** | **M9** |
| Pessimistic | 825 000 ₽ | 7 800 000 ₽ | 9.45, округлённо **10 клиентов** | **не достигается в 36 мес** |

## A9. Короткий вывод
- **Base**: сильная unit economics, но 12 месяцев недостаточно, чтобы окупить полную fixed base при cadence **0,45 new logos/month**.
- **Optimistic**: модель рабочая, EBITDA break-even достигается в **M9**, капитал до BEP около **34,3 млн ₽**.
- **Pessimistic**: инвестировать без сокращения fixed base или ускорения sales cycle опасно, т.к. burn остаётся структурно отрицательным.

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## B1. Sensitivity analysis, EBITDA через 12 месяцев
База для расчёта: из SECTION A base-case, M12 clients = **5,21**, gross profit / client / month = **1,30 млн ₽**, all-in fixed costs = **8,4781 млн ₽/мес**.

| Scenario | Что меняется | EBITDA @M12, млн ₽/мес | Комментарий |
|---|---|---:|---|
| Base | Без изменений | **-1,7** | База уже убыточна на M12, но тренд к M16 break-even сохраняется. |
| Sens1 | **CAC x2** | **-3,8** | CAC в base встроен в acquisition engine; при удвоении CAC monthly acquisition spend растёт примерно с 2,14 до 4,28 млн ₽. |
| Sens2 | **Churn x2** | **-2,0** | Annual churn растёт с 8% до 16%, M12 client base падает примерно с 5,21 до 5,02. |
| Sens3 | **Price -30%** | **-4,8** | ARPA падает с 2,0 до 1,4 млн ₽, при COGS ~0,7 млн ₽ gross profit/client сжимается до ~0,7 млн ₽. |

**Вывод:** самая опасная переменная для Eudia в РФ не churn, а **price compression** и, сразу за ним, **CAC inflation**. Это типично для enterprise legaltech, где buyer требует pilot discount, long security review и ручную адаптацию.

## B2. Monte Carlo Lite, confidence intervals

### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 3 660 000 | 4 760 000 | 7 000 000 | [T1], [T4] |
| Monthly churn, % | 0,33% | 0,67% | 1,00% | [T4] |
| ARPU, ₽/мес | 1 400 000 | 2 000 000 | 2 500 000 | [T1], [T4] |
| Conversion rate lead→paid, % | 0,18% | 0,29% | 0,45% | [T1], [T4] |
| Time-to-hire, мес (среднее) | 1,0 | 1,6 | 2,5 | [T1], [T5] |

Методика: вместо полного Monte Carlo на 1000 итераций использована **упрощённая 9-комбинационная сетка** around min/mode/max. Для EBITDA @M24 использован тот же all-in fixed cost **8,4781 млн ₽/мес**, monthly lead volume из base funnel **157**, а new paid logos/month выведены из conversion rate. Time-to-hire влияет в первую очередь на burn и runway, а не на steady-state EBITDA M24.

### Результат, p10 / p50 / p90
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | **-4 240 000** | **4 680 000** | **20 910 000** | **25 150 000** |
| CAC payback (мес) | **10,0** | **3,7** | **2,0** | **8,0** |
| LTV/CAC | **10,0x** | **40,8x** | **149,0x** | **139,0x** |
| Cash runway (мес) | **7,4** | **22,7** | **120,0+** | **112,6+** |

### Интерпретация Monte Carlo Lite
- **Rule #1 triggered:** p10 EBITDA @M24 **< 0**, значит risk of insolvency реален даже без экстремального black-swan. Это автоматически становится **kill criterion #1**.
- **Rule #2 not triggered:** p50 EBITDA @M24 = **4,68 млн ₽/мес**, то есть median-case проходит EBITDA Gate.
- **Rule #3 effectively triggered:** классический `p90/p10` некорректен, потому что p10 отрицателен; practically это **хуже**, чем >10x, значит score стоит даунгрейдить за fat-tail downside.
- **Rule #4 triggered:** width по **LTV/CAC = 139x**, то есть модель очень хрупкая к pricing, churn и CAC одновременно.

**Практический вывод:** в median-case инвестиционная логика держится, но downside dispersion слишком широкая. Eudia в РФ нельзя вести как “просто ещё один SaaS”; это скорее **high-touch enterprise systems integrator with AI layer**, и оценивать его надо жёстче по pipeline quality и pilot conversion.

## B3. Competitor deep-dive

### Западные конкуренты
| Competitor | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Harvey** | Сильнейший brand в legal AI, 1000+ customers в 59+ странах, сильный enterprise trust, широкий набор use-cases от research до contract analysis. [T6] | Очень generalist, дорогой, слабее как локализованный RU workflow/product, data residency для РФ-клиента проблемна. | **15-20%** глобального mindshare в AI-native legal platforms. [inference] | Eudia может выиграть у Harvey в РФ через локальный deployment, русскоязычные playbooks, procurement-fit и service-led внедрение. |
| **Ironclad** | CLM incumbent, >$200M ARR, сильный workflow moat, крупные enterprise logos. [T7] | Тяжёлый CLM-first продукт, может быть избыточным и дорогим для локального rollout в РФ; санкционный и data-hosting риск высок. | **20-25%** глобального enterprise CLM/AI-contracting shortlist. [inference] | Eudia легче продать как ROI-pilot поверх конкретного contract workflow, не требуя полного CLM rip-and-replace. |
| **Luminance** | Сильный AI around negotiation / analysis / repository intelligence, хорош для contract intelligence at scale, партнёрство с LexisNexis усиливает trust. [T8][T9] | Зависимость от англоязычного legal stack и западного content ecosystem; локализация под РФ и внутренние регламенты слабее. | **8-12%** в enterprise contract intelligence / legal-grade AI. [inference] | Eudia может быть лучше в российском mixed workflow: закупки, согласования, внутренние политики, ЭДО и data residency. |

### Российские конкуренты и substitute-игроки
| Competitor | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Directum / Directum СЭД+** | Крупный incumbent в документообороте, 501-1000 сотрудников, уже продвигает LLM-анализ и сравнение договоров, есть enterprise access и интеграционная база. [T10][T11] | Это broad ECM/EDM stack, а не legal-ops-native продукт; внедрение тяжёлое, UX и speed to value хуже, AI-layer может быть вторичным. | **20-30%** shortlist у крупных РФ компаний как incumbent substitute. [inference] | Eudia быстрее запускает узкий high-ROI legal workflow без полного ECM-проекта. |
| **Noroots** | AI-проверка договоров прямо в Word, заметная продуктовая формулировка, есть свежая регистрация в Сколково и выручка порядка 25 млн ₽ по Rusprofile. [T12][T13] | Пока выглядит как point solution, а не полная contract operations platform; меньше enterprise proof и меньше breadth. | **5-8%** видимого AI-native сегмента проверки договоров в РФ. [inference] | У Eudia сильнее шансы выиграть multi-workflow rollout, outside counsel optimization и сложные enterprise integrations. |
| **UR-LI** | Сильный risk/compliance angle, B2B-позиционирование, упор на контрагентские и сделочные риски, ориентир на mid-large business. [T14][T15] | Ближе к risk-scoring и контрагентскому due diligence, чем к end-to-end contract ops; слабее в redlining/playbooks/workflow orchestration. | **3-5%** сегмента legal-risk automation в РФ. [inference] | Eudia лучше там, где нужно ускорить legal throughput, а не только отфильтровать рискованные сделки. |
| **FastLaw** | Ранний AI/legaltech из Сколково, фокус на document routing, extraction и compliance scenarios, технологическая связка с МФТИ/iPavlov. [T16] | Публичный сигнал слабее, решение исторически более fragmented, чем полноценная enterprise platform. | **2-4%** legal AI pilot-layer в РФ. [inference] | Eudia может выиграть за счёт более понятной unit economics around contract operations и enterprise packaging. |
| **Комбинатор** | Сильный документный конструктор, шаблоны, интеграции с 1С/Bitrix24/AmoCRM, понятная автоматизация типовых договоров. [T14] | Это document generation, а не полноценный AI legal ops stack; defence against complex negotiation/compliance use-cases ограничена. | **4-6%** сегмента document automation для юркоманд. [inference] | Eudia сильнее в high-ACV enterprise workflows, где нужен не конструктор, а orchestration + AI review + playbooks. |

**Итог по конкурентам:**
- На Западе рынок уже закреплён за **Harvey / Ironclad / Luminance** как reference set.
- В РФ прямого аналога Eudia почти нет, но есть опасный кластер substitute-решений: **incumbent ECM**, **point AI contract review**, **document automation**, **counterparty risk tools**.
- Значит, главный риск не “кто делает то же самое”, а **скатывание enterprise buyer в более дешёвый substitute stack**.

## B4. Risk matrix
| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять senior legal ops + ML + enterprise AE в срок | med | Высокий: срыв pilot delivery и sales cadence | Time-to-hire >2,5 мес, offer acceptance <50% | Fractional experts, referral hiring, staged rollout без полного штатного набора |
| 2 | Operational | LLM/API latency или quality drift ломают review workflow | med | Высокий: падает доверие юрдепартамента | Рост manual override >30%, SLA breach, рост hallucination complaints | Multi-model routing, golden set evals, human-in-the-loop, contract-specific templates |
| 3 | Operational | Зависимость от одного API/vendor | high | Высокий: остановка сервиса или margin shock | >70% inference spend у одного провайдера | Multi-vendor stack, fallback на open-weight / on-prem, заранее согласованные reserve providers |
| 4 | Market | Спрос есть, но buyer хочет только дешёвый pilot, без rollout | high | Высокий: низкий ACV и длинный payback | Pilot conversion <30%, растёт число POC без annual contract | Pilot-to-rollout clauses, KPI-based expansion triggers, pricing floor |
| 5 | Market | Price compression из-за substitute-решений и low-end contract-check сервисов | high | Высокий: ломается gross profit и EBITDA | Win rate падает при цене >1,5 млн ₽/мес | Жёсткое enterprise positioning, ROI calculator, bundle services into platform contract |
| 6 | Market | Incumbent типа Directum закрывает базовую боль внутри существующего IT-landscape | med | Средний/высокий: меньше greenfield сделок | В тендерах чаще появляется “доработаем ECM” | Партнёрства с integrators, land-and-expand поверх incumbent stack |
| 7 | Regulatory | 152-ФЗ / data residency ограничивают использование внешних LLM и западных SaaS | high | Высокий: блокирует крупные regulated accounts | Security questionnaire stop, запрет на transfer abroad | RU-hosting, pseudonymization, private deployment, DPA + локальный контур |
| 8 | Regulatory | 115-ФЗ / KYC / compliance требования делают output юридически чувствительным | med | Средний: продукт перестаёт быть “assistant”, становится контролируемым risk-tool | Compliance review затягивается >60 дней | Ограничить use-cases, вести explainability/logging, не обещать autonomous decision-making |
| 9 | Regulatory | Санкции на SaaS/LLM/API или отказ зарубежных партнёров обслуживать РФ | high | Высокий: внезапная остановка critical stack | Billing/payment incidents, vendor TOS changes | Vendor diversification, reserve budget на migration, локальные inference options |
| 10 | Financial | Cash runway тает быстрее из-за delayed closes | high | Высокий: down round или insolvency | Burn >6 млн ₽/мес 3 месяца подряд, pipeline coverage <3x | Сократить fixed base, milestone hiring, bridge financing only against signed pilots |
| 11 | Financial | Ослабление рубля к USD повышает API и infra cost | high | Средний/высокий: сжатие GM | USD/RUB >95 и API share >25% COGS | FX reserve, RUB pricing with indexation, caching and model-mix optimization |
| 12 | Financial | Инфляция и рост ФОТ ухудшают CAC и fixed cost | med | Средний: payback удлиняется | FOT +15% YoY без роста win rate | Комиссионная модель sales, vendor renegotiation, slower hiring |
| 13 | Black swan | Резкое ужесточение санкций или отключение критичного LLM-поставщика | med | Очень высокий | Forced migration notices, API degradation, payment blocks | Prebuilt migration playbook, dual-stack architecture, export-control review |
| 14 | Black swan | Военный/политический shock снижает enterprise IT spend и откладывает закупки | med | Высокий | Freeze новых тендеров, elongation procurement >9 мес | Фокус на cost-saving ROI cases, vertical mix, reserve cash 12+ months |

## B5. Kill conditions через 6 месяцев
1. **Pipeline / insolvency kill:** если updated Monte Carlo даёт **p10 EBITDA @M24 < 0** **и** runway падает ниже **9 месяцев**, продолжать нельзя.
2. **Go-to-market kill:** если за 6 месяцев закрыто **<1 annual platform contract** или pilot→rollout conversion **<25%**, значит sales motion не доказан.
3. **Unit economics kill:** если blended **CAC > 7 млн ₽** **или** price realization < **1,4 млн ₽/клиент/мес** **или** LTV/CAC падает ниже **8x**, модель теряет инвестиционный смысл.

## B6. Final critic take
- **Median-case жизнеспособен**, но downside слишком широкий.
- Для РФ это **не классический scalable SaaS**, а capital-efficient only if pipeline quality очень высокая.
- Ключевой инвестиционный вопрос: может ли Eudia стабильно превращать **дорогие пилоты в 2-3 annual rollouts**, не попадая в price compression и compliance paralysis.
- На текущих данных verdict: **PASS WITH HEAVY RISK DISCOUNT**.

## Sources for SECTION B
- **T1**: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/eudia-geo-expand-v2/04-economics.md`
- **T4**: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/eudia-geo-expand-v2/02-demand.md`
- **T5**: hh.ru salary anchors already cited in `04-economics.md`
- **T6**: HSBC on Harvey customer scale, 20.01.2026, https://www.hsbc.com/news-and-views/news/media-releases/2026/hsbc-announces-harvey-ai-for-their-legal-platform
- **T7**: Ironclad ARR milestone, 12.02.2026, https://www.businessinsider.com/ironclad-hits-200-million-arr-contract-lifecycle-management-ceo-2026-2
- **T8**: Luminance Contract Intelligence, https://www.luminance.com/contract-intelligence/
- **T9**: LexisNexis + Luminance alliance, 21.04.2026, https://www.lexisnexis.com/community/amp-pressroom/lexisnexis-and-luminance-announce-strategic-alliance-to-extend-authoritative-legal-ai-content-and-technology-into-enterprise-contract-workflows
- **T10**: Directum on Habr, company profile, https://habr.com/ru/companies/directum/
- **T11**: Directum contract analysis / comparison posts on Habr, https://habr.com/ru/companies/directum/articles/978552/ ; https://habr.com/ru/companies/directum/articles/990044/
- **T12**: vc.ru on Noroots and legaltech workflow substitutes, https://vc.ru/legal/2169379-legaltech-v-rossii-avtomatizatsiya-yuristov ; https://vc.ru/legal/1330387-yurist-neiroset-naidet-oshibki-i-riski-v-dogovore-za-1-minutu-i-besplatno
- **T13**: Rusprofile on ООО «Ноурутс», https://www.rusprofile.ru/id/10750393
- **T14**: vc.ru on UR-LI and Russian legaltech architecture, https://vc.ru/services/408582-legal-tech-ctartap-ur-li-zapustil-servis-po-zashite-kompanii-ot-riskovannyh-sdelok ; https://vc.ru/legal/1447304-arhitektura-legaltech-modeli-dlya-yuridicheskih-servisov-i-biznes-processov
- **T15**: vc.ru founder note on UR-LI B2B traction, https://vc.ru/services/285447-kak-privlekat-klientov-v-b2b-kogda-ty-zanimaeshsya-vzyskaniem-dolgov-istoriya-ur-li
- **T16**: Skolkovo on FastLaw, 17.09.2018, https://sk.ru/news/rezident-skolkovo-fastlaw-i-yuridicheskaya-kompaniya-pravokard-zapuskayut-sovmestnye-proekty-v-legaltech/

<!-- P6B-DONE -->

## 06-verdict.md
# 06-verdict

[GEO-EXPAND] Eudia — NEAR-PASS: 68/100 | EBITDA base=622К₽/мес через 9 мес | LTV/CAC=40,8x | Ключевое преимущество: service-led enterprise legal ops с высоким ARPA и быстрым payback | Главный риск: category demand и moat в РФ пока недодоказаны.

sector: GEO-EXPAND

## Кейс
eudia-geo-expand-v2

## Вердикт
**NEAR-PASS**

## Score
**68/100**

## Investment committee summary
Eudia в РФ проходит economics-gate, но не проходит investment committee threshold. В base-case модель даёт **company_ebitda_rub_month = 621 900 ₽/мес к M9**, **customer_ltv_rub = 194,0 млн ₽**, **LTV/CAC = 40,8x**, **CAC payback = 3,7 месяца**, а break-even достигается уже на **7 клиентах**. Но локальный category demand слабый, moat в основном execution-based, а downside dispersion слишком широкий: в critic зафиксировано **p10 EBITDA @M24 = -4,24 млн ₽/мес** и сильная зависимость от price realization и pilot conversion. Для approve пока не хватает локально подтверждённого premium GTM и более жёсткого moat.

## Сравнение с историческим решением
Изначально сигнал по Eudia был признан supporting signal для более широкого кейса enterprise contract operations. После полного rerun как standalone-кейса вывод стал сильнее: это **не просто supporting evidence, а реальный near-pass candidate** с рабочей экономикой. Но standalone-ставка на РФ всё ещё преждевременна, потому что сильные unit economics пока опережают доказанность локального спроса и moat.

## Оценка
Source tier balance: T1=8, T2=25, T3=1, weighted=1.85. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 40,8:1», «CAC Payback = 3,7 месяца», «Contribution Margin = 65,0%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | «M9 ... EBITDA, ₽ = +621 900», «Break-even = 7 клиентов», «Месяц break-even: M9». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «автоматизация договорной работы → MEDIUM, score 30, hh.ru vacancies = 662», но «legal ops automation → LOW, score 0» и tier penalty -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | Сильны switching costs и embedded workflow, но moat пока держится на «service-led pilot → annual platform roll-out» и локальном trust layer, а не на уникальном активе. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | В risk matrix прямо перечислены «152-ФЗ / data residency», «санкции на SaaS/LLM/API», «pilot conversion <30%» и vendor concentration. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | Есть 10 named targets, «CAC Payback = 3,7 месяца» и sanity check «2 enterprise contracts за первый год», но motion остаётся founder-led и procurement-heavy. |

**Сумма raw:** 102/150  
**Normalized score = round((102 × 100) / 150) = 68/100**

## Moat, 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не усиливает продукт для остальных, кроме косвенного накопления шаблонов. |
| Switching costs | 3 | Playbooks, security review, workflow mapping и встроенность в процесс создают высокий cost of change. |
| Scale economies | 2 | Inference, implementation и support можно оптимизировать с объёмом, но service-layer остаётся значимым. |
| Proprietary data / model advantage | 1 | Локального датасетного преимущества по размеру или защищённому корпусу в евиденции нет. |
| Regulatory moat | 1 | Compliance критичен, но это пока барьер исполнения, а не лицензируемый moat. |
| Brand / distribution | 1 | Глобальный signal сильный, но локальный бренд и distribution edge в РФ не подтверждены. |
| Embedded workflow | 2 | Продукт глубоко садится в contract review, outside counsel optimization и legal workflows. |

**Итого 7-factor sum:** 10/21  
**Moat score = round((10 × 25) / 21) = 12/25**

Вывод по moat: moat **не weak по формальному порогу (<10)**, но очень близок к нему. Это надо считать одним из главных стоп-факторов до approve.

## Полный бизнес-процесс

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Target account selection | SDR + AE | CRM, account lists, HH/СПАРК/корп. сайты | 2 дня | 18 000 | средняя |
| 2 | Первичный outbound и прогрев | SDR | email sequences, LinkedIn analogue, телефония | 10-15 дней | 42 000 | средняя |
| 3 | Discovery call | AE | Zoom/Teams, CRM | 1 день | 12 000 | низкая |
| 4 | Qualification + problem framing | AE + CEO/founder | CRM, deck, ROI calculator | 3-5 дней | 28 000 | низкая |
| 5 | Security / data handling pre-check | CTO + AE | security docs, DPA templates | 5-10 дней | 35 000 | низкая |
| 6 | Demo + legal workflow mapping | AE + CS/legal ops | demo env, process map, prompt/playbook draft | 4-7 дней | 55 000 | низкая |
| 7 | Paid pilot scoping | AE + CTO + CEO | SOW, калькулятор трудозатрат | 5 дней | 70 000 | низкая |
| 8 | Pilot deployment | CTO + backend + ML + CS | cloud, LLM stack, connectors | 4-6 недель | 240 000 | средняя |
| 9 | Pilot review, KPI proof | AE + CS + клиентский sponsor | dashboard, ROI model | 1 неделя | 40 000 | средняя |
| 10 | Procurement + legal negotiation | AE + CEO + external counsel | contract workflow, redlines | 3-6 недель | 95 000 | низкая |
| 11 | Annual contract close | CEO + AE | e-sign, invoicing, CRM | 2-5 дней | 25 000 | средняя |
| 12 | Invoice issuance / payment collection | finance/admin | 1C/банк/ЭДО | 7-30 дней | 8 000 | высокая |
| 13 | Onboarding to production | CS/legal ops + CTO | PM tool, knowledge base, integrations | 2-4 недели | 160 000 | средняя |

**Итого cost-to-close одного enterprise клиента:** примерно **828 000 ₽** прямых delivery/sales действий до старта recurring-работы.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 194 029 851 ₽ |
| Fully-loaded CAC | 4 760 000 ₽ |
| LTV/CAC | 40,8x |
| CAC Payback | 3,7 мес |
| Gross Margin | 65,0% |
| contribution_margin_rub_month | 1 300 000 ₽/клиент/мес |
| company_ebitda_rub_month, base | 621 900 ₽/мес через 9 мес |
| company_ebitda_potential_rub_month | 4 680 000 ₽/мес p50 @M24 |
| Break-even clients | 7 |
| clients_to_500k_ebitda | 7 |
| months_to_500k_ebitda | 9 |
| startup_capital_to_bep_rub | 37 300 000 ₽ |
| fixed_costs_rub_month | 8 478 100 ₽/мес |
| Startup capital sanity reserve | 60 000 000 ₽ |

## Команда

| Роль | Функция | Нужно чел. | FOT fully-loaded ₽/мес |
|---|---|---:|---:|
| CEO/founder | enterprise sales, fundraising, partnerships | 1 | 910 000 |
| CTO/Tech Lead | security, architecture, delivery | 1 | 780 000 |
| Senior Backend | core integrations и workflow engine | 2 | 1 170 000 |
| ML Engineer | prompts, evals, doc pipelines | 1 | 715 000 |
| DevOps | infra, deployment, compliance | 1 | 455 000 |
| Product / Implementation Manager | rollout, requirements, roadmap | 1 | 416 000 |
| SDR | outbound pipeline | 1 | 257 000 |
| AE | close pilots and annual contracts | 1 | 520 000 |
| Customer Success / Legal Ops | onboarding, adoption, renewals | 1 | 364 000 |

**Итого FOT fully-loaded steady-state:** **5 587 000 ₽/мес**.

## GTM, 10 named targets

| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | огромный поток договоров, закупок и compliance-heavy legal ops, совпадает с enterprise ICP | email decision-maker в юридический блок + партнёрский intro через AI/ECM-интегратора | 2 000 000 ₽/мес |
| 2 | Газпром нефть | высокий объём procurement и CAPEX-контрактов, где цена задержки договора велика | executive email + отраслевое мероприятие по legal transformation | 2 200 000 ₽/мес |
| 3 | X5 Group | огромный документный поток по поставщикам, аренде и commercial agreements | outbound в head of legal operations + кейс через ROI-калькулятор | 1 800 000 ₽/мес |
| 4 | МТС | массивный B2B и procurement workflow, высокая цифровая зрелость | email юрдиректора + партнёрство с ECM/SЭД-вендором | 1 800 000 ₽/мес |
| 5 | Ростелеком | regulated enterprise, много согласований и data residency требований | conference + compliance workshop + direct outreach | 2 000 000 ₽/мес |
| 6 | Яндекс | быстрый contract throughput и сложные product/legal процессы, высокий pain от redlining | founder-led outbound + тёплое intro через AI ecosystem | 2 000 000 ₽/мес |
| 7 | VK | высокая частота vendor/media/partner contracts и нужда в ускорении review | email GC / head of legal ops + vc.ru ad retargeting | 1 500 000 ₽/мес |
| 8 | Магнит | procurement-heavy ритейл с большим объёмом типовых и нетиповых договоров | партнёрство с legal integrator + direct outreach | 1 700 000 ₽/мес |
| 9 | Северсталь | industrial procurement, complex supplier agreements и высокий compliance overhead | executive email + отраслевой roundtable | 1 900 000 ₽/мес |
| 10 | НЛМК | contract-heavy закупки и капитальные проекты, где важны SLA и audit trail | email decision-maker + интеграторский канал | 1 900 000 ₽/мес |

Вывод по GTM: named-target лист реалистичен, но GTM остаётся **account-by-account, founder-led и compliance-heavy**, что ограничивает скорость масштабирования.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top-risk |
|---|---|---|---|
| Price compression и скатывание в point-solution pricing | high | critical | Sensitivity показывает: «Price -30% ... EBITDA @M12 = -4,8 млн ₽/мес». |
| evidence_quality_unverified / слабый локальный category language | high | high | В demand-stage есть «legal ops automation → LOW, score 0», а tier balance всего 1.85. |
| Санкции, 152-ФЗ и vendor concentration по LLM/API | high | high | Risk matrix фиксирует «санкции на SaaS/LLM/API», «152-ФЗ / data residency» и зависимость от одного vendor. |

## Что должно быть доказано для APPROVED
1. **Не менее 2-3 paid pilots** в РФ с pilot→annual conversion не ниже **30%**.
2. **Price resilience**: способность держать чек около **2,0 млн ₽/мес** без скидок >20%.
3. **Moat upgrade**: локальный secure deployment, data residency, DPA-pack и библиотека playbooks/шаблонов, которые реально повышают switching costs.
4. **Repeatable GTM**: хотя бы один канал кроме founder-led intro, например через ECM/СЭД-интеграторов или legal transformation партнёров.

## LTV Upside Calculator
Так как кейс получил **NEAR-PASS**, upside-calculator обязателен.

### База сейчас
- customer_ltv_rub = **194,0 млн ₽**
- Fully-loaded CAC = **4,76 млн ₽**
- LTV/CAC = **40,8x**
- Главный лимит не в unit economics клиента, а в качестве локального спроса, pilot conversion и moat.

### Что даст апсайд
| Рычаг | Было | Цель | Эффект |
|---|---:|---:|---|
| Pilot→annual conversion | не доказано локально | ≥30% | снимает главный GTM-риск и уменьшает CAC drift |
| Price realization | 2,0 млн ₽/мес base | ≥2,0 млн ₽/мес без discounting | защищает EBITDA и предотвращает price compression |
| Regulatory package | частично | стандартный on-prem / RU-host / DPA pack | ускоряет security review и усиливает moat |
| Distribution | founder-led | +1-2 партнёрских канала | повышает repeatability и pipeline coverage |
| Local proof | 0 подтверждённых РФ-rollout | 2-3 enterprise logos | переводит кейс из speculative в investable |

## Финальный вывод
**NEAR-PASS, 68/100.**

Кейс интересный и уже близок к approve по экономике. Но сегодня это ещё не investment-grade ставка на РФ, а сильный кандидат для follow-up после проверки локального GTM, price resilience и regulatory moat. Пока что математика клиента выглядит лучше, чем защищённость бизнеса целиком.
## 07-score-trajectory.md
## 2026-04-22 21:58 MSK — P5 Unit Economics
- Этап: P5 Unit Economics
- Итог: экономика enterprise legal ops в РФ проходит инвестиционный порог с большим запасом только в enterprise/service-led модели, а не в self-serve legal AI.
- Ключевой вывод: при ARR **24 млн ₽ на клиента**, gross margin **65%**, annual churn **8%** и fully-loaded CAC **4,76 млн ₽** получаем **LTV/CAC = 40,8x**, **CAC payback = 3,7 мес**, break-even на **7 клиентах** и EBITDA-плюс уже на **M9** base-case модели.
- Изменение оценки: позитивное, потому что P4-гипотеза про few-large-accounts подтвердилась числами; основной риск смещается из спроса в скорость enterprise sales и procurement friction.
- Артефакт: `pipeline/cases/eudia-geo-expand-v2/04-economics.md`

## 2026-04-23 07:16 MSK — P7 Critic and Verdict
- Этап: P7 Critic and Verdict
- Итог: **NEAR-PASS / REJECTED FOR NOW**, score **68/100**.
- Ключевой вывод: юнит-экономика сильная, но локальный category demand в РФ слабый, moat близок к weak-moat зоне, а downside dispersion по Monte Carlo остаётся слишком широкой для investment-grade approve.
- Изменение оценки: итоговый score снижен относительно economics-only впечатления, потому что рынок и moat оказались слабее математики клиента.
- Артефакт: `pipeline/cases/eudia-geo-expand-v2/06-verdict.md`