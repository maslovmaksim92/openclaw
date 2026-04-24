# DeepIP Patent AI GEO Expand v2 — Full Verdict Dossier


---

# 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-deepip-patent-ai-geo-expand.md
created: 2026-04-20T12:12:13+03:00
---

# 01-intake

## Кейс
deepip-patent-ai-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — deepip-patent-ai-geo-expand

## Meta
- source: triage/triage-2026-04-14-deepip-patent-ai-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-deepip-patent-ai-geo-expand.md

## Классификация
новый сигнал, но кейс не открываем

## Решение
Не открывать новый кейс на этом этапе.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы не покрывают вертикаль patent AI / IP operations / patent prosecution как отдельную сервисную модель.
- Сигнал выглядит содержательным, но по экономике не проходит порог Program 1: в raw-файле указан `ltv_signal: 1200000-5000000 ₽ в год на клиента`, то есть примерно 100 000-417 000 руб. в месяц. Это ниже порога `> 500 000 руб./мес.`.
- GEO-EXPAND логика присутствует, но локализация отмечена как `hard`: для России потребуются адаптация под сервисы и процессы Роспатента, локальные патентные бюро, русскоязычные документы и отраслевые workflow в IP-операциях.
- В raw-файле нет достаточного подтверждения тяжёлого recurring service layer с высоким ежемесячным чеком, например managed implementation, интеграций, защищённого контура или регулярного сопровождения крупных корпоративных IP-портфелей.

## Что сделано
- Новый кейс не создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Пометка для следующего шага
Вернуться к теме, если появятся дополнительные сигналы, подтверждающие хотя бы один из пунктов:
- enterprise LTV уверенно выше 500 000 руб. в месяц на клиента или контур;
- заметный спрос со стороны крупных корпораций с большими IP-портфелями, а не только патентных фирм;
- тяжёлый сервисный слой: внедрение, интеграции, secure deployment, recurring сопровождение;
- российские или СНГ-сценарии, где patent AI становится не point solution, а операционным контуром.

## Вердикт
Сигнал интересный, но пока недостаточно сильный для открытия нового кейса в Program 1: LTV ниже порога, локализация тяжёлая, сервисная экономика не подтверждена.

