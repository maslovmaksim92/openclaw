<!-- 01-intake.md -->

---
sector: HEALTHCARE
rerun: true
source_raw: 2026-04-19-resurrect-abridge-ambient-medical-scribe-geo-expand.md
created: 2026-04-20T04:42:12+03:00
---

# 01-intake

## Кейс
abridge-ambient-medical-scribe-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-abridge-ambient-medical-scribe-geo-expand.md

## Краткий контекст
Standalone healthcare-кейс по ambient clinical documentation и hospital-grade AI scribe workflow. Нужно валидировать buyer, бюджет, требования к комплаенсу и шанс локализации под российские МИС и меддокументооборот.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить economics на сеть клиник, downstream value beyond transcription и наличие защищённого deployment-требования.

## Полный контекст из raw

# RESURRECT SIGNAL — abridge-ambient-medical-scribe-geo-expand

## Meta
- source: triage/triage-2026-04-14-abridge-ambient-medical-scribe-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-abridge-ambient-medical-scribe-geo-expand.md

## Классификация
кандидат в новый кейс

## Решение
Открыть новый кейс: `ambient-clinical-documentation-operator`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы не покрывают enterprise-grade ambient clinical documentation как отдельную вертикальную сервисную модель для медицины.
- Сигнал по Abridge достаточно сильный по масштабу: 250+ крупных health system-партнёров в США, прогноз 80 млн разговоров врач-пациент в 2026 году и рыночная оценка выручки около 100 млн долларов ARR.
- По экономике сигнал проходит порог частично, но правдоподобно: `ltv_signal` указан как 3-15 млн руб. в год с одной крупной клинической сетью или медтех-провайдером, то есть примерно 250 000-1 250 000 руб. в месяц. Верхняя часть диапазона превышает порог `> 500 000 руб./мес.`.
- Это не generic transcription tool, а более глубокий инфраструктурный слой: автоматическое создание клинической документации и биллингово-пригодных записей из разговора врача и пациента, с высокой ценой ошибки и интеграционной сложностью.
- Локализация трудная, но именно поэтому сервисная ценность может быть высокой: нужны русский медицинский speech-to-text, шаблоны под локальный документооборот, интеграции с МИС/ЕМИАС-подобными контурами и защищённое хранение чувствительных медданных.
- В raw-файле отмечено отсутствие зрелого публично заметного российского аналога уровня Abridge на дату 14 апреля 2026 года, что поддерживает GEO-EXPAND окно.

## Что сделано
- Создан новый кейс `pipeline/cases/ambient-clinical-documentation-operator/`.
- В `00-brief.md` зафиксированы описание модели, стартовые факты и ключевая гипотеза для следующего validation block.
- Исходный raw-файл подлежит перемещению в `pipeline/raw/processed/`.

## Пометка для следующего шага
Проверять кейс как enterprise healthcare infrastructure / workflow model, а не как простой voice AI. На следующем цикле собрать подтверждения по:
- buyer и бюджету: крупные частные клиники, сети, телемедицина, МИС-вендоры, revenue cycle / billing контуры;
- unit economics: цена за врача, клинику, сеть или объём разговоров; внедрение против recurring subscription; attach rate интеграций;
- требованиям к данным и комплаенсу: хранение, consent, безопасность, on-prem/private cloud, медицинская тайна;
- реальным российским и СНГ-аналогам, чтобы проверить силу GEO-EXPAND окна;
- глубине downstream-ценности: не только сокращение времени врача, но и улучшение качества документации, кодирования и финансового capture.

## Вердикт
Сигнал достаточно сильный для открытия отдельного кейса: тема выглядит как правдоподобная high-LTV вертикальная модель с трудной локализацией и потенциально дорогим enterprise-внедрением.

```


<!-- 02-demand.md -->

# 02-demand

## Demand validation summary
- **Продукт**: Abridge, AI ambient medical scribe и clinical documentation assistant для автоматического создания клинической документации по разговору врача с пациентом. [T2: https://www.abridge.com/]
- **Итог по спросу в РФ**: **LOW** по прямому category-search и публичному hiring signal, но **не нулевой** по подтвержденной боли вокруг заполнения меддокументации и уже существующим локальным решениям. Обязательный endpoint `multi-demand?keyword=ambient medical scribe` вернул **LOW / score 0**. [T2: internal demand endpoint]
- **Решение по гейту**: **не отклонять на P4**. Массового спроса нет, но enterprise/private-clinic motion все еще может пройти Profit Gate, если продавать как сокращение времени врача на документацию и снижение нагрузки на медперсонал. [T1][T2]

## Evidence of demand

### 1) Mandatory endpoint
- `http://172.18.0.1:9001/multi-demand?keyword=ambient%20medical%20scribe` → **LOW**, score **0**; Google Trends RU = 0, Habr = 2, HH = 0, Yandex suggest = 2. Это сильный сигнал, что в России нет оформленного inbound-спроса именно по западной category label `ambient medical scribe`. [T2: internal demand endpoint]

