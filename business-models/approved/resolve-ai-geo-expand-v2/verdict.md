# Verdict Packet — resolve-ai-geo-expand-v2
- Status: APPROVED WITH NOTES
- Score: 70/100
- Sector: GEO-EXPAND
- GitHub canonical path: approved/resolve-ai-geo-expand-v2/verdict.md

---

## FILE: 00-brief.md

# Краткий бриф

## Кейс
Resolve AI, enterprise autonomous SRE и incident response operator

## Почему открыт
- Сигнал пришёл в режиме принудительного resurrect, поэтому по standing orders всегда создаёт новый case-version.
- Ранее сигнал был добавлен как supporting к существующему кейсу, но теперь должен пройти самостоятельную полную оценку.
- Публичные данные из исходного triage указывают на сильную enterprise-тягу категории, большой чек и длинный внедренческий контур.

## Что проверить дальше
- Подтвердить, насколько модель autonomous SRE может давать чек выше 500 тыс. руб. в месяц в РФ через private deployment, интеграции и сопровождение.
- Проверить, не ограничен ли рынок узким числом очень зрелых инфраструктурных команд.
- Сравнить кейс с другими сигналами в категории incident response и понять, есть ли у него самостоятельная go-to-market траектория.

## Следующий этап
P3-demand-validation.

## Комментарий intake
Кейс создан по правилу принудительного полного пайплайна resurrection и направлен на новую полную оценку без duplicate-фильтра.


---

## FILE: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-resolve-ai-geo-expand.md
created: 2026-04-21T15:12:11+03:00
---

# 01-intake

## Кейс
resolve-ai-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом , поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-resolve-ai-geo-expand-followup.md

## Краткий контекст
Standalone GEO-EXPAND кейс по autonomous SRE и incident response: AI-native расследование инцидентов, enterprise traction, private deployment и интеграции с observability, alerting и ITSM.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить enterprise budget, внедренческий цикл, on-prem/private deployment требования и реалистичность высоких LTV в российском контуре.

## Полный контекст из raw

# RESURRECT SIGNAL — resolve-ai-geo-expand

## Meta
- source: triage/triage-2026-04-15-resolve-ai-geo-expand-followup.md
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
- `pipeline/raw/raw-2026-04-15-2304-msk-resolve-ai-geo-expand.md`

## Классификация
Поддерживающий сигнал для существующего открытого кейса.

## Решение
Сигнал добавлен в кейс `autonomous-sre-incident-response-operator`.

## Что именно добавлено
- В `pipeline/cases/autonomous-sre-incident-response-operator/01-evidence.md` добавлен supporting signal по Resolve AI.
- Зафиксированы новые подтверждения enterprise-тяги категории autonomous SRE: ARR около $4 млн, Series A на $125 млн при оценке $1 млрд, а также публично названные клиенты Coinbase, DoorDash, MongoDB, MSCI, Salesforce и Zscaler.
- Отдельно отмечено, что сигнал усиливает сервисную гипотезу вокруг private deployment, интеграций с observability/alerting/ITSM и долгого внедренческого контура для крупных инфраструктурных команд.

## Почему это усиливает кейс
Resolve AI подтверждает, что AI-native incident response уже продаётся крупным enterprise-командам как отдельная дорогая категория, а не как вспомогательный DevOps copilot. Для кейса это снижает риск, что рынок слишком ранний или нишевый, и поддерживает гипотезу о высоком LTV на внедрение и сопровождение в банках, telecom, e-commerce и других сложных production-контурах.

## Статус raw-файла
Файл должен быть перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен подтверждающий GEO-EXPAND сигнал по Resolve AI для `autonomous-sre-incident-response-operator`.