```



---

# 02-demand.md

# 02-demand

## Вывод
**Статус спроса: LOW-MODERATE / нишевый, но платёжеспособный.**

По РФ это не массовый рынок, а узкий enterprise/professional сегмент: патентные бюро, крупные R&D-корпорации, in-house IP teams. Сигнал спроса слабый по широкой воронке, но есть признаки готовности платить в верхнем сегменте, если продукт локализован под Роспатент, русский язык, безопасный контур и Word/IPMS workflow.

## Demand signals
- `multi-demand(patent AI)` вернул **LOW**, score 15: Google Trends RU = 0, HH = 3 вакансии, Habr = 2, Yandex Suggest = 100. Это подтверждает слабый массовый спрос по самому термину. [T2 supporting, internal endpoint]
- `multi-demand(патентный бот)` / `патентный поиск` / `patent drafting` показывают ту же картину: широкого consumer-like спроса в РФ нет, спрос концентрирован в профессиональных workflow. [T2 supporting, internal endpoint]
- DeepIP на своём сайте указывает adoption у Am Law 100 и Fortune 500, а также кейсы с ~20% ростом эффективности drafting/prosecution во время trial. Это сильный глобальный WTP signal, но не прямое доказательство по РФ. [T2] https://www.deepip.ai/
- В РФ в 2025 году сохранялся объём патентной активности: за 11 месяцев подано **18 тыс. заявок на изобретения**, из них 5,5 тыс. от российских заявителей. Это подтверждает, что базовый workflow существует и не исчез. [T1] https://rospatent.gov.ru/ru/news/v-2025-godu-rospatent-prinyal-18-tys-zayavok-na-izobreteniya-1212
- В реестре Роспатента доступен большой корпус действующих патентных поверенных, то есть профессиональная buyer-base в стране существует. [T1] https://new.fips.ru/registers-web/action?acName=clickTree&currType=4b7a90b1-17e4-4f68-a4c0-8ff2ac56032c

## Конкуренты и цены
Минимум 3 реальных competitor/pricing points:

1. **Patent Bots**: Prosecution / Patent Analyzer от **$450/месяц**, Drafting tools от **$500/месяц**, combo от **$800/месяц**. Это прямой price anchor для AI-помощника патентного юриста. [T2] https://patentbots.com/pricing
2. **ClaimMaster**: solo annual plan около **$1995/год**, team/business pricing выше. Это нижний price anchor для productivity tooling вокруг claim review/drafting. [T2] https://www.patentclaimmaster.com/pricing/
3. **IP.com**: semantic/patent search pricing начинается примерно от **$99/месяц** за user-tier, enterprise выше. Это price anchor для search/research слоя. [T2] https://ip.com/products/
4. **Онлайн Патент (RU)**: сервис патентного поиска/регистрации, экспресс-проверка знака от **~9 900 ₽**, отдельные услуги регистрации кратно выше. Это не прямой AI competitor, но важный локальный willingness-to-pay benchmark в РФ. [T2] https://onlinepatent.ru/

### Что это значит
- Для SMB/solo IP lawyers рынок готов платить примерно **8-40 тыс. ₽/мес на пользователя**. [T2]
- Для team/enterprise legal ops реалистичен чек **100-300 тыс. ₽/мес на команду** при secure deployment, Word add-in, shared context, шаблонах под Роспатент и поддержке. Это inference из vendor price anchors и enterprise workflow complexity. **Пометка: inference.** [T2+T1]
- Для крупного enterprise/private deployment возможен чек **400-900 тыс. ₽/мес** вместе с внедрением, инфобезом и сопровождением. **Пометка: inference, high variance.** [T2]

## Telegram / RU bots & services
- Прямого крупного category-leading Telegram-бота по patent AI в РФ не видно; это отрицательный сигнал для массового спроса. [T2/T3, market scan]
- В РФ есть сервисы вокруг IP digital workflow, например **Онлайн Патент**, но их core-distribution не через Telegram. [T2] https://onlinepatent.ru/
- Вывод: Telegram как канал acquisition для этого кейса слабый; продавать надо через direct sales, партнёров, патентные бюро, legal/IP conferences. **Это снижает скорость органического роста.** [T2]

## WTP: proof of willingness to pay
1. **Глобально WTP подтверждён.** DeepIP пишет про использование Am Law 100 и Fortune 500, а также measurable efficiency gains в trial. [T2] https://www.deepip.ai/
2. **Рынок already pays за adjacent tooling.** Patent Bots, ClaimMaster, IP.com публикуют цены, значит категория software budget реально существует. [T2]
3. **В РФ already pay за IP automation/services.** Онлайн Патент и аналогичные игроки продают цифровые патентные услуги, хотя чаще как service-led bundle, а не AI seat. [T2]

Итог по WTP: **сильный за рубежом, умеренный в РФ, но достаточный для нишевого enterprise-case при правильной локализации.**

## Profit Gate (EBITDA >= 500k ₽/мес): проверка сценариев монетизации

### Сценарий A. Self-serve для solo/малых бюро
- Цена: 25-40 тыс. ₽/мес за seat.
- Чтобы получить EBITDA 500k ₽/мес при валовой марже ~75% и fixed costs 600-900k ₽/мес, нужно примерно 40-60 платящих seat-equivalent.
- Для РФ patent-AI спроса это выглядит тяжело и медленно. **FAIL.**

### Сценарий B. Team SaaS для патентных бюро
- Цена: 120-250 тыс. ₽/мес на фирму.
- При 8-10 клиентах и валовой марже 75-80% бизнес уже может выйти на EBITDA >500k ₽/мес.
- Достижимо, но только если есть локализация под Роспатент и хороший sales-led motion. **BORDERLINE PASS.**

### Сценарий C. Enterprise/private deployment для крупных корпораций
- Цена: 400-900 тыс. ₽/мес + setup/integration.
- 3-5 крупных клиентов достаточно для EBITDA >500k ₽/мес даже при heavier support load.
- Это реалистичный путь, если целиться в компании с постоянным patent pipeline и инфобез требованиями. **PASS.**

### Общий итог Profit Gate
**Profit Gate = PASS, но только через enterprise/service-led motion.** Массовый self-serve в РФ почти наверняка не работает.

## Market sizing

### Методика
Считаю двумя путями и беру более консервативное значение.

#### Top-down
- База мира: WIPO фиксирует около **3,7 млн** patent applications globally в 2024. [T1] https://www.wipo.int/web-publications/world-intellectual-property-indicators-2025/en/
- Addressable share для AI drafting/prosecution/copilot беру **10%**: это не весь рынок патентов, а только high-value professional workflow, где есть смысл покупать отдельный AI-инструмент. **Inference.** [T1+T2]
- Average software spend беру **$500/год на matter-equivalent** как консервативный blended proxy между low-end tools и enterprise bundle. **Inference from competitor pricing.** [T2]
- Курс USD беру по ЦБ РФ: **75,2370 ₽/$** на 21.04.2026. [T1] https://www.cbr.ru/currency_base/daily/

Расчёт:
- **TAM (мир)** = 3,7 млн × 10% × $500 × 75,237 = **13,9 млрд ₽** [T1+T2]
- База РФ: 18 тыс. заявок на изобретения за 11 месяцев 2025, annualized ~19,6 тыс.; для консервативности беру **18 тыс.** [T1]
- Addressable share в РФ = **35%** сложных/профессионально сопровождаемых заявок. **Inference.** [T1+T2]
- Blended software spend = **15 тыс. ₽ на matter/год**. [T2]
- **TAM (РФ, top-down)** = 18 000 × 35% × 15 000 ₽ = **94,5 млн ₽**
- **SAM (РФ, top-down)** = TAM × 70% (только бюро + крупные корпорации, где buying power выше) = **66,2 млн ₽**
- **SOM Y1 (top-down)** = 2% SAM = **1,3 млн ₽**
- **SOM Y3 (top-down)** = 8% SAM = **5,3 млн ₽**

#### Bottom-up
- Buyer universe: беру **220 организаций** как целевой список из крупных патентных бюро, активных IP boutiques и крупных корпораций с регулярным patent workflow в РФ. Это консервативный addressable-org estimate, не весь рынок. **[LOW CONFIDENCE]**, но опирается на реестр патентных поверенных Роспатента [T1], публичную активность IP firms [T2] и top filers/corps [T2].
- % with need = **55%**: не всем нужен AI layer, но у части есть объём drafting/prosecution и pressure на эффективность. [T1+T2]
- ARR avg = **900 тыс. ₽/год** на buyer (75 тыс. ₽/мес blended между SMB и enterprise-lite). [T2]
- **SAM (bottom-up)** = 220 × 55% × 900 000 ₽ = **108,9 млн ₽**
- **TAM (РФ, bottom-up)** для сравнения беру как 220 × 100% × 900 000 ₽ = **198,0 млн ₽**
- **SOM Y1 (bottom-up)** = 3% SAM = **3,3 млн ₽**
- **SOM Y3 (bottom-up)** = 10% SAM = **10,9 млн ₽**

### Таблица cross-check
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 13,9 млрд ₽ [T1+T2] | — | — | top-down |
| TAM (РФ) | 94,5 млн ₽ [T1+T2] | 198,0 млн ₽ [T1+T2, low confidence] | diff=2,1x, допустимо; bottom-up шире по buyer universe | **94,5 млн ₽** |
| SAM (РФ) | 66,2 млн ₽ [T1+T2] | 108,9 млн ₽ [T1+T2, low confidence] | diff=1,6x, в пределах sanity | **66,2 млн ₽** |
| SOM Y1 | 1,3 млн ₽ | 3,3 млн ₽ | diff=2,5x | **1,3 млн ₽** |
| SOM Y3 | 5,3 млн ₽ | 10,9 млн ₽ | diff=2,1x | **5,3 млн ₽** |

## 10 реальных buyers для bottom-up
1. Городисский и Партнёры [T2]
2. Онлайн Патент [T2]
3. PATENTUS [T2]
4. Semenov&Pevzner IP practice [T2]
5. Росатом [T2]
6. Ростех [T2]
7. Сбер [T2]
8. Яндекс [T2]
9. КАМАЗ [T2]
10. Татнефть [T2]

Это не полный рынок, а стартовый GTM-10 список для sales-led проверки.

## Риски
- Сильная локализация под Роспатент и русскоязычные drafting norms обязательна. [T1]
- Узкий buyer universe, длинный sales cycle, высокие требования к security/конфиденциальности. [T2]
- Telegram/discovery channel слабый, рынок не consumerized. [T2]

## Verdict for demand stage
**Не reject на этом этапе.**

Хотя composite demand по широкой воронке низкий, **Profit Gate проходит** в enterprise/private-deployment сценарии. Значит ранний reject по правилу `DEMAND=LOW AND Profit Gate FAIL` **не срабатывает**.

Рекомендация: двигать кейс дальше только как **нишевый enterprise/IP-ops продукт**, без иллюзии массового PLG в РФ.

Sources: T1=5, T2=9, T3=0. Primary evidence basis: T2 with T1 market anchors.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.


---

# 03-solution.md

---
stage: solution
case: deepip-patent-ai-geo-expand-v2
date: 2026-04-23
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
DeepIP как AI-native платформа для patent drafting, prosecution, search и portfolio intelligence при выходе на рынок РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. DeepIP решает не абстрактную задачу «AI для юристов», а тяжёлый патентный workflow: invention capture, patentability search, drafting, prosecution, risk assessment и portfolio intelligence. [T1][T2][T3][T4]
2. Для РФ рабочая гипотеза выглядит не как массовый legal SaaS, а как узкий **enterprise IP workflow layer** для патентных бюро, in-house IP-команд и R&D-heavy корпораций.
3. Наиболее реалистичный wedge, это вход через один дорогой workflow, где можно померить ROI: prior-art / disclosure prep / drafting / office action support, а потом расширяться в platform layer. [T2][T3][T4]
4. Главный риск, без локализации под Роспатент, русскоязычные документы и secure deployment кейс быстро схлопывается либо в point tool, либо в дорогую ручную услугу.

## 1. Какую проблему реально решает продукт

DeepIP продаёт не просто генерацию текста, а устранение дорогих потерь в patent/IP workflow:
- долгий сбор и структурирование invention disclosure; [T2]
- ручной prior-art search и novelty assessment; [T2]
- медленный drafting внутри Word с большим количеством рутинной доработки; [T3]
- перегруженный prosecution workflow по office actions; [T4]
- фрагментацию между drafting, prosecution, risk analysis и portfolio intelligence. [T1]

По официальному позиционированию компания делает ставку именно на end-to-end coverage и замену разрозненного набора инструментов единым AI-системным слоем. [T1]

Для локального ICP это painkiller только там, где patent work идёт регулярно и дорого. Для редких заявок value proposition намного слабее, потому что задачу проще закрыть внешним бюро или ручной работой.

## 2. Целевой ICP в РФ

### Primary ICP
- крупные патентные бюро и IP-консалтинг;
- in-house IP-команды в технологических, промышленных и фарма-компаниях;
- корпорации с постоянным invention pipeline и patent prosecution workload;
- legal/IP practices внутри больших юрфирм.

### Фильтр на ICP
Клиент подходит, если одновременно есть:
1. повторяемый объём patent workflow, а не единичные filing-задачи;
2. дорогой ручной труд патентных поверенных, инженеров и IP-юристов;
3. owner на стороне head of IP, patent counsel, practice lead или innovation director;
4. чувствительность к turnaround time, consistency и auditability результата;
5. готовность платить не только за seat, но и за настройку шаблонов, security, rollout и workflow integration.

### Нецелевой сегмент
- одиночные патентные поверенные без premium-бюджета;
- SMB с редкими патентными задачами;
- general legal teams без выделенной IP-функции;
- клиенты, которым дешевле купить разовую экспертизу, чем внедрять platform layer.

## 3. Продуктовый wedge

### Core wedge
**AI-native patent workflow platform**
- invention harvesting / disclosure enhancement; [T2]
- patentability и prior-art search; [T2]
- patent drafting внутри Microsoft Word; [T3]
- office action / prosecution support; [T4]
- portfolio intelligence и risk workflows. [T1]

### Что делает wedge сильнее обычного point tool
1. **Workflow depth.** DeepIP покрывает несколько дорогих этапов patent lifecycle, а не один use case. [T1]
2. **Word-native fit.** Важный плюс для юристов и бюро, продукт встроен в Microsoft Word, а не вынуждает работать через отдельный браузерный интерфейс. [T3]
3. **Enterprise/security story.** Компания подчёркивает enterprise-grade security, работу с law firms и Fortune 500, zero data retention и встроенность в существующие инструменты. [T1][T3]
4. **Service-to-platform bridge.** Можно зайти через один pilot-workflow и затем расшириться в более широкий operating layer.
5. **Verifiable output thesis.** DeepIP продаёт ускорение без полной замены эксперта, то есть это copilot для дорогого специалиста, а не low-end automation. [T1][T4]

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Что, вероятно, не взлетит
- generic позиционирование как «AI для патентных юристов»;
- self-serve seat-based motion;
- ставка на широкий inventors/SMB market;
- слабая адаптация под Роспатент, русский язык и локальные workflow.

### Что выглядит реалистично
- заход через один monetizable workflow: disclosure prep, prior-art, drafting или office-action support;
- top-down продажа в head of IP / patent practice lead / innovation director;
- pilot на 4-8 недель с KPI: меньше часов на кейс, быстрее turnaround, выше throughput на специалиста;
- private deployment или как минимум жёсткий security/governance contour;
- последующее расширение в единый IP operating layer после доказанного ROI.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У локального клиента уже есть substitutes:
- внешние патентные бюро;
- ручная работа in-house IP-команды;
- классические патентные базы и поиск;
- самосборка на general-purpose LLM;
- документы, шаблоны и knowledge base без единой workflow-логики.

DeepIP может выиграть только если одновременно докажет три вещи:
1. **заметно сокращает cycle time** по сравнению с ручным процессом; [T3][T4]
2. **лучше удерживает workflow continuity** между disclosure, drafting и prosecution, чем набор отдельных тулов; [T1]
3. **проходит security-проверку** у бюро и корпораций, где конфиденциальность и traceability критичны. [T1][T3]

Если этого нет, buyer рационально останется на комбинации «бюро + ручной поиск + точечные AI-помощники».

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего patent/IP workflow и bottleneck'ов;
2. выбор одного дорогого процесса с измеримым ROI;
3. настройка шаблонов, style controls, prompts и security-политик;
4. pilot на одной практике или in-house IP-команде;
5. сравнение turnaround time, expert-hours и качества output до/после;
6. rollout на соседние workflows после доказанного эффекта.

### Кто должен быть buyer'ом
- head of IP;
- chief IP counsel;
- руководитель патентной практики;
- innovation / R&D director;
- операционный руководитель патентного бюро.

### Кто редко будет настоящим buyer'ом
- одиночный исполнитель без бюджета;
- procurement без sponsor'а в IP-функции;
- general legal ops без прямой связи с patent workload.

## 7. Конкурентная позиция

### Против локальных патентных бюро
Преимущество возникает, если DeepIP помогает бюро делать больше кейсов на ту же команду и не разрушает economics billable work.

### Против ручной in-house работы
Шанс высокий, если платформа реально экономит часы на disclosure prep, drafting и office-action analysis. [T2][T3][T4]

### Против generic AI
Преимущество есть, если специализация на patent workflow, Word-native delivery и enterprise security дают лучший результат, чем general LLM stack. [T1][T3]

## 8. Основные риски solution-fit

1. **Локализационный риск.** Сейчас продукт явно заточен под major jurisdictions вроде USPTO, EPO и PCT; адаптация под российский контур не доказана. [T3][T4]
2. **Services risk.** В РФ внедрение может потребовать слишком много ручной настройки, шаблонов и экспертного сопровождения.
3. **Narrow ICP risk.** Платёжеспособный buyer universe в РФ узкий, это уже видно на demand-stage.
4. **Proof risk.** Без измеримого throughput uplift продукт выглядит как nice-to-have.
5. **Security/compliance risk.** Для части корпораций даже сильной security-story может быть недостаточно без локального размещения и отдельного контракта.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой ACV реалистичен для бюро, in-house IP и enterprise R&D buyers в РФ;
- сколько solution engineering и human-in-the-loop реально нужно на запуск;
- держится ли gross margin после локализации и enterprise deployment;
- сколько клиентов нужно для выхода на `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не растворяется ли software-layer в дорогом сервисном сопровождении.

