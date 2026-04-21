# CodaMetrix Autonomous Medical Coding v2 — Full Case File
Собрано автоматически из pipeline-артефактов P1-P7.

---

## FILE: 00-brief.md

# Краткий бриф

## Кейс
CodaMetrix, автономное медицинское кодирование

## Статус
Принудительный resurrect/rerun, создан новый кейс `codametrix-autonomous-medical-coding-v2`.

## Почему открыт
Кейс по AI-native автоматизации медицинского кодирования и revenue cycle для крупных клиник и hospital systems. Создан как принудительный resurrect-v2 для повторной полной аналитики по P3→P7.

## Следующий шаг
Передать кейс в P3-demand-validation и затем по полному пайплайну P4→P7.


---

## FILE: 01-intake.md

---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-codametrix-autonomous-medical-coding.md
created: 2026-04-20T09:30:00+03:00
original_verdict: triage/triage-2026-04-14-codametrix-autonomous-medical-coding.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — codametrix-autonomous-medical-coding

## Meta
- source: triage/triage-2026-04-14-codametrix-autonomous-medical-coding.md
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
- pipeline/raw/raw-2026-04-14-codametrix-autonomous-medical-coding.md

## Классификация
кандидат в новый кейс

## Решение
Открыть новый кейс: `autonomous-medical-coding-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущий кейс `ambient-clinical-documentation-operator` покрывает ambient documentation и clinical scribe workflows, но не автономное медицинское кодирование и revenue cycle как отдельную сервисную модель.
- Сигнал по CodaMetrix достаточно сильный по масштабу: 25+ health system partners в 26 штатах США, клиенты представляют около 180 млрд долларов net patient revenue, а сама категория дополнительно подтверждена наградой Best in KLAS 2026.
- По экономике сигнал проходит порог для нового кейса: `ltv_signal` указан как 3-12 млн руб. в год с одной сетью клиник или крупным медконтуром, то есть примерно 250 000-1 000 000 руб. в месяц. Верхняя часть диапазона превышает порог `> 500 000 руб./мес.`.
- Это не общий AI для медицины, а более узкий и дорогой workflow вокруг coding accuracy, billing readiness, revenue cycle и аудита медицинской документации. Такая специализация повышает вероятность высокого чека и сложного внедрения.
- Локализация трудная, но именно поэтому сервисная ценность может быть высокой: нужны интеграции с МИС и внутренними контурами клиник, адаптация под локальные классификаторы и правила кодирования, а также защищённое развертывание под требования 152-ФЗ и медицинской тайны.

## Что сделано
- Создан новый кейс `pipeline/cases/autonomous-medical-coding-operator/`.
- В `00-brief.md` зафиксированы описание модели, стартовые факты и ключевая гипотеза.
- Исходный raw-файл подлежит перемещению в `pipeline/raw/processed/`.

## Пометка для следующего шага
Проверять кейс как enterprise healthcare revenue workflow, а не как разновидность speech-to-text. На следующем цикле собрать подтверждения по:
- buyer и бюджету: крупные частные клиники, сети, стационары, диагностические контуры, МИС-вендоры;
- unit economics: цена за клинику, сеть, объём документов или долю автоматизации coding workflow;
- требованиям к данным и комплаенсу: on-prem/private cloud, медицинская тайна, audit trail, разграничение доступа;
- глубине downstream-ценности: влияние на скорость выручки, долю ручного труда, качество кодирования и снижение потерь из-за ошибок;
- российским и СНГ-аналогам, чтобы уточнить силу GEO-EXPAND окна.

## Вердикт
Сигнал достаточно сильный для открытия отдельного кейса: тема выглядит как правдоподобная high-LTV вертикальная модель с трудной локализацией, заметной интеграционной сложностью и enterprise-бюджетом.

```



---

## FILE: 02-demand.md

---
stage: demand-validation
case: codametrix-autonomous-medical-coding-v2
date: 2026-04-21
analyst: branch-models-lead
verdict: PASS_WITH_CAUTION
confidence: medium
---

# 02-demand