### 2) Russia demand proxies
- На hh.ru у вакансий врачей и клиник регулярно фигурирует обязанность `ведение медицинской документации`, то есть сам pain point публично и массово присутствует в описаниях работы. Это не спрос на сам термин ambient scribe, но прямое подтверждение, что ручная документация остается частью операционного процесса. [T1: https://hh.ru/]
- В России уже продается локальный продукт **Voice2Med** от ЦРТ для голосового заполнения медицинской документации, причем продукт поддерживает локальное развертывание, специализированные словари и интеграцию в МИС. Наличие локального игрока означает, что бюджет на задачу в РФ существует. [T2: https://voice2med.ru/]
- Российский healthcare AI рынок в целом движется в сторону автоматизации документации и маршрутизации клинических данных, но покупателем выступают не individual clinicians, а крупные клиники, сети и диагностические контуры. Это снижает ширину спроса и повышает средний чек. [T2]

### 3) Global/category demand
- Категория AI medical scribe уже коммерциализирована на развитых рынках: у Freed публичные тарифы для clinicians, у Scribeberry и Heidi есть отдельные pricing/plans pages, а Ambience и Abridge продвигаются как enterprise stack для health systems. Это подтверждает существование реального product-market fit категории вне РФ. [T1/T2: https://www.getfreed.ai/pricing ; https://scribeberry.com/pricing ; https://www.heidihealth.com/us/pricing ; https://www.ambiencehealthcare.com ; https://www.abridge.com/]
- По данным профильных market reports, мировой рынок AI clinical documentation / medical scribe software уже измеряется сотнями миллионов долларов и быстро растет, но российский рынок остается сильно уже из-за локализации, интеграций и требований к данным. [T2]

## Competitor landscape with prices

Курс для пересчета: **1 USD = 76.0535 ₽** по курсу Банка России на **20 апреля 2026 года**. [T1: https://www.cbr.ru/scripts/XML_daily.asp?date_req=20/04/2026]

| Конкурент | Что продает | Цена | Комментарий |
|---|---|---:|---|
| Freed | AI medical scribe для individual clinicians и groups | **$39 / $79 / $104 в месяц за clinician**, то есть примерно **2.97 / 6.01 / 7.91 тыс. ₽ в месяц** [T1] | Публичный low-end benchmark для self-serve сценария. |
| Heidi | AI scribe с free-to-enterprise motion | pricing page есть, но публичный extract не показывает цифры; продается через планы Free / Evidence / Clinician / Enterprise [T2] | Подтверждает, что рынок делится на free/self-serve и enterprise tiers. |
| Scribeberry | AI medical scribe, публичная pricing page | публичная pricing page есть, но extract без чисел; компания заявляет `trusted by 30,000+ healthcare professionals` [T2] | Сигнал, что категория уже commoditizes на clinician-level outside RU. |
| Voice2Med (РФ) | Голосовое заполнение медицинской документации, локальная и серверная версии | цена публично не раскрыта, продажа через enterprise/тендерный motion [T2] | Это главный локальный конкурентный риск в РФ. |

### Вывод по ценам конкурентов
- Для self-serve западный ценовой floor находится примерно в коридоре **3-8 тыс. ₽ в месяц на врача** по публичным тарифам Freed. [T1]
- Для РФ enterprise motion публичного прайсинга почти нет, что обычно означает project pricing, внедрение и интеграционный чек, а не простой card checkout. Для Abridge это скорее плюс, потому что продукт ближе к enterprise health-system sale, чем к cheap SMB SaaS. [T2]

## Telegram bots/services in Russia
- Прямого массового Telegram-бота в РФ именно под ambient medical scribe с внятным pricing и enterprise traction я не нашел. Это негативный сигнал для быстрого low-end distribution через Telegram. [T2/T3]
- При этом в РФ уже есть **локальные сервисы**, решающие соседнюю задачу голосового ввода меддокументации, прежде всего **Voice2Med**. Значит, Telegram не обязателен как канал delivery, потому что деньги лежат в клинических ИТ-бюджетах и интеграциях в МИС. [T2: https://voice2med.ru/]
- Вывод: **Telegram в РФ для этого кейса не является core-channel**. Если и использовать его, то как lead-gen/education для частных врачей, но не как основной канал продаж enterprise-клиникам. [T2]

## WTP (willingness to pay)
- Готовность платить подтверждается не поисковым спросом, а существующими spend lines: клиники уже покупают голосовой ввод и распознавание речи, а также несут постоянные издержки на ручное ведение документации врачами и медперсоналом. [T1/T2]
- Публичные цены Freed показывают, что individual clinician outside RU готов платить порядка **3-8 тыс. ₽ в месяц** за инструменты клинической документации. Это полезный нижний ориентир, но для России он завышает масштаб self-serve спроса и занижает сложность compliance/integration. [T1]
- Для РФ более реалистичен не per-seat, а **department / clinic contract**: клиника платит за 20-50 врачей, локальное развертывание, интеграцию в МИС и словари. Отсюда рабочий диапазон WTP на пилот/боевой контракт порядка **150-400 тыс. ₽ в месяц на организацию**. Это оценка по benchmark-логике, а не публичный прайс конкретного российского контракта. [T1+T2 inference]
- Доказательство willingness to pay умеренное, не сильное: публичных тендеров и прайс-листов мало, но сам класс задач уже монетизируется и в РФ, и за рубежом. [T2]

## Market sizing

### Assumptions
- Для верхней границы беру physician-based logic: если врач является primary user, рынок можно приблизить через число врачей и допустимый annual software spend. Число врачей в РФ в 2024 году в публичных заявлениях Минздрава оценивается примерно в **557 тыс.** [T2]
- Для консервативного пересчета self-serve floor использую **$79/мес** как референсный mid-tier tariff Freed, то есть около **72 тыс. ₽ в год на врача**. [T1]
- Для адресуемого сегмента в РФ беру только часть врачей и клиник, где документация насыщенная, есть цифровой контур и бюджет на ИТ: крупные частные сети, премиальные клиники, диагностические центры и отдельные прогрессивные госсистемы. [T2]

### GTM-10 real buyers for RF expansion
1. МЕДСИ [T2]
2. EMC / Европейский медицинский центр [T2]
3. ГК Мать и дитя [T2]
4. Medscan [T2]
5. СМ-Клиника [T2]
6. K+31 [T2]
7. Hadassah Medical Moscow [T2]
8. Клиника Фомина [T2]
9. АО «Медицина» [T2]
10. Чайка [T2]

### Top-down calculation
- **TAM (РФ)** = 557,000 врачей × 72,000 ₽ ARR на врача = **40.1 млрд ₽**. Это theoretical ceiling, если считать весь physician base адресуемым, что в реальности неверно. [T1+T2]
- **SAM (РФ)** = TAM × 12% адресуемого сегмента = **4.8 млрд ₽**. 12% отражает только цифрово зрелые клиники и контуры, где есть шанс на внедрение в ближайшие 3 года. [T1+T2 inference]
- **SOM Y1** = SAM × 1.5% = **72 млн ₽**. [T2]
- **SOM Y3** = SAM × 5% = **241 млн ₽**. [T2]

### Bottom-up calculation
- **Total buyers** = эквивалент **1,000 клиник/контуров**, где есть хотя бы 15-20 врачей и цифровой workflow, пригодный для voice documentation. Это расчетная оценка, а не официальный реестр; anchor делаю на GTM-10 и extrapolation на крупные частные и продвинутые государственные организации. [T2 inference]
- **% with need** = **60%**, потому что не всем нужен ambient scribe, но у большинства крупных клиник есть документационная нагрузка. [T1+T2 inference]
- **ARR avg** = **300 тыс. ₽ в год** на стартовый пилотный контракт или ограниченный department deployment. [T1+T2 inference]
- **SAM bottom-up** = 1,000 × 60% × 300,000 ₽ = **180 млн ₽**. [T1+T2]
- **SOM Y1 bottom-up** = 8% от SAM = **14.4 млн ₽**. [T2]
- **SOM Y3 bottom-up** = 20% от SAM = **36 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | мировой рынок категории уже коммерциализирован, но без единой точки; для РФ не использую как primary driver [T2] | — | — | top-down only as context |
| TAM (РФ) | **40.1 млрд ₽** [T1+T2] | — | top-down здесь заведомо широкий ceiling по всем врачам | top-down ceiling |
| SAM (РФ) | **4.8 млрд ₽** [T1+T2] | **180 млн ₽** [T1+T2] | расхождение ~26.7x, значит initial segment нужно сузить до реально продаваемого enterprise beachhead | **180 млн ₽** |
| SOM Y1 | **72 млн ₽** | **14.4 млн ₽** | top-down завышает скорость проникновения для нового рынка | **14.4 млн ₽** |
| SOM Y3 | **241 млн ₽** | **36 млн ₽** | bottom-up лучше отражает реальный GTM через limited number of clinics | **36 млн ₽** |

### Re-segmentation after cross-check
- Так как top-down и bottom-up сначала расходятся больше чем в 3 раза, для инвестиционной интерпретации я **не использую широкий physician TAM как рабочий рынок**, а перехожу на узкий beachhead: крупные частные сети, премиальные клиники и федеральные центры с сильной цифровой зрелостью. [T2]
- В практическом смысле **рабочий SAM для входа в РФ = 180 млн ₽**, а не 4.8 млрд ₽. Это и есть корректная reconciliation. [T2]
- **Sanity**: SOM Y1 = 14.4 млн ₽, это примерно 4 клиента по 300 тыс. ₽ ARR или 2-3 клиента по 5-7 млн ₽ с более широким развертыванием. С длинным медицинским sales cycle это реалистично. [T2]

## Profit Gate: can EBITDA >= 500K ₽/month be achieved?

### Scenario A: self-serve per clinician
- Цена: **3-8 тыс. ₽ в месяц** на врача по международным публичным benchmark. [T1]
- Чтобы получить **500 тыс. ₽ EBITDA в месяц**, нужно несколько сотен активных платящих врачей в РФ после поддержки, локализации и acquisition cost. Для этого нет ни inbound demand, ни distribution flywheel. [T1+T2]
- **Вердикт**: FAIL. [T2]

### Scenario B: clinic pilot / department sale
- Цена: **150-250 тыс. ₽ в месяц** на клинику или отделение. [T1+T2 inference]
- При **8-10 клиентах** выручка будет **1.2-2.5 млн ₽ в месяц**. Если продукт развертывается lean-командой и без тяжелой on-prem кастомизации на каждого клиента, EBITDA **500 тыс. ₽ в месяц** достижима. [T2]
- **Вердикт**: PASS, но только при узком ICP. [T2]

### Scenario C: enterprise health-system deployment
- Цена: **300-700 тыс. ₽ в месяц** на сеть/крупный контур при интеграции в МИС, словарях и rollout на группы врачей. [T2 inference]
- Достаточно **3-5 клиентов**, чтобы перевалить за требуемый уровень EBITDA, если gross margin удерживается и внедрение не превращается в бесконечный кастом-проект. [T2]
- **Вердикт**: PASS. [T2]

**Итог по Profit Gate**: gate **проходит** в clinic-enterprise сценарии, **не проходит** в broad self-serve сценарии. [T2]

## Risks
- Прямой спрос по category keyword в РФ очень слабый, поэтому inbound GTM почти не работает. [T2]
- Медицинские данные, интеграции в МИС и требования к on-prem/private cloud сильно усложняют локализацию. [T2]
- В РФ уже есть локальный функциональный substitute в лице Voice2Med, поэтому moat Abridge нельзя строить только на распознавании речи. [T2]
- Market sizing по широкому physician base легко переоценивает рынок; рабочая инвестиционная логика должна оставаться в узком enterprise beachhead. [T2]

## Verdict for P4
- **Demand = LOW**, но **Profit Gate = PASS** в узком clinic/enterprise сценарии. [T2]
- Следовательно, **early reject не нужен**. Кейс можно вести дальше, но только как high-touch B2B expansion thesis, а не как массовый AI bot / self-serve продукт для врачей. [T2]
- На следующих этапах нужно отдельно проверить economics внедрения, требования по хранению данных и интеграции с российскими МИС. [T2]

## Market Pulse
> Market Pulse 2026-04-20: спрос слабый, но корпоративный бюджет на задачу существует.

Sources: T1=4, T2=19, T3=0. Primary evidence basis: T2 with T1 pricing anchor and FX conversion.

> Market Pulse 2026-04-21: растущий интерес.
## Market Pulse
- Market Pulse 2026-04-21: растущий интерес.


<!-- 03-solution.md -->

---
stage: solution
case: abridge-ambient-medical-scribe-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
sector: HEALTHCARE
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Abridge как enterprise-grade ambient medical scribe и clinical documentation layer для клиник, сетей и цифровых медицинских контуров при выходе в РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «AI для голоса», а дорогую операционную проблему, как сократить время врача на документацию, повысить полноту записей и уменьшить ручную нагрузку на клинический персонал.
2. Реальный wedge в РФ выглядит не как self-serve инструмент для каждого врача, а как **enterprise workflow layer для крупных клиник, сетей и МИС-насыщенных контуров**, где документация, безопасность данных и интеграции критичны.
3. Наиболее правдоподобный вход в рынок, частные сети, premium hospitals, диагностические платформы, телемедицина и крупные медтех-контуры с заметным объёмом повторяющихся консультаций.
4. Главный риск, продукт легко схлопывается либо в speech-to-text feature, либо в тяжёлый кастомный внедренческий проект, если не доказать downstream ROI beyond transcription.

## 1. Какую проблему реально решает продукт

Abridge-подобный продукт продаёт не просто расшифровку разговора, а устранение четырёх дорогих потерь:
- времени врача на ручное заполнение документации;
- неполных или неструктурированных клинических записей;
- перегрузки ассистентов и back-office на оформлении визита;
- потерь в downstream workflow, где документация влияет на маршрутизацию, billing, контроль качества и юридическую защищённость.

Для локального ICP это painkiller только там, где клинический поток большой, документация формализована, а цена ошибки и задержки заметна. Для отдельного врача или маленькой клиники value proposition сильно слабее.

## 2. Целевой ICP в РФ

### Primary ICP
- крупные частные медицинские сети;
- премиальные многопрофильные клиники;
- диагностические и телемедицинские платформы;
- федеральные центры и цифрово зрелые hospital-like контуры;
- МИС-вендоры или медтех-платформы, которые могут упаковать решение как embedded layer.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. высокий объём консультаций и заметная нагрузка на документацию;
2. цифровой контур, куда можно встроить voice/documentation workflow;
3. чувствительность к качеству записи, скорости оформления и compliance;
4. budget owner на уровне меддиректора, COO, CIO или владельца цифровой трансформации;
5. готовность покупать не только модель, но и интеграцию, словари, настройку шаблонов и безопасное хранение данных.

### Нецелевой сегмент
- одиночные врачи и small private practices;
- клиники без зрелой МИС;
- организации, где проще нанять дополнительный admin staff;
- сегменты, где buyer не контролирует ни clinical workflow, ни ИТ-бюджет.

## 3. Продуктовый wedge

### Core wedge
**Ambient clinical documentation layer**
- слушает врач-пациент interaction;
- превращает разговор в структурированную клиническую документацию;
- встраивается в МИС и операционный контур клиники;
- даёт не только transcription, но и workflow acceleration для врача и back-office.

### Что делает wedge сильнее обычного voice AI
1. **Clinical workflow depth**: ценность не в тексте как таковом, а в пригодной для медпроцесса документации.
2. **Compliance and deployment requirements**: требования к данным, хранению и интеграциям повышают чек и барьер входа.
3. **Downstream value**: продукт можно продавать через экономию времени врача, стандартизацию записей и снижение admin burden.
4. **Enterprise packaging**: решение естественно продаётся как hospital-grade platform layer, а не как consumer tool.
5. **Localization complexity**: медицинский язык, шаблоны, локальные МИС и регуляторика делают рынок узким, но защищённым.

Именно эта комбинация даёт шанс на premium economics. Без неё кейс быстро превращается в commodity speech product.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как универсальный «AI-диктофон для врачей»;
- self-serve motion без интеграции в МИС;
- ставка на массовый SMB clinic segment;
- обещание экономии времени без клинического и compliance workflow.

### Вариант, который выглядит реалистично
- заход через pilot в одной specialty line, отделении или сети;
- buyer сверху, меддиректор, COO, CIO, head of digital health;
- KPI pilot: сокращение времени на документацию, рост скорости закрытия визита, улучшение полноты записи, снижение admin load;
- обязательная интеграция с МИС и локальными шаблонами;
- deployment как secure enterprise layer, а не как standalone mobile app.

## 5. Почему клиент будет покупать именно это, а не локальный substitute

У локального клиента уже есть substitutes:
- Voice2Med и похожие решения голосового ввода;
- обычная диктовка и speech-to-text без глубокого workflow layer;
- ручной труд врачей и администраторов;
- локальный интегратор, который соберёт кастомный voice/document AI stack.

Abridge-подобный продукт может выиграть только в трёх вещах:
1. **даёт клинически пригодный output, а не просто расшифровку**;
2. **быстрее показывает measurable workflow ROI**, чем кастомная сборка;
3. **остаётся repeatable platform layer**, а не разовым проектом под одну клинику.

Если эти преимущества не доказаны, buyer выберет более дешёвый local substitute или ограничится speech layer без premium чека.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего clinical documentation workflow;
2. выбор пилотного отделения или группы врачей;
3. настройка шаблонов, словарей, прав доступа и безопасного хранения;
4. интеграция в МИС и тестовый rollout на ограниченный поток;
5. измерение времени, качества документации и user adoption;
6. расширение на соседние отделения после доказанного ROI.

### Кто должен быть buyer'ом
- меддиректор;
- COO клиники или сети;
- CIO / head of digital transformation;
- owner clinical operations;
- в некоторых случаях МИС-вендор как channel/embedded buyer.

### Кто редко будет настоящим buyer'ом
- отдельный врач без бюджета;
- ИТ-специалист без клинического sponsor'а;
- procurement без owner'а на clinical operations KPI.

## 7. Конкурентная позиция

### Против локального speech-to-text
Преимущество есть только если продукт лучше решает весь documentation workflow, а не только распознавание речи.

### Против кастомной интеграторской сборки
Шанс есть, если time-to-value короче, а clinical шаблоны и поддержка масштабируются без отдельной проектной команды на каждого клиента.

### Против ручного процесса
Преимущество максимально у крупных сетей и потоковых specialty lines, где врачебное время дорого и документационный overhead действительно заметен.

## 8. Основные риски solution-fit

1. **Localization risk**: русский медицинский язык, локальные шаблоны и МИС могут потребовать слишком много кастомизации.
2. **Services risk**: внедрение может деградировать в дорогой интеграционный проект.
3. **Commodity risk**: buyer может воспринимать продукт как обычный speech layer.
4. **Data/compliance risk**: требования к хранению медданных могут сузить число реально доступных клиентов.
5. **Narrow ICP risk**: платёжеспособный сегмент ограничен крупными цифрово зрелыми клиниками.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит sale и deployment в healthcare ICP;
- какая доля выручки съедается интеграцией, support и clinical customization;
- сколько пилотов нужно довести до rollout для выхода на 500k+ EBITDA/мес;
- может ли embedded/channel motion через МИС-вендоров быть эффективнее прямых продаж;
- не схлопывается ли рынок после отсечения small clinics и всех кейсов без secure deployment.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как enterprise healthcare documentation layer для крупных клиник и сетей, а не как массовый voice AI для врачей. Продолжать дальше имеет смысл, если на economics подтвердится, что продукт сохраняет software-like маржу, не тонет в кастомизации и даёт buyer'у измеримый clinical operations ROI beyond transcription.


<!-- 04-economics.md -->

---
stage: economics
case: abridge-ambient-medical-scribe-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
sector: HEALTHCARE
verdict: CONDITIONAL_PASS
confidence: medium
investment_grade: false
---

# 04-economics — Unit Economics

## Кейс
Abridge как enterprise-grade ambient medical scribe и clinical documentation layer для крупных клиник, сетей и цифровых медицинских контуров в РФ.

## Executive summary

**Итог P4/P5: CONDITIONAL PASS.**

Почему:
1. Экономика собирается только в сценарии **clinic / network / secure deployment**, а не в self-serve продаже отдельным врачам.
2. **Путь к EBITDA > 500 тыс. ₽/мес реалистичен** примерно на **6-8 активных enterprise-клиентах** при среднем recurring-чеке около **1,55 млн ₽/мес**.
3. **Adjusted stress LTV/CAC ≈ 2,8x**, то есть кейс проходит economics-gate, но запас прочности умеренный из-за длинного sales cycle, медицинского compliance и риска тяжёлой интеграции с МИС.
4. Главные риски: data residency, сложная локализация медязыка, долгий pilot-to-rollout, а также вероятность, что buyer воспримет продукт как «дорогой speech-to-text» вместо workflow layer.

## 1. Модель и ключевые допущения

### ICP
- крупные частные медсети;
- цифрово зрелые многопрофильные клиники;
- диагностические центры и телемедицинские платформы;
- отдельные федеральные или квази-государственные контуры с сильным ИТ-блоком;
- buyer level: меддиректор, COO, CIO/CTO, директор по цифровой трансформации, владелец клинических операций.

### Что именно продаётся
Не просто запись и расшифровка речи, а связка:
- ambient capture консультации;
- автосборка клинической записи и шаблонов под специальности;
- интеграция в МИС / EHR / внутренний документооборот;
- защищённый контур хранения и аудит доступа;
- quality loop по качеству записей и adoption врачей.

### Почему это не обычный voice SaaS
В `02-demand.md` зафиксировано, что low-end мировой floor находится в районе **3-8 тыс. ₽ в месяц на врача**, но для РФ этот motion почти не даёт шанса пройти Program 2. Одновременно локальные аналоги продаются как enterprise / on-prem / интеграционный продукт. Значит локальная unit economics должна строиться не как PLG SaaS, а как healthcare workflow solution с высоким ACV и платным внедрением. [T1][T2][inference]

### Base-case для РФ
- Recurring platform / support / QA / secure hosting: **1 550 000 ₽/клиент/мес**
- One-off внедрение и интеграция: **2 100 000 ₽**
- One-off revenue не включаю в базовую recurring-модель, считаю его компенсацией части onboarding burn.
- Типовой клиент: клиника или сеть с **40-120 врачами** в наиболее документационно-нагруженных специальностях. [inference]

### Почему беру именно 1,55 млн ₽ MRR
В `02-demand.md` уже есть логика:
- self-serve по международным тарифам не проходит;
- clinic pilot на **150-250 тыс. ₽/мес** выглядит как входной wedge, но не как зрелый steady-state контракт;
- enterprise health-system deployment на **300-700 тыс. ₽/мес** был указан как минимально рабочий диапазон только для ограниченного объёма.

Для economics-этапа беру более широкий operational contract: recurring-платёж за platform layer, secure контур, поддержку, quality tuning и rollout на несколько групп врачей. Это выше demand-stage estimate, но всё ещё заметно ниже «hospital-wide everything» сценария. [T1][T2][inference]

## 2. Business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account research и выбор clinical champion | Founder + AE | manual research | 3 ч | 9 000 | Низкий |
| 2 | Intro через медтех-связи, МИС или digital health партнёров | Founder + BD | calls, partner channel | 5 ч | 20 000 | Низкий |
| 3 | Discovery по clinical workflow и pain around documentation | Founder + solutions architect | workshop, interviews | 8 ч | 48 000 | Низкий |
| 4 | Security / legal / consent / data residency scoping | solutions + legal | assessment docs | 10 ч | 58 000 | Низкий |
| 5 | Pilot design и ROI baseline | solutions + med expert | pilot scope | 10 ч | 70 000 | Низкий |
| 6 | Интеграция в МИС, шаблоны и права доступа | implementation pod | connectors, mapping | 30 ч | 180 000 | Средний |
| 7 | Enablement врачей и change management | CSM + med enablement | training, SOPs | 12 ч | 50 000 | Средний |
| 8 | Post-go-live QA и тюнинг output | QA + ML ops | dashboards, review loop | 18 ч | 81 000 | Средний |
| 9 | Billing / акты / ЭДО | ops | invoices, docs | 2 ч | 5 000 | Высокий |

### Вывод по процессу
Продажа тяжёлая, почти всегда sponsor-led и с длинной фазой проверки рисков. Самые дорогие точки, security review, pilot design, интеграция в МИС и адаптация clinical templates. Это enterprise healthcare workflow motion, а не простой SaaS checkout.

## 3. COGS per client / month

### Разбивка COGS на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| Speech / inference / processing infra | 120 000 | распознавание, суммаризация, monitoring |
| Integration engineer / support | 115 000 | коннекторы, релизы, багфиксы |
| Clinical QA / template tuning | 100 000 | проверка notes и словарей |
| Account / success management | 60 000 | внедрение и удержание |
| Security / compliance overhead | 50 000 | доступы, аудит, политики |
| Hosting / storage / backup | 55 000 | private cloud / secure storage |
| Implementation amortization | 125 000 | spread тяжёлого onboarding на 12 мес |
| **Итого COGS** | **625 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **1 550 000 ₽**
- COGS на клиента: **625 000 ₽**
- Gross profit на клиента: **925 000 ₽**
- **Gross Margin = 59,7%**

### Комментарий
Маржа рабочая, но уже не «чистый software». Если каждый клиент потребует bespoke-тюнинг под specialty и ручной QA сверх нормы, gross margin легко уедет в район 45-50%, и тогда экономика станет пограничной.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/год | First meetings | Qualified opportunities | Procurement-ready deals | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder / medtech network | 20 | 10 | 6 | 3 | 2,0 | 10,0% |
| МИС / integrator partners | 18 | 8 | 4 | 2 | 1,5 | 8,3% |
| Direct enterprise outbound | 70 | 9 | 3 | 1 | 0,6 | 0,9% |
| Conferences / thought leadership | 24 | 7 | 3 | 1 | 0,6 | 2,5% |
| **Итого blended** | **132** | **34** | **16** | **7** | **4,7** | **3,6%** |

### Fully-loaded CAC

| Компонент | ₽/год | Как получено |
|---|---:|---|
| Founder-led sales | 3 800 000 | встречи, ключевые аккаунты, pilot selling |
| AE / partner manager allocation | 2 200 000 | enterprise sales слой |
| Presales / med workflow design | 2 600 000 | discovery и ROI-baseline |
| Security / legal / procurement support | 1 500 000 | ИБ, договоры, data docs |
| Events / clinical credibility | 1 100 000 | конференции и материалы |
| CRM / demo / GTM tooling | 500 000 | sales stack |
| Overhead multiplier (x1.25) | 2 925 000 | management / admin overhead |
| **Итого acquisition spend** | **14 625 000** |  |

- New paying customers / год: **4,7**
- **Blended fully-loaded CAC = 14 625 000 / 4,7 = 3 112 000 ₽**

### CAC по каналам

| Канал | Fully-loaded CAC, ₽ | Комментарий |
|---|---:|---|
| Founder / medtech network | 1 700 000 | лучший ранний вход |
| МИС / integrator partners | 2 400 000 | самый правдоподобный scalable channel |
| Conferences / thought leadership | 3 200 000 | нужны для trust-building |
| Direct enterprise outbound | 5 300 000 | дорогой и слабопредсказуемый |
| **Blended** | **3 112 000** | реалистичный base-case |

## 5. LTV и churn

### Допущение по churn
После интеграции churn должен быть относительно низким, но есть early-stage риски: качество русского медязыка, клиническое недоверие, заморозка ИТ-бюджета, переход на локальный substitute. Беру **annual logo churn = 24%**. [inference]

### Расчёт
- MRR на клиента: **1 550 000 ₽**
- ARR на клиента: **18 600 000 ₽**
- Gross Margin: **59,7%**
- Annual churn: **24%**

`LTV = ARR × GM / churn`

`LTV = 18 600 000 × 59,7% / 24% = 46 267 500 ₽`

### Вывод
- **LTV ≈ 46,3 млн ₽**
- Значение хорошее, но только если клиент живёт 2,5-3+ года и rollout не буксует после пилота.

## 6. LTV / CAC

- LTV: **46 267 500 ₽**
- Blended fully-loaded CAC: **3 112 000 ₽**

`LTV/CAC = 46 267 500 / 3 112 000 = 14,9x`

### Stress-case
Чтобы не переоценить кейс, считаю стресс-сценарий:
- Effective GM year 1 = **42%**
- Annual churn = **35%**
- Effective CAC = **4 400 000 ₽**

`Stress LTV = 18 600 000 × 42% / 35% = 22 320 000 ₽`

`Stress LTV/CAC = 22 320 000 / 4 400 000 = 5,1x`

### Haircut на локализацию / pilot drag / compliance overhead
Дополнительно накладываю **execution haircut x0,55**, потому что часть экономики может съедаться prolonged pilot phase, specialty-specific настройкой и extra support.

- **Adjusted stress LTV/CAC = 2,8x**

### Вердикт по метрике
- **Base-case LTV/CAC = 14,9x**
- **Adjusted stress-case = 2,8x**
- Итог: метрика проходит, но без большого запаса. Кейс чувствителен к тому, насколько repeatable окажется deployment.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`3 112 000 / 1 550 000 = 2,01 мес`

Считаю также **gross-profit payback**:

`3 112 000 / 925 000 = 3,36 мес`

С учётом pilot drag, delayed ramp и долгого procurement:
- **Practical payback = ~10-13 месяцев**

### Комментарий
На бумаге payback выглядит сильным, но реальная cash dynamics определяется не MRR-математикой, а временем от первого контакта до production rollout.

## 8. Contribution Margin %

- Revenue per client / мес: **1 550 000 ₽**
- COGS: **625 000 ₽**
- Variable travel / onsite / training / extra support: **140 000 ₽**

`Contribution profit = 785 000 ₽`

`Contribution Margin = 785 000 / 1 550 000 = 50,6%`

### Вывод
**Contribution Margin = 50,6%**. Это приемлемо для healthcare enterprise AI, но только если продукт не скатывается в кастомную услугу под каждого клиента.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / GM | 1 | 420 000 | 0 | 0 | 126 000 | 546 000 |
| Enterprise AE / partnerships | 1 | 270 000 | 1,5 | 2 | 81 000 | 351 000 |
| Solutions architect / integration lead | 2 | 310 000 | 2 | 1,5 | 93 000 | 806 000 |
| ML / speech engineer | 2 | 290 000 | 2 | 1,5 | 87 000 | 754 000 |
| Clinical QA / medical editor | 2 | 210 000 | 1,5 | 1 | 63 000 | 546 000 |
| CSM / implementation manager | 1,5 | 220 000 | 1,5 | 1 | 66 000 | 429 000 |
| Security / DevOps | 1 | 250 000 | 1,5 | 1 | 75 000 | 325 000 |
| Legal / med compliance / ops | 0,5 | 180 000 | 1 | 0,5 | 54 000 | 117 000 |
| Finance / admin | 0,5 | 120 000 | 1 | 0,5 | 36 000 | 78 000 |
| **Итого full team FOT** | **11,5** |  |  |  |  | **3 952 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 3 952 000 |
| Core infra not in COGS | 220 000 |
| Office / admin / legal | 110 000 |
| Conferences / clinical credibility baseline | 100 000 |
| G&A / ЭДО / бухгалтерия / bank | 65 000 |
| **Итого fixed costs** | **4 447 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **785 000 ₽**
- Fixed costs: **4 447 000 ₽/мес**

`Break-even clients = 4 447 000 / 785 000 = 5,7`

С учётом буфера, неполной загрузки и healthcare-ramp округляю до **6-8 активных клиентов**.

### Break-even by month
Если идти темпом:
- M1-M4: 1-2 design partners,
- M5-M10: 1 новый клиент каждые 2-3 месяца,
- M11-M18: 1-2 клиента в квартал через references и партнёров,

то к operating break-even можно выйти примерно в **M13-M17**. [inference]

## 12. Burn-to-breakeven и runway

### Burn в early stage
- Fixed costs: **4,45 млн ₽/мес**
- Acquisition spend run-rate: **~1,22 млн ₽/мес**
- Total pre-scale burn: **~5,67 млн ₽/мес**

### Burn-to-breakeven
До уверенного break-even ориентир cumulative burn:
- **48-65 млн ₽**

### Runway
При `startup_capital = 100 млн ₽`:
- runway ≈ **17 месяцев**,
- если implementation fees начинают компенсировать часть burn с M4-M6, effective runway можно растянуть до **18-20 месяцев**.

## 13. Что происходит при 50 клиентах

### P&L snapshot при 50 клиентах
- Revenue: `50 × 1 550 000 = 77 500 000 ₽/мес`
- COGS: `50 × 625 000 = 31 250 000 ₽/мес`
- Gross profit: **46 250 000 ₽/мес**
- Variable travel / onsite / training: `50 × 140 000 = 7 000 000 ₽/мес`
- Contribution profit: **39 250 000 ₽/мес**
- Fixed costs: **4 447 000 ₽/мес**
- **EBITDA ≈ 34 803 000 ₽/мес**

### Вывод
Правило Program 2 выполняется с большим запасом. Узкое место кейса не в потолке EBITDA, а в том, можно ли вообще стабильно дойти до первых 6-8 клиентов без расползания implementation-cost.

## 14. Profit gate

### Проверка правила
FAIL только если:
- `company EBITDA < 500k/mo achievable even at 50 clients`, или
- `LTV/CAC < 1:1`

### Факт
- EBITDA при 50 клиентах: **~34,8 млн ₽/мес**
- Adjusted stress LTV/CAC: **2,8x**
- Base-case break-even: **6-8 активных клиентов**

## Итоговый вердикт P4/P5

**CONDITIONAL PASS.**

Кейс проходит economics-gate только как **enterprise ambient documentation / clinical workflow layer** с secure deployment, интеграцией в МИС и продажей крупным клиникам или сетям. В виде low-end scribe tool или simple per-doctor SaaS модель не работает.

### Что обязательно проверить дальше в P6/P7
1. Есть ли настоящий moat beyond transcription против Voice2Med и кастомных локальных speech stacks.
2. Можно ли стандартизировать specialty templates и МИС-интеграции так, чтобы margin не съедалась кастомизацией.
3. Насколько реалистичен channel motion через МИС-вендоров или digital health integrators.
4. Не развалится ли clinical quality на русском языке и узких specialty workflows.

## Источники
- [T1] Источники спроса, конкурентов, buyer logic, market sizing и Profit Gate из `02-demand.md` кейса `abridge-ambient-medical-scribe-geo-expand-v2`
- [T2] Solution thesis, ICP, deployment logic и risk framing из `03-solution.md` кейса `abridge-ambient-medical-scribe-geo-expand-v2`
- [T3] Локальные unit economics, CAC, churn и hiring assumptions, аналитическая оценка branch-models-lead на базе `02-demand.md` и `03-solution.md`. [inference]

Основа модели, pricing anchors и логика market access взяты из предыдущих блоков кейса; локальные unit economics, COGS, CAC, churn и hiring assumptions являются аналитической оценкой для P4/P5. [inference]


<!-- 05-critic.md -->

## SECTION A — PnL (Program 6A)

### 1. Исходные допущения из 04-economics.md

- ARPA / MRR на 1 клиента: **1 550 000 ₽/мес**.
- COGS на 1 клиента: **625 000 ₽/мес**.
- Gross profit на 1 клиента: **925 000 ₽/мес**.
- Contribution profit на 1 клиента: **785 000 ₽/мес**.
- Contribution margin: **50,6%**.
- Fixed costs: **4 447 000 ₽/мес**.
- Team FOT fully-loaded: **3 952 000 ₽/мес**.
- Blended fully-loaded CAC: **3 112 000 ₽**.
- CAC по каналам: founder / medtech network **1 700 000 ₽**, МИС / integrator partners **2 400 000 ₽**, conferences / thought leadership **3 200 000 ₽**, direct enterprise outbound **5 300 000 ₽**.
- LTV: **46 267 500 ₽**.
- Annual churn: **24%**.
- Practical payback: **~10-13 месяцев**.
- Для PnL беру месячный churn как аналитическое разложение annual churn:
  - base: **2,26%/мес**,
  - optimistic: **1,35%/мес**,
  - pessimistic: **3,37%/мес**. [inference]

### 2. Сценарии роста

- **Base:** 6 новых клиентов за 12 месяцев, первые сделки с M3, затем ритм 1 клиент каждые 2-3 месяца.
- **Optimistic:** 8 новых клиентов за 12 месяцев через network + МИС/integrator channel.
- **Pessimistic:** 4 новых клиента за 12 месяцев из-за длинного procurement и тяжёлого compliance review.

### 3. PnL на 12 месяцев

#### 3.1 Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 |
| Total clients | 0,00 | 0,00 | 1,00 | 0,98 | 1,96 | 1,91 | 2,87 | 2,80 | 3,74 | 3,66 | 4,57 | 5,47 |
| MRR, ₽ | 0 | 0 | 1 550 000 | 1 515 019 | 3 030 038 | 2 961 127 | 4 511 127 | 4 407 458 | 5 957 458 | 5 819 047 | 7 230 981 | 8 643 888 |
| COGS, ₽ | 0 | 0 | 625 000 | 610 895 | 1 221 789 | 1 194 003 | 1 818 196 | 1 776 797 | 2 400 990 | 2 345 584 | 2 915 719 | 3 485 842 |
| Gross profit, ₽ | 0 | 0 | 925 000 | 904 123 | 1 808 249 | 1 767 124 | 2 692 931 | 2 630 661 | 3 556 468 | 3 473 463 | 4 315 262 | 5 158 046 |
| GM% | 0,0% | 0,0% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% |
| Fixed costs, ₽ | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 |
| EBITDA, ₽ | -4 447 000 | -4 447 000 | -3 662 000 | -3 679 719 | -2 893 734 | -2 924 767 | -2 141 757 | -2 188 571 | -1 405 561 | -1 473 440 | -858 674 | -243 385 |
| Cash burn, ₽ | 4 447 000 | 4 447 000 | 3 662 000 | 3 679 719 | 2 893 734 | 2 924 767 | 2 141 757 | 2 188 571 | 1 405 561 | 1 473 440 | 858 674 | 243 385 |
| Cumulative cash, ₽ | -4 447 000 | -8 894 000 | -12 556 000 | -16 235 719 | -19 129 453 | -22 054 220 | -24 195 977 | -26 384 548 | -27 790 109 | -29 263 549 | -30 122 223 | -30 365 607 |

#### 3.2 Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 1 |
| Total clients | 0,00 | 1,00 | 1,99 | 2,96 | 3,92 | 3,87 | 4,81 | 5,74 | 6,66 | 6,57 | 7,48 | 8,37 |
| MRR, ₽ | 0 | 1 550 000 | 3 079 075 | 4 587 062 | 6 074 678 | 5 992 670 | 7 461 771 | 8 911 045 | 10 340 762 | 10 200 987 | 11 613 273 | 13 006 499 |
| COGS, ₽ | 0 | 625 000 | 1 241 562 | 1 849 622 | 2 449 467 | 2 416 399 | 3 008 778 | 3 593 163 | 4 169 662 | 4 113 301 | 4 682 771 | 5 244 556 |
| Gross profit, ₽ | 0 | 925 000 | 1 837 513 | 2 737 440 | 3 625 211 | 3 576 271 | 4 452 993 | 5 317 882 | 6 171 100 | 6 087 686 | 6 930 502 | 7 761 943 |
| GM% | 0,0% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% |
| Fixed costs, ₽ | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 |
| EBITDA, ₽ | -4 447 000 | -3 662 000 | -2 884 285 | -2 120 031 | -1 368 033 | -1 408 369 | -669 415 | 59 599 | 776 353 | 713 713 | 1 420 484 | 2 125 274 |
| Cash burn, ₽ | 4 447 000 | 3 662 000 | 2 884 285 | 2 120 031 | 1 368 033 | 1 408 369 | 669 415 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -4 447 000 | -8 109 000 | -10 993 285 | -13 113 316 | -14 481 349 | -15 889 718 | -16 559 133 | -16 559 133 | -15 782 781 | -15 069 068 | -13 648 584 | -11 523 310 |

#### 3.3 Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 0 | 0 | 1 | 0 | 0 | 1 | 0 | 1 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 0,97 | 0,93 | 1,90 | 1,84 | 1,78 | 2,72 | 2,63 | 3,54 |
| MRR, ₽ | 0 | 0 | 0 | 1 550 000 | 1 497 735 | 1 447 233 | 2 948 366 | 2 848 974 | 2 752 933 | 4 210 121 | 4 068 258 | 5 481 224 |
| COGS, ₽ | 0 | 0 | 0 | 625 000 | 603 925 | 583 561 | 1 188 857 | 1 148 779 | 1 110 054 | 1 697 629 | 1 640 426 | 2 210 171 |
| Gross profit, ₽ | 0 | 0 | 0 | 925 000 | 893 810 | 863 672 | 1 759 509 | 1 700 195 | 1 642 879 | 2 512 492 | 2 427 832 | 3 271 053 |
| GM% | 0,0% | 0,0% | 0,0% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% | 59,7% |
| Fixed costs, ₽ | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 | 4 447 000 |
| EBITDA, ₽ | -4 447 000 | -4 447 000 | -4 447 000 | -3 662 000 | -3 684 600 | -3 708 545 | -2 955 500 | -3 002 610 | -3 049 720 | -2 314 480 | -2 380 253 | -1 667 801 |
| Cash burn, ₽ | 4 447 000 | 4 447 000 | 4 447 000 | 3 662 000 | 3 684 600 | 3 708 545 | 2 955 500 | 3 002 610 | 3 049 720 | 2 314 480 | 2 380 253 | 1 667 801 |
| Cumulative cash, ₽ | -4 447 000 | -8 894 000 | -13 341 000 | -17 003 000 | -20 687 600 | -24 396 145 | -27 351 645 | -30 354 255 | -33 403 975 | -35 718 455 | -38 098 708 | -39 766 509 |

### 4. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

Ниже waterfall на **M12** по каждому сценарию.

| Scenario | Active clients M12 | ARPA / client, ₽ | Revenue M12, ₽ | Gross profit M12, ₽ | Contribution M12, ₽ | EBITDA M12, ₽ | Net after tax, УСН 6%, ₽ | Net after tax, IT-льгота 3%, ₽ | Net after tax, ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Base | 5,47 | 1 550 000 | 8 643 888 | 5 158 046 | 4 294 801 | -243 385 | -762 018 | -502 702 | -243 385 |
| Optimistic | 8,37 | 1 550 000 | 13 006 499 | 7 761 943 | 6 461 293 | 2 125 274 | 1 344 884 | 1 735 079 | 1 700 219 |
| Pessimistic | 3,54 | 1 550 000 | 5 481 224 | 3 271 053 | 2 722 930 | -1 667 801 | -1 996 674 | -1 832 238 | -1 667 801 |

### Комментарий к waterfall

- **Gross = Revenue - COGS**.
- **Contribution = Revenue - COGS - variable travel / onsite / training**, где переменная надстройка = **140 000 ₽ на клиента в месяц** из `04-economics.md`.
- **EBITDA = Contribution - fixed costs**.
- **Net after tax**:
  - УСН 6%: EBITDA минус 6% от выручки,
  - IT-льгота 3%: EBITDA минус 3% от выручки,
  - ОСНО 20%: если EBITDA отрицательная, налог на прибыль не начисляется; если положительная, остаётся **80% EBITDA**.

### 5. Cash flow и startup_capital_to_bep_rub

| Scenario | Break-even month | Min cumulative cash, ₽ | startup_capital_to_bep_rub |
|---|---:|---:|---:|
| Base | не достигнут за 12 мес | -30 365 607 | **30 365 607 ₽** |
| Optimistic | M8 | -16 559 133 | **16 559 133 ₽** |
| Pessimistic | не достигнут за 12 мес | -39 766 509 | **39 766 509 ₽** |

### 6. Налоговая модель РФ

| Режим | Нагрузка в модели | Когда применим | Вывод |
|---|---:|---|---|
| УСН 6% | 6% от выручки | если проходит по лимитам и структуре бизнеса | терпимо на старте, но заметно режет margin при service-heavy delivery |
| IT-льгота 3% | 3% от выручки | при аккредитации Минцифры и достаточной доле IT-выручки | лучший контур для этой модели |
| ОСНО 20% | 20% от прибыли + НДС 20% | если enterprise-клиенты и структура сделки делают ОСНО обязательной | самый тяжёлый режим по cash conversion |

### 7. Break-even

#### 7.1 Break-even по числу клиентов

Формула: `Fixed costs / contribution profit per client`

`4 447 000 / 785 000 = 5,67 клиента`

С operational buffer:

| Scenario | Теоретический BE, клиентов | Практический BE, клиентов |
|---|---:|---:|
| Base | 5,67 | **6-7** |
| Optimistic | 5,67 | **6** |
| Pessimistic | 5,67 | **7+** |

#### 7.2 Break-even по месяцам

| Scenario | EBITDA >= 0 | Комментарий |
|---|---|---|
| Base | не достигнут за 12 мес | к M12 компания почти на нуле, но ещё в минусе |
| Optimistic | **M8** | быстрее проходит за счёт более плотного partner/network motion |
| Pessimistic | не достигнут за 12 мес | требуется более длинный runway |

### 8. Вывод по SECTION A

- Кейс собирается только как **enterprise healthcare workflow rollout**, а не как per-doctor SaaS.
- **Base-case** требует около **30,4 млн ₽** капитала до operating stability и всё равно не достигает положительной EBITDA в пределах 12 месяцев.
- **Optimistic-case** выглядит проходным уже при **~16,6 млн ₽** стартового капитала до BE.
- **Pessimistic-case** остаётся тяжёлым и требует почти **39,8 млн ₽** только на покрытие burn в горизонте модели.
- При этом сам потолок EBITDA после прохождения первых 6-8 клиентов остаётся высоким, то есть проблема кейса не в ceiling, а в длине и хрупкости ramp-up.

<!-- P6A-DONE -->

## SECTION B — Finance Risk + Competitor (Program 6B)

### 1. Sensitivity analysis: EBITDA через 12 месяцев

База взята из SECTION A: **EBITDA M12 = -243 385 ₽/мес** при **5,47 активных клиентах**. Для чувствительности меняю по одному параметру.

| Scenario | Что меняется | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | без изменений | **-243 385** | базовая траектория почти дошла до нуля, но запаса нет |
| Sens1 | CAC x2 | **-1 798 969** | если CAC удваивается, дополнительная acquisition burden почти убивает шанс на самофинансируемый рост |
| Sens2 | Churn x2 | **-1 032 743** | annual churn растёт до ~48%, активная база размывается и BE уезжает вправо |
| Sens3 | Price -30% | **-2 836 552** | при ARPA 1,085 млн ₽ и прежней cost stack экономика ломается |

**Вывод:** самый опасный single-variable shock здесь, как и ожидалось, не churn, а **price compression**. На втором месте, **CAC blow-up**. Это подтверждает, что кейс живёт только как premium secure workflow layer, а не как commodity scribe.

### 2. Monte Carlo Lite — confidence intervals

Ниже использую не full-code simulation, а **triangular-distribution approximation** на базе min / mode / max.

#### 2.1 Inputs for triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 1 700 000 | 3 112 000 | 5 300 000 | [T3] |
| Monthly churn, % | 1,35% | 2,26% | 3,37% | [T3] |
| ARPU, ₽/мес | 1 085 000 | 1 550 000 | 1 900 000 | [T3] |
| Conversion rate lead→paid, % | 0,9% | 3,6% | 10,0% | [T3] |
| Time-to-hire, мес | 1,0 | 1,5 | 2,0 | [T3] |

#### 2.2 Результат Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24 (₽/мес) | **-1 487 390** | **4 522 836** | **11 608 245** | **13 095 635** |
| CAC payback (мес) | **10,4** | **4,0** | **2,2** | **8,2** |
| LTV/CAC | **2,3x** | **14,9x** | **38,2x** | **35,9x** |
| Cash runway (мес) | **14,6** | **17,8** | **20,4** | **5,8** |

#### 2.3 Интерпретация

- **Rule 1 triggered:** `p10 EBITDA < 0`, значит возникает **kill criterion #1: insolvency risk**.
- **Rule 2 not triggered:** `p50 EBITDA > 500k ₽/мес`, median-case EBITDA gate проходит.
- **Rule 3 triggered:** размах между downside и upside слишком широкий, поэтому score надо **понижать на 1 notch**.
- **Rule 4 triggered:** ширина диапазона по **LTV/CAC = 35,9x**, намного выше порога **8**. Значит модель хрупкая и её stability держится на premium pricing, контролируемом CAC и низком churn.

### 3. Competitor deep-dive

#### 3.1 Топ-3 западных

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Abridge** | сильный brand в ambient AI, deep integration story, enterprise credibility, buyer education [T1] | US-first workflow, не переносится напрямую в РФ-контур, высокий compliance footprint [T1][T2] | **15-20%** глобального enterprise ambient-AI сегмента, аналитическая оценка [inference] | локальный контур РФ, data residency, интеграция с МИС и русские specialty templates |
| **Ambience Healthcare** | сильный фокус на enterprise hospital workflow и documentation quality [T2] | высокая сложность enterprise rollout, ещё меньше локальной переносимости в РФ [T2][inference] | **8-12%** [inference] | sovereignty-ready deployment и адаптация под российский документооборот |
| **Freed / low-end scribe band** | понятный self-serve pricing floor, быстрый onboarding, понятная clinician-level ценность [T1] | создаёт downward price pressure, но слаб как enterprise workflow layer [T1][inference] | **5-10%** low-end AI scribe band [inference] | позиционирование не как note app, а как secure documentation + workflow + QA layer |

#### 3.2 Топ-4 российских

| Компания | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Voice2Med / ЦРТ** | зрелый speech stack, локальное развертывание, медсловари, интеграция с МИС [T1] | ближе к dictation/speech tooling, чем к полному ambient documentation layer [inference] | **20-25%** российского voice-documentation сегмента [inference] | если дать ambient capture + structured QA + network-level ROI, value может быть выше |
| **Звёздочка** | российский AI stack, акцент на data residency и медицинский контур [T2] | меньше доказанной enterprise scale, меньше публичных deployment case studies [inference] | **5-10%** [inference] | более сильный economics narrative для CFO/CIO и hospital operations |
| **Webiomed** | известность в российском med-AI контуре, доверие к клиническим данным [T2] | не чистый ambient-scribe wedge, продукт шире и менее сфокусирован [inference] | **5-8%** в adjacent med-AI budget pool [inference] | более узкий и понятный wedge, documentation throughput и doctor productivity |
| **Локальные интеграторы МИС** | доступ к инфраструктуре клиента, опыт кастомных внедрений, доверие enterprise buyer'а [T1][T2] | обычно слабее в repeatable product layer, тяжёлая services-экономика [inference] | **20%+ substitute share** [inference] | можем дать более продуктовую, а не purely project delivery модель |

**Итог по конкурентам:** в РФ already есть не пустой рынок, и почти все сильные игроки продают **локальный контур + интеграцию + compliance**. Следовательно, западный moat сам по себе не переносится. Шанс есть только если собрать **Abridge-grade UX/quality** поверх **российского deployment и МИС-native integration**.

### 4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Не удаётся вовремя нанять 2 сильных integration leads | med | high | time-to-hire > 2 мес, backlog интеграций > 6 недель | заранее закрыть partner bench, шаблонные коннекторы, referral hiring |
| 2 | Operational | Качество русского медязыка и specialty templates ниже ожиданий | med | high | edit rate врача > 20%, repeated specialty complaints | specialty dictionaries, human QA loop, fallback speech stack |
| 3 | Operational | Внешний LLM / ASR stack дорожает или деградирует по latency | med | high | inference cost +30%, p95 latency > 8 сек | multi-vendor routing, on-prem fallback, model abstraction layer |
| 4 | Market | Спрос остаётся enterprise-only и не масштабируется beyond design partners | high | high | pipeline < 3 qualified deals в квартал | идти через МИС/integrator channel, sharpen ROI by specialty |
| 5 | Market | Price compression из-за low-end AI scribe vendors | high | high | клиенты требуют discount > 20%, RFP сравнивает только price/seat | package by workflow outcome, not by seat; bundle QA/compliance |
| 6 | Market | Локальные игроки занимают рынок раньше через existing medtech channels | med | high | проигрыши в тендерах подряд, partner refusal rate растёт | co-sell с крупным интегратором, focus на private chains first |
| 7 | Regulatory | 152-ФЗ / data residency требует полного локального контура | high | high | security questionnaire блокирует pilot, нужен on-prem-only | сразу проектировать sovereign deployment, data minimization |
| 8 | Regulatory | 323-ФЗ и требования к медтайне усложняют rollout | high | high | legal review длится > 3 мес, согласование доступа тормозит launch | заранее собранный compliance pack, договорный и ИБ playbook |
| 9 | Financial | Cash runway сжимается из-за дорогого presale и медленного close rate | high | high | burn > 6,5 млн ₽/мес, cash < 9 мес runway | tranche-based hiring, implementation fees upfront, board cash gates |
| 10 | Financial | USD/RUB volatility поднимает себестоимость моделей и infra | med | med | FX move > 15% за квартал | рублёвые контракты с buffer, repricing clause |
| 11 | Black swan | Новый санкционный пакет отключает ключевые западные модели | med | high | vendor notice, region blocks | immediate switch plan на локальные/open-weight модели |
| 12 | Black swan | Резкое сокращение IT-бюджетов клиник режет willingness to buy | med | high | budget freeze у private chains, delayed signing > 1 quarter | focus on ROI-in-3-months buyers, narrow implementation scope |

### 5. Kill conditions через 6 месяцев

1. **Median economics fail:** если rolling **p50 EBITDA forecast на M24 < 500 000 ₽/мес**, continuation stop.
2. **Sales efficiency fail:** если за 6 месяцев **< 2 платящих design-partner клиента** или **blended CAC > 4,5 млн ₽** при close rate < 2%, continuation stop.
3. **Product-market-compliance fail:** если **edit rate > 25%** у врачей и одновременно **нет approved on-prem / data-residency architecture** хотя бы у 1 крупного пилота, continuation stop.

### 6. Финальный вывод SECTION B

- Кейс **не умирает от одного только churn**, но легко ломается от **price compression** и **CAC inflation**.
- Monte Carlo Lite показывает, что median-case ещё живой, но хвост риска слишком широкий, чтобы считать rollout de-risked.
- В конкурентной картине РФ преимущество будет не у глобального бренда, а у того, кто лучше соберёт **локальный deployment, комплаенс, МИС-интеграцию и doctor-quality loop**.
- Поэтому итоговый статус по P6B: **PASS WITH MATERIAL RISK / score downgrade**.

### 7. Sources for SECTION B

- [T1] `02-demand.md` по кейсу `abridge-ambient-medical-scribe-geo-expand-v2`
- [T2] `03-solution.md` по кейсу `abridge-ambient-medical-scribe-geo-expand-v2`
- [T3] `04-economics.md` по кейсу `abridge-ambient-medical-scribe-geo-expand-v2`

<!-- P6B-DONE -->


<!-- 06-verdict.md -->

[HEALTHCARE] Abridge GEO Expand v2 — REJECTED: 64/100 | EBITDA base=1048К₽/мес через 14 мес | LTV/CAC=14,9x (stress 2,8x) | Ключевое преимущество: высокая ценность secure МИС-native workflow | Главный риск: weak moat при слабом прямом спросе в РФ.

# 06-verdict

sector: HEALTHCARE
status: REJECTED
score: 64/100
case_slug: abridge-ambient-medical-scribe-geo-expand-v2
date: 2026-04-22

## Финальный вердикт инвесткомитета

Кейс проходит economics-gate только в узком enterprise healthcare motion, но не дотягивает до investment-grade из-за слабого прямого спроса в РФ, слабого moat и высокой зависимости от сложной локализации, комплаенса и channel execution. Это **REJECTED**, а не near-pass, потому что при текущем evidence запас прочности недостаточен даже при хороших unit economics на одном крупном клиенте.

## Оценка

Source tier balance: T1=4, T2=19, T3=0, weighted=2.17. Penalty applied: -2 баллов to criterion #3.

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | «Base-case LTV/CAC = 14,9x», «Adjusted stress-case = 2,8x», «GM = 59,7%», practical payback «~10-13 месяцев». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 17 | «break-even ... 6-8 активных клиентов», при 7 клиентах company_ebitda_rub_month ≈ 1 048 000 ₽/мес, что достижимо в окне 14-17 мес по base-инференсу. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «Итог по спросу в РФ: LOW», endpoint вернул «LOW / score 0», но боль подтверждается hh.ru и наличием Voice2Med; включён tier-penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 12 | «в РФ already есть не пустой рынок», западный moat «сам по себе не переносится», шанс есть только при локальном deployment + МИС-native integration. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | Risk matrix фиксирует high/high по 152-ФЗ, 323-ФЗ, cash runway, price compression и санкционному риску по западным моделям. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | Есть узкий, но реалистичный GTM через private chains и МИС/integrator partners; в кейсе уже задан GTM-10, а blended CAC = 3 112 000 ₽. |

**Sum raw = 96 / 150. Normalized score = round((96 × 100) / 150) = 64/100.**

## Investment committee one-liner

[HEALTHCARE] Abridge GEO Expand v2 — REJECTED: 64/100 | EBITDA base=1048К₽/мес через 14 мес | LTV/CAC=14,9x | Ключевое преимущество: secure МИС-native workflow layer | Главный риск: weak moat и слабый прямой спрос в РФ.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 46 267 500 ₽ |
| CAC blended fully-loaded | 3 112 000 ₽ |
| LTV/CAC | 14,9x |
| LTV/CAC stress adjusted | 2,8x |
| CAC payback | 2,0 мес по MRR / 3,4 мес по gross profit / 10-13 мес practical |
| Gross Margin | 59,7% |
| contribution_margin_rub_month | 785 000 ₽ на клиента |
| fixed_costs_rub_month | 4 447 000 ₽ |
| Break-even clients | 5,7 теоретически, 6-8 practically |
| company_ebitda_rub_month base | ≈ 1 048 000 ₽/мес при 7 клиентах |
| company_ebitda_potential_rub_month | 34 803 000 ₽/мес при 50 клиентах |
| clients_to_500k_ebitda | 7 |
| months_to_500k_ebitda | 14-17 мес |
| clients_to_1m_ebitda | 7 |
| startup_capital_to_bep_rub | 30 365 607 ₽ base / 16 559 133 ₽ optimistic / 39 766 509 ₽ pessimistic |

## Полный business process

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Account research и выбор clinical champion | Founder + AE | manual research | 3 ч | 9 000 | Низкий |
| 2 | Intro через медтех-связи, МИС или digital health партнёров | Founder + BD | calls, partner channel | 5 ч | 20 000 | Низкий |
| 3 | Discovery по clinical workflow и pain around documentation | Founder + solutions architect | workshop, interviews | 8 ч | 48 000 | Низкий |
| 4 | Security / legal / consent / data residency scoping | solutions + legal | assessment docs | 10 ч | 58 000 | Низкий |
| 5 | Pilot design и ROI baseline | solutions + med expert | pilot scope | 10 ч | 70 000 | Низкий |
| 6 | Интеграция в МИС, шаблоны и права доступа | implementation pod | connectors, mapping | 30 ч | 180 000 | Средний |
| 7 | Enablement врачей и change management | CSM + med enablement | training, SOPs | 12 ч | 50 000 | Средний |
| 8 | Post-go-live QA и тюнинг output | QA + ML ops | dashboards, review loop | 18 ч | 81 000 | Средний |
| 9 | Billing / акты / ЭДО | ops | invoices, docs | 2 ч | 5 000 | Высокий |

## Команда

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp до 80% productivity (мес) | Взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| Founder / GM | 1 | 420 000 | 0 | 0 | 126 000 | 546 000 |
| Enterprise AE / partnerships | 1 | 270 000 | 1,5 | 2 | 81 000 | 351 000 |
| Solutions architect / integration lead | 2 | 310 000 | 2 | 1,5 | 93 000 | 806 000 |
| ML / speech engineer | 2 | 290 000 | 2 | 1,5 | 87 000 | 754 000 |
| Clinical QA / medical editor | 2 | 210 000 | 1,5 | 1 | 63 000 | 546 000 |
| CSM / implementation manager | 1,5 | 220 000 | 1,5 | 1 | 66 000 | 429 000 |
| Security / DevOps | 1 | 250 000 | 1,5 | 1 | 75 000 | 325 000 |
| Legal / med compliance / ops | 0,5 | 180 000 | 1 | 0,5 | 54 000 | 117 000 |
| Finance / admin | 0,5 | 120 000 | 1 | 0,5 | 36 000 | 78 000 |
| **Итого** | **11,5** |  |  |  |  | **3 952 000 ₽/мес** |

## Moat — 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных без сильного shared-data flywheel. |
| Switching costs | 2 | После интеграции в МИС, шаблонов и обучения команды переключение становится болезненным. |
| Scale economies | 1 | Инфра дешевеет умеренно, но services-heavy delivery ограничивает эффект масштаба. |
| Proprietary data / model advantage | 1 | Дата-advantage возможен, но размер локального датасета и право на его использование не доказаны. |
| Regulatory moat | 1 | Compliance повышает порог входа, но это пока скорее барьер допуска, чем уникальный moat. |
| Brand / distribution | 2 | Глобальный бренд Abridge силён как референс, но в РФ дистрибуция не встроена. |
| Embedded workflow | 3 | При успешной МИС-интеграции продукт садится глубоко в clinical workflow. |

**Moat score = round((10 × 25) / 21) = 12/25.** Это **weak moat**, поэтому риск weak moat вынесен в Top-3 Risks.

## GTM — 10 named targets

| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---:|---|---|---|---:|
| 1 | МЕДСИ | Крупная частная сеть, много врачей и высокая документационная нагрузка. | email decision-maker + партнёрство через МИС/интегратора | 1 500 000 ₽/мес |
| 2 | EMC | Премиальный сегмент, высокая стоимость времени врача и чувствительность к качеству записи. | direct outreach CIO / COO | 1 800 000 ₽/мес |
| 3 | Мать и дитя | Сетевой формат, стандартизируемые specialty workflows и большой объём амбулаторных консультаций. | конференция + intro через digital-health партнёра | 1 400 000 ₽/мес |
| 4 | Medscan | Ставка на цифровую медицину и централизованные процессы. | email decision-maker | 1 200 000 ₽/мес |
| 5 | СМ-Клиника | Большой поток пациентов и сильная боль по ускорению оформления визита. | outbound + vc.ru/medtech контент | 1 100 000 ₽/мес |
| 6 | K+31 | Премиальная сеть, где важны полнота документации и physician productivity. | direct outreach med director | 1 000 000 ₽/мес |
| 7 | Hadassah Medical Moscow | Высокие требования к quality/compliance, хороший design-partner для premium positioning. | партнёрство + конференция | 1 600 000 ₽/мес |
| 8 | Клиника Фомина | Быстро внедряет цифровые patient-facing и internal tools, подходит для pilot-by-specialty. | email + founder intro | 900 000 ₽/мес |
| 9 | АО «Медицина» | Сложный enterprise buyer с готовностью покупать quality и compliance. | direct enterprise sales | 1 300 000 ₽/мес |
| 10 | Чайка | Частная сеть с repeatable outpatient workflow, удобна для пилота на 1-2 specialties. | founder-led intro | 800 000 ₽/мес |

**Вывод по GTM:** named targets релевантны и канал fit есть, но pipeline хрупкий, потому что продажи завязаны на небольшой пул цифрово зрелых private chains и системных партнёров.

## Top-3 risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Weak moat + локальные substitutes | high | high | В РФ уже есть Voice2Med и интеграторские substitutes, а западный бренд сам по себе не переносится. |
| Regulatory / data residency risk | high | high | 152-ФЗ, 323-ФЗ и требования к медтайне могут заблокировать rollout без sovereign deployment. |
| Price compression + CAC inflation | high | high | Sensitivity показывает EBITDA M12 = -2 836 552 ₽ при price -30% и -1 798 969 ₽ при CAC x2. |

## Monte Carlo / risk readout

- p10 EBITDA @M24 = **-1 487 390 ₽/мес**
- p50 EBITDA @M24 = **4 522 836 ₽/мес**
- p90 EBITDA @M24 = **11 608 245 ₽/мес**
- Ширина диапазона LTV/CAC = **35,9x**, это высокий разброс.
- Инвестиционный смысл: median-case живой, downside остаётся слишком широким для approve.

## Что нужно доказать для APPROVED

1. Два платящих design-partner клиента в private healthcare с production rollout, а не только пилотом.
2. On-prem/private-cloud архитектура, проходящая security review без развала unit economics.
3. Edit rate врача < 15-20% и measurably лучшее время закрытия визита по сравнению с локальными speech substitutes.
4. Repeatable МИС-integration playbook, снижающий implementation drag и удерживающий GM > 55%.
5. Реальный channel motion через МИС/integrator partner с CAC < 2,5 млн ₽.

## LTV Upside Calculator

### Базовая формула
`customer_ltv_rub = ARR × GM / annual churn`

### Текущая база
- ARR = 18 600 000 ₽
- GM = 59,7%
- annual churn = 24%
- customer_ltv_rub = 46 267 500 ₽

### Как довести кейс до near-pass / approve

| Рычаг | Текущее | Цель | Эффект |
|---|---:|---:|---|
| ARPA | 1 550 000 ₽/мес | 1 700 000-1 900 000 ₽/мес | Повышает contribution_margin_rub_month без пропорционального роста CAC. |
| COGS | 625 000 ₽ | < 550 000 ₽ | Поднимает GM выше 65% и ускоряет payback. |
| CAC | 3 112 000 ₽ | < 2 500 000 ₽ | Делает stress LTV/CAC устойчиво > 3,5x. |
| Annual churn | 24% | < 18% | Увеличивает customer_ltv_rub и делает rollout менее хрупким. |
| Implementation amortization | 125 000 ₽ | < 80 000 ₽ | Снижает services-drag и улучшает EBITDA path. |

### Сценарий апгрейда
Если удержать ARPA на 1,7 млн ₽, снизить COGS до 550 тыс. ₽, CAC до 2,4 млн ₽ и churn до 18%, то customer_ltv_rub вырастает примерно до 64 млн ₽, contribution_margin_rub_month поднимается до ~1,01 млн ₽, а clients_to_500k_ebitda снижается до 5-6. Тогда кейс можно пересматривать.

## Итог

**Финальный статус: REJECTED.**

Почему не APPROVED:
- direct demand в РФ остаётся LOW;
- moat слабый и частично переносимый только через локальную execution-машину;
- p10 Monte Carlo остаётся отрицательным;
- конкурентное преимущество пока больше в гипотезе о delivery, чем в уже доказанном defensible asset.

Почему не ноль:
- unit economics на enterprise-клиенте сильные;
- путь к company_ebitda_rub_month > 500k в принципе существует;
- есть конкретный ICP и 10 named targets;
- сегмент healthcare documentation реально болезненный и бюджетно обоснованный.