## Итог для пайплайна

**P4 пройден условно.**

DeepIP выглядит жизнеспособным только как узкий enterprise IP workflow layer для high-frequency patent teams. Продолжать дальше имеет смысл, если на economics подтвердится premium-чек, повторяемый rollout и возможность не утонуть в кастомной локализации.

## Источники
- [T1] https://www.deepip.ai/why-us
- [T2] https://www.deepip.ai/products/ai-patentability
- [T3] https://www.deepip.ai/products/patent-drafting
- [T4] https://www.deepip.ai/products/patent-prosecution
- [T5] /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/deepip-patent-ai-geo-expand-v2/02-demand.md


---

# 04-economics.md

---
stage: unit-economics
case: deepip-patent-ai-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS_WITH_CAUTION
confidence: medium
---

# 04-economics

## Executive summary
**Итог: PASS WITH CAUTION.**

Для DeepIP-подобного кейса в РФ экономика собирается только как **enterprise-only patent workflow platform** с secure deployment, длинным sales cycle и дорогим внедрением. В базовом сценарии при **420 000 ₽ MRR на клиента** и fully-loaded blended CAC **1,27 млн ₽** модель даёт:

- **COGS / клиент / месяц:** **124 000 ₽**
- **Contribution Margin:** **70,5%**
- **Blended fully-loaded CAC:** **1,27 млн ₽**
- **LTV:** **14,8 млн ₽ gross profit**
- **LTV/CAC:** **11,65x**
- **CAC Payback:** **4,3 мес** по gross profit, **3,0 мес** по MRR
- **Break-even:** **22 клиента** или **9,24 млн ₽ MRR**
- **EBITDA при 50 клиентах:** около **8,44 млн ₽ / мес**

Вывод: Profit Gate проходит. Инвестиционная логика есть, но только в узком сегменте крупных патентных бюро и корпораций с постоянным patent/IP workflow. Главный риск не CAC, а узкий buyer universe и тяжёлая локализация под Роспатент.

## 1. Ключевые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Крупные патентные бюро, in-house IP-команды, R&D-heavy корпорации | Основано на 02-demand.md и 03-solution.md |
| Средний контракт | 5,04 млн ₽ ARR | 420 тыс. ₽ MRR на аккаунт |
| Onboarding fee | 900 тыс. ₽ one-off | Не включаю в обязательную recurring-экономику |
| MRR на клиента | 420 000 ₽ | Base case для team + enterprise-lite mix |
| COGS на клиента | 124 000 ₽ | LLM, hosting, support, solution engineering |
| Gross margin | 70,5% | После переменных затрат |
| Sales cycle | 6-9 мес | Enterprise legal / IP software motion |
| Monthly logo churn | 2,0% | Консервативно, чуть хуже good-quartile для high-ARPA SaaS |
| Startup capital | 45,0 млн ₽ | Нужно, чтобы дотянуть до break-even без кассового разрыва |

## 2. Подробный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list по бюро и корпорациям | SDR | CRM, СПАРК, ручной ресерч | 2,0 ч | 2 600 | частичная |
| 2 | Первый outbound touch / warm intro | SDR | CRM, почта, телефония, Telegram | 2,5 ч | 3 300 | частичная |
| 3 | Qualification call | SDR + AE | Телефония, CRM | 1,0 ч | 3 700 | низкая |
| 4 | Discovery по текущему patent workflow | AE | Zoom/Meet, discovery-шаблон | 1,5 ч | 5 900 | низкая |
| 5 | Product demo и ROI framing | AE + CEO | Demo env, презентация | 2,0 ч | 9 400 | частичная |
| 6 | Сбор sample matters / disclosure / office actions | AE + Solutions | Secure storage, dataroom | 3,0 ч | 11 200 | низкая |
| 7 | Pilot scoping и проектный план | Solutions + CTO | PM board, архитектурный шаблон | 2,5 ч | 12 800 | низкая |
| 8 | Настройка sandbox / template layer | Solutions + ML + DevOps | Cloud, monitoring, prompt/config layer | 8,0 ч | 31 500 | частичная |
| 9 | Pilot execution и quality review | Solutions + patent analyst | QA checklist, review queue | 12,0 ч | 42 000 | частичная |
| 10 | Security / procurement review | CTO + AE | Dataroom, policy docs, security questionnaire | 4,0 ч | 18 500 | низкая |
| 11 | Коммерческое предложение и переговоры | AE + CEO | CRM, CPQ, docs | 2,0 ч | 8 900 | частичная |
| 12 | Contracting / legal review | CEO + external legal | ЭДО, шаблон договора | 3,0 ч | 16 000 | низкая |
| 13 | Счёт и закрывающие документы | Finance/Ops | 1С, банк-клиент, ЭДО | 0,7 ч | 2 300 | высокая |
| 14 | Оплата и go-live | Finance + CSM | Банк-клиент, CRM reminders, onboarding board | 1,5 ч | 5 800 | высокая |

**Итого прямой process cost-to-close:** около **174 600 ₽** на клиента до fully-loaded CAC. Самая дорогая часть, это pilot, security review и solution setup, а не реклама.

## 3. COGS breakdown на клиента в месяц

Базовая выручка на клиента: **420 000 ₽ MRR**.

| Компонент COGS | ₽ / клиент / мес | Как получено | Источник |
|---|---:|---|---|
| Cloud / hosting / secure storage | 28 000 | inference для enterprise workload + isolated storage | T1 + inference |
| LLM / embeddings / OCR / search | 24 000 | inference для drafting + search + prosecution workloads | T1 + T2 |
| Support / CSM allocation | 22 000 | 1 CSM на ~15-18 клиентов | T6 + inference |
| Solutions / implementation amortization | 26 000 | onboarding labor размазан на 12 мес | T6 + inference |
| Patent QA / human review | 14 000 | human-in-the-loop quality control | T1 + inference |
| Security / audit / monitoring | 7 000 | логи, backup, policy tooling | T1 + inference |
| Billing / admin variable | 3 000 | ЭДО, биллинг, документооборот | inference |
| **Итого COGS** | **124 000** |  |  |

**Gross profit / клиент / мес = 420 000 - 124 000 = 296 000 ₽.**

## 4. CAC по acquisition channels с funnel conversion

### 4.1 CAC по каналам

| Канал | Spend / мес, ₽ | Leads / мес | Meeting rate | SQL rate | Pilot rate | Win rate | New paying customers / мес | CAC / клиент, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound enterprise | 1 360 000 | 140 | 12% | 35% | 40% | 20% | 1,18 | 1 152 542 |
| Партнёрства / IP conferences | 720 000 | 22 | 45% | 45% | 35% | 22% | 0,35 | 2 057 143 |
| Inbound content / founder-led | 460 000 | 18 | 35% | 45% | 38% | 25% | 0,27 | 1 703 704 |

### 4.2 Blended funnel

| Метрика | Значение |
|---|---:|
| Общий spend / мес | 2 540 000 ₽ |
| Leads / мес | 180 |
| Meetings | 33 |
| SQL | 10 |
| Pilots | 4 |
| Wins | 1,8 |
| **Blended channel CAC** | **1 411 111 ₽** |