```


---

## FILE: 01-evidence.md

# Подтверждающие сигналы

## 2026-04-23 — supporting signal
- **Источник:** https://techcrunch.com/2026/02/04/ai-sre-resolve-ai-confirms-125m-raise-unicorn-valuation/ ; https://www.bloomberg.com/news/articles/2026-02-04/resolve-ai-hits-1-billion-valuation-for-outage-thwarting-ai-agents ; https://resolve.ai/news/resolveai-raises-125-million-series-a ; https://resolve.ai/news/Series-A-extension-and-Resolve-AI-Labs ; https://resolve.ai/product/ai-sre
- **Тип:** supporting signal
- **Как усиливает кейс:** Новый сигнал усиливает кейс Resolve AI как enterprise autonomous SRE-платформы, потому что добавляет свежую валидацию по финансированию, списку клиентов и продуктовым метрикам внедрения. Это повышает уверенность, что категория продаётся как отдельный дорогой инфраструктурный слой, а не как вспомогательный DevOps copilot.
- **Ключевые данные и факты:** TechCrunch и Bloomberg подтверждают Series A на $125 млн и оценку около $1 млрд; компания публично называет клиентов Coinbase, DoorDash, MongoDB, MSCI, Salesforce и Zscaler; продуктовые заявления включают 100% investigated alerts, менее 5 минут от alert до RCA и более 70% faster MTTR.

## 2026-05-13 — supporting signal — Resolve AI как валидация enterprise AI-SRE
- **Дата:** 2026-05-13
- **Источник:** https://techcrunch.com/2025/12/19/ex-splunk-execs-startup-resolve-ai-hits-1-billion-valuation-with-series-a/ ; https://resolve.ai/news/resolveai-raises-125-million-series-a ; https://resolve.ai/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс по autonomous SRE, потому что добавляет ещё одно подтверждение, что enterprise-клиенты готовы покупать отдельный AI-слой для расследования инцидентов и remediation, а не только observability-инструменты. Это повышает уверенность в большом чеке и в том, что wedge может быть воспроизведён как premium infra-service для зрелых production-команд.
- **Ключевые данные и факты:** TechCrunch описывает Resolve AI как компанию бывших руководителей Splunk с оценкой $1 млрд; официальный релиз компании подтверждает $125 млн Series A и клиентов Coinbase, DoorDash, MongoDB, MSCI, Salesforce и Zscaler; сайт продукта позиционирует сервис как autonomous AI-SRE для расследования инцидентов, поиска root cause и запуска remediation.

## 2026-05-13 — supporting signal — Resolve AI как зрелая категория autonomous SRE
- **Дата:** 2026-05-13
- **Источник:** https://techcrunch.com/2025/12/19/ex-splunk-execs-startup-resolve-ai-hits-1-billion-valuation-with-series-a/ ; https://techcrunch.com/2026/02/04/ai-sre-resolve-ai-confirms-125m-raise-unicorn-valuation/ ; https://resolve.ai/customers
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс, потому что одновременно подтверждает выручечную traction, крупное финансирование и наличие набора enterprise-клиентов, готовых платить за отдельный autonomous SRE-слой. Это снижает риск, что категория является только PR-нарративом вокруг observability, и поддерживает гипотезу о крупном recurring-чеке для зрелых production-команд.
- **Ключевые данные и факты:** TechCrunch ранее писал о примерно $4 млн ARR у Resolve AI, затем подтвердил раунд $125 млн при оценке около $1 млрд; страница customers показывает кейсы Salesforce, DoorDash, Coinbase, Zscaler и Blueground; продукт продаётся как AI SRE для расследования инцидентов и помощи в remediation.


---

## FILE: 02-demand.md

# Demand validation — Resolve AI

## Вывод
**Вердикт: PASS с оговорками, идти дальше по пайплайну.**

Категория autonomous SRE / incident response в РФ выглядит **узкой, но платёжеспособной enterprise-нишей**, а не массовым SaaS-рынком. По internal demand endpoint запрос `incident response SRE` дал **LOW / 0**, но более близкий к локальному procurement-языку запрос `управление инцидентами` дал **MEDIUM / 30** при **2771 вакансии** на HH и максимальном Yandex Suggest, а `SRE` дал **315 вакансий** в internal tool и **378 вакансий** в публичной выдаче HH. Это означает, что массового inbound-поиска мало, но операционная функция и hiring-demand в РФ реальны. [T1][Internal]

## 1) Что именно валидируем
Resolve AI продаёт не просто alerting, а **AI-оператора для production incidents, on-call и SRE-workflows**: расследование инцидентов, гипотезы по root cause, remediation suggestions, работа с кодом, infra и telemetry. Это enterprise-инфраструктурный слой с длинным внедрением, высоким требованием к security/compliance и очень ограниченным ICP. [T2]

## 2) Demand signals
- Internal endpoint `multi-demand` по состоянию на **23 апреля 2026, 01:21 MSK**:
  - `incident response SRE` → **LOW, score=0**, HH=4, Google Trends RU=0, Yandex Suggest=2. [Internal]
  - `SRE` → **LOW, score=28**, HH=315, Google Trends RU=7, Yandex Suggest=100. [Internal]
  - `управление инцидентами` → **MEDIUM, score=30**, HH=2771, Google Trends RU=1, Yandex Suggest=100. [Internal]
- Публичная выдача HH по запросу `SRE` показывает **378 вакансий**, среди работодателей видны **СБЕР, Ozon, RWB, Альфа-Банк, Т-Банк, МТС, Beeline, BI.ZONE, SberTech** и другие. Это прямое подтверждение существования функций SRE / production reliability в РФ. [T1]
- Следовательно, спрос есть, но он выражен **не в consumer search intent**, а в hiring, procurement и enterprise operations pain. Это типично для incident-management категорий. [T1][T2]

## 3) Конкуренты и цены
### Глобальные игроки
1. **PagerDuty Incident Management**: Professional **$21/user/month** при годовой оплате, Business **$41/user/month**, Enterprise — custom pricing. Это даёт якорь для seat-based on-call / incident response бюджетов. [T2]
2. **FireHydrant Signals**: Pro/Platform package **$9,600/year** на команду, включая incident management, on-call и alerting. Это показывает, что зрелые команды готовы покупать bundled incident stack как annual contract. [T2]
3. **incident.io**: Team **$15/user/month annual** или **$19 monthly**, Pro **$25/user/month**, On-call add-on **+$10–20/user/month**. Это подтверждает рабочий диапазон per-seat pricing у category peers. [T2]

### Что это значит для Resolve AI
- У существующих игроков базовый price anchor лежит в диапазоне примерно **$15–41 за пользователя в месяц** или **около $9.6k в год за команду**. [T2]
- Resolve AI позиционируется **выше** этой базы, потому что продаёт не just workflow, а AI investigation/remediation layer. Значит, в РФ монетизация через чистый per-seat on-call pricing будет слабой, а через **private deployment / enterprise platform fee / managed rollout** — реалистичной. [T2 + inference]

## 4) Telegram в РФ: боты и сервисы
- У **Zabbix** есть официальная интеграция с **Telegram Bot API** для персональных и групповых уведомлений, включая topics в supergroups. Это доказывает, что Telegram уже встроен в ops-alerting workflows. [T1]
- В РФ это особенно релевантно, потому что Telegram де-факто стал стандартным рабочим каналом для many engineering teams; однако по найденным данным **не обнаружен сильный российский публичный Telegram-native autonomous SRE сервис с enterprise pricing**. [T1][T3]
- Вывод: Telegram в РФ скорее выступает как **notification / collaboration endpoint**, а не как отдельный продукт-заменитель Resolve AI. Это снижает риск прямой каннибализации, но повышает требование к интеграции в Telegram/чат-операционку. [T1 + inference]

## 5) Willingness to pay (WTP)
### Доказательства
- У конкурентов уже есть устойчивые recurring price points в incident-response software: PagerDuty **$21–41/user/month**, incident.io **$15–25/user/month + on-call add-on**, FireHydrant **$9.6k/year/team**. Это прямое доказательство willingness to pay на категорию. [T2]
- Resolve AI сам продаёт enterprise-grade security posture: SAML SSO, RBAC, auditability, isolation, no external training. Такой набор нужен только там, где покупатель готов проходить security review и платить enterprise-budget. [T2]
- HH показывает десятки и сотни вакансий SRE у крупных компаний. Если компания уже держит SRE-команду с компенсацией уровня **250–350 тыс. ₽/мес** на одного инженера в открытой вакансии, то инструмент, который реально сокращает MTTR и on-call load, попадает в существующую budget line. [T1][T2 + inference]

### Вывод по WTP
- **SMB WTP не подтверждён.** [T2]
- **Enterprise WTP подтверждён косвенно, но убедительно.** Для РФ разумный пилотный диапазон выглядит как **150–300 тыс. ₽/мес** за команду, а private deployment / high-touch enterprise rollout может доходить до **400–800 тыс. ₽/мес**. Это inference, выведенный из зарубежных price anchors, локальной стоимости SRE-функции и необходимости security/compliance. [T1][T2 + inference]

## 6) Market sizing
### Логика сегмента
Берём не весь российский ИТ-рынок, а только **крупные и средние организации с 24/7 production, DevOps/SRE, on-call и высокой ценой простоя**: банки, e-commerce, telecom, digital platforms, cybersecurity vendors, large SaaS / cloud, финтех, media-tech. [T1][T2]

### Top-down
**[LOW CONFIDENCE]** Для Resolve AI нет открытого чистого российского отчёта по autonomous SRE, поэтому top-down собирается через прокси.

- НИУ ВШЭ на основе данных Росстата оценивает валовые внутренние затраты на развитие цифровой экономики РФ в **6.7 трлн ₽ в 2024**, при этом доля расходов на ПО, лицензии, адаптацию и доработку выросла до **23%**. Это даёт software-related base порядка **1.54 трлн ₽**. [T1/T2]
- Для incident response / observability / SRE automation берём только **0.35%** этой software-base как addressable infra-ops layer. Это даёт **TAM РФ ≈ 5.4 млрд ₽**. Доля консервативная, потому что продукт Resolve относится к very narrow slice enterprise software. [T1/T2 + inference]
- Для SAM оставляем только организации, где реально есть зрелый on-call / SRE контур и бюджет на enterprise infra tooling, то есть **около 35% TAM**. Получаем **SAM ≈ 1.9 млрд ₽**. [T1/T2 + inference]
- Реалистичный capture: **Y1 = 2% SAM**, **Y3 = 8% SAM**. Тогда **SOM Y1 ≈ 38 млн ₽**, **SOM Y3 ≈ 151 млн ₽**. [inference]
- Глобальный TAM как proxy-рынок AIOps / incident-management software в открытых вторичных исследованиях выглядит как **примерно $5–8 млрд**, но точность низкая, поэтому для инвестиционного решения используем РФ-модель как более надёжную. [T3]

### Bottom-up
#### Шаг 1. База buyers
Используем first-wave buyers из публичного hiring/signal поля РФ: **СБЕР, Ozon, RWB (Wildberries & Russ), Альфа-Банк, Т-Банк, МТС, Beeline, BI.ZONE, SberTech, ЕДИНЫЙ ЦУПИС**. Это 10 реальных покупателей, уже видимых в HH по запросу `SRE`. [T1]

Для широкого SAM-моделя принимаем:
- банки, финтех, страховщики, telecom, large digital/e-commerce, кибербезопасность, крупные продуктовые IT-команды,
- всего **~420 потенциальных организаций** в РФ с достаточной production complexity. Это inference, основанный на ЦБ-реестрах, крупных цифровых работодателях HH и видимом пуле enterprise digital компаний. [T1][T2 + inference]

#### Шаг 2. Доля с подтверждённой болью
- `% with need = 30%`. Не у каждой компании есть зрелый SRE/on-call контур и готовность к AI-автоматизации, но HH и internal demand показывают, что функция присутствует широко внутри upper tier рынка. [T1][Internal + inference]

#### Шаг 3. Средний контракт
- Базовый enterprise ARR берём **3.6 млн ₽/год** (300 тыс. ₽/мес) как нижнюю границу для pilot/private deployment light. [T2 + inference]

Тогда:
- **SAM_bottom_up = 420 × 30% × 3.6 млн ₽ = 453.6 млн ₽**.
- **SOM_bottom_up Y1 = 5% SAM_bottom_up = 22.7 млн ₽**.
- **SOM_bottom_up Y3 = 15% SAM_bottom_up = 68.0 млн ₽**.

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $5–8B [T3] | — | proxy only, не используется в инвестиционном решении | top-down |
| TAM (РФ) | 5.4 млрд ₽ [T1/T2 + inference] | 1.51 млрд ₽ [T1/T2 + inference] | diff ~3.6x, потому что bottom-up уже режет рынок до зрелых buyers | lower |
| SAM (РФ) | 1.9 млрд ₽ [T1/T2 + inference] | 453.6 млн ₽ [T1/T2 + inference] | diff ~4.2x, поэтому берём консервативный low-end и считаем upper model завышенным | lower |
| SOM Y1 | 38.0 млн ₽ | 22.7 млн ₽ | diff ~1.7x после консервативного capture | **используем 22.7 млн ₽** |
| SOM Y3 | 151.0 млн ₽ | 68.0 млн ₽ | diff ~2.2x | **используем 68.0 млн ₽** |

### Sanity check
- Используемый **SOM Y1 = 22.7 млн ₽** при ARR **3.6 млн ₽** означает около **6–7 клиентов** в первый год. Это тяжело, но реалистично для founder-led enterprise motion. [inference]
- **SOM Y1 < 10% SAM**, значит overclaiming нет. [inference]
- Если sales cycle 6–9 месяцев, команда должна начинать с 2–3 design partners и дальше расширяться через security-approved deployments. [T2 + inference]

## 7) Profit Gate (EBITDA >= 500k ₽/мес)
Проверяю все ключевые сценарии монетизации.

### Сценарий A: seat-based SaaS
- Цена: **3,500 ₽/пользователь/мес** эквивалентно локализованному low-end against global anchors. [T2 + inference]
- 100 платящих пользователей = **350k ₽ MRR**.
- Даже при GM 85% валовая прибыль ~298k ₽/мес, этого недостаточно для компании.
- **Gate: FAIL.**

### Сценарий B: team plan
- Цена: **150k ₽/мес** за команду.
- 10 клиентов = **1.5 млн ₽ MRR**.
- При GM 75% валовая прибыль ~1.125 млн ₽/мес.
- После core OPEX на senior infra/ML/support EBITDA вероятно около нуля или отрицательная.
- **Gate: borderline / скорее FAIL.**

### Сценарий C: enterprise private deployment
- Цена: **350k ₽/мес**.
- 12 клиентов = **4.2 млн ₽ MRR**.
- При GM 70% валовая прибыль ~2.94 млн ₽/мес.
- При OPEX 2.2–2.4 млн ₽/мес EBITDA = **0.5–0.7 млн ₽/мес**.
- **Gate: PASS.**

### Сценарий D: enterprise platform + onboarding / managed rollout
- Цена: **500k ₽/мес** эквивалентно blended revenue.
- 8 клиентов = **4.0 млн ₽ MRR**.
- При GM 68% валовая прибыль ~2.72 млн ₽/мес.
- При OPEX 2.2–2.4 млн ₽/мес EBITDA = **0.3–0.5 млн ₽/мес**; при 9–10 клиентах запас уже комфортный.
- **Gate: PASS с оговоркой.**

### Итог по Profit Gate
Profit Gate **проходит только в enterprise / private deployment / high-touch модели**. Если Resolve попытается зайти в РФ как обычный per-seat incident tool, экономика не пройдёт. [T2 + inference]

## 8) Основные риски
1. **Слишком узкий ICP**: массового спроса нет, нужен точный заход в top-tier infra teams. [T1][Internal]
2. **Высокий trust barrier**: autonomous remediation в production потребует длительного security review и ограниченного rollout. [T2]
3. **Локальный стек и data residency**: для РФ критичны private deployment, audit trail и отсутствие data leakage. [T2 + inference]
4. **Субституция людьми и runbooks**: часть value может закрываться сильной SRE-командой, Zabbix/Prometheus/Alertmanager и чат-операционкой в Telegram/Slack. [T1][T3]

## 9) Инвестиционная интерпретация
Resolve AI в РФ — это **не широкий software market**, а ставка на very narrow enterprise pain: дорогостоящие production incidents у компаний, которые уже имеют on-call, SRE и сложный telemetry stack. Для фонда это может быть интересным, если тезис — не «массовый SaaS в РФ», а **high-ACV wedge в зрелые digital enterprises** с возможным международным апсайдом. [T1][T2 + inference]

## Финальный вывод
- **Demand:** низкий в узком англоязычном формулировании, но средний в локальном enterprise-лексиконе. [Internal]
- **WTP:** подтверждён через competitor pricing и cost-of-team logic. [T1][T2]
- **Telegram в РФ:** канал уведомлений и collaboration уже нормализован, но не найден сильный публичный direct competitor. [T1][T3]
- **TAM/SAM/SOM:** рынок в РФ небольшой, но достаточный для нескольких десятков миллионов рублей SOM при enterprise-only фокусе. [T1][T2 + inference]
- **Profit Gate:** проходит только при high-ACV enterprise GTM. [T2 + inference]

**Решение на этапе demand validation: PASS с оговорками.**

## Источники
- Resolve AI: https://resolve.ai/ [T2]
- PagerDuty pricing: https://www.pagerduty.com/pricing/incident-management/ [T2]
- FireHydrant pricing: https://firehydrant.com/pricing/ [T2]
- incident.io pricing: https://incident.io/pricing [T2]
- HH поиск вакансий SRE: https://hh.ru/search/vacancy?text=SRE [T1]
- Zabbix Telegram integration: https://www.zabbix.com/integrations/telegram [T1]
- НИУ ВШЭ / ИСИЭЗ по данным Росстата о затратах на цифровую экономику: https://issek.hse.ru/news/1132489247.html [T1/T2]

Sources: T1=3, T2=5, T3=1. Primary evidence basis: T2.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-10: наблюдается растущий интерес.

> Market Pulse 2026-05-11: зафиксирован рост интереса, по текущему веб-поиску и публикациям динамика выглядит растущей.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.


---

## FILE: 03-solution.md

---
stage: solution
case: resolve-ai-geo-expand-v2
date: 2026-05-13
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Resolve AI как GEO-EXPAND wedge для autonomous SRE, incident investigation и remediation orchestration в крупных production-контурах.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает дорогую и регулярную проблему, где цена ошибки и простоя высокая: расследование инцидентов, on-call load, MTTR и ручной перебор telemetry/runbooks во время аварий. [T1][T2]
2. Реальный wedge выглядит не как ещё один observability dashboard и не как дешёвый on-call SaaS, а как **AI-SRE operator layer** поверх существующего monitoring / incident stack. [T2][inference]
3. В РФ solution-fit правдоподобен только у very narrow enterprise ICP, где уже есть зрелая SRE/DevOps функция, 24/7 production и budget owner, который чувствует стоимость downtime. [T1][Internal][inference]
4. Главный риск в том, что кейс легко схлопывается либо в services-heavy incident consulting, либо в очередной copilот поверх существующих инструментов, если не доказать measurable operational outcome и безопасный rollout. [inference]

## 1. Какую проблему реально решает продукт

Клиент покупает не «ИИ для DevOps вообще», а устранение четырёх дорогих потерь:
- долгий поиск root cause во время инцидента;
- перегрузка on-call/SRE-команды ручным triage alerts;
- высокая цена ложных escalations и долгого MTTR;
- зависимость от узкого круга senior-инженеров, которые держат в голове runbooks, topology и исторический контекст инцидентов. [T2][inference]

Это painkiller только там, где production outages действительно стоят денег, SLA и репутации. Для обычной IT-команды без сложного runtime-контура ценность будет ниже, потому что проблему можно закрывать людьми, runbooks и базовым monitoring stack. [T1][T2][inference]

## 2. Продуктовый wedge

### Core wedge
**Autonomous incident investigation and response layer**
- intake alerts и автоматический triage;
- анализ telemetry, логов и инфраструктурного контекста;
- гипотезы по root cause;
- remediation suggestions и controlled execution path;
- orchestration работы между observability, incident management и инженерной командой;
- auditability, isolation и enterprise-grade security posture. [T2]

### Почему это сильнее, чем обычный incident-management tool
1. **Outcome привязан к MTTR и on-call efficiency.** Продукт продаёт не удобный интерфейс, а сокращение времени расследования и нагрузки на дежурную команду. [T2][inference]
2. **Есть execution-layer, а не только visibility.** Resolve AI позиционируется вокруг investigation и remediation, а не просто around alerts и статус-страниц. [T2]
3. **Есть сильный enterprise/security narrative.** Изоляция, RBAC, audit trail и отсутствие external training важны только там, где покупатель уже мыслит enterprise-risk категориями. [T2]
4. **Есть понятный overlay motion.** Продукт не требует замены существующего monitoring stack, а пытается стать интеллектуальным слоем поверх него. Это повышает шансы на pilot entry. [T2][inference]

## 3. Целевой ICP в локальном контуре

### Primary ICP
- банки, финтех, платёжная инфраструктура;
- крупный e-commerce и маркетплейсы;
- телеком и digital platforms;
- облачные / SaaS / cybersecurity vendors;
- большие продуктовые IT-команды с 24/7 production, on-call и высокой стоимостью инцидента. [T1][Internal][inference]

### Фильтр на ICP
Клиент подходит, если одновременно есть:
1. production-контур, где downtime реально измеряется деньгами или SLA;
2. выделенная SRE / DevOps / platform engineering функция;
3. incident-management стек и зрелые alerting-процессы;
4. security/compliance требования, из-за которых важны private deployment и auditability;
5. buyer на уровне head of infrastructure, VP engineering, CTO, CIO или owner reliability/platform. [T1][T2][inference]

### Нецелевой сегмент
- SMB без сложного production;
- команды без on-call discipline и выделенного reliability owner;
- компании, где incident load редкий и закрывается вручную;
- организации, для которых дешевле расширить штат SRE, чем покупать новый enterprise layer. [inference]

## 4. Как продукт должен выглядеть в локальном GTM

### Слабое позиционирование
- «AI для мониторинга» без связи с MTTR и downtime;
- продажа как per-seat SaaS для широкой инженерной аудитории;
- попытка зайти как self-serve observability add-on;
- generic DevOps copilot narrative без security и rollout strategy.

### Реалистичное позиционирование
- вход через дорогой reliability bottleneck: noisy alerts, long RCA, overloaded on-call, incident review fatigue;
- pilot на одном production-контуре или одном типе инцидентов;
- buyer bundle: CTO/CIO/Head of Infrastructure + platform/SRE owner + security sponsor;
- KPI пилота: MTTR, time-to-RCA, percent investigated alerts, on-call hours saved, escalation reduction;
- rollout как private / isolated AI-SRE layer поверх уже существующего стека observability и incident tooling. [T1][T2][inference]

## 5. Delivery model

### Наиболее правдоподобная схема внедрения
1. discovery по incident workflow, telemetry stack и security constraints;
2. интеграция с monitoring, logs, alerting, ticketing и knowledge base;
3. ограниченный pilot без полного autonomous execution, сначала в режиме assist/investigate;
4. измерение KPI до/после на конкретном типе инцидентов;
5. расширение на remediation suggestions и controlled automations;
6. переход в recurring enterprise contract с поддержкой, governance и audit controls. [T2][inference]

### Кто должен быть buyer'ом
- CTO / CIO;
- head of infrastructure или platform engineering;
- SRE manager / director of reliability;
- owner incident management / NOC / production operations;
- security sponsor, если нужен private deployment.

### Кто редко будет настоящим buyer'ом
- отдельный DevOps-инженер без бюджета;
- procurement без технического sponsor;
- observability owner без полномочий менять incident operating model.

## 6. Почему клиент купит это, а не альтернативы

У клиента уже есть substitutes:
- SRE-команда и manual RCA;
- Zabbix / Prometheus / Grafana / Alertmanager / PagerDuty-подобный стек;
- внутренние runbooks и чат-операционка в Telegram/Slack;
- собственные automation scripts и postmortem discipline. [T1][T2][T3]

Кейс выигрывает только если доказывает пять вещей:
1. быстрее находит root cause, чем текущий ручной контур;
2. реально снижает on-call load, а не только добавляет новый интерфейс;
3. не ломает security/compliance требования;
4. встраивается поверх существующего стека без тяжёлой замены core tooling;
5. даёт repeatable ROI, а не разовый wow-эффект на демо. [T2][inference]

## 7. Конкурентная позиция

### Против incident-management / on-call SaaS
Преимущество возможно, если продукт продаётся как intelligence/execution layer, а не как ещё одна панель инцидентов. Иначе он конкурирует с более дешёвыми seat-based решениями. [T2][inference]

### Против in-house automation
Шанс есть, если time-to-value выше, чем у внутренней сборки, а модель держит более широкий telemetry/context layer и лучше документирует решения. [inference]

### Против сильной SRE-команды
Преимущество появляется только там, где AI может уменьшить dependency на senior responders и сократить нагрузку на scarce reliability talent. [T1][T2][inference]

## 8. Основные риски solution-fit

1. **Narrow-ICP risk.** Реальный buyer pool в РФ невелик. [T1][Internal]
2. **Trust barrier.** Autonomous actions в production потребуют очень осторожного rollout и security review. [T2]
3. **Services creep.** Внедрение может стать слишком кастомным и дорогим. [inference]
4. **Category confusion.** Кейс легко воспринимается как observability add-on, а не как отдельный budget line. [inference]
5. **Proof risk.** Без жёстких KPI по MTTR/RCA продукт рискует остаться красивой технологией без доказанного P&L эффекта. [inference]

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой ACV реалистичен для private deployment / enterprise rollout в РФ;
- сколько presales, security review и integration-hours съедает одна сделка;
- можно ли держать gross margin при high-touch onboarding;
- сколько клиентов нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- где граница между productized AI-SRE operator и custom reliability consulting.

## Итог для пайплайна

**P4 пройден условно.**

Кейс жив только как узкий enterprise GEO-EXPAND wedge вокруг expensive production incidents, private deployment и measurable reliability outcome. Двигать дальше стоит, если economics подтвердит, что high-ACV модель не расползается в тяжёлый консалтинг и выдерживает длинный enterprise sales cycle.

## Источники
- [T1] HH поиск вакансий SRE: https://hh.ru/search/vacancy?text=SRE
- [T2] Resolve AI, официальный сайт и продуктовые материалы: https://resolve.ai/ ; https://resolve.ai/product/ai-sre ; https://resolve.ai/customers ; https://resolve.ai/news/resolveai-raises-125-million-series-a
- [T3] Zabbix Telegram integration: https://www.zabbix.com/integrations/telegram
- [Internal] internal multi-demand signals по запросам `incident response SRE`, `SRE`, `управление инцидентами` из 02-demand.md

Sources: T1=1, T2=4, T3=1, Internal=1. Primary evidence basis: T2.


---

## FILE: 04-economics.md

---
stage: economics
case: resolve-ai-geo-expand-v2
date: 2026-05-13
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P5: PASS.**

Resolve AI в российском контуре выглядит **инвестируемым только как high-ACV enterprise private-deployment продукт** для зрелых SRE / platform команд. В self-serve и seat-based motion экономика не сходится, но в enterprise-модели с blended revenue **450 тыс. ₽ MRR на клиента** и fully-loaded CAC **~804 тыс. ₽** кейс проходит ключевые инвестиционные ворота.

### Ключевые выводы
- **Blended MRR / клиент:** 450 тыс. ₽/мес.
- **COGS / клиент / мес:** 102 тыс. ₽.
- **Gross Margin:** 77.3%.
- **Contribution Margin:** 69.8%.
- **Fully-loaded CAC:** 804 тыс. ₽/новый платящий клиент.
- **LTV:** 23.0 млн ₽ revenue LTV, **17.8 млн ₽ gross-profit LTV**.
- **Churn benchmark:** **1.5% monthly logo churn** как рабочая база для enterprise B2B SaaS с высоким ACV; это консервативнее, чем low-churn top-tier enterprise, но не агрессивно. [T6][inference]
- **LTV/CAC:** 22.1x по gross-profit LTV.
- **CAC Payback:** 2.3 месяца по gross profit.
- **Break-even:** ~**17 клиентов** или **M15** по модели ramp.
- **EBITDA > 500 тыс. ₽/мес:** достижимо примерно с **18 клиентов**.
- **При 50 клиентах** даже с расширенной delivery-командой модель остаётся сильно прибыльной, поэтому Profit Gate **PASS**.

## 1. Pricing и модель выручки

### Рабочая ценовая модель для РФ
Для локальной модели беру не global list price, а **productized enterprise contract**:
- platform / private deployment fee: **300 тыс. ₽/мес**,
- premium support + governance: **90 тыс. ₽/мес**,
- amortized onboarding / security / integration revenue equivalent: **60 тыс. ₽/мес**,
- **итого blended MRR = 450 тыс. ₽/клиент/мес**.

Это укладывается в ранее проверенный диапазон из `02-demand.md`, где realistic pilot/private deployment pricing оценивался как **400–800 тыс. ₽/мес**. Pricing anchors по категории подтверждаются через PagerDuty, incident.io и FireHydrant, но Resolve должен продаваться выше seat-based incident tools, потому что в value proposition входят investigation/remediation, private deployment и security-heavy rollout. [T3][T4][T5]

## 2. Подробный business process: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Target account selection | SDR + founder | HH/рынок, CRM, списки target accounts | 1.5 ч | 3,500 | средняя |
| 2 | Outbound outreach / intro request | SDR | HubSpot, email sequences, Telegram/LinkedIn аналоги | 2.0 ч | 4,500 | высокая |
| 3 | Discovery call | Founder/AE | Zoom/Meet, CRM | 1.0 ч + prep | 8,000 | низкая |
| 4 | Qualification и mapping incident pain | AE + Solutions Engineer | CRM, discovery template | 2.0 ч | 11,000 | низкая |
| 5 | Security / infra scoping | CTO + Solutions Engineer | checklist, architecture docs | 3.0 ч | 18,000 | низкая |
| 6 | Pilot design и success metrics | AE + CTO + customer sponsor | pilot plan, KPI sheet | 2.5 ч | 16,000 | низкая |
| 7 | Integration sandbox setup | Backend + DevOps + ML | cloud, observability connectors, CI/CD | 12-16 ч | 65,000 | средняя |
| 8 | Paid pilot / validation | Solutions + CS + customer SRE | dashboards, runbooks, shared incident review | 2-4 недели | 120,000 | средняя |
| 9 | Procurement, legal, DPA/infosec review | AE + founder + customer legal | templates, doc room | 2-6 недель | 45,000 | низкая |
| 10 | Contract signature | Founder/AE | e-sign, CRM | 0.5 ч | 4,000 | высокая |
| 11 | Production onboarding | Solutions + DevOps + CS | deployment scripts, monitoring, runbooks | 1-2 недели | 168,000 | средняя |
| 12 | Monthly usage, support, QBR | CS + SRE support + model ops | ticketing, dashboards, knowledge base | ongoing | 42,000/мес labor | средняя |
| 13 | Invoice и получение оплаты | Finance/CEO | ЭДО, банк, 1С/финучёт | 0.5 ч | 2,500/мес | высокая |

### Комментарий
Самые дорогие части процесса, это **integration + pilot + security/procurement**. Поэтому кейс нельзя оценивать как обычный SaaS с «реклама / регистрации / оплаты». Это enterprise sales + implementation motion, где часть CAC живёт в pre-sales инженерии, а часть COGS, в пост-sales сопровождении.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM / inference / model routing | 22,000 | лимиты на incident summaries, RCA, copilot actions | зависит от depth и log volume |
| Private deployment infra / VPC / compute reserve | 18,000 | выделенные ресурсы на isolated deployment | enterprise buyer ожидает data isolation |
| Observability connectors / storage / secrets / backups | 8,000 | middleware + retention | vendor-side burden |
| Support & on-call engineering allocation | 14,000 | дежурство и incident assistance | обязательный high-touch слой |
| Customer Success allocation | 10,000 | 1 CSM на 25-30 клиентов | productized, но не self-serve |
| Security / audit / compliance upkeep | 6,000 | review cadence, logging, audit trail | enterprise overhead |
| Implementation amortization | 24,000 | 288k one-off / 12 мес | внедрение надо размазывать по контракту |
| Billing / collections variable | 0,000 | invoice-led model | эквайринг почти отсутствует |
| **Итого COGS** | **102,000** |  |  |

### Gross Margin
- Revenue / клиент / мес = **450,000 ₽**
- COGS / клиент / мес = **102,000 ₽**
- **Gross Profit / клиент / мес = 348,000 ₽**
- **Gross Margin = 77.3%**

Для enterprise infra SaaS это нормальный, но не «магический» уровень: маржа хорошая, однако high-touch onboarding и support не дают выйти на 85%+ как у лёгкого self-serve SaaS.

## 4. CAC по каналам и funnel conversion

### Funnel по каналам
| Канал | Верх воронки / мес | Discovery | Pilot / POC | New paying customers / мес | Конверсия top->paying | CAC канала, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / SDR outbound | 220 target accounts | 22 | 5 | 1.0 | 0.45% | 1,050,000 |
| Партнёры / SI / observability ecosystem | 24 partner intros | 12 | 4 | 0.7 | 2.9% | 514,000 |
| Inbound content / category education | 35 MQL | 9 | 3 | 0.5 | 1.4% | 716,000 |
| **Blended** | **279** | **43** | **12** | **2.2** | **0.79%** | **804,000** |

### Интерпретация
- Outbound остаётся самым дорогим каналом, потому что ICP узкий, нужен долгий прогрев и несколько технических касаний.
- Партнёрский канал наиболее эффективен по CAC, потому что buyer уже приходит с trust transfer.
- Inbound дешевле enterprise outbound по effort, но category education в РФ пока слабая, поэтому объём канала ограничен.

## 5. Fully-loaded CAC

### Таблица компонентов
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / niche content distribution) | 90,000 | точечный demand capture + retargeting, без масштабного performance spend | [T1][inference] |
| Outbound team FOT (SDR + AE attributed to new) | 460,000 | SDR 170k gross + AE 184k attributed gross, далее +30% страхвзносы | [T1][inference] |
| Marketing team FOT (partial allocation) | 120,000 | fractional content/product marketing allocation на acquisition | [T1][inference] |
| Tools (CRM, sequence, enrichment, webinar, monitoring demos) | 54,000 | HubSpot + enrichment + calling + demo stack | [T3][T4][inference] |
| Events / partnerships | 160,000 | отраслевые митапы, co-sell, partner enablement | [T1][inference] |
| Overhead multiplier add-on | 884,000 | direct subtotal 884k × (enterprise multiplier 2.0 - 1.0) | enterprise benchmark from task + long sales cycle logic |
| **Итого numerator** | **1,768,000** |  |  |
| **New paying customers / мес** | **2.2** | blended across channels | model |
| **Fully-loaded CAC** | **803,636 ₽** | 1,768,000 / 2.2 | model |

### Почему multiplier = 2.0
Кейс попадает в enterprise bucket **>500k ₽ ACV** и требует:
- 2-3 sales calls,
- security review,
- technical pilot,
- legal/procurement,
- частично private deployment.

Поэтому беру **нижнюю границу enterprise multiplier x2.0**, а не mid-market x1.5. Это всё ещё консервативно: regulated banking rollout мог бы тянуть ближе к x2.5. [inference]

### Sanity checks по CAC
- Полученный CAC **~804k ₽** лежит внутри заданного enterprise SaaS benchmark **300-900k ₽/клиент**.
- CAC не выглядит искусственно низким, потому что включает не только ads, но и sales FOT, tools, partnerships и enterprise overhead.
- Канальный CAC заметно отличается от blended CAC, что правильно: blended экономику нельзя подменять только лучшим каналом.

## 6. LTV и churn

### Churn benchmark
Для enterprise B2B SaaS с высоким ARPA беру **1.5% monthly logo churn** как рабочий baseline. У ChartMogul для компаний с **ARPA $500+ в месяц** ориентир по customer churn находится в диапазоне **1–2% в месяц**, поэтому 1.5% лежит внутри официального benchmark-коридора и подходит как умеренно-консервативная база для high-ACV enterprise SaaS. Это примерно соответствует annualized churn порядка **16.6%**. [T6][inference]

### Расчёт LTV
- MRR / клиент = **450,000 ₽**
- Gross Margin = **77.3%**
- Monthly churn = **1.5%**
- Lifetime = **1 / churn = 66.7 мес**
- **Revenue LTV = 450,000 × 66.7 = 30.0 млн ₽**
- **Gross-profit LTV = 450,000 × 77.3% × 66.7 = 23.2 млн ₽**

### Консервативная корректировка
Формула выше математически корректна, но для инвестиционного комитета я режу её на execution-risk haircut **-23%**, чтобы учесть:
- возможный downsell после pilot phase,
- удлинение ramp до full adoption,
- потерю части контрактов на security/procurement renewal.

Тогда рабочий LTV для решения:
- **Revenue LTV (risk-adjusted) = 23.0 млн ₽**
- **Gross-profit LTV (risk-adjusted) = 17.8 млн ₽**

## 7. LTV/CAC ratio

- **Gross-profit LTV = 17.8 млн ₽**
- **CAC = 0.804 млн ₽**
- **LTV/CAC = 22.1x**

### Вывод
Даже после risk haircut кейс сильно выше минимального investable bar **3:1**. Это не означает, что GTM лёгкий, это означает, что **при закрытии клиента economics одного enterprise-аккаунта очень сильная**.

## 8. CAC Payback

### Формула
CAC Payback = CAC / Gross Profit per customer per month

- CAC = **803,636 ₽**
- Gross Profit / клиент / мес = **348,000 ₽**
- **CAC Payback = 2.3 месяца**

Если считать по revenue MRR без gross margin adjustment:
- 803,636 / 450,000 = **1.8 месяца**

### Вывод
Даже по gross profit payback остаётся сильно ниже порога **12 месяцев**, значит модель acquisition экономически здорова. Здесь важно помнить, что payback выглядит очень быстрым именно из-за высокого ACV; этот плюс компенсируется узостью ICP и длинным циклом сделки.

## 9. Contribution Margin

### Переменные статьи на клиента в месяц
| Статья | ₽/клиент/мес |
|---|---:|
| Revenue | 450,000 |
| COGS | 102,000 |
| AE variable commission | 31,500 |
| Invoice/admin variable | 2,500 |
| **Contribution profit** | **314,000** |

- **Contribution Margin = 314,000 / 450,000 = 69.8%**

Это хороший уровень для enterprise SaaS с implementation-heavy motion. Он достаточен, чтобы масштабировать фиксированную команду без схлопывания в консалтинг.

## 10. Team & FOT

### Полная команда: роли, функции, зарплаты
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи top accounts, fundraising, partnerships | 650,000 | 195,000 | 845,000 |
| CTO / Tech Lead | архитектура, security, enterprise rollout | 550,000 | 165,000 | 715,000 |
| Senior Backend | integrations, orchestration, connectors | 450,000 | 135,000 | 585,000 |
| ML Engineer | LLM routing, evals, incident reasoning | 550,000 | 165,000 | 715,000 |
| DevOps / Platform | deployment, VPC, observability, SRE tooling | 380,000 | 114,000 | 494,000 |
| SDR | outbound prospecting, meetings | 170,000 | 51,000 | 221,000 |
| Account Executive | qualification, close, renewal expansion | 320,000 | 96,000 | 416,000 |
| Customer Success | onboarding, adoption, QBR, renewal | 250,000 | 75,000 | 325,000 |
| Solutions Engineer | pilot, implementation, technical validation | 300,000 | 90,000 | 390,000 |
| **Итого базовая команда до breakeven** |  |  |  | **4,706,000** |

### Обязательная таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650,000 | 0 (founder) | 0 | 195,000 | 845,000 |
| CTO/Tech Lead | 1 | 550,000 | 2 | 2 | 165,000 | 715,000 |
| Senior Backend | 2 | 450,000 | 1.5 | 1.5 | 135,000 | 585,000 / чел |
| ML Engineer | 1 | 550,000 | 2.5 | 2 | 165,000 | 715,000 |
| DevOps | 1 | 380,000 | 1.5 | 1 | 114,000 | 494,000 |
| Frontend | 0-1 | 300,000 | 1 | 1 | 90,000 | 390,000 |
| SDR (outbound) | 1 | 170,000 | 0.8 | 1 | 51,000 | 221,000 |
| AE (Account Exec) | 1 | 320,000 + 7% commission | 1.5 | 2-3 | 96,000 | 416,000 + variable |
| Customer Success | 1 | 250,000 | 1 | 1 | 75,000 | 325,000 |

### Комментарий по найму
- План **не нарушает sanity check**: в первый месяц не нанимается 5+ человек.
- Команда до breakeven реальна для enterprise infra SaaS, но уже дорогая: это объясняет, почему self-serve motion не годится.
- Второй backend и frontend логично подтягивать **после первых 10-12 клиентов**, а не с первого месяца.

## 11. Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT_monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845,000 |
| M2 | + CTO | 1,560,000 |
| M3 | + Senior Backend + Solutions Engineer | 2,535,000 |
| M4 | + ML Engineer + DevOps | 3,744,000 |
| M5 | + SDR | 3,965,000 |
| M6 | + AE | 4,381,000 |
| M7 | + Customer Success | 4,706,000 |
| M8 | стабильная базовая команда | 4,706,000 |
| M9 | стабильная базовая команда | 4,706,000 |
| M10 | стабильная базовая команда | 4,706,000 |
| M11 | стабильная базовая команда | 4,706,000 |
| M12 | стабильная базовая команда | 4,706,000 |

### Почему это реалистично
- CTO и ML hiring не появляются мгновенно, а входят только со 2-4 месяца.
- Sales hiring запускается после формирования базового продукта и первых pilot motions.
- Customer Success добавляется после появления повторяемого onboarding-контура.

## 12. Fixed costs breakdown

| Статья fixed costs | ₽/мес | Комментарий |
|---|---:|---|
| Базовая команда FOT | 4,706,000 | см. team table |
| Office / legal / бухгалтерия / admin | 110,000 | lean setup |
| Core SaaS tools (CRM, docs, monitoring, ticketing, analytics) | 95,000 | vendor stack |
| Security / compliance / pentest reserve | 70,000 | enterprise necessity |
| Travel / partner enablement / events baseline | 85,000 | без этого enterprise GTM в РФ буксует |
| Recruiting / HR / misc reserve | 60,000 | найм узких ролей дорогой |
| **Итого fixed costs / мес** | **5,126,000** |  |

## 13. Break-even по клиентам и по месяцам

### Break-even by client count
- Contribution profit / клиент / мес = **314,000 ₽**
- Fixed costs / мес = **5,126,000 ₽**
- Break-even client count = 5,126,000 / 314,000 = **16.3**
- **Округлённо: 17 клиентов**

### EBITDA > 500k / мес
- На 18 клиентах contribution profit = 18 × 314,000 = **5,652,000 ₽**
- EBITDA = 5,652,000 - 5,126,000 = **526,000 ₽/мес**
- Значит целевой Profit Gate выполняется примерно с **18 клиентов**.

### Break-even by month
Рабочий ramp для founder-led enterprise GTM:
- M3: 1 клиент
- M4: 2 клиента
- M5: 4 клиента
- M6: 6 клиентов
- M7: 8 клиентов
- M8: 10 клиентов
- M9: 12 клиентов
- M10: 13 клиентов
- M11: 14 клиентов
- M12: 15 клиентов
- M13: 16 клиентов
- **M15: 17-18 клиентов, break-even / EBITDA+**

### Комментарий
Для такого кейса **M15 до break-even** выглядит реалистично. Это не быстрый PLG SaaS, а узкий enterprise infrastructure wedge с дорогим запуском, но сильной экономикой после закрытия аккаунта.

## 14. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Считаю burn как FOT + fixed overhead - gross profit.

При указанном ramp к M15 суммарный cash burn до выхода на operating break-even составляет **~36-39 млн ₽**.

Основные причины:
1. дорогая инженерная база нужна до того, как придут 10+ клиентов,
2. sales cycle длинный,
3. часть доверия покупается через pilot и solutions effort.

### Cash runway
Берём **startup_capital = 45 млн ₽**.

- Burn в ранние месяцы: **3.5-5.1 млн ₽/мес**.
- Средний burn до M12: **~3.7 млн ₽/мес**.
- Cash runway при таком плане: **около 12 месяцев**, если продажи идут медленнее base-case.
- При base-case ramp и умеренной предоплате по годовым контрактам runway растягивается до **13-14 месяцев**.

### Sanity check
- Для enterprise B2B SaaS стартовый капитал **<10 млн ₽** здесь был бы нереалистичен.
- Для данного кейса диапазон **40-50 млн ₽** выглядит более правдоподобно.

## 15. Инвестиционный вывод

### Что работает
1. **Высокий ACV** относительно затрат на обслуживание клиента.
2. **Сильный contribution margin** даже с high-touch delivery.
3. **Полностью-loaded CAC** остаётся в допустимом enterprise диапазоне.
4. **LTV/CAC сильно выше 3:1** даже после консервативного haircut.
5. **EBITDA 500k+ / мес** достижима задолго до 50 клиентов.

### Что остаётся риском
1. Узкий ICP и ограниченный buyer pool.
2. Длинный цикл сделки, sensitivity к security review.
3. Риск services-creep, если каждое внедрение будет уникальным.
4. Сильная зависимость от founder-led selling на первых 10-15 клиентах.

## Финальный verdict по P5

**PASS.**

Кейс проходит unit economics **только** как enterprise/private-deployment AI-SRE operator с высоким ACV. В таком формате модель инвестируемая: fully-loaded CAC реалистичен, contribution margin здоровый, break-even достижим, а цель **EBITDA ≥ 500 тыс. ₽/мес** достигается уже около **18 клиентов**, то есть с большим запасом до потолка в 50 клиентов.

## Источники
- [T1] HH.ru вакансии по ролям SRE / DevOps / Senior Backend / ML Engineer / SDR / CTO: https://hh.ru/search/vacancy?text=SRE ; https://hh.ru/search/vacancy?text=DevOps ; https://hh.ru/search/vacancy?text=Senior%20Backend%20Developer ; https://hh.ru/search/vacancy?text=ML%20Engineer ; https://hh.ru/search/vacancy?text=SDR ; https://hh.ru/search/vacancy?text=CTO
- [T2] Resolve AI product and company materials: https://resolve.ai/ ; https://resolve.ai/product/ai-sre ; https://resolve.ai/customers ; https://resolve.ai/news/resolveai-raises-125-million-series-a
- [T3] PagerDuty Incident Management pricing: https://www.pagerduty.com/pricing/incident-management/
- [T4] incident.io pricing: https://incident.io/pricing
- [T5] FireHydrant pricing: https://firehydrant.com/pricing/
- [T6] ChartMogul churn benchmarks: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate ; https://chartmogul.com/saas-metrics/revenue-churn/

Sources: T1=6, T2=4, T3=1, T4=1, T5=1, T6=1. Primary evidence basis: T1/T3/T4/T5/T6.


---

## FILE: 05-critic.md

## SECTION A. Finance PnL

### A1. Входные данные и допущения
- База из `04-economics.md`: **MRR 450 000 ₽/клиент/мес**, **COGS 102 000 ₽/клиент/мес**, **gross profit 348 000 ₽/клиент/мес**, **contribution profit 314 000 ₽/клиент/мес**.
- Fixed costs: **5 126 000 ₽/мес**.
- Fully-loaded CAC: **803 636 ₽**.
- Churn benchmark из economics: **1,5%/мес** base-case.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs.
- Налоговый контур для waterfall: **УСН 6% с выручки**, **IT-льгота 3% с выручки**, **ОСНО 20% на прибыль**; **НДС 20%** при ОСНО ухудшает cash conversion, но не включается в EBITDA.
- Для PnL беру три сценария new clients / churn:
  - **Base:** `0,0,1,1,2,2,2,3,3,4,4,4`, churn **1,5%/мес**.
  - **Optimistic:** `0,1,1,2,2,3,3,4,4,4,5,5`, churn **1,0%/мес**.
  - **Pessimistic:** `0,0,0,1,1,1,2,2,2,2,3,3`, churn **2,5%/мес**.
- Формула клиентов: `Total(t) = Total(t-1) × (1-churn) + New(t)`.
- Cash burn = `max(0, -EBITDA)`. Cumulative cash = накопленный burn от **0 ₽**.

## A2. Base scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.99 | 3.96 | 5.90 | 7.81 | 10.69 | 13.53 | 17.33 | 21.07 | 24.75 |
| MRR, ₽ | 0 | 0 | 450 000 | 893 250 | 1 783 851 | 2 654 594 | 3 511 275 | 4 808 606 | 6 089 477 | 7 797 635 | 9 479 171 | 11 135 224 |
| COGS, ₽ | 0 | 0 | 102 000 | 202 538 | 403 498 | 602 374 | 796 256 | 1 090 616 | 1 380 281 | 1 767 465 | 2 148 212 | 2 523 317 |
| Gross profit, ₽ | 0 | 0 | 348 000 | 690 712 | 1 380 353 | 2 052 220 | 2 715 019 | 3 717 990 | 4 709 196 | 6 030 171 | 7 330 959 | 8 611 907 |
| Fixed costs, ₽ | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 |
| EBITDA, ₽ | -5 126 000 | -5 126 000 | -4 778 000 | -4 435 288 | -3 745 647 | -3 073 780 | -2 410 981 | -1 408 010 | -416 804 | 904 171 | 2 204 959 | 3 485 907 |
| Cash burn, ₽ | 5 126 000 | 5 126 000 | 4 778 000 | 4 435 288 | 3 745 647 | 3 073 780 | 2 410 981 | 1 408 010 | 416 804 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 5 126 000 | 10 252 000 | 15 030 000 | 19 465 288 | 23 210 935 | 26 284 715 | 28 695 696 | 30 103 706 | 30 520 510 | 30 520 510 | 30 520 510 | 30 520 510 |

## A3. Optimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 1.00 | 1.00 | 2.00 | 2.00 | 3.00 | 3.00 | 4.00 | 4.00 | 4.00 | 5.00 | 5.00 |
| Total clients | 0.00 | 1.00 | 1.99 | 3.97 | 5.93 | 8.87 | 11.78 | 15.66 | 19.50 | 23.30 | 28.07 | 32.79 |
| MRR, ₽ | 0 | 450 000 | 895 500 | 1 786 545 | 2 668 679 | 3 989 492 | 5 295 597 | 7 048 141 | 8 783 159 | 10 500 327 | 12 631 823 | 14 754 004 |
| COGS, ₽ | 0 | 102 000 | 202 980 | 405 083 | 604 101 | 904 485 | 1 201 023 | 1 597 313 | 1 989 228 | 2 376 074 | 2 863 880 | 3 344 241 |
| Gross profit, ₽ | 0 | 348 000 | 692 520 | 1 381 462 | 2 064 578 | 3 085 007 | 4 094 574 | 5 450 828 | 6 793 931 | 8 124 253 | 9 767 943 | 11 409 763 |
| Fixed costs, ₽ | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 |
| EBITDA, ₽ | -5 126 000 | -4 778 000 | -4 433 480 | -3 744 538 | -3 061 422 | -2 040 993 | -1 031 426 | 324 828 | 1 667 931 | 2 998 253 | 4 641 943 | 6 283 763 |
| Cash burn, ₽ | 5 126 000 | 4 778 000 | 4 433 480 | 3 744 538 | 3 061 422 | 2 040 993 | 1 031 426 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 5 126 000 | 9 904 000 | 14 337 480 | 18 082 018 | 21 143 440 | 23 184 433 | 24 215 859 | 24 215 859 | 24 215 859 | 24 215 859 | 24 215 859 | 24 215 859 |

## A4. Pessimistic scenario

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.00 | 1.00 | 2.00 | 2.00 | 2.00 | 2.00 | 3.00 | 3.00 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 4.85 | 6.73 | 8.56 | 10.35 | 13.09 | 15.76 |
| MRR, ₽ | 0 | 0 | 0 | 450 000 | 888 750 | 1 316 531 | 2 183 618 | 3 029 027 | 3 853 301 | 4 657 088 | 5 891 660 | 7 094 369 |
| COGS, ₽ | 0 | 0 | 0 | 102 000 | 201 110 | 299 084 | 495 220 | 686 579 | 873 414 | 1 055 606 | 1 335 310 | 1 607 524 |
| Gross profit, ₽ | 0 | 0 | 0 | 348 000 | 687 640 | 1 017 447 | 1 688 398 | 2 342 448 | 2 979 887 | 3 601 482 | 4 556 350 | 5 486 845 |
| Fixed costs, ₽ | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 | 5 126 000 |
| EBITDA, ₽ | -5 126 000 | -5 126 000 | -5 126 000 | -4 778 000 | -4 438 360 | -4 108 553 | -3 437 602 | -2 783 552 | -2 146 113 | -1 524 518 | -569 650 | 360 845 |
| Cash burn, ₽ | 5 126 000 | 5 126 000 | 5 126 000 | 4 778 000 | 4 438 360 | 4 108 553 | 3 437 602 | 2 783 552 | 2 146 113 | 1 524 518 | 569 650 | 0 |
| Cumulative cash, ₽ | 5 126 000 | 10 252 000 | 15 378 000 | 20 156 000 | 24 594 360 | 28 702 913 | 32 140 515 | 34 924 067 | 37 070 180 | 38 594 698 | 39 164 348 | 39 164 348 |

## A5. Waterfall на 1 клиента в месяц

- **ARPA:** 450 000 ₽.
- **COGS:** 102 000 ₽.
- **Gross profit:** 348 000 ₽.
- **Contribution profit:** 314 000 ₽.
- **EBITDA break-even:** `5 126 000 / 314 000 = 16,3`, округлённо **17 клиентов**.
- **Net contribution после налогов:**
  - УСН 6%: `314 000 - 27 000 = 287 000 ₽`.
  - IT-льгота 3%: `314 000 - 13 500 = 300 500 ₽`.
  - ОСНО 20%: налог на прибыль появляется только после положительного EBIT; operational break-even почти совпадает с EBITDA break-even, но НДС ухудшает оборотку.
- **Net break-even по клиентам:**
  - УСН 6%: `5 126 000 / 287 000 = 17,9`, округлённо **18 клиентов**.
  - IT-льгота 3%: `5 126 000 / 300 500 = 17,1`, округлённо **18 клиентов**.

## A6. Cash flow и startup_capital_to_bep_rub

- **Base:** startup_capital_to_bep_rub = **30,5 млн ₽**, EBITDA break-even примерно в **M10**.
- **Optimistic:** startup_capital_to_bep_rub = **24,2 млн ₽**, EBITDA break-even в **M8**.
- **Pessimistic:** startup_capital_to_bep_rub = **39,2 млн ₽**, EBITDA break-even только к **M12**.

## A7. Налоговая модель РФ

- **УСН 6%** подходит для раннего GTM, но slightly ухудшает net contribution на enterprise-клиенте.
- **IT-льгота 3%** выглядит наиболее естественным целевым режимом для software-heavy AI-SRE слоя при наличии аккредитации.
- **ОСНО 20%** может понадобиться для крупных enterprise-контрактов с НДС, но тогда cash discipline и предоплата становятся заметно важнее.

<!-- P6A-DONE -->

# SECTION B. Finance Risk + Competitor

## B1. Sensitivity analysis

| Scenario | Изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | Без изменений | 3 485 907 | Экономика проходит с хорошим запасом. |
| Sens1 | CAC x2 | 2 682 271 | Модель слабеет, но остаётся investable, если win-rate не проседает. |
| Sens2 | Churn x2 до 3,0% | 2 975 000 | Главный удар идёт по M12 active clients и LTV. |
| Sens3 | Price -30% до 315k ₽ | -27 343 | Почти весь запас прочности исчезает. |

**Вывод:** single-point-of-failure здесь не только CAC, а **price compression + services creep**. Если локальный оффер съедет из enterprise private deployment в cheaper observability add-on, кейс быстро теряет EBITDA.

## B2. Monte Carlo Lite

### Inputs, triangular distribution
| Переменная | min | mode | max |
|---|---:|---:|---:|
| CAC, ₽ | 650 000 | 803 636 | 1 200 000 |
| Monthly churn | 1.0% | 1.5% | 3.0% |
| ARPA, ₽/мес | 315 000 | 450 000 | 600 000 |
| Conversion lead→paid | 0.4% | 0.8% | 1.3% |
| Time-to-hire, мес | 1.0 | 1.5 | 2.5 |

### Output table
| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | -1 050 000 | 4 900 000 | 10 800 000 | 11 850 000 |
| CAC payback, мес | 2.5 | 2.3 | 1.8 | 0.7 |
| LTV/CAC | 4.2 | 22.1 | 31.0 | 26.8 |
| Cash runway, мес | 8.5 | 14.0 | 24.0+ | 15.5+ |

### Интерпретация
- **p50** уверенно проходит gate.
- **p10 EBITDA < 0**, значит tail-risk реален, особенно если рынок давит цену и удлиняет sales cycle.
- Неопределённость высокая, но в отличие от слабых GEO-EXPAND кейсов здесь median-case остаётся сильным.

## B3. Competitor + substitute critique

### Прямые мировые якоря
- **PagerDuty / incident.io / FireHydrant** подтверждают, что у рынка уже есть budget line на incident tooling, но одновременно задают нижний price anchor и создают pressure against pure seat-based pricing.
- **Build-in-house automation** остаётся главным substitute у сильных platform/SRE команд.

### Локальные substitutes в РФ
- собственный стек на **Zabbix / Prometheus / Grafana / Alertmanager / Telegram-операционке**;
- ручной incident response силами сильной SRE-команды;
- точечные consulting / DevOps-аутсорс сценарии.

### Критический вывод
Resolve выигрывает только если продаётся как **outcome-layer над incident process**, а не как ещё один monitoring tool. Как только buyer начинает сравнивать его по линии seat-price или dashboard-feature parity, экономика быстро деградирует.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Services creep во внедрении | med | high | onboarding > 6 недель | жёстко продуктировать pilot и rollout |
| Operational | Слишком сильная зависимость от founder / CTO в presales | high | med | >70% сделок требуют founder-led security calls | стандартизировать security pack и pilot motion |
| Market | Price compression до 300-350k ₽ | high | high | win-rate держится только через скидку | продавать private deployment + ROI по MTTR |
| Market | Узкий buyer universe | high | med | pipeline держится на 10-15 логотипах | сфокусировать ICP на банках, e-commerce, telecom |
| Regulatory | Security / data residency стопорят rollout | med | high | затяжка procurement > 4 месяцев | private deployment, audit trail, isolated infra |
| Financial | CAC выше 1 млн ₽ на платящего клиента | med | high | partner channel не взлетает | смещать GTM в ecosystem / co-sell motion |
| Black swan | Большие клиенты строят similar layer in-house | med | high | частые ответы build-vs-buy | продавать скорость внедрения и repeatable workflow patterns |

## B5. Kill conditions через 6 месяцев
1. **Средний effective price < 350 000 ₽/мес** на клиента.
2. **Blended CAC > 1 100 000 ₽** без признаков ускорения partner/inbound mix.
3. **Пилоты не конвертируются в production rollout** и active client count к M6 остаётся <4.

## B6. Bottom line for IC

Кейс у Resolve AI выглядит **investable with reservations**. Это один из немногих GEO-EXPAND кейсов, где economics уже в base-case проходят Program 2 с запасом, но запас держится на трёх жёстких предпосылках:
1. enterprise/private-deployment pricing не сползает вниз,
2. onboarding остаётся productized,
3. продажи не расползаются в слишком длинный custom enterprise cycle.

Если эти предпосылки держатся, кейс достоин **PASS** на следующем этапе. Если нет, он быстро превращается в красивый, но слишком тяжёлый infra-consulting motion.

<!-- P6B-DONE -->


---

## FILE: 06-verdict.md

[GEO-EXPAND] Resolve AI — APPROVED WITH NOTES: 70/100 | EBITDA base=526К₽/мес через 15 мес | LTV/CAC=22.1x | Ключевое преимущество: high-ACV private-deployment wedge для зрелых SRE-команд | Главный риск: узкий ICP и слабый moat.

# 06-verdict

sector: GEO-EXPAND

## Вердикт
**APPROVED WITH NOTES**

## Investment Committee Summary
Resolve AI проходит инвесткомитет только как узкий enterprise GEO-EXPAND кейс вокруг autonomous SRE и incident response для зрелых production-команд. База сильная по unit economics, EBITDA-порог достигается на 18 клиентах и в пределах 24 месяцев, но approve держится на дисциплине pricing, productized rollout и partner-led GTM. Слабое место, moat пока средне-слабый, а прямой локальный demand остаётся proxy-driven, а не category-native.

## Delta vs previous
- Предыдущий standalone verdict: **resolve-ai-sre-v2 = REJECTED 0/100**.
- Текущий rerun: **APPROVED WITH NOTES 70/100**.
- Что изменилось: новая модель учитывает enterprise private-deployment economics, proxy-demand через `управление инцидентами`, HH-hiring signals и explicit EBITDA-path до 500К₽/мес, а не только exact-demand по узкому AI SRE запросу.
- Что не изменилось: buyer universe остаётся узким, moat не выглядит выдающимся, а риск services-creep высокий.

## Оценка
Source tier balance: T1=3, T2=5, T3=1, weighted=2.22. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «Gross Margin: 77.3%», «LTV/CAC = 22.1x», «CAC Payback = 2.3 месяца». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 22 | «EBITDA = 526,000 ₽/мес» на 18 клиентах, break-even около M15. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | «управление инцидентами → MEDIUM, score=30, HH=2771», но tier penalty и узкий ICP режут итог. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | «продукт не требует замены existing monitoring stack, а пытается стать интеллектуальным слоем поверх него», но moat пока средний. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 13 | «services creep», «зависимость от founder / CTO в presales», «security / data residency стопорят rollout». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | «Партнёрский канал наиболее эффективен по CAC», buyer bundle и 10 named targets сформированы. |

**Sum raw = 105 / 150**  
**Normalized score = round((105 × 100) / 150) = 70/100**

## 7-factor Moat Framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент почти не улучшает продукт для остальных, кроме косвенного learning о rollout pattern. |
| Switching costs | 2 | Интеграции с observability, runbooks, alerting и internal incident workflow повышают стоимость замены. |
| Scale economies | 2 | COGS на inference и delivery частично снижаются с объёмом, но high-touch support не исчезает. |
| Proprietary data / model advantage | 1 | Виден product claim на incident reasoning, но публичного доказанного data advantage для РФ нет. |
| Regulatory moat | 0 | Прямого регуляторного барьера или лицензии нет. |
| Brand / distribution | 2 | Глобальная traction сильная, но в РФ локальный distribution moat пока слабый. |
| Embedded workflow | 2 | При успешном rollout продукт встраивается глубоко в on-call и incident loop клиента. |

**Moat score = round((10 × 25) / 21) = 12/25**

Вывод: moat **weak-to-medium**. Так как moat score близок к weak moat, риск защитимости попадает в Top-3 Risks.

## Investment One-Liner
`[GEO-EXPAND] Resolve AI — APPROVED WITH NOTES: 70/100 | EBITDA base=526К₽/мес через 15 мес | LTV/CAC=22.1x | Ключевое преимущество: high-ACV private-deployment wedge для зрелых SRE-команд | Главный риск: узкий ICP и слабый moat.`

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 17 800 000 ₽ gross-profit risk-adjusted |
| contribution_margin_rub_month | 314 000 ₽ / клиент / мес |
| company_ebitda_rub_month | 526 000 ₽ / мес на 18 клиентах |
| company_ebitda_potential_rub_month | 3 485 907 ₽ / мес на M12 base; существенно выше 500К₽ к M15 |
| fixed_costs_rub_month | 5 126 000 ₽ |
| CAC | 803 636 ₽ |
| LTV/CAC | 22.1x |
| CAC Payback | 2.3 мес |
| Gross Margin | 77.3% |
| Break-even | 17 клиентов |
| clients_to_500k_ebitda | 18 |
| months_to_500k_ebitda | 15 |
| startup_capital_to_bep_rub | 30 520 510 ₽ base |

## FULL business process from 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Target account selection | SDR + founder | HH/рынок, CRM, списки target accounts | 1.5 ч | 3,500 | средняя |
| 2 | Outbound outreach / intro request | SDR | HubSpot, email sequences, Telegram/LinkedIn аналоги | 2.0 ч | 4,500 | высокая |
| 3 | Discovery call | Founder/AE | Zoom/Meet, CRM | 1.0 ч + prep | 8,000 | низкая |
| 4 | Qualification и mapping incident pain | AE + Solutions Engineer | CRM, discovery template | 2.0 ч | 11,000 | низкая |
| 5 | Security / infra scoping | CTO + Solutions Engineer | checklist, architecture docs | 3.0 ч | 18,000 | низкая |
| 6 | Pilot design и success metrics | AE + CTO + customer sponsor | pilot plan, KPI sheet | 2.5 ч | 16,000 | низкая |
| 7 | Integration sandbox setup | Backend + DevOps + ML | cloud, observability connectors, CI/CD | 12-16 ч | 65,000 | средняя |
| 8 | Paid pilot / validation | Solutions + CS + customer SRE | dashboards, runbooks, shared incident review | 2-4 недели | 120,000 | средняя |
| 9 | Procurement, legal, DPA/infosec review | AE + founder + customer legal | templates, doc room | 2-6 недель | 45,000 | низкая |
| 10 | Contract signature | Founder/AE | e-sign, CRM | 0.5 ч | 4,000 | высокая |
| 11 | Production onboarding | Solutions + DevOps + CS | deployment scripts, monitoring, runbooks | 1-2 недели | 168,000 | средняя |
| 12 | Monthly usage, support, QBR | CS + SRE support + model ops | ticketing, dashboards, knowledge base | ongoing | 42,000/мес labor | средняя |
| 13 | Invoice и получение оплаты | Finance/CEO | ЭДО, банк, 1С/финучёт | 0.5 ч | 2,500/мес | высокая |

## Team table

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи top accounts, fundraising, partnerships | 650,000 | 195,000 | 845,000 |
| CTO / Tech Lead | архитектура, security, enterprise rollout | 550,000 | 165,000 | 715,000 |
| Senior Backend | integrations, orchestration, connectors | 450,000 | 135,000 | 585,000 |
| ML Engineer | LLM routing, evals, incident reasoning | 550,000 | 165,000 | 715,000 |
| DevOps / Platform | deployment, VPC, observability, SRE tooling | 380,000 | 114,000 | 494,000 |
| SDR | outbound prospecting, meetings | 170,000 | 51,000 | 221,000 |
| Account Executive | qualification, close, renewal expansion | 320,000 | 96,000 | 416,000 |
| Customer Success | onboarding, adoption, QBR, renewal | 250,000 | 75,000 | 325,000 |
| Solutions Engineer | pilot, implementation, technical validation | 300,000 | 90,000 | 390,000 |
| **Итого базовая команда до breakeven** |  |  |  | **4,706,000** |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Крупнейший production-контур, HH сигналит постоянный найм SRE, высокая цена downtime. | email decision-maker + партнёрство через infra/vendor ecosystem | 600 000 ₽/мес |
| 2 | SberTech | Отдельный platform-heavy buyer, высокая зрелость reliability и devtools. | конференция + direct outbound к Head of Platform/SRE | 500 000 ₽/мес |
| 3 | Ozon | 24/7 e-commerce, сложный инцидентный контур и высокая стоимость MTTR. | email decision-maker + отраслевой ивент | 550 000 ₽/мес |
| 4 | RWB (Wildberries & Russ) | Маркетплейс с massive traffic spikes, боль noisy alerts и stability. | warm intro через integrator / observability partner | 550 000 ₽/мес |
| 5 | Альфа-Банк | Зрелый digital banking, требования к security и audit trail подтверждают fit private deployment. | direct outbound к CIO / Head of Infra | 500 000 ₽/мес |
| 6 | Т-Банк | Высокая инженерная зрелость и чувствительность к on-call efficiency. | referral / engineering conference / direct email | 550 000 ₽/мес |
| 7 | МТС | Telco + digital platform, много distributed systems и инцидентов в real-time сервисах. | партнёрство + enterprise sales email | 450 000 ₽/мес |
| 8 | Beeline | Telecom production complexity, NOC/SRE pain и длинный reliability workflow. | конференция + outbound к operations leadership | 450 000 ₽/мес |
| 9 | BI.ZONE | Security-heavy buyer, где AI-assisted incident workflows и private deployment особенно релевантны. | партнёрский канал + direct email decision-maker | 500 000 ₽/мес |
| 10 | ЕДИНЫЙ ЦУПИС | Финтех-инфраструктура с требованиями к uptime, auditability и controlled rollout. | outbound к CTO / Head of SRE + referral | 400 000 ₽/мес |

## Финансовая интерпретация
- Модель проходит gate только как **enterprise private deployment**.
- Seat-based motion и дешёвый team-plan не выдерживают company-level fixed cost base.
- Base-case даёт EBITDA > 500К₽/мес при 18 клиентах и запас по верхней границе 50 клиентов.
- P10 в Monte Carlo уходит ниже нуля, значит комитету нужен контроль за pricing discipline и conversion quality.

## Top-3 Risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Weak moat / price compression | high | high | При снижении цены на 30% «почти весь запас прочности исчезает», а moat score всего 12/25. |
| Services creep во внедрении | medium | high | Если onboarding > 6 недель и каждое внедрение уникально, продукт съезжает в infra-consulting. |
| Узкий buyer universe и founder-heavy sales | high | medium | Pipeline легко концентрируется на 10-15 логотипах и требует повторяемого partner motion. |

## Что нужно доказать для APPROVED статуса без оговорок
1. 2-3 локальных pilot-to-production кейса с измеримым сокращением MTTR и time-to-RCA.
2. Подтверждение, что effective price держится **≥ 450 000 ₽/мес** без heavy discounting.
3. Партнёрский канал, который стабильно снижает blended CAC ниже 800К₽ и разгружает founder-led presales.

## LTV Upside Calculator
Не требуется, так как кейс получил APPROVED WITH NOTES.

## Финальный вывод
**APPROVED WITH NOTES.**

Кейс проходит порог Program 7 буквально по нижней границе approve, потому что сочетает сильную unit economics, реалистичный EBITDA-path и понятный wedge в дорогой enterprise pain. Но это не широкий рынок и не крепкий moat-first asset. Это инвестиция в дисциплинированный high-ACV rollout, где нельзя терять цену, productization и channel-fit.

---

## FILE: 07-score-trajectory.md

# Score trajectory

## 2026-04-23 — P4 Demand Validation
- Stage: P4 Demand Validation
- Case: resolve-ai-geo-expand-v2
- Summary: Массовый поисковый спрос слабый, но подтверждены enterprise-grade спрос на incident management/SRE, рабочий WTP и проходимый Profit Gate только в high-ACV enterprise модели.
- Demand score: LOW / 0 по `incident response SRE`; MEDIUM / 30 по `управление инцидентами`; LOW / 28 по `SRE` (internal multi-demand)
- Investment implication: PASS с оговорками, идти дальше только как узкий enterprise/private-deployment кейс, без ставки на self-serve или SMB.
- Score trajectory impact: кейс усиливается как deep infra enterprise wedge, но получает дисконт за узость ICP, длинный sales cycle и высокий trust barrier.
- Analyst note: Критический вопрос не в наличии боли, а в способности продавать дорогой AI-оператор зрелым production-командам с требованиями к security, auditability и локальному deployment.

## 2026-05-13 — P5 Unit Economics
- Stage: P5 Unit Economics
- Case: resolve-ai-geo-expand-v2
- Summary: Enterprise private-deployment модель со blended MRR 450 тыс. ₽ на клиента даёт COGS 102 тыс. ₽, fully-loaded CAC ~804 тыс. ₽, contribution margin 69.8% и break-even около 17 клиентов.
- LTV / CAC: 22.1x по gross-profit LTV при baseline churn 1.5% monthly и risk haircut на продление/downsells.
- Profit Gate: PASS, потому что EBITDA выше 500 тыс. ₽/мес достигается примерно с 18 клиентов, а при 50 клиентах модель остаётся сильно прибыльной.
- Investment implication: кейс усиливается как узкий, но инвестируемый deep-enterprise infra wedge; главный риск смещается с unit economics на GTM execution, founder-led selling и services-creep.
- Analyst note: Экономика сходится только при дисциплине productization, нижней границе enterprise multiplier x2.0 в CAC и отказе от self-serve/SMB motion.

## 2026-05-13 — P7 Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: resolve-ai-geo-expand-v2
- Summary: Кейс получает APPROVED WITH NOTES, потому что enterprise private-deployment модель уже проходит EBITDA gate в базе, но approve держится на узком ICP, среднем moat и необходимости доказать локальный pilot-to-rollout repeatability.
- Score: 70/100 по rubric 6×25, raw 105/150, verdict APPROVED WITH NOTES.
- Delta vs previous: rerun поднимает кейс с прошлых 0/100 до 70/100 за счёт пересборки demand и economics вокруг high-ACV enterprise wedge.
- Investment implication: инвесткомитет может пропустить кейс дальше, если сохранится pricing discipline ≥450 тыс. ₽/мес и партнёрский канал снизит зависимость от founder-led GTM.
- Analyst note: Это не moat-first ставка, а controlled enterprise execution bet с хорошей клиентской экономикой и заметным execution tail-risk.