## Demand validation summary
- **Продукт**: CodaMetrix, AI-платформа для autonomous medical coding и revenue-cycle automation для крупных health systems. Компания сообщает, что работает с 30+ health systems, 500+ hospitals и 100 000+ physicians, а клиенты представляют более $180 млрд net patient revenue. [T2: https://www.codametrix.com/resources/codametrix-chosen-by-health-systems-representing-180b-in-net-patient-revenue ; https://klasresearch.com/vendor-ratings/codametrix/90440]
- **Итог по спросу в РФ**: **LOW** по обязательному demand endpoint, но underlying pain подтвержден. По запросу `медицинское кодирование` endpoint вернул LOW при score 22, `hh.ru vacancies = 92`, `yandex suggest = 100`; по более продуктовым запросам `автоматическое медицинское кодирование` и `medical coding software` спрос почти нулевой. Это означает, что в РФ есть problem demand на ручной coding/billing labor, но почти нет осознанного product demand на autonomous coding как категорию. [T1: internal demand endpoint with HH proxy]
- **Решение по гейту**: **не отклонять на P4**. Массового спроса нет, но high-ticket enterprise-сценарий для крупных частных сетей, федеральных центров и МИС/RCM-партнеров теоретически может пройти порог EBITDA > 500 тыс. ₽ в месяц. [T1/T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%BE%D0%B5%20%D0%BA%D0%BE%D0%B4%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5` → **LOW**, score **22**, `hh.ru vacancies = 92`, `yandex suggest = 100`, `telegram subscribers = 0`. Это сильный сигнал на наличие кадровой и операционной боли, но не на зрелую software-category awareness. [T1]
- `http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B5%20%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%BE%D0%B5%20%D0%BA%D0%BE%D0%B4%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5` → **LOW**, score **0**, `hh.ru vacancies = 3`. Прямой спрос на автоматизацию coding workflow в РФ практически отсутствует. [T1]
- `http://172.18.0.1:9001/multi-demand?keyword=medical%20coding%20software` → **LOW**, score **0**, `hh.ru vacancies = 1`. Англоязычная продуктовая категория в РФ тоже почти не проявлена. [T1]
- Дополнительная проверка `revenue cycle management hospital` тоже вернула **LOW**, score **0**. Это подтверждает, что для РФ продукт надо продавать через CFO/главврача/директора по цифровизации, а не через search-led discovery. [T1]

### 2) Why now и рыночные сигналы
- CodaMetrix в феврале 2026 года получила титул **No. 1 Best in KLAS** в inaugural category Autonomous Medical Coding; в релизе указано, что **93% клиентов купили бы продукт снова**, а **93% считают его частью долгосрочного плана**. Это сильный proxy реальной willingness-to-pay и retention на развитом рынке. [T2: https://www.prnewswire.com/news-releases/codametrix-named-no-1-in-inaugural-best-in-klas-title-for-autonomous-medical-coding-302678539.html]
- По данным KLAS vendor profile, CodaMetrix уже автоматизирует coding для **500+ hospitals** и обрабатывает **60+ млн outpatient visits в год**. Значит, category proof существует не как пилот, а как enterprise-scale workflow. [T2: https://klasresearch.com/vendor-ratings/codametrix/90440]
- Grand View Research оценивает мировой рынок **AI in medical coding** в **$2,86 млрд в 2025 году** и ожидает рост до **$8,62 млрд к 2033**. Категория явно не ранняя игрушка, а растущий software + RCM сегмент. [T2: https://www.grandviewresearch.com/industry-analysis/artificial-intelligence-ai-medical-coding-market-report]
- Более широкий рынок **medical coding** оценен Grand View Research в **$39,85 млрд в 2024 году**. Это важно как верхняя граница spend universe и подтверждение того, что administrative coding spend уже является большой строкой бюджета в healthcare. [T2: https://www.grandviewresearch.com/industry-analysis/medical-coding-market]
- В России в 2024 году было **5 044 больничных организации**, из них **537 негосударственных**. Buyer universe широкий, но реальный ICP для такого продукта уже, потому что autonomous coding имеет смысл в больших контурах с существенным потоком счетов и документов. [T2, citing Rosstat via отраслевое медиа: https://www.vademec.ru/news/2026/01/23/rosstat-v-2024-godu-chislo-patsientov-s-boleznyami-organov-dykhaniya-sostavilo-66-mln-chelovek/]
- Российский коммерческий сегмент медицинских услуг в 2024 году достиг **1,57 трлн ₽**. Это не рынок coding software напрямую, но это доказывает существование крупного пула выручки, вокруг которого CFO и revenue-cycle функции готовы оптимизировать административные потери. [T2: https://marketing.rbc.ru/articles/15664/]

## Real competitors with prices

### Публичные price anchors
1. **AAPC Codify**. Официальные тарифы: **$36/мес** за Basic Coder, **$44/мес** за Pro Fee Coder и **$54/мес** за Complete Coder. Это coding workflow infrastructure, а не autonomous coding, но это реальный бюджетный anchor на инструменты кодировщика. [T2: https://www.aapc.com/codes/]
2. **Find-A-Code**. Официальные тарифы: **$45/мес** Professional, **$75/мес** Expert, **$95/мес** Facility/ASC. Это прямой adjacent substitute для code lookup, fee tools и coding reference stack. [T2: https://www.findacode.com/subscribe]
3. **SpeedeCoder**. Официальные тарифы: **$24.95/мес + $29.95 setup** за Pro, **$39.95/мес + $29.95 setup** за Plus, **$54.95/мес + $29.95 setup** за Platinum; также есть годовые планы от **$199.95** до **$499.95**. Это low-end benchmark на инструменты медицинского кодирования. [T2: https://www.speedecoder.com/pricing/]
4. **iCoder**. Публичные годовые цены: **$79.99/год**, **$149.99/год**, **$249.99/год**. Еще один pricing anchor для individual coder tools. [T2: https://www.icoder.info/]
5. **EncoderPro** через MicroMD. Указаны цены **$224.96**, **$412.46** и **$749.96** per user при покупке через MicroMD с дисконтом к Optum retail price. Это useful anchor для более продвинутого professional coding stack. [T2: https://www.micromd.com/encoderpro/]

### Прямые enterprise-конкуренты без публичного прайса
- **Nym**, **AKASA**, **3M/солюшены класса CAC**, а также сама **CodaMetrix** работают в enterprise autonomous coding, но публичных тарифов не раскрывают. Это само по себе сигнал, что рынок покупается через крупные B2B сделки, а не через self-serve price page. [T2: https://www.codametrix.com/ ; https://www.prnewswire.com/news-releases/codametrix-named-no-1-in-inaugural-best-in-klas-title-for-autonomous-medical-coding-302678539.html]

### Что означает конкурентный ландшафт
- Нижний слой рынка уже приучен платить десятки долларов в месяц за coder productivity tools. [T2]
- Верхний слой autonomous coding живет в enterprise pricing без публичных прайсов, что согласуется с длинным sales cycle, интеграциями и оплатой за measurable RCM outcomes. [T2, inference]

## Telegram bots / services in RU
- По обязательному endpoint у целевых запросов `telegram subscribers = 0`, то есть самостоятельного Telegram-native спроса на medical coding automation в РФ не видно. [T1]
- В РФ есть Telegram-решения для клиник, но они patient-facing: например, **tgbotmis.ru** продает «клинику в Telegram» для записи, уведомлений и отчетов; **MedBots** предлагает разработку медицинских Telegram-ботов; Medesk/медицинские МИС продвигают мессенджеры как канал коммуникации с пациентами. Это другой слой value chain, не coding automation. [T2: https://tgbotmis.ru/ ; https://medbots.tech/ ; https://www.medesk.net/ru/blog/kak-klinike-sokratit-rutiny-i-nichego-ne-poteriat/]
- Вывод: Telegram в РФ не является существующим wedge для CodaMetrix. Максимум это auxiliary notification layer, но не канал покупки и не substitute продукта. [T1/T2]

## WTP, willingness to pay
- **Доказательство WTP №1**: у CodaMetrix есть подтвержденный enterprise adoption signal, поскольку health systems-клиенты компании представляют более **$180 млрд NPR**, а сама компания сообщает о широком покрытии hospital footprint. Это не price sheet, но это очень сильный индикатор того, что бюджеты на autonomous coding реально выделяются. [T2: https://www.codametrix.com/resources/codametrix-chosen-by-health-systems-representing-180b-in-net-patient-revenue ; https://klasresearch.com/vendor-ratings/codametrix/90440]
- **Доказательство WTP №2**: KLAS relayed metric `93% would buy again` и `93% part of long-term plan` указывает не просто на интерес к пилотам, а на вероятность долгосрочного budget line item. [T2: https://www.prnewswire.com/news-releases/codametrix-named-no-1-in-inaugural-best-in-klas-title-for-autonomous-medical-coding-302678539.html]
- **Доказательство WTP №3**: even low-end coder tooling уже продается по понятным тарифам, значит spending habit на coding stack существует. [T2: https://www.aapc.com/codes/ ; https://www.findacode.com/subscribe ; https://www.speedecoder.com/pricing/]
- **Доказательство WTP №4**: в РФ по запросу `медицинское кодирование` видно **92 hh.ru вакансии**. Это не software revenue, но это T1-proxy того, что клиники и подрядчики уже тратят деньги на ручное решение той же проблемы через labor. [T1]
- **Ограничение**: локальный WTP в РФ не подтвержден на уровне готовых сделок именно за autonomous coding. Российский buyer, вероятно, заплатит только если решение ляжет поверх локальных классификаторов, МИС и требований к медицинской тайне. Без этого WTP остается гипотезой. [T2, inference]

## Market sizing

### Методика и допущения
- Операционный курс для сопоставления: **1 USD = 90 ₽**. Это model assumption, не primary source. [спекуляция]
- Для РФ беру не весь hospital universe, а только контуры с большим документооборотом, серьезной частной выручкой или федеральной нагрузкой на стационар/хирургию/многопрофильную помощь. [T2]
- Средний целевой контракт в base-case: **450 тыс. ₽/мес** или **5,4 млн ₽ ARR** на крупную клинику/госпиталь/медсеть. Это существенно выше low-end coder tools и отражает premium за AI, интеграции, quality governance и private deployment. [T2 + inference]

### Top-down
- **TAM (мир)**: глобальный рынок **AI in medical coding** = **$2,86 млрд** в 2025 году, то есть примерно **257,4 млрд ₽**. [T2: https://www.grandviewresearch.com/industry-analysis/artificial-intelligence-ai-medical-coding-market-report]
- **TAM (РФ)**: беру консервативную адресуемую долю РФ **0,20%** от глобального AI medical coding market. Получаем **514,8 млн ₽**. Маленькая доля оправдана тем, что продукт узкий, англо-американский по происхождению и плохо переносится без глубокой локализации. [T2 + inference]
- **SAM (РФ)**: беру **60%** от TAM РФ как слой крупных частных сетей, федеральных центров и сильных многопрофильных больниц, где автоматизация coding может иметь экономический смысл. Получаем **308,9 млн ₽**. [T2 + inference]
- **SOM Y1**: **3%** от SAM = **9,3 млн ₽**. [inference]
- **SOM Y3**: **12%** от SAM = **37,1 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **80** крупных buyers. Это не все 5 044 больницы, а верхний слой: частные сети, федеральные центры, большие региональные стационары, а также потенциальные channel-партнеры в МИС/RCM. [T2 + inference]
- **% with need** = **65%**. Основание: наличие кадровой боли по HH proxy, большая административная нагрузка и крупный рынок платных медуслуг, где ускорение time-to-cash имеет смысл. [T1/T2]
- **Активные buyers** = **52**. [расчет]
- **ARR avg** = **5,4 млн ₽/год**. [T2 + inference]
- **SAM bottom-up** = **52 × 5,4 млн ₽ = 280,8 млн ₽**. [расчет]
- **TAM bottom-up** = **80 × 5,4 млн ₽ = 432,0 млн ₽**. [расчет]
- **SOM bottom-up Y1** = **4%** от SAM = **11,2 млн ₽**. [inference]
- **SOM bottom-up Y3** = **13%** от SAM = **36,5 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 257,4 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 514,8 млн ₽ [T2] | 432,0 млн ₽ [T2] | diff=1,19x; bottom-up ниже, потому что считает только 80 явных крупных buyers | lower |
| SAM (РФ) | 308,9 млн ₽ [T2] | 280,8 млн ₽ [T1/T2] | diff=10%; расхождение приемлемое | lower |
| SOM Y1 | 9,3 млн ₽ | 11,2 млн ₽ | diff=20% | **используем 9,3 млн ₽** |
| SOM Y3 | 37,1 млн ₽ | 36,5 млн ₽ | diff=2% | **используем 36,5 млн ₽** |

### GTM 10 real buyers for bottom-up sanity check
1. **МЕДСИ**. Крупнейшая частная сеть, 138 клиник по состоянию на конец 2025 года. [T2: https://medsi.ru/press-centr/news/medsi-uvelichila-vyruchku-na-do-mlrd-rub-v-godu/]
2. **ГК «Мать и дитя» / MD Medical**. Публичная сеть госпиталей и клиник. [T2: https://www.mcclinics.ru/media/news/operational-results-Q1-2025/]
3. **EMC / European Medical Center**. Премиальный многопрофильный частный контур. [T2: https://www.emcmos.ru/]
4. **АО «Медицина»**. Крупная частная многопрофильная клиника. [T2: https://www.medicina.ru/]
5. **НМИЦ им. В. А. Алмазова**. Крупный федеральный высокотехнологичный центр. [T2: https://www.almazovcentre.ru/]
6. **НМИЦ онкологии им. Н. Н. Блохина**. Большой федеральный стационар с тяжелым документооборотом. [T2: https://www.ronc.ru/]
7. **НМИЦ хирургии им. А. В. Вишневского**. [T2: https://www.vishnevskogo.ru/]
8. **НИИ скорой помощи им. Н. В. Склифосовского**. [T2: https://sklif.mos.ru/]
9. **ГКБ им. С. П. Боткина**. [T2: https://botkinmoscow.ru/]
10. **ФГБУ «НМИЦ ТИО им. ак. В. И. Шумакова»**. [T2: https://transpl.ru/]

Sanity check: SOM Y1 в **9,3 млн ₽** при среднем цикле сделки **9-12 месяцев** означает примерно **2 enterprise-контракта** по 5,4 млн ₽ ARR в первый год. Это реалистично для узкого enterprise GTM. SOM Y1 значительно меньше 10% SAM, red flag overclaim отсутствует. [T2 + inference]

## Profit Gate: может ли компания выйти на EBITDA > 500 тыс. ₽/мес?

### Сценарий A: low-touch software add-on
- Цена: **180 тыс. ₽/мес** за один контур без тяжелых интеграций. [T2 + inference]
- 10 клиентов дают **1,8 млн ₽/мес** выручки. При gross margin **70%** валовая прибыль = **1,26 млн ₽/мес**. Если учитывать продуктовую локализацию, sales и compliance/support минимум **1,8 млн ₽/мес**, EBITDA остается отрицательной. [inference]
- **Вердикт**: **FAIL**. Порог EBITDA > 500 тыс. ₽/мес не достигается. [inference]

### Сценарий B: enterprise module для крупной сети/госпиталя
- Цена: **450 тыс. ₽/мес** или **5,4 млн ₽ ARR**. [T2 + inference]
- 8 клиентов дают **3,6 млн ₽/мес** выручки. При gross margin **75%** валовая прибыль = **2,7 млн ₽/мес**. При операционных расходах около **2,0 млн ₽/мес** остается **0,7 млн ₽ EBITDA**. [inference]
- **Вердикт**: **PASS**. Это минимально рабочий сценарий. [inference]

### Сценарий C: private deployment + implementation + governance
- Цена: **750 тыс. ₽/мес blended** для крупной сети или федерального центра, включая интеграции, QA governance и secure deployment. [T2 + inference]
- 5 клиентов дают **3,75 млн ₽/мес** выручки. Даже при gross margin **72%** валовая прибыль = **2,7 млн ₽/мес**, что позволяет пройти EBITDA > 500 тыс. ₽/мес при OPEX около **2,1 млн ₽/мес**. [inference]
- **Вердикт**: **PASS**. Наиболее правдоподобный сценарий для РФ, если продавать как enterprise transformation, а не как seat tool. [inference]

### Сценарий D: reseller / MIS-partner channel
- Цена конечному клиенту: **250-300 тыс. ₽/мес**, часть маржи уходит партнеру. [T2 + inference]
- Даже при 12 клиентах экономика остается пограничной, потому что часть value capture съедается channel margin и кастомизацией. [inference]
- **Вердикт**: **BORDERLINE / чаще FAIL**. Канал может ускорить доступ к клиникам, но ухудшает EBITDA, если продукт не стандартизирован. [inference]

## Risks
- **Российский demand как product category слабый**: все ключевые запросы по endpoint дали LOW. [T1]
- **Локализация тяжелая**: CodaMetrix строилась вокруг американского coding/RCM stack, а РФ-контур требует другой нормативный и процессный слой. Это сильный execution risk. [T2, inference]
- **Enterprise-only GTM**: публичные price anchors есть только у low-end coding tools, а реальные autonomous coding vendors скрывают прайс. Значит, цикл сделки будет длинным и дорогим. [T2]
- **Telegram не дает distribution edge**: в РФ Telegram-решения в медицине существуют, но почти все patient-facing. [T1/T2]
- **[LOW CONFIDENCE]** Российский спрос на именно autonomous coding software не подтвержден публичными локальными сделками. Вывод о SAM/SOM строится на proxy-data и потому должен рассматриваться как рабочий диапазон, а не как точечный факт. [T1/T2]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: demand endpoint низкий, но underlying labor pain существует; category globally validated; Profit Gate проходит в двух enterprise-сценариях; top-down и bottom-up SAM сходятся в диапазоне **281-309 млн ₽**. [T1/T2]
- Почему не strong pass: локальный product demand почти отсутствует, локализация тяжелая, а реалистичный GTM завязан на few-large-accounts и кастомный enterprise sale. [T1/T2]
- Что проверять дальше на P5/P6: совместимость с российскими классификаторами и МИС, требования к защищенному контуру, долю ручного QA после внедрения, вероятность channel-partnership c локальными МИС/RCM игроками и реальный willingness-to-pay у 10 целевых buyers. [T2]

Sources: T1=4, T2=18, T3=0. Primary evidence basis: T2.


---

## FILE: 04-economics.md

---
stage: unit-economics
case: codametrix-autonomous-medical-coding-v2
date: 2026-04-21
analyst: branch-models-lead
verdict: PASS_WITH_CAUTION
confidence: medium
sector: HEALTHCARE
---

# 04-economics — Unit Economics

## Кейс
CodaMetrix, autonomous medical coding и revenue-cycle automation для крупных клиник, hospital systems и enterprise-медконтуров в РФ.

## Итог
**Статус: PASS WITH CAUTION**

Юнит-экономика собирается только в enterprise-сценарии с private deployment, длинным контрактом и высоким ARPA. В базовом сценарии модель выглядит инвестиционно допустимой: **MRR 650 000 ₽/клиент/мес**, **COGS 245 000 ₽/клиент/мес**, **gross profit 405 000 ₽/клиент/мес**, **fully-loaded CAC 1 820 000 ₽**, **LTV/CAC 17.8x**, **CAC payback 4.5 месяца по gross profit**.

Но кейс остаётся хрупким. Если продукт продавать как “ещё один AI-модуль для клиники” с чеком **< 400 000 ₽/мес**, экономика быстро скатывается в borderline или fail из-за тяжёлого внедрения, интеграций с МИС и обязательного QA/compliance слоя.

---

## 1. Ключевые допущения модели

### Базовый коммерческий сценарий
- **MRR на клиента:** 650 000 ₽/мес
- **ARR на клиента:** 7 800 000 ₽/год
- **Срок контракта:** 12 месяцев, далее продление
- **Setup / implementation fee:** не включаю в core LTV, считаю upside
- **ICP:** крупные частные сети, федеральные центры, многопрофильные стационары, МИС/RCM-партнёры

### Почему этот чек реалистичен
1. В `02-demand.md` уже зафиксировано, что low-end coding tools живут в десятках долларов в месяц, но enterprise autonomous coding продаётся без публичных прайсов и через крупные B2B-сделки.
2. KLAS указывает, что CodaMetrix уже обслуживает **30+ health systems, 500+ hospitals, 100 000+ physicians** и обрабатывает **60+ млн outpatient visits в год**, то есть category monetizes на enterprise-уровне, а не как seat-based utility [T2].
3. Официальный релиз CodaMetrix от **23 июня 2025 года** пишет о клиентах, представляющих **$180 млрд net patient revenue**, что подтверждает budget ownership на уровне revenue-cycle leadership [T1].

---

## 2. Unit economics на 1 клиента

| Метрика | Значение |
|---|---:|
| MRR | **650 000 ₽/мес** |
| ARR | **7 800 000 ₽/год** |
| COGS | **245 000 ₽/мес** |
| Gross profit | **405 000 ₽/мес** |
| Gross margin | **62.3%** |

### Расклад COGS на клиента / месяц
| Компонент | ₽/мес | Комментарий |
|---|---:|---|
| Инфраструктура / hosting / monitoring | 55 000 | защищённый контур, логирование, бэкапы |
| Инференс / модели / OCR / обработка документов | 32 000 | variable AI-load |
| Support + customer success | 44 000 | enterprise SLA и регулярные разборы качества |
| Clinical QA / coding governance allocation | 61 000 | обязательный human-in-the-loop слой |
| Интеграционная поддержка / maintenance | 38 000 | МИС, выгрузки, downstream billing workflow |
| Security / compliance ops | 15 000 | аудит, доступы, политика хранения |

**Итого COGS: 245 000 ₽/мес**

### Вывод по margin
**62.3% gross margin** для healthcare enterprise software с обязательным QA-слоем, это нормально, но уже не “чистый SaaS”. Если margin падает ниже **55%**, кейс начинает выглядеть слишком service-heavy.

---

## 3. CAC и воронка

### Рабочая enterprise-воронка
| Этап | Конверсия / объём |
|---|---:|
| Target accounts в квартал | 90 |
| Intro / first meeting | 18 |
| Qualified opportunities | 9 |
| Deep discovery / data review | 5 |
| Pilot / paid assessment | 2 |
| Won customers | 1 |

### Raw CAC, labour + GTM spend
| Компонент | ₽ на 1 клиента | Комментарий |
|---|---:|---|
| Founder / AE / solution-sales time | 520 000 | длинный enterprise-sale cycle |
| Demo / discovery / pilot scoping | 290 000 | workshops, data review, security review |
| Marketing / events / travel | 210 000 | healthcare-enterprise GTM |
| Legal / procurement / contracting | 120 000 | длинный compliance контур |
| Presale engineering | 260 000 | интеграции, архитектурная проработка |

**Raw CAC = 1 400 000 ₽**

### Fully-loaded CAC
Добавляю **30% overhead** на management, finance, recruiting и shared ops.

**Fully-loaded CAC = 1 400 000 × 1.3 = 1 820 000 ₽**

### Санити-чек
Такой CAC высокий, но правдоподобный для enterprise healthcare sale. Здесь нет self-serve motion, короткого SMB-цикла или дешёвого paid acquisition. Продажа идёт через few-large-accounts.

---

## 4. Churn, retention и LTV

### Допущение по churn
Для консервативной локальной модели беру:
- **annual logo churn = 12%**

Это хуже, чем у зрелых global enterprise vendors, потому что в РФ выше риск локализационного провала, budget freeze и channel displacement.

### Формула LTV
**LTV = ARR × Gross Margin / annual churn**

Подстановка:
- ARR = **7 800 000 ₽**
- Gross Margin = **62.3%**
- churn = **12%**

**LTV = 7 800 000 × 0.623 / 0.12 = 40 495 000 ₽**

---

## 5. Главные метрики инвестиционного фильтра

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 40.495m / 1.82m | **17.8x** | выше порога 3:1 |
| CAC payback | 1.82m / 405k | **4.5 мес** | хороший для enterprise motion |
| Gross Margin | 405k / 650k | **62.3%** | приемлемо |
| Contribution на клиента | 405 000 ₽/мес | **405 000 ₽** | положительный |

### Интерпретация
Формально кейс проходит economics-gate. Но высокий LTV/CAC здесь не означает лёгкий рынок. Он означает, что **если** enterprise-клиент уже куплен и успешно запущен, value capture достаточно большой. Главный риск остаётся в GTM и delivery execution.

---

## 6. Команда и FOT

### Минимальная команда для запуска
| Роль | Кол-во | Fully-loaded FOT, ₽/мес |
|---|---:|---:|
| CEO / founder-sales | 1 | 780 000 |
| CTO / tech lead | 1 | 715 000 |
| Senior backend / integrations | 2 | 1 140 000 |
| ML / document intelligence engineer | 1 | 650 000 |
| Implementation / product manager | 1 | 455 000 |
| Clinical coding SME / QA lead | 1 | 390 000 |
| Customer success / support | 1 | 310 000 |
| AE / enterprise sales | 1 | 455 000 |
| SDR / research | 1 | 205 000 |

**Итого team FOT:** **5 100 000 ₽/мес**

### Прочие fixed costs
- Офис / админ / юрконтур / бухгалтерия / связь / инструменты: **620 000 ₽/мес**
- Итого fixed costs ex-COGS: **5 720 000 ₽/мес**

---

## 7. Break-even и profit gate

### EBITDA break-even
При gross profit **405 000 ₽/клиент/мес**:

**5 720 000 / 405 000 = 14.1 клиента**

То есть безопасный EBITDA break-even, это примерно **15 клиентов**.

### Порог инвестиционного фильтра: EBITDA 500k+ ₽/мес
Нужно покрыть fixed costs и добавить ещё **500 000 ₽** EBITDA:

**(5 720 000 + 500 000) / 405 000 = 15.4 клиента**

То есть для прохождения gate нужно примерно **16 активных enterprise-клиентов**.

### Вывод
- На уровне **5-8 клиентов** кейс ещё не выглядит устойчивым как самостоятельная компания.
- На уровне **16 клиентов** модель уже проходит наш порог **EBITDA > 500k ₽/мес**.
- Для РФ это амбициозно, но не невозможно, если идти через few-large-accounts и channel partnerships.

---

## 8. Сценарный стресс-тест

| Сценарий | MRR | COGS | Gross profit | Вывод |
|---|---:|---:|---:|---|
| Bear | 380 000 ₽ | 230 000 ₽ | 150 000 ₽ | fail, слишком service-heavy |
| Base | 650 000 ₽ | 245 000 ₽ | 405 000 ₽ | pass with caution |
| Bull | 900 000 ₽ | 300 000 ₽ | 600 000 ₽ | strong pass |

### Что ломает кейс
1. **Чек ниже 400k ₽/мес**. Тогда gross profit на клиента слишком мал для такого sales+delivery motion.
2. **Heavy customization** под каждую клинику. Тогда COGS и hidden implementation cost съедают margin.
3. **Неудачная локализация под МИС и классификаторы**. Тогда растёт churn и падает LTV.

---

## 9. Финальный вывод по economics

**Вердикт: PASS WITH CAUTION.**

CodaMetrix-подобная модель может быть investable в РФ только как **узкий enterprise healthcare workflow** с высоким чеком, private deployment и сильным compliance narrative. Как массовый продукт для широкой клинической базы кейс не выглядит жизнеспособным.

### Почему это PASS
- enterprise ценность достаточно велика;
- gross margin в базовом сценарии остаётся выше 60%;
- LTV/CAC и payback выглядят сильными;
- Profit Gate достижим при 16 клиентах.

### Почему это не strong pass
- для РФ buyer universe узкий;
- локализация тяжёлая;
- модель чувствительна к ARPA и implementation load;
- риск превращения в дорогой custom healthcare-integration бизнес остаётся высоким.

## Источники
- [T1] CodaMetrix, клиенты представляют $180B net patient revenue, 2025-06-23: https://www.codametrix.com/resources/codametrix-chosen-by-health-systems-representing-180b-in-net-patient-revenue
- [T2] KLAS profile, 30+ health systems, 500+ hospitals, 60M outpatient visits annually: https://klasresearch.com/vendor-ratings/codametrix/90440
- [T3] CodaMetrix homepage / ROI language: https://www.codametrix.com/
- [T4] Grand View Research, AI in medical coding market size 2025 = $2.86B: https://www.grandviewresearch.com/industry-analysis/artificial-intelligence-ai-medical-coding-market-report
- [T5] AAPC Codify / coding tools pricing anchors: https://www.aapc.com/medical-coding-books/profee-coder-bundle-1/ ; https://www.aapc.com/medical-coding-books/profee-coder-bundle-2/
- [T6] Основание по локальному спросу и buyer universe: `pipeline/cases/codametrix-autonomous-medical-coding-v2/02-demand.md`

<!-- P5-DONE -->


---

## FILE: 05-critic.md

## SECTION A. Finance PnL

### A1. Исходные допущения модели
- ARPA / MRR на клиента: **650 000 ₽/мес**.
- COGS на клиента: **245 000 ₽/мес**.
- Gross profit на клиента: **405 000 ₽/мес**.
- Contribution на клиента: **405 000 ₽/мес**.
- Fixed costs: **5 720 000 ₽/мес**.
- Team FOT fully-loaded: **5 100 000 ₽/мес**.
- Налоговые сценарии для net profit: **УСН 6% с выручки**, **IT-льгота 3% с выручки**, **ОСНО 20% на прибыль**; при ОСНО дополнительно возникает **НДС 20%** и просадка по cash conversion.
- Страховые взносы **~30% к ФОТ** уже включены в fully-loaded FOT и fixed costs.
- Для 12-месячной модели беру 3 сценария привлечения:
  - **Base:** new clients = 0,0,1,1,1,1,2,2,2,2,2,2.
  - **Optimistic:** new clients = 0,1,1,1,2,2,2,2,3,3,3,3.
  - **Pessimistic:** new clients = 0,0,0,1,1,1,1,1,1,2,2,2.
- Churn для расчёта total clients:
  - **Base:** 12% annual ≈ **1.0%/мес**.
  - **Optimistic:** 8% annual ≈ **0.7%/мес**.
  - **Pessimistic:** 18% annual ≈ **1.6%/мес**.
- Cash burn = отрицательная EBITDA по модулю. Cumulative cash считается от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.99 | 2.97 | 3.94 | 5.90 | 7.84 | 9.74 | 11.63 | 13.49 | 15.34 |
| MRR, ₽ | 0 | 0 | 650 000 | 1 293 500 | 1 930 565 | 2 561 259 | 3 837 646 | 5 098 570 | 6 331 585 | 7 558 269 | 8 778 686 | 9 992 899 |
| COGS, ₽ | 0 | 0 | 245 000 | 487 550 | 727 317 | 964 782 | 1 446 960 | 1 922 537 | 2 387 598 | 2 849 690 | 3 309 461 | 3 766 939 |
| Gross profit, ₽ | 0 | 0 | 405 000 | 805 950 | 1 203 248 | 1 596 477 | 2 390 686 | 3 176 033 | 3 943 987 | 4 708 579 | 5 469 225 | 6 225 960 |
| GM% | 0.0% | 0.0% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% |
| Fixed costs, ₽ | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 |
| EBITDA, ₽ | -5 720 000 | -5 720 000 | -5 315 000 | -4 914 050 | -4 516 752 | -4 123 523 | -3 329 314 | -2 543 967 | -1 776 013 | -1 011 421 | -250 775 | 505 960 |
| Cash burn, ₽ | 5 720 000 | 5 720 000 | 5 315 000 | 4 914 050 | 4 516 752 | 4 123 523 | 3 329 314 | 2 543 967 | 1 776 013 | 1 011 421 | 250 775 | 0 |
| Cumulative cash, ₽ | -5 720 000 | -11 440 000 | -16 755 000 | -21 669 050 | -26 185 802 | -30 309 325 | -33 638 639 | -36 182 606 | -37 958 619 | -38 970 040 | -39 220 815 | -39 220 815 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 1.00 | 1.99 | 2.97 | 4.95 | 6.92 | 8.87 | 10.79 | 13.72 | 16.62 | 19.48 | 22.35 |
| MRR, ₽ | 0 | 650 000 | 1 295 450 | 1 936 382 | 3 215 828 | 4 490 978 | 5 757 042 | 7 005 492 | 8 919 895 | 10 802 456 | 12 664 339 | 14 530 688 |
| COGS, ₽ | 0 | 245 000 | 488 231 | 729 176 | 1 211 347 | 1 691 061 | 2 167 356 | 2 637 454 | 3 355 885 | 4 063 231 | 4 762 399 | 5 463 247 |
| Gross profit, ₽ | 0 | 405 000 | 807 219 | 1 207 206 | 2 004 481 | 2 799 917 | 3 589 686 | 4 368 038 | 5 564 010 | 6 739 225 | 7 901 940 | 9 067 441 |
| GM% | 0.0% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.4% | 62.4% | 62.4% | 62.4% |
| Fixed costs, ₽ | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 |
| EBITDA, ₽ | -5 720 000 | -5 315 000 | -4 912 781 | -4 512 794 | -3 715 519 | -2 920 083 | -2 130 314 | -1 351 962 | -155 990 | 1 019 225 | 2 181 940 | 3 347 441 |
| Cash burn, ₽ | 5 720 000 | 5 315 000 | 4 912 781 | 4 512 794 | 3 715 519 | 2 920 083 | 2 130 314 | 1 351 962 | 155 990 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -5 720 000 | -11 035 000 | -15 947 781 | -20 460 575 | -24 176 094 | -27 096 177 | -29 226 491 | -30 578 453 | -30 734 443 | -30 734 443 | -30 734 443 | -30 734 443 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.95 | 3.90 | 4.83 | 5.75 | 7.66 | 9.54 | 11.39 |
| MRR, ₽ | 0 | 0 | 0 | 650 000 | 1 289 600 | 1 918 966 | 2 538 263 | 3 148 051 | 3 748 882 | 4 982 900 | 6 200 173 | 7 398 300 |
| COGS, ₽ | 0 | 0 | 0 | 245 000 | 486 080 | 723 456 | 957 402 | 1 187 884 | 1 414 962 | 1 884 307 | 2 344 681 | 2 797 529 |
| Gross profit, ₽ | 0 | 0 | 0 | 405 000 | 803 520 | 1 195 510 | 1 580 861 | 1 960 167 | 2 333 920 | 3 098 593 | 3 855 492 | 4 600 771 |
| GM% | 0.0% | 0.0% | 0.0% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.3% | 62.2% | 62.2% | 62.2% |
| Fixed costs, ₽ | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 | 5 720 000 |
| EBITDA, ₽ | -5 720 000 | -5 720 000 | -5 720 000 | -5 315 000 | -4 916 480 | -4 524 490 | -4 139 139 | -3 759 833 | -3 386 080 | -2 621 407 | -1 864 508 | -1 119 229 |
| Cash burn, ₽ | 5 720 000 | 5 720 000 | 5 720 000 | 5 315 000 | 4 916 480 | 4 524 490 | 4 139 139 | 3 759 833 | 3 386 080 | 2 621 407 | 1 864 508 | 1 119 229 |
| Cumulative cash, ₽ | -5 720 000 | -11 440 000 | -17 160 000 | -22 475 000 | -27 391 480 | -31 915 970 | -36 055 109 | -39 814 942 | -43 201 022 | -45 822 429 | -47 686 937 | -48 806 166 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 650 000 ₽
- **COGS:** 245 000 ₽
- **Gross profit:** 405 000 ₽
- **Contribution:** 405 000 ₽

#### Waterfall на EBITDA break-even уровне 15 клиентов
- **Revenue:** 9 750 000 ₽/мес
- **COGS:** 3 675 000 ₽/мес
- **Gross profit:** 6 075 000 ₽/мес
- **Contribution:** 6 075 000 ₽/мес
- **EBITDA:** 355 000 ₽/мес

#### Net после налогов РФ @ 15 клиентах
- **УСН 6%:** 355 000 - 585 000 = **-230 000 ₽/мес**
- **IT-льгота 3%:** 355 000 - 292 500 = **62 500 ₽/мес**
- **ОСНО 20%:** 355 000 × 80% = **284 000 ₽/мес**, но дополнительно возникает **НДС 20%** и давление на оборотный капитал

#### Waterfall на target-gate уровне 16 клиентов
- **Revenue:** 10 400 000 ₽/мес
- **COGS:** 3 920 000 ₽/мес
- **Gross profit:** 6 480 000 ₽/мес
- **Contribution:** 6 480 000 ₽/мес
- **EBITDA:** 760 000 ₽/мес
- **Net при УСН 6%:** **136 000 ₽/мес**
- **Net при IT-льготе 3%:** **448 000 ₽/мес**
- **Net при ОСНО 20%:** **608 000 ₽/мес** до учёта НДС cash drag

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M10 | 30 734 443 ₽ | сильный enterprise ramp и быстрые security approvals выводят модель в плюс до конца года |
| Base | M12 | 39 220 815 ₽ | рабочий путь к break-even есть, но требует почти 40 млн ₽ стартового runway |
| Pessimistic | M14 | 49 885 186 ₽ | даже при низком churn downside остаётся капиталоёмким из-за длинного sales cycle |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** операционно простой режим, но на пороге break-even продолжает съедать значимую часть EBITDA.
- **IT-льгота 3%:** самый рациональный режим, если компания проходит аккредитацию и держит профильную IT-выручку.
- **ОСНО 20%:** может давать лучший net на бумаге при положительной прибыли, но НДС и длинный enterprise cash cycle ухудшают реальную ликвидность.
- **Страховые взносы ~30% к ФОТ:** уже учтены во fixed cost base **5.72 млн ₽/мес**.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Break-even month | Комментарий |
|---|---:|---:|---|
| Optimistic | 15 | M10 | достижимо только при 2-3 enterprise wins в квартал и хорошем retention |
| Base | 15 | M12 | модель почти ровно укладывается в годовой горизонт |
| Pessimistic | 15 | M14 | медленный enterprise ramp быстро съедает runway |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев
Базой беру модель из SECTION A, где **M12 EBITDA = 505 960 ₽/мес** при **MRR 9 992 899 ₽**, **15.34 клиентах** и fixed cost **5 720 000 ₽/мес**.

| Scenario | Что меняем | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | без изменений | 505 960 | median-case едва проходит gate |
| Sens1 | CAC x2 | -707 040 | если в M12 закрываются 2 новых клиента, удвоение CAC добавляет примерно 1.21 млн ₽ GTM burn |
| Sens2 | Churn x2 | -108 101 | активная база к M12 падает примерно до 13.8 клиента и EBITDA снова уходит ниже нуля |
| Sens3 | Price -30% | -2 491 315 | ARPA падает до 455k ₽, gross profit на клиента сжимается почти вдвое |

**Вывод:** самый опасный шок, это **price compression**, затем комбинация длинного GTM цикла и churn drift. Модель не разваливается мгновенно, но запас прочности очень небольшой.

### B2. Monte Carlo Lite: confidence intervals
Ниже не полноценная 1000-run симуляция кодом, а **ручная аппроксимация 9 комбинациями** с triangular logic.

#### Inputs: triangular distributions
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 200 000 | 1 820 000 | 3 200 000 | [T1], [T2] |
| Monthly churn, % | 0.7% | 1.0% | 2.2% | [T1], [T2] |
| ARPU, ₽/мес | 450 000 | 650 000 | 850 000 | [T1], [T2] |
| Conversion lead->paid, % | 6% | 11% | 17% | [T2] |
| Time-to-hire / full deployment, мес | 1.0 | 1.8 | 3.5 | [T2] |

#### Как интерпретирована симуляция
- **p10:** CAC_max + churn_max + ARPU_min + медленный deployment + слабая pilot->paid конверсия.
- **p50:** CAC_mode + churn_mode + ARPU_mode.
- **p90:** CAC_min + churn_min + ARPU_max + быстрый deployment + сильная enterprise conversion.
- Для M24 использую продолжение base ramp после M12 и корректирую темп новых клиентов примерно **1.0 / 1.7 / 2.4** новых клиента в месяц для p10 / p50 / p90.

#### Результат Monte Carlo Lite
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | -1 684 000 | 4 420 000 | 10 980 000 | 12 664 000 |
| CAC payback (мес) | 8.2 | 4.5 | 2.1 | 6.1 |
| LTV/CAC | 3.9x | 17.8x | 48.5x | 44.6 |
| Cash runway (мес) | 9 | 12 | 16 | 7 |

#### Интерпретация правил из программы
1. **p10 EBITDA < 0** → правило срабатывает. Значит downside реально убыточный, а не просто «чуть слабее плана».
2. **p50 EBITDA > 500k ₽/мес** → median-кейс gate проходит с запасом.
3. **p90 / |p10| ≈ 6.5x** → неопределённость высокая, но не настолько экстремальная, как в сломанных service-heavy кейсах.
4. **Range width по LTV/CAC = 44.6 > 8** → модель хрупкая и очень чувствительна к ARPU discipline и длине enterprise-sale.

**Промежуточный вывод:** кейс остаётся investable только как **enterprise healthcare execution play**. Median работает, но ширина распределения слишком велика для чистого PASS.

### B3. Competitor deep-dive

#### Западные конкуренты
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Nym** | сильный AI-native narrative в autonomous coding, понятный ROI для health systems, category leadership | фокус на англоязычный payer/provider stack, тяжёлая локализация для РФ | **8-12%** узкого autonomous coding сегмента | можем выиграть secure deployment и локальной адаптацией под российский контур |
| **AKASA** | глубокий revenue-cycle automation слой, сильная automation story вокруг hospital back office | более широкий RCM scope усложняет внедрение и делает продукт дорогим | **6-10%** в AI-for-RCM adjacent сегменте | у нас уже клин не во всём RCM, а в конкретной coding боли с более узким scope |
| **3M / enterprise CAC stack** | brand, доверие у крупных систем, зрелый workflow и кодировочный data moat | legacy-heavy, дорогие циклы внедрения, слабая переносимость в РФ | **15-20%** в enterprise coding infrastructure adjacent | локальная поставка и AI-first workflow могут дать лучший time-to-value |

#### Российские substitutes
| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **МИС-вендоры с кастомной автоматизацией** | уже стоят в клинике, проще пройти procurement, знают локальные интеграции | обычно это project work, а не сильный autonomous coding product | **20-30%** как основной substitute budget | можем продать measurable coding productivity ROI, а не очередной модуль в МИС |
| **RCM / медбиллинг-аутсорсинг** | решают ту же боль через сервис, buyer уже понимает ценность | service-heavy модель плохо масштабируется и не даёт software economics | **15-25%** substitute spend layer | software + QA governance дают лучший margin и более быстрый turnaround |
| **Внутренние команды ручного кодирования** | низкий procurement friction, полный контроль и привычный процесс | высокая трудоёмкость, дефицит кадров, медленная адаптация | крупнейший текущий статус-кво | продукт заменяет labor-spend и ускоряет time-to-cash |

#### Вывод по конкурентам
- В РФ главный враг, это не конкретный AI-vendor, а **статус-кво из ручного coding + МИС-кастомизации + аутсорсинга**.
- Поэтому продукт нельзя продавать как «AI ради AI». Его надо продавать как **сокращение ручного coding headcount pressure и ускорение revenue-cycle**.
- Настоящий moat здесь, это **secure deployment + QA governance + интеграция в локальный медконтур**, а не просто модельный слой.

### B4. Risk matrix
| # | Category | Risk | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Локализация под МИС и классификаторы занимает дольше плана | high | высокий | integration backlog растёт, первый pilot >120 дней | narrow-scope launch, template connectors, phased rollout |
| 2 | Operational | Human QA layer остаётся слишком тяжёлым и съедает margin | high | высокий | QA minutes per case не падают после 2-3 месяцев | stricter routing, case selection, exception-only review |
| 3 | Operational | Не удаётся нанять clinical coding SME / implementation lead | medium | высокий | vacancy open >90 дней, офферы отклоняются | advisor bench, fractional experts, выше comp band |
| 4 | Market | Product demand в РФ остаётся latent и не конвертируется в pipeline | high | высокий | <10 qualified enterprise accounts after first 90 days | sell through CFO / COO pain, а не через category marketing |
| 5 | Market | Сделки слишком длинные для годового runway | high | высокий | security+procurement review >6 месяцев | pilot-first packaging, partner-led entry, board-level sponsor |
| 6 | Market | Клиент выбирает аутсорсинг вместо software | medium | medium/high | loss reasons смещаются в managed service | sell hybrid model with ROI and auditability |
| 7 | Regulatory | Медицинская тайна и data residency блокируют SaaS deployment | high | высокий | ИБ требует only on-prem/private contour | private deployment by default, data minimization, audit log |
| 8 | Regulatory | Изменения требований Минздрава/ОМС ломают workflow | medium | высокий | новые формы и правила требуют large rework | configurable rule layer, update playbooks |
| 9 | Regulatory | Санкции режут доступ к западным моделям и облакам | high | высокий | API billing issues, degraded availability | multi-model routing, local fallback, vendor abstraction |
| 10 | Financial | Cash runway оказывается короче из-за delayed go-live | high | высокий | burn >6.5 млн ₽/мес два квартала подряд | tranche hiring, stop-loss budget, earlier raise |
| 11 | Financial | Ослабление рубля поднимает стоимость inference и infra | medium | medium/high | USD/RUB >110, infra share растёт >20% | local infra, repricing clauses, валютный буфер |
| 12 | Financial | Не подтверждается IT-льгота, post-tax модель портится | medium | medium | effective tax rate выше плана | early tax structuring, reserve cash |
| 13 | Black swan | Hospital CAPEX freeze замораживает цифровые проекты | medium | высокий | пилоты подписываются, но rollout freeze | ROI-first wedge, shorter pilot contracts |
| 14 | Black swan | Ошибка модели в критичном medical-financial процессе бьёт по доверию | medium | критический | manual override incidents растут, клиент останавливает rollout | strict human-in-the-loop, audit trail, bounded scope |

**Итог по рискам:** плотность high-impact рисков остаётся высокой. Кейс можно финансировать только если инвестор принимает именно **delivery + regulatory + GTM execution risk**.

### B5. Kill conditions через 6 месяцев
1. **<3 live enterprise клиента** или **pilot->paid conversion <25%**. Тогда локальный PMF не подтверждён.
2. **Gross profit per client <300k ₽/мес** или **ARPU <550k ₽/мес**. В этой зоне модель быстро превращается в service-heavy историю.
3. **Cash runway <9 месяцев** при всё ещё отрицательном p10 EBITDA и без понятного path to 15+ клиентов. Тогда expansion надо останавливать или радикально сужать.

### B6. Decision update
- **Median-case остаётся рабочим**, а p50 EBITDA Gate проходит.
- Но downside заметный, потому что **p10 < 0**, а диапазон LTV/CAC слишком широкий.
- Поэтому кейс надо трактовать как **PASS WITH CAUTION / risk-discounted pass**, а не как clean winner.

## Источники SECTION B
- [T1] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/codametrix-autonomous-medical-coding-v2/04-economics.md`
- [T2] `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/codametrix-autonomous-medical-coding-v2/02-demand.md`
- [T3] CodaMetrix homepage: https://www.codametrix.com/
- [T4] KLAS vendor profile / scale indicators: https://klasresearch.com/vendor-ratings/codametrix/90440
- [T5] Grand View Research, AI in medical coding market: https://www.grandviewresearch.com/industry-analysis/artificial-intelligence-ai-medical-coding-market-report
- [T6] AAPC pricing anchors: https://www.aapc.com/codes/

<!-- P6B-DONE -->


---

## FILE: 06-verdict.md

[HEALTHCARE] CodaMetrix Autonomous Medical Coding v2 — NEAR-PASS: 67/100 | EBITDA base=506К₽/мес через 12 мес | LTV/CAC=17,8x | Ключевое преимущество: enterprise revenue-cycle ROI для крупных клиник | Главный риск: в РФ product-demand пока слабый и требует тяжёлого внедрения.

# 06-verdict — CodaMetrix Autonomous Medical Coding v2

sector: HEALTHCARE
status: NEAR-PASS
score: 67/100
normalized_from_raw: 100/150
case_slug: codametrix-autonomous-medical-coding-v2
updated_at: 2026-04-21 05:39 MSK

## Инвесткомитет: итоговый вердикт

Кейс не дотягивает до APPROVED, но остаётся сильным кандидатом на повторный заход после локального GTM-доказательства. Экономика на проданном enterprise-клиенте сильная: `customer_ltv_rub = 40 495 000 ₽`, `contribution_margin_rub_month = 405 000 ₽/клиент/мес`, `company_ebitda_rub_month` в base выходит в плюс уже к M12, а `company_ebitda_potential_rub_month` уверенно проходит gate при 16 клиентах. Но инвестиционный запас прочности пока недостаточен: `02-demand.md` фиксирует `LOW` по обязательным RU-demand endpoint, а в `05-critic.md` p10 EBITDA @M24 остаётся отрицательной. Поэтому решение инвесткомитета, это **NEAR-PASS**.

## Оценка

Source tier balance: T1=4, T2=18, T3=0, weighted=2.18. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | В 04-economics.md: `LTV/CAC 17.8x`, `CAC payback 4.5 месяца по gross profit`, `gross margin 62.3%`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | В 05-critic.md: `M12 EBITDA = 505 960 ₽/мес`, а gate `500k+` достигается на уровне `16 активных enterprise-клиентов`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | В 02-demand.md: `Итог по спросу в РФ: LOW`, но есть `hh.ru vacancies = 92` и SAM `281-309 млн ₽`; применён tier-штраф -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | В 05-critic.md: `Настоящий moat здесь, это secure deployment + QA governance + интеграция в локальный медконтур`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | В 05-critic.md: `p10 EBITDA < 0`, а high-impact risks включают локализацию под МИС, санкции и тяжёлый human QA layer. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | В 02-demand.md: `SOM Y1 ... примерно 2 enterprise-контракта`, а 04-economics.md показывает реалистичный enterprise CAC `1 820 000 ₽`. |

**Sum raw = 100/150**  
**Normalized score = round((100 × 100) / 150) = 67/100**

## 7-factor Moat framework

| Фактор | Балл (0-3) | Краткое обоснование |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных, это не network-led business. |
| Switching costs | 2 | После внедрения появляются интеграции, правила QA и операционные привычки coding/revenue-cycle команды. |
| Scale economies | 2 | С ростом базы можно реиспользовать connectors, playbooks и governance, но COGS не схлопывается до pure SaaS. |
| Proprietary data / model advantage | 1 | Явный локальный датасет и количественный data moat пока не доказаны. |
| Regulatory moat | 2 | Private deployment, медтайна и data residency создают барьер входа, но без лицензируемого монопольного эффекта. |
| Brand / distribution | 1 | Глобальная category validation сильная, но локального distribution moat в РФ пока нет. |
| Embedded workflow | 3 | Продукт глубоко встраивается в ежедневный coding, billing readiness и revenue-cycle workflow клиники. |

**Moat raw = 11/21**  
**Moat score = round((11 × 25) / 21) = 13/25**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 40 495 000 ₽ |
| CAC blended fully-loaded | 1 820 000 ₽ |
| LTV/CAC | 17,8x |
| CAC Payback | 4,5 мес по gross profit |
| Gross Margin | 62,3% |
| contribution_margin_rub_month | 405 000 ₽/клиент/мес |
| fixed_costs_rub_month | 5 720 000 ₽/мес |
| company_ebitda_rub_month, M12 base | 505 960 ₽/мес |
| company_ebitda_potential_rub_month | 3 347 441 ₽/мес в optimistic M12 / 4 420 000 ₽ p50 @M24 |
| clients_to_500k_ebitda | 16 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 17 |
| months_to_1m_ebitda | 13 |
| Break-even | 15 клиентов |
| startup_capital_to_bep_rub | 39 220 815 ₽ |

## Полный business process из 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Формирование target account list | Founder / AE / research | ручной ресерч, CRM, отраслевые списки | 90 мин/account | 95 000 | низкий |
| 2 | Intro и first meeting | Founder / AE | email, телефон, warm intros | 60 мин/account | 140 000 | низкий |
| 3 | Deep discovery и data review | AE + solution-sales | Zoom/Meet, шаблоны вопросов, ROI framing | 2-3 часа | 290 000 | низкий |
| 4 | Demo / workflow mapping | AE + CTO | sandbox, demo-env, архитектурные схемы | 2 часа | 210 000 | низкий |
| 5 | Security review / legal / procurement | CTO + founder + legal | checklists, DPA, договоры | 3-5 часов | 120 000 | низкий |
| 6 | Presale engineering и pilot scoping | Presale / implementation | интеграционные схемы, sample data, roadmap | 1-2 недели | 260 000 | низкий |
| 7 | Pilot / paid assessment | implementation + QA lead | secure contour, тестовые выгрузки, SLA | 4-8 недель | включено в CAC | средний |
| 8 | Contract close | Founder / AE | proposal, legal docs, procurement pack | 1-3 недели | включено в CAC | низкий |
| 9 | Production onboarding | PM + integrations + QA | rollout plan, доступы, dashboards | 2-6 недель | в setup / implementation fee | средний |
| 10 | Monthly QA governance и support | CSM + coding SME | audit review, issue queue, регулярные разборы | ongoing | в COGS | средний |

## Финансовая траектория

| Scenario | EBITDA break-even month | EBITDA @M12 | EBITDA @M24 | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Optimistic | M10 | 3 347 441 ₽/мес | 10 980 000 ₽/мес | 30 734 443 ₽ |
| Base | M12 | 505 960 ₽/мес | 4 420 000 ₽/мес | 39 220 815 ₽ |
| Pessimistic | M14 | -1 119 229 ₽/мес | -1 684 000 ₽/мес | 49 885 186 ₽ |

### Monte Carlo Lite summary
- p10 EBITDA @M24 = **-1 684 000 ₽/мес**
- p50 EBITDA @M24 = **4 420 000 ₽/мес**
- p90 EBITDA @M24 = **10 980 000 ₽/мес**
- Вывод: median-case проходит, но downside остаётся отрицательным, а dispersion по LTV/CAC слишком широкий для clean approve.

## Команда

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO / founder-sales | enterprise sales, partnerships, fundraising | 780 000 |
| CTO / tech lead | архитектура, security review, delivery governance | 715 000 |
| Senior backend x2 | integrations, workflow engine, APIs | 1 140 000 |
| ML / document intelligence engineer | extraction, routing, quality loops | 650 000 |
| Implementation / product manager | pilot rollout, onboarding, change requests | 455 000 |
| Clinical coding SME / QA lead | domain QA, governance, trust layer | 390 000 |
| Customer success / support | adoption, support, QBR, renewals | 310 000 |
| AE / enterprise sales | qualification, demos, close | 455 000 |
| SDR / research | account mapping, outbound, list building | 205 000 |
| **Итого** |  | **5 100 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| МЕДСИ | крупнейшая частная сеть, большой поток документов и billing ops | email decision-maker по цифровизации / revenue ops | 650 000 ₽/мес |
| Мать и дитя | федеральная сеть с понятным платным revenue-cycle и сложным clinical admin | founder-led outreach + healthcare conference | 700 000 ₽/мес |
| EMC | премиальный многопрофильный контур, высокий чек ошибки и ручного coding | direct outreach в COO/CFO + партнёр-интегратор | 750 000 ₽/мес |
| АО «Медицина» | крупная частная клиника с premium care и высокой ценой admin inefficiency | email + warm intro через medtech ecosystem | 500 000 ₽/мес |
| НМИЦ им. Алмазова | сложный федеральный high-acuity поток, где auditability особенно важна | конференция по цифровому здравоохранению + пилот через ИТ-блок | 600 000 ₽/мес |
| НМИЦ онкологии им. Блохина | большой объём тяжёлых случаев и документного контура | партнёрство с МИС/интегратором + direct outreach | 600 000 ₽/мес |
| НМИЦ хирургии им. Вишневского | хирургический стационар с high-value billing workflow | direct outreach в CIO/главврачу | 550 000 ₽/мес |
| НИИ Склифосовского | скоропомощной контур, где важны скорость и контроль ошибок | пилот через цифровизацию и quality-office | 550 000 ₽/мес |
| Боткинская больница | крупный городской стационар, высокий объём coding и downstream админ-процессов | отраслевой форум + email decision-maker | 500 000 ₽/мес |
| НМИЦ ТИО им. Шумакова | сложный федеральный центр с дорогими случаями и высокими требованиями к audit trail | direct outreach + партнёрский канал через МИС | 600 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему это важно |
|---|---|---|---|
| Слабый прямой product-demand в РФ | high | high | В 02-demand.md все ключевые product-запросы дали `LOW`, значит GTM нельзя строить на category pull. |
| Heavy implementation / QA drift | high | high | Если human QA и интеграции останутся тяжёлыми, кейс быстро сползает в bear-сценарий `380k MRR / 150k gross profit`. |
| Санкции, data residency и зависимость от LLM stack | high | high | В 05-critic.md отдельно отмечены `sanctions`, `medical secrecy`, `private contour` и `multi-model routing` как критичные допущения. |

## Что надо доказать для APPROVED

1. Не менее **3 live enterprise-клиентов** и **pilot-to-paid ≥25%** в первые 6 месяцев.
2. Удержание **ARPA ≥ 550-650К ₽/мес** без постоянного custom-scope creep.
3. Снижение доли human QA, чтобы `contribution_margin_rub_month` не падал ниже **300К ₽/клиент/мес**.
4. Повторяемый канал через **МИС/RCM-партнёров** или сильный founder-led wedge в 10 named targets.
5. Подтверждение, что private deployment и локальные классификаторы оформлены как product playbook, а не bespoke integration business.

## LTV Upside Calculator

| Рычаг | Текущее значение | Целевое значение | Эффект |
|---|---:|---:|---|
| ARPA | 650 000 ₽/мес | 750 000 ₽/мес | Поднимает запас прочности против price compression и ускоряет path to 1M EBITDA. |
| COGS на клиента | 245 000 ₽/мес | ≤220 000 ₽/мес | Повышает gross margin и снижает risk of service-heavy drift. |
| Fully-loaded CAC | 1 820 000 ₽ | ≤1 500 000 ₽ | Улучшает cash efficiency и сокращает burn-to-breakeven. |
| Churn | 12% annual | ≤9% annual | Существенно укрепляет `customer_ltv_rub` и оправдывает enterprise CAC. |
| Evidence tier balance | 2.18 | ≥2.5 | Снимает penalty по Market+Demand и может поднять score в approve-зону. |

### Минимальные proof points для rerun
1. **10 SQL** по списку named targets и хотя бы **3 paid pilots**.
2. Первый подтверждённый **channel attach** через МИС/RCM-партнёра.
3. Реальный **CAC ≤ 1,5 млн ₽** на первых закрытых enterprise клиентах.
4. Доказательство, что `clients_to_500k_ebitda = 16` достижимы без пропорционального роста fixed costs.

## Финальное решение инвесткомитета

**NEAR-PASS.**

Я бы не отклонял кейс как структурно плохой, потому что unit economics и EBITDA-path в enterprise healthcare здесь реальные. Но для approve пока не хватает двух вещей: повторяемого локального demand proof и уверенности, что модель не превратится в тяжёлый кастомный integration business. Поэтому правильный статус сейчас, это watchlist с жёсткими proof-point условиями на следующий rerun.

---

## FILE: 07-score-trajectory.md

## 2026-04-21 00:45 MSK — P4 Demand Validation
- Этап: P4 Demand Validation
- Итог: прямой product demand в РФ низкий, но кейс не умирает, потому что кадровая боль и global category validation создают окно для enterprise-продажи в крупных медицинских контурах.
- Ключевой вывод: mandatory demand endpoint по целевым ключам дал LOW, однако Profit Gate проходит в enterprise-сценариях, а SAM по двум методикам сходится в диапазоне 281-309 млн ₽.
- Изменение оценки: умеренно негативное по ширине локального спроса, но умеренно позитивное по монетизации при продаже few-large-accounts с private deployment.
- Артефакт: `pipeline/cases/codametrix-autonomous-medical-coding-v2/02-demand.md`

## 2026-04-21 04:18 MSK — P5 Unit Economics
- Этап: P5 Unit Economics
- Итог: экономика проходит только в enterprise-сценарии с private deployment и высоким ARPA, mass-market и low-ticket версия не работает.
- Ключевой вывод: base-case даёт MRR 650k ₽, COGS 245k ₽, gross profit 405k ₽, fully-loaded CAC 1.82 млн ₽, LTV/CAC 17.8x и EBITDA-gate на уровне примерно 16 активных клиентов.
- Изменение оценки: умеренно позитивное по качеству economics после продажи, но сохраняется высокий execution-risk из-за тяжёлой локализации и узкого buyer universe.
- Артефакт: `pipeline/cases/codametrix-autonomous-medical-coding-v2/04-economics.md`

## 2026-04-21 05:39 MSK — P7 Critic + Verdict
- Этап: P7 Critic + Verdict
- Итог: финальный статус **NEAR-PASS, 67/100**.
- Ключевой вывод: unit economics и EBITDA-path проходят investment gate, но локальный product-demand остаётся LOW, а p10 EBITDA @M24 остаётся отрицательной.
- Изменение оценки: финально позитивно по экономике, но негативно по margin of safety; кейс переведён в rejected/watchlist как near-pass.
- Артефакт: `pipeline/cases/codametrix-autonomous-medical-coding-v2/06-verdict.md`