Вывод: channel CAC выше всего у партнёрств, зато этот канал повышает качество сделок. Для scale-up опорным должен быть outbound + founder-led inbound, а events, как поддерживающий слой.

## 5. FULLY-LOADED CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Таблица расчёта

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | брендовый спрос + pain-keywords по patent/IP automation | T3 + inference |
| Outbound team FOT (SDR/AE attributed to new) | 624 000 | 1 SDR 180k + 1 AE 300k + 30% соцвзносы | T4, T5 |
| Marketing team FOT (partial allocation) | 208 000 | 0,4 founder marketing + 0,4 content/demand gen, fully-loaded | inference |
| Tools (CRM, sales stack, телефония, ЭДО) | 88 000 | amo/HubSpot-like CRM, телефония, sales automation, ЭДО | inference |
| Events / partnerships | 220 000 | 1 профильное событие/мес + партнёрские активности | inference |
| **Subtotal raw CAC spend** | **1 320 000** | сумма прямых acquisition cost |  |
| Overhead multiplier (x1.3) | 396 000 | enterprise B2B overhead на presale, management, admin | task standard |
| **Fully-loaded CAC** | **1 716 000** | raw CAC × 1,3 |  |

### Коррекция на фактический win-rate и blended funnel

В enterprise legal/IP motion 1,8 wins/мес из blended funnel выглядит слишком оптимистично для ранней команды. Для инвесткомитета беру **консервативный normalised new customer rate = 1,35 клиента/мес**, то есть запас на удлинение procurement и legal cycle.

`Normalized blended CAC = 1 716 000 / 1,35 = 1 271 111 ₽`

### Sanity checks
- Сегмент: **enterprise (>500k ₽ ACV)**, значит использовать multiplier ниже x1.3 было бы слишком агрессивно, но x2.0-x2.5 дал бы завышение, потому что часть продаж идёт в team/enterprise-lite, а не только в Fortune-500-like корпорации.
- Полученный normalized CAC **1,27 млн ₽** выше указанного в задаче RU benchmark **300-900k ₽** для enterprise SaaS, то есть underestimate нет. Это допустимо из-за узкого ICP, pilot-heavy presale и security review.
- CAC payback по gross profit получается существенно ниже 12 мес, значит юнит-экономика у premium-чека держится.

## 6. LTV и churn benchmark

### Benchmark churn source
ChartMogul показывает, что для SaaS с **ARPA > $1k/мес** monthly customer churn у **top quartile** около **1,1%**, у **median** около **1,8%**, у нижнего квартиля около **3,5%**. Для российского niche enterprise legal/IP software беру **2,0% monthly logo churn** как консервативный base case, то есть чуть хуже median/high-ARPA global benchmark из-за локализационного риска и узкого buyer universe.

Источник: ChartMogul, customer churn benchmarks by ARPA range, https://chartmogul.com/saas-metrics/revenue-churn/

### Расчёт LTV

| Метрика | Формула | Значение |
|---|---|---:|
| MRR / клиент | — | 420 000 ₽ |
| Gross margin | — | 70,5% |
| Gross profit / мес | 420 000 × 70,5% | 296 000 ₽ |
| Monthly churn | benchmark | 2,0% |
| Lifetime, мес | 1 / 0,02 | 50,0 |
| **LTV (gross profit)** | 296 000 / 0,02 | **14 800 000 ₽** |
| LTV (revenue basis) | 420 000 / 0,02 | 21 000 000 ₽ |

## 7. LTV/CAC, CAC Payback, Contribution Margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 14,8 млн / 1,271 млн | **11,65x** | сильно выше порога 3,0x |
| CAC Payback | 1,271 млн / 296 тыс. | **4,3 мес** | хорошо для enterprise |
| CAC Payback (MRR basis) | 1,271 млн / 420 тыс. | **3,0 мес** | sanity-check из задачи пройден |
| Contribution Margin % | 296 / 420 | **70,5%** | хороший уровень для B2B software + services |
| EBITDA @ 50 clients | 50 × 296 тыс. - fixed costs | **≈ 8,44 млн ₽ / мес** | Profit Gate пройден |

## 8. Team & FOT

### 8.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | enterprise sales, fundraising, ключевые сделки | 600 000 | 180 000 | 780 000 |
| CTO / Tech Lead | архитектура, security, enterprise rollout | 650 000 | 195 000 | 845 000 |
| Senior Backend #1 | core platform | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | integrations / workflow | 420 000 | 126 000 | 546 000 |
| ML Engineer | retrieval, drafting quality, evaluation | 500 000 | 150 000 | 650 000 |
| DevOps | infra / CI/CD / secure deployment | 350 000 | 105 000 | 455 000 |
| Frontend | internal UI / workflow cockpit | 300 000 | 90 000 | 390 000 |
| SDR | target accounts, outbound | 180 000 | 54 000 | 234 000 |
| AE | discovery, pilots, close | 300 000 | 90 000 | 390 000 |
| Customer Success | onboarding, retention, expansion | 240 000 | 72 000 | 312 000 |
| Patent Solutions / Analyst | pilot delivery, QA, шаблоны | 240 000 | 72 000 | 312 000 |
| **Итого** |  |  |  | **5 460 000 ₽ / мес** |

### 8.2 Таблица найма с realism check

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 650 000 | 2-3 | 2 | 195 000 | 845 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 + бонус | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 300 000 + комиссия | 1-2 | 2-3 | 90 000 | 390 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Patent Solutions / Analyst | 1 | 240 000 | 1-2 | 1 | 72 000 | 312 000 |

**Salary benchmark notes:**
- Senior backend: HH показывает московские вилки вроде **300-600k ₽** для senior backend, что поддерживает принятые **420k gross**. T4.
- SDR: HH показывает вилки **100-180k ₽** для IT/SaaS SDR, что поддерживает **180k gross**. T5.
- DevOps: HH показывает senior DevOps около **350k ₽** и выше, что поддерживает **350k gross**. T6.
- CTO: HH-страницы по CTO в Москве показывают **600-850k ₽**, что поддерживает **650k gross**. T7.

## 9. Cumulative FOT timeline M1-M12

Нанимаю команду ступенчато, без нереалистичного найма 5+ человек в первый месяц.

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO, CTO, Backend #1 | 1 859 000 |
| M2 | состав без изменений, идёт поиск Frontend и SDR | 1 859 000 |
| M3 | + Frontend, SDR, DevOps | 2 756 000 |
| M4 | + AE, Patent Solutions | 3 367 000 |
| M5 | + ML Engineer, Customer Success | 4 329 000 |
| M6 | ramp existing team, без новых ролей | 4 329 000 |
| M7 | + Backend #2 | 4 875 000 |
| M8 | команда укомплектована | 5 460 000 |
| M9 | команда укомплектована | 5 460 000 |
| M10 | команда укомплектована | 5 460 000 |
| M11 | команда укомплектована | 5 460 000 |
| M12 | команда укомплектована | 5 460 000 |

## 10. Fixed costs breakdown

| Компонент | ₽ / мес |
|---|---:|
| Full team FOT | 5 460 000 |
| Office / admin / бухгалтерия | 180 000 |
| Core infra not in COGS | 220 000 |
| Legal / audit / compliance | 140 000 |
| Internal software stack | 110 000 |
| Misc reserve | 90 000 |
| **Итого fixed costs** | **6 200 000 ₽ / мес** |

## 11. Break-even по клиентам и по месяцам

### 11.1 Break-even по client count

| Метрика | Формула | Значение |
|---|---|---:|
| Contribution / клиент / мес | 420 000 - 124 000 | 296 000 ₽ |
| Fixed costs / мес | — | 6 200 000 ₽ |
| **Break-even clients** | 6 200 000 / 296 000 | **20,95** |
| **Округлённый break-even** | — | **22 клиента** |
| **Break-even MRR** | 22 × 420 000 | **9 240 000 ₽ / мес** |

### 11.2 Break-even по месяцам

Допущение по привлечению платящих клиентов: M1-M3 ноль, дальше 1, 1, 2, 2, 3, 3, 4, 4, 4 клиентов. К концу M12 база = **24 клиента**.

| Месяц | Клиентов на конец месяца | Gross profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 2 599 000 | -2 599 000 |
| M2 | 0 | 0 | 2 599 000 | -2 599 000 |
| M3 | 0 | 0 | 3 496 000 | -3 496 000 |
| M4 | 1 | 296 000 | 4 107 000 | -3 811 000 |
| M5 | 2 | 592 000 | 5 069 000 | -4 477 000 |
| M6 | 4 | 1 184 000 | 5 069 000 | -3 885 000 |
| M7 | 6 | 1 776 000 | 5 615 000 | -3 839 000 |
| M8 | 9 | 2 664 000 | 6 200 000 | -3 536 000 |
| M9 | 12 | 3 552 000 | 6 200 000 | -2 648 000 |
| M10 | 16 | 4 736 000 | 6 200 000 | -1 464 000 |
| M11 | 20 | 5 920 000 | 6 200 000 | -280 000 |
| M12 | 24 | 7 104 000 | 6 200 000 | **904 000** |

**Вывод:** операционный break-even достигается примерно в **M12**.

## 12. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Суммарный отрицательный EBITDA до выхода в плюс, это примерно **32,6 млн ₽**. Добавляю резерв на непредвиденные задержки procurement и hiring, итого нужен капитал не ниже **40-45 млн ₽**.

### Cash runway
При startup capital = **45 млн ₽**:
- средний burn за первые 12 месяцев ≈ **2,72 млн ₽ / мес**;
- runway ≈ **16,5 месяца**;
- при задержке выхода на 24 клиента на 2-3 месяца запас остаётся, но без агрессивного расширения команды.

### Sanity checks
- Hire-plan не нарушает правило 5+ человек в первый месяц.
- FOT M1 уже **1,86 млн ₽**, что выглядит реалистично для founder + CTO + senior backend.
- Startup capital до break-even **45 млн ₽**, то есть выше red-flag уровня 10 млн ₽ для B2B enterprise SaaS.

## 13. Profit Gate check

| Проверка | Результат |
|---|---|
| EBITDA > 500k ₽/мес achievable even at 50 clients? | **Да.** При 50 клиентах EBITDA ≈ **8,44 млн ₽/мес** |
| LTV/CAC >= 1:1? | **Да.** 11,65x |
| LTV/CAC >= 3:1 investment grade? | **Да.** 11,65x |
| CAC Payback < 12 мес (или <18 enterprise)? | **Да.** 4,3 мес |

**Profit Gate = PASS.**

## 14. Главные риски модели

1. **Narrow-market risk.** Юнит-экономика хорошая, но SAM в РФ ограничен, поэтому потолок масштабирования ниже типичного venture SaaS.
2. **Localization risk.** Любая серьёзная адаптация под Роспатент и русскоязычный drafting может съесть часть gross margin.
3. **Pilot-to-prod risk.** Если pilot win-rate упадёт ниже ~15%, CAC быстро уйдёт выше 2 млн ₽.
4. **Founder dependency.** Первые сделки будут сильно зависеть от founder-led sales и личного enterprise closing.

## Итог

**Вердикт по P5: PASS WITH CAUTION.**

Кейс не надо отклонять по unit economics. При enterprise-only positioning, premium чеке и дисциплинированном найме экономика держится уверенно. Но это не широкий софтверный рынок, а узкий investment thesis на несколько десятков качественных клиентов в РФ.

## Sources
- **T1** DeepIP product / enterprise positioning: https://www.deepip.ai/why-us
- **T2** DeepIP drafting / prosecution workflow pages: https://www.deepip.ai/products/patent-drafting , https://www.deepip.ai/products/patent-prosecution
- **T3** 02-demand.md, pricing anchors and RU demand notes: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/deepip-patent-ai-geo-expand-v2/02-demand.md
- **T4** HH.ru senior backend salary market: https://hh.ru/vacancies/senior-backend-developer
- **T5** HH.ru SDR salary examples: https://hh.ru/vacancy/129774256
- **T6** HH.ru senior DevOps salary market: https://hh.ru/vacancies/senior-devops/za_sutki
- **T7** HH.ru CTO salary example: https://hh.ru/vacancy/125002805
- **T8** ChartMogul churn benchmarks: https://chartmogul.com/saas-metrics/revenue-churn/


---

# 05-critic.md

# SECTION A. Finance PnL
## 1. Допущения для 3 сценариев
| Параметр | Base | Optimistic | Pessimistic |
|---|---:|---:|---:|
| ARPA / MRR на клиента, ₽/мес | 420 000 | 441 000 | 399 000 |
| COGS на клиента, ₽/мес | 124 000 | 120 000 | 130 000 |
| Gross profit / клиент / мес, ₽ | 296 000 | 321 000 | 269 000 |
| Monthly churn | 2.0% | 1.5% | 3.0% |
| New clients by month | 0,0,0,1,1,2,2,3,3,4,4,4 | 0,0,1,1,2,2,3,3,4,4,5,5 | 0,0,0,0,1,1,1,2,2,3,3,3 |
| Fixed costs used in model, ₽/мес | ramp from 2 599 000 to 6 200 000 | same ramp | same ramp |

## 2.1 Базовый сценарий: 12-месячный PnL
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 |
| Total clients | 0 | 0 | 0 | 1 | 2 | 3.9 | 5.9 | 8.7 | 11.6 | 15.3 | 19 | 22.7 |
| MRR, ₽ | 0 | 0 | 0 | 420 000 | 831 600 | 1 654 968 | 2 461 869 | 3 672 631 | 4 859 179 | 6 441 995 | 7 993 155 | 9 513 292 |
| COGS, ₽ | 0 | 0 | 0 | 124 000 | 245 520 | 488 610 | 726 837 | 1 084 301 | 1 434 615 | 1 901 922 | 2 359 884 | 2 808 686 |
| Gross profit, ₽ | 0 | 0 | 0 | 296 000 | 586 080 | 1 166 358 | 1 735 031 | 2 588 331 | 3 424 564 | 4 540 073 | 5 633 271 | 6 704 606 |
| GM % | 0.0% | 0.0% | 0.0% | 70.5% | 70.5% | 70.5% | 70.5% | 70.5% | 70.5% | 70.5% | 70.5% | 70.5% |
| Fixed costs, ₽ | 2 599 000 | 2 599 000 | 3 496 000 | 4 107 000 | 5 069 000 | 5 069 000 | 5 615 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 |
| EBITDA, ₽ | -2 599 000 | -2 599 000 | -3 496 000 | -3 811 000 | -4 482 920 | -3 902 642 | -3 879 969 | -3 611 669 | -2 775 436 | -1 659 927 | -566 729 | 504 606 |
| Cash burn, ₽ | 2 599 000 | 2 599 000 | 3 496 000 | 3 811 000 | 4 482 920 | 3 902 642 | 3 879 969 | 3 611 669 | 2 775 436 | 1 659 927 | 566 729 | 0 |
| Cumulative cash, ₽ | -2 599 000 | -5 198 000 | -8 694 000 | -12 505 000 | -16 987 920 | -20 890 562 | -24 770 530 | -28 382 200 | -31 157 636 | -32 817 563 | -33 384 292 | -32 879 686 |

## 2.2 Оптимистичный сценарий: 12-месячный PnL
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 5 | 5 |
| Total clients | 0 | 0 | 1 | 2 | 4 | 5.9 | 8.8 | 11.7 | 15.5 | 19.3 | 24 | 28.6 |
| MRR, ₽ | 0 | 0 | 441 000 | 875 385 | 1 744 254 | 2 600 090 | 3 884 089 | 5 148 828 | 6 835 595 | 8 497 061 | 10 574 605 | 12 620 986 |
| COGS, ₽ | 0 | 0 | 120 000 | 238 200 | 474 627 | 707 508 | 1 056 895 | 1 401 042 | 1 860 026 | 2 312 126 | 2 877 444 | 3 434 282 |
| Gross profit, ₽ | 0 | 0 | 321 000 | 637 185 | 1 269 627 | 1 892 583 | 2 827 194 | 3 747 786 | 4 975 569 | 6 184 936 | 7 697 162 | 9 186 704 |
| GM % | 0.0% | 0.0% | 72.8% | 72.8% | 72.8% | 72.8% | 72.8% | 72.8% | 72.8% | 72.8% | 72.8% | 72.8% |
| Fixed costs, ₽ | 2 599 000 | 2 599 000 | 3 496 000 | 4 107 000 | 5 069 000 | 5 069 000 | 5 615 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 |
| EBITDA, ₽ | -2 599 000 | -2 599 000 | -3 175 000 | -3 469 815 | -3 799 373 | -3 176 417 | -2 787 806 | -2 452 214 | -1 224 431 | -15 064 | 1 497 162 | 2 986 704 |
| Cash burn, ₽ | 2 599 000 | 2 599 000 | 3 175 000 | 3 469 815 | 3 799 373 | 3 176 417 | 2 787 806 | 2 452 214 | 1 224 431 | 15 064 | 0 | 0 |
| Cumulative cash, ₽ | -2 599 000 | -5 198 000 | -8 373 000 | -11 842 815 | -15 642 188 | -18 818 605 | -21 606 411 | -24 058 625 | -25 283 055 | -25 298 120 | -23 800 958 | -20 814 253 |

## 2.3 Пессимистичный сценарий: 12-месячный PnL
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 2 | 2.9 | 4.8 | 6.7 | 9.5 | 12.2 | 14.8 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 399 000 | 786 030 | 1 161 449 | 1 924 606 | 2 664 867 | 3 781 921 | 4 865 464 | 5 916 500 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 130 000 | 256 100 | 378 417 | 627 064 | 868 253 | 1 232 205 | 1 585 239 | 1 927 682 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 269 000 | 529 930 | 783 032 | 1 297 541 | 1 796 615 | 2 549 716 | 3 280 225 | 3 988 818 |
| GM % | 0.0% | 0.0% | 0.0% | 0.0% | 67.4% | 67.4% | 67.4% | 67.4% | 67.4% | 67.4% | 67.4% | 67.4% |
| Fixed costs, ₽ | 2 599 000 | 2 599 000 | 3 496 000 | 4 107 000 | 5 069 000 | 5 069 000 | 5 615 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 | 6 200 000 |
| EBITDA, ₽ | -2 599 000 | -2 599 000 | -3 496 000 | -4 107 000 | -4 800 000 | -4 539 070 | -4 831 968 | -4 902 459 | -4 403 385 | -3 650 284 | -2 919 775 | -2 211 182 |
| Cash burn, ₽ | 2 599 000 | 2 599 000 | 3 496 000 | 4 107 000 | 4 800 000 | 4 539 070 | 4 831 968 | 4 902 459 | 4 403 385 | 3 650 284 | 2 919 775 | 2 211 182 |
| Cumulative cash, ₽ | -2 599 000 | -5 198 000 | -8 694 000 | -12 801 000 | -17 601 000 | -22 140 070 | -26 972 038 | -31 874 497 | -36 277 882 | -39 928 165 | -42 847 940 | -45 059 122 |

## 3. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
Waterfall ниже показан на **M12 run-rate**. Contribution здесь = gross profit после COGS, так как отдельные sales/marketing CAC не входят в ежемесячный PnL, а страховые взносы уже сидят во fixed costs через ФОТ.

| Scenario | ARPA, ₽ | Gross profit / client, ₽ | EBITDA M12, ₽ | Net after tax (УСН 6%), ₽ | Net after tax (IT 3%), ₽ | Net after tax (ОСНО 20% profit tax), ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Базовый | 420 000 | 296 000 | 504 606 | -66 192 | 219 207 | 403 685 |
| Оптимистичный | 441 000 | 321 000 | 2 986 704 | 2 229 445 | 2 608 075 | 2 389 363 |
| Пессимистичный | 399 000 | 269 000 | -2 211 182 | -2 566 172 | -2 388 677 | -2 211 182 |

## 4. Cash flow и startup capital до break-even
| Scenario | startup_capital_to_bep_rub | Min cumulative cash, ₽ | EBITDA break-even month | Break-even clients | Break-even MRR, ₽/мес |
|---|---:|---:|---:|---:|---:|
| Базовый | 33 384 292 | -33 384 292 | M12 | 20.9 | 8 797 297 |
| Оптимистичный | 25 298 120 | -25 298 120 | M11 | 19.3 | 8 517 757 |
| Пессимистичный | 45 059 122 | -45 059 122 | >M12 | 23.0 | 9 196 283 |

## 5. Налоговая модель РФ
- **УСН 6%**: налог считаю как 6% от выручки, обычно лучший режим для non-accredited SaaS без тяжёлого входящего НДС.
- **IT-льгота 3%**: применимо при аккредитации Минцифры и соблюдении условий по IT-выручке. В модели это лучший net outcome.
- **ОСНО 20%**: в PnL считаю 20% налога на прибыль от положительного EBITDA как упрощённый ориентир. **НДС 20%** при ОСНО обычно проходит вне EBITDA как pass-through, если цены выставляются *без НДС*; если продавать *с НДС внутри цены*, фактическая маржа будет хуже.
- **Страховые взносы ~30% к ФОТ** уже включены в fixed costs и FOT из 04-economics.md.

## 6. Вывод по break-even
| Scenario | Break-even client count | Break-even month | Комментарий |
|---|---:|---:|---|
| Базовый | 20.9 | M12 | Выход в плюс к концу горизонта, модель требует дисциплины по найму и удержанию. |
| Оптимистичный | 19.3 | M11 | Плюс достигается быстрее за счёт более раннего набора клиентской базы и IT-льготы. |
| Пессимистичный | 23.0 | >M12 | На горизонте 12 месяцев EBITDA остаётся отрицательной, нужен больший запас капитала. |

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

Допущения для stress-тестов:
- **Base**: как в SECTION A.
- **Sens1 / CAC x2**: канал становится вдвое дороже, поэтому new customers/month снижаю примерно в 2 раза при том же fixed-cost base. Это не бухгалтерский EBITDA-эффект через P&L-строку CAC, а операционный эффект через более слабый набор клиентов.
- **Sens2 / Churn x2**: monthly churn растёт с 2,0% до 4,0%.
- **Sens3 / Price -30%**: ARPA падает с 420k до 294k ₽/мес, COGS на клиента оставляю прежним 124k ₽ как консервативный stress-case. [T5]

| Сценарий | Ключевое изменение | Клиентов к M12 | Gross profit / клиент, ₽/мес | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---:|---|
| Base | без изменений | 22,7 | 296 000 | 504 606 | Модель едва проходит gate к концу года |
| Sens1 | CAC x2 | 11,3 | 296 000 | -2 847 697 | Самый болезненный риск, узкий ICP не прощает удорожание привлечения |
| Sens2 | Churn x2 | 21,4 | 296 000 | 133 733 | Gate почти схлопывается даже без падения цены |
| Sens3 | Price -30% | 22,7 | 170 000 | -2 349 382 | Ценовое давление быстро ломает enterprise-only economics |

**Вывод:** экономика DeepIP-подобного кейса чувствительна прежде всего к **CAC inflation** и **price compression**. Это подтверждает, что moat должен строиться на workflow depth, security и локализации, а не на ценовой конкуренции.

## 2. Monte Carlo Lite: confidence intervals

### 2.1 Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 900 000 | 1 271 111 | 2 100 000 | base CAC из 04-economics + stress до pilot-heavy enterprise motion [T5] |
| Monthly churn, % | 1,1% | 2,0% | 4,0% | ChartMogul benchmark + stress case [T8] |
| ARPU, ₽/мес | 300 000 | 420 000 | 500 000 | price anchors Patent Bots / ClaimMaster / IP.com + premium enterprise fit [T3][T4][T11] |
| Conversion rate lead→paid, % | 0,5% | 1,0% | 1,5% | blended funnel: 1,8 wins на 180 leads ≈ 1,0%, с downside/upside corridor [T5] |
| Time-to-hire, мес (среднее) | 1,0 | 1,7 | 3,0 | hire plan из 04-economics, усреднение по ключевым ролям [T5] |

### 2.2 Методика

Полную 1000-итерационную симуляцию здесь не запускаю. Вместо этого использую **9-комбинационный Monte Carlo Lite**:
- best: CAC_min + churn_min + ARPU_max
- median: CAC_mode + churn_mode + ARPU_mode
- worst: CAC_max + churn_max + ARPU_min
- плюс 6 mixed-комбинаций вокруг mode

Для EBITDA @M24 беру продолжение базового go-to-market после M12: в median-case команда держит около **4 новых клиентов/мес**, в downside ближе к **2**, в upside ближе к **5**. Это согласуется с existing PnL ramp и узким enterprise buyer universe. [T5]

### 2.3 Итоги Monte Carlo Lite

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -900 000 | 11 805 986 | 22 400 000 | 23 300 000 |
| CAC payback, мес | 9,9 | 4,3 | 2,6 | 7,3 |
| LTV/CAC | 2,5x | 11,65x | 20,0x | 17,5 |
| Cash runway, мес | 9 | 16,5 | 22 | 13 |

### 2.4 Интерпретация правил

1. **p10 EBITDA < 0**, значит автоматически срабатывает **kill criterion #1: insolvency risk**.
2. **p50 EBITDA > 500k ₽/мес**, значит median-case EBITDA Gate проходит.
3. Разброс между downside и upside фактически больше 10x по magnitude, значит неопределённость слишком высокая, score надо **даунгрейдить на 1 notch**.
4. **Range width по LTV/CAC = 17,5**, то есть заметно выше порога 8. Модель хрупкая и критично зависит от стабильности pricing, churn и CAC.

## 3. Competitor deep-dive

### 3.1 Top-3 западных конкурента

| Конкурент | Что делает | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Patent Bots | AI-first drafting, prosecution, analyzer, опубликованный pricing | узкий фокус на patent workflow, прозрачный pricing, productized self-serve wedge [T3] | слабее enterprise platform-layer, меньше security / deployment moat для крупных корпораций | ~5-8% в global AI-patent-tools niche | можем выиграть secure private deployment, RU localization и end-to-end workflow для корпораций |
| ClaimMaster | Word-centric patent drafting/review add-in | сильный Word-native UX, узнаваемость у patent practitioners, низкий входной чек [T4] | скорее productivity layer, чем full operating system; слабее copilot for portfolio/prosecution intelligence | ~8-12% в drafting/review niche | можем выиграть глубиной workflow, совместной работой команды и enterprise governance |
| IP.com | search, prior-art, patent intelligence, enterprise IP stack | сильная база данных, search/analytics, многолетний enterprise brand [T11] | менее AI-native в drafting/prosecution UX, сложнее как быстрый copilot-product | ~10-15% в adjacent patent-intelligence software | можем зайти снизу через faster drafting/prosecution copilot и затем расшириться в platform layer |

**Вывод по Западу:** рынок уже валидирован, но fragmented. Для DeepIP-подобного продукта нет смысла конкурировать по низкой цене, только по **workflow depth + enterprise security + локальной адаптации**.

### 3.2 Топ российских конкурентов / substitutes

| Игрок | Источник сигнала | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|---|
| Онлайн Патент | Habr, Rusprofile, Skolkovo [T12][T13][T14] | сильный local brand, цифровой IP lifecycle, синхронизация с реестрами, крупная клиентская база и явный traction | сервисно-операционный уклон, не видно сильного AI-native drafting moat именно под patent copilot | ~20-25% в RU digital IP-management niche | можем выиграть именно AI-first patent drafting/prosecution и ROI на expert-hours, а не только digitization |
| Patentus | vc.ru ranking / market mentions [T15] | сильная юрэкспертиза, long-standing bureau, судебная и регистрационная практика, доверие на сложных кейсах | сервисный бизнес масштабируется медленнее software; меньше product leverage | ~8-12% в premium patent bureau/services | можем дать software margin и throughput uplift для in-house IP teams и бюро |
| Нева-Патент | Rusprofile [T16] | длинная история, устойчивость, репутация в классическом патентном консалтинге | legacy-service model, меньше digital moat, не видно AI-platform layer | ~5-8% в классическом patent services сегменте СПб/федерал | можем выиграть скоростью, workflow automation и централизованной аналитикой |
| Ручной стек: патентные бюро + Excel + Word + general LLM | market substitute, подтверждён в 02-demand и 03-solution [T2][T6] | дешёвый старт, не требует отдельного внедрения | слабая auditability, низкая repeatability, риски confidentiality и quality drift | самый крупный substitute, вероятно >40% рынка workflow | можем дать контролируемый enterprise contour и измеримый cycle-time reduction |

### 3.3 Что это значит для GTM

1. В РФ главный конкурент, это не столько другой AI-native vendor, сколько **service-led incumbent + ручной процесс**.
2. Следовательно, selling point должен быть не «мы тоже патентное бюро, но с AI», а **сокращение часов эксперта и ускорение prosecution/drafting без потери качества**.
3. Для выигрыша нужен wedge в одном дорогом workflow: **drafting**, **office action support** или **prior-art with reusable knowledge layer**.

## 4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|---|
| 1 | Operational | Не удаётся нанять CTO/ML и patent solutions в срок | med | Высокий, сдвиг roadmap и pilot delivery | time-to-hire > 3 мес, offer acceptance < 50% | заранее вести talent bench, contractor bench, founder-heavy старт |
| 2 | Operational | Качество AI-выхода нестабильно на RU patent drafting | med | Высокий, erosion trust у первых клиентов | >15% outputs требуют полного rewrite человеком | evaluation harness, human-in-the-loop QA, narrow templates |
| 3 | Operational | Зависимость от внешних LLM API и OCR/search vendors | high | Высокий, может ударить по SLA и марже | рост latency/cost, изменение rate limits, vendor incidents | multi-model routing, fallback providers, on-prem/open-weight path |
| 4 | Market | Buyer universe в РФ слишком узкий | high | Высокий, ограничение ceiling по ARR | pipeline coverage < 80 target accounts, повторные отказы «нет объёма» | идти в top-200 accounts, СНГ/MEA expansion, adjacent IP workflows |
| 5 | Market | Конкуренты давят ценой, возникает price compression | med | Высокий, ломает EBITDA | скидки >20% становятся нормой, win-rate растёт только при discount | value-based pricing, packaging по workflow/ROI, не продавать как commodity seat |
| 6 | Market | Pilot-to-paid conversion падает | med | Высокий, CAC резко растёт | pilot win-rate < 15%, sales cycle > 9 мес | жёсткий pilot design с KPI, sponsor map, procurement plan до старта |
| 7 | Regulatory | 152-ФЗ / data residency не позволяет использовать иностранный SaaS-контур | high | Высокий, блок на enterprise deals | security/compliance review стопорит сделки >45 дней | RU-hosting, private deployment, DPA и data map заранее |
| 8 | Regulatory | 115-ФЗ / KYC и комплаенс госзаказчиков усложняют onboarding | med | Средний, удлиняет cash cycle | больше запросов по бенефициарам, ИБ, платежам | compliance pack, юрструктура и пакет документов с первого дня |
| 9 | Regulatory | Санкции SaaS / ограничения на зарубежные модели и облака | high | Очень высокий, возможна остановка сервиса | поставщик прекращает доступ, проблемы с оплатой USD | dual-stack architecture, российские и open-weight резервные модели |
| 10 | Financial | Cash runway съедается до достижения repeatable sales | high | Очень высокий | runway < 9 мес, burn > 3,5 млн ₽/мес | raise buffer 40-45 млн ₽, phase hiring, weekly cash review |
| 11 | Financial | Рост курса USD увеличивает COGS и API bill | high | Средний-высокий | USD/RUB > 95, доля долларовых затрат >35% COGS | рублёвый pricing с FX clauses, annual prepay, reserve in FX |
| 12 | Financial | Инфляция ФОТ и налоги повышают fixed cost быстрее revenue | med | Средний | FOT inflation > 15% YoY, новые налоговые требования | slower hiring, variable comp, IT benefits/аккредитация |
| 13 | Black swan | Эскалация войны/санкций режет enterprise budget и сделки | med | Очень высокий | freeze CAPEX, legal review всех зарубежных закупок | focus on ROI cases, public/private sector mix, geo diversification |
| 14 | Black swan | Массовое отключение внешних LLM или резкий policy shift | med | Очень высокий | недоступность API > 24ч, уведомления о termination | локальные модели, кэширование knowledge layer, degrade-mode service |

## 5. Kill conditions через 6 месяцев

1. **p10 EBITDA @M24 остаётся < 0** или текущий cash runway опускается ниже **9 месяцев** без подтверждённого финансирования. Продолжать нельзя, риск неплатёжеспособности слишком высок.
2. **Median-case не подтверждается операционно:** фактический MRR < **2,5 млн ₽**, платящих клиентов < **6**, либо pilot→paid conversion < **15%**. Это означает, что GTM не собирается даже на уровне базовой воронки.
3. **Юнит-экономика ломается:** blended CAC > **2,0 млн ₽**, churn > **4% monthly** или средняя реализованная цена < **300k ₽/мес**. В этом режиме LTV/CAC и EBITDA Gate больше не держатся.

## 6. Общий вывод SECTION B

Кейс остаётся **инвестиционно интересным только как premium enterprise patent-workflow platform**, но после риск-блока его надо вести с пониженным уровнем уверенности. Позитивный median-case существует, однако downside уже показывает отрицательный EBITDA и короткий runway. Значит рекомендованный статус, это **PASS WITH CAUTION / high execution risk**.

## Additional sources for SECTION B
- [T11] IP.com products / platform pages: https://ip.com/products/
- [T12] Онлайн Патент, Habr company profile: https://habr.com/en/companies/onlinepatent/profile/
- [T13] ООО "Онлайн Патент", Rusprofile: https://www.rusprofile.ru/id/10557889
- [T14] Skolkovo о переходе HeadHunter на платформу резидента «Онлайн патент»: https://sk.ru/news/headhunter-pereshel-na-razrabotku-rezidenta-fonda-skolkovo/
- [T15] vc.ru, Patentus в рейтинге патентных бюро: https://vc.ru/legal/2128279-top-12-patentnyh-byuro-moskvy
- [T16] ООО "Нева-Патент", Rusprofile: https://www.rusprofile.ru/id/3959320

<!-- P6B-DONE -->


---

# 06-verdict.md

[GEO-EXPAND] DeepIP Patent AI GEO Expand v2 — REJECTED: 53/100 | EBITDA base=505К₽/мес через 12 мес | LTV/CAC=11,65x | Ключевое преимущество: глубокий patent workflow и enterprise security | Главный риск: рынок РФ слишком узкий и moat слабый.

# 06-verdict

sector: GEO-EXPAND

## Финальный вердикт
**REJECTED**

Несмотря на сильную unit economics на уровне одного клиента, кейс не проходит инвестиционный комитет как standalone GEO-EXPAND модель для РФ. Причина не в валовой марже, а в комбинации из узкого buyer universe, слабого локального demand proof, weak moat и высокого execution/compliance риска. Модель может стать хорошим boutique enterprise-бизнесом, но пока не выглядит как фондовый кейс с достаточным запасом прочности.

## Score summary
- **Raw score:** 80/150
- **Normalized score:** **53/100**
- **Порог:** <65 = REJECTED
- **Дополнительный gate:** EBITDA-потенциал формально проходит, но approve невозможен без investment-grade спроса, moat и repeatable GTM.

## Оценка
Source tier balance: T1=5, T2=9, T3=0, weighted=2.36. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «LTV/CAC: 11,65x», «CAC Payback: 4,3 мес», «Contribution Margin: 70,5%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 16 | В PnL: «EBITDA @M12, ₽/мес = 504 606», но «p10 EBITDA @M24 < 0». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 12 | «Статус спроса: LOW-MODERATE / нишевый», «multi-demand(patent AI) вернул LOW, score 15», penalty за tier balance -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 9 | Есть workflow depth и security story, но «buyer universe в РФ слишком узкий» и локальный regulatory/data moat не доказан. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 12 | В risk matrix есть «152-ФЗ / data residency», «санкции SaaS», «зависимость от внешних LLM API» с high impact. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 13 | 10 целевых аккаунтов есть, но сам кейс требует «top-down продажу», «pilot на 4-8 недель» и sales cycle «6-9 мес». |

**Normalized score = round((80 × 100) / 150) = 53/100.**

## Moat: 7-factor framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных в локальном РФ-контуре. |
| Switching costs | 2 | После внедрения шаблонов, security-политик и workflow-интеграций выйти будет сложнее. |
| Scale economies | 2 | COGS на inference и support частично улучшается с масштабом, но не радикально. |
| Proprietary data / model advantage | 1 | Глобальная продуктовая экспертиза есть, но локальный датасет РФ и явное data-advantage не подтверждены. |
| Regulatory moat | 0 | Регуляторная сложность есть, но лицензируемого или аккредитационного moat пока нет. |
| Brand / distribution | 1 | Глобальный бренд в нише заметен, но локальная дистрибуция в РФ слабая. |
| Embedded workflow | 2 | В случае успеха продукт встраивается в drafting/prosecution/Word-процесс довольно глубоко. |

**Итого 7-factor:** 8/21  
**Moat score = round((8 × 25) / 21) = 10/25**

Вывод: moat на границе weak. Он недостаточно силён, чтобы компенсировать узкий рынок и высокий execution risk.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 14 800 000 ₽ |
| Fully-loaded CAC | 1 271 111 ₽ |
| LTV/CAC | 11,65x |
| CAC payback | 4,3 мес |
| Gross margin | 70,5% |
| contribution_margin_rub_month | 296 000 ₽ |
| fixed_costs_rub_month | 6 200 000 ₽ |
| company_ebitda_rub_month (base, M12) | 504 606 ₽ |
| company_ebitda_potential_rub_month (50 клиентов) | 8 440 000 ₽ |
| Break-even clients | 22 |
| Break-even MRR | 9 240 000 ₽/мес |
| startup_capital_to_bep_rub | 45 000 000 ₽ |
| clients_to_500k_ebitda | 23 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 25 |
| months_to_1m_ebitda | 13-14 |

## Полный бизнес-процесс

| Шаг | Что происходит | Роль | Time | Cost |
|---|---|---|---:|---:|
| 1 | Формирование target-account list по бюро и корпорациям | SDR | 2,0 ч | 2 600 ₽ |
| 2 | Первый outbound touch / warm intro | SDR | 2,5 ч | 3 300 ₽ |
| 3 | Qualification call | SDR + AE | 1,0 ч | 3 700 ₽ |
| 4 | Discovery по patent workflow | AE | 1,5 ч | 5 900 ₽ |
| 5 | Product demo и ROI framing | AE + CEO | 2,0 ч | 9 400 ₽ |
| 6 | Сбор sample matters / office actions | AE + Solutions | 3,0 ч | 11 200 ₽ |
| 7 | Pilot scoping и проектный план | Solutions + CTO | 2,5 ч | 12 800 ₽ |
| 8 | Настройка sandbox / template layer | Solutions + ML + DevOps | 8,0 ч | 31 500 ₽ |
| 9 | Pilot execution и quality review | Solutions + patent analyst | 12,0 ч | 42 000 ₽ |
| 10 | Security / procurement review | CTO + AE | 4,0 ч | 18 500 ₽ |
| 11 | Коммерческое предложение и переговоры | AE + CEO | 2,0 ч | 8 900 ₽ |
| 12 | Contracting / legal review | CEO + external legal | 3,0 ч | 16 000 ₽ |
| 13 | Счёт и закрывающие документы | Finance/Ops | 0,7 ч | 2 300 ₽ |
| 14 | Оплата и go-live | Finance + CSM | 1,5 ч | 5 800 ₽ |

**Итого process cost-to-close:** около **174 600 ₽** до fully-loaded CAC. Узкое место, это pilot, security review и solution setup.

## Команда

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | enterprise sales, ключевые сделки | 780 000 |
| CTO / Tech Lead | архитектура, security, rollout | 845 000 |
| Senior Backend #1 | core platform | 546 000 |
| Senior Backend #2 | integrations / workflow | 546 000 |
| ML Engineer | retrieval, evaluation, quality | 650 000 |
| DevOps | infra / secure deployment | 455 000 |
| Frontend | workflow UI | 390 000 |
| SDR | target accounts, outbound | 234 000 |
| AE | discovery, pilots, close | 390 000 |
| Customer Success | onboarding, retention | 312 000 |
| Patent Solutions / Analyst | pilot delivery, QA | 312 000 |
| **Итого** |  | **5 460 000 ₽/мес** |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Городисский и Партнёры | крупное патентное бюро, много повторяемого drafting/prosecution workload | email managing partner / warm intro через IP-конференцию | 450 000 ₽/мес |
| 2 | Онлайн Патент | уже продают цифровые IP-сервисы, логичен AI-upgrade к текущему стеку | партнёрство / email product lead | 400 000 ₽/мес |
| 3 | PATENTUS | premium patent bureau, где ценны throughput и сокращение часов эксперта | email practice lead | 350 000 ₽/мес |
| 4 | Semenov&Pevzner IP practice | сильная IP-практика, подходит pilot на office-action workflow | warm intro / профильная конференция | 300 000 ₽/мес |
| 5 | Росатом | регулярный invention pipeline и тяжёлый in-house IP-процесс | email head of IP / enterprise security-led sale | 800 000 ₽/мес |
| 6 | Ростех | большой портфель технологий, важны confidentiality и speed-to-filing | email innovation/IP director | 750 000 ₽/мес |
| 7 | Сбер | сильный legal/IP контур и зрелость по enterprise software procurement | email decision-maker / партнёрство через integrator | 700 000 ₽/мес |
| 8 | Яндекс | активная R&D-компания с внутренними patent/intangible asset workflow | founder-led outreach / email legal ops | 650 000 ₽/мес |
| 9 | КАМАЗ | промышленный игрок с инженерными разработками и патентной активностью | cold outreach + промышленная конференция | 500 000 ₽/мес |
| 10 | Татнефть | регулярные технологические заявки и чувствительность к защищённому контуру | партнёрство / email innovation director | 500 000 ₽/мес |

Вывод по GTM: список целевых аккаунтов реалистичен, но это очень узкая top-down воронка. Повторяемость зависит от 20-30 аккаунтов, а не от широкого рынка.

## Top-3 risks

| Риск | Вероятность | Влияние | Почему это критично |
|---|---|---|---|
| Узкий buyer universe в РФ | Высокая | Очень высокое | Даже при хорошем LTV/CAC рынок может не дать достаточно качественных wins для повторяемого scale. |
| Regulatory / data residency / санкции / LLM dependency | Высокая | Очень высокое | 152-ФЗ, private deployment и зависимость от внешних моделей могут ломать сделки и SLA. |
| Pilot-to-paid и price compression | Средняя | Очень высокое | При CAC x2 или price -30% модель уходит в отрицательный EBITDA. |

## Почему кейс отклонён
1. **Спрос в РФ не investment-grade.** В 02-demand прямо указано: «Статус спроса: LOW-MODERATE / нишевый». Для фонда этого мало.
2. **Moat слабый.** Есть product depth, но нет сетевых эффектов, сильного local data advantage или regulatory moat.
3. **Execution risk слишком высокий.** Команда дорогая, локализация тяжёлая, private deployment обязателен, санкционный и LLM risk высокий.
4. **Monte Carlo ломает уверенность.** В 05-critic: «p10 EBITDA @M24 < 0», значит downside слишком хрупкий.

## Что должно быть доказано для upgrade до APPROVED
- 3 реальных LOI или pilot в РФ с ICP уровня enterprise IP / patent bureau.
- Доказанный pilot-to-paid conversion не ниже 20%.
- Private deployment или sovereign-hosting контур без деградации gross margin ниже 65%.
- Реальный локальный proprietary data layer или интеграция в реестры/документооборот, повышающая switching costs.
- Подтверждение, что компания способна получать 500К₽+ company_ebitda_rub_month при 20-25 клиентах без founder-only sales.

## LTV Upside Calculator

Цель: понять, какие рычаги должны измениться, чтобы кейс приблизился к near-pass/approve.

| Рычаг | Текущее значение | Upside-case | Эффект |
|---|---:|---:|---|
| ARPA / MRR на клиента | 420 000 ₽ | 550 000 ₽ | Повышает contribution_margin_rub_month до ~426 000 ₽ при том же COGS 124k. |
| COGS / клиент / мес | 124 000 ₽ | 105 000 ₽ | Gross margin вырастает до ~80,9%, улучшается payback. |
| Monthly churn | 2,0% | 1,5% | customer_ltv_rub растёт с 14,8 млн ₽ до ~19,7 млн ₽. |
| Fully-loaded CAC | 1,27 млн ₽ | 950 000 ₽ | LTV/CAC растёт примерно до 20,7x. |
| Fixed costs / мес | 6,2 млн ₽ | 5,4 млн ₽ | Break-even снижается с 22 до ~14 клиентов в зависимости от ARPA. |
| Pilot-to-paid conversion | ~20% | 30% | Снижает CAC inflation и делает GTM ближе к repeatable. |

**Интерпретация:** даже для перехода к near-pass нужен не один косметический сдвиг, а одновременное улучшение pricing, retention, CAC и локального moat.

## Proof points для инвесткомитета
- Есть глобальные price anchors: Patent Bots, ClaimMaster, IP.com.
- Есть локальный IP workflow и рынок услуг: Роспатент, реестр патентных поверенных, Онлайн Патент.
- Есть рабочая unit economics на уровне premium enterprise-клиента.
- Но нет достаточного локального подтверждения, что эта economics масштабируется в repeatable РФ-бизнес, а не в boutique services.

## Итог инвесткомитета
**REJECTED.**

Кейс можно держать в watchlist как узкую enterprise/IP-ops гипотезу. Возвращаться стоит только если появятся локальные pilot proof, sovereign deployment и evidence, что РФ buyer universe шире 20-30 качественных аккаунтов.
